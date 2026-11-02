# How to fill in this document

> **Read this box first. It takes 3 minutes and saves hours.**

## What is this document?

This document is your **safety plan for launching**. It answers two simple questions:

1. **"How do we turn a new feature on slowly and safely?"** (that is *Feature Flags*)
2. **"If something goes wrong, how do we go back to the safe version fast?"** (that is *Rollback*)

You will fill it in **once per project**, **before** you launch. You will use it again if something breaks. It covers the whole journey: from the first line of code until your **first 500 customers** are happily using the product.

## The 7 rules of filling it in

| # | Rule | Why |
|---|------|-----|
| 1 | **Go in order.** Start at Part 0 and finish at Part 17. | Later parts depend on earlier answers. |
| 2 | **Answer every question.** Write your answer on the line that starts with `Answer:`. | Empty answers are guesses waiting to happen. |
| 3 | **Don't know? Write `UNKNOWN - [name] will find out by [date]`.** Never leave a blank. | A named owner and date turns a gap into a task. |
| 4 | **Not relevant? Write `N/A - because [reason]`.** (Example: `N/A - because we have no mobile app`.) | Proves you thought about it. |
| 5 | **Use real names, real numbers, real links.** Not "soon", "some", "the team", or "high". | Anyone (or any AI agent) reading it must not have to guess. |
| 6 | **Never paste passwords, API keys, or secret tokens here.** Write where they are stored instead (example: `in the password manager, vault "Release"`). | This file may be shared. |
| 7 | **Change something? Add a line to Part 17 (Change history).** | So everyone trusts the latest version. |

## How the questions look

```
Q4.2  What is the name of your feature-flag tool?
      Hint: The app where you switch features on and off. If you don't have one, write "config file" or "environment variable".
      Example: "Unleash (self-hosted)"
Answer: ______________________________
```

- **Q-number**: the question number (Q4.2 = Part 4, question 2).
- **Hint**: help in plain words.
- **Example**: a sample answer. **Do not copy it blindly.** Replace it with your own.
- **Answer**: where you write.

## Symbols used

| Symbol | Meaning |
|--------|---------|
| `[ ]` | A box to tick. Change to `[x]` when true. |
| **HUMAN** | Only a person may do this. |
| **AGENT** | An AI agent may do this (within the limits in Part 9). |
| **BOTH** | Either one, and the other is told. |
| 🟢 / 🟡 / 🔴 | Normal / Warning (look now) / Danger (roll back now) |

## Words you need (tiny dictionary)

| Word | Plain-language meaning |
|------|------------------------|
| **Deploy** | Putting new code on the servers or in the store. Users may not see it yet. |
| **Release** | Letting users actually see and use the new thing. |
| **Feature flag** | A light switch in your app. ON = users see the feature. OFF = they don't. |
| **Kill switch** | A flag whose only job is to turn something OFF fast in an emergency. |
| **Rollback** | Going back to the last version that worked. |
| **Rollout / Ring** | Letting more and more people in, step by step (like opening a door a little wider each time). |
| **Canary** | A tiny first group that tries the new thing first, like the canary in the coal mine. |
| **Blast radius** | How many people, or how much of the product, a mistake can hurt. |
| **Bake time** | How long you wait and watch at each step before opening wider. |
| **Guardrail metric** | A number you watch to make sure you are not breaking things (errors, crashes, failed payments). |
| **Migration** | A change to your database structure (adding a column, renaming a table). |
| **Expand / Contract** | A safe 3-step way to change the database: add the new thing, move over, remove the old thing later. |
| **Halt / Pause** | Stop a store release from reaching *more* people. It does **not** take the app off phones that already have it. |
| **On-call** | The person who answers when something breaks. |
| **Owner** | The one named person responsible. Not a team. One person. |

## How long will this take?

| Project size | Time |
|--------------|------|
| Small (1 feature, 1 platform) | about 1-2 hours |
| Medium (several features, web + mobile) | about half a day |
| Large (payments, user data, many features) | about 1 day, plus a team review |

## Who fills in what?

- **Product owner / founder (HUMAN):** Parts 1, 2, 3, 5, 7, 9, 12, 16.
- **Developer or AI coding agent (drafts, HUMAN approves):** Parts 4, 6, 8, 10, 11, 14.
- **Everyone:** Parts 13 (Incident log) and 17 (Change history), kept up to date during the launch.

> **AI agents:** You may draft answers. A HUMAN must confirm every answer in Parts 5, 7, and 9 before they take effect. Never invent a number. If an answer is unknown, write `UNKNOWN` with an owner and date.

## Before you start: have these open

- [ ] Your product's dashboard or monitoring page
- [ ] Your list of features planned for launch
- [ ] Your list of tools (hosting, flag tool, app stores, database)
- [ ] A pen or keyboard, and a calm hour

---

# Part 0 - Document Control

**Why this matters:** So everyone knows this is the right, current version.

| Field | Answer |
|-------|--------|
| Project name | |
| Document version (start at 1.0) | |
| Date first written | |
| Last updated | |
| Document owner (one person) | |
| Status | `[ ] Draft   [ ] In review   [ ] Approved   [ ] Retired` |
| Approved by (name + date) | |
| Next review date (suggest: before each ring in Part 5, and every 90 days) | |
| Link to the code repository | |
| Link to the project's main plan or spec | |

---

# Part 1 - Project Snapshot

**Why this matters:** Risk depends on what you are building. A to-do app and a payments app need different care.

**Q1.1** In one or two sentences, what does your product do, and who is it for?
Answer:

**Q1.2** Where do customers use it? Tick all that apply.
- [ ] Website / web app
- [ ] iPhone / iPad app
- [ ] Android app
- [ ] Public API used by other developers
- [ ] Other: ______

