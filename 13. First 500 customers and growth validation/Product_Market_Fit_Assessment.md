# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **What is this file?** A guided questionnaire. You answer the questions, and at the end the document tells you whether your product has **Product-Market Fit (PMF)** and what to do next. PMF means *the right people need your product so much that they would be upset to lose it.*
>
> **Who is it for?** Anyone: founders, product managers, engineers, interns, or AI agents. If you can read and write, you can fill it in.
>
> **How long does it take?** About 2–3 hours the first time. You will come back to it at each stage (see Part 3), so the full journey from first build to your first 500 customers takes months.

## The 8 simple rules

1. **Go in order.** Start at Part 1 and move down. Each part tells you what to write.
2. **Write only in the answer spots.** Answer spots look like this: `✏️ ANSWER:`. Never delete the questions.
3. **Tick boxes like this:** change `[ ]` to `[x]`.
4. **Use real facts, not hopes.** A fact has a number, a name, or a date. A hope sounds like "I think users like it."
5. **If you do not know, write `UNKNOWN`.** Do not guess. `UNKNOWN` is a good answer, because it shows what you still need to find out.
6. **If a question does not apply to your product, write `N/A` and say why in one line.**
7. **Show your proof.** Every important number needs a place where someone can check it (a link, a file name, a dashboard). Put it in Part 18 (Evidence Log).
8. **Never put secrets here.** No passwords, API keys, customer emails, phone numbers, or private data. Use first names or IDs like `Customer-014`.

## How to rate your proof (use this everywhere)

| Level | Name | Meaning | Example |
|---|---|---|---|
| **E3** | Strong proof | Real behaviour measured from real users or real payments | "212 of 400 users came back in week 4 (dashboard link)" |
| **E2** | Medium proof | What real users told you directly | "9 of 12 interviewed customers said they use it weekly" |
| **E1** | Weak proof | Your own opinion, friends and family, or a guess | "My team thinks it's great" |
| **E0** | No proof | Nothing yet | `UNKNOWN` |

> **Golden rule:** Only E3 and E2 proof can earn high scores in Part 17. E1 and E0 earn low scores.

## Colour codes for status (use these words exactly)

| Code | Meaning |
|---|---|
| 🟢 GREEN | Done and proven |
| 🟡 YELLOW | In progress or partly proven |
| 🔴 RED | Not done, failing, or blocked |
| ⚪ GREY | Not started yet / does not apply |

## What "your product" and "customer" mean in this file

- **Product** = the thing you are building (app, website, tool, AI agent, service).
- **Customer** = a person or company who uses it. Count a customer when they have **done the main action** at least once (see question 2.6). Signing up alone does not count.
- **AI-driven** = AI helps you build it (AI coding assistants, AI testers, AI writers), and/or AI is inside it (an AI feature that talks, decides, or creates).

## Which parts must I fill at which time?

| When you are here | Fill these parts |
|---|---|
| Just starting (idea or early build) | Parts 1–6 |
| Almost ready to launch | Parts 1–8, then Part 17 |
| First 10 customers | Parts 1–9, 12 |
| Around 50–100 customers | Everything except 20; re-score Part 17 |
| Around 500 customers | Everything; final decision in Part 17 |

> 💡 **Copy this file for each new project.** Save it as `Product_Market_Fit_Assessment_<ProductName>_v1.md`. Never edit the blank master.

---

# GLOSSARY (plain-English words)

| Word | Simple meaning |
|---|---|
| **PMF (Product-Market Fit)** | The right customers want your product so much they would be upset to lose it. |
| **ICP (Ideal Customer Profile)** | A description of the person or company who gets the most value from your product. |
| **Problem** | Something painful or annoying your customer wants fixed. |
| **JTBD (Job To Be Done)** | The "job" a customer "hires" your product to do. Example: "Help me reply to emails faster." |
| **Activation** | The moment a new user first gets real value (the "aha!" moment). |
| **Retention** | How many customers keep coming back over time. |
| **Cohort** | A group of users who joined in the same week or month. |
| **Churn** | The share of customers who stop using or paying. Churn is the opposite of retention. |
| **D1 / D7 / D30 retention** | The % of a cohort still active 1, 7, or 30 days after starting. |
| **GRR / NRR** | Gross Revenue Retention (money kept, ignoring upsells) / Net Revenue Retention (money kept including upsells). |
| **CAC** | Customer Acquisition Cost: money spent to win one customer. |
| **LTV** | Lifetime Value: total profit one customer brings before they leave. |
| **Payback period** | Months needed to earn back the CAC. |
| **Gross margin** | (Revenue − direct costs) ÷ Revenue. For AI products, direct costs include AI usage costs. |
| **Inference cost** | What you pay each time the AI model produces an answer. |
| **Token** | A small chunk of text the AI reads or writes. AI vendors usually charge per token. |
| **Hallucination** | When AI confidently says something false. |
| **Eval (evaluation)** | A repeatable test that scores how good the AI's answers are. |
| **Human-in-the-loop** | A person checks or approves what the AI did before it matters. |
| **Sean Ellis test** | A one-question survey: "How would you feel if you could no longer use this product?" 40% or more answering "Very disappointed" suggests PMF. |
| **High-Expectation Customer (HXC)** | The "very disappointed" group. They define who you should build for. |
| **Beta** | A limited test release with real users before the public launch. |
| **Gate** | A checkpoint you must pass before moving to the next stage. |
| **MVP** | Minimum Viable Product: the smallest version that solves the core problem. |
| **North Star Metric** | The one number that best shows customers getting value. |

---

# PART 1: DOCUMENT CONTROL

> **What to do:** Fill this once at the start. Update it every time you change the document.

| Field | ✏️ Your answer |
|---|---|
| Product name | |
| One-line description (max 20 words) | |
| Document owner (name + role) | |
| Reviewers (names + roles) | |
| Document version (start with 0.1) | 0.1 |
| Date created (YYYY-MM-DD) | |
| Last updated (YYYY-MM-DD) | |
| Current stage (pick from Part 3: S0–S6) | |
| Current customer count (people who did the main action) | |
| Document status | `[ ] Draft` `[ ] In review` `[ ] Approved` `[ ] Archived` |
| Where is the proof stored? (folder/link) | |

