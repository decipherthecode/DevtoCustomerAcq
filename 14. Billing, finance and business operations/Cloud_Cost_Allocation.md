# How to Fill This Document (Read This First)

**Template name:** Cloud Cost Allocation
**Folder:** Billing, Finance and Business Operations
**Template version:** 1.0
**Covers:** Idea → Build → Test → Launch → Customer 1 → Customer 500
**Cloud services covered:** AWS, Microsoft Azure, Google Cloud, Cloudflare, AI and SaaS APIs

---

## What is this document for?

Every project spends money on cloud services (servers, storage, AI, networking). This document answers four simple questions, and it answers them **before** the money is spent:

1. **Who** is spending the money?
2. **What** are they spending it on?
3. **How much** is allowed, and who says "stop"?
4. **How much does each customer cost us** (up to our first 500 customers)?

If you fill every blank, nobody has to guess later. That is the whole goal.

---

## The 10 Golden Rules

1. **Answer every question.** Do not skip any. If you truly do not know, write `TBD | Owner: <name> | Due: <date>`. Never leave a blank.
2. **Write in plain words.** If a 10-year-old cannot understand your answer, rewrite it.
3. **Use numbers, not feelings.** Write `$250 per month`, not `a small amount`.
4. **Always write the unit.** Money needs a currency (`USD`), time needs a period (`per month`), and size needs a unit (`GB`).
5. **Always write a name.** "The team" is not an owner. A person's name is.
6. **Never write passwords, API keys, card numbers or secret tokens in this file.** Write where they are stored instead (for example "Stored in 1Password, vault: Billing").
7. **Do not delete the examples.** Write your answer on the `ANSWER:` line. Keep the example so the next person understands.
8. **Dates use one format:** `YYYY-MM-DD` (example: `2026-10-19`).
9. **One project = one copy of this file.** Never mix two projects in one file.
10. **When something changes, update the Change Log (Part 15).** Do not silently overwrite.

---

## How to read the symbols

| Symbol | Meaning |
|---|---|
| `ANSWER:` | Write your answer on this line. |
| `Example:` | A sample answer. Do not copy it unless it is true for your project. |
| `[ ]` | A checkbox. Change it to `[x]` to tick it. |
| `REQUIRED` | You must answer before the project moves to the next phase. |
| `OPTIONAL` | Answer it if it applies. If it does not apply, write `N/A because <reason>`. |
| `TBD` | Unknown for now. Must have an owner and a due date. |
| `$` | Money. Replace with your currency if you do not use USD. |

---

## How to fill it in (step by step)

| Step | What to do | Time needed |
|---|---|---|
| 1 | Fill **Document Control** and **Part 1 (Project Basics)** | 10 min |
| 2 | List every service you will pay for in **Part 2** | 20 min |
| 3 | Name people in **Part 3** | 10 min |
| 4 | Set money rules in **Part 4** | 20 min |
| 5 | Set tags in **Part 5** | 15 min |
| 6 | Choose how costs are split in **Part 6** | 20 min |
| 7 | Set up cost per customer in **Part 7** | 30 min |
| 8 | Fill each lifecycle phase in **Part 8** (do Phase 1 now, others as you reach them) | 15 min per phase |
| 9 | Set AI agent rules in **Part 9** | 20 min |
| 10 | Set the review routine in **Part 10** | 10 min |
| 11 | Tick the saving ideas in **Part 11** | 10 min |
| 12 | Write risks in **Part 12** | 15 min |
| 13 | Run the **Quality Checklist (Part 13)**, then collect signatures in **Part 14** | 15 min |

**When to fill which part**

- **Before you spend any money:** Document Control, Parts 1 to 7, Part 8 Phase 1, Parts 9 and 10.
- **At the start of each new phase:** the matching block in Part 8.
- **Every week and every month:** Part 10 routine.
- **Whenever something changes:** Part 15 Change Log.

---

## What "done" looks like

This document is finished and safe to use when:

- [ ] Every `REQUIRED` question has a real answer (no empty lines).
- [ ] Every `TBD` has an owner and a due date.
- [ ] Every service in Part 2 has an owner and a monthly limit.
- [ ] The Quality Checklist (Part 13) is 100% ticked.
- [ ] The Approver has signed in Part 14.

---

# Document Control

| Field | ANSWER |
|---|---|
| Project name | |
| Project code (short, no spaces, e.g. `acme-notes`) | |
| Document owner (one person) | |
| Document created on | |
| Last updated on | |
| Current phase (1 to 6, see Part 8) | |
| Status | [ ] Draft  [ ] In review  [ ] Approved  [ ] Retired |
| Where this file is stored (link or folder) | |
| Billing currency used everywhere | |

---

# Part 0: Quick Summary for Humans and AI Agents

> Fill this part **last**, after all other parts are done. It must be short and must match the rest of the file. AI agents read this block first.

```
PROJECT_CODE:
CURRENT_PHASE:
MONTHLY_BUDGET_TOTAL (currency):
TRAFFIC_LIGHT_YELLOW_AT (% of budget):
TRAFFIC_LIGHT_RED_AT (% of budget):
BUDGET_OWNER:
CLOUD_PROVIDERS_USED:
REQUIRED_TAGS:
SHARED_COST_METHOD:
COST_PER_CUSTOMER_TARGET (currency):
CUSTOMERS_NOW:
CUSTOMERS_TARGET: 500
AI_AGENT_MONTHLY_SPEND_LIMIT (currency):
WHO_TO_CALL_IF_RED:
```

Example:

```
PROJECT_CODE: acme-notes
CURRENT_PHASE: 2
MONTHLY_BUDGET_TOTAL: USD 800
TRAFFIC_LIGHT_YELLOW_AT: 70
TRAFFIC_LIGHT_RED_AT: 90
BUDGET_OWNER: Maria Lopez
CLOUD_PROVIDERS_USED: AWS, Cloudflare, Anthropic API
REQUIRED_TAGS: project, owner, environment, phase, cost-center
SHARED_COST_METHOD: by usage
COST_PER_CUSTOMER_TARGET: USD 3.50 per month
CUSTOMERS_NOW: 0
CUSTOMERS_TARGET: 500
AI_AGENT_MONTHLY_SPEND_LIMIT: USD 150
WHO_TO_CALL_IF_RED: Maria Lopez, +1-555-0100
```

