# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

> **Who this is for:** anyone. You do NOT need to be technical. If you can answer questions about your own product, you can fill this in.
> **What this document does:** It records *what counts as a "win" (a conversion) in your product, how you will count it, and how you will know the counting is correct* — from the first line of code until your first 500 customers.
> **Where it lives:** `Product Analytics and Instrumentation/Conversion_Tracking.md`
> **One file only:** Everything is in this single file. Do not create extra files.

---

## Step-by-step instructions

1. **Copy this file** into your project's `Product Analytics and Instrumentation` folder. Keep the name `Conversion_Tracking.md`.
2. **Fill in the Document Header** (Section A) first. It takes 2 minutes.
3. **Choose your path** in Section B:
   - **Quick Path** = small or simple projects. Fill only the sections marked ⚡.
   - **Full Path** = everything. Fill all sections.
4. **Go top to bottom.** Each section is a list of questions. Every question has:
   - **Why we ask** — one sentence so you understand the point.
   - **Example answer** — a sample so you can copy the style.
   - **➡️ Your answer:** — the line where you write your answer.
5. **Write simple words.** Short sentences are better than long ones. If a 10-year-old could read your answer and understand it, it is a good answer.
6. **Never guess silently.** If you do not know an answer, write it in the TBD format (see rules below). Do not invent an answer.
7. **Update the Completion Tracker** (Section A) when you finish a section.
8. **Ask for a review** when all required sections are done. Change the Status from `Draft` to `In review`.
9. **Get approval.** The approver signs off in Section 16. Status becomes `Approved`.
10. **Keep it alive.** After launch, update this file whenever you add, change, or remove anything you track. Add a line to the Change Log.

---

## Rules for filling answers

| Rule | What it means | Example |
|---|---|---|
| **Be specific** | Use real names and real numbers. | ❌ "Many users" → ✅ "500 paying users" |
| **One idea per answer** | Don't pack three answers into one line. | Split into three lines. |
| **Use the choices** | When you see `[ ]` boxes, put an `x` inside the ones that apply: `[x]`. | `[x] Web app` |
| **TBD format** | If unknown: `TBD — Owner: <name> — Due: <date>`. Then copy it to Section 14 (Open Questions). | `TBD — Owner: Priya — Due: 2026-11-05` |
| **N/A needs a reason** | If a question does not apply, write `N/A — because <reason>`. | `N/A — because we have no mobile app` |
| **Assumptions are labeled** | If you are assuming something, start with `ASSUMPTION:` and add it to Section 14. | `ASSUMPTION: Most users come from Google.` |
| **No secrets** | Never write passwords, API keys, or private customer data in this file. | Write "stored in the team password manager". |
| **Dates** | Use `YYYY-MM-DD`. | `2026-10-18` |

---

## Words you will see (mini dictionary)

| Word | Simple meaning |
|---|---|
| **Conversion** | A visitor or user does something valuable to your business (signs up, buys, books a call). A "win". |
| **Macro conversion** | The BIG win. Usually money or a major commitment (a purchase, a paid subscription). |
| **Micro conversion** | A small step toward the big win (watches a demo, adds to cart, creates an account). |
| **Event** | A single action we record, like "button clicked" or "order placed". |
| **Property** | Extra details attached to an event (which product, how much money, which page). |
| **Funnel** | The steps people go through from first visit to the big win. Like a slide that gets narrower. |
| **Attribution** | Figuring out *where a customer came from* (Google, Instagram, a friend). |
| **UTM** | Little labels added to a web link so we know which campaign sent the visitor. |
| **Instrumentation** | Adding tracking code to the product so events get recorded. |
| **QA** | Quality Assurance. Testing that the tracking really works. |
| **PII** | Personal info that identifies a person (name, email, phone, address). Handle with extra care. |
| **Consent** | Permission from the user to track them. |
| **Source of truth** | The one place we trust when numbers disagree. |
| **AI agent** | An AI helper that reads this file and does work (writes code, tests, reports). |

---

# A. DOCUMENT HEADER

> **Why we ask:** So anyone opening this file knows whose it is, how fresh it is, and whether it can be trusted.

| Field | Your answer |
|---|---|
| **Project name** | ➡️ |
| **Product one-line description** | ➡️ |
| **Document owner (one person)** | ➡️ |
| **Document created on** | ➡️ |
| **Last updated on** | ➡️ |
| **Version** (start at `0.1`; `1.0` when first approved) | ➡️ |
| **Status** (pick one) | `[ ] Draft` `[ ] In review` `[ ] Approved` |
| **Approver name** | ➡️ |
| **Current lifecycle phase** (see Section 9) | `[ ] Plan` `[ ] Build` `[ ] Test` `[ ] Launch` `[ ] Customers 1–500` `[ ] Beyond 500` |

## A.1 Completion tracker

> Tick the box when a section is fully done (no empty answers, TBDs listed in Section 14).

| # | Section | Path | Done? |
|---|---|---|---|
| 1 | Project snapshot | ⚡ Quick | `[ ]` |
| 2 | Goals and conversion definitions | ⚡ Quick | `[ ]` |
| 3 | Product type and tool choices | ⚡ Quick | `[ ]` |
| 4 | Customer journey and funnel | ⚡ Quick | `[ ]` |
| 5 | Event tracking plan | ⚡ Quick | `[ ]` |
| 6 | Properties, identity, naming rules | Full | `[ ]` |
| 7 | Attribution: UTM and channels | ⚡ Quick | `[ ]` |
| 8 | Privacy, consent, compliance | ⚡ Quick | `[ ]` |
| 9 | Lifecycle plan (Plan → Customer 500) | Full | `[ ]` |
| 10 | QA and test checklist | ⚡ Quick | `[ ]` |
| 11 | Dashboards and reports | Full | `[ ]` |
| 12 | First 500 customers: milestones and weekly rhythm | ⚡ Quick | `[ ]` |
| 13 | Data quality and maintenance | Full | `[ ]` |
| 14 | Risks, assumptions, open questions | ⚡ Quick | `[ ]` |
| 15 | AI Agent Handoff | ⚡ Quick | `[ ]` |
| 16 | Review and sign-off | ⚡ Quick | `[ ]` |

**Completion:** ➡️ ___ of 16 sections done = ___ %

## A.2 Change log

> Add one row every time you change something important. Newest on top.

| Date | Version | Who | What changed | Why |
|---|---|---|---|---|
| ➡️ 2026-10-18 | 0.1 | ➡️ | Created from template | Project start |
| | | | | |
| | | | | |
| | | | | |

---

# B. CHOOSE YOUR PATH

**Question B.1 — How big is this project?**
> **Why we ask:** Small projects should not drown in paperwork.

- `[ ]` **Quick Path** — one product, small team, simple sales (fill only ⚡ sections)
- `[ ]` **Full Path** — multiple products, paid ads, many channels, regulated data, or a big team (fill everything)

➡️ **Why I chose this path:**

**Question B.2 — What is the plan for the first 500 customers?**
> **Why we ask:** Every section of this file is aimed at one finish line: *500 customers using the product.*

- **What exactly is a "customer" for us?** (Example: "A person who has paid at least once" or "A person who completed onboarding and used the product 3 times".)
  ➡️ Your answer:
- **Target date to reach 500 customers:**
  ➡️ Your answer:
- **How many customers do we have today?**
  ➡️ Your answer:

---

# 1. PROJECT SNAPSHOT ⚡

> **Goal of this section:** Describe the product in plain words so that nobody has to guess what we are tracking.

**Q1.1 — What does the product do, in one sentence?**
- *Why we ask:* Tracking only makes sense if everyone agrees what the product is.
- *Example:* "A mobile app that helps dog owners book local dog walkers."
- ➡️ Your answer:

**Q1.2 — Who is the main customer?**
- *Why we ask:* Different customers behave differently, so we must know who we are measuring.
- *Example:* "Busy dog owners aged 25–45 in large cities."
- ➡️ Your answer:

**Q1.3 — How does the business make money?**
- `[ ]` One-time purchase
- `[ ]` Monthly or yearly subscription
- `[ ]` Free trial then paid
- `[ ]` Freemium (free plan + paid upgrade)
- `[ ]` Marketplace commission
- `[ ]` Advertising
- `[ ]` Leads sold or passed to sales (no online payment)
- `[ ]` Donations
- `[ ]` Other: ➡️

**Q1.4 — What are the product types we need to track? (pick all)**
- `[ ]` Web app / SaaS
- `[ ]` Mobile app (iOS)
- `[ ]` Mobile app (Android)
- `[ ]` E-commerce store
- `[ ]` Marketplace (buyers and sellers)
- `[ ]` Content or lead-generation website
- `[ ]` Other: ➡️

**Q1.5 — Where can people meet the product? List every "front door".**
- *Why we ask:* Every front door needs tracking, or we will have blind spots.
- *Example:* "Landing page, app store listing, Instagram bio link, email newsletter."
- ➡️ Your answer:

**Q1.6 — Who are the people involved with this document?**

