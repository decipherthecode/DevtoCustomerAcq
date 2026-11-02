# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **File name:** `Churn_and_Cancellation_Analysis.md`
> **Folder:** `Product analytics and instrumentation/`
> **Template version:** 1.0 | **Works for:** any product (software, app, marketplace, subscription, or one-time-purchase with repeat use)
> **Covers:** Development, Beta, Launch, and the journey to the **first 500 customers**
> **Who can fill it in:** anyone. If you can read and answer questions, you can fill this in.

---

## 0.1 What is this document?

When a customer **leaves** your product, that is called **churn**. When they press a button or send a message to stop, that is a **cancellation**.

This document is a **question-and-answer workbook**. You answer questions about your product. At the end you will have:

1. A clear plan for **measuring** why customers leave.
2. A clear plan for **fixing** the reasons they leave.
3. A clear list of **what to build and track** so an engineer or an AI agent can do the work without guessing.

You do **not** need to know anything technical. Every hard word is explained in the Glossary (Part 20).

## 0.2 The 7 golden rules

| # | Rule | Why it matters |
|---|------|----------------|
| 1 | **Answer every question, or write `UNKNOWN`.** Never leave a blank. | A blank looks like "forgot." `UNKNOWN` says "I need help." |
| 2 | **Replace every `[brackets]`** with your own words. | Brackets are placeholders, not answers. |
| 3 | **Use real numbers.** Write `12 customers`, not `some customers`. | Numbers can be checked. Feelings cannot. |
| 4 | **Do not delete the example.** Examples are marked `🟦 Example`. Keep them or grey them out. | The next person learns from them. |
| 5 | **One answer per line marked `✏️ Your answer:`** | Keeps the file easy for humans and AI to read. |
| 6 | **If you guess, label it `ASSUMPTION`** and add it to Part 18. | Guesses are fine. Hidden guesses are dangerous. |
| 7 | **Update the Status box at the top of each Part** when you finish. | Anyone can see progress at a glance. |

## 0.3 Symbols used in this document

| Symbol | Meaning |
|--------|---------|
| ✏️ | **Your turn.** Write your answer here. |
| 🟦 | **Example.** Shows what a good answer looks like. Do not copy blindly. |
| ⚠️ | **Careful.** A common mistake. |
| 🤖 | **For AI agents.** Instruction or prompt an AI can follow. |
| ✅ | Done / yes |
| ⬜ | Not done yet |
| 🔒 | Privacy or legal item. Handle with care. |
| ⏱️ | Estimated time to fill in |

## 0.3.1 Status codes (use these exactly)

| Code | Meaning |
|------|---------|
| `NOT STARTED` | Nobody has touched it. |
| `IN PROGRESS` | Someone is filling it in. |
| `NEEDS INPUT` | Waiting for a person or data. Say who in the notes. |
| `READY FOR REVIEW` | Filled in. Needs a second pair of eyes. |
| `APPROVED` | Reviewed and signed off. |

## 0.4 How long will this take?

| If your product is... | Time to fill in (first pass) |
|-----------------------|------------------------------|
| In idea or planning stage | 2 to 3 hours (many answers will be "planned") |
| In Build or Beta | 3 to 5 hours |
| Already launched, under 100 customers | 4 to 6 hours |
| Between 100 and 500 customers | 5 to 8 hours (you have real data to add) |

⚠️ **Do not try to finish in one sitting.** Fill in Parts 1 to 3 first. Then do the rest as your product grows. Each Part has a **"When to fill this in"** line.

## 0.5 Which Parts do I fill in, and when?

| Your stage | Must fill in | Can wait |
|------------|--------------|----------|
| **Idea / Planning** | Parts 1, 2, 3, 13, 14 | Everything else |
| **Build** | Parts 1 to 6, 13, 14, 17 | Parts 9 to 12, 15 |
| **Beta** | Parts 1 to 9, 13, 14, 17 | Parts 10 to 12, 15 |
| **Launch** | Everything except Part 19 | Part 19 |
| **Customers 1 to 100** | Everything | Part 19 |
| **Customers 101 to 500** | Everything including Part 19 | nothing |

## 0.6 Simple "if you are stuck" guide

- **"I don't know the answer."** Write `UNKNOWN` and add one line to Part 18 (Open Questions).
- **"I don't understand the question."** Read the Glossary (Part 20), then read the 🟦 Example under it.
- **"My product doesn't have this."** Write `NOT APPLICABLE` and one sentence on why.
- **"I have no data yet."** Write `NO DATA YET` and the date you expect to have data.
- **"Two answers seem right."** Write both. Mark the one you pick with `(CHOSEN)`.

---

# 🤖 PART A. INSTRUCTIONS FOR AI AGENTS (READ BEFORE TOUCHING THIS FILE)

> Humans may skip this Part. AI agents **must** follow it.

**Status:** `NOT STARTED`

## A.1 Your role

You are helping a person complete or use this document. You are **not** allowed to invent facts about the product, customers, prices, or numbers.

## A.2 Hard rules

1. **Never invent data.** If a number is missing, write `UNKNOWN` and add it to Part 18.
2. **Never delete a question.** You may add notes under it.
3. **Always keep the `✏️ Your answer:` marker** so the structure stays parseable.
4. **Quote sources.** When you fill in a fact from a dashboard, file, or message, add `(Source: [where it came from], [date])`.
5. **Label guesses** as `ASSUMPTION` and log them in Part 18.
6. **Never include personal data** (names, emails, phone numbers, card numbers) in this file. Use IDs or counts only. 🔒
7. **Ask before deciding.** If two options are possible and the document does not choose, ask the human. Do not pick silently.
8. **Keep reading level simple.** Short sentences. No unexplained jargon.
9. **Do not change event names** in Part 4 after they are marked `APPROVED` without human sign-off.
10. **Run the QA checklist (Part 17) before saying you are done.**

## A.3 How to read this document

- Each Part has a **Status** line, a **Goal**, and a **When to fill in** line.
- Answers live on lines beginning `✏️ Your answer:` or inside tables with empty cells.
- Anything in `[square brackets]` is a placeholder and must be replaced.
- Anything marked `UNKNOWN` is a work item for a human.

## A.4 How to report back to the human (use this format)

```
SUMMARY: [one or two sentences]
PARTS COMPLETED: [list]
PARTS NEEDING HUMAN INPUT: [list with the exact question]
ASSUMPTIONS MADE: [list, or "none"]
RISKS FOUND: [list, or "none"]
NEXT BEST ACTION: [one thing]
```

## A.5 Machine-readable summary (AI keeps this updated)

```yaml
document: Churn_and_Cancellation_Analysis
template_version: 1.0
project_name: UNKNOWN
current_stage: UNKNOWN        # idea | build | beta | launch | customers_1_100 | customers_101_500
parts_status:
  part_1: NOT STARTED
  part_2: NOT STARTED
  part_3: NOT STARTED
  part_4: NOT STARTED
  part_5: NOT STARTED
  part_6: NOT STARTED
  part_7: NOT STARTED
  part_8: NOT STARTED
  part_9: NOT STARTED
  part_10: NOT STARTED
  part_11: NOT STARTED
  part_12: NOT STARTED
  part_13: NOT STARTED
  part_14: NOT STARTED
  part_15: NOT STARTED
  part_16: NOT STARTED
  part_17: NOT STARTED
  part_18: NOT STARTED
  part_19: NOT STARTED
open_questions_count: 0
assumptions_count: 0
customers_to_date: UNKNOWN
last_updated: UNKNOWN
```

---

# PART 1. PROJECT SNAPSHOT (THE BASICS)

**Status:** `NOT STARTED`
**Goal:** Tell the reader what this product is, so nobody has to guess.
**When to fill in:** Day 1, in any stage.
⏱️ 20 minutes

## 1.1 Document details

| Field | Your answer |
|-------|-------------|
| Project name | ✏️ |
| Product name (as customers see it) | ✏️ |
| Document owner (one person) | ✏️ |
| Date started | ✏️ |
| Last updated | ✏️ |
| Current life-cycle stage (pick one: Idea, Build, Beta, Launch, Customers 1-100, Customers 101-500) | ✏️ |
| Customers today (number) | ✏️ |
| Target date for customer #500 | ✏️ |

## 1.2 What is your product, in plain words?

**Question:** Explain your product as if talking to a 10-year-old. Two or three sentences.

🟦 *Example: "It's an app that helps small bakeries take orders online. The baker adds a menu, and customers pay on their phone."*

✏️ Your answer:

## 1.3 Who pays, and who uses it?

**Question:** Are these the same person? Describe each.

| Role | Who they are | Example |
|------|--------------|---------|
| **Buyer** (the one who pays) | ✏️ | 🟦 Bakery owner |
| **User** (the one who uses it daily) | ✏️ | 🟦 Bakery staff |
| **Decision maker to cancel** | ✏️ | 🟦 Bakery owner |

## 1.4 What type of product is it? (tick all that fit)

- ⬜ Subscription, billed monthly
- ⬜ Subscription, billed yearly
- ⬜ Free trial that converts to paid
- ⬜ Freemium (free forever plan plus paid upgrade)
- ⬜ Pay as you go (usage based)
- ⬜ One-time purchase with repeat use
- ⬜ Marketplace (buyers and sellers)
- ⬜ Contract (fixed term, such as 12 months)
- ⬜ Other: ✏️

