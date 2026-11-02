# How to Fill This Document

> **Location:** Documentation Management and Institutional Knowledge / Architecture_Decision_Records.md
> **Template version:** 1.0 | **Covers:** first idea → build → test and security → launch → first 500 customers
> **Who can fill it:** a person (even a beginner) or an AI agent. Both follow the same rules.

---

## 0. The 60-second explanation

An **Architecture Decision Record (ADR)** is a short note that answers three things about one important choice:

1. **What did we choose?**
2. **Why did we choose it?**
3. **What happens because of it?**

Think of it as a diary entry for a big decision. Six months from now, nobody remembers why you picked a database. The ADR remembers for you.

**One ADR = one decision.** Never mix two decisions in one ADR.

---

## 1. Seven golden rules (read these first)

| # | Rule | Why |
|---|------|-----|
| 1 | **Never guess.** If you do not know something, write `UNKNOWN` and add who can find out. | A guess looks like a fact later. |
| 2 | **Answer every question.** Use `N/A - reason` if it truly does not apply. | Blank spaces hide missing thinking. |
| 3 | **Use plain words.** Say "database" not "persistence layer". If you must use a hard word, add it to the Glossary (Part 7). | Anyone should be able to read it. |
| 4 | **Write numbers, not feelings.** Write "costs about $40 per month", not "cheap". | Numbers can be checked. |
| 5 | **Never edit an accepted ADR's decision.** Write a new ADR that replaces it. | The history stays honest. |
| 6 | **Never put secrets in this file.** No passwords, keys, tokens or customer data. Write where they are stored instead. | This file gets shared widely. |
| 7 | **Write the ADR when you decide, not later.** | Memory fades fast. |

---

## 2. When do I need to write an ADR?

Write an ADR if you can answer **YES** to any of these:

- [ ] Would it be **hard or expensive to undo** this choice later?
- [ ] Will it **affect more than one person, team, or feature**?
- [ ] Will someone **new ask "why did we do it this way?"** in the future?
- [ ] Does it involve **customer data, money, security, or the law**?
- [ ] Does it involve an **AI model, AI agent, or prompt** that the product depends on?

**Do NOT write an ADR for:** colour choices, variable names, small bug fixes, or anything you can change in under one day with no side effects.

### Examples of decisions that deserve an ADR

| Group | Examples |
|-------|----------|
| **Tech and architecture** | Programming language, framework, database, hosting provider, how parts talk to each other, third-party services |
| **AI choices** | Which AI model or coding agent we use, what data we send to it, how we write and store prompts, fallback if the AI provider goes down |
| **Security and privacy** | Login method, where customer data is stored, encryption, privacy law compliance, backup rules |
| **Business-impacting** | Payment provider, analytics tool, customer support tool, email provider, vendors that are expensive to switch away from |

---

## 3. How to fill this document: 6 simple steps

**Step 1: Fill Part 1 (Project Passport) once per project.** It takes 10 minutes.

**Step 2: When a big decision comes up, copy the blank template in Part 3.** Paste it at the bottom of Part 4 (the ADR Log).

**Step 3: Give it a number and a phase tag.**
- Number: next free number, 4 digits, never reused. Example: `ADR-0007`.
- Phase tag: pick ONE:

| Tag | Use for decisions made during |
|-----|-------------------------------|
| `BUILD` | Idea, design, and development |
| `TEST` | Testing, quality, and security |
| `LAUNCH` | Getting the product live |
| `GROW` | Launch day up to the first 500 customers |

**Step 4: Answer every question in the template.** Each question has a hint and an example. Replace the grey instruction text and the `[brackets]` with your answers. Keep answers short: 1 to 3 sentences each unless a table is shown.

**Step 5: Ask someone else to review it.** The Owner writes it. A Reviewer checks it. Use the checklist in Part 6 before you ask.

**Step 6: Add one row to the Decision Index (Part 2).** If you skip this, nobody will find your ADR.

### Status labels (pick exactly one)

| Status | Meaning |
|--------|---------|
| `Proposed` | Written, waiting for review. Not final. |
| `Accepted` | Approved. This is the rule everyone follows now. |
| `Rejected` | We looked at it and said no. Keep it so nobody proposes it again without new reasons. |
| `On Hold` | Paused. Write what must happen before it continues. |
| `Deprecated` | Still in use but we plan to stop using it. |
| `Superseded` | Replaced by a newer ADR. Write the new ADR's number. |

