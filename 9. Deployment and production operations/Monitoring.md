# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**File:** `Deployment and production operations / Monitoring.md`
**Purpose:** Decide, in plain words, how you will *watch* your product so you find out about problems **before your customers do**, from the first line of code until your first 500 customers.
**Who can fill it:** Anyone. No technical background needed. If you can answer questions about your own product, you can fill this.

## The 7 simple rules

1. **Answer every question.** Never leave a blank. If you don't know, write `NOT SURE` and use the **Safe Default** shown under the question.
2. **Fill in order, top to bottom.** Later sections use your earlier answers.
3. **Four ways to answer** (the question tells you which):
   - `Answer: ________` -> write your own words or a number.
   - `[ ] Yes  [ ] No  [ ] Not sure` -> put an `x` inside one box, like `[x]`.
   - `Pick one: Low / Medium / High` -> delete the ones that don't fit.
   - `Safe Default:` -> a ready-made answer. Keep it unless you have a reason to change it.
4. **Words in `CODE STYLE`** are tool names or technical terms. Each one has a "In plain words" explanation. You never need to look anything up.
5. **Don't invent numbers.** If you don't know a number, write `NOT SURE`. The default will be used and flagged for review.
6. **Date every change.** Add a line to the Change Log (Section 16) whenever you edit.
7. **Done means:** every `________` is replaced, every checkbox is ticked, and Section 15 (Final Checklist) is all `[x]`.

## Key words in plain words

