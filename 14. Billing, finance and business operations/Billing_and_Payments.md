# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **Folder:** Billing, Finance and Business Operations / `Billing_and_Payments.md`
> **Template version:** 1.0 | **Covers:** first line of code, through launch, until your first **500 paying customers**
> **Who can fill this in:** anyone. If you can read and type, you can do this. No finance or coding knowledge needed.

## The 7 simple rules

1. **Copy this file** for each new project. Name the copy `Billing_and_Payments_<ProjectName>.md`. Never edit the blank template.
2. **Go top to bottom.** Sections are in the order things happen in real life.
3. **Answer every question.** Write your answer on the line that says `ANSWER:`. Short is fine. One clear sentence beats a long vague one.
4. **Tick boxes** by changing `[ ]` to `[x]`.
5. **Don't know? Never guess and never leave it blank.** Write: `UNKNOWN - ask <name> - by <date>`. Then add it to **Section 15, Open Questions**.
6. **Not relevant to you?** Write `N/A - because <reason>`. A reason is required, so nobody wonders if you forgot.
7. **NEVER paste secrets** (passwords, API keys, full card numbers, bank logins) anywhere in this file. Write where the secret is stored instead, for example `Stored in: company password manager, vault "Payments"`.

## Symbols used in this document

| Symbol | Meaning |
|---|---|
| 🟢 | **Required.** Must be answered for every project. |
| 🟡 | **Only if it applies** to your product. Otherwise write `N/A - because ...`. |
| 🤖 | **AI-agent block.** Copy the text and give it to your AI coding agent after you finish the section above it. |
| ✅ | **Human checkpoint.** A real person must review and approve before moving on. |
| 💡 | **Hint** explaining the question in plain words. |
| `ANSWER:` | Where you type. |

## Examples of good and bad answers

| Question | Bad answer | Good answer |
|---|---|---|
| What do customers pay for? | "Stuff" | "A monthly plan for a photo-editing app. Free plan, Pro plan at $12/month." |
| Who decides refunds? | "Support" | "Support lead (Sam) can approve refunds up to $50. Above $50 needs the finance owner (Priya)." |
| What happens if a card fails? | "We retry" | "Retry on day 1, 3, 5 and 7. Email the customer each time. Cancel access on day 8." |

## Progress tracker (update as you go)

| # | Section | Status (Not started / In progress / Done) | Owner | Date done |
|---|---|---|---|---|
| 0 | Document control | | | |
| 1 | Product basics | | | |
| 2 | Pricing and plans | | | |
| 3 | Customers, countries, currencies, taxes | | | |
| 4 | Payment provider and methods | | | |
| 5 | Billing lifecycle (what happens when) | | | |
| 6 | Marketplace and payouts | | | |
| 7 | How it works inside (technical design) | | | |
| 8 | Security and legal compliance | | | |
| 9 | Finance operations (money, books, reports) | | | |
| 10 | Customer experience (pages, emails, support) | | | |
| 11 | Building with AI agents | | | |
| 12 | Testing and quality checks | | | |
| 13 | Launch readiness (go / no-go) | | | |
| 14 | Road to 500 customers | | | |
| 15 | Open questions, decisions, risks, glossary, sign-off | | | |

**Done means:** every `ANSWER:` has an answer, `UNKNOWN`, or `N/A - because ...`, and every ✅ checkpoint is signed.

---

# SECTION 0: DOCUMENT CONTROL 🟢

| Field | ANSWER |
|---|---|
| Project name | |
| Product one-line description | |
| Document owner (one person, full name) | |
| Backup owner | |
| Finance contact | |
| Engineering contact | |
| Support contact | |
| Legal / compliance contact (or "none yet") | |
| Date started | |
| Target launch date | |
| Current phase | [ ] Idea [ ] Building [ ] Testing [ ] Launched [ ] Growing (first 500) |
| Where is the code? (link) | |
| Where is the project board / task list? (link) | |

**Change log** (add a row every time you change something important)

| Date | Who | What changed | Why |
|---|---|---|---|
| | | | |

---

# SECTION 1: PRODUCT BASICS 🟢

💡 *Billing only makes sense if we first agree on what we are selling and to whom.*

**1.1 What does the product do, in two sentences a 10-year-old would understand?**
ANSWER:

**1.2 Who pays for it?** (tick all that apply)
- [ ] Individual people (consumers)
- [ ] Small businesses
- [ ] Large companies
- [ ] Schools / non-profits
- [ ] Other: ______

**1.3 Who uses it?** Is the payer the same person as the user?
ANSWER:

