# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

> **Delete this whole "How to fill out" section once you understand it, or keep it. Either is fine.**

## What is this document?

This document answers one big question for ONE product:

> **"Who is in charge of what, at every step, from the first idea until the first 500 customers are using the product?"**

It is called **Lifecycle Ownership** because a product has a "life" (idea, build, launch, growth). Every step of that life needs **one clear owner**. Nobody should have to guess.

Copy this file once for **each new project**. Name your copy like this:
`Lifecycle_Ownership_[ProjectName].md`  (example: `Lifecycle_Ownership_PlantPal.md`)

## The 7 simple rules

1. **Answer every question in your own simple words.** Short is fine. "I don't know yet" is a valid answer, but you must then write WHO will find out and BY WHEN.
2. **Find the `[[PLACEHOLDER]]` marks and replace them.** A placeholder looks like `[[YOUR ANSWER HERE]]`. When you are finished, search the file for `[[`. If you still find any, you are not finished.
3. **Every step has exactly ONE owner.** One name (a person), not "the team" and not "we". Helpers are allowed, but only ONE person is accountable.
4. **Look at the Example, then write your own.** Every question shows an example. Never copy the example. It only shows the style.
5. **Tick the checkboxes honestly.** Change `- [ ]` into `- [x]` only when it is really true. A step is only finished when ALL its "Done when" boxes are ticked.
6. **Never write secrets in this file.** No passwords, API keys, card numbers, or private tokens. Write WHERE they are kept (example: "in my password manager, entry called PlantPal-Prod"), never the secret itself.
7. **Update the file when things change**, and add a line to the Version History table (Part 0).

## Marks used in this document

| Mark | Meaning |
|---|---|
| **[REQUIRED]** | You must answer this. |
| **[OPTIONAL]** | Skip it if it does not apply. Write `N/A - because [reason]`. |
| **[WEB]** | Only for web apps / SaaS products. |
| **[MOBILE]** | Only for iOS / Android apps. |
| `[[ ... ]]` | A blank you need to fill in. |
| `- [ ]` / `- [x]` | A checkbox: empty = not done, ticked = done. |
| 🧑 HUMAN DECISION | Only a human may decide this. AI must not decide alone. |
| 🤝 AI ASSIST | AI makes a draft or suggestion; a human checks and approves it. |
| 🤖 AI AUTOMATE | AI does a safe, repeatable task alone; a human spot-checks the results. |

## How the document is organized

| Part | What it is for | Fill it when |
|---|---|---|
| 0 | Project card and version history | Day 1 |
| 1 | Project basics (what are we building and for whom?) | Day 1 |
| 2 | People and owners (who is in charge of each stage?) | Day 1 |
| 3 | AI Agent Workflow (how AI helps, and the rules it follows) | Before building starts |
| 4 | The 14 lifecycle stages (the main part) | Fill each stage as you reach it. Skim all of them on Day 1. |
| 5 | The 500-customer plan | Before launch, update weekly after launch |
| 6 | Risk register | Day 1, then update at every stage |
| 7 | Decision log | Every time you make an important choice |
| 8 | Handover and continuity | Before launch, update at Stage 14 |
| 9 | Document map (links to other files) | Keep updated all along |
| 10 | Lessons learned | At the end (and a little after every stage) |
| 11 | Final sign-off | At the end |
| Appendix | Glossary, example, common mistakes | Look up when stuck |

## How to know the document is "good enough"

Hand it to someone who has never seen your project. If they can answer all five questions below using ONLY this file, you did a great job:

1. What are we building, and for whom?
2. Who owns each stage right now?
3. What must be true before we can move to the next stage?
4. What can AI do alone, and what needs a human?
5. How will we know we reached 500 customers, and who counts as a customer?

## Quick-start for the very impatient (15 minutes)

1. Fill **Part 0** and **Part 1** (10 minutes).
2. Fill the **owner table in Part 2** (5 minutes).
3. Read the stage list in **Part 4**, then fill only the stage you are in today.
4. Come back later for the rest. Do NOT start a stage until its owner is named.

---

# LIFECYCLE OWNERSHIP: [[PROJECT NAME]]

*AI-Driven Development Life Cycle: from first idea to the first 500 customers*

## Table of Contents

