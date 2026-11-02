# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **What is this document?**
> A *Customer Health Score* is a number from 0 to 100 that tells you, at a glance, whether a customer is **happy and likely to stay (Green)**, **unsure (Yellow)**, or **unhappy and likely to leave (Red)**.
> This document is where you decide, **in plain words**, how your product will calculate that number, who looks at it, and what you do about it. It covers the whole journey: **build the product, test it, launch it, and reach your first 500 customers.**

## Who can fill this in?

Anyone. If you can answer "What does our product do?" and "What would make a customer happy?", you can fill this in. You do **not** need to know math, coding, or AI.

## The 5 simple rules

1. **Answer every question.** Look for the text `[FILL IN]` and replace it with your answer. Delete the brackets.
2. **Never guess.** If you do not know, write: `TBD - [who will find out] - [date]`. A visible "TBD" is better than a hidden guess.
3. **Use numbers where you can.** "Many users" is weak. "At least 3 logins per week" is strong.
4. **Copy the examples.** Every question has an `Example:` line. Change the example to fit your product. Then delete the example line if you like.
5. **Keep it short.** One or two sentences per answer is enough.

## Symbols used in this document

| Symbol | Meaning |
|---|---|
| `[FILL IN]` | You must type your answer here |
| `Example:` | A sample answer. Do not leave the example as your answer |
| `[PICK ONE]` | Choose one option and delete the others |
| `[ ]` / `[x]` | A checkbox. Replace `[ ]` with `[x]` when done |
| 🟢 🟡 🔴 | Healthy / Watch closely / At risk |
| 👤 | A human must do or approve this |
| 🤖 | An AI agent can do this |

## How to answer ONE question (a walk-through)

Here is a real question from Section 1, answered step by step.

1. **Read the question.** "What problem does your product solve, in one sentence?"
2. **Read the example.** "People forget to drink water, so our app reminds them."
3. **Think about YOUR product.** Say it out loud to a friend. If they understand, you are done.
4. **Type your answer** where it says `[FILL IN]` and delete the brackets.
   - Before: `[FILL IN]`
   - After: `Parents forget school pickup times, so our app sends them a reminder.`
5. **Do not know the answer?** Write `TBD - Maria - 20 March` (a name and a date). Move on. Come back later.

## If you get stuck

| Problem | What to do |
|---|---|
| I do not understand a word | Look it up in **Appendix A (Glossary)**. Every word is explained in plain language. |
| I do not know a number | Use the **suggested value** in the table, then write "suggested value, not tested" next to it. |
| The question does not fit my product | Write `Not applicable because ...` and give a short reason. Never leave it blank. |
| I am scared of a section with legal words (Section 13) | That is normal. Answer what you can, then ask a lawyer to check it. You are **not** expected to be a lawyer. |
| I have too many ideas | Pick the **three most important** and write only those. |
| Two people disagree | The **document owner** (Section 0) decides. Write down why. |

## Two ways to fill it in

| Path | Time | Do this |
|---|---|---|
| **Quick Start** | about 20 minutes | Fill in only sections marked **⚡ QUICK START**: 0, 1, 3, 4, 5. You will have a working first version. |
| **Full Version** | 3 to 6 hours (spread over several days is fine) | Fill in every section 0 to 16, then complete the checklist in Section 12. |

> **Important:** Quick Start is enough to **start**. Before you collect real customer data, Section 13 (legal and privacy) must be done.

**Recommended order:** Start with Quick Start. Launch with it. Come back and fill in the rest as you learn.

## When to update this document

- At the **end of every phase** (Section 2)
- After every **major product change**
- When the team says "this score does not match reality"
- At least **once every 3 months**

## Where to save it

Save the finished file as `Customer_Health_Scoring.md` in the **Customer feedback and product improvement** folder of your project. Use one copy **per project**. Never edit this master template directly; copy it first.

---

# TABLE OF CONTENTS

| # | Section | Quick Start? |
|---|---|---|
| 0 | Document control | ⚡ |
| 1 | Project snapshot | ⚡ |
| 2 | The 6-phase journey: build to 500 customers | |
| 3 | Customer definition and segments | ⚡ |
| 4 | Health signals: what we measure | ⚡ |
| 5 | The scoring model | ⚡ |
| 6 | Data collection and tools | |
| 7 | AI agent workflow and AI governance | |
| 8 | Action playbooks, churn exit survey and win-back | |
| 9 | Feedback-to-roadmap loop | |
| 10 | Roles, owners and rhythm (RACI) | |
| 11 | Reporting and dashboard | |
| 12 | QA and launch checklist (phase gates) | |
| 13 | Privacy, legal and compliance | |
| 14 | Tools and integration setup | |
| 15 | Budget, staffing and timeline | |
| 16 | Risks, open questions and lessons learned | |
| A to F | Glossary, one-page summary, final check, sources, industry add-ons, filled-in sample project | |

---

# 0. DOCUMENT CONTROL ⚡ QUICK START

| Field | Your answer |
|---|---|
| Project name | `[FILL IN]` (Example: "FitTrack App") |
| Product one-line description | `[FILL IN]` (Example: "A phone app that helps people log workouts") |
| Document owner (one person) | `[FILL IN]` |
| Backup owner | `[FILL IN]` |
| Version | `v0.1` |
| Date created | `[FILL IN]` |
| Last reviewed | `[FILL IN]` |
| Next review date | `[FILL IN]` |
| Current phase (see Section 2) | `[PICK ONE: 1 Build / 2 Internal Test / 3 Beta / 4 Launch / 5 First 100 / 6 First 500]` |
| Current number of customers | `[FILL IN]` |
| Status | `[PICK ONE: Draft / In Review / Approved]` |

### Approvals

| Role | Name | Date approved |
|---|---|---|
| Product owner | `[FILL IN]` | `[FILL IN]` |
| Engineering lead | `[FILL IN]` | `[FILL IN]` |
| Customer success / support lead | `[FILL IN]` | `[FILL IN]` |
| QA lead | `[FILL IN]` | `[FILL IN]` |

---

# 1. PROJECT SNAPSHOT ⚡ QUICK START

> **Why this matters:** Everything else in this document depends on these answers. If these are fuzzy, the health score will be fuzzy.
>
> **In plain words:** Pretend you are introducing your product to a new friend. Who is it for, and what makes them happy?

**1.1 What problem does your product solve, in one sentence?**
`[FILL IN]`
Example: "People forget to drink water, so our app reminds them."

**1.2 Who is the customer?** (the person or company who uses or pays)
`[FILL IN]`
Example: "Adults aged 25 to 45 who want to be healthier."

**1.3 What type of product is this?**
`[PICK ONE: B2B (sells to companies) / B2C (sells to individuals) / Marketplace (two sides, such as buyers and sellers) / Other: ____ ]`

**1.4 How do customers pay?**
`[PICK ONE: Free / Free trial then paid / Monthly subscription / Yearly subscription / One-time purchase / Usage-based / Other: ____ ]`

**1.5 What is the "aha moment"?** This is the first moment a customer thinks, "This is useful!"
`[FILL IN]`
Example: "The user logs their first workout and sees their progress chart."

**1.6 How long should it take a new customer to reach the aha moment?**
`[FILL IN]` (Example: "Within 10 minutes of signing up")

**1.7 What does a "successful customer" look like?** Describe one customer who is clearly getting value.
`[FILL IN]`
Example: "Logs at least 3 workouts a week for 4 weeks in a row."

**1.8 What does a customer who is about to leave look like?**
`[FILL IN]`
Example: "Has not opened the app for 14 days, and complained about syncing."

**1.9 What does "churn" (leaving) mean for your product?**
`[PICK ONE: Cancels subscription / Stops logging in for ___ days / Does not renew / Deletes account / Other: ____ ]`

**1.10 What is the goal for the first 500 customers?** (Pick the goals that matter most and rank them 1 to 3.)

| Goal | Rank (1 = most important, blank if not used) |
|---|---|
| Customers stay (retention) | `[FILL IN]` |
| Customers use the main features (adoption) | `[FILL IN]` |
| Customers recommend us (referrals, NPS) | `[FILL IN]` |
| Customers pay more over time (expansion) | `[FILL IN]` |
| We learn what to build next (product learning) | `[FILL IN]` |

---

# 2. THE 6-PHASE JOURNEY: FROM BUILD TO 500 CUSTOMERS

> **Why this matters:** Health scoring means different things at different times. When you have 5 testers, you talk to each one. When you have 500 customers, you need an automatic score. This section defines what "health" means in each phase.
>
> **In plain words:** A video game has levels, and each level has different goals. Your product's journey also has levels. We decide the goal of each level before we start.

### 2.1 Phase map

| Phase | Name | Who uses the product | Customer count (suggested) | Main question we answer |
|---|---|---|---|---|
| 1 | **Build** | Nobody yet (the team builds) | 0 | "Are we building the right thing and tracking the right signals?" |
| 2 | **Internal Test** | Team and friendly insiders | 0 paying (5 to 20 testers) | "Does the product work, and does tracking work?" |
| 3 | **Beta** | Invited early users | 10 to 50 | "Do real people get value? What breaks?" |
| 4 | **Launch** | Public, first 30 days | 1 to 100 | "Do new customers reach the aha moment?" |
| 5 | **First 100** | Early customers | 1 to 100 | "Who stays, who leaves, and why?" |
| 6 | **First 500** | Growing customer base | 101 to 500 | "Can we score and support customers at scale?" |

**Adjust the customer counts if your numbers differ:**
`[FILL IN]` Example: "Beta = 25 customers. Launch begins when beta health average is above 70."

### 2.2 What to do in each phase (fill in the blanks)

#### Phase 1: Build
- Goal: Decide the signals and set up tracking **before** customers arrive.
- 🤖 AI can help: draft the event list, write tracking code, create the dashboard.
- 👤 Human must: approve which signals and weights are used.

| Question | Your answer |
|---|---|
| What tracking events must be built into the product? | `[FILL IN]` |
| Who builds the tracking? | `[FILL IN]` |
| What is the target date for tracking to be ready? | `[FILL IN]` |
| Exit rule: We move to Phase 2 when... | `[FILL IN]` (Example: "All events in Section 4 fire correctly in the test environment.") |

#### Phase 2: Internal Test
- Goal: Prove that the data is correct and the score calculates.
- Use **fake or test customers**. Check that the score matches what you expect by hand.

| Question | Your answer |
|---|---|
| How many test customers? | `[FILL IN]` |
| Who checks the score by hand? | `[FILL IN]` |
| Acceptable error between hand calculation and automatic score | `[FILL IN]` (Example: "0 points. They must match exactly.") |
| Exit rule: We move to Phase 3 when... | `[FILL IN]` |

#### Phase 3: Beta
- Goal: Learn from real people. Talk to every beta user.
- With under 50 users, the score is a **conversation starter, not a verdict**.