**1.4 What is the single most important moment where money changes hands?** (Example: "when someone clicks Upgrade to Pro")
ANSWER:

**1.5 What is the goal of billing for the first 500 customers?** (tick the top 2)
- [ ] Learn what people will pay
- [ ] Make money quickly
- [ ] Keep checkout as simple as possible
- [ ] Prove the product to investors
- [ ] Other: ______

**1.6 What is out of scope for now?** (Things billing will NOT do at launch, so nobody builds them by accident. Example: "No invoices in 20 languages.")
ANSWER:

---

# SECTION 2: PRICING AND PLANS 🟢

💡 *Tick every way you make money. Then fill in only the matching parts.*

**2.1 How do you make money?**
- [ ] **Subscription** (customer pays every month or year) → fill 2.3
- [ ] **Usage-based** (customer pays for what they use: credits, tokens, API calls, seats) → fill 2.4
- [ ] **One-time purchase** (customer pays once) → fill 2.5
- [ ] **Marketplace** (money flows between buyers and sellers, and we take a cut) → also fill Section 6
- [ ] **Free plan** (people use it free forever) → fill 2.2

**2.2 Free plan 🟡**

| Question | ANSWER |
|---|---|
| What is included free? | |
| What are the limits? (number of items, days, features) | |
| Is a credit card needed to start free? | [ ] Yes [ ] No |
| What makes a free user become a paying user? | |

**2.3 Subscription plans 🟡**

| Plan name | Price | Billed (monthly / yearly) | What is included | Limits | Free trial days |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

| Question | ANSWER |
|---|---|
| Discount for paying yearly? How much? | |
| Can customers buy more than one seat/user? | |
| Is there a "contact sales" plan? | |
| Do prices differ by country? | |

**2.4 Usage-based pricing 🟡**

| Question | ANSWER |
|---|---|
| What exactly do we count? (credits, API calls, tokens, GB, minutes) | |
| Price per unit | |
| Is there a free allowance each month? | |
| Do unused units expire or roll over? | |
| Pay before using (prepaid credits) or after (bill at month end)? | |
| What happens at the limit? | [ ] Stop service [ ] Allow and charge extra [ ] Ask customer first |
| Spending cap or alert so customers are not surprised? | |
| Where is usage measured and stored? | |

**2.5 One-time purchases 🟡**

| Item | Price | What the customer gets | Refundable? |
|---|---|---|---|
| | | | |

**2.6 Add-ons, coupons and promotions**

| Question | ANSWER |
|---|---|
| Add-ons sold separately? | |
| Coupon / promo codes at launch? Rules? | |
| Early-bird or launch discount for the first 500? | |
| Can discounts be stacked? | [ ] Yes [ ] No |
| Student / non-profit discount? | |

**2.7 Price changes**
How will we change prices later without upsetting existing customers? (Example: "Old customers keep their price for 12 months.")
ANSWER:

✅ **Checkpoint 2:** Pricing approved by (name): ______ Date: ______

---

# SECTION 3: CUSTOMERS, COUNTRIES, CURRENCIES AND TAXES 🟢

💡 *Selling worldwide means different money and different tax rules. Decide now, not after the first angry email.*

**3.1 Where will we sell at launch?**
- [ ] Everywhere we legally can
- [ ] Only these countries: ______
- [ ] Countries we will NOT sell to (sanctions or business reasons): ______

**3.2 Currencies**

| Question | ANSWER |
|---|---|
| Main currency (example: USD) | |
| Other currencies shown to customers | |
| Do we show prices in local currency, or convert at checkout? | |
| Who pays currency-conversion fees? | |
| Currency we keep our books in | |

**3.3 Taxes** (VAT, GST, sales tax)

| Question | ANSWER |
|---|---|
| Where is our business legally registered? | |
| Are we registered for tax anywhere? Where? | |
| Who collects and pays sales tax / VAT / GST? | [ ] Our payment provider (automatic tax tool) [ ] A merchant of record [ ] We do it ourselves [ ] Not decided |
| Are prices shown **with** or **without** tax? | |
| How do we handle business customers with a tax ID (B2B)? | |
| Who is the tax advisor / accountant? | |

**3.4 Customer details we must collect at checkout**
- [ ] Name
- [ ] Email
- [ ] Billing address
- [ ] Country
- [ ] Company name
- [ ] Tax ID / VAT number
- [ ] Other: ______

**3.5 Customer types**

| Type | Allowed? | Special rules |
|---|---|---|
| Individuals | | |
| Businesses | | |
| Under-18s | [ ] Yes [ ] No | |
| Customers in restricted countries | [ ] Yes [ ] No | |

