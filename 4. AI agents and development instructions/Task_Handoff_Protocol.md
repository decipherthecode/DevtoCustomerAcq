# Task Handoff Protocol

> **Template version:** 1.0 | **Covers:** idea → build → test → launch → first 500 customers
> **Works for:** Human → AI agent, AI agent → AI agent, AI agent → Human
> **Save this file in:** `AI agents and development instructions/Task_Handoff_Protocol.md`

---

# How to Fill This Document

Read this section first. It takes 3 minutes.

## What is this file?
When one person or AI agent gives work to another, the second one often has to **guess** what you meant. Guessing causes mistakes. This file is a **form** that removes the guessing. You fill it in, and the next person or agent knows exactly what to do, what "done" looks like, and when to stop and ask.

## The 10 steps

1. **Copy this file** into your new project folder. Never edit the master template. Rename the copy: `Task_Handoff_Protocol_<ProjectName>.md`.
2. **Fill in Part 1 (Project Setup) once.** This is the only place project facts live (names, tools, links). Everything else points back to it.
3. **Fill in Part 2 (Roles).** Write down who (or which agent) does what. Every role needs a name.
4. **Read Parts 3 to 6 and change only what you must.** These are the safety rules. They already work for most projects.
5. **For every task you hand off, copy the Handoff Packet (Part 7)** and fill it in. One task = one packet.
6. **Use the stage checklists (Part 8)** to know which tasks to create at each stage of the product.
7. **Before calling anything finished, tick the Definition of Done (Part 9).**
8. **The receiver reads the packet and runs the Receiver Checklist (Part 10) before starting.**
9. **Write every handoff in the Handoff Log (Part 13)** and every decision in the Decision Log (Part 14).
10. **Update the Change Log (Part 17)** whenever you edit the protocol itself.

## How to fill each kind of field

| You see | What to do | Example |
|---|---|---|
| `[FILL: ...]` | Replace the whole thing with your answer. | `[FILL: project name]` → `Pet Walker App` |
| `[ ]` | Change to `[x]` when it is true. Leave `[ ]` if not. | `[x] Tests pass` |
| `A / B / C` | Keep **one** option, delete the rest. | `Priority: High` |
| `> Example:` | Read it for help. Delete it when you are done (optional). | |
| `N/A` | Write this if a field truly does not apply, **and add a short reason**. | `N/A - no database in this project` |

## Five golden writing rules
1. **Use simple words.** Short sentences. No secret abbreviations (or explain them in the Glossary).
2. **Be specific.** Not "make it fast." Write "page loads in under 2 seconds."
3. **Use numbers, dates, and links** instead of "soon", "a lot", "the usual place."
4. **Never leave a field empty.** Write your answer, `N/A - reason`, or `UNKNOWN - asking <name>`.
5. **If you are unsure, do not guess.** Use the Stop-and-Ask format (Part 6).

## Quick start (if you only have 10 minutes)
Fill Part 1 → Part 2 → Part 7 for your first task. Do the rest later, but **do not skip Part 5 (Human Approval Gates)**.

## Colour and word meanings
- **MUST** = required, no exceptions.
- **SHOULD** = strongly recommended; skip only with a written reason.
- **MAY** = optional.
- **Sender** = the person or agent giving the task.
- **Receiver** = the person or agent getting the task.

---

# Part 0: Document Control

| Field | Value |
|---|---|
| Project name | [FILL: project name] |
| Protocol owner (a human) | [FILL: name and contact] |
| Date created | [FILL: YYYY-MM-DD] |
| Last updated | [FILL: YYYY-MM-DD] |
| Current protocol version | [FILL: e.g. 1.0] |
| Where this file lives | [FILL: repo path or link] |

---

# Part 1: Project Setup (Fill Once Per Project)

> Everything here is the **single source of truth**. If a fact changes, change it **here only**.

## 1.1 The Product in Plain Words

| Field | Your answer |
|---|---|
| Product name | [FILL] |
| One-sentence description (what it does, for whom) | [FILL] |
| The problem it solves | [FILL] |
| Who the customers are | [FILL] |
| What is **not** part of this product (out of scope) | [FILL] |
| Final goal | **First 500 customers actively using the product** |
| Target date for launch | [FILL: YYYY-MM-DD] |
| Target date for customer #500 | [FILL: YYYY-MM-DD] |

> Example: "Pet Walker App - lets busy dog owners book a trusted local walker in 2 taps. Out of scope: cat sitting, payments in other countries."

## 1.2 What Does "Active Customer" Mean?
(This decides when you can say "we reached 500".)

| Field | Your answer |
|---|---|
| An "active customer" is someone who... | [FILL: e.g. completed signup AND used the main feature at least once] |
| How we count them (tool / report) | [FILL] |
| Who confirms the count | [FILL: name] |

## 1.3 Tools, Tech and Places

