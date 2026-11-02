# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **What is this file?** It is the **map of all documents** for one project. It does not hold the details. It tells you (and your AI agent) **which document exists, what it is for, where it lives, and whether it can be trusted.**
> **Where does it live?** `Documentation management and institutional knowledge/Documentation_Index.md` (one copy per project).
> **Who is it for?** A founder working with AI agents (Claude / Claude Code), and anyone who joins later, including a beginner.
> **Goal of the project covered:** Build with AI, launch, and serve the **first 500 customers.**

## The 7 steps (do them in order)

| Step | What to do | Time |
|---|---|---|
| 1 | Copy this file into your project's documentation folder. Rename nothing. | 1 min |
| 2 | Fill **Section 1 (Project Snapshot)**. Answer every question. Use the example as a guide. | 10 min |
| 3 | Go to **Section 3 (the four phase tables)**. For each document, set its **Status** and fill the **Path**. | 20 min |
| 4 | If a document is not needed, do not delete the row. Write `N/A` in Status and put the reason in Purpose. | 2 min |
| 5 | Check **Section 4 (AI Agent Reading Rules)**. Change nothing unless you must. | 3 min |
| 6 | Tick the boxes in **Section 5 (Gates)** only when you have proof. | ongoing |
| 7 | Every time a document changes, update its row (Status, Version, Last updated). Add a line to **Section 8 (Change Log)**. | 1 min each |

## The 6 golden rules

1. **Never guess.** If you do not know, write `UNKNOWN` and add a row in **Section 7 (Open Questions)**. A blank is not allowed; `UNKNOWN` is.
2. **One answer per box.** Short and plain. One sentence is enough.
3. **Dates use `YYYY-MM-DD`** (example: `2026-10-19`).
4. **Paths are real.** A path must open a real file. If the file does not exist yet, write `TO-CREATE` and set Status to `Not started`.
5. **Rows marked `EXAMPLE - DELETE ME`** show what a finished row looks like. Delete them after you understand.
6. **Text in `[square brackets]`** is a placeholder. Replace the whole thing, brackets included.

## Status words (use ONLY these)

| Status | Meaning |
|---|---|
| `Not started` | Document is needed but not written |
| `Draft` | Being written; do not rely on it yet |
| `In review` | Written; someone is checking it |
| `Approved` | Checked and OK to rely on |
| `Outdated` | Was right once; now wrong or old. Fix or retire it |
| `Retired` | Replaced or no longer needed; kept for history |
| `N/A` | Not needed for this project (give the reason) |

## Other short codes

- **Document ID** = phase letter + number, for example `A-01`, `B-03`, `C-07`, `D-02`, `E-01`. Never reuse an ID.
- **Owner / Reviewer** = a person's name, or `AI:Claude`, or `AI:Claude + Human:[Name]`. The Reviewer should be a different person or agent than the Owner.
- **Must-have** documents are marked with a star in the document name. For the first 500 customers these are required. Others are "should have".
- **Depends on** = the IDs that must be `Approved` before this document is reliable (example: `A-04, B-02`). Write `None` if nothing.
- **Read when** = the moment a person or AI agent should open it (example: `Before writing any code`).

---

# Documentation Index: [PROJECT NAME]

| Item | Value |
|---|---|
| Template version | 1.0 |
| Index version | [example: 0.1] |
| Last updated | [YYYY-MM-DD] |
| Updated by | [name or AI:Claude] |

---

# Section 1: Project Snapshot

**Instructions:** Answer each question in the last column. Keep each answer to one or two lines.

