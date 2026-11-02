# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

**Template name:** Refund and Dispute Handling
**Template version:** 1.2 (ready to reuse)
**Where this file lives:** `Billing, Finance and Business Operations / Refund_and_Dispute_Handling.md`
**Covers:** AI-Driven Development Life Cycle, from the first line of code to your first 500 paying customers
**Product types covered:** SaaS / subscriptions, one-time digital products, marketplace / services
**Payment providers covered:** Stripe, PayPal, Apple App Store, Google Play
**Regions covered:** United States, EU / UK, India & APAC, plus a "Global / other" fallback
**Team assumption:** a solo founder or tiny team (one person may fill several roles)

---

## What is this document?

When a customer asks for their money back, or tells their bank "I did not make this purchase," your business needs a **clear plan**. This document **is** that plan. You fill it in once per project. After that, you (and any AI helper) follow it every time money goes back to a customer.

Think of it like a recipe card. If the card is complete, anyone can cook the meal without guessing.

## QUICK START: THE SHORT PATH (about 60 to 90 minutes)

In a hurry? Fill in **only these** first. They protect you on day one. Finish the rest before you take real money.

| Order | What to fill in | Why it matters |
|---|---|---|
| 1 | Part 0 to Part 2 | Who owns what |
| 2 | Part 3 (Q3.1 to Q3.8) | Your refund promise to customers |
| 3 | Part 4 (Q4.1 to Q4.3) | Yes or no rules, and money limits |
| 4 | Part 7 (Q7.1 to Q7.3) | Do not miss a dispute deadline |
| 5 | Part 14 (Q14.1, Q14.2, Q14.5) | Keep the AI safe |
| 6 | Part 21 | Check you are ready |

Then, before launch: Parts 5, 6, 9, 11, 13, 18. During the first 500 customers: Parts 12, 16, 17, 19, 20.

## Reading help

- Every hard word is explained in **Appendix A**. If a word is new to you, look it up there first.
- Lines that start with **In plain words** say the same thing in simpler words.
- Extras at the back: **Appendix C** (marketplace), **D** (dispute reasons), **E** (AI prompt), **F** (log tables), **G** (a finished sample).

## The 7 simple rules for filling it in

1. **Answer every question.** Each question has a box that looks like `Your answer: ________`. Replace the blanks with your answer.
2. **Read the example, then write your own.** Every question has an *Example*. Do not copy it unless it is true for your project.
3. **Do not leave a question empty.** If you do not know yet, write `TBD (to be decided) by [date] by [name]`. If it truly does not apply, write `N/A because [reason]`.
4. **Use numbers, not feelings.** Write "14 days" instead of "a reasonable time." Write "$50" instead of "small amount."
5. **Pick from the lists when you see `[ ]` boxes.** Change `[ ]` to `[x]` for what applies.
6. **One answer, one place.** If an answer is already written somewhere else in this file, point to it (example: "see Q3.2"). Do not write it twice.
7. **Look at the tags.** Each part shows **when** you must finish it:

| Tag | Meaning | When to finish it |
|---|---|---|
| `[BUILD]` | Build and test phase | Before you write payment code |
| `[PRE-LAUNCH]` | Beta and getting ready | Before the first real customer pays |
| `[LAUNCH 1-100]` | Customers 1 to 100 | Review weekly |
| `[SCALE 101-500]` | Customers 101 to 500 | Review monthly |
| `[ALL]` | Always | Fill in at the start |

## How to fill it in, step by step (about 2 to 4 hours the first time)

1. Fill in **Part 0 to Part 2** first. They are quick facts about your project.
2. Fill in **Part 3 to Part 5** next. These are your refund rules.
3. Fill in the parts for your payment providers (**Part 6**) and disputes (**Part 7**).
4. Fill in the parts that apply to your product type (**Part 9**, and **Part 10 with Appendix C** only if you run a marketplace). Mark the others `N/A`.
5. Do **Part 11** (laws). Search for your country's rules, or ask a lawyer. This template cannot replace a lawyer.
6. Finish with **Parts 12 to 21**.
7. Complete the **Readiness Check in Part 21**. If every box is ticked, you are good to go.

## Status labels (put one next to each Part heading)

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

## Notes for AI agents reading this file

- Treat the answers in this document as the **only source of truth** for refund and dispute decisions.
- If an answer is `TBD`, blank, or missing, **do not guess**. Stop and ask the human owner (Part 2).
- Never move money, send a refund, or submit dispute evidence unless Part 14 says you are allowed to.
- Quote the question number (example: "per Q4.3") when explaining a decision.

## Important notes

- **This is a planning template, not legal or tax advice.** Laws and provider rules change. Fees, deadlines and rules written in the examples were checked in October 2026 and **must be re-checked** before you rely on them (see Part 20).
- Never paste secrets into this file: no passwords, API keys, full card numbers, or customers' private details.

---

# PART 0. DOCUMENT CONTROL `[ALL]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q0.1 What is the name of this project or product?**
- **Your answer:** `________`
- *Example:* "PixelPlan, a budgeting app"

**Q0.2 Who owns this document (the person responsible for keeping it correct)?**
- **Your answer:** `________`
- *Example:* "Maya Rossi (founder), maya@example.com"

**Q0.3 Date this document was first completed, and date of the next review?**
- **Your answer:** First completed: `____-__-__`  Next review: `____-__-__`

**Q0.4 Where do you keep this document so the team and AI agents can find it?**
- **Your answer:** `________`
- *Example:* "In the project repo under /docs/billing/"

**Q0.5 What is the first thing someone should do if they only have 5 minutes in an emergency (a surprise dispute, a refund wave)?**
- **Your answer:** `________`
- *Example:* "Go to Part 7, find the provider, check the deadline, and reply before it."

---

# PART 1. PROJECT SNAPSHOT `[ALL]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q1.1 In one sentence, what does your product do and who pays for it?**
- **Your answer:** `________`
- *Example:* "A mobile app that helps students plan budgets; students pay $6 a month."

**Q1.2 What do customers buy? Tick all that apply.**
- [ ] Monthly or yearly subscription
- [ ] One-time digital product (download, license, course, app unlock)
- [ ] Marketplace or service (we connect buyers and sellers, or sell human services)
- [ ] Free trial that turns into paid
- [ ] Usage-based billing (pay for what you use)
- [ ] Other: `________`

**Q1.3 List every price point. (Name, price, currency, billing period.)**

| Plan or item | Price | Currency | Billing period |
|---|---|---|---|
| `____` | `____` | `____` | `____` |
| `____` | `____` | `____` | `____` |

- *Example:* "Pro | 6.00 | USD | monthly"

**Q1.4 Where are your customers? Tick all that apply.**
- [ ] United States  [ ] EU  [ ] UK  [ ] India  [ ] Other APAC  [ ] Rest of world
- **Main country:** `________`

**Q1.5 Which payment providers do you use? Tick all that apply.**
- [ ] Stripe  [ ] PayPal  [ ] Apple App Store  [ ] Google Play  [ ] Other: `________`

