---
document: Customer_Acquisition_Strategy
template_version: 1.0.0
folder: First 500 customers and growth validation
lifecycle: AI-Driven Development Life Cycle (idea -> build -> beta -> launch -> first 500 customers)
project_name: "<<FILL: CAS-0.1>>"
owner: "<<FILL: CAS-0.2>>"
status: draft            # draft | in-review | approved | in-use | closed
last_updated: "<<YYYY-MM-DD>>"
---

# HOW TO FILL THIS DOCUMENT (read this first, 3 minutes)

> **What is this file?** It is your plan for finding, winning and keeping your **first 500 customers**, and for proving (validating) that your growth is real. It is written as a **questionnaire**. You answer the questions. The plan builds itself from your answers.

## The 7 simple rules

1. **Go in order.** Start at Part 0 and finish at Part 13 (the final check). Do not skip ahead.
2. **Replace every `<<FILL: ...>>`** with your own words. Short answers are fine. One sentence is often enough.
3. **Tick checkboxes** by changing `[ ]` to `[x]`.
4. **Look at the "Example"** under each question. Copy its *style*, not its words.
5. **Never guess numbers.** If you do not know, write `UNKNOWN`, then fill in *who* will find out and *by when* (see the "I don't know" rule below).
6. **Do not delete questions.** If a question does not apply, write `N/A - because <reason>`.
7. **Keep it honest.** A true "we have 0 customers" is more useful than a nice-sounding guess.

## Status markers (use these everywhere)

| Marker | Meaning |
|---|---|
| `[ ]` | Not started |
| `[~]` | In progress |
| `[x]` | Done |
| `UNKNOWN` | I do not know yet (must have an owner and a date) |
| `N/A` | Does not apply (must have a reason) |

## The "I don't know" rule

If you cannot answer, write it like this and keep going:

```
UNKNOWN | Who finds out: Sam | By when: 2026-11-05 | How: ask 5 target customers
```

## How the questions are written

Every question has the same four lines so nobody has to guess:

- **Q** - the question, in plain words.
- **Why we ask** - one line on why it matters.
- **Answer** - where you write.
- **Example** - a sample answer from a made-up product.

## Words you will see (mini dictionary)

| Word | Simple meaning |
|---|---|
| **Customer** | A real person or company outside your team who **paid**, or who **actively uses** the product (you define which in Part 1). Friends and family do not count. |
| **ICP** (Ideal Customer Profile) | The kind of customer who gets the most value from you and is easiest to win. |
| **Channel** | A place or way you reach customers (e.g., email, search, referrals, partners). |
| **CAC** | Customer Acquisition Cost: how much you spend to win one customer. |
| **LTV** | Lifetime Value: how much money one customer brings you over their whole time with you. |
| **Activation** | The moment a new customer first gets real value from the product. |
| **Retention** | Customers who stay and keep using the product. |
| **Gate** | A checkpoint. You must pass it (or decide to change course) before moving on. |
| **Experiment** | A small, cheap test with a clear pass/fail rule. |
| **AI agent** | An AI tool that does tasks for you (writing, analysing, building). |

## Who can fill what

| Part | Best filled by |
|---|---|
| 0-2 (basics, goal, customer) | Founder / product owner |
| 3-5 (offer, channels, journey) | Product + marketing/sales |
| 6-7 (phases, AI work) | Product + engineering + AI agents |
| 8-9 (metrics, budget, roles) | Founder + finance/ops |
| 10-12 (risks, experiments, review) | Whole team |

## Instructions for AI agents filling this file

1. Only fill a field if you have a **source** (a file, a link, a number someone gave you). Cite the source next to the answer: `(source: <file or link>)`.
2. **Never invent** customer counts, prices, costs, quotes, or results. Write `UNKNOWN` and add an owner and a date.
3. Keep the structure: do not rename headings, field IDs (`CAS-x.y`), or table columns.
4. Ask a human before any action that spends money, contacts a real person, publishes content, or collects personal data.
5. After filling, run the **Part 13 checklist** and report which items fail.

## Product type switch (tick ONE; it unlocks extra questions later)

- [ ] **B2C app / consumer product** (people buy for themselves)
- [ ] **B2B SaaS** (companies or teams buy)
- [ ] **Marketplace** (two sides: buyers and sellers/providers)
- [ ] **Developer tool / API** (developers adopt it)
- [ ] **Service-led / other** (describe in CAS-0.6)

> Look for blocks marked **[B2C only]**, **[B2B only]**, **[Marketplace only]**, **[Dev tool only]**. Answer only the ones that match your tick. Write `N/A - not my type` on the others.

---

# PART 0 - BASICS (the 2-minute identity card)

**CAS-0.1 Q: What is the project/product called?**
*Why we ask: so everyone and every AI agent talks about the same thing.*
Answer: `<<FILL>>`
Example: `PlantPal - an app that reminds people to water houseplants.`

**CAS-0.2 Q: Who owns this document (one person)?**
*Why we ask: one owner means someone keeps it up to date.*
Answer: `<<FILL: name + role>>`

**CAS-0.3 Q: In one sentence, what does the product do and for whom?**
*Why we ask: if you cannot say it simply, customers cannot understand it either.*
Answer: `<<FILL: "We help [WHO] to [DO WHAT] so that [GOOD RESULT]."`
Example: `We help busy plant owners remember to water plants so that their plants stay alive.`