| Question | Your answer |
|---|---|
| How many beta users? | `[FILL IN]` |
| How will beta users be chosen? | `[FILL IN]` |
| How often will we personally contact each user? | `[FILL IN]` (Example: "Once a week by email or call.") |
| What do we want to learn? (3 questions) | `[FILL IN]` |
| Exit rule: We move to Phase 4 when... | `[FILL IN]` (Example: "At least 70% of beta users are Green or Yellow, and no Sev-1 bugs are open.") |

#### Phase 4: Launch (first 30 days public)
- Goal: Get new customers to the aha moment fast.
- The most important signal is **onboarding success**.

| Question | Your answer |
|---|---|
| Launch date | `[FILL IN]` |
| What share of new customers should reach the aha moment? | `[FILL IN]` (Example: "60% within 24 hours.") |
| Who watches the launch dashboard daily? | `[FILL IN]` |
| What is the "pause launch" rule? | `[FILL IN]` (Example: "If more than 30% of new customers are Red in week 1, stop marketing and fix.") |

#### Phase 5: First 100 customers
- Goal: Understand **why** customers stay or leave. Contact every Red customer personally.

| Question | Your answer |
|---|---|
| Do we contact every Red customer personally? | `[PICK ONE: Yes / No]` |
| How fast must we respond to a Red customer? | `[FILL IN]` (Example: "Within 1 business day.") |
| Target: share of customers Green at day 30 | `[FILL IN]` |
| Exit rule: We move to Phase 6 when... | `[FILL IN]` |

#### Phase 6: First 500 customers
- Goal: Make scoring automatic. Humans focus on the customers who need them most.
- By now you should have enough data to **check whether the score predicts leaving** (see Section 5.8). A common rule of thumb is to wait for roughly 20 to 30 customers who have actually left before trusting the weights.

| Question | Your answer |
|---|---|
| Which tasks become fully automatic? | `[FILL IN]` |
| Which tasks still need a human? | `[FILL IN]` |
| Target: 90-day retention | `[FILL IN]` |
| Done when... | `[FILL IN]` (Example: "500 customers, retention above 80%, score validated against churn.") |

---

# 3. CUSTOMER DEFINITION AND SEGMENTS ⚡ QUICK START

> **Why this matters:** A "healthy" customer for a tiny team is different from a "healthy" customer at a giant company. Group customers so you judge them fairly.
>
> **In plain words:** A kid who plays 1 hour a week and a kid who plays 10 hours a week may both be happy. Put similar customers in the same group so the score is fair.

**3.1 What is one "customer" in your product?**
`[PICK ONE: One person (user) / One company (account) / One team / One household / Other: ____ ]`

**3.2 Who gets a health score?**
`[PICK ONE: Every user / Every account (company) / Both, with account score built from user scores]`

**3.3 Customer segments** (groups that behave differently). Use at least one, at most five.

| Segment name | How to recognize it | Different expectations? |
|---|---|---|
| `[FILL IN]` (Example: "Free users") | `[FILL IN]` (Example: "No payment on file") | `[FILL IN]` (Example: "Lower usage is normal.") |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

**3.4 When does scoring start for a new customer?**
`[FILL IN]` Example: "Day 0 for onboarding score; full score after day 14."

**3.5 Which customers are NOT scored?** (testers, employees, spam, duplicates)
`[FILL IN]` Example: "Any email ending in @ourcompany.com and any account flagged as test."

---

# 4. HEALTH SIGNALS: WHAT WE MEASURE ⚡ QUICK START

> **Why this matters:** A signal is a measurable clue about customer happiness. You chose **four signal groups**: Usage, Feature Adoption, Feedback, and Support & Bugs. Define each one carefully so everyone measures the same thing.
>
> **In plain words:** A signal is a clue, like a doctor taking your temperature. We take four "temperatures" for each customer: how often they use us, which features they use, what they say, and what problems they have.

> **How to fill each signal:** Answer the five questions: **What? Where does the data come from? How often? What is healthy? What is risky?**

## 4.1 SIGNAL GROUP A: PRODUCT USAGE

**What it tells us:** Is the customer showing up?

| Question | Your answer |
|---|---|
| A1. What is the one "active" action? (what counts as using the product) | `[FILL IN]` (Example: "Logs a workout.") |
| A2. How do we measure usage? | `[PICK: Active days per week / Sessions per week / Minutes per week / Actions per week / Other]` |
| A3. Where does the data come from? | `[FILL IN]` (Example: "Product analytics tool, event `workout_logged`.") |
| A4. How often is it refreshed? | `[PICK: Real time / Daily / Weekly]` |
| A5. Time window | `[FILL IN]` (Example: "Last 14 days.") |
| A6. Do we also look at the **trend** (going up or down compared with before)? | `[PICK: Yes, compare with the previous 14 days (Recommended) / No]` |

**Scoring table for Usage** (give a 0 to 100 points for each level)

| Level | What it looks like | Points |
|---|---|---|
| 🟢 Healthy | `[FILL IN]` (Example: "4 or more active days per week") | 100 |
| 🟢 Good | `[FILL IN]` (Example: "2 to 3 active days per week") | 75 |
| 🟡 Watch | `[FILL IN]` (Example: "1 active day per week") | 40 |
| 🔴 Risk | `[FILL IN]` (Example: "No activity in 14 days") | 0 |

> **Tip: direction matters.** A customer who used the product 5 days last week but only 2 days this week is sending a warning, even though 2 days still looks "OK". Published guidance on health scores recommends looking at the **trend**, not only the raw amount. If you chose "Yes" in A6, write your trend rule here: `[FILL IN]` (Example: "Down 25% or more vs. previous period = move down one level.")

**Events that must be tracked** (the product must send these):

| Event name | When it fires | Built? (Y/N) | Tested? (Y/N) |
|---|---|---|---|
| `[FILL IN]` (Example: `signup_completed`) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` (Example: `first_login`) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` (Example: `core_action_done`) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 4.2 SIGNAL GROUP B: FEATURE ADOPTION

**What it tells us:** Is the customer using the features that make them stay?

| Question | Your answer |
|---|---|
| B1. List the **3 to 5 "sticky" features**. Customers who use these stay longer. | `[FILL IN]` (Example: "Progress chart, Reminders, Friend challenge.") |
| B2. How do you know these features are sticky? | `[PICK: We have data / It is our best guess / TBD]` |
| B3. Where does the data come from? | `[FILL IN]` |
| B4. Time window | `[FILL IN]` |

**Scoring table for Adoption**

| Level | What it looks like | Points |
|---|---|---|
| 🟢 Healthy | `[FILL IN]` (Example: "Uses 3 or more sticky features.") | 100 |
| 🟢 Good | `[FILL IN]` (Example: "Uses 2 sticky features.") | 70 |
| 🟡 Watch | `[FILL IN]` (Example: "Uses 1 sticky feature.") | 35 |
| 🔴 Risk | `[FILL IN]` (Example: "Uses none; only the basic screen.") | 0 |

**Onboarding milestones** (steps a new customer should finish)

| Step | Target time | Done by what share of customers? (goal) |
|---|---|---|
| `[FILL IN]` (Example: "Create profile") | `[FILL IN]` (Example: "Day 0") | `[FILL IN]` |
| `[FILL IN]` (Example: "Reach aha moment") | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 4.3 SIGNAL GROUP C: FEEDBACK SCORES

**What it tells us:** What do customers say about us?

**The three standard survey types (use the standard wording so your numbers can be compared):**

| Survey | Question to ask | Scale | How to read ONE answer | Group formula | When to ask |
|---|---|---|---|---|---|
| **NPS** | "How likely are you to recommend us to a friend or colleague?" | 0 to 10 | 9 to 10 = Promoter, 7 to 8 = Passive, 0 to 6 = Detractor | % Promoters minus % Detractors (result is -100 to +100) | Every so often, as a "relationship check" |
| **CSAT** | "How satisfied were you with [this experience]?" | 1 to 5 | 4 or 5 = satisfied | Satisfied answers divided by all answers, times 100 | Right after a support chat, purchase, or task |
| **CES** | "[Company] made it easy to solve my problem." | 1 to 7 (strongly disagree to strongly agree) | High = easy | Average rating, or % who found it easy | Right after something that takes effort |

> **Important:** One customer gives **one answer**. The health score uses that customer's **own answer** (for example, "this customer answered 9"). The NPS formula (Promoters minus Detractors) is only for a **group** of customers.

| Question | Your answer |
|---|---|
| C1. Which survey will you use? | `[PICK any: NPS (would you recommend us, 0-10) / CSAT (how satisfied, 1-5) / CES (how easy, 1-7) / Other]` |
| C2. When do we ask? | `[FILL IN]` (Example: "NPS at day 30, then every 90 days. CSAT after each support chat.") |
| C3. How do we ask? | `[PICK: In the app / Email / Both]` |
| C4. How do we limit survey fatigue? | `[FILL IN]` (Example: "Max one survey per customer per 30 days.") |
| C5. What if a customer does not answer? | `[PICK: Use "No data" rule from Section 5.5 / Count as neutral (50) / Other]` |

**Scoring table for Feedback**

| Level | What it looks like | Points |
|---|---|---|
| 🟢 Healthy | `[FILL IN]` (Example: "NPS 9 to 10, or CSAT 5") | 100 |
| 🟢 Good | `[FILL IN]` (Example: "NPS 7 to 8, or CSAT 4") | 70 |
| 🟡 Watch | `[FILL IN]` (Example: "NPS 5 to 6, or CSAT 3") | 35 |
| 🔴 Risk | `[FILL IN]` (Example: "NPS 0 to 4, or CSAT 1 to 2") | 0 |

> **Note:** The standard NPS method calls every answer from 0 to 6 a "Detractor". The table above splits detractors into Watch (5 to 6) and Risk (0 to 4) so you can tell the *mildly* unhappy from the *very* unhappy. You may keep or change this split.

**Free-text feedback** (comments, reviews, emails, chats): where do we collect it?
`[FILL IN]` Example: "In-app form, support inbox, app store reviews, user interviews."

## 4.4 SIGNAL GROUP D: SUPPORT AND BUGS

**What it tells us:** Is the customer struggling?

| Question | Your answer |
|---|---|
| D1. Where do support tickets live? | `[FILL IN]` (Example: "Help desk tool.") |
| D2. How do we rate bug severity? | `[FILL IN]` (Example: "Sev-1 = product unusable; Sev-2 = main feature broken; Sev-3 = small problem.") |
| D3. What is the target time to first reply? | `[FILL IN]` (Example: "Within 4 working hours.") |
| D4. What is the target time to fix? | `[FILL IN]` (Example: "Sev-1: 24 hours. Sev-2: 3 days. Sev-3: next release.") |
| D5. Time window | `[FILL IN]` |

**Scoring table for Support & Bugs**

