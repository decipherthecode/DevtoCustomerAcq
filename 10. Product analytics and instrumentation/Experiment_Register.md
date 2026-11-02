<!--
FILE: Product analytics and instrumentation/Experiment_Register.md
TEMPLATE NAME: Experiment Register (Universal Template)
TEMPLATE VERSION: 1.1.0
COVERS: Build -> Beta -> Launch -> Growth (first 500 customers)
FOR: Humans (beginners welcome) AND AI agents
HOW TO USE THE TEMPLATE: Copy this whole file into your project folder. Replace everything marked <<LIKE THIS>>. You may delete the worked examples in Part 9 once you understand them.
-->

# How to Fill This Document

**Read this first. It takes 3 minutes.**

## What is this document?

An **experiment** is a small test. You change **one** thing, watch what happens, and learn whether the change was good.

This file is the **one place** where your team writes down every test: why you ran it, what you changed, what happened, and what you decided. Nobody has to guess later, because the answer is written here.

## The 6 Golden Rules

1. **One file only.** Everything about experiments lives here. Do not scatter notes in chats or other files.
2. **Answer every question.** If a question does not apply, write `N/A - <short reason>`. Never leave a blank.
3. **Never guess.** If you do not know, write `UNKNOWN - ask <name>` and tell that person. A visible "unknown" is better than a hidden guess.
4. **Use real numbers.** Write `20%`, not `better`. Write `by 2026-11-15`, not `soon`.
5. **Write the plan BEFORE you run the test.** Never change the question after you see the results.
6. **Choose from the lists.** When a field shows options like `Idea \| Ready \| Running`, pick exactly one of those words.

## Symbols used in this file

| Symbol | Meaning |
|---|---|
| 🟢 | Required. You must fill it before you move on. |
| 🔵 | Optional. Fill it if you can. |
| 🤖 | Extra instruction for AI agents. |
| `<<TEXT>>` | A blank. Replace it with your own answer. |
| `[ ]` / `[x]` | An empty / ticked checkbox. Tick it only when it is really true. |

## Your path through this file (do the steps in order)

| Step | What you do | Where |
|---|---|---|
| 1 | Fill in the **Project Header** (once per project) | Part 1 |
| 2 | Read the **4 Stages** and pick the one you are in | Part 2 |
| 3 | Write new ideas in the **Idea Backlog** and score them | Part 3 |
| 4 | Pick the best idea. Copy the **Entry Template** and answer its questions | Part 7 |
| 5 | Add one new row to the **Experiment Index** | Part 4 |
| 6 | Ask a second person to **review** each section (Section 17) | Part 7 |
| 7 | Pass the **"Ready to Run" checklist** | Part 8 |
| 8 | Run the test. Write in the **Run Log** each time something happens | Section 13 |
| 9 | When it ends, fill **Results**, **Decision** and **Lessons** | Sections 14-16 |
| 10 | Add a row to the **Decision Log** and **Lessons Library** | Part 5 |
| 11 | Every week, hold the **Weekly Review** | Part 6 |

## Stuck? Use this table

| If you are thinking... | Do this |
|---|---|
| "I don't know what to test." | Look at the **funnel** in Part 1. Find the step where most people leave. Test there. |
| "I don't know my number (metric)." | Pick one thing you can count (sign-ups, clicks, payments). Write how you count it. |
| "We have very few users." | That is normal. Read the **Small Numbers Warning** in Section 7. |
| "The result is unclear." | Choose the decision `Need more data` and write what extra data you need. |
| "Something broke." | Follow the **Rollback Plan** you wrote in Section 10. Then write it in the Run Log. |
| "I don't understand a word." | Look in the **Glossary** (Part 12). |

---

# Part 1. Project Header (fill once per project)

> Answer these once. Every experiment below links back to this part.

| # | Question | Your answer |
|---|---|---|
| 1.1 🟢 | What is the **project name**? | `<<PROJECT NAME>>` |
| 1.2 🟢 | What is the **project code**? (2 to 5 capital letters. It goes at the start of every ID so IDs never clash between projects.) | `<<e.g. SHOP>>` |
| 1.3 🟢 | In **one sentence**, what does the product do, and for whom? | `<<e.g. "A phone app that helps small shops track daily sales.">>` |
| 1.4 🟢 | Who is the **register owner** (the person who keeps this file correct)? | `<<NAME, ROLE>>` |
| 1.5 🟢 | **Start date** and **planned launch date** | Start: `<<YYYY-MM-DD>>` / Launch: `<<YYYY-MM-DD>>` |
| 1.6 🟢 | **Big goal:** how many customers do we want, and by when? | `<<500>>` customers by `<<YYYY-MM-DD>>` |
| 1.7 🟢 | What counts as a **"customer"**? (Be exact. Example: "a person who paid at least once".) | `<<DEFINITION>>` |
| 1.8 🟢 | How many customers do we have **right now**? On what date? | `<<NUMBER>>` on `<<YYYY-MM-DD>>` |
| 1.9 🟢 | **Current stage** (see Part 2) | `Build \| Beta \| Launch \| Growth` |
| 1.10 🟢 | Write the **funnel**: the steps a person takes from "never heard of us" to "customer". | `<<e.g. Visit -> Sign up -> First use -> Pay -> Still using after 30 days>>` |
| 1.11 🟢 | Which funnel step is **weakest** right now, and how do you know? | `<<STEP + NUMBER + WHERE YOU SAW IT>>` |
| 1.12 🟢 | Which **analytics tool** do we use? | `<<PostHog / Amplitude / Mixpanel / GA4 / Other: ___ / None yet>>` |
| 1.13 🔵 | Which **tag or event manager** do we use? | `<<Google Tag Manager / Segment / None>>` |
| 1.14 🟢 | Which **feature-flag / experiment tool** do we use? (A feature flag is an on/off switch for a change.) | `<<LaunchDarkly / Statsig / GrowthBook / Unleash / Own code / None>>` |
| 1.15 🟢 | Link to the **main dashboard** | `<<URL>>` |
| 1.16 🟢 | Link to the **event dictionary** (the list of everything we track). If none exists, write `NONE - create one before Beta`. | `<<URL OR PATH>>` |
| 1.17 🟢 | Who may **approve** experiments? | Product: `<<NAME>>` / Engineering: `<<NAME>>` / QA: `<<NAME>>` / Data: `<<NAME>>` / Privacy or Legal: `<<NAME>>` |
| 1.18 🟢 | **Things we must NEVER test** (examples: changing payments without sign-off, hiding legal text) | `<<LIST>>` |
| 1.19 🟢 | **Most tests allowed at the same time** (so tests do not disturb each other) | `<<e.g. 2>>` |
| 1.20 🔵 | Where do we talk about experiments (chat channel, meeting day and time)? | `<<CHANNEL / DAY / TIME>>` |

