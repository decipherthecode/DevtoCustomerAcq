<!--
TEMPLATE VERSION: 1.0
HOW TO REUSE: Copy this file into a new project, then fill it in top to bottom.
Delete nothing. If a section does not apply, write "N/A because ..." (see Rule 3).
-->

# How to Fill This Document (Read First)

**What this file is:** One place to plan, build, launch, and track how your product gets its **first 500 customers**. You fill it in by answering questions. Nobody has to guess, because every question has an example.

**Who can fill it in:** A solo founder, a small team, an AI agent, or a beginner. If you can read and type, you can do this.

## The 7 Rules

1. **Go top to bottom.** Phases go in order: Define → Instrument → Launch → Acquire. Do not skip ahead.
2. **Type your answer on the line that says `ANSWER:`.** Keep each answer short: one to three sentences, or a table row.
3. **Never leave a blank.** If you don't know, write `UNKNOWN - who will find out - by when`. If a question doesn't apply, write `N/A - because ...`.
4. **Use numbers, not feelings.** Write "50 sign-ups per week", not "a lot".
5. **Set the status badge** at the top of every section: `⬜ Not started` → `🟨 In progress` → `✅ Done` → `🔒 Approved` (a human signed off).
6. **Stop at every 🛑 Approval Gate.** A human must say yes before moving on (spending money, switching on tracking, launching).
7. **Write down every big change** in the Decision & Change Log at the bottom (who, what, why).

## Words You Might Not Know (Glossary)

| Word | Simple meaning |
|---|---|
| **Customer** | A person or company that did the one action you decide counts (you choose it in Q1.1) |
| **Funnel** | The steps a person walks through: visits → signs up → tries → pays |
| **Event** | A tiny note your product records when someone does something (e.g., "clicked Sign Up") |
| **Activation** | The first moment a user gets real value ("aha!") |
| **Channel** | Where customers come from (search, friends, ads, social media, etc.) |
| **CAC** | Customer Acquisition Cost = money spent ÷ customers gained |
| **Conversion rate** | Of 100 people at one step, how many reach the next step |
| **Retention / Churn** | Retention = people who stay. Churn = people who leave |
| **UTM tag** | A label added to a link so you know which post or ad it came from |
| **PII** | Personal info that identifies someone (name, email, phone) |
| **Consent** | A clear "yes" from the person to be tracked |
| **QA** | Testing to make sure things work |
| **Go / No-Go** | The final yes or no before launch |

## Instructions for AI Agents (Mandatory)

If you are an AI agent reading or editing this file:

- **Read the whole file first.** Treat the `project_summary` block and approved (🔒) sections as the source of truth.
- **Never invent facts.** If an answer is blank or `UNKNOWN`, ask the human. Do not fill it with a guess.
- **Never pass a 🛑 Approval Gate** on your own. Prepare the work, then stop and request human approval.
- **Never collect, store, or write real personal data** (names, emails, phone numbers) into this file.
- **Update only what you were asked to.** Keep wording simple. Keep the example lines.
- **Log every change** in the Decision & Change Log with `Actor: AI-agent` and the reason.
- **Mark your work `🟨 In progress`.** Only a human sets `🔒 Approved`.
- **Check your work:** numbers add up, dates make sense, every event name matches the Tracking Plan exactly.

---

# Customer Acquisition Tracker

## Project Summary (Machine-Readable)

> Fill this in last, after the sections below. AI agents read this block first.

```yaml
project_summary:
  project_name: ""            # Example: "PlantPal"
  product_type: ""            # B2C app | B2B SaaS | Mobile app | Marketplace | Other
  owner_name: ""              # Human who is responsible
  start_date: ""              # YYYY-MM-DD
  target_launch_date: ""      # YYYY-MM-DD
  actual_launch_date: ""      # YYYY-MM-DD or UNKNOWN
  customer_definition: ""     # Copy from Q1.1
  goal_customers: 500
  customers_to_date: 0
  current_phase: ""           # 1-Define | 2-Instrument | 3-Launch | 4-Acquire | Done
  analytics_tool: ""
  top_channel: ""
  monthly_budget: ""          # With currency
  last_updated: ""            # YYYY-MM-DD
  last_updated_by: ""         # Human name or AI-agent
```

## Document Status Board

| # | Section | Status | Approved by (name + date) |
|---|---|---|---|
| 0 | Project Basics | ⬜ Not started | |
| 1 | Define & Plan | ⬜ Not started | |
| 2 | Instrument & Build | ⬜ Not started | |
| 3 | Test & Launch | ⬜ Not started | |
| 4 | Acquire 0 to 500 | ⬜ Not started | |
| 5 | Risks & Blockers Log | ⬜ Not started | |
| 6 | Final Retro | ⬜ Not started | |

