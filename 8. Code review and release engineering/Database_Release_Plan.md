# How to Fill This Document (Read This First)

**What is this?** A Database Release Plan is a checklist-plus-story that explains how every change to your database (tables, fields, data, settings, indexes) travels safely from "an idea" to "live for real customers", and keeps working until your **first 500 customers** are happily using the product.

**Who can fill it?** Anyone: founder, developer, tester, project manager, or an AI agent working with a human. No technical background is needed for Sections 0–3. Ask a developer for help if a question says *(Tech)*.

## The 7 Simple Rules

1. **Answer every question.** Write under `Your answer:`. Delete the `Example answer:` lines only when you are done.
2. **Don't know? Write `UNKNOWN - ask [name] by [date]`.** Never guess. A visible UNKNOWN is safer than a wrong answer.
3. **Not needed? Write `N/A - because [reason]`.** Never leave blanks.
4. **Use plain words.** If a 10-year-old could not understand a sentence, rewrite it. Explain any short form once.
5. **Use real names, real dates, real numbers.** Write "Friday 14 Nov 2026, 10:00 UTC", not "soon". Write "under 200 ms", not "fast".
6. **Tick boxes like this:** `[x]` = yes/done, `[ ]` = not yet.
7. **Human approval is required for anything touching production data.** AI agents may draft and suggest. A named person approves and presses the button.

## Status Labels (use only these)

| Label | Meaning |
|---|---|
| `NOT STARTED` | Nobody has begun |
| `IN PROGRESS` | Someone is working on it |
| `BLOCKED` | Waiting on something (say what) |
| `DONE` | Finished and checked by a second person |

## Instructions for AI Agents Filling This Document

- Fill only what you can verify from code, schema files, migration files, configs, or the person's answers. Cite the file or source next to the answer.
- Never invent names, dates, numbers, credentials, or connection strings. Use `UNKNOWN` and list it in Section 16 (Open Questions).
- Never write real passwords, API keys, or customer data in this file. Write where the secret is stored instead (e.g. "in the team password manager, vault: Prod-DB").
- Do not run any command against production. Draft it, mark it `NEEDS HUMAN APPROVAL`, and stop.
- After filling a section, re-read it and check: could someone act on this without asking a follow-up question? If not, improve it.

## How the Plan Flows (Big Picture)

```
Phase 1 PLAN -> Phase 2 BUILD -> Phase 3 REVIEW -> Phase 4 TEST -> Phase 5 STAGING
   -> Phase 6 GO-LIVE -> Phase 7 LAUNCH WAVES (customer 1 -> 500) -> Phase 8 HAND-OFF & REVIEW
```

Each phase has a **gate**: a short list of things that must be true before you move on. Gates are in the sections below.

---

# 0. Document Control

| Field | Your answer |
|---|---|
| Project name | |
| Release name / version (e.g. `db-release-1.0`) | |
| Document owner (one person, not a team) | |
| Database approver (the person who can say "yes" to production) | |
| Backup approver (if owner is away) | |
| Date created | |
| Last updated | |
| Document status (`DRAFT` / `IN REVIEW` / `APPROVED` / `RELEASED`) | |
| Link to the code repository | |
| Link to the product requirements / spec | |
| Link to the main ticket board | |

**Version history**

| Version | Date | Who changed it | What changed |
|---|---|---|---|
| 0.1 | | | First draft |

---

# 1. Project Snapshot (Plain-Language Story)

**Q1.1 In 2-3 sentences, what does your product do, and who uses it?**
Example answer: "A mobile app that helps dog owners book trusted walkers. Owners and walkers both create accounts."
Your answer:

**Q1.2 Why does this database release exist? What can customers do after it that they cannot do now?**
Example answer: "It adds the bookings and payments tables so customers can book and pay for walks."
Your answer:

**Q1.3 What is the single worst thing that could go wrong with the database? (Pick one.)**
Example answer: "Customer bookings or payments get lost or shown to the wrong person."
Your answer:

**Q1.4 What is the launch target date and the "first 500 customers" target date?**
| Milestone | Date |
|---|---|
| Database ready in staging | |
| Production go-live | |
| Customer 1 (first real customer) | |
| Customer 500 reached (target) | |

---

# 2. Database Inventory (What Are We Releasing?)

**Q2.1 List every database or data store the product uses. Add rows as needed.**

