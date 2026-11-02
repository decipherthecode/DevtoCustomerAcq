# How to Fill This Document (Read This First)

> **What this file is:** A reusable, fill-in-the-blank template for studying your first 500 customers in groups ("cohorts") from before launch until you decide whether the product is ready to grow.
> **Who can fill it:** Anyone. If you can answer a question in plain words, you can fill this in. No data-science skills needed.
> **How long it takes:** 30 minutes to start (Parts 0-4). Then 10-20 minutes each time you update it (weekly during beta, monthly later).

## 0.1 The 5 Golden Rules

1. **Answer every question.** If you do not know, write `UNKNOWN` and add an owner and a date in Part 18 (Action Log). Never leave a blank and never guess silently.
2. **Replace everything inside `[square brackets]`.** Square brackets mean "write your answer here". Delete the brackets after you write.
3. **Use numbers, not feelings.** Write "42 of 100 customers (42%)", not "many customers".
4. **Write the date next to every number.** Numbers change. Format: `YYYY-MM-DD`.
5. **Keep the example, delete it later.** Every section has an `Example:` line in italics. Read it, copy its style, then you may delete it in your final copy.

## 0.2 Symbols Used in This Document

| Symbol | Meaning |
|---|---|
| `[ ]` | Not done yet (tick box: change to `[x]` when done) |
| `[x]` | Done |
| `REQUIRED` | You must fill this before moving on |
| `OPTIONAL` | Fill it if it applies to your product |
| `UNKNOWN` | You do not know yet (must be tracked in the Action Log) |
| `N/A` | Does not apply (write one short reason) |
| 🟢 / 🟡 / 🔴 | Healthy / Needs attention / Problem |

## 0.3 Quick-Start Path (the shortest way to a useful document)

1. Fill **Part 2** (Document Control) and **Part 5** (Goal and Context).
2. Fill **Part 6** (Cohort Definitions) by picking how you will group customers.
3. Fill **Part 7** and **Part 8** (Data and Tracking) *before launch*.
4. Pass the **Part 9** checklist *before you let the first customer in*.
5. After launch, update **Parts 11-16** on a schedule.
6. At customers 100, 250 and 500, complete **Part 17** (Scorecard) and **Part 18** (Decisions).

## 0.4 Which Parts to Fill in Which Phase

| Phase | Customers so far | Fill these Parts |
|---|---|---|
| **Phase 1: Build and Test** (before launch) | 0 | 1-10 |
| **Phase 2: Beta / Soft Launch** | 1-50 | 11-16 (weekly), 19 |
| **Phase 3: Public Launch** | 51-200 | 11-16 (weekly), 17 at 100 customers, 19 |
| **Phase 4: Growth Validation** | 201-500 | 11-16 (weekly), 17 at 250 and 500, 18 |

## 0.5 Reusing This Template Across Many Projects

**Do this for every new project:**
1. Copy this file. Name the copy `Customer_Cohort_Analysis_[ProjectName].md`. Never fill in the master template.
2. Fill the copy. Do not rename, delete or reorder Parts (this keeps every project comparable).
3. If a Part does not apply, keep its heading and write `N/A` plus one short reason.

**What you may change in a copy:**
- Add rows to tables.
- Add extra channels, plans, events, metrics, or questions at the end of a Part, labelled `ADDED`.
- Change targets in Part 18 (always log the change in Part 21.3).

**What you may NOT change in a copy:**
- Part numbers and headings.
- The Golden Rules (0.1) and the AI Agent Rules (Part 3).
- Metric definitions in Part 10, unless you log it in Part 21.3.

**Improving the master template:** If you find something confusing or missing, write it in the master's Change Log and bump the template version (1.0 to 1.1). Do this in one place only, by the template owner.

## 0.6 Plain-Words Promise

Every question can be answered with a short sentence, a number, or a tick box. If a word looks hard, look it up in Part 1. If you are still stuck, write `UNKNOWN` and move on.

## 0.7 Fill-In Style Used by Every Question

Every question looks like this:

```
Q#.# [REQUIRED] Plain-language question?
Why we ask: one sentence explaining why it matters.
Answer: [write here]
Example: what a good answer looks like.
```

---

# 1. Glossary (Plain-Language Definitions)

| Word | Meaning in simple words |
|---|---|
| **Customer** | A person or company that has used your product for real (see your definition in Q5.4). |
| **Cohort** | A group of customers who share something, such as the week they joined. We study each group separately so we can see if things get better over time. |
| **Signup cohort** | Customers grouped by the week or month they joined. |
| **Channel cohort** | Customers grouped by how they found you (ad, friend, search, etc.). |
| **Plan cohort** | Customers grouped by what they chose (free, paid, enterprise). |
| **Key-action cohort** | Customers grouped by when they first did the most important thing in your product. |
| **Activation** | The moment a new customer first gets real value ("aha!"). |
| **Retention** | How many customers from a group are still using the product after some time. |
| **Churn** | The opposite of retention: customers who left or stopped using it. |
| **Day-N / Week-N retention** | Share of a cohort that came back on day N or in week N after joining. |
| **DAU / WAU / MAU** | Daily / weekly / monthly active users. |
| **Stickiness** | DAU divided by MAU. Higher means people use it more often. |
| **ARPU** | Average revenue per user in a period. |
| **CAC** | Customer acquisition cost: money spent to win one customer. |
| **LTV** | Lifetime value: total money one customer is expected to bring. |
| **Payback period** | Months needed to earn back the CAC. |
| **NRR** | Net revenue retention (B2B): revenue today from last period's customers, as a share of their revenue then. |
| **NPS** | Net Promoter Score: "How likely are you to recommend us (0-10)?" |
| **CSAT** | Customer satisfaction score for a specific experience. |
| **PMF score** | The "how would you feel if you could no longer use this?" question. Share answering "very disappointed". |
| **Event** | One action the product records (for example `signed_up`, `created_project`). |
| **PII** | Personal information that identifies a person (name, email, phone). |
| **Product-market fit (PMF)** | Enough of the right customers love and keep using the product that growth makes sense. |
| **AI agent** | A software assistant (such as an AI model) that can read this document and help fill or check it. |
| **Go / Pivot / Stop** | The three possible decisions at the end of validation. |

---

# 2. Document Control

**Q2.1 [REQUIRED] What is the project name?**
Why we ask: so nobody mixes up two projects.
Answer: `[Project name]`
*Example: PlantPal Mobile App*

**Q2.2 [REQUIRED] What is the product version this analysis covers?**
Answer: `[v0.0.0 or "all versions"]`
*Example: v1.2.0 and later*

**Q2.3 [REQUIRED] Who owns this document (one name, one role)?**
Answer: `[Name, role, contact]`

**Q2.4 [REQUIRED] Who helps fill it?**
Answer: `[Names and roles: product, engineering, marketing, support, finance]`

**Q2.5 [REQUIRED] Which phase are we in right now?**
Answer: `[ ] Phase 1 Build/Test   [ ] Phase 2 Beta   [ ] Phase 3 Public Launch   [ ] Phase 4 Growth Validation`

