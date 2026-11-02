# How to Fill This Document (Read This First)

**What is this document?**
It is your project's money plan. It answers three simple things:
1. **How much will this project cost us?** (Budgets)
2. **How will we notice if costs go wrong?** (Monitoring and alerts)
3. **What do we do if costs go wrong?** (Emergency plan)

**Who is it for?** A solo founder (one person does everything). If you later add teammates, keep your name in every "Owner" box and add theirs next to it.

**Time needed:** 60-90 minutes the first time. After that, 15 minutes per review.

## The 7 Rules for Filling It In

1. **Go in order.** Start at Section 0 and finish at Section 12. Do not skip ahead.
2. **Every question has 4 parts:**
   - **Question:** what we are asking, in plain words.
   - **Your answer:** write here. Replace the text in `[square brackets]`.
   - **Example:** a filled-in sample so you can see what "good" looks like.
   - **If unsure:** a safe default. Use it and mark the answer `(default)`.
3. **Never leave a blank.** Use one of these three words instead:
   - `N/A - [reason]` means it does not apply (example: `N/A - we do not use AI APIs`).
   - `TBD - [date]` means you do not know yet; write the date you will find out.
   - `(default)` means you used the "If unsure" answer.
4. **Money rules:** write one currency for the whole document (set in Section 1). Write every cost per **month** unless a table says otherwise. Round up, never down.
5. **Dates:** use `YYYY-MM-DD` (example: `2026-10-18`).
6. **Do not paste secrets.** Never write passwords, API keys, or card numbers in this file. Write only *where* they are stored (example: "in my password manager").
7. **Track your progress** with the status marks below.

| Mark | Meaning |
|---|---|
| ⬜ | Not started |
| 🟨 | In progress |
| ✅ | Done and checked |

## The 5 Stages Used in This Document

Your product moves through 5 stages, from the first line of code to your first 500 customers. Every budget, alert, and check in this file is split by these stages.

| Stage | Name | Starts when | Ends when |
|---|---|---|---|
| 1 | **Build** | You start building | The product works on your own computer or a test server |
| 2 | **Staging / Beta** | Test users (friends, testers) try it | You are ready to open to the public |
| 3 | **Launch Day** | You announce it publicly | The first 7 days after launch are over |
| 4 | **Customers 1-100** | Your first paying or active customer | You reach 100 customers |
| 5 | **Customers 101-500** | Customer 101 | You reach 500 customers (goal reached) |

> **"Customer"** means one real person or business who signed up and uses the product. Write your own meaning in Section 2, Question 2.4.

## Words You Will See (Mini Dictionary)

| Word | Simple meaning |
|---|---|
| **Budget** | The most money you allow yourself to spend on something in a month |
| **Alert** | A message that warns you when spending is getting close to the budget |
| **Hard cap** | A setting that **stops** spending automatically when the limit is reached |
| **Soft limit** | A setting that only **warns** you; spending continues |
| **Cloud / Hosting** | The company that runs your product on the internet (servers, databases, storage) |
| **Third-party service** | Any other company's tool you pay for (email sender, payments, analytics) |
| **AI / LLM usage** | Money paid to AI companies each time your product (or your AI agents) asks an AI model to do something. Usually billed per "token" (a small chunk of text) |
| **Fixed cost** | Same price every month (example: a $20 monthly subscription) |
| **Variable cost** | Price goes up when usage goes up (example: AI calls, emails sent) |
| **Cost per customer** | Total monthly cost divided by number of customers |
| **Gross margin** | The share of each sale left after paying the costs of serving the customer |
| **Runaway cost** | A sudden, unexpected spike in spending (example: a bug that calls an AI model in an endless loop) |
| **Tag / Label** | A name stuck on a cloud resource (example: `project=myapp`) so you can see what it costs |
| **Kill switch** | A fast way to turn something off in an emergency |

---

# Cost Monitoring and Budgets

## Section 0: Document Status

| Field | Your answer |
|---|---|
| Template version | `1.0` (do not change) |
| Progress | ⬜ / 🟨 / ✅ |
| Last full update | `[YYYY-MM-DD]` |
| Next review due | `[YYYY-MM-DD]` |

### Related Documents

> Link the other documents in your project folder so nothing is guessed. If a document does not exist yet, write `Not created yet` and add it to Section 12.

| Topic | File name (default shown) | Link or path | Exists? (Yes / Not created yet) |
|---|---|---|---|
| Pricing and plans | `Pricing_and_Packaging.md` | `[ ]` | `[ ]` |
| System design and services used | `System_Architecture.md` | `[ ]` | `[ ]` |
| Security and keys | `Security_and_Secrets.md` | `[ ]` | `[ ]` |
| Incidents and outages | `Incident_Response.md` | `[ ]` | `[ ]` |
| Launch steps | `Launch_Checklist.md` | `[ ]` | `[ ]` |
| Monitoring and alerts (technical) | `Monitoring_and_Alerting.md` | `[ ]` | `[ ]` |

