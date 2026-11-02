# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **What is this document?**
> A *Product Analytics Dashboard Spec* is a plan that says: **"What do we want to know about our product, what do we need to measure to know it, and what screens (dashboards) will show it?"**
> If you can answer simple questions in plain words, you can fill this in. No coding knowledge is needed.

> **Who is it for?** Product owners, founders, analysts, engineers, designers, QA testers, project managers, and **AI agents**. Anyone should be able to read a finished spec and build the dashboards **without guessing**.

> **Covers:** AI-driven development → internal testing → launch → **your first 500 customers**.
> **Works for:** B2C apps (web/mobile), B2B SaaS, and marketplaces / e-commerce. It is tool-agnostic (works with Mixpanel, Amplitude, PostHog, GA4, Looker, Metabase, Power BI, SQL warehouses, etc.).

---

## 1. The 10 golden rules

1. **Answer every question.** Never leave a field empty. If you don't know yet, write `TBD — owner: <name> — by: <date>`.
2. **Use plain words first.** Write like you are explaining to a 10-year-old. Add technical terms *after* the plain words.
3. **One thing = one name.** Pick a name for each metric, event, and dashboard and use it everywhere. Never rename without writing it in the Change History (Section 21).
4. **Give numbers, not feelings.** Write "at least 40% of new users finish setup within 24 hours", not "most users should finish setup quickly".
5. **Every metric needs: a plain definition, a formula, an owner, and a target.**
6. **Every dashboard chart must answer a question** from Section 4. If a chart answers nothing, delete it.
7. **Look at the example, then write your own.** Examples are marked `Example:`. Do **not** leave examples in your final version unless they are true for your product.
8. **Tick the boxes.** Each section ends with a `✅ Done when` list. Tick `[x]` only when it is really true.
9. **Do not collect data you do not need.** Every event and property must have a reason (privacy rule).
10. **If two people could read a sentence two different ways, rewrite it.**

---

## 2. Symbols used in this document

| Symbol | Meaning |
|---|---|
| 🟢 | **Required.** Must be filled before the spec is approved. |
| 🟡 | **Recommended.** Fill if it applies; otherwise write `N/A — because …`. |
| 🔵 | **Optional / advanced.** Skip with `N/A` if your product is small. |
| 🤖 | **AI-agent block.** Written for AI agents. Humans may skim; do not delete. |
| ✏️ | **Your answer goes here.** Replace the placeholder text. |
| 💡 | Helpful tip. |
| ⚠️ | Common mistake — read before answering. |
| `[ ]` / `[x]` | Not done / done. |

---

## 3. How to answer (answer formats)

| If the question asks for… | Write it like this | Example |
|---|---|---|
| A name | Short, no spaces problems, same everywhere | `Activation Rate` |
| A date | `YYYY-MM-DD` | `2026-11-30` |
| A percentage | Number + `%` + time window | `35% within 7 days` |
| A person | Role + name | `Product Owner — Priya S.` |
| A choice | Tick `[x]` exactly one (or many if allowed) | `[x] Weekly` |
| Unknown | `TBD — owner: <name> — by: <date>` | `TBD — owner: Sam — by: 2026-11-05` |
| Not applicable | `N/A — because <reason>` | `N/A — because we have no mobile app` |

---

## 4. Recommended order of filling (do NOT start at Section 1)

1. Sections 0–2 (basics) → 15 minutes
2. Sections 3–5 (phases, goals, audience) → 1 hour
3. Sections 6–7 (metrics, funnels) → 2 hours
4. Sections 8–10 (events, identity, data pipeline) → 2 hours (with an engineer)
5. Sections 11–12 (dashboards, alerts) → 2 hours (with a designer/analyst)
6. Sections 13–14 (privacy, QA) → 1 hour (with legal/QA)
7. Sections 15–20 (plan, rollout, risks, decisions) → 1 hour
8. **Last:** Section 1 (the one-page summary) and Section 22 (sign-off).

💡 Tip: Fill with **two people** — one who knows the *business*, one who knows the *product/tech*. Review the finished spec together.

---

## 5. Who does what while filling this

| Role | Fills sections | Reviews |
|---|---|---|
| Product Owner | 0–7, 16, 18 | Everything |
| Analyst / Data Lead | 6, 7, 9, 11, 12 | 8, 14 |
| Engineer | 8, 9, 10, 15 | 11, 13 |
| Designer | 11 | 5, 7 |
| QA | 14 | 8, 11 |
| Privacy / Legal | 13 | 8, 9 |
| Project Manager | 15, 19, 20, 22 | Everything |
| AI Agent 🤖 | Drafts proposals only; a human approves | — |

---

## 6. Words you will see (mini dictionary)

| Word | Plain meaning |
|---|---|
| **Event** | One thing a person does, e.g. "clicked Buy". |
| **Property** | Extra detail about an event, e.g. "price = 20". |
| **User** | One real person using your product. |
| **Account / Workspace** | A company or team (B2B) that has many users. |
| **Metric** | A number that tells us how we are doing, e.g. "signups per day". |
| **Dimension / Segment** | A way to split a number, e.g. by country or device. |
| **Funnel** | Steps people go through, and how many drop off at each step. |
| **Cohort** | A group of users who started in the same week/month. |
| **Retention** | How many people come back later. |
| **Churn** | How many people leave. |
| **Activation** | The moment a new user first gets real value ("aha!"). |
| **North Star Metric** | The ONE number that best shows customers getting value. |
| **Guardrail metric** | A number that must NOT get worse while we improve another. |
| **Dashboard** | A screen with charts that answer questions. |
| **Instrumentation** | Adding tracking so events get recorded. |
| **PII** | Personal info (name, email, phone, exact location). Handle with care. |
| **SLA / Freshness** | How old the data on the dashboard is allowed to be. |

*(Full glossary in Appendix E.)*

---

## 7. 🤖 Instructions for AI agents reading this file

> Humans: you may skip this box.
> 1. Treat this file as the **single source of truth**. Do not use outside assumptions.
> 2. If a field says `TBD` or is empty, **ask a human**; **do not invent** values.
> 3. Only content inside tables and fenced `yaml` blocks is machine-readable. Prose is context.
> 4. Never create an event, metric, or dashboard that is not listed in Sections 6, 8, or 11.
> 5. Full rules are in **Appendix A**.

---

## 8. 🟢 Document status badge (update every time)

| Status | Meaning | Tick one |
|---|---|---|
| Draft | Being written | `[ ]` |
| In Review | Waiting for feedback | `[ ]` |
| Approved | Signed off (Section 22) | `[ ]` |
| Live | Dashboards are built and used | `[ ]` |
| Retired | No longer used | `[ ]` |

---

# TABLE OF CONTENTS

0. Document Control
1. One-Page Summary *(fill last)*
2. Product Context
3. Lifecycle Phase Map (Build → Launch → 500 Customers)
4. Goals and Decisions
5. Audience and Access
6. Metrics (North Star, Input Metrics, Guardrails, Dictionary)
7. Customer Journey and Funnels
8. Tracking Plan (Events and Properties)
9. Identity and Data Rules
10. Data Sources and Pipeline
11. Dashboard Design
12. Alerts and Anomaly Rules
13. Privacy, Consent and Security
14. Data Quality and QA Test Plan
15. Implementation Plan and Responsibilities
16. Rollout and the 500-Customer Milestone Tracker
17. Operations and Maintenance
18. Risks, Assumptions and Open Questions
19. Decision Log
20. Dependencies and Related Documents
21. Change History
22. Approvals and Sign-Off

Appendix A — 🤖 AI-Agent Instructions
Appendix B — 🤖 Machine-Readable Blocks (YAML)
Appendix C — Starter Event Packs (B2C, B2B, Marketplace)
Appendix D — Metric Formula Cheat Sheet
Appendix E — Full Glossary
Appendix F — Final "Ready to Ship" Checklist

---

# 0. 🟢 Document Control

> **Why this matters:** So anybody can tell who owns this file, how fresh it is, and where it lives.

| Field | ✏️ Your answer | Example |
|---|---|---|
| Spec title | `[ANSWER]` | `Acme Planner — Product Analytics Dashboard Spec` |
| Product name | `[ANSWER]` | `Acme Planner` |
| Product type (tick all that apply) | `[ ] B2C app  [ ] B2B SaaS  [ ] Marketplace / e-commerce  [ ] Other: ___` | `[x] B2C app` |
| Platforms | `[ ] Web  [ ] iOS  [ ] Android  [ ] Desktop  [ ] API  [ ] Other: ___` | `[x] Web [x] iOS` |
| Spec version | `[ANSWER]` | `0.1.0` |
| Status | (see badge in "How to fill") | `Draft` |
| Created on | `YYYY-MM-DD` | `2026-10-18` |
| Last updated on | `YYYY-MM-DD` | `2026-10-18` |
| Spec owner (one person) | `[ANSWER]` | `Product Owner — Priya S.` |
| Reviewers | `[ANSWER]` | `Analyst — Sam; Engineer — Lee` |
| Where this file lives | `[ANSWER: link or path]` | `/Product analytics and instrumentation/` |
| Project / Epic link | `[ANSWER: link]` | `PROJ-123` |
| Target launch date | `YYYY-MM-DD` | `2027-02-01` |
| Target date for 500 customers | `YYYY-MM-DD` | `2027-06-30` |
| Language of this spec | `[ANSWER]` | `English` |
| Confidentiality | `[ ] Public  [ ] Internal  [ ] Confidential` | `[x] Internal` |

**✅ Done when**
- [ ] Every row is filled (no empty cells).
- [ ] There is exactly **one** spec owner.
- [ ] The file name is `Product_Analytics_Dashboard_Spec.md` and lives in the "Product analytics and instrumentation" folder.

---

# 1. 🟢 One-Page Summary *(fill this LAST)*

> **Why this matters:** A busy executive should understand the whole plan in 2 minutes.

| Question | ✏️ Your answer |
|---|---|
| 1.1 In one sentence, what is the product? | `[ANSWER]` |
| 1.2 In one sentence, why do we need these dashboards? | `[ANSWER]` |
| 1.3 What is our **North Star Metric**? | `[ANSWER]` |
| 1.4 What are the top 3 decisions these dashboards will help us make? | `1. ___  2. ___  3. ___` |
| 1.5 How many dashboards will we build? | `[ANSWER: number]` |
| 1.6 How many events will we track? | `[ANSWER: number]` |
| 1.7 What is the biggest risk? | `[ANSWER]` |
| 1.8 What do we need from leadership? | `[ANSWER]` |
| 1.9 What does "success" look like at 500 customers? | `[ANSWER]` |

**Example (1.2):** "So that the team can see every week whether new users reach the 'aha' moment and decide where to fix onboarding."

**✅ Done when**
- [ ] A new person can read this section alone and explain the project.
- [ ] Numbers here match Sections 6, 8, and 11.

---

# 2. 🟢 Product Context

> **Why this matters:** Metrics only make sense if we know what the product does and how it makes money.

## 2.1 About the product

| Question | ✏️ Your answer | Example |
|---|---|---|
| 2.1.1 What does the product do? (2–3 sentences) | `[ANSWER]` | "Acme Planner helps freelancers plan their week and send invoices." |
| 2.1.2 Who is it for? (the main customer) | `[ANSWER]` | "Freelance designers in the US." |
| 2.1.3 What problem do we solve for them? | `[ANSWER]` | "They lose track of tasks and get paid late." |
| 2.1.4 How do customers find us? (tick all) | `[ ] Search  [ ] Social  [ ] Ads  [ ] Referral  [ ] Sales team  [ ] App store  [ ] Partners  [ ] Other: ___` | `[x] Search [x] Referral` |
| 2.1.5 How does the product make money? | `[ ] Free  [ ] Freemium  [ ] Subscription  [ ] One-time purchase  [ ] Usage-based  [ ] Commission (marketplace)  [ ] Ads  [ ] Other: ___` | `[x] Freemium [x] Subscription` |
| 2.1.6 What are the price plans? | `[ANSWER]` | "Free, Pro $12/mo, Team $29/mo." |
| 2.1.7 Is there a free trial? How long? | `[ANSWER]` | "14 days, no card needed." |

## 2.2 What counts as a "customer"? ⚠️ *Very important — define it exactly.*

| Question | ✏️ Your answer | Example |
|---|---|---|
| 2.2.1 What is a **user**? | `[ANSWER]` | "A person with a verified email who has logged in once." |
| 2.2.2 What is a **customer** for the "500 customers" goal? | `[ANSWER]` | "A person or team who paid at least once, OR (free product) reached Activation." |
| 2.2.3 Does one customer have many users? (B2B) | `[ ] Yes  [ ] No` | `[x] Yes — a workspace has many users` |
| 2.2.4 What is an **account / workspace / seller / buyer**? | `[ANSWER]` | "A workspace = one company." |
| 2.2.5 What counts as **active**? (the exact action + time window) | `[ANSWER]` | "Created or completed at least 1 task in the last 7 days." |
| 2.2.6 What counts as **churned**? | `[ANSWER]` | "No active days for 30 days, or subscription cancelled." |
| 2.2.7 Who do we **exclude** from all numbers? | `[ANSWER]` | "Internal staff, test accounts, bots." |

