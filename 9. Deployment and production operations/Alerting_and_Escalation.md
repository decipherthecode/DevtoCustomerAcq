# How to Fill This Document

**Read this first. It takes 2 minutes.**

## What is this document?
This document answers one big question: **"When something goes wrong with our product, who finds out, how fast, and what do they do?"**

- An **alert** is a warning message (a text, call, email, or chat ping) that says "something is broken or about to break."
- An **escalation** is passing the problem to the next person (or to a more senior person) when the first person cannot fix it in time.
- An **incident** is any moment when real customers are hurt, or could soon be hurt, by a problem.

## How to fill it in (5 simple rules)
1. **Go in order.** Start at Section 0 and move down. Do not skip around.
2. **Answer every question under "Your answer:".** Write plain sentences. Short is fine.
3. **Never leave a blank.** If you don't know, write `UNKNOWN - [name] will find out by [date]`. If a question does not apply, write `N/A - because [reason]`. A blank means someone will have to guess later, and guessing during an outage is dangerous.
4. **Use real names, real numbers, real links.** Not "soon" but "within 5 minutes". Not "the team" but "Priya (priya@example.com, +1-555-0100)".
5. **Look at the "Example answer" under each question** to see what a good answer looks like. Then replace it with your own.

## Symbols used
- `[ ]` = a box to tick. Change it to `[x]` when done or true.
- `<angle brackets>` = replace this with your own information.
- **Phase tags** tell you when an answer is needed:
  - **[BUILD]** = needed while you are still building the product
  - **[PRE-LAUNCH]** = needed before the first real customer arrives
  - **[LAUNCH]** = needed on launch day and the first weeks
  - **[1-500]** = needed while growing from customer 1 to customer 500

## Who should fill it, and when?
- **Who:** the project owner, with one other person (or an AI assistant) reading it back to check for missing answers.
- **When:** fill Sections 0-3 during build; Sections 4-10B before launch; Sections 11-12 as people and facts change; review everything again at launch day, at 100 customers, and at 500 customers.
- **Appendices:** A is a filled example to learn from, B is a runbook (fix guide) to copy, C is a postmortem (review form) to copy.
- **For AI agents:** if an AI agent reads this file, it must treat unanswered questions as "ask a human," never as permission to guess.

## Finished? Final check
Before you call this document done, confirm:
- [ ] No question is blank (every answer is a real answer, `UNKNOWN - ...`, or `N/A - ...`)
- [ ] Every person named has a working phone number or contact method
- [ ] You sent a **test alert** and a person really received it (Section 9)
- [ ] A second person read the document and said "I could run an incident with only this file"

---

# 0. Document Control

**Q0.1 What is the name of the product or project?**
Example answer: *"PetPal - an app that reminds owners to feed their pets."*
**Your answer:**

**Q0.2 Who owns this document (one named person)?**
Example answer: *"Sam Lee, sam@example.com"*
**Your answer:**

**Q0.3 What is today's date, and what version is this?**
Example answer: *"2026-10-18, v1.0"*
**Your answer:**

**Q0.4 Which phase is the project in right now?** (Choose one: BUILD / PRE-LAUNCH / LAUNCH / 1-500)
**Your answer:**

**Q0.5 When will this document be reviewed again?** (Set specific dates.)
Example answer: *"On launch day, at 100 customers, at 500 customers, and after every SEV1 incident."*
**Your answer:**

---

# 1. Know Your Product (so alerts make sense)

**Q1.1 In one or two sentences, what does the product do for a customer?**
Example answer: *"Customers log in, add their pets, and get a reminder on their phone."*
**Your answer:**

**Q1.2 What are the 3-5 most important things a customer must be able to do?** (If any of these stop working, it is an emergency.)
Example answer: *"1. Sign up. 2. Log in. 3. Receive reminders. 4. Pay for a subscription."*
**Your answer:**