---

## Section 1: Project Basics

**Question 1.1 - What is the project called?**
- Your answer: `[Project name]`
- Example: `PetPal Booking App`

**Question 1.2 - Who owns this document?** (the person who makes money decisions)
- Your answer: `[Your name]` and `[email or phone for urgent contact]`
- Example: `Sam Lee, sam@example.com`

**Question 1.3 - Who is your backup if you are unreachable for 3 days?** (a trusted person who could pause spending in an emergency)
- Your answer: `[Name and contact]` or `N/A - no one yet`
- If unsure: `N/A - no one yet`, then add a task in Section 12 to find one before Stage 3.

**When a team joins (fill in later; leave as-is while you work alone):**

| Role | What this person does | Who (name) | Date added |
|---|---|---|---|
| Budget Owner | Keeps this document up to date; you, until you hire | `[Your name]` | `[ ]` |
| Approver | Says yes or no to any budget increase over `[amount]` | `[Your name]` | `[ ]` |
| Backup | Can pause spending in an emergency | `[Name]` | `[ ]` |
| Finance contact | Handles tax, invoices, and bookkeeping | `[Name or N/A]` | `[ ]` |

- Rule: one person can hold several roles. Nobody should approve their own budget increase once there are two or more people.

**Question 1.4 - Which currency will you use everywhere?**
- Your answer: `[USD / EUR / GBP / other]`
- If unsure: `USD (default)`

**Question 1.5 - On which day of the month do your main bills renew?**
- Your answer: `[Day of month, 1-31]`
- Example: `The 15th`
- If unsure: `1st (default)`

**Question 1.6 - Where is the product built and run?** (list each company or tool, one per line)
- Your answer: `[Hosting company], [database company], [AI model company], [others]`
- Example: `Vercel (hosting), Supabase (database), Anthropic (AI), Stripe (payments)`

**Question 1.7 - Where do you keep logins for these billing accounts?**
- Your answer: `[Name of password manager or safe place, NOT the passwords]`
- Example: `1Password, vault "Business"`

---

## Section 2: Project Snapshot (the numbers that drive your costs)

**Question 2.1 - In one sentence, what does your product do?**
- Your answer: `[One sentence]`
- Example: `Lets dog owners book trusted sitters in under 2 minutes.`

**Question 2.2 - How do you earn money?**
- Choose one: `Free / One-time purchase / Monthly subscription / Pay-per-use / Ads / Other`
- Your answer: `[Choice]`
- If unsure: `Monthly subscription (default)`

**Question 2.3 - What is the average price one customer pays per month?** (write `0` if free)
- Your answer: `[Amount per month]`
- Example: `$12`

**Question 2.4 - What counts as a "customer" for you?**
- Your answer: `[Definition]`
- Example: `Someone who created an account AND used the product at least once.`
- If unsure: `A person who signed up and used the product at least once (default)`

**Question 2.5 - Does your product call AI models while customers use it?**
- Choose one: `Yes / No / Not sure`
- Your answer: `[Choice]`
- If `No`, still complete Section 3.4 for the AI tools you use to **build** the product.
- If `Not sure`, answer `Yes (default)`: it is safer to track it.

**Question 2.6 - How many customers do you expect at each stage?**

| Stage | Expected customers at END of stage | Your answer |
|---|---|---|
| 1. Build | 0 | `0` |
| 2. Staging / Beta | Testers | `[number]` |
| 3. Launch Day (first 7 days) | New sign-ups | `[number]` |
| 4. Customers 1-100 | 100 | `100` |
| 5. Customers 101-500 | 500 | `500` |

- If unsure for stage 2-3: use `10` and `30 (default)`.

**Question 2.7 - What is the maximum you could lose on this project without serious trouble?** (your "pain limit" for ALL costs combined, per month)
- Your answer: `[Amount per month]`
- Example: `$600`
- If unsure: `10% of your monthly savings you can afford to lose (default)`. This number is your **Absolute Monthly Ceiling**. No budget below may add up to more than this.

---

## Section 3: Cost Inventory (list EVERYTHING you pay for)

> **How to fill each table:** one row per service. Add rows as needed. If you pay for nothing in a table, write one row: `N/A - [reason]`.
> **Cost type:** `Fixed` (same every month) or `Variable` (grows with use).
> **Cost per month:** your honest estimate for the **end of Stage 5** (500 customers). You will split by stage in Section 4.

### 3.1 Cloud and Hosting

**Question 3.1 - What do you pay for to run the product online?** (servers, database, storage, file hosting, domain name, content delivery, backups, logging)

