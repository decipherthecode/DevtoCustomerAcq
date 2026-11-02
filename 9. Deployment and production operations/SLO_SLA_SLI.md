# How to fill in this document (READ THIS FIRST)

**What this file is:** One file that records, for one product, *how reliable it must be* (SLO), *how we measure that* (SLI), and *what we promise customers* (SLA) — from the first line of code until the first **500 customers** are happily using it.

**Who can fill it in:** Anyone. You do not need to be an engineer. If you can read a question and type an answer, you can do this.

**How long it takes:** About 90–120 minutes for a new product. Update it at every phase change (see Section 3).

**Template version:** v1.1. Sections numbered with a letter (9B, 11A, 11B, 11C) were added after v1.0 so older section references still work.

## The 8 rules

1. **Go top to bottom.** Answer every question in order. Do not skip.
2. **Replace every `[FILL]`** with your answer. At the end, search this file for the text `[FILL`. If you find any, you are not done.
3. **Never leave a blank.** If something does not apply, write `N/A — because <reason>`. If you do not know, write `UNKNOWN — <who will find out> — <date>` and add it to Section 15.
4. **Do not guess silently.** If you are guessing, write `ASSUMED:` before the answer so reviewers can challenge it.
5. **Examples are not answers.** Text marked *Example* shows the style. Do not copy it unless it is truly correct for your product.
6. **Use numbers, not feelings.** "Fast" is not an answer. "95% of pages load in under 2 seconds" is an answer.
7. **Keep the question text.** Only change the answer lines. This keeps 100s of projects comparable.
8. **Ask for help early.** Stuck for more than 10 minutes? Write `UNKNOWN` and move on.

## Symbols used in this file

| Symbol | Meaning |
|---|---|
| `[FILL]` | You must replace this with your answer |
| `[PICK]` | Choose one option and delete the others |
| `[x]` / `[ ]` | Tick a box by changing `[ ]` to `[x]` |
| *Example:* | Sample answer, not for copying |
| 💡 | Hint that explains why we ask |
| ⚠️ | Common mistake |

## If you are an AI agent filling this in

- Never invent a number. If the user or the data has not given it, write `UNKNOWN` and ask a human.
- Mark every inferred value `ASSUMED:` and name the evidence you used.
- Use only the user's own data, repo, dashboards, and contracts as sources of truth.
- Do not change a question, a heading, or the order of sections.
- After finishing, complete Section 17 (Final checklist) and Section 18 (machine-readable summary).
- Stop and ask a human before filling Section 9 (SLA) and Section 16 (Sign-off). These have legal and business effects.

---

# 0. Mini glossary (kid-friendly)

Imagine a **pizza shop**.

| Word | Plain meaning | Pizza version | Software version |
|---|---|---|---|
| **SLI** (Service Level Indicator) | A number we *measure* | "How many minutes did this pizza take?" | "What % of requests worked?" |
| **SLO** (Service Level Objective) | Our *own goal* for that number | "95% of pizzas arrive in under 30 minutes." | "99.5% of requests work, every 30 days." |
| **SLA** (Service Level Agreement) | A *promise to customers* with a penalty if broken | "Late pizza = free pizza." | "Below 99% uptime = 10% credit." |
| **Error budget** | How many bad events we can afford before breaking the goal | "We can be late 5 times out of 100." | "0.5% of requests may fail." |
| **Burn rate** | How fast we are using up the error budget | "We were late 5 times in 1 hour!" | "We spent the monthly budget in 2 days." |
| **Window** | The time period we measure over | "Last 30 days" | "Rolling 30 days" |
| **Percentile (p95, p99)** | "95 out of 100 were at least this good" | "95 pizzas out of 100 took 30 min or less" | "p95 latency = 800 ms" |
| **Critical user journey** | A path the customer *must* be able to finish | "Order → Pay → Receive" | "Sign up → Log in → Pay" |
| **RPO / RTO** | How much data we can lose / how long to recover | "Lost orders from the last 5 min / back open in 30 min" | "Backup every 15 min / restore in 1 hr" |
| **MTTD / MTTR** | How long to *notice* a problem / how long to *fix* it | "Minutes until we saw the oven was broken / minutes until it worked again" | "Alert fired 4 min after failure / fixed in 35 min" |
| **Load test** | Practice run with fake crowds | "Pretend 100 hungry people arrive at once" | "Send 5× the expected traffic to staging" |
| **Vulnerability SLA** | How fast we fix a security hole | "Fix a broken lock within 2 days" | "Patch critical security bugs within 48 hours" |
| **Cost guardrail** | A spending limit per customer | "Ingredients must cost less than the pizza price" | "AI spend per customer stays under the monthly cap" |

**The golden rules that connect them:**

- **SLI** is what we measure → **SLO** is the goal for it → **SLA** is the promise built on top of it.
- **Error budget = 100% − SLO.** (A 99.9% SLO leaves a 0.1% error budget.)
- **The SLA must be easier than the SLO.** Example: internal goal 99.9%, public promise 99.5%. The gap is your safety margin.
- **An SLO with no written action when it is missed is only decoration.** That is why Section 7 exists.

---

# 1. Document control

| Field | Your answer |
|---|---|
| Product name | `[FILL]` |
| Product ID / repo name | `[FILL]` |
| Template version used | `v1.1` |
| This document's version | `[FILL]` *Example: 0.1 draft* |
| Document status `[PICK]` | Draft / In review / Approved / Needs update |
| Product owner (a named person) | `[FILL]` |
| Reliability owner (person who wakes up when it breaks) | `[FILL]` |
| Filled in by | `[FILL]` |
| Date filled in | `[FILL]` *Format: YYYY-MM-DD* |
| Next scheduled review date | `[FILL]` |
| Link to related runbook / incident process / monitoring dashboard | `[FILL]` |

💡 A document with no owner is the same as a document nobody reads.

---

# 2. Product snapshot (so nobody has to guess)

