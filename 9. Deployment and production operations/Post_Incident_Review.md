# How to fill in this document

**What this is:** A Post Incident Review (PIR) is a short report you write after something went wrong in production (the live product your customers use). It answers four questions: *What happened? Why? How do we fix it? How do we stop it happening again?*

**Who it is for:** Anyone. A solo founder, a small team, or an AI agent helping you. You do not need technical knowledge to start. Write in plain words, like you are explaining it to a friend.

**Where it lives:** `Deployment and production operations/Post_Incident_Review.md`. This file is the **master template**. Make **one copy per incident** and rename it `PIR_YYYY-MM-DD_short-name.md` (example: `PIR_2026-10-18_checkout-down.md`).

**What it covers:** The whole life of an AI-driven product, from the first build, through testing and launch day, up to and beyond your first **500 customers**.

## The 12 rules (read these first)

1. **Copy this file first.** Never fill in the master template.
2. **Answer every question.** Each question has a `YOUR ANSWER:` line or a table cell. Type there.
3. **Read the `Example:` lines.** They show what a good answer looks like. Delete the examples in your copy if you like, but never copy them as your answer.
4. **Do not guess.** If you do not know, write `UNKNOWN`, and add a task in section 13 (Action Items) to find out.
5. **Not applicable?** Write `N/A` and one short reason. Never leave a blank.
6. **No blame.** Write about *systems and steps*, never about *people*. Say "the deploy check was missing", not "Sam forgot".
7. **Use real facts.** Numbers, times, links, and screenshots beat opinions. Write times with the time zone (example: `14:05 UTC`).
8. **Tick boxes like this:** `[x]` = yes, `[ ]` = no or not done.
9. **Items marked ⭐ are required** for every incident, even tiny ones. Everything else is required for SEV1 and SEV2, and optional for SEV3 and SEV4.
10. **Time limits:** Start this document within **24 hours** of the incident ending. Finish it within **5 working days**.
11. **Never paste secrets.** No passwords, API keys, tokens, or customers' personal data. Write `[REDACTED]` instead.
12. **Stuck?** Write what you *do* know in plain words, then write `UNKNOWN` for the rest. A true, incomplete answer is better than a neat, wrong one.

## Which path should I take?

| Your severity (see section 2) | What to fill in |
|---|---|
| **SEV1 or SEV2** | Everything, sections 1 to 16. Also send customers a message (section 17) and fill in the cost calculator (section 18). |
| **SEV3 or SEV4 (quick path)** | Only the ⭐ items plus sections 1, 2, 3, 8, 13 and 16. In every skipped section write `Skipped: SEV3` or `Skipped: SEV4`. Do not delete sections. |

## How to use AI agents with this document

You may ask an AI agent to help. Give it your logs, chat history, and this file, then tell it:

> "Fill in only facts you can prove from the evidence I gave you. Write UNKNOWN for everything else. Do not invent times, numbers, or causes. Do not name individual people as the cause. Show me the evidence for every time in the timeline."

A human must read and approve every answer before section 16 is signed. An AI agent must **never** mark the review Final on its own.

## Before you start: 5-minute gather list

Collect these first, so you do not have to guess later. Tick each when found, or write where it should be.

- [ ] Alert messages or screenshots of the problem
- [ ] Chat messages from during the incident (team chat, support inbox, social posts)
- [ ] Logs or error messages from around the time (remove secrets)
- [ ] The release, merge, or settings change that came just before the problem
- [ ] Dashboard graphs for the time window (traffic, errors, response times, AI cost)
- [ ] Customer complaints or support tickets
- [ ] Status page of any outside service you rely on (hosting, payments, email, AI model provider)

---

# Post Incident Review

## 1. Quick facts ⭐

| Field | YOUR ANSWER |
|---|---|
| Incident title (5-10 plain words). *Example: Checkout failed for new customers* | |
| Incident ID. *Example: INC-0007* | |
| Product / project name | |
| Environment (Production / Staging / Other) | |
| Date and time the incident started (with time zone) | |
| Date and time the incident ended (with time zone) | |
| Total duration (hours and minutes) | |
| Author of this review | |
| Date this review was started | |
| Review status (Draft / In review / Final) | |
| Links to evidence folder, chat, tickets, dashboards | |

## 2. Severity ⭐

**Pick the highest level that is true. When unsure, pick the more serious one.**

