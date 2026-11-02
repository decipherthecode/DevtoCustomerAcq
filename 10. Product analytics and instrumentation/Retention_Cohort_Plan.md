# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What is this?** A Retention Cohort Plan answers one question: *"After people start using our product, do they come back, and how do we know?"*
It covers the whole life of the product, from the first line of code to the day your **500th customer** is using it.

**Who can fill it?** Anyone. If you can answer a question in a full sentence, you can fill this in. No analytics experience is needed.

## The 7 Rules

1. **Answer every question.** Never leave a blank. Write one of these instead:
   - `TBD – <name of owner> – <date>` → "I don't know yet, and this person will find out by this date."
   - `N/A – <reason>` → "This does not apply to us, and here is why."
2. **Replace everything in `[square brackets]`.** Text like `[ANSWER HERE]` means "write your answer here."
3. **Use numbers, not feelings.** Write "30% of users" instead of "most users." Write "by 15 Mar 2027" instead of "soon."
4. **One thing, one name.** Pick a name for each event or metric (for example `signup_completed`) and use that exact name everywhere.
5. **Copy the style of the examples.** Each question has an `Example:` line. Do not copy the example's content, only its style.
6. **Do not delete questions.** If a question does not apply, mark it `N/A – <reason>`. This keeps all 100+ projects comparable.
7. **Fill in the order below, then run the checklist in Section 19.**

## Fill-In Order and Time Estimate

| Step | Sections | What you are doing | Time |
|---|---|---|---|
| 1 | Document Control, 1–3 | Describe the product, the goal and the people | 30 min |
| 2 | 4–6 | Decide what "retained" means and how to measure it | 45 min |
| 3 | 7–8 | Plan the journey from build to 500 customers | 45 min |
| 4 | 9–12 | Plan the tracking (events, identity, testing, privacy) | 90 min |
| 5 | 13–16 | Set targets, reports, experiments and customer feedback | 60 min |
| 6 | 17–18 | Risks, owners, timeline | 30 min |
| 7 | 19 | Final checklist and sign-off | 15 min |

**Total: about 5 hours for the first version.** Update it at every phase gate (Section 7).

## Status Tags (use at the top of each section)

| Tag | Meaning |
|---|---|
| `⬜ Not started` | Nothing written yet |
| `🟨 Draft` | Written but not reviewed |
| `🟩 Reviewed` | Checked by a second person |
| `🔒 Approved` | Locked; change only through the Change Log |

## Plain-English Glossary

| Word | Meaning in one line |
|---|---|
| **User** | One person (or one account) that uses the product |
| **Customer** | A user who signed up (free plan) or paid (paid plan). **Section 1 tells you which one counts toward the "500".** |
| **Cohort** | A group of users who share something, usually the week or month they started |
| **Retention** | The share of a cohort that comes back to use the product later |
| **Churn** | The opposite of retention; the share that did not come back |
| **Activation** | The first time a user gets real value from the product (the "aha moment") |
| **Active event** | The one action that counts as "used the product" (for example, "logged a habit") |
| **Day-N retention** | % of a cohort active exactly on day N after starting (Day 1, Day 7, Day 30) |
| **Week-N retention** | The same idea, measured in weeks |
| **Unbounded retention** | % of a cohort active on day N *or any later day* |
| **Bracket retention** | % of a cohort active at any time inside a window (for example, days 8–14) |
| **Rolling retention** | Another name for unbounded retention |
| **Stickiness** | How often active users come back (daily active users ÷ monthly active users) |
| **DAU / WAU / MAU** | Users active on one day / in one week / in one month |
| **Resurrected user** | Someone who left and then came back |
| **Logo retention** | B2B: % of customer *companies* that stay |
| **Net revenue retention (NRR)** | B2B: money kept and grown from existing customers, as a % |
| **Event** | One tracked action (for example, `habit_logged`) |
| **Property** | Extra detail about an event (for example, `habit_type = "water"`) |
| **Instrumentation** | The code that records events |
| **Event tracking plan** | The master list of every event and property (Section 9) |
| **North Star metric** | The single number that best shows customers getting value |
| **Guardrail metric** | A number that must *not* get worse while you improve another one |
| **Phase gate** | A checkpoint you must pass before moving to the next phase |
| **SRM** | Sample Ratio Mismatch: a sign that an experiment's groups were split unfairly |
| **PII** | Personally Identifiable Information (name, email, phone, precise location) |
| **Consent** | Permission from the user to track them |
| **Sample size** | How many users are in a group. Too few means the percentages cannot be trusted |

---

# AI-AGENT INSTRUCTIONS (for any AI tool filling or checking this plan)

> Humans can skip this section. AI agents **must** follow it.

## A. Your Role
You help a human complete this plan. You do **not** invent facts about the product, its users or its data.

## B. Rules for AI Agents
1. **Never guess.** If an answer is not provided by the human or by a source they gave you, write `TBD – <suggested owner> – <suggested date>` and add the question to the "Open Questions for the Human" list in Section 19.
2. **Mark your work.** Put `🤖 AI-drafted` next to anything you wrote, so a human can review it.
3. **Ask before assuming.** Ask the human a question if any of these are unknown: the product type, the definition of "customer", the active event, the analytics tool, the legal region(s).
4. **Keep names consistent.** Reuse the exact event, metric and cohort names already defined. Do not create synonyms.
5. **Never fabricate numbers.** Targets must come from the human, from a cited benchmark, or from their own past data. Label benchmarks as `Benchmark – <source> – <date>`.
6. **Do not delete or reorder sections.** Only fill, mark `N/A`, or add notes.
7. **Respect privacy.** Never put real personal data (names, emails, IDs) in this document. Use fake examples.
8. **Stop and ask a human before** any of the following:
   - Recommending that tracking start for children, health or financial data.
   - Changing a metric definition after the Approved tag is set.
   - Dropping a phase gate or lowering a target.
   - Treating a result from fewer than 30 users per cohort as a conclusion.
9. **Show your reasoning briefly.** For every metric definition or target you propose, add one line starting with `Why:`.

## C. Inputs the Agent Needs Before Starting
| Input | Provided? (Yes/No) | Where |
|---|---|---|
| Product description / PRD | `[Yes/No]` | `[link]` |
| Target users | `[Yes/No]` | `[link]` |
| Analytics tool name | `[Yes/No]` | `[name]` |
| Existing event list (if any) | `[Yes/No]` | `[link]` |
| Legal regions of users | `[Yes/No]` | `[list]` |

## D. Outputs the Agent Must Produce
1. A fully filled document with no empty answers.
2. The Open Questions list (Section 19).
3. A list of every `TBD` with owner and date.
4. A one-paragraph summary at the top of Section 1.