**Q2.6 [REQUIRED] How many real customers do we have today, and as of what date?**
Answer: `[number] customers as of [YYYY-MM-DD]`

**Q2.7 [REQUIRED] How often will this document be updated, and who reminds us?**
Answer: `[Weekly / Monthly] by [name]`

**Q2.8 [OPTIONAL] Where does this document live, and where are the raw data files?**
Answer: `[Folder path or link]`

### Document Status
| Field | Value |
|---|---|
| Template version | 1.2 |
| Document status | `[Draft / In review / Approved]` |
| Last updated | `[YYYY-MM-DD]` |
| Next update due | `[YYYY-MM-DD]` |

---

# 3. AI Agent Instructions (Read by AI Agents, Useful for Humans Too)

> If an AI agent is helping, give it this whole file. The agent must follow every rule below.

## 3.1 Agent Role
You are a careful analyst. You help the owner fill and check this document using only the data provided. You explain results in simple words.

## 3.2 Agent Rules (Hard Rules)

1. **Never invent data.** If a number is not provided, write `UNKNOWN` and add an item to Part 18.
2. **Show your math.** For every metric, show the formula and the inputs next to the result.
3. **Use the definitions in this document.** Do not change a definition (for example, what counts as "active") without asking the owner.
4. **Mark small samples.** If a cohort has fewer than 30 customers, label results `LOW SAMPLE` and do not draw strong conclusions.
5. **Protect privacy.** Never copy names, emails, phone numbers or any PII into this document. Use anonymous IDs only.
6. **Ask when unclear.** If two answers are possible, ask the owner one short question instead of choosing.
7. **Keep the structure.** Do not rename, delete or reorder parts. Only fill the answers.
8. **Cite the source.** After every number, write where it came from (file, dashboard, date).
9. **Flag conflicts.** If two sources disagree, show both numbers and ask which is correct.
10. **Do not give final go / pivot / stop decisions alone.** Recommend, explain, and let the human decide in Part 18.

## 3.3 Agent Inputs (What the Owner Should Provide)

| Input | Required? | Format |
|---|---|---|
| Customer list with anonymous ID, signup date, channel, plan | Required | CSV |
| Event log (customer ID, event name, timestamp) | Required | CSV |
| Revenue records (customer ID, date, amount) | Required for Part 14 | CSV |
| Marketing/sales spend by channel and month | Required for CAC | CSV |
| Survey answers (NPS, PMF) | Optional | CSV |
| Interview notes (anonymous) | Optional | Text |

## 3.4 Agent Outputs (What the Agent Must Return)

1. The filled parts requested, with `Source:` and `As of:` lines.
2. A short list titled **"What I could not fill and why"**.
3. A short list titled **"Things that look wrong or unusual"**.
4. Three plain-language insights (see Part 16 format).
5. Questions for the owner (maximum 5).

## 3.5 Agent Self-Check Before Replying
- [ ] Every number has a source and a date.
- [ ] Every percentage shows numerator and denominator.
- [ ] No PII appears anywhere.
- [ ] Small cohorts are labelled.
- [ ] Nothing was guessed.

---

# 4. Lifecycle Map: What You Are Trying to Learn in Each Phase

| Phase | Customers | Main question | What success looks like |
|---|---|---|---|
| 1. Build and Test | 0 | Can we measure the right things? | Tracking works and passes the Part 9 checklist |
| 2. Beta | 1-50 | Do early customers reach value and come back? | A clear "aha" action and early retention signal |
| 3. Public Launch | 51-200 | Does it still work with strangers and different channels? | Retention holds across channels; costs are known |
| 4. Growth Validation | 201-500 | Is it ready to grow without breaking? | Scorecard in Part 17 is mostly green; decision made |

## 4.1 "Definition of Done" Gate for Each Phase

> A phase is finished only when every box in its gate is ticked. Do not move to the next phase until then. If you must move on early, write the reason in Part 19.

**Gate 1: Build and Test is done when...**
- [ ] Part 9 checklist is fully ticked.
- [ ] A test customer went from signup to key action to payment and all events appeared in the data.
- [ ] Definitions in Part 5 and cohorts in Part 6 are agreed.
- [ ] Targets in Part 18 are written (before any real results exist).
- [ ] A person other than the builder checked the data export.

**Gate 2: Beta is done when...**
- [ ] At least `[50]` real customers exist (Q5.4 definition).
- [ ] Activation rate and week-1 retention are measured for at least 2 cohorts.
- [ ] At least `[10]` customer interviews are done and written in Q15.5.
- [ ] The top 3 reasons customers leave are known (Q11.4).
- [ ] Part 20 checklist passed.

**Gate 3: Public Launch is done when...**
- [ ] At least `[200]` real customers exist.
- [ ] At least 2 acquisition channels have been tried and compared (Part 13).
- [ ] Week-4 retention is measured for at least 4 cohorts.
- [ ] First revenue and CAC numbers are real (Part 14), not guesses.
- [ ] Part 18 scorecard was completed once at 100 customers.

**Gate 4: Growth Validation is done when...**
- [ ] At least `[500]` real customers exist.
- [ ] Part 18 scorecard is completed with a written decision (Q18.1).
- [ ] Every `UNKNOWN` is either answered or has an owner and date in Part 19.
- [ ] Part 20 checklist passed and the owner signed Part 22.

## 4.2 AI-Driven Development Workflow and Cohorts

> In AI-driven development, features, prompts, models and AI agents change quickly. Each change can make customers behave differently. Record changes so you can tell **what changed** from **who joined**.

**Q4.2 [REQUIRED] Which parts of our product are built or run by AI?**
Answer: `[ ] AI wrote code   [ ] AI generates content for customers   [ ] AI agent talks to customers   [ ] AI decides or recommends   [ ] AI runs tests/releases   [ ] Other: [ ]`

**Q4.3 [REQUIRED] How do we label each release so we can tie it to cohorts?**
Answer: `Release label format: [e.g., 2026-10-19-r3]. Saved in event property: [name].`

**Q4.4 [REQUIRED] Which AI model, prompt, or agent version is each customer served by?**
Answer: `Saved as event property [name]. Owner of version list: [name]. / N/A`

**Q4.5 [REQUIRED] What human check do we do before AI-built changes reach customers?**
Answer: `[Review, test, approval steps and owner]`