## 2.3 Product-type questions (answer the ones for your product type)

**If B2C app**
| Question | ✏️ Your answer |
|---|---|
| Do users sign up before using the product? | `[ANSWER]` |
| Is there a mobile app AND a website? How do we know it is the same person? | `[ANSWER]` |
| Which "habit" do we want users to form (daily/weekly)? | `[ANSWER]` |

**If B2B SaaS**
| Question | ✏️ Your answer |
|---|---|
| What is the buying process (self-serve, sales-led, both)? | `[ANSWER]` |
| Who are the roles (admin, member, viewer, billing owner)? | `[ANSWER]` |
| What is the unit of billing (seat, usage, flat)? | `[ANSWER]` |
| What is the expansion path (more seats, higher plan)? | `[ANSWER]` |

**If marketplace / e-commerce**
| Question | ✏️ Your answer |
|---|---|
| Who are the two (or more) sides (buyers / sellers / drivers…)? | `[ANSWER]` |
| What is a "successful transaction"? | `[ANSWER]` |
| How do we make money (commission %, fees, ads)? | `[ANSWER]` |
| What is "supply" and what is "demand"? Which is harder to get? | `[ANSWER]` |

## 2.4 Current situation

| Question | ✏️ Your answer |
|---|---|
| 2.4.1 Do we already track anything today? What and with which tool? | `[ANSWER]` |
| 2.4.2 Do we have a past dashboard we are replacing? Link it. | `[ANSWER]` |
| 2.4.3 What is broken or missing today? | `[ANSWER]` |
| 2.4.4 How many users do we have today? | `[ANSWER: number]` |

**✅ Done when**
- [ ] "Customer", "active" and "churned" are defined with numbers and time windows.
- [ ] Internal/test users are listed as excluded.
- [ ] The business model is clear to a new reader.

---

# 3. 🟢 Lifecycle Phase Map (Build → Launch → First 500 Customers)

> **Why this matters:** What you measure changes as the product grows. In week 1 you check "does it work?". At 500 customers you check "do they stay and pay?". This map prevents building dashboards too early or too late.

## 3.1 The phases

| Phase | Name | What is happening | Main question | Typical dashboard |
|---|---|---|---|---|
| P0 | **Plan** | Writing this spec, choosing tools | "What must we know?" | None yet |
| P1 | **Build** | AI-assisted development; tracking code is written | "Is tracking implemented correctly?" | Instrumentation Health |
| P2 | **Test (Pre-launch)** | QA, internal / friends & family use | "Do events fire and numbers add up?" | QA / Data Quality |
| P3 | **Launch** | Product goes public (soft or hard launch) | "Are people arriving and getting in?" | Launch Command Center |
| P4 | **Early users (1–50 customers)** | First real users; talk to everyone | "Do early users get value?" | Activation & Funnel |
| P5 | **Growing (51–250 customers)** | Patterns appear | "What brings them back?" | Retention & Engagement |
| P6 | **Scaling to 500 (251–500 customers)** | Repeatable growth | "Is this working, and what to fix first?" | Executive Scorecard + Revenue |

### ✏️ Fill in your dates

| Phase | Start date | End date | Owner | Exit rule (what must be true to move on) |
|---|---|---|---|---|
| P0 Plan | `YYYY-MM-DD` | `YYYY-MM-DD` | `[ANSWER]` | This spec approved (Section 22) |
| P1 Build | `YYYY-MM-DD` | `YYYY-MM-DD` | `[ANSWER]` | All 🟢 events implemented in staging |
| P2 Test | `YYYY-MM-DD` | `YYYY-MM-DD` | `[ANSWER]` | QA test plan (Section 14) 100% passed |
| P3 Launch | `YYYY-MM-DD` | `YYYY-MM-DD` | `[ANSWER]` | `[ANSWER: e.g. 100 signups and 0 critical bugs]` |
| P4 Early (1–50) | `YYYY-MM-DD` | `YYYY-MM-DD` | `[ANSWER]` | 50 customers reached |
| P5 Growing (51–250) | `YYYY-MM-DD` | `YYYY-MM-DD` | `[ANSWER]` | 250 customers reached |
| P6 Scaling (251–500) | `YYYY-MM-DD` | `YYYY-MM-DD` | `[ANSWER]` | 500 customers reached |

## 3.2 What do we measure in each phase?

> 💡 Tick what applies. Use Section 6 metric IDs (e.g. `M-003`).

| Phase | Metrics we watch (IDs) | Dashboards we use (IDs) | Review rhythm |
|---|---|---|---|
| P1 Build | `[ANSWER]` e.g. event coverage | `[ANSWER]` e.g. `D-001` | Daily (dev stand-up) |
| P2 Test | `[ANSWER]` e.g. event pass rate, duplicate rate | `[ANSWER]` | Daily |
| P3 Launch | `[ANSWER]` e.g. visits, signups, errors | `[ANSWER]` | Daily |
| P4 Early | `[ANSWER]` e.g. activation, time-to-value | `[ANSWER]` | Daily → Weekly |
| P5 Growing | `[ANSWER]` e.g. W1/W4 retention, engagement | `[ANSWER]` | Weekly |
| P6 Scaling | `[ANSWER]` e.g. conversion to paid, churn, revenue | `[ANSWER]` | Weekly + Monthly |

## 3.3 AI-driven development steps for analytics 🤖

> This shows where AI helps at each stage. A **human must approve** each output.

| Step | What AI may do | What the human must do | Output | Done? |
|---|---|---|---|---|
| 1. Spec | Review this spec for gaps, contradictions, vague words | Answer the questions it raises | Gap report | `[ ]` |
| 2. Event design | Propose event names/properties from the journey in Section 7 | Approve the final list | Section 8 filled | `[ ]` |
| 3. Code | Generate tracking code / SDK calls from Section 8 and Appendix B | Review code, run it in staging | Pull request | `[ ]` |
| 4. Tests | Generate test cases from Section 14 | Run them and record results | Test report | `[ ]` |
| 5. Dashboards | Draft queries and chart configs from Section 11 | Verify numbers against raw data | Live dashboards | `[ ]` |
| 6. Monitoring | Draft alert rules from Section 12 | Approve thresholds and owners | Alert list | `[ ]` |
| 7. Weekly review | Summarize changes and anomalies | Decide actions | Weekly note (Section 16) | `[ ]` |

**✅ Done when**
- [ ] Every phase has dates, an owner, and an exit rule.
- [ ] Every phase has at least one metric and one dashboard (or `N/A — because …`).
- [ ] The word "customer" here matches Section 2.2.2.

---

# 4. 🟢 Goals and Decisions

> **Why this matters:** A dashboard without a decision is just wall art. Start with the *decisions*, then work backwards to the numbers.

## 4.1 Business goals

| ID | Goal (plain words) | Number target | By when | Owner |
|---|---|---|---|---|
| G-001 | `[ANSWER]` | `[ANSWER]` | `YYYY-MM-DD` | `[ANSWER]` |
| G-002 | `[ANSWER]` | `[ANSWER]` | `YYYY-MM-DD` | `[ANSWER]` |
| G-003 | `[ANSWER]` | `[ANSWER]` | `YYYY-MM-DD` | `[ANSWER]` |

**Example:** `G-001 | Get 500 paying customers | 500 customers | 2027-06-30 | CEO`

## 4.2 Questions the dashboards must answer

> ⚠️ Write real questions that end with a "?". Aim for 8–20 questions.

| ID | Question | Who asks it | How often | Which decision does the answer change? | Priority |
|---|---|---|---|---|---|
| Q-001 | `[ANSWER]` | `[ANSWER]` | `Daily / Weekly / Monthly` | `[ANSWER]` | `High / Med / Low` |
| Q-002 | | | | | |
| Q-003 | | | | | |
| Q-004 | | | | | |
| Q-005 | | | | | |
| Q-006 | | | | | |
| Q-007 | | | | | |
| Q-008 | | | | | |

**Example:** `Q-001 | Where do new users quit during onboarding? | Product Owner | Weekly | Which onboarding step to redesign next | High`

## 4.3 Decision list

| ID | Decision we will make | Which metric(s) trigger it | Rule ("if X then Y") | Who decides |
|---|---|---|---|---|
| DEC-A | `[ANSWER]` | `M-___` | `[ANSWER]` | `[ANSWER]` |
| DEC-B | | | | |
| DEC-C | | | | |

**Example:** `DEC-A | Pause paid ads | M-012 Cost per Activated User | If > $40 for 7 days in a row, pause and review | Marketing Lead`

## 4.4 What we will NOT measure (non-goals)

| Item | Reason |
|---|---|
| `[ANSWER]` | `[ANSWER]` |

**Example:** "Heatmaps and session recordings — not needed until 1,000 users."

**✅ Done when**
- [ ] Each question links to a decision.
- [ ] No question is "nice to know" only (or it is marked Low).
- [ ] Non-goals are listed, so scope does not grow silently.

---

# 5. 🟢 Audience and Access

> **Why this matters:** The CEO, a developer, and a support agent need different screens and different permissions.

## 5.1 Who uses the dashboards?

| Persona | Role | What they need | How often | Skill level with data | Dashboards they use |
|---|---|---|---|---|---|
| `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `Beginner / Intermediate / Expert` | `D-___` |
| Example: Founder | CEO | "Are we on track?" | Weekly | Beginner | `D-010` |
| Example: Growth PM | PM | "Where do users drop?" | Daily | Intermediate | `D-003, D-004` |

## 5.2 Access and sharing

| Question | ✏️ Your answer |
|---|---|
| 5.2.1 Who can **view** dashboards? | `[ANSWER]` |
| 5.2.2 Who can **edit** dashboards? | `[ANSWER]` |
| 5.2.3 Who can see **raw user-level data**? (should be very few) | `[ANSWER]` |
| 5.2.4 Can dashboards be shared outside the company (investors, partners)? | `[ ] Yes  [ ] No — if yes, how: ___` |
| 5.2.5 How are access requests handled? | `[ANSWER]` |
| 5.2.6 How often do we review who has access? | `[ ] Monthly  [ ] Quarterly  [ ] Yearly` |

**✅ Done when**
- [ ] Every dashboard in Section 11 has at least one named audience.
- [ ] Access rules follow "least access needed" (Section 13).

---

# 6. 🟢 Metrics

> **Why this matters:** Metrics are the numbers everyone will trust — or argue about. Define each one *once*, here.

## 6.1 North Star Metric (the ONE number)

| Question | ✏️ Your answer | Example |
|---|---|---|
| 6.1.1 North Star name | `[ANSWER]` | `Weekly Active Planners` |
| 6.1.2 Plain meaning | `[ANSWER]` | "People who planned at least 3 tasks in a week." |
| 6.1.3 Why does it show customer value? | `[ANSWER]` | "Planning regularly means they rely on us." |
| 6.1.4 Formula | `[ANSWER]` | `count(distinct user_id with ≥3 task_created in 7 days)` |
| 6.1.5 Target at 500 customers | `[ANSWER]` | `≥ 350 weekly active planners` |
| 6.1.6 Why NOT revenue alone? | `[ANSWER]` | "Revenue lags; this predicts it." |

> ⚠️ A good North Star measures **value delivered to the customer**, goes **up when the business is healthier**, and is **something the team can influence**.

## 6.2 Metric tree (how small numbers add up to the big one)

```
North Star: [Name]
├── Input 1: [Name]  (e.g. New users activated)
│   ├── Sub-input: [Name]  (e.g. Signup conversion)
│   └── Sub-input: [Name]  (e.g. Onboarding completion)
├── Input 2: [Name]  (e.g. Returning users)
│   └── Sub-input: [Name]  (e.g. Week-4 retention)
└── Input 3: [Name]  (e.g. Depth of use)
    └── Sub-input: [Name]  (e.g. Key actions per active user)
```

✏️ **Redraw this tree for your product:**

```
[PASTE YOUR TREE HERE]
```

## 6.3 Metric categories to cover (tick what you will use)

| Category | Plain question | Use? | Starter metrics (pick or replace) |
|---|---|---|---|
| **Acquisition** | How do people find us? | `[ ]` | Visitors, signups, signup conversion, cost per signup, traffic by source |
| **Activation** | Do they get the "aha" quickly? | `[ ]` | Activation rate, time to first value, onboarding completion |
| **Engagement** | Do they use it often and deeply? | `[ ]` | DAU/WAU/MAU, stickiness (DAU/MAU), feature adoption, sessions per user |
| **Retention** | Do they come back? | `[ ]` | Day-1/7/30 retention, weekly cohort retention, resurrection rate |
| **Revenue** | Do they pay? | `[ ]` | Trial→paid, MRR/ARR, ARPU/ARPA, LTV, expansion, refunds |
| **Referral** | Do they bring friends? | `[ ]` | Invites sent, invite acceptance, viral coefficient, NPS |
| **Quality / Health** | Does it work and feel good? | `[ ]` | Error rate, load time, crash-free sessions, support tickets |
| **Marketplace** (if used) | Is supply meeting demand? | `[ ]` | Liquidity, GMV, take rate, time to first transaction, repeat rate by side |
| **B2B** (if used) | Do accounts grow? | `[ ]` | Seats activated, accounts activated, net revenue retention, logo churn |
| **Data health** | Can we trust the numbers? | `[ ]` | Event coverage, duplicates, nulls, freshness |

## 6.4 Guardrail metrics (numbers that must NOT get worse)

| ID | Guardrail | Limit | Why | Owner |
|---|---|---|---|---|
| GR-001 | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` |
| GR-002 | | | | |

