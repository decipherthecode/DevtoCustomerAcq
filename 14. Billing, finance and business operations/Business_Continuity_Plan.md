# How to Fill In This Document (Read This First)

**What is this?** A Business Continuity Plan (BCP) is a "what do we do if something breaks?" guide. It keeps your product, your customers, and your money flowing when things go wrong (a server crashes, an AI service goes down, a payment tool stops, a key person is unavailable).

**Who is it for?** Anyone. If you can answer questions about your own project, you can fill this in. No technical background needed.

## The 8 simple rules

1. **Go in order, MUST first.** Start at Part 1 and work to Part 15, answering the **MUST** questions (no tag). Questions tagged **[ADVANCED]** can wait until your project is ready (see "MUST vs ADVANCED" below). Each part builds on the one before it.
2. **Answer every question.** Write in the line that says `Your answer:`. Delete the grey hint text in `(brackets)` if you like.
3. **Look at the Example.** Every question has an `Example:` so you can see what a good answer looks like. Copy the style, not the words.
4. **Don't know yet? Write `TBD (name, date)`.** Example: `TBD (Sam, 30 Nov)`. Never leave a blank. A blank means "forgot"; a TBD means "someone is on it".
5. **Doesn't apply? Write `N/A: because ...`** Always give the reason in a few words.
6. **Use real names, real numbers, real links.** Not "the team" but "Priya". Not "quickly" but "within 2 hours".
7. **One fact per answer.** Short sentences. If an answer needs more than 3 lines, put it in a table or list.
8. **Never write passwords, API keys, or card numbers in this file.** Write *where* they are stored instead (example: "in the team password manager, folder 'Prod'").

## Key words in plain English

| Word | Simple meaning | Example |
|---|---|---|
| **BCP** | Plan to keep the business running during a problem | This document |
| **Incident** | Anything that breaks or threatens normal work | Website is down |
| **RTO** (Recovery Time Objective) | *How long* can this be broken before it really hurts? | "Back within 4 hours" |
| **RPO** (Recovery Point Objective) | *How much recent work* can we afford to lose? | "Lose at most 1 hour of data" |
| **Critical function** | Something that must keep working or be restored first | Taking payments, logging in |
| **Vendor / dependency** | An outside company or tool you rely on | Stripe, AWS, OpenAI, App Store |
| **Workaround** | A temporary way to keep going while the real fix happens | Take orders by email form |
| **Single point of failure** | One thing or person whose failure stops everything | Only one person knows the password vault |
| **Failover** | Switching to a backup automatically or manually | Switch to backup AI model |
| **Runbook** | Step-by-step instructions for one problem | "If database is down, do 1, 2, 3" |
| **First 500 customers** | The period from first paying customer until customer #500 | Your early-growth stage |

## How the plan is organised

| Part | What you will answer | Time to fill |
|---|---|---|
| 1 | Basics: project, owner, scope | 10 min |
| 2 | Lifecycle stage and stage gates: where is the project today? | 20 min |
| 3 | What must keep working (importance + time limits) | 30 min |
| 4 | What could go wrong (risks) | 30 min |
| 5 | Who and what you depend on (vendors, tools, exit plans) | 45 min |
| 6 | People, roles, on-call, and who to call | 30 min |
| 7 | Step-by-step recovery playbooks (5 core + 12 ready-made) | 90 min |
| 8 | Billing, finance, and money continuity | 60 min |
| 9 | Data backup and recovery | 20 min |
| 10 | AI-specific continuity (models, agents, prompts, costs) | 45 min |
| 11 | Customer milestones and stage gates (customers 1 to 500) | 30 min |
| 12 | Communication plan | 20 min |
| 13 | Legal, insurance, and compliance | 30 min |
| 14 | Testing, review, and updates | 10 min |
| 15 | Final checklist and sign-off | 10 min |

## Quick start: the "Lite" path (first 90 minutes)

Short on time (solo founder, Stage A or B)? Answer **only** these first, then come back for the rest: **Q1.1 to Q1.4, Q2.1, Q3.1, Q3.2, Q4.1, Q5.1, Q5.4, Q6.1, Playbooks P-A, P-C and P-E, Q8.5, Q9.1, Q9.4**. Mark everything else `TBD (name, date)`. A partly finished plan that exists beats a perfect plan that never gets written.

**Total: about 7 to 8 hours the first time (spread over a few days is fine). Then about 45 minutes per review.**

## Cloning this template for a new project (do this first)

This file is a **master template**. For each new project, copy it, then use find-and-replace on these placeholders:

| Placeholder | Replace with | Example |
|---|---|---|
| `[PROJECT_NAME]` | Product name | BillPilot |
| `[COMPANY_NAME]` | Legal company name | BillPilot Pvt Ltd |
| `[PLAN_OWNER]` | Person responsible for this plan | Priya Sharma |
| `[BACKUP_OWNER]` | Backup person | Ravi Kumar |
| `[LAUNCH_DATE]` | Public launch date | 2027-02-01 |
| `[CLOUD_PROVIDER]` | Where the product runs | AWS |
| `[PAYMENT_PROVIDER]` | Who takes payments | Stripe |
| `[AI_PROVIDER]` | Main AI model provider | (your provider) |
| `[STATUS_PAGE_URL]` | Public status page link | status.example.com |
| `[SUPPORT_EMAIL]` | Support inbox | support@example.com |
| `[TODAY]` | Today's date (YYYY-MM-DD) | 2026-10-19 |

> Tip: after replacing, search the file for `[` to find any placeholder you missed.

## Progress tracker (update as you go)

Mark each part: **Not started / In progress / Done / N/A**. Add the date and the person who completed it.

| Part | Title | Status | Completed by | Date |
|---|---|---|---|---|
| 1 | The Basics | Not started | | |
| 2 | Where Is Your Project Right Now? (lifecycle) | Not started | | |
| 3 | What Must Keep Working? | Not started | | |
| 4 | What Could Go Wrong? | Not started | | |
| 5 | Who and What You Depend On | Not started | | |
| 6 | People, Roles, and Who to Call | Not started | | |
| 7 | Recovery Playbooks | Not started | | |
| 8 | Billing, Finance, and Money Continuity | Not started | | |
| 9 | Data Backup and Recovery | Not started | | |
| 10 | AI-Specific Continuity | Not started | | |
| 11 | Customer Milestones and Stage Gates | Not started | | |
| 12 | Communication Plan | Not started | | |
| 13 | Legal, Insurance, and Compliance | Not started | | |
| 14 | Testing, Review, and Updates | Not started | | |
| 15 | Final Checklist and Sign-Off | Not started | | |

## MUST vs ADVANCED: what to fill and when

Every question is either **MUST** or **ADVANCED**.

- **MUST** (no tag): fill in now. These protect you if something breaks this month.
- **[ADVANCED]**: fill in when you reach Stage E (early customers), when the topic applies to you, or when you have time. Until then write `TBD (name, date)`. Advanced items are still worth doing before customer #100.
- **Stage gates (Q2.4 to Q2.9):** fill in **only** the gate for the stage you are leaving next. Leave later gates for later.
- **Playbooks:** P-A to P-E are MUST. P-F to P-Q are ADVANCED, but write the matching playbook as soon as its risk score is 13 or higher.

| Part | MUST (fill now) | ADVANCED (fill later) |
|---|---|---|
| 1 | Q1.1 to Q1.9 | Q1.10 |
| 2 | Q2.1 to Q2.3 + your next gate | Other gates |
| 3 | Q3.1 to Q3.5, Q3.7 | Q3.6 |
| 4 | Q4.1 to Q4.4 | Q4.5 |
| 5 | Q5.1 to Q5.4 | Q5.5 to Q5.8 |
| 6 | Q6.1 to Q6.7 | Q6.8 to Q6.12 |
| 7 | Q7.1 to Q7.4, P-A to P-E | P-F to P-Q |
| 8 | Q8.1 to Q8.11 | 8B (Q8.12 to Q8.26) |
| 9 | All | None |
| 10 | Q10.1 to Q10.11 (skip if no AI) | 10B (Q10.12 to Q10.25) |
| 11 | Q11.1 to Q11.5 | Q11.6 to Q11.11 |
| 12 | All | None |
| 13 | Q13.1 to Q13.16 | 13B and 13C (Q13.17 to Q13.26) |
| 14 | Q14.1 to Q14.5 | Q14.6, Q14.7 |
| 15 | All | None |

## Question IDs

Every question has an ID such as **Q3.2** (Part 3, question 2). Playbooks use IDs like **P-A**. Use these IDs when you talk to a teammate or an AI assistant ("please help me with Q8.5").

## Rating guide (used in several places)

**Importance level**

| Level | Name | Meaning |
|---|---|---|
| 1 | Critical | Business or customers are badly hurt within hours |
| 2 | Important | Painful, but we can cope for a day or two |
| 3 | Nice to have | Can wait a week or more |

**Risk score = Likelihood (1 to 5) x Impact (1 to 5)**

| Score | Meaning | What to do |
|---|---|---|
| 1 to 5 | Low | Accept and watch |
| 6 to 12 | Medium | Write a workaround |
| 13 to 25 | High | Write a full playbook (Part 7) and test it |

**Likelihood:** 1 = almost never, 3 = maybe once a year, 5 = happens often.
**Impact:** 1 = barely noticed, 3 = customers annoyed, 5 = customers leave or money is lost or laws are broken.

## Instructions for AI Assistants (Agents)

> **If you are an AI assistant helping a person fill in this document, follow this section exactly. If you are a human, you can skip it, or paste the prompt below into your AI assistant.**

### Rules for the AI

1. **Interview, don't invent.** Ask **one question at a time**, in plain words a 10-year-old can follow. Wait for the answer. Never make up names, numbers, dates, prices, vendors, or promises.
2. **Go in order, by level.** Fill every MUST question first (see "MUST vs ADVANCED"). Offer ADVANCED questions only after the MUST parts are done, or when the person asks.
3. **Use the question ID** (for example Q3.2) when you ask and when you write the answer into the file.
4. **Show the Example, then ask.** Read the example, then ask the person for *their* real answer. Offer to explain any term using the "Key words in plain English" table.
5. **Missing information:** write `TBD (name, date)`. If the topic does not apply, write `N/A: reason`. Never leave a blank, never guess.
6. **Confirm before saving.** After each part, show the answers back in a short list and ask: "Is this right?" Fix anything the person corrects.
7. **No secrets.** If the person pastes a password, key, token, or card number, **do not copy it into the file.** Say so, and ask where it is stored instead.
8. **Keep consistency.** Check that RTO is shorter than the absolute limit (Q3.7), every Critical function has an owner, every risk scoring 13+ has a playbook, and every role has a backup person.
9. **Flag, don't decide, on law, tax, and insurance.** Write the person's answer, mark unclear items "Not sure", and suggest a qualified professional.
10. **Update the Progress tracker** when a part is finished and tick the Part 15 checklist honestly.
11. **Stay at the right stage.** Use Part 2 to match depth to the project's stage. Do not demand enterprise-level detail from a Stage A or B project.
12. **A human signs off.** Never fill in names or dates in the Sign-off table on behalf of a person. End with: "A person must review this plan and sign it in Part 15."

### Copy-and-paste prompt

```
You are helping me complete the Business Continuity Plan template (Business_Continuity_Plan.md) for my project, [PROJECT_NAME].
Follow the section "Instructions for AI Assistants (Agents)" in the file.
Start with the cloning step: ask me for the values of the placeholders and replace them.
Then interview me, one question at a time, starting with Part 1.
Fill MUST questions first. Do not invent facts. Use TBD (name, date) when I don't know.
Never write passwords, keys, or card numbers into the file.
After each Part, summarize my answers and ask me to confirm before you save them.
At the end, run the Part 15 checklist and tell me what is missing.
```

