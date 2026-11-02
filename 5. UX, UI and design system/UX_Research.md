---
# MACHINE-READABLE HEADER: keep the keys, change only the values. Humans: fill these in last.
doc_type: ux_research
template_version: "1.1"
project_id: "[FILL: short-lowercase-id, e.g. plantpal]"
product_name: "[FILL]"
owner: "[FILL]"
created: "[DATE: YYYY-MM-DD]"
last_updated: "[DATE: YYYY-MM-DD]"
current_phase: "setup"   # setup | discover | define | design_build | launch_grow | learn_close
overall_status: "NOT STARTED"   # NOT STARTED | IN PROGRESS | NEEDS REVIEW | DONE
customer_goal: 500
customers_so_far: 0
customer_definition: "UNKNOWN"   # fill from Section 22
current_gate: "none"   # none | G1 | G2 | G3 | G4 | G5 | G6 | G7
blocked: false   # set true when an AI agent hits a STOP rule
blocked_reason: ""
---

# How to Fill This Document

> **Read this whole box first. It takes 3 minutes and saves hours.**

## What is this file?
This is the **single source of truth for all UX research** of ONE product, from the first idea to your first **500 customers**. Copy this file into a new project, fill it in from top to bottom, and keep it updated. Everything lives in this one file. You never need another document to complete it.

## Who is it for?
- **You** (founder, designer, developer, or beginner).
- **AI agents** that help you build. They read this file to understand your users before they write designs, code, or copy.

## The 7 simple rules

| # | Rule | Why |
|---|------|-----|
| 1 | Go **top to bottom**. Do not skip ahead unless a section says "OPTIONAL". | Later sections use answers from earlier ones. |
| 2 | Replace every `[FILL: ...]` with your real answer. Delete the brackets. | A leftover `[FILL: ...]` means "not done". |
| 3 | Write in **short, plain sentences**. One idea per line. | If a 10-year-old can't read it, rewrite it. |
| 4 | Never guess. If you don't know, write `UNKNOWN` and add it to **Section 21 (Open Questions)**. | Guesses hidden as facts cause the most expensive mistakes. |
| 5 | Every claim needs **evidence**: write who said it, where you saw it, or the number. Use the tag `[Source: ...]`. | "I think" is not research. |
| 6 | Use the **tags** below on every section so everyone knows what is required. | Clear priorities, less confusion. |
| 7 | When you finish a section, tick its **Done when** box and set its status. | Progress is visible at a glance. |

## Tags used in this file

| Tag | Meaning | Can I skip it? |
|-----|---------|----------------|
| 🔴 **MUST** | Required. The product cannot move to the next phase without it. | No |
| 🟡 **SHOULD** | Strongly recommended. Skip only with a written reason. | Rarely |
| ⚪ **OPTIONAL** | Helpful but not essential. | Yes |

## Status values (use only these exact words)

| Status | Meaning |
|--------|---------|
| `NOT STARTED` | Nothing written yet |
| `IN PROGRESS` | Partly filled |
| `NEEDS REVIEW` | Filled, waiting for another person to check |
| `DONE` | Passed the "Done when" checklist |
| `SKIPPED` | Intentionally not done, with a reason written next to it |

