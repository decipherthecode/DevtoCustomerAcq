# Classifier Prompt

**Version:** v1.0
**Last Updated:** [Date]
**Used In:** [e.g., "Support ticket triage", "Lead scoring", "Sentiment detection", "Content moderation"]
**Model:** claude-haiku-3-5 ← Use this! Classification is simple; haiku is 10× cheaper.

---

## Purpose

Assign input text to one or more predefined categories. This is your routing, tagging, and scoring engine. Use it any time you need Claude to make a decision about what something IS or WHERE it belongs.

---

## System Prompt

```
You are a precise text classification engine. Your job is to read a piece of text and assign it to one or more predefined categories.

## Core Rules
1. ONLY return the category name(s) exactly as they appear in the list provided. No extra words.
2. If the input clearly belongs to multiple categories, return all that apply, separated by commas.
3. If the input does not fit any category, return: UNKNOWN
4. Do not explain your reasoning unless explicitly asked.
5. Base your decision only on the text provided — do not make assumptions.
6. If you are less than 70% confident in a classification, return: UNCERTAIN:[your best guess]

## Output Format
- Single category: return the category name only. Example: POSITIVE
- Multiple categories: comma-separated. Example: BILLING, URGENT
- No match: UNKNOWN
- Low confidence: UNCERTAIN:POSITIVE
```

---

## User Message Template

```
Classify the following text into one of these categories:

## Categories
{{categories}}

## Text to Classify
{{input_text}}
```

---

## Example Category Sets

### 📧 Support Ticket Triage

```
## Categories
- BILLING: Questions about invoices, payments, refunds, or pricing
- BUG: Something in the product is broken or not working as expected
- FEATURE_REQUEST: The user wants a new feature or improvement
- ACCOUNT: Login issues, password reset, profile changes
- GENERAL_QUESTION: A general how-to or usage question
- URGENT: The issue is blocking the user from doing their work right now
```

### 😊 Sentiment Detection

```
## Categories
- POSITIVE: The user is happy, satisfied, or praising the product
- NEGATIVE: The user is unhappy, frustrated, or complaining
- NEUTRAL: The message is informational or has no clear positive/negative feeling
- MIXED: The message contains both positive and negative sentiments
```

### 🎯 Lead Intent Scoring

```
## Categories
- HOT: Ready to buy — mentions budget, timeline, or asks about pricing/contracts
- WARM: Interested but not ready — asks about features, requests a demo, follows up
- COLD: Just browsing — vague questions, no urgency, no specifics
- NOT_A_LEAD: Competitor, existing customer, job seeker, or spam
```

---

## Expected Output Format

Plain text only. Category name(s), exactly as listed. Nothing else.

```
BILLING, URGENT
```

---

## Example Input / Output

**Input:**

```
Hi, my team has been unable to log in since this morning and we have a product demo with a major client at 3pm today. This is really bad timing. Can someone help us ASAP?

Also, our last invoice seems to have been charged twice — can someone look into that too?
```

**Output:**

```
ACCOUNT, BILLING, URGENT
```

---

## Implementation Tips

```typescript
type Category = string; // Or use a TypeScript enum for your specific categories

async function classify(inputText: string, categories: string): Promise<Category[]> {
  const response = await client.messages.create({
    model: "claude-haiku-3-5",   // ← Haiku is 10× cheaper and fast enough for classification
    max_tokens: 64,              // ← Short — we only expect a category name back
    system: classifierSystemPrompt,
    messages: [{
      role: "user",
      content: `Classify the following text into one of these categories:\n\n## Categories\n${categories}\n\n## Text to Classify\n${inputText}`
    }]
  });

  const raw = response.content[0].text.trim();

  // Handle uncertain classifications
  if (raw.startsWith("UNCERTAIN:")) {
    const guess = raw.replace("UNCERTAIN:", "");
    console.warn(`Low-confidence classification: ${guess} — routing to human review`);
    return ["NEEDS_REVIEW"];
  }

  if (raw === "UNKNOWN") return ["UNCATEGORIZED"];

  return raw.split(",").map(c => c.trim());
}
```

---

## Adding Confidence Scores (Advanced)

To get a confidence score alongside the category, modify the system prompt:

```
Return your answer as JSON in this format:
{
  "categories": ["CATEGORY_1", "CATEGORY_2"],
  "confidence": 0.92
}
Where confidence is a number from 0.0 (no idea) to 1.0 (absolutely certain).
```

Then parse the JSON response instead of plain text.

---

## Known Failure Cases

| Input | Failure Mode | Fix |
|---|---|---|
| Category list is too long (> 15) | Claude picks the wrong one or returns UNKNOWN | Group into parent categories first, then sub-classify |
| Category names overlap (e.g., BUG vs TECHNICAL_ISSUE) | Claude alternates randomly | Make category names mutually exclusive; add descriptions to each |
| Very short input ("no" or "ok") | Returns UNKNOWN or UNCERTAIN | Add minimum input length validation before calling Claude |
| Input in multiple languages | Mixed results | Detect language first; use language-specific classifier if needed |

---

## Version History

| Date | Version | Change | Result |
|---|---|---|---|
| [Date] | v1.0 | Initial version | — |
