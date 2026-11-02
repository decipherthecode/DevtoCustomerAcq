# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

> **Template name:** Knowledge_Base.md
> **Template version:** 1.0
> **Folder it lives in:** `Documentation Management and Institutional Knowledge/`
> **What this file is:** The ONE file that holds everything we know about a product, from the first idea until the first 500 paying customers. It is the single source of truth for humans AND for AI agents (such as Claude).

## Step 1. Copy the template
1. Copy this whole file into your new project folder.
2. Rename it to `Knowledge_Base.md` (keep the name the same in every project so everyone can find it).
3. Fill in the **Project Passport** (Part A) first. Do not delete anything else yet.

## Step 2. Answer the questions in order
Every item looks like this:

```
**Q1.1 What is the product called?**
- Why we ask: So everyone uses the same name.
- Example: "PlantPal"
- Answer:
```

How to answer:
- Write your answer on the line after **Answer:**. One sentence is fine. Short and clear beats long and fancy.
- Pretend you are explaining to a smart 10-year-old. No secret words. If you must use a hard word, explain it in brackets, like this: "API (a way for two programs to talk)".
- Use **numbers, dates and names**, not vague words. Write "50 customers by 31 Dec 2026", not "lots of customers soon".
- Do not guess. If you do not know yet, write exactly one of these:
  - `TBD - owner: <name> - by: <date>` (we will find out later, and here is who will do it)
  - `N/A - because: <reason>` (this does not apply, and here is why)
  - `DECISION NEEDED - options: A / B` (a human must choose)
- Never leave an Answer line empty. An empty line is a trap for the next reader.
- **Never put passwords, secret keys, or customers' private data in this file.** Write where they are stored instead (example: "stored in the password manager, vault 'Project X'").

## Step 3. Set the status tag of each Part
Every Part starts with a status line. Change it as you go:

| Tag | Meaning |
|---|---|
| `[NOT STARTED]` | Nothing filled in yet |
| `[IN PROGRESS]` | Some answers are in, some are `TBD` |
| `[DONE]` | Every question answered, no `TBD` left that blocks work |
| `[SKIPPED]` | Does not apply (write why next to the tag) |

## Step 4. Keep it alive
- Update this file whenever something real changes (a decision, a launch, a mistake). Add a line to the **Change Log** (Appendix B).
- Put "last reviewed" dates on important answers.
- Review the whole file at the end of every phase (see the **Phase Gates** table in Part A).
- Finish with the **Ready-to-Go Checklist** (Appendix F).

## Quick start for beginners (15 minutes)
If the file looks big, do only this first. You can finish the rest later.
1. Fill in Part A (the Project Passport).
2. Answer B1, B4, C1 and D1 (the problem, the solution, the customer, the smallest version).
3. Answer E2, E3 and E4 (what the AI may do, must ask about, and must never do).
4. Set every other Part to `[NOT STARTED]`. You are now safe to begin.
5. Each time you finish a phase, fill in the Parts for the next phase.
- Stuck? Copy the question, paste it to Claude, and say: "Ask me simple questions one by one until you can write this answer for me. Do not guess." Then read the answer, fix anything wrong, and paste it here.
- A worked, filled-in sample project lives in **Appendix G**. Look at it when you are unsure what a good answer looks like.

## Good answers vs bad answers
| Bad (makes people guess) | Good (nobody has to guess) |
|---|---|
| "We will launch soon." | "We launch on 2027-02-01." |
| "Fast website." | "Pages open in under 2 seconds on a phone." |
| "The team will handle it." | "Sam owns it. Backup: Priya." |
| "Use the usual database." | "PostgreSQL 16, hosted on Supabase, project 'plantpal-prod'." |
| "Be careful with customer data." | "Never copy customer emails into prompts, logs, or this file." |
| Empty answer | `TBD - owner: Sam - by: 2026-11-01` |

## Rules for AI agents (Claude and others) reading this file
1. Read **Part A** and **Part E (AI Working Agreement)** before doing any task.
2. This file beats your own assumptions. If an answer is missing or says `TBD`, **ask the human; do not invent an answer.**
3. If two answers disagree, stop and report the conflict. Do not pick one silently.
4. Only a human may approve: spending money, deleting data, publishing to real customers, changing legal text, changing prices. (Details in Part E.)
5. When you finish work that changes a fact in this file, propose an edit to the matching answer and add a Change Log line.
6. Quote the question number (example: "per E3") when you explain a decision.

## Phases covered (the whole journey)
| Phase | Name | Parts |
|---|---|---|
| 0 | Idea and Discovery | B, C |
| 1 | Planning and Scope | D, E, F |
| 2 | Design and Build | G, H, I, J |
| 3 | Test and Secure | K, L |
| 4 | Release and Launch | M, N, O |
| 5 | Grow to 500 Customers | P, Q, R, S |
| 6 | Run, Learn, Improve | T, U |
| 7 | After 500: Next Stage | Y |
| All | Reference and growth support | V, W, X + Appendices |

---

# PART A. PROJECT PASSPORT (fill this in first)

**Status:** `[NOT STARTED]`

**A1. What is the product called?**
- Why we ask: One name, used everywhere.
- Example: "PlantPal"
- Answer:

**A2. Explain the product in ONE sentence a 10-year-old would understand.**
- Example: "PlantPal reminds you when to water your plants so they stop dying."
- Answer:

**A3. Who owns this project (the final decision-maker)?**
- Example: "Sam Lee, founder, sam@example.com"
- Answer:

**A4. What kind of product is it? (circle/keep one)**
- Options: Website / Web app / Mobile app / Desktop app / AI agent or chatbot / API / Browser extension / Hardware + software / Other
- Answer:

**A5. What is the current phase? (see the phase table above)**
- Example: "Phase 1, Planning and Scope"
- Answer:

**A6. What date did the project start, and what is the target date for the first public launch?**
- Example: "Started 2026-10-19. Launch target 2027-02-01."
- Answer:

**A7. What is the finish line? (the "first 500 customers" goal in exact words)**
- Why we ask: So everybody knows when we have won this stage.
- Example: "500 paying customers who each completed at least one real use of the product, by 2027-08-31."
- Answer:

**A8. Where do the other important things live? (links only, no secrets)**
- Example: "Code: github.com/org/plantpal. Design: Figma link. Tasks: Notion board. Support inbox: help@plantpal.com."
- Answer:

**A9. Phase Gates (a gate is a stop sign: do not go on until the checks pass).**
Fill in the date each gate was passed and who approved it.

| Gate | Must be true before passing | Date passed | Approved by |
|---|---|---|---|
| G0 Idea approved | Parts B and C are `[DONE]` | | |
| G1 Plan approved | Parts D, E, F are `[DONE]` | | |
| G2 Build-ready | Parts G to J are `[DONE]` enough to start building | | |
| G3 Launch-ready | Parts K to O are `[DONE]`; Ready-to-Go Checklist passed | | |
| G4 Customer 100 | 100 customers reached; Part Q reviewed | | |
| G5 Customer 500 | 500 customers reached; Part U lessons written | | |
| G6 Next stage planned | Part Y is `[DONE]` | | |

**Done when (Part A is really finished):**
- [ ] Every Answer in Part A is filled (no empty lines).
- [ ] The finish line (A7) has a number and a date.
- [ ] Links in A8 open.

---

# PART B. THE IDEA AND THE PROBLEM

**Status:** `[NOT STARTED]`

**B1. What problem are we solving? Describe it as a short story about a real person.**
- Example: "Maria buys plants but forgets to water them. Three died last year. She feels bad and wastes money."
- Answer:

**B2. How do people solve this problem today (without our product)?**
- Example: "Sticky notes, phone alarms, or they just forget."
- Answer:

**B3. Why are those current ways not good enough?**
- Example: "Alarms do not know which plant needs water, and they do not adapt to the season."
- Answer:

**B4. What is our solution, in plain words?**
- Example: "An app that knows each plant and tells you exactly when and how much to water."
- Answer:

**B5. What makes us different from other options? (the one thing they cannot easily copy)**
- Answer:

**B6. Why are we the right people to build this?**
- Example: "I worked 5 years at a garden store and know the plant problems."
- Answer:

**B7. How do we know people really have this problem? (what proof do we have)**
- Example: "Talked to 12 plant owners; 9 said they lose plants from forgetting."
- Answer:

**B8. What would make us STOP the project? (our "kill" signal)**
- Example: "If after talking to 30 people fewer than 5 say they would pay."
- Answer:

**B9. What is the big dream for the product in 3 years?**
- Answer:

**Done when (Part B is really finished):**
- [ ] A stranger could explain the problem back to you after reading B1 to B4.
- [ ] B7 has real proof (people or numbers), not opinions.
- [ ] B8 (the stop signal) is written.

---

# PART C. CUSTOMERS AND MARKET

**Status:** `[NOT STARTED]`

**C1. Who is our ideal customer? Describe one real-feeling person (name, age, job, daily life).**
- Example: "Maria, 29, office worker, lives in an apartment, owns 8 plants."
- Answer:

**C2. Where do these people hang out online and offline? (so we can find them later)**
- Example: "Instagram plant groups, Reddit r/houseplants, local garden centers."
- Answer:

**C3. What do they care about most when choosing a product like ours? (top 3)**
- Answer:

**C4. Who are our competitors or "almost" competitors? List at least 3 and one thing they do well and one thing they do badly.**

| Competitor | Link | They do well | They do badly | Price |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

**C5. How big is the market? (how many possible customers exist; say where the number came from)**
- Example: "About 20 million US plant owners (source: survey link)."
- Answer:

**C6. Which customers will we NOT serve? (saying no keeps us focused)**
- Answer:

**C7. Customer interview log (talk to real people; write what they said, not what we hoped).**

| Date | Who (first name / type) | Key thing they said | What we learned |
|---|---|---|---|
| | | | |

**Done when (Part C is really finished):**
- [ ] C1 describes one specific person.
- [ ] At least 3 competitors are listed in C4.
- [ ] At least 5 real customer talks are logged in C7.

---

# PART D. SCOPE AND REQUIREMENTS

**Status:** `[NOT STARTED]`

**D1. What is the smallest version we can launch that still helps the customer? (the MVP, "minimum viable product")**
- Example: "Add plants, get a watering reminder, mark as watered."
- Answer:

**D2. List every feature and mark its priority.** (Must = cannot launch without, Should = important, Could = nice, Won't = not now)

| ID | Feature (plain words) | Who needs it | Priority | Done when... (a test anyone can check) |
|---|---|---|---|---|
| F1 | | | Must | |
| F2 | | | Must | |
| F3 | | | Should | |
| F4 | | | Could | |
| F5 | | | Won't (now) | |

**D3. What is NOT part of the first launch? (write it down so nobody asks for it by surprise)**
- Answer:

**D4. User stories (one per Must feature). Format: "As a ___, I want to ___, so that ___."**
- Example: "As a plant owner, I want a reminder, so that my plant does not die."
- Answer:

**D5. What must the product be like besides features? (speed, safety, reliability, works offline, languages, accessibility)**
- Example: "Pages load in under 2 seconds. Works on phones. Readable by screen readers."
- Answer:

**D6. What are we assuming is true but have not checked? (assumptions)**
- Example: "People will accept notifications."
- Answer:

**D7. What must be true for the outside world? (constraints: budget, deadline, law, technology we must use)**
- Answer:

**Done when (Part D is really finished):**
- [ ] Every Must feature has a 'Done when' test you can check.
- [ ] D3 lists what is NOT in the first launch.
- [ ] An AI or new person could build F1 to F4 from this Part without asking you questions.

---

# PART E. AI WORKING AGREEMENT (how humans and AI build together)

**Status:** `[NOT STARTED]`
> This Part is what Claude and other AI agents read before they touch the project. Keep it exact.

**E1. Which AI tools do we use, and for what job?**

| Tool | Job (coding, writing, testing, research, design...) | Who may use it | Where its settings live |
|---|---|---|---|
| Claude (chat) | | | |
| Claude Code or another coding agent | | | |
| Other: | | | |

**E2. What can the AI do on its own? (green list)**
- Example: "Write code on a branch, write tests, write draft docs, summarize research."
- Answer:

**E3. What must the AI ASK a human before doing? (yellow list)**
- Example: "Install new libraries, change the database layout, change a price, send any email."
- Answer:

**E4. What must the AI NEVER do? (red list)**
- Example: "Delete data, publish to customers, touch money or legal pages, read secret keys, push straight to the main branch."
- Answer:

**E5. Who approves what? (human approval map)**

| Action | Approver (name/role) | How they approve (PR review, message, ticket) |
|---|---|---|
| Merge code to main | | |
| Release to customers | | |
| Spend money / buy a service | | |
| Change prices or legal text | | |
| Delete or change real customer data | | |

**E6. How do we give the AI its starting instructions? (project instruction file, e.g. a `CLAUDE.md` or "Project Instructions")**
- Example: "File CLAUDE.md in the repo root tells Claude: read Knowledge_Base.md Parts A, E, H first."
- Answer:

**E7. Prompt Library (the best prompts that worked; reuse them).**

| Name | When to use | The prompt (copy/paste) | Last tested | Result quality (1-5) |
|---|---|---|---|---|
| Plan a feature | | | | |
| Write tests | | | | |
| Review code | | | | |
| Explain an error | | | | |

**E8. How do we check AI work before trusting it? (review checklist)**
- Example: "Human reads the change, tests pass, no new secrets, matches Part H standards."
- Answer:

**E9. What does the AI need to know that it often gets wrong here? (known traps)**
- Example: "Our dates are always UTC. Never use the old payment API."
- Answer:

**E10. If the product itself uses AI (a model inside the product), answer these. Otherwise write `N/A - because: ...`**
- Which model/provider and version?
- What is the AI's job in the product?
- What must it never say or do?
- How do we test its answers (a list of test questions and ideal answers)?
- What does each AI call cost, and what is our monthly limit?
- What happens when the AI is down or gives a bad answer?
- Answer:

**E11. How do we record AI work so a human can trace it? (logs, pull request notes, session notes)**
- Answer:

**E12. Agent roles (who does which job). Give each AI "hat" one clear job.**

| Role | Job | Must read first (Part/Question) | Output it hands back | Human who checks it |
|---|---|---|---|---|
| Planner | Turns a goal into small tasks | A, D, F | Task list with "done when" | |
| Builder | Writes code or content | A, E, H | Change on a branch, with notes | |
| Reviewer | Checks the Builder's work | E, H, K | Review comments | |
| Tester | Writes and runs tests | D, K | Test results | |
| Researcher | Finds facts, cites sources | B, C | Summary with links | |
| Writer | Drafts docs, emails, help pages | G, O, P | Draft, flagged "needs human check" | |

**E13. Task brief template. Every job given to an AI uses this shape (copy it).**
```
Goal: (one sentence)
Why it matters: (one sentence)
Read first: (Parts/Questions of this file, and any other files)
Must do:
Must NOT do:
Done when: (checks a human can see)
Output format: (file, message, pull request...)
If unsure: stop and ask. Do not guess.
```
- Answer (our team's tweaks to the template):

**E14. Which files must the AI read at the start of EVERY session, in what order, and where does it save notes between sessions? (memory)**
- Example: "1) CLAUDE.md 2) Knowledge_Base.md Parts A, E, H 3) the task brief 4) docs/session-notes.md (write 5 lines at the end)."
- Answer:

**E15. Handoff note (when an AI session or a person stops, leave this for the next one).**
```
Date / who:
What I finished:
What is still open:
Files I changed:
What I was unsure about:
Next best step:
```
- Answer (where handoff notes are stored):

**E16. What does the AI do when it is stuck, unsure, or finds a conflict?**
- Example: "Stop. Write what is missing as a question with 2 options. Wait for a human. Never fill a gap with a guess."
- Answer:

**E17. AI quality scoreboard (how we know the AI is helping, not hurting).**

| Measure | How we count it | Target | Current |
|---|---|---|---|
| AI changes accepted without edits | % of AI changes merged unchanged | | |
| Bugs found after AI work | Count per month | | |
| Time saved | Hours per week vs doing it by hand | | |
| Rework | % of AI output thrown away | | |

**E18. AI usage limits and money (so there are no surprise bills).**
- Monthly AI budget:
- Who is told when 80% is used:
- What gets switched off at 100%:
- Answer:

**E19. AI mistakes log (write down every AI mistake so it never repeats).**

| Date | What the AI did wrong | Damage | Rule we added (and where) |
|---|---|---|---|
| | | | |

**E20. How often do humans review this Part and the instruction file? Who does it?**
- Example: "First Monday of each month, Sam."
- Answer:

**E21. Starting-instructions file for Claude (copy this into the project, for example as `CLAUDE.md` in the main folder, and keep it SHORT).**
```text
# CLAUDE.md - <Project name>

## Read first
1. Knowledge_Base.md Parts A, E and H, plus the Part for today's task.
2. The task brief (see E13).

## What this project is
<one sentence, copied from A2>

## How to run things
Run the app:   <command from H4>
Run tests:     <command>
Check style:   <command>

## Rules
- Follow the green, yellow and red lists in E2, E3 and E4.
- Never edit the parts listed in H7 without asking.
- Dates are UTC. Never put secrets in files or messages.
- If something is missing or unclear, stop and ask. Do not guess.

## Done means
Tests pass, a "What the AI did" note is written, and any changed fact is
proposed as an edit to Knowledge_Base.md with a Change Log line.
```
- Answer (where the file lives, who may edit it, and the date it was last checked):

**E22. Claude Code safety settings (permissions, automatic checks, helper agents). If you do not use Claude Code, write `N/A - because: ...`**

| Setting | Our choice | Must match |
|---|---|---|
| Things Claude may do without asking (allow list) | | E2 |
| Things Claude must ask about first (ask list) | | E3 |
| Things Claude is blocked from doing (deny list) | | E4 |
| Automatic checks that run by themselves (for example: run tests or style checks after every change, block secrets from being saved) | | E8, K7 |
| Helper agents and their jobs (one per role) | | E12 |
| Where these settings are stored (project file shared with the team, or private to one person) | | E6 |
| Who is allowed to change these settings | | E5 |

- Answer (how we test that the red list really blocks the action):

**Done when (Part E is really finished):**
- [ ] E2, E3 and E4 (green, yellow, red lists) are filled in.
- [ ] Every approval in E5 has a named human.
- [ ] E14 names the exact files the AI reads first.
- [ ] E21 (instructions file) exists in the project and E22 matches the green, yellow and red lists.
- [ ] A human has read this whole Part out loud and agrees.

---

# PART F. PLAN, PEOPLE AND RISKS

**Status:** `[NOT STARTED]`

**F1. Who is on the team, and what does each person own?**

| Name | Role | Owns | Hours per week | Contact |
|---|---|---|---|---|
| | | | | |

**F2. Roadmap (big steps in order, each with a date).**

| Milestone | Target date | Owner | Done when... | Status |
|---|---|---|---|---|
| Idea approved (G0) | | | | |
| Plan approved (G1) | | | | |
| First working version | | | | |
| Testing finished | | | | |
| Public launch | | | | |
| 100 customers | | | | |
| 500 customers | | | | |

**F3. How do we organize daily work? (method, board, meeting rhythm)**
- Example: "One-week sprints, Notion board, 15-minute check-in on Mondays."
- Answer:

**F4. What could go wrong? (top 10 risks)**

| Risk | How likely (Low/Med/High) | How bad (Low/Med/High) | What we do to prevent it | Who watches it |
|---|---|---|---|---|
| | | | | |

**F5. What is our "Plan B" if the launch date slips by one month?**
- Answer:

**F6. How do we make and record decisions? (see the Decision Log in Appendix A)**
- Answer:

**Done when (Part F is really finished):**
- [ ] Every team member has an owner line in F1.
- [ ] Roadmap dates are real dates.
- [ ] At least 5 risks have a prevention step and a watcher.

---

# PART G. DESIGN AND USER EXPERIENCE

**Status:** `[NOT STARTED]`

**G1. What should the product feel like? (3 words)**
- Example: "Calm, friendly, simple."
- Answer:

**G2. Brand basics: name, logo location, colors (with codes), fonts, tone of voice.**
- Example: "Green #2E7D32, font Inter, voice: warm and short."
- Answer:

**G3. List every screen or page and what it is for.**

| Screen/page | Purpose | Link to design | Status |
|---|---|---|---|
| | | | |

**G4. Walk through the main journey, step by step, from "never heard of us" to "happy customer."**
- Example: "Sees ad, opens site, signs up, adds first plant, gets first reminder."
- Answer:

**G5. Accessibility promises (so everyone can use it).**
- Example: "Readable colors, big tap buttons, works with a keyboard, text can be enlarged."
- Answer:

**G6. Where are the written words kept? (button text, error messages, emails)**
- Answer:

**Done when (Part G is really finished):**
- [ ] Every screen in G3 has a link or a sketch.
- [ ] Brand colors and fonts have exact codes.
- [ ] The main journey (G4) has no missing step.

---

# PART H. TECHNOLOGY, ARCHITECTURE AND CODING RULES

**Status:** `[NOT STARTED]`

**H1. What technology do we use, and why? (language, framework, database, hosting)**

| Layer | Choice | Version | Why we chose it | Cost per month |
|---|---|---|---|---|
| Front end (what people see) | | | | |
| Back end (the engine) | | | | |
| Database (where data is kept) | | | | |
| Hosting (where it runs) | | | | |
| Login / accounts | | | | |
| Payments | | | | |
| Email / notifications | | | | |
| Monitoring | | | | |

**H2. Draw or describe how the parts connect. (a simple picture or a list: "A talks to B")**
- Answer:

**H3. Where is the code, and how is it organized? (repository link, folder map)**
- Answer:

**H4. How do I run the project on my own computer? (exact steps, copy/paste commands)**
- Example: "1) Install Node 22. 2) Run `npm install`. 3) Run `npm run dev`. 4) Open http://localhost:3000."
- Answer:

**H5. Coding rules everyone (and every AI) must follow.**
- Naming rules:
- Formatting/lint tool:
- How to write a commit message:
- How we name branches:
- How big a change may be:
- Answer:

**H6. External services and keys: list each service, why we use it, and WHERE its key is stored (never the key itself).**

| Service | Why | Where key is stored | Who can rotate it | Monthly cost |
|---|---|---|---|---|
| | | | | |

**H7. What are the "do not touch without asking" parts of the code?**
- Answer:

**H8. Known technical debt (shortcuts we took on purpose, to fix later).**
- Answer:

**Done when (Part H is really finished):**
- [ ] A new person can run the project using only H4.
- [ ] Every service in H6 says where its key lives.
- [ ] H7 names the parts nobody may change alone.

---

# PART I. DATA, PRIVACY AND SECURITY

**Status:** `[NOT STARTED]`

**I1. What information do we collect from customers? (list every kind)**
- Example: "Email, first name, plant list, payment (handled by the payment company, we never see card numbers)."
- Answer:

**I2. Why do we need each item? (if we do not need it, do not collect it)**
- Answer:

**I3. Where is the data stored, who can see it, and how long do we keep it?**
- Answer:

**I4. How is the data protected? (passwords, encryption, backups, access rules)**
- Answer:

**I5. Backups: how often, where kept, and when did we last TEST restoring one?**
- Answer:

**I6. Security checklist (mark yes/no, add date).**

| Check | Yes/No | Date |
|---|---|---|
| Strong login (and two-step login for the team) | | |
| Secrets kept out of code | | |
| Dependencies checked for known problems | | |
| Customers can only see their own data | | |
| Backups restore correctly | | |
| Team access removed when someone leaves | | |

**I7. What do we do if there is a data leak? (who to tell, within how many hours, in what order)**
- Answer:

**Done when (Part I is really finished):**
- [ ] Every piece of customer data is listed in I1 and has a reason in I2.
- [ ] Backup restore was tested, and the date is in I5.
- [ ] The leak plan (I7) names a person and a time limit.

---

# PART J. LEGAL AND COMPLIANCE

**Status:** `[NOT STARTED]`
> We are not a law firm. Use this Part to track what has been checked and by whom. Ask a qualified lawyer for anything important.

**J1. Which country/countries is the business in, and where are our customers?**
- Answer:

**J2. What legal papers do we need, and where are they?**

| Document | Needed? | Link | Last reviewed | Reviewed by |
|---|---|---|---|---|
| Terms of Service | | | | |
| Privacy Policy | | | | |
| Cookie notice | | | | |
| Refund policy | | | | |
| Open-source license list | | | | |
| Contracts with vendors/freelancers | | | | |

**J3. Which privacy or industry rules apply? (examples: GDPR for Europe, CCPA for California, children's privacy rules, health or finance rules)**
- Answer:

**J4. Who owns the code, the brand name, and the content? (ownership, trademark, licenses)**
- Answer:

**J5. If AI creates parts of our product or content, do we know the rules and licenses that apply?**
- Answer:

**J6. Business setup: company type, tax registration, bank account, insurance.**
- Answer:

**Done when (Part J is really finished):**
- [ ] Every needed legal paper in J2 has a link and a reviewer.
- [ ] Rules that apply to us (J3) are named, not guessed.
- [ ] A qualified lawyer or advisor has been asked about anything high-risk.

---

# PART K. TESTING AND QUALITY

**Status:** `[NOT STARTED]`

**K1. What does "good enough to launch" mean? (the quality bar, in numbers)**
- Example: "Zero known crashes on main journey, all Must features pass, page loads under 2 seconds."
- Answer:

**K2. Which kinds of tests do we run?**

| Test type | What it checks | Tool | Who runs it | When |
|---|---|---|---|---|
| Automatic small tests (unit) | Single pieces work | | | Every change |
| Connection tests (integration) | Pieces work together | | | Every change |
| Full journey tests (end-to-end) | A real user path works | | | Before release |
| Speed tests | It is fast enough | | | Before release |
| Security tests | It is safe | | | Before release |
| Accessibility tests | Everyone can use it | | | Before release |
| Real people tests (beta) | Real users can do the task | | | Before launch |

**K3. Test cases for each Must feature (what we do, what should happen).**

| Feature ID | Steps | Expected result | Pass/Fail | Date |
|---|---|---|---|---|
| F1 | | | | |

**K4. What devices, browsers and screen sizes must work?**
- Answer:

**K5. How do we report and rank bugs?**
- Example: "Critical = blocks customers, fix today. High = fix this week. Low = fix when time allows."
- Answer:

**K6. Beta test plan: who, how many, for how long, what we ask them.**
- Answer:

**K7. If AI writes code or tests, what extra checks do we do?**
- Answer:

**Done when (Part K is really finished):**
- [ ] The quality bar (K1) is written as numbers.
- [ ] Every Must feature has test cases in K3.
- [ ] Beta testers (K6) are chosen.

---

# PART L. BUILD, RELEASE AND DEPLOYMENT

**Status:** `[NOT STARTED]`

**L1. What environments exist? (e.g. local, test, staging, live) and how do they differ?**

| Environment | Link | Purpose | Who can use it | Real customer data? |
|---|---|---|---|---|
| Local | | | | No |
| Test / staging | | | | No |
| Live (production) | | | | Yes |

**L2. How does code get from a developer to live? (the exact steps)**
- Example: "Branch, pull request, review, tests pass automatically, merge, auto-deploy to staging, human approves, deploy live."
- Answer:

**L3. Release checklist (do every time).**
- [ ] All tests pass
- [ ] Change Log updated
- [ ] Backup taken
- [ ] Human approver said yes (see E5)
- [ ] Team knows the release time
- [ ] Monitoring is open and watched for 1 hour after

**L4. How do we undo a bad release? (rollback steps, exact commands, who can do it)**
- Answer:

**L5. How do we version the product and name releases?**
- Example: "v1.0.0 launch, v1.1.0 new feature, v1.0.1 bug fix."
- Answer:

**L6. If this is a mobile or desktop app: store accounts, review rules, review times, release steps.**
- Answer:

**L7. Release history.**

| Version | Date | What changed | Released by | Problems |
|---|---|---|---|---|
| | | | | |

**Done when (Part L is really finished):**
- [ ] The release steps (L2) have been practiced at least once.
- [ ] The rollback (L4) was tested, not just written.
- [ ] The release checklist (L3) is accepted by the approver.

---

# PART M. LAUNCH PLAN

**Status:** `[NOT STARTED]`

**M1. What kind of launch is it? (secret test, invite-only, soft public, big public)**
- Answer:

**M2. Launch countdown (what happens when).**

| When | Task | Owner | Done? |
|---|---|---|---|
| 8 weeks before | | | |
| 4 weeks before | | | |
| 1 week before | | | |
| Launch day | | | |
| 1 week after | | | |
| 4 weeks after | | | |

**M3. Where do we announce the launch?**
- Example: "Our email list, Product Hunt, 2 community groups, personal social posts."
- Answer:

**M4. Launch-day team plan: who watches what, who answers customers, who can say "stop."**
- Answer:

**M5. What does success look like on Day 1, Day 7 and Day 30? (numbers)**
- Example: "Day 1: 50 signups. Day 7: 150. Day 30: 300."
- Answer:

**M6. Launch "stop" signals (when we pause or roll back).**
- Example: "More than 5% of signups fail, or payments fail twice in a row."
- Answer:

**Done when (Part M is really finished):**
- [ ] The launch countdown (M2) has an owner on every row.
- [ ] Success numbers (M5) and stop signals (M6) are written.
- [ ] Everyone knows who can say 'stop' on launch day.

---

# PART N. PRICING, MONEY AND PAYMENTS

**Status:** `[NOT STARTED]`

**N1. How do we make money? (subscription, one-time, usage-based, ads, free with paid upgrade)**
- Answer:

**N2. What are the plans and prices?**

| Plan name | Price | What is included | Who it is for |
|---|---|---|---|
| | | | |

**N3. Why this price? (what we compared, what customers said)**
- Answer:

**N4. What does it cost us to run the product each month? (servers, AI usage, tools, support)**

| Cost item | Monthly cost | Grows with customers? |
|---|---|---|
| | | |
| **Total** | | |

**N5. Break-even: how many customers do we need to cover costs?**
- Example: "Costs $400/month, price $8/month, so 50 customers."
- Answer:

**N6. How much money do we have, and how many months can we keep going (runway)?**
- Answer:

**N7. How do payments work? (provider, refunds, failed payments, taxes, invoices)**
- Answer:

**N8. Do we offer a free trial, free plan or discounts? What are the rules?**
- Answer:

**N9. Money numbers to track at the 500-customer goal.**

| Number | What it means | Our target | Current |
|---|---|---|---|
| Monthly Recurring Revenue (MRR) | Money we expect each month | | |
| Customer Acquisition Cost (CAC) | What it costs to win one customer | | |
| Churn | % of customers who leave each month | | |
| Lifetime Value (LTV) | Money one customer brings in total | | |

**N10. Which accounting tool keeps our books, and who updates it? How often?**
- Example: "A simple online accounting tool. Sam records money in and out every Friday."
- Answer:

**N11. Taxes: what do we owe, to whom, and when? (income tax, sales tax or VAT, payroll tax if any; who files; due dates)**
- Why we ask: Missing a tax date can cost real money. Ask an accountant if unsure.
- Answer:

**N12. Invoices and receipts: how do customers get them, and where are copies kept?**
- Answer:

**N13. Money rules for spending: who may spend, how much without asking, and who double-checks?**
- Example: "Anyone on the team up to $50. Above $50 Sam approves. Above $500 Sam and a second person approve."
- Answer:

**N14. Where does money come from to run the business? (savings, customers, investors, grants, loans) and what rules or promises come with each?**
- Answer:

**N15. Monthly money log (fill in once a month; this is the number sheet you check against runway in N6).**

| Month | Money in | Money out | Cash left | Runway (months) | Notes |
|---|---|---|---|---|---|
| | | | | | |

**Done when (Part N is really finished):**
- [ ] Every plan has a price (N2) and a reason (N3).
- [ ] Monthly costs (N4) add up to a total.
- [ ] A real small test payment worked end to end.
- [ ] Accounting, tax dates and spending rules (N10 to N13) are written, and the monthly log (N15) has a first row.

---

# PART O. ONBOARDING, SUPPORT AND FEEDBACK

**Status:** `[NOT STARTED]`

**O1. What is the first "wow, this works!" moment for a new customer? (called the "activation" moment)**
- Example: "They get their first correct watering reminder."
- Answer:

**O2. How does a new customer get from signup to that moment? (steps, and how long it should take)**
- Answer:

**O3. How can customers get help? (email, chat, help pages, community)**
- Answer:

**O4. How fast do we reply, and who replies?**
- Example: "Within 24 hours on weekdays, Sam replies, Claude drafts, human sends."
- Answer:

**O5. Top 10 questions customers will ask (and the answers). Keep growing this list.**

| Question | Answer | Help page link |
|---|---|---|
| | | |

**O6. Reply templates for common situations (thanks, bug found, refund, cannot log in, angry customer).**
- Answer:

**O7. How do we collect feedback? (surveys, calls, in-product button) and how often do we review it?**
- Answer:

**O8. Feedback log (write what customers said; mark what we did about it).**

| Date | Customer type | Feedback | Decision (do/later/no) | Reason |
|---|---|---|---|---|
| | | | | |

**O9. When do we ask for reviews or referrals?**
- Answer:

**Done when (Part O is really finished):**
- [ ] The 'wow' moment (O1) is clear and measurable.
- [ ] Support has an inbox, a reply time and at least 10 answered questions (O5).
- [ ] The feedback log (O8) is ready to receive entries.

---

# PART P. MARKETING AND GROWTH (WINNING THE FIRST 500)

**Status:** `[NOT STARTED]`

**P1. Our one-line promise to the customer (headline).**
- Example: "Never lose a plant to thirst again."
- Answer:

**P2. Our story in 3 sentences (problem, solution, proof).**
- Answer:

**P3. Which 2 or 3 channels will we focus on to reach customers? (do few things well)**
- Example: "Reddit communities, short videos, partnerships with plant shops."
- Answer:

**P4. Growth plan from 0 to 500. Fill in how many customers each step should bring.**

| Step | Customers needed | Main channel | Main action | Deadline |
|---|---|---|---|---|
| First 10 (friends, interviews) | 10 | | | |
| 11 to 50 | 40 | | | |
| 51 to 100 | 50 | | | |
| 101 to 250 | 150 | | | |
| 251 to 500 | 250 | | | |

**P5. Website and landing page: link, headline, main button, what we track.**
- Answer:

**P6. Content plan: what we publish, how often, who makes it.**
- Answer:

**P7. Email plan: list size, welcome email, update schedule.**
- Answer:

**P8. Experiments log (one change at a time; keep what works).**

| Date | What we tried | Result (numbers) | Keep / Drop |
|---|---|---|---|
| | | | |

**P9. What is our marketing budget, and how do we measure if it paid off?**
- Answer:

**P10. Rules for AI-made marketing content (who checks facts, tone, and claims before it goes out).**
- Answer:

**Done when (Part P is really finished):**
- [ ] The headline (P1) and story (P2) are written.
- [ ] P4 shows how many customers each step needs.
- [ ] Each chosen channel has a first action and a date.

---

# PART Q. METRICS AND THE 500-CUSTOMER TRACKER

**Status:** `[NOT STARTED]`

**Q1. What is the exact definition of "a customer" for our 500 goal?**
- Example: "A person who paid at least once and used the product in the last 30 days."
- Answer:

**Q2. What numbers do we check every week? (keep to 5 to 8)**

| Metric | Why it matters | Where to see it | Target | Owner |
|---|---|---|---|---|
| New signups | | | | |
| Activation rate (% reaching the "wow" moment) | | | | |
| Paying customers | | | | |
| Weekly active users | | | | |
| Churn | | | | |
| Support tickets | | | | |
| Revenue | | | | |

**Q3. What tools measure this, and is tracking turned on and tested?**
- Answer:

**Q4. Customer milestone tracker (update weekly).**

| Week ending | Signups | Paying customers | Total customers | Revenue | Churned | Notes |
|---|---|---|---|---|---|---|
| | | | | | | |

**Q5. When do we hold a metrics review, and who attends?**
- Answer:

**Q6. What do we do if growth is slower than plan? (our decision rules)**
- Example: "If under 50% of target for 3 weeks, pause new features and talk to 10 lost visitors."
- Answer:

**Done when (Part Q is really finished):**
- [ ] The word 'customer' is defined exactly (Q1).
- [ ] Tracking was tested with a fake signup.
- [ ] The weekly tracker (Q4) has its first row.

---

# PART R. SCALING TO 500 (PERFORMANCE AND COST)

**Status:** `[NOT STARTED]`

**R1. How many users can the product handle today? How do we know (load test result)?**
- Answer:

**R2. What breaks first when we grow? (our best guess) and what is the plan?**
- Answer:

**R3. How do costs change at 100, 250 and 500 customers?**

| Customers | Expected monthly cost | Expected monthly revenue | Profit/Loss |
|---|---|---|---|
| 100 | | | |
| 250 | | | |
| 500 | | | |

**R4. What must be automated before we reach 500? (support replies, onboarding, billing, reports)**
- Answer:

**R5. Do we need help (hire, freelancer, tool) before 500? What and when?**
- Answer:

**Done when (Part R is really finished):**
- [ ] Costs at 100, 250 and 500 customers are estimated.
- [ ] The first thing likely to break (R2) has a plan.
- [ ] Things to automate (R4) have owners.

---

# PART S. COMMUNITY AND PARTNERSHIPS

**Status:** `[NOT STARTED]`

**S1. Who could help us reach customers? (partners, influencers, communities, shops)**

| Name | Why they fit | How we approach | Status | Result |
|---|---|---|---|---|
| | | | | |

**S2. Do we offer a referral or affiliate program? Rules and rewards?**
- Answer:

**S3. Do we have a community space (forum, chat group)? Who manages it?**
- Answer:

**Done when (Part S is really finished):**
- [ ] At least 3 partners or communities are listed.
- [ ] Referral rules (S2) are decided or marked N/A with a reason.

---

# PART T. RUNNING THE PRODUCT (OPERATIONS AND INCIDENTS)

**Status:** `[NOT STARTED]`

**T1. How do we know if the product is broken? (monitoring, alerts, who gets them)**
- Answer:

**T2. Incident plan: steps when something breaks.**
1. Who is on call?
2. How do we tell customers (status page, email)?
3. How do we fix and confirm it is fixed?
4. How do we write what happened and how to prevent it?
- Answer:

**T3. Incident log.**

| Date | What broke | How long | Customers affected | Cause | Fix | Prevention |
|---|---|---|---|---|---|---|
| | | | | | | |

**T4. Regular chores (backups, updates, cost review, security review).**

| Chore | How often | Owner | Last done |
|---|---|---|---|
| | | | |

**T5. Who can access what, and how do we add or remove people?**
- Answer:

**T6. If the main person is away for 2 weeks, who runs things? (bus plan)**
- Answer:

**Done when (Part T is really finished):**
- [ ] Someone gets the alert when the product breaks (T1).
- [ ] The incident steps (T2) were practiced once.
- [ ] Chores in T4 have owners and dates.

---

# PART U. LESSONS LEARNED AND INSTITUTIONAL KNOWLEDGE

**Status:** `[NOT STARTED]`
> This is the part that makes the NEXT project easier. Write it honestly. Nobody gets blamed.

**U1. What went well?**
- Answer:

**U2. What went badly?**
- Answer:

**U3. What surprised us?**
- Answer:

**U4. What would we do differently next time?**
- Answer:

**U5. What should every future project copy from this one?**
- Answer:

**U6. Which parts of this template were confusing or missing? (so the template improves)**
- Answer:

**U7. Reusable assets we made (code pieces, designs, prompts, checklists) and where they live.**

| Asset | What it does | Link | Reuse in next project? |
|---|---|---|---|
| | | | |

**Done when (Part U is really finished):**
- [ ] Every U question has a real answer, not 'nothing'.
- [ ] At least 3 reusable assets are saved (U7).
- [ ] Suggestions to improve this template are written (U6).

---

# PART V. REFERENCE

**Status:** `[NOT STARTED]`

**V1. Glossary (every hard word used in this project, explained simply).**

| Word | Simple meaning |
|---|---|
| MVP | The smallest version that still helps customers |
| Sprint | A short work period, often one week |
| Deploy | Put the product online for others to use |
| Rollback | Undo a release |
| Churn | Customers who leave |

**V2. Important links (one place for all).**

| What | Link | Who can open it |
|---|---|---|
| | | |

**V3. Contacts (people and companies we depend on).**

| Name | Role / company | How to reach | When to contact |
|---|---|---|---|
| | | | |

**V4. Learning resources the team used (docs, courses, articles).**
- Answer:

**Done when (Part V is really finished):**
- [ ] The glossary covers every hard word used.
- [ ] Links and contacts are current.

---

# PART W. HIRING, CONTRACTORS AND TEAM GROWTH

**Status:** `[NOT STARTED]`

**W1. When will we need extra help, and for what? (what hurts most today)**
- Example: "Customer support once we pass 150 customers."
- Answer:

**W2. Roles we may add (job title, what they own, hours, budget).**

| Role | Owns | Hours/week | Budget | Needed by (date or customer count) |
|---|---|---|---|---|
| | | | | |

**W3. How do we find and choose people? (where we post, how we test skills, who decides)**
- Answer:

**W4. Rules for contractors and freelancers.**
- Contract signed before work starts? Who owns the work they make?
- What access do they get (least possible), and how is it removed on the last day?
- Do they follow Part E (AI Working Agreement)?
- Answer:

**W5. New-person day one: what do they read, in what order, and what is their first small task?**
- Example: "Read Quick start, Parts A, E, H. Run the app (H4). First task: fix a tiny bug."
- Answer:

**W6. How do we say goodbye safely? (offboarding checklist: accounts, keys, files, handoff note)**
- Answer:

**Done when (Part W is really finished):**
- [ ] Hiring needs (W1, W2) are tied to customer counts or dates.
- [ ] Contractor rules (W4) are written.
- [ ] A new person could start from W5 alone.

---

# PART X. SEARCH (SEO), LANGUAGES AND ACCESSIBILITY

**Status:** `[NOT STARTED]`

**X1. What words do customers type into Google when they look for us? (list 10)**
- Example: "how often to water a snake plant", "plant care app".
- Answer:

**X2. Page titles and descriptions for the 5 most important pages.**

| Page | Title (under 60 letters) | Description (under 160 letters) | Main search words |
|---|---|---|---|
| | | | |

**X3. Technical search basics: sitemap, page speed, mobile friendly, no broken links. Who checks them and how often?**
- Answer:

**X4. Which languages and countries do we support at launch, and which later?**
- Answer:

**X5. Local formats: date, money, number and time zone rules.**
- Example: "Dates stored in UTC, shown in the customer's time zone. Prices shown in USD at launch."
- Answer:

**X6. Accessibility level we promise (example: WCAG 2.2 level AA) and how we test it.**
- Answer:

**X7. If we have a mobile app: app store name, short description, screenshots, keywords, and review request plan.**
- Answer:

**X8. Consent and tracking: which cookies or trackers do we use, and how do customers say yes or no?**
- Answer:

**Done when (Part X is really finished):**
- [ ] 10 search phrases (X1) are chosen and the top pages have titles (X2).
- [ ] The accessibility promise (X6) is stated and testable.
- [ ] Languages and formats (X4, X5) are decided.

---

# PART Y. AFTER CUSTOMER 500: THE NEXT STAGE

**Status:** `[NOT STARTED]`
> Fill this in when you pass customer 100, and finish it at customer 500. It turns the finish line into the next starting line.

**Y1. What is our next big goal, with a number and a date?**
- Example: "2,000 paying customers by 2028-06-30."
- Answer:

**Y2. Keep, stop, start: what keeps working, what we should stop, what we should begin?**

| Keep | Stop | Start |
|---|---|---|
| | | |

**Y3. What must be fixed BEFORE we grow again? (technical shortcuts from H8, slow support, high costs, risks from F4)**
- Answer:

**Y4. Next 90 days plan.**

| Week range | Goal | Owner | Done when... |
|---|---|---|---|
| Weeks 1-4 | | | |
| Weeks 5-8 | | | |
| Weeks 9-12 | | | |

**Y5. What people and money do we need for the next goal? (see Parts N and W)**
- Answer:

**Y6. Who else could we serve, or what else could we build? (new customer types, new features, new products). Which one do we test first and how?**
- Answer:

**Y7. What would make us pause, sell, or close the product? (our honest exit signals)**
- Answer:

**Y8. Which answers in this file are now old and must be rewritten for the next stage? (list Parts)**
- Answer:

**Done when (Part Y is really finished):**
- [ ] The next goal (Y1) has a number and a date.
- [ ] The next 90 days (Y4) have owners.
- [ ] Things to fix before growing (Y3) are in the roadmap (F2) or the decision log.

---

# APPENDIX A. DECISION LOG

Record every important choice so nobody has to guess "why did we do that?"

| ID | Date | Decision | Options we considered | Why we chose this | Decided by | Revisit on |
|---|---|---|---|---|---|---|
| D-001 | | | | | | |

# APPENDIX B. CHANGE LOG (changes to THIS document)

| Date | Who (human or AI) | Part/Question changed | What changed | Why |
|---|---|---|---|---|
| | | | | |

# APPENDIX C. OPEN QUESTIONS (everything still `TBD` or `DECISION NEEDED`)

| Question number | What is missing | Owner | Due date | Blocks which gate? |
|---|---|---|---|---|
| | | | | |

# APPENDIX D. ASSUMPTIONS TO TEST

| Assumption | How we will test it | Result | Date |
|---|---|---|---|
| | | | |

# APPENDIX E. DOCUMENT HEALTH (is this file trustworthy?)

| Check | Yes/No |
|---|---|
| Every Part has a status tag | |
| No empty Answer lines | |
| No secrets or passwords in this file | |
| Every `TBD` has an owner and date | |
| Links all open | |
| Last full review date is within 30 days | |

# APPENDIX F. READY-TO-GO CHECKLIST

Tick each box only when it is truly true. If any box is unticked, you are not ready for that gate.

**Before building (Gate G1 and G2)**
- [ ] The problem, customer and finish line are written (Parts A, B, C)
- [ ] MVP and "not now" list are agreed (Part D)
- [ ] AI Working Agreement exists, the instructions file (E21) is in the project, and a human has read it (Part E)
- [ ] Team, roadmap and risks are written (Part F)
- [ ] Technology and coding rules are written, and a new person can run the project from H4 (Part H)

**Before launch (Gate G3)**
- [ ] Every Must feature has passing tests (Part K)
- [ ] Security and privacy checks done; backups restore (Part I)
- [ ] Legal papers published and reviewed (Part J)
- [ ] Rollback tested (Part L)
- [ ] Prices, payments, accounting and tax dates are set; a real small payment was tested (Part N)
- [ ] Support inbox, help pages and reply templates ready (Part O)
- [ ] Tracking works and the 500 tracker is set up (Part Q)
- [ ] Launch plan and "stop" signals written (Part M)

**After launch (Gates G4 and G5)**
- [ ] Weekly metrics reviews are happening (Part Q)
- [ ] Feedback and experiments logs are current (Parts O, P)
- [ ] Incident log and chores are current (Part T)
- [ ] 500 customers reached and verified against the definition in Q1
- [ ] Lessons learned written and reusable assets saved (Part U)
- [ ] Next-stage plan written (Part Y)

**Final sign-off**
- Approved by: ______________________  Date: ______________

---

# APPENDIX G. FULL WORKED EXAMPLE: "PlantPal" (a made-up project)

> Everything below is **sample content** so you can see what good answers look like. Names, numbers and links are invented. Delete this whole Appendix in your real project (or keep it in the master template only). Each line uses the real question numbers.

## G-A. Project Passport `[DONE]`
- **A1.** PlantPal
- **A2.** PlantPal reminds you when to water each of your plants, so they stop dying.
- **A3.** Sam Lee, founder and final decision-maker, sam@example.com
- **A4.** Mobile app (iPhone and Android) plus a small marketing website
- **A5.** Phase 1, Planning and Scope
- **A6.** Started 2026-10-19. Public launch target 2027-02-01.
- **A7.** 500 paying customers who each marked at least one plant as watered, by 2027-08-31.
- **A8.** Code: github.com/example/plantpal. Design: Figma "PlantPal v1". Tasks: Notion board "PlantPal Sprint". Support inbox: help@plantpal.example.
- **A9.** G0 passed 2026-11-02, approved by Sam. G1 to G5 not yet.

## G-B. Idea and Problem `[DONE]`
- **B1.** Maria buys plants but forgets to water them. Three died last year. She feels bad and wastes about $60 a year.
- **B2.** Phone alarms, sticky notes, or memory.
- **B3.** Alarms do not know which plant needs water, and watering needs change by season.
- **B4.** An app that knows each plant, says when and how much to water, and adapts to the season.
- **B5.** Reminders use the plant's type, pot size and room light, not one-size-fits-all timers.
- **B6.** Sam worked 5 years in a garden store and answered "why is my plant dying" daily.
- **B7.** Talked to 12 plant owners. 9 said they lose plants from forgetting. 7 said they would pay $3 to $6 per month.
- **B8.** Stop if, after 30 interviews, fewer than 5 would pay.
- **B9.** The most trusted plant-care companion, used by 100,000 homes in 3 years.

## G-C. Customers and Market `[DONE]`
- **C1.** Maria, 29, office worker, apartment, 8 plants, shops at local garden centers, uses her phone for everything.
- **C2.** Instagram plant groups, Reddit r/houseplants, garden centers.
- **C3.** Easy to set up, does not nag, trustworthy plant advice.
- **C4.** Competitors: (1) "LeafLog" (example): strong plant database, weak reminders, $4/month. (2) "WaterMe" (example): simple reminders, no plant knowledge, free with ads. (3) Phone alarms: free, but not plant-specific.
- **C5.** About 20 million US houseplant owners (source: example industry survey, 2025).
- **C6.** Commercial greenhouses and farms. Not our customer.
- **C7.** 12 interviews logged between 2026-10-05 and 2026-10-18. Biggest learning: people want one daily summary, not many alerts.

## G-D. Scope and Requirements `[DONE]`
- **D1.** Add plants, get a watering reminder, mark as watered.
- **D2.** F1 Add a plant (Must; done when a plant appears in the list within 3 taps). F2 Daily reminder (Must; done when a push arrives at the chosen time). F3 Mark as watered (Must; done when next reminder date updates). F4 Plant photo (Could). F5 Social sharing (Won't, now).
- **D3.** Not in v1: social features, plant disease scanner, shop, smart-sensor support.
- **D4.** "As a plant owner, I want a daily reminder, so that my plants do not die."
- **D5.** Screens open in under 2 seconds. Works offline for viewing. Text can be enlarged. Works on iOS 17+ and Android 13+.
- **D6.** Assumption: people will allow notifications. Test: onboarding test with 20 beta users.
- **D7.** Budget $5,000. Launch by 2027-02-01. No health or medical claims.

## G-E. AI Working Agreement `[DONE]`
- **E1.** Claude (chat): research, writing, planning. Claude Code: writes and tests code on branches. Both used by Sam and Priya only.
- **E2.** Green: write code on a branch, write tests, draft help pages, summarize research.
- **E3.** Yellow (ask first): add new libraries, change the database layout, send any email, change any price.
- **E4.** Red (never): delete data, publish to customers, touch payment or legal pages, read secret keys, push to main.
- **E5.** Merge to main: Priya (pull request review). Release: Sam (message "approved v1.0.0"). Spending: Sam. Prices and legal text: Sam. Customer data changes: Sam.
- **E6.** `CLAUDE.md` in the repo root says: read Knowledge_Base.md Parts A, E, H first, then the task brief.
- **E7.** Prompt library kept in `docs/prompts.md`. Best one: "Plan feature F2 in 5 small tasks, each with a done-when test."
- **E8.** Human reads every AI change. Tests pass. No secrets. Matches Part H rules.
- **E9.** Dates are always UTC. We use the new payment API only (the old one is retired).
- **E10.** N/A, because: v1 has no AI inside the product. Revisit at v1.2 for a "diagnose my plant" idea.
- **E11.** Every AI pull request has a "What the AI did" note. Session notes in `docs/session-notes.md`.
- **E12.** Planner, Builder, Reviewer, Tester roles are used. Priya checks Reviewer output.
- **E13.** Task brief template used as written. We added a line: "Link the question number you are following."
- **E14.** Read order: CLAUDE.md, Knowledge_Base.md Parts A, E, H, the task brief, `docs/session-notes.md`. Write 5 lines of notes at the end.
- **E15.** Handoff notes live at the bottom of `docs/session-notes.md`.
- **E16.** Stop, write the missing fact as a question with 2 options, wait for a human.
- **E17.** Target: 70% of AI changes merged with fewer than 3 edits; under 2 AI-caused bugs per month.
- **E18.** AI budget $60 per month. Sam is told at $48. At $60 coding agent runs are paused.
- **E19.** 2026-12-05: AI changed a date format to local time. Rule added to E9 and H5.
- **E20.** First Monday of each month, Sam.
- **E21.** `CLAUDE.md` in the repo root, 25 lines, last checked 2027-01-04, only Sam and Priya may edit.
- **E22.** Allow: edit files in `app/` and `api/`, run tests. Ask first: install new libraries, change database layout. Block: delete files outside the project, read key files, push to main. Automatic check: tests and style check run after each change. Helpers: Planner, Builder, Reviewer, Tester. Settings file is shared in the repo; only Sam changes it. Red list tested on 2027-01-05 by asking Claude to push to main (it was blocked).

## G-F. Plan, People and Risks `[DONE]`
- **F1.** Sam: product and money. Priya: code review and releases (10 hours a week). Claude: planning, drafts, code on branches.
- **F2.** Idea approved 2026-11-02. Plan approved 2026-11-16. First working version 2027-01-04. Testing finished 2027-01-20. Public launch 2027-02-01. 100 customers 2027-04-15. 500 customers 2027-08-31.
- **F3.** One-week sprints, Notion board, 15-minute check-in every Monday.
- **F4.** Top risks: (1) Few people allow notifications (Medium/High; test in beta; Sam). (2) App store review delay (Medium/Medium; submit 3 weeks early; Priya). (3) AI-written bug in reminders (Medium/High; tests plus human review; Priya).
- **F5.** Plan B: launch web version first and add the app 4 weeks later.
- **F6.** Every real choice goes into Appendix A with options and reasons.

## G-G. Design and User Experience `[DONE]`
- **G1.** Calm, friendly, simple.
- **G2.** Green #2E7D32, cream #FAF7F0, font Inter, voice: warm and short, no jargon.
- **G3.** Screens: Welcome, Add plant, Plant list, Plant detail, Today (daily summary), Settings. Designs linked in Figma.
- **G4.** Sees ad, installs app, adds first plant in under 60 seconds, gets first reminder next morning, taps "watered," sees the next date.
- **G5.** Contrast checked, tap targets at least 44 px, works with screen readers, text can be enlarged.
- **G6.** All words kept in `copy.md` in the repo.

## G-H. Technology `[DONE]`
- **H1.** Front end: React Native 0.76. Back end: Node 22 with a small API. Database: PostgreSQL 16 on Supabase. Hosting: Supabase plus Vercel (website). Login: email link. Payments: a payment provider (Stripe-style). Email: a transactional email service. Monitoring: an error tracker. About $90 per month at launch.
- **H2.** App talks to the API. API talks to the database and to the push-notification service.
- **H3.** Repo `github.com/example/plantpal`. Folders: `app/`, `api/`, `docs/`.
- **H4.** 1) Install Node 22. 2) `npm install`. 3) Copy `.env.example` to `.env` and ask Sam for test values. 4) `npm run dev`. 5) Open the simulator.
- **H5.** Names: `camelCase`. Lint: ESLint. Commit message: "feat: short description (F2)". Branches: `feature/f2-reminders`. Max change: about 300 lines.
- **H6.** Supabase (data) key in password manager vault "PlantPal", rotated by Sam. Payment provider key in the same vault, rotated by Sam. Push service key same vault.
- **H7.** Do not touch without asking: payment code, login code, database migrations.
- **H8.** Reminder time zones use a quick fix. Real fix due in v1.1.