**CAS-0.4 Q: Where is the project today? (tick one)**
- [ ] Only an idea
- [ ] Being built (AI-assisted development in progress)
- [ ] Private beta (a few testers)
- [ ] Publicly launched, fewer than 10 customers
- [ ] 10-100 customers
- [ ] 100-500 customers

**CAS-0.5 Q: Key dates**

| Milestone | Planned date | Real date |
|---|---|---|
| Plan approved | `<<FILL>>` | |
| First working version (MVP) | `<<FILL>>` | |
| Private beta starts | `<<FILL>>` | |
| Public launch | `<<FILL>>` | |
| Customer #100 | `<<FILL>>` | |
| Customer #500 | `<<FILL>>` | |

**CAS-0.6 Q: Anything special about your product type? (write "none" if not)**
Answer: `<<FILL>>`

**CAS-0.7 Q: Who must approve this plan before work starts?**

| Name | Role | Approved? (date) |
|---|---|---|
| `<<FILL>>` | | |

---

# PART 1 - THE GOAL (what does "success" mean?)

**CAS-1.1 Q: What counts as ONE customer for this project? (tick one, then explain)**
*Why we ask: "customer" means different things. Your 500 must mean one thing only.*
- [ ] Someone who **paid** at least once
- [ ] Someone who pays **every month/year** (subscriber)
- [ ] Someone who **actively uses** it (free plan) at least `<<N>>` times in `<<N>>` days
- [ ] A **company/team** that signed a paid pilot or contract
- [ ] Other: `<<FILL>>`

Answer (exact definition): `<<FILL>>`
Example: `A customer is a person who paid for PlantPal Pro and opened the app at least once in the last 30 days.`

**CAS-1.2 Q: Who does NOT count? (always include these)**
- [x] Team members and their families
- [x] Friends who signed up only to be kind
- [x] Test accounts and fake sign-ups
- [x] Refunded or cancelled-within-trial accounts
- Other exclusions: `<<FILL or "none">>`

**CAS-1.3 Q: What is the big goal and deadline?**

| Item | Answer |
|---|---|
| Target number of customers | 500 (change only if you have a reason: `<<FILL>>`) |
| Deadline for 500 | `<<FILL: date>>` |
| Target monthly revenue at 500 customers | `<<FILL>>` or `UNKNOWN` |
| Why does this goal matter? | `<<FILL: e.g., enough proof to raise money / break even>>` |

**CAS-1.4 Q: Milestone targets (fill the "by when" for each step)**

| Step | Customers | By when | Main way to get them |
|---|---|---|---|
| Step 1: first proof | 1-10 | `<<FILL>>` | Personal outreach, interviews, beta invites |
| Step 2: early traction | 11-50 | `<<FILL>>` | `<<FILL>>` |
| Step 3: repeatable | 51-100 | `<<FILL>>` | `<<FILL>>` |
| Step 4: growth | 101-250 | `<<FILL>>` | `<<FILL>>` |
| Step 5: validated growth | 251-500 | `<<FILL>>` | `<<FILL>>` |

**CAS-1.5 Q: What would make you STOP or change direction?**
*Why we ask: deciding "when to quit or pivot" before you are emotional saves time and money.*
Answer: `<<FILL>>`
Example: `If after 8 weeks of outreach fewer than 3 of 50 target users agree to try it, we rethink who we sell to.`

---

# PART 2 - THE CUSTOMER (who exactly are we looking for?)

> Rule: **a specific customer is easier to find than "everyone."** Pick one group first.

**CAS-2.1 Q: Describe your single best first customer (ICP).**

| Question | Answer |
|---|---|
| Who are they (job, age group, or company type)? | `<<FILL>>` |
| Where do they live/work (country, city, industry)? | `<<FILL>>` |
| What problem do they have *right now*? | `<<FILL>>` |
| How do they solve it today (the competitor can be "a spreadsheet" or "nothing")? | `<<FILL>>` |
| How much does that problem cost them (time, money, stress)? | `<<FILL>>` or `UNKNOWN` |
| Why would they pick *you*? | `<<FILL>>` |
| Where do they spend time (websites, communities, events)? | `<<FILL>>` |

Example: `Busy city workers aged 25-40 with 5+ houseplants. They use sticky notes today. They lose about $40 a year on dead plants. They hang out on Instagram plant groups and r/houseplants.`

**CAS-2.2 Q: Who is NOT a good customer? (so you do not waste time)**
Answer: `<<FILL>>`
Example: `Professional florists - they need bulk tools we don't have.`

**CAS-2.3 Q: Reachable-first rule: which customers can you actually contact in the next 14 days?**
*Why we ask: the dream customer may be hard to reach. Start with people you can really reach, learn from them, then aim higher.*
Answer: `<<FILL: list 3 groups you can reach>>`

**CAS-2.4 Q: Evidence check. How many real conversations have you had with target customers?**

| Item | Number |
|---|---|
| Interviews or calls done | `<<N>>` |
| Of those, how many said the problem is painful | `<<N>>` |
| How many asked to try it or pre-pay | `<<N>>` |
| Where are the notes saved? | `<<LINK>>` |

> Warning: friends and family are not valid proof. Count only real target customers.

**CAS-2.5 Q: Write 3 real quotes from target customers about the problem (exact words, with permission).**
1. `<<FILL>>`
2. `<<FILL>>`
3. `<<FILL>>`

**CAS-2.6 [B2B only] Who is who inside the buying company?**

| Role | Job title | What they care about |
|---|---|---|
| User (uses it daily) | `<<FILL>>` | |
| Champion (loves it, pushes inside) | `<<FILL>>` | |
| Budget holder (pays) | `<<FILL>>` | |
| Blocker (could say no: IT, legal) | `<<FILL>>` | |