## 1.5 Business-to-business or business-to-consumer?

- ⬜ **B2B** (customers are companies; churn = whole account leaves)
- ⬜ **B2C** (customers are individuals; churn = person leaves)
- ⬜ **Both** (explain in one sentence): ✏️

## 1.6 Pricing and plans

| Plan name | Price | Billing cycle (monthly/yearly) | Free trial length (days) | Who is it for |
|-----------|-------|-------------------------------|--------------------------|---------------|
| ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |

## 1.7 How do customers cancel today (or how WILL they)?

**Question:** Describe every way a customer can stop. Tick all that apply.

- ⬜ A "Cancel" button inside the product
- ⬜ Email to support
- ⬜ Phone call
- ⬜ Chat message
- ⬜ Through an app store (Apple, Google)
- ⬜ Through a payment provider portal
- ⬜ They just stop paying (card fails)
- ⬜ They just stop using it (never cancel)
- ⬜ Other: ✏️

## 1.8 Tools and systems you use (so nobody guesses where data lives)

| Purpose | Tool name | Who has access |
|---------|-----------|----------------|
| Billing / payments | ✏️ | ✏️ |
| Product analytics (events) | ✏️ | ✏️ |
| Customer database | ✏️ | ✏️ |
| Customer support / helpdesk | ✏️ | ✏️ |
| Email / messaging | ✏️ | ✏️ |
| Dashboards | ✏️ | ✏️ |
| Surveys | ✏️ | ✏️ |
| Data warehouse (if any) | ✏️ | ✏️ |
| AI agents used | ✏️ | ✏️ |

✏️ **Where is the single "source of truth" for who is a paying customer?** (Name one system.)

---

# PART 2. DEFINITIONS (AGREE ON WORDS BEFORE COUNTING)

**Status:** `NOT STARTED`
**Goal:** Make sure everyone means the same thing by "churn," "active," and "cancelled."
**When to fill in:** Before any measuring. This Part prevents arguments later.
⏱️ 30 minutes

⚠️ **Most common mistake:** Two people count churn differently and get two different numbers. Fix it here, once.

## 2.1 What is an "active customer"?

**Question:** What must be true for someone to count as an active, paying customer today?

🟦 *Example: "A customer with a paid plan, a successful payment in the last 35 days, and who has logged in at least once in the last 30 days."*

✏️ Your answer:

## 2.2 What is "churn" for YOUR product?

**Question:** At what exact moment do you say "this customer has churned"?

| Churn type | Plain meaning | Your exact rule | 🟦 Example rule |
|------------|---------------|-----------------|-----------------|
| **Voluntary churn** | Customer chose to leave | ✏️ | Cancellation confirmed by customer |
| **Involuntary churn** | Customer left because payment failed | ✏️ | Subscription ended after 3 failed payment tries over 14 days |
| **Trial drop-off** | Trial ended without paying | ✏️ | Trial ended and no paid plan within 3 days |
| **Silent churn** | Customer stopped using it but still pays or has not cancelled | ✏️ | No login for 30 days |
| **Downgrade** | Customer moved to a cheaper plan | ✏️ | Plan price decreased |
| **Pause** | Customer paused on purpose | ✏️ | Pause button used |

## 2.3 Important dates and time windows

| Question | Your answer | 🟦 Example |
|----------|-------------|-----------|
| How many days after a failed payment do we wait before calling it churn? (grace period) | ✏️ | 14 days |
| How many days of no use before we call a customer "inactive"? | ✏️ | 30 days |
| If someone cancels and comes back, is that a new customer or the same one? | ✏️ | Same customer if within 90 days |
| Do we count the day they ask to cancel, or the day access ends? | ✏️ | Day access ends |
| Do refunds change how we count? | ✏️ | No, but we record refunds separately |
| What is our time zone for all reports? | ✏️ | UTC |

## 2.4 Words we will use (our shared dictionary)

| Word | Our meaning (one sentence) |
|------|-----------------------------|
| Customer | ✏️ |
| Account | ✏️ |
| User | ✏️ |
| Subscription | ✏️ |
| Cancellation request | ✏️ |
| Cancellation effective | ✏️ |
| Reactivation (coming back) | ✏️ |
| Win-back | ✏️ |

## 2.5 Count rules (decide once)

- ✏️ Are **free** users counted in churn? (Yes / No / Separately): 
- ✏️ Are **test accounts and staff accounts** removed from numbers? (Yes / No, and how do we spot them?): 
- ✏️ Are **customers who joined and left in the same month** counted? (Yes / No): 
- ✏️ For B2B: do we count churn by **account** or by **seat/user**? (Account / Seat / Both): 
- ✏️ For yearly plans: do we count churn at **cancel time** or at **renewal time**? (Cancel / Renewal): 

---

# PART 3. LIFE-CYCLE STAGE PLAN (DEVELOPMENT TO FIRST 500 CUSTOMERS)

**Status:** `NOT STARTED`
**Goal:** Decide what churn work happens at each stage, so you never over-build early or under-build late.
**When to fill in:** At the start, then revisit at every stage change.
⏱️ 45 minutes

## 3.1 The map

```
IDEA ──► BUILD ──► BETA ──► LAUNCH ──► CUSTOMERS 1–100 ──► CUSTOMERS 101–500
 │         │         │         │              │                    │
Plan    Add         Test      Go          Learn why           Find patterns,
churn   tracking    with      live        people leave        fix big causes,
words   and the    real                    (talk to each)      automate
        cancel     people                                       
        flow
```

## 3.2 Stage-by-stage questionnaire

For each stage, answer the questions. If a stage has already passed, answer what actually happened.

### Stage 1: IDEA / PLANNING

| Question | ✏️ Your answer |
|----------|----------------|
| What is the biggest reason we THINK customers might leave? | |
| What is the single best thing that will make them stay? | |
| What is the one number we will watch first? | |
| Who on the team owns churn? | |
| Date this stage ends | |

**Done when:** Part 2 definitions are agreed and Part 14 owners are named.

### Stage 2: BUILD

| Question | ✏️ Your answer |
|----------|----------------|
| Is the "cancel" path designed? (Yes/No, link to design) | |
| Is the event tracking plan (Part 4) approved? | |
| Are the cancel reasons list (Part 5) and survey ready? | |
| Is payment-failure handling planned (Part 6)? | |
| Are privacy rules checked (Part 13)? | |
| What tests will prove tracking works (Part 17)? | |
| Date this stage ends | |

**Done when:** Every event in Part 4 fires in a test environment and shows up in the analytics tool.

### Stage 3: BETA

| Question | ✏️ Your answer |
|----------|----------------|
| How many beta users? | |
| How will we talk to every beta user who leaves? | |
| Are the dashboards (Part 11) showing test data correctly? | |
| What did beta users complain about most? | |
| Date this stage ends | |

**Done when:** At least 90% of beta cancellations have a recorded reason, and tracking numbers match billing numbers.

### Stage 4: LAUNCH

| Question | ✏️ Your answer |
|----------|----------------|
| Launch date | |
| Is every event live in production? | |
| Is the alert system (Part 11) turned on? | |
| Who watches the dashboard daily in the first 2 weeks? | |
| What is our "red alarm" churn number that triggers an emergency meeting? | |

**Done when:** First real cancellation was recorded end to end (event, reason, billing, dashboard) without manual fixing.

### Stage 5: CUSTOMERS 1 TO 100 (LEARN BY TALKING)

| Question | ✏️ Your answer |
|----------|----------------|
| Do we personally contact every person who cancels? (Yes/No) | |
| How many exit interviews or messages will we do? (Target: all of them) | |
| What are the top 3 reasons so far? | |
| What changed in the product because of cancellations? | |
| Churn rate at customer #100 | |

**Done when:** You can name the top 3 reasons with a count for each, and one fix is shipped for the #1 reason.

### Stage 6: CUSTOMERS 101 TO 500 (FIND PATTERNS, AUTOMATE)

| Question | ✏️ Your answer |
|----------|----------------|
| Which customer groups churn most? (plan, source, size, country) | |
| Which first-week actions predict staying? | |
| Which automated save or win-back messages are running? | |
| What is our churn rate at 200, 300, 400, 500 customers? | |
| What experiments did we run and what did we learn? | |

**Done when:** Part 19 (the 500-customer review) is complete.

## 3.3 Quick stage tracker

| Milestone | Planned date | Actual date | Status |
|-----------|--------------|-------------|--------|
| Definitions agreed (Part 2) | ✏️ | ✏️ | ⬜ |
| Tracking plan approved (Part 4) | ✏️ | ✏️ | ⬜ |
| Tracking tested (Part 17) | ✏️ | ✏️ | ⬜ |
| Cancel flow live (Part 5) | ✏️ | ✏️ | ⬜ |
| Dashboards live (Part 11) | ✏️ | ✏️ | ⬜ |
| First customer | ✏️ | ✏️ | ⬜ |
| Customer #100 | ✏️ | ✏️ | ⬜ |
| Customer #250 | ✏️ | ✏️ | ⬜ |
| Customer #500 | ✏️ | ✏️ | ⬜ |

---

# PART 4. TRACKING PLAN (WHAT WE RECORD, EXACTLY)

**Status:** `NOT STARTED`
**Goal:** List every action we record so engineers and AI agents can build tracking without guessing.
**When to fill in:** During Build. Must be approved before Beta.
⏱️ 90 minutes

