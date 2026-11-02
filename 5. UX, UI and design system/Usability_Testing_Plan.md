# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **One file, one plan.** Copy this file once per project. Rename it to `Usability_Testing_Plan_<ProjectName>_v1.0.md`. Keep it in your `UX-UI-Design-System/` folder.

## What is a Usability Testing Plan?
A usability test means watching real people try to use your product, so you learn what is confusing **before** you spend money fixing it later. This plan is the single page of truth that says **who** you test, **what** you test, **when**, **how**, and **what result means "we can launch."**

This template covers the whole journey: **build, prototype, alpha, beta, launch, and your first 500 customers.** It works for **web apps, mobile apps, and AI-powered products.**

## The 7 simple rules
1. **Fill every section in order, top to bottom.** Do not jump around.
2. **Look at the tag next to each heading:**
   - 🔴 **[REQUIRED]** — you must fill it in. The plan is not valid without it.
   - 🟡 **[RECOMMENDED]** — fill it unless you have a good reason not to. Write the reason if you skip.
   - ⚪ **[OPTIONAL]** — fill it only if it applies. Otherwise write `N/A`.
3. **Replace everything in `[square brackets]`.** Delete the brackets when done.
4. **Never leave a field empty.** Write `TBD – owner: <name> – due: <date>`, `N/A – <reason>`, or the real answer.
5. **If you are unsure, use the "If unsure, write:" default** shown under many fields.
6. **Use numbers, not feelings.** Write "8 of 10 people finished," not "most people did fine."
7. **Use plain words.** If a 10-year-old cannot understand a sentence, rewrite it.

## Quick-start (about 30 minutes for a first draft)
Fill these first: **Sections 0, 1, 2, 3, 5, 9, 13 and 21.** That gives you a usable draft. Then complete every other 🔴 **[REQUIRED]** section and run the checklist in **Section 23** before you approve the plan (Section 24).

**New to this? Read Section 28 (a fully filled example) before you start.**

## Mini glossary (plain English)
| Word | Meaning |
|---|---|
| **Participant** | A real person who tests your product |
| **Facilitator** | The person who runs the test and guides the participant |
| **Task** | One thing you ask the participant to try ("Buy a plan") |
| **Moderated test** | A facilitator is present (live call or in person) |
| **Unmoderated test** | The participant tests alone with a tool; nobody watches live |
| **Success rate** | % of participants who finished a task |
| **Severity** | How bad a problem is (0 = not a problem, 4 = blocks the user) |
| **SUS** | System Usability Scale: a 10-question score from 0 to 100 |
| **SEQ** | Single Ease Question: "How easy was this task?" (1–7) |
| **NPS** | Net Promoter Score: "How likely are you to recommend us?" (0–10) |
| **CSAT** | Customer Satisfaction: "How satisfied are you?" (1–5) |
| **Go / No-Go** | The decision to continue to the next phase or stop and fix |
| **WCAG** | Web Content Accessibility Guidelines (rules for making products usable by everyone) |
| **Hallucination** | When an AI states something false as if it were true |
| **Trust calibration** | Trusting the AI the *right* amount: not too much, not too little |
| **Calibration gap** | The difference between how much users trust an AI answer and how often it is actually correct |
| **Design token** | A named design value (a color, spacing size, or font size) reused everywhere |
| **Component** | A reusable piece of interface, like a button, form field, or chat bubble |

## How to use AI agents with this document
- Every section has an **`Agent Check`** line. An AI agent can read it and verify the section is complete.
- Humans write the decisions. Agents may **draft, summarize, check for gaps, and format.** Agents must **not** approve Go/No-Go decisions (Section 21).
- Ready-to-paste agent prompts for every phase are in **Section 27**.
- Quick check prompt: *"Read `Usability_Testing_Plan.md`. For each section, list any `[bracket]` left unfilled, any `TBD` without owner and date, and any rule it breaks. Do not change my answers."*

---

# 0. DOCUMENT CONTROL 🔴 [REQUIRED]

| Field | Your answer |
|---|---|
| Project name | [e.g., "Acme Budget App"] |
| Product type | [ ] Web app  [ ] Mobile app (iOS / Android)  [ ] AI-powered feature/product  [ ] Mix: [describe] |
| Plan version | [v1.0] |
| Plan status | [ ] Draft  [ ] In review  [ ] Approved  [ ] Archived |
| Plan owner (one person) | [Name, role, email] |
| Created on | [YYYY-MM-DD] |
| Last updated | [YYYY-MM-DD] |
| Linked documents | [PRD link, design files link, research repo link, issue tracker link] |
| **Project ID** (unique across all projects) | [e.g., PRJ-2026-0042] |
| Portfolio / program | [e.g., Consumer Apps / Finance] |
| Business priority | [ ] P1 Critical  [ ] P2 High  [ ] P3 Medium  [ ] P4 Low |
| Risk tier | [ ] High (money, health, children, safety, AI decisions)  [ ] Medium  [ ] Low |
| Tags (for searching across projects) | [e.g., mobile, ai, fintech, onboarding] |
| Design system and version used | [e.g., "Acme DS v3.2" or "None"] |
| Related plans (same product, earlier or later) | [Project IDs] |
| Reuse note | [Was this plan copied from another? Which Project ID?] |

**Agent Check:** All rows filled; exactly one owner; dates in `YYYY-MM-DD`.

---

# 1. PLAN IN ONE PARAGRAPH 🔴 [REQUIRED]

Fill this sentence template. It is your plan in 30 seconds:

> We will test **[product/feature]** with **[number]** people who are **[who they are]** during **[phases]**, to find out whether they can **[main thing they must be able to do]**. We will launch when **[success rule]**. The plan runs from **[start date]** to **[end date / first 500 customers reached]**.

If unsure, write: *Keep it to 3 sentences. No jargon.*

**Agent Check:** Paragraph mentions product, participant count, goal, launch rule, and dates.

---

# 2. GOALS AND QUESTIONS 🔴 [REQUIRED]

## 2.1 Business goal
[Why does this product exist? Example: "Help people track spending in under 2 minutes a day."]

## 2.2 Usability goals (pick 1–5, each measurable)
| # | Goal | How we measure it | Target |
|---|---|---|---|
| G1 | [e.g., New users can create an account] | [Task success rate] | [≥ 90%] |
| G2 | [e.g., Users find the "Pay" button fast] | [Time on task] | [≤ 30 seconds] |
| G3 | [e.g., Users trust AI answers] | [Trust rating 1–5] | [≥ 4.0] |

## 2.3 Research questions (what you want to learn)
Write questions that start with "Can…", "Why…", or "How…".
1. [e.g., Can first-time users finish sign-up without help?]
2. [e.g., Why do users abandon the checkout?]
3. [e.g., How do users react when the AI gives a wrong answer?]

## 2.4 What we will do with the answers (decisions this test will drive)
[e.g., "If checkout success < 80%, redesign the payment screen before beta."]

**Agent Check:** Every goal has a number target; every question maps to a decision.

---

# 3. SCOPE 🔴 [REQUIRED]

| In scope (we test this) | Out of scope (we do NOT test this) |
|---|---|
| [e.g., Sign-up, onboarding, checkout, AI assistant] | [e.g., Admin panel, billing emails] |