## G-I. Data, Privacy and Security `[DONE]`
- **I1.** Email, first name, plant list, notification time zone. Card details are handled by the payment provider only.
- **I2.** Email to log in. Plant list to give reminders. Time zone so reminders arrive at the right hour.
- **I3.** Stored in Supabase (EU region), visible only to Sam and Priya, kept until the customer deletes their account, then erased within 30 days.
- **I4.** Encrypted in transit and at rest. Two-step login for the team. Row-level rules so customers see only their own plants.
- **I5.** Daily backups, restore test done 2027-01-10.
- **I6.** All checks passed on 2027-01-12.
- **I7.** Tell Sam at once. Tell affected customers within 72 hours. Steps in `docs/leak-plan.md`.

## G-J. Legal and Compliance `[DONE]`
- **J1.** Company in Delaware, USA. Customers in the USA and EU at launch.
- **J2.** Terms, Privacy Policy, Cookie notice, Refund policy all published, reviewed by a lawyer on 2027-01-15. Open-source license list in `docs/licenses.md`.
- **J3.** GDPR (EU customers) and CCPA (California) apply. Not a health product. Not for children under 13.
- **J4.** The company owns the code, the name and the content. Trademark search started 2026-11-20.
- **J5.** AI-written code is reviewed by a human and covered by the company's ownership policy (confirmed by the lawyer).
- **J6.** LLC formed, bank account open, tax ID registered.

