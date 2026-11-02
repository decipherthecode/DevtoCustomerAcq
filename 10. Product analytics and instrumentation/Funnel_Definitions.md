# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**File:** `Funnel_Definitions.md`
**Folder:** `Product Analytics and Instrumentation/`
**Template version:** 1.0
**Covers:** Development, Pre-launch, Launch, Early traction, and Growth until your **first 500 customers**.

## What is this document?

A **funnel** is the path people walk from "I have never heard of this product" to "I am a happy customer." At every step some people leave. This document writes down, in plain words, **every step of that path, how we count it, and what we want to happen**.

If this document is complete, a new teammate, a developer, or an AI agent can set up tracking and read the numbers **without guessing**.

## The 10 golden rules

1. **Answer every question.** Never delete a question. If it does not apply, write `N/A - because <reason>`.
2. **If you do not know, write `UNKNOWN`** and add a line in Part 13 (Assumptions and Unknowns Log). Never invent an answer.
3. **Use simple words.** Write as if explaining to a 10-year-old. Short sentences. No secret jargon. If you must use a technical word, add it to the glossary in Part 0.
4. **Replace everything in `[square brackets]`.** Brackets mean "your answer goes here."
5. **Italic lines starting with `Example:` are samples.** Read them, then **delete them** (or keep them if they help).
6. **Use numbers, not feelings.** Write "20 percent within 7 days," not "good" or "fast."
7. **One name per thing.** If you call it "Signup" once, never call it "Registration" later. Names must be identical everywhere in this file.
8. **Every event name uses `snake_case`** (lowercase, words joined by underscores), like `account_created`.
9. **Every row needs an owner.** An owner is a real person or role who answers questions about that row.
10. **Mark your status.** At the top of each Part, set the status: `TODO`, `IN PROGRESS`, `DONE`, or `NEEDS REVIEW`.

## Fill-in order (follow this)

| Order | Part | Time needed |
|---|---|---|
| 1 | Part 1 to 3: Product, Customer, Phases | 20 min |
| 2 | Part 4: The five core funnels (AARRR) | 40 min |
| 3 | Part 5 to 6: Custom funnels and steps | 30 min |
| 4 | Part 7 to 9: Events, Metrics, Identity | 60 min |
| 5 | Part 10 to 11: Privacy, Edge cases, QA | 40 min |
| 6 | Part 12 to 15: Lifecycle, AI rules, Logs, Summary | 30 min |
| 7 | Part 16: Final "Is it done?" check | 10 min |

## Status key

| Tag | Meaning |
|---|---|
| `TODO` | Not started |
| `IN PROGRESS` | Being written |
| `NEEDS REVIEW` | Written, waiting for a second pair of eyes |
| `DONE` | Reviewed and approved |

## Quick example of a finished answer

> **Question:** What is the exact moment a person becomes "Activated"?
> **Good answer:** "When a user creates their first project AND invites at least one teammate, within 7 days of signing up. Event: `project_created` followed by `teammate_invited`."
> **Bad answer:** "When they start using the product properly."

---

# DOCUMENT CONTROL

**Status:** `TODO`

| Field | Your answer |
|---|---|
| Product name | [name] |
| Project / code name | [name] |
| Document owner (one person) | [name, role] |
| Reviewer(s) | [names] |
| Date created | [YYYY-MM-DD] |
| Last updated | [YYYY-MM-DD] |
| Current lifecycle phase (see Part 3) | [Phase 1 / 2 / 3 / 4 / 5] |
| Document status | [DRAFT / IN REVIEW / APPROVED] |
| Analytics tool(s) used | [e.g. Mixpanel, Amplitude, PostHog, GA4, Segment, SQL warehouse, spreadsheet, none yet] |
| Where is the raw data stored? | [tool or database name] |
| Link to product requirements / PRD | [link or UNKNOWN] |
| Link to dashboard(s) | [link or "not built yet"] |

---

# PART 0: GLOSSARY (WORDS USED IN THIS FILE)

Add any word that a beginner might not know. Keep the starter list.

| Word | Plain meaning |
|---|---|
| Funnel | The path of steps people take toward a goal. Fewer people reach each next step. |
| Step | One stage inside a funnel (for example, "Visited pricing page"). |
| Event | A record that says "something happened" (for example, `account_created`). |
| Property | Extra detail attached to an event (for example, `plan = "pro"`). |
| User | A person using the product. |
| Anonymous ID | A temporary label for a visitor we do not know yet. |
| User ID | A permanent label for a person after they sign up or log in. |
| Conversion rate | Out of the people who started a step, the percent who finished it. |
| Drop-off | People who left the funnel at a step. |
| Cohort | A group of people who started in the same week or month. |
| Activation | The first moment a person feels the real value of the product. |
| Retention | People coming back after their first visit. |
| Attribution | Figuring out where a person came from (ad, search, friend, and so on). |
| Instrumentation | Adding the tracking code that records events. |
| Source of truth | The one place we trust when numbers disagree. |
| [your word] | [meaning] |