---

# Part 2. The 4 Stages (from first build to 500 customers)

Pick the stage you are in. Each stage has a different goal, so the tests look different.

| Stage | Who uses it | Main question | Good example tests | You may leave the stage when... |
|---|---|---|---|---|
| **Build** (and internal testing) | Team only | "Does it work, and do we count things correctly?" | Tracking check (A/A test), QA of events, prototype shown to 3-5 friends | All key events are checked, QA signed off, no serious bugs |
| **Beta** (private test, about 1-50 users) | Invited users | "Do real people understand it and get value?" | Interviews, hand-made service ("Concierge"), onboarding changes, fake-door test | At least 5 users reached the "aha moment" and the team knows the top 3 problems |
| **Launch** (public) | Anyone | "Can strangers find it, sign up and start?" | Landing page headline, sign-up form, pricing page, launch message | The funnel (Part 1, question 1.10) is tracked from start to end and the first paying customers exist |
| **Growth** (to 500 customers) | Customers | "How do we get more customers and keep them?" | First-use steps, price tests, reminder emails, referral offers, channel tests | Customer count (1.8) reaches the goal (1.6) |

**Stage rules**
- One experiment belongs to **one** stage.
- In Build and Beta you will have very few users. Prefer the methods marked "Small numbers OK" in Section 4.
- Do not run Growth-style price or growth tests until Launch tracking is checked.

---

# Part 3. Idea Backlog (a parking lot for ideas, scored)

> Anyone may add an idea. Ideas are **not** experiments yet. Score them, then pick the best one for a real entry (Part 7).

**How to score (each from 1 to 5)**
- **Impact:** how big is the win if it works? (5 = huge)
- **Confidence:** how sure are we, with proof? (5 = very sure)
- **Ease:** how easy and quick to do? (5 = very easy)
- **Score** = Impact x Confidence x Ease (highest is 125).

| Idea ID | Idea (one sentence) | Funnel step | Stage | Proof or reason | Impact | Confidence | Ease | Score | Idea status | Linked experiment |
|---|---|---|---|---|---|---|---|---|---|---|
| `<<CODE>>-IDEA-001` | `<<IDEA>>` | `<<STEP>>` | `<<STAGE>>` | `<<LINK OR NOTE>>` | `<<1-5>>` | `<<1-5>>` | `<<1-5>>` | `<<NUMBER>>` | New | - |

**Idea status values:** `New | Chosen | Parked | Rejected`.
**Rules**
- Only pick an idea with a high score **and** only if the number of running tests stays within question 1.19.
- When you pick an idea, change its status to `Chosen` and write the new experiment ID in "Linked experiment".
- Never delete an idea. Mark it `Parked` or `Rejected` and write why.

---

# Part 4. Experiment Index (one row per experiment)

> 🤖 Agents: keep this table sorted by ID. Never delete a row. Use `Archived` instead.

| ID | Title | Stage | Type | Funnel step | Owner | Status | Start | End | Decision | Link |
|---|---|---|---|---|---|---|---|---|---|---|
| `<<CODE>>-EXP-001` | `<<SHORT TITLE>>` | Build | `<<TYPE>>` | `<<STEP>>` | `<<NAME>>` | Idea | - | - | - | `<<link to entry>>` |
| | | | | | | | | | | |

**ID rule:** your project code + `-EXP-` + a 3-digit number that goes up by one. Example: `SHOP-EXP-001`, `SHOP-EXP-002`. Never reuse an ID.

---

# Part 5. Rules, Status Steps, Decision Log and Lessons Library

## 5.1 Status steps

An experiment moves in this order. Do not skip a step.

```
Idea -> Ready -> Running -> Analyzing -> Decided -> Archived
```

| Status | Meaning | You may move on when... |
|---|---|---|
| **Idea** | Someone picked an idea. Still being planned. | Sections 1-8 are answered |
| **Ready** | Fully planned, approved, tracking checked. | The Part 8 checklist is 100% ticked, approvers signed (Section 12), and reviewers signed Sections 1-12 (Section 17) |
| **Running** | Real users are in the test right now. | The planned end date or a stop rule is reached |
| **Analyzing** | The test stopped. We are looking at the numbers. | Section 14 (Results) is filled |
| **Decided** | A decision is made and written down. | Sections 15-16 are filled, reviewers signed Sections 13-16, and the Decision Log is updated |
| **Archived** | Finished and filed. Nothing left to do. | (final) |

Two side-statuses you may write in the Status field: `Paused` (stopped on purpose, will restart) and `Stopped Early` (ended before the plan, with the reason in the Run Log).

## 5.2 Decision choices (pick exactly one)

| Decision | Use it when... | What happens next |
|---|---|---|
| **Ship** | The change clearly helped and nothing important got worse. | Turn it on for everyone. Remove the old version and the switch. |
| **Iterate** | There is a good sign, but it is not good enough yet. | Make a NEW experiment (new ID) with a better idea. |
| **Kill** | It did not help, or it caused harm. | Turn the change off. Write why. |
| **Need more data** | The result is unclear or too few people took part. | Extend **once only**, or redesign. |

## 5.3 Decision Log (one row per finished experiment)

| Date | ID | Decision | One-sentence reason (with a number) | Decided by | Follow-up ID(s) |
|---|---|---|---|---|---|
| `<<YYYY-MM-DD>>` | `<<CODE>>-EXP-001` | Ship / Iterate / Kill / Need more data | `<<e.g. "Sign-up rate rose from 38% to 45% in 14 days.">>` | `<<NAME>>` | `<<ID or ->>` |

## 5.4 Lessons Library (the most useful table for your next project)

| ID | Lesson in one sentence | Tags (pick 1-3) | Useful for future projects? |
|---|---|---|---|
| `<<CODE>>-EXP-001` | `<<LESSON>>` | `<<onboarding / pricing / copy / tracking / channel / retention / technical>>` | Yes / No |

---

# Part 6. Weekly Review (20 minutes, same time every week)