| Word | In plain words |
|---|---|
| **Monitoring** | Watching your product all day and night so you know when something is wrong |
| **Alert** | A message (phone, email, chat) that says "look at this now" |
| **Uptime** | The percentage of time your product is working and reachable |
| **Latency / Speed** | How long a customer waits for something to happen |
| **Error** | Something that failed (a button that doesn't work, a page that crashes) |
| **Log** | A diary the product writes about what it did |
| **Metric** | A number you track over time (e.g., how many people signed up today) |
| **Dashboard** | One screen showing your most important numbers |
| **Incident** | A real problem affecting customers |
| **Runbook** | A step-by-step "what to do when X breaks" guide |
| **Severity** | How bad a problem is (SEV1 = disaster, SEV4 = tiny) |
| **Synthetic check** | A robot that pretends to be a customer every few minutes to test your product |
| **Owner** | The one named person responsible for something |

## Status tags (use these everywhere)

- `TODO` = not started | `DOING` = in progress | `DONE` = finished | `N/A` = does not apply (write why)

---

# 0. DOCUMENT CONTROL

| Field | Answer |
|---|---|
| Product name | ________ |
| One-sentence description of what it does | ________ |
| Document owner (one person) | ________ |
| Team size today | Safe Default: Solo founder (1 person) -> Answer: ________ |
| Document version | Safe Default: 0.1 -> Answer: ________ |
| Date created | ________ |
| Last reviewed (date + name) | ________ |
| Review rhythm | Pick one: Weekly / Monthly / Every launch stage |

---

# 1. PRODUCT SNAPSHOT (so monitoring matches what you built)

**1.1 What type of product is it?** (tick all that apply)
- [ ] Website / web app (SaaS)
- [ ] Mobile app (iPhone)
- [ ] Mobile app (Android)
- [ ] Both web and mobile
- [ ] Has a backend or API behind it
- [ ] Uses AI (chat, generation, recommendations)
- [ ] Takes payments
- [ ] Sends emails, texts, or push notifications

**1.2 Where does it live?** (the place that runs your product)
Answer: ________ (examples: a cloud provider, a hosting service, "not sure")
Safe Default: use whatever your developer or AI agent chose, and write its name here.

**1.3 What are the 3 most important things a customer must be able to do?**
(If these break, you have a disaster. These become your **Critical Journeys**.)

| # | Critical Journey (plain words) | Example |
|---|---|---|
| 1 | ________ | "Sign up and log in" |
| 2 | ________ | "Pay for the plan" |
| 3 | ________ | "Use the main feature" |

**1.4 What third-party services does your product depend on?** (if one of them breaks, you break)

| Service | What it does for you | Do they publish a status page? (Y/N) |
|---|---|---|
| ________ | ________ | ____ |
| ________ | ________ | ____ |
| ________ | ________ | ____ |

Examples: payment provider, login provider, email sender, AI model provider, database host, app store.

---

# 2. GOALS AND PROMISES (what "good" looks like)

**2.1 Why are we monitoring?** Pick your top 3 (rank 1, 2, 3):
- [ ] Find problems before customers do
- [ ] Protect revenue
- [ ] Keep customers' data safe
- [ ] Keep the product fast
- [ ] Control spending
- [ ] Learn how customers actually use it
- [ ] Meet legal or contract promises

**2.2 How much downtime is OK?**

| Uptime promise | Allowed downtime per month |
|---|---|
| 99% | ~7 hours |
| 99.5% | ~3.5 hours |
| 99.9% | ~43 minutes |
| 99.99% | ~4 minutes |

Safe Default: **99.5% before launch, 99.9% after customer 100**.
Answer: ________ %

**2.2b Did you promise any customer or contract a number?** (a "Service Level Agreement", or SLA)
- [ ] Yes -> Promise: ________ - [ ] No - [ ] Not sure (treat as No, but ask your lawyer or advisor)

**2.3 How fast should it feel?**

| What | Good | Acceptable | Too slow (alert!) |
|---|---|---|---|
| Web page opens | under 2 sec | 2-4 sec | over 4 sec |
| Button click gets a response | under 1 sec | 1-2 sec | over 2 sec |
| Mobile app starts | under 3 sec | 3-5 sec | over 5 sec |
| Main feature finishes | ________ | ________ | ________ |

Safe Default: use the "Good / Acceptable / Too slow" numbers above.

**2.4 How many errors are OK?**
Safe Default: **fewer than 1 in 100 requests fail (under 1%)**; alert at 2% or more.
Answer: ________ %

**2.5 Crash-free mobile sessions target?**
Safe Default: **99.5% crash-free**. Answer: ________ %
- [ ] N/A (no mobile app)

---

# 3. WHAT WE WATCH (the monitoring map)

Tick every box you will watch. For each ticked row fill **Owner**, **Tool**, and **From stage** (stages are in Section 4).

> **Tool column rule:** write the *name of the tool you picked* or `TBD`. This template does not choose tools for you.

## 3.1 Is it alive? (Availability)

| Watch this | Tick | Check how often | Owner | Tool | From stage |
|---|---|---|---|---|---|
| Home page reachable | [ ] | Safe Default: every 1 min | ____ | ____ | 3 |
| Login works (robot test) | [ ] | every 5 min | ____ | ____ | 2 |
| Each Critical Journey from 1.3 (robot test) | [ ] | every 5 min | ____ | ____ | 2 |
| Backend / API health | [ ] | every 1 min | ____ | ____ | 2 |
| Database reachable | [ ] | every 1 min | ____ | ____ | 2 |
| Expiring certificate / domain (the "padlock" and web address) | [ ] | daily | ____ | ____ | 2 |
| Third-party status pages | [ ] | automatic | ____ | ____ | 3 |

## 3.2 Is it fast? (Performance)

| Watch this | Tick | Owner | Tool | From stage |
|---|---|---|---|---|
| Page load time | [ ] | ____ | ____ | 2 |
| Server response time | [ ] | ____ | ____ | 2 |
| Slow database questions | [ ] | ____ | ____ | 4 |
| Mobile app start time | [ ] | ____ | ____ | 2 |
| Mobile screen lag / freezing | [ ] | ____ | ____ | 4 |

## 3.3 Is it breaking? (Errors)

| Watch this | Tick | Owner | Tool | From stage |
|---|---|---|---|---|
| Website errors (browser side) | [ ] | ____ | ____ | 1 |
| Server errors (backend side) | [ ] | ____ | ____ | 1 |
| Mobile app crashes | [ ] | ____ | ____ | 1 |
| Failed background jobs | [ ] | ____ | ____ | 2 |
| Failed emails / texts / push messages | [ ] | ____ | ____ | 2 |
| Failed payments | [ ] | ____ | ____ | 2 |

## 3.4 Is the machine healthy? (Infrastructure)

| Watch this | Tick | Alert when | Owner | Tool |
|---|---|---|---|---|
| Processor busy (CPU) | [ ] | Safe Default: over 80% for 10 min | ____ | ____ |
| Memory used | [ ] | over 85% for 10 min | ____ | ____ |
| Disk space | [ ] | over 80% full | ____ | ____ |
| Database connections | [ ] | over 80% of limit | ____ | ____ |
| Queue of waiting jobs | [ ] | growing for 15 min | ____ | ____ |

## 3.5 Is the business healthy? (Business signals)

| Watch this | Tick | Alert when | Owner |
|---|---|---|---|
| New sign-ups per day | [ ] | drops 50% below normal | ____ |
| Successful payments per day | [ ] | drops 50% below normal, or 0 for 4 hours | ____ |
| Sign-up completion rate | [ ] | drops 20% below normal | ____ |
| Cancellations / refunds | [ ] | doubles | ____ |
| Support tickets per day | [ ] | doubles | ____ |
| App store rating and reviews (mobile) | [ ] | any 1-star review, or average drops 0.3 | ____ |

## 3.6 Is the AI behaving? (Only if you ticked "Uses AI" in 1.1)

| Watch this | Tick | Alert when | Owner | Tool |
|---|---|---|---|---|
| AI provider errors / rate limits | [ ] | over 2% of calls fail | ____ | ____ |
| AI answer speed | [ ] | slower than ____ sec | ____ | ____ |
| AI cost per customer per day | [ ] | over $ ____ | ____ | ____ |
| Bad / unsafe answers reported by customers | [ ] | any report | ____ | ____ |
| Answer quality spot-check (a human reads a sample) | [ ] | weekly | ____ | ____ |
- [ ] N/A (no AI)

## 3.7 Are people safe? (Security signals)

| Watch this | Tick | Alert when | Owner |
|---|---|---|---|
| Many failed logins in a row | [ ] | 10+ from one place in 5 min | ____ |
| Logins from strange places | [ ] | impossible travel, new country | ____ |
| Admin actions | [ ] | any admin change is logged and reviewed | ____ |
| Secret keys leaked in code | [ ] | any detection | ____ |
| Out-of-date software with known holes | [ ] | any "critical" finding | ____ |
| Unusual spike in traffic | [ ] | 5x normal | ____ |

---

# 4. THE 5 STAGES: DEVELOPMENT TO FIRST 500 CUSTOMERS

> Each stage has a **Goal**, a **Minimum Monitoring Checklist**, and a **Gate** (a yes/no test you must pass before moving on). Tick as you go.

## STAGE 1: BUILD (Development)
**Goal:** Catch mistakes while building. No customers yet.
**Dates:** Start ________ End ________

- [ ] Error tracking turned on for web and mobile (Section 3.3)
- [ ] Logs are written and readable (Section 8)
- [ ] Every AI-agent or developer change leaves a note of what changed
- [ ] Test and real environments are separate (test mistakes never touch real data)
- [ ] Secrets (passwords, keys) are NOT written in plain text in code

**Gate 1 - can we move on?**
- [ ] Yes, an error on purpose shows up in the error tool within 5 minutes
- [ ] Yes, I can read logs for the last hour
Not both ticked? **Do not move on.**

## STAGE 2: PRE-LAUNCH (Testing with friends / beta)
**Goal:** Test the watching itself, with a few trusted people.
**Dates:** Start ________ End ________
**Number of beta users:** Safe Default: 5-20. Answer: ____

- [ ] All Critical Journeys (1.3) have robot checks
- [ ] Availability checks on (Section 3.1)
- [ ] Alerts reach a real phone (test: send a fake alert, it arrived in ____ min)
- [ ] First dashboard exists (Section 6)
- [ ] First **runbook** exists for each Critical Journey (Section 9)
- [ ] Backup works AND a restore has been tested once
- [ ] Practice incident done ("fire drill"): date ________

**Gate 2 - can we launch?**
- [ ] Fake alert reached me in under 5 minutes
- [ ] I practiced one incident from start to finish
- [ ] No unresolved SEV1 or SEV2 issues
- [ ] Payment test (test money) succeeded and was seen in monitoring

## STAGE 3: LAUNCH DAY
**Goal:** Watch everything closely during the first 24-72 hours.
**Launch date/time:** ________ **Time zone:** ________

- [ ] Someone is **watching the dashboard live** for the first ____ hours (Safe Default: 4)
- [ ] Alert sensitivity raised (Safe Default: alert at half the normal limit)
- [ ] Every channel (phone/email/chat) tested again that morning
- [ ] "Rollback" plan written (how to go back to the last good version): ________
- [ ] Status page ready (a public page that tells customers "we know, we're fixing it")
- [ ] Support inbox is being watched
- [ ] Launch-day log kept (Section 11.2)

**Gate 3 - launch healthy?** (check after 72 hours)
- [ ] Uptime met target in 2.2
- [ ] Error rate under target in 2.4
- [ ] No unresolved SEV1 incidents

## STAGE 4: CUSTOMERS 1-100
**Goal:** Learn what normal looks like. Fix the first surprises fast.
**Reached customer #100 on:** ________

- [ ] Every alert has been reviewed: keep, change, or delete (too noisy = delete)
- [ ] "Normal" numbers recorded (usual sign-ups, usual speed, usual errors)
- [ ] Weekly 30-minute monitoring review is on the calendar
- [ ] Every real incident has a written review (Section 10.4)
- [ ] Cost tracking turned on (Section 12)
- [ ] Customer-reported problems are matched against what monitoring saw: *did we see it first?* Record ____ out of ____

**Gate 4 - ready to scale?**
- [ ] We found over half of problems before customers told us
- [ ] Under 5 alerts per week need no action (noise is low)
- [ ] Monthly cost within budget (Section 12)

## STAGE 5: CUSTOMERS 101-500
**Goal:** Stay reliable as traffic grows. Prepare for success.
**Reached customer #500 on:** ________

- [ ] Alerts tuned using real "normal" numbers
- [ ] Load check: product tested at 2x today's traffic
- [ ] Uptime promise upgraded if needed (2.2)
- [ ] Backup restore tested again
- [ ] Access list reviewed: only needed people have access
- [ ] Monitoring cost reviewed against revenue
- [ ] On-call plan reviewed (Section 7)
- [ ] Monthly report to stakeholders (Section 11.3)

**Gate 5 - done!**
- [ ] 500 customers reached with uptime at or above target
- [ ] Monitoring document fully up to date
- [ ] Lessons written for the next product (Section 14)

---

# 5. ALERTS (who gets told, how, and when)

**5.1 Severity levels** (use these exact words everywhere)

| Level | Plain words | Examples | Respond within | Wake someone at night? |
|---|---|---|---|---|
| **SEV1** | Disaster: product down or data at risk | Nobody can log in; payments failing; data leak | 15 min | Yes |
| **SEV2** | Major: a key feature broken for many | Main feature errors for 10%+ of users | 1 hour | Yes (Safe Default) |
| **SEV3** | Minor: small group affected, workaround exists | One screen broken on one phone model | Next working day | No |
| **SEV4** | Cosmetic / info only | Typo, slow admin page | This week | No |

**5.2 Where do alerts go?** (tick all you will use)

| Channel | Used for | Tick | Details (name / address) |
|---|---|---|---|
| Phone call or loud push | SEV1 | [ ] | ____ |
| Text message | SEV1, SEV2 | [ ] | ____ |
| Chat app message | SEV2, SEV3 | [ ] | ____ |
| Email | SEV3, SEV4 | [ ] | ____ |
Safe Default: SEV1 = call + text; SEV2 = text + chat; SEV3 = chat; SEV4 = email.

**5.3 Alert quality rules** (keep alerts useful, not annoying)
- Every alert must answer: **What broke? Who is affected? What do I do first?**
- If an alert fires and needs no action 3 times in a row, **fix or delete it**.
- Alert on **customer pain** (people can't pay), not on tiny technical noise.
- One alert per problem, not 50.
- [ ] I agree to these rules.

**5.4 Alert list** (copy one row per alert; start with your Critical Journeys)

| Alert name | Condition (plain words) | Severity | Goes to | Runbook link | Owner | Status |
|---|---|---|---|---|---|---|
| Example: Payments failing | Fewer than 1 successful payment in 4 hours during the day | SEV1 | Founder phone | Runbook R-02 | Founder | TODO |
| ________ | ________ | ____ | ________ | ____ | ____ | ____ |
| ________ | ________ | ____ | ________ | ____ | ____ | ____ |
| ________ | ________ | ____ | ________ | ____ | ____ | ____ |

---

# 6. DASHBOARDS (the screens you look at)

**6.1 Which dashboards will you have?** (Safe Default: all three)

| Dashboard | Who looks | What's on it | Tick | Link |
|---|---|---|---|---|
| **Health** (one screen) | Everyone, daily | Up/down, error rate, speed, active alerts | [ ] | ____ |
| **Business** | Founder, weekly | Sign-ups, payments, cancellations, support | [ ] | ____ |
| **Deep-dive / technical** | Developer or AI agent, during incidents | Logs, slow queries, machine health | [ ] | ____ |

**6.2 The "Glance Test":** Can a new person, in 10 seconds, say whether the product is healthy?
- [ ] Yes - [ ] No (simplify the Health dashboard)

**6.3 Rule:** Green = fine, Yellow = watch, Red = act now. Use colors AND words (some people can't tell colors apart).
- [ ] I agree.

---

# 7. PEOPLE AND ON-CALL (who does what)

**7.1 Roles** (one named person each; a solo founder can hold all roles, write the same name)

| Role | What they do | Name | Contact | Backup person |
|---|---|---|---|---|
| Monitoring Owner | Keeps this document alive | ____ | ____ | ____ |
| First Responder | Answers alerts first | ____ | ____ | ____ |
| Incident Lead | Decides what to do during a SEV1/SEV2 | ____ | ____ | ____ |
| Customer Communicator | Tells customers what's happening | ____ | ____ | ____ |
| Technical Fixer | Fixes the problem | ____ | ____ | ____ |

**7.2 When are you reachable?**
Safe Default (solo founder): phone alerts on 24/7 for SEV1 only; everything else waits until working hours.
Answer: ________

**7.3 What if nobody answers an alert in ____ minutes?** (Safe Default: 15)
Who is called next? ________

**7.4 Burnout protection**
- [ ] At least one full day per week with no alerts except SEV1
- [ ] Planned time off has a named backup
- [ ] After a night-time alert, the next morning starts later

---

# 8. LOGS (the product's diary)

**8.1 What must be logged?** (tick all)
- [ ] Every error, with what happened and when
- [ ] Every login, logout, failed login
- [ ] Every payment attempt and result (never card numbers)
- [ ] Every admin or settings change
- [ ] Every AI request and result summary (if using AI)
- [ ] Which version of the product was running

**8.2 What must NEVER be logged?**
- Passwords, card numbers, secret keys, full ID numbers
- Private messages or personal content (unless needed AND approved)
- [ ] I confirm no sensitive data is written to logs.

**8.3 How long do we keep logs?** Safe Default: 30 days searchable, 12 months archived (or what the law requires).
Answer: ________

**8.4 Who can read logs?** Names: ________ (fewest people possible)

---

# 9. RUNBOOKS (what to do when something breaks)

> One runbook per Critical Journey and per big alert. Keep each **under one page**. Write as if the reader is half-asleep.

**9.1 Runbook index**

| ID | Problem | Linked alert | Owner | Last tested |
|---|---|---|---|---|
| R-01 | Product is completely down | ____ | ____ | ____ |
| R-02 | Payments failing | ____ | ____ | ____ |
| R-03 | Nobody can log in | ____ | ____ | ____ |
| R-04 | Product is very slow | ____ | ____ | ____ |
| R-05 | A bad release went out (rollback) | ____ | ____ | ____ |
| R-06 | Suspected security problem | ____ | ____ | ____ |
| R-07 | Third-party service is down | ____ | ____ | ____ |
| R-08 | AI model is failing or behaving badly (if AI) | ____ | ____ | ____ |
| R-09 | Mobile app crashing after release | ____ | ____ | ____ |

**9.2 Runbook template** (copy for each one)

```
RUNBOOK ID & NAME: ________
WHEN TO USE: (which alert or symptom)
HOW BAD IS IT? Severity: ____
STEP 1 - CHECK: (what to look at first, with link)
STEP 2 - QUICK FIX: (safest action that stops the pain)
STEP 3 - IF THAT FAILED: (next action)
STEP 4 - ROLL BACK: (how to return to last good version)
WHO TO CALL: ________
WHAT TO TELL CUSTOMERS: (copy-paste message)
HOW I KNOW IT'S FIXED: (what the dashboard should show)
AFTER: write the incident review (Section 10.4)
```

---

# 10. INCIDENT RESPONSE (when it really breaks)

**10.1 The 6 steps (same every time)**
1. **Notice** - alert fires or customer reports
2. **Decide severity** (5.1)
3. **Tell people** - team first, then customers
4. **Fix or roll back** - safest fast action, not the perfect fix
5. **Confirm fixed** - dashboard returns to green
6. **Learn** - write the review within 3 working days

**10.2 Customer messages** (pre-write them; edit the blanks)

| Moment | Message |
|---|---|
| We know there's a problem | "We're aware of an issue with ________ and are working on it. Next update by ____." |
| Update | "Update: ________. Next update by ____." |
| Fixed | "The issue with ________ is fixed as of ____. We're sorry. What happened: ________." |

Where will these be posted? (status page / email / in-app / social) Answer: ________
**Rule:** update customers at least every **30 minutes** for SEV1 and **2 hours** for SEV2.

**10.3 Incident log** (one row per incident)

| Date | Severity | What broke | Found by (monitoring / customer) | Minutes to notice | Minutes to fix | Review link |
|---|---|---|---|---|---|---|
| ____ | ____ | ____ | ____ | ____ | ____ | ____ |

**10.4 Incident review template** (no blame; about the system, not the person)
- What happened? ________
- What was the customer impact (how many, how long)? ________
- How did we find out? ________
- Why did it happen? (ask "why?" five times) ________
- What worked well? ________
- What will we change? (each with an **owner** and **due date**) ________
- Did a monitor or alert need to be added or fixed? [ ] Yes -> added in Section 5.4 on ________

---

# 11. REPORTING AND REVIEW RHYTHM

**11.1 Rhythm** (Safe Default shown)

| When | What | Who | Time |
|---|---|---|---|
| Every day | Look at the Health dashboard | ____ | 2 min |
| Every week | Review alerts, incidents, noise | ____ | 30 min |
| Every month | Uptime, speed, errors, cost report | ____ | 1 hour |
| Every launch stage | Gate check (Section 4) | ____ | 1 hour |
| Every 6 months | Review whole document | ____ | 2 hours |

**11.2 Launch-day log** (Stage 3)

| Time | What I saw | What I did |
|---|---|---|
| ____ | ____ | ____ |

**11.3 Monthly report: fill these numbers**

| Number | This month | Target | OK? |
|---|---|---|---|
| Uptime % | ____ | from 2.2 | [ ] |
| Error rate % | ____ | from 2.4 | [ ] |
| Average speed (sec) | ____ | from 2.3 | [ ] |
| Incidents (SEV1/2/3) | ____ | 0 SEV1 | [ ] |
| Alerts that needed no action | ____ | under 5/week | [ ] |
| Problems found by us before customers | ____ % | over 70% | [ ] |
| Customers total | ____ | toward 500 | [ ] |
| Monitoring cost | $ ____ | from Section 12 | [ ] |

---

# 12. COST AND BUDGET MONITORING

**12.1 Monthly budget**

| Item | Budget $ | Alert at (80% of budget) |
|---|---|---|
| Hosting / cloud | ____ | ____ |
| Monitoring tools | ____ | ____ |
| AI model usage (if any) | ____ | ____ |
| Messaging (email, text, push) | ____ | ____ |
| Other third-party services | ____ | ____ |
| **Total** | ____ | ____ |

Safe Default: total monitoring + hosting should be **under 15% of monthly revenue** once you have paying customers.

**12.2 Cost alerts** (tick)
- [ ] Alert when daily spend is 2x normal
- [ ] Alert when monthly spend reaches 80% of budget
- [ ] Hard spending limit set where the service allows (with whom?: ____)
- [ ] Monthly review of unused services to cancel

**12.3 Cost per customer** (check at 100, 250 and 500 customers)

| Customers | Total monthly cost | Cost per customer |
|---|---|---|
| 100 | ____ | ____ |
| 250 | ____ | ____ |
| 500 | ____ | ____ |

---

# 13. PRIVACY, SECURITY AND COMPLIANCE

**13.1 What personal data does the product handle?** (tick all)
- [ ] Names / emails - [ ] Phone numbers - [ ] Payment info - [ ] Location - [ ] Photos / files - [ ] Health info - [ ] Children's data - [ ] Other: ____

**13.2 Which rules apply to you?** (tick all; "not sure" is fine, then ask an advisor)

| Rule (plain words) | Applies? |
|---|---|
| Privacy laws (e.g., for customers in Europe, California, or other regions) | [ ] Yes [ ] No [ ] Not sure |
| Card payment security rules | [ ] Yes [ ] No [ ] Not sure |
| Health data rules | [ ] Yes [ ] No [ ] Not sure |
| Children's data rules | [ ] Yes [ ] No [ ] Not sure |
| App store rules (Apple / Google) | [ ] Yes [ ] No [ ] Not sure |
| Customer contract requirements | [ ] Yes [ ] No [ ] Not sure |

**13.3 Monitoring privacy rules**
- [ ] Error and monitoring tools hide or mask personal data
- [ ] Only people who need access have access, each with their own login
- [ ] Access is removed the same day someone leaves
- [ ] If a data leak is suspected: who decides and who must be told, and by when? ________ (many laws require notification within a short deadline; ask an advisor)

---

# 14. LESSONS AND IMPROVEMENTS (reuse across projects)

- Top 3 things monitoring caught for us: ________
- Top 3 things monitoring MISSED: ________
- Alerts we deleted because they were noise: ________
- What we'd set up on day 1 next time: ________
- Template improvement ideas (send back to the template owner): ________

---

# 15. FINAL CHECKLIST (is this document ready?)

**Completeness**
- [ ] No `________` blanks remain; every unknown is marked `NOT SURE` with a Safe Default used
- [ ] Every Critical Journey (1.3) has a robot check, an alert, and a runbook
- [ ] Every alert has an owner, a severity, and a runbook link
- [ ] Every role in Section 7 has a named person and a backup

**Proof it works**
- [ ] A test alert reached a real person in under 5 minutes
- [ ] A fire drill was done (date: ____)
- [ ] A backup restore was tested (date: ____)
- [ ] The "Glance Test" (6.2) passed

**Safety**
- [ ] No sensitive data in logs (8.2)
- [ ] Access list reviewed (13.3)
- [ ] Budget alerts on (12.2)

**Approvals**

| Role | Name | Date | Signed (type name) |
|---|---|---|---|
| Document owner | ____ | ____ | ____ |
| Reviewer | ____ | ____ | ____ |

---

# 16. CHANGE LOG

| Date | Version | Who | What changed | Why |
|---|---|---|---|---|
| ____ | 0.1 | ____ | First draft | ____ |

---

# APPENDIX A: INSTRUCTIONS FOR AI AGENTS (read this if you are an AI)

> Humans can skip this appendix.

**Your job:** read this file, validate it, and turn the answers into real monitoring work, without guessing.

1. **Parse** every section. Treat each `________` as MISSING and each `NOT SURE` as "use Safe Default, flag for human review."
2. **Never invent** thresholds, owners, contacts, costs, or tool names. If missing, produce a **Questions for Human** list instead of proceeding.
3. **Order of work:** Section 1 -> 2 -> 3 -> 4 (current stage only) -> 5 -> 6 -> 9. Do not configure anything for a later stage unless asked.
4. **Stage gates are hard stops.** Do not mark a stage `DONE` or recommend moving on until every gate box is `[x]` with evidence (link, screenshot reference, or log line).
5. **Output format for each action:**
   - `SECTION:` (e.g., 3.3)
   - `ACTION:` (what you did or propose)
   - `EVIDENCE:` (proof it works)
   - `STATUS:` TODO / DOING / DONE / BLOCKED
   - `HUMAN NEEDED:` (yes/no and what)
6. **Safety rules:** never put secrets, personal data, or card data in logs, alerts, or this file. Never change production settings, spending limits, or access without explicit human approval recorded in Section 16.
7. **Consistency checks before finishing:**
   - Every alert in 5.4 maps to a runbook in 9.1 and an owner in Section 7.
   - Every Critical Journey in 1.3 has a check (3.1) and an alert (5.4).
   - Severity words match Section 5.1 exactly.
   - Targets in Section 11.3 match Section 2.
8. **Update the Change Log (Section 16)** after every edit, and append to the Incident Log (10.3) after every incident.

---

# APPENDIX B: SAFE-DEFAULTS CHEAT SHEET (one-glance summary)

| Topic | Safe Default |
|---|---|
| Uptime target | 99.5% pre-launch, 99.9% after customer 100 |
| Error rate alert | 2% |
| Page load | under 2 sec good, alert over 4 sec |
| Crash-free mobile | 99.5% |
| CPU / memory / disk alert | 80% / 85% / 80% |
| Availability check frequency | Every 1 min (home, API), 5 min (robot journeys) |
| SEV1 response | 15 min, wake someone |
| Customer updates | SEV1 every 30 min, SEV2 every 2 hours |
| Log retention | 30 days searchable, 12 months archived |
| Weekly review | 30 minutes |
| Incident review | within 3 working days |
| Monitoring + hosting cost | under 15% of revenue |
| Launch-day live watching | first 4 hours, alerts at half normal limits |