---

# PART 1: THE PRODUCT IN PLAIN WORDS

**Status:** `TODO`

**Q1.1. In one sentence, what does this product do, and for whom?**
Answer: [one sentence]
*Example: "A mobile app that helps freelancers send invoices and get paid faster."*

**Q1.2. What problem does it solve for the person using it?**
Answer: [one or two sentences]

**Q1.3. What type of product is it? (Tick all that apply)**
- [ ] Web app
- [ ] Mobile app (iOS)
- [ ] Mobile app (Android)
- [ ] Desktop app
- [ ] Marketplace (two sides: sellers and buyers)
- [ ] E-commerce (people buy physical or digital goods)
- [ ] Content / media
- [ ] API / developer tool
- [ ] Other: [describe]

**Q1.4. How does the product make money?**
- [ ] Free (no revenue yet)
- [ ] One-time purchase
- [ ] Subscription (monthly / yearly)
- [ ] Usage-based (pay for what you use)
- [ ] Ads
- [ ] Commission / transaction fee
- [ ] Other: [describe]

**Q1.5. Who is the buyer, and who is the user? (Sometimes they are different people.)**
| Role | Who is it? |
|---|---|
| Person who uses the product | [description] |
| Person who pays | [description] |
| Person who decides to buy | [description] |

**Q1.6. What is the single "aha moment"?** (The first time a new person thinks, "Oh, this is useful!")
Answer: [describe the moment in one sentence]
*Example: "The user sees their first invoice marked as paid."*

---

# PART 2: WHO COUNTS AS A "CUSTOMER"? (THE 500 GOAL)

**Status:** `TODO`

This is the most important definition in the document. **Everyone must agree on it.** The goal is the **first 500 customers**, so we must define "customer" with zero doubt.

**Q2.1. Choose ONE definition of "customer" (tick exactly one):**
- [ ] **A. Paying customer:** paid at least once (real money, not a trial, not refunded).
- [ ] **B. Activated free user:** reached the aha moment (Q1.6) and the product is free.
- [ ] **C. Signed-up user:** created an account.
- [ ] **D. Custom:** [write your own definition below]

**Q2.2. Write the exact definition in one sentence:**
Answer: [sentence]
*Example: "A customer is a person or company that has completed one successful payment and has not requested a refund in 14 days."*

**Q2.3. Which exact event proves someone is a customer?**
| Field | Your answer |
|---|---|
| Event name | [e.g. `payment_succeeded`] |
| Where it fires (app, server, payment tool) | [answer] |
| Which counts toward 500: people or companies/accounts? | [people / accounts] |

**Q2.4. What does NOT count? (Tick all that apply and add more.)**
- [ ] Team members of our own company
- [ ] Test accounts and fake data
- [ ] Refunded or charged-back payments
- [ ] Free trials that never paid
- [ ] Duplicates (same person, two accounts)
- [ ] Other: [add]

**Q2.5. Goal and deadline**
| Field | Your answer |
|---|---|
| Target number of customers | 500 |
| Target date | [YYYY-MM-DD] |
| Who agreed to this goal? | [names, date] |
| Dashboard or report that shows the count | [link or "to be built"] |

---

# PART 3: THE FIVE LIFECYCLE PHASES

**Status:** `TODO`

We split the journey from first line of code to customer number 500 into **five phases**. Each phase has an **entry gate** (when it starts) and an **exit gate** (when we are allowed to move on).

**Q3.1. Fill in the phase table.**

| # | Phase | What happens | Start date | End date | Customers at the end | Phase owner |
|---|---|---|---|---|---|---|
| 1 | **Build** | Product is being designed and developed. Tracking is planned and coded. | [date] | [date] | 0 | [name] |
| 2 | **Pre-launch** | Testing with internal people and a small private group. Waitlist, landing page, beta. | [date] | [date] | 0 to [n] | [name] |
| 3 | **Launch** | Product is open to the public for the first time. | [date] | [date] | 1 to [n] | [name] |
| 4 | **Early traction** | First 1 to 100 customers. We learn fast and fix the biggest leaks. | [date] | [date] | up to 100 | [name] |
| 5 | **Growth to 500** | Repeatable ways of getting customers. We improve each funnel step. | [date] | [date] | up to 500 | [name] |