## E. Agent Self-Check Before Handing Back
- [ ] No answer is blank
- [ ] Every metric in Section 6 has a formula and a denominator
- [ ] Every event in Section 9 appears in at least one cohort or metric
- [ ] Every metric in Section 6 has all the events it needs in Section 9
- [ ] Every target in Section 13 has a source
- [ ] Every phase in Section 7 has an exit rule

---

# RETENTION COHORT PLAN

## Document Control

| Field | Answer |
|---|---|
| Product name | `[ANSWER HERE]` |
| Project ID / code | `[ANSWER HERE]` |
| Plan version | `[v0.1]` |
| Status tag | `[⬜ / 🟨 / 🟩 / 🔒]` |
| Author | `[name]` |
| Reviewer | `[name]` |
| Approver | `[name]` |
| Date created | `[YYYY-MM-DD]` |
| Last updated | `[YYYY-MM-DD]` |
| Next review date | `[YYYY-MM-DD]` |
| Related documents (PRD, tracking spec, dashboard) | `[links]` |

### Change Log
| Date | Version | Who | What changed | Why |
|---|---|---|---|---|
| `[date]` | `[v0.1]` | `[name]` | First draft | New plan |

---

# PART A: FOUNDATIONS

## 1. Product Snapshot  `[status tag]`

**Q1.1. In one or two sentences, what does the product do, and for whom?**
*Why it matters: everyone must start with the same picture.*
*Example: "A phone app that helps adults build daily water-drinking habits with reminders and streaks."*
**Answer:** `[ANSWER HERE]`

**Q1.2. What type of product is it? (pick all that apply)**
- [ ] B2C mobile app
- [ ] B2C web app
- [ ] B2B SaaS (companies buy it, many people use it)
- [ ] Marketplace (buyers and sellers)
- [ ] E-commerce (repeat purchases)
- [ ] AI / agent product
- [ ] Other: `[describe]`

**Q1.3. How do customers pay?**
- [ ] Free forever
- [ ] Free trial, then paid
- [ ] Subscription (monthly / yearly)
- [ ] Pay per use
- [ ] One-time purchase
- [ ] Other: `[describe]`

**Q1.4. What counts as a "customer" for the goal of reaching 500?** (choose ONE and stick with it)
- [ ] A person who signed up
- [ ] A person who finished onboarding
- [ ] A person who reached activation (Section 4)
- [ ] A person or company who paid
- [ ] Other: `[describe]`

*Why it matters: "500 customers" means very different things in each case. This choice is used by every phase in Section 7.*

**Q1.5. Which platforms are included?** (iOS, Android, web, desktop, API, etc.)
**Answer:** `[ANSWER HERE]`

**Q1.6. Which countries or regions will your first 500 customers come from?**
*Example: "United States and Canada only."*
**Answer:** `[ANSWER HERE]`

**Q1.7. Today's stage (pick one):**
- [ ] Idea  [ ] Building  [ ] Internal testing  [ ] Private beta  [ ] Public beta  [ ] Launched

**Q1.8. Plan summary (write this last, 3–5 sentences):**
*What will we measure, over what period, and what will we do with the answer?*
**Answer:** `[ANSWER HERE]`

---

## 2. Goal and Decisions  `[status tag]`

**Q2.1. Why are we measuring retention? Finish the sentence:**
"We want to know if users come back so that we can decide whether to ______."
*Example: "...decide whether to spend money on ads, or fix the product first."*
**Answer:** `[ANSWER HERE]`

**Q2.2. List the 3 biggest decisions this plan will inform.**

| # | Decision | Who decides | By when |
|---|---|---|---|
| 1 | `[ANSWER HERE]` | `[name]` | `[date]` |
| 2 | `[ANSWER HERE]` | `[name]` | `[date]` |
| 3 | `[ANSWER HERE]` | `[name]` | `[date]` |

**Q2.3. What is the North Star metric (the one number that shows users get value)?**
*Example: "Number of users who log 5+ drinks in a week."*
**Answer:** `[ANSWER HERE]`

**Q2.4. What is the single most important retention question for the first 500 customers?**
*Example: "Do at least 30% of new users still log a drink in week 4?"*
**Answer:** `[ANSWER HERE]`

**Q2.5. What would make you say "this plan worked"?** (list 2–4 success statements with numbers)
**Answer:** `[ANSWER HERE]`

**Q2.6. What is out of scope?** (things this plan will NOT measure)
**Answer:** `[ANSWER HERE]`

**Q2.7. Guardrail metrics.** What must *not* get worse while we improve retention?
*Example: "App crash rate", "Refund rate", "Support tickets per 100 users".*
**Answer:** `[ANSWER HERE]`

---

## 3. People and Segments  `[status tag]`

**Q3.1. Who is the ideal customer?** (age range, job, need, situation)
**Answer:** `[ANSWER HERE]`

**Q3.2. List the segments you want to compare.** Keep it to 3–6.

| Segment name | How to recognise it (a rule) | Why we care |
|---|---|---|
| `[e.g. "Came from ads"]` | `[e.g. "signup_source = ad"]` | `[ANSWER HERE]` |
| `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` |
| `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` |

**Q3.3. Who must be excluded from every number?** (tick all that apply)
- [ ] Employees and team members
- [ ] Test accounts
- [ ] Bots / automated traffic
- [ ] Beta testers who are friends and family
- [ ] Duplicate accounts
- [ ] Refunded or fraudulent accounts
- [ ] Other: `[describe]`

**Q3.4. How will excluded users be recognised in the data?**
*Example: "email ends with @ourcompany.com, or property is_internal = true."*
**Answer:** `[ANSWER HERE]`

**Q3.5. (B2B only) Who is the "account" and who are the "users" inside it?**
*Example: "Account = a company. Users = employees with a login. Retention is measured at the account level."*
**Answer:** `[ANSWER HERE / N/A – <reason>]`

**Q3.6. (Marketplace only) Which side is measured: buyers, sellers, or both?**
**Answer:** `[ANSWER HERE / N/A – <reason>]`

---

# PART B: DEFINITIONS (WHAT "RETAINED" MEANS)

## 4. Activation and the Active Event  `[status tag]`

**Q4.1. What is the "aha moment"?** (the first time a user clearly gets value)
*Example: "The user logs their first drink and sees their daily progress bar fill."*
**Answer:** `[ANSWER HERE]`

**Q4.2. Which tracked event shows the aha moment happened?**
*Example: `first_habit_logged`*
**Answer:** `[event name]`  *(must exist in Section 9)*

**Q4.3. How soon after signup should the aha moment happen?**
*Example: "Within 24 hours."*
**Answer:** `[ANSWER HERE]`