| # | Question | Example answer | YOUR ANSWER |
|---|---|---|---|
| 1 | What is the project called? | `PetPal` | |
| 2 | What is the short project ID (no spaces)? | `PETPAL` | |
| 3 | In ONE sentence, what does it do? ("This helps ___ to ___.") | `This helps busy dog owners find a nearby dog walker in 2 minutes.` | |
| 4 | Who is it for? (one clear group) | `Dog owners in big cities who work full time` | |
| 5 | What problem does it solve? | `Owners cannot find trusted walkers quickly` | |
| 6 | What stage is the project in right now? (`Discovery` / `Design` / `Build & QA` / `Launch` / `Growth to 500`) | `Design` | |
| 7 | Who is the Owner (final decision maker)? | `Sam Lee` | |
| 8 | Which AI agents or tools are used? | `Claude Code for coding, Claude for writing` | |
| 9 | Where is the code stored? (link or path) | `github.com/samlee/petpal` | |
| 10 | Where is the documentation folder? (path) | `/docs/` | |
| 11 | What does "customer" mean here? (Signed up? Paid? Active in last 30 days?) | `Paid at least once` | |
| 12 | How many customers today? | `0` | |
| 13 | Target date for the 500th customer | `2027-06-30` | |
| 14 | Target launch date (first public release) | `2027-02-01` | |
| 15 | What ONE number tells us the project is working? | `Weekly repeat bookings` | |
| 16 | Budget and time you can spend per month | `$500 and 20 hours/week` | |
| 17 | What must NEVER happen? (safety, legal, money, data) | `Never store card numbers ourselves` | |

---

# Section 2: How the Phases Fit Together

| Phase | Letter | Plain-language question it answers | Ends at |
|---|---|---|---|
| Discovery and Strategy | A | Should we build this, for whom, and how will we know it works? | Gate 0 |
| Design and Architecture | B | What will it look like and how will it be built? | Gate 1 |
| Build and QA | C | Is it built correctly, safely, and tested? | Gate 2 |
| Launch and Growth to 500 | D | Can customers use it, and are we getting to 500 happily? | Gate 5 |
| Shared Knowledge (all phases) | E | What must everyone remember? | Never ends |

---

# Section 3: The Document Tables

**Instructions for every table below**
- Fill **Status**, **Version**, **Last updated**, **Owner**, **Reviewer**, **Path**, **Depends on**, **Read when** for each row.
- The **Purpose** column is pre-filled. Change it only if your project needs a different meaning.
- Need a new document? Add a row at the bottom of the right table with the next free ID.
- Star = must-have for the first 500 customers.

## Phase A: Discovery and Strategy

**Guiding questions (answer in your head or in the documents):**
1. What problem are we solving, and for whom? *(Example: "Dog owners cannot find walkers fast.")*
2. Who else solves it today, and why are they not enough? *(Example: "Facebook groups are slow and unsafe.")*
3. How will we know it works? *(Example: "50% of customers book again within 14 days.")*
4. What could go wrong? *(Example: "Walkers do not show up.")*

| ID | Document name | Purpose | Status | Ver | Last updated | Owner | Reviewer | Path | Depends on | Read when |
|---|---|---|---|---|---|---|---|---|---|---|
| A-00 | *EXAMPLE - DELETE ME: Product Vision* | *One page: the problem, the customer, the promise* | *Approved* | *1.0* | *2026-10-01* | *Sam Lee* | *AI:Claude* | */docs/a-discovery/vision.md* | *None* | *Before any other work* |
| A-01 | Product Vision and Problem Statement ★ | The problem, the customer, the promise, in one page | | | | | | | None | Before any other work |
| A-02 | Target Customer and Personas ★ | Who exactly the customer is, what they need and fear | | | | | | | A-01 | Before design or marketing |
| A-03 | Market and Competitor Research | What alternatives exist and how we are different | | | | | | | A-01 | Before pricing or positioning |
| A-04 | Product Requirements Document (PRD) ★ | What the product must do (features, rules, limits), in priority order | | | | | | | A-01, A-02 | Before writing any code |
| A-05 | Success Metrics and 500-Customer Plan ★ | The numbers that prove it works and the path to 500 | | | | | | | A-01 | Before launch and every month |
| A-06 | Scope, Assumptions and Risks ★ | What is IN, what is OUT, what we are assuming, what could fail | | | | | | | A-04 | Before planning work |
| A-07 | Business Model and Pricing | How we earn money and what customers pay | | | | | | | A-02, A-03 | Before launch |
| A-08 | Budget and Resource Plan | Money, time and tools available | | | | | | | A-06 | Before committing to work |

## Phase B: Design and Architecture