| Level | What it looks like | Points |
|---|---|---|
| 🟢 Healthy | `[FILL IN]` (Example: "No open tickets, or all resolved within target.") | 100 |
| 🟢 Good | `[FILL IN]` (Example: "1 ticket, resolved, customer satisfied.") | 75 |
| 🟡 Watch | `[FILL IN]` (Example: "2 or more tickets in 30 days, or 1 unresolved past target.") | 35 |
| 🔴 Risk | `[FILL IN]` (Example: "Open Sev-1 or Sev-2 bug affecting this customer, or 3+ unresolved tickets.") | 0 |

## 4.5 Optional extra signals (Full Version only)

Only add a signal if you can answer: "Will this change what we do?" If not, skip it.

| Optional signal | Use it? | How it is measured |
|---|---|---|
| Payment failures or billing problems | `[Yes / No]` | `[FILL IN]` |
| Number of users in the account | `[Yes / No]` | `[FILL IN]` |
| Contact with our team (calls, emails answered) | `[Yes / No]` | `[FILL IN]` |
| Referrals made | `[Yes / No]` | `[FILL IN]` |
| Other: `[FILL IN]` | `[Yes / No]` | `[FILL IN]` |

---

# 5. THE SCORING MODEL ⚡ QUICK START

> **Why this matters:** This is the math. Do not worry: it is only multiplying and adding. A worked example is in 5.4.
>
> **In plain words:** Each clue gets points. Some clues matter more, so they get a bigger "weight". We add everything up to get one number from 0 to 100. High = happy. Low = needs help.

## 5.1 Weights: how important is each signal?

Weights must add up to **100**. Higher weight = more important. The starting suggestion is in the table.

| Signal | Suggested weight | **Your weight** |
|---|---|---|
| A. Product Usage | 35 | `[FILL IN]` |
| B. Feature Adoption | 25 | `[FILL IN]` |
| C. Feedback Scores | 20 | `[FILL IN]` |
| D. Support & Bugs | 20 | `[FILL IN]` |
| **Total** | **100** | **`[must equal 100]`** |

> **Be honest about the weights.** The suggested weights are a **starting guess**, not a fact. Published guidance on health scores says weights should be **tested against real customers who left**: signals that clearly separate customers who left from customers who stayed deserve more weight, and signals that do not should get little. You cannot do this test until you have customers who have actually left (see Section 5.8). Until then, write "starting guess, not yet tested" below.

**Is this weight tested against real churn yet?** `[PICK ONE: Not yet (starting guess) / Yes, tested on ___ customers who left]`

**Why did you choose these weights?** (one sentence)
`[FILL IN]` Example: "Usage predicts leaving best in similar products, so it gets the most weight."

**Different weights by phase?** (Optional)

| Phase | Usage | Adoption | Feedback | Support |
|---|---|---|---|---|
| 3 Beta | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 4 Launch | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 5 First 100 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 6 First 500 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 5.2 The formula

```
HEALTH SCORE = (Usage points   x Usage weight   / 100)
             + (Adoption points x Adoption weight / 100)
             + (Feedback points x Feedback weight / 100)
             + (Support points  x Support weight  / 100)
```

The result is a number from **0 to 100**.

## 5.3 Color bands: what does the score mean?

| Color | Score range | Meaning | **Your range** |
|---|---|---|---|
| 🟢 Green | 75 to 100 | Healthy. Keep them happy. | `[FILL IN]` |
| 🟡 Yellow | 50 to 74 | Watch closely. Needs attention soon. | `[FILL IN]` |
| 🔴 Red | 0 to 49 | At risk. Act now. | `[FILL IN]` |

> **Note on the limits (75 and 50):** These round numbers are a starting point so you can launch. Once you have enough data (Section 5.8), move the Red line to where **most customers who left actually scored**. Avoid keeping round numbers forever just because they look neat.

## 5.4 Worked example (use this to check your own math)

Customer "Sam" with the suggested weights:

| Signal | Sam's points | Weight | Calculation | Result |
|---|---|---|---|---|
| Usage | 75 | 35 | 75 x 35 / 100 | 26.25 |
| Adoption | 35 | 25 | 35 x 25 / 100 | 8.75 |
| Feedback | 70 | 20 | 70 x 20 / 100 | 14.00 |
| Support | 100 | 20 | 100 x 20 / 100 | 20.00 |
| **Health score** | | | | **69.0 = 🟡 Yellow** |

**Your own worked example** (needed for QA in Phase 2):

| Signal | Points | Weight | Calculation | Result |
|---|---|---|---|---|
| Usage | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Adoption | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Feedback | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Support | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| **Health score** | | | | `[FILL IN]` |

## 5.5 What if data is missing? (very important)

Customers will not always answer surveys. **Do not treat "no data" as zero.** Choose a rule:

`[PICK ONE]`
- **Option 1 (recommended): Re-balance.** Ignore the missing signal and spread its weight across the others. Mark the score "Low confidence."
- **Option 2: Neutral.** Give the missing signal 50 points.
- **Option 3: Other:** `[FILL IN]`

Example of Option 1: Feedback is missing. Add up the other three weights (80), then divide each by 80 and multiply by 100. The new weights are Usage 43.75, Adoption 31.25, Support 25.

**Confidence label:**

| Data available | Label |
|---|---|
| All 4 signals | High confidence |
| 3 of 4 | Medium confidence |
| 2 or fewer | Low confidence. Human review needed. |

## 5.6 Override rules (automatic Red flags)

Some events mean a customer is at risk **no matter what the score says**. Fill in your rules.

| Rule | Forces color to | Your version |
|---|---|---|
| Open Sev-1 bug for more than `[FILL IN]` hours | 🔴 Red | Example: "48 hours" |
| No activity for `[FILL IN]` days | 🔴 Red | Example: "21 days" |
| Customer asks to cancel or delete account | 🔴 Red | `[FILL IN]` |
| NPS 0 to 3 in last survey | 🔴 Red | `[FILL IN]` |
| Other: `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 5.7 Trend rule (direction matters)

A score of 70 that was 90 last month is worse than a 70 that was 50 last month.

| Question | Your answer |
|---|---|
| How far back do we compare? | `[FILL IN]` (Example: "14 days") |
| A drop of how many points raises an alert? | `[FILL IN]` (Example: "15 points or more") |
| What happens when the alert fires? | `[FILL IN]` (Example: "Customer moves down one color and goes on the Watch list.") |

## 5.8 Does the score actually work? (check from Phase 5 onward)

A health score is only useful if **low scores really lead to leaving**. Test it.

| Question | Your answer |
|---|---|
| When do we first test? | `[FILL IN]` (Example: "When at least 20 to 30 customers have left and we have their scores from before they left.") |
| How do we test? | Compare the average score of customers who **left** against those who **stayed**. If there is no clear gap, change the weights. |
| Who does the test? | `[FILL IN]` |
| What gap means "it works"? | `[FILL IN]` (Example: "Customers who left averaged at least 20 points lower.") |
| How often do we recheck? | `[FILL IN]` (Example: "At least twice a year, and after any big product change.") |

**The simple 2-by-2 test** (use a spreadsheet):

|  | Left (churned) | Stayed |
|---|---|---|
| **Low score before they left (Red)** | `[count]` (good: we saw it coming) | `[count]` (false alarm) |
| **High score (Green/Yellow)** | `[count]` (bad: we missed it) | `[count]` (good) |

If most of the customers who left were in the **low-score** row, your score is beating a coin flip. If they are spread evenly, change the weights.

**Your test results** (fill in each time you test):

| Date tested | Customers who left | How many were Red beforehand? | False alarms (Red but stayed) | Changes we made |
|---|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> **Caution for small numbers:** With fewer than about 20 to 30 customers who have left, test results can be mostly noise. Do not over-adjust the weights from a handful of cases. Use the score to decide **who to call**, not to make big business decisions. Treat the score as a **triage tool** (who needs attention first), not as an alarm that is always right. Also, keep a human note on important customers, because some warning signs (such as a worried tone on a call) never show up in the numbers.

---

# 6. DATA COLLECTION AND TOOLS

> **Where to find what:** This section says **which number comes from where**. Section 14 says **how to set up and connect each tool**. Fill in this section first.

> **Why this matters:** A score is only as good as its data. This section lists where every number comes from so nobody has to guess.
>
> **In plain words:** If a number is on the dashboard, anyone should be able to say exactly which tool it came from.

**6.1 Data source map**

| Signal | Tool or system | Who owns it | How the score system gets the data | Refresh rate |
|---|---|---|---|---|
| Usage | `[FILL IN]` | `[FILL IN]` | `[PICK: API / Export / Database / Manual]` | `[FILL IN]` |
| Adoption | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Feedback | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Support & bugs | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

**6.2 Where is the final score stored and shown?**

| Question | Your answer |
|---|---|
| Where does the score live? | `[PICK: Spreadsheet / Database / Customer success tool / Dashboard / Other]` |
| Who can see it? | `[FILL IN]` |
| How often is it recalculated? | `[PICK: Real time / Daily / Weekly]` |
| Do we keep score history? | `[PICK: Yes (how long: ___) / No]` |

**6.3 Customer identity matching**

Different tools may call the same customer by different names. How do we match them?
`[FILL IN]` Example: "By email address. The customer ID from the product is copied into the help desk."

**6.4 Data quality rules**

| Rule | Your answer |
|---|---|
| How do we remove test and employee data? | `[FILL IN]` |
| How do we handle duplicate customers? | `[FILL IN]` |
| Who fixes wrong data, and how fast? | `[FILL IN]` |

---

# 7. AI AGENT WORKFLOW AND AI GOVERNANCE (AI-DRIVEN DEVELOPMENT)

> **Why this matters:** AI agents can collect data, calculate scores, and flag risks around the clock. But AI makes mistakes, so humans must stay in charge of anything important. This section sets the rules.
>
> **In plain words:** AI is like a very fast helper who sometimes gets things wrong. We decide what the helper can do alone, what needs a grown-up to say yes, and what it must never do.

## 7.1 What can AI do in your project?

Tick what you want AI to do, and say who watches it.

| Task | AI does it? | Human checks? | Who is the human? |
|---|---|---|---|
| 🤖 Collect data from tools | `[ ]` | `[ ]` | `[FILL IN]` |
| 🤖 Calculate health scores | `[ ]` | `[ ]` | `[FILL IN]` |
| 🤖 Flag at-risk customers | `[ ]` | `[ ]` | `[FILL IN]` |
| 🤖 Summarize customer feedback into themes | `[ ]` | `[ ]` | `[FILL IN]` |
| 🤖 Draft messages to customers | `[ ]` | `[ ]` | `[FILL IN]` |
| 🤖 Suggest product improvements | `[ ]` | `[ ]` | `[FILL IN]` |
| 🤖 Write and test tracking code | `[ ]` | `[ ]` | `[FILL IN]` |

## 7.2 The AI agents (one row per agent)

| Agent name | Its one job | What it reads (inputs) | What it produces (outputs) | How often it runs |
|---|---|---|---|---|
| Data Collector | Pull signal data from each tool | `[FILL IN]` | A clean data table | `[FILL IN]` |
| Scorer | Calculate score using Section 5 | Data table | Score, color, confidence | `[FILL IN]` |
| Risk Flagger | Find Red customers and big drops | Scores and history | Alert list with reasons | `[FILL IN]` |
| Feedback Summarizer | Group comments into themes | Comments, tickets, reviews | Top themes with counts | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 7.3 Human-in-the-loop rules (MUST FILL IN)

This is the most important part of the AI section.

**AI may do ALONE (no approval needed):**
`[FILL IN]`
Example: "Read data, calculate scores, create internal reports, tag feedback themes."

**AI must ASK A HUMAN FIRST:**
`[FILL IN]`
Example: "Send any message to a customer, change a customer's plan, change score weights, delete any data, change product code in production."

**AI must NEVER do:**
`[FILL IN]`
Example: "Share one customer's data with another, guess missing data without saying so, contact customers in Red without approval, process data the customer did not agree to."

| Question | Your answer |
|---|---|
| Who approves AI actions that need approval? | `[FILL IN]` |
| How fast must they respond? | `[FILL IN]` |
| What happens if nobody responds? | `[FILL IN]` (Example: "The action waits. AI does not proceed.") |
| Where are AI actions recorded (audit log)? | `[FILL IN]` |
| When AI chats with or writes to customers, do we tell them it is AI? | `[PICK: Yes, always (Recommended) / Only when asked / No]`. Where is this shown? `[FILL IN]` (See Section 13.4: some laws now require this.) |
| Is every AI-drafted customer message reviewed by a person before sending? | `[PICK: Yes, always / Only for Red customers / No]` |

## 7.4 AI quality checks

| Check | How often | Who |
|---|---|---|
| Compare 10 random AI scores against hand calculation | `[FILL IN]` | `[FILL IN]` |
| Read 20 random AI feedback summaries against the original comments | `[FILL IN]` | `[FILL IN]` |
| Check AI alerts: how many were real problems vs. false alarms? | `[FILL IN]` | `[FILL IN]` |
| Review the AI audit log | `[FILL IN]` | `[FILL IN]` |

**Acceptable AI accuracy:** `[FILL IN]` Example: "Scores must match hand calculation 100%. At least 8 out of 10 alerts must be real problems."

**What happens when AI gets it wrong?** `[FILL IN]` Example: "Switch that agent to manual mode, fix the cause, re-test before turning it back on."

## 7.5 Instruction template for an AI agent

Copy this block, fill it in, and give it to the AI agent. Clear instructions mean fewer mistakes.

```
ROLE:        You are the [agent name] for [project name].
GOAL:        [one sentence: what success looks like]
INPUTS:      [the data you may read]
RULES:       Follow Section 5 of Customer_Health_Scoring.md exactly.
             If data is missing, apply the rule in Section 5.5.
             If you are not sure, say "I am not sure" and ask a human.
