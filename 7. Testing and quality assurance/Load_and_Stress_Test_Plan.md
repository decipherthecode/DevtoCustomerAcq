# How to Fill in This Document (Read This First)

**Folder:** `Testing and quality assurance/Load_and_Stress_Test_Plan.md`
**Template version:** 1.0 | **Covers:** AI-driven development → launch → first 500 customers
**Project types:** Web apps / SaaS and Mobile apps (with their backends)

## What is this document?

A **Load and Stress Test Plan** is a written agreement that answers four things:

1. **How many people** will use our product, and when?
2. **What does "fast enough" and "stable enough" mean** in numbers?
3. **How will we test it** before real customers get hurt?
4. **What do we do** when the test fails?

Think of it like testing a bridge. *Load test* = drive the number of cars we expect over it. *Stress test* = keep adding cars until it bends, so we know exactly where it breaks.

## The 7 rules for filling this out

1. **Fill every section in order.** Do not skip. If it does not apply, write `N/A – because <reason>`. Never leave a blank.
2. **Use numbers, not feelings.** Write "page loads in under 2 seconds for 95% of users", not "fast".
3. **Each question has an example.** Copy the *style*, not the words. Replace the example with your own answer.
4. **Do not guess.** If you do not know an answer, write `UNKNOWN – owner: <name> – date to find out: <date>`. Then use the Open Questions list (Section 18).
5. **Words in `<angle brackets>`** are placeholders. Replace them, including the brackets.
6. **Tick boxes** like this: `[x]` = yes, `[ ]` = no.
7. **When finished, run the Final Checklist (Section 19).** If anything fails, the plan is not ready.

## Word helper (plain-English dictionary)

| Word | Meaning in plain English |
|---|---|
| **Load test** | Test with the amount of traffic we *expect*. |
| **Stress test** | Test with *more than expected* until something breaks. |
| **Spike test** | A sudden jump in users (e.g., a viral post). |
| **Soak / endurance test** | Normal traffic for many hours to find slow leaks. |
| **Baseline** | The first measurement, used to compare all later tests. |
| **Virtual user (VU)** | A robot pretending to be one real person. |
| **Concurrent users** | People using the product at the exact same moment. |
| **RPS / TPS** | Requests (or transactions) per second. |
| **Latency / response time** | How long the user waits for an answer. |
| **p95 / p99** | The time that 95% / 99% of users are faster than. (p95 = 2s means 95 of 100 users wait 2 seconds or less.) |
| **Error rate** | Percent of requests that fail. |
| **Throughput** | How much work gets done per second. |
| **Breaking point** | The load at which the system stops working properly. |
| **Bottleneck** | The slowest part that limits everything else. |
| **SLO** | Service Level Objective: our own promise (e.g., 99.9% uptime). |
| **Exit criteria** | The checklist that must be green before moving to the next phase. |
| **Go / No-Go** | The decision to continue or to stop and fix. |

## Who can fill which section?

| Sections | Best filled by |
|---|---|
| 1–3 (Overview, Goals, Scope) | Product owner / founder |
| 4–6 (Users, Phases, Environment) | Product owner + Engineer |
| 7–10 (Scenarios, Data, Targets, Test Types) | QA + Engineer |
| 9A, 9B (Cost, Mobile) | Product owner + Engineer |
| 11–13 (Tools, Monitoring, AI Agents) | Engineer / DevOps |
| 12A (Security and Compliance) | Security / privacy contact + Engineer |
| 14–17 (Execution, Defects, Risks, Roles) | Project manager |
| 17A (After Launch) | DevOps + Project manager |
| 18–20 (Open Questions, Checklist, Approvals) | Everyone |

---

# Load and Stress Test Plan

## 0. Document Control

| Field | Your Answer |
|---|---|
| **Project name** | `<e.g., Acme Notes>` |
| **Plan ID** | `<e.g., LSTP-ACME-001>` |
| **Version** | `<e.g., 0.1 draft>` |
| **Author** | `<name>` |
| **Reviewer** | `<name>` |
| **Approver** | `<name>` |
| **Created on** | `<YYYY-MM-DD>` |
| **Last updated** | `<YYYY-MM-DD>` |
| **Status** | `[ ] Draft  [ ] In review  [ ] Approved  [ ] Retired` |
| **Link to product requirements (PRD)** | `<URL or "none">` |
| **Link to architecture diagram** | `<URL or "none">` |
| **Link to code repository** | `<URL>` |

### Change history

| Version | Date | Who | What changed |
|---|---|---|---|
| 0.1 | `<date>` | `<name>` | First draft |

---

## 1. Overview

**Q1.1 In one or two sentences, what does the product do, and for whom?**
*Example: "Acme Notes is a mobile and web app that lets students turn lecture audio into notes using AI."*
**Your answer:**

**Q1.2 Why are we writing this plan? (tick all that apply)**
- `[ ]` To make sure the product does not crash on launch day
- `[ ]` To find the maximum number of users the system can handle
- `[ ]` To prove we meet a promise made to customers (SLA)
- `[ ]` To control cloud costs under load
- `[ ]` Other: `<write here>`

**Q1.3 What is the single most important outcome of this plan?**
*Example: "Reach 500 paying customers with no outage longer than 5 minutes."*
**Your answer:**

**Q1.4 Product type (tick all that apply)**
- `[ ]` Web app / SaaS
- `[ ]` Mobile app (iOS)
- `[ ]` Mobile app (Android)
- `[ ]` Public API
- `[ ]` Uses AI/LLM features (chatbot, summaries, image generation, etc.)
- `[ ]` Takes payments
- `[ ]` Stores personal data

**Q1.5 What is the date of the planned public launch?**
*Example: 2026-12-01.* **Your answer:**

**Q1.6 What is the launch style?**
- `[ ]` Invite-only / waitlist
- `[ ]` Soft launch in one country
- `[ ]` Full public launch
- `[ ]` Launch with a marketing campaign or press (expect a spike)

---

## 2. Goals and Success Definition