**CAS-2.7 [Marketplace only] Two sides. Which side do you win first, and why?**

| Side | Who | First side to win? | Why this side first? |
|---|---|---|---|
| Supply (sellers/providers) | `<<FILL>>` | [ ] | `<<FILL>>` |
| Demand (buyers) | `<<FILL>>` | [ ] | `<<FILL>>` |

How will you avoid an "empty marketplace" at launch? `<<FILL>>`
Example: `We hand-recruit 30 tutors in one city first, then invite students.`

**CAS-2.8 [Dev tool only] Which developers first (language, stack, company size)? Where do they learn about tools?**
Answer: `<<FILL>>`
Example: `Python backend developers at startups; they read Hacker News and GitHub.`

---

# PART 3 - THE OFFER (what are we asking them to say yes to?)

**CAS-3.1 Q: Positioning sentence (fill the blanks).**
Answer: `For <<WHO>> who <<PROBLEM>>, <<PRODUCT>> is a <<CATEGORY>> that <<MAIN BENEFIT>>. Unlike <<ALTERNATIVE>>, we <<DIFFERENCE>>.`

**CAS-3.2 Q: The top 3 benefits (results for the customer, not features).**
1. `<<FILL>>`
2. `<<FILL>>`
3. `<<FILL>>`

**CAS-3.3 Q: Pricing and offer**

| Item | Answer |
|---|---|
| Free plan / free trial? | [ ] Free plan [ ] Free trial (`<<days>>`) [ ] Neither |
| Paid price | `<<FILL: amount per month/year or per use>>` |
| Why this price? (cost, competitor price, customer said so) | `<<FILL>>` |
| Early-bird / founding-customer offer | `<<FILL>>` or `none` |
| Refund policy | `<<FILL>>` |
| First-time-win moment: what is the first value they get, and how fast? | `<<FILL>>` |

**CAS-3.4 Q: Proof we can show (tick what you really have; do NOT invent).**
- [ ] Demo video
- [ ] Real customer quotes (with permission)
- [ ] Case study / before-and-after result
- [ ] Numbers (e.g., "saves 3 hours a week" - source: `<<FILL>>`)
- [ ] Logos of known users (with permission)
- [ ] Security / privacy statement
- [ ] None yet -> plan to collect: `<<FILL>>`

**CAS-3.5 Q: Main objections (reasons people say "no") and our honest answer.**

| Objection | Honest answer |
|---|---|
| "Too expensive" | `<<FILL>>` |
| "I already use X" | `<<FILL>>` |
| "I don't trust a new product" | `<<FILL>>` |
| `<<FILL>>` | `<<FILL>>` |

**CAS-3.6 Q: Competitors and alternatives (include "do nothing").**

| Name | What they do well | Where we are better | Their price |
|---|---|---|---|
| `<<FILL>>` | | | |
| Do nothing / manual way | | | |

---

# PART 4 - CHANNELS (where and how do we reach customers?)

> Founders often only try the channels they already know. Look at **all** the options below, then pick **three to test**, then focus on **one winner**. (This is the "Bullseye" idea from the book *Traction*.)

## 4A. Brainstorm: score every channel

For each channel write a one-line idea of how it could work for you. Then score 1 (unlikely) to 5 (very promising) for **Fit** (do customers hang out there?), **Cost** (5 = cheap), and **Speed** (5 = fast results).

| # | Channel | Idea for our product | Fit | Cost | Speed | Total |
|---|---|---|---|---|---|---|
| 1 | Personal outreach (email, DM, calls) | `<<FILL>>` | | | | |
| 2 | Warm network and introductions | | | | | |
| 3 | Referrals / word of mouth | | | | | |
| 4 | Content marketing (blog, video, guides) | | | | | |
| 5 | Search engine optimization (SEO) | | | | | |
| 6 | Paid search / social ads | | | | | |
| 7 | Social media (organic) | | | | | |
| 8 | Community building (forums, Discord, Slack groups) | | | | | |
| 9 | Product launch sites and directories | | | | | |
| 10 | Public relations and press | | | | | |
| 11 | Partnerships / business development | | | | | |
| 12 | Integrations and app stores / marketplaces | | | | | |
| 13 | Email marketing and newsletters | | | | | |
| 14 | Influencers and creators | | | | | |
| 15 | Events, webinars, conferences | | | | | |
| 16 | Sales team / cold outbound at scale | | | | | |
| 17 | Viral features / invite loops | | | | | |
| 18 | Affiliate / reseller programs | | | | | |
| 19 | Offline (flyers, local ads, trade shows) | | | | | |
| 20 | Other: `<<FILL>>` | | | | | |

**Total = Fit + Cost + Speed (max 15).**

## 4B. Pick your 3 test channels

| Rank | Channel | Why chosen | Test budget | Test length (1-2 weeks) | Pass rule (what result = success?) |
|---|---|---|---|---|---|
| 1 | `<<FILL>>` | | | | `<<FILL>>` |
| 2 | `<<FILL>>` | | | | |
| 3 | `<<FILL>>` | | | | |

Example pass rule: `Out of 40 personalised emails, at least 4 replies and 2 booked demos.`

## 4C. Channel rules (so tests are fair)

- Run **small** tests (e.g., 2-4 ads, not 40).
- Time-box each test (1-2 weeks).
- Write down results in **Part 11 (Experiment Log)**.
- Keep **one** winner focus; add a second channel only after the first works.
- When a channel stops working (rising cost, falling results), run 4A again.

