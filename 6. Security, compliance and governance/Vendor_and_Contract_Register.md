# HOW TO FILL IN THIS DOCUMENT (READ THIS FIRST)

> **Version of this template:** 1.0  |  **Template owner:** [NAME]  |  **Last template update:** [DATE]
> **Lives in folder:** `Security, compliance and governance/`
> **Covers:** AI-driven product development, from the first idea to the day your **500th customer** is using the product.

---

## 1. What is this document?

A **vendor** is any outside company, tool, or person your project depends on (for example: an AI model provider, a cloud host, an email tool, a payment service, a freelancer, a law firm).

A **contract** is any agreement with that vendor: a signed paper, a click-to-accept "Terms of Service", a free-plan agreement, an invoice, or an email promise.

This document is your project's **one place** to answer, for every vendor:

1. **Who** are they, and **why** do we use them?
2. **What** of ours do they touch (code, customer data, money, AI prompts)?
3. **What** did we agree to (price, dates, rules, how to leave)?
4. **How risky** are they (Green / Yellow / Red)?
5. **What do we do** when it ends or goes wrong?

If someone new joins the project, or an AI agent picks it up, they should understand your vendors in 15 minutes **without asking anyone**.

## 2. Who fills it in, and when?

| Person | What they do |
|---|---|
| **Register Owner** (one named person) | Keeps the file complete and correct. Runs the reviews in Part 6. |
| **Anyone who adds a new tool or vendor** | Adds a Vendor Card (Part 2) **before** they start using it with real data. |
| **Budget holder** | Confirms the money answers. |
| **Legal / security helper** (or a trusted advisor, if you have one) | Checks the red-flag questions and the legal answers. |

**Fill it in at these moments:**

- **Day 1** of the project: fill Part 0, then add every vendor you already know about.
- **Every time** you add, change, or remove a vendor: update the same day.
- **Before each lifecycle gate** (Part 5): do the gate checklist.
- **Every 3 months**: do the review in Part 6.

## 3. How to reuse this file across many projects

1. **Copy** this file. Rename it: `Vendor_and_Contract_Register_[PROJECT-NAME].md`.
2. **Never edit the blank master.** Only edit your copy.
3. Fill in **Part 0** first.
4. Delete the example in Part 8 from your copy only when you no longer need it (or keep it at the bottom, clearly marked as an example).
5. Copy the **Vendor Card** (Part 2) once per vendor. Copy the **Contract Card** (Part 3) once per contract.

## 4. The 8 golden rules (a 10-year-old can follow these)

1. **Never leave a blank.** If you do not know, write `UNKNOWN - [name of person] will find out by [date]`.
2. **If a question does not apply, write `N/A - [one-line reason]`.** Do not just write "N/A".
3. **Use plain words.** Short sentences. No guessing, no "probably". Write what you know and say how you know it.
4. **Use real dates** in this format: `YYYY-MM-DD` (example: `2026-11-30`).
5. **Use real money amounts with the currency** (example: `USD 49 per month`, not "cheap").
6. **NEVER paste secrets here.** No passwords, API keys, tokens, card numbers, or customer data. Write where the secret is stored instead (example: "stored in our password manager, vault: Engineering").
7. **Link to proof.** When you say "we signed a DPA", add a link or file path to the signed document.
8. **One vendor = one ID.** Use `V-001`, `V-002`... for vendors and `C-001`, `C-002`... for contracts. Never reuse an ID, even if a vendor is removed.

## 5. How to answer the questions

Every question in this document has one of these answer types. The type is written in brackets.

| Bracket | How to answer | Example |
|---|---|---|
| `[Text]` | One or two short sentences | "We use it to send login emails." |
| `[Date]` | `YYYY-MM-DD` | `2026-12-01` |
| `[Money]` | Amount + currency + how often | `USD 200 per month` |
| `[Pick one]` | Circle or keep only one option (delete the others) | `Yes` |
| `[Pick many]` | Keep all that apply | `Customer emails, Names` |
| `[Link]` | Paste a web link or file path | `/contracts/acme-dpa.pdf` |
| `[Person]` | Full name + role | `Sam Lee, Founder` |

**Do not delete questions.** Answer them or mark them `N/A - reason`.

## 6. The traffic-light colors (what they mean)

| Color | Meaning | What you must do |
|---|---|---|
| 🟢 **GREEN** | Low risk. Safe to use. | Review every 12 months. |
| 🟡 **YELLOW** | Some risk. Usable with care. | Write a "reduce risk" action. Review every 6 months. |
| 🔴 **RED** | High risk. | **Do not use with real customer data** until a named person approves in writing. Review every 3 months. |

The scoring questions are in **Part 4**. You do not need to guess the color. The answers decide it.

## 7. Status words (use only these)

