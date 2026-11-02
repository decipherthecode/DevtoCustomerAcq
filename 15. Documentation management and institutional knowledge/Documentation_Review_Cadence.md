# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**File name:** `Documentation_Review_Cadence.md`
**Folder:** `Documentation Management and Institutional Knowledge/`
**Template version:** 1.0
**Covers:** the full AI-Driven Development Life Cycle, from first idea to the day your **500th customer** is using the product.

---

## What is this document?

This document answers one question:

> **"How often do we check our documents, who checks them, what do they look for, and what do we do when something is wrong?"**

You fill it in **once per project**, then follow it. Keep it up to date as the project grows.

## Who can fill it in?

Anyone. If you can read a question and type an answer, you can complete it. No technical knowledge is needed. Every question comes with a plain-English reason and an example.

## How long will it take?

| Your situation | Time needed |
|---|---|
| First time, brand-new project | 60 to 90 minutes |
| Copying from an earlier project and changing details | 20 to 30 minutes |

## The 7 rules for filling it in

1. **Work top to bottom.** Later parts depend on earlier answers.
2. **Look for `YOUR ANSWER:`.** Type your answer on that line, or fill the blank table cells. Delete nothing else.
3. **Read the example before answering.** Examples start with `Example:`. Copy the style, not the words.
4. **Never leave a blank.** If you do not know yet, write `TBD - decide by YYYY-MM-DD`. A blank forces the next person to guess. `TBD` with a date does not.
5. **Use real names and real dates.** Write `Priya, 2026-11-03`, not `soon` or `the team`.
6. **Tick boxes by changing `[ ]` to `[x]`.**
7. **Do not paste secrets.** Never write passwords, API keys, tokens, customer personal data, or private links in this file. Write where they are stored instead (for example: "stored in the password manager, vault: Company").

## Symbols used in this document

| Symbol | Meaning |
|---|---|
| `YOUR ANSWER:` | You must type something here |
| `[ ]` / `[x]` | Not done / Done |
| `Example:` | A sample answer. Do not leave it in your final file |
| `TBD` | Not decided yet. Must include a date |
| **REQUIRED** | Cannot be skipped |
| *Optional* | Skip only if it truly does not apply. Write `N/A - reason` |

## The finished-file test

You are done when:

- [ ] Every `YOUR ANSWER:` line has a real answer, `TBD - decide by <date>`, or `N/A - <reason>`.
- [ ] Every `Example:` line has been deleted or replaced.
- [ ] A stranger could run the review process from this file alone **without asking you anything**.

If the stranger would have to guess, the template is not finished. Go to **Part 17** for the final check.

## Table of contents

- Part 1: Project identity
- Part 2: What documents exist (inventory)
- Part 3: Who does what (roles)
- Part 4: What "good" means (quality bar)
- Part 5: The seven lifecycle phases
- Part 6: The calendar rhythm (weekly, monthly, quarterly)
- Part 7: Review triggers (extra reviews)
- Part 8: Using AI agents in reviews
- Part 9: First 500 customers tracker
- Part 10: Step-by-step review procedure
- Part 11: Checklists per document type
- Part 12: Review log
- Part 13: Documentation problems list (doc debt)
- Part 14: Health scorecard (metrics)
- Part 15: Exceptions, escalation, archiving
- Part 16: Security and privacy rules
- Part 17: Final sign-off
- Appendix A: Worked example (filled-in sample)
- Appendix B: Glossary
- Appendix C: Ready-to-use AI agent prompts
- Appendix D: One-page quick reference
- Appendix E: Template change log

---

# PART 1: PROJECT IDENTITY

**Why we ask:** Everything else in this file refers back to these answers. Fill this part first.

### 1.1 Project name **REQUIRED**
What is the product or project called?
Example: `PlantPal`

YOUR ANSWER:

### 1.2 One-sentence description **REQUIRED**
Finish this sentence: "This product helps ______ to ______."
Example: `This product helps busy people remember to water their houseplants.`

YOUR ANSWER:

### 1.3 Project owner **REQUIRED**
Who is responsible for this document and the reviews? (One person only.)
Example: `Priya Shah`

YOUR ANSWER:

### 1.4 Contact for questions **REQUIRED**
How can someone reach the owner? Use a work email or chat handle, not a personal phone number.
Example: `priya@example.com`

YOUR ANSWER:

### 1.5 Project start date **REQUIRED**
When did (or will) work begin? Use `YYYY-MM-DD`.

YOUR ANSWER:

### 1.6 Target launch date **REQUIRED**
When do you plan to open the product to the public? If unknown: `TBD - decide by <date>`.

YOUR ANSWER:

### 1.7 Where documents live **REQUIRED**
List every place your documents are stored. Be specific.

| Place | What is kept there | Link or path |
|---|---|---|
| Example: Git repository | Code docs, README, ADRs | `github.com/org/plantpal` |
| | | |
| | | |
| | | |

### 1.8 Where this file lives **REQUIRED**
Full path to this file. A reviewer must be able to find it in under one minute.

YOUR ANSWER:

### 1.9 Today's status **REQUIRED**
Which phase are you in right now? (You will define phases in Part 5.)

- [ ] Phase 1: Discover
- [ ] Phase 2: Plan
- [ ] Phase 3: Build
- [ ] Phase 4: Test
- [ ] Phase 5: Launch
- [ ] Phase 6: Early Users (customers 1 to 100)
- [ ] Phase 7: Growth to 500 (customers 101 to 500)

### 1.10 Who is this file for?
Tick everyone who will read it.

- [ ] Me (solo founder)
- [ ] A future teammate
- [ ] A freelancer or contractor
- [ ] An AI agent
- [ ] An investor or auditor
- [ ] Other: __________

---

# PART 2: WHAT DOCUMENTS EXIST (INVENTORY)

**Why we ask:** You cannot review what you have not listed. This is your master list. Every document in this table gets reviewed under this plan.

### 2.1 How to fill the inventory

For each document, write one row. Use the lists below as prompts. If a document type does not apply, write `N/A - reason` in the first row of that table.

**Column guide**

| Column | What to write |
|---|---|
| **ID** | A short code: PRD-01, TECH-01, AI-01, CUST-01. Numbers go up by one |
| **Document name** | The real file name or title |
| **Location** | Link or path |
| **Owner** | One person |
| **Importance** | **H** = product breaks or customers are hurt if wrong. **M** = causes confusion or delay. **L** = nice to have |
| **Change speed** | **Fast** = changes weekly. **Medium** = monthly. **Slow** = rarely |
| **Review rhythm** | Weekly, Monthly, or Quarterly (see Part 6). Rule: High + Fast = Weekly. High + Slow = Monthly. Medium = Monthly or Quarterly. Low = Quarterly |
| **Last reviewed** | `YYYY-MM-DD`, or `Never` |

### 2.2 Product documents
Think: what are we building, for whom, and why?
Examples: product vision, product requirements (PRD), user personas, user stories, roadmap, pricing notes, launch plan, competitor notes, success metrics.

| ID | Document name | Location | Owner | Importance (H/M/L) | Change speed | Review rhythm | Last reviewed |
|---|---|---|---|---|---|---|---|
| PRD-01 | | | | | | | |
| PRD-02 | | | | | | | |
| PRD-03 | | | | | | | |
| PRD-04 | | | | | | | |
| PRD-05 | | | | | | | |

### 2.3 Technical documents
Think: how is it built, run, and fixed?
Examples: README, setup guide, architecture overview, API reference, database schema, decision records (ADRs), deployment steps, runbooks, incident playbook, backup and restore guide, dependency list, environment variable list (names only, never values).

| ID | Document name | Location | Owner | Importance (H/M/L) | Change speed | Review rhythm | Last reviewed |
|---|---|---|---|---|---|---|---|
| TECH-01 | | | | | | | |
| TECH-02 | | | | | | | |
| TECH-03 | | | | | | | |
| TECH-04 | | | | | | | |
| TECH-05 | | | | | | | |