## 4.1 Plain-English explanation

An **event** is a note the product writes down when something happens. Example: "Maria clicked Cancel at 3:04 PM." An event has:

- a **name** (what happened),
- **properties** (details about it),
- a **who** (which customer), and
- a **when** (the time).

## 4.2 Naming rules (do not break these)

1. Use lowercase with underscores: `subscription_cancelled`.
2. Use **past tense**: something that already happened (`cancel_button_clicked`, not `click_cancel`).
3. Format: `object_action` (`subscription_cancelled`, `payment_failed`).
4. One name = one meaning. Never reuse a name for two things.
5. Never put personal data in an event name.
6. Property names also use lowercase_with_underscores.

✏️ Do you accept these rules? (Yes / No, and what changes): 

## 4.3 Customer identity (so the same person is always the same person)

| Question | ✏️ Your answer | 🟦 Example |
|----------|----------------|-----------|
| What is the unique ID for a customer? | | `customer_id` (random number, not email) |
| What is the unique ID for an account (B2B)? | | `account_id` |
| What is the unique ID for a subscription? | | `subscription_id` |
| When does an anonymous visitor become a known customer? | | At signup |
| How do we join analytics data to billing data? | | By `customer_id` |
| Who creates IDs, and can they ever change? | | Backend, never changes |

⚠️ **Never use email address as the ID.** People change emails.

## 4.4 Properties added to EVERY event

| Property | Meaning | Type | Required? | 🟦 Example |
|----------|---------|------|-----------|-----------|
| `event_time` | When it happened (UTC) | date-time | Yes | 2026-10-18T14:03:00Z |
| `customer_id` | Who | text | Yes | cus_48213 |
| `account_id` | Which company (B2B) | text | If B2B | acc_9921 |
| `plan_name` | Which plan at that moment | text | Yes | pro_monthly |
| `platform` | web, ios, android, backend | text | Yes | web |
| `app_version` | Version of the product | text | Yes | 2.4.1 |
| `source` | Where the action started | text | Yes | settings_page |
| `environment` | production or test | text | Yes | production |

## 4.5 THE TRACKING TABLE (fill in or approve every row)

**Instructions:** Keep all rows marked `REQUIRED`. Add rows for your product. Set status to `PLANNED`, `BUILT`, `TESTED`, or `LIVE`.

### 4.5.1 Sign-up and activation events

| # | Event name | When it fires (plain words) | Extra properties | Priority | Status |
|---|-----------|------------------------------|------------------|----------|--------|
| 1 | `account_created` | Customer finishes signing up | `signup_method`, `acquisition_channel`, `campaign` | REQUIRED | ⬜ |
| 2 | `onboarding_started` | Customer begins setup | `step_total` | REQUIRED | ⬜ |
| 3 | `onboarding_step_completed` | Each setup step done | `step_number`, `step_name` | REQUIRED | ⬜ |
| 4 | `onboarding_completed` | All setup done | `minutes_taken` | REQUIRED | ⬜ |
| 5 | `first_value_reached` | Customer gets the main benefit for the first time (see 4.6) | `value_action` | REQUIRED | ⬜ |
| 6 | ✏️ | | | | ⬜ |

### 4.5.2 Trial and payment events

| # | Event name | When it fires | Extra properties | Priority | Status |
|---|-----------|---------------|------------------|----------|--------|
| 7 | `trial_started` | Free trial begins | `trial_length_days` | REQUIRED | ⬜ |
| 8 | `trial_ending_reminder_sent` | Reminder sent before trial ends | `days_left` | REQUIRED | ⬜ |
| 9 | `trial_converted` | Trial becomes paid | `plan_name`, `days_to_convert` | REQUIRED | ⬜ |
| 10 | `trial_expired` | Trial ended without paying | `trial_active_days` | REQUIRED | ⬜ |
| 11 | `subscription_started` | First payment succeeds | `plan_name`, `price`, `currency`, `billing_cycle` | REQUIRED | ⬜ |
| 12 | `payment_succeeded` | A payment goes through | `amount`, `currency`, `payment_method_type` | REQUIRED | ⬜ |
| 13 | `payment_failed` | A payment is rejected | `failure_reason`, `attempt_number`, `amount` | REQUIRED | ⬜ |
| 14 | `payment_retry_scheduled` | We will try again | `next_attempt_date` | REQUIRED | ⬜ |
| 15 | `payment_method_updated` | Customer fixes card | `source` (email, in_app) | REQUIRED | ⬜ |
| 16 | `dunning_message_sent` | Reminder about failed payment | `channel`, `message_number` | REQUIRED | ⬜ |
| 17 | `subscription_renewed` | Renewal payment succeeds | `renewal_number` | REQUIRED | ⬜ |
| 18 | ✏️ | | | | ⬜ |

### 4.5.3 Cancellation flow events

| # | Event name | When it fires | Extra properties | Priority | Status |
|---|-----------|---------------|------------------|----------|--------|
| 19 | `cancel_flow_entered` | Customer opens the cancel page | `entry_point` | REQUIRED | ⬜ |
| 20 | `cancel_reason_selected` | Customer picks a reason | `reason_code`, `reason_text_provided` (yes/no) | REQUIRED | ⬜ |
| 21 | `save_offer_shown` | We show a discount, pause, or help | `offer_type`, `offer_value` | REQUIRED | ⬜ |
| 22 | `save_offer_accepted` | Customer takes the offer | `offer_type` | REQUIRED | ⬜ |
| 23 | `save_offer_declined` | Customer says no thanks | `offer_type` | REQUIRED | ⬜ |
| 24 | `cancel_flow_abandoned` | Customer leaves cancel page without finishing | `last_step` | REQUIRED | ⬜ |
| 25 | `cancellation_requested` | Customer confirms they want to cancel | `reason_code`, `effective_date` | REQUIRED | ⬜ |
| 26 | `subscription_cancelled` | Access actually ends (cancellation effective) | `reason_code`, `tenure_days`, `churn_type` (voluntary/involuntary) | REQUIRED | ⬜ |
| 27 | `cancellation_reversed` | Customer changes mind before it takes effect | `days_before_effective` | REQUIRED | ⬜ |
| 28 | `subscription_paused` | Customer pauses | `pause_length_days` | If pause exists | ⬜ |
| 29 | `subscription_downgraded` | Moved to cheaper plan | `from_plan`, `to_plan` | REQUIRED | ⬜ |
| 30 | `refund_issued` | Money returned | `amount`, `reason` | REQUIRED | ⬜ |
| 31 | `exit_survey_submitted` | Customer fills survey | `survey_version` | REQUIRED | ⬜ |
| 32 | `cancellation_contacted_support` | Customer asked support to cancel | `channel` | REQUIRED | ⬜ |
| 33 | ✏️ | | | | ⬜ |

### 4.5.4 Usage and warning-sign events

| # | Event name | When it fires | Extra properties | Priority | Status |
|---|-----------|---------------|------------------|----------|--------|
| 34 | `session_started` | Customer opens the product | `session_number` | REQUIRED | ⬜ |
| 35 | `core_action_completed` | Customer does the main thing (see 4.6) | `action_name` | REQUIRED | ⬜ |
| 36 | `feature_used` | Customer uses a named feature | `feature_name` | RECOMMENDED | ⬜ |
| 37 | `support_ticket_created` | Customer asks for help | `category`, `priority` | REQUIRED | ⬜ |
| 38 | `support_ticket_resolved` | Help finished | `minutes_to_resolve`, `satisfaction_score` | RECOMMENDED | ⬜ |
| 39 | `error_shown` | Customer saw an error | `error_code`, `screen` | RECOMMENDED | ⬜ |
| 40 | `inactivity_threshold_reached` | Customer has not used product for N days | `days_inactive` | REQUIRED | ⬜ |
| 41 | `winback_message_sent` | We emailed a former customer | `campaign_id`, `days_since_churn` | REQUIRED | ⬜ |
| 42 | `subscription_reactivated` | Former customer returned | `days_since_churn`, `via_campaign` | REQUIRED | ⬜ |
| 43 | `nps_response_submitted` | Customer answers satisfaction survey | `score` | RECOMMENDED | ⬜ |
| 44 | ✏️ | | | | ⬜ |

## 4.6 The two most important actions (YOU must define these)

**Question A: What is the "first value" moment?** This is the first time a customer gets the benefit they came for.

🟦 *Example: "Bakery receives its first online order."*

✏️ Your answer:

**Question B: What is the "core action"?** The main thing a happy customer does again and again.

🟦 *Example: "Accepts an order, at least 3 times a week."*

✏️ Your answer:

**Question C: How often should a healthy customer do the core action?** 

✏️ Your answer:

## 4.7 Where does each event come from? (Frontend vs Backend)

| Event group | Fires from | Why |
|-------------|-----------|-----|
| Button clicks and screens | Frontend (what the customer sees) | Only the screen knows |
| Payments, cancellations, renewals | **Backend** (server) | More reliable; cannot be blocked by ad blockers |
| Billing provider events | Webhook from billing tool | Billing tool knows the truth |

✏️ Confirm or change: 

⚠️ **Rule:** Any event that affects money or access (`subscription_cancelled`, `payment_failed`) must come from the **backend**, never only from the screen.

## 4.8 Data quality rules