**Example:** `GR-001 | App crash-free rate | Must stay ≥ 99.5% | Growth must not break quality | Engineering Lead`

## 6.5 📖 Metric Dictionary *(the most important table in this file)*

> **How to fill:** Copy the block below once for **each** metric. Give each metric an ID `M-001`, `M-002`, …
> ⚠️ If the formula could be read two ways, rewrite it. Show numerator and denominator separately.

### Metric block template

| Field | ✏️ Your answer | Example |
|---|---|---|
| **Metric ID** | `M-001` | `M-003` |
| **Name** | `[ANSWER]` | `Activation Rate` |
| **Category** | `Acquisition / Activation / Engagement / Retention / Revenue / Referral / Quality / Marketplace / B2B / Data health` | `Activation` |
| **Phase(s) it matters** | `P3, P4…` | `P3–P6` |
| **Plain-words definition** | `[ANSWER]` | "Out of new signups, how many reach their first real success quickly." |
| **Formula** | `[ANSWER]` | `activated_users / new_signups` |
| **Numerator** | `[ANSWER]` | "Users with `first_plan_completed` within 24h of `signup_completed`" |
| **Denominator** | `[ANSWER]` | "Users with `signup_completed` in the period" |
| **Unit** | `% / count / currency / seconds / ratio` | `%` |
| **Source events** | `[Event IDs from Section 8]` | `E-002, E-014` |
| **Time window** | `[ANSWER]` | "Within 24h of signup, grouped by signup day" |
| **Counted per** | `User / Account / Session / Order` | `User` |
| **Filters / exclusions** | `[ANSWER]` | "Exclude internal & test users" |
| **Can be split by (segments)** | `[ANSWER]` | `Platform, Country, Acquisition source, Plan` |
| **Good direction** | `Higher is better / Lower is better / Stay in range` | `Higher` |
| **Target (per phase)** | `P4: __ , P5: __ , P6: __` | `P4: 30%, P5: 38%, P6: 45%` |
| **Owner** | `[ANSWER]` | `Growth PM` |
| **Refresh** | `Real-time / Hourly / Daily / Weekly` | `Daily` |
| **Where it is shown** | `[Dashboard IDs]` | `D-003, D-010` |
| **Known caveats** | `[ANSWER]` | "Not reliable if user blocks tracking." |
| **Status** | `Proposed / Approved / Live / Retired` | `Approved` |

### ✏️ Your metrics (copy the block above for each; or fill this summary table and keep details in Appendix B)

| ID | Name | Category | Formula (short) | Unit | Owner | Target P6 | Status |
|---|---|---|---|---|---|---|---|
| M-001 | `[North Star]` | | | | | | |
| M-002 | | | | | | | |
| M-003 | | | | | | | |
| M-004 | | | | | | | |
| M-005 | | | | | | | |
| M-006 | | | | | | | |
| M-007 | | | | | | | |
| M-008 | | | | | | | |
| M-009 | | | | | | | |
| M-010 | | | | | | | |

## 6.6 Targets: how did we choose the numbers?

| Question | ✏️ Your answer |
|---|---|
| 6.6.1 Where did the targets come from (benchmarks, past data, guess)? | `[ANSWER]` |
| 6.6.2 How sure are we (High / Medium / Low)? | `[ANSWER]` |
| 6.6.3 When will we re-check targets? | `[ANSWER: date]` |

💡 If you have no data yet, write "initial guess" and plan to reset targets after the first 50 customers (P4 exit).

## 6.7 Small-number warning (important for the first 500 customers)

> With few users, percentages jump wildly (1 person = 10% when you have 10 users). Fill this in so nobody over-reacts.

| Question | ✏️ Your answer | Example |
|---|---|---|
| 6.7.1 Below how many users do we show **counts** instead of **percentages**? | `[ANSWER]` | "Below 30 users, show counts." |
| 6.7.2 Minimum sample before we act on a change | `[ANSWER]` | "At least 50 users in each compared group." |
| 6.7.3 Do we show confidence ranges? | `[ ] Yes  [ ] No` | `[x] Yes` |
| 6.7.4 How do we read individual user sessions/feedback in early phases? | `[ANSWER]` | "Review every new customer manually until P5." |

**✅ Done when**
- [ ] North Star has name, formula, and target.
- [ ] Every metric has an owner, formula, numerator, denominator, source events, and target.
- [ ] Every source event exists in Section 8.
- [ ] At least 2 guardrails exist.
- [ ] Small-number rules are written.

---

# 7. 🟢 Customer Journey and Funnels

> **Why this matters:** The journey tells us *which events must exist*. Draw the path a customer takes from "never heard of us" to "happy paying customer".

## 7.1 The journey (fill each stage)

| Stage | What does the person do? | What does success look like? | Event(s) that prove it (IDs) | Possible drop-off reason |
|---|---|---|---|---|
| 1. Discover | `[ANSWER]` | `[ANSWER]` | `E-___` | `[ANSWER]` |
| 2. Visit / Install | | | | |
| 3. Sign up | | | | |
| 4. Onboard | | | | |
| 5. **Activate (aha!)** | | | | |
| 6. Use regularly | | | | |
| 7. Pay / Transact | | | | |
| 8. Expand / Refer | | | | |
| 9. Get help | | | | |
| 10. Leave / Cancel | | | | |

## 7.2 Activation: define the "aha" moment 🟢

| Question | ✏️ Your answer | Example |
|---|---|---|
| 7.2.1 What is the **first moment** a new user gets real value? | `[ANSWER]` | "Completes their first weekly plan." |
| 7.2.2 Which event(s) mean "activated"? | `[ANSWER]` | `first_plan_completed (E-014)` |
| 7.2.3 How fast should it happen? | `[ANSWER]` | "Within 24 hours of signup." |
| 7.2.4 How do we know this action predicts staying? | `[ ] Data  [ ] Interviews  [ ] Guess — we will test at P4` | `[x] Guess` |
| 7.2.5 (B2B) What makes an **account** activated? | `[ANSWER]` | "3+ users invited and 1 project created." |
| 7.2.6 (Marketplace) What makes a **buyer/seller** activated? | `[ANSWER]` | "Seller lists 3 items; buyer views 5 and saves 1." |

## 7.3 Funnel definitions

> **How to fill:** One block per funnel. List the steps in order, with the event for each.

| Funnel ID | Name | Start event | End event | Max time to finish | Counted per | Segments to compare |
|---|---|---|---|---|---|---|
| F-001 | `[ANSWER]` | `E-___` | `E-___` | `[ANSWER]` | `User / Session / Account` | `[ANSWER]` |
| F-002 | | | | | | |
| F-003 | | | | | | |

**Example F-001 — Signup funnel:** `landing_page_viewed → signup_started → signup_completed → email_verified → onboarding_completed → first_plan_completed`

### ✏️ Steps of each funnel

| Funnel | Step # | Step name | Event ID | Required properties | Must happen in order? |
|---|---|---|---|---|---|
| F-001 | 1 | `[ANSWER]` | `E-___` | `[ANSWER]` | `Yes / No` |
| F-001 | 2 | | | | |
| F-001 | 3 | | | | |
| F-001 | 4 | | | | |
| F-002 | 1 | | | | |
| F-002 | 2 | | | | |

## 7.4 Retention definition

| Question | ✏️ Your answer | Example |
|---|---|---|
| 7.4.1 Which action means a user "came back"? | `[ANSWER]` | "Any `plan_created` or `task_completed`." |
| 7.4.2 Which retention type? | `[ ] Classic (exact day)  [ ] Range (on/after day)  [ ] Rolling` | `[x] Classic` |
| 7.4.3 Which days/weeks do we track? | `[ANSWER]` | `D1, D7, D30; W1–W8` |
| 7.4.4 How do we group users into cohorts? | `[ ] Signup week  [ ] Signup month  [ ] Plan  [ ] Source` | `[x] Signup week` |
| 7.4.5 How long without activity = "lapsed"? | `[ANSWER]` | `14 days` |

## 7.5 Revenue path (if you earn money)

| Question | ✏️ Your answer |
|---|---|
| 7.5.1 Where does a user hit the paywall / upgrade prompt? | `[ANSWER]` |
| 7.5.2 Events for: trial start, upgrade, payment success, payment failure, cancel, refund | `[Event IDs]` |
| 7.5.3 How do we count revenue (gross, net of refunds, recognized)? | `[ANSWER]` |
| 7.5.4 Which currency is the reporting currency? | `[ANSWER]` |
| 7.5.5 Where is the "source of truth" for money (payment tool or our database)? | `[ANSWER]` |

**✅ Done when**
- [ ] Each journey stage has at least one event.
- [ ] "Activated" has a clear event and time window.
- [ ] Every funnel step maps to a real event ID in Section 8.

---

# 8. 🟢 Tracking Plan (Events and Properties)

> **Why this matters:** If an event is not tracked, it never happened as far as the dashboard knows. This section is the contract between product, engineering, and analytics.

## 8.1 Naming rules (set once; follow always)

| Rule | ✏️ Your choice | Recommended default |
|---|---|---|
| Event name style | `[ANSWER]` | `snake_case`, **object_action** in past tense (e.g. `task_created`) |
| Property name style | `[ANSWER]` | `snake_case` (e.g. `plan_type`) |
| Language of names | `[ANSWER]` | English only |
| Max name length | `[ANSWER]` | 40 characters |
| Allowed characters | `[ANSWER]` | a–z, 0–9, underscore |
| Forbidden | `[ANSWER]` | spaces, emojis, personal data, dynamic text in event names |
| Boolean properties start with | `[ANSWER]` | `is_` / `has_` |
| Date/time format | `[ANSWER]` | ISO 8601 UTC, e.g. `2026-10-18T14:30:00Z` |
| Money format | `[ANSWER]` | Amount as number in smallest unit + separate `currency` (e.g. `1200` + `USD`) |
| Who can add a new event? | `[ANSWER]` | Only after review by the Data Lead |

⚠️ **Never** put a value in the event name (bad: `clicked_button_blue`; good: `button_clicked` with property `color = blue`).

## 8.2 Global properties (sent with EVERY event)

| Property | Type | Required? | Example value | Why we need it |
|---|---|---|---|---|
| `event_id` | string (unique) | 🟢 | `8f1c…` | Remove duplicates |
| `event_time` | timestamp UTC | 🟢 | `2026-10-18T14:30:00Z` | When it happened |
| `user_id` | string | 🟢 (when known) | `u_48213` | Who did it |
| `anonymous_id` | string | 🟢 | `a_7c3d…` | Who did it before login |
| `session_id` | string | 🟢 | `s_9921` | Group actions |
| `account_id` (B2B) | string | 🟡 | `acc_77` | Which company |
| `platform` | enum | 🟢 | `web / ios / android / api` | Split by device |
| `app_version` | string | 🟢 | `2.3.1` | Find bugs by version |
| `environment` | enum | 🟢 | `production / staging / dev` | Keep test data out |
| `country` | ISO code | 🟡 | `US` | Segment |
| `locale / language` | string | 🟡 | `en-US` | Segment |
| `acquisition_source` | string | 🟡 | `google_organic` | Marketing |
| `experiment_variants` | map | 🔵 | `{"onb_v2":"B"}` | A/B tests |

✏️ **Add or remove rows for your product:**

| Property | Type | Required? | Example | Why |
|---|---|---|---|---|
| `[ANSWER]` | | | | |

## 8.3 User properties (facts about the person that change rarely)

| Property | Type | Example | Contains PII? | Required? | Why |
|---|---|---|---|---|---|
| `signup_date` | date | `2026-10-18` | No | 🟢 | Cohorts |
| `plan_type` | enum | `free/pro/team` | No | 🟢 | Segment |
| `user_role` | enum | `admin/member` | No | 🟡 | B2B roles |
| `signup_source` | string | `referral` | No | 🟡 | Marketing |
| `[ANSWER]` | | | | | |

## 8.4 Account / group properties (B2B and marketplace)

| Property | Type | Example | PII? | Required? | Why |
|---|---|---|---|---|---|
| `account_created_date` | date | `2026-10-20` | No | 🟢 | Cohorts |
| `seats_purchased` | number | `12` | No | 🟡 | Expansion |
| `industry` | enum | `design` | No | 🔵 | Segment |
| `company_size_band` | enum | `11-50` | No | 🔵 | Segment |
| `seller_tier` / `buyer_type` | enum | `verified` | No | 🟡 | Marketplace |
| `[ANSWER]` | | | | | |

## 8.5 📋 THE EVENT LIST (the heart of this section)

> **How to fill:** One row per event. Use the starter packs in **Appendix C** to save time; delete what you do not need and add what is missing.
> **Priority:** 🟢 Must have for launch · 🟡 Should have by P5 · 🔵 Nice to have.
> **Where fired:** `client` (app/browser) or `server` (backend). 💡 Money and signup events should be **server-side** (more trustworthy).