## G-K. Testing and Quality `[DONE]`
- **K1.** All Must features pass, no known crashes on the main journey, screens open in under 2 seconds.
- **K2.** Unit and integration tests run on every change. End-to-end tests run before each release. Accessibility check by Priya before launch.
- **K3.** F1: open app, tap Add plant, choose "Snake plant" (expected: plant appears in the list within 3 taps). F2: set time 08:00 (expected: push arrives at 08:00 local time). F3: tap "Watered" (expected: next date moves forward).
- **K4.** iPhone 12 and newer, 3 Android phones, small and large screens.
- **K5.** Critical = customers blocked, fix today. High = fix this week. Low = when time allows.
- **K6.** 20 beta users for 2 weeks. We ask: "Did you get your reminder on time?" and "What confused you?"
- **K7.** Humans read every AI-written test and run it against a deliberately broken change to prove it can fail.

## G-L. Build, Release and Deployment `[DONE]`
- **L1.** Local, Staging, Live. Only Live has real customer data.
- **L2.** Branch, pull request, review by Priya, tests pass, merge, auto-deploy to staging, Sam approves, release to stores.
- **L3.** Standard checklist used on every release.
- **L4.** Staging rollback by redeploying the last good version. Live app: switch off the new feature flag, then submit the previous build. Priya does it.
- **L5.** v1.0.0 launch, v1.1.0 new feature, v1.0.1 bug fix.
- **L6.** Apple and Google developer accounts under the company. Review takes 1 to 3 days, so submit 3 weeks early.
- **L7.** v1.0.0 released 2027-02-01, no problems.

