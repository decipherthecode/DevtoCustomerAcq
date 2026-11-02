# HOW TO FILL OUT THIS FILE

> Part of `Prompt_Versioning.md` (Sections 4-6). Copy this file once for **each** prompt, rename it to `<prompt-id>.md`, and delete this box.

1. **Copy** this file into the right folder (for example `prompts/agents/`). Name it with the prompt ID: lowercase letters, numbers and hyphens only.
2. **Fill in the header** (the block between the `---` lines). Every line is required.
3. **Write the prompt** in the sections below. Keep each instruction short and clear. One idea per sentence.
4. **Never put secrets or personal data** in this file (no passwords, API keys, customer details).
5. **Update the header** every time you change the prompt: version, status, date, model, eval report.
6. Add a matching entry in the changelog **before** you edit.
7. If something does not apply, write `N/A - [reason]`. If you do not know, write `UNKNOWN - [who will find out] - [date]`.

---

```yaml
---
prompt_id: [FILL IN: e.g. support-agent-system]
version: [FILL IN: e.g. 0.1.0]
type: [FILL IN: A agent system / B dev instruction / C in-product / D eval-test]
status: [FILL IN: Draft / In Review / Staging / Production / Deprecated / Retired]
owner: [FILL IN: name]
author: [FILL IN: name]
reviewer: [FILL IN: name, a different person from the author]
last_changed: [FILL IN: YYYY-MM-DD]
tested_on_model: [FILL IN: exact model name/ID]
model_settings: [FILL IN: e.g. temperature, max output length]
eval_report: [FILL IN: link or path for THIS version]
changelog_entry: [FILL IN: link or line in changelog]
rollback_to: [FILL IN: previous version, or N/A - first version]
output_contract: [FILL IN: who reads the output and the promised shape, or N/A - [reason]]
depends_on: [FILL IN: other prompt IDs and versions this one passes work to or receives from, or N/A]
---
```

# [FILL IN: Prompt ID]: [FILL IN: plain-English title]

## 1. Purpose (for humans, not the AI)

[FILL IN: Two sentences. What is this prompt for, and who benefits?]

*Example: Tells the support agent how to answer customer questions about orders and when to hand off to a human.*

## 2. Role and goal

[FILL IN: Who is the AI in this task, and what is it trying to achieve?]

*Example: You are a friendly support assistant for [Product]. Your goal is to answer order questions correctly and quickly.*

## 3. Rules the AI must follow

*List each rule on its own line. Put the most important rules first.*

1. [FILL IN: e.g. Use only the facts given to you. If you do not know, say so.]
2. [FILL IN]
3. [FILL IN]

## 4. Things the AI must never do

1. [FILL IN: e.g. Never promise a refund above $100. Hand off to a human.]
2. [FILL IN: e.g. Never share another customer's information.]
3. [FILL IN]

## 5. Tools and permissions (only if the AI can take actions)

| Tool | Allowed to do | Not allowed to do | Needs human approval first? |
|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | ☐ Yes ☐ No |

## 6. Output format

[FILL IN: Exactly how the answer must look. Paste a sample.]

```text
[FILL IN: sample output]
```

## 7. Examples (good and bad)

**Good example**

- Input: [FILL IN]
- Output: [FILL IN]

**Bad example (what NOT to do)**

- Input: [FILL IN]
- Bad output: [FILL IN]
- Why it is bad: [FILL IN]

## 8. Variables (placeholders filled in by the app)

| Variable | Meaning | Example | Can it contain private data? |
|---|---|---|---|
| `{[FILL IN]}` | [FILL IN] | [FILL IN] | ☐ Yes ☐ No |

## 9. When unsure or something breaks (fallback)

[FILL IN: What should the AI say or do if it cannot answer, if a tool fails, or if the user tries to break the rules?]

*Example: Say "I'm not sure about that. Let me connect you with a teammate." and hand off.*

## 10. Safety notes

- Anything in this prompt that would be harmful if someone saw it? [FILL IN: No / Yes + what]
- Which hand-offs or tools could be abused? [FILL IN]
- Safety check link: [FILL IN]

## 11. Last-minute checklist before saving

- ☐ Header filled in and version raised correctly
- ☐ Changelog entry written
- ☐ No secrets or personal data
- ☐ Examples still match the rules
- ☐ Eval run and report linked