OUTPUT:      [exact format, e.g., a table with: customer, score, color, confidence, reason]
MUST ASK A HUMAN BEFORE: [list from Section 7.3]
MUST NEVER: [list from Section 7.3]
```

## 7.6 AI governance: keep the AI safe and accountable

> **In plain words:** Before you trust a helper, you write down who is in charge of it, what it can touch, how you check its work, and how you stop it fast if it goes wrong. This follows the four ideas in the US NIST AI Risk Management Framework: **Govern, Map, Measure, Manage**.

### Govern: who is in charge?

| Question | Your answer |
|---|---|
| Who is the named owner of each AI agent? | `[FILL IN]` |
| Who is allowed to change an agent's instructions or the score weights? | `[FILL IN]` |
| What is the process to approve a **new** AI use (who says yes)? | `[FILL IN]` |
| What is the written limit on AI risk we accept? | `[FILL IN]` (Example: "AI may never contact a customer without approval.") |

### Map: what does each agent touch?

| Agent | What data it reads | What it writes or sends | Who could be affected | What could go wrong |
|---|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

### Measure: is it working, or drifting?

| Measure | What it means | Our target |
|---|---|---|
| Error rate | How often the AI output is wrong when a person checks it | `[FILL IN]` |
| Override rate | How often a human has to change what the AI did. A rising number means trouble. | `[FILL IN]` |
| False alarm rate | Alerts that were not real problems | `[FILL IN]` |
| Consistency | Give the same input twice. Do we get the same answer? | `[FILL IN]` |
| Tested on OUR data? | Test with our own customers' data, not only sample data | `[PICK: Yes / No]` |

### Manage: what do we do when something goes wrong?

| Question | Your answer |
|---|---|
| What number makes us **pause** the agent? | `[FILL IN]` (Example: "Override rate above 20%, or any wrong message sent to a customer.") |
| Who can press pause, and how? | `[FILL IN]` |
| Who is told, and how fast? | `[FILL IN]` |
| What must the audit log record? | What data was read, what the AI produced, who approved it, and when. (A bare score is **not** enough to reconstruct what happened.) |
| Practice drill: "Pretend the AI sent a wrong message. Can we find out exactly what happened?" | Done on `[FILL IN]` (do once before Beta, again before 500 customers) |

---

# 8. ACTION PLAYBOOKS: WHAT DO WE DO?

> **Why this matters:** A score nobody acts on is useless. For each color, decide the exact action, the owner, and the deadline.
>
> **In plain words:** A smoke alarm is only useful if someone comes when it rings. Decide who comes, and how fast.

## 8.1 🔴 RED customer (score below Red limit, or an override rule fired)

| Question | Your answer |
|---|---|
| Who is told? | `[FILL IN]` |
| How fast? | `[FILL IN]` (Example: "Same business day.") |
| First action | `[FILL IN]` (Example: "A person calls or emails to ask what is wrong.") |
| What do we find out? | `[FILL IN]` (Example: "Is it a bug, confusion, wrong fit, or price?") |
| Who can offer help (discount, extra training, a fix)? | `[FILL IN]` |
| When do we check again? | `[FILL IN]` |
| When do we give up and mark as churned? | `[FILL IN]` |
| After they leave: do we ask why? | `[PICK: Yes, with a short exit survey / No]` |

## 8.2 🟡 YELLOW customer

| Question | Your answer |
|---|---|
| Who is told? | `[FILL IN]` |
| First action | `[FILL IN]` (Example: "Send a helpful tip about an unused feature.") |
| Which signal is weakest? Offer help for that one | `[FILL IN]` (Example: "Low adoption: send a 2-minute tutorial video.") |
| When do we check again? | `[FILL IN]` |
| When does Yellow become Red? | `[FILL IN]` (Example: "No improvement after 14 days.") |

## 8.3 🟢 GREEN customer

| Question | Your answer |
|---|---|
| Action | `[FILL IN]` (Example: "Ask for a review or referral. Invite to share feedback.") |
| When is it OK to ask for a review or referral? | `[FILL IN]` (Example: "Only if Green for 30 days and NPS 9 or 10.") |
| Do we offer upgrades or extra features? | `[PICK: Yes / No]` |
| How do we thank them? | `[FILL IN]` |

## 8.4 New customer onboarding (first 14 days)

| Day | What we do | Owner | Done by AI or human? |
|---|---|---|---|
| Day 0 | `[FILL IN]` (Example: "Welcome message.") | `[FILL IN]` | `[FILL IN]` |
| Day 1 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Day 3 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Day 7 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Day 14 | `[FILL IN]` (Example: "First score review.") | `[FILL IN]` | `[FILL IN]` |

## 8.5 Message rules

| Question | Your answer |
|---|---|
| Who may send customer messages? | `[FILL IN]` |
| Tone of voice | `[FILL IN]` (Example: "Friendly, short, no jargon.") |
| Do we say "your health score is low" to customers? | `[PICK: Never / Only if they ask]` (Recommended: never say this. Say "We noticed you may need help with...") |
| How many messages per week at most? | `[FILL IN]` |

## 8.6 When customers leave: exit survey, churn log and win-back

> **In plain words:** Some customers will leave, and that is normal. What matters is that we find out **why**, check whether our score warned us, and decide whether to invite them back politely.

**Recap:** Our definition of "churn" is in Section 1.9. Write it here again so this section stands alone: `[FILL IN]`

### Exit survey (keep it very short: 2 to 4 questions)

| Question | Your answer |
|---|---|
| When is the exit survey sent? | `[FILL IN]` (Example: "Right after cancellation, and once only.") |
| How is it sent? | `[PICK: In the cancel flow / Email / Both]` |
| Is it optional? | `[PICK: Yes (Recommended) / No]` |
| Who reads the answers? | `[FILL IN]` |
| Question 1: "What is the main reason you are leaving?" Choices | `[FILL IN]` (Example: "Too expensive / Missing a feature / Hard to use / Bugs or problems / Found something else / I no longer need it / Support experience / Other") |
| Question 2: "What could we have done to keep you?" (free text) | `[FILL IN]` |
| Question 3: "Would you consider coming back in the future?" (Yes / Maybe / No) | `[FILL IN]` |
| Question 4: "May we contact you about this?" (Yes / No) | `[FILL IN]` |

### Churn log (one row per customer who leaves)

| Date left | Customer ID | Last score and color | Days between turning Red and leaving | Main reason | Was it preventable? (Y/N) | Feedback tag (Section 9.2) | What we learned |
|---|---|---|---|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> **Why we log "days between Red and leaving":** If most customers turned Red only 2 days before leaving, we are warned too late. If they turned Red 3 weeks before, we have time to help. Use this to decide how fast the playbook in 8.1 must be.

### How we measure churn

```
CHURN RATE     = (customers lost in the period / customers at the start of the period) x 100
RETENTION RATE = 100 - churn rate
```

| Question | Your answer |
|---|---|
| Which period do we measure? | `[PICK: Month / Quarter]` |
| Our target churn rate | `[FILL IN]` |
| Do we separate **voluntary** churn (customer chose to leave) from **involuntary** churn (payment failed, card expired)? | `[PICK: Yes (Recommended) / No]` |
| Who reviews the top three leaving reasons, and when? | `[FILL IN]` (Example: "Product owner, at every roadmap review in Section 9.4.") |

### Win-back (inviting people back)

| Question | Your answer |
|---|---|
| Do we try to win customers back? | `[PICK: Yes / No]` |
| When do we contact them? | `[FILL IN]` (Example: "After we ship a fix for the reason they gave, or 60 days after they left.") |
| Who may contact them? | `[FILL IN]` |
| What may we offer? | `[FILL IN]` (Example: "A free month, or an update about the feature they wanted.") |
| How many attempts at most? | `[FILL IN]` (Example: "2, then stop.") |
| How do we respect "do not contact" and legal rules? | `[FILL IN]` (See Section 13.4 on marketing messages. Honor every unsubscribe request.) |
| When do we delete the data of customers who left and did not return? | `[FILL IN]` (Must match Section 13.1.) |

---

# 9. FEEDBACK-TO-ROADMAP LOOP

> **Why this matters:** The goal is not only keeping customers. It is also **learning what to build next**. This section turns what customers tell you into product improvements.
>
> **In plain words:** Customers tell us what is broken and what they wish for. We collect it, sort it, pick the most important ideas, build them, and tell customers.

```
 Customer feedback and health data
              |
              v
   1. COLLECT  -->  2. TAG  -->  3. COUNT  -->  4. DECIDE  -->  5. BUILD  -->  6. TELL CUSTOMERS  -->  7. MEASURE
                                                                                                          |
                                                                          (did health improve?) <---------+
