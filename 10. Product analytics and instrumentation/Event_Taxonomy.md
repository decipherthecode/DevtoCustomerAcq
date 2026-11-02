---
document: Event_Taxonomy
template_version: 1.2.0
folder: Product analytics and instrumentation
project_name: "TBD"
project_slug: "TBD"            # lowercase, no spaces, e.g. lemonade_stand
product_type: ["web_app"]      # web_app | mobile_app | marketplace (pick all that apply)
owner: "TBD"                   # one named person, not a team
reviewers: ["TBD"]
status: draft                  # draft | in_review | approved | live | deprecated
document_version: 0.1.0
last_updated: "YYYY-MM-DD"
current_phase: build           # build | qa | beta | launch | growth_to_500
analytics_tool: "TBD"          # name of the tool you send events to (e.g. any tool)
naming_standard: object_action_snake_case
target_customers: 500
---

# How to fill this document

**Read this first. It takes 3 minutes.**

## What is this document?
An **event** is a small note your product writes down when someone does something. Example: someone clicks "Buy" → the product writes down `order_placed`.

This document is the **one master list** of every note (event) your product is allowed to write down, why it is written, and when. Everyone (people and AI helpers) uses this list so nobody has to guess.

## Who uses it?
- **People** answer the questions and write their answers in the boxes.
- **AI agents** read the finished document and use it to write tracking code and tests.

## Quick start in 5 steps (the super-simple version)
1. **Fill the top box** (the lines between the `---` marks). Write your project's name and your name.
2. **Answer Sections 1-3.** They say what you are building and what "success" means.
3. **Write your events in Section 7.** Think: "What do people DO in my product?" Each thing = one event.
4. **Write the extra details in Section 8.** Think: "What would I want to know about that moment?"
5. **Tick the boxes in Section 18.** Then ask a grown-up (or teammate) to check your work.

> **Tip for a first-timer:** Read the Lemonade Stand examples first. They are tiny and show exactly what a good answer looks like. Appendix A has a whole finished copy.

## Short path or full path? (Pick one on day one)
This file is long on purpose, so nobody has to guess. You do **not** have to fill every part at the same time.

| Path | Use it when | Fill these sections | Everything else |
|---|---|---|---|
| **Short path (about 1-2 hours)** | Tiny project, first draft, or `build` / `beta` phase | 1, 2 (Q2.1-Q2.5 only), 3, 4 (just read), 6, 7, 8 (P0 events only), 11 (Q11.1-Q11.2), 18 | Write `N/A for now - short path` |
| **Full path** | Before `launch`, or any project that takes payments or holds personal data | Every section | Nothing skipped |

Before the `launch` phase starts, every project must switch to the **full path**. Write your chosen path here: `YOUR ANSWER HERE`

## Three ways to answer a question
| Type | When to use it | Example |
|---|---|---|
| **A full answer** | You know it | "A customer is someone who paid for one order." |
| **TBD with owner and date** | You do not know yet | `TBD \| owner: Sam \| due: 2026-11-01` |
| **N/A with a reason** | The question does not apply | `N/A - we have no mobile app` |

Never leave a question empty. Empty means "forgot". `TBD` or `N/A` means "thought about it".

## The 6 rules for filling it in
1. **Go in order.** Start at Section 1 and finish at Section 19. Each section asks questions.
2. **Answer under every question.** Replace the text `YOUR ANSWER HERE` with your answer.
3. **Look at the Lemonade Stand example** under each question. Copy its style, not its words.
4. **Never leave a blank.** If you do not know, write `TBD | owner: <name> | due: <date>` and also add it to Section 16 (Open Questions). AI helpers are NOT allowed to guess a `TBD`.
5. **One event = one meaning.** If you cannot say what an event means in one short sentence, split it into two events.
6. **Ask for help early.** If a question confuses you, write `HELP` next to it and tell the owner.

## Words you will see
| Word | Plain meaning |
|---|---|
| Event | A note the product writes when something happens |
| Property | An extra detail attached to an event (like "price" or "size") |
| User | A real person using the product |
| Funnel | A path of steps people follow (visit → sign up → buy) |
| Activation | The first moment a new person gets real value |
| PII | Private info that identifies a person (name, email, phone, address) |
| Phase | A stage of the project (Build, QA, Beta, Launch, Growth to 500) |
| P0 / P1 / P2 | Importance. P0 = must have, P1 = should have, P2 = nice to have |

## Status words you can use
`planned` → `in_build` → `in_qa` → `live` → `deprecated`

## How to know the document is finished
Go to **Section 18 (Ready Checklist)**. When every box is ticked, change `status` at the top to `approved`.

---

# 1. Project Basics

> **Why:** So anyone opening this file knows what product it is about.

**Q1.1 What is the product called, and what does it do in one sentence?**
- *Example (Lemonade Stand):* "Lemonade Stand is a mobile app where neighbors order fresh lemonade from kids nearby."
- Your answer: `YOUR ANSWER HERE`

**Q1.2 Who is the main customer?**
- *Example:* "Parents and neighbors aged 25-60 who live near a participating stand."
- Your answer: `YOUR ANSWER HERE`

**Q1.3 Where does the product run? (tick all)**
- [ ] Website  [ ] iPhone app  [ ] Android app  [ ] Backend/server  [ ] Admin panel  [ ] Other: ____

**Q1.4 What is the goal of this document in one sentence?**
- *Example:* "Make sure we can measure how people find, order, and love Lemonade Stand until we have 500 paying customers."
- Your answer: `YOUR ANSWER HERE`

**Q1.5 Who owns this document, who reviews it, and who has final say?**
| Role | Name | Contact |
|---|---|---|
| Owner (keeps it updated) | TBD | TBD |
| Product reviewer | TBD | TBD |
| Engineering reviewer | TBD | TBD |
| QA reviewer | TBD | TBD |
| Privacy / legal reviewer | TBD | TBD |
| Final approver | TBD | TBD |