---

## Section 0: Project Basics

**Status:** ⬜ Not started

**Q0.1 What is your product called, and what does it do in one sentence?**
*Example: "PlantPal is a phone app that reminds people when to water their plants."*
ANSWER:

**Q0.2 Which type of product is it?** (Pick one: B2C app/SaaS, B2B SaaS, Mobile app, Marketplace, Other)
*Example: "Mobile app."*
ANSWER:

**Q0.3 Who is responsible for this document, and who else helps?**
*Example: "Owner: Sam (founder). Helpers: Priya (marketing), AI-agent (data setup)."*

| Name | Role | Can approve gates? (Yes/No) |
|---|---|---|
| | | |

**Q0.4 What is your launch date, and what is the date you want 500 customers by?**
*Example: "Launch 2026-12-01. 500 customers by 2027-03-01."*
ANSWER:

**Q0.5 How much money and time can you spend each month on getting customers?**
*Example: "$300 and 10 hours per week."*
ANSWER:

---

## Section 1: Define & Plan

**Status:** ⬜ Not started
**Goal of this phase:** Decide exactly what you are counting and who you are trying to reach, before you build anything.

**Q1.1 What counts as ONE customer for this project?** (Pick one. Lock it in. Do not change it later without writing it in the Change Log.)
- Option A: Signed up (made an account)
- Option B: Activated (did the first important action)
- Option C: Paying (made a first payment)
- Option D: Other (describe it)

*Example: "Option B. A customer is someone who adds their first plant and gets one reminder."*
ANSWER:

**Q1.2 Who is your ideal customer?** (Age or job, the problem they have, where they spend time online or offline.)
*Example: "Adults 25-40 who keep killing houseplants. They use Instagram and Reddit."*
ANSWER:

**Q1.3 What problem do you solve for them, and why would they pick you over what they use now?**
*Example: "Plants die because people forget. Alternative is a calendar note; we are simpler and send smart reminders."*
ANSWER:

**Q1.4 Write the steps a person takes from first hearing about you to becoming a customer (your funnel).**
*Example: "Sees post → visits site → downloads app → creates account → adds first plant → gets first reminder."*

| Step # | What the person does | Event name (from Section 2) |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |
| 5 | | |

**Q1.5 What numbers mean success?** Fill in each line. If unsure, write your best estimate and mark it `(estimate)`.

| Measure | Target | How sure are you? (Low/Med/High) |
|---|---|---|
| Total customers | 500 | High |
| Customers per week needed | | |
| Visitor → sign-up conversion rate | | |
| Sign-up → customer conversion rate | | |
| Maximum cost per customer (CAC) | | |
| Customers still active after 30 days (retention) | | |

**Q1.6 Which channels will you use to find customers?** (Pick 2 to 4 to start. More is harder to track.)
*Example channels: search engines, social media, friends and family, referrals, email, paid ads, partnerships, communities, events, cold outreach, app store.*

| Channel | Why it fits your customer | Weekly time/money | Owner |
|---|---|---|---|
| | | | |

**Q1.7 How will you label links so you know where each customer came from (UTM naming rule)?**
*Example: "utm_source=instagram, utm_medium=social, utm_campaign=launch-week. All lowercase, dashes not spaces."*
ANSWER:

**Q1.8 Which questions must your data answer?**
*Example: "Which channel brings the most customers? Where do people quit the funnel? How much does each customer cost?"*
ANSWER:

### 🛑 Approval Gate 1: Plan Approved

- [ ] Customer definition (Q1.1) is clear and written once
- [ ] Targets (Q1.5) are filled in (estimates are marked)
- [ ] Budget (Q0.5) is confirmed
- [ ] Human approver name and date: ______________________

---

## Section 2: Instrument & Build

**Status:** ⬜ Not started
**Goal of this phase:** Set up the "counting machine" so every important action is recorded correctly.

**AI-agent tasks here:** Draft the event list, write tracking code or config, create dashboards, run data checks.
**Human must approve:** Which tool is used, which data is collected, and switching tracking on in the live product.

**Q2.1 Which tools will you use to count and look at your data?** (Tool-neutral: write any tool you like.)
*Examples: Google Analytics 4, Mixpanel, PostHog, Amplitude, Plausible, a simple spreadsheet, your database.*

