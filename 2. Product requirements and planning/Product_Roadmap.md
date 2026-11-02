# 📌 Product Roadmap Template
### AI-Driven Development Life Cycle | From First Idea to First 500 Customers
**Version:** 1.0 | **Last Updated:** `YYYY-MM-DD` | **Owner:** `Your Name`

---

<!--
╔══════════════════════════════════════════════════════════════════╗
║          👋 HOW TO USE THIS TEMPLATE                            ║
╠══════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  STEP 1 — Read the instructions at the top of EACH section.     ║
║           They are in gray comment blocks like this one.        ║
║                                                                  ║
║  STEP 2 — Replace every placeholder that looks like             ║
║           [THIS] or `YYYY-MM-DD` or "Example: ..." with         ║
║           your real information.                                 ║
║                                                                  ║
║  STEP 3 — Delete any row or section you don't need.             ║
║           This template is a menu, not a checklist.             ║
║                                                                  ║
║  STEP 4 — Keep it SHORT and HONEST. A roadmap is a             ║
║           living document. Update it every 2 weeks.             ║
║                                                                  ║
║  STEP 5 — Share it with your team. Ask: "Does this make         ║
║           sense if you read it for the first time?"             ║
║                                                                  ║
║  💡 TIP: If you're using Claude, paste a section and ask:       ║
║     "Help me fill this out based on my product idea: [idea]"    ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
-->

---

## 📋 Table of Contents

