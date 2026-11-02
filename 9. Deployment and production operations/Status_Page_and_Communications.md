# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What this document is:** A questionnaire. You answer the questions, and by the end you have a complete plan for how your product tells customers "we are up", "we have a problem", and "we fixed it", from the first line of code until your first 500 customers.

**Who can fill it in:** Anyone. If you can read and type, you can do this. You do not need to be technical.

## The 6 simple rules

1. **Find the line that says `ANSWER:`** and type your answer right after it. Do not change the questions.
2. **Never leave a blank.** If something does not apply, write `N/A - <short reason>`. If you do not know yet, write `TBD - <who will find out> - <date>`. A blank is not allowed because blanks make people guess.
3. **Use real names and real links**, not "the team" or "the dashboard". Write `Priya Shah`, not "someone in support".
4. **Pick from the options when you see `[ ]` boxes.** Change `[ ]` to `[x]` for your choice.
5. **Write short, plain sentences.** If a 10-year-old could not understand your answer, make it simpler.
6. **Never type passwords, API keys, or tokens in this file.** Write where they are stored (example: "in our password manager, vault 'Ops'"), not what they are.

## How the questions look

| Symbol | Meaning |
|---|---|
| 🔴 **MUST** | You cannot launch without this answered. |
| 🟡 **SHOULD** | Strongly recommended. Skip only with a written reason. |
| 🟢 **NICE** | Helpful, but can wait until later phases. |
| 🤖 **AI** | An AI agent may draft this. A human must approve it. |
| 👤 **HUMAN** | Only a human may do or decide this. |
| ✅ | A checkbox. Mark `[x]` when done. |

## What the colored words in examples mean

- `Example:` shows you what a good answer looks like. Do not copy it blindly.
- `<angle brackets>` mean "replace this with your own value".

## How long this takes

| Phase of your product | Parts to fill | Time needed |
|---|---|---|
| Just starting to build | Parts 0-5 | About 60-90 minutes |
| Before launch | Parts 6-12 | About 2-3 hours |
| After launch, growing to 500 customers | Parts 13-17, review every 30 days | 30 minutes per review |

## How to know you are finished

You are finished when **Part 18 (Final Readiness Checklist)** is fully ticked and has no `TBD` left in any 🔴 MUST question.

## What to do if you get stuck

1. Read the `Why this matters` line under the question.
2. Look at the `Example`.
3. If still stuck, write `TBD - <your name> - <date>` and ask your Project Manager. Do not guess.

## The AI-agent rule (very important)

This template is built for AI-Driven Development. AI agents may **draft** messages, **suggest** severity levels, and **prepare** reports. **Only a named human can approve and publish** anything customers can see. This is set in Part 7, and every other part follows it.

---

# STATUS PAGE AND COMMUNICATIONS

> **Template version:** 1.0 · **Folder:** Deployment and production operations · **File:** `Status_Page_and_Communications.md`
> **Scope:** From first development work through launch, until the product has served its first 500 customers.
> **Reuse note:** Copy this file into each new project, then fill it in. Never edit the master template for a single project.

---

## PART 0. DOCUMENT CONTROL

🔴 **MUST.** Why this matters: so everyone knows which version is the real one and who owns it.

| Field | ANSWER |
|---|---|
| Project name | ANSWER: |
| Product one-line description (what it does, in 15 words or fewer) | ANSWER: |
| Document owner (one named human) | ANSWER: |
| Backup owner (one named human) | ANSWER: |
| Date first filled in (YYYY-MM-DD) | ANSWER: |
| Date of last review (YYYY-MM-DD) | ANSWER: |
| Next review date (at most 30 days after the last) | ANSWER: |
| Current lifecycle phase (pick one from Part 8) | ANSWER: |
| Where this file is stored (link) | ANSWER: |
| Document status | [ ] Draft  [ ] In review  [ ] Approved  [ ] Live |

### Change log

Add one row every time you change an answer. Newest on top.

| Date | Who | What changed | Why |
|---|---|---|---|
| ANSWER: | | | |

---

## PART 1. PROJECT SNAPSHOT (THE 10 FACTS EVERYONE NEEDS)

🔴 **MUST.** Why this matters: every later answer depends on these facts. Wrong facts here cause wrong messages later.

**1.1 What type of product is this?** (tick all that apply)
- [ ] Web app / SaaS
- [ ] Mobile app (iOS)
- [ ] Mobile app (Android)
- [ ] Other: ANSWER:

**1.2 Who are your customers?** (Example: "small bakeries in the US who need online orders")
ANSWER:

**1.3 What time zones are your customers in?** (This decides when you can send messages.)
ANSWER:

**1.4 Which languages must customer messages be written in?**
ANSWER:

**1.5 What is the customer-facing product URL?** ANSWER:

**1.6 Does the product use AI features** (chatbots, AI answers, AI-generated content)?
- [ ] Yes. Describe what happens if the AI breaks or gives bad answers: ANSWER:
- [ ] No

**1.7 Which outside services does your product depend on?** If these break, your customers feel it too. (Example: payment provider, login provider, email sender, cloud host, AI model provider.)

| Outside service | What it does for us | Their own status page link | Owner on our side |
|---|---|---|---|
| ANSWER: | | | |

**1.8 What is the launch date?** (YYYY-MM-DD) ANSWER:

**1.9 What is the goal for customer count?** `500 customers by` ANSWER: (date)

**1.10 What is the worst thing that could happen to a customer if the product breaks?** (Example: "they cannot take payments for their shop".) This sets how serious you treat problems.
ANSWER:

---

## PART 2. STATUS PAGE SETUP

A **status page** is a public web page that shows whether your product is working. Customers visit it first when something feels wrong. If you tell them quickly, they trust you more and contact support less.

### 2.1 Basic choices

🔴 **MUST**