**Q1.3 What parts is the product made of?** List every piece that could break (website, app, database, payment provider, email service, AI model provider, hosting company, etc.).
Example answer: *"Website on Vercel, database on Supabase, payments through Stripe, emails through Resend, AI replies through an AI provider."*
**Your answer:**

**Q1.4 Which of those parts are run by other companies that we cannot fix ourselves?** (For these, alerts mean "check their status page and tell customers," not "fix it.")
**Your answer:**

**Q1.5 Where are the status pages of those outside companies?**
Example answer: *"Stripe: status.stripe.com"*
**Your answer:**

**Q1.6 What does "normal" look like?** (Typical number of visitors, typical speed of the site, typical errors per day.)
Example answer: *"About 200 visits a day, pages load in under 2 seconds, fewer than 5 errors a day."*
**Your answer:**

---

# 2. Severity Levels (how bad is it?)

Severity is a simple scale that tells everyone how urgent a problem is. Use the same scale in every project. You may change the examples, but not the response times without writing why.

| Level | Plain meaning | Example | Who is woken up? | Must start responding within |
|---|---|---|---|---|
| **SEV1 - Critical** | Product is down or data/money/security is at risk for many customers | Nobody can log in; payments failing; data leak | Everyone needed, day or night | **5-15 minutes** |
| **SEV2 - Major** | An important feature is broken or very slow for many customers | Reminders are not sending | Primary person, day or night | **30 minutes** |
| **SEV3 - Minor** | Something is wrong but customers can still do their main tasks | One page looks wrong; slow for a few people | Primary person, work hours only | **Next business day** |
| **SEV4 - Low** | Small annoyance or a warning sign | Disk is 70% full | Nobody woken; goes into a to-do list | **Within 1 week** |

**Q2.1 Do you agree with the table above, or do you want to change anything?** (If you change any time, write why.)
**Your answer:**

**Q2.2 Write 2 real examples from YOUR product for each level.**
**Your answer:**
- SEV1:
- SEV2:
- SEV3:
- SEV4:

**Q2.3 What is the one-sentence rule when you are unsure which level to pick?**
Recommended answer: *"When unsure, pick the higher (more serious) level. We can lower it later."*
**Your answer:**

**Q2.4 Who has the right to declare a SEV1, and can anyone (including a customer-support person or an AI agent) do it?**
**Your answer:**

---

# 3. What Triggers an Alert? (alert rules)

An alert should fire when a **customer is hurt or about to be hurt**, not for every tiny change. Too many alerts cause "alert fatigue": people start ignoring them.

**Q3.1 For each important customer action in Q1.2, how will you know it broke?** Fill the table.

| Customer action | How we check | Alert fires when... | Severity | Where is the alert set up (link)? |
|---|---|---|---|---|
| Example: Log in | Test login every 1 minute | 3 failures in a row | SEV1 | <link> |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

**Q3.2 Which of these standard checks will you use?** Tick all that apply and add the tool name and threshold.
- [ ] **Uptime check** (is the site reachable?) - tool: ______  fires after ____ minutes down
- [ ] **Error rate** (too many errors) - tool: ______  fires above ____% of requests
- [ ] **Speed** (too slow) - tool: ______  fires when slower than ____ seconds
- [ ] **Payments failing** - tool: ______  fires after ____ failures
- [ ] **Database or storage nearly full** - tool: ______  fires at ____% full
- [ ] **Background jobs not running** (reminders, emails) - tool: ______  fires if silent for ____ minutes
- [ ] **Security signals** (many failed logins, strange admin activity) - tool: ______
- [ ] **Money/cost spike** (cloud or AI bill jumps) - tool: ______  fires above $____ per day
- [ ] **AI quality problems** (AI answers failing, timing out, or behaving strangely) - tool: ______
- [ ] **Certificate or domain expiring** - tool: ______  fires ____ days before
- [ ] **Customer complaints spike** (support messages, bad reviews) - tool: ______

**Q3.3 How will you stop false alarms and alert fatigue?**
Example answer: *"An alert must fire only after 3 failed checks in a row. Every month we delete or fix any alert that fired and needed no action."*
**Your answer:**