**Who comes:** register owner, product, engineering, and anyone who owns a running experiment.
**Before the meeting (5 minutes, owner of each running test):** update the Run Log (Section 13) and check your safety numbers.

| Minutes | Agenda item | Questions to ask | Output |
|---|---|---|---|
| 0-3 | **Goal check** | How many customers now (1.8)? Are we on track for the goal (1.6)? | Update 1.8 |
| 3-9 | **Running experiments** | Is each test within its min and max days? Is any safety number in danger? Is tracking still working? | Continue / Pause / Stop Early |
| 9-14 | **Tests that ended** (status `Analyzing`) | Are Results (Section 14) filled? Are we ready to decide? Does a human confirm the decision? | Decisions logged in Part 5 |
| 14-18 | **Idea Backlog** | Which top-scored idea should start next? Is there room (1.19)? | Chosen idea gets an entry |
| 18-20 | **Actions** | Who does what by when? | Action list below |

**Weekly rules**
- Nobody decides on a test before its minimum days and minimum people (Section 7) are reached.
- If a safety number is broken, stop the test first and talk after.
- Every review ends with at least one written action and one owner.

| Week of | Attendees | Tests reviewed | Decisions made | Actions (who / what / by when) |
|---|---|---|---|---|
| `<<YYYY-MM-DD>>` | `<<NAMES>>` | `<<IDs>>` | `<<IDs + decision>>` | `<<ACTIONS>>` |

---

# Part 7. Experiment Entry Template

> **How to use:** Copy everything between `START OF ENTRY` and `END OF ENTRY`. Paste it into Part 9 under a heading with the new ID. Replace each `<<...>>`. Answer in order. Do not skip.

<!-- ================= START OF ENTRY ================= -->

## <<CODE>>-EXP-XXX: <<SHORT TITLE, 5-8 WORDS>>

| Field | Value |
|---|---|
| **Status** 🟢 | `Idea \| Ready \| Running \| Analyzing \| Decided \| Archived \| Paused \| Stopped Early` |
| **Stage** 🟢 | `Build \| Beta \| Launch \| Growth` |
| **Owner** 🟢 | `<<ONE NAME>>` |
| **Created on** 🟢 | `<<YYYY-MM-DD>>` |
| **Last updated** 🟢 | `<<YYYY-MM-DD>>` |
| **Idea it came from** 🔵 | `<<CODE>>-IDEA-XXX` |

### Section 1. Basics

| # | Question | Your answer |
|---|---|---|
| 1.1 🟢 | **Type of experiment** (pick one) | `Feature \| Onboarding \| Pricing \| Message/Copy \| Acquisition channel \| Retention/Email \| Technical/Speed \| Tracking check \| Fake-door \| Manual (Concierge)` |
| 1.2 🟢 | **Which funnel step** (from Part 1, question 1.10) are we trying to improve? | `<<STEP>>` |
| 1.3 🟢 | **How does this help us reach the customer goal?** (one sentence) | `<<e.g. "More sign-ups means more chances to get paying customers.">>` |
| 1.4 🟢 | **Score** (copy from the Idea Backlog) | Impact `<<1-5>>` x Confidence `<<1-5>>` x Ease `<<1-5>>` = `<<TOTAL>>` |

### Section 2. Why are we doing this? (the problem)

| # | Question | Your answer |
|---|---|---|
| 2.1 🟢 | **What problem did we see?** | `<<WHAT HAPPENED>>` |
| 2.2 🟢 | **How do we know?** Give proof: a number, a user quote, a bug report, a dashboard link. | `<<PROOF + LINK>>` |
| 2.3 🟢 | **What happens if we do nothing?** | `<<RESULT>>` |

### Section 3. Our guess (the hypothesis)

Finish this sentence. All 3 blanks are required.

> **If we** `<<CHANGE THIS>>`, **then** `<<THIS NUMBER>>` **will** `<<GO UP or GO DOWN>> by <<HOW MUCH>>`, **because** `<<REASON>>`.

| # | Question | Your answer |
|---|---|---|
| 3.1 🟢 | **What result would show we were wrong?** | `<<e.g. "Sign-up rate stays at 4% or goes down.">>` |

### Section 4. What exactly do we change?

| # | Question | Your answer |
|---|---|---|
| 4.1 🟢 | **Method** (pick one, see the table below) | `A/B test \| Before-and-after \| Step-by-step rollout \| Fake-door \| Concierge \| Interviews \| A/A tracking check` |
| 4.2 🟢 | **A = what people see today (control)** | `<<DESCRIBE OR SCREENSHOT LINK>>` |
| 4.3 🟢 | **B = what people will see in the test (variant)** | `<<DESCRIBE OR SCREENSHOT / DESIGN LINK>>` |
| 4.4 🟢 | **Is there only ONE change between A and B?** If not, split it into separate tests. | `Yes \| No - reason: <<...>>` |
| 4.5 🔵 | **Name of the on/off switch (feature flag)** | `<<flag_name_in_snake_case>>` |

**Which method should I pick?**

| Method | Good when... | Small numbers OK? |
|---|---|---|
| A/B test | You have many visitors (hundreds per week or more) | No |
| Before-and-after | You cannot split users, so you compare "last 2 weeks" with "next 2 weeks" | Somewhat |
| Step-by-step rollout | The change is risky: show to 5%, then 25%, then 100% | Somewhat |
| Fake-door | You want to know if people want something **before** you build it (a button that says "coming soon") | Yes |
| Concierge (by hand) | You do the service by hand for a few people to learn what they need | Yes |
| Interviews | You talk to 5-10 people | Yes |
| A/A tracking check | You split users but change nothing, to prove your tracking is fair (Build stage) | No |

### Section 5. Who is in the test?

| # | Question | Your answer |
|---|---|---|
| 5.1 🟢 | **Who can enter?** (new users / all users / paying users / one country / one device) | `<<WHO>>` |
| 5.2 🟢 | **Who is left out?** (team members, test accounts, people already in another test) | `<<WHO>>` |
| 5.3 🟢 | **How are people split?** | `<<e.g. "Half see A, half see B, chosen by chance">>` |
| 5.4 🟢 | **Does this overlap with another running test?** | `No \| Yes - ID: <<...>> and how we stop them mixing: <<...>>` |

### Section 6. How will we know? (measures)