| Question | ANSWER |
|---|---|
| Name of the status page tool you use (or "building our own") | ANSWER: |
| Public status page address (Example: `status.yourproduct.com`) | ANSWER: |
| Is the status page hosted **separately** from your main product? (It must be. If your product goes down and the status page is on the same server, customers see nothing.) | [ ] Yes  [ ] No - fix this before launch |
| Who pays for / renews the status page tool? | ANSWER: |
| Where are the admin login details stored? (Name the vault. **Never** the password.) | ANSWER: |
| Who has admin access? (Names. At least two people, so one vacation does not block you.) | ANSWER: |
| Does it use your own domain name and your logo? | [ ] Yes  [ ] No |

🟡 **SHOULD**

| Question | ANSWER |
|---|---|
| Is the page readable on a phone? | [ ] Yes, tested on date: ANSWER: |
| Does it pass basic accessibility checks (readable colors, works with a screen reader)? | [ ] Yes  [ ] No  [ ] Not tested |
| Is there a link to the status page in the product footer, the help center, and the "contact support" page? | [ ] Yes  [ ] No |
| Can customers subscribe to updates by email? | [ ] Yes  [ ] No |
| Can customers subscribe by text message, RSS, or webhook? | ANSWER: |

### 2.2 Public or private?

🔴 **MUST**

- [ ] **Public** (anyone can see it)
- [ ] **Private** (only logged-in customers can see it)
- [ ] **Both** (public summary and a private detailed page)

Why you chose this: ANSWER:

### 2.3 Components (the parts of your product shown on the page)

A **component** is one piece customers care about, for example "Login", "Payments", "Mobile app", "API". Keep it to **3-10 components**. Use names customers understand, not your internal server names.

🔴 **MUST**

| # | Component name (customer-friendly) | One sentence: what it means to the customer | Owner (human) | How we check it is working (tool or test) | Depends on (from 1.7) |
|---|---|---|---|---|---|
| 1 | ANSWER: | | | | |
| 2 | | | | | |
| 3 | | | | | |

### 2.4 Status words (use exactly these everywhere)

Do not invent new words. The same words must appear on the status page, in emails, and in support replies.

| Status word | Meaning in plain English | Color |
|---|---|---|
| **Operational** | Everything works. | Green |
| **Degraded performance** | It works, but slowly or with small errors. | Yellow |
| **Partial outage** | Some customers or some features do not work. | Orange |
| **Major outage** | It does not work for most customers. | Red |
| **Under maintenance** | We are doing planned work. | Blue |

Do you want to change any of these words? [ ] No (recommended)  [ ] Yes: ANSWER:

### 2.5 Automatic vs. manual updates

🟡 **SHOULD.** Why this matters: automatic checks can wrongly say "all good" when something is broken, and humans can forget to update.

| Component (from 2.3) | Updated by | How |
|---|---|---|
| ANSWER: | [ ] Automatic checks  [ ] Human  [ ] Both | |

**What must never be automatic?** Writing the public words about a problem (see Part 7). ✅ Confirmed: [ ]

### 2.6 History and transparency

🟡 **SHOULD**

- How many days of past problems are shown on the page? (Recommended: 90.) ANSWER:
- Do you show uptime percentages? [ ] Yes  [ ] No. If yes, who checks these numbers are honest? ANSWER:
- Rule: **we never delete a past incident to look better.** ✅ Agreed: [ ]

---

## PART 3. SEVERITY LEVELS (HOW BAD IS IT?)

**Severity** is how serious a problem is. It decides who gets woken up, how fast you speak, and how often you update. Using the same four levels in every project means every team speaks the same language.

🔴 **MUST.** Read the table, then answer 3.2 for your product.

### 3.1 The four standard levels

| Level | Name | Plain-English meaning | Example | Status page word | First public message within | Update every |
|---|---|---|---|---|---|---|
| **Sev1** | Critical | The product is down or unsafe for most customers. Money, data, or security is at risk. | Nobody can log in. Payments fail. Customer data exposed. | Major outage | 15 minutes | 30 minutes |
| **Sev2** | Major | An important feature is broken for many customers, with no good workaround. | Search is broken. Mobile app crashes on opening for some phones. | Partial outage | 30 minutes | 60 minutes |
| **Sev3** | Minor | Something is broken or slow, but customers can still do their main task. | Reports load slowly. One setting will not save. | Degraded performance | 2 hours | 4 hours, or when something changes |
| **Sev4** | Informational | Small issue, cosmetic problem, or a heads-up. | A typo on a page. A third-party service has a small hiccup. | Usually no status change; a note may be added | Next business day | When resolved |

> You may change the minutes and hours below in 3.2. Do not change the level names.

### 3.2 Your product's version

🔴 **MUST**

| Question | ANSWER |
|---|---|
| Keep the standard timings above? | [ ] Yes (recommended)  [ ] No, use the timings below |
| Sev1 first message within (minutes) | ANSWER: |
| Sev1 update every (minutes) | ANSWER: |
| Sev2 first message within (minutes) | ANSWER: |
| Sev2 update every (minutes) | ANSWER: |
| Sev3 first message within | ANSWER: |
| Sev3 update every | ANSWER: |

**Write 2 examples from YOUR product for each level.** (This is what removes guessing during a real emergency.)

| Level | Example 1 from our product | Example 2 from our product |
|---|---|---|
| Sev1 | ANSWER: | |
| Sev2 | | |
| Sev3 | | |
| Sev4 | | |

### 3.3 "If unsure" rules

🔴 **MUST.** Why this matters: in the first minutes nobody knows how big a problem is.

- **If unsure between two levels, pick the more serious one.** You can lower it later. ✅ Agreed: [ ]
- **If you are not sure whether to post, post.** A short "we are looking into it" is better than silence. ✅ Agreed: [ ]
- **Who can change a severity level?** ANSWER:

### 3.4 Special triggers (these always count as at least Sev2)

Tick everything that applies to you:
- [ ] Any suspected leak or loss of customer data (also read Part 15)
- [ ] Payments or billing wrong or failing
- [ ] Login or sign-up not working
- [ ] Mobile app crashes on launch
- [ ] AI feature giving harmful, wrong, or private answers
- [ ] Wrong data shown to the wrong customer
- [ ] Other: ANSWER:

---

## PART 4. PEOPLE AND ROLES (WHO DOES WHAT)

🔴 **MUST.** Why this matters: during a problem, people freeze or all do the same job. Named roles fix this. One person can hold several roles in a tiny team, but **every role must have a name and a backup**.

### 4.1 The roles

| Role | What they do in plain English | Primary (name) | Backup (name) | How to reach them (phone/chat, not password) |
|---|---|---|---|---|
| **Incident Lead** | Runs the response. Makes the calls. Does not fix things. | ANSWER: | | |
| **Communications Lead** | Writes and posts customer messages. | ANSWER: | | |
| **Approver** 👤 | The only person who can say "yes, publish this". Can be the Incident Lead. | ANSWER: | | |
| **Technical Lead** | Finds and fixes the problem. | ANSWER: | | |
| **Support Lead** | Answers customers who write in. Uses the same words as the status page. | ANSWER: | | |
| **Executive contact** | Told about every Sev1. | ANSWER: | | |
| **Scribe** (optional) | Writes down times and decisions as they happen. | ANSWER: | | |

### 4.2 Small-team rule

If your team has fewer than 5 people, write who holds two or more roles and who is their backup. **A person must never be both the only fixer and the only communicator during a Sev1.** If you cannot avoid it, write the plan:
ANSWER:

### 4.3 On-call

| Question | ANSWER |
|---|---|
| Is there an on-call schedule? | [ ] Yes, link: ANSWER:  [ ] No, explain: ANSWER: |
| What tool pages people? | ANSWER: |
| Who is paged for Sev1 outside work hours? | ANSWER: |
| What if the first person does not answer in 10 minutes? | ANSWER: |
| Official work hours and time zone | ANSWER: |

---

## PART 5. COMMUNICATION CHANNELS (WHERE WE TALK TO CUSTOMERS)

🔴 **MUST.** For each channel, tick whether you use it, say who owns it, and say when to use it.

| Channel | Used? | Owner | Use it for which severities? | Notes |
|---|---|---|---|---|
| Status page | [ ] Yes  [ ] No | ANSWER: | Sev1, Sev2, Sev3 | **The single source of truth.** All other channels must match it. |
| Email to subscribers | [ ] Yes  [ ] No | | Sev1, Sev2 | |
| In-app banner (web or mobile) | [ ] Yes  [ ] No | | Sev1, Sev2 | Banner must link to the status page. |
| Mobile push notification | [ ] Yes  [ ] No | | Sev1 only, or major planned downtime | Overuse annoys people into turning notifications off. |
| Social media (name the accounts) | [ ] Yes  [ ] No | | Sev1, Sev2 | Account names: ANSWER: |
| Community (Discord, Slack, forum) | [ ] Yes  [ ] No | | Sev1, Sev2 | Which community: ANSWER: |
| Support desk auto-reply / macro | [ ] Yes  [ ] No | | Sev1, Sev2, Sev3 | |
| Direct text or phone call to VIP customers | [ ] Yes  [ ] No | | Sev1 | Who counts as VIP is defined in Part 12. |

### 5.1 Golden rules (do not skip)

1. **One source of truth.** Status page first. Every other channel repeats it or links to it. ✅ [ ]
2. **Same facts, same words, everywhere.** ✅ [ ]
3. **Do not guess the cause in public.** Say what customers experience, not why. ✅ [ ]
4. **Never blame a person, a vendor, or a customer in public.** ✅ [ ]
5. **Never promise a fix time you cannot guarantee.** Say when the next update comes instead. ✅ [ ]
6. **Never share private customer data, secrets, or internal system details in public.** ✅ [ ]
7. **Always say when the next update will come, then keep that promise.** ✅ [ ]

### 5.2 If the status page itself is down

🔴 **MUST**

| Question | ANSWER |
|---|---|
| Backup channel we use instead | ANSWER: |
| Who can post there | ANSWER: |
| Link to the backup | ANSWER: |

---

## PART 6. CUSTOMER SUBSCRIPTIONS AND CONTACT LISTS

🟡 **SHOULD**

| Question | ANSWER |
|---|---|
| Where do customers sign up for updates? | ANSWER: |
| Do we ask for permission before emailing them? | [ ] Yes (required in most countries)  [ ] No - fix this |
| Does every email include an unsubscribe link? | [ ] Yes  [ ] No |
| Is the "from" email address one customers recognize? | ANSWER: |
| Are status emails sent from a **different** email service than our normal product emails? (If the main email service fails, status emails still go out.) | [ ] Yes  [ ] No |
| Who keeps the VIP / key-customer list up to date? | ANSWER: |

---

## PART 7. AI-AGENT RULES FOR COMMUNICATIONS

This product is built with AI-Driven Development. This part sets what an AI agent **may** and **may not** do. Chosen mode for this template: **AI drafts, a human approves.**

🔴 **MUST.** Why this matters: an AI can write a perfect-sounding message that is factually wrong. A wrong public message is worse than a late one.

### 7.1 What AI agents MAY do

- 🤖 Suggest a severity level (a human confirms).
- 🤖 Draft status updates from the templates in Part 10.
- 🤖 Draft emails, in-app banners, and support macros.
- 🤖 Check drafts for tone, spelling, and the golden rules in 5.1.
- 🤖 Summarize logs and timelines for the humans.
- 🤖 Draft the post-incident report (Part 14).
- 🤖 Prepare the weekly numbers (Part 13).

### 7.2 What AI agents MAY NOT do

- ❌ Publish anything customers can see without human approval.
- ❌ Change a status page component to "Operational" without a human check.
- ❌ State a cause, a fix time, or a customer count as fact unless a named human confirmed it.
- ❌ Send a message to a VIP, to the press, or to regulators.
- ❌ Delete or edit past incident records.
- ❌ Receive or store passwords, keys, or private customer data.