**Platforms and devices to cover:**
| Platform | Versions / devices | In scope? |
|---|---|---|
| Web | [Chrome, Safari, Firefox, Edge — latest 2 versions] | [Yes/No] |
| iOS | [e.g., iPhone 13 and newer, iOS 17+] | [Yes/No] |
| Android | [e.g., Pixel 7, Samsung S23, Android 13+] | [Yes/No] |
| Tablet / desktop widths | [e.g., 768px, 1280px] | [Yes/No] |

If unsure, write: *Test on the devices your real users use most. Check your analytics.*

**Agent Check:** Scope and out-of-scope lists both non-empty; platforms have versions.

---

# 4. PRODUCT SNAPSHOT 🔴 [REQUIRED]

| Field | Your answer |
|---|---|
| One-line product description | [What it is and who it is for] |
| Top 3 user journeys | 1. [e.g., Sign up] 2. [e.g., Add first expense] 3. [e.g., Ask AI for advice] |
| Current stage | [ ] Idea  [ ] Wireframe  [ ] Clickable prototype  [ ] Working build  [ ] Live |
| Test environment | [Link to prototype / staging / beta build + login details location (NOT the password itself)] |
| Is this product AI-powered? | [ ] Yes (fill Section 15)  [ ] No (write "N/A" in Section 15) |

**Agent Check:** Three journeys listed; test link present; AI flag set.

---

# 5. PHASED TEST PLAN (BUILD → FIRST 500 CUSTOMERS) 🔴 [REQUIRED]

This is the heart of the document. Each phase is a separate round of testing. **Skip a phase only if you write the reason.**

## 5.1 Phase overview table

| Phase | Name | Product stage tested | Participants | Main method | Main question | Exit gate (Section 21) |
|---|---|---|---|---|---|---|
| P0 | Concept & prototype | Sketches, wireframes, clickable mockups | 5–8 | Moderated, think-aloud | Do people understand the idea and flow? | [ ] Passed |
| P1 | Development / alpha | Early working build (internal + friendly users) | 5–10 | Moderated + unmoderated task tests | Do the core tasks work for real? | [ ] Passed |
| P2 | Closed beta | Near-final build | 20–50 | Unmoderated + in-product surveys | Is it easy, reliable, and trustworthy at small scale? | [ ] Passed |
| P3 | Pre-launch / open beta | Release candidate | 50–150 | Unmoderated + analytics + accessibility audit | Is it ready for the public? | [ ] Passed |
| P4 | Launch (customers 1–100) | Live product | First 100 users | In-product feedback, session replays, short interviews | What breaks in the real world? | [ ] Passed |
| P5 | Growth (customers 101–500) | Live product | Next 400 users | Surveys (SUS, NPS, CSAT), analytics, support tickets | Does usability hold as we grow? | [ ] Passed |

> Change numbers if needed, but write why. If unsure, keep the defaults.

## 5.2 Phase details (copy this block for each phase P0–P5)