| Rule | Your confirmation (Yes/No) |
|------|---------------------------|
| Every event has `customer_id` | ✏️ |
| No event is sent twice for the same action (no duplicates) | ✏️ |
| Test events are marked `environment = test` and excluded from reports | ✏️ |
| Events arrive within 5 minutes (or state your limit): ✏️ | ✏️ |
| Money amounts are stored in the smallest unit (cents) with currency code | ✏️ |
| Reason codes come from the fixed list in Part 5, not free typing | ✏️ |

## 4.9 Billing vs analytics: do they agree?

**Question:** Billing tool is the truth for money. Analytics is the truth for behavior. How will we check they match?

| Check | How often | Allowed difference | Owner |
|-------|-----------|--------------------|-------|
| Count of cancellations: analytics vs billing | ✏️ weekly | ✏️ 2% | ✏️ |
| Count of active subscriptions | ✏️ | ✏️ | ✏️ |
| Revenue churn amount | ✏️ | ✏️ | ✏️ |

---

# PART 5. CANCELLATION FLOW AND EXIT SURVEY

**Status:** `NOT STARTED`
**Goal:** Design the moment a customer leaves so we learn the true reason, treat them fairly, and offer help.
**When to fill in:** Build stage. Test in Beta.
⏱️ 60 minutes

## 5.1 Fairness rules (non-negotiable)

1. Cancelling must be **as easy as signing up.** No hiding the button.
2. No tricking, guilt-tripping, or endless loops. 🔒 (Some countries and states have laws about this; see Part 13.)
3. Asking "why" is **optional to answer**, but required to be asked.
4. Customers can always finish cancelling after at most **[number] clicks**.

✏️ How many clicks does it take from "Settings" to "Cancelled"? Target 3 or fewer: 

## 5.2 Draw your cancel flow (write each step)

| Step | What the customer sees | What we record (event from Part 4) |
|------|------------------------|-------------------------------------|
| 1 | ✏️ | `cancel_flow_entered` |
| 2 | ✏️ (ask reason) | `cancel_reason_selected` |
| 3 | ✏️ (offer help or discount, if any) | `save_offer_shown` |
| 4 | ✏️ (confirm) | `cancellation_requested` |
| 5 | ✏️ (thank you and what happens next) | `subscription_cancelled` (when access ends) |

🟦 *Example: Step 3 says "Having trouble setting up? Book a free 15-minute help call." with buttons [Book call] and [No thanks, continue cancelling].*

## 5.3 FIXED LIST OF CANCEL REASONS (reason codes)

**Instructions:** Keep these standard codes. Add your own at the bottom. Never rename a code after launch (it breaks old data).

| Code | Customer sees | Group |
|------|--------------|-------|
| `too_expensive` | "It costs too much" | Price |
| `not_using_enough` | "I'm not using it enough" | Value |
| `missing_feature` | "It's missing something I need" | Product |
| `found_alternative` | "I found something else" | Competition |
| `hard_to_use` | "It's too hard or confusing" | Product |
| `bugs_or_errors` | "It's buggy or unreliable" | Quality |
| `poor_support` | "Support did not help" | Service |
| `no_longer_needed` | "I don't need it anymore" | Need ended |
| `temporary_need` | "I only needed it for a short time" | Need ended |
| `business_closed` | "My business closed or changed" | Customer situation |
| `switching_internal` | "We are building or using our own tool" | Competition |
| `billing_issue` | "I had a billing or payment problem" | Billing |
| `privacy_or_trust` | "I'm worried about privacy or trust" | Trust |
| `performance_slow` | "It's too slow" | Quality |
| `other` | "Something else" (free text) | Other |
| `no_reason_given` | Customer skipped | Unknown |
| ✏️ your own | | |
| ✏️ your own | | |

## 5.4 The "tell us more" question

✏️ Exact wording of the optional free-text box: 

🟦 *Example: "Anything we could have done better? (Optional)"*

## 5.5 Save offers (ways to keep the customer, honestly)

| Reason code | Honest offer | Cost to us | Who approves | Turn on at what stage? |
|-------------|--------------|-----------|--------------|------------------------|
| `too_expensive` | ✏️ (cheaper plan, discount for N months) | ✏️ | ✏️ | ✏️ |
| `not_using_enough` | ✏️ (pause, tips email) | ✏️ | ✏️ | ✏️ |
| `missing_feature` | ✏️ (tell us which; add to wish list) | ✏️ | ✏️ | ✏️ |
| `hard_to_use` | ✏️ (free setup call) | ✏️ | ✏️ | ✏️ |
| `bugs_or_errors` | ✏️ (fast support contact) | ✏️ | ✏️ | ✏️ |
| `temporary_need` | ✏️ (pause) | ✏️ | ✏️ | ✏️ |

⚠️ **Do not offer a discount to everyone.** You teach customers to threaten to cancel. Offer only matching help.

## 5.6 After they cancel

| Question | ✏️ Your answer |
|----------|----------------|
| Do they keep access until the end of the paid period? | |
| What happens to their data? For how long? | |
| What email do they get right after cancelling? | |
| What email do they get after 7 days? 30 days? 90 days? | |
| How can they come back with one click? | |

## 5.7 Cancelling through other doors (support, app store, phone)

**Question:** Cancellations that do NOT happen in your cancel flow will have no reason. How will you capture them?

| Door | How we capture the reason | Who is responsible |
|------|---------------------------|--------------------|
| Support email or chat | ✏️ (agent selects reason code in helpdesk) | ✏️ |
| Phone | ✏️ | ✏️ |
| App store | ✏️ (usually no reason; send follow-up survey) | ✏️ |
| Payment portal | ✏️ | ✏️ |
| Card failed (no choice) | Automatic: `payment_failed` reasons in Part 6 | System |

## 5.8 Exit survey and exit interview plan

| Question | ✏️ Your answer |
|----------|----------------|
| Survey length (max 3 questions recommended) | |
| When is it sent? (in the flow / by email after) | |
| Target response rate | |
| Will we offer a small thank-you for a 15-minute call? | |
| For customers 1 to 100: will we try to call or message **every** leaver? | |
| Who runs the interviews? | |
| Where are notes saved? (link) | |

**Interview questions to ask (edit as needed):**

1. What made you sign up in the first place?
2. What did you hope it would do for you?
3. Was there a moment you decided to leave? What happened?
4. What did you try before cancelling?
5. What will you use instead?
6. What one change would have kept you?
7. Would you come back? What would have to be true?

---

# PART 6. INVOLUNTARY CHURN (FAILED PAYMENTS)

**Status:** `NOT STARTED`
**Goal:** Stop losing customers who never wanted to leave: their card just failed.
**When to fill in:** Build stage; review monthly after launch.
⏱️ 45 minutes

**Plain meaning:** Sometimes a card expires, has no money, or is blocked. The customer is lost without ever deciding to leave. In many subscription businesses this is a large share of churn. **Track it separately.**

## 6.1 Our payment failure plan

| Question | ✏️ Your answer | 🟦 Example |
|----------|----------------|-----------|
| How many times do we retry a failed payment? | | 4 times |
| On which days? | | Day 1, 3, 5, 7 |
| How many total days of grace before access stops? | | 14 days |
| Does the customer keep access during grace? | | Yes, with a banner |
| Which billing tool handles retries? | | [Billing tool name] |
| Do we send an email when a card is about to expire? | | Yes, 30 and 7 days before |

## 6.2 Failed-payment message schedule ("dunning")

| Message # | When | Channel (email / in-app / SMS) | Goal | ✏️ Exact message wording or link |
|-----------|------|-------------------------------|------|-----------------------------------|
| 1 | Day 0 (failure) | ✏️ | "Your payment didn't go through. Update here." | |
| 2 | Day 3 | ✏️ | Friendly reminder | |
| 3 | Day 7 | ✏️ | Warn access may stop | |
| 4 | Day 13 | ✏️ | Last chance | |
| 5 | After access ends | ✏️ | Easy way to come back | |

## 6.3 Failure reasons we record

| Code | Meaning | Can we fix it automatically? |
|------|---------|-------------------------------|
| `card_expired` | Card is out of date | Yes: card updater or ask customer |
| `insufficient_funds` | No money available | Retry later |
| `card_declined_generic` | Bank said no | Retry, then ask customer |
| `card_lost_or_stolen` | Card cancelled | Ask for new card |
| `authentication_required` | Bank needs extra check | Send customer to confirm |
| `processing_error` | Our payment provider had a problem | Retry |
| ✏️ your own | | |

## 6.4 Numbers to watch

| Number | Formula (plain words) | Target | ✏️ Today |
|--------|----------------------|--------|----------|
| Failed payment rate | Failed payments ÷ all payment attempts | ✏️ | |
| Recovery rate | Failed payments later fixed ÷ failed payments | ✏️ | |
| Involuntary churn rate | Customers lost to payment failure ÷ customers at start of period | ✏️ | |
| Share of all churn that is involuntary | Involuntary churn ÷ total churn | ✏️ | |

---

# PART 7. TRIAL-TO-PAID DROP-OFF

**Status:** `NOT STARTED`
**Goal:** Understand why people try the product but never pay.
**When to fill in:** Before launch if you have trials; skip with `NOT APPLICABLE` if you don't.
⏱️ 30 minutes