**Guiding questions:**
1. What will the customer do from first click to getting value? *(Example: "Sign up, enter address, pick walker, pay.")*
2. What parts does the system have and how do they talk? *(Example: "Phone app, server, database, payment service.")*
3. What data do we store and how do we protect it? *(Example: "Names and addresses; encrypted; deleted on request.")*
4. Where will AI make decisions, and what are its limits? *(Example: "AI suggests walkers; a human approves refunds.")*

| ID | Document name | Purpose | Status | Ver | Last updated | Owner | Reviewer | Path | Depends on | Read when |
|---|---|---|---|---|---|---|---|---|---|---|
| B-00 | *EXAMPLE - DELETE ME: System Architecture* | *Boxes-and-arrows picture of how the system works* | *Draft* | *0.3* | *2026-10-05* | *AI:Claude* | *Sam Lee* | */docs/b-design/architecture.md* | *A-04* | *Before building or changing structure* |
| B-01 | User Journeys and Wireframes ★ | Screen-by-screen path a customer takes | | | | | | | A-02, A-04 | Before building any screen |
| B-02 | Design System and Brand Guide | Colors, fonts, tone of voice, reusable parts | | | | | | | B-01 | Before building any screen or message |
| B-03 | System Architecture ★ | How the parts fit together and why | | | | | | | A-04 | Before building or changing structure |
| B-04 | Tech Stack and Decision Records (ADRs) ★ | Which tools were chosen, why, and what was rejected | | | | | | | B-03 | Before adding any new tool |
| B-05 | Data Model and Data Flow ★ | What data exists, where it is stored, how it moves | | | | | | | B-03 | Before touching the database |
| B-06 | API and Integration Specification | How our system talks to other systems (payments, email, maps) | | | | | | | B-03 | Before connecting anything external |
| B-07 | Security, Privacy and Compliance Plan ★ | How we protect data and follow laws | | | | | | | B-05 | Before storing real customer data |
| B-08 | AI Agent Design (models, prompts, guardrails) ★ | What the AI does, what it may never do, how we check its work | | | | | | | A-06, B-03 | Before any AI feature or workflow |

## Phase C: Build and QA

**Guiding questions:**
1. Can a new person or AI agent set up and run the project from scratch? *(Example: "Yes, in 10 minutes using the README.")*
2. How do we decide what to build next? *(Example: "Top of the backlog, matching the PRD.")*
3. How do we know something works? *(Example: "Automated tests pass and a human tried it.")*
4. What do AI agents do alone, and what needs a human's OK? *(Example: "Agents write code; a human approves releases.")*

| ID | Document name | Purpose | Status | Ver | Last updated | Owner | Reviewer | Path | Depends on | Read when |
|---|---|---|---|---|---|---|---|---|---|---|
| C-00 | *EXAMPLE - DELETE ME: Test Strategy* | *What we test, how, and what "passing" means* | *In review* | *0.9* | *2026-10-10* | *AI:Claude* | *Sam Lee* | */docs/c-build/test-strategy.md* | *A-04, B-03* | *Before writing tests or approving a release* |
| C-01 | AI Agent Instructions (AGENTS.md / CLAUDE.md) ★ | Rules the AI agent follows in this project | | | | | | | B-03, B-08 | At the start of every AI session |
| C-02 | README and Setup Guide ★ | How to install and run the project | | | | | | | B-04 | When joining or setting up a machine |
| C-03 | Coding Standards and Git Workflow | How code is written, named, reviewed and merged | | | | | | | B-04 | Before writing code |
| C-04 | Backlog and Task Plan ★ | The list of work, in order, with who does it | | | | | | | A-04, A-06 | When choosing the next task |
| C-05 | Execution Plans (per feature) | Step-by-step plan for one large piece of work | | | | | | | C-04 | Before starting a big feature |
| C-06 | Test Strategy and Test Cases ★ | What we test and the checks that must pass | | | | | | | A-04, B-03 | Before writing tests or releasing |
| C-07 | QA Reports and Bug Log ★ | Test results, bugs found, bugs fixed | | | | | | | C-06 | Before every release |
| C-08 | Security Review and Checklist ★ | Proof that security checks were done | | | | | | | B-07 | Before launch and after big changes |
| C-09 | Environments and CI/CD Guide | Test, staging and live setups and how code gets released | | | | | | | B-04 | Before releasing or fixing live problems |
| C-10 | AI Workflow and Prompt Library | Prompts and agent steps that work, with examples | | | | | | | B-08, C-01 | When starting repeatable AI work |
| C-11 | Current State and Handoff Notes ★ | What is done, what is in progress, what is blocked | | | | | | | None | At the start and end of every work session |