**Q4.4. Which single action counts as "active" (used the product again)?**
*Rule: it must show real value. Opening the app or logging in alone does NOT count unless that is truly the value.*
*Example: `habit_logged`*
**Answer:** `[event name]`  *(must exist in Section 9)*

**Q4.5. Why is this the right "active" action?**
**Answer:** `[ANSWER HERE]`

**Q4.6. How often should a healthy user be active?** (pick one)
- [ ] Daily  [ ] A few times a week  [ ] Weekly  [ ] Monthly  [ ] Per purchase / per project  [ ] Other: `[describe]`

*Why it matters: this decides whether you measure by day, week or month in Section 5.*

**Q4.7. What counts as a "lost" (churned) user?**
*Example: "No active event for 30 days."*
**Answer:** `[ANSWER HERE]`

**Q4.8. What counts as a "resurrected" user?** (someone who was lost and came back)
**Answer:** `[ANSWER HERE]`

**Q4.9. Time zone used for all dates:** `[e.g. UTC]`
**Q4.10. Does a "day" start at midnight in the user's time zone or in the company time zone?** `[ANSWER HERE]`

---

## 5. Cohort Definitions  `[status tag]`

**Q5.1. What event puts a user into a cohort? (the "start" event)**
*Example: `signup_completed`, or `first_purchase`, or `trial_started`.*
**Answer:** `[event name]`

**Q5.2. How big is each cohort "bucket"?**
- [ ] Daily  [ ] Weekly (Recommended for the first 500 customers)  [ ] Monthly
*Why it matters: with few customers, daily cohorts are too small. Weekly is a safe default.*

**Q5.3. Which week starts the cohort?** (Monday or Sunday) `[ANSWER HERE]`

**Q5.4. List every cohort you will track.**

| Cohort name | Type | Who is in it | Start event | Bucket | Used in phase |
|---|---|---|---|---|---|
| `All new users` | Acquisition | Everyone who starts | `[event]` | `[weekly]` | `[all]` |
| `[e.g. Activated users]` | Behaviour | Users who did `[event]` in first `[X]` days | `[event]` | `[weekly]` | `[phase]` |
| `[e.g. Paid users]` | Revenue | Users who paid | `[event]` | `[monthly]` | `[phase]` |
| `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` | `[event]` | `[bucket]` | `[phase]` |

**Q5.5. How long will you follow each cohort?**
*Example: "12 weeks for B2C apps, 12 months for B2B SaaS."*
**Answer:** `[ANSWER HERE]`

**Q5.6. Can a user be in more than one cohort of the same type?**
*Example: "No. A user joins only the cohort of the week of their FIRST signup, even if they come back later."*
**Answer:** `[ANSWER HERE]`

**Q5.7. What happens to a user who signs up twice or deletes and rejoins?**
**Answer:** `[ANSWER HERE]`

**Q5.8. Minimum cohort size before we trust its percentages.**
*Recommended: at least 30 users per cohort. Below that, show raw counts only.*
**Answer:** `[30 / your number]`

---

## 6. Retention Metrics  `[status tag]`

**Q6.1. Which retention measures will you use?** (tick all and complete the table)

| Use? | Metric | Plain-English meaning | Formula | Best for |
|---|---|---|---|---|
| [ ] | **Day-N (classic)** retention | % of cohort active exactly on day N | users active on day N ÷ users in cohort | Daily-use apps |
| [ ] | **Week-N retention** | % of cohort active in week N | users active in week N ÷ users in cohort | Weekly-use products |
| [ ] | **Unbounded (rolling)** retention | % active on day N or later | users active on or after day N ÷ users in cohort | Products used rarely |
| [ ] | **Bracket retention** | % active inside a window | users active in the window ÷ users in cohort | Smoothing noisy data |
| [ ] | **Stickiness** | How often monthly users are active | DAU ÷ MAU | Daily-use products |
| [ ] | **Logo retention** (B2B) | % of companies that stay | companies at end ÷ companies at start | B2B SaaS |
| [ ] | **Net revenue retention** (B2B) | Revenue kept and grown from existing customers | (start revenue + upgrades − downgrades − cancels) ÷ start revenue | B2B SaaS |
| [ ] | **Repeat purchase rate** | % of buyers who buy again | buyers with 2+ orders ÷ buyers | E-commerce, marketplace |
| [ ] | **Time to second purchase / action** | Days until they come back | median days between first and second action | E-commerce, marketplace |
| [ ] | **Resurrection rate** | % of lost users who return | returned ÷ lost | All |

**Q6.2. For each metric you ticked, fill this card.** (copy the card once per metric)

```
Metric name:            [ANSWER HERE]
Formula:                [ANSWER HERE]
Numerator (top):        [who is counted]
Denominator (bottom):   [who is counted]
Active event used:      [event name from Section 4]
Time window:            [e.g. day 7, week 4]
Cohort(s) used:         [from Section 5]
Segments to compare:    [from Section 3]
Refresh how often:      [daily / weekly]
Owner:                  [name]
Why this metric:        [one sentence]
```

**Q6.3. What are the 3 headline numbers you will look at first, every time?**
*Example: Day-1, Day-7 and Week-4 retention of "Activated users".*
**Answer:** `[ANSWER HERE]`

**Q6.4. How will you show cohort results?**
- [ ] Cohort table (rows = cohorts, columns = time since start)
- [ ] Retention curve (a line that shows how fast people leave)
- [ ] Both (Recommended)

**Q6.5. How do you read the curve?** (circle one after you see real data)
- Falls then **flattens** → you have a core group that stays. Good sign.
- Falls **to zero** → users do not find lasting value. Fix the product first.
- Falls then **rises** → users are coming back (resurrection or seasonality). Investigate.

**Q6.6. Seasonality and special days.** Which dates distort numbers?
*Example: "Holidays, launch day press spike, big sales."*
**Answer:** `[ANSWER HERE]`

---

# PART C: THE JOURNEY FROM BUILD TO 500 CUSTOMERS

## 7. Lifecycle Phases and Phase Gates  `[status tag]`

**How to use this section:** the journey has 8 phases. For each phase, answer the questions and write a **gate**: a rule that must be true before you move on. Phases 0–3 happen *before* real customers. Phases 4–7 are measured by the number of customers (using your answer to Q1.4).

### Overview Table (fill the dates and owners)