## How every section is laid out
Each section has the same 5 parts, so you always know where to look:
1. **Why this matters** (one or two sentences)
2. **Fill this in** (tables and fields to complete)
3. **Example** (a finished sample you can copy the style from)
4. **Done when** (a checklist, so nobody has to guess if it's finished)
5. **AI-agent note** (hidden instructions in comments like `<!-- AI-AGENT: ... -->`; humans can ignore them)

## The 6 lifecycle phases (the map)

```
PHASE 0  SETUP          → Sections 1–3     (who, what, why, rules)
PHASE 1  DISCOVER       → Sections 4–11    (research the problem and the people)
PHASE 2  DEFINE         → Sections 12–16   (turn research into decisions)
PHASE 3  DESIGN & BUILD → Sections 17–19   (test ideas, build with AI, check quality)
PHASE 4  LAUNCH & GROW  → Sections 20–22   (beta → launch → first 500 customers)
PHASE 5  LEARN & CLOSE  → Sections 23–28   (metrics, risks, questions, decisions, final check, handoff)

EXTRAS  Appendix A: AI prompts | B: Quick-start | C: Role prompts per AI agent | D: Fully worked example
```

## Rules for AI agents reading this file
<!-- AI-AGENT: Follow these rules every time you open this file. -->
<!-- 1. READ this entire file before doing any design, code, or copywriting task. -->
<!-- 2. NEVER invent users, quotes, numbers, or sources. If a field says UNKNOWN or still contains [FILL: ...], say so and ask the human. -->
<!-- 3. WRITE only inside the fields you were asked to fill. Do NOT rename headings, delete sections, or change tags. -->
<!-- 4. Every insight you write must include [Source: ...] pointing to a real interview, survey, analytics, or document. -->
<!-- 5. If two sections disagree, the NEWER dated entry wins; log the conflict in Section 21 (Open Questions). -->
<!-- 6. Never paste real personal data (names, emails, phone numbers) of participants. Use IDs like P01, P02. -->
<!-- 7. After editing, update the "Change Log" in Section 27 and the section status. -->

## STOP rules for AI agents (hard stops)
<!-- AI-AGENT: If ANY row below is true, STOP. Set `blocked: true` and `blocked_reason` in the header, write the reason in Section 25, tell the human in plain words, and WAIT. Do not continue "just this once". -->

| # | STOP if... | Then do this |
|---|------------|--------------|
| S1 | A field you need still says `[FILL: ...]` or `UNKNOWN` | Ask the human; never fill it with a guess |
| S2 | You would be creating a user quote, statistic, competitor fact, or source that you cannot link | Say "I have no evidence for this" and ask for a source |
| S3 | A task has no Requirement ID (Section 16) or research question (Section 2) | Ask which one it belongs to |
| S4 | You are about to pass a gate (Section 18) and any item for it is missing | List what is missing; do not proceed |
| S5 | A step would contact real people (send email, post, reply, invite) | Draft only; a human must send |
| S6 | Data contains real names, emails, phone numbers, or faces | Redact to IDs (P01, B01) before using it |
| S7 | Two sections contradict each other and you cannot tell which is newer | Log both in Section 25; ask the human |
| S8 | A change would delete content, rename headings, or alter another person's entry | Ask first; prefer adding over deleting |
| S9 | Participants are under 18 or consent is not recorded (Section 3) | Do not use their data until the human confirms |
| S10 | You are unsure whether something is allowed | Treat it as not allowed and ask |

**How to ask well:** Give 2–3 options, say which one you recommend, and say what you will do if there is no answer (usually: nothing).

## Placeholder cheat sheet

| You see | You do |
|---------|--------|
| `[FILL: ...]` | Replace with your answer |
| `[PICK ONE: A / B / C]` | Keep one option, delete the others |
| `[PICK MANY: A / B / C]` | Keep all that apply |
| `[DATE: YYYY-MM-DD]` | Write a date like `2026-10-17` |
| `[LINK]` | Paste a web link or a file path |
| `[Source: ...]` | Say where the fact came from |
| `UNKNOWN` | You truly don't know yet. Log it in Section 21 |

---

# UX RESEARCH: [FILL: Product Name]

| Field | Value |
|-------|-------|
| Document version | `v0.1` |
| Created on | [DATE: YYYY-MM-DD] |
| Last updated | [DATE: YYYY-MM-DD] |
| Document owner | [FILL: name and role] |
| Reviewers | [FILL: names, or "none yet"] |
| Current lifecycle phase | [PICK ONE: Setup / Discover / Define / Design & Build / Launch & Grow / Learn & Close] |
| Overall status | [PICK ONE: NOT STARTED / IN PROGRESS / NEEDS REVIEW / DONE] |
| Customer goal | **500 customers who actually use the product** |
| Customers so far | [FILL: number] |

## Progress Tracker (update after each work session)

| # | Section | Phase | Tag | Status |
|---|---------|-------|-----|--------|
| 1 | Product Snapshot | Setup | 🔴 | `NOT STARTED` |
| 2 | Research Goals and Questions | Setup | 🔴 | `NOT STARTED` |
| 3 | Ethics, Privacy and Consent | Setup | 🔴 | `NOT STARTED` |
| 4 | Assumptions to Test | Discover | 🔴 | `NOT STARTED` |
| 5 | Market and Competitor Analysis | Discover | 🔴 | `NOT STARTED` |
| 6 | Existing Data and Desk Research | Discover | 🟡 | `NOT STARTED` |
| 7 | Participant Plan and Recruiting | Discover | 🔴 | `NOT STARTED` |
| 8 | Interviews | Discover | 🔴 | `NOT STARTED` |
| 9 | Surveys | Discover | 🟡 | `NOT STARTED` |
| 10 | Insights and Synthesis | Discover | 🔴 | `NOT STARTED` |
| 11 | Personas | Discover | 🔴 | `NOT STARTED` |
| 12 | Jobs To Be Done | Define | 🟡 | `NOT STARTED` |
| 13 | Journey Maps | Define | 🟡 | `NOT STARTED` |
| 14 | Accessibility and Inclusive Design | Define | 🔴 | `NOT STARTED` |
| 15 | Problem Statements and "How Might We" | Define | 🔴 | `NOT STARTED` |
| 16 | Research-to-Requirements Traceability | Define | 🔴 | `NOT STARTED` |
| 17 | Prototype and Concept Testing | Design & Build | 🔴 | `NOT STARTED` |
| 18 | AI-Driven Build: Research Checkpoints | Design & Build | 🔴 | `NOT STARTED` |
| 19 | Usability Testing and QA | Design & Build | 🔴 | `NOT STARTED` |
| 20 | Beta Program | Launch & Grow | 🔴 | `NOT STARTED` |
| 21 | Launch Plan and Research | Launch & Grow | 🔴 | `NOT STARTED` |
| 22 | Road to 500 Customers | Launch & Grow | 🔴 | `NOT STARTED` |
| 23 | Metrics and Success Criteria | Learn & Close | 🔴 | `NOT STARTED` |
| 24 | Risks Log | Learn & Close | 🔴 | `NOT STARTED` |
| 25 | Open Questions | Learn & Close | 🔴 | `NOT STARTED` |
| 26 | Decision Log | Learn & Close | 🔴 | `NOT STARTED` |
| 27 | Final Readiness Check, Change Log, Glossary | Learn & Close | 🔴 | `NOT STARTED` |
| 28 | Next-Phase Handoff (Beyond 500 Customers) | Learn & Close | 🟡 | `NOT STARTED` |

---

# PHASE 0: SETUP

## 1. Product Snapshot 🔴 MUST

**Why this matters:** Everyone (including AI agents) must agree on what the product is before researching it.

**Fill this in:**

| Question | Your answer |
|----------|-------------|
| Product name | [FILL] |
| One-sentence description (say it so a 10-year-old understands) | [FILL] |
| Product type | [PICK ONE: Web app / Mobile app / SaaS / Marketplace / AI product / Browser extension / Other: ___] |
| Platforms | [PICK MANY: Web / iOS / Android / Desktop / API] |
| Business model | [PICK ONE: Free / Freemium / Subscription / One-time purchase / Ads / Marketplace fee / Other: ___] |
| What problem does it solve? (1–2 sentences) | [FILL] |
| Who do you think it is for? (your first guess) | [FILL] |
| What do people use today instead? | [FILL] |
| Stage today | [PICK ONE: Idea / Prototype / Building / Beta / Launched] |
| Target launch date | [DATE: YYYY-MM-DD] |
| Team size (humans) and AI agents used | [FILL] |
| Budget for research | [FILL: amount or "none"] |
| Hours per week available for research | [FILL] |

> **Example:** "PlantPal is a mobile app that reminds people when to water their plants. People use sticky notes and phone alarms today. First guess: busy city workers with 5+ plants. Stage: Prototype. Launch: 2027-02-01."

**Done when:**
- [ ] Every row above is filled (or marked `UNKNOWN` and logged in Section 25)
- [ ] A stranger could explain the product after reading only this table

<!-- AI-AGENT: Treat this section as the ground truth for product context. Do not contradict it. -->

---

## 2. Research Goals and Questions 🔴 MUST

**Why this matters:** Research without questions collects noise. Good questions tell you when to stop.

**Fill this in:**

**Main research goal (one sentence):** [FILL: "We want to learn ___ so we can decide ___."]

| # | Research question (must be answerable with evidence) | Why it matters (the decision it affects) | Method to use | Phase | Priority |
|---|------------------------------------------------------|-------------------------------------------|---------------|-------|----------|
| RQ1 | [FILL] | [FILL] | [PICK: Interview / Survey / Analytics / Usability test / Desk research] | [PICK] | [High/Med/Low] |
| RQ2 | [FILL] | [FILL] | [PICK] | [PICK] | [PICK] |
| RQ3 | [FILL] | [FILL] | [PICK] | [PICK] | [PICK] |
| RQ4 | [FILL] | [FILL] | [PICK] | [PICK] | [PICK] |
| RQ5 | [FILL] | [FILL] | [PICK] | [PICK] | [PICK] |

**What we will NOT research right now (out of scope):** [FILL]

> **Example:**
> Goal: "We want to learn why people forget to water plants so we can decide which reminder style to build."
> RQ1: "What makes people forget to water plants?" → decides the reminder feature → Interviews → Discover → High.

**Choose your methods (tick all you will use):**

| Method | Use it to answer | Tick |
|--------|------------------|------|
| Competitor analysis | What exists already? | [ ] |
| Interviews | Why do people behave this way? | [ ] |
| Surveys | How many people feel this way? | [ ] |
| Usability tests | Can people actually use it? | [ ] |
| Analytics | What do people really do? | [ ] |
| Feedback, reviews, support tickets | What are people complaining about? | [ ] |
| AI-assisted synthesis | What patterns are hiding in lots of data? | [ ] |

**Done when:**
- [ ] 3–7 research questions written
- [ ] Each question links to a real decision
- [ ] Out-of-scope list written

<!-- AI-AGENT: When creating tasks, tie each one to an RQ number. Do not run research that has no RQ. -->

---

## 3. Ethics, Privacy and Consent 🔴 MUST

**Why this matters:** You are talking to real people. You must protect them and follow the law.

**Fill this in:**

| Question | Your answer |
|----------|-------------|
| Where do participants live? (decides which privacy laws apply, e.g. GDPR, CCPA) | [FILL] |
| Will you talk to anyone under 18? | [PICK ONE: Yes / No]. If yes, get a parent or guardian's written permission. |
| What personal data will you collect? | [PICK MANY: Name / Email / Voice recording / Video / Screen recording / Location / Other: ___] |
| Where will data be stored? | [FILL: tool and region] |
| Who can see raw data? | [FILL: names or roles] |
| How long will you keep it? | [FILL: e.g. 12 months] |
| How can a participant delete their data? | [FILL: e.g. "email privacy@..."] |
| Will participants be paid or rewarded? | [FILL: amount or gift] |

**Consent script (read this out loud or show it BEFORE every session):**

> "Hi, I'm [FILL: name]. We're studying [FILL: topic] to improve [FILL: product]. This takes about [FILL: minutes] minutes. Taking part is **voluntary** and you can **stop at any time** without giving a reason. With your permission we'd like to **record** [FILL: audio/screen] so we can remember what you said. Only [FILL: who] will see it, we'll keep it for [FILL: time], and we will never share your name. There are no wrong answers, and we are testing the product, **not you**. Do you agree to take part? Do you agree to be recorded?"

**Consent tracking (use IDs, not names):**

| Participant ID | Date | Agreed to take part | Agreed to recording | Method (verbal/written) |
|----------------|------|--------------------|--------------------|-------------------------|
| P01 | [DATE] | [Y/N] | [Y/N] | [FILL] |

**Done when:**
- [ ] Consent script is ready and reviewed
- [ ] Data storage place and deletion method are decided
- [ ] No real names appear anywhere in this file (use P01, P02, ...)

<!-- AI-AGENT: Never output real participant names, emails, or phone numbers. Redact them to IDs. Flag any consent gaps in Section 25. -->

---

# PHASE 1: DISCOVER

## 4. Assumptions to Test 🔴 MUST

**Why this matters:** Every product is built on hidden guesses. Writing them down lets you test the riskiest ones first.

**Fill this in:**

| ID | We believe that... | Category | Risk if wrong (1 low – 5 high) | Confidence today (1 low – 5 high) | How we will test it | Result | Evidence |
|----|--------------------|----------|-------------------------------|-----------------------------------|---------------------|--------|----------|
| A1 | [FILL] | [PICK: User need / Behavior / Willingness to pay / Technical / Market] | [1-5] | [1-5] | [FILL] | [PICK: Untested / Confirmed / Rejected / Unclear] | [Source: ...] |

**Test first:** anything with **risk 4–5 and confidence 1–2**.

> **Example:** A1: "Busy workers forget to water plants because they travel." | User need | Risk 5 | Confidence 2 | 8 interviews | Untested

**Done when:**
- [ ] At least 5 assumptions written
- [ ] The top 3 riskiest have a test plan

<!-- AI-AGENT: Update the Result and Evidence columns only after real evidence exists. Never mark Confirmed without a source. -->

---

## 5. Market and Competitor Analysis 🔴 MUST

**Why this matters:** You must know what already exists so you can be different, not just louder.

**Fill this in:**

### 5.1 Competitor table (find at least 5: direct, indirect, and "do nothing")

| # | Name | Type | Link | Who it's for | Main strength | Main weakness | Price | Users' top complaints | Source |
|---|------|------|------|--------------|---------------|---------------|-------|----------------------|--------|
| 1 | [FILL] | [PICK: Direct / Indirect / Workaround] | [LINK] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [Source] |

> "Workaround" means what people do today without any product (spreadsheet, paper, asking a friend).

### 5.2 Feature comparison (tick = has it)

| Feature | Us (planned) | Competitor 1 | Competitor 2 | Competitor 3 |
|---------|--------------|--------------|--------------|--------------|
| [FILL] | [ ] | [ ] | [ ] | [ ] |

### 5.3 Heuristic review (pick the top 2 competitors; rate 1 bad – 5 great)

| Area | Competitor 1 | Competitor 2 | Notes |
|------|--------------|--------------|-------|
| Easy first-time sign-up | | | |
| Clear navigation | | | |
| Speed and feedback | | | |
| Error messages | | | |
| Mobile experience | | | |
| Accessibility basics | | | |

### 5.4 Market size (rough numbers are fine, but cite the source)

| Question | Answer | Source |
|----------|--------|--------|
| How many people have this problem? | [FILL] | [Source] |
| How many could we realistically reach in 12 months? | [FILL] | [Source] |
| Trends (growing or shrinking?) | [FILL] | [Source] |

### 5.5 Our gap
**Where competitors fail and we can win (2–3 sentences):** [FILL]

**Done when:**
- [ ] 5+ competitors listed, including "do nothing"
- [ ] At least 20 real user reviews of competitors read and summarized
- [ ] The "Our gap" paragraph is written and backed by a source

<!-- AI-AGENT: Only cite competitors and facts you can link to. Mark unverified data as UNKNOWN. Prefer sources from the last 12 months. -->

---

## 6. Existing Data and Desk Research 🟡 SHOULD

**Why this matters:** Cheap answers may already exist: reports, reviews, forums, old analytics.

**Fill this in:**

| # | Source type | Where (link/file) | Date | Key finding (1–2 lines) | Trust level |
|---|-------------|-------------------|------|--------------------------|-------------|
| 1 | [PICK: Industry report / Academic paper / App-store reviews / Reddit or forum / Support tickets / Analytics / Social media / Internal docs] | [LINK] | [DATE] | [FILL] | [High / Med / Low] |

**Done when:**
- [ ] 5+ sources reviewed
- [ ] Each has a trust level (Low = opinion, High = measured data)

<!-- AI-AGENT: When summarizing sources, quote less than 15 words and always link the original. -->

---

## 7. Participant Plan and Recruiting 🔴 MUST

**Why this matters:** Talking to the wrong people gives confident but wrong answers.

**Fill this in:**

### 7.1 Who we want

| Question | Answer |
|----------|--------|
| **Must have** (e.g. "owns 3+ plants") | [FILL] |
| **Must NOT have** (e.g. "works in plant retail") | [FILL] |
| Age range, location, language | [FILL] |
| Tech comfort | [PICK: Low / Medium / High / Mixed] |
| Include people with disabilities or assistive tech? | [PICK: Yes / No]; see Section 14 |
| Target number of participants (guide below) | [FILL] |

**Guide:** Interviews 5–8 per user type. Usability tests 5 per round. Surveys 100+ if you want numbers. Beta 20–100.

### 7.2 Screener questions (use to filter people in or out)

| # | Question | Accept answer | Reject answer |
|---|----------|---------------|---------------|
| S1 | [FILL] | [FILL] | [FILL] |

### 7.3 Where to find people (tick all you'll try)

- [ ] Friends of friends (NOT close family or friends; they are too polite)
- [ ] Social media groups, forums, communities
- [ ] Email list or waitlist
- [ ] Research platforms (e.g. UserTesting, Prolific, Respondent)
- [ ] Customer support contacts
- [ ] Cold outreach (LinkedIn, X, email)
- [ ] Other: [FILL]

### 7.4 Participant tracker (IDs only)

| ID | User type | Source | Date contacted | Status | Session date | Reward sent |
|----|-----------|--------|----------------|--------|--------------|-------------|
| P01 | [FILL] | [FILL] | [DATE] | [PICK: Invited / Booked / Done / No-show / Withdrew] | [DATE] | [Y/N] |

**Done when:**
- [ ] Screener written and tested on 2 people
- [ ] Target count reached or a plan to reach it exists
- [ ] Tracker uses IDs only

<!-- AI-AGENT: You may draft screener and outreach messages, but never send them. A human must approve every outreach. -->

---

## 8. Interviews 🔴 MUST

**Why this matters:** Interviews tell you WHY people do things. They are the best way to learn about real problems.

**Golden rules (keep these open during interviews):**
1. Ask about the **past** ("Tell me about the last time you..."), not the future ("Would you ever...?").
2. Ask **open** questions ("How", "What", "Tell me more"), not yes/no.
3. **Stay quiet** after a question. Count to 5.
4. **Never pitch** your product during discovery.
5. Write what people **did**, not only what they **said**.

### 8.1 Interview guide (copy for each study)

| Part | Minutes | Questions |
|------|---------|-----------|
| Welcome and consent | 3 | Read the script from Section 3 |
| Warm-up | 5 | "Tell me a little about yourself and your day." |
| Context | 10 | [FILL: 2–3 questions about their life or work around the problem] |
| Main story | 15 | "Tell me about the last time you [FILL: the problem moment]." Then ask: "What happened first? What then? How did you feel? What did you try? What went wrong?" |
| Current solutions | 10 | "What do you use today? What do you like and hate about it?" |
| Magic wand | 3 | "If you could change one thing, what would it be?" |
| Close | 4 | "Anything I didn't ask that I should have? Can I contact you again?" |

### 8.2 Interview log (one row per interview)

| ID | Date | User type | Length (min) | Recording link | Notes link | Top 3 takeaways |
|----|------|-----------|--------------|----------------|------------|-----------------|
| P01 | [DATE] | [FILL] | [FILL] | [LINK] | [LINK] | 1) ___ 2) ___ 3) ___ |

