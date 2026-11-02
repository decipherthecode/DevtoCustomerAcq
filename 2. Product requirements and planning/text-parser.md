# Text / Email Parser Prompt

**Version:** v1.0
**Last Updated:** [Date]
**Used In:** [e.g., "Email import feature", "Document upload parser"]
**Model:** claude-sonnet-4-5 (switch to claude-haiku-3-5 if accuracy holds — much cheaper)

---

## Purpose

Extract specific, structured information from free-form text (emails, messages, documents, etc.) and return it as clean JSON that your app can use directly.

---

## System Prompt

```
You are a precise data extraction assistant. Your job is to read unstructured text and extract specific information, returning it as valid JSON.

## Rules
1. ONLY return a JSON object — no explanation, no preamble, no markdown fences.
2. If a field is not found in the text, return null for that field. Never guess or infer.
3. Do not add fields that were not asked for.
4. Preserve the original meaning — do not paraphrase or interpret beyond what is written.
5. If the input text is empty or clearly not relevant to the task, return: {"error": "Input not parseable", "reason": "[brief reason]"}
```

---

## User Message Template

```
Extract the following information from the text below.

## Fields to Extract
{{fields_to_extract}}

## Text to Parse
{{input_text}}

Return only a JSON object with the exact field names listed above.
```

### Example `{{fields_to_extract}}` value:

```
- sender_name: The name of the person who sent this message
- sender_email: Their email address
- meeting_requested: true if they are requesting a meeting, false otherwise
- proposed_date: Any date or time mentioned for the meeting (in ISO 8601 format if possible)
- preferred_times: Any time preferences mentioned (e.g., "mornings", "after 3pm")
- urgency: "high", "medium", or "low" based on tone
```

---

## Expected Output Format

```json
{
  "sender_name": "Sarah Johnson",
  "sender_email": "sarah@example.com",
  "meeting_requested": true,
  "proposed_date": "2026-10-20",
  "preferred_times": "mornings",
  "urgency": "medium"
}
```

---

## Example Input / Output

**Input:**

```
Hi there,

It was great meeting you at the conference last week! I'd love to catch up and discuss the project proposal I sent over. Would sometime next Tuesday morning work for you? I'm usually free before noon.

Best,
Sarah Johnson
sarah@acmecorp.com
```

**Output:**

```json
{
  "sender_name": "Sarah Johnson",
  "sender_email": "sarah@acmecorp.com",
  "meeting_requested": true,
  "proposed_date": null,
  "preferred_times": "Tuesday morning, before noon",
  "urgency": "low"
}
```

*(Note: `proposed_date` is null because "next Tuesday" is relative and we don't know today's date — a pre-processing step should resolve this before sending to Claude, or ask Claude to flag it.)*

---

## Implementation Tips

```typescript
async function parseText(inputText: string, fieldsToExtract: string): Promise<Record<string, unknown>> {
  const response = await client.messages.create({
    model: "claude-sonnet-4-5",
    max_tokens: 512,
    system: textParserSystemPrompt,
    messages: [{
      role: "user",
      content: `Extract the following information from the text below.\n\n## Fields to Extract\n${fieldsToExtract}\n\n## Text to Parse\n${inputText}\n\nReturn only a JSON object.`
    }]
  });

  try {
    return JSON.parse(response.content[0].text);
  } catch {
    // JSON parsing failed — log and return error
    console.error("Failed to parse AI output:", response.content[0].text);
    return { error: "Output was not valid JSON", raw: response.content[0].text };
  }
}
```

---

## Known Failure Cases

| Input | Failure Mode | Fix |
|---|---|---|
| Very long emails (> 4,000 words) | Claude may miss details at the end | Chunk the text into segments before passing to Claude |
| Non-English text | Fields may be partially extracted or wrong | Add language detection step; route to multilingual prompt variant |
| Ambiguous dates ("next week") | Returns null or wrong date | Inject today's date into the prompt: "Today is {{today_date}}" |
| HTML/code content in email | Claude may get confused by tags | Strip HTML before sending with a simple regex or library |

---

## Version History

| Date | Version | Change | Result |
|---|---|---|---|
| [Date] | v1.0 | Initial version | — |
