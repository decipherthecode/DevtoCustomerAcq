# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **Time needed:** 20 minutes for the first pass. Then 5–15 minutes at the end of each phase.
> **Who can fill this in:** Anyone. If you can read, you can fill it in. No technical skill needed.
> **Where this file lives:** `/docs/00-documentation-management/Documentation_Standards.md` in the project repo (the repo is the **source of truth**; any copy in Notion or Google Drive is a read-only mirror).

## Step 1: Copy this file

1. Copy this whole file into your new project's `/docs/00-documentation-management/` folder.
2. Keep the file name exactly: `Documentation_Standards.md`.
3. Do **not** delete any section. If something does not apply, write `N/A – because …` (one short reason).

## Step 2: Learn the 6 symbols

| Symbol | Meaning | What you do |
|---|---|---|
| **Q:** | A question | Read it. |
| **Your answer:** | A blank line | Type your answer right after it. |
| **Pick one:** | A list of choices | Delete the choices that do not fit. Keep one. |
| **Pick all that apply:** | A list with `[ ]` boxes | Change `[ ]` to `[x]` for each one that is true. |
| **Example:** | A sample answer for a pretend app called **PlantPal** | Read it for ideas. Never copy it blindly. Delete it when you are done. |
| **[REQUIRED]** / **[IF YES]** | How important it is | `[REQUIRED]` must be filled. `[IF YES]` only if the question before it was "Yes". |

## Step 3: Follow the 5 golden rules

1. **Never guess.** If you do not know an answer, write `UNKNOWN – owner: <name> – due: <date>`. Do not invent one.
2. **One fact, one home.** Write each fact in only one document. Everywhere else, link to it.
3. **Short sentences.** One idea per sentence. No secret abbreviations. (See the Glossary in Part 9.)
4. **Dates are always `YYYY-MM-DD`** (example: `2026-10-19`). Money always shows its currency (example: `USD 9.99`).
5. **A human approves.** AI agents may *draft* any document. Only a human may mark it **Approved**.

## Step 4: Use the status labels

Put one of these at the top of every document:

| Status | Meaning |
|---|---|
| `DRAFT` | Being written. Do not trust it yet. |
| `IN REVIEW` | Written. Waiting for a human to check it. |
| `APPROVED` | A human checked it. It is the truth. |
| `DEPRECATED` | Old. Kept only for history. Link to the replacement. |

## Step 5: Work in order

Fill **Part 0 → Part 1 → Part 2 → Part 3 first** (one time per project). Then work through **Phases 0 to 8** (Part 4) in order. Each phase ends with a **Phase Gate Checklist**. Do not start the next phase until the gate is fully ticked (or each skipped item has a written reason).

## Step 6: Use the Quick Start if you are in a hurry

Fill only the items marked **⭐ QUICK START** in Parts 0–3 and in each phase gate. This gives a safe minimum. Come back later for the rest.

## Table of Contents