**Q3.4 What is the rule for every alert?** (Recommended: *"Every alert must say what is broken, how bad it is, and link to a runbook (the step-by-step fix guide). If an alert needs no action, delete it."*)
**Your answer:**

**Q3.5 What should an alert message always contain?** Tick the minimum.
- [ ] What is broken (plain words)
- [ ] Severity level
- [ ] Since when
- [ ] Which customers or how many are affected
- [ ] Link to the dashboard
- [ ] Link to the runbook (fix guide)
- [ ] Who owns it

---

# 4. Who Gets Alerted? (on-call)

**On-call** means one person is responsible for answering alerts during a set period (for example, this week). With 1-3 people, it can be simple, but it must still be written down.

**Q4.1 Who is on-call, and in what order do we try people?** Fill the table (this is the **escalation ladder**).

| Step | Who | Contact method (phone, SMS, chat, email) | If no answer within... then go to next step |
|---|---|---|---|
| 1 - Primary on-call |  |  | 5 minutes |
| 2 - Backup |  |  | 10 minutes |
| 3 - Project owner / founder |  |  | 15 minutes |
| 4 - Last resort (e.g., outside expert or hosting-company emergency support) |  |  | - |

**Q4.2 How do we make sure a person actually wakes up?** (Chat messages alone are not enough at night.)
Example answer: *"The paging tool sends a push notification, then an SMS after 2 minutes, then a phone call after 5 minutes."*
**Your answer:**

**Q4.3 Which paging/alerting tool do we use?** (Examples: PagerDuty, Opsgenie, Better Stack, Grafana OnCall, or a simple phone call tree if solo.)
**Your answer:**

**Q4.4 What are the on-call hours?** Do we cover nights and weekends? Which severity levels wake people at night?
**Your answer:**

**Q4.5 How does the on-call duty rotate, and how do people swap?**
Example answer: *"Each person is on-call one week, Monday to Monday. Swaps are agreed in chat and written in the schedule."*
**Your answer:**

**Q4.6 What happens if the primary person is on holiday, sick, or has no phone signal?**
**Your answer:**

**Q4.7 When must the on-call person escalate (pass the problem up) instead of fixing it alone?** Tick all that apply.
- [ ] They have no idea what is wrong after ____ minutes
- [ ] They cannot fix it within ____ minutes
- [ ] Customer data, money, or security might be involved
- [ ] The problem is in another company's service
- [ ] The problem is getting worse
- [ ] They feel unsure or unsafe making a change
- [ ] Other: ____________________

**Q4.8 Is it OK to escalate early?** (Recommended answer: *"Yes. Nobody is ever blamed for asking for help too early."*)
**Your answer:**

---

# 5. During an Incident (what people do)

**Q5.1 Who is the "Incident Lead"?** (The one person who makes decisions and keeps everyone organized. In a tiny team, this may be the same person fixing the problem. Write who.)
**Your answer:**

**Q5.2 Where do we talk during an incident?** (One chat room or call link, same every time.)
**Your answer:**

**Q5.3 What are the first 5 steps anyone follows when an alert arrives?** (Recommended default below; edit to fit.)
1. **Acknowledge:** press "I am looking at it" in the paging tool so others know.
2. **Check:** is it real? Open the dashboard. Is a customer hurt?
3. **Label:** pick the severity (Section 2).
4. **Stop the bleeding first:** the fastest safe action (roll back the last release, switch a feature off, restart) comes before finding the root cause.
5. **Tell people:** post an update in the incident chat and, for SEV1/SEV2, start customer communication (Section 6).

**Your changes or additions:**

**Q5.4 Where is the "runbook" (step-by-step fix guide) for each common problem?** List links.

| Problem | Runbook link | Who wrote it | Last tested on |
|---|---|---|---|
| Site is down |  |  |  |
| Payments failing |  |  |  |
| Database problem |  |  |  |
| Bad release / need to undo |  |  |  |
| Security concern |  |  |  |