| Role | Name | Contact | What they decide |
|---|---|---|---|
| Business owner / founder | ➡️ | ➡️ | Goals, budget |
| Product manager | ➡️ | ➡️ | What gets tracked |
| Developer / AI agent operator | ➡️ | ➡️ | How tracking is built |
| QA tester | ➡️ | ➡️ | Whether it works |
| Marketing lead | ➡️ | ➡️ | Channels, campaigns |
| Legal / privacy contact | ➡️ | ➡️ | Consent and compliance |

**Q1.7 — Which countries or regions will our users live in?**
- *Why we ask:* Privacy laws depend on where users live (see Section 8).
- *Example:* "USA, Canada, UK, Germany."
- ➡️ Your answer:

---

# 2. GOALS AND CONVERSION DEFINITIONS ⚡

> **Goal of this section:** Decide, in writing, what a "win" is. If we do not agree on this, our numbers will be meaningless.

## 2.1 Business goals

**Q2.1 — What is the #1 business goal for the next 90 days?**
- *Why we ask:* Everything we track should help answer whether we are reaching this goal.
- *Example:* "Get 100 paying customers."
- ➡️ Your answer:

**Q2.2 — What is the goal for the first 500 customers?**
- *Example:* "Reach 500 paying customers with at least 30% still active after 30 days."
- ➡️ Your answer:

**Q2.3 — What would make us say "tracking was a failure"?**
- *Why we ask:* Naming failure upfront stops arguments later.
- *Example:* "We cannot tell which ad brought a customer."
- ➡️ Your answer:

## 2.2 Macro conversions (the BIG wins)

> Rule: Most products have **1 to 3** macro conversions. More than 3 is a warning sign.

**Q2.4 — Fill the macro conversion table.**

| ID | Conversion name | Plain-words definition (exactly when does it count?) | Money value (if any) | Counted once per… | Owner |
|---|---|---|---|---|---|
| M1 | *Example:* Paid Subscription Started | *The first time a user's card is charged successfully* | *$29* | *user* | *Ana* |
| M2 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| M3 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |

**Q2.5 — For each macro conversion, what does NOT count?**
- *Why we ask:* Edge cases create false numbers.
- *Example:* "Test purchases, refunds within 24 hours, and employee accounts do not count."
- ➡️ M1 does not count: 
- ➡️ M2 does not count: 
- ➡️ M3 does not count: 

## 2.3 Micro conversions (the small steps)

**Q2.6 — Fill the micro conversion table.**
> Micro conversions are steps that show someone is getting closer to a macro conversion.

| ID | Micro conversion | Which macro does it lead to? | Why it matters | Example of when it counts |
|---|---|---|---|---|
| m1 | *Example:* Account Created | M1 | *Can't pay without an account* | *User finishes signup form* |
| m2 | *Example:* Added Payment Method | M1 | *Strongest sign of buying intent* | *Card saved successfully* |
| m3 | ➡️ | ➡️ | ➡️ | ➡️ |
| m4 | ➡️ | ➡️ | ➡️ | ➡️ |
| m5 | ➡️ | ➡️ | ➡️ | ➡️ |
| m6 | ➡️ | ➡️ | ➡️ | ➡️ |

**Q2.7 — Activation: what is the first moment a new user "gets value"?**
- *Why we ask:* People who reach this moment are far more likely to become paying customers.
- *Example:* "User books their first dog walk."
- ➡️ Your answer:
- **How long should it take a new user to reach this? (minutes/days)** ➡️

**Q2.8 — Retention: what does "came back" mean?**
- *Example:* "Opened the app and viewed a booking on 3 different days in their first 14 days."
- ➡️ Your answer:

## 2.4 Targets

**Q2.9 — Fill the target table (use best guesses, mark as ASSUMPTION).**

| Metric | Today | Target at 100 customers | Target at 500 customers | How it is measured |
|---|---|---|---|---|
| Visitor → signup rate | ➡️ | ➡️ | ➡️ | ➡️ |
| Signup → activation rate | ➡️ | ➡️ | ➡️ | ➡️ |
| Activation → paid rate | ➡️ | ➡️ | ➡️ | ➡️ |
| Cost to get one customer | ➡️ | ➡️ | ➡️ | ➡️ |
| Refund / cancel rate | ➡️ | ➡️ | ➡️ | ➡️ |
| 30-day retention | ➡️ | ➡️ | ➡️ | ➡️ |

---

# 3. PRODUCT TYPE AND TOOL CHOICES ⚡

> **Goal of this section:** Pick the tools that will collect and show the numbers. This template works with any tool.

**Q3.1 — Which analytics tool(s) will record events?**
- *Why we ask:* The AI agent and developers must know where to send data.
- `[ ]` Google Analytics 4 (GA4)
- `[ ]` Mixpanel
- `[ ]` Amplitude
- `[ ]` PostHog
- `[ ]` Segment (data pipe to other tools)
- `[ ]` RudderStack
- `[ ]` Heap
- `[ ]` Firebase Analytics (mobile)
- `[ ]` Our own database / warehouse (name): ➡️
- `[ ]` Other: ➡️
- `[ ]` Not decided yet → `TBD — Owner: ___ — Due: ___`

**Q3.2 — Which advertising platforms need conversion data sent back to them?**
- `[ ]` Google Ads
- `[ ]` Meta (Facebook / Instagram) Ads
- `[ ]` TikTok Ads
- `[ ]` LinkedIn Ads
- `[ ]` Apple Search Ads
- `[ ]` Reddit / X / Pinterest / Snapchat Ads (circle which): ➡️
- `[ ]` None right now

**Q3.3 — Which other tools need to know about conversions?**
- `[ ]` Payment provider (Stripe, PayPal, etc.): ➡️
- `[ ]` Email / marketing tool (Mailchimp, Klaviyo, etc.): ➡️
- `[ ]` CRM (HubSpot, Salesforce, etc.): ➡️
- `[ ]` Customer support tool: ➡️
- `[ ]` Spreadsheet / BI dashboard tool: ➡️
- `[ ]` Other: ➡️

**Q3.4 — Where will tracking code run? (pick all)**

| Place | Used? | Notes |
|---|---|---|
| In the user's browser (client-side) | `[ ]` | Easy, but ad blockers can hide events |
| On our server (server-side) | `[ ]` | More reliable, better for money events |
| Inside the mobile app (SDK) | `[ ]` | iOS / Android |
| Tag manager (e.g., Google Tag Manager) | `[ ]` | Lets non-developers change tags |
| Payment provider webhooks | `[ ]` | Best proof that money moved |

> **Simple rule of thumb:** Track **money** events on the **server** (or from payment webhooks). Track **clicks and views** in the **browser or app**.

**Q3.5 — What is our "source of truth" for each important number?**
- *Why we ask:* When two tools show different numbers, we need to know which one wins.

| Number | Source of truth (the tool we trust) | Why |
|---|---|---|
| Revenue | ➡️ *Example: Payment provider* | *It holds the real money records* |
| Signups | ➡️ *Example: Our database* | *Every account is a row* |
| Visits / traffic | ➡️ | ➡️ |
| Ad spend | ➡️ | ➡️ |

**Q3.6 — Who has access to the analytics tool, and how is access given?**
- ➡️ Your answer (names/roles only, never passwords):

**Q3.7 — What is the monthly budget for analytics tools?**
- ➡️ Your answer:

**Q3.8 — Per product type, which extra things must we plan for? (tick what applies)**

**Web app / SaaS**
- `[ ]` Signup and login tracking
- `[ ]` Free trial start and end
- `[ ]` Plan upgrade / downgrade / cancel
- `[ ]` Team invites

**Mobile app**
- `[ ]` App install and first open
- `[ ]` Push notification permission
- `[ ]` In-app purchase and subscription renewal
- `[ ]` Deep links (links that open a specific screen)
- `[ ]` App store attribution (where the install came from)

**E-commerce / marketplace**
- `[ ]` Product viewed → added to cart → checkout → paid
- `[ ]` Discount codes
- `[ ]` Refunds and returns
- `[ ]` Seller onboarding and first listing (marketplaces)
- `[ ]` Buyer–seller messages and first transaction (marketplaces)

**Content / lead-generation site**
- `[ ]` Form submitted
- `[ ]` Newsletter signup
- `[ ]` Call or meeting booked
- `[ ]` File downloaded
- `[ ]` Lead became a customer (offline or CRM step)

---

# 4. CUSTOMER JOURNEY AND FUNNEL ⚡

> **Goal of this section:** Draw the path a person walks from "never heard of us" to "happy customer".

**Q4.1 — List the journey steps in order.**
- *Why we ask:* Each step becomes something we can count and improve.
- *Example for a SaaS app:* Visit site → Click "Start free" → Create account → Verify email → Finish setup → Use main feature → Add card → Pay → Use again in week 2.

| Step # | Step name | Where does it happen? | Which micro/macro conversion is it? | Event name (from Section 5) |
|---|---|---|---|---|
| 1 | ➡️ | ➡️ | ➡️ | ➡️ |
| 2 | ➡️ | ➡️ | ➡️ | ➡️ |
| 3 | ➡️ | ➡️ | ➡️ | ➡️ |
| 4 | ➡️ | ➡️ | ➡️ | ➡️ |
| 5 | ➡️ | ➡️ | ➡️ | ➡️ |
| 6 | ➡️ | ➡️ | ➡️ | ➡️ |
| 7 | ➡️ | ➡️ | ➡️ | ➡️ |
| 8 | ➡️ | ➡️ | ➡️ | ➡️ |
| 9 | ➡️ | ➡️ | ➡️ | ➡️ |
| 10 | ➡️ | ➡️ | ➡️ | ➡️ |