| Phase | Name | Customers (by Q1.4) | Start | End | Owner | Gate passed? |
|---|---|---|---|---|---|---|
| 0 | Plan and design the tracking | 0 | `[date]` | `[date]` | `[name]` | `[ ]` |
| 1 | Build and add tracking | 0 | `[date]` | `[date]` | `[name]` | `[ ]` |
| 2 | Test the tracking (QA) | 0 | `[date]` | `[date]` | `[name]` | `[ ]` |
| 3 | Private beta | up to `[e.g. 25]` | `[date]` | `[date]` | `[name]` | `[ ]` |
| 4 | Launch | 1–50 | `[date]` | `[date]` | `[name]` | `[ ]` |
| 5 | Early traction | 51–200 | `[date]` | `[date]` | `[name]` | `[ ]` |
| 6 | Growth | 201–500 | `[date]` | `[date]` | `[name]` | `[ ]` |
| 7 | Review at 500 | 500+ | `[date]` | `[date]` | `[name]` | `[ ]` |

*If your product has a different journey, rename phases but keep all 8 steps.*

### Phase 0: Plan and Design the Tracking
- **Goal:** agree on definitions before any code is written.
- **Q7.0.1. What must be finished?** (tick) [ ] Sections 1–6 filled  [ ] Event tracking plan drafted (Section 9)  [ ] Privacy review started (Section 12)  [ ] Tool chosen
- **Q7.0.2. Which analytics tool is used?** `[tool name, version, plan]`
- **Gate (must all be true):** Sections 1–6 reviewed; every event has an owner.
- **Gate result:** `[Passed / Not passed – reason]`

### Phase 1: Build and Add Tracking
- **Goal:** the product is built and every planned event exists in the code.
- **Q7.1.1. How will events be added?** (tick) [ ] Developers add them as each feature is built  [ ] Added in one batch at the end  [ ] Using an SDK or auto-capture
- **Q7.1.2. Which AI-assisted development tasks are used here?** (tick) [ ] Generate tracking code from Section 9  [ ] Generate tests from Section 11  [ ] Review code for missing events  [ ] None
- **Q7.1.3. Which events are "must have before launch"?** `[list from Section 9]`
- **Gate:** 100% of "must have" events exist in a test environment.
- **Gate result:** `[Passed / Not passed – reason]`

### Phase 2: Test the Tracking (QA)
- **Goal:** prove that the numbers will be right before real people use the product.
- **Q7.2.1. Who runs the tests?** `[name]`
- **Q7.2.2. Which test cases are run?** (from Section 11) `[list or "all"]`
- **Gate:** all "must have" events pass every test in Section 11, and a test cohort shows the expected counts.
- **Gate result:** `[Passed / Not passed – reason]`

### Phase 3: Private Beta
- **Goal:** learn from a small, friendly group, and check that the cohort report works end-to-end.
- **Q7.3.1. How many beta users?** `[number]`
- **Q7.3.2. How are they invited, and are they marked as beta in the data?** `[ANSWER HERE]`
- **Q7.3.3. What are you looking for?** *Example: "Do 5 of 20 users reach the aha moment in 24 hours? Do any events look broken?"*
- **Q7.3.4. Will beta users count toward the 500?** `[Yes / No – reason]`
- **Gate:** the cohort report matches manual counts; activation rate is at least `[X]%`; no "critical" bugs in tracking.
- **Gate result:** `[Passed / Not passed – reason]`

### Phase 4: Launch (Customers 1–50)
- **Goal:** make sure the first real customers can reach value, and watch each of them closely.
- **Q7.4.1. Launch date:** `[date]`
- **Q7.4.2. How will the first 50 customers be found?** `[ANSWER HERE]`
- **Q7.4.3. How often is the dashboard checked?** *Recommended: daily.*
- **Q7.4.4. Do you talk to every customer?** *Recommended: yes, every one (Section 16).*
- **Q7.4.5. What numbers are allowed to be shown as percentages?** *With under 30 users, show counts only (for example "7 of 12 came back").*
- **Gate:** `[X]` customers reached the aha moment (Section 4); top 3 drop-off reasons found.
- **Gate result:** `[Passed / Not passed – reason]`

### Phase 5: Early Traction (Customers 51–200)
- **Goal:** find out if retention is repeatable and which channels bring users who stay.
- **Q7.5.1. What do you change in the product during this phase?** `[ANSWER HERE]`
- **Q7.5.2. Which two segments from Section 3 are compared?** `[ANSWER HERE]`
- **Q7.5.3. What is the minimum cohort size used to draw conclusions?** `[30 or more]`
- **Gate:** Week-`[N]` retention is at least the "Yellow" line in Section 13 for 2 cohorts in a row.
- **Gate result:** `[Passed / Not passed – reason]`

### Phase 6: Growth (Customers 201–500)
- **Goal:** confirm that retention stays good as volume grows, and start experiments.
- **Q7.6.1. Which growth channels are turned on?** `[ANSWER HERE]`
- **Q7.6.2. Which experiments are planned?** (from Section 15) `[list]`
- **Q7.6.3. What will make you slow down or pause marketing?** *Example: "Week-4 retention below Red line for 2 cohorts."*
- **Gate:** retention is at or above the "Green" line for at least `[N]` recent cohorts, or a written plan explains why not.
- **Gate result:** `[Passed / Not passed – reason]`

### Phase 7: Review at 500 Customers
- **Goal:** look back, decide what to do next, and update this template with what you learned.
- **Q7.7.1. What did we learn?** (3–5 bullets) `[ANSWER HERE]`
- **Q7.7.2. Which definitions or targets must change?** `[ANSWER HERE]`
- **Q7.7.3. What is the plan for the next 500–5,000 customers?** `[ANSWER HERE]`
- **Q7.7.4. What should be improved in this template for the next project?** `[ANSWER HERE]`
- **Gate:** review meeting held and decisions recorded in the Change Log.
- **Gate result:** `[Passed / Not passed – reason]`

---

## 8. First 500 Customers: Milestone Tracker  `[status tag]`

**Q8.1. Write the milestones. Fill expected numbers BEFORE launch and real numbers AFTER.**

| Customers reached | Target date | Actual date | Activation rate (expected / actual) | Week-1 retention (expected / actual) | Week-4 retention (expected / actual) | What we learned |
|---|---|---|---|---|---|---|
| 10 | `[date]` | | `[%]` / | `[%]` / | `[%]` / | |
| 25 | `[date]` | | `[%]` / | `[%]` / | `[%]` / | |
| 50 | `[date]` | | `[%]` / | `[%]` / | `[%]` / | |
| 100 | `[date]` | | `[%]` / | `[%]` / | `[%]` / | |
| 200 | `[date]` | | `[%]` / | `[%]` / | `[%]` / | |
| 350 | `[date]` | | `[%]` / | `[%]` / | `[%]` / | |
| 500 | `[date]` | | `[%]` / | `[%]` / | `[%]` / | |