### Change log (add a row every time you update)

| Version | Date | Who changed it | What changed | Why |
|---|---|---|---|---|
| 0.1 | | | First draft | |
| | | | | |

---

# PART 2: PRODUCT BASICS AND HOW AI IS USED

> **What to do:** Describe your product in simple words. Imagine explaining it to a 10-year-old.

### 2.1 What does your product do?
`✏️ ANSWER (2–3 sentences):`

### 2.2 Who is it for? (a sentence, not a list)
Use this sentence: *"For ____ (who) who struggle with ____ (problem), our product ____ (what it does) so they can ____ (result)."*
`✏️ ANSWER:`

### 2.3 What type of product is it? (tick all that apply)
- [ ] Software for businesses (B2B SaaS)
- [ ] App for people (B2C / consumer)
- [ ] Marketplace (connects buyers and sellers)
- [ ] AI agent / assistant / chatbot
- [ ] Developer tool or API
- [ ] Hardware + software
- [ ] Other: `________`

### 2.4 How do customers pay? (tick one)
- [ ] Free (no money yet)
- [ ] Free + paid upgrade
- [ ] Monthly/yearly subscription
- [ ] Pay per use
- [ ] One-time purchase
- [ ] Commission / % of sales
- [ ] Other: `________`

### 2.5 Where does AI appear in your product? (tick all that apply)
- [ ] **AI helps BUILD it** (AI coding assistant, AI test writer, AI designer, AI agents running tasks)
- [ ] **AI is INSIDE it** (answers questions, writes, recommends, decides, automates)
- [ ] **No AI inside**, only used while building
- [ ] **No AI at all** (then write `N/A` in Parts 6.3, 14, 15.3 and the AI lines in Part 13)

`✏️ Name the AI models/tools used and what each does:`

| AI tool / model | Used for | Built-in or build-time? | Who approves its output? |
|---|---|---|---|
| | | | |

### 2.6 What is the "main action"? (this defines a real customer)
The main action is the one thing a user does when they get real value. Examples: "sent their first invoice", "finished a workout", "got an AI answer they saved".
`✏️ ANSWER:`

> **A customer = someone who completed this action at least once.** Use this definition for every count in this file.

### 2.7 Your North Star Metric (the one number that shows customers get value)
Example: "Number of weekly users who complete the main action 3+ times."
`✏️ ANSWER:`

### 2.8 Who are your top 3 competitors or alternatives? (include "doing it by hand" or "spreadsheets")

| Alternative | Why do people use it? | Why might they switch to you? |
|---|---|---|
| 1. | | |
| 2. | | |
| 3. | | |

---

# PART 3: THE JOURNEY: STAGES AND GATES (CONTROL PANEL)

> **What to do:** This is your map from idea to 500 customers. Each stage has a **gate** (a checkpoint). Do **not** move to the next stage until the gate is passed, or you write down why you moved anyway in the "Override" column.
>
> Update the Status column often. Use 🟢 🟡 🔴 ⚪.

| Stage | Name | Customers | Gate: you may move on when… | Status | Date passed | Override reason (if gate not met) |
|---|---|---|---|---|---|---|
| **S0** | Problem check | 0 | You spoke to **10+ target people** and **at least 6** confirm the problem is painful (Part 4, 12) | | | |
| **S1** | Build the MVP (AI-driven development) | 0 | MVP does the main action end to end; automated tests pass; AI-agent work log filled (Part 6) | | | |
| **S2** | Private beta | 1–10 | **5+ beta users** completed the main action; top 5 bugs fixed; first quick survey done | | | |
| **S3** | Public launch | 1–10+ | Launch checklist 100% (Part 8); support and rollback ready | | | |
| **S4** | First 10 customers | 10 | **10 real customers** (not friends); you talked to each one; activation measured | | | |
| **S5** | 10 → 100 customers | 100 | **First PMF survey with 40+ valid answers**; retention curve exists; unit economics calculated | | | |
| **S6** | 100 → 500 customers | 500 | Part 17 score **75+**, all gates green, repeatable growth channel found | | | |

### 3.1 Where are you today?
- Current stage: `✏️ ____`
- Why you think you are in this stage (one sentence): `✏️ ____`
- The ONE thing blocking you from the next gate: `✏️ ____`

---

# PART 4: PROBLEM AND CUSTOMER

> **What to do:** Prove that a real group of people has a real problem worth solving. Facts beat opinions here.

### 4.1 The problem in one sentence
`✏️ ANSWER:`

### 4.2 How painful is the problem? (tick one and explain)
- [ ] Mild annoyance (nice to fix)
- [ ] Real frustration (they would try a fix)
- [ ] Painful (costs them time or money every week)
- [ ] Urgent (they are already paying or hacking a workaround)

Proof (level E0–E3 and where it is stored): `✏️ ____`

### 4.3 How do people solve the problem today?
`✏️ ANSWER (name the workaround, the cost, and what annoys them about it):`

### 4.4 Ideal Customer Profile (ICP)

| Question | ✏️ Your answer |
|---|---|
| Who exactly? (job title or life situation) | |
| Company size (B2B) or age group (B2C) | |
| Country / region | |
| How often do they feel the problem? (daily / weekly / monthly) | |
| What do they already pay for to fix it? | |
| Where do they hang out online/offline? (communities, events, sites) | |
| Who decides to buy? Who uses it? (can be different) | |

### 4.5 Who is NOT your customer? (be brave; narrowing helps)
`✏️ ANSWER:`

### 4.6 Customer job (JTBD) sentence
Use this sentence: *"When ____ (situation), I want to ____ (action), so I can ____ (result)."*
`✏️ ANSWER:`

### 4.7 Market size reality check (rough numbers are fine, show how you got them)

| Question | ✏️ Answer | Source (link) |
|---|---|---|
| How many people/companies match your ICP? | | |
| How many could you realistically reach in 12 months? | | |
| Is 500 customers a small slice of this group? (`[ ] Yes  [ ] No  [ ] UNKNOWN`) | | |

---

# PART 5: VALUE PROMISE AND ALTERNATIVES

> **What to do:** Say clearly why someone should choose you.

