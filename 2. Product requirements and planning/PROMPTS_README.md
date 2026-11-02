# 📚 AI Prompt Library

> **What is this folder?**
> This is your prompt library — a collection of Claude AI prompts that power your product. Every prompt your app sends to Claude should live here as a `.md` file, version-controlled alongside your code.

---

## 🗂️ Folder Structure

```
/prompts
  PROMPTS_README.md          ← You are here
  /system                    ← System prompts (the AI's "personality" and rules)
      base-system.md         ← The default system prompt for your app
  /features                  ← One file per AI feature in your product
      text-parser.md         ← Extract structured info from free-form text
      content-generator.md   ← Generate written content (emails, posts, etc.)
      data-extractor.md      ← Pull specific fields out of messy data
      classifier.md          ← Sort input into categories
      summarizer.md          ← Condense long content into short summaries
  /experiments               ← Test new prompt ideas here before promoting to /features
  /archive                   ← Old prompt versions (don't delete — you may need to rollback)
```

---

## 📏 Prompt File Format (Always Use This)

Every prompt file in this library follows the same structure:

```
# [Prompt Name]

**Version:** v1.0
**Last Updated:** [Date]
**Used In:** [Feature name in your app]
**Model:** claude-sonnet-4-5 (or claude-haiku-3-5 for simple tasks)

## Purpose
[One sentence: what does this prompt do?]

## System Prompt
[The actual system prompt — this is what Claude reads before every conversation]

## User Message Template
[The template for the user's message — use {{variables}} for dynamic content]

## Expected Output Format
[Describe what Claude should return: JSON, plain text, markdown, etc.]

## Example Input / Output
[A real example so you can test quickly]

## Known Failure Cases
[What breaks this prompt? What inputs cause bad results?]

## Version History
[Date | Version | What changed | Result]
```

---

## ✅ Rules for Prompts in This Library

1. **One file per feature** — don't mix multiple unrelated tasks in one prompt
2. **Always version your prompts** — when you change a prompt, bump the version number and note what changed
3. **Test before shipping** — run at least 10 diverse inputs through any new or changed prompt
4. **Never put secrets in prompts** — no API keys, passwords, or real user PII in example sections
5. **Archive, don't delete** — move old prompt versions to `/archive` so you can roll back
6. **Comments are welcome** — use `<!-- comment -->` in the prompt file to explain design decisions

---

## 🚀 How to Use These Prompts in Code

### Basic API Call (JavaScript/TypeScript)

```typescript
import Anthropic from "@anthropic-ai/sdk";
import fs from "fs";

const client = new Anthropic();

// Load prompt from file (keep prompts version-controlled!)
const systemPrompt = fs.readFileSync("./prompts/features/text-parser.md", "utf8");

async function runAI(userInput: string) {
  const response = await client.messages.create({
    model: "claude-sonnet-4-5",       // Use claude-haiku-3-5 for cheaper/faster tasks
    max_tokens: 1024,
    system: systemPrompt,
    messages: [
      {
        role: "user",
        content: userInput,
      },
    ],
  });

  return response.content[0].text;
}
```

### With Variable Substitution

```typescript
function buildPrompt(template: string, variables: Record<string, string>): string {
  return Object.entries(variables).reduce(
    (prompt, [key, value]) => prompt.replace(`{{${key}}}`, value),
    template
  );
}

// Usage:
const userMessage = buildPrompt(
  "Parse this email: {{email_content}}\nUser timezone: {{timezone}}",
  {
    email_content: userInput,
    timezone: user.timezone,
  }
);
```

---

## 💰 Token Cost Quick Reference (Anthropic Claude, Oct 2026)

| Model | Input (per 1M tokens) | Output (per 1M tokens) | Best For |
|---|---|---|---|
| claude-opus-5-5 | ~$15 | ~$75 | Complex reasoning, nuanced writing |
| claude-sonnet-4-5 | ~$3 | ~$15 | Most product features (recommended default) |
| claude-haiku-3-5 | ~$0.80 | ~$4 | Classification, simple extraction, high-volume tasks |

**Rule of thumb:** 1,000 tokens ≈ 750 words. Most prompts + responses = 500–2,000 tokens.

---

*Library started: [Date] | Maintained by: [Your name]*