| # | Question | Your answer |
|---|---|---|
| 6.1 🟢 | **MAIN number (only one).** Give it a name. | `<<e.g. "Sign-up rate">>` |
| 6.2 🟢 | **How is it calculated?** (top number divided by bottom number) | `<<e.g. "people who finished sign-up / people who opened the form">>` |
| 6.3 🟢 | **The number today (baseline)** and **where we found it** | `<<VALUE>>` from `<<DASHBOARD LINK + DATE RANGE>>` |
| 6.4 🟢 | **Target number** (what would make us happy) | `<<VALUE>>` |
| 6.5 🟢 | **Safety numbers (guardrails).** These must NOT get worse. List 1-3 and the limit for each. | `<<e.g. "Payment success stays above 95%. Page opens in under 3 seconds.">>` |
| 6.6 🔵 | **Helper numbers** (extra things to watch, not used to decide) | `<<LIST>>` |

### Section 7. When do we stop? (simple rules)

| # | Question | Your answer |
|---|---|---|
| 7.1 🟢 | **Start date** | `<<YYYY-MM-DD>>` |
| 7.2 🟢 | **Shortest it may run** (rule of thumb: at least 7 full days so every weekday counts) | `<<DAYS>>` |
| 7.3 🟢 | **Longest it may run** (rule of thumb: no more than 28 days) | `<<DAYS>>` |
| 7.4 🟢 | **Smallest number of people needed in EACH group before we look** | `<<NUMBER>>` |
| 7.5 🟢 | **Early-stop rule** (stop right away if a safety number in 6.5 breaks) | `<<RULE>>` |
| 7.6 🟢 | **Promise:** we will NOT decide before 7.2 and 7.4 are met. | `[ ] I promise` |

> ⚠️ **Small Numbers Warning.** With fewer than about 500 customers, most A/B tests cannot give a trustworthy answer. If your groups are small, choose Fake-door, Concierge, Interviews or Before-and-after in 4.1, and write "directional only" in Section 14.

<details>
<summary>🔵 Advanced (optional): only for people who know statistics</summary>

| # | Item | Your answer |
|---|---|---|
| 7.A1 | Smallest change worth finding (minimum detectable effect) | `<<VALUE>>` |
| 7.A2 | Significance level (usual: 5%) | `<<VALUE>>` |
| 7.A3 | Power (usual: 80%) | `<<VALUE>>` |
| 7.A4 | People needed per group, and how you worked it out | `<<NUMBER + TOOL>>` |
| 7.A5 | Test type (one-sided or two-sided; frequentist or Bayesian) | `<<CHOICE>>` |
| 7.A6 | How you handle several variants or several numbers at once | `<<METHOD>>` |
</details>

### Section 8. Tracking checklist (instrumentation)

> No tracking = no experiment. Write down every event the test needs and check each one.

| # | Event name (`object_action`, lowercase, underscores) | When does it fire? | Details it carries (properties) | Who builds it | Checked in test area (staging)? | Checked live (production)? |
|---|---|---|---|---|---|---|
| 8.1 | `<<e.g. signup_completed>>` | `<<e.g. "User taps Create account and the server says OK">>` | `<<e.g. user_id, variant, source>>` | `<<NAME>>` | `[ ]` | `[ ]` |
| 8.2 | | | | | `[ ]` | `[ ]` |

| # | Tracking question | Your answer |
|---|---|---|
| 8.A 🟢 | Does the data **say which group (A or B)** the person was in? | `Yes - property name: <<variant>> \| No - fix first` |
| 8.B 🟢 | Is every event **listed in the event dictionary** (Part 1, question 1.16)? | `Yes \| No - fix first` |
| 8.C 🟢 | Did **someone other than the builder** test each event and see it appear in the analytics tool? | `Yes - <<NAME, DATE>>` |
| 8.D 🟢 | Does the **dashboard or report** for this test exist? | `<<LINK>>` |
| 8.E 🟢 | Are **test accounts and team members** filtered out of the numbers? | `Yes \| No - fix first` |

### Section 9. Stage questions (answer ONLY the block for your stage)

**If your stage is Build (does it work, and do we count correctly?)**

| # | Question | Your answer |
|---|---|---|
| 9.B1 🟢 | Which parts of the product does this check? | `<<LIST>>` |
| 9.B2 🟢 | Which phones, computers and browsers did we test on? | `<<LIST>>` |
| 9.B3 🟢 | Does each event fire **exactly once** per action (not zero, not twice)? | `Yes \| No - what we saw: <<...>>` |
| 9.B4 🟢 | Do the numbers in the analytics tool **match** our own database for the same day? | `Yes \| No - difference: <<...>>` |
| 9.B5 🟢 | Who is allowed to use the product at this stage? | `<<TEAM ONLY / FRIENDS / OTHER>>` |

**If your stage is Beta (do real people understand it and get value?)**

| # | Question | Your answer |
|---|---|---|
| 9.P1 🟢 | How many people are in the test and how did we find them? | `<<NUMBER + HOW>>` |
| 9.P2 🟢 | Did they **agree** to be part of the test and to be contacted? | `Yes - proof: <<LINK>> \| No - STOP` |
| 9.P3 🟢 | What is the **"aha moment"** (the first time a user clearly gets value)? How do we count it? | `<<DEFINITION>>` |
| 9.P4 🟢 | How will we collect feedback? | `Interview \| Survey \| Watching them use it \| Other: <<...>>` |
| 9.P5 🟢 | Are these people **like our real future customers**? If not, how do they differ? | `<<ANSWER>>` |

**If your stage is Launch (can strangers find it, sign up and start?)**

| # | Question | Your answer |
|---|---|---|
| 9.L1 🟢 | Where will people come from (channel)? Are the links tagged so we can see the source? | `<<CHANNEL + YES/NO>>` |
| 9.L2 🟢 | Is the path from first visit to sign-up tracked from start to end? | `Yes \| No - fix first` |
| 9.L3 🟢 | Is the system ready for more visitors than usual? | `Yes - checked by <<NAME>> \| No - fix first` |
| 9.L4 🟢 | Is someone ready to answer questions from new users (support)? | `Yes - <<NAME>> \| No` |
| 9.L5 🟢 | Is the message honest (no false promises)? | `Yes - checked by <<NAME>>` |

**If your stage is Growth (how do we get more customers and keep them?)**