**Q1.3** Which of these does your product handle? (Each ticked item raises the risk. Rollback must be faster.)
- [ ] Money or payments
- [ ] Logins and passwords
- [ ] Personal information (names, emails, addresses, health data)
- [ ] Children's data
- [ ] Customer files or content that can't be recreated
- [ ] AI-generated content shown to customers
- [ ] Messages sent to customers (email, SMS, push notifications)
- [ ] None of these

**Q1.4** What is the **most important thing** a customer must always be able to do? (If this breaks, we roll back immediately.)
Hint: Usually sign up, log in, pay, or do the one main job of the product.
Example: "Sign in, create an invoice, and pay."
Answer:

**Q1.5** List up to 5 **critical user journeys**, the paths that must never break.

| # | Journey (start to finish) | Platform |
|---|---------------------------|----------|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |
| 5 | | |

**Q1.6** What is the **launch goal**?
- Customers expected at launch day: ______
- Target: first **500 customers** by (date): ______
- Biggest fear about the launch (one sentence):
Answer:

**Q1.7** Is there a date we cannot move? (A promised launch date, a conference, a contract.)
Answer:

---

# Part 2 - Launch Features Covered by This Plan

**Why this matters:** Every new feature should be able to be switched off on its own.

**Q2.1** List every feature or change that ships in this launch. Add rows as needed.

| # | Feature or change (plain words) | Risk: Low / Medium / High | Has a flag? (Yes/No) | Has a database change? (Yes/No) | Touches the mobile app? (Yes/No) |
|---|----------------------------------|---------------------------|----------------------|----------------------------------|----------------------------------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**How to rate risk:**
- **Low:** Looks or wording only. No money, no data.
- **Medium:** New behaviour users notice, but it's not the core journey.
- **High:** Touches money, logins, personal data, the core journey, or changes the database.

**Q2.2** Which features must **always** have a flag? (Rule: every **High** and **Medium** feature gets a flag. Low-risk features may skip.)
Answer:

**Q2.3** Which features can **not** use a flag, and what is the rollback plan instead?
Hint: Examples are a database structure change, a security patch, or code inside a mobile app binary.

| Feature | Why no flag | Rollback plan instead |
|---------|-------------|-----------------------|
| | | |

---

# Part 3 - People, Roles, and AI Agents

**Why this matters:** In an emergency nobody should wonder "who decides?"

## 3A - Humans

| Role | Name | Phone / chat handle | Backup person | Works when? (hours / time zone) |
|------|------|---------------------|---------------|---------------------------------|
| **Decision owner** (final say on rollback) | | | | |
| **On-call person** (first to respond) | | | | |
| **Flag owner** (manages flags) | | | | |
| **Database owner** (migrations and backups) | | | | |
| **Mobile release owner** (store consoles) | | | | |
| **Customer communication owner** | | | | |
| **QA / tester** | | | | |

**Q3.1** If the Decision owner cannot be reached for 15 minutes, who decides? (Write a name.)
Answer:

**Q3.2** Does anyone have a **hard "no-launch" window**? (Weekends, holidays, nights, travel.)
Hint: Avoid launching and ramping when the on-call person is asleep or travelling.
Example: "No ramp-ups on Fridays after 2 pm or on weekends."
Answer:

## 3B - AI agents

**Q3.3** List every AI agent that can touch code, flags, deploys, or monitoring.

| Agent name / tool | Job (in plain words) | Can it change flags? | Can it deploy? | Can it roll back? | Which HUMAN is responsible for it? |
|-------------------|----------------------|----------------------|-----------------|--------------------|-------------------------------------|
| | | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | |
| | | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | |

> The detailed limits for agents are set in **Part 9**. Part 3 only lists who they are.

---

# Part 4 - Tools and Places

**Why this matters:** In an emergency you need to know **where to click**. Write the link now.

**Q4.1** Fill in every row. Write `N/A - because ...` if you don't use it.

| What | Tool name | Link | Who has access? | Where is the login stored? |
|------|-----------|------|-----------------|----------------------------|
| Feature-flag tool (or "config file" / "environment variable") | | | | |
| Code repository | | | | |
| Build and deploy pipeline | | | | |
| Hosting / servers | | | | |
| Database | | | | |
| Database backups | | | | |
| Monitoring and error tracking | | | | |
| Uptime checks | | | | |
| Alerts (where do they go?) | | | | |
| Product analytics | | | | |
| App Store Connect (iOS) | | | | |
| Google Play Console (Android) | | | | |
| Over-the-air update service (if any) | | | | |
| Status page | | | | |
| Customer support inbox / chat | | | | |
| Incident chat room | | | | |
| Payment provider | | | | |
| Other third-party services that can break us | | | | |

**Q4.2** Which feature-flag tool features do you need? (Tick what your tool supports. If it lacks a ticked item, write how you will cover it.)
- [ ] Turn a flag on/off instantly without redeploying
- [ ] Percentage rollout (example: 5% of users)
- [ ] Target specific people or groups (internal team, beta list)
- [ ] Audit log (who changed what, when)
- [ ] Permissions (not everyone may flip every flag)
- [ ] Works if the flag service is down (safe fallback value)
- [ ] Separate settings for test, staging, and production
- [ ] Alerts for stale or orphaned flags

Gaps and how we cover them:
Answer:

**Q4.3** **What happens to the app if the flag tool is unreachable?** (This is called the "fallback value".)
Hint: The safe answer is almost always "feature OFF."
Answer:

**Q4.4** Where do we see **live health**, meaning the one page to look at during a rollout?
Answer (link):

---

# Part 5 - Rollout Plan (Ring Stages and Customer Milestones)

**Why this matters:** You never go from 0 to everyone in one step. You open the door a little wider each time and look around before opening more.

## 5A - The rings

**Q5.1** Confirm or change the ring ladder. These are the recommended defaults. Fill in the date and approver for each.