**Q2.1 What does "success" mean for this test plan? Write 3–5 measurable goals.**
*Example:*
1. *Support 200 people using the app at the same time with page loads under 2 seconds (p95).*
2. *Error rate below 1% at the expected peak.*
3. *Know the breaking point within 30 minutes of a stress test.*

**Your goals:**
1.
2.
3.

**Q2.2 What does "failure" look like? (the things that must never happen)**
*Example: "Users lose data", "Payments charged twice", "App down for more than 10 minutes".*
**Your answer:**

**Q2.3 Who will be unhappy if the system is slow or down? (customers, boss, investors, partners)**
**Your answer:**

**Q2.4 What is the business cost of one hour of downtime?**
*Example: "About $200 of lost sales plus support time." If unknown, write UNKNOWN.*
**Your answer:**

---

## 3. Scope

### 3.1 In scope (what we WILL test)

**Q3.1 List every part of the product to be tested.**
Fill the table. Add rows as needed.

| # | Feature / API / Screen | Why it matters | Priority (High/Med/Low) |
|---|---|---|---|
| 1 | *Example: Sign-up and login* | *Every user does this* | *High* |
| 2 | *Example: Upload audio file* | *Heaviest feature* | *High* |
| 3 | *Example: AI summary generation* | *Slow and costly* | *High* |
| 4 | | | |

### 3.2 Out of scope (what we will NOT test)

**Q3.2 List what is excluded, and give a reason.**
*Example: "Third-party payment page – tested by the provider themselves."*

| # | Excluded item | Reason | Who accepts the risk? |
|---|---|---|---|
| 1 | | | |

### 3.3 Third-party services we depend on

**Q3.3 Which outside services does the product use?** (payments, email, login, AI model providers, maps, push notifications)

| Service | What we use it for | Can we load-test it? (Yes/No) | Their rate limit | How we fake it during tests (mock/sandbox) |
|---|---|---|---|---|
| *Example: AI model API* | *Summaries* | *No – costs money and has limits* | *60 requests/min* | *Mock that waits 3 sec then replies* |

> **Safety rule:** Never run stress tests against another company's live system without their written permission. Use a mock, sandbox, or test account.

---

## 4. Users and Traffic (How Many People?)

This is the most important section. Everything else depends on it.

**Q4.1 How many customers do we expect at each stage?**

| Stage | Registered users | Daily active users | Peak users at the same moment | How we got this number |
|---|---|---|---|---|
| Internal testing | *10* | *10* | *5* | *Team size* |
| Beta / early access | *50* | *30* | *15* | *Waitlist size* |
| Launch day | *200* | *100* | *40* | *Marketing estimate* |
| Customer #100 | | | | |
| Customer #250 | | | | |
| Customer #500 | | | | |

> **Beginner tip:** If you do not know peak users, use this rule of thumb: peak concurrent users ≈ 10% of daily active users. Write "estimated" in the last column.

**Q4.2 When is the busiest time of day/week?**
*Example: "Weekdays 6–9 pm local time, because students study after class."*
**Your answer:**

**Q4.3 What is the safety multiplier?** We always test above the expected peak.

| Test level | Multiplier | Calculated users |
|---|---|---|
| Expected peak (normal) | 1× | `<number>` |
| Safe headroom | 2× | `<number>` |
| Spike (sudden jump) | 3× | `<number>` |
| Stress (find the break) | 5× or until failure | `<number>` |

**Q4.4 Where are the users located? (so we test from the right places)**
*Example: "70% USA, 20% Europe, 10% India."*
**Your answer:**

**Q4.5 Device mix (mark percentages, total 100%)**

| Device | % of users |
|---|---|
| Desktop browser | |
| Mobile web | |
| iOS app | |
| Android app | |
| API / other | |

**Q4.6 Mobile only: what networks do users have?**
*Example: "40% on 4G/5G, 40% Wi-Fi, 20% slow 3G."* (Slow networks keep connections open longer and add load.)
**Your answer:**

**Q4.7 Could something cause a sudden surge?** (tick all)
- `[ ]` Press / blog post / social media mention
- `[ ]` Email blast to a list
- `[ ]` Product Hunt / app store feature
- `[ ]` Sale or promotion
- `[ ]` End of month / deadline (e.g., tax day)
- `[ ]` None expected

---

## 5. Lifecycle Phases and Exit Gates (Development → First 500 Customers)

The plan is split into phases. **You cannot enter the next phase until the gate is green.**

```
Phase 1        Phase 2         Phase 3          Phase 4        Phase 5
Development -> Integration  -> Pre-Launch    -> Launch Day -> Customers 1–500
(small tests)  (staging)       (full dress)     (watch live)   (grow safely)
```

### 5.1 Phase table

Fill the "Your answer" column for each row.

| Phase | Goal | Tests to run | Load level | Exit gate (must be true to continue) | Owner | Planned dates |
|---|---|---|---|---|---|---|
| **P1 – Development** | Catch slow code early | Unit-level performance checks, single-user timing, AI agent runs smoke load on every merge | 1–10 virtual users | *No endpoint slower than 1s with 1 user; no new slow queries* | `<name>` | `<dates>` |
| **P2 – Integration / Staging** | Test the whole system together | Baseline test, first load test, first stress test | 25–50% of expected peak | *Baseline recorded; errors < 2%; all top-priority scenarios tested* | `<name>` | `<dates>` |
| **P3 – Pre-launch** | Full rehearsal | Load at 1×, 2×, spike, 4–8 hour soak, stress to failure, failover test | 1× to 5× launch peak | *All targets in Section 9 met; no High/Critical open defects; rollback tested* | `<name>` | `<dates>` |
| **P4 – Launch day** | Watch the real thing | Live monitoring, small canary checks, no stress tests on production | Real traffic | *Error rate and speed inside targets for 24 hours* | `<name>` | `<dates>` |
| **P5 – Customers 1–500** | Grow without breaking | Re-test at each customer milestone (below) | Next milestone × 2 | *See milestone table* | `<name>` | `<dates>` |

