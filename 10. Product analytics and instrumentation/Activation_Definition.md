---
doc_type: activation_definition
template_version: 1.0.0
project_name: "[FILL: product name]"
doc_version: "0.1.0"
status: draft            # draft | in_review | approved | superseded
owner: "[FILL: one named person]"
last_updated: "YYYY-MM-DD"
product_type: "[FILL: b2c | b2b_saas | marketplace | ai_product | other]"
activation_unit: "[FILL: person | account | buyer | seller | other]"
activation_window_days: 7
first_500_goal: "500 activated users"
minors_possible: "[FILL: yes | no | unknown]"
analytics_tool: "[FILL: tool name or 'not chosen yet']"
---

# How to Fill This Document

**Read this box first. It takes 2 minutes.**

## What is this document?
This document answers one question: **"What exactly does a new person do in our product that tells us they got real value?"**
That action is called **activation**. Everyone on the team (humans and AI agents) will use your answer to build, measure, test, and launch the product until **500 people have activated**.

## The 4 symbols you will see

| Symbol | Meaning | What you do |
|---|---|---|
| ✏️ **WRITE** | A question for you | Type your answer under it |
| 💡 **EXAMPLE** | A sample answer from a pretend app called **TaskBuddy** (a to-do list app) | Read it, then write your own. Never copy it as your answer. |
| 🛟 **IF STUCK** | A safe fallback answer | Use it only if you truly don't know, and mark it `(default)` |
| 🤖 **AI AGENT** | A rule for AI helpers | Humans can skip it |

## The 7 golden rules
1. **Never leave a blank.** If you don't know, write `UNKNOWN - [who will find out] - [date]`.
2. **One answer per question.** Short and plain. If it needs "and/or", split it.
3. **Use numbers, not feelings.** Write "within 7 days", not "soon". Write "3 or more", not "a few".
4. **Use real names from the product.** Write the actual button or screen name, e.g. "Add task button".
5. **Don't guess silently.** If you guessed, add `(guess)` after the answer so someone can check it.
6. **Never put real personal data** (names, emails, phone numbers, passwords) in this file.
7. **Change the answer, not the question.** Don't delete or rename questions or their IDs (like `Q2.1`). Machines read those IDs.

## Pick your path

| If you have... | Do this |
|---|---|
| **5 minutes** | Fill **Section 1, 2, and 3** only. Mark everything else `UNKNOWN`. |
| **30 minutes** | Fill Sections 1 to 6. |
| **A full session** | Fill everything, then finish with **Section 14: Final Self-Check**. |

## Who fills what

| Section | Best filled by |
|---|---|
| 1 to 3 | Founder / product owner (the person who knows *why* people use it) |
| 4, 8 | Engineer + tester |
| 5, 10 | Analyst or product owner |
| 6 | Whoever handles legal or privacy (or the owner, asking for review) |
| 7, 9, 12 to 14 | Project manager / owner |

## When to update this document
Update it (and add a line to Section 13) whenever: the product's main promise changes, the activation action changes, a stage gate is passed, or the numbers in Section 5 show a red alert.

---

# 0. Document Control

✏️ **Fill the table.**

| Field | Answer |
|---|---|
| Q0.1 Project name | |
| Q0.2 Document owner (one person) | |
| Q0.3 Date started | |
| Q0.4 Current lifecycle stage (pick one: Idea / Build / Test+Beta / Launch / Post-500) | |
| Q0.5 Where do the team and AI agents find the latest version? (link or folder path) | |
| Q0.6 Related documents (product brief, tracking plan, privacy policy) | |

💡 **Example:** TaskBuddy / Maria Lopez / 2026-10-01 / Build / `Product analytics and instrumentation/Activation_Definition.md` / Product brief v2

---

# 1. Product in One Breath

*Goal: anyone, even a new teammate or a child, should understand what you are making in one minute.*

**Q1.1 ✏️ What does your product do? Finish this sentence: "[Product] helps [who] to [do what]."**

> Your answer:

💡 *TaskBuddy helps busy parents to remember family chores without arguing.*