| Field | Allowed words |
|---|---|
| **Vendor status** | `Considering`, `Approved`, `In use`, `Paused`, `Being replaced`, `Removed` |
| **Contract status** | `Draft`, `Signed`, `Active`, `Expiring soon` (within 90 days), `Expired`, `Terminated` |
| **Lifecycle stage** | `1-Plan`, `2-Build`, `3-Launch`, `4-Grow to 500` |

## 8. The 4 lifecycle stages (where this fits in your product journey)

| Stage | What is happening | Typical vendors | Main question |
|---|---|---|---|
| **1-Plan** | Deciding what to build and how | Research tools, AI assistants, design tools, advisors | "Is it OK to try this tool, and what are we allowed to put in it?" |
| **2-Build** | AI-assisted coding, testing, staging | AI model APIs, coding agents, code hosting, CI/CD, test services | "Does our code or data leak to the vendor or train their AI?" |
| **3-Launch** | Going live to the public | Production cloud, domain, payments, email, monitoring, support | "Can this vendor handle real customers safely?" |
| **4-Grow to 500** | First customers use it | Same vendors at higher usage, plus analytics, billing, helpdesk | "What happens to cost, limits, and risk as customers grow?" |

A vendor can belong to more than one stage. Tag **all** that apply.

## 9. Which rules might apply to you? (quick helper)

Tick the ones that apply in **Part 0**. If unsure, tick "Not sure" and ask your legal or security helper. These are *prompts to think*, not legal advice.

| Rule or standard | Plain-words meaning | Triggered when... |
|---|---|---|
| **GDPR / privacy laws** | Rules for protecting personal data of people in the EU/UK (and similar laws elsewhere) | You have customers in those places, or any vendor stores personal data |
| **SOC 2 / ISO 27001** | Independent "security report cards" a vendor can show you | A vendor handles your customer data or runs critical systems |
| **EU AI Act / AI governance** | Rules about how AI is used and how risky that use is | Your product uses AI that affects people, or you use AI vendors in the EU |
| **PCI DSS** | Rules for handling card payments | You take card payments (best practice: let a payment vendor handle all card data) |
| **HIPAA** | Rules for US health information | Your product touches US health data |

---

# PART 0 - PROJECT COVER SHEET

*Fill this once per project. Everything else depends on it.*

| # | Question | Your answer |
|---|---|---|
| 0.1 | Project name `[Text]` | |
| 0.2 | One-sentence description of what the product does `[Text]` | |
| 0.3 | Register Owner `[Person]` | |
| 0.4 | Backup owner (if the owner is away) `[Person]` | |
| 0.5 | Project start date `[Date]` | |
| 0.6 | Planned launch date `[Date]` | |
| 0.7 | Current lifecycle stage `[Pick one]` | `1-Plan` / `2-Build` / `3-Launch` / `4-Grow to 500` |
| 0.8 | Current number of customers `[Text]` | |
| 0.9 | Where do your customers live? (countries or regions) `[Text]` | |
| 0.10 | What kind of customer data do you collect? `[Pick many]` | `None`, `Names`, `Emails`, `Passwords/logins`, `Payment info`, `Health info`, `Files/uploads`, `Chats/prompts`, `Location`, `Other: ___` |
| 0.11 | Does the product itself use AI to make decisions or content that customers see? `[Pick one]` | `Yes` / `No` / `Planned` |
| 0.12 | Which rules apply? (see section 9) `[Pick many]` | `GDPR/privacy`, `SOC 2/ISO 27001`, `EU AI Act`, `PCI DSS`, `HIPAA`, `None`, `Not sure` |
| 0.13 | Total monthly vendor budget `[Money]` | |
| 0.14 | Who may approve a 🔴 RED vendor? `[Person]` | |
| 0.15 | Where are signed contracts stored? `[Link]` | |
| 0.16 | Where are passwords/keys stored? (location only, never the secrets) `[Text]` | |
| 0.17 | Date this register was last fully reviewed `[Date]` | |

---

# PART 1 - MASTER SUMMARY TABLE

*One row per vendor. This is your "dashboard". Update it **after** you finish each Vendor Card. Keep it in sync.*

| Vendor ID | Vendor name | What we use it for (5 words max) | Type | Stage(s) | Vendor status | Touches customer data? | Risk color | Contract ID(s) | Monthly cost | Next renewal / end date | Owner |
|---|---|---|---|---|---|---|---|---|---|---|---|
| V-001 | | | | | | Yes / No | 🟢 🟡 🔴 | C-001 | | | |
| V-002 | | | | | | | | | | | |
| V-003 | | | | | | | | | | | |

**Type options:** `AI model/API`, `Cloud/hosting/DevOps`, `SaaS/business tool`, `People/services`, `Other`.

**Quick totals (update each review):**