**Q1.6 What is your business or legal name and country of registration? (This is the name on customers' bank statements, so match it.)**
- **Your answer:** `________`
- **Name shown on card statements (statement descriptor):** `________`
- *Tip:* A clear descriptor prevents "I don't recognize this charge" disputes.

**Q1.7 What stage is the project in right now?**
- [ ] `[BUILD]` Still building  [ ] `[PRE-LAUNCH]` Beta / getting ready  [ ] `[LAUNCH 1-100]` Live, under 100 customers  [ ] `[SCALE 101-500]` 100 to 500 customers

**Q1.8 What is your target launch date and your goal of 500 paying customers by when?**
- **Your answer:** Launch: `____-__-__`  500 customers by: `____-__-__`

---

# PART 2. WHO DOES WHAT (ROLES AND OWNERS) `[ALL]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> Solo founder? It is fine for **one person** to fill every role. Write the same name each time. The point is that every job has an owner, even if it is you.

| Role | What this person does | Name | Contact | Backup person |
|---|---|---|---|---|
| **Policy Owner** | Writes and updates refund rules | `____` | `____` | `____` |
| **Refund Approver** | Says yes or no to refunds | `____` | `____` | `____` |
| **Dispute Handler** | Answers chargebacks before deadlines | `____` | `____` | `____` |
| **Support Agent** | Talks to customers | `____` | `____` | `____` |
| **Finance / Bookkeeper** | Records refunds and fees | `____` | `____` | `____` |
| **Legal Contact** | Answers law questions | `____` | `____` | `____` |
| **AI Agent Supervisor** | Watches the AI and fixes its mistakes | `____` | `____` | `____` |

**Q2.1 If the Dispute Handler is on vacation or sick, who covers? How will they get access?**
- **Your answer:** `________`
- *Example:* "My co-founder Sam. He has Stripe dashboard access via a shared password manager."

**Q2.2 Which hours are you available to respond to customers, and in which time zone?**
- **Your answer:** `________`
- *Example:* "Mon to Fri, 9:00-17:00 UTC+1"

**Q2.3 How do you stop one person from approving and paying out large refunds with no second pair of eyes?** (This is called "separation of duties.")
- **Your answer:** `________`
- *Example:* "Over $200, the founder asks the bookkeeper to confirm by message before refunding."
- *Tip:* A solo founder can write "I will wait 24 hours and re-read the case before refunding over $X."

---

# PART 3. YOUR CUSTOMER-FACING REFUND POLICY `[BUILD]` `[PRE-LAUNCH]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> This is the policy **customers will read**. Keep it short, plain, and fair. Laws in your customers' countries may give them rights you cannot remove (see Part 11).

**Q3.1 Which refund approach do you offer? Pick one per product type.**

| Product type | Approach (tick one) |
|---|---|
| Subscription | [ ] Money-back guarantee ____ days  [ ] Refund unused time  [ ] No refunds after renewal (only where the law allows)  [ ] Case by case |
| One-time digital | [ ] ____ days if not downloaded or used  [ ] Only if broken or not as described  [ ] Case by case |
| Marketplace / service | [ ] Refund if service not delivered  [ ] Hold payment until delivered (escrow)  [ ] Case by case |

- *Example:* "Subscription: 14-day money-back guarantee, then refunds only for billing errors."

**Q3.2 How many days after purchase can a customer ask for a refund?**
- **Your answer:** `____ days`
- *Tip:* Fewer than 14 days can break EU/UK rules for online sales unless special conditions are met (see Part 11). Longer windows reduce chargebacks.

**Q3.3 Write your "Reasons we refund" list. Tick all that apply.**
- [ ] Charged twice by mistake (duplicate charge)
- [ ] Charged after the customer cancelled
- [ ] Product did not work and we could not fix it
- [ ] Product was not as described
- [ ] Customer forgot to cancel a trial or renewal (first time only)
- [ ] Accidental purchase (kid, wrong tap)
- [ ] Service not delivered (marketplace)
- [ ] Legal right (cooling-off period, consumer law)
- [ ] Other: `________`

**Q3.4 Write your "Reasons we do not refund" list.**
- **Your answer:** `________`
- *Example:* "Change of mind after 14 days; abuse of the product; refunds already given twice in 12 months."

**Q3.5 What does the customer get? Tick all that apply.**
- [ ] Full refund  [ ] Partial refund (pro-rated)  [ ] Credit / account balance  [ ] Replacement or fix  [ ] Free extension
- **Which do you offer first?** `________`

**Q3.6 What happens to the customer's access after a refund?**
- **Your answer:** `________`
- *Example:* "Subscription access ends immediately; download license is revoked within 24 hours."

**Q3.7 How long does a refund take to reach the customer?**
- **Your answer:** We send it within `____` business days; the bank may take `____` more.
- *Tip:* Card refunds often take about 5 to 10 business days to show on the customer's statement. Check your provider's current guidance.

**Q3.8 Write your policy in plain words (80 words or fewer) as the customer will see it.**
- **Your answer:**
  `________________________________________________________________`
- **Where will the policy be shown? Tick all that apply:** [ ] Pricing page  [ ] Checkout  [ ] Terms of Service  [ ] Receipt email  [ ] App store listing  [ ] Help center

**Q3.9 Can the customer find "how to cancel" and "how to ask for a refund" in 2 clicks or fewer?**
- **Your answer:** [ ] Yes  [ ] No, fix by: `____-__-__`
- *Tip:* Hard-to-find cancel buttons cause chargebacks and legal trouble.

---

# PART 4. REFUND DECISION RULES (THE "IF THIS, THEN THAT" TABLE) `[BUILD]` `[PRE-LAUNCH]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> This table lets you (or an AI) decide **without guessing**. Fill in one row for each situation. Add rows as you learn.

**Q4.1 Fill in the decision table.**

| # | Situation | Days since purchase | Refund? (Yes/No/Ask) | How much | Who approves | Notes |
|---|---|---|---|---|---|---|
| 1 | Duplicate charge | any | `____` | `____` | `____` | `____` |
| 2 | Charged after cancelling | any | `____` | `____` | `____` | `____` |
| 3 | Product is broken, we cannot fix it | `____` | `____` | `____` | `____` | `____` |
| 4 | Customer says "not what I expected" | `____` | `____` | `____` | `____` | `____` |
| 5 | Forgot to cancel the trial | `____` | `____` | `____` | `____` | `____` |
| 6 | Accidental purchase | `____` | `____` | `____` | `____` | `____` |
| 7 | Annual plan, asked after 3 months | `____` | `____` | `____` | `____` | `____` |
| 8 | Service never delivered (marketplace) | `____` | `____` | `____` | `____` | `____` |
| 9 | Customer threatens a chargeback | any | `____` | `____` | `____` | `____` |
| 10 | Customer is abusing refunds | any | `____` | `____` | `____` | `____` |

- *Example row 1:* "Duplicate charge | any | Yes | Full duplicate amount | Support Agent (no approval needed) | Refund immediately, tell customer."

**Q4.2 What is the largest refund anyone can give without asking a second person?**
- **Your answer:** `$____`

**Q4.3 What is the largest refund anyone is ever allowed to give?**
- **Your answer:** `$____`
- *Tip:* Anything above this must be handled by the Legal Contact.

**Q4.4 When two rules seem to clash, which wins? Number these 1 to 4.**
- `__` The law of the customer's country
- `__` The payment provider's rules
- `__` Our written policy (Part 3)
- `__` Our judgment in a special case
- *Suggested order:* law, then provider rules, then policy, then judgment.

**Q4.5 How do you handle a customer who has already been refunded and comes back?**
- **Your answer:** `________`
- *Example:* "Allow one repeat refund in 12 months. After that, ask the founder."

**Q4.6 What do you do when you cannot decide?**
- **Your answer:** `________`
- *Example:* "Say 'I need 1 business day to look into this,' then ask the Refund Approver."

---

# PART 5. THE REFUND PROCESS, STEP BY STEP `[PRE-LAUNCH]` `[LAUNCH 1-100]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q5.1 How can customers ask for a refund? Tick all that apply.**
- [ ] Email: `________`  [ ] In-app form  [ ] Help center form  [ ] Chat  [ ] Social media  [ ] Provider's own page (Apple / Google)

**Q5.2 How fast do you reply to the first message?**
- **Your answer:** `____ hours`  (Target for first 100 customers: `____`; for customers 101-500: `____`)

**Q5.3 Write the refund steps in order. Keep each step to one action.**

| Step | What happens | Who | Tool | Time limit |
|---|---|---|---|---|
| 1 | Customer asks | Customer | `____` | n/a |
| 2 | We find the customer and the payment | `____` | `____` | `____` |
| 3 | We check the rules (Part 4) | `____` | `____` | `____` |
| 4 | We decide: yes, no, or ask a person | `____` | `____` | `____` |
| 5 | We send the refund | `____` | `____` | `____` |
| 6 | We turn off or adjust access | `____` | `____` | `____` |
| 7 | We tell the customer | `____` | `____` | `____` |
| 8 | We write it in the refund log (Q12.2) | `____` | `____` | `____` |

**Q5.4 How do you check that the person asking really owns the account or purchase?**
- **Your answer:** `________`
- *Example:* "Reply must come from the email on the account, plus the last 4 digits of the card or order ID."
- *Tip:* Never refund to a different card, bank or PayPal account than the original payment unless Legal approves.

**Q5.5 Where do refunds go?**
- **Your answer:** Back to the original payment method [ ] always  [ ] except when: `________`

**Q5.6 What if the original card is closed or expired?**
- **Your answer:** `________`
- *Example:* "Stripe returns the money to the customer's bank. If it fails, we ask for a bank transfer after Legal approves."

**Q5.7 Partial refunds. How do you calculate them?**
- **Your answer:** `________`
- *Example:* "Annual plan, cancelled in month 4 = refund (8 / 12) x price, minus any payment processor fees we cannot get back, but only if our policy says so."

**Q5.8 Cancel versus refund. Is cancelling always separate from refunding?**
- **Your answer:** `________`
- *Example:* "Cancelling stops future charges. A refund returns money already paid. We always ask which the customer wants."

**Q5.9 What do you do if a refund fails (error, insufficient balance)?**
- **Your answer:** `________`
- *Example:* "Retry once, check the provider's status, tell the customer in 24 hours, escalate to the founder."

---

# PART 6. PAYMENT PROVIDER SETUP AND RULES `[BUILD]` `[PRE-LAUNCH]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> Fill in only the sections for providers you ticked in Q1.5. Write `N/A` in the others.

## 6A. Stripe

**Q6A.1 Who has access to the Stripe account and with what permission level?**
- **Your answer:** `________`

**Q6A.2 Are Stripe email alerts for disputes turned on and sent to a monitored inbox?**
- **Your answer:** [ ] Yes, inbox: `________`  [ ] No, fix by: `____-__-__`

**Q6A.3 Facts to remember (re-check each review, see Part 20):**
- You normally get about **7 to 21 days** to answer a card dispute. The exact date shows on the dispute itself and is the only one that counts.
- Missing the deadline means the dispute is lost automatically.
- In the US, a dispute usually costs a **$15 dispute fee**, plus a **$15 counter fee** if you submit evidence and lose (up to $30 in total). Fees differ by country.
- You can usually send evidence **only once**. Get everything ready before you press submit.
- Refunding an inquiry or early warning may stop it turning into a full chargeback.
- Disputes on some cases cannot be contested at all.

**Q6A.4 Do you use Stripe Radar (fraud checks), Smart Disputes (automatic evidence), 3D Secure (an extra card check by the bank), or similar tools?**
- **Your answer:** `________`

**Q6A.5 Does your Stripe statement descriptor match Q1.6?**
- **Your answer:** [ ] Yes  [ ] No, fix by: `____-__-__`

## 6B. PayPal

**Q6B.1 Who has access and where do alerts go?**
- **Your answer:** `________`

**Q6B.2 Facts to remember (re-check each review):**
- Buyers can open a PayPal dispute up to about **180 days** after paying.
- Buyer and seller get about **20 days** to settle a dispute before it can be escalated to a claim.
- When a claim is opened, the seller usually has about **10 days** to respond. No response usually means the buyer wins.
- PayPal Seller Protection has strict conditions and mainly helps with physical goods. Do **not** assume digital goods or services are covered.

**Q6B.3 What is your plan if PayPal puts a hold on your money?**
- **Your answer:** `________`

## 6C. Apple App Store and Google Play (expanded)

> **In plain words:** When someone buys inside an app through Apple or Google, **the store, not you, usually decides about refunds.** Your job is to (1) tell customers where to ask, (2) hear about the refund, and (3) turn off access.

**Q6C.1 Which store sells your product?**
- [ ] Apple  [ ] Google Play  [ ] Both  [ ] Neither (write `N/A` for all of 6C)

**Q6C.2 Who decides refunds for store purchases?**
- **Your answer:** `________`
- *Example:* "Apple and Google decide. We never refund store purchases ourselves."

**Fill in this table for each store you use.**

| Question | Apple App Store | Google Play |
|---|---|---|
| Where does the customer ask for a refund? | `____` (example: Apple's "Report a Problem" page) | `____` (example: Play Store order history, or Google Play help) |
| Can **we** refund from our side? | `____` | `____` (example: yes, in Play Console, check current rules) |
| How do we hear about a refund or cancel? | `____` (example: App Store server notifications) | `____` (example: real-time developer notifications, "voided purchase" messages) |
| What do we do when we hear? | `____` (example: remove Pro access within 1 hour) | `____` |
| Does the store ask us for information about the purchase? | `____` (Apple may send a request asking how much the customer used the product; note how fast you must answer: `____`) | `____` |
| How does a customer cancel a subscription? | `____` (example: iPhone Settings > Subscriptions) | `____` (example: Play Store > Subscriptions) |
| Who answers customer emails about store refunds? | `____` | `____` |
| What fee does the store take, and do we get it back on a refund? | `____` | `____` |
| Where do we find the store's refund rules, and date last checked? | `____` | `____` |

**Q6C.3 Write the short reply you send when a customer asks you for a store refund.**
- **Your answer:** `________`
- *Example:* "Hi {{name}}, because you bought in the app, Apple handles refunds. Please use this link: [link]. If Apple approves it, your access will update automatically."

**Q6C.4 How do you make sure access is removed when a store refund happens?**
- **Your answer:** `________`
- *Tip:* Test this in the store's sandbox before launch (Test #10 in Part 18).

**Q6C.5 Do customers also buy on your website? How do rules differ between web and store purchases?**
- **Your answer:** `________`
- *Tip:* A customer who subscribed in the store usually must cancel in the store. Write that on your cancel page so people do not get charged by mistake.

**Q6C.6 If a customer asks to move from a store plan to the website plan (or the opposite), what are the steps?**
- **Your answer:** `________`

**Q6C.7 What do you do about a customer who asks you for a refund **and** asks the store at the same time?**
- **Your answer:** `________`
- *Tip:* Do not refund on your side for a charge the store collected. Check first.

---

# PART 7. DISPUTES AND CHARGEBACKS `[PRE-LAUNCH]` `[LAUNCH 1-100]` `[SCALE 101-500]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> **Words to know.** A **refund** is when YOU give money back. A **dispute** or **chargeback** is when the customer's BANK takes the money back after the customer complains to it. Chargebacks cost you time and fees. Too many can get your payment account closed.

**Q7.1 Where will every dispute be recorded?**
- **Your answer:** `________`
- *Example:* "A spreadsheet called 'Dispute Tracker' (see Q7.8)."

**Q7.2 Write your dispute steps in order.**

| Step | Action | Who | Deadline |
|---|---|---|---|
| 1 | Alert arrives. Write down the deadline **at once**. | `____` | within `____` hours |
| 2 | Find the order, customer, product, and all messages | `____` | `____` |
| 3 | Decide: **Fight** or **Accept** or **Refund first** | `____` | `____` |
| 4 | Collect evidence (Q7.4) | `____` | `____` |
| 5 | Submit evidence **once**, at least `____` days before the deadline | `____` | `____` |
| 6 | Record the result | `____` | `____` |
| 7 | Learn: fix the cause (Q7.9) | `____` | `____` |

**Q7.3 How do you decide whether to fight or accept?**
- **Your answer:** `________`
- *Example:* "Fight if we have proof the customer used the product. Accept if the amount is under $20 and evidence would take longer than it is worth. Always fight clear fraud."
- *Tip:* A weak answer and no answer both lose, but a weak answer may also cost a counter fee.

**Q7.4 What proof do you keep for each sale? Tick all that apply.**
- [ ] Customer email and name  [ ] IP address and country  [ ] Login history  [ ] Proof of use (logs, downloads, files created)
- [ ] Signed-up and accepted-terms record with date  [ ] Refund policy shown at checkout  [ ] Cancellation steps shown
- [ ] Support chat and email history  [ ] Delivery proof (for services: messages, files, completion)  [ ] Receipts and invoices
- [ ] 3D Secure or other authentication result  [ ] Other: `________`

**Q7.5 Where is this evidence stored and for how long?**
- **Your answer:** `________`
- *Example:* "In our database and exports, for 18 months after each purchase."
- *Tip:* Customers can dispute months later. Keep proof at least as long as the longest dispute window you face. Also check privacy rules (Part 15).

**Q7.6 How do you stop disputes before they happen?**
- [ ] Easy cancel button  [ ] Receipt email after every charge  [ ] Renewal reminder email `____` days before charging
- [ ] Clear statement descriptor  [ ] Fast support replies  [ ] Proactive refunds on obvious cases  [ ] Chargeback alert service: `________`

**Q7.7 What is your **dispute rate limit** (disputes divided by sales) before you act?**
- **Your answer:** Warning at `____%`, emergency at `____%`
- *Tip:* Card companies and payment providers watch this number. Keep it well under about 1%. Ask your provider for their current limit.

**Q7.8 Dispute Tracker columns. Tick the columns you will keep.**
- [ ] Date received  [ ] Deadline  [ ] Provider  [ ] Customer ID  [ ] Order ID  [ ] Amount  [ ] Reason code  [ ] Decision (fight/accept/refund)
- [ ] Evidence sent (yes/no)  [ ] Outcome (won/lost/withdrawn)  [ ] Fees paid  [ ] Root cause  [ ] Fix done (yes/no)

**Q7.9 After every lost dispute, what do you do to make sure it does not happen again?**
- **Your answer:** `________`
- *Example:* "Within 7 days, write the cause in the tracker, and fix checkout text or support steps."

**Q7.10 What if the customer refuses to refund **and** files a dispute anyway (so you refund twice)?**
- **Your answer:** `________`
- *Tip:* Refund **or** fight. Never do both on the same charge without checking with the provider, or you may pay twice.

---

# PART 8. FRAUD, ABUSE, AND SAFETY `[PRE-LAUNCH]` `[LAUNCH 1-100]` `[SCALE 101-500]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> **In plain words:** Some people try to cheat. This part is your plan for spotting cheaters without being unfair to honest customers.

**Q8.1 What kinds of misuse worry you? Tick all that apply.**
- [ ] Stolen cards  [ ] "Friendly fraud" (customer used the product and still disputes)  [ ] Refund hopping (buy, use, refund, repeat)
- [ ] Fake accounts and free-trial abuse  [ ] Marketplace sellers who do not deliver  [ ] Sharing account logins  [ ] Other: `________`

**Q8.2 What warning signs trigger a closer look?**
- **Your answer:** `________`
- *Example:* "Many sign-ups from one IP, billing country differs from IP country, 3+ refunds in 30 days."

**Q8.3 What action do you take on a confirmed abuser?**
- **Your answer:** `________`
- *Example:* "Block refunds, disable account, add email to a block list, record the reason."

**Q8.4 How do you treat customers fairly so you do not punish honest ones?**
- **Your answer:** `________`
- *Tip:* Always give a person a way to appeal.

**Q8.5 What do you do if you suspect a stolen card or a hacked account?**
- **Your answer:** `________`
- *Example:* "Refund the real cardholder, lock the account, report to the provider, and tell the real account owner."

---

# PART 9. SUBSCRIPTIONS, TRIALS, AND RENEWALS `[ALL]` (Mark `N/A` if you have no subscriptions)

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q9.1 How does a free trial work?**
- **Your answer:** Length `____` days. Card required? [ ] Yes  [ ] No. Auto-charges after? [ ] Yes  [ ] No

**Q9.2 What reminders do customers get before they are charged?**
- **Your answer:** Trial ends: `____` days before. Yearly renewal: `____` days before. Monthly renewal: `____`

**Q9.3 How does a customer cancel? How many clicks?**
- **Your answer:** `________`
- *Tip:* Cancelling should be as easy as signing up.

**Q9.4 What happens at cancellation?**
- **Your answer:** [ ] Access ends now  [ ] Access ends at end of paid period  [ ] Other: `________`

**Q9.5 Failed payments. How many retries, how many days, and what do you tell the customer?**
- **Your answer:** `________`
- *Example:* "Retry on day 3, 5, and 7. Email each time. Cancel on day 10."

**Q9.6 Price changes. How do you warn customers, and how far ahead?**
- **Your answer:** `________`

**Q9.7 Upgrades and downgrades. Do you pro-rate? How?**
- **Your answer:** `________`

**Q9.8 Pausing. Do you offer a pause instead of a cancellation?**
- **Your answer:** [ ] Yes, up to `____` months  [ ] No

**Q9.9 How do you handle one-time digital products (licenses, downloads)?**
- **Your answer:** `________`
- *Example:* "Refund within 14 days only if the file was not downloaded or the license not activated."

---

# PART 10. MARKETPLACE AND SERVICE PAYMENTS (OPTIONAL) `[ALL]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q10.0 Do you run a marketplace (buyers and sellers) or sell human services?**
- **Your answer:** [ ] No. Write `N/A` here and skip to Part 11.  [ ] Yes. Fill in **Appendix C** (questions Q10.1 to Q10.7), then come back.

---

# PART 11. LAWS AND RULES BY REGION `[BUILD]` `[PRE-LAUNCH]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> **Plain words:** Laws can give customers rights that your policy cannot take away. This template cannot give you legal advice. Use it to **list what applies** and ask a lawyer to check it. Search the official site of each regulator listed here for the current rule.

**Q11.1 Which laws did you check, and when? Fill in only the regions you ticked in Q1.4.**

| Region | What to check (starting points) | Did we check? | Date | Who checked |
|---|---|---|---|---|
| **United States (federal)** | FTC Negative Option Rule and ROSCA (US rules for online subscriptions: clear terms, clear consent, easy cancel); FTC rules on deceptive advertising; card network rules for recurring billing and free trials | [ ] | `____` | `____` |
| **United States (states)** | State auto-renewal laws (for example California, New York and many others: reminder emails, cancel online, special rules for free trials); state sales tax on refunds | [ ] | `____` | `____` |
| **European Union** | Consumer Rights Directive (14-day right to withdraw from online sales; digital content and services need clear agreement and acknowledgement to start early); Digital Content Directive (customer remedies when digital products do not work); rules on clear price information; strong customer authentication for card payments (PSD2, an extra ID check); GDPR for data | [ ] | `____` | `____` |
| **United Kingdom** | Consumer Contracts Regulations (14-day cancellation for distance sales); Consumer Rights Act 2015 (digital content must be as described and work); new subscription rules coming from the Digital Markets, Competition and Consumers Act 2024 (check the start date and details); UK GDPR | [ ] | `____` | `____` |
| **India** | Consumer Protection Act 2019 and E-Commerce Rules 2020 (a named grievance officer, quick acknowledgement of complaints, clear refund and cancellation terms); guidelines against "dark patterns" (tricks that push people to pay or stay); RBI rules for recurring card payments (customer approval, advance notice before each charge, extra approval above set limits); local tax (GST) on refunds | [ ] | `____` | `____` |
| **Australia / New Zealand** | Consumer guarantees (digital products must work and match the description; refund or replacement for major faults); rules on subscriptions and surcharges | [ ] | `____` | `____` |
| **Singapore / Japan / South Korea / Hong Kong** | Local e-commerce and consumer protection laws (for example Singapore's CPFTA, Japan's Act on Specified Commercial Transactions, South Korea's E-Commerce Act with a withdrawal period). List the ones you checked: `____` | [ ] | `____` | `____` |
| **Other countries** | Local rules for every country where you have `____` or more customers. List them: `____` | [ ] | `____` | `____` |
| **Everywhere** | Payment provider terms; card network rules; app store developer rules; your own Terms of Service; privacy law in each country | [ ] | `____` | `____` |

> **Where to look:** Search the official website of each regulator, for example the FTC and your state attorney general, the European Commission and your EU country's consumer office, the UK Government and Citizens Advice, India's Department of Consumer Affairs and RBI. Rules change, so write the **date** you checked next to each row.

**Facts to know (verify before relying):**
- **United States:** The FTC's 2024 "Click-to-Cancel" amendments were struck down by a federal appeals court in July 2025 on procedural grounds, and the FTC started a new rulemaking in March 2026. The older ROSCA law and state laws still apply, so keep cancelling easy and your terms clear.
- **EU and UK:** Online buyers usually have a 14-day cooling-off right. For digital content or services, the right can be lost only if the customer clearly agrees and acknowledges that before access starts. Save that proof with the date.
- **India:** Recurring card payments usually need customer approval and a notice before each charge. Check the current limits with your payment provider.

**Q11.1a For each region you sell to, write the 3 rules that most change your refund policy.**
- **Your answer:** Region: `____` Rule 1: `____` Rule 2: `____` Rule 3: `____`

**Q11.1b Where do you show different terms for different regions, and how does the checkout know which to show?**
- **Your answer:** `________`

**Q11.2 What cooling-off or withdrawal rights apply to your product, and how do you honor them?**
- **Your answer:** `________`
- *Example:* "EU/UK customers get 14 days. At checkout, they tick 'start now and lose cancellation right for digital content.' We save the tick with the date."

**Q11.3 Where do you state your refund terms legally? Tick all.**
- [ ] Terms of Service  [ ] Refund Policy page  [ ] Checkout page  [ ] Receipt  [ ] Subscription terms

**Q11.4 Do you need to show prices with taxes, and how are taxes handled on refunds?**
- **Your answer:** `________`
- *Tip:* Usually the tax collected must also be returned. Ask your accountant (see Part 12).

**Q11.5 How do you handle complaints that go to a regulator, consumer office, or ombudsman?**
- **Your answer:** `________`

**Q11.6 Have you had a lawyer review this document?**
- **Your answer:** [ ] Yes, date `____-__-__`  [ ] Not yet, planned for `____-__-__`

---

# PART 12. MONEY, RECORDS, AND TAXES `[PRE-LAUNCH]` `[LAUNCH 1-100]` `[SCALE 101-500]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> **In plain words:** Every refund is money moving out of your business. Write it down, match it to the bank, and know the tax effect.

**Q12.1 Who does your bookkeeping and which tool do you use?**
- **Your answer:** `________`

**Q12.2 What do you write in the Refund Log for each refund?**
- [ ] Date  [ ] Order ID  [ ] Customer ID  [ ] Amount  [ ] Currency  [ ] Reason (from Q3.3)  [ ] Full or partial
- [ ] Who approved  [ ] Provider  [ ] Provider refund ID  [ ] Link to the support conversation

**Q12.3 Who pays the processing fees when you refund?**
- **Your answer:** `________`
- *Tip:* Providers often keep the original fee on a refund. Check your provider's current rule and write it here: `________`

**Q12.4 How do you handle refunds in different currencies and exchange rates?**
- **Your answer:** `________`

**Q12.5 How do you handle tax (VAT, GST, sales tax) on refunds and credit notes?**
- **Your answer:** `________`

**Q12.6 How often do you reconcile (match your records to the provider's)?**
- **Your answer:** Weekly for first 100 customers; `____` after that.

**Q12.7 How much money do you keep aside to cover refunds and disputes?**
- **Your answer:** `____%` of monthly revenue, or `$____`
- *Tip:* Some providers hold a rolling reserve. Know the amount and release dates.

**Q12.8 How long do you keep financial records?**
- **Your answer:** `____ years`
- *Tip:* Check your country's tax authority for the minimum.

**Q12.9 Who approves the monthly refund and dispute report, and where is it saved?**
- **Your answer:** `________`

---

# PART 13. CUSTOMER MESSAGES (COPY-AND-PASTE TEMPLATES) `[PRE-LAUNCH]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> Write each message in your brand voice. Keep messages short, kind and clear. Fill in each box. Use `{{name}}`, `{{order_id}}`, `{{amount}}`, `{{date}}` as placeholders.

**Q13.1 Refund approved.**
- **Your answer:** `________`
- *Example:* "Hi {{name}}, we have refunded {{amount}} for order {{order_id}}. It can take {{days}} business days to appear. Sorry for the trouble."

**Q13.2 Refund denied (with a kind reason and another option).**
- **Your answer:** `________`

**Q13.3 We need more information.**
- **Your answer:** `________`

**Q13.4 Partial refund offered.**
- **Your answer:** `________`

**Q13.5 We found a duplicate or billing mistake on our side.**
- **Your answer:** `________`

**Q13.6 Trial or renewal reminder.**
- **Your answer:** `________`

**Q13.7 Subscription cancelled confirmation.**
- **Your answer:** `________`

**Q13.8 Store purchase: how to request a refund from Apple or Google.**
- **Your answer:** `________`

**Q13.9 A dispute was opened. (Message to customer asking if there was a mistake, only where allowed.)**
- **Your answer:** `________`
- *Tip:* Do not pressure the customer to cancel the dispute in ways the card rules forbid. Ask your provider.

**Q13.10 Account locked for abuse, with how to appeal.**
- **Your answer:** `________`

**Q13.11 Tone rules. List 3 do's and 3 don'ts.**
- **Do:** `________`
- **Don't:** `________`
- *Example:* "Do say sorry once. Do give a date. Don't blame the customer."

---

# PART 14. RULES FOR AI AGENTS `[BUILD]` `[PRE-LAUNCH]` `[LAUNCH 1-100]` `[SCALE 101-500]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> **In plain words:** An AI helper is like a very fast new employee. It can prepare work, but a named human checks it before any money moves.

> **Chosen model: "AI drafts, a human approves."** The AI collects facts, applies Part 4, drafts the answer and the refund request. **A named human gives the final yes** before any money moves or any dispute evidence is sent.

**Q14.1 Which tasks can AI do on its own? Tick all that apply.**
- [ ] Read refund requests and summarize them
- [ ] Look up the order and payment in read-only mode
- [ ] Apply the Part 4 table and recommend yes / no / ask
- [ ] Draft the customer reply (human sends)
- [ ] Draft dispute evidence (human submits)
- [ ] Add rows to the Refund Log and Dispute Tracker
- [ ] Send low-risk messages (e.g., "we received your request"): `________`

**Q14.2 Which tasks must ALWAYS wait for a human? Tick all that apply.**
- [ ] Sending any refund  [ ] Submitting dispute evidence  [ ] Closing or locking accounts  [ ] Changing prices or plans
- [ ] Messages to lawyers, regulators, or banks  [ ] Anything above `$____`  [ ] Anything involving a minor, health, or legal threat

**Q14.3 Which human approves, and how do they approve (button, reply, ticket)?**
- **Your answer:** `________`

**Q14.4 When must the AI stop and hand over to a person? Tick all that apply.**
- [ ] The answer in this document is blank or `TBD`  [ ] Two rules conflict  [ ] The customer is angry or threatens legal action
- [ ] The customer is under 18  [ ] Possible fraud  [ ] Amount above Q4.2  [ ] Provider outage or tool error  [ ] AI confidence below `____%`

**Q14.5 What should the AI never do? (Hard no's.)**
- **Your answer:** `________`
- *Example:* "Never invent policy. Never promise a refund before approval. Never reveal other customers' data. Never refund to a different payment method."

**Q14.6 What must the AI write down for every case? (So a human can check it.)**
- [ ] The question numbers it used  [ ] The facts it found  [ ] Its recommendation  [ ] Its confidence  [ ] What it could not find

**Q14.7 How does the AI access your systems?**
- **Your answer:** Read-only keys? [ ] Yes  [ ] No. Refund-capable keys? [ ] No (recommended)  [ ] Yes, limited to `$____`
- *Tip:* Give AI the least access that does the job. Store keys in a secrets manager, never in this file.

**Q14.8 How will you check the AI's work?**
- **Your answer:** Review `____%` of cases weekly (suggested: 100% for the first 100 customers, then 20% sampling).

**Q14.9 What do you do when the AI makes a mistake?**
- **Your answer:** `________`
- *Example:* "Fix the customer's case first, record the error, update Part 4 or Part 14, re-run test cases (Part 18)."

**Q14.10 Which AI tools or models are used, and who can change their settings?**
- **Your answer:** `________`

**Q14.11 Is the customer told when AI helped write the reply, if required by law or by your policy?**
- **Your answer:** `________`

---

# PART 15. TOOLS, DATA, AND PRIVACY `[BUILD]` `[PRE-LAUNCH]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q15.1 List every tool involved in refunds and disputes.**

| Tool | What it does | Who can use it | Where the data lives |
|---|---|---|---|
| `____` (example: Stripe) | Payments | `____` | `____` |
| `____` (example: help desk) | Support messages | `____` | `____` |
| `____` (example: database) | Orders and usage | `____` | `____` |
| `____` (example: spreadsheet) | Refund Log, Dispute Tracker | `____` | `____` |

**Q15.2 What customer data do you keep for refunds and disputes, and why?**
- **Your answer:** `________`

**Q15.3 How long do you keep it, and how do you delete it when asked?**
- **Your answer:** `________`
- *Tip:* Some laws let people ask for deletion, but you may keep records needed for taxes, fraud and disputes. Ask a lawyer.

**Q15.4 Never store full card numbers or security codes yourself. Confirm.**
- **Your answer:** [ ] Confirmed, only the provider stores card data

**Q15.5 Who can see refund and dispute data? Are logs kept of who looked?**
- **Your answer:** `________`

**Q15.6 If there is a data leak, who do you tell and within how many hours?**
- **Your answer:** `________`

---

# PART 16. THE JOURNEY: FROM BUILD TO YOUR FIRST 500 CUSTOMERS `[ALL]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> Tick each box when it is finished. Add a date. If a step does not apply, write `N/A`.

## Phase 1: BUILD AND TEST `[BUILD]`

- [ ] Parts 0 to 5 filled in (date `____-__-__`)
- [ ] Payment accounts created in **test mode** (Stripe test mode, PayPal sandbox, store sandbox)
- [ ] Refund button or API call built and tested with fake payments
- [ ] Partial refunds tested
- [ ] Failed refund handled
- [ ] Webhooks and notifications tested (refund created, dispute opened, subscription cancelled)
- [ ] Access removal after refund tested
- [ ] Receipts, renewal emails, and cancel flow tested
- [ ] Statement descriptor set and checked
- [ ] Evidence data being saved from day one (Q7.4)
- [ ] AI agent run on **fake** cases only; all Part 18 tests passed
- [ ] Legal basics researched (Part 11)

**Q16.1 What blocks you in this phase?**
- **Your answer:** `________`

## Phase 2: PRE-LAUNCH AND BETA `[PRE-LAUNCH]`

- [ ] Refund policy published everywhere in Q3.8
- [ ] "How to cancel" and "How to get a refund" pages live
- [ ] Support inbox monitored and replies tested
- [ ] Dispute alert emails reaching a real person
- [ ] Lawyer or advisor reviewed Parts 3, 9, 11 (or risk accepted by: `____`)
- [ ] Provider accounts switched to live mode and verified
- [ ] One **real** $1 or small test purchase and refund done
- [ ] Beta users told how refunds work
- [ ] Refund Log and Dispute Tracker created
- [ ] Emergency plan (Part 19) written

**Q16.2 How many beta users, and how will you collect feedback about billing?**
- **Your answer:** `________`

## Phase 3: LAUNCH TO CUSTOMER 100 `[LAUNCH 1-100]`

**Rule of this phase: do things by hand and learn.** A human reads every refund request and every AI draft.

- [ ] Every refund reviewed by a human
- [ ] Every dispute answered personally
- [ ] Weekly 30-minute review of the Refund Log and Dispute Tracker
- [ ] Top 3 refund reasons identified and written below
- [ ] Policy or product fixed for each top reason
- [ ] Part 4 table updated with real cases
- [ ] First month-end reconciliation done

**Q16.3 Top refund reasons so far:**
- 1. `________`  2. `________`  3. `________`

**Q16.4 What did you change because of customers' complaints?**
- **Your answer:** `________`

**Q16.5 Are refunds above your goal? (Goal from Part 17)**
- **Your answer:** `________`

## Phase 4: CUSTOMER 101 TO 500 `[SCALE 101-500]`

**Rule of this phase: automate the easy cases, protect the hard ones.**

- [ ] Easy cases (duplicates, clear policy matches) drafted faster with AI and approved in batches
- [ ] Human sampling of AI cases (Q14.8) kept running
- [ ] Monthly report on refunds, disputes, fees, and root causes
- [ ] Dispute rate under the limit in Q7.7
- [ ] Chargeback alert or prevention tool considered
- [ ] Second backup person trained (Q2.1)
- [ ] Policy reviewed after 250 customers and again at 500
- [ ] Taxes and accounting for refunds checked with an accountant
- [ ] Lawyer re-check if you entered new countries

**Q16.6 What will change when you pass 500 customers?**
- **Your answer:** `________`

---

# PART 17. NUMBERS TO WATCH (KPIs) `[LAUNCH 1-100]` `[SCALE 101-500]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q17.1 Fill in your targets. If unsure, start with the suggestions and adjust after 100 customers.**

| Number | How to calculate | Your target | Suggested start | Check how often |
|---|---|---|---|---|
| Refund rate | refunds / sales | `____%` | under 5% | weekly, then monthly |
| Dispute (chargeback) rate | disputes / sales | `____%` | under 0.5% | weekly |
| Dispute win rate | won / disputes fought | `____%` | above 40% | monthly |
| First reply time | hours until first reply | `____` | under 24h | weekly |
| Refund completion time | request to money sent | `____` | under 3 business days | weekly |
| Money refunded | total refunded / revenue | `____%` | under 5% | monthly |
| Dispute and counter fees paid | sum of fees | `$____` | track only | monthly |
| AI draft accepted unchanged | accepted / total drafts | `____%` | track only | weekly |
| AI mistakes found | errors / reviewed cases | `____%` | under 2% | weekly |
| Repeat refund customers | repeat / refunded customers | `____%` | track only | monthly |
| Refunds by plan | refunds for a plan / sales of that plan | `____%` | track only | monthly |
| Early churn | customers who leave within 30 days / new customers | `____%` | track only | monthly |
| Trial-to-paid refund rate | refunds in first 14 days / trial conversions | `____%` | under 8% | monthly |
| Average refund amount | total refunded / number of refunds | `$____` | track only | monthly |
| Net money lost to refunds | refunds + fees not returned + dispute losses | `$____` | track only | monthly |
| Dispute rate by provider | disputes / sales for each provider | `____%` | under 0.5% | weekly |
| Disputes with evidence sent on time | on-time submissions / disputes fought | `____%` | 100% | weekly |
| Days left when evidence is sent | average days before deadline | `____` | at least 3 | monthly |
| Refunds that stopped a dispute | refunds given after a customer warned of a dispute | `____` | track only | monthly |
| Billing support tickets per 100 customers | billing tickets / customers x 100 | `____` | track only | monthly |
| Solved in one reply | cases closed in first reply / all cases | `____%` | above 60% | monthly |
| Customer rating after a refund | average score from a short survey | `____` | above 4 of 5 | monthly |
| Top 3 refund reasons (share of all refunds) | reason count / total refunds | `____` | track only | monthly |
| AI drafts changed by a human | changed drafts / total drafts | `____%` | track only | weekly |
| AI cases handed to a person | handed over / all AI cases | `____%` | track only | weekly |

**Q17.2 What do you do if a number goes past its limit?**
- **Your answer:** `________`
- *Example:* "If dispute rate passes 0.5%, pause paid ads, review the last 10 disputes, fix the cause within 7 days."

---

# PART 18. TEST CASES (QUALITY CHECK) `[BUILD]` `[PRE-LAUNCH]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

> Run these tests with fake data. Write **Pass** or **Fail** and the date. Fix failures before launch. Re-run after every big change to policy, payment code, or AI settings.

| # | Test | Expected result | Pass/Fail | Date |
|---|---|---|---|---|
| 1 | Full refund, card, within window | Money returned, access removed, log entry, email sent | `____` | `____` |
| 2 | Partial refund | Correct amount (Q5.7) | `____` | `____` |
| 3 | Refund after window | Declined politely, offer in Q3.5 | `____` | `____` |
| 4 | Duplicate charge | Refund automatic or fast | `____` | `____` |
| 5 | Cancel during trial | No charge | `____` | `____` |
| 6 | Cancel a paid subscription | Stops next charge, access per Q9.4 | `____` | `____` |
| 7 | Refund fails | Handled as Q5.9 | `____` | `____` |
| 8 | Dispute opened (test mode) | Alert arrives, deadline recorded | `____` | `____` |
| 9 | Dispute evidence package | All Q7.4 items found in under `____` minutes | `____` | `____` |
| 10 | Apple/Google store refund notice | Access removed | `____` | `____` |
| 11 | Wrong person asks for refund | Identity check (Q5.4) stops it | `____` | `____` |
| 12 | Customer in EU or UK asks inside 14 days | Cooling-off handled per Q11.2 | `____` | `____` |
| 13 | AI sees a blank or `TBD` answer | AI stops and asks a human | `____` | `____` |
| 14 | AI asked to refund above its limit | AI refuses and hands over | `____` | `____` |
| 15 | AI asked to reveal another customer's data | AI refuses | `____` | `____` |
| 16 | Angry customer threatens legal action | Handed to human | `____` | `____` |
| 17 | Marketplace: seller did not deliver | Process in Q10.5 followed | `____` | `____` |
| 18 | Currency refund (non-USD) | Correct amount and currency | `____` | `____` |
| 19 | Refund plus tax | Tax handled per Q12.5 | `____` | `____` |
| 20 | Provider outage during a deadline | Plan in Part 19 followed | `____` | `____` |

**Q18.1 Who signs off that all tests pass?**
- **Your answer:** `________` Date: `____-__-__`

---

# PART 19. WHEN THINGS GO WRONG (EMERGENCY AND ESCALATION) `[PRE-LAUNCH]` `[ALL]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q19.1 What counts as an emergency? Tick all that apply.**
- [ ] A wave of refunds in one day (more than `____`)  [ ] Dispute rate above Q7.7 emergency level  [ ] A bug that charged many people wrongly
- [ ] The provider froze or threatens to close our account  [ ] Fraud attack  [ ] AI sent wrong refunds or wrong messages  [ ] Data leak

**Q19.2 First hour checklist.**
1. Stop the damage (pause billing, pause AI refunds, pause ads): `________`
2. Tell the owner: `________`
3. Write what happened and the time: `________`
4. Contact the provider if needed: `________`
5. Tell affected customers when you know the facts: `________`

**Q19.3 Who has the power to pause billing or turn off the AI agent, and how?**
- **Your answer:** `________`

**Q19.4 What do you say to customers after a billing mistake on your side?**
- **Your answer:** `________`
- *Tip:* Say what happened, what you did, and what you will do. Do it fast.

**Q19.5 If your payment account is frozen, what is the plan to keep refunds and support running?**
- **Your answer:** `________`

**Q19.6 After the emergency, what is the review process?**
- **Your answer:** `________`
- *Example:* "Within 5 days, write what happened, why, and what will change; update this document."

---

# PART 20. KEEPING THIS DOCUMENT FRESH `[ALL]`

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q20.1 When do you review this document? Tick all that apply.**
- [ ] Every month for the first 3 months after launch  [ ] Every quarter after that  [ ] After every lost dispute pattern
- [ ] When a provider changes fees or rules  [ ] When a law changes  [ ] When you add a country, product, or provider  [ ] When AI tools change

**Q20.2 Which "facts to remember" in this document must be re-checked each review?**
- Stripe fees and deadlines (Part 6A)
- PayPal time windows and Seller Protection rules (Part 6B)
- Apple and Google refund rules (Part 6C)
- US subscription rules (Part 11)
- EU, UK, India, APAC consumer rules (Part 11)
- **Your answer:** Date last checked: `____-__-__` by `____`

**Q20.3 Change log. Write each change.**

| Date | What changed | Why | Who |
|---|---|---|---|
| `____` | `____` | `____` | `____` |
| `____` | `____` | `____` | `____` |

---

# PART 21. FINAL READINESS CHECK (IS THIS DOCUMENT GOOD TO GO?) `[ALL]`

Tick every box. If any box cannot be ticked, fix it first.

**Completeness**
- [ ] No question is blank. Every unknown says `TBD by [date] by [name]` or `N/A because [reason]`
- [ ] Every number has a unit (days, dollars, percent)
- [ ] Every role in Part 2 has a name and a backup

**Clarity**
- [ ] A stranger could follow Part 5 and Part 7 without asking you anything
- [ ] The decision table in Part 4 has no row that says "it depends"
- [ ] Customer messages in Part 13 are written and tested

**Safety and law**
- [ ] Refund policy matches the law of every country you sell to (Part 11)
- [ ] No secrets or private customer data are written in this file
- [ ] A lawyer reviewed it, or the owner accepted the risk in writing

**Money**
- [ ] Refund Log, Dispute Tracker, and reconciliation plan exist
- [ ] Reserve for refunds and disputes decided (Q12.7)

**AI**
- [ ] AI limits (Part 14) are written and tested
- [ ] All 20 tests in Part 18 passed

**Extras**
- [ ] Appendix D reason-code table matched to my provider's wording
- [ ] Appendix E AI prompt pasted into my AI tool with all `[brackets]` filled
- [ ] Appendix F tables copied into my spreadsheet and tested with one fake row
- [ ] Appendix C filled in, or marked `N/A` (Part 10)

**Launch journey**
- [ ] Phases 1 and 2 of Part 16 are complete before taking real money
- [ ] Review dates are in the calendar (Q20.1)

**Sign-off**
- **Document owner:** `________`  **Date:** `____-__-__`
- **Second reviewer:** `________`  **Date:** `____-__-__`

---

# APPENDIX A. SIMPLE WORD LIST (GLOSSARY)

| Word | Simple meaning |
|---|---|
| **Refund** | You give the money back to the customer. |
| **Chargeback / Dispute** | The customer's bank takes the money back after the customer complains. |
| **Evidence** | Proof you send to show the sale was real and the customer got what they paid for. |
| **Reason code** | A short code the bank gives to say why the customer disputed. |
| **Friendly fraud** | A real customer who got the product but disputes the charge anyway. |
| **Merchant of record** | The seller the customer legally buys from. |
| **Statement descriptor** | The business name on the customer's bank statement. |
| **Cooling-off period** | A short time when the law lets a customer change their mind. |
| **Pro-rated refund** | A refund for only the unused part of what was paid. |
| **Webhook** | An automatic message from a payment provider to your system. |
| **Reconciliation** | Checking your records match the provider's records. |
| **Sandbox / test mode** | A fake version of a payment system for safe testing. |
| **Rolling reserve** | Money a provider holds back for a time to cover possible refunds and disputes. |
| **Separation of duties** | Two different people (or two different steps) handle a risky task. |
| **KPI** | A number you watch to know if things are going well. |

# APPENDIX B. SOURCES TO RE-CHECK AT EVERY REVIEW

- Stripe: dispute and refund documentation in the Stripe Docs and Support pages
- PayPal: Resolution Center and Seller Protection pages
- Apple: App Store refunds and "Report a Problem" help pages; App Store Server Notifications; App Store Review rules
- Google: Google Play refund policy; Play Console help; real-time developer notifications
- US: FTC (Negative Option Rule, ROSCA), your state's attorney general site
- EU / UK: official consumer rights pages (European Commission; UK Government and Citizens Advice)
- India: Department of Consumer Affairs and RBI circulars
- Card networks (Visa, Mastercard): dispute monitoring programs, as described by your provider

---

# APPENDIX C. MARKETPLACE AND SERVICE PAYMENTS (FILL IN ONLY IF YOU RUN A MARKETPLACE) `[ALL]`

> **In plain words:** A marketplace is a place where one group sells and another buys, and you sit in the middle. When something goes wrong, you may need to decide who gets the money.

`Status: [ ] Not started   [ ] In progress   [ ] Done   [ ] Needs review`

**Q10.1 Who is the "merchant of record" (the one the customer legally buys from)?**
- **Your answer:** `________`

**Q10.2 When do sellers get paid?**
- **Your answer:** [ ] Right away  [ ] After delivery is confirmed  [ ] After `____` days  [ ] Other: `________`

**Q10.3 Who pays when a refund or chargeback happens: you or the seller?**
- **Your answer:** `________`
- *Example:* "The seller's payout is reduced. If the seller has no balance, we cover it and recover later."

**Q10.4 How do buyers and sellers report problems, and who judges them?**
- **Your answer:** `________`

**Q10.5 What is your step-by-step process to settle a buyer-versus-seller dispute?**

| Step | Action | Who | Time limit |
|---|---|---|---|
| 1 | Buyer opens a problem report | Buyer | within `____` days of delivery |
| 2 | Seller answers | Seller | within `____` days |
| 3 | We review the proof from both | `____` | `____` days |
| 4 | We decide: refund / partial / no refund | `____` | `____` |
| 5 | Either side can appeal once | `____` | `____` |

**Q10.6 What do you do if a seller disappears or does not deliver?**
- **Your answer:** `________`

**Q10.7 How do you protect against sellers cheating?**
- **Your answer:** `________`
- *Example:* "Holdback of 10% for 14 days, identity check before first payout."

---

# APPENDIX D. DISPUTE REASON-CODE GUIDE (WHAT TO DO FOR EACH KIND OF DISPUTE)

### D1. Card disputes (Stripe reason names)

> **In plain words:** When a customer's bank takes money back, it gives a **reason**. The reason tells you what proof to send. Find the reason on the dispute page, find it in this table, then gather the proof in the third column. Names below follow Stripe's reason names. PayPal and card networks use different words for the same ideas.

**Step 1.** Find the reason shown on the dispute. **Step 2.** Match it below. **Step 3.** Decide to fight or accept (Q7.3). **Step 4.** Send proof **once**, before the deadline.

| Reason (Stripe name) | What the customer is saying | Best proof to send | How to prevent it | Usually fight? |
|---|---|---|---|---|
| **fraudulent** | "I did not make this purchase." | Login history, IP and device match, email and name match, 3D Secure result, delivery or use proof | Card checks, 3D Secure, fraud tools, clear descriptor | Yes if proof of use exists |
| **unrecognized** | "I don't know this charge." | Receipt email, sign-up record, descriptor explanation, proof of use | Clear descriptor, receipt after every charge | Yes if the customer used the product |
| **subscription_canceled** | "I cancelled but you charged me." | Cancel history (was there one?), terms shown, renewal reminder emails | Easy cancel, reminders before charging | Only if no cancel was ever made |
| **product_not_received** | "I never got it." | Delivery proof, download logs, login after purchase, messages | Instant delivery emails, activity logs | Yes if delivered |
| **product_unacceptable** | "It was not as described or it is broken." | Product description at checkout, support chats, proof you tried to fix | Honest descriptions, fast support | Case by case |
| **duplicate** | "I was charged twice." | Show the two charges are for two different orders, or refund the extra one | Stop double-clicks, code that stops double charges | Refund if you did double charge |
| **credit_not_processed** | "I was promised a refund and did not get it." | Proof the refund was sent (provider refund ID, date) or send it now | Refund fast, send confirmation | Refund if owed |
| **incorrect_account_details / insufficient_funds / bank_cannot_process / debit_not_authorized** | Bank or account problems, mostly for bank debits | Proof the customer agreed to the bank debit, plus payment records | Clear sign-up consent, retry rules | Case by case |
| **customer_initiated / general** | "Something is wrong." (no clear reason) | Everything: receipt, usage, messages, policy shown | Good records for every sale | Usually yes |

**Q-D1 Which reason do you expect most often, and what is your plan for it?**
- **Your answer:** `________`
- *Example:* "subscription_canceled: add a reminder email 7 days before renewal and a one-click cancel link in every receipt."

**Q-D2 For each reason in your table above, who gathers the proof and how long do they have?**
- **Your answer:** `________`


### D2. PayPal dispute types (same idea, PayPal's words)

> **In plain words:** PayPal calls the reason a "dispute type." Match it, gather the proof, and answer **inside the time PayPal gives you** (see Part 6B). PayPal seller protection often does **not** cover digital goods or services, so strong proof matters even more.

| PayPal type | What the customer is saying | Best proof to send | How to prevent it | Usually fight? |
|---|---|---|---|---|
| **Unauthorized transaction** | "I did not make this payment." | Login and IP history, matching email and name, proof of use, receipt | Clear descriptor, receipt emails, fraud checks | Yes if proof of use exists |
| **Item not received** | "I never got it." | Proof of delivery: download or access logs, delivery email, login after purchase | Instant delivery emails, activity logs | Yes if delivered |
| **Significantly not as described** | "It is not what you said." | Product page and checkout text (with date), support chats, proof you tried to fix it | Honest descriptions, fast support | Case by case |
| **Duplicate transaction** | "I was charged twice." | Show two separate orders, or refund the extra one | Code that stops double charges | Refund if you double charged |
| **Incorrect amount / credit not received** | "The amount is wrong" or "my refund never arrived." | Invoice, price shown at checkout, refund ID and date | Show the price clearly, refund fast | Refund if owed |
| **Cancelled subscription still charged** | "I cancelled but you charged me." | Cancel history, reminder emails, terms shown | Easy cancel, reminders before charging | Only if no cancel was ever made |
| **Other** | Something else | Everything: receipt, usage, messages, policy shown | Good records for every sale | Usually yes |

**Q-D3 Which PayPal dispute type do you expect most, and what is your plan for it?**
- **Your answer:** `________`

**Evidence packet checklist (copy for each dispute)**
- [ ] Customer name and email  [ ] Order ID and date  [ ] Amount  [ ] Product or plan bought
- [ ] Proof the customer used it (dates, logs)  [ ] Terms and refund policy shown at checkout (screenshot with date)
- [ ] Support messages  [ ] Cancel history  [ ] Receipts and reminder emails sent
- [ ] One-page summary (5 sentences: who, what, when, proof, what you ask the bank to do)

---

# APPENDIX E. AI AGENT PROMPT BLOCK (COPY AND PASTE)

> **How to use:** Paste the text below into your AI tool's instructions (system prompt). Replace the parts in `[square brackets]`. Keep this file in the AI's reach so it can read your answers. Update the prompt whenever Part 14 changes.

```text
ROLE
You are the Refund and Dispute Assistant for [PROJECT NAME].
Your job: read refund requests and disputes, check them against the company's
Refund and Dispute Handling document, and prepare a recommendation for a human.

SOURCE OF TRUTH
Use ONLY the file "Refund_and_Dispute_Handling.md" (version [X.Y]).
If an answer you need is blank, says TBD, or is missing: STOP and ask [HUMAN OWNER NAME].
Never guess. Never invent policy, prices, deadlines, or legal rules.

WHAT YOU MAY DO (see Part 14, Q14.1)
- Read requests and summarize them.
- Look up orders and payments in READ-ONLY mode.
- Apply the decision table (Part 4) and recommend: YES, NO, or ASK A PERSON.
- Draft the reply using the message templates in Part 13.
- Draft dispute evidence using Appendix D and Part 7.
- Add rows to the Refund Log and Dispute Tracker (Appendix F).

WHAT YOU MAY NOT DO WITHOUT A HUMAN YES (see Part 14, Q14.2)
- Send a refund. Submit dispute evidence. Lock or close an account.
- Change prices or plans. Contact lawyers, banks, or regulators.
- Anything above $[AMOUNT]. Anything about a minor, health, or a legal threat.

HARD NO'S
- Never refund to a different payment method than the original.
- Never share one customer's data with another person.
- Never promise a refund before a human approves.
- Never pressure a customer to drop a dispute.

STOP AND HAND OVER WHEN
- The document is unclear or contradicts itself.
- The customer is angry, threatens legal action, or may be under 18.
- You suspect fraud, or the amount is above the limit.
- A tool fails or a provider is down.
- Your confidence is below [XX]%.

OUTPUT FORMAT (always)
1. Case summary (2 lines)
2. Facts found (bullet list, with where you found each)
3. Rules used (question numbers, for example "Q4.1 row 2")
4. Recommendation: YES / NO / ASK A PERSON
5. Draft reply to the customer
6. What you could not find or are unsure about
7. Deadline (if a dispute) and who must act

TONE
Kind, short, clear. Say sorry once. Give dates. Do not blame the customer.
```

**Q-E1 What did you put in each `[square bracket]`?**
- **Your answer:** `________`

**Q-E2 How will you test the prompt?**
- **Your answer:** Run the 20 tests in Part 18 and write results there.

---

# APPENDIX F. READY-TO-COPY TABLES

> **How to use:** Copy these tables into your spreadsheet (Google Sheets, Excel, Notion, Airtable). One row per refund or dispute. Do not put card numbers or passwords in them.

## F1. Refund Log

| Date | Order ID | Customer ID | Product / plan | Amount | Currency | Reason (from Q3.3) | Full or partial | Approved by | Provider | Provider refund ID | Access changed? | Support link | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` |
| `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` |
| `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` |

*Copy-paste header (CSV):*
`date,order_id,customer_id,product,amount,currency,reason,full_or_partial,approved_by,provider,provider_refund_id,access_changed,support_link,notes`

## F2. Dispute Tracker

| Date received | **Deadline** | Provider | Customer ID | Order ID | Amount | Reason | Decision (fight / accept / refund) | Evidence sent (date) | Outcome (won / lost / withdrawn) | Fees paid | Root cause | Fix done (date) |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` |
| `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` |
| `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` | `____` |

*Copy-paste header (CSV):*
`date_received,deadline,provider,customer_id,order_id,amount,reason,decision,evidence_sent,outcome,fees_paid,root_cause,fix_done`

## F3. Weekly Review Sheet (10 minutes)

| Week of | Refunds | Disputes | New disputes with deadline this week | Top reason | Any AI mistakes? | One fix to make |
|---|---|---|---|---|---|---|
| `____` | `____` | `____` | `____` | `____` | `____` | `____` |

---

# APPENDIX G. WORKED EXAMPLE (A COMPLETELY FILLED-IN SAMPLE)

> **This is a made-up project.** Use it only to see what a good answer looks like. Do not copy it. Your answers must be about **your** project.

**Project:** PixelPlan, a budgeting app for students. **Plans:** Pro, $6 per month or $60 per year. **Sold via:** Stripe on the web, and the Apple App Store in the app. **Team:** Maya (founder), Sam (part-time helper). **Customers:** US, UK, India. **AI tool:** a chat AI that drafts replies.

| Question | Sample answer |
|---|---|
| **Q0.1** Project | PixelPlan, a budgeting app for students |
| **Q0.2** Owner | Maya Rossi, maya@pixelplan.example |
| **Q1.2** What customers buy | Monthly and yearly subscription, 7-day free trial |
| **Q1.5** Providers | Stripe (web), Apple App Store (iPhone app) |
| **Q1.6** Statement descriptor | "PIXELPLAN.APP" |
| **Q2** Roles | Maya is Policy Owner, Refund Approver, Dispute Handler, Legal Contact and AI Supervisor. Sam is Support Agent and backup Dispute Handler. |
| **Q2.3** Second pair of eyes | Over $60, Maya waits 24 hours and re-reads the case. |
| **Q3.1** Approach | Subscription: 14-day money-back guarantee, then refunds only for billing mistakes |
| **Q3.2** Window | 14 days |
| **Q3.3** Refund reasons | Duplicate charge, charged after cancelling, product broken and not fixed, first-time forgotten trial, legal right |
| **Q3.4** No refund | Change of mind after 14 days, repeat refunds (more than 2 in 12 months) |
| **Q3.6** After refund | Pro access ends right away; free plan stays |
| **Q3.7** Timing | We send within 2 business days; the bank may take 5 to 10 more |
| **Q3.8** Short policy | "Try Pro for 14 days. If it's not for you, email us and we'll refund your payment. After 14 days we refund billing mistakes. Cancel any time in Settings, in 2 clicks." |
| **Q4.1 row 2** Charged after cancelling | Refund: Yes. Amount: full last charge. Approver: Support Agent. Note: check cancel date in Stripe. |
| **Q4.1 row 5** Forgot trial | Refund: Yes, once. Amount: full. Approver: Support Agent. |
| **Q4.1 row 7** Annual plan after 3 months | Refund: No refund of unused time. Offer 2 free months. Approver: Maya. |
| **Q4.2 / Q4.3** Limits | Support Agent up to $60. Never above $120 without Maya. |
| **Q5.2** First reply | Within 24 hours on weekdays |
| **Q5.4** Identity check | Reply from the account email, plus last 4 card digits |
| **Q6A.2** Stripe alerts | Alerts go to disputes@pixelplan.example, read daily at 9:00 |
| **Q6C.2** Who decides for iPhone purchases | Apple decides. We send customers to Apple's "Report a problem" page and remove Pro access when Apple tells us about a refund. |
| **Q7.2 step 5** Evidence deadline | Submit 3 days before the deadline shown |
| **Q7.3** Fight or accept | Fight if the user logged in after the charge. Accept under $10 if evidence would take longer than it is worth. |
| **Q7.7** Dispute rate limits | Warning at 0.4%, emergency at 0.8% |
| **Q9.2** Reminders | Trial ends: email 2 days before. Yearly renewal: email 14 days before. |
| **Q9.5** Failed payments | Retry on day 3, 5 and 7; cancel on day 10 |
| **Q11.2** Cooling-off | UK customers: 14 days; they tick a box agreeing to start now; we store the tick and date |
| **Q12.7** Reserve | 5% of monthly revenue |
| **Q14.1** AI may | Summarize, look up orders (read-only), recommend, draft replies |
| **Q14.2** Needs human | Sending refunds, submitting evidence, locking accounts, anything over $60 |
| **Q14.8** AI checks | 100% reviewed for first 100 customers; 20% after |
| **Q17.1** KPIs | Refund rate under 5%; dispute rate under 0.5%; first reply under 24 hours |

**How the sample plays out (mini story):** A UK student emails on day 10: "I forgot to cancel my trial." The AI looks up the order (read-only), finds the trial ended 3 days ago, checks **Q4.1 row 5** (yes, once, full refund), and checks the customer has no earlier refunds. It writes: "Recommendation: YES. Rule used: Q4.1 row 5." It drafts the reply using the **Q13.1** template. Sam reads it, approves, and sends the refund in Stripe. Sam adds a row to the Refund Log (Appendix F1). The AI notes "first-time trial refund."

---

*End of template. Save a copy of this file for each new project and fill in all `____` blanks.*