| Level | Plain-English meaning | Example |
|---|---|---|
| **SEV1** | Product is down or unusable for most customers, **or** data was lost, leaked, or corrupted, **or** customers were wrongly charged. | Nobody can log in. |
| **SEV2** | A main feature is broken or very slow for many customers, and there is no easy workaround. | Checkout fails for 1 in 5 customers. |
| **SEV3** | A feature is broken for some customers, but a workaround exists. | PDF export fails, but copy-paste works. |
| **SEV4** | Small problem. Customers barely notice, or only you noticed. | A typo on the pricing page. |

**Which level was it?** (tick one)
- [ ] SEV1 · [ ] SEV2 · [ ] SEV3 · [ ] SEV4

**Why did you pick it? (one sentence)** *Example: "Checkout failed for about 20% of customers and there was no other way to pay."*
YOUR ANSWER:

**Did the level change during the incident?** *Example: "Started SEV3 at 14:05 UTC, became SEV1 at 15:10 UTC when we found data was affected."*
YOUR ANSWER:

## 3. Summary ⭐

Write this **last**, but keep it at the top. Use **3 to 5 sentences** and **no jargon**.

**Fill in this pattern:**
> On **[date]**, **[what customers experienced]** for **[how long]**. It affected **[how many customers or what share]**. The cause was **[one-line cause]**. We fixed it by **[one-line fix]**. We are preventing it from happening again by **[one-line prevention]**.

*Example: "On 18 October 2026, new customers could not pay for 47 minutes. It affected about 30 of our 410 customers. The cause was a new payment setting that was wrong in production. We fixed it by going back to the old setting. We are preventing it again by adding a test that checks the payment page before every release."*

YOUR ANSWER:

## 4. Where in the product's life did this happen? ⭐

**Which stage was the product in?** (tick one)
- [ ] Building (not yet released)
- [ ] Testing / staging (internal only)
- [ ] Launch day or launch week
- [ ] Live with **1-50** customers
- [ ] Live with **51-200** customers
- [ ] Live with **201-500** customers
- [ ] Beyond 500 customers

**How many customers existed at the time of the incident?**
YOUR ANSWER:

**Which part of the work broke?** (tick all that apply)
- [ ] Idea / requirements · [ ] Design · [ ] Coding by a human · [ ] Coding by AI
- [ ] Code review · [ ] Automated tests · [ ] Manual testing · [ ] Build / packaging
- [ ] Deployment / release · [ ] Settings / secrets · [ ] Database / data
- [ ] Hosting / infrastructure · [ ] Outside service (payments, email, AI model, etc.)
- [ ] Monitoring / alerts · [ ] Customer support · [ ] Documentation · [ ] Other: ______

**Where *should* this have been caught?** (tick the earliest stage that could have caught it)
- [ ] When writing the requirements · [ ] During code review · [ ] By an automated test
- [ ] In staging · [ ] During release checks · [ ] By an alert right after release · [ ] It could not have been caught earlier

## 5. Impact ⭐

Answer with numbers. If you only have estimates, write `ESTIMATE:` before the number.

| Question | YOUR ANSWER |
|---|---|
| How many customers were affected? *Example: 30* | |
| What share of all customers is that (%)? *Example: 7%* | |
| What exactly could customers NOT do? *Example: Could not click "Pay now"; page showed an error.* | |
| Did customers lose, or see, wrong data? (Yes / No / Unknown) | |
| Was any personal or private data exposed? (Yes / No / Unknown) | |
| Were customers charged wrongly, or not charged when they should have been? | |
| Money lost or refunded (amount and currency) | |
| Extra costs (cloud, AI usage, overtime, vendors) | |
| Support tickets and complaints received (count) | |
| Customers who cancelled or threatened to cancel (count) | |
| Reviews, social posts, or press about it (links) | |
| Did we break a promise (SLA, contract, public statement)? | |

## 6. Timeline ⭐

List **every important moment**, oldest first. For each, say what was **seen**, **decided**, or **done**. One line per event. Add rows as needed.

**Required milestones. Fill in each:**

| Milestone | Time (with time zone) | Evidence link |
|---|---|---|
| The cause was introduced (code merged, setting changed, etc.) | | |
| The change reached production | | |
| Customers first affected | | |
| We first noticed (alert, customer message, or person) | | |
| Someone started working on it | | |
| Cause understood | | |
| Fix or workaround applied | | |
| Customers no longer affected | | |
| Incident declared over | | |

**Full timeline:**