---

# Part 1: Project Basics

**1.1 In one sentence, what does this product do?** `REQUIRED`
Example: "A notes app that turns voice recordings into tidy summaries."
ANSWER:

**1.2 Who are the customers?** `REQUIRED`
Example: "Freelancers and small business owners."
ANSWER:

**1.3 What is the total money you can spend on cloud and AI services from now until customer number 500?** `REQUIRED`
Example: "USD 12,000 in total."
ANSWER:

**1.4 Where does that money come from?** `REQUIRED`
- [ ] Own savings
- [ ] Investor money
- [ ] Company profit
- [ ] Customer revenue
- [ ] Grant or credits (e.g. cloud startup credits)
- [ ] Other: ______

**1.5 Do you have free cloud credits?** `REQUIRED`
- [ ] No
- [ ] Yes. Fill the table below.

| Provider | Credit amount | Expires on | Who tracks it |
|---|---|---|---|
| | | | |

**1.6 What is the planned date for each milestone?** `REQUIRED`

| Milestone | Planned date | Real date (fill later) |
|---|---|---|
| Build starts | | |
| First test version ready | | |
| Launch to public | | |
| First paying customer | | |
| Customer 100 | | |
| Customer 500 | | |

**1.7 How will customers pay you?** (tick all that apply) `REQUIRED`
- [ ] Monthly subscription
- [ ] Usage-based (they pay for what they use)
- [ ] Free plan plus paid plan
- [ ] One-time purchase

**1.8 What is the price you charge?** `REQUIRED`

| Plan name | Price | How often (month, year, one time, per use) | Expected number of customers on this plan |
|---|---|---|---|
| | | | |

**1.9 Which customers are free (free plan, trial, demo accounts, employees)?** `REQUIRED`
Example: "Free plan users: about 70% of all sign-ups. Trials last 14 days."
ANSWER:

---

# Part 2: Service Inventory (Everything You Pay For)

> **Why this matters:** You cannot control what you cannot see. List **every** service that sends you a bill, even a tiny one.

**2.1 Which providers do you use?** `REQUIRED`
- [ ] AWS
- [ ] Microsoft Azure
- [ ] Google Cloud
- [ ] Cloudflare
- [ ] AI model APIs (e.g. Anthropic, OpenAI, Google)
- [ ] Hosting or app platforms (e.g. Vercel, Supabase, Netlify)
- [ ] Other SaaS tools that bill by usage: ______

**2.2 Fill one row per service.** `REQUIRED`

| # | Provider | Service name | What it does (plain words) | Billing type | Expected cost per month | Monthly limit | Owner | Needed in which phases |
|---|---|---|---|---|---|---|---|---|
| 1 | AWS | S3 | Stores user files | Pay per GB | $20 | $40 | Maria | 2 to 6 |
| 2 | | | | | | | | |
| 3 | | | | | | | | |
| 4 | | | | | | | | |
| 5 | | | | | | | | |
| 6 | | | | | | | | |
| 7 | | | | | | | | |
| 8 | | | | | | | | |

*Billing type choices:* `Fixed monthly` · `Pay per use` · `Pay per user` · `Prepaid credits` · `Free tier`

**2.3 For each provider, how do you see the bill?** `REQUIRED`

| Provider | Where to look at the bill (name of tool or page) | Who has access | How often is it updated |
|---|---|---|---|
| AWS | Billing and Cost Management, Cost Explorer | | |
| Azure | Cost Management | | |
| Google Cloud | Billing reports | | |
| Cloudflare | Billing page | | |
| AI APIs | Provider usage dashboard | | |

**2.4 Which services could cost a surprise amount if they go wrong?** `REQUIRED`
These are usually: data leaving the cloud (egress), AI calls in a loop, forgotten servers, logging, and backups.

| Service | What could go wrong | Worst-case cost per day | How we prevent it |
|---|---|---|---|
| | | | |

**2.5 Which accounts, subscriptions or projects exist?** `REQUIRED`
(One account per environment is best. Write names only, never secrets.)

| Provider | Account / subscription / project name | Environment (dev, test, prod) | Owner |
|---|---|---|---|
| | | | |

---

# Part 3: People and Responsibilities

> **Rule:** Every row needs a real person's name. If you work alone, write your own name in every row.

**3.1 Who does what?** `REQUIRED`

| Job | Person's name | Contact | Backup person |
|---|---|---|---|
| Budget Owner (decides how much can be spent) | | | |
| Cost Watcher (checks the bill every week) | | | |
| Tagger (makes sure every resource has tags) | | | |
| Technical Lead (can turn things off) | | | |
| Finance Contact (pays the bills, keeps invoices) | | | |
| Approver (signs this document) | | | |
| AI Agent Supervisor (checks what AI agents spend) | | | |

**3.2 Who can turn off or delete a service in an emergency?** `REQUIRED`
ANSWER:

**3.3 Who is allowed to create a new cloud account or start a new paid service?** `REQUIRED`
ANSWER:

**3.4 How fast must someone respond when a Red alert happens?** `REQUIRED`
- [ ] Within 1 hour
- [ ] Within 4 hours
- [ ] Within 1 working day
- [ ] Other: ______

---

# Part 4: Money Rules (Budgets and Traffic Lights)

**4.1 What is the monthly budget for this project?** `REQUIRED`

| Phase | Monthly budget | Total budget for the phase |
|---|---|---|
| 1. Plan | | |
| 2. Build | | |
| 3. Test | | |
| 4. Launch | | |
| 5. Customers 1 to 100 | | |
| 6. Customers 101 to 500 | | |

**4.2 Traffic-light rules.** `REQUIRED`
Change the numbers only if you have a good reason, and write the reason in the Change Log.

