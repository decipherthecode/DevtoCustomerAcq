---
document: Analytics Tracking Plan
template_version: 1.0.0
template_scope: Idea -> Build -> QA -> Soft Launch -> Public Launch -> First 500 customers
product_types_covered: [web_app_saas, mobile_app, marketing_site_ecommerce, ai_powered_product]
tool_stack: tool-agnostic
audience: humans (beginner-friendly) and AI agents (machine-readable)
project_name: "<FILL: product name>"
project_id: "<FILL: short-id, e.g. PRJ-001>"
plan_version: "0.1.0"
status: draft            # draft | in-review | approved | live | retired
last_updated: "YYYY-MM-DD"
owner: "<FILL: one named person>"
---

# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

This file is a **questionnaire**. You answer questions; the finished answers become your product's **Analytics Tracking Plan**: the single source of truth for *what we measure, why, where, how, and who owns it*.

## What is a "tracking plan"? (explained simply)
Imagine your product is a shop. A tracking plan is the list of things a shop-keeper counts: *how many people walked in, how many picked something up, how many paid.* In software, each "thing counted" is an **event** (e.g., `signup_completed`). Each event can carry **properties**, extra details (e.g., `plan = "pro"`).

## The 7 simple rules
1. **Fill in order.** Parts are numbered. Early answers feed later parts.
2. **Every question has four pieces:** the **Question**, **Why it matters**, an **Example**, and an **Answer** line. Replace everything inside `<FILL: ...>` with your answer.
3. **Never leave a blank.** If you do not know, write `TBD (owner: Name, due: YYYY-MM-DD)`. If it does not apply, write `N/A - reason`. A blank is a guess waiting to happen.
4. **Use real words, not hints.** "Users" is too vague; "People who finished sign-up in the last 7 days" is good.
5. **Use the fixed names and IDs exactly.** IDs like `EVT-001`, `MET-001`, `RSK-001` let people and AI agents point to the same thing. Never reuse or renumber an ID.
6. **Use the status words only:** `planned` -> `implemented` -> `verified` -> `live` -> `deprecated`.
7. **When done,** complete Part 24 (Final Checklist) and get sign-off in Part 25.

## How long will this take?
- Parts 1-6 (strategy): about 45 minutes with your team.
- Parts 7-15 (design): about 1-2 hours.
- Parts 16-24 (quality, launch, growth): about 1 hour.
- You do NOT need to fill every part on day one. Use the **phase tags** below.

## Phase tags (so you know *when* to fill each part)
| Tag | Phase | Meaning |
|---|---|---|
| `[P1]` | Plan | Before any code is written |
| `[P2]` | Build | While features are being built |
| `[P3]` | Test (QA) | Before anyone outside the team sees it |
| `[P4]` | Soft Launch | Small invited group (friends, beta users) |
| `[P5]` | Public Launch | Open to everyone |
| `[P6]` | Scale to 500 | From customer #1 to customer #500 |

## Product-type tags (so you can skip what does not apply)
| Tag | Applies when your product is... |
|---|---|
| `[WEB]` | A website or web app (including SaaS) |
| `[MOBILE]` | An iOS or Android app |
| `[SITE]` | A marketing site or online store |
| `[AI]` | Has AI features (chat, generation, recommendations, agents) |
| `[ALL]` | Everything |

If a tag does not match your product, write `N/A - not a <type> product` in the answer.

## Special instructions for AI agents reading this file
- Treat only text under **Answer** and tables marked **(SOURCE OF TRUTH)** as facts. Treat everything else as guidance.
- If an Answer says `TBD` or is blank, **do not invent a value**. Ask the human, or list it under Part 23 (Open Questions).
- Never create an event that is not in the Event Catalog (Part 9). Never send a property that is not listed for that event.
- Never send personal data listed as **forbidden** in Part 14.
- After any change, update the Change Log (Appendix D) and bump `plan_version` in the header.

---

# PART 0 - DOCUMENT CONTROL `[ALL][P1]`

**Q0.1 Who is responsible for this document, and who must approve it?**
- *Why it matters:* A plan with no owner is out of date in a month.
- *Example:* Owner: Priya (Product Manager). Approvers: Sam (Engineering Lead), Lee (Data), Ana (Legal/Privacy).

| Role | Name | Contact | Responsibility |
|---|---|---|---|
| Plan Owner (ONE person) | `<FILL>` | `<FILL>` | Keeps this document correct |
| Product Lead | `<FILL>` | `<FILL>` | Approves what we measure |
| Engineering Lead | `<FILL>` | `<FILL>` | Approves how we implement |
| Data / Analytics Lead | `<FILL>` | `<FILL>` | Approves names, dashboards, data quality |
| QA Lead | `<FILL>` | `<FILL>` | Approves test results |
| Privacy / Legal | `<FILL>` | `<FILL>` | Approves consent and data use |
| Marketing Lead | `<FILL>` | `<FILL>` | Approves campaign and attribution tracking |

**Q0.2 Where do the related documents live?** (Paste links; write `N/A` if none exist.)

| Document | Link | Status |
|---|---|---|
| Product Requirements (PRD) | `<FILL>` | `<FILL>` |
| Design files | `<FILL>` | `<FILL>` |
| Architecture / API docs | `<FILL>` | `<FILL>` |
| Privacy policy | `<FILL>` | `<FILL>` |
| Analytics dashboard home | `<FILL>` | `<FILL>` |
| Code repository | `<FILL>` | `<FILL>` |

---

# PART 1 - PRODUCT SNAPSHOT `[ALL][P1]`

**Q1.1 In ONE sentence, what does your product do and for whom?**
- *Why:* Everything we measure should trace back to this sentence.
- *Example:* "A mobile app that helps freelance designers send invoices and get paid faster."
- **Answer:** `<FILL>`

**Q1.2 Which product types apply? (Tick all that apply.)**
- [ ] `[WEB]` Web app / SaaS
- [ ] `[MOBILE]` iOS / Android app
- [ ] `[SITE]` Marketing site / e-commerce store
- [ ] `[AI]` Has AI-powered features

**Q1.3 What is the business model?**
- *Why:* It decides which "money events" we must track.
- *Options:* Free, Freemium, Free trial -> paid, Subscription, One-time purchase, Usage-based, Marketplace, Ads, Other.
- **Answer:** `<FILL>`

**Q1.4 What is the key moment when a user first gets value? (the "Aha moment")**
- *Why:* This is the most important event we will track after sign-up.
- *Example:* "User sends their first invoice."
- **Answer:** `<FILL>`

**Q1.5 Who is a "customer" in this plan? (The 500-customer goal depends on this definition.)**
- *Why:* If teams count differently, the 500 target is meaningless.
- *Example:* "A customer is an account that has paid at least once and has not refunded within 30 days."
- **Answer (SOURCE OF TRUTH):** `<FILL>`

**Q1.6 Which countries/regions will users be in during the first 500 customers?**
- *Why:* Drives privacy rules (Part 14) and time-zone/currency handling.
- **Answer:** `<FILL>`