### 7.3 The approval rule

| Question | ANSWER |
|---|---|
| Who is the named human Approver? (from 4.1) | ANSWER: |
| Backup Approver | ANSWER: |
| How does the Approver say yes? (Example: reply "APPROVED" in the incident chat channel) | ANSWER: |
| How long can a draft wait for approval before escalating to the backup? | ANSWER: minutes |
| For Sev3 and Sev4, can a Communications Lead (not just the Approver) approve? | [ ] Yes  [ ] No |

### 7.4 Required "AI draft check" (the human checks all 6 before approving)

1. ☐ Are the facts true right now? (Time, affected feature, status word.)
2. ☐ Does it say what customers **feel**, not our internal cause?
3. ☐ Is the next-update time included, and can we keep it?
4. ☐ Is it free of blame, guesses, secrets, and private data?
5. ☐ Does it use the exact status words from 2.4?
6. ☐ Would a non-technical customer understand it?

### 7.5 AI agent setup

| Question | ANSWER |
|---|---|
| Which AI tool or agent is used for drafting? | ANSWER: |
| Where are the agent's instructions stored? (link) | ANSWER: |
| What files may the agent read? (name them) | ANSWER: |
| Where does the agent save drafts before approval? | ANSWER: |
| Who reviews the agent's drafts weekly to catch mistakes? | ANSWER: |
| Where do we record every AI mistake we catch? | ANSWER: |

---

## PART 8. THE LIFECYCLE: FROM FIRST CODE TO 500 CUSTOMERS

Your product moves through **6 phases**. For each phase this part gives you questions and a checklist. **Fill in only your current phase and the ones before it.** The later phases can wait, but read them early so nothing surprises you.

| Phase | Name | You are here when... | Customers |
|---|---|---|---|
| **1** | Build | Code is being written. No outside users yet. | 0 |
| **2** | Pre-launch | Testing with a small private group; getting ready. | 0-20 testers |
| **3** | Launch day and week 1 | The product opens to the public. | 1-10 |
| **4** | Early customers | Learning fast; many small problems. | 11-50 |
| **5** | Growing | Customers rely on you; problems cost money. | 51-200 |
| **6** | Scaling to 500 | Process must work without heroics. | 201-500 |

**Which phase are you in now?** ANSWER:

### PHASE 1: BUILD (0 customers)

Goal: decide the plan before there is any pressure.

🔴 **MUST**
- ✅ Parts 0-5 and 7 are filled in. [ ]
- ✅ Status page tool chosen and account created. [ ]
- ✅ Components listed (2.3) and match what the product really has. [ ]
- ✅ Every outside service in 1.7 has its status page link saved. [ ]
- ✅ Health checks exist for each component (the product can tell us when something is broken). [ ]

🟡 **SHOULD**
- ✅ Draft all message templates in Part 10 using your product's real names. [ ]
- ✅ AI agent has the instructions in Part 7 and can draft a test message. [ ]

Questions:

| Question | ANSWER |
|---|---|
| What does the status page show while no customers exist yet? (Example: "Coming soon", or all Operational) | ANSWER: |
| What is the first alarm that will tell us something broke? | ANSWER: |
| Who receives it? | ANSWER: |

### PHASE 2: PRE-LAUNCH (private testers)

Goal: prove the plan works **before** real customers need it.

🔴 **MUST**
- ✅ Run one **practice drill** (Part 16): pretend a Sev2 happened; post a test update to a **private** test status page. [ ]
- ✅ Measure: how many minutes from "we noticed" to "first message approved"? ANSWER: minutes
- ✅ Every person in 4.1 has been told their role in writing. [ ]
- ✅ Subscriber sign-up and unsubscribe tested end to end. [ ]
- ✅ In-app banner shown correctly on web and on a real phone. [ ]
- ✅ Backup channel (5.2) tested. [ ]
- ✅ Legal and privacy review of Part 15 done. [ ]
- ✅ Support Lead has the support macros (Part 12) loaded. [ ]

Questions:

| Question | ANSWER |
|---|---|
| Who are the testers? (number and how chosen) | ANSWER: |
| How do testers report problems? | ANSWER: |
| What did the drill teach us? | ANSWER: |
| What did we change after the drill? | ANSWER: |

### PHASE 3: LAUNCH DAY AND WEEK 1 (1-10 customers)

Goal: stay calm and visible during the busiest week.

🔴 **MUST**
- ✅ Status page is **public** and linked from the product and help center. [ ]
- ✅ Someone is on call for the whole launch window (name and hours): ANSWER:
- ✅ A "launch war room" chat channel exists: ANSWER:
- ✅ Launch announcement mentions the status page. [ ]
- ✅ Check status page and alarms every 2 hours on launch day (who does this): ANSWER:
- ✅ Daily 10-minute review in week 1: "Any problems? Anything customers asked about?" [ ]

Questions:

| Question | ANSWER |
|---|---|
| What is the exact date and time of launch? (include time zone) | ANSWER: |
| What do we do if launch must be paused? Who decides? What do we tell customers? | ANSWER: |
| What is our "pause launch" trigger? (Example: "Sev1 open for more than 30 minutes") | ANSWER: |

### PHASE 4: EARLY CUSTOMERS (11-50 customers)

Goal: learn from every problem; every customer matters a lot.

🔴 **MUST**
- ✅ Every incident, even Sev4, has a short record (Part 14, "short form"). [ ]
- ✅ Weekly 30-minute review of incidents and customer complaints. [ ]
- ✅ Personally reply to every customer who reports a problem. [ ]

🟡 **SHOULD**
- ✅ Ask affected customers: "Was our message clear?" [ ]
- ✅ Add new components to the status page if customers asked about a feature that is missing. [ ]

Questions:

| Question | ANSWER |
|---|---|
| Which problem happened most often? | ANSWER: |
| Did any customer first learn about a problem from us, or did we learn from them? (Goal: from us.) | ANSWER: |
| What one thing do we fix first? | ANSWER: |