### 2.4 AI-agent documents
Think: what instructions, rules, and knowledge do the AI agents use?
Examples: system prompts, agent instruction files, skill files, tool lists and permissions, evaluation test sets, guardrail rules, model and version notes, memory or knowledge-base files, prompt change history, known-failures list.

| ID | Document name | Location | Owner | Importance (H/M/L) | Change speed | Review rhythm | Last reviewed |
|---|---|---|---|---|---|---|---|
| AI-01 | | | | | | | |
| AI-02 | | | | | | | |
| AI-03 | | | | | | | |
| AI-04 | | | | | | | |
| AI-05 | | | | | | | |

### 2.5 Customer-facing documents
Think: what do customers read?
Examples: help center articles, getting-started guide, FAQ, release notes, terms of service, privacy policy, support reply templates, onboarding emails, status-page messages, pricing page text.

| ID | Document name | Location | Owner | Importance (H/M/L) | Change speed | Review rhythm | Last reviewed |
|---|---|---|---|---|---|---|---|
| CUST-01 | | | | | | | |
| CUST-02 | | | | | | | |
| CUST-03 | | | | | | | |
| CUST-04 | | | | | | | |
| CUST-05 | | | | | | | |

### 2.6 Legal documents need extra care
Terms, privacy policy, and any contract text must be reviewed by a qualified legal professional before launch. This template does not replace legal advice.

- Who will review legal documents? YOUR ANSWER:
- Date legal review is planned: YOUR ANSWER:

### 2.7 Missing documents
List documents you know you **should** have but do not yet. These go to the Part 13 problems list.

YOUR ANSWER:

### 2.8 Inventory check
- [ ] Every document in all four tables has an owner.
- [ ] Every document has a review rhythm.
- [ ] Every High-importance document is reviewed at least monthly.
- [ ] I counted the documents. Total: ____

---

# PART 3: WHO DOES WHAT (ROLES)

**Why we ask:** Reviews fail when nobody knows whose job they are. This template assumes you may be working **alone**. When you are alone, you still wear different "hats". Wearing a hat means you act in that role for a moment, then switch.

### 3.1 The five hats

| Hat | What this hat does | Who wears it |
|---|---|---|
| **Owner** | Decides what must be documented and keeps the plan alive | |
| **Author** | Writes and edits documents | |
| **Reviewer** | Checks a document against the quality bar (Part 4) | |
| **Approver** | Says "this is good to publish" | |
| **AI Assistant** | Drafts, checks, and suggests (never approves). See Part 8 | |

Example: `Owner = Priya, Author = Priya + AI Assistant, Reviewer = Priya (next-day fresh eyes), Approver = Priya`

### 3.2 Solo-founder safety rule **REQUIRED**
If you are both Author and Reviewer, you miss your own mistakes. Pick **at least one** safeguard:

- [ ] **Wait 24 hours** between writing and reviewing.
- [ ] **Read it out loud** during review.
- [ ] **Ask an AI agent** to review it first (Part 8), then you decide.
- [ ] **Ask a friend or advisor** to review High-importance documents.
- [ ] **Read it as a beginner**: pretend you know nothing about the product.

YOUR ANSWER (which ones will you actually do?):

### 3.3 Backup person
If you are away for two weeks, who runs the reviews? A name, or `Nobody - reviews pause and the pause is logged in Part 12`.

YOUR ANSWER:

### 3.4 When the team grows
Write who joins and when. Update the table in 3.1 the day they start.

| New person or role | Start date | Hat they take |
|---|---|---|
| | | |
| | | |

---

# PART 4: WHAT "GOOD" MEANS (QUALITY BAR)

**Why we ask:** A review without a definition of "good" is just opinion. A document **passes review** only if it passes all four tests below.

### 4.1 The four tests

| # | Test | The question a reviewer asks | Pass means |
|---|---|---|---|
| 1 | **Accurate** | Does this match how the product, code, and process work **today**? | Every fact, step, number, and screenshot is still true |
| 2 | **Complete** | Is anything missing? | No empty sections, no `TBD` past its date, owner, date, and links all present |
| 3 | **Understandable** | Could a new person or AI agent follow this **without guessing**? | Plain words, steps in order, terms explained, one idea per sentence |
| 4 | **Findable and Safe** | Is it in the right place with a clear name, and free of secrets? | Correct folder, clear title, no passwords, keys, or private customer data |

### 4.2 Scoring a document
Give each test a score of 0, 1, or 2.

| Score | Meaning |
|---|---|
| 2 | Fully passes |
| 1 | Small problem. Fix within the time limit in 4.3 |
| 0 | Fails. Document is marked **Needs Fix** and must not be relied on until fixed |

**Overall result**

| Total (of 8) | Result |
|---|---|
| 8 | **Pass** |
| 6 to 7 | **Pass with fixes** (log fixes in Part 13) |
| 0 to 5, or any single 0 | **Fail** (fix, then re-review) |

### 4.3 Fix deadlines **REQUIRED**
How fast must problems be fixed? Suggested defaults are shown. Change them if needed.

| Problem size | Suggested deadline | YOUR deadline |
|---|---|---|
| Wrong information that could hurt customers or break the product (Critical) | Same day | |
| Wrong or missing information that causes confusion (Major) | 7 days | |
| Small wording or formatting issue (Minor) | 30 days | |

### 4.4 Your own writing rules
Tick the rules you will follow. Add more at the bottom.

- [ ] Every document has an **owner**, a **last reviewed** date, and a **next review** date at the top.
- [ ] Use short sentences. Aim for under 25 words.
- [ ] Explain each special word the first time it appears, or link to the glossary.
- [ ] Number steps in the order they happen.
- [ ] Say what the reader will **have** or **know** when they finish.
- [ ] Use the same name for the same thing everywhere.
- [ ] Use descriptive link text, not "click here".
- [ ] Add alt text to images, and do not put text only inside images.
- [ ] Write dates as `YYYY-MM-DD`.
- [ ] Never use "soon", "recently", "currently" without a date.

Extra rules: YOUR ANSWER:

### 4.5 Document header standard **REQUIRED**
Every document in the inventory should start with this block. Copy it.

```
Owner:            <name>
Status:           Draft | In Review | Approved | Needs Fix | Archived
Last reviewed:    YYYY-MM-DD
Next review due:  YYYY-MM-DD
Applies to:       <product version, phase, or date range>
Related docs:     <links>
```

- [ ] I will add this header to all documents in the inventory by this date: YOUR ANSWER:

---

# PART 5: THE SEVEN LIFECYCLE PHASES

**Why we ask:** Different phases need different documents and different review speed. A document that is fine in Phase 2 can be dangerously wrong in Phase 6. In each phase you will say **what must be written**, **what must be reviewed**, and **what must be true before moving on** (the "exit gate").

**How to read each phase**

- **Goal:** Why this phase exists.
- **Documents that must exist by the end:** Your minimum.
- **Review speed in this phase:** How often to review.
- **Exit gate:** Tick every box before moving to the next phase.

Fill in the planned dates now. Update actual dates when you finish.

| Phase | Planned start | Planned end | Actual end |
|---|---|---|---|
| 1. Discover | | | |
| 2. Plan | | | |
| 3. Build | | | |
| 4. Test | | | |
| 5. Launch | | | |
| 6. Early Users (1-100) | | | |
| 7. Growth to 500 (101-500) | | | |

---

## PHASE 1: DISCOVER

**Goal:** Learn whether the problem is real and worth solving.

**Documents that must exist by the end**

- [ ] Problem statement (who has the problem, how bad, what they do today)
- [ ] Target customer description
- [ ] Competitor and alternatives notes
- [ ] Early success idea (how you will know it works)
- [ ] Assumptions list (things you believe but have not proven)

**Review speed in this phase:** Monthly (documents change fast but stakes are low).

**Questions**

1.1 Who exactly has this problem? (One sentence, a real kind of person.)
YOUR ANSWER:

1.2 How will you check that the problem is real? (Talk to people, survey, research.)
YOUR ANSWER:

1.3 What are your 3 biggest assumptions?
YOUR ANSWER:

**Review checklist**
- [ ] Problem statement still matches what I learned from real people.
- [ ] Each assumption is marked **Proven**, **Disproven**, or **Still unknown**.
- [ ] Sources are linked, not just remembered.

**Exit gate**
- [ ] I can explain the problem and customer in two sentences.
- [ ] Every Phase 1 document has an owner and a date.
- [ ] I decided **go** or **stop**, and wrote the reason. Decision and reason: YOUR ANSWER:

---

## PHASE 2: PLAN

**Goal:** Decide exactly what to build first, and how.

**Documents that must exist by the end**

- [ ] Product requirements (what the first version must do, and must not do)
- [ ] User stories or use cases with "done when" rules
- [ ] Roadmap (what comes first, next, later)
- [ ] High-level architecture sketch and technology choices, with reasons
- [ ] AI-agent plan: which tasks AI agents do, which tools they may use, what they must never do
- [ ] Risks list (what could go wrong, and what you will do about it)
- [ ] Launch plan draft (including "first 500 customers" goal, see Part 9)
- [ ] Privacy and data plan (what customer data you collect, why, where it is stored)

**Review speed in this phase:** Monthly, plus a full review before Build begins.

**Questions**

2.1 What is the smallest useful first version? List its features.
YOUR ANSWER:

2.2 What is **not** in the first version? (Writing this prevents scope creep.)
YOUR ANSWER:

2.3 Which technical decisions are hard to undo, and where are they recorded?
YOUR ANSWER:

2.4 What data will the product collect about customers, and why is each item needed?
YOUR ANSWER:

**Review checklist**
- [ ] Every requirement can be tested (someone can say pass or fail).
- [ ] Requirements, roadmap, and architecture do not contradict each other.
- [ ] Every major decision lists the options considered and the reason for the choice.
- [ ] Risks have an owner and a next step.

**Exit gate**
- [ ] A new person could build the first version from these documents without asking you questions.
- [ ] Scope, budget, and date are written down.
- [ ] Legal and privacy needs have been identified (not necessarily finished).

---

## PHASE 3: BUILD

**Goal:** Create the product. Documents must keep up with the code and the AI agents.

**Documents that must exist by the end**

- [ ] README with setup steps that work on a clean computer
- [ ] Architecture overview (updated to match what was actually built)
- [ ] API reference or interface description (if any)
- [ ] Decision records for changes made during the build
- [ ] AI-agent instruction files, prompts, and tool permissions
- [ ] AI evaluation set (example inputs and the answers you expect)
- [ ] Environment and configuration guide (variable **names** and purpose only)
- [ ] Deployment and rollback steps (draft)
- [ ] Draft help articles and onboarding flow text

**Review speed in this phase:** **Weekly** for fast-changing documents (setup, API, AI prompts). Monthly for the rest.

**Questions**

3.1 Which documents change every time code changes?
YOUR ANSWER:

3.2 How will you notice when a document becomes outdated? (Example: a reminder on every release.)
YOUR ANSWER:

3.3 Which AI-agent files must be re-checked whenever a prompt, tool, or model changes?
YOUR ANSWER:

**Review checklist**
- [ ] I followed the README on a clean setup, and it worked **exactly** as written.
- [ ] Architecture documents match the real code and services.
- [ ] Every AI-agent file shows the model name and version it was written for.
- [ ] Every API example still runs.
- [ ] No secrets appear in any document, example, or screenshot.

**Exit gate**
- [ ] Documents match the build that is about to be tested.
- [ ] Every Critical or Major problem in Part 13 for these documents is fixed.

---

## PHASE 4: TEST

**Goal:** Prove the product and its documents work before real customers see them.

**Documents that must exist by the end**

- [ ] Test plan and test results summary
- [ ] AI evaluation results (what passed, what failed, what you changed)
- [ ] Known issues list
- [ ] Final help center articles, FAQ, and onboarding guide
- [ ] Support reply templates
- [ ] Incident playbook (what to do when something breaks)
- [ ] Backup and restore guide, tested at least once
- [ ] Security and privacy review notes
- [ ] Terms of service and privacy policy (legally reviewed)

**Review speed in this phase:** Weekly for all High-importance documents.

**Questions**

4.1 Who outside the project (friend, tester, beta user) will follow the customer documents and report where they got stuck?
YOUR ANSWER:

4.2 How will you test the incident playbook before you need it?
YOUR ANSWER:

**Review checklist**
- [ ] A person who has never seen the product completed the getting-started guide alone.
- [ ] Every place the tester got stuck is fixed in the document or logged in Part 13.
- [ ] Restore from backup was tried, and the document says how long it took.
- [ ] The AI evaluation set passes at or above the level you wrote down. Required pass level: YOUR ANSWER:

**Exit gate**
- [ ] No Critical documentation problems are open.
- [ ] Customer-facing documents are approved by the Approver.
- [ ] A **pre-launch full review** (Part 6.4) is complete.

---

## PHASE 5: LAUNCH

**Goal:** Release to the public safely, and keep every document correct during the busiest time.

**Documents that must exist by the end**

- [ ] Launch checklist
- [ ] Rollback plan
- [ ] Status page text for outages
- [ ] Release notes for version 1
- [ ] Support contact and escalation steps
- [ ] Launch-day roles ("who does what if something goes wrong")

**Review speed in this phase:** **Daily quick check** for 7 days around launch (see 6.5). Then weekly.

**Questions**

5.1 What is the exact launch date and time?
YOUR ANSWER:

5.2 Who checks documents on launch day, and what will they check?
YOUR ANSWER:

5.3 How will you hear when a customer is confused by a document?
YOUR ANSWER:

**Review checklist**
- [ ] All links in customer-facing documents work.
- [ ] Release notes match what was actually released.
- [ ] Pricing, limits, and promises match the product and the terms.
- [ ] The rollback plan was read out loud by the person who would run it.

**Exit gate**
- [ ] The product is live.
- [ ] Day 1, Day 3, and Day 7 reviews are logged in Part 12.
- [ ] Customer 1 is recorded in Part 9.

---

## PHASE 6: EARLY USERS (CUSTOMERS 1 TO 100)

**Goal:** Learn from real use. Documents change fastest here because real customers find real gaps.

**Documents that must exist by the end**

- [ ] FAQ built from real questions (not guesses)
- [ ] Updated help articles for the top 10 support topics
- [ ] Release notes for every release
- [ ] Customer feedback summary
- [ ] Updated onboarding guide
- [ ] Updated AI-agent files based on real failures
- [ ] Updated known-issues list

**Review speed in this phase:** **Weekly** for customer-facing and AI-agent documents. Monthly for the rest.

**Questions**

6.1 Where do customers ask questions? (Email, chat, social, support form.)
YOUR ANSWER:

6.2 Who reads those questions every week, and where are patterns written down?
YOUR ANSWER:

6.3 What rule will you use to turn a repeated question into a document fix? (Example: any question asked 3 times becomes a help article.)
YOUR ANSWER:

**Review checklist**
- [ ] The top 10 support questions are each answered in a document.
- [ ] Documents use the same words customers use.
- [ ] Any AI answers that were wrong are traced to a document or prompt and fixed.
- [ ] The first 10, 50, and 100 customer milestone reviews (Part 9) are done.

**Exit gate**
- [ ] 100 customers reached.
- [ ] Documentation problems from the last 30 days are fixed or scheduled.
- [ ] Support questions about "how do I...?" are falling, or you wrote why not.

---

## PHASE 7: GROWTH TO 500 (CUSTOMERS 101 TO 500)

**Goal:** Make the product and documents work for people who are **not** like your first 100 customers, and prepare to run without constant founder effort.

**Documents that must exist by the end**

- [ ] Self-serve help center covering the top 25 questions
- [ ] Documented support and escalation process
- [ ] Onboarding guide split by customer type (if you have more than one type)
- [ ] Runbooks for the top failures
- [ ] A hand-off guide: "If someone new takes over this product, read this first"
- [ ] Quarterly audit report (Part 6.3) for at least one quarter
- [ ] Lessons learned document