**Q3.2. What must be TRUE before we leave each phase? (Exit gates.)**

| Phase | Exit gate (a checklist that is clear YES or NO) |
|---|---|
| 1. Build | [e.g. "All events in Part 7 are coded and pass the QA checklist in Part 11."] |
| 2. Pre-launch | [e.g. "20 beta users completed the full funnel with no tracking gaps."] |
| 3. Launch | [e.g. "Launch day passed with no critical bugs; first 10 customers counted correctly."] |
| 4. Early traction | [e.g. "100 customers and activation rate at or above target."] |
| 5. Growth to 500 | [e.g. "500 customers counted; all dashboards match the source of truth."] |

**Q3.3. Which parts of this document are MOST important in each phase?**

| Phase | Focus on these Parts |
|---|---|
| Build | 7, 9, 10, 11 (events, identity, privacy, QA) |
| Pre-launch | 4, 8, 11 (funnel definitions, metrics, testing) |
| Launch | 4, 8 (watch the funnel live) |
| Early traction | 4, 5, 8 (find leaks, adjust) |
| Growth to 500 | 5, 6, 8 (custom funnels, benchmarks) |

---

# PART 4: THE FIVE CORE FUNNELS (AARRR)

**Status:** `TODO`

AARRR stands for **A**cquisition, **A**ctivation, **R**etention, **R**evenue, **R**eferral. Each one is a mini-funnel. Fill **all five blocks**. Copy the block structure exactly.

> **How to think about it:** Acquisition = "They found us." Activation = "They liked it." Retention = "They came back." Revenue = "They paid." Referral = "They told a friend."

## 4.1 ACQUISITION: "How do people find us?"

| Question | Your answer |
|---|---|
| What counts as "acquired" (one clear sentence)? | [e.g. "A visitor lands on our website for the first time."] |
| Start event | [event name or `UNKNOWN`] |
| End event | [event name] |
| Channels we use (tick) | [ ] Search / SEO  [ ] Paid ads  [ ] Social  [ ] Email  [ ] Referral  [ ] Partnerships  [ ] Content / blog  [ ] Communities  [ ] Direct  [ ] Other: [ ] |
| How do we tell channels apart? | [e.g. UTM tags, referrer, signup question] |
| Time window (how long a person has to finish this stage) | [e.g. 30 days] |
| Owner | [name] |

**Steps in this funnel (add or remove rows):**

| Step ID | Step name | Plain description | Event name | Required? |
|---|---|---|---|---|
| ACQ-1 | [Visit] | [Person opens the site/app store page] | [`page_viewed`] | [Yes/No] |
| ACQ-2 | [Interest] | [Person views pricing or features] | [`pricing_viewed`] | [Yes/No] |
| ACQ-3 | [Sign-up started] | [Person clicks "Sign up"] | [`signup_started`] | [Yes/No] |
| ACQ-4 | [Account created] | [Person finishes sign-up] | [`account_created`] | [Yes/No] |

## 4.2 ACTIVATION: "Do they feel the value?"

| Question | Your answer |
|---|---|
| What counts as "activated" (one clear sentence)? | [must match the aha moment in Q1.6] |
| Start event | [e.g. `account_created`] |
| End event (the aha) | [e.g. `first_invoice_paid`] |
| Time window | [e.g. within 7 days of sign-up] |
| What could block activation? (list top 3) | [1] [2] [3] |
| Owner | [name] |

| Step ID | Step name | Plain description | Event name | Required? |
|---|---|---|---|---|
| ACT-1 | [Onboarding started] | [answer] | [event] | [Yes/No] |
| ACT-2 | [First key action] | [answer] | [event] | [Yes/No] |
| ACT-3 | [Aha moment] | [answer] | [event] | [Yes/No] |

## 4.3 RETENTION: "Do they come back?"

| Question | Your answer |
|---|---|
| What counts as "retained" (one clear sentence)? | [e.g. "Does the key action at least once in a week after sign-up."] |
| What is the "key action" that proves real use? | [event name] |
| How do we measure return? | [ ] Day 1 / Day 7 / Day 30  [ ] Week 1 / Week 4  [ ] Monthly active  [ ] Other: [ ] |
| What is "churn" for us (when we say they left)? | [e.g. "No key action for 30 days" or "Cancelled subscription"] |
| Owner | [name] |

| Step ID | Step name | Plain description | Event name | Required? |
|---|---|---|---|---|
| RET-1 | [Returned day 1] | [answer] | [event] | [Yes/No] |
| RET-2 | [Returned week 1] | [answer] | [event] | [Yes/No] |
| RET-3 | [Returned month 1] | [answer] | [event] | [Yes/No] |