| Ring | Who can see it | Suggested minimum bake time (watch before opening wider) | Planned start date | Approved by (name) | Done? |
|------|----------------|-----------------------------------------------------------|--------------------|--------------------|-------|
| **Ring 0 - Team only** | Our own team and test accounts | 1 day | | | `[ ]` |
| **Ring 1 - Canary: about 1%** | A tiny group (or named friendly users when your user base is small) | 1 day | | | `[ ]` |
| **Ring 2 - About 5%** | Early adopters | 2 days | | | `[ ]` |
| **Ring 3 - About 25%** | A large slice | 2-3 days | | | `[ ]` |
| **Ring 4 - 100%** | Everyone | 7 days of extra watching | | | `[ ]` |

> **Small-audience rule:** When you only have a few dozen customers, 1% rounds to almost nobody. Replace percentages with **named people** or **customer counts** (example: "the first 10 customers"), and write the list here.

Answer (our small-audience approach):

**Q5.2** Who picks the people in each ring?
- [ ] Random users (the flag tool picks)
- [ ] Hand-picked friendly customers
- [ ] Internal team first, then random
- [ ] By region, plan, or platform (describe): ______

**Q5.3** Is there any customer who should **never** be in an early ring? (Biggest paying customers, regulated users, people in the middle of a payment.)
Answer:

## 5B - Customer milestones: the road to the first 500

**Q5.4** At each milestone, stop and check before moving on. Fill in your own date and owner.

| Milestone | Extra checks before continuing | Target date | Passed? |
|-----------|--------------------------------|-------------|---------|
| **First 10 customers** | Every journey in Q1.5 tested by a real customer. Someone talks to each customer personally. | | `[ ]` |
| **50 customers** | No unresolved High-severity bug. Support questions are being answered within the target time. | | `[ ]` |
| **100 customers** | Backups restored successfully at least once (see Part 10). The rollback drill (Part 15) has been done. | | `[ ]` |
| **250 customers** | Costs and speed are fine at this size. Flag clean-up (Part 14) is up to date. | | `[ ]` |
| **500 customers** | Launch review held. Lessons written. Decide which flags to retire and what changes before scaling further. | | `[ ]` |

## 5C - Rules for moving to the next ring

**Q5.5** Before **any** ring is widened, ALL of these must be true. Tick to confirm they are your rules, or edit them.
- [ ] The bake time for the current ring has passed.
- [ ] No 🔴 rollback trigger (Part 7) fired in that time.
- [ ] No unexplained 🟡 warnings are still open.
- [ ] The Decision owner (or an approved AGENT; see Part 9) said "go".
- [ ] The on-call person is awake and available for the next 24 hours.
- [ ] The kill switch for this feature has been tested in production **in this ring**.
- [ ] Nothing else big is shipping at the same time.

Changes to the list above:
Answer:

**Q5.6** Can an AI agent automatically move the rollout to the next ring?
- [ ] No. A human always moves it.
- [ ] Yes, but only for rings ______ and only if every box in Q5.5 is true. A human is notified.

---

# Part 6 - Feature Flags

**Why this matters:** Flags are powerful but messy if left alone. Every flag needs a name, an owner, a reason, and an end date.

## 6A - Flag types

| Type | Purpose | How long it lives | Example name |
|------|---------|-------------------|--------------|
| **release-** | Gradually show a new feature | Days to weeks. **Remove after 100% rollout.** | `release-new-checkout` |
| **ops-** (kill switch) | Emergency "turn this OFF" button | Long-lived, reviewed every quarter | `ops-disable-payments-v2` |
| **exp-** | A/B test | Until the test ends | `exp-onboarding-video` |
| **perm-** | Who is allowed (plan, role, beta list) | Long-lived | `perm-beta-testers` |

**Q6.1** Which flag types will you use? Tick all.
- [ ] release- [ ] ops- (kill switch) [ ] exp- [ ] perm-

## 6B - Naming rules

**Q6.2** Confirm or edit the naming rule. Recommended: `type-area-what-it-does`, all lowercase, words joined with dashes. The name must make sense to a stranger.
- Good: `release-checkout-new-address-form`
- Bad: `newFeature`, `test2`, `johns-flag`

Our naming rule:
Answer:

## 6C - Flag rules (confirm each)

Tick each rule you accept. If you reject one, write why.

- [ ] **Default is OFF.** A new flag starts OFF everywhere.
- [ ] **Every flag has ONE owner** (a person, not a team).
- [ ] **Every flag has a "remove by" date** (except ops- and perm- flags, which have a "review by" date).
- [ ] **Test BOTH paths** (flag ON and flag OFF) before launch. The OFF path is your rollback.
- [ ] **The server decides, not just the screen.** Hiding a button is not enough. The back end must also refuse the action when the flag is OFF.
- [ ] **A kill switch covers the whole feature**, including back-end work, scheduled jobs, emails, and notifications. A switch that only hides the button is not a kill switch.
- [ ] **One flag per feature.** Avoid flags that depend on other flags. If unavoidable, write the dependency in the registry.
- [ ] **No secrets or personal data inside flags.**
- [ ] **No reusing an old flag name for something new.**
- [ ] **Flags are not permanent settings.** Use normal configuration for settings.
- [ ] **Every flag change is logged** (who, what, when, why).
- [ ] **Only approved people can change production flags.**
- [ ] **A safe fallback value is defined** if the flag tool is unreachable (Q4.3).

Rules we are changing or rejecting, and why:
Answer:

## 6D - Flag registry (one block per flag)

**Instructions:** Copy this block for each flag. Keep all blocks in this section so there is one list of every flag. Add more blocks below as you create flags.

### Flag #1

| Field | Answer |
|-------|--------|
| Flag name | |
| Type (release / ops / exp / perm) | |
| What does it control? (one sentence) | |
| Feature it belongs to (from Q2.1) | |
| Owner (one person) | |
| Platforms affected | `[ ] Web  [ ] iOS  [ ] Android  [ ] API` |
| Default value | OFF |
| Value in production now | |
| Safe fallback if flag tool is down | |
| Depends on another flag? | `[ ] No  [ ] Yes: ______` |
| Created on | |
| **Remove by / review by** | |
| What turning it OFF does for the user (one sentence) | |
| Does the back end also check this flag? | `[ ] Yes  [ ] No - fix before launch` |
| OFF path tested on (date) | |
| ON path tested on (date) | |
| Who may change it in production? | |
| Can an AI agent switch it OFF during an emergency? | `[ ] Yes  [ ] No` |
| Link to flag in the tool | |