✅ **Checkpoint 3:** Tax setup reviewed by a qualified accountant or tax advisor. Name: ______ Date: ______

---

# SECTION 4: PAYMENT PROVIDER AND PAYMENT METHODS 🟢

💡 *The payment provider is the company that safely takes the card and moves the money. Examples: Stripe, Adyen, PayPal, Braintree, Razorpay. Default assumption in this template: a Stripe-style provider where we are responsible for tax and compliance.*

**4.1 Provider**

| Question | ANSWER |
|---|---|
| Provider chosen | |
| Why this one? (fees, countries, features) | |
| Backup provider if it goes down or freezes our account | |
| Provider account owner (a person, not a shared mailbox) | |
| Is the provider account verified/approved for live payments? | [ ] Yes [ ] No [ ] Waiting |
| Where are the provider keys stored? (location only, never the keys) | |
| Test account and live account are separate? | [ ] Yes [ ] No |

**4.2 Fees**

| Fee type | Amount | Who pays |
|---|---|---|
| Per transaction | | |
| Monthly | | |
| Currency conversion | | |
| Refund fee | | |
| Chargeback (dispute) fee | | |
| Payout fee | | |

**4.3 Payment methods at launch**
- [ ] Credit / debit cards
- [ ] Apple Pay / Google Pay
- [ ] PayPal
- [ ] Bank debit (ACH, SEPA)
- [ ] Bank transfer / invoice (pay later)
- [ ] Local methods (UPI, iDEAL, etc.): ______
- [ ] Buy now pay later
- [ ] Crypto
- [ ] Other: ______

**4.4 Checkout style**
- [ ] Provider-hosted page (safest, easiest)
- [ ] Embedded form inside our app
- [ ] In-app purchases (Apple App Store / Google Play) → note: stores take their own cut and have their own rules. Explain: ______

**4.5 Payout (when money reaches our bank)**

| Question | ANSWER |
|---|---|
| How often are we paid out? | |
| Which bank account? (name only, no numbers) | |
| Do we keep a reserve or hold-back? | |

---

# SECTION 5: BILLING LIFECYCLE, WHAT HAPPENS WHEN 🟢

💡 *This is the heart of the document. For every situation, say what the customer sees, what the system does, and who handles problems.*

**5.1 Sign-up and first payment**

| Question | ANSWER |
|---|---|
| Steps from "Buy" to "Access granted" (list 1, 2, 3...) | |
| How fast must access start after payment? | |
| What if payment succeeds but access is not given? | |
| Free trial: when do we ask for a card? What happens at trial end? | |
| Do we send a reminder before the trial ends? When? | |

**5.2 Renewals (subscriptions) 🟡**

| Question | ANSWER |
|---|---|
| Renewal date rule (same day each month? What about the 31st?) | |
| Reminder email before renewal? When? | |
| Do we auto-renew? How do customers agree? | |

**5.3 Upgrades, downgrades and plan changes 🟡**

| Question | ANSWER |
|---|---|
| Upgrade: pay the difference now (proration) or at next renewal? | |
| Downgrade: effective now or at period end? | |
| Seat added or removed mid-month? | |
| Switching monthly ↔ yearly? | |

**5.4 Failed payments (when a card does not work)**

| Day | What the system does | What the customer is told | Access status |
|---|---|---|---|
| Day 0 (first failure) | | | |
| Day 1-3 | | | |
| Day 5-7 | | | |
| Final | | | |

Other questions:
- Do we automatically retry? How many times?
- Do we ask customers to update their card? Where do they do it?
- After how many days do we cancel? ANSWER:

**5.5 Cancellations**

| Question | ANSWER |
|---|---|
| Where does the customer cancel? | |
| Cancel immediately or at end of paid period? | |
| What happens to their data? How long do we keep it? | |
| Do we ask why they left? | |
| Can they come back? How? | |

**5.6 Refunds and credits**

| Question | ANSWER |
|---|---|
| Refund policy in plain words | |
| Refund window (days) | |
| Full or partial refunds? | |
| Who can approve? Up to what amount? | |
| Where is the refund made? (provider dashboard, our admin tool) | |
| How long until the customer gets the money? | |
| Do we give credit instead of cash in some cases? | |
| What happens to the customer's access after refund? | |

**5.7 Chargebacks (customer disputes the charge with their bank)**

| Question | ANSWER |
|---|---|
| Who watches for disputes? | |
| Deadline to respond (usually only a few days; check the provider) | |
| What proof do we keep? (logins, delivery proof, emails) | |
| At what chargeback rate do we raise an alarm? | |