**Q1.7 Which platforms and versions will we support?**
- *Example:* Chrome/Safari/Firefox latest 2 versions; iOS 16+; Android 10+.
- **Answer:** `<FILL>`

---

# PART 2 - GOALS AND SUCCESS DEFINITION `[ALL][P1]`

**Q2.1 What is the ONE main goal for the first 500 customers?**
- *Example:* "Reach 500 paying customers within 9 months of public launch."
- **Answer:** `<FILL>`

**Q2.2 What is your North Star Metric? (The one number that best shows users getting value.)**
- *Why:* A single shared number keeps the team aligned.
- *Example:* "Invoices paid per week."
- **Answer (SOURCE OF TRUTH):** Name: `<FILL>` | Exact formula: `<FILL>` | Time window: `<FILL>`

**Q2.3 What are your top business questions? (Write 5-10. Every event must help answer at least one.)**

| ID | Question we must be able to answer | Who asks it | Phase needed |
|---|---|---|---|
| BQ-001 | Example: Where do new visitors drop off before signing up? | Marketing | P4 |
| BQ-002 | `<FILL>` | `<FILL>` | `<FILL>` |
| BQ-003 | `<FILL>` | `<FILL>` | `<FILL>` |
| BQ-004 | `<FILL>` | `<FILL>` | `<FILL>` |
| BQ-005 | `<FILL>` | `<FILL>` | `<FILL>` |

**Q2.4 What decisions will this data change?**
- *Why:* If no decision changes, do not track it.
- *Example:* "If fewer than 40% finish onboarding, we redesign onboarding before spending on ads."
- **Answer:** `<FILL>`

---

# PART 3 - LIFECYCLE PHASES AND GATES `[ALL][P1]`

**Q3.1 What are the dates and exit rules (gates) for each phase?**
- *Why:* A gate is a simple "may we move on?" check. It stops half-measured launches.

| Phase | Start date | Target end | Analytics gate (must be true to move on) | Gate owner |
|---|---|---|---|---|
| P1 Plan | `<FILL>` | `<FILL>` | This plan is approved (Part 25) | `<FILL>` |
| P2 Build | `<FILL>` | `<FILL>` | All P2-priority events are `implemented` | `<FILL>` |
| P3 Test (QA) | `<FILL>` | `<FILL>` | 100% of critical events `verified`; no open "blocker" bugs | `<FILL>` |
| P4 Soft Launch | `<FILL>` | `<FILL>` | Data matches reality in a manual check (see Q16.6) | `<FILL>` |
| P5 Public Launch | `<FILL>` | `<FILL>` | Launch checklist (Part 18) complete; consent works | `<FILL>` |
| P6 Scale to 500 | `<FILL>` | `<FILL>` | Customer #500 reached and data-quality score stays healthy | `<FILL>` |

**Q3.2 What milestone reviews will we hold on the way to 500 customers?**

| Milestone | Customers | Review date | What we check |
|---|---|---|---|
| M1 | 10 | `<FILL>` | Are events firing for every real customer? |
| M2 | 50 | `<FILL>` | Is the funnel understandable? Any big drop-offs? |
| M3 | 100 | `<FILL>` | Retention curve shape; first cohort analysis |
| M4 | 250 | `<FILL>` | Unit economics; remove or add events |
| M5 | 500 | `<FILL>` | Full plan review; decide the next plan version |

---

# PART 4 - USERS, ACCOUNTS AND IDENTITY `[ALL][P1]`

**Q4.1 Who uses the product? (Write simple personas.)**

| ID | Persona name | Who they are | Main job to be done |
|---|---|---|---|
| PER-001 | Example: Solo Sam | Freelancer working alone | Send invoices in under 2 minutes |
| PER-002 | `<FILL>` | `<FILL>` | `<FILL>` |

**Q4.2 What is the difference between a "user" and an "account" in your product?**
- *Why:* Business products often have many users inside one paying account. Counting 500 customers requires account-level tracking.
- *Example:* "User = a person with a login. Account = a company that pays. One account has 1-50 users."
- **Answer:** `<FILL>`

**Q4.3 How do we recognise a person over time? (Identity rules - SOURCE OF TRUTH)**

| Question | Answer |
|---|---|
| ID given to a visitor before login (anonymous ID) - how created, how long it lasts? | `<FILL>` |
| ID given after login (user ID) - what value? **Must NOT be an email or phone number.** | `<FILL>` |
| ID for the account/company (account ID) | `<FILL>` |
| When do we link anonymous ID to user ID? (e.g., at sign-up and login) | `<FILL>` |
| What happens on logout? (reset the anonymous ID?) | `<FILL>` |
| What happens on shared devices? | `<FILL>` |
| How do we avoid counting the same person twice (web + mobile)? | `<FILL>` |

**Q4.4 Which users must be EXCLUDED from analytics? (Very important.)**
- *Example:* team members, test accounts, bots, QA devices, demo accounts.
- **Answer:** Rule used to detect them: `<FILL>` | Property that flags them: `is_internal_user = true`

---

# PART 5 - ANALYTICS TOOL STACK `[ALL][P1]`

**Q5.1 Which tools will we use? (Write `None` if not needed. Add rows freely.)**

| Purpose | Tool name | Owner | Plan/cost limit | Data region |
|---|---|---|---|---|
| Product analytics (events, funnels, retention) | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Web analytics / traffic | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Tag manager / event pipeline (CDP) | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Mobile analytics / attribution | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Consent management platform (CMP) | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Error / crash monitoring | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Session replay / heatmaps (optional) | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| A/B testing / feature flags | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Data warehouse | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Dashboards / BI | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| Billing / payments system | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| CRM / email / support tools | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

**Q5.2 Which events are sent from the user's device (client-side) and which from our server (server-side)?**
- *Why:* Ad blockers can hide client-side events. Money and account events should come from the server, where they are reliable.
- *Rule of thumb:* Clicks/views = client. Payments, sign-ups, subscription changes, AI usage cost = server.
- **Answer (rule for this project):** `<FILL>`

**Q5.3 Do we have separate environments?**

| Environment | Analytics project/key name | Who can see it | Used for |
|---|---|---|---|
| Development | `<FILL>` | `<FILL>` | Coding |
| Staging / Test | `<FILL>` | `<FILL>` | QA |
| Production | `<FILL>` | `<FILL>` | Real users |

*Rule:* Never mix test data into Production. Secret keys are NEVER written in this file; write only the **name** of where they are stored (e.g., "Secrets Manager: `analytics_prod_key`").

---

# PART 6 - MEASUREMENT FRAMEWORK: FUNNEL AND METRICS `[ALL][P1]`

**Q6.1 What are the steps a person takes from stranger to customer? (Your funnel - SOURCE OF TRUTH)**
- *Why:* Each step becomes one or more events.
- *Example (SaaS):* Visit site -> Start sign-up -> Verify email -> Finish onboarding -> Aha moment -> Start trial -> Pay -> Repeat use.