**Q4.2 — Where do you think people get stuck or leave? (best guess)**
- *Why we ask:* These are the first places to watch closely.
- ➡️ Your answer:

**Q4.3 — Are there different journeys for different people?**
- *Example:* "Buyers and sellers", "Free users and business users", "People from ads and people from friends".

| Journey name | Who | Steps that are different |
|---|---|---|
| ➡️ | ➡️ | ➡️ |
| ➡️ | ➡️ | ➡️ |

**Q4.4 — Is there any step that happens OFF our product?**
- *Example:* "Sales call", "bank transfer", "in-store pickup", "customer pays by invoice".
- `[ ]` No
- `[ ]` Yes → How will we record it? ➡️ (Example: "Sales rep marks it in the CRM, which sends an event.")

**Q4.5 — Can a person complete the funnel in more than one session or on more than one device?**
- `[ ]` No
- `[ ]` Yes → How long can the journey take? ➡️ (Example: "Up to 30 days between first visit and purchase.")
- **How will we connect the same person across devices?** ➡️ (Example: "By user ID after login.")

**Q4.6 — Draw the funnel (optional but helpful).**

```
[ Visit ] → [ Signup ] → [ Activate ] → [ Pay ] → [ Come back ]
   ???%        ???%          ???%         ???%        ???%
```
➡️ Replace the steps above with yours:

```
(your funnel here)
```

---

# 5. EVENT TRACKING PLAN ⚡

> **Goal of this section:** This is the *heart* of the document. Every action we record has one row. If it is not in this table, it is not tracked.

## 5.1 Naming rules (read before filling the table)

| Rule | Good example | Bad example |
|---|---|---|
| Use **Object + Past-tense action** | `Account Created` | `create_account_click_button` |
| Use **Title Case** with spaces (or snake_case — pick ONE style for the whole project) | `Order Completed` | `orderCOMPLETED` |
| Describe **what happened**, not which button | `Checkout Started` | `Blue Button Clicked` |
| Keep names **short** (max 40 characters) | `Trial Started` | `User_Has_Successfully_Started_Their_Free_Trial` |
| Never put **personal data** in an event name | `Form Submitted` | `Form Submitted by john@mail.com` |
| Never reuse a name for two different things | one name = one meaning | |

➡️ **Our chosen naming style (circle one):** `[ ] Title Case With Spaces` `[ ] snake_case`

## 5.2 The event table

> **How to fill each column**
> - **Event ID:** `E01`, `E02`, … (never reuse an ID)
> - **Event name:** following the naming rules above
> - **When exactly does it fire?** Write it so a stranger could test it
> - **Where?** Web / iOS / Android / Server
> - **Key properties:** The extra details (Section 6)
> - **Conversion?** `M` = macro, `m` = micro, `-` = not a conversion
> - **Priority:** `P0` = must have before launch, `P1` = needed before first 100 customers, `P2` = nice to have
> - **Status:** `Planned` / `Built` / `Tested` / `Live` / `Retired`

| Event ID | Event name | When exactly does it fire? | Where? | Key properties | Conversion? | Priority | Status | Owner |
|---|---|---|---|---|---|---|---|---|
| E01 | *Page Viewed* | *Every time a page finishes loading* | *Web* | *page_name, url* | *-* | *P1* | *Planned* | *Dev* |
| E02 | *Account Created* | *After the server confirms the new account is saved* | *Server* | *signup_method, plan* | *m* | *P0* | *Planned* | *Dev* |
| E03 | *Order Completed* | *After the payment provider confirms money received* | *Server* | *order_id, revenue, currency* | *M* | *P0* | *Planned* | *Dev* |
| E04 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E05 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E06 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E07 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E08 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E09 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E10 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E11 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E12 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E13 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E14 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| E15 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |

> Need more rows? Copy the last row and keep numbering.

## 5.3 Event idea checklist (tick the ones you need, then add them to the table)

> **Why we give this:** Beginners forget important events. This is a menu to remind you.

**For every product**
- `[ ]` Page / Screen Viewed
- `[ ]` Call To Action Clicked (the main button)
- `[ ]` Signup Started
- `[ ]` Account Created
- `[ ]` Logged In
- `[ ]` Logged Out
- `[ ]` Email Verified
- `[ ]` Onboarding Started / Step Completed / Completed / Skipped
- `[ ]` Key Feature Used (the thing that gives value)
- `[ ]` Invite Sent
- `[ ]` Error Shown (user saw an error)
- `[ ]` Support Contacted
- `[ ]` Feedback Submitted

**For money**
- `[ ]` Pricing Page Viewed
- `[ ]` Plan Selected
- `[ ]` Checkout Started
- `[ ]` Payment Info Added
- `[ ]` Payment Failed
- `[ ]` Order / Subscription Completed
- `[ ]` Subscription Renewed
- `[ ]` Subscription Cancelled
- `[ ]` Refund Issued
- `[ ]` Coupon Applied

**For e-commerce / marketplace**
- `[ ]` Product Viewed
- `[ ]` Product Searched
- `[ ]` Product Added To Cart
- `[ ]` Product Removed From Cart
- `[ ]` Cart Viewed
- `[ ]` Shipping Info Added
- `[ ]` Order Shipped / Delivered
- `[ ]` Review Left
- `[ ]` Listing Created (seller)
- `[ ]` Message Sent (buyer ↔ seller)

**For mobile apps**
- `[ ]` App Installed
- `[ ]` App Opened
- `[ ]` Push Permission Granted / Denied
- `[ ]` Push Notification Opened
- `[ ]` Deep Link Opened
- `[ ]` App Updated
- `[ ]` App Uninstalled (if the tool can detect it)

**For lead-generation / content sites**
- `[ ]` Form Started
- `[ ]` Form Submitted
- `[ ]` Newsletter Subscribed
- `[ ]` Content Downloaded
- `[ ]` Video Played / Completed
- `[ ]` Meeting Booked
- `[ ]` Phone Number Clicked
- `[ ]` Lead Qualified (by sales)
- `[ ]` Lead Became Customer

## 5.4 Event detail cards for P0 events

> For each **P0** event, fill one card. This is what the developer or AI agent will build from.

### Card for event: ➡️ (copy this card for each P0 event)

| Question | Your answer |
|---|---|
| Event ID and name | ➡️ |
| Plain-words description | ➡️ |
| Trigger: the exact moment it fires | ➡️ |
| Fires from (browser / app / server / webhook) | ➡️ |
| Must NOT fire when… | ➡️ *(Example: "page is refreshed", "test user", "payment fails")* |
| Fires how many times per user? | `[ ]` Once ever `[ ]` Once per session `[ ]` Every time |
| Required properties | ➡️ |
| Optional properties | ➡️ |
| Example of a correct event (fill it like a receipt) | ➡️ *(Example: `Order Completed — order_id: 1042, revenue: 29.00, currency: USD`)* |
| Which tools receive it? | ➡️ |
| Is it sent to ad platforms? | `[ ]` No `[ ]` Yes → which: ➡️ |
| Does it need user consent first? | `[ ]` Yes `[ ]` No |
| How do we test it? | ➡️ |

---

# 6. PROPERTIES, IDENTITY, AND NAMING RULES

> **Goal of this section:** Make sure every event carries the same helpful details, and every person is recognised correctly.

## 6.1 Properties that go on EVERY event

| Property | What it holds | Example | Include? |
|---|---|---|---|
| `timestamp` | When it happened | `2026-10-18T14:03:00Z` | `[x]` always |
| `user_id` | Our internal ID for a logged-in person | `u_48291` | `[ ]` |
| `anonymous_id` | Temporary ID for people not logged in | `a_f83k29` | `[ ]` |
| `session_id` | Groups events from one visit | `s_77310` | `[ ]` |
| `platform` | web, ios, android, server | `web` | `[ ]` |
| `app_version` | Which version of the product | `2.4.1` | `[ ]` |
| `page_url` / `screen_name` | Where it happened | `/pricing` | `[ ]` |
| `utm_source`, `utm_medium`, `utm_campaign` | Campaign labels (see Section 7) | `google`, `cpc`, `spring_sale` | `[ ]` |
| `device_type` | phone, tablet, desktop | `phone` | `[ ]` |
| `country` | Country (approximate) | `US` | `[ ]` |
| Other: ➡️ | ➡️ | ➡️ | `[ ]` |

## 6.2 Properties for money events

| Property | Example | Rule |
|---|---|---|
| `order_id` | `1042` | Must be unique. Prevents counting the same sale twice. |
| `revenue` | `29.00` | A number, no currency symbol, no commas. |
| `currency` | `USD` | Three-letter code. |
| `plan` / `product_id` | `pro_monthly` | Same names as in the billing system. |
| `coupon_code` | `WELCOME10` | Leave empty if none. |
| `is_first_purchase` | `true` | Helps spot new vs returning customers. |
| Other: ➡️ | ➡️ | ➡️ |