**Q1.6 Who does what, from build to the first 500 customers? (R = does the work, A = answers for it, C = gives advice, I = is told)**
| Job | Product | Engineering | AI agent | QA | Privacy / legal | Founder / approver |
|---|---|---|---|---|---|---|
| Fill and update this document | A, R | C | C | C | C | I |
| Decide which events exist (Section 7) | A, R | C | C (may propose) | I | C | I |
| Write the tracking code | I | A | R | I | I | I |
| Test events (Section 13) | I | C | R (automated) | A, R (manual) | I | I |
| Approve privacy rules (Section 11) | C | C | I | I | A, R | I |
| Mark an event `live` | I | C | **Not allowed** | A, R | I | I |
| Watch dashboards and alerts (Section 15) | R | R | I | I | I | A |
| Approve changes and version bumps (Section 17) | A | C | I | C | C | I |
- Your changes to this table (or write `NONE`): `YOUR ANSWER HERE`

---

# 2. The 500-Customer Goal

> **Why:** Every event should help answer a question about getting to 500 customers. If an event helps no question, do not add it.

**Q2.1 What does "a customer" mean for this product? Be exact.**
- *Example:* "A person who completed one paid order that was not refunded within 7 days."
- Your answer: `YOUR ANSWER HERE`

**Q2.2 By what date do you want 500 customers?**
- Your answer: `YYYY-MM-DD`

**Q2.3 What are the 5-8 questions you must be able to answer with data?**
| # | Question | Which stage? | Event(s) that answer it |
|---|---|---|---|
| 1 | *Where do visitors come from?* | Acquisition | `page_viewed` (with `utm_source`) |
| 2 | *How many visitors create an account?* | Acquisition | `signup_completed` |
| 3 | *How many reach their first lemonade order?* | Activation | `order_placed` |
| 4 | *Do people order a second time?* | Retention | `order_placed` (2nd+) |
| 5 | *How much money do we make per customer?* | Revenue | `payment_succeeded` |
| 6 | *Do customers tell friends?* | Referral | `invite_sent`, `invite_accepted` |
| 7 | `YOUR ANSWER HERE` | | |
| 8 | `YOUR ANSWER HERE` | | |

**Q2.4 Fill in the metrics table. (Leave no row empty; use TBD if unsure.)**
| Stage | Metric name | Formula (plain words) | Event(s) used | Target | Review how often |
|---|---|---|---|---|---|
| Acquisition | Visit-to-signup rate | signups ÷ unique visitors | `page_viewed`, `signup_completed` | 8% | Weekly |
| Activation | Activation rate | new users who place 1st order within 7 days ÷ new users | `signup_completed`, `order_placed` | 40% | Weekly |
| Retention | 30-day repeat rate | customers who order again within 30 days ÷ customers | `order_placed` | 25% | Monthly |
| Revenue | Average order value | total paid ÷ number of paid orders | `payment_succeeded` | $6 | Weekly |
| Referral | Invite conversion | invites accepted ÷ invites sent | `invite_sent`, `invite_accepted` | 15% | Monthly |
| Goal | Customers so far | count of unique users with first paid order | `customer_milestone_reached` | 500 | Daily |

Your table (copy the rows above and change them):
| Stage | Metric name | Formula | Event(s) used | Target | Review how often |
|---|---|---|---|---|---|
| | | | | | |

**Q2.5 Which single number tells you "we are winning"? (North Star)**
- *Example:* "Number of orders delivered per week."
- Your answer: `YOUR ANSWER HERE`

**Q2.6 Which "guardrail" numbers must NOT get worse while you chase growth?**
> A guardrail protects quality. Example: you can get more signups by being sloppy, but then people leave.
| Guardrail metric | Formula (plain words) | Event(s) used | Danger line (alert if...) |
|---|---|---|---|
| Payment failure rate | failed payments ÷ payment tries | `payment_failed`, `payment_succeeded` | above 5% |
| Refund rate | refunded orders ÷ paid orders | `order_refunded`, `payment_succeeded` | above 4% |
| Error rate | sessions with an error ÷ all sessions | `error_occurred`, `app_opened` | above 2% |
| Your guardrail | | | |

**Q2.7 Which groups (cohorts) do you want to compare?**
> A cohort is a group of people who started in the same week or came from the same place.
- *Example:* "Compare signups by week, by `source` (ads vs friends), and by `platform` (web vs phone)."
- Your answer: `YOUR ANSWER HERE`

**Q2.8 How did you pick your targets? (Do not invent numbers.)**
| Choose one | What it means |
|---|---|
| `guess` | A first guess. Review after the first 50 users. |
| `benchmark` | Copied from a similar product. Write the source. |
| `own data` | Based on your own past numbers. Write the date range. |
- Your answer (per metric): `YOUR ANSWER HERE`

**Q2.9 What is the "Road to 500" plan by phase?**
| Phase | Customers expected by end | Main thing to learn | Events that must be working |
|---|---|---|---|
| beta | 0-10 | Does the signup→order path work? | `signup_completed`, `order_placed` |
| launch | 10-100 | Do strangers buy? | full buy funnel, `payment_*` |
| growth_to_500 | 100-500 | Do people come back and bring friends? | `invite_*`, repeat `order_placed`, `customer_milestone_reached` |
| Your plan | | | |

**Q2.10 What decision will each number change?**
- *Example:* "If activation is under 20% after 100 signups, we fix onboarding before spending on ads."
- Your answer: `YOUR ANSWER HERE`

---

# 3. Project Phases (Idea → First 500 Customers)

> **Why:** Not every event is built on day one. Tagging each event with a phase tells everyone *when* to build it.