| Light | Meaning | Default | Your number | What must happen | Who acts |
|---|---|---|---|---|---|
| Green | All is fine | Under 70% of the monthly budget | | Do nothing special | Cost Watcher |
| Yellow | Slow down and look | 70% to 90% | | Find out why. Write a note in Part 10. | Cost Watcher |
| Red | Stop and decide | Over 90% | | Stop non-essential spending and call the Budget Owner. | Budget Owner |
| Black | Emergency | Over 100%, or a sudden jump of more than 2x in one day | | Turn off the most expensive service now. | Technical Lead |

**4.3 Alerts: where will the warnings go?** `REQUIRED`

| Provider | Budget alert switched on? | Anomaly (sudden jump) alert switched on? | Sent to (email or chat channel) |
|---|---|---|---|
| AWS | [ ] Yes [ ] No | [ ] Yes [ ] No | |
| Azure | [ ] Yes [ ] No | [ ] Yes [ ] No | |
| Google Cloud | [ ] Yes [ ] No | [ ] Yes [ ] No | |
| Cloudflare | [ ] Yes [ ] No | [ ] Yes [ ] No | |
| AI APIs | [ ] Yes [ ] No | [ ] Yes [ ] No | |

> An alert that goes to nobody is no alert. Use a place that someone actually reads.

**4.4 What are the approval rules for spending?** `REQUIRED`

| One new spend of... | Who must say yes first |
|---|---|
| Under $____ | Nobody, just tell the Cost Watcher |
| $____ to $____ | Budget Owner |
| Over $____ | Approver |

**4.5 What is the hard stop?** `REQUIRED`
When the monthly budget is used up, what happens?
- [ ] Spending stops automatically (limits set on the provider)
- [ ] Spending continues but the Budget Owner is called immediately
- [ ] Only non-production (dev and test) is turned off
- [ ] Other: ______

**4.6 How do you pay the bills?** `REQUIRED`

| Provider | Payment method (write type only, e.g. "company card ending in 1234" is NOT allowed; write "company card") | Invoice goes to | Invoice kept where |
|---|---|---|---|
| | | | |

**4.7 Reserve for surprises.** What percent of the budget is kept as a safety cushion? `REQUIRED`
Example: "10%".
ANSWER:

---

# Part 5: Tags (Name Labels on Every Cloud Item)

> **What is a tag?** A tag is a small label like a name sticker. If every cloud item wears a sticker saying whose it is, the bill can be split fairly. **No tag = no allocation = guessing.**
> (AWS and Azure call it a "tag". Google Cloud calls it a "label". Cloudflare and many SaaS tools use names, projects or notes instead.)

**5.1 Required tags (every item must have all of these).** `REQUIRED`
Keep the defaults unless you have a good reason.

| Tag name (use lowercase) | What it means | Allowed values | Example |
|---|---|---|---|
| `project` | Which project | Your project code | `acme-notes` |
| `owner` | The responsible person | A name or email prefix | `maria` |
| `environment` | Where it runs | `dev`, `test`, `prod` | `prod` |
| `phase` | Lifecycle phase (Part 8) | `1` to `6` | `2` |
| `cost-center` | Who pays | A code or name | `product` |
| `customer-type` | Who it serves (optional but recommended) | `shared`, `free`, `paid`, `internal` | `shared` |
| `managed-by` | How it was made | `human`, `terraform`, `ai-agent` | `ai-agent` |

Your extra tags (optional):

| Tag name | Meaning | Allowed values |
|---|---|---|
| | | |

**5.2 Tag rules.** `REQUIRED`
- [ ] Tag names are always lowercase with dashes (no spaces).
- [ ] The same tag name is used on every provider.
- [ ] No tag has a secret or personal data in it.
- [ ] On AWS, tags have been **activated for cost allocation** in the billing area (creating a tag is not enough).
- [ ] On Azure, a rule (Azure Policy) stops untagged things from being created, or someone checks weekly.
- [ ] On Google Cloud, labels are used and billing data is exported for reporting.
- [ ] On Cloudflare and SaaS tools that cannot tag, we use naming rules instead (see 5.3).

**5.3 What do we do for things that cannot be tagged?** `REQUIRED`
Example: "Cloudflare: one account per environment and the zone name starts with the project code. AI APIs: one API key per project and per environment, named `acme-notes-prod`."
ANSWER:

**5.4 Who checks tags, and how often?** `REQUIRED`
Example: "Cost Watcher, every Monday, using the 'untagged resources' report."
ANSWER:

**5.5 Goal for tagged spending.** What percent of the bill must be tagged? `REQUIRED`
Suggested: 90% in Phase 2, 95% in Phase 4, 98% from Phase 5.
ANSWER:

**5.6 What happens to an item with no tag after 7 days?** `REQUIRED`
- [ ] Owner is asked to fix it
- [ ] It is stopped
- [ ] It is deleted after approval
- [ ] Other: ______

---

# Part 6: How We Split the Bill (Allocation Rules)

> **Simple idea:** Some costs belong to one thing only (**direct costs**). Some costs are used by everything (**shared costs**). A few costs we cannot place yet (**unallocated costs**). We need a written rule for each, so nobody argues later.

## 6A: Direct costs

**6A.1 Which costs belong to exactly one project, product or customer?** `REQUIRED`
Example: "A dedicated database for the Pro plan."

| Cost | Belongs to | How we know (tag, account, key name) |
|---|---|---|
| | | |

## 6B: Shared costs

**6B.1 Which costs are used by many things at once?** `REQUIRED`
Example: "Main database, Cloudflare plan, monitoring, logging, the shared AI key."

| Shared cost | Monthly amount | Used by |
|---|---|---|
| | | |

**6B.2 Pick the method for splitting shared costs.** `REQUIRED`
Choose **one** method per shared cost.

| Method | Plain meaning | Good when | Not good when |
|---|---|---|---|
| **Even split** | Every user or product pays the same share | You have no usage data, early stage | Some customers use far more than others |
| **By usage** | Share depends on how much each one used (calls, GB, minutes, tokens) | You can measure usage | You cannot measure usage |
| **By revenue** | Share depends on how much each one pays you | You want costs to follow income | Free users would show zero cost |