## Phase D: Launch and Growth to 500 Customers

**Guiding questions:**
1. What exactly happens on launch day, and who does what? *(Example: "9:00 release, 9:30 smoke test, 10:00 announce.")*
2. How does a new customer learn to use it? *(Example: "3-step welcome screen and a help page.")*
3. How do we help a customer who is stuck or upset? *(Example: "Reply within 24 hours using the FAQ.")*
4. How do we learn from customers and get to 500? *(Example: "Weekly feedback review; 3 outreach channels.")*
5. What do we do if something breaks? *(Example: "Roll back within 15 minutes.")*

| ID | Document name | Purpose | Status | Ver | Last updated | Owner | Reviewer | Path | Depends on | Read when |
|---|---|---|---|---|---|---|---|---|---|---|
| D-00 | *EXAMPLE - DELETE ME: Launch Plan and Checklist* | *Hour-by-hour launch steps and who does each* | *Draft* | *0.2* | *2026-10-12* | *Sam Lee* | *AI:Claude* | */docs/d-launch/launch-plan.md* | *C-07, C-08* | *In the 2 weeks before launch* |
| D-01 | Launch Plan and Checklist ★ | Step-by-step launch with owners and times | | | | | | | C-07, C-08 | In the 2 weeks before launch |
| D-02 | Release Notes and Changelog ★ | What changed in each version, in plain words | | | | | | | C-09 | Every release |
| D-03 | User Guide, Onboarding and Help Center ★ | How customers get started and solve common problems | | | | | | | B-01 | Before launch and when features change |
| D-04 | Support Playbook and FAQ ★ | How to answer customers, with ready answers | | | | | | | D-03 | Before launch and when a customer writes |
| D-05 | Monitoring, Incident Response and Rollback ★ | How we notice problems, fix them, and undo a bad release | | | | | | | C-09 | Before launch and during any outage |
| D-06 | Analytics and Metrics Dashboard Spec ★ | What we measure and where to see it | | | | | | | A-05 | Before launch and in monthly reviews |
| D-07 | Customer Feedback Log ★ | Everything customers tell us and what we did about it | | | | | | | D-04 | Weekly |
| D-08 | Customer Acquisition Plan (1 to 500) ★ | Where customers come from and the plan for each milestone | | | | | | | A-02, A-05, A-07 | Before launch and monthly |
| D-09 | Legal Pages (Terms, Privacy, Refunds) ★ | The rules customers agree to | | | | | | | B-07 | Before launch |
| D-10 | Milestone Reviews and Retrospectives | What we learned at 10, 100 and 500 customers | | | | | | | D-06, D-07 | At each milestone |

## Phase E: Shared Knowledge (all phases)

**Guiding question:** *What must stay true and be remembered even when people or AI agents change?*

| ID | Document name | Purpose | Status | Ver | Last updated | Owner | Reviewer | Path | Depends on | Read when |
|---|---|---|---|---|---|---|---|---|---|---|
| E-00 | *EXAMPLE - DELETE ME: Glossary* | *Plain meaning of every special word we use* | *Approved* | *1.1* | *2026-10-03* | *Sam Lee* | *AI:Claude* | */docs/e-shared/glossary.md* | *None* | *When a word is unclear* |
| E-01 | Glossary ★ | Plain meaning of every special word we use | | | | | | | None | When a word is unclear |
| E-02 | Decision Log ★ | Every big decision, the date, the reason, who decided | | | | | | | None | Before changing a past decision |
| E-03 | Lessons Learned | Mistakes and wins to repeat or avoid | | | | | | | None | Before starting similar work |
| E-04 | Contacts and Access Map | Who to ask, and which accounts and tools exist (never write passwords here) | | | | | | | None | When access or help is needed |