## 4.4 REVENUE: "Do they pay?"

| Question | Your answer |
|---|---|
| What counts as "revenue event" (one clear sentence)? | [e.g. "First successful payment."] |
| Start event | [e.g. `checkout_started`] |
| End event | [e.g. `payment_succeeded`] |
| Currency and tax rules | [e.g. "USD, amounts shown before tax"] |
| Is there a free trial? How long? | [Yes (n days) / No] |
| What happens on failed payment? | [answer] |
| Owner | [name] |

| Step ID | Step name | Plain description | Event name | Required? |
|---|---|---|---|---|
| REV-1 | [Plan selected] | [answer] | [event] | [Yes/No] |
| REV-2 | [Checkout started] | [answer] | [event] | [Yes/No] |
| REV-3 | [Payment succeeded] | [answer] | [event] | [Yes/No] |
| REV-4 | [Payment failed] | [answer] | [event] | [Yes/No] |
| REV-5 | [Refund / cancellation] | [answer] | [event] | [Yes/No] |

## 4.5 REFERRAL: "Do they tell friends?"

| Question | Your answer |
|---|---|
| What counts as "referral" (one clear sentence)? | [e.g. "A customer invites someone, and that person signs up."] |
| Is there a referral program or reward? | [Yes: describe / No] |
| How do we know who referred whom? | [e.g. unique invite link or code] |
| Owner | [name] |

| Step ID | Step name | Plain description | Event name | Required? |
|---|---|---|---|---|
| REF-1 | [Invite sent] | [answer] | [event] | [Yes/No] |
| REF-2 | [Invitee signed up] | [answer] | [event] | [Yes/No] |
| REF-3 | [Invitee became customer] | [answer] | [event] | [Yes/No] |

---

# PART 5: CUSTOM FUNNELS (EXTRA PATHS THAT MATTER TO THIS PRODUCT)

**Status:** `TODO`

AARRR may not cover everything. Examples of custom funnels: "Waitlist to beta invite," "Free to paid upgrade," "Seller lists first item" (marketplace), "Developer makes first API call," "Cart to order."

**Q5.1. How many custom funnels do you need?** [number, 0 is allowed]
If 0, write `N/A - AARRR is enough because [reason]`.

**Q5.2. Copy the block below once per custom funnel.**

### Custom Funnel [C1]: [name]

| Question | Your answer |
|---|---|
| Funnel name | [name] |
| Why does it matter? | [one sentence] |
| Which phase(s) is it used in? (Part 3) | [phase numbers] |
| Start event | [event] |
| End event (success) | [event] |
| Time window | [e.g. 14 days] |
| Must steps happen in order? | [Yes (strict order) / No (any order)] |
| Owner | [name] |

| Step ID | Step name | Plain description | Event name | Required? |
|---|---|---|---|---|
| C1-1 | [name] | [answer] | [event] | [Yes/No] |
| C1-2 | [name] | [answer] | [event] | [Yes/No] |

---

# PART 6: FUNNEL RULES (HOW WE COUNT)

**Status:** `TODO`

These rules make sure two people counting the same funnel get the same number.

| Question | Your answer |
|---|---|
| **Counting unit:** do we count people (users), accounts/companies, devices, or sessions? | [choose one per funnel] |
| **Order rule:** must steps happen in order? | [Yes/No, per funnel] |
| **Time window rule:** what is the default time limit to finish a funnel? | [e.g. 7 days for activation, 30 days for revenue] |
| **Re-entry rule:** if someone leaves and comes back, do they count again? | [Yes/No and why] |
| **Time zone** used for all reports | [e.g. UTC] |
| **Week starts on** | [Monday / Sunday] |
| **Which date counts for a person?** (when they first appeared, or when they finished a step) | [answer] |
| **Attribution rule:** which channel gets credit? | [first touch / last touch / other] |
| **Attribution window** | [e.g. 30 days] |
| **Cohort grouping** | [by sign-up week / month] |

---

# PART 7: EVENT AND PROPERTY TRACKING PLAN

**Status:** `TODO`

This is the "shopping list" for developers. **Every step in Parts 4 and 5 must appear here.** If a step has no event, it cannot be measured.

## 7.1 Naming rules

- Event names: `snake_case`, past tense, object then action. Example: `invoice_sent`, not `SendInvoice`.
- Property names: `snake_case`. Example: `plan_name`.
- Never put personal data (names, emails, phone numbers) in event names.
- One meaning per event. Never reuse an event for two different things.

