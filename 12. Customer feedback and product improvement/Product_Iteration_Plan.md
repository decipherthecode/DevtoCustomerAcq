<!--
TEMPLATE NAME:    Product_Iteration_Plan.md
TEMPLATE VERSION: 1.0
FOLDER:           Customer feedback and product improvement/
BEST FOR:         Solo founder · Web / SaaS apps · Mobile apps · AI-driven development
COVERS:           Build → Internal Test → Closed Beta → Launch → Growth → Review (first 500 customers)
HOW TO REUSE:     Copy this file into a new project folder. Fill every ANSWER line. Never edit the questions.
-->

---
doc_type: product_iteration_plan
template_version: "1.0"
project_name: ""
project_id: ""
owner: ""
status: "DRAFT"          # DRAFT | IN_REVIEW | APPROVED | LIVE | CLOSED
last_updated: ""         # YYYY-MM-DD
current_phase: ""        # P1 | P2 | P3 | P4 | P5 | P6
target_customers: 500
customers_so_far: 0
team_size: "solo"        # solo | small_team | larger_org
fill_path: "fast"        # fast (MUST questions only) | full (everything)
has_ai_features: false   # true → fill PART 9C
has_payments: false      # true → fill PART 4A fully
has_mobile_app: false    # true → fill mobile lines
---

# HOW TO FILL THIS DOCUMENT

Read this part first. It takes 3 minutes.

## What is this document?

This is the **one file** that tells you (and your AI helpers) how your product will go from **"I am building it"** to **"500 real customers are using it and loving it."**

It is a **questionnaire**. You do not write an essay. You answer questions, tick boxes and fill small tables.

## The 7 golden rules

1. **Answer on the `ANSWER:` line.** Write right after the colon. Do not change the questions.
2. **Short is good.** One sentence is usually enough.
3. **Use numbers, not feelings.** Write `20 people`, not `some people`. Write `by 30 Nov`, not `soon`.
4. **Do not guess. Do not leave blanks.** If you do not know, write `UNKNOWN (who finds out, by when)`. Example: `UNKNOWN (me, by 5 Nov)`.
5. **Not needed? Write `N/A` and one reason.** Example: `N/A – no mobile app yet.`
6. **Fill the document in order, top to bottom.** Later parts need the earlier answers.
7. **Update it as you learn.** This is a living plan. Add a line to the Decision Log (Part 12) every time you change your mind.

## Two ways to fill this document

| Path | What you fill | Use it when |
|---|---|---|
| ⚡ **Fast path** | Only ⭐ MUST questions. Skip ➕ OPTIONAL ones. | First draft, small or low-risk project |
| 📘 **Full path** | Everything | Paid product, personal data, AI features, or a team |

Hint: Start with the fast path. Add the optional parts later when you reach that phase. Set `fill_path` at the top.

## Which parts must I fill?

| If your product… | Then fill |
|---|---|
| Is anything | Parts 0–3, 4, 5–8, 9A–9B, 10, 11, 12, 14 |
| Charges money | Part 4A (Pricing and Payments) |
| Collects any personal data (email counts) | Part 4B (Legal and Privacy) |
| Has AI features inside the product | Part 9C (AI Product Safety) |
| Has more than one person on the team | Q3.6–Q3.9 (Bigger Team Add-on) |

Not needed? Write `N/A – reason` at the top of that part.

## Symbols you will see

| Symbol | Meaning |
|---|---|
| `ANSWER:` | Type your answer here |
| `Hint:` | Help for answering |
| `Example:` | A sample answer. Never copy it blindly |
| `[ ]` | Not done yet. Change to `[x]` when done |
| 🛑 **HUMAN GATE** | A real person (you) must say YES before moving on. AI cannot approve this |
| 🤖 **AI JOB** | A task you can give to an AI agent |
| ⭐ **MUST** | Required. The plan is not finished without it |
| ➕ **OPTIONAL** | Fill it if it helps. Otherwise write `N/A` |

## Status words (use only these)

`TODO` · `DOING` · `BLOCKED` · `DONE` · `DROPPED`

## Good answer vs bad answer

| ❌ Bad | ✅ Good |
|---|---|
| `Make it better` | `Cut sign-up from 6 steps to 3 steps by 15 Dec` |
| `Many users` | `50 closed-beta users` |
| `Fix bugs` | `Fix the 5 bugs tagged "blocker" in the backlog (Part 10)` |
| `Ask AI to test` | `QA Agent runs the Part 9 checklist and lists every failure` |

## How AI agents must read this file

- Every question has an ID like `Q2.3`. Refer to answers by ID.
- Treat `ANSWER:` lines as the **only source of truth**. If an answer is `UNKNOWN`, **stop and ask the human. Do not invent it.**
- Never tick a 🛑 HUMAN GATE box. Only the human does.
- After any change, update `last_updated`, `current_phase` and `customers_so_far` at the top of this file.

## How long will it take?

| Part | Time |
|---|---|
| Fast path: Parts 0–4 (before you build) | ~45–60 minutes |
| Full path: Parts 0–4B (before you build) | ~90–120 minutes |
| Phase parts 5–11 (each phase) | ~15–30 minutes per phase, when you reach it |
| Parts 12–14 (logs and final check) | Keep adding as you go |

## The big picture (read once)

```
P1 BUILD → P2 INTERNAL TEST → P3 CLOSED BETA → P4 LAUNCH → P5 GROWTH TO 500 → P6 REVIEW
                                    ▲                              │
                                    └──── feedback → fix → ship ───┘  (the loop never stops)
```

**The loop:** collect feedback → sort it → pick the most important → build the fix → release → tell customers → measure → repeat.

---

# PART 0 — DOCUMENT CONTROL

**Q0.1 — Who owns this plan (one name)?** ⭐ MUST
ANSWER:

**Q0.2 — Where is this project's code, design files and notes stored? (links)** ⭐ MUST
ANSWER:

**Q0.3 — Which AI tools do you use? (names only)** ⭐ MUST
Hint: chat assistant, coding agent, testing tool, analytics helper.
ANSWER:

**Q0.4 — How often will you re-read and update this document?** ➕ OPTIONAL
Hint: Weekly is a good habit.
ANSWER:

---

# PART 1 — PRODUCT SNAPSHOT (What are we making?)

**Q1.1 — Product name** ⭐ MUST
ANSWER:

**Q1.2 — Product type (tick all that apply)** ⭐ MUST
- [ ] Web app / SaaS
- [ ] iOS app
- [ ] Android app
- [ ] AI-powered features inside the product
- [ ] Other: ______

**Q1.3 — Describe your product in ONE sentence a 10-year-old would understand.** ⭐ MUST
Hint: "[Product] helps [who] do [what] so they can [good result]."
Example: `Tidy helps small shops send bills in 1 minute so they get paid faster.`
ANSWER:

**Q1.4 — Who is the ideal customer? (one specific group)** ⭐ MUST
Hint: Job, age or business size, and where they work.
ANSWER:

**Q1.5 — What painful problem do they have today?** ⭐ MUST
ANSWER:

**Q1.6 — How do they solve it today without your product?** ⭐ MUST
ANSWER:

**Q1.7 — Why will they switch to you? (one clear reason)** ⭐ MUST
ANSWER:

**Q1.8 — List the 3–5 features in the first version (MVP). Nothing else.** ⭐ MUST

| # | Feature | Why it is needed | Status |
|---|---|---|---|
| 1 | | | TODO |
| 2 | | | TODO |
| 3 | | | TODO |
| 4 | | | TODO |
| 5 | | | TODO |

**Q1.9 — List 3 things you will NOT build yet.** ⭐ MUST
Hint: Saying "no" now keeps you on schedule.
ANSWER:

**Q1.10 — Which AI features does the product itself use? (if any)** ➕ OPTIONAL
Hint: chatbot, summaries, recommendations, image generation, etc. Write `N/A` if none.
ANSWER:

**Q1.11 — Tech stack (short list)** ⭐ MUST
Hint: language, framework, database, hosting, payment tool, analytics tool.
ANSWER:

---

# PART 2 — GOALS AND SUCCESS NUMBERS (How will we know it worked?)

**Q2.1 — What exactly counts as a "customer" for the number 500?** ⭐ MUST
Pick ONE and never change it mid-project.
- [ ] Signed up (created an account)
- [ ] Activated (did the key first action, see Q2.4)
- [ ] Active (came back in the last 30 days)
- [ ] Paying
ANSWER (write your choice + one sentence why):

**Q2.2 — Start date and target date for reaching 500 customers** ⭐ MUST
ANSWER: Start: ____ · Target: ____

**Q2.3 — The ONE sentence goal for this plan** ⭐ MUST
Example: `Reach 500 activated customers by 31 Jul with at least 40% still active after 30 days.`
ANSWER:

**Q2.4 — What is the "aha moment"? (the first action where a customer sees the value)** ⭐ MUST
Hint: The smallest action that proves the product works for them.
Example: `Sends their first invoice.`
ANSWER:

**Q2.5 — Set your target numbers.** ⭐ MUST

| Metric | What it means | Target | How we measure it |
|---|---|---|---|
| Activation rate | % of sign-ups who reach the aha moment (Q2.4) within 7 days | | |
| Time to first value | Minutes/days from sign-up to aha moment | | |
| Retention (day 30) | % still using it 30 days after sign-up | | |
| Customer happiness | Score from 0–10 ("How likely are you to recommend us?") | | |
| Crash / error rate | % of sessions with an error | | |
| Support load | Number of help requests per 100 customers | | |
| Cost per customer (money) | Total spend ÷ customers | | |
| AI cost per customer (if AI features) | AI usage bill ÷ customers | | |

Hint: Not sure what is "good"? Write your best guess and tag it `GUESS`. Fix it after Phase 3 with real data.

**Q2.6 — What are your customer-count milestones?** ⭐ MUST

| Milestone | Customers | Target date | Phase |
|---|---|---|---|
| M1 | 10 | | P3 |
| M2 | 50 | | P3 |
| M3 | 100 | | P4 |
| M4 | 250 | | P5 |
| M5 | 500 | | P5 |

**Q2.7 — What would make you STOP or CHANGE direction? (kill / pivot rules)** ⭐ MUST
Example: `If activation is below 15% after 100 sign-ups and two fixes, I will re-think the onboarding or the audience.`
ANSWER:

---

# PART 3 — YOUR TEAM: YOU + AI AGENTS (Who does what?)

As a solo founder you wear many hats. List which **AI agent** does each job and what **only you** can decide.

**Q3.1 — Fill the roles table.** ⭐ MUST

| Hat (job) | Who does it | AI tool used | What the AI may do | What ONLY the human decides |
|---|---|---|---|---|
| Product Manager | Human + AI | | Draft plans, sort feedback, write user stories | What to build next, what to drop |
| Product Architect | Human + AI | | Suggest designs and data models | Final design choice |
| Software Engineer | AI agent + Human review | | Write and change code in small steps | Merging code, anything touching money or customer data |
| QA Specialist | AI agent | | Write and run tests, list bugs | Declaring "good enough to ship" |
| Technical Writer | AI agent | | Draft help pages, release notes, emails | Final wording customers see |
| Feedback Analyst | AI agent | | Read, tag and summarise feedback | Which feedback to act on |
| Support / Community | AI agent drafts, Human sends | | Draft replies | Sending sensitive replies |
| Release Manager | AI agent + Human | | Prepare release checklist | Pressing the "release" button |

**Q3.2 — The 8 safety rules for AI helpers. Tick the ones you accept.** ⭐ MUST
- [ ] AI never gets live passwords, payment keys or production database access
- [ ] AI works in small tasks (one change at a time) and shows its work
- [ ] A human reads every change before it goes live
- [ ] AI must say "I don't know" instead of guessing
- [ ] AI never sends messages to customers without human approval
- [ ] AI never deletes customer data
- [ ] Every AI-made decision is written in the Decision Log (Part 12)
- [ ] There is a way to undo (roll back) every release (see Q9.5)

**Q3.3 — Which actions need 🛑 HUMAN GATE approval in this project?** ⭐ MUST
Hint: Keep gates for risky things only (money, customer data, public messages, releases). Too many gates become "click yes without reading".
ANSWER:

**Q3.4 — How many hours per week can you give this project?** ⭐ MUST
ANSWER:

**Q3.5 — Does anyone else help (friend, freelancer, advisor)? Their role?** ➕ OPTIONAL
ANSWER:

## Bigger Team Add-on (➕ OPTIONAL — solo founders write `N/A – solo`)

**Q3.6 — Who is on the team and what do they own?** ➕ OPTIONAL

| Name | Role | Owns which Parts / phases | Approves which 🛑 gates | Backup person |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

**Q3.7 — Meeting rhythm** ➕ OPTIONAL
Example: `Mon 15 min plan the iteration · Fri 30 min demo and numbers review.`
ANSWER:

**Q3.8 — Who is the ONE person who gives the final YES on each gate?** ➕ OPTIONAL
Hint: One name per gate. Never "everyone".

| Gate | Final decider | Must be consulted first |
|---|---|---|
| Phase 1 → 2 (Build done) | | |
| Phase 2 → 3 (Invite real people) | | |
| Phase 3 → 4 (Public launch) | | |
| Phase 4 → 5 (Scale up) | | |
| Every release | | |
| Customer-facing messages | | |