| Shared cost | Method chosen (even / usage / revenue) | What we measure | Where the number comes from |
|---|---|---|---|
| | | | |

**6B.3 Rule for free users.** `REQUIRED`
Do free users get a share of shared costs?
- [ ] Yes, they count like everyone (recommended, because they really use the system)
- [ ] No, free users are paid for by the "marketing" budget
- [ ] Other: ______

**6B.4 When do we review these rules?** `REQUIRED`
Suggested: every 3 months and at the start of every phase.
ANSWER:

## 6C: Unallocated costs

**6C.1 What is the largest share of the bill we are allowed to leave unallocated?** `REQUIRED`
Suggested: 10% in the build phases, 5% after launch.
ANSWER:

**6C.2 Who must clean up unallocated costs, and by when?** `REQUIRED`
ANSWER:

## 6D: Credits, discounts and refunds

**6D.1 How do we count free credits and discounts?** `REQUIRED`
- [ ] Show cost **before** credits (true cost, recommended for planning)
- [ ] Show cost **after** credits (cash cost)
- [ ] Show both
ANSWER (write which one you will use in reports):

**6D.2 Taxes, support plans and marketplace fees.** Are they included in the project cost? `REQUIRED`
ANSWER:

---

# Part 7: Cost Per Customer (The Most Important Number)

> **Why?** Your bill going up is fine **if** you earn more from each customer than it costs you. The way to know is "cost per customer".

## 7A: The numbers

**7A.1 Who counts as a "customer"?** `REQUIRED`
Write one clear rule. Example: "A customer is a person who logged in at least once in the last 30 days."
ANSWER:

**7A.2 Count types.** `REQUIRED`

| Type | Definition | How we count it | Where the number comes from |
|---|---|---|---|
| Registered users | Signed up | | |
| Active users | Used the product in the last 30 days | | |
| Paying customers | Paid us in the last billing period | | |
| Free users | Active but not paying | | |

**7A.3 Formulas we will use.** `REQUIRED`
Do not change the formulas. Fill in your own numbers in the tables after them.

```
1. Total cloud cost for the month        = Direct costs + Shared costs + Unallocated costs
2. Blended cost per active customer      = Total cloud cost / Active customers
3. Cost per paying customer              = Total cloud cost / Paying customers
4. Cost per free user                    = Cost caused by free users / Free users
5. Gross margin per paying customer      = Price per customer - Cost per paying customer
6. Gross margin percent                  = Gross margin / Price per customer x 100
7. Cost per usage unit (if usage-based)  = Cost of the service / Units used  (e.g. per 1,000 AI calls)
8. Cost per customer for one-time sale   = Estimated cost to serve a customer over its life
```

**7A.4 What is the target?** `REQUIRED`

| Measure | Target | Phase it must be reached |
|---|---|---|
| Cost per active customer per month | | |
| Cost per paying customer per month | | |
| Gross margin percent (aim for at least 70% for software) | | |
| Largest allowed cost for one free user per month | | |

## 7B: Your revenue model

Fill only the blocks that match what you ticked in Part 1.7. Write `N/A` for the others.

**Monthly subscription** `OPTIONAL`

| Question | ANSWER |
|---|---|
| Monthly price | |
| Expected share of customers who cancel each month | |
| Average months a customer stays | |
| Cost to serve one customer per month | |
| Profit per customer per month | |

**Usage-based pricing** `OPTIONAL`

| Question | ANSWER |
|---|---|
| What is the unit we charge for (call, minute, GB, task)? | |
| Price per unit | |
| Our cost per unit | |
| Safe minimum price per unit (cost plus margin) | |
| Is there a free allowance? How big? | |

**Free plan plus paid plan** `OPTIONAL`

| Question | ANSWER |
|---|---|
| Free users as a share of all users | |
| Free users who become paying (conversion goal) | |
| Maximum cost we accept for one free user | |
| What stops free users from overspending (limits)? | |

**One-time purchase** `OPTIONAL`

| Question | ANSWER |
|---|---|
| Price | |
| How long do we promise to run it (months or years)? | |
| Expected monthly cost to serve one customer | |
| Total cost over the promised time | |
| What is left as profit? | |

## 7C: AI usage per customer

**7C.1 Does your product call AI models?** `REQUIRED`
- [ ] No (write `N/A` for the rest of 7C)
- [ ] Yes

**7C.2 If yes, fill this in.** `OPTIONAL`

| Question | ANSWER |
|---|---|
| Which AI model or provider? | |
| What does one customer action cost in AI (average)? | |
| How many AI actions does one customer do per month (average)? | |
| What is the cost for a heavy customer (top 10%)? | |
| What limit do we put on each customer (daily or monthly)? | |
| What happens when a customer reaches the limit? | |

> Tip: Count cost in the unit that matches your product (per task, per answer, per document). Raw token counts alone are hard for others to understand.

## 7D: Cost per customer tracker

> Fill one row each month. Copy the table below into your monthly report if it gets long.

| Month | Active customers | Paying customers | Total cloud cost | Cost per active customer | Cost per paying customer | Revenue | Gross margin % | Notes |
|---|---|---|---|---|---|---|---|---|
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |

## 7E: What-if table (fill before launch)

| What if... | Customers | Estimated monthly cost | Estimated cost per customer | Still profitable? (yes/no) |
|---|---|---|---|---|
| Launch month | 25 | | | |
| Customer 100 | 100 | | | |
| Customer 250 | 250 | | | |
| Customer 500 | 500 | | | |
| 500 customers, all heavy users | 500 | | | |
| Viral spike: 5x traffic for one week | | | | |

---

# Part 8: The Lifecycle (From First Idea to Customer 500)

> There are **6 phases**. Fill each block **at the start** of that phase. Do not move on until the **Exit Gate** is fully ticked.
>
> **AI-driven development note:** In every phase, AI agents may write code, create servers and run tests. That spends money. Part 9 sets the rules. Every phase block asks you about it.

## Phase overview