**Q1.2 ✏️ Who is the main user? (Describe one real kind of person in 1 to 2 sentences.)**

> Your answer:

💡 *A parent with 2 to 4 kids who uses a phone for everything.*

**Q1.3 ✏️ What problem does the user have *before* using your product?**

> Your answer:

**Q1.4 ✏️ What product type is it? (circle/mark one)**
- [ ] B2C (individual people)
- [ ] B2B SaaS (teams or companies)
- [ ] Marketplace (two sides, like buyers and sellers)
- [ ] AI product (value = a useful AI result)
- [ ] Other: ______

**Q1.5 ✏️ Who is the "unit" that can be activated?**
- [ ] A person (one user)
- [ ] An account (a team or company)
- [ ] A buyer
- [ ] A seller / supplier / creator
- [ ] Other: ______

🛟 *If stuck: B2C = person. B2B = account (and also track the person). Marketplace = track buyer and seller **separately** and write one activation definition for each in Section 2.*

**Q1.6 ✏️ Could any users be under 18?**
- [ ] Yes   - [ ] No   - [ ] Not sure → *If "Yes" or "Not sure", you MUST answer Section 6.4.*

**Q1.7 ✏️ Where will people first use it?** (mark all) 
- [ ] Web   - [ ] iPhone   - [ ] Android   - [ ] API / developer   - [ ] Other: ______

**Q1.8 ✏️ How will people find out about it? (top 1 to 3 ways)**

> Your answer:

---

# 2. The Activation Definition (the most important section)

## 2.1 Plain-words background

- **Aha moment** = the instant the user *feels* "this is useful!"
- **Activation event** = the exact action in the product that *proves* they reached the Aha moment.
- **Activated user** = someone who did the activation event, in the right time, with the right conditions.

Signing up is **not** activation. Opening the app is **not** activation. Activation is **getting a real result**.

## 2.2 Find the Aha moment

**Q2.1 ✏️ Imagine your happiest new user. In one sentence, what did they just get or achieve?**

> Your answer:

💡 *They created a chore, assigned it to a child, and the child ticked it off.*

**Q2.2 ✏️ List 3 to 5 early actions a new user can take, in the order they usually happen.**

| # | Action (use the real button/screen name) | Is it a "real result"? (Y/N) |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |
| 5 | | |

💡 *1 Sign up (N) · 2 Add a child (N) · 3 Create a chore (N) · 4 Child marks chore done (Y)*

## 2.3 Choose the Activation Event

**Q2.3 ✏️ Which ONE action from Q2.2 proves value? Write it as: "[Person/Account] [past-tense verb] [thing]".**

> Your answer:

💡 *A parent account has one chore marked done by a child.*