| Step # | Stage name | Plain-language definition | Linked event ID(s) |
|---|---|---|---|
| 1 | Acquisition | `<FILL>` | `<FILL>` |
| 2 | Activation | `<FILL>` | `<FILL>` |
| 3 | Conversion (becomes customer) | `<FILL>` | `<FILL>` |
| 4 | Retention (comes back) | `<FILL>` | `<FILL>` |
| 5 | Revenue growth (pays more) | `<FILL>` | `<FILL>` |
| 6 | Referral (tells others) | `<FILL>` | `<FILL>` |

**Q6.2 Metric dictionary - define each metric exactly once. (SOURCE OF TRUTH)**
- *Why:* "Active user" means different things to different people. Write the formula so nobody argues later.

| ID | Metric name | Exact formula | Time window | Segment/filters | Source events | Owner | Target by customer #500 |
|---|---|---|---|---|---|---|---|
| MET-001 | Visitor -> Sign-up rate | sign-ups / unique visitors | 30 days | exclude internal users | EVT-001, EVT-010 | `<FILL>` | `<FILL>` |
| MET-002 | Activation rate | users reaching Aha / users signed up | 7 days after sign-up | exclude internal | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-003 | Trial -> Paid rate | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-004 | Week-1 / Week-4 retention | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-005 | Monthly recurring revenue (MRR) | `<FILL>` | monthly | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-006 | Churn rate | `<FILL>` | monthly | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-007 | Customer acquisition cost (CAC) | `<FILL>` | monthly | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-008 | Customers count (matches Q1.5) | `<FILL>` | cumulative | `<FILL>` | `<FILL>` | `<FILL>` | 500 |
| MET-009 | North Star (matches Q2.2) | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-010 | `[AI]` AI answer helpfulness rate | thumbs-up / (thumbs-up + thumbs-down) | 7 days | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-011 | `[AI]` AI cost per active user | AI provider cost / active users | monthly | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| MET-012 | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

**Q6.3 What "guardrail" metrics must NOT get worse while we grow?**
- *Example:* Page load time, crash-free sessions, refund rate, AI error rate.
- **Answer:** `<FILL>`

**Q6.4 Minimum Viable Analytics (MVA): if we could track only 15 events at launch, which ones?**
- *Why:* Protects you from tracking everything and trusting nothing.
- **Answer (list event IDs):** `<FILL>`

---

# PART 7 - NAMING RULES (THE LANGUAGE OF THE PLAN) `[ALL][P1]`

Fill this part ONCE per organisation if a company standard exists; then copy it to every project. If no standard exists, **keep the defaults below** (recommended) and change nothing.

| Item | Rule (default) | Good example | Bad example |
|---|---|---|---|
| Event name format | `object_action` in lowercase `snake_case`, past tense | `invoice_sent` | `SendInvoice`, `click1`, `evt_1a` |
| Property name format | lowercase `snake_case` | `plan_type` | `PlanType`, `plan-type` |
| Names are... | English only, no spaces, no personal data, max 40 chars | `checkout_completed` | `John's checkout!` |
| Booleans | start with `is_` or `has_` | `is_trial` | `trial` |
| Time values | ISO 8601 in UTC; durations in milliseconds, named `_ms` | `2026-10-18T09:30:00Z` | `Oct 18` |
| Money | amount as a number in the smallest unit or decimal (choose ONE), plus `currency` ISO code | `amount: 49.00`, `currency: "USD"` | `"$49"` |
| Versions | Never put versions in event names; use `schema_version` property | `schema_version: 2` | `signup_v2` |
| Allowed values | Lists (enums) are defined in Part 10 and nothing else is accepted | `source: "google"` | `source: "Google Ads!!"` |

**Q7.1 Do we want to change any default rules?** If yes, write the new rule and the reason: `<FILL>` (otherwise write `No changes`).