### 5.2 Customer milestone gates (Phase 5)

Before reaching the next milestone, re-run the tests and check the gate.

| Milestone | Re-test required? | Test load (× expected peak) | Gate to pass | Date tested | Result (Pass/Fail) |
|---|---|---|---|---|---|
| Customer 10 | Smoke test | 1× | No errors on main scenarios | | |
| Customer 50 | Load test | 2× of 50-user peak | Targets in Section 9 | | |
| Customer 100 | Load + spike | 2× | Targets in Section 9 | | |
| Customer 250 | Load + stress + soak | 2× then until failure | Breaking point is at least 2× the next milestone | | |
| Customer 500 | Full suite | 2× of 500-user peak | Breaking point is at least 2× of 500-user peak | | |

**Q5.1 Who decides Go / No-Go at each gate?**
*Example: "Product owner decides, QA gives recommendation."* **Your answer:**

**Q5.2 What happens if a gate fails?**
*Example: "Pause new sign-ups (waitlist), fix, re-test, then reopen."* **Your answer:**

**Q5.3 Can we slow down sign-ups if the system struggles?** (waitlist, invite codes, rate limits)
- `[ ]` Yes, how: `<explain>`
- `[ ]` No

---

## 6. Test Environment

**Q6.1 Where will each phase's tests run?**

| Phase | Environment name | Same size as production? (Yes / No / % of size) | Who owns it | Cost per day |
|---|---|---|---|---|
| P1 | *Example: Local / dev* | *No – 5%* | | |
| P2 | *Example: Staging* | *No – 25%* | | |
| P3 | *Example: Pre-prod clone* | *Yes – 100%* | | |
| P4/P5 | Production | – | | |

> **Golden rule:** Test results only count for the size of the environment you tested. If staging is half the size of production, do not claim production can handle double. Write the scaling assumption below.

**Q6.2 If the test environment is smaller than production, how will we convert the results?**
*Example: "Staging has 2 servers, production has 8. We expect near-linear scaling, so results × 4, and we will verify with a short test in production at off-peak hours."*
**Your answer:**

**Q6.3 Describe the system under test (tick everything used and name it)**

| Part | Used? | Product / version | Size (CPU, memory, count) | Auto-scaling? (Y/N, limits) |
|---|---|---|---|---|
| Web servers / containers | `[ ]` | | | |
| Backend API | `[ ]` | | | |
| Database | `[ ]` | | | |
| Cache (e.g., Redis) | `[ ]` | | | |
| File / object storage | `[ ]` | | | |
| Message queue / background jobs | `[ ]` | | | |
| Search | `[ ]` | | | |
| CDN | `[ ]` | | | |
| Load balancer | `[ ]` | | | |
| AI / LLM provider or self-hosted model | `[ ]` | | | |
| Push notification service | `[ ]` | | | |

**Q6.4 Add or link an architecture picture.** `<URL or file name>`

**Q6.5 Which cloud / hosting do we use?** `<e.g., AWS, GCP, Azure, Vercel, own servers>`

**Q6.6 Cost cap: what is the most we can spend on running tests?**
*Example: "$300 for all of P3". Include the cost of AI API calls.* **Your answer:**

**Q6.7 Where do the "robot users" (load generators) run, and are they strong enough?**
*Example: "3 cloud machines, 4 CPU each, in us-east. Each can simulate about 1,000 users."*
**Your answer:**

**Q6.8 Is the test environment isolated, so tests will not touch real customers or real money?**
- `[ ]` Yes, completely separate
- `[ ]` Partly – explain: `<>`
- `[ ]` No – STOP, explain the risk: `<>`

---

## 7. User Scenarios (What Do the Robots Do?)

A scenario is a short story of what one real person does. Tests copy these stories thousands of times.

**Q7.1 List the top journeys, in order of importance. Aim for 5–10.**

| ID | Scenario name | Steps (short) | % of all traffic | Think time between steps | Priority |
|---|---|---|---|---|---|
| S1 | *Example: Browse and log in* | *Open app → log in → see home* | *40%* | *3–8 sec* | *High* |
| S2 | *Example: Create a note* | *Log in → upload audio → wait for result → open note* | *30%* | *5–15 sec* | *High* |
| S3 | *Example: Search notes* | *Log in → type search → open result* | *20%* | *2–6 sec* | *Medium* |
| S4 | *Example: Upgrade to paid* | *Open pricing → pay (test mode) → confirm* | *5%* | *10–30 sec* | *High* |
| S5 | | | | | |

> Percentages must add up to 100%.

**Q7.2 Which scenarios are the heaviest on the system? (big uploads, reports, AI calls, search)**
**Your answer:**

**Q7.3 Which scenarios are the most valuable to the business? (sign-up, payment)**
**Your answer:**

**Q7.4 Where do we get this information?** (tick all)
- `[ ]` Real analytics from a similar product
- `[ ]` Beta test data
- `[ ]` Product team's best guess (mark as ESTIMATE)
- `[ ]` Competitor research

### 7.1 Special scenarios (mark which apply)

- `[ ]` Many users sign up at once
- `[ ]` Many users log in at once (e.g., 9 am Monday)
- `[ ]` Large file uploads at the same time
- `[ ]` Long-running background jobs
- `[ ]` Real-time features (chat, live updates, WebSockets)
- `[ ]` Mobile app wakes up from push notification (everyone opens at once)
- `[ ]` Flash sale / limited item
- `[ ]` Same item edited by many users at once
- `[ ]` AI feature used by many users at once

---

## 8. Test Data

**Q8.1 What data do the robots need?** (accounts, files, products, messages)
*Example: "5,000 fake user accounts, 200 sample audio files from 1 to 30 minutes."*
**Your answer:**

**Q8.2 Where does the data come from?**
- `[ ]` Generated fake data
- `[ ]` Copy of production with personal data removed (anonymized)
- `[ ]` Real data (**NOT allowed** without written approval from the data owner)

**Q8.3 How big should the database be when we test?**
*Example: "Match what we expect after 12 months: 500 users × 200 notes = 100,000 notes."*
**Your answer:**