### Flag #2

| Field | Answer |
|-------|--------|
| Flag name | |
| Type | |
| What does it control? | |
| Feature | |
| Owner | |
| Platforms | `[ ] Web  [ ] iOS  [ ] Android  [ ] API` |
| Default value | OFF |
| Value in production now | |
| Safe fallback | |
| Depends on another flag? | |
| Created on | |
| Remove by / review by | |
| What OFF does for the user | |
| Back end checks it? | `[ ] Yes  [ ] No` |
| OFF path tested on | |
| ON path tested on | |
| Who may change it? | |
| AI agent may switch OFF? | `[ ] Yes  [ ] No` |
| Link | |

*(Copy and paste more blocks as needed.)*

## 6E - Kill switch checklist (one per High-risk feature)

For each High-risk feature, tick when true:
- [ ] It has an ops- kill switch.
- [ ] The kill switch has been **tested in production** by flipping it OFF and ON again with a test account.
- [ ] Turning it OFF stops the back-end work too, not only the screen.
- [ ] Turning it OFF leaves users with a clear message, not an error page.
- [ ] Anyone on-call can find it in under 60 seconds (link in Part 4).
- [ ] It takes effect in less than ______ minutes (write your target; 5 is typical).

---

# Part 7 - Rollback Triggers ("When do we go back?")

**Why this matters:** Decide **now**, while calm, what counts as "too broken." Most teams write these after something breaks. Don't.

## 7A - What we watch

**Q7.1** The default numbers below are starting points. Edit them to fit your product. Never leave a number blank. Write your real value in the last three columns.

**How to read:** 🟢 = fine. 🟡 = look now. 🔴 = **roll back now.**

| What we watch | How to measure | 🟢 Normal (write your own) | 🟡 Warning (default) | 🔴 Roll back (default) | Platform |
|---------------|----------------|---------------------------|----------------------|------------------------|----------|
| Error rate (failed requests) | % of requests failing | ______ | above 1% for 5 min | above 2% for 5 min | Web / API |
| Page or API speed | 95th percentile response time | ______ | 1.5x normal for 10 min | 2x normal for 10 min | Web / API |
| Crash-free sessions | % of sessions with no crash | ______ | below 99.5% | below 99.0% | iOS / Android |
| Payment failures | % of payment attempts failing | ______ | above 2% | above 3%, or any unexplained cluster | All |
| Login / sign-up failures | % failing | ______ | above 3% | above 5% | All |
| Core journey success (Q1.4) | % completing the journey | ______ | drops 5 points | drops 10 points | All |
| Customer complaints about the same problem | Count in support inbox | ______ | 2 in 1 hour | 3 in 1 hour | All |
| Data problem (wrong, missing, or leaked data) | Any report | n/a | any suspicion | **any confirmed case. Roll back immediately.** | All |
| Security concern | Any report | n/a | any suspicion | **any confirmed case. Roll back immediately.** | All |
| Server cost or load | % above normal | ______ | 1.5x | 3x | Hosting |
| AI output quality (if you use AI features) | Bad/unsafe answers per 100 | ______ | ______ | any unsafe output shown to customers | All |
| Other: ______ | | | | | |

> **Small-audience rule (very important for your first 500 customers):** With few users, percentages jump around. **Use both:**
> - "At least **100 events** in the time window" before trusting a percentage. Otherwise watch **counts**.
> - Counts rule: **3 or more of the same failure in 30 minutes** is a 🔴, even if the percentage looks small.
> - **Any** failed payment, data loss, or security issue is looked at by a human the same hour.

**Q7.2** How long do we wait before reacting to a 🔴? (Recommended: **none**. A 🔴 means act now.)
Answer:

**Q7.3** For each 🔴 in Q7.1, **who** may pull the trigger?

| Trigger | HUMAN only | AGENT may act then notify a human | BOTH |
|---------|-----------|-----------------------------------|------|
| Error rate | | | |
| Page/API speed | | | |
| Crash-free sessions | | | |
| Payment failures | | | |
| Login failures | | | |
| Core journey drops | | | |
| Complaints | | | |
| Data problem | | | |
| Security concern | | | |
| Cost/load | | | |
| AI quality | | | |

*(Tick one box per row. For Data and Security rows, the safe recommendation is "AGENT may act" to switch the feature OFF **and** "HUMAN" for everything after that.)*

## 7B - "What do I do first?" decision table

**Rule: take the smallest safe step first.** Work down the list. Stop when the problem is fixed.

| Step | Action | Typical time | Use when |
|------|--------|--------------|----------|
| 1 | **Pause the rollout.** Stop widening. Do not add more people. | seconds | Any 🟡 |
| 2 | **Turn the feature flag OFF.** | seconds to minutes | A flagged feature is the cause |
| 3 | **Shrink the ring** (example: 25% back to 5%). | minutes | Problem only with some users |
| 4 | **Revert a setting** (configuration change). | minutes | A setting was changed |
| 5 | **Redeploy the previous version** of the server or web app. | 5-30 min | Unflagged code is the cause |
| 6 | **Switch traffic back** to the old environment (blue/green). | minutes | You kept the old one running |
| 7 | **Halt the store release** and ship a fix (mobile; see Part 11). | hours-days | Mobile app is the cause |
| 8 | **Database recovery** (see Part 10). | varies | **Last resort.** Needs a human. |

**Q7.4** Is this order right for your product? Write any changes.
Answer:

**Q7.5** **Rollback speed targets.** How fast must we be back to safe?