## G-M. Launch Plan `[DONE]`
- **M1.** Invite-only for week 1, then public.
- **M2.** 8 weeks before: landing page live. 4 weeks before: beta finished. 1 week before: support inbox and help pages ready. Launch day: announcement. 1 week after: first review of numbers. 4 weeks after: lessons note.
- **M3.** Email list (target 300 people), two plant communities, personal social posts.
- **M4.** Sam watches signups, Priya watches errors, Claude drafts replies, Sam sends. Either of them can say "stop."
- **M5.** Day 1: 50 signups. Day 7: 150. Day 30: 300.
- **M6.** Pause if more than 5% of signups fail or payments fail twice in a row.

## G-N. Pricing, Money and Payments `[DONE]`
- **N1.** Monthly or yearly subscription.
- **N2.** Free (3 plants), Plus $4.99/month (unlimited plants), Plus Yearly $39/year.
- **N3.** Competitors charge $4 to $6. 7 of 12 interviewees named $3 to $6.
- **N4.** Servers $60, tools $30, AI $60, email $10, total $160 per month.
- **N5.** $160 divided by $4.99 is about 33 paying customers to cover costs.
- **N6.** $5,000 budget, about 9 months of runway at launch costs.
- **N7.** Payments through the provider. Refund within 14 days, no questions asked. Failed payments retried 3 times.
- **N8.** 14-day free trial of Plus. No other discounts at launch.
- **N9.** Targets at 500: MRR about $2,500, CAC under $12, churn under 5% per month, LTV above $60.
- **N10.** Simple online accounting tool, updated by Sam every Friday.
- **N11.** US income tax filed by the accountant each year; sales tax collected by the payment provider; EU VAT handled by the provider. Dates in the shared calendar.
- **N12.** Customers get a receipt by email; copies are in the payment dashboard and exported monthly to the accounting tool.
- **N13.** Up to $50 anyone; above $50 Sam; above $500 Sam plus Priya.
- **N14.** Founder savings ($5,000) and customer revenue. No investors yet. No grants.
- **N15.** 2027-02: money in $190, money out $160, cash left $4,540, runway about 28 months at current spend.