| Job | Tool chosen | Cost | Who sets it up |
|---|---|---|---|
| Count website/app actions | | | |
| Look at charts and dashboards | | | |
| Track money/payments | | | |
| Send emails or messages | | | |
| Store customer list (CRM) | | | |
| Track ad spend | | | |

**Q2.2 Write your Tracking Plan: every event you will record.** Use the same names everywhere. Rule: `object_action` in lowercase with underscores.
*Example: `account_created`, `first_plant_added`, `payment_completed`.*

| Event name | When it fires (plain words) | Info saved with it (properties) | Funnel step # | Built? | Tested? |
|---|---|---|---|---|---|
| `page_viewed` | Someone opens a page | page_name, utm_source | 1 | ⬜ | ⬜ |
| `signup_started` | Taps "Sign up" | method | 2 | ⬜ | ⬜ |
| `account_created` | Account is made | method, utm_source | 3 | ⬜ | ⬜ |
| | | | | ⬜ | ⬜ |
| | | | | ⬜ | ⬜ |
| | | | | ⬜ | ⬜ |

**Q2.3 How will you tell one person from another without storing private details?**
*Example: "A random user ID created at sign-up. We never put emails inside events."*
ANSWER:

**Q2.4 Where will tracking be added?** (Website, iOS, Android, backend server, payment system, email tool.)
ANSWER:

**Q2.5 What dashboard will you look at every week, and what 5 numbers are on it?**
*Example: "Weekly dashboard: visitors, sign-ups, customers, cost per customer, 30-day retention."*
ANSWER:

**Q2.6 Who checks that the numbers are right, and how often?**
*Example: "Priya compares dashboard sign-ups with the database every Monday."*
ANSWER:

### Privacy & Consent Checklist (answer Yes, No, or N/A + reason)

| # | Question | Answer |
|---|---|---|
| P1 | Do we ask for permission (consent) before tracking, where the law requires it? | |
| P2 | Is personal info (name, email, phone) kept OUT of event data? | |
| P3 | Is there a privacy policy visible to users? | |
| P4 | Can a user ask us to delete their data, and do we know how? | |
| P5 | Could any users be children under 13 (or under 16 in some regions)? If yes, what is the plan? | |
| P6 | Do we know which laws apply (e.g., GDPR, CCPA, local rules)? List them. | |
| P7 | Is data stored only in places we trust and have chosen on purpose? | |
| P8 | How long do we keep data, and what happens after? | |

> This checklist is a guide, not legal advice. If any answer is "No" or `UNKNOWN`, ask a qualified person before launch.

### 🛑 Approval Gate 2: Tracking Approved to Switch On

- [ ] Tracking Plan (Q2.2) is complete and names are consistent
- [ ] Privacy checklist has no unanswered "No" or `UNKNOWN` items
- [ ] Tools and costs are approved
- [ ] Human approver name and date: ______________________

---

## Section 3: Test & Launch

**Status:** ⬜ Not started
**Goal of this phase:** Prove the counting works, then launch with a clear Go or No-Go.

**AI-agent tasks here:** Run test sign-ups, compare events to the Tracking Plan, list mismatches, draft the launch checklist.
**Human must approve:** The Go / No-Go decision.

### Tracking Test (Do this before launch)

**Q3.1 Walk through your funnel yourself, step by step, with a test account. Did each event show up correctly?**

| Funnel step | Event | Appeared in tool? (Y/N) | Properties correct? (Y/N) | Fix needed |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

**Q3.2 Do the numbers in your analytics tool match your real database or payment system?**
*Example: "10 test sign-ups made; tool shows 10; database shows 10. Match."*
ANSWER:

### Product Readiness Quick Check

- [ ] Main user journey works from start to finish with no errors
- [ ] Sign-up and (if used) payment work on all devices you support
- [ ] Support contact is visible (email or chat) and someone answers it
- [ ] Error reporting is on so you hear about problems
- [ ] Backup or rollback plan exists if something breaks

### Launch Checklist

- [ ] Every channel from Q1.6 has its link, tag (Q1.7), and first post ready
- [ ] Welcome message or email is ready
- [ ] Weekly dashboard (Q2.5) is live
- [ ] Owner for each channel is named and available launch week
- [ ] Customer counter in `project_summary` is set to 0

**Q3.3 What would make you pause or cancel the launch?**
*Example: "If sign-up fails more than 1 in 20 tries, or tracking misses key events."*
ANSWER:

### 🛑 Approval Gate 3: Go / No-Go

- [ ] Tracking test passed
- [ ] Product readiness checks passed
- [ ] Launch checklist done
- Decision (circle): **GO / NO-GO**   Reason: ______________________
- Human approver name and date: ______________________