**5.8 Invoices and receipts**

| Question | ANSWER |
|---|---|
| Receipt after every payment? | [ ] Yes [ ] No |
| Formal invoice with tax details? | [ ] Yes [ ] No |
| Invoice number format (example: INV-2026-000001) | |
| Can customers download past invoices? Where? | |
| Can customers add company name / tax ID later? | |
| Who fixes a wrong invoice? | |

**5.9 Special cases** (write what happens, or `N/A`)

| Situation | What happens |
|---|---|
| Customer pays twice by mistake | |
| Customer changes email | |
| Customer changes country | |
| Card expires | |
| Customer account deleted while subscription is active | |
| Suspected fraud | |
| Customer cannot afford it, asks for a discount | |
| Pricing mistake discovered after sales | |

✅ **Checkpoint 5:** Someone who did NOT write this section has read it and says every situation is clear. Name: ______ Date: ______

---

# SECTION 6: MARKETPLACE AND PAYOUTS 🟡

💡 *Only fill this if buyers pay sellers through your product. Otherwise write `N/A - not a marketplace` here and skip to Section 7.*

| Question | ANSWER |
|---|---|
| Who are the sellers? Who are the buyers? | |
| What is our cut (commission / platform fee)? | |
| Who pays the provider's fees? | |
| How are sellers verified (identity, KYC)? | |
| How do sellers get paid? (provider's connect/split-payment feature, manual) | |
| Payout schedule (instant, weekly, after delivery) | |
| Do we hold money until the order is delivered (escrow-style)? | |
| Minimum payout amount | |
| What if the buyer asks for a refund after the seller was paid? | |
| Who is responsible for seller taxes and forms? | |
| What if a seller breaks the rules? | |
| Seller support contact | |
| Are we legally allowed to hold or move other people's money in our country? Who confirmed? | |

✅ **Checkpoint 6:** Legal review of marketplace money flow. Name: ______ Date: ______

---

# SECTION 7: HOW IT WORKS INSIDE (TECHNICAL DESIGN) 🟢

💡 *Fill with the engineering contact. If you are not technical, ask them the question and write down their answer.*

**7.1 Technology**

| Question | ANSWER |
|---|---|
| Programming language / framework | |
| Database | |
| Where does the app run (hosting)? | |
| Do we use the provider's ready-made subscription / billing tool, or build our own? | |

**7.2 The money story in a simple diagram.** Fill the boxes or paste a picture link.

```
Customer → Checkout → Payment Provider → Our App (is told "paid") → Access given
                                      ↓
                             Receipt email + Invoice + Accounting record
```
Differences from our real design:
ANSWER:

**7.3 What we store about billing**

| Data | Stored by us? | Where | How long |
|---|---|---|---|
| Customer ID from provider | | | |
| Subscription status | | | |
| Plan name / price | | | |
| Invoices | | | |
| Usage counts | | | |
| Last 4 digits of card (OK) | | | |
| Full card numbers | **MUST BE NO. Never store.** | | |

**7.4 Notifications from the provider (webhooks)** 💡 *The provider tells our app "payment succeeded" or "payment failed" by sending a message.*

| Event we must handle | Handled? | What our system does |
|---|---|---|
| Payment succeeded | [ ] | |
| Payment failed | [ ] | |
| Subscription created | [ ] | |
| Subscription changed | [ ] | |
| Subscription cancelled | [ ] | |
| Refund issued | [ ] | |
| Dispute opened | [ ] | |
| Invoice created / paid | [ ] | |
| Payout paid / failed | [ ] | |

Safety questions:
- Do we check the message is really from the provider (signature check)? ANSWER:
- If the same message arrives twice, do we avoid doing things twice (idempotency)? ANSWER:
- If our app was down and missed a message, how do we catch up? ANSWER:

**7.5 Access control** (who gets what)

| Question | ANSWER |
|---|---|
| How does the app know what a customer paid for? | |
| How fast does access change after payment/cancellation? | |
| What if the provider is down? Do paying customers keep access? | |

**7.6 Usage tracking 🟡**

| Question | ANSWER |
|---|---|
| How is each usage event recorded? | |
| Can usage be double-counted or lost? How do we prevent that? | |
| How do customers see their usage? | |
| How are usage disputes resolved? | |

**7.7 Admin tool**
What can our team do without a developer? (tick)
- [ ] Look up a customer's payments
- [ ] Issue a refund
- [ ] Give a free month / credit
- [ ] Change a plan
- [ ] Cancel a subscription
- [ ] Resend an invoice
- [ ] Leave notes on an account
- [ ] See an audit log of who did what

**7.8 Environments**

| Environment | Uses test money? | URL / name |
|---|---|---|
| Development | [ ] | |
| Testing / staging | [ ] | |
| Live (production) | Real money | |

✅ **Checkpoint 7:** Technical design reviewed by someone other than the builder. Name: ______ Date: ______

---

# SECTION 8: SECURITY AND LEGAL COMPLIANCE 🟢

💡 *Mistakes here cost real money and trust. If unsure, write `UNKNOWN` and get expert help.*

**8.1 Card data safety (PCI)**

| Question | ANSWER |
|---|---|
| Do card numbers ever touch our servers? (Best answer: No, only the provider handles them.) | |
| Which PCI self-assessment form applies? (Ask your provider; hosted checkout is usually the simplest.) | |
| Who completes and renews it each year? | |

**8.2 Security checklist**
- [ ] Provider keys are kept in a secrets manager, not in code
- [ ] Different keys for test and live
- [ ] Keys can be replaced quickly if leaked (who and how: ______)
- [ ] Two-factor login on provider, bank and accounting accounts
- [ ] Only the people who need billing access have it
- [ ] Billing actions are logged (who, what, when)
- [ ] Webhooks are verified
- [ ] Customers can only see their own invoices
- [ ] Logs never contain card numbers or secret keys
- [ ] Rate limits on checkout to stop card-testing attacks
- [ ] Fraud tools turned on at the provider

**8.3 Privacy**

| Question | ANSWER |
|---|---|
| Which privacy laws apply? (GDPR, CCPA, etc.) | |
| Privacy policy mentions payments and payment providers? | [ ] Yes [ ] No |
| How long do we keep billing records? (tax law often requires several years) | |
| How does a customer ask us to delete their data? What must we keep by law? | |

**8.4 Legal documents**
- [ ] Terms of Service (includes billing, renewal and cancellation terms)
- [ ] Refund policy page
- [ ] Privacy policy
- [ ] Clear price and renewal info shown BEFORE payment
- [ ] Automatic-renewal consent wording (needed in many places)
- [ ] Reviewed by a lawyer? Name: ______ Date: ______

**8.5 Other rules to check**

| Rule | Applies? | Handled by |
|---|---|---|
| Strong customer authentication (SCA / 3-D Secure, e.g. in Europe) | | |
| Anti-money-laundering / identity checks (marketplaces) | | |
| Sanctions screening | | |
| Consumer cancellation rights ("cooling-off" periods) | | |
| Subscription cancellation laws (easy cancel, e.g. US/EU rules) | | |
| Money-transmitter licensing (marketplaces) | | |
| Accessibility of the checkout | | |

✅ **Checkpoint 8:** Security and compliance reviewed. Name: ______ Date: ______

---

# SECTION 9: FINANCE OPERATIONS (MONEY, BOOKS, REPORTS) 🟢

**9.1 Accounting**

| Question | ANSWER |
|---|---|
| Accounting software | |
| Accountant / bookkeeper | |
| How do payments reach accounting? (manual, automatic sync) | |
| Who records provider fees? | |
| Who records refunds, chargebacks and taxes? | |
| How is subscription money counted as revenue? (e.g., yearly payment spread over 12 months; confirm with accountant) | |

**9.2 Reconciliation** 💡 *Checking that the provider, our app, our bank and our books all show the same money.*

| Question | ANSWER |
|---|---|
| How often do we check? | [ ] Daily [ ] Weekly [ ] Monthly |
| Who does it? | |
| What do we compare? | |
| What if numbers do not match? Who investigates? How fast? | |

**9.3 Month-end routine**
- [ ] Download provider reports
- [ ] Reconcile payouts to bank
- [ ] Review refunds and disputes
- [ ] Review failed-payment backlog
- [ ] File / prepare tax returns
- [ ] Review revenue numbers with the owner

**9.4 Reports we need to see**

| Report | How often | Who reads it |
|---|---|---|
| Revenue (MRR/ARR, new, lost, upgrades) | | |
| Refunds and disputes | | |
| Failed payments and recovered payments | | |
| Taxes collected | | |
| Payouts | | |
| Usage vs. revenue | | |
| Customers by plan / country | | |

**9.5 Money limits and approvals**

| Action | Who can do it | Needs second approval above |
|---|---|---|
| Refund | | |
| Credit / free months | | |
| Price change | | |
| Manual invoice | | |
| Payout change | | |

---

# SECTION 10: CUSTOMER EXPERIENCE (PAGES, EMAILS, SUPPORT) 🟢

**10.1 Pages**
- [ ] Pricing page
- [ ] Checkout page
- [ ] Payment success page
- [ ] Payment failed page
- [ ] "My account / Billing" page (see plan, card, invoices, cancel)
- [ ] Update-card page
- [ ] Cancellation page
- [ ] Refund policy page
- [ ] Receipt / invoice download

**10.2 Emails and messages**

| Message | Sent when | Sent by | Written? |
|---|---|---|---|
| Welcome / payment receipt | | | [ ] |
| Trial ending soon | | | [ ] |
| Upcoming renewal | | | [ ] |
| Payment failed | | | [ ] |
| Final warning before cancel | | | [ ] |
| Cancellation confirmed | | | [ ] |
| Refund confirmed | | | [ ] |
| Plan changed | | | [ ] |
| Usage limit warning | | | [ ] |
| Price change notice | | | [ ] |

Tone of messages (friendly, formal, short, etc.): ______

**10.3 Support**

| Question | ANSWER |
|---|---|
| Where do billing questions go? (email, chat, form) | |
| Reply time promised | |
| Top 10 billing questions and ready answers | (add a link or list) |
| What can support do alone? What must be escalated? | |
| Who is on call for payment emergencies? | |

---

# SECTION 11: BUILDING WITH AI AGENTS 🟢

💡 *In AI-driven development, an AI agent writes much of the code and documents. Agents are fast but can be confidently wrong, so billing code (money!) needs extra human checks.*

**11.1 Ground rules (tick to confirm)**
- [ ] An AI agent never gets live provider keys. Only test keys.
- [ ] An AI agent never moves real money or issues real refunds on its own.
- [ ] Every billing change made by an agent is reviewed by a human before it goes live.
- [ ] Agents work from THIS document. If the document is unclear, they must ask, not guess.
- [ ] Every agent task has tests that must pass.
- [ ] All agent work is saved in version control with clear messages.

**11.2 Which agents and tools do we use?**

| Job | Tool / agent | Human reviewer |
|---|---|---|
| Writing code | | |
| Writing tests | | |
| Reviewing code | | |
| Writing emails and policy pages | | |
| Checking security | | |

**11.3 Prompts to give your AI agent** (copy and use; replace words in `<angle brackets>`)

🤖 **Step A: Understand**
```
Read Billing_and_Payments_<ProjectName>.md fully. List (1) what you understood,
(2) every UNKNOWN or blank answer, (3) any contradictions, (4) questions you
need answered before writing code. Do not write code yet.
```

🤖 **Step B: Plan**
```
Using Sections 2-9 of the document, write a step-by-step build plan for billing:
database tables, webhook handlers, checkout flow, billing page, emails, admin tool,
tests. Mark which steps touch money. Stop and wait for my approval.
```

🤖 **Step C: Build (small pieces)**
```
Build ONLY: <one piece, e.g. "webhook handler for payment failed">.
Follow Section 5 and Section 7 exactly. Use test keys and test mode only.
Never store card numbers. Make it safe to run twice with the same event.
Write tests, run them, and show me the results.
```

🤖 **Step D: Review**
```
Review the billing code against Sections 5, 7, 8 and 12. Look for: double charges,
missed webhooks, wrong tax, wrong proration, access given without payment, access
removed after payment, leaked secrets, missing logs. List problems by severity.
```

🤖 **Step E: Test**
```
Run every test case in Section 12. Report pass/fail. For each fail, explain the cause
and propose a fix. Do not change the tests to make them pass.
```

🤖 **Step F: Launch check**
```
Go through the checklist in Section 13. For each item, say Ready / Not ready and
show the evidence. Do not mark anything Ready without evidence.
```

**11.4 What the agent must NEVER do** (add your own)
- Guess a price, tax rate, refund rule, or legal text that is not in this document
- Use live keys
- Skip failing tests
- Delete billing records
- ______

**11.5 Human review log**

| Date | What the agent built | Reviewer | Result (OK / fix needed) |
|---|---|---|---|
| | | | |

---

# SECTION 12: TESTING AND QUALITY CHECKS 🟢

💡 *Run these in test mode with fake money first. Mark each as Pass, Fail or N/A. Use your provider's test cards (found in the provider's test docs).*