---

# Section 4: AI Agent Reading Rules (Claude / Claude Code)

**Instructions:** Keep this section short and true. Humans: do not change it unless a rule is wrong. Claude Code: read this section at the start of every session.

## 4.1 Where AI agents start

1. Read **this index first**.
2. Read **C-01 (AGENTS.md / CLAUDE.md)** and **C-11 (Current State)**.
3. Use the table in 4.2 to open only the documents the task needs. Do not read everything.

> Tip: Claude Code reads `CLAUDE.md` automatically. Make `CLAUDE.md` point to this file, or make it a link to `AGENTS.md`, so every session begins here.

## 4.2 Task-to-document map (fill the last column with your real paths)

| If the task is... | Read these IDs first | Then confirm status is `Approved` |
|---|---|---|
| Understanding what to build | A-01, A-04, A-06 | A-04 |
| Designing a screen or flow | B-01, B-02, A-02 | B-01 |
| Changing structure or tools | B-03, B-04, E-02 | B-03 |
| Touching data or the database | B-05, B-07 | B-05 |
| Writing or changing code | C-01, C-03, C-04, B-03 | C-01 |
| Building an AI feature | B-08, C-10, B-07 | B-08 |
| Writing or running tests | C-06, A-04 | C-06 |
| Preparing a release | C-07, C-08, C-09, D-01 | C-07 |
| Answering a customer | D-04, D-03, D-07 | D-04 |
| Deciding on growth or pricing | A-05, A-07, D-08, D-06 | A-05 |

## 4.3 Rules the AI must follow

1. **Never guess.** If a needed document is `Not started`, `Draft`, `Outdated` or `UNKNOWN`, **stop and ask the Owner** (listed in Section 1). Do not invent facts.
2. **Trust order when documents disagree:** (1) Decision Log E-02, (2) `Approved` documents, (3) `In review`, (4) `Draft`. Never rely on `Outdated` or `Retired`.
3. **Stay in scope.** Only do what A-04 and A-06 allow. Out-of-scope ideas go in Section 7.
4. **Ask a human before:** deleting data, spending money, changing prices, changing security settings, publishing to customers, or breaking an item listed in Question 17 of Section 1.
5. **Update the paperwork.** After you change or create a document, update its row here (Status, Ver, Last updated) and add a line to Section 8.
6. **Show your work.** Write what you did and what is still open in C-11 at the end of each session.
7. **Do not store secrets** (passwords, keys, card numbers) in any document.

---

# Section 5: Gates (Launch and 500-Customer Checks)

**Instructions:** A gate is a "stop and check" door. Tick `[x]` **only** if you can point to proof (a document ID, link, or number). If one box is empty, do not pass the gate.

## Gate 0: Ready to Design (end of Phase A)
- [ ] A-01, A-02, A-04, A-05, A-06 are `Approved`. Proof: [IDs]
- [ ] "Customer" is defined (Section 1, Q11). Proof: [answer]
- [ ] The success number is chosen (Section 1, Q15). Proof: [number]

## Gate 1: Ready to Build (end of Phase B)
- [ ] B-01, B-03, B-04, B-05, B-07, B-08 are `Approved`. Proof: [IDs]
- [ ] Every big tool choice is in E-02. Proof: [link]

## Gate 2: Ready for Customers to Try (end of Phase C)
- [ ] C-01, C-02, C-06, C-07, C-08 are `Approved`. Proof: [IDs]
- [ ] All tests pass; no open bug that loses data or money. Proof: [QA report date]
- [ ] Security checklist is done. Proof: [C-08]

## Gate 3: Ready to Launch Publicly (start of Phase D)
- [ ] D-01, D-03, D-04, D-05, D-09 are `Approved`. Proof: [IDs]
- [ ] Rollback was practised once. Proof: [date]
- [ ] Analytics shows real numbers (D-06). Proof: [screenshot or link]

