# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **Template:** Go-to-Market (GTM) Plan, AI-Driven Development Life Cycle
> **Template version:** 1.1.0
> **Save this file as:** `Go_To_Market_Plan.md`
> **Folder:** `Launch, marketing and customer acquisition/`
> **Goal of this document:** Take a software product from "built with AI" to "500 real people actively using it", with no guessing.
> **Works for:** Solo founders and indie builders (one person wearing every hat). Teams can use it too.

---

## 0.1 What is this document? (Plain English)

Think of a lemonade stand. Before you open, you decide:

- Who will buy it? (customers)
- Why will they pick yours? (value)
- How much does it cost? (price)
- Where do you put the stand? (channels)
- How will people hear about it? (marketing)
- How do you know it is working? (numbers)

A **Go-to-Market Plan** answers those same questions for your software. This file is a **questionnaire**. You answer the questions, and at the end you have a complete plan.

## 0.2 How to fill it in (5 simple steps)

1. **Copy this file** into your new project's folder. Never write in the original template.
2. **Fill the header** in Section 1 (project name, dates, owner).
3. **Go top to bottom.** Answer every question on the line that starts with `> ANSWER:`.
4. **Use the example** under each question as a guide. Replace it with YOUR answer. Do not copy the example.
5. **Tick the gates.** At the end of each phase there is a checklist. Only move to the next phase when every box is ticked (or you wrote why a box does not apply).

## 0.3 The 7 golden rules

| # | Rule | Why |
|---|------|-----|
| 1 | **Never leave a blank.** Write your answer, `N/A - because ...`, or `UNKNOWN - will find out by [date]`. | Blanks cause guessing. |
| 2 | **Use numbers, not feelings.** "Many users" is bad. "300 users" is good. | Numbers can be checked. |
| 3 | **One question, one answer.** Keep answers short (1-3 sentences) unless asked for a list. | Short answers are easier to review. |
| 4 | **Write facts, mark guesses.** If you are not sure, add `(ASSUMPTION)` after it. | Later you will test every assumption. |
| 5 | **Add a date and a source** to any fact from outside (for example, "Source: competitor pricing page, 2026-10-18"). | Facts get old. |
| 6 | **Do not delete questions.** Mark them `N/A - because ...` instead. | Keeps every project's file the same shape. |
| 7 | **A human approves every phase gate.** AI can draft; a person signs off. | AI can sound sure and still be wrong. |

## 0.4 The symbols used in this file

| Symbol | Meaning |
|--------|---------|
| `> ANSWER:` | Type your answer on this line (or below it). |
| `EXAMPLE:` | A sample answer. Learn from it, then replace it. |
| `WHY:` | One line on why the question matters. |
| `AI PROMPT:` | A ready-to-paste instruction for an AI agent to help you answer. |
| `[ ]` / `[x]` | Not done / done. |
| `(ASSUMPTION)` | You believe it but have not proven it. |
| `(VERIFIED)` | You checked it with real evidence. |
| `{{double braces}}` | A placeholder you must replace. |
| `GATE` | A checkpoint. Do not pass until it is satisfied. |

## 0.5 How to use the "AI PROMPT" blocks

1. Copy the text inside the `AI PROMPT:` block.
2. Paste it into your AI assistant.
3. Replace every `{{placeholder}}` with your real details first.
4. Read what the AI says. **Check every fact.** AI can invent numbers and competitors.
5. Paste the improved answer into `> ANSWER:`. Mark anything unchecked as `(ASSUMPTION)`.

## 0.6 Quick-start version (15 minutes)

In a hurry? Fill only these items first: 1.1 to 1.6, 2.1 to 2.4, 4.1, 5.1, 8.1, 9.1, 15.1. Then come back for the rest. The plan is not "done" until the Final Review (Section 22) passes.

## 0.7 What "done" looks like

- Every question has an answer, `N/A`, or `UNKNOWN` with a date.
- Every gate in every phase is ticked or explained.
- The Final Review score (Section 22) is **90 or higher out of 100**.
- A stranger could read the file and run your launch without asking you a single question.

---

# TABLE OF CONTENTS

1. Project Identity and Document Control
2. AI-Agent Operating Rules
3. The Big Picture: Goal, Lifecycle and Gates
4. Customer and Problem
5. Market and Competitors
6. Positioning and Messaging
7. Pricing and Packaging
8. Product Readiness (AI-Driven Development)
9. Phase 1: BUILD
10. Phase 2: TEST
11. Phase 3: PRE-LAUNCH
12. Phase 4: LAUNCH
13. Phase 5: EARLY GROWTH (Users 1 to 100)
14. Phase 6: SCALE TO 500
15. Channels and Customer Acquisition
    - 15A. Mobile App Store Launch
    - 15B. B2B Sales (Selling to Businesses)
    - 15C. Community Building
16. Funnel Math (How Many People You Need)
17. Onboarding, Activation and Retention
18. Support and Feedback
19. Budget and Resources
20. Metrics and Tracking
21. Legal, Privacy and Compliance
22. Risk Register
23. Timeline and Owners
24. Decision Log and Change Log
25. Final Review and Sign-Off
26. Glossary
27. Appendix A: AI Prompt Library
28. Appendix B: Filled-In Mini Example
29. Appendix C: Troubleshooting ("What if...?")
30. Appendix D: Ready-to-Use Tracking Tables

---

# 1. PROJECT IDENTITY AND DOCUMENT CONTROL

> **WHY THIS SECTION EXISTS:** So anyone (including future you) knows what this file is about, who owns it, and whether it is current.

## 1.1 Project name
**WHY:** One official name stops confusion.
**EXAMPLE:** `PlantPal`
> ANSWER:

## 1.2 One-sentence description (max 25 words)
**WHY:** If you cannot explain it in one sentence, customers cannot either.
**EXAMPLE:** `PlantPal is a phone app that reminds busy people when to water each houseplant.`
> ANSWER:

## 1.3 Product type
**WHY:** Different types need different launch paths.
Tick one:
- [ ] Web app (SaaS)
- [ ] Mobile app (iOS / Android)
- [ ] Desktop app
- [ ] API / developer tool
- [ ] Browser extension / plugin
- [ ] AI agent / AI-powered tool
- [ ] Other: {{describe}}

## 1.4 Business model
Tick one:
- [ ] Free (no money)
- [ ] Freemium (free plan + paid plan)
- [ ] Free trial then paid
- [ ] Paid only
- [ ] Usage-based (pay for what you use)
- [ ] Other: {{describe}}

## 1.5 Document owner (the ONE person accountable)
**EXAMPLE:** `Sam Lee, sam@example.com`
> ANSWER:

## 1.6 Project dates

| Item | Date (YYYY-MM-DD) |
|------|-------------------|
| Development start | |
| Planned private test start | |
| Planned public launch | |
| Date I expect to reach 500 active users | |
| Today (date you started this file) | |

## 1.7 Where are the other project files?
**WHY:** This plan connects to other documents. List them so nobody hunts.
| Document | Link or path |
|----------|--------------|
| Product Requirements (PRD) | |
| Architecture / tech design | |
| Test plan | |
| Brand and logo files | |
| Analytics dashboard | |
| Customer feedback tracker | |

## 1.8 Document status
Tick one:
- [ ] Draft (still filling in)
- [ ] In review
- [ ] Approved
- [ ] Out of date (needs refresh)

## 1.9 Version history
| Version | Date | Who changed it | What changed |
|---------|------|----------------|--------------|
| 0.1 | | | First draft |

---

# 2. AI-AGENT OPERATING RULES

> **WHY THIS SECTION EXISTS:** If an AI agent reads or helps fill this file, these rules keep it honest and safe. Humans: you can skim this section. AI agents: you MUST obey it.

## 2.1 Rules for AI agents (mandatory)

1. **Do not invent facts.** If a number, price, competitor, law or statistic is not in this file or a source the human provided, write `UNKNOWN` and say how to find it.
2. **Cite sources.** Every outside fact needs a source and a date.
3. **Label guesses.** Add `(ASSUMPTION)` to anything unproven.
4. **Do not skip questions.** Answer, mark `N/A - because ...`, or mark `UNKNOWN - will find out by [date]`.
5. **Keep the structure.** Do not rename, delete or reorder sections or questions.
6. **Ask when unclear.** If a question cannot be answered from provided info, ask the human. Do not guess.
7. **Never approve a gate.** Only a human can tick a GATE box.
8. **Never publish, send or spend.** Do not post content, send emails, buy ads or move money without explicit human approval for that exact action.
9. **Protect private data.** Do not put passwords, API keys, personal data or customer lists in this file. Use `{{SECRET}}` placeholders.
10. **Stay consistent.** Numbers in one section must match the same numbers elsewhere (price, targets, dates). Flag any mismatch.
11. **Be plain.** Use short sentences. Define any term that a 10-year-old would not know.
12. **Show your work.** For any calculation, show the formula and inputs.

## 2.2 Human review checklist (after any AI edit)
- [ ] I read every sentence the AI wrote.
- [ ] I checked every number and every outside fact.
- [ ] I removed anything that sounds good but is not true.
- [ ] All guesses are labeled `(ASSUMPTION)`.
- [ ] No secrets or private data were pasted in.

## 2.3 Which AI tools are you using for this project?
**WHY:** Tools differ in limits, cost and data-privacy rules.
| Task | AI tool / agent | Who reviews its output |
|------|-----------------|------------------------|
| Writing code | | |
| Writing marketing copy | | |
| Research (market, competitors) | | |
| Testing / QA | | |
| Customer support drafts | | |
| Analytics summaries | | |

## 2.4 What must a human ALWAYS do (never AI alone)?
Tick all that apply, and add your own:
- [ ] Approve pricing
- [ ] Approve legal text (terms, privacy policy)
- [ ] Approve any public post or announcement
- [ ] Approve any spending above ${{amount}}
- [ ] Reply to angry or sensitive customer messages
- [ ] Approve the production release
- [ ] {{your own rule}}

---

# 3. THE BIG PICTURE: GOAL, LIFECYCLE AND GATES

> **WHY THIS SECTION EXISTS:** This is the map. It shows the road from "idea built" to "500 active users".

## 3.1 The one goal of this plan
**Reach 500 active users.**

## 3.2 Define "active user" (be exact)
**WHY:** If "active" is vague, you will fool yourself about progress.
**RECOMMENDED DEFAULT:** *A person who signed up AND completed the key action at least once in the last 30 days.*
**EXAMPLE:** `A person who signed up and added at least 1 plant in the last 30 days.`
> ANSWER (Key action = {{what}}; time window = {{days}}):

## 3.3 How will you count it? (one source of truth)
**EXAMPLE:** `Analytics tool "X", dashboard "Active Users", counted weekly on Mondays.`
> ANSWER:

## 3.4 Why 500?
**WHY:** 500 is big enough to see real patterns and small enough to reach without a big team.
> ANSWER (what will 500 prove or unlock for you?):

## 3.5 The 6 phases at a glance

| Phase | Name | Plain-English goal | Done when (exit gate) |
|-------|------|--------------------|-----------------------|
| 1 | BUILD | Make the product work | Core features work; no critical bugs |
| 2 | TEST | Make sure real people can use it | Test users succeed without help |
| 3 | PRE-LAUNCH | Get ready and gather interested people | Waitlist + launch assets ready |
| 4 | LAUNCH | Open the doors | Product live; first users arriving |
| 5 | EARLY GROWTH | Get users 1 to 100 and learn | 100 active users; clear best channel |
| 6 | SCALE TO 500 | Repeat what works | 500 active users; steady growth |

## 3.6 How AI helps in each phase
| Phase | Where AI helps | Where a human must decide |
|-------|----------------|---------------------------|
| 1 BUILD | Write code, tests, docs | What to build, security review |
| 2 TEST | Generate test cases, find bugs | Is it good enough to ship? |
| 3 PRE-LAUNCH | Draft copy, landing page, emails | Message, tone, brand |
| 4 LAUNCH | Schedule content, monitor errors | Go / no-go, public posts |
| 5 EARLY GROWTH | Analyze feedback, suggest fixes | Which fixes to make |
| 6 SCALE | Automate support, reports, outreach drafts | Spend, strategy, hiring |

## 3.7 How does a phase end? (The Gate Rule)
- Each phase ends with a **GATE** checklist.
- Every box must be `[x]` or marked `N/A - because ...`.
- A **human** writes their name and date to pass the gate.
- If a gate fails, stay in the phase. Write what is missing in the Decision Log (Section 24).

## 3.8 What counts as "stuck"?
**WHY:** Knowing when to change plans prevents wasted months.
> ANSWER (If a phase takes longer than {{X}} weeks past plan, I will {{action}}):

## 3.9 AI agent workflow map (who does what, and who hands off to whom)

> **WHY:** In an AI-driven life cycle, different AI "agents" (or different AI prompts) do different jobs. This table stops two agents doing the same job, and stops jobs falling through the cracks. **Solo founder:** you are the human in every row. **Rule:** every handoff ends with a human check before anything public, paid or permanent.

### 3.9.1 Agent roles
Fill in the tool or agent name you use for each role. Write `N/A - because ...` if a role is not used.

| Agent role | Its job in plain words | Tool / agent name | What it may do alone | What needs a human OK |
|------------|------------------------|-------------------|----------------------|------------------------|
| Planner | Breaks goals into small tasks | | Draft task lists | Approve the plan |
| Researcher | Finds facts about customers and competitors | | Gather and summarize with sources | Decide what is true |
| Builder (coder) | Writes and changes code | | Write code in a branch | Merge to main |
| Tester (QA) | Writes and runs tests, finds bugs | | Run tests, report bugs | Mark a bug "won't fix" |
| Security checker | Looks for obvious security holes | | Scan and report | Accept any risk |
| Writer (marketing) | Drafts copy, emails, posts | | Draft only | Publish or send anything |
| Analyst | Reads the numbers and explains them | | Summarize metrics | Change targets or strategy |
| Support helper | Drafts replies to user messages | | Draft replies, tag topics | Send sensitive replies |
| Release helper | Prepares release notes and checklists | | Prepare | Press the "go live" button |
| Reviewer (independent) | Checks another agent's work for mistakes | | Flag problems | Final sign-off |

### 3.9.2 Handoff map (what each agent passes to the next)
| Phase | From (agent) | To (agent) | What is handed over (the "package") | Human check before handoff? |
|-------|--------------|------------|--------------------------------------|------------------------------|
| 1 BUILD | Planner | Builder | Task list and acceptance rules | Yes |
| 1 BUILD | Builder | Tester | Code branch + what to test | Yes |
| 2 TEST | Tester | Builder | Bug list with steps to repeat | No (automatic) |
| 2 TEST | Tester | Release helper | Test report | Yes |
| 3 PRE-LAUNCH | Researcher | Writer | Customer quotes and facts with sources | Yes |
| 3 PRE-LAUNCH | Writer | Human | Draft copy, emails, posts | Yes (always) |
| 4 LAUNCH | Release helper | Human | Release checklist and rollback steps | Yes (always) |
| 4 LAUNCH | Support helper | Human | Draft replies for sensitive messages | Yes |
| 5-6 GROWTH | Analyst | Planner | Weekly findings and ideas | Yes |
| 5-6 GROWTH | Planner | Builder / Writer | Next week's tasks | Yes |

### 3.9.3 Rules for agent handoffs
- [ ] Every handoff package is written down (a file, a ticket or a note). Nothing lives only in a chat.
- [ ] The receiving agent restates the task in its own words before starting.
- [ ] An agent never reviews its own work. Another agent or a human does.
- [ ] If an agent is unsure, it asks the human instead of guessing.
- [ ] Every agent action that spends money, sends messages or changes live data is logged in the Decision Log (Section 24).
- [ ] If two agents disagree, the human decides and writes down why.