**Q6.1 — Is revenue recorded before or after tax, discounts, and fees?**
- ➡️ Your answer: *(Example: "After discounts, before tax and payment fees.")*

**Q6.2 — Which currency do we report in, and how do we convert other currencies?**
- ➡️ Your answer:

## 6.3 Identity: how do we know who is who?

**Q6.3 — What is the permanent ID for a person?**
- *Why we ask:* If the same person has two IDs, we will count them twice.
- *Example:* "The `id` column in our users table. Never the email."
- ➡️ Your answer:

**Q6.4 — What happens to tracking when someone who is not logged in later signs up?**
- *Example:* "We link the anonymous ID to the new user ID at the moment of signup, so earlier visits are credited."
- ➡️ Your answer:

**Q6.5 — What happens if someone uses two devices?**
- ➡️ Your answer:

**Q6.6 — How do we treat team / company accounts?**
- `[ ]` Not applicable (individuals only)
- `[ ]` Yes → What is the group ID? ➡️ How do we link people to a company? ➡️

**Q6.7 — How do we exclude our own team and test accounts from the numbers?**
- *Example:* "Any user with an email ending in `@ourcompany.com` gets `is_internal = true` and is filtered out of dashboards."
- ➡️ Your answer:

## 6.4 Property naming rules

- Use `snake_case` for property names (`order_id`, not `OrderID`).
- Use the same property name for the same thing everywhere (`plan`, never `plan` in one place and `tier` in another).
- Use the right type: numbers as numbers, true/false as booleans, dates as ISO dates.
- Never store free-typed personal text (names, emails, messages) as a property unless Section 8 allows it.
- Keep the list of allowed values written down:

| Property | Allowed values |
|---|---|
| `signup_method` | ➡️ *(Example: email, google, apple)* |
| `plan` | ➡️ |
| `platform` | ➡️ |
| ➡️ | ➡️ |

---

# 7. ATTRIBUTION: UTM AND CHANNELS ⚡

> **Goal of this section:** Know *where each customer came from*, so we spend money on what works.

## 7.1 Channels

**Q7.1 — Which ways will we try to get customers? (tick all, add the owner)**

| Channel | Using it? | Owner | Monthly budget |
|---|---|---|---|
| Organic search (Google / Bing, SEO) | `[ ]` | ➡️ | ➡️ |
| Paid search ads | `[ ]` | ➡️ | ➡️ |
| Paid social ads (Meta, TikTok, LinkedIn…) | `[ ]` | ➡️ | ➡️ |
| Organic social posts | `[ ]` | ➡️ | ➡️ |
| Email newsletter | `[ ]` | ➡️ | ➡️ |
| Influencers / creators | `[ ]` | ➡️ | ➡️ |
| Affiliates / partners | `[ ]` | ➡️ | ➡️ |
| Word of mouth / referral program | `[ ]` | ➡️ | ➡️ |
| App store search / ads | `[ ]` | ➡️ | ➡️ |
| Content marketing / blog / YouTube | `[ ]` | ➡️ | ➡️ |
| Communities (Reddit, Discord, forums) | `[ ]` | ➡️ | ➡️ |
| Direct sales / outbound | `[ ]` | ➡️ | ➡️ |
| Offline (events, flyers, QR codes) | `[ ]` | ➡️ | ➡️ |
| Other: ➡️ | `[ ]` | ➡️ | ➡️ |

## 7.2 UTM rules (the labels on links)

> **Simple explanation:** A UTM is a tail added to a link, like `?utm_source=instagram&utm_medium=social&utm_campaign=launch_week`. When someone clicks, we learn where they came from.

| UTM field | What it means | Rule for us | Example |
|---|---|---|---|
| `utm_source` | The place the click came from | lowercase, no spaces | `instagram` |
| `utm_medium` | The type of channel | pick from the list below | `paid_social` |
| `utm_campaign` | The name of the campaign | `topic_month_year` | `launch_oct_2026` |
| `utm_content` *(optional)* | Which ad or button | short label | `video_a` |
| `utm_term` *(optional)* | Paid search keyword | the keyword | `dog_walker` |

**Q7.2 — Allowed `utm_medium` values (edit this list):**
- `organic_search`, `paid_search`, `paid_social`, `organic_social`, `email`, `referral`, `affiliate`, `influencer`, `display`, `qr_offline`
- ➡️ Add or remove:

**Q7.3 — Who creates and approves campaign links?**
- ➡️ Your answer:

**Q7.4 — Where do we keep the list of all links we created?**
- ➡️ Your answer: *(Example: "Shared spreadsheet called 'UTM Register' — link here.")*

**Q7.5 — How is a conversion credited to a channel? (attribution model)**
- *Why we ask:* If someone saw an ad, then later clicked an email, then bought, who gets the credit?
- `[ ]` **Last click** — credit goes to the final channel before the win (simplest)
- `[ ]` **First click** — credit goes to the first channel that brought them
- `[ ]` **Both reported side by side** (recommended when starting)
- `[ ]` Other: ➡️

**Q7.6 — Attribution window (how long after a click do we still give credit?)**
- *Example:* "7 days after a click, 1 day after an ad view."
- ➡️ Your answer:

**Q7.7 — Where do we store the first-touch source so it is never lost?**
- *Example:* "We save the first UTM values in the user profile when the account is created."
- ➡️ Your answer:

**Q7.8 — How do we track channels with no link? (word of mouth, direct)**
- *Example:* "A 'How did you hear about us?' question at signup."
- `[ ]` Signup question → Options: ➡️
- `[ ]` Referral codes → Format: ➡️
- `[ ]` Promo codes per channel
- `[ ]` Other: ➡️

**Q7.9 — Mobile attribution (only if you have a mobile app)**
- `[ ]` N/A — no mobile app
- Which tool tells us which ad caused an install? ➡️
- How do deep links work? ➡️

**Q7.10 — Sending conversions back to ad platforms**

| Platform | Which events do we send back? | How? (browser pixel / server API) | Consent needed? |
|---|---|---|---|
| ➡️ | ➡️ | ➡️ | ➡️ |
| ➡️ | ➡️ | ➡️ | ➡️ |

> Avoid sending the same conversion twice (browser + server). Use a shared `event_id` so the platform can remove duplicates.

---

# 8. PRIVACY, CONSENT, AND COMPLIANCE ⚡

> **Goal of this section:** Collect only what we are allowed to collect and treat people's data with respect.
> ⚠️ **This is a planning aid, not legal advice. Ask a qualified lawyer or privacy professional to review.**

**Q8.1 — What personal information do we collect?**

| Data | Collected? | Why we need it | Sent to analytics tools? |
|---|---|---|---|
| Name | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |
| Email | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |
| Phone number | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |
| Home / delivery address | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |
| Payment details | `[ ]` | ➡️ | ❌ Never |
| Exact location (GPS) | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |
| IP address | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |
| Device identifiers (advertising ID, etc.) | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |
| Health, financial, or children's data | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |
| Other: ➡️ | `[ ]` | ➡️ | `[ ]` Yes `[ ]` No |

> **Golden rules:**
> 1. Never send passwords, full card numbers, government IDs, or health details to analytics tools.
> 2. If you can track without personal data, do.
> 3. If you hash an email (scramble it) before sending to ad platforms, write down how.

**Q8.2 — Which laws or rules might apply? (tick all that may apply; confirm with a professional)**
- `[ ]` GDPR (European Union / UK)
- `[ ]` CCPA / CPRA (California) and other US state privacy laws
- `[ ]` COPPA (children under 13 in the US)
- `[ ]` HIPAA (US health information)
- `[ ]` PIPEDA / Quebec Law 25 (Canada)
- `[ ]` LGPD (Brazil)
- `[ ]` Apple App Tracking Transparency / Google Play data safety rules
- `[ ]` Industry rules (finance, education, etc.): ➡️
- `[ ]` Other: ➡️
- `[ ]` Not sure → `TBD — Owner: ___ — Due: ___`

**Q8.3 — Consent: when must we ask permission before tracking?**
- `[ ]` Cookie / tracking banner on the website
- `[ ]` Consent screen inside the app
- `[ ]` Only for marketing / ad tracking (not basic product analytics)
- `[ ]` Not required (explain why): ➡️

**Q8.4 — What happens when a user says NO to tracking?**
- *Why we ask:* The product must still work, and we must truly stop tracking.
- *Example:* "No marketing tags load. Only anonymous, essential counts are recorded."
- ➡️ Your answer:

**Q8.5 — Which tool manages consent?** (Example: a cookie banner tool)
- ➡️ Your answer:

**Q8.6 — Where do we record that a user gave or withdrew consent, and when?**
- ➡️ Your answer:

**Q8.7 — How can a user ask us to delete or download their data?**
- ➡️ Your answer: *(Example: "Email privacy@ourcompany.com; we reply within 30 days; we delete in the database and analytics tools.")*

**Q8.8 — How long do we keep tracking data?**
- ➡️ Your answer: *(Example: "26 months in the analytics tool, then auto-deleted.")*

**Q8.9 — Where is the data stored (country / region)?**
- ➡️ Your answer:

**Q8.10 — Do we share data with outside companies?**
- `[ ]` No
- `[ ]` Yes → list them and why:

| Company | What data | Why | Agreement signed? |
|---|---|---|---|
| ➡️ | ➡️ | ➡️ | `[ ]` |
| ➡️ | ➡️ | ➡️ | `[ ]` |

**Q8.11 — Is our privacy policy updated to describe this tracking?**
- `[ ]` Yes — link: ➡️
- `[ ]` No → `TBD — Owner: ___ — Due: ___`

**Q8.12 — Are children ever users?**
- `[ ]` No (we block / do not target under-age users)
- `[ ]` Yes → Extra rules: ➡️

---

# 9. LIFECYCLE PLAN: FROM FIRST IDEA TO CUSTOMER #500

> **Goal of this section:** Show *what happens with tracking at each stage* of an AI-driven development life cycle. Think of it as a staircase: Plan → Build → Test → Launch → Customers 1–500.
> **How to use it:** At each phase, answer the questions and tick the checklist. Do not move on until the phase is done.

```
PLAN  →  BUILD  →  TEST  →  LAUNCH  →  CUSTOMERS 1–500  →  BEYOND 500
```

## 9.0 AI-driven workflow overview

| Phase | What the human does | What the AI agent does | Output of the phase |
|---|---|---|---|
| **Plan** | Answers the questions in this file | Checks for gaps and conflicts, suggests missing events | A filled, approved plan |
| **Build** | Reviews and approves | Writes tracking code from Section 5 | Tracking code ready |
| **Test** | Confirms the results | Runs checks, finds mistakes, suggests fixes | A passed QA report (Section 10) |
| **Launch** | Gives the go / no-go | Monitors events and raises alerts | Live tracking and dashboards |
| **Customers 1–500** | Reviews numbers weekly | Prepares reports and spots problems | Decisions based on real data |

**Q9.1 — Which AI tools/agents will help? (names and what each is allowed to do)**

| AI tool / agent | Allowed to… | NOT allowed to… |
|---|---|---|
| ➡️ | ➡️ *(Example: write tracking code in a branch)* | ➡️ *(Example: change live settings alone)* |
| ➡️ | ➡️ | ➡️ |

**Q9.2 — Who must approve before AI-written tracking code goes live?**
- ➡️ Your answer:

## 9.1 PHASE 1 — PLAN

**Goal:** Everything in this file is decided before code is written.

**Q9.3 — Do we have a sketch, prototype, or list of screens/pages?**
- `[ ]` Yes — link: ➡️
- `[ ]` No → `TBD — Owner: ___ — Due: ___`

**Q9.4 — What date should Plan be finished?**
- ➡️ Your answer:

**Plan-phase checklist**
- `[ ]` Sections 1–8 are filled in
- `[ ]` Macro and micro conversions are agreed by the business owner
- `[ ]` Every journey step has an event in Section 5
- `[ ]` Tool choices are made (Section 3)
- `[ ]` Privacy review started (Section 8)
- `[ ]` Open questions are listed with owners (Section 14)
- `[ ]` Status moved to **In review**

## 9.2 PHASE 2 — BUILD

**Goal:** Tracking code is written alongside the product, not bolted on later.

**Q9.5 — Where will the tracking code live?**
- *Example:* "One file called `analytics` that every part of the app calls, so there is only one place to change."
- ➡️ Your answer:

**Q9.6 — How will developers/AI avoid typing event names wrong?**
- *Example:* "A single list of allowed event names in code; anything else causes a warning."
- ➡️ Your answer:

**Q9.7 — Do we have separate environments?**

| Environment | Used for | Analytics project / key name (not the secret itself) |
|---|---|---|
| Development | Building | ➡️ |
| Staging / Test | Testing | ➡️ |
| Production | Real customers | ➡️ |

> **Rule:** Test data must NEVER go into the production analytics project.

**Q9.8 — Where are secret keys stored?**
- ➡️ Your answer: *(Example: "In the hosting platform's secret manager. Never in the code or this file.")*

**Q9.9 — What does "code review" look like for tracking changes?**
- ➡️ Your answer:

**Build-phase checklist**
- `[ ]` All **P0** events are built
- `[ ]` Events match names and properties in Section 5 exactly
- `[ ]` Money events fire from the server or payment webhook
- `[ ]` Consent logic built (Section 8)
- `[ ]` Test and production data are separated
- `[ ]` User identity is set correctly (Section 6)
- `[ ]` UTM / first-source values are saved (Section 7)
- `[ ]` Event status in Section 5 updated to `Built`
- `[ ]` Change Log updated

## 9.3 PHASE 3 — TEST

**Goal:** Prove every important event works *before* real customers arrive.

*(The detailed test list is in Section 10.)*

**Q9.10 — Who tests, and when?**
- ➡️ Your answer:

**Q9.11 — How many "pretend customers" will we run through the whole funnel?**
- *Example:* "At least 10 test runs on each device type."
- ➡️ Your answer:

**Test-phase checklist**
- `[ ]` Section 10 is completely ticked
- `[ ]` All **P0** events show `Tested`
- `[ ]` Numbers from analytics tool match numbers in our database/payment tool (within an agreed gap)
- `[ ]` No personal data appears where it should not
- `[ ]` Dashboards show test data correctly
- `[ ]` Known problems are written in Section 14

## 9.4 PHASE 4 — LAUNCH

**Goal:** Go live safely and watch closely.

**Q9.12 — What is the launch date and time?**
- ➡️ Your answer:

**Q9.13 — Launch type**
- `[ ]` Private beta (invited people only)
- `[ ]` Public soft launch (limited promotion)
- `[ ]` Full public launch

**Q9.14 — Who is "on watch" during the first 72 hours?**
- ➡️ Your answer:

**Q9.15 — What would make us pause the launch (stop signs)?**
- *Example:* "Money events not appearing; purchase count in analytics differs from payment tool by more than 5%."
- ➡️ Your answer:

**Q9.16 — What is the rollback plan if tracking breaks?**
- ➡️ Your answer:

**Launch-phase checklist**
- `[ ]` Production tracking switched on
- `[ ]` Test accounts and internal users are filtered out
- `[ ]` First real event seen in the live dashboard
- `[ ]` First real money event matched with the payment tool
- `[ ]` Alerts for missing events are on (Section 13)
- `[ ]` Privacy policy and consent banner are live
- `[ ]` Ad platform conversion tags are verified (if ads are running)
- `[ ]` Status in this file moved to **Approved**
- `[ ]` Launch recorded in the Change Log

## 9.5 PHASE 5 — CUSTOMERS 1 TO 500

**Goal:** Learn quickly and fix what hurts conversions.

*(Milestones and weekly rhythm are in Section 12.)*

**Q9.17 — Who reads the numbers and makes decisions?**
- ➡️ Your answer:

**Q9.18 — How fast must we react to a tracking problem?**
- *Example:* "Money-related problems fixed within 24 hours; others within 1 week."
- ➡️ Your answer:

**Customers 1–500 checklist**
- `[ ]` Weekly review meeting set (Section 12)
- `[ ]` Each milestone has been reviewed
- `[ ]` At least one improvement experiment per month based on the data
- `[ ]` Data quality check done monthly (Section 13)
- `[ ]` File updated after every product change

## 9.6 BEYOND 500

**Q9.19 — What changes after we reach 500 customers?**
- *Example:* "We will add cohort reports, move to a data warehouse, and review privacy again."
- ➡️ Your answer:

---

# 10. QA AND TEST CHECKLIST ⚡

> **Goal of this section:** A step-by-step way to prove the tracking works. Think of it as checking a recipe was followed.

## 10.1 Test setup

**Q10.1 — Where do testers see events as they happen?**
- *Example:* "The 'live events' or 'debug' view of our analytics tool."
- ➡️ Your answer:

**Q10.2 — What test accounts and test payment methods will we use?**
- *Why we ask:* So testing does not cost real money or pollute real data.
- ➡️ Your answer: *(Example: "Payment provider's test mode and its test card numbers.")*

**Q10.3 — Which devices and browsers must we test?**

| Device / browser | Tested? | Tester | Date | Result |
|---|---|---|---|---|
| Chrome (computer) | `[ ]` | ➡️ | ➡️ | ➡️ |
| Safari (computer) | `[ ]` | ➡️ | ➡️ | ➡️ |
| Firefox / Edge | `[ ]` | ➡️ | ➡️ | ➡️ |
| iPhone (Safari) | `[ ]` | ➡️ | ➡️ | ➡️ |
| Android (Chrome) | `[ ]` | ➡️ | ➡️ | ➡️ |
| iOS app | `[ ]` | ➡️ | ➡️ | ➡️ |
| Android app | `[ ]` | ➡️ | ➡️ | ➡️ |
| With an ad blocker turned on | `[ ]` | ➡️ | ➡️ | ➡️ |
| With cookies refused | `[ ]` | ➡️ | ➡️ | ➡️ |
| Slow internet | `[ ]` | ➡️ | ➡️ | ➡️ |

## 10.2 Event-by-event test sheet

> For each event, do the action, then check the analytics tool. Write what you saw.