## G-O. Onboarding, Support and Feedback `[DONE]`
- **O1.** The first correct watering reminder arrives and the customer taps "Watered."
- **O2.** Install, sign in with email link, add one plant, set a time. Goal: under 2 minutes.
- **O3.** Email and a help page. No chat at launch.
- **O4.** Reply within 24 hours on weekdays. Claude drafts, Sam sends.
- **O5.** Example: "Why did my reminder come late?" Answer: "Check your phone's time zone and notification settings. Steps here: (help page link)."
- **O6.** Templates in `docs/replies.md` for thanks, bug found, refund, cannot log in.
- **O7.** In-app "How are we doing?" button and a 3-question email after 14 days. Review every Friday.
- **O8.** 2027-02-05: "Want to name my plants." Decision: later. Reason: nice, not needed.
- **O9.** Ask for an app store review after the customer marks 5 waterings.

## G-P. Marketing and Growth `[DONE]`
- **P1.** "Never lose a plant to thirst again."
- **P2.** People forget to water plants. PlantPal knows each plant and reminds you at the right time. In our beta, 85% of reminders were on time.
- **P3.** Plant communities, short videos, partnerships with garden centers.
- **P4.** First 10: friends and interviewees. 11 to 50: posts in two plant communities. 51 to 100: garden-center partnership flyers. 101 to 250: short videos and referrals. 251 to 500: search pages and reviews.
- **P5.** plantpal.example, headline P1, button "Try free for 14 days," tracked: visits and signups.
- **P6.** 2 short videos and 1 article per week. Priya edits, Claude drafts, Sam approves.
- **P7.** Welcome email on signup, a monthly "plant tip" email.
- **P8.** 2027-02-12: tried video vs photo post. Video brought 3x clicks. Keep video.
- **P9.** $300 per month. Success: CAC under $12.
- **P10.** Claude drafts, Sam checks every fact and claim. No health or "guaranteed" claims.