| # | Phase | Main goal | Exit gate in one line |
|---|---|---|---|
| 1 | Plan | Decide what to build and what it will cost | Budget approved, tags and alerts set |
| 2 | Build | Create the product (humans plus AI agents) | Costs are tagged and within budget |
| 3 | Test | Prove it works, safely and cheaply | Test costs known, test resources cleaned up |
| 4 | Launch | Open to the public | Alerts tested, limits tested, rollback plan ready |
| 5 | Customers 1 to 100 | Learn real cost per customer | Cost per customer measured for 2 months in a row |
| 6 | Customers 101 to 500 | Grow without losing money | Margin target met and review report signed |

Use this same block for every phase. **Copy one block per phase and rename it.**

---

## Phase 1: Plan

**Dates:** Start: ______  End: ______

| Question | ANSWER |
|---|---|
| What is the goal of this phase in one sentence? | |
| Monthly budget in this phase | |
| Total budget for this phase | |
| Customers expected at the end of this phase | |
| Which services from Part 2 are used? | |
| Which services are NOT allowed yet? | |
| Who approves spending in this phase? | |
| Estimated AI agent spend in this phase | |
| What is the biggest cost risk? | |
| What did we assume that we have not yet proven? | |

**Phase 1 questions about planning:** `REQUIRED`
1. Did we compare at least 2 options for the main hosting choice (cost and effort)? ANSWER:
2. Did we estimate costs for 25, 100 and 500 customers (Part 7E)? ANSWER:
3. Did we check free-tier and startup credit limits? ANSWER:
4. Did we choose which provider holds the main database, files and AI calls, and why? ANSWER:
5. Did we decide where in the world (region) data will live? Cost differs by region. ANSWER:

**Exit Gate: Phase 1**
- [ ] Parts 1 to 7 are complete
- [ ] Budget approved by the Approver
- [ ] Accounts created, owners named, billing alerts switched on (Part 4.3)
- [ ] Tags decided (Part 5)
- [ ] Phase 2 budget written in Part 4.1

---

## Phase 2: Build

**Dates:** Start: ______  End: ______

| Question | ANSWER |
|---|---|
| What is the goal of this phase in one sentence? | |
| Monthly budget in this phase | |
| Total budget for this phase | |
| Customers expected at the end of this phase | 0 |
| Which services are switched on? | |
| Which environments exist (dev, test)? | |
| Who approves new spending? | |
| AI agent monthly limit in this phase | |
| What is the biggest cost risk? | |
| What did we learn about real costs so far? | |

**Phase 2 questions about building:** `REQUIRED`
1. Do all items created by developers **and AI agents** carry the required tags? ANSWER:
2. Is there a rule that dev resources shut down at night or on weekends? ANSWER:
3. Are there separate accounts or keys for dev and prod? ANSWER:
4. Is there a size limit on test data so tests cannot create huge bills? ANSWER:
5. Is "infrastructure as code" used, so everything can be rebuilt or deleted in one go? ANSWER:
6. What is the plan to delete leftover test items? Who and when? ANSWER:

**Exit Gate: Phase 2**
- [ ] At least 90% of spend is tagged
- [ ] Spend stayed under budget (or the reason is written in the Change Log)
- [ ] No unknown or "mystery" services on the bill
- [ ] AI agent spend was reviewed
- [ ] Draft cost estimates in Part 7E are updated with real numbers

---

## Phase 3: Test

**Dates:** Start: ______  End: ______

| Question | ANSWER |
|---|---|
| What is the goal of this phase in one sentence? | |
| Monthly budget in this phase | |
| Total budget for this phase | |
| How many test users or test runs? | |
| Which services are used for load testing? | |
| Who approves load tests (they can be costly)? | |
| AI agent monthly limit in this phase | |
| What is the biggest cost risk? | |
| What did we measure as "cost per test user"? | |

**Phase 3 questions about testing:** `REQUIRED`
1. Did we run a load test and write down the cost of it? ANSWER:
2. Did we test that budget alerts really arrive (send a test alert)? ANSWER:
3. Did we test the per-customer limit (Part 7C)? ANSWER:
4. Did we test turning off the most expensive service? ANSWER:
5. What was the cost of one customer action in testing? ANSWER:

**Exit Gate: Phase 3**
- [ ] Alerts tested and received by a real person
- [ ] Test resources deleted or stopped
- [ ] Estimated cost per customer is updated (Part 7D)
- [ ] Safe limits exist for free users

---

## Phase 4: Launch

**Dates:** Start: ______  End: ______

| Question | ANSWER |
|---|---|
| What is the goal of this phase in one sentence? | |
| Monthly budget in this phase | |
| Total budget for this phase | |
| Customers expected at the end of this phase | |
| Expected traffic on launch day | |
| Maximum traffic we can afford | |
| What happens if traffic is bigger than we can afford? | |
| Who is on call during launch week? | |
| AI agent monthly limit in this phase | |
| What is the biggest cost risk? | |

**Phase 4 questions about launching:** `REQUIRED`
1. Are daily (not only monthly) cost checks done during launch week? Who? ANSWER:
2. Are Cloudflare rules in place to block bad or fake traffic that would raise the bill? ANSWER:
3. Are rate limits in place on every API that costs money? ANSWER:
4. Is there a "kill switch" that anyone on call can use? ANSWER:
5. Is there a written plan to go back to the previous state (rollback) if costs explode? ANSWER:

**Exit Gate: Phase 4**
- [ ] Alerts tested in production
- [ ] On-call person named for every day of launch week
- [ ] Limits and kill switch tested
- [ ] First real invoice reviewed line by line

---

## Phase 5: Customers 1 to 100

**Dates:** Start: ______  End: ______

| Question | ANSWER |
|---|---|
| What is the goal of this phase in one sentence? | |
| Monthly budget in this phase | |
| Customer number reached at the end | |
| Real cost per active customer (latest month) | |
| Real cost per paying customer (latest month) | |
| Real gross margin % (latest month) | |
| Is cost per customer going up or down? | |
| What are the top 3 most expensive services? | |
| What is the biggest cost risk? | |