**Q2.1 — In one sentence, what does your product do, and for whom?**
*Example: "A web app that helps small shops send invoices, used by shop owners."*
Your answer: `[FILL]`

**Q2.2 — What type of product is it?** (tick all that apply)

- [ ] Web app / SaaS
- [ ] API or backend service (other software calls it)
- [ ] Mobile app (iOS / Android)
- [ ] AI / LLM-powered feature
- [ ] AI agent that performs multi-step tasks
- [ ] Other: `[FILL]`

💡 Your ticks decide which SLI menus you fill in Section 5.

**Q2.3 — Where does it run?** (cloud provider, region, hosting service)
Your answer: `[FILL]`

**Q2.4 — What outside services does it depend on?** (payments, login, email, AI model provider, database host, maps, etc.)
Your answer: `[FILL]` *(You will detail these in Section 10.)*

**Q2.5 — What happens to a customer if the product is down for one hour?** `[PICK]`

- [ ] Nothing serious — they wait
- [ ] They are annoyed or lose a little time
- [ ] They lose money or miss a deadline
- [ ] Safety, legal, or health impact

💡 Higher impact means stricter targets in Section 6.

**Q2.6 — What is the product's reliability tier?** `[PICK]`

| Tier | Meaning | Typical use |
|---|---|---|
| Tier 1 — Critical | Down = customers lose money, data, or safety | Payments, healthcare, core platform |
| Tier 2 — Important | Down = customers blocked from main task | Most paid SaaS |
| Tier 3 — Standard | Down = inconvenient only | Internal tools, free tools |

Your answer (Tier 1 / 2 / 3): `[FILL]` Why: `[FILL]`

---

# 3. Lifecycle phases (development → first 500 customers)

Every project uses the same five phases so reports can be compared. **Targets in Section 6 tighten phase by phase.**

**Q3.1 — Which phase is the product in right now?** `[PICK]`

| # | Phase | Who uses it | Customers (default range) |
|---|---|---|---|
| P1 | **Build** (development) | Team only | 0 |
| P2 | **Staging / QA** (test copy of production) | Team + testers | 0 |
| P3 | **Private beta** (invited users) | Invited users | 1–25 |
| P4 | **Public launch** | Anyone | 26–150 |
| P5 | **Scale to 500** | Anyone | 151–500 |

Current phase: `[FILL]`

**Q3.2 — What exactly counts as a "customer"?** (so the number 500 means the same thing for everyone)
*Example: "A customer is an account that logged in at least once in the last 30 days and is not an employee or test account."*
Your answer: `[FILL]`

**Q3.3 — Planned dates for each phase.**

| Phase | Planned start | Planned end | Actual start | Actual end |
|---|---|---|---|---|
| P1 Build | `[FILL]` | `[FILL]` | | |
| P2 Staging / QA | `[FILL]` | `[FILL]` | | |
| P3 Private beta | `[FILL]` | `[FILL]` | | |
| P4 Public launch | `[FILL]` | `[FILL]` | | |
| P5 Scale to 500 | `[FILL]` | `[FILL]` | | |

**Q3.4 — If you changed the default customer ranges above, what are they and why?**
Your answer: `[FILL]` *(or write `Not changed`)*

---

# 4. Critical user journeys (what we protect first)

💡 Do not measure everything. Measure the 3–5 things a customer *must* be able to finish. Everything else is a bonus.

**Q4.1 — List your top 3–5 critical user journeys.**

| ID | Journey name | Steps in plain words | Why it matters | Tier (1/2/3) |
|---|---|---|---|---|
| J1 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| J2 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| J3 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| J4 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| J5 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

*Example row: J1 — Sign up and log in — enter email → get code → see dashboard — no login, no customers — Tier 1.*

⚠️ Common mistake: listing technical parts ("database", "server"). List what the *customer* does.

**Q4.2 — What would make a customer leave or ask for a refund?** (list top 3 failures)
Your answer: `[FILL]`

---

# 5. SLIs — what we measure

**How an SLI works (one formula):**

> **SLI % = good events ÷ valid events × 100**

- *Valid event* = something we should count (a real customer request).
- *Good event* = a valid event that went well.
- Leave out test traffic, bots you blocked on purpose, and customer mistakes (like a wrong password).

## 5A. SLIs for every product

Fill one row for each journey from Section 4. Add rows if needed.

| SLI ID | Journey | What we measure `[PICK type]` | "Good event" means | "Valid event" means | Measured where | Tool / data source | Owner |
|---|---|---|---|---|---|---|---|
| SLI-1 | J1 | Availability | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| SLI-2 | J1 | Speed (latency) | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| SLI-3 | J2 | Availability | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| SLI-4 | J2 | Speed (latency) | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| SLI-5 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

*Example SLI-1: Availability — Good = request returns status 200–399 — Valid = all real user requests to /login — Measured at the load balancer — Tool: cloud monitoring — Owner: Sam.*
*Example SLI-2: Speed — Good = response in under 800 ms — Valid = all successful /login requests — Measured at the server (p95).*

**Type menu `[PICK type]`:** Availability · Latency (speed) · Correctness (right answer) · Freshness (data is up to date) · Durability (data not lost) · Throughput (how many handled).