Write any extra project rules: [answer or N/A]

## 7.2 Event table

| Event ID | Event name | Funnel step(s) it powers | When exactly does it fire? | Fired from (web / iOS / Android / server) | Properties it carries | Owner (dev) | Status |
|---|---|---|---|---|---|---|---|
| EV-001 | [`account_created`] | [ACQ-4] | [When the account is saved successfully, not when the button is clicked] | [server] | [`signup_method`, `utm_source`] | [name] | [TODO] |
| EV-002 | [event] | [step] | [trigger] | [where] | [props] | [name] | [TODO] |
| EV-003 | [event] | [step] | [trigger] | [where] | [props] | [name] | [TODO] |

## 7.3 Property table

| Property name | Meaning in plain words | Type (text / number / true-false / date / list) | Allowed values or example | Required? | Used by events |
|---|---|---|---|---|---|
| [`plan_name`] | [Which plan the person picked] | [text] | [`free`, `pro`, `team`] | [Yes] | [EV-010, EV-011] |
| [property] | [meaning] | [type] | [values] | [Yes/No] | [events] |

## 7.4 Standard properties on EVERY event

Tick the ones you will attach to every event, and add your own.

- [ ] `user_id` (empty before sign-up)
- [ ] `anonymous_id`
- [ ] `timestamp` (with time zone)
- [ ] `platform` (web / ios / android / server)
- [ ] `app_version`
- [ ] `environment` (production / staging / test)
- [ ] `utm_source`, `utm_medium`, `utm_campaign`
- [ ] `country` or `locale`
- [ ] Other: [add]

---

# PART 8: METRICS, TARGETS AND BENCHMARKS

**Status:** `TODO`

## 8.1 Metric definitions (the exact math)

| Metric | Plain meaning | Formula (top / bottom) | Time window | Source of truth | Owner |
|---|---|---|---|---|---|
| Visitor-to-signup rate | Of visitors, how many sign up | [`account_created` users / `page_viewed` users] | [30 days] | [tool] | [name] |
| Activation rate | Of sign-ups, how many reach the aha | [users with aha event / users with `account_created`] | [7 days] | [tool] | [name] |
| Day-7 retention | Of new users, how many return on day 7 | [returned on day 7 / cohort size] | [per weekly cohort] | [tool] | [name] |
| Free-to-paid rate | Of activated users, how many pay | [paying / activated] | [30 days] | [tool] | [name] |
| Referral rate | Of customers, how many invite someone | [customers who invited / customers] | [60 days] | [tool] | [name] |
| Customer acquisition cost (CAC) | Money spent to get one customer | [total acquisition spend / new customers] | [month] | [tool] | [name] |
| Time to first value | How long from sign-up to aha | [median time between events] | [per cohort] | [tool] | [name] |
| [your metric] | [meaning] | [formula] | [window] | [tool] | [name] |

## 8.2 Targets for each phase

Write a real number. If you have no data yet, write your best guess **and** mark it `GUESS`. Replace guesses after real data arrives.

| Funnel step or metric | Phase 2 Pre-launch | Phase 3 Launch | Phase 4 Early traction | Phase 5 Growth to 500 | Is it a GUESS? |
|---|---|---|---|---|---|
| Visitor-to-signup | [%] | [%] | [%] | [%] | [Y/N] |
| Activation rate | [%] | [%] | [%] | [%] | [Y/N] |
| Day-7 retention | [%] | [%] | [%] | [%] | [Y/N] |
| Free-to-paid | [%] | [%] | [%] | [%] | [Y/N] |
| Referral rate | [%] | [%] | [%] | [%] | [Y/N] |
| CAC | [$] | [$] | [$] | [$] | [Y/N] |
| Total customers | [n] | [n] | [n] | 500 | [Y/N] |

## 8.3 Benchmarks (what "good" looks like)

| Question | Your answer |
|---|---|
| Where did the benchmark numbers come from? | [past project, similar product, public report, guess] |
| Link or note for each source | [links] |
| Date of benchmark | [YYYY-MM-DD] |
| What number is a "red alert" (something is broken)? | [e.g. "Activation below 10 percent for 2 weeks"] |

## 8.4 The "Back-of-the-napkin" math to reach 500

Work backward from 500. This shows whether the plan is realistic.

| Line | Your number |
|---|---|
| Customers needed | 500 |
| Free-to-paid rate (or equivalent last-step rate) | [%] |
| Activated users needed (500 divided by the rate above) | [n] |
| Activation rate | [%] |
| Sign-ups needed | [n] |
| Visitor-to-signup rate | [%] |
| Visitors needed | [n] |
| Weeks we have | [n] |
| Visitors needed per week | [n] |
| Does this look possible with our channels? | [Yes / No / Unsure, why] |