| # | Question | Your answer |
|---|---|---|
| 9.G1 🟢 | How many customers do we have now, and how many do we need? | Now: `<<NUMBER>>` / Goal: `<<NUMBER>>` |
| 9.G2 🟢 | About how many **extra customers** do we hope this adds? (Rough guess is fine. Write "guess".) | `<<NUMBER, guess>>` |
| 9.G3 🟢 | Could this **upset current paying customers**? How do we protect them? | `<<ANSWER>>` |
| 9.G4 🟢 | How long until we can see the effect? (Example: a reminder email shows results in 7 days; "still using after 30 days" needs 30 days.) | `<<DAYS>>` |
| 9.G5 🟢 | If it involves money or price: did we check refund rules and the law with the right person? | `N/A \| Yes - <<NAME, DATE>> \| No - STOP` |
| 9.G6 🔵 | If it costs money to bring in customers: how much does one new customer cost us? | `<<AMOUNT or N/A>>` |

### Section 10. What could go wrong? (risks, safety and rollback)

| # | Question | Your answer |
|---|---|---|
| 10.1 🟢 | **List up to 3 risks** (ways it could hurt users, money, trust or the system) | `<<RISK 1 / RISK 2 / RISK 3>>` |
| 10.2 🟢 | **Who is on call** if something breaks? | `<<NAME + CONTACT>>` |
| 10.3 🟢 | **Rollback plan:** the exact steps to turn it off | `<<e.g. "Switch flag short_signup_form to OFF in the flag tool.">>` |
| 10.4 🟢 | **How long does a rollback take?** | `<<MINUTES>>` |
| 10.5 🟢 | **Can users go back to the old experience?** | `Yes \| No - extra approval needed` |

### Section 11. Privacy and consent check

| # | Question | Your answer |
|---|---|---|
| 11.1 🟢 | Does this test collect or use **personal data** (name, email, phone, location, device ID)? | `No \| Yes - which: <<LIST>>` |
| 11.2 🟢 | If yes: did users **agree** (consent) in a way we can prove? | `N/A \| Yes - proof: <<LINK>> \| No - STOP and ask the privacy owner` |
| 11.3 🟢 | Are we tracking **children under 16** or sensitive data (health, money details, ID numbers)? | `No \| Yes - STOP and get written approval` |
| 11.4 🟢 | Do we follow our **data-keeping rules** (how long we keep data)? | `Yes \| Unsure - ask <<NAME>>` |
| 11.5 🔵 | Is the text users see **honest** (no tricks, no fake urgency, no hidden costs)? | `Yes \| Unsure - ask <<NAME>>` |

### Section 12. Approvals (sign before the test goes live)

| Role | Name | Approved? (tick and date) | Notes |
|---|---|---|---|
| Product | `<<NAME>>` | `[ ] <<DATE>>` | |
| Engineering | `<<NAME>>` | `[ ] <<DATE>>` | |
| QA | `<<NAME>>` | `[ ] <<DATE>>` | |
| Data / Analytics | `<<NAME>>` | `[ ] <<DATE>>` | |
| Privacy or Legal (needed only if 11.1 is "Yes") | `<<NAME>>` | `[ ] <<DATE>>` | |

### Section 13. Run Log (add a line every time something happens)

| Date and time | Who | What happened (launched / paused / bug / change / checked numbers / stopped) | Numbers at that time (if any) |
|---|---|---|---|
| `<<YYYY-MM-DD HH:MM>>` | `<<NAME>>` | `<<EVENT>>` | `<<NUMBERS or ->>` |

> Rule: do not change Sections 3, 4 or 6 after launch. If you must change something, write it here and think about starting a new experiment.

### Section 14. Results (fill after the test ends)

| # | Question | Your answer |
|---|---|---|
| 14.1 🟢 | **Real start and end dates** | `<<START>> to <<END>>` |
| 14.2 🟢 | **People in A / people in B** | A: `<<NUMBER>>` / B: `<<NUMBER>>` |
| 14.3 🟢 | **Main number: A vs B** | A: `<<VALUE>>` / B: `<<VALUE>>` / Change: `<<+ or - VALUE>>` |
| 14.4 🟢 | **Safety numbers: did any break?** | `No \| Yes - which: <<...>>` |
| 14.5 🟢 | **Did we meet the rules in 7.2 and 7.4?** | `Yes \| No - what was missing: <<...>>` |
| 14.6 🟢 | **How sure are we?** | `Strong (clear difference, enough people) \| Medium \| Directional only (too few people)` |
| 14.7 🟢 | **Did anything odd happen?** (outage, holiday, big advert, bug) | `<<DESCRIBE or "Nothing odd">>` |
| 14.8 🟢 | **Was our guess in Section 3 right?** | `Right \| Wrong \| Partly \| Cannot tell` |
| 14.9 🟢 | **Link to the report or dashboard that shows the proof** | `<<URL>>` |

### Section 15. Decision

| # | Question | Your answer |
|---|---|---|
| 15.1 🟢 | **Decision** | `Ship \| Iterate \| Kill \| Need more data` |
| 15.2 🟢 | **Reason in one sentence, with a number** | `<<REASON>>` |
| 15.3 🟢 | **Decided by (a human) and date** | `<<NAME, YYYY-MM-DD>>` |
| 15.4 🟢 | **Next action, owner and due date** | `<<ACTION / NAME / DATE>>` |
| 15.5 🟢 | **Switch cleanup:** is the feature flag removed or set to 100%? | `[ ] Done <<DATE>> \| N/A` |

### Section 16. Lessons learned

| # | Question | Your answer |
|---|---|---|
| 16.1 🟢 | **What did we learn about our users?** | `<<LESSON>>` |
| 16.2 🟢 | **What did we learn about how we run tests?** | `<<LESSON>>` |
| 16.3 🟢 | **What would we do differently next time?** | `<<LESSON>>` |
| 16.4 🔵 | **New ideas that came from this** (add them to the Idea Backlog) | `<<IDEA or ID>>` |

### Section 17. Reviewer sign-off (a second person checks each section)

> **Rule:** the reviewer must be a **different person** from the one who wrote the section.
> **"Complete"** = every required answer is filled (or marked `N/A` / `UNKNOWN` with a reason).
> **"Clear"** = someone new to the project could understand it with no extra help.
> Sections 1-12 must be signed before status `Ready`. Sections 13-16 must be signed before status `Decided`.