| # | Section | Purpose |
|---|---------|---------|
| 1 | [Product Snapshot](#1-product-snapshot) | One-page summary anyone can understand |
| 2 | [Vision & Strategy](#2-vision--strategy) | The big "why" behind the product |
| 3 | [Target Users & Problem Statement](#3-target-users--problem-statement) | Who you're building for and what pain you solve |
| 4 | [Goals & Success Metrics](#4-goals--success-metrics) | How you'll know you've won |
| 5 | [Phases of Development](#5-phases-of-development) | Your journey from idea → 500 customers |
| 6 | [Feature Planning & Prioritization](#6-feature-planning--prioritization) | What gets built, in what order, and why |
| 7 | [AI Dev Workflow](#7-ai-dev-workflow-how-ai-helps-you-build) | How AI tools power your development process |
| 8 | [In-Product AI Agent Design](#8-in-product-ai-agent-design-canvas) | Blueprint for every AI agent inside your product |
| 9 | [Technical Architecture](#9-technical-architecture) | The tech stack and how pieces connect |
| 10 | [Budget & Cost Tracking](#10-budget--cost-tracking) | AI costs, infra, tools, and marketing spend |
| 11 | [Risk Register](#11-risk-register) | What could go wrong and how you'll handle it |
| 12 | [Go-To-Market Strategy](#12-go-to-market-strategy) | How you'll reach your first 500 customers |
| 13 | [Quality Assurance Standards](#13-quality-assurance-standards) | How you ensure what ships actually works |
| 14 | [Customer Milestone Tracker](#14-customer-milestone-tracker-0--500) | Your real-time journey from 0 to 500 |
| 15 | [Revision History](#15-revision-history) | A log of every meaningful update to this doc |
| 16 | [Team & Roles](#16-team--roles) | RACI chart, responsibilities, when to hire |
| 17 | [Legal & Compliance](#17-legal--compliance-checklist) | Pre-launch checklist, data map, AI compliance |
| C | [Worked Example: TaskAI](#appendix-c--worked-example-taskai-) | Fully filled-out fictional product to guide you |

---

## 1. Product Snapshot

<!--
  🟡 INSTRUCTIONS — Section 1: Product Snapshot
  ─────────────────────────────────────────────
  Think of this as your product's "ID card." Fill in each field below
  in plain, simple language. Avoid jargon — if your 10-year-old cousin
  wouldn't understand it, rewrite it.

  "One-line pitch" = what your product does, for whom, and the #1 benefit.
  Example: "Notion for plumbers — lets field crews log jobs on mobile without paperwork."
-->

| Field | Your Answer |
|-------|-------------|
| **Product Name** | `[Name of your product]` |
| **One-Line Pitch** | `[What it does, who it's for, and the #1 benefit — in one sentence]` |
| **Product Type** | ☐ SaaS Web App &nbsp; ☐ Mobile App (iOS) &nbsp; ☐ Mobile App (Android) &nbsp; ☐ Both |
| **Current Status** | ☐ Just an Idea &nbsp; ☐ Prototyping &nbsp; ☐ In Development &nbsp; ☐ Beta &nbsp; ☐ Live |
| **Document Owner** | `[Your name / GitHub username]` |
| **Target Launch Date** | `YYYY-MM-DD` |
| **Primary AI Tool** | ☑ Claude (Anthropic) &nbsp; ☐ GPT-4 &nbsp; ☐ Gemini &nbsp; ☐ Other: `__________` |
| **Primary Dev Environment** | `[Cursor / Windsurf / VS Code / Replit / etc.]` |
| **Hosting Platform** | `[Vercel / Railway / Supabase / AWS / etc.]` |
| **Target Customer Count** | `500 paying or active users by [Target Date]` |

---

## 2. Vision & Strategy

<!--
  🟡 INSTRUCTIONS — Section 2: Vision & Strategy
  ────────────────────────────────────────────────
  Answer the big "why" questions here. Don't overthink it.
  Write like you're explaining this to a smart friend over coffee.

  PRODUCT VISION = Where are you going? What does the world look like
                   when your product succeeds?

  MISSION        = How will you get there? What is your team's daily job?

  NORTH STAR     = ONE number that, if it grows, everything is going well.
                   Examples: "Weekly Active Users", "Revenue", "Hours Saved"

  UNIQUE ANGLE   = Why will customers choose YOU over competitors?
-->

### 2.1 Product Vision

> **Fill in:** Complete the sentence below. Delete the examples.
>
> *"In [2–5 years], [target user] will use [Product Name] to [do something better/faster/cheaper], making [old painful way] completely obsolete."*

`[Write your vision statement here]`

---

### 2.2 Mission Statement

> **Fill in:** What does your product do every day for users?
>
> *"[Product Name] helps [target user] [achieve specific outcome] by [method/approach]."*

`[Write your mission statement here]`

---

### 2.3 North Star Metric

<!--
  Pick ONLY ONE metric that best represents your product's health.
  More = diluted focus. The table below shows examples — delete all but yours.
-->

| Your North Star Metric | Target by Customer 500 |
|------------------------|------------------------|
| `[e.g., Weekly Active Users]` | `[e.g., 500 WAU with 40% retention]` |

---

### 2.4 Strategic Bets (What You're Betting On)

<!--
  List 2–4 big assumptions your entire strategy depends on.
  These are not risks — they're the things you BELIEVE are true.
  Example: "We believe solo founders will pay $29/mo for a tool that saves 5 hrs/week."
-->

| # | Strategic Bet | Why You Believe It |
|---|--------------|-------------------|
| 1 | `[Bet 1]` | `[Evidence or reasoning]` |
| 2 | `[Bet 2]` | `[Evidence or reasoning]` |
| 3 | `[Bet 3]` | `[Evidence or reasoning]` |

---

## 3. Target Users & Problem Statement

<!--
  🟡 INSTRUCTIONS — Section 3: Target Users & Problem Statement
  ──────────────────────────────────────────────────────────────
  Before you build anything, you must be obsessively clear about:
  (A) WHO you are building for — their job, frustrations, habits
  (B) WHAT problem they have RIGHT NOW (not a hypothetical one)
  (C) HOW they solve it today (and why that's painful)
  (D) WHAT your product does differently

  USER PERSONA = A fictional-but-realistic description of your ideal customer.
  Fill in 1–2 personas. More than 2 usually means you're not focused yet.
-->

### 3.1 Primary User Persona

| Field | Details |
|-------|---------|
| **Persona Name** | `[Give them a made-up name, e.g., "Founder Felix"]` |
| **Age / Role** | `[e.g., 28 / Solo SaaS Founder]` |
| **Where They Work** | `[e.g., Home office, small startup, remote team]` |
| **Technical Level** | ☐ Non-Technical &nbsp; ☐ Semi-Technical &nbsp; ☐ Developer |
| **Their #1 Job** | `[What they're hired to do / their main responsibility]` |
| **Their #1 Frustration** | `[The problem they complain about most — your product solves THIS]` |
| **How They Solve It Today** | `[Current workaround — spreadsheet, manual process, competitor, etc.]` |
| **Why That Sucks** | `[Time lost / money wasted / errors made with current solution]` |
| **Where They Hang Out** | `[Twitter/X, LinkedIn, Reddit, Slack communities, Discord, etc.]` |
| **What They'll Pay** | `[Price point they expect — e.g., "$20–$50/mo" or "one-time $99"]` |

---

### 3.2 Secondary User Persona (Optional)

| Field | Details |
|-------|---------|
| **Persona Name** | `[e.g., "PM Priya"]` |
| **Age / Role** | `[e.g., 34 / Product Manager at a 50-person startup]` |
| **Their #1 Frustration** | `[Different from primary — why do they need you?]` |
| **How They Solve It Today** | `[Current workaround]` |
| **What They'll Pay** | `[Expected price]` |

---

### 3.3 Problem Statement

<!--
  Write your problem statement using this exact format. It forces clarity.
  Fill in the blanks and delete the placeholder text.
-->

> **Problem Statement:**
>
> **[Persona Name]** struggles to **[do a specific task]** because **[root cause of the problem]**.
>
> Today, they **[current workaround]**, which costs them **[time / money / frustration]**.
>
> If nothing changes, they will **[negative consequence — lost revenue, burnout, missed opportunity]**.

---

### 3.4 Competitive Landscape

<!--
  List your top 3 competitors and be honest about what they do better.
  Then show YOUR edge. Don't lie to yourself here — this section is
  most useful when it's brutally honest.
-->

| Competitor | Their Strength | Their Weakness | Your Edge vs. Them |
|-----------|---------------|----------------|-------------------|
| `[Competitor 1]` | `[What they do really well]` | `[Where they fall short]` | `[Why you win here]` |
| `[Competitor 2]` | `[What they do really well]` | `[Where they fall short]` | `[Why you win here]` |
| `[Competitor 3]` | `[What they do really well]` | `[Where they fall short]` | `[Why you win here]` |
| **Your Product** | **`[Your core strength]`** | `[Be honest about your gap]` | `[Your unfair advantage]` |

---

## 4. Goals & Success Metrics

<!--
  🟡 INSTRUCTIONS — Section 4: Goals & Success Metrics
  ──────────────────────────────────────────────────────
  Goals without numbers are wishes. Every goal needs:
  → A METRIC (what you're measuring)
  → A TARGET (the specific number)
  → A DEADLINE (by when)

  This section tracks your journey from 0 to 500 customers.
  Divide your goals into phases that match Section 5.
-->

### 4.1 Phase-by-Phase Goals

| Phase | Goal Description | Key Metric | Target | Deadline |
|-------|-----------------|------------|--------|----------|
| **Discovery** | Validate problem with real people | Interviews completed | `10 interviews` | `YYYY-MM-DD` |
| **Discovery** | Confirm willingness to pay | Pre-signups or LOIs | `25 waitlist signups` | `YYYY-MM-DD` |
| **MVP Build** | Ship first working version | Features shipped | `[List your MVP features]` | `YYYY-MM-DD` |
| **Beta** | Get first real users using product | Beta users active | `10–25 beta users` | `YYYY-MM-DD` |
| **Beta** | Achieve core user satisfaction | NPS or CSAT score | `NPS > 30` | `YYYY-MM-DD` |
| **Launch** | Public availability | Product is live | `Yes/No` | `YYYY-MM-DD` |
| **Growth** | Reach first paying customers | Paying users | `50` | `YYYY-MM-DD` |
| **Growth** | Hit MRR milestone | Monthly Recurring Revenue | `$[X] MRR` | `YYYY-MM-DD` |
| **Growth** | Reach first 500 customers | Total active users | `500` | `YYYY-MM-DD` |

---

### 4.2 Product Quality Targets

<!--
  Quality isn't optional. Set standards early so bugs don't haunt you at scale.
-->

| Quality Metric | Definition | Your Target |
|---------------|-----------|-------------|
| **Uptime / Reliability** | % of time the product is online and working | `≥ 99.5%` |
| **Bug-Free Sprint Rate** | % of sprints with zero critical bugs shipped | `≥ 85%` |
| **Response Time (API/page load)** | How fast the app responds | `< 1.5 seconds` |
| **AI Response Accuracy** | % of AI outputs rated correct by user | `> 90%` |
| **User-Reported Bugs per Month** | Bugs reported by real users monthly | `< 5 per month at launch` |
| **Time-to-Fix Critical Bug** | Max time from bug report to fix deployed | `< 24 hours` |

---

### 4.3 AI Performance Metrics (If AI is in your product)

| AI Metric | Definition | Your Target |
|-----------|-----------|-------------|
| **Average Latency** | Time for AI response to appear | `< 3 seconds` |
| **Token Cost per User Session** | Average Claude API cost per user action | `< $0.0X per session` |
| **Monthly AI Infra Cost** | Total AI API spend per month | `< $[X]/mo at 500 users` |
| **Hallucination / Error Rate** | % of AI outputs flagged as wrong | `< 5%` |
| **Feature Usage Rate** | % of users who use the AI feature | `> 60%` |

---

## 5. Phases of Development

<!--
  🟡 INSTRUCTIONS — Section 5: Phases of Development
  ────────────────────────────────────────────────────
  Your product will go through 5 phases from idea to 500 customers.
  Each phase has a clear START, END, and GOAL.

  Fill in the dates and specific deliverables for each phase.
  The sub-sections inside each phase tell you exactly what to do.

  PHASE OVERVIEW:
  ┌─────────────────────────────────────────────────────────────────┐
  │  0. Discovery    → Understand users BEFORE writing a line       │
  │  1. MVP Build    → Build the simplest working version           │
  │  2. Beta         → Get real humans to use and break it         │
  │  3. Launch       → Open the doors to the public                 │
  │  4. Growth       → Scale to 500 customers                       │
  └─────────────────────────────────────────────────────────────────┘
-->

### Phase 0 — Discovery & Validation

> **Goal:** Prove the problem is real and people will pay before writing code.
> **Duration:** `[e.g., 2–4 weeks]` &nbsp; | &nbsp; **Start:** `YYYY-MM-DD` &nbsp; | &nbsp; **End:** `YYYY-MM-DD`
> **Exit Criteria:** Move to Phase 1 ONLY when ALL items below are checked.

**What You'll Do:**

| # | Task | How | Done? |
|---|------|-----|-------|
| 1 | Define the problem in one paragraph | Write it in this doc (Section 3.3) | ☐ |
| 2 | List 3 competitors and their weaknesses | Section 3.4 | ☐ |
| 3 | Interview 10 real potential users | Video call, voice note, or DM | ☐ |
| 4 | Identify the ONE core pain to solve in V1 | Must be a burning pain, not a nice-to-have | ☐ |
| 5 | Validate willingness to pay | Ask: "Would you pay $X/month for this?" | ☐ |
| 6 | Create a landing page with waitlist | Use Carrd, Framer, or v0 | ☐ |
| 7 | Get 25+ waitlist signups | Share in communities, DMs, Twitter | ☐ |
| 8 | Define MVP feature set (max 3 features) | Section 6 — Feature Table | ☐ |

**AI Usage in This Phase:**

| AI Task | Tool | Prompt Template |
|---------|------|-----------------|
| Generate user interview questions | Claude | `"Generate 10 discovery interview questions for [target user] about [problem]"` |
| Synthesize interview notes | Claude | `"Here are my 10 interview notes: [paste notes]. Summarize the top 3 pain themes."` |
| Write landing page copy | Claude | `"Write a landing page for [Product Name] targeting [persona] with problem [X] and benefit [Y]"` |
| Competitive analysis | Claude + Web Search | `"Research top competitors for [category]. Compare features, pricing, and gaps."` |

**Phase 0 Exit Criteria:**
- [ ] 10+ user interviews completed
- [ ] Willingness to pay confirmed (at least 5 people said "yes")
- [ ] 25+ waitlist signups collected
- [ ] MVP scope locked to ≤ 3 core features

---

### Phase 1 — MVP Build

> **Goal:** Ship the smallest possible version that solves the core problem.
> **Duration:** `[e.g., 4–8 weeks]` &nbsp; | &nbsp; **Start:** `YYYY-MM-DD` &nbsp; | &nbsp; **End:** `YYYY-MM-DD`
> **Rule:** No feature that isn't in Phase 0's MVP list. Ship fast, ship scrappy.

**What You'll Build:**

| Feature | Why It's In MVP | How Complex (1–5) | Status |
|---------|----------------|-------------------|--------|
| `[Feature 1]` | `[The one thing without which the product is useless]` | `[1–5]` | ☐ Not Started |
| `[Feature 2]` | `[Second most critical function]` | `[1–5]` | ☐ Not Started |
| `[Feature 3]` | `[Third — be strict, does it NEED to be here?]` | `[1–5]` | ☐ Not Started |

**What You Will NOT Build in MVP:**

<!--
  This list is as important as your build list.
  Writing down what you're deferring prevents scope creep.
-->

- ❌ `[Deferred Feature 1]` — Reason: `[Why it's not MVP]`
- ❌ `[Deferred Feature 2]` — Reason: `[Why it's not MVP]`
- ❌ `[Deferred Feature 3]` — Reason: `[Why it's not MVP]`

**AI Dev Loop for MVP Build:**

```
Daily AI-Assisted Development Cycle (Vibe Coding Method)
─────────────────────────────────────────────────────────
1. PLAN     → Ask Claude: "I'm building [feature]. What are the steps?"
2. SCAFFOLD → Use Claude Code or Cursor to generate boilerplate
3. BUILD    → Implement with AI pair-programming in real time
4. REVIEW   → Ask Claude: "Review this code for bugs and security issues"
5. TEST     → Ask Claude to generate test cases; run them
6. COMMIT   → Push to GitHub with clear commit message
7. REFLECT  → End of day: "What did I ship? What's blocked?"
```

**Phase 1 Exit Criteria:**
- [ ] All 3 MVP features are working end-to-end
- [ ] App runs without crashes for 30 minutes of continuous use
- [ ] At least 1 person outside your team has used it successfully
- [ ] Basic error handling is in place (no blank white screen on errors)
- [ ] Code is committed to GitHub

---

### Phase 2 — Beta Testing

> **Goal:** Get 10–25 real users to use the product and collect honest feedback.
> **Duration:** `[e.g., 2–4 weeks]` &nbsp; | &nbsp; **Start:** `YYYY-MM-DD` &nbsp; | &nbsp; **End:** `YYYY-MM-DD`

**Beta Recruitment Plan:**

| Channel | How Many to Invite | Message Template |
|---------|-------------------|-----------------|
| Waitlist signups | `[e.g., All 25]` | `"Hey [name], your spot is ready — try [Product Name] free: [link]"` |
| Twitter/X DMs | `[e.g., 10]` | `[Short DM to followers who fit your persona]` |
| Reddit / Discord communities | `[e.g., 15]` | `[Community post offering free access for feedback]` |
| Friends and network | `[e.g., 5]` | `[Personal text or email]` |

**Feedback Collection:**

| Method | Tool | Frequency |
|--------|------|-----------|
| In-app feedback widget | Tally, Featurebase, or custom form | Always-on |
| Weekly user interview | Calendly + Zoom/Loom | Weekly |
| Bug reports | GitHub Issues or Linear | Always-on |
| NPS survey | Tally or TypeForm | End of beta |
| Usage analytics | PostHog, Mixpanel, or Plausible | Daily review |

**Beta Feedback Log:**

| Date | User | Feedback Summary | Priority | Action Taken |
|------|------|-----------------|----------|-------------|
| `YYYY-MM-DD` | `[User name/ID]` | `[What they said]` | 🔴 Critical / 🟡 Nice-to-have / 🟢 Positive | `[Fix / Defer / Accept]` |

**Phase 2 Exit Criteria:**
- [ ] 10+ beta users have used the core feature at least twice
- [ ] NPS score ≥ 30 OR ≥ 5 users say they'd be "very disappointed" without it
- [ ] All critical (🔴) bugs from beta are resolved
- [ ] Pricing page or payment flow is ready

---

### Phase 3 — Public Launch

> **Goal:** Open the product to the public and convert first paying customers.
> **Duration:** `[e.g., 1–2 weeks]` &nbsp; | &nbsp; **Start:** `YYYY-MM-DD` &nbsp; | &nbsp; **End:** `YYYY-MM-DD`

**Launch Checklist:**

| Category | Task | Done? |
|----------|------|-------|
| **Product** | All critical bugs fixed | ☐ |
| **Product** | Onboarding flow is smooth (< 5 min to first value) | ☐ |
| **Product** | Payment / subscription flow working (Stripe, LemonSqueezy) | ☐ |
| **Product** | Error monitoring is live (Sentry, LogRocket) | ☐ |
| **Marketing** | Product Hunt submission prepared | ☐ |
| **Marketing** | Launch post written for Twitter/X, LinkedIn, Reddit | ☐ |
| **Marketing** | Email to waitlist is ready to send | ☐ |
| **Legal** | Privacy Policy is published | ☐ |
| **Legal** | Terms of Service is published | ☐ |
| **Support** | FAQ page or docs site is live | ☐ |
| **Support** | Support email or chat (Crisp, Intercom) is working | ☐ |

**Launch Day Timeline:**

| Time (UTC) | Action |
|-----------|--------|
| `06:00` | Send launch email to waitlist |
| `07:00` | Post on Twitter/X with demo video |
| `08:00` | Submit to Product Hunt |
| `09:00` | Post in top 3 Reddit / Discord communities |
| `12:00` | Share on LinkedIn with your story |
| `18:00` | Check metrics — respond to every comment and DM |
| `23:59` | End-of-day debrief: what worked, what didn't |

**Phase 3 Exit Criteria:**
- [ ] Product is publicly accessible
- [ ] First paying customer acquired
- [ ] Analytics and error monitoring are live
- [ ] No P0 (showstopper) bugs in production

---

### Phase 4 — Growth (to 500 Customers)

> **Goal:** Scale from first customer to 500 active or paying users.
> **Duration:** `[e.g., 3–6 months]` &nbsp; | &nbsp; **Start:** `YYYY-MM-DD` &nbsp; | &nbsp; **End:** `YYYY-MM-DD`

**Growth Milestones:**

| Milestone | Target | Date Achieved | Notes |
|-----------|--------|---------------|-------|
| First 10 customers | `10` | `YYYY-MM-DD` | |
| First $1 in revenue | `$1 MRR` | `YYYY-MM-DD` | |
| First 50 customers | `50` | `YYYY-MM-DD` | |
| First $1,000 MRR | `$1,000/mo` | `YYYY-MM-DD` | |
| First 100 customers | `100` | `YYYY-MM-DD` | |
| First 250 customers | `250` | `YYYY-MM-DD` | |
| **500 customers 🎉** | **`500`** | `YYYY-MM-DD` | **MAJOR MILESTONE** |

**Growth Tactics:**

| Tactic | Channel | Budget | Owner | Status |
|--------|---------|--------|-------|--------|
| `[SEO blog posts]` | `Organic Search` | `$0` | `You` | ☐ Planned |
| `[Cold email outreach]` | `Email` | `$X/mo (tool cost)` | `You` | ☐ Planned |
| `[Twitter/X content]` | `Social` | `$0` | `You` | ☐ Planned |
| `[Paid ads — Google/Meta]` | `Paid` | `$X/mo` | `You` | ☐ Planned |
| `[Affiliate/referral program]` | `Word-of-mouth` | `Revenue share` | `You` | ☐ Planned |
| `[Community building]` | `Discord/Slack` | `$0` | `You` | ☐ Planned |

---

## 6. Feature Planning & Prioritization

<!--
  🟡 INSTRUCTIONS — Section 6: Feature Planning & Prioritization
  ────────────────────────────────────────────────────────────────
  List ALL features you've ever thought of. Then sort them.

  PRIORITY LEVELS:
  🔴 P0 — Must have. Product is broken without it.
  🟡 P1 — Should have. Significantly improves the product.
  🟢 P2 — Nice to have. Adds value but not urgent.
  ⚫ P3 — Future / Backlog. Don't think about this yet.

  RICE SCORE (optional but powerful):
  RICE = (Reach × Impact × Confidence) ÷ Effort
  Higher score = build sooner. Use it to avoid gut-feel prioritization.
-->

### 6.1 Master Feature Backlog

| Feature Name | Description | Priority | Phase | RICE Score | Status |
|-------------|-------------|----------|-------|-----------|--------|
| `[Feature 1]` | `[What it does and why users need it]` | 🔴 P0 | MVP | `[0–100]` | ☐ Not Started |
| `[Feature 2]` | `[What it does and why users need it]` | 🔴 P0 | MVP | `[0–100]` | ☐ Not Started |
| `[Feature 3]` | `[What it does and why users need it]` | 🟡 P1 | Beta | `[0–100]` | ☐ Not Started |
| `[Feature 4]` | `[What it does and why users need it]` | 🟡 P1 | Launch | `[0–100]` | ☐ Not Started |
| `[Feature 5]` | `[What it does and why users need it]` | 🟢 P2 | Growth | `[0–100]` | ☐ Not Started |
| `[Feature 6]` | `[What it does and why users need it]` | ⚫ P3 | Future | `—` | ☐ Backlog |

---

### 6.2 How to Calculate RICE Score

```
RICE SCORE FORMULA
──────────────────
Reach      = How many users will this affect per month? (Number)
Impact     = How much does it help each user? (3=massive, 2=high, 1=medium, 0.5=low)
Confidence = How sure are you about reach & impact? (100%, 80%, 50%)
Effort     = How many weeks of work? (1 week = 1 point)

RICE = (Reach × Impact × Confidence) ÷ Effort

Example:
  Feature: "Save to PDF"
  Reach = 200 users/month
  Impact = 2 (high)
  Confidence = 80% = 0.8
  Effort = 1 week

  RICE = (200 × 2 × 0.8) ÷ 1 = 320

Higher score → build it sooner.
```

---

### 6.3 Feature Roadmap by Quarter (Visual Overview)

```
FEATURE ROADMAP TIMELINE
─────────────────────────────────────────────────────────────────────────
PHASE 0       PHASE 1          PHASE 2         PHASE 3       PHASE 4
[Discovery]   [MVP Build]      [Beta]          [Launch]      [Growth]
──────────    ─────────────    ─────────────   ──────────    ─────────────
              ✅ Feature 1     ✅ Feature 3    🚀 Feature 4  📈 Feature 5
              ✅ Feature 2                     🚀 Feature X  📈 Feature 6
              (Deferred →)     (Deferred →)                  (Backlog...)
─────────────────────────────────────────────────────────────────────────
              ← Edit this with your actual feature names →
```

---

## 7. AI Dev Workflow: How AI Helps You Build

<!--
  🟡 INSTRUCTIONS — Section 7: AI Dev Workflow
  ──────────────────────────────────────────────
  This section documents HOW you use AI throughout the development process.
  It's your AI-first development playbook.

  For each phase, fill in:
  → WHAT AI tool you use
  → WHAT you use it for (the specific task)
  → THE EXACT PROMPT or prompt pattern you use
  → WHAT you review before accepting the output

  This becomes your reusable playbook for every future project.
-->

### 7.1 AI Dev Stack

| Tool | Role in Your Workflow | Cost/Month |
|------|-----------------------|-----------|
| **Claude (claude.ai or API)** | Product thinking, writing, code review, documentation | `$X/mo` |
| **Claude Code (CLI)** | Terminal-based AI coding agent | Included in API |
| **Cursor / Windsurf** | AI-powered IDE for building features | `$X/mo` |
| `[Add your tools]` | `[Role]` | `$X/mo` |

---

### 7.2 AI Prompt Playbook by Phase

#### Phase 0 — Discovery

| Task | AI Tool | Prompt to Use |
|------|---------|---------------|
| User interview questions | Claude | `"Generate 12 discovery interview questions for [persona] who struggles with [problem]. Focus on uncovering root causes, workarounds, and emotional pain."` |
| Competitor analysis | Claude + Web | `"Analyze the top 5 tools in [category]. For each: summarize features, pricing model, weak points, and who their ideal customer is."` |
| Landing page copy | Claude | `"Write a SaaS landing page for [Product Name]. Target user: [persona]. Core problem: [pain]. Core solution: [how it works]. Tone: [casual/professional]. Include: headline, sub-headline, 3 benefits, 1 CTA."` |
| Validate problem statement | Claude | `"Here are notes from 10 user interviews: [paste notes]. Identify the top 3 common pain themes, any surprising insights, and whether the data supports building [Product Name]."` |

#### Phase 1 — MVP Build

| Task | AI Tool | Prompt to Use |
|------|---------|---------------|
| Architecture planning | Claude | `"I'm building a [SaaS/mobile app] with these features: [list]. Recommend a tech stack for a solo founder using [budget/preference]. Include: frontend, backend, DB, auth, hosting."` |
| Feature scaffolding | Claude Code / Cursor | `"Build the [feature name] feature. Stack: [your stack]. Requirements: [detailed spec]. Add comments explaining each function."` |
| Code review | Claude | `"Review this code for: bugs, security issues, performance problems, and anything a junior dev might have missed. Code: [paste code]"` |
| Writing tests | Claude | `"Write unit tests for this function: [paste function]. Use [testing library]. Cover: happy path, edge cases, and error states."` |
| Git commit messages | Claude | `"Write a clear git commit message for: [describe what changed]"` |

#### Phase 2 — Beta

| Task | AI Tool | Prompt to Use |
|------|---------|---------------|
| Synthesize user feedback | Claude | `"Here are 15 pieces of user feedback: [paste]. Categorize by theme, identify the top 3 fixes needed, and suggest which to prioritize."` |
| Bug triage | Claude | `"This is the bug report: [paste]. This is the relevant code: [paste]. Identify the likely root cause and suggest a fix."` |
| Write onboarding copy | Claude | `"Write a 3-email onboarding sequence for new users of [Product Name]. Goal: help them reach their first success within 48 hours."` |

#### Phase 3 — Launch

| Task | AI Tool | Prompt to Use |
|------|---------|---------------|
| Product Hunt description | Claude | `"Write a Product Hunt submission for [Product Name]: tagline (< 60 chars), description (< 260 chars), and 3 gallery captions."` |
| Launch tweet thread | Claude | `"Write a 5-tweet launch thread for [Product Name]. Angle: [founder story / problem solved / demo]. Tone: authentic and conversational."` |
| Press/media pitch | Claude | `"Write a cold email pitch to a tech journalist at [publication] about [Product Name]. One paragraph. Hook: [angle]. CTA: [request]."` |

#### Phase 4 — Growth

| Task | AI Tool | Prompt to Use |
|------|---------|---------------|
| SEO blog post | Claude | `"Write a 1,200-word SEO blog post targeting the keyword '[keyword]' for [target user]. Include: intro hook, 3 main sections with H2s, and a CTA to try [Product Name]."` |
| Customer success email | Claude | `"Write a check-in email to a customer who signed up 7 days ago but hasn't used [key feature]. Goal: re-engage them without being pushy."` |
| Feature announcement | Claude | `"Write an in-app announcement and email for the new [feature] in [Product Name]. Explain: what it is, why it matters, how to try it."` |

---

### 7.3 AI Output Review Checklist

<!--
  NEVER ship AI-generated code or content without checking this list.
  AI makes confident-sounding mistakes. You are responsible.
-->

Before accepting any AI output, check:

- [ ] **Is it correct?** Does the code actually do what you asked?
- [ ] **Does it run?** Did you test it locally before committing?
- [ ] **Is it secure?** No exposed API keys, no SQL injection risks, no hardcoded secrets?
- [ ] **Is it readable?** Can you explain every line to someone else?
- [ ] **Is it honest?** No hallucinated facts, libraries, or function names?
- [ ] **Is it on-brand?** Does generated copy sound like your product's voice?

---

## 8. In-Product AI Agent Design Canvas

<!--
  🟡 INSTRUCTIONS — Section 8: In-Product AI Agent Design Canvas
  ───────────────────────────────────────────────────────────────
  If your PRODUCT itself uses AI agents (not just your dev process),
  design each agent here BEFORE you build it.

  One table per agent. Copy the template for each additional agent.

  DEFINITIONS:
  → Agent     = A piece of AI that does a specific job automatically
  → Tool      = A function the agent can call (search web, send email, etc.)
  → Guardrail = A rule that prevents the agent from doing something harmful
  → Fallback  = What happens when the AI fails or is unsure
-->

### 8.1 Agent #1 — [Agent Name]

| Field | Your Answer |
|-------|-------------|
| **Agent Name** | `[e.g., "Onboarding Coach" / "Content Generator" / "Bug Triage Bot"]` |
| **Agent Role** | `[One sentence: what does this agent do for the user?]` |
| **Trigger** | `[What causes this agent to activate? e.g., "User clicks Generate", "New signup event", "Scheduled daily at 8am"]` |
| **Input** | `[What data does the agent receive? e.g., "User's draft text", "Form answers", "User ID + context"]` |
| **Core Prompt / System Prompt** | `[Paste or describe the system prompt that defines this agent's behavior]` |
| **Output** | `[What does the agent produce? e.g., "3-paragraph email", "Classified bug category", "Action plan"]` |
| **AI Model Used** | `[e.g., claude-3-5-sonnet, claude-3-haiku — choose based on cost vs quality]` |
| **Tools / Functions** | `[List any tools the agent can call: web_search, send_email, create_task, query_db, etc.]` |
| **Max Tokens / Cost Limit** | `[e.g., "Max 1,000 output tokens per call = ~$0.003/call"]` |
| **Guardrails** | `[Rules: "Never make up data", "Always cite sources", "Do not send emails without confirmation", etc.]` |
| **Fallback Behavior** | `[What happens if the agent fails or has low confidence? e.g., "Show error message + manual option"]` |
| **Logging** | `[How are agent calls logged? e.g., "Input/output saved to DB for review"]` |
| **Human-in-the-Loop?** | `[Does a human approve before agent acts? Yes/No/Sometimes — explain]` |

---

### 8.2 Agent #2 — [Agent Name]

| Field | Your Answer |
|-------|-------------|
| **Agent Name** | `[Name]` |
| **Agent Role** | `[Role]` |
| **Trigger** | `[Trigger event]` |
| **Input** | `[Input data]` |
| **Core Prompt** | `[System prompt]` |
| **Output** | `[What it produces]` |
| **AI Model Used** | `[Model name]` |
| **Tools / Functions** | `[Tool list]` |
| **Max Tokens / Cost Limit** | `[Limits]` |
| **Guardrails** | `[Rules]` |
| **Fallback Behavior** | `[Fallback]` |
| **Logging** | `[Logging method]` |
| **Human-in-the-Loop?** | `[Yes/No/When]` |

> 💡 **Add more agents** by copying the table above. Label them Agent #3, #4, etc.

---

### 8.3 AI Agent Interaction Map

```
AI AGENT INTERACTION MAP
────────────────────────────────────────────────────────────────
  USER ACTION
       │
       ▼
  ┌─────────────────────────────────────┐
  │         Your Product (Frontend)      │
  └─────────────────┬───────────────────┘
                    │ API call
                    ▼
  ┌─────────────────────────────────────┐
  │        Agent Orchestrator            │
  │  (Routes to correct agent based on  │
  │   user intent / trigger)            │
  └──────┬──────────┬────────────┬──────┘
         │          │            │
         ▼          ▼            ▼
  ┌──────────┐ ┌──────────┐ ┌──────────┐
  │ Agent #1 │ │ Agent #2 │ │ Agent #3 │
  │ [Name]   │ │ [Name]   │ │ [Name]   │
  └────┬─────┘ └────┬─────┘ └────┬─────┘
       │            │            │
       ▼            ▼            ▼
  ┌──────────────────────────────────────┐
  │   Outputs: Text / Data / Actions     │
  └──────────────────────────────────────┘
                    │
                    ▼
            User sees result
────────────────────────────────────────────────────────────────
  Replace agent names with your actual agents above.
```

---

## 9. Technical Architecture

<!--
  🟡 INSTRUCTIONS — Section 9: Technical Architecture
  ──────────────────────────────────────────────────────
  You don't need to be super technical to fill this out.
  Just list what tools and services you're using for each role.
  If you used Claude to pick your stack, paste the recommendation here.

  If you're unsure, use this as your prompt:
  "I'm a solo founder building a [SaaS / mobile] app. I need: auth, database,
  file storage, AI (Claude API), payments, analytics, and hosting.
  Recommend a cheap, fast, beginner-friendly stack."
-->

### 9.1 Tech Stack

| Layer | Category | Tool / Service | Why You Chose It |
|-------|----------|---------------|-----------------|
| **Frontend** | Web Framework | `[Next.js / React / Svelte / Vue]` | `[Reason]` |
| **Frontend** | Styling | `[Tailwind CSS / shadcn/ui / MUI]` | `[Reason]` |
| **Backend** | API / Server | `[Next.js API routes / Express / FastAPI]` | `[Reason]` |
| **Database** | Primary DB | `[Supabase / PlanetScale / MongoDB / SQLite]` | `[Reason]` |
| **Auth** | Authentication | `[Clerk / Supabase Auth / Auth.js / Firebase Auth]` | `[Reason]` |
| **AI** | LLM Provider | `[Anthropic Claude API]` | `[Reason]` |
| **AI** | Model | `[claude-3-5-sonnet / claude-3-haiku]` | `[Cost/quality tradeoff]` |
| **Storage** | Files | `[Supabase Storage / Cloudflare R2 / S3]` | `[Reason]` |
| **Payments** | Billing | `[Stripe / LemonSqueezy]` | `[Reason]` |
| **Email** | Transactional | `[Resend / SendGrid / Postmark]` | `[Reason]` |
| **Analytics** | Product Analytics | `[PostHog / Mixpanel / Plausible]` | `[Reason]` |
| **Errors** | Monitoring | `[Sentry / LogRocket]` | `[Reason]` |
| **Hosting** | Deployment | `[Vercel / Railway / Fly.io]` | `[Reason]` |
| **CI/CD** | Pipelines | `[GitHub Actions / Vercel auto-deploy]` | `[Reason]` |
| **Mobile** | Framework | `[Expo / React Native / Flutter — if applicable]` | `[Reason]` |

---

### 9.2 High-Level Architecture Diagram

```
HIGH-LEVEL ARCHITECTURE
────────────────────────────────────────────────────────────────────
  ┌──────────────────────────────┐
  │  USER (Browser or Mobile)     │
  └──────────────┬───────────────┘
                 │ HTTPS
                 ▼
  ┌──────────────────────────────┐
  │  Frontend ([Next.js / Expo])  │  ← Hosted on [Vercel / EAS]
  └──────────────┬───────────────┘
                 │ REST / tRPC / GraphQL
                 ▼
  ┌──────────────────────────────┐
  │  Backend API ([Framework])    │  ← Hosted on [Railway / Vercel]
  │  - Auth middleware            │
  │  - Business logic             │
  │  - AI orchestration layer     │
  └───────┬──────────┬───────────┘
          │          │
          ▼          ▼
  ┌────────────┐ ┌──────────────────┐
  │  Database  │ │  Claude AI API    │
  │ [Supabase] │ │  (Anthropic)      │
  └────────────┘ └──────────────────┘
          │
          ▼
  ┌────────────┐
  │  File Store│   ← Supabase Storage / R2
  └────────────┘
────────────────────────────────────────────────────────────────────
  Replace placeholders with your actual tools above.
```

---

## 10. Budget & Cost Tracking

<!--
  🟡 INSTRUCTIONS — Section 10: Budget & Cost Tracking
  ──────────────────────────────────────────────────────
  Money matters from Day 1. Track everything.
  Costs before revenue = investment in learning.
  Costs after revenue = business expenses.

  Fill in your actual or estimated costs.
  Review this table every month and update actuals.

  COLUMNS:
  Category     = Type of expense
  Tool/Service = Exact service name
  Plan/Tier    = Which pricing plan you're on
  Est. Cost    = What you expect to pay
  Actual Cost  = What you actually paid (fill in monthly)
  Notes        = When it scales or spikes
-->

### 10.1 Monthly Operating Costs

| Category | Tool / Service | Plan / Tier | Est. Monthly Cost | Actual Cost | Notes |
|----------|---------------|------------|------------------|-------------|-------|
| **AI — LLM** | Claude API (Anthropic) | Pay-per-token | `$[X]` | `$` | Scales with usage |
| **Hosting** | `[Vercel / Railway]` | `[Free/Pro]` | `$[X]` | `$` | Upgrade at scale |
| **Database** | `[Supabase]` | `[Free/Pro]` | `$[X]` | `$` | Pro at 500MB+ |
| **Auth** | `[Clerk / Supabase Auth]` | `[Free/Pro]` | `$[X]` | `$` | Per Monthly Active User |
| **Email** | `[Resend]` | `[Free/Pro]` | `$[X]` | `$` | 3,000/mo free |
| **Analytics** | `[PostHog]` | `[Free]` | `$0` | `$` | Free up to 1M events |
| **Error Monitoring** | `[Sentry]` | `[Free]` | `$0` | `$` | Free up to 5K errors |
| **Domain** | `[Namecheap / Cloudflare]` | Annual | `~$1/mo` | `$` | Paid annually |
| **Dev Tools** | Cursor / Windsurf | `[Pro]` | `$[X]` | `$` | IDE subscription |
| **Marketing** | `[Ads / Tools]` | `[Varies]` | `$[X]` | `$` | Increase at launch |
| **Miscellaneous** | Other tools | `[Varies]` | `$[X]` | `$` | |
| | **TOTAL** | | **`$[X]/mo`** | **`$`** | |

---

### 10.2 AI Cost Estimation (Claude API)

<!--
  Use this to plan your Claude API budget before costs explode.
  Formula: Cost = (Input Tokens + Output Tokens) × Model Price per 1M tokens
-->

| Model | Input Cost (per 1M tokens) | Output Cost (per 1M tokens) | Best For |
|-------|--------------------------|----------------------------|----------|
| claude-3-haiku-20240307 | ~$0.25 | ~$1.25 | High-volume, simple tasks |
| claude-3-5-sonnet-20241022 | ~$3.00 | ~$15.00 | Balanced quality + cost |
| claude-3-opus | ~$15.00 | ~$75.00 | Complex reasoning only |

**Your Cost Estimate:**

| Scenario | Calls/Day | Avg Tokens/Call | Est. Monthly Cost |
|----------|-----------|----------------|------------------|
| 10 beta users | `[X calls]` | `[X tokens]` | `$[X]` |
| 50 users at launch | `[X calls]` | `[X tokens]` | `$[X]` |
| 500 users (growth) | `[X calls]` | `[X tokens]` | `$[X]` |

---

### 10.3 One-Time / Setup Costs

| Item | Cost | Date Paid |
|------|------|-----------|
| Domain name | `$[X]` | `YYYY-MM-DD` |
| Design assets / icons | `$[X]` | `YYYY-MM-DD` |
| Legal (Privacy Policy, ToS) | `$[X]` | `YYYY-MM-DD` |
| `[Other one-time costs]` | `$[X]` | `YYYY-MM-DD` |
| **TOTAL ONE-TIME** | **`$[X]`** | |

---

## 11. Risk Register

<!--
  🟡 INSTRUCTIONS — Section 11: Risk Register
  ─────────────────────────────────────────────
  A risk is something that MIGHT go wrong and hurt your product.
  The goal is to think about problems BEFORE they happen.

  HOW TO USE THIS TABLE:
  1. List every risk you can think of
  2. Rate Likelihood: Low / Medium / High
  3. Rate Impact: Low / Medium / High
  4. Calculate Risk Level: Likelihood × Impact
     Low×Low = Low | Low×High = Medium | High×High = CRITICAL
  5. Write a mitigation = what you'll do to prevent it
  6. Write a contingency = what you'll do IF it happens anyway
-->

### 11.1 Risk Register Table

| # | Risk Description | Category | Likelihood | Impact | Risk Level | Mitigation Plan | Contingency Plan | Owner | Status |
|---|-----------------|----------|-----------|--------|-----------|----------------|-----------------|-------|--------|
| R01 | AI API costs spike unexpectedly at scale | Technical | Medium | High | 🔴 Critical | Set token limits per user; monitor daily; use cheaper model for simple tasks | Implement rate limiting; add usage caps | `You` | 🟡 Monitoring |
| R02 | Key competitor copies core feature | Market | Medium | High | 🔴 Critical | Build fast; own the customer relationship; add switching costs | Double down on UX and community | `You` | 🟢 Watching |
| R03 | No one pays after free trial | Business | Medium | Critical | 🔴 Critical | Validate pricing in discovery; interview churned users | Redesign pricing; run limited offers | `You` | ⚪ Not Yet |
| R04 | Solo founder burnout | People | High | High | 🔴 Critical | Set working hours; take weekends; track mental health | Hire help; reduce scope; take break | `You` | 🟡 Monitoring |
| R05 | Data breach or security incident | Security | Low | Critical | 🔴 Critical | Use Clerk/Supabase auth; never store raw passwords; run dependency audits | Notify users; patch immediately; post incident report | `You` | 🟢 Mitigated |
| R06 | Core AI model deprecated by Anthropic | Technical | Low | High | 🟡 Medium | Monitor Anthropic announcements; abstract AI calls behind a wrapper | Switch model version in config | `You` | 🟢 Watching |
| R07 | App crashes during Product Hunt launch | Technical | Medium | High | 🟡 Medium | Load test before launch; scale hosting the day before | Enable maintenance mode; communicate on Twitter | `You` | ⚪ Not Yet |
| R08 | Wrong ICP targeted | Strategy | Low | High | 🟡 Medium | Validate ICP in Phase 0 interviews | Pivot persona; run new discovery round | `You` | ⚪ Not Yet |
| `R09` | `[Your risk]` | `[Category]` | `Low/Med/High` | `Low/Med/High` | `🔴/🟡/🟢` | `[What you'll do to prevent it]` | `[What you'll do if it happens]` | `You` | `⚪ New` |

**Status Key:** 🔴 Active Issue | 🟡 Monitoring | 🟢 Mitigated | ⚪ Not Yet Relevant

---

## 12. Go-To-Market Strategy

<!--
  🟡 INSTRUCTIONS — Section 12: Go-To-Market Strategy
  ──────────────────────────────────────────────────────
  Your GTM strategy is HOW you get customers.
  Without a plan here, great products gather dust.

  Fill in ONLY the channels you'll actually commit to.
  1 channel done well beats 10 channels done poorly.
-->

### 12.1 GTM Overview

| Field | Your Answer |
|-------|-------------|
| **Target ICP** | `[Exact person: title, company size, industry — from Section 3]` |
| **Primary GTM Motion** | ☐ Product-Led Growth &nbsp; ☐ Sales-Led &nbsp; ☐ Community-Led &nbsp; ☐ Content-Led |
| **First 10 Customers Source** | `[Who they are and how you'll find them personally]` |
| **Primary Launch Channel** | `[Product Hunt / Twitter / Reddit / Email / etc.]` |
| **Pricing Strategy** | ☐ Freemium &nbsp; ☐ Free Trial (X days) &nbsp; ☐ Paid from Day 1 &nbsp; ☐ Invite-Only Beta |
| **Price Points** | `[e.g., Free / $19/mo Starter / $49/mo Pro]` |

---

### 12.2 Pricing Tiers

<!--
  Keep pricing simple at launch. 2-3 tiers max.
  "Free" tier should give just enough to get addicted, not enough to avoid paying.
-->

| Tier | Price | What's Included | Who It's For |
|------|-------|----------------|-------------|
| **Free / Starter** | `$0/mo` | `[List features included — keep it limited]` | `[People who are exploring]` |
| **Pro** | `$[X]/mo` | `[Everything in Free + key power features]` | `[Your core paying customer]` |
| **Business / Team** | `$[X]/mo` | `[Everything in Pro + collaboration/admin features]` | `[Teams and companies]` |

---

### 12.3 Channel Strategy

| Channel | Tactic | Goal | Owner | Timeline | Budget |
|---------|--------|------|-------|----------|--------|
| **Product Hunt** | Launch on PH on a Tuesday | Top 5 of the day | `You` | Launch day | `$0` |
| **Twitter/X** | Daily build-in-public posts; launch thread | 500 followers → 50 signups | `You` | Ongoing | `$0` |
| **Reddit** | Post in r/SaaS, r/startups, niche subreddits | 100 clicks on launch | `You` | Launch week | `$0` |
| **Email / Waitlist** | Email blast to waitlist on launch day | 30% open rate, 10% conversion | `You` | Launch day | `$0` |
| **SEO Content** | Write 2 posts/week targeting pain keywords | 100 organic visitors/mo by month 3 | `You` | Ongoing | `$0` |
| **Paid Ads** | Google/Meta retargeting after first $1K MRR | 2x ROAS | `You` | Phase 4 | `$[X]/mo` |
| **Referral Program** | 1 month free for every paid referral | 20% of growth from referrals | `You` | Phase 4 | Revenue share |

---

### 12.4 Onboarding Journey Map

<!--
  Onboarding = the most important feature you'll ever build.
  Map the path from "just signed up" to "I love this product."
-->

```
ONBOARDING JOURNEY
───────────────────────────────────────────────────────────────────────
  USER SIGNS UP
       │
       ▼
  Welcome email sent (automated)
       │
       ▼
  First login → Guided setup wizard (< 3 steps)
       │
       ▼
  User reaches "Aha! Moment" → [Define yours: the exact action that
  makes them realize your product's value. e.g., "First report generated"]
       │
       ▼
  Day 2 email: "Here's a tip to get even more value..."
       │
       ▼
  Day 7 check-in: "How's it going? Need help?"
       │
       ▼
  User becomes ACTIVE (uses core feature 3x in first week)
       │
       ▼
  Upgrade prompt shown (if on free plan)
       │
       ▼
  PAYING CUSTOMER 💰
───────────────────────────────────────────────────────────────────────
  Fill in your actual "Aha! Moment" above — it's your #1 activation lever.
```

---

## 13. Quality Assurance Standards

<!--
  🟡 INSTRUCTIONS — Section 13: QA Standards
  ─────────────────────────────────────────────
  QA is not optional. Even solo founders need standards.
  Define what "done" means for every feature before you ship.

  DEFINITION OF DONE = A feature is only "done" when ALL items pass.
-->

### 13.1 Definition of Done (DoD)

Before any feature is marked complete, it must pass ALL of:

- [ ] Feature works as described in the feature spec
- [ ] Works in both Chrome and Safari (web)
- [ ] Works on mobile screen size (responsive)
- [ ] No console errors in browser dev tools
- [ ] AI-generated output has been reviewed for accuracy
- [ ] Error states are handled gracefully (no blank crashes)
- [ ] Loading states are shown for async operations
- [ ] Feature has been tested by at least one person who didn't build it
- [ ] Code is committed to GitHub with a clear commit message

---

### 13.2 QA Checklist Per Phase

| Phase | Must Test | How to Test |
|-------|-----------|------------|
| **MVP** | Core user flow works end-to-end | Walk through the flow as a new user manually |
| **MVP** | Sign up → onboard → core feature | Record a Loom of yourself using it cold |
| **Beta** | All P0 and P1 features work | Beta users naturally break things |
| **Beta** | Payment flow completes correctly | Use Stripe test mode |
| **Launch** | Load test — does it survive 100 concurrent users? | Use k6 or Artillery |
| **Launch** | All links on landing page work | Click every link manually |
| **Growth** | New features don't break existing ones | Regression test list |

---

### 13.3 Bug Severity Levels

| Level | Label | Definition | Max Time to Fix |
|-------|-------|-----------|----------------|
| P0 | 🔴 Showstopper | App is down or data is being lost | Fix in **< 4 hours** |
| P1 | 🟠 Critical | Core feature broken for all users | Fix in **< 24 hours** |
| P2 | 🟡 Major | Feature broken for some users | Fix in **< 3 days** |
| P3 | 🟢 Minor | UI glitch, non-critical issue | Fix in **next sprint** |
| P4 | ⚪ Cosmetic | Typos, visual polish | Fix **when convenient** |

---

## 14. Customer Milestone Tracker (0 → 500)

<!--
  🟡 INSTRUCTIONS — Section 14: Customer Milestone Tracker
  ──────────────────────────────────────────────────────────
  This is your journey log. Fill in each milestone as you hit it.
  Date: when you hit it. How: what caused the milestone. Learnings: what surprised you.
  This becomes the most interesting part of your story.
-->

### 14.1 Milestone Log

| Milestone | Target Date | Date Achieved | # of Days to Hit | How You Got Here | Key Learning |
|-----------|------------|---------------|-----------------|-----------------|-------------|
| 🚀 First line of code written | `YYYY-MM-DD` | `YYYY-MM-DD` | `—` | `[How you started]` | `[What you learned]` |
| 👥 First 10 waitlist signups | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[What drove signups]` | `[What surprised you]` |
| 🧪 MVP shipped to first beta user | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[What you built]` | `[Their first reaction]` |
| 💬 First unsolicited positive feedback | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[Who said it]` | `[What they loved]` |
| 💰 **First $1 in revenue** | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[Who paid and why]` | `[What made them pay]` |
| 🎯 10 customers | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[Channel that worked]` | `[Pattern noticed]` |
| 📈 $1,000 MRR | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[What changed]` | `[What to double down on]` |
| 🚀 50 customers | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[Growth engine]` | `[Biggest lesson]` |
| 💥 100 customers | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[What clicked]` | `[What to automate now]` |
| 🌟 250 customers | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[Primary channel]` | `[Who is your real ICP?]` |
| 🏆 **500 customers 🎉** | `YYYY-MM-DD` | `YYYY-MM-DD` | `[#]` | `[The story]` | `[What you'd tell Day 1 you]` |

---

### 14.2 Retention & Churn Tracker

| Month | New Customers | Churned | Net New | Total Customers | MRR |
|-------|--------------|---------|---------|-----------------|-----|
| Month 1 | `[#]` | `[#]` | `[#]` | `[#]` | `$[X]` |
| Month 2 | `[#]` | `[#]` | `[#]` | `[#]` | `$[X]` |
| Month 3 | `[#]` | `[#]` | `[#]` | `[#]` | `$[X]` |
| Month 4 | `[#]` | `[#]` | `[#]` | `[#]` | `$[X]` |
| Month 5 | `[#]` | `[#]` | `[#]` | `[#]` | `$[X]` |
| Month 6 | `[#]` | `[#]` | `[#]` | `[#]` | `$[X]` |

---

## 16. Team & Roles

<!--
  🟡 INSTRUCTIONS — Section 16: Team & Roles
  ────────────────────────────────────────────
  Even solo founders need to define who is responsible for what —
  especially when you bring on contractors, co-founders, or advisors.

  RACI CHART DEFINITIONS:
  R = Responsible  → Does the actual work
  A = Accountable  → Makes the final call / signs off
  C = Consulted    → Asked for input before decisions
  I = Informed     → Told what happened after decisions

  If you are a solo founder, almost every cell says "You (R+A)".
  That's fine — the chart still helps when you hand things off.
-->

### 16.1 Team Directory

| Name | Role / Title | Responsibilities | Contact / GitHub | Start Date |
|------|-------------|-----------------|-----------------|-----------|
| `[Your Name]` | Founder / Everything | `[Product, Code, Marketing, Support]` | `[@handle]` | `YYYY-MM-DD` |
| `[Contractor Name]` | `[UI Designer / Backend Dev / etc.]` | `[Specific scope]` | `[@handle]` | `YYYY-MM-DD` |
| `[Advisor Name]` | `[Advisor — Marketing / Technical]` | `[Monthly advisory, intro to investors]` | `[@handle]` | `YYYY-MM-DD` |

---

### 16.2 RACI Chart by Function

| Function | You (Founder) | Designer | Dev Contractor | Advisor |
|----------|:---:|:---:|:---:|:---:|
| Product strategy & vision | **A+R** | I | I | C |
| Feature prioritization | **A+R** | C | C | C |
| UI/UX design | C | **A+R** | I | I |
| Frontend development | **A+R** | C | R | I |
| Backend / AI development | **A+R** | I | R | I |
| QA / testing | **A+R** | C | R | I |
| DevOps / deployment | **A+R** | I | C | I |
| Marketing copy & GTM | **A+R** | C | I | C |
| Customer support | **A+R** | I | I | I |
| Finances & billing | **A+R** | I | I | I |
| Legal & compliance | **A+R** | I | I | C |

---

### 16.3 Responsibilities by Phase

| Phase | Primary Owner | What They're Accountable For |
|-------|-------------|------------------------------|
| Phase 0 — Discovery | `[You]` | User interviews, problem validation, waitlist |
| Phase 1 — MVP Build | `[You + Dev Contractor?]` | All MVP features shipped and working |
| Phase 2 — Beta | `[You]` | Beta recruitment, feedback synthesis, bug fixes |
| Phase 3 — Launch | `[You]` | Launch execution, community posts, first sales |
| Phase 4 — Growth | `[You]` | GTM channels, content, customer success, hiring |

---

### 16.4 When to Hire / Delegate

<!--
  Copy this checklist. When you hit the trigger, it's time to bring someone in.
-->

| Role | Hire When... | Type |
|------|-------------|------|
| Designer | You've gotten 3+ complaints about UI/UX from users | Freelance first |
| Backend Dev | Your codebase is taking > 50% of your time to maintain | Part-time contractor |
| Customer Support | Spending > 2 hrs/day on support tickets | VA / part-time hire |
| Marketing | Organic growth has flatlined after 90 days of effort | Growth freelancer |
| Full-time Co-founder | You've validated the idea AND feel you need a partner daily | Co-founder (equity) |

---

## 17. Legal & Compliance Checklist

<!--
  🟡 INSTRUCTIONS — Section 17: Legal & Compliance
  ───────────────────────────────────────────────────
  You don't need a lawyer to get started — but you do need the basics.
  Check these off before you launch publicly.

  IMPORTANT: This is a checklist, NOT legal advice.
  If you're handling medical data, financial data, or EU user data at scale,
  consult an actual lawyer.

  QUICK WINS: Use free tools like:
  → Termly.io or iubenda.com to generate Privacy Policy + ToS
  → Stripe Atlas for US company formation
  → GDPR.eu for EU compliance guidance
-->

### 17.1 Pre-Launch Legal Checklist

| Category | Item | Required By | Done? | Notes |
|----------|------|------------|-------|-------|
| **Company** | Register your business entity (LLC, Sole Trader, etc.) | You | ☐ | Recommended before taking payments |
| **Company** | Open a business bank account | You | ☐ | Separate personal and business finances |
| **Privacy** | Write and publish a Privacy Policy | Law (GDPR, CCPA) | ☐ | Must state what data you collect and why |
| **Privacy** | Write and publish Terms of Service | Best practice | ☐ | Defines what users can/can't do |
| **Privacy** | Cookie banner (if using analytics/tracking) | GDPR (EU users) | ☐ | Use Cookiebot or CookieYes |
| **Data** | Define what user data you store | GDPR / CCPA | ☐ | List it in your Privacy Policy |
| **Data** | Implement user data deletion on request | GDPR (Right to be Forgotten) | ☐ | Add a "Delete my account" feature |
| **Data** | Never store raw passwords | Security law | ☐ | Use bcrypt hashing or delegate to Clerk/Supabase |
| **Payments** | Use a licensed payment processor (Stripe, LemonSqueezy) | PCI-DSS | ☐ | Never handle raw card numbers yourself |
| **AI** | Document your AI model usage in Privacy Policy | Best practice | ☐ | State if Claude/OpenAI processes user data |
| **AI** | Review Anthropic's Terms of Service for your use case | Anthropic ToS | ☐ | Ensure your use case is permitted |
| **Email** | Include unsubscribe link in all marketing emails | CAN-SPAM / GDPR | ☐ | Mandatory for marketing emails |
| **Email** | Don't email users who haven't opted in | GDPR | ☐ | Double opt-in for EU users |
| **Copyright** | Ensure all images, fonts, icons are licensed | IP Law | ☐ | Use Unsplash, Lucide, Google Fonts |

---

### 17.2 Data Handling Map

<!--
  For every type of user data you collect, document it here.
  This becomes your Privacy Policy's backbone and helps you comply with GDPR/CCPA.
-->

| Data Type | What You Collect | Why You Collect It | Where It's Stored | Who Can See It | Retention Period |
|-----------|-----------------|-------------------|------------------|----------------|-----------------|
| **Email address** | User's email | Account login, communications | `[Supabase / Your DB]` | You + Email provider | Until account deleted |
| **Password hash** | Hashed password (never raw) | Authentication | `[Supabase Auth / Clerk]` | No one (hashed) | Until account deleted |
| **Usage data** | Pages visited, features used | Product analytics | `[PostHog / Plausible]` | You only | 12 months rolling |
| **AI prompts / inputs** | What user types into your AI feature | To generate AI response | `[Your DB / not stored?]` | You + Anthropic (via API) | `[Define retention]` |
| **Billing info** | Name, card last 4 digits | Subscription billing | `[Stripe — never your DB]` | Stripe only | Per Stripe policy |
| **Support messages** | What user says in support | To resolve issues | `[Crisp / Intercom / Email]` | You only | 2 years |
| `[Add your data types]` | `[What]` | `[Why]` | `[Where]` | `[Who]` | `[How long]` |

---

### 17.3 AI-Specific Compliance Notes

| Topic | What You Need to Know | Your Action |
|-------|----------------------|-------------|
| **User data sent to Claude API** | When a user's input goes to Claude, Anthropic processes it. This must be disclosed. | Add to Privacy Policy: "We use Claude (Anthropic) to power AI features. Your inputs may be processed by Anthropic per their Privacy Policy." |
| **AI output accuracy disclaimer** | AI can be wrong. You may be liable if users act on incorrect AI output. | Add to ToS: "AI-generated content is for informational purposes only. Verify before acting." |
| **Storing AI conversations** | If you store chat history, it's user data subject to GDPR. | Define retention period; allow users to delete their chat history. |
| **Automated decisions** | If your AI makes decisions that affect users (e.g., credit, hiring), additional GDPR rules apply. | Consult a lawyer if AI makes consequential decisions. |
| **Children's data** | If users under 13 (US) or 16 (EU) might use your product, strict rules apply. | Add age verification or explicitly restrict to adults in your ToS. |

---

## 15. Revision History

<!--
  🟡 INSTRUCTIONS — Section 15: Revision History
  ─────────────────────────────────────────────────
  Every time you make a meaningful update to this document,
  add a row here. This keeps everyone on the same page
  and shows how your thinking evolved over time.

  "Meaningful" = changed strategy, added/removed features,
  updated milestones, changed pricing, major pivot.
  NOT: fixed a typo, updated a date.
-->

| Version | Date | Author | What Changed | Why It Changed |
|---------|------|--------|--------------|----------------|
| `1.0` | `YYYY-MM-DD` | `[Your name]` | Initial draft | `First version` |
| `1.1` | `YYYY-MM-DD` | `[Your name]` | `[Description of change]` | `[Reason for change]` |
| `1.2` | `YYYY-MM-DD` | `[Your name]` | `[Description of change]` | `[Reason for change]` |

---

## 📎 Appendix

### A. Glossary (For Beginners)

| Term | Plain English Definition |
|------|--------------------------|
| **MVP** | Minimum Viable Product — the simplest version that solves the core problem |
| **ICP** | Ideal Customer Profile — a description of your perfect customer |
| **NPS** | Net Promoter Score — a survey question: "Would you recommend us 0–10?" Scores above 30 are good |
| **MRR** | Monthly Recurring Revenue — how much money you make every month from subscriptions |
| **Churn** | When a customer cancels. High churn = customers leaving faster than you acquire them |
| **LLM** | Large Language Model — the AI brain behind Claude, GPT, etc. |
| **Token** | A chunk of text (~¾ of a word). Claude charges per token used |
| **Prompt** | The text you send to an AI to get a response |
| **Agent** | An AI system that can take actions, not just generate text |
| **RICE Score** | A formula to prioritize features: (Reach × Impact × Confidence) ÷ Effort |
| **GTM** | Go-To-Market — the strategy for how you launch and sell your product |
| **Guardrail** | A rule that prevents an AI agent from doing something harmful or wrong |
| **P0/P1/P2** | Bug priority levels. P0 = everything is on fire. P1 = serious. P2 = moderate |
| **Vibe Coding** | Building software using AI pair-programmers with minimal manual coding |
| **Dogfooding** | Using your own product before releasing it to catch problems first |

---

### B. Quick-Start Prompt Library (Copy & Paste)

```
PROMPT 1 — Fill in the product snapshot
─────────────────────────────────────────────────────────────────────
"I'm building a [describe your product in 2 sentences].
My target user is [describe them]. Help me fill out a Product Roadmap
for this product, starting with the product snapshot and vision sections."

PROMPT 2 — Generate user personas
─────────────────────────────────────────────────────────────────────
"Create 2 detailed user personas for a [SaaS/mobile app] that [what it does].
For each persona include: name, age, job, frustrations, current workaround,
what would make them pay, and where they hang out online."

PROMPT 3 — Prioritize your features
─────────────────────────────────────────────────────────────────────
"Here are all the features I'm considering: [list features].
I'm a solo founder. Using RICE scoring, prioritize which 3 features
should be in the MVP, which go to Phase 2, and which to defer."

PROMPT 4 — Design your AI agent
─────────────────────────────────────────────────────────────────────
"I want to add an AI agent to my [product type] that [what it does].
Design the agent including: system prompt, tools it needs, guardrails,
fallback behavior, and estimated Claude API cost per 1,000 calls."

PROMPT 5 — Draft your GTM plan
─────────────────────────────────────────────────────────────────────
"My product is [name] — [one-line pitch]. Target user: [persona].
Price: $[X]/mo. I'm a solo founder with $[X] marketing budget.
Create a Go-To-Market plan to reach my first 500 customers."
```

---

---

## Appendix C — Worked Example: "TaskAI" 🤖

<!--
  This is a COMPLETELY FILLED-OUT example of the template using a fictional product.
  Product: TaskAI — an AI task manager for solo founders.
  Use this as a guide for what good answers look like.
  Your answers will be different — this just shows the depth expected.
-->

> **📌 HOW TO USE THIS EXAMPLE**
> Read each section below. Then go back to the blank template above and fill in YOUR version.
> The goal is to show what "done well" looks like — not to copy these answers.

---

### [EXAMPLE] Section 1 — Product Snapshot

| Field | Example Answer |
|-------|---------------|
| **Product Name** | TaskAI |
| **One-Line Pitch** | TaskAI helps solo founders clear their task list 3x faster using an AI copilot that writes, prioritizes, and executes tasks for you — no project manager needed. |
| **Product Type** | ✅ SaaS Web App + ✅ Mobile App (iOS) |
| **Current Status** | In Development |
| **Document Owner** | Alex Rivera |
| **Target Launch Date** | 2026-12-01 |
| **Primary AI Tool** | ✅ Claude (Anthropic) |
| **Primary Dev Environment** | Cursor + Claude Code |
| **Hosting Platform** | Vercel (frontend) + Railway (backend) + Supabase (DB) |
| **Target Customer Count** | 500 paying users by 2027-03-31 |

---

### [EXAMPLE] Section 2 — Vision & Strategy

**Vision:**
> *"By 2028, every solo founder will have an AI operations partner in TaskAI — making the chaos of wearing 50 hats feel manageable, and making heavyweight project tools like Asana irrelevant for one-person businesses."*

**Mission:**
> *"TaskAI helps solo founders stay focused by turning vague to-do lists into clear, AI-prioritized action plans — so they spend time building, not managing."*

**North Star Metric:**

| Metric | Target |
|--------|--------|
| Weekly Active Users completing at least 5 tasks via AI | 500 WAU with 45% week-4 retention |

**Strategic Bets:**

| # | Bet | Why |
|---|-----|-----|
| 1 | Solo founders hate traditional PM tools — they're built for teams | Every founder I interviewed said Notion/Asana felt like "overkill" |
| 2 | AI can do 80% of task planning if given the right context | Claude can turn "ship my app" into a 10-step action plan in seconds |
| 3 | Mobile-first task completion is an unserved niche in AI productivity | No AI task tool has a great mobile UX yet |

---

### [EXAMPLE] Section 3 — Target Users & Problem Statement

**Primary Persona: "Founder Felix"**

| Field | Details |
|-------|---------|
| **Persona Name** | Founder Felix |
| **Age / Role** | 31 / Solo SaaS Founder |
| **Where They Work** | Home office |
| **Technical Level** | Semi-Technical |
| **Their #1 Job** | Ship product and grow revenue |
| **Their #1 Frustration** | Every morning he opens his 200-item Notion to-do list and freezes. He doesn't know where to start. |
| **How They Solve It Today** | Manually reviewing Notion tasks, trying to prioritize by gut feel |
| **Why That Sucks** | He spends 45 min/day just deciding what to work on. That's 3.5 hrs/week on planning instead of doing. |
| **Where They Hang Out** | Twitter/X, Indie Hackers, r/startups, Solo Founder Discord |
| **What They'll Pay** | $20–$39/mo for a tool that actually saves him time |

**Problem Statement:**
> **Founder Felix** struggles to prioritize his 200+ tasks each morning because he has no AI system that understands his business context and goals.
>
> Today, he reviews his Notion database manually and picks tasks by gut feel — which costs him 45 minutes every day and leads to working on low-priority tasks.
>
> If nothing changes, he'll continue grinding on the wrong things, miss his launch deadline, and eventually burn out.

---

### [EXAMPLE] Section 5 — Phase 0 Highlights

**What was learned from 10 user interviews:**
- 9/10 founders said "I lose at least 30 min/day to deciding what to work on"
- 7/10 already used Claude for writing, but not for task management
- Willingness to pay: 6/10 said yes to $29/mo without hesitation
- Surprising insight: Founders want the AI to explain *why* it prioritized a task, not just list it

**Waitlist:** 47 signups in the first 5 days after posting on Indie Hackers

---

### [EXAMPLE] Section 6 — Feature Prioritization

| Feature | Why It's In MVP | Priority | RICE Score |
|---------|----------------|----------|-----------|
| AI Task Prioritizer (ranks your list by impact) | The #1 pain from interviews | 🔴 P0 | 87 |
| Natural language task creation ("add task: review pricing") | Removes friction of task entry | 🔴 P0 | 74 |
| Daily AI briefing (3 things to do today, generated at 8am) | The "wow" moment Felix described in interviews | 🟡 P1 | 62 |
| Mobile app (iOS) | 60% of beta users said they check tasks on phone | 🟡 P1 | 55 |
| Team collaboration | Founders are solo — not needed yet | ⚫ P3 | — |
| Calendar sync | Nice to have, complex to build | ⚫ P3 | — |

**NOT in MVP:**
- ❌ Calendar sync — complex API integration; not mentioned in top 3 pains
- ❌ Time tracking — only 2/10 users asked for it
- ❌ Team features — our ICP is solo founders

---

### [EXAMPLE] Section 8 — AI Agent: "Daily Briefing Agent"

| Field | Example Answer |
|-------|---------------|
| **Agent Name** | Daily Briefing Agent |
| **Agent Role** | Generates a personalised "top 3 priorities for today" based on the user's task list, deadlines, and goals — delivered every morning at 8am. |
| **Trigger** | Scheduled cron job — 8:00am in user's timezone |
| **Input** | User's full task list, project goals, recent activity, any deadlines in the next 7 days |
| **Core Prompt** | `"You are a Chief of Staff for a solo SaaS founder. Given their task list below, identify the top 3 highest-impact tasks for today. For each task: state why it matters, estimate time to complete, and flag any dependency. Be concise. The founder is busy. [TASK LIST: {task_list}] [GOALS: {user_goals}] [DEADLINES: {deadlines}]"` |
| **Output** | A formatted daily briefing: 3 tasks with explanations, estimated time, and 1 "quick win" bonus task |
| **AI Model Used** | claude-3-5-sonnet-20241022 (balanced quality and cost) |
| **Tools / Functions** | `get_user_tasks()`, `get_user_goals()`, `get_upcoming_deadlines()`, `send_push_notification()` |
| **Max Tokens / Cost Limit** | Max 800 output tokens = ~$0.012/briefing/user/day. At 500 users: ~$6/day = $180/month |
| **Guardrails** | Never invent tasks; only use tasks from the DB. Never reschedule a deadline without user confirmation. If task list is empty, send an encouraging empty-state message. |
| **Fallback Behavior** | If API call fails, send fallback message: "Your AI briefing is taking longer than usual. Check your tasks manually today." |
| **Logging** | Input + output saved to `briefing_logs` table with timestamp and user_id for quality review |
| **Human-in-the-Loop?** | No — fully automated. User sees the output and can dismiss or accept suggestions |

---

### [EXAMPLE] Section 10 — Budget at Launch (Month 1)

| Category | Tool | Est. Monthly Cost |
|----------|------|-----------------|
| Claude API | Anthropic | $45/mo (at 100 beta users, ~2 briefings/day each) |
| Hosting | Vercel Pro + Railway Starter | $20 + $5 = $25/mo |
| Database | Supabase Pro | $25/mo |
| Auth | Clerk Free → Pro at 500 MAU | $0 → $25/mo |
| Email | Resend Free | $0 |
| Analytics | PostHog Free | $0 |
| Error Monitoring | Sentry Free | $0 |
| Domain | Cloudflare | $1/mo |
| Dev Tools | Cursor Pro | $20/mo |
| **TOTAL (Month 1 MVP)** | | **~$116/mo** |

---

### [EXAMPLE] Section 12 — Go-To-Market (First 500 Customers)

| Channel | What Felix Does | Result |
|---------|----------------|--------|
| Twitter/X build-in-public | Posts daily screenshots of TaskAI in action, growth stats, lessons | 800 followers → 80 signups in month 1 |
| Indie Hackers | Wrote launch post: "I built an AI task manager in 6 weeks" | 1,200 upvotes, 120 signups |
| Product Hunt | Launched on a Tuesday, got 340 upvotes, #4 of the day | 200 signups in 48 hours |
| Email list | Sent 3-email onboarding series to 340 waitlist members | 28% converted to trial |
| SEO content | Wrote "How I use Claude to prioritize my startup tasks" | 2,100 organic visitors in month 2 |

**Pricing:**
- Free: 20 tasks, 1 AI briefing/day
- Pro ($29/mo): Unlimited tasks, full AI briefing, mobile app
- Founder ($49/mo): Everything + Slack bot + weekly AI review

---

### [EXAMPLE] Section 14 — Customer Milestone Log

| Milestone | Date Achieved | Days to Hit | How | Learning |
|-----------|--------------|-------------|-----|---------|
| First line of code | 2026-10-14 | Day 1 | Started with Next.js + Supabase scaffold via Claude Code | Claude Code scaffolded 80% of auth in 20 minutes |
| 10 waitlist signups | 2026-10-16 | Day 3 | One tweet about the idea | "Build in public before you build the product" |
| MVP shipped to 5 beta users | 2026-11-01 | Day 18 | Invited Indie Hacker connections | First user session was 27 minutes — that's product-market fit signal |
| First $1 in revenue | 2026-11-15 | Day 32 | Beta user upgraded to Pro after 5 days | "People pay when they feel the pain being solved, not when they see features" |
| 10 paying customers | 2026-11-28 | Day 45 | Product Hunt micro-launch | All 10 from Product Hunt — IH + PH are the right channels |
| 50 paying customers | 2026-12-20 | Day 67 | SEO post went viral on Hacker News | Organic SEO is slow but free — start writing early |
| 100 customers | 2027-01-10 | Day 88 | Referral program launched | Every 5th customer came from a referral |
| **500 customers 🎉** | 2027-03-15 | Day 152 | Combination of SEO, referrals, and PH re-feature | "The bottleneck was retention, not acquisition — fix onboarding first" |

---

*End of Worked Example — TaskAI is fictional. Use it as inspiration only.*

---

*Document Template Version: 1.1 | Created: 2026-10-13 | Updated: 2026-10-13 | Framework: AI-Driven Development Life Cycle*
*Designed for Solo Founders building SaaS & Mobile Products with Vibe Coding + Claude AI*