---

# PART 9: IDENTITY AND ATTRIBUTION

**Status:** `TODO`

If we cannot tell who is who, the funnel breaks.

| Question | Your answer |
|---|---|
| How do we label a visitor before sign-up? | [anonymous ID by tool / cookie / device ID] |
| What is the permanent user ID? | [database ID, not email] |
| At which exact moment do we link anonymous ID to user ID? | [e.g. at `account_created` and at login] |
| What if one person uses web and mobile? | [how we connect them] |
| What if one account has many people (a team)? | [which ID is the "account" ID] |
| How do we pass UTM tags from the website to the app? | [method] |
| Where is the source channel saved for each user? | [field name and table] |
| Who is allowed to change identity rules? | [name] |

---

# PART 10: PRIVACY, CONSENT AND EDGE CASES

**Status:** `TODO`

## 10.1 Privacy and consent

| Question | Your answer |
|---|---|
| Which laws apply? (tick) | [ ] GDPR  [ ] CCPA/CPRA  [ ] COPPA (children)  [ ] HIPAA  [ ] Other: [ ]  [ ] Unsure (ask legal) |
| Do we need a cookie or tracking consent banner? | [Yes/No/Unsure] |
| What do we track if the person says NO to tracking? | [nothing / only anonymous / only essential] |
| Personal data we must NEVER send to analytics | [e.g. passwords, card numbers, health data, full emails] |
| How long do we keep raw event data? | [e.g. 24 months] |
| How does a person ask us to delete their data? | [process and owner] |
| Who approved this privacy section? | [name, date] |

## 10.2 Edge cases (decide NOW, not later)

| Situation | What we do | Count it in the funnel? |
|---|---|---|
| Internal team uses the product | [exclude by flag `is_internal = true`] | [No] |
| Test / QA accounts | [exclude by flag or email rule] | [No] |
| Bots and spam sign-ups | [filter rule] | [No] |
| Same person signs up twice | [merge rule] | [Once] |
| User refunds or charges back | [rule] | [answer] |
| User cancels and later returns (win-back) | [counts as new customer or returning?] | [answer] |
| User upgrades or downgrades plan | [rule] | [answer] |
| Free trial ends without payment | [rule] | [answer] |
| Failed payment, then successful retry | [rule] | [answer] |
| Event arrives late (offline mobile) | [which timestamp wins] | [answer] |
| Event fires twice by mistake | [dedupe rule] | [Once] |
| Customer is added by sales manually (no app event) | [how we record it] | [answer] |
| [your situation] | [rule] | [answer] |

---

# PART 11: QUALITY ASSURANCE (TESTING THE TRACKING)

**Status:** `TODO`

Do not trust a number until it passes these checks.

## 11.1 Pre-launch checklist

Tick when done. Each line needs a name and date.

- [ ] Every step in Parts 4 and 5 has an event in Part 7.
- [ ] Every event in Part 7 is coded.
- [ ] Event names exactly match this document (spelling and case).
- [ ] Each event fires **once**, not twice.
- [ ] Each event fires **only when the real action succeeds** (not on a failed attempt).
- [ ] All required properties are present and have the right type.
- [ ] No personal data leaks into events (Part 10).
- [ ] Anonymous ID links to User ID after sign-up (Part 9).
- [ ] UTM / source data arrives correctly.
- [ ] Test data is separated from real data (`environment` flag).
- [ ] Internal and test users are excluded from reports.
- [ ] The full funnel was walked through by a real person on every platform (web / iOS / Android).
- [ ] Funnel numbers in the dashboard match the raw database within [n] percent.
- [ ] Payment events match the payment provider's records.
- [ ] Consent rules (Part 10) work when tracking is declined.
- [ ] Dashboards load correctly and show the right time zone.
- [ ] An alert exists for "event volume dropped to zero."

## 11.2 Test script (walk it step by step)

| Test # | What the tester does | Expected event(s) | Expected properties | Pass / Fail | Tester | Date |
|---|---|---|---|---|---|---|
| T-01 | [Open the site from a test ad link] | [`page_viewed`] | [`utm_source=test`] | [ ] | [name] | [date] |
| T-02 | [Click Sign up and finish] | [`signup_started`, `account_created`] | [`signup_method`] | [ ] | [name] | [date] |
| T-03 | [Do the aha action] | [event] | [props] | [ ] | [name] | [date] |
| T-04 | [Pay with a test card] | [`payment_succeeded`] | [`amount`, `currency`] | [ ] | [name] | [date] |
| T-05 | [Refund the payment] | [`refund_issued`] | [props] | [ ] | [name] | [date] |