### 5.1 Your main benefit (what customers say they get, not what you think)
`✏️ ANSWER (use customer words; fill again after Part 10 survey):`

### 5.2 Your "10x" claim: what is much better than the old way?

| Measure | Old way | With your product | How you measured |
|---|---|---|---|
| Time taken | | | |
| Money cost | | | |
| Quality or errors | | | |

### 5.3 Why can't a competitor copy this next month? (tick all that apply)
- [ ] Special data we own
- [ ] Deep fit into customer workflow (hard to rip out)
- [ ] Community or network effect
- [ ] Brand or trust
- [ ] Speed of learning from customer feedback
- [ ] Other: `________`
- [ ] **Honest answer: they could copy us easily** (then say what you will do about it): `________`

### 5.4 Price you charge today (or plan to) and why
`✏️ ANSWER:`

---

# PART 6: BUILD PHASE: AI-DRIVEN DEVELOPMENT (S1)

> **What to do:** Show how the product was built using AI and humans together, and that it is safe to ship. This part makes your work repeatable and checkable.

### 6.1 Scope of the MVP

| Question | ✏️ Answer |
|---|---|
| The ONE core use case the MVP must do | |
| 3 features included in MVP | |
| 3 features deliberately left OUT | |
| Planned build time and actual build time | |

### 6.2 Build quality checklist (tick when true)

**Planning**
- [ ] Requirements written in plain language (user stories) and stored: `link`
- [ ] "Done" defined for each feature (acceptance rules)
- [ ] Architecture or system sketch exists: `link`

**Building**
- [ ] Code is in version control with history
- [ ] Every AI-written change was **reviewed by a human** before merge
- [ ] Secrets (keys, passwords) are stored safely, never in the code
- [ ] Environments exist: development, testing, live

**Testing (QA)**
- [ ] Automated tests run on every change (pass rate: `___%`)
- [ ] Main user journey tested end to end by a person
- [ ] Tested on the devices/browsers your ICP uses
- [ ] Speed/load checked for expected first-100-customer traffic
- [ ] Basic security check done (logins, permissions, input checks)
- [ ] Accessibility basics checked (readable text, keyboard use)

**Release safety**
- [ ] You can undo (roll back) a bad release in under 30 minutes
- [ ] Error alerts reach a real person
- [ ] Usage analytics tracks the main action, sign-ups, and return visits

### 6.3 AI-agent work log (who/what did what)

> **What to do:** Every time an AI agent does meaningful work (writes code, tests, writes docs, answers customers), add a row. This lets anyone repeat or audit the work. Keep prompts and settings short; store long versions in a file and link it.

| Date | Stage | Task | AI agent/tool + version | Prompt or instruction file (link) | Human who approved | Result (`PASS` / `FIX` / `FAIL`) | Notes (what went wrong/right) |
|---|---|---|---|---|---|---|---|
| | | | | | | | |
| | | | | | | | |
| | | | | | | | |

### 6.4 AI development rules (tick the rules you follow)
- [ ] AI never ships to customers without human approval
- [ ] AI cannot access customer private data while building
- [ ] Every AI-written feature has at least one test
- [ ] AI model/prompt versions are recorded (so results can be repeated)
- [ ] There is a written "stop rule": if AI quality drops below `____`, we pause releases

### 6.5 Build gate (S1)
Pass only if all are true: MVP does main action `[ ]`  tests pass `[ ]`  rollback ready `[ ]`  analytics ready `[ ]`  work log filled `[ ]`
Gate result: `✏️ 🟢 / 🟡 / 🔴`

---

# PART 7: PRIVATE BETA (S2)

> **What to do:** Test with a small, friendly-but-honest group before the public sees it.

| Question | ✏️ Answer |
|---|---|
| How many beta users invited / joined / completed the main action? | ___ / ___ / ___ |
| How did you pick them? (they must match your ICP) | |
| How long was the beta? (dates) | |
| Top 5 problems found | 1. 2. 3. 4. 5. |
| How many of the top 5 are fixed? | |
| Biggest surprise from beta users | |
| Quote from a beta user (exact words, first name only) | |
| Did any beta user pay or pre-order? (`Yes/No`, how many) | |

### 7.1 Beta survey (send to everyone who tried the main action at least twice)
Ask the 4 questions from Part 10.2 now. Record results in Part 10 (label cohort `Beta`).

### 7.2 Beta gate (S2)
Pass only if: 5+ users completed main action `[ ]`  top bugs fixed `[ ]`  at least 1 user said they would be upset to lose it `[ ]`
Gate result: `✏️ 🟢 / 🟡 / 🔴`

---

# PART 8: PUBLIC LAUNCH (S3)

> **What to do:** Make sure launch day is calm, not chaos.

### 8.1 Launch readiness checklist
- [ ] Clear homepage: a stranger understands the product in **10 seconds**
- [ ] Sign-up to main action takes under **`___` minutes** (your target)
- [ ] Pricing page or clear "how to pay" path
- [ ] Terms, privacy policy, and cookie notice published
- [ ] Support channel works (email/chat) and has an owner and reply-time promise
- [ ] Help guide or FAQ covers the top 10 questions
- [ ] Billing tested with a real small payment (if you charge)
- [ ] Analytics confirmed (sign-up, main action, return visits)
- [ ] Monitoring and alerts live; on-call person named: `____`
- [ ] Rollback plan tested
- [ ] AI safety limits on (Part 14, 15 checklists done)
- [ ] Launch message prepared for each channel (Part 16)

### 8.2 Launch plan

| Question | ✏️ Answer |
|---|---|
| Launch date | |
| Launch channels (where will you announce?) | |
| Goal for launch week (number of customers who do the main action) | |
| Who answers support in week 1? | |
| What will you do if something breaks? | |

### 8.3 Launch results (fill after launch week)

| Measure | Goal | Actual | Proof |
|---|---|---|---|
| Visitors | | | |
| Sign-ups | | | |
| Reached the main action (new customers) | | | |
| Paid customers | | | |
| Top complaint | | | |

### 8.4 Launch gate (S3)
Pass only if checklist 8.1 is fully ticked. Gate result: `✏️ 🟢 / 🟡 / 🔴`

---

# PART 9: STAGE CHECKPOINTS: CUSTOMERS 1–500 (S4, S5, S6)

