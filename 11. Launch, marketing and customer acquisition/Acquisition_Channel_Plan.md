<!--
TEMPLATE: Acquisition_Channel_Plan.md
TEMPLATE VERSION: 1.0.0
FOLDER: Launch, Marketing and Customer Acquisition/
SCOPE: From the first line of code to the first 500 customers who actually use the product.
REUSE RULE: Copy this file for each project. Never edit the master. Replace every {{PLACEHOLDER}}.
-->

---
doc_type: acquisition_channel_plan
template_version: 1.0.0
project_name: "{{PROJECT_NAME}}"
project_id: "{{PROJECT_ID}}"
document_owner: "{{OWNER_NAME}}"
product_type: "{{B2C | B2B_SaaS | Marketplace | DevTool_API}}"   # pick ONE (see Section 1)
current_phase: "{{0_PreLaunch | 1_SoftLaunch | 2_EarlyTraction | 3_Growth | 4_Milestone}}"
status: "{{Draft | In Review | Approved | Live | Archived}}"
last_updated: "{{YYYY-MM-DD}}"
ai_agent_mode: "{{Human_Only | AI_Drafts_Human_Approves | AI_Runs_Human_Monitors}}"
target_customers: 500
---

# HOW TO FILL THIS DOCUMENT (READ THIS FIRST — 5 MINUTES)

