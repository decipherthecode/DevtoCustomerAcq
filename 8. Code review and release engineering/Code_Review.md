# Code Review & Release Template (AI-Driven Development Life Cycle)

> **Template version:** 1.0 | **Scope:** from first line of code → release → the first 500 customers
> **Works for:** any language, any framework, any team size (solo founder to 20 people), humans and AI agents working together.
> **One file only.** Everything you need is in this document.

---

# How to fill this document (READ THIS FIRST)

**This document is a questionnaire. You do not need to be a programmer to fill it in.** If you can answer a question in a sentence, you can fill it in.

## Step-by-step

1. **Copy this file** into your project and rename it `Code_Review.md` (keep it at the project root or in `/docs`).
2. **Fill Part A once** per project (about 45-60 minutes). Part A is your project's "rule book".
3. **Copy Part B for every code change** (every pull request / PR). Takes 5-15 minutes.
4. **Copy Part C for every release** (every time customers get something new).
5. **Copy Part D for every launch stage** (Stage 0 → Stage 6, up to your first 500 customers).
6. **Finish with Part E** (final check) before you call the document "ready".

## The 7 golden rules of filling

| # | Rule | Example |
|---|------|---------|
| 1 | **Replace every `[...]`** with your real answer. Nothing in square brackets may remain. | `[Project name]` → `PetCare App` |
| 2 | **Never leave a blank.** If you truly don't know, write `TBD - owner: <name> - by: <date>`. | `TBD - owner: Asha - by: 2026-11-01` |
| 3 | **Use numbers, not feelings.** Write "under 2 seconds", not "fast". | `Page loads in under 2 seconds` |
| 4 | **Use real names and dates.** Write "Ravi, 2026-11-05", not "someone, soon". | |
| 5 | **Tick boxes like this:** `[x]` = yes/done, `[ ]` = no/not done, `[N/A]` = does not apply (add a reason). | `[x] Tests pass` |
| 6 | **Pick from options when you see `( ) A  ( ) B`.** Change exactly one to `(x)`. | `(x) Weekly` |
| 7 | **Do not delete questions.** If a question does not apply, write `N/A - because ...`. | `N/A - no mobile app` |

## What the symbols mean

- 🟥 **MUST** = required. You cannot launch without it.
- 🟨 **SHOULD** = strongly recommended. Skip only with a written reason.
- 🟩 **COULD** = nice to have.
- 💡 **Hint** = help text. Delete hints once you understand them (optional).
- ✍️ **Answer:** = write your answer on this line.
- 🤖 = something an AI agent can do. 👤 = something only a human may do.

## Words you may not know

| Word | Plain meaning |
|------|---------------|
| **Code review** | Another person (or AI) reads the code change before it is accepted, to catch mistakes. |
| **PR (Pull Request)** | A request that says "please review and add my change to the main code". |
| **Merge** | Adding the approved change into the main code. |
| **Release** | Giving a new version of the product to customers. |
| **Rollback** | Going back to the previous working version if something breaks. |
| **Staging** | A practice copy of the product used for testing. |
| **Production (prod)** | The real product that customers use. |
| **Feature flag** | An on/off switch to show a new feature to only some customers. |
| **Hotfix** | A fast, small fix for a serious problem in production. |
| **CI/CD** | Robots that automatically test (CI) and deliver (CD) your code. |
| **AI agent** | An AI that can write, review, or test code with some independence. |
| **SLA** | A time promise, e.g. "review within 24 hours". |
| **Blast radius** | How many customers a mistake can hurt. |

## If you get stuck

- Write your best honest answer, then add `(unsure)` after it. A reviewer will help.
- Ask: *"What would a stranger need to know to do this without asking me?"* Write that.

---

# Document Control