| Time | What happened | Who or what did it (use a role or tool, not blame) | Evidence link |
|---|---|---|---|
| *14:02 UTC* | *Release 1.8.3 went live* | *Automatic deploy tool* | *link* |
| *14:05 UTC* | *Payment errors began* | *Payment service* | *link* |
| | | | |
| | | | |
| | | | |

**Key time gaps (work these out from the milestones above):**
- Cause introduced → customers affected: ______
- Customers affected → we noticed (**time to detect**): ______
- We noticed → someone started working on it (**time to respond**): ______
- Started working → customers recovered (**time to fix**): ______
- Total time customers were affected: ______

## 7. Detection: How did we find out? ⭐

**Who or what noticed first?** (tick one)
- [ ] Automatic alert · [ ] Dashboard check · [ ] A customer told us · [ ] A teammate noticed
- [ ] An AI agent noticed · [ ] An outside company told us · [ ] Other: ______

**Could we have noticed sooner? What would have caught it?** *Example: "An alert when failed payments go above 5 in 10 minutes."*
YOUR ANSWER:

**Did an alert fire?** (Yes / No / It fired but was ignored). If it fired but was ignored, why?
YOUR ANSWER:

**If no alert existed, write the alert we need** (what to watch, and the number that should trigger it):
YOUR ANSWER:

## 8. Cause: Why did it happen? ⭐

### 8a. Direct cause (the thing that broke)
**In one or two sentences, what technically broke?** *Example: "The payment page pointed to the test payment account instead of the real one."*
YOUR ANSWER:

### 8b. The "5 Whys" (keep asking "why?")

Start from the direct cause. Keep going until your answer is something you can fix with a rule, a check, or a tool. You may stop before 5 if you reach that point, and write `Stopped here: root cause` on that row.

| # | Question | YOUR ANSWER |
|---|---|---|
| 1 | Why did customers have the problem? *Ex: The real payment account was not used.* | |
| 2 | Why was that? *Ex: A setting still had the test value.* | |
| 3 | Why was that? *Ex: The setting is changed by hand at release.* | |
| 4 | Why was that? *Ex: There is no checklist for release settings.* | |
| 5 | Why was that? **(Root cause)** *Ex: We have no automatic check that release settings are correct.* | |

### 8c. Root cause category (tick one main, add any extras)
- [ ] Code bug · [ ] Wrong setting · [ ] Bad release step · [ ] Missing test
- [ ] Weak or missing code review · [ ] Database change or migration · [ ] Capacity (too much traffic or data)
- [ ] Outside service outage or change · [ ] Expired certificate, key, or domain · [ ] Security issue
- [ ] Unclear requirements · [ ] Missing monitoring · [ ] Missing guide or runbook · [ ] Manual step went wrong
- [ ] AI-related (also fill in section 9) · [ ] Unknown (say what you still need to learn)

### 8d. Contributing factors (things that made it worse, or let it slip through)
*Example: "We released on a Friday evening, when fewer people were watching."*
YOUR ANSWER:

### 8e. Has this happened before?
**Yes / No.** If yes, link the old review and explain why the old fix did not work:
YOUR ANSWER:

### 8f. Proof check
**What evidence shows that the root cause is true?** (log lines, graphs, a test that reproduces it)
*A cause with no evidence must be written as `SUSPECTED:` not as a fact.*
YOUR ANSWER:

## 9. AI-related questions

If AI played no part in the cause, detection, or fix, tick this and move on:
- [ ] **No AI was involved in the cause, detection, or fix.**

### 9a. AI-written code or settings
| Question | YOUR ANSWER |
|---|---|
| Was the faulty code or setting written wholly or partly by an AI agent? (Yes / No / Unknown) | |
| Which AI tool or model wrote it? (name and version if known) | |
| What task or prompt was the AI given? (paste a short version) | |
| Did a human read and understand the change before release? (Yes / No) | |
| Was it covered by automated tests? (Yes / No / Partly) | |
| Were the AI's instructions unclear, missing, or in conflict? | |
| Did the AI change files it was not asked to change? | |
| Did the AI "invent" something that does not exist (a function, package, setting)? | |
| Did the AI say "done" when the work was not actually finished or tested? | |

### 9b. AI features inside your product (chatbots, summaries, recommendations, etc.)
| Question | YOUR ANSWER |
|---|---|
| Did the AI give wrong, made-up, harmful, or off-brand answers? Give an example (remove private data). | |
| Did a change to the prompt or settings cause it? (link the change) | |
| Did the AI provider change or retire a model version? | |
| Did the AI provider have an outage or slowdown? (link their status page) | |
| Was there a safety check on AI answers before customers saw them? | |
| How many customers saw bad AI output? | |
| Did we keep a record of the AI's answers so we can check them later? | |