**Q8.4 How do we reset data between test runs?** `<e.g., restore database snapshot>`

**Q8.5 Do tests send real emails, texts, or payments?**
- `[ ]` No – we use mocks or sandboxes (**required**)
- `[ ]` Yes – STOP: needs written approval from `<name>`

**Q8.6 Privacy check:** Does any test data contain real personal information?
- `[ ]` No   - `[ ]` Yes → who approved, and where is it protected? `<>`

---

## 9. Performance Targets (The Pass / Fail Numbers)

**Q9.1 Fill in the target for each measurement.** These are the rules that decide pass or fail. Change the example numbers to match your product.

| Measurement | What it means | Target (PASS if...) | Warning (investigate if...) | Fail (STOP if...) |
|---|---|---|---|---|
| **Page / screen load, p95** | 95% of users wait this long or less | *≤ 2 sec* | *2–3 sec* | *> 3 sec* |
| **API response, p95** | Server answer time | *≤ 500 ms* | *500 ms–1 sec* | *> 1 sec* |
| **API response, p99** | Slowest 1% | *≤ 1.5 sec* | *1.5–3 sec* | *> 3 sec* |
| **Error rate** | % of failed requests | *< 1%* | *1–2%* | *> 2%* |
| **Throughput** | Requests per second handled | *≥ `<number>`* | | |
| **CPU use** | % of server brain used | *< 70%* | *70–85%* | *> 85% for 5 min* |
| **Memory use** | % of server memory used | *< 75% and flat* | *75–85%* | *> 85% or keeps climbing* |
| **Database** | Slow queries, connections used | *No query > 1 sec; < 70% connections* | | *Connections exhausted* |
| **Uptime during test** | System stays up | *100%* | | *Any crash* |
| **Recovery time** | Time to return to normal after overload ends | *≤ 5 min* | *5–15 min* | *> 15 min or needs manual fix* |
| **Cost per 1,000 users** | Cloud + AI cost | *≤ `<amount>`* | | |

**Q9.2 Mobile app targets (only if mobile)**

| Measurement | Target |
|---|---|
| App cold start (opening from closed) | *≤ 3 sec* |
| Screen to screen response | *≤ 1 sec* |
| Works on slow network (3G) | *Core flow completes in ≤ 10 sec* |
| Battery / data use during load | *`<limit>`* |
| App does not crash when server is slow | *0 crashes* |

**Q9.3 AI / LLM targets (only if the product uses AI)**

| Measurement | Target |
|---|---|
| Time to first word of AI answer | *≤ 2 sec* |
| Full AI answer time, p95 | *≤ 15 sec* |
| AI provider rate-limit errors | *< 0.5%* |
| Cost per AI request | *≤ `<amount>`* |
| What users see when AI is busy | *Friendly "try again" message, queue, or fallback* |

**Q9.4 Where do these numbers come from?** (tick all)
- `[ ]` Promise to customers (SLA)
- `[ ]` Industry standard
- `[ ]` Our own decision
- `[ ]` Copied from a competitor
- `[ ]` Estimate (needs review on `<date>`)

**Q9.5 Uptime promise:** `[ ] 99%  [ ] 99.5%  [ ] 99.9%  [ ] Other: ___` (99.9% allows about 43 minutes of downtime per month.)

---

## 9A. Cost and AI-Token Budget

Load makes money leave your account. Know the cost *before* you test and *before* you grow.

**Q9A.1 What does one active user cost per month at normal use?**

| Cost item | How it is charged | Cost per user per month | Source of number |
|---|---|---|---|
| Servers / containers | *per hour / per instance* | | |
| Database & storage | *per GB / per request* | | |
| Bandwidth / CDN | *per GB* | | |
| AI model calls | *per 1,000 input + output tokens* | | |
| Third-party services (email, SMS, maps) | *per message* | | |
| Monitoring tools | *per host / per GB logs* | | |
| **Total** | | **`$___`** | |

**Q9A.2 AI-token model (only if the product uses AI)**

| Question | Your answer |
|---|---|
| Which AI model(s) do we call? | |
| Average input size per request (tokens) | *Example: 1,500* |
| Average output size per request (tokens) | *Example: 500* |
| Requests per user per day | *Example: 5* |
| Price per 1,000 input / output tokens | |
| Daily cost at 500 customers (= requests × tokens × price) | |
| Provider rate limit (requests/min, tokens/min) | |
| What happens when we hit the limit? (queue, retry, message) | |
| Do we cache repeated answers to save money? | |

**Q9A.3 Spend alerts and caps**

| Alert | Limit | Who is notified | Automatic action |
|---|---|---|---|
| Test spend warning | `$___` | | |
| Test spend hard stop | `$___` | | *Shut down load generators* |
| Production daily warning | `$___` | | |
| Production daily hard cap | `$___` | | *Slow down heavy features* |

**Q9A.4 Break-even check:** Revenue per customer `$___` − cost per customer `$___` = `$___`. Is it positive at 500 customers? `[ ] Yes  [ ] No  [ ] UNKNOWN (add to Section 18)`

---

## 9B. Mobile App Specifics (Skip with "N/A" if there is no mobile app)

**Q9B.1 Which platforms and versions must work?**

| Platform | Oldest version supported | Share of users | Test devices |
|---|---|---|---|
| iOS | | | |
| Android | | | |

**Q9B.2 Device range:** Do we test on low-end phones (slow CPU, little memory)? `[ ] Yes  [ ] No → reason: ___`

**Q9B.3 Mobile risks to plan for (tick all that apply)**
- `[ ]` Push notification sent to everyone at once → everyone opens the app together (spike)
- `[ ]` Old app versions still calling old APIs after an update
- `[ ]` App retries too fast when the server is slow (retry storms)
- `[ ]` Weak or switching networks (Wi-Fi ↔ 4G) cause repeated requests
- `[ ]` Background sync or uploads at the same time
- `[ ]` App store review delays when we need an urgent fix (**how long? ___ days**)
- `[ ]` Offline mode syncing many changes at once on reconnect