**Q5.5 How do we undo the last change (rollback) in under 10 minutes?** Write the exact steps or link.
**Your answer:**

**Q5.6 How often should the Incident Lead post an update in the incident chat?**
Recommended answer: *"SEV1: every 15 minutes. SEV2: every 30 minutes. Even if the update is 'still working, nothing new.'"*
**Your answer:**

**Q5.7 What must NOT be done without asking the owner first?** (Examples: deleting data, changing passwords for everyone, turning off security protections, spending money.)
**Your answer:**

**Q5.8 When is the incident "over"?**
Recommended answer: *"Customers can do the actions in Q1.2 again, the alert has stopped, and we watched for 30 minutes with no repeat."*
**Your answer:**

---

# 6. Telling Customers and Other People

**Q6.1 Who needs to be told, and when?**

| Who | Tell them for which severity | How | Within how long | Who sends it |
|---|---|---|---|---|
| Customers (status page) | SEV1, SEV2 |  | 15 minutes |  |
| Customers (email or in-app message) | SEV1 or data/security issue |  |  |  |
| Founder / owner | SEV1, SEV2 |  |  |  |
| Investors / partners | SEV1 longer than ____ |  |  |  |
| Support team (so they can answer messages) | SEV1, SEV2 |  |  |  |
| Legal / privacy contact | Any data or security issue |  | Immediately |  |
| Payment/hosting providers | When their service is involved |  |  |  |

**Q6.2 Where is the public status page?** (A web page telling customers what is happening.)
**Your answer:**

**Q6.3 Write the four message templates now, so nobody has to invent words in a crisis.** Keep them short, honest, and free of blame and technical jargon.

- **"We are investigating":**
  *Example: "Some customers cannot log in. We are looking into it and will update you in 30 minutes."*
  **Your version:**
- **"We found the cause / we are fixing it":**
  **Your version:**
- **"Fixed":**
  **Your version:**
- **"What happened and what we are changing" (after SEV1):**
  **Your version:**

**Q6.4 What is our promise to customers?** (Example: *"We will always tell you within 30 minutes if something big is wrong, and we will never hide it."*)
**Your answer:**

**Q6.5 Who is allowed to speak publicly (social media, press) about an incident?**
**Your answer:**

**Q6.6 If customer data or privacy might be affected, what must we do and by when?** (Rules differ by country and customer type. Ask a lawyer and write the answer here. This is a template, not legal advice.)
**Your answer:**

## 6A. Rules That Apply to Us (tick every one that applies)

**Q6.7 Which of these rules apply to our product?** For each ticked rule, fill in the "what we must do" line.

- [ ] **Privacy / data breach: GDPR (Europe/UK), CCPA/CPRA (California), other: ______**
  - Who decides whether personal data was exposed? ______
  - Deadline to tell the regulator (GDPR is generally 72 hours after we become aware, where required): ______
  - Deadline and method to tell affected customers: ______
  - Who is our privacy/legal contact? ______
- [ ] **Payments: PCI DSS (we take or store card payments)**
  - Do we only use a payment provider that handles card numbers for us? Yes / No: ______
  - Who do we call at the payment provider if payments are attacked or fail? ______
  - Where do we keep logs and proof of alerts? ______
- [ ] **Security audits: SOC 2, ISO 27001, or customer security questionnaires**
  - Where is the evidence kept (alert history, on-call schedule, postmortems, test results)? ______
  - How long do we keep it? ______
- [ ] **Health data: HIPAA (US) or similar**
  - Who is the security/privacy officer? ______
  - Who must be told within what time if health data is exposed? ______
- [ ] **Children's data: COPPA (US), age-appropriate design rules, or similar**
  - Who must be told, and how fast, if a child's data is exposed? ______
  - Any extra rule that makes escalation faster? ______
- [ ] **None of these apply.** Why do we believe that, and who checked? ______

**Q6.8 Who confirmed with a lawyer or compliance expert that Q6.7 is correct, and when?**
**Your answer:**