| Field | ✍️ Answer |
|-------|----------|
| Project name | [ ] |
| Product one-line description (what it does, for whom) | [ ] |
| Document owner (name + role) | [ ] |
| Created on (YYYY-MM-DD) | [ ] |
| Last reviewed on (YYYY-MM-DD) | [ ] |
| Next review date (suggested: every 90 days) | [ ] |
| Status | ( ) Draft  ( ) In review  ( ) Approved |
| Approved by (name + date) | [ ] |

---

# PART A - PROJECT CODE REVIEW STANDARD (fill once per project)

## A1. Project Basics

**A1.1** What problem does the product solve? (max 3 sentences)
✍️ Answer:

**A1.2** Who are the customers? (e.g. "small shop owners in India")
✍️ Answer:

**A1.3** Product type (tick all that apply):
`[ ] Website  [ ] Web app  [ ] Mobile app (iOS)  [ ] Mobile app (Android)  [ ] API / backend  [ ] Desktop app  [ ] Browser extension  [ ] AI/LLM feature  [ ] Other: ____`

**A1.4** Main programming languages and frameworks used:
✍️ Answer:

**A1.5** Where is the code stored? (link)
✍️ Answer:

**A1.6** How sensitive is the data you handle? (pick one)
`( ) Public only  ( ) Names/emails  ( ) Payments  ( ) Health/children data  ( ) Other regulated data: ____`
💡 The more sensitive, the stricter the review rules in A5 and A8 must be.

**A1.7** What is the worst thing that could happen if the code has a bug? (e.g. "customers charged twice")
✍️ Answer:

## A2. People & Roles (humans and AI agents)

**A2.1** Fill the table. Every role needs **one** named owner. One person may hold several roles.

| Role | What they do | Name (human) | Backup person |
|------|--------------|--------------|---------------|
| Product Owner 👤 | Decides *what* is built | [ ] | [ ] |
| Tech Lead / Architect 👤 | Decides *how* it is built | [ ] | [ ] |
| Developer(s) 👤/🤖 | Writes code | [ ] | [ ] |
| Code Reviewer(s) 👤/🤖 | Checks the code | [ ] | [ ] |
| QA / Tester 👤/🤖 | Tests the product | [ ] | [ ] |
| Security Reviewer 👤 | Checks safety/privacy | [ ] | [ ] |
| Release Manager 👤 | Decides when to release | [ ] | [ ] |
| On-call Engineer 👤 | Fixes urgent problems | [ ] | [ ] |
| Customer Support Lead 👤 | Collects customer problems | [ ] | [ ] |

**A2.2** List each AI agent used in this project:

| AI agent name / tool | Job (write / review / test / docs / other) | Human who is responsible for it |
|----------------------|--------------------------------------------|---------------------------------|
| [ ] | [ ] | [ ] |
| [ ] | [ ] | [ ] |

**A2.3** How do people contact each other for urgent problems? (chat channel, phone, email)
✍️ Answer:

## A3. Tools & Environments

**A3.1** Fill the table with the real tool or link. Write `N/A` if you don't use it.

| Purpose | Tool used | Link |
|---------|-----------|------|
| Code hosting (GitHub, GitLab, etc.) | [ ] | [ ] |
| Task / bug tracking | [ ] | [ ] |
| Automatic testing & build (CI) | [ ] | [ ] |
| Automatic delivery (CD) | [ ] | [ ] |
| Error tracking | [ ] | [ ] |
| Uptime & performance monitoring | [ ] | [ ] |
| Log storage | [ ] | [ ] |
| Secrets storage (passwords, keys) | [ ] | [ ] |
| Customer feedback / support desk | [ ] | [ ] |
| Analytics (usage numbers) | [ ] | [ ] |

**A3.2** Your environments (places the product runs):