**Q4.6 [REQUIRED] Release and change log (add a row for every release or AI version change)**
| Date | Release / AI version label | What changed (one sentence) | Customers affected (all / cohort) | Expected effect on a metric | Actual effect (fill later) |
|---|---|---|---|---|---|
| `[YYYY-MM-DD]` | `[label]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q4.7 [REQUIRED] What do we do if an AI change makes a metric worse?**
Answer: `If [metric] drops by more than [ ]% within [ ] days, we [roll back / pause / investigate]. Owner: [name].`

**Q4.8 [REQUIRED] How do we handle AI mistakes that customers notice (wrong answers, bad outputs)?**
Answer: `We count them as [event name]. We review them [how often]. Rate target: under [ ] per 100 customers.`

## 4.3 Phase Dates

**Q4.9 [REQUIRED] What are the planned dates for each phase?**
Answer:
| Phase | Start | End |
|---|---|---|
| 1. Build and Test | `[YYYY-MM-DD]` | `[YYYY-MM-DD]` |
| 2. Beta | `[YYYY-MM-DD]` | `[YYYY-MM-DD]` |
| 3. Public Launch | `[YYYY-MM-DD]` | `[YYYY-MM-DD]` |
| 4. Growth Validation | `[YYYY-MM-DD]` | `[YYYY-MM-DD]` |

---

# 5. Goal and Context

**Q5.1 [REQUIRED] In one sentence, what does the product do and for whom?**
Why we ask: everyone must describe it the same way.
Answer: `[Product] helps [type of customer] to [result].`
*Example: PlantPal helps busy apartment owners keep houseplants alive with simple reminders.*

**Q5.2 [REQUIRED] What type of product is it?**
Answer: `[ ] B2C app/consumer   [ ] B2B SaaS   [ ] Marketplace (buyers and sellers)   [ ] Other: [describe]`

**Q5.3 [REQUIRED] How does it earn money?**
Answer: `[ ] Free   [ ] One-time purchase   [ ] Subscription   [ ] Usage-based   [ ] Commission/fee per transaction   [ ] Ads   [ ] Other: [describe]`

**Q5.4 [REQUIRED] What exactly counts as a "customer"?**
Why we ask: this is the number we are counting up to 500. Different meanings give different results.
Answer: `A customer is someone who [did exactly what?]. Free signups only [count / do not count].`
*Example: A customer is someone who signed up AND completed at least one watering reminder. Free signups who never did that do not count.*

**Q5.5 [REQUIRED] What is the "key action": the single most important thing a customer does that shows they got value?**
Answer: `[Action name]`
*Examples: B2C: "played first full session"; B2B: "invited a teammate and created a project"; Marketplace: "completed first transaction (buyer) / first sale (seller)".*

**Q5.6 [REQUIRED] What is the "aha moment", and how soon should it happen?**
Answer: `The aha moment is when [describe]. Target: within [number] [minutes/hours/days] of signup.`

**Q5.7 [REQUIRED] What counts as an "active" customer in one period?**
Why we ask: retention depends on this definition. Write it once and never change it without logging the change in Part 21.
Answer: `A customer is active in a [day/week/month] if they [did which action at least how many times].`
*Example: Active in a week = completed at least 1 key action in that calendar week.*

**Q5.8 [REQUIRED] What counts as "churned"?**
Answer: `A customer has churned if [no active period for N days/weeks] OR [cancelled subscription].`

**Q5.9 [REQUIRED] For marketplace products only: what are the two sides, and which side do you track first?**
Answer: `Side A: [e.g., sellers]. Side B: [e.g., buyers]. Tracked first: [A/B]. Reason: [why]. / N/A`

**Q5.10 [REQUIRED] For B2B products only: what is the "account" and who counts as a "user" inside it?**
Answer: `Account = [company/team]. User = [person]. Cohorts are counted by [accounts / users]. / N/A`

**Q5.11 [REQUIRED] What are our top 3 beliefs (hypotheses) we want this analysis to prove or disprove?**
Answer:
| # | We believe that... | We will know it is true if... | Status |
|---|---|---|---|
| H1 | `[belief]` | `[number/threshold]` | `[Open/Proved/Disproved]` |
| H2 | `[belief]` | `[number/threshold]` | `[Open/Proved/Disproved]` |
| H3 | `[belief]` | `[number/threshold]` | `[Open/Proved/Disproved]` |

*Example: H1: People who add 3 plants in their first day are still active after 4 weeks. True if week-4 retention for that group is at least 35%.*

**Q5.12 [REQUIRED] What is the single biggest decision this analysis will help us make?**
Answer: `[e.g., spend money on ads / hire / raise money / change the product / stop]`

---

# 6. Cohort Definitions

> Cohorts are groups. The same customer can appear in more than one type of cohort (for example, a March signup who came from referral on the Pro plan).

## 6.1 Signup-Date Cohorts (Primary Cohort Type)

**Q6.1 [REQUIRED] How will we cut signup groups?**
Answer: `[ ] By week (recommended for first 500 customers)   [ ] By month   [ ] By phase (beta / launch / growth)`

**Q6.2 [REQUIRED] What day does a week start, and which time zone do we use?**
Answer: `Week starts on [Monday/Sunday]. Time zone: [e.g., UTC].`

**Q6.3 [REQUIRED] Which event marks "signup date" (day 0)?**
Answer: `Day 0 = the date of event [event name].`

## 6.2 Acquisition-Channel Cohorts

**Q6.4 [REQUIRED] List every channel customers can come from.**
Answer:
| Channel code | Channel name | How we tell (link tag, form question, promo code) | Paid or free |
|---|---|---|---|
| `[CH01]` | `[Organic search]` | `[how identified]` | `[Free]` |
| `[CH02]` | `[Referral]` | `[how identified]` | `[Free]` |
| `[CH03]` | `[Paid ads]` | `[how identified]` | `[Paid]` |
| `[CH04]` | `[Direct outreach]` | `[how identified]` | `[Free]` |
| `[CH05]` | `[Other]` | `[how identified]` | `[ ]` |

**Q6.5 [REQUIRED] What do we do when the channel is unknown?**
Answer: `Label as "UNKNOWN_CHANNEL". Target: under [number]% of customers.`

## 6.3 Plan / Pricing-Tier Cohorts

**Q6.6 [REQUIRED] List every plan.**
Answer:
| Plan code | Plan name | Price | Billing period | Who it is for |
|---|---|---|---|---|
| `[P1]` | `[Free]` | `[$0]` | `[n/a]` | `[ ]` |
| `[P2]` | `[Pro]` | `[$ ]` | `[monthly/yearly]` | `[ ]` |
| `[P3]` | `[Business]` | `[$ ]` | `[monthly/yearly]` | `[ ]` |

**Q6.7 [REQUIRED] If a customer changes plan, which plan do we count them in?**
Answer: `[ ] The plan at signup   [ ] The current plan   [ ] Both (show separately)`

## 6.4 First-Key-Action Cohorts

**Q6.8 [REQUIRED] Which "first actions" do we want to compare?**
Why we ask: this finds which early behaviour predicts staying.
Answer:
| Behaviour code | Description | Time limit after signup |
|---|---|---|
| `[A1]` | `[Did the key action]` | `[within 24 hours]` |
| `[A2]` | `[Did the key action]` | `[within 7 days]` |
| `[A3]` | `[Never did the key action]` | `[after 7 days]` |

## 6.5 Minimum Cohort Size

**Q6.9 [REQUIRED] What is the smallest cohort we will trust?**
Answer: `[30] customers. Smaller cohorts will be labelled LOW SAMPLE.`

## 6.6 Customer Segments and Personas

> A segment is a type of customer (for example "busy parents" or "small agencies"). Segments help you see who the product works for.

**Q6.10 [REQUIRED] Who is our ideal customer? Describe one real-sounding person or company.**
Answer: `[Who they are, what problem they have, what they use today instead, why they would pay]`
*Example: Maya, 32, works full-time, lives in a flat, forgets to water plants, tried sticky notes and failed.*

**Q6.11 [REQUIRED] List up to 4 customer segments we expect.**
Answer:
| Segment code | Name | How to recognise them (question at signup, company size, job, age band) | Expected to love us? (Yes/Maybe/No) |
|---|---|---|---|
| `[SG1]` | `[ ]` | `[ ]` | `[ ]` |
| `[SG2]` | `[ ]` | `[ ]` | `[ ]` |
| `[SG3]` | `[ ]` | `[ ]` | `[ ]` |
| `[SG4]` | `[ ]` | `[ ]` | `[ ]` |

**Q6.12 [REQUIRED] Which segment keeps best after the first 100 customers? (Fill later)**
Answer: `[Segment] week-4 retention [ ]% vs overall [ ]% (n=[ ]).`

**Q6.13 [REQUIRED] Is there a segment we should NOT target? Why?**
Answer: `[ ]`

## 6.7 Cohort Summary (Fill After Launch)

| Cohort ID | Type | Start date | Size | Notes |
|---|---|---|---|---|
| `[SU-2026-W01]` | Signup week | `[YYYY-MM-DD]` | `[n]` | `[ ]` |
| `[CH-REFERRAL]` | Channel | `[YYYY-MM-DD]` | `[n]` | `[ ]` |
| `[PL-PRO]` | Plan | `[YYYY-MM-DD]` | `[n]` | `[ ]` |
| `[KA-A1]` | Key action | `[YYYY-MM-DD]` | `[n]` | `[ ]` |

---

# 7. Data Sources and Privacy

## 7.1 Where the Data Comes From

**Q7.1 [REQUIRED] Where is each type of data stored, and who can export it?**
Answer:
| Data | Tool / location | Owner | Export method | Refresh rate |
|---|---|---|---|---|
| Customer list | `[tool]` | `[name]` | `[how]` | `[daily/weekly]` |
| Product events | `[tool]` | `[name]` | `[how]` | `[ ]` |
| Payments | `[tool]` | `[name]` | `[how]` | `[ ]` |
| Marketing spend | `[tool]` | `[name]` | `[how]` | `[ ]` |
| Surveys / feedback | `[tool]` | `[name]` | `[how]` | `[ ]` |
| Support tickets | `[tool]` | `[name]` | `[how]` | `[ ]` |

**Q7.2 [REQUIRED] Which single source is the "truth" if two numbers disagree?**
Answer: `For customers: [source]. For revenue: [source]. For usage: [source].`

## 7.2 Privacy and Consent

**Q7.3 [REQUIRED] Do customers know and agree that we measure their usage?**
Answer: `[ ] Yes, in [terms / privacy policy / consent screen]   [ ] No (fix before launch)`

**Q7.4 [REQUIRED] Which laws or rules apply to our customers?**
Answer: `[ ] GDPR   [ ] CCPA/CPRA   [ ] Children's privacy rules   [ ] Health/finance rules   [ ] Other: [ ]   [ ] Not sure (ask a legal professional)`