| Situation | Target time from decision to safe |
|-----------|-----------------------------------|
| Feature flag OFF | ______ minutes (typical: 5) |
| Redeploy previous version | ______ minutes (typical: 30) |
| Mobile: halt the store release | ______ minutes (typical: 15) |
| Mobile: fix reaches users | ______ hours/days (depends on store review) |
| Database restore | ______ hours |

---

# Part 8 - Rollback Methods by Layer

**Why this matters:** "Roll back" means different things for a website, a server, a database, and a phone app. For each layer, write **how** and **who**.

**Q8.1** Fill in each row. Write `N/A - because ...` if you don't have that layer.

| Layer | Method (exact steps or link to steps) | Who may do it | Tested on (date) |
|-------|---------------------------------------|---------------|------------------|
| Feature flag | Flip flag OFF in ______ | | |
| Web front end | Redeploy previous build: ______ | | |
| Back-end services / API | Redeploy previous version: ______ | | |
| Configuration / settings | Revert to previous value: ______ | | |
| Database | See Part 10 | | |
| Mobile app (store build) | See Part 11 | | |
| Mobile (over-the-air update) | Roll back or republish the previous update: ______ | | |
| Background jobs / scheduled tasks | Pause: ______ | | |
| Emails / SMS / push notifications | Stop sending: ______ | | |
| Third-party services | Switch off integration: ______ | | |
| AI model, prompt, or agent behaviour | Return to the previous version: ______ | | |

**Q8.2** **Version memory.** Do we always know the "last known good" version?
- Last known good web/API version: ______
- Last known good mobile version: ______
- Where is that written down and kept up to date? ______

**Q8.3** **Are old versions kept and ready?** (Previous build artifacts stored, not deleted.)
- [ ] Yes, for the last ______ releases
- [ ] No - fix before launch

**Q8.4** What can **not** be rolled back, and what do we do about it?
Hint: Emails already sent, payments already taken, notifications already delivered, data already shown to other people.

| Thing that cannot be undone | What we do instead |
|------------------------------|--------------------|
| | |
| | |

---

# Part 9 - AI Agent Rules (Who May Do What Without Asking)

**Why this matters:** AI agents are fast. That is great for rollback and risky for mistakes. This part draws clear lines.

**The principle:** Agents may **act on pre-approved triggers** (Part 7) to make things **safer** (turn a flag OFF, pause a rollout). Agents never make things **riskier** without a human.

## 9A - Pre-approved agent actions (edit or delete to match your trust level)

Tick the ones you allow. Each allowed action only works when a 🔴 trigger from Part 7 (that you ticked "AGENT may act" for) has fired.

- [ ] **Pause** a rollout (stop widening).
- [ ] Switch an **ops- kill switch OFF**.
- [ ] Switch a **release- flag OFF**.
- [ ] **Shrink** a ring to a smaller percentage.
- [ ] **Open an incident** record (Part 13) and start the notification list (Part 12).
- [ ] **Halt** a store rollout (Google Play / App Store Connect), if the agent has store access.
- [ ] Redeploy the **last known good** version (backend / web only).
- [ ] Other: ______

## 9B - Always needs a human (agents must stop and ask)

These are the recommended defaults. Untick (remove) only if you truly accept the risk.
- [x] Turning any flag **ON** in production for **more** people.
- [x] Moving the rollout to the **next ring** (unless Q5.6 allows it).
- [x] Changing **database structure** or restoring a database.
- [x] Deleting data, backups, flags, or deployments.
- [x] Anything involving **money** (refunds, payment settings, pricing).
- [x] Anything touching **security settings**, keys, or permissions.
- [x] **Sending messages** to customers (emails, SMS, push, status page), unless using an approved template from Part 12 and a human is told at the same time.
- [x] Changing the numbers in Part 7 or the rules in Part 9.
- [x] Any action outside its **blast radius** (Q9.1).

## 9C - Limits and safety

**Q9.1** **Blast radius.** What is the biggest thing an agent may switch off at once?
Hint: Example "one feature at a time" or "everything shipped in the last 24 hours."
Answer:

**Q9.2** **Rate limit.** Maximum number of agent changes in one hour before it must stop and ask a human.
Hint: Typical answer: 3.
Answer:

**Q9.3** **How is a human told?** Where does the agent post, and how fast?
Example: "Posts in #incidents and calls the on-call phone within 1 minute."
Answer:

**Q9.4** **Undo.** Can a human easily reverse what an agent did?
- [ ] Yes. Steps: ______
- [ ] No - fix before launch

**Q9.5** **Stop word.** What phrase or button lets a human **freeze** all agent actions immediately?
Answer:

**Q9.6** **Proof.** Where is every agent action recorded (what, when, why, which trigger)?
Answer:

**Q9.7** **If an agent is unsure,** it must:
- [ ] Do nothing risky, ask a human, and keep watching. (Recommended)
- [ ] Other: ______

**Q9.8** **Independent check.** How do we check that the agent's "all clear" is true? (Example: "A human reads the dashboard before moving up a ring.")
Answer:

**Q9.9** **Review.** After every agent-triggered rollback, a human reviews: was it right, too early, or too late? (Recorded in Part 13.)
- [ ] Agreed

---

# Part 10 - Database and Data Rollback

**Why this matters:** Code is easy to undo. **Data is not.** A good plan avoids needing to undo it.

**Q10.1** Does this launch change the database structure (add, rename, or remove columns or tables)?
- [ ] No -> write `N/A` for the rest of this part.
- [ ] Yes -> continue.

## 10A - The safe 3-step method (Expand, Migrate, Contract)

**Rule:** Never rename or remove something in the same release that stops using it. Instead:

| Step | What happens | Separate release? |
|------|--------------|-------------------|
| **1. Expand** | **Add** the new column or table. Old code still works. | Yes |
| **2. Migrate** | New code writes to **both** old and new. Existing data is copied over. Reads move over step by step. | Yes |
| **3. Contract** | **Remove** the old column or table only after nothing uses it and you no longer need to roll back. | Yes, **later** |