✏️ Do we have a free trial or free plan? (Yes / No / If No, write NOT APPLICABLE and skip this Part): 

## 7.1 Trial basics

| Question | ✏️ Your answer |
|----------|----------------|
| Trial length (days) | |
| Is a card required to start? | |
| What must a person do during the trial to "get it"? (link to Part 4.6) | |
| Target trial-to-paid rate | |
| Number of people who started a trial so far | |
| Number who paid so far | |

## 7.2 The trial funnel (fill in counts when you have data)

| Step | Event | Count | % of previous step |
|------|-------|-------|--------------------|
| Signed up | `account_created` | ✏️ | |
| Started setup | `onboarding_started` | ✏️ | ✏️ |
| Finished setup | `onboarding_completed` | ✏️ | ✏️ |
| Reached first value | `first_value_reached` | ✏️ | ✏️ |
| Started trial | `trial_started` | ✏️ | ✏️ |
| Paid | `trial_converted` | ✏️ | ✏️ |

**Question:** Where is the biggest drop? (Circle the step with the lowest %.) 

✏️ Your answer:

## 7.3 Trial reminders

| Day of trial | Message | Sent? |
|--------------|---------|-------|
| Day 1 | ✏️ Welcome and first step | ⬜ |
| Day [ ] | ✏️ Tip to reach first value | ⬜ |
| Day [ ] (halfway) | ✏️ | ⬜ |
| 3 days before end | ✏️ Trial ending soon | ⬜ |
| Last day | ✏️ | ⬜ |
| 1 day after end | ✏️ Last offer | ⬜ |

---

# PART 8. SILENT CHURN (CUSTOMERS WHO FADE AWAY)

**Status:** `NOT STARTED`
**Goal:** Spot customers who stopped using the product before they cancel (or before their card fails).
**When to fill in:** Beta and after.
⏱️ 30 minutes

## 8.1 What does "fading" look like?

**Question:** List the warning signs for YOUR product.

| Warning sign | How we detect it (event or number) | 🟦 Example |
|--------------|-------------------------------------|-----------|
| No login for N days | ✏️ | No `session_started` for 14 days |
| Core action stops | ✏️ | No `core_action_completed` for 21 days |
| Usage drops by half | ✏️ | Weekly uses fell 50% for 2 weeks |
| Opened many support tickets | ✏️ | 3 tickets in 14 days |
| Visited the cancel page but did not cancel | ✏️ | `cancel_flow_abandoned` |
| Removed teammates (B2B) | ✏️ | Seats dropped |
| Stopped opening our emails | ✏️ | No opens in 60 days |

## 8.2 What do we do when we see a warning sign?

| Warning sign | Action | Who | Within how many days |
|--------------|--------|-----|----------------------|
| ✏️ | ✏️ | ✏️ | ✏️ |
| ✏️ | ✏️ | ✏️ | ✏️ |
| ✏️ | ✏️ | ✏️ | ✏️ |

## 8.3 Health score (simple version, only after 100 customers)

**Question:** Give 3 to 5 signals a point value. Add them up for a score from 0 to 100.

| Signal | Points if yes | ✏️ Your threshold |
|--------|---------------|--------------------|
| Used core action in last 7 days | ✏️ | |
| Completed onboarding | ✏️ | |
| Logged in at least 3 times last 14 days | ✏️ | |
| No unresolved support ticket | ✏️ | |
| On annual plan | ✏️ | |

✏️ **Score below what number means "at risk"?** 

---

# PART 9. METRICS AND FORMULAS

**Status:** `NOT STARTED`
**Goal:** Choose a few numbers, calculate them the same way every time, and know what "good" looks like for you.
**When to fill in:** Beta, with real numbers from Launch onward.
⏱️ 45 minutes

## 9.1 The simple formulas

| Metric | Plain meaning | Formula |
|--------|---------------|---------|
| **Customer (logo) churn rate** | What share of customers left this period | Customers lost in period ÷ Customers at start of period × 100 |
| **Revenue churn rate** | What share of money we lost | Recurring revenue lost ÷ Recurring revenue at start × 100 |
| **Net revenue churn** | Lost money minus extra money from upgrades | (Lost + Downgrade − Upgrade revenue) ÷ Revenue at start × 100 |
| **Retention rate** | What share stayed | 100 − Customer churn rate |
| **Average customer lifetime** | How long customers stay on average | 1 ÷ Monthly churn rate |
| **Customer lifetime value (LTV), simple** | Total money from an average customer | Average monthly revenue per customer ÷ Monthly churn rate |
| **Trial conversion rate** | Share of trials that pay | Trials converted ÷ Trials ended × 100 |
| **Save rate** | Share of would-be leavers we kept | Save offers accepted ÷ Cancel flows entered × 100 |
| **Reactivation rate** | Share of leavers who come back | Reactivated ÷ Churned × 100 |
| **Time to first value** | How fast customers get the benefit | Median days from signup to `first_value_reached` |
| **Cancel flow completion** | Share who finish cancelling once they start | Cancellations requested ÷ Cancel flows entered |

🟦 **Worked example:** Start of month: 200 customers. During the month 10 left. 
Churn rate = 10 ÷ 200 × 100 = **5%**. Retention = **95%**. Average lifetime = 1 ÷ 0.05 = **20 months**.

⚠️ **Small-number warning:** With fewer than 100 customers, one person leaving moves the percentage a lot. Always show the **count** next to the **percentage** (for example "3 of 60 = 5%").

## 9.2 Choose your headline numbers

**Question:** Pick no more than 5 numbers the team looks at every week.

| # | Metric | Why we chose it | Target | Alarm (too bad) | Owner |
|---|--------|-----------------|--------|-----------------|-------|
| 1 | ✏️ | | | | |
| 2 | ✏️ | | | | |
| 3 | ✏️ | | | | |
| 4 | ✏️ | | | | |
| 5 | ✏️ | | | | |

## 9.3 Metrics scoreboard by milestone (fill in as you grow)

| Metric | Beta | Launch + 30 days | At customer #100 | #250 | #500 |
|--------|------|------------------|-----------------|------|------|
| Customers (count) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Monthly customer churn % | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Monthly revenue churn % | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Voluntary churn % | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Involuntary churn % | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Trial-to-paid % | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Save rate % | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Median time to first value | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| 30-day retention % | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| 90-day retention % | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |

## 9.4 Cohort retention table (customers grouped by signup month)

**Plain meaning:** Group customers by the month they joined. Then see what share is still active 1, 2, 3 months later.

| Signup month | Customers who joined | Still active after 1 month | 2 months | 3 months | 6 months |
|--------------|---------------------|----------------------------|----------|----------|----------|
| ✏️ | ✏️ | ✏️ % | ✏️ % | ✏️ % | ✏️ % |
| ✏️ | ✏️ | ✏️ % | ✏️ % | ✏️ % | ✏️ % |
| ✏️ | ✏️ | ✏️ % | ✏️ % | ✏️ % | ✏️ % |

**Question:** Does the line flatten (good: a loyal core) or keep falling (bad)? 

✏️ Your answer:

## 9.5 What numbers count as "good"? (set your own benchmark)

⚠️ Benchmarks differ a lot by product type and customer size. Do not copy another company's numbers without checking.

| Question | ✏️ Your answer |
|----------|----------------|
| Where did our target numbers come from? (similar product, public report, past project) | |
| Are they for the same type of customer (small company vs large, consumer vs business)? | |
| Date benchmarks were last checked | |

---

# PART 10. ANALYSIS PLAN (HOW WE FIND THE "WHY")

**Status:** `NOT STARTED`
**Goal:** Turn raw cancellations into a ranked list of reasons and fixes.
**When to fill in:** Plan at Beta; run monthly after launch (weekly for the first 100 customers).
⏱️ 60 minutes

## 10.1 The five questions we ask every month

1. **How many** customers left, and what did it cost us?
2. **Who** left? (which plan, size, source, country, age of account)
3. **When** did they leave? (first week? after the first bill? at renewal?)
4. **Why** did they say they left? And does their behavior agree?
5. **What** will we change, and by when?

## 10.2 Slice the data (groups to compare)

| Slice | Why it matters | Do we have this data? (Yes/No) |
|-------|----------------|---------------------------------|
| Plan or price | Do cheap or expensive plans leave more? | ✏️ |
| How they found us (channel, campaign) | Do some sources bring poor-fit customers? | ✏️ |
| Customer size or type | Do small or big customers leave more? | ✏️ |
| Country or region | Is there a local problem? | ✏️ |
| Device or platform | Is one platform worse? | ✏️ |
| Signup month (cohort) | Did a change help or hurt? | ✏️ |
| Months since signup (tenure) | When is the danger zone? | ✏️ |
| Onboarding completed or not | Does setup predict staying? | ✏️ |
| Reached first value or not | Does it predict staying? | ✏️ |
| Number of support tickets | Do unhappy customers leave? | ✏️ |
| Billing cycle (monthly / yearly) | Do monthly customers leave faster? | ✏️ |

## 10.3 Reason ranking table (update monthly)

| Rank | Reason code | Count this month | % of all cancellations | Revenue lost | Trend (up / down / same) | Fix planned |
|------|-------------|------------------|------------------------|--------------|--------------------------|-------------|
| 1 | ✏️ | | | | | |
| 2 | ✏️ | | | | | |
| 3 | ✏️ | | | | | |
| 4 | ✏️ | | | | | |
| 5 | ✏️ | | | | | |