**Q7.5 [REQUIRED] How do we hide identity in this analysis?**
Answer: `Customers are shown only by anonymous ID: [format]. No names or emails are stored in this file.`

**Q7.6 [REQUIRED] How long do we keep the raw data, and who may see it?**
Answer: `Kept for [period]. Access: [roles].`

**Q7.7 [REQUIRED] How does a customer ask us to delete their data, and is it reflected in the analysis?**
Answer: `[Process and owner]`

---

# 8. Tracking Plan (Decide in Phase 1, Before Any Customer Arrives)

> If it is not tracked, it cannot be analysed later. List every event the product must record.

**Q8.1 [REQUIRED] List the events we will track.**
Answer:
| Event name | When it fires | Properties to save (attributes) | Needed for which metric | Built? | Tested? |
|---|---|---|---|---|---|
| `signed_up` | `[account created]` | `channel, plan, device, country` | Cohort start | `[ ]` | `[ ]` |
| `activated` | `[key action done first time]` | `time_since_signup` | Activation | `[ ]` | `[ ]` |
| `key_action_done` | `[each time]` | `feature, count` | Engagement | `[ ]` | `[ ]` |
| `session_started` | `[app/site opened]` | `device` | Retention | `[ ]` | `[ ]` |
| `plan_changed` | `[upgrade/downgrade]` | `from_plan, to_plan` | Plan cohorts | `[ ]` | `[ ]` |
| `payment_succeeded` | `[money received]` | `amount, currency` | Revenue | `[ ]` | `[ ]` |
| `cancelled` | `[subscription ended]` | `reason` | Churn | `[ ]` | `[ ]` |
| `feedback_given` | `[survey answered]` | `score, text_id` | Satisfaction | `[ ]` | `[ ]` |
| `[add more]` | | | | | |

**Q8.2 [REQUIRED] For marketplaces: which extra events do we track?**
Answer: `[ ] listing_created  [ ] search_done  [ ] message_sent  [ ] transaction_completed  [ ] review_left  [ ] dispute_opened / N/A`

**Q8.3 [REQUIRED] For B2B: which team-level events do we track?**
Answer: `[ ] account_created  [ ] teammate_invited  [ ] teammate_joined  [ ] integration_connected  [ ] admin_action / N/A`

**Q8.4 [REQUIRED] How does each customer get a permanent anonymous ID, and how is it linked across tools?**
Answer: `[Describe]`

**Q8.5 [REQUIRED] How do we record the channel at signup so it is not lost?**
Answer: `[ ] Link tags (UTM)  [ ] "How did you hear about us?" question  [ ] Promo/referral code  [ ] Other: [ ]`

---

# 9. Pre-Launch Readiness Checklist (Pass Before Customer #1)

Tick `[x]` only after you have actually tested it.

**Definitions**
- [ ] "Customer", "key action", "active" and "churned" are written in Part 5.
- [ ] Cohort rules in Part 6 are agreed by the team.

**Tracking**
- [ ] All events in Part 8 fire correctly in a test account.
- [ ] Test accounts are tagged so they are excluded from results.
- [ ] Signup date and channel are saved for every new account.
- [ ] Events keep the same anonymous ID for the same person.

**Data**
- [ ] A person can export customers, events and payments.
- [ ] A sample export has been opened and looked at by a human.
- [ ] Time zone is the same everywhere.

**Privacy**
- [ ] Consent or notice is in place (Q7.3).
- [ ] No PII is copied into this document.

**Process**
- [ ] The update schedule and owner are set (Q2.7).
- [ ] Everyone knows where this file lives.