> **What to do:** Fill each block when you reach that customer count. Keep older blocks; never overwrite them.

## 9.1 Checkpoint S4: first 10 customers

| Question | ✏️ Answer |
|---|---|
| Date you reached 10 customers | |
| How many are strangers (not friends, family, or colleagues)? | |
| How did each of the 10 find you? | |
| What % reached "aha" (first real value) in their first session? | |
| Average time from sign-up to main action | |
| Did you speak to every customer? (`Yes/No`, how many) | |
| Top 3 reasons people left or got stuck | 1. 2. 3. |
| What did you change because of what they said? | |

**Gate S4:** 10 real customers `[ ]`  you spoke to most of them `[ ]`  top blockers have owners `[ ]`  → `🟢/🟡/🔴`

## 9.2 Checkpoint S5: 10 → 100 customers

| Question | ✏️ Answer |
|---|---|
| Date you reached 100 customers | |
| New customers per week (last 4 weeks) | |
| Best channel (most customers) | |
| Worst channel (most money, few customers) | |
| First PMF survey run? (`Yes/No`) Score: ___% (Part 10) | |
| Retention curve built? (`Yes/No`) Shape: flattening / still falling / to zero (Part 11) | |
| Unit economics calculated? (`Yes/No`) (Part 13) | |
| Biggest product change since customer #10 | |

**Gate S5:** survey has 40+ valid answers `[ ]`  retention curve built `[ ]`  CAC and margin known `[ ]`  → `🟢/🟡/🔴`

## 9.3 Checkpoint S6: 100 → 500 customers

| Question | ✏️ Answer |
|---|---|
| Date you reached 500 customers | |
| How many came from word of mouth, referrals, or organic search? (%) | |
| Is growth repeatable? (could you do it again next month with the same steps? `Yes/No`) | |
| Support load per customer (tickets per 100 customers per month) | |
| Biggest risk to getting to 1,000+ | |
| Latest PMF survey score | ___% |
| Final Part 17 score | ___/100 |

**Gate S6:** Part 17 score 75+ `[ ]`  all must-pass gates green `[ ]`  repeatable growth channel `[ ]`  → `🟢/🟡/🔴`

---

# PART 10: THE PMF SURVEY (SEAN ELLIS TEST + SUPERHUMAN 4 QUESTIONS)

> **What this is:** The best-known quick PMF test. The idea comes from Sean Ellis; Superhuman's founder Rahul Vohra turned it into a repeatable method. Many teams use **40% "Very disappointed"** as the sign of fit. Treat 40% as a **rule of thumb, not a law**. It was drawn from looking at many startups, and it is only one signal. That is why this file also checks retention, conversations, and money.

### 10.1 Who should you send it to? (important)
Send to users who:
- [ ] Used your product's main action **at least 2 times**
- [ ] Used it **recently** (e.g., within the last 2 weeks)
- [ ] Are real users (not your team, friends, or people who only signed up)

Do **not** include: people who only signed up, churned users (their answers distort the score), your own team.

| Question | ✏️ Answer |
|---|---|
| Survey tool used (Google Forms, Typeform, etc.) | |
| Date sent / date closed | |
| How many people received it? | |
| How many answered? | |
| How many are valid (match the rules above)? | |

> **Rule:** Results are only **directional** with ~40 valid answers. Fewer than 40 = treat the score as a hint, not proof. More answers = more trust.

### 10.2 The 4 questions (copy these into your survey tool)

1. **How would you feel if you could no longer use [Product]?**
   `( ) Very disappointed   ( ) Somewhat disappointed   ( ) Not disappointed   ( ) N/A, I no longer use it`
2. **What type of people do you think would most benefit from [Product]?** *(free text)*
3. **What is the main benefit you receive from [Product]?** *(free text)*
4. **How can we improve [Product] for you?** *(free text)*

### 10.3 Count the answers to Question 1

| Answer | Number of people | % of valid answers |
|---|---|---|
| Very disappointed | | |
| Somewhat disappointed | | |
| Not disappointed | | |
| N/A (no longer use it), *remove from the count* | | (not counted) |
| **Total valid answers** | | 100% |

**How to calculate:** `PMF score % = (Very disappointed ÷ Total valid answers) × 100`
(Choose one counting rule and keep it the same every time you re-run the survey. Write the rule here: `✏️ ____`)

`✏️ YOUR PMF SURVEY SCORE: ____ %`

### 10.4 What does your score mean?

| Score | Meaning | What to do |
|---|---|---|
| **Below 25%** | No fit yet | Stop scaling. Go back to the problem and customer (Parts 4, 12). |
| **25%–39%** | Getting closer | Follow the improvement loop in 10.6. Do not spend big on growth yet. |
| **40%–49%** | Probable fit | Double down on what fans love; start controlled growth. |
| **50%+** | Strong fit | Scale growth channels carefully; watch retention and margin. |

### 10.5 Find your real fans (segmentation)
Look only at the **"Very disappointed"** group. Read their answers to questions 2 and 3.

| Question | ✏️ Answer |
|---|---|
| Who are these fans? (job, company type, situation) | |
| The most common **main benefit** they named (use their words) | |
| What do they have in common? | |
| Which people answered "Not disappointed"? (ignore their feedback; they are not your fans) | |

**Re-score using only people who match your fan profile (High-Expectation Customer):**
`✏️ Score among fan-profile users only: ____ %` *(this usually goes up and shows who you should target)*

### 10.6 The improvement loop (do this every quarter until you pass 40%)
1. Take the **"Somewhat disappointed"** people who named the **same main benefit as your fans**. Read their answer to question 4.
2. Make a roadmap that is about **half "build more of what fans love"** and **half "fix what holds the almost-fans back."**
3. Ship, wait, and run the survey again with fresh users.
4. Track the score over time:

| Survey round | Date | Valid answers | Score | What we changed since last time |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

### 10.7 Warnings about this survey (be honest with yourself)
- It asks people to **imagine** the future, so it can mislead. Always check it against retention (Part 11) and real behaviour.
- Some great products have users who say "I'd be relieved to stop," yet they never leave. Behaviour beats opinion.
- A high score from friendly or tiny samples is E1 proof. Only count it as E2/E3 if the sample is real.
- Free users and paying users can answer very differently. Run it for both and write down the difference.