## G-Q. Metrics and the 500-Customer Tracker `[DONE]`
- **Q1.** A person who paid at least once and marked a plant as watered in the last 30 days.
- **Q2.** Weekly numbers: signups, activation rate, paying customers, weekly active users, churn, support tickets, revenue.
- **Q3.** Analytics tool and payment dashboard. Tested with fake signups on 2027-01-20.
- **Q4.** Week ending 2027-02-07: signups 160, paying 41, total customers 41, revenue $190, churned 0.
- **Q5.** Every Monday, Sam and Priya, 20 minutes.
- **Q6.** If under 50% of target for 3 weeks: pause new features and interview 10 people who did not sign up.

## G-R. Scaling to 500 `[DONE]`
- **R1.** Load test on 2027-01-18 handled 2,000 users at once.
- **R2.** Push notification volume at 8:00 AM. Plan: spread sending over 15 minutes.
- **R3.** 100 customers: cost $180, revenue $500. 250: cost $240, revenue $1,250. 500: cost $400, revenue $2,500.
- **R4.** Automate: welcome email, failed-payment emails, weekly numbers report.
- **R5.** Part-time support helper at about 150 customers (see Part W).

## G-S. Community and Partnerships `[DONE]`
- **S1.** Green Leaf Garden Center: flyers at checkout, invited 2027-03-01.
- **S2.** Referral: both people get one free month.
- **S3.** Private community group, managed by Sam.

## G-T. Running the Product `[DONE]`
- **T1.** Error tracker and uptime monitor alert Priya's phone.
- **T2.** Priya is on call. Status page and email tell customers. Fix, confirm, then write a short report within 2 days.
- **T3.** 2027-03-02: reminders delayed 40 minutes. 120 customers affected. Cause: push service limit. Fix: slower send. Prevention: R2 plan.
- **T4.** Backups checked monthly. Updates monthly. Cost review monthly. Security review quarterly.
- **T5.** Only Sam and Priya have access. Anyone joining or leaving follows W5 and W6.
- **T6.** Priya runs the product when Sam is away. Sam when Priya is away.

## G-U. Lessons Learned `[DONE]`
- **U1.** Interviewing 12 people before building saved months.
- **U2.** We built the plant photo feature too early.
- **U3.** More people paid yearly than we expected.
- **U4.** Start beta 2 weeks earlier.
- **U5.** Keep Part E and the handoff notes. They made AI work safe.
- **U6.** The template needed a simpler money section (now fixed).
- **U7.** Reusable: prompt library, release checklist, leak plan, reply templates.

## G-V to G-X. Reference, Hiring, Search `[DONE]`
- **V1.** Glossary has 20 words. Links and contacts are in the project folder.
- **W1.** Need support help when customers pass 150.
- **W2.** Part-time support helper, 10 hours per week, $400 per month, needed at 150 customers.
- **W3.** Post in two communities, 30-minute paid trial task, Sam decides.
- **W4.** Signed contract first. Company owns all work. Access limited to the support inbox. Access removed on the last day. They follow Part E.
- **W5.** Read Quick start, then Parts A, E and H. Run the app (H4). First task: fix one tiny bug.
- **W6.** Offboarding checklist: remove accounts, rotate shared keys, collect handoff note.
- **X1.** "how often to water a snake plant", "plant care app", "plant watering reminder", and 7 more.
- **X2.** Home: "PlantPal: Plant Watering Reminders" / "Never lose a plant to thirst again. Free for 3 plants." / main words: plant watering reminder.
- **X3.** Sitemap submitted, page speed under 2 seconds, broken-link check monthly by Priya.
- **X4.** English at launch. Spanish in v1.3.
- **X5.** Dates stored in UTC, shown in the customer's time zone. Prices in USD at launch.
- **X6.** WCAG 2.2 level AA, tested with a screen reader before each release.
- **X7.** App store name "PlantPal: Plant Reminders," keywords chosen, 5 screenshots, review request after 5 waterings.
- **X8.** Only privacy-friendly analytics and essential cookies. Customers can say no in the cookie banner.

## G-Y. After Customer 500 `[DONE]`
- **Y1.** 2,000 paying customers by 2028-06-30.
- **Y2.** Keep: videos and referrals. Stop: paid ads (CAC too high). Start: yearly plan push and garden-center partnerships.
- **Y3.** Fix the time-zone shortcut (H8) and automate failed-payment emails (R4) first.
- **Y4.** Weeks 1-4: fix shortcuts. Weeks 5-8: Spanish version. Weeks 9-12: partner program.
- **Y5.** One part-time support helper (W2) and $400 per month for them.
- **Y6.** Test a "gift a plant plan" idea with 20 customers first.
- **Y7.** Pause if churn stays above 8% per month for 3 months.
- **Y8.** Parts F, P and Q are rewritten for the next goal.

> End of worked example.