**Q9B.4 Does the app back off politely when the server is overloaded?** (wait longer between retries)
`[ ] Yes  [ ] No  [ ] UNKNOWN`

**Q9B.5 Can we turn features off remotely without an app update?** (feature flags) `[ ] Yes  [ ] No`

**Q9B.6 What does the user see when the server is down?** *(friendly message, cached data)*
**Your answer:**

---

## 10. Test Types

**Q10.1 For each test type, decide Yes / No, and fill in the details.**

| Test type | What it answers | Use it? | Load | How long | Phase | Pass rule |
|---|---|---|---|---|---|---|
| **Smoke** | "Does the test even work?" | `[ ]` | 1–5 users | 2–5 min | P1–P5 | No errors |
| **Baseline** | "What is normal speed with a few users?" | `[ ]` | 1–10 users | 10 min | P2 | Numbers recorded |
| **Load** | "Can we handle expected traffic?" | `[ ]` | 1× peak | 30–60 min | P2–P5 | Section 9 targets |
| **Stress** | "Where does it break?" | `[ ]` | Ramp to 5× or failure | Until failure | P2–P3, P5 | Breaking point ≥ 2× peak, fails gracefully |
| **Spike** | "Can it survive a sudden jump?" | `[ ]` | 0 → 3× in under 1 min | 10–20 min | P3 | Recovers in ≤ 5 min |
| **Soak / endurance** | "Does it leak or slow down over time?" | `[ ]` | 1× peak | 4–8 hours (24 for key releases) | P3 | Memory flat, speed stable |
| **Scalability** | "Do extra servers actually help?" | `[ ]` | Step up 25%, 50%, 100% | 1–2 hours | P3 | Near-linear gain |
| **Breakpoint / capacity** | "What is our exact maximum?" | `[ ]` | Slow steady increase | Until limit | P3, P5 | Limit documented |
| **Failover / recovery** | "What if a server dies mid-test?" | `[ ]` | 1× | 30 min | P3 | Automatic recovery |
| **Rate-limit / abuse** | "What if someone hammers us?" | `[ ]` | Many requests from one user | 10 min | P3 | Blocked politely, others unaffected |
| **Regression** | "Did the new version get slower?" | `[ ]` | 1× | 30 min | Every release | No worse than baseline by > 10% |

**Q10.2 For the stress test, what do we want to learn?** (tick all)
- `[ ]` The exact number of users when speed becomes unacceptable
- `[ ]` What fails first (database, servers, AI provider, memory)
- `[ ]` Whether it fails gracefully (friendly error) or badly (crash, data loss)
- `[ ]` How fast it recovers when load drops
- `[ ]` Whether auto-scaling kicks in fast enough
- `[ ]` Whether the cost explodes

**Q10.3 Load shape: how will traffic grow?** Draw or describe for each test.
*Example (load test): "Ramp from 0 to 200 users over 10 min, hold 30 min, ramp down over 5 min."*

| Test | Ramp up | Hold | Ramp down |
|---|---|---|---|
| Load | | | |
| Stress | | | |
| Spike | | | |
| Soak | | | |

**Q10.4 Stop rules: when do we STOP a test early to avoid damage?**
*Example: "Stop if error rate > 20% for 2 min, or if real customers are affected, or cloud spend exceeds the cap."*
**Your answer:**

---

## 11. Tools

**Q11.1 Which tools will we use? Tick one in each row, or write your own.**

| Job | Options | Our choice |
|---|---|---|
| Create load (robots) | `[ ]` k6  `[ ]` JMeter  `[ ]` Locust  `[ ]` Gatling  `[ ]` Artillery  `[ ]` Cloud service  `[ ]` Other | |
| Mobile app load | `[ ]` Test the backend API directly  `[ ]` Device farm  `[ ]` Other | |
| Browser-level checks | `[ ]` Lighthouse  `[ ]` Playwright  `[ ]` WebPageTest  `[ ]` None | |
| Watch servers | `[ ]` Grafana/Prometheus  `[ ]` Datadog  `[ ]` New Relic  `[ ]` Cloud-native monitor  `[ ]` Other | |
| Watch errors | `[ ]` Sentry  `[ ]` Logs  `[ ]` Other | |
| Watch database | `[ ]` Built-in slow query log  `[ ]` APM tool  `[ ]` Other | |
| Reports | `[ ]` Tool built-in  `[ ]` Spreadsheet  `[ ]` Dashboard | |
| Run in pipeline | `[ ]` GitHub Actions  `[ ]` GitLab CI  `[ ]` Jenkins  `[ ]` Other  `[ ]` Not yet | |
| Defect tracking | `[ ]` Jira  `[ ]` GitHub Issues  `[ ]` Linear  `[ ]` Other | |

**Q11.2 Why did we choose them?** *(cost, skills we have, protocols supported)*
**Your answer:**

**Q11.3 Does anyone need training on these tools?** `[ ] No  [ ] Yes → who / what / by when: ___`

**Q11.4 Where will the test scripts live?** `<repository path>` (scripts must be in version control)

---

## 12. Monitoring: What We Watch During Tests

**Q12.1 Check every item that will be recorded during each test.**

**Users' view (what the customer feels)**
- `[ ]` Response time (average, p95, p99)
- `[ ]` Error rate and error types
- `[ ]` Number of active virtual users
- `[ ]` Requests per second

**Servers' view**
- `[ ]` CPU
- `[ ]` Memory
- `[ ]` Disk and network
- `[ ]` Number of running servers/containers
- `[ ]` Auto-scaling events

**Database / storage**
- `[ ]` Slow queries
- `[ ]` Connections in use
- `[ ]` Locks or waiting queries
- `[ ]` Storage growth

**Background work and AI**
- `[ ]` Queue length and waiting time
- `[ ]` AI provider response time, rate-limit errors
- `[ ]` AI cost during the test

**Money**
- `[ ]` Cloud cost per hour