**Q3.9 — What happens when two people disagree?** ➕ OPTIONAL
Example: `Look at the numbers. If no numbers exist, run a 1-week test. If still stuck, the product owner decides.`
ANSWER:

---

# PART 4 — THE FEEDBACK SYSTEM (How do we hear customers?)

**Q4.1 — Where will feedback come from? Tick all and say who checks it.** ⭐ MUST

| Channel | Use? | Who checks it | How often |
|---|---|---|---|
| In-app feedback button / form | [ ] | | |
| Email | [ ] | | |
| 1-to-1 calls / video chats | [ ] | | |
| Short survey (after the aha moment) | [ ] | | |
| App store reviews (mobile) | [ ] | | |
| Social media / community group | [ ] | | |
| Support chat | [ ] | | |
| Usage data (what people click) | [ ] | | |
| Error reports / crash logs | [ ] | | |
| AI conversation logs (if AI features) | [ ] | | |

**Q4.2 — Which 3 questions will you ask every customer?** ⭐ MUST
Examples: `What nearly stopped you from using it?` · `What is the one thing you would change?` · `How would you feel if you could no longer use it?`
ANSWER:

**Q4.3 — When will you ask? (the moment)** ⭐ MUST
Example: `Right after first success, on day 7, and on day 30.`
ANSWER:

**Q4.4 — Where will ALL feedback be stored? (one place only)** ⭐ MUST
Hint: One sheet, board or folder. Link it.
ANSWER:

**Q4.5 — Feedback tags. Every piece of feedback gets ONE type and ONE area.** ⭐ MUST

| Type tag | Meaning |
|---|---|
| `BUG` | Something is broken |
| `IDEA` | Customer wants something new |
| `CONFUSION` | Customer did not understand |
| `PRAISE` | Customer is happy (keep this safe!) |
| `COMPLAINT` | Customer is unhappy but no clear fix |
| `QUESTION` | Customer needs an answer |

Area tags (edit for your product): `ONBOARDING` · `CORE_FEATURE` · `BILLING` · `SPEED` · `DESIGN` · `AI_QUALITY` · `OTHER`

**Q4.6 — How do you pick WHAT to fix first? Score each item 1–5.** ⭐ MUST

| Score | Question | 1 = low · 5 = high |
|---|---|---|
| **Impact** | How many customers does it affect, and how badly? | |
| **Reach to goal** | Does it help the Part 2 goal (activation / retention)? | |
| **Effort** (reverse) | How easy is it? (5 = very easy, 1 = very hard) | |
| **Confidence** | How sure are we it is a real problem? | |

**Priority score = Impact + Reach + Effort + Confidence (max 20).**
ANSWER (any change to this rule you want):

**Q4.7 — Emergency rule: what counts as a "drop everything" problem?** ⭐ MUST
Example: `Customers cannot log in, data is lost, wrong charges, security problem.`
ANSWER:

**Q4.8 — Reply promise: how fast will you answer customers?** ⭐ MUST
Example: `Within 1 working day. Emergencies within 2 hours.`
ANSWER:

**Q4.9 — How will you tell customers "we heard you and fixed it"?** ⭐ MUST
Hint: Release notes, email, in-app message. Closing the loop keeps customers giving feedback.
ANSWER:

**Q4.10 — Privacy: what do you promise about their feedback and data?** ⭐ MUST
Hint: Ask permission before quoting anyone. Never put passwords, card numbers or private details in the feedback sheet.
ANSWER:

---

# PART 4A — PRICING AND PAYMENTS 💳

Fill this if your product will ever charge money. Free forever? Write `N/A – free` at the top and skip.
Fill before Phase 3 ends. Test prices with real people, not just guesses.

**Q4A.1 — Is the product free, paid, or both?** ⭐ MUST
- [ ] Free
- [ ] Free trial then paid (length: ____ days)
- [ ] Free plan + paid upgrade
- [ ] Paid from day one
- [ ] Not decided yet (decide by: ______)

**Q4A.2 — What is the product worth to the customer in money or time?** ⭐ MUST
Example: `Saves 3 hours a week. At their pay rate that is worth about $60 per week.`
ANSWER:

**Q4A.3 — Plans and prices** ⭐ MUST

| Plan | Price and billing period | What is included | Who it is for | Tested with how many people | Result |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |

**Q4A.4 — How will you test the price?** ⭐ MUST
Hint: Ask 10 people: "At what price would this be so cheap you doubt it? A bargain? Getting expensive? Too expensive?" Or show two prices to two groups.
ANSWER:

**Q4A.5 — What do beta customers pay when the beta ends?** ⭐ MUST
Example: `Free for the first 3 months, then 50% off for 12 months.`
ANSWER:

**Q4A.6 — Money math** ⭐ MUST

| Number | Value |
|---|---|
| Price per customer per month | |
| Cost to serve one customer per month (hosting, AI usage, tools, payment fees) | |
| Profit per customer per month | |
| Fixed monthly costs | |
| Customers needed to break even | |

**Q4A.7 — Payment tools and rules** ⭐ MUST

| Question | Answer |
|---|---|
| Which payment provider do you use? | |
| Do you store card numbers yourself? (Answer must be NO. Let the provider handle it.) | |
| Which currencies and countries? | |
| Who handles sales tax / VAT and invoices or receipts? | |
| Refund rule (how many days, who approves) | |
| What happens when a payment fails? (retry, email, pause access) | |
| How does a customer cancel? (must be easy and clear) | |

**Q4A.8 — Mobile only: payment through the app store?** ➕ OPTIONAL
Hint: Apple and Google have their own rules and fees for selling digital goods inside apps. Read the **current** store rules before you design the payment flow. Write what you found and the date you checked.
ANSWER:

**Q4A.9 — Payment safety checklist** ⭐ MUST
- [ ] Payments tested in the provider's test mode
- [ ] One small real payment tested and refunded
- [ ] Customers get a receipt
- [ ] Failed and cancelled payments are handled with clear messages
- [ ] You can see who paid and who did not (a simple list or dashboard)
- 🛑 **HUMAN GATE:** I approve the pricing and the payment flow.  [ ] Approved on: ______

🤖 **AI JOBS:** Summarise price-test answers · calculate break-even · draft pricing page text · list edge cases (refund, failed payment, cancel) to test. AI never touches live payment keys.

---

# PART 4B — LEGAL AND PRIVACY 🔒

Fill this if you collect any personal data (even just an email address) or accept payments.
**This section is a checklist to help you ask the right questions. It is not legal advice.** Rules differ by country and change over time. Before launch, ask a qualified professional if you handle sensitive data, payments, health, children's data, or customers in several countries.

**Q4B.1 — Where are you based, and where will your customers be?** ⭐ MUST
ANSWER:

**Q4B.2 — What personal data do you collect?** ⭐ MUST
Hint: Include emails, names, phone numbers, locations, payment details, usage data, and anything people type into the product.

| Data | Why you need it | Where stored | Who can see it | How long you keep it | Can customers delete it? |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |

**Q4B.3 — Does your product collect data from children?** ⭐ MUST
Hint: Many countries have strict rules for children's data. If YES, stop and get professional advice before building further.
ANSWER: Yes / No

**Q4B.4 — Required pages and notices. Tick when live.** ⭐ MUST
- [ ] Privacy policy (says what you collect, why, who you share it with, how to ask questions)
- [ ] Terms of service
- [ ] Cookie / tracking notice with a real choice (if you use analytics or ads)
- [ ] Marketing emails only to people who agreed, with an unsubscribe link
- [ ] Contact email for privacy questions: ______

**Q4B.5 — How can customers see, export or delete their data? What is your time promise?** ⭐ MUST
Example: `Email privacy@... or use Settings → Delete account. Done within 14 days.`
ANSWER:

**Q4B.6 — Tools that touch customer data (analytics, email, payments, support, AI provider)** ⭐ MUST

| Tool | What customer data it gets | Privacy terms read? | Data location | Can be removed? |
|---|---|---|---|---|
| | | | | |
| | | | | |

**Q4B.7 — AI providers: do you send customer data to an AI provider?** ⭐ MUST (write `N/A` if no AI)
Hint: Check whether your data is used for training, how long it is kept, and what settings you can change. Remove personal details before sending whenever you can.
ANSWER:

**Q4B.8 — Security basics** ⭐ MUST
- [ ] Passwords stored safely (hashed by a trusted library, never plain text)
- [ ] Everything travels over HTTPS
- [ ] Secret keys are kept outside the code, and not shared with AI tools
- [ ] Each person can see only their own data
- [ ] Two-step login turned on for your own accounts (hosting, code, payments, email)
- [ ] Backups run automatically, and a restore was tested
- [ ] You know what to do if data leaks (Q4B.9)

**Q4B.9 — If something goes wrong with customer data, what will you do?** ⭐ MUST
Hint: Stop the problem, find out who is affected, tell them quickly and honestly, and check whether the law requires you to tell an authority by a deadline.
ANSWER:

**Q4B.10 — Content and licence check** ⭐ MUST
- [ ] Images, icons, fonts and music are licensed for commercial use
- [ ] Open-source libraries' licences allow your use
- [ ] Product name and logo checked so you do not copy someone else's
- [ ] (Mobile) Store listing rules and age rating understood

**Q4B.11 — Who reviewed your legal pages and when?** ⭐ MUST
ANSWER:
- 🛑 **HUMAN GATE:** I accept responsibility for the legal and privacy answers above.  [ ] Approved on: ______

🤖 **AI JOBS:** Draft a first version of privacy policy and terms for review · list the data you collect from the code · flag third-party tools that send data out. A human or professional reviews everything before it goes live.

---

# PART 5 — PHASE 1: BUILD 🔨

**Phase purpose:** Make the first version that does the one important job from Q1.3.
**Customers in this phase:** 0 (only you).
**Typical mistakes:** adding extra features · forgetting usage tracking · no feedback button · building everything before showing anyone.

**Q5.1 — Start date / target end date** ⭐ MUST
ANSWER:

**Q5.2 — Build plan in slices. Each slice must be small enough to finish in 1–3 days.** ⭐ MUST

| Slice | What it delivers (one result a person can see) | Done when… (test) | AI agent | Status |
|---|---|---|---|---|
| S1 | | | | TODO |
| S2 | | | | TODO |
| S3 | | | | TODO |
| S4 | | | | TODO |
| S5 | | | | TODO |

**Q5.3 — Design basics ready?** ⭐ MUST
- [ ] Screens or sketches exist for the main journey (sign-up → aha moment)
- [ ] Words on screen are simple (no jargon)
- [ ] Works on a phone-size screen (web) / right screen sizes (mobile)
- [ ] Error messages tell people what to do next

**Q5.4 — Basics every product needs. Tick when built.** ⭐ MUST
- [ ] Sign-up / log-in / password reset
- [ ] Core feature(s) from Q1.8
- [ ] Feedback button or form (so Phase 3 can start)
- [ ] Usage tracking for the aha moment (Q2.4)
- [ ] Error and crash logging
- [ ] Backups of customer data
- [ ] Privacy policy and terms pages
- [ ] (If paid) Payment flow tested in test mode
- [ ] (If AI features) Spending limit and fallback message when AI fails

**Q5.5 — Biggest risks while building (top 3) and what you will do** ⭐ MUST
ANSWER:

🤖 **AI JOBS in this phase:** Break features into slices · write code in small steps · write tests for each slice · draft help text.

**Phase 1 EXIT CHECK**
- [ ] All Q1.8 features work end-to-end on a test account
- [ ] Q5.3 and Q5.4 are ticked
- [ ] No known "blocker" bugs
- 🛑 **HUMAN GATE:** I (the owner) approve moving to Phase 2.  [ ] Approved on: ______

---

# PART 6 — PHASE 2: INTERNAL TEST 🧪

**Phase purpose:** Find and fix problems before any outside person sees it.
**Customers in this phase:** 0 (you + 2–5 trusted helpers, optional).
**Typical mistakes:** testing only on your own device · fixing small bugs while blockers remain · helping testers instead of watching where they get stuck.

**Q6.1 — Who will test? (you, friends, family, other founders)** ⭐ MUST
ANSWER:

**Q6.2 — List the 5 most important customer journeys to test** ⭐ MUST
Example: `Sign up → create first invoice → send it → get paid → log out.`

| # | Journey (start → end) | Web | Phone browser | iOS | Android | Result |
|---|---|---|---|---|---|---|
| 1 | | [ ] | [ ] | [ ] | [ ] | |
| 2 | | [ ] | [ ] | [ ] | [ ] | |
| 3 | | [ ] | [ ] | [ ] | [ ] | |
| 4 | | [ ] | [ ] | [ ] | [ ] | |
| 5 | | [ ] | [ ] | [ ] | [ ] | |

**Q6.3 — Quality check (Part 9 checklist) completed?** ⭐ MUST
ANSWER: Yes / No — link to results:

**Q6.4 — Bug count** ⭐ MUST

| Severity | Meaning | Found | Fixed | Left |
|---|---|---|---|---|
| Blocker | Stops the main journey, loses data, security problem | | | |
| Major | Hurts the experience, there is a workaround | | | |
| Minor | Small annoyance | | | |

**Q6.5 — Beta readiness: can a stranger finish Journey #1 without your help?** ⭐ MUST
Hint: Watch one person try it. Do not help. Write down where they got stuck.
ANSWER:

🤖 **AI JOBS:** Write and run tests · try weird inputs · list bugs by severity · check speed · check accessibility basics.

**Phase 2 EXIT CHECK**
- [ ] 0 blocker bugs · 0 major bugs on the main journey
- [ ] A stranger finished Journey #1 alone
- [ ] Feedback tools work (a test message reached Q4.4)
- [ ] Rollback tested (Q9.5)
- 🛑 **HUMAN GATE:** I approve inviting real people.  [ ] Approved on: ______

---

# PART 7 — PHASE 3: CLOSED BETA 🧑‍🤝‍🧑 (first 10 → 50 customers)

**Phase purpose:** Learn from a small, friendly group. Fix the biggest problems fast. Prove people get value.
**Customers in this phase:** 10 to 50.
**Typical mistakes:** inviting people who are not your ideal customer (Q1.4) · asking only "Do you like it?" · not replying to feedback · changing too many things at once to know what helped.

**Q7.1 — Who is invited? Describe the perfect beta tester.** ⭐ MUST
ANSWER:

**Q7.2 — How will you find them? (list channels and target numbers)** ➕ OPTIONAL

| Channel | How many invites | How many joined |
|---|---|---|
| | | |
| | | |

**Q7.3 — What do beta testers get? (free access, discount, name in credits, direct line to you)** ⭐ MUST
ANSWER:

**Q7.4 — Welcome message (write it here)** ⭐ MUST
Hint: Say what the product is, what you need from them, how to give feedback, and how long the beta lasts.
ANSWER:

**Q7.5 — How long is each feedback round?** ⭐ MUST
Example: `1 week of use → 2 days of fixes → release → next round.`
ANSWER:

**Q7.6 — Beta exit rules. All must be true to leave beta.** ⭐ MUST

| Rule | Target | Actual |
|---|---|---|
| Customers who joined | at least 10 (M1) → 50 (M2) | |
| Activation rate | ≥ Q2.5 target | |
| Customers who say they would be "very disappointed" without it | ≥ 40% | |
| Blocker bugs open | 0 | |
| Top 3 feedback problems fixed | Yes | |

**Q7.7 — Feedback round log.** Copy one row per round.

| Round | Dates | Customers | Feedback items | Top 3 problems | Fixed & shipped | Notes |
|---|---|---|---|---|---|---|
| R1 | | | | | | |
| R2 | | | | | | |
| R3 | | | | | | |

🤖 **AI JOBS:** Read and tag all feedback (Q4.5) · group similar items · score with Q4.6 · write a one-page summary for you · draft thank-you and "we fixed it" messages · turn top problems into small build slices.

**Phase 3 EXIT CHECK**
- [ ] Q7.6 rules met
- [ ] Pricing / plan idea tested with real people (even if just a conversation)
- [ ] Support answers and help pages cover the top 10 questions
- [ ] Launch message drafted (Part 8)
- 🛑 **HUMAN GATE:** I approve the public launch.  [ ] Approved on: ______

---

# PART 8 — PHASE 4: LAUNCH 🚀 (customers 50 → 100)

**Phase purpose:** Open the doors safely and let more people in.
**Customers in this phase:** 50 to 100.
**Typical mistakes:** launching with no monitoring · launching late on a Friday · submitting to app stores too late for review · promising features that do not exist yet.

**Q8.1 — Launch date and time** ⭐ MUST
ANSWER:

**Q8.2 — Launch type** ⭐ MUST
- [ ] Soft launch (open to a waiting list in batches)
- [ ] Public launch (anyone can sign up)
- [ ] Store launch (App Store / Google Play) — approval time planned: ______

**Q8.3 — Where will you announce it? (list places and dates)** ⭐ MUST
Examples: email list, social posts, communities, product directories, partner shout-outs.
ANSWER:

**Q8.4 — Launch message (write the main text here)** ⭐ MUST
Hint: Use Q1.3. Show the problem, the fix and one clear button: "Try it".
ANSWER:

**Q8.5 — Launch week checklist** ⭐ MUST
- [ ] Site and app tested on a fresh account
- [ ] Servers can handle many sign-ups at once (load tested or scaling turned on)
- [ ] Payments work with real cards in a small test (if paid)
- [ ] Monitoring and alerts on (errors, slow pages, server down)
- [ ] Help page, FAQ and contact method are live
- [ ] Terms, privacy policy and cookie notice are live
- [ ] Analytics dashboard shows sign-ups and the aha moment in real time
- [ ] Rollback plan written and tested (Q9.5)
- [ ] Who watches the product during launch day: ______
- [ ] Sleep plan: you are not working 24 hours straight

**Q8.6 — Launch day watch. Check these every few hours.** ➕ OPTIONAL

| Time | Sign-ups | Activated | Errors | Support messages | Action taken |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |

**Q8.7 — What will you do if something goes wrong on launch day?** ⭐ MUST
Hint: Pause sign-ups? Roll back? Post a status message? Write the steps.
ANSWER:

**Q8.8 — First 2 weeks plan after launch** ⭐ MUST
Example: `Daily: check errors and feedback. Every 3 days: ship one fix. Day 14: review numbers vs Part 2.`
ANSWER:

🤖 **AI JOBS:** Draft announcement posts and emails · prepare FAQ · write release notes · watch dashboards and flag unusual numbers · draft replies to support messages.

**Phase 4 EXIT CHECK**
- [ ] Launch week checklist (Q8.5) complete
- [ ] 100 customers reached (M3) OR a written reason and new date
- [ ] Activation and error numbers are within 20% of Part 2 targets
- [ ] No open blocker bugs
- 🛑 **HUMAN GATE:** I approve scaling up growth efforts.  [ ] Approved on: ______

---

# PART 9 — QUALITY AND RELEASE RULES (use in EVERY phase)

## 9A. Quality checklist (run before every release)

**Q9.1 — Tick the checks that apply to your product.** ⭐ MUST

**Works**
- [ ] Main journey works end-to-end
- [ ] New change does not break old features (regression check)
- [ ] Works in the main browsers (Chrome, Safari, Edge, Firefox) — web
- [ ] Works on small and large phone screens
- [ ] Works on the latest and one older OS version — mobile
- [ ] Works with a slow internet connection and when offline (mobile)

**Safe**
- [ ] Passwords and keys are not visible in code or logs
- [ ] People can only see their own data
- [ ] Customer data is backed up and a restore was tested once
- [ ] (AI features) AI cannot reveal other customers' data; bad answers are handled with a safe message

**Easy**
- [ ] Words are clear and error messages help
- [ ] Buttons are big enough to tap; text is readable; colors have good contrast
- [ ] Sign-up takes no more steps than needed