| # | Name | Type (tick one) | Product / vendor | Where it runs | What it stores (plain words) | Owner |
|---|---|---|---|---|---|---|
| 1 | | `[ ]` Relational SQL `[ ]` NoSQL / document `[ ]` Managed backend (BaaS) `[ ]` Vector / search / analytics `[ ]` Cache / queue `[ ]` File storage | | | | |
| 2 | | | | | | |

Example row: `1 | main-db | Relational SQL | PostgreSQL 16 on Supabase | EU region | users, bookings, payments | Priya`

**Q2.2 For each store, what is the most important thing to protect?**
(Tick all that apply per store: `[ ]` no data loss `[ ]` no data leaks `[ ]` always available `[ ]` fast answers `[ ]` correct totals/money)
Your answer:

**Q2.3 (Tech) What is the version of each database, and who upgrades it?**
Your answer:

**Q2.4 Which type-specific details apply? Fill only the ones you use.**

| Type | Questions to answer |
|---|---|
| Relational SQL | Migration tool used (Flyway, Prisma, Alembic, Liquibase, Supabase migrations, etc.)? Where are migration files kept? Are foreign keys and constraints used? |
| NoSQL / document | Is there a data "shape" (schema) rules file? How are old documents with the old shape handled? Are there indexes to build? |
| Managed backend (BaaS) | Which dashboard settings change (security rules, row-level security, auth, storage rules, edge functions)? Are those settings saved as code, or clicked by hand? |
| Vector / search / analytics | What embedding model and vector size? What happens if the model changes (full re-index)? How long does a rebuild take? |

Your answer:

---

# 3. Release Goals and "Done" Definition

**Q3.1 What must be true for this release to be called a success? Write 3-6 measurable goals.**
Example answers:
- "0 lost bookings during release"
- "Release causes under 1 minute of downtime (or 0)"
- "Page load stays under 2 seconds for 95% of users"
Your answer:

**Q3.2 What is NOT part of this release? (Prevents scope creep.)**
Your answer:

**Q3.3 What does "first 500 customers used the product" mean here?**
(Tick one definition and fill in the details.)
- `[ ]` 500 accounts created
- `[ ]` 500 accounts that finished onboarding
- `[ ]` 500 accounts that did the key action at least once (name the action: ______ )
- `[ ]` Other: ______
Your answer:

---

# 4. Roles and Responsibilities

**Q4.1 Who does what? Every row needs a real name.**

| Role | Name | Contact | Can approve production? (Y/N) |
|---|---|---|---|
| Release owner (runs the plan) | | | |
| Database engineer / developer | | | |
| Code reviewer (must differ from author) | | | |
| QA / tester | | | |
| Product owner (decides what ships) | | | |
| Security / privacy contact | | | |
| On-call person during release | | | |
| Customer-support contact | | | |
| AI agent(s) used (name, tool, job) | | | N (always) |

**Q4.2 Who is the human responsible for each AI agent's work?**
Your answer:

---

# 5. AI Agent Rules for This Database (Human Approves)

**Q5.1 What are AI agents allowed to do? Tick one level per environment.**

| Environment | `Draft only` | `Run with human watching` | `Not allowed` |
|---|---|---|---|
| Local / dev | `[ ]` | `[ ]` | `[ ]` |
| Test / CI | `[ ]` | `[ ]` | `[ ]` |
| Staging | `[ ]` | `[ ]` | `[ ]` |
| Production | `[ ]` | `[ ]` | `[x]` (recommended default: production is human-run) |

**Q5.2 Which tasks may an AI agent do? (Tick all that apply.)**
- `[ ]` Write migration scripts
- `[ ]` Review migration scripts written by humans
- `[ ]` Generate test data (fake only)
- `[ ]` Write rollback scripts
- `[ ]` Check for risky operations (drop, delete, lock, full-table rewrite)
- `[ ]` Draft release notes and customer messages
- `[ ]` Watch dashboards and summarize alerts

**Q5.3 Hard "never" list for AI agents (copy and add to it).**
- Never run commands against production.
- Never see, copy, or store real customer data, passwords, or keys.
- Never delete data, drop tables, or turn off backups.
- Never approve its own work.
- Never change access rules or security settings without a human signing off.
Your additions:

**Q5.4 How does a human approve AI work?**
Example answer: "Reviewer reads the script and the AI's summary, runs it in staging, writes 'Approved - [name] - [date]' on the pull request."
Your answer:

**Q5.5 Where are AI prompts, outputs, and decisions saved so someone can check them later?**
Your answer:

---

# 6. Environments and Access

**Q6.1 List each place the database lives.**