**Q10.2** For each database change, fill in a row.

| Change | Step (1/2/3) | Old code still works after this? | Safe to roll back the app after this? | Release date | Owner |
|--------|--------------|-----------------------------------|----------------------------------------|--------------|-------|
| | | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | | |
| | | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | | |

> If the answer to "Old code still works?" is **No**, stop. Redesign the change into smaller steps.

## 10B - Before any database change

- [ ] **A backup was taken** within the last ______ hours (write your rule; same-day is typical).
- [ ] **We restored that backup at least once** into a test place and the data looked right. (Date: ______)
- [ ] The change was tried on a **copy of real-shaped data**.
- [ ] The change is **backward compatible** with the version of the app currently live.
- [ ] We know how long it will run and whether it **locks** a table (customers cannot use it while locked).
- [ ] We list **everything else** that reads these tables: reports, background jobs, other services, views.
- [ ] The Database owner approved. Name and date: ______

## 10C - Four different "undo" options

**Q10.3** For this launch, write the plan for each:

| Undo type | Our plan |
|-----------|----------|
| **App rollback** (put back the previous app version) | |
| **Traffic rollback** (send reads/writes back to the old path) | |
| **Data rollback** (convert new-format data back to the old format) | |
| **Schema rollback** (put the structure back) | |

> Being compatible with old code does **not** mean you can undo the data. Plan each separately.

**Q10.4** Which database changes are **one-way** (cannot be undone)? What extra approval do they need?
Answer:

**Q10.5** What is our **backup restore** target?
- Maximum data we can afford to lose: ______ (example: "1 hour")
- Maximum time to restore: ______
Answer:

---

# Part 11 - Mobile App Rollback (iOS and Android)

**Why this matters:** Once an app is on a phone, **you cannot take it back.** The only safety nets are slow release, remote switches, and fast fixes.

Skip this part with `N/A - no mobile app` if you have none.

## 11A - What "rollback" really means on mobile

| Layer | Can we undo it? | What we do instead |
|-------|----------------|--------------------|
| **App-store build already installed** | **No.** | Halt the rollout, turn flags OFF remotely, ship a fixed version. |
| **Google Play staged rollout** | **Halt** stops *new* people getting it. It is *not* a rollback. | Halt, then ship a fix as a new version. |
| **Apple phased release** | **Pause** stops further automatic rollout. People can still download it manually from the App Store. | Pause, then ship a fix or a new version. |
| **Remote feature flag** | **Yes**, instantly (if the app can read flags). | Flag OFF. |
| **Over-the-air (OTA) update of app logic** | **Yes**, for the logic that OTA can change. | Republish the previous update. |
| **Native code bug** | **No.** OTA cannot fix it. | New store release. |

## 11B - Our mobile plan

**Q11.1** Which stores do we ship to?
- [ ] Apple App Store [ ] Google Play [ ] Other: ______

**Q11.2** **Phased / staged release is ALWAYS turned on for production.**
- [ ] Agreed.
- Our Google Play percentages: ______ (example: 1% -> 5% -> 20% -> 50% -> 100%)
- Apple phased release: `[ ] On  [ ] Off - reason: ______`

**Q11.3** **Who may halt or pause** a store release, and where is the button (link)?
Answer:

**Q11.4** **Review time.** How long does store review usually take for us? Plan emergency fixes around it.
- Apple: ______ Google: ______

**Q11.5** **Do all new features ship behind a remote flag?**
- [ ] Yes
- [ ] No. Exceptions: ______

**Q11.6** **Can the app read flags quickly and safely?**
- How often does the app refresh flags? ______
- What happens if the phone has no internet? (safe default) ______
- Is there a **remote kill switch** that works for old app versions too? `[ ] Yes  [ ] No`

**Q11.7** **Minimum supported version.**
- Oldest app version we still support: ______
- Can we **force an update** (show "please update" screen)? `[ ] Yes  [ ] No`
- When would we use it? (Example: "Security hole, or a broken version that can't be fixed with flags.")
Answer:

**Q11.8** **Old versions and the server.** Does the server stay compatible with the older app versions still on people's phones?
- [ ] Yes, for at least the last ______ versions
- [ ] No - fix before launch

**Q11.9** **Hotfix plan:** how do we get a fix to users fast?
- Who can build and submit an urgent version? ______
- Expedited review request process (link or steps): ______
- Time from "bug found" to "fix available to users" at best: ______

**Q11.10** **Crash monitoring** by app version is on and sends alerts to: ______

**Q11.11** **Users who can't update.** What do we tell them, and how?
Answer:

---

# Part 12 - Communication Plan

**Why this matters:** In a bad moment, people need the right words fast. Write them now.

## 12A - Who is told, and when?

**Q12.1**

| Audience | When told | By whom | Where (channel) | Template below |
|----------|-----------|---------|-----------------|----------------|
| On-call person | Immediately, automatically | Alert system | | |
| Decision owner | Within ______ minutes | | | |
| Whole team | Within ______ minutes | | | |
| Affected customers | Within ______ minutes of confirming impact | | | T1 / T2 |
| All customers (status page) | If more than ______ people affected | | | T1 / T2 |
| Investors / partners / leaders | If ______ happens | | | |
| Regulators / legal | If data or security issue | | | |
| App stores | If needed | | | |

**Q12.2** When must we involve **legal or privacy** people? (Example: "Any confirmed leak of personal data.")
Answer:

## 12B - Message templates (edit once; reuse always)

**T1 - We found a problem:**
> "We're aware of a problem with [feature]. Some customers may see [what they see]. We're working on it and will update you by [time]. Sorry for the trouble."

**T2 - We fixed it:**
> "The problem with [feature] is fixed as of [time]. [What customers should do, if anything.] Thanks for your patience."

**T3 - We turned a feature off to keep you safe:**
> "We've temporarily switched off [feature] while we make an improvement. Your data is safe. We'll let you know when it's back."