---

## Section 4: Acquire 0 to 500

**Status:** ⬜ Not started
**Goal of this phase:** Track every customer from #1 to #500, learn what works, and do more of it.

**AI-agent tasks here:** Update the weekly log from dashboard numbers, calculate rates and CAC, flag odd numbers, suggest experiments.
**Human must approve:** Spending money, running paid ads, any message sent to real customers.

**How to use this section:** Fill in one row of the Weekly Log every week on the same day. Update `customers_to_date` in the Project Summary each time.

### 4A. Milestone Ladder (check each one when reached)

| Milestone | Date reached | What we learned |
|---|---|---|
| ☐ Customer #1 | | |
| ☐ Customer #10 | | |
| ☐ Customer #50 | | |
| ☐ Customer #100 | | |
| ☐ Customer #250 | | |
| ☐ Customer #500 🎉 | | |

### 4B. Weekly Log (copy a new row each week)

| Week # | Week starting | Visitors | Sign-ups | New customers | Total customers | Money spent | CAC (spent ÷ new customers) | 30-day retention % | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | | |
| 2 | | | | | | | | | |
| 3 | | | | | | | | | |
| 4 | | | | | | | | | |

*Tip: If a number isn't available, write `UNKNOWN` and why.*

### 4C. Channel Scoreboard (update every week or two)

| Channel | Visitors | Sign-ups | Customers | Money spent | CAC | Keep / Change / Stop |
|---|---|---|---|---|---|---|
| | | | | | | |
| | | | | | | |
| | | | | | | |

### 4D. Customer Quality Check (monthly)

**Q4.1 Are customers staying and happy?** Fill in the numbers and one sentence.

| Measure | This month | Last month | Comment |
|---|---|---|---|
| Still active after 30 days (%) | | | |
| Customers who left (churn) | | | |
| Refunds or complaints | | | |
| Feedback score (e.g., 1-10 or NPS) | | | |
| Top thing customers like | | | |
| Top thing customers complain about | | | |

### 4E. Experiment Log (one row per test)

*Example: Hypothesis "A shorter sign-up form will raise sign-ups by 20%." Test: "Remove 2 fields for 2 weeks." Result: "+12%." Decision: "Keep."*

| # | Hypothesis (what we think will happen) | What we changed | Start–End dates | Success number | Result | Decision (Keep/Drop/Retest) |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |

**Q4.2 Every week, answer three questions:**
1. What worked best? ANSWER:
2. What worked worst? ANSWER:
3. What will we do differently next week? ANSWER:

### 🛑 Approval Gate 4: Spending and Customer Messages

Before spending money or sending any message to real customers, a human writes here: ______________________
(What it is, how much, and date approved.)

---

## Section 5: Risks & Blockers Log

**Status:** ⬜ Not started
*Write down anything that could go wrong, or is already stopping you. Update weekly.*

| # | What could go wrong / is stuck | How bad? (Low/Med/High) | Who owns it | Plan to fix | Due date | Status |
|---|---|---|---|---|---|---|
| 1 | | | | | | Open |
| 2 | | | | | | Open |

---

## Section 6: Final Retro (When You Reach 500, or When You Stop)

**Status:** ⬜ Not started
*Do this together. Be honest. No blame.*

**Q6.1 Did you reach 500 customers? Date reached, total time, total money spent, and final CAC.**
ANSWER:

**Q6.2 What were your top 3 channels, and which one was a surprise?**
ANSWER:

**Q6.3 Where did people quit the funnel most? Was your tracking good enough to see it?**
ANSWER:

**Q6.4 What 3 things would you do the SAME next time?**
ANSWER:

**Q6.5 What 3 things would you do DIFFERENTLY next time?**
ANSWER:

**Q6.6 What should be changed in this template so the next project goes smoother?**
ANSWER:

---

## Decision & Change Log

*Write a line every time you change something important (customer definition, targets, tools, budget, channels, event names, launch date).*

| Date | Who (name or AI-agent) | What changed | Why | Approved by |
|---|---|---|---|---|
| | | | | |

---

## Final Self-Check (Before You Say "Done")

- [ ] No blank answers: everything is filled, `UNKNOWN` (with owner and date), or `N/A` (with reason)
- [ ] `project_summary` block at the top is current
- [ ] All 🛑 Approval Gates are signed by a human
- [ ] Status Board is up to date
- [ ] Event names in Section 2 match what is really in the product
- [ ] Weekly Log numbers add up (new customers sum to total customers)
- [ ] No real personal data appears anywhere in this file