| Section | Reviewer name | Date | Complete? | Clear? | Notes or fixes needed |
|---|---|---|---|---|---|
| 1 Basics | | | `[ ]` | `[ ]` | |
| 2 Why | | | `[ ]` | `[ ]` | |
| 3 Our guess | | | `[ ]` | `[ ]` | |
| 4 What we change | | | `[ ]` | `[ ]` | |
| 5 Who is in the test | | | `[ ]` | `[ ]` | |
| 6 Measures | | | `[ ]` | `[ ]` | |
| 7 Stop rules | | | `[ ]` | `[ ]` | |
| 8 Tracking | | | `[ ]` | `[ ]` | |
| 9 Stage questions | | | `[ ]` | `[ ]` | |
| 10 Risks and rollback | | | `[ ]` | `[ ]` | |
| 11 Privacy | | | `[ ]` | `[ ]` | |
| 12 Approvals | | | `[ ]` | `[ ]` | |
| 13 Run Log | | | `[ ]` | `[ ]` | |
| 14 Results | | | `[ ]` | `[ ]` | |
| 15 Decision | | | `[ ]` | `[ ]` | |
| 16 Lessons | | | `[ ]` | `[ ]` | |

<!-- ================== END OF ENTRY ================== -->

---

# Part 8. "Ready to Run" Checklist (every box must be ticked before status = Ready)

Copy this under each entry. Tick a box only if it is **really** true.

- [ ] Sections 1-9 are fully answered (no blank and no `<<...>>` left).
- [ ] There is **one** main number, with a number-today (baseline) and a target.
- [ ] Safety numbers and their limits are written down.
- [ ] Shortest days, longest days and smallest number of people are written down.
- [ ] Every event is in the tracking table and in the event dictionary.
- [ ] A second person tested each event and saw it appear in the analytics tool.
- [ ] The group (A or B) is recorded on the events.
- [ ] Test accounts and team members are filtered out.
- [ ] The stage questions in Section 9 are answered for the right stage.
- [ ] The rollback plan is written and someone practised it once.
- [ ] The privacy check is answered and nothing says STOP.
- [ ] No overlap with another running test (or an overlap plan is written).
- [ ] The number of running tests stays within Part 1, question 1.19.
- [ ] All approvals in Section 12 are signed by humans.
- [ ] Reviewers signed Sections 1-12 in Section 17.
- [ ] The Index row (Part 4) is added and the status is updated.

---

# Part 9. Experiment Entries (paste your entries below this line)

## Example 1 (Launch stage, A/B test): SHOP-EXP-001, Shorter Sign-Up Form

> Worked examples show what good answers look like. Delete them in your own project when you are comfortable.

| Field | Value |
|---|---|
| **Status** | Decided |
| **Stage** | Launch |
| **Owner** | Priya |
| **Created / Updated** | 2026-09-01 / 2026-09-24 |

**1 Basics:** Type: Onboarding. Funnel step: Visit -> Sign up. It helps the customer goal because more sign-ups means more chances to get paying customers. Score: 4 x 3 x 5 = 60.
**2 Why:** 62% of people who open the sign-up form leave without finishing (dashboard, 2026-08-15 to 2026-08-31). Three beta users said the form "asks too much". If we do nothing, sign-ups stay near 4 per 100 visitors.
**3 Guess:** If we cut the form from 6 fields to 3, then the sign-up rate will go up by 1.5 points or more, because fewer fields means less effort. We are wrong if the rate stays at 4% or falls.
**4 Change:** Method: A/B test. A = 6-field form. B = name, email, password only. Only one change: yes. Switch: `short_signup_form`.
**5 Who:** New visitors, all countries, phone and computer. Left out: team members and test accounts. Split 50/50 by chance. No overlap with other tests.
**6 Measures:** Main number = sign-up rate (people who finish sign-up / people who open the form). Today: 38% (dashboard, 2026-08-15 to 2026-08-31). Target: 43%. Safety: spam sign-ups under 2%; page opens in under 3 seconds.
**7 Stop rules:** Start 2026-09-03. At least 14 days, at most 28. At least 400 people per group. Stop early if spam goes over 5%. Promise made.
**8 Tracking:** `signup_form_opened` and `signup_completed`, both carry `variant`. Tested in staging by Marco (2026-09-02) and live (2026-09-03). Dashboard exists. Test accounts filtered.
**9 Launch questions:** Source links tagged: yes. Start-to-end path tracked: yes. System ready: checked by Marco. Support ready: Dana. Message honest: yes.
**10 Risks:** More spam accounts. Rollback: turn `short_signup_form` OFF, about 1 minute. On call: Marco. Users can go back: yes.
**11 Privacy:** Name and email only, same as before. Consent text unchanged. No children's data.
**12 Approvals:** Product, Engineering, QA, Data signed on 2026-09-02.
**13 Run Log:** 2026-09-03 launched. 2026-09-10 safety numbers fine. 2026-09-17 reached 14 days and 400+ per group.
**14 Results:** 2026-09-03 to 2026-09-17. A: 612 people, B: 598 people. Sign-up rate A = 38.1%, B = 44.6% (+6.5 points). Spam 1.1%. Nothing odd. Sure: Medium. Guess was right.
**15 Decision:** Ship. The rate rose from 38.1% to 44.6% with spam under the limit. Decided by Priya on 2026-09-24. Next: remove old form and switch by 2026-10-01.
**16 Lessons:** Users prefer fewer fields at the first step. Ask for extra details after first use. Next time run 28 days to include weekend effects.
**17 Reviewer sign-off:** All 16 sections signed by Marco and Dana (different from the writers).

## Example 2 (Beta stage, Concierge test): SHOP-EXP-002, Do Shop Owners Want a Daily Summary?

| Field | Value |
|---|---|
| **Status** | Decided |
| **Stage** | Beta |
| **Owner** | Marco |
| **Created / Updated** | 2026-08-10 / 2026-08-24 |