| # | Service name | What it is for | Cost type | Billing unit (example: per GB, flat) | Cost per month at 500 customers | Where do I see the bill? (link) |
|---|---|---|---|---|---|---|
| 1 | `[Example: Hosting]` | `[Runs the website]` | `Fixed` | `Flat monthly` | `[$25]` | `[URL]` |
| 2 | | | | | | |
| 3 | | | | | | |

- If unsure about a number: look at the provider's price page and write `(default: from price page, [date])`.

### 3.2 Third-Party Services and APIs

**Question 3.2 - What other companies' tools does your product depend on?** (sign-in service, email or text-message sending, payments, analytics, error tracking, search, maps, customer support chat)

| # | Service name | What it is for | Cost type | Billing unit (example: per 1,000 emails) | Cost per month at 500 customers | Where do I see the bill? (link) |
|---|---|---|---|---|---|---|
| 1 | `[Example: Payment processor]` | `[Takes card payments]` | `Variable` | `[2.9% + 0.30 per sale]` | `[$180]` | `[URL]` |
| 2 | | | | | | |
| 3 | | | | | | |

> **Reminder:** payment companies take a cut of each sale. That is a real cost. Include it.

### 3.3 People and Tools

**Question 3.3 - What do you pay for to *make* the product?** (developer tools, design tools, code hosting, AI coding assistants, contractors or freelancers, legal or accounting, domain renewals, marketing tools)

| # | Item | What it is for | Cost type | Billing unit | Cost per month | Renewal date |
|---|---|---|---|---|---|---|
| 1 | `[Example: AI coding assistant subscription]` | `[Writes code with me]` | `Fixed` | `Per month` | `[$20]` | `[YYYY-MM-DD]` |
| 2 | | | | | | |
| 3 | | | | | | |

- Do **not** include your own salary unless you want to. Write your choice: `Salary included / Salary NOT included`. If unsure: `Salary NOT included (default)`.

### 3.4 AI and LLM Usage

> Skip nothing here. If your product does not call AI models, write `N/A - product makes no AI calls` in the first row, but **still fill in AI used to build** (rows marked "Build").

**Question 3.4 - Which AI models do you use, and for what?**

| # | AI provider and model | Used for | Build or Product? | Billed by (example: per million tokens) | Price per unit (from price page) | Cost per month at 500 customers |
|---|---|---|---|---|---|---|
| 1 | `[Example: Provider X, Model Y]` | `[Answers customer questions]` | `Product` | `Per million tokens` | `[$input / $output]` | `[$120]` |
| 2 | | | `Build` | | | |
| 3 | | | | | | |

**Question 3.4a - How many AI calls does ONE customer cause in a typical month?**
- Your answer: `[Number of calls]`
- Example: `40 calls`
- If unsure: `100 calls per customer per month (default)`

**Question 3.4b - About how big is one AI call?** (small: a short question; medium: a page of text; large: a long document)
- Choose one: `Small / Medium / Large`
- Your answer: `[Choice]`
- If unsure: `Medium (default)`

**Question 3.4c - Which AI agents run by themselves (without you watching), for example for code, testing, support, or content?**
- Your answer: `[List each agent and what it does]` or `N/A - none`
- Example: `Support-reply agent: drafts answers to customer emails, runs on every new email.`

**Question 3.4d - Is there a limit on how many calls or how much money an agent may use per day?**
- Your answer: `[Limit]` or `No limit yet`
- If `No limit yet`: add a task in Section 12. **Never go live with unlimited AI spending.**

**How to estimate AI cost (simple formula):**
`customers x calls per customer x cost per call = AI cost per month`
Cost per call: ask the provider's price page, or run 10 real calls and divide the bill by 10. Then add **20% extra** for mistakes and retries.

### 3.5 One-Time Costs (not monthly)

**Question 3.5 - What do you pay only once or once a year?** (domain, trademark, security audit, legal documents, launch ads, app store fees)

| # | Item | Amount | Date paid or due | Stage it belongs to (1-5) |
|---|---|---|---|---|
| 1 | | | | |

### 3.6 Tax, Refunds, and Currency

**Question 3.6a - Do your prices include sales tax or VAT?**
- Choose one: `Yes, included / No, added on top / Not sure`
- Your answer: `[Choice]`
- If unsure: `Not sure`, then add a task in Section 12 to check with the payment provider or an accountant.

**Question 3.6b - Who collects and pays tax to governments?**
- Choose one: `The payment provider does it for me / I do it myself / Not sure`
- Your answer: `[Choice]`
- If unsure: `Not sure`. Do not launch to paying customers until this is answered (Section 11, Gate B).

**Question 3.6c - Out of every 100 sales, how many do you expect to refund?**
- Your answer: `[Number out of 100]`
- If unsure: `5 (default)`
- Monthly refund cost = `monthly sales x refund rate`. Add it to Section 4 under Third-Party Services and APIs.