---

# PART 11: RETENTION AND COHORTS (DO PEOPLE KEEP COMING BACK?)

> **Why it matters:** A product with fit has a retention curve that **flattens** (some people stay for good). If the curve keeps falling to zero, people try it and leave. That is a fit problem, not just an onboarding problem.

### 11.1 Choose how you measure "active"
`✏️ Active means: ____` *(Example: "completed the main action at least once in the week")*
Measuring window: `[ ] Daily  [ ] Weekly  [ ] Monthly`. Pick based on how often a happy customer should use the product.

### 11.2 Cohort table
Group customers by the week or month they joined. Fill what % are **still active** at each point. Leave blank if the time has not arrived yet.

| Cohort (joined) | Size | Week 1 / Day 1 | Week 2 / Day 7 | Week 4 / Day 30 | Week 8 | Week 12 / Day 90 |
|---|---|---|---|---|---|---|
| | | % | % | % | % | % |
| | | % | % | % | % | % |
| | | % | % | % | % | % |
| | | % | % | % | % | % |

### 11.3 Read the curve (tick one)
- [ ] **Flattening above zero**: later cohorts level off at some %. 🟢
- [ ] **Still falling**: no flat part yet, but slowing. 🟡
- [ ] **Falling to zero**: almost everyone leaves. 🔴
- [ ] **Not enough data yet** (need at least 3 cohorts and 8 weeks): `UNKNOWN` ⚪

### 11.4 Compare with typical ranges

> ⚠️ These ranges are rough guides from public sources and differ a lot by product type. Replace them with benchmarks for **your** category and write the source.

| Product type | Rough "healthy" signal | Your number |
|---|---|---|
| Consumer app | Day 30 retention roughly 20–40% for strong fit; some sources use lower floors for mobile apps. Check your category. | |
| B2B SaaS | Annual gross revenue retention above ~90%, net revenue retention above ~100% | |
| Marketplace / other | Repeat purchase or repeat use within a normal buying cycle | |

`✏️ Our benchmark source and date: ____`

### 11.5 Revenue retention (only if you charge)

| Measure | Formula | Your number |
|---|---|---|
| Monthly churn % | customers lost ÷ customers at start of month | |
| Gross Revenue Retention | money kept from a cohort ÷ money at start (ignore upsells) | |
| Net Revenue Retention | money from a cohort now ÷ money at start (include upsells) | |

### 11.6 Early habits that predict staying
`✏️ ANSWER: What do customers who stay for 90 days do in their first 7 days that others don't? (example: "invited a teammate", "saved 3 items")`

### 11.7 Why do people leave? (ask 5+ churned users; add proof)

| Reason | How many people said it | Fixable? (Y/N) | Owner |
|---|---|---|---|
| | | | |

---

# PART 12: CUSTOMER CONVERSATIONS (INTERVIEWS AND JOBS TO BE DONE)

> **What to do:** Talk to real people. Numbers tell you **what** happened; conversations tell you **why**.

### 12.1 Interview plan
- Goal: at least **5 interviews per stage** (S0, S2, S4, S5) and **5 churned-user interviews**.
- Each interview: 20–30 minutes. Ask permission to take notes.

| Question | ✏️ Answer |
|---|---|
| Interviews done so far (total) | |
| How many were with ICP matches? | |
| How many were with people who stopped using the product? | |

### 12.2 Question bank (ask open questions; do not pitch)
**Their situation**
1. Tell me about the last time you had to ____ (the job).
2. What did you do? What tools or people helped?
3. What was hardest or most annoying?

**Their solution today**
4. What have you tried before? Why did you stop?
5. How much time or money does this cost you each month?

**Their experience with your product**
6. What made you try it? What nearly stopped you?
7. When did you first think "this is useful"? (find the aha moment)
8. What would you use instead if it disappeared tomorrow?
9. Who else would you tell about it? What would you say?

**Closing**
10. What is the one thing we should fix first?

### 12.3 Interview log

| ID | Date | Who (role, no private data) | Matches ICP? | Main job they need done | Strongest quote (exact words) | Would be upset to lose it? (Y/N/Maybe) | Next step |
|---|---|---|---|---|---|---|---|
| C-001 | | | | | | | |
| C-002 | | | | | | | |
| C-003 | | | | | | | |
| C-004 | | | | | | | |
| C-005 | | | | | | | |

### 12.4 Patterns after 5+ interviews

| Pattern | How many interviews it showed up in | What we will do |
|---|---|---|
| | | |

### 12.5 Net Promoter Score (optional extra signal)
Question: "How likely are you to recommend us to a friend or colleague? (0–10)"
`NPS = % scoring 9–10 minus % scoring 0–6`
`✏️ NPS: ____` (responses: ____) *Treat NPS as supporting evidence only; the Part 10 survey is the main test.*

---

# PART 13: MONEY MATH (UNIT ECONOMICS, INCLUDING AI COSTS)

> **What to do:** Prove that each customer brings in more money than they cost. Use real numbers. If you do not know a number, write `UNKNOWN` and decide how to find it. Use one month as your time period unless stated.

### 13.1 Revenue per customer

| Item | ✏️ Number | Proof |
|---|---|---|
| Average revenue per customer per month (ARPA) | | |
| Free-to-paid conversion % (if you have a free plan) | | |
| Average months a customer stays (= 1 ÷ monthly churn) | | |

### 13.2 What it costs to serve one customer (per month)

| Cost | ✏️ Number |
|---|---|
| Hosting / servers | |
| **AI usage cost** (model fees: inference/tokens, image, voice, search tools) | |
| Payment fees | |
| Customer support cost | |
| Other direct costs | |
| **Total cost to serve** | |

> **AI cost tip:** AI products tend to have **lower margins than classic software**. Public 2026 industry reports suggest healthy AI-product gross margins of roughly **50–70%** (versus 75–90% for traditional software), with model usage often a big share of revenue. Do not assume 80%. Measure yours. Heavy users can cost far more than average users, so check the top 10% of users separately.