### Copy-and-paste prompt: review only

```
Review my filled-in Business_Continuity_Plan.md. List, in priority order:
1) blank or TBD answers without an owner or date,
2) Critical functions without an owner, RTO, RPO, or workaround,
3) risks scoring 13 or higher without a playbook,
4) roles without a backup person,
5) anything that looks like a secret (password, key, card number),
6) answers that contradict each other (for example RTO longer than the absolute limit).
Do not rewrite my answers. Only list the problems and the question IDs.
```

---

# Document Control

| Field | Your answer |
|---|---|
| Document name | Business_Continuity_Plan.md |
| Project / product name | [PROJECT_NAME] |
| Company name | [COMPANY_NAME] |
| Template version | 3.0 |
| Plan version | (Example: 0.1 draft, 1.0 approved) |
| Date created | [TODAY] |
| Last reviewed | (YYYY-MM-DD) |
| Next review due | (YYYY-MM-DD, at most 6 months away) |
| Plan owner (one person) | [PLAN_OWNER] |
| Backup owner | [BACKUP_OWNER] |
| Planned public launch date | [LAUNCH_DATE] |
| Confidentiality | (Example: Internal only. Share a summary with customers on request.) |
| Where this file lives | (Link or folder path) |
| Where a printed/offline copy lives | (Example: "PDF in owner's phone and in shared drive") |

> **Important:** Keep one copy of this plan **outside** the systems it protects. If your cloud drive is down, you still need to read this.

---

# Part 1: The Basics

**Q1.1. In one or two sentences, what does this product do?**
Example: *"BillPilot is a mobile and web app that lets freelancers send invoices and get paid by card."*
Your answer:

**Q1.2. Who are your customers?**
Example: *"Freelancers and small agencies in the US and EU."*
Your answer:

**Q1.3. What type of product is it? (tick all that apply)**
- [ ] SaaS web app
- [ ] Mobile app (iOS / Android)
- [ ] Marketplace / e-commerce (buyers and sellers, orders, payments)
- [ ] AI / LLM-powered features
- [ ] Other: ______

**Q1.4. What is covered by this plan?** (what is IN)
Example: *"Production app, billing, customer support, AI features, company bank account, key vendors."*
Your answer:

**Q1.5. What is NOT covered?** (what is OUT)
Example: *"Office building (we are remote), internal side projects."*
Your answer:

**Q1.6. Where do you operate and where are your customers?** (countries or regions; this matters for law)
Example: *"Team in India; customers in US, UK, Germany."*
Your answer:

**Q1.7. How many people are on the team (including part-time and contractors)?**
Your answer:

**Q1.8. Does anyone outside the team need to approve this plan?** (investor, client, auditor)
Example: *"No."* or *"Yes, our enterprise client Acme requires a copy."*
Your answer:

**Q1.9. Our continuity promise to ourselves (policy and goals).** In 2 to 3 sentences: why do we keep this plan, and what are our goals?
Example: *"We keep customers' data safe and our service running. Goal: Critical functions back within their time limits (Part 3), no customer is charged wrongly without a fix within 3 days, and the plan is tested twice a year."*
Your answer:

**[ADVANCED] Q1.10. Who else cares about this plan, and what do they expect?** (customers, investors, regulators, payment provider, app stores, insurers, partners)

| Who | What they expect from us | Where it is written (contract, law, terms) |
|---|---|---|
| (Example) Customers | 99.5% uptime, data safe | Terms of service |
| (Example) Payment provider | Low chargebacks, fast response to disputes | Provider agreement |
| | | |

---

# Part 2: Where Is Your Project Right Now?

The right level of detail depends on your stage. Pick **one** current stage; you will revisit this plan when you move to the next stage.

**Q2.1. Current stage (tick one):**
- [ ] **Stage A: Planning and design** (idea, requirements, designs)
- [ ] **Stage B: Building** (AI-assisted development, coding, integrating)
- [ ] **Stage C: Testing and pre-launch** (QA, security checks, beta users)
- [ ] **Stage D: Launch week** (going live, first public users)
- [ ] **Stage E: Early customers (1 to 100)**
- [ ] **Stage F: Growing customers (101 to 500)**
- [ ] **Stage G: Beyond 500** (time to upgrade this plan)

**Q2.2. Target dates**

| Milestone | Planned date | Actual date |
|---|---|---|
| Build starts | | |
| Beta / test users start | | |
| Public launch | | |
| Customer #1 pays | | |
| Customer #100 | | |
| Customer #500 | | |

**Q2.3. What is the single most important thing that must NOT fail at this stage?**
Example (Stage B): *"Our source code and AI prompts must never be lost."*
Example (Stage D): *"Sign-up and payment must work on launch day."*
Your answer:

> **Rule of thumb by stage**
> - **A to B:** Protect code, designs, accounts, and keys. Backups and who-has-access matter most.
> - **C:** Protect test data, check restore works, avoid real customer data in test systems.
> - **D:** Protect sign-up, login, payments, and support. Have a launch-day rollback plan.
> - **E to F:** Protect customer data, billing accuracy, uptime, and trust. Every unhappy customer is a big share of your base.

## Stage Gates: "Are we safe to move on?"

A **gate** is a short checkpoint. Before you move from one stage to the next, every **Must** item below should be `Yes`. If an item is `No`, either fix it or write down who accepts the risk and until when. Tick the gate only when the evidence exists (a link, a screenshot, a test result).

**Q2.4. Gate A to B: Planning is done, we can start building**

| Check | Must / Should | Yes / No | Evidence (link, note) |
|---|---|---|---|
| Parts 1 to 3 of this plan are filled in | Must | | |
| Code lives in a shared code host (not only on one laptop) | Must | | |
| Two people can reach every key account (cloud, code, domain, payments) | Must | | |
| Password manager and two-step login are used by everyone | Must | | |
| AI tools used for development are approved (which tools, which data may be shared) | Must | | |
| Rules exist for what must never be pasted into an AI tool (customer data, keys) | Must | | |
| Budget and monthly cost limit are set | Should | | |

**Q2.5. Gate B to C: Build is done, we can start testing**

| Check | Must / Should | Yes / No | Evidence |
|---|---|---|---|
| Automatic backups are on for code and data | Must | | |
| Every change is reviewed by a human before merging (extra care for AI-written code) | Must | | |
| Automated tests run on every change | Must | | |
| Secrets (keys, passwords) are not stored in code | Must | | |
| Staging (practice copy) exists and is separate from live | Must | | |
| Release can be rolled back | Must | | |
| Parts 4 to 7 of this plan are filled in | Must | | |
| Dependencies and vendors listed (Part 5) | Should | | |

**Q2.6. Gate C to D: Testing is done, we can launch**

| Check | Must / Should | Yes / No | Evidence |
|---|---|---|---|
| A backup restore was tested and worked | Must | | |
| A rollback was practiced | Must | | |
| Sign-up, login, payment, refund, and cancel flows were tested end to end | Must | | |
| Payment backup path is ready (Playbook P-E) | Must | | |
| Monitoring and alerts reach a real person | Must | | |
| Status page is live and hosted separately | Must | | |
| Support inbox is ready and someone owns it | Must | | |
| AI off switch and backup model tested (if AI is used) | Must | | |
| Privacy policy, terms, and refund policy are published | Must | | |
| Security checks done (scan for leaked keys, known holes) | Must | | |
| Load test shows the system handles launch-day traffic | Should | | |
| Parts 8 to 13 of this plan are filled in | Must | | |
| One tabletop talk-through completed | Should | | |

**Q2.7. Gate D to E: Launch week is done, we are in early customer stage**

| Check | Must / Should | Yes / No | Evidence |
|---|---|---|---|
| Launch incidents are written down with lessons learned | Must | | |
| Every payment in the first week was checked by a human | Must | | |
| Every support message was answered within the promised time | Must | | |
| Cost report vs. budget reviewed (cloud and AI) | Must | | |
| This plan was updated with what we learned | Must | | |

**Q2.8. Gate E to F: We reach about 100 customers**

| Check | Must / Should | Yes / No | Evidence |
|---|---|---|---|
| Monthly billing reconciliation done for at least 2 months | Must | | |
| Chargeback and fraud checks in place | Must | | |
| A second person can run every Critical function | Must | | |
| Quarterly restore test done | Must | | |
| Customer data request process tested (see my data / delete my data) | Must | | |
| Uptime and support response numbers are tracked | Should | | |

**Q2.9. Gate F to G: We reach about 500 customers (time to level up this plan)**

| Check | Must / Should | Yes / No | Evidence |
|---|---|---|---|
| Written security and access policy exists | Must | | |
| Incident log kept for the whole period | Must | | |
| On-call schedule exists (no one is "always on" by default) | Must | | |
| Customer-ready summary of this plan is available | Should | | |
| Decision made on SOC 2 / ISO 27001 and the date | Should | | |
| Second region or provider plan for the most critical function | Should | | |
| Cyber insurance reviewed (see Part 13) | Should | | |

---

# Part 3: What Must Keep Working? (Business Impact)

This is the **most important** part. It decides what gets fixed first.

**Q3.1. List every "function" the business needs.** A function is a job the business does. Use the table below. Start with the examples, then add your own. Delete example rows that don't apply.

How to fill each column:
- **Importance:** 1, 2, or 3 (see Rating guide).
- **RTO:** longest acceptable time it can be down.
- **RPO:** longest acceptable time of lost data/work.
- **Workaround:** what you do while it is broken.
- **Owner:** one named person.

| # | Function | Importance (1/2/3) | RTO | RPO | Workaround while down | Owner |
|---|---|---|---|---|---|---|
| 1 | Customers can sign up and log in | 1 | 2 hours | 15 min | Manual account creation by support | |
| 2 | Customers can pay / subscribe | 1 | 4 hours | 0 (no lost payments) | Send payment link by email; record manually | |
| 3 | Core product works (main feature) | 1 | 4 hours | 1 hour | Status page + read-only mode | |
| 4 | AI features work | 2 | 8 hours | N/A | Switch to backup model or turn off AI feature with a notice | |
| 5 | Customer support can answer | 2 | 8 hours | 1 day | Shared inbox + auto-reply | |
| 6 | Invoices and receipts are sent | 2 | 24 hours | 1 day | Send manually later | |
| 7 | Refunds and chargebacks are handled | 2 | 48 hours | 1 day | Handle in payment provider dashboard | |
| 8 | Team can write and ship code | 2 | 24 hours | 1 hour | Use local copies and backup repo | |
| 9 | Marketing site / app store listing | 3 | 3 days | 1 day | Social post with status | |
| 10 | Payroll and paying contractors | 2 | 3 days | N/A | Manual bank transfer | |
| 11 | | | | | | |
| 12 | | | | | | |

**Q3.2. Which functions are Importance 1 (Critical)? Write the list in priority order. This is your "restore first" list.**
Example: *"1) Log in, 2) Payments, 3) Core product."*
Your answer:

**Q3.3. For each Critical function, what is the cost of being down?** (Estimate. A rough number is better than none.)

| Function | Money lost per hour down | Other harm (trust, legal, refunds) |
|---|---|---|
| (Example) Payments | $50 in missed sign-ups | Angry customers, possible churn |
| | | |

**Q3.4. What is the "Minimum Service"?** If everything went wrong, what is the *smallest* version of your service that would still be acceptable?
Example: *"Customers can log in, view data, and download invoices. New sign-ups paused."*
Your answer:

**Q3.5. Are there busy days when downtime hurts more?** (launch day, month-end billing, sale days, tax season)
Example: *"1st of each month: subscription renewals run."*
Your answer:

**[ADVANCED] Q3.6. What does each Critical function need to run?** (people, tools, data, vendors, place to work). If any item is missing, the function cannot be restored.