### 8.3 Raw observations (write each on its own line, **one fact each**)

| # | Participant | Observation (what they did or said) | Type | Source (quote/time) |
|---|-------------|--------------------------------------|------|---------------------|
| O1 | P01 | [FILL] | [PICK: Behavior / Quote / Pain / Goal / Workaround / Emotion] | [Source] |

> **Example:** O1 | P03 | "Waters plants only when leaves droop." | Behavior | Interview P03, 12:40

**Done when:**
- [ ] 5+ interviews per main user type
- [ ] Every interview has takeaways and at least 10 observations
- [ ] You stopped when new interviews stopped giving new insights (this is called "saturation")

<!-- AI-AGENT: When analyzing transcripts, extract observations verbatim-in-spirit, label each with a Type, and keep the participant ID and timestamp. Do not summarize away contradictions. Surface them. -->

---

## 9. Surveys 🟡 SHOULD

**Why this matters:** Interviews find the *why*. Surveys count *how many*.

**Fill this in:**

| Question | Answer |
|----------|--------|
| What do we want to measure? | [FILL] |
| Tool used | [FILL: e.g. Google Forms, Typeform] |
| Target responses | [FILL: aim 100+] |
| Survey link | [LINK] |
| Open dates | [DATE] to [DATE] |

**Survey question list (keep it under 10 minutes):**

| # | Question | Type | Required? | Answers / scale |
|---|----------|------|-----------|-----------------|
| Q1 | [FILL: screener question] | [PICK: Single choice / Multi choice / Scale 1–5 / Open text] | [Y/N] | [FILL] |

**Rules:** One idea per question. No leading words (not "How great is...?"). Offer "Other" and "None". Test on 3 people first.

**Results summary:**

| Question | Result (with % and number of responses) | What it means |
|----------|------------------------------------------|---------------|
| Q1 | [FILL] | [FILL] |

**Done when:**
- [ ] Survey tested before sending
- [ ] Response count and drop-off rate recorded
- [ ] Results summarized with numbers, not feelings

<!-- AI-AGENT: Report counts alongside percentages. Warn the human if responses are fewer than 30; results are weak below that. -->

---

## 10. Insights and Synthesis 🔴 MUST

**Why this matters:** Raw notes are not answers. This step turns notes into clear, evidence-backed insights.

**How (do these in order):**
1. Put all observations from Sections 6, 8, and 9 together.
2. Group similar ones (this is called **affinity mapping**).
3. Name each group with a short sentence.
4. Count how many people support each group.
5. Write an insight: **"[People] [do/feel/need] ___ because ___."**

**Fill this in:**

| ID | Theme (group name) | Insight (full sentence) | Evidence (observation IDs) | # of participants | Strength | Impact on product |
|----|--------------------|--------------------------|----------------------------|-------------------|----------|-------------------|
| I1 | [FILL] | [FILL] | [e.g. O1, O7, O12, S-Q4] | [FILL] | [PICK: Strong 5+ / Medium 3–4 / Weak 1–2] | [PICK: Critical / Important / Nice-to-have] |

> **Example:** I1 | Forgetting | "Busy workers forget to water plants because watering has no fixed place in their routine." | O1, O7, O12 | 6 of 8 | Strong | Critical

**Assumption check-back:** Go back to Section 4 and update every assumption's Result.

**Top 5 findings (the "if you read only one thing" list):**
1. [FILL]
2. [FILL]
3. [FILL]
4. [FILL]
5. [FILL]

**Done when:**
- [ ] Every insight points to at least 2 pieces of evidence
- [ ] Strength is rated honestly
- [ ] Section 4 results are updated
- [ ] Top 5 findings are written