**Q9.1 [REQUIRED] Is the product ready to measure?**
Answer: `[ ] Yes, all boxes ticked on [date] by [name]   [ ] No. Blockers: [list and add to Part 18]`

---

# 10. Metric Definitions (The Rulebook: Do Not Change Without Logging in Part 21)

> **In simple words:** A metric is just a number that answers a question. "Retention" asks "how many people stayed?" "Churn" asks "how many people left?" "CAC" asks "how much did it cost to get one customer?" You do not need to calculate these by hand. Use the formula only if you are doing the math yourself, or give it to your AI agent.

| Metric | Plain meaning | Formula | Good direction |
|---|---|---|---|
| **Cohort size** | How many joined in the group | Count of customers with the cohort label | n/a |
| **Activation rate** | Share who reached the key action in the time limit | Customers who did key action in time ÷ cohort size | Up |
| **Time to value** | How long until the aha moment | Median (first key action time − signup time) | Down |
| **Day-N retention** | Share active on day N | Cohort customers active on day N ÷ cohort size | Up |
| **Week-N retention** | Share active in week N | Cohort customers active in week N ÷ cohort size | Up |
| **Churn rate (period)** | Share lost in the period | Customers lost in period ÷ customers at start of period | Down |
| **DAU / WAU / MAU** | Active customers per day / week / month | Distinct active customers | Up |
| **Stickiness** | How often monthly users show up | DAU ÷ MAU | Up |
| **Engagement depth** | Average key actions per active customer | Total key actions ÷ active customers | Up |
| **Conversion to paid** | Share who start paying | Paying customers ÷ cohort size | Up |
| **ARPU** | Average revenue per user | Revenue in period ÷ active customers | Up |
| **CAC** | Cost to win one customer | Sales and marketing spend ÷ new customers | Down |
| **LTV (simple)** | Expected total revenue per customer | ARPU per month × gross margin × expected lifetime in months | Up |
| **LTV : CAC** | Return on acquisition spend | LTV ÷ CAC | Up |
| **Payback period** | Months to earn back CAC | CAC ÷ (monthly ARPU × gross margin) | Down |
| **Net revenue retention (B2B)** | Revenue kept and grown from the same customers | (Start revenue + expansion − downgrades − churn) ÷ start revenue | Up |
| **NPS** | Would they recommend us | % promoters (9-10) − % detractors (0-6) | Up |
| **PMF score** | Would they miss us | % answering "very disappointed" | Up |
| **Marketplace liquidity** | Do listings get fulfilled | Listings with a completed transaction in N days ÷ listings | Up |
| **Repeat rate** | Do people return to buy again | Customers with 2+ transactions ÷ customers with 1+ | Up |

**Q10.1 [REQUIRED] Which metrics from this list are our "main 5" that we watch every week?**
Answer: `1. [ ]  2. [ ]  3. [ ]  4. [ ]  5. [ ]`

**Q10.2 [REQUIRED] How long is a customer's expected lifetime for the LTV formula, and why?**
Answer: `[number] months because [evidence]. Until we have enough data, this is labelled ESTIMATE.`

**Q10.3 [REQUIRED] What gross margin do we use?**
Answer: `[ ]% from [source, date]`

---

# 11. Retention and Churn Tables

> Fill one table per cohort type you actively use. Each cell = share of the cohort still active. Leave future periods blank. Add `n=` for the cohort size.

## 11.1 Weekly Retention by Signup Week

| Signup week | n | Week 0 | Week 1 | Week 2 | Week 3 | Week 4 | Week 6 | Week 8 | Week 12 |
|---|---|---|---|---|---|---|---|---|---|
| `[2026-W01]` | `[ ]` | 100% | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` |
| `[2026-W02]` | `[ ]` | 100% | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` |
| `[2026-W03]` | `[ ]` | 100% | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` |
| `[add rows]` | | | | | | | | | |

Source: `[file/dashboard]`. As of: `[YYYY-MM-DD]`.

**Q11.1 [REQUIRED] Reading the table: do newer cohorts keep more, the same, or fewer customers than older ones?**
Answer: `[ ] Better   [ ] Same   [ ] Worse. Evidence: [numbers].`

**Q11.2 [REQUIRED] Where does the curve flatten (retention stops dropping)?**
Why we ask: a flat line means a core group has found lasting value.
Answer: `Flattens at about [ ]% around week [ ]. / It does not flatten yet.`

**Q11.3 [REQUIRED] Where is the biggest drop?**
Answer: `Between week [ ] and week [ ], customers fall from [ ]% to [ ]%.`

## 11.2 Churn Summary

| Period | Customers at start | Customers lost | Churn rate | Top reason |
|---|---|---|---|---|
| `[Month 1]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| `[Month 2]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| `[Month 3]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |

**Q11.4 [REQUIRED] What are the top 3 reasons customers leave, with counts?**
Answer: `1. [reason] ([n])  2. [reason] ([n])  3. [reason] ([n])`  Source: `[exit survey / interviews]`

**Q11.5 [OPTIONAL] Can any churn be prevented? Which actions might save those customers?**
Answer: `[Ideas]`

---

# 12. Activation and Engagement

## 12.1 Activation by Signup Cohort

| Signup cohort | n | Did key action within target time | Activation rate | Median time to value |
|---|---|---|---|---|
| `[2026-W01]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| `[2026-W02]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| `[add rows]` | | | | |

**Q12.1 [REQUIRED] Where do new customers get stuck before the aha moment?**
Answer: `Step [name] loses [ ]% of customers. Evidence: [data/interviews].`

**Q12.2 [REQUIRED] Which early behaviour best predicts long-term retention?**
Why we ask: this shows what to push new customers toward.
Answer: `Customers who [behaviour] in the first [time] stay at [ ]% vs [ ]% for others (n=[ ] vs n=[ ]).`

## 12.2 Engagement Over Time

| Cohort | Metric | Week 1 | Week 4 | Week 8 | Week 12 |
|---|---|---|---|---|---|
| `[2026-W01]` | Key actions per active customer | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| `[2026-W01]` | Sessions per active customer | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| `[add rows]` | | | | | |

| Date | DAU | WAU | MAU | Stickiness (DAU ÷ MAU) |
|---|---|---|---|---|
| `[YYYY-MM-DD]` | `[ ]` | `[ ]` | `[ ]` | `[ ]%` |

**Q12.3 [REQUIRED] Which features do retained customers use that churned customers do not?**
Answer: `[Feature list with percentages]`

**Q12.4 [REQUIRED] Marketplace only: is activity balanced between both sides?**
Answer: `Side A active: [ ]. Side B active: [ ]. Imbalance: [describe] / N/A`

**Q12.5 [REQUIRED] B2B only: how many users per account are active, and does more usage inside an account predict renewal?**
Answer: `Median active users per account: [ ]. Accounts with 3+ active users retain at [ ]% vs [ ]%. / N/A`

## 12.3 Onboarding and Support Playbook (Hands-On Help for the First 50+ Customers)

> Early on, doing things by hand ("do things that do not scale") teaches you more than any chart. Record what you do so it can later be turned into product features.