**Q2.4 ✏️ Why is this action the proof? (Write the reason in 1 to 2 sentences. If you have data, say so. If it's a hunch, write `(hypothesis)`.)**

> Your answer:

**Q2.5 ✏️ Which other actions did you consider, and why did you say no?**

| Rejected action | Why not? |
|---|---|
| | |
| | |

💡 *Created a chore: easy to do without ever getting value.*

## 2.4 Make it exact (no guessing allowed)

**Q2.6 ✏️ Time window: the activation event must happen within ___ days of signup.**

> Your answer: ______ days

🛟 *If stuck: 7 days (default). Use 1 day for simple tools, 14 to 30 days for slow-adoption B2B products.*

**Q2.7 ✏️ Minimum count: how many times? (Once is fine for big actions. Use more for habit-type actions.)**

> Your answer: ______ time(s)

**Q2.8 ✏️ Extra conditions that MUST be true for it to count? (e.g., real data, not a demo; not done by your own team)**

> Your answer:

💡 *The chore must belong to a real account, not the demo account.*

**Q2.9 ✏️ Who or what must be EXCLUDED from the count?** (mark all)
- [ ] Our own team / test accounts
- [ ] Bots or automated traffic
- [ ] Demo or sandbox data
- [ ] Duplicate accounts of the same person
- [ ] Other: ______

**Q2.10 ✏️ (Marketplaces and B2B only) Write one separate activation sentence for each side/role.**

| Side / role | Activation sentence |
|---|---|
| Buyer / user | |
| Seller / admin | |

## 2.5 The official sentence

**Q2.11 ✏️ Combine your answers into ONE sentence. Copy it exactly into the YAML header's team docs too.**

Template: *"A [unit] is activated when [event from Q2.3] [Q2.7 count] within [Q2.6] days of signup, excluding [Q2.9]."*

> **OFFICIAL ACTIVATION DEFINITION:**
>
> _______________________________________________

💡 *A parent account is activated when at least 1 chore is marked done by a child within 7 days of signup, excluding team and test accounts.*

## 2.6 The 5-point check (answer Yes/No to each)

| # | Check | Yes/No |
|---|---|---|
| 1 | Can a stranger measure it with a yes/no answer? | |
| 2 | Does it show real value, not just effort or curiosity? | |
| 3 | Can a new user reach it fast enough (inside the window)? | |
| 4 | Can we track it with an event in Section 4? | |
| 5 | Do people who do it stay or return more than people who don't? (If unknown, write `(to verify at 100 users)`) | |

**If any answer is "No", go back to Q2.3 and change it.**

## 2.7 Backup and "stickiness" definitions

**Q2.12 ✏️ Optional: What does a returning, healthy user do after activation? (e.g., "does the activation event again in week 2")**

> Your answer:

---

# 3. User Journey to Activation

*Goal: draw the path from "never heard of us" to "activated" in simple steps.*

**Q3.1 ✏️ Fill the table. Add rows if needed. Each step must be a thing the user can do or see.**

| Step | What the user does | Screen / page name | Event name (from Section 4) | Expected % who continue |
|---|---|---|---|---|
| 1 Arrive | Opens site or app | | | 100% |
| 2 Sign up | | | | |
| 3 Set up | | | | |
| 4 First try | | | | |
| 5 Aha moment | | | | |
| 6 **Activation** | | | | |

💡 *Step 2: creates account · Screen: "Create account" · Event: `account_created` · 60%*

**Q3.2 ✏️ Count the steps and clicks between signup and activation.**

> Number of steps: ______ Number of clicks (estimate): ______

🛟 *If it's more than 7 steps, write down which one you could remove in Section 11 (Risks).*

**Q3.3 ✏️ Where do you EXPECT people to quit? (top 2 spots) Why?**

> Your answer:

**Q3.4 ✏️ What help does the product give at each hard spot? (tooltip, email, checklist, chat)**

> Your answer:

---

# 4. Tracking Plan (What the Product Must Record)

*Goal: list every event the product must send so that activation can be counted correctly.*

## 4.1 Naming rules (do not change these without writing it in Section 13)

- Event names use `snake_case`, written as **object + past-tense verb**: `chore_completed`, `account_created`.
- Property names use `snake_case`: `plan_type`, `item_count`.
- Never use spaces, capital letters, or emojis.
- One event = one meaning. Never reuse an event for something else.

**Q4.1 ✏️ Do you agree with the naming rules?** - [ ] Yes - [ ] No, changes: ______

## 4.2 Identity rules

**Q4.2 ✏️ How will you recognize the same person before and after signup?**

> Your answer:

🛟 *If stuck: give every visitor an `anonymous_id`. On signup or login, link it to a permanent `user_id`. For B2B also record `account_id` on every event.*

**Q4.3 ✏️ Which ID counts as the "unit" in Q1.5?** `user_id` / `account_id` / other: ______

## 4.3 Properties sent with EVERY event

| Property | Meaning | Required? |
|---|---|---|
| `event_name` | What happened | Yes |
| `timestamp_utc` | When it happened (UTC) | Yes |
| `user_id` or `anonymous_id` | Who did it | Yes |
| `account_id` | Which company/team (B2B only) | If B2B |
| `platform` | web / ios / android / api | Yes |
| `app_version` | Which version of the product | Yes |
| `environment` | production / staging / test | Yes |
| `is_internal_user` | true if it is our own team | Yes |

**Q4.4 ✏️ Any extra properties for every event?**

> Your answer:

## 4.4 The event list

**Q4.5 ✏️ List every event. The first rows are required. Add the rest of your funnel.**

| ID | Event name | When exactly does it fire? | Properties (besides 4.3) | Where it fires (client/server) | Owner | Built? | Tested? |
|---|---|---|---|---|---|---|---|
| E1 | `account_created` | Right after signup succeeds | `signup_method` | server | | ☐ | ☐ |
| E2 | | | | | | ☐ | ☐ |
| E3 | | | | | | ☐ | ☐ |
| E4 | **[ACTIVATION EVENT]** | | | | | ☐ | ☐ |
| E5 | | | | | | ☐ | ☐ |

💡 *E4 `chore_completed` · fires when a child taps "Done" and the server confirms · properties `chore_id`, `completed_by_role` · server*

🛟 *If stuck on client vs. server: choose **server** for anything money-related or activation-related. Server events are harder to fake or lose.*

**Q4.6 ✏️ Write the exact "activated" rule in event terms.**

> Your answer: *"A unit is activated when event ______ happens ___ time(s) within ___ days after `account_created`, where [conditions]."*

**Q4.7 ✏️ Where will the data be stored and who may look at it?**

> Your answer:

---

# 5. Metrics, Targets, and Alerts

*Goal: decide what "good" looks like before launch, so nobody changes the goalposts.*

## 5.1 The metrics

| Metric | How to calculate it | Your starting target | Source |
|---|---|---|---|
| **Activation rate** | Activated units ÷ new signups (same time period, same window) | | |
| **Time to activate** | Median time from signup to activation | | |
| **Funnel step conversion** | Users at step N+1 ÷ users at step N | | |
| **Activated count (the 500 counter)** | Total activated units so far | 500 | |
| **Week-1 return** | Activated users who return in days 8 to 14 ÷ activated users | | |

**Q5.1 ✏️ Fill the "Your starting target" column.**

🛟 *Starter defaults (change after real data): Activation rate green ≥ 40%, yellow 20 to 39%, red < 20%. Time to activate: green ≤ 1 day, yellow 2 to 3, red > 3. These are not facts. They are placeholders to be replaced at 100 users.*

## 5.2 Traffic-light rules

**Q5.2 ✏️ Fill the table.**

| Metric | 🟢 Green (keep going) | 🟡 Yellow (look into it) | 🔴 Red (stop and fix) |
|---|---|---|---|
| Activation rate | | | |
| Time to activate | | | |
| Biggest funnel drop | | | |
| Data quality (events arriving correctly) | ≥ 99% | 95 to 98% | < 95% |

**Q5.3 ✏️ What do we do when something is red? (who gets told, within how long, what is paused)**

> Your answer:

## 5.3 The "first 500" milestone

**Q5.4 ✏️ How will you count the 500th activated unit?**

> Counting rule: **500 activated units** as defined in Q2.11, counted from the public launch date: ____ (date).
> Do beta users count? - [ ] Yes - [ ] No
> Do paid-ad or invite-only users count? - [ ] Yes - [ ] No

**Q5.5 ✏️ By what date do you hope to reach 500?** ______  **Review checkpoints:** 25, 100, 250, 500 activated.

**Q5.6 ✏️ How many signups do you need to reach 500 activated?** *(Formula: 500 ÷ expected activation rate.)*

> Your answer: ______ signups

💡 *500 ÷ 0.40 = 1,250 signups.*

## 5.4 Segments to break the numbers down

**Q5.7 ✏️ Mark the groups you want to compare (so you can see who activates best).**
- [ ] Platform (web / iOS / Android)
- [ ] Traffic source (ad, friend invite, search...)
- [ ] Country
- [ ] Plan type
- [ ] Company size (B2B)
- [ ] Buyer vs. seller (marketplace)
- [ ] Other: ______

---

# 6. Privacy, Consent, and Safety

*Goal: make sure tracking never hurts the people we are trying to help.*

**⚠️ This section must be reviewed by a person who understands your local privacy laws before launch. This template is not legal advice.**

## 6.1 Consent

**Q6.1 ✏️ Which regions will your users be in?** - [ ] EU/UK (GDPR) - [ ] California (CCPA/CPRA) - [ ] Rest of US - [ ] Other: ______

**Q6.2 ✏️ Do you need to ask permission before tracking? How do you ask and where is the answer stored?**

> Your answer:

🛟 *If stuck: assume YES for EU/UK users. Track nothing optional until they agree. Make "Decline" as easy as "Accept". Link a privacy policy that states what you record.*

**Q6.3 ✏️ What happens to events when someone says no?** 
- [ ] Nothing is sent
- [ ] Only anonymous, essential events are sent
- [ ] Other: ______

## 6.2 The "Never Record" list

**Never put these into any event or property:**
- Passwords, security codes, API keys
- Full names, emails, phone numbers, home addresses
- Payment card numbers, bank details, government IDs
- Health, religion, political, or sexual information
- Free-text typed by users (it may contain any of the above)
- Exact location (use country/region instead)

**Q6.4 ✏️ Add anything specific to your product that must never be recorded:**

> Your answer:

## 6.3 Data rights and storage

**Q6.5 ✏️ How long do you keep event data?** ______ months *(🛟 default: 14 months)*

**Q6.6 ✏️ If a user asks "delete my data", who does it and how fast?**

> Your answer:

## 6.4 Children and minors (answer if Q1.6 was "Yes" or "Not sure")

**Q6.7 ✏️ Do you ask for age? How? What happens if the user is under 13 (US) or under 16 (some EU countries)?**

> Your answer:

🛟 *If stuck: don't track users known to be children until a qualified person approves in writing. Never use their data for ads.*

## 6.5 Safety of the activation event itself

**Q6.8 ✏️ Could the activation event push users to do something risky or annoying just to be counted? (e.g., spam invites, fake data)**

> Your answer:

---

# 7. Lifecycle Gates: From Idea to the First 500 Activated Users

*A gate is a checkpoint. You may not move to the next stage until every box is ticked by a human.*

```
STAGE 1            STAGE 2              STAGE 3                STAGE 4
Idea → Spec   →   Build + Instrument → Test + Private Beta → Launch → 500 activated
  Gate A             Gate B               Gate C                Gate D (done!)
```

## Stage 1: Idea → Spec (Gate A)
**Goal:** write down activation *before* writing code.

- [ ] Sections 1 and 2 are filled, and Q2.11 is written
- [ ] The 5-point check (2.6) has no "No" answers
- [ ] The owner and approver are named (Section 12)
- [ ] The analytics tool is chosen, or "not chosen yet" has a decision date
- [ ] Section 6 has been looked at (even if not final)

**Q7.1 ✏️ Date Gate A was passed and by whom:** ______

## Stage 2: Build + Instrument (Gate B)
**Goal:** every event in Section 4 is built *as features are built*, not after.

- [ ] Every event in 4.4 is built in a **test** environment
- [ ] Each event is documented with its exact "when it fires" rule
- [ ] Activation can be calculated in the analytics tool (a rough chart exists)
- [ ] No item from the "Never Record" list is sent
- [ ] Consent logic works (Section 6.1)
- [ ] Section 8 test cases are written

**Q7.2 ✏️ Date Gate B was passed and by whom:** ______

## Stage 3: Test + Private Beta (Gate C)
**Goal:** prove the data is *correct* with a small group (10 to 50 real people).

- [ ] Section 8 checklist is 100% complete
- [ ] At least ___ beta users tried it (🛟 default: 20)
- [ ] Beta events match what people actually did (spot-check ≥ 10 sessions by hand)
- [ ] Activation rate is calculated, even if the group is small
- [ ] Data quality is green (Section 5.2)
- [ ] The most common drop-off point is written in Section 11
- [ ] Beta users who were *not* activated were asked why (at least 5 conversations or surveys)

**Q7.3 ✏️ What did beta tell us? (3 bullet points)**

> Your answer:

**Q7.4 ✏️ Date Gate C was passed and by whom:** ______

## Stage 4: Public Launch → First 500 Activated (Gate D)
**Goal:** get to 500 activated users while keeping the data honest.

**Launch-day checklist**
- [ ] Production events were tested on a real production account today
- [ ] Dashboards and the 500 counter are visible to the whole team
- [ ] Alerts from 5.2 are turned on and reach a real person
- [ ] The rollback / pause plan is written (Q5.3)
- [ ] Launch date is written in Q5.4

**Checkpoints (fill in as you go)**

| Checkpoint | Date reached | Activation rate | Time to activate | Biggest drop-off | Decision made |
|---|---|---|---|---|---|
| 25 activated | | | | | |
| 100 activated | | | | | |
| 250 activated | | | | | |
| **500 activated** | | | | | |

**At 100 activated: you MUST do these 3 things**
- [ ] Check if activated users really return more than non-activated users (Q2.6 check #5)
- [ ] Re-confirm or change the activation definition (write the result in Section 13)
- [ ] Replace the starter targets in 5.1 with real ones

**At 500 activated: you MUST do these 3 things**
- [ ] Write a 1-page summary: what worked, what didn't, what to change
- [ ] Update Section 2 with what you learned and bump the version number
- [ ] Decide the next goal (e.g., 5,000 activated or first paying customers)

**Q7.5 ✏️ Date Gate D was passed and by whom:** ______

---

# 8. QA and Instrumentation Test Plan

*Goal: prove the numbers are true before anyone makes decisions from them.*

## 8.1 Test environments

**Q8.1 ✏️ Where do you test, and how do test events stay out of real reports?** (use `environment = test` and `is_internal_user = true`)

> Your answer:

## 8.2 Required test cases

| ID | Test | Expected result | Pass? | Tester | Date |
|---|---|---|---|---|---|
| T1 | New user signs up | `account_created` arrives **once** | ☐ | | |
| T2 | User does the activation action exactly as in Q2.11 | Activation event arrives **once** with all properties | ☐ | | |
| T3 | User does the activation action **after** the time window | Not counted as activated | ☐ | | |
| T4 | Team/test account does the activation action | Not counted (Q2.9) | ☐ | | |
| T5 | User refreshes, double-clicks, or goes offline | No duplicate events | ☐ | | |
| T6 | User declines consent | Behaves as Q6.3 says | ☐ | | |
| T7 | Anonymous visitor then signs up | Both identities are linked (Q4.2) | ☐ | | |
| T8 | Same user on web, then on phone | Counted as **one** unit | ☐ | | |
| T9 | Event properties checked | No item from "Never Record" present | ☐ | | |
| T10 | User deletes their account | Data handled per Q6.6 | ☐ | | |
| T11 | (B2B) Second person joins the same account | Account is still **one** unit | ☐ | | |
| T12 | (Marketplace) Buyer and seller act | Each counted under the right side | ☐ | | |

**Q8.2 ✏️ Add product-specific tests:**

| ID | Test | Expected result | Pass? |
|---|---|---|---|
| T13 | | | ☐ |

## 8.3 Data-quality checks (run weekly after launch)

- [ ] Event counts today are within ±30% of normal (no silent breaks)
- [ ] No event has missing required properties
- [ ] No duplicate events for the same action
- [ ] Time stamps are in UTC and make sense
- [ ] No spike of events from test or internal accounts
- [ ] Number of activated units in the dashboard = number from a manual count of 10 random users

**Q8.3 ✏️ Who runs the weekly check?** ______

---

# 9. AI Agent Rules

*These rules tell AI agents (and the humans who use them) what is allowed. Agents may **draft, check, and flag**. Humans **decide and approve**.*

## 9.1 What an AI agent MAY do
- Read this document and answer questions about it
- Draft answers for blank questions, marked `(AI draft - needs human review)`
- Check this document for gaps, contradictions, and missing IDs
- Compare the tracking plan (Section 4) with the test results (Section 8) and list mismatches
- Suggest improvements and flag risks
- Draft summaries for each checkpoint in Section 7

## 9.2 What an AI agent MUST NOT do
- Change the Official Activation Definition (Q2.11) without a human writing "Approved" in Section 13
- Mark any gate, test, or checklist item as passed
- Invent numbers, quotes, or user data (if unknown, write `UNKNOWN`)
- Add personal data to this file or to any event
- Skip or rename question IDs
- Approve privacy or legal questions (Section 6)

## 9.3 Agent checklist (run before saying "this document is ready")

1. Every `Q` has an answer, `UNKNOWN`, or `(default)`
2. Q2.11 matches Q4.6 word for word in meaning
3. Every event in the Section 3 journey table exists in the Section 4 event list
4. The activation event (E4) has an owner and a test (T2)
5. Time window is the same everywhere it appears (Q2.6, Q4.6, Q5.4)
6. Section 6 answers exist if `minors_possible` is not `no`
7. Gates only show "passed" if a named human and a date are present
8. The YAML header matches the answers in the document

**Q9.1 ✏️ Which AI tools or agents will work with this file?**

> Your answer:

**Q9.2 ✏️ Who reviews and approves AI-drafted answers?** ______

## 9.4 Reply format for agents
When reporting back, an agent should use exactly three headings: **Done**, **Gaps found (with Q-IDs)**, **Needs a human decision**.

---

# 10. Learning and Improvement Loop

*Goal: get smarter after every 100 new users.*

**Q10.1 ✏️ How often does the team look at the activation numbers?** - [ ] Daily - [ ] Weekly - [ ] Each checkpoint (25/100/250/500)
🛟 *Default: weekly, plus every checkpoint.*

**Q10.2 ✏️ Who attends the review, and where are decisions recorded?**

> Your answer:

**Q10.3 ✏️ How will you learn *why* people don't activate? (mark all)**
- [ ] Short email or in-app question to non-activated users
- [ ] 5 user interviews per checkpoint
- [ ] Watching session recordings (only if consent allows)
- [ ] Support messages
- [ ] Other: ______

## 10.1 Experiment log

*Test one change at a time. Write the guess *before* you start.*

| # | Date | What we changed | What we expected | What happened | Keep / Undo / Retest |
|---|---|---|---|---|---|
| X1 | | | | | |
| X2 | | | | | |

---

# 11. Risks and Open Questions

**Q11.1 ✏️ List what could make this activation definition wrong or hard to measure.**

| # | Risk | How likely (Low/Med/High) | How bad (Low/Med/High) | What we will do | Owner |
|---|---|---|---|---|---|
| R1 | | | | | |
| R2 | | | | | |

💡 *R1: Kids tap "Done" without doing the chore. Med / High. Add parent approval and track `chore_approved` as well. Owner: Maria.*

**Q11.2 ✏️ Things you don't know yet (every `UNKNOWN` in this file should appear here):**

| # | Question | Who will find out | By when |
|---|---|---|---|
| U1 | | | |

---

# 12. Owners and Sign-Off

## 12.1 Who does what

| Role | Name | What they are responsible for |
|---|---|---|
| **Owner** (final answer) | | Q2.11 and keeping this document alive |
| **Product / Project manager** | | Gates and checkpoints (Section 7) |
| **Engineering lead** | | Section 4 events built correctly |
| **QA / Tester** | | Section 8 tests |
| **Analyst / Data person** | | Section 5 numbers and dashboard |
| **Privacy / Legal reviewer** | | Section 6 |
| **AI agent supervisor** | | Section 9 |

## 12.2 Approvals (a human writes name and date; agents may not)

| Approval | Name | Date | OK? |
|---|---|---|---|
| Activation definition (Section 2) | | | ☐ |
| Tracking plan (Section 4) | | | ☐ |
| Privacy (Section 6) | | | ☐ |
| Gate A / B / C / D | | | ☐ |

---

# 13. Decision Log and Changelog

## 13.1 Decision log
*Every time you change the activation definition, targets, or event list, write a line here.*

| Date | What changed | Why | Who approved | Old → New version |
|---|---|---|---|---|
| | Created first draft | | | → 0.1.0 |

## 13.2 Version rules
- **Patch** (0.1.1): typo or clarification, no meaning change
- **Minor** (0.2.0): new events, targets, or tests
- **Major** (1.0.0): the activation definition itself changed

---

# 14. Final Self-Check (do this before sharing)

**The 10-year-old test:** Hand this file to someone who doesn't know your product. Can they, within 10 minutes, tell you (1) what the product does, (2) what an activated user is, and (3) how many you want? If not, rewrite until yes.

- [ ] Every question has an answer, `UNKNOWN`, or `(default)`
- [ ] Section 2 has one clear official sentence
- [ ] Words like "soon", "many", "some", "good" were replaced with numbers
- [ ] No real personal data appears anywhere
- [ ] The YAML header at the top is filled in
- [ ] Section 9.3 agent checklist is all ✅
- [ ] An owner is named and the owner has read it all
- [ ] Next review date: ______

**Q14.1 ✏️ In your own words: what is the one thing a new user must do for us to call them activated?**

> Your answer:

---

# Appendix A: Activation Ideas by Product Type

*Use these to spark ideas. Never copy them blindly. Your own data decides.*

| Product type | Possible Aha moment | Possible activation event | Watch out for |
|---|---|---|---|
| **B2C content / media app** | Finds something they love | Finishes 1 item, or saves 3 items | Counting a click as "watching" |
| **B2C habit / health / learning** | Sees first progress | Completes a first session and returns once | Counting setup steps as value |
| **B2C social / community** | Gets a response from someone | Posts and receives 1 reply or reaction | Needing other users to exist first |
| **B2B SaaS (tool)** | Team gets a result together | 2+ people complete the core task in the account | Counting accounts where only the admin did everything |
| **B2B SaaS (data/integration)** | Sees their own real data in it | Connects 1 data source and views 1 report | Trial with sample data counted as real |
| **Marketplace (buyer)** | Finds what they need | First successful search leading to a contact or order | Searches with no results |
| **Marketplace (seller)** | Gets first interest | Publishes a complete listing and receives 1 inquiry | Empty or low-quality listings |
| **AI product** | Gets a useful answer or output | Receives an output and keeps, copies, or uses it | Counting any prompt sent as success |
| **Developer / API** | First successful call | Makes 1 successful call in production-like setting | Failed calls counted as activation |

---

# Appendix B: Glossary (plain words)

| Word | Plain meaning |
|---|---|
| **Activation** | A new user gets real value for the first time |
| **Activated user** | Someone who did the activation event in the right time with the right conditions |
| **Aha moment** | The moment the user feels "this is useful" |
| **Event** | A note the product writes down when something happens (like "chore_completed") |
| **Property** | An extra detail attached to an event (like which chore) |
| **Tracking plan** | The list of all events and properties |
| **Funnel** | The steps from arriving to activating, with the % who continue at each |
| **Conversion** | The % of people who go from one step to the next |
| **Cohort** | A group of users who started in the same period |
| **Segment** | A group of users who share something (like the same country) |
| **Instrumentation** | Adding tracking to the product |
| **Gate** | A checkpoint you must pass before the next stage |
| **UTC** | A world standard time, so all time stamps match |
| **PII** | Personal information that could identify someone |
| **Consent** | The user's "yes" to being tracked |
| **Environment** | Where the product runs: test, staging, or production (real) |
| **Hypothesis** | A guess you plan to check with data |
| **Dashboard** | A screen that shows the numbers |
| **UNKNOWN** | The honest answer when you don't know yet, with who/when to find out |

---

# Appendix C: Common Mistakes (and fixes)

| Mistake | Fix |
|---|---|
| Choosing "signed up" as activation | Pick the first moment of real value instead |
| Choosing a very late action | Pick the earliest action that still shows value |
| No time window | Always add a window (Q2.6) |
| Counting your own team | Add `is_internal_user` and exclude (Q2.9) |
| Changing the definition mid-way without writing it down | Log every change in Section 13 |
| Building tracking after launch | Do it during Stage 2 |
| Same event name meaning different things | One event = one meaning |
| Leaving blanks | Use `UNKNOWN` with an owner and date |
| Sending emails or names inside events | Follow the "Never Record" list (6.2) |

---

*End of template. Template version 1.0.0. Copy this file for each new project, keep the section and question IDs unchanged, and only change the answers.*