| Measure | Value |
|---|---|
| Total vendors in use | |
| 🟢 Green / 🟡 Yellow / 🔴 Red | / / |
| Total monthly spend | |
| Contracts ending in the next 90 days | |
| Vendors with UNKNOWN answers still open | |

---

# PART 2 - VENDOR CARDS (QUESTIONNAIRE)

*Copy the whole card below once for each vendor. Name it by ID. Answer every question.*

## VENDOR CARD: V-___ : [Vendor name]

### Section A - Basics

| # | Question | Your answer |
|---|---|---|
| A1 | Vendor ID `[Text]` | V-___ |
| A2 | Vendor name (legal name if known) `[Text]` | |
| A3 | Website `[Link]` | |
| A4 | Vendor type `[Pick one]` | `AI model/API` / `Cloud/hosting/DevOps` / `SaaS/business tool` / `People/services` / `Other` |
| A5 | In plain words: what do we use them for? `[Text]` | |
| A6 | Why did we choose them instead of others? `[Text]` | |
| A7 | What would we use if they disappeared tomorrow? (backup option) `[Text]` | |
| A8 | Lifecycle stage(s) `[Pick many]` | `1-Plan`, `2-Build`, `3-Launch`, `4-Grow to 500` |
| A9 | Vendor status `[Pick one]` | `Considering`, `Approved`, `In use`, `Paused`, `Being replaced`, `Removed` |
| A10 | Our internal owner for this vendor `[Person]` | |
| A11 | Vendor contact for support or sales `[Text]` | Name, email or support link |
| A12 | Date we started using them `[Date]` | |
| A13 | Who approved using them? `[Person]` + date | |

### Section B - What of ours do they touch?

| # | Question | Your answer |
|---|---|---|
| B1 | What do we send or store with them? `[Pick many]` | `Source code`, `Customer personal data`, `Payment info`, `Health info`, `Business documents`, `AI prompts/chats`, `Logins/credentials`, `Nothing sensitive`, `Other: ___` |
| B2 | How many people or customers' data could be involved? `[Text]` | |
| B3 | Where in the world is our data stored? `[Text]` | Country or region. If unknown, write UNKNOWN. |
| B4 | Do they hire other companies (sub-processors) that also touch our data? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| B5 | Link to their list of sub-processors `[Link]` | |
| B6 | Can they see our data in readable form (not scrambled)? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| B7 | How does our system connect to them? `[Pick many]` | `API key`, `Login (SSO)`, `Plugin/integration`, `Manual upload`, `Email`, `Other: ___` |
| B8 | Where is the key or login stored? (location only) `[Text]` | |
| B9 | Is our connection to them protected (HTTPS/encrypted)? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |

### Section C - Security and trust

| # | Question | Your answer |
|---|---|---|
| C1 | Do they have a security report card (SOC 2 Type II, ISO 27001)? `[Pick one]` | `SOC 2 Type II` / `ISO 27001` / `Both` / `None` / `UNKNOWN` |
| C2 | Link to the report or certificate, and its expiry date `[Link]` + `[Date]` | |
| C3 | Do they require 2-step login (MFA) for our accounts? `[Pick one]` | `Yes` / `No` / `Optional - we turned it on` / `Optional - we have NOT turned it on` |
| C4 | Have they had a public data leak or security incident in the past 3 years? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| C5 | If yes: what happened and what did they fix? `[Text]` | |
| C6 | Will they tell us quickly if there is a leak? How fast? `[Text]` | Hours or days, and where it is written |
| C7 | Can we delete our data when we leave, and do they confirm in writing? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| C8 | Is there a status page showing outages? `[Link]` | |
| C9 | Do they handle card payments or health data for us? `[Pick one]` | `Card payments (PCI DSS)` / `Health data (HIPAA)` / `Both` / `Neither` |
| C10 | If yes to C9: do they prove compliance (certificate or attestation)? `[Link]` | |

### Section D - Privacy (GDPR and similar laws)

*If you answered `Nothing sensitive` in B1, write `N/A - no personal data shared` for all of D.*

| # | Question | Your answer |
|---|---|---|
| D1 | Is a Data Processing Agreement (DPA) signed? `[Pick one]` | `Yes` / `No` / `Not needed - reason: ___` / `UNKNOWN` |
| D2 | Link to the signed DPA `[Link]` | |
| D3 | Is personal data sent outside the EU/UK? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| D4 | If yes: what legal protection covers the transfer? `[Text]` | Example: Standard Contractual Clauses |
| D5 | Is the vendor listed in our privacy policy? `[Pick one]` | `Yes` / `No` |
| D6 | Can we answer a customer's "delete my data" request through this vendor? How? `[Text]` | |
| D7 | How long does the vendor keep our data? `[Text]` | |

### Section E - AI-specific questions