## What is this document?
This is the **plan for how people will find your product and become real users**, from the day you start building until **500 customers are actually using it**. A "channel" is simply a *place where you meet your future customers* (for example: Google search, Instagram, a friend's newsletter, a community forum, an email to your contact list).

## Who can fill it?
Anyone. If you can answer questions like "Who is this for?" and "Where do they hang out online?", you can fill this in. You do not need marketing experience.

## The 12 rules (follow these and you cannot go wrong)

1. **Work top to bottom.** Sections are in the order you need them. Don't skip ahead.
2. **Replace every `{{LIKE_THIS}}`.** Anything inside double curly braces is a blank to fill. Delete the braces when you're done.
3. **Answer on the `ANSWER:` lines.** Each question has an `ANSWER:` line or a table to fill. Write below it, not above it.
4. **Choose by changing `[ ]` into `[x]`.** Only tick what is true today, not what you hope will be true.
5. **Use the example as a guide, never as an answer.** Examples are labelled `EXAMPLE:`. Copy the *style*, not the words.
6. **Not sure? Use the default.** Many questions have a `DEFAULT IF UNSURE:`. Use it, then tag your answer `[ASSUMPTION]` so everyone knows it should be checked later.
7. **Never leave a blank.** If something does not apply, write `N/A — because {{reason}}`. A blank looks like you forgot; an N/A with a reason shows you thought about it.
8. **Numbers need a source.** After every number write where it came from: `(source: my estimate)`, `(source: Google Analytics)`, `(source: competitor's website)`. Never invent a number without labelling it.
9. **Tag your confidence.** Add one of these after important answers: `[FACT]` (I have proof), `[ASSUMPTION]` (my best guess), `[UNKNOWN]` (I need to find out).
10. **Each section ends with a "DONE WHEN" box.** Tick every box before moving on. If you can't tick one, write what is blocking you under `BLOCKED BY:`.
11. **Keep answers short.** One to three sentences per question is plenty. Lists are better than paragraphs.
12. **Ask for help early.** If a word is confusing, check **Appendix A (Glossary)**. If a whole section is confusing, check **Appendix C (Filled Sample)**.

## Legend (symbols used in this document)

| Symbol / Tag | Meaning |
|---|---|
| `{{BLANK}}` | You must fill this in |
| `ANSWER:` | Write your answer on the next line |
| `[ ]` / `[x]` | Not chosen / chosen |
| `EXAMPLE:` | A sample answer, for guidance only |
| `DEFAULT IF UNSURE:` | A safe starting value you can use |
| `WHY THIS MATTERS:` | One sentence on why we ask |
| `DONE WHEN:` | The checklist that proves the section is finished |
| `[FACT]` `[ASSUMPTION]` `[UNKNOWN]` | How sure you are |
| `🤖` | A note aimed at AI agents (humans may skip) |
| `👤 HUMAN GATE` | A human must approve before work continues |

## How long will it take?

| Version | Time | When to use |
|---|---|---|
| Fast pass (answer only the `★` questions) | ~1 hour | You need a first draft today |
| Full pass (answer everything) | ~3–4 hours | Normal projects |
| Full pass + review | ~1 day | Big launches or paid-ads budgets above {{$5,000}} |

Questions marked `★` are **required**. The rest are strongly recommended.

## How the document is used over time
- **Fill Sections 0–16 before you start building** (a rough version is fine).
- **Update Section 9 (Phase Plan), Section 12 (Experiment Log), and Section 15 (Weekly Review) every week.**
- **Re-approve (Section 17) whenever you change a goal, a budget, or add/remove a channel.**

---

# 🤖 AI AGENT OPERATING INSTRUCTIONS

> Humans may skip this block. AI agents MUST read it fully before editing any other section.

## Role
You are the **Acquisition Planning Agent**. You help humans complete, update, and execute this plan. You do not own decisions that involve money, legal risk, or public messaging; those require a human gate.

## Hard rules
1. **Do not guess.** If a required (`★`) answer is missing, ask the human a single clear question. Do not fabricate numbers, customer quotes, competitor data, or benchmarks.
2. **Label everything.** Every number gets a source and a tag: `[FACT]`, `[ASSUMPTION]`, or `[UNKNOWN]`.
3. **Stay in your lane.** Edit only the sections you are told to. Never edit Section 17 (Approvals) — only humans sign there.
4. **Respect human gates.** Any action marked `👤 HUMAN GATE` (spending money, publishing publicly, sending bulk messages, collecting personal data) must wait for explicit written approval.
5. **Stop on red flags.** If a legal/compliance risk in Section 14 is rated High and not mitigated, stop and escalate.
6. **Preserve structure.** Don't rename headings, remove questions, or reorder sections. Add content only in answer areas.
7. **Log your work.** Every change gets a line in Section 17 (Change Log): date, section, what changed, why.
8. **Prefer small tests.** Recommend the cheapest experiment that can answer the question.

## Inputs agents should read (if they exist)
`PRD / product spec` · `User research notes` · `Brand guidelines` · `Pricing page` · `Analytics dashboard` · `Competitor notes` · `Previous version of this plan`

## Outputs agents must produce
Completed sections · A list of open questions for humans · Updated experiment log · Weekly summary (Section 15 format)

## AI-Driven Development Life Cycle (AIDLC) handoff map

| AIDLC Stage | What the product team does | What THIS document provides | Agent output to hand to the next stage |
|---|---|---|---|
| 1. Discover | Define problem, customer, market | Sections 1–4 | Customer profile + channel long list |
| 2. Specify | Write requirements | Sections 5, 7, 8 | Channel shortlist + messaging + funnel definitions → feeds PRD "acquisition requirements" (e.g., share buttons, referral codes, SEO pages) |
| 3. Design | UX, architecture | Sections 6, 11 | Landing-page requirements, tracking plan, event names |
| 4. Build | Code with AI assistance | Sections 11, 13 | Tracking implemented, landing pages and onboarding built |
| 5. Test | QA, security, privacy | Sections 14, 16 | Passed pre-launch checklist, tracking verified |
| 6. Launch | Release to users | Sections 9 (Phase 1), 10, 12 | Live campaigns, first-10 customers |
| 7. Learn & Scale | Measure, iterate | Sections 9 (Phases 2–4), 12, 15 | Weekly reports, scale/kill decisions, 500-customer milestone report |

---

# SECTION 0 — DOCUMENT CONTROL ★

**WHY THIS MATTERS:** So anyone opening this file knows whose it is, how fresh it is, and what it covers.

| Field | ANSWER |
|---|---|
| Project name ★ | {{PROJECT_NAME}} |
| One-line description ★ | {{What it is, in under 15 words}} |
| Document owner (one person) ★ | {{NAME}} |
| Backup owner | {{NAME}} |
| Contributors | {{NAMES}} |
| Planned build start date | {{YYYY-MM-DD}} |
| Planned launch date | {{YYYY-MM-DD}} |
| Target date for 500th customer | {{YYYY-MM-DD}} |
| Link to product spec / PRD | {{URL or N/A — because ...}} |
| Link to analytics dashboard | {{URL or "Not created yet"}} |
| Link to project board | {{URL or N/A — because ...}} |

**DONE WHEN:**
- [ ] Every row has an answer or an N/A with reason
- [ ] There is exactly **one** document owner

---

# SECTION 1 — YOUR PRODUCT IN PLAIN WORDS ★

**WHY THIS MATTERS:** Every channel decision depends on what you sell and how people buy it.

### Q1.1 ★ What type of product is it? (tick ONE main type)
- [ ] **B2C** — Individuals use or buy it (apps, consumer sites)
- [ ] **B2B SaaS** — Companies/teams buy it (trials, demos, invoices)
- [ ] **Marketplace** — Needs two groups (e.g., sellers AND buyers)
- [ ] **Developer tool / API** — Developers adopt it (docs, code, communities)

> Marketplace? Also fill the "Side A / Side B" columns wherever tables ask for them.
> Mixed product? Pick the type that brings the money, and note the other in the next line.

ANSWER (extra notes): {{...}}

### Q1.2 ★ What problem does it solve, in one sentence?
EXAMPLE: *"Busy parents can't plan healthy weekly dinners without spending an hour."*
ANSWER: {{...}}

### Q1.3 ★ What is the single best thing a new user can do in your product? (This is the "aha moment".)
EXAMPLE: *"Gets a full weekly meal plan in under 2 minutes."*
ANSWER: {{...}}

### Q1.4 ★ How do people pay (or what do they give you)?
- [ ] Free forever  - [ ] Free trial then paid  - [ ] Freemium (free + paid upgrade)
- [ ] One-time purchase  - [ ] Subscription  - [ ] Usage-based  - [ ] Commission/fees (marketplace)
- [ ] Other: {{...}}

Price (if known): {{$ per month / per use / per transaction}} (source: {{...}}) `[FACT | ASSUMPTION]`

### Q1.5 What are 3 alternatives people use today (including "do nothing" or spreadsheets)?
| # | Alternative | Why people choose it | Why they might switch |
|---|---|---|---|
| 1 | {{...}} | {{...}} | {{...}} |
| 2 | {{...}} | {{...}} | {{...}} |
| 3 | {{...}} | {{...}} | {{...}} |

### Q1.6 What stage is the product in right now? ★
- [ ] Idea only  - [ ] Designs/prototype  - [ ] Building  - [ ] Working beta  - [ ] Already launched

**DONE WHEN:**
- [ ] A stranger could read Q1.2–Q1.3 and understand the product
- [ ] Product type is ticked
- [ ] Payment model is ticked

---

# SECTION 2 — YOUR GOAL: 500 REAL CUSTOMERS ★

**WHY THIS MATTERS:** "500 customers" means nothing until you define what a *customer* is. This section removes the guesswork.

### Q2.1 ★ What counts as ONE "customer" for this plan? (tick ONE — this is your official definition)
- [ ] **Signed up** (created an account) — weakest, not recommended alone
- [ ] **Activated** (reached the "aha moment" from Q1.3) — **recommended default for free products**
- [ ] **Paid** (made a first payment) — **recommended default for paid products**
- [ ] **Active** (used it at least {{3}} times in {{14}} days)
- [ ] Other: {{...}}

DEFAULT IF UNSURE: *Activated* for free/freemium, *Paid* for paid products.

> For marketplaces: count **Side A customers** and **Side B customers** separately (see Q2.3).

### Q2.2 ★ Goal and deadline
| Item | ANSWER |
|---|---|
| Customer goal | 500 |
| Customer definition (from Q2.1) | {{...}} |
| Deadline | {{YYYY-MM-DD}} (source: {{...}}) |
| Minimum acceptable result (if things go badly) | {{e.g., 250 by deadline}} |
| Stretch result | {{e.g., 750}} |

### Q2.3 Marketplace split (skip if not a marketplace → write `N/A — not a marketplace`)
| | Side A ({{e.g., sellers}}) | Side B ({{e.g., buyers}}) |
|---|---|---|
| Customers needed of 500 | {{...}} | {{...}} |
| Which side do we get first? | {{...}} | {{...}} |
| Why? | {{...}} | {{...}} |

### Q2.4 ★ Why 500? What happens at 500?
EXAMPLE: *"500 users gives enough data to price properly and justifies seed funding conversations."*
ANSWER: {{...}}

### Q2.5 ★ What are the top 3 success numbers (besides customer count)?
| Metric | Target | Source of target |
|---|---|---|
| Cost to get one customer (CAC) | ≤ {{$...}} | {{...}} |
| % of signups who become customers (activation rate) | ≥ {{...%}} | {{...}} |
| % still using after 30 days (retention) | ≥ {{...%}} | {{...}} |

DEFAULT IF UNSURE: CAC ≤ one-third of what a customer pays you in their lifetime. Activation ≥ 30% `[ASSUMPTION]`. 30-day retention ≥ 20% `[ASSUMPTION]`.

**DONE WHEN:**
- [ ] "Customer" is defined by one tick in Q2.1
- [ ] Goal has a date
- [ ] Every number has a source or `[ASSUMPTION]` tag

---

# SECTION 3 — WHO ARE THE CUSTOMERS? ★

**WHY THIS MATTERS:** You can't choose the right channel until you know exactly who you're talking to.

### Q3.1 ★ Describe your #1 customer (the "Ideal Customer Profile")
Fill one table per customer type (copy the table for a second type; marketplaces need two).

| Question | ANSWER |
|---|---|
| Job title or role (B2B) / life situation (B2C) ★ | {{...}} |
| Age range / company size ★ | {{...}} |
| Country / language ★ | {{...}} |
| What problem keeps them up at night? ★ | {{...}} |
| What do they do today to solve it? | {{...}} |
| What would make them say "I need this now"? (the trigger) | {{...}} |
| Who decides / who pays? (B2B: user vs buyer) | {{...}} |
| Budget they can spend | {{...}} |
| Tools/apps they already use | {{...}} |
| Websites, creators, newsletters, communities they follow ★ | {{...}} |
| What would stop them from trying you? (objections) ★ | {{...}} |

EXAMPLE: *"Maya, 34, working parent in Canada. Spends Sunday night stressed about meals. Follows 'Budget Bytes' on Instagram. Worries the plans will be too complicated."*

### Q3.2 ★ Have you talked to real people from this group?
- [ ] Yes, {{number}} people `[FACT]`  - [ ] Not yet — plan to talk to {{number}} by {{date}}
DEFAULT IF UNSURE: Talk to 10 people before spending any money.

What did they say, in their own words? (paste 3 quotes — never invent quotes)
1. "{{...}}"
2. "{{...}}"
3. "{{...}}"

### Q3.3 Who is NOT your customer? (This stops wasted ad spend.)
ANSWER: {{...}}

**DONE WHEN:**
- [ ] The profile names a specific person type (not "everyone")
- [ ] At least 3 places they spend time are listed
- [ ] Either real quotes are pasted OR a customer-conversation plan is written

---

# SECTION 4 — WHERE DO YOUR CUSTOMERS HANG OUT? (CHANNEL DISCOVERY) ★

**WHY THIS MATTERS:** A channel is a place where your customers already are. Start by listing all possible places, then narrow down in Section 5.

### Q4.1 ★ Tick every channel that *could* reach your customer (the "long list")

**Free / organic**
- [ ] Search engines (SEO — blog, how-to pages, comparison pages)
- [ ] Social media — organic posting: {{Instagram / TikTok / X / LinkedIn / YouTube / Reddit / Facebook / other}}
- [ ] Communities & forums (Reddit, Discord, Slack groups, Facebook groups, Stack Overflow, Hacker News)
- [ ] Content: blog, YouTube, podcast, newsletter
- [ ] App store / marketplace listing optimization (ASO)
- [ ] Product directories (Product Hunt, G2, Capterra, AlternativeTo, GitHub topics)
- [ ] Open source / GitHub / developer docs / SDKs (DevTools)
- [ ] Referrals / word of mouth / invite-a-friend
- [ ] Your personal network and warm contacts
- [ ] Partnerships / integrations / co-marketing
- [ ] PR / press / guest articles / podcasts as a guest
- [ ] Events: webinars, meetups, conferences

**Direct outreach**
- [ ] Cold email
- [ ] LinkedIn / DM outreach
- [ ] Phone / sales calls (B2B)
- [ ] Door-to-door / local offline

**Paid**
- [ ] Search ads (Google, Bing)
- [ ] Social ads (Meta, TikTok, LinkedIn, X, Reddit)
- [ ] Influencer / creator sponsorships
- [ ] Newsletter sponsorships
- [ ] Affiliate / reseller programs
- [ ] Retargeting
- [ ] Marketplace seeding (paying or rewarding early supply or demand)

**Other:** {{...}}

### Q4.2 ★ For each channel you ticked, answer: "Have I seen my customer there?"
| Channel | Evidence customers are here | Evidence type |
|---|---|---|
| {{...}} | {{e.g., 12 posts asking for exactly this problem}} | `[FACT]` / `[ASSUMPTION]` |
| {{...}} | {{...}} | {{...}} |
| {{...}} | {{...}} | {{...}} |

**DONE WHEN:**
- [ ] At least 5 channels are ticked
- [ ] Each has evidence or an `[ASSUMPTION]` tag
- [ ] At least one free and one direct-outreach channel considered

---

# SECTION 5 — CHANNEL SCORECARD AND SELECTION ★

**WHY THIS MATTERS:** You cannot run 15 channels well. This section forces you to pick **at most 3 main channels** and decide what's left for later.

### Q5.1 ★ Score each shortlisted channel from 1 (bad) to 5 (great)

| Score question | What 5 means |
|---|---|
| **Reach** | Many of my target customers are here |
| **Fit** | My message and product format work naturally here |
| **Speed** | I can get results within 4 weeks |
| **Cost** | Cheap to test (5 = under $200 / few hours) |
| **Control** | I'm not dependent on a platform that can ban or change rules |
| **Skill** | My team already knows how to do this |

| Channel | Reach | Fit | Speed | Cost | Control | Skill | **TOTAL (max 30)** | Chosen? |
|---|---|---|---|---|---|---|---|---|
| {{...}} | | | | | | | | [ ] |
| {{...}} | | | | | | | | [ ] |
| {{...}} | | | | | | | | [ ] |
| {{...}} | | | | | | | | [ ] |
| {{...}} | | | | | | | | [ ] |
| {{...}} | | | | | | | | [ ] |

### Q5.2 ★ Select your channels (choose by total score, within the limits)

**DEFAULT IF UNSURE:** pick **1 primary + up to 2 supporting channels**, with at least one that needs no ad budget.

| Role | Channel | Why chosen (one line) |
|---|---|---|
| ★ Primary channel (gets most effort) | {{...}} | {{...}} |
| Supporting channel #1 | {{...}} | {{...}} |
| Supporting channel #2 | {{...}} | {{...}} |

### Q5.3 Channels we are NOT using now (and when we will revisit)
| Channel | Reason to wait | Revisit when |
|---|---|---|
| {{...}} | {{...}} | {{e.g., after 100 customers}} |

### Q5.4 Starter guide: which channels usually suit which product type?
`[ASSUMPTION]` — These are common starting points, not rules. Your evidence in Section 4 overrides this table.

| Product type | Often works early | Often works later |
|---|---|---|
| B2C app / site | Social content, communities, referrals, ASO, creators | Paid social, search ads, partnerships |
| B2B SaaS | Cold outreach, LinkedIn, founder-led sales, communities, integrations | SEO, webinars, paid search, partnerships |
| Marketplace | Hand-recruiting the hard side, local/niche communities, SEO pages for supply | Paid ads, referrals, partnerships |
| Developer tool / API | Docs, GitHub, Hacker News, dev communities, tutorials, example apps | SEO, conference talks, partner integrations, sponsorships |

**DONE WHEN:**
- [ ] No more than 3 channels are chosen
- [ ] Every chosen channel has a score and a reason
- [ ] The "not now" list exists

---

# SECTION 6 — CHANNEL PLAYBOOKS (ONE PER CHOSEN CHANNEL) ★

**WHY THIS MATTERS:** A channel without a plan is a hope. Copy the block below once for each channel chosen in Q5.2 (Primary, Supporting #1, Supporting #2).

---
## 6.A — Channel Playbook: {{CHANNEL_NAME}} (Primary)

| Question | ANSWER |
|---|---|
| ★ What exactly will we do here? (specific actions, not "do social media") | {{e.g., post 5 short videos per week and answer 10 Reddit questions per week}} |
| ★ How many customers do we expect from this channel? | {{number}} of 500 (source: {{...}}) `[ASSUMPTION]` |
| ★ Who is responsible? | {{NAME or AI agent name + human approver}} |
| ★ Weekly time needed | {{hours}} |
| ★ Weekly money needed | {{$}} |
| Content/assets needed | {{...}} |
| Tools needed | {{...}} |
| ★ Platform rules we must follow (check the real rules!) | {{...}} |
| ★ Which phases is it used in? | [ ] 1 Soft launch  [ ] 2 Early traction  [ ] 3 Growth  [ ] 4 Milestone |
| ★ The "kill rule" (when we stop) | {{e.g., if after 4 weeks and $300 we have 0 signups, stop}} |
| ★ The "scale rule" (when we do more) | {{e.g., if cost per customer ≤ $X for 2 weeks, double budget}} |
| First experiment (see Section 12) | {{experiment ID}} |
| Biggest risk | {{...}} |

**Messages for this channel** (what you will actually say; one example per format):
- Headline / hook: {{...}}
- Call to action (what we ask them to do): {{...}}
- Link destination: {{landing page URL}} with tracking tag `{{utm_source=...}}`

**Is this channel paid?** [ ] No  [ ] Yes → 👤 **HUMAN GATE:** budget approved in Section 17? [ ] Yes  [ ] No

**DONE WHEN (per channel):**
- [ ] Specific actions are written
- [ ] Owner is named
- [ ] Kill rule and scale rule both exist
- [ ] Rules of the platform were checked

---
## 6.B — Channel Playbook: {{CHANNEL_NAME}} (Supporting #1)
*(Copy the full 6.A table here.)*

---
## 6.C — Channel Playbook: {{CHANNEL_NAME}} (Supporting #2)
*(Copy the full 6.A table here, or write `N/A — only two channels chosen`.)*

---

# SECTION 7 — MESSAGE AND OFFER ★

**WHY THIS MATTERS:** The right channel with a confusing message gets zero customers.

### Q7.1 ★ Complete this sentence (the "positioning statement")
> For **{{target customer}}** who **{{has this problem}}**, **{{PRODUCT_NAME}}** is a **{{product category}}** that **{{key benefit}}**. Unlike **{{main alternative}}**, we **{{key difference}}**.

ANSWER: {{...}}

### Q7.2 ★ Your 3 key messages (each must pass the "so what?" test)
| # | Message | Proof (number, demo, quote) |
|---|---|---|
| 1 | {{...}} | {{...}} |
| 2 | {{...}} | {{...}} |
| 3 | {{...}} | {{...}} |

### Q7.3 ★ The offer (why should someone act TODAY?)
- [ ] Free trial ({{days}})  - [ ] Free plan  - [ ] Discount ({{%}}) for first customers
- [ ] Early-access / founding-member perks  - [ ] Money-back guarantee  - [ ] Bonus  - [ ] None
ANSWER (details): {{...}}

### Q7.4 ★ Landing page checklist (the place every channel sends people to)
- [ ] Headline says what it is and who it's for in under 10 words
- [ ] One clear main button
- [ ] Proof (testimonials, logos, numbers) — *real only*
- [ ] Works on a phone
- [ ] Loads in under 3 seconds
- [ ] Privacy policy and terms linked
- [ ] Tracking installed (see Section 11)

### Q7.5 Brand/tone rules
Tone: [ ] Friendly  [ ] Professional  [ ] Playful  [ ] Technical  [ ] Other: {{...}}
Words to always use: {{...}}  Words to never use: {{...}}
Link to brand guide: {{URL or N/A — because ...}}

**DONE WHEN:**
- [ ] Positioning sentence has no blanks
- [ ] Each message has proof or is tagged `[ASSUMPTION]`
- [ ] An offer is chosen (or "None" is chosen on purpose)

---

# SECTION 8 — THE CUSTOMER JOURNEY (FUNNEL) ★

**WHY THIS MATTERS:** You can only fix what you can measure. A funnel is the path from "never heard of us" to "happy customer".

### Q8.1 ★ Define each step and how you'll know someone completed it

| Step | Plain meaning | Your definition (what exact action?) | Target conversion to next step |
|---|---|---|---|
| 1. Aware | Saw us | {{e.g., visited landing page}} | {{%}} |
| 2. Interested | Wanted to know more | {{e.g., clicked "Try it"}} | {{%}} |
| 3. Signed up | Gave email/created account | {{...}} | {{%}} |
| 4. Activated | Reached the "aha moment" (Q1.3) | {{...}} | {{%}} |
| 5. Customer | Meets Q2.1 definition | {{...}} | {{%}} |
| 6. Retained | Still using after 30 days | {{...}} | {{%}} |
| 7. Referred | Told someone else | {{...}} | {{%}} |

DEFAULT IF UNSURE: Visit→Signup 3–5%, Signup→Activated 30%, Activated→Paid or Customer 10–20%. `[ASSUMPTION]` — replace with your real data after Phase 1.

### Q8.2 ★ Work backwards: how many visitors do you need for 500 customers?
`Visitors needed = 500 ÷ (Signup rate × Activation rate × Customer rate)`

| Item | ANSWER |
|---|---|
| Signup rate | {{...%}} |
| Activation rate | {{...%}} |
| Customer conversion rate | {{...%}} |
| Visitors/leads needed | {{...}} |
| Per month over {{months}} months | {{...}} |

### Q8.3 ★ Where do people drop out the most? (fill after Phase 1 data)
ANSWER: {{...}}

### Q8.4 What happens right after signup? (onboarding)
- [ ] Welcome email  - [ ] In-app guide  - [ ] Personal message from a human  - [ ] Template/sample data  - [ ] Checklist
ANSWER (the first 3 things a new user sees): {{...}}

**DONE WHEN:**
- [ ] Every step has a measurable definition
- [ ] The math in Q8.2 is done
- [ ] Onboarding is described

---

# SECTION 9 — THE 5-PHASE PLAN: FROM FIRST CODE TO 500 CUSTOMERS ★

**WHY THIS MATTERS:** Different customer counts need different actions. Each phase has *entry criteria* (ready to start?) and *exit criteria* (ready to move on?). Don't move on until exit criteria are true.

### Phase overview

| Phase | Name | Customers | AIDLC stages | Main question |
|---|---|---|---|---|
| 0 | **Pre-Launch (Build)** | 0 | Discover → Build → Test | Are we ready and is anyone waiting? |
| 1 | **Soft Launch** | 1–10 | Launch | Can we get *any* real customers and learn? |
| 2 | **Early Traction** | 11–100 | Learn & Scale | Which channel works repeatably? |
| 3 | **Growth** | 101–300 | Learn & Scale | Can we do it faster without losing quality? |
| 4 | **Milestone** | 301–500 | Learn & Scale | Can we finish and learn what's next? |

---
## PHASE 0 — PRE-LAUNCH (BUILD) · 0 customers

| Question | ANSWER |
|---|---|
| ★ Start date → end date | {{...}} → {{...}} |
| ★ Goal | Build an audience and a launch-ready product |
| ★ Waitlist/email list target | {{number, DEFAULT: 100 signups}} |
| ★ Customer conversations target | {{DEFAULT: 10}} |
| Pre-launch actions (tick and describe) | [ ] Landing page + waitlist  [ ] "Build in public" posts  [ ] Interview customers  [ ] Beta testers  [ ] Partner conversations  [ ] Content stockpile  [ ] Other |
| Product work that supports acquisition | [ ] Tracking built  [ ] Referral/share feature  [ ] Onboarding flow  [ ] SEO pages  [ ] Docs/tutorials (DevTools)  [ ] Supply seeded (Marketplace) |

**EXIT CRITERIA — move to Phase 1 only when ALL are ticked:**
- [ ] Product's core flow works end to end (a stranger can reach the "aha moment")
- [ ] Tracking verified (Section 11 checklist passed)
- [ ] Landing page live and passes Q7.4
- [ ] Waitlist/beta list has ≥ {{target}} people (or `N/A — because ...`)
- [ ] Pre-launch checklist (Section 16) is ≥ 90% ticked
- [ ] 👤 **HUMAN GATE:** launch approval signed in Section 17

🤖 *Agent tasks in this phase:* draft channel playbooks, landing-page copy, tracking plan, interview scripts, content calendar. *Humans approve all public-facing copy.*

---
## PHASE 1 — SOFT LAUNCH · customers 1–10

| Question | ANSWER |
|---|---|
| ★ Start → end date | {{...}} → {{...}} |
| ★ Goal | Get 10 real customers and learn *why* they came |
| ★ Channels used | {{usually: warm network + 1 primary channel}} |
| ★ How will we personally help each customer? | {{e.g., founder emails each new user within 1 hour}} |
| Budget cap | {{$ — DEFAULT: $0–$300}} |
| What we're learning | {{e.g., what words they use, what confuses them, what they'd pay}} |