| Environment | Purpose | Real customer data? | Who can read | Who can change | Connection secret stored in |
|---|---|---|---|---|---|
| Local / dev | Building | No | | | |
| Test / CI | Automatic checks | No | | | |
| Staging | Final rehearsal (copy of production's shape) | No (fake or masked) | | | |
| Production | Real customers | Yes | | | |

**Q6.2 Is staging an honest copy of production (same type, same version, same settings)?** `[ ] Yes` `[ ] No - differences are:`
Your answer:

**Q6.3 How is access removed when someone leaves the team or a temporary helper finishes?**
Your answer:

---

# 7. Phase 1: PLAN (Decide What Changes)

**Q7.1 List every database change in this release.**

| ID | Change (plain words) | Type (`Add` / `Change` / `Remove` / `Move data` / `Setting` / `Index`) | Touches existing data? (Y/N) | Risk (`Low` / `Medium` / `High`) | Owner | Status |
|---|---|---|---|---|---|---|
| DB-01 | | | | | | `NOT STARTED` |
| DB-02 | | | | | | |

Example row: `DB-01 | Add "bookings" table | Add | N | Low | Priya | NOT STARTED`

**Q7.2 How do you rate risk? (Use this guide.)**
- **Low:** adds something new; nothing existing is touched.
- **Medium:** changes existing structure or moves/rewrites some data.
- **High:** removes things, rewrites a large table, changes money/identity/security data, or cannot easily be undone.

**Q7.3 Which changes must be made in several small steps so old and new app versions both keep working?** (The "expand, then switch, then clean up" way.)

| Change ID | Step 1: Add new (safe) | Step 2: Move app to new | Step 3: Remove old (later release) |
|---|---|---|---|
| | | | |

**Q7.4 What data will be created, copied, or changed? How much (rows, GB)? How long will it take?**
Your answer:

**Q7.5 Privacy and legal: does this release store or move personal data (names, emails, locations, payments, children's data, health data)?**
`[ ] Yes` `[ ] No`. If yes: what is it, why do you need it, how long do you keep it, which laws apply (GDPR, CCPA, HIPAA, PCI, others)?
Your answer:

**Gate 1: Plan is ready when all are `[x]`:**
- `[ ]` Every change has an owner and a risk level
- `[ ]` High-risk changes have a written reason and a safer alternative considered
- `[ ]` Privacy question answered
- `[ ]` Approver has read the plan

---

# 8. Phase 2: BUILD (Write the Change)

**Q8.1 Where do the change scripts live, and what is the naming rule?**
Example answer: "`/db/migrations/2026_11_14_001_add_bookings_table.sql`, numbered in order, one purpose per file."
Your answer:

**Q8.2 Build rules (tick what you follow; add your own):**
- `[ ]` One purpose per script
- `[ ]` Every script has a matching "undo" script, or a written reason why it cannot
- `[ ]` Scripts can be safely run twice without harm (no double-adding)
- `[ ]` No real customer data in scripts or test files
- `[ ]` Big data moves run in small batches, not all at once
- `[ ]` New columns/fields start empty-allowed or with a safe default
- `[ ]` Indexes on big tables are built without blocking customers
- `[ ]` Naming follows the team style guide: link ______

**Q8.3 Which data is "seed" or reference data (countries, plans, settings) and where is it kept?**
Your answer:

**Gate 2: Build is ready when:**
- `[ ]` All scripts are in the repository (not on someone's laptop)
- `[ ]` Undo scripts exist or exceptions are written down
- `[ ]` Scripts run cleanly on an empty dev database

---

# 9. Phase 3: CODE REVIEW (Second Pair of Eyes)

**Q9.1 Who reviews, and how many approvals are needed?**
Example answer: "2 approvals: 1 database engineer + 1 other developer. The author cannot approve their own work."
Your answer:

**Q9.2 Reviewer checklist (every box must be `[x]` or explained):**

| # | Check | Done |
|---|---|---|
| 1 | The change does only what the plan (Q7.1) says | `[ ]` |
| 2 | No dropping, deleting, or renaming that old app versions still need | `[ ]` |
| 3 | No step locks a busy table for long | `[ ]` |
| 4 | Undo script reviewed and tested | `[ ]` |
| 5 | Indexes exist for the new questions the app will ask | `[ ]` |
| 6 | Rules/constraints protect data quality (required fields, unique values, links between tables) | `[ ]` |
| 7 | Security rules limit who sees what (row-level rules, roles, document rules) | `[ ]` |
| 8 | No secrets, keys, or real data inside the change | `[ ]` |
| 9 | Personal data is minimized, protected, and has a retention plan | `[ ]` |
| 10 | AI-written parts were read line by line by a human | `[ ]` |
| 11 | App code and database change are released in a safe order | `[ ]` |
| 12 | Monitoring and alerts for this change are defined (Section 13) | `[ ]` |

**Q9.3 Where are review comments and approvals recorded?** (link)
Your answer:

**Gate 3:** all required approvals recorded, all review comments resolved.

---

# 10. Phase 4: TEST (Prove It Works)

**Q10.1 Which tests will you run? Tick and name the owner.**

| Test | What it proves | Run? | Owner | Result |
|---|---|---|---|---|
| Run change on empty database | Scripts work from scratch | `[ ]` | | |
| Run change on copy of production-like data | Works on realistic data | `[ ]` | | |
| Run undo script | You can go back | `[ ]` | | |
| Old app version vs new database | Nothing breaks mid-release | `[ ]` | | |
| New app version vs new database | New features work | `[ ]` | | |
| Data check (counts before = counts after) | No data lost or doubled | `[ ]` | | |
| Speed test with expected load | Fast enough at 500 customers (and 10x that) | `[ ]` | | |
| Security test (can user A see user B's data?) | Privacy rules hold | `[ ]` | | |
| Backup restore test | Backups really work | `[ ]` | | |

**Q10.2 What numbers pass or fail a test?**
Example answer: "Every table row count matches within 0; slowest common question under 200 ms; restore finishes in under 30 minutes."
Your answer:

**Q10.3 How is test data made safe? (Fake data, or masked copy of real data?)**
Your answer:

**Gate 4:** all tests pass, failures are fixed or accepted in writing by the approver.

---

# 11. Phase 5: STAGING (Dress Rehearsal)

**Q11.1 Rehearsal steps. Do them exactly as you will on release day, with a timer.**

| Step | Command / action (or link) | Who | Expected time | Actual time | Result |
|---|---|---|---|---|---|
| 1 Take a backup | | | | | |
| 2 Run database changes | | | | | |
| 3 Deploy app version | | | | | |
| 4 Check health (Section 13) | | | | | |
| 5 Practice undo | | | | | |

**Q11.2 What surprised you in the rehearsal and what did you change?**
Your answer:

**Gate 5:** one full rehearsal succeeded, including undo, with times written down.

---

# 12. Phase 6: GO-LIVE (Production Release Day)

## 12.1 Backup and Recovery (Before Anything Else)

**Q12.1 What backups exist, how often, how long are they kept, and where?**
| Data store | Backup type | Frequency | Kept for | Stored where | Last restore test date |
|---|---|---|---|---|---|
| | | | | | |

**Q12.2 Recovery targets (write numbers):**
- Most data you can afford to lose (e.g. "5 minutes of data"): ______
- Longest you can be down (e.g. "30 minutes"): ______

## 12.2 Release-Day Schedule

**Q12.3 When is the release window, and why that time?**
Example answer: "Tuesday 10:00-12:00 UTC, quiet hours for customers, whole team awake, not a Friday."
Your answer:

**Q12.4 Release-day run sheet (fill with real steps).**

| Time | Step | Owner | Done |
|---|---|---|---|
| T-60 min | Team joins call; confirm everyone is present | | `[ ]` |
| T-45 min | Confirm fresh backup exists and is restorable | | `[ ]` |
| T-30 min | Freeze other changes (no one else touches the database) | | `[ ]` |
| T-15 min | Post "release starting" message to team and support | | `[ ]` |
| T-0 | Run database changes | | `[ ]` |
| T+10 min | Run data checks (counts, sample records) | | `[ ]` |
| T+15 min | Deploy app version | | `[ ]` |
| T+30 min | Run health checks and one real test purchase/sign-up with a test account | | `[ ]` |
| T+60 min | Decide: keep or undo. Write the decision here: | | `[ ]` |
| T+120 min | Post "release complete" message | | `[ ]` |

## 12.3 Go / No-Go Checklist (All must be `[x]` to start)

- `[ ]` Gates 1-5 passed
- `[ ]` Fresh backup taken and restore tested within the last 30 days
- `[ ]` Undo plan tested in staging
- `[ ]` Approver is present and says "Go" (name/time: ______ )
- `[ ]` On-call person is present
- `[ ]` Monitoring screens are open
- `[ ]` Support team has been told
- `[ ]` No other big releases or outages happening at the same time

## 12.4 Undo Plan (Rollback)

**Q12.5 When do we undo? (Write clear triggers.)**
Example answer: "Undo if error rate is above 2% for 5 minutes, any data mismatch is found, or checkout fails twice."
Your answer:

**Q12.6 How exactly do we undo? (Numbered steps, who, how long.)**
Your answer:

**Q12.7 What can NOT be undone, and what is the plan for that part?**
Example answer: "Deleting the old column cannot be undone, so we only remove it in a later release, after a backup."
Your answer:

**Gate 6:** release finished, checks pass, approver signs: ______ date: ______

---

# 13. Monitoring, Alerts, and Health Checks

**Q13.1 What do we watch, what is "normal", and when do we raise an alarm?**

| What we watch | Normal | Warning at | Alarm at | Who is told | How (chat / phone / email) |
|---|---|---|---|---|---|
| Errors from the database | | | | | |
| Slow questions (queries) | | | | | |
| Database CPU / memory | | | | | |
| Disk space remaining | | | | | |
| Connections used | | | | | |
| Backup succeeded last night | | | | | |
| Copy (replica) delay, if any | | | | | |
| Data-quality check (e.g. orphan records, duplicates) | | | | | |
| Cost per day (cloud bill) | | | | | |
| Search/vector quality (relevance sample), if used | | | | | |

**Q13.2 Where is the dashboard? (link) Who looks at it, and when? (e.g. every 15 min on release day, daily for 2 weeks)**
Your answer:

**Q13.3 Who is on call, and how do they get woken up?**
Your answer:

---

# 14. Phase 7: LAUNCH WAVES (Customer 1 to Customer 500)

Releasing to everyone at once is risky. Grow in waves. Do not start the next wave until the current wave's exit checks are `[x]`.

**Q14.1 Wave plan (change numbers if your plan differs).**

| Wave | Customers | Who is invited | How long you watch before next wave | Database focus |
|---|---|---|---|---|
| 0: Team and friends | 1-10 | Team, trusted testers | 3 days | Does everything work with real people? |
| 1: Early users | 11-50 | Invited beta users | 1 week | Fix surprises; check data accuracy |
| 2: Growing | 51-200 | Waitlist / limited public | 1-2 weeks | Speed, indexes, slow questions |
| 3: Open | 201-500 | Public sign-ups | Until 500 | Capacity, costs, backups, support load |

**Q14.2 How do you control who gets in? (invite list, feature switch, sign-up cap)**
Your answer:

**Q14.3 Exit checks for each wave (all must be `[x]` to open the next wave).**

| Check | Wave 0 | Wave 1 | Wave 2 | Wave 3 |
|---|---|---|---|---|
| No lost or wrong data found | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Error rate below ______ % | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Slowest common question below ______ ms | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Backup + restore still works | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Disk, memory, connections below ______ % of limit | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Daily cost within budget (______ per day) | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Support tickets about data are fewer than ______ per week | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Approver says "open next wave": name/date | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q14.4 Capacity planning. Estimate and re-check each wave.**

| Item | Now | At 500 customers | At 5,000 customers (just to be safe) |
|---|---|---|---|
| Rows / documents stored | | | |
| Storage size | | | |
| Requests per second at busiest time | | | |
| Monthly database cost | | | |
| Plan limit of the database service | | | |

**Q14.5 If a wave goes badly, what do you do?** (pause sign-ups, go back one wave, undo, fix and retry)
Your answer:

**Q14.6 Further database changes during the launch waves.** Each new change after go-live needs: a mini-plan (Section 7 row), a review (Section 9), a test (Section 10), and an approver. List them here:

| Date | Change | Wave it happened in | Approved by | Result |
|---|---|---|---|---|
| | | | | |

---

# 15. Communication Plan

**Q15.1 Who needs to know, when, and how?**

| Audience | What they need to know | When | Who tells them | Channel |
|---|---|---|---|---|
| Team | Release schedule, freeze | Before | | |
| Leadership | Risk and result | Before / after | | |
| Support team | What changed, what to say if customers ask | Before | | |
| Customers | Planned downtime or new features | Before / after | | |

**Q15.2 Write the short message for customers if something goes wrong. (Honest, calm, no blame.)**
Your answer:

**Q15.3 Incident rules:** Who decides it is an "incident"? Who leads? Where do updates go? When is the first update due (e.g. within 15 minutes)?
Your answer:

---

# 16. Risks, Assumptions, and Open Questions

**Q16.1 Risk register (list at least 5).**

| ID | What could go wrong | Chance (`L/M/H`) | Impact (`L/M/H`) | How we prevent it | If it happens we... | Owner |
|---|---|---|---|---|---|---|
| R1 | Release takes longer than window | | | | | |
| R2 | Data lost or duplicated during move | | | | | |
| R3 | Database slows down as customers grow | | | | | |
| R4 | One customer sees another's data | | | | | |
| R5 | Cloud bill jumps unexpectedly | | | | | |

**Q16.2 Assumptions (things you believe but have not proven).**
Your answer:

**Q16.3 Open Questions / UNKNOWN list (every UNKNOWN from this document goes here).**

| # | Question | Who will answer | Due date | Answer |
|---|---|---|---|---|
| | | | | |

---

# 17. Phase 8: HAND-OFF AND REVIEW (After Customer 500)

**Q17.1 Exit criteria: when is this plan finished?**
- `[ ]` 500 customers reached by the definition in Q3.3
- `[ ]` Two weeks with no data incidents
- `[ ]` Last restore test passed
- `[ ]` All temporary access, test data, and launch switches cleaned up
- `[ ]` Old columns/tables scheduled for removal (the "clean up" step) with a date
- `[ ]` Runbook handed to the ongoing operations owner

**Q17.2 Who owns the database day to day from now on?**
Your answer:

**Q17.3 What was planned vs what actually happened?**

| Measure | Planned | Actual |
|---|---|---|
| Downtime during go-live | | |
| Days from go-live to 500 customers | | |
| Data incidents | | |
| Undos / rollbacks needed | | |
| Total database cost | | |

**Q17.4 Lessons learned (blame-free).**
- What went well:
- What went badly:
- What surprised us:
- What we will change in this template and process next time:

**Q17.5 Sign-off**

| Role | Name | Date | Signature / "Approved" note |
|---|---|---|---|
| Release owner | | | |
| Database approver | | | |
| Product owner | | | |

---

# 18. Quick Final Quality Check (Before Sharing This Document)

- `[ ]` No blank answers remain (each is filled, `UNKNOWN`, or `N/A - reason`)
- `[ ]` Every task has one named owner and a date
- `[ ]` No secrets or real customer data appear anywhere in this file
- `[ ]` Numbers (not words like "fast") are used for goals and alarms
- `[ ]` Undo plan has been tested
- `[ ]` A person who did not write this has read it and can explain the plan back
- `[ ]` All `UNKNOWN`s appear in Section 16.3

---

# Appendix A: Plain-Language Glossary

| Word | Meaning |
|---|---|
| Database | A digital filing cabinet where the product keeps its information |
| Table / collection | One drawer in the cabinet (for example "users") |
| Schema | The rules for what each drawer holds |
| Migration | A recorded, step-by-step change to the database |
| Rollback / undo | Going back to how things were before the change |
| Backup | A saved copy you can restore if something breaks |
| Restore | Putting a backup back |
| Staging | A practice copy of production |
| Production | The real, live version customers use |
| Index | A shortcut that makes looking things up faster |
| Query | A question asked to the database |
| Lock | When the database makes others wait while it changes something |
| Feature switch | An on/off button that controls who sees something new |
| Gate | A "must be true" checklist before moving on |
| Go-live | The moment real customers start using the change |
| Wave | A group of customers let in at the same time |
| On-call | The person who answers if an alarm goes off |
| Row-level security | Rules that make each user see only their own data |
| Embedding / vector | A list of numbers an AI uses to find similar things |

# Appendix B: Filled-In Mini Example (So You Can See What "Good" Looks Like)

**Project:** DogWalk app. **Release:** `db-release-1.0`.
**Q7.1 row:** `DB-01 | Add "bookings" table | Add | N | Low | Priya | DONE`
**Q12.5 answer:** "Undo if error rate is above 2% for 5 minutes, or any booking is missing a payment record."
**Q14.3 Wave 1 answer:** "No lost data found; error rate below 1%; slowest common question below 300 ms; disk under 50%; daily cost under $10; fewer than 3 data support tickets; approved by Priya on 2026-12-03."

# Appendix C: Reference Checklists This Template Draws On

This template combines widely used practices: database change management with versioned migrations, the expand/contract (parallel change) pattern, backup and disaster-recovery planning (RPO/RTO), release readiness and go/no-go reviews, phased or staged rollouts, SRE-style monitoring and incident handling, blameless post-release reviews, and data-privacy basics. Adapt the thresholds (percentages, milliseconds, wave sizes) to each project.