*Only for vendors of type `AI model/API`, or any vendor with AI features. Otherwise write `N/A - not an AI vendor`.*

| # | Question | Your answer |
|---|---|---|
| E1 | Which AI model(s) and version(s) do we use? `[Text]` | |
| E2 | Does the vendor use **our** prompts, files, or code to train its AI? `[Pick one]` | `Yes` / `No - written in contract` / `No - only in marketing` / `UNKNOWN` |
| E3 | Is there a "zero retention" or "do not train" setting, and is it ON? `[Pick one]` | `Yes, ON` / `Yes, OFF` / `Not available` / `UNKNOWN` |
| E4 | How long does the vendor keep our prompts and outputs? `[Text]` | |
| E5 | Who owns the AI's outputs (text, code, images)? `[Text]` | Quote or link the contract clause |
| E6 | Does the vendor protect us if an output copies someone else's work (IP indemnity)? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| E7 | Can AI agents using this vendor change code, spend money, or contact customers without a human check? `[Pick one]` | `Yes` / `No` |
| E8 | If yes to E7: what limits or approvals are in place? `[Text]` | |
| E9 | Is the AI's output shown directly to customers? `[Pick one]` | `Yes` / `No` |
| E10 | How risky is our use of AI under the EU AI Act? `[Pick one]` | `Minimal` / `Limited (must tell users it is AI)` / `High` / `Not sure - ask helper` |
| E11 | What happens if the AI gives a wrong or harmful answer? Who checks? `[Text]` | |
| E12 | What is our fallback if the AI model is retired, changed, or becomes much more expensive? `[Text]` | |

### Section F - Reliability and growth (up to 500 customers)

| # | Question | Your answer |
|---|---|---|
| F1 | What is the vendor's promised uptime (SLA)? `[Text]` | Example: 99.9%. Write "none" if none. |
| F2 | What are the usage limits on our plan? `[Text]` | Example: 10,000 requests per day |
| F3 | At what customer count will we hit those limits? `[Text]` | Your best estimate and how you calculated it |
| F4 | What does this vendor cost at 10, 100, and 500 customers? `[Money]` | |
| F5 | What happens when we hit the limit? `[Text]` | Slows down, stops, or charges extra |
| F6 | Is there a single point of failure (if they go down, we go down)? `[Pick one]` | `Yes` / `No` |
| F7 | If yes: what is our plan during an outage? `[Text]` | |

### Section G - Money

| # | Question | Your answer |
|---|---|---|
| G1 | Pricing model `[Pick one]` | `Free`, `Monthly`, `Yearly`, `Pay-as-you-go`, `One-time`, `Mixed` |
| G2 | Current cost `[Money]` | |
| G3 | Can the bill jump unexpectedly? `[Pick one]` | `Yes` / `No` |
| G4 | If yes: what spending alert or hard cap is set? `[Money]` | |
| G5 | Who pays and from which account/card? (name only, never numbers) `[Text]` | |
| G6 | Last invoice date and amount `[Date]` + `[Money]` | |

### Section H - Leaving (exit plan)

| # | Question | Your answer |
|---|---|---|
| H1 | How do we take our data out? `[Text]` | Export button, API, or ask support |
| H2 | In what file format? `[Text]` | |
| H3 | How long would it take us to switch to a replacement? `[Text]` | |
| H4 | Who is the replacement vendor candidate? `[Text]` | |
| H5 | What must we do on our last day with them? `[Pick many]` | `Export data`, `Delete our data`, `Cancel billing`, `Remove keys/logins`, `Update privacy policy`, `Tell the team` |
| H6 | Will we get written proof that our data is deleted? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |

### Section I - Risk score (answers decide the color; see Part 4)

| # | Question | Your answer |
|---|---|---|
| I1 | Red-flag count (from Part 4, Step 1) `[Text]` | |
| I2 | Yellow-flag count (from Part 4, Step 2) `[Text]` | |
| I3 | **Final color** `[Pick one]` | 🟢 / 🟡 / 🔴 |
| I4 | Biggest risk in one sentence `[Text]` | |
| I5 | Action to reduce that risk, who does it, by when `[Text]` | |
| I6 | If 🔴 RED: who approved it, on what date, and until when? `[Person]` + `[Date]` | |

### Section J - Sign-off

| # | Question | Your answer |
|---|---|---|
| J1 | Card filled in by `[Person]` | |
| J2 | Date filled `[Date]` | |
| J3 | Checked by (second person) `[Person]` | |
| J4 | Date checked `[Date]` | |
| J5 | Next review date `[Date]` | |
| J6 | Any `UNKNOWN` answers still open? List question numbers + who will find out + by when `[Text]` | |

---

# PART 3 - CONTRACT CARDS (QUESTIONNAIRE)