| AI cost check | ✏️ Answer |
|---|---|
| AI cost per active customer per month | |
| AI cost per main-action completed | |
| AI cost for your top 10% heaviest users | |
| Any usage limit or fair-use rule? | |
| What would a 2× price drop or 2× price rise from your AI vendor do to your margin? | |

### 13.3 Gross margin
`Gross margin % = (Monthly revenue per customer − Total cost to serve) ÷ Monthly revenue per customer × 100`
`✏️ Gross margin: ____ %`   Is it above 0 with room to grow? `[ ] Yes  [ ] No  [ ] UNKNOWN`

### 13.4 Cost to win a customer (CAC)

| Item | ✏️ Number |
|---|---|
| Total sales + marketing spend this period (ads, tools, salaries for growth work, freelancers) | |
| New paying customers this period | |
| **CAC = spend ÷ new customers** | |
| CAC for each channel (copy rows from Part 16) | |

### 13.5 Lifetime value and payback

| Measure | Formula | ✏️ Your number |
|---|---|---|
| Customer lifetime (months) | 1 ÷ monthly churn | |
| LTV (simple) | monthly gross profit per customer × lifetime months | |
| **LTV ÷ CAC** | Healthy products often aim for **3 or more**, but this varies | |
| **CAC payback (months)** | CAC ÷ monthly gross profit per customer | |

### 13.6 Money verdict (tick one)
- [ ] 🟢 Each customer earns more than they cost, and LTV ÷ CAC is healthy or improving
- [ ] 🟡 Close, but one number (margin, CAC, or churn) needs work. Name it: `____`
- [ ] 🔴 We lose money on each customer and have no clear fix
- [ ] ⚪ Not enough data yet (free product, or fewer than 30 paying customers)

---

# PART 14: AI QUALITY AND TRUST (ONLY IF AI IS INSIDE YOUR PRODUCT)

> **What to do:** Prove the AI is good enough that customers trust it. If no AI is inside the product, write `N/A, no AI inside` here and skip to Part 15.

### 14.1 What does "a good AI answer" mean for your product?
`✏️ ANSWER (3 rules a human could check; example: "factually correct, cites the source, under 150 words"):`

### 14.2 Test set (the "eval")
Build a list of real questions/tasks with known good answers. Re-run it every time you change the model or the prompt.

| Item | ✏️ Answer |
|---|---|
| Number of test cases in your eval set | (aim for 50+ before launch, 200+ later) |
| Where the eval set lives (link) | |
| Who checks the AI's answers (human or another AI, and how often a human spot-checks) | |

### 14.3 Quality scoreboard (update each release)

| Measure | How to measure | Target | Latest result | Date |
|---|---|---|---|---|
| Correct-answer rate | Passed test cases ÷ total test cases | | | |
| Hallucination rate | Answers with false claims ÷ answers checked | | | |
| Human-override rate | Answers a human had to fix or reject ÷ total | | | |
| Refusal/"I don't know" rate (not too high, not too low) | | | | |
| Speed (seconds to answer, typical and slowest) | | | | |
| Thumbs-up rate from users | | | | |
| Safety failures (harmful or off-topic answers) | Count per 1,000 answers | | | |

### 14.4 Trust signals from users
- [ ] Users can **see why** the AI said something (sources, steps, or explanation)
- [ ] Users can **correct, undo, or report** a bad answer in one click
- [ ] Users are told clearly when they are talking to AI
- [ ] Users stay in control of important actions (the AI asks before spending money, deleting, sending)

| Question | ✏️ Answer |
|---|---|
| What % of customers use the AI feature regularly? | |
| Do customers who use the AI feature stay longer than those who don't? (cite the numbers) | |
| Biggest trust complaint from customers (quote) | |

### 14.5 AI quality verdict
- [ ] 🟢 Meets targets and trusted by users
- [ ] 🟡 Meets some targets; fixes planned: `____`
- [ ] 🔴 Frequent wrong or unsafe answers
- [ ] ⚪ `N/A`: no AI inside the product

---

# PART 15: DATA, PRIVACY AND SAFETY

> **What to do:** Customers will not stay if they do not trust you with their information. Tick honestly. Any unticked item must appear in Part 18 (Risks).
> *This is a checklist, not legal advice. Ask a qualified lawyer or compliance advisor for rules that apply in your country and industry.*

### 15.1 What data do you collect?

| Data type | Do you collect it? (Y/N) | Why you need it | Where stored | How long kept |
|---|---|---|---|---|
| Name / email | | | | |
| Payment details (should be handled by your payment provider, not you) | | | | |
| Usage activity | | | | |
| User-created content | | | | |
| Sensitive data (health, children, finance, location) | | | | |

### 15.2 Privacy and security checklist
- [ ] Privacy policy is written in plain language and published
- [ ] Users agree (consent) where required
- [ ] Users can see, export, and delete their data
- [ ] Data is encrypted when stored and when sent
- [ ] Only the people who need access have access
- [ ] Customer data is **not** used to train AI models unless the customer agreed
- [ ] A plan exists for a data leak (who is told, in what time)
- [ ] We know which privacy rules apply to us (for example GDPR in the EU, CCPA/CPRA in California): `list them: ____`
- [ ] Children under 13 (or the legal age where you operate) are handled correctly or not allowed

### 15.3 AI-specific safety checklist (skip if no AI inside)
- [ ] We tested for prompt tricks (users trying to make the AI ignore its rules)
- [ ] The AI cannot reveal other customers' data
- [ ] Harmful and abusive requests are blocked or flagged
- [ ] Spending limits and rate limits stop runaway AI costs
- [ ] We know which AI regulations apply to our use case and where we sell (for example the EU AI Act): `list: ____`
- [ ] AI vendor terms reviewed (data use, data location, retention)
- [ ] Human review exists for high-risk decisions (money, health, legal, jobs)

### 15.4 Open safety or privacy issues

| Issue | Severity (`Low / Medium / High / Critical`) | Owner | Fix date |
|---|---|---|---|
| | | | |

> **Must-pass rule:** Any open **Critical** issue means the product **cannot pass** Part 17, no matter the score.

---

# PART 16: GROWTH: WHERE CUSTOMERS COME FROM

> **What to do:** Find at least one way to win customers again and again. One channel that works beats five that sort of work.