**Q12.6 [REQUIRED] How does a new customer get welcomed?**
Answer: `[ ] Welcome email   [ ] In-app guide   [ ] Personal message   [ ] Call/demo   [ ] Other: [ ]. Sent within [ ] of signup by [name].`

**Q12.7 [REQUIRED] What do we do if a customer has not reached the key action after [ ] days?**
Answer: `[Message, offer, call. Who does it, using which template]`

**Q12.8 [REQUIRED] Where do customers ask for help, and how fast do we answer?**
Answer: `Channels: [ ]. Target first reply: [ ] hours. Owner: [name].`

**Q12.9 [REQUIRED] What manual work are we doing that a customer would not see in the product?**
Answer: `[List, and how many hours per week it takes]`

**Q12.10 [REQUIRED] Help log (add a row for each important help request or call)**
| Date | Cohort / customer ID (anonymous) | Problem | What we did | Did it work? | Product fix idea |
|---|---|---|---|---|---|
| `[YYYY-MM-DD]` | `[ ]` | `[ ]` | `[ ]` | `[Yes/No]` | `[ ]` |

---

# 13. Acquisition and Channel Comparison

| Channel | Customers | Activation rate | Week-4 retention | Conversion to paid | CAC | Verdict |
|---|---|---|---|---|---|---|
| `[Organic search]` | `[ ]` | `[ ]%` | `[ ]%` | `[ ]%` | `[$ ]` | `[🟢/🟡/🔴]` |
| `[Referral]` | `[ ]` | `[ ]%` | `[ ]%` | `[ ]%` | `[$ ]` | `[ ]` |
| `[Paid ads]` | `[ ]` | `[ ]%` | `[ ]%` | `[ ]%` | `[$ ]` | `[ ]` |
| `[Outreach]` | `[ ]` | `[ ]%` | `[ ]%` | `[ ]%` | `[$ ]` | `[ ]` |

**Q13.1 [REQUIRED] Which channel brings the customers who stay longest?**
Answer: `[Channel] (week-4 retention [ ]%, n=[ ])`

**Q13.2 [REQUIRED] Which channel is the cheapest per retained customer (not just per signup)?**
Answer: `[Channel] at [$ ] per customer still active at week 4.`

**Q13.3 [REQUIRED] Which channel should we stop, keep, or grow, and why?**
Answer: `Stop: [ ]. Keep: [ ]. Grow: [ ]. Reason: [ ]`

---

# 14. Plan, Revenue and Unit Economics

## 14.1 Plan Cohort Comparison