**Q8.2. How many customers do you need per cohort to see a trustworthy pattern?**
*Plain guide: under 30 = look at counts and talk to people. 30–100 = rough trend. 100+ = trustworthy percentages.*
**Answer:** `[ANSWER HERE]`

**Q8.3. What will you do if you are growing too slowly to ever fill a cohort?**
*Example: "Switch from weekly to monthly cohorts, or combine two weeks."*
**Answer:** `[ANSWER HERE]`

**Q8.4. What will you do if you grow so fast that quality drops?** `[ANSWER HERE]`

---

# PART D: INSTRUMENTATION (HOW WE RECORD THE DATA)

## 9. Event Tracking Plan  `[status tag]`

**Q9.1. Naming rule.** Pick one style and write it down.
*Recommended: `object_action` in lowercase with underscores, past tense (for example `habit_logged`, `invoice_paid`).*
**Answer:** `[ANSWER HERE]`

**Q9.2. List every event needed to build the cohorts and metrics in Sections 4–6.** Start with the basics below, then add yours.

| Event name | When it fires (exact trigger) | Why we need it | Cohort / metric that uses it | Phase it must exist | Platform(s) | Owner | Status |
|---|---|---|---|---|---|---|---|
| `app_opened` | App comes to the front | Context only | None | 1 | `[all]` | `[name]` | ⬜ |
| `signup_completed` | Account created successfully | Start event | All new users | 1 | `[all]` | `[name]` | ⬜ |
| `onboarding_completed` | User finishes the last onboarding step | Funnel | Activated users | 1 | `[all]` | `[name]` | ⬜ |
| `[aha_moment_event]` | `[exact trigger]` | Activation | Activated users | 1 | `[all]` | `[name]` | ⬜ |
| `[active_event]` | `[exact trigger]` | Defines "active" | All retention metrics | 1 | `[all]` | `[name]` | ⬜ |
| `subscription_started` | Payment succeeds | Revenue cohort | Paid users | 1 | `[all]` | `[name]` | ⬜ |
| `subscription_cancelled` | User cancels | Churn | Paid users | 1 | `[all]` | `[name]` | ⬜ |
| `account_deleted` | User deletes account | Exclusion and privacy | All | 1 | `[all]` | `[name]` | ⬜ |
| `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` | `[phase]` | `[platform]` | `[name]` | ⬜ |

*Add more rows as needed. Every row must be used by at least one cohort or metric. Remove nothing; mark unused events `Parked – <reason>`.*

**Q9.3. Event properties (details sent with events).**
Fill one card for each important event. Events with no properties can be skipped.

```
Event name:         [ANSWER HERE]
Property name:      [ANSWER HERE]
Type:               [text / number / true-false / date / list]
Allowed values:     [list, or range]
Required?           [Yes / No]
Example value:      [fake example]
Contains PII?       [Yes / No]  (if Yes, see Section 12)
```

**Q9.4. Properties that go on EVERY event.** (tick the ones you use)
- [ ] `user_id`  [ ] `anonymous_id`  [ ] `timestamp`  [ ] `platform`  [ ] `app_version`
- [ ] `country`  [ ] `signup_source`  [ ] `plan`  [ ] `is_internal` (true for team and test)
- [ ] Other: `[list]`

**Q9.5. User properties (facts about the user that rarely change).**
*Example: `signup_date`, `signup_source`, `plan`, `country`, `segment`.*

| User property | Meaning | Set when | Allowed values |
|---|---|---|---|
| `signup_date` | Date of the first signup | Signup | date |
| `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` |

**Q9.6. Which events are sent from the server (more reliable) and which from the app/browser?**
*Rule of thumb: money events and account events should come from the server.*
**Answer:** `[ANSWER HERE]`

**Q9.7. How do you handle offline use or delayed events?** *(for mobile apps)*
**Answer:** `[ANSWER HERE / N/A – <reason>]`

**Q9.8. How will new events be added or changed later?** (who approves, where it is written, how it is announced)
**Answer:** `[ANSWER HERE]`

---

## 10. Identity and Data Model  `[status tag]`

**Q10.1. What is the main ID for a user?** `[e.g. user_id from our database]`
**Q10.2. How do you connect a visitor before signup to the same person after signup?** *(Example: "anonymous_id is merged into user_id at signup.")*
**Answer:** `[ANSWER HERE]`
**Q10.3. What happens when one person uses two devices?** `[ANSWER HERE]`
**Q10.4. (B2B) How do users link to accounts?** `[ANSWER HERE / N/A]`
**Q10.5. Where does the data live?** (tick) [ ] Analytics tool only  [ ] Data warehouse  [ ] Both
**Q10.6. List every data source and how it joins.**

| Source | What it holds | Joins on | Refresh |
|---|---|---|---|
| `[e.g. analytics tool]` | Events | `user_id` | `[real time]` |
| `[e.g. billing system]` | Payments | `user_id` | `[daily]` |
| `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` |

**Q10.7. Where is the single "source of truth" if two systems disagree?** `[ANSWER HERE]`

---

## 11. Tracking QA (Testing That The Numbers Are Right)  `[status tag]`

**Q11.1. Test checklist. Tick and add a date when each passes.**

| # | Test | How to check | Passed (date / who) |
|---|---|---|---|
| 1 | Every "must have" event fires exactly once per action | Do the action once and count in the debug view | |
| 2 | Event names match Section 9 exactly | Compare spelling and case | |
| 3 | Required properties are present and the right type | Inspect 10 sample events | |
| 4 | Timestamps are correct and in the right time zone | Compare with a clock | |
| 5 | Signup connects anonymous visitor to user | Sign up and check merged history | |
| 6 | Internal and test users are excluded | Create a test user and check that it is filtered out | |
| 7 | Events work on every platform listed in Q1.5 | Repeat on each | |
| 8 | Events work offline or on a slow network (mobile) | Turn off Wi-Fi, act, turn on | |
| 9 | Events fire from the server for money and account actions | Check logs | |
| 10 | Cohort report matches a hand count | Count 10 test users on paper and compare | |
| 11 | No duplicate events | Look for the same event twice in the same second | |
| 12 | Consent "No" really stops tracking | Decline consent and check that nothing is sent | |
| 13 | Deleting an account removes or anonymises data | Delete test account and check the data | |

**Q11.2. The "10 test users" check.** Create 10 fake users who do known things (for example 6 come back in week 1, 3 in week 2, 1 never). Expected retention is 60% week 1. Does the cohort report show it?
**Expected:** `[ANSWER HERE]`  **Actual:** `[fill later]`  **Result:** `[Pass / Fail]`

**Q11.3. What are the alert rules once live?**
*Example: "If events per day drop by 30% versus the same weekday last week, notify `[name]`."*
**Answer:** `[ANSWER HERE]`