**Q6.9 Any suspected data leak, security break-in, or child/health data exposure is automatically at least which severity?** (Recommended: *SEV1, and the legal/privacy contact is told immediately.*)
**Your answer:**

---

# 7. After the Incident (learn and improve)

**Q7.1 When do we write a short review (postmortem)?**
Recommended answer: *"After every SEV1 and SEV2, within 3 business days."*
**Your answer:**

**Q7.2 Where do postmortems get saved?** (A link or folder.)
**Your answer:**

**Q7.3 What does each postmortem contain?** Tick the minimum (recommended: all).
- [ ] What happened, in plain words, with a timeline
- [ ] How many customers were affected and for how long
- [ ] How we found out (alert or customer?)
- [ ] The root cause (why it really happened)
- [ ] What went well and what went badly
- [ ] Action items: each with **one owner** and **a due date**

**Q7.4 What is our rule about blame?** (Recommended: *"We fix systems and habits, not blame people."*)
**Your answer:**

**Q7.5 Who checks that action items actually get done, and when?**
**Your answer:**

---

# 8. Using AI Agents Safely

If AI agents help watch, sort, or fix problems, the rules must be written down. Fill in every row.

**Q8.1 What AI agents (if any) are involved in alerting and incidents?**
Example answer: *"A monitoring agent reads alerts and groups duplicates. A support agent drafts customer replies."*
**Your answer:**

**Q8.2 What may an AI agent do, and what needs a human?**

| Action | AI may do alone | AI may suggest, human approves | AI must never do |
|---|---|---|---|
| Read logs and dashboards | [ ] | [ ] | [ ] |
| Group duplicate alerts and propose a severity | [ ] | [ ] | [ ] |
| Page a human | [ ] | [ ] | [ ] |
| Draft a status page or customer message | [ ] | [ ] | [ ] |
| Publish a customer message | [ ] | [ ] | [ ] |
| Restart a service or roll back a release | [ ] | [ ] | [ ] |
| Change database data or settings | [ ] | [ ] | [ ] |
| Spend money or change access/passwords | [ ] | [ ] | [ ] |

**Q8.3 Who is the named human responsible for what the AI agents do?**
**Your answer:**

**Q8.4 How do we know an AI agent is behaving badly?** (Examples: sending wrong messages, looping, using too much money.)
**Your answer:**

**Q8.5 How does a human turn the AI agent off in an emergency ("kill switch")?** Write exact steps.
**Your answer:**

**Q8.6 What do AI agents do when they are unsure?** (Recommended: *"Stop, page a human, and say exactly what they are unsure about. Never guess on SEV1 or on anything involving customer data."*)
**Your answer:**

**Q8.7 Is every AI action written in a log a human can read later?**
**Your answer:**

---

# 9. Prove It Works (test before you trust)

An alert nobody has tested is just a hope.

**Q9.1 Did we send a real test alert to each person on the ladder in Q4.1?**
- [ ] Primary received it on ____ (date) in ____ minutes
- [ ] Backup received it on ____ (date) in ____ minutes
- [ ] Owner received it on ____ (date) in ____ minutes

**Q9.2 Did we practice one fake incident ("fire drill")?** What did we learn?
**Your answer:**

**Q9.3 How often will we test alerts and run a drill?**
Recommended answer: *"Test alerts monthly. Run a drill before launch and every 3 months."*
**Your answer:**

**Q9.4 Final test: could a new person run an incident using only this document?** Who tried it, and what was confusing?
**Your answer:**

---

# 10. The Phases: What You Need and When

Tick each box when it is true. Do not move to the next phase until the current phase is fully ticked.

## Phase 1 - BUILD (still making the product)
- [ ] Sections 0, 1, 2 filled in
- [ ] Basic error logging turned on in development
- [ ] Uptime check on the test version
- [ ] Runbook started for "undo the last change"
- [ ] AI-agent rules (Section 8) drafted, if agents are used