| Environment | Who can use it | Real customer data? | Link |
|-------------|----------------|---------------------|------|
| Local (developer's computer) | Developer | 🟥 NEVER | N/A |
| Development / Test | Team | 🟥 NEVER | [ ] |
| Staging (practice copy) | Team + invited testers | ( ) No  ( ) Fake copy only | [ ] |
| Production (real) | Customers | Yes | [ ] |

## A4. Branches, Changes & Size Rules

**A4.1** Name of the main code branch (usually `main`):
✍️ Answer:

**A4.2** Can anyone put code directly into the main branch without review? 🟥 Recommended: **No**.
`( ) No - every change needs a PR  ( ) Yes (explain why): ____`

**A4.3** Branch naming rule. Pick one and write an example:
`( ) feature/short-name   ( ) fix/short-name   ( ) type/ticket-number-short-name   ( ) Other: ____`
✍️ Example:

**A4.4** Maximum size of one change (smaller = safer to review). Suggested: **400 changed lines**.
✍️ Answer:
💡 If bigger, split it into smaller PRs.

**A4.5** Commit message rule (pick one):
`( ) Free text   ( ) Conventional format, e.g. "fix: stop double payment"   ( ) Ticket number first`

**A4.6** Every PR must link to a task/ticket? `( ) Yes  ( ) No`

**A4.7** Every PR must have a clear description saying: *what changed, why, how it was tested, what could break.* `( ) Yes (required)  ( ) No`

## A5. Review Rules (who approves what)

**A5.1** Classify changes by risk. Fill the last two columns.

| Risk level | Examples | Approvals needed (number + who) | Review time promise (SLA) |
|------------|----------|----------------------------------|---------------------------|
| 🟢 Low | Text change, colour, docs, comments | [ ] | [ ] |
| 🟡 Medium | New small feature, bug fix, UI flow | [ ] | [ ] |
| 🟠 High | Login, payments, database change, permissions, personal data | [ ] | [ ] |
| 🔴 Critical | Security fix, hotfix, data migration, anything that can lose data | [ ] | [ ] |

💡 Suggested: Low = 1 approval / 2 working days. Medium = 1 human approval / 1 day. High = 2 approvals including Security Reviewer / 1 day. Critical = 2 approvals, same-day.

**A5.2** The author of the change can never approve their own change. 🟥 `( ) Agreed  ( ) Exception: ____`

**A5.3** What happens when a review is late (past SLA)?
✍️ Answer:

**A5.4** How are disagreements between author and reviewer resolved? Who has the final say?
✍️ Answer:

**A5.5** Review comment labels used by the team (tick all you accept):
`[ ] BLOCKER = must fix before merge   [ ] SUGGESTION = optional improvement   [ ] QUESTION = reviewer needs an answer   [ ] NIT = tiny style detail   [ ] PRAISE = something done well`

**A5.6** Reviewers must read the code in this order (tick to keep):
`[ ] 1. Purpose (does it solve the ticket?)  [ ] 2. Safety  [ ] 3. Correctness  [ ] 4. Tests  [ ] 5. Readability  [ ] 6. Speed  [ ] 7. Style`

## A6. AI Agent Rules (AI-Driven Development)

**A6.1** What may AI agents do in this project? Tick all that are allowed:

| Action | 🤖 Allowed? | Human approval required? |
|--------|------------|--------------------------|
| Write new code | `[ ]` | `[ ]` |
| Edit existing code | `[ ]` | `[ ]` |
| Review human code | `[ ]` | `[ ]` |
| Write tests | `[ ]` | `[ ]` |
| Write documentation | `[ ]` | `[ ]` |
| Open pull requests | `[ ]` | `[ ]` |
| Merge pull requests | `[ ]` (🟥 recommended: NO) | `[ ]` |
| Change database structure | `[ ]` (🟥 recommended: NO) | `[ ]` |
| Deploy to staging | `[ ]` | `[ ]` |
| Deploy to production | `[ ]` (🟥 recommended: NO) | `[ ]` |
| Touch secrets / passwords | `[ ]` (🟥 recommended: NO) | `[ ]` |
| Install new libraries | `[ ]` | `[ ]` |

**A6.2** Where do AI instructions live (e.g. a `CLAUDE.md` / `AGENTS.md` / rules file)? Link:
✍️ Answer:

**A6.3** Every PR created with AI help must say so? `( ) Yes, label "ai-assisted"  ( ) No`

**A6.4** A human must understand and be able to explain every AI-written line before approving. 🟥 `( ) Agreed`

**A6.5** AI-specific checks a reviewer must do (tick all you require):
`[ ] Do the libraries/functions used really exist (no invented ones)?`
`[ ] Does the code do ONLY what was asked (no extra hidden changes)?`
`[ ] Any copied code with an unclear licence?`
`[ ] Any secrets, keys or private data pasted into prompts or code?`
`[ ] Are the tests real (they could fail), not tests that always pass?`
`[ ] Were old tests deleted or weakened to make things pass?`
`[ ] Does it follow the project's existing style and structure?`

**A6.6** What data is **never** allowed to be sent to an AI tool? (e.g. customer emails, keys)
✍️ Answer:

**A6.7** If the product itself uses AI/LLM features, answer these:
- Which model/provider is used? ✍️
- What happens if the AI gives a wrong or harmful answer? ✍️
- Is there a human fallback or a "report this answer" button? `( ) Yes  ( ) No`
- Is there a test set of questions that is re-run before every release? `( ) Yes  ( ) No`
- Is there a cost limit per day? ✍️

**A6.8** Where are AI actions recorded (a log of what the AI did)? ✍️

## A7. Automatic Quality Gates (robots must pass before a human reviews)

**A7.1** Tick each check you will run automatically on every PR and write the tool name:

| Check | Required? | Tool used |
|-------|-----------|-----------|
| Code builds without errors | 🟥 MUST | [ ] |
| Automatic tests pass | 🟥 MUST | [ ] |
| Code style / formatting check | 🟨 SHOULD | [ ] |
| Static code analysis (finds bugs) | 🟨 SHOULD | [ ] |
| Secret scanner (finds leaked keys) | 🟥 MUST | [ ] |
| Dependency scan (finds unsafe libraries) | 🟥 MUST | [ ] |
| Security scan of code | 🟨 SHOULD | [ ] |
| Test coverage check | 🟨 SHOULD | [ ] |
| Speed/performance check | 🟩 COULD | [ ] |
| Accessibility check (for UI) | 🟨 SHOULD | [ ] |

**A7.2** Minimum test coverage allowed (suggested: 70% for new code):
✍️ Answer:

**A7.3** Which kinds of tests exist? `[ ] Unit  [ ] Integration  [ ] End-to-end  [ ] Manual  [ ] Load  [ ] Security  [ ] AI-quality`

**A7.4** If a robot check fails, can a human override it? `( ) Never  ( ) Yes, with written reason + Tech Lead approval`

## A8. Security & Privacy Rules

**A8.1** Answer Yes/No/N/A. Every "No" needs an owner and date.

| Question | Y / N / N/A | Owner & date if "No" |
|----------|-------------|----------------------|
| Passwords and keys are never in code | [ ] | [ ] |
| Customer passwords are stored hashed, never plain | [ ] | [ ] |
| All traffic uses HTTPS | [ ] | [ ] |
| Users can only see their own data | [ ] | [ ] |
| User input is checked before use | [ ] | [ ] |
| Personal data is limited to what we need | [ ] | [ ] |
| A privacy policy and terms page exist | [ ] | [ ] |
| Customers can delete their data / account | [ ] | [ ] |
| Backups exist and a restore was tested once | [ ] | [ ] |
| Admin accounts use two-step login | [ ] | [ ] |

**A8.2** Which laws or rules apply? `[ ] GDPR  [ ] CCPA  [ ] India DPDP  [ ] HIPAA  [ ] PCI (payments)  [ ] Children's privacy  [ ] Other: ____  [ ] Don't know → ask a lawyer`

**A8.3** How are security problems reported and fixed, and how fast? (suggested: critical within 24 hours)
✍️ Answer:

## A9. Release Engineering Rules

**A9.1** Version numbering (pick one): `( ) 1.2.3 (major.minor.patch)  ( ) Date-based 2026.10.18  ( ) Other: ____`

**A9.2** Release types used:

| Type | When | Who approves | Typical frequency |
|------|------|--------------|-------------------|
| Regular release | Planned new features/fixes | [ ] | [ ] |
| Patch release | Small bug fixes | [ ] | [ ] |
| Hotfix | Urgent production problem | [ ] | As needed |

**A9.3** Days/times when releases are **not** allowed (e.g. Fridays after 2pm, holidays):
✍️ Answer:

**A9.4** How are releases delivered? `( ) All customers at once  ( ) Slowly to a few customers first (recommended)  ( ) Feature flags  ( ) App store review`

**A9.5** Rollback plan: 🟥 MUST be written *before* releasing.
- How do we go back to the last good version? ✍️
- Who can press the rollback button? ✍️
- How long does rollback take (minutes)? ✍️
- What about database changes - can they be undone? ✍️

**A9.6** Database changes (migrations) must be: `[ ] Reviewed by 2 people  [ ] Tested on a copy of real-shaped data  [ ] Reversible  [ ] Done in small safe steps`

**A9.7** Release notes are written for: `[ ] Customers  [ ] Internal team  [ ] App store`. Where are they published? ✍️

**A9.8** How are customers told about big changes or downtime? ✍️

## A10. Launch Roadmap: First Line of Code → First 500 Customers

💡 **Idea:** do not give the product to 500 people on day one. Grow in stages. Move to the next stage ONLY if the "Exit rules" are met. This protects customers and your reputation.

Fill the blanks. Suggested numbers are given; change them if you need to.

| Stage | Name | Who uses it | Suggested size | Start date | Target end date |
|-------|------|-------------|----------------|------------|-----------------|
| 0 | Build & internal test | Team only | 0 customers | [ ] | [ ] |
| 1 | Private alpha | Friends, family, invited testers | 5-10 | [ ] | [ ] |
| 2 | Closed beta | Invited target customers | 25-50 | [ ] | [ ] |
| 3 | Soft launch | Small slice of real market | 100 | [ ] | [ ] |
| 4 | Public beta / limited launch | Open sign-ups with a limit | 250 | [ ] | [ ] |
| 5 | Full launch target | Open to everyone | 500 | [ ] | [ ] |
| 6 | Post-500 review | Team | N/A | [ ] | [ ] |

**A10.1** For each stage, define **Entry rules** (what must be true to start) and **Exit rules** (what must be true to move on). Use numbers.

| Stage | Entry rules | Exit rules (numbers!) |
|-------|-------------|-----------------------|
| 0 | Part A complete; core features done | All 🟥 checks in Part B & C pass; zero known critical bugs |
| 1 | Stage 0 exit met; rollback tested | e.g. ≥ [ ] testers finished the main task; ≤ [ ] critical bugs |
| 2 | Stage 1 exit met; support channel open | e.g. crash-free sessions ≥ [ ] %; ≥ [ ] % complete sign-up |
| 3 | Stage 2 exit met; monitoring alerts live | e.g. error rate ≤ [ ] %; support replies within [ ] hours |
| 4 | Stage 3 exit met; load tested for 2× users | e.g. uptime ≥ [ ] %; speed under [ ] sec |
| 5 | Stage 4 exit met; legal pages live | e.g. [ ] % of customers active after 30 days |
| 6 | 500 customers reached | Lessons learned document written |

**A10.2** What is "success" for the first 500 customers? Write 3 measurable goals:
1. ✍️
2. ✍️
3. ✍️

**A10.3** What makes you **pause** the rollout? (e.g. any data loss, error rate above X%, security issue)
✍️ Answer:

**A10.4** Who has the right to say "stop the launch"? (name)
✍️ Answer:

## A11. Monitoring, Incidents & Support

**A11.1** What are the 5 numbers you watch after every release?
`[ ] Errors  [ ] Crashes  [ ] Speed  [ ] Uptime  [ ] Sign-ups  [ ] Payments succeeded  [ ] Support tickets  [ ] AI answer quality  [ ] Other: ____`

**A11.2** Who gets an alert when something breaks, and how? (phone, chat, email)
✍️ Answer:

**A11.3** Define problem severity:

| Level | Meaning | Response time | Fix time target |
|-------|---------|---------------|-----------------|
| SEV1 | Product down / data loss / security breach | [ ] | [ ] |
| SEV2 | Main feature broken for many | [ ] | [ ] |
| SEV3 | Small problem, workaround exists | [ ] | [ ] |
| SEV4 | Cosmetic / idea | [ ] | [ ] |

**A11.4** After every SEV1/SEV2, we write a short "what happened and how to stop it happening again" note within `[ ]` days. `( ) Agreed`

**A11.5** Where do customers report problems? (email, form, chat link)
✍️ Answer:

**A11.6** How often do we read customer feedback and turn it into tasks? `( ) Daily  ( ) Weekly  ( ) Other: ____`

## A12. Project Health Numbers (optional but useful)

| Number | How measured | Target |
|--------|--------------|--------|
| Time from PR opened → first review | [ ] | [ ] |
| Time from PR opened → merged | [ ] | [ ] |
| % of PRs sent back for fixes | [ ] | [ ] |
| Bugs found after release (per release) | [ ] | [ ] |
| % of releases rolled back | [ ] | [ ] |
| Time to fix SEV1 | [ ] | [ ] |

---

# PART B - PER-CHANGE REVIEW CHECKLIST (copy for every pull request)

> **How to use:** Copy everything from "B-Header" to the end of Part B into the PR description. The **author** fills B1-B3. The **reviewer** fills B4-B9. 🟥 items must be ticked before merge.

## B-Header

| Field | ✍️ Answer |
|-------|----------|
| PR title / link | [ ] |
| Ticket link | [ ] |
| Author (human or AI agent name) | [ ] |
| Human responsible (if AI wrote it) | [ ] |
| Reviewer(s) | [ ] |
| Date opened | [ ] |
| Risk level (from A5.1) | ( ) 🟢 Low  ( ) 🟡 Medium  ( ) 🟠 High  ( ) 🔴 Critical |
| AI-assisted? | ( ) No  ( ) Yes - tool: [ ] |
| Launch stage this will ship in (from A10) | [ ] |

## B1. Author: What & Why

- What does this change do? (1-3 sentences) ✍️
- Why is it needed? (link to problem/ticket) ✍️
- What is **not** included in this change? ✍️
- Screenshots / short recording (for anything customers see) ✍️

## B2. Author: Self-check before asking for review

`[ ] 🟥 I re-read my own change line by line`
`[ ] 🟥 It builds and all automatic checks are green`
`[ ] 🟥 No secrets, keys, or customer data in the code or comments`
`[ ] 🟥 I ran it myself and it works`
`[ ] 🟨 No leftover debug lines, unused code, or "TODO" without a ticket`
`[ ] 🟨 Change is smaller than the limit in A4.4 (or I explained why)`
`[ ] 🟨 Docs / comments / release note updated`

## B3. Author: Testing evidence

| Test | Done? | Result / link |
|------|-------|---------------|
| New automatic tests added | [ ] | [ ] |
| Old tests still pass | [ ] | [ ] |
| Tried the "happy path" (everything goes right) | [ ] | [ ] |
| Tried the "unhappy path" (wrong input, no internet, empty data) | [ ] | [ ] |
| Tested on needed devices/browsers | [ ] | [ ] |

## B4. Reviewer: Does it solve the right problem?

`[ ] 🟥 The change matches the ticket - nothing extra, nothing missing`
`[ ] 🟥 I understand what the change does (if not, I asked - label QUESTION)`
`[ ] 🟨 There is no simpler way to do the same thing`

## B5. Reviewer: Correctness

`[ ] 🟥 Logic is right for normal cases`
`[ ] 🟥 Edge cases handled: empty, very large, zero, negative, wrong type, duplicates`
`[ ] 🟥 Errors are handled and give a helpful message (no silent failures)`
`[ ] 🟨 Time zones, currencies, languages handled if relevant`
`[ ] 🟨 Two users acting at the same time cannot break it`

## B6. Reviewer: Security & Privacy

`[ ] 🟥 No secrets/keys in code`
`[ ] 🟥 Only the right people can use this feature (permissions checked)`
`[ ] 🟥 User input is checked before it is used`
`[ ] 🟥 No customer personal data written to logs`
`[ ] 🟨 New libraries are trusted, maintained, and licence-compatible`
`[ ] 🟨 Personal data collected is the minimum needed`

## B7. Reviewer: Tests & Quality

`[ ] 🟥 Tests check real behaviour (they would fail if the code were wrong)`
`[ ] 🟥 No tests deleted or weakened without a reason`
`[ ] 🟨 Names are clear; a new teammate could read this`
`[ ] 🟨 No copy-pasted blocks that should be shared`
`[ ] 🟨 Follows project style and structure`

## B8. Reviewer: Performance & Reliability

`[ ] 🟨 No slow loops or repeated database calls for each item`
`[ ] 🟨 Works for 10× today's number of users`
`[ ] 🟨 Handles other services being slow or down`
`[ ] 🟨 Logging/monitoring added for anything that can fail`

## B9. Reviewer: Release safety

`[ ] 🟥 Can this be switched off or rolled back easily?`
`[ ] 🟥 If it touches the database: migration reviewed and reversible`
`[ ] 🟨 Behind a feature flag if risky`
`[ ] 🟨 Customer-facing text is clear and error-free`

## B10. AI-assisted change extra checks (only if AI wrote or edited code)

`[ ] 🟥 A human can explain every changed part`
`[ ] 🟥 All libraries/functions used actually exist`
`[ ] 🟥 No unrelated files were changed`
`[ ] 🟥 No private data was shared with the AI tool (see A6.6)`
`[ ] 🟨 Code licence is clear`

## B11. Decision

| Field | ✍️ Answer |
|-------|----------|
| Decision | ( ) ✅ Approve  ( ) 🔁 Approve after fixes  ( ) ❌ Request changes  ( ) 🚫 Reject |
| Open BLOCKER comments count (must be 0 to approve) | [ ] |
| Reviewer name + date | [ ] |
| Second reviewer (if High/Critical) + date | [ ] |
| Merged by + date | [ ] |

---

# PART C - RELEASE CHECKLIST (copy for every release)

## C-Header

| Field | ✍️ Answer |
|-------|----------|
| Release version | [ ] |
| Release type | ( ) Regular  ( ) Patch  ( ) Hotfix |
| Launch stage (from A10) | [ ] |
| Release manager | [ ] |
| Planned date & time (with time zone) | [ ] |
| List of changes included (PR links) | [ ] |

## C1. Before release

`[ ] 🟥 Every included PR has an approved Part B`
`[ ] 🟥 All automatic checks are green on the release version`
`[ ] 🟥 Tested on staging by someone who did not write the code`
`[ ] 🟥 No open SEV1 or SEV2 bugs`
`[ ] 🟥 Rollback plan written and the person who can run it is available (A9.5)`
`[ ] 🟥 Database migrations tested on a copy; backup taken just before release`
`[ ] 🟥 Security scan clean (no critical/high findings)`
`[ ] 🟨 Speed/load test done if traffic will grow`
`[ ] 🟨 Release notes written (A9.7)`
`[ ] 🟨 Support team told what is changing`
`[ ] 🟨 Monitoring dashboards and alerts checked`
`[ ] 🟩 Customers warned if downtime is expected`

## C2. During release

`[ ] Release started at: ____ (time)`
`[ ] Released to the smallest group first (percent: ___ %)`
`[ ] Watched numbers for ___ minutes: errors normal? speed normal? sign-ups normal?`
`[ ] Increased to ___ % at ____ (time)`
`[ ] Reached 100% at ____ (time)`

## C3. After release (first 24-72 hours)

`[ ] 🟥 Smoke test passed (log in, main feature, payment if any)`
`[ ] 🟥 No new SEV1/SEV2 problems`
`[ ] 🟨 Error rate: ___ (before: ___)`
`[ ] 🟨 Speed: ___ (before: ___)`
`[ ] 🟨 Support tickets: ___ new about this release`
`[ ] 🟨 Release marked "stable" or "rolled back" with reason`

## C4. Release decision

| Field | ✍️ Answer |
|-------|----------|
| Go / No-Go decision | ( ) GO  ( ) NO-GO |
| Reason (if NO-GO) | [ ] |
| Approved by (Release Manager + Product Owner) + date | [ ] |
| Rolled back? | ( ) No  ( ) Yes - why: [ ] |

---

# PART D - LAUNCH STAGE REVIEW (copy once per stage in A10)

> Use this at the end of each stage (Alpha, Beta, Soft launch, etc.) to decide: **move on, stay, or go back.**

| Field | ✍️ Answer |
|-------|----------|
| Stage number & name | [ ] |
| Dates (start → end) | [ ] |
| Customers in this stage (target vs actual) | [ ] / [ ] |
| Total customers so far (goal: 500) | [ ] |

## D1. Exit rules check (copy numbers from A10.1)

| Exit rule | Target | Actual | Met? |
|-----------|--------|--------|------|
| [ ] | [ ] | [ ] | `[ ]` |
| [ ] | [ ] | [ ] | `[ ]` |
| [ ] | [ ] | [ ] | `[ ]` |

## D2. What did customers say?

- Top 3 things customers love: ✍️
- Top 3 things customers complain about: ✍️
- Top 3 things customers asked for: ✍️
- Number of customers who stopped using it, and the reasons: ✍️

## D3. What did the code and product teach us?

- Biggest bugs found after release and why review missed them: ✍️
- Which review rules should get stricter or looser? ✍️
- Any technical debt (shortcuts) we must fix before the next stage? ✍️

## D4. Stage decision

`( ) ✅ Move to next stage   ( ) ⏸ Stay in this stage   ( ) ⏪ Go back one stage   ( ) 🛑 Pause everything`
Reason: ✍️
Decided by + date: ✍️

---

# PART E - FINAL "IS THIS DOCUMENT READY?" CHECK

Tick everything before you call this document finished.

`[ ] No square brackets [ ] remain unless they are tick boxes`
`[ ] Every role in A2 has a named human`
`[ ] Every "TBD" has an owner and a date`
`[ ] Rollback plan (A9.5) is written and someone has practiced it once`
`[ ] Launch stages and exit rules (A10) use numbers`
`[ ] A stranger could follow Part B without asking you a question`
`[ ] AI rules (A6) were read and agreed by everyone on the team`
`[ ] Document approved and date saved in Document Control`
`[ ] Next review date set`

## Glossary additions (add words your team uses)

| Word | Meaning |
|------|---------|
| [ ] | [ ] |

## Change log of this document

| Date | Version | What changed | Changed by |
|------|---------|--------------|------------|
| [ ] | 1.0 | First version created from template | [ ] |

---

# Quick Example (how a filled answer looks)

> **A4.4** Maximum size of one change → ✍️ *"400 changed lines. Bigger changes are split into smaller PRs."*
> **A5.1 (High risk row)** Approvals → *"2 approvals: Tech Lead + Security Reviewer (Priya). Review within 1 working day."*
> **A10.1 Stage 2 exit** → *"At least 30 of 50 beta users finished sign-up; crash-free sessions ≥ 99%; zero data-loss bugs."*
> **A9.5 rollback** → *"Release Manager clicks 'Rollback' in the deploy tool; takes about 5 minutes; database change is reversible."*

---

*End of template. Keep this file in version control and review it every 90 days.*