### 9c. AI cost and limits
| Question | YOUR ANSWER |
|---|---|
| Did AI spending spike? From what to what, per day? *Example: $12/day to $340/day.* | |
| Did we hit a rate limit or quota? | |
| Did an AI agent get stuck in a loop or repeat the same action? | |
| Is there a spending cap or a budget alert? (Yes / No) If no, add it to section 13. | |

### 9d. AI-agent workflow lessons
| Question | YOUR ANSWER |
|---|---|
| Which agent step, tool, or permission should change? | |
| Should a human approve before this kind of change goes live? Where in the process? | |
| Should an agent be **blocked** from doing something (example: releasing to production alone)? | |
| What sentence should be added to the agent's rules file so this never repeats? Write the exact sentence. *Example: "Never change payment settings without asking a human to confirm."* | |

## 10. Response: How did we handle it?

| Question | YOUR ANSWER |
|---|---|
| Who led the response? (a role or name; solo founders write "me") | |
| Did we have a runbook or checklist for this kind of problem? (Yes / No / It was out of date) | |
| What was the first thing we tried? Did it work? | |
| What stopped the customer pain (the **mitigation**)? *Examples: rollback, turn off a feature, restart, add capacity.* | |
| What permanently fixed it (the **resolution**)? | |
| Could we roll back? How long did it take? If we could not, why? | |
| Did we need help from outside (vendor, friend, community)? | |
| Which steps were slow, confusing, or risky? | |
| Did we make any change in a hurry that needs to be checked again? | |

## 11. What went well, what went badly, where we got lucky

**What went well?** (list at least 2)
YOUR ANSWER:

**What went badly or was confusing?** (list at least 2)
YOUR ANSWER:

**Where did we get lucky?** (things that could have made it worse, but did not, by chance)
YOUR ANSWER:

## 12. Communication

| Question | YOUR ANSWER |
|---|---|
| Did we tell customers? (Yes / No). If yes, when and how (status page, email, in-app message)? | |
| Paste the message we sent (remove private data): | |
| How long after the start did we first tell customers? | |
| Did we need to tell anyone else (investors, partners, payment provider, regulators)? | |
| Did we follow up after the fix with an explanation, apology, or credit? | |
| Does a legal or privacy rule require a notice (example: a data leak)? If you are unsure, write `ASK A LAWYER`. | |

## 13. Action items ⭐ (the most important section)

**Rules for good action items:**
- **Specific:** "Add an alert when payment failures exceed 5 in 10 minutes", never "Improve monitoring".
- **One owner** (a name, or "me") and a **due date**.
- **Types:** **Prevent** (stop it happening) · **Detect** (notice sooner) · **Mitigate** (reduce the damage) · **Process** (change how we work) · **Learn** (find out something unknown).
- **Priority:** P1 = within 1 week · P2 = within 1 month · P3 = within 3 months.
- **Status:** Not started / In progress / Done / Dropped (write why).

| # | Action (specific) | Type | Priority | Owner | Due date | Ticket link | Status |
|---|---|---|---|---|---|---|---|
| 1 | | | | | | | Not started |
| 2 | | | | | | | Not started |
| 3 | | | | | | | Not started |
| 4 | | | | | | | Not started |

**Did you cover all of these? (tick each, or write why not)**
- [ ] A fix so this exact problem cannot happen again
- [ ] A test that would have caught it
- [ ] An alert or check that would have noticed it sooner
- [ ] An update to the runbook or checklist
- [ ] A change to how we review or release code
- [ ] A change to AI-agent rules or permissions (if AI was involved)
- [ ] A task to find out every `UNKNOWN` in this document

## 14. Lessons for the next launch stage

**What will we do differently before reaching the next customer milestone (50 → 200 → 500)?**
YOUR ANSWER:

**Check what is now in place:**
- [ ] Every release can be rolled back in under 15 minutes
- [ ] Backups exist, and we have tested restoring one
- [ ] Alerts exist for: site down, error rate, slow responses, failed payments, AI errors, AI cost
- [ ] A status page or customer message plan exists
- [ ] Secrets and keys are stored safely, with an expiry reminder
- [ ] Changes to production need a second check (a person, a test run, or both)
- [ ] Runbooks exist for our top 5 failure types
- [ ] Customer support knows where and how to report an incident
- [ ] Each outside service has a "what if it goes down" note
- [ ] AI agents cannot release to production without a human approval