| Critical function | People needed | Tools and systems | Data needed | Vendors needed | Place / equipment |
|---|---|---|---|---|---|
| (Example) Take payments | Meera, Ravi | Billing service, payment provider | Customer and plan records | Payment provider, cloud | Any laptop + internet |
| | | | | | |

**Q3.7. Absolute limit (Maximum Tolerable Downtime).** For each Critical function, how long can it be down before the business is in serious trouble (customers leave in large numbers, money is lost that cannot be recovered, laws are broken)? This must be **longer** than the RTO.

| Critical function | RTO (goal) | Absolute limit | What happens past the limit |
|---|---|---|---|
| (Example) Take payments | 4 hours | 24 hours | Lost sign-ups; provider review risk |
| | | | |

---

# Part 4: What Could Go Wrong? (Risks)

**Q4.1. Review the risk list. Score each: Likelihood (1 to 5) x Impact (1 to 5) = Score.** Add your own at the bottom. Any score **13 or higher** needs a playbook in Part 7.

| # | Risk | Likelihood | Impact | Score | Playbook needed? (Y/N) |
|---|---|---|---|---|---|
| R1 | Website or app is down (hosting/cloud outage) | | | | |
| R2 | Database lost or corrupted | | | | |
| R3 | Bad release / bug deployed to everyone | | | | |
| R4 | Cyberattack, ransomware, or data breach | | | | |
| R5 | Stolen or leaked passwords / API keys | | | | |
| R6 | Payment provider outage or account frozen | | | | |
| R7 | Payment fraud, chargeback spike | | | | |
| R8 | AI model provider outage or rate limit | | | | |
| R9 | AI gives wrong, harmful, or unsafe output | | | | |
| R10 | AI costs spike unexpectedly (bill shock) | | | | |
| R11 | AI vendor changes or removes a model you depend on | | | | |
| R12 | App store rejects or removes your app | | | | |
| R13 | Key person leaves, is sick, or is unreachable | | | | |
| R14 | Lost access to an important account (email, domain, cloud) | | | | |
| R15 | Domain or SSL certificate expires | | | | |
| R16 | Run out of cash / customer pays late / bank issue | | | | |
| R17 | A key vendor shuts down or raises price sharply | | | | |
| R18 | Sudden traffic spike (viral launch) overloads system | | | | |
| R19 | Law or regulation change, privacy complaint, legal notice | | | | |
| R20 | Internet, power, or natural disaster where team lives | | | | |
| R21 | Support overwhelmed (too many tickets) | | | | |
| R22 | Marketplace: sellers or buyers dispute or leave | | | | |
| R23 | Accidental deletion of data or code by a team member | | | | |
| R24 | Poor-quality AI-generated code causes a hidden bug or security hole | | | | |
| R25 | | | | | |

**Q4.2. Which 3 risks worry you most, and why?**
Your answer:

**Q4.3. Has something already gone wrong in the past? What happened and what did you learn?**
Example: *"Last month our database ran out of disk space. We now have alerts."*
Your answer:

**Q4.4. Single points of failure.** List anything where "if this one thing/person fails, we stop."
Example: *"Only Ravi has the production database password."*

| Single point of failure | Fix (backup person, second copy, etc.) | Owner | Due date |
|---|---|---|---|
| | | | |

**[ADVANCED] Q4.5. Prevention.** What do we already do to make each high risk less likely or less harmful?

| Risk ID | Prevention in place (examples: backups, two-step login, alerts, code review, spending caps, tests) | Gap still open | Owner | Due date |
|---|---|---|---|---|
| | | | | |

---

# Part 5: Who and What You Depend On

**Q5.1. List every outside tool or company you rely on.** Include hosting, payments, AI providers, email, app stores, analytics, support, banking, and accounting tools.

| # | Vendor | What it does for you | Importance (1/2/3) | Account owner | Status page link | Contract or plan end date | Backup option if it fails |
|---|---|---|---|---|---|---|---|
| 1 | (Example) AWS / Vercel / other cloud | Hosts app | 1 | | | | Restore to second region or provider |
| 2 | (Example) Stripe / Razorpay / other | Takes card payments | 1 | | | | Second provider or payment links |
| 3 | (Example) OpenAI / Anthropic / other AI | Powers AI features | 2 | | | | Second AI model; feature switch off |
| 4 | (Example) Apple App Store / Google Play | Distributes mobile app | 1 | | | | Web version of the app |
| 5 | (Example) Email service | Sends emails | 2 | | | | Second email provider |
| 6 | (Example) Code host (GitHub etc.) | Stores code | 1 | | | | Offline mirror copy |
| 7 | (Example) Bank | Holds company money | 1 | | | | Second bank account |
| 8 | (Example) Accounting / invoicing tool | Keeps books | 2 | | | | Monthly exports in spreadsheet |
| 9 | (Example) Customer support tool | Handles tickets | 2 | | | | Shared email inbox |
| 10 | (Example) Domain registrar | Owns your web address | 1 | | | | Auto-renew + backup contact |
| 11 | | | | | | | |

**Q5.2. For each Importance 1 vendor, answer these:**

| Vendor | Do we get outage alerts? (Y/N) | Do we have a copy of our data outside this vendor? (Y/N) | Do we have a written uptime promise (SLA)? (Y/N) | Do we know their support contact? (Y/N) |
|---|---|---|---|---|
| | | | | |

**Q5.3. Which vendors could cut you off with little warning?** (payment providers, app stores, AI platforms can suspend accounts)
Example: *"Stripe can hold payouts during a review."*
Your answer:

**Q5.4. What shared accounts, domains, and secrets exist, and where are they stored?** (Do NOT write the secrets here.)
Example: *"Domain at Namecheap, login in team password manager 'Core' vault, recovery codes in safe."*

| Item | Where it is stored | Who can access it (names) | Backup person |
|---|---|---|---|
| Password manager master access | | | |
| Domain registrar | | | |
| Cloud admin account | | | |
| Payment provider admin | | | |
| App store developer accounts | | | |
| AI provider keys | | | |
| Company email admin | | | |
| Bank account | | | |

**[ADVANCED] Q5.5. Vendor exit plans.** For each Importance 1 vendor, write how you would leave it if you had to (shutdown, price jump, account ban, bad support).

| Vendor | Can we export all our data? (how) | Time to move (days) | Replacement vendor(s) | What would it cost? | Who leads the move? |
|---|---|---|---|---|---|
| (Example) Payment provider | Yes, customer and payment export from dashboard | 14 | Second provider | Setup fee + engineer time | Finance Lead |
| | | | | | |

**[ADVANCED] Q5.6. Vendor review.** How often do we check each vendor's health, price, and terms? (Example: "Every 6 months, owner reads the latest terms and status history.")
Your answer:

**[ADVANCED] Q5.7. Vendor "concentration" check.** Is more than half of your critical work on one vendor (same cloud for app, backups, and email)? (Y/N) ______ If Y, what is the plan? ______

**[ADVANCED] Q5.8. Are important contracts and renewals tracked?** Where, and who gets a reminder 60 days before each end date?
Your answer:

---

# Part 6: People, Roles, and Who to Call

**Q6.1. Fill in the Emergency Team.** These are the people who act when something goes wrong. One-person teams: write your name in several rows, and name a trusted outside helper as backup.

| Role | What they do in an emergency | Primary person | Phone / chat | Backup person | Phone / chat |
|---|---|---|---|---|---|
| **Incident Leader** | Makes the final calls, declares "plan activated" | | | | |
| **Technical Lead** | Finds and fixes the technical problem | | | | |
| **Customer Communicator** | Tells customers what is happening | | | | |
| **Finance Lead** | Protects cash, payments, invoices, refunds | | | | |
| **Legal / Privacy Contact** | Decides if laws apply (data breach, etc.) | | | | |
| **Scribe** | Writes down what happened and when | | | | |

**Q6.2. How do we reach each other if normal chat/email is down?**
Example: *"Phone call, then SMS, then personal email. Group chat on Signal as backup."*
Your answer:

**Q6.3. Call tree.** Who calls whom, in order?
Example: *"Whoever notices -> Incident Leader -> Technical Lead -> Customer Communicator -> Finance Lead."*
Your answer:

**Q6.4. What time zones is the team in, and who covers nights and weekends?**
Your answer:

**Q6.5. Who has the authority to spend money in an emergency?** (and what is the limit)
Example: *"Incident Leader, up to $500 without asking anyone."*
Your answer:

**Q6.6. Outside helpers on speed dial.** (freelance developer, lawyer, accountant, security consultant, cloud support)

| Who | What for | Contact | Contract / retainer? (Y/N) |
|---|---|---|---|
| | | | |

**Q6.7. Key-person cover.** For each person whose absence would stop work, who can step in, and is their knowledge written down?

| Person | What only they know/do | Stand-in | Where it is documented |
|---|---|---|---|
| | | | |

**[ADVANCED] Q6.8. On-call.** Who is "on call" (the person who gets alerted first) and when?
Example: *"Weekly rotation. Handover on Mondays at 10:00. On-call person responds to SEV 1 within 15 minutes, 24/7; SEV 2 within working hours."*

| Week or period | On-call person | Backup | Handover done? |
|---|---|---|---|
| | | | |

**[ADVANCED] Q6.9. What alerts wake the on-call person up?** (only the ones that truly need action)
Example: *"Site down, payments failing, error rate above 5%, AI cost above hard limit."*
Your answer:

**[ADVANCED] Q6.10. Rest and fairness.** What is the rule after a long night incident? (Example: "The on-call person starts late the next day.")
Your answer:

**[ADVANCED] Q6.11. Access check for new and leaving people.** Who gives and removes access when someone joins or leaves, and how fast? (Example: "Remove all access within 1 hour of leaving; owner signs the checklist.")
Your answer:

**[ADVANCED] Q6.12. Where and how do we work if home internet, power, or our usual place fails?**
Example: *"Mobile hotspot as backup internet. Co-working day pass. Laptops charged. Two people in different cities."*
Your answer:

---

# Part 7: Recovery Playbooks (Step by Step)

**How to use this part:** Write one short playbook for **every risk scoring 13 or higher** in Part 4, and always for the **five core playbooks** below (P-A to P-E). Copy the playbook template for each extra risk.

## When do we "activate" this plan?

**Q7.1. Complete these trigger rules.** If any is true, the Incident Leader declares an incident.

| Trigger | Your threshold |
|---|---|
| Product down for more than | (Example: 10 minutes) |
| Payments failing for more than | (Example: 15 minutes) |
| Customer data possibly exposed | (Example: any suspicion at all) |
| Error rate above | (Example: 5% of requests) |
| Number of customer complaints in an hour | (Example: 5) |
| AI giving unsafe output | (Example: any confirmed case) |
| Bank or payment account frozen | (Example: immediately) |

**Q7.2. Severity levels**

| Level | Meaning | Response time | Who is told |
|---|---|---|---|
| **SEV 1** | Critical function down or data at risk | Respond within 15 min | All team, customers |
| **SEV 2** | Important function down or partly working | Respond within 1 hour | Team, affected customers |
| **SEV 3** | Small problem, workaround exists | Next working day | Owner only |

Adjust the times if needed. Your answer (changes only):

**Q7.3. Stand-down: when is an incident over?** (How do we decide to go back to normal, and who says so?)
Example: *"Incident Leader declares it over when the Critical functions pass their checks for 30 minutes, customers are told, and open tasks have owners."*
Your answer:

**Q7.4. After every incident (SEV 1 and SEV 2): the review.** Within how many days do we hold a short, blame-free review, and where do we save the notes?
Example: *"Within 5 working days. Notes in the incident log. We list: what happened, timeline, cause, what worked, what to fix, owner, due date."*
Your answer:

## Playbook template (copy this for each risk)