**Review speed in this phase:** Weekly quick check, monthly full review, quarterly deep audit.

**Questions**

7.1 What differs between customers 1-100 and 101-500? (Different needs, skills, countries, languages.)
YOUR ANSWER:

7.2 Which documents still depend on your memory instead of being written down?
YOUR ANSWER:

7.3 What would a new teammate need on day 1 that is not written yet?
YOUR ANSWER:

**Review checklist**
- [ ] Every document is still accurate for the **current** product version.
- [ ] Old documents are archived (Part 15.3), not left to confuse people.
- [ ] Support questions are answered by documents at least as often as by you personally.
- [ ] Customers can find the right document in under one minute.

**Exit gate**
- [ ] 500 customers are using the product.
- [ ] Final lessons-learned review is written (Part 9.5).
- [ ] This file's next step is decided: keep as is, or change to a bigger-company process. Decision: YOUR ANSWER:

---

# PART 6: THE CALENDAR RHYTHM

**Why we ask:** A calendar makes reviews happen even when nothing is going wrong. Reviews that wait for "when I have time" do not happen.

### 6.1 Weekly quick check (about 30 minutes)

**Which documents:** Every document with rhythm = **Weekly** in Part 2.

**When:** Day and time of the week. YOUR ANSWER:

**Where it is recorded:** Part 12 (one row per week).

**Checklist for each document**
- [ ] Does anything in this document describe something we changed this week?
- [ ] Are the steps still correct? (Try one.)
- [ ] Any broken links, screenshots, or version numbers?
- [ ] Any new customer question that this document should answer?
- [ ] Any AI answer this week that was wrong because of this document?
- [ ] Update **Last reviewed** and **Next review due** in the document header.

**Time limit:** If a fix takes more than 15 minutes, log it in Part 13 and move on.

### 6.2 Monthly full review (about 2 to 3 hours)

**Which documents:** Every document with rhythm = **Monthly** or **Weekly** in Part 2.

**When:** Day of the month. Example: "first Monday". YOUR ANSWER:

**Checklist**
- [ ] Run the four-test score (Part 4) on every document in scope.
- [ ] Review the problems list (Part 13). Close fixed items, re-rank open items.
- [ ] Check that every document still has an owner.
- [ ] Look for documents that contradict each other.
- [ ] Look for missing documents (anything you explained out loud this month should maybe be written).
- [ ] Update the scorecard (Part 14).
- [ ] Check the customer milestone tracker (Part 9).
- [ ] Update Part 2 (add new documents, retire old ones).

### 6.3 Quarterly deep audit (about half a day)

**Which documents:** **Everything** in the inventory.

**When:** Months. Example: "January, April, July, October". YOUR ANSWER:

**Checklist**
- [ ] Open every document. Do not trust the date in the header. Re-test the facts.
- [ ] Is each document still needed? If not, archive it (Part 15.3).
- [ ] Do names, folders, and links still make sense?
- [ ] Do all four document groups (product, technical, AI-agent, customer) agree with each other?
- [ ] Review AI-agent files against the current model, tools, and policies (Part 8).
- [ ] Review security and privacy (Part 16).
- [ ] Review this file. Does the cadence still match reality? Update it.
- [ ] Write a short audit summary: what improved, what got worse, what to do next quarter.

Audit summary location: YOUR ANSWER:

### 6.4 Pre-launch full review (one time, in Phase 4)
Same as the quarterly deep audit, plus:
- [ ] A person who has not seen the product follows the customer documents without help.
- [ ] Legal documents have been reviewed (Part 2.6).
- [ ] All Critical and Major problems in Part 13 are closed.

### 6.5 Launch week daily check (Phase 5, 7 days)
Each day, 10 minutes:
- [ ] Any customer-facing document wrong, confusing, or missing something that someone asked about?
- [ ] Any status or release note that no longer matches reality?
- [ ] Log in Part 12.

### 6.6 Review rhythm adjustment rules
You may change a rhythm. Write the reason in Part 12.

| If this happens... | Then do this |
|---|---|
| A document fails review twice in a row | Move it **one step faster** (Quarterly to Monthly, Monthly to Weekly) |
| A document passes with a full score three times in a row | Move it **one step slower**, but **never** slower than Quarterly for High importance |
| The product enters a new phase | Re-check every rhythm against that phase's "Review speed" |

### 6.7 My calendar **REQUIRED**
Put these in your real calendar. Tick when done.

- [ ] Weekly check added as a repeating event.
- [ ] Monthly review added as a repeating event.
- [ ] Quarterly audit added as a repeating event.
- [ ] Reminder set: "update document header after every release".

Calendar app or tool used: YOUR ANSWER:

### 6.8 Summary table (copy your answers here)

| Review | Day and time | Length | Documents in scope | Recorded in |
|---|---|---|---|---|
| Weekly quick check | | 30 min | Rhythm = Weekly | Part 12 |
| Monthly full review | | 2-3 hours | Rhythm = Monthly or faster | Part 12 |
| Quarterly deep audit | | Half day | All | Part 12 |

---

# PART 7: REVIEW TRIGGERS (EXTRA REVIEWS)

**Why we ask:** Some events make documents wrong **immediately**. Waiting for the calendar is too late. A **trigger** is an event that starts an extra review right away.

### 7.1 The four standard triggers

| Trigger | What starts it | Which documents to check | Do it within |
|---|---|---|---|
| **T1: Release or launch** | A new version, feature, price, or launch milestone goes out (or is about to) | Product, technical, customer-facing, release notes, AI-agent files that use that feature | Before release for customer-facing; within 2 days after for the rest |
| **T2: Bug or incident** | A production problem, outage, data issue, or security event | Runbooks, incident playbook, status text, the document that failed to prevent it | 3 days after the incident is resolved |
| **T3: Customer feedback** | A customer is confused, a support question repeats, a bad review mentions unclear help | The help article, FAQ, onboarding guide, any AI answer involved | 7 days (24 hours if the confusion could cause harm or loss) |
| **T4: AI model or prompt change** | A new model version, prompt edit, tool added or removed, permission changed, guardrail changed | Every AI-agent file, evaluation set, tool list, and any document that describes AI behavior to customers | Before the change goes live; re-check within 2 days after |

Change the times above to what you can really do:

YOUR ANSWER (new deadlines, or "keep defaults"):

### 7.2 Trigger checklists

**T1: Release or launch**
- [ ] List every feature, setting, or price that changed.
- [ ] Search all documents for those names and update each one.
- [ ] Update release notes, version numbers, and screenshots.
- [ ] Update the README or setup guide if steps changed.
- [ ] Update the help center and FAQ.
- [ ] Re-run the AI evaluation set if AI behavior might be affected.
- [ ] Log in Part 12.

**T2: Bug or incident**
- [ ] Write what happened, when, who was affected, and how it was fixed.
- [ ] Ask: "Which document should have prevented or shortened this?" Fix it or create it.
- [ ] Update the runbook with the real steps that worked.
- [ ] Update customer-facing text if customers were told something inaccurate.
- [ ] Add a "lesson learned" line to the problems list (Part 13).
- [ ] Log in Part 12.

**T3: Customer feedback**
- [ ] Copy (without personal details) the question or complaint.
- [ ] Find the document that should have answered it.
- [ ] Decide: wrong, missing, hard to find, or hard to understand?
- [ ] Fix it, then tell the customer if appropriate.
- [ ] If the same issue appears 3 times, mark it as a priority fix.
- [ ] Log in Part 12.

**T4: AI model or prompt change**
- [ ] Write down what changed (model name and version, prompt, tool, permission, guardrail).
- [ ] Update every AI-agent file to show the new model name, version, and date.
- [ ] Re-run the evaluation set. Record before and after results.
- [ ] Read three real or sample AI conversations to see if behavior still matches documentation.
- [ ] Update customer-facing text that describes what the AI can or cannot do.
- [ ] Keep the old prompt or settings in history so you can roll back.
- [ ] Log in Part 12.

