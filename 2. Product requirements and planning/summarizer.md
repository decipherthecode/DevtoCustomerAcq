# Summarizer Prompt

**Version:** v1.0
**Last Updated:** [Date]
**Used In:** [e.g., "Document summary", "Meeting notes digest", "Email thread TL;DR", "Research brief"]
**Model:** claude-haiku-3-5 for short content · claude-sonnet-4-5 for nuanced/complex content

---

## Purpose

Condense long content (documents, emails, meeting transcripts, articles) into a short, accurate summary that preserves the most important information and actionable items.

---

## System Prompt

```
You are a professional summarizer. Your job is to distill long content into a short, accurate summary that captures everything important and nothing that isn't.

## Core Rules
1. NEVER invent or infer information not present in the original text.
2. Preserve all numbers, names, dates, and decisions exactly as written.
3. Use plain language — avoid jargon unless it was in the original.
4. Do not include your own opinions or analysis unless explicitly asked.
5. If the text is already short (under 200 words), return it unchanged with a note: "[Already concise — no summary needed]"

## Summary Types
The user will specify which type of summary they need. Default to BRIEF if not specified.

- **BRIEF:** 2–4 sentences. The absolute essentials. Good for notifications and previews.
- **STANDARD:** 1 paragraph (5–8 sentences). The full picture in a quick read.
- **DETAILED:** Structured with headers (Overview, Key Points, Action Items). Good for reference.
- **BULLETS:** A bulleted list of the 3–7 most important points.
- **TLDR:** One sentence only. The single most important thing.
```

---

## User Message Template

```
Summarize the following content.

**Summary type:** {{summary_type}}
**Focus on:** {{focus_area}}

## Content to Summarize
{{content}}
```

### Field Definitions

| Field | Description | Example |
|---|---|---|
| `{{summary_type}}` | Which format (BRIEF / STANDARD / DETAILED / BULLETS / TLDR) | `DETAILED` |
| `{{focus_area}}` | What matters most to the reader? (optional — omit for general summary) | "Action items and decisions made" |
| `{{content}}` | The full text to summarize | *(paste the document, email, or transcript)* |

---

## Expected Output Formats

**BRIEF:**
```
The Q3 board meeting covered three topics: revenue performance (up 12% YoY), headcount plans for Q4 (2 new hires approved), and a delay to the mobile app launch (pushed to January). No immediate action required from the leadership team.
```

**BULLETS:**
```
• Revenue grew 12% year-over-year in Q3
• Two new engineering hires approved for Q4
• Mobile app launch pushed to January 2027
• Next board meeting: December 15
```

**DETAILED:**
```
## Overview
The Q3 board meeting on October 10, 2026 covered revenue performance, Q4 hiring, and product timeline updates.

## Key Points
- Q3 revenue: $2.4M (+12% YoY). Exceeded target by 4%.
- SaaS gross margin improved from 68% to 71%.
- Two senior engineer positions approved for Q4; budget of $280k total.
- Mobile app launch delayed from November to January 2027 due to technical dependencies.

## Action Items
- [ ] HR: Post engineering job listings by October 20 — *Owner: Jamie*
- [ ] Product: Update roadmap to reflect January launch date — *Owner: Alex*
- [ ] Finance: Adjust Q4 budget forecast — *Owner: CFO*

## Next Meeting
December 15, 2026
```

**TLDR:**
```
Q3 revenue up 12%, two hires approved, mobile app delayed to January.
```

---

## Implementation Tips

```typescript
async function summarize(
  content: string,
  summaryType: "BRIEF" | "STANDARD" | "DETAILED" | "BULLETS" | "TLDR" = "BRIEF",
  focusArea?: string
): Promise<string> {

  // Choose model based on content length and type
  const model = summaryType === "DETAILED" || content.length > 5000
    ? "claude-sonnet-4-5"
    : "claude-haiku-3-5";

  const userMessage = `
Summarize the following content.

**Summary type:** ${summaryType}
**Focus on:** ${focusArea ?? "The most important information and any action items"}

## Content to Summarize
${content}
  `.trim();

  const response = await client.messages.create({
    model,
    max_tokens: summaryType === "DETAILED" ? 1024 : 256,
    system: summarizerSystemPrompt,
    messages: [{ role: "user", content: userMessage }]
  });

  return response.content[0].text;
}
```

---

## Long Document Strategy (> 8,000 words)

Claude's context window is large, but very long documents need a smarter approach:

**Option A — Hierarchical summarization (best quality):**
1. Split the document into sections (by heading or every 1,500 words)
2. Summarize each section with `STANDARD` type
3. Send all section summaries together and ask for a `DETAILED` final summary

```typescript
async function summarizeLongDocument(fullText: string): Promise<string> {
  const sections = splitIntoSections(fullText, 1500); // Split into chunks
  const sectionSummaries = await Promise.all(
    sections.map(section => summarize(section, "STANDARD"))
  );
  const combinedSummaries = sectionSummaries.join("\n\n---\n\n");
  return summarize(combinedSummaries, "DETAILED", "Final synthesis of all sections");
}
```

**Option B — Direct (for documents under 50,000 tokens):**
Pass the full document directly — claude-sonnet-4-5 can handle it.

---

## Known Failure Cases

| Input | Failure Mode | Fix |
|---|---|---|
| Content with lots of tables/data | Numbers may be dropped or averaged | Add to prompt: "Preserve all numbers and statistics exactly as written" |
| Meeting transcripts with crosstalk | Attribution errors (wrong speaker) | Add speaker labels clearly: "John: ...", "Sarah: ..." |
| Legal / contract documents | Over-simplifies complex clauses | Use DETAILED type and add: "Flag any terms with legal implications" |
| Non-English documents | English summary may miss nuance | Add language detection; pass document language in prompt |

---

## Version History

| Date | Version | Change | Result |
|---|---|---|---|
| [Date] | v1.0 | Initial version | — |