```
### Playbook: [Risk name]
- Linked risk ID: R__
- Severity if it happens: SEV _
- Owner: [Name]
- How we notice it (alarm, customer report, vendor alert): 
- First 15 minutes (stop the bleeding):
  1.
  2.
  3.
- Next 1 hour (restore the minimum service):
  1.
  2.
- Customer message to send (see Part 12): [template name]
- Done when (how we know it is fixed): 
- After it is fixed (clean up, write report): 
- Last tested on: [date]   Result: [pass/fail + notes]
```

## P-A (Core): App or website is down

- Linked risk: R1, R18
- Owner:
- **How we notice:** (Example: uptime monitor texts us)
- **First 15 minutes:** (Example: 1. Check vendor status page. 2. Check last release. 3. Post "investigating" on status page.)
  1.
  2.
  3.
- **Next 1 hour:**
  1.
  2.
- **Roll back plan:** How do we undo the last release? (Example: "Run `deploy rollback` in the dashboard.")
- **Done when:**
- **After:**

## P-B (Core): Bad release or AI-generated code causes a bug

- Linked risk: R3, R24
- Owner:
- **How we notice:**
- **First 15 minutes:** (Example: turn off the feature flag; roll back the release)
  1.
  2.
- **Next 1 hour:**
  1.
  2.
- **Who reviews AI-written code before it ships?** (Example: "A second human must approve every change to payments, login, or data.")
- **Done when:**

## P-C (Core): Data loss, corruption, or accidental deletion

- Linked risk: R2, R23
- Owner:
- **First 15 minutes:** (Example: stop writes, take a snapshot, do not delete anything else)
  1.
  2.
- **Restore steps:** (Example: restore latest backup into a copy, check, then switch over)
  1.
  2.
  3.
- **Which backup do we use, and how old is it?**
- **Done when:**

## P-D (Core): Security incident (hack, ransomware, leaked keys, data breach)

- Linked risk: R4, R5
- Owner:
- **First 15 minutes:** (Example: 1. Change passwords and rotate keys. 2. Remove access for suspect accounts. 3. Keep evidence, do not wipe machines. 4. Call Legal/Privacy contact.)
  1.
  2.
  3.
- **Is personal data involved? Who decides?**
- **Legal clock:** Under GDPR, the authority usually must be told **within 72 hours** of becoming aware of a personal-data breach, unless it is unlikely to risk people's rights. Your lawyer decides. Record the time you became aware: ______
- **Who do we notify?** (customers, authority, payment provider, insurance, police)
- **Done when:**

## P-E (Core): Payment provider problem (outage, account frozen, fraud spike)

- Linked risk: R6, R7
- Owner:
- **First 15 minutes:** (Example: check provider status, switch to payment links, pause promotions)
  1.
  2.
- **Backup provider or method:**
- **How do we make sure no customer is charged twice or not charged at all?**
- **Who contacts the provider and with what information?**
- **Done when:**

## [ADVANCED] Ready-Made Playbooks P-F to P-Q

Each playbook has **suggested first steps** in `(brackets)`. Keep, change, or replace them to fit your project. If a playbook does not apply, write `N/A: reason` in the Owner line. Every playbook needs: **Owner, First 15 minutes, Next 1 hour, Done when, Last tested.**

### P-F: AI provider outage, slowdown, or rate limit (Risks R8, R11)
- Severity: SEV 2 (SEV 1 if the core product depends on it)  |  Owner:
- **How we notice:** (error rate on AI calls, vendor status page, customer reports)
- **First 15 minutes:** (1. Confirm on the vendor status page. 2. Switch to backup model using the config switch. 3. If no backup, show "AI is busy, try again soon" and queue requests.)
  1.
  2.
  3.
- **Next 1 hour:** (Check quality of the backup model on 5 test cases. Raise limits or contact vendor support.)
  1.
  2.
- **Done when:** (Error rate back to normal for 30 minutes. Queue emptied. Backup switched off if desired.)
- **Last tested:** ______

### P-G: AI gives harmful, wrong, or unsafe output (Risks R9, R24)
- Severity: SEV 1 if harm to a person, money, or data; otherwise SEV 2  |  Owner:
- **How we notice:** (customer report, feedback button, monitoring, review of samples)
- **First 15 minutes:** (1. Turn off the AI feature or agent action using the off switch. 2. Save the bad examples and logs. 3. Stop any automatic actions the AI could take.)
  1.
  2.
  3.
- **Next 1 hour:** (Find what changed: prompt, model version, data, tool permissions. Roll back the last change. Add the bad case to the test set.)
  1.
  2.
- **Customers affected?** (List, correct the harm, apologize, see Template 4.)
- **Done when:** (Fix tested on the bad cases, human review on for first week back, written report done.)
- **Last tested:** ______

### P-H: Cost spike or bill shock (Risks R10, R16)
- Severity: SEV 2  |  Owner:
- **How we notice:** (budget alert at 80% and 100%, daily cost report)
- **First 15 minutes:** (1. Find the biggest cost source in the billing dashboard. 2. Pause the runaway job or lower the limit. 3. Rotate keys if abuse is suspected.)
  1.
  2.
  3.
- **Next 1 hour:** (Set a hard cap. Check for leaked keys or an AI agent in a loop. Estimate the extra cost and tell the Finance Lead.)
  1.
  2.
- **Done when:** (Costs back to normal, cap in place, cause written down.)
- **Last tested:** ______

### P-I: Key person unavailable or leaves suddenly (Risk R13)
- Severity: SEV 2  |  Owner:
- **First 15 minutes:** (1. Try every contact in the call tree. 2. Name the stand-in from Q6.7. 3. List what only that person controls.)
  1.
  2.
- **Next 1 hour:** (Secure accounts: reset shared access, keep their work safe, check scheduled jobs and pending payments.)
  1.
  2.
- **If they have left:** (Remove their access within 1 hour, collect devices and keys, move their accounts to the company, document their knowledge.)
- **Done when:** (Stand-in confirmed, access list updated, plan updated.)
- **Last tested:** ______