### PHASE 5: GROWING (51-200 customers)

Goal: stop relying on any one hero.

🔴 **MUST**
- ✅ On-call schedule rotates; no one is on call alone for more than 1 week at a time. [ ]
- ✅ Planned maintenance is announced at least 72 hours ahead (Part 11). [ ]
- ✅ Postmortems done for all Sev1 and Sev2 (Part 14). [ ]
- ✅ VIP/key-customer list exists and is used (Part 12). [ ]

🟡 **SHOULD**
- ✅ Uptime numbers reported monthly (Part 13). [ ]
- ✅ Status page subscribers ≥ 30% of customers. [ ]
- ✅ A second Approver is trained. [ ]

Questions:

| Question | ANSWER |
|---|---|
| How many incidents this month by level (Sev1 / Sev2 / Sev3 / Sev4)? | ANSWER: |
| Are we meeting the timings in 3.2? | [ ] Always  [ ] Mostly  [ ] No |
| Do we need to add a customer agreement on uptime (SLA)? See Part 15. | ANSWER: |

### PHASE 6: SCALING TO 500 (201-500 customers)

Goal: the system works even when the usual people are away.

🔴 **MUST**
- ✅ Every role has a trained backup who has run at least one drill. [ ]
- ✅ Quarterly drill done (Part 16). [ ]
- ✅ A full review of this document completed; template improvements sent back to the master template. [ ]
- ✅ Customer communication metrics (Part 13) meet targets, or there is a written plan to fix. [ ]

Questions:

| Question | ANSWER |
|---|---|
| At 500 customers, what breaks first in this plan? | ANSWER: |
| What must change for the next stage (500 to 5,000)? | ANSWER: |
| What did we learn that should go in the master template? | ANSWER: |

---

## PART 9. THE INCIDENT COMMUNICATION WORKFLOW (STEP BY STEP)

Use this during a real problem. Print it. Pin it. Follow the steps in order.

### The 7 stages

| # | Stage | What you do | Who | Public status word | Done? |
|---|---|---|---|---|---|
| 1 | **Detect** | An alarm, a customer, or a teammate reports a problem. Write down the time. | Anyone | (none yet) | ☐ |
| 2 | **Decide severity** | Use Part 3. If unsure, pick the higher level. | Incident Lead | (none yet) | ☐ |
| 3 | **Assign roles** | Name Incident Lead, Communications Lead, Technical Lead in the incident chat. | Incident Lead | (none yet) | ☐ |
| 4 | **Acknowledge** | Post the first message (Template A, Part 10). Short. No guessing. | Communications Lead + Approver | Per severity table | ☐ |
| 5 | **Update** | Post on the schedule in 3.2, even if nothing changed ("still working on it"). | Communications Lead | Same or changed | ☐ |
| 6 | **Resolve** | Confirm it is fixed and **stays** fixed for at least 15 minutes. Post Template D. | Incident Lead + Approver | Operational | ☐ |
| 7 | **Learn** | Write the post-incident report (Part 14) in the time set there. | Incident Lead | n/a | ☐ |

### 9.1 Message must-haves (every public update contains)

1. **What** customers experience (plain words).
2. **Who** is affected (everyone? some? which feature, which region?).
3. **Since when** (time with time zone).
4. **What to do** (a workaround, or "no action needed").
5. **When** the next update comes.

### 9.2 Incident chat rules

| Question | ANSWER |
|---|---|
| Where do we run the incident chat? (channel name) | ANSWER: |
| Who creates it? | ANSWER: |
| Where are timestamps and decisions written down? | ANSWER: |
| Where does the Technical Lead post fixes? (separate from customer messages) | ANSWER: |

### 9.3 When a vendor is the cause

Example: your payment provider is down.

- Show the affected component as degraded or down on **your** status page. ✅ [ ]
- Say "a service we depend on" — do not name or blame. ✅ [ ]
- Link to their status page only if it helps customers. Decision: ANSWER:

---

## PART 10. MESSAGE TEMPLATES (COPY, FILL IN, SEND)

All templates are written in simple words. **Replace everything in `<angle brackets>`.** Approver must approve before publishing (Part 7).

### Template A: First message ("We are looking into it")

**Title:** `<Feature name> issue`
**Status word:** `<Investigating / pick from 2.4>`

> We are looking into a problem with **<feature>**. Some customers may see **<what they see>**. This started around **<time and time zone>**.
> We are working on it. Our next update will be by **<time>**.

### Template B: Identified ("We know what it is")

> Update: We found the cause of the **<feature>** problem and are working on a fix. **<Who is affected, plainly>**.
> **<Workaround if any, otherwise "You do not need to do anything.">**
> Next update by **<time>**.

### Template C: Monitoring ("Fixed, watching")

> A fix has been applied to the **<feature>** problem. We are watching to make sure it stays fixed. You may need to **<action, e.g., refresh the page>**.
> Next update by **<time>**.

### Template D: Resolved

> The **<feature>** problem is resolved as of **<time and time zone>**. It affected **<who>** for about **<duration>**.
> We are sorry for the trouble. We will share what happened in a short summary within **<days>**.

### Template E: Still working (no news)

> We are still working on the **<feature>** problem. No change yet. Our next update will be by **<time>**.

### Template F: Short email subject lines

- `[Active] <Feature> issue: we are working on it`
- `[Resolved] <Feature> issue`
- `[Planned] <Feature> maintenance on <date>`

### Template G: In-app banner (max 140 characters)

> `<Feature> is having problems. We are on it. Details: <status page link>`

### Template H: Social media post (keep under 280 characters)

> We are aware of an issue affecting **<feature>**. We are working on it. Updates: **<status page link>**

### Template I: Support reply (for Support Lead)

> Hi **<name>**, thank you for writing in. Yes, we are aware of the issue with **<feature>**. Our team is working on it. The latest update is at **<status page link>**. We will email you when it is resolved. Sorry for the trouble.