**EXIT CRITERIA:**
- [ ] ≥ 10 customers meeting the Q2.1 definition `[FACT]`
- [ ] We talked to ≥ 5 of them and wrote down why they chose us
- [ ] Top 3 problems found and logged (bugs, confusion, missing features)
- [ ] At least 1 channel brought ≥ 3 customers

🤖 *Agent tasks:* summarize feedback, tag customers by source, propose next experiments. *Do not send mass messages without 👤 approval.*

---
## PHASE 2 — EARLY TRACTION · customers 11–100

| Question | ANSWER |
|---|---|
| ★ Start → end date | {{...}} → {{...}} |
| ★ Goal | Find the 1–2 channels that work repeatedly |
| ★ Weekly new-customer target | {{DEFAULT: 5–10}} |
| ★ Experiments per week | {{DEFAULT: 2 small tests}} |
| Budget cap | {{$}} |
| Referral/word-of-mouth tactic | {{e.g., invite link with reward}} |

**EXIT CRITERIA:**
- [ ] ≥ 100 customers `[FACT]`
- [ ] ≥ 1 channel produced customers in 3 different weeks in a row
- [ ] CAC known for each paid/effort channel (Section 10)
- [ ] 30-day retention measured on at least the first 30 customers
- [ ] Funnel drop-off point identified (Q8.3)