| ID | Event name | Plain description (when exactly does it fire?) | Where fired | Priority | Properties (name:type) | Linked metrics | Owner | Phase live | Status |
|---|---|---|---|---|---|---|---|---|---|
| E-001 | `[object_action]` | `[ANSWER]` | `client/server` | 🟢 | `[ANSWER]` | `M-___` | `[ANSWER]` | `P3` | `Planned` |
| E-002 | | | | | | | | | |
| E-003 | | | | | | | | | |
| E-004 | | | | | | | | | |
| E-005 | | | | | | | | | |
| E-006 | | | | | | | | | |
| E-007 | | | | | | | | | |
| E-008 | | | | | | | | | |
| E-009 | | | | | | | | | |
| E-010 | | | | | | | | | |
| E-011 | | | | | | | | | |
| E-012 | | | | | | | | | |
| E-013 | | | | | | | | | |
| E-014 | | | | | | | | | |
| E-015 | | | | | | | | | |

**Example row:**
`E-014 | first_plan_completed | Fires once, the first time a user marks all tasks of a weekly plan as done | server | 🟢 | plan_id:string, task_count:int, minutes_since_signup:int | M-003 | Engineer — Lee | P3 | Planned`

### Status values
`Planned → In Progress → In Staging → Verified → Live → Deprecated`

## 8.6 Detail block for tricky events 🟡

> Use for events with rules like "fire only once", "fire after payment success", etc.

| Field | ✏️ Your answer | Example |
|---|---|---|
| Event ID / name | `[ANSWER]` | `E-020 payment_succeeded` |
| Exact trigger (what must be true) | `[ANSWER]` | "Payment provider confirms charge success (webhook)" |
| What must NOT trigger it | `[ANSWER]` | "Pending, failed, or test-mode payments" |
| Fires once per… | `[ANSWER]` | "Per invoice" |
| Required properties | `[ANSWER]` | `invoice_id, amount, currency, plan_type` |
| Example payload (JSON) | `[ANSWER]` | see below |
| Edge cases | `[ANSWER]` | "Refund → `payment_refunded` instead; retries must reuse same `event_id`" |

```json
{
  "event": "payment_succeeded",
  "event_id": "evt_01H...",
  "event_time": "2026-10-18T14:30:00Z",
  "user_id": "u_48213",
  "account_id": "acc_77",
  "properties": {
    "invoice_id": "inv_555",
    "amount": 1200,
    "currency": "USD",
    "plan_type": "pro"
  }
}
```

## 8.7 Property dictionary (allowed values)

| Property | Type | Allowed values / format | Required in events | Notes |
|---|---|---|---|---|
| `platform` | enum | `web, ios, android, api` | all | |
| `plan_type` | enum | `[ANSWER]` | `E-___` | |
| `[ANSWER]` | | | | |

## 8.8 Events we deliberately do NOT track

| Item | Reason |
|---|---|
| Every mouse move / scroll | Too noisy and costly |
| Free-text typed by users | May hold personal data |
| `[ANSWER]` | `[ANSWER]` |

## 8.9 Coverage check (fill after listing events)

| Journey stage (Section 7.1) | Number of events | At least one 🟢 event? |
|---|---|---|
| Discover | `[#]` | `[ ]` |
| Visit / Install | `[#]` | `[ ]` |
| Sign up | `[#]` | `[ ]` |
| Onboard | `[#]` | `[ ]` |
| Activate | `[#]` | `[ ]` |
| Use regularly | `[#]` | `[ ]` |
| Pay / Transact | `[#]` | `[ ]` |
| Expand / Refer | `[#]` | `[ ]` |
| Get help | `[#]` | `[ ]` |
| Leave / Cancel | `[#]` | `[ ]` |

**✅ Done when**
- [ ] Naming rules are chosen and applied to every event.
- [ ] Every metric's source event exists here, and every event serves at least one metric/funnel (or is marked 🔵).
- [ ] Each event has an exact trigger described in plain words.
- [ ] Money, signup, and account events are fired from the **server**.
- [ ] No event or property holds personal data unless approved in Section 13.
- [ ] Coverage check has no empty stage.

---

# 9. 🟢 Identity and Data Rules

> **Why this matters:** If the same person looks like 3 people, every number is wrong.

## 9.1 Identity

| Question | ✏️ Your answer | Example |
|---|---|---|
| 9.1.1 What is the **permanent user ID**? | `[ANSWER]` | "Database UUID, never the email." |
| 9.1.2 How do we track people **before** login? | `[ANSWER]` | "Anonymous ID in cookie / device storage." |
| 9.1.3 When do we **link** anonymous → known user? | `[ANSWER]` | "At `signup_completed` and `login_succeeded`." |
| 9.1.4 What if one person uses web **and** mobile? | `[ANSWER]` | "Same `user_id` after login." |
| 9.1.5 What if two people share one device? | `[ANSWER]` | "New `anonymous_id` at logout." |
| 9.1.6 (B2B) How do users link to accounts? Can a user be in 2 accounts? | `[ANSWER]` | "Yes; `account_id` on each event." |
| 9.1.7 What happens when a user deletes their account? | `[ANSWER]` | "Events anonymized within 30 days." |

## 9.2 Sessions, time, and money

| Question | ✏️ Your answer | Example |
|---|---|---|
| 9.2.1 What is a **session**? | `[ANSWER]` | "Activity with no gap longer than 30 minutes." |
| 9.2.2 Which **time zone** do dashboards use? | `[ANSWER]` | "UTC for storage; viewers can switch." |
| 9.2.3 When does a "day" / "week" start? | `[ANSWER]` | "Week starts Monday, 00:00 UTC." |
| 9.2.4 How are late events handled (arrive after the day ended)? | `[ANSWER]` | "Accepted up to 7 days late; numbers restate." |
| 9.2.5 Reporting currency and exchange-rate rule | `[ANSWER]` | "USD; daily rate from payment provider." |
| 9.2.6 Is revenue shown with tax? | `[ ] With tax  [ ] Without tax` | `[x] Without tax` |

## 9.3 Internal and test traffic

| Question | ✏️ Your answer |
|---|---|
| 9.3.1 How do we identify team members / test accounts? | `[ANSWER]` |
| 9.3.2 How do we block bots? | `[ANSWER]` |
| 9.3.3 Do staging/dev events go to the same project as production? | `[ ] No (recommended)  [ ] Yes — because ___` |

## 9.4 Duplicates and missing data

| Question | ✏️ Your answer |
|---|---|
| 9.4.1 How are duplicate events removed? | `[ANSWER: e.g. by event_id]` |
| 9.4.2 What happens when an ad-blocker/offline user blocks events? | `[ANSWER]` |
| 9.4.3 Expected % of missing events we accept | `[ANSWER]` |
| 9.4.4 Can we **backfill** (re-send old data) if tracking breaks? | `[ ] Yes  [ ] No` |

**✅ Done when**
- [ ] One permanent user ID is chosen and is not an email/phone.
- [ ] The anonymous → known link moment is defined.
- [ ] Internal/test traffic can be filtered out on every dashboard.
- [ ] Time zone, week start, and currency are written down.

---

# 10. 🟢 Data Sources and Pipeline

> **Why this matters:** Shows where data comes from, where it is stored, and how it reaches the dashboard.

## 10.1 Tool list

| Purpose | Tool name | Owner | Cost / month | Contract end | Notes |
|---|---|---|---|---|---|
| Event collection (SDK) | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | | |
| Product analytics UI | `[ANSWER]` | | | | |
| Data warehouse / database | `[ANSWER]` | | | | |
| Dashboard / BI tool | `[ANSWER]` | | | | |
| Payments | `[ANSWER]` | | | | |
| Marketing / ads | `[ANSWER]` | | | | |
| CRM / support | `[ANSWER]` | | | | |
| Error / performance monitoring | `[ANSWER]` | | | | |
| Feature flags / A/B tests | `[ANSWER]` | | | | |

## 10.2 Data flow (draw it in words or arrows)

```
[Product app/web] → [Tracking SDK / API] → [Collector] → [Storage / warehouse] → [Transform / models] → [Dashboard tool] → [People + Alerts]
```

✏️ **Redraw for your product (include every extra source such as payments, CRM, ads):**

```
[PASTE YOUR FLOW HERE]
```

## 10.3 Source inventory