### P-J: Lost access to an important account (email, cloud, domain, code host, app store, bank) (Risks R5, R14)
- Severity: SEV 1 if it blocks a Critical function  |  Owner:
- **First 15 minutes:** (1. Check the recovery options listed in Q5.4. 2. Contact a second admin. 3. Contact the vendor's support with proof of ownership.)
  1.
  2.
- **Next 1 hour:** (If a hacker has access: change passwords, remove unknown devices, check for changed payment or payout details.)
  1.
  2.
- **Prevention reminders:** (Two admins per account. Recovery codes stored offline. Company email, not personal email, as owner.)
- **Done when:**
- **Last tested:** ______

### P-K: App store rejects, suspends, or removes the app (Risk R12)
- Severity: SEV 1 if mobile is the main way customers use the product  |  Owner:
- **First 15 minutes:** (1. Read the exact reason in the store notice. 2. Save screenshots. 3. Tell customers the web version still works.)
  1.
  2.
- **Next 1 hour:** (Fix the issue or write an appeal. Submit the new build. Ask the store for an expedited review if allowed.)
  1.
  2.
- **Backup path:** (Web app, direct download where allowed, email-based access.)
- **Done when:** (App is live again; cause written down; a pre-submission checklist added to release steps.)
- **Last tested:** ______

### P-L: Domain, SSL certificate, or key subscription expires (Risk R15)
- Severity: SEV 1  |  Owner:
- **First 15 minutes:** (1. Renew immediately; pay with a backup card if needed. 2. Check DNS. 3. Post status.)
  1.
  2.
- **Next 1 hour:** (Confirm site, email, and app all work again. Clear caches. Check email deliverability.)
  1.
  2.
- **Prevention:** (Auto-renew on; two reminder dates (60 and 14 days before); card on file not about to expire; shared calendar.)
- **Done when:**
- **Last tested:** ______

### P-M: Traffic spike or overload (Risk R18)
- Severity: SEV 2 (SEV 1 on launch day)  |  Owner:
- **First 15 minutes:** (1. Turn on caching / scale up. 2. Turn off heavy non-essential features. 3. Switch on a waiting page if needed.)
  1.
  2.
- **Next 1 hour:** (Raise limits with the cloud provider. Find the slow part. Block abusive traffic.)
  1.
  2.
- **Done when:** (Response times normal for 30 minutes. Capacity plan updated.)
- **Last tested:** ______

### P-N: Support overwhelmed (Risk R21)
- Severity: SEV 2  |  Owner:
- **First 15 minutes:** (1. Post a banner and auto-reply explaining delays. 2. Put the top three questions on a help page. 3. Ask the backup person to help.)
  1.
  2.
- **Next 1 hour:** (Sort tickets: money problems and access problems first. Use saved replies. Assign owners.)
  1.
  2.
- **Done when:** (Backlog under target for 2 days. Fixes for the top causes planned.)
- **Last tested:** ______

### P-O: Bank account frozen, or cash is about to run out (Risk R16)
- Severity: SEV 1  |  Owner (Finance Lead):
- **First 15 minutes:** (1. Contact the bank and ask what documents they need. 2. Switch to the second account or card. 3. List payments due in the next 14 days.)
  1.
  2.
- **Next 1 hour:** (Tell payroll and key vendors early if payments will be late. Delay non-essential spending. Check the payment provider payout settings.)
  1.
  2.
- **Cash rescue options:** (Annual plan offer, invoice customers early, delay a hire, ask investors, short loan.)
- **Done when:**
- **Last tested:** ______

### P-P: Billing error (double charge, wrong amount, missed charge, wrong tax) (Risks R6, R7)
- Severity: SEV 1 if many customers are affected  |  Owner (Finance Lead):
- **First 15 minutes:** (1. Pause automatic billing runs. 2. Count who is affected. 3. Take a snapshot of the data.)
  1.
  2.
- **Next 1 hour:** (Fix the cause. Refund or correct in batches. Check totals against the payment provider report. Send Template 3.)
  1.
  2.
- **Reconcile:** (Match every corrected charge to a bank or provider record. Keep a list with date, customer, amount, action.)
- **Done when:** (Zero open affected customers; totals match; billing run restarted and watched.)
- **Last tested:** ______

### P-Q: Marketplace dispute, fraud, or seller/buyer crisis (Risk R22) (use `N/A` if not a marketplace)
- Severity: SEV 2  |  Owner:
- **First 15 minutes:** (1. Freeze payouts for the affected sellers. 2. Hold the disputed funds. 3. Collect messages and order records.)
  1.
  2.
- **Next 1 hour:** (Contact both sides. Apply the written dispute rules. Refund if the rules say so.)
  1.
  2.
- **Done when:** (Both sides told the result; money moved or returned; rules improved if a gap was found.)
- **Last tested:** ______

## Extra Playbooks (copy the template above for each)

| Risk ID | Playbook title | Owner | Written? (Y/N) | Last tested |
|---|---|---|---|---|
| | | | | |

---

# Part 8: Billing, Finance, and Money Continuity

Money problems can end a young company faster than technical ones.

**Q8.1. How does money come in?** (subscriptions, one-time sales, marketplace fees, invoices)
Example: *"Monthly subscriptions via Stripe; enterprise invoices paid by bank transfer."*
Your answer:

**Q8.2. What is your billing cycle?** (when are customers charged)
Example: *"Charged on signup date each month; annual plans on anniversary."*
Your answer:

**Q8.3. How many months of cash do you have today ("runway")?**
Your answer:

**Q8.4. Minimum monthly cost to stay alive** (servers, AI, salaries/contractors, tools, taxes)

| Cost | Per month |
|---|---|
| Hosting / cloud | |
| AI usage | |
| Tools and subscriptions | |
| People / contractors | |
| Taxes, legal, accounting | |
| Other | |
| **Total** | |

**Q8.5. What happens to billing if the billing system is down?**
Example: *"We stop charging, keep service on, and run a catch-up charge within 24 hours. No customer loses access because of our error."*
Your answer:

**Q8.6. Billing safeguards**

| Question | Your answer |
|---|---|
| How do we check each month that charges match what customers owe? | (Example: "Monthly report vs bank deposits") |
| How do we avoid double charging? | (Example: "Idempotency keys; daily check") |
| Who can issue refunds, and what is the limit? | |
| How are failed payments retried and for how long? | (Example: "Retry at day 1, 3, 7; then pause account") |
| What is our refund and chargeback process? | |
| How do we keep invoices and receipts for the legal period? | (Example: "7 years in accounting tool + yearly export") |

**Q8.7. Bank and cash backups**
- Do we have a **second bank account or card** in case one is frozen? (Y/N) ______
- Do two people have access to the bank? (Y/N) ______
- Is there an **emergency cash buffer**? How much? ______
- Which payments are due on fixed dates (salaries, rent, tax, vendor renewals)? ______

**Q8.8. Cost-spike protection (especially AI and cloud)**

| Question | Your answer |
|---|---|
| Do we have budget alerts? At what amounts? | (Example: "80% and 100% of $2,000 monthly") |
| Do we have a hard spending cap or auto-shutdown? | |
| Who gets the alert and what do they do? | |
| What is the first thing we switch off to save money? | (Example: "Free-tier AI features") |

**Q8.9. Tax and legal money duties** (sales tax / VAT, payroll tax, company filings)
Example: *"VAT filed quarterly by our accountant, reminders in calendar."*
Your answer:

**Q8.10. If we lose access to financial records, how do we rebuild them?**
Example: *"Bank statements + payment provider exports + monthly accounting backup."*
Your answer:

**Q8.11. Marketplace only: how are seller payouts and buyer refunds protected during an outage?**
Example: *"Payouts pause automatically; no payout is sent until the system is verified."*
Your answer (or `N/A: not a marketplace`):

## 8B. [ADVANCED] Revenue Protection and Recovery

**[ADVANCED] Q8.12. Plans and prices.** List what customers can buy.

| Plan / product | Price | Billing period | Free trial? | Who can change the price? |
|---|---|---|---|---|
| (Example) Starter | $9 | Monthly | 14 days | Product lead + Finance Lead |
| | | | | |

**[ADVANCED] Q8.13. Failed-payment recovery ("dunning").** What happens, step by step, when a card payment fails?
Example: *"Day 0: auto retry + email. Day 3: retry + email. Day 7: final retry, warning in app. Day 10: pause account (data kept for 30 days). Day 40: close account."*
Your answer:

**[ADVANCED] Q8.14. Do customers keep access during a billing-system outage or a failed-payment period?** For how long?
Example: *"Yes. We never cut access because of our own billing outage. For customer card failures, access continues 7 days."*
Your answer:

**[ADVANCED] Q8.15. Missed revenue catch-up.** After an outage, how do we find and collect charges that were missed?
Example: *"Run a report of active customers with no charge this period; charge or invoice within 3 days; tell customers first."*
Your answer:

**[ADVANCED] Q8.16. Invoices.** How are invoices made, numbered, and sent? What if the invoice tool is down?
Example: *"Auto-generated by the billing tool with continuous numbering. If down, we issue invoices from a spreadsheet template and enter them later."*
Your answer:

**[ADVANCED] Q8.17. Refund and credit rules.**

| Situation | What we do | Who approves | Limit |
|---|---|---|---|
| Customer asks within 14 days | (Example: Full refund) | Support | $100 |
| Outage longer than our promise | (Example: Credit of 1 day per hour down, up to 30 days) | Finance Lead | |
| Billing mistake by us | (Example: Refund plus apology) | Finance Lead | |
| Suspected fraud | (Example: Refund, block, report to provider) | Finance Lead | |

**[ADVANCED] Q8.18. Chargebacks (a customer's bank takes the money back).**

| Question | Your answer |
|---|---|
| Who sees chargeback alerts? | |
| How many days do we have to answer? | (Check with your payment provider) |
| What evidence do we keep? (signup record, usage logs, emails, terms accepted) | |
| What chargeback rate would make us act? | (Example: 0.5% of payments) |
| What would we do if the rate stays high? | (Example: stricter signup checks, clearer descriptor, faster refunds) |

**[ADVANCED] Q8.19. Reconciliation (checking that records match).**

| Check | How often | Who | Where the result is saved |
|---|---|---|---|
| Payment provider report = bank deposits | Weekly | | |
| Billing system = payment provider | Weekly | | |
| Billing system = accounting books | Monthly | | |
| Active customers = customers being charged | Monthly | | |
| Refunds and credits = approved list | Monthly | | |

**[ADVANCED] Q8.20. Month-end and year-end close.** What are the steps, who does them, and what is the backup plan if that person is away?
Example: *"Day 1 to 3: export reports. Day 4: reconcile. Day 5: accountant review. Backup: Meera."*
Your answer:

**[ADVANCED] Q8.21. Separation of duties.** Does anyone both create and approve the same payment or refund? (Y/N) ______ If yes, what is the safeguard? ______

**[ADVANCED] Q8.22. Money KPIs we watch weekly** (so we notice trouble early)

| KPI | Today | Alert level | Who watches |
|---|---|---|---|
| Cash in bank | | (Example: below 3 months of costs) | |
| Monthly recurring revenue | | (Example: drop of 10%) | |
| Failed payment rate | | (Example: above 5%) | |
| Refund rate | | (Example: above 3%) | |
| Chargeback rate | | (Example: above 0.5%) | |
| Customers who cancel each month | | (Example: above 5%) | |
| Cloud + AI cost per customer | | (Example: above $2) | |

**[ADVANCED] Q8.23. Cash scenarios.** How many months can we last if:

| Scenario | Months of cash left |
|---|---|
| Revenue drops 30% | |
| Payment provider holds our payouts for 30 days | |
| AI and cloud costs double | |
| A large customer stops paying | |

**[ADVANCED] Q8.24. Who is allowed to see and change financial data and payment settings?** (Name each person and their access level. Remove access when roles change.)
Your answer:

**[ADVANCED] Q8.25. Accounting backup.** Where are books, invoices, receipts, contracts, and bank statements backed up, and how often? Can we rebuild books if the accounting tool is unavailable?
Your answer:

**[ADVANCED] Q8.26. Tax and filing calendar**

| Duty | Due date | Owner | Reminder set? |
|---|---|---|---|
| (Example) Sales tax / VAT return | Quarterly | | |
| (Example) Payroll taxes | Monthly | | |
| (Example) Company annual filing | Yearly | | |
| | | | |

---

# Part 9: Data Backup and Recovery

**Q9.1. List every important kind of data and how it is protected.**

| Data | Where it lives | Backup method | How often | Kept how long | Stored where (different place from the original?) | Last restore test |
|---|---|---|---|---|---|---|
| Customer accounts and data | (Example: main database) | Automatic snapshots | Every hour | 30 days | Different region | |
| Payments and invoice records | | | | | | |
| Source code | | | | | | |
| AI prompts, agent instructions, configurations | | | | | | |
| AI knowledge data (documents, embeddings) | | | | | | |
| Uploaded files (images, documents) | | | | | | |
| Secrets and keys (list only, not the values) | | | | | | |
| Design files and documents | | | | | | |
| Accounting records | | | | | | |
| Support conversations | | | | | | |

**Q9.2. The 3-2-1 check.** Do we have **3** copies, on **2** different types of storage, with **1** copy in a **different location**? (Y/N) ______ If N, what is the plan? ______

**Q9.3. Are backups protected from accidental or malicious deletion?** (Example: "Backups are read-only for 30 days.")
Your answer:

**Q9.4. When did we last try restoring a backup, and did it work?**
Example: *"15 Sep 2026, restored staging database in 40 minutes. Passed."*
Your answer:

**Q9.5. Data we collect that is personal or sensitive** (names, emails, addresses, IDs, payment details)
Your answer:

**Q9.6. Is test or AI-development data free of real customer data?** (Y/N) ______ If N, how is it protected? ______

---

# Part 10: AI-Specific Continuity

Skip questions that do not apply, but write `N/A: reason`.

**Q10.1. Where do we use AI?** (tick all)
- [ ] AI helps us write code (development)
- [ ] AI features inside the product for customers
- [ ] AI agents that take actions (send emails, update records, issue refunds)
- [ ] AI for support, marketing, or finance work
- [ ] Other: ______

**Q10.2. AI vendors and models we rely on**

| Use | Provider / model | What if it is down? (backup model, switch off, queue) | What if its price or rules change? |
|---|---|---|---|
| | | | |

**Q10.3. Can we switch to a backup AI model quickly?** How long does it take, and who does it?
Example: *"Yes, via a config switch. 15 minutes. Technical Lead."*
Your answer:

**Q10.4. Is there an "off switch"?** Can we disable AI features instantly without redeploying the app? (Y/N) ______ Where is the switch? ______

**Q10.5. Where are prompts, agent instructions, and settings stored, and are they version-controlled?** (so you can undo a bad change)
Your answer:

**Q10.6. Human checks.** Which AI actions need a human to approve before they happen?
Example: *"Refunds over $50, any message to all customers, any database change, any payments code."*
Your answer:

**Q10.7. What limits keep an AI agent from causing big damage?** (spending limit, permission limit, rate limit, "read only" mode)
Your answer:

**Q10.8. How do we notice when AI output gets worse, wrong, or unsafe?** (testing set, user feedback button, monitoring)
Your answer:

**Q10.9. What is the plan when AI gives a harmful or wrong answer to a customer?**
Example: *"Turn off feature, apologize, review logs, fix, test, re-enable with human review."*
Your answer:

**Q10.10. Do we send customer data to AI vendors? Is it allowed in our privacy promise and their terms?** (Y/N and notes)
Your answer:

**Q10.11. AI-written code safety.**

| Question | Your answer |
|---|---|
| Does a human review all AI-written code before release? | |
| Are automated tests run before every release? | |
| Is there a scan for security holes and leaked keys? | |
| Can we roll back a release in minutes? | |

## 10B. [ADVANCED] AI Systems in Depth

**[ADVANCED] Q10.12. AI inventory.** List every AI feature or agent that runs in production.

| AI feature / agent | What it does | Model and version | What data it sees | What actions it can take | Owner | Off switch location |
|---|---|---|---|---|---|---|
| (Example) Support reply drafter | Drafts replies for staff to approve | (model name + version) | Ticket text | None (draft only) | | Feature flag `ai_support` |
| | | | | | | |

**[ADVANCED] Q10.13. Permissions ("least power").** For each agent that can take actions, what is the most damage it could do, and what stops it?
Example: *"Refund agent can refund up to $50 per case and $500 per day. Anything above needs a human."*
Your answer:

**[ADVANCED] Q10.14. Model version control.** Do we pin to a specific model version, and how do we find out when a model is retired or changed?
Example: *"We pin versions. Owner subscribes to vendor deprecation notices. We re-test 30 days before any retirement."*
Your answer:

**[ADVANCED] Q10.15. Test set (evaluation).** Do we keep a set of example questions with the expected good answers, and do we run it before every change to prompts, models, or data?
Example: *"Yes, 50 cases in the repo. Must pass at least 95% before release."*
Your answer:

**[ADVANCED] Q10.16. Change control for AI.** Who can change prompts, models, tools, and knowledge data in production, and how is it approved and recorded?
Your answer:

**[ADVANCED] Q10.17. Logs and traceability.** Do we keep a record of what the AI was asked, what it answered, and what it did (without storing secrets or more personal data than needed)? How long?
Your answer:

**[ADVANCED] Q10.18. Quality levels during an outage ("graceful fallback").**

| Level | What customers get | When we use it |
|---|---|---|
| Full | All AI features with the main model | Normal |
| Reduced | Backup model or smaller model, slower or simpler | Main model down or limited |
| Basic | AI off; non-AI version of the feature | Both models down or unsafe |
| Paused | Feature hidden, clear message | Safety problem |

Adjust to fit your product. Your changes:

**[ADVANCED] Q10.19. Data sent to AI providers.** Do they keep it, train on it, or store it? Which region? Do we have a signed data-protection agreement? Can we switch off storage or training?
Your answer:

**[ADVANCED] Q10.20. Prompt injection and misuse.** Could a customer or an outside document trick the AI into leaking data or taking a bad action? What stops it?
Example: *"AI never sees other customers' data. Outside text is treated as data, not instructions. Actions need approval."*
Your answer:

**[ADVANCED] Q10.21. Customer honesty.** Do customers know when they are talking to AI or seeing AI-made content? Where do we say so?
Your answer:

**[ADVANCED] Q10.22. AI rules and laws.** Are there AI-specific rules we must follow (for example, transparency duties or rules for certain uses in the EU or your industry)? Who checks? (Not legal advice: ask a professional.)
Your answer:

**[ADVANCED] Q10.23. AI in development.** When AI writes or changes code, what keeps us safe?

| Safeguard | In place? (Y/N) | Notes |
|---|---|---|
| Human review for every change | | |
| Extra review for payments, login, permissions, data deletion | | |
| Automated tests and security scans before release | | |
| AI tools cannot access production data or secrets | | |
| AI tools cannot deploy to production without human approval | | |
| Prompts and agent instructions used in development are saved | | |
| Every change can be traced to a person who approved it | | |

**[ADVANCED] Q10.24. AI cost controls.**

| Control | Setting |
|---|---|
| Daily and monthly spend alert | |
| Hard spending cap per project key | |
| Maximum tokens or requests per customer | |
| Loop protection (agent stops after N steps) | |
| Who is alerted | |

**[ADVANCED] Q10.25. What is our "AI kill switch" drill?** Who flips it, how long does it take, and how do we confirm that it worked?
Your answer:

---

# Part 11: Customer Milestones and Stage Gates (Customer 1 to Customer 500)

Your risk changes as customers grow. Fill in this table so the plan grows with you. (The go/no-go checks for each stage are in Part 2, Q2.4 to Q2.9. This part tracks **what changes** and **how you measure it**.)

**Q11.1. What changes at each milestone?**

| Milestone | New risks to expect | What we must have in place | Done? (Y/N) | Date |
|---|---|---|---|---|
| **Before launch** | Launch bugs, payment errors, no support process | Backups tested, rollback tested, payment test passed, status page ready, support inbox ready | | |
| **Customer 1 to 10** | Billing mistakes, onboarding failures | Manual check of every payment; owner reads every support message | | |
| **Customer 11 to 50** | Support delays, small outages hurt trust | Uptime monitoring and alerts, support reply target, refund policy | | |
| **Customer 51 to 100** | Chargebacks, abuse, data requests | Fraud checks, privacy request process, written status updates | | |
| **Customer 101 to 250** | Slowdowns, rising AI and cloud costs, key person overload | Cost alerts, backup person per role, capacity check, quarterly restore test | | |
| **Customer 251 to 500** | Bigger customers ask for proof of security and reliability | Written security policy, incident log, vendor list, customer-ready summary of this plan | | |
| **Customer 500+** | Formal audits, 24/7 expectations | Upgrade this plan: dedicated on-call, formal audit (SOC 2 or ISO 27001), second region | | |

**Q11.2. Our service promise to customers (uptime target and support reply time)**
Example: *"99.5% uptime. First support reply within 1 business day."*
Your answer:

**Q11.3. What do we do for a customer who suffers a bad outage?** (apology, credit, refund)
Your answer:

**Q11.4. How many customers do we have today?** ______ **How many do we expect in 3 months?** ______

**Q11.5. What will break first if we grow 10x?**
Your answer:

**[ADVANCED] Q11.6. Milestone scorecard.** Fill in the numbers at each milestone so you can see trends.

| Measure | Launch | 10 customers | 50 | 100 | 250 | 500 |
|---|---|---|---|---|---|---|
| Date reached | | | | | | |
| Uptime that month (%) | | | | | | |
| Number of incidents (SEV 1 / 2 / 3) | | | | | | |
| Average support reply time | | | | | | |
| Failed payment rate (%) | | | | | | |
| Refunds and chargebacks (count) | | | | | | |
| Monthly cloud + AI cost | | | | | | |
| Cost per customer | | | | | | |
| Months of cash left | | | | | | |
| Backup restore test passed? | | | | | | |

**[ADVANCED] Q11.7. Customer concentration.** Do a few customers make up a big share of revenue? (Example: "Top 3 customers = 40%".) What happens if one leaves or has a bad outage?
Your answer:

**[ADVANCED] Q11.8. Larger customers will ask "Can you prove you are reliable?"** What can we show today?
Example: *"Uptime history, summary of this plan, backup test date, privacy policy, vendor list."*
Your answer:

**[ADVANCED] Q11.9. Early warning signs.** What small signals tell us a problem is starting?

| Signal | Where we see it | What we do |
|---|---|---|
| (Example) Support tickets double in one day | Support tool | Check status, post notice |
| (Example) Slow page loads | Monitoring | Run P-M |
| (Example) Failed payments rising | Payment dashboard | Run P-E or P-P |
| | | |

**[ADVANCED] Q11.10. Customer feedback loop.** How do customers tell us about problems, and how do we show we listened?
Your answer:

**[ADVANCED] Q11.11. Who owns the customer promise and its updates as we grow?** (uptime, support, refund, data protection)
Your answer:

---

# Part 12: Communication Plan

**Q12.1. Who needs to hear from us during an incident, and how?**

| Audience | What they need to know | How we reach them | Who sends it | How soon (SEV 1) |
|---|---|---|---|---|
| Customers | What is wrong, what to do, next update time | Status page, in-app banner, email | Customer Communicator | Within 30 min |
| Team | What to do, who is leading | Chat / phone | Incident Leader | Immediately |
| Investors / partners | Impact, plan, ETA | Email | Incident Leader | Within 4 hours |
| Payment provider / vendors | Details, request help | Support ticket / call | Technical or Finance Lead | As needed |
| Regulators (if data breach) | Required facts | Official form | Legal / Privacy Contact | Within legal deadline |
| App stores (if needed) | Issue and fix | Developer console | Technical Lead | As needed |

**Q12.2. Where is our status page?** (link) ______ **Who can update it?** ______ **Is it hosted somewhere separate from our product?** (Y/N) ______

**Q12.3. Message templates.** Write short messages now, so you don't have to think during a crisis.

**Template 1: "We are looking into it"**
Example: *"We are aware that [problem]. We are working on it. Next update by [time]."*
Your answer:

**Template 2: "Fixed"**
Example: *"[Problem] is fixed as of [time]. Cause: [short]. Your data is [safe / affected]. We are sorry."*
Your answer:

**Template 3: "Billing problem"**
Example: *"You may see a wrong or delayed charge from [date]. We will correct it by [date]. No action needed."*
Your answer:

**Template 4: "Data incident"**
Example: *"We found that [what happened]. This affected [who/what]. Steps we took: [...]. What you should do: [...]. Contact: [...]."*
Your answer:

**Q12.4. Rules for all messages**
- Say what happened in plain words, no blame, no guessing.
- Give the **time of the next update**.
- Never promise a fix time you cannot keep.
- Legal/Privacy contact approves any data-incident message.

**Q12.5. Who handles press, social media, or angry public posts?**
Your answer:

---

# Part 13: Legal, Insurance, and Compliance

Answer **Yes / No / Not sure** and write who will check anything "Not sure." This is a checklist, **not legal advice**; ask a qualified professional for your situation. Parts 13B and 13C cover insurance and contracts.

| # | Question | Yes / No / Not sure | Notes or owner |
|---|---|---|---|
| Q13.1 | Do we handle personal data of people in the EU/UK (GDPR)? | | |
| Q13.2 | Do we handle data of California residents or other US state privacy laws (CCPA/CPRA)? | | |
| Q13.3 | Do we know how fast we must report a data breach? (GDPR: 72 hours to authority in most cases) | | |
| Q13.4 | Do we have a way to handle customer requests (see, fix, delete their data)? | | |
| Q13.5 | Do we take card payments? Do we only use a provider that handles card data (so card numbers never touch our servers)? (PCI-DSS) | | |
| Q13.6 | Do we keep card numbers anywhere in our logs, files, or chats? (Should be NO) | | |
| Q13.7 | Do customers or investors expect SOC 2 or ISO 27001? When? | | |
| Q13.8 | Do we have written security basics (access rules, password manager, 2-step login)? | | |
| Q13.9 | Do we have contracts or terms with customers that promise uptime, refunds, or data protection? | | |
| Q13.10 | Do we have contracts (DPA) with vendors that handle customer data, including AI providers? | | |
| Q13.11 | Do we have insurance (cyber, business)? | | |
| Q13.12 | Are there special rules in our industry (health, finance, children)? | | |
| Q13.13 | Where must data be stored (country restrictions)? | | |
| Q13.14 | Do we keep records long enough, and delete them when required? | | |

**Q13.15. Which standards might we be asked about later?** (tick)
- [ ] GDPR / UK GDPR
- [ ] CCPA / CPRA
- [ ] PCI-DSS
- [ ] SOC 2 (Availability and Security)
- [ ] ISO 27001
- [ ] ISO 22301 (business continuity)
- [ ] Other: ______

**Q13.16. Legal / compliance contact (name and contact):** ______

## 13B. [ADVANCED] Insurance

**[ADVANCED] Q13.17. What insurance do we have or need?**

| Type | What it covers (plain words) | Do we have it? (Y/N/Not sure) | Provider and policy end date | Amount covered | Who to call for a claim |
|---|---|---|---|---|---|
| Cyber insurance | Costs of hacks, data breaches, ransomware, outage response | | | | |
| Professional / tech errors and omissions | Claims that our product caused a customer's loss | | | | |
| General business liability | Injury or property claims | | | | |
| Business interruption | Lost income after a covered event | | | | |
| Crime / fraud cover | Theft by staff, payment fraud, social-engineering fraud | | | | |
| Directors and officers (D&O) | Claims against leaders | | | | |
| Key-person cover | Money if a key person is lost | | | | |

**[ADVANCED] Q13.18. Insurance basics:** When should we call the insurer after an incident (often *immediately* or within a few days)? Who calls?
Your answer:

**[ADVANCED] Q13.19. Are we required by customers, investors, or contracts to hold specific insurance?** (Y/N and details) ______

## 13C. [ADVANCED] Contracts and Promises (SLAs)

**[ADVANCED] Q13.20. What have we promised customers in writing?**

| Promise | Where written (terms, contract, website) | Number or detail | What happens if we miss it? (credit, refund) |
|---|---|---|---|
| Uptime | | (Example: 99.5% monthly) | |
| Support response time | | | |
| Data protection and location | | | |
| Data return or deletion when they leave | | | |
| Refund policy | | | |
| Maximum liability | | | |

**[ADVANCED] Q13.21. What have vendors promised us (their SLAs), and does it cover what we promised customers?**
Example: *"Our cloud promises 99.9%. We promise customers 99.5%. OK."*
Your answer:

**[ADVANCED] Q13.22. Does any contract include "force majeure" (events outside our control) or a right for customers to end the contract after repeated outages?** Where is it written, and who understands it? ______

**[ADVANCED] Q13.23. Customer data agreements.** Do we have signed data processing agreements (DPA) with customers who ask and with every vendor handling their data? Where are they stored? ______

**[ADVANCED] Q13.24. Records of incidents.** Who keeps the incident log, and where? (Needed for regulators, insurers, auditors, and customers.) ______

**[ADVANCED] Q13.25. Legal hold.** If we get a legal notice or suspect a dispute, who tells the team to stop deleting records, and how? ______

**[ADVANCED] Q13.26. Who is our outside lawyer and accountant, and what do they help with?**

| Name | Firm | Helps with | Contact |
|---|---|---|---|
| | | | |

---

# Part 14: Testing, Review, and Updates

A plan nobody tests is a guess.

**Q14.1. Test schedule**

| Test | What we do | How often | Next date | Owner |
|---|---|---|---|---|
| Backup restore test | Restore a backup to a test system and check it | Every 3 months | | |
| Rollback test | Practice undoing a release | Every 3 months | | |
| Tabletop talk-through | The team reads a scenario aloud and walks through the plan | Every 6 months | | |
| Contact check | Call or message everyone in the call tree | Every 6 months | | |
| AI switch-off / backup model test | Practice the off switch and model switch | Every 6 months | | |
| Payment backup test | Test backup payment path with a small real or test charge | Every 6 months | | |
| Billing reconciliation review | Check Q8.19 results and billing safeguards | Monthly (quick), yearly (deep) | | |
| AI test set run | Run the AI test cases (Q10.15) after any model or prompt change | Every change + every 3 months | | |
| Vendor and contract review | Check vendor health, price, terms, renewals (Q5.6, Q5.8) | Every 6 months | | |
| Access review | Remove old access; confirm two admins per key account | Every 3 months | | |
| Insurance and legal review | Check Part 13 answers and policy end dates | Every 12 months | | |
| Stage gate review | Re-check the gate for the next stage (Q2.4 to Q2.9) | At each milestone | | |
| Full plan review | Read this plan, update answers | Every 6 months, plus after any major event | | |

**Q14.2. Suggested practice scenarios for tabletop talks (pick one each time)**
1. Our main cloud provider is down for 6 hours on launch day.
2. Our payment provider freezes our account on the 1st of the month.
3. The AI provider goes down and our AI feature gets stuck.
4. A team member's laptop with admin access is stolen.
5. A bug double-charges 50 customers.
6. A leaked API key racks up a large AI bill overnight.

**Q14.3. After every incident or test, record what we learned**

| Date | What happened / what we tested | What worked | What did not | Fix to make | Owner | Done? |
|---|---|---|---|---|---|---|
| | | | | | | |

**Q14.4. When must we update this plan?** (tick all that apply and add your own)
- [ ] After any SEV 1 or SEV 2 incident
- [ ] When we add a new vendor or remove one
- [ ] When a team member joins or leaves
- [ ] When we move to the next customer milestone (Part 11)
- [ ] When we change how we take payments
- [ ] When laws or customer promises change
- [ ] Every 6 months at the latest

**Q14.5. Version history**

| Version | Date | What changed | Changed by | Approved by |
|---|---|---|---|---|
| 0.1 | | First draft | | |
| | | | | |

**[ADVANCED] Q14.6. Training and awareness.** How does everyone (including new joiners and contractors) learn this plan?
Example: *"30-minute walk-through when someone joins, a tabletop talk every 6 months, and the Emergency Card is pinned in team chat."*

| Who | What they learn | When | Done? |
|---|---|---|---|
| | | | |

**[ADVANCED] Q14.7. Management review and improvement.** Who reviews results (incidents, tests, gate checks, costs) with leadership, how often, and how do fixes get tracked to done?
Example: *"Priya and Ravi review every quarter. Open fixes live in the project board with owners and dates."*
Your answer:

---

# Part 15: Final Checklist and Sign-Off

## Completion checklist (tick when true)

**Completeness**
- [ ] Every question has an answer, a `TBD (name, date)`, or `N/A: reason`
- [ ] All `[PLACEHOLDERS]` were replaced (search the file for `[`)
- [ ] The Progress tracker at the top is up to date
- [ ] The gate for our current stage (Part 2) is answered, and every Must is Yes or has an approved exception
- [ ] No passwords, keys, or card numbers appear anywhere in this file
- [ ] Every function in Part 3 has an owner, an RTO, and an RPO
- [ ] Every risk scoring 13+ has a playbook in Part 7
- [ ] The five core playbooks (P-A to P-E) are filled in

**People**
- [ ] Every role in Part 6 has a primary and a backup person
- [ ] Everyone named has seen this document
- [ ] Contact details were checked in the last 30 days

**Systems**
- [ ] Backups exist for every item in Part 9 and one restore has been tested
- [ ] There is a rollback path for releases
- [ ] There is an off switch for AI features (if used)
- [ ] There are cost and spending alerts

**Money**
- [ ] A backup payment path exists
- [ ] A second bank account or card exists (or a plan with a date)
- [ ] Billing checks are written (Part 8)

**Communication**
- [ ] A status page exists and is hosted separately from the product
- [ ] The four message templates are written

**Compliance, insurance, and contracts**
- [ ] Part 13 is fully answered, with owners for every "Not sure"
- [ ] Insurance needs were reviewed (13B) and a decision was recorded
- [ ] Customer promises (SLAs) do not exceed what vendors promise us (Q13.21)
- [ ] The breach-reporting clock and decision-maker are written down (P-D)

**Billing and AI (if used)**
- [ ] Reconciliation steps and owners are written (Q8.19)
- [ ] Failed-payment, refund, and chargeback rules are written (Q8.13, Q8.17, Q8.18)
- [ ] AI inventory, kill switch, test set, and spend cap exist (Q10.12 to Q10.25)

**Practice**
- [ ] The first test date is booked in a calendar
- [ ] A copy of this plan is stored outside our main systems

## Quality self-check: "Would a stranger understand this?"

Ask someone who did not write it to read Parts 3, 6, and 7 and answer:
1. Can you tell what to fix first? ______
2. Can you tell who to call? ______
3. Can you follow Playbook P-A without asking me anything? ______

If any answer is "no", improve that part before signing.

## Sign-off

| Role | Name | Signature / approval note | Date |
|---|---|---|---|
| Plan owner | | | |
| Backup owner | | | |
| Business / product lead | | | |
| Technical lead | | | |
| Finance lead | | | |
| External approver (if required) | | | |

---

# Appendix A: One-Page Emergency Card (print this)

Fill this in last, then print it and keep it somewhere you can reach even when everything is down.

```
PROJECT: ______________________   PLAN VERSION: ______
INCIDENT LEADER: __________ PHONE: __________
BACKUP LEADER:   __________ PHONE: __________
TECH LEAD:       __________ PHONE: __________
COMMS LEAD:      __________ PHONE: __________
FINANCE LEAD:    __________ PHONE: __________
LEGAL/PRIVACY:   __________ PHONE: __________

STEP 1  Stay calm. Note the TIME you noticed: ______
STEP 2  Tell the Incident Leader.
STEP 3  Decide the level: SEV 1 (critical) / SEV 2 / SEV 3
STEP 4  Open the right playbook (Part 7).
STEP 5  Post a status update within 30 minutes (SEV 1).
STEP 6  Write down everything with times.
STEP 7  If personal data may be exposed: call Legal/Privacy NOW.

RESTORE FIRST: 1) ____________ 2) ____________ 3) ____________
STATUS PAGE: ______________________
FULL PLAN LOCATION: ______________________
PASSWORD MANAGER ACCESS HELD BY: ______________________
```

---

# Appendix B: Filled-In Sample (All Parts)

> **Read this to see what "good" looks like.** Everything below is **fictional**. The project, people, and numbers are made up. Copy the *style* of the answers, not the content. Answers are short on purpose: one fact each, real names, real numbers.

**Sample project: BillPilot**, a mobile and web invoicing app for freelancers. Team of 3: **Priya** (founder, plan owner), **Ravi** (tech lead), **Meera** (finance and support). Currently at **Stage D (launch week)**.

## Part 1: The Basics (sample)

| ID | Answer |
|---|---|
| Q1.1 | BillPilot lets freelancers create and send invoices and get paid by card. |
| Q1.2 | Freelancers and small agencies in the US and Germany. |
| Q1.3 | SaaS web app, mobile app (iOS and Android), AI features (invoice text suggestions). |
| Q1.4 | In scope: production app, billing, support inbox, AI features, company bank account, key vendors. |
| Q1.5 | Out of scope: personal laptops' non-work files, internal side projects. |
| Q1.6 | Team in India. Customers in the US (60%) and Germany (40%). |
| Q1.7 | 3 people, plus 1 part-time designer. |
| Q1.8 | No outside approver yet. Investor Arjun gets a copy each year. |

## Part 2: Lifecycle (sample)

| ID | Answer |
|---|---|
| Q2.1 | Stage D: Launch week. |
| Q2.2 | Public launch 2027-02-01. Customer #1 target 2027-02-03. Customer #100 target 2027-05-01. Customer #500 target 2027-11-01. |
| Q2.3 | Sign-up and payment must work on launch day. |
| Q2.6 (Gate C to D) | 11 of 13 checks are Yes. "Load test" = No (due 2027-01-25, Ravi). "Tabletop talk-through" = No (booked 2027-01-27, Priya). Priya accepts these two risks until those dates. |

## Part 3: What Must Keep Working (sample)

| Function | Importance | RTO | RPO | Workaround while down | Owner |
|---|---|---|---|---|---|
| Sign up and log in | 1 | 2 hours | 15 min | Meera creates accounts by hand | Ravi |
| Take payments | 1 | 4 hours | 0 | Email a payment link; record by hand | Meera |
| Create and send invoices | 1 | 4 hours | 1 hour | Customers download a PDF template | Ravi |
| AI invoice suggestions | 3 | 3 days | N/A | Turn feature off with a notice | Ravi |
| Support replies | 2 | 8 hours | 1 day | Auto-reply + shared inbox | Meera |

| ID | Answer |
|---|---|
| Q3.2 | Restore first: 1) Log in, 2) Payments, 3) Invoices. |
| Q3.3 | Payments down costs about $40 per hour in missed sign-ups, plus trust. |
| Q3.4 | Minimum service: customers can log in, view and download invoices. New sign-ups paused. |
| Q3.5 | Busy days: 1st of each month (customers send invoices) and launch week. |
| Q3.7 (absolute limit) | Payments: 24 hours. Past that we lose customers and risk provider review. |