- **Part 0:** Document Control and Project ID Card
- **Part 1:** Documentation Principles (the rules)
- **Part 2:** Folder Map and Naming Rules
- **Part 3:** AI-Agent Rules (Claude Code)
- **Part 4:** The Life-Cycle Phases (Phase 0 → Phase 8)
- **Part 4A:** Business Tracks (Marketing and Sales, Finance, Team and Hiring)
- **Part 5:** Writing Quality Standards (includes the RACI table)
- **Appendix A:** A Fully Filled Example (PlantPal)
- **Part 6:** Keeping Knowledge Alive (maintenance, lessons learned)
- **Part 7:** Ready-to-Copy Document Templates
- **Part 8:** Final Master Checklist (launch to customer #500)
- **Part 9:** Glossary
- **Part 10:** Change Log for This File

---

# PART 0: DOCUMENT CONTROL AND PROJECT ID CARD

## 0.1 Document control ⭐ QUICK START

| Field | Your answer |
|---|---|
| Document title | Documentation Standards for **<Project Name>** |
| Template version | `1.1` |
| Project version of this file | `0.1` |
| Status | `DRAFT` |
| Date created | `YYYY-MM-DD` |
| Last updated | `YYYY-MM-DD` |
| Owner (one human, full name) | |
| Backup owner | |
| Reviewer (a different human, if any) | |
| Next review date (every 90 days) | |

## 0.2 Project ID card ⭐ QUICK START

**Q: What is the project called?**
Your answer:
Example: PlantPal

**Q: Give it a short code with no spaces (used in file names).**
Your answer:
Example: `plantpal`

**Q: In one sentence a 10-year-old would understand, what does it do?**
Your answer:
Example: "PlantPal reminds people when to water their plants."

**Q: Who is it for? (Describe one real kind of person.)**
Your answer:
Example: "Busy city workers who keep killing their houseplants."

**Q: What kind of product is it?**
Pick all that apply:
- [ ] Web app / SaaS (people use it in a browser and usually pay monthly)
- [ ] Mobile app, iOS
- [ ] Mobile app, Android
- [ ] Has AI features (chatbot, agent, summaries, etc.)
- [ ] Has an API for other developers
- [ ] Other: ________

**Q: Who are the humans on this project?**

| Name | Role (Owner / Builder / Tester / Support / Other) | How to reach them |
|---|---|---|
| | | |

**Q: Which AI agents help on this project?**
Pick all that apply:
- [ ] Claude Code (main builder)
- [ ] Other coding agent: ________
- [ ] Research agent
- [ ] Support/chat agent for customers
- [ ] None

**Q: What are the 5 key dates?**

| Milestone | Date (`YYYY-MM-DD`) | Real or guess? |
|---|---|---|
| Project start | | |
| Build complete | | |
| Private beta | | |
| Public launch | | |
| Customer #500 target | | |

**Q: What is the single sentence that says "we won" at customer #500?**
Your answer:
Example: "500 people have signed up, and at least 40% still use PlantPal every week."

---

# PART 1: DOCUMENTATION PRINCIPLES (THE RULES)

These rules apply to **every** document in the project. Read them. Tick the box to say you accept each one, or write a change under it.

- [ ] **P1. Docs are part of the product.** A feature is not "done" until its docs are done.
- [ ] **P2. Docs live next to the work.** Docs are plain text files (Markdown) in the repo, saved with every change (docs-as-code).
- [ ] **P3. One source of truth.** Each fact lives in exactly one place. Other places link to it.
- [ ] **P4. Write for the reader, not the writer.** Say who the reader is at the top of each document.
- [ ] **P5. Four kinds of documents. Never mix them.** (This follows the well-known Diátaxis idea.)

| Kind | Reader's goal | Example |
|---|---|---|
| **Tutorial** (learning) | "Teach me from zero." | "Your first plant reminder in 5 minutes" |
| **How-to guide** (doing) | "Help me finish one task." | "How to restore a backup" |
| **Reference** (looking up) | "Tell me the exact facts." | API list, settings list, error codes |
| **Explanation** (understanding) | "Help me understand why." | Why we chose this database |

- [ ] **P6. Decisions get written down.** Every big choice gets a short Decision Record (ADR, Part 7). Future you will forget why.
- [ ] **P7. No secrets in docs.** Never write passwords, API keys, tokens, or customer personal data in any document. Write where the secret is stored instead (example: "stored in the password manager under *PlantPal Prod*").
- [ ] **P8. Every doc has an owner, a status, a date.** (See Part 5.)
- [ ] **P9. Old docs are marked, not deleted.** Mark `DEPRECATED` and link to the new one. Archive after 12 months.
- [ ] **P10. Docs must be testable.** If a doc has steps, someone who did not write it must be able to follow them and get the same result.
- [ ] **P11. Accessible by default.** Headings in order, descriptions for images, no meaning shown by colour alone.
- [ ] **P12. AI drafts, humans decide.** See Part 3.

**Q: Do you want to add or change any principle?**
Your answer:

---

# PART 2: FOLDER MAP AND NAMING RULES

## 2.1 The standard folder map ⭐ QUICK START

Create exactly this tree at the root of the project repo. The numbers keep folders in order.

```
/docs
├── 00-documentation-management/      <- this folder (rules, templates, index)
│   ├── Documentation_Standards.md    <- THIS FILE
│   ├── INDEX.md                      <- list of every doc + status + owner
│   ├── glossary.md                   <- project-specific words (extends Part 9)
│   └── templates/                    <- empty copies of Part 7 templates
├── 01-discovery/                     <- Phase 0: idea, research, customers
├── 02-requirements/                  <- Phase 1: PRD, user stories, scope
├── 03-design-architecture/           <- Phase 2: designs, system map, ADRs
│   └── decisions/                    <- one ADR per file
├── 04-development/                   <- Phase 3: setup, coding rules, API docs
├── 05-quality/                       <- Phase 4: test plans, test reports, bugs
├── 06-security-legal-privacy/        <- Phase 5: risks, policies, compliance
├── 07-release-launch/                <- Phase 6: launch plan, release notes
├── 08-operations-support/            <- Phase 7: runbooks, support, incidents
├── 09-growth-metrics/                <- Phase 8: goals, dashboards, experiments
├── 10-institutional-knowledge/       <- lessons learned, FAQs, history, postmortems
├── 11-marketing-sales/               <- Track A: positioning, messaging, outreach
├── 12-finance-business/              <- Track B: budget, runway, invoicing, tax
├── 13-team-hiring/                   <- Track C: roles, onboarding, contractors
└── 99-archive/                       <- DEPRECATED docs older than 12 months
```

Also at the **repo root** (not in /docs):

```
README.md        <- front door: what it is, how to run it, where docs are
AGENTS.md        <- instructions for ANY AI agent (see Part 3)
CLAUDE.md        <- short file that points Claude Code to AGENTS.md (see Part 3)
CHANGELOG.md     <- what changed in each release
```

**Q: Is your project using this exact folder map?**
Pick one:
- [ ] Yes, exactly.
- [ ] Yes, with changes (list them): ________
- [ ] No (explain why): ________

**Q: Where is the read-only mirror (if any)?**
Pick all that apply:
- [ ] Notion → link: ________
- [ ] Google Drive → link: ________
- [ ] None
**Q: Who updates the mirror, and how often?** Your answer:

## 2.2 File naming rules ⭐ QUICK START

1. Use **lowercase**, words joined with **hyphens**: `release-plan.md` (not `Release Plan.md`).
2. No spaces, no special characters, no accents.
3. Start with the **document type**, then the **subject**: `adr-0007-choose-database.md`.
4. Numbered things use **4 digits**: `adr-0001`, `adr-0002`.
5. Dated things start with the date: `2026-10-19-postmortem-login-outage.md`.
6. Never put a version in the file name (`final-v2-REAL.md` is banned). Versions live inside the file and in git history.
7. The only exception: the standard names at the root (`README.md`, `AGENTS.md`, `CLAUDE.md`, `CHANGELOG.md`) and this file.

| Document type | Name pattern | Example |
|---|---|---|
| Product Requirements | `prd-<topic>.md` | `prd-water-reminders.md` |
| Decision Record | `adr-NNNN-<title>.md` | `adr-0003-use-postgres.md` |
| Runbook | `runbook-<task>.md` | `runbook-restore-database.md` |
| Postmortem | `YYYY-MM-DD-postmortem-<title>.md` | `2026-11-02-postmortem-email-outage.md` |
| Release notes | `release-vX.Y.Z.md` | `release-v1.0.0.md` |
| Test plan | `test-plan-<area>.md` | `test-plan-checkout.md` |
| Lessons learned | `YYYY-MM-DD-lessons-<phase>.md` | `2026-12-01-lessons-launch.md` |

**Q: Any naming rule you want to change?**
Your answer:

## 2.3 The INDEX.md rule ⭐ QUICK START

`INDEX.md` lists **every** document. Add a row the moment you create a document.

| Document | Path | Phase | Owner | Status | Last reviewed |
|---|---|---|---|---|---|
| | | | | | |

**Q: Who keeps `INDEX.md` correct?** Your answer:

## 2.4 Document header (every document starts with this)

```
---
title: <clear title>
type: tutorial | how-to | reference | explanation | decision | template
phase: 0-8
owner: <full name>
status: DRAFT | IN REVIEW | APPROVED | DEPRECATED
created: YYYY-MM-DD
last_reviewed: YYYY-MM-DD
next_review: YYYY-MM-DD
audience: <who reads this>
replaces: <link or "none">
---
```

---

# PART 3: AI-AGENT RULES (CLAUDE CODE)

AI agents (like Claude Code) read files, write code, and write docs. Agents have no memory between sessions, so **the files are their memory**. Good docs = good agent work.

## 3.1 The agent context files ⭐ QUICK START

| File | Purpose | Rule |
|---|---|---|
| `AGENTS.md` (repo root) | The **one** place that tells every AI agent how this project works. | Keep under ~200 lines. Update when rules change. |
| `CLAUDE.md` (repo root) | Used by Claude Code. Keep tiny: it points to `AGENTS.md` and adds Claude-only notes. | Never copy rules into both files. |
| `/docs/00-documentation-management/INDEX.md` | The agent's map of all documents. | Agent must read it before searching. |

**Q: Will you create `AGENTS.md` and `CLAUDE.md` now?**
Pick one:
- [ ] Yes, today.
- [ ] Yes, before Phase 3 (Build) starts.
- [ ] No (reason): ________

**Q: What goes in `AGENTS.md`? Fill each line.**

| Section | Your answer |
|---|---|
| What the project is (1–2 sentences) | |
| How to run it (exact commands) | |
| How to test it (exact commands) | |
| Code style rules (link, do not paste) | |
| Folders agents may edit | |
| Folders agents must **never** edit | |
| Words and names to use (and avoid) | |
| Where the docs index is | `/docs/00-documentation-management/INDEX.md` |
| Who to ask when stuck | |

Example (PlantPal): "Run: `npm run dev`. Test: `npm test`. Never edit `/docs/06-security-legal-privacy/` without a human."

## 3.2 What agents MAY do ⭐ QUICK START

Pick all that apply:
- [ ] Draft new documents from the templates in Part 7.
- [ ] Update docs when code changes (README, API reference, CHANGELOG).
- [ ] Fix typos, broken links, and formatting.
- [ ] Update `INDEX.md` rows.
- [ ] Summarize meetings, research, and bug reports into docs.
- [ ] Propose Decision Records (ADRs) for a human to approve.
- [ ] Run the review checklist in Part 5 on any document.

## 3.3 What agents MUST NOT do ⭐ QUICK START

- [ ] Mark any document `APPROVED` (only a human does this).
- [ ] Write secrets, passwords, keys, or real customer data into any file.
- [ ] Invent facts, numbers, dates, quotes, or links. If unknown, write `UNKNOWN – owner – due date`.
- [ ] Edit legal, privacy, security, or pricing documents without a named human reviewer.
- [ ] Delete documents (mark `DEPRECATED` instead).
- [ ] Change this file (`Documentation_Standards.md`) without human approval.
- [ ] Add a feature or change behaviour without updating the matching doc in the same change.

**Q: Add any extra "never do this" rules.**
Your answer:

## 3.4 The human gate (who approves what) ⭐ QUICK START

| Document type | Agent may draft | Human reviewer (name) | Needed before |
|---|---|---|---|
| Idea, research notes | Yes | | Phase 1 |
| PRD / scope | Yes | | Build starts |
| Architecture and ADRs | Yes | | Build starts |
| Code docs, API reference | Yes | | Each release |
| Test plans and reports | Yes | | Launch |
| Security, legal, privacy | Yes (draft only) | | Launch |
| Pricing, terms, refunds | Yes (draft only) | | Launch |
| Release notes | Yes | | Each release |
| Runbooks, support articles | Yes | | Launch |
| Postmortems, lessons learned | Yes | | Within 5 days |

## 3.5 How to give an agent a good task (the "5-line brief")

Whenever you ask an agent to write or change a document, give it these five lines:

1. **Goal:** What must exist when finished?
2. **Reader:** Who will read it?
3. **Inputs:** Which files or facts to use? (links)
4. **Rules:** Which template and which parts of this standard apply?
5. **Done means:** How will we check it? (example: "All blanks filled; Part 5 checklist passes; no `UNKNOWN` left without owner.")

Example: "Goal: write `prd-water-reminders.md`. Reader: the founder and testers. Inputs: `/docs/01-discovery/customer-interviews.md`. Rules: use the PRD template (Part 7.1). Done means: the Part 5 checklist passes and every open question has an owner."

## 3.6 Agent-memory hygiene

- [ ] After each work session, the agent adds a **3-line note** to `/docs/10-institutional-knowledge/session-log.md`: what changed, what is unfinished, what to do next.
- [ ] Decisions made during the session become ADRs, not chat messages.
- [ ] If chat is the only place a decision exists, it does not exist.

## 3.7 Documenting AI features inside the product (skip if no AI features)

**Q: Does the product itself use AI (prompts, models, agents)?** Pick one: [ ] Yes [ ] No

**[IF YES]** Keep these documents in `/docs/04-development/ai/`:

| Document | What it must say |
|---|---|
| `ai-feature-spec.md` | What the AI does, what it must never do, who it affects |
| `prompts.md` | Every prompt, its purpose, version, and owner |
| `model-register.md` | Model name, provider, version, date chosen, cost per use |
| `evals.md` | The test questions, expected answers, pass score, last result |
| `ai-safety-notes.md` | Known failure modes, safeguards, how a human can step in |
| `ai-costs.md` | Expected cost per user per month; alert limit |
| `ai-human-oversight.md` | When a human reviews AI output, and how a person can stop or override the AI |

**Q: What is the AI allowed and not allowed to do? (Write plain rules.)**

| Question | Your answer |
|---|---|
| What is the AI's one job? | |
| What must it **never** do? (example: give medical advice, share another customer's data, make payments) | |
| What does it say when it does not know? (it must not make things up) | |
| Does it tell people they are talking to an AI? | [ ] Yes [ ] No (explain) |
| Can the AI take actions (send email, change data, spend money)? | [ ] No [ ] Yes, only these: ________ |
| Which actions need a human to click "approve" first? | |

**Q: How will you check the AI before and after launch?**

| Check | Plain meaning | Done? | Pass score | Owner |
|---|---|---|---|---|
| Good-answer test set | 30+ real questions with the right answers written down | [ ] | | |
| Bad-input test set | Tricky or harmful questions (tries to trick it, asks for private data) | [ ] | | |
| Prompt-injection test | Hidden instructions inside pasted text must not control the AI | [ ] | | |
| Privacy test | Customer A can never see customer B's data through the AI | [ ] | | |
| Re-test rule | Re-run all tests when the model, prompt, or data changes | [ ] | | |

**Q: How do you control AI cost and failures?**

| Question | Your answer |
|---|---|
| Max AI spend per customer per month | |
| Max AI spend per day for the whole product (hard stop) | |
| Who is alerted at 80% of the limit? | |
| What happens when the AI provider is down? (backup message, fallback model, or pause feature) | |
| How do customers report a bad AI answer? | |
| Who reads those reports, and how often? | |
| Where is every change to a prompt or model recorded? | `prompts.md` and `model-register.md` |

---

# PART 4: THE LIFE-CYCLE PHASES

**The journey:** Phase 0 Discovery → Phase 1 Requirements → Phase 2 Design → Phase 3 Build → Phase 4 Quality → Phase 5 Security/Legal/Privacy → Phase 6 Launch → Phase 7 Operate and Support → Phase 8 Grow to 500 customers.

**How each phase is laid out:**
1. **Purpose** (why this phase exists)
2. **Required documents** (what must exist)
3. **Questions** (fill these in)
4. **Phase Gate Checklist** (tick before moving on)

> Phases may overlap in real life. The gates still apply: a document is "done" only when its gate item is ticked.

---

## PHASE 0: DISCOVERY (IDEA → "SHOULD WE BUILD THIS?")

**Purpose:** Prove the problem is real before you build anything.
**Folder:** `/docs/01-discovery/`

**Required documents:**

| Document | File name | Required? |
|---|---|---|
| Problem and idea brief | `idea-brief.md` | Yes |
| Customer research notes | `customer-interviews.md` | Yes |
| Competitor list | `competitors.md` | Yes |
| Risks and assumptions | `assumptions-risks.md` | Yes |
| Go / No-go decision | `adr-0001-go-no-go.md` | Yes |

### Questions

**0.1 [REQUIRED] What problem are we solving? (Say it from the customer's view.)**
Your answer:
Example: "I forget to water my plants, so they die."

**0.2 [REQUIRED] How do people solve this today?**
Your answer:
Example: "Sticky notes, phone alarms, or they give up."

**0.3 [REQUIRED] How many people did you talk to? Write what they said (not what you hoped).**

| Person (initials only, no private data) | Date | Their problem in their words | Would they pay? (Y/N/Maybe) |
|---|---|---|---|
| | | | |

**0.4 [REQUIRED] Who are 3 competitors or alternatives, and why do customers pick them?**

| Name | Price | Strength | Weakness |
|---|---|---|---|
| | | | |

**0.5 [REQUIRED] What are the 5 biggest things we are *assuming* but have not proven?**

| # | Assumption | How we will test it | Result |
|---|---|---|---|
| 1 | | | |

**0.6 [REQUIRED] What are the biggest risks?**
Pick all that apply:
- [ ] Nobody wants it
- [ ] Too expensive to build or run
- [ ] Law or privacy problems
- [ ] App store may reject it
- [ ] Depends on one outside company
- [ ] I do not have the skills or time
- [ ] Other: ________

**0.7 [REQUIRED] What is the decision?**
Pick one: [ ] GO [ ] NO-GO [ ] GO, BUT CHANGE THE IDEA (explain): ________
**Who decided, and on what date?** Your answer:

### Phase 0 Gate Checklist

- [ ] ⭐ The problem is written in one clear sentence.
- [ ] ⭐ At least 5 real people were asked (write the number: ___).
- [ ] ⭐ A named human wrote the Go / No-go decision.
- [ ] Competitors listed.
- [ ] Top 5 assumptions listed with a test plan.
- [ ] Documents added to `INDEX.md`.

---

## PHASE 1: REQUIREMENTS (WHAT EXACTLY ARE WE BUILDING?)

**Purpose:** Agree on what the product must do, so nobody guesses later.
**Folder:** `/docs/02-requirements/`

**Required documents:**

| Document | File name | Template |
|---|---|---|
| Product Requirements Document | `prd-<topic>.md` | Part 7.1 |
| User stories | `user-stories.md` | in the PRD |
| Scope: in / out | `scope.md` | in the PRD |
| Success numbers | `success-metrics.md` | below |
| Pricing and plans (draft) | `pricing.md` | below |

### Questions

**1.1 [REQUIRED] Who are the users? Name each type.**

| User type | What they want | How often they use it |
|---|---|---|
| | | |

**1.2 [REQUIRED] Write the user stories (one line each).**
Format: *As a ___, I want to ___, so that ___.*
Example: "As a busy worker, I want a phone reminder, so that I never forget to water."

| ID | Story | Priority (Must / Should / Could / Won't) |
|---|---|---|
| US-01 | | |

**1.3 [REQUIRED] What is IN the first release, and what is OUT?**

| In (we will build) | Out (we will NOT build yet) |
|---|---|
| | |

**1.4 [REQUIRED] What numbers show the product is working?**

| Metric | Plain-English meaning | Starting value | Target by customer #500 |
|---|---|---|---|
| Sign-ups | People who made an account | 0 | 500 |
| Activation | % who do the first key action within 24 hours | | |
| Weekly active | % who come back each week | | |
| Retention (day 30) | % still using after 30 days | | |
| Paying customers | People who pay | | |
| Support tickets per customer | Problems per person | | |

**1.5 [REQUIRED] How will people pay?**
Pick one: [ ] Free [ ] Free trial then paid [ ] Monthly subscription [ ] One-time purchase [ ] Free with ads [ ] Not decided (owner/date): ________
**Price (with currency):** ________

**1.6 [REQUIRED] What must be true for it to be "good enough"? (Non-functional needs)**

| Topic | Question | Your answer |
|---|---|---|
| Speed | How fast must a page or screen load? | |
| Uptime | How much downtime is OK per month? | |
| Devices | Which browsers, phones, and OS versions? | |
| Languages | Which languages at launch? | |
| Accessibility | Which standard? (suggested: WCAG 2.2 level AA) | |
| Data | What data do we store about people? | |
| Scale | How many users must it handle at launch? In 6 months? | |

**1.7 [REQUIRED] What are the open questions?**

| # | Question | Owner | Due | Answer |
|---|---|---|---|---|
| | | | | |

### Phase 1 Gate Checklist

- [ ] ⭐ PRD written and set to `APPROVED` by a human.
- [ ] ⭐ "In" and "Out" lists exist.
- [ ] ⭐ Every user story has a priority.
- [ ] Success numbers have a target for customer #500.
- [ ] No open question without an owner and date.
- [ ] Documents added to `INDEX.md`.

---

## PHASE 2: DESIGN AND ARCHITECTURE (HOW WILL IT WORK?)

**Purpose:** Decide how it will look and how it will be built, and write down why.
**Folder:** `/docs/03-design-architecture/`

**Required documents:**

| Document | File name | Required? |
|---|---|---|
| Design notes (screens, flows) | `design-overview.md` | Yes |
| System map (parts and how they connect) | `architecture-overview.md` | Yes |
| Data map (what we store) | `data-model.md` | Yes |
| Decision Records | `decisions/adr-NNNN-*.md` | One per big choice |
| Tech stack list | `tech-stack.md` | Yes |
| Cost estimate | `cost-estimate.md` | Yes |

### Questions

**2.1 [REQUIRED] Where are the designs?**
Your answer (link to Figma or files):

**2.2 [REQUIRED] List every screen or page and what it does.**

| Screen | Purpose | Linked user story |
|---|---|---|
| | | |

**2.3 [REQUIRED] Which technology will we use? Write the reason for each in one sentence.**

| Part | Choice | Why | ADR link |
|---|---|---|---|
| Front end (what people see) | | | |
| Back end (the "engine") | | | |
| Database | | | |
| Login / accounts | | | |
| Payments | | | |
| Email / notifications | | | |
| Hosting | | | |
| Mobile build and store tools | | | |
| AI model / provider (if any) | | | |
| Monitoring and error tracking | | | |

**2.4 [REQUIRED] Draw or describe how the parts connect.**
Pick one: [ ] Diagram attached (link: ____) [ ] Text description below
Your answer:

**2.5 [REQUIRED] What data do we store?**

| Data item | Example | Personal? (Y/N) | Where stored | How long kept | Who can see it |
|---|---|---|---|---|---|
| | | | | | |

**2.6 [REQUIRED] What outside services do we depend on?**

| Service | What for | Cost | What happens if it goes down? |
|---|---|---|---|
| | | | |

**2.7 [REQUIRED] What will it cost to run per month?**

| Item | At launch | At 500 customers |
|---|---|---|
| Hosting | | |
| Database | | |
| AI / model usage | | |
| Email / SMS | | |
| Other | | |
| **Total** | | |

### Phase 2 Gate Checklist

- [ ] ⭐ Every big choice has an ADR (Part 7.2).
- [ ] ⭐ Tech stack table filled with reasons.
- [ ] ⭐ Data table lists all personal data.
- [ ] System map exists and matches the tech stack.
- [ ] Monthly cost estimate exists for launch and customer #500.
- [ ] Human approved the architecture.
- [ ] Documents added to `INDEX.md`.

---

## PHASE 3: BUILD (MAKING THE PRODUCT)

**Purpose:** Build the product while keeping docs and code in sync.
**Folder:** `/docs/04-development/` (plus root `README.md`, `AGENTS.md`, `CHANGELOG.md`)

**Required documents:**

| Document | File name | Required? |
|---|---|---|
| README | `/README.md` | Yes |
| Setup guide (new person → running app) | `setup-guide.md` | Yes |
| Coding rules | `coding-standards.md` | Yes |
| Branch and release rules | `git-workflow.md` | Yes |
| API reference (if any) | `api-reference.md` | If API |
| Environment settings list (names only, no secrets) | `environment-variables.md` | Yes |
| Changelog | `/CHANGELOG.md` | Yes |
| Mobile build guide | `mobile-build-guide.md` | If mobile |

### Questions

**3.1 [REQUIRED] What are the exact steps for a brand-new person to run the product on their computer?**
Your answer (numbered steps, copy-paste commands):

**3.2 [REQUIRED] Where is the code?**
Your answer (repo link and main branch name):

**3.3 [REQUIRED] How do changes get saved and checked?**

| Question | Your answer |
|---|---|
| Branch naming rule | Example: `feature/short-name`, `fix/short-name` |
| Who reviews changes? | |
| Do automatic checks run before merge? (tests, lint, build) | |
| How are versions numbered? | Suggested: Semantic Versioning `MAJOR.MINOR.PATCH` |

**3.4 [REQUIRED] What are the environment settings? (Names only. Never write the values.)**

| Name | What it controls | Where the real value is stored |
|---|---|---|
| | | |

**3.5 [REQUIRED] The "Definition of Done" for any change. Tick what you require.**
- [ ] Code works and passes tests
- [ ] Matching docs updated in the same change
- [ ] CHANGELOG line added
- [ ] Reviewed by a human
- [ ] No secrets in the change
- [ ] Accessibility checked (if screen changed)
- [ ] Other: ________

**3.6 [IF API] How is every API endpoint documented?**
Must include: name, purpose, who may call it, inputs, outputs, error codes, one working example.
Pick one: [ ] Generated from code (OpenAPI) [ ] Written by hand [ ] N/A

**3.7 [IF MOBILE] What do we need to record for each store?**

| Item | iOS | Android |
|---|---|---|
| Developer account owner | | |
| App ID / bundle name | | |
| Signing keys: **where stored** (never the key itself) | | |
| Min. OS version supported | | |
| Store listing text and screenshots location | | |
| Review notes / test login for store reviewers (where stored) | | |

### Phase 3 Gate Checklist

- [ ] ⭐ README lets a stranger run the product in under 30 minutes.
- [ ] (If AI features) AI safety questions in 3.7 answered and AI tests written.
- [ ] ⭐ `AGENTS.md` and `CLAUDE.md` exist (Part 3).
- [ ] ⭐ `CHANGELOG.md` is updated for every change.
- [ ] Environment settings are listed (names only).
- [ ] API reference matches the real behaviour (if API).
- [ ] Every ADR from Phase 2 is still true (or replaced).
- [ ] Documents added to `INDEX.md`.

---

## PHASE 4: QUALITY (DOES IT WORK?)

**Purpose:** Prove it works, on the devices and for the people we promised.
**Folder:** `/docs/05-quality/`

**Required documents:**

| Document | File name | Required? |
|---|---|---|
| Test plan | `test-plan-<area>.md` | Yes (Part 7.5) |
| Test results report | `test-report-<date>.md` | Yes |
| Bug list (or link to tracker) | `bug-tracker-link.md` | Yes |
| Accessibility check | `accessibility-check.md` | Yes |
| Performance check | `performance-check.md` | Yes |
| Beta test plan | `beta-plan.md` | Yes |

### Questions

**4.1 [REQUIRED] What kinds of tests will you run? Tick and name the owner.**

| Test type | Plain meaning | Will do? | Owner |
|---|---|---|---|
| Unit tests | Small pieces of code work alone | [ ] | |
| Integration tests | Pieces work together | [ ] | |
| End-to-end tests | A "fake person" clicks through whole journeys | [ ] | |
| Manual testing | A human tries it | [ ] | |
| Device testing | Works on target phones/browsers | [ ] | |
| Performance testing | Fast enough under load | [ ] | |
| Accessibility testing | Usable with screen reader, keyboard, zoom | [ ] | |
| Payment testing (test mode) | Money flows work | [ ] | |
| AI evals (if AI) | AI answers pass the test questions | [ ] | |

**4.2 [REQUIRED] List the top 10 user journeys that **must** work.**
Example: "Sign up → add a plant → get a reminder → pay."

| # | Journey | Result (Pass/Fail) | Date tested | Tester |
|---|---|---|---|---|
| 1 | | | | |

**4.3 [REQUIRED] How bad is a bug? Agree the levels.**

| Level | Meaning | Rule |
|---|---|---|
| S1 Critical | Data loss, security hole, payments broken, app unusable | Blocks launch. Fix now. |
| S2 Major | Main feature broken, workaround exists | Blocks launch unless a human signs off. |
| S3 Minor | Annoying but usable | Fix after launch. |
| S4 Cosmetic | Looks wrong | Fix when convenient. |

**4.4 [REQUIRED] Launch rule: how many open bugs are allowed?**

| Level | Allowed open at launch |
|---|---|
| S1 | 0 |
| S2 | |
| S3 | |

**4.5 [REQUIRED] Private beta: who tests, for how long, how do they report problems?**

| Question | Your answer |
|---|---|
| Number of beta testers | |
| Where do we find them? | |
| Start and end dates | |
| How do they send feedback? | |
| What is "beta passed"? | |

### Phase 4 Gate Checklist

- [ ] ⭐ All top-10 journeys passed.
- [ ] ⭐ Zero open S1 bugs.
- [ ] ⭐ Test report saved and `APPROVED` by a human.
- [ ] Accessibility check done (target standard met).
- [ ] Performance targets from Phase 1 met.
- [ ] Beta results written down, including what we changed.
- [ ] Documents added to `INDEX.md`.

---

## PHASE 5: SECURITY, LEGAL AND PRIVACY (IS IT SAFE AND ALLOWED?)

**Purpose:** Protect customers and the business before strangers use the product.
**Folder:** `/docs/06-security-legal-privacy/`

> ⚠️ This template is not legal advice. For anything legal, a qualified person must review. AI may only draft.

**Required documents:**

| Document | File name | Required? |
|---|---|---|
| Security checklist and risks | `security-review.md` | Yes |
| Privacy policy (public) | `privacy-policy.md` | Yes |
| Terms of service (public) | `terms-of-service.md` | Yes |
| What personal data we hold | `data-inventory.md` | Yes |
| Third-party services list | `vendor-list.md` | Yes |
| Incident (breach) plan | `incident-response-plan.md` | Yes |
| Cookie / tracking notes | `tracking-and-cookies.md` | If web |
| Store compliance notes | `store-compliance.md` | If mobile |
| Refund and cancellation policy | `refund-policy.md` | If paid |

### Questions

**5.1 [REQUIRED] Whose personal data do we collect, and in which countries do they live?**
Your answer:

**5.2 [REQUIRED] Which rules might apply?** (Check with a qualified reviewer.)
Pick all that apply:
- [ ] GDPR (people in the EU / UK)
- [ ] CCPA / CPRA (people in California)
- [ ] COPPA / rules for children (users under 13 or 16)
- [ ] HIPAA (health data)
- [ ] PCI-DSS (card payments, usually handled by the payment provider)
- [ ] App Store and Google Play policies
- [ ] Accessibility laws
- [ ] AI-specific rules (EU AI Act, etc.), if AI is used
- [ ] None / not sure → reviewer name: ________

**5.3 [REQUIRED] Security basics. Tick each one that is true today.**
- [ ] Everyone uses a password manager and two-step login on all project accounts
- [ ] Secrets are stored in a secrets manager, never in code
- [ ] Data is encrypted in transit (HTTPS) and at rest
- [ ] Customers can only see their own data (tested)
- [ ] Backups exist and a restore has been **tested**
- [ ] Dependencies are checked for known problems
- [ ] Admin access is limited to named people
- [ ] Logs do not contain passwords or personal data
- [ ] AI prompts cannot leak other customers' data (if AI)

**5.4 [REQUIRED] What do we do if there is a data breach?**

| Step | Who | Within how many hours |
|---|---|---|
| Find out and stop it | | |
| Tell the owner | | |
| Tell customers / authorities if required | | |
| Write a postmortem (Part 7.4) | | |

**5.5 [REQUIRED] Can customers ask us to delete or export their data? How?**
Your answer:

**5.6 [REQUIRED] Who reviewed the legal documents, and when?**
Your answer:

### Phase 5 Gate Checklist

- [ ] ⭐ Privacy policy and terms published (or ready to publish) and reviewed by a qualified human.
- [ ] ⭐ Data inventory lists every kind of personal data.
- [ ] ⭐ Backup restore tested once.
- [ ] ⭐ Breach plan names real people.
- [ ] Store rules checked (if mobile).
- [ ] Vendor list complete.
- [ ] Documents added to `INDEX.md`.

---

## PHASE 6: LAUNCH (GOING PUBLIC)

**Purpose:** Release safely, tell people, and be able to undo it.
**Folder:** `/docs/07-release-launch/`

**Required documents:**

| Document | File name | Required? |
|---|---|---|
| Launch plan | `launch-plan.md` | Yes |
| Launch-day checklist | `launch-day-checklist.md` | Yes |
| Release notes | `release-v1.0.0.md` | Yes (Part 7.6) |
| Rollback plan | `rollback-plan.md` | Yes |
| Launch messages (email, social, store text) | `launch-messages.md` | Yes |
| Go / No-go meeting notes | `go-no-go-launch.md` | Yes |

### Questions

**6.1 [REQUIRED] What is the launch plan in one table?**

| When | What happens | Owner |
|---|---|---|
| T-14 days | Feature freeze | |
| T-7 days | Final test and store submission (if mobile) | |
| T-1 day | Go / No-go meeting | |
| T-0 (launch day) | Release goes live | |
| T+1 day | First check of numbers and feedback | |
| T+7 days | Launch review | |

**6.2 [REQUIRED] How will we know the launch is going well or badly?**

| Signal | Where to look | "Bad" means | Who gets alerted |
|---|---|---|---|
| App is up | | | |
| Errors | | | |
| Sign-ups | | | |
| Payments | | | |
| Support messages | | | |

**6.3 [REQUIRED] How do we undo the release? (Rollback)**
Your answer (numbered steps, who may press the button, how long it takes):

**6.4 [REQUIRED] Launch type**
Pick one: [ ] Soft launch (small group first) [ ] Full public launch [ ] Invite only
**How will the first 50 customers be found?** Your answer:

**6.5 [REQUIRED] Is every customer-facing page ready?**
- [ ] Home / landing page
- [ ] Pricing page
- [ ] Help center / FAQ
- [ ] Contact / support page
- [ ] Privacy policy and terms linked
- [ ] Store listing complete (if mobile)

**6.7 [IF MOBILE] App Store and Google Play submission record.** Put this in `/docs/07-release-launch/store-submission.md`.

| Question | iOS (App Store) | Android (Google Play) |
|---|---|---|
| Developer account type and owner | | |
| Store listing: name, subtitle, description, keywords, category | | |
| Screenshots and preview video: where saved, which device sizes | | |
| Age rating answers and who answered them | | |
| Privacy "nutrition label" / Data safety form: who filled it, date, matches Phase 5 data inventory? | [ ] Yes | [ ] Yes |
| Privacy policy link and support link entered | [ ] | [ ] |
| Test login for store reviewers (where stored, never in this file) | | |
| Review notes for reviewers (how to find the main feature, any hidden steps) | | |
| In-app purchases or subscriptions: names, prices, restore-purchase works? | [ ] | [ ] |
| Permissions requested (camera, location, notifications) and the plain reason for each | | |
| Test channel used before public (TestFlight / internal or closed testing) | | |
| Rollout style (phased / staged percentage / all at once) | | |
| Submission date and build number | | |
| Review result and date | | |

**6.8 [IF MOBILE] If the store rejects the app, what do we do?**

| Step | Owner | Written in |
|---|---|---|
| Copy the exact rejection message into `store-submission.md` | | |
| Find which store rule it names | | |
| Fix, or reply with an explanation | | |
| Note the cause in `10-institutional-knowledge/` so we never repeat it | | |
| Update the launch date in Part 0.2 | | |

**6.9 [IF MOBILE] What if a bad version is already live?**
Your answer (stop the rollout, ship a fixed build, or remove from sale; who decides; the store limits what "rollback" means, so write the real steps):

### Phase 6 Gate Checklist

- [ ] (If mobile) Store submission record complete and privacy answers match the data inventory.
- [ ] ⭐ Go / No-go decision written by a human.
- [ ] ⭐ Rollback plan tested or walked through once.
- [ ] ⭐ Monitoring and alerts are on.
- [ ] ⭐ Support is ready (Phase 7 documents exist).
- [ ] Release notes published.
- [ ] CHANGELOG updated.
- [ ] Launch messages approved.
- [ ] Documents added to `INDEX.md`.

---

## PHASE 7: OPERATE AND SUPPORT (KEEPING IT RUNNING AND HELPING PEOPLE)

**Purpose:** Fix problems fast and help customers well.
**Folder:** `/docs/08-operations-support/`

**Required documents:**

| Document | File name | Required? |
|---|---|---|
| Runbooks (step-by-step fixes) | `runbook-<task>.md` | Yes (Part 7.3) |
| On-call / who-to-call list | `contacts-and-escalation.md` | Yes |
| Support playbook | `support-playbook.md` | Yes |
| Help center articles | `help-<topic>.md` | Yes |
| FAQ | `faq.md` | Yes |
| Incident log | `incident-log.md` | Yes |
| Monitoring and alerts guide | `monitoring-guide.md` | Yes |
| Backup and restore guide | `runbook-backup-restore.md` | Yes |

### Questions

**7.1 [REQUIRED] How can customers reach us?**
Pick all that apply: [ ] Email [ ] In-app chat [ ] Help center only [ ] Social media [ ] Phone
**Promised reply time:** ________ hours

**7.2 [REQUIRED] What are the top 10 questions customers will ask? Write the answer to each.**

| # | Question | Short answer | Help article link |
|---|---|---|---|
| 1 | | | |

**7.3 [REQUIRED] How serious is a problem? (Incident levels)**

| Level | Meaning | Respond within | Who is told |
|---|---|---|---|
| SEV1 | Everything down, data at risk, or payments broken | 15 minutes | |
| SEV2 | A main feature is broken for many people | 1 hour | |
| SEV3 | A small problem or a few people | 1 business day | |

**7.4 [REQUIRED] Which runbooks must exist? Tick when written.**
- [ ] The app is down
- [ ] Restore from backup
- [ ] Roll back a release
- [ ] Payment problems
- [ ] Email/notifications not sending
- [ ] Login problems / locked-out customers
- [ ] A customer asks to delete their data
- [ ] AI feature gives wrong or harmful output (if AI)
- [ ] Rotate a leaked secret
- [ ] Other: ________

**7.5 [REQUIRED] When something goes wrong, what happens afterward?**
Rule: Every SEV1 and SEV2 gets a **postmortem within 5 business days**, using Part 7.4. It is **blameless**: it asks "what failed?", never "who failed?".

**7.6 [REQUIRED] How do customer complaints turn into improvements?**
Your answer (where feedback is collected, who reads it weekly, where it is logged):

### Phase 7 Gate Checklist

- [ ] ⭐ Top-10 customer questions have written answers.
- [ ] ⭐ Runbooks for "down", "restore backup", and "roll back" are written and tried once by someone who did not write them.
- [ ] ⭐ Incident levels and the contact list name real people.
- [ ] Support playbook written.
- [ ] Help center published.
- [ ] Alerts reach a human who will wake up.
- [ ] Documents added to `INDEX.md`.

---

## PHASE 8: GROW TO THE FIRST 500 CUSTOMERS

**Purpose:** Learn from real customers, grow safely, and keep docs true.
**Folder:** `/docs/09-growth-metrics/` and `/docs/10-institutional-knowledge/`

**Required documents:**

| Document | File name | Required? |
|---|---|---|
| Growth goals and milestones | `growth-milestones.md` | Yes |
| Weekly numbers log | `weekly-metrics.md` | Yes |
| Customer feedback log | `feedback-log.md` | Yes |
| Experiments log | `experiments.md` | Yes |
| Roadmap (next 90 days) | `roadmap.md` | Yes |
| Lessons-learned notes | `YYYY-MM-DD-lessons-<topic>.md` | At each milestone |
| Support trends | `support-trends.md` | Monthly |

### Questions

**8.1 [REQUIRED] Fill the customer milestone table. Use it for the whole journey.**

| Milestone | Date reached | What we must check at this milestone | Done? |
|---|---|---|---|
| Customer #1 | | The first customer completed signup and the key action. Watch them if possible. | [ ] |
| Customer #10 | | Read every piece of feedback. Fix top 3 problems. Update FAQ. | [ ] |
| Customer #50 | | Are support questions repeating? Turn each one into a help article. Check cost per customer. | [ ] |
| Customer #100 | | Review security, backups, and cost. Run a restore test. Write a lessons-learned doc. Review all `APPROVED` docs older than 90 days. | [ ] |
| Customer #250 | | Check performance under growth. Review pricing and refunds. Update the roadmap from real data. | [ ] |
| Customer #500 | | Hold a full review (see Phase 8 Gate). Decide: scale, fix, change, or stop. | [ ] |

**8.2 [REQUIRED] What do we look at every week? (Fill once, then keep the log up to date.)**

| Metric | This week | Last week | Change | Note |
|---|---|---|---|---|
| New sign-ups | | | | |
| Activated (did the key action) | | | | |
| Weekly active users | | | | |
| Paying customers | | | | |
| Cancellations and why | | | | |
| Support tickets | | | | |
| Top bug | | | | |
| Monthly running cost | | | | |

**8.3 [REQUIRED] How do we run experiments safely?**

| Experiment | What we change | What we expect | Start / end | Result | Keep / drop |
|---|---|---|---|---|---|
| | | | | | |

**8.4 [REQUIRED] How do we keep docs true while the product changes?**
Rule: Any change to behaviour must update its doc **in the same change**. Once a month, run the **Docs Health Check** in Part 6.2.

**8.5 [REQUIRED] What is our plan if growth is faster than expected?**

| Risk | Early warning | What we do |
|---|---|---|
| Servers too slow | | |
| Costs too high (especially AI usage) | | |
| Support overwhelmed | | |
| Fraud or abuse | | |

### Phase 8 Gate Checklist (at customer #500)

- [ ] ⭐ 500 customers reached (date: ______).
- [ ] ⭐ Success sentence from Part 0.2 checked: **met / not met**.
- [ ] ⭐ A full "Lessons Learned" document is written for the whole journey (Part 7.7).
- [ ] ⭐ All docs reviewed in the last 90 days, or marked `DEPRECATED`.
- [ ] Top 10 support questions updated from real data.
- [ ] Costs per customer calculated.
- [ ] Roadmap for the next 90 days written.
- [ ] Decision recorded: Scale / Fix / Change direction / Stop (human decision).
- [ ] This standards file updated with what we learned (Part 10).

---

# PART 4A: BUSINESS TRACKS (RUN ALONGSIDE PHASES 0 TO 8)

These three tracks are not phases. They run at the same time as the phases. Each has its own folder, documents, questions, and a track gate.

| Track | Starts at | Folder | Must be ready before |
|---|---|---|---|
| A: Marketing and Sales | Phase 1 | `/docs/11-marketing-sales/` | Phase 6 (launch) |
| B: Finance and Business | Phase 0 | `/docs/12-finance-business/` | Phase 6 (launch) |
| C: Team and Hiring | Phase 2 | `/docs/13-team-hiring/` | Phase 3 (build) |

## TRACK A: MARKETING AND SALES

**Required documents:**

| Document | File name |
|---|---|
| Positioning and message | `positioning.md` |
| Customer profile (who we sell to) | `ideal-customer.md` |
| Landing page and store copy | `website-copy.md` |
| Channel plan (how we find the first 500) | `channel-plan.md` |
| Outreach scripts (emails / messages) | `outreach-scripts.md` |
| Sales or sign-up flow | `signup-flow.md` |
| Brand rules (name, logo, colours, tone) | `brand-guide.md` |
| Marketing results log | `marketing-results.md` |

**A.1 [REQUIRED] Fill the positioning card.**

| Question | Your answer |
|---|---|
| For (who)... | |
| Who need (problem)... | |
| Our product is a (type)... | |
| That gives (main benefit)... | |
| Unlike (alternative)... | |
| Because (proof we can show)... | |

**A.2 [REQUIRED] Where will the first 500 customers come from? Give a target number per channel.**

| Channel | Example | Target customers | Cost per customer | Owner | Start date |
|---|---|---|---|---|---|
| Friends, beta list, waiting list | | | | | |
| Social media | | | | | |
| Communities and forums | | | | | |
| Search (SEO) / content | | | | | |
| Paid ads | | | | | |
| Partnerships / referrals | | | | | |
| App store search (if mobile) | | | | | |

**A.3 [REQUIRED] How do we talk to customers? (Rules for AI and humans)**
- [ ] No false promises or made-up reviews, numbers, or customer quotes.
- [ ] Every claim in marketing can be shown to be true (link the proof).
- [ ] Every email includes an unsubscribe link and our real contact.
- [ ] Human approves all public posts before they go out.
- [ ] Tone: ________ (example: friendly, calm, no hype)

**Track A gate:**
- [ ] ⭐ Positioning card complete.
- [ ] ⭐ Channel plan with numbers for 500 customers.
- [ ] ⭐ Landing page and store text approved by a human.
- [ ] Brand guide exists.
- [ ] Results log is started.

## TRACK B: FINANCE AND BUSINESS

> This is not accounting, tax, or legal advice. A qualified accountant must check numbers and tax questions.

**Required documents:**

| Document | File name |
|---|---|
| Budget and runway | `budget-and-runway.md` |
| Pricing logic | `pricing-logic.md` |
| Business accounts register (names only) | `accounts-register.md` |
| Invoicing, refunds, and tax notes | `billing-and-tax.md` |
| Subscriptions and renewals list | `subscriptions-renewals.md` |
| Monthly money review | `monthly-money-review.md` |

**B.1 [REQUIRED] How much money do we have, and how long will it last?**

| Question | Your answer (with currency) |
|---|---|
| Money available now | |
| Planned monthly spend | |
| **Runway** (months until money runs out) | |
| Date we must decide to raise money, earn money, or stop | |

**B.2 [REQUIRED] What are all the costs?**

| Cost | One-time or monthly | Amount | Renewal date | Owner |
|---|---|---|---|---|
| Hosting and tools | | | | |
| AI / model usage | | | | |
| Store fees (Apple / Google) | | | | |
| Payment fees | | | | |
| Domain | | | | |
| Legal / accounting | | | | |
| Marketing | | | | |
| People / contractors | | | | |

**B.3 [REQUIRED] Pricing and break-even**

| Question | Your answer |
|---|---|
| Price per customer per month | |
| Average cost to serve one customer per month | |
| Profit per customer per month (price minus cost) | |
| Customers needed to cover monthly costs (break-even) | |
| Refund and cancellation rule | |

**B.4 [REQUIRED] Money safety.**
- [ ] Business money is in a separate account from personal money.
- [ ] At least two named humans know where all money accounts are (handover test, Part 6.6).
- [ ] Payment provider account has two-step login.
- [ ] Sales tax / VAT questions have been asked to an accountant (name: ________).
- [ ] Monthly review of costs is on the calendar.

**Track B gate:**
- [ ] ⭐ Runway and break-even calculated and dated.
- [ ] ⭐ Refund rule written and matches the public refund policy.
- [ ] ⭐ Accountant or qualified reviewer named for tax questions.
- [ ] All renewals listed with dates.

## TRACK C: TEAM AND HIRING

**Required documents:**

| Document | File name |
|---|---|
| Who does what (roles) | `roles.md` |
| Onboarding guide for new people | `onboarding.md` |
| Contractor rules and agreement checklist | `contractors.md` |
| Access list (who can open what, names only) | `access-list.md` |
| Offboarding checklist | `offboarding.md` |
| Hiring plan | `hiring-plan.md` |

**C.1 [REQUIRED] What jobs must someone do? Who does them today?**

| Job | Person today | Backup | Hours per week |
|---|---|---|---|
| Product decisions | | | |
| Building | | | |
| Testing | | | |
| Support | | | |
| Marketing | | | |
| Money and admin | | | |

**C.2 [REQUIRED] Which jobs do we need help with before customer #500?**

| Job | Why needed | When | Employee or contractor? | Budget |
|---|---|---|---|---|
| | | | | |

**C.3 [REQUIRED] Onboarding: what does a new person need on day 1?**
- [ ] Read `README.md`, this standards file, and `AGENTS.md`
- [ ] Access to only the tools they need (least access)
- [ ] A named buddy
- [ ] First small task with a written "done means"
- [ ] Signed agreement (reviewed by a qualified person): ________

**C.4 [REQUIRED] Offboarding: when someone leaves, what do we do the same day?**
- [ ] Remove access to code, hosting, accounts, and mirrors
- [ ] Change any shared secrets they knew
- [ ] Move their documents' ownership to someone else
- [ ] Update `INDEX.md` owners and `access-list.md`

**Track C gate:**
- [ ] ⭐ Every document in `INDEX.md` has a current owner.
- [ ] ⭐ Offboarding checklist exists.
- [ ] Contractor rules written (ownership of work, confidentiality) and reviewed by a qualified person.

---

# PART 5: WRITING QUALITY STANDARDS

## 5.1 Style rules ⭐ QUICK START

| Rule | Do | Don't |
|---|---|---|
| Short sentences | "Click Save." | "It is recommended that the user should click on the save button." |
| Active voice | "The app sends an email." | "An email is sent." |
| One idea per paragraph | | Wall of text |
| Same word, same meaning | Always "customer" (or always "user") | Mixing words |
| Explain every short form on first use | "Product Requirements Document (PRD)" | "PRD" with no explanation |
| Numbered steps for actions | 1, 2, 3 | A paragraph of instructions |
| Show an example | A real sample | "etc." |
| Say how you know | "Tested on 2026-10-19" | "I think it works" |

**Q: Which one word will you use for the people who use the product?**
Pick one: [ ] customer [ ] user [ ] member [ ] other: ________

## 5.2 Review checklist (run on EVERY document before IN REVIEW) ⭐ QUICK START

**Complete and clear**
- [ ] Header filled (title, owner, status, dates, audience).
- [ ] The first 3 lines say what this is and who it is for.
- [ ] Every blank is filled, or says `UNKNOWN – owner – due date`, or `N/A – reason`.
- [ ] No "TBD", "later", "etc." without an owner.

**True and checkable**
- [ ] Every number has a unit and a date.
- [ ] Every claim has a link or a test.
- [ ] Steps were followed by a second person (or by the agent in a clean session).
- [ ] Links work.

**Safe**
- [ ] No passwords, keys, tokens, or real customer data.
- [ ] No private person's details.

**Tidy**
- [ ] Right folder, right file name, added to `INDEX.md`.
- [ ] Headings in order (one `#`, then `##`, then `###`).
- [ ] Images have text descriptions.
- [ ] Spelling checked.

## 5.3 Roles in a document (so nobody guesses)

| Role | Who | What they do |
|---|---|---|
| **Owner** | One human | Answers for the document being true and current |
| **Author** | Human or AI agent | Writes the draft |
| **Reviewer** | A human who is not the author | Checks against 5.2 |
| **Approver** | A human | Sets status to `APPROVED` |

For a solo founder: you may be Owner and Approver, but an AI agent should be the Author and a **fresh agent session** the checker. Wait one night before approving anything legal, pricing, or security.

## 5.4 Who does what: the RACI table ⭐ QUICK START

**R** = Responsible (does the work) · **A** = Accountable (final yes or no; only **one** A per row) · **C** = Consulted (asked first) · **I** = Informed (told after)

Write a name or role in each box. Leave nothing blank. Use `—` if a person is not involved.

| Document or task | Founder / Owner | Builder (human) | AI agent | Tester | Support | Legal / Accountant (outside) |
|---|---|---|---|---|---|---|
| Idea brief and Go / No-go (Phase 0) | A | C | R (draft) | — | I | — |
| PRD (Phase 1) | A | C | R (draft) | C | C | — |
| Architecture and ADRs (Phase 2) | A | R | R (draft) | I | — | — |
| README, setup, API docs (Phase 3) | I | A | R | C | I | — |
| Test plan and report (Phase 4) | I | C | R (draft) | A | I | — |
| Privacy, terms, refund policy (Phase 5) | A | C | R (draft only) | — | I | C (must review) |
| Launch plan and rollback (Phase 6) | A | R | R (draft) | C | C | — |
| Runbooks and support articles (Phase 7) | I | A | R (draft) | C | R | — |
| Weekly metrics (Phase 8) | A | I | R | — | C | — |
| Budget and pricing (Track B) | A | C | R (draft) | — | — | C |
| Positioning and copy (Track A) | A | C | R (draft) | — | C | — |
| This standards file | A | C | R (draft) | — | — | — |

**Q: Does your team match this table?**
Pick one: [ ] Yes [ ] No, changes: ________
**Rule:** if there are no humans besides the founder, the founder holds every **A** and the "fresh agent session" does the **C** check.

---

# PART 6: KEEPING KNOWLEDGE ALIVE

## 6.1 Review rhythm ⭐ QUICK START

| Document group | Review how often | Who |
|---|---|---|
| Legal, privacy, security | Every 90 days, and on any change in law or data use | Owner + qualified reviewer |
| Runbooks and support | Every 90 days; also after every incident | Owner |
| Architecture and ADRs | Every 6 months, and on big changes | Owner |
| PRD and roadmap | Every month during growth | Owner |
| README and setup guide | Every release | Builder |
| Glossary and FAQ | Every month | Support owner |

## 6.2 Monthly Docs Health Check (15 minutes)

- [ ] Open `INDEX.md`. Is every doc listed? Is every owner a real person?
- [ ] Any `APPROVED` doc not reviewed in 90 days? Review or mark `DEPRECATED`.
- [ ] Any doc with `UNKNOWN` past its due date? Chase the owner.
- [ ] Does the README setup still work on a clean machine?
- [ ] Did we ship anything this month without updating its doc?
- [ ] Are the top 5 support questions in the FAQ?
- [ ] Is `AGENTS.md` still true?
Record the result in `/docs/10-institutional-knowledge/docs-health-log.md`.

## 6.3 Institutional knowledge: what we keep forever ⭐ QUICK START

Tick what you will keep in `/docs/10-institutional-knowledge/`:
- [ ] Decision history (ADR index)
- [ ] Lessons learned per phase
- [ ] Postmortems
- [ ] Session log for AI agents
- [ ] "Why we did not build X" list
- [ ] Customer insights summary
- [ ] People and role history
- [ ] Vendor history (why we picked them, what we paid)
- [ ] Reusable prompts and checklists

## 6.4 Lessons learned: when to write one

Write a lessons-learned note (Part 7.7) at: end of every phase, after every SEV1/SEV2, at customers #100 and #500, and any time you say "we should never do that again."

## 6.5 Deprecating and archiving

1. Change status to `DEPRECATED`.
2. Add at the top: "Replaced by: <link>" and the date.
3. Update `INDEX.md`.
4. After 12 months, move it to `/docs/99-archive/` (keep git history; do not delete).

## 6.6 Handing the project to someone else (the "Bus Test")

**Q: If you disappeared tomorrow, could a stranger run the product using only the docs?**
Pick one: [ ] Yes, I tested it. [ ] Not yet.
**Checklist for a handover:**
- [ ] README, setup guide
- [ ] Where every account lives (names only; credentials in the password manager with an emergency-access contact)
- [ ] Who to call (contacts file)
- [ ] Runbooks
- [ ] Cost list and renewal dates
- [ ] Domain, store, and payment account owners

---

# PART 7: READY-TO-COPY DOCUMENT TEMPLATES

Copy a template into a new file, add the Part 2.4 header, and fill every blank.

## 7.1 PRD (Product Requirements Document) Template

```
# PRD: <feature or product name>

## 1. In one sentence
<what it is and who it is for>

## 2. The problem
<the problem in the customer's words; link to evidence>

## 3. Goals and non-goals
Goals:
- 
Non-goals (we will NOT do):
- 

## 4. Users and stories
| ID | As a... | I want... | So that... | Priority |
|---|---|---|---|---|

## 5. Requirements
| ID | Requirement | How we will check it (test) |
|---|---|---|

## 6. Screens and flows
<link to designs>

## 7. Success numbers
| Metric | Now | Target | How measured |
|---|---|---|---|

## 8. Risks and open questions
| # | Item | Owner | Due | Answer |
|---|---|---|---|---|

## 9. Release plan
<when, to whom, how we undo it>
```

## 7.2 ADR (Architecture Decision Record) Template

```
# ADR-NNNN: <short decision title>

Status: PROPOSED | ACCEPTED | SUPERSEDED by ADR-NNNN
Date: YYYY-MM-DD
Decider (human): <name>

## The situation (context)
<what problem forced a choice?>

## Options we looked at
1. <Option A> – good: … / bad: …
2. <Option B> – good: … / bad: …

## The decision
We will <choice>, because <one or two plain reasons>.

## What happens because of this
Good: 
Bad / costs: 
What would make us change our mind: 
```

## 7.3 Runbook Template

```
# Runbook: <task, e.g. "Restore the database">

When to use this: <the exact situation or alert>
Who may do this: <names or roles>
Time it takes: <minutes>
Before you start (you need): <access, tools>

## Steps
1. <one action>. You should see: <expected result>.
2. 
3. 

## If it did not work
- <what to try>
- Call: <name, how to reach>

## After you are done
- [ ] Tell: <who>
- [ ] Write it in the incident log
- [ ] Last tested by someone else on: YYYY-MM-DD
```

## 7.4 Postmortem Template (blameless)

```
# Postmortem: <title>
Date of incident: YYYY-MM-DD   Severity: SEV1 | SEV2
Written by: <name>   Reviewed by: <name>

## Summary (3 sentences)
## Impact: how many customers, how long, any money or data lost?
## Timeline (all times with time zone)
| Time | What happened |
|---|---|
## Why it happened (root causes, not people)
## What went well
## What went badly
## Actions
| Action | Owner | Due | Done? |
|---|---|---|---|
## Docs to update because of this (runbook? FAQ? AGENTS.md?)
```

## 7.5 Test Plan Template

```
# Test Plan: <area>
Goal: <what we want to prove>
Not testing: <what is out of scope>
Devices and versions: 
Test data: <where from; no real customer data>

| ID | Journey / case | Steps | Expected result | Result | Tester | Date |
|---|---|---|---|---|---|---|

Pass rule: <e.g. all S1 and S2 cases pass>
Bugs found: <links>
Sign-off (human): <name, date>
```

## 7.6 Release Notes Template

```
# Release vX.Y.Z – YYYY-MM-DD

## Summary (2 sentences, plain words for customers)
## New
- 
## Improved
- 
## Fixed
- 
## Known issues
- 
## For the team
- Upgrade steps: 
- Rollback steps: <link>
- Docs updated: <links>
```

## 7.7 Lessons-Learned Template

```
# Lessons Learned: <phase or event>   Date: YYYY-MM-DD

1. What did we plan?
2. What really happened?
3. What worked (keep doing)?
4. What did not work (stop or change)?
5. What surprised us?
6. What will we do differently next project?
7. Which template, checklist, or standard should change because of this?
   (Link the change in Part 10.)
```

## 7.8 Help Article Template

```
# How to <do one thing>
Applies to: web | iOS | Android   Last checked: YYYY-MM-DD
Time needed: 
1. <step with exact button names>
2. 
Still stuck? <how to contact us>
```

## 7.9 Support Playbook Entry Template

```
Problem customers report: 
How to confirm it: 
Fix (steps): 
When to escalate (and to whom): 
What to tell the customer (copy-ready message): 
Which doc to update if this keeps happening: 
```

---

# PART 8: FINAL MASTER CHECKLIST (LAUNCH → CUSTOMER #500)

Use this as the last check. Every row needs a name and date.

| # | Gate | Evidence (link) | Checked by | Date | OK? |
|---|---|---|---|---|---|
| 1 | Phase 0: Go decision written | | | | [ ] |
| 2 | Phase 1: PRD approved by a human | | | | [ ] |
| 3 | Phase 2: ADRs and architecture approved | | | | [ ] |
| 4 | Phase 3: README works for a stranger; `AGENTS.md` exists | | | | [ ] |
| 5 | Phase 4: Journeys pass; zero S1 bugs | | | | [ ] |
| 6 | Phase 5: Legal docs reviewed; restore tested; breach plan | | | | [ ] |
| 7 | Phase 6: Go / No-go signed; rollback ready | | | | [ ] |
| 8 | Phase 7: Runbooks, FAQ, support ready | | | | [ ] |
| 9 | Phase 8: Milestones #1, #10, #50, #100, #250 logged | | | | [ ] |
| 10 | Phase 8: Customer #500 review and decision | | | | [ ] |
| 11 | All docs in `INDEX.md` with owners | | | | [ ] |
| 12 | Lessons learned written and template updated | | | | [ ] |

**Final sign-off:**
Project owner: ________  Date: ________  Decision: [ ] Scale [ ] Fix [ ] Change direction [ ] Stop

---

# PART 9: GLOSSARY (PLAIN-ENGLISH WORDS)

| Word | What it means |
|---|---|
| **ADR** | Architecture Decision Record. A short note saying what we chose and why. |
| **Agent (AI agent)** | An AI that can do tasks by itself, like reading files and writing code. |
| **API** | A way for one program to talk to another. |
| **Archive** | Old documents kept for history. |
| **Backup** | A saved copy of your data, used if something breaks. |
| **Beta** | Early testing with a small group before public launch. |
| **Breach** | When private data is seen by someone who should not see it. |
| **Changelog** | A list of what changed in each version. |
| **CLAUDE.md / AGENTS.md** | Instruction files that tell AI agents how the project works. |
| **Docs-as-code** | Writing docs as text files saved with the code. |
| **Environment variable** | A named setting (like a secret key) kept outside the code. |
| **Evals** | Tests for AI answers. |
| **Feature freeze** | A date after which no new features are added before launch. |
| **Go / No-go** | A yes-or-no decision to continue or stop. |
| **Incident** | Something broke and affects customers. |
| **Milestone** | A checkpoint on the road (like 100 customers). |
| **Postmortem** | A blameless write-up after an incident. |
| **PRD** | Product Requirements Document. What we are building and why. |
| **Retention** | How many people keep using the product over time. |
| **Rollback** | Going back to the last working version. |
| **Runbook** | Step-by-step instructions to fix a known problem. |
| **SaaS** | Software you use online and usually pay for monthly. |
| **Semantic Versioning** | Numbering versions `MAJOR.MINOR.PATCH`. |
| **SEV (Severity)** | How serious a problem is. SEV1 is worst. |
| **Source of truth** | The one place where the real answer lives. |
| **Status label** | Draft, In Review, Approved, or Deprecated. |
| **WCAG** | Web Content Accessibility Guidelines. Rules to make products usable by everyone. |

**Q: Add project-specific words here (or in `glossary.md`).**
Your answer:

---

# PART 10: CHANGE LOG FOR THIS FILE

| Version | Date | What changed | Why | Changed by | Approved by (human) |
|---|---|---|---|---|---|
| 0.1 | YYYY-MM-DD | First copy from template v1.1 | New project | | |

> **Reminder before you finish:** Set the Status in Part 0.1 to `IN REVIEW`. A human reads it. Only then does it become `APPROVED`.

---

# APPENDIX A: A FULLY FILLED EXAMPLE (PLANTPAL)

> **This is a pretend project.** Read it to see what "done" looks like. Delete this appendix from your copy when you are finished.

## A.1 Part 0 filled

| Field | Answer |
|---|---|
| Title | Documentation Standards for **PlantPal** |
| Owner / Backup | Maya Lopez / Sam Okafor |
| Status | `IN REVIEW` |
| Project code | `plantpal` |
| One sentence | PlantPal reminds people when to water their plants. |
| Who it is for | Busy city workers who keep killing their houseplants |
| Product kind | [x] Web app [x] Mobile iOS [x] Mobile Android [x] Has AI features [ ] API |
| Humans | Maya (Owner/Builder), Sam (Tester/Support) |
| AI agents | [x] Claude Code |
| Dates | Start 2026-11-02 · Build done 2027-02-15 · Beta 2027-03-01 · Launch 2027-04-05 · Customer #500 target 2027-09-30 |
| "We won" sentence | 500 people have signed up, and at least 40% still use PlantPal every week. |

## A.2 Phase 0 filled (shortened)

- **Problem:** "I forget to water my plants, so they die."
- **Today's solutions:** Phone alarms, sticky notes, giving up.
- **Interviews:** 9 people. 6 said they would pay about USD 3 per month.
- **Competitors:** Plant app A (USD 6.99, too complex), Plant app B (free, full of ads), phone reminders (free, no plant info).
- **Top assumptions:** (1) People will add plants by taking a photo → test with 10 people; (2) A reminder is worth USD 3 per month → test with a pre-order page.
- **Risks:** [x] Nobody wants it [x] AI plant recognition may be wrong [x] App store may reject it.
- **Decision:** GO. Decided by Maya on 2026-11-09. Written in `adr-0001-go-no-go.md`.

## A.3 Phase 1 filled (shortened)

| ID | Story | Priority |
|---|---|---|
| US-01 | As a busy worker, I want a phone reminder, so that I never forget to water. | Must |
| US-02 | As a new plant owner, I want to photo my plant and learn its needs, so that I do not guess. | Should |
| US-03 | As a traveller, I want to pause reminders, so that I am not nagged on holiday. | Could |

| In (first release) | Out (not yet) |
|---|---|
| Account, add plant, reminders, pause | Plant social feed, shop, smart sensors |

| Metric | Start | Target by customer #500 |
|---|---|---|
| Sign-ups | 0 | 500 |
| Activation (add 1 plant in 24 h) | n/a | 70% |
| Weekly active | n/a | 40% |
| Day-30 retention | n/a | 35% |
| Paying customers | 0 | 100 |

Pricing: Free trial 14 days, then **USD 3.00 per month**. Refund: full refund within 14 days.

## A.4 Phase 2 filled (shortened)

| Part | Choice | Why | ADR |
|---|---|---|---|
| Front end | React web + React Native mobile | One team can build both | adr-0002 |
| Back end | Node API | Maya knows it | adr-0003 |
| Database | PostgreSQL | Safe, widely known | adr-0004 |
| Payments | Stripe + store purchases | Handles cards for us | adr-0005 |
| AI | Image-recognition model via provider | Faster than building our own | adr-0006 |
| Hosting | Managed cloud host | Backups included | adr-0007 |

Monthly cost: launch **USD 85**; at 500 customers **USD 310** (AI usage is the biggest part).

## A.5 Phase 3 to 8: one example answer each

- **Phase 3:** README steps: 1) `git clone` 2) `npm install` 3) copy `.env.example` to `.env` 4) `npm run dev`. Setup tested by Sam on a clean laptop: 22 minutes.
- **Phase 4:** Top-10 journeys: 10 of 10 passed on 2027-02-25. Open S1 bugs: 0. Open S2 bugs: 1 (signed off by Maya, fix in v1.0.1).
- **Phase 5:** Privacy policy reviewed by a lawyer on 2027-03-08. Backup restore tested on 2027-03-10 (took 18 minutes).
- **Phase 6:** Soft launch to the 120-person waiting list on 2027-04-05. Rollback = re-deploy previous build, takes 10 minutes, only Maya may press the button. iOS review took 2 days; first rejection was for a missing reviewer test login, which was added to `store-submission.md`.
- **Phase 7:** Top question #1: "Why did I not get my reminder?" → Help article `help-missing-reminders.md` (check notification permission, battery saver, time zone). SEV1 reply target: 15 minutes.
- **Phase 8:** Customer #100 reached 2027-06-14. Restore test re-run: pass. Lesson: "AI cost per photo was 4 times higher than planned → added daily spend cap of USD 10."

## A.6 AI rules filled (from Part 3.7)

| Question | Answer |
|---|---|
| The AI's one job | Name a plant from a photo and suggest watering needs |
| Must never | Give advice about eating plants or toxic exposure as medical advice; share any customer's photo |
| When it does not know | Says "I am not sure" and shows 3 possible plants for the customer to pick |
| Tells people it is AI? | Yes, a label next to every result |
| Can it take actions? | No |
| Spend limit | USD 0.05 per customer per month; USD 10 per day hard stop |

## A.7 Business tracks filled (one line each)

- **Track A:** First 500 customers: 120 waiting list, 100 social posts and plant communities, 80 app store search, 100 referrals, 100 content and search.
- **Track B:** Money available USD 18,000. Monthly spend USD 1,400. Runway about 12.8 months. Break-even is about 470 paying customers (USD 1,400 ÷ USD 3.00), so 100 paying customers at customer #500 does **not** cover costs yet. This is the number the founder must act on.
- **Track C:** Two people. One contractor hired for design (Track C.2), agreement reviewed by a lawyer.

---

*End of Documentation_Standards.md (template v1.1)*