**Q12.3** Rewrite each template in your own brand voice. Paste your versions here.
Answer (T1):
Answer (T2):
Answer (T3):

**Q12.4** Who has to **approve** public wording? (Name) ______
**Q12.5** Rule: we **never** say we know the cause until we do. `[ ] Agreed`

---

# Part 13 - Incident Log (Fill In During a Rollback)

**Instructions:** Don't fill this in now. **Copy this block every time something goes wrong** (or a rollback is triggered by a person or an agent). Keep each copy in this part, newest first.

### Incident #__ (copy me)

| Field | Answer |
|-------|--------|
| Incident number and date | |
| Time problem started (best guess) | |
| Time we noticed | |
| Time we acted (flag off / rollback started) | |
| Time safe again | |
| Who noticed? (person / agent / customer) | |
| Which ring or milestone were we in? | |
| Which trigger fired? (from Part 7) | |
| What did customers experience? | |
| How many customers affected? | |
| Which flag, version, or change was involved? | |
| What action did we take? (steps from 7B) | |
| Who acted? | `[ ] Human  [ ] Agent` Name: ______ |
| Did it work the first time? | `[ ] Yes  [ ] No - what happened next: ______` |
| Was data affected? | `[ ] No  [ ] Yes: ______` |
| Customers told? (template used, time) | |
| Severity | `[ ] Low  [ ] Medium  [ ] High` |

**Post-rollback review (within 3 working days; no blaming people):**

| Question | Answer |
|----------|--------|
| What went well? | |
| What went badly? | |
| Did the trigger fire at the right time? (too early / right / too late) | |
| Was the agent's action right? (if an agent acted) | |
| Root cause (plain words) | |
| What will we change in this document? | |
| New tasks (what, owner, due date) | |
| Safe to try the release again when? | |

---

# Part 14 - Flag Clean-Up and Lifecycle

**Why this matters:** Old flags are clutter that confuses people and hides bugs. Every flag must end.

## 14A - Life of a flag

`CREATE (OFF) -> TEST both paths -> RING 0 -> RING 1 -> RING 2 -> RING 3 -> 100% -> WATCH 7 DAYS -> REMOVE FLAG FROM CODE -> DELETE FLAG IN TOOL`

**Q14.1** How long after 100% do we remove a **release-** flag? (Recommended: 30 days maximum.)
Answer:

**Q14.2** **Clean-up rules** (tick to accept):
- [ ] A release- flag still around 30 days after 100% is **stale** and raises an alert/ticket.
- [ ] A flag with **no owner** is **orphaned** and raises an alert/ticket.
- [ ] Every month, the Flag owner reviews all flags (Q14.3).
- [ ] ops- kill switches are reviewed every quarter and **tested** at least that often.
- [ ] Max number of active flags per project: ______ (a "flag budget"; example: 20)

**Q14.3** **Monthly flag review.** For each flag ask:

| Question | If yes |
|----------|--------|
| Is a release- flag at 100%? | Remove it from the code, then delete it. |
| Is the flag at 0% and not coming back? | Remove it. |
| Does the flag have no owner? | Assign one or delete it. |
| Is it an ops- flag? | Test it. Confirm it still works. |
| Is it older than its "remove by" date? | Decide today: remove, or write a new date and reason. |

Review day of the month: ______ Reviewer: ______

**Q14.4** **Removal checklist** (for each flag removed):
- [ ] Feature has been at 100% for at least the agreed time with no 🔴.
- [ ] Code for the OFF path is removed.
- [ ] Flag is removed from the code, then deleted in the tool.
- [ ] Tests updated.
- [ ] Registry (6D) updated with the removal date.
- [ ] Mobile: confirm no supported app version still needs the flag (see Q11.7).

---

# Part 15 - Practice (Drills and Tests)

**Why this matters:** A rollback you have never practised is a rollback you cannot trust.

**Q15.1** Tick and date each drill.

| Drill | Must be done by | Done on | Result (worked / failed) | Fixes needed |
|-------|-----------------|---------|--------------------------|--------------|
| Flip a kill switch OFF then ON in production with a test account | Before Ring 1 | | | |
| Redeploy the previous web/back-end version in a test place | Before Ring 1 | | | |
| Restore the database backup into a test place | Before Ring 3 (100 customers) | | | |
| Simulate a 🔴 alert and walk through Part 7B with a human | Before Ring 2 | | | |
| Agent drill: agent turns a test flag OFF after a fake 🔴 and notifies a human | Before agent has live permission | | | |
| Halt a store rollout (practice in the console, no release needed) | Before first mobile release | | | |
| Send a test message using the status-page template | Before Ring 2 | | | |
| Full "game day": pretend a launch breaks, everyone follows this document | Before 250 customers | | | |

**Q15.2** Repeat drills every ______ months (suggest: 3). Next drill date: ______

---

# Part 16 - Lifecycle Checklist (From First Code to 500 Customers)

**Why this matters:** This is the **master checklist**. It places rollback and flag work at every stage of AI-driven development. Tick each box when it's true. Don't move to the next stage with an empty box unless you write why.

## Stage 1 - Build (AI agents and developers writing code)
- [ ] Every Medium/High feature has a flag created, default OFF (Part 6).
- [ ] The back end enforces the flag, not just the screen.
- [ ] Database changes are written as Expand / Migrate / Contract (Part 10).
- [ ] No secrets in code or flags.
- [ ] Agent-written code is labelled and reviewed by a human before merge.

## Stage 2 - Code review
- [ ] Reviewer asked: "What happens if this is switched OFF?"
- [ ] Reviewer asked: "Can we go back to the old version without losing data?"
- [ ] The change is small enough to roll back alone (not bundled with unrelated things).
- [ ] Flag names follow the naming rule (Q6.2) and flag has an owner and a remove-by date.
- [ ] Mobile: confirmed the server still works with older app versions (Q11.8).