## Part 4: Risks (sample)

| Risk | Likelihood | Impact | Score | Playbook? |
|---|---|---|---|---|
| R1 Cloud outage | 3 | 5 | 15 | Yes (P-A) |
| R6 Payment provider freezes account | 2 | 5 | 10 | Yes (P-E, because impact is severe) |
| R8 AI provider outage | 4 | 2 | 8 | Yes (P-F, short) |
| R10 AI cost spike | 3 | 4 | 12 | Yes (P-H) |
| R13 Key person unavailable | 3 | 4 | 12 | Yes (P-I) |
| R24 AI-written code hides a bug | 3 | 4 | 12 | Yes (P-B) |

| ID | Answer |
|---|---|
| Q4.2 | Top 3 worries: payment freeze, a bad release on launch day, Ravi being the only one with cloud admin access. |
| Q4.4 | Single point of failure: only Ravi has cloud admin. Fix: Priya becomes second admin by 2027-01-20. |

## Part 5: Dependencies (sample)

| Vendor | What it does | Importance | Account owner | Status page | Backup option |
|---|---|---|---|---|---|
| Cloud host | Runs the app | 1 | Ravi | (their status page) | Restore into second region within 6 hours |
| Payment provider | Takes cards | 1 | Meera | (their status page) | Second provider account (approved, not yet live) |
| AI provider | Powers suggestions | 3 | Ravi | (their status page) | Second model; or switch the feature off |
| App stores | Distribute the mobile app | 1 | Priya | Not applicable | Web app works in any browser |
| Domain registrar | Owns billpilot web address | 1 | Priya | n/a | Auto-renew; reminders at 60 and 14 days |