**Q12.2 Who watches the dashboards during a test?** `<name + backup>`

**Q12.3 Where do we save raw results?** `<folder / URL>` (Keep for at least `<e.g., 12 months>`.)

---

## 12A. Security, Privacy and Compliance During Testing

**Q12A.1 Which rules apply to this product? (tick all)**
- `[ ]` GDPR / UK GDPR (EU/UK personal data)
- `[ ]` CCPA / CPRA (California)
- `[ ]` HIPAA (health data, USA)
- `[ ]` PCI DSS (card payments)
- `[ ]` SOC 2 / ISO 27001 (customer security audits)
- `[ ]` Children's data (COPPA, etc.)
- `[ ]` Other: `<>`
- `[ ]` None known (confirm with `<name>`)

**Q12A.2 Test-data rules**

| Rule | Agreed? |
|---|---|
| Test data is fake or fully anonymized | `[ ]` |
| No real card numbers (use the payment provider's test cards) | `[ ]` |
| Test data never leaves the approved region | `[ ]` |
| Test data is deleted after testing within `___` days | `[ ]` |
| Results and logs contain no personal data | `[ ]` |

**Q12A.3 Do we need written permission before testing?**

| System | Owner | Permission needed? | Obtained on | Reference |
|---|---|---|---|---|
| Our cloud provider (some require notice for large tests) | | | | |
| AI model provider | | | | |
| Payment, email, SMS providers | | | | |

**Q12A.4 Security-under-load tests (tick those to run, in staging only)**

| Test | Run? | Pass rule |
|---|---|---|
| Login attempts flood (password guessing) | `[ ]` | Blocked or slowed after `___` tries |
| One user sends thousands of requests (rate limiting) | `[ ]` | Others stay fast; user gets polite error |
| Many sign-ups from one place (fake accounts) | `[ ]` | Throttled, CAPTCHA, or email checks |
| Large or odd uploads | `[ ]` | Rejected safely; no crash |
| Basic DDoS protection check (WAF / CDN rules, **only with provider approval**) | `[ ]` | Bad traffic blocked, good users served |
| System under load still enforces permissions (users cannot see others' data) | `[ ]` | 0 data leaks |
| Errors under load do not reveal secrets | `[ ]` | No stack traces or keys shown |

**Q12A.5 Evidence for auditors:** Where do we keep signed test reports, approvals and permissions? `<location>` Keep for `___` years.

> **Rule:** Never launch a real attack on any system. Security-under-load tests run only in our own staging environment with written approval.

---

## 13. AI-Agent Instructions (For AI Helpers Running This Plan)

> This section is for AI agents (coding agents, test agents, report agents). Humans fill in the blanks. Agents must follow the rules exactly.

### 13.1 Machine-readable summary (keep in sync with the rest of the plan)

```yaml
plan_id: "<LSTP-XXX-001>"
project: "<name>"
version: "<0.1>"
launch_date: "<YYYY-MM-DD>"
customer_target: 500
phase_now: "<P1|P2|P3|P4|P5>"
environments:
  allowed_for_stress: ["<staging>", "<pre-prod>"]
  forbidden_for_stress: ["production"]
targets:
  page_load_p95_ms: 2000
  api_p95_ms: 500
  api_p99_ms: 1500
  error_rate_percent_max: 1
  cpu_percent_max: 70
  memory_percent_max: 75
  recovery_minutes_max: 5
load_levels:
  expected_peak_users: "<number>"
  spike_multiplier: 3
  stress_multiplier: 5
stop_rules:
  error_rate_percent_over: 20
  max_cloud_spend_usd: "<number>"
scripts_path: "<repo/path>"
results_path: "<folder/URL>"
owners:
  plan_owner: "<name>"
  go_no_go: "<name>"
```

### 13.2 Rules every AI agent must follow

1. **Never** run stress, spike, or soak tests against production or against anyone's live system unless a human wrote "APPROVED" with a date in Section 20.
2. **Always** read Sections 3, 6, 8, 9 and 10 before running anything.
3. **Never** use real customer data, real payment methods, or send real emails/messages.
4. **Stop immediately** when any stop rule in Section 10 (Q10.4) is hit, and tell a human.
5. **Do not change** targets, scope, or pass/fail rules. Propose changes in Section 18 (Open Questions) for a human to approve.
6. **Do not guess** missing numbers. Write `UNKNOWN`, and ask a human.
7. **Record everything**: tool version, script version (commit ID), environment size, start/end time, and raw results.
8. **Report honestly**, including failures and tests that were skipped.
9. **Respect cost limits.** Check spend at least every `<15>` minutes.
10. **Never delete** results or logs.

### 13.3 What each agent role does (tick the ones you use)

| Role | Used? | Job | Allowed to do | Not allowed to do | Human who approves |
|---|---|---|---|---|---|
| Script-writing agent | `[ ]` | Turn Section 7 scenarios into test scripts | Write scripts in the repo, open a pull request | Merge without review | `<name>` |
| Test-runner agent | `[ ]` | Run tests listed in Section 10 | Run in approved environments | Run on production, change targets | `<name>` |
| Monitoring agent | `[ ]` | Watch dashboards, trigger stop rules | Stop a test, send alerts | Change system settings | `<name>` |
| Analysis agent | `[ ]` | Compare results with Section 9 targets, find bottlenecks | Read results, suggest fixes | Apply fixes to production | `<name>` |
| Report agent | `[ ]` | Write the report in Section 14.5 format | Draft and publish to the results folder | Mark a gate as passed without human sign-off | `<name>` |
| Defect agent | `[ ]` | Open tickets for failures | Create tickets with evidence | Close tickets | `<name>` |

### 13.4 AI-agent inputs and outputs

| Step | Input the agent needs | Output the agent must produce |
|---|---|---|
| 1. Prepare | This plan, repo, environment access | Checklist showing environment ready, data loaded |
| 2. Script | Section 7 scenarios | Test scripts + short README |
| 3. Dry run | Scripts | Smoke test result (pass/fail) |
| 4. Run | Approved test list | Raw results + timestamps |
| 5. Analyze | Raw results + Section 9 targets | Pass/Warn/Fail table + top 3 bottlenecks |
| 6. Report | Analysis | Report in Section 14.5 format |
| 7. Escalate | Any failure | Defect ticket + message to human owner |

**Q13.1 Which AI tools / agents will we use?** `<names, versions>`
**Q13.2 What are agents never allowed to touch in this project?** `<e.g., production database, billing>`
**Q13.3 How do humans review agent work?** `<e.g., all pull requests need 1 human approval>`

---

## 14. Test Execution Process

### 14.1 Before each test (checklist)

- `[ ]` Test environment is up and matches Section 6
- `[ ]` Test data loaded and checked (Section 8)
- `[ ]` Monitoring is running and showing data (Section 12)
- `[ ]` Alerts will not wake up the wrong people (or the team is warned)
- `[ ]` Third-party services are mocked or in sandbox mode
- `[ ]` Nobody else is using the test environment
- `[ ]` Stop rules and the emergency contact are known
- `[ ]` A baseline exists to compare against
- `[ ]` Cloud spend cap is set
- `[ ]` The team is told the start time

### 14.2 During each test

1. Run the smoke test first.
2. Start monitoring, then start the load.
3. Follow the ramp shape in Q10.3.
4. Note events with the time (e.g., "10:42 error rate jumped").
5. Apply stop rules immediately if triggered.

### 14.3 After each test

- `[ ]` Stop the robots; confirm the system returns to normal
- `[ ]` Save raw results and screenshots
- `[ ]` Compare results with Section 9
- `[ ]` Note the top 3 problems
- `[ ]` Open defects (Section 15)
- `[ ]` Write the report (14.5)
- `[ ]` Clean up test data and shut down expensive resources

### 14.4 Schedule

| Test | Phase | Planned date | Duration | Environment | Owner | Status |
|---|---|---|---|---|---|---|
| | | | | | | `[ ] Planned [ ] Done [ ] Skipped` |

### 14.5 Test report format (use for every test)

```
Test name:                 Date/time:           Version tested (commit):
Environment & size:        Test type:           Load level:
Duration:                  Tool/version:        Run by (human/agent):

RESULT:   PASS / WARN / FAIL
Summary (3 sentences max):

| Measurement | Target | Actual | Pass? |
|-------------|--------|--------|-------|

Breaking point found (stress): ______ users / ______ requests per second
What failed first:             ____________________
Top 3 bottlenecks:             1.  2.  3.
Cost of this test:             $______
Defects opened:                #____, #____
Recommendation:                Go / No-Go / Re-test after fix
Raw data location:             ____________________
```

### 14.6 Communication

**Q14.1 Who gets reports, and how often?**

| Who | What they receive | How often | Channel |
|---|---|---|---|
| Product owner | One-page summary | After every gate | `<email/chat>` |
| Engineers | Full report + bottlenecks | After every test | `<>` |
| Executives / investors | Pass/Fail status | Weekly | `<>` |

**Q14.2 Emergency contact if a test goes wrong:** `<name, phone, backup>`

---

## 15. Defects and Re-testing

**Q15.1 How serious is a problem? Fill in or accept the example scale.**

| Level | Meaning | Example | Must fix before... |
|---|---|---|---|
| **Critical** | Data loss, crash, payments wrong | Database stops at 80 users | Next phase |
| **High** | Target missed by a lot | p95 is 6 sec, target 2 sec | Launch |
| **Medium** | Target missed slightly | p95 is 2.4 sec | Customer 100 |
| **Low** | Cosmetic, minor | Dashboard label wrong | When convenient |

**Q15.2 Where do defects go?** `<tool + project>`

**Q15.3 What must a defect ticket include?**
Test name · version · load level · screenshot or graph · time of failure · steps to repeat · suspected cause · owner.

**Q15.4 Re-test rule:** after every fix, re-run the *same* test at the *same* load and compare with the failed run.
- `[ ]` Agreed    **Exceptions:** `<>`

**Q15.5 Known issues we choose to accept (with reason, owner, and expiry date):**

| Issue | Why accepted | Accepted by | Revisit by |
|---|---|---|---|

---

## 16. Risks and Plan B

**Q16.1 What could go wrong, and what will we do?**

| # | Risk | How likely (L/M/H) | How bad (L/M/H) | What we do about it | Owner |
|---|---|---|---|---|---|
| 1 | *Test environment too small to be realistic* | M | H | *Run a short check in production off-peak* | |
| 2 | *AI provider limits or blocks our test traffic* | M | M | *Use mock provider, ask provider for limits* | |
| 3 | *Cloud bill jumps from tests* | M | M | *Spend cap + automatic shutdown* | |
| 4 | *Real users harmed by testing* | L | H | *Never stress production; isolate environments* | |
| 5 | *Launch spike larger than expected* | M | H | *Waitlist, auto-scale, queue, rate limits* | |
| 6 | *Key person unavailable* | M | M | *Backup named in Section 17* | |
| 7 | | | | | |

**Q16.2 Launch-day Plan B (rollback and emergency steps)**

| Question | Answer |
|---|---|
| Can we roll back to the previous version? How fast? | |
| Can we pause sign-ups or turn off heavy features? How? | |
| Who can flip the switch? | |
| What do customers see during an outage? (status page, message) | |
| Where is the status page? | |

**Q16.3 Assumptions (things we believe are true but have not verified):**
1.
2.

**Q16.4 Dependencies (things we need from others, and by when):**

| Need | From whom | Needed by | Status |
|---|---|---|---|

---

## 17. Team and Responsibilities

**Q17.1 Who does what?** (one person can have several jobs, but every job needs a name and a backup)

| Role | Name | Backup | Responsibility |
|---|---|---|---|
| Plan owner | | | Keeps this document up to date |
| Product owner | | | Provides user numbers, decides Go/No-Go |
| QA / performance lead | | | Designs and reviews tests |
| Engineer(s) | | | Fixes bottlenecks |
| DevOps / platform | | | Environments, scaling, monitoring |
| Project manager | | | Schedule, communication |
| Security / privacy contact | | | Approves test data use |
| AI-agent supervisor | | | Reviews agent work (Section 13) |

**Q17.2 Training needs and budget**

| Item | Who | Cost | Date |
|---|---|---|---|

**Q17.3 Total test budget:** tools `$___` + cloud `$___` + AI calls `$___` + people `___ hours` = **`$___`**

---

## 17A. After Launch: Keeping It Healthy (Customers 1–500 and Beyond)

**Q17A.1 What do we watch in production every day?**

| Signal | Alert when | Who gets alerted | Response time goal |
|---|---|---|---|
| Error rate | `> ___%` for `___` min | | |
| p95 response time | `> ___` sec | | |
| CPU / memory | `> ___%` | | |
| Queue backlog | `> ___` items | | |
| AI provider errors | `> ___%` | | |
| Daily cloud / AI cost | `> $___` | | |
| Crash rate (mobile) | `> ___%` | | |

**Q17A.2 On-call plan**

| Question | Answer |
|---|---|
| Who is on call, and when? | |
| How are they reached? | |
| What do they do first? (link to runbook) | |
| When do they escalate, and to whom? | |

**Q17A.3 When do we re-run load tests after launch?** (tick all)
- `[ ]` At every customer milestone (Section 5.2)
- `[ ]` Before every major release
- `[ ]` Before every marketing campaign or expected spike
- `[ ]` After any change to servers, database, or AI model/provider
- `[ ]` Every `___` months, even if nothing changed

**Q17A.4 Compare real traffic with the plan every `___` weeks.**

| Measure | Planned (Section 4) | Actual | Gap | Action |
|---|---|---|---|---|
| Peak concurrent users | | | | |
| Busiest scenario | | | | |
| Cost per user | | | | |

If actual is above 70% of the tested safe level, schedule new tests *before* the next growth step.

**Q17A.5 After any incident, do we write a short review (what happened, why, fix, test added)?** `[ ] Yes  [ ] No`

**Q17A.6 Where is the incident runbook?** `<URL>`

---

## 18. Open Questions (Nothing Gets Guessed)

Write down everything unknown here. Review at the start of each phase.

| # | Question | Why it matters | Owner | Answer needed by | Answer | Status (Open/Closed) |
|---|---|---|---|---|---|---|
| 1 | | | | | | |

---

## 19. Final Checklist (Is This Plan Ready?)

Tick every box. If one is unticked, the plan is **not** approved.

**Completeness**
- `[ ]` Every section is filled in or marked `N/A – reason`
- `[ ]` No placeholder `<angle brackets>` remain
- `[ ]` Every `UNKNOWN` has an owner and a date in Section 18

**Clarity**
- `[ ]` Another person (or a 10-year-old) could read Section 4 and say how many users we expect
- `[ ]` Every target in Section 9 is a number, not a feeling
- `[ ]` Every phase in Section 5 has an exit gate

**Safety**
- `[ ]` No stress test is planned against production or third-party live systems without written approval
- `[ ]` No real personal data, real payments, or real emails in tests
- `[ ]` Stop rules and the emergency contact are written down
- `[ ]` Rollback plan is written and has been tried at least once

**Coverage**
- `[ ]` All top-priority scenarios in Section 7 are tested
- `[ ]` All customer milestones up to 500 have a test and a gate
- `[ ]` Web and mobile (if applicable) targets are filled in
- `[ ]` AI-feature targets are filled in (if applicable)

**Cost, security and operations**
- `[ ]` Cost per user and AI-token budget are filled in (Section 9A) and positive at 500 customers
- `[ ]` Spend caps are set for tests and production
- `[ ]` Compliance rules identified and test-data rules agreed (Section 12A)
- `[ ]` Mobile specifics filled in or marked N/A (Section 9B)
- `[ ]` Post-launch monitoring, on-call and re-test schedule are written (Section 17A)

**People**
- `[ ]` Every role has a name and a backup
- `[ ]` Budget approved
- `[ ]` The AI-agent rules (Section 13) were read by everyone running agents

---

## 20. Approvals

| Role | Name | Decision | Signature / typed name | Date |
|---|---|---|---|---|
| Plan owner | | `[ ] Approve  [ ] Changes needed` | | |
| Product owner | | `[ ] Approve  [ ] Changes needed` | | |
| QA lead | | `[ ] Approve  [ ] Changes needed` | | |
| Engineering lead | | `[ ] Approve  [ ] Changes needed` | | |
| Security / privacy (if real or sensitive data is involved) | | `[ ] Approve  [ ] Changes needed` | | |

**Special approval for production testing** (only fill in if truly needed):
APPROVED by `<name>` on `<date>` for `<exact test, load level, time window>`.

---

## Appendix A: Result Log (Fill in as you test)

| Date | Test | Phase | Load | Result | Report link | Defects |
|---|---|---|---|---|---|---|

## Appendix B: Environment Snapshot (Copy for each test)

```
Date:                 Commit/build:
Servers (count/size): Database (type/size):
Cache:                Queue:
AI provider/model:    Auto-scaling settings:
Feature flags on:     Region(s):
```

## Appendix C: Quick Sizing Cheat Sheet

| If you know... | Use this rough rule |
|---|---|
| Daily active users (DAU) | Peak concurrent users ≈ 10% of DAU |
| Concurrent users + think time | Requests/sec ≈ concurrent users ÷ (think time in seconds + average response time) |
| Expected peak | Test at 2× for safety, 3× for spike, 5× for stress |
| Soak test length | At least 4 hours; 8–24 hours for major releases |
| Mark all rules of thumb | As ESTIMATE, then replace with real data after launch |

## Appendix D: Glossary of Reference Standards (for further reading)

- ISO/IEC/IEEE 29119-3: test documentation
- IEEE 829: classic test plan structure
- ISTQB Performance Testing syllabus: terms and test types
- Google SRE book: SLOs and error budgets