### 3.9.4 Where is the shared "source of truth"?
> ANSWER (the ONE place all agents read the current plan, for example this file's path: {{path}}):

---

# 4. CUSTOMER AND PROBLEM

> **WHY THIS SECTION EXISTS:** Products fail when they solve a problem nobody has. Start here.

## 4.1 Who has the problem? (your ideal customer)
Describe ONE specific type of person or business. "Everyone" is not allowed.
**EXAMPLE:** `Busy people aged 25-40 in apartments who own 3+ houseplants and keep killing them.`
> ANSWER:

## 4.2 Customer profile card
| Field | Your answer |
|-------|-------------|
| Job or role | |
| Age range (or company size if business) | |
| Location / language | |
| Tools they already use | |
| How tech-savvy (low / medium / high) | |
| Where they spend time online | |
| Who influences their buying (friend, boss, reviewer) | |
| Typical budget they have for this | |

## 4.3 What problem do they have? (in THEIR words)
**WHY:** The best marketing copy is the customer's own words.
**EXAMPLE:** `"I always forget to water my plants and they die."`
> ANSWER (write 3 real quotes if possible, with where you heard them):

## 4.4 How painful is the problem? (1 to 10)
| Score | Meaning |
|-------|---------|
| 1-3 | Mild annoyance. People will not pay or switch. |
| 4-6 | Real pain. Some will try something new. |
| 7-10 | Severe. People actively search for a fix. |
> ANSWER (score + why):

## 4.5 What do they do today instead? (current alternatives)
**EXAMPLE:** `Sticky notes, phone alarms, guessing.`
> ANSWER:

## 4.6 What does the problem cost them? (time, money, stress)
> ANSWER (use numbers if you can):

## 4.7 "Jobs to be done"
Fill in the blank:
**"When ____ (situation), I want to ____ (action), so I can ____ (result)."**
> ANSWER:

## 4.8 Evidence that this problem is real
**WHY:** Opinions are cheap. Evidence is gold.
| Evidence type | Count | Details / link |
|---------------|-------|----------------|
| Customer interviews done | | |
| Survey responses | | |
| People on waitlist | | |
| Search volume for related keywords | | |
| Existing paying competitors | | |
| Online posts/complaints found | | |

## 4.9 Who is NOT your customer?
**WHY:** Saying "no" keeps your marketing sharp.
> ANSWER (list 2-3 groups you will NOT target at first):

## 4.10 Early-adopter profile (your first 50 users)
**WHY:** Your first users are not "the average person". They are people who feel the pain most.
> ANSWER (who exactly, and where can you find 50 of them?):

## 4.11 AI PROMPT: pressure-test the customer
```
I am building {{product one-sentence description}} for {{ideal customer}}.
Their problem is {{problem}}.
1. List 5 reasons this customer might NOT care about this problem.
2. List 5 questions I should ask in customer interviews (no leading questions).
3. Tell me what evidence would prove I am wrong.
Do not invent statistics. If you cite a fact, give the source or say "unverified".
```

---

# 5. MARKET AND COMPETITORS

> **WHY THIS SECTION EXISTS:** You are not alone. Know the neighbors.

## 5.1 What category is your product in?
**EXAMPLE:** `Plant care apps.`
> ANSWER:

## 5.2 How big is the market? (rough, honest)
**WHY:** You only need 500 users, but you must know there are more where they came from.
| Level | Meaning | Your estimate | Source + date |
|-------|---------|---------------|---------------|
| Total market | Everyone who could ever use it | | |
| Reachable market | People you can realistically reach in 12 months | | |
| First target | People matching your early-adopter profile | | |

## 5.3 Competitor table (list at least 3, including "do nothing")
| Name | Link | What they do well | What they do badly | Price | Why customers pick them |
|------|------|-------------------|--------------------|-------|-------------------------|
| Competitor 1 | | | | | |
| Competitor 2 | | | | | |
| Competitor 3 | | | | | |
| "Do nothing / DIY" | N/A | | | Free | |

## 5.4 Gap: what do none of them do?
> ANSWER:

## 5.5 Why will customers switch to you?
**WHY:** Switching takes effort. Your reason must be bigger than the effort.
> ANSWER (one clear reason):

## 5.6 Trends helping you
> ANSWER (2-3 trends, each with a source and date):

## 5.7 Trends hurting you
> ANSWER (2-3, honestly):

## 5.8 AI PROMPT: competitor research
```
Research competitors for {{category}} aimed at {{ideal customer}}.
Return a table: name, URL, main features, pricing (as listed publicly), strengths, weaknesses.
For every fact include the source URL and today's date. If you cannot verify something, write "UNVERIFIED".
Do not guess prices.
```

---

# 6. POSITIONING AND MESSAGING

> **WHY THIS SECTION EXISTS:** Positioning is the short answer to "Why should I use this instead of something else?"

## 6.1 Positioning statement (fill the blanks)
**"For {{target customer}} who {{problem}}, {{product name}} is a {{category}} that {{main benefit}}. Unlike {{main alternative}}, we {{key difference}}."**
> ANSWER:

## 6.2 Top 3 benefits (benefits, not features)
**WHY:** A feature is what it does. A benefit is what the customer gets.
| Feature (what it does) | Benefit (what the customer gets) |
|------------------------|----------------------------------|
| Sends watering reminders | Plants stay alive without thinking about it |
| | |
| | |

## 6.3 The headline (max 10 words)
**EXAMPLE:** `Never kill a houseplant again.`
> ANSWER:

## 6.4 The sub-headline (max 25 words)
> ANSWER:

## 6.5 The "elevator pitch" (30 seconds, about 75 words)
> ANSWER:

## 6.6 Proof you can show
Tick all you have, and add details:
- [ ] Real customer quotes: {{how many}}
- [ ] Before/after numbers: {{what}}
- [ ] Screenshots or demo video
- [ ] Press mentions or awards
- [ ] Security or trust badges
- [ ] Founder story
> ANSWER (details):

## 6.7 Tone of voice
Tick 3 words that describe how you sound:
- [ ] Friendly  - [ ] Professional  - [ ] Playful  - [ ] Bold  - [ ] Calm
- [ ] Expert  - [ ] Simple  - [ ] Witty  - [ ] Warm  - [ ] Direct
> ANSWER (words to always use / words to never use):

## 6.8 Objections (why people say "no") and your answers
| Objection | Your honest answer |
|-----------|--------------------|
| "It costs too much." | |
| "I do not trust new apps." | |
| "I already use something else." | |
| "It looks hard to learn." | |
| "What happens to my data?" | |

## 6.9 Message test
**WHY:** Check that your message works before spending money.
- [ ] I showed the headline to 5 people in my target group.
- [ ] At least 4 of 5 could say, in their own words, what the product does.
> ANSWER (what they said, and what I changed):

## 6.10 AI PROMPT: messaging
```
Write 5 headline options (max 10 words each) for {{product}} aimed at {{customer}}.
Use plain words a 12-year-old understands. No hype words like "revolutionary" or "game-changing".
Base them ONLY on these customer quotes: {{quotes}}.
Mark which benefit each headline highlights.
```

---

# 7. PRICING AND PACKAGING

> **WHY THIS SECTION EXISTS:** Price tells people what your product is worth, and decides whether you survive.

## 7.1 Pricing model
Tick one:
- [ ] Free forever
- [ ] Freemium
- [ ] Monthly subscription
- [ ] Yearly subscription
- [ ] One-time purchase
- [ ] Usage-based
- [ ] Other: {{describe}}

## 7.2 Plans and prices
| Plan name | Price | Billing (month/year/once) | Who it is for | What is included | Limits |
|-----------|-------|---------------------------|---------------|------------------|--------|
| Free | $0 | | | | |
| Plan 2 | | | | | |
| Plan 3 | | | | | |

## 7.3 How did you choose this price?
Tick what you used and add details:
- [ ] Competitor prices (list in 5.3)
- [ ] Customer interviews ("at what price is it too cheap / too expensive?")
- [ ] My costs plus margin
- [ ] Value to customer (what they save or earn)
> ANSWER:

## 7.4 Cost to serve one active user (monthly)
**WHY:** AI products can cost more per user than you expect. Do not lose money on every customer.
| Cost item | Per user / month |
|-----------|------------------|
| Hosting / servers | |
| AI model / API usage | |
| Database / storage | |
| Email / SMS | |
| Payment fees | |
| Support time | |
| **Total** | |

> ANSWER (Price per user minus cost per user = ${{profit}}):

## 7.5 Free trial or free plan rules
> ANSWER (length, limits, whether a card is required, what happens when it ends):

## 7.6 Launch offers (if any)
**EXAMPLE:** `First 100 users get 30% off for life.`
> ANSWER (offer, limit, end date, how many you can afford):

## 7.7 Refund and cancellation policy (plain English)
> ANSWER:

## 7.8 Payment setup
- [ ] Payment provider chosen: {{name}}
- [ ] Test payment completed (with test card)
- [ ] Taxes handled (see Section 21)
- [ ] Receipts / invoices working
- [ ] Failed-payment emails working

## 7.9 Price test plan
> ANSWER (when and how will I test a higher or lower price, and what result changes my mind?):

---

# 8. PRODUCT READINESS (AI-DRIVEN DEVELOPMENT)

> **WHY THIS SECTION EXISTS:** Marketing a broken product only makes more people unhappy, faster.

## 8.1 Core promise
What is the ONE thing the product must do really well?
> ANSWER:

## 8.2 Must-have features for launch (MVP)
**WHY:** Launch with the smallest version that solves the problem.
| # | Feature | Why it is a must-have | Status (not started / building / done) |
|---|---------|-----------------------|-----------------------------------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

## 8.3 Features NOT in launch (the "later" list)
> ANSWER:

## 8.4 How was the product built?
| Item | Answer |
|------|--------|
| AI coding tools used | |
| % of code written by AI (estimate) | |
| Who reviewed AI-written code | |
| Tech stack (languages, hosting, database) | |
| Repository link | |

## 8.5 AI-specific safety checks (if the product uses AI)
- [ ] I tested the AI with wrong, odd and rude inputs.
- [ ] The AI cannot reveal private data of other users.
- [ ] The AI tells users when it is unsure or cannot help.
- [ ] Users are told clearly that they are interacting with AI.
- [ ] There is a limit on AI usage per user (to protect my costs).
- [ ] There is a fallback if the AI service is down.
- [ ] I have a way to report and fix bad AI answers.
> ANSWER (notes):

## 8.6 Security basics
- [ ] Passwords are never stored in plain text
- [ ] No secrets or API keys in the code repository
- [ ] HTTPS everywhere
- [ ] Login protected against too many attempts
- [ ] Backups run automatically and a restore was tested
- [ ] Dependencies scanned for known problems
- [ ] AI-written code was reviewed by a human for security

## 8.7 Performance basics
| Check | Target | Result |
|-------|--------|--------|
| Page / app load time | under 3 seconds | |
| Works on slow internet | yes | |
| Works on mobile | yes | |
| Handles {{N}} users at once | yes | |

## 8.8 Accessibility basics
- [ ] Text is readable (good contrast)
- [ ] Works with keyboard only (web)
- [ ] Images have text descriptions
- [ ] Not dependent on color alone

## 8.9 Monitoring (so you know when it breaks)
| Item | Tool | Alert goes to |
|------|------|---------------|
| Uptime | | |
| Errors / crashes | | |
| Slow responses | | |
| AI cost spikes | | |

## 8.10 If something breaks: the emergency plan
> ANSWER (who fixes it, how fast, how users are told, how to roll back to the last good version):

## 8.11 AI PROMPT: release readiness review
```
Act as a skeptical QA lead. Here is my feature list: {{features}} and my launch checklist: {{section 8 answers}}.
List the 10 most likely ways this product fails on launch day.
For each: how to test it, and how severe it is (low/medium/high).
Do not assume anything works unless I said it was tested.
```

---

# 9. PHASE 1: BUILD

> **GOAL:** The product works end to end for the main use case.
> **TARGET DATES:** Start {{date}}  End {{date}}

## 9.1 What are we building in this phase?
> ANSWER (3 bullet points max):

## 9.2 Task list
| # | Task | Owner | Done by | Status |
|---|------|-------|---------|--------|
| 1 | Set up code repository and project board | | | |
| 2 | Write the product requirements (what "done" means) | | | |
| 3 | Build feature 1 | | | |
| 4 | Build feature 2 | | | |
| 5 | Build feature 3 | | | |
| 6 | Set up login and accounts | | | |
| 7 | Set up payments (if paid) | | | |
| 8 | Set up analytics events (see Section 20) | | | |
| 9 | Set up error monitoring | | | |
| 10 | Write basic help text inside the product | | | |

## 9.3 AI-assisted build rules
- [ ] AI writes code in small pieces, and I review each piece.
- [ ] Every AI-written feature has automated tests.
- [ ] I keep a list of what AI generated and what I changed.
- [ ] I never paste secrets into AI tools.
- [ ] I commit to version control often, so I can undo mistakes.

## 9.4 Marketing work that starts NOW (while building)
**WHY:** Waiting until the product is finished to find customers is the most common mistake.
- [ ] Pick the product name and check it is free (domain, app stores, social handles, trademark search)
- [ ] Buy the domain: {{domain}}
- [ ] Create a one-page "coming soon" site with an email sign-up
- [ ] Start customer interviews (goal: {{N}} interviews)
- [ ] Create social accounts: {{list}}
- [ ] Start a "building in public" log (optional)

## 9.5 Risks in this phase
> ANSWER (top 3 risks and what you will do about each):

## 9.6 GATE 1: BUILD COMPLETE
All must be ticked to move on.
- [ ] All must-have features (8.2) work end to end
- [ ] No known "critical" or "high" bugs open
- [ ] Automated tests pass
- [ ] Security basics (8.6) done
- [ ] Monitoring (8.9) is running
- [ ] Analytics events fire correctly (tested)
- [ ] Payments work in test mode (if paid)
- [ ] Domain, email and landing page exist
- [ ] At least {{N}} customer interviews completed
- [ ] Emergency plan (8.10) written

> Approved by (human name): ________  Date: ________

---

# 10. PHASE 2: TEST

> **GOAL:** Real people, who are not you, can use the product successfully without your help.
> **TARGET DATES:** Start {{date}}  End {{date}}

## 10.1 Test types

| Test | What it checks | Who does it | Result |
|------|----------------|-------------|--------|
| Automated tests | Code does what it should | AI + me | |
| Manual walkthrough | Every screen and button | Me | |
| Usability test | Can a stranger finish the main task? | 5 target users | |
| Device / browser test | Works on common devices | Me | |
| Security check | Obvious holes | Me / tool | |
| Load test | Handles many users | Tool | |
| AI behavior test | AI answers safely and correctly | Me | |
| Payment test | Money flows, refunds work | Me | |

## 10.2 Usability test script (beginner version)
Watch 5 people from your target group try the product. Do NOT help them.
1. Say: "Please try to {{main task}}. Talk out loud while you do it."
2. Stay quiet. Write down where they hesitate, get lost or complain.
3. At the end ask: "What was confusing?" and "Would you use this? Why or why not?"

| Tester | Finished the main task? (Y/N) | Time taken | Where they got stuck | Quote |
|--------|-------------------------------|------------|----------------------|-------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

> ANSWER (Top 3 problems found, and how I will fix each):

## 10.3 Private beta
| Item | Answer |
|------|--------|
| Number of beta testers wanted | |
| Where I will find them | |
| How long the beta runs | |
| What I give them (free access, discount, thanks) | |
| How they send feedback | |
| How I thank them | |

## 10.4 Bug priority rules
| Level | Meaning | Rule |
|-------|---------|------|
| Critical | Product unusable, data lost, security hole | Fix before launch. No exceptions. |
| High | Main feature broken for many users | Fix before launch. |
| Medium | Annoying, has a workaround | Fix within 2 weeks of launch. |
| Low | Cosmetic | Put on the "later" list. |

## 10.5 Early success signals from beta
| Measure | Target | Actual |
|---------|--------|--------|
| Testers who finish the main task | 80% or more | |
| Testers who say they would be "very disappointed" if the product vanished | 40% or more | |
| Testers who come back in week 2 | 40% or more | |
| Testers who would recommend it | 7 of 10 or more | |

## 10.6 GATE 2: TEST COMPLETE
- [ ] 4 of 5 usability testers finished the main task without help
- [ ] Zero critical and zero high bugs open
- [ ] Beta feedback has been read, grouped and acted on
- [ ] Load test passed for {{N}} users
- [ ] AI behavior test passed (if applicable)
- [ ] Payments tested end to end, including refund
- [ ] I changed the product based on what I learned (list in Decision Log)

> Approved by (human name): ________  Date: ________

---

# 11. PHASE 3: PRE-LAUNCH

> **GOAL:** Before opening the doors, have people waiting and everything prepared.
> **TARGET DATES:** Start {{date}}  End {{date}}
> **TARGET:** {{N}} people on the waitlist (suggested: 200 to 500 for a goal of 500 active users)

## 11.1 Waitlist
| Item | Answer |
|------|--------|
| Tool for the waitlist | |
| What people get for joining | |
| Current sign-ups | |
| Goal by launch | |
| How I will reach the goal | |

## 11.2 Launch asset checklist
- [ ] Landing page live (headline, benefits, proof, price, sign-up button)
- [ ] Demo video or screenshots (under 90 seconds)
- [ ] Product name, logo and brand colors final
- [ ] Short description (under 160 characters) for search and stores
- [ ] Long description for stores / directories
- [ ] 5+ screenshots or images
- [ ] FAQ page
- [ ] Pricing page
- [ ] Terms of Service and Privacy Policy published
- [ ] Welcome email written
- [ ] Onboarding emails written (Section 17)
- [ ] Support email address works: {{email}}
- [ ] Social profiles complete
- [ ] Press / media kit (logo, photos, one-pager)
- [ ] Analytics and cookie consent set up
- [ ] App store listing approved (if mobile)

## 11.3 Landing page quality check
| Check | Yes / No |
|-------|----------|
| A stranger understands what it is in 5 seconds | |
| One main button and it is obvious | |
| Benefits are listed before features | |
| Real proof is shown (quotes, numbers) | |
| Price is clear (or "how pricing works") | |
| Loads in under 3 seconds | |
| Works on a phone | |
| No broken links | |

## 11.4 Content created before launch
| Type | Count planned | Count ready | Where it will be published |
|------|---------------|-------------|----------------------------|
| Blog posts / articles | | | |
| Short videos | | | |
| Social posts | | | |
| Emails | | | |
| Tutorials / guides | | | |

## 11.5 Build relationships before launch
List people and communities who could help spread the word.
| Name / community | Why they matter | How I will approach them (honestly and politely) | Status |
|------------------|-----------------|--------------------------------------------------|--------|
| | | | |
| | | | |
| | | | |

## 11.6 Launch-day rehearsal
- [ ] I ran a full "pretend launch" with a friend
- [ ] The sign-up to first-use flow was tested on fresh accounts
- [ ] Support inbox tested
- [ ] Alerts tested (I received a test alert)
- [ ] Rollback plan tested

## 11.7 GATE 3: PRE-LAUNCH COMPLETE
- [ ] Waitlist reached {{target}} (or I wrote why launching earlier is fine)
- [ ] Every item in 11.2 is done or marked N/A
- [ ] Landing page passes 11.3
- [ ] Legal pages published and reviewed (Section 21)
- [ ] Rehearsal (11.6) completed
- [ ] Launch date and time chosen: {{date/time/timezone}}
- [ ] Budget for launch approved (Section 19)

> Approved by (human name): ________  Date: ________

---

# 12. PHASE 4: LAUNCH

> **GOAL:** Open the doors, welcome people, fix problems fast.
> **TARGET DATES:** Launch day {{date}}  Launch week ends {{date}}

## 12.1 Launch day plan (hour by hour)
| Time | Action | Owner | Done |
|------|--------|-------|------|
| T-24h | Final check of everything; freeze new changes | | [ ] |
| T-2h | Confirm monitoring and support are ready | | [ ] |
| T-0 | Switch product to live | | [ ] |
| T+15m | Test sign-up and first-use as a brand-new user | | [ ] |
| T+30m | Email the waitlist | | [ ] |
| T+1h | Publish launch posts on {{channels}} | | [ ] |
| T+3h | Reply to every comment and message | | [ ] |
| T+6h | Check numbers; fix urgent bugs | | [ ] |
| T+24h | Review day-1 results; write notes | | [ ] |

## 12.2 Where will you announce? (see Section 15 for full channel plan)
| Place | What I will post | Time | Approved by human? |
|-------|------------------|------|--------------------|
| Waitlist email | | | |
| Social media | | | |
| Communities (follow each community's rules) | | | |
| Product directories | | | |
| Friends / network | | | |

## 12.3 Launch week targets
| Measure | Target | Actual |
|---------|--------|--------|
| Visitors to landing page | | |
| Sign-ups | | |
| Activated users (did the key action) | | |
| Paying users (if applicable) | | |
| Support messages | | |
| Critical bugs | 0 | |

## 12.4 War-room rules (launch week)
- Check errors and support **every 2 hours** during waking time.
- Reply to every user message within **{{hours}}** hours.
- Fix critical bugs first. Everything else waits.
- Write down every complaint. Patterns matter more than single messages.

## 12.5 What if launch is quiet?
**WHY:** Silence on day 1 is normal. Have a plan.
> ANSWER (what I will do on day 2, 3 and 7 if I get fewer than {{N}} sign-ups):

## 12.6 What if launch is too busy?
> ANSWER (what breaks first, and how I will protect the product and my AI/hosting bill):

## 12.7 GATE 4: LAUNCH COMPLETE
- [ ] Product is live and stable for 7 days
- [ ] No critical bugs open
- [ ] Every user message answered within the promised time
- [ ] Launch week numbers recorded in 12.3
- [ ] Launch lessons written down (3 things that worked, 3 that did not)
- [ ] First user quotes / testimonials collected (with permission)

> Approved by (human name): ________  Date: ________

---

# 13. PHASE 5: EARLY GROWTH (USERS 1 TO 100)

> **GOAL:** Reach 100 active users and learn what works. Do things that do not scale (personal attention).
> **TARGET DATES:** Start {{date}}  End {{date}}

## 13.1 The weekly growth routine (do this every week)
| Day | Task |
|-----|------|
| Monday | Look at numbers (Section 20). Write 3 findings. |
| Tuesday | Talk to 3 users (call, chat or email). |
| Wednesday | Make one improvement to the product from feedback. |
| Thursday | Publish content or outreach on the best channel. |
| Friday | Write the weekly note: what happened, what I learned, what is next. |

## 13.2 Do things that do not scale
Tick what you will do for your first 100:
- [ ] Welcome every new user personally (message or email)
- [ ] Ask each user "What nearly stopped you from signing up?"
- [ ] Offer a 15-minute call to the first 30 users
- [ ] Fix small user-reported issues within 48 hours and tell them
- [ ] Ask happy users to introduce one friend

## 13.3 Channel experiments (pick 3 to 5 from Section 15)
| Experiment | Hypothesis ("If I do X, I expect Y") | Time and money to spend | Success number | Result | Keep / stop |
|------------|--------------------------------------|--------------------------|----------------|--------|-------------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

## 13.4 Activation check (are new people succeeding?)
| Measure | Target | Week 1 | Week 2 | Week 3 | Week 4 |
|---------|--------|--------|--------|--------|--------|
| Sign-up to key action in 24 hours | 40% or more | | | | |
| Day-7 return rate | 30% or more | | | | |
| Day-30 return rate | 20% or more | | | | |

## 13.5 Feedback loop
| Step | How |
|------|-----|
| Collect | In-product button, email replies, interviews |
| Group | Put every piece of feedback in the tracker and tag it |
| Count | Which tag shows up the most? |
| Decide | Fix the top-voted problem that affects the most users |
| Tell | Tell users when you fixed their issue |

## 13.6 What to learn in this phase (answer by the end)
> ANSWER:
> 1. Which channel brought the most ACTIVE users (not just sign-ups)?
> 2. What does a happy user say in their own words?
> 3. What is the number-one reason people leave?
> 4. Is my price right? (Evidence:)
> 5. What is the cost to get one active user so far? ($)

## 13.7 GATE 5: EARLY GROWTH COMPLETE
- [ ] 100 active users (as defined in 3.2), counted from the source in 3.3
- [ ] Best channel identified with numbers (Section 15)
- [ ] Top 3 churn (leaving) reasons known and at least 1 fixed
- [ ] Day-30 return rate recorded
- [ ] Cost to get one active user recorded
- [ ] At least 5 testimonials or case notes collected (with permission)
- [ ] Support load is manageable (hours per week: {{N}})

> Approved by (human name): ________  Date: ________

---

# 14. PHASE 6: SCALE TO 500

> **GOAL:** Repeat what works, steadily, until 500 active users.
> **TARGET DATES:** Start {{date}}  End {{date}}

## 14.1 Growth math (work backwards)
| Item | Value |
|------|-------|
| Active users needed | 500 |
| Active users I already have | |
| Gap | |
| Expected people who leave per month (churn %) | |
| Weeks I have | |
| New active users needed per week (including replacing leavers) | |

> ANSWER (formula shown: gap + expected leavers, divided by weeks):

## 14.2 Double down on what works
| Channel | Active users from it so far | Cost per active user | Plan to grow it |
|---------|------------------------------|----------------------|-----------------|
| | | | |
| | | | |

## 14.3 Referral and word of mouth
| Item | Answer |
|------|--------|
| Do users have an easy way to invite friends? | |
| What do inviter and friend get? | |
| Target: % of users who invite someone | |
| Share button / link location in product | |

## 14.4 Automation (use AI carefully)
| Task | Tool | Human check before it goes out? |
|------|------|----------------------------------|
| Welcome and onboarding emails | | Yes |
| Answering common support questions | | Yes for new topics |
| Weekly metrics report | | Yes |
| Content drafts | | Yes, always |
| Outreach drafts | | Yes, always |

## 14.5 Keep quality while growing
- [ ] Bug count is not rising
- [ ] Support response time is still within promise
- [ ] AI and hosting cost per user is still below target (7.4)
- [ ] User satisfaction score is not falling (Section 20)

## 14.6 Milestone tracker
| Milestone | Target date | Actual date | Notes |
|-----------|-------------|-------------|-------|
| 100 active users | | | |
| 200 active users | | | |
| 300 active users | | | |
| 400 active users | | | |
| 500 active users | | | |

## 14.7 GATE 6: 500 ACTIVE USERS
- [ ] 500 active users, counted by the rule in 3.2 and source in 3.3
- [ ] Number held for at least 2 weeks (not just a one-day spike)
- [ ] Growth channels documented and repeatable
- [ ] Unit economics positive or a clear plan to get there (7.4)
- [ ] Retention (day-30) is at or above target
- [ ] Retrospective written (Section 24.3)
- [ ] Next goal chosen (for example 2,000 users) and a new plan started

> Approved by (human name): ________  Date: ________

---

# 15. CHANNELS AND CUSTOMER ACQUISITION

> **WHY THIS SECTION EXISTS:** A "channel" is a road that brings customers to you. Pick a few roads and travel them well. Do not try all of them.

## 15.1 Channel menu: score each (1 = poor fit, 5 = great fit)
| Channel | Fit with my customer (1-5) | Effort (1-5, 5 = lots) | Cost (1-5, 5 = expensive) | Speed (1-5, 5 = fast) | Pick? |
|---------|----------------------------|------------------------|---------------------------|-----------------------|-------|
| Search (SEO, blog content) | | | | | |
| Social media (organic) | | | | | |
| Short video | | | | | |
| Communities / forums | | | | | |
| Email list / newsletter | | | | | |
| Product directories / launch sites | | | | | |
| Partnerships / integrations | | | | | |
| Influencers / creators | | | | | |
| Direct outreach (email, DM, calls) | | | | | |
| Paid ads | | | | | |
| App store search | | | | | |
| Referrals / word of mouth | | | | | |
| Events / webinars / meetups | | | | | |
| Press / media | | | | | |
| Open source / free tool / template | | | | | |

## 15.2 My chosen channels (pick 3 to 5; ONE main channel)
| Rank | Channel | Why I chose it | Weekly time (hours) | Weekly money |
|------|---------|----------------|---------------------|--------------|
| 1 (Main) | | | | |
| 2 | | | | |
| 3 | | | | |

## 15.3 Plan for each chosen channel
Copy this block once per channel.

**Channel name:** {{name}}
| Question | Answer |
|----------|--------|
| Who exactly am I reaching here? | |
| What do I post / send / do? | |
| How often? | |
| Call-to-action (what do I ask people to do)? | |
| How do I track results (link, code)? | |
| Success number after 4 weeks | |
| Stop-or-continue rule | |

## 15.4 Rules for honest marketing (mandatory)
- [ ] Follow each community's rules; no spam
- [ ] Say you built the product when you recommend it
- [ ] No fake reviews, fake users or fake urgency
- [ ] Every claim is true and provable
- [ ] Emails include an unsubscribe link and follow the law (Section 21)
- [ ] Ads follow platform rules

## 15.5 Content plan (if using content)
| Topic | Customer question it answers | Format | Publish date | Link to product? |
|-------|------------------------------|--------|--------------|------------------|
| | | | | |
| | | | | |
| | | | | |

## 15.6 Direct outreach plan (if used)
| Item | Answer |
|------|--------|
| Who I contact | |
| Where I find them | |
| Message in 4 sentences (who I am, why them, what I offer, simple ask) | |
| Messages per week | |
| Expected reply rate | |
| Tracking sheet link | |

## 15.7 Paid ads plan (only after Phase 5 shows people want it)
| Item | Answer |
|------|--------|
| Platform | |
| Monthly budget | |
| Max cost per active user I can afford | |
| Ad message | |
| Target audience | |
| Stop rule (if cost per active user exceeds X for Y days) | |

## 15.8 Partnerships (if used)
| Partner | What they get | What I get | Next step |
|---------|---------------|------------|-----------|
| | | | |

## 15.9 AI PROMPT: channel plan
```
My product: {{one sentence}}. My customer: {{profile}}. My budget: ${{amount}} per month and {{hours}} hours per week.
Suggest the 3 best acquisition channels, and for each:
- why it fits this customer
- a 4-week experiment with a clear success number
- the main risk
Do not invent statistics. Mark anything you are unsure about "UNVERIFIED".
```

---

# 15A. MOBILE APP STORE LAUNCH

> **REQUIRED SECTION.** If your product is not a mobile app, write `N/A - because it is not a mobile app` in 15A.1 and move on. Do not delete this section.
> **WHY THIS SECTION EXISTS:** App stores have their own rules, review times and search systems. Missing one can delay your launch by weeks.

## 15A.1 Is this a mobile app?
Tick one:
- [ ] Yes, iOS (Apple App Store)
- [ ] Yes, Android (Google Play)
- [ ] Yes, both
- [ ] No. `N/A - because ...`
> ANSWER (reason or details):

## 15A.2 Developer accounts
| Item | Apple | Google |
|------|-------|--------|
| Developer account created | [ ] | [ ] |
| Fee paid (check the current fee on the store's website) | [ ] | [ ] |
| Identity / business verification finished | [ ] | [ ] |
| Account owner and recovery email | | |

## 15A.3 Store listing content
| Item | Your answer | Notes |
|------|-------------|-------|
| App name (short and clear) | | Check store limits |
| Subtitle / short description | | |
| Full description (first lines matter most) | | |
| Keywords / search terms | | |
| Category | | |
| Age rating answers | | Answer honestly |
| Screenshots (list sizes needed per device) | | Show benefits, not just screens |
| App icon | | |
| Preview video (optional) | | |
| Support URL | | |
| Privacy policy URL | | Required |
| Marketing URL | | |

## 15A.4 Store search (ASO = App Store Optimization) basics
> ANSWER:
> 1. What 10 words would my customer type to find me?
> 2. Which of those are in my name, subtitle and keywords?
> 3. Which competitor apps rank for those words, and what do their listings do well?

## 15A.5 Review and rules checklist
- [ ] I read the current store review guidelines (Apple and/or Google) and compared them with my app.
- [ ] Sign-in, payments and subscriptions follow store rules (including how in-app purchases must work).
- [ ] Privacy "nutrition label" / data-safety form is filled in honestly.
- [ ] Permission requests (camera, location, notifications) explain WHY in plain words.
- [ ] A demo account and review notes are ready for the reviewer.
- [ ] No hidden features, placeholder text or broken links.
- [ ] AI-generated content rules checked (reporting, filtering and labeling where required).

## 15A.6 Beta testing in the store
| Item | Answer |
|------|--------|
| Beta tool (for example TestFlight for iOS, Internal/Closed testing for Android) | |
| Number of testers | |
| Date I submit the first build | |

## 15A.7 Review timeline (leave a buffer)
| Step | Planned date | Actual date |
|------|--------------|-------------|
| Submit for review | | |
| Expected review time (check current store guidance) | | |
| Buffer for rejection and resubmission (suggest 1-2 weeks) | | |
| Approved | | |
| Release on (manual or automatic) | | |

## 15A.8 If the app is rejected
> ANSWER (who reads the rejection, how fast I fix it, who approves the resubmission):

## 15A.9 Ratings and reviews plan
| Item | Answer |
|------|--------|
| When do I ask for a rating? (after a happy moment, never during a problem) | |
| How do I reply to reviews? (always kindly, within {{days}}) | |
| How many ratings do I want by 100 users? | |

## 15A.10 Update plan
> ANSWER (how often I release updates, how I write release notes, how I avoid breaking older versions):

## 15A.11 GATE: STORE READY
- [ ] Listing complete (15A.3)
- [ ] Review checklist done (15A.5)
- [ ] Beta feedback fixed (15A.6)
- [ ] Release timeline and buffer set (15A.7)
- [ ] Ratings and reply plan set (15A.9)

---

# 15B. B2B SALES (SELLING TO BUSINESSES)

> **REQUIRED SECTION.** If you sell only to individuals (not to companies), write `N/A - because we sell to individuals` in 15B.1 and move on. Do not delete this section.
> **WHY THIS SECTION EXISTS:** Businesses buy differently. They have several decision makers, ask security questions, and take longer to say yes.

## 15B.1 Will businesses buy this?
Tick one:
- [ ] Yes, mainly businesses
- [ ] Yes, businesses and individuals
- [ ] No. `N/A - because ...`

## 15B.2 Ideal company profile
| Field | Your answer |
|-------|-------------|
| Company size (employees) | |
| Industry | |
| Country / region | |
| Team that would use it | |
| Tools they use today | |
| Typical yearly budget for this kind of tool | |
| A sign they need me (for example: "hiring for X", "using spreadsheets for Y") | |

## 15B.3 The buying team (who says yes?)
| Role | Name type / job title | What they care about | What I give them |
|------|-----------------------|----------------------|------------------|
| User (uses it daily) | | | |
| Champion (wants it to win) | | | |
| Decision maker (signs) | | | |
| Money holder (budget) | | | |
| Technical / security reviewer | | | |
| Blocker (may say no) | | | |

## 15B.4 Sales process (step by step)
| Step | What happens | My target time | Success rule |
|------|--------------|----------------|--------------|
| 1. Find | Build a list of {{N}} matching companies | | |
| 2. Reach out | Short, honest message | | Reply rate: {{%}} |
| 3. Talk | 20-minute discovery call | | |
| 4. Show | Demo focused on THEIR problem | | |
| 5. Pilot / trial | Small test with success numbers agreed upfront | | |
| 6. Propose | Price, scope, start date | | |
| 7. Buy | Contract or card payment | | |
| 8. Start | Onboarding and first win | | |

## 15B.5 Discovery call questions (use at least 7)
- [ ] What are you doing today to solve this?
- [ ] What does it cost you (time, money, mistakes)?
- [ ] Who else is involved in a decision like this?
- [ ] What happened the last time you bought a tool like this?
- [ ] What would make this a clear success for you in 30 days?
- [ ] What is your budget and timeline?
- [ ] What could stop this from happening?
> ANSWER (my own extra questions):

## 15B.6 Pilot rules
| Item | Answer |
|------|--------|
| Pilot length | |
| Price (free, paid, discounted) | |
| Success numbers we agree on in writing BEFORE the pilot | |
| What happens if the pilot succeeds | |
| What happens if it does not | |

## 15B.7 Pricing for businesses
| Item | Answer |
|------|--------|
| Per seat, per usage or flat? | |
| Monthly or yearly billing? | |
| Discounts (limits and who may give them) | |
| Invoice and payment terms | |

## 15B.8 Security and trust questions businesses will ask
- [ ] Where is data stored?
- [ ] Who can access it?
- [ ] Is data encrypted?
- [ ] Do you use customer data to train AI models?
- [ ] What happens if there is a breach?
- [ ] Can we delete our data at any time?
- [ ] Do you have backups and a recovery plan?
- [ ] Do you have a standard security answer sheet or trust page?
> ANSWER (link to my security / trust page, or when I will write it):

## 15B.9 Contracts and legal for business customers
- [ ] Terms for business customers reviewed by a qualified person
- [ ] Data processing terms prepared if the customer is in a region that requires them
- [ ] Service promises (uptime, support hours) are things I can truly deliver

## 15B.10 Sales tracking
Use the "Outreach tracker" in Appendix D.

## 15B.11 B2B targets for this plan
| Item | Target |
|------|--------|
| Companies contacted | |
| Calls booked | |
| Demos done | |
| Pilots started | |
| Paying customers | |
| Active users inside those customers | |

> ANSWER (Do the 500 active users come from companies? If yes, how many companies times how many users each = 500?):

---

# 15C. COMMUNITY BUILDING

> **REQUIRED SECTION.** If you will not build a community, write `N/A - because ...` in 15C.1 and move on. Do not delete this section.
> **WHY THIS SECTION EXISTS:** A community is a place where users help each other and talk to you directly. It lowers support work and raises retention.

## 15C.1 Will I build a community?
Tick one:
- [ ] Yes, my own (Discord, Slack, forum, group)
- [ ] Yes, inside an existing community (I take part, I do not own it)
- [ ] Not yet. I will revisit at {{N}} users
- [ ] No. `N/A - because ...`

## 15C.2 Purpose
> ANSWER (Why would a user join, in one sentence? What do they get that they cannot get elsewhere?):

## 15C.3 Platform choice
| Option | Fits my users? | Effort | Cost | Pick |
|--------|----------------|--------|------|------|
| Chat server (for example Discord, Slack) | | | | |
| Forum | | | | |
| Social group | | | | |
| In-product community | | | | |
| Email newsletter replies | | | | |

## 15C.4 Rules (write them BEFORE you invite anyone)
- [ ] Be kind and respectful
- [ ] No spam or self-promotion outside allowed places
- [ ] No sharing of private data
- [ ] How reports and removals work: {{details}}
- [ ] Consequences for breaking rules: {{details}}

## 15C.5 Who runs it?
| Role | Name | Time per week |
|------|------|---------------|
| Community owner | | |
| Moderator(s) | | |
| Backup | | |

## 15C.6 First 30 days
| Week | Action |
|------|--------|
| 1 | Invite the first 20 happy users personally |
| 2 | Start one weekly topic (tips, Q&A, show-and-tell) |
| 3 | Highlight a user story |
| 4 | Ask for feedback on what to improve |

## 15C.7 Champions (your helpful early fans)
| Name | Why they are a good champion | What I give them (access, thanks, credit) |
|------|------------------------------|--------------------------------------------|
| | | |

## 15C.8 Community health numbers
| Metric | Target | Current |
|--------|--------|---------|
| Members | | |
| Weekly active members | | |
| Questions answered by other users (not me) | | |
| Posts per week | | |
| New sign-ups from the community | | |

## 15C.9 AI in the community
- [ ] AI may draft answers, but a human approves anything about money, safety or legal topics.
- [ ] AI-written replies are labeled when required or expected by the community.
- [ ] AI never pretends to be a human member.

---

# 16. FUNNEL MATH (HOW MANY PEOPLE YOU NEED)

> **WHY THIS SECTION EXISTS:** To get 500 active users you need many more visitors. Math tells you how many.

## 16.1 The funnel in plain English
**Visitors → Sign-ups → Activated (did the key action) → Active users (still using after 30 days)**

## 16.2 Fill in your funnel (start with assumptions, replace with real numbers)
| Step | Rate (%) | Source (ASSUMPTION or VERIFIED) |
|------|----------|----------------------------------|
| Visitors who sign up | | |
| Sign-ups who activate | | |
| Activated who are still active after 30 days | | |
| **Overall: visitors to active user** | (multiply the three) | |

## 16.3 Work backwards
| Item | Value |
|------|-------|
| Active users wanted | 500 |
| Overall conversion (from 16.2) | |
| Visitors needed = 500 divided by overall conversion | |
| Weeks to get them | |
| Visitors needed per week | |

**EXAMPLE:** `If overall conversion is 2%, I need 500 / 0.02 = 25,000 visitors.`
> ANSWER (show your numbers):

## 16.4 Is the plan realistic?
> ANSWER (can my chosen channels (Section 15) bring the weekly visitors in 16.3? If not, what changes?):

## 16.5 Cost to get one active user (CAC)
| Item | Value |
|------|-------|
| Total marketing money spent | |
| Value of my time (hours x hourly rate) | |
| Active users gained | |
| Cost per active user = (money + time value) / active users | |

## 16.6 Payback (if paid product)
| Item | Value |
|------|-------|
| Monthly price | |
| Monthly cost to serve (7.4) | |
| Monthly profit per user | |
| Months to earn back cost per active user | |

## 16.7 Update schedule
> ANSWER (I will replace assumptions with real numbers on {{dates}}):

---

# 17. ONBOARDING, ACTIVATION AND RETENTION

> **WHY THIS SECTION EXISTS:** Getting someone to sign up is half the job. Helping them succeed is the other half.

## 17.1 The "aha moment"
The moment a user first thinks "Oh, this is useful!"
**EXAMPLE:** `Adding the first plant and getting the first reminder.`
> ANSWER:

## 17.2 First-use path (from sign-up to aha moment)
| Step | What the user does | Possible problem | Fix |
|------|--------------------|------------------|-----|
| 1 | Arrives from {{source}} | | |
| 2 | Signs up | | |
| 3 | | | |
| 4 | Reaches the aha moment | | |

> ANSWER (Target: aha moment within {{minutes}} minutes of signing up):

## 17.3 Onboarding emails / messages
| When | Subject (max 50 characters) | Goal | Status |
|------|------------------------------|------|--------|
| Immediately | Welcome | Get them to the first action | |
| Day 1 | | Help if stuck | |
| Day 3 | | Show a second benefit | |
| Day 7 | | Ask for feedback | |
| Day 14 | | Invite to share or upgrade | |
| Inactive for 7 days | | Win them back | |

## 17.4 Why users leave (churn)
| Reason (from exit survey / interviews) | How many | Fix planned |
|----------------------------------------|----------|-------------|
| | | |
| | | |

## 17.5 Retention tactics
Tick what you will use:
- [ ] Helpful reminders / notifications (not annoying)
- [ ] Weekly summary email
- [ ] New features announced
- [ ] Habit loop (a reason to return)
- [ ] Community or user group
- [ ] Win-back email for inactive users

## 17.6 Collecting testimonials
> ANSWER (when and how will I ask happy users? Always get written permission before using a name or photo):

---

# 18. SUPPORT AND FEEDBACK

> **WHY THIS SECTION EXISTS:** Fast, kind support turns early users into fans.

## 18.1 Support channels
| Channel | Address / link | Hours | Response promise |
|---------|----------------|-------|------------------|
| Email | | | |
| In-app chat / form | | | |
| Help center / FAQ | | | |
| Community | | | |

## 18.2 Top 10 questions you expect
| # | Question | Answer (short) |
|---|----------|----------------|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |
| 5 | | |

## 18.3 AI in support: rules
- [ ] AI drafts replies; a human approves anything sensitive (refunds, anger, legal, safety).
- [ ] AI never promises refunds, features or dates on its own.
- [ ] AI never shares one user's data with another.
- [ ] Users can always reach a human.
- [ ] New or unusual questions go to a human and then into the FAQ.

## 18.4 Feedback tracker
| Field | Description |
|-------|-------------|
| Date | When it arrived |
| User (ID, not name, where possible) | Who |
| Source | Email, chat, interview |
| Type | Bug / idea / question / complaint / praise |
| Impact | Low / medium / high |
| Status | New / planned / fixed / not doing |

## 18.5 Satisfaction measurement
Tick one and set a target:
- [ ] "How disappointed would you be if this product disappeared?" (very / somewhat / not) Target: 40% say "very".
- [ ] Net Promoter Score (0 to 10 "How likely to recommend?") Target: {{N}}
- [ ] Simple thumbs up / down after key action Target: {{N}}%

## 18.6 Bad review / angry user playbook
> ANSWER (steps: reply within X hours, say sorry, fix, follow up; never argue publicly):

---

# 19. BUDGET AND RESOURCES

> **WHY THIS SECTION EXISTS:** Running out of money or time quietly ends more products than bad ideas.

## 19.1 Money I can spend (total, until 500 users)
> ANSWER ($):

## 19.2 Budget table
| Category | Phase 1-2 | Phase 3 | Phase 4 | Phase 5-6 | Total | Actual spent |
|----------|-----------|---------|---------|-----------|-------|--------------|
| Hosting and servers | | | | | | |
| AI model / API costs | | | | | | |
| Software tools and subscriptions | | | | | | |
| Design (logo, images) | | | | | | |
| Domain and email | | | | | | |
| Legal (terms, privacy review) | | | | | | |
| Marketing / ads | | | | | | |
| Content and video | | | | | | |
| Contractors / freelancers | | | | | | |
| App store fees | | | | | | |
| Payment fees | | | | | | |
| Emergency buffer (10-20%) | | | | | | |
| **Total** | | | | | | |

## 19.3 My time
| Item | Hours per week |
|------|----------------|
| Building / fixing | |
| Marketing | |
| Support | |
| Admin / learning | |
| **Total** (is this realistic next to my other life commitments?) | |

## 19.4 Spending rules
- No spending above ${{amount}} without writing the reason in the Decision Log.
- Review spending every {{week/month}}.
- Stop any paid test that breaks its stop rule (15.7).

## 19.5 Runway
> ANSWER (If I spend as planned, I have money and time for {{N}} months. The plan needs {{N}} months.):

## 19.6 What I will do if money runs low
> ANSWER:

---

# 20. METRICS AND TRACKING

> **WHY THIS SECTION EXISTS:** What you measure is what you can improve.

## 20.1 The one number that matters (North Star)
**Default:** Active users (as defined in 3.2).
> ANSWER:

## 20.2 Metrics table (one row per metric)
| Metric | What it means | Where it comes from | How often I check | Target | Current |
|--------|---------------|---------------------|-------------------|--------|---------|
| Visitors | People reaching my site/store page | | Weekly | | |
| Sign-ups | People who created accounts | | Weekly | | |
| Activation rate | Sign-ups who do the key action | | Weekly | | |
| Active users | Definition in 3.2 | | Weekly | 500 | |
| Day-7 retention | Still using after 7 days | | Weekly | | |
| Day-30 retention | Still using after 30 days | | Monthly | | |
| Churn | Users who leave per month | | Monthly | | |
| Revenue (if paid) | Money in | | Weekly | | |
| Cost per active user | See 16.5 | | Monthly | | |
| Support tickets | Messages per week | | Weekly | | |
| Support response time | Hours to first reply | | Weekly | | |
| Bugs open | Number by severity | | Weekly | | |
| AI cost per user | From billing | | Weekly | | |
| Satisfaction score | See 18.5 | | Monthly | | |

## 20.3 Events to track in the product
List each action you track. Use clear names.
| Event name | When it fires | Why I track it |
|------------|----------------|-----------------|
| `signed_up` | Account created | Count sign-ups |
| `key_action_completed` | User does the main thing | Count activation |
| `returned_day_7` | User comes back | Retention |
| | | |
| | | |

## 20.4 Tracking setup checklist
- [ ] Analytics tool installed on website and product
- [ ] Every event above tested and visible
- [ ] Source of each sign-up recorded (link tags / "How did you hear about us?")
- [ ] A dashboard shows the metrics in 20.2
- [ ] Privacy rules followed (consent, no needless personal data)
- [ ] Numbers cross-checked once against raw data

## 20.5 Weekly review (10 minutes)
> ANSWER (write each week): What went up? What went down? What will I do about it?

## 20.6 Warning signs (decide your alarms now)
| Warning | Trigger | What I will do |
|---------|---------|----------------|
| Sign-ups drop | Down 30% week-on-week | |
| Activation falls | Below {{X}}% | |
| Errors rise | Above {{X}} per day | |
| AI cost spike | Above ${{X}} per day | |
| Support backlog | Over {{X}} open for 48 hours | |

## 20.7 AI PROMPT: weekly analysis
```
Here are this week's numbers: {{paste metrics}} and last week's: {{paste metrics}}.
1. What changed, in plain words?
2. List 3 possible reasons for each big change (clearly labeled as guesses).
3. For each, tell me one cheap test to check it.
Do not claim certainty. Do not invent numbers.
```

---

# 21. LEGAL, PRIVACY AND COMPLIANCE

> **WHY THIS SECTION EXISTS:** Breaking a rule can end your product. **This section is a checklist, not legal advice.** If unsure, ask a qualified lawyer.

## 21.1 Where do my users live?
> ANSWER (countries and regions; this decides which laws apply):

## 21.2 Legal basics checklist
- [ ] Business registered (or I confirmed I can operate as an individual): {{details}}
- [ ] Terms of Service written and shown at sign-up
- [ ] Privacy Policy written, honest and shown at sign-up
- [ ] Cookie / tracking consent where required
- [ ] Marketing emails: permission obtained, unsubscribe link included, sender identified
- [ ] Taxes understood (sales tax / VAT / income): {{notes}}
- [ ] Refund and cancellation rules follow local law
- [ ] Trademark / name conflicts checked
- [ ] Licenses for code, images, fonts and AI output checked
- [ ] Open-source licenses in my code reviewed

## 21.3 Personal data
| Question | Answer |
|----------|--------|
| What personal data do I collect? | |
| Why do I need each item? | |
| Where is it stored? | |
| Who can access it? | |
| How long do I keep it? | |
| How can a user see, export or delete their data? | |
| Do I share it with anyone (analytics, payment, AI provider)? | |

## 21.4 Special rules to check (tick any that apply, then research)
- [ ] Children under 13 / 16 may use the product
- [ ] Health information
- [ ] Financial information
- [ ] Biometric data
- [ ] Regulated industry (finance, health, education, law)
- [ ] AI-specific rules in my users' regions (transparency, labeling, high-risk uses)

## 21.5 AI-specific legal and trust items
- [ ] I read my AI provider's terms on commercial use and data handling.
- [ ] User data is not used to train models unless users agreed.
- [ ] Users are told when they interact with AI or see AI-generated content.
- [ ] I can explain, in plain words, what the AI does with user input.

## 21.6 Advertising claims
- [ ] Every claim ("fastest", "saves 5 hours") has evidence on file.
- [ ] Testimonials are real, with written permission.
- [ ] No hidden fees or tricks.

## 21.7 Who reviewed this?
> ANSWER (name of the lawyer or advisor, date; or "No review. Risk accepted by {{owner}} on {{date}}"):

---

# 22. RISK REGISTER

> **WHY THIS SECTION EXISTS:** A risk is something that might go wrong. Naming it now means you are ready.

## 22.1 Risk table
Score: Chance (1-5) x Impact (1-5) = Risk score. Anything 15 or higher needs a real plan.

| # | Risk | Phase | Chance (1-5) | Impact (1-5) | Score | What I will do to prevent it | What I will do if it happens | Owner |
|---|------|-------|--------------|--------------|-------|------------------------------|-------------------------------|-------|
| 1 | Nobody signs up | 3-4 | | | | | | |
| 2 | Users sign up but do not come back | 5 | | | | | | |
| 3 | Serious bug or outage at launch | 4 | | | | | | |
| 4 | AI/hosting costs higher than expected | 4-6 | | | | | | |
| 5 | AI gives harmful or wrong answers | 4-6 | | | | | | |
| 6 | Security breach or data leak | All | | | | | | |
| 7 | Competitor copies or undercuts me | 5-6 | | | | | | |
| 8 | A platform I depend on changes rules or prices | All | | | | | | |
| 9 | I run out of time or energy | All | | | | | | |
| 10 | I run out of money | All | | | | | | |
| 11 | Legal / privacy complaint | All | | | | | | |
| 12 | Negative review or public criticism | 4-6 | | | | | | |
| 13 | | | | | | | | |

## 22.2 Assumptions to test
Every `(ASSUMPTION)` you wrote must be listed here and tested.
| Assumption | Where it appears | How I will test it | Test by (date) | Result |
|------------|------------------|--------------------|----------------|--------|
| | | | | |
| | | | | |

## 22.3 Dependencies (things I rely on that I do not control)
| Dependency | What happens if it fails | Backup plan |
|------------|--------------------------|-------------|
| AI model provider | | |
| Hosting provider | | |
| Payment provider | | |
| App store / marketplace | | |
| Email provider | | |
| Social platform | | |

## 22.4 Kill / pivot rule
**WHY:** Deciding now when to change direction removes emotion later.
> ANSWER (If after {{N}} weeks I have fewer than {{N}} active users AND {{another condition}}, I will {{pivot / pause / stop / change channel}}):

---

# 23. TIMELINE AND OWNERS

> **WHY THIS SECTION EXISTS:** A plan without dates is a wish.

## 23.1 Master timeline
| Phase | Start | End | Planned weeks | Actual end | Gate passed (date) |
|-------|-------|-----|---------------|------------|--------------------|
| 1 BUILD | | | | | |
| 2 TEST | | | | | |
| 3 PRE-LAUNCH | | | | | |
| 4 LAUNCH | | | | | |
| 5 EARLY GROWTH | | | | | |
| 6 SCALE TO 500 | | | | | |

## 23.2 Typical duration guide (adjust honestly)
| Phase | Typical range for a solo builder |
|-------|----------------------------------|
| 1 BUILD | 4 to 12 weeks |
| 2 TEST | 2 to 4 weeks |
| 3 PRE-LAUNCH | 3 to 6 weeks (overlaps with 1 and 2) |
| 4 LAUNCH | 1 to 2 weeks |
| 5 EARLY GROWTH | 4 to 8 weeks |
| 6 SCALE TO 500 | 8 to 16 weeks |

*(These are rough guides, not facts about your product. Replace with your own.)*

## 23.3 Who does what
Solo founder: write your name on every row. Teams: use real names.
| Area | Owner (does the work) | Approver (says yes) | Backup |
|------|-----------------------|---------------------|--------|
| Product / code | | | |
| Design | | | |
| Marketing / content | | | |
| Support | | | |
| Analytics | | | |
| Legal / finance | | | |

## 23.4 Check-in rhythm
| Meeting / check | How often | Where notes go |
|-----------------|-----------|----------------|
| Weekly growth review | Weekly | |
| Phase gate review | End of each phase | Section 24 |
| Budget review | | |
| Risk review | Monthly | Section 22 |

---

# 24. DECISION LOG AND CHANGE LOG

## 24.1 Decision log
Write down every important choice so you do not repeat debates.
| Date | Decision | Options considered | Why this one | Who decided | Review date |
|------|----------|--------------------|--------------|-------------|-------------|
| | | | | | |

## 24.2 Gate log
| Gate | Date | Passed? | What was missing (if failed) | Approved by |
|------|------|---------|------------------------------|-------------|
| 1 BUILD | | | | |
| 2 TEST | | | | |
| 3 PRE-LAUNCH | | | | |
| 4 LAUNCH | | | | |
| 5 EARLY GROWTH | | | | |
| 6 500 USERS | | | | |

## 24.3 Retrospective (fill in at 500 active users)
| Question | Answer |
|----------|--------|
| What worked best? | |
| What wasted the most time or money? | |
| What surprised me about customers? | |
| What would I do differently next time? | |
| What should go into the template for the next project? | |

## 24.4 Template improvement notes
> ANSWER (what in this template was unclear, missing or unnecessary? Send to the template owner):

---

# 25. FINAL REVIEW AND SIGN-OFF

> Do this before calling the plan "ready", and again at each phase gate.

## 25.1 Completeness check (5 points each, total 100)
| # | Check | Points | Score |
|---|-------|--------|-------|
| 1 | Every question answered, N/A with reason, or UNKNOWN with date | 10 | |
| 2 | "Active user" defined precisely and consistently (3.2, 3.3) | 5 | |
| 3 | Customer described with evidence (Section 4) | 10 | |
| 4 | Competitors listed with sources and dates (Section 5) | 5 | |
| 5 | Positioning, headline and proof are clear (Section 6) | 5 | |
| 6 | Price chosen with reasoning and cost per user known (Section 7) | 10 | |
| 7 | Product readiness checks done (Section 8) | 10 | |
| 8 | All six phase gates have clear tick-lists and owners | 10 | |
| 9 | Channels chosen with experiments and stop rules (Section 15, plus 15A, 15B, 15C answered or marked N/A with reason) | 10 | |
| 10 | Funnel math shows how 500 is reachable (Section 16) | 10 | |
| 11 | Metrics, events and dashboard defined (Section 20) | 5 | |
| 12 | Budget, risks and legal items covered (Sections 19, 21, 22) | 10 | |
| | **TOTAL** | **100** | |

**Pass mark: 90.** Below 90? List the gaps below and fix them.

## 25.2 Consistency check
- [ ] The price is the same everywhere it appears.
- [ ] The dates in Section 1, Section 23 and each phase match.
- [ ] The "active user" definition is identical everywhere.
- [ ] Every number has a unit ($, %, hours, users).
- [ ] The budget total matches the per-phase budgets.
- [ ] Every `(ASSUMPTION)` is in the test table (22.2).
- [ ] No secrets, passwords or private data in this file.
- [ ] No leftover `{{placeholders}}` (search the file for `{{`).

## 25.3 "Stranger test"
Give this file to someone who has never seen the project.
- [ ] They can explain, in their own words, who the product is for and why they would use it.
- [ ] They can find the launch date, the price and the owner in under one minute.
- [ ] They can say what happens next without asking you.
> ANSWER (their feedback and my changes):

## 25.4 Sign-off
| Role | Name | Date | Signature / initials |
|------|------|------|----------------------|
| Document owner | | | |
| Reviewer (a different person or an independent AI check plus human) | | | |

---

# 26. GLOSSARY (WORDS EXPLAINED SIMPLY)

| Word | Simple meaning |
|------|----------------|
| Active user | Someone who signed up AND uses the product regularly (defined in 3.2) |
| Activation | The first time a new user does the key action |
| Aha moment | The moment a user first sees real value |
| API | A way for programs to talk to each other |
| Assumption | A belief you have not proven yet |
| Beta | A test version given to a small group before public launch |
| CAC | Customer Acquisition Cost: money and time spent to get one customer or active user |
| Call-to-action (CTA) | The button or sentence telling people what to do next |
| Channel | A road that brings customers to you (search, social, email, etc.) |
| Churn | The share of users who leave in a period |
| Conversion rate | The percent of people who do the next step (for example, visitors who sign up) |
| Early adopter | A person who tries new products first and feels the problem strongly |
| Feature | Something the product does |
| Benefit | What the customer gets from a feature |
| Freemium | A free plan plus paid upgrades |
| Funnel | The steps from stranger to active user |
| Gate | A checkpoint you must pass before moving on |
| GTM | Go-to-Market: your plan for reaching customers |
| ICP | Ideal Customer Profile: the exact type of customer you serve best |
| KPI | Key Performance Indicator: a number that shows progress |
| Landing page | The web page where people arrive and decide to sign up |
| MVP | Minimum Viable Product: the smallest version that solves the core problem |
| North Star metric | The one number that best shows success |
| NPS | Net Promoter Score: how likely users are to recommend you (0-10) |
| Onboarding | Helping new users succeed in their first days |
| Positioning | How you want customers to see you compared with alternatives |
| Retention | The share of users who keep coming back |
| Runway | How long your money and time last |
| SEO | Making your pages easy to find in search engines |
| Unit economics | Whether you earn more from a customer than they cost you |
| Waitlist | A list of people who asked to be told when you launch |

---

# 27. APPENDIX A: AI PROMPT LIBRARY

> Paste a prompt into your AI assistant after replacing every `{{placeholder}}`. Always review the output (Section 2.2).

## A.1 Customer discovery
```
Create an interview guide with 10 questions to learn whether {{customer}} has this problem: {{problem}}.
Rules: ask about past behavior, not future promises; no leading questions; no mention of my product in the first 8 questions.
Add a short note on how to record answers.
```

## A.2 Landing page copy
```
Write landing page copy for {{product}}.
Customer: {{customer}}. Problem in their words: "{{quote}}".
Include: headline (max 10 words), sub-headline (max 25 words), 3 benefit blocks, 1 proof section using ONLY the real proof I provide: {{proof}}, FAQ with 5 questions, one call-to-action.
Use plain language. No hype words. Do not invent testimonials or numbers.
```

## A.3 Launch email to the waitlist
```
Write a launch email under 150 words. From: {{my name}}. Product: {{product}}.
Include: why I built it, what they can do today, one button, the launch offer: {{offer}}.
Tone: {{3 tone words}}. Include a clear unsubscribe line.
```

## A.4 Onboarding email series
```
Write 5 short onboarding emails (days 0, 1, 3, 7, 14) for {{product}}.
Goal of each: {{goals from 17.3}}. The aha moment is: {{aha moment}}.
Each email: subject (max 50 characters), body (max 100 words), one call-to-action.
```

## A.5 Community post (honest, rule-following)
```
Draft a post for the community "{{community}}" whose rules are: {{rules}}.
I built {{product}} to solve {{problem}}. Disclose that I am the builder.
Ask for feedback instead of selling. Keep it under 200 words. No promotional hype.
```

## A.6 Test case generator
```
Here are my features and acceptance rules: {{list}}.
Write test cases: normal use, empty inputs, very long inputs, wrong inputs, slow network, and permission errors.
Format: ID, steps, expected result, priority.
```

## A.7 Risk review
```
Review this GTM plan: {{paste}}.
Act as a skeptical investor. List the 10 weakest assumptions, why each is weak, and one cheap test for each.
```

## A.8 Metrics explainer
```
Explain these metrics to me like I am 12: {{metrics}}.
Then tell me which one to look at first each week and why.
```

## A.9 Consistency checker
```
Read this document: {{paste}}.
List every place where numbers, dates, prices or definitions disagree. Do not fix anything; just list: location, conflict, suggested fix.
```

## A.10 Retrospective helper
```
Here are my weekly notes and metrics: {{paste}}.
Summarize: what drove growth, what slowed it, and 3 changes for the next project template.
Label guesses clearly.
```

---

# 28. APPENDIX B: FILLED-IN MINI EXAMPLE

> This tiny example shows what good answers look like. It is fictional. Do not copy it.

| Question | Example answer |
|----------|----------------|
| 1.1 Project name | PlantPal |
| 1.2 One sentence | PlantPal is a phone app that reminds busy people when to water each houseplant. |
| 3.2 Active user | A person who signed up AND added at least 1 plant in the last 30 days. |
| 4.1 Ideal customer | Busy people aged 25-40 in apartments who own 3+ houseplants and keep killing them. |
| 4.3 Problem in their words | "I always forget to water my plants and they die." (Interview 3, 2026-10-02) |
| 4.4 Pain score | 6/10. People care, but few currently pay for a fix. (ASSUMPTION) |
| 5.5 Why switch | It tells you exactly which plant needs water today, with no setup. |
| 6.3 Headline | Never kill a houseplant again. |
| 7.2 Price | Free for 5 plants; $3/month for unlimited. |
| 7.4 Cost per user | About $0.40/month (hosting + notifications). Profit per paid user about $2.30 after fees. |
| 15.2 Main channel | Short videos about plant care (customers hang out there). |
| 16.3 Funnel | 3% visit-to-sign-up x 50% activation x 40% 30-day retention = 0.6%. For 500 active users I need about 83,000 visitors. (ASSUMPTION) |
| 22.4 Pivot rule | If after 10 weeks I have fewer than 100 active users AND cost per active user is above $8, I will switch to a different customer group. |

---

# 29. APPENDIX C: TROUBLESHOOTING ("WHAT IF...?")

| Problem | What to do |
|---------|-----------|
| "I do not know the answer to a question." | Write `UNKNOWN - will find out by [date]` and add a task to find out. |
| "A question does not apply to my product." | Write `N/A - because ...`. Never delete the question. |
| "I only have guesses, no data yet." | That is normal early on. Write the guess, mark `(ASSUMPTION)`, and add it to table 22.2. |
| "My AI gave me a confident answer I cannot verify." | Treat it as an assumption until you find a source. |
| "I cannot pass a gate." | Stay in the phase. Write what is missing in 24.2. Fix it or consciously change the gate in the Decision Log. |
| "I got 500 sign-ups but few active users." | Sign-ups are not the goal. Look at activation (17.2) and retention (17.4). Fix the first-use path. |
| "Nobody is coming to my landing page." | Revisit Section 15. You may be on the wrong channel, or you may have no channel yet. |
| "People visit but do not sign up." | Improve the headline, proof and button (6.3, 11.3). Test with 5 people. |
| "People sign up but never use it." | Shorten the path to the aha moment (17.1, 17.2). Ask them why. |
| "Costs are higher than income." | Check 7.4 and 16.6. Raise price, limit free use, or reduce AI usage per user. |
| "I feel overwhelmed." | Use the quick-start list (0.6). Do one question at a time. |
| "The plan changed." | Update the document, add a row to the version history (1.9) and the Decision Log (24.1). |

---

# 30. APPENDIX D: READY-TO-USE TRACKING TABLES

> Copy any table below into a spreadsheet, or keep it here. Each table has one example row. Replace the example and add rows as you go.

## D.1 Customer interview tracker
| ID | Date | Person type | Source | Key quote | Pain (1-10) | Would they pay? | Follow-up |
|----|------|-------------|--------|-----------|-------------|-----------------|-----------|
| I-001 | 2026-10-02 | Apartment plant owner | Friend of friend | "I forget to water them." | 6 | Maybe $3/mo (ASSUMPTION) | Invite to beta |

## D.2 Feedback tracker
| ID | Date | User ID | Source | Type (bug/idea/question/praise) | Summary | Impact (L/M/H) | Status | Fixed on |
|----|------|---------|--------|---------------------------------|---------|----------------|--------|----------|
| F-001 | 2026-11-05 | U-014 | Email | Idea | Wants reminders at 8am | M | Planned | |

## D.3 Experiment tracker
| ID | Channel | Hypothesis | Start | End | Cost ($) | Time (hrs) | Success number | Result | Decision (keep/stop/change) |
|----|---------|------------|-------|-----|----------|------------|----------------|--------|-----------------------------|
| E-001 | Short video | If I post 3 videos a week, I get 40 sign-ups in 4 weeks | 2026-12-01 | 2026-12-28 | 0 | 12 | 40 | | |

## D.4 Outreach tracker (direct outreach and B2B)
| ID | Name / company | Role | Source | Date contacted | Message version | Replied? | Call date | Stage | Next step | Next-step date |
|----|----------------|------|--------|----------------|-----------------|----------|-----------|-------|-----------|----------------|
| O-001 | Example Co | Operations lead | Directory | 2026-12-03 | v1 | No | | Contacted | Follow up | 2026-12-07 |

## D.5 Waitlist and sign-up source tracker
| Week starting | Source | Visitors | Sign-ups | Activated | Active at day 30 |
|---------------|--------|----------|----------|-----------|------------------|
| 2026-11-30 | Short video | | | | |

## D.6 Weekly scorecard
| Week | Visitors | Sign-ups | Activated | Active users | Day-7 retention | Revenue | AI cost | Support tickets | Top lesson |
|------|----------|----------|-----------|--------------|-----------------|---------|---------|-----------------|------------|
| 1 | | | | | | | | | |
| 2 | | | | | | | | | |
| 3 | | | | | | | | | |
| 4 | | | | | | | | | |

## D.7 Bug tracker
| ID | Date | Where | Steps to repeat | Severity (Critical/High/Medium/Low) | Owner | Status | Fixed in version |
|----|------|-------|-----------------|-------------------------------------|-------|--------|------------------|
| B-001 | | | | | | Open | |

## D.8 Testimonial and permission tracker
| ID | User | Quote | Date | Permission to use name? | Permission to use photo? | Where used |
|----|------|-------|------|-------------------------|--------------------------|------------|
| T-001 | | | | Yes / No | Yes / No | |

## D.9 Agent action log (from Section 3.9)
| Date | Agent / tool | What it did | Human who checked | Approved? | Notes |
|------|--------------|-------------|-------------------|-----------|-------|
| | | | | | |

## D.10 Spending log
| Date | Item | Category | Amount | Paid by | Approved by | Result |
|------|------|----------|--------|---------|-------------|--------|
| | | | | | | |

---

**END OF TEMPLATE**

*Template maintenance: Review this template after every 5 projects. Keep a list of unclear questions (24.4) and update the version number in the header.*