**Q7.2 Which "object" words are allowed?** (Your product's nouns. Keep this list short.)
- *Example:* `account, user, invoice, project, subscription, page, screen, prompt, response, checkout`
- **Answer (SOURCE OF TRUTH):** `<FILL>`

**Q7.3 Which "action" words are allowed?**
- *Default list:* `viewed, clicked, started, completed, failed, submitted, created, updated, deleted, enabled, disabled, upgraded, downgraded, cancelled, shared, invited, received, rated`
- **Answer (changes only):** `<FILL>`

---

# PART 8 - COMMON PROPERTIES (ATTACHED TO EVERY EVENT) `[ALL][P1-P2]`

*Why:* These "free" details let you slice any chart (by device, country, plan) without extra work.

**Q8.1 Confirm or edit this standard set. (SOURCE OF TRUTH)**

| Property | Type | Required? | Example value | Set by | Notes |
|---|---|---|---|---|---|
| `event_id` | string (UUID) | Yes | `b6f1...` | Code | Unique per event; used to remove duplicates |
| `timestamp` | datetime (UTC) | Yes | `2026-10-18T09:30:00Z` | Client/Server | Time user acted |
| `anonymous_id` | string | Yes (if logged out) | `a1b2...` | SDK | See Q4.3 |
| `user_id` | string | If logged in | `usr_8841` | Code | NEVER email |
| `account_id` | string | If B2B/team | `acc_220` | Code | |
| `session_id` | string | Yes | `s_55` | SDK | |
| `platform` | enum | Yes | `web / ios / android / server` | SDK | |
| `app_version` | string | Yes | `1.4.2` | Code | |
| `environment` | enum | Yes | `production` | Config | Block test data from prod |
| `schema_version` | integer | Yes | `1` | Code | Raise when event shape changes |
| `is_internal_user` | boolean | Yes | `false` | Code | See Q4.4 |
| `locale` | string | Yes | `en-US` | SDK | |
| `country` | string (ISO) | Auto | `US` | Tool | Coarse location only |
| `consent_analytics` | boolean | Yes | `true` | CMP | No consent = event must not be sent (Part 14) |
| `consent_marketing` | boolean | Yes | `false` | CMP | |
| `experiment_variants` | object | If testing | `{"onboarding_v2":"B"}` | Code | |
| `page_url` / `screen_name` | string | `[WEB]` / `[MOBILE]` | `/pricing` | SDK | Strip tokens and emails from URLs |
| `referrer` | string | `[WEB]` | `google.com` | SDK | |
| `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`, `utm_term` | string | If present | `newsletter` | SDK | See Part 12 |
| `device_type` | enum | Auto | `mobile` | SDK | |
| `os_name` / `os_version` | string | `[MOBILE]` | `iOS 17` | SDK | |

**Q8.2 Any extra common property needed?** `<FILL>`

---

# PART 9 - EVENT CATALOG (THE HEART OF THE PLAN) `[ALL][P2-P6]`

## How to fill the catalog
1. Start from the **Funnel (Q6.1)** and **Business Questions (Q2.3)**.
2. Add **one row per event**. Give it the next ID: `EVT-001`, `EVT-002`...
3. Set **Priority:** `P0` = needed to measure the funnel/customers; `P1` = needed for launch decisions; `P2` = nice to have.
4. Set **Trigger** in plain words: *exactly when* the event fires. If two people could read it differently, rewrite it.
5. Any **new** event after approval needs a change request (Part 21).

## 9A. Master Event Table (SOURCE OF TRUTH)

| ID | Event name | Category | Plain-language trigger (fires WHEN...) | Priority | Source (client/server) | Platform | Owner | Phase to ship | Status | Answers (BQ-IDs / MET-IDs) |
|---|---|---|---|---|---|---|---|---|---|---|
| EVT-001 | `page_viewed` | Acquisition | A page finishes loading (and again on route change in single-page apps) | P0 | client | web | `<FILL>` | P2 | planned | BQ-001 |
| EVT-002 | `signup_started` | Acquisition | User clicks the sign-up button or opens the form | P0 | client | all | `<FILL>` | P2 | planned | MET-001 |
| EVT-003 | `signup_completed` | Activation | The server confirms the new account was created | P0 | server | all | `<FILL>` | P2 | planned | MET-001, MET-008 |
| EVT-004 | `login_succeeded` | Retention | Server confirms a successful login | P0 | server | all | `<FILL>` | P2 | planned | MET-004 |
| EVT-005 | `onboarding_step_completed` | Activation | User completes a step in onboarding | P1 | client | all | `<FILL>` | P2 | planned | MET-002 |
| EVT-006 | `onboarding_completed` | Activation | User finishes the final onboarding step | P0 | client | all | `<FILL>` | P2 | planned | MET-002 |
| EVT-007 | `<FILL: your Aha event>` | Activation | `<FILL>` | P0 | `<FILL>` | `<FILL>` | `<FILL>` | P2 | planned | MET-002, MET-009 |
| EVT-008 | `pricing_viewed` | Conversion | User opens the pricing page/screen | P1 | client | all | `<FILL>` | P2 | planned | MET-003 |
| EVT-009 | `checkout_started` | Conversion | User begins checkout | P0 | client | all | `<FILL>` | P2 | planned | MET-003 |
| EVT-010 | `checkout_completed` | Revenue | Payment is confirmed by the billing system | P0 | server | all | `<FILL>` | P2 | planned | MET-003, MET-005, MET-008 |
| EVT-011 | `subscription_cancelled` | Retention | Cancellation is confirmed | P0 | server | all | `<FILL>` | P2 | planned | MET-006 |
| EVT-012 | `error_displayed` | Quality | User sees an error message | P1 | client | all | `<FILL>` | P2 | planned | Guardrails |
| EVT-013 | `feedback_submitted` | Quality | User submits rating or comment | P2 | client | all | `<FILL>` | P4 | planned | BQ |
| EVT-014 | `invite_sent` | Referral | User invites someone | P2 | server | all | `<FILL>` | P4 | planned | MET |
| EVT-015 | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | planned | `<FILL>` |

*(Add rows. Keep rows in ID order. Never delete a row; set Status to `deprecated`.)*

## 9B. Event Specification Cards (one card per P0 and P1 event)

Copy this card for each event. A finished example is in Appendix B.

```
EVENT CARD
id: EVT-___
name: ___                      # follows Part 7
description: ___               # one plain sentence
trigger: ___                   # exact moment it fires
does_NOT_fire_when: ___        # edge cases (e.g., page refresh, retry, background)
source: client | server
platforms: web | ios | android | server
frequency: once-per-user | once-per-session | every-time
dedupe_rule: ___               # how repeats/retries are avoided (use event_id)
required_properties:
  - name: ___  type: ___  allowed_values: ___  example: ___
optional_properties:
  - name: ___  type: ___  allowed_values: ___  example: ___
forbidden_properties: [email, full_name, phone, free_text_with_personal_data]
consent_required: analytics | marketing | none(necessary only)
sent_to: [analytics_tool, warehouse, crm, ads]   # see Part 13
owner: ___
qa_test: ___                   # see Part 16 test case ID
status: planned
schema_version: 1
```

## 9C. `[WEB]` Web-specific events - answer these questions
- **Q9.1 Is the site a single-page app (pages change without reloading)?** If yes, `page_viewed` must fire on route changes. Answer: `<FILL>`
- **Q9.2 Which form interactions matter?** (start, field error, submit, success). Answer: `<FILL>`
- **Q9.3 Do we track outbound clicks, file downloads, video plays, scroll depth?** Answer: `<FILL>`
- **Q9.4 Cross-domain journeys?** (e.g., site on `example.com`, app on `app.example.com`, checkout on a payment site). How do we keep one visitor identity? Answer: `<FILL>`

## 9D. `[MOBILE]` Mobile-specific events - answer these questions
- **Q9.5 Which lifecycle events matter?** `app_installed, app_opened, app_backgrounded, app_updated, app_uninstalled (if available)`. Answer: `<FILL>`
- **Q9.6 Which permission events matter?** `push_permission_requested, push_permission_granted/denied, tracking_permission_*`. Answer: `<FILL>`
- **Q9.7 What happens when the phone is offline?** (events queued and sent later? with original time?) Answer: `<FILL>`
- **Q9.8 How do we handle app updates when old versions still send old events?** Answer: `<FILL>`
- **Q9.9 Deep links, push notifications, and app-store attribution - how are they tracked?** Answer: `<FILL>`

## 9E. `[SITE]` Marketing site / e-commerce events - answer these questions
- **Q9.10 Which product-browsing events do we need?** `product_list_viewed, product_viewed, product_searched, product_filtered`. Answer: `<FILL>`
- **Q9.11 Which cart/checkout events do we need?** `cart_item_added, cart_item_removed, cart_viewed, checkout_started, shipping_info_submitted, payment_info_submitted, order_completed, order_refunded, coupon_applied`. Answer: `<FILL>`
- **Q9.12 Which "lead" events do we need?** `lead_form_submitted, demo_requested, newsletter_subscribed, pricing_calculator_used`. Answer: `<FILL>`
- **Q9.13 Standard product properties** (`product_id, product_name, category, price, currency, quantity, variant`): changes? Answer: `<FILL>`

## 9F. `[AI]` AI-feature events - answer these questions
*Why:* AI features cost money per use, can be wrong, and need quality tracking, not only click tracking.

| ID | Event name | Fires when | Key properties | Forbidden in properties |
|---|---|---|---|---|
| EVT-A01 | `ai_prompt_submitted` | User sends a request to an AI feature | `feature_name, input_type, input_length_chars, model_name, model_version, prompt_template_id` | Raw prompt text if it may contain personal data |
| EVT-A02 | `ai_response_received` | AI answer is shown | `latency_ms, output_length_chars, tokens_in, tokens_out, cost_usd, finish_reason, safety_filter_triggered, fallback_used` | Raw response text unless approved |
| EVT-A03 | `ai_response_failed` | AI call errors or times out | `error_type, latency_ms, retry_count` | Stack traces with personal data |
| EVT-A04 | `ai_feedback_given` | User rates the answer | `rating (up/down), reason_code` | Free text with personal data |
| EVT-A05 | `ai_output_used` | User accepts, copies, or applies the output | `action (accepted/edited/copied/discarded), edit_distance_bucket` | |
| EVT-A06 | `ai_agent_task_completed` | An AI agent finishes a multi-step task | `steps_count, tools_used_count, success, duration_ms, human_handoff` | |
| EVT-A07 | `ai_limit_reached` | User hits usage cap/paywall | `limit_type, plan_type` | |

- **Q9.14 Will we store prompts/responses?** Yes/No. If yes: where, who can read, for how many days, is it anonymised? Answer: `<FILL>`
- **Q9.15 How do we measure answer quality?** (thumbs, edits, repeat questions, human review sample). Answer: `<FILL>`
- **Q9.16 What is the budget alert for AI cost per user per month?** Answer: `<FILL>`
- **Q9.17 How do we tag which model and prompt version produced each answer?** (Needed to compare versions.) Answer: `<FILL>`
- **Q9.18 Do we need to disclose AI usage to users and record consent for using their data to improve AI?** Answer: `<FILL>`

---

# PART 10 - PROPERTY AND VALUE DICTIONARY `[ALL][P2]`

*Why:* The same property must mean the same thing in every event. Lists of allowed values prevent messy data ("Pro", "pro", "PRO").

**Q10.1 Property dictionary (SOURCE OF TRUTH)**

| Property | Type | Allowed values / format | Description | Used in events | PII? (Y/N) |
|---|---|---|---|---|---|
| `plan_type` | enum | `free, trial, starter, pro, enterprise` | Plan at the time of event | EVT-009, EVT-010 | N |
| `signup_method` | enum | `email, google, apple, sso, other` | How the user signed up | EVT-003 | N |
| `cancel_reason` | enum | `too_expensive, missing_feature, not_using, switched_tool, other` | | EVT-011 | N |
| `amount` | number | decimal, >= 0 | | EVT-010 | N |
| `currency` | string | ISO 4217 (`USD`, `EUR`) | | EVT-010 | N |
| `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

**Q10.2 Who may add a new allowed value?** `<FILL: usually Data Lead>`

---

# PART 11 - USER AND ACCOUNT PROPERTIES `[ALL][P2]`

*Why:* These are facts that describe a person/company (not a single action). They let us group users into segments.

| Property | Level (user/account) | Type | Example | When updated | PII? | Source |
|---|---|---|---|---|---|---|
| `signup_date` | user | date | `2026-10-18` | once | N | server |
| `plan_type` | account | enum | `pro` | on change | N | billing |
| `is_customer` | account | boolean | `true` | on first payment | N | billing |
| `customer_since` | account | date | | on first payment | N | billing |
| `industry` | account | enum | `design` | on onboarding | N | form |
| `team_size_bucket` | account | enum | `2-10` | on onboarding | N | form |
| `acquisition_channel` | user | enum | `organic_search` | at signup | N | attribution |
| `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

**Q11.1 Which user segments do we need to compare?** *(Example: new vs returning; free vs paid; mobile vs web; by country; by acquisition channel.)* Answer: `<FILL>`

---

# PART 12 - ATTRIBUTION AND MARKETING TRACKING `[WEB][SITE][MOBILE][P2-P6]`

**Q12.1 How will we know where each customer came from?**
- *Why:* Needed to decide where to spend money before customer #500.
- **Answer:** Channels used: `<FILL>` (e.g., organic search, paid ads, email, social, referral, partners, app stores)

**Q12.2 UTM / campaign naming rules (SOURCE OF TRUTH)**

| Field | Rule | Allowed examples |
|---|---|---|
| `utm_source` | lowercase platform name | `google, linkedin, newsletter` |
| `utm_medium` | channel type | `cpc, email, social, referral, affiliate` |
| `utm_campaign` | `yyyymm_short-name` | `202611_launch-promo` |
| `utm_content` | creative or variant | `video_a` |
| `utm_term` | keyword (paid search) | `invoice-app` |

**Q12.3 Attribution model for reports:** First touch / Last touch / Both. Window length (days): `<FILL>`

**Q12.4 What do we send to ad platforms and how do we respect consent?** (e.g., purchase conversions only, hashed, only if `consent_marketing = true`). Answer: `<FILL>`

**Q12.5 `[MOBILE]` Which attribution/install tools and privacy frameworks apply (e.g., iOS app-tracking prompts)?** Answer: `<FILL>`

---

# PART 13 - DATA FLOW AND DESTINATIONS `[ALL][P2]`

**Q13.1 Draw (or describe) how data travels from the user to a dashboard.**
- *Example:* User device -> Event SDK -> Event pipeline -> (Analytics tool, Data warehouse, CRM) -> Dashboard.
- **Answer (diagram link or text):** `<FILL>`

**Q13.2 Which event goes to which tool? (SOURCE OF TRUTH)**
- *Rule:* Not every event needs to go everywhere. Send the minimum.

| Event ID | Analytics tool | Warehouse | CRM/Email | Ad platforms | Error tool |
|---|---|---|---|---|---|
| EVT-003 | Yes | Yes | Yes | No | No |
| EVT-010 | Yes | Yes | Yes | Yes (conversion only) | No |
| `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

**Q13.3 Rules for handling problems**
- Duplicate events: dropped using `event_id` -> `<FILL: confirm>`
- Late/offline events: accepted up to `<FILL>` days using original `timestamp`.
- Events that break the plan (unknown event or bad property): **blocked / quarantined / allowed-with-warning** -> `<FILL>`
- Retries after network failure: `<FILL>`

**Q13.4 Which data is the "official record" for money and customer counts?** (Must be the billing system, not the analytics tool.) Answer: `<FILL>`

---

# PART 14 - PRIVACY, CONSENT AND COMPLIANCE `[ALL][P1-P6]`

> This is not legal advice. Have your Privacy/Legal person review and sign Part 25. **Collect the least data you can. When in doubt, don't collect it.**

**Q14.1 Which rules apply to us? (Tick all that apply.)**
- [ ] **GDPR / ePrivacy** (users in the EU/EEA/UK): consent before non-essential tracking, rights to access/delete.
- [ ] **CCPA / CPRA** (California): notice, opt-out of "sale/sharing", honor opt-out signals.
- [ ] **COPPA / children's data** (under 13 in the US; check local age limits elsewhere): do not track children without verified parental consent.
- [ ] **HIPAA** (US health data) / **SOC 2** / other sector rules (finance, education, etc.): `<FILL which>`
- [ ] Other country laws: `<FILL>`

**Q14.2 What personal data do we collect, why, and is it needed? (SOURCE OF TRUTH)**

| Data item | Why we need it | Legal basis (consent / contract / legitimate interest) | Stored where | Retention (days) | Allowed in analytics? |
|---|---|---|---|---|---|
| Email | Account & billing | Contract | App database | `<FILL>` | **No** (hash only if approved) |
| IP address | Coarse location | `<FILL>` | `<FILL>` | `<FILL>` | Truncate/anonymise |
| Device ID | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |
| `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

**Q14.3 FORBIDDEN data (never in events, properties, URLs, or screenshots).**
- Default list: passwords, full card numbers, government IDs, health details, exact precise location, full names, raw emails/phones, access tokens, private messages, free-text fields a user can type into (unless scrubbed).
- Additional forbidden items for this project: `<FILL>`

**Q14.4 Consent rules**

| Question | Answer |
|---|---|
| Which tool collects consent (CMP)? | `<FILL>` |
| Which categories exist? (necessary / analytics / marketing / personalisation) | `<FILL>` |
| What is blocked BEFORE consent? (default: all analytics and marketing events) | `<FILL>` |
| What happens if the user says "no"? (no identifiers, no events, or only anonymous counts) | `<FILL>` |
| How can a user change their mind later? (link/button location) | `<FILL>` |
| How do we honor browser opt-out signals (e.g., Global Privacy Control)? | `<FILL>` |
| `[MOBILE]` How is the OS tracking permission handled? | `<FILL>` |
| `[AI]` Is use of user content for model improvement opt-in? | `<FILL>` |
| How long do we keep consent records? | `<FILL>` |

**Q14.5 Children and age rules:** Minimum age for the product: `<FILL>`. How do we prevent tracking below that age? `<FILL>`

**Q14.6 User rights process (access, delete, correct, opt-out)**
- Who receives requests? `<FILL>`
- How do we find a person's analytics data? (which ID?) `<FILL>`
- How do we delete it from the analytics tool, warehouse, CRM, and backups? `<FILL>`
- Time limit to complete: `<FILL>` days (check the law that applies)

**Q14.7 Where is data stored (country/region), and who are our vendors/processors?** Do we have signed data-processing agreements? `<FILL>`

**Q14.8 Security basics**
- Who can see raw events? `<FILL>` | Who can export? `<FILL>`
- Access is reviewed every `<FILL>` days.
- Keys/secrets are stored in: `<FILL>` (never in code or this file).
- `[HIPAA/SOC 2 only]` Audit logging, encryption, and breach-notification process: `<FILL>`

---

# PART 15 - IMPLEMENTATION PLAN (AI-DRIVEN DEVELOPMENT) `[ALL][P2]`

**Q15.1 Where does the tracking code live?** (one central "analytics wrapper" file, not scattered calls)
- *Rule:* All events must be sent through ONE function (e.g., `track(eventName, properties)`) that checks consent, adds common properties, and validates against this plan.
- **Answer (repo path / module name):** `<FILL>`

**Q15.2 How does an AI coding agent get its instructions?**
- Fill this table, then paste the "Agent Brief" (Appendix C) into your AI tool.

| Item | Answer |
|---|---|
| Machine-readable plan file path (e.g., `analytics/tracking-plan.yaml`) generated from Part 9 | `<FILL>` |
| Languages / frameworks | `<FILL>` |
| Where tests live | `<FILL>` |
| Which AI agents/tools are allowed to edit analytics code | `<FILL>` |
| Human approval needed before merge? | Yes - by `<FILL>` |

**Q15.3 Agent guardrails (defaults - edit only if needed)**
1. The agent may only implement events with Status `planned` and Priority matching the current phase.
2. The agent must not invent events, properties, or values. Unknown -> ask a human.
3. The agent must add or update a test for every event it implements.
4. The agent must never log or send forbidden data (Q14.3).
5. The agent must update the event Status and the Change Log in this file.

**Q15.4 Implementation task list (one row per event or group)**

| Task ID | Event ID(s) | Description | Assignee (human/agent) | Phase | Definition of done | Status |
|---|---|---|---|---|---|---|
| IMP-001 | EVT-001..004 | Core acquisition events | `<FILL>` | P2 | Fires on staging; unit test passes; QA case passes | not-started |
| IMP-002 | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | not-started |

**Q15.5 Feature-development rule:** *No feature is "done" until its tracking is built and verified.* Where is this written into your team's "Definition of Done"? `<FILL>`

---

# PART 16 - QUALITY ASSURANCE (TESTING THE TRACKING) `[ALL][P3-P4]`

**Q16.1 Test types we will run (tick all that apply and name an owner)**
- [ ] Unit tests: the right event and properties are built in code - Owner: `<FILL>`
- [ ] Schema validation: event matches Part 9/10 automatically - Owner: `<FILL>`
- [ ] Manual walkthrough: a human performs the user journey and watches events arrive - Owner: `<FILL>`
- [ ] Consent tests: with "No", nothing non-essential is sent - Owner: `<FILL>`
- [ ] Cross-device tests (web, iOS, Android, browsers) - Owner: `<FILL>`
- [ ] Ad-blocker / offline / slow-network tests - Owner: `<FILL>`
- [ ] Reconciliation: analytics numbers vs billing/database numbers - Owner: `<FILL>`

**Q16.2 Test case table (SOURCE OF TRUTH)**

| Test ID | Event ID | Steps (plain words) | Expected result | Platform | Tester | Date | Pass/Fail | Bug link |
|---|---|---|---|---|---|---|---|---|
| QA-001 | EVT-003 | 1) Open sign-up. 2) Enter a test email. 3) Submit. | `signup_completed` arrives ONCE with `signup_method` set and no email | web | `<FILL>` | `<FILL>` | `<FILL>` | |
| QA-002 | EVT-010 | Buy with a test card | `checkout_completed` arrives once from the server; amount matches billing | all | `<FILL>` | `<FILL>` | `<FILL>` | |
| QA-003 | All | Refuse consent, then browse | Zero analytics events sent | web | `<FILL>` | `<FILL>` | `<FILL>` | |
| QA-004 | EVT-001 | Refresh a page | One `page_viewed` per load, no duplicates | web | `<FILL>` | `<FILL>` | `<FILL>` | |
| QA-005 | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | |

**Q16.3 What is a "pass"?** Default: right name, right trigger, all required properties present and correctly typed, no forbidden data, no duplicates, arrives in the correct environment, delay under `<FILL>` minutes.

**Q16.4 Severity levels** - Blocker: money/customer events wrong or privacy leak (stop launch). Major: funnel event missing. Minor: optional property wrong.

**Q16.5 Coverage rule:** 100% of P0 events verified before P5; at least `<FILL>`% of P1.

**Q16.6 Soft-launch reality check `[P4]`:** For the first `<FILL>` real users, a person manually compares the product's database with analytics. Differences allowed: under `<FILL>`%. Result: `<FILL>`

---

# PART 17 - DASHBOARDS AND REPORTING `[ALL][P4-P6]`

**Q17.1 Which dashboards do we need? (SOURCE OF TRUTH)**

| ID | Dashboard | Audience | Questions answered | Metrics | Refresh | Owner | Link |
|---|---|---|---|---|---|---|---|
| DSH-001 | Launch health | Whole team | Is tracking working today? | event volume, error rate, consent rate | Hourly | `<FILL>` | |
| DSH-002 | Funnel | Product/Marketing | Where do we lose people? | MET-001..003 | Daily | `<FILL>` | |
| DSH-003 | Path to 500 | Leadership | How close are we to 500 customers? | MET-008, MET-005, MET-009 | Daily | `<FILL>` | |
| DSH-004 | Retention & cohorts | Product | Do people come back? | MET-004, MET-006 | Weekly | `<FILL>` | |
| DSH-005 | Acquisition channels | Marketing | Which channel brings customers cheaply? | MET-007 | Weekly | `<FILL>` | |
| DSH-006 | `[AI]` AI quality & cost | Product/Eng | Is AI good and affordable? | MET-010, MET-011 | Daily | `<FILL>` | |