---
## PHASE 3 — GROWTH · customers 101–300

| Question | ANSWER |
|---|---|
| ★ Start → end date | {{...}} → {{...}} |
| ★ Goal | Scale what works; add one new channel carefully |
| ★ Weekly new-customer target | {{DEFAULT: 15–25}} |
| ★ Which channel gets more investment? | {{...}} |
| New channel to test (max 1) | {{...}} |
| Support plan (can we serve this many?) | {{...}} |

**EXIT CRITERIA:**
- [ ] ≥ 300 customers `[FACT]`
- [ ] CAC within target (Q2.5) for the main channel
- [ ] Support/response times still within promise
- [ ] No unresolved High-rated risk in Section 14

---
## PHASE 4 — MILESTONE · customers 301–500

| Question | ANSWER |
|---|---|
| ★ Start → end date | {{...}} → {{...}} |
| ★ Goal | Reach 500 customers and document what we learned |
| ★ Weekly new-customer target | {{DEFAULT: 25–40}} |
| ★ Post-500 plan | [ ] Keep growing same channels  [ ] Raise prices  [ ] Open new market  [ ] Pause and fix retention  [ ] Raise funding  [ ] Other |

**EXIT CRITERIA (project complete):**
- [ ] 500th customer reached and verified `[FACT]` on {{date}}
- [ ] Final report written (template in Section 15.C)
- [ ] Lessons moved into the next project's copy of this template
- [ ] 👤 **HUMAN GATE:** sign-off in Section 17