| ID | Answer |
|---|---|
| Q5.3 | The payment provider and app stores can suspend us with little warning. |
| Q5.4 | Domain and cloud logins are in the team password manager. Recovery codes are printed and kept in Priya's locked drawer. |
| Q5.5 | Payment provider exit: full export from dashboard; second provider already approved; 14 days to move; Meera leads. |

## Part 6: People (sample)

| Role | Primary | Backup |
|---|---|---|
| Incident Leader | Priya | Ravi |
| Technical Lead | Ravi | Freelancer Dev (contract on call) |
| Customer Communicator | Meera | Priya |
| Finance Lead | Meera | Priya |
| Legal / Privacy Contact | Outside lawyer (retainer) | Priya |

| ID | Answer |
|---|---|
| Q6.2 | If chat is down: phone call, then SMS, then personal email. Group on Signal as backup. |
| Q6.3 | Whoever notices tells Priya. Priya calls Ravi, then Meera. |
| Q6.5 | Priya can spend up to $500 in an emergency without asking anyone. |
| Q6.8 | Weekly on-call rotation between Ravi and the freelancer. Handover Mondays 10:00. |

## Part 7: Playbook P-A, App is down (sample)

- **Owner:** Ravi.
- **How we notice:** Uptime monitor texts Ravi and Priya.
- **First 15 minutes:** 1) Check the cloud status page. 2) Check whether a release went out in the last hour. 3) Post "We are investigating" on the status page.
- **Next 1 hour:** 1) If a release caused it, roll back with the rollback command (about 5 minutes). 2) If the cloud is down, wait for vendor updates and prepare to restore in the second region. 3) Post an update every 30 minutes.
- **Done when:** Login, payment, and invoice sending all pass the 3-step check, and error rate has been normal for 30 minutes.
- **After:** Meera writes a short incident note within 2 days.
- **Last tested:** Rollback practiced 2027-01-18. Passed (6 minutes).