*Copy once per contract. A vendor can have many contracts (for example: Terms of Service + DPA + an order form). Each gets its own ID.*

## CONTRACT CARD: C-___ for Vendor V-___

### Section A - Basics

| # | Question | Your answer |
|---|---|---|
| A1 | Contract ID `[Text]` | C-___ |
| A2 | Vendor ID this belongs to `[Text]` | V-___ |
| A3 | Contract type `[Pick one]` | `Terms of Service (click-to-accept)`, `Signed service agreement`, `DPA`, `NDA`, `SLA`, `Order form/quote`, `Freelancer/contractor agreement`, `Other: ___` |
| A4 | What does it cover, in one sentence? `[Text]` | |
| A5 | Contract status `[Pick one]` | `Draft`, `Signed`, `Active`, `Expiring soon`, `Expired`, `Terminated` |
| A6 | Who signed or accepted for us? `[Person]` | |
| A7 | Date signed or accepted `[Date]` | |
| A8 | Link to the document (or saved copy of the Terms page) `[Link]` | |
| A9 | Version or date of the Terms we accepted `[Text]` | Online Terms change. Save a copy. |

### Section B - Dates and renewal

| # | Question | Your answer |
|---|---|---|
| B1 | Start date `[Date]` | |
| B2 | End date `[Date]` | |
| B3 | Does it renew automatically? `[Pick one]` | `Yes` / `No` |
| B4 | How many days of notice to cancel? `[Text]` | |
| B5 | **Last day we can cancel** (end date minus notice days) `[Date]` | |
| B6 | Reminder set in calendar for 30 days before B5? `[Pick one]` | `Yes` / `No` |
| B7 | Can the vendor change price or terms during the contract? How much notice? `[Text]` | |

### Section C - Money

| # | Question | Your answer |
|---|---|---|
| C1 | Price `[Money]` | |
| C2 | Billing cycle `[Pick one]` | `Monthly` / `Yearly` / `Usage-based` / `One-time` |
| C3 | Minimum commitment (must we pay even if we use less?) `[Money]` | |
| C4 | Extra charges (overage, setup fee, support fee) `[Text]` | |
| C5 | Refund or free-cancel period `[Text]` | |
| C6 | Total committed spend over the contract `[Money]` | |
| C7 | Budget owner `[Person]` | |

### Section D - Legal terms (check with a legal helper for 🟡 and 🔴 vendors)

| # | Question | Your answer |
|---|---|---|
| D1 | Who owns the work/output/data we create using this vendor? `[Text]` | Quote the clause number |
| D2 | Does the vendor limit how much they owe us if something goes wrong (liability cap)? `[Text]` | Example: "capped at 12 months of fees" |
| D3 | Is that cap high enough compared to the damage a failure could cause us? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| D4 | Does the vendor promise to pay if their service breaks others' IP rights (indemnity)? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| D5 | Which country's law governs the contract? `[Text]` | |
| D6 | Can the vendor stop the service with no warning? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| D7 | Confidentiality: are they bound to keep our information secret? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| D8 | Can they use our name or logo in marketing? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| D9 | Does the contract allow us to run a security check or ask for audit reports? `[Pick one]` | `Yes` / `No` / `UNKNOWN` |
| D10 | Are there rules about what we may NOT do with their product? `[Text]` | Example: no medical use, no reselling |

### Section E - Service promises (SLA)

| # | Question | Your answer |
|---|---|---|
| E1 | Promised uptime `[Text]` | |
| E2 | Support response time promised `[Text]` | |
| E3 | What do we get if they miss the promise? `[Text]` | Credits, refund, nothing |

### Section F - Ending the contract

| # | Question | Your answer |
|---|---|---|
| F1 | How can we terminate? `[Text]` | |
| F2 | Penalty for ending early `[Money]` | |
| F3 | What happens to our data after termination, and in how many days is it deleted? `[Text]` | |
| F4 | Plan for this contract's end (renew / replace / stop) and decision date `[Text]` + `[Date]` | |

---

# PART 4 - RISK TRAFFIC LIGHT GUIDE

*Follow the steps in order. Count honestly. Do not skip.*

### Step 1 - Count the RED flags (any one = at least a 🟡; two or more = 🔴)

| # | Red flag | Where to find the answer | Yes? |
|---|---|---|---|
| R1 | Vendor can see readable customer personal, payment, or health data **and** has no SOC 2 / ISO 27001 | B1, B6, C1 | |
| R2 | Personal data is involved **and** there is no signed DPA (when one is needed) | D1 | |
| R3 | Vendor uses our prompts, code, or data to train its AI, and we did not agree | E2 | |
| R4 | Card payment or health data is involved **and** the vendor has no PCI DSS / HIPAA proof | C9, C10 | |
| R5 | AI agents can act without any human check (change code, spend money, message customers) | E7, E8 | |
| R6 | We have no way to get our data out | H1 | |
| R7 | Single point of failure **and** no outage plan | F6, F7 | |
| R8 | Bill can jump and no spending cap or alert is set | G3, G4 | |
| R9 | Vendor had a serious security incident in 3 years and has not fixed it | C4, C5 | |
| R10 | Contract lets the vendor stop service with no warning, and we depend on them | Contract D6 | |