**Q11.4. How often will you re-test after releases?** `[ANSWER HERE]`

**Q11.5. Who signs off that tracking is correct?** `[name, date]`

---

## 12. Data Quality, Privacy and Consent  `[status tag]`

> This section is a planning guide, not legal advice. Have a qualified person review it.

**Q12.1. Which laws or rules might apply to your users?** (tick)
- [ ] GDPR (Europe / UK)  [ ] CCPA/CPRA (California)  [ ] Children's rules (COPPA or similar)
- [ ] Health data rules  [ ] Financial data rules  [ ] Other: `[list]`  [ ] Not sure → write `TBD – <legal reviewer> – <date>`

**Q12.2. Are any of your users under 18 (or under 13)?** `[Yes / No / Not sure]`
*If Yes or Not sure, stop and get a legal review before tracking starts.*

**Q12.3. What personal data do you collect?** (tick; avoid if you can)
- [ ] Email  [ ] Name  [ ] Phone  [ ] Precise location  [ ] Device ID  [ ] IP address  [ ] Payment details
- [ ] None of these in the analytics tool (Recommended)

**Q12.4. How do you ask for consent?** *(describe where and when; what happens if the user says no)*
**Answer:** `[ANSWER HERE]`

**Q12.5. How long is data kept?** `[e.g. 25 months]`

**Q12.6. How can users ask for their data to be deleted, and who handles it?** `[ANSWER HERE]`

**Q12.7. Who can see raw user-level data?** `[names or roles]`

**Q12.8. Data quality rules. Tick those you will use.**
- [ ] Count each user once per day for "active"
- [ ] Drop events with missing `user_id`
- [ ] Drop events dated in the future
- [ ] Ignore users with more than `[N]` events per minute (likely bots)
- [ ] Mark small cohorts (under 30) clearly in every chart
- [ ] Record the date of any tracking bug and mark affected cohorts
- [ ] Other: `[ANSWER HERE]`

**Q12.9. Known data limits and gaps** (for example, "Android events missing before v1.2")
**Answer:** `[ANSWER HERE / None known]`

---

# PART E: TARGETS, REPORTING AND ACTION

## 13. Targets and Alert Lines  `[status tag]`

**Q13.1. Fill the traffic-light table for each headline metric (Q6.3).**
*Where do numbers come from? Use (a) your own past data, (b) a similar product, or (c) a published benchmark. Write the source. If you have none, write `TBD – <owner> – <date>` and set a first guess to be corrected after 50 customers.*

| Metric | 🟥 Red (act now) | 🟨 Yellow (watch) | 🟩 Green (good) | Source of these numbers | Review date |
|---|---|---|---|---|---|
| Activation rate | below `[%]` | `[%]–[%]` | above `[%]` | `[source]` | `[date]` |
| Day-1 retention | below `[%]` | `[%]–[%]` | above `[%]` | `[source]` | `[date]` |
| Day-7 / Week-1 retention | below `[%]` | `[%]–[%]` | above `[%]` | `[source]` | `[date]` |
| Day-30 / Week-4 retention | below `[%]` | `[%]–[%]` | above `[%]` | `[source]` | `[date]` |
| `[ANSWER HERE]` | | | | | |

**Q13.2. Are targets different per phase?** *Example: "Phase 4 targets are lower because the product is new."*
**Answer:** `[ANSWER HERE]`

**Q13.3. Action rules: what happens when a metric hits each color?**

| Color | What we do | Who | Within |
|---|---|---|---|
| 🟥 Red | `[e.g. pause ads, talk to 10 lapsed users, create a fix ticket]` | `[name]` | `[e.g. 48 hours]` |
| 🟨 Yellow | `[ANSWER HERE]` | `[name]` | `[ANSWER HERE]` |
| 🟩 Green | `[ANSWER HERE]` | `[name]` | `[ANSWER HERE]` |

**Q13.4. How many cohorts in a row must be bad before you act?** *Recommended: 2, unless a bug is suspected.*
**Answer:** `[ANSWER HERE]`

**Q13.5. What would make you change a target?** (who approves, where it is logged)
**Answer:** `[ANSWER HERE]`

---

## 14. Reports, Dashboards and Meetings  `[status tag]`

**Q14.1. List every report.**

| Report | Question it answers | Who reads it | How often | Link | Owner |
|---|---|---|---|---|---|
| Cohort retention table | Do new users come back? | `[roles]` | `[weekly]` | `[link]` | `[name]` |
| Retention curve by segment | Which segments stay longer? | `[roles]` | `[weekly]` | `[link]` | `[name]` |
| Activation funnel | Where do users drop off? | `[roles]` | `[weekly]` | `[link]` | `[name]` |
| 500-customer milestone tracker | Are we on schedule? | `[roles]` | `[weekly]` | `[link]` | `[name]` |
| `[ANSWER HERE]` | `[ANSWER HERE]` | `[roles]` | `[ANSWER HERE]` | `[link]` | `[name]` |

**Q14.2. Which weekly meeting reviews retention, and what is its fixed agenda?**
*Example: "30 minutes, Monday: (1) Numbers vs targets, (2) Biggest drop-off, (3) Experiment updates, (4) Decisions."*
**Answer:** `[ANSWER HERE]`

**Q14.3. How do you write a weekly retention note?** Use this template:
```
Week of:          [date]
Customers so far: [number] of 500
Headline numbers: [Activation %, Week-1 %, Week-4 %] with color
What changed:     [one sentence]
Why (best guess): [one sentence + evidence]
Next action:      [what, who, by when]
```

**Q14.4. Who has access to dashboards and who can edit definitions?** `[ANSWER HERE]`

---

## 15. Experiments and Fixes Backlog  `[status tag]`

**Q15.1. How do findings become actions?** *(describe in 2–3 sentences)*
**Answer:** `[ANSWER HERE]`

**Q15.2. Backlog. Add one row per idea.**

| # | Problem we saw (with number) | Idea to fix it | Expected effect on which metric | Effort (S/M/L) | Impact (S/M/L) | Owner | Status |
|---|---|---|---|---|---|---|---|
| 1 | `[e.g. 60% leave before logging first habit]` | `[ANSWER HERE]` | `[Activation +10 points]` | `[S]` | `[L]` | `[name]` | ⬜ |
| 2 | `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` | `[ ]` | `[ ]` | `[name]` | ⬜ |

**Q15.3. Experiment card (one per test).**
```
Name:                  [ANSWER HERE]
Hypothesis:            "If we ___, then ___ will ___, because ___."
Metric to improve:     [name from Section 6]
Guardrail metric:      [name from Section 2]
Who is included:       [segment]
Split:                 [e.g. 50/50]
Minimum users needed:  [number]
Start / end dates:     [dates]
How we will decide:    [rule written BEFORE the test]
Result:                [fill later]
Decision:              [Ship / Stop / Iterate]
```