| # | Test | Expected result | Pass / Fail | Tester | Date |
|---|---|---|---|---|---|
| 1 | Buy a plan with a working test card | Access starts, receipt sent | | | |
| 2 | Buy with a card that is declined | Clear error, no access, nothing charged | | | |
| 3 | Buy with a card needing extra authentication (3-D Secure) | Customer can complete it | | | |
| 4 | Start free trial, let it end | Charged or downgraded as designed | | | |
| 5 | Renew a subscription | Charged once, invoice created | | | |
| 6 | Renewal payment fails | Retries, emails, access rules from 5.4 | | | |
| 7 | Customer updates card after failure | Payment recovers, access returns | | | |
| 8 | Upgrade mid-month | Correct proration | | | |
| 9 | Downgrade mid-month | Correct behavior from 5.3 | | | |
| 10 | Cancel subscription | Ends as designed, confirmation sent | | | |
| 11 | Full refund | Money returned, access follows policy | | | |
| 12 | Partial refund | Correct amount | | | |
| 13 | Dispute / chargeback test | Alert reaches the owner | | | |
| 14 | Same webhook sent twice | Only processed once | | | |
| 15 | Webhook arrives late or out of order | System ends in the right state | | | |
| 16 | App down during a payment | System catches up after restart | | | |
| 17 | Tax for 3 different countries | Correct tax each time | | | |
| 18 | Business customer with tax ID | Handled as designed | | | |
| 19 | Currency other than main | Correct amount and invoice | | | |
| 20 | Coupon code (valid, expired, stacked) | Works per 2.6 | | | |
| 21 | Usage billing: normal, over limit, zero use 🟡 | Correct charges | | | |
| 22 | Marketplace payout, success and failure 🟡 | Correct split and payout | | | |
| 23 | Customer sees only their own invoices | No access to others' | | | |
| 24 | Invoice download | Correct details and numbering | | | |
| 25 | All emails in 10.2 | Correct text, links work | | | |
| 26 | Admin tool: refund, credit, plan change | Works and is logged | | | |
| 27 | Mobile checkout | Easy and works | | | |
| 28 | Slow internet / double-click on Pay | No double charge | | | |
| 29 | Secrets search in code and logs | None found | | | |
| 30 | Switch to live mode with a tiny real payment, then refund it | Everything matches | | | |