**Q17.2 Reporting rhythm:** Daily check `<FILL>`; weekly review `<FILL>`; milestone reviews at 10/50/100/250/500 customers (Q3.2).

**Q17.3 Which alerts notify us? (Examples: event volume drops by more than 30% vs same day last week; zero `signup_completed` in 2 hours; AI cost above budget.)**

| Alert | Rule | Channel | Who is paged | Runbook (Part 20) |
|---|---|---|---|---|
| `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

---

# PART 18 - LAUNCH READINESS CHECKLISTS `[ALL][P3-P5]`

**Q18.1 Soft-launch (P4) checklist - all must be "Yes" or have a written reason.**
- [ ] All P0 events `verified` on staging AND production
- [ ] Test and internal users are excluded
- [ ] Consent banner works on web and mobile
- [ ] Launch-health dashboard (DSH-001) is live
- [ ] Alerts are on and tested
- [ ] Rollback plan exists (how to switch tracking off safely)
- [ ] Support team knows where to ask analytics questions

**Q18.2 Public-launch (P5) checklist**
- [ ] Soft-launch data matches reality (Q16.6)
- [ ] Billing numbers reconcile with analytics
- [ ] Privacy policy updated and published
- [ ] Data-processing agreements signed with vendors
- [ ] Deletion request process tested end-to-end
- [ ] Ad and campaign tracking (UTMs, conversions) tested
- [ ] Load expectations checked (event volume, cost limits)
- [ ] Final sign-off in Part 25

---

# PART 19 - EXPERIMENTS AND LEARNING `[ALL][P4-P6]`

**Q19.1 Will we run A/B tests or feature flags before 500 customers?** Yes/No. Tool: `<FILL>`
**Q19.2 For each experiment, fill this table.**

| Exp ID | Hypothesis ("If we..., then..., because...") | Variant property name | Primary metric | Guardrail metric | Minimum sample | Start | End | Decision |
|---|---|---|---|---|---|---|---|---|
| EXP-001 | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

*Note:* With very few customers (under 500), tests are often underpowered. Prefer qualitative research plus before/after comparisons, and say so in the decision.

**Q19.3 Who has the final say when data is unclear?** `<FILL>`

---

# PART 20 - DATA QUALITY MONITORING AND INCIDENT RUNBOOK `[ALL][P4-P6]`

**Q20.1 Daily data-quality checks (write who checks and how)**
- [ ] Event volume vs normal: `<FILL>`
- [ ] New unknown events or properties appeared: `<FILL>`
- [ ] Required properties missing > `<FILL>`%: `<FILL>`
- [ ] Duplicate rate > `<FILL>`%: `<FILL>`
- [ ] Money/customer counts match billing: `<FILL>`
- [ ] Consent rate unexpectedly dropped: `<FILL>`

**Q20.2 Incident steps (default - edit as needed)**

| Step | Action | Owner |
|---|---|---|
| 1 | Detect (alert or person) and log an incident ID `INC-___` | `<FILL>` |
| 2 | Decide severity (Q16.4) and notify owners | `<FILL>` |
| 3 | Stop the damage (turn off the bad event or fix) | `<FILL>` |
| 4 | Fix root cause; add a test so it can't happen again | `<FILL>` |
| 5 | Repair bad data (backfill, filter, or flag the date range) | `<FILL>` |
| 6 | Tell dashboard users which dates are affected | `<FILL>` |
| 7 | Write a short summary in Part 22 | `<FILL>` |

**Q20.3 Data quality score (optional):** Formula and healthy range: `<FILL>`

---

# PART 21 - GOVERNANCE, CHANGES AND VERSIONING `[ALL][P2-P6]`

**Q21.1 How do changes to this plan work? (Defaults below. Edit only if needed.)**
1. Anyone may **request** a change (new/changed event or property) in `<FILL: tracker/link>`.
2. The Plan Owner checks: *Does it answer a business question (Part 2)? Is it named per Part 7? Is it allowed by Part 14?*
3. Data Lead approves names; Engineering Lead approves effort; Privacy approves personal data.
4. Update Parts 9-11, bump `plan_version`, add a Change Log row (Appendix D).
5. Ship code and tests together. Status moves `planned -> implemented -> verified -> live`.

**Q21.2 Version numbering:** `MAJOR.MINOR.PATCH` - MAJOR = breaking change to existing events; MINOR = new events/properties; PATCH = wording fixes.

**Q21.3 How do we retire an event?** Mark `deprecated`, keep sending until `<FILL>` date, tell dashboard owners, then stop sending. **Never reuse an old name or ID for a new meaning.**

**Q21.4 Who reviews the whole plan, and how often?** `<FILL>` (suggest: every 30 days until customer #500, then every quarter).

**Q21.5 Roles in plain words (RACI)**

| Task | Product | Engineering | Data | QA | Privacy | Marketing |
|---|---|---|---|---|---|---|
| Decide what to measure | A/R | C | C | I | C | C |
| Name events and properties | C | C | A/R | I | I | C |
| Build tracking | C | A/R | C | C | I | I |
| Test tracking | I | C | C | A/R | I | I |
| Approve privacy | I | I | C | I | A/R | C |
| Build dashboards | C | I | A/R | I | I | C |

*(R = does the work, A = final say, C = consulted, I = informed.)*

---

# PART 22 - RISKS, ASSUMPTIONS AND DEPENDENCIES `[ALL][P1-P6]`

| ID | Type | Description | Impact (L/M/H) | Likelihood (L/M/H) | What we will do | Owner | Status |
|---|---|---|---|---|---|---|---|
| RSK-001 | Risk | Ad blockers hide client events, so web sign-ups look lower than reality | M | H | Send money/account events from the server | `<FILL>` | open |
| RSK-002 | Risk | Consent refusal lowers visible traffic | M | H | Use server-side counts for official numbers | `<FILL>` | open |
| RSK-003 | Risk | Event names drift as new people join | M | M | Enforce Part 7 with automated checks | `<FILL>` | open |
| RSK-004 | Assumption | Billing system is the source of truth for customer count | H | L | Reconcile weekly | `<FILL>` | open |
| RSK-005 | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | open |

**Incident summaries (from Part 20):** `<FILL or "None yet">`

---

# PART 23 - OPEN QUESTIONS AND DECISIONS LOG `[ALL][P1-P6]`

| ID | Question or decision | Why it matters | Owner | Due date | Answer / decision | Date decided |
|---|---|---|---|---|---|---|
| OQ-001 | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` | `<FILL>` |