| Phase code | Name | What happens | Events needed |
|---|---|---|---|
| `build` | Build | Team creates the product (humans + AI agents) | Basic: app opened, errors, core actions |
| `qa` | QA | Testers check everything works | Test-only checks, event validation |
| `beta` | Beta | 10-50 friendly users try it | Signup, activation, feedback |
| `launch` | Launch | Product opens to everyone | Full funnel + payments |
| `growth_to_500` | Growth to 500 | Push toward 500 customers | Referral, retention, milestone counters |

**Q3.1 What is the date range for each phase?**
| Phase | Start date | End date | Exit rule (how do we know it is done?) |
|---|---|---|---|
| build | TBD | TBD | *e.g. "All P0 events are `in_qa`"* |
| qa | TBD | TBD | *e.g. "100% of P0 events pass the QA checklist"* |
| beta | TBD | TBD | *e.g. "30 beta users, 0 critical tracking bugs"* |
| launch | TBD | TBD | *e.g. "Public sign-up is open"* |
| growth_to_500 | TBD | TBD | *e.g. "500th customer recorded"* |

**Q3.2 What is the current phase?** (also set `current_phase` at the top)
- Your answer: `YOUR ANSWER HERE`

---

# 4. Naming Rules (The Standard — Do Not Change Per Project)

> **Why:** If everyone names events differently, the data becomes a mess. These rules are fixed for every project.

## 4.1 Event names
- Format: **`object_action`**, all **lowercase**, words joined by **underscores** (`snake_case`).
- `object` = the thing (`order`, `project`, `invoice`). `action` = what happened, in **past tense** (`placed`, `created`, `paid`).
- Max 40 characters. Letters, numbers, underscores only. No spaces, dots, or dashes.
- Do not put values in the name. Wrong: `order_placed_5_dollars`. Right: `order_placed` with a property `amount`.
- Do not put the screen or tool name in the name. Wrong: `button_click_blue`. Right: `checkout_started`.

| ✅ Good | ❌ Bad | Why bad |
|---|---|---|
| `order_placed` | `PlaceOrder` | Not snake_case, not past tense |
| `signup_completed` | `user signed up!!` | Spaces and symbols |
| `invite_sent` | `click_invite_btn` | Describes the button, not the meaning |
| `payment_failed` | `payment_failed_visa` | Value in the name |

## 4.2 Property names
- Same style: lowercase `snake_case`. Example: `order_total`, `item_count`.
- Money: whole number in the **smallest unit** (cents) plus a `currency` property. Example: `amount_cents: 600`, `currency: "USD"`.
- Time: ISO 8601 in UTC. Example: `2026-10-18T14:30:00Z`.
- True/false: names start with `is_` or `has_`. Example: `is_first_order`.
- IDs end with `_id`. Example: `order_id`.
- Fixed lists (enums) use lowercase words. Example: `payment_method: "card" | "wallet" | "cash"`.

## 4.3 Allowed categories (pick one per event)
`acquisition` · `account` · `activation` · `engagement` · `commerce` · `retention` · `referral` · `support` · `system` · `ai_feature`

**Q4.1 Do you need any extra category? Why?**
- Your answer: `NO` or `YOUR ANSWER HERE`

---

# 5. Who Is Doing the Action? (Identity Rules)

> **Why:** We must connect what a person did before and after they sign up, without guessing.

**Q5.1 Fill in the identity table.**
| Item | Rule | Example |
|---|---|---|
| `anonymous_id` | Random ID created on first visit/app open, before login | `anon_7f3a...` |
| `user_id` | Our own internal ID, created at signup. Never an email or phone | `usr_10482` |
| When do we link them? | At `signup_completed` and `login_completed` | |
| What happens on logout? | Keep `anonymous_id`, clear `user_id` | |
| Same person, 2 devices? | Both share the same `user_id` after login | |

**Q5.2 Any other ID you need? (for a business account, a stand, a store, etc.)**
- *Example:* "`stand_id` = the lemonade stand being ordered from."
- Your answer: `YOUR ANSWER HERE`

---

# 6. Properties Sent With EVERY Event (Global Properties)

> **Why:** Add these once, so you never repeat them. AI agents must add them automatically.

| Property | Type | Required? | Example | Notes |
|---|---|---|---|---|
| `event_id` | string | Yes | `evt_9c1d...` | Unique per event; used to stop duplicates |
| `timestamp` | datetime | Yes | `2026-10-18T14:30:00Z` | UTC |
| `anonymous_id` | string | Yes | `anon_7f3a...` | |
| `user_id` | string | If logged in | `usr_10482` | |
| `session_id` | string | Yes | `ses_55a0...` | |
| `platform` | enum | Yes | `web` / `ios` / `android` / `server` | |
| `app_version` | string | Yes | `1.4.2` | |
| `environment` | enum | Yes | `dev` / `staging` / `production` | Only `production` counts in reports |
| `phase` | enum | Yes | `beta` | One of the phase codes in Section 3 |
| `source` | string | No | `google_ads` | From the link the person came from |
| `locale` | string | No | `en-US` | |

**Q6.1 Do you need any extra global property?**
- Your answer: `NO` or `YOUR ANSWER HERE`

---

# 7. The Event Catalog (The Main List)

> **Why:** This is the heart of the document. One row = one event.

## How to fill one row
1. Pick a **name** using Section 4.
2. Write **what happens** in one simple sentence (when exactly should it fire?).
3. Say **where** it fires: web, iOS, Android, or server.
4. Pick a **category** (Section 4.3), **phase** (Section 3), and **priority** (P0/P1/P2).
5. Say **which question** from Section 2.3 it answers. If none, do not add it.
6. Set **status** and **owner**.
7. Add properties for this event in Section 8.

> **Skip-if hint:** If you are not sure an event is needed, mark it `P2` and `planned`. Do NOT delete it. Decide later.

## 7.1 Catalog table