| Event ID | Event name | Action to perform | Expected result | Fires exactly once? | Properties correct? | Result | Tester | Date |
|---|---|---|---|---|---|---|---|---|
| E01 | ➡️ | ➡️ | ➡️ | `[ ]` | `[ ]` | `[ ] Pass` `[ ] Fail` | ➡️ | ➡️ |
| E02 | ➡️ | ➡️ | ➡️ | `[ ]` | `[ ]` | `[ ] Pass` `[ ] Fail` | ➡️ | ➡️ |
| E03 | ➡️ | ➡️ | ➡️ | `[ ]` | `[ ]` | `[ ] Pass` `[ ] Fail` | ➡️ | ➡️ |
| E04 | ➡️ | ➡️ | ➡️ | `[ ]` | `[ ]` | `[ ] Pass` `[ ] Fail` | ➡️ | ➡️ |
| E05 | ➡️ | ➡️ | ➡️ | `[ ]` | `[ ]` | `[ ] Pass` `[ ] Fail` | ➡️ | ➡️ |
| E06 | ➡️ | ➡️ | ➡️ | `[ ]` | `[ ]` | `[ ] Pass` `[ ] Fail` | ➡️ | ➡️ |
| E07 | ➡️ | ➡️ | ➡️ | `[ ]` | `[ ]` | `[ ] Pass` `[ ] Fail` | ➡️ | ➡️ |
| E08 | ➡️ | ➡️ | ➡️ | `[ ]` | `[ ]` | `[ ] Pass` `[ ] Fail` | ➡️ | ➡️ |

## 10.3 Bad-situation tests (try to break it)

- `[ ]` Refresh the page on the "thank you" page — does the conversion count twice? (It must not.)
- `[ ]` Press the browser Back button after paying — any duplicate?
- `[ ]` Pay with a card that fails — is `Payment Failed` recorded and no `Order Completed`?
- `[ ]` Refund a test purchase — is revenue reduced correctly?
- `[ ]` Sign up twice with the same email — is it counted once?
- `[ ]` Leave halfway and return the next day — is the same person recognized?
- `[ ]` Switch from logged-out to logged-in — are earlier visits linked?
- `[ ]` Open a campaign link with UTMs — are UTMs saved on the signup?
- `[ ]` Open a link with **no** UTMs — does it show as "direct" (not broken)?
- `[ ]` Decline consent — are marketing tags really off?
- `[ ]` Accept, then withdraw consent — does tracking stop?
- `[ ]` Turn off internet in the app, do an action, turn it back on — does the event arrive once?
- `[ ]` Use an internal/test account — is it excluded from reports?
- `[ ]` Look inside events — is there any email, password, or card number? (There must not be.)
- `[ ]` Switch currency or language — is revenue still correct?

## 10.4 Number matching (reconciliation)

> Compare the number in the analytics tool with the "source of truth" from Section 3.

| Metric | Analytics tool says | Source of truth says | Gap (%) | Allowed gap | Pass? |
|---|---|---|---|---|---|
| Signups | ➡️ | ➡️ | ➡️ | ➡️ *(e.g., 2%)* | `[ ]` |
| Orders | ➡️ | ➡️ | ➡️ | ➡️ *(e.g., 1%)* | `[ ]` |
| Revenue | ➡️ | ➡️ | ➡️ | ➡️ *(e.g., 1%)* | `[ ]` |
| Ad conversions in ad platform | ➡️ | ➡️ | ➡️ | ➡️ *(e.g., 10–15%)* | `[ ]` |

## 10.5 Definition of "Tested" (Done criteria)

An event is `Tested` only when **all** are true:
- `[ ]` It fires at the right moment
- `[ ]` It fires the right number of times
- `[ ]` Required properties are present and correct
- `[ ]` No personal data leaks
- `[ ]` It respects consent rules
- `[ ]` It appears in the dashboard
- `[ ]` Someone other than the builder verified it

## 10.6 Bug log

| Bug # | What went wrong | Event | Severity (High/Med/Low) | Found by | Fixed by | Date fixed | Re-tested? |
|---|---|---|---|---|---|---|---|
| 1 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | `[ ]` |
| 2 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | `[ ]` |
| 3 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | `[ ]` |

---

# 11. DASHBOARDS AND REPORTS

> **Goal of this section:** Decide what we look at, how often, and who looks.

**Q11.1 — What questions must the numbers answer?**
- *Why we ask:* A dashboard without a question is just decoration.
- *Example:* "How many visitors become paying customers? Which channel brings the best customers? Where do people quit in checkout?"
- ➡️ Your answer:

**Q11.2 — Dashboard plan**

| Dashboard / report | Question it answers | Main numbers | Who looks | How often | Tool |
|---|---|---|---|---|---|
| Executive summary | *Are we on track for 500?* | *Customers, revenue, conversion rate* | ➡️ | Weekly | ➡️ |
| Funnel | *Where do people drop off?* | *Step-by-step conversion %* | ➡️ | Weekly | ➡️ |
| Channels | *Which source works?* | *Visits, signups, customers, cost per customer by channel* | ➡️ | Weekly | ➡️ |
| Activation | *Do new users get value?* | *% reaching the activation moment* | ➡️ | Weekly | ➡️ |
| Revenue | *How much and from what?* | *Revenue, refunds, average order value* | ➡️ | Weekly | ➡️ |
| Retention | *Do they come back?* | *Day 1 / 7 / 30 return rates* | ➡️ | Monthly | ➡️ |
| Tracking health | *Is tracking still working?* | *Events per day, errors* | ➡️ | Daily | ➡️ |
| ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |

**Q11.3 — The "North Star" number (the ONE number that shows we are winning)**
- *Example:* "Number of customers who booked at least 2 walks in a month."
- ➡️ Your answer:

**Q11.4 — Number definitions (so everyone reads numbers the same way)**

| Metric | Exact formula | Example |
|---|---|---|
| Conversion rate | ➡️ *(e.g., customers ÷ visitors in same period × 100)* | ➡️ |
| Cost per customer | ➡️ *(e.g., ad spend ÷ new customers)* | ➡️ |
| Average order value | ➡️ | ➡️ |
| Churn / cancel rate | ➡️ | ➡️ |
| Retention (Day N) | ➡️ | ➡️ |
| ➡️ | ➡️ | ➡️ |

**Q11.5 — Alerts: who is told when a number jumps or drops suddenly?**
- *Example:* "If signups drop more than 40% from the same day last week, email the product owner."
- ➡️ Your answer:

**Q11.6 — Where are reports shared, and who can see them?**
- ➡️ Your answer:

---

# 12. FIRST 500 CUSTOMERS: MILESTONES AND WEEKLY RHYTHM ⚡

> **Goal of this section:** Combine big checkpoints with a regular weekly habit so learning never stops.

## 12.1 The finish line

| Item | Your answer |
|---|---|
| Definition of "customer" (from B.2) | ➡️ |
| Target number | 500 |
| Target date | ➡️ |
| Owner of this goal | ➡️ |

## 12.2 Milestone checkpoints

> At each milestone, stop and review. Fill in the "What we saw" column when you reach it.

| Milestone | Date reached | What to check | What we saw | Decision / next action |
|---|---|---|---|---|
| **0 — Before launch** | ➡️ | All P0 events tested; dashboards ready; consent working | ➡️ | ➡️ |
| **1st customer** | ➡️ | Did the first real money event arrive correctly? Did we match it with the payment tool? | ➡️ | ➡️ |
| **10 customers** | ➡️ | Talk to every customer. Is each journey visible in the data? Any missing events? | ➡️ | ➡️ |
| **50 customers** | ➡️ | First reliable funnel numbers. Biggest drop-off step? Which channel is best? | ➡️ | ➡️ |
| **100 customers** | ➡️ | Activation rate, cost per customer, refunds. Retire useless events. | ➡️ | ➡️ |
| **250 customers** | ➡️ | Retention at Day 7 and Day 30. Compare cohorts (groups by signup week). | ➡️ | ➡️ |
| **500 customers** | ➡️ | Did we hit the goal? What worked? What is the plan for the next stage? | ➡️ | ➡️ |

## 12.3 What to track at each stage (guidance)

| Stage | Main focus | Typical tracking questions |
|---|---|---|
| 0–10 | "Does the journey work at all?" | Can every customer's journey be seen end to end? Are there missing or duplicate events? |
| 10–50 | "Where do people struggle?" | Which step loses the most people? How long to activate? |
| 50–100 | "Which channels are worth paying for?" | Cost per customer by channel; best-quality channel |
| 100–250 | "Do customers stay?" | Retention, repeat purchase, cancels, refund reasons |
| 250–500 | "Can this grow steadily?" | Stable conversion rates, predictable channels, healthy data |

## 12.4 Weekly rhythm

**Q12.1 — When is the weekly review?**
- ➡️ Day/time: ➡️ Who attends: ➡️ Length: ➡️

**Weekly review agenda (copy for each week)**
1. How many new customers this week vs target?
2. Funnel: which step improved or worsened?
3. Channels: best and worst performer
4. Tracking health: any missing or strange events?
5. Customer feedback: any quotes that explain the numbers?
6. Decisions: what ONE thing do we change this week?
7. Update this file if tracking changed