**Allowed movement:** `Proposed` → `Accepted` or `Rejected` or `On Hold`. `Accepted` → `Deprecated` or `Superseded`. Nothing goes backwards to `Proposed`; write a new ADR instead.

### Review triggers (very important for reaching 500 customers)

Every ADR must say **when to look at it again**. Pick one or more:

| Trigger type | Example |
|--------------|---------|
| Customer count | "Re-check at 50, 100, 250, and 500 customers" |
| Date | "Re-check on 2027-03-01" |
| Cost | "Re-check if monthly cost goes above $300" |
| Problem | "Re-check if we have 2 outages in one month" |
| Change | "Re-check if the AI provider changes its prices or terms" |

### Extra rules when an AI agent fills this document

- The AI **may draft** an ADR but a **human must approve** it before the status becomes `Accepted`.
- The AI must **never invent** facts, prices, limits, or dates. If it did not read it in a source, it writes `UNKNOWN`.
- The AI must **list its sources** (links or file names) in the "Evidence" question.
- The AI must **keep the key-value block** (the lines in the `ADR Header`) exactly in the given format so tools can read it.
- The AI must **never edit** an ADR with status `Accepted`, except to change its status to `Deprecated` or `Superseded` and add a link.
- When unsure, the AI **asks the human a question** instead of choosing.

---

# Part 1: Project Passport (fill once per project)

> **Hint:** This tells readers what the project is. Fill it before writing any ADR.

| Question | Your answer |
|----------|-------------|
| **Project name?** (example: "PetPal App") | [ ] |
| **Project ID or code?** (example: `PP-2026`) | [ ] |
| **One sentence: what does this product do, and for whom?** | [ ] |
| **Who is the Project Owner?** (name and role) | [ ] |
| **Who is the Technical Lead?** | [ ] |
| **Today's date and template version used** | [ ] |
| **Where is the code stored?** (link) | [ ] |
| **Where do other project documents live?** (link) | [ ] |
| **Current life-cycle phase?** (`BUILD`, `TEST`, `LAUNCH`, `GROW`) | [ ] |
| **Current customer count?** (write `0` before launch) | [ ] |
| **Target launch date?** | [ ] |
| **Target date to reach 500 customers?** | [ ] |
| **Does the product use AI inside it?** (Yes / No) | [ ] |
| **Do we use AI tools to build it?** (Yes / No, which ones) | [ ] |
| **What kind of customer data do we hold?** (none / email only / payment / health / other) | [ ] |
| **Which laws or rules apply?** (example: GDPR, none known, UNKNOWN) | [ ] |
| **Monthly budget limit for tools and hosting?** | [ ] |

---

# Part 2: Decision Index (one row per ADR)

> **Hint:** This is the table of contents. Add a row every time you add an ADR. Keep newest at the bottom.

| ADR No. | Phase | Title (max 10 words) | Status | Owner | Date decided | Review trigger | Replaced by |
|---------|-------|----------------------|--------|-------|--------------|----------------|-------------|
| ADR-0001 | BUILD | Example: Choose database for customer data | Accepted | Sam | 2026-10-19 | At 100 and 500 customers | none |
| | | | | | | | |

---

# Part 3: Blank ADR Template (copy everything between the lines)

> **How to use:** Copy from `START OF TEMPLATE` to `END OF TEMPLATE`. Paste it into Part 4. Replace every `[ ]` and every instruction line. Delete the instruction lines when done (the `> Hint` lines are optional to keep).

````markdown
<!-- START OF TEMPLATE -->

## ADR-0000: [Short title: verb + thing, max 10 words]

### ADR Header (do not change the format)

```
adr_id: ADR-0000
title: [same as above]
phase: [BUILD | TEST | LAUNCH | GROW]
status: [Proposed | Accepted | Rejected | On Hold | Deprecated | Superseded]
owner: [name and role]
reviewers: [names]
final_approver: [name]
date_proposed: [YYYY-MM-DD]
date_decided: [YYYY-MM-DD or UNKNOWN]
review_trigger: [see "Review triggers" in the instructions]
supersedes: [ADR number or none]
superseded_by: [ADR number or none]
related_adrs: [ADR numbers or none]
involves_ai: [Yes | No]
reversibility: [Easy | Medium | Hard]
```