**Fast**
- [ ] Main pages/screens load in under 3 seconds on a normal connection
- [ ] App does not crash during the main journey

**Mobile store rules (if mobile)**
- [ ] Store listing text, screenshots and icon ready
- [ ] Privacy details and permission explanations ready
- [ ] Test accounts for the store reviewers ready
- [ ] Release is staged (small % of people first) if the store allows it

## 9B. Release steps

**Q9.2 — How often will you release?** ⭐ MUST
Example: `Small fixes anytime. Bigger changes on Fridays only after 10:00.`
ANSWER:

**Q9.3 — Release recipe (edit if needed)** ⭐ MUST
1. Pick the items from the backlog (Part 10)
2. AI writes/updates tests; AI lists what changed
3. Run Q9.1 checklist
4. Human reads changes 🛑
5. Release to a small group first (if possible)
6. Watch errors for 30 minutes
7. Release to everyone
8. Write release note and tell customers (Q4.9)

**Q9.4 — Release note format** ⭐ MUST
Example: `What's new · What we fixed · Thanks to everyone who told us about [thing].`
ANSWER:

**Q9.5 — Rollback plan: how do you undo a bad release in under 15 minutes?** ⭐ MUST
Hint: Write the exact steps. Test it once before launch.
ANSWER:

**Q9.6 — "Done" means all of these** ⭐ MUST
- [ ] Code reviewed by a human
- [ ] Tests pass
- [ ] Checklist Q9.1 passed
- [ ] Help page / release note updated
- [ ] Customer who reported it told (if known)

---

# PART 9C — AI PRODUCT SAFETY 🤖🛡️

Fill this ONLY if your product has AI features that customers use (chat, summaries, recommendations, generated text or images). No AI inside the product? Write `N/A – no AI features`.

**Q9.7 — What is the AI allowed to do, and what must it NEVER do?** ⭐ MUST
Example: `Allowed: summarise a customer's own invoices. Never: give legal or medical advice, reveal other customers' data, or take actions (send email, charge money) without a click from the customer.`
ANSWER:

**Q9.8 — Test set: 20 real-style questions with the good answer described.** ⭐ MUST
Hint: Include easy ones, tricky ones, and ones where the right answer is "I don't know". Re-run this set before every release that changes prompts, models or settings.

| # | Customer input | What a good answer looks like | Actual answer (summary) | Pass? |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| … | | | | |

**Q9.9 — Pass mark and what happens if the AI fails it** ⭐ MUST
Example: `At least 18 of 20 pass, and 0 unsafe answers. Otherwise the release waits.`
ANSWER:

**Q9.10 — What happens when the AI is wrong or unsure?** ⭐ MUST
Hint: Allow "I'm not sure". Show where the answer came from when possible. Give an easy way to reach a human or fix the answer.
ANSWER:

**Q9.11 — Trick and abuse tests** ⭐ MUST
- [ ] Tried to make the AI reveal its hidden instructions
- [ ] Tried to make the AI show another customer's data
- [ ] Tried to make the AI do something it must not (Q9.7)
- [ ] Pasted harmful or confusing text into the product to see if the AI obeys it
- [ ] Tried very long, empty, and wrong-language inputs

**Q9.12 — Cost limits** ⭐ MUST

| Limit | Value | What happens when reached |
|---|---|---|
| AI cost per customer per day | | |
| AI cost per month for the whole product | | |
| Alert when spending reaches | | |

**Q9.13 — Do customers know it is AI?** ⭐ MUST
- [ ] AI-made content is labelled
- [ ] The limits of the AI are explained in plain words
- [ ] Every AI answer has a 👍 / 👎 button, and 👎 feedback goes to Q4.4 tagged `AI_QUALITY`

**Q9.14 — Model changes** ⭐ MUST
Hint: AI providers update or retire models. Write which model and version you use. When it changes, re-run Q9.8 before switching.
ANSWER: Model and version: ______ · Last tested on: ______

**Q9.15 — What AI data do you keep, for how long, and who can read it?** ⭐ MUST
ANSWER:

🤖 **AI JOBS:** Draft the 20-question test set (you review it) · run it and score results · report failures with examples · never score its own work as final. 🛑 A human signs off on every AI quality result.

---

# PART 10 — ITERATION ENGINE (the repeating loop)

**Q10.1 — Iteration length** ⭐ MUST
Hint: 1 week is common for beta; 1–2 weeks for growth.
ANSWER:

**Q10.2 — The loop (follow every iteration)** ⭐ MUST

| Step | What happens | Who |
|---|---|---|
| 1. Collect | Gather all new feedback and numbers | Feedback Analyst (AI) |
| 2. Sort | Tag and score using Q4.5 and Q4.6 | AI proposes, human confirms 🛑 |
| 3. Choose | Pick the top items that fit this iteration (max 3–5) | Human |
| 4. Build | Slice into small tasks and build | AI + human review |
| 5. Test | Run Q9.1 checklist | QA Agent |
| 6. Release | Follow Q9.3 | Human presses the button 🛑 |
| 7. Tell | Message customers (Q4.9) | AI drafts, human approves |
| 8. Measure | Compare numbers before and after | AI + human |
| 9. Learn | Write one lesson in the iteration log | Human |

**Q10.3 — Backlog (list of everything we might do).** Keep sorted by priority score.

| ID | Title | Type (Q4.5) | Area | Source (who/where) | Score /20 | Status | Iteration |
|---|---|---|---|---|---|---|---|
| B-001 | | | | | | TODO | |
| B-002 | | | | | | TODO | |
| B-003 | | | | | | TODO | |

**Q10.4 — Iteration log.** One row per iteration.

| # | Dates | Goal (one sentence) | Shipped | Number before → after | Lesson learned |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

**Q10.5 — Rule: how do you decide NOT to build something?** ⭐ MUST
Example: `If fewer than 3 customers ask and it does not help activation or retention, it waits.`
ANSWER:

---

# PART 11 — PHASE 5: GROWTH TO 500 📈 (customers 100 → 500) AND PHASE 6: REVIEW 🔍

## Phase 5: Growth

**Phase purpose:** Bring in more of the *right* customers and keep them.
**Customers in this phase:** 100 to 500.
**Typical mistakes:** chasing sign-ups while activation is low · trying five channels at once · ignoring costs · stopping the feedback loop because "it is working".

**Q11.1 — Which 2–3 ways will you find customers? (be specific)** ⭐ MUST
Examples: content, communities, direct outreach, partnerships, referrals, ads, app store search.

| Channel | Weekly effort | Expected sign-ups / week | Cost | Actual |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

**Q11.2 — Onboarding: what happens in a customer's first 7 days?** ⭐ MUST
Hint: Welcome message, first-win guide, check-in on day 3, feedback ask on day 7.
ANSWER:

**Q11.3 — How will you keep customers coming back?** ⭐ MUST
Examples: useful emails, reminders, new features they asked for, helpful tips.
ANSWER:

**Q11.4 — Referral and happy-customer plan** ➕ OPTIONAL
Hint: Ask delighted customers for a review, a testimonial (with permission) or an introduction.
ANSWER:

**Q11.5 — Cost check: can you afford 500 customers?** ⭐ MUST

| Item | Cost per month at 100 customers | At 500 customers |
|---|---|---|
| Hosting / servers | | |
| AI usage (if any) | | |
| Tools and subscriptions | | |
| Support time | | |
| Ads / marketing | | |
| **Total** | | |

**Q11.6 — If numbers are bad, what is the fix list? (decide now, use later)** ⭐ MUST

| If this is low… | First thing to try |
|---|---|
| Sign-ups | Change the message, channel or audience |
| Activation | Shorten the path to the aha moment; improve onboarding |
| Retention | Ask churned customers why; add reminders or value |
| Happiness | Fix the top complaint; talk to 5 unhappy customers |
| Cost per customer | Cut the least useful channel; reduce AI usage cost |

**Q11.7 — Weekly growth log.**

| Week | New customers | Total | Activation % | Day-30 retention % | Happiness score | Biggest lesson |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |

🤖 **AI JOBS:** Weekly numbers report · churn reasons summary · draft emails and help articles · suggest experiments (you choose) · keep backlog sorted.

**Phase 5 EXIT CHECK**
- [ ] 500 customers by the Q2.1 definition (M5), dated: ______
- [ ] Activation, retention and happiness targets met (or reasons written)
- [ ] No blocker bugs; support answers within the Q4.8 promise
- [ ] Costs are sustainable (Q11.5)
- 🛑 **HUMAN GATE:** I declare the 500-customer goal reached.  [ ] Approved on: ______

## 11A. Growth plan detail (marketing for the first 500)

**Q11A.1 — Where do your ideal customers (Q1.4) already spend time? List 5 places.** ⭐ MUST
Hint: Online groups, forums, newsletters, social platforms, events, search terms they type, other tools they use.
ANSWER:

**Q11A.2 — Your message** ⭐ MUST

| Part | Your words |
|---|---|
| Headline (the result they get) | |
| 3 proof points (numbers, quotes, demos) | |
| One clear button (e.g., "Try it free") | |
| Message A / B to test (what differs) | |

**Q11A.3 — Funnel math: how many people must you reach to get 500?** ⭐ MUST

| Step | Target conversion | Actual | People needed for 500 |
|---|---|---|---|
| Reached / visited | | | |
| Signed up | | | |
| Activated (aha moment) | | | |
| Still active at day 30 | | | |
| Paying (if paid) | | | |

Hint: Work backwards from 500. Example: if 40% of sign-ups activate, you need 1,250 sign-ups to get 500 activated customers.

**Q11A.4 — Weekly routine (small, repeatable, written down)** ⭐ MUST
Example: `Each week: 2 helpful posts, 20 personal messages to ideal customers, 1 answer in a community, 1 customer story.`
ANSWER:

**Q11A.5 — Marketing assets ready? Tick when done.** ⭐ MUST
- [ ] Simple landing page with a clear button
- [ ] 60-second demo video or 3 screenshots
- [ ] Waiting list / email list with target size: ______
- [ ] One customer story or testimonial (with permission)
- [ ] Share link with tracking so you know which channel brought each sign-up

**Q11A.6 — Experiments log.** Rule: one experiment per channel at a time. ➕ OPTIONAL

| Idea | What we expect | Length | Success number | Result | Keep / Drop |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |

**Q11A.7 — Paid ads (skip if none): budget and stop rule** ➕ OPTIONAL
Example: `Max $200 for 2 weeks. Stop if cost per activated customer is above $15.`
ANSWER:

**Q11A.8 — Fair play rules** ⭐ MUST
- [ ] I read each community's rules before posting
- [ ] No fake reviews, no fake accounts, no buying reviews
- [ ] I say who I am when I promote my own product
- [ ] I do not message strangers in a way that looks like spam
- [ ] Claims about the product are true and I can prove them

🤖 **AI JOBS:** Draft messages A/B · create the funnel math · draft the weekly posts (you edit and publish) · summarise which channels brought activated customers. AI never posts or messages on your behalf without 🛑 your approval.

## Phase 6: Review (Look back, decide next)

**Typical mistakes:** skipping the review; keeping lessons in your head; changing the 500 definition afterward.

**Q11.8 — Did we reach the goal in Q2.3? Yes / Partly / No — the numbers** ⭐ MUST
ANSWER:

**Q11.9 — What are the 3 things that worked best?** ⭐ MUST
ANSWER:

**Q11.10 — What are the 3 things that wasted time or money?** ⭐ MUST
ANSWER:

**Q11.11 — What did customers love most? (their own words, with permission)** ⭐ MUST
ANSWER:

**Q11.12 — What did customers complain about most, and is it fixed?** ⭐ MUST
ANSWER:

**Q11.13 — What did the AI helpers do well? Where did they need correcting?** ⭐ MUST
ANSWER:

**Q11.14 — What will you do differently in the next project? (add to this template)** ⭐ MUST
ANSWER:

**Q11.15 — Next step** ⭐ MUST
- [ ] Keep iterating toward the next goal (write a new Q2.3: ______)
- [ ] Hand over to a bigger team
- [ ] Pause the product
- [ ] Stop the product (plan to inform customers and export their data: ______)

---

# PART 12 — LOGS (keep adding)

## 12A. Decision Log
Write every important choice, including choices made with AI help.

| Date | Decision | Why | Alternatives rejected | Made by (human / AI+human) |
|---|---|---|---|---|
| | | | | |
| | | | | |

## 12B. Risk Log

| # | Risk (what could go wrong) | Chance (L/M/H) | Damage (L/M/H) | What we will do | Owner | Status |
|---|---|---|---|---|---|---|
| R1 | Customers do not understand the product | | | | | |
| R2 | A serious bug harms customer data | | | | | |
| R3 | Too few sign-ups | | | | | |
| R4 | Running costs (hosting / AI) grow faster than income | | | | | |
| R5 | Store rejects the app (mobile) | | | | | |
| R6 | You run out of time or energy | | | | | |
| R7 | An AI mistake reaches customers | | | | | |

## 12C. Assumptions (things we believe but have not proven) ➕ OPTIONAL

| # | Assumption | How we will test it | Result |
|---|---|---|---|
| A1 | | | |
| A2 | | | |

## 12D. Questions waiting for answers (UNKNOWN items)