| Item | Your answer |
|---|---|
| Code repository link | [FILL] |
| Main branch name | [FILL: e.g. main] |
| Programming languages / frameworks | [FILL] |
| Hosting / cloud provider | [FILL] |
| Database | [FILL or N/A - reason] |
| Task board / tracker link | [FILL] |
| Chat / communication channel | [FILL] |
| Design files link | [FILL or N/A] |
| Documentation folder | [FILL] |
| Test environment link | [FILL] |
| Production (live) link | [FILL or "not yet live"] |
| Analytics tool | [FILL or N/A] |
| Customer support tool | [FILL or N/A] |
| AI agents/models in use | [FILL: names and what each is used for] |

## 1.4 Naming and ID Rules
Use these everywhere so nothing gets confused.

| Thing | Format | Example |
|---|---|---|
| Task ID | `T-###` | `T-014` |
| Handoff ID | `H-###` | `H-027` |
| Blocker / question ID | `Q-###` | `Q-003` |
| Decision ID | `D-###` | `D-008` |
| Assumption ID | `A-###` | `A-005` |
| Risk ID | `R-###` | `R-002` |
| Dates | `YYYY-MM-DD` | `2026-10-17` |
| Time zone for the whole project | [FILL: e.g. UTC] | |

## 1.5 Secrets and Private Data Rules
- **Never** write passwords, API keys, tokens, or customer personal data in this file or in any handoff.
- Write **where the secret is stored** instead.

| Item | Your answer |
|---|---|
| Where secrets are stored | [FILL: e.g. "Password manager vault named X"] |
| Who can grant access to secrets | [FILL: name] |
| Types of private data in this project | [FILL: e.g. emails, addresses, payment info, or none] |

---

# Part 2: Roles and Who Hands Off to Whom

## 2.1 Roles
> A role can be a human **or** an AI agent. One person or agent can hold several roles. Every role MUST have a name.

| Role | What they do | Name (human or agent) | Backup |
|---|---|---|---|
| **Product Owner** | Decides what to build and why. Final say on scope. | [FILL] | [FILL] |
| **Project Manager** | Tracks progress, deadlines, and blockers. | [FILL] | [FILL] |
| **Architect** | Decides how the system is built. | [FILL] | [FILL] |
| **Builder(s)** | Writes code, content, or designs. | [FILL] | [FILL] |
| **QA Tester** | Checks that it works and is safe. | [FILL] | [FILL] |
| **Reviewer** | Reads finished work before it is accepted. | [FILL] | [FILL] |
| **Release Manager** | Puts the product live; can roll it back. | [FILL] | [FILL] |
| **Customer Success / Support** | Helps customers and collects feedback. | [FILL] | [FILL] |
| **Human Approver** | The human who can say "yes" at approval gates (Part 5). | [FILL] | [FILL] |

## 2.2 Who May Hand Off to Whom

Tick what is allowed in this project.

| From → To | Allowed? | Extra rule |
|---|---|---|
| Human → AI agent | [x] | Use a full Handoff Packet (Part 7). |
| AI agent → AI agent | [ ] | Must still use a full packet; Human Approver is copied on every handoff touching an approval gate. |
| AI agent → Human | [x] | Agent writes a "Return Handoff" (Part 7.9). |
| Human → Human | [ ] | Use the same packet so nothing lives only in someone's head. |

> Change `[ ]` to `[x]` for the ones you allow. Add a rule if needed.

## 2.3 Agent Capabilities Card (Fill one per AI agent)

| Field | Your answer |
|---|---|
| Agent name | [FILL] |
| Good at | [FILL: e.g. writing code, tests, docs] |
| NOT allowed to do | [FILL: e.g. deploy to production, spend money] |
| Tools / access it has | [FILL] |
| Memory: does it remember past chats? | Yes / No |
| How it receives work | [FILL: pasted packet / file in repo / task board] |
| How it returns work | [FILL] |

> **Why this matters:** AI agents usually start each task **with no memory**. The packet MUST contain everything needed. Never write "as we discussed."

---

# Part 3: The Golden Rules (No-Guessing Rules)

These apply to every handoff. They are **MUST** rules.

1. **One task, one owner.** At any moment, exactly one named owner holds a task.
2. **Nothing lives only in chat or memory.** If it is not written in the packet or logs, it does not exist.
3. **Do not guess. Ask.** Use the Stop-and-Ask format (Part 6). Never invent missing facts, files, numbers, or requirements.
4. **Stay inside the scope.** Do only what the packet says. Extra ideas go in the "Suggestions" box, not into the work.
5. **Say what you did, and what you did not do.** Honest status. Never report "done" if any check is incomplete.
6. **Show your proof.** Every "done" claim has evidence: a test result, screenshot, link, or file.
7. **Respect the approval gates (Part 5).** No exceptions, even if the task is urgent.
8. **Leave things better and safer than you found them.** Keep a rollback path; never break working things silently.
9. **Keep secrets secret.** See Part 1.5.
10. **Handoffs are acknowledged.** A handoff is not complete until the receiver writes "Accepted" (Part 10).
11. **Log it.** Every handoff goes in the Handoff Log; every decision in the Decision Log; every assumption in the Assumption Log.
12. **When in doubt, stop.** A pause costs minutes. A wrong guess can cost weeks.