### 7.3 Your own triggers (optional)
Add triggers specific to your project (for example: "a new country is added", "a payment provider changes terms").

| Trigger name | What starts it | Documents to check | Do within |
|---|---|---|---|
| | | | |
| | | | |

### 7.4 How you will notice a trigger **REQUIRED**
A trigger you do not notice is useless. How will you know each one happened?

| Trigger | How you will notice |
|---|---|
| T1 Release | Example: release checklist includes "run Part 7 T1 checklist" |
| T2 Incident | |
| T3 Customer feedback | |
| T4 AI change | |

---

# PART 8: USING AI AGENTS IN REVIEWS

**Why we ask:** AI agents are fast at finding stale, missing, or confusing text. They can also make confident mistakes. This part sets the rule: **AI drafts and suggests. A human decides and approves.**

### 8.1 The golden rules

1. **AI never approves.** Only the human Approver sets a document to **Approved**.
2. **AI never gets secrets.** Do not paste passwords, API keys, tokens, or private customer data into any AI tool.
3. **AI must show its evidence.** Every issue it reports must point to the exact document and line, and say what it compared it to.
4. **AI suggestions are checked.** A human verifies at least the High-importance changes by testing the steps or reading the source.
5. **AI changes are labeled.** Mark documents that AI helped write or review in the header or change history.
6. **When AI and reality disagree, reality wins.** Test the product.

### 8.2 What AI may and may not do

| Task | AI may do it? | Human check needed? |
|---|---|---|
| Find broken links and old version numbers | Yes | Spot check |
| Compare a document with the code or another document and list differences | Yes | Yes |
| Suggest clearer wording | Yes | Yes |
| Draft a new document from notes you provide | Yes | Yes (full read) |
| Score a document against the four tests (Part 4) | Yes, as a first pass | Yes. Human gives final score |
| Run the steps in a setup guide in a safe test environment | Yes, if permitted | Yes |
| Decide a document is **Approved** | **No** | N/A |
| Edit legal documents | **No** (suggest only) | Legal professional |
| Change live customer-facing text without review | **No** | N/A |
| Access customer personal data | **No** | N/A |

### 8.3 Your AI review setup **REQUIRED**

8.3.1 Which AI tools or agents will you use for documentation review?
YOUR ANSWER:

8.3.2 What documents may the AI read? (Folders or files.)
YOUR ANSWER:

8.3.3 What documents may the AI **edit**? (Suggested: none directly. It proposes changes.)
YOUR ANSWER:

8.3.4 Where do AI suggestions go before a human sees them? (Example: a "Suggested Changes" file, a comment, a draft branch.)
YOUR ANSWER:

8.3.5 Who reviews AI suggestions, and how fast?
YOUR ANSWER:

### 8.4 When AI runs
Tick when AI should run a first-pass review.

- [ ] Before every weekly quick check
- [ ] Before every monthly review
- [ ] Before every quarterly audit
- [ ] On every trigger (T1 to T4)
- [ ] When I ask

### 8.5 Checking the AI itself
AI reviewers can drift or hallucinate. Each quarter:

- [ ] Give the AI a document with 3 mistakes you planted on purpose. Did it find them?
- [ ] Check three AI-reported issues. Were they real?
- [ ] Check three "no issue" results. Were they truly fine?
- [ ] Write the result in the Part 12 log.

### 8.6 AI-agent documents have special review needs
For every AI-agent file (prompts, instructions, skills, tool lists), the review must also confirm:

- [ ] The model name and version the file was written for is stated.
- [ ] The tools the agent may use are listed, and each one has a purpose.
- [ ] What the agent must **never** do is written plainly.
- [ ] What the agent should do when it is unsure (ask, refuse, hand to a human) is written.
- [ ] Example inputs and the expected outputs exist and still pass.
- [ ] No private data, secrets, or real customer details are in the file.
- [ ] A change history exists (what changed, when, why, who approved).
- [ ] A rollback copy of the previous version exists.

### 8.7 Prompts you can copy
Ready-to-use prompts are in **Appendix C**.

---

# PART 9: FIRST 500 CUSTOMERS TRACKER

**Why we ask:** "500 customers" is your finish line for this template. Milestones tell you **when to look harder** at your documents, because new kinds of customers bring new confusion.

### 9.1 What counts as a "customer"? **REQUIRED**
Write one clear definition. Everyone must count the same way.
Example: `A person who completed sign-up and used the product on at least 2 different days.`

YOUR ANSWER:

### 9.2 How you count **REQUIRED**
Where is the number found, and who updates it?
YOUR ANSWER:

### 9.3 Milestone reviews

When the customer count reaches each number, run the extra review. Tick when done.

| Milestone | Date reached | Extra review to do | Done |
|---|---|---|---|
| **1st customer** | | Read the onboarding guide as that customer. Watch or ask how they got started. Fix the first gaps. | [ ] |
| **10 customers** | | Ask each customer what confused them. Update FAQ and getting-started guide. Check AI answers for wrong or missing info. | [ ] |
| **25 customers** | | Group support questions into themes. Create or fix a help article for each top theme. | [ ] |
| **50 customers** | | Review all customer-facing and AI-agent documents against real conversations. Update known-issues list. | [ ] |
| **100 customers** | | **Full review** (like Part 6.3). Phase 6 exit gate. Decide what should be automated or self-serve. | [ ] |
| **250 customers** | | Check documents against different customer types, devices, countries, and languages. Update runbooks for top failures. | [ ] |
| **400 customers** | | Test the hand-off guide. Could a new person support customers using documents alone? | [ ] |
| **500 customers** | | **Final review**, lessons-learned document, decision about the next process (9.5). | [ ] |

### 9.4 Customer-document health at each milestone
Fill in at each milestone.

| Milestone | Support questions this period | Answered by a document | Unanswered or unclear | Top 3 confusing topics | Docs fixed |
|---|---|---|---|---|---|
| 10 | | | | | |
| 25 | | | | | |
| 50 | | | | | |
| 100 | | | | | |
| 250 | | | | | |
| 500 | | | | | |

### 9.5 Final lessons-learned (at 500)
Answer in plain words.

9.5.1 Which documents saved us the most time?
YOUR ANSWER:

9.5.2 Which documents were wrong most often, and why?
YOUR ANSWER:

9.5.3 What should we have documented earlier?
YOUR ANSWER:

9.5.4 Which review rhythm was too slow or too fast?
YOUR ANSWER:

9.5.5 What do we change in this template for the next project?
YOUR ANSWER:

---

# PART 10: STEP-BY-STEP REVIEW PROCEDURE

**Why we ask:** Use this every time you review one document. It is the same for weekly, monthly, quarterly, and trigger reviews.

### 10.1 The 10 steps

| Step | What to do | Done when |
|---|---|---|
| 1 | **Open the document** and read its header (owner, last reviewed, next review due). | You know who owns it and when it was last checked |
| 2 | **Know why you are reviewing.** Calendar review? Which trigger? | Reason written in the log |
| 3 | **Gather the truth.** Open the product, code, settings, or process the document describes. | The real thing is in front of you |
| 4 | **Read the document slowly, start to finish.** Do not skim. | You read every line |
| 5 | **Test it.** Follow steps, click links, run examples, try commands in a safe place. | Every step was tried, or marked "not testable - reason" |
| 6 | **Score it** with the four tests (Part 4). | You have 4 scores |
| 7 | **Write down problems** with size (Critical, Major, Minor) and fix by date. | Problems are in Part 13 |
| 8 | **Fix quick problems now** (under 15 minutes). | Fixed, or logged |
| 9 | **Update the header:** Last reviewed, Next review due, Status. | Header is correct |
| 10 | **Log the review** in Part 12. | One new row exists |

### 10.2 Who does what in each step
In a solo project, all steps are yours. If the AI Assistant helps, it may do steps 3 to 5 as a first pass, but **you** do steps 6, 9, and approval.