---

### A. The Problem (Context)

**A1. What problem are we solving, in plain words?**
> Hint: Write as if explaining to a friend. 2 to 4 sentences.
> Example: "Customers need to log in. We must store their emails safely."

[ ]

**A2. Why do we have to decide this NOW?**
> Hint: What breaks or gets harder if we wait?

[ ]

**A3. What are the must-haves (rules we cannot break)?**
> Hint: Money limits, laws, deadlines, skills we have, tools we already use.

| # | Must-have | Source (who or what says so) |
|---|-----------|------------------------------|
| 1 | [ ] | [ ] |
| 2 | [ ] | [ ] |

**A4. What matters most when choosing? (rank the top 3 to 5)**
> Hint: Pick from: cost, speed to launch, safety, ease of use, ability to grow, ease of changing later, team skill. Rank 1 = most important.

| Rank | What matters | Why it matters for us |
|------|--------------|-----------------------|
| 1 | [ ] | [ ] |
| 2 | [ ] | [ ] |
| 3 | [ ] | [ ] |

**A5. Which customer stage is this decision built for?**
> Hint: Pick one and say why. Example: "Good enough for 0 to 100 customers; revisit after."

[ ] Before launch  [ ] 0 to 50 customers  [ ] 50 to 250 customers  [ ] 250 to 500 customers  [ ] Beyond 500

**A6. What do we NOT know yet?**
> Hint: Honest gaps. Write `UNKNOWN` and who will find out by when.

[ ]

---

### B. The Choices (Options Considered)

> Hint: List **at least 2** real options. "Do nothing" counts as an option.

| Option | What it is (one sentence) | Good things | Bad things | Cost (one-time and monthly) | Effort (days) |
|--------|---------------------------|-------------|------------|-----------------------------|---------------|
| **Option 1:** [name] | [ ] | [ ] | [ ] | [ ] | [ ] |
| **Option 2:** [name] | [ ] | [ ] | [ ] | [ ] | [ ] |
| **Option 3:** Do nothing | Keep things as they are | [ ] | [ ] | [ ] | 0 |

**B1. Which options did we throw out early, and why?**

[ ]

**B2. What evidence did we use?** (links, tests, price pages, documents, quotes, trial results)
> Hint: Every number above should have a source here. AI agents: list every source you read.

| # | Source (link or file name) | What it told us | Date checked |
|---|----------------------------|-----------------|--------------|
| 1 | [ ] | [ ] | [ ] |

---

### C. The Decision

**C1. Our decision in ONE sentence.**
> Hint: Use this pattern: "We will use **[choice]** for **[purpose]**, because **[main reason]**, accepting that **[main downside]**."

[ ]

**C2. Why this option beat the others?**
> Hint: Link back to the rankings in A4. 2 to 5 sentences.

[ ]

**C3. Who made the final call, and when?**

[ ]

**C4. Who disagreed, and what was their concern?**
> Hint: Write `No disagreement` if true. Do not hide disagreement. It helps future readers.

[ ]

---

### D. What Happens Next (Consequences)

**D1. Good results we expect.**

[ ]

**D2. Bad results or new problems we accept.**

[ ]

**D3. Risks.**

| Risk | How likely (Low / Med / High) | How bad (Low / Med / High) | What we do about it |
|------|-------------------------------|----------------------------|---------------------|
| [ ] | [ ] | [ ] | [ ] |

**D4. How hard is it to undo this decision?**
> Hint: Easy = under 1 day. Medium = 1 to 10 days. Hard = more than 10 days or costs real money.

[ ] Easy  [ ] Medium  [ ] Hard   **What would undoing involve?** [ ]

**D5. What must we do to make this decision real? (action list)**

| # | Action | Owner | Due date | Done? |
|---|--------|-------|----------|-------|
| 1 | [ ] | [ ] | [ ] | [ ] |

**D6. How will we know it was a good decision? (success measures)**
> Hint: Use numbers. Example: "Login works for 99.9% of attempts" or "Costs under $50 per month at 500 customers".