## 11.3 Ongoing health checks (after launch)

| Check | How often | Who | What counts as a problem |
|---|---|---|---|
| Event volume is not zero | [daily] | [name] | [drops over 30 percent versus last week] |
| Funnel total vs database total | [weekly] | [name] | [difference over 3 percent] |
| New unknown event names appear | [weekly] | [name] | [any new name not in Part 7] |
| Payment records match analytics | [weekly] | [name] | [any mismatch] |

---

# PART 12: LIFECYCLE CHECKLIST (DEVELOPMENT TO CUSTOMER 500)

**Status:** `TODO`

Tick each item as it is finished. This ties tracking to every phase.

### Phase 1: Build
- [ ] Customer definition agreed (Part 2)
- [ ] Funnels and steps defined (Parts 4 to 6)
- [ ] Event plan written and reviewed (Part 7)
- [ ] Identity and privacy rules approved (Parts 9, 10)
- [ ] Tracking code written for all events
- [ ] Test and staging environments separated

### Phase 2: Pre-launch
- [ ] QA test script passed (Part 11)
- [ ] Beta users completed full funnel
- [ ] Dashboards built for each funnel
- [ ] Targets entered (Part 8)
- [ ] Alerts configured

### Phase 3: Launch
- [ ] Launch-day dashboard watched live
- [ ] First 10 customers manually verified against payment records
- [ ] Any broken event fixed within [n] hours

### Phase 4: Early traction (customers 1 to 100)
- [ ] Weekly funnel review held
- [ ] Biggest drop-off step identified and written down
- [ ] Targets updated using real data (GUESS flags removed)
- [ ] First cohort retention measured

### Phase 5: Growth to 500
- [ ] Best acquisition channel identified
- [ ] Custom funnels reviewed (Part 5)
- [ ] CAC and payback tracked
- [ ] Referral loop measured
- [ ] Customer 500 reached and verified against the source of truth
- [ ] Lessons written in the Decision Log (Part 14)

---

# PART 13: RULES FOR AI AGENTS, ASSUMPTIONS AND UNKNOWNS

**Status:** `TODO`

## 13.1 Rules for any AI agent reading or editing this file

An AI agent (such as a coding assistant) that uses this document **must**:

1. Treat Parts 2, 4, 5, 6, 7 and 8 as the **source of truth**. Do not rename events or change formulas on its own.
2. **Never guess.** If a value is `UNKNOWN` or missing, add a question to the Unknowns Log (13.3) and ask the owner.
3. **Never invent event names or properties** that are not listed in Part 7. Propose them instead, and wait for approval.
4. **Never send personal data** listed as forbidden in Part 10.
5. When writing tracking code, use the exact event names, property names, and trigger moments from Part 7.
6. After writing code, run or describe the tests from Part 11 and report pass or fail for each.
7. Keep the YAML summary (Part 15) in sync with every change to this file.
8. Record every change in the Change Log (Part 14).
9. If two parts of this file disagree, stop and ask. Do not pick one.
10. Never mark a status `DONE` or a checklist item ticked unless it was actually verified.

**Allowed without asking:** fixing typos, formatting, adding glossary words.
**Needs human approval first:** changing the customer definition, any event name or meaning, any formula, any target, privacy rules.

## 13.2 Assumptions log

Write down everything you assumed because you did not have facts.

| # | Assumption | Why we assumed it | Risk if wrong (Low / Med / High) | Who will confirm | Confirm by (date) | Confirmed? |
|---|---|---|---|---|---|---|
| A-01 | [assumption] | [reason] | [risk] | [name] | [date] | [ ] |

## 13.3 Unknowns and open questions log