### 10.3 What "Status" means

| Status | Meaning | May customers or agents rely on it? |
|---|---|---|
| Draft | Being written | No |
| In Review | Written, awaiting review | No |
| Approved | Passed review | Yes |
| Needs Fix | Failed review or found wrong | **No**, mark clearly at the top |
| Archived | No longer used | No |

### 10.4 Overdue rule **REQUIRED**
A document is **overdue** when today is later than its Next review due date.

What will you do when something is overdue?
- [ ] Mark it **Needs Fix** until reviewed (strict).
- [ ] Review it within 7 days and log why it was late (flexible).
- [ ] Other: YOUR ANSWER:

---

# PART 11: CHECKLISTS PER DOCUMENT TYPE

**Why we ask:** Different documents break in different ways. Use the matching list **in addition to** the four tests.

### 11.1 Product documents (PRD, roadmap, personas)
- [ ] Goal and customer are stated in the first paragraph.
- [ ] Every requirement is testable (pass/fail).
- [ ] Out-of-scope items are listed.
- [ ] Roadmap dates and priorities match reality.
- [ ] Success measures have numbers and a date.
- [ ] Customer descriptions are based on real people, with sources.
- [ ] Pricing and promises match the customer-facing text.

### 11.2 Technical documents (README, architecture, API, runbooks)
- [ ] Setup steps work on a clean machine, exactly as written.
- [ ] Software versions and system requirements are stated.
- [ ] Commands and code examples run.
- [ ] Diagrams match the real structure.
- [ ] Every decision lists reason, date, and who decided.
- [ ] Runbooks say: what you see, what it means, what to do, who to call, how to confirm it is fixed.
- [ ] Backup and restore were tested, with date and time taken.
- [ ] Environment variables list names and purposes, **not values**.
- [ ] Known limits (rate limits, size limits, supported platforms) are current.

### 11.3 AI-agent documents (prompts, instructions, skills, tools, evals)
- [ ] Model name and version, and date last tested, are stated.
- [ ] Purpose of the agent in one sentence.
- [ ] Allowed tools and permissions listed; forbidden actions listed.
- [ ] Instructions are specific, not vague ("be helpful" is not an instruction).
- [ ] Unsure behavior is defined (ask, refuse, escalate).
- [ ] Examples of good and bad outputs exist.
- [ ] Evaluation set passes at the required level (Part 5, Phase 4).
- [ ] Instructions do not contradict each other or customer-facing promises.
- [ ] No secrets or real personal data.
- [ ] Change history and rollback copy exist.
- [ ] Safety, privacy, and human-handoff rules are present.

### 11.4 Customer-facing documents (help, FAQ, release notes, policies)
- [ ] Written in the customer's words, at about a middle-school reading level.
- [ ] Starts with what the customer wants to do.
- [ ] Steps are numbered, one action each, with expected result.
- [ ] Screenshots match the current product.
- [ ] Links work and go to the right place.
- [ ] Contact or escalation path is shown.
- [ ] Release notes state date, version, what changed, and any action needed.
- [ ] Pricing, limits, refunds, and data promises match terms and the product.
- [ ] Accessible: headings, alt text, readable colors, plain language.
- [ ] Legal text reviewed by a qualified person.

### 11.5 Quick check for any document
- [ ] Right folder and clear name
- [ ] Owner, dates, and status present
- [ ] No "TBD" older than its date
- [ ] No duplicate copy that disagrees with it
- [ ] No secrets

---

# PART 12: REVIEW LOG

**Why we ask:** If it is not logged, it did not happen. One row per review. Newest at the **bottom**.

**Review type codes:** W = Weekly, M = Monthly, Q = Quarterly, T1 = Release, T2 = Incident, T3 = Customer feedback, T4 = AI change, L = Launch week, P = Pre-launch, MS = Customer milestone.

**Result codes:** P = Pass, PF = Pass with fixes, F = Fail.

| Date | Review type | Phase | Document ID(s) | Reviewer | AI used? | Score (of 8) | Result | Problems found (count) | Rhythm changed? | Notes or link |
|---|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |

**Missed reviews.** Missed a review? Write it here instead of hiding it.

| Planned date | Review type | Why missed | Makeup date |
|---|---|---|---|
| | | | |
| | | | |

(Add rows as needed. Copy the last row and keep going.)

---

# PART 13: DOCUMENTATION PROBLEMS LIST (DOC DEBT)

**Why we ask:** Every problem you find but cannot fix right now goes here, so nothing is forgotten.

**Size codes:** C = Critical (could hurt customers or break the product), MJ = Major (causes confusion or delay), MN = Minor (wording or format).
**Status codes:** Open, In progress, Fixed, Won't fix (explain).

| ID | Date found | Document ID | What is wrong (one sentence) | Which test failed (Accurate, Complete, Understandable, Findable/Safe) | Size | Fix by | Owner | Status | Date fixed |
|---|---|---|---|---|---|---|---|---|---|
| P-001 | | | | | | | | | |
| P-002 | | | | | | | | | |
| P-003 | | | | | | | | | |
| P-004 | | | | | | | | | |
| P-005 | | | | | | | | | |
| P-006 | | | | | | | | | |
| P-007 | | | | | | | | | |
| P-008 | | | | | | | | | |

### 13.1 Rules for this list
- Critical problems are fixed before anything else.
- A problem open longer than **twice its deadline** is escalated (Part 15.2).
- "Won't fix" requires a written reason and a date to revisit.
- Review this list at every monthly review.

### 13.2 Missing documents list
Documents that should exist but do not. Create them in priority order.

| Wanted document | Why it is needed | Priority (H/M/L) | Owner | Create by |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

---

# PART 14: HEALTH SCORECARD (METRICS)

**Why we ask:** Numbers show if your documentation is getting better or quietly rotting. Update at every monthly review. Keep it simple.

### 14.1 The scorecard

| Measure | How to calculate | Healthy target | Month 1 | Month 2 | Month 3 | Month 4 | Month 5 | Month 6 |
|---|---|---|---|---|---|---|---|---|
| **On-time reviews** | Reviews done on time / reviews planned | 90% or higher | | | | | | |
| **Overdue documents** | Documents past their review date | 0 for High importance | | | | | | |
| **Average score** | Average of the 8-point scores | 7 or higher | | | | | | |
| **Open Critical problems** | Count in Part 13 | 0 | | | | | | |
| **Open Major problems** | Count in Part 13 | 3 or fewer | | | | | | |
| **Average fix time (days)** | Date fixed minus date found | Within deadlines in 4.3 | | | | | | |
| **Documents with owners** | Documents with an owner / total documents | 100% | | | | | | |
| **Documents with current header** | Documents with all header fields / total | 100% | | | | | | |
| **Questions answered by documents** | Support questions answered by a document / total (Phase 6 and 7) | Rising each month | | | | | | |
| **AI review accuracy** | Real issues the AI found / issues it reported (Part 8.5) | 80% or higher | | | | | | |

Change the targets to what makes sense for you.

YOUR ANSWER (changed targets, if any):

### 14.2 How to read the scorecard

| Sign | Likely meaning | Do this |
|---|---|---|
| On-time reviews falling | Too many reviews, or no time | Lower scope or slow low-importance rhythms. Do not skip High ones |
| Many overdue High documents | The plan is too heavy | Move rhythms, ask for help, or cut documents |
| Average score falling | Product changes faster than documents | Add triggers; review after each release |
| Same problem returns | Fixed the symptom, not the cause | Find why it keeps happening and change the process |
| Many "unanswered" support questions | Missing or hard-to-find documents | Create or rename documents; add to help center |

### 14.3 Monthly summary (3 lines)
What got better? What got worse? What will I do about it?

YOUR ANSWER:

---

# PART 15: EXCEPTIONS, ESCALATION, ARCHIVING

### 15.1 Exceptions
Sometimes a review must be skipped or delayed. Allowed reasons, and the rule:

- Illness or emergency
- Holiday
- A launch emergency