| Measure | Target | How we measure | When we check |
|---------|--------|----------------|---------------|
| [ ] | [ ] | [ ] | [ ] |

**D7. When do we look at this decision again?**
> Hint: Copy your `review_trigger` from the header and explain it. Include at least one customer-count trigger for GROW decisions.

[ ]

---

### E. Safety, Privacy and Law

> Hint: Answer even if the decision seems unrelated. Write `N/A - reason` if not relevant.

**E1. Does this touch customer data?** (Yes / No)  If yes, what kind and where does it live?

[ ]

**E2. Does this affect login, payments, or access rights?**

[ ]

**E3. Which laws or rules could apply?** (example: GDPR, CCPA, payment card rules, accessibility rules, app store rules)

[ ]

**E4. What is the worst thing that could go wrong, and how do we recover?**

[ ]

**E5. Where are backups, and who can restore them?**

[ ]

---

### F. Running It (Launch and Operations)

> Hint: Fill this mainly for `LAUNCH` and `GROW` decisions. For `BUILD` and `TEST` decisions, answer briefly or write `N/A - reason`.

**F1. How do we put this into the live product?** (steps or link)

[ ]

**F2. How do we go back if it goes wrong? (rollback plan)**

[ ]

**F3. How will we notice if it breaks?** (alerts, checks, who gets told)

[ ]

**F4. Who gets called when it breaks, and what is the backup plan?**

[ ]

**F5. What does it cost to run at each stage?**

| Stage | Expected monthly cost | Where the number comes from |
|-------|-----------------------|-----------------------------|
| Launch day | [ ] | [ ] |
| 50 customers | [ ] | [ ] |
| 100 customers | [ ] | [ ] |
| 500 customers | [ ] | [ ] |

**F6. What will customers or support staff notice?** (new screens, new rules, downtime, new help articles needed)

[ ]

---

### G. AI Section (fill only if `involves_ai: Yes`; otherwise write "N/A - no AI involved")

**G1. Model and tool choice**

| Question | Answer |
|----------|--------|
| Which AI model, agent, or tool? (exact name and version) | [ ] |
| What job does it do? (write code, answer customers, summarize, other) | [ ] |
| Is it used **to build** the product, **inside** the product, or both? | [ ] |
| Why this one and not the others? | [ ] |
| Who supplies it (company) and where do their terms and prices live? (link) | [ ] |
| What happens to our data when we send it? (stored? used for training?) | [ ] |
| What do we do if the provider stops working or changes the rules? (backup model or manual process) | [ ] |

**G2. Prompts and guardrails**

| Question | Answer |
|----------|--------|
| Where are the prompts or instructions stored? (file path or link) | [ ] |
| Who may change them, and how is a change approved? | [ ] |
| What must the AI **always** do? | [ ] |
| What must the AI **never** do? (example: never see customer passwords, never delete data, never publish without approval) | [ ] |
| Which steps need a **human to approve** before they happen? | [ ] |
| What data is the AI allowed to see? What is it NOT allowed to see? | [ ] |
| What should the AI say or do when it is unsure? | [ ] |

**G3. Cost and limits**

| Question | Answer |
|----------|--------|
| Price per use (per token, per request, per seat) and where we got it | [ ] |
| Expected monthly AI cost at 50 / 100 / 500 customers | [ ] |
| Usage limits (requests per minute, daily caps) | [ ] |
| What is our monthly AI spending limit, and what happens when we reach it? | [ ] |
| Who watches the bill, and how often? | [ ] |

**G4. Quality checks**

| Question | Answer |
|----------|--------|
| How do we check AI-written code before it is used? (human review, automatic tests, both) | [ ] |
| How do we check AI answers inside the product? (sample reviews, test questions, customer reports) | [ ] |
| How do we measure AI quality? (example: "9 out of 10 test questions answered correctly") | [ ] |
| What do we do when the AI gives a wrong or harmful answer? | [ ] |
| How do we spot "made-up" facts (hallucinations) before customers do? | [ ] |
| How often do we re-test when the AI provider updates the model? | [ ] |

---

### H. Sign-off and History