**Weekly log**

| Week # | Date | New customers | Total customers | Visitor → customer % | Top channel | Tracking issues? | Decision this week |
|---|---|---|---|---|---|---|---|
| 1 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| 2 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| 3 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| 4 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| 5 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| 6 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| 7 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| 8 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |

> Add more rows as needed.

**Q12.2 — Experiments: how do we test improvements?**
- *Example:* "One change at a time; run for 2 weeks or until 100 conversions; compare before and after."

| Experiment | What we change | Expected effect | Start | End | Result |
|---|---|---|---|---|---|
| ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |

> **Small-numbers warning:** With very few customers, numbers jump around a lot. Do not make big decisions from fewer than ~30 conversions. Mark such numbers as "early signal".

---

# 13. DATA QUALITY AND MAINTENANCE

> **Goal of this section:** Keep tracking correct as the product changes. Tracking rots quietly if nobody looks after it.

**Q13.1 — Who owns data quality?**
- ➡️ Your answer:

**Q13.2 — What happens when the product changes? (checklist for every new feature)**
- `[ ]` Decide if the feature needs events
- `[ ]` Add rows to Section 5 *before* building
- `[ ]` Build and test events
- `[ ]` Update dashboards
- `[ ]` Update privacy notes if new data is collected
- `[ ]` Add a Change Log entry

**Q13.3 — How do we spot broken tracking?**
- *Example:* "Daily check: events per day compared with the last 7 days. Alert if any P0 event drops to zero."
- ➡️ Your answer:

**Q13.4 — Monthly health check (tick each month)**

| Check | Month 1 | Month 2 | Month 3 | Month 4 | Month 5 | Month 6 |
|---|---|---|---|---|---|---|
| All P0 events still fire | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| No duplicate conversions | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Revenue matches payment tool | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| UTM labels follow the rules | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| No personal data leaks | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Unused events removed | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Consent still works | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| This file is up to date | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q13.5 — How do we retire (delete) an event?**
- *Example:* "Mark status `Retired` in Section 5, remove the code, leave the row for history, add Change Log note."
- ➡️ Your answer:

**Q13.6 — How do we rename or change an event without breaking old reports?**
- *Example:* "Never rename. Create a new event, run both for 30 days, then retire the old one."
- ➡️ Your answer:

**Q13.7 — Event versioning**
- Do we keep an `event_version` property? `[ ]` Yes `[ ]` No

**Q13.8 — How do we fix wrong data already collected?**
- *Example:* "Mark affected dates in the dashboard notes; correct from the source of truth."
- ➡️ Your answer:

**Q13.9 — How do we onboard a new team member to this file?**
- ➡️ Your answer:

**Q13.10 — Common data problems (know them so you can spot them)**

| Problem | What it looks like | Typical cause | Fix |
|---|---|---|---|
| Duplicate conversions | Orders higher than the payment tool shows | Event fires twice or page refresh | Use unique `order_id`; deduplicate |
| Missing conversions | Orders lower than payment tool | Ad blocker, consent refusal, code error | Track money on the server |
| "Direct" traffic too high | Most visits show no source | Missing UTMs, redirects drop labels | Fix links; keep UTMs through redirects |
| Spike of strange traffic | Sudden huge visits | Bots or testing | Filter bots; check internal traffic |
| Same person counted twice | More users than real people | No shared ID across devices | Use user ID after login |
| Wrong revenue | Revenue ten times too high or low | Cents vs dollars, currency mix | Agree one unit; document it |
| Events vanished | Zero events after release | Code removed by mistake | Alerts and release test |

---

# 14. RISKS, ASSUMPTIONS, AND OPEN QUESTIONS ⚡

> **Goal of this section:** Nothing is hidden. Every unknown has a name, a person, and a date.

## 14.1 Open questions (copy every `TBD` here)

| # | Question | Where it came from (section) | Owner | Due | Status (Open / Answered) | Answer |
|---|---|---|---|---|---|---|
| 1 | ➡️ | ➡️ | ➡️ | ➡️ | Open | ➡️ |
| 2 | ➡️ | ➡️ | ➡️ | ➡️ | Open | ➡️ |
| 3 | ➡️ | ➡️ | ➡️ | ➡️ | Open | ➡️ |
| 4 | ➡️ | ➡️ | ➡️ | ➡️ | Open | ➡️ |
| 5 | ➡️ | ➡️ | ➡️ | ➡️ | Open | ➡️ |

## 14.2 Assumptions (copy every `ASSUMPTION:` here)

| # | Assumption | Why we believe it | How we will check | Checked on | Still true? |
|---|---|---|---|---|---|
| 1 | ➡️ | ➡️ | ➡️ | ➡️ | `[ ]` |
| 2 | ➡️ | ➡️ | ➡️ | ➡️ | `[ ]` |
| 3 | ➡️ | ➡️ | ➡️ | ➡️ | `[ ]` |

## 14.3 Risks

| # | Risk | Chance (Low/Med/High) | Damage (Low/Med/High) | What we do to prevent it | What we do if it happens | Owner |
|---|---|---|---|---|---|---|
| 1 | *Example:* Ad blockers hide many browser events | High | Med | Track money events on server | Compare with payment tool | ➡️ |
| 2 | *Example:* Privacy law changes or consent rate is low | Med | High | Review quarterly; privacy-friendly tracking | Switch to aggregated reporting | ➡️ |
| 3 | *Example:* Tracking breaks after a release | Med | High | Release checklist and alerts | Hotfix within 24 hours | ➡️ |
| 4 | *Example:* Too few customers to trust the numbers | High | Low | Mark as "early signal" | Talk to customers directly | ➡️ |
| 5 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |
| 6 | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ | ➡️ |

## 14.4 Dependencies (things we are waiting on)

| What we need | From whom | Needed by | Status |
|---|---|---|---|
| ➡️ | ➡️ | ➡️ | ➡️ |
| ➡️ | ➡️ | ➡️ | ➡️ |

## 14.5 Out of scope (things we are choosing NOT to track now)

- *Why we ask:* Saying "no" clearly prevents endless additions.
- ➡️ Your answer: *(Example: "Heatmaps and session recordings — maybe after 500 customers.")*

---

# 15. AI AGENT HANDOFF ⚡

> **Goal of this section:** A short, precise briefing for any AI agent that reads this file. Humans: fill the blanks; AI: follow the rules.

## 15.1 Rules for the AI agent (do not delete)

1. **This file is the single source of truth.** Build only what is written here.
2. **Do not guess.** If something is empty, marked `TBD`, or unclear, STOP and ask a human. List what you are missing.
3. **Do not invent** event names, properties, or conversion definitions. Use exactly what is in Section 5 and Section 6.
4. **Never collect personal data** beyond what Section 8 allows. Never put emails, names, passwords, card numbers, or health data into event properties.
5. **Never commit secrets** (keys, tokens, passwords) to code or to this file.
6. **Respect consent.** Marketing and ad events must not fire without consent (Section 8).
7. **Money events** come from the server or payment webhooks, with a unique `order_id`, never only from the browser.
8. **Work in small steps.** One event at a time, tested before moving on.
9. **Work in non-production first.** Never touch live analytics settings without human approval.
10. **Update this file.** After each change, update event Status (Section 5), the Change Log (A.2), and Completion Tracker (A.1).
11. **Report honestly.** State what was done, what was tested, what failed, and what is still open. Never say "done" if it was not tested.
12. **Stop and ask** before: deleting events, renaming events, changing conversion definitions, sending data to a new outside company, or changing consent behaviour.

## 15.2 Handoff briefing (human fills this before giving the file to an AI agent)

| Question | Your answer |
|---|---|
| What should the AI do right now? | ➡️ *(Example: "Build all P0 events from Section 5.")* |
| Which sections are final and safe to build from? | ➡️ |
| Which sections are NOT final (do not build from them)? | ➡️ |
| Which code location / repository should it work in? | ➡️ |
| Which branch or environment? | ➡️ |
| What tools may it use? | ➡️ |
| What is it NOT allowed to touch? | ➡️ |
| How will you check its work? | ➡️ |
| What should it send back when finished? | ➡️ *(Example: "List of events built, test results, open questions.")* |
| Who does it ask when stuck? | ➡️ |

## 15.3 Ready-to-use prompts (copy and paste)

**Prompt 1 — Check the document for gaps**
```
Read Conversion_Tracking.md completely. List every question that is empty,
marked TBD, or contradicts another section. Do not fill anything in.
Return a numbered list with the section number and what is missing.
```

**Prompt 2 — Suggest missing events**
```
Read Sections 2 and 4 of Conversion_Tracking.md. Compare each macro conversion,
micro conversion, and journey step with the events in Section 5. List any step
that has no event. Suggest event names following Section 5.1. Do not edit the file.
```

**Prompt 3 — Build the tracking**
```
Using only Section 5 (events with Priority P0 and Status Planned), Section 6
(properties and identity), and Section 8 (consent), write the tracking code in
<repository/location>. Build one event at a time. After each event, show how to
test it. Do not invent names. Do not send personal data. Ask me if anything is unclear.
```