| ID | Question | Who finds out | By when | Answer |
|---|---|---|---|---|
| | | | | |

## 12E. Change History of this document

| Date | Version | What changed | Changed by |
|---|---|---|---|
| | 1.0 | First version | |

---

# PART 13 — COPY-AND-PASTE PROMPTS FOR YOUR AI HELPERS

Replace `[ ... ]` parts. Always paste this line first:
`Read Product_Iteration_Plan.md. Use only the ANSWER lines as facts. If something is UNKNOWN, ask me. Do not guess.`

**P-1 Build slices**
`Using Q1.8 and Q1.11, split each feature into build slices that take 1–3 days. For each slice give: what a person can see, a "done when" test, and risks. Fill the Q5.2 table.`

**P-2 Tests**
`For slice [S#], write tests and a manual test script. Cover normal use, wrong input, slow internet and logged-out users. List what could break old features.`

**P-3 Quality check**
`Run the Q9.1 checklist on [feature/release]. Mark each line Pass / Fail / Not checked and explain every Fail in one sentence. Do not mark anything Pass without evidence.`

**P-4 Feedback sorting**
`Here is new feedback: [paste]. For each item give: type and area tags (Q4.5), a one-line summary, the customer's exact words (short), and a priority score using Q4.6 with a reason for each score. Group similar items. Do not include private details.`

**P-5 Iteration plan**
`From the scored backlog (Q10.3) and the Part 2 targets, propose the best 3–5 items for the next [length from Q10.1] iteration. Explain trade-offs. I will decide.`

**P-6 Release notes**
`Write release notes in the Q9.4 format for these changes: [paste]. Use simple words. Thank customers who reported the issues (first names only if I have permission).`

**P-7 Customer reply draft**
`Draft a reply to this customer message: [paste]. Be kind and honest, no promises I cannot keep, and match my reply promise in Q4.8. Do not send it.`

**P-8 Weekly numbers report**
`Here are this week's numbers: [paste]. Compare them to Q2.5 targets and Q2.6 milestones. Tell me what is on track, what is off, and 3 things to check. Mark anything you are unsure about.`

**P-9 Launch pack**
`Using Q1.3, Q1.4 and Q1.7, draft: a launch email, 3 social posts, an FAQ with 10 questions, and a help page for the aha moment (Q2.4).`

**P-10 Phase gate check**
`Check the EXIT CHECK of Phase [P#]. List each item as Met / Not met / Unknown with evidence. Do not tick the HUMAN GATE.`

**P-11 Pricing check**
`Read Part 4A. Check my break-even math, find missing costs (payment fees, AI usage, taxes, support time), and list payment edge cases I should test (refund, failed payment, cancel, trial end). Do not touch live payment settings.`

**P-12 Privacy check**
`Read Part 4B. Scan the product description and code I share for every place personal data is collected, stored or sent to another tool. Compare with my Q4B.2 and Q4B.6 tables and list anything missing. This is a checklist aid, not legal advice.`

**P-13 AI safety test**
`Read Part 9C. Create a 20-question test set for my AI feature (Q9.8), including tricky, off-limits and "should say I don't know" cases. Run it and mark each Pass / Fail with evidence. Also run the Q9.11 trick tests and report what happened.`

**P-14 Growth experiment**
`Read Part 11A and my last 4 weeks in Q11.7. Suggest 3 experiments for the weakest funnel step. For each: idea, expected result, length, success number, and what could go wrong. I will pick one.`

**P-15 Final review**
`Check this whole document for blanks, UNKNOWNs without owners, numbers that contradict each other, and goals that cannot be measured. Give me a fix list.`

---

# PART 14 — IS THIS DOCUMENT READY? (final self-check)

Before you start Phase 1, every box here must be ticked.

- [ ] Every ⭐ MUST question in Parts 1–4 has an answer (or `UNKNOWN (who, when)`)
- [ ] The goal in Q2.3 has a number and a date
- [ ] "Customer" is defined once (Q2.1) and the milestones are set (Q2.6)
- [ ] The aha moment is clear (Q2.4) and we can measure it
- [ ] Each AI agent has a role and limits (Q3.1) and the safety rules are accepted (Q3.2)
- [ ] There is one place for feedback and a way to rank it (Q4.4, Q4.6)
- [ ] There is a rollback plan (Q9.5)
- [ ] If we charge money: Part 4A is filled and the payment flow has a human approval
- [ ] If we collect personal data: Part 4B is filled and the privacy policy and terms are live before Phase 3
- [ ] If the product has AI: Part 9C is filled and the Q9.8 test set exists
- [ ] If there is a team: Q3.6–Q3.9 name one final decider per gate
- [ ] Top-of-file settings (`team_size`, `fill_path`, `has_ai_features`, `has_payments`, `has_mobile_app`) are set
- [ ] A friend who does not know the product can read Parts 1–2 and explain it back to you in one sentence
- 🛑 **HUMAN GATE:** I approve this plan and start Phase 1.  [ ] Approved on: ______

---

# APPENDIX A — SIMPLE WORD LIST

| Word | Simple meaning |
|---|---|
| Iteration | One turn of the loop: listen → fix → release → measure |
| MVP | The smallest version that still does the main job |
| Beta | Early version shared with a small group to learn from them |
| Launch | Opening the product to everyone |
| Activation | A new person does the first important thing and sees the value |
| Aha moment | The moment a customer thinks "oh, this is useful!" |
| Retention | Customers still using it after some time |
| Churn | Customers who stop using it |
| Backlog | The to-do list of ideas and fixes |
| Rollback | Going back to the last good version |
| Regression | An old feature breaks because of a new change |
| Human gate | A checkpoint where a real person must say yes |
| AI agent | An AI helper that does tasks for you |
| Blocker | A problem so bad that nothing can move forward |
| Slice | A small piece of work that gives one visible result |

# APPENDIX B — ONE FILLED-IN EXAMPLE (fake product, for learning only)

| Question | Example answer |
|---|---|
| Q1.3 | `Tidy helps small shops send bills in 1 minute so they get paid faster.` |
| Q2.1 | `Activated customer = sent at least 1 invoice.` |
| Q2.3 | `Reach 500 activated customers by 31 Jul, with 40% still active after 30 days.` |
| Q2.4 | `Sends their first invoice.` |
| Q4.2 | `What nearly stopped you? What is the one thing you would change? How would you feel if you could no longer use it?` |
| Q4.7 | `Cannot log in, wrong amount on an invoice, data loss.` |
| Q7.6 | `50 beta customers, 45% activation, 0 blocker bugs, top 3 problems fixed.` |
| Q9.5 | `Deploy tool → choose previous version → click "restore" → check login page (10 minutes).` |

---

*End of template. Copy this file for every new project. Keep improving it using your answers to Q11.14.*