### Step 2 - Count the YELLOW flags

| # | Yellow flag | Where | Yes? |
|---|---|---|---|
| Y1 | Any `UNKNOWN` answer is still open for more than 14 days | J6 | |
| Y2 | Data stored outside our customers' region without legal protection noted | D3, D4 | |
| Y3 | Vendor has no status page and no SLA | C8, F1 | |
| Y4 | We will hit the plan limit before 500 customers | F3 | |
| Y5 | Auto-renews and the cancel date is within 90 days | Contract B3, B5 | |
| Y6 | Only one person knows how this vendor is set up | A10 | |
| Y7 | MFA is available but we have not turned it on | C3 | |
| Y8 | No backup vendor identified | A7, H4 | |
| Y9 | Liability cap is low compared to potential harm | Contract D3 | |
| Y10 | Vendor can change terms or price with little notice | Contract B7 | |

### Step 3 - Decide the color

| Result | Color |
|---|---|
| 0 red flags and 0-2 yellow flags | 🟢 GREEN |
| 0 red flags and 3+ yellow flags, **or** exactly 1 red flag | 🟡 YELLOW |
| 2+ red flags | 🔴 RED |
| Any red flag involving **R3, R4, or R5** | Treat as at least 🟡, and 🔴 if the vendor touches real customer data |

### Step 4 - What to do next

- 🟢 Write the next review date (12 months).
- 🟡 Fill in I5 (risk reduction action). Review in 6 months.
- 🔴 Stop using it with real customer data until the person in 0.14 approves in writing (fill I6). Review in 3 months.

---

# PART 5 - LIFECYCLE GATE CHECKLISTS

*Before moving to the next stage, tick every box. If you cannot tick one, write who will fix it and by when.*

### Gate 1 → 2: Ready to Build

- [ ] Part 0 is fully filled in.
- [ ] Every tool the team already uses has a Vendor Card.
- [ ] Every AI tool used on source code has answers for E2, E3, and E4.
- [ ] A written rule exists: what may and may not be pasted into AI tools (example: no customer data, no secrets).
- [ ] Every vendor has a color.

### Gate 2 → 3: Ready to Launch

- [ ] Production vendors (hosting, database, email, payments, monitoring) all have Vendor and Contract Cards.
- [ ] No 🔴 vendor touches real customer data without written approval.
- [ ] All DPAs are signed where personal data is shared (D1, D2).
- [ ] Privacy policy lists the vendors that process customer data (D5).
- [ ] Payment vendor handles all card data (so we never store card numbers).
- [ ] Every vendor has an exit plan (Section H).
- [ ] Spending alerts or caps are set on every pay-as-you-go vendor (G4).
- [ ] Contracts with auto-renew have reminders in the calendar.
- [ ] AI features shown to customers have a human-check or fallback plan (E11, E12) and are labeled as AI where required (E10).
- [ ] Status pages or outage alerts are set up for critical vendors.

### Gate 3 → 4: Ready to Grow to 500 Customers

- [ ] F3 and F4 are filled in for every vendor (limits and costs at 10 / 100 / 500).
- [ ] We know the first vendor that will hit its limit and have a plan.
- [ ] First quarterly review (Part 6) is done.
- [ ] Customer data requests (delete, export) have been tested through each vendor that stores customer data (D6).
- [ ] Total monthly vendor cost at 500 customers is within budget (0.13).

### Gate "500 customers reached": Closing the first phase

- [ ] Full review of all vendors done within the last 30 days.
- [ ] Every UNKNOWN is resolved or has an owner and a date.
- [ ] Vendors that did not scale are marked `Being replaced` with a plan.
- [ ] "Lessons learned" written in Part 11.

---

# PART 6 - REVIEW AND RENEWAL CALENDAR

### Quarterly review (every 3 months) - 30-minute checklist

- [ ] Open Part 1. Does every row still match reality?
- [ ] Any new tool being used that has no card? Add it now.
- [ ] Any vendor no longer used? Mark `Removed` and complete the H5 checklist.
- [ ] Any contract ending in the next 90 days? Decide: renew, replace, stop.
- [ ] Any 🔴 vendor: is the approval still valid?
- [ ] Any `UNKNOWN` left? Chase.
- [ ] Did any vendor change its terms, price, or privacy rules? Update the cards.
- [ ] Update the quick totals in Part 1.
- [ ] Update 0.17 (date last fully reviewed).