## 15. Security and data check

| Question | YOUR ANSWER |
|---|---|
| Could someone who should not have access have seen or changed data? (Yes / No / Unknown) | |
| Were any keys, passwords, or tokens exposed? If yes, were they replaced? | |
| Is there a legal or contract duty to report? Write `N/A` or `ASK A LAWYER`. | |
| Was customer data repaired or restored? How did we confirm it is correct? | |

## 16. Follow-up and closing ⭐

**Check the fix worked (come back after 1 week and after 1 month):**
- [ ] 1-week check done on ______ · Result: ______
- [ ] 1-month check done on ______ · Result: ______

**Closing checklist (all must be ticked before status becomes Final):**
- [ ] Every ⭐ question is answered, with no blank lines
- [ ] Every `UNKNOWN` has an action item in section 13
- [ ] No blame language, and no individual named as the cause
- [ ] No secrets or customer private data in this file
- [ ] A human has read it. (Solo founders: read it again after a break, or ask a friend)
- [ ] All P1 action items are done, or scheduled with a date
- [ ] The review is saved in the incident archive and added to the log in section 19

**Approved by (name) and date:**
YOUR ANSWER:

---

## 17. Customer message templates (copy, fill in the [brackets], send)

Keep messages short, honest, and free of jargon. Say what happened, what you are doing, and when you will update next. Never blame a person or a supplier by name unless it is public. Never promise what you cannot guarantee.

### A. "We're looking into it" (send within 30 minutes of confirming SEV1 or SEV2)
> **Subject: We're aware of a problem with [feature]**
> Hi [name or "there"], some customers cannot [what they cannot do] right now. We know about it and we are working on it. Your [data / money / account] is [safe / being checked]. We will update you by [time, with time zone].

### B. "Update" (send every 30-60 minutes, or at the time you promised)
> **Subject: Update on [feature] problem**
> Here is where we are: [one sentence of progress]. Next update by [time].

### C. "Fixed" (send when customers are no longer affected)
> **Subject: [Feature] is working again**
> Good news: [feature] is working again as of [time]. It was down for about [duration]. The cause was [one plain sentence]. We are sorry for the trouble. If anything still looks wrong, reply to this message and we will help right away.

### D. "Apology and follow-up" (send within 5 working days for SEV1 and SEV2)
> **Subject: What happened on [date], and what we are changing**
> On [date], [what customers experienced] for [duration]. This was our mistake. We have [fixed it / changed X]. To prevent it happening again we are [one or two specific actions]. [If it applies: As a thank-you for your patience we have added [credit or refund] to your account.] You can contact us any time at [contact].

### E. "Data problem" (only for lost, wrong, or exposed data. Ask a lawyer before sending)
> **Subject: Important: an issue that affected some of your data**
> We found that [plain description of what happened] between [start] and [end]. The information involved was [what kind of data]. We have [what you did to stop it]. You should [what the customer should do, if anything]. For questions contact [contact].

**Which templates did we send, and when?**
YOUR ANSWER:

## 18. Cost-of-incident calculator

Fill in the numbers, then add up. Use `0` if nothing applies. This helps you decide how much prevention work is worth doing.

| Cost line | How to work it out | Your number |
|---|---|---|
| **Lost sales** | Average sales per hour × hours customers could not buy | |
| **Refunds and credits** | Total value given back to customers | |
| **Support time** | Hours spent answering customers × your hourly cost | |
| **Fix time** | Hours spent fixing × your hourly cost (include AI agent time if billed) | |
| **Extra AI and cloud spend** | Spend during the incident − normal spend | |
| **Outside help** | Fees paid to vendors or freelancers | |
| **Lost customers** | Customers who cancelled × their average yearly value | |
| **Other** | Fines, legal advice, etc. | |
| **TOTAL** | Add all rows | |

**What is the cheapest action in section 13 that would have prevented most of this cost?**
YOUR ANSWER:

## 19. Incident log index (one row per review, kept in the master copy of your project folder)

Add a row each time a review is finished. This lets you spot patterns across 100s of projects.