### Template J: Message for VIP / key customers (human-written only)

> Hi **<name>**, a quick personal note. We have a problem with **<feature>** that may affect **<their usage>**. We are working on it and I will update you by **<time>**. You can reach me directly at **<contact>**.

### Your project's custom wording

🟡 **SHOULD.** Fill these in so nobody invents words in a crisis.

| Question | ANSWER |
|---|---|
| Our brand voice in 3 words (Example: "calm, honest, friendly") | ANSWER: |
| Words we always use for our product's main feature | ANSWER: |
| Words and phrases we never use (Example: "unfortunately", "glitch", blaming words) | ANSWER: |
| Our standard apology sentence | ANSWER: |
| Our sign-off | ANSWER: |

---

## PART 11. PLANNED MAINTENANCE COMMUNICATION

Maintenance is work you plan ahead (upgrades, moving servers). Telling customers early is a trust-builder.

🔴 **MUST**

| Question | ANSWER |
|---|---|
| How far ahead do we announce planned downtime? (Recommended: 72 hours or more) | ANSWER: |
| Reminder messages: how many and when? (Example: 24 hours before and 1 hour before) | ANSWER: |
| Preferred maintenance window (day, time, time zone). Pick the quietest time for customers. | ANSWER: |
| Who approves a maintenance announcement? | ANSWER: |
| What do we do if maintenance runs longer than promised? (Post Template E and a new time.) | ANSWER: |

### Template K: Maintenance announcement

> **Planned maintenance:** On **<date>** from **<start>** to **<end>** (**<time zone>**), **<feature>** will be **<unavailable / slower>** while we **<plain-English reason>**. **<What customers should do beforehand, if anything>**. Questions? **<contact>**.

### Template L: Maintenance finished

> Maintenance on **<feature>** is complete. Everything is working normally. Thank you for your patience.

---

## PART 12. SUPPORT AND VIP CUSTOMER HANDLING

🟡 **SHOULD**

| Question | ANSWER |
|---|---|
| Who counts as a VIP / key customer? (Example: first 25 customers, or paying over $X, or named partners) | ANSWER: |
| Where is the VIP list stored? | ANSWER: |
| Which severity triggers a personal message to VIPs? | ANSWER: |
| Who sends it? (human only) | ANSWER: |
| Support macros loaded in our help desk (list names) | ANSWER: |
| Does support have a link to the status page pinned? | [ ] Yes  [ ] No |
| What do support agents say if a customer is angry? (link to guide or write 3 sentences) | ANSWER: |
| Compensation rules (credit, refund, extension) — who decides, and under what conditions? | ANSWER: |

**Rule:** Support never contradicts the status page. If support knows something the page does not, tell the Communications Lead first.  ✅ Agreed: [ ]

---

## PART 13. METRICS: HOW WE KNOW COMMUNICATIONS ARE WORKING

🟡 **SHOULD** (start tracking from Phase 3).

### 13.1 Numbers to track

| Metric | What it means | Target | Current value |
|---|---|---|---|
| **Time to first message** | Minutes from "we noticed" to first public message | Follow 3.2 | ANSWER: |
| **Update on time %** | Share of updates sent by the promised time | 90%+ | |
| **Time to resolve** | Minutes from start to fixed | Track trends | |
| **Customers told by us first %** | Share of incidents where we posted before customers complained | 80%+ | |
| **Support tickets per incident** | How many customers wrote in | Lower is better | |
| **Status page subscribers** | Number of subscribers | Phase targets below | |
| **Uptime %** (by component) | Share of time working | State target in Part 15 | |
| **Post-incident reports finished on time %** | Reports done within deadline | 100% for Sev1/2 | |
| **AI draft corrections** | How often a human had to fix an AI draft | Falling over time | |

### 13.2 Customer milestone targets

| Customer count | Required before this milestone | Review by |
|---|---|---|
| 1 | Status page public, roles named | ANSWER: |
| 10 | First real incident handled using this document | |
| 50 | Weekly incident review running; VIP list exists | |
| 100 | Postmortems for Sev1/Sev2; subscribers ≥ 30% | |
| 250 | Trained backups for every role; quarterly drill done | |
| 500 | Full review of this document; lessons sent to master template | |

### 13.3 Reporting rhythm

| Question | ANSWER |
|---|---|
| Who prepares the weekly summary? (AI may draft, a human checks) | ANSWER: |
| Where is it posted? | ANSWER: |
| Who reads it? | ANSWER: |
| Who decides what to change? | ANSWER: |

---

## PART 14. POST-INCIDENT REPORTS (LEARNING, NOT BLAMING)

After a problem is fixed, write down what happened so it does not happen again. **No blaming people.** Blame the process.

🔴 **MUST**

| Question | ANSWER |
|---|---|
| Which severities need a **full** report? (Recommended: Sev1, Sev2) | ANSWER: |
| Which need the **short form**? (Recommended: Sev3, Sev4) | ANSWER: |
| Deadline to finish a full report after resolve (Recommended: 5 business days) | ANSWER: |
| Deadline to share a customer summary after a Sev1 (Recommended: 3 business days) | ANSWER: |
| Who owns the report? | ANSWER: |
| Where are reports stored? | ANSWER: |

### Short form (copy for each small incident)

| Field | ANSWER |
|---|---|
| Date and time start / end (with time zone) | |
| Severity | |
| What customers experienced | |
| Cause in one sentence | |
| What we did | |
| Did we post on time? | [ ] Yes  [ ] No |
| One thing to change | |

### Full form

1. **Summary** (3 sentences, plain language):
2. **Impact** (who, how many, how long, money lost if known):
3. **Timeline** (every key time, with time zone):

   | Time | What happened | Who |
   |---|---|---|
   | | | |