### 16.1 Channel table (add every channel you tried)

| Channel (e.g., search, social posts, communities, partners, ads, outreach, referrals) | Time period | Money spent | Time spent (hours) | Visitors | Sign-ups | Customers (main action done) | CAC | Verdict (`Keep / Test more / Stop`) |
|---|---|---|---|---|---|---|---|---|
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |

### 16.2 Pull signals (customers coming without you pushing)

| Signal | ✏️ Number or answer |
|---|---|
| % of new customers from word of mouth, referrals, or organic search | |
| Number of customers who invited others on their own | |
| Do people ask for features or beg to be added to a waiting list? | |
| Are you getting inbound requests from people who match your ICP? | |
| Growth per week, last 8 weeks (e.g., +4%, +6%) | |

### 16.3 Repeatability test
- [ ] I can describe our best channel in **5 steps** that someone else could repeat
- [ ] We got customers from this channel **at least 3 times** in a row
- [ ] CAC from this channel is stable or falling

`✏️ Our best repeatable channel and its 5 steps: ____`

---

# PART 17: SCORECARD AND DECISION (GO / FIX / STOP)

> **What to do:** Score each row from **0 to 10** using the rules. Be honest. **You must have proof (E2 or E3) for any score of 7 or higher.** Write the proof level and where it lives.

### 17.1 The 10 score rows

| # | What we score | From | Scoring guide (0 = nothing, 10 = excellent) | ✏️ Score (0–10) | Proof level (E0–E3) | Why this score (1 line) |
|---|---|---|---|---|---|---|
| 1 | Problem clarity and pain | Part 4 | 0–3 vague problem; 4–6 clear, medium pain; 7–10 clear, painful, people already pay or hack around it | | | |
| 2 | Customer match (clear ICP and fan profile) | Parts 4, 10.5 | 0–3 "everyone"; 4–6 rough ICP; 7–10 sharp fan profile with evidence | | | |
| 3 | PMF survey result | Part 10 | `<25%` → 0–2; `25–39%` → 3–6; `40–49%` → 7–8; `50%+` → 9–10. Fewer than 40 valid answers: max 6. No survey yet: score 0. | | | |
| 4 | Retention curve | Part 11 | 0–3 falls to zero; 4–6 falling but slowing; 7–10 clearly flattens above zero in 3+ cohorts | | | |
| 5 | Customer conversation evidence | Part 12 | 0–3 under 5 interviews; 4–6 patterns emerging; 7–10 10+ interviews, strong repeated pull | | | |
| 6 | Money math | Part 13 | 0–3 losing money each customer; 4–6 near break-even; 7–10 healthy margin and payback | | | |
| 7 | AI quality and trust | Part 14 | 0–3 frequent failures; 4–6 mixed; 7–10 meets targets and users trust it. (No AI inside: score using the average of the other rows) | | | |
| 8 | Data, privacy, and safety | Part 15 | 0–3 major gaps; 4–6 some gaps with plan; 7–10 checklist complete, no open High/Critical | | | |
| 9 | Growth and pull | Part 16 | 0–3 only paid or personal push; 4–6 one channel working sometimes; 7–10 repeatable channel plus organic pull | | | |
| 10 | Build and launch execution | Parts 6–9 | 0–3 gates skipped; 4–6 most gates passed; 7–10 all gates passed on time with proof | | | |
| | **TOTAL (add rows 1–10)** | | | **___ / 100** | | |

### 17.2 Must-pass gates (all four must be 🟢 to say "PASS")

| Gate | Rule | Status (`🟢 / 🟡 / 🔴 / ⚪`) | Proof |
|---|---|---|---|
| G1: Fans exist | PMF survey ≥ **40%** "very disappointed" with **40+ valid answers** (or fan-profile segment ≥ 40% and you are focusing on that segment) | | |
| G2: People stay | Retention curve **flattens above zero** | | |
| G3: Money works | Gross margin is **above 0 per customer** after AI costs, with a believable path to a healthy margin | | |
| G4: Safe to grow | **No open Critical** safety or privacy issue | | |

> If you are at stage S0–S4 and a gate cannot be measured yet (`⚪`), your best possible decision is **FIX** (keep going and measure), never PASS.

### 17.3 The decision (use this table, do not improvise)

| Total score | All 4 gates 🟢? | Decision |
|---|---|---|
| **75–100** | Yes | **✅ PASS**: You have PMF. Invest in growth. Keep re-checking every quarter. |
| **75–100** | No | **🛠 FIX**: Strong score but a gate is not green. Fix the gate first. |
| **50–74** | Any | **🛠 FIX**: Promising. Pick the **2 lowest rows** and improve them. Re-score in 4–8 weeks. |
| **Below 50** | Any | **🛑 STOP and RETHINK**: Do not scale. Go back to Parts 4 and 12. Consider changing customer, problem, or product. |

`✏️ OUR DECISION: [ ] PASS   [ ] FIX   [ ] STOP and RETHINK`
`✏️ Decision date: ____    Re-score date: ____`

### 17.4 Our two lowest rows and the plan

| Row # | Why it is low | The ONE action that would raise it most | Owner | Due date |
|---|---|---|---|---|
| | | | | |
| | | | | |

### 17.5 Score history (keep adding rows; never delete old ones)

| Date | Stage | Customers | Survey % | Total score | Decision |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |

---

# PART 18: RISKS, EVIDENCE LOG, AND NEXT ACTIONS

### 18.1 Evidence log (where proof lives)

> **What to do:** Every important number in this file needs one row here. If someone asks "how do you know?" the answer is in this table.

| ID | What it proves | Part | Proof level (E0–E3) | Where it lives (link or file) | Date collected | Collected by |
|---|---|---|---|---|---|---|
| EV-001 | | | | | | |
| EV-002 | | | | | | |
| EV-003 | | | | | | |
| EV-004 | | | | | | |

### 18.2 Risk register

> Rate **Chance** and **Impact** as `Low / Medium / High`. Write the first step you will take.