## 4D. Extra questions by product type

**[B2C only]**
- What is the "hook" (first 10 seconds) that makes people care? `<<FILL>>`
- Is there a share/invite feature, and what does the sharer get? `<<FILL>>`
- Which app store or platform rules affect us? `<<FILL>>`

**[B2B only]**
- Sales motion: [ ] Self-serve (credit card) [ ] Founder-led sales [ ] Sales team [ ] Mix
- First 10 target companies (names or lists): `<<FILL>>`
- Pilot offer (length, price, success criteria): `<<FILL>>`
- Proof the buyer will ask for (security review, references): `<<FILL>>`

**[Marketplace only]**
- How do we get the first 50 on the hard side by hand? `<<FILL>>`
- How do we stop buyers and sellers from leaving to trade outside the platform? `<<FILL>>`

**[Dev tool only]**
- Time for a developer to get a first result ("time to hello world"): `<<minutes>>`
- Docs, examples, open-source or SDK plan: `<<FILL>>`
- Where do we answer developer questions (GitHub, Discord, Stack Overflow)? `<<FILL>>`

---

# PART 5 - THE CUSTOMER JOURNEY (from stranger to happy customer)

> Fill one row per stage. Each stage needs **one action** and **one number** to watch.

| Stage | Question the customer asks | What we do | Where | Number to watch | Target |
|---|---|---|---|---|---|
| 1. Aware | "What is this?" | `<<FILL>>` | | Visitors | `<<N>>` |
| 2. Interested | "Is this for me?" | | | Sign-ups / demo requests | |
| 3. Trying | "Can I get started easily?" | | | Activation rate | |
| 4. Buying | "Is it worth paying?" | | | Free-to-paid conversion | |
| 5. Using | "Does it keep helping me?" | | | Weekly active users / retention | |
| 6. Loving | "Would I tell others?" | | | Referrals, reviews, "very disappointed" score | |
| 7. Staying | "Why would I not leave?" | | | Churn rate | |

**CAS-5.1 Q: What exactly is the "activation moment" (the first real win)?**
Answer: `<<FILL>>`
Example: `User adds their first plant and receives their first reminder.`

**CAS-5.2 Q: Onboarding: first 10 customers get a personal welcome. How?**
Answer: `<<FILL>>`

**CAS-5.3 Q: How do we ask for feedback and referrals (and when)?**
Answer: `<<FILL>>`
Example: `Day 3: short survey. Day 14: ask "who else would love this?" and offer one free month for each friend who joins.`

**CAS-5.4 Q: Where do we record every lead and customer?**
Tool/Link: `<<FILL: spreadsheet, CRM, or database>>`
Fields saved at minimum: name/company, source channel, date, stage, owner, next step, consent status.

---

# PART 6 - PHASES AND GATES (from idea to first 500 customers)

> This is the heart of the plan. Work in **phases**. At the end of each phase is a **GATE**: a short checklist. If the gate is passed, move on. If not, fix or change course. **Write the decision in the gate box.**

## Phase map

```
P0 Discover  ->  P1 Build  ->  P2 Private Beta  ->  P3 Public Launch  ->  P4 Repeatable Growth  ->  P5 Validate at 500
  (idea)      (AI-assisted    (customers 1-10)     (customers 11-100)     (customers 101-500)       (decide next)
               MVP)
```

## PHASE P0 - DISCOVER (customers: 0, goal: prove the problem is real)

**Do these things (tick when done):**
- [ ] Filled Parts 1-3 of this document
- [ ] Held at least `<<N, suggest 15-20>>` real customer interviews (notes at: `<<LINK>>`)
- [ ] Made a simple landing page or one-page description with a "join waitlist" button
- [ ] Collected `<<N>>` waitlist sign-ups from the target group (not friends)
- [ ] Wrote the top-3 problems customers named

**GATE P0 (answer all):**

| Check | Pass rule (edit if needed) | Result | Pass? |
|---|---|---|---|
| Problem is painful | At least `<<e.g., 7 of 15>>` interviewees say it is a top-3 problem | `<<FILL>>` | [ ] |
| Willingness to act | At least `<<e.g., 5>>` agree to test, join a pilot, or pre-pay | `<<FILL>>` | [ ] |
| Reachable | We can name `<<e.g., 50>>` target people we can contact | `<<FILL>>` | [ ] |

Decision: [ ] GO  [ ] CHANGE (what?) `<<FILL>>`  [ ] STOP     Date: `<<FILL>>`  Decided by: `<<FILL>>`

## PHASE P1 - BUILD (customers: 0, goal: a small working product + growth tools ready)

**Do these things:**
- [ ] MVP does the **one** main job from CAS-0.3 (nothing extra)
- [ ] Sign-up/onboarding works end to end
- [ ] Payments or pilot agreement ready (CAS-3.3)
- [ ] Tracking set up for the Part 8 numbers (sign-ups, activation, paid, churn, source channel)
- [ ] Landing page, pricing page, and demo/walkthrough ready
- [ ] Privacy policy, terms, and consent prompts in place (Part 10)
- [ ] Feedback button or short survey inside the product
- [ ] Support email/chat working
- [ ] Customer list/CRM ready (CAS-5.4)

**GATE P1:**

| Check | Pass rule | Result | Pass? |
|---|---|---|---|
| A new user can reach the first win (CAS-5.1) without help | `<<e.g., 8 of 10 testers in under 10 minutes>>` | `<<FILL>>` | [ ] |
| Tracking works | Test sign-up shows up in the numbers with its source channel | `<<FILL>>` | [ ] |
| Can take payment or sign a pilot | A test purchase succeeds | `<<FILL>>` | [ ] |
| No blocking bugs | `<<e.g., 0 critical, <=3 minor>>` | `<<FILL>>` | [ ] |