4. **Cause** (what actually broke and why, in plain words):
5. **What went well:**
6. **What went badly:**
7. **Communication review.** Answer each:
   - Did we post the first message on time? [ ] Yes  [ ] No
   - Did every update arrive when we promised? [ ] Yes  [ ] No
   - Were messages clear to non-technical customers? [ ] Yes  [ ] No
   - Did support and the status page agree? [ ] Yes  [ ] No
   - Did the AI agent draft help or hurt? Explain:
8. **Action items** (each needs an owner and a due date):

   | Action | Owner | Due date | Done |
   |---|---|---|---|
   | | | | ☐ |

9. **Customer-facing summary** (short, honest, no blame):

> **Template M: Customer summary**
> On **<date>**, **<feature>** was **<unavailable / slow>** for about **<duration>**. This affected **<who>**. The cause was **<one plain sentence>**. We fixed it by **<one plain sentence>**. To prevent it from happening again, we are **<one or two changes>**. We are sorry for the trouble.

---

## PART 15. LEGAL, PRIVACY, AND AGREEMENTS

🔴 **MUST.** Why this matters: some problems carry legal deadlines that cannot be missed. **This section is not legal advice. Have a qualified lawyer review your answers.**

### 15.1 Data and security incidents

| Question | ANSWER |
|---|---|
| Does the product store personal data (names, emails, payment info, health data)? | [ ] Yes  [ ] No |
| In which countries/regions do customers live? (This decides which privacy laws apply.) | ANSWER: |
| Which privacy laws apply? (Example: GDPR, CCPA, HIPAA, local laws) | ANSWER: |
| Who is the person responsible for privacy / data protection? | ANSWER: |
| Who must be told if personal data leaks, and within what deadline? (Ask your lawyer; some laws require notice within 72 hours.) | ANSWER: |
| Who writes and approves a breach notice? (Always a human, with legal review.) | ANSWER: |
| Who contacts regulators? | ANSWER: |

**Rule:** If a data leak is even suspected, tell the Incident Lead and privacy owner immediately. **Do not** post details publicly until they approve. ✅ Agreed: [ ]

### 15.2 Uptime promises (SLA)

| Question | ANSWER |
|---|---|
| Do we promise customers a minimum uptime? | [ ] Yes: ANSWER: % per month  [ ] No (write "best effort" in the terms) |
| What do customers get if we miss it? (credit, refund, none) | ANSWER: |
| How do customers ask for it? | ANSWER: |
| Who checks the uptime numbers? | ANSWER: |

### 15.3 Terms and records

| Question | ANSWER |
|---|---|
| Do our terms of service mention the status page? | [ ] Yes  [ ] No |
| How long do we keep incident records? | ANSWER: |
| Do we have to keep records for audits? (Example: SOC 2, ISO 27001) | [ ] Yes: ANSWER:  [ ] No |

### 15.4 Honesty rule

> **We never hide an outage, delete a past incident, or claim "operational" while customers are affected.** ✅ Agreed: [ ]

---

## PART 16. PRACTICE DRILLS AND TESTING

You do not know whether this plan works until you try it. A drill is a pretend problem.

🔴 **MUST** before launch; 🟡 **SHOULD** every 3 months afterward.

### 16.1 Drill plan

| Question | ANSWER |
|---|---|
| Date of first drill | ANSWER: |
| Who runs the drill? | ANSWER: |
| Which scenario? (Example: "Login stops working", "Payment provider down", "AI feature gives wrong answers", "Status page tool down") | ANSWER: |
| Where do we post drill messages? (a **private test** page, never the public page) | ANSWER: |
| Next drill date | ANSWER: |

### 16.2 Drill scorecard (fill in after each drill)

| Check | Result |
|---|---|
| Time from alarm to first approved message | ANSWER: minutes |
| Was severity chosen within 10 minutes? | [ ] Yes  [ ] No |
| Did every role-holder know their job? | [ ] Yes  [ ] No |
| Did the AI draft follow the templates and rules? | [ ] Yes  [ ] No |
| Did the Approver respond within the time in 7.3? | [ ] Yes  [ ] No |
| Did the backup channel work (5.2)? | [ ] Yes  [ ] No |
| Were updates sent on schedule? | [ ] Yes  [ ] No |
| What do we change now? | ANSWER: |

### 16.3 Pre-launch test checklist

- ☐ Create a test incident on the private test page. Confirm it shows correctly.
- ☐ Subscribe a test email. Confirm it receives the message.
- ☐ Unsubscribe the test email. Confirm it stops.
- ☐ Show the in-app banner on web and on a real phone.
- ☐ Send a test push notification to a team phone (if used).
- ☐ Confirm the status page loads on mobile.
- ☐ Switch off the main product in a test environment; confirm the status page still loads.
- ☐ Ask an AI agent to draft a message; run the 6-point check in 7.4.
- ☐ Ask someone outside the team to read a draft; ask "Do you understand it?"
- ☐ Confirm all admin people can log in to the status page tool.

---

## PART 17. KEEPING THIS DOCUMENT HEALTHY

🟡 **SHOULD**

| Question | ANSWER |
|---|---|
| Review rhythm (Recommended: every 30 days until 500 customers, then every 90 days) | ANSWER: |
| Who reviews? | ANSWER: |
| What triggers an extra review? (Example: any Sev1, a new component, a new vendor, a new team member, a new country) | ANSWER: |
| When someone leaves the team, who updates Part 4? | ANSWER: |
| When we add a new feature, who updates Part 2.3? | ANSWER: |

### Review checklist (each review)

- ☐ All names and phone/chat contacts still correct (Part 4).
- ☐ All components still match the product (Part 2.3).
- ☐ All outside services and their status links still correct (Part 1.7).
- ☐ Subscriber sign-up still works.
- ☐ Templates still sound like us.
- ☐ All incident action items from last month are done.
- ☐ Change log updated (Part 0).

---

## PART 18. FINAL READINESS CHECKLIST (GO / NO-GO)

Answer **Yes** or **No**. Any 🔴 **No** means **do not launch** until fixed.

### Before launch (Phase 2 to Phase 3)