**Q5.1 — Is each SLI measured as close to the customer as possible?** (best: from the customer's browser/app; good: at the edge/load balancer; weaker: inside the server)
Your answer: `[FILL]`

**Q5.2 — Did you test that the measurement is correct?** (e.g., break something on purpose in staging and confirm the number goes down)
Your answer: `[FILL]` *Date tested: `[FILL]`*

**Q5.3 — Which events do you exclude from the count, and why?** (test accounts, planned maintenance, customer errors)
Your answer: `[FILL]`

## 5B. Extra SLIs — Web app / SaaS (fill only if ticked in Q2.2, else write `N/A`)

| SLI | Plain meaning | Your measure | Tool |
|---|---|---|---|
| Page load speed (LCP) | How fast the main content appears | `[FILL]` | `[FILL]` |
| Page responsiveness (INP) | How fast the page reacts to a click | `[FILL]` | `[FILL]` |
| Front-end error rate | % of visits with a browser error | `[FILL]` | `[FILL]` |
| Login success rate | % of valid logins that work | `[FILL]` | `[FILL]` |
| Checkout / payment success | % of valid payments that complete | `[FILL]` | `[FILL]` |
| Background jobs finish on time | % of jobs (emails, reports) done within target | `[FILL]` | `[FILL]` |

## 5C. Extra SLIs — API / backend (fill only if ticked, else `N/A`)

| SLI | Plain meaning | Your measure | Tool |
|---|---|---|---|
| Success rate | % of calls with no server error (5xx) | `[FILL]` | `[FILL]` |
| Latency p95 / p99 | Speed for 95% / 99% of calls | `[FILL]` | `[FILL]` |
| Rate-limit rejections | % of valid calls blocked by our own limits | `[FILL]` | `[FILL]` |
| Data freshness | How old the newest data is | `[FILL]` | `[FILL]` |
| Queue delay | How long work waits before starting | `[FILL]` | `[FILL]` |

## 5D. Extra SLIs — Mobile app (fill only if ticked, else `N/A`)

| SLI | Plain meaning | Your measure | Tool |
|---|---|---|---|
| Crash-free sessions | % of app sessions with no crash | `[FILL]` | `[FILL]` |
| Crash-free users | % of users who never crashed | `[FILL]` | `[FILL]` |
| App-not-responding (ANR) rate | % of sessions where the app froze | `[FILL]` | `[FILL]` |
| Cold start time | Time from tap to usable screen | `[FILL]` | `[FILL]` |
| App-to-server call success | % of calls from the app that work | `[FILL]` | `[FILL]` |
| Offline sync success | % of offline changes that sync later | `[FILL]` | `[FILL]` |

## 5E. Extra SLIs — AI / LLM feature or AI agent (fill only if ticked, else `N/A`)

💡 Normal monitoring misses AI's most dangerous failure: the system answers fast, with no error, but the answer is **wrong**. So we also measure quality.

| SLI | Plain meaning | Your measure | How measured (tool / test set) |
|---|---|---|---|
| Time to first token (TTFT) | How long until the answer *starts* appearing | `[FILL]` | `[FILL]` |
| End-to-end response time | Question sent → full answer done | `[FILL]` | `[FILL]` |
| AI request success rate | % of AI calls with no error or timeout | `[FILL]` | `[FILL]` |
| Provider failure / fallback rate | % of calls that needed a backup model | `[FILL]` | `[FILL]` |
| Answer quality pass rate | % of answers that pass our quality test | `[FILL]` | `[FILL]` |
| Grounded-answer rate (no made-up facts) | % of answers supported by our sources | `[FILL]` | `[FILL]` |
| Format compliance | % of answers in the required format (e.g., valid JSON) | `[FILL]` | `[FILL]` |
| Safety / PII leak rate | % of answers that leak private data or break safety rules | `[FILL]` | `[FILL]` |
| Quality drift | Change in quality score vs the 30-day baseline | `[FILL]` | `[FILL]` |
| Cost per request / per customer | Money spent on AI per request or per customer | `[FILL]` | `[FILL]` |

**Extra rows for AI agents that do multi-step tasks:**

| SLI | Plain meaning | Your measure | How measured |
|---|---|---|---|
| Task success rate | % of tasks finished correctly | `[FILL]` | `[FILL]` |
| Tool-call failure rate | % of tool/API calls the agent made that failed | `[FILL]` | `[FILL]` |
| Human hand-off rate | % of tasks that needed a human | `[FILL]` | `[FILL]` |
| Loop / runaway rate | % of tasks that exceeded step or cost limits | `[FILL]` | `[FILL]` |

**Q5.4 — How is AI quality judged?** (tick all that apply)

- [ ] A fixed test set of questions with known good answers → size: `[FILL]`
- [ ] Another AI model scores the answers ("AI judge") → known weaknesses checked? `[FILL]`
- [ ] Humans review a random sample → how many per week: `[FILL]`
- [ ] Customer thumbs-up / thumbs-down
- [ ] Other: `[FILL]`

⚠️ AI judges can favor longer answers. Check a sample by hand.

**Q5.5 — Which AI model(s) and version(s) are used, and what happens when the provider changes or retires one?**
Your answer: `[FILL]`

---

# 6. SLOs — our goals (tighten as the product matures)

## 6A. Pick the window

**Q6.1 — Measurement window `[PICK]`:** Rolling 30 days (recommended) / Rolling 28 days / Calendar month / Other: `[FILL]`
💡 Use the *same* window for every SLO in this document.

## 6B. Do you have enough traffic to measure?

**Q6.2 — About how many valid events (requests, logins, payments, AI calls) do you expect in 30 days at each phase?**

| Phase | Expected valid events in 30 days | Source of estimate |
|---|---|---|
| P3 Private beta | `[FILL]` | `[FILL]` |
| P4 Public launch | `[FILL]` | `[FILL]` |
| P5 Scale to 500 | `[FILL]` | `[FILL]` |

**Rule of thumb:** Allowed bad events = events × (100% − SLO).
*Example: 20,000 events × 0.1% = only 20 bad events allowed at a 99.9% goal.*
If the answer is **fewer than about 10**, your goal is too strict for your traffic. Either lower it, widen the window, or add a **synthetic probe** (a robot that tests the journey every minute).

**Q6.3 — Will you use synthetic probes (robot checks)?** `[PICK]` Yes / No. If yes, what and how often: `[FILL]`

## 6C. Targets per phase

Suggested starting points are in *italics* (v1.1 uses a **strict profile**: customers should see high reliability from the very first beta). Replace with your real numbers. `Measure only` means track the number but do not fail anything yet.

**Availability (the journey works)**

| Journey | P1 Build | P2 Staging | P3 Beta | P4 Launch | P5 Scale to 500 |
|---|---|---|---|---|---|
| Suggested for Tier 1 journeys | *Measure only* | *98%* | *99.5%* | *99.9%* | *99.95%* |
| Suggested for Tier 2 journeys | *Measure only* | *97%* | *99.0%* | *99.5%* | *99.9%* |
| Your J1 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Your J2 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Your J3 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Your J4–J5 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

**Latency (speed) — use "X% of events faster than Y"**

| SLI | P1 Build | P2 Staging | P3 Beta | P4 Launch | P5 Scale to 500 |
|---|---|---|---|---|---|
| *Suggested API p95* | *Measure only* | *1000 ms* | *800 ms* | *500 ms* | *400 ms* |
| *Suggested API p99* | *Measure only* | *2500 ms* | *2000 ms* | *1500 ms* | *1000 ms* |
| *Suggested web LCP p75* | *Measure only* | *3 s* | *2.5 s* | *2.5 s* | *2 s* |
| Your latency SLO 1 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Your latency SLO 2 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

**Mobile (skip if not mobile)**

| SLI | P1 | P2 | P3 | P4 | P5 |
|---|---|---|---|---|---|
| *Suggested crash-free sessions* | *Measure only* | *99.5%* | *99.7%* | *99.9%* | *99.95%* |
| *Suggested cold start p90* | *Measure only* | *3 s* | *2.5 s* | *2 s* | *2 s* |
| Your mobile SLO | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

**AI / agent (skip if not AI)**

| SLI | P1 | P2 | P3 | P4 | P5 |
|---|---|---|---|---|---|
| *Suggested TTFT p95* | *Measure only* | *2 s* | *1.5 s* | *1 s* | *0.8 s* |
| *Suggested end-to-end p95* | *Measure only* | *10 s* | *8 s* | *6 s* | *5 s* |
| *Suggested AI request success rate* | *Measure only* | *98%* | *99.5%* | *99.9%* | *99.9%* |
| *Suggested quality pass rate* | *Measure only* | *85%* | *90%* | *95%* | *97%* |
| *Suggested grounded-answer rate* | *Measure only* | *90%* | *95%* | *97%* | *98%* |
| *Suggested safety / PII leak rate* | *Measure only* | *≤ 0.5%* | *≤ 0.1%* | *≤ 0.05%* | *0 known leaks* |
| *Suggested agent task success rate* | *Measure only* | *80%* | *88%* | *93%* | *95%* |
| Your AI SLO 1 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Your AI SLO 2 | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Max AI cost per customer per month | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

⚠️ Suggested numbers are starting points, not rules. Product type, customer impact (Q2.5) and traffic (Q6.2) decide your real numbers. A strict number you cannot measure or afford to defend (see Q6.2 and Section 11C) is worse than an honest looser one.

**Q6.6 — Which profile did you use?** `[PICK]` Strict (as suggested above) / Relaxed (my own looser numbers, explained in Q6.4) / Custom. Why: `[FILL]`

**Q6.7 — Does each phase's target tighten or stay equal (never loosen)?** `[PICK]` Yes / No → if No, why: `[FILL]`

**Q6.4 — For each target you chose above, why is it the right level?** (what does a customer feel at this number?)
Your answer: `[FILL]`

**Q6.5 — Is any SLO stricter than a company you depend on can support?** (see Section 10 before answering)
Your answer: `[FILL]`

## 6D. Error budget cheat sheet (30-day window = 43,200 minutes)

| SLO | Error budget | Allowed "down" time per 30 days | Per week (approx.) |
|---|---|---|---|
| 95% | 5% | 36 hours | 8.4 hours |
| 99% | 1% | 7 hours 12 min | 1 hour 40 min |
| 99.5% | 0.5% | 3 hours 36 min | 50 min |
| 99.9% | 0.1% | 43 min 12 s | 10 min |
| 99.95% | 0.05% | 21 min 36 s | 5 min |
| 99.99% | 0.01% | 4 min 19 s | 1 min |

💡 Each extra "9" makes the budget 10 times smaller and costs much more to achieve. Pick the *lowest* goal that keeps customers happy.

---

# 7. Error budget policy — what we DO when the budget is used

💡 This is the most important section. An SLO without clear actions does nothing.

**Q7.1 — Fill in what happens at each level of remaining budget.** Be specific. "Discuss as a team" is not an action.

| Budget remaining | Status | What we do (specific actions) | Who decides |
|---|---|---|---|
| More than 50% | 🟢 Healthy | *Normal releases. Experiments allowed.* `[FILL]` | `[FILL]` |
| 25%–50% | 🟡 Careful | `[FILL]` *Example: extra testing, smaller releases, no risky changes on Fridays* | `[FILL]` |
| 1%–25% | 🟠 Danger | `[FILL]` *Example: only reliability fixes and urgent bugs ship* | `[FILL]` |
| 0% (used up) | 🔴 Exhausted | `[FILL]` *Example: feature freeze until back above 25%; write a post-incident review* | `[FILL]` |

**Q7.2 — Who may approve an exception** (ship something risky even when the budget is low), and what must they write down?
Your answer: `[FILL]`

**Q7.3 — What does NOT count against the budget?** (planned maintenance announced in advance, customer mistakes, attacks handled by security, etc.)
Your answer: `[FILL]`

**Q7.4 — If the problem is caused by a vendor outside our control, do we still spend our budget?** `[PICK]` Yes (customers feel it either way) / No (we track it separately). Why: `[FILL]`

**Q7.5 — Who gets the budget report and how often?**
Your answer: `[FILL]`

---

# 8. Alerts — how we find out fast

**How burn rate works:** A burn rate of **1×** uses the whole budget in exactly one window (30 days). **14.4×** uses it in about 2 days. Alert when a *short* window and a *long* window both look bad. This catches fast disasters quickly and avoids false alarms.

**Q8.1 — Starting alert set (edit if needed).**

| Alert | Burn rate | Long window | Short window | Budget used if it continues | Action | Who is notified |
|---|---|---|---|---|---|---|
| Fast burn | 14.4× | 1 hour | 5 min | 2% | 📟 Page someone now | `[FILL]` |
| Medium burn | 6× | 6 hours | 30 min | 5% | 📟 Page someone now | `[FILL]` |
| Slow burn | 1× | 3 days | 6 hours | 10% | 🎫 Create a ticket | `[FILL]` |
| Budget remaining < 25% | n/a | 30 days | n/a | n/a | 📧 Email + see Section 7 | `[FILL]` |

**Q8.2 — Low-traffic fix.** At few customers, one failure can look like a disaster. What is the minimum number of events before an alert may fire?
Your answer: `[FILL]` *Example: Ignore alerts if fewer than 20 events in the short window.*

**Q8.3 — Who is on call?** (even if it is one founder)

| Hours | Person | Backup | How they are reached |
|---|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

**Q8.4 — Where do alerts go and where is the dashboard?** Alert tool: `[FILL]` Dashboard link: `[FILL]`

**Q8.5 — How do we avoid alert overload?** (what do we do if the same alert fires 3 times and nobody acts?)
Your answer: `[FILL]`

**Q8.6 — Every page-level alert needs a "what do I do?" link.**

| Alert name | Journey / SLI | First 3 things to check | Runbook link | Owner |
|---|---|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

⚠️ An alert with no runbook wakes a person up to guess.

**Q8.7 — Detection and recovery speed targets.**

| Measure | Meaning | P3 Beta | P4 Launch | P5 Scale to 500 |
|---|---|---|---|---|
| MTTD (time to notice) | Failure starts → alert fires | `[FILL]` | `[FILL]` | `[FILL]` |
| MTTA (time to acknowledge) | Alert fires → a person is working on it | `[FILL]` | `[FILL]` | `[FILL]` |
| MTTR (time to restore) | Failure starts → customers fine again | `[FILL]` | `[FILL]` | `[FILL]` |

*Example: MTTD 5 min · MTTA 15 min · MTTR 60 min at launch.*

**Q8.8 — How and when did we test that alerts really fire and reach a human?** (simulate a failure in staging, check the phone rings)
Date tested: `[FILL]` Result: `[FILL]` Next test date: `[FILL]`

**Q8.9 — Do alerts also watch for "silent failure"?** (traffic suddenly drops to zero, jobs stop running, AI quality score drops with no errors)
Your answer: `[FILL]`

---

# 9. SLA — what we promise customers (optional until public launch)

⚠️ **Stop here and talk to a human decision-maker and a lawyer before filling this in.** This document is not legal advice.

**Q9.1 — Do we offer an SLA?** `[PICK]`

- [ ] No SLA yet (normal for P1–P3). Revisit date: `[FILL]`
- [ ] Yes — from phase: `[FILL]`
- [ ] Only for paid / enterprise customers

If **No SLA yet**, write `N/A` in Q9.2–Q9.7 and move on.

**Q9.2 — What is promised?**

| Item | Your answer |
|---|---|
| Metric promised | `[FILL]` *Example: monthly uptime of the main app* |
| Promised level | `[FILL]` *Must be easier than the matching SLO.* |
| Matching internal SLO (from Section 6) | `[FILL]` |
| Safety margin (SLO minus SLA) | `[FILL]` |
| Measurement window | `[FILL]` |
| Who measures and where customers can see it | `[FILL]` |

**Q9.3 — What is NOT covered?** (planned maintenance, customer mistakes, free plans, force majeure, third-party outages, beta features)
Your answer: `[FILL]`

**Q9.4 — What happens when we miss it?** (service credit, refund, other)

| Result for the month | Remedy |
|---|---|
| `[FILL]` | `[FILL]` |
| `[FILL]` | `[FILL]` |

**Q9.5 — How does a customer claim, and within how many days?** `[FILL]`

**Q9.6 — Support promises (optional but common in the first 500 customers).**

| Severity | Example | First reply within | Fix or workaround target |
|---|---|---|---|
| Critical | Customer cannot use the product | `[FILL]` | `[FILL]` |
| High | Major feature broken | `[FILL]` | `[FILL]` |
| Normal | Small bug or question | `[FILL]` | `[FILL]` |
| Support hours | | `[FILL]` | |

**Q9.7 — Where is the SLA text published, and who approved it?** Link: `[FILL]` Approved by (name, date): `[FILL]`

---

# 9B. Customer-facing wording (plain-language reliability promise)

💡 Customers do not read SLO tables. Write the version they will read. Keep it short, honest, and free of jargon. Have a lawyer check it before publishing (Q9.7).

**Q9B.1 — Fill in this sentence pattern for each promise.** If there is no SLA yet, write the *goal* version and say it is a goal, not a guarantee.

> "We aim for **`[FILL: promise, e.g. the app to be available 99.9% of the time each month]`**. We measure it by **`[FILL: how, e.g. automatic checks every minute]`** and show the results at **`[FILL: status page link]`**. If we miss it, **`[FILL: remedy, e.g. you can request a 10% credit within 30 days]`**. This does not cover **`[FILL: exclusions in plain words]`**."

**Q9B.2 — Reading-level check.** Could a 10-year-old understand the text above? `[PICK]` Yes / No → rewrite until Yes.

**Q9B.3 — Where will customers see it?** (pricing page, terms of service, welcome email, status page) `[FILL]`

**Q9B.4 — How do customers report a problem and what will we reply within?** Channel: `[FILL]` First reply within: `[FILL]` (must match Q9.6)

**Q9B.5 — Words we must NOT use** unless approved (for example "guaranteed", "100%", "never down", "unlimited"): `[FILL]`

---

# 10. Dependencies — can our promise be higher than theirs?

💡 If your product needs five services to work, you cannot promise more than they can deliver — unless you have a backup. Rough check: multiply their availabilities. Two services at 99.9% each → about 99.8% combined.

**Q10.1 — List every outside service that can break a critical journey.**

| Service | Used for | Journeys affected | Their published SLA / uptime | Our backup if it fails | Status page link |
|---|---|---|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

**Q10.2 — Combined best possible availability of the chain** (multiply the numbers above):
Your answer: `[FILL]` Is it at least as high as our SLO in Section 6? `[PICK]` Yes / No → if No, what changes: `[FILL]`

**Q10.3 — Rate limits and quotas we could hit** (AI provider tokens per minute, email per day, API calls per second):
Your answer: `[FILL]`

**Q10.4 — What is our plan if the AI provider (or other key vendor) is slow, wrong, or down?** (fallback model, cached answer, friendly error message, queue and retry)
Your answer: `[FILL]`

---

# 11. Data safety — backups and recovery

**Q11.1 — What data would hurt most to lose?** `[FILL]`

**Q11.2 — Recovery targets.**

| Item | Meaning | P3 Beta | P4 Launch | P5 Scale to 500 |
|---|---|---|---|---|
| RPO (maximum data we can lose) | *Example: 24 hours → 1 hour → 15 min* | `[FILL]` | `[FILL]` | `[FILL]` |
| RTO (maximum time to restore service) | *Example: 8 hours → 4 hours → 1 hour* | `[FILL]` | `[FILL]` | `[FILL]` |

**Q11.3 — Backups: how often, where stored, who can restore?** `[FILL]`

**Q11.4 — When was a restore last tested successfully?** Date: `[FILL]` Result: `[FILL]`
⚠️ A backup that was never restored is only a hope.

---

# 11A. Security and compliance targets

💡 Security is reliability's cousin: a hacked product is a "down" product. Set time limits so problems do not sit around. This section sets targets; your security policy has the details.

**Q11A.1 — Which rules or standards apply to this product?** (tick all that apply)

- [ ] Privacy law (e.g. GDPR, CCPA, other): `[FILL]`
- [ ] Payments rules (PCI DSS)
- [ ] Health data rules (HIPAA or local equivalent)
- [ ] Security audit expected by customers (SOC 2, ISO 27001)
- [ ] AI-specific rules or customer AI policies: `[FILL]`
- [ ] None known — confirmed by: `[FILL]`

**Q11A.2 — Security fix-time targets.** Time from "we know about it" to "fixed or safely worked around".

| Severity of the weakness | P3 Beta | P4 Launch | P5 Scale to 500 |
|---|---|---|---|
| Critical (attackers can get in or steal data) | `[FILL]` *Example: 72 h → 48 h → 24 h* | `[FILL]` | `[FILL]` |
| High | `[FILL]` *Example: 14 d → 7 d → 7 d* | `[FILL]` | `[FILL]` |
| Medium | `[FILL]` *Example: 60 d → 30 d → 30 d* | `[FILL]` | `[FILL]` |

**Q11A.3 — Security health checks.**

| Check | How often | Target | Owner |
|---|---|---|---|
| Dependency and package scan | `[FILL]` | `[FILL]` *Example: 0 unfixed critical findings* | `[FILL]` |
| Secrets rotation (keys, tokens, passwords) | `[FILL]` | `[FILL]` | `[FILL]` |
| Access review (who can reach production) | `[FILL]` | `[FILL]` | `[FILL]` |
| Penetration test or security review | `[FILL]` | `[FILL]` | `[FILL]` |
| Login-failure and abuse monitoring | `[FILL]` | `[FILL]` | `[FILL]` |

**Q11A.4 — If customer data is exposed, who is told, by whom, and within how long?** (customers, regulators, partners) `[FILL]`

**Q11A.5 — AI-specific safety targets** (skip if not AI): prompt-injection tests run how often `[FILL]` · harmful-output review sample size `[FILL]` · customer data never used for model training unless agreed — confirmed by `[FILL]`

---

# 11B. Capacity and load testing

💡 The first 500 customers do not arrive evenly. A launch post or an email can bring many people in minutes.

**Q11B.1 — Expected traffic.**

| Item | P3 Beta | P4 Launch | P5 Scale to 500 | Source of estimate |
|---|---|---|---|---|
| Customers at the end of the phase | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Typical peak requests per second | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Biggest spike we can imagine (× normal) | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Largest data size or file we must handle | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| AI calls or tokens per minute at peak (if AI) | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

**Q11B.2 — Load test pass rules.** A load test is a rehearsal with fake traffic in staging. It passes only if the SLOs of that phase still hold.

| Test | Traffic level | How long | Pass rule (numbers) | Last run | Result |
|---|---|---|---|---|---|
| Normal load | `[FILL]` *Example: expected peak* | `[FILL]` | `[FILL]` *Example: p95 under target, errors under 0.1%* | `[FILL]` | `[FILL]` |
| Spike | `[FILL]` *Example: 5× expected peak* | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Long run (soak) | `[FILL]` *Example: normal for 4 hours* | `[FILL]` | `[FILL]` *Example: no memory growth, no slowdown* | `[FILL]` | `[FILL]` |

**Q11B.3 — Where is the first thing most likely to break?** (database, queue, AI provider limit, third-party API) `[FILL]`

**Q11B.4 — Limits and protection.** Rate limits per customer `[FILL]` · automatic scaling on/off and its maximum `[FILL]` · what the product does when overloaded (slow down, queue, show a friendly message, turn off a non-critical feature) `[FILL]`

**Q11B.5 — Headroom rule.** How much unused capacity must we keep? *Example: stay below 60% of the tested maximum.* `[FILL]`

---

# 11C. Cost and FinOps targets

💡 A product that is reliable but loses money on every customer will not last to customer 500. Track cost the same way as reliability: with a number and an action.

**Q11C.1 — What does each customer cost us per month?**

| Cost item | P3 Beta | P4 Launch | P5 Scale to 500 | Measured how |
|---|---|---|---|---|
| Hosting / cloud | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| AI model usage (tokens, calls) | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Third-party services | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| Monitoring and tools | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| **Total cost per customer** | `[FILL]` | `[FILL]` | `[FILL]` | |
| Revenue per customer (if known) | `[FILL]` | `[FILL]` | `[FILL]` | |

**Q11C.2 — Cost guardrails.** Maximum monthly spend `[FILL]` · maximum cost per customer `[FILL]` · maximum cost per AI request `[FILL]`

**Q11C.3 — Cost alerts and actions.**

| When | Action | Who |
|---|---|---|
| Spend reaches 70% of monthly limit | `[FILL]` *Example: email the owner* | `[FILL]` |
| Spend reaches 90% | `[FILL]` *Example: turn off non-critical AI features* | `[FILL]` |
| Spend reaches 100% | `[FILL]` *Example: hard cap; show friendly message* | `[FILL]` |
| One customer uses more than `[FILL]`× the average | `[FILL]` | `[FILL]` |

**Q11C.4 — Does saving money ever beat reliability?** Write the rule. *Example: we never cut backups or security to save money, but we may switch to a cheaper AI model for non-critical features if quality stays above target.* `[FILL]`

**Q11C.5 — Who reviews cost, and how often?** `[FILL]`

---

# 12. Incidents and communication

**Q12.1 — Severity levels tied to our SLOs.**

| Level | When it applies | Who responds | Customer notice |
|---|---|---|---|
| SEV1 | A Tier 1 journey is down, or a fast-burn alert is firing, or data is at risk | `[FILL]` | `[FILL]` within `[FILL]` min |
| SEV2 | A Tier 2 journey is degraded, or a medium-burn alert is firing | `[FILL]` | `[FILL]` |
| SEV3 | Small impact, slow-burn alert | `[FILL]` | `[FILL]` |

**Q12.2 — Where do customers see status?** (status page, in-app banner, email) Link: `[FILL]`

**Q12.3 — When is a written post-incident review required, and who writes it?** `[FILL]` *Example: any SEV1, or any event using more than 20% of the monthly budget, due within 5 working days.*

**Q12.4 — Where do post-incident reviews live, and who tracks the follow-up tasks?** `[FILL]`

---

# 13. Phase gates — when can we move to the next phase?

Fill the "Evidence needed" column with measurable proof. A phase may not start until every row is ticked and the owner signs.

| Gate | Evidence needed (numbers, not feelings) | Done `[ ]` | Date | Signed by |
|---|---|---|---|---|
| **P1 → P2** (Build → Staging) | All SLIs defined and measured in staging; dashboards exist; synthetic probes running (if used). Details: `[FILL]` | `[ ]` | | |
| **P2 → P3** (Staging → Private beta) | Targets from Section 6 met for `[FILL]` consecutive days; alerts tested (Q8.8); on-call set (Q8.3); backup restore tested (Q11.4); no open critical security findings (Q11A.2); normal-load test passed (Q11B.2). Details: `[FILL]` | `[ ]` | | |
| **P3 → P4** (Beta → Public launch) | Beta SLOs met for `[FILL]` days; budget policy rehearsed once; status page live; SLA decision made (Q9.1) and customer wording approved (Section 9B); spike test passed at `[FILL]`× expected launch traffic (Q11B.2); cost per customer under limit (Q11C.2); security health checks done (Q11A.3). Details: `[FILL]` | `[ ]` | | |
| **P4 → P5** (Launch → Scale to 500) | Launch SLOs met for `[FILL]` days; no unresolved SEV1 follow-ups; soak test passed (Q11B.2); cost per customer under limit for `[FILL]` months; security fix-time targets met (Q11A.2). Details: `[FILL]` | `[ ]` | | |
| **P5 complete** (500 customers reached) | 500 customers per Q3.2 definition; P5 SLOs met for `[FILL]` days; cost and capacity reviewed; lessons recorded in Section 15. Details: `[FILL]` | `[ ]` | | |

**Q13.1 — What do we do if a gate fails?** (wait, fix, shrink launch size, pause sign-ups)
Your answer: `[FILL]`

**Q13.2 — What is our "stop sign-ups" rule?** (what number or event pauses new customer onboarding)
Your answer: `[FILL]`

---

# 14. Reporting and review

**Q14.1 — Review schedule.**

| Meeting | How often | Who attends | What we check |
|---|---|---|---|
| Quick check | Weekly | `[FILL]` | Budget remaining, burn rate, open alerts |
| Report | Monthly | `[FILL]` | SLO results table below, incidents, actions |
| SLO review | Every phase change and at least every 90 days | `[FILL]` | Are the targets right? Still the right journeys? |

**Q14.2 — Monthly results table (copy one block per month).**

| Month | SLI / SLO | Target | Actual | Budget left | Met? | Notes / action |
|---|---|---|---|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[ ]` | `[FILL]` |

**Q14.3 — SLO change log.** Record every change to a target and why. Never delete rows.

| Date | Changed | From → To | Why | Approved by |
|---|---|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

---

# 15. Risks, assumptions, and open questions

**Q15.1 — Top risks to hitting our SLOs.**

| Risk | Chance (L/M/H) | Impact (L/M/H) | What we do about it | Owner |
|---|---|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |
| `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` | `[FILL]` |

**Q15.2 — Assumptions we made** (everything marked `ASSUMED:` above)
Your answer: `[FILL]`

**Q15.3 — Open questions** (everything marked `UNKNOWN` above)

| Question | Who finds out | Due date |
|---|---|---|
| `[FILL]` | `[FILL]` | `[FILL]` |

---

# 16. Sign-off

| Role | Name | Decision (Approved / Changes needed) | Date |
|---|---|---|---|
| Product owner | `[FILL]` | `[FILL]` | `[FILL]` |
| Engineering / reliability owner | `[FILL]` | `[FILL]` | `[FILL]` |
| QA | `[FILL]` | `[FILL]` | `[FILL]` |
| Support / customer success | `[FILL]` | `[FILL]` | `[FILL]` |
| Legal / business (required if an SLA is offered) | `[FILL]` | `[FILL]` | `[FILL]` |

---

# 17. Final checklist — "Am I done?"

Tick every box. If you cannot tick one, go back to that section.

- [ ] I searched this file for `[FILL` and found none
- [ ] Every "not applicable" answer says why
- [ ] Every guess is marked `ASSUMED:` and every unknown is in Section 15
- [ ] I listed 3–5 critical journeys, written from the customer's side (Section 4)
- [ ] Every SLI says what a good event and a valid event are (Section 5A)
- [ ] I proved at least one SLI shows the right number when something breaks (Q5.2)
- [ ] SLO targets exist for all five phases, and each is stricter than or equal to the one before (Section 6C)
- [ ] I checked I have enough traffic for each SLO (Q6.2)
- [ ] Section 7 has specific actions, not "discuss as a team"
- [ ] Alerts have named people and a low-traffic rule (Section 8)
- [ ] If there is an SLA, it is easier than the SLO and a lawyer approved it (Section 9)
- [ ] Every outside service is listed with a backup plan (Section 10)
- [ ] Alerts have runbook links and were tested end to end (Q8.6, Q8.8)
- [ ] A customer-friendly version of the promise exists and a 10-year-old can read it (Section 9B)
- [ ] A backup restore has been tested (Q11.4)
- [ ] Security fix-time targets and applicable standards are filled in (Section 11A)
- [ ] Expected traffic, load-test pass rules and overload behavior are filled in (Section 11B)
- [ ] Cost per customer, guardrails, and cost actions are filled in (Section 11C)
- [ ] Severity levels and customer notices are defined (Section 12)
- [ ] Every phase gate has measurable evidence (Section 13)
- [ ] Review dates are on the calendar (Section 14)
- [ ] Section 18 summary matches the answers above
- [ ] Sign-offs are complete (Section 16)

---

# 18. Machine-readable summary (for dashboards and automation across all projects)

Copy your answers into this block. Keep the keys exactly as written so one script can read 100s of projects.

```yaml
slo_sla_sli_summary:
  template_version: "1.1"
  product_name: "[FILL]"
  product_id: "[FILL]"
  product_types: []            # web | api | mobile | ai | agent
  reliability_tier: 0          # 1, 2, or 3
  current_phase: ""            # P1 | P2 | P3 | P4 | P5
  customer_definition: "[FILL]"
  customers_now: 0
  measurement_window_days: 30
  reliability_owner: "[FILL]"
  slis:
    - id: "SLI-1"
      journey: "J1"
      type: ""                 # availability | latency | correctness | freshness | durability | throughput
      good_event: "[FILL]"
      valid_event: "[FILL]"
      tool: "[FILL]"
  slos:
    - sli_id: "SLI-1"
      p1: "measure_only"
      p2: ""
      p3: ""
      p4: ""
      p5: ""
  sla:
    offered: false
    from_phase: ""
    promised_level: ""
    approved_by: ""
  slo_profile: ""              # strict | relaxed | custom
  error_budget_policy_defined: false
  alerts_defined: false
  alerts_tested_date: ""
  on_call_defined: false
  mttd_target_minutes_p5: 0
  mttr_target_minutes_p5: 0
  customer_wording_approved: false
  backup_restore_tested_date: ""
  security:
    applicable_standards: []   # gdpr | pci | hipaa | soc2 | iso27001 | other | none
    critical_fix_hours_p5: 0
    last_security_review_date: ""
  capacity:
    expected_peak_rps_p5: 0
    spike_multiplier_tested: 0
    last_load_test_date: ""
    load_test_passed: false
  cost:
    max_monthly_spend: 0
    max_cost_per_customer: 0
    cost_per_customer_now: 0
  next_review_date: ""
  open_unknowns: 0
```

---

# Appendix A — Common mistakes (and fixes)

| Mistake | Why it hurts | Fix |
|---|---|---|
| Measuring server health (CPU, memory) instead of customer results | The server can look fine while customers fail | Measure the journey (Section 4–5) |
| 100% target | Impossible and blocks all change | Use an SLO with a real error budget |
| SLA equal to or stricter than SLO | You break promises before you notice | SLA must be easier than SLO (Q9.2) |
| Too many SLOs | Nobody can watch 40 numbers | 3–5 journeys, 1–3 SLOs each |
| Average only | Hides the slow 5% | Use percentiles (p95 / p99) |
| No action when budget is spent | SLO is decoration | Fill Section 7 |
| Strict target with tiny traffic | One failure breaks it | Fill Q6.2 and Q8.2 |
| AI: only measuring speed | Fast wrong answers go unseen | Measure quality (Section 5E) |
| Never testing the backup | Restore fails when needed | Q11.4 |
| Setting it once and forgetting | Targets go stale | Review at each phase and every 90 days |

# Appendix B — Where these ideas come from

- Google, *Site Reliability Engineering* book — Ch. 3 "Embracing Risk" and Ch. 4 "Service Level Objectives" (definitions of SLI, SLO, SLA, error budget).
- Google, *SRE Workbook* — "Implementing SLOs" and "Alerting on SLOs" (SLA looser than SLO; multi-window, multi-burn-rate alerts: 14.4× / 6× / 1×).
- Google Cloud Monitoring docs — alerting on error-budget burn rate.
- Core Web Vitals (LCP, INP) for web experience SLIs.
- LLM serving and observability literature — time to first token, inter-token latency, end-to-end latency, error and timeout rate, hallucination or groundedness rate, format compliance, cost per request, quality drift.
- General practice for security fix-time targets, load testing (normal, spike, soak), MTTD/MTTA/MTTR, and cloud cost guardrails. Check your own contracts and standards for exact required values.

Suggested target numbers in this file are starting points; check them against your own customers and contracts.

# Appendix C — Template change log

| Version | Date | Change | By |
|---|---|---|---|
| 1.0 | 2026-10-18 | First draft of the standard template | Claude (draft for owner review) |
| 1.1 | 2026-10-18 | Strict default targets; added Section 9B (customer wording), 11A (security and compliance), 11B (capacity and load testing), 11C (cost and FinOps); deeper alerting (runbooks, MTTD/MTTA/MTTR, alert testing, silent failure); phase gates, checklist and YAML summary extended | Claude (draft for owner review) |