- [Part 0: Project Card and Version History](#part-0-project-card-and-version-history)
- [Part 1: Project Basics](#part-1-project-basics)
- [Part 2: People and Owners](#part-2-people-and-owners)
- [Part 3: AI Agent Workflow](#part-3-ai-agent-workflow)
- [Part 4: The 14 Lifecycle Stages](#part-4-the-14-lifecycle-stages)
- [Part 5: The Road to 500 Customers](#part-5-the-road-to-500-customers)
- [Part 6: Risk Register](#part-6-risk-register)
- [Part 7: Decision Log](#part-7-decision-log)
- [Part 8: Handover and Continuity](#part-8-handover-and-continuity)
- [Part 9: Document Map](#part-9-document-map)
- [Part 10: Lessons Learned](#part-10-lessons-learned)
- [Part 11: Final Sign-off](#part-11-final-sign-off)
- [Appendix A: Glossary](#appendix-a-glossary)
- [Appendix B: A Filled-In Example](#appendix-b-a-filled-in-example)
- [Appendix C: Common Mistakes](#appendix-c-common-mistakes)

---

# Part 0: Project Card and Version History

## 0.1 Project Card **[REQUIRED]**

| Field | Your answer |
|---|---|
| Project name | `[[PROJECT NAME]]` |
| Project ID (short unique code, e.g. `PRJ-0042`) | `[[PROJECT ID]]` |
| One-sentence description | `[[ONE SENTENCE: "A [type of product] that helps [who] to [do what]."]]` |
| Product type | ☐ Web app / SaaS  ☐ Mobile app (iOS)  ☐ Mobile app (Android)  ☐ Web + Mobile |
| Project owner (the ONE person in charge of everything) | `[[FULL NAME]]` |
| Date this file was created | `[[YYYY-MM-DD]]` |
| Date of last update | `[[YYYY-MM-DD]]` |
| Template version used | `1.0.0` |
| Current stage (number and name) | `[[e.g. Stage 5 - Development]]` |
| Overall status | ☐ On track  ☐ At risk  ☐ Blocked  ☐ Paused  ☐ Completed  ☐ Cancelled |
| Where this project's main folder lives | `[[FOLDER PATH OR LINK]]` |
| Where the code lives | `[[REPOSITORY LINK]]` |

**Example:** One-sentence description: "A mobile app that helps busy people remember when to water their houseplants."

## 0.2 Version History **[REQUIRED]**

Add one new row every time you change this document in an important way.

| Version | Date | Changed by | What changed (one line) |
|---|---|---|---|
| 0.1 | `[[YYYY-MM-DD]]` | `[[NAME]]` | First draft created from the template |
| | | | |

---

# Part 1: Project Basics

*Goal: anyone can understand the project in 5 minutes.*

## 1.1 The problem **[REQUIRED]**

**Q1.1.1: What problem are you solving? Describe it as if explaining to a friend.**
*Example: "People buy plants and then forget to water them, so the plants die."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q1.1.2: Who has this problem? (Your first target customer.)**
*Example: "City apartment dwellers aged 22-40 who own 3 or more houseplants."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q1.1.3: How do people solve this problem today without your product?**
*Example: "Sticky notes, phone reminders, or they just forget."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q1.1.4: Why is your solution better? (One or two sentences.)**
*Example: "It knows each plant's type and reminds you at the right time, with one tap to log watering."*
**Your answer:** `[[YOUR ANSWER HERE]]`

## 1.2 The goal **[REQUIRED]**

**Q1.2.1: What does "success" look like? Complete the sentence.**
*Example: "Success = 500 people have used the product, at least 100 of them still use it every week, and at least 50 would be upset if it disappeared."*
**Your answer:** `Success = [[YOUR ANSWER HERE]]`

**Q1.2.2: What is the target date for the first public launch?**
**Your answer:** `[[YYYY-MM-DD]]`

**Q1.2.3: What is the target date for reaching 500 customers?**
**Your answer:** `[[YYYY-MM-DD]]`

**Q1.2.4: What is the single most important thing the product must do well? (Your "core promise".)**
*Example: "Send a correct watering reminder on time."*
**Your answer:** `[[YOUR ANSWER HERE]]`

## 1.3 Limits and boundaries **[REQUIRED]**

| Question | Your answer |
|---|---|
| Money: total budget until 500 customers | `[[AMOUNT AND CURRENCY]]` |
| Money: monthly spend limit on tools, AI, hosting | `[[AMOUNT AND CURRENCY]]` |
| Time: hours per week you can work on this | `[[NUMBER]]` |
| What is OUT of scope for now? (things you will NOT build before 500 customers) | `[[LIST AT LEAST 3 THINGS]]` |
| Anything legally or ethically off-limits? (e.g. children's data, health data, payments) | `[[YOUR ANSWER OR "None known"]]` |

## 1.4 Tech choices **[REQUIRED]**

| Area | Your choice | Why (one line) |
|---|---|---|
| Platform(s) | `[[WEB / iOS / ANDROID]]` | `[[REASON]]` |
| Programming language(s) and framework(s) | `[[YOUR ANSWER]]` | `[[REASON]]` |
| Hosting / cloud provider | `[[YOUR ANSWER]]` | `[[REASON]]` |
| Database | `[[YOUR ANSWER]]` | `[[REASON]]` |
| Login / accounts system | `[[YOUR ANSWER]]` | `[[REASON]]` |
| Payments provider (if you charge money) | `[[YOUR ANSWER OR "None"]]` | `[[REASON]]` |
| Email / notification provider | `[[YOUR ANSWER]]` | `[[REASON]]` |
| Analytics tool | `[[YOUR ANSWER]]` | `[[REASON]]` |
| Error and crash monitoring tool | `[[YOUR ANSWER]]` | `[[REASON]]` |
| Customer support tool (inbox, chat, tickets) | `[[YOUR ANSWER]]` | `[[REASON]]` |

---

# Part 2: People and Owners

*Rules: one owner per stage. An owner is a real person's name. A backup is the person who steps in if the owner is away. In a solo project you may be the owner of everything. If so, write your own name each time, and name a backup you trust (a friend, a freelancer, or an advisor).*

## 2.1 The people list **[REQUIRED]**

| Role | Name | How to reach them | Time zone | Backup for this person |
|---|---|---|---|---|
| Project owner (final decision-maker) | `[[NAME]]` | `[[EMAIL / PHONE / CHAT]]` | `[[TZ]]` | `[[NAME]]` |
| Builder (writes or directs the code) | `[[NAME]]` | `[[CONTACT]]` | `[[TZ]]` | `[[NAME]]` |
| Designer (or the person making design choices) | `[[NAME]]` | `[[CONTACT]]` | `[[TZ]]` | `[[NAME]]` |
| Tester (checks that things work) | `[[NAME]]` | `[[CONTACT]]` | `[[TZ]]` | `[[NAME]]` |
| Customer support person | `[[NAME]]` | `[[CONTACT]]` | `[[TZ]]` | `[[NAME]]` |
| Legal / privacy advisor (if any) | `[[NAME OR "None yet"]]` | `[[CONTACT]]` | `[[TZ]]` | `[[NAME]]` |
| Emergency contact (if the owner cannot be reached) | `[[NAME]]` | `[[CONTACT]]` | `[[TZ]]` | n/a |

## 2.2 Who owns each stage? **[REQUIRED]**

*One row per stage. "Owner" = the ONE accountable person. "Does the work" = who actually does it (a person and/or an AI agent from Part 3). "Asked for advice" = people consulted. "Kept informed" = people who just get updates.*

| # | Stage | Owner (ONE name) | Backup owner | Does the work (person + AI agent) | Asked for advice | Kept informed |
|---|---|---|---|---|---|---|
| 1 | Idea and Problem Validation | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 2 | Requirements and Scope | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 3 | Design (Look and Feel) | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 4 | Architecture and Technical Setup | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 5 | Development (Building) | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 6 | Code Review and Integration | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 7 | Testing and Quality Assurance | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 8 | Security, Privacy and Legal | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 9 | Beta / Pilot | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 10 | Launch Readiness (Go / No-Go) | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 11 | Launch Day | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 12 | First 100 Customers: Support and Feedback | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 13 | Growth from 100 to 500 Customers | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 14 | Review, Handover and Lessons Learned | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |

## 2.3 Ownership self-check **[REQUIRED]**

- [ ] Every stage has exactly ONE owner name (not "team", not "we", not blank).
- [ ] Every owner has a backup who is a DIFFERENT person.
- [ ] No single person owns more stages at the same time than they can handle (write the number you think is fair: `[[NUMBER]]`).
- [ ] Every person listed knows they are listed and agreed to it.
- [ ] If an owner leaves or is unavailable for more than 3 days, the backup takes over automatically.

## 2.4 What happens when nobody answers? **[REQUIRED]**

**Q2.4.1: If a decision is waiting and the owner does not reply, how many hours or days until the backup decides?**
*Example: "24 hours for normal things, 2 hours during a launch emergency."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q2.4.2: Who has the final say if two people disagree?**
**Your answer:** `[[NAME]]`

---

# Part 3: AI Agent Workflow

*This part explains how AI helps build the product, and the safety rules it must follow. Think of AI agents like very fast helpers who still need a human boss. AI can prepare and suggest; humans decide.*

## 3.1 The three levels of AI help **[REQUIRED READING]**

| Level | What it means | Example |
|---|---|---|
| 🧑 **HUMAN DECISION** | Only a human decides. AI may give information but cannot choose. | Pricing, launch go/no-go, deleting customer data, legal wording, spending money |
| 🤝 **AI ASSIST** | AI makes a draft; a human reads, checks, and approves it before it is used. | Writing code for a new feature, drafting a privacy policy, writing test plans |
| 🤖 **AI AUTOMATE** | AI does a safe, repeatable job by itself; a human spot-checks the results regularly. | Running tests on every code change, formatting code, summarizing support emails |

## 3.2 Your AI tools **[REQUIRED]**

| Tool name | What it is used for | Who set it up | Monthly cost limit | Where its settings are kept |
|---|---|---|---|---|
| `[[e.g. Claude Code]]` | `[[e.g. writing and testing code]]` | `[[NAME]]` | `[[AMOUNT]]` | `[[LINK / LOCATION]]` |
| `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |

## 3.3 Your AI agent roster **[REQUIRED]**

*An "agent" here means one AI helper with ONE narrow job. Narrow jobs are safer and easier to check than one agent doing everything. Delete rows you do not need, add rows you do.*

| Agent name | Its ONE job | Level (🧑/🤝/🤖) | Human who checks its work | What it can touch | What it must NEVER touch |
|---|---|---|---|---|---|
| Requirements Agent | Turns my ideas and customer notes into clear written requirements | 🤝 | `[[NAME]]` | Docs folder | Code, customer data |
| Design Agent | Suggests screens, layouts, and wording | 🤝 | `[[NAME]]` | Design files | Production systems |
| Code Agent | Writes and changes code in a branch | 🤝 | `[[NAME]]` | Code repository (non-main branches) | Production, secrets, main branch without review |
| Review Agent | Reads code changes and flags problems | 🤖 | `[[NAME]]` | Code repository (read-only) | Anything it can change |
| Test Agent | Writes and runs tests, reports failures | 🤖 | `[[NAME]]` | Test environment | Production data |
| Security Agent | Scans for weak spots and leaked secrets | 🤖 | `[[NAME]]` | Code repository (read-only) | Live customer data |
| Docs Agent | Keeps documentation up to date | 🤝 | `[[NAME]]` | Docs folder | Code |
| Support Agent | Drafts replies and groups customer feedback | 🤝 | `[[NAME]]` | Support inbox (drafts only) | Sending replies without approval, refunds |
| Analytics Agent | Summarizes numbers and spots trends | 🤖 | `[[NAME]]` | Analytics (read-only) | Raw personal data exports |
| `[[YOUR OWN AGENT]]` | `[[ONE JOB]]` | `[[LEVEL]]` | `[[NAME]]` | `[[ALLOWED]]` | `[[FORBIDDEN]]` |

## 3.4 The "Context Pack": what every AI agent must read first **[REQUIRED]**

*AI works best when it is given the same clear background every time. List the files an AI agent must read before starting any task.*

| File | Where it is | What it tells the AI | Owner who keeps it current |
|---|---|---|---|
| This file (Lifecycle Ownership) | `[[LINK]]` | Who owns what, and the stage rules | `[[NAME]]` |
| Product requirements | `[[LINK]]` | What we are building and why | `[[NAME]]` |
| Architecture and tech rules | `[[LINK]]` | How the system is built, coding rules | `[[NAME]]` |
| Design guide | `[[LINK]]` | Colors, fonts, tone of voice | `[[NAME]]` |
| AI instructions file (e.g. `AGENTS.md` or `CLAUDE.md`) | `[[LINK]]` | Short rules for the AI in the code repository | `[[NAME]]` |
| Glossary of project words | `[[LINK]]` | What our special words mean | `[[NAME]]` |

## 3.5 Rules every AI agent follows **[REQUIRED. Tick what applies, add your own.]**

- [ ] AI never works directly on live/production systems without a human approving each change.
- [ ] AI never sees real passwords, API keys, or payment details. Secrets are stored in a secrets manager and given to systems, not to AI chats.
- [ ] AI never receives real customer personal data unless the owner approved it in writing in the Decision Log (Part 7).
- [ ] AI-written code is always reviewed by a human or by the Review Agent plus a human spot-check before it is merged.
- [ ] AI work happens in a separate branch or draft, never straight into the final version.
- [ ] AI must say "I do not know" instead of guessing. Any guess must be labeled as a guess.
- [ ] AI never deletes data or files permanently. Deleting is a human action.
- [ ] AI never sends messages to customers, posts publicly, or spends money without human approval.
- [ ] Every AI task has a written goal, a "done" definition, and a named human checker.
- [ ] Our own extra rule: `[[YOUR RULE]]`
- [ ] Our own extra rule: `[[YOUR RULE]]`

## 3.6 Handoffs: how work moves between AI and humans **[REQUIRED]**

**Q3.6.1: Where do you give an AI agent its task, and how do you write it? (A simple task format keeps it clear.)**
*Example: "I write a task in the file `tasks/TASK-014.md` with: Goal, Inputs, Done when, Do not touch."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.6.2: Where does the AI put its finished work so a human can check it?**
*Example: "In a branch named `ai/TASK-014` with a pull request."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.6.3: How does a human say "approved" or "redo"? Where is that recorded?**
*Example: "A comment on the pull request. Approved = merged. Redo = comment explaining what to fix."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.6.4: If an AI agent gets stuck, confused, or loops, what happens?**
*Example: "After 3 failed tries it stops and writes 'BLOCKED: reason' in the task file, and the owner is notified."*
**Your answer:** `[[YOUR ANSWER HERE]]`

## 3.7 Logging: keeping a record of what AI did **[REQUIRED]**

**Q3.7.1: Where is the log of AI actions kept? (What was asked, what was changed, who approved.)**
*Example: "Pull request history plus a monthly `ai-log.md`."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.7.2: How often does a human review the AI log for surprises?**
**Your answer:** `[[e.g. Every Friday]]`

**Q3.7.3: How do you check that AI-written code is correct, secure, and not copied from somewhere it should not be?**
*Example: "Automated tests, a security scan, human review, and a license scan."*
**Your answer:** `[[YOUR ANSWER HERE]]`

## 3.8 AI mistakes and emergencies **[REQUIRED]**

**Q3.8.1: What counts as an "AI incident"? (e.g. AI changed the wrong thing, leaked data, deleted something, produced harmful content.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.8.2: Who is told first, and how fast?**
**Your answer:** `[[NAME AND TIME LIMIT]]`

**Q3.8.3: How do you undo AI changes? (Backups, version history, rollback steps.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

## 3.9 If your product itself uses AI (answer only if it does) **[OPTIONAL]**

| Question | Your answer |
|---|---|
| What does the AI inside the product do for customers? | `[[ANSWER OR N/A]]` |
| Which AI model/provider is used, and which version? | `[[ANSWER]]` |
| How do you check its answers are good? (test questions, sample reviews) | `[[ANSWER]]` |
| What happens when the AI is wrong or unavailable? | `[[ANSWER]]` |
| Do customers know they are talking to AI? Where is that said? | `[[ANSWER]]` |
| Is customer data sent to the AI provider? Is it used for training? | `[[ANSWER]]` |
| Spending limit per customer / per month for AI usage | `[[ANSWER]]` |

---

# Part 4: The 14 Lifecycle Stages

## How to use Part 4

- Work through the stages **in order**. A stage is only finished when **every "Done when" box is ticked**.
- At the top of each stage, fill in the **Stage Card** (owner, dates, status).
- Answer the questions, then fill the **Done when** gate. If you cannot tick a box, write in the "Blocked because" line.
- You may run two stages together (for example 5 and 6) only if each still has its own named owner.
- Never skip Stage 8 (Security, Privacy and Legal) or Stage 10 (Go / No-Go). These protect you and your customers.

### Stage overview map

```
1 Idea → 2 Requirements → 3 Design → 4 Architecture → 5 Build → 6 Review
  → 7 Testing → 8 Security/Legal → 9 Beta → 10 Go/No-Go → 11 Launch
  → 12 First 100 customers → 13 Grow to 500 → 14 Review & Handover
```

### Stage Card (copy this pattern; it already appears inside each stage)

| Field | Meaning |
|---|---|
| Owner | The ONE accountable person |
| Backup | Who steps in |
| Status | Not started / In progress / Blocked / Done |
| Start / Target end / Actual end | Dates |
| AI helpers | Agents from Part 3 used in this stage |
| Blocked because | Only fill when stuck |

---

## Stage 1: Idea and Problem Validation

**Purpose:** Prove that a real problem exists and that real people want it solved, *before* spending months building.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Requirements Agent for summarizing interviews]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤝 AI ASSIST for research and summaries. 🧑 HUMAN DECISION for "is this worth building?"

**Q1.1: How many real people did you talk to about the problem? Who were they?**
*Example: "12 people: 8 from a plant-lovers group, 4 coworkers. Notes are in `research/interviews.md`."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q1.2: What were the top 3 things they said? (Use their words if you can.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q1.3: Who else already solves this? What do they do well and badly?**
*Example: "Competitor A is free but ugly. Competitor B costs $10/month and has too many features."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q1.4: Would anyone pay, or give something valuable (time, email, a pre-order)? Proof?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q1.5: What is the biggest reason this could fail?**
**Your answer:** `[[YOUR ANSWER HERE]]` *(Also add it to the Risk Register, Part 6.)*

**Done when (Gate):**
- [ ] At least `[[NUMBER, suggest 10]]` real people were asked about the problem.
- [ ] The problem is written in one clear sentence (Part 1.1).
- [ ] At least 3 existing alternatives are listed.
- [ ] There is evidence (not just opinion) that people want a solution.
- [ ] The owner decided: ☐ GO ☐ CHANGE DIRECTION ☐ STOP. Date: `[[DATE]]`. Recorded in Decision Log.

**Output documents:** `[[LINKS: interview notes, competitor list]]`

---

## Stage 2: Requirements and Scope

**Purpose:** Write down exactly what the first version (MVP, the smallest useful product) will and will not do.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Requirements Agent]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤝 AI ASSIST to draft requirements. 🧑 HUMAN DECISION on what is in or out of scope.

**Q2.1: List the "must-have" features for version 1. (Without these the product is useless.)**
*Example: "Add a plant, set watering days, receive a reminder, mark as watered."*
**Your answer:** `[[LIST]]`

**Q2.2: List the "nice-to-have" features for LATER. (Not in version 1.)**
**Your answer:** `[[LIST]]`

**Q2.3: For each must-have feature, how will you know it works? (Write it as a simple test.)**
*Example: "When I set a reminder for 9:00, my phone shows a notification at 9:00."*
**Your answer:** `[[LIST]]`

**Q2.4: What rules or limits must the product obey? (speed, devices, languages, accessibility, age limits)**
*Example: "Must work on phones from the last 4 years; must load in under 3 seconds."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q2.5: What is the pricing plan for the first customers? (Free, trial, paid, price.)**
**Your answer:** `[[YOUR ANSWER HERE]]` 🧑 *(A human must decide pricing.)*

**Q2.6: How will new customers find the product? (Your first 3 ways of reaching people.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Done when (Gate):**
- [ ] A written requirements document exists and is linked in Part 9.
- [ ] Must-have and nice-to-have lists are separate.
- [ ] Every must-have has a simple pass/fail test.
- [ ] The "out of scope" list (Part 1.3) is up to date.
- [ ] The scope is small enough to build by `[[TARGET DATE]]`.
- [ ] The owner approved the scope. Date: `[[DATE]]`.

**Output documents:** `[[LINKS: requirements doc, feature list]]`

---

## Stage 3: Design (Look and Feel)

**Purpose:** Decide how the product looks, feels, and flows *before* it is built.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Design Agent]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤝 AI ASSIST for layouts and wording ideas. 🧑 HUMAN DECISION for the final look and brand.

**Q3.1: What is the product's name, logo, main colors, and fonts? Where are they stored?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.2: What are the 3-5 most important screens/pages? Link to sketches or mockups.**
*Example: "Home (my plants), Add Plant, Reminder, Settings. Mockups: [link]."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.3: What is the first-time-user journey from opening the product to getting value? (List the steps.)**
*Example: "Open → create account → add first plant → set reminder → see success message."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.4: How will you make it usable for everyone? (readable text size, color contrast, screen-reader labels)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.5: Did at least 3 people who match your customer try the design and say what confused them?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.6 [MOBILE]: Which phone sizes and system versions will you support? Do the designs follow Apple's and Google's design guidelines?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q3.7 [WEB]: Which browsers and screen sizes will you support (phone, tablet, desktop)?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Done when (Gate):**
- [ ] Designs exist for every must-have feature.
- [ ] The first-time-user journey is drawn.
- [ ] At least 3 people from the target group saw the design and feedback was recorded.
- [ ] Brand assets (logo, colors, fonts) are saved in one place and linked in Part 9.
- [ ] The owner approved the design. Date: `[[DATE]]`.

**Output documents:** `[[LINKS: mockups, design guide]]`

---

## Stage 4: Architecture and Technical Setup

**Purpose:** Decide how the product is built and prepare a safe workshop (tools, accounts, environments) before real coding starts.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Code Agent for scaffolding, Docs Agent]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤝 AI ASSIST for proposing designs and setup. 🧑 HUMAN DECISION for technology choices, costs, and anything touching secrets or accounts.

**Q4.1: Draw or describe the main parts of the system and how they talk to each other.**
*Example: "Phone app → our server → database. The server also talks to the email service."*
**Your answer:** `[[YOUR ANSWER OR LINK TO DIAGRAM]]`

**Q4.2: What data will you store about customers? (List each kind and why you need it.)**
*Example: "Email (login), plant list (core feature). No birthdays, no location."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q4.3: What are your separate environments? (e.g. Development = my laptop, Staging = a safe copy, Production = the real thing customers use.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q4.4: Where are secrets (passwords, keys) stored? Who has access? (Write the location, never the secret.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q4.5: How are backups made, how often, and has restoring from a backup ever been tested?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q4.6: What is the estimated monthly cost at 0, 100, and 500 customers?**
**Your answer:** `0 customers: [[ ]]   100 customers: [[ ]]   500 customers: [[ ]]`

**Q4.7: What coding rules must everyone (including AI) follow? (naming, folders, testing expectations)**
**Your answer:** `[[YOUR ANSWER OR LINK]]`

**Q4.8: How does new code get from a laptop to customers? (the release pipeline)**
*Example: "Code is merged → automatic tests run → staging → I click approve → production."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q4.9 [MOBILE]: Do you have developer accounts (Apple Developer Program, Google Play Console)? Who owns them? Which email is registered?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q4.10 [WEB]: What is the domain name? Who owns the registration, and when does it renew?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Safety / risk check:**
- [ ] Two-step login (2FA) is on for every important account (hosting, code, domain, app stores, payments).
- [ ] The owner AND the backup can both get into every critical account.
- [ ] No secrets are saved in the code or in chat messages with AI.

**Done when (Gate):**
- [ ] The architecture is described and linked in Part 9.
- [ ] Development, staging, and production environments exist and are separate.
- [ ] Backups are set up.
- [ ] The code repository, task board, and release pipeline work (a "hello world" test went all the way through).
- [ ] The AI instructions file (Part 3.4) exists in the repository.
- [ ] The owner approved the technical plan. Date: `[[DATE]]`.

**Output documents:** `[[LINKS: architecture doc, diagrams, cost estimate]]`

---

## Stage 5: Development (Building)

**Purpose:** Build the must-have features, in small safe steps.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Code Agent, Test Agent, Docs Agent]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤝 AI ASSIST for writing code. 🤖 AI AUTOMATE for formatting and running tests. 🧑 HUMAN DECISION to merge anything into the main version.

**Q5.1: How is the work cut into small pieces? (Where is the task list, and how big is one task?)**
*Example: "Task board link. One task should take at most 1 day. Bigger ones are split."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q5.2: What order will you build the must-have features in, and why?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q5.3: How often will you show or demo progress? To whom?**
**Your answer:** `[[e.g. Every Friday, to my advisor]]`

**Q5.4: When is a single task "done"? (Your Definition of Done.)**
*Example: "Code written + tests pass + a human reviewed it + documentation updated."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q5.5: What happens when a task takes much longer than planned?**
*Example: "At 2x the estimate I stop, decide whether to shrink the task or move it later, and note it in the Decision Log."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q5.6: What tracking do you add while building? (analytics events for key actions, error reporting, logs)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q5.7: How do you keep AI-written code understandable by a human who joins later?**
*Example: "Comments explain WHY, each feature has a short note in the docs folder."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Safety / risk check:**
- [ ] No real customer data is used in development. Fake test data only.
- [ ] Every third-party package/library is listed with its license `[[LINK TO LIST]]`.
- [ ] Features beyond the agreed scope are NOT being added (scope creep check).

**Done when (Gate):**
- [ ] Every must-have feature from Stage 2 is built.
- [ ] Each feature meets its Definition of Done (Q5.4).
- [ ] The product runs end to end in the staging environment.
- [ ] Analytics and error reporting work in staging.
- [ ] Documentation is current (how to run it, how to release it).
- [ ] The owner confirmed the build is complete. Date: `[[DATE]]`.

**Output documents:** `[[LINKS: repository, task board, release notes]]`

---

## Stage 6: Code Review and Integration

**Purpose:** A second pair of eyes (human and AI) checks quality before anything is combined into the main product.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Review Agent, Security Agent]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤖 AI AUTOMATE for first-pass review. 🧑 HUMAN DECISION for final approval to merge.

**Q6.1: Who reviews the code, and what do they look for? (Correct, readable, safe, matches requirements.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q6.2: If you are working alone, who is your outside reviewer? (A friend, a freelancer, a mentor, or an extra-careful AI review plus a "sleep on it" rule.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q6.3: What automatic checks must pass before code is merged?**
*Example: "All tests, style check, security scan, and the app builds successfully."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q6.4: How are bugs found in review recorded and fixed?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Done when (Gate):**
- [ ] All code in the release version was reviewed by someone other than its writer (AI counts as the writer for AI-written code).
- [ ] Automatic checks pass.
- [ ] All "must-fix" review comments are resolved.
- [ ] The release version is "frozen" (only bug fixes allowed from now on). Date: `[[DATE]]`.

**Output documents:** `[[LINKS: review records]]`

---

## Stage 7: Testing and Quality Assurance (QA)

**Purpose:** Prove the product works for real people, in real situations, and does not break easily.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Test Agent]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤖 AI AUTOMATE for running repeated tests. 🤝 AI ASSIST for writing test cases. 🧑 HUMAN DECISION on whether quality is good enough.

**Q7.1: What kinds of testing will you do? Tick the ones you will do and say who does them.**

| Test type | Plain meaning | Will do? | Who |
|---|---|---|---|
| Feature test | Does each feature do what the requirement says? | ☐ Yes ☐ No | `[[ ]]` |
| Full-journey test | Can a new user complete the whole journey (sign up → get value)? | ☐ Yes ☐ No | `[[ ]]` |
| Break-it test | What happens with wrong inputs, no internet, slow connection? | ☐ Yes ☐ No | `[[ ]]` |
| Speed test | Is it fast enough, also with many users at once? | ☐ Yes ☐ No | `[[ ]]` |
| Device/browser test | Does it work on the devices and browsers we promised? | ☐ Yes ☐ No | `[[ ]]` |
| Accessibility test | Can people with different needs use it? | ☐ Yes ☐ No | `[[ ]]` |
| Payment test (if paid) | Do purchases, refunds, and failed cards work (test mode)? | ☐ Yes ☐ No | `[[ ]]` |
| Upgrade test | Can customers get a new version without losing data? | ☐ Yes ☐ No | `[[ ]]` |
| Restore test | Can you actually restore from a backup? | ☐ Yes ☐ No | `[[ ]]` |

**Q7.2 [MOBILE]: Which real phones (not just simulators) did you test on? List models and system versions.**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q7.3 [WEB]: Which browsers and screen sizes did you test? Was it tested on a real phone?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q7.4: How do you rate bugs?**

| Level | Meaning | Rule |
|---|---|---|
| Blocker | Product unusable, data lost, security hole | Must fix before launch |
| Major | Important feature broken, no easy workaround | Must fix before launch |
| Minor | Annoying but there is a workaround | Can launch; fix later (list it) |
| Cosmetic | Small visual issue | Can launch |

**Q7.5: What is the number of open bugs you accept at launch?**
**Your answer:** `Blockers: 0   Majors: 0   Minors: [[NUMBER]]`

**Done when (Gate):**
- [ ] Every must-have feature passed its pass/fail test from Stage 2.
- [ ] The full journey works on all promised devices/browsers.
- [ ] Zero open Blocker and Major bugs.
- [ ] Remaining Minor/Cosmetic bugs are written in a list: `[[LINK]]`.
- [ ] A backup restore was successfully tested.
- [ ] The owner accepted the test results. Date: `[[DATE]]`.

**Output documents:** `[[LINKS: test plan, test results, bug list]]`

---

## Stage 8: Security, Privacy and Legal

**Purpose:** Protect customers' data, and make sure you are legally allowed to launch. *This stage is not optional.*

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Security Agent, Docs Agent for drafts]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤖 AI AUTOMATE for security scanning. 🤝 AI ASSIST for first drafts of policies. 🧑 HUMAN DECISION for anything legal (ideally checked by a qualified lawyer; AI is not a lawyer).

> **Note:** Laws differ by country and change over time. Write which countries/regions your customers live in and check the rules for each one.

**Q8.1: Where do your customers live? (Countries/regions.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q8.2: What personal data do you collect, why, where is it stored, and how long do you keep it?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q8.3: Which privacy and data laws might apply? (Examples: GDPR in Europe, CCPA/CPRA in California, rules for children's data, health or payment data rules.) Who checked?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q8.4: How can a customer see, correct, export, or delete their data? Who handles such a request, and how fast?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q8.5: Which third parties receive customer data? (Payments, analytics, email, AI providers.)**

| Third party | What data they get | Why | Their privacy/terms link |
|---|---|---|---|
| `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |

**Q8.6: Who checked the product for common security weak spots?**
*Example: "Automatic scan + manual check of the login, payment, and data-access features against a standard security checklist."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Security checklist**
- [ ] All traffic is encrypted (HTTPS / secure connections).
- [ ] Passwords are never stored as plain text; login is handled by a trusted system.
- [ ] Each customer can only see their own data (tested with two test accounts).
- [ ] Secrets are not in the code or in public files (scanned).
- [ ] Software packages are up to date and checked for known problems.
- [ ] Rate limits / protection against repeated login attempts exist.
- [ ] Logs do not contain passwords or full personal data.
- [ ] There is a written plan for a data leak (who is told, in what time, what is said).

**Legal checklist**
- [ ] **Privacy Policy** is written, published at a live web address, linked inside the product and (for apps) in the store listing.
- [ ] **Terms of Service** is written and published.
- [ ] Customers actively agree to terms (checkbox or clear button) where required.
- [ ] Cookie/consent notice is in place where required. [WEB]
- [ ] Refund and cancellation rules are written (if you charge money).
- [ ] Business registration, tax setup, and payment-provider requirements are handled: `[[NOTES]]`
- [ ] Trademarks/names/images/fonts/music used are legally allowed (licenses saved).
- [ ] Age rating and content rules are answered honestly. [MOBILE]
- [ ] App-store privacy/data-safety forms are filled in and match what the product really does. [MOBILE]
- [ ] Open-source licenses of included packages are compatible with how you use the product.

**Done when (Gate):**
- [ ] All security and legal checklists above are ticked, or each unticked item has a written reason and an accepted-risk decision in the Decision Log.
- [ ] Privacy Policy and Terms are live and linked.
- [ ] A data-leak response plan exists: `[[LINK]]`
- [ ] The owner AND (if available) a qualified advisor reviewed the legal items. Date: `[[DATE]]`.

**Output documents:** `[[LINKS: privacy policy, terms, security checklist, license list]]`

---

## Stage 9: Beta / Pilot

**Purpose:** Let a small, friendly group use the real product, so surprises happen before the public launch.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Support Agent, Analytics Agent]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤝 AI ASSIST for grouping feedback. 🤖 AI AUTOMATE for usage summaries. 🧑 HUMAN DECISION on what to fix first.

**Q9.1: How many beta users will you invite, who are they, and how will you recruit them?**
*Example: "20-30 people from the plant-lovers group who said yes in Stage 1."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q9.2: How long will the beta last?**
**Your answer:** `[[e.g. 3 weeks]]`

**Q9.3: What exactly will you learn from the beta? (List 3 questions.)**
*Example: "Do they reach their first reminder within 10 minutes? Where do they get stuck? Would they be disappointed if it disappeared?"*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q9.4: How will beta users give feedback, and how do they get help?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q9.5: What do you tell beta users about the product being unfinished and about their data?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q9.6 [MOBILE]: How do you distribute the beta? (e.g. TestFlight for iOS, a closed/internal testing track for Android.) Are store testing requirements met?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q9.7: What is your "aha moment"? (The first moment a user feels the value.) How is it measured?**
*Example: "User receives and acts on their first reminder."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Done when (Gate):**
- [ ] The planned number of beta users actually used the product.
- [ ] Feedback was collected, grouped, and ranked: `[[LINK]]`
- [ ] The top problems found were fixed or consciously postponed (with reasons).
- [ ] At least `[[NUMBER]]`% of beta users reached the "aha moment".
- [ ] No new Blocker or Major bugs remain.
- [ ] The owner decided the product is ready for the Go / No-Go review. Date: `[[DATE]]`.

**Output documents:** `[[LINKS: feedback summary, beta metrics]]`

---

## Stage 10: Launch Readiness (Go / No-Go)

**Purpose:** One final, honest check before showing the product to the world. **One person makes the call.**

| Stage Card | |
|---|---|
| Owner (the "Launch Owner", makes the Go / No-Go call) | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Docs Agent for the checklist, Test Agent for a final run]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤖 AI AUTOMATE for final checks. 🧑 HUMAN DECISION: GO or NO-GO is always human.

**Q10.1: What is the planned launch date and time? Is it a good day (not a holiday, and not a day you cannot be available)?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.2: Who will be available during launch day and the 3 days after? List names and hours.**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.3: What is the "stop signal"? (What bad thing would make you pause or undo the launch?)**
*Example: "Crash-free sessions below 98%, or any data-leak report, or payment failures above 5%."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.4: What is the rollback plan? (How do you go back to the previous version, and how long does it take?)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.5: What is the rollout plan? (Everyone at once, or a small percentage first and then more?)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Launch readiness checklist: tick only what is truly done**

*Product*
- [ ] Stage 7 (Testing), Stage 8 (Security/Legal) and Stage 9 (Beta) gates are all done.
- [ ] Production environment is set up and tested with a real (own) test purchase/signup.
- [ ] Backups are running in production.
- [ ] Monitoring and alerts work (errors, downtime, slow responses). Alerts go to: `[[NAME / CHANNEL]]`
- [ ] Analytics track the key steps (signup, aha moment, purchase).

*Accounts and access*
- [ ] Domain, hosting, email sending, and payment accounts are paid/active and renew automatically. [WEB]
- [ ] Custom domain connected (not a temporary test address). [WEB]
- [ ] Email sending is verified so messages do not land in spam. 

*Store and publishing* [MOBILE]
- [ ] Store listing complete: name, description, screenshots, icon, keywords, category.
- [ ] Privacy policy link, age rating, and data-safety/privacy answers are complete and accurate.
- [ ] Release build is signed and submitted; store review approval received (or a buffer of days is planned).
- [ ] Release date is shown as a range until approval is confirmed.

*Customers and support*
- [ ] Support email/chat works and a human answers within `[[TIME]]`.
- [ ] Help articles or a short FAQ exist (at least the top 5 questions).
- [ ] Onboarding (first-use experience) is tested by someone new.
- [ ] Pricing, trial, and cancellation work and are clearly shown.

*Marketing and message*
- [ ] Landing page or store page explains the value in one sentence and has a clear action button.
- [ ] Launch message is written for each channel: `[[LIST CHANNELS]]`
- [ ] First 20 people you will personally tell about the launch: `[[LINK TO LIST]]`

*People and plan*
- [ ] Everyone named in Part 2 knows the launch date and their job.
- [ ] Rollback plan was read by the owner AND the backup.
- [ ] A "what if something breaks" list exists: who does what in the first hour.

**GO / NO-GO decision**

| Item | Your answer |
|---|---|
| Decision | ☐ GO  ☐ GO with conditions  ☐ NO-GO |
| Conditions or reasons | `[[WRITE THEM]]` |
| Decided by | `[[NAME]]` |
| Date and time | `[[YYYY-MM-DD HH:MM]]` |
| Recorded in Decision Log (Part 7) | ☐ Yes |

**Done when (Gate):**
- [ ] Every box in the launch readiness checklist is ticked or has a written, accepted reason.
- [ ] The Go / No-Go table above is filled in.

---

## Stage 11: Launch Day

**Purpose:** Release the product to the public safely and watch it closely.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Analytics Agent for hourly summaries, Support Agent for draft replies]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤖 AI AUTOMATE for monitoring summaries. 🤝 AI ASSIST for drafting replies. 🧑 HUMAN DECISION for every customer-facing message, rollbacks, and fixes in production.

**Q11.1: What are the launch-day steps, in order, with times?**

| Time | Step | Who | Done? |
|---|---|---|---|
| `[[ ]]` | `[[e.g. Release to production]]` | `[[ ]]` | ☐ |
| `[[ ]]` | `[[e.g. Test signup myself on production]]` | `[[ ]]` | ☐ |
| `[[ ]]` | `[[e.g. Announce on channel 1]]` | `[[ ]]` | ☐ |
| `[[ ]]` | `[[e.g. Check dashboards]]` | `[[ ]]` | ☐ |
| `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ |

**Q11.2: What numbers will you watch in the first 24 hours? How often will you check them?**
*Example: "Every hour: signups, crash/error rate, payment failures, support messages."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q11.3: Who decides to pause or roll back, and by what rule?**
**Your answer:** `[[NAME AND RULE]]`

**Q11.4: Where do you record anything unexpected that happens on launch day?**
**Your answer:** `[[LINK TO LAUNCH LOG]]`

**Done when (Gate):**
- [ ] The product is live and a real signup (and purchase if applicable) worked on production.
- [ ] No stop signal was triggered in the first 24 hours (or each one was handled and recorded).
- [ ] The first customers got a human reply to any question.
- [ ] A short launch summary was written: what went well, what broke, what changed. `[[LINK]]`
- [ ] The first 7-day review is scheduled for `[[DATE]]`.

---

## Stage 12: First 100 Customers: Support and Feedback

**Purpose:** Learn fast from your first real customers. Talk to them directly, fix what hurts, and prove people get value and come back.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Support Agent, Analytics Agent]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤝 AI ASSIST for drafting replies and grouping feedback. 🤖 AI AUTOMATE for weekly number summaries. 🧑 HUMAN DECISION for refunds, tone in sensitive replies, what to build next.

**Q12.1: How quickly will you reply to customers, and during which hours?**
*Example: "Within 24 hours, Monday-Friday. Urgent problems: within 4 hours."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q12.2: How will you personally welcome and help each of your first customers?**
*Example: "A personal email from me on day 1 asking what they hope to do, and a check-in on day 7."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q12.3: How do you sort incoming problems and requests?**

| Type | Example | Who handles | Target reply time |
|---|---|---|---|
| Urgent: product broken or data/money at risk | Cannot log in, wrong charge | `[[NAME]]` | `[[TIME]]` |
| Bug | Button does nothing | `[[NAME]]` | `[[TIME]]` |
| Question | "How do I...?" | `[[NAME]]` | `[[TIME]]` |
| Feature request | "Please add..." | `[[NAME]]` | `[[TIME]]` |
| Praise / complaint | "Love it" / "This is bad" | `[[NAME]]` | `[[TIME]]` |

**Q12.4: How often do you review all feedback and decide what to fix or build?**
*Example: "Every Monday, 1 hour. Top 3 items go on the task board."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q12.5: How do you find out why people leave or stop using the product?**
*Example: "Cancellation question: 'What made you leave?' plus a personal email to anyone who stops using it after day 14."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q12.6: What are your rules for fixing urgent problems in production?**
*Example: "Smallest possible fix → test on staging → human approves → release → tell affected customers."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q12.7: What is your plan for the first "silence" signal, customers who sign up and then disappear?**
*Example: "Anyone with no activity for 7 days gets one friendly email and a short help link."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Done when (Gate):**
- [ ] 100 customers reached (using the definition in Part 5.1). Date: `[[DATE]]`
- [ ] Every customer message got a reply within the promised time (or misses were recorded).
- [ ] At least `[[NUMBER, suggest 10]]` customers were spoken to one-on-one.
- [ ] The top 5 customer problems are known, ranked, and each is fixed or planned.
- [ ] Activation (aha moment) rate is measured: `[[NUMBER]]`%.
- [ ] A plan exists for what to improve before pushing for faster growth.

---

## Stage 13: Growth from 100 to 500 Customers

**Purpose:** Find repeatable ways to reach new customers while keeping them happy and the product stable.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Analytics Agent, Support Agent, Code Agent for improvements]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤖 AI AUTOMATE for reports and monitoring. 🤝 AI ASSIST for content drafts and improvements. 🧑 HUMAN DECISION for pricing, spending on ads, and public messages.

**Q13.1: Which 2-3 ways of reaching customers brought your first 100? Which will you do more of?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q13.2: What is the plan to reach the next 400 customers? (Channels, how many per week.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q13.3: What is your monthly budget for reaching customers, and what result do you expect?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q13.4: How do you know the product can handle more customers? (speed, cost, support workload)**
*Example: "Cost per customer is tracked monthly. If support takes more than 10 hours/week, I improve help articles first."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q13.5: How do you release improvements safely now that real customers depend on you?**
*Example: "Small releases, announced in the app; staged rollout; stop signal rules from Stage 10 still apply."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q13.6: When will you ask happy customers for reviews, referrals, or testimonials? How do you make sure they are real?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q13.7: What would make you pause growth and fix things first?**
*Example: "Activation drops below 30%, or refunds above 10%, or support backlog above 2 days."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Done when (Gate):**
- [ ] 500 customers reached (using the definition in Part 5.1). Date: `[[DATE]]`
- [ ] The product stayed stable (no unresolved Blocker bugs, no unhandled data problems).
- [ ] Support is manageable (reply times still met, or a fix is planned).
- [ ] At least `[[NUMBER]]` customers use the product regularly (see Part 5 metrics).
- [ ] The owner recorded what the next growth goal is, or decided to stop/change direction.

---

## Stage 14: Review, Handover and Lessons Learned

**Purpose:** Capture what you learned, tidy up, and make sure anyone could take over the product tomorrow.

| Stage Card | |
|---|---|
| Owner | `[[NAME]]` |
| Backup | `[[NAME]]` |
| Status | ☐ Not started  ☐ In progress  ☐ Blocked  ☐ Done |
| Start / Target end / Actual end | `[[DATE]]` / `[[DATE]]` / `[[DATE]]` |
| AI helpers | `[[e.g. Docs Agent to refresh documentation]]` |
| Blocked because | `[[ONLY IF BLOCKED]]` |

**AI level here:** 🤝 AI ASSIST to draft summaries and refresh docs. 🧑 HUMAN DECISION on what the lessons are and what happens next.

**Q14.1: Did you reach the goal you wrote in Part 1.2? Compare plan vs. reality.**

| Measure | Planned | Actual |
|---|---|---|
| Launch date | `[[ ]]` | `[[ ]]` |
| Date of customer #500 | `[[ ]]` | `[[ ]]` |
| Total money spent | `[[ ]]` | `[[ ]]` |
| Total hours spent | `[[ ]]` | `[[ ]]` |
| Customers still active after 30 days | `[[ ]]` | `[[ ]]` |

**Q14.2: What will happen next with the product? Tick one and explain.**
☐ Keep growing (new goal: `[[ ]]`)  ☐ Hand over to someone else  ☐ Maintain only  ☐ Pause  ☐ Shut down properly

**Q14.3: Fill in Part 8 (Handover) and Part 10 (Lessons Learned) completely.**

**Done when (Gate):**
- [ ] Plan vs. reality table is filled in.
- [ ] Part 8 (Handover and Continuity) is complete, and someone else tested it by following it.
- [ ] Part 10 (Lessons Learned) is complete and copied to the shared knowledge folder.
- [ ] Documentation is current and every link in Part 9 works.
- [ ] Unused accounts, test data, and old secrets were cleaned up or rotated.
- [ ] Part 11 (Final Sign-off) is signed.

---

# Part 5: The Road to 500 Customers

## 5.1 What counts as a "customer"? **[REQUIRED]**

*Decide this on Day 1 and do not change it halfway. Changing the definition later makes your numbers meaningless. If you must change it, write why in the Decision Log.*

**Q5.1.1: Pick ONE definition of "customer" for the 500 goal.**

☐ **A. Signed up** (created an account)
☐ **B. Activated** (reached the aha moment: `[[DESCRIBE IT]]`)
☐ **C. Paying** (made at least one payment)
☐ **D. Active** (used the product at least `[[NUMBER]]` times in the last `[[NUMBER]]` days)
☐ **E. My own definition:** `[[WRITE IT]]`

**Q5.1.2: Why this definition?**
*Example: "Signing up is too easy. Real value is when someone gets their first reminder, so I chose B."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q5.1.3: What do you NOT count?**
*Example: "Test accounts, my own accounts, friends who never opened the app, duplicates, refunded accounts."*
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q5.1.4: Where do you read the customer number from, and who checks that it is correct?**
**Your answer:** `[[TOOL / DASHBOARD LINK AND NAME]]`

## 5.2 The Milestone Ladder **[REQUIRED]**

*Climb one step at a time. At every step, stop and ask: "Is it working? Are people happy? What broke?" Fill in the target date and the lesson as you go.*

| Step | Customers | Target date | Actual date | The main goal at this step | What to check before climbing | Lesson learned |
|---|---|---|---|---|---|---|
| 1 | 1 | `[[ ]]` | `[[ ]]` | Prove the whole journey works for a real stranger | A real person signed up, got value, nothing broke | `[[ ]]` |
| 2 | 10 | `[[ ]]` | `[[ ]]` | Talk to every customer personally | You know each customer's reason for using it | `[[ ]]` |
| 3 | 50 | `[[ ]]` | `[[ ]]` | Find the most common problem and fix it | Top 3 problems are known; the aha moment is clear | `[[ ]]` |
| 4 | 100 | `[[ ]]` | `[[ ]]` | Prove that customers come back | Repeat usage is visible; you know why people stay | `[[ ]]` |
| 5 | 250 | `[[ ]]` | `[[ ]]` | Find a repeatable way to get customers | At least one channel works more than once | `[[ ]]` |
| 6 | 500 | `[[ ]]` | `[[ ]]` | Keep quality while growing; decide what next | Support and stability are manageable | `[[ ]]` |

## 5.3 Metrics: the numbers to watch **[REQUIRED]**

*A "metric" is just a number that tells you how things are going. Only track what you will actually look at. A few good numbers beat many unused ones.*

| Metric | Plain meaning | How it is calculated | Where to read it | Checked how often | Target |
|---|---|---|---|---|---|
| Signups | New people who created an account | Count per week | `[[TOOL]]` | Weekly | `[[ ]]` |
| Activation rate | Share of new users who reach the aha moment | Activated users ÷ new signups × 100, within `[[NUMBER]]` days | `[[TOOL]]` | Weekly | `[[ ]]`% |
| Time to first value | How long until the aha moment | Median time from signup to aha moment | `[[TOOL]]` | Weekly | `[[ ]]` |
| Weekly active users | People who used the product this week | Count | `[[TOOL]]` | Weekly | `[[ ]]` |
| Retention | Share who come back after day 7 / day 30 | Users active on day N ÷ users who signed up N days ago | `[[TOOL]]` | Weekly | `[[ ]]`% |
| Paying customers (if you charge) | People who paid | Count | `[[TOOL]]` | Weekly | `[[ ]]` |
| Revenue (if you charge) | Money received per month | Sum | `[[TOOL]]` | Monthly | `[[ ]]` |
| Churn (people who leave) | Share who stop in a month | Customers lost ÷ customers at start of month × 100 | `[[TOOL]]` | Monthly | `[[ ]]`% |
| Crash / error rate | How often the product fails | Failed sessions ÷ all sessions | `[[TOOL]]` | Daily at launch, then weekly | `[[ ]]`% |
| Support load | Messages per week and time to answer | Count and median reply time | `[[TOOL]]` | Weekly | `[[ ]]` |
| Customer satisfaction | How happy people say they are | Short survey (e.g. 1-5 stars or "How disappointed if this disappeared?") | `[[TOOL]]` | After each milestone | `[[ ]]` |
| Cost per customer | Money spent to get one customer | Spend ÷ new customers | `[[SHEET]]` | Monthly | `[[ ]]` |

> **Beginner tip:** With fewer than about 50-100 customers, percentages like churn jump around wildly and can mislead you. In that early phase, **talk to people and read each case**. Rely on numbers more as your customer count grows. Activation (did new people reach value?) is usually the most useful early number.

## 5.4 Weekly 15-minute check **[REQUIRED]**

Every week, answer these five questions in your notes file `[[LINK TO NOTES FILE]]`:

1. How many new customers this week, and how many total?
2. Of the new people, how many reached the aha moment?
3. What was the #1 complaint or confusion this week?
4. What is the ONE thing I will fix or try next week?
5. Is anything on fire (security, money, data, trust)? If yes, who handles it today?

## 5.5 Feedback and support loop **[REQUIRED]**

*How customer words travel back into the product.*

```
Customer says something → Support inbox → Tagged (bug / question / request)
→ Weekly review → Top items → Task board → Built → Released
→ Tell the customer who asked: "You asked, we fixed it"
```

| Question | Your answer |
|---|---|
| Where can customers reach you? (email, in-app chat, form) | `[[ ]]` |
| Where are all feedback items collected in one place? | `[[ ]]` |
| Who tags and sorts feedback, and how often? | `[[ ]]` |
| How do you decide what to build next? (e.g. most-requested + biggest pain + smallest effort) | `[[ ]]` |
| How do you tell customers that you fixed something? | `[[ ]]` |
| When do you answer personally, and when with a standard reply? | `[[ ]]` |
| What is the rule for refunds and apologies? Who may decide? | `[[ ]]` |

---

# Part 6: Risk Register

*A risk is something that might go wrong. Writing risks down early means you are ready, not scared. Review this table at the end of every stage. Add new risks any time.*

**How to rate:** Likelihood = Low / Medium / High. Impact = Low / Medium / High. **Priority** = High if either is High.

| ID | Stage | Risk (what could go wrong) | Likelihood | Impact | What I will do to prevent it | What I will do if it happens | Risk owner | Status |
|---|---|---|---|---|---|---|---|---|
| R1 | `[[ ]]` | Nobody wants the product | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R2 | `[[ ]]` | A key account (domain, store, hosting) is lost or locked | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R3 | `[[ ]]` | Customer data leaks | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R4 | `[[ ]]` | AI makes a harmful change or wrong decision | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R5 | `[[ ]]` | Owner becomes unavailable (illness, job change) | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R6 | `[[ ]]` | Costs grow faster than money | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R7 | `[[ ]]` | App store rejects or delays the release [MOBILE] | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R8 | `[[ ]]` | A key outside service (payments, AI provider, hosting) fails or changes terms | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R9 | `[[ ]]` | Support gets overwhelmed | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R10 | `[[ ]]` | Legal or privacy rules are broken by mistake | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R11 | `[[ ]]` | Technical debt: quick AI-generated code becomes hard to change | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |
| R12 | `[[ ]]` | `[[YOUR OWN RISK]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | ☐ Open ☐ Closed |

---

# Part 7: Decision Log

*Write down every important choice. Future you (and AI helpers) will not remember WHY you chose something. A decision is "important" if it changes scope, money, data, legal terms, security, pricing, or the plan.*

| # | Date | Stage | Decision (what we chose) | Why (the reason) | Other options we rejected | Decided by | Who was told | Can it be undone? How? |
|---|---|---|---|---|---|---|---|---|
| D1 | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[NAME]]` | `[[ ]]` | `[[ ]]` |
| D2 | | | | | | | | |
| D3 | | | | | | | | |

**Example row:** D1 | 2026-11-02 | Stage 2 | Charge a $4/month subscription after a 14-day free trial | Free users did not show commitment in interviews | Fully free; one-time payment | Maria | Advisor Sam | Yes, can change price for new customers any time |

---

# Part 8: Handover and Continuity

*Goal: if the owner disappears tomorrow, a stranger can keep the product alive using only this section and the links in it.*

## 8.1 The "keys to the kingdom" list **[REQUIRED]**

*Write WHERE each thing is and WHO can access it. NEVER write passwords or keys here.*

| Thing | Where it is / how to find it | Who owns it (name) | Who else has access | Renewal / expiry date |
|---|---|---|---|---|
| Password manager (shared vault) | `[[ ]]` | `[[ ]]` | `[[ ]]` | n/a |
| Domain name | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[DATE]]` |
| Hosting / cloud account | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[DATE]]` |
| Code repository | `[[ ]]` | `[[ ]]` | `[[ ]]` | n/a |
| Database and backups | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[DATE]]` |
| Email sending service | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[DATE]]` |
| Payments account | `[[ ]]` | `[[ ]]` | `[[ ]]` | n/a |
| Apple Developer / Google Play accounts [MOBILE] | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[DATE]]` |
| App signing keys and certificates [MOBILE] | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[DATE]]` |
| Analytics and monitoring | `[[ ]]` | `[[ ]]` | `[[ ]]` | n/a |
| Support inbox and tools | `[[ ]]` | `[[ ]]` | `[[ ]]` | n/a |
| AI tool accounts and billing | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[DATE]]` |
| Social media / community accounts | `[[ ]]` | `[[ ]]` | `[[ ]]` | n/a |
| Business, tax, and legal records | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[DATE]]` |

## 8.2 "If I vanished tomorrow" instructions **[REQUIRED]**

**Q8.2.1: How do you release a new version of the product, step by step?**
**Your answer:** `[[STEPS OR LINK]]`

**Q8.2.2: How do you undo a bad release?**
**Your answer:** `[[STEPS OR LINK]]`

**Q8.2.3: How do you restore from a backup?**
**Your answer:** `[[STEPS OR LINK]]`

**Q8.2.4: What are the recurring jobs that must happen? (renewals, backups check, updates, monthly reports, tax)**

| Job | How often | Who | How |
|---|---|---|---|
| `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |

**Q8.2.5: What are the top 5 things that most often go wrong, and what fixes them?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q8.2.6: Who should a new person call first, second, and third?**
**Your answer:** `[[NAMES AND CONTACTS]]`

## 8.3 Handover test **[REQUIRED before Stage 14 closes]**

- [ ] A person who did NOT build the product followed Part 8 and successfully (a) found every account, (b) did a test release, (c) found the latest backup.
- [ ] Tester name: `[[NAME]]`  Date: `[[DATE]]`
- [ ] Problems they found were fixed in this document.

## 8.4 If the product must be shut down **[OPTIONAL but wise]**

| Question | Your answer |
|---|---|
| How and when will customers be told? | `[[ ]]` |
| How can customers export their data? | `[[ ]]` |
| How is customer data deleted afterwards, and by whom? | `[[ ]]` |
| What happens to paid-up customers (refunds)? | `[[ ]]` |
| Which accounts and domains must be cancelled or kept? | `[[ ]]` |

---

# Part 9: Document Map

*A list of every other document about this project. This helps people (and AI agents) find the truth fast. "Single source of truth" = one place where the official answer lives.*

| Document | Link / location | Owner | Last updated | Status |
|---|---|---|---|---|
| Product requirements (PRD) | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Design files and brand guide | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Architecture and technical decisions | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| AI instructions file (`AGENTS.md` / `CLAUDE.md`) | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Test plan and results | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Security checklist and review | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Privacy Policy and Terms of Service | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Launch plan and launch log | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Runbook (how to operate and fix) | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Customer support guide and FAQ | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Metrics dashboard | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Customer interview notes | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| AI action log | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| Budget and cost tracker | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |
| `[[OTHER]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Draft ☐ Approved |

**Link check:**
- [ ] Every link above opens (checked on `[[DATE]]`).
- [ ] If two documents disagree, we know which one wins: `[[NAME THE ONE]]`.

---

# Part 10: Lessons Learned

*Do a short version after every stage (3 minutes) and a full version at the end. Be honest and kind. The goal is to make the NEXT project easier, not to blame anyone.*

## 10.1 Quick lesson after each stage **[REQUIRED]**

| Stage | One thing that went well | One thing that went badly | One thing I will do differently |
|---|---|---|---|
| 1 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 2 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 3 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 4 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 5 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 6 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 7 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 8 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 9 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 10 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 11 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 12 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 13 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| 14 | `[[ ]]` | `[[ ]]` | `[[ ]]` |

## 10.2 Final reflection **[REQUIRED at Stage 14]**

**Q10.2.1: What are the 3 biggest things you would do the same way next time?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.2.2: What are the 3 biggest things you would do differently?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.2.3: What did AI do really well, and where did it need the most human help or correction?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.2.4: Which rules in Part 3 (AI Workflow) should be changed for the next project?**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.2.5: Which parts of THIS TEMPLATE were confusing, missing, or unnecessary? (Send this back to the template owner.)**
**Your answer:** `[[YOUR ANSWER HERE]]`

**Q10.2.6: Which reusable things came out of this project? (checklists, code, prompts, designs, scripts) Where are they saved for the next project?**
**Your answer:** `[[YOUR ANSWER HERE]]`

---

# Part 11: Final Sign-off

## 11.1 Completeness check **[REQUIRED]**

- [ ] Search this file for `[[`. **None remain** (or each remaining one says `N/A - because ...`).
- [ ] Every stage in Part 4 shows Status = Done, Skipped (with reason), or Cancelled (with reason).
- [ ] Every stage gate has all boxes ticked, or each unticked box has a reason in the Decision Log.
- [ ] Parts 5-10 are filled in.
- [ ] No passwords, keys, or personal customer data were written in this file.
- [ ] The Version History (Part 0.2) is up to date.

## 11.2 Sign-off

| Role | Name | Date | Notes |
|---|---|---|---|
| Project owner | `[[NAME]]` | `[[DATE]]` | `[[ ]]` |
| Backup owner (read and understood Part 8) | `[[NAME]]` | `[[DATE]]` | `[[ ]]` |
| Independent reader (answered the 5 questions at the top using only this file) | `[[NAME]]` | `[[DATE]]` | `[[ ]]` |

**Final status:** ☐ Completed: 500 customers reached  ☐ Completed: changed direction  ☐ Paused  ☐ Shut down

---

# Appendix A: Glossary

| Word | Simple meaning |
|---|---|
| **AI agent** | An AI helper with one specific job, working under human rules. |
| **Accountable / Owner** | The ONE person who answers for the result. |
| **Activation / Aha moment** | The first time a new user feels the product's value. |
| **API** | A way for two computer programs to talk to each other. |
| **Architecture** | The plan for how the parts of the product fit together. |
| **Backup** | A safe copy of your data you can restore if something is lost. |
| **Beta** | A trial version for a small friendly group before the public launch. |
| **Branch** | A separate copy of the code to work on safely without breaking the main version. |
| **Bug** | A mistake that makes the product behave wrongly. |
| **Churn** | Customers who stop using or paying. |
| **Context Pack** | The set of files an AI must read before it works. |
| **Decision Log** | A diary of important choices and the reasons for them. |
| **Definition of Done** | The checklist that says a task is really finished. |
| **Environment** | A separate place where the product runs (development, staging, production). |
| **Gate** | A checklist you must pass before moving to the next stage. |
| **GO / NO-GO** | The final yes/no decision before launch. |
| **MVP** | Minimum Viable Product: the smallest version that is still useful. |
| **Metric** | A number that shows how things are going. |
| **Pull request** | A request to add changes to the main code, which lets others review them first. |
| **Production** | The real, live product that customers use. |
| **Staging** | A practice copy of production used for final testing. |
| **Retention** | How many customers keep coming back. |
| **Rollback** | Going back to the previous working version. |
| **Runbook** | Step-by-step instructions for running and fixing the product. |
| **Scope creep** | Slowly adding extra features until the project never finishes. |
| **Secret** | A password, key, or token that must never be shared or written in documents. |
| **2FA** | Two-step login: a password plus a second proof such as a phone code. |

---

# Appendix B: A Filled-In Example

*This is what ONE small piece looks like when filled in well. Use it for style only.*

### Stage 7: Testing and Quality Assurance (EXAMPLE, project "PlantPal")

| Stage Card | |
|---|---|
| Owner | Maria Lopez |
| Backup | Sam Patel |
| Status | ☑ In progress |
| Start / Target end / Actual end | 2027-01-10 / 2027-01-24 / (not yet) |
| AI helpers | Test Agent (runs the regression tests every night) |
| Blocked because | n/a |

**Q7.4 Bug levels:** Blocker = app crashes on open; Major = reminders do not fire; Minor = icon slightly blurry.

**Q7.5 Accepted bugs at launch:** Blockers: 0, Majors: 0, Minors: 5 (listed in `bugs/minor.md`).

**Done when (Gate):**
- [x] Every must-have feature passed its pass/fail test from Stage 2.
- [x] The full journey works on all promised devices.
- [ ] Zero open Blocker and Major bugs. *(Blocked because: 1 Major bug, reminders late on Android 12. Fix due 2027-01-17. Sam checks.)*

**Why this is good:** It has one owner, a named backup, a clear status, a reason for the one unticked box, a date, and a person to check.

---

# Appendix C: Common Mistakes

| Mistake | Why it hurts | What to do instead |
|---|---|---|
| Writing "the team" as the owner | Nobody feels responsible | Write ONE person's name |
| Leaving `[[ ]]` marks | The document looks finished but is not | Search for `[[` before sign-off |
| Ticking boxes "to be done with it" | You launch with hidden problems | Tick only what you actually verified |
| Skipping Stage 8 (Security/Legal) | Fines, store rejection, lost trust | Do the minimum checklist even for small products |
| Letting AI work directly on production | One wrong command can hurt real customers | Follow Part 3.5 rules; humans approve production changes |
| Writing passwords in this file | Anyone with the file has your keys | Write WHERE the secret is stored, not the secret |
| Changing the definition of "customer" mid-way | Your 500 number becomes meaningless | Decide in Part 5.1 and log any change |
| Building everything before talking to anyone | Months wasted on something nobody wants | Finish Stage 1 and Stage 9 properly |
| Chasing percentages with very few customers | Small numbers swing wildly | Talk to people; use numbers more as you grow |
| Not naming a backup | Everything stops when one person is away | Fill Part 2 and Part 8 completely |
| Never updating this file | It becomes a fairy tale | Update at every stage and every big decision |
| Adding features during testing | The launch date slips forever | Add them to the "later" list in Stage 2 |

---

*End of template. Template version 1.0.0. If you found anything confusing, write it in Part 10.2.5 so the template can be improved for every future project.*