| Source ID | Source | What it gives us | How data arrives (SDK / API / export / webhook) | Refresh | Owner | Source of truth for… |
|---|---|---|---|---|---|---|
| S-001 | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` |
| S-002 | | | | | | |
| S-003 | | | | | | |

## 10.4 Service levels

| Question | ✏️ Your answer | Example |
|---|---|---|
| 10.4.1 Max age of data on dashboards (freshness) | `[ANSWER]` | "Launch dashboard: 15 min. Others: 24h." |
| 10.4.2 How long do we keep raw events? | `[ANSWER]` | "25 months." |
| 10.4.3 How long do we keep aggregated numbers? | `[ANSWER]` | "Forever (no PII)." |
| 10.4.4 Expected events per day at 500 customers | `[ANSWER]` | "~200,000" |
| 10.4.5 Budget limit for analytics tools | `[ANSWER]` | "$500 / month" |
| 10.4.6 What happens if the tool goes down? | `[ANSWER]` | "Queue events locally and retry." |

## 10.5 Environments

| Environment | Purpose | Where data goes | Who can access |
|---|---|---|---|
| Development | Engineers test code | Separate project / key | Engineers |
| Staging | QA tests (Section 14) | Separate project / key | Eng + QA |
| Production | Real customers | Production project | Per Section 5 |

**✅ Done when**
- [ ] Each metric traces back to a source in 10.3.
- [ ] Freshness is stated for each dashboard.
- [ ] Dev/staging data cannot mix into production.
- [ ] Retention period is written down.

---

# 11. 🟢 Dashboard Design

> **Why this matters:** This is what people actually look at. Design for the *question*, not for decoration.

## 11.1 Design rules (set once)

| Rule | ✏️ Your choice | Recommended default |
|---|---|---|
| Max charts per dashboard | `[ANSWER]` | 8–12 |
| Top row shows | `[ANSWER]` | 3–5 "big numbers" (KPIs) with change vs. last period |
| Default date range | `[ANSWER]` | Last 30 days (Launch: last 24h) |
| Compare to | `[ANSWER]` | Previous period |
| Global filters | `[ANSWER]` | Date, platform, country, plan, source, "exclude internal" |
| Colors | `[ANSWER]` | Max 6; same meaning everywhere (green=good, red=bad) |
| Accessibility | `[ANSWER]` | Do not rely on color alone; readable labels |
| Naming | `[ANSWER]` | `[Team] – [Purpose] – [Audience]` |
| Empty/low-data message | `[ANSWER]` | "Not enough data yet (need ≥ 30 users)" |
| Every chart shows | `[ANSWER]` | Title, plain-words explanation (ⓘ), last-updated time |

## 11.2 Dashboard inventory

> One row per dashboard. Suggested set for this lifecycle is pre-listed — keep, rename, or delete.

| ID | Dashboard name | Phase it starts | Main audience | Questions answered (Q-IDs) | Refresh | Priority | Owner | Status |
|---|---|---|---|---|---|---|---|---|
| D-001 | Instrumentation Health | P1 | Engineers | `Q-___` | Real-time | 🟢 | `[ANSWER]` | `Planned` |
| D-002 | QA / Data Quality | P2 | QA, Analyst | `Q-___` | Hourly | 🟢 | | |
| D-003 | Launch Command Center | P3 | Whole team | `Q-___` | 15 min | 🟢 | | |
| D-004 | Acquisition & Signup Funnel | P3 | Growth | `Q-___` | Daily | 🟢 | | |
| D-005 | Activation & Onboarding | P4 | Product | `Q-___` | Daily | 🟢 | | |
| D-006 | Engagement & Feature Adoption | P4 | Product | `Q-___` | Daily | 🟡 | | |
| D-007 | Retention & Cohorts | P5 | Product, Growth | `Q-___` | Daily | 🟡 | | |
| D-008 | Revenue & Conversion | P5 | Founder, Finance | `Q-___` | Daily | 🟡 | | |
| D-009 | Customer Health / Accounts (B2B) | P5 | Success team | `Q-___` | Daily | 🟡 | | |
| D-010 | Executive Scorecard + 500 Tracker | P4 | Founder, Leadership | `Q-___` | Daily | 🟢 | | |
| D-011 | Marketplace Liquidity (marketplace only) | P5 | Ops | `Q-___` | Daily | 🟡 | | |
| D-012 | `[ANSWER]` | | | | | | | |

## 11.3 📋 Dashboard spec block (copy once per dashboard)

> **How to fill:** Complete a full block for every 🟢 dashboard. Keep it simple: *question → chart → metric → filter*.

### Dashboard `D-___` — `[Name]`

| Field | ✏️ Your answer | Example |
|---|---|---|
| **Purpose in one sentence** | `[ANSWER]` | "Show where new users drop during signup." |
| **Main audience** | `[ANSWER]` | `Growth PM` |
| **Decisions it supports** | `[DEC-IDs]` | `DEC-B` |
| **Questions answered** | `[Q-IDs]` | `Q-001, Q-004` |
| **Refresh rate** | `[ANSWER]` | `Daily at 06:00 UTC` |
| **Default date range** | `[ANSWER]` | `Last 30 days` |
| **Filters** | `[ANSWER]` | `Date, Platform, Source, Plan` |
| **Data sources** | `[S-IDs]` | `S-001, S-002` |
| **Who can view / edit** | `[ANSWER]` | `View: all staff. Edit: Analyst` |
| **Link (after built)** | `[ANSWER]` | `[URL]` |
| **Links to other dashboards (drill-down)** | `[ANSWER]` | `Click funnel step → D-005` |
| **Mobile-friendly needed?** | `[ ] Yes  [ ] No` | `[x] No` |
| **Export/email schedule** | `[ANSWER]` | `Monday 08:00 email to leadership` |

**Layout sketch** *(draw with text; rows = lines, boxes = charts)*

```
┌───────────────────────────────────────────────────────────┐
│ [KPI 1]      [KPI 2]       [KPI 3]       [KPI 4]          │
├───────────────────────────────┬───────────────────────────┤
│ Chart 1: Trend over time      │ Chart 2: Funnel           │
├───────────────────────────────┼───────────────────────────┤
│ Chart 3: Breakdown by segment │ Chart 4: Table (top 10)   │
└───────────────────────────────┴───────────────────────────┘
```

✏️ **Your layout:**

```
[DRAW HERE]
```

**Chart list for this dashboard**

| Chart ID | Chart title | Question it answers | Chart type | Metric ID(s) | X-axis | Y-axis | Split by | Filter/exclusion | Comparison | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| C-001 | `[ANSWER]` | `Q-___` | `KPI / Line / Bar / Stacked bar / Funnel / Cohort grid / Table / Map / Pie (≤5 slices)` | `M-___` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `Exclude internal` | `Prev. period` | `[ANSWER]` |
| C-002 | | | | | | | | | | |
| C-003 | | | | | | | | | | |
| C-004 | | | | | | | | | | |
| C-005 | | | | | | | | | | |
| C-006 | | | | | | | | | | |

💡 **Which chart for which question?**

| If you want to show… | Use |
|---|---|
| One key number | KPI tile |
| Change over time | Line chart |
| Compare categories | Bar chart |
| Steps and drop-off | Funnel |
| Return over time | Cohort retention grid |
| Parts of a whole (few parts) | Stacked bar / small pie |
| Exact values / lists | Table |
| Where in the world | Map |

**Acceptance (when is this dashboard "done"?)**
- [ ] Every chart's number matches a manual check from raw data (Section 14).
- [ ] Every chart has a plain-words ⓘ explanation.
- [ ] Filters work and "exclude internal" is on by default.
- [ ] Loads in under `[ANSWER: e.g. 5]` seconds.
- [ ] Reviewed by the audience persona and the owner.

*(Repeat 11.3 for D-002, D-003, … Keep copies below this line.)*

---

## 11.4 Suggested contents for the standard dashboards (starting points)

| Dashboard | Suggested big numbers (top row) | Suggested charts |
|---|---|---|
| **D-001 Instrumentation Health** | Events received today; Event coverage %; Error rate; Last event time | Events per hour; Events by name; Events missing required props; SDK version split |
| **D-002 QA / Data Quality** | Test pass rate; Duplicate rate; Null rate | Failed tests list; Event schema violations; Staging vs expected counts |
| **D-003 Launch Command Center** | Visitors (24h); Signups (24h); Activated (24h); Errors (24h) | Hourly traffic; Signup funnel today; Top sources; Error log |
| **D-004 Acquisition & Signup Funnel** | Visitors; Signup conversion; Cost per signup | Funnel by source; Signups by channel; Drop-off by device |
| **D-005 Activation & Onboarding** | Activation rate; Time to activate (median); Onboarding completion | Step-by-step funnel; Activation by source/plan; Time-to-value distribution |
| **D-006 Engagement** | WAU; Stickiness; Key actions / user | Feature adoption; Sessions per user; Power users list |
| **D-007 Retention** | D1 / D7 / D30 retention; Lapsed users | Cohort grid by signup week; Retention curve; Reactivation |
| **D-008 Revenue** | MRR / GMV; Trial→paid; Churn; ARPU | Revenue trend; Plan mix; Refunds; Failed payments |
| **D-009 Customer Health (B2B)** | Active accounts; Seats used / bought; At-risk accounts | Account activity score; Expansion candidates; Churn risk list |
| **D-010 Executive Scorecard + 500 Tracker** | North Star; Customers vs 500 goal; Activation; Retention; Revenue | Progress bar to 500; Weekly trend of 5 key metrics; Targets vs actuals |
| **D-011 Marketplace Liquidity** | Listings; Searches with a result %; Transactions; Time to first transaction | Supply vs demand by category; Repeat rate by side; Take rate |

## 11.5 Dashboard-level rules

| Question | ✏️ Your answer |
|---|---|
| 11.5.1 What does a user do when a chart looks wrong? | `[ANSWER: e.g. Report in #data-help]` |
| 11.5.2 Who approves a **new** dashboard? | `[ANSWER]` |
| 11.5.3 Who deletes unused dashboards and when (e.g. 90 days no views)? | `[ANSWER]` |
| 11.5.4 Are numbers "locked" after the month closes? | `[ ] Yes  [ ] No` |

**✅ Done when**
- [ ] Every 🟢 dashboard has a full spec block.
- [ ] Every chart cites a question (Q-ID) and a metric (M-ID).
- [ ] No dashboard has more than the max charts.
- [ ] The Executive Scorecard shows progress to 500 customers.

---

# 12. 🟡 Alerts and Anomaly Rules

> **Why this matters:** Nobody stares at dashboards 24/7. Alerts tell you when something breaks or jumps.

## 12.1 Alert rules

| ID | Alert name | What we watch (Metric/Event) | Rule (plain words + number) | Check every | Severity | Who gets it | Where (email/chat/pager) | What to do first | Phase active |
|---|---|---|---|---|---|---|---|---|---|
| A-001 | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `Critical / High / Medium / Low` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `P3` |
| A-002 | | | | | | | | | |
| A-003 | | | | | | | | | |
| A-004 | | | | | | | | | |

**Starter ideas (pick, edit, or delete):**

| Alert idea | Example rule |
|---|---|
| Tracking stopped | "No `signup_completed` events for 60 minutes during working hours" |
| Sudden drop | "Signups down > 40% vs same hour last week" |
| Sudden spike | "Events up > 300% in 1 hour (bot or duplicate bug)" |
| Duplicate events | "Duplicate rate > 2%" |
| Missing properties | "> 5% of `payment_succeeded` without `amount`" |
| Funnel break | "Onboarding completion < 50% of 7-day average" |
| Payment trouble | "Payment failure rate > 5%" |
| Error surge | "Crash-free sessions < 99.5%" |
| Data freshness | "Dashboard data older than its freshness limit" |
| Milestone reached | "Customer count reaches 10 / 50 / 100 / 250 / 500" |

## 12.2 Alert hygiene

| Question | ✏️ Your answer |
|---|---|
| 12.2.1 Who owns each alert? (a person, not a team) | `[ANSWER]` |
| 12.2.2 How long until someone must respond? | `[ANSWER]` |
| 12.2.3 What is the escalation path if no one responds? | `[ANSWER]` |
| 12.2.4 How do we avoid alert fatigue (too many)? | `[ANSWER: e.g. max 10 active alerts; review monthly]` |
| 12.2.5 Do alerts account for small numbers (Section 6.7)? | `[ ] Yes  [ ] No` |
| 12.2.6 Where are incidents recorded? | `[ANSWER]` |

**✅ Done when**
- [ ] Every Critical alert has a named owner and a first action.
- [ ] At least one alert protects each of: tracking health, signups, payments (if any).
- [ ] Alerts avoid false alarms when user counts are very small.

---

# 13. 🟢 Privacy, Consent and Security

> **Why this matters:** Trust and the law. Collect only what you need, protect it, and honor people's choices. *(This is a practical checklist, not legal advice — have your legal/privacy contact review.)*

## 13.1 Data classification

| Question | ✏️ Your answer |
|---|---|
| 13.1.1 Which countries are our users in? | `[ANSWER]` |
| 13.1.2 Which rules apply? | `[ ] GDPR (EU/UK)  [ ] CCPA/CPRA (California)  [ ] Other US states  [ ] Children's privacy (COPPA / age rules)  [ ] Health (HIPAA)  [ ] Payments (PCI)  [ ] Other: ___` |
| 13.1.3 Do we collect children's data (under 13/16/18)? | `[ ] Yes  [ ] No` |
| 13.1.4 Who is our privacy contact / DPO? | `[ANSWER]` |

## 13.2 PII register (list every personal data item we store in analytics)

| Data item | Is it in analytics? | Reason we need it | How protected (hash / mask / drop) | Retention | Approved by |
|---|---|---|---|---|---|
| Email | `[ ] Yes [ ] No` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` |
| Name | | | | | |
| Phone | | | | | |
| IP address | | | | | |
| Exact location | | | | | |
| Device ID / ad ID | | | | | |
| Payment details (card numbers must **never** be here) | `[x] No — never` | — | — | — | — |
| Free-text typed by users | | | | | |
| `[ANSWER]` | | | | | |

💡 **Best practice:** Use an internal user ID; keep emails/names in your main database, not in analytics.

## 13.3 Consent and user rights

| Question | ✏️ Your answer |
|---|---|
| 13.3.1 Do we show a cookie/consent banner? Where? | `[ANSWER]` |
| 13.3.2 What do we track **before** consent? **After** consent? | `[ANSWER]` |
| 13.3.3 What happens if the user says "No"? | `[ANSWER]` |
| 13.3.4 How does a user ask us to delete their data? | `[ANSWER]` |
| 13.3.5 How fast do we respond (days)? | `[ANSWER]` |
| 13.3.6 Do we respect "Do Not Track / Global Privacy Control"? | `[ ] Yes  [ ] No` |
| 13.3.7 Mobile: do we handle app-store tracking prompts correctly? | `[ ] Yes  [ ] No  [ ] N/A` |
| 13.3.8 Is the privacy policy updated to mention analytics? | `[ ] Yes  [ ] No` |

## 13.4 Security checklist

- [ ] Access follows "least access needed" (Section 5.2).
- [ ] API keys / secrets are **not** in the code repo or in this document.
- [ ] Production and test keys are different.
- [ ] Raw user-level data is visible to the fewest people possible.
- [ ] Exports/downloads from dashboards are limited or logged.
- [ ] Access review is scheduled (Section 5.2.6).
- [ ] Data is encrypted in transit; storage is encrypted at rest.
- [ ] A breach/incident contact exists: `[ANSWER]`
- [ ] Third-party tools have a signed data-processing agreement: `[ ] Yes  [ ] N/A`

**✅ Done when**
- [ ] Every PII item is listed with a reason and a protection.
- [ ] Consent behavior is clear for "yes" and "no".
- [ ] Deletion requests have a process.
- [ ] Legal/privacy has reviewed this section (name & date in Section 22).

---

# 14. 🟢 Data Quality and QA Test Plan

> **Why this matters:** Wrong data is worse than no data. Test the tracking **before** launch and keep testing after.

## 14.1 Quality targets

| Quality check | Plain meaning | Target | How measured |
|---|---|---|---|
| **Completeness** | Required events/properties are present | `≥ 99%` | `[ANSWER]` |
| **Accuracy** | Numbers match the source of truth | `± 1%` | `[ANSWER]` |
| **Uniqueness** | No double-counted events | `Duplicate rate ≤ 1%` | `[ANSWER]` |
| **Validity** | Values are in the allowed list/format | `≥ 99.5%` | `[ANSWER]` |
| **Timeliness** | Data arrives on time | `Per Section 10.4` | `[ANSWER]` |
| **Consistency** | Same metric = same number on every dashboard | `100%` | `[ANSWER]` |

## 14.2 Test cases

> **How to fill:** One row per test. Use the examples, then add yours. Run in **staging** first, then in **production** with a test account.
> **Result:** Pass / Fail / Blocked. **Never** ship with a Failed 🟢 test.

| ID | What we test | Steps (plain words) | Expected result | Event(s) | Env | Tester | Result | Date | Notes / Bug link |
|---|---|---|---|---|---|---|---|---|---|
| T-001 | Signup event fires once | Create a new test account | 1 `signup_completed` with correct properties | `E-___` | Staging | `[ANSWER]` | `[ ]` | | |
| T-002 | Event names follow rules | Review all events in debug view | 100% match naming rules | All | Staging | | `[ ]` | | |
| T-003 | Required global properties exist | Trigger 5 different events | Each has all 🟢 global props | All | Staging | | `[ ]` | | |
| T-004 | Anonymous → known user link | Browse, then sign up | Pre-signup events join the same user | `E-___` | Staging | | `[ ]` | | |
| T-005 | No duplicate events | Click twice quickly; refresh page | Only legitimate events recorded | `E-___` | Staging | | `[ ]` | | |
| T-006 | Offline/retry behavior | Turn off network, act, turn on | Events arrive once, correct time | `E-___` | Staging | | `[ ]` | | |
| T-007 | Server events fire on real success only | Make a failed and a successful payment | Only success fires `payment_succeeded` | `E-___` | Staging | | `[ ]` | | |
| T-008 | Money values correct | Pay a test amount | Amount and currency match the invoice | `E-___` | Staging | | `[ ]` | | |
| T-009 | Consent respected | Decline consent | No analytics events (or only allowed ones) | All | Staging | | `[ ]` | | |
| T-010 | PII not leaked | Search events for emails/names | None found | All | Staging | | `[ ]` | | |
| T-011 | Funnel adds up | Compare funnel to raw counts | Equal within tolerance | `F-001` | Staging | | `[ ]` | | |
| T-012 | Dashboard number = source of truth | Compare 3 KPIs to the database | Within tolerance | `M-___` | Prod | | `[ ]` | | |
| T-013 | Internal users excluded | Use a team account | Not shown in dashboards | All | Prod | | `[ ]` | | |
| T-014 | All platforms work | Repeat T-001 on web, iOS, Android | Pass on each | `E-___` | Staging | | `[ ]` | | |
| T-015 | Old app versions | Use the previous app version | Events still valid or safely ignored | `E-___` | Staging | | `[ ]` | | |
| T-016 | Alerts fire | Cause a safe test breach | Alert reaches owner in time | `A-___` | Staging | | `[ ]` | | |
| T-017 | Dashboard speed | Load each dashboard | Under target seconds | `D-___` | Prod | | `[ ]` | | |
| T-018 | Access control | Log in as viewer / editor | Can only do allowed actions | `D-___` | Prod | | `[ ]` | | |
| T-019 | Deletion request | Delete a test user | Data removed/anonymized as promised | All | Staging | | `[ ]` | | |
| T-020 | `[ANSWER]` | | | | | | `[ ]` | | |

## 14.3 Reconciliation checks (numbers must match another source)

| Check | Compare A | with B | Allowed difference | Frequency | Owner |
|---|---|---|---|---|---|
| Signups | Analytics | App database | `[ANSWER]` | Daily | `[ANSWER]` |
| Revenue | Analytics | Payment provider | `[ANSWER]` | Weekly | `[ANSWER]` |
| Orders / GMV (marketplace) | Analytics | Order database | `[ANSWER]` | Daily | `[ANSWER]` |
| Ad spend | Dashboard | Ad platform | `[ANSWER]` | Weekly | `[ANSWER]` |

## 14.4 Go / No-Go checklist before launch (P2 → P3)

- [ ] All 🟢 events are **Verified** in staging **and** production.
- [ ] All 🟢 tests in 14.2 are **Passed**.
- [ ] Reconciliation checks are within tolerance.
- [ ] Privacy checklist (Section 13) is approved.
- [ ] Alerts for tracking-stopped and payments are live.
- [ ] Launch Command Center (D-003) and Executive Scorecard (D-010) are live.
- [ ] Rollback / "turn tracking off" plan exists: `[ANSWER]`
- [ ] Owners for the first 2 weeks are named and reachable.

**Decision:** `[ ] GO  [ ] NO-GO` — Decided by: `[ANSWER]` — Date: `YYYY-MM-DD`

## 14.5 After launch: ongoing quality routine

| Routine | Who | How often |
|---|---|---|
| Check D-001 / D-002 health | `[ANSWER]` | Daily (P3–P4), weekly after |
| Re-run top 10 tests after each release that touches tracking | `[ANSWER]` | Every release |
| Review schema violations | `[ANSWER]` | Weekly |
| Clean unused events | `[ANSWER]` | Quarterly |

**✅ Done when**
- [ ] Every 🟢 event has at least one test.
- [ ] Every 🟢 metric has at least one reconciliation check.
- [ ] Go/No-Go is signed.

---

# 15. 🟢 Implementation Plan and Responsibilities

> **Why this matters:** A spec nobody builds is just a story. Say who builds what, and by when.

## 15.1 Work breakdown

| ID | Task | Phase | Owner | Helper | Start | Due | Depends on | Ticket link | Status |
|---|---|---|---|---|---|---|---|---|---|
| W-001 | Approve this spec | P0 | `[ANSWER]` | | `YYYY-MM-DD` | `YYYY-MM-DD` | — | `[URL]` | `[ ]` |
| W-002 | Set up tools & environments (dev/staging/prod) | P1 | | | | | W-001 | | `[ ]` |
| W-003 | Add tracking SDK + global properties | P1 | | | | | W-002 | | `[ ]` |
| W-004 | Implement 🟢 events | P1 | | | | | W-003 | | `[ ]` |
| W-005 | Identity and consent handling | P1 | | | | | W-003 | | `[ ]` |
| W-006 | Build D-001 & D-002 | P1–P2 | | | | | W-004 | | `[ ]` |
| W-007 | Run QA test plan | P2 | | | | | W-004 | | `[ ]` |
| W-008 | Build D-003, D-004, D-010 | P2 | | | | | W-006 | | `[ ]` |
| W-009 | Set up alerts | P2 | | | | | W-008 | | `[ ]` |
| W-010 | Go / No-Go meeting | P2 | | | | | W-007 | | `[ ]` |
| W-011 | Launch & watch D-003 | P3 | | | | | W-010 | | `[ ]` |
| W-012 | Build D-005 to D-009 | P4–P5 | | | | | W-011 | | `[ ]` |
| W-013 | Reset targets after first 50 customers | P4 | | | | | | | `[ ]` |
| W-014 | `[ANSWER]` | | | | | | | | `[ ]` |

## 15.2 RACI (who is Responsible, Accountable, Consulted, Informed)

| Task area | Product Owner | Engineer | Analyst | Designer | QA | Privacy/Legal | PM |
|---|---|---|---|---|---|---|---|
| Metric definitions | A | C | R | I | I | I | I |
| Event design | A | R | C | I | C | C | I |
| Tracking code | I | R/A | C | I | C | I | I |
| Dashboards | A | C | R | R | C | I | I |
| QA tests | I | C | C | I | R/A | I | I |
| Privacy review | C | C | C | I | I | R/A | I |
| Launch decision | A | C | C | I | C | C | R |

*R = does the work · A = final say (only ONE per row) · C = asked for advice · I = told the result.*

## 15.3 Delivery questions

| Question | ✏️ Your answer |
|---|---|
| 15.3.1 How will AI assistants be used? (code, tests, queries, review) | `[ANSWER]` |
| 15.3.2 What must a human always review? | `[ANSWER: e.g. all tracking code, all money metrics]` |
| 15.3.3 How do we prevent tracking from breaking in later releases? | `[ANSWER: e.g. automated schema tests in CI]` |
| 15.3.4 What is the process to add/change an event later? | `[ANSWER]` |
| 15.3.5 Where is the tracking code documented? | `[ANSWER]` |

**✅ Done when**
- [ ] Every task has one owner and a due date.
- [ ] Dependencies are listed; no task is blocked silently.
- [ ] Each RACI row has exactly one "A".

---

# 16. 🟢 Rollout and the 500-Customer Milestone Tracker

> **Why this matters:** Your goal is *first 500 customers*. This section turns the goal into gates and a weekly habit, so surprises show up early.

## 16.1 Milestone gates

> At each gate, the team looks at the data, decides what to fix, and updates targets.

| Gate | Customers | Target date | What we must learn | Metrics to check (M-IDs) | Review meeting date | Result (Pass / Adjust) |
|---|---|---|---|---|---|---|
| G1 | **10** | `YYYY-MM-DD` | Does anyone reach "aha"? Why do people sign up? | `M-___` | `YYYY-MM-DD` | `[ ]` |
| G2 | **50** | `YYYY-MM-DD` | Is activation repeatable? Reset targets (W-013). | `M-___` | | `[ ]` |
| G3 | **100** | `YYYY-MM-DD` | Do people return in week 2–4? Which channel works? | `M-___` | | `[ ]` |
| G4 | **250** | `YYYY-MM-DD` | Is paying/transacting growing? What causes churn? | `M-___` | | `[ ]` |
| G5 | **500** | `YYYY-MM-DD` | Is growth repeatable and healthy? What next? | `M-___` | | `[ ]` |

## 16.2 Launch plan (P3)

| Question | ✏️ Your answer | Example |
|---|---|---|
| 16.2.1 Soft launch (small group) or hard launch (public)? | `[ ] Soft  [ ] Hard  [ ] Both` | `[x] Both` |
| 16.2.2 Who is in the first group? How many? | `[ANSWER]` | "100 waitlist users" |
| 16.2.3 Launch day watchers & schedule | `[ANSWER]` | "Lee and Sam, 9am–9pm" |
| 16.2.4 Where do we talk during launch? | `[ANSWER]` | "#launch-war-room" |
| 16.2.5 What are the stop conditions (when do we pause launch)? | `[ANSWER]` | "Crash-free < 98% or payment failures > 10%." |
| 16.2.6 Who can say "stop"? | `[ANSWER]` | `[ANSWER]` |

## 16.3 Weekly review (every week from P3 to G5)

**Agenda (30 minutes):**
1. Open D-010 Executive Scorecard (5 min).
2. Check data health D-001/D-002 — can we trust the numbers? (3 min)
3. Look at the funnel: where is the biggest drop? (7 min)
4. Read 5 customer comments / support tickets (5 min).
5. Decide **one** thing to improve and **one** thing to test (7 min).
6. Update the table below (3 min).

| Question | ✏️ Your answer |
|---|---|
| 16.3.1 Day/time of the weekly review | `[ANSWER]` |
| 16.3.2 Who attends / who runs it? | `[ANSWER]` |
| 16.3.3 Where are notes kept? | `[ANSWER]` |

### Weekly tracker (add a row every week)

| Week of | Customers (total) | New this week | North Star | Activation % | W1 retention % | Revenue | Biggest problem found | Action chosen | Owner | Done? |
|---|---|---|---|---|---|---|---|---|---|---|
| `YYYY-MM-DD` | | | | | | | | | | `[ ]` |
| `YYYY-MM-DD` | | | | | | | | | | `[ ]` |
| `YYYY-MM-DD` | | | | | | | | | | `[ ]` |
| `YYYY-MM-DD` | | | | | | | | | | `[ ]` |
| `YYYY-MM-DD` | | | | | | | | | | `[ ]` |
| `YYYY-MM-DD` | | | | | | | | | | `[ ]` |
| `YYYY-MM-DD` | | | | | | | | | | `[ ]` |
| `YYYY-MM-DD` | | | | | | | | | | `[ ]` |

## 16.4 Experiments (tests of ideas)

| ID | Idea | Which metric should move | Success rule | Needed users | Start | End | Result | Decision |
|---|---|---|---|---|---|---|---|---|
| X-001 | `[ANSWER]` | `M-___` | `[ANSWER]` | `[ANSWER]` | | | | |
| X-002 | | | | | | | | |

💡 With fewer than ~200 users, prefer **talking to users** and **before/after comparisons** over formal A/B tests.

## 16.5 Learning from customers (not only numbers)

| Question | ✏️ Your answer |
|---|---|
| 16.5.1 How do we collect feedback (survey, interview, in-app)? | `[ANSWER]` |
| 16.5.2 Do we ask "How would you feel if you could no longer use this?" | `[ ] Yes  [ ] No` |
| 16.5.3 Do we track NPS / CSAT? When? | `[ANSWER]` |
| 16.5.4 How do we link feedback to analytics (same user ID)? | `[ANSWER]` |

## 16.6 What happens at 500 customers?

| Question | ✏️ Your answer |
|---|---|
| 16.6.1 Which parts of this spec do we re-write? | `[ANSWER]` |
| 16.6.2 What new dashboards will we need (e.g. cohort revenue, LTV, forecasting)? | `[ANSWER]` |
| 16.6.3 Who owns the analytics long-term? | `[ANSWER]` |
| 16.6.4 Date of the "500-customer retrospective" | `YYYY-MM-DD` |

**✅ Done when**
- [ ] All five gates have dates and metrics.
- [ ] Launch stop conditions exist.
- [ ] The weekly review has an owner and a calendar slot.

---

# 17. 🟡 Operations and Maintenance

> **Why this matters:** Dashboards rot. Someone must keep them true.

| Question | ✏️ Your answer |
|---|---|
| 17.1 Who is the **long-term owner** of this spec? | `[ANSWER]` |
| 17.2 How do people **request** a new metric/dashboard? | `[ANSWER: form/link]` |
| 17.3 How fast do we answer requests (days)? | `[ANSWER]` |
| 17.4 How do we **rename or retire** an event/metric? | `[ANSWER: e.g. mark Deprecated, keep 90 days, remove]` |
| 17.5 How often do we **review this spec**? | `[ ] Monthly  [ ] Quarterly  [ ] After each gate` |
| 17.6 Where do people ask questions about the data? | `[ANSWER: channel]` |
| 17.7 Is there a "data dictionary" page for non-experts? | `[ANSWER: link]` |
| 17.8 How do we train new team members? | `[ANSWER]` |
| 17.9 Cost review of tools (how often)? | `[ANSWER]` |
| 17.10 Backup / recovery plan for dashboards and queries | `[ANSWER]` |

### Change process (simple)

1. Someone asks for a change → written in Section 19 (Decision Log) or Section 21 (Change History).
2. Owner + Analyst review (impact on metrics, privacy, cost).
3. Update this spec **first**, then the code and dashboards.
4. QA re-tests affected events (Section 14).
5. Announce to users of the affected dashboards.

**✅ Done when**
- [ ] A long-term owner is named.
- [ ] Retiring/renaming rules exist.
- [ ] Review schedule is set.

---

# 18. 🟢 Risks, Assumptions and Open Questions

## 18.1 Risks

| ID | Risk (what could go wrong) | Chance (H/M/L) | Impact (H/M/L) | Early warning sign | What we do to prevent | What we do if it happens | Owner |
|---|---|---|---|---|---|---|---|
| R-001 | Tracking breaks after a release | `M` | `H` | Event counts drop | Automated tests in CI | Roll back; backfill | `[ANSWER]` |
| R-002 | Too few users for reliable percentages | `H` | `M` | Charts jump wildly | Section 6.7 rules | Show counts; interview users | `[ANSWER]` |
| R-003 | Privacy complaint or fine | `L` | `H` | Deletion requests rising | Section 13 | Follow incident plan | `[ANSWER]` |
| R-004 | Two teams define a metric differently | `M` | `M` | Numbers disagree | Single metric dictionary | Merge definitions | `[ANSWER]` |
| R-005 | Tool cost grows faster than revenue | `M` | `M` | Bill > budget | Sampling, retention limits | Reduce events | `[ANSWER]` |
| R-006 | AI-generated code tracks wrong things | `M` | `M` | Test failures | Human review + QA | Fix and re-test | `[ANSWER]` |
| R-007 | `[ANSWER]` | | | | | | |

## 18.2 Assumptions (things we believe but have not proven)

| ID | Assumption | How we will check it | By when | Status |
|---|---|---|---|---|
| AS-001 | `[ANSWER]` | `[ANSWER]` | `YYYY-MM-DD` | `Open / Confirmed / Wrong` |
| AS-002 | | | | |

**Example:** "Users who finish onboarding in the first day stay longer — check at G2 (50 customers)."

## 18.3 Open questions (things we still do not know)

| ID | Question | Why it matters | Who can answer | Needed by | Answer | Status |
|---|---|---|---|---|---|---|
| OQ-001 | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `YYYY-MM-DD` | | `Open / Answered` |
| OQ-002 | | | | | | |
| OQ-003 | | | | | | |

> ⚠️ Spec cannot be Approved while any 🟢-related open question is still `Open` past its due date.

---

# 19. 🟡 Decision Log

> **Why this matters:** Six months from now nobody remembers *why* you chose a rule. Write it here.

| ID | Date | Decision | Options we considered | Why we chose this | Decided by | Affects (sections) |
|---|---|---|---|---|---|---|
| DL-001 | `YYYY-MM-DD` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` |
| DL-002 | | | | | | |
| DL-003 | | | | | | |
| DL-004 | | | | | | |

**Example:** `DL-001 | 2026-10-20 | Activation = first_plan_completed within 24h | (a) first signup, (b) first task created, (c) first plan completed | Plan completion best matched interview feedback on "value" | Product Owner | Sections 6, 7`

---

# 20. 🟡 Dependencies and Related Documents

| Document / System | Link | Owner | Why it matters |
|---|---|---|---|
| Product Requirements Document (PRD) | `[URL]` | `[ANSWER]` | Source of features and journeys |
| Design files (Figma etc.) | `[URL]` | `[ANSWER]` | Screens to attach events to |
| Technical architecture doc | `[URL]` | `[ANSWER]` | Data flow |
| Privacy policy & data-processing agreements | `[URL]` | `[ANSWER]` | Legal basis |
| Tracking code repository | `[URL]` | `[ANSWER]` | Where events live |
| Data dictionary / catalog | `[URL]` | `[ANSWER]` | Shared definitions |
| Test plan / QA tool | `[URL]` | `[ANSWER]` | Section 14 results |
| Dashboard folder in BI tool | `[URL]` | `[ANSWER]` | Live dashboards |
| Support / feedback tool | `[URL]` | `[ANSWER]` | Qualitative data |
| Go-to-market / launch plan | `[URL]` | `[ANSWER]` | Marketing events and channels |

---

# 21. 🟢 Change History

> Add a new row **every time** this file changes. Never delete old rows.

| Version | Date | Changed by | What changed (sections) | Why | Approved by |
|---|---|---|---|---|---|
| 0.1.0 | `YYYY-MM-DD` | `[ANSWER]` | Initial draft | First version | |
| | | | | | |
| | | | | | |

**Version numbering:** `MAJOR.MINOR.PATCH`
- **MAJOR** — a metric meaning or North Star changed.
- **MINOR** — new events, metrics, or dashboards added.
- **PATCH** — typos, links, clarifications.

---

# 22. 🟢 Approvals and Sign-Off

> A spec is **Approved** only when every 🟢 box in every section is ticked **and** the people below sign.

## 22.1 Completeness check (tick before asking for signatures)

- [ ] Sections 0–16, 18, 21 have no empty cells (`TBD` has an owner and date).
- [ ] No example text remains unless it is true for this product.
- [ ] All IDs (M-, E-, F-, D-, C-, A-, T-, W-) are unique and cross-referenced correctly.
- [ ] Every 🟢 metric → has events → has tests → appears on a dashboard.
- [ ] Section 1 summary is updated and matches the rest.
- [ ] Appendix B YAML matches the tables (if used by AI agents).

## 22.2 Signatures

| Role | Name | Decision (Approve / Approve with notes / Reject) | Date | Notes |
|---|---|---|---|---|
| Product Owner | | | | |
| Engineering Lead | | | | |
| Data / Analytics Lead | | | | |
| QA Lead | | | | |
| Privacy / Legal | | | | |
| Executive Sponsor | | | | |

---

# APPENDIX A — 🤖 AI-Agent Instructions

> **For humans:** This appendix lets AI coding and analysis agents work safely from this file. You do not need to fill anything here unless your team adds extra rules.

## A.1 Agent contract (rules agents must follow)

1. **Source of truth:** Only use information in this file. If a value is `TBD`, empty, or conflicting → **stop and ask a human**; list the exact section and question.
2. **No invention:** Do not create events, properties, metrics, filters, or dashboards that are not defined here. Propose additions in a separate "Proposed changes" list instead.
3. **IDs:** Always reference items by ID (`E-014`, `M-003`, `D-005`). Never rename an item.
4. **Naming:** Follow Section 8.1 exactly.
5. **Privacy first:** Never add personal data to events. Never send data to a tool not listed in Section 10.1. Never place secrets or keys in code, logs, or this file.
6. **Server vs client:** Fire money, signup, and account events from the **server** as specified.
7. **Human approval required** before: changing metric formulas, adding PII, changing identity rules, changing alert thresholds, deleting data, or publishing dashboards to external audiences.
8. **Explain uncertainty:** State assumptions plainly. Prefer asking over guessing.
9. **Keep in sync:** When code, queries, or dashboards change, list which sections of this file must be updated.
10. **Test everything:** Every event/metric the agent touches needs a test from Section 14 (create it if missing, marked `proposed`).

## A.2 Reading order for an agent

1. Section 2.2 (definitions) → 2. Section 3 (phase) → 3. Section 6 (metrics) → 4. Section 7 (funnels) → 5. Section 8 (events) → 6. Section 9 (identity) → 7. Section 13 (privacy) → 8. Section 11 (dashboards) → 9. Section 14 (tests) → 10. Appendix B.

## A.3 Standard agent tasks and what to deliver

| Task | Input from this file | Output the agent must produce | Human checks |
|---|---|---|---|
| **Spec review** | Whole file | List of gaps, contradictions, vague words, missing owners (with section numbers) | Product Owner |
| **Event proposal** | Sections 7, 8.1 | Draft rows for 8.5 (ID, name, trigger, props, linked metrics) | Analyst + Engineer |
| **Tracking code** | Sections 8, 9, 13, Appendix B | Code that sends only listed events; unit tests; no PII | Engineer |
| **Test generation** | Sections 8, 14 | Test cases in 14.2 format; automated schema checks | QA |
| **Query / model writing** | Section 6.5, 8, 9 | Queries per metric with filters (exclude internal), tolerance notes | Analyst |
| **Dashboard build** | Section 11 | Chart configs matching chart list; layout; filters | Designer + Analyst |
| **Alert drafting** | Section 12 | Alert rules with thresholds and owners (proposed) | Data Lead |
| **Weekly summary** | Section 16.3 + live data | 1-page summary: customers, North Star, biggest drop, anomalies, suggested action | Product Owner |
| **Data-quality triage** | Section 14.1, D-001/D-002 | Ranked issues with likely cause and fix | Engineer |

## A.4 Ready-to-use prompt snippets

**Spec gap review**
```
Read Product_Analytics_Dashboard_Spec.md. Do not assume anything not written there.
List: (1) empty or TBD fields, (2) contradictions between sections, (3) vague words
(e.g. "fast", "many"), (4) metrics without events, (5) events without metrics,
(6) dashboards without questions. Output a table with section number, problem, and
the exact question a human must answer.
```

**Generate tracking code**
```
Using only Sections 8, 9 and Appendix B of Product_Analytics_Dashboard_Spec.md,
implement the events marked priority 🟢 and status "Planned" for platform: <platform>.
Follow naming rules in 8.1. Do not send personal data. Fire events marked "server"
from the backend. Add unit tests. List any ambiguity as questions instead of guessing.
```

**Weekly summary**
```
Using the metric definitions in Section 6.5 and the latest data, write a one-page weekly
summary: customers vs milestone gate, North Star, activation, retention, biggest funnel
drop, anomalies, and ONE recommended action with the data behind it. Apply the small-number
rules in 6.7. Mark anything uncertain.
```

## A.5 "Definition of Done" for agent output

- [ ] Every item is traceable to an ID in this file.
- [ ] No unapproved events, properties, or tools.
- [ ] Privacy rules respected.
- [ ] Tests included and passing, or listed as `proposed`.
- [ ] Questions for humans are listed clearly.
- [ ] Sections needing updates are listed.

---

# APPENDIX B — 🤖 Machine-Readable Blocks (YAML)

> **How to fill:** Mirror your tables here so tools can read them. Keep IDs identical to the tables. If a table and YAML disagree, the **table wins** and the YAML must be fixed.
> 💡 Humans may leave this empty until engineering starts; AI agents may draft it, humans approve.

## B.1 Product

```yaml
product:
  name: "[ANSWER]"
  type: [b2c_app]            # b2c_app | b2b_saas | marketplace
  platforms: [web, ios]      # web | ios | android | desktop | api
  customer_definition: "[ANSWER — same as Section 2.2.2]"
  reporting_timezone: "UTC"
  reporting_currency: "USD"
  week_starts_on: "monday"
  excluded_traffic: [internal_users, test_accounts, bots]
```

## B.2 Metrics

```yaml
metrics:
  - id: M-001
    name: "[North Star name]"
    category: engagement
    definition: "[plain words]"
    formula: "[exact formula]"
    numerator: "[ANSWER]"
    denominator: "[ANSWER or null]"
    unit: count            # percent | count | currency | seconds | ratio
    counted_per: user      # user | account | session | order
    source_events: [E-005]
    time_window: "7d"
    filters: ["exclude_internal"]
    segments: [platform, country, source, plan]
    good_direction: up     # up | down | range
    targets: { P4: null, P5: null, P6: null }
    owner: "[ANSWER]"
    refresh: daily
    dashboards: [D-010]
    status: proposed       # proposed | approved | live | retired
```

## B.3 Events

```yaml
events:
  - id: E-001
    name: "signup_completed"
    description: "Fires once when a new account is successfully created."
    fired_from: server       # client | server
    priority: must           # must | should | nice
    properties:
      - { name: signup_method, type: enum, values: [email, google, apple], required: true }
      - { name: acquisition_source, type: string, required: false }
    pii: false
    metrics: [M-002]
    owner: "[ANSWER]"
    phase_live: P3
    status: planned          # planned | in_progress | in_staging | verified | live | deprecated
```

## B.4 Funnels

```yaml
funnels:
  - id: F-001
    name: "Signup funnel"
    counted_per: user
    max_duration: "7d"
    steps: [E-010, E-011, E-001, E-012, E-014]
```

## B.5 Dashboards

```yaml
dashboards:
  - id: D-010
    name: "Executive Scorecard + 500 Tracker"
    audience: [founder, leadership]
    refresh: daily
    default_range: "last_30d"
    filters: [date, platform, country, plan, source, exclude_internal]
    charts:
      - { id: C-001, title: "Customers vs 500 goal", type: kpi, metrics: [M-020] }
      - { id: C-002, title: "North Star weekly", type: line, metrics: [M-001] }
```

## B.6 Alerts

```yaml
alerts:
  - id: A-001
    name: "Signup tracking stopped"
    watch: E-001
    rule: "count == 0 for 60 minutes during 08:00-22:00 UTC"
    severity: critical
    owner: "[ANSWER]"
    channel: "[ANSWER]"
    first_action: "[ANSWER]"
```

## B.7 Tests

```yaml
tests:
  - id: T-001
    covers: [E-001]
    env: staging
    steps: ["Create a new test account"]
    expected: "Exactly 1 signup_completed with required properties"
    status: not_run          # not_run | pass | fail | blocked
```

---

# APPENDIX C — Starter Event Packs

> **How to use:** Copy the rows you need into Section 8.5, give them IDs, and change names/properties to fit. Delete what you do not need. `S` = best fired from server, `C` = client.

## C.1 Core pack (everyone)

| Event name | When it fires | Where | Key properties |
|---|---|---|---|
| `app_opened` | App/site session begins | C | `entry_source` |
| `page_viewed` / `screen_viewed` | A page/screen is shown | C | `page_name`, `referrer` |
| `signup_started` | User begins signup | C | `signup_method` |
| `signup_completed` | Account successfully created | S | `signup_method` |
| `login_succeeded` | User logs in | S | `login_method` |
| `login_failed` | Login fails | S | `reason` |
| `logout_completed` | User logs out | C | — |
| `onboarding_step_completed` | Each onboarding step done | C | `step_name`, `step_number` |
| `onboarding_completed` | All onboarding done | S | `duration_seconds` |
| `activation_reached` | User hits the "aha" moment (Section 7.2) | S | `minutes_since_signup` |
| `feature_used` | Key feature is used | C/S | `feature_name` |
| `search_performed` | User searches | C | `result_count` (no raw text if sensitive) |
| `notification_received` / `_clicked` | Push/email interaction | C/S | `channel`, `campaign_id` |
| `invite_sent` / `invite_accepted` | Referral or teammate invite | S | `channel` |
| `error_shown` | User sees an error | C | `error_code`, `screen` |
| `support_contacted` | User asks for help | S | `channel`, `topic` |
| `feedback_submitted` | Survey/NPS answered | C | `score`, `survey_id` |
| `consent_updated` | User changes consent | C | `categories_allowed` |
| `account_deleted` | User deletes account | S | `reason` |

## C.2 Revenue pack (any paid product)

| Event name | When it fires | Where | Key properties |
|---|---|---|---|
| `paywall_viewed` | Upgrade screen shown | C | `trigger`, `plan_shown` |
| `trial_started` | Free trial begins | S | `plan_type`, `trial_days` |
| `checkout_started` | User begins checkout | C | `plan_type`, `amount`, `currency` |
| `payment_succeeded` | Charge confirmed | S | `invoice_id`, `amount`, `currency`, `plan_type` |
| `payment_failed` | Charge fails | S | `invoice_id`, `failure_reason` |
| `subscription_upgraded` / `_downgraded` | Plan changes | S | `from_plan`, `to_plan` |
| `subscription_cancelled` | User cancels | S | `plan_type`, `cancel_reason` |
| `refund_issued` | Money returned | S | `invoice_id`, `amount`, `currency` |

## C.3 B2C add-ons

| Event name | When it fires | Where | Key properties |
|---|---|---|---|
| `content_viewed` | Item/article/video opened | C | `content_id`, `content_type` |
| `content_created` | User makes something | C/S | `content_type` |
| `streak_continued` / `streak_broken` | Habit loop | S | `streak_length` |
| `share_clicked` | User shares | C | `destination` |
| `app_installed` / `app_uninstalled` | Install lifecycle | S | `store`, `campaign` |
| `permission_prompt_answered` | Push/location permission | C | `permission`, `granted` |

## C.4 B2B SaaS add-ons

| Event name | When it fires | Where | Key properties |
|---|---|---|---|
| `workspace_created` | New account/workspace | S | `plan_type`, `company_size_band` |
| `teammate_invited` | Admin invites a user | S | `role`, `invite_count` |
| `teammate_joined` | Invited user joins | S | `role` |
| `integration_connected` | Tool connected | S | `integration_name` |
| `project_created` | Core object created | C/S | `project_type` |
| `data_imported` | Data brought in | S | `source`, `row_count_band` |
| `report_exported` | Output exported | C/S | `format` |
| `seat_added` / `seat_removed` | Seats change | S | `seats_total` |
| `admin_setting_changed` | Settings change | S | `setting_name` |
| `sso_enabled` | Enterprise login on | S | `provider` |
| `contract_signed` (sales-led) | Deal closes | S | `contract_value`, `term_months` |

## C.5 Marketplace / e-commerce add-ons

| Event name | When it fires | Where | Key properties |
|---|---|---|---|
| `listing_created` | Seller adds item/service | S | `category`, `price`, `currency` |
| `listing_published` | Listing goes live | S | `listing_id` |
| `search_performed` | Buyer searches | C | `query_category`, `result_count`, `filters_used` |
| `search_no_results` | Zero results returned | C/S | `query_category` |
| `listing_viewed` | Buyer opens listing | C | `listing_id`, `position` |
| `item_saved` / `wishlisted` | Buyer saves | C | `listing_id` |
| `message_sent` | Buyer↔seller message | S | `listing_id`, `sender_role` |
| `offer_made` / `offer_accepted` | Negotiation | S | `listing_id`, `amount` |
| `add_to_cart` / `remove_from_cart` | Cart changes | C | `listing_id`, `quantity` |
| `order_placed` | Order created | S | `order_id`, `amount`, `currency`, `item_count` |
| `order_fulfilled` | Delivered/completed | S | `order_id`, `days_to_fulfil` |
| `order_cancelled` | Order cancelled | S | `order_id`, `cancelled_by`, `reason` |
| `review_submitted` | Rating left | C/S | `order_id`, `rating`, `side` |
| `dispute_opened` | Problem reported | S | `order_id`, `reason` |
| `payout_sent` | Seller paid | S | `payout_id`, `amount`, `currency` |

---

# APPENDIX D — Metric Formula Cheat Sheet

> 💡 Use these as starting points. **Always** write the final exact version in Section 6.5.

| Metric | Plain meaning | Common formula |
|---|---|---|
| Signup conversion | Visitors who sign up | `signups / unique_visitors` |
| Activation rate | New users who reach "aha" | `activated_users / new_signups` (within window) |
| Time to value | How fast they get value | `median(activation_time − signup_time)` |
| DAU / WAU / MAU | Active users per day / week / month | `count(distinct active_user_id)` in period |
| Stickiness | How habitual | `DAU / MAU` |
| Classic D-N retention | Came back exactly on day N | `users active on day N / users in cohort` |
| Rolling retention | Came back on or after day N | `users active on or after day N / cohort` |
| Churn rate (users) | Users lost in period | `users_lost / users_at_start` |
| Revenue churn | Revenue lost | `MRR_lost / MRR_at_start` |
| MRR | Monthly recurring revenue | `sum(active subscription monthly value)` |
| ARR | Annual recurring revenue | `MRR × 12` |
| ARPU / ARPA | Average revenue per user / account | `revenue / active_users (or accounts)` |
| Trial → paid | Trials that convert | `paid_conversions / trials_started` |
| LTV (simple) | Lifetime value | `ARPU × gross_margin / churn_rate` |
| CAC | Cost to win a customer | `sales+marketing_spend / new_customers` |
| LTV : CAC | Is acquisition worth it | `LTV / CAC` (aim to learn your own benchmark) |
| CAC payback | Months to earn CAC back | `CAC / (ARPU × gross_margin)` |
| Net revenue retention (B2B) | Revenue kept + grown from existing | `(start + expansion − contraction − churn) / start` |
| Logo churn (B2B) | Accounts lost | `accounts_lost / accounts_at_start` |
| Viral coefficient | New users brought per user | `invites_per_user × invite_conversion` |
| NPS | Would they recommend? | `% promoters (9–10) − % detractors (0–6)` |
| GMV (marketplace) | Total value of goods sold | `sum(order_amount)` |
| Take rate | Share we keep | `net_revenue / GMV` |
| Liquidity (supply side) | Listings that sell | `listings_with_≥1_order / active_listings` |
| Liquidity (demand side) | Searches that succeed | `searches_with_result_clicked / searches` |
| Time to first transaction | Speed to first deal | `median(first_order_time − signup_time)` |
| Repeat purchase rate | Buyers who buy again | `buyers_with_≥2_orders / buyers_with_≥1_order` |
| Event coverage | Tracked vs planned | `verified_live_events / planned_must_events` |
| Duplicate rate | Double-counted events | `duplicate_events / total_events` |
| Error rate | Failed actions | `error_events / total_actions` |

---

# APPENDIX E — Full Glossary

| Term | Plain-words meaning |
|---|---|
| A/B test | Show two versions to different people and see which does better |
| Account | A company/team/organization in a B2B product |
| Activation | First time a new user gets real value |
| Alert | An automatic warning when a number looks wrong |
| Anonymous ID | A temporary ID for someone not logged in |
| ARPU / ARPA | Average revenue per user / account |
| ARR / MRR | Yearly / monthly repeating revenue |
| Attribution | Giving credit to the channel that brought a user |
| Backfill | Re-sending or re-computing past data |
| BI tool | Software that makes charts and dashboards |
| Churn | People or revenue lost over time |
| Client-side event | Recorded from the user's device |
| Cohort | A group that started in the same time period |
| Consent | The user's permission to be tracked |
| Conversion | A person completing a wanted step |
| DAU / WAU / MAU | Daily / weekly / monthly active users |
| Dashboard | A screen of charts for answering questions |
| Data warehouse | A big database for analysis |
| Deduplication | Removing repeated copies of the same event |
| Dimension | A way to split data (country, device…) |
| Event | A recorded user or system action |
| Freshness | How recent the data is |
| Funnel | Ordered steps with drop-off |
| Guardrail | A number we protect from getting worse |
| Identity resolution | Joining one person's anonymous and logged-in activity |
| Instrumentation | Adding tracking code |
| KPI | Key performance indicator — an important metric |
| Liquidity | How easily marketplace supply meets demand |
| LTV | Lifetime value of a customer |
| Metric | A number that measures something |
| North Star Metric | The single best measure of delivered value |
| NPS | Net Promoter Score — willingness to recommend |
| PII | Personally identifiable information |
| Property | Extra details attached to an event |
| Retention | People coming back over time |
| Segment | A slice of users |
| Server-side event | Recorded by your backend (more reliable) |
| Session | One continuous visit/use period |
| Source of truth | The system we trust when numbers disagree |
| Stickiness | How often monthly users come daily (DAU/MAU) |
| Take rate | The share of each transaction the marketplace keeps |
| Time to value | Time from signup to first real benefit |
| UTM | Tags on links that show which campaign brought a visitor |

---

# APPENDIX F — Final "Ready to Ship" Checklist

> Tick everything before changing Status to **Approved**, and again before **Go-Live**.

## F.1 Writing quality

- [ ] A 10-year-old could read my answers and understand what we are measuring.
- [ ] No empty fields; every `TBD` has an owner and a date.
- [ ] Examples were replaced or confirmed true.
- [ ] Every number has a unit and a time window.
- [ ] No vague words left ("fast", "many", "soon", "good", "some").
- [ ] One name per thing, used everywhere.

## F.2 Content completeness

- [ ] Customer, active, churned defined (2.2).
- [ ] Phase map with dates, owners, exit rules (3).
- [ ] Questions → decisions mapped (4).
- [ ] Audience and access rules (5).
- [ ] North Star, input metrics, guardrails, dictionary (6).
- [ ] Journey, activation, funnels, retention (7).
- [ ] Tracking plan: naming, global props, events, coverage (8).
- [ ] Identity, time, money, test traffic rules (9).
- [ ] Tools, flow, freshness, retention, environments (10).
- [ ] Dashboards with chart-level specs and acceptance (11).
- [ ] Alerts with owners (12).
- [ ] Privacy, consent, security (13).
- [ ] QA plan and Go/No-Go (14).
- [ ] Implementation plan and RACI (15).
- [ ] 500-customer gates, launch plan, weekly review (16).
- [ ] Maintenance and ownership (17).
- [ ] Risks, assumptions, open questions (18).

## F.3 Traceability (nothing floating)

- [ ] Goal → Question → Decision → Metric → Event → Test → Dashboard → Alert are all linked by IDs.
- [ ] Every event serves a metric or funnel.
- [ ] Every metric appears on a dashboard.
- [ ] Every dashboard chart answers a question.
- [ ] Every Critical alert has an owner and first action.

## F.4 Safety and trust

- [ ] No personal data in events beyond what Section 13 approves.
- [ ] No secrets in this file.
- [ ] Consent and deletion paths are defined and tested.
- [ ] Internal/test traffic is excluded everywhere.

## F.5 Launch readiness (before P3)

- [ ] Go/No-Go decision recorded (14.4).
- [ ] Launch watchers named (16.2).
- [ ] Stop conditions agreed (16.2.5).
- [ ] Weekly review scheduled (16.3).

## F.6 After launch

- [ ] D-010 (Executive Scorecard + 500 Tracker) is reviewed weekly.
- [ ] Targets reset at G2 (50 customers).
- [ ] Spec reviewed at each gate and version bumped (Section 21).
- [ ] 500-customer retrospective scheduled (16.6).

---

*End of template. Keep this file in the "Product analytics and instrumentation" folder. For each new project, copy it, rename the title in Section 0, and start at "How to fill this document".*