## 10.4 "Says" vs "does" check

**Plain meaning:** What customers **say** (survey) and what they **do** (usage) can differ. Example: "too expensive" is often really "not using it enough."

| Reason they gave | What their behavior shows | Do they match? | Likely real cause |
|------------------|---------------------------|----------------|-------------------|
| ✏️ | ✏️ | | |
| ✏️ | ✏️ | | |

## 10.5 Find the "stay signals" (what happy customers do early)

**Question:** Compare customers who stayed 90+ days with those who left in under 30. What did the stayers do in the first 7 days?

| First-week action | % of stayers who did it | % of leavers who did it | Difference |
|-------------------|-------------------------|--------------------------|------------|
| ✏️ | | | |
| ✏️ | | | |
| ✏️ | | | |

⚠️ **Careful:** Doing something together with staying does not prove the action caused staying. Test it (Part 15) before you bet the product on it.

## 10.6 Root-cause method ("5 Whys")

For your #1 reason, ask "why?" five times.

🟦 *Example: Reason = "not using enough". Why? They forgot it. Why? No reminders. Why? We never built reminders. Why? We assumed customers would log in daily. Why? We never checked how they really work. → Fix: build reminders and check real behavior.*

| Why # | ✏️ Your answer |
|-------|----------------|
| 1 | |
| 2 | |
| 3 | |
| 4 | |
| 5 | |

**Root cause in one sentence:** ✏️

## 10.7 Monthly analysis report (copy this block each month)

```
MONTH: [Month Year]
CUSTOMERS AT START: [number]    LOST: [number]    CHURN %: [number]
VOLUNTARY: [number]   INVOLUNTARY: [number]   TRIAL DROP-OFF: [number]
TOP 3 REASONS: 1) [ ]  2) [ ]  3) [ ]
BIGGEST SURPRISE: [one sentence]
WHAT WE CHANGED LAST MONTH: [list]  DID IT WORK? [yes/no/too early]
WHAT WE WILL CHANGE NEXT: [list with owner and date]
DATA PROBLEMS FOUND: [list or "none"]
```

---

# PART 11. DASHBOARDS AND ALERTS

**Status:** `NOT STARTED`
**Goal:** Put the key numbers where everyone can see them, and ring a bell when something goes wrong.
**When to fill in:** Plan in Build; turn on by Launch.
⏱️ 40 minutes

## 11.1 Dashboard list

| Dashboard name | Who looks at it | How often | Tool | Link | Status |
|----------------|-----------------|-----------|------|------|--------|
| Churn overview (headline numbers) | ✏️ | ✏️ weekly | ✏️ | ✏️ | ⬜ |
| Cancellation reasons | ✏️ | ✏️ | ✏️ | ✏️ | ⬜ |
| Cohort retention | ✏️ | ✏️ | ✏️ | ✏️ | ⬜ |
| Payment failures and recovery | ✏️ | ✏️ | ✏️ | ✏️ | ⬜ |
| Trial funnel | ✏️ | ✏️ | ✏️ | ✏️ | ⬜ |
| At-risk customers list | ✏️ | ✏️ | ✏️ | ✏️ | ⬜ |

## 11.2 Every chart must answer a question

| Chart | The question it answers | Type (line, bar, table) |
|-------|-------------------------|--------------------------|
| ✏️ | ✏️ | ✏️ |
| ✏️ | ✏️ | ✏️ |
| ✏️ | ✏️ | ✏️ |

## 11.3 Alerts (the "bell")

| Alert name | Triggers when | Sent to | Channel | Action to take |
|------------|---------------|---------|---------|-----------------|
| Cancellation spike | More than ✏️ [N] cancellations in 24 hours | ✏️ | ✏️ | ✏️ |
| Payment failure spike | Failed payment rate above ✏️ % | ✏️ | ✏️ | ✏️ |
| Tracking broke | Zero `subscription_cancelled` events when billing shows some | ✏️ | ✏️ | ✏️ |
| Big customer at risk | High-value customer opens cancel flow | ✏️ | ✏️ | ✏️ |
| Reason "bugs_or_errors" rising | Share above ✏️ % | ✏️ | ✏️ | ✏️ |

## 11.4 Meeting rhythm

| Meeting | When | Who | What we look at | Output |
|---------|------|-----|-----------------|--------|
| Churn check-in | ✏️ weekly | ✏️ | Dashboard 11.1 #1 and #2 | Short notes |
| Monthly churn review | ✏️ | ✏️ | Part 10.7 report | Decisions and owners |
| 500-customer review | When customer #500 arrives | ✏️ | Part 19 | Lessons for next project |

---

# PART 12. PREVENTION AND WIN-BACK PLAN

**Status:** `NOT STARTED`
**Goal:** Decide what we do **before** customers leave (prevent) and **after** (win back).
**When to fill in:** Plan at Launch; build the automated parts between customer #100 and #500.
⏱️ 45 minutes

## 12.1 Prevention ideas checklist (tick what you will do)

- ⬜ Make setup shorter and clearer (fix the biggest onboarding drop)
- ⬜ Help new customers reach first value within [N] days
- ⬜ Send tips emails for the core action
- ⬜ Offer a yearly plan with a fair discount
- ⬜ Offer a pause instead of cancel
- ⬜ Offer a cheaper plan instead of cancel
- ⬜ Fix the top 3 bugs customers mention
- ⬜ Speed up support replies
- ⬜ Reach out personally to at-risk customers
- ⬜ Ask for feedback at day 7, 30, 90
- ⬜ Card-expiry reminders (see Part 6)
- ⬜ Share customer success stories
- ⬜ Add missing feature that appears in `missing_feature` reasons
- ⬜ Other: ✏️

## 12.2 Prevention action plan (top 5)

| # | Action | Reason it fights | Owner | Due date | How we measure it worked | Status |
|---|--------|------------------|-------|----------|--------------------------|--------|
| 1 | ✏️ | | | | | |
| 2 | ✏️ | | | | | |
| 3 | ✏️ | | | | | |
| 4 | ✏️ | | | | | |
| 5 | ✏️ | | | | | |

## 12.3 Win-back plan (getting leavers to return)

| Question | ✏️ Your answer |
|----------|----------------|
| Which leavers do we contact? (by reason) | |
| Which leavers do we NOT contact? (asked not to be; privacy rule) | |
| When do we contact them? (days after leaving) | |
| What is different now? (new feature, fix, price) | |
| What offer, if any? | |
| How do we count a win-back? | |
| Target win-back rate | |

| Message | Days after churn | Reason group | Subject / main line |
|---------|------------------|--------------|---------------------|
| Win-back 1 | 7 | ✏️ | ✏️ |
| Win-back 2 | 30 | ✏️ | ✏️ |
| Win-back 3 | 90 | ✏️ | ✏️ |

🔒 **Always include an easy "unsubscribe" in win-back messages.**

---

# PART 13. PRIVACY, CONSENT, AND FAIRNESS

**Status:** `NOT STARTED`
**Goal:** Protect customers and protect us. Collect only what we need, and handle it safely.
**When to fill in:** Before collecting any data (Build stage at the latest).
⏱️ 30 minutes

⚠️ This Part is a checklist, **not legal advice.** Ask a qualified person (lawyer or privacy officer) to review it.

## 13.1 What personal data do we collect for churn analysis?

| Data | Why we need it | Where stored | How long kept | Who can see it |
|------|----------------|--------------|---------------|----------------|
| Customer ID | Join data | ✏️ | ✏️ | ✏️ |
| Email | Contact about cancellation or win-back | ✏️ | ✏️ | ✏️ |
| Cancel reason | Learn why | ✏️ | ✏️ | ✏️ |
| Free-text comments | Learn why in detail | ✏️ | ✏️ | ✏️ |
| Usage events | Spot warning signs | ✏️ | ✏️ | ✏️ |
| Payment failure reason | Fix billing | ✏️ | ✏️ | ✏️ |
| Interview notes | Learn why | ✏️ | ✏️ | ✏️ |
| ✏️ | | | | |

## 13.2 Checklist

| Item | Yes / No / N/A | Notes |
|------|----------------|-------|
| We tell customers what we track (privacy policy updated) | ✏️ | |
| We have the needed consent for tracking and marketing messages | ✏️ | |
| Customers can ask to see or delete their data | ✏️ | |
| We never store full card numbers (the payment provider does) | ✏️ | |
| Free-text comments are checked for personal data before sharing | ✏️ | |
| Raw personal data is NOT pasted into AI tools without approval | ✏️ | |
| Access to churn data is limited to those who need it | ✏️ | |
| Data is deleted or anonymized after the keep-time ends | ✏️ | |
| Rules for each country where we have customers are checked (for example EU/UK, California, others) | ✏️ | |
| Rules about easy cancellation and auto-renewal are checked for each country or state where we sell | ✏️ | |
| Customers who ask not to be contacted are marked and skipped | ✏️ | |
| Data sent to third-party tools is listed (who gets what) | ✏️ | |

## 13.3 AI agent and privacy rules 🔒

1. Give AI agents **IDs and counts**, not names or emails, unless approved.
2. Remove personal details from comments before analysis.
3. Log what data an AI agent used.
4. A human must approve any message an AI sends to a customer.

✏️ Who is our privacy contact? 

---