| Role | Name | Decision (Approve / Reject / Needs changes) | Date |
|------|------|---------------------------------------------|------|
| Owner | [ ] | [ ] | [ ] |
| Reviewer 1 | [ ] | [ ] | [ ] |
| Reviewer 2 (optional) | [ ] | [ ] | [ ] |
| Final approver | [ ] | [ ] | [ ] |

**Change history of this ADR** (status changes and small fixes only; never change the decision itself)

| Date | Who | What changed |
|------|-----|--------------|
| [ ] | [ ] | Created as `Proposed` |

**Links:** Related ADRs [ ] | Tickets or tasks [ ] | Design files [ ] | Test reports [ ] | Meeting notes [ ]

<!-- END OF TEMPLATE -->
````

---

# Part 4: ADR Log (paste finished ADRs below, oldest first)

> **Hint:** Everything below this line is real decisions for this project. The example in Part 5 is NOT part of the log.

<!-- ADR LOG STARTS HERE -->

*(No decisions recorded yet.)*

<!-- ADR LOG ENDS HERE -->

---

# Part 5: Filled Example (copy the style, not the content)

> This is a made-up project called "PetPal". It shows how short, clear answers look.

## ADR-0001: Use a managed database for customer accounts

### ADR Header

```
adr_id: ADR-0001
title: Use a managed database for customer accounts
phase: BUILD
status: Accepted
owner: Sam Lee, Technical Lead
reviewers: Priya Rao, Jo Kim
final_approver: Maria Gomez, Project Owner
date_proposed: 2026-10-12
date_decided: 2026-10-19
review_trigger: At 100 and 500 customers; if monthly cost exceeds $100
supersedes: none
superseded_by: none
related_adrs: none
involves_ai: No
reversibility: Medium
```

### A. The Problem

**A1.** PetPal customers create accounts with an email and pet details. We need a safe place to store this information.

**A2.** Developers start building account screens next week and need to know where data goes.

**A3. Must-haves**

| # | Must-have | Source |
|---|-----------|--------|
| 1 | Total tools and hosting under $150 per month | Project budget, Part 1 |
| 2 | Automatic daily backups | Owner request |
| 3 | Team already knows SQL | Skills list |

**A4. What matters most**

| Rank | What matters | Why |
|------|--------------|-----|
| 1 | Safety of customer data | We hold emails |
| 2 | Low cost | Small budget |
| 3 | Easy for the team to run | Only 2 developers |

**A5.** Good enough for 0 to 500 customers.

**A6.** UNKNOWN: exact pricing above 500 customers. Sam will check the price page by 2026-11-01.

### B. The Choices

| Option | What it is | Good | Bad | Cost | Effort |
|--------|-----------|------|-----|------|--------|
| **Option 1:** Managed SQL database | A hosted database a provider looks after | Backups included, low upkeep | Provider lock-in | About $25 per month | 2 days |
| **Option 2:** Run our own database on a rented server | We install and manage it | Full control | We must fix it ourselves; backups are our job | About $15 per month plus our time | 6 days |
| **Option 3:** Do nothing (spreadsheets) | Store accounts in files | Free | Not safe, not searchable | $0 | 0 |

**B1.** Option 3 was thrown out: it fails the safety must-have.

**B2. Evidence**

| # | Source | What it told us | Date |
|---|--------|-----------------|------|
| 1 | Provider price page (link) | $25 per month for our size | 2026-10-10 |
| 2 | 1-day trial by Jo | Setup took 3 hours | 2026-10-11 |

### C. The Decision

**C1.** We will use a **managed SQL database** for **customer accounts**, because **it keeps data safe with backups and little upkeep**, accepting that **we depend on one provider**.

**C2.** It wins on the top two priorities (safety, cost) and is easy for two developers to run.

**C3.** Maria Gomez, 2026-10-19.

**C4.** Priya preferred running our own for control. She accepted the decision once the backup plan was clear.

### D. What Happens Next

**D1.** Backups happen automatically. Developers spend time on features, not servers.

**D2.** Monthly fee. Moving to another provider later takes about 5 to 10 days.

**D3. Risks**

| Risk | Likelihood | Impact | What we do |
|------|-----------|--------|------------|
| Provider has a long outage | Low | High | Keep weekly exported backup in separate storage |
| Price rises | Medium | Medium | Review at 100 customers |

**D4.** Medium. Undoing means exporting data and re-importing it elsewhere (about 5 to 10 days).