| # | Question we cannot answer yet | Which Part it blocks | Owner | Due date | Answer (when found) |
|---|---|---|---|---|---|
| U-01 | [question] | [Part #] | [name] | [date] | [answer] |

## 13.4 Hand-off checklist (before giving this to a developer, agent, or new teammate)

- [ ] No `UNKNOWN` left in Parts 2, 4, 7 (or each one is listed in 13.3)
- [ ] Every `[bracket]` was replaced
- [ ] Every example line was removed or kept on purpose
- [ ] Every table row has an owner
- [ ] Glossary covers every special word used
- [ ] YAML summary (Part 15) matches the tables above

---

# PART 14: DECISION LOG AND CHANGE LOG

**Status:** `TODO`

## 14.1 Decision log (important choices and why)

| Date | Decision | Why we chose it | Other options we rejected | Decided by |
|---|---|---|---|---|
| [date] | [e.g. "Customer = first successful payment"] | [reason] | [options] | [names] |

## 14.2 Change log (every edit to this file)

| Version | Date | Changed by | What changed | Why | Approved by |
|---|---|---|---|---|---|
| 1.0 | [date] | [name] | [Initial version] | [New project] | [name] |

---

# PART 15: MACHINE-READABLE SUMMARY (FOR AI AGENTS AND AUTOMATION)

**Status:** `TODO`

Copy the answers from the tables above into this block. **Do not add new facts here that are not in the tables.** If the block and the tables disagree, the tables win and the block must be fixed.

```yaml
funnel_definitions:
  template_version: "1.0"
  product:
    name: ""
    type: []            # web, ios, android, marketplace, ecommerce, api, other
    monetization: ""    # free, one_time, subscription, usage, ads, commission
    aha_moment: ""
  customer_definition:
    type: ""            # paying, activated, signed_up, custom
    sentence: ""
    proof_event: ""
    counts: ""          # users or accounts
    exclusions: []
    goal_count: 500
    goal_date: ""
  analytics:
    tools: []
    source_of_truth: ""
    timezone: "UTC"
    week_starts_on: "Monday"
    attribution:
      model: ""         # first_touch, last_touch, other
      window_days: 30
  phases:
    - id: 1
      name: "Build"
      start: ""
      end: ""
      exit_gate: ""
    - id: 2
      name: "Pre-launch"
      start: ""
      end: ""
      exit_gate: ""
    - id: 3
      name: "Launch"
      start: ""
      end: ""
      exit_gate: ""
    - id: 4
      name: "Early traction"
      start: ""
      end: ""
      exit_gate: ""
    - id: 5
      name: "Growth to 500"
      start: ""
      end: ""
      exit_gate: ""
  funnels:
    - id: "acquisition"
      type: "aarrr"
      definition: ""
      start_event: ""
      end_event: ""
      window_days: 0
      ordered: true
      owner: ""
      steps:
        - id: "ACQ-1"
          name: ""
          event: ""
          required: true
    - id: "activation"
      type: "aarrr"
      steps: []
    - id: "retention"
      type: "aarrr"
      steps: []
    - id: "revenue"
      type: "aarrr"
      steps: []
    - id: "referral"
      type: "aarrr"
      steps: []
    # add custom funnels below, same shape, type: "custom"
  events:
    - id: "EV-001"
      name: ""
      powers_steps: []
      fires_when: ""
      source: ""        # web, ios, android, server
      properties: []
      owner: ""
      status: "TODO"
  metrics:
    - name: ""
      formula: ""
      window: ""
      owner: ""
      targets:
        phase_2: null
        phase_3: null
        phase_4: null
        phase_5: null
      target_is_guess: true
  privacy:
    laws: []
    forbidden_data: []
    retention_months: 0
    consent_required: null
  open_unknowns: []     # list ids from the Unknowns Log, for example U-01
  document_status: "DRAFT"
```

---

# PART 16: FINAL "IS IT DONE?" CHECK

**Status:** `TODO`

Answer YES or NO to every line. **Any NO means the document is not ready.**

| # | Question | YES / NO |
|---|---|---|
| 1 | Can a stranger read Part 2 and know exactly who counts as a customer? | [ ] |
| 2 | Does every funnel step have exactly one event? | [ ] |
| 3 | Does every event have a trigger moment, a platform, and an owner? | [ ] |
| 4 | Does every metric have a formula, a time window, and a source of truth? | [ ] |
| 5 | Are targets written as numbers for all five phases (guesses marked)? | [ ] |
| 6 | Do the back-of-the-napkin numbers (8.4) reach 500 in a believable way? | [ ] |
| 7 | Is the identity rule clear (anonymous to user)? | [ ] |
| 8 | Are privacy and consent rules approved by a named person? | [ ] |
| 9 | Are all edge cases in 10.2 decided? | [ ] |
| 10 | Did the QA checklist (Part 11) pass? | [ ] |
| 11 | Is every `UNKNOWN` listed in 13.3 with an owner and a date? | [ ] |
| 12 | Does the YAML summary match the tables? | [ ] |
| 13 | Would a 10-year-old understand each question well enough to answer it? | [ ] |
| 14 | Has a second person reviewed this document? | [ ] |

**Approved by:** [name] **Date:** [YYYY-MM-DD] **Final status:** [APPROVED / NEEDS WORK]