**DONE WHEN (Section 9):**
- [ ] All five phases have dates, goals, and exit criteria
- [ ] Every phase budget fits the total in Section 10

---

# SECTION 10 — BUDGET AND UNIT ECONOMICS ★

**WHY THIS MATTERS:** It stops you from spending more to get a customer than the customer is worth.

### Q10.1 ★ Total budget
| Item | ANSWER |
|---|---|
| Total money for acquisition until 500 customers | {{$}} |
| Money reserved for experiments (DEFAULT: 20% of total) | {{$}} |
| Money reserved for emergencies (DEFAULT: 10%) | {{$}} |
| Team time available (hours/week) | {{...}} |
| Currency | {{USD / other}} |

### Q10.2 ★ Budget by phase and channel

| Phase | Channel | Planned spend | Planned hours | Expected customers | Expected cost per customer |
|---|---|---|---|---|---|
| 0 | {{...}} | {{$}} | {{...}} | {{...}} | {{...}} |
| 1 | {{...}} | {{$}} | {{...}} | {{...}} | {{...}} |
| 2 | {{...}} | {{$}} | {{...}} | {{...}} | {{...}} |
| 3 | {{...}} | {{$}} | {{...}} | {{...}} | {{...}} |
| 4 | {{...}} | {{$}} | {{...}} | {{...}} | {{...}} |
| **Total** | | **{{$}}** | **{{...}}** | **500** | **{{...}}** |

### Q10.3 ★ Unit economics (how much is a customer worth?)