Decision: [ ] GO  [ ] FIX FIRST  Date: `<<FILL>>`  Decided by: `<<FILL>>`

## PHASE P2 - PRIVATE BETA (customers 1-10, goal: first real proof + learn fast)

**Do these things:**
- [ ] Invite the first `<<N, suggest 20-50>>` target users **personally** (channel #1 or #2 in Part 4)
- [ ] Talk to every beta user at least once (call, chat, or video)
- [ ] Offer a founding-customer deal (CAS-3.3)
- [ ] Fix the top 3 problems they report
- [ ] Collect 3 real quotes and permission to use them
- [ ] Ask "How would you feel if you could no longer use this?" (see Part 8)

**GATE P2:**

| Check | Pass rule | Result | Pass? |
|---|---|---|---|
| First customers | At least `<<10>>` real customers per CAS-1.1 | `<<FILL>>` | [ ] |
| Activation | At least `<<e.g., 60%>>` reach first win | `<<FILL>>` | [ ] |
| Retention signal | At least `<<e.g., 40%>>` still active after `<<30>>` days | `<<FILL>>` | [ ] |
| "Very disappointed" score | At least `<<e.g., 40%>>` say they would be very disappointed without it | `<<FILL>>` | [ ] |
| We know where each customer came from | 100% have a source channel | `<<FILL>>` | [ ] |

Decision: [ ] GO to launch  [ ] STAY IN BETA (what to fix?) `<<FILL>>`  [ ] CHANGE audience/offer  Date: `<<FILL>>`

## PHASE P3 - PUBLIC LAUNCH (customers 11-100, goal: find the channel that works)

**Do these things:**
- [ ] Launch plan done: date `<<FILL>>`, where we announce `<<FILL>>`
- [ ] Launch assets ready: short description, 3 screenshots, demo video, FAQ, pricing, press/launch post
- [ ] Run the 3 test channels from Part 4B (one at a time or in parallel, time-boxed)
- [ ] Log every test in Part 11
- [ ] Weekly review held (Part 12)
- [ ] Reply to every question and review within `<<hours>>` hours
- [ ] Choose one **winner channel** after tests

**GATE P3:**

| Check | Pass rule | Result | Pass? |
|---|---|---|---|
| Customers | At least `<<100>>` | `<<FILL>>` | [ ] |
| One winner channel | One channel gives at least `<<e.g., 30%>>` of new customers at an acceptable CAC | `<<FILL>>` | [ ] |
| Not only friends | At least `<<e.g., 80%>>` of customers are outside the team's network | `<<FILL>>` | [ ] |
| Activation and retention | Not worse than Phase P2 by more than `<<e.g., 10 points>>` | `<<FILL>>` | [ ] |
| Support is coping | Median reply time under `<<FILL>>` | `<<FILL>>` | [ ] |

Decision: [ ] GO to growth  [ ] RETEST channels  [ ] FIX product  Date: `<<FILL>>`

## PHASE P4 - REPEATABLE GROWTH (customers 101-500, goal: make it predictable)

**Do these things:**
- [ ] Put more effort and budget into the winner channel
- [ ] Add one second channel only after the first works
- [ ] Write simple "playbooks" so anyone can repeat the winning steps (scripts, templates, checklists)
- [ ] Set up referral or invite programme (CAS-5.3)
- [ ] Review CAC, LTV, and payback every month by channel (Part 8)
- [ ] Automate repeat tasks (with human review) - see Part 7
- [ ] Re-run the channel brainstorm (4A) if a channel gets too expensive

**GATE P4 (mid-point, at about 250 customers):**

| Check | Pass rule | Result | Pass? |
|---|---|---|---|
| Customers | At least `<<250>>` | `<<FILL>>` | [ ] |
| Unit economics | LTV : CAC at least `<<3:1>>` or a clear plan to reach it | `<<FILL>>` | [ ] |
| Payback | CAC repaid in under `<<e.g., 12 months, or 3 months for low-price B2C>>` | `<<FILL>>` | [ ] |
| Churn | Monthly churn at or under `<<FILL>>` | `<<FILL>>` | [ ] |

Decision: [ ] CONTINUE  [ ] FIX economics  [ ] CHANGE channel mix  Date: `<<FILL>>`

## PHASE P5 - VALIDATE AT 500 (goal: decide what comes next with evidence)

**Do these things:**
- [ ] Finish the **Growth Validation Scorecard** in Part 8.4
- [ ] Write a one-page "What we learned" summary (Part 12.3)
- [ ] Decide: scale, adjust, or stop

**GATE P5 (final):**

| Check | Pass rule | Result | Pass? |
|---|---|---|---|
| 500 customers reached | Meets CAS-1.1 definition | `<<FILL>>` | [ ] |
| Growth is repeatable | At least `<<2 or 3>>` months of steady new customers from known channels | `<<FILL>>` | [ ] |
| Customers stay | Retention at or above `<<FILL>>` | `<<FILL>>` | [ ] |
| Economics work | LTV : CAC at or above `<<3:1>>` | `<<FILL>>` | [ ] |
| Customers love it | "Very disappointed" at or above `<<40%>>` | `<<FILL>>` | [ ] |

Decision: [ ] SCALE  [ ] ADJUST (what?) `<<FILL>>`  [ ] STOP/PIVOT  Date: `<<FILL>>`

---

# PART 7 - AI-DRIVEN WORK PLAN (how AI agents and humans share the work)

> Rule of thumb: **AI drafts, humans decide.** AI can prepare, analyse, and automate. A human approves anything that spends money, talks to real people, or goes public.

## 7.1 Who does what, by phase

| Phase | Tasks AI agents can do | Tasks humans must do | Human approval needed for |
|---|---|---|---|
| P0 Discover | Summarise interview notes, group problems, draft interview questions, scan competitors | Hold interviews, judge what matters | Contacting real people |
| P1 Build | Write code, tests, tracking events, landing-page text, docs | Review code, set product scope, test with users | Releasing to users |
| P2 Beta | Draft invites, tag feedback, summarise calls, flag bugs | Talk to users, decide fixes | Sending messages |
| P3 Launch | Draft launch posts, FAQs, ad variants, reports on results | Final wording, replies to customers, budget | Publishing, spending money |
| P4 Growth | Analyse channels, find patterns, draft playbooks, automate reports | Choose channels, manage partners, handle key accounts | Spend increases, new channels |
| P5 Validate | Build scorecard, write learnings draft | Make the decision | Final decision |

## 7.2 AI tools and agents in use

| Task | Tool / agent name | Who owns it | Data it can see | Human check before output goes out? |
|---|---|---|---|---|
| `<<FILL>>` | | | | [ ] Yes |

## 7.3 Rules for AI use (tick all that you agree to)

- [ ] AI never invents customer quotes, reviews, numbers, or case studies
- [ ] AI-written messages to real people are reviewed by a human first
- [ ] Personal data is only given to tools approved in 7.2
- [ ] We tell users when they talk to an AI (if applicable): `<<FILL>>`
- [ ] Every AI result that drives a decision is checked against real data
- [ ] AI prompts/instructions used are saved here: `<<LINK>>`

## 7.4 Tracking the AI-build side (what must exist before launch)

| Item | Done? | Link / note |
|---|---|---|
| Event tracking: visit, sign-up, activation, purchase, cancel | [ ] | |
| Source tracking (UTM links or "how did you hear about us?") | [ ] | |
| Dashboard showing Part 8 numbers | [ ] | |
| Error monitoring and uptime alerts | [ ] | |
| Feedback and support inbox | [ ] | |
| Backups and data export | [ ] | |

---

# PART 8 - NUMBERS (how we know it is working)

## 8.1 Formulas (copy exactly)

| Name | Formula | Plain meaning |
|---|---|---|
| **CAC** | Total acquisition spend ÷ new customers | Cost to win one customer. Include ads, tools, and the **paid time** of people doing outreach. |
| **LTV** | Average revenue per customer per month × average months they stay × gross margin | Money one customer is worth over their life. |
| **LTV : CAC** | LTV ÷ CAC | Common target is **3 : 1 or better**. |
| **Payback months** | CAC ÷ (monthly revenue per customer × gross margin) | How fast you earn back what you spent. |
| **Conversion rate** | People who did the step ÷ people who could | e.g., visitors who signed up. |
| **Activation rate** | New users who reach the first win ÷ new users | |
| **Churn (monthly)** | Customers lost this month ÷ customers at start of month | |
| **Retention (day 30)** | Users still active on day 30 ÷ users who started | |
| **"Very disappointed" score** | Users answering "very disappointed" ÷ all who answered "How would you feel if you could no longer use this product?" | A common product-fit signal; **40% or more** is a widely used benchmark. |
| **Referral rate** | New customers from referrals ÷ all new customers | |

> Benchmarks vary by product and market. Treat the targets below as **starting guesses** and replace them with your own once you have real data.

## 8.2 Targets and actuals (update every week)

| Metric | Target | Week 1 | Week 2 | Week 3 | Week 4 | Source of number |
|---|---|---|---|---|---|---|
| New customers | `<<FILL>>` | | | | | |
| Total customers | | | | | | |
| Visitors | | | | | | |
| Sign-ups / demo requests | | | | | | |
| Activation rate | | | | | | |
| Free-to-paid conversion | | | | | | |
| Monthly churn | | | | | | |
| Day-30 retention | | | | | | |
| Revenue this period | | | | | | |
| Total acquisition spend | | | | | | |
| Blended CAC | | | | | | |
| LTV (estimate) | | | | | | |
| LTV : CAC | | | | | | |
| Payback months | | | | | | |
| "Very disappointed" score | | | | | | |
| Support: median first reply time | | | | | | |

## 8.3 Numbers by channel (one row per channel you use)

| Channel | Spend | Leads | New customers | CAC | Share of all customers | Quality note (do they stay?) |
|---|---|---|---|---|---|---|
| `<<FILL>>` | | | | | | |

> Warning: a low CAC from a channel that brings customers who leave quickly is a trap. Always look at **retention by channel**.

## 8.4 Growth Validation Scorecard (fill at 100, 250, and 500 customers)

Score each line: **Green** (meets target), **Yellow** (close, with a plan), **Red** (missed).

| # | Validation question | Evidence (number + link) | Green / Yellow / Red |
|---|---|---|---|
| 1 | Do real target customers (not friends) buy or use it? | `<<FILL>>` | |
| 2 | Do they get value fast (activation)? | | |
| 3 | Do they stay (retention / churn)? | | |
| 4 | Would they be very disappointed without it (>= target)? | | |
| 5 | Do we have at least one channel that works repeatedly? | | |
| 6 | Does each customer earn more than they cost (LTV : CAC)? | | |
| 7 | Do customers tell others (referrals / reviews)? | | |
| 8 | Can the team handle more customers without quality dropping? | | |
| 9 | Are risks (legal, privacy, platform rules) under control? | | |
| 10 | Is growth predictable month to month? | | |

**Reading the scorecard:** 8+ Green = scale. 5-7 Green = adjust and re-test. Fewer than 5 Green = pause growth spending and fix the biggest Red first.

---

# PART 9 - BUDGET, TOOLS AND TEAM

## 9.1 Budget (money and time)

| Item | Phase | Planned amount | Limit (stop-spending line) | Actual spent | Owner |
|---|---|---|---|---|---|
| Ads / paid tests | P3-P4 | `<<FILL>>` | | | |
| Tools and software (CRM, email, analytics) | P1-P5 | | | | |
| AI tools and usage | P0-P5 | | | | |
| Content (video, design, writing) | P1-P4 | | | | |
| Events / partnerships | P3-P4 | | | | |
| Incentives (discounts, referral rewards) | P2-P4 | | | | |
| People time (hours per week) | P0-P5 | | | | |
| **Total** | | | | | |

**CAS-9.2 Q: Spending rule.** Who can approve spend, and up to how much without asking?
Answer: `<<FILL>>`
Example: `Anyone up to $50 per test. Over $50 needs the owner. Over $500 needs two approvers.`

## 9.3 Tools

| Need | Tool chosen | Cost | Owner | Data stored here |
|---|---|---|---|---|
| Customer list / CRM | `<<FILL>>` | | | |
| Email sending | | | | |
| Analytics | | | | |
| Payments | | | | |
| Support inbox / chat | | | | |
| Scheduling / calls | | | | |
| Surveys / feedback | | | | |

## 9.4 Team roles (RACI)

**R** = Responsible (does it), **A** = Accountable (final yes/no, only one), **C** = Consulted, **I** = Informed.

| Activity | Founder/Owner | Product | Engineering / AI agents | Marketing / Growth | Sales / Success | Finance / Ops |
|---|---|---|---|---|---|---|
| Customer interviews | A | R | I | C | C | I |
| Channel tests | A | C | C | R | C | I |
| Launch plan | A | R | C | R | C | I |
| Tracking and dashboards | C | A | R | C | I | C |
| Customer onboarding | I | C | C | C | A/R | I |
| Support | I | C | C | I | A/R | I |
| Budget control | A | I | I | C | I | R |
| Weekly review | A | R | R | R | R | C |

> Edit letters to match your team. Each row must have **exactly one A**. Write real names here: `<<FILL: name = role>>`.

**CAS-9.5 Q: Hours per week each person gives to growth work.**
Answer: `<<FILL>>`
Example: `Founder 15 h, marketer 20 h, engineer 5 h, AI agents: weekly report only.`

---

# PART 10 - RISKS, LEGAL AND TRUST

> This part is a practical checklist, **not legal advice**. Ask a qualified professional about the laws that apply where you and your customers live.

## 10.1 Rules to check before you contact or track anyone

- [ ] **Permission (consent):** we know when we need people's permission to email, text, or call them
- [ ] **Privacy:** privacy policy is published and matches what we really do with data
- [ ] **Data rights:** people can ask to see or delete their data, and we know how to do it
- [ ] **Email rules:** every marketing email has our real address and an easy unsubscribe
- [ ] **Cookies/tracking:** consent banner or notice in place where required
- [ ] **Children:** we do not target or collect data from children, or we follow the extra rules
- [ ] **Ads and platforms:** we read the rules of every ad platform, app store, and site where we post
- [ ] **Honest claims:** every claim on our site can be proven; no fake reviews, fake counts, or invented logos
- [ ] **Payments and taxes:** we know which taxes and payment rules apply
- [ ] **Security:** passwords/keys are stored safely; customer data is protected; AI tools only get data they need

Countries/regions our customers live in: `<<FILL>>`
Laws or rules that apply (to confirm with a professional): `<<FILL>>`

## 10.2 Risk register

| # | What could go wrong? | How likely (L/M/H) | How bad (L/M/H) | What we do to prevent it | What we do if it happens | Owner |
|---|---|---|---|---|---|---|
| 1 | No channel works | | | | | |
| 2 | Customers sign up but do not stay | | | | | |
| 3 | Acquisition costs more than customers are worth | | | | | |
| 4 | Ad account blocked / platform rule broken | | | | | |
| 5 | Product breaks when many people join | | | | | |
| 6 | Privacy or data problem | | | | | |
| 7 | AI writes something wrong or off-brand | | | | | |
| 8 | Key team member unavailable | | | | | |
| 9 | Competitor copies us or cuts price | | | | | |
| 10 | `<<FILL>>` | | | | | |

---

# PART 11 - EXPERIMENT LOG (one row per test; copy the row to add more)

> A good experiment has a **clear guess**, a **small cost**, a **time limit**, and a **pass rule written BEFORE you start**.

| ID | Date start-end | Channel | Guess ("If we do X, then Y will happen because Z") | Cost | Pass rule | Result (numbers) | Pass / Fail / Unclear | What we learned | Next step |
|---|---|---|---|---|---|---|---|---|---|
| EXP-001 | `<<FILL>>` | | | | | | | | |
| EXP-002 | | | | | | | | | |
| EXP-003 | | | | | | | | | |

Example row: `EXP-001 | 3-14 Mar | Cold email | If we email 40 plant-shop owners with a short offer, 10% will book a demo because they lose sales to dead plants | $0 + 3 h | >= 4 demos | 2 demos | Fail | Subject line too vague | Rewrite subject, test on 40 new shops (EXP-002)`

**Experiment rules**
1. Write the pass rule **before** running the test.
2. Run one change at a time when you can.
3. Record failures too; they save money later.
4. After each test choose one: **Scale it, Fix it, Drop it.**

---

# PART 12 - WEEKLY REVIEW AND LEARNING

## 12.1 Weekly review (30 minutes, same day every week)

**Meeting day/time:** `<<FILL>>`  **Who attends:** `<<FILL>>`

Copy this block each week:

```
WEEK OF: <<date>>
Customers this week: <<N>>  | Total: <<N>> | Target: <<N>>
Best channel this week: <<name>>   Worst channel: <<name>>
What worked: <<FILL>>
What did not: <<FILL>>
Biggest thing customers said: <<FILL>>
Experiments running / finished: <<IDs>>
Decisions made: <<FILL>>
Next week's top 3 actions: 1) <<FILL>> (owner, date)  2) <<FILL>>  3) <<FILL>>
Blocked by: <<FILL or "nothing">>
```

## 12.2 Monthly check

- [ ] Update Part 8.2 and 8.3
- [ ] Recalculate CAC, LTV, LTV : CAC by channel
- [ ] Re-read Part 10.2 risks and update
- [ ] Check budget vs. plan (Part 9.1)
- [ ] Decide if the next gate is close

## 12.3 Final "What We Learned" (fill at the end of P5)

| Question | Answer |
|---|---|
| Who turned out to be our real best customer? | `<<FILL>>` |
| Which channel won, and why? | `<<FILL>>` |
| Which channels did not work, and why? | `<<FILL>>` |
| What surprised us? | `<<FILL>>` |
| What would we do differently next time? | `<<FILL>>` |
| What is the next goal after 500 customers? | `<<FILL>>` |
| Template improvements to make for the next project | `<<FILL>>` |

---

# PART 13 - FINAL CHECK (the "is this ready?" list)

Tick each item. If any item is unticked, the document is **not ready**.

**Completeness**
- [ ] No `<<FILL>>` markers remain (or each is replaced by `UNKNOWN` with an owner and date, or `N/A` with a reason)
- [ ] Product type chosen and only matching blocks answered
- [ ] "Customer" is defined once (CAS-1.1) and used the same way everywhere

**Clarity**
- [ ] A stranger can read Part 0 and Part 1 and understand the goal in 2 minutes
- [ ] Every channel test has a pass rule written before the test
- [ ] Every gate has pass rules and a named decision-maker

**Honesty**
- [ ] Every number has a source
- [ ] No friends, family, or team members are counted as customers
- [ ] No invented quotes, reviews, or results

**Safety**
- [ ] Part 10.1 legal and privacy checklist reviewed
- [ ] Human approval steps listed in Part 7.1 are in place

**Ownership**
- [ ] Every action has one owner and one date
- [ ] Budget limits and approvers are written (CAS-9.2)

**Sign-off**

| Role | Name | Date | Approved |
|---|---|---|---|
| Owner | `<<FILL>>` | | [ ] |
| Reviewer | `<<FILL>>` | | [ ] |

---

# APPENDIX A - WORKED MINI-EXAMPLE (made-up, so you can see the style)

| Field | Filled example |
|---|---|
| Product | PlantPal, a plant-watering reminder app |
| Product type | B2C app |
| Customer definition | Paid for Pro and active in last 30 days |
| ICP | City workers aged 25-40 with 5+ houseplants |
| Top 3 test channels | Plant communities, short videos, plant-shop partnerships |
| Pass rule (community test) | 30 posts/replies in 2 weeks give 100 visits and 15 sign-ups |
| P2 gate | 10 paying customers, 60% activation, 40% still active at day 30 |
| CAC / LTV | $12 / $54 (LTV : CAC = 4.5 : 1) |
| Decision at P3 | GO: community wins at $9 CAC; videos fail; partnerships retest |

# APPENDIX B - IF YOU ARE STUCK

| Problem | Try this |
|---|---|
| "I can't find customers to talk to" | Search for where they ask for help online; offer a 15-minute chat and a small thank-you. |
| "Nobody replies" | Shorten your message to 3 sentences, mention their problem first, ask one easy question. |
| "People sign up but never use it" | Watch 5 new users try it live; fix the first 5 minutes before spending on ads. |
| "People use it but won't pay" | Re-check the price, the offer, or whether the problem is painful enough (Part 2). |
| "Ads cost too much" | Pause ads; go back to personal outreach, communities, or partnerships. |
| "I don't know my numbers" | Start with just three: new customers, source channel, and who is still active after 30 days. |

# APPENDIX C - CHANGE LOG

| Date | Version | What changed | Who |
|---|---|---|---|
| `<<FILL>>` | 1.0.0 | First version from template | `<<FILL>>` |

# APPENDIX D - SOURCES THAT SHAPED THIS TEMPLATE

- *Traction* by Gabriel Weinberg and Justin Mares: the 19 traction channels, the Bullseye test-then-focus method, and the 50/50 product-and-traction rule.
- Founder go-to-market guides for the first 100 customers (for example Mercury's founder guide, which warns that friends are not valid customers).
- Customer-acquisition planning guides covering ICP, channels, CAC, LTV, payback, and the 3:1 LTV:CAC rule of thumb.
- The widely used "very disappointed" product-fit survey with a 40% benchmark.