**Bugs found**

| # | Description | Severity (blocker / high / low) | Owner | Fixed? |
|---|---|---|---|---|
| | | | | |

✅ **Checkpoint 12:** All blocker and high bugs fixed. QA signed by: ______ Date: ______

---

# SECTION 13: LAUNCH READINESS (GO / NO-GO) 🟢

💡 *Tick only with proof. "I think so" is not a tick.*

**Money and provider**
- [ ] Live provider account approved
- [ ] Live keys stored safely
- [ ] Bank account connected and payout tested
- [ ] Tax settings confirmed live
- [ ] Prices in live mode match Section 2

**Product and technical**
- [ ] Section 12 tests passed
- [ ] Live webhooks connected and tested
- [ ] Monitoring and alerts on (failed payments, webhook errors, spikes)
- [ ] Backups working
- [ ] Rollback plan written: ______

**Legal and people**
- [ ] Terms, privacy and refund pages live
- [ ] Renewal and cancellation info shown before payment
- [ ] Support trained and has answers ready
- [ ] On-call person named for launch week
- [ ] Finance knows how to reconcile

**Day-one plan**

| Question | ANSWER |
|---|---|
| Launch date and time | |
| Who watches payments in the first 24 hours? | |
| Who can say "stop, pause sales"? | |
| How do we pause billing quickly? | |
| Who talks to customers if something breaks? | |