```

## 9.1 Collect
List every place feedback arrives: `[FILL IN]`
Example: "Support tickets, in-app form, surveys, app store reviews, sales calls, social media."

## 9.2 Tag (give each piece of feedback a label)

Use the same labels everywhere. Starting list (edit it):

| Tag type | Options |
|---|---|
| **Kind** | Bug / Feature request / Confusing / Praise / Pricing / Other |
| **Area** | `[FILL IN]` (Example: Sign-up, Dashboard, Reminders, Payments) |
| **Severity** | Blocker / Painful / Annoying / Nice-to-have |
| **Customer color** | 🟢 / 🟡 / 🔴 |
| **Segment** | From Section 3.3 |

Who tags? `[PICK: AI suggests, human confirms / Human only / AI only]`

## 9.3 Count and rank (a simple priority score)

```
PRIORITY = (How many customers asked)
         x (How badly it hurts: Blocker 4, Painful 3, Annoying 2, Nice-to-have 1)
         x (Extra weight if the customers are Red or Yellow: Red 2, Yellow 1.5, Green 1)
         / (Effort to build: Small 1, Medium 2, Large 3)
```

Do you want to change the formula? `[FILL IN or write "No"]`

## 9.4 Decide

| Question | Your answer |
|---|---|
| How often do we hold the roadmap review? | `[FILL IN]` (Example: "Every 2 weeks.") |
| Who attends? | `[FILL IN]` |
| Who makes the final call? | `[FILL IN]` |
| How many items can we commit to per cycle? | `[FILL IN]` |
| What feedback do we say "no" to? | `[FILL IN]` (Example: "Requests from only one customer, unless they are a blocker.") |

## 9.5 Close the loop

| Question | Your answer |
|---|---|
| How do we tell customers their idea was built? | `[FILL IN]` (Example: "Personal email plus release notes.") |
| How do we tell customers an idea was NOT chosen? | `[FILL IN]` |
| How long should we take to reply to feedback? | `[FILL IN]` |

## 9.6 Measure the result

After shipping a fix or feature, did it help?

| Question | Your answer |
|---|---|
| What number should improve? | `[FILL IN]` (Example: "Adoption of Reminders; fewer tickets about syncing.") |
| How long do we wait before checking? | `[FILL IN]` |
| Who checks? | `[FILL IN]` |

---

# 10. ROLES, OWNERS AND RHYTHM (RACI)

> **How to read RACI:** **R** = Responsible (does the work). **A** = Accountable (final say; only one person per row). **C** = Consulted (asked for input). **I** = Informed (told the result).

## 10.1 Who does what

| Activity | Product owner | Engineering | Customer success / Support | QA | AI agent | Names |
|---|---|---|---|---|---|---|
| Choose signals and weights | A | C | R | I | C | `[FILL IN]` |
| Build tracking events | C | A/R | I | C | R | `[FILL IN]` |
| Calculate scores | I | C | I | C | A/R | `[FILL IN]` |
| Review Red customers | I | I | A/R | I | C | `[FILL IN]` |
| Contact customers | I | I | A/R | I | C (draft only) | `[FILL IN]` |
| Tag and summarize feedback | C | I | A | I | R | `[FILL IN]` |
| Decide roadmap | A/R | C | C | I | C | `[FILL IN]` |
| Test scoring accuracy | I | C | I | A/R | C | `[FILL IN]` |
| Update this document | A/R | C | C | C | C | `[FILL IN]` |

Edit letters if your team works differently. **Every row must have exactly one A.**

## 10.2 Meeting and report rhythm

| Meeting or report | How often | Who attends | What we decide |
|---|---|---|---|
| Daily health check | `[FILL IN]` (Suggested: daily in Phases 4 to 5) | `[FILL IN]` | Who needs a call today? |
| Weekly health review | `[FILL IN]` (Suggested: weekly) | `[FILL IN]` | Trends, Red list, actions |
| Roadmap review | `[FILL IN]` (Suggested: every 2 weeks) | `[FILL IN]` | What to build next |
| Phase-gate review | End of each phase | Everyone | Move on to the next phase? |
| Score accuracy review | `[FILL IN]` (Suggested: quarterly) | `[FILL IN]` | Change weights? |

## 10.3 Escalation: who do we tell when things go wrong?

| Situation | Tell this person | Within |
|---|---|---|
| Many customers turn Red at once | `[FILL IN]` | `[FILL IN]` |
| Score system is broken or wrong | `[FILL IN]` | `[FILL IN]` |
| Customer complains publicly | `[FILL IN]` | `[FILL IN]` |
| AI sent something it should not have | `[FILL IN]` | `[FILL IN]` |
| Customer data leak suspected | `[FILL IN]` | Immediately |

---

# 11. REPORTING AND DASHBOARD

**11.1 Main numbers to show** (tick what you want)

- `[ ]` Number of customers now
- `[ ]` Share of customers: Green / Yellow / Red
- `[ ]` Average health score
- `[ ]` Customers who changed color this week
- `[ ]` New customers who reached the aha moment
- `[ ]` Retention at day 30 / 60 / 90
- `[ ]` Average NPS or CSAT
- `[ ]` Open Sev-1 / Sev-2 bugs
- `[ ]` Top 5 feedback themes
- `[ ]` Progress toward 500 customers
- `[ ]` Other: `[FILL IN]`

**11.2 Who reads the report, and how do they receive it?**

| Reader | How often | Format (email, dashboard, chat) |
|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

**11.3 Progress tracker toward 500 customers**

| Milestone | Target date | Actual date | Green share at that point |
|---|---|---|---|
| First customer | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 10 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 50 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 100 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 250 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 500 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

---

# 12. QA AND LAUNCH CHECKLIST (PHASE GATES)

> **How to use:** Do not move to the next phase until every box for the current phase is `[x]` or has a written reason and a person responsible. This is your safety net.

### Gate 1: Ready to leave Build (Phase 1 to 2)
- `[ ]` Sections 0 to 5 completed with no `[FILL IN]` left
- `[ ]` Weights add up to 100
- `[ ]` All tracking events in Section 4 are built
- `[ ]` Data source map (Section 6) completed
- `[ ]` Legal and privacy review (Section 13) signed off, **before any real customer data is collected**
- `[ ]` Tools chosen, accounts created, access list done (Section 14)
- `[ ]` Budget approved and timeline agreed (Section 15)
- `[ ]` Human-in-the-loop rules (Section 7.3) approved

### Gate 2: Ready to leave Internal Test (Phase 2 to 3)
- `[ ]` Worked example (5.4) matches the automatic score exactly
- `[ ]` Every tracking event tested and firing once, not twice
- `[ ]` Missing data rule (5.5) tested with a customer who has no survey answer
- `[ ]` Override rules (5.6) tested
- `[ ]` Test and employee accounts are excluded
- `[ ]` Red alert reaches the right person
- `[ ]` Dashboard shows correct numbers
- `[ ]` AI agents pass the quality checks in 7.4
- `[ ]` AI pause button tested, and the "wrong message" drill in 7.6 completed
- `[ ]` Audit log shows what data was read, what was produced, who approved it, and when
- `[ ]` Customers are told when they are dealing with AI (if applicable, Section 13.4)
- `[ ]` Integration tests in Section 14.6 all passed

### Gate 3: Ready to leave Beta (Phase 3 to 4)
- `[ ]` Every beta user has been spoken to at least once
- `[ ]` Scores compared against what we learned from the conversations (do they feel right?)
- `[ ]` Top 3 beta problems fixed or scheduled
- `[ ]` No open Sev-1 bugs
- `[ ]` Support process tested with real tickets
- `[ ]` Survey sent and answers recorded correctly
- `[ ]` Playbooks (Section 8) tried at least once

### Gate 4: Ready to leave Launch (Phase 4 to 5)
- `[ ]` Aha-moment target reached (Section 2.2)
- `[ ]` Daily health check run for 30 days
- `[ ]` Every Red customer contacted in time
- `[ ]` Feedback tags are in use and consistent
- `[ ]` First roadmap review held

### Gate 5: Ready to leave First 100 (Phase 5 to 6)
- `[ ]` Score tested against who left and who stayed (5.8)
- `[ ]` Exit survey running and churn log filled in (8.6)
- `[ ]` Weights adjusted if needed, and the change recorded in the Change Log
- `[ ]` Feedback loop closed at least once (feature or fix shipped from customer feedback)
- `[ ]` Decision made about which tasks to automate more (7.1)
- `[ ]` Support load manageable for the team

### Gate 6: Done at First 500 (Phase 6 complete)
- `[ ]` 500 customers reached
- `[ ]` Retention target met (Section 2.2)
- `[ ]` Score accuracy reviewed and documented
- `[ ]` Lessons learned written down (Section 16)
- `[ ]` Actual spend and timeline compared with plan (Section 15)
- `[ ]` Legal and privacy review re-checked (Section 13.9)
- `[ ]` Next goal decided (Example: 5,000 customers)

---

# 13. PRIVACY, LEGAL AND COMPLIANCE

> **Why this matters:** You are collecting and analyzing data about real people, and in some places the law has rules about scoring people and using AI. Doing this early prevents expensive fixes later.
>
> **In plain words:** Be careful with people's information, be honest about what you do with it, and make sure a real person is in charge of decisions that affect customers.

> **This is not legal advice.** The summaries below were checked in October 2026 against published articles (see Appendix D) and the law keeps changing. Fill in what you can, then ask a qualified lawyer or privacy expert to confirm. Do this **before** collecting real customer data (before Beta).

## 13.1 What data do we collect? (data inventory)

| Data item | Is it personal data? (Y/N) | Why do we collect it? | Where is it stored? | Who can see it? | How long do we keep it? |
|---|---|---|---|---|---|
| Name and email | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Usage events (logins, actions) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Feature use | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Survey answers (NPS, CSAT, CES) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Support tickets and chats | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Free-text comments and reviews | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| The health score itself | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Other: `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> **Rule of thumb (data minimization):** If you cannot say why you need a piece of data, **do not collect it.**

## 13.2 Where do our customers live? (tick every place)

Tick where your **customers** live, not where your company is. The rules follow the customer.