| Number | How to calculate | Your number | Source |
|---|---|---|---|
| Average revenue per customer per month (ARPU) | total revenue ÷ customers | {{$}} | {{...}} |
| Gross margin (what's left after costs of serving) | (revenue − cost to serve) ÷ revenue | {{%}} | {{...}} |
| Expected months a customer stays | 1 ÷ monthly churn rate | {{...}} | {{...}} |
| **Customer lifetime value (LTV)** | ARPU × gross margin × months | {{$}} | calculated |
| **Customer acquisition cost (CAC)** | total acquisition spend ÷ new customers | {{$}} | calculated |
| **LTV ÷ CAC** | | {{...}} | calculated |
| **Payback time** | CAC ÷ (ARPU × gross margin) | {{months}} | calculated |

DEFAULT IF UNSURE: Aim for LTV ÷ CAC ≥ 3 and payback ≤ 12 months. `[ASSUMPTION]` Free products: replace "revenue" with the value of an activated user (e.g., future conversion rate × price) and label it clearly `[ASSUMPTION]`.

### Q10.4 ★ Spending rules (money safety)
- [ ] No single test spends more than {{DEFAULT: 10% of experiment budget}} before a human reviews results
- [ ] Any new paid channel needs 👤 approval
- [ ] Stop all paid spend if CAC is above {{2× target}} for {{7}} days
- [ ] Daily spending caps set inside every ad platform

**DONE WHEN:**
- [ ] Budget table adds up to the total
- [ ] LTV ÷ CAC is calculated (or `N/A — because ...`)
- [ ] Spending rules are ticked

---

# SECTION 11 — TRACKING AND ANALYTICS SETUP ★

**WHY THIS MATTERS:** If you can't see where customers come from, you can't tell which channel is working.

### Q11.1 ★ Tools (tick what you will use)
- [ ] Web analytics: {{GA4 / Plausible / PostHog / Mixpanel / other}}
- [ ] Product analytics: {{...}}
- [ ] Tag manager: {{...}}
- [ ] Email tool: {{...}}
- [ ] CRM or customer sheet: {{...}}
- [ ] Ad platform pixels: {{...}}
- [ ] Dashboard: {{Looker Studio / Metabase / spreadsheet / other}}
- [ ] "How did you hear about us?" question at signup

### Q11.2 ★ Link naming rule (UTM tags). Use the same format every time, lowercase, no spaces.

`https://yoursite.com/?utm_source={{channel}}&utm_medium={{type}}&utm_campaign={{name}}&utm_content={{variant}}`

| Part | Rule | EXAMPLE |
|---|---|---|
| utm_source | Where the link lives | `reddit`, `linkedin`, `newsletter-xyz` |
| utm_medium | Type | `organic`, `cpc`, `email`, `referral`, `influencer` |
| utm_campaign | Plan/phase + purpose | `p1-launch`, `p2-webinar` |
| utm_content | Which version | `video-a`, `headline-b` |

### Q11.3 ★ Events to track (name them once, use forever)

| Funnel step (Section 8) | Event name | Fires when | Properties to save | Built? |
|---|---|---|---|---|
| Aware | `page_view` | Landing page loads | source, campaign | [ ] |
| Interested | `cta_click` | Main button clicked | button_id | [ ] |
| Signed up | `signup_completed` | Account created | method, source | [ ] |
| Activated | `{{aha_event}}` | {{...}} | {{...}} | [ ] |
| Customer | `{{customer_event}}` | {{...}} | plan, amount | [ ] |
| Retained | `returned_day_30` | Active again after 30 days | — | [ ] |
| Referred | `invite_sent` | Invite link used | channel | [ ] |

### Q11.4 ★ Dashboard — which numbers must be visible in one place?
- [ ] Visitors by channel  - [ ] Signups by channel  - [ ] Customers by channel  - [ ] Cost per customer by channel
- [ ] Funnel conversion by step  - [ ] 30-day retention  - [ ] Total customers vs. 500 goal  - [ ] Spend vs. budget

Dashboard link: {{URL}}

### Q11.5 Privacy and consent for tracking
- [ ] Cookie/consent banner (if required in your markets)  - [ ] Privacy policy describes tracking
- [ ] No sensitive personal data in analytics  - [ ] Data deletion process exists

**DONE WHEN:**
- [ ] A test signup travelled through every event and showed up on the dashboard
- [ ] UTM rule is shared with everyone who posts links
- [ ] Privacy items are ticked

🤖 *Agent rule: never log or store customer personal data in this document. Use counts and anonymous IDs only.*

---

# SECTION 12 — EXPERIMENT LOG AND DECISION RULES ★

**WHY THIS MATTERS:** Acquisition is learning by testing. This log shows what was tried, what happened, and what to do next, so nobody repeats mistakes.

### Q12.1 ★ The rules (agree on these BEFORE you test)

| Rule | ANSWER |
|---|---|
| Max experiments running at once | {{DEFAULT: 3}} |
| Minimum test length | {{DEFAULT: 2 weeks or 100 visitors, whichever comes later}} |
| What counts as "winner" | {{e.g., cost per customer ≥ 30% better than baseline}} |
| What counts as "loser" | {{e.g., 0 signups after spending the test budget}} |
| What if it's unclear | Extend once by {{1 week}}, then decide |
| Who decides | {{NAME}} |

### Q12.2 ★ Experiment log (add one row per test; never delete rows)

| ID | Date start–end | Phase | Channel | Hypothesis ("If we … then … because …") | Cost | Result number | Decision | What we learned |
|---|---|---|---|---|---|---|---|---|
| E-001 | {{...}} | {{...}} | {{...}} | {{...}} | {{$}} | {{...}} | [ ] Scale [ ] Kill [ ] Retest | {{...}} |
| E-002 | | | | | | | [ ] Scale [ ] Kill [ ] Retest | |
| E-003 | | | | | | | [ ] Scale [ ] Kill [ ] Retest | |

EXAMPLE: *E-001 · If we post a 30-second demo video on TikTok 5×/week, then we will get 50 signups in 3 weeks, because our audience watches short how-tos.*

### Q12.3 Idea backlog (not yet scheduled)
| Idea | Expected impact (H/M/L) | Effort (H/M/L) | Channel |
|---|---|---|---|
| {{...}} | | | |

**DONE WHEN:**
- [ ] Rules are agreed before the first test
- [ ] First experiment is logged with a hypothesis and a stop rule

---

# SECTION 13 — TEAM, TOOLS AND AI-AGENT RESPONSIBILITIES ★

**WHY THIS MATTERS:** Work with no owner doesn't get done.

### Q13.1 ★ Who does what? (R = does the work, A = approves, C = consulted, I = informed)

| Task | Human owner | AI agent (if any) | R | A | C | I |
|---|---|---|---|---|---|---|
| Customer interviews | {{...}} | Summarize notes | | | | |
| Landing page copy | {{...}} | Draft | | | | |
| Content creation | {{...}} | Draft | | | | |
| Posting / publishing | {{...}} | Schedule only after approval | | | | |
| Outreach messages | {{...}} | Draft | | | | |
| Paid ads setup | {{...}} | Suggest; no spend | | | | |
| Tracking & dashboard | {{...}} | Build report | | | | |
| Weekly review | {{...}} | Prepare summary | | | | |
| Customer support | {{...}} | Draft replies | | | | |
| Legal/privacy check | {{...}} | Flag only | | | | |

### Q13.2 ★ What can the AI agent do WITHOUT asking? What needs approval?

| Action | AI may do alone | Needs 👤 approval |
|---|---|---|
| Draft text, plans, reports | [ ] | [ ] |
| Analyze data and recommend | [ ] | [ ] |
| Publish public posts | [ ] | [ ] |
| Send emails/DMs to customers or prospects | [ ] | [ ] |
| Spend money or change budgets | [ ] | [ ] |
| Change tracking or website code | [ ] | [ ] |
| Collect or store personal data | [ ] | [ ] |

DEFAULT IF UNSURE: Tick "Needs approval" for everything except drafting and analysis.

### Q13.3 Tools list
| Purpose | Tool | Owner | Cost/month |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{$}} |

**DONE WHEN:**
- [ ] Every task has a human name next to it
- [ ] AI permissions are ticked

---

# SECTION 14 — RISKS, LEGAL AND COMPLIANCE ★

**WHY THIS MATTERS:** One banned account or one legal complaint can end your launch. This is a planning aid, **not legal advice**; ask a qualified professional for anything uncertain.

### Q14.1 ★ Compliance checklist (tick what applies, then confirm it's handled)

