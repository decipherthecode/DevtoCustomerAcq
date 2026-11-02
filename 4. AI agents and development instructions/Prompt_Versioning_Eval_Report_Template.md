# HOW TO FILL OUT THIS FILE

> Part of `Prompt_Versioning.md` (Section 11). Make **one copy per prompt version** you test, name it `eval-<prompt-id>-<version>.md`, and link it from the prompt file header and the changelog. Delete this box when done.

1. Fill the top table first: it says exactly what was tested.
2. Run the **same** test set on the **old** and **new** versions. Fair comparison only.
3. Copy the thresholds from the gate table in `Prompt_Versioning.md` Section 11.2. Do not invent new ones here.
4. Write the result as **PASS** or **FAIL**. No "mostly".
5. If a gate fails and you still want to release, you need a written **exception** signed by the Final Approver (bottom of this file).
6. If something does not apply, write `N/A - [reason]`. If you do not know, write `UNKNOWN - [who will find out] - [date]`.

---

# Eval Report: [FILL IN: prompt-id] [FILL IN: version]

## 1. What was tested

| Field | Your answer |
|---|---|
| Prompt ID and **new** version | [FILL IN] |
| Compared against (previous version) | [FILL IN] |
| Date of run | [FILL IN: YYYY-MM-DD] |
| Run by | [FILL IN: name] |
| Model name/ID and settings | [FILL IN] |
| Test set name and version | [FILL IN: e.g. golden-support-v3] |
| Number of test cases | [FILL IN] |
| Times each case was run | [FILL IN: *suggested: 3*] |
| Who or what scored the answers | [FILL IN: people / AI judge / automatic checks] |
| Human re-check of AI-scored cases | [FILL IN: % checked and by whom] |

## 2. Results by gate

| Gate | Threshold | Previous version | New version | PASS / FAIL |
|---|---|---|---|---|
| Task success | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Format validity | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Safety pass rate | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Made-up facts | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Speed (average / slowest typical) | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Cost / length | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| No-regression slice | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Tool and action checks (if the agent uses tools) | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

## 3. Results by slice

| Slice | Cases | Previous | New | Notes |
|---|---|---|---|---|
| Normal | [FILL IN] | | | |
| Edge | [FILL IN] | | | |
| Format | [FILL IN] | | | |
| Refusal | [FILL IN] | | | |
| Attack | [FILL IN] | | | |
| Real-world | [FILL IN] | | | |

## 4. Cases that got worse (regressions)

| Case ID | What the old version did | What the new version did | Is it acceptable? Why? |
|---|---|---|---|
| [FILL IN: or `None`] | | | |

## 5. Cases that got better

[FILL IN: Short list, or `None`.]

## 6. Safety and privacy result

- Safety checklist (Section 12 of `Prompt_Versioning.md`) completed: ☐ Yes, link: [FILL IN]
- New problems found: [FILL IN: or `None`]

## 7. Overall decision

| Decision | Tick one |
|---|---|
| **PROMOTE**: all gates passed | ☐ |
| **HOLD**: fix and re-run | ☐ |
| **ROLLBACK / DO NOT RELEASE** | ☐ |
| **EXCEPTION**: gate failed, released anyway with sign-off (fill in 8) | ☐ |

Summary in one sentence: [FILL IN]

## 8. Exception record (only if used)

| Field | Your answer |
|---|---|
| Gate that failed | [FILL IN or N/A] |
| Why release anyway | [FILL IN or N/A] |
| Risk accepted and how it is limited | [FILL IN or N/A] |
| Deadline to fix | [FILL IN or N/A] |
| Final Approver (name, date) | [FILL IN or N/A] |

## 9. Sign-off

| Role | Name | Date |
|---|---|---|
| QA / Eval Lead | [FILL IN] | [FILL IN] |
| Reviewer | [FILL IN] | [FILL IN] |
| Safety Reviewer | [FILL IN] | [FILL IN] |