### Renewal timeline (copy one row per contract)

| Contract ID | Vendor | End date | Last day to cancel | 30-day reminder date | Decision (renew / replace / stop) | Decided by | Decision date |
|---|---|---|---|---|---|---|---|
| C-001 | | | | | | | |
| C-002 | | | | | | | |

### Review log

| Review date | Done by | Vendors added | Vendors removed | Issues found | Next review date |
|---|---|---|---|---|---|
| | | | | | |

---

# PART 7 - COMPLETENESS CHECKLIST ("IS THIS READY?")

Tick everything. If anything is unticked, the register is **not ready**.

- [ ] Part 0 has no blank answers.
- [ ] Part 1 has one row for every vendor, and totals are updated.
- [ ] Each vendor has a Vendor Card (Part 2) with no blank answers (UNKNOWN is OK, but must have an owner and date).
- [ ] Each contract has a Contract Card (Part 3).
- [ ] Every vendor has a color from Part 4 (not guessed).
- [ ] Every 🔴 vendor has a written approval or has been paused.
- [ ] No secrets, passwords, keys, or customer data are written in this file.
- [ ] All dates use `YYYY-MM-DD`.
- [ ] All money values include a currency.
- [ ] Links open and point to the right files.
- [ ] Two different people have signed off (J1 and J3) on each card.
- [ ] Next review date is in the calendar.

---

# PART 8 - FILLED-IN EXAMPLE (FAKE DATA - FOR LEARNING ONLY)

*Look at this to see what a good answer looks like. Do not copy the facts. "Example Mail Co" is made up.*

## VENDOR CARD: V-001 : Example Mail Co

**Section A - Basics**

| # | Question | Example answer |
|---|---|---|
| A2 | Vendor name | Example Mail Co, Inc. |
| A4 | Vendor type | SaaS/business tool |
| A5 | What do we use them for? | Send sign-up and password-reset emails to customers. |
| A6 | Why them? | Cheapest option with good delivery rates and a signed DPA. |
| A7 | Backup option | Switch to Backup Mail Ltd. Takes about 1 day. |
| A8 | Stage(s) | 3-Launch, 4-Grow to 500 |
| A9 | Status | In use |
| A10 | Owner | Priya Shah, Co-founder |

**Section B - Data**

| # | Question | Example answer |
|---|---|---|
| B1 | What do we send them? | Customer emails, Names |
| B3 | Where is data stored? | Ireland (EU), per their DPA |
| B4 | Sub-processors? | Yes |
| B6 | Can they read it? | Yes (they must, to send the email) |
| B8 | Where is the key stored? | Team password manager, vault "Production" |

**Section C - Security**

| # | Question | Example answer |
|---|---|---|
| C1 | Security report card | SOC 2 Type II |
| C2 | Link + expiry | `/compliance/examplemail-soc2.pdf`, expires 2027-03-31 |
| C3 | MFA | Optional - we turned it on |
| C4 | Leaks in 3 years | No |

**Section D - Privacy**

| # | Question | Example answer |
|---|---|---|
| D1 | DPA signed? | Yes |
| D2 | Link | `/contracts/examplemail-dpa.pdf` |
| D3 | Data leaves EU? | No |
| D5 | In privacy policy? | Yes |

**Section E - AI**

`N/A - not an AI vendor`

**Section F, G, H (short version)**

| # | Question | Example answer |
|---|---|---|
| F2 | Limits | 50,000 emails per month on current plan |
| F3 | When hit? | At about 400 customers (125 emails per customer per month) |
| F4 | Cost at 10 / 100 / 500 | USD 20 / USD 20 / USD 90 per month |
| G4 | Spending cap | Alert at USD 100 per month |
| H1 | How to export? | CSV export button in Settings > Data |
| H5 | Last-day tasks | Export data, Delete our data, Remove keys, Update privacy policy |

**Section I - Risk**

| # | Question | Example answer |
|---|---|---|
| I1 | Red flags | 0 |
| I2 | Yellow flags | 1 (Y4: will hit plan limit before 500 customers) |
| I3 | Final color | 🟢 GREEN |
| I4 | Biggest risk | Email limit may be reached around 400 customers. |
| I5 | Action | Priya Shah to upgrade the plan before customer 350. Reminder set for 2027-01-15. |

## CONTRACT CARD: C-001 for Vendor V-001 (example)