| Plan | Customers | Week-4 retention | Month-3 retention | ARPU | Upgrades | Downgrades | Cancellations |
|---|---|---|---|---|---|---|---|
| `[Free]` | `[ ]` | `[ ]%` | `[ ]%` | `[$ ]` | `[ ]` | `[ ]` | `[ ]` |
| `[Pro]` | `[ ]` | `[ ]%` | `[ ]%` | `[$ ]` | `[ ]` | `[ ]` | `[ ]` |
| `[Business]` | `[ ]` | `[ ]%` | `[ ]%` | `[$ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q14.1 [REQUIRED] What share of free customers become paying, and how long does it take?**
Answer: `[ ]% within [ ] days (n=[ ]). / N/A (no free plan)`

## 14.2 Revenue by Signup Cohort

| Signup cohort | n | Month 0 revenue | Month 1 | Month 2 | Month 3 | Cumulative per customer |
|---|---|---|---|---|---|---|
| `[2026-01]` | `[ ]` | `[$ ]` | `[$ ]` | `[$ ]` | `[$ ]` | `[$ ]` |
| `[add rows]` | | | | | | |

## 14.3 Unit Economics (Show the Math)

| Item | Value | Formula or source | As of |
|---|---|---|---|
| Total sales and marketing spend | `[$ ]` | `[source]` | `[date]` |
| New customers in period | `[ ]` | `[source]` | `[date]` |
| CAC | `[$ ]` | spend ÷ new customers | `[date]` |
| Monthly ARPU | `[$ ]` | revenue ÷ active customers | `[date]` |
| Gross margin | `[ ]%` | `[source]` | `[date]` |
| Expected lifetime (months) | `[ ]` | Q10.2 | `[date]` |
| LTV | `[$ ]` | ARPU × margin × lifetime | `[date]` |
| LTV : CAC | `[ ]` | LTV ÷ CAC | `[date]` |
| Payback (months) | `[ ]` | CAC ÷ (ARPU × margin) | `[date]` |
| Net revenue retention (B2B) | `[ ]%` | see Part 10 | `[date]` |

**Q14.2 [REQUIRED] Do we earn back what we spend to win a customer, and how fast?**
Answer: `[Yes/No/Not yet known]. Payback [ ] months. LTV:CAC [ ]. Confidence: [High/Medium/Low] because [reason].`

**Q14.3 [REQUIRED] Do the numbers include all costs (tools, people time, discounts, refunds)?**
Answer: `[ ] Yes   [ ] No. Missing: [list]`

---

# 15. Satisfaction and Customer Voice

## 15.1 Survey Scores by Cohort

| Cohort | Responses | NPS | CSAT | "Very disappointed" (PMF) |
|---|---|---|---|---|
| `[Beta customers]` | `[ ]` | `[ ]` | `[ ]` | `[ ]%` |
| `[Launch customers]` | `[ ]` | `[ ]` | `[ ]` | `[ ]%` |
| `[Growth customers]` | `[ ]` | `[ ]` | `[ ]` | `[ ]%` |

**Q15.1 [REQUIRED] When and how do we ask the PMF question ("How would you feel if you could no longer use this product?")?**
Answer: `Ask customers who used the product at least [ ] times, at day [ ]. Options: Very disappointed / Somewhat disappointed / Not disappointed.`

**Q15.2 [REQUIRED] What are the top 3 things customers love, with counts?**
Answer: `1. [ ] ([n])  2. [ ] ([n])  3. [ ] ([n])`

**Q15.3 [REQUIRED] What are the top 3 things that annoy or confuse them, with counts?**
Answer: `1. [ ] ([n])  2. [ ] ([n])  3. [ ] ([n])`

**Q15.4 [REQUIRED] Who are the customers who would be "very disappointed" to lose us? What do they have in common?**
Answer: `[Describe who they are, why they use it, and what they use it for]`

**Q15.5 [REQUIRED] How many customer interviews have we done, and what did we learn?**
Answer: `[n] interviews between [date] and [date]. Main lessons: [ ]`

**Q15.6 [OPTIONAL] What do support tickets say?**
Answer: `Top 3 ticket topics: [ ]. Ticket volume per 100 customers: [ ].`

---

# 16. Customer Milestone Tracker (Customers 1 to 500)

| Milestone | Date reached | Days since previous | Main channel in this group | Week-4 retention of group | Notes |
|---|---|---|---|---|---|
| Customer #1 | `[YYYY-MM-DD]` | n/a | `[ ]` | `[ ]%` | `[ ]` |
| #10 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #25 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #50 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #100 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #150 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #200 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #250 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #300 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #400 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |
| #500 | `[ ]` | `[ ]` | `[ ]` | `[ ]%` | `[ ]` |

**Q16.1 [REQUIRED] Is customer growth speeding up, steady, or slowing down?**
Answer: `[ ] Speeding up   [ ] Steady   [ ] Slowing. Evidence: [days between milestones].`

**Q16.2 [REQUIRED] Did anything change at specific milestones (new feature, new price, new channel, bug)?**
Answer: `[Date, change, effect on metrics]`

---

# 17. Insights and Findings

> Write each insight in this exact 4-part sentence style so anyone can understand it and act on it.

| # | What we saw (with numbers) | Why we think it happened | How sure are we (High / Medium / Low) | What we will do |
|---|---|---|---|---|
| I1 | `[e.g., Referral customers keep 48% at week 4 vs 21% for ads (n=62 vs n=140)]` | `[ ]` | `[ ]` | `[ ]` |
| I2 | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| I3 | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q17.1 [REQUIRED] What surprised us most?**
Answer: `[ ]`

**Q17.2 [REQUIRED] What do we still not understand?**
Answer: `[ ]` (add each item to the Action Log in Part 19)

## 17.1 Experiment Log (Tests We Ran on Purpose)

> An experiment changes one thing for some customers and compares the result. Write the plan **before** the test, and the result **after**.

| ID | What we changed (one thing only) | Who got it (cohort / %) | Who did not (comparison group) | Metric we expect to move | Success means | Start | End | Result (numbers) | Decision (Keep / Drop / Retest) |
|---|---|---|---|---|---|---|---|---|---|
| E1 | `[e.g., shorter onboarding]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| E2 | `[e.g., new price on Pro plan]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q17.3 [REQUIRED] Do we have enough customers for the test to mean something?**
Answer: `Test group n=[ ], comparison group n=[ ]. If either is under [30], label the result LOW SAMPLE and do not treat it as final.`

**Q17.4 [REQUIRED] Did anything else change during the test (release, campaign, AI version in Q4.6)?**
Answer: `[Yes: describe / No]`

---

# 18. Growth Validation Scorecard and Decision (Complete at Customers 100, 250 and 500)

> Targets are set **before** you look at results. Writing targets after seeing results is cheating yourself.

## 18.0 Starting Guidance by Product Type (Rough Guesses, Not Facts)

> These ranges are rough starting points so you are not staring at a blank box. They vary widely by market, price and audience. **Replace them with your own numbers within your first week of Phase 1, and write where your numbers came from** (competitors, past projects, interviews). Do not treat them as pass/fail rules from any authority.

| What to set | B2C app / consumer | B2B SaaS | Marketplace |
|---|---|---|---|
| Activation rate (did key action in time) | `[start guess: 30-50%]` | `[start guess: 40-60% of accounts]` | `[start guess: 20-40% of each side]` |
| Retention check-point | Week 4: `[start guess: 15-25%]` | Month 3 accounts still active: `[start guess: 70-85%]` | Month 3 repeat activity: `[start guess: 20-35%]` |
| Monthly churn (paying) | `[start guess: under 8%]` | `[start guess: under 3% per month]` | `[start guess: depends on side; set per side]` |
| Retention curve flattens? | `[Within 8-12 weeks]` | `[Within 3-6 months]` | `[Within 8-12 weeks]` |
| "Very disappointed" score | `[40% rule of thumb]` | `[40% rule of thumb]` | `[40% rule of thumb, ask each side]` |
| LTV : CAC | `[start guess: 3 or more]` | `[start guess: 3 or more]` | `[start guess: 3 or more]` |
| Payback | `[start guess: under 6 months]` | `[start guess: under 12 months]` | `[start guess: under 12 months]` |
| Special metric | Stickiness (DAU ÷ MAU) `[ ]%` | Net revenue retention `[start guess: above 100%]` | Liquidity (listings that sell) `[ ]%` |

**Q18.0 [REQUIRED] Where did our own targets come from?**
Answer: `[Competitor info / past project / interviews / expert advice / educated guess]. Set on [date] by [name].`

| # | Question | Your target (agree in advance) | Actual | n | 🟢/🟡/🔴 |
|---|---|---|---|---|---|
| 1 | Do customers reach the key action? | Activation rate ≥ `[ ]%` | `[ ]%` | `[ ]` | `[ ]` |
| 2 | Do they come back? | Week-4 retention ≥ `[ ]%` | `[ ]%` | `[ ]` | `[ ]` |
| 3 | Does retention flatten? | Curve flattens by week `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 4 | Is it getting better with newer cohorts? | Newer cohorts ≥ older cohorts | `[ ]` | `[ ]` | `[ ]` |
| 5 | Would they miss us? | "Very disappointed" ≥ `[40]%` (common rule of thumb) | `[ ]%` | `[ ]` | `[ ]` |
| 6 | Will they pay? | Conversion to paid ≥ `[ ]%` | `[ ]%` | `[ ]` | `[ ]` |
| 7 | Do we earn back acquisition cost? | Payback ≤ `[ ]` months; LTV:CAC ≥ `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 8 | Is there a channel that works repeatably? | At least `[1]` channel meeting targets | `[ ]` | `[ ]` | `[ ]` |
| 9 | Does quality hold as we grow? | Support tickets per 100 customers ≤ `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 10 | Is the data trustworthy? | Part 20 checklist 100% passed | `[ ]` | n/a | `[ ]` |

**Scorecard result:** `[ ]` green, `[ ]` yellow, `[ ]` red.

## 18.1 Decision

**Q18.1 [REQUIRED] What is our decision?**
Answer: `[ ] GO: invest in growth   [ ] FIX FIRST: fix specific problems then re-test   [ ] PIVOT: change who or what   [ ] STOP`

**Q18.2 [REQUIRED] Why? (Maximum 5 sentences, with numbers)**
Answer: `[ ]`

**Q18.3 [REQUIRED] What must be true to start growth spending safely?**
Answer: `[ ]`

**Q18.4 [REQUIRED] What are we most afraid of getting wrong?**
Answer: `[ ]`

**Q18.5 [REQUIRED] Who decided and when?**
Answer: `[Names, role, YYYY-MM-DD]`

---

# 19. Action Log (Every UNKNOWN and Every Next Step Goes Here)

| ID | What needs to happen | Why | Owner | Due date | Status |
|---|---|---|---|---|---|
| A1 | `[ ]` | `[ ]` | `[ ]` | `[YYYY-MM-DD]` | `[Open/Doing/Done]` |
| A2 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| A3 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

---

# 20. Quality and Data-Accuracy Checklist (Run Before Sharing Any Numbers)

**Counting**
- [ ] Test accounts, team members and fake signups are excluded.
- [ ] Each customer appears once (no duplicates).
- [ ] Customer total here matches the source of truth (Q7.2). Difference: `[ ]`
- [ ] Cohort sizes add up to the total customer count.