**Phase 5 questions about the first 100 customers:** `REQUIRED`
1. Is the Part 7D tracker filled every month without gaps? ANSWER:
2. Which customers cost much more than average? Why? ANSWER:
3. Did the shared cost method (Part 6B) still make sense? ANSWER:
4. Which 3 savings ideas from Part 11 have we done? ANSWER:
5. Is the price still right for the real cost? ANSWER:

**Exit Gate: Phase 5**
- [ ] Cost per customer measured for 2 months in a row
- [ ] Gross margin target reached, or a written plan exists to reach it
- [ ] At least 95% of spend is tagged
- [ ] Unallocated spend under the limit in Part 6C

---

## Phase 6: Customers 101 to 500

**Dates:** Start: ______  End: ______

| Question | ANSWER |
|---|---|
| What is the goal of this phase in one sentence? | |
| Monthly budget in this phase | |
| Customer number reached at the end | 500 |
| Real cost per active customer (latest month) | |
| Real cost per paying customer (latest month) | |
| Real gross margin % (latest month) | |
| Which services grew fastest in cost? | |
| What is the cost forecast for the next 3 months? | |
| What is the biggest cost risk? | |

**Phase 6 questions about growing to 500:** `REQUIRED`
1. Do we have commitments or discounts (reserved capacity, savings plans, committed use) and do they match real usage? ANSWER:
2. Which part of the product costs most per customer, and can it be redesigned cheaper? ANSWER:
3. How much would cost rise if customers doubled? ANSWER:
4. What changes are needed at 1,000 customers? ANSWER:
5. What did we learn that should change the template? (Write it in Part 15.) ANSWER:

**Exit Gate: Phase 6 (Customer 500 reached)**
- [ ] A final "first 500 customers" cost review is written (see 8.7 below)
- [ ] The Approver has signed Part 14
- [ ] Improvements to this template are noted for the next project

## 8.7: First 500 customers review `REQUIRED at the end`

| Question | ANSWER |
|---|---|
| Total cloud spend from start until customer 500 | |
| Total revenue from start until customer 500 | |
| Average cost per customer over the whole time | |
| Cost per customer at customer 500 | |
| Budget used vs. planned (%) | |
| Biggest cost surprise | |
| Biggest saving made | |
| What would we do differently next time? | |

---

# Part 9: Rules for AI Agents

> **Why this part exists:** AI agents (such as coding assistants) can start servers, run tests and call AI models by themselves. They are fast. They can also spend a lot, very quickly. These rules keep them safe.

**9.1 Which AI agents or AI tools are used on this project?** `REQUIRED`

| Agent or tool | What it does | Who supervises it | Which accounts or keys it can use | Monthly spend limit |
|---|---|---|---|---|
| | | | | |

**9.2 What an AI agent MAY do** `REQUIRED`
Tick what is allowed:
- [ ] Read cost reports
- [ ] Create resources in **dev** only
- [ ] Create resources in **test**
- [ ] Add required tags to everything it creates
- [ ] Suggest savings
- [ ] Write cost reports
- [ ] Other: ______

**9.3 What an AI agent MUST ASK about first** `REQUIRED`
Tick what needs a human "yes" first:
- [ ] Creating any resource that costs more than $____ per month
- [ ] Creating anything in the production environment
- [ ] Turning on a new paid service
- [ ] Changing a budget, alert or limit
- [ ] Increasing the size of a database or server
- [ ] Running a load test
- [ ] Other: ______

**9.4 What an AI agent must NEVER do** `REQUIRED`
These are the defaults. Add more if you need to.
- [x] Never change billing or payment settings
- [x] Never create new cloud accounts or subscriptions
- [x] Never switch off budget or anomaly alerts
- [x] Never delete data or resources permanently without a human "yes"
- [x] Never create resources without the required tags
- [x] Never write secrets, keys or passwords into files, chats or logs
- [x] Never run loops that call paid APIs without a limit on the number of calls
- [ ] Other: ______

**9.4b Does this project use AI model calls inside the product itself?** `REQUIRED`
- [ ] No
- [ ] Yes. Each customer has a limit set in Part 7C.

**9.5 AI agent spending limits** `REQUIRED`

| Limit | Value |
|---|---|
| Monthly cloud spend an agent may cause in dev | |
| Monthly cloud spend an agent may cause in test | |
| Monthly AI model cost (tokens, API calls) in total | |
| Highest cost of one single task | |
| Highest number of loops or retries before it must stop and ask | |

**9.6 How do we see what the agents spent?** `REQUIRED`
Example: "Each agent has its own API key named `agent-<name>-<env>`. Cost Watcher checks the usage page every Monday."
ANSWER:

**9.7 What does an agent do when it is unsure about cost?** `REQUIRED`
Default answer: **Stop and ask the human. Do not guess.**
ANSWER (keep the default or write your own):

**9.8 After an agent finishes a task, what must it report?** `REQUIRED`
- [ ] What it created (with tags)
- [ ] What it deleted
- [ ] Estimated monthly cost of what was created
- [ ] What it left running
- [ ] Anything it was unsure about

---

# Part 10: Watching the Bill (Routine)

**10.1 When do we check, and who?** `REQUIRED`

| Check | How often | Who | What they look at | Where the result is written |
|---|---|---|---|---|
| Quick look | Every week (suggested: Monday) | Cost Watcher | Total so far, top 5 services, traffic light color, untagged spend, AI agent spend | Weekly log below |
| Deep review | Every month (suggested: first week) | Budget Owner, Cost Watcher, Finance Contact | Full cost per customer, forecasts, savings, tag health, shared cost method | Monthly report below |
| Launch watch | Daily during Phase 4, then weekly | Person on call | Costs, traffic, errors | Weekly log below |
| Method review | Every 3 months | Budget Owner | Part 6 rules, Part 5 tags, Part 7 targets | Change Log |