## Phase 2 - PRE-LAUNCH (before customer number 1)
- [ ] Sections 3-9 completely filled in
- [ ] Alerts exist for every action in Q1.2
- [ ] Test alerts reached every person on the ladder
- [ ] Rollback tested end-to-end (Q5.5)
- [ ] Status page live and message templates ready
- [ ] Fire drill done
- [ ] Cost/budget alert set
- [ ] Contact list checked (everyone has phone, backup contact)

## Phase 3 - LAUNCH (launch day and the first 2-4 weeks)
- [ ] Someone is on-call and available during the launch window (name: ____)
- [ ] Dashboard open and watched on launch day
- [ ] Support inbox watched, and the support team knows the escalation steps
- [ ] Alert thresholds checked against real traffic after day 1, day 3, and day 7
- [ ] Noisy alerts removed or fixed

## Phase 4 - CUSTOMERS 1 to 500
Review this document at each milestone and write the date.

| Milestone | What to check | Reviewed on | Reviewed by |
|---|---|---|---|
| 10 customers | Are alerts too noisy or too quiet? |  |  |
| 100 customers | Is one on-call person still enough? Are thresholds still right? Is the database/cost growing as expected? |  |  |
| 250 customers | Do we need a second support person or a better paging tool? |  |  |
| 500 customers | Rewrite thresholds. Consider formal on-call pay, 24/7 coverage, and an uptime promise (SLA). |  |  |

**Q10.1 What number of customers or what event makes us upgrade our on-call setup?**
**Your answer:**

**Q10.2 What do we promise customers about uptime (for example, 99.5% each month)?** Have we told them? (Write "N/A - no promise yet" if none.)
**Your answer:**

## 10A. Service Goals (how good do we promise to be?)

An **SLO** is our own goal (for example, "the site works 99.5% of the time"). An **SLA** is a promise we make to customers, often with a refund if we miss it. Start with goals; make promises only when you can keep them.

**Q10.3 Fill in the goals table.**

| Goal | Our target | How we measure it | Told to customers? (Yes/No) |
|---|---|---|---|
| Uptime per month (example: 99.5%) |  |  |  |
| Login success rate (example: 99.9%) |  |  |  |
| Page speed (example: 95% of pages under 2 seconds) |  |  |  |
| Support first reply time (example: within 4 hours) |  |  |  |
| SEV1 first response (from Section 2) |  |  |  |

**Helper:** 99.5% uptime allows about 3.6 hours of downtime in a 30-day month. 99.9% allows about 43 minutes. 99% allows about 7.2 hours.

**Q10.4 What do we do if we miss a goal?** (Example: *"Write a postmortem, and if it is a customer promise, offer a credit or apology within 5 business days."*)
**Your answer:**

## 10B. Budget for Alerting and On-Call

**Q10.5 What do alerting, monitoring, and on-call cost us each month, and what is the maximum we will spend?**

| Item | Tool / provider | Cost per month | Maximum allowed |
|---|---|---|---|
| Monitoring and uptime checks |  |  |  |
| Paging / on-call tool |  |  |  |
| Status page |  |  |  |
| Log storage |  |  |  |
| AI agent usage (monitoring and support) |  |  |  |
| Compensation or time off for on-call people |  |  |  |
| **Total** |  |  |  |

**Q10.6 What is the daily spend limit that triggers a cost alert for cloud and AI usage?** (Connect this to the cost check in Q3.2.)
**Your answer:**

**Q10.7 How are on-call people compensated or rested?** (Example: *"A day off after any night-time SEV1."*)
**Your answer:**

**Q10.8 What happens to the budget at 100 and 500 customers?** (Costs usually grow.)
**Your answer:**

---

# 11. Contact Directory (keep this up to date)

| Name | Role | Phone | Email | Time zone | Backup contact |
|---|---|---|---|---|---|
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

**Q11.1 Where are the emergency logins (hosting, domain, payments, paging tool) stored safely?** (Write where. **Never write passwords in this document.**)
**Your answer:**

**Q11.2 Who can get into those logins if the owner cannot be reached?**
**Your answer:**

---

# 12. Open Questions and Change Log