## Stage 3 - Testing
- [ ] Flag **ON** path tested.
- [ ] Flag **OFF** path tested. (This is your rollback path.)
- [ ] All critical journeys (Q1.5) pass in both states.
- [ ] Tests for flag-tool-down fallback (Q4.3) pass.
- [ ] Database change tested on realistic data; rollback steps tried.
- [ ] Load or speed checked for High-risk features.

## Stage 4 - Staging / pre-production
- [ ] Previous version is stored and can be redeployed (Q8.3).
- [ ] Last known good version is written down (Q8.2).
- [ ] Alerts exist for every trigger in Part 7 and reach the on-call person.
- [ ] Dashboards for each ring are ready (Q4.4).
- [ ] Backups taken and restore tested (Part 10).
- [ ] Mobile build uploaded to testers (TestFlight / internal track) and flags read correctly.

## Stage 5 - Pre-launch (go / no-go)
- [ ] Parts 0-15 are complete (no blank answers).
- [ ] All drills for Ring 1 in Part 15 are done.
- [ ] On-call schedule confirmed for the first 7 days.
- [ ] Message templates ready (Part 12).
- [ ] Agent permissions confirmed in writing (Part 9).
- [ ] Decision owner has signed off (see go / no-go below).

## Stage 6 - Launch rings (Ring 0 to Ring 4)
- [ ] Every ring move follows Q5.5.
- [ ] Each ring's bake time observed.
- [ ] Incident log used for every problem (Part 13).
- [ ] Mobile: store release in phased/staged mode; halt button known.

## Stage 7 - Customer milestones (10 -> 50 -> 100 -> 250 -> 500)
- [ ] 10 customers: all milestone checks done (Q5.4).
- [ ] 50 customers: done.
- [ ] 100 customers: done, including restore drill.
- [ ] 250 customers: done, including game day.
- [ ] 500 customers: launch review held, lessons written, flags cleaned (Part 14).

## Stage 8 - After 500 customers
- [ ] All release- flags removed or have a dated plan.
- [ ] ops- kill switches kept and tested.
- [ ] This document updated with what we learned and saved as the starting point for the next project.

## Go / No-Go sign-off (before Ring 1)

| Question | Answer |
|----------|--------|
| Can we turn every High-risk feature OFF in under ______ minutes? | `[ ] Yes  [ ] No` |
| Do all alerts reach a human who is awake? | `[ ] Yes  [ ] No` |
| Has someone **other than the author** read this document? | `[ ] Yes  [ ] No` |
| Is any answer in this document still `UNKNOWN`? | `[ ] No  [ ] Yes (all have owners and dates)` |
| **Decision:** | `[ ] GO   [ ] NO-GO` |
| Decision owner name, date | |

---

# Part 17 - Change History

| Date | Version | What changed | Who | Why |
|------|---------|--------------|-----|-----|
| | 1.0 | First version | | |

---

# Appendix A - Quick Example (a tiny filled-in sample)

*Imagine a small shop app called "Tiny Shop" with a new "Fast Checkout" feature.*

**Q1.4:** "A customer can add something to the basket and pay."
**Q2.1:** Fast Checkout - risk High - has flag Yes - database change Yes - mobile Yes.
**Q6.2 flag name:** `release-checkout-fast-checkout`; kill switch: `ops-disable-fast-checkout`.
**Flag owner:** Maya. Remove by: 30 days after 100%.
**Q7.1:** Payment failures: normal 1%, 🟡 above 2%, 🔴 above 3%. Small-audience rule: 3 failed payments in 30 minutes is also 🔴.
**Q7.3:** Payment failures -> "AGENT may act" (switch `ops-disable-fast-checkout` OFF, then notify Maya within 1 minute).
**Q5.1:** Ring 1 = 10 hand-picked friendly shops, Ring 2 = first 50 customers, and so on.
**Q10.2:** Step 1 adds `new_address_id` column in release 1; Step 2 writes both columns in release 2; Step 3 removes `old_address` in release 4, a month later.
**Q11.2:** Google Play staged rollout 1% -> 5% -> 20% -> 50% -> 100%. Apple phased release on.

---

# Appendix B - Common Mistakes (and the fix)

| Mistake | Why it hurts | Fix |
|---------|--------------|-----|
| Writing rollback rules **after** something breaks | You decide while stressed | Fill Part 7 before launch |
| A kill switch **nobody has ever tested** | It may not work | Drill it (Part 15) |
| A flag that only hides the button | Someone can still call the back end | Check on the server too (Q6.2 rules) |
| Never testing the **OFF** path | Rollback itself breaks | Test OFF and ON |
| Removing a database column in the same release | Old code crashes and rollback becomes impossible | Expand / Migrate / Contract |
| Treating "halt" as "rollback" on mobile | Bad app stays on phones | Use remote flags + fast fix |
| Percentages with only a few users | Numbers jump around | Use counts and the 100-events rule |
| Flags left forever | Clutter, bugs, confusion | Remove-by dates, monthly review |
| Agents allowed to do anything | One mistake hits everyone | Part 9 limits and logs |
| Several big changes in one release | Can't tell which one broke things | Ship one risky thing at a time |

---

# Appendix C - Reference Sources Used to Build This Template

- Feature-flag lifecycle, kill switches, rollback-before-deploy criteria: VWO "Feature Flag Best Practices"; ConfigCat "Feature Flag Best Practices: 7 Common Mistakes"; Swetrix "Feature Flag Best Practices"; minware "Feature Flagging Playbook"; Plane "What is a feature flag".
- Mobile staged rollouts, halt vs rollback: Google Play Console Help "Release app updates with staged rollouts"; Expo "Updates and rollouts"; ProAndroidDev "Android app rollout tips".
- Safe database changes (expand / migrate / contract): PlanetScale "Backward compatible database changes"; Redgate "How to avoid rollbacks in Database DevOps"; DEV Community "The Expand and Contract Pattern".

*End of template. Save a copy per project, named `Rollback_and_Feature_Flags_[ProjectName].md`.*