| Incident ID | Date | Project | Severity | Root cause category | Duration | Customers affected | Total cost | Link to PIR | Actions done / total |
|---|---|---|---|---|---|---|---|---|---|
| *INC-0007* | *2026-10-18* | *Example App* | *SEV2* | *Wrong setting* | *47 min* | *30* | *$850* | *PIR_2026-10-18_checkout-down.md* | *3 / 4* |
| | | | | | | | | | |
| | | | | | | | | | |

**Every quarter, look at the log and answer:**
- Which root cause category appears most?
- Which life-cycle stage (section 4) catches the least?
- Are we noticing problems faster or slower than before?
- Which action items keep getting dropped?

## 20. Worked example (a finished review, to copy the style)

> This is a **made-up** incident to show what finished answers look like. Do not copy these facts.

**Title:** Checkout failed for new customers · **ID:** INC-0007 · **Severity:** SEV2 · **Stage:** Live with 201-500 customers (410 customers)

**Summary:** On 18 October 2026, new customers could not pay for 47 minutes. It affected about 30 of our 410 customers. The cause was a payment setting that still used the test account after release. We fixed it by going back to the previous version. We are preventing it again by adding an automatic check of release settings.

**Timeline highlights (UTC):** 14:02 release went live · 14:05 payment errors began · 14:23 first customer email arrived (we noticed) · 14:30 started working · 14:41 found the test setting · 14:49 rolled back · 14:52 payments working · 15:00 incident declared over.

**Time gaps:** time to detect 18 min · time to respond 7 min · time to fix 22 min · total 47 min.

**Impact:** 30 customers affected (7%). Could not pay. No data lost or exposed. 12 support emails. 2 customers asked for refunds. Estimated lost sales $620.

**Detection:** A customer told us. No alert existed. *Needed alert: failed payments above 5 in 10 minutes.*

**Direct cause:** The payment page pointed to the test payment account.

**5 Whys:**
1. Customers could not pay → real payment account was not used.
2. Why → a setting still had the test value.
3. Why → the setting is edited by hand at release time.
4. Why → no checklist exists for release settings.
5. **Root cause →** no automatic check that release settings match production.

**AI involvement:** Yes. The release notes and settings file were drafted by an AI agent. A human skimmed them but did not check the payment setting. The agent's rules file did not mention payments. *Rule added: "Never change payment settings without a human confirming the value."*

**What went well:** Rollback took only 3 minutes. The customer message went out within 40 minutes.
**What went badly:** We found out from a customer, not an alert. The runbook did not cover payments.
**Where we got lucky:** It happened in the afternoon when I was at my desk.

**Action items:**

| # | Action | Type | Priority | Owner | Due | Status |
|---|---|---|---|---|---|---|
| 1 | Add automatic check that fails the release if payment mode is "test" | Prevent | P1 | Me | 25 Oct 2026 | Done |
| 2 | Add alert: failed payments above 5 in 10 minutes | Detect | P1 | Me | 25 Oct 2026 | Done |
| 3 | Add "payments" runbook with rollback steps | Process | P2 | Me | 18 Nov 2026 | In progress |
| 4 | Add the payment rule to the AI agent's rules file | Prevent | P1 | Me | 20 Oct 2026 | Done |

**Total estimated cost:** $850 (lost sales $620, refunds $90, support and fix time $140).

---

## Glossary (plain words)

| Word | Meaning |
|---|---|
| **Incident** | Something unplanned that hurt, or could hurt, customers. |
| **Production** | The live product real customers use. |
| **Staging** | A practice copy of the product used for testing before release. |
| **Deploy / release** | Putting new code or settings into production. |
| **Rollback** | Going back to the previous working version. |
| **Mitigation** | A quick step that stops the pain, even if the real problem is not fixed yet. |
| **Resolution** | The proper fix. |
| **Root cause** | The deepest reason it happened that we can actually fix. |
| **Runbook** | A step-by-step "what to do when X breaks" guide. |
| **Alert** | An automatic message that says something is wrong. |
| **SLA** | A promise to customers about uptime or response time. |
| **Prompt** | The instructions given to an AI model or agent. |
| **Hallucination** | When an AI states something false as if it were true. |
| **Rate limit / quota** | A cap on how much an outside service lets you use. |
| **Status page** | A public web page where you tell customers if something is wrong. |
| **Blameless** | Looking for what in the system failed, not who failed. |

## Change history of this template

| Version | Date | Change | Author |
|---|---|---|---|
| 0.1 | 2026-10-18 | First draft | |
| 0.2 | 2026-10-18 | Added examples to every question, customer message templates, cost calculator, incident log index, worked example | |