# PART 14. ROLES AND OWNERS (WHO DOES WHAT)

**Status:** `NOT STARTED`
**Goal:** Every task has exactly one owner.
**When to fill in:** Idea stage. Update when the team changes.
⏱️ 15 minutes

**Legend:** **R** = Does the work. **A** = Final say (only ONE per row). **C** = Must be asked. **I** = Must be told.

| Task | Product | Engineer | Data analyst | Support | Marketing | Founder / Lead | AI agent |
|------|---------|----------|--------------|---------|-----------|----------------|----------|
| Agree definitions (Part 2) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Approve tracking plan (Part 4) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Build tracking | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Build cancel flow (Part 5) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Handle exit interviews | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Fix failed payments (Part 6) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Build dashboards (Part 11) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Monthly churn report (Part 10.7) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Run experiments (Part 15) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Win-back messages (Part 12) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Privacy review (Part 13) | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |
| Keep this document updated | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ | ✏️ |

🟦 *Example row: "Build tracking" → Engineer = R, Product = A, Analyst = C, Founder = I.*

## 14.1 People list

| Name or role | Responsible for | How to reach | Backup person |
|--------------|-----------------|--------------|----------------|
| ✏️ | | | |
| ✏️ | | | |
| ✏️ | | | |

---

# PART 15. EXPERIMENTS (TEST BEFORE YOU BET)

**Status:** `NOT STARTED`
**Goal:** Try one change at a time and measure honestly.
**When to fill in:** After about 100 customers (with fewer, talk to people instead).
⏱️ 30 minutes per experiment

⚠️ **Small-number warning:** With under about 100 customers, tests rarely give clear answers. Prefer interviews and quick fixes. Use experiments more after 100 to 200 customers.

## 15.1 Experiment backlog

| # | Idea | Reason it fights | Expected effect | Effort (S/M/L) | Priority |
|---|------|------------------|-----------------|----------------|----------|
| 1 | ✏️ | | | | |
| 2 | ✏️ | | | | |
| 3 | ✏️ | | | | |

## 15.2 Experiment card (copy one per experiment)

```
EXPERIMENT NAME: [short name]
OWNER: [name]                 START DATE: [date]       END DATE: [date]
THE PROBLEM: [what is going wrong, with numbers]
OUR GUESS (HYPOTHESIS): "If we [change], then [metric] will [go up/down] by [amount], because [reason]."
WHO IS INCLUDED: [group]      HOW MANY: [number]
WHO IS NOT INCLUDED: [group]
GROUPS: Control (no change) vs Test (change). Split: [50/50 or other]
MAIN NUMBER WE WATCH: [metric]
SAFETY NUMBERS (must not get worse): [metrics]
HOW LONG WE RUN IT: [days] (decide BEFORE starting; no peeking and stopping early)
WHAT RESULT MEANS "SHIP IT": [rule]
WHAT RESULT MEANS "STOP": [rule]
RESULT: [numbers]
DECISION: [ship / stop / run again]
WHAT WE LEARNED: [one or two sentences]
```

## 15.3 Rules for fair tests

1. Change **one thing** at a time.
2. Choose who gets the change **randomly**.
3. Decide how long it runs and what "success" means **before** you start.
4. Do not stop early because it "looks good."
5. Write down the result even if it failed.

---

# PART 16. AI PROMPT LIBRARY (COPY, PASTE, FILL IN)

**Status:** `NOT STARTED`
**Goal:** Ready-made instructions that give AI agents the right context, so they don't guess.
**When to fill in:** Any time. Replace every `[brackets]` before use. 🔒 Remove personal data first.

## 16.1 Prompt: complete this document

```
You are a careful analyst. Read Churn_and_Cancellation_Analysis.md, starting with
Part A (AI rules). Fill in only Part [number], using ONLY the facts I give you
below. If a fact is missing write UNKNOWN and list the exact question for me.
Label any guess as ASSUMPTION. Keep the format and the ✏️ markers.

FACTS:
[paste facts, with sources and dates]
```

## 16.2 Prompt: group exit-survey comments into reasons

```
Below are anonymized free-text cancellation comments. For each comment:
1) pick ONE reason code from Part 5.3 (or "other" and say why),
2) give a one-line summary,
3) note if it mentions a competitor, a bug, a price, or a missing feature.
Then show a table: reason code, count, % of total, and two short example summaries
(not full quotes). Do not invent reasons. If a comment is unclear, mark UNCLEAR.

COMMENTS (anonymized, one per line with an ID):
[paste]
```

## 16.3 Prompt: monthly churn report

```
Using ONLY the data below, write the monthly report in the format in Part 10.7.
Show counts next to percentages. If a number is missing, write UNKNOWN. Flag any
number that looks odd (for example billing and analytics disagree by more than 2%).
Do not explain causes unless the data supports it; otherwise say "needs investigation."

DATA:
[paste counts, tables]
```

## 16.4 Prompt: turn the tracking plan into code tasks

```
Read Part 4 of Churn_and_Cancellation_Analysis.md. For each event with status
PLANNED, create a task with: event name, where it fires (frontend or backend),
required properties, a test that proves it fires once and only once, and an
acceptance check ("event appears in [analytics tool] within 5 minutes with all
required properties"). List any event whose firing moment is unclear as a QUESTION.
Do not rename events.
```

## 16.5 Prompt: audit this document for gaps

```
Review Churn_and_Cancellation_Analysis.md. List:
1) every UNKNOWN, blank ✏️ answer, and unreplaced [bracket],
2) every place two Parts disagree (for example different definitions of churn),
3) every ASSUMPTION without an entry in Part 18,
4) every event in Part 4 not used by any metric in Part 9.
Output a table: location, problem, suggested question for the owner.
```

## 16.6 Prompt: draft a save or win-back message

```
Write 3 short, honest, friendly versions of a [save offer / win-back] message.
Audience: customers who left because [reason code]. What is new or different: [facts].
Offer (if any): [offer]. Rules: no pressure or guilt, no false urgency, plain words,
include an easy way to opt out, under [120] words. Do not send; a human approves.
```

## 16.7 Prompt: find early warning signs

```
Here is a table of customers (IDs only) with columns: stayed_or_left, and counts of
actions in their first 7 days: [list columns]. Compare the two groups. Show which
actions differ most. Remind me that this shows association, not proof of cause, and
suggest one experiment for the top difference.
```

---

# PART 17. QUALITY ASSURANCE (IS EVERYTHING REALLY DONE?)

**Status:** `NOT STARTED`
**Goal:** Prove the document is complete, and the tracking actually works.
**When to fill in:** Before Beta, before Launch, and before the 500-customer review.
⏱️ 60 minutes

## 17.1 Document completeness check

| Check | Pass? |
|-------|-------|
| Every Part has a Status other than `NOT STARTED` (or is marked `NOT APPLICABLE` with a reason) | ⬜ |
| No `[brackets]` remain | ⬜ |
| Every `UNKNOWN` has a matching line in Part 18 | ⬜ |
| Every `ASSUMPTION` has a matching line in Part 18 | ⬜ |
| Part 2 definitions match how Parts 9 and 11 calculate numbers | ⬜ |
| Every event in Part 4 is used by at least one metric, dashboard, or alert, or marked as future use | ⬜ |
| Every reason code in Part 5.3 appears in the dashboard | ⬜ |
| Every owner in Part 14 is a real, reachable person | ⬜ |
| Privacy checklist (Part 13) reviewed by a qualified person | ⬜ |
| A new person could read this and explain the plan without asking anyone | ⬜ |

## 17.2 Tracking test script (do this in a test environment, then in production with a test account)