**Rule:** Write it in the missed-review table (Part 12), pick a makeup date within **14 days**, and **never skip** Critical fixes or the launch-week checks.

What reasons will you allow?
YOUR ANSWER:

### 15.2 Escalation
When something is stuck, who decides?

| Situation | Who decides | How fast |
|---|---|---|
| A Critical problem is open past its deadline | | |
| An owner leaves or is unavailable | | |
| Two documents disagree and no one knows which is right | | |
| An AI agent suggests something risky or unclear | | |
| A customer reports that a document caused harm or loss | | |

Solo founder note: if you are the only person, write `Me, and I will also ask <advisor name or AI second opinion> for High-importance decisions`.

### 15.3 Archiving old documents
Old documents confuse people and AI agents. Archive when a document is no longer true or no longer used.

**Steps**
1. Set Status to **Archived** and add the reason and date at the top.
2. Move it to the archive folder: YOUR ANSWER (folder path):
3. Remove it from navigation, help center, and AI-agent knowledge sources.
4. Search for links pointing to it. Fix or redirect them.
5. Remove it from the active inventory (Part 2) and note it in Part 12.

**Never delete** documents that might be needed for legal, financial, or audit reasons. How long will you keep archived documents? YOUR ANSWER:

### 15.4 Hand-over when an owner changes
- [ ] New owner is named in Part 2 and in each document header.
- [ ] Old owner writes a short note: what is risky, what is overdue, what only they know.
- [ ] New owner reviews the first three High-importance documents within 14 days.

---

# PART 16: SECURITY AND PRIVACY RULES

**Why we ask:** Documents are a common place for secrets to leak. These rules protect you and your customers.

### 16.1 Never put these in any document, example, screenshot, or AI prompt
- Passwords, API keys, tokens, private keys
- Customer names, emails, phone numbers, addresses, payment details, or any identifying information (unless the document is a protected system built for that and approved)
- Internal system addresses or admin links that must stay private
- Anything covered by a contract that says it must stay private

**Instead write:** where the secret is stored (for example, "in the password manager") and who can access it.

### 16.2 Review checks
At every quarterly audit:
- [ ] Search all documents for the words: password, secret, token, key, private, apikey.
- [ ] Check screenshots for names, emails, and addresses.
- [ ] Confirm customer examples use made-up data.
- [ ] Confirm who can view and edit each folder. Remove anyone who no longer needs access.
- [ ] Confirm AI tools can read only the folders listed in Part 8.3.2.

### 16.3 If a secret is found
1. **Treat it as leaked.** Change or revoke it immediately.
2. Remove it from the document and from its history, where possible.
3. Log it as a Critical problem (Part 13) and an incident (T2).
4. Check whether any customer data was exposed. Follow your legal duties to report if required.

Who is responsible for this? YOUR ANSWER:

### 16.4 Privacy and law
Laws about customer data differ by country and by industry. This template does not give legal advice. Have a qualified professional confirm your privacy policy and data handling before launch.

- Countries where customers live (or will live): YOUR ANSWER:
- Who confirmed the privacy policy, and when: YOUR ANSWER:

---

# PART 17: FINAL SIGN-OFF

Use this before you start following the plan, and again after major changes.

### 17.1 Completeness check
- [ ] Part 1: identity filled; no blanks.
- [ ] Part 2: all four inventory tables are filled or marked `N/A - reason`.
- [ ] Part 3: roles and the solo safeguard chosen.
- [ ] Part 4: deadlines and writing rules chosen.
- [ ] Part 5: dates and phase answers filled for every phase.
- [ ] Part 6: weekly, monthly, and quarterly times chosen **and added to calendar**.
- [ ] Part 7: trigger deadlines and ways to notice them chosen.
- [ ] Part 8: AI tools, permissions, and approval path chosen.
- [ ] Part 9: customer definition and counting method written.
- [ ] Part 15 and 16: escalation, archiving, and security answers filled.
- [ ] Every `Example:` line was removed or replaced.
- [ ] No `TBD` without a date.

### 17.2 The stranger test
Hand this file to someone who has never seen the project. Ask them to answer these using **only** this file:

1. Which documents exist, and who owns each? (Part 2)
2. When is the next weekly, monthly, and quarterly review? (Part 6)
3. What do you do if a customer reports a wrong help article? (Part 7, T3)
4. What do you do after changing an AI prompt? (Part 7, T4)
5. May an AI agent approve a document? (Part 8)
6. How do you know a document passed? (Part 4)
7. What happens at customer number 100? (Part 9)

- [ ] They answered all seven correctly without asking questions.
- [ ] Where they struggled, I improved the file.

### 17.3 Sign-off

| | Name | Date |
|---|---|---|
| Completed by | | |
| Approved by | | |
| First review scheduled for | | |
| Next review of **this file** | | |

**Review of this file itself:** Review this file at every quarterly audit and at every phase change.

---

# APPENDIX A: WORKED EXAMPLE (FILLED-IN SAMPLE)

**Purpose:** See what "good" looks like. This is for a made-up product. Do not copy it; copy the style.

### Part 1 (example)
- 1.1 Project name: `PlantPal`
- 1.2 Description: `This product helps busy people remember to water their houseplants.`
- 1.3 Owner: `Priya Shah`
- 1.5 Start date: `2026-09-01`
- 1.6 Target launch: `2027-02-15`
- 1.7 Where documents live:

| Place | What is kept there | Link or path |
|---|---|---|
| Git repository | README, API docs, ADRs, AI-agent files | `github.com/example/plantpal` |
| Notion workspace | Product docs, support templates | `Notion > PlantPal` |
| Help center | Customer articles | `help.example.com` |

### Part 2 inventory (example)

| ID | Document name | Location | Owner | Importance | Change speed | Review rhythm | Last reviewed |
|---|---|---|---|---|---|---|---|
| PRD-01 | Product requirements v1 | Notion > Product | Priya | H | Medium | Monthly | 2026-10-05 |
| TECH-01 | README and setup guide | Repo `/README.md` | Priya | H | Fast | Weekly | 2026-10-12 |
| TECH-02 | Incident playbook | Repo `/docs/incident.md` | Priya | H | Slow | Monthly | Never |
| AI-01 | Watering-reminder agent instructions | Repo `/agents/reminder.md` | Priya | H | Fast | Weekly | 2026-10-12 |
| AI-02 | Evaluation set for reminder agent | Repo `/agents/evals.md` | Priya | M | Medium | Monthly | 2026-10-05 |
| CUST-01 | Getting started guide | Help center | Priya | H | Medium | Monthly | Never |
| CUST-02 | FAQ | Help center | Priya | M | Fast | Weekly | Never |

### Part 3 (example)
- Roles: `Owner, Author, Reviewer, Approver = Priya. AI Assistant = Claude (drafts and suggests).`
- Solo safeguard chosen: `Wait 24 hours and run an AI first-pass review before I decide.`
- Backup person: `Nobody - reviews pause, and I log the pause in Part 12.`

### Part 6 (example)

| Review | Day and time | Length | Documents in scope | Recorded in |
|---|---|---|---|---|
| Weekly quick check | Friday 10:00 | 30 min | TECH-01, AI-01, CUST-02 | Part 12 |
| Monthly full review | First Monday 09:00 | 2-3 hours | All Weekly and Monthly | Part 12 |
| Quarterly deep audit | First Monday of Jan, Apr, Jul, Oct | Half day | All | Part 12 |

### Part 7 (example)
- `T4 AI change: before any prompt edit goes live, I run the evaluation set and save results in /agents/evals-results/.`
- How I notice T1: `The release checklist has a final item: "Run Part 7 T1 checklist".`

### Part 9 (example)
- Customer definition: `A person who completed sign-up and used the app on at least 2 different days.`
- Counted by: `Dashboard number "Active customers", updated by Priya every Monday.`

### Part 12 log (example rows)