| Area | Applies? | Handled? | Notes |
|---|---|---|---|
| Privacy laws for your customers' regions (e.g., GDPR, UK GDPR, CCPA/CPRA, others) | [ ] Yes [ ] No [ ] Unsure | [ ] | {{...}} |
| Email/SMS rules (opt-in, unsubscribe, sender identity — e.g., CAN-SPAM, CASL, PECR, TCPA) | [ ] [ ] [ ] | [ ] | |
| Advertising rules (honest claims, disclosures, endorsements/influencer labels) | [ ] [ ] [ ] | [ ] | |
| Platform policies (each ad/social/app-store platform's rules) | [ ] [ ] [ ] | [ ] | |
| Cookies/consent banner | [ ] [ ] [ ] | [ ] | |
| Children's data (under 13/16) | [ ] [ ] [ ] | [ ] | |
| Industry rules (health, finance, education, etc.) | [ ] [ ] [ ] | [ ] | |
| Terms of Service & Privacy Policy published | [ ] [ ] [ ] | [ ] | |
| Intellectual property (images, music, trademarks, competitor names in ads) | [ ] [ ] [ ] | [ ] | |
| Accessibility of landing pages | [ ] [ ] [ ] | [ ] | |
| Testimonials are real and permission was given | [ ] [ ] [ ] | [ ] | |
| Scraping/outreach lists obtained legally | [ ] [ ] [ ] | [ ] | |
| Community/forum self-promotion rules followed | [ ] [ ] [ ] | [ ] | |

### Q14.2 ★ Risk register (rate each: Likelihood and Impact as Low / Medium / High)

| # | Risk | Likelihood | Impact | What we'll do to prevent it | What we'll do if it happens | Owner |
|---|---|---|---|---|---|---|
| R1 | Main channel changes rules or bans account | | | {{...}} | {{...}} | |
| R2 | Ads cost more than expected | | | {{...}} | {{...}} | |
| R3 | Product not ready when traffic arrives | | | {{...}} | {{...}} | |
| R4 | Tracking is broken so we're flying blind | | | {{...}} | {{...}} | |
| R5 | Customers sign up but don't activate | | | {{...}} | {{...}} | |
| R6 | Can't support customers at volume | | | {{...}} | {{...}} | |
| R7 | Negative public feedback or reviews | | | {{...}} | {{...}} | |
| R8 | Privacy or legal complaint | | | {{...}} | {{...}} | |
| R9 | Only one person knows how this works | | | {{...}} | {{...}} | |
| R10 | Marketplace: one side shows up, the other doesn't | | | {{...}} | {{...}} | |
| R11 | {{your own risk}} | | | {{...}} | {{...}} | |

**RULE:** Any risk rated **High + High** must be fixed or explicitly accepted by a human in Section 17 before Phase 1 starts.

**DONE WHEN:**
- [ ] Every row of Q14.1 has an answer
- [ ] No High/High risk is unaddressed
- [ ] A qualified person reviewed the legal items, or a note says why not: {{...}}

---

# SECTION 15 — WEEKLY REVIEW AND REPORTING ★

**WHY THIS MATTERS:** A plan nobody checks is a wish.

### 15.A Review rhythm
| Item | ANSWER |
|---|---|
| Weekly review day/time | {{e.g., Monday 10:00}} |
| Who attends | {{...}} |
| Where notes are stored | {{...}} |
| Who gets the weekly summary | {{...}} |

### 15.B Weekly report (copy this block every week)

```
WEEK OF: {{date}}      PHASE: {{0–4}}
Customers total: {{n}} / 500   (this week: +{{n}})
Visitors: {{n}}   Signups: {{n}}   Activated: {{n}}   Customers: {{n}}
Spend this week: ${{n}}   Spend total: ${{n}} / ${{budget}}
CAC this week: ${{n}}   Target: ${{n}}
Best channel this week: {{...}} ({{n}} customers)
Worst channel this week: {{...}}
Experiments finished: {{IDs and decisions}}
Experiments started: {{IDs}}
Biggest learning: {{one sentence}}
Biggest problem: {{one sentence}}
Decisions needed from humans: {{list or "none"}}
On track for 500 by deadline?  [ ] Yes  [ ] At risk  [ ] No → why: {{...}}
```

### 15.C Final report at 500 customers (fill once)
| Question | ANSWER |
|---|---|
| Date 500th customer reached | {{...}} |
| Total spend / total hours | {{...}} |
| Final CAC / LTV ÷ CAC | {{...}} |
| Customers by channel | {{...}} |
| Top 3 things that worked | {{...}} |
| Top 3 things that failed | {{...}} |
| What we would do differently | {{...}} |
| Changes to push back into the master template | {{...}} |

**DONE WHEN:**
- [ ] First weekly review is scheduled
- [ ] Report format is agreed

---

# SECTION 16 — PRE-LAUNCH READINESS CHECKLIST ★

**WHY THIS MATTERS:** A final gate before the first real customer arrives. Aim for **100% ticked** (or N/A with a reason).

### Product readiness
- [ ] A new user can reach the "aha moment" without help
- [ ] Signup, login, and (if paid) payment work on phone and desktop
- [ ] Core bugs fixed; known issues listed and accepted
- [ ] Performance tested for expected first-month traffic ({{n}} visitors)
- [ ] Support channel is live (email/chat) and someone is assigned
- [ ] Onboarding emails/messages tested

### Acquisition readiness
- [ ] Landing page passes Q7.4
- [ ] Every chosen channel has a playbook (Section 6)
- [ ] Content for the first 2 weeks is ready
- [ ] Tracking verified end-to-end (Section 11)
- [ ] Dashboard shows live data
- [ ] UTM links created and tested
- [ ] Accounts for each channel created and secured (two-factor on)

### Legal and trust
- [ ] Privacy policy and terms are live
- [ ] Consent/opt-in and unsubscribe work
- [ ] Section 14 reviewed; no unmitigated High/High risks
- [ ] Testimonials/claims are real and provable

### People and money
- [ ] Owners named for every channel (Section 13)
- [ ] Budget approved (Section 17)
- [ ] Spending caps set inside ad platforms
- [ ] Weekly review in the calendar

### Developer tools / API extras (else `N/A — not a dev tool`)
- [ ] Quick-start guide works in under 10 minutes  - [ ] Code examples tested  - [ ] API keys/self-serve signup works
- [ ] Public repo/readme/license clear  - [ ] Status page and changelog exist

### B2B extras (else `N/A — not B2B`)
- [ ] Demo or trial path works  - [ ] Pricing/contact path clear  - [ ] Security questionnaire answers ready  - [ ] Sales script or outreach sequence ready

### Marketplace extras (else `N/A — not a marketplace`)
- [ ] Enough supply seeded so first buyers see value  - [ ] Trust/safety rules and reporting exist  - [ ] Payment/payout flow tested

**Score:** {{ticked}} / {{total}} = {{%}}   → Ready for Phase 1? [ ] Yes (≥ 90%)  [ ] No — blockers: {{...}}

---

# SECTION 17 — APPROVALS, CHANGE LOG AND OPEN QUESTIONS

### 17.A Approvals (humans only — agents must not edit this table)

| Gate | What is approved | Approver | Date | Decision |
|---|---|---|---|---|
| G1 | This plan (Sections 0–16) | {{NAME}} | {{date}} | [ ] Approved [ ] Changes needed |
| G2 | Budget (Section 10) | {{NAME}} | {{date}} | [ ] Approved [ ] Changes needed |
| G3 | Risks and compliance (Section 14) | {{NAME}} | {{date}} | [ ] Approved [ ] Changes needed |
| G4 | Launch to Phase 1 | {{NAME}} | {{date}} | [ ] Approved [ ] Changes needed |
| G5 | Move to Phase 2 | {{NAME}} | {{date}} | [ ] Approved [ ] Changes needed |
| G6 | Move to Phase 3 | {{NAME}} | {{date}} | [ ] Approved [ ] Changes needed |
| G7 | Move to Phase 4 | {{NAME}} | {{date}} | [ ] Approved [ ] Changes needed |
| G8 | Project complete (500 reached) | {{NAME}} | {{date}} | [ ] Approved [ ] Changes needed |

### 17.B Open questions (anything you couldn't answer)
| # | Question | Section | Who can answer | Needed by | Status |
|---|---|---|---|---|---|
| 1 | {{...}} | {{...}} | {{...}} | {{date}} | [ ] Open [ ] Answered |

### 17.C Change log (newest at the top)
| Date | Who (human or agent name) | Section | What changed | Why |
|---|---|---|---|---|
| {{date}} | {{...}} | {{...}} | Created from template v1.0.0 | Project start |

---

# FINAL QUALITY CHECK — IS THIS DOCUMENT READY? (5 minutes)

Tick every line. If you can't, go back to that section.

**Completeness**
- [ ] No `{{...}}` left anywhere (search the file for `{{`)
- [ ] No empty answers: everything is filled or `N/A — because ...`
- [ ] All `★` questions answered
- [ ] Every "DONE WHEN" box is ticked

**Clarity ("fewer reasons to guess")**
- [ ] "Customer" is defined in exactly one place (Q2.1) and used consistently
- [ ] Every number has a source and a tag (`[FACT]`, `[ASSUMPTION]`, `[UNKNOWN]`)
- [ ] Each chosen channel has a named owner, a kill rule, and a scale rule
- [ ] A new teammate could run next week's work from this document alone

**Consistency**
- [ ] Budget in Section 10 matches channel spend in Section 6
- [ ] Funnel math (Q8.2) supports the 500-customer goal
- [ ] Phase dates fit the deadline in Q2.2
- [ ] No more than 3 channels chosen

**Safety**
- [ ] Approvals (Section 17) are signed by humans
- [ ] Paid spend has a human gate and daily caps
- [ ] No personal customer data is stored in this file

---

# APPENDIX A — GLOSSARY (PLAIN-ENGLISH)

| Word | Simple meaning |
|---|---|
| **Acquisition** | Getting new customers |
| **Channel** | A place or method to reach customers (e.g., Google search, Instagram, email) |
| **Funnel** | The steps from "never heard of us" to "happy customer" |
| **ICP (Ideal Customer Profile)** | A description of the person/company who gets the most value from your product |
| **Persona** | A made-up but realistic example of one ICP person |
| **Aha moment** | The first moment a user feels "this is useful!" |
| **Activation** | A new user reaching the aha moment |
| **Conversion rate** | Of 100 people at one step, how many reach the next step |
| **CAC (Customer Acquisition Cost)** | Money (and time value) spent to win one customer |
| **LTV (Lifetime Value)** | Total profit you expect from one customer over their time with you |
| **ARPU** | Average revenue per user (per month, unless stated) |
| **Churn** | The share of customers who leave in a period |
| **Retention** | The share of customers who stay |
| **Payback period** | How many months until a customer has paid back what you spent to win them |
| **CTR (Click-Through Rate)** | Of 100 people who saw something, how many clicked |
| **CPC / CPM** | Cost per click / cost per 1,000 views |
| **SEO** | Making your pages easy to find in search engines for free |
| **ASO** | Same idea, for app stores |
| **UTM tag** | A label added to a link so you can tell where visitors came from |
| **Attribution** | Deciding which channel deserves credit for a customer |
| **Cold outreach** | Contacting people who don't know you yet |
| **Warm network** | People who already know and trust you |
| **Landing page** | The page people arrive at after clicking; it has one goal |
| **Waitlist** | A list of people who want access when you launch |
| **Beta** | Early version shared with a small group to find problems |
| **Referral** | A customer inviting someone else |
| **Freemium** | Free basic plan, paid upgrades |
| **Marketplace (two-sided)** | A product that needs two groups (e.g., buyers and sellers) |
| **Hypothesis** | A guess you can test: "If we do X, then Y will happen because Z" |
| **Kill rule / Scale rule** | When to stop a test / when to do more of it |
| **Human gate** | A step where a person must say yes before work continues |
| **AIDLC** | AI-Driven Development Life Cycle: building and launching a product with AI agents helping at each stage |
| **PRD** | Product Requirements Document: what the product must do |
| **MVP** | Minimum viable product: the smallest version worth giving to customers |

---

# APPENDIX B — DEFAULT VALUES CHEAT SHEET (USE WHEN UNSURE, TAG `[ASSUMPTION]`)

| Question | Safe starting default |
|---|---|
| "Customer" definition | Activated (free/freemium) or Paid (paid products) |
| Number of main channels | 1 primary + up to 2 supporting |
| Customer conversations before spending | 10 |
| Waitlist target before launch | 100 |
| Experiment budget share | 20% of total |
| Emergency reserve | 10% of total |
| Min test length | 2 weeks or 100 visitors |
| Max simultaneous experiments | 3 |
| Visit → signup rate | 3–5% |
| Signup → activation rate | 30% |
| Activation → customer rate | 10–20% |
| 30-day retention target | 20% |
| LTV ÷ CAC target | ≥ 3 |
| Payback period target | ≤ 12 months |
| Phase 1 spend cap | $0–$300 |
| AI agent permissions | Draft and analyze only; everything else needs approval |

> These are starting guesses, not facts. Replace each with real data as soon as you have it.

---

# APPENDIX C — FILLED SAMPLE (FICTIONAL PRODUCT: "MealMate")

*Use this to see what a good answer looks like. Never copy these numbers.*

**Section 1:** B2C app. Problem: "Busy parents can't plan healthy weekly dinners without spending an hour." Aha moment: "Gets a full weekly meal plan in under 2 minutes." Pricing: Free plan + $6/month premium `[ASSUMPTION]`. Alternatives: Pinterest boards, spreadsheets, takeout.

**Section 2:** Customer = *Activated* (generated a first meal plan). Goal: 500 by 2027-03-31. Minimum: 250. CAC target ≤ $8 `[ASSUMPTION]`.

**Section 3:** Maya, 34, working parent, Canada. Trigger: Sunday-night stress. Follows budget-cooking creators. Objection: "Meal apps are complicated." Talked to 12 parents `[FACT]`. Quote: "I just want someone to tell me what to cook." (parent #4)

**Section 5:** Scores — Short-form video 24/30, Parenting communities 22/30, Paid social 15/30. Primary: short-form video. Supporting: parenting communities. Not now: paid social (revisit after 100 customers).

**Section 6 (Primary):** Post 5 short videos/week showing the 2-minute plan. Expect 200 of 500 customers `[ASSUMPTION]`. Weekly time 6 hours, money $0. Kill rule: if 4 weeks of posting give < 20 signups, change format or stop. Scale rule: if a video format averages ≥ 30 signups/week for 2 weeks, add 3 posts/week.

**Section 8:** Visit → signup 4%, signup → activated 35%. Visitors needed = 500 ÷ (0.04 × 0.35) ≈ 35,700 `[ASSUMPTION]`. Over 6 months ≈ 6,000/month.

**Section 9, Phase 1 exit:** 10 activated users `[FACT]`; 5 interviewed; top problems: "too many questions at signup", "can't swap a meal", "no grocery list".

**Section 12, E-001:** If we post a 30-second demo video 5×/week for 3 weeks, then we'll get 50 signups, because our audience watches how-tos. Cost: $0. Result: 38 signups → Decision: Retest with a stronger hook.

**Section 14:** High risk R1 (account ban) → mitigated by building an email list from day one.

---

# APPENDIX D — TEMPLATE MAINTENANCE (FOR THE TEMPLATE OWNER ONLY)

| Item | Rule |
|---|---|
| Master location | `Launch, Marketing and Customer Acquisition/Acquisition_Channel_Plan.md` |
| Never edit the master while filling a project copy | Copy it first and rename to `Acquisition_Channel_Plan_{{PROJECT_ID}}.md` |
| Version number | Raise the minor number for new questions (1.1.0) and the major number for structural changes (2.0.0) |
| After each project | Review the "Changes to push back into the master template" row from Section 15.C |
| Review cycle | Every 6 months, or after 10 projects, whichever comes first |
| Changes to the master | Add a row below |

| Version | Date | Change | Author |
|---|---|---|---|
| 1.0.0 | {{date}} | First release | {{...}} |

**— END OF TEMPLATE —**