### Phase [P#] – [Name]
| Field | Your answer |
|---|---|
| Start date / end date | [YYYY-MM-DD → YYYY-MM-DD] |
| Phase owner | [Name] |
| Number of participants | [#] |
| Who they are | [Link to Section 7 segment] |
| Test method(s) | [Moderated / Unmoderated / In-product / Survey] |
| Tasks used | [Task IDs from Section 9] |
| Metrics collected | [From Section 10] |
| Tools used | [From Section 12] |
| Budget for this phase | [$] |
| Risks | [Link to Section 20] |
| Result summary (fill AFTER the phase) | [3 sentences max] |
| Decision | [ ] Go  [ ] Go with conditions  [ ] No-Go |

**Agent Check:** All six phases present (or skipped with reason); dates don't overlap illegally; every phase has an owner and a gate.

## 5.3 Timeline summary
| Milestone | Date | Done? |
|---|---|---|
| Plan approved | [date] | [ ] |
| Recruitment starts | [date] | [ ] |
| P0 complete | [date] | [ ] |
| P1 complete | [date] | [ ] |
| P2 complete | [date] | [ ] |
| P3 complete | [date] | [ ] |
| Public launch | [date] | [ ] |
| Customer #100 reached | [date] | [ ] |
| Customer #500 reached | [date] | [ ] |
| Final report delivered | [date] | [ ] |

---

# 6. TEAM AND ROLES (RACI) 🔴 [REQUIRED]

**R** = Does the work · **A** = Final say (only ONE per row) · **C** = Gives advice · **I** = Kept informed

| Activity | Plan owner | Facilitator | Designer | Developer | Product manager | QA | Legal/Privacy | AI agent |
|---|---|---|---|---|---|---|---|---|
| Write the plan | A/R | C | C | C | C | C | C | R (draft) |
| Recruit participants | C | R | I | I | A | I | C | R (screening drafts) |
| Prepare prototype/build | I | C | R | R | A | C | I | I |
| Run sessions | I | A/R | C | I | I | C | I | R (notes only) |
| Analyze results | A | R | R | C | C | C | I | R (summary drafts) |
| Rate issue severity | C | R | C | C | A | C | I | R (suggest only) |
| Approve Go / No-Go | C | C | C | C | A | C | C | **Never** |
| Fix issues | I | I | R | R | A | C | I | R (suggest fixes) |

**People list**
| Name | Role | Email / chat handle | Backup person |
|---|---|---|---|
| [Name] | [Role] | [handle] | [Name] |

**Agent Check:** Every row has exactly one `A`; AI agent never has `A`.

---

# 7. PARTICIPANTS 🔴 [REQUIRED]

## 7.1 Who are your users? (segments)
| Segment ID | Description | Why they matter | Share of total participants |
|---|---|---|---|
| S1 | [e.g., First-time budgeters aged 18–25] | [Biggest target market] | [40%] |
| S2 | [e.g., Experienced spreadsheet users] | [Likely early adopters] | [30%] |
| S3 | [e.g., People who use assistive technology] | [Accessibility coverage] | [at least 10–15%] |
| S4 | [Other] | [Why] | [%] |

If unsure, write: *Describe your real customer in one sentence, then add one "edge" group (for example, someone with low tech skill).*

## 7.2 Screening questions (who qualifies?)
| # | Question | Correct answer to qualify | Disqualify if |
|---|---|---|---|
| 1 | [e.g., Do you manage a personal budget?] | [Yes] | [No] |
| 2 | [e.g., Which phone do you use?] | [iPhone or Android] | [Other] |
| 3 | [e.g., Do you work in UX, design, or for a competitor?] | [No] | [Yes] |

## 7.3 Recruitment
| Field | Your answer |
|---|---|
| How we find people | [ ] Own customers/waitlist  [ ] Panel service  [ ] Social media  [ ] Community  [ ] Internal friendly users |
| Backup plan if too few show up | [e.g., Recruit 20% extra] |
| No-show expectation | [Plan for 10–20% no-shows] |
| Incentive per participant | [e.g., $50 gift card / free credits / none] |
| When incentive is paid | [e.g., Within 5 days of session] |
| Diversity goals | [e.g., Mix of ages, regions, devices, abilities] |

## 7.4 Special groups
| Group | Included? | Extra rules |
|---|---|---|
| People with disabilities | [Yes/No] | See Section 14 |
| **Children / minors (under 18, or the legal age in your region)** | [Yes/No] | See Section 13.4. **Never test with a child without a parent/guardian's written consent.** |
| Non-English speakers | [Yes/No] | See Section 14.3 |

**Agent Check:** Screener exists; segment percentages add up to 100%; minors flagged if yes.

---

# 8. TEST METHODS 🔴 [REQUIRED]

Pick a method per phase. Mixed methods are expected.

| Method | What it is | Best for phases | Pros | Cons | Use? |
|---|---|---|---|---|---|
| **Moderated (live)** | Facilitator watches and asks "why" | P0, P1 | Deep insight | Slow, costly | [ ] |
| **Unmoderated remote** | Participant tests alone via tool | P1, P2, P3 | Fast, scalable | No follow-up questions | [ ] |
| **In-product feedback** | Pop-up question or button inside the real product | P4, P5 | Real behavior | Shallow answers | [ ] |
| **Think-aloud** | Participant speaks thoughts while working | P0–P3 | Reveals confusion | Can feel odd | [ ] |
| **First-click test** | Where do people click first? | P0, P1 | Quick navigation check | Limited scope | [ ] |
| **Survey (SUS, NPS, CSAT)** | Standard questionnaires | P2–P5 | Easy to compare | Self-reported | [ ] |
| **Analytics + session replay** | Watch real usage data | P4, P5 | Real at scale | Needs privacy care | [ ] |
| **Accessibility audit** | Check against WCAG | P1–P3 | Catches legal risks | Needs expertise | [ ] |
| **Interviews (short)** | 15–20 min chat | P4, P5 | Understand "why" | Time-intensive | [ ] |

## 8.1 Session format (for live sessions)
| Field | Your answer |
|---|---|
| Session length | [e.g., 45 minutes] |
| Place | [ ] Remote  [ ] In person  [ ] Both |
| Recording | [ ] Screen  [ ] Audio  [ ] Video  [ ] None (consent needed for all) |
| Observers allowed | [Max #, they stay silent and muted] |
| Language | [e.g., English] |

**Agent Check:** Every phase in Section 5 maps to at least one method here.

---

# 9. TASKS AND SCENARIOS 🔴 [REQUIRED]

Each task is a small story. **Do not tell people which button to press.** Tell them the goal only.

| Task ID | Scenario (what you read aloud) | Start screen | Success looks like | Failure looks like | Max time | Phase(s) |
|---|---|---|---|---|---|---|
| T1 | "You just downloaded the app. Create an account." | [Welcome] | [Account created, reached home] | [Gave up, needed hint, error] | [2 min] | [P0–P5] |
| T2 | "[Goal in the user's words]" | [Screen] | [Result] | [Result] | [Time] | [P#] |
| T3 | | | | | | |

**Rules for writing good tasks**
- ✅ "Find out how much you spent on food last month."
- ❌ "Click the Reports tab and select Food."
- Write 5–8 tasks per session. More than that tires people.
- Put the easiest task first and the riskiest in the middle.

**Success levels (use for every task):**
| Code | Meaning |
|---|---|
| ✅ Success | Finished with no help |
| 🟡 Partial | Finished with a hint or a detour |
| ❌ Fail | Did not finish, or finished incorrectly |
| ⛔ Abandoned | Gave up |

**Agent Check:** Every task has a measurable success and failure definition; no task names a button.

---

# 10. METRICS AND TARGETS 🔴 [REQUIRED]

## 10.1 Core metrics (pre-loaded)

| Metric | What it tells you | How to calculate | Good-enough target (edit if needed) | Phases |
|---|---|---|---|---|
| **Task success rate** | Can people do it? | Participants who succeeded ÷ total participants × 100 | ≥ 90% core tasks; ≥ 80% secondary | P0–P5 |
| **Time on task** | How long it takes | Average seconds (successful tasks only) | Within 1.25× the expert time | P1–P5 |
| **Error count** | Wrong clicks or wrong results | Errors per task | ≤ 0.5 per task | P0–P3 |
| **SEQ** (Single Ease Question) | Perceived ease per task | "Overall, how easy was this task?" 1 (very hard) – 7 (very easy). Average. | ≥ 6.0 | P1–P3 |
| **SUS** | Overall usability | Standard 10-question form, score 0–100 (not a percentage) | ≥ 72 in P2; **≥ 80 (grade A) at launch.** Note: 68 is only *average* | P2, P3, P5 |
| **CSAT** | Satisfaction | "How satisfied are you?" 1–5; % of 4s and 5s | ≥ 85% | P4, P5 |
| **NPS** | Would they recommend? | % promoters (9–10) − % detractors (0–6) | ≥ +40 early; ≥ +50 mature | P4, P5 |

**How to read a SUS score** (curved grading from Sauro & Lewis; 68 is the average across hundreds of studies):
| SUS score | Grade | Meaning |
|---|---|---|
| 84.1 or higher | A+ | Best imaginable |
| 80.8 – 84.0 | A | Excellent. **This is your launch target.** |
| 74 – 80.7 | B | Good, but below the launch bar |
| 65 – 71 | C | Average |
| 51 – 64 | D | Poor |
| Below 51 | F | Failing. Fix before continuing |

**SUS rules:** never change the wording of the 10 questions (it breaks comparison with benchmarks) · collect at least 30 responses before trusting a score · SUS tells you *how usable* it feels, not *what* is broken; use task results and the issue log for that.

## 10.2 AI-specific trust metrics (only if Section 15 applies)

| Metric | Question or method | Target |
|---|---|---|
| **Helpfulness** | "Was this AI answer helpful?" 👍 / 👎 | ≥ 80% 👍 |
| **Trust rating** | "How much do you trust this answer?" 1–5 | ≥ 4.0 |
| **Hallucination reports** | # of times a user flags a false/misleading answer ÷ total AI answers | ≤ [set your limit, e.g., 2%] |
| **Override rate** | % of times the user edits or rejects AI output | Track trend; investigate sudden jumps |
| **Recovery success** | When AI is wrong, can the user fix or retry? | ≥ 80% |
| **Safe-failure rate** | AI says "I don't know" instead of making things up | ≥ [set target] |

## 10.3 Behavior metrics for P4–P5 (live product)
| Metric | Definition | Target |
|---|---|---|
| Activation rate | % of new users who complete the key first action | [e.g., ≥ 60%] |
| Drop-off point | Screen where most people leave | [Identify top 3] |
| Support tickets per 100 users | Volume of "I'm confused" tickets | [≤ X] |
| Return rate (day 7) | % who come back in 7 days | [≥ X%] |

If unsure, write: *Keep the defaults above and change them only after your first test round.*

**Agent Check:** Every goal in Section 2.2 has at least one metric here; SUS/SEQ/Task success/NPS/CSAT present.

---

# 11. ISSUE SEVERITY AND BACKLOG HAND-OFF 🔴 [REQUIRED]

## 11.1 Severity scale (use for every problem found)

| Level | Name | Meaning | Example | Rule |
|---|---|---|---|---|
| **0** | Not a problem | Disagreement only | "I'd prefer blue." | Log it, ignore |
| **1** | Cosmetic | Noticed but no harm | Misaligned icon | Fix when convenient |
| **2** | Minor | Slows people down | Confusing label, recovered | Fix in next sprint |
| **3** | Major | Many users struggle or fail | Cannot find checkout | Fix before next phase |
| **4** | Blocker | Prevents the task, loses data/money, harms safety, or breaks the law | Payment fails; AI gives dangerous advice; inaccessible to screen reader | **Fix before ANY release** |

## 11.2 Priority formula (simple)
**Priority = Severity × How many people hit it × How easy it is to hit.**
If unsure: any Severity 4, or any Severity 3 hit by ≥ 30% of participants, is **top priority.**

## 11.3 Issue log template (one row per problem)

| Issue ID | Phase | Task | What happened (facts only) | Evidence (video time / quote / screenshot) | # of participants affected | Severity (0–4) | Suggested fix | Ticket link | Owner | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| U-001 | [P#] | [T#] | [Plain facts] | [link] | [x of y] | [#] | [Idea] | [Jira/Linear/GitHub link] | [Name] | [ ] Open  [ ] In progress  [ ] Fixed  [ ] Retested  [ ] Won't fix (reason) |

## 11.4 Hand-off to the development backlog
| Step | Who | When |
|---|---|---|
| 1. Group duplicate issues | [Analyst/AI agent drafts, human confirms] | [Within 2 days of last session] |
| 2. Assign severity | [Facilitator + PM] | [Within 3 days] |
| 3. Create tickets with label `usability` | [PM] | [Within 4 days] |
| 4. Link every ticket to the Issue ID | [PM] | [Same time] |
| 5. Retest fixed Severity 3–4 issues | [QA + Facilitator] | [Before the next phase gate] |

**Agent Check:** Issue log exists; every Severity 3–4 issue has a ticket and owner; "Won't fix" has a reason.

---

# 12. TOOLS AND MATERIALS 🔴 [REQUIRED]

| Purpose | Tool chosen | Cost | Owner | Backup tool |
|---|---|---|---|---|
| Prototype / test build | [Figma / TestFlight / Staging URL] | [$] | [Name] | [Tool] |
| Video call + recording | [Zoom / Meet / Teams] | [$] | [Name] | [Tool] |
| Unmoderated testing | [Maze / UserTesting / Lookback / other] | [$] | [Name] | [Tool] |
| Surveys | [Typeform / Google Forms / in-product] | [$] | [Name] | [Tool] |
| Analytics / session replay | [PostHog / Mixpanel / Hotjar / other] | [$] | [Name] | [Tool] |
| Notes and analysis | [Notion / Sheets / Dovetail] | [$] | [Name] | [Tool] |
| Issue tracking | [Jira / Linear / GitHub] | [$] | [Name] | [Tool] |
| Accessibility testing | [axe / Lighthouse / screen readers: NVDA, VoiceOver, TalkBack] | [$] | [Name] | [Tool] |

## 12.1 Materials checklist (prepare before each phase)
- [ ] Facilitator script (Section 12.2)
- [ ] Consent form (Section 13)
- [ ] Task cards (Section 9)
- [ ] Prototype/build link tested and working on every device
- [ ] Test accounts and sample data ready (no real customer data)
- [ ] Recording turned on and tested
- [ ] Survey links tested
- [ ] Incentive ready to send
- [ ] Note-taking template ready
- [ ] Backup device and backup internet plan

## 12.2 Facilitator script (use word for word)

**Welcome (3 min)**
> "Thank you for helping us today. I'm [name]. We are testing the product, **not you**. There are no wrong answers. If something is confusing, that is our fault, and that is exactly what we want to learn. Please think out loud as you go. I may not answer questions right away; that's normal, and I will explain at the end. You can stop at any time. With your permission, I'll record the screen and your voice so I can learn from it later. Is that okay?"

**Warm-up (3 min)**
> "Tell me a little about how you currently [do the thing the product helps with]."

**Tasks (25–35 min)**
> Read one task at a time. Do not help. If they are stuck for more than [2 minutes], say: "What would you do if I weren't here?" After [3 minutes] mark as Fail and move on.

**Neutral prompts you MAY use:** "What are you thinking?" · "What did you expect to happen?" · "What would you do next?"
**Prompts you must NOT use:** "Did you see the button?" · "Why didn't you click Save?" (these lead the person)

**Wrap-up (5 min)**
> Ask the SUS survey. Then: "What was the best part? What was the most frustrating part? Anything else?" Thank them and confirm the incentive.

---

# 13. ETHICS, PRIVACY AND CONSENT 🔴 [REQUIRED]

## 13.1 Consent form must include
- [ ] What the test is and how long it takes
- [ ] What is recorded (screen, voice, face, clicks)
- [ ] Who will see the recordings
- [ ] How long data is kept
- [ ] Right to stop at any time without losing the incentive
- [ ] How to ask for deletion of their data
- [ ] Contact person's email

## 13.2 Privacy rules (GDPR / CCPA and similar laws)
| Rule | Your answer |
|---|---|
| Legal basis / consent type | [Explicit written or digital consent] |
| Personal data collected | [Name, email, voice, screen, device info] |
| Where data is stored | [Tool + region, e.g., EU server] |
| Who can access | [Names/roles only] |
| Retention period | [e.g., Delete recordings after 12 months; keep anonymized notes] |
| Deletion request process | [How, who, within how many days; e.g., 30 days] |
| Participants' names in reports | [Never; use P1, P2, P3] |
| Real customer data in test | [Never; use fake data] |
| Data processor agreements with tools | [ ] Signed / [ ] N/A |

If unsure, write: *Ask your Legal or Privacy person to review this section before recruiting. Do not skip.*

## 13.3 AI-specific privacy
- Do **not** paste participant recordings or personal details into AI tools unless your company has approved that tool and the participant consented.
- Redact names, emails, and faces before an AI agent summarizes any session.

## 13.4 Children and minors 🟡 [REQUIRED if any participant is under 18]
| Rule | Your answer |
|---|---|
| Age limit in your region | [e.g., under 18; some places under 16] |
| Written parent/guardian consent | [Required before any session] |
| Child's own agreement ("assent") in simple words | [Required] |
| Parent/guardian present during session | [Yes / within sight] |
| Session length | [Shorter, e.g., 20–30 min] |
| Extra laws to check | [COPPA (US, children **under 13**): the amended rule is now fully in force, with its compliance deadline of 22 April 2026 passed. It adds stricter parental-consent rules, covers biometric identifiers (a child's voice or face in a recording may count), and requires a written data-retention policy and security program. Also check GDPR rules for children, other national laws, and, for AI features, the EU AI Act. **Ask Legal. Do not guess.**] |
| Recordings of minors | [Default: do NOT record faces or voices unless Legal approves; use screen + notes only] |
| No sensitive questions | [Confirmed] |
| Stop rule | [Stop instantly if child is upset or tired] |

**Agent Check:** Consent items all ticked; retention period set; minors rules filled or `N/A – no minors`.

---

# 14. ACCESSIBILITY AND INCLUSION 🔴 [REQUIRED]

## 14.1 Standard to meet
| Field | Your answer |
|---|---|
| Target standard | [WCAG 2.2 Level AA] |
| Platforms | [Web / iOS / Android] |

## 14.2 Accessibility checklist (test in P1–P3)
- [ ] All images have text descriptions (alt text)
- [ ] The whole product works with **keyboard only**
- [ ] Works with screen readers (NVDA, JAWS, VoiceOver, TalkBack)
- [ ] Text contrast is at least 4.5:1 (normal text)
- [ ] Text can zoom to 200% without breaking
- [ ] Nothing depends on color alone
- [ ] Touch targets: **at least 24×24 CSS px is the WCAG 2.2 AA minimum; aim for 44×44 px on mobile (best practice)**
- [ ] Videos have captions; audio has transcripts
- [ ] Animations can be reduced or turned off
- [ ] Error messages are clear and read out by screen readers
- [ ] Forms have labels, and users can fix mistakes
- [ ] AI responses are readable by screen readers and not time-limited

**New in WCAG 2.2 (Level A / AA). Test these too:**
- [ ] 2.4.11 Focus Not Obscured: the keyboard focus is never hidden behind sticky headers, banners, or chat widgets
- [ ] 2.5.7 Dragging Movements: anything done by dragging can also be done with a simple click or tap
- [ ] 2.5.8 Target Size (Minimum): see the 24×24 px rule above
- [ ] 3.2.6 Consistent Help: help or contact options appear in the same place on every page
- [ ] 3.3.7 Redundant Entry: users never have to type the same information twice in one process
- [ ] 3.3.8 Accessible Authentication (Minimum): login does not require solving a puzzle or remembering/typing codes without alternatives (paste and password managers work)

## 14.3 Language and region (global)
| Field | Your answer |
|---|---|
| Languages supported at launch | [e.g., English, Spanish] |
| Languages tested | [Which and by whom: native speakers only] |
| Things to check | [Text length breaking layout, right-to-left layouts, date/time/currency formats, names and address forms, cultural icons/colors, tone of AI replies] |
| Regions tested | [e.g., US, EU, India] |

## 14.4 Participants with disabilities
| Field | Your answer |
|---|---|
| Minimum number | [At least 10–15% of participants, or 3+ per phase] |
| Types included | [ ] Vision  [ ] Hearing  [ ] Motor  [ ] Cognitive  [ ] Other |
| Extra support offered | [Longer sessions, own device allowed, sign-language interpreter, etc.] |

**Agent Check:** Standard named; checklist items tested or marked with a reason; at least one accessibility participant planned.

---

# 15. AI-POWERED PRODUCT TESTING 🟡 [REQUIRED if product uses AI; otherwise write `N/A – no AI features`]

## 15.1 AI feature inventory
| Feature | What the AI does | Risk if wrong | Human can override? |
|---|---|---|---|
| [e.g., Chat assistant] | [Answers budget questions] | [Bad financial advice] | [Yes] |

## 15.2 AI-specific things to test
| Area | What to check | How to test | Pass rule |
|---|---|---|---|
| **Clarity** | Do users know it's AI? | Ask "Who wrote this answer?" | ≥ 90% say "AI" |
| **Expectations** | Do users understand what it can/can't do? | Ask before and after | Mismatch ≤ [X]% |
| **Accuracy** | Are answers correct? | Review [N] sample answers with experts | ≥ [X]% correct |
| **Hallucination handling** | What if AI invents facts? | Seed tricky questions | Users notice ≥ [X]% or AI admits uncertainty |
| **Trust calibration** | Do users trust it the right amount? | Trust rating vs correctness | No big gap |
| **Error recovery** | Can users fix or retry? | Task: "Get a better answer." | ≥ 80% succeed |
| **Control** | Can users edit, undo, turn off AI? | Task: "Turn off suggestions." | ≥ 90% succeed |
| **Safety** | Does it refuse harmful requests politely? | Red-team prompts | 100% safe refusals |
| **Bias and fairness** | Same quality for all groups? | Compare across segments | No significant gap |
| **Tone** | Helpful, respectful, consistent? | Rate by participants | ≥ 4/5 |
| **Speed** | Does waiting feel OK? | Time to first response | ≤ [X] seconds |
| **Privacy** | Does the AI reveal others' data? | Probe prompts | 0 leaks |
| **Transparency** | Sources, explanations, "why this answer" | Task: "Find where this came from." | ≥ [X]% succeed |
| **Calibration gap** | Does trust match real accuracy? | Check each AI answer against an expert-verified correct answer **before** the session (ground truth). Compare each participant's trust rating with correctness. | Trust on correct answers ≥ 4/5; trust on wrong answers ≤ 2/5 (users notice errors) |
| **Variability** | Does the AI give different answers to the same question? | Run each key prompt at least 3 times; compare | No harmful or contradictory answers; differences explained to users |
| **Real outputs, not mockups** | Participants see real model answers | Use the real model (or a Wizard-of-Oz setup in P0 only) | Any "mock" test is labelled as such in the report |
| **Reliance over time** | Does trust change after a failure? | Interview 8–12 users after they see an AI error; re-measure at day 30, 60, 90 live | Trust recovers within [X] sessions |

## 15.3 AI test prompt set
| Prompt ID | Type | Prompt | Expected behavior | Result |
|---|---|---|---|---|
| A-01 | Normal | [Typical question] | [Helpful, correct] | |
| A-02 | Tricky | [Ambiguous question] | [Asks to clarify] | |
| A-03 | Unknown | [Question it can't know] | [Says "I don't know"] | |
| A-04 | Risky | [Asks for harmful help] | [Refuses safely, offers alternatives] | |
| A-05 | Personal data | [Asks about someone else's data] | [Refuses] | |

## 15.4 AI model changes
> Every time the AI model, prompt, or settings change, rerun the AI prompt set and at least tasks [T#] before release.

| Date | Change | Retest done? | Result |
|---|---|---|---|
| [date] | [Model/prompt update] | [ ] | [Pass/Fail] |

**Agent Check:** Feature inventory present; every feature has risk and override; prompt set has ≥ 5 prompts; retest rule defined.

---

# 16. SAMPLE SIZE AND BUDGET 🔴 [REQUIRED]

## 16.1 Sample size guide (if unsure, use these)
| Goal | Suggested participants |
|---|---|
| Find big problems in a design (qualitative) | **5 per user group** (3–7 is the range); run several small rounds instead of one big test. If your segments behave very differently, test about 3–5 in each. |
| Compare scores with confidence (quantitative) | **At least 20**; more if you need tight confidence limits |
| Card sorting | At least 15 per user group |
| Survey-based measures (SUS, NPS) | 30+ to trust a score; 30–50 per release when tracking over time |
| AI trust-calibration interviews | 8–12 target users |
| Accessibility | 3+ per disability type if possible |

## 16.2 Budget
| Item | Phase | Cost per unit | Quantity | Total |
|---|---|---|---|---|
| Incentives | [P#] | [$] | [#] | [$] |
| Recruitment panel fees | | | | |
| Tools / licenses | | | | |
| Translators / interpreters | | | | |
| Accessibility audit | | | | |
| Facilitator time | | | | |
| Contingency (add 10–15%) | | | | |
| **Grand total** | | | | **[$]** |

**Agent Check:** Math adds up; contingency present.

---

# 17. DATA COLLECTION AND ANALYSIS 🔴 [REQUIRED]

## 17.1 Note-taking template (one per session)
| Field | Notes |
|---|---|
| Session ID / participant ID (P1, P2…) | |
| Date, phase, facilitator, note-taker | |
| Segment / device | |
| Task results (T1 ✅/🟡/❌/⛔ + time) | |
| Quotes (exact words, with timestamps) | |
| Problems seen (facts only) | |
| Surprises | |
| SUS / SEQ / other scores | |

## 17.2 Analysis steps
1. Within 24 hours of each session: finish notes and upload recordings to the secure folder.
2. After all sessions in a phase: tally task success, time, errors, SEQ, and SUS.
3. Group problems that look alike (affinity grouping).
4. Assign severity (Section 11).
5. Write the phase report (Section 19).
6. Share within [3] working days.

## 17.3 Rules for honest results
- Report **numbers and quotes**, not opinions.
- Show bad news and good news.
- Do not remove a problem because "that participant was unusual." Write it down and mark it as one case.
- AI agents may summarize, but a human must check every finding against the recording.

**Agent Check:** Template present; analysis steps have time limits; human verification rule stated.

---

# 18. LAUNCH SUPPORT AND FIRST-500-CUSTOMERS MONITORING 🔴 [REQUIRED]

## 18.1 In-product feedback setup
| Item | Your answer |
|---|---|
| Feedback button location | [e.g., Settings and every error screen] |
| Quick question after key task | [SEQ-style: "How easy was that?"] |
| SUS timing | [After day 7 for customers 1–500, sample the first 100 + each following 100] |
| NPS timing | [Day 14 and day 60] |
| CSAT timing | [After support interaction and after first key task] |
| AI answer feedback | [👍 / 👎 + optional reason] |

## 18.2 Customer milestone checkpoints
| Checkpoint | Customers reached | Review meeting date | What we check | Action if bad |
|---|---|---|---|---|
| C1 | 10 | [date] | Any crash, blocker, or confusion on first use | Fix within 24–48 hrs |
| C2 | 50 | [date] | Task success on key flows, top 3 drop-offs | Hotfix + retest |
| C3 | 100 | [date] | Activation, CSAT, support tickets | Update backlog; run P5 plan |
| C4 | 250 | [date] | SUS, NPS, retention, AI trust metrics | Targeted tests on weak areas |
| C5 | 500 | [date] | Full review; compare with P2/P3 results | Final report + next-plan decision |

## 18.3 Re-test triggers (test again if any of these happen)
- [ ] Task success drops by more than 10 points
- [ ] Support tickets about the same issue exceed [X] per week
- [ ] A Severity 4 issue is reported
- [ ] A major redesign or new feature ships
- [ ] The AI model or prompt changes
- [ ] A new platform, region, or language launches
- [ ] SUS drops below [75]

**Agent Check:** All five milestones scheduled; triggers listed.

---

# 19. REPORTING 🔴 [REQUIRED]

## 19.1 Phase report template (1–2 pages)
| Section | Content |
|---|---|
| 1. Summary | 3 sentences: what we tested, top finding, decision |
| 2. Who | Number and types of participants |
| 3. Scores | Task success, time, SEQ, SUS, (NPS/CSAT), AI metrics vs targets (green/yellow/red) |
| 4. Top 5 problems | Issue ID, severity, # affected, evidence link |
| 5. What worked well | At least 3 items |
| 6. Recommendations | Fix list ordered by priority |
| 7. Go / No-Go | Decision from Section 21 |
| 8. Next steps | Owner + date |

## 19.2 Who gets reports
| Audience | Format | When |
|---|---|---|
| Product team | Full report + issue log | Within 3 days |
| Leadership | One-page summary | Within 5 days |
| Customers/public (optional) | "You said, we did" update | After fixes ship |

## 19.3 Final report after customer #500
Includes: all phase results, trend charts, issues found vs fixed, lessons learned, and recommendations for the next plan.

**Agent Check:** Template used for every phase; leadership summary exists.

---

# 20. RISKS AND BACKUP PLANS 🔴 [REQUIRED]

| # | Risk | Chance (Low/Med/High) | Impact (Low/Med/High) | What we will do | Owner |
|---|---|---|---|---|---|
| 1 | Too few participants show up | [Med] | [High] | Recruit 20% extra; have a standby list | [Name] |
| 2 | Prototype/build crashes during a session | [Med] | [High] | Test link 1 hour before; have a backup device and recording of a working flow | [Name] |
| 3 | Recording fails | [Low] | [Med] | Use a second recorder; take written notes | [Name] |
| 4 | Privacy mistake (data leak) | [Low] | [High] | Follow Section 13; report incidents within 24 hrs to [Name] | [Name] |
| 5 | AI gives harmful or wrong answer to participant | [Med] | [High] | Facilitator stops the task, explains, logs as Severity 4 | [Name] |
| 6 | Schedule slips | [Med] | [Med] | Keep a buffer of [1 week] per phase | [Name] |
| 7 | Results are biased (wrong participants) | [Med] | [High] | Re-check screeners; add a segment | [Name] |
| 8 | Budget overrun | [Low] | [Med] | 10–15% contingency; weekly check | [Name] |
| 9 | [Your risk] | | | | |

**Agent Check:** Every risk has an owner and an action; top risks (High impact) reviewed weekly.

---

# 21. GO / NO-GO LAUNCH GATES 🔴 [REQUIRED]

> **Only humans decide.** The Product Manager (the `A` in Section 6) signs. AI agents may prepare data but never approve.

## 21.1 Gate rules (edit numbers if needed)

| Gate | Moving from → to | Must be true to pass |
|---|---|---|
| **G0** | P0 → P1 | ≥ 85% of participants understand the idea; 0 open Severity 4; main flow validated |
| **G1** | P1 → P2 | Core task success ≥ 85%; 0 open Severity 4; ≤ 2 open Severity 3 with fix plans; accessibility basics checked |
| **G2** | P2 → P3 | Core task success ≥ 90%; SUS ≥ 72; SEQ ≥ 6.0; 0 Severity 4; AI trust ≥ 4.0, calibration-gap check passed, and 0 safety failures |
| **G3 (Launch)** | P3 → P4 | Core task success ≥ 95%; **SUS ≥ 80**; 0 Severity 4 and 0 Severity 3 on key flows; WCAG 2.2 AA checklist passed; privacy/legal sign-off done (incl. minors rules if relevant); design-system checks passed (Section 26); support team trained; rollback plan ready |
| **G4** | P4 → P5 (after customer 100) | CSAT ≥ 80%; activation ≥ target; no unresolved Severity 4; feedback loop working |
| **G5 (Final)** | After customer 500 | SUS ≥ 82; NPS ≥ +40; CSAT ≥ 85%; trend stable or improving; final report delivered |

## 21.2 Decision log
| Gate | Date | Decision | Conditions (if any) | Approver | Signature/initials |
|---|---|---|---|---|---|
| [G#] | [date] | [ ] Go  [ ] Go with conditions  [ ] No-Go | [Text] | [Name] | |

**Agent Check:** Each gate has numeric rules; every decision has a human approver; no agent listed as approver.

---

# 22. QUICK EXAMPLE SNIPPETS ⚪ [OPTIONAL – DELETE BEFORE SHARING IF NOT NEEDED. A full example is in Section 28.]

> **Tiny example, Section 2.2 for "Acme Budget App":**
> | G1 | New users can create an account | Task success rate | ≥ 90% |
> | G2 | Users can add an expense | Time on task | ≤ 30 seconds |
> | G3 | Users trust the AI savings tips | Trust rating 1–5 | ≥ 4.0 |
>
> **Example task (Section 9):** "You just bought lunch for $12. Record it." → Success: expense appears in list; Fail: cannot find add button; Max time 60 seconds.
>
> **Example issue (Section 11.3):** U-001 · P1 · T2 · "5 of 8 participants tapped the logo instead of the + button." · Severity 3 · Fix: make + button larger and add label.

---

# 23. PRE-FLIGHT CHECKLIST (BEFORE YOU APPROVE THE PLAN) 🔴 [REQUIRED]

- [ ] Section 0: one owner named, dates filled
- [ ] Section 1: paragraph written in plain words
- [ ] Section 2: every goal has a number
- [ ] Section 3: in-scope and out-of-scope both listed
- [ ] Section 5: all six phases filled (or skipped with reason)
- [ ] Section 6: each activity has exactly one `A`
- [ ] Section 7: screener ready, minors/disability groups addressed
- [ ] Section 9: tasks do not tell people where to click
- [ ] Section 10: SUS, SEQ, success, time, NPS, CSAT defined
- [ ] Section 11: severity scale and issue log ready
- [ ] Section 13: consent form and privacy rules reviewed by Legal
- [ ] Section 14: accessibility standard picked
- [ ] Section 15: AI testing filled or `N/A`
- [ ] Section 16: budget adds up
- [ ] Section 18: first-500-customers checkpoints scheduled
- [ ] Section 20: top risks have owners
- [ ] Section 21: gate rules agreed by Product Manager
- [ ] Section 26: design-system checks filled or `N/A – no design system`
- [ ] No `[bracket]` or `TBD` remains without owner and date
- [ ] Plan approved in Section 24

**Final Agent Check (copy and give to an AI agent):**
> "Read the whole file. Return: (1) a list of every unfilled `[bracket]`; (2) every `TBD` missing owner/date; (3) any section tagged REQUIRED that is empty; (4) any goal without a metric; (5) any Go/No-Go gate without numeric rules; (6) any place where an AI agent is listed as an approver. Do not rewrite my answers."

---

# 24. APPROVAL 🔴 [REQUIRED]

| Role | Name | Decision | Date | Signature/initials |
|---|---|---|---|---|
| Plan owner | | [ ] Approve  [ ] Changes needed | | |
| Product manager | | [ ] Approve  [ ] Changes needed | | |
| Design lead | | [ ] Approve  [ ] Changes needed | | |
| Engineering lead | | [ ] Approve  [ ] Changes needed | | |
| Legal / privacy | | [ ] Approve  [ ] Changes needed | | |

---

# 25. CHANGE LOG AND VERSION HISTORY 🔴 [REQUIRED]

> Every time you edit this plan after approval, add a row. Never delete old rows.

| Version | Date | Author | What changed | Why | Approved by |
|---|---|---|---|---|---|
| v0.1 | [YYYY-MM-DD] | [Name] | First draft | New plan | |
| v1.0 | [YYYY-MM-DD] | [Name] | Approved version | | [Name] |

**Version rule:** Small fix (typo, date) = `v1.0 → v1.1`. Big change (new phase, new goal, new gate rule) = `v1.0 → v2.0` and needs re-approval.

---

# 26. DESIGN-SYSTEM CHECKS 🟡 [RECOMMENDED – write `N/A – no design system` if you have none]

> Goal: make sure the buttons, colors, forms, and AI chat pieces that you reuse across projects are easy to use **everywhere**, so one fix helps all your projects.

## 26.1 Design system in use
| Field | Your answer |
|---|---|
| Design system name and version | [e.g., Acme DS v3.2] |
| Library link (Figma / Storybook / code repo) | [link] |
| Design-system owner | [Name] |
| Custom pieces made just for this project (not in the system) | [List them. Each one is a candidate to add to the system.] |

## 26.2 Token checks (colors, spacing, type)
| Check | How to test | Pass rule | Result |
|---|---|---|---|
| Color contrast of every text/background pair | Contrast checker | ≥ 4.5:1 for normal text, ≥ 3:1 for large text and UI borders | [ ] Pass  [ ] Fail |
| Colors never carry meaning alone | Look at it in grayscale | Meaning still clear | [ ] |
| Type scale readable on small phones | Test on the smallest supported device | Body text ≥ 16 px; no horizontal scrolling | [ ] |
| Spacing and tap-target sizes | Check on real devices | See Section 14.2 | [ ] |
| Dark mode / high-contrast mode (if offered) | Run the same tasks | Same success rate as light mode | [ ] |

## 26.3 Component checks (copy one row per component used in your key tasks)
| Component | States tested (default, hover, focus, pressed, disabled, error, loading, empty) | Used in tasks | Participants who struggled | Issue ID | Decision |
|---|---|---|---|---|---|
| [e.g., Primary button] | [all 8] | [T1, T3] | [0 of 8] | [none] | [ ] Keep  [ ] Fix in system  [ ] Fix locally  [ ] Retire |
| [e.g., Form field + error message] | [default, focus, error] | [T1] | [3 of 8] | [U-004] | [ ] Keep  [ ] Fix in system |
| [e.g., AI chat message + feedback buttons] | [loading, streaming, answer, error, "I don't know"] | [T5] | [2 of 8] | [U-007] | [ ] Keep  [ ] Fix in system |

## 26.4 Consistency checks
- [ ] The same action looks and is named the same everywhere (e.g., always "Save", never "Save" on one screen and "Submit" on another)
- [ ] Error, success, and loading messages follow one pattern
- [ ] Navigation works the same on web and mobile (where possible)
- [ ] Icons are labeled or have a tooltip/accessible name
- [ ] AI features use the same patterns: a clear "AI" label, a way to give feedback, a way to retry, a way to turn off, and a way to see sources

## 26.5 What happens with the results
| Finding type | Action | Who decides | When |
|---|---|---|---|
| A component failed for many users | Open a ticket in the design-system backlog; fix once, benefit everywhere | Design-system owner | Before the next release of the system |
| A custom piece worked very well | Propose adding it to the system | Design-system owner + Designer | Next system review |
| A custom piece failed | Replace it with the system component or fix it locally | Designer | Before the next phase gate |
| A fix changes a system component | Retest other projects that use it (use Project ID tags in Section 0) | Plan owner | Within 2 weeks |

**Agent Check:** Version named; every component used in a key task has a row; every failed component has an issue ID and decision.

---

# 27. AI AGENT PROMPT LIBRARY 🟡 [RECOMMENDED]

> **How to use:** copy a prompt, replace `<...>`, and paste it into your AI agent together with this file.
> **Rules for every prompt:** (1) Never paste real participant names, emails, faces, or recordings into an AI tool unless your company approved that tool and the participant consented. (2) The agent drafts; **a human checks every result**. (3) The agent never approves a Go/No-Go (Section 21).

| # | When | Prompt (copy this) |
|---|---|---|
| A1 | Before starting | "Read the whole file. List every `[bracket]` still unfilled, every `TBD` without owner and date, every empty REQUIRED section, and every goal without a metric. Do not rewrite my answers." |
| A2 | Section 1–2 | "Using my Product Snapshot (Section 4) and business goal, suggest 3–5 measurable usability goals and 5 research questions. Show them in the Section 2 table format. Every goal needs a number target." |
| A3 | Section 7 | "Draft 8 screening questions for these segments: <segments>. For each, give the qualifying answer and the disqualifying answer. Avoid leading questions. Do not ask for sensitive personal data." |
| A4 | Section 9 | "Write <5–8> task scenarios for these user journeys: <journeys>. Rules: describe the goal in the user's words, never name a button or menu, and give success/failure definitions and a max time." |
| A5 | Section 12.2 | "Create a facilitator script for a <45>-minute session testing <product>. Use neutral prompts only (no leading questions), include a welcome, warm-up, tasks, and wrap-up." |
| A6 | Section 13 | "Draft a plain-language consent form (reading level: age 12) covering recording, data use, retention (<period>), the right to stop, and deletion requests. Flag items my Legal team must check." |
| A7 | After sessions | "Here are anonymized notes from <N> sessions (no names). Group the problems that look alike, count how many participants hit each one, and propose a severity (0–4) using Section 11. Quote evidence by participant ID and timestamp. Mark anything you are unsure about." |
| A8 | After sessions | "Calculate task success rate, average time on task, and average SEQ per task from this data. Then compare each result with the targets in Section 10 and mark green/yellow/red." |
| A9 | SUS | "Score these SUS responses with the standard method (odd items: score−1; even items: 5−score; add up; ×2.5). Show the average score, the grade from the Section 10 table, and how many responses you used." |
| A10 | AI products | "For these AI answers and their verified correct answers, and these participant trust ratings, calculate the calibration gap (trust on correct vs wrong answers) and list the answers where users trusted a wrong answer." |
| A11 | Reporting | "Write the phase report using the Section 19.1 template from these results. Keep it to 2 pages. Include what worked well. Do not hide bad news." |
| A12 | Gate | "Prepare a Go/No-Go evidence pack for gate <G#>: for each rule in Section 21, show the result, pass/fail, and the evidence link. Do not make the decision; the Product Manager decides." |
| A13 | Hand-off | "Turn each Severity 3–4 issue in the issue log into a ticket with title, steps to reproduce, expected vs actual, evidence link, and acceptance test." |
| A14 | Final check | "Run the Section 23 checklist and report each unchecked item." |

---

# 28. FULLY WORKED EXAMPLE (FICTIONAL PRODUCT) ⚪ [OPTIONAL – read it to see what "good" looks like, then delete it from your own copy]

> This is a shortened, filled-in sample for a made-up product. Your real plan fills **every** section.

**Product:** *PennyPal* — a mobile + web budgeting app with an AI assistant ("Penny") that answers spending questions.

### Section 0 (Document control)
| Field | Answer |
|---|---|
| Project name / ID | PennyPal v1 / PRJ-2026-0042 |
| Product type | Mobile (iOS/Android), web, AI feature |
| Owner | Maya Lopez, UX Research Lead |
| Priority / risk tier | P1 Critical / High (money + AI advice) |
| Tags | mobile, web, ai, fintech |
| Design system | PennyUI v2.4 |
| Status / version | Approved / v1.0 |

### Section 1 (Plan in one paragraph)
We will test **PennyPal's sign-up, expense tracking and the Penny AI assistant** with **6 people per phase early on, growing to 150 in open beta**, who are **adults aged 18–45 who track money on a phone or spreadsheet**, during **six phases from prototype to customer 500**, to find out whether they can **record an expense in under 30 seconds and trust Penny's answers correctly**. We will launch when **task success is at least 95%, SUS is at least 80, and there are no Severity 3–4 issues on key flows**. The plan runs from **2026-11-02 to 2027-05-28**.

### Section 2.2 (Goals)
| # | Goal | Measure | Target |
|---|---|---|---|
| G1 | New users create an account | Task success | ≥ 95% |
| G2 | Users add an expense quickly | Time on task | ≤ 30 s |
| G3 | Users trust Penny the right amount | Trust on correct answers / on wrong answers | ≥ 4 / ≤ 2 (of 5) |

### Section 5 (Phases, abbreviated)
| Phase | Dates | Participants | Method |
|---|---|---|---|
| P0 Prototype | Nov 2–13 | 6 (Figma) | Moderated, think-aloud |
| P1 Alpha | Dec 7–18 | 8 | Moderated + unmoderated |
| P2 Closed beta | Jan 11–29 | 30 | Unmoderated + SUS |
| P3 Open beta | Feb 15–Mar 12 | 120 | Unmoderated + accessibility audit |
| P4 Launch (1–100) | Mar 29–Apr 23 | first 100 | In-product feedback + 10 interviews |
| P5 Growth (101–500) | Apr 26–May 28 | next 400 | SUS/NPS/CSAT + analytics |

### Section 7 (Participants, abbreviated)
S1 first-time budgeters 18–25 (40%) · S2 spreadsheet users 26–45 (30%) · S3 assistive-technology users (15%) · S4 non-native English speakers (15%). Incentive: $50 gift card within 5 days. Minors: **No** (age 18+ only, so Section 13.4 = `N/A – 18+ only`).

### Section 9 (Tasks, 3 of 6 shown)
| ID | Scenario | Success | Failure | Max time |
|---|---|---|---|---|
| T1 | "You just downloaded PennyPal. Create an account." | Account created, home screen reached | Gave up or needed a hint | 2 min |
| T2 | "You bought lunch for $12. Record it." | Expense in the list with correct amount | Cannot find how, wrong amount | 60 s |
| T5 | "Ask Penny how much you spent on food last month." | Reads a correct answer and says what it means | Misreads or accepts a wrong answer | 3 min |

### Section 11.3 (One issue logged)
| U-001 | P1 | T2 | 5 of 8 participants tapped the logo instead of the "+" button | video 12:41, P3, P5 | 5 of 8 | **3** | Make "+" larger, add the label "Add expense" | PP-212 | Dev: Ravi | In progress |

### Section 15.2 (One AI check)
Calibration: 10 Penny answers were verified by a finance expert first (8 correct, 2 wrong). Results in P2: average trust 4.3 on correct answers, **3.9 on wrong answers** → fails the "≤ 2" rule → fix: show "How sure am I?" and sources on every answer; **retest before G2.**

### Section 21.2 (One decision logged)
| G1 | 2026-12-21 | Go with conditions | Fix U-001 and U-004 before P2 starts | Maya Lopez (PM sign-off: Dev Patel) | M.L. |

---

# 29. REFERENCES AND FURTHER READING ⚪ [OPTIONAL]

**Sources checked when this template was last reviewed (October 2026). Re-check yearly, especially laws.**
- Nielsen Norman Group, *How Many Test Users in a Usability Study?* (5 per group for qualitative studies; at least 20 for quantitative studies; 15 per group for card sorting)
- MeasuringU / Jeff Sauro & James Lewis, *Quantifying the User Experience* and the SUS pages (average SUS is about 68; scores of about 80 and above are grade A)
- W3C, *What's New in WCAG 2.2* (published 5 October 2023; Target Size Minimum is 24×24 CSS px)
- FTC, amended COPPA Rule (effective June 2025; compliance deadline 22 April 2026). Not legal advice; ask Legal.
- Industry guidance on AI product research (trust calibration, ground-truth checks, testing real model outputs). These are practitioner sources, so treat as good practice, not law.

**More reading:**

- Nielsen Norman Group: usability testing guides and the "5 users" research
- Jakob Nielsen's 10 usability heuristics
- System Usability Scale (SUS) scoring guide: usability.gov
- W3C WCAG 2.2: w3.org/WAI/standards-guidelines/wcag
- Google PAIR *People + AI Guidebook*
- Microsoft *Guidelines for Human-AI Interaction*
- Steve Krug, *Don't Make Me Think* and *Rocket Surgery Made Easy*
- GDPR (gdpr.eu), CCPA (oag.ca.gov/privacy/ccpa), COPPA (ftc.gov)

*End of template. Keep this footer: Template version T-1.0 · Owner: [Your name/team].*