| Date | Review type | Phase | Document ID(s) | Reviewer | AI used? | Score | Result | Problems found | Rhythm changed? | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| 2026-10-12 | W | 3 Build | TECH-01, AI-01 | Priya | Yes | 7 | PF | 2 | No | Setup step 4 used old command (P-003) |
| 2026-10-19 | W | 3 Build | TECH-01, AI-01 | Priya | Yes | 8 | P | 0 | No | P-003 fixed |
| 2026-11-02 | M | 3 Build | All Monthly | Priya | Yes | 6 | PF | 5 | TECH-02 Monthly to Weekly | Incident playbook never tested (P-006) |

### Part 13 (example)

| ID | Date found | Document ID | What is wrong | Failed test | Size | Fix by | Owner | Status | Date fixed |
|---|---|---|---|---|---|---|---|---|---|
| P-003 | 2026-10-12 | TECH-01 | Setup step 4 uses a command that no longer exists | Accurate | MJ | 2026-10-19 | Priya | Fixed | 2026-10-17 |
| P-006 | 2026-11-02 | TECH-02 | Restore steps never tested | Accurate | C | 2026-11-02 | Priya | In progress | |

---

# APPENDIX B: GLOSSARY

Plain-English meanings. If a word confuses you, look here.

| Word | Meaning |
|---|---|
| **AI agent** | A computer program powered by AI that can follow instructions and take actions, such as writing text, using tools, or answering customers |
| **Approver** | The human who says a document is good to use |
| **Archive** | Move an old document to a safe place and mark it as no longer in use, without deleting it |
| **Architecture** | A description of the parts of a product and how they fit and talk to each other |
| **ADR (decision record)** | A short note that says what was decided, why, and what else was considered |
| **API** | A way for one piece of software to ask another for something |
| **Cadence** | A regular rhythm; how often something happens |
| **Critical / Major / Minor** | Sizes of a problem. Critical can hurt customers or break the product; Major causes confusion or delay; Minor is wording or formatting |
| **Doc debt** | A pile of documentation problems not yet fixed |
| **Evaluation set (eval)** | A list of sample questions with the answers you expect, used to test whether an AI agent still behaves correctly |
| **Exit gate** | A checklist that must be fully ticked before moving to the next phase |
| **Guardrail** | A rule that stops an AI agent from doing something unsafe or off-limits |
| **Hallucination** | When an AI states something that sounds confident but is false |
| **Header** | The top block of a document with owner, dates, and status |
| **Incident** | A real problem in the live product such as an outage or data issue |
| **Inventory** | The master list of all documents |
| **Model (AI model)** | The AI "engine" that powers an agent. It has a name and a version |
| **Owner** | The one person responsible for a document |
| **Prompt** | The written instructions given to an AI |
| **Rollback** | Going back to an earlier working version |
| **Runbook** | A step-by-step guide for fixing a specific problem |
| **Stale** | No longer true because something changed |
| **Status** | Where a document stands: Draft, In Review, Approved, Needs Fix, or Archived |
| **Trigger** | An event that starts an extra review immediately |
| **Version** | A numbered copy of a product or document at a point in time |

---

# APPENDIX C: READY-TO-USE AI AGENT PROMPTS

Copy a prompt, replace anything in `<angle brackets>`, and give it to your AI agent along with only the documents it is allowed to read (Part 8.3.2). **Never include secrets or private customer data.**

### C.1 Review one document

```
You are a documentation reviewer. You do not approve documents; a human does.

Document to review: <paste the document or its path>
What it describes (the real thing to compare against): <paste code, settings, or the product description>
Current phase: <phase name>
Reason for review: <weekly | monthly | quarterly | trigger T1-T4>

Score the document from 0 to 2 on each test:
1. Accurate: matches the real thing today
2. Complete: nothing missing, header present, no overdue TBD
3. Understandable: a beginner could follow it without guessing
4. Findable and Safe: right name and place, no secrets or private data

For every problem, give:
- the exact line or section
- what is wrong
- what evidence you used
- size: Critical, Major, or Minor
- a suggested fix

If you are unsure, say "I cannot verify this" and do not guess.
Do not rewrite the whole document. Only suggest changes.
```

### C.2 Find stale information across documents

```
Here is a list of changes in the latest release: <paste the list>.
Search these documents: <list>.
Find every place that mentions anything affected by the changes.
For each place give: document, line or section, the old statement, and what likely needs to change.
Mark each as "Confirmed difference" or "Possible, needs a human check".
Do not edit anything.
```

### C.3 Check an AI-agent instruction file

```
Review this AI-agent instruction file: <paste>.
Check and report on each of these:
- Is the model name and version stated?
- Is the purpose clear in one sentence?
- Are allowed tools and forbidden actions listed?
- Is there a rule for what the agent does when unsure?
- Are there example inputs and expected outputs?
- Are there contradictions or vague instructions?
- Does anything conflict with these customer-facing promises: <paste>?
- Are there secrets or private data?
Give a list of problems with severity and a suggested fix for each.
```

### C.4 Test a setup or how-to guide as a beginner

```
Pretend you know nothing about this product. Follow this guide exactly: <paste>.
Report every point where:
- a step is missing or out of order
- a term is not explained
- a result you expected was not described
- you had to guess
Do not fix the guide. Only report where you would have been stuck.
```

### C.5 Turn customer questions into document fixes

```
Here are support questions from the last <period>, with personal details removed: <paste>.
1. Group them into themes.
2. For each theme, say which existing document should have answered it: <list of customer documents>.
3. For each, say whether that document is: missing, wrong, hard to find, or hard to understand.
4. Suggest a short plain-language fix.
Rank themes by how many questions they cover.
```

### C.6 Draft a missing document (human must review fully)

```
Draft a first version of: <document name>.
Audience: <who will read it>.
Goal: <what the reader should be able to do afterward>.
Facts you may use (do not invent any others): <paste notes>.
Use short sentences, numbered steps, and the document header from my template:
Owner, Status (Draft), Last reviewed, Next review due, Applies to, Related docs.
Mark anything you are unsure about as [NEEDS HUMAN CHECK].
```

### C.7 Quarterly check of the AI reviewer

```
I planted 3 mistakes in the document below. Find every problem and list them with evidence.
<paste document>
```
(Afterward, compare with the 3 planted mistakes and record in Part 12.)

### C.8 After an incident

```
Here is the incident summary: <paste, no private data>.
Here are the related documents: <list>.
Tell me:
1. Which document should have prevented or shortened this incident?
2. What was missing, wrong, or unclear?
3. What steps from the real fix should be added to the runbook?
4. Which customer-facing text may now be inaccurate?
Give suggestions only. Do not edit.
```

---

# APPENDIX D: ONE-PAGE QUICK REFERENCE

Print or pin this.

**The three questions behind every review**
1. Is it **true** today?
2. Is it **complete**?
3. Could a beginner **follow it without guessing**?

**The rhythm**

| When | What |
|---|---|
| Every week (30 min) | Check fast-changing docs: setup, API, AI-agent files, FAQ |
| Every month (2-3 hrs) | Full review of Weekly + Monthly docs, update problems list and scorecard |
| Every quarter (half day) | Audit everything, archive old, check security, review this file |
| Right now (trigger) | Release, incident, customer confusion, AI change |

**Pass rule:** 8 of 8 = Pass. 6-7 = Pass with fixes. Anything with a 0 = Fail.

**Fix deadlines:** Critical same day. Major 7 days. Minor 30 days (change in Part 4.3).

**AI rule:** AI drafts and suggests. A human approves. No secrets to AI.

**Customer milestones:** 1, 10, 25, 50, 100, 250, 400, 500.

**Every document needs:** owner, status, last reviewed, next review due, clear name, right folder.

**If you do not know:** write `TBD - decide by <date>`. Never leave it blank.

---

# APPENDIX E: TEMPLATE CHANGE LOG

Keep a record of changes to **this file**.

| Version | Date | Changed by | What changed | Why |
|---|---|---|---|---|
| 1.0 | | | First version created | Standard template for AI-Driven Development Life Cycle documentation reviews |
| | | | | |
| | | | | |