## Part 8: Billing and Finance (sample)

| ID | Answer |
|---|---|
| Q8.1 | Monthly and yearly card subscriptions through the payment provider. |
| Q8.3 | Runway: 14 months. |
| Q8.4 | Minimum monthly cost: $6,800 (cloud $400, AI $300, tools $500, people $5,000, accounting and legal $600). |
| Q8.5 | If billing is down we keep service on, stop charging, and run catch-up charges within 24 hours. No customer loses access because of our own outage. |
| Q8.8 | AI and cloud alerts at 80% and 100% of $700 monthly. Hard cap on AI keys. Ravi gets the alert. First thing we switch off: free-tier AI suggestions. |
| Q8.13 | Failed payment: retry on days 0, 3, 7. Warning in app on day 7. Pause on day 10. Data kept 30 days after pause. |
| Q8.17 | Refund within 14 days: yes, support up to $100. Outage over our promise: credit of 1 day per hour down, approved by Meera. |
| Q8.19 | Weekly: provider report equals bank deposits (Meera). Monthly: billing system equals accounting books (Meera, reviewed by accountant). |
| Q8.23 | If revenue drops 30%: 11 months. If provider holds payouts 30 days: 12 months. |

## Part 9: Backups (sample)

| Data | Backup method | How often | Kept | Stored where | Last restore test |
|---|---|---|---|---|---|
| Customer database | Automatic snapshot | Hourly | 30 days | Second region | 2027-01-15, 40 minutes, passed |
| Source code | Mirror of the code host | Daily | 90 days | Separate account | 2027-01-15, passed |
| AI prompts and settings | Stored in code, version-controlled | Every change | Forever | Code host | 2027-01-15, passed |
| Accounting records | Export from accounting tool | Monthly | 7 years | Cloud drive + offline copy | Due 2027-02-28 |

## Part 10: AI Continuity (sample)

| ID | Answer |
|---|---|
| Q10.1 | AI helps write code. AI suggests invoice wording for customers. No AI agents take actions. |
| Q10.3 | Yes: switch to the backup model with a config change in about 15 minutes. Ravi does it. |
| Q10.4 | Off switch: feature flag `ai_suggestions` in the admin dashboard. |
| Q10.6 | Human approval for every change to payments, login, or database structure. |
| Q10.12 | One AI feature: invoice wording suggestions. Sees only the text the user types. Takes no actions. Off switch `ai_suggestions`. |
| Q10.15 | 40 test cases in the repository. Must pass 95% before a prompt or model change ships. |
| Q10.23 | A human reviews all AI-written code. Extra review for payments, login, and deletion. AI tools cannot reach production data or secrets. |

## Part 11: Milestones (sample)

| ID | Answer |
|---|---|
| Q11.2 | Promise: 99.5% uptime. First support reply within 1 business day. |
| Q11.3 | After a bad outage: apology plus a credit of one day per hour down. |
| Q11.5 | Support will break first. Plan: help center and saved replies before customer #50. |
| Q11.7 | No concentration risk yet. Largest customer is under 3% of revenue. |

## Part 12: Communication (sample)

- **Status page:** hosted by a separate provider. Priya and Meera can update it.
- **Template 1 (looking into it):** "We know some customers cannot log in. We are working on it. Next update by [time]."
- **Template 3 (billing):** "Some customers may see a late or wrong charge since [date]. We will correct it by [date]. No action is needed."

## Part 13: Legal, Insurance, Compliance (sample)

| Question | Answer |
|---|---|
| Q13.1 EU/UK personal data (GDPR)? | Yes. German customers. Owner: Priya. |
| Q13.2 California (CCPA)? | Not sure. Outside lawyer to confirm by 2027-01-31. |
| Q13.5 Card payments, provider handles card data? | Yes. Card numbers never touch our servers. |
| Q13.7 SOC 2 or ISO 27001 expected? | Not yet. Revisit at customer #250. |
| Q13.17 Cyber insurance | Quote requested. Decision due 2027-02-15. |
| Q13.20 Uptime promise | 99.5% monthly. Written in terms of service. Credit if missed. |
| Q13.21 Vendor promise vs our promise | Cloud promises 99.9%; we promise 99.5%. OK. |

## Part 14: Testing (sample)

- Backup restore test: every 3 months. Next 2027-04-15, Ravi.
- Tabletop talk-through: every 6 months. First 2027-01-27, scenario "payment provider freezes our account on the 1st".
- Contact check: every 6 months. Meera.

## Part 15: Sign-Off (sample)

| Role | Name | Date |
|---|---|---|
| Plan owner | Priya | 2027-01-28 |
| Technical lead | Ravi | 2027-01-28 |
| Finance lead | Meera | 2027-01-28 |

---

# Appendix C: Plain-Language Glossary (Extra Terms)

| Term | Meaning |
|---|---|
| **Backup** | A saved copy you can restore if the original is lost |
| **Chargeback** | A customer disputes a card payment through their bank and the money is taken back |
| **Feature flag** | A switch that turns a feature on or off without a new release |
| **Idempotency** | A safety method so the same payment request cannot charge twice |
| **Monitoring** | Automatic checking that tells you when something breaks |
| **On-call** | The person who must respond when an alarm goes off |
| **Rate limit** | A cap on how many requests a service allows |
| **Rollback** | Going back to the previous working version |
| **SLA** | A written promise about uptime or response time |
| **Staging** | A practice copy of your product used for testing |
| **Status page** | A public page that shows whether your service is working |
| **Tabletop exercise** | A talk-through of a pretend emergency |
| **Two-step login (2FA/MFA)** | A second proof of identity beyond a password |
| **Uptime** | The share of time the service works (99.9% = about 8.8 hours of downtime per year) |

---

# Appendix D: Sources and Standards This Template Follows

This template is original text, structured to match widely used continuity practice:
- ISO 22301 (business continuity management): business impact analysis, strategies, plans, exercising, and maintenance
- NIST SP 800-34 Rev. 1 (contingency planning): policy, impact analysis, recovery strategies, plan development, testing and training, maintenance
- GDPR Articles 33 and 34 (breach notification) and the "availability and resilience" principle
- PCI-DSS (incident response planning requirement)
- SOC 2 Availability criteria and ISO 27001 (documented recovery objectives, tested recovery, review)

> This template is a planning aid, not legal advice. Check legal and compliance answers with a qualified professional. See **Appendix E** for the coverage map against ISO 22301 and NIST SP 800-34.

---

# Appendix E: Coverage Map (ISO 22301, NIST SP 800-34, and Related Frameworks)

Use this table to show a customer, investor, or auditor where each standard's topics are covered. It is a **map for planning**, not a certification or legal advice. Clause numbers follow the commonly published ISO 22301:2019 structure and the seven-step NIST SP 800-34 Rev. 1 process; **check them against your licensed copy of the standard** before quoting them in an audit.

| Topic | ISO 22301 area | NIST SP 800-34 step | Where in this template |
|---|---|---|---|
| Scope, context, who cares (interested parties) | 4 Context | 1 Policy | Part 1 (Q1.4 to Q1.10) |
| Policy and objectives | 5 Leadership, 6 Planning | 1 Policy | Q1.9, Part 11 (Q11.2) |
| Roles, responsibilities, authority | 5 Leadership | 5 Plan | Part 6 |
| Risk assessment | 6 Planning, 8.2 | 3 Preventive controls | Part 4 (Q4.1 to Q4.5) |
| Business impact analysis (importance, RTO, RPO, minimum service) | 8.2 | 2 BIA | Part 3 |
| Resources needed to recover (people, tools, data, suppliers) | 8.3, 8.4 | 2 and 4 | Q3.6, Part 5, Part 9 |
| Recovery strategies and solutions | 8.3 | 4 Strategies | Parts 5, 8, 9, 10, Q6.12 |
| Plans and procedures (activation, response, recovery, stand-down) | 8.4 | 5 Plan | Part 7 (Q7.1 to Q7.4, P-A to P-Q) |
| Communication | 7.4, 8.4 | 5 Plan | Part 12 |
| Training, awareness, competence | 7.2, 7.3 | 6 Test and train | Q14.6 |
| Exercises and tests | 8.5 | 6 Test and train | Part 14 (Q14.1, Q14.2), Part 2 gates |
| Evaluation, audit, management review | 9 Evaluation | 7 Maintenance | Q14.3, Q14.7, Part 15 |
| Corrective action and improvement | 10 Improvement | 7 Maintenance | Q14.3, Q14.4, Q7.4 |
| Document control and records | 7.5 | 7 Maintenance | Document Control, Q14.5 |
| Supplier / vendor dependency | 8.3, 8.4 | 4 Strategies | Part 5 (Q5.1 to Q5.8) |
| Data backup and recovery | 8.3 | 4 Strategies | Part 9 |

| Related framework | What it asks in simple terms | Where covered |
|---|---|---|
| **GDPR** (availability and resilience; breach notice, usually within 72 hours of becoming aware) | Keep personal data available and secure; report breaches on time | P-D, Part 9, Part 13 |
| **CCPA / CPRA** | Respect consumer data rights | Q13.2, Q13.4 |
| **PCI-DSS** (incident response plan; do not store card data you do not need) | Have a tested incident plan; protect card data | P-D, P-E, Q13.5, Q13.6 |
| **SOC 2** (Availability and Security) | Documented recovery goals, tested recovery, regular review | Parts 3, 9, 14 |
| **ISO 27001** | Continuity of information security, supplier controls | Parts 5, 9, 13, 14 |

## Known limits of this template (be honest with auditors)

- It does **not** replace a formal disaster-recovery runbook for infrastructure at larger scale (for example, step-by-step server rebuild scripts). Add those as separate technical documents and link them from Part 9 and the playbooks.
- Physical premises are covered only lightly (Q6.12) because most early teams work remotely. If you have an office, warehouse, or lab, add a short section for it.
- Certification (ISO 22301, SOC 2, ISO 27001) needs an auditor, evidence, and management review beyond this document.
- Legal, tax, and insurance answers must be confirmed by qualified professionals.