| # | Test | Expected result | Passed? | Tester | Date |
|---|------|-----------------|---------|--------|------|
| 1 | Create a test account | `account_created` appears once | ⬜ | ✏️ | |
| 2 | Finish onboarding | `onboarding_completed` appears once | ⬜ | | |
| 3 | Do the core action | `core_action_completed` appears with correct properties | ⬜ | | |
| 4 | Start a trial | `trial_started` appears | ⬜ | | |
| 5 | Pay | `subscription_started` and `payment_succeeded` appear; match billing | ⬜ | | |
| 6 | Make a payment fail (use payment provider's test card) | `payment_failed` with a reason; dunning message sent | ⬜ | | |
| 7 | Fix the card | `payment_method_updated` appears; subscription continues | ⬜ | | |
| 8 | Open the cancel page and leave | `cancel_flow_entered`, `cancel_flow_abandoned` | ⬜ | | |
| 9 | Go through cancel flow, pick a reason | `cancel_reason_selected` has a valid code | ⬜ | | |
| 10 | Decline the save offer, confirm cancel | `save_offer_declined`, `cancellation_requested` | ⬜ | | |
| 11 | Reach the effective date | `subscription_cancelled` from backend, one time only | ⬜ | | |
| 12 | Reverse a cancellation | `cancellation_reversed` appears; subscription active | ⬜ | | |
| 13 | Cancel via support | Reason code recorded by agent | ⬜ | | |
| 14 | Reactivate | `subscription_reactivated` appears | ⬜ | | |
| 15 | Check counts vs billing tool | Within allowed difference (Part 4.9) | ⬜ | | |
| 16 | Check test data excluded from dashboards | Test events not in reports | ⬜ | | |
| 17 | Block tracking in browser (ad blocker) | Money and cancel events still arrive from backend | ⬜ | | |
| 18 | Alerts fire when you simulate a spike | Alert received by right person | ⬜ | | |

## 17.3 Number sanity checks (every month)

| Check | Pass? |
|-------|-------|
| Customers at start + new − lost = customers at end | ⬜ |
| Sum of reason counts = total cancellations (include `no_reason_given`) | ⬜ |
| Voluntary + involuntary + trial drop-off = total lost (as defined in Part 2) | ⬜ |
| Percentages shown with counts | ⬜ |
| Same time zone and same date range in every chart | ⬜ |
| Duplicate events checked | ⬜ |

## 17.4 Release gates (do not move on until all are ticked)

| Gate | Requirements | Approved by | Date |
|------|--------------|-------------|------|
| Build → Beta | Parts 1–6 done; tracking tested (17.2 #1–16) | ✏️ | |
| Beta → Launch | Dashboards and alerts working; privacy checklist done; 90% of beta cancellations have reasons | ✏️ | |
| Launch → Scale (after 100 customers) | Top 3 reasons known; one fix shipped; monthly report running | ✏️ | |
| Close at 500 customers | Part 19 complete; lessons saved | ✏️ | |

---

# PART 18. RISKS, ASSUMPTIONS, AND OPEN QUESTIONS

**Status:** `NOT STARTED`
**Goal:** One place for everything we are unsure about, so nothing hides.
**When to fill in:** Continuously.

## 18.1 Open questions (every `UNKNOWN` goes here)

| # | Question | Where in the document | Who can answer | Needed by | Answer | Closed? |
|---|----------|-----------------------|----------------|-----------|--------|---------|
| 1 | ✏️ | | | | | ⬜ |
| 2 | ✏️ | | | | | ⬜ |
| 3 | ✏️ | | | | | ⬜ |

## 18.2 Assumptions (every guess goes here)

| # | Assumption | Why we believe it | How we will check | Check by | Result |
|---|-----------|-------------------|-------------------|----------|--------|
| 1 | ✏️ | | | | |
| 2 | ✏️ | | | | |

## 18.3 Risks

| # | What could go wrong | How likely (Low/Med/High) | How bad (Low/Med/High) | What we do to prevent it | What we do if it happens | Owner |
|---|--------------------|----------------------------|-------------------------|--------------------------|---------------------------|-------|
| 1 | 🟦 Tracking breaks after an app update and cancellations stop being recorded | Med | High | Alert when billing and analytics disagree | Fix and backfill from billing data | ✏️ |
| 2 | 🟦 Too few customers to see patterns | High | Med | Talk to every leaver | Use interviews instead of numbers | ✏️ |
| 3 | 🟦 Cancel flow feels sneaky and hurts trust | Low | High | Follow Part 5.1 | Simplify flow | ✏️ |
| 4 | ✏️ | | | | | |
| 5 | ✏️ | | | | | |

---

# PART 19. THE 500-CUSTOMER REVIEW (CLOSE-OUT AND LESSONS)

**Status:** `NOT STARTED`
**Goal:** When customer #500 arrives, look back, record what we learned, and improve the template for the next project.
**When to fill in:** Within 2 weeks of reaching 500 customers.
⏱️ 2 hours

## 19.1 The journey in numbers

| Question | ✏️ Your answer |
|----------|----------------|
| Date of customer #1 | |
| Date of customer #500 | |
| Days it took | |
| Total customers ever acquired | |
| Customers lost along the way | |
| Customers active today | |
| Final monthly churn rate | |
| Biggest churn rate we saw, and when | |
| Best churn rate we saw, and when | |
| Trial-to-paid rate (final) | |
| Total reactivations | |

## 19.2 What did customers tell us?

| Rank | Top reasons (final) | Count | % | Did we fix it? (Yes / Partly / No) |
|------|---------------------|-------|---|--------------------------------------|
| 1 | ✏️ | | | |
| 2 | ✏️ | | | |
| 3 | ✏️ | | | |
| 4 | ✏️ | | | |
| 5 | ✏️ | | | |

## 19.3 What worked and what didn't

| Change we made | Date | Result (with numbers) | Keep, change, or drop? |
|----------------|------|------------------------|--------------------------|
| ✏️ | | | |
| ✏️ | | | |
| ✏️ | | | |

## 19.4 Retrospective questions

1. **What surprised us most about why people left?** ✏️
2. **Which number misled us at first?** ✏️
3. **Which events did we track that we never used?** ✏️
4. **Which events did we wish we had tracked from day 1?** ✏️
5. **Was our definition of churn (Part 2) right? What would we change?** ✏️
6. **Did the cancel flow feel fair to customers? Evidence?** ✏️
7. **What would we do in the first 30 days differently?** ✏️
8. **Which AI prompts saved the most time? Which gave bad results?** ✏️
9. **Where did the AI agent guess or make mistakes?** ✏️
10. **What question in this template was confusing, missing, or useless?** ✏️

## 19.5 Next 90 days

| Goal | Metric | Target | Owner | Due |
|------|--------|--------|-------|-----|
| ✏️ | | | | |
| ✏️ | | | | |
| ✏️ | | | | |

## 19.6 Improve this template (so the next project is easier)

| Change to template | Part affected | Suggested by | Approved? |
|--------------------|---------------|--------------|-----------|
| ✏️ | | | ⬜ |

---

# PART 20. GLOSSARY (HARD WORDS MADE EASY)

| Word | Simple meaning |
|------|----------------|
| **Account** | A company or group that uses the product. It can have many users. |
| **Active customer** | A customer who counts as "still with us" by the rule in Part 2. |
| **Alert** | An automatic message that says "something looks wrong." |
| **Analytics tool** | Software that stores and shows what customers do in the product. |
| **Assumption** | A guess we are treating as true for now. |
| **Backend** | The behind-the-scenes server part of the product. |
| **Benchmark** | A "normal" number from similar products, used for comparison. |
| **Billing cycle** | How often a customer pays (monthly, yearly). |
| **Cancellation** | A customer asking to stop. |
| **Churn** | Customers or money lost over a time period. |
| **Cohort** | A group of customers who joined in the same period. |
| **Control group** | The group that does not get the change in an experiment. |
| **Core action** | The main thing happy customers do again and again. |
| **Dashboard** | A screen with charts and key numbers. |
| **Downgrade** | Moving to a cheaper plan. |
| **Dunning** | Messages and retries that try to fix a failed payment. |
| **Event** | A note the product writes when something happens. |
| **Experiment (A/B test)** | A fair test comparing two versions. |
| **First value** | The first time a customer gets the benefit they wanted. |
| **Freemium** | A free plan plus an optional paid plan. |
| **Frontend** | What the customer sees on the screen. |
| **Grace period** | Extra days we wait after a failed payment before cutting access. |
| **Health score** | A number showing how likely a customer is to stay. |
| **Hypothesis** | A clear guess we can test. |
| **Involuntary churn** | Leaving because of a payment problem, not by choice. |
| **LTV (lifetime value)** | Total money a customer is expected to bring us. |
| **Logo churn** | Churn counted by number of customers, not money. |
| **MRR** | Monthly recurring revenue: the subscription money we expect each month. |
| **Net revenue churn** | Lost money minus extra money from upgrades. |
| **NPS** | A 0 to 10 question: "How likely are you to recommend us?" |
| **Onboarding** | The setup steps a new customer goes through. |
| **Pause** | Temporarily stopping a subscription. |
| **Property** | A detail attached to an event (for example, which plan). |
| **Reactivation** | A former customer coming back. |
| **Reason code** | A fixed label for why someone left. |
| **Retention rate** | The share of customers who stayed. |
| **Revenue churn** | Churn counted by money lost. |
| **Save offer** | An honest offer made to a customer thinking of leaving. |
| **Silent churn** | A customer who stopped using the product but has not cancelled. |
| **Source of truth** | The one system we trust when numbers disagree. |
| **Tenure** | How long a customer has been with us. |
| **Tracking plan** | The list of all events and properties (Part 4). |
| **Trial** | A free try-out period. |
| **Voluntary churn** | A customer chose to leave. |
| **Webhook** | An automatic message one system sends to another when something happens. |
| **Win-back** | Getting a former customer to return. |

---

# PART 21. FINAL SIGN-OFF AND CHANGE LOG

## 21.1 Sign-off

| Role | Name | Date | Signature or "Approved" |
|------|------|------|--------------------------|
| Document owner | ✏️ | | |
| Product lead | ✏️ | | |
| Engineering lead | ✏️ | | |
| Data / analytics lead | ✏️ | | |
| Privacy reviewer | ✏️ | | |

## 21.2 Change log (add a line every time you change something important)

| Date | Version | Who | What changed | Why |
|------|---------|-----|--------------|-----|
| ✏️ | 1.0 | ✏️ | First version | |
| | | | | |
| | | | | |

## 21.3 Last check before you share this file

- ⬜ I replaced every `[bracket]`.
- ⬜ I wrote `UNKNOWN` instead of leaving blanks, and logged each in Part 18.
- ⬜ I removed any real names, emails, or card details. 🔒
- ⬜ I updated the Status line of every Part I touched.
- ⬜ I updated the YAML summary in Part A.5.
- ⬜ I added a line to the change log.
- ⬜ I ran the QA checklist (Part 17) for my current stage.

**🎉 When all boxes are ticked, you are ready to go.**