| # | Question | Example answer |
|---|---|---|
| A3 | Contract type | Terms of Service (click-to-accept) |
| A7 | Date accepted | 2026-09-02 |
| A9 | Version of Terms | "Terms updated 2026-06-10". Saved to `/contracts/examplemail-tos-2026-06-10.pdf` |
| B2 | End date | 2027-09-02 |
| B3 | Auto-renews? | Yes |
| B4 | Notice to cancel | 30 days |
| B5 | Last day to cancel | 2027-08-03 |
| C1 | Price | USD 20 per month |
| D2 | Liability cap | Capped at 12 months of fees (about USD 240) |
| D3 | Cap high enough? | No - but the data involved is low sensitivity. Risk accepted by Priya Shah on 2026-09-02. |

---

# PART 9 - INSTRUCTIONS FOR AI AGENTS

*If you are an AI agent reading, updating, or checking this file, follow these rules exactly.*

1. **Source of truth.** This file is the only source of truth for vendors and contracts. Do not invent facts. If an answer is missing, write `UNKNOWN - [owner] will find out by [date]`. Never fill in a plausible guess.
2. **Never write secrets.** Do not write passwords, API keys, tokens, card numbers, or customer data. If you find one in the file, remove it, tell the Register Owner, and note it in Part 11.
3. **Cite evidence.** For every legal or security claim (DPA signed, SOC 2 valid, no-training promise), there must be a `[Link]` to proof. If there is none, mark the answer `UNKNOWN`.
4. **IDs.** Vendor IDs are `V-###`, contract IDs are `C-###`. Never reuse or renumber an ID.
5. **Keep tables in sync.** After changing any Vendor Card, update its row in Part 1 and the quick totals.
6. **Compute risk by rules.** Calculate the color using Part 4 only. Do not override a color without a written human approval.
7. **Do not approve for humans.** You may recommend. You may not mark a 🔴 vendor as approved. Only the person named in 0.14 can approve.
8. **Date logic.** Last day to cancel = End date minus notice days. Flag any contract whose cancel date is within 90 days as `Expiring soon`.
9. **Validation checklist before saving:**
   - No blank answers (only `UNKNOWN` or `N/A - reason`)
   - Dates are `YYYY-MM-DD`
   - Money has currency
   - Every vendor has an owner
   - Every contract maps to a real vendor ID
   - Part 1 matches the cards
10. **When you change something**, add a line to the change log in Part 11 with date, what changed, and why.
11. **Ask, don't assume.** If a request would break any rule here (for example, "add this API key to the register"), refuse and explain.
12. **Escalate** to the Register Owner when you find: a 🔴 vendor in use without approval, an expired contract still in use, a missing DPA with personal data involved, or an AI agent permitted to act without a human check.

---

# PART 10 - GLOSSARY (SIMPLE WORDS)

| Word | Simple meaning |
|---|---|
| **Vendor** | An outside company, tool, or person we depend on. |
| **Contract** | Any agreement with a vendor, including click-to-accept terms. |
| **API** | A way for our software to talk to another company's software. |
| **API key** | A secret password our software uses to talk to a vendor. Never write it here. |
| **AI model** | The "brain" behind an AI tool. |
| **Prompt** | What we type or send to an AI. |
| **Training** | When an AI company learns from data to improve its AI. We do not want our private data used for this unless we agree. |
| **Zero retention** | The vendor does not keep what we send them. |
| **DPA (Data Processing Agreement)** | A signed promise about how a vendor handles personal data. |
| **Sub-processor** | Another company our vendor uses that also touches our data. |
| **SOC 2 / ISO 27001** | Independent security "report cards" for companies. |
| **PCI DSS** | Security rules for handling card payments. |
| **HIPAA** | US rules for protecting health information. |
| **GDPR** | EU rules for protecting personal data. |
| **EU AI Act** | EU rules about how AI is built and used, sorted by risk level. |
| **MFA / 2-step login** | Logging in with a password **and** a code from your phone. |
| **SLA** | A promise about uptime and support speed. |
| **Uptime** | How often the service works. 99.9% means about 9 hours of downtime per year. |
| **Liability cap** | The most a vendor must pay us if something goes wrong. |
| **Indemnity** | A promise to cover our costs if something they provided causes a legal problem. |
| **Auto-renew** | The contract continues (and charges) unless we cancel in time. |
| **Single point of failure** | One thing that, if it breaks, stops everything. |
| **Exit plan** | The steps to leave a vendor safely. |
| **Personal data** | Anything that can identify a person (name, email, location, IP address). |

---

# PART 11 - CHANGE LOG AND LESSONS LEARNED

### Change log

| Date | Who | What changed | Why |
|---|---|---|---|
| | | | |

### Lessons learned (fill at the "500 customers" gate)

| # | Question | Your answer |
|---|---|---|
| 11.1 | Which vendor surprised us most (cost, limits, or terms)? | |
| 11.2 | Which vendor decision would we make differently? | |
| 11.3 | Which question in this template was the most useful? | |
| 11.4 | Which question was confusing or missing? (send to the template owner) | |
| 11.5 | What should we change in the master template? | |