**1 Basics:** Type: Manual (Concierge). Funnel step: First use -> Still using. Helps the goal because shops that come back are more likely to pay. Score: 5 x 3 x 4 = 60.
**2 Why:** Only 2 of 8 beta shops opened the app after day 3 (dashboard). Two said "I forget to check it". If we do nothing, we may build the wrong feature.
**3 Guess:** If we send each beta shop a hand-made daily sales summary by message, then at least 5 of 8 shops will open the app within 2 days of getting it, because a summary shows them the value without effort. We are wrong if fewer than 3 shops open the app.
**4 Change:** Method: Concierge. A = nothing sent (last week). B = summary message sent by Marco each evening at 7pm. One change: yes. No switch needed.
**5 Who:** The 8 beta shops. Left out: none. Everyone gets B (compare with last week).
**6 Measures:** Main number = shops that open the app within 2 days of the summary. Today: 2 of 8. Target: 5 of 8. Safety: no shop asks us to stop messages.
**7 Stop rules:** 2026-08-12 start. At least 7 days, at most 14. Group is small, so the result is "directional only". Promise made.
**8 Tracking:** `app_opened` (with `shop_id`) tested by Dana on 2026-08-11. Summary sends noted by hand in the Run Log. Test accounts filtered.
**9 Beta questions:** 8 shops found through the owner's friend list. All agreed in writing (link). Aha moment = seeing the first day's total in the app. Feedback by 10-minute phone call. Shops are like our real future customers: yes.
**10 Risks:** Messages feel annoying. Rollback: stop sending. On call: Marco. Reversible: yes.
**11 Privacy:** Uses shop phone numbers they gave for this test, with written consent. No children's data.
**12 Approvals:** Product and Data signed on 2026-08-11. Privacy owner signed (phone numbers used).
**13 Run Log:** 2026-08-12 first summary sent. 2026-08-16 one shop said "very useful". 2026-08-19 safety fine.
**14 Results:** 2026-08-12 to 2026-08-19. 6 of 8 shops opened the app within 2 days. No stop requests. Sure: Directional only (8 shops). Guess was right.
**15 Decision:** Iterate. Six of 8 shops responded, so build an automatic daily summary (new test SHOP-EXP-005). Decided by Marco on 2026-08-24.
**16 Lessons:** Shops respond to simple results shown for free. Always ask phone-call feedback within 24 hours. Next time record why the 2 shops did not open the app.

## Example 3 (Growth stage, Before-and-after): SHOP-EXP-003, Reminder Email After Sign-Up

| Field | Value |
|---|---|
| **Status** | Analyzing |
| **Stage** | Growth |
| **Owner** | Priya |
| **Created / Updated** | 2026-10-01 / 2026-10-17 |

**1 Basics:** Type: Retention/Email. Funnel step: Sign up -> First use. Helps the goal because people who use the app once are more likely to pay. Score: 4 x 4 x 4 = 64.
**2 Why:** 41% of new sign-ups never add their first sale (dashboard, September). If we do nothing, we waste half of the sign-ups we already paid to get.
**3 Guess:** If we send a reminder email 24 hours after sign-up, then the share who add a first sale within 3 days will go up from 59% to 65% or more, because they get a nudge at the right time. We are wrong if it stays below 62%.
**4 Change:** Method: Before-and-after (we cannot split users with our email tool yet). A = sign-ups from 2026-09-15 to 2026-09-28 (no email). B = sign-ups from 2026-10-01 to 2026-10-14 (email on). One change: yes. Switch: `first_use_reminder_email`.
**5 Who:** All new sign-ups. Left out: team and test accounts. No other test overlaps.
**6 Measures:** Main number = share of new sign-ups who add a first sale within 3 days. Today: 59%. Target: 65%. Safety: email unsubscribe rate under 2%.
**7 Stop rules:** 14 days, shortest 14, longest 21. At least 150 people per period. Stop early if unsubscribes exceed 5%.
**8 Tracking:** `first_sale_added` and `reminder_email_sent`, tested by Marco on 2026-09-30.
**9 Growth questions:** Customers now 212, goal 500. Hope to add about 10 extra paying customers (guess). Current customers are not emailed. Effect visible in 3 days. No money or price change. Cost per new customer: N/A.
**10 Risks:** Email looks like spam. Rollback: set the switch OFF, 1 minute. On call: Priya. Reversible: yes.
**11 Privacy:** Uses email addresses already collected with consent for product emails. No children's data.
**12 Approvals:** Signed by Product, Engineering, QA, Data on 2026-09-30.
**13 Run Log:** 2026-10-01 launched. 2026-10-08 unsubscribes 0.9%. 2026-10-14 period ended.
**14 Results:** (in progress) A: 168 people, B: 171 people. First-sale share A = 59%, B = 63%. Unsubscribes 1.1%. Compared with a different calendar period, so Sure: Directional only. Waiting for the human decision.

---

# Part 10. Naming and Quality Rules

## 10.1 Naming rules (so everyone writes the same way)

| Thing | Rule | Good example | Bad example |
|---|---|---|---|
| Experiment ID | project code + `-EXP-` + 3 digits | `SHOP-EXP-014` | `exp14`, `Test A` |
| Idea ID | project code + `-IDEA-` + 3 digits | `SHOP-IDEA-007` | `idea 7` |
| Event name | `object_action`, lowercase, past tense, underscores | `signup_completed` | `Sign Up Done!` |
| Property name | lowercase with underscores | `plan_type` | `PlanType` |
| Feature flag | lowercase with underscores, says what it does | `short_signup_form` | `flag1` |
| Dates | `YYYY-MM-DD` | `2026-11-15` | `15/11/26` |
| Percent change | say "points" or "percent" | `+6.5 points` | `6.5` |

## 10.2 "Good answer" versus "bad answer"

| Question | Bad answer (guessing) | Good answer (clear) |
|---|---|---|
| What is the main number? | "Engagement" | "Share of new users who finish setup within 24 hours" |
| How long will it run? | "A while" | "Shortest 14 days, longest 28 days" |
| What is the target? | "Higher" | "From 38% to 43%" |
| What is the rollback? | "We will fix it" | "Set switch `short_signup_form` to OFF, about 1 minute" |

## 10.3 Tool hints (use with your own tools from Part 1, questions 1.12-1.14)

| Tool type | Where numbers for Sections 6 and 14 usually come from | Tip |
|---|---|---|
| PostHog | Insights, Funnels, Experiments | Use one feature flag key per experiment. Save the insight link in 14.9. |
| Amplitude | Charts, Funnels, Experiment | Add `variant` as an event or user property. |
| Mixpanel | Funnels, Retention, Experiments | Name the report after the experiment ID. |
| GA4 / Tag Manager | Explore reports. Tag Manager Preview mode to test events. | Mark key actions as key events. Test in Preview before launch. |
| Feature-flag tools (LaunchDarkly, Statsig, GrowthBook, Unleash) | Flag dashboard and exposure logs | Log "exposure" when a person actually **sees** the change, not only when the page loads. |