**D5. Actions**

| # | Action | Owner | Due | Done? |
|---|--------|-------|-----|-------|
| 1 | Create the database account | Sam | 2026-10-21 | No |
| 2 | Set up weekly export backup | Jo | 2026-10-28 | No |

**D6. Success measures**

| Measure | Target | How measured | When |
|---------|--------|--------------|------|
| Monthly cost | Under $100 at 500 customers | Provider bill | Monthly |
| Backup restore test | Works in under 1 hour | Test restore | Every 3 months |

**D7.** Review at 100 and 500 customers, or if monthly cost passes $100.

### E. Safety, Privacy and Law

**E1.** Yes. Emails and pet names. Stored in the managed database, encrypted at rest.
**E2.** Yes, login uses this database. See ADR-0002 (planned).
**E3.** GDPR may apply to European customers. UNKNOWN; Maria will ask a lawyer by 2026-11-15.
**E4.** Data loss. Recover from the daily backup or weekly export.
**E5.** Daily by the provider; weekly export in a separate storage. Sam and Jo can restore.

### F. Running It

**F1.** N/A for now: build phase. Launch steps will be added in a later ADR.
**F2.** N/A - build phase.
**F3.** N/A - build phase.
**F4.** N/A - build phase.

**F5. Cost per stage**

| Stage | Monthly cost | Source |
|-------|--------------|--------|
| Launch day | $25 | Price page |
| 50 customers | $25 | Price page |
| 100 customers | $25 | Price page |
| 500 customers | UNKNOWN | Sam will check by 2026-11-01 |

**F6.** Nothing visible to customers.

### G. AI Section

N/A - no AI involved.

### H. Sign-off and History

| Role | Name | Decision | Date |
|------|------|----------|------|
| Owner | Sam Lee | Approve | 2026-10-12 |
| Reviewer 1 | Priya Rao | Approve | 2026-10-16 |
| Reviewer 2 | Jo Kim | Approve | 2026-10-16 |
| Final approver | Maria Gomez | Approve | 2026-10-19 |

| Date | Who | What changed |
|------|-----|--------------|
| 2026-10-12 | Sam | Created as `Proposed` |
| 2026-10-19 | Maria | Status changed to `Accepted` |

---

# Part 6: Quality Checklist (tick every box before asking for review)

### Completeness
- [ ] The ADR has a unique number and a phase tag (`BUILD`, `TEST`, `LAUNCH`, or `GROW`).
- [ ] The Header block is filled and in the exact format.
- [ ] Every question in sections A to H has an answer, `UNKNOWN` plus an owner and date, or `N/A - reason`.
- [ ] Only **one** decision is described.
- [ ] At least **two real options** are listed (and "do nothing" is considered).

### Clarity
- [ ] The decision fits in **one sentence** (question C1).
- [ ] A 10-year-old could understand A1 and C1.
- [ ] Every hard word is explained or added to the Glossary.
- [ ] Numbers have units and a source (dollars, days, customers).

### Honesty
- [ ] Nothing is guessed. Gaps say `UNKNOWN`.
- [ ] Bad results (D2) and risks (D3) are written down, not hidden.
- [ ] Disagreement (C4) is recorded.
- [ ] Every source is listed in B2 with a date.

### Safety
- [ ] No passwords, keys, tokens, or real customer data appear anywhere.
- [ ] Section E is answered.
- [ ] A way back (rollback) or an undo plan exists (D4 and F2).

### Follow-through
- [ ] Actions have owners and dates (D5).
- [ ] Success measures have targets (D6).
- [ ] A review trigger is set, with a customer-count trigger if phase is `GROW` (D7).
- [ ] A row was added to the Decision Index in Part 2.
- [ ] Related ADRs are linked in both directions.

### AI-specific (only if `involves_ai: Yes`)
- [ ] Exact model name and version are written.
- [ ] Things the AI must never do are written.
- [ ] A human approves the risky steps.
- [ ] Monthly AI cost and a spending limit are written.
- [ ] A backup plan exists if the AI provider fails.
- [ ] A way to check AI quality is written.

**If any box is unticked, the ADR is not ready. Fix it first.**

---

# Part 7: Glossary (plain-English words)