**GO / NO-GO decision**
- [ ] GO [ ] NO-GO Decided by: ______ Date: ______ Reason: ______

---

# SECTION 14: ROAD TO 500 CUSTOMERS 🟢

💡 *Watch billing closely while the numbers are small. Every customer matters and every problem is easy to find.*

**14.1 Milestones**

| Milestone | Target date | What to check | Done |
|---|---|---|---|
| First paying customer | | Payment, receipt, access, bank payout all correct. Check by hand. | [ ] |
| 10 customers | | First renewals or failed payments seen; support questions reviewed | [ ] |
| 50 customers | | Refund rate, failed-payment recovery, tax handled for each country | [ ] |
| 100 customers | | Reconciliation matches. Review pricing and plans. | [ ] |
| 250 customers | | Cost of fees, automation of manual tasks, fraud patterns | [ ] |
| 500 customers | | Full review: what to keep, change, or automate next | [ ] |

**14.2 Numbers to track** (write the target and how it is measured)

| Metric | Target | Where to see it | Checked how often |
|---|---|---|---|
| Paying customers (goal: 500) | 500 | | |
| Monthly recurring revenue | | | |
| Checkout completion rate | | | |
| Failed-payment rate | | | |
| Failed payments recovered | | | |
| Refund rate | | | |
| Chargeback rate | | | |
| Average revenue per customer | | | |
| Customer cancel rate (churn) | | | |
| Support tickets about billing | | | |
| Payment fees as a % of revenue | | | |
| Days to resolve a billing problem | | | |