*AI agents: put every unanswered question here instead of guessing.*

---

# PART 24 - FINAL CHECKLIST ("IS THIS DOCUMENT PERFECT?")

Tick each box. If any box is unticked, the document is **not ready**.

**Completeness**
- [ ] No `<FILL>` markers remain (each is answered, `TBD (owner, date)`, or `N/A - reason`)
- [ ] Customer is defined (Q1.5) and North Star formula is written (Q2.2)
- [ ] Every metric has an exact formula, window, and owner (Q6.2)
- [ ] Every event has an ID, trigger, owner, status, and links to a question or metric (Part 9)
- [ ] Every P0/P1 event has an Event Card (9B)
- [ ] All allowed values are listed (Part 10)

**Clarity (fewer reasons to guess)**
- [ ] A new team member can explain each event's trigger without asking
- [ ] No vague words ("some", "often", "soon", "etc.") remain
- [ ] Every date is written as `YYYY-MM-DD` and every person is named

**Safety and trust**
- [ ] No forbidden data in any event or property (Q14.3)
- [ ] Consent behavior is defined for web, mobile, and AI features
- [ ] Deletion process exists (Q14.6)
- [ ] Money and customer counts reconcile with billing (Q13.4, Q16.2)

**Execution**
- [ ] QA tests exist for all P0 events (Part 16)
- [ ] Dashboards and alerts are defined (Part 17)
- [ ] Launch checklists are complete for the current phase (Part 18)
- [ ] Review rhythm is scheduled to customer #500 (Q3.2, Q21.4)