| Word | Simple meaning |
|------|----------------|
| **ADR** | A short note recording one big decision, why it was made, and what follows. |
| **Architecture** | The big-picture plan of how the parts of a product fit and talk to each other. |
| **Context** | The situation and problem that led to the decision. |
| **Consequence** | What happens because of the decision, good or bad. |
| **Stakeholder** | Anyone affected by the decision or who has a say in it. |
| **Owner** | The person who writes the ADR and makes sure its actions happen. |
| **Reviewer** | A person who reads the ADR and checks it for mistakes and gaps. |
| **Final approver** | The person with the power to say "yes, this is now the rule". |
| **Phase** | The stage of the product's life: build, test, launch, or grow. |
| **Review trigger** | The event or date that tells us to look at a decision again. |
| **Reversibility** | How hard it is to undo a decision. |
| **Supersede** | To replace an old decision with a new one. |
| **Deprecated** | Still used for now, but planned to be retired. |
| **Rollback** | Going back to the way things were before a change. |
| **Backup** | A safe copy of data you can restore if the original is lost. |
| **Hosting** | The computers (usually rented) where your product runs. |
| **Database** | A organized place where a product stores information such as customer accounts. |
| **API** | A doorway that lets one piece of software ask another for something. |
| **Third-party service** | A tool or company outside your team that your product relies on. |
| **Vendor lock-in** | Being stuck with one provider because switching is costly or hard. |
| **Encryption** | Scrambling data so only people with the key can read it. |
| **Compliance** | Following the laws and rules that apply to your product. |
| **GDPR** | A European privacy law about how personal data must be handled. |
| **Monitoring and alerts** | Tools that watch the product and warn people when something breaks. |
| **Outage** | A time when the product does not work for customers. |
| **QA (Quality Assurance)** | Checking that the product works properly before and after release. |
| **AI model** | The "brain" of an AI tool, made by a company such as Anthropic or others. |
| **AI agent** | An AI that can take multiple steps or actions on its own to finish a task. |
| **Prompt** | The instructions or question you give to an AI. |
| **Guardrails** | Rules that keep an AI from doing unsafe or unwanted things. |
| **Token** | A small piece of text an AI reads or writes; usage is often priced per token. |
| **Rate limit** | A cap on how many requests you may send to a service in a set time. |
| **Hallucination** | When an AI states something made-up as if it were true. |
| **Human in the loop** | A person must check or approve before an AI action goes ahead. |
| **Fallback** | The backup plan used when the main tool fails. |
| **UNKNOWN** | The honest answer when you do not know yet. Add who will find out and by when. |
| **N/A** | "Not applicable": the question does not apply. Always add the reason. |

---

# Part 8: Quick-Start Prompts for Common Decisions (optional idea list)

> **Hint:** Not sure what needs an ADR? Use this list as a starting point. Tick the ones you have already recorded.

### `BUILD` phase
- [ ] Programming language and framework
- [ ] Database and where it is hosted
- [ ] How parts of the product talk to each other
- [ ] Login and account method
- [ ] Which AI coding tools or agents are allowed, and what they may touch
- [ ] How code is stored, reviewed, and merged

### `TEST` phase
- [ ] How and how often we test (automatic tests, manual checks)
- [ ] How AI-written code is reviewed
- [ ] Security checks before launch
- [ ] Privacy and legal review
- [ ] Performance targets (how fast it must be, how many people at once)

### `LAUNCH` phase
- [ ] Hosting, domain, and release method
- [ ] Monitoring, alerts, and who is on call
- [ ] Rollback and backup plan
- [ ] Payment provider (if charging customers)
- [ ] Customer support tool and process
- [ ] Analytics tool and what we measure

### `GROW` phase (launch to 500 customers)
- [ ] When and how to scale (move to bigger hosting)
- [ ] Cost controls for hosting and AI
- [ ] How feedback from the first customers is collected and used
- [ ] Changing or replacing a tool that no longer fits
- [ ] Support workload and automation (including AI support)
- [ ] Re-checking earlier ADRs at 50, 100, 250, and 500 customers

---

# Part 9: Document History (for this template itself)

| Version | Date | Who | What changed |
|---------|------|-----|--------------|
| 1.0 | 2026-10-19 | [ ] | First version of the template |