- `[ ]` European Union / European Economic Area
- `[ ]` United Kingdom
- `[ ]` California
- `[ ]` Other US states: `[FILL IN]`
- `[ ]` Canada
- `[ ]` Australia / New Zealand
- `[ ]` Brazil
- `[ ]` India
- `[ ]` Other: `[FILL IN]`

## 13.3 The "STOP and ask a lawyer" test

Answer each question **Yes** or **No**.

| Question | Yes / No |
|---|---|
| Does the score (alone, with no person checking) automatically decide anything that seriously affects a person? Examples: whether they get a loan, housing, a school place, a job, or health care | `[FILL IN]` |
| Does the score automatically cancel, refuse, restrict, or change the price for a customer? | `[FILL IN]` |
| Do we use sensitive data? Examples: health, biometrics, race, religion, exact location, financial account details | `[FILL IN]` |
| Do we use AI to read emotions in voice, video, or text? | `[FILL IN]` |
| Are any customers children? (Age limits differ by place. Check yours.) | `[FILL IN]` |
| Do we sell or share customer data with other companies? | `[FILL IN]` |
| Do AI chatbots or AI agents talk directly to customers? | `[FILL IN]` |

**If ANY answer is "Yes", STOP. Get legal advice before launching.**

> **Our recommended design rule (write it in your own words in Section 7.3 too):**
> *The health score only helps a human decide **who to contact and when**. It never automatically cancels, denies, reprices, or restricts anyone.*
> This keeps most projects away from the strictest rules below.

## 13.4 Rules snapshot (plain words)

| Rule | What it says (checked October 2026) | Does it apply to us? | What we do about it |
|---|---|---|---|
| **GDPR Article 22** (EU, and similar rules in the UK) | Decisions made **only** by software that have legal or similarly significant effects on a person are restricted. Exceptions exist (needed for a contract, allowed by law, or the person gives clear consent). People can ask for a human to review, give their view, and challenge the decision. Human review must be **real**: the person must have the power and information to change the result, not just click "OK". | `[Yes / No / Not sure]` | `[FILL IN]` |
| **Other general privacy duties** (GDPR and similar laws) | In general: have a lawful reason for using data, tell people what you do, collect only what you need, delete it when done, let people see or delete their data, sign contracts with vendors who handle data, and do a risk assessment for risky profiling. *(General summary. Confirm with counsel.)* | `[Yes / No / Not sure]` | `[FILL IN]` |
| **California CCPA / CPRA: automated decision-making rules** | The updated regulations took effect 1 January 2026. Software used to make "significant decisions" (finance or lending, housing, education, jobs, health care) must comply by **1 January 2027**: advance notice, a way to opt out (with some exceptions), the right to ask how it works, and a human-review appeal. Risk assessments are also required in some cases. A score used only to decide who gets outreach normally falls outside "significant decisions", but **confirm this**. | `[Yes / No / Not sure]` | `[FILL IN]` |
| **EU AI Act: Article 50 transparency** | Since **2 August 2026**, AI systems that talk directly with people (chatbots, voice assistants, AI agents) must tell people they are dealing with AI, unless that is obvious. If you use emotion recognition, you must inform the people affected. Marking of AI-generated content for systems already on the market is due **2 December 2026**. Fines can reach 15 million euros or 3% of worldwide yearly turnover, whichever is higher. *(We could not confirm whether any later EU changes moved these dates. Check.)* | `[Yes / No / Not sure]` | `[FILL IN]` |
| **Marketing messages** (email, text, calls) | Most places require permission and an easy way to unsubscribe. Examples: CAN-SPAM, CASL, ePrivacy, TCPA. *(General summary. Confirm with counsel.)* | `[Yes / No / Not sure]` | `[FILL IN]` |
| **Children's privacy** | Extra rules usually apply to children's data. | `[Yes / No / Not sure]` | `[FILL IN]` |
| **Industry rules** (health, finance, education, and so on) | Your industry may have its own rules. | `[Yes / No / Not sure]` | `[FILL IN]` |
| Other: `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 13.5 Telling customers, and honoring their rights

| Question | Your answer |
|---|---|
| Where is our privacy notice? (link) | `[FILL IN]` |
| Does it say, in plain words, that we look at usage, feedback, and support history to understand customer needs? | `[PICK: Yes / No, we must add it]` |
| Where do customers agree or consent (if needed)? | `[FILL IN]` |
| How can a customer ask to **see** their data? | `[FILL IN]` |
| How can a customer ask to **delete** their data? | `[FILL IN]` |
| How can a customer **correct** wrong data? | `[FILL IN]` |
| How can a customer **opt out** of scoring or ask for a **human review**? | `[FILL IN]` |
| Who handles these requests? | `[FILL IN]` |
| How fast must we reply? | `[FILL IN]` (Many laws set a deadline of roughly 30 to 45 days. Confirm yours.) |
| How do we prove who is asking? | `[FILL IN]` |
| When someone asks us to delete, how do we also remove them from scores, AI memory, and backups? | `[FILL IN]` |

**Sample notice wording (edit with your lawyer):**

> "We look at how you use our product, which features you try, your survey answers, and your support history. We use this to understand whether you need help and to improve our product. A person reviews this information before we contact you. We do not use it to automatically cancel your account or change your price. You can ask to see, correct, or delete your information at any time by contacting [email]."

## 13.6 AI tools and vendors that touch customer data

| AI tool or vendor | What customer data does it see? | Contract (DPA) signed? | Does the vendor use our data to train its models? (we want "No") | Where is data processed? | Can we delete the data? | Approved by |
|---|---|---|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[FILL IN]` |

| Question | Your answer |
|---|---|
| How do we remove personal details (names, emails, phone numbers) from comments **before** AI reads them? | `[FILL IN]` |
| Can AI see the full customer record, or only what it needs? | `[FILL IN]` |
| Do we tell customers when AI is used with their data? | `[FILL IN]` |

## 13.7 Security basics

| Item | Your answer |
|---|---|
| Who can see individual customer scores and data? (least access needed) | `[FILL IN]` |
| Is data protected while stored and while sent (encryption)? | `[PICK: Yes / No / Not sure]` |
| Do all team members use two-step login (MFA) on tools holding customer data? | `[PICK: Yes / No]` |
| Where are passwords and API keys stored? (name the tool, **never write the secret here**) | `[FILL IN]` |
| How do we remove access when someone leaves the team? | `[FILL IN]` |
| Are backups made, and who can restore them? | `[FILL IN]` |
| Retention: when do we delete old data? | `[FILL IN]` |
| **Data breach plan:** who is told, and within how many hours? | `[FILL IN]` (Some laws require telling authorities within a set time. Confirm yours.) |

## 13.8 Fairness check

A score can accidentally treat groups of customers unfairly. Check it.

| Question | Your answer |
|---|---|
| Do we compare the share of Red customers across segments (new vs. old, region, plan, language)? | `[FILL IN]` |
| Could a language or writing style make AI read a comment as "negative" when it is not? | `[FILL IN]` |
| Can a person override a score they believe is wrong? | `[PICK: Yes / No]` (Recommended: yes) |
| Who reviews fairness, and how often? | `[FILL IN]` |

## 13.9 Legal review sign-off

| Reviewer (name and role) | Date | Regions covered | Conditions or changes required | Next re-check (every 6 months) |
|---|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

---

# 14. TOOLS AND INTEGRATION SETUP

> **Why this matters:** Every number in the score comes from a tool. If tools are not connected or tested, the score will be wrong or empty.
>
> **In plain words:** Decide which apps hold which information, connect them so they can talk to each other, and test that the information arrives correctly.

## 14.1 Keep the tools as simple as the phase needs

| Phase | A good-enough setup | Upgrade when... |
|---|---|---|
| 1 Build, 2 Internal Test | Spreadsheet plus exports from each tool | You are tired of copying numbers by hand |
| 3 Beta | Spreadsheet plus the analytics, survey, and help desk tools already chosen | Collecting data takes more than `[FILL IN]` hours per week |
| 4 Launch, 5 First 100 | Automatic data collection into one place (database or sheet) plus alerts | You can no longer review every customer by hand |
| 6 First 500 | A proper dashboard and, if needed, a customer success platform | The team spends more time on the tool than on customers |

> **Rule:** Pick the simplest tool that works. You can upgrade later. Do not buy an expensive platform before you know which signals matter.

## 14.2 Tool register (one row per job)

The "Example tools" column lists well-known options **only as examples**, not recommendations. Check current features and pricing before choosing.

| Job | Example tools | Tool we chose | Admin (name) | Plan and monthly cost | Customer data it holds | Connected? | Tested? |
|---|---|---|---|---|---|---|---|
| Product usage analytics | Amplitude, Mixpanel, PostHog, Google Analytics | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| Help desk and support | Zendesk, Freshdesk, Intercom, Help Scout | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| Surveys (NPS, CSAT, CES) | Typeform, SurveyMonkey, in-app survey | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| Bug tracker | Jira, Linear, GitHub Issues | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| Customer records / CRM / customer success | HubSpot, Salesforce, Gainsight, ChurnZero | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| Where the data and scores are stored | Google Sheets, Airtable, Supabase, BigQuery, Snowflake | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| Messages to customers | Customer.io, Mailchimp, in-app messages | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| Team alerts | Slack, Microsoft Teams, email | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| Dashboards | Looker Studio, Metabase, Power BI, Tableau | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |
| AI service for agents | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[Y/N]` | `[Y/N]` |

## 14.3 Setup checklist (repeat for every tool)

For each tool, tick these steps. Make a copy of this list for each tool.

Tool name: `[FILL IN]`

- `[ ]` Account created with a **company** email, not a personal one
- `[ ]` At least **two** people have admin access (so one person leaving does not lock the team out)
- `[ ]` Only the data we need is switched on (see Section 13.1)
- `[ ]` Test accounts and team members are marked so they are excluded from scores (Section 3.5)
- `[ ]` The tool is connected to the data store (API, export, or automatic sync)
- `[ ]` The **customer ID** is passed along so records match across tools (Section 14.4)
- `[ ]` A test customer was sent through and the data showed up correctly
- `[ ]` An alert fires if the connection breaks (Example: "No data for 24 hours")
- `[ ]` Where the login and keys are stored is written down (name the password manager, not the password)
- `[ ]` Data retention and deletion settings match Section 13

## 14.4 Customer ID map (how to match the same customer across tools)

Pick one "master key" (usually a customer ID created by your product). Then fill in what each tool calls it.

| Tool | Name of the field | Example value | How it is filled in |
|---|---|---|---|
| Product database (master) | `[FILL IN]` (Example: `customer_id`) | `[FILL IN]` | Created at sign-up |
| Analytics | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Help desk | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Survey tool | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| CRM / customer success | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Data store / dashboard | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 14.5 How the data flows (draw or edit)

```
 PRODUCT        HELP DESK       SURVEYS       BUG TRACKER
 (usage,        (tickets)       (NPS,         (severity,
  features)                      CSAT, CES)    status)
     |              |              |              |
     +--------------+------+-------+--------------+
                           |
                           v
                  DATA STORE (one place, matched by customer ID)
                           |
                           v
             AI "Data Collector" -> AI "Scorer" -> AI "Risk Flagger"
                           |
                           v
        DASHBOARD  +  ALERTS  ->  HUMAN reviews  ->  PLAYBOOK action (Section 8)