---

# Part 4: Status Words

Use **only** these 7 statuses. No other words.

| Status | Meaning | Who sets it |
|---|---|---|
| **Not Started** | Task exists; nobody has begun. | Sender |
| **In Progress** | Owner is actively working. | Owner |
| **Blocked** | Cannot continue. A Stop-and-Ask (Q-###) is open. | Owner |
| **Ready for Review** | Work finished; evidence attached; waiting for review. | Owner |
| **Changes Requested** | Reviewer found problems; back to owner. | Reviewer |
| **Done** | All acceptance criteria and the Definition of Done are met and reviewed. | Reviewer / Product Owner |
| **Cancelled** | Will not be done. A reason is written. | Product Owner |

**Allowed moves:**
`Not Started → In Progress → Ready for Review → Done`
`In Progress ↔ Blocked`
`Ready for Review → Changes Requested → In Progress`
`Any → Cancelled` (Product Owner only, with a reason)

**Staleness rule:** If a task is *In Progress* or *Blocked* for more than [FILL: e.g. 2] working days with no update, the owner MUST post a short update and the Project Manager follows up.

---

# Part 5: Human Approval Gates

An AI agent (or any team member without authority) **MUST STOP and get a written "Yes" from the Human Approver** before doing any of the following.

## 5.1 The Four Gates

| Gate | Stop and ask before... | Examples |
|---|---|---|
| **G1: Money** | Spending money or using paid services | New paid API, upgrading a cloud plan, buying a domain, running large AI jobs |
| **G2: Data and Production** | Deleting or changing data, or touching the live product | Dropping a database table, running a migration on production, deploying, force-pushing, mass-emailing customers |
| **G3: Security and Secrets** | Anything involving keys, passwords, permissions, or personal data | Creating/rotating keys, changing who has access, exporting customer data, adding a new third-party tool that sees customer data |
| **G4: Scope** | Changing what is being built | New feature, removed feature, changed acceptance criteria, changed deadline, changed target customer |

## 5.2 Approval Request Format

| Field | Your answer |
|---|---|
| Gate (G1/G2/G3/G4) | [FILL] |
| Task ID | [FILL: T-###] |
| What I want to do (1-2 sentences) | [FILL] |
| Why it is needed | [FILL] |
| What could go wrong | [FILL] |
| Cost (money/time) | [FILL] |
| Can it be undone? How? | [FILL] |
| My recommendation | [FILL] |
| Deadline for the answer | [FILL] |

## 5.3 Approval Record

| Field | Your answer |
|---|---|
| Decision | Approved / Rejected / Approved with conditions |
| Conditions | [FILL or N/A] |
| Approved by (human name) | [FILL] |
| Date | [FILL: YYYY-MM-DD] |
| Logged as Decision ID | [FILL: D-###] |

> **Rules:** Silence is **not** approval. Approval covers **only** the exact action described. An approval from one task does not carry over to another.

## 5.4 Gate Extras for This Project
(Add rules specific to your project, or write N/A.)
[FILL or N/A - reason]

---

# Part 6: Stop-and-Ask Format (Blockers and Questions)

When something is unclear, missing, or conflicting, **stop that part of the work** and write a question. Keep working on anything that is **not** affected.

## 6.1 Question Card

| Field | Your answer |
|---|---|
| Question ID | [FILL: Q-###] |
| Task ID | [FILL: T-###] |
| Asked by | [FILL] |
| Asked to | [FILL: a named person/role] |
| Date asked | [FILL: YYYY-MM-DD] |
| **The question** (one clear sentence) | [FILL] |
| What I already tried / checked | [FILL] |
| What is blocking me because of this | [FILL] |
| Options I see (A / B / C) and my recommendation | [FILL] |
| What I will do if no answer by the deadline | [FILL: usually "wait" - never "guess" at a gate] |
| Needed by | [FILL: date/time] |
| **Answer** | [FILL: filled by the answerer] |
| Answered by / date | [FILL] |

> Example: "Q-003: The packet says 'send a welcome email' but Part 1.3 lists no email tool. Which email service should I use? Options: A) Mailgun, B) SES. I recommend A. I will keep working on the signup page meanwhile."

## 6.2 Good Questions vs Bad Questions

| Bad | Good |
|---|---|
| "What should I do?" | "Should the signup page ask for a phone number? A) Yes, B) No. I recommend B." |
| "It doesn't work." | "Login returns error 500 after step 3. Log attached. I checked X and Y." |

## 6.3 Response Time Rules
| Priority | Answer needed within |
|---|---|
| Critical (blocks launch or live customers) | [FILL: e.g. 2 hours] |
| High | [FILL: e.g. 1 working day] |
| Normal | [FILL: e.g. 2 working days] |

---

# Part 7: The Handoff Packet (Copy This For Every Task)

> **Copy everything from "7.1" to "7.10" for each task.** Name it `H-###` and log it in Part 13.
> A packet is **good** when the receiver can finish the task with **zero** follow-up questions.

## 7.1 Basics

| Field | Your answer |
|---|---|
| Handoff ID | [FILL: H-###] |
| Task ID | [FILL: T-###] |
| Task title (verb + thing) | [FILL: e.g. "Build the signup page"] |
| Lifecycle stage | Idea & Planning / Design & Build / Testing & QA / Launch / First 500 Customers |
| Sender (name, role) | [FILL] |
| Receiver (name, role) | [FILL] |
| Date handed off | [FILL: YYYY-MM-DD] |
| Priority | Critical / High / Normal / Low |
| Deadline | [FILL: YYYY-MM-DD, time, time zone] |
| Estimated effort | [FILL: e.g. 3 hours] |
| Status | Not Started *(use the words from Part 4)* |

## 7.2 The Goal (Why)

| Field | Your answer |
|---|---|
| In one sentence, what must exist when this is finished? | [FILL] |
| Why does it matter to the product / customers? | [FILL] |
| Which goal in Part 1 does it support? | [FILL] |

## 7.3 Background (What the Receiver Must Know)
> Write as if the receiver has **never seen this project**.

| Field | Your answer |
|---|---|
| What has already been done (with links) | [FILL] |
| Decisions already made that must be respected (D-### IDs) | [FILL] |
| Assumptions currently being made (A-### IDs) | [FILL or None] |
| Related tasks / handoffs | [FILL] |
| Terms the receiver might not know | [FILL or "see Glossary"] |

## 7.4 The Work (What)

**Do exactly this:**
1. [FILL: step or requirement]
2. [FILL]
3. [FILL]

**Do NOT do this (out of scope):**
- [FILL]
- [FILL]

**Inputs given to the receiver** (files, links, data, designs, credentials *location* only):

| Input | Where to find it | Version/date |
|---|---|---|
| [FILL] | [FILL] | [FILL] |

**Outputs expected from the receiver:**

| Output | Format | Where to put it | Name |
|---|---|---|---|
| [FILL] | [FILL] | [FILL] | [FILL] |

**Rules and standards to follow** (coding style, brand, tone, accessibility, legal):
[FILL or "see Part 1"]

## 7.5 Acceptance Criteria (How We Know It Is Right)

> Each line MUST be **checkable with yes/no**. If you cannot test it, rewrite it.

- [ ] AC-1: [FILL: e.g. "A new user can sign up with email in under 60 seconds."]
- [ ] AC-2: [FILL]
- [ ] AC-3: [FILL]
- [ ] AC-4: [FILL]
- [ ] **The shared Definition of Done (Part 9) is also met.**

**How it will be tested/verified** (who, how, with what data):
[FILL]

**Evidence the receiver must attach:** (tick what applies)
- [ ] Test results
- [ ] Screenshot or screen recording
- [ ] Link to code change / file
- [ ] Log output
- [ ] Short written summary
- [ ] Other: [FILL]

## 7.6 Limits and Permissions

| Field | Your answer |
|---|---|
| Receiver MAY (without asking) | [FILL: e.g. edit files in /src/signup, run tests] |
| Receiver MUST ASK FIRST (see Part 5 gates) | [FILL: e.g. new packages, DB changes] |
| Receiver MUST NOT | [FILL: e.g. touch production, change billing] |
| Budget limit | [FILL: amount or "$0 - no spending"] |
| Time limit before the receiver must check in | [FILL: e.g. "after 4 hours or at first blocker"] |
| Data allowed to be used | [FILL: e.g. fake test data only] |

## 7.7 Risks and Watch-Outs

| Risk | How to avoid or handle it |
|---|---|
| [FILL] | [FILL] |

**If it goes wrong:** [FILL: the exact undo/rollback step, or "see Part 11"]

## 7.8 Check-ins and Contacts

| Field | Your answer |
|---|---|
| Who to ask questions (named) | [FILL] |
| Where to ask (channel/tool) | [FILL] |
| Check-in schedule | [FILL: e.g. "short update at end of each day"] |
| Who to tell when finished | [FILL] |
| Who is the backup if the contact is away | [FILL] |

## 7.9 Return Handoff (Receiver Fills This When Finished)

| Field | Your answer |
|---|---|
| Return date/time | [FILL] |
| Final status (Part 4 words) | [FILL] |
| **What I did** (short list) | [FILL] |
| **What I did NOT do, and why** | [FILL or "Everything requested was done"] |
| Acceptance criteria results | AC-1: Pass/Fail · AC-2: Pass/Fail · … |
| Evidence links | [FILL] |
| Files/places changed | [FILL] |
| Assumptions I made (A-### IDs) | [FILL or None] |
| Open questions (Q-### IDs) | [FILL or None] |
| Problems found along the way | [FILL or None] |
| Suggestions (not done, just ideas) | [FILL or None] |
| How to undo my work | [FILL] |
| Recommended next task | [FILL] |
| Time spent vs. estimate | [FILL] |

## 7.10 Review Decision (Reviewer Fills This)

| Field | Your answer |
|---|---|
| Reviewer | [FILL] |
| Date | [FILL] |
| Result | Accepted / Changes Requested |
| What needs changing (numbered, specific) | [FILL or N/A] |
| Final status set | [FILL] |

### Filled-in Mini Example (Delete when using)

> **H-004 · T-007 · "Build the signup page"** · Human → AI agent · Priority High · Deadline 2026-10-20 17:00 UTC
> **Goal:** A visitor can create an account with email + password.
> **Do:** Build page at `/signup` using the design in Figma link; validate email format; show friendly errors.
> **Do NOT:** Add social login; touch the database schema; deploy.
> **Acceptance:** AC-1 valid signup creates user in test DB · AC-2 bad email shows message "Please enter a valid email" · AC-3 passes accessibility check.
> **Ask first:** new packages (Gate G3 if it handles personal data).
> **Evidence:** test results + screenshot.
> **If wrong:** revert the single change set `feat/signup`.

---

# Part 8: Lifecycle Stage Checklists

Use these to decide **which tasks to create** at each stage. Tick items as they become handoff tasks or are finished. Add your own.

## Stage 1: Idea & Planning

**Goal of this stage:** Everyone agrees what is being built, for whom, and how success is measured.

- [ ] Problem statement written (Part 1.1)
- [ ] Target customer described with a real example person/persona
- [ ] Customer interviews or research done (at least [FILL: number])
- [ ] Competitor check done
- [ ] Scope defined: **must-have / nice-to-have / not now**
- [ ] Success metrics set (see Part 12)
- [ ] "Active customer" defined (Part 1.2)
- [ ] Budget and timeline approved (Gate G1 / G4)
- [ ] Legal/privacy basics checked (terms, privacy policy, data laws that apply)
- [ ] Risks listed (Part 11.1)
- [ ] Roles filled (Part 2)
- [ ] Tools chosen and recorded (Part 1.3)
- [ ] Task list/backlog created with IDs

**Exit check (all must be true to move on):** Product Owner signs: [FILL: name / date]

## Stage 2: Design & Build

**Goal of this stage:** A working product built in small, tested pieces.

- [ ] Architecture/plan written and approved (record as Decision D-###)
- [ ] User flows and screens designed
- [ ] Data model defined; personal data identified
- [ ] Security basics planned (login, permissions, secrets storage)
- [ ] Development, test, and live environments set up and kept separate
- [ ] Work split into small tasks (each doable in about a day or less)
- [ ] Each task handed off with a full packet (Part 7)
- [ ] Code is reviewed before merging
- [ ] Automated tests written alongside code
- [ ] Documentation updated as you build (setup steps, how it works)
- [ ] Analytics/tracking added for the metrics in Part 12 (respecting privacy)
- [ ] Error monitoring and logs set up
- [ ] Progress reviewed [FILL: e.g. weekly]

**Exit check:** All "must-have" features built and reviewed. Product Owner signs: [FILL]

## Stage 3: Testing & QA

**Goal of this stage:** Prove it works, is safe, and is understandable before real customers touch it.

- [ ] Test plan written (what, how, who, with what data)
- [ ] Functional tests pass (every must-have feature)
- [ ] Edge cases tested (empty fields, wrong inputs, slow network)
- [ ] Security checks done (secrets not exposed, permissions work, inputs sanitized)
- [ ] Performance checked against targets: [FILL: e.g. page < 2s, 100 users at once]
- [ ] Accessibility checked
- [ ] Works on target devices/browsers: [FILL]
- [ ] Privacy checked (only needed data collected; deletion works)
- [ ] Real people test it (at least [FILL: number] beta users)
- [ ] All bugs triaged: **Critical** (blocks launch) / **Major** / **Minor**
- [ ] Zero open Critical bugs; Major bugs have owner and date
- [ ] Rollback plan tested (Part 11.2)
- [ ] Support and help content ready

**Exit check:** QA Tester and Product Owner sign: [FILL]

## Stage 4: Launch

**Goal of this stage:** Release safely, watch closely, fix fast.

- [ ] Launch date and time chosen (avoid Fridays/holidays unless justified)
- [ ] Launch checklist (below) completed
- [ ] Human Approver gives written approval for go-live (Gate G2)
- [ ] Backup taken before release
- [ ] Release done by named Release Manager
- [ ] Smoke test on live product immediately after release
- [ ] Monitoring watched closely for first [FILL: e.g. 48] hours
- [ ] Customers can reach support
- [ ] Launch announcement sent (Gate G2 if mass email)
- [ ] Launch recorded in Handoff Log and Change Log

**Launch Readiness Checklist (all MUST be "Yes"):**

| Question | Yes/No |
|---|---|
| All Critical and Major bugs fixed or accepted in writing? | |
| Backups and rollback ready and tested? | |
| Monitoring and alerts working? | |
| Support path ready (who answers customers, how fast)? | |
| Terms, privacy policy, and required notices published? | |
| Payment/billing tested (if any)? | |
| Secrets rotated/stored safely? | |
| Human Approver says GO? | |

**Exit check:** Product is live and stable for [FILL: e.g. 7] days. Signed: [FILL]

## Stage 5: First 500 Customers

**Goal of this stage:** Get 500 *active* customers, learn from them, and keep them.

- [ ] Customer acquisition plan written (where the first customers come from)
- [ ] Onboarding is simple and tested (time to first success: [FILL: target])
- [ ] Feedback channel open and checked daily
- [ ] Support questions logged and tagged
- [ ] Weekly review of metrics (Part 12)
- [ ] Top 3 customer problems chosen each week and handed off as tasks
- [ ] Bugs from real use fixed in priority order
- [ ] Customer milestones tracked: 1, 10, 50, 100, 250, 500 (Part 12.3)
- [ ] Stay within budget; ask at G1 before increasing ad/AI/cloud spend
- [ ] Retrospective held at each milestone
- [ ] At customer #500: final report written and signed

**Exit check:** 500 active customers (per Part 1.2 definition), confirmed by [FILL: name / date].

---

# Part 9: Definition of Done (Shared Checklist)

A task is **Done** only when its own acceptance criteria (Part 7.5) **and every item below that applies** are ticked. If an item does not apply, write `N/A - reason`.

- [ ] All acceptance criteria pass, with evidence attached
- [ ] Work is inside the agreed scope (nothing extra, nothing missing)
- [ ] Tests written and passing
- [ ] Nothing that worked before is now broken (regression check)
- [ ] Reviewed by someone other than the creator
- [ ] No secrets, keys, or customer data in code, files, logs, or this document
- [ ] Documentation updated (how to use, how to run, known limits)
- [ ] Errors are handled and messages are understandable
- [ ] Rollback/undo steps written
- [ ] Assumptions logged (Part 14), questions closed or handed over
- [ ] Return Handoff (7.9) completed honestly
- [ ] Handoff Log updated (Part 13)
- [ ] Status set to **Done** by Reviewer / Product Owner (not by the creator)

---

# Part 10: Receiver Checklist (Do This Before Starting)

The receiver reads the packet and answers **before touching the work**.

- [ ] I understand the goal in my own words (write it below)
- [ ] I have every input listed (files, access, links all open)
- [ ] I know exactly what is **in** and **out** of scope
- [ ] Every acceptance criterion is clear and testable
- [ ] I know what I may do, must ask first, and must never do
- [ ] I know the deadline and the check-in schedule
- [ ] I know who to ask and how
- [ ] I see no conflicts or missing facts

**My one-sentence summary of the task:** [FILL]

**Result:**
- All boxes ticked → write **"Accepted"** + date, set status **In Progress**.
- Any box not ticked → write a Question Card (Part 6) and set status **Blocked** *before* starting.

| Field | Your answer |
|---|---|
| Accepted / Questions raised | [FILL] |
| Date and time | [FILL] |
| Accepted by | [FILL] |

---

# Part 11: Risk, Rollback and Incident Handling

## 11.1 Risk Register

| ID | Risk | Chance (Low/Med/High) | Impact (Low/Med/High) | Prevention | If it happens | Owner | Status |
|---|---|---|---|---|---|---|---|
| R-001 | [FILL: e.g. AI agent changes live data by mistake] | | | [FILL: Gate G2] | [FILL] | [FILL] | Open |
| R-002 | [FILL: e.g. Customer data leaks] | | | [FILL] | [FILL] | [FILL] | Open |
| R-003 | [FILL: e.g. Launch bug blocks signups] | | | [FILL] | [FILL] | [FILL] | Open |
| R-004 | [FILL: e.g. Not enough customers by target date] | | | [FILL] | [FILL] | [FILL] | Open |
| R-005 | [FILL: e.g. Key person or agent unavailable] | | | [FILL] | [FILL] | [FILL] | Open |

## 11.2 Rollback Plan (Undoing a Release)

| Field | Your answer |
|---|---|
| What triggers a rollback | [FILL: e.g. signups failing > 5% for 15 min] |
| Who may decide to roll back | [FILL: Release Manager, without waiting for approval] |
| Exact steps to undo | 1. [FILL] 2. [FILL] 3. [FILL] |
| How long it should take | [FILL] |
| Where backups are | [FILL] |
| How to check rollback worked | [FILL] |
| Last time the rollback was tested | [FILL: date] |

## 11.3 Failed Handoff (When a Handoff Goes Wrong)

Signs: wrong thing built, work lost, receiver silent, work not matching packet.

1. **Stop** further work on that task.
2. **Write down** what happened (facts only, no blame).
3. **Tell** the Project Manager and Product Owner.
4. **Check** whether the packet was unclear (fix the packet or this protocol).
5. **Reassign or restart** with a corrected packet.
6. **Log** it in the Decision Log and Change Log.

## 11.4 Incident Handling (Something Broke for Customers)

| Step | Action | Who |
|---|---|---|
| 1. Spot | Alert, customer message, or monitoring notices it | Anyone |
| 2. Declare | Write: what, since when, how many customers affected | Release Manager |
| 3. Severity | **S1** all customers/data at risk · **S2** many customers affected · **S3** few customers/minor | Release Manager |
| 4. Contain | Stop the damage first (roll back, turn off feature). Do not try to fix and investigate at the same time | Release Manager |
| 5. Tell | Update the Human Approver and (if needed) customers, in plain words | Product Owner |
| 6. Fix | Fix with a normal handoff, marked **Critical** | Builder |
| 7. Verify | QA confirms fixed on live | QA Tester |
| 8. Learn | Write a short review within [FILL: e.g. 3 days]: what happened, why, what changes | Project Manager |

**Incident Record**

| Field | Your answer |
|---|---|
| Incident ID | [FILL: INC-###] |
| Severity | [FILL] |
| Start / end time | [FILL] |
| Customers affected | [FILL] |
| Cause | [FILL] |
| Fix | [FILL] |
| Prevent next time | [FILL] |

**S1 incidents involving personal data:** Follow the legal reporting rules that apply to you: [FILL: where the rules and contacts are written].

---

# Part 12: First 500 Customers Tracker

## 12.1 Success Metrics

| Metric | How measured | Target | Checked how often |
|---|---|---|---|
| Active customers (Part 1.2) | [FILL] | **500** | Weekly |
| New signups per week | [FILL] | [FILL] | Weekly |
| Signup → first success rate | [FILL] | [FILL: e.g. 60%] | Weekly |
| Time to first success | [FILL] | [FILL: e.g. < 5 min] | Weekly |
| Customers still active after 7 / 30 days | [FILL] | [FILL] | Weekly |
| Support tickets per 100 customers | [FILL] | [FILL] | Weekly |
| Average support reply time | [FILL] | [FILL] | Weekly |
| Customer happiness (rating or score) | [FILL] | [FILL] | Weekly |
| Crashes / errors per day | [FILL] | [FILL] | Daily |
| Cost per customer | [FILL] | [FILL] | Weekly |

## 12.2 Customer Source Tracker

| Source (where they came from) | Customers | Cost | Notes |
|---|---|---|---|
| [FILL: e.g. friends & family] | | | |
| [FILL: e.g. social media] | | | |
| [FILL: e.g. partner/referral] | | | |
| [FILL: e.g. paid ads (Gate G1)] | | | |

## 12.3 Milestone Checkpoints

At each milestone, hold a short review and write down what was learned.

| Milestone | Date reached | Active customers confirmed by | What worked | What to fix | Tasks created (T-###) |
|---|---|---|---|---|---|
| 1st customer | | | | | |
| 10 customers | | | | | |
| 50 customers | | | | | |
| 100 customers | | | | | |
| 250 customers | | | | | |
| **500 customers** | | | | | |

## 12.4 Customer Feedback Log

| Date | Customer (ID only, no private data) | Channel | Feedback (short) | Type (Bug / Idea / Question / Praise) | Priority | Task created (T-###) | Closed? |
|---|---|---|---|---|---|---|---|
| | | | | | | | |

## 12.5 Feedback Handling Rules
1. Log every piece of feedback within [FILL: 1 working day].
2. Reply to the customer within the time in Part 6.3 / support targets.
3. Group similar feedback; count how many customers mention each problem.
4. Each week, pick the **top 3** problems and turn them into tasks with full packets.
5. Tell customers when their problem is fixed.
6. Never write customer names, emails, or private details into this document. Use customer IDs.

---

# Part 13: Handoff Log

> One row per handoff. Newest at the top.

| Handoff ID | Date | Task ID | From | To | Stage | Accepted (date) | Returned (date) | Result | Notes |
|---|---|---|---|---|---|---|---|---|---|
| H-001 | | T-001 | | | | | | | |

---

# Part 14: Decision and Assumption Logs

## 14.1 Decision Log
(Write down every choice that others must follow.)

| ID | Date | Decision | Why | Options rejected | Decided by | Approval gate (G1-G4 or N/A) |
|---|---|---|---|---|---|---|
| D-001 | | | | | | |

## 14.2 Assumption Log
(An assumption is something we are treating as true but have **not verified**. Review each at every stage exit.)

| ID | Date | Assumption | Who made it | How to check it | Checked? Result | Impact if wrong |
|---|---|---|---|---|---|---|
| A-001 | | | | | | |

> **Rule:** Assumptions are allowed only for **low-risk** items and never at an approval gate. High-risk gaps use the Stop-and-Ask format (Part 6).

## 14.3 Open Questions Log

| Question ID | Task | Asked | Needed by | Status (Open / Answered) |
|---|---|---|---|---|
| Q-001 | | | | |

---

# Part 15: Glossary (Plain-English Words)

| Word | Simple meaning |
|---|---|
| **Handoff** | Giving a task from one person or agent to another, with everything they need. |
| **Sender / Receiver** | The one giving the task / the one getting it. |
| **Packet** | The filled form (Part 7) that travels with the task. |
| **AI agent** | A computer program using AI that can do tasks, like writing code or tests. |
| **Scope** | The edges of the job: what is in and what is out. |
| **Out of scope** | Things we are *not* doing in this task. |
| **Acceptance criteria** | Yes/no checks that prove the task is right. |
| **Definition of Done** | The checks *every* task must pass before it is finished. |
| **Blocker** | Something that stops you from continuing. |
| **Gate (approval gate)** | A stop sign where a human must say yes first. |
| **Assumption** | Something we believe is true but have not checked. |
| **Decision log** | A diary of choices we made and why. |
| **Rollback** | Undoing a release to return to the last good version. |
| **Production / live** | The real product customers use. |
| **Test environment** | A practice copy where it is safe to try things. |
| **Deploy / release** | Putting new work live. |
| **Regression** | Something that used to work and now is broken. |
| **QA** | Quality Assurance: checking that it works and is safe. |
| **Smoke test** | A quick check that the main parts work right after release. |
| **Bug (Critical / Major / Minor)** | A problem. Critical blocks launch; Major hurts a lot; Minor is small. |
| **Metric** | A number we track to see if we are succeeding. |
| **Onboarding** | Helping a new customer get started. |
| **Active customer** | A customer who meets the definition in Part 1.2. |
| **Milestone** | A checkpoint on the way to a goal (e.g. 100 customers). |
| **Incident** | An unexpected problem hurting customers. |
| **Secret** | A password, key, or token that must stay private. |
| **Personal data** | Information that identifies a person (name, email, address). |
| **Retrospective** | A short meeting to learn what went well and what to improve. |
| **Evidence** | Proof the work is done: results, screenshots, links. |
| [FILL: add your own] | [FILL] |

---

# Part 16: FAQ for Beginners

**Q: Do I have to fill in every part?**
A: Fill Parts 0-2 once per project. Fill Part 7 for every task. Parts 3-6 and 9-10 are rules; read them and change only if needed. Parts 11-14 are logs you add to as you go.

**Q: What if a field does not apply?**
A: Write `N/A - <reason>`. Never leave it empty.

**Q: What if I do not know the answer?**
A: Write `UNKNOWN - asking <name>` and open a Question Card (Part 6).

**Q: Can the AI agent fill this in for me?**
A: It can *draft* answers, but a human MUST confirm Parts 1, 2, and 5.

**Q: The task is small. Do I still need a full packet?**
A: Yes, but a small task has small answers. Sections can be one line each.

**Q: Can I add my own sections?**
A: Yes. Add them at the end (Part 18+) and record it in the Change Log.

**Q: What if two agents disagree or two instructions conflict?**
A: Stop. Write a Question Card to the Product Owner. Do not pick one yourself.

**Q: Someone says "just do it quickly, skip the approval."**
A: Approval gates cannot be skipped. If it is truly urgent, ask for a fast answer (Part 6.3, Critical priority).

**Q: How do I reuse this for another project?**
A: Copy the master file, rename it, clear Part 1 to Part 2 answers, empty the logs (Parts 12-14), and fill Part 1 again.

---

# Part 17: Change Log (Edits to This Protocol)

| Version | Date | What changed | Why | Changed by | Approved by |
|---|---|---|---|---|---|
| 1.0 | [FILL: YYYY-MM-DD] | First version of the template | Starting point | [FILL] | [FILL] |

**Rule:** Change the protocol only between tasks, never in the middle of a handoff. Tell everyone who uses it.

---

# Part 18: Final Self-Check (Before You Share This File)

- [ ] Part 0 and Part 1 are fully filled (no `[FILL]` left)
- [ ] Every role in Part 2 has a named person or agent
- [ ] Human Approver is named and reachable
- [ ] No secrets or private customer data are in this file
- [ ] Each active task has its own Handoff Packet
- [ ] Every acceptance criterion is a yes/no check
- [ ] Rollback plan (Part 11.2) is filled and tested
- [ ] "Active customer" is defined (Part 1.2)
- [ ] All logs (Parts 13-14) are up to date
- [ ] Someone who has never seen the project read it and could start work with **zero** questions

**Search tip:** search this file for the text `[FILL` - if you find any, something is still unanswered.

---

*End of Task Handoff Protocol*