**14.3 Weekly check (10 minutes)**
- [ ] Any payments stuck or failed?
- [ ] Any disputes opened?
- [ ] Any angry billing emails?
- [ ] Do provider total, app total and bank total agree?
- [ ] Any unusual spikes (many small charges = possible card-testing fraud)?
- [ ] Anything customers keep asking that the page should answer?

Owner of the weekly check: ______

**14.4 When to automate more**
Write the rule. Example: "If we do the same manual refund task more than 10 times a week, we build a button for it."
ANSWER:

**14.5 What we learn at 500** (fill in at the end)
- What worked:
- What hurt:
- Changes to this template:

---

# SECTION 15: OPEN QUESTIONS, DECISIONS, RISKS, GLOSSARY AND SIGN-OFF

**15.1 Open questions** (every `UNKNOWN` goes here)

| # | Question | Who can answer | Needed by | Answer | Status |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |

**15.2 Decision log** (write down WHY big choices were made)

| Date | Decision | Why | Decided by |
|---|---|---|---|
| | | | |

**15.3 Risks**

| Risk | How likely (L/M/H) | How bad (L/M/H) | What we do about it | Owner |
|---|---|---|---|---|
| Provider freezes our account | | | | |
| Wrong tax charged | | | | |
| Double charges | | | | |
| Fraud / card testing | | | | |
| Too many chargebacks | | | | |
| Webhook outage | | | | |
| AI-written bug in billing code | | | | |
| Price set wrong | | | | |
| Key person unavailable | | | | |
| Law or tax rule changes | | | | |

**15.4 Incident plan (something goes wrong with money)**

| Step | ANSWER |
|---|---|
| Who is told first? | |
| How do we stop more damage (pause checkout, turn off renewals)? | |
| How do we find who was affected? | |
| How do we fix and refund? | |
| How do we tell customers? | |
| How do we write down what we learned? | |

**15.5 Glossary** (plain words)

| Word | Meaning |
|---|---|
| Billing | Working out what a customer owes |
| Payment | The actual moving of money |
| Payment provider | The company that safely handles cards and moves money (e.g., Stripe) |
| Subscription | A plan the customer pays for again and again |
| Proration | Charging only for part of a billing period after a mid-period change |
| Invoice | A formal bill |
| Receipt | Proof that a payment happened |
| Refund | Giving money back |
| Chargeback / dispute | The customer asks their bank to take the money back |
| Webhook | A message the provider sends our app about something that happened |
| Idempotency | Doing the same request twice has the same result as doing it once |
| Dunning | The process of reminding and retrying after a payment fails |
| Churn | Customers leaving |
| MRR / ARR | Money coming in every month / year from subscriptions |
| Reconciliation | Checking that all records of money agree |
| PCI | Rules for keeping card data safe |
| SCA / 3-D Secure | Extra identity check on card payments, required in some regions |
| KYC | "Know Your Customer," identity checks |
| Merchant of Record | A company that legally sells for you and handles tax |
| Payout | Money sent from the provider to our bank (or from us to sellers) |
| Test mode | Fake-money mode for safe practice |

**15.6 Final sign-off**

| Role | Name | I confirm this document is complete and correct | Date |
|---|---|---|---|
| Document owner | | [ ] | |
| Engineering | | [ ] | |
| Finance | | [ ] | |
| Legal / compliance | | [ ] | |
| QA | | [ ] | |
| Support | | [ ] | |

---

# AI-AGENT SUMMARY (fill LAST; agents read this first)

```yaml
project: ""
launch_date: ""
business_model: []            # subscription | usage | one_time | marketplace | free
payment_provider: ""
live_countries: []
main_currency: ""
tax_handling: ""              # provider_auto | merchant_of_record | self | undecided
payment_methods: []
plans:
  - name: ""
    price: ""
    interval: ""
trial_days: 0
refund_window_days: 0
failed_payment_retry_days: []
cancel_behavior: ""           # immediate | end_of_period
webhooks_required: []
manual_approval_needed_for: []
agent_must_not: ["use live keys", "guess prices or tax", "store card numbers"]
unknown_items_count: 0
go_no_go: ""
```

*End of template. Remember: no guessing. Write the answer, write UNKNOWN, or write N/A with a reason.*