**Q15.4. When is it too early to run experiments?**
*Plain guide: with under about 200 customers, tests are rarely conclusive. Prefer talking to users and fixing obvious problems.*
**Answer:** `[ANSWER HERE]`

**Q15.5. How will you check the groups were split fairly (SRM)?** `[ANSWER HERE]`

---

## 16. Voice of the Customer (Why Do They Stay or Leave?)  `[status tag]`

**Q16.1. Numbers show WHAT happened. People tell you WHY. How will you ask?** (tick)
- [ ] Short in-app survey after the aha moment
- [ ] Exit survey on cancel or delete
- [ ] 1-to-1 interviews with `[N]` users per phase
- [ ] Support tickets reviewed weekly
- [ ] Review sites / app store reviews
- [ ] Other: `[ANSWER HERE]`

**Q16.2. Whom will you interview?** *Recommended: 5 who stayed, 5 who left, in each of phases 4–6.*
**Answer:** `[ANSWER HERE]`

**Q16.3. Write 5 questions you will always ask.**
*Examples: "What were you trying to do when you signed up?" · "What nearly stopped you from coming back?" · "What would you use instead?"*
1. `[ANSWER HERE]`
2. `[ANSWER HERE]`
3. `[ANSWER HERE]`
4. `[ANSWER HERE]`
5. `[ANSWER HERE]`

**Q16.4. Where do you record findings so the whole team can read them?** `[link]`

**Q16.5. Churn reason categories** (fixed list, so reasons can be counted)
*Example: Not useful · Too hard · Too expensive · Missing feature · Bug · Found alternative · No longer needed · Other.*
**Answer:** `[ANSWER HERE]`

---

# PART F: RISKS, PEOPLE AND SIGN-OFF

## 17. Risks, Assumptions and Dependencies  `[status tag]`

**Q17.1. Assumptions.** (things you believe but have not proven)

| # | Assumption | How we will test it | By when |
|---|---|---|---|
| 1 | `[e.g. "Users want daily reminders"]` | `[ANSWER HERE]` | `[date]` |
| 2 | `[ANSWER HERE]` | `[ANSWER HERE]` | `[date]` |

**Q17.2. Risks.**

| # | What could go wrong | Chance (L/M/H) | Damage (L/M/H) | What we will do | Owner |
|---|---|---|---|---|---|
| 1 | Tracking bug makes numbers wrong for weeks | `[ ]` | `[ ]` | Alerts in Section 11, re-test after every release | `[name]` |
| 2 | Too few customers to read cohorts | `[ ]` | `[ ]` | Use monthly cohorts and interviews (Section 8) | `[name]` |
| 3 | Users decline consent, so data is missing | `[ ]` | `[ ]` | `[ANSWER HERE]` | `[name]` |
| 4 | Fast growth from a single channel hides poor retention | `[ ]` | `[ ]` | Segment by channel (Section 3) | `[name]` |
| 5 | `[ANSWER HERE]` | `[ ]` | `[ ]` | `[ANSWER HERE]` | `[name]` |

**Q17.3. Dependencies.** (things you need from others)

| Need | From whom | Needed by | Status |
|---|---|---|---|
| `[e.g. analytics tool account]` | `[name]` | `[date]` | ⬜ |
| `[ANSWER HERE]` | `[name]` | `[date]` | ⬜ |

---

## 18. People, Roles and Timeline  `[status tag]`

**Q18.1. Who does what?** (R = does the work, A = final say, C = consulted, I = kept informed)

| Task | Product | Engineering | Data / Analytics | QA | Legal / Privacy | Leadership |
|---|---|---|---|---|---|---|
| Define "active" and cohorts (Sections 4–5) | A/R | C | R | I | I | I |
| Event tracking plan (Section 9) | A | R | R | C | C | I |
| Implement tracking | C | A/R | C | C | I | I |
| Tracking QA (Section 11) | I | R | C | A/R | I | I |
| Privacy review (Section 12) | C | C | C | I | A/R | I |
| Weekly retention review (Section 14) | R | C | A/R | I | I | I |
| Experiments (Section 15) | A/R | R | R | C | I | I |
| Phase gate sign-off (Section 7) | R | C | C | C | C | A |

*Replace roles with real names. A person may fill several roles. Exactly one "A" per row.*

**Q18.2. Who is the single person responsible for this whole plan?** `[name]`
**Q18.3. Who covers if that person is away?** `[name]`
**Q18.4. Key dates.**

| Milestone | Date |
|---|---|
| Plan approved | `[date]` |
| Tracking complete | `[date]` |
| Private beta start | `[date]` |
| Public launch | `[date]` |
| 50 customers | `[date]` |
| 200 customers | `[date]` |
| 500 customers | `[date]` |
| Final review (Phase 7) | `[date]` |

---

# SECTION 19: COMPLETENESS CHECKLIST AND SIGN-OFF

## 19.1 "Is this plan ready?" Checklist

**Clarity**
- [ ] A new teammate can read Section 1 and explain the product in 30 seconds
- [ ] "Customer" (Q1.4) is defined and used the same way in every phase
- [ ] No blank answers; every gap is `TBD` with owner and date or `N/A` with reason
- [ ] Every `[square bracket]` is replaced

**Definitions**
- [ ] The aha moment (Q4.1) and the active event (Q4.4) exist in Section 9
- [ ] Churn and resurrection are defined (Q4.7, Q4.8)
- [ ] Every cohort in Section 5 has a start event and a size rule
- [ ] Every metric in Section 6 has a formula, numerator, denominator and owner

**Journey**
- [ ] All 8 phases have dates, owners and gates (Section 7)
- [ ] Milestone table to 500 customers is filled (Section 8)
- [ ] Small-sample rule is written (Q5.8, Q8.2)

**Tracking**
- [ ] Naming rule is chosen (Q9.1)
- [ ] Every event has a trigger, an owner and a use
- [ ] Identity rules are written (Section 10)
- [ ] All tests in Section 11 have a result or a date
- [ ] The 10-test-users check was done

**Privacy and quality**
- [ ] Laws and minors are addressed (Q12.1, Q12.2)
- [ ] Consent and deletion are described (Q12.4, Q12.6)
- [ ] Internal and test users are excluded (Q3.3, Q3.4)

**Action**
- [ ] Traffic-light targets have a source (Section 13)
- [ ] Each color has an action, an owner and a deadline
- [ ] Weekly meeting and report owner exist (Section 14)
- [ ] Customer interviews are planned (Section 16)

