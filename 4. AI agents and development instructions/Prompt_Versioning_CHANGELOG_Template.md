# HOW TO FILL OUT THIS FILE

> Part of `Prompt_Versioning.md` (Section 7). Delete this box when done.

1. **Newest entry goes on top.** Copy the "Entry template" below and paste it just under the line `<!-- NEW ENTRIES GO HERE -->`.
2. **Write the entry BEFORE you change the prompt.** It forces you to say what you want to achieve.
3. Replace every `[FILL IN: ...]`. If it does not apply, write `N/A - [reason]`. If you do not know, write `UNKNOWN - [who will find out] - [date]`.
4. **Never delete or rewrite an old entry.** If one was wrong, add a new entry that corrects it.
5. "Improved prompt" is not allowed as a description. Say *what* changed and *what you expect to see*.

**Version number help:** MAJOR = format, role, tools or safety rules change. MINOR = new or better behavior that does not break old behavior. PATCH = typo or clearer wording only. Not sure? Pick the higher one.

---

# Prompt Changelog: [FILL IN: Project Name]

This file follows the spirit of [Keep a Changelog](https://keepachangelog.com) and [Semantic Versioning](https://semver.org).

## Entry template (copy this)

```markdown
## [FILL IN: prompt-id] [FILL IN: version] - [FILL IN: YYYY-MM-DD]
- **Change type:** [FILL IN: MAJOR / MINOR / PATCH]
- **Author / Reviewer:** [FILL IN: names, must be different people]
- **What changed:** [FILL IN: one or two plain sentences]
- **Why:** [FILL IN: the problem or goal, with a ticket or incident link if any]
- **Expected effect on output:** [FILL IN: what a user should notice]
- **Contract or handoff affected?:** [FILL IN: Yes + which / No]
- **Model and settings tested on:** [FILL IN]
- **Risk:** [FILL IN: Low / Medium / High + one sentence]
- **Eval result:** [FILL IN: report link] - Score [x] vs previous [y] - Gate: [PASS / FAIL / EXCEPTION + link]
- **Safety and privacy check:** [FILL IN: link or `Done on YYYY-MM-DD by name`]
- **Rollback to:** [FILL IN: previous version number]
- **Approved by / date:** [FILL IN: name, YYYY-MM-DD]
- **Released:** [FILL IN: environment, rollout %, date]
```

---

<!-- NEW ENTRIES GO HERE -->

## support-agent-system 0.1.0 - [FILL IN: YYYY-MM-DD]
*Example entry. Replace or delete.*
- **Change type:** MINOR
- **Author / Reviewer:** [FILL IN] / [FILL IN]
- **What changed:** First working version of the support agent instructions.
- **Why:** Start of Phase 1 (Build).
- **Expected effect on output:** Agent answers order-status questions and hands off refunds.
- **Contract or handoff affected?:** N/A - first version
- **Model and settings tested on:** [FILL IN]
- **Risk:** Low. Not live.
- **Eval result:** N/A - golden set not built yet
- **Safety and privacy check:** UNKNOWN - [name] - [date]
- **Rollback to:** N/A - first version
- **Approved by / date:** [FILL IN]
- **Released:** Development only