| ID | Risk (what could go wrong) | Chance | Impact | What we will do | Owner | Status |
|---|---|---|---|---|---|---|
| R-001 | Customers like it but don't come back | | | | | |
| R-002 | AI costs grow faster than revenue | | | | | |
| R-003 | AI gives a harmful or very wrong answer | | | | | |
| R-004 | Our best channel stops working | | | | | |
| R-005 | A competitor copies us | | | | | |
| R-006 | Data leak or privacy complaint | | | | | |
| R-007 | AI vendor changes price, terms, or model | | | | | |
| R-008 | (add your own) | | | | | |

### 18.3 Assumptions we are making (things we believe but haven't proven)

| Assumption | How we will test it | By when |
|---|---|---|
| | | |

### 18.4 Next actions (maximum 5; each needs one owner and one date)

| # | Action | Owner | Due | Done? |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

---

# PART 19: INSTRUCTIONS FOR AI AGENTS FILLING THIS DOCUMENT

> **For humans:** Share this part with any AI agent that will help fill or review the file.

**Role:** You help a person complete this assessment. You do not invent facts.

**Rules**
1. **Never fabricate** numbers, quotes, customer names, links, or dates. If a fact is missing, write `UNKNOWN` and add a question for the human at the end.
2. **Always attach a proof level (E0–E3)** and a source to every number you enter. If no source exists, set the level to E0 or E1.
3. **Keep every question and heading unchanged.** Only fill answer spots and tick boxes.
4. **Do the maths and show it.** Use the formulas in Parts 10, 11, 13 and 17. Re-add the Part 17 total yourself and flag any row where the score is 7+ but the proof is E0 or E1.
5. **Keep private data out.** Never write customer emails, phone numbers, keys, or passwords.
6. **Do not change a decision on your own.** You may suggest PASS / FIX / STOP with reasons. The named human owner makes and signs the final decision.
7. **Log your work** in Part 6.3 (AI-agent work log) and the Part 1 change log.
8. **Stop and ask the human** when: two sources disagree, a number looks unlikely (for example retention above 95% or survey score jumps by 20+ points), or a Critical safety issue appears.

**Before you finish, run this self-check and write the result at the bottom of Part 19:**
- [ ] No answer spot left empty (each has an answer, `UNKNOWN`, or `N/A` with reason)
- [ ] All formulas re-calculated
- [ ] Every score of 7+ has E2 or E3 proof
- [ ] Part 17 total adds up correctly and the decision matches the table in 17.3
- [ ] Evidence log (18.1) covers every important number
- [ ] No private data present
- [ ] Questions for the human listed

`✏️ AI self-check result and open questions for the human:`

---

# PART 20: SMALL FILLED EXAMPLE (SO YOU CAN SEE WHAT "GOOD" LOOKS LIKE)

> This is a **made-up** product called **"ReplyPal"**. Do not copy these numbers. Use this only to see the style: short, factual answers with proof.

**2.1 What does it do?** ReplyPal reads a customer-support email and writes a draft reply using the company's own help articles. A human clicks "send".

**2.2 Sentence:** For small online shops who struggle with answering the same support emails all day, ReplyPal drafts correct replies in seconds so owners get hours back each week.

**2.6 Main action:** Sending an AI-drafted reply to a real customer.

**4.2 Pain level:** Painful. 9 of 12 shop owners interviewed spend 5+ hours a week on repeat emails (E2, interview notes `C-001` to `C-012`).

**10.3 Survey (example):** 62 valid answers; 21 "Very disappointed" → **34%** (21 ÷ 62 × 100). Rule: "N/A, no longer use" removed from the count.

**10.5 Fan profile:** Shops with 1–5 staff and 20+ support emails a day. Among that segment: 17 of 36 → **47%**. Main benefit named by fans (their words): "saves me my evenings."

**11.3 Retention:** Week-8 retention for the last three cohorts: 41%, 44%, 43%. The curve **flattens** 🟢. (E3, dashboard export `EV-004`)

**13.2–13.5 Money math (per customer per month):** Revenue $49; AI cost $9; hosting + support + fees $7 → total cost to serve $16 → gross margin **67%**. CAC $140; monthly gross profit $33 → payback ≈ **4.2 months**; monthly churn 4% → lifetime 25 months → LTV ≈ $825 → LTV ÷ CAC ≈ **5.9**.

**14.3 AI quality:** Eval set 120 cases; correct-answer rate 91% (target 90%); hallucination rate 3% (target ≤ 3%); human-override rate 14%.

**17.1 Scorecard (example):** Row scores 8, 7, 6, 8, 7, 8, 7, 7, 5, 7 → **total 70 / 100**.
**17.2 Gates:** G1 🟡 (34% overall, 47% in fan segment, so "focus on the segment" rule applies); G2 🟢; G3 🟢; G4 🟢.
**17.3 Decision:** **🛠 FIX.** Score is 50–74. Two lowest rows: Growth (5) and Customer match (6). Action: run all outreach only at shops with 1–5 staff and re-run the survey in 6 weeks.

---

# SIGN-OFF

| Role | Name | Decision agreed? | Signature or approval note | Date |
|---|---|---|---|---|
| Document owner | | `[ ] Yes  [ ] No` | | |
| Product lead | | `[ ] Yes  [ ] No` | | |
| Engineering / AI lead | | `[ ] Yes  [ ] No` | | |
| Quality (QA) reviewer | | `[ ] Yes  [ ] No` | | |
| Privacy / safety reviewer | | `[ ] Yes  [ ] No` | | |

---

# TEMPLATE NOTES (for the template maintainer; delete in project copies if you like)

- **Template version:** 1.0 (created 2026-10-19)
- **Where it lives:** `First-500-Customers-and-Growth-Validation/Product_Market_Fit_Assessment.md`
- **Methods built in:** Sean Ellis 40% "very disappointed" test; Superhuman PMF engine (4 questions, fan segmentation, 50/50 roadmap loop); cohort retention and curve-shape reading; interviews and Jobs-To-Be-Done; CAC / LTV / payback with AI inference cost; AI quality (eval sets, hallucination, human override); privacy and safety; stage gates S0–S6; scorecard with must-pass gates.
- **Benchmarks are guides, not laws.** The 40% line, retention ranges, and AI-margin ranges come from public sources and vary by product. Update them in this master file once a year and note the date and source.
- **Review cycle:** Review this template every 6 months, and after every 20 projects that use it.