```

If your flow is different, redraw it here: `[FILL IN]`

## 14.6 Integration tests (do these in Phase 2 before any real customer)

| # | Test | What should happen | Result (pass/fail) | Date | Tester |
|---|---|---|---|---|---|
| 1 | Create a test customer and do the main action once | The usage event appears exactly **once** | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 2 | Use each "sticky" feature | Each feature event appears | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 3 | Answer a survey as the test customer | The answer attaches to the right customer | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 4 | Open a support ticket and a Sev-1 bug | Both show on the right customer | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 5 | Calculate the score by hand and compare with the automatic score | Numbers match exactly (Section 5.4) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 6 | Remove one data source on purpose | Missing-data rule (Section 5.5) works and shows "Low confidence" | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 7 | Make the test customer go Red | The right person gets the alert | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 8 | Delete the test customer | Data is removed from every tool (Section 13.5) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 9 | Break a connection on purpose | The "no data" alert fires | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 14.7 Who can access what

| Person | Tool | Access level (view / edit / admin) | Why they need it | Date granted | Next review |
|---|---|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> Review this list **every quarter** and whenever someone joins or leaves the team.

## 14.8 If a tool breaks (fallback plan)

| Tool | If it is down, we... | Who decides | Maximum time we can live without it |
|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` (Example: "Use the last exported spreadsheet and mark scores 'Low confidence'.") | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

---

# 15. BUDGET, STAFFING AND TIMELINE

> **Why this matters:** A plan without dates, people, and money is a wish. This section turns your plan into something you can track.
>
> **In plain words:** How long will each phase take, who will do the work, and how much will it cost?

> **Every number below is a planning guess until you have real data.** Write what you expect, then compare with what actually happens at each phase gate and learn from the difference.

## 15.1 Timeline

| Phase | Suggested starting length (a guess; replace it) | Planned start | Planned end | Actual start | Actual end | Depends on | Owner | Gate review date |
|---|---|---|---|---|---|---|---|---|
| 1 Build | `[FILL IN]` (depends on your product) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 2 Internal Test | 1 to 2 weeks | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | Phase 1 gate | `[FILL IN]` | `[FILL IN]` |
| 3 Beta | 4 to 6 weeks | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | Phase 2 gate and legal review | `[FILL IN]` | `[FILL IN]` |
| 4 Launch | 4 weeks | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | Phase 3 gate | `[FILL IN]` | `[FILL IN]` |
| 5 First 100 | Until you reach 100 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | Phase 4 gate | `[FILL IN]` | `[FILL IN]` |
| 6 First 500 | Until you reach 500 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | Phase 5 gate | `[FILL IN]` | `[FILL IN]` |

**Buffer:** How much extra time is built in for delays? `[FILL IN]` (Example: "2 weeks per phase.")

**What must finish before something else can start?**

| Task | Must finish before | Owner | Due date |
|---|---|---|---|
| Legal and privacy review (Section 13) | Beta starts (real customer data) | `[FILL IN]` | `[FILL IN]` |
| Tracking events built and tested | Internal Test ends | `[FILL IN]` | `[FILL IN]` |
| Tools connected and ID map done (Section 14) | Internal Test starts | `[FILL IN]` | `[FILL IN]` |
| Survey and support process ready | Beta starts | `[FILL IN]` | `[FILL IN]` |
| Playbooks written (Section 8) | Launch | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 15.2 Staffing: who spends how many hours per week?

| Role | Name | Backup | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 |
|---|---|---|---|---|---|---|---|---|
| Product owner | `[FILL IN]` | `[FILL IN]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` |
| Engineering | `[FILL IN]` | `[FILL IN]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` |
| Customer success / support | `[FILL IN]` | `[FILL IN]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` |
| QA | `[FILL IN]` | `[FILL IN]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` |
| Data / analytics | `[FILL IN]` | `[FILL IN]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` |
| Legal / privacy (outside help is fine) | `[FILL IN]` | `[FILL IN]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` | `[hrs]` |

**Capacity rule:** How many Red or Yellow customers can one person look after properly each week? `[FILL IN]`

**What do we do when the Red list gets longer than that?** `[FILL IN]` (Example: "Hire help, pause new sign-ups, or only contact the highest-value Reds first.")

## 15.3 Budget (planned)

Use one currency throughout: `[FILL IN]`

| Cost line | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5 | Phase 6 | Total |
|---|---|---|---|---|---|---|---|
| Tool subscriptions (Section 14.2) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| AI usage costs | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Engineering time | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Support / customer success time | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Survey rewards or beta gifts | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Legal and privacy review | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Training | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Extra safety cushion (contingency) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| **Total planned** | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

**How big is the safety cushion?** `[FILL IN]` (Many teams add some percentage on top for surprises. Choose yours and say why.)

## 15.4 Plan vs. actual (fill in at the end of every phase)

| Phase | Planned cost | Actual cost | Difference | Planned weeks | Actual weeks | Why they differ | What we change next |
|---|---|---|---|---|---|---|---|
| 1 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 2 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 3 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 4 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 5 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 6 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 15.5 Cost per customer

```
COST PER CUSTOMER = (total spent on scoring, support, and customer success) / (number of customers)
```

| Question | Your answer |
|---|---|
| Our target cost per customer | `[FILL IN]` |
| Our actual cost per customer at 100 customers | `[FILL IN]` |
| Our actual cost per customer at 500 customers | `[FILL IN]` |
| If it is too high, what do we automate or stop doing? | `[FILL IN]` |

## 15.6 Approval

| Role | Name | What they approve | Date |
|---|---|---|---|
| Budget owner | `[FILL IN]` | Budget in 15.3 | `[FILL IN]` |
| Product owner | `[FILL IN]` | Timeline in 15.1 | `[FILL IN]` |
| Team leads | `[FILL IN]` | Staffing in 15.2 | `[FILL IN]` |

---

# 16. RISKS, OPEN QUESTIONS AND LESSONS LEARNED

## 16.1 Risks

| What could go wrong? | How likely (Low/Med/High) | How bad (Low/Med/High) | What do we do to prevent or reduce it? | Owner |
|---|---|---|---|---|
| Too few customers to trust the score | `[FILL IN]` | `[FILL IN]` | Use the score to decide who to call; talk to customers directly | `[FILL IN]` |
| Missing or wrong data gives a false score | `[FILL IN]` | `[FILL IN]` | Section 5.5 and QA gates | `[FILL IN]` |
| Team ignores the score | `[FILL IN]` | `[FILL IN]` | Weekly review and clear owners | `[FILL IN]` |
| AI sends a wrong message to a customer | `[FILL IN]` | `[FILL IN]` | Human approval (Section 7.3) | `[FILL IN]` |
| Survey fatigue lowers response rates | `[FILL IN]` | `[FILL IN]` | Survey limit (Section 4.3) | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 16.2 Open questions (everything marked TBD goes here)

| # | Question | Who will answer | Due date | Answer |
|---|---|---|---|---|
| 1 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 2 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

## 16.3 Lessons learned (fill in at the end of each phase)

| Phase | What worked | What did not | What we will change |
|---|---|---|---|
| 1 Build | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 2 Internal Test | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 3 Beta | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 4 Launch | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 5 First 100 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 6 First 500 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

---

# APPENDIX A: PLAIN-WORDS GLOSSARY

| Word | What it means |
|---|---|
| **Health score** | A number from 0 to 100 showing how happy and likely to stay a customer is |
| **Signal** | A measurable clue about customer happiness (such as logins) |
| **Weight** | How much one signal counts toward the total score |
| **Churn** | When a customer leaves |
| **Retention** | The share of customers who stay |
| **Aha moment** | The first time a customer sees the product's value |
| **Onboarding** | Helping a new customer get started |
| **NPS** | Net Promoter Score: "How likely are you to recommend us?" (0 to 10) |
| **CSAT** | Customer Satisfaction: "How satisfied are you?" (usually 1 to 5) |
| **CES** | Customer Effort Score: "How easy was it?" (usually 1 to 7) |
| **Sev-1 / Sev-2 / Sev-3** | Bug severity levels: 1 is the worst |
| **Segment** | A group of similar customers |
| **Beta** | An early version tested by a small group |
| **Playbook** | A step-by-step plan for a situation |
| **RACI** | A table showing who is Responsible, Accountable, Consulted, Informed |
| **Human-in-the-loop** | A person checks or approves what AI does |
| **Phase gate** | A checkpoint you must pass before the next phase |
| **Override rule** | A rule that forces a color no matter what the score says |
| **Trend** | Whether a number is going up or down compared with before |
| **Back-test** | Checking whether the score would have warned you about customers who really left |
| **Triage** | Deciding who needs help first |
| **Cohort** | A group of customers who joined in the same period |
| **Audit log** | A written record of what happened, who did it, and when |
| **ADMT** | Automated decision-making technology: software that makes or strongly drives decisions about people |
| **Profiling** | Using data to predict or judge something about a person |
| **DPA** | Data Processing Agreement: a contract with a vendor that handles customer data for you |
| **Personal data** | Any information that can identify a person (name, email, device ID, and so on) |
| **Data minimization** | Collecting only the data you really need |
| **Retention period** | How long you keep data before deleting it |

---

# APPENDIX B: QUICK START ONE-PAGE SUMMARY

Fill this in after finishing the Quick Start sections. Paste it where the whole team can see it.

| Item | Your answer |
|---|---|
| Product | `[FILL IN]` |
| Customer = | `[FILL IN]` |
| Aha moment | `[FILL IN]` |
| Usage measured by | `[FILL IN]` (weight: `[ ]`) |
| Adoption measured by | `[FILL IN]` (weight: `[ ]`) |
| Feedback measured by | `[FILL IN]` (weight: `[ ]`) |
| Support measured by | `[FILL IN]` (weight: `[ ]`) |
| Green / Yellow / Red limits | `[ ]` / `[ ]` / `[ ]` |
| Override rules | `[FILL IN]` |
| Missing data rule | `[FILL IN]` |
| Who acts on Red customers | `[FILL IN]` |
| Where the score lives | `[FILL IN]` |
| Next review date | `[FILL IN]` |

---

# APPENDIX C: FINAL "NO GUESSING" CHECK

Before you call this document finished, answer **Yes** to all of these:

- `[ ]` There is no `[FILL IN]` left anywhere (or each remaining one is a `TBD` with a name and a date)
- `[ ]` Weights add up to exactly 100
- `[ ]` Someone who did not write this document read it and could explain how a score is calculated
- `[ ]` Every row in the RACI table has exactly one **A**
- `[ ]` The human-in-the-loop rules (7.3) are filled in
- `[ ]` The worked example (5.4) was checked with a calculator
- `[ ]` The next review date is written in Section 0
- `[ ]` A lawyer or privacy expert has looked at Section 13
- `[ ]` Every tool in Section 14 has a named admin and **no passwords or keys are written in this file**
- `[ ]` The budget and timeline (Section 15) have a named approver

---

# APPENDIX D: SOURCES USED TO CHECK THIS TEMPLATE

Checked in October 2026. Laws and best practices change, so re-check Section 13 at least every 6 months.

| Topic | Source |
|---|---|
| Health score weighting, trend, back-testing against churn, minimum data, common mistakes | [How to Build a Customer Health Score That Predicts Churn (BuildBetter)](https://blog.buildbetter.ai/how-to-build-a-customer-health-score/) |
| NPS, CSAT and CES definitions, scales, formulas | [NPS vs CSAT vs CES: Key Differences (Omniconvert)](https://www.omniconvert.com/blog/nps-csat-ces/) |
| NIST AI Risk Management Framework: Govern, Map, Measure, Manage | [NIST AI RMF in operations (Kognitos)](https://www.kognitos.com/blog/nist-ai-risk-management-framework/) |
| GDPR Article 22 automated decision-making | [Overview of GDPR Article 22 (GDPR Local)](https://gdprlocal.com/automated-decision-making-gdpr/) |
| California CCPA 2026 regulations on automated decision-making | [California's 2026 CCPA Regulations (Thompson Coburn)](https://www.thompsoncoburn.com/insights/californias-2026-ccpa-regulations-summary-and-preparation-guide/) |
| EU AI Act transparency obligations from 2 August 2026 | [EU AI Act: Transparency Obligations (Cooley)](https://www.cooley.com/news/insight/2026/2026-08-03-eu-ai-act-transparency-obligations-take-effect-2-august-2026) |

**What could not be confirmed:** The EU AI Act source did not say whether the EU "digital omnibus" proposals changed any dates, so confirm current deadlines with a lawyer. Rights-request deadlines and children's age limits vary by law and region; confirm them locally.

---

# APPENDIX E: INDUSTRY ADD-ONS

> **How to use:** Find your industry. Copy the **extra signals** into Section 4.5 and the **extra rules to check** into Section 13.4. These are starting points, not complete lists. Confirm the rules with a specialist for your industry and region.

| Industry | Extra signals worth considering | Extra rules to check (examples) | Special cautions |
|---|---|---|---|
| **Health and wellness apps** | Streaks (days in a row), goals set and met, reminders turned on | Health-data privacy rules (for example HIPAA in the US, special-category data under GDPR), medical-claims rules | Health data is highly sensitive. Collect the minimum. Never use health details to score or contact someone in a way they would not expect. |
| **Finance and payments** | Transactions per month, failed payments, identity-check status, linked accounts | Payment-card security standards (PCI DSS), financial regulators, anti-money-laundering checks, rules on automated credit decisions | Keep the health score **separate** from anything that decides credit, limits, or account closure. Get legal review first. |
| **Education and kids** | Lessons finished, parent or teacher activity, time on task | Children's privacy laws (for example COPPA in the US, age limits under GDPR), student-records laws (for example FERPA in the US) | Children's data needs extra care and often parent consent. Do not run emotion detection on children. |
| **E-commerce and marketplaces** | Repeat orders, cart abandonment, returns, seller response time, dispute rate | Consumer protection, marketing consent, marketplace rules | Score **both sides** (buyers and sellers) separately, since a happy seller can still hide an unhappy buyer. |
| **B2B software (companies as customers)** | Seats used vs. seats bought, admin activity, executive sponsor contact, number of integrations, contract renewal date | Contract terms, data-processing agreements with the customer, security reviews | Score the **account** and the **users** separately. One champion leaving a company is a major warning sign. |
| **Games and consumer apps** | Sessions per week, levels reached, in-app purchases, friends invited | Children's privacy, loot-box and in-app purchase rules, app-store policies | Short lifetimes are normal here. Use shorter time windows (days, not weeks). |
| **AI-powered products** | Number of prompts, accepted vs. rejected AI suggestions, thumbs up/down, corrections made | AI transparency rules (Section 13.4), data-use and model-training promises | Track whether customers **trust** the AI output, not only how often they use it. |
| Your industry: `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

---

# APPENDIX F: FILLED-IN SAMPLE PROJECT ("WaterBuddy")

> **How to use:** This is a made-up example so you can see what finished answers look like. Do **not** copy the numbers. Replace everything with your own. WaterBuddy is a fictional phone app.

## F.1 Sections 0 and 1 (project and snapshot)

| Question | Sample answer |
|---|---|
| Project name | WaterBuddy |
| One-line description | A phone app that reminds people to drink water and shows their daily progress |
| Document owner | Maria Lopez (product owner) |
| Product type | B2C subscription (free plan and paid plan) |
| Problem solved | People forget to drink enough water during the day |
| Who is the customer | Adults aged 25 to 45 who want healthier habits |
| Aha moment | The user logs their first glass of water and sees the progress ring fill up |
| Target time to aha moment | Within 5 minutes of signing up |
| Successful customer | Logs water on at least 5 days per week for 4 weeks in a row |
| Customer about to leave | No log for 10 days, and has turned reminders off |
| Churn means | Cancels the paid plan, or has no activity for 30 days on the free plan |
| Top goals for the first 500 | 1. Retention, 2. Feature adoption, 3. Learn what to build next |

## F.2 Section 3 (segments)

| Segment | How to recognize it | Different expectations? |
|---|---|---|
| Free users | No payment on file | Fewer logins are normal |
| Paid users | Active subscription | Expect daily use and fast support |

Scoring starts: Day 0 for onboarding. Full score from day 14. Not scored: team emails and accounts flagged "test".

## F.3 Section 4 (signals)

| Signal | Sample measure | Healthy (100) | Good | Watch | Risk (0) |
|---|---|---|---|---|---|
| Usage | Active days in last 14 days, plus trend vs. previous 14 days | 10 or more days | 6 to 9 days | 2 to 5 days | 0 to 1 day |
| Adoption | Uses sticky features: Reminders, Progress ring, Friend challenge | 3 features | 2 features | 1 feature | None |
| Feedback | Latest NPS answer (0 to 10) or CSAT (1 to 5) | NPS 9 to 10 or CSAT 5 | NPS 7 to 8 or CSAT 4 | NPS 5 to 6 or CSAT 3 | NPS 0 to 4 or CSAT 1 to 2 |
| Support & bugs | Tickets and bugs in last 30 days | None open | 1 resolved ticket | 2+ tickets or 1 past target | Open Sev-1 or Sev-2 bug, or 3+ unresolved |

Survey rule: NPS at day 30, then every 90 days. CSAT after each support chat. Max one survey per customer per 30 days.

## F.4 Section 5 (scoring)

| Item | Sample answer |
|---|---|
| Weights | Usage 35, Adoption 25, Feedback 20, Support 20 (total 100). Marked "starting guess, not yet tested". |
| Bands | Green 75 to 100, Yellow 50 to 74, Red 0 to 49 |
| Missing data rule | Re-balance the remaining weights and mark the score "Low confidence" if fewer than 3 signals |
| Override to Red | No activity for 21 days, open Sev-1 bug for more than 48 hours, or customer asks to cancel |
| Trend rule | A drop of 15 points or more in 14 days moves the customer down one color and onto the Watch list |
| First validation | When 25 customers have left (about month 5) |

**Sample calculation 1: Priya (all four signals present)**

| Signal | Points | Weight | Calculation | Result |
|---|---|---|---|---|
| Usage | 75 | 35 | 75 x 35 / 100 | 26.25 |
| Adoption | 70 | 25 | 70 x 25 / 100 | 17.50 |
| Feedback | 100 | 20 | 100 x 20 / 100 | 20.00 |
| Support | 100 | 20 | 100 x 20 / 100 | 20.00 |
| **Score** | | | | **83.75 = 🟢 Green (High confidence)** |

**Sample calculation 2: Leo (no survey answer, so we re-balance)**

The three signals present have weights 35 + 25 + 20 = 80. New weights: Usage 35 / 80 = 43.75, Adoption 25 / 80 = 31.25, Support 20 / 80 = 25.

| Signal | Points | New weight | Calculation | Result |
|---|---|---|---|---|
| Usage | 40 | 43.75 | 40 x 43.75 / 100 | 17.50 |
| Adoption | 35 | 31.25 | 35 x 31.25 / 100 | 10.94 |
| Support | 35 | 25.00 | 35 x 25 / 100 | 8.75 |
| **Score** | | | | **37.19 = 🔴 Red (Medium confidence)** |

## F.5 Sections 7 and 8 (AI and playbooks)

| Item | Sample answer |
|---|---|
| AI may do alone | Read data, calculate scores, tag feedback themes, write internal reports |
| AI must ask a human first | Send any customer message, change weights, delete data |
| AI must never | Contact a customer without approval, share one customer's data with another, guess missing data without saying so |
| Customers told about AI? | Yes. The chat says "You are chatting with an AI assistant" |
| Pause rule | Pause the agent if the override rate is above 20% or any wrong message reaches a customer |
| Red playbook | A person emails the customer within 1 business day: "We noticed you may need help with reminders. Can we help?" |
| Yellow playbook | Automatic tip about the unused feature, reviewed weekly |
| Green playbook | After 30 days Green and NPS 9 or 10, ask for an app store review |
| Exit survey | Sent once in the cancel flow, 3 questions, optional |
| Win-back | One email 60 days later if a fix was shipped for their reason, then stop |

## F.6 Section 13 quick answers (legal)

| Question | Sample answer |
|---|---|
| Customers live in | USA and EU |
| STOP test result | All "No". The score only decides who gets a friendly message, and a person reviews it. |
| Design rule | The score never cancels, denies, or reprices anyone |
| Lawyer review | Booked for week 6, before Beta |

## F.7 Section 15 (timeline and budget, sample)

| Phase | Length | Customers at the end |
|---|---|---|
| 1 Build | 8 weeks | 0 |
| 2 Internal Test | 2 weeks | 0 (15 testers) |
| 3 Beta | 5 weeks | 30 beta users |
| 4 Launch | 4 weeks | about 40 |
| 5 First 100 | 6 weeks | 100 |
| 6 First 500 | about 4 months | 500 |

---

# CHANGE LOG

| Version | Date | Who | What changed | Why |
|---|---|---|---|---|
| v0.1 | `[FILL IN]` | `[FILL IN]` | First draft | New project |
| | | | | |
| | | | | |

---

*End of document. Template version 1.0. Copy this file for each new project and keep the master unchanged.*