**Time**
- [ ] Same time zone everywhere.
- [ ] Incomplete periods (the current week or month) are not shown as final numbers.
- [ ] Dates were checked at the edges (week and month starts).

**Definitions**
- [ ] "Active" and "churned" match Part 5 exactly.
- [ ] The same metric formula was used for all cohorts.

**Math**
- [ ] Percentages have a numerator and a denominator written down.
- [ ] Two numbers were recalculated by hand or by a second person.
- [ ] Revenue matches payment records.
- [ ] Refunds and discounts are handled consistently.

**Interpretation**
- [ ] Cohorts under the minimum size are marked LOW SAMPLE.
- [ ] Conclusions are not based on one unusual cohort.
- [ ] We checked whether a launch, campaign or bug explains a spike or drop.
- [ ] We looked for survivorship bias (only counting people who stayed).

**Privacy**
- [ ] No names, emails, phone numbers or other PII in this file.
- [ ] Shared with approved people only.

**Result:** `[ ] Passed on [date] by [name]   [ ] Failed. Issues: [list]`

---

# 21. Assumptions, Risks and Change Log

## 21.1 Assumptions

| # | Assumption | How we will check it | Check by | Result |
|---|---|---|---|---|
| 1 | `[ ]` | `[ ]` | `[date]` | `[ ]` |

## 21.2 Risks

| # | What could go wrong | Likelihood (L/M/H) | Impact (L/M/H) | What we do about it | Owner |
|---|---|---|---|---|---|
| 1 | `[e.g., Only friends of the team signed up, so retention looks too good]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 2 | `[e.g., Tracking breaks after an app update]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 3 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

## 21.3 Change Log (Record Every Definition or Structure Change)

| Date | What changed | Why | Changed by | Effect on past numbers |
|---|---|---|---|---|
| `[YYYY-MM-DD]` | `[ ]` | `[ ]` | `[ ]` | `[Past numbers recalculated / Not affected]` |

---

# 22. Sign-Off

| Role | Name | Date | Approved? |
|---|---|---|---|
| Document owner | `[ ]` | `[ ]` | `[ ]` |
| Product lead | `[ ]` | `[ ]` | `[ ]` |
| Engineering lead | `[ ]` | `[ ]` | `[ ]` |
| Data / QA reviewer | `[ ]` | `[ ]` | `[ ]` |
| Business / finance lead | `[ ]` | `[ ]` | `[ ]` |

---

# Appendix A. Worked Mini-Example (How a Finished Section Looks)

**Product:** PlantPal (B2C app). **Key action:** "Added 3 plants". **Active week:** at least 1 reminder completed.

| Signup week | n | Week 0 | Week 1 | Week 2 | Week 4 |
|---|---|---|---|---|---|
| 2026-W10 | 42 | 100% | 61% | 48% | 38% |
| 2026-W11 | 55 | 100% | 64% | 52% | 41% |
| 2026-W12 | 61 | 100% | 70% | 57% | 45% |

*Reading it:* Each newer week keeps more customers (week-4: 38% → 41% → 45%). Source: events export, 2026-04-02. Confidence: Medium (cohorts have 42-61 customers; test accounts excluded).

*Insight (Part 17 style):* "Customers who added 3 plants on day 1 keep 52% at week 4 vs 19% for others (n=88 vs n=70). We think early success builds the habit. Confidence: Medium. Action: make 'add 3 plants' the first onboarding goal."

## A.2 Mini-Example: B2B SaaS (counted by accounts)

**Product:** TeamTasks (B2B). **Account** = a company. **Key action:** "Invited 2 teammates and created a project." **Active month:** at least 3 users did something in the account.

| Signup month | Accounts (n) | Activated within 14 days | Month 1 active | Month 2 active | Month 3 active | Revenue vs start (NRR) |
|---|---|---|---|---|---|---|
| 2026-05 | 18 | 11 (61%) | 83% | 78% | 72% | 104% |
| 2026-06 | 24 | 17 (71%) | 88% | 83% | `[not yet]` | 101% |

*Reading it:* Newer accounts activate more (61% to 71%). Month-3 active is 72% for May. Source: events and billing exports, 2026-09-05. Confidence: Low to Medium because only 18-24 accounts per cohort (under the 30 minimum, labelled LOW SAMPLE).

*Insight:* "Accounts that invited 2 or more teammates in week 1 are active at month 3 at 85% vs 40% for others (n=14 vs n=10). We think teams need each other to get value. Confidence: Low. Action: prompt for invites during onboarding and keep collecting data."

## A.3 Mini-Example: Marketplace (two sides)

**Product:** LocalCraft (buyers and sellers of handmade items). **Seller key action:** "Listed 3 items". **Buyer key action:** "Completed first purchase". **Active week (seller):** at least 1 item viewed, messaged or sold.

| Signup month | Side | n | Did key action in 14 days | Week-4 active | Repeat (2+ transactions) |
|---|---|---|---|---|---|
| 2026-07 | Sellers | 40 | 22 (55%) | 45% | n/a |
| 2026-07 | Buyers | 120 | 30 (25%) | 18% | 9% |

| Seller cohort | Listings | Listings sold within 30 days | Liquidity |
|---|---|---|---|
| 2026-07 | 130 | 26 | 20% |

*Reading it:* Sellers join and list, but only 20% of listings sell, so buyers are the bottleneck. Source: marketplace database export, 2026-09-02. Confidence: Medium.

*Insight:* "Sellers with at least one sale in 14 days are active at week 4 at 78% vs 22% for sellers with no sale (n=14 vs n=26). We think first sales keep sellers around. Confidence: Medium. Action: focus the next channel test on buyers in the areas where sellers are located."

# Appendix B. Common Mistakes to Avoid

1. Counting signups instead of real customers (Q5.4).
2. Changing the definition of "active" after seeing results.
3. Mixing test accounts and real customers.
4. Showing the current, unfinished week as if it were final.
5. Judging a channel on signups instead of customers who stay.
6. Drawing strong conclusions from fewer than 30 customers.
7. Averaging all customers together and hiding cohort differences.
8. Forgetting costs (tools, discounts, refunds, time) in CAC.
9. Writing targets after seeing the results.
10. Copying personal information into this file.

# Appendix C. Quick Calculation Cheat Sheet

- Percent = (part ÷ whole) × 100. Always write both numbers.
- Retention at week N = active in week N ÷ cohort size.
- Churn = 100% − retention (for the same period and definition).
- CAC = spend ÷ new customers.
- Payback months = CAC ÷ (monthly ARPU × gross margin).
- NPS = % scoring 9-10 minus % scoring 0-6.

# Appendix D. Final "Is This Document Ready?" Test

- [ ] No `[square brackets]` remain unless marked `UNKNOWN` with an Action Log entry.
- [ ] Every number has a source and date.
- [ ] Parts 9 and 20 are fully ticked.
- [ ] A person who has never seen the project could understand Parts 5, 17 and 18.
- [ ] The decision in Part 18 can be explained in under one minute.