<!-- AI-AGENT: You may cluster and draft insights. Every insight MUST list real observation IDs. If evidence is under 3 participants, label it Weak. Highlight any evidence that CONTRADICTS the team's assumptions. -->

---

## 11. Personas 🔴 MUST

**Why this matters:** A persona is a *summary of real patterns*, not an imaginary friend. Build 1–3, based on evidence only.

**Fill this in (copy this block for each persona):**

### Persona 1: [FILL: memorable name, e.g. "Busy Bella"]

| Field | Answer | Evidence |
|-------|--------|----------|
| Based on participants | [FILL: e.g. P01, P03, P05] | |
| Short description | [FILL] | [Source] |
| Age range, job, location | [FILL] | [Source] |
| Tech comfort | [PICK: Low / Medium / High] | [Source] |
| Goals (what they want) | [FILL] | [Source] |
| Frustrations (what hurts) | [FILL] | [Source] |
| Current behavior and tools | [FILL] | [Source] |
| What would make them switch to us | [FILL] | [Source] |
| What would make them leave | [FILL] | [Source] |
| Where they spend time (channels) | [FILL] | [Source] |
| Accessibility needs | [FILL or "none found"] | [Source] |
| Real quote | [FILL: one short quote] | [Source] |
| Size of this group | [PICK: Primary (build for them) / Secondary / Edge case] | |

**Anti-persona (who this product is NOT for):** [FILL]