**Prompt 4 — Create the test plan**
```
Read Section 5 and Section 10. For each P0 event, write exact step-by-step test
instructions a beginner can follow, plus the result that proves it works.
Include the bad-situation tests from Section 10.3.
```

**Prompt 5 — Weekly report**
```
Using the data I paste below, fill in the weekly log in Section 12.4 and answer the
agenda questions. Mark any number based on fewer than 30 conversions as "early signal".
Flag anything that looks like a tracking problem rather than a real change in behaviour.
```

**Prompt 6 — Monthly health check**
```
Run the checks in Section 13.4 using the information I provide. Report each check as
Pass, Fail, or Cannot Check, with a reason. Update nothing without asking me.
```

## 15.4 When the AI must stop and ask (stop signs)

- Any `TBD` on a P0 event
- Two sections that disagree
- A request to send new data to an outside company
- Anything that touches payments or personal data
- A test that fails twice in a row
- Numbers that differ from the source of truth by more than the allowed gap

---

# 16. REVIEW AND SIGN-OFF ⚡

## 16.1 Final self-check (the person who filled this file ticks every box)

- `[ ]` Every question is answered, or marked `TBD` with an owner and date
- `[ ]` No section is left blank
- `[ ]` Every `TBD` and `ASSUMPTION` is copied into Section 14
- `[ ]` Every journey step has an event
- `[ ]` Every macro conversion is defined with what counts and what does NOT count
- `[ ]` Every P0 event has a detail card
- `[ ]` Naming rules are followed everywhere
- `[ ]` No secrets or personal data are written in this file
- `[ ]` Privacy section was reviewed by someone qualified
- `[ ]` Dashboards and weekly review are scheduled
- `[ ]` The Completion Tracker and Change Log are up to date

## 16.2 The "Stranger Test"

> Give this file to someone who has never seen the project. Ask them to explain back to you: (1) what a conversion is for this product, (2) where customers come from, (3) how we know the tracking is correct. If they struggle, improve the unclear parts.

| Question | Did the stranger understand? | Notes |
|---|---|---|
| What counts as a conversion? | `[ ]` Yes `[ ]` No | ➡️ |
| Where do customers come from? | `[ ]` Yes `[ ]` No | ➡️ |
| How do we know tracking is correct? | `[ ]` Yes `[ ]` No | ➡️ |
| What happens if someone declines tracking? | `[ ]` Yes `[ ]` No | ➡️ |

## 16.3 Approvals

| Role | Name | Decision (Approved / Changes needed) | Date | Comments |
|---|---|---|---|---|
| Business owner | ➡️ | ➡️ | ➡️ | ➡️ |
| Product manager | ➡️ | ➡️ | ➡️ | ➡️ |
| Engineering lead | ➡️ | ➡️ | ➡️ | ➡️ |
| QA lead | ➡️ | ➡️ | ➡️ | ➡️ |
| Privacy / legal | ➡️ | ➡️ | ➡️ | ➡️ |

**Next review date:** ➡️ *(Suggestion: every 3 months, and always after a big product change.)*

---

# APPENDIX

## Appendix A — Example of a finished mini-plan (for inspiration)

**Project:** "WalkMyDog" — mobile app and website to book dog walkers.

| Item | Example answer |
|---|---|
| Macro conversion M1 | Paid Booking Completed — counts when the payment provider confirms payment for a walk |
| Micro conversions | App Installed → Account Created → Dog Profile Added → Walker Searched → Booking Started |
| Activation moment | First booking completed |
| Customer (for the 500 goal) | A person who has paid for at least one walk |
| Source of truth: revenue | Payment provider |
| Channels | Instagram ads, local Facebook groups, referral codes |
| Naming style | Title Case With Spaces |
| Sample events | `App Installed`, `Account Created`, `Dog Profile Added`, `Walker Searched`, `Booking Started`, `Paid Booking Completed`, `Booking Cancelled`, `Review Left` |
| Money events from | Server, using payment webhooks |
| Consent | Banner on website; consent screen in the app; marketing tags only after "Accept" |
| North Star | Customers with 2+ bookings in 30 days |

## Appendix B — Starter event libraries by product type

### SaaS / web app
`Visited Landing Page` · `Signup Started` · `Account Created` · `Email Verified` · `Onboarding Step Completed` · `Onboarding Completed` · `Key Feature Used` · `Teammate Invited` · `Trial Started` · `Plan Selected` · `Checkout Started` · `Subscription Started` · `Subscription Upgraded` · `Subscription Downgraded` · `Subscription Cancelled` · `Payment Failed`

### Mobile app
`App Installed` · `App Opened` · `Account Created` · `Permission Prompt Shown` · `Push Permission Granted` · `Onboarding Completed` · `Key Feature Used` · `Paywall Viewed` · `Trial Started` · `In-App Purchase Completed` · `Subscription Renewed` · `Subscription Cancelled` · `Deep Link Opened`

### E-commerce
`Product Viewed` · `Product Searched` · `Product Added To Cart` · `Cart Viewed` · `Checkout Started` · `Shipping Info Added` · `Payment Info Added` · `Order Completed` · `Order Refunded` · `Review Left` · `Wishlist Added`

### Marketplace
`Buyer Account Created` · `Seller Account Created` · `Seller Verified` · `Listing Created` · `Listing Viewed` · `Message Sent` · `Offer Made` · `Order Completed` · `Payout Sent` · `Review Left` · `Dispute Opened`

### Content / lead-gen
`Page Viewed` · `Content Read (50% scrolled)` · `Form Started` · `Form Submitted` · `Newsletter Subscribed` · `Content Downloaded` · `Meeting Booked` · `Lead Qualified` · `Lead Became Customer`

## Appendix C — Recommended property cheat sheet

| Property | Type | Example |
|---|---|---|
| `order_id` | text | `"1042"` |
| `revenue` | number | `29.00` |
| `currency` | text (3 letters) | `"USD"` |
| `quantity` | whole number | `2` |
| `plan` | text from allowed list | `"pro_monthly"` |
| `signup_method` | text from allowed list | `"google"` |
| `is_first_purchase` | true/false | `true` |
| `utm_source` | text, lowercase | `"instagram"` |
| `error_code` | text | `"card_declined"` |
| `event_id` | unique text (for deduplication) | `"evt_9f3a2"` |

## Appendix D — Quick consent cheat sheet

| Type of tracking | Usually needs consent? | Notes |
|---|---|---|
| Essential (login, security, payment, fraud checks) | Usually no | Still describe it in the privacy policy |
| Basic product analytics | Depends on region and settings | Confirm with a privacy professional |
| Advertising / retargeting pixels | Usually yes in many regions | Must be off until user accepts |
| Cross-site tracking / data sharing | Usually yes | Check platform rules too |
| Children's data | Special rules apply | Get expert advice before collecting |

> ⚠️ Rules differ by country, state, and platform and change over time. This table is a reminder, not legal advice.

## Appendix E — Common beginner mistakes

1. **Tracking everything.** More events ≠ better. Track what helps a decision.
2. **No clear definition of a conversion.** Teams argue later about what the numbers mean.
3. **Counting money from the browser only.** Ad blockers and refreshes break it.
4. **Forgetting to exclude team and test accounts.**
5. **No unique ID per order.** Leads to double counting.
6. **Changing event names casually.** Breaks old reports.
7. **Skipping UTM rules.** Everything becomes "direct".
8. **Ignoring consent.** A legal and trust problem.
9. **Never checking again after launch.** Tracking breaks silently.
10. **Reading too much into tiny numbers.** Wait for enough data.
11. **Writing the plan after the code.** Plan first.
12. **Leaving questions blank.** Blank = guess. Use `TBD` with owner and date.

## Appendix F — Glossary (extended)

| Term | Meaning |
|---|---|
| **A/B test** | Showing two versions to different people to see which works better |
| **Activation** | The first moment a user gets real value |
| **AOV** | Average order value |
| **Bounce** | Visiting one page and leaving |
| **CAC** | Cost to acquire one customer |
| **Cohort** | A group of users who started in the same period |
| **Churn** | Customers who stop paying or using |
| **CTA** | Call to action — the main button |
| **Deduplication** | Making sure one real action is counted once |
| **Deep link** | A link that opens a specific place in an app |
| **First touch / last touch** | The first / the final channel before a conversion |
| **LTV** | Lifetime value — total money a customer brings |
| **Pixel** | A small tracking snippet from an ad platform |
| **Server-side tracking** | Events sent from our server, not the user's device |
| **Session** | One visit or one app use |
| **SDK** | A ready-made code kit for adding a tool to an app |
| **Webhook** | An automatic message from one tool (e.g., payments) to another |

## Appendix G — Where this document connects to others (optional)

| Related document | Link / location | What it covers |
|---|---|---|
| Product requirements | ➡️ | What we are building |
| Privacy policy | ➡️ | What we tell users |
| Analytics tool workspace | ➡️ | Where events appear |
| Dashboard links | ➡️ | Where numbers are shown |
| Launch plan | ➡️ | Marketing and release timing |
| Incident / bug tracker | ➡️ | Where problems are recorded |

---

**END OF DOCUMENT** — Remember: update this file whenever tracking changes. 🎯