**Safety**
- [ ] Top 5 risks have owners (Section 17)
- [ ] One person owns the whole plan (Q18.2)

## 19.2 Open Questions for the Human (AI agents: list every unanswered item here)

| # | Question | Section | Suggested owner | Needed by |
|---|---|---|---|---|
| 1 | `[ANSWER HERE]` | `[#]` | `[name]` | `[date]` |

## 19.3 Sign-Off

| Role | Name | Decision (Approve / Request changes) | Date | Comments |
|---|---|---|---|---|
| Author | `[name]` | | | |
| Reviewer | `[name]` | | | |
| Approver | `[name]` | | | |

---

# APPENDIX A: WORKED EXAMPLE (A Fictional Habit-Tracker App Called "SipStreak")

> Read this to see what a well-filled plan looks like. All data is made up.

**Product (Q1.1):** "SipStreak is a phone app that helps adults build a daily habit of drinking water, using reminders and streaks."
**Product type (Q1.2):** B2C mobile app.
**Payment (Q1.3):** Free, with a paid plan for extra stats.
**Customer for the 500 goal (Q1.4):** "A person who reached activation: logged their first drink within 24 hours."
**Regions (Q1.6):** United States and Canada only.

**Goal (Q2.1):** "...decide whether to spend money on ads, or fix onboarding first."
**North Star (Q2.3):** "Users who log 5 or more drinks in a week."
**Key question (Q2.4):** "Do at least 30% of activated users still log a drink in week 4?"
**Guardrails (Q2.7):** crash rate under 1%; uninstall rate under 5% in week 1.

**Aha moment (Q4.1):** "The user logs their first drink and sees the progress bar fill." → event `first_drink_logged`.
**Active event (Q4.4):** `drink_logged`.
**Healthy frequency (Q4.6):** A few times a week.
**Churned (Q4.7):** "No `drink_logged` for 14 days."
**Resurrected (Q4.8):** "A churned user who logs a drink again."

**Cohorts (Q5.4):** weekly cohorts of "All new users" (start event `signup_completed`) and "Activated users" (start event `first_drink_logged`). Followed for 12 weeks. Minimum size 30.

**Headline metrics (Q6.3):** Activation rate (activated within 24 hours ÷ signups), Week-1 retention, Week-4 retention.

**Events (Q9.2, shortened):**

| Event name | Trigger | Used by |
|---|---|---|
| `signup_completed` | Account created | All new users cohort |
| `first_drink_logged` | First time a drink is logged | Activated users cohort |
| `drink_logged` | Any drink logged | All retention metrics |
| `reminder_tapped` | User taps a reminder | Experiment on reminders |
| `subscription_started` | Payment succeeds | Paid users cohort |

**Targets (Q13.1, first guess, to be corrected after 50 customers):**

| Metric | 🟥 Red | 🟨 Yellow | 🟩 Green | Source |
|---|---|---|---|---|
| Activation rate | below 30% | 30–50% | above 50% | Team estimate from beta |
| Week-1 retention | below 20% | 20–35% | above 35% | Team estimate from beta |
| Week-4 retention | below 10% | 10–25% | above 25% | Team estimate from beta |

**Actions (Q13.3):** Red → pause ads, interview 10 lapsed users within 48 hours, open a fix ticket. Yellow → review at the next Monday meeting. Green → keep going and test one improvement per week.

**Journey highlights (Section 7):**
- Phase 2 gate: all 13 QA tests pass and the 10-test-users check shows 60% week-1 retention as expected.
- Phase 4 gate: 50 customers reached; at least 25 activated; top 3 drop-off reasons found through 15 interviews.
- Phase 6 gate: Week-4 retention at or above the Green line for 2 cohorts in a row, or a written plan explains why not.

**Weekly note (Q14.3), sample:**
```
Week of:          2027-03-08
Customers so far: 112 of 500
Headline numbers: Activation 44% 🟨, Week-1 31% 🟨, Week-4 12% 🟨
What changed:     Week-1 retention rose 4 points after the new reminder text.
Why (best guess): Reminder taps went up 18%.
Next action:      Test a second reminder time. Owner: Priya, by 2027-03-15.
```

---

# APPENDIX B: QUICK FORMULA CARDS

**Retention rate (any window):**
`retention = users from the cohort who did the active event in the window ÷ users in the cohort`

**Example:** 40 users joined in week of 1 Mar. 14 of them logged a drink in their 4th week. Week-4 retention = 14 ÷ 40 = **35%**.

**Activation rate:** `users who did the aha event within the allowed time ÷ users who started`

**Stickiness:** `average daily active users ÷ monthly active users` (for example 3,000 ÷ 10,000 = 30%)

**Churn rate:** `100% − retention rate`

**Logo retention (B2B):** `companies still active at the end ÷ companies active at the start`

**Net revenue retention (B2B):** `(starting revenue + upgrades − downgrades − cancellations) ÷ starting revenue`

**Repeat purchase rate:** `customers with 2 or more orders in the period ÷ customers with 1 or more orders`

**Small-sample warning:** with 20 users, one person is 5 points. Do not celebrate or panic over a single swing.

---

# APPENDIX C: COMMON MISTAKES (AVOID THESE)

1. **Using "logged in" as the active event** when the real value is something else.
2. **Mixing cohort types.** Do not compare weekly signup cohorts with monthly payer cohorts.
3. **Including test accounts and team members** in the first 50 customers; it can double your retention.
4. **Trusting percentages from tiny cohorts.** Show counts below 30.
5. **Changing the definition of "active" halfway.** Log the change and restate old cohorts.
6. **Forgetting time zones.** Pick one and use it everywhere.
7. **Counting the same user twice** after reinstall or second device.
8. **Measuring only averages.** Always compare by segment (channel, platform, plan).
9. **Skipping the "why".** Numbers without interviews give no explanation.
10. **Letting the plan go stale.** Update at every phase gate and write it in the Change Log.

---

# APPENDIX D: DECISION LOG

| Date | Decision | Options considered | Why we chose this | Who decided |
|---|---|---|---|---|
| `[date]` | `[ANSWER HERE]` | `[ANSWER HERE]` | `[ANSWER HERE]` | `[name]` |

# APPENDIX E: LINKS AND SOURCES

| Item | Link |
|---|---|
| Product requirements (PRD) | `[link]` |
| Event tracking spreadsheet or tool | `[link]` |
| Dashboards | `[link]` |
| Interview notes | `[link]` |
| Benchmarks used (with date) | `[link]` |
| Legal / privacy review | `[link]` |

---

*End of template. Template version: 1.0. Copy this file for every new project, rename it `Retention_Cohort_Plan.md`, and fill it in using the instructions at the top.*