**Done when:**
- [ ] Each persona is based on 3+ real participants
- [ ] One persona is marked **Primary**
- [ ] No field is made up (remove any detail you can't source)

<!-- AI-AGENT: Do not add fictional details (hobbies, stock photos, invented names of people) unless the human asks. Every persona field needs a [Source]. -->

---

# PHASE 2: DEFINE

## 12. Jobs To Be Done 🟡 SHOULD

**Why this matters:** People "hire" products to make progress. Understanding the job helps you build the right thing.

**Format:** *When [situation], I want to [motivation], so I can [expected outcome].*

| ID | Persona | Job statement | Functional need | Emotional need | Social need | Importance (1–5) | How well served today (1–5) | Opportunity (importance high, served low) |
|----|---------|---------------|-----------------|----------------|-------------|------------------|-----------------------------|---------------------------------------------|
| J1 | [FILL] | When ___, I want to ___, so I can ___. | [FILL] | [FILL] | [FILL] | [1-5] | [1-5] | [High/Med/Low] |

> **Example:** J1 | Busy Bella | "When I come home late, I want to know which plant needs water, so I can avoid killing it without thinking."

**Done when:**
- [ ] 3–8 jobs written
- [ ] The top 3 opportunities are marked

<!-- AI-AGENT: Use the job statement format exactly. Link each job to insight IDs from Section 10. -->

---

## 13. Journey Maps 🟡 SHOULD

**Why this matters:** A journey map shows the whole experience, step by step, so you can spot where people struggle.

**Fill this in (one map per primary persona; cover the whole life with the product):**

| Stage | Awareness (hears about it) | Consideration (compares) | Sign-up / Start | First use (onboarding) | Regular use | Problem / support | Advocacy (tells others) |
|-------|---------------------------|--------------------------|-----------------|------------------------|-------------|-------------------|--------------------------|
| What the user does | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| What the user thinks | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| What the user feels | [PICK: 😀 😐 😟] | [PICK] | [PICK] | [PICK] | [PICK] | [PICK] | [PICK] |
| Pain points | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Opportunities | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Touchpoints (where it happens) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Evidence | [Source] | [Source] | [Source] | [Source] | [Source] | [Source] | [Source] |

**Biggest "moment of truth" (the make-or-break moment):** [FILL]

**Done when:**
- [ ] All stages are filled from evidence, not imagination
- [ ] The 3 worst pain points are circled in text: [FILL]

<!-- AI-AGENT: If a stage has no evidence, write UNKNOWN and add a research task to Section 25. -->

---

## 14. Accessibility and Inclusive Design 🔴 MUST

**Why this matters:** About 1 in 6 people live with a disability. Accessible products reach more customers and are often required by law.

**Fill this in:**

| Question | Answer |
|----------|--------|
| Target standard | [PICK ONE: WCAG 2.2 AA (Recommended) / WCAG 2.2 AAA / Other: ___] |
| Laws that apply in our markets | [FILL: e.g. ADA, EAA, Section 508] |
| Did we include people with disabilities in research? | [PICK: Yes / No]; how many: [FILL] |

**Accessibility research checklist (tick when verified):**

| Area | Check | Done |
|------|-------|------|
| Vision | Text contrast at least 4.5:1; works at 200% zoom; no info by color alone | [ ] |
| Screen readers | Tested with VoiceOver / TalkBack / NVDA; all images have alt text | [ ] |
| Keyboard | Everything usable without a mouse; visible focus | [ ] |
| Hearing | Captions and transcripts for audio and video | [ ] |
| Motor | Tap targets at least 44×44 px; no tiny precise gestures | [ ] |
| Cognitive | Plain language; clear steps; no time pressure; easy undo | [ ] |
| Seizures | Nothing flashes more than 3 times per second | [ ] |
| Situational | Works one-handed, in sunlight, on a slow connection | [ ] |

**Inclusive design check (who might we be leaving out?):**

| Group | Risk | What we'll do |
|-------|------|---------------|
| [PICK: Older adults / Low vision / Non-native speakers / Low literacy / Low-end phones / Slow internet / Neurodivergent users / Other] | [FILL] | [FILL] |

**Done when:**
- [ ] Target standard chosen
- [ ] At least one inclusion risk and action recorded
- [ ] Accessibility testing is scheduled in Section 19

<!-- AI-AGENT: When generating UI or copy, apply the checklist above by default. Flag any decision that could harm accessibility. -->

---

## 15. Problem Statements and "How Might We" 🔴 MUST

**Why this matters:** A great problem statement keeps the team building the right thing.

**Fill this in:**

| ID | Persona | Problem statement ("[Persona] needs a way to ___ because ___.") | Based on insights | Priority |
|----|---------|------------------------------------------------------------------|-------------------|----------|
| PS1 | [FILL] | [FILL] | [I1, I3] | [High/Med/Low] |

**How Might We questions (turn problems into opportunities):**

| ID | From PS | "How might we ___ so that ___?" |
|----|---------|----------------------------------|
| HMW1 | PS1 | [FILL] |

**Value proposition (one sentence):** For [FILL: persona] who [FILL: problem], [Product] is a [FILL: category] that [FILL: key benefit]. Unlike [FILL: alternative], we [FILL: difference].

**Done when:**
- [ ] 1–3 top problem statements
- [ ] 3+ HMW questions
- [ ] Value proposition written

<!-- AI-AGENT: Never write a problem statement without linking an insight ID. -->

---

## 16. Research-to-Requirements Traceability 🔴 MUST

**Why this matters:** Every feature must trace back to evidence. If you can't, you may be building something nobody wants.

**Fill this in:**

| Req ID | Requirement (what the product must do) | Type | Insight IDs | Persona | Priority (MoSCoW) | Design component or screen | Build status | Test status | Validated by (test ID) |
|--------|----------------------------------------|------|-------------|---------|-------------------|----------------------------|--------------|-------------|------------------------|
| R1 | [FILL] | [PICK: Functional / Usability / Accessibility / Content / Performance] | [I1, I2] | [FILL] | [PICK: Must / Should / Could / Won't] | [FILL: screen or component name] | [PICK: Not started / In progress / Built] | [PICK: Not tested / Passed / Failed] | [FILL] |

**MoSCoW guide:** **Must** = no launch without it. **Should** = important, but can wait. **Could** = nice extra. **Won't** = not this time.

**Orphan check (important):**
- Requirements with NO insight ID: [FILL: list them, then justify or delete]
- Insights with NO requirement: [FILL: list them, then decide]

**MVP scope (the smallest product that solves the primary problem):**

| In MVP | Not in MVP (and why) |
|--------|----------------------|
| [FILL] | [FILL] |

**Done when:**
- [ ] Every requirement links to at least one insight
- [ ] Every "Must" has a test planned
- [ ] MVP is clearly bounded

<!-- AI-AGENT: Before building any feature, find its Req ID here. If it has no Req ID or no insight link, STOP and ask the human. Update Build status and Test status when you finish work. -->

---

# PHASE 3: DESIGN & BUILD

## 17. Prototype and Concept Testing 🔴 MUST

**Why this matters:** Testing a cheap sketch costs hours. Fixing a built mistake costs weeks.

**Fill this in:**

### 17.1 Test rounds

| Round | Date | What was tested | Fidelity | Participants | Goal | Result summary |
|-------|------|-----------------|----------|--------------|------|----------------|
| T1 | [DATE] | [FILL] | [PICK: Paper sketch / Clickable wireframe / High-fidelity prototype / Working build] | [FILL: IDs] | [FILL] | [FILL] |

### 17.2 Tasks to give people (2–6 per round; never explain how to do them)

| Task ID | Task (a real-life goal) | Success looks like | Max time |
|---------|--------------------------|--------------------|----------|
| TK1 | "You want to [FILL]. Show me how you'd do that." | [FILL] | [FILL] |

### 17.3 Results per task

| Task | Participant | Success? (Y / Partial / N) | Time (sec) | Errors | Confusion points | Quote |
|------|-------------|----------------------------|------------|--------|------------------|-------|
| TK1 | P01 | [PICK] | [FILL] | [FILL] | [FILL] | [FILL] |

### 17.4 Issues found

| Issue ID | Description | Severity | Found by (# people) | Related req | Fix decision | Status |
|----------|-------------|----------|---------------------|-------------|--------------|--------|
| U1 | [FILL] | [PICK: 4 Blocker / 3 Major / 2 Minor / 1 Tip] | [FILL] | [R#] | [FILL] | [PICK: Open / Fixed / Won't fix] |

**Severity guide:** 4 = user cannot finish the task. 3 = user struggles a lot. 2 = small annoyance. 1 = suggestion.

**Done when:**
- [ ] At least 2 rounds with 5 people each
- [ ] All severity 3–4 issues are fixed or have a written reason
- [ ] Task success rate is at least 80% on key tasks

<!-- AI-AGENT: When creating or changing designs, re-check open issues here. Don't mark an issue Fixed until a retest confirms it. -->

---

## 18. AI-Driven Build: Research Checkpoints 🔴 MUST

**Why this matters:** AI can build very fast, but fast in the wrong direction wastes the most. These checkpoints keep AI-built work tied to real user needs.

**Fill this in:**

### 18.1 Tools and agents

| Role | Tool or agent used | What it is allowed to do | What it is NOT allowed to do |
|------|--------------------|--------------------------|------------------------------|
| [PICK: Designer / Coder / Tester / Writer / Analyst] | [FILL] | [FILL] | [FILL] |

### 18.2 Checkpoint gates (a human must tick each before moving on)

| Gate | Before this happens... | ...confirm this | Done | Date | Approved by |
|------|------------------------|-----------------|------|------|-------------|
| G1 | AI writes the first line of code | Sections 1–16 are `DONE`; MVP scope is frozen | [ ] | | |
| G2 | AI generates UI or screens | Primary persona and journey map are ready; accessibility target is chosen | [ ] | | |
| G3 | AI writes product copy (buttons, errors, onboarding) | Language from real interviews collected (users' own words) | [ ] | | |
| G4 | A feature is marked "built" | Its Req ID exists in Section 16 and its test is written | [ ] | | |
| G5 | Code is merged to main | Automated tests pass; human reviewed the user-facing change | [ ] | | |
| G6 | Beta invitations go out | Sections 17 and 19 are `DONE` | [ ] | | |
| G7 | Public launch | Section 27 readiness check passes | [ ] | | |

### 18.3 AI work log (one line per important AI-made change)

| Date | Req ID | What AI did | Human who reviewed | Passed review? | Notes |
|------|--------|-------------|--------------------|----------------|-------|
| [DATE] | [R#] | [FILL] | [FILL] | [Y/N] | [FILL] |

### 18.4 AI-quality risks to watch

| Risk | Example | What we do about it |
|------|---------|---------------------|
| Made-up content | AI invents a user quote or statistic | Require `[Source]` on every claim |
| Hidden bias | Personas based on stereotypes | Base personas only on real participants |
| Inaccessible output | Missing labels, poor contrast | Run the Section 14 checklist on every AI-made screen |
| Feature creep | AI adds features nobody asked for | Only build items with a Req ID |
| Privacy leak | Real user data pasted into prompts | Use IDs and redacted data only |

**Done when:**
- [ ] Gates G1–G7 are defined and understood
- [ ] AI roles and limits are written
- [ ] The log is being updated

<!-- AI-AGENT: You MUST stop at each gate and ask the human to confirm. Never skip a gate even if the human seems in a hurry; instead, list what is missing. -->

---

## 19. Usability Testing and QA 🔴 MUST

**Why this matters:** Before real customers arrive, make sure the product works, is understandable, and is safe.

**Fill this in:**

### 19.1 Quality checks

| Area | Check | Method | Result | Evidence |
|------|-------|--------|--------|----------|
| Core flows | Sign-up, first success, and main task work end-to-end | [PICK: Manual / Automated] | [PICK: Pass / Fail] | [LINK] |
| Usability | 5+ people complete key tasks (see Section 17) | Moderated or unmoderated test | [PICK] | [LINK] |
| Accessibility | Section 14 checklist, plus an automated scan (e.g. axe, Lighthouse) | [FILL] | [PICK] | [LINK] |
| Devices and browsers | Tested on [FILL: list] | [FILL] | [PICK] | [LINK] |
| Speed | Main screens load in under 3 seconds on a slow connection | [FILL] | [PICK] | [LINK] |
| Error handling | Wrong input, no internet, and empty states are clear and kind | [FILL] | [PICK] | [LINK] |
| Content | Words are plain, consistent, and typo-free | [FILL] | [PICK] | [LINK] |
| Security and privacy | Consent, data deletion, and permissions work | [FILL] | [PICK] | [LINK] |
| Analytics | Every event in Section 23 fires correctly | [FILL] | [PICK] | [LINK] |

### 19.2 Standard usability score (optional but powerful)
After testing, ask each person the **10 SUS questions** (free; search "System Usability Scale"). Record:

| Round | # People | SUS score (0–100) | Meaning |
|-------|----------|-------------------|---------|
| 1 | [FILL] | [FILL] | Below 68 = below average, 68–80 = good, above 80 = excellent |

### 19.3 Bug and UX issue summary

| Severity | Found | Fixed | Still open |
|----------|-------|-------|------------|
| 4 Blocker | | | |
| 3 Major | | | |
| 2 Minor | | | |
| 1 Tip | | | |

**Done when:**
- [ ] Zero open blockers (severity 4)
- [ ] All 9 quality areas have a result
- [ ] The analytics events work

<!-- AI-AGENT: Do not report a check as Pass without a result and an evidence link. -->

---

# PHASE 4: LAUNCH & GROW

## 20. Beta Program 🔴 MUST

**Why this matters:** A small real-world test finds problems before everyone sees them.

**Fill this in:**

| Question | Answer |
|----------|--------|
| Beta type | [PICK ONE: Closed (invite only) / Open] |
| Target beta users | [FILL: aim 20–100] |
| Start and end dates | [DATE] to [DATE] |
| How people sign up | [FILL] |
| How they give feedback | [PICK MANY: In-app button / Email / Short survey / Call / Community chat] |
| What we ask them to do | [FILL] |
| Success of beta looks like | [FILL: numbers, e.g. "60% finish setup, no blockers"] |

**Beta feedback log (IDs only):**

| Date | User ID | Channel | Feedback | Type | Severity | Req link | Action | Status |
|------|---------|---------|----------|------|----------|----------|--------|--------|
| [DATE] | B01 | [PICK] | [FILL] | [PICK: Bug / Confusion / Idea / Praise] | [1-4] | [R#] | [FILL] | [PICK: Open / Done] |

**Beta check-in questions (ask at day 1, day 7, day 14):**
1. "What were you trying to do?"
2. "Did it work? What got in your way?"
3. "How disappointed would you be if this product disappeared tomorrow?" *(Very / Somewhat / Not)*
4. "What is the one thing we should fix first?"

**Beta result:** Very disappointed = [FILL]%. (Around 40% or more suggests strong product-market fit.)

**Done when:**
- [ ] Beta goal numbers are met, or a decision is logged in Section 26
- [ ] Top 5 beta issues are fixed or explained

<!-- AI-AGENT: You may cluster beta feedback into themes and propose priorities. A human decides what gets fixed. -->

---

## 21. Launch Plan and Research 🔴 MUST

**Why this matters:** Launch is not the end. It's when real learning begins.

**Fill this in:**

### 21.1 Launch basics

| Question | Answer |
|----------|--------|
| Launch date | [DATE] |
| Launch type | [PICK ONE: Soft launch (small group) / Public launch] |
| Channels we will use | [PICK MANY: Product Hunt / Social media / Email list / Communities / Ads / Partners / Press / SEO / Referral] |
| Who is on call for problems during launch week | [FILL] |
| Rollback plan (if something breaks badly) | [FILL] |

### 21.2 Onboarding research (the first 5 minutes decide everything)

| Question | Answer |
|----------|--------|
| What is the "aha moment" (the moment a user first gets value)? | [FILL] |
| How many steps to reach it? | [FILL] (goal: fewer is better) |
| Where do people drop off? | [FILL: from analytics] |
| What do new users say about the first experience? | [FILL: from feedback or sessions] |

### 21.3 Launch-week learning checklist
- [ ] Watched at least 5 real user sessions (screen recordings) or did 5 quick calls
- [ ] Read every piece of feedback within 24 hours
- [ ] Posted a "we heard you" update to early users
- [ ] Logged every major problem in the Risks Log (Section 24)

**Done when:**
- [ ] Launch date and rollback plan are set
- [ ] The "aha moment" is defined and measured
- [ ] Learning checklist is ticked

<!-- AI-AGENT: During launch, summarize new feedback daily and flag anything that matches a known risk. Do not post or reply publicly on the human's behalf. -->

---

## 22. Road to 500 Customers 🔴 MUST

**Why this matters:** "500 customers" is the finish line for this document. Define clearly what counts, then climb in small, measurable steps.

**Define "customer" (be exact; pick ONE):**

| Definition | Choose |
|------------|--------|
| Signed up | [ ] |
| Completed onboarding / reached aha moment | [ ] |
| Used the product at least 3 times in 14 days (**Recommended: "active customer"**) | [ ] |
| Paid at least once | [ ] |
| Our own definition: [FILL] | [ ] |

**Milestone ladder (update "Reached on" as you go):**

| Milestone | Goal | Main focus | What to research | Reached on | What we learned |
|-----------|------|------------|------------------|------------|-----------------|
| M1 | First 10 | Do things that don't scale: personally onboard each person | Watch every user; call all of them | [DATE] | [FILL] |
| M2 | 50 | Fix the biggest drop-offs | Funnel analysis; 5 exit interviews with people who left | [DATE] | [FILL] |
| M3 | 100 | Find the channel that works | Ask "How did you hear about us?"; compare channels | [DATE] | [FILL] |
| M4 | 250 | Make it easy to stay and share | Retention and cohort review; referral test | [DATE] | [FILL] |
| M5 | 500 | Prove it repeats | Confirm the same growth works without founder effort | [DATE] | [FILL] |

**Acquisition channels (where customers come from):**

| Channel | Cost | Visitors | Sign-ups | Customers (per your definition) | Cost per customer | Keep / Stop / Test more |
|---------|------|----------|----------|----------------------------------|-------------------|-------------------------|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [PICK] |

**Funnel (fill monthly or weekly):**

| Stage | Week 1 | Week 2 | Week 3 | Week 4 | Notes |
|-------|--------|--------|--------|--------|-------|
| Visited | | | | | |
| Signed up | | | | | |
| Finished onboarding | | | | | |
| Became a customer (per definition) | | | | | |
| Still active after 30 days | | | | | |

**Ongoing research rhythm (do every week):**

| Day | Activity | Done? |
|-----|----------|-------|
| Weekly | Talk to 2–3 customers | [ ] |
| Weekly | Review analytics dashboard | [ ] |
| Weekly | Read all new support tickets and reviews | [ ] |
| Weekly | Update insights and Section 16 | [ ] |
| Monthly | Run 1 survey or a 5-person usability round | [ ] |
| Monthly | Review churn: ask 3 people who left why | [ ] |
| Monthly | Update this whole file's tracker | [ ] |

**AI-assisted feedback analysis (a repeatable routine):**
1. Export all new reviews, tickets, survey answers, and chat feedback (remove names).
2. Ask the AI to group them into themes and count each.
3. Check 10 random items by hand to confirm the AI grouped them correctly.
4. Add confirmed themes as new insights in Section 10.

**Done when:**
- [ ] "Customer" is defined exactly
- [ ] Customers reach 500 under that definition
- [ ] At least 2 channels are proven to work
- [ ] 30-day retention is measured and recorded

<!-- AI-AGENT: When asked "how are we doing", report counts from the Funnel table and the current milestone only. Do not estimate or round up. -->

---

# PHASE 5: LEARN & CLOSE

## 23. Metrics and Success Criteria 🔴 MUST

**Why this matters:** If you can't measure it, you can't tell if research helped.

**Fill this in:**

### 23.1 Key numbers

| Metric | What it tells you | How to measure | Target | Today | Review how often |
|--------|-------------------|----------------|--------|-------|------------------|
| Task success rate | Can people do the main thing? | Usability tests | 80%+ | | Each test round |
| Time on task | Is it quick? | Usability tests | [FILL] | | Each test round |
| SUS score | Overall ease of use | 10-question survey | 68+ | | Each test round |
| Activation rate | % reaching the aha moment | Analytics | [FILL] | | Weekly |
| Onboarding completion | % finishing setup | Analytics | [FILL] | | Weekly |
| Retention (Day 7 / Day 30) | Do they come back? | Analytics | [FILL] | | Weekly |
| NPS or "very disappointed" % | Would they miss it? | Survey | 40%+ | | Monthly |
| Support tickets per 100 users | Where it confuses people | Support tool | [FILL] | | Weekly |
| Customer count | Progress to 500 | Section 22 | 500 | | Weekly |
| Accessibility issues open | Inclusion health | Section 14/19 | 0 serious | | Each release |

### 23.2 Events we track (for analytics; use plain names)

| Event name | Fires when | Linked metric | Tested? |
|------------|------------|---------------|---------|
| `signup_completed` | A user finishes sign-up | Activation | [ ] |
| [FILL] | [FILL] | [FILL] | [ ] |

### 23.3 Research impact (did the research change anything?)

| Research finding | Decision made | Result after change |
|------------------|---------------|---------------------|
| [FILL] | [FILL] | [FILL: metric before → after] |

**Done when:**
- [ ] Every metric has a target
- [ ] Every event is tested
- [ ] At least 3 decisions were changed by research

<!-- AI-AGENT: Report metrics with the date range and sample size. If sample size is under 30, say "too few to be sure". -->

---

## 24. Risks Log 🔴 MUST

**Why this matters:** Naming risks early is how you avoid disasters.

| ID | Risk | Category | Likelihood (1-5) | Impact (1-5) | Score (L × I) | Early warning sign | Plan to reduce | Owner | Status |
|----|------|----------|------------------|--------------|---------------|--------------------|----------------|-------|--------|
| RK1 | [FILL] | [PICK: Users / Research quality / Privacy / Technical / Business / AI quality / Timeline] | [1-5] | [1-5] | [calc] | [FILL] | [FILL] | [FILL] | [PICK: Open / Reduced / Happened / Closed] |

**Common risks to consider:** too few participants; biased participants; leading questions; building before testing; consent gaps; AI inventing data; ignoring accessibility; launching without analytics; no plan to retain users.

**Done when:**
- [ ] At least 8 risks listed
- [ ] All with score 15+ have a plan and an owner

<!-- AI-AGENT: Add new risks whenever you notice a problem. Never delete a risk. Change its status instead. -->

---

## 25. Open Questions 🔴 MUST

**Why this matters:** Writing down what you don't know prevents guessing.

| ID | Question | Why it matters | Section affected | Who can answer | How we'll find out | Due date | Status |
|----|----------|----------------|------------------|----------------|--------------------|----------|--------|
| Q1 | [FILL] | [FILL] | [#] | [FILL] | [FILL] | [DATE] | [PICK: Open / Answered / Dropped] |

**Done when:**
- [ ] Every `UNKNOWN` in this file appears here
- [ ] Every open question has an owner and a date

<!-- AI-AGENT: Whenever you hit missing information, add a row here instead of guessing. -->

---

## 26. Decision Log 🔴 MUST

**Why this matters:** In 6 months nobody remembers why you chose what you chose. This log does.

| ID | Date | Decision | Options considered | Why we chose this | Evidence (insight/test IDs) | Decided by | Can we undo it? |
|----|------|----------|--------------------|-------------------|------------------------------|------------|-----------------|
| D1 | [DATE] | [FILL] | [FILL] | [FILL] | [I#, T#] | [FILL] | [Y/N] |

**Done when:**
- [ ] Every major product decision since Phase 1 is logged
- [ ] Each links to evidence (or says "gut feeling" honestly)

<!-- AI-AGENT: Draft decision entries for human approval. Never mark a decision as final yourself. -->

---

## 27. Final Readiness Check, Change Log, Glossary 🔴 MUST

### 27.1 Final readiness check (tick every box before launch and again at 500 customers)

**Research quality**
- [ ] Every 🔴 section above is `DONE`
- [ ] No `[FILL: ...]` placeholders remain
- [ ] Every insight and persona has sources
- [ ] No real personal data exists in this file

**Product quality**
- [ ] MVP scope is frozen and every "Must" requirement is tested
- [ ] Task success rate is 80% or higher
- [ ] Zero open blocker issues
- [ ] Accessibility target is met

**Launch readiness**
- [ ] Analytics events are tested
- [ ] Rollback plan exists
- [ ] Support path exists (people know how to get help)
- [ ] Consent and privacy steps are in place

**Growth readiness**
- [ ] "Customer" is defined
- [ ] Milestone ladder is set
- [ ] Weekly research rhythm is running

**500-customer wrap-up (do when you reach 500)**
- [ ] Wrote a one-page "What we learned" summary: [FILL]
- [ ] Updated personas using real customer data
- [ ] Archived raw research files where the team can find them
- [ ] Decided next goal: [FILL]

**Final sign-off:**

| Name | Role | Date | Approved |
|------|------|------|----------|
| [FILL] | [FILL] | [DATE] | [ ] |

### 27.2 Change Log (newest at the top)

| Date | Version | Who (human or AI) | What changed | Sections touched |
|------|---------|-------------------|--------------|------------------|
| [DATE] | v0.1 | [FILL] | Created from template (template v1.1) | All |

### 27.3 Glossary (simple words for hard ideas)

| Word | Simple meaning |
|------|----------------|
| UX research | Finding out what real people need and how they behave |
| Participant | A person who helps your research |
| Insight | A proven lesson learned from evidence |
| Persona | A summary of a group of real users |
| JTBD (Jobs To Be Done) | The job a person "hires" your product to do |
| Journey map | A picture of every step a person takes with your product |
| Affinity mapping | Sorting notes into groups by similarity |
| Screener | Questions to pick the right participants |
| Saturation | When new interviews stop teaching you new things |
| Usability test | Watching someone try to use your product |
| Prototype | An early, cheap version used for testing |
| MVP | Smallest product that solves the main problem |
| MoSCoW | Must / Should / Could / Won't priority system |
| WCAG | International rules for accessible websites and apps |
| SUS | A 10-question score for ease of use |
| NPS | Score for how likely people are to recommend you |
| Activation | A new user reaching their first real success |
| Retention | People who keep coming back |
| Churn | People who leave |
| Funnel | The steps from visitor to customer |
| Cohort | A group of users who started in the same period |
| Traceability | A link from every feature back to proof it's needed |
| Product-market fit | When enough people truly need your product |
| Anti-persona | Someone you are not building for |

---

## 28. Next-Phase Handoff (Beyond 500 Customers) 🟡 SHOULD

**Why this matters:** Reaching 500 is a start, not an end. This section turns what you learned into a clear plan for the next stage, so nothing is lost.

**Fill this in:**

### 28.1 What worked and what didn't

| Area | What worked (with evidence) | What did not work (with evidence) | Keep / Change / Stop |
|------|------------------------------|-----------------------------------|----------------------|
| Product | [FILL] | [FILL] | [PICK] |
| Onboarding | [FILL] | [FILL] | [PICK] |
| Acquisition channels | [FILL] | [FILL] | [PICK] |
| Retention | [FILL] | [FILL] | [PICK] |
| Research methods | [FILL] | [FILL] | [PICK] |

### 28.2 Next goal

| Question | Answer |
|----------|--------|
| Next customer goal | [PICK ONE: 1,000 / 5,000 / 10,000 / Revenue goal: ___ / Other: ___] |
| Target date | [DATE] |
| Biggest unknown to solve next | [FILL] |
| New user groups to research (not covered so far) | [FILL] |
| New markets or languages to research | [FILL] |

### 28.3 Research that changes at a bigger size

| Today (up to 500) | Next (500+) |
|--------------------|-------------|
| Talk to customers one by one | Add a regular survey and in-app feedback prompt |
| Founder reads all feedback | Use tagged feedback and AI-assisted theme counts, with human spot-checks |
| Manual funnel tracking | Cohort dashboards and A/B tests |
| 5-person usability rounds | Add remote unmoderated tests and session replays |
| One persona set | Segments with their own journeys and metrics |

### 28.4 Handoff checklist (for a new teammate, a new AI agent, or future you)

- [ ] This file is up to date and the Change Log is current
- [ ] Raw research files are stored here: [LINK]
- [ ] Top 10 learnings are written in Section 10
- [ ] Open Questions (Section 25) are sorted by priority
- [ ] A new copy of this template is started for the next research cycle: [LINK]

**Done when:**
- [ ] Next goal and date are written
- [ ] The next three research questions are named: 1) [FILL] 2) [FILL] 3) [FILL]
- [ ] Handoff checklist is ticked

<!-- AI-AGENT: Draft this section from Sections 22, 23, 24, and 26 only. Mark every item you cannot support with evidence as UNKNOWN. A human approves the final next goal. -->

---

## Appendix A: Copy-and-Paste Prompts for AI Agents

> Replace anything in `{CURLY BRACES}`. Always paste the relevant section of this file along with the prompt.

**A1. Find themes in interview notes**
```
Read the observations below. Group them into themes. For each theme give: a short name, a one-sentence insight, the observation IDs that support it, and how many different participants support it. Do NOT invent anything. If evidence is under 3 participants, label it Weak. List any contradictions you notice.
{PASTE Section 8.3}
```

**A2. Check my interview questions**
```
Review these interview questions. Find any that are leading, ask about the future, or can be answered with yes/no. Rewrite them as open questions about past behavior.
{PASTE Section 8.1}
```

**A3. Analyze customer feedback**
```
Group this feedback into themes with counts. Show 3 example IDs per theme. Separate bugs, confusion, and feature ideas. Do not guess when feedback is unclear; list it as "Unclear".
{PASTE feedback with names removed}
```

**A4. Check requirement traceability**
```
Compare Section 10 (insights) and Section 16 (requirements). List: (1) requirements with no insight, (2) insights with no requirement, (3) requirements that seem to contradict an insight.
{PASTE both sections}
```

**A5. Pre-gate check**
```
I want to pass Gate {G#} from Section 18. Read this whole file. List every item that is still missing, UNKNOWN, or marked NOT STARTED that blocks this gate. Do not proceed; just report.
{PASTE whole file}
```

**A6. Accessibility review of a design**
```
Review this screen description or code against the checklist in Section 14. List every failing item and a specific fix. Do not say "looks fine" without naming each check.
{PASTE design or code + Section 14}
```

## Appendix C: Role Prompts for Each AI Agent

> Paste the role prompt at the start of a session, then paste this whole file. Every agent must obey the **STOP rules** at the top.

**C1. Research Analyst agent**
```
You are the Research Analyst for this product. Read the whole attached UX_Research.md first.
YOU MAY: cluster observations, draft insights (Section 10), update assumption results (Section 4), summarize surveys and feedback (Sections 9, 20, 22), and propose open questions (Section 25).
YOU MAY NOT: invent participants, quotes, numbers, or sources; contact anyone; change other sections' headings.
RULES: Every insight lists real observation IDs and a participant count. Label evidence under 3 participants as Weak. Show contradictions. Obey every STOP rule (S1–S10). Finish by listing what you changed and what you need from me.
```

**C2. UX Designer agent**
```
You are the UX Designer for this product. Read the whole attached UX_Research.md first.
Before designing, confirm: Gate G2 is passed (Section 18), the Primary persona exists (Section 11), and the accessibility target is chosen (Section 14).
YOU MAY: propose flows, wireframes, screens, and microcopy for requirements that have a Req ID (Section 16).
YOU MAY NOT: add features without a Req ID; use invented personas or quotes; ignore open severity 3–4 issues (Section 17).
RULES: For each screen, name the Req ID, the persona, the insight IDs behind it, and any Section 14 checks it must pass. Use the users' own words from Section 8. Obey every STOP rule. If something is missing, ask me; don't guess.
```

**C3. Developer agent**
```
You are the Developer for this product. Read the whole attached UX_Research.md first.
Before writing code, confirm: Gate G1 is passed (Section 18) and the task has a Req ID (Section 16).
YOU MAY: build and test only the requirement I name; update Build status and Test status for that Req ID; add rows to the AI work log (Section 18.3).
YOU MAY NOT: add unrequested features; collect extra personal data; skip tests; merge without a human review (Gate G5).
RULES: Follow the Section 14 accessibility checklist in all UI code. Fire only the analytics events listed in Section 23.2. Obey every STOP rule. End each task by stating: what you built, how you tested it, and what a human must check.
```

**C4. QA and Usability Tester agent**
```
You are the QA and Usability Tester for this product. Read the whole attached UX_Research.md first.
YOU MAY: write test cases from Section 16 and Section 17 tasks; run the Section 19 quality checks; log issues with severity (4 Blocker, 3 Major, 2 Minor, 1 Tip).
YOU MAY NOT: mark any check as Pass without a result and an evidence link; mark an issue Fixed before a retest.
RULES: Report counts, not feelings. Test accessibility using the Section 14 checklist plus an automated scan. Obey every STOP rule. Finish with a table: check, result, evidence, and open issues.
```

**C5. Content and Copy agent**
```
You are the Content Writer for this product. Read the whole attached UX_Research.md first.
Before writing, confirm Gate G3 is passed (Section 18).
YOU MAY: draft button labels, onboarding text, error messages, and help articles in plain language (reading level around age 10–12).
YOU MAY NOT: invent testimonials, reviews, statistics, or quotes; promise features that are not built.
RULES: Reuse the users' own words from Section 8 where they fit. Keep each message short, kind, and specific, saying what happened and what to do next. Obey every STOP rule.
```

**C6. Growth and Analytics agent**
```
You are the Growth and Analytics agent for this product. Read the whole attached UX_Research.md first.
YOU MAY: update the funnel and channel tables (Section 22), calculate metrics (Section 23), propose experiments, and draft the Section 28 handoff.
YOU MAY NOT: round numbers up, report results from fewer than 30 people as certain, or post or message anyone.
RULES: Always show the date range and sample size. Use the exact customer definition in Section 22. Obey every STOP rule.
```

---

## Appendix B: Quick-Start Path for Beginners (in a hurry? do this order)

1. Fill **Sections 1, 2, 3** (about 1 hour).
2. Fill **Section 5** (competitors) and **Section 4** (assumptions).
3. Find 5 people (Section 7) and interview them (Section 8).
4. Do **Section 10** (insights) and **Section 11** (one persona).
5. Do **Sections 15 and 16** (problem and requirements).
6. Test a sketch with 5 people (**Section 17**).
7. Build with AI using the gates in **Section 18**.
8. QA, beta, launch, then climb the ladder in **Sections 19–22**.
9. Track **Section 23**, and keep **Sections 24–26** current.
10. At 500 customers, finish **Section 27** and write the handoff in **Section 28**.
11. Stuck on how a section should look? Open **Appendix D** for a fully worked example.

> **Remember:** If you are ever unsure, write `UNKNOWN`, add it to Section 25, and keep going. A truthful gap is better than a confident guess.

---

## Appendix D: Fully Worked Example ("PlantPal", a made-up product)

> **This is a pretend product so you can see what "well filled" looks like.** All people, numbers, and quotes below are invented for teaching. Never copy them into a real project. Use them only to see the style: short sentences, one fact per line, a source on every claim.

### D1. Section 1: Product Snapshot (filled)

| Question | Your answer |
|----------|-------------|
| Product name | PlantPal |
| One-sentence description | A phone app that tells you which plant needs water today. |
| Product type | Mobile app |
| Platforms | iOS, Android |
| Business model | Freemium |
| What problem does it solve? | People forget to water plants, and the plants die. |
| Who do you think it is for? | Busy city workers with 5 or more plants. |
| What do people use today instead? | Phone alarms, sticky notes, memory. |
| Stage today | Prototype |
| Target launch date | 2027-02-01 |
| Team size and AI agents | 1 founder; 1 designer agent, 1 coder agent, 1 tester agent |
| Budget for research | $300 for rewards |
| Hours per week | 8 |

### D2. Section 2: Research Goals (filled)

**Main goal:** We want to learn why people forget to water plants so we can decide which reminder style to build.

| # | Research question | Why it matters | Method | Phase | Priority |
|---|-------------------|----------------|--------|-------|----------|
| RQ1 | What makes people forget to water plants? | Decides the reminder feature | Interview | Discover | High |
| RQ2 | How many plant owners have lost a plant in the last year? | Shows how big the problem is | Survey | Discover | High |
| RQ3 | Can people add 5 plants in under 2 minutes? | Decides the onboarding design | Usability test | Design & Build | High |

**Out of scope for now:** Plant disease detection, plant shop, social features.

### D3. Section 4: Assumptions (filled)

| ID | We believe that... | Category | Risk | Confidence | How we will test it | Result | Evidence |
|----|--------------------|----------|------|------------|---------------------|--------|----------|
| A1 | Busy workers forget because watering has no fixed place in their routine | User need | 5 | 2 | 8 interviews | Confirmed | [Source: I1, 6 of 8 interviews] |
| A2 | People will pay $3 a month for reminders | Willingness to pay | 5 | 1 | Survey + beta | Unclear | [Source: Survey Q7; only 12% said yes] |

### D4. Section 5: Competitor row (filled)

| # | Name | Type | Link | Who it's for | Main strength | Main weakness | Price | Users' top complaints | Source |
|---|------|------|------|--------------|---------------|---------------|-------|----------------------|--------|
| 1 | Sticky notes | Workaround | n/a | Everyone | Free, instant | Falls off, gets ignored | Free | "I forget to look at them" (3 of 8 interviews) | Interviews P02, P04, P07 |
| 2 | LeafAlarm (invented) | Direct | https://example.com | Plant hobbyists | Huge plant database | Too many steps to set up | $4/month | "Took 15 minutes to add my plants" | [Source: 20 store reviews, read 2026-10-01] |

**Our gap:** Existing apps are built for hobbyists and are slow to set up. Busy workers need a 2-minute setup and one daily nudge.

### D5. Section 8: Observations (filled)

| # | Participant | Observation | Type | Source |
|---|-------------|-------------|------|--------|
| O1 | P03 | Waters plants only when leaves droop. | Behavior | Interview P03, 12:40 |
| O2 | P03 | "I always mean to, and then I get home and forget." | Quote | Interview P03, 14:05 |
| O3 | P05 | Set 3 phone alarms; turned them all off after a week. | Behavior | Interview P05, 09:10 |
| O4 | P07 | Feels guilty when a plant dies. | Emotion | Interview P07, 21:30 |

### D6. Section 10: Insight (filled)

| ID | Theme | Insight | Evidence | # of participants | Strength | Impact |
|----|-------|---------|----------|-------------------|----------|--------|
| I1 | Forgetting | Busy workers forget to water plants because watering has no fixed place in their routine. | O1, O2, O3 | 6 of 8 | Strong | Critical |
| I2 | Alarm fatigue | People stop using alarms because alarms are not tied to a specific plant. | O3, O9 | 3 of 8 | Medium | Important |

### D7. Section 11: Persona (filled, shortened)

**Persona 1: Busy Bella (Primary).** Based on P01, P03, P05.

| Field | Answer | Evidence |
|-------|--------|----------|
| Description | Works long hours; owns 6 plants; wants a calm home. | Interviews P01, P03, P05 |
| Goals | Keep plants alive with no extra thinking. | I1 |
| Frustrations | Forgets; feels guilty; alarms get ignored. | O3, O4 |
| What would make her switch | Setup under 2 minutes; one daily nudge. | Interview P05 |
| What would make her leave | Too many notifications. | Interview P03 |
| Accessibility needs | None found; 1 participant uses large text. | Interview P06 |
| Size | Primary | |

**Anti-persona:** Plant hobbyists who want detailed care science.

### D8. Section 16: Traceability (filled)

| Req ID | Requirement | Type | Insight IDs | Persona | MoSCoW | Screen | Build | Test | Validated by |
|--------|-------------|------|-------------|---------|--------|--------|-------|------|--------------|
| R1 | User can add a plant in under 20 seconds. | Usability | I1 | Bella | Must | Add Plant | Built | Passed | T2 / TK1 |
| R2 | App sends one daily "water these today" message at a time the user picks. | Functional | I1, I2 | Bella | Must | Today | In progress | Not tested | n/a |
| R3 | User can mark a plant "watered" with one tap. | Usability | I1 | Bella | Must | Today | Built | Passed | T2 / TK2 |
| R4 | Dark mode. | Functional | none | any | Could | Settings | Not started | Not tested | n/a |

**Orphan check:** R4 has no insight. Decision: move to "Won't (this time)" until research shows a need. (Logged as D2 in Section 26.)

### D9. Section 17: Test results (filled)

| Task | Participant | Success? | Time (sec) | Errors | Confusion points | Quote |
|------|-------------|----------|------------|--------|------------------|-------|
| TK1: Add 5 plants | P11 | Y | 95 | 0 | None | "That was quick." |
| TK1: Add 5 plants | P12 | Partial | 160 | 2 | Could not find the "Add" button | "Where do I tap?" |

| Issue ID | Description | Severity | Found by | Related req | Fix decision | Status |
|----------|-------------|----------|----------|-------------|--------------|--------|
| U1 | "Add" button is too small and hard to find | 3 Major | 3 of 5 | R1 | Make it bigger; place it at the bottom center | Fixed (retested T3) |

### D10. Section 18: Gate log (filled)

| Gate | Before this happens... | ...confirm this | Done | Date | Approved by |
|------|------------------------|-----------------|------|------|-------------|
| G1 | AI writes the first line of code | Sections 1–16 are `DONE`; MVP scope is frozen | [x] | 2026-11-20 | Founder |
| G2 | AI generates UI or screens | Persona and journey map ready; accessibility target chosen | [x] | 2026-11-22 | Founder |

### D11. Section 22: Milestones (filled)

**Customer definition chosen:** Used the app at least 3 times in 14 days.

| Milestone | Goal | Reached on | What we learned |
|-----------|------|------------|-----------------|
| M1 | First 10 | 2027-02-10 | Setup was fine; people wanted to pick the reminder time. |
| M2 | 50 | 2027-03-05 | 40% quit during setup; we cut it from 6 steps to 3. |
| M3 | 100 | 2027-03-28 | Plant-lover groups gave 3× more customers than ads. |

### D12. Section 24 and 26: Risk and decision (filled)

| ID | Risk | Category | L | I | Score | Early warning | Plan | Owner | Status |
|----|------|----------|---|---|-------|---------------|------|-------|--------|
| RK1 | Users disable notifications and never return. | Users | 4 | 5 | 20 | Day-7 retention under 25% | Let users choose the time; limit to 1 message a day | Founder | Open |

| ID | Date | Decision | Options considered | Why | Evidence | Decided by | Undo? |
|----|------|----------|--------------------|-----|----------|------------|-------|
| D1 | 2026-11-18 | Build one daily reminder, not per-plant alarms. | Per-plant alarms; one daily reminder | Alarm fatigue (I2) and the daily routine need (I1) | I1, I2, A1 | Founder | Yes |

---
*End of template. Template version: 1.1 | Copy this file into each new project's "UX, UI and design system" folder, rename the title in the first heading, and fill the YAML header at the very top.*