## Gate 4: First 10 and First 100 Customers
- [ ] First 10 customers used the product without our help. Proof: [D-07 notes]
- [ ] Top 3 customer complaints are fixed or planned. Proof: [D-07]
- [ ] At 100 customers: success number (Q15) is at or above target. Proof: [number and date]
- [ ] Milestone review written (D-10). Proof: [link]

## Gate 5: 500 Customers Reached
- [ ] 500 customers by the definition in Q11. Proof: [number, date, source]
- [ ] Support answers within the promised time. Proof: [D-04 numbers]
- [ ] No unresolved serious security or legal issue. Proof: [C-08, D-09]
- [ ] Lessons learned recorded (E-03, D-10) and every row in Section 3 is `Approved`, `N/A` or `Retired`. Proof: [date]

---

# Section 6: Keeping This Index Healthy

## 6.1 Review schedule

| How often | What to check | Who |
|---|---|---|
| Every work session | C-11 Current State is updated; changed rows updated here | Whoever worked (human or AI) |
| Weekly | Any `Draft` older than 14 days; any `Outdated` rows; new customer feedback (D-07) | Owner |
| Monthly | Every row's "Last updated" date; success numbers (A-05, D-06) | Owner + Reviewer |
| At every Gate | All "Depends on" documents are `Approved` | Owner |

## 6.2 Rules for old documents

1. A document older than **90 days** with changes in the project since then becomes `Outdated` until checked.
2. Never delete a document. Set it to `Retired`, add the replacement ID in the Purpose column, and note it in Section 8.
3. If two documents disagree, fix the weaker one the same day, or log it in Section 7.

## 6.3 Quick health check (answer Yes or No)

| Question | Yes / No |
|---|---|
| Does every row have a Status? | |
| Does every `Approved` row have a real Path that opens? | |
| Does every Must-have (star) row have an Owner and a Reviewer? | |
| Are there any rows with "Depends on" documents that are not `Approved`? | |
| Is the Change Log (Section 8) up to date? | |

*If any answer is No, fix it before you move to the next gate.*

---

# Section 7: Open Questions and Unknowns

**Instructions:** Every `UNKNOWN` in this file gets a row here. Close it when answered.

| # | Question | Where it was found (ID or Section) | Who can answer | Date asked | Answer | Date closed |
|---|---|---|---|---|---|---|
| 1 | *EXAMPLE - DELETE ME: What is the refund time limit?* | *D-09* | *Sam Lee* | *2026-10-12* | *14 days* | *2026-10-14* |
| 2 | | | | | | |

---

# Section 8: Change Log

**Instructions:** Newest on top. One line per change. Add a line every time you change this file or any row.

| Date | Who | What changed (Index version) | Why |
|---|---|---|---|
| *EXAMPLE - DELETE ME: 2026-10-19* | *AI:Claude* | *B-03 set to Approved (v0.2)* | *Owner approved the architecture* |
| [YYYY-MM-DD] | [name] | Index created (v0.1) | Project start |

---

# Section 9: Final Check Before You Call This File "Done"

- [ ] Section 1 has an answer for every question (or `UNKNOWN` with a row in Section 7).
- [ ] Every row in Section 3 has a Status; the `N/A` rows have a reason.
- [ ] All `EXAMPLE - DELETE ME` rows are removed.
- [ ] Every Path opens a real file (or says `TO-CREATE`).
- [ ] Section 4 points to the right IDs for this project.
- [ ] A different person (or AI agent) read this file and could find any document in under 1 minute.
- [ ] Index version and Last updated date at the top are correct.

---

# Mini Glossary (for beginners)

| Word | Plain meaning |
|---|---|
| Index | A map that says which documents exist and where |
| Document / doc | A written file about one topic |
| PRD | Product Requirements Document: the list of what the product must do |
| ADR | Architecture Decision Record: a short note on a big technical choice and why |
| QA | Quality Assurance: checking that things work before customers see them |
| Gate | A stop-and-check point before moving on |
| Rollback | Undoing a bad release and going back to the last good one |
| AI agent | An AI (like Claude Code) that does tasks for you, such as writing code |
| Path | The address of a file (example: `/docs/a-discovery/vision.md`) |
| Approved | Checked by a second person or agent and safe to rely on |