| # | Question | Level | Yes | No |
|---|---|---|---|---|
| 1 | Every 🔴 MUST question in this file has a real answer (no blanks, no TBD)? | 🔴 | ☐ | ☐ |
| 2 | Status page is hosted separately from the product? | 🔴 | ☐ | ☐ |
| 3 | At least two people have admin access? | 🔴 | ☐ | ☐ |
| 4 | Every role in Part 4 has a primary and a backup, who both know it? | 🔴 | ☐ | ☐ |
| 5 | The human-approval rule (Part 7) is written down and understood? | 🔴 | ☐ | ☐ |
| 6 | Severity table is customized with examples from our product (Part 3.2)? | 🔴 | ☐ | ☐ |
| 7 | All templates in Part 10 are filled with our real product names? | 🔴 | ☐ | ☐ |
| 8 | Backup channel for when the status page is down is tested? | 🔴 | ☐ | ☐ |
| 9 | At least one practice drill is complete, and fixes are done? | 🔴 | ☐ | ☐ |
| 10 | Legal and privacy review of Part 15 is done? | 🔴 | ☐ | ☐ |
| 11 | Status page link is in the product, help center, and support replies? | 🟡 | ☐ | ☐ |
| 12 | Subscribers can join and leave correctly? | 🟡 | ☐ | ☐ |
| 13 | Launch-week on-call schedule exists? | 🟡 | ☐ | ☐ |

### Before 500 customers (Phase 6 exit)

| # | Question | Yes | No |
|---|---|---|---|
| 1 | At least one drill per quarter has been run? | ☐ | ☐ |
| 2 | All Sev1 and Sev2 incidents have completed reports? | ☐ | ☐ |
| 3 | Every action item from reports is closed or has a new date? | ☐ | ☐ |
| 4 | Metrics in Part 13 are tracked and reviewed monthly? | ☐ | ☐ |
| 5 | Every role has a trained backup? | ☐ | ☐ |
| 6 | Lessons are sent back to improve the master template? | ☐ | ☐ |

### Sign-off

| Role | Name | Date | Signature (type name) |
|---|---|---|---|
| Document owner | ANSWER: | | |
| Approver | | | |
| Project Manager | | | |
| Privacy / legal reviewer | | | |

---

## APPENDIX A. SIMPLE WORD LIST (GLOSSARY)

| Word | Plain meaning |
|---|---|
| **Status page** | A public web page that says whether your product works. |
| **Incident** | Any problem that hurts or could hurt customers. |
| **Outage** | The product (or a part) does not work. |
| **Degraded** | It works, but badly (slow, some errors). |
| **Component** | One part of your product shown separately on the status page. |
| **Severity (Sev1-Sev4)** | How serious a problem is. Sev1 is the worst. |
| **Incident Lead** | The person running the response. |
| **Communications Lead** | The person writing customer messages. |
| **Approver** | The human who says "OK to publish". |
| **On-call** | The person who must respond if an alarm rings. |
| **Workaround** | A temporary way for customers to get things done. |
| **Postmortem / post-incident report** | A written look-back at what happened and how to prevent it. |
| **SLA** | A written promise about uptime and what you give if you miss it. |
| **Uptime** | The share of time your product works. |
| **Maintenance** | Planned work that may cause downtime. |
| **Subscriber** | A customer who gets status updates automatically. |
| **VIP / key customer** | A customer you inform personally. |
| **Single source of truth** | The one place (the status page) all other messages must match. |
| **Runbook** | A step-by-step guide for fixing a known problem. |
| **Drill** | A practice incident. |
| **AI agent** | An AI program that can draft or do tasks. Humans stay in charge. |

## APPENDIX B. COMMON MISTAKES (AND HOW THIS TEMPLATE PREVENTS THEM)

| Mistake | What goes wrong | Where this template fixes it |
|---|---|---|
| Staying silent until the cause is known | Customers panic and flood support | Part 3.3, Template A |
| Status page on the same server as the product | Page dies with the product | Part 2.1 |
| Updates promised but not delivered | Trust drops | Part 5.1, Part 9 |
| Nobody knows who can publish | Delays, or conflicting messages | Part 4, Part 7 |
| AI posts a wrong fact | Public embarrassment | Part 7 |
| Different words on different channels | Confusion | Part 2.4, Part 5.1 |
| Blaming a vendor or a person | Looks unprofessional | Part 5.1 |
| Skipping practice | Plan fails when needed | Part 16 |
| One person does everything | Burnout; single point of failure | Part 4.2 |
| Forgetting legal deadlines for data leaks | Fines and lost trust | Part 15 |
| Never reviewing the document | It goes out of date | Part 17 |

## APPENDIX C. SOURCES CONSULTED WHEN DESIGNING THIS TEMPLATE

This template follows widely used incident-communication practice. Titles and links from the research pass:

- [Atlassian: Incident management for high-velocity teams (incident communication)](https://www.atlassian.com/incident-management/tutorials/incident-communication)
- [Atlassian: Incident communication templates](https://www.atlassian.com/incident-management/incident-communication/templates)
- [Atlassian Statuspage: Incident template library](https://support.atlassian.com/statuspage/docs/incident-template-library/)
- [incident.io: Incident communication best practices](https://incident.io/blog/incident-communication-best-practices)
- [Rootly: How to build an incident response communication plan](https://rootly.com/incident-communications.md)
- [PostHog Handbook: Communication templates for incidents](https://posthog.com/handbook/growth/sales/communications-templates-incidents.md)
- [OpenStatus: Incident communication guide](https://www.openstatus.dev/guides/incident-communication)
- [UptimeRobot: Incident communication guide](https://uptimerobot.com/knowledge-hub/observability/incident-communication-guide/)
- [Inventive HQ: Incident communication plan templates](https://inventivehq.com/blog/incident-communication-plan-templates)

> Review the sources periodically. Practices and tools change.

---

**END OF DOCUMENT.** If every 🔴 question is answered and Part 18 is ticked, you are ready.