**10.2 Weekly checklist** (Cost Watcher)
- [ ] Opened the bill page for **every** provider in Part 2.3
- [ ] Wrote down total spend so far this month
- [ ] Wrote down the traffic light color
- [ ] Looked at the top 5 most expensive services
- [ ] Checked for anything new or unknown
- [ ] Checked the untagged spend number
- [ ] Checked AI agent spend
- [ ] If Yellow or Red: contacted the person named in Part 4.2

**10.3 Weekly log**

| Week starting | Total this month so far | Light (G/Y/R/B) | Top service | Anything strange? | Action | Done by |
|---|---|---|---|---|---|---|
| | | | | | | |
| | | | | | | |
| | | | | | | |
| | | | | | | |

**10.4 Monthly deep review checklist**
- [ ] Compared real cost with budget (each provider and each phase)
- [ ] Filled the Part 7D tracker
- [ ] Reviewed top 10 most expensive items
- [ ] Reviewed untagged and unallocated costs
- [ ] Reviewed what AI agents spent versus their limit
- [ ] Reviewed free credits left and the expiry dates
- [ ] Picked at least one saving to act on (Part 11)
- [ ] Made a 3-month cost forecast
- [ ] Updated the Change Log if rules changed
- [ ] Saved all invoices where Part 4.6 says

**10.5 Monthly report**

| Month | Planned cost | Real cost | Difference | Cost per customer | Biggest change | Decision made | Next steps and owner |
|---|---|---|---|---|---|---|---|
| | | | | | | | |
| | | | | | | | |
| | | | | | | | |

**10.6 If something goes wrong (Red or Black)** `REQUIRED`
Write the exact steps, in order. A new team member must be able to follow them.

| Step | What to do | Who |
|---|---|---|
| 1 | Check which service caused it (open the bill, sort by cost, look at the last 24 hours) | |
| 2 | Tell the Budget Owner | |
| 3 | Stop the cause (turn off, limit, or block) | |
| 4 | Write down what happened and when | |
| 5 | Fix the cause so it cannot happen again | |
| 6 | Update the Change Log | |

---

# Part 11: Saving Ideas Checklist

> Tick what you have **done**. Write the owner and date for what you **will** do.

## 11.1 Works on every cloud
- [ ] Delete things that are not used (old servers, disks, test data, old copies)
- [ ] Shut down dev and test outside working hours
- [ ] Pick the right size (not too big) for servers and databases
- [ ] Choose a cheaper region if the customers allow it
- [ ] Set storage to move old files to cheaper storage after some time
- [ ] Remove old backups and logs after a fixed time
- [ ] Reduce logging noise (logs can cost a lot)
- [ ] Use caching so we do not do the same work twice
- [ ] Put a limit on every API that costs money
- [ ] Look for sudden jumps in data leaving the cloud (egress)
- [ ] Use commitments or reserved capacity **only after** two or more months of steady usage
- [ ] Use cheaper "interruptible" machines (spot) for work that can be redone

## 11.2 AWS
- [ ] Billing alerts, Cost Explorer and Cost Anomaly Detection switched on
- [ ] Cost allocation tags **activated**
- [ ] Unused disks, IP addresses and load balancers removed
- [ ] Storage lifecycle rules set
- [ ] Savings Plans considered after steady usage

## 11.3 Microsoft Azure
- [ ] Budgets set in Cost Management
- [ ] Tag rules enforced with Azure Policy
- [ ] Unused disks, public IPs and old snapshots removed
- [ ] Dev/test machines auto-shut down
- [ ] Reservations considered after steady usage

## 11.4 Google Cloud
- [ ] Budgets and alerts set in Billing
- [ ] Labels applied everywhere
- [ ] Billing data exported for reports
- [ ] Idle resources removed (use the recommender)
- [ ] Committed use discounts considered after steady usage

## 11.5 Cloudflare
- [ ] Plan size matches real traffic
- [ ] Caching rules set to reduce requests to our servers
- [ ] Bot and abuse rules set to reduce fake traffic
- [ ] Usage-based items (workers, storage, bandwidth) have alerts

## 11.6 AI and SaaS APIs
- [ ] One key per project **and** per environment
- [ ] Hard monthly spend limit set at the provider (if available)
- [ ] Smaller or cheaper model used for simple jobs
- [ ] Repeated questions are cached
- [ ] Prompts and inputs are kept as short as possible
- [ ] Retries and loops have a maximum count
- [ ] Per-customer usage limit set (Part 7C)
- [ ] Unused seats and subscriptions cancelled

**11.7 Our top 3 savings to do next**

| # | Idea | Expected saving per month | Owner | Due date | Done? |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

---

# Part 12: Risks and "What If" Plans

**12.1 Risk list** `REQUIRED`
Write at least 5 risks. Use the starter rows, add your own.

| # | What could go wrong | How likely (low, medium, high) | How costly (low, medium, high) | What we do to prevent it | Who owns it |
|---|---|---|---|---|---|
| 1 | A forgotten server keeps running | | | | |
| 2 | An AI agent or script loops and calls a paid API thousands of times | | | | |
| 3 | A sudden traffic spike or attack raises the bill | | | | |
| 4 | Free credits run out earlier than expected | | | | |
| 5 | A few heavy customers cost more than they pay | | | | |
| 6 | Tags are missing and we cannot split the bill | | | | |
| 7 | Nobody reads the alert emails | | | | |
| 8 | A provider changes its prices | | | | |
| 9 | | | | | |
| 10 | | | | | |

**12.2 What do we do if cost per customer is higher than the price?** `REQUIRED`
Write your choices in order (for example: limit free users, reduce usage, raise price, change provider).
ANSWER:

**12.3 What do we do if a provider account is locked or suspended?** `REQUIRED`
ANSWER:

---

# Part 13: Quality Checklist (Check Before Sign-Off)

> Tick every box honestly. If you cannot tick a box, fix the document first.

**Completeness**
- [ ] No `REQUIRED` question is blank
- [ ] Every `TBD` has an owner and a due date
- [ ] Every `OPTIONAL` question that does not apply says `N/A because ...`
- [ ] Part 0 matches the rest of the document