| Event name | Category | Fires when (one sentence) | Where | Who | Phase | Priority | Answers (Q#) | Status | Owner |
|---|---|---|---|---|---|---|---|---|---|
| `app_opened` | engagement | The app opens or the site loads for the first time in a session | web, ios, android | anyone | beta | P0 | 1 | planned | TBD |
| `signup_started` | account | The person taps "Create account" | web, ios, android | anonymous | beta | P0 | 2 | planned | TBD |
| `signup_completed` | account | The account is successfully created | server | new user | beta | P0 | 2 | planned | TBD |
| `login_completed` | account | A returning person logs in successfully | server | user | beta | P1 | 4 | planned | TBD |
| `stand_viewed` | engagement | A person opens a lemonade stand page | web, ios, android | anyone | beta | P1 | 3 | planned | TBD |
| `cart_item_added` | commerce | A drink is added to the cart | web, ios, android | user | launch | P0 | 3 | planned | TBD |
| `checkout_started` | commerce | The person opens the payment screen | web, ios, android | user | launch | P0 | 3 | planned | TBD |
| `order_placed` | commerce | An order is created and accepted by the system | server | user | launch | P0 | 3, 4 | planned | TBD |
| `payment_succeeded` | commerce | Money was taken successfully | server | user | launch | P0 | 5 | planned | TBD |
| `payment_failed` | commerce | Payment was tried and failed | server | user | launch | P0 | 5 | planned | TBD |
| `order_refunded` | commerce | An order is refunded | server | system/admin | launch | P1 | 5 | planned | TBD |
| `invite_sent` | referral | A person sends an invite to a friend | web, ios, android | user | growth_to_500 | P1 | 6 | planned | TBD |
| `invite_accepted` | referral | An invited friend creates an account | server | new user | growth_to_500 | P1 | 6 | planned | TBD |
| `customer_milestone_reached` | retention | A user becomes a counted "customer" (Q2.1) | server | system | growth_to_500 | P0 | 7 | planned | TBD |
| `feedback_submitted` | support | A person sends feedback or a rating | web, ios, android | user | beta | P2 | 7 | planned | TBD |
| `error_occurred` | system | A visible error stops the person's task | web, ios, android, server | anyone | build | P0 | — | planned | TBD |

**Your catalog (add all your own events here):**

| Event name | Category | Fires when | Where | Who | Phase | Priority | Answers (Q#) | Status | Owner |
|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | |

## 7.2 Starter ideas by product type (copy only what fits)

**Web app / SaaS:** `workspace_created`, `project_created`, `teammate_invited`, `feature_used`, `subscription_started`, `subscription_upgraded`, `subscription_cancelled`, `invoice_paid`, `trial_started`, `trial_ended`

**Mobile app:** `app_installed`, `app_opened`, `push_permission_responded`, `push_notification_opened`, `app_updated`, `deep_link_opened`, `app_crashed`, `offline_mode_entered`

**Marketplace / e-commerce:** `search_performed`, `listing_viewed`, `listing_created`, `wishlist_item_added`, `cart_item_added`, `checkout_started`, `order_placed`, `order_shipped`, `order_delivered`, `order_cancelled`, `order_refunded`, `review_submitted`, `seller_onboarded`, `payout_sent`

**AI features (if any):** see Section 7.3 below.

## 7.3 AI-feature events (only if your product has an AI/LLM feature; otherwise write `N/A - no AI feature`)

> **Why:** AI features cost money, can be slow, and can be wrong. We need to see all three, without storing what people typed.

| Event name | Category | Fires when | Where | Phase | Priority |
|---|---|---|---|---|---|
| `ai_request_sent` | ai_feature | A person asks the AI to do something | server | beta | P0 |
| `ai_response_received` | ai_feature | The AI answers successfully | server | beta | P0 |
| `ai_request_failed` | ai_feature | The AI call fails, times out, or is blocked | server | beta | P0 |
| `ai_response_rated` | ai_feature | The person gives thumbs up/down or a rating | web, ios, android | beta | P1 |
| `ai_response_edited` | ai_feature | The person changes the AI's answer before using it | web, ios, android | launch | P2 |
| `ai_response_accepted` | ai_feature | The person uses/keeps the AI's answer | web, ios, android | launch | P1 |
| `ai_limit_reached` | ai_feature | The person hits a usage or cost limit | server | launch | P1 |

**Properties to use (never the prompt text or answer text):**
| Property | Type | Example | Notes |
|---|---|---|---|
| `ai_feature_name` | string | `lemon_recipe_helper` | Which AI feature |
| `model_name` | string | `TBD` | Write what you actually use; do not guess |
| `prompt_length_chars` | number | `120` | Length only, not the text |
| `response_length_chars` | number | `800` | Length only |
| `latency_ms` | number | `1900` | Time to answer |
| `input_tokens` / `output_tokens` | number | `350` / `500` | For cost tracking |
| `cost_cents_estimate` | number | `2` | Estimated cost of the call |
| `error_type` | enum | `timeout`, `rate_limited`, `blocked`, `other` | Only on failure |
| `rating` | enum | `up`, `down` | Only on `ai_response_rated` |
| `request_id` | string | `req_77ab...` | Links sent, received, and rated together |

**Extra AI guardrails to add to Section 2.6:** AI failure rate, average latency, cost per customer, share of thumbs-down answers.

---

# 8. Event Property Details

> **Why:** Properties are the extra facts. Each important event gets a small table. Copy the block for each event.

## How to fill
- List **only** properties beyond the global ones in Section 6.
- **Type:** string, number, boolean, datetime, enum, or list.
- **Required?:** Yes / No / Sometimes (say when).
- **Contains PII?:** Yes or No. If Yes, stop and read Section 11.

### Example: `order_placed`
| Property | Type | Required? | Allowed values / format | Example | Contains PII? | Description |
|---|---|---|---|---|---|---|
| `order_id` | string | Yes | `ord_` + number | `ord_2041` | No | Unique order ID |
| `stand_id` | string | Yes | `stand_` + number | `stand_17` | No | Which stand sold it |
| `item_count` | number | Yes | integer ≥ 1 | `2` | No | Number of drinks |
| `amount_cents` | number | Yes | integer ≥ 0 | `600` | No | Total price in cents |
| `currency` | enum | Yes | ISO 4217 code | `USD` | No | |
| `payment_method` | enum | Yes | `card`, `wallet`, `cash` | `card` | No | |
| `is_first_order` | boolean | Yes | true/false | `true` | No | First order ever for this user |
| `coupon_code` | string | Sometimes | Only if a coupon is used | `SUMMER5` | No | |

### Example: `signup_completed`
| Property | Type | Required? | Allowed values / format | Example | Contains PII? | Description |
|---|---|---|---|---|---|---|
| `signup_method` | enum | Yes | `email`, `google`, `apple` | `email` | No | How they signed up |
| `referral_code` | string | Sometimes | Only if referred | `FRIEND42` | No | |
| `has_accepted_terms` | boolean | Yes | true | `true` | No | |

### Your event: `YOUR_EVENT_NAME`
| Property | Type | Required? | Allowed values / format | Example | Contains PII? | Description |
|---|---|---|---|---|---|---|
| | | | | | | |

*(Copy this block once for every event in your catalog.)*

---

# 9. Funnels and the 500-Customer Counter

> **Why:** Funnels show where people drop out. The counter tells us when we hit 500.

**Q9.1 Define your main funnel(s). List steps in order.**
| Funnel name | Step 1 | Step 2 | Step 3 | Step 4 | Step 5 | Time limit |
|---|---|---|---|---|---|---|
| Buy funnel | `app_opened` | `stand_viewed` | `cart_item_added` | `checkout_started` | `order_placed` | 7 days |
| Signup funnel | `app_opened` | `signup_started` | `signup_completed` | `order_placed` | | 7 days |
| Your funnel | | | | | | |

**Q9.2 How is the "customer" counter calculated?**
- *Example:* "Fire `customer_milestone_reached` once per user, the first time `payment_succeeded` happens AND no refund occurs within 7 days. Properties: `customer_number` (1 to N)."
- Your answer: `YOUR ANSWER HERE`

**Q9.3 What happens at customers 1, 100, 250 and 500?**
- *Example:* "At 500, the team gets a message and we start the 'First 500' review."
- Your answer: `YOUR ANSWER HERE`

---

# 10. Platform Notes (Web, Mobile, Server)

> **Why:** Each place behaves differently. Say who sends which events so numbers are not counted twice.

**Q10.1 Which events are sent from the server (safer) and which from the app/browser?**
| Rule | Your answer |
|---|---|
| Money events (`payment_*`, `order_*`) are sent from | *Example: server only* → `YOUR ANSWER HERE` |
| Account events (`signup_completed`) are sent from | *Example: server only* → `YOUR ANSWER HERE` |
| Screen/click events are sent from | *Example: app or browser* → `YOUR ANSWER HERE` |

**Q10.2 Mobile only: what happens with no internet?**
- *Example:* "Events are saved on the phone and sent when the internet returns, keeping the original `timestamp`. Keep up to 500 events, send oldest first."
- Your answer: `YOUR ANSWER HERE`

**Q10.3 Web only: what about ad blockers and cookies?**
- *Example:* "Money and signup events come from the server, so ad blockers cannot hide them."
- Your answer: `YOUR ANSWER HERE`

**Q10.4 How do we stop the same event being counted twice?**
- *Example:* "Every event has a unique `event_id`; the tool ignores repeats."
- Your answer: `YOUR ANSWER HERE`

---

# 11. Privacy, Consent, and Safety

> **Why:** Protecting people comes first. This section is a **hard rule**. AI agents must obey it.

## 11.1 Never track (fixed rule for all projects)
- Passwords, security answers, API keys, tokens
- Full card numbers, bank numbers, government IDs
- Health, religion, politics, or other sensitive details
- Free text a person typed (messages, search words, AI prompts), unless approved in 11.3
- Exact home address or precise location, unless approved in 11.3
- Anything about children under 13 unless legal has approved it in writing

## 11.2 Answer these questions
**Q11.1 Which laws or rules apply? (tick all that apply)**
- [ ] GDPR (Europe)  [ ] UK GDPR  [ ] CCPA/CPRA (California)  [ ] COPPA (children, USA)  [ ] Other: ____ [ ] TBD

**Q11.2 What does the person agree to, and when?**
- *Example:* "A cookie/consent banner appears on first visit. Until the person says yes, only `essential` events are sent."
- Your answer: `YOUR ANSWER HERE`

**Q11.2b Fill in what each consent choice allows.**
| Consent state | What may be sent | Example |
|---|---|---|
| `not_asked_yet` | Only `essential` events (errors, security, payments needed to run the service) | `error_occurred`, `payment_succeeded` |
| `accepted_all` | All events in the catalog | everything |
| `accepted_essential_only` | Only `essential` events | same as not asked |
| `declined` | Only `essential` events, no `user_id` in analytics | |
| `withdrawn` (changed their mind) | Stop sending immediately; delete past data if the law requires it | |

Mark each event `essential: yes/no` in your catalog notes. Your rule for "essential": `YOUR ANSWER HERE`

**Q11.2c Region checklist (tick what you must do).**
- [ ] Show a clear consent choice before non-essential tracking (Europe/UK)
- [ ] Offer "Do not sell or share my data" (California)
- [ ] Get a parent's permission for under-13 users (COPPA)
- [ ] Respect browser "Do Not Track" / global privacy signals where required
- [ ] Keep a record of when and what each person agreed to
- [ ] Not sure → write `TBD` and ask the privacy reviewer before launch

**Q11.2d How do we hide or shrink data that is close to personal?**
| Data | Safe way to track | Example |
|---|---|---|
| Email | Do not send. Send `user_id` only | `usr_10482` |
| Exact location | Send only country or region | `region: "TX"` |
| Birthday | Send age group | `age_band: "25-34"` |
| IP address | Do not store, or cut the last part | |
| What someone typed | Send the length or a category, not the text | `query_length: 12` |

**Q11.3 List any event or property that holds personal data and has been approved.**
| Event / property | What personal data | Why needed | Approved by | Date | Delete after |
|---|---|---|---|---|---|
| *(none)* | | | | | |

**Q11.4 How long do we keep event data?**
- *Example:* "26 months, then delete."
- Your answer: `YOUR ANSWER HERE`

**Q11.5 How does a person ask us to delete their data, and who does it?**
- Your answer: `YOUR ANSWER HERE`

**Q11.6 Who may see the raw event data?**
- Your answer: `YOUR ANSWER HERE`

---

# 12. Tool Mapping (Keep This Tiny)

> **Why:** The rest of the document does not depend on a tool. Only this section does. If you change tools, change only this section.

| Item | Your answer |
|---|---|
| Tool name | `TBD` |
| Where do the keys/secrets live? (never write the secret here) | `TBD` |
| Separate projects for dev / staging / production? | `TBD` |
| How are `user_id` and properties set in the tool? | `TBD` |
| Any tool limits (property count, name length)? | `TBD` |
| Dashboard link(s) | `TBD` |

---

# 13. QA and Validation Checklist

> **Why:** An event that is wrong is worse than no event. Test every P0 event before launch.

## 13.1 Test one event (copy this for each event)
**Event: `__________`**
- [ ] Fires **exactly once** when the action happens
- [ ] Does **not** fire when the action does not happen
- [ ] Name matches Section 4 and the catalog exactly
- [ ] All **required** properties are present
- [ ] Property types and formats are correct (cents, ISO time, enums)
- [ ] All global properties (Section 6) are present
- [ ] `environment` is correct (`dev`/`staging` data never mixes with `production`)
- [ ] No PII or forbidden data (Section 11)
- [ ] Works on every listed platform (web / iOS / Android / server)
- [ ] Fires correctly with no internet (mobile) and after refresh (web)
- [ ] No duplicate when the user taps twice
- [ ] Appears in the tool within ____ minutes
- [ ] Tested by: ______ Date: ______ Result: pass / fail

## 13.2 Test the whole product
- [ ] Every funnel in Section 9 can be completed with test accounts and each step appears in order
- [ ] The customer counter increases by 1 (and only 1) per new customer
- [ ] Consent "no" really stops non-essential events
- [ ] Logging in links `anonymous_id` to `user_id` correctly
- [ ] Refund test lowers the right numbers
- [ ] A dashboard number matches a manual count for 10 test orders

## 13.3 Bug log
| # | Event | What went wrong | Severity (blocker/major/minor) | Owner | Status |
|---|---|---|---|---|---|
| | | | | | |

---

# 14. AI-Agent Instructions (Read by AI Coding/QA Agents)

> **Humans:** Do not edit the rules below unless the template owner approves. Fill only the blanks marked `TBD`.

## 14.1 Rules the AI agent MUST follow
1. **This document is the single source of truth.** Never create, rename, or remove an event or property that is not in Section 7 and Section 8.
2. **Never guess.** If a value is `TBD`, a section is empty, or something conflicts, stop, list it in Section 16, and ask the owner.
3. Follow Section 4 naming exactly. Reject any name that breaks the rules.
4. Always attach every global property from Section 6 automatically.
5. Obey Section 11. Never send forbidden data. If unsure whether a field is personal data, treat it as personal data and ask.
6. Only implement events whose `phase` is the current phase or earlier, and whose `status` is `planned` or `in_build`.
7. Send money, account, and counter events from the **server** (Section 10).
8. For every event you implement, also write an automated test that checks name, required properties, and "fires once".
9. After finishing, update the event's `status` in Section 7 and add a line to the Change Log (Section 17).
10. Never put secrets, keys, or real customer data in code, tests, examples, or this document.
11. Do not change `status` to `live` yourself. Only a human QA reviewer may do that.

## 14.1b More rules for the AI agent
12. **Read in this order before any work:** top box → Section 3 (phase) → Section 4 (names) → Section 6 (global properties) → Section 7 and 8 (events) → Section 11 (privacy) → Section 16 (open questions).
13. **One event, one place in code.** Create a single helper function that sends events; never call the analytics tool directly from many places.
14. **Validate before sending.** The helper must check name and required properties against Section 7-8, and refuse (in dev/staging) or drop and log (in production) anything invalid. A bad event must never crash the product.
15. **Do not block the user.** Sending an event must not slow or break the screen. Send it in the background.
16. **No hidden events.** Do not add "just in case" events. If you think one is needed, add it to Section 16 as a proposal.
17. **Use only test data** in dev and staging. Mark all test traffic with `environment`.
18. **Respect consent.** Check the consent state (Section 11) before sending any non-essential event.
19. **If two sections disagree, stop.** Priority order when in conflict: Section 11 (privacy) > Section 4 (names) > Section 8 (properties) > Section 7 (catalog) > everything else. Report the conflict.
20. **Keep changes small.** One pull request = one group of related events.

## 14.1c What the agent may decide alone vs must ask
| Situation | Agent may decide alone? | What to do |
|---|---|---|
| Fix a typo in code comments | Yes | Just do it |
| Choose a variable name in code | Yes | Follow code style |
| An event is in the catalog but a property detail is `TBD` | **No** | Ask; add to Section 16 |
| A needed event is missing from the catalog | **No** | Propose it in Section 16 |
| A property might be personal data | **No** | Treat as personal; ask privacy reviewer |
| Change an existing event's meaning or type | **No** | Needs major-version change (Section 17) |
| Mark an event `live` | **No** | Human QA only |

## 14.1d Definition of done (for each event the agent builds)
- [ ] Event is sent from the right place (Section 10)
- [ ] Name, properties, and types match Sections 7-8
- [ ] Global properties are attached
- [ ] Consent is checked
- [ ] Automated test passes
- [ ] Section 7 `status` updated to `in_qa`
- [ ] Change log line added (Section 17)

## 14.1e Copy-paste handoff format (agent to human)
```
EVENT WORK REPORT
Phase: <phase>            Document version: <x.y.z>
Events done:   <names>
Events blocked: <names> because <reason> -> added to Section 16 as #<n>
Files changed: <paths>
Tests:         <added> / <passing>
Privacy check: <pass | needs review: why>
Questions for owner: <list or "none">
```

## 14.2 What the agent must report after each task
- Events added/changed (names only)
- Files changed
- Tests added and whether they pass
- Anything it could not do and why (reference Section 16)

## 14.3 Where to find things (fill in once per project)
| Item | Location |
|---|---|
| Tracking code folder | `TBD` |
| Tracking helper / wrapper file | `TBD` |
| Tests folder | `TBD` |
| Event schema file (if any) | `TBD` |
| How to run the tests | `TBD` |

---

# 15. Reports and Dashboards

> **Why:** Events are only useful if someone looks at them.

**Q15.1 What dashboards do you need?**
| Dashboard | Who looks | How often | Events used | Link |
|---|---|---|---|---|
| Daily health (events arriving? errors?) | Engineering | Daily | all, `error_occurred` | TBD |
| Funnel (Section 9) | Product | Weekly | funnel events | TBD |
| Road to 500 | Everyone | Daily | `customer_milestone_reached` | TBD |
| Revenue | Founder/Finance | Weekly | `payment_succeeded`, `order_refunded` | TBD |

**Q15.2 What alerts do you need?**
- *Example:* "Alert the owner if `order_placed` drops to 0 for 2 hours, or `error_occurred` doubles in a day."
- Your answer: `YOUR ANSWER HERE`

---

# 16. Open Questions and Risks (The "TBD" List)

> **Why:** Every unknown goes here so nothing is forgotten or guessed.

| # | Question or risk | Where it came from (section) | Owner | Due date | Status (open/answered) | Answer |
|---|---|---|---|---|---|---|
| 1 | | | | | open | |

---

# 17. Change Log and Versioning

> **Why:** Data must stay trustworthy over time. Changes are recorded, never silent.

## 17.1 Rules
- **Never reuse an old event name for a new meaning.**
- **Adding** an event or optional property → raise the **minor** version (0.1.0 → 0.2.0).
- **Renaming, removing, or changing the meaning/type** of an event or property → raise the **major** version (1.x → 2.0) and mark the old one `deprecated`.
- **Typos and wording fixes** → raise the **patch** version (0.1.0 → 0.1.1).
- A deprecated event keeps being listed for at least **90 days** with a replacement named.
- Every change needs a reviewer other than the person who made it.

## 17.2 Deprecated events
| Old event | Replaced by | Deprecated on | Remove on | Reason |
|---|---|---|---|---|
| | | | | |

## 17.3 Log
| Version | Date | Changed by | What changed | Why | Approved by |
|---|---|---|---|---|---|
| 0.1.0 | YYYY-MM-DD | TBD | First draft created from template | Start | TBD |

---

# 18. Ready Checklist and Sign-Off

Tick each box. When all are ticked, set `status: approved` at the top.

**Content**
- [ ] Sections 1-3 are fully answered
- [ ] Every event has a name, trigger, category, phase, priority, status, owner
- [ ] Every P0 event has a property table in Section 8
- [ ] Every event answers at least one question from Section 2.3
- [ ] Funnels and the 500 counter are defined (Section 9)
- [ ] There are no empty cells; unknowns are `TBD` and listed in Section 16

**Quality**
- [ ] All names follow Section 4
- [ ] Privacy section reviewed by the privacy/legal reviewer
- [ ] QA checklist completed for every P0 event
- [ ] Dashboards and alerts exist for the "Road to 500"

**Launch readiness**
- [ ] No open blocker bugs in Section 13.3
- [ ] Section 16 has no open item that affects a P0 event
- [ ] Change log is up to date

**Sign-off**
| Role | Name | Date | Approved? |
|---|---|---|---|
| Owner | | | |
| Product | | | |
| Engineering | | | |
| QA | | | |
| Privacy / legal | | | |

---

# 19. Quick Glossary and Fast Fixes

| Problem | Fix |
|---|---|
| "I don't know the answer" | Write `TBD \| owner: name \| due: date` and add to Section 16 |
| "My event name is long" | Split it into object + action; move extra words into a property |
| "I need to change an old event" | Do not edit. Add a new one and deprecate the old (Section 17) |
| "Is this personal data?" | If it could point to one real person, say yes and ask the privacy reviewer |
| "Two people count the same thing differently" | Write one exact definition in Section 2 and use it everywhere |
| "The number looks wrong" | Run Section 13.2 checks first, then check `environment` and duplicates |

---
# Appendix A. Finished Mini Example: "Lemonade Stand"

> A tiny, completely filled version so you can see the finish line. Delete this appendix in your own copy if you like.

**Basics:** Lemonade Stand is a mobile app where neighbors order fresh lemonade from kids nearby. Owner: Sam. Phase: `beta`. Tool: any analytics tool. Goal: 500 customers by 2027-03-31.

**Customer means:** a person who completed one paid order that was not refunded within 7 days.

**North Star:** orders delivered per week.

**Events (short version):**
| Event | Fires when | Where | Phase | Priority |
|---|---|---|---|---|
| `app_opened` | App opens | ios, android | beta | P0 |
| `signup_completed` | Account created | server | beta | P0 |
| `stand_viewed` | A stand page is opened | ios, android | beta | P1 |
| `cart_item_added` | Drink added to cart | ios, android | launch | P0 |
| `order_placed` | Order accepted | server | launch | P0 |
| `payment_succeeded` | Money taken | server | launch | P0 |
| `invite_sent` | Invite sent | ios, android | growth_to_500 | P1 |
| `customer_milestone_reached` | First paid, non-refunded order (after 7 days) | server | growth_to_500 | P0 |

**`order_placed` properties:** `order_id`, `stand_id`, `item_count`, `amount_cents`, `currency`, `payment_method`, `is_first_order`, `coupon_code` (sometimes).

**Privacy:** no emails or phone numbers in events; `user_id` only; consent banner for web; data kept 26 months.

**Open question #1:** "Is a tip part of `amount_cents`?" | owner: Sam | due: 2026-11-05 | status: open.

---

# Appendix B. Copy-Paste AI Prompts

## B.1 Prompt to FILL this document (give to an AI helper along with your project notes)
```
You are a careful product analytics specialist. Fill in Event_Taxonomy.md for my project.
Rules:
- Follow the template's questions in order. Do not remove sections.
- Use only facts I provided. For anything missing, write "TBD | owner: <name> | due: <date>" and add it to Section 16. Do not invent numbers, tools, or laws.
- Event names must follow Section 4 (object_action, snake_case, past tense).
- Every event must answer a question from Section 2.3, or be marked P2 with a reason.
- Never include personal data in events. Apply Section 11.
- Keep wording simple enough for a 10-year-old to understand.
- At the end, list the 10 questions you most need me to answer.
My project notes: <paste here>
```

## B.2 Prompt to IMPLEMENT events from this document
```
You are a senior software engineer. Implement the events in Event_Taxonomy.md.
Follow Section 14 exactly. Only build events whose status is "planned" or "in_build" and whose phase is the current phase or earlier.
Use one central helper to send events; validate every event against Sections 4, 6, 7, 8; check consent (Section 11) first; never block the user interface.
Write automated tests for each event. If anything is TBD or conflicting, stop and report it instead of guessing.
When done, reply using the handoff format in Section 14.1e and update Sections 7 and 17.
```

## B.3 Prompt to REVIEW/QA this document
```
You are a QA specialist. Review Event_Taxonomy.md against Section 18.
List: (1) naming errors, (2) events with no question they answer, (3) missing or TBD required properties, (4) possible personal data, (5) funnel steps that do not exist in the catalog, (6) conflicts between sections.
Do not fix anything. Give a numbered list with section references and severity (blocker / major / minor).
```

---

# Appendix C. Machine-Readable Event Definition (JSON Schema Snippet)

> AI agents and test tools can use this to check events automatically. Keep one definition per event in your code repo and keep it identical to Sections 7-8.

**C.1 Shape of one event definition**
```json
{
  "name": "order_placed",
  "category": "commerce",
  "description": "An order is created and accepted by the system.",
  "phase": "launch",
  "priority": "P0",
  "status": "planned",
  "essential": false,
  "platforms": ["server"],
  "owner": "TBD",
  "answers_questions": [3, 4],
  "properties": {
    "order_id":       { "type": "string",  "required": true,  "pii": false },
    "stand_id":       { "type": "string",  "required": true,  "pii": false },
    "item_count":     { "type": "integer", "required": true,  "pii": false, "min": 1 },
    "amount_cents":   { "type": "integer", "required": true,  "pii": false, "min": 0 },
    "currency":       { "type": "string",  "required": true,  "pii": false, "pattern": "^[A-Z]{3}$" },
    "payment_method": { "type": "string",  "required": true,  "pii": false, "enum": ["card", "wallet", "cash"] },
    "is_first_order": { "type": "boolean", "required": true,  "pii": false },
    "coupon_code":    { "type": "string",  "required": false, "pii": false }
  }
}
```

**C.2 JSON Schema that checks the shape above**
```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "title": "EventDefinition",
  "type": "object",
  "required": ["name", "category", "description", "phase", "priority", "status", "platforms", "owner", "properties"],
  "additionalProperties": false,
  "properties": {
    "name":        { "type": "string", "pattern": "^[a-z][a-z0-9]*(_[a-z0-9]+)+$", "maxLength": 40 },
    "category":    { "enum": ["acquisition","account","activation","engagement","commerce","retention","referral","support","system","ai_feature"] },
    "description": { "type": "string", "minLength": 10 },
    "phase":       { "enum": ["build","qa","beta","launch","growth_to_500"] },
    "priority":    { "enum": ["P0","P1","P2"] },
    "status":      { "enum": ["planned","in_build","in_qa","live","deprecated"] },
    "essential":   { "type": "boolean" },
    "platforms":   { "type": "array", "items": { "enum": ["web","ios","android","server"] }, "minItems": 1 },
    "owner":       { "type": "string" },
    "answers_questions": { "type": "array", "items": { "type": "integer" } },
    "replaced_by": { "type": "string" },
    "properties": {
      "type": "object",
      "propertyNames": { "pattern": "^[a-z][a-z0-9_]*$" },
      "additionalProperties": {
        "type": "object",
        "required": ["type", "required", "pii"],
        "properties": {
          "type": { "enum": ["string","integer","number","boolean","datetime","list"] },
          "required": { "type": "boolean" },
          "pii": { "type": "boolean" },
          "enum": { "type": "array" },
          "pattern": { "type": "string" },
          "min": { "type": "number" },
          "max": { "type": "number" }
        }
      }
    }
  }
}
```

---
*Template: Event_Taxonomy v1.2.0. Reuse this file for every project. Copy it, fill in the top block, and work through Sections 1-18 in order.*