**Question 3.6d - What does your payment provider charge for a chargeback (when a customer disputes a payment with their bank)?**
- Your answer: `[Fee per chargeback]`
- If unsure: `15 in your currency (default)`; check the provider's price page.

**Question 3.6e - Do customers pay you in a different currency than the one in Question 1.4?**
- Your answer: `Yes - [currencies] / No`
- If `Yes`, what is the currency-exchange fee? `[%]`. If unsure: `2% (default)`.

| Extra cost | Rate or fee | Estimated per month at 500 customers |
|---|---|---|
| Refunds | `[ ]` | `[ ]` |
| Chargebacks | `[ ]` | `[ ]` |
| Currency exchange | `[ ]` | `[ ]` |
| Tax tools or accountant | `[ ]` | `[ ]` |

### 3.7 Discounts, Free Credits, and Commitments

**Question 3.7a - Do you have free credits or discounts right now?** (startup programs, free tiers, trial months, coupons)

| # | Provider | What you get | Amount | Ends on (date) | What the monthly cost becomes after it ends |
|---|---|---|---|---|---|
| 1 | `[ ]` | `[ ]` | `[ ]` | `[YYYY-MM-DD]` | `[ ]` |

- Write `N/A - no credits` if none.
- **Golden rule: build every budget in Section 4 at FULL price, as if the credits did not exist.** Credits are a bonus, not a plan.

**Question 3.7b - Did you promise to pay for a long time to get a cheaper price?** (annual plans, reserved servers, minimum-spend deals)

| # | Item | Total promised | Months locked in | Can I cancel? | Renewal date |
|---|---|---|---|---|---|
| 1 | `[ ]` | `[ ]` | `[ ]` | `Yes / No` | `[YYYY-MM-DD]` |

- Write `N/A - none` if none.
- If unsure: do **not** sign a long commitment before Stage 4. Use monthly plans until your costs are stable.

**Question 3.7c - What is the date of your earliest credit expiry or renewal?** Put it in your calendar now.
- Your answer: `[YYYY-MM-DD]`

---

## Section 4: Budgets by Stage

> **How to fill this:** For each stage, write the **maximum** you will allow yourself to spend **per month** in each area. Use the inventory from Section 3 and the customer numbers from Question 2.6.
> **Golden rule:** The "Total" row for any stage must be **less than or equal to** your Absolute Monthly Ceiling (Question 2.7).
> **If unsure:** Take your estimate and add **20% buffer** `(default)`.

### 4.1 Monthly Budget Table

| Cost area | Stage 1 Build | Stage 2 Staging/Beta | Stage 3 Launch Day (first month) | Stage 4 Customers 1-100 | Stage 5 Customers 101-500 |
|---|---|---|---|---|---|
| Cloud and Hosting | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Third-Party Services and APIs | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| People and Tools | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| AI and LLM Usage | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| **Subtotal** | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Safety buffer (20%) | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| **TOTAL monthly budget** | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Question 4.2 - Does every TOTAL stay under your Absolute Monthly Ceiling (Question 2.7)?**
- Your answer: `Yes / No`
- If `No`: lower a budget, raise the ceiling on purpose (write why), or raise prices. Write what you decided: `[Decision]`

**Question 4.3 - What is your total one-time budget for launch (Section 3.5 items plus launch marketing)?**
- Your answer: `[Amount]`

**Question 4.4 - How many months of costs could you pay with the money you have right now (your "runway")?**
- Your answer: `[Number of months]`
- Formula: `money available / Stage 5 total monthly budget`
- If unsure: `TBD - [date]`

### 4.5 Budget Approval

| Item | Your answer |
|---|---|
| Budget approved by | `[Your name]` |
| Date approved | `[YYYY-MM-DD]` |
| Rule for changing a budget | `Write the reason in Section 13 (Change Log) BEFORE changing any number` (do not edit) |

---

## Section 5: Alerts (how you get warned)

**Question 5.1 - Where will warnings reach you?** (pick every channel you will actually check daily)
- Options: `Email / Phone text / Phone app notification / Chat app message / Other`
- Your answer: `[Channels]`
- If unsure: `Email + phone notification (default)`
- Warning: never send alerts only to a mailbox you do not read daily.

**Question 5.2 - What alert levels will you use?**

> Defaults are already filled in. Change only if you have a reason.