## 10.4 Common mistakes (read before you start)

1. Testing more than one change at once, so you cannot tell what worked.
2. Looking at the numbers every day and stopping as soon as they look good.
3. Forgetting to filter out team and test accounts.
4. Not recording which group (A or B) each person was in.
5. Starting a test that mixes with another running test.
6. Calling a small-group result "proven". Write "directional only" instead.
7. Forgetting to remove the on/off switch (feature flag) after the decision.
8. Letting the same person write and review a section.

---

# Part 11. Instructions for AI Agents 🤖

> Humans can skip this part. AI agents must follow it exactly when creating, updating or closing entries.

## 11.1 Rules

1. **Never invent data.** If a value is missing or cannot be read from a linked source, write `UNKNOWN - ask <role>`. Do not estimate numbers today (baselines), group sizes or results.
2. **Never change** Sections 3, 4 or 6 after the status is `Running`. Add a line to the Run Log (Section 13) and tell the owner.
3. **Never mark** an entry `Ready` unless the Part 8 checklist is 100% ticked, every approval in Section 12 has a human name and date, and a different human reviewer has signed Sections 1-12 in Section 17.
4. **Never tick a reviewer box** in Section 17 for a section you wrote. Agents may write a section, but a different human (or a different agent plus a human) must review it.
5. **Never write a decision** (Section 15) on behalf of a human. You may write an `AGENT RECOMMENDATION`, but a named human must confirm it.
6. **Always use the exact allowed words** for fields with lists (`Status`, `Stage`, `Method`, `Decision`).
7. **Always update four places** after any change: the entry's `Last updated` date, the Index row (Part 4), the Idea Backlog link (if any), and (if decided) the Decision Log and Lessons Library (Part 5).
8. **Touch only** the entry you were asked to work on.
9. **Stop and ask a human** if: Section 11 contains a `STOP`; a safety number in 6.5 breaks; two running tests overlap; or the number of running tests would go above Part 1, question 1.19.
10. **Cite the source** (dashboard link and date range) for every number you write.
11. **Keep language simple.** Short sentences. Explain any hard word in one line.

## 11.2 What an agent does for each task

| Task given | Agent steps |
|---|---|
| "Create an experiment from this idea" | 1) Read Part 1. 2) Take the next free ID. 3) Copy the Part 7 template. 4) Fill what is known and mark the rest `UNKNOWN - ask <role>`. 5) Set status `Idea`. 6) Add the Index row and link the Idea Backlog row. 7) List open questions for the owner. |
| "Score and rank the backlog" | Read each idea. Fill Impact, Confidence and Ease only when the proof column supports them. Otherwise write `UNKNOWN - ask <role>`. Sort by score. |
| "Check if this is ready" | Go through Part 8 line by line. Report each unticked item with the exact missing field. Do not tick boxes yourself. |
| "Update the run" | Add a Run Log line with date, what happened and numbers (with source). Compare safety numbers (6.5) with stop rules (7.5). If broken, alert a human. |
| "Close this experiment" | Fill Section 14 from the linked report. Check 14.5 honestly. Write an `AGENT RECOMMENDATION` in Section 15. Wait for the human decision. Then update Part 5 and the Index. |
| "Prepare the weekly review" | List running tests with days used, min and max days, and safety number status. List tests in `Analyzing`. List the top 3 backlog ideas. List open `UNKNOWN` items. |
| "Audit the register" | Report: entries with blanks or `UNKNOWN`; entries `Running` past their longest days; entries `Decided` with the switch not cleaned up; duplicate IDs; missing Index rows; missing reviewer sign-offs. |

## 11.3 Machine-readable header (optional, put at the top of each entry for automation)

```yaml
experiment:
  id: CODE-EXP-XXX
  title: "<<TITLE>>"
  stage: Build         # Build | Beta | Launch | Growth
  status: Idea         # Idea | Ready | Running | Analyzing | Decided | Archived | Paused | Stopped Early
  owner: "<<NAME>>"
  type: "<<TYPE>>"
  method: "<<METHOD>>"
  funnel_step: "<<STEP>>"
  source_idea: "CODE-IDEA-XXX"
  primary_metric: "<<METRIC NAME>>"
  baseline: null       # number
  target: null         # number
  guardrails: ["<<METRIC: LIMIT>>"]
  start_date: null     # YYYY-MM-DD
  min_days: null
  max_days: null
  min_per_group: null
  flag_key: "<<flag_name>>"
  reviews_signed: []   # list of section numbers signed by a reviewer
  decision: null       # Ship | Iterate | Kill | Need more data
```

---

# Part 12. Glossary (simple words)

| Word | Simple meaning |
|---|---|
| Experiment | A small test where you change one thing to learn something. |
| Hypothesis | Your best guess about what will happen, and why. |
| Control (A) | What people see today. |
| Variant (B) | The new thing you are testing. |
| Metric | A number you can count. |
| Baseline | The number today, before the test. |
| Guardrail | A safety number that must not get worse. |
| Funnel | The steps a person takes from first visit to becoming a customer. |
| Instrumentation | The tracking code that counts what people do. |
| Event | One thing a person did that we count (for example "signed up"). |
| Property | A detail attached to an event (for example which group the person was in). |
| Feature flag | An on/off switch that turns a change on or off without a new release. |
| Rollback | Turning the change off to go back to how things were. |
| Staging | A safe copy of the product used for testing before real users see changes. |
| Sample size | How many people are in the test. |
| Significance / power / MDE | Advanced ideas that tell you if a difference is real and big enough to notice. Optional. |
| Fake-door test | Showing a button or page for something not built yet, to see if people want it. |
| Concierge test | Doing the service by hand for a few users to learn what they need. |
| Dogfooding | The team uses its own product before customers do. |
| Aha moment (activation) | The first time a new user clearly gets value. |
| Retention | People coming back and still using the product later. |
| Reviewer | A second person who checks that a section is complete and clear. |

---

# Part 13. Template Change Log

| Version | Date | Change | By |
|---|---|---|---|
| 1.0.0 | 2026-10-18 | First draft of the universal Experiment Register template | `<<NAME>>` |
| 1.1.0 | 2026-10-18 | Project-code IDs, plain stage names, numbered parts, Idea Backlog, Weekly Review, stage-specific questions, per-section reviewer sign-off, simpler wording, two more worked examples | `<<NAME>>` |

*End of document.*