---

# PART 25 - SIGN-OFF

| Role | Name | Decision (Approved / Changes requested) | Date | Notes |
|---|---|---|---|---|
| Product Lead | `<FILL>` | `<FILL>` | `<FILL>` | |
| Engineering Lead | `<FILL>` | `<FILL>` | `<FILL>` | |
| Data / Analytics Lead | `<FILL>` | `<FILL>` | `<FILL>` | |
| QA Lead | `<FILL>` | `<FILL>` | `<FILL>` | |
| Privacy / Legal | `<FILL>` | `<FILL>` | `<FILL>` | |

---

# APPENDIX A - GLOSSARY (PLAIN WORDS)

| Word | Meaning |
|---|---|
| Event | One thing a user or system did, at one moment (e.g., "invoice sent") |
| Property | An extra detail about an event or person (e.g., "plan = pro") |
| User property | A detail about a person that stays until changed |
| Funnel | The steps from stranger to customer; we count how many pass each step |
| Cohort | A group of people who started in the same week/month |
| Retention | How many people come back after a few days or weeks |
| Churn | People or accounts who stop paying or using |
| Activation / Aha moment | The first time a user gets real value |
| North Star Metric | The one number that best shows value delivered |
| Client-side / Server-side | Sent from the user's device / sent from our own servers |
| SDK | A small code package that sends events to a tool |
| Consent | The user's permission to be tracked |
| PII | Personally identifiable information: data that can point to one person |
| CMP | Consent management platform: the banner/tool that collects consent |
| UTM | Tags added to links to show which campaign sent the visitor |
| Schema | The agreed shape of an event: its name, properties, and types |
| Deduplication | Removing repeated copies of the same event |
| Source of truth | The one place everyone trusts when numbers disagree |
| MVA | Minimum Viable Analytics: the smallest set of events that still answers the key questions |
| Gate | A checkpoint that must pass before moving to the next phase |

---

# APPENDIX B - FINISHED EXAMPLE EVENT CARD

```
EVENT CARD
id: EVT-003
name: signup_completed
description: A new account was successfully created.
trigger: The server saves the new account and returns success.
does_NOT_fire_when: The form is submitted but validation fails; the user refreshes the success page; an existing user logs in.
source: server
platforms: web, ios, android
frequency: once-per-user
dedupe_rule: One event per user_id; event_id sent with each retry.
required_properties:
  - name: signup_method  type: enum  allowed_values: [email, google, apple, sso, other]  example: "google"
  - name: plan_type      type: enum  allowed_values: [free, trial]  example: "trial"
  - name: acquisition_channel type: enum  allowed_values: [organic_search, paid_search, social, email, referral, direct, other]  example: "referral"
optional_properties:
  - name: referral_code  type: string  allowed_values: "6 uppercase letters"  example: "ABCDEF"
forbidden_properties: [email, full_name, phone, password]
consent_required: none(necessary only)  # account creation is a core service event; analytics copy follows consent rules
sent_to: [analytics_tool, warehouse, crm]
owner: Priya
qa_test: QA-001
status: planned
schema_version: 1
```

---

# APPENDIX C - AGENT BRIEF (COPY-PASTE FOR AI CODING/QA AGENTS)

```
You are implementing analytics tracking for <PROJECT NAME>.
Source of truth: Analytics_Tracking_Plan.md (this file). Read Parts 4, 7, 8, 9, 10, 13, 14 and 16 first.

Rules:
1. Implement ONLY events with status "planned" and priority P0 (or the priority I tell you).
2. Send every event through the single wrapper at <PATH>. Do not call analytics SDKs directly elsewhere.
3. Use exact event names, property names, types and allowed values from Parts 9-10. Do not invent any.
4. Never send forbidden data (Part 14, Q14.3). Check consent before sending (Part 14, Q14.4).
5. Money and account events are sent from the server (Part 5, Q5.2).
6. Add a unit test per event and map it to its QA ID in Part 16.
7. If anything is TBD, unclear, or contradictory, STOP and add it to Part 23 as an open question. Do not guess.
8. When done, list: events implemented, files changed, tests added, and open questions.
   Then update event statuses and the Change Log (Appendix D).
```

---

# APPENDIX D - CHANGE LOG

| Version | Date | Author | What changed | Why | Approved by |
|---|---|---|---|---|---|
| 0.1.0 | YYYY-MM-DD | `<FILL>` | First draft from template v1.0.0 | Project start | `<FILL>` |

---

# APPENDIX E - TEMPLATE MAINTAINER NOTES (DELETE THIS APPENDIX IN PROJECT COPIES)

- Template version: **1.0.0**. Keep the header `template_version` unchanged in project copies so you can see which template each project started from.
- To reuse across many projects: copy the file, rename the project, fill the header, then work through Parts 0-25 in order.
- Keep Parts 7, 8, 14, 20, and 21 identical across projects where possible so that data stays comparable and governance stays consistent.
- Improve the template only through a versioned change here (MAJOR.MINOR.PATCH) and note it in a template change log.