| Level | When it triggers (share of the month's budget used) | Name | What YOU do |
|---|---|---|---|
| 1 | 50% | Heads-up | Look at the dashboard. Is it too early to be at 50%? Note it in the log. |
| 2 | 80% | Warning | Find the top 3 costs. Decide: slow down, optimize, or raise the budget (write why in Section 13). |
| 3 | 100% | Limit reached | Stop non-essential spending. Turn on soft limits or caps. Follow Section 10, Steps 1-3. |
| 4 | 120% | Emergency | Follow the **full Emergency Plan in Section 10 immediately.** |

**Question 5.3 - For each cost area, how will the alert be created?**

| Cost area | Tool or setting that sends the alert (example: provider "Budget Alerts" page) | Alert set up? (⬜/✅) | Date tested |
|---|---|---|---|
| Cloud and Hosting | `[ ]` | ⬜ | `[ ]` |
| Third-Party Services and APIs | `[ ]` | ⬜ | `[ ]` |
| People and Tools | `[ ]` | ⬜ | `[ ]` |
| AI and LLM Usage | `[ ]` | ⬜ | `[ ]` |

**Question 5.4 - Did you TEST an alert (for example by setting a tiny test budget) to prove the message reaches you?**
- Your answer: `Yes, on [date] / No`
- If `No`: do it before Stage 3.

**Question 5.5 - Do you have a "sudden spike" alert, separate from the budget alert?** (example: "tell me if today costs 3 times more than normal")
- Your answer: `[Tool and setting]` or `No`
- If unsure: set it to `3x normal daily spend (default)`

---

## Section 6: Monitoring Setup (how you SEE your costs)

**Question 6.1 - Where is your one "cost dashboard"?** (one page or sheet where you can see all four cost areas together)
- Your answer: `[Link or name]`
- Example: `Google Sheet "Cost Tracker" + each provider's billing page`
- If unsure: `A simple spreadsheet with one row per day or week (default)`

**Question 6.2 - How will you separate this project's costs from other things you pay for?**
- Options: `Separate account / Separate billing project / Tags or labels / Separate API keys / Nothing yet`
- Your answer: `[Choice]`
- If unsure: `Tags or labels + a separate API key for each environment (default)`
- Tag names to use (do not change): `project`, `stage`, `owner`.

**Question 6.3 - Do you use different accounts or keys for testing and for real customers?**
- Your answer: `Yes / No`
- If `No`: create them. This stops test mistakes from costing real money.

**Question 6.4 - Which automatic safety limits are switched on?** (tick each one you have, write `N/A` if the provider does not offer it)

| Safety limit | On? (✅/⬜/N/A) | Where I set it |
|---|---|---|
| Monthly spending cap at the hosting provider (hard cap if offered) | ⬜ | `[ ]` |
| Spending limit on the AI provider account | ⬜ | `[ ]` |
| Rate limit (max requests per minute) on public pages and APIs | ⬜ | `[ ]` |
| Daily limit per AI agent (Question 3.4d) | ⬜ | `[ ]` |
| Per-customer usage limit (example: max 100 AI calls per day) | ⬜ | `[ ]` |
| Separate payment card with a spending limit for this project | ⬜ | `[ ]` |
| Auto-shutdown for test servers outside working hours | ⬜ | `[ ]` |

**Question 6.5 - Which costs are you tracking daily, weekly, or monthly?**

| What | How often | Where |
|---|---|---|
| Total spend so far this month | `Daily` | `[ ]` |
| Spend per cost area | `Weekly` | `[ ]` |
| AI usage (calls, tokens, money) | `Daily` | `[ ]` |
| Spend per customer | `Monthly` | `[ ]` |

- If unsure: keep the frequencies above `(default)`.

---

## Section 7: Cost per Customer and Profit Check

> Fill this in at the **end of each stage**. It tells you if the business can survive.

**Question 7.1 - What do you actually pay, per month, at the end of each stage?** (use real bills, not estimates)

| Measure | Stage 2 | Stage 3 | Stage 4 | Stage 5 |
|---|---|---|---|---|
| A. Real total monthly cost | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| B. Number of customers | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| C. Cost per customer (A divided by B) | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| D. Average price per customer (Question 2.3) | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| E. Profit per customer (D minus C) | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| F. Gross margin % (E divided by D x 100) | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Question 7.2 - What minimum gross margin do you want?**
- Your answer: `[%]`
- If unsure: `70% (default)`

**Question 7.3 - If margin is below your minimum, what will you do?** (pick the first that fits)
1. Lower AI or hosting costs (smaller model, caching, cheaper plan).
2. Raise the price.
3. Limit free usage.
- Your answer: `[Decision]`

**Question 7.4 - What does your single most expensive customer cost per month, compared with your average?**
- Your answer: `[Number]`
- If this is more than 5 times the average, add a per-customer limit (Section 6.4).

---

## Section 8: Planned vs Real (Monthly Cost Log)

> Fill one row per month, on your review day (Section 9). Never delete old rows.

| Month | Planned total | Real total | Difference (real minus planned) | Biggest cost this month | What I learned or changed |
|---|---|---|---|---|---|
| `[YYYY-MM]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| | | | | | |
| | | | | | |

**Question 8.1 - If real is more than 10% above planned two months in a row, what will you do?**
- Your answer: `[Action]`
- If unsure: `Re-do Section 3 and Section 4 with real numbers (default)`

---

## Section 9: Review Schedule

**Question 9.1 - When will you review costs?**

| Review | How often | Your day and time | Time needed |
|---|---|---|---|
| Quick check | Stage 1-2: weekly. Stage 3: **daily for 7 days**. Stage 4-5: weekly. | `[e.g., Monday 9:00]` | 10 minutes |
| Full review | Monthly | `[e.g., 1st Monday]` | 45 minutes |
| Big review | At the end of every stage | `[date]` | 90 minutes |

**Quick check agenda (copy into your calendar):**
1. Open your cost dashboard (Question 6.1).
2. Is this month's spend above the expected line for today's date?
3. Did any alert fire since last time?
4. Any new service or subscription added? If yes, add it to Section 3.
5. Write one line in Section 8 if anything surprised you.

**Full review agenda (monthly):**
1. Fill the Section 8 row with real numbers.
2. Update Section 7 (cost per customer, margin).
3. Find the top 3 costs. Can any be cut by 10% or more?
4. Cancel anything unused (subscriptions, test servers, unused API keys).
5. Check alerts still go to the right place.
6. Set next month's budgets (Section 4). Record changes in Section 13.

**Question 9.2 - Where is the reminder set?**
- Your answer: `[Calendar name]`

---

## Section 10: Runaway-Cost Emergency Plan

> Use this when alerts say you hit 120%, or any cost jumps suddenly. **Stay calm. Follow the steps in order. Write down times.**

**Question 10.1 - What are your emergency "kill switches"?** (fast ways to stop spending)

| Kill switch | How to do it (exact steps) | How long it takes | Tested? (✅/⬜) |
|---|---|---|---|
| Pause or revoke the AI provider key | `[ ]` | `[ ]` | ⬜ |
| Turn off AI agents | `[ ]` | `[ ]` | ⬜ |
| Disable sign-ups or a feature (feature flag) | `[ ]` | `[ ]` | ⬜ |
| Scale down or pause servers | `[ ]` | `[ ]` | ⬜ |
| Pause email/text sending | `[ ]` | `[ ]` | ⬜ |

**Emergency steps (default, edit only if you have a better plan):**

| Step | Action | Done (time) |
|---|---|---|
| 1. **Confirm** | Open the dashboard. Is the spike real? Which cost area? | `[ ]` |
| 2. **Stop the bleeding** | Use the kill switch for that area (Question 10.1). | `[ ]` |
| 3. **Tell people** | Tell your backup (Question 1.3). If customers are affected, post a short status note. | `[ ]` |
| 4. **Find the cause** | Check: new release? a bug causing loops? a bot attack? a leaked key? one very heavy customer? | `[ ]` |
| 5. **Secure** | If a key may be leaked, replace the key now. | `[ ]` |
| 6. **Fix and restart** | Fix the cause. Restart slowly (test first with a tiny limit). | `[ ]` |
| 7. **Ask for help from the provider** | Many providers give a one-time credit after a mistake. Ask politely with the dates and cause. | `[ ]` |
| 8. **Write it down** | Fill the incident record below within 48 hours. | `[ ]` |

**Question 10.2 - What is the most you can pay for ONE emergency without borrowing money?**
- Your answer: `[Amount]`
- If unsure: `1 month of your Stage 5 total budget (default)`

### Incident Record (copy this table for each incident)

| Field | Your answer |
|---|---|
| Date and time started | `[ ]` |
| Date and time stopped | `[ ]` |
| Which cost area | `[ ]` |
| Extra money lost | `[ ]` |
| Cause (one sentence) | `[ ]` |
| What fixed it | `[ ]` |
| What will stop it happening again | `[ ]` |
| Credit asked from provider? | `Yes / No` |

---

## Section 11: Stage Gates (Can I move to the next stage?)

> Before moving to the next stage, every box for that gate must be ✅. If a box cannot be ✅, write `Blocked - [reason]` and fix it first.

### Gate A: Before Stage 2 (Staging / Beta)
- ⬜ Section 3 inventory has every service I use.
- ⬜ Stage 1 real cost is written in Section 8.
- ⬜ Budgets for Stage 2 are set (Section 4).
- ⬜ Alerts exist for all four cost areas (Section 5.3).
- ⬜ Test and real accounts/keys are separate (Question 6.3).

### Gate B: Before Stage 3 (Launch Day)
- ⬜ An alert was tested and reached me (Question 5.4).
- ⬜ A hard cap or limit exists on hosting and AI accounts (Question 6.4).
- ⬜ Every AI agent has a daily limit (Question 3.4d).
- ⬜ Kill switches are written and at least one was practiced (Section 10).
- ⬜ A backup contact is named, or I accepted the risk in writing: `[ ]`
- ⬜ I can afford the Stage 3 budget AND one emergency (Question 10.2).
- ⬜ Rate limits are on public pages and APIs.
- ⬜ I know who collects and pays sales tax or VAT (Question 3.6b).
- ⬜ Credit expiry and renewal dates are in my calendar (Question 3.7c).

### Gate C: Before Stage 4 → Stage 5 (reaching 100 customers)
- ⬜ Section 7 is filled with real numbers for Stage 4.
- ⬜ Gross margin is at or above my minimum (Question 7.2), or I decided what to change.
- ⬜ I cancelled unused services.
- ⬜ Stage 5 budgets are updated from real data.
- ⬜ Cost per customer is NOT rising month after month. If it is: `[Reason and plan]`

### Gate D: Goal Reached (500 customers)
- ⬜ Section 7 and Section 8 are complete for Stage 5.
- ⬜ I wrote what worked and what to do differently next time in Section 14.
- ⬜ I decided the plan for customers 501+: `Keep this document and update budgets / Create a new growth budget`.

---

## Section 12: Open Tasks

> Anything marked `TBD`, `No limit yet`, `No`, or `Blocked` above goes here.

| # | Task | Why it matters | Due date | Done? |
|---|---|---|---|---|
| 1 | | | | ⬜ |
| 2 | | | | ⬜ |
| 3 | | | | ⬜ |

---

## Section 13: Change Log

> Write a line **every time** you change a budget, alert level, or limit.

| Date | What changed | Old value | New value | Why |
|---|---|---|---|---|
| `[YYYY-MM-DD]` | | | | |

---

## Section 14: Lessons Learned (fill at end of each stage)

| Stage | What cost more than expected | What cost less | One thing to do differently |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |

---

## Section 15: Instructions for AI Agents (do not edit this section)

> If an AI agent reads this file, it must follow these rules.

1. **Source of truth:** The numbers in Sections 2, 4, 5, and 6 are the only budget rules. Never invent a number. If a field says `TBD`, `[ ]`, or is blank, **stop and ask the owner** (Question 1.2).
2. **Never increase** a budget, cap, limit, or alert threshold by yourself. Only the owner may, and the change must be logged in Section 13.
3. **Never delete or shut down** servers, databases, keys, or customer data without written approval from the owner in the current conversation. Pausing a **non-production** agent you started is allowed.
4. **Before any action that may cost money** (starting servers, running large AI jobs, loops over many items), state the estimated cost. If the estimate is more than **5%** of the current stage's monthly budget, ask for approval first.
5. **Respect limits:** Do not exceed the daily limit in Question 3.4d. Stop and report if you reach 80% of it.
6. **Alerts:** If you notice spending at 80% or more of the monthly budget (Section 5.2), send the owner a message through the channels in Question 5.1 and follow the "What YOU do" column.
7. **Emergency:** At 120% or a sudden spike (Question 5.5), follow Section 10 steps 1-3 immediately, using only the kill switches listed in Question 10.1 that you are allowed to use. Report every step you take.
8. **Secrets:** Never write keys, passwords, or card numbers into this file or any log.
9. **Report format** (use for weekly or monthly reports):
   - Month and stage
   - Planned vs real total (Section 8 format)
   - Top 3 costs
   - Alerts fired
   - Cost per customer and margin (Section 7)
   - Recommended actions (max 3), clearly marked as recommendations
10. **Gates:** Do not mark a Stage Gate (Section 11) as ✅ unless you checked the proof yourself. Write how you checked.

---

## Final Check (tick before calling this document "done")

- ⬜ No field is blank (each has a real answer, `N/A - reason`, `TBD - date`, or `(default)`).
- ⬜ No passwords, keys, or card numbers appear anywhere.
- ⬜ Section 4 totals are under the Absolute Monthly Ceiling.
- ⬜ Dates in Section 0 and Section 9 are filled.
- ⬜ Section 12 lists every `TBD`.
- ⬜ I read the document once, top to bottom, as if I were a stranger.

---

# Appendix A: Where to Find Budgets and Alerts (Provider Cheat-Sheet)

> Menu names change often. If you cannot find a setting, open the provider's help page and search the **keywords** below. Write the exact place you found it in Section 5.3 and Section 6.4.

| Provider type | What to search for | What to set up |
|---|---|---|
| Amazon Web Services (AWS) | "Budgets", "Cost Explorer", "Cost Anomaly Detection", "Cost Allocation Tags" | A monthly budget with email alerts at 50 / 80 / 100 / 120 percent, plus an anomaly alert |
| Google Cloud | "Billing", "Budgets and alerts", "Quotas" | A budget with alert thresholds; lower quotas on costly services |
| Microsoft Azure | "Cost Management", "Budgets", "Alerts" | A budget with alert rules and an action group (who gets notified) |
| Vercel | "Spend Management" or "Usage" | A spend limit with notifications |
| Supabase | "Spend cap", "Usage", "Billing" | Turn the spend cap on if available; watch database, storage, and bandwidth |
| Other hosting (any) | "Billing", "Usage", "Spending limit", "Alerts" | A monthly limit plus an email alert; or a separate payment card with a limit |
| AI model providers | "Usage", "Limits", "Spend limit", "Budget", "API keys" | A monthly spend limit, separate keys per environment, and usage alerts |
| Payment processors | "Fees", "Disputes", "Refunds", "Reports" | A monthly export of fees, refunds, and chargebacks into your tracker |
| Email and text-message services | "Usage", "Limits", "Quota" | A daily send limit and an alert at 80% |
| Any provider with no budget tool | "Invoices", "Usage export" | A weekly manual check and a prepaid or capped payment card |

**Question A.1 - Which of your providers have NO built-in alerts or caps?**
- Your answer: `[List]`
- For each one, write your workaround (weekly manual check, capped card, prepaid credits): `[ ]`

---

# Appendix B: Filled-In Example (made-up app, for learning only)

> **Do not copy these numbers.** This shows what a finished document looks like. The app, names, and prices are invented.

**Project:** PetPal Booking App. **Owner:** Sam Lee. **Currency:** USD. **Billing day:** 15th.
**What it does:** Lets dog owners book trusted sitters in under 2 minutes.
**How it earns:** Monthly subscription, `12` per customer. **Customer means:** signed up and booked at least once.
**Absolute Monthly Ceiling:** `1,000`.

**Cost inventory at 500 customers (monthly):**

| Area | Item | Type | Estimate |
|---|---|---|---|
| Cloud and Hosting | Web hosting 25, database 25, file storage 10 | Fixed/Variable | `60` |
| Third-Party | Payments (2.9% + 0.30 per sale: 174 + 150), email service 25, analytics 20, error tracking 26, refunds and chargebacks ~ 0 (included in buffer) | Variable | `395` |
| People and Tools | AI coding assistant 20, design tool 15, code hosting 4, domain 2 (about) | Fixed | `45` |
| AI and LLM | 500 customers x 40 calls x 0.01 per call | Variable | `200` |

**Budgets by stage (monthly, 20% buffer included in TOTAL):**

| Cost area | S1 Build | S2 Beta | S3 Launch month | S4 (1-100) | S5 (101-500) |
|---|---|---|---|---|---|
| Cloud and Hosting | 10 | 25 | 40 | 45 | 60 |
| Third-Party and APIs | 10 | 20 | 110 | 140 | 400 |
| People and Tools | 45 | 45 | 45 | 45 | 45 |
| AI and LLM | 10 | 15 | 30 | 40 | 200 |
| Subtotal | 75 | 105 | 225 | 270 | 705 |
| Safety buffer (20%) | 15 | 21 | 45 | 54 | 141 |
| **TOTAL** | **90** | **126** | **270** | **324** | **846** |

Check: every TOTAL is under the 1,000 ceiling. ✅

**Alerts:** email + phone notification at 50 / 80 / 100 / 120 percent. Spike alert at 3x normal daily spend. Alert test passed on `2026-11-02`.
**Safety limits on:** hosting spend cap, AI provider monthly limit of 250, 100 AI calls per customer per day, separate test and live keys.
**Cost per customer at Stage 5:** about `1.41` (705 / 500). Profit per customer: `12 - 1.41 = 10.59`. Gross margin: about `88%` (above the 70% minimum). ✅
**Biggest risk spotted:** payment fees are over half of Third-Party costs. Decision: review the payment plan at 100 customers.
**Credits:** AI provider gives `500` free credit that ends `2027-03-01`. Budgets above ignore it, as the golden rule says.
**Review day:** quick check every Monday 9:00; full review on the 1st Monday of each month.

---

# Appendix C: Quick Reference Card (print or pin)

| If this happens | Do this |
|---|---|
| Spend hits 50% of budget early in the month | Look at the dashboard and note it |
| Spend hits 80% | Find the top 3 costs; decide to slow, optimize, or raise budget (and log it) |
| Spend hits 100% | Stop non-essential spending; turn on caps; Section 10 steps 1-3 |
| Spend hits 120%, or a sudden spike | Section 10, full plan, now |
| New subscription added | Add it to Section 3 the same day |
| Credit or discount about to end | Update Section 3.7 and the budget before it ends |
| Customer count passes 100 or 500 | Do the Stage Gate (Section 11) and update Section 7 |