**Q12.1 What is still unknown or undecided?**

| Question | Who will answer | By when |
|---|---|---|
|  |  |  |

**Change log**

| Date | Who | What changed | Why |
|---|---|---|---|
|  |  |  |  |

---

# Final Sign-Off

- [ ] Every question answered (real answer, `UNKNOWN - ...`, or `N/A - ...`)
- [ ] Test alerts received by everyone (Section 9)
- [ ] Second person reviewed and could run an incident with this file alone

**Approved by:** ____________________  **Date:** ____________

---

# Appendix A. Filled Example (fictional app "PetPal")

Use this to see what finished answers look like. Do not copy the facts; copy the level of detail.

- **Q1.2 Most important things:** Sign up, log in, receive feed reminders, pay for Premium.
- **Q2.2 Examples:** SEV1: nobody can log in. SEV2: reminders are late by more than 1 hour. SEV3: pet photos upload slowly. SEV4: database 70% full.
- **Q3.1 Alert row:** Action = "Receive reminders". Check = "A test reminder is sent every 5 minutes and must arrive". Fires when = "2 missed in a row". Severity = SEV2. Link = (dashboard URL).
- **Q4.1 Ladder:** Step 1 Priya (push, then SMS, then call) - 5 min. Step 2 Sam (call) - 10 min. Step 3 Founder Alex (call) - 15 min. Step 4 Hosting company emergency support.
- **Q4.4 Hours:** Nights and weekends covered for SEV1 only. SEV2 wakes the primary between 7am and 11pm. SEV3 and SEV4 wait until work hours.
- **Q5.5 Rollback:** Open the deployment dashboard, click the previous release, press "Promote". Takes about 3 minutes.
- **Q6.3 "We are investigating":** "Some PetPal users cannot log in. We are looking into it and will post another update by 3:30 PM."
- **Q8.2 AI rows:** Reads logs = AI alone. Proposes severity = AI alone. Pages a human = AI alone. Drafts status message = AI alone. Publishes status message = human approves. Rolls back a release = human approves. Changes database data, spends money, or changes access = AI never.
- **Q9.3 Testing:** Test alerts on the 1st of every month; fire drill every 3 months.

---

# Appendix B. Runbook Starter Templates (copy one per problem)

## Runbook: <Problem name, e.g., "Site is down">
- **Owner:** ______   **Last tested:** ______
- **How do I know this is happening?** (alert name, what the customer sees) ______
- **Severity:** ______
- **Step 1 - Check:** What do I look at first? (link) ______
- **Step 2 - Quick safe fix:** (restart / roll back / switch feature off) ______
- **Step 3 - If that did not work, escalate to:** ______ after ____ minutes
- **Step 4 - What do I tell customers?** (template from Q6.3) ______
- **Step 5 - How do I confirm it is fixed?** ______
- **Do NOT:** ______
- **After:** Write a postmortem if SEV1 or SEV2 (Appendix C).

Create at least these three before launch: **Site is down**, **Payments failing**, **Bad release (undo it)**.

---

# Appendix C. Postmortem Template (copy after every SEV1 and SEV2)

- **Title:** ______   **Date:** ______   **Severity:** ______   **Incident Lead:** ______
- **Summary (2-3 plain sentences):** ______
- **Customer impact:** how many customers, which actions broke, for how long ______
- **Timeline** (time, what happened, who did it):
  - ______
- **How did we find out?** Alert / Customer / AI agent / Other: ______  (If a customer told us first, which alert is missing?)
- **Root cause (ask "why?" five times):** ______
- **What went well:** ______
- **What went badly or was confusing:** ______
- **Did the AI agents help, hurt, or do nothing? Did they stay within Section 8 rules?** ______
- **Did we meet our promises to customers (Q6.4) and any legal deadlines (Section 6A)?** ______
- **Action items** (each needs ONE owner and a due date):

| Action | Owner | Due date | Done? |
|---|---|---|---|
|  |  |  | [ ] |

- **Document updates needed:** which answers in this file must change? ______