**Clarity**
- [ ] A new team member could understand every answer without asking anyone
- [ ] Every number has a unit and currency
- [ ] Every owner is a real person's name
- [ ] Every date uses `YYYY-MM-DD`

**Money**
- [ ] Budget for the current phase is set
- [ ] Traffic-light numbers are set and make sense
- [ ] Budget and anomaly alerts are switched on for every provider and go to a real place
- [ ] There is a hard-stop rule (Part 4.5)
- [ ] Credits and their expiry dates are listed

**Allocation**
- [ ] Every service in Part 2 has an owner and a limit
- [ ] Required tags are defined and used on every provider
- [ ] Shared costs each have one clear splitting method
- [ ] The unallocated limit is set

**Cost per customer**
- [ ] "Customer" is defined clearly
- [ ] Formulas are untouched
- [ ] Targets are set
- [ ] What-if table (7E) is filled

**AI agents**
- [ ] Allowed, ask-first and never-do lists are complete
- [ ] Spend limits are set
- [ ] There is a way to see what agents spent

**Safety**
- [ ] No passwords, keys, tokens or card numbers appear anywhere in this file
- [ ] Emergency steps (Part 10.6) are clear
- [ ] Someone can turn off services at any time (Part 3.2)

**Process**
- [ ] Review routine is scheduled in people's calendars
- [ ] Change Log is up to date

**Result**

| Total boxes | Ticked | Percent |
|---|---|---|
| | | |

Must be **100%** before sign-off.

---

# Part 14: Approvals and Signatures

| Role | Name | Decision (Approved / Needs changes) | Date | Comment |
|---|---|---|---|---|
| Document Owner | | | | |
| Budget Owner | | | | |
| Finance Contact | | | | |
| Technical Lead | | | | |
| Approver | | | | |

---

# Part 15: Change Log

> Add a new row every time you change a number, rule, owner or limit.

| Date | Who changed it | Which part and question | Old value | New value | Why | Approved by |
|---|---|---|---|---|---|---|
| | | | | | | |
| | | | | | | |
| | | | | | | |
| | | | | | | |

**Lessons for the next project** (fill at the end of Phase 6)

| What worked well | What did not | What should change in this template |
|---|---|---|
| | | |

---

# Part 16: Glossary (Plain-English Words)

| Word | Simple meaning |
|---|---|
| **Cloud** | Computers owned by another company that you rent over the internet. |
| **Cloud cost allocation** | Deciding which project, product or customer should pay for which part of the cloud bill. |
| **Direct cost** | A cost that belongs to one thing only. |
| **Shared cost** | A cost used by many things at once. |
| **Unallocated cost** | A cost we cannot place yet. |
| **Showback** | Showing people what they cost, without moving real money. |
| **Chargeback** | Actually billing a team or a client for what they used. |
| **Tag (or label)** | A name sticker on a cloud item (like "project: acme-notes"). |
| **Budget** | The most you plan to spend. |
| **Traffic light** | Green, Yellow, Red or Black colors that tell you how close you are to the budget. |
| **Anomaly** | A sudden, unusual jump in cost. |
| **Unit cost** | What one "unit" costs, such as one customer, one AI answer or one GB. |
| **Cost per customer** | Total cloud cost divided by number of customers. |
| **Gross margin** | What is left from the price after paying the cost to serve the customer. |
| **Free tier** | A small amount of a service that a provider gives for free. |
| **Credits** | Prepaid money from a provider that reduces your bill. |
| **Egress** | Data leaving a cloud provider. It is often charged. |
| **Region** | The place in the world where a provider keeps your data. |
| **Environment** | A separate copy of the system: dev (building), test (checking), prod (real customers). |
| **Production (prod)** | The real system that customers use. |
| **Reserved capacity / commitment** | A promise to use a service for a long time in return for a lower price. |
| **Spot / interruptible** | Cheaper computers that the provider can take back at any time. |
| **Rate limit** | A rule that stops anyone from calling something too many times. |
| **Kill switch** | A way to turn off something quickly in an emergency. |
| **Rollback** | Going back to the last working version. |
| **AI agent** | A computer program powered by AI that can take actions by itself, such as writing code or creating servers. |
| **Token** | A small piece of text that AI models count and charge for. |
| **Infrastructure as code** | Writing the setup of your cloud as a file so it can be repeated or deleted in one go. |
| **Owner** | One named person who is responsible. |
| **TBD** | "To be decided", with an owner and a due date. |

---

# Appendix A: Filled Mini Example (for Reference Only)

> A tiny project filled in so you can see what a good answer looks like. **Do not copy it. Use it as a guide.**

| Question | Example answer |
|---|---|
| 1.1 What does it do? | A notes app that turns voice recordings into tidy summaries. |
| 1.3 Total money until customer 500 | USD 12,000 |
| 2.2 Service row | AWS S3, stores audio files, pay per GB, expected $20 per month, limit $40, owner Maria, phases 2 to 6 |
| 4.2 Yellow | 70% of the monthly budget; Cost Watcher writes a note in the weekly log the same day |
| 5.1 Tag | `project = acme-notes`, `environment = prod`, `owner = maria` |
| 6B.2 Shared cost method | Main database: by usage (number of notes saved per customer) |
| 7A.1 Customer | A person who logged in at least once in the last 30 days |
| 7A.4 Target | Cost per paying customer: USD 3.50 per month; gross margin at least 70% |
| 9.5 AI limit | AI agent may cause at most USD 150 per month in dev and test together |
| 10.1 Weekly check | Every Monday, Cost Watcher (Ben), checks all providers and writes the result in the weekly log |

---

# Appendix B: Reference Sources Used to Design This Template

- FinOps Foundation framework: cost allocation, tagging, shared cost strategy, showback and chargeback, unit economics, and the Inform, Optimize, Operate cycle
- FinOps Open Cost and Usage Specification (FOCUS) for consistent multi-cloud cost data
- AWS, Azure and Google Cloud native budgeting, tagging and anomaly detection guidance
- FinOps guidance on SaaS and AI spend (cost per task or inference as a business-friendly unit)

*End of template. Save a fresh copy of this file for every new project and fill it in from the top.*
