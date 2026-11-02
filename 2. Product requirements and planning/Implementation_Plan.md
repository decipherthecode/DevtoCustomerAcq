# 📖 HOW TO FILL THIS DOCUMENT (Read Me First!)

> **Who is this for?** Anyone building an AI-powered product — solo founders, tiny teams, or first-time builders. If you have never written an implementation plan before, that is perfectly fine. Every section below tells you **exactly what to write** and gives you a **real example** to copy and adapt.

## ✏️ 5 Simple Rules Before You Start

1. **Replace every line that starts with `>` —** those are instructions. Delete the `>` line after you fill in your own answer.
2. **Delete sections you don't need yet** — it's better to have a short accurate plan than a long empty one.
3. **Use plain language** — write the way you'd explain it to a friend, not a professor.
4. **Update this doc as you build** — it is a living document, not a one-time report.
5. **When in doubt, write less** — a one-sentence answer is always better than leaving it blank.

---
---

# 🚀 Implementation Plan

| Field | Details |
|---|---|
| **Project Name** | *(What is your product called?)* |
| **Document Version** | `v1.0` |
| **Last Updated** | *(Today's date — e.g., October 14, 2026)* |
| **Owner / Author** | *(Your name or handle)* |
| **Status** | `🟡 Draft` → `🟢 Active` → `✅ Complete` |
| **Target Launch Date** | *(When do you want to go live?)* |
| **500-Customer Goal Date** | *(When do you want to reach 500 paying/active customers?)* |

---

## 📌 Table of Contents

1. [Project Overview](#1-project-overview)
2. [Problem & Solution](#2-problem--solution)
3. [Product Scope](#3-product-scope)
4. [AI Stack & Tech Choices](#4-ai-stack--tech-choices)
5. [Team & Roles](#5-team--roles)
6. [Phase-by-Phase Plan](#6-phase-by-phase-plan)
7. [AI Agent Workflow Design](#7-ai-agent-workflow-design)
8. [Risk, Rollback & Quality Checks](#8-risk-rollback--quality-checks)
9. [Go-to-Market & 500-Customer Plan](#9-go-to-market--500-customer-plan)
10. [Compliance & Privacy Checklist](#10-compliance--privacy-checklist)
11. [Milestone Tracker](#11-milestone-tracker)
12. [Change Log](#12-change-log)

---

## 1. Project Overview

> **How to fill this:** Write 3–5 sentences that explain what you're building, who it's for, and why it matters. Imagine you're texting a friend who has never heard of your idea.

**One-Line Summary:**

> *Example: "An AI scheduling assistant that reads your emails and automatically books meetings so busy freelancers never miss a client call."*

---

**Elevator Pitch (3–5 sentences):**

> *Example: "Most freelancers lose 2+ hours a week playing email ping-pong to book client meetings. Our app uses Claude AI to read the conversation, understand availability, and send a calendar invite — automatically. No more back-and-forth. It works on web and mobile, and the first version will be live in 8 weeks."*

---

**Key Links:**

| Resource | Link |
|---|---|
| GitHub / Code Repo | *(Paste your repo URL or write "TBD")* |
| Design / Wireframes | *(Figma, Excalidraw, or "None yet")* |
| Project Board | *(GitHub Project, Notion, or "This file")* |
| Staging URL | *(Will be added after Phase 2)* |
| Production URL | *(Will be added at launch)* |

---

## 2. Problem & Solution

### 2.1 The Problem

> **How to fill this:** Describe the pain point your product fixes. Answer these three questions:
> - **Who** has this problem?
> - **What** exactly is the problem?
> - **Why** is it painful or expensive to leave it unsolved?

**Who has this problem?**

> *Example: "Freelance designers and consultants who communicate with clients via email."*

**What is the problem?**

> *Example: "Scheduling a single meeting takes an average of 6 email exchanges and wastes 20 minutes of their time."*

**Why does it hurt?**

> *Example: "It breaks focus, delays projects, and makes them look unprofessional when they forget to follow up."*

---

### 2.2 The Solution

> **How to fill this:** Describe what your product does in simple steps. Think: "When the user does X, the AI does Y, and the result is Z."

**Core Solution:**

> *Example: "When a user forwards a client email thread to our app, Claude AI reads it, detects the meeting request, checks the user's calendar, and sends a polished booking link — all in under 30 seconds."*

**Why AI makes this better than existing tools:**

> *Example: "Calendly requires the client to pick a slot. Our AI understands natural language ('Let's meet next week, mornings are best') and handles the entire back-and-forth automatically — no manual setup needed."*

---

### 2.3 Success Metrics (How We Know We Won)

> **How to fill this:** Pick 2–4 numbers that prove your product is working. These are called KPIs (Key Performance Indicators). Don't overthink it — just think "what number going up means we're winning?"

| Metric | Starting Value | Target at Launch | Target at 500 Customers |
|---|---|---|---|
| *Example: Active users/week* | *0* | *50* | *500+* |
| *Example: Time saved per user* | *0 min* | *20 min/week* | *20+ min/week* |
| *Example: AI task success rate* | *N/A* | *> 85%* | *> 95%* |
| *(Add your own)* | | | |

---

## 3. Product Scope

> **How to fill this:** List exactly what your product WILL and WON'T do in the first version. This prevents scope creep (when the project keeps growing and never ships).

### 3.1 ✅ In Scope (We ARE building this)

> *List the features you are committing to build before launch. Be specific.*

- [ ] Feature 1: *(e.g., "User can sign up and connect their Google Calendar")*
- [ ] Feature 2: *(e.g., "AI reads forwarded email and extracts meeting request")*
- [ ] Feature 3: *(e.g., "App sends booking link to the email thread")*
- [ ] Feature 4: *(e.g., "Mobile-responsive web app")*
- [ ] Feature 5: *(e.g., "Basic dashboard showing meetings booked this week")*

### 3.2 ❌ Out of Scope (We are NOT building this — yet)

> *List things people might expect but that you're saving for later. This is how you ship fast.*

- *(e.g., "Native iOS/Android app — web first")*
- *(e.g., "Outlook/Office 365 integration — only Gmail in v1")*
- *(e.g., "Team accounts — solo users only at launch")*
- *(e.g., "AI-generated meeting agendas — Phase 2 feature")*

### 3.3 🤔 Parking Lot (Ideas to revisit later)

> *Great ideas you don't want to forget but won't build now.*

- *(e.g., "AI follow-up reminders")*
- *(e.g., "Slack integration")*
- *(e.g., "Analytics dashboard for meeting trends")*

---

## 4. AI Stack & Tech Choices

> **How to fill this:** List the tools and services you'll use to build the product. If you're not technical, just copy the example and change what doesn't apply.

### 4.1 AI Layer

| Component | Tool / Service | Why We Chose It |
|---|---|---|
| **Primary LLM** | Anthropic Claude (claude-sonnet-4-5 or latest) | Best reasoning + instruction-following for our use case |
| **AI Framework** | *(e.g., Claude API directly / LangChain / LlamaIndex)* | *(e.g., "Simple direct API calls — no extra complexity needed")* |
| **Prompt Storage** | *(e.g., Markdown files in `/prompts` folder)* | *(e.g., "Version-controlled alongside code")* |
| **AI Observability** | *(e.g., Langfuse / Helicone / Custom logging)* | *(e.g., "Track token costs and failures")* |
| **Model Fallback** | *(e.g., claude-haiku-3-5 for simple tasks)* | *(e.g., "10× cheaper for low-complexity steps")* |

### 4.2 Frontend

| Component | Tool | Notes |
|---|---|---|
| **Web Framework** | *(e.g., Next.js / React / Svelte)* | |
| **Mobile** | *(e.g., Expo / React Native / PWA / None in v1)* | |
| **UI Library** | *(e.g., Tailwind CSS + shadcn/ui)* | |
| **Hosting** | *(e.g., Vercel / Netlify / Cloudflare Pages)* | |

### 4.3 Backend & Data

| Component | Tool | Notes |
|---|---|---|
| **Backend / API** | *(e.g., Next.js API Routes / Supabase Edge Functions)* | |
| **Database** | *(e.g., Supabase / PlanetScale / SQLite via Turso)* | |
| **Auth** | *(e.g., Supabase Auth / Clerk / NextAuth)* | |
| **File Storage** | *(e.g., Supabase Storage / Cloudflare R2)* | |
| **Queue / Jobs** | *(e.g., Trigger.dev / Inngest / None)* | |

### 4.4 Development Tools (Vibe Coding Setup)

| Tool | Purpose |
|---|---|
| **Cursor / Claude Code** | AI-assisted code generation and refactoring |
| **GitHub / GitLab** | Version control and code review |
| **Claude MCP servers** | Extend Claude with local tools (file access, browser, etc.) |
| *(Add others)* | |

### 4.5 Third-Party APIs & Integrations

| Service | What It Does | Free Tier? | Monthly Cost Estimate |
|---|---|---|---|
| *Example: Google Calendar API* | *Read/write calendar events* | *Yes* | *$0* |
| *Example: Anthropic Claude API* | *Core AI reasoning* | *No* | *~$20–$50* |
| *(Add yours)* | | | |

---

## 5. Team & Roles

> **How to fill this:** Even if you're solo, fill this out. If one person is doing everything, write their name in all rows. This section helps you spot gaps.

### 5.1 Core Team

| Role | Name / Handle | Responsibilities | Time Commitment |
|---|---|---|---|
| **Product Owner** | *(Your name)* | Decides what to build and in what order | *(e.g., Full-time)* |
| **AI/Prompt Engineer** | *(Your name or teammate)* | Designs prompts, evaluates AI output quality | *(e.g., 50% of time)* |
| **Frontend Developer** | *(Your name or "Using Cursor AI")* | Builds UI, connects to backend | *(e.g., Full-time)* |
| **Backend Developer** | *(Your name or "Using Claude Code")* | API design, database, integrations | *(e.g., Full-time)* |
| **QA / Tester** | *(Your name or beta user)* | Finds bugs before users do | *(e.g., 10% of time)* |
| **Marketing / GTM** | *(Your name)* | Gets first 500 customers | *(e.g., 20% after Phase 4)* |

### 5.2 External Support (Optional)

| Who | What They Help With | Cost |
|---|---|---|
| *Example: Freelance designer* | *Logo and landing page design* | *$200 one-time* |
| *Example: Domain expert / advisor* | *Industry knowledge for prompt design* | *Free / equity* |

---

## 6. Phase-by-Phase Plan

> **How to fill this:** This is the heart of the document. Each phase is a chapter of your build journey. Fill in the dates, tasks, and mark tasks as done with `[x]` as you complete them.
>
> **How to read the status icons:**
> - 🔲 = Not started yet
> - 🔄 = In progress right now
> - ✅ = Done!
> - ⏸️ = Paused or blocked
> - ❌ = Cancelled

---

### Phase 0: Discovery & Foundation *(~1–2 weeks)*

**Goal:** Understand the problem deeply and set up your environment before writing a single line of code.

**Start Date:** ___________  **End Date:** ___________

#### 0.1 Research & Validation

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 0.1.1 | Interview 5 potential users about the problem | | 🔲 | *Ask open-ended questions — don't pitch yet* |
| 0.1.2 | Document key pain points from interviews | | 🔲 | *Look for patterns across 3+ people* |
| 0.1.3 | Research 3–5 existing competitors | | 🔲 | *What do they do well? What's missing?* |
| 0.1.4 | Define your Unique Value Proposition (UVP) | | 🔲 | *"Only we do X better than anyone else because…"* |
| 0.1.5 | Validate willingness to pay (ask users directly) | | 🔲 | *"Would you pay $X/month for this?"* |

#### 0.2 Planning & Setup

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 0.2.1 | Fill in this Implementation Plan fully | | 🔲 | *You are doing this right now!* |
| 0.2.2 | Set up GitHub repo with folder structure | | 🔲 | *See recommended structure below* |
| 0.2.3 | Set up Anthropic Claude API account & get API key | | 🔲 | *console.anthropic.com* |
| 0.2.4 | Set up staging environment (Vercel / Netlify etc.) | | 🔲 | |
| 0.2.5 | Create basic `.env` file with all required keys | | 🔲 | *Never commit this file to GitHub* |
| 0.2.6 | Install and configure Cursor / Claude Code | | 🔲 | *Your AI coding assistant* |

**📁 Recommended Folder Structure:**

```
/my-ai-product
  /app             ← Frontend code
  /api             ← Backend / server code
  /prompts         ← All Claude prompt files (version them!)
  /agents          ← AI agent definitions and workflows
  /tests           ← Automated tests
  /docs            ← Documentation (this plan lives here)
  /scripts         ← Utility scripts (deployment, seeding, etc.)
  .env             ← Secret keys (NEVER commit to git)
  .env.example     ← Template for secrets (safe to commit)
```

**Phase 0 Exit Criteria (all must be ✅ before moving on):**
- [ ] At least 5 user interviews completed and documented
- [ ] Competitors researched and UVP defined
- [ ] Dev environment fully set up and working
- [ ] This Implementation Plan is at least 70% filled in

---

### Phase 1: Prototype & Proof of Concept *(~1–2 weeks)*

**Goal:** Build the simplest possible version that proves the AI can do the core task. No UI needed yet — just make the AI work.

**Start Date:** ___________  **End Date:** ___________

#### 1.1 AI Core Proof of Concept

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 1.1.1 | Write the first version of the core prompt | | 🔲 | *Start simple — 5–10 lines max* |
| 1.1.2 | Test the prompt manually in Claude.ai (no code) | | 🔲 | *Run 20+ test cases by hand* |
| 1.1.3 | Identify the top 3 failure modes of the prompt | | 🔲 | *What inputs break it?* |
| 1.1.4 | Iterate prompt until 80% of test cases pass | | 🔲 | *80% is good enough for a prototype* |
| 1.1.5 | Write a basic script that calls the Claude API | | 🔲 | *Just `console.log` the result is fine* |
| 1.1.6 | Log raw inputs and outputs to a file | | 🔲 | *You'll need this for debugging later* |

#### 1.2 Core Data & Backend Skeleton

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 1.2.1 | Design the database schema (tables and fields) | | 🔲 | *Sketch on paper first — keep it simple* |
| 1.2.2 | Set up database (Supabase or chosen tool) | | 🔲 | |
| 1.2.3 | Create the 2–3 most important API endpoints | | 🔲 | *Only what the AI feature needs right now* |
| 1.2.4 | Test API endpoints work with Postman or curl | | 🔲 | |

**Phase 1 Exit Criteria:**
- [ ] AI can complete the core task with ≥ 80% accuracy on test inputs
- [ ] API can receive input and return AI output
- [ ] Database is set up and accepting test data

---

### Phase 2: MVP Build — Core Features *(~3–5 weeks)*

**Goal:** Build a working product end-to-end. Real UI, real users can try it, real AI doing the work.

**Start Date:** ___________  **End Date:** ___________

#### 2.1 Authentication & User Accounts

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 2.1.1 | Implement user sign-up (email or Google OAuth) | | 🔲 | |
| 2.1.2 | Implement user login and session management | | 🔲 | |
| 2.1.3 | Implement password reset flow | | 🔲 | |
| 2.1.4 | Protect all API routes — unauthenticated = blocked | | 🔲 | |

#### 2.2 Core Feature Build (Your AI Feature)

> *Replace the example tasks below with YOUR product's specific features.*

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 2.2.1 | *(e.g., "Build email parsing input form")* | | 🔲 | |
| 2.2.2 | *(e.g., "Connect frontend to Claude API endpoint")* | | 🔲 | |
| 2.2.3 | *(e.g., "Show AI output to user with copy button")* | | 🔲 | |
| 2.2.4 | *(e.g., "Add user feedback: 👍 / 👎 on AI responses")* | | 🔲 | |
| 2.2.5 | *(e.g., "Save history of AI interactions per user")* | | 🔲 | |
| 2.2.6 | *(Add your own feature tasks here)* | | 🔲 | |

#### 2.3 UI & User Experience

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 2.3.1 | Build landing page (the page before sign-up) | | 🔲 | *Focus on the headline and one CTA* |
| 2.3.2 | Build onboarding flow (3 steps max) | | 🔲 | *First-time user experience matters most* |
| 2.3.3 | Build main app dashboard / home screen | | 🔲 | |
| 2.3.4 | Ensure all pages are mobile-responsive | | 🔲 | *Test on your phone at every step* |
| 2.3.5 | Add loading states while AI is thinking | | 🔲 | *Streaming response or spinner* |
| 2.3.6 | Add error messages when something goes wrong | | 🔲 | *"Something went wrong — try again" is fine* |

#### 2.4 Payments (If Charging at Launch)

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 2.4.1 | Set up Stripe / Lemon Squeezy account | | 🔲 | *Lemon Squeezy is easier for solo founders* |
| 2.4.2 | Create pricing plans (monthly / yearly) | | 🔲 | |
| 2.4.3 | Build upgrade / payment page | | 🔲 | |
| 2.4.4 | Test payment flow end-to-end in sandbox mode | | 🔲 | |
| 2.4.5 | Gate premium features behind paid tier | | 🔲 | |

**Phase 2 Exit Criteria:**
- [ ] A real person can sign up, use the AI feature, and see results — without your help
- [ ] No critical errors (app doesn't crash for basic use cases)
- [ ] Payments work (if charging at launch)
- [ ] Works on mobile browsers

---

### Phase 3: Alpha Testing *(~1 week)*

**Goal:** Give the product to 5–15 trusted people (friends, colleagues, target users). Collect feedback before the world sees it.

**Start Date:** ___________  **End Date:** ___________

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 3.1 | Identify 5–15 alpha testers (write their names below) | | 🔲 | |
| 3.2 | Create a simple feedback form (Tally / Typeform) | | 🔲 | *Ask: "What confused you? What would you pay for?"* |
| 3.3 | Send alpha testers access + instructions | | 🔲 | |
| 3.4 | Monitor usage and check for crashes daily | | 🔲 | |
| 3.5 | Do a 20-minute call with each tester if possible | | 🔲 | *You learn 10× more from talking than surveys* |
| 3.6 | Fix all Critical bugs (app-breaking issues) | | 🔲 | *These MUST be fixed before beta* |
| 3.7 | Prioritize feedback into: "Fix now", "Later", "No" | | 🔲 | |
| 3.8 | Update AI prompts based on real user inputs | | 🔲 | |

**Alpha Testers List:**

| Name | Email | Feedback Collected? | Key Insight |
|---|---|---|---|
| 1. | | ☐ | |
| 2. | | ☐ | |
| 3. | | ☐ | |
| *(Add more)* | | | |

**Phase 3 Exit Criteria:**
- [ ] At least 5 people completed the core user journey
- [ ] All "Critical" bugs fixed
- [ ] At least 3 pieces of actionable feedback collected and reviewed

---

### Phase 4: Hardening & Launch Prep *(~1–2 weeks)*

**Goal:** Make the product reliable, secure, and ready for the public. This is the "boring but important" phase.

**Start Date:** ___________  **End Date:** ___________

#### 4.1 Performance & Reliability

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 4.1.1 | Add error tracking (Sentry — free tier is fine) | | 🔲 | *You'll know when things break without a user telling you* |
| 4.1.2 | Add basic analytics (Plausible / PostHog free tier) | | 🔲 | *See which pages users visit and drop off* |
| 4.1.3 | Set up Claude API cost alerts (daily limit) | | 🔲 | *Prevent surprise $500 AI bills* |
| 4.1.4 | Add rate limiting to AI endpoints | | 🔲 | *Prevent one user from draining your API budget* |
| 4.1.5 | Test app under load (10 simultaneous users min) | | 🔲 | |
| 4.1.6 | Ensure AI response times are < 10 seconds | | 🔲 | *If slower, add a "working on it…" UI* |

#### 4.2 Security

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 4.2.1 | Check all API keys are in `.env`, not in code | | 🔲 | *Search codebase for "sk-ant" and any hardcoded keys* |
| 4.2.2 | Ensure all user data is isolated per account | | 🔲 | *User A must NEVER see User B's data* |
| 4.2.3 | Add input sanitization (prevent prompt injection) | | 🔲 | *Strip or escape user inputs before sending to Claude* |
| 4.2.4 | Enable HTTPS everywhere | | 🔲 | *Vercel/Netlify do this automatically* |
| 4.2.5 | Add GDPR-compliant cookie banner (if applicable) | | 🔲 | |

#### 4.3 Documentation & Support

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 4.3.1 | Write a simple FAQ page or Help doc | | 🔲 | *Answer the top 5 questions alpha testers asked* |
| 4.3.2 | Set up a support email or chat widget | | 🔲 | *Crisp.chat or Tally form both free* |
| 4.3.3 | Write Terms of Service and Privacy Policy | | 🔲 | *Use Termageddon or a lawyer-reviewed template* |

**Phase 4 Exit Criteria:**
- [ ] Error tracking live and sending alerts
- [ ] No hardcoded API keys in the codebase
- [ ] Privacy Policy and Terms of Service pages are live
- [ ] AI cost limits are configured

---

### Phase 5: Public Launch *(~1 week)*

**Goal:** Flip the switch. Get real strangers using and paying for your product.

**Start Date:** ___________  **End Date:** ___________

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 5.1 | Remove all "beta" or "coming soon" flags | | 🔲 | |
| 5.2 | Launch on Product Hunt (schedule in advance) | | 🔲 | *Schedule for Tuesday–Thursday at 12:01 AM PST* |
| 5.3 | Post in relevant communities (Reddit, X, LinkedIn, Discord) | | 🔲 | *Be helpful, not spammy — share the story* |
| 5.4 | Email your waitlist / newsletter (if you have one) | | 🔲 | |
| 5.5 | Monitor Sentry and server logs for first 48 hours | | 🔲 | *Things will break. Be ready to fix fast.* |
| 5.6 | Reply to every single comment and review | | 🔲 | *This is your best marketing in week 1* |
| 5.7 | Track Day 1 signups and first paying customer | | 🔲 | *Note the date — it's a milestone worth celebrating!* |
| 5.8 | Set up weekly metrics email to yourself | | 🔲 | *Revenue, active users, churn, AI cost* |

**Launch Day Checklist:**

- [ ] All pages load correctly on desktop and mobile
- [ ] Sign-up flow works end-to-end
- [ ] Payment works (run a real $1 test transaction)
- [ ] Error tracking is live
- [ ] Someone is monitoring for the first 24 hours

---

### Phase 6: Growth to 500 Customers *(~4–12 weeks post-launch)*

**Goal:** Turn launch momentum into sustainable growth. Get to 500 active or paying customers.

> *See Section 9 (Go-to-Market Plan) for the detailed strategy. This phase tracks the execution.*

**Start Date (Launch Date):** ___________  **Target 500-Customer Date:** ___________

| # | Task | Owner | Status | Notes |
|---|---|---|---|---|
| 6.1 | Implement referral program or invite mechanic | | 🔲 | *Best growth lever for solo founders* |
| 6.2 | Build in-app onboarding tooltips / walkthroughs | | 🔲 | *Reduce support load and improve activation* |
| 6.3 | Start a weekly "what's new" email to users | | 🔲 | *Build habit and reduce churn* |
| 6.4 | Ship top 3 features requested during alpha/beta | | 🔲 | *Show users you're listening* |
| 6.5 | Improve AI prompts based on real usage failures | | 🔲 | *Review 👎 feedback weekly* |
| 6.6 | Optimize AI costs as volume grows | | 🔲 | *Cache repeated calls, use haiku for simple tasks* |
| 6.7 | Add "Share" or embed mechanic (if applicable) | | 🔲 | *Let your users market for you* |
| 6.8 | Reach 100 customers milestone — celebrate & reflect | | 🔲 | |
| 6.9 | Reach 500 customers milestone — document learnings | | 🔲 | |

---

## 7. AI Agent Workflow Design

> **How to fill this:** If your product uses Claude to do multi-step tasks (not just one question → one answer), use this section to map out how the AI thinks and acts. Think of it like a recipe — what ingredients go in, what steps happen, what comes out.

### 7.1 AI Feature Inventory

> *List every place in your product where Claude is called.*

| Feature Name | User Trigger | Input to Claude | Expected Output | Model Used |
|---|---|---|---|---|
| *Example: Email Parser* | *User submits email text* | *Email thread + calendar data* | *Meeting time + draft reply* | *claude-sonnet-4-5* |
| *(Your feature 1)* | | | | |
| *(Your feature 2)* | | | | |

---

### 7.2 Core Agent Workflow Diagram

> **How to fill this:** Describe how the AI works step by step for your most important feature. Use the template below.

**Feature Name:** *(e.g., "Email-to-Meeting Booking Agent")*

```
STEP 1: USER INPUT
  └── What the user provides: ___________________________

STEP 2: PRE-PROCESSING (before Claude sees it)
  └── What we clean/format/add to the input: ___________________________
  └── What context we inject (user preferences, history, etc.): ___________________________

STEP 3: CLAUDE API CALL
  └── System Prompt file: /prompts/[name].md
  └── Model: claude-sonnet-4-5 (or claude-haiku-3-5 for simple tasks)
  └── Max tokens: ___________
  └── Temperature: 0 (for factual/structured) or 0.7 (for creative)

STEP 4: CLAUDE RESPONSE
  └── Expected format: Plain text / JSON / Structured list
  └── Validation: Does it contain required fields? If not → retry or fallback

STEP 5: POST-PROCESSING
  └── What we parse/transform: ___________________________
  └── What we save to the database: ___________________________

STEP 6: OUTPUT TO USER
  └── How it appears on screen: ___________________________
  └── Any follow-up actions triggered: ___________________________

STEP 7: LOGGING & FEEDBACK
  └── What we log: input, output, latency, cost, model used
  └── How user gives feedback: 👍 / 👎 button
```

---

### 7.3 Prompt Design Record

> **How to fill this:** Document your most important prompts here. This helps you improve them over time without losing track of what changed.

**Prompt Name:** *(e.g., "Email Parser System Prompt")*
**File Location:** `/prompts/email-parser-v1.md`
**Current Version:** `v1.0`
**Last Updated:** ___________

**What This Prompt Does:**
> *(e.g., "Extracts meeting request details from an email thread and formats them as structured JSON.")*

**Key Design Decisions:**
- *(e.g., "We tell Claude to respond ONLY in JSON to make parsing easier")*
- *(e.g., "We include the user's timezone in the system prompt to avoid scheduling errors")*

**Known Failure Cases:**
- *(e.g., "Fails when email is in a language other than English — added a language detection step")*

**Prompt Version History:**

| Version | Date | Change Made | Result |
|---|---|---|---|
| v1.0 | | Initial version | |
| v1.1 | | | |

---

### 7.4 AI Cost & Token Budget

> **How to fill this:** Estimate how much each AI call costs. This prevents surprise bills.

| Feature | Avg Input Tokens | Avg Output Tokens | Model | Cost Per Call | Expected Daily Calls | Daily Cost |
|---|---|---|---|---|---|---|
| *(Example: Email Parser)* | *1,000* | *200* | *claude-sonnet* | *~$0.004* | *100* | *~$0.40* |
| *(Your feature)* | | | | | | |
| **TOTAL** | | | | | | **$___/day** |

**Monthly AI Cost Estimate:** $___________

**Cost Control Rules:**
- [ ] Set Anthropic API spend limit to $___/month
- [ ] Use `claude-haiku` for simple classification tasks
- [ ] Cache repeated prompts where possible
- [ ] Alert when daily spend exceeds $___

---

### 7.5 Multi-Agent & Tool Use (if applicable)

> *Only fill this section if your product uses Claude with tools (function calling) or multiple AI agents working together.*

**Does your product use Claude Tools / Function Calling?** Yes / No

If Yes, list the tools:

| Tool Name | What It Does | When Claude Calls It |
|---|---|---|
| `get_calendar_events` | Fetches user's calendar from Google Calendar | When planning a meeting time |
| `send_email` | Sends an email on behalf of the user | After user confirms the draft |
| *(Add your tools)* | | |

**Agent Orchestration Pattern:**
- [ ] Single agent (one Claude call per user action) — *simplest, best to start here*
- [ ] Sequential agents (Agent A output feeds Agent B)
- [ ] Parallel agents (multiple Claude calls run simultaneously)
- [ ] Human-in-the-loop (Claude proposes, user approves, then Claude acts)

---

## 8. Risk, Rollback & Quality Checks

> **How to fill this:** Think of this as your "what if things go wrong" plan. Identify risks before they happen and decide in advance how to respond.

### 8.1 Risk Register

> *Rate each risk: Likelihood (L) and Impact (I) on a 1–5 scale. Risks with L×I > 10 are HIGH PRIORITY.*

| # | Risk | L (1–5) | I (1–5) | Score | Mitigation Plan |
|---|---|---|---|---|---|
| R1 | Claude API is down or slow | 2 | 5 | 10 | Show clear error message; queue requests; display retry button |
| R2 | AI gives wrong or harmful output | 3 | 4 | 12 | Add output validation; human-review mode; user feedback → fast fix |
| R3 | API cost spike (viral moment or bug) | 2 | 5 | 10 | Daily spend cap in Anthropic console; rate limit per user |
| R4 | Data breach / user data exposed | 1 | 5 | 5 | Use Supabase RLS; no PII in prompts; regular security checks |
| R5 | Product doesn't get users after launch | 4 | 4 | 16 | Pre-launch waitlist; launch on Product Hunt; community outreach |
| R6 | Key feature doesn't work at scale | 3 | 4 | 12 | Load test in Phase 4; queue jobs for heavy processing |
| *(Add your own)* | | | | | |

**Legend:** 1 = Very unlikely / Very minor · 5 = Almost certain / Catastrophic

---

### 8.2 Rollback Plan

> **How to fill this:** If something breaks after you ship it, how do you go back to the safe version? Answer these questions now so you're not panicking later.

**How do we deploy a rollback?**
- *(e.g., "Vercel keeps the last 10 deploys. Click 'Redeploy' on the previous version in the dashboard.")*

**Who is responsible for making the call to rollback?**
- *(e.g., "Any team member can rollback immediately if 3+ users report the same critical bug.")*

**When do we rollback vs. hotfix?**

| Severity | Definition | Response |
|---|---|---|
| 🔴 Critical | App is down or data is being corrupted | Rollback immediately; fix and redeploy within 2 hours |
| 🟠 High | Core feature broken for all users | Hotfix within 4 hours; no rollback needed if DB is safe |
| 🟡 Medium | Feature broken for some users | Fix in next 24 hours; communicate in status page |
| 🟢 Low | Minor visual bug or typo | Fix in next sprint/batch |

---

### 8.3 Quality Assurance Checklist

> **How to fill this:** Run through this list before every major release. Tick each box only when you've actually checked it — not "I think it's fine."

#### AI Quality Checks

- [ ] **Accuracy Test:** Run 20 representative user inputs through the AI — ≥ 85% must give a correct, useful output
- [ ] **Edge Case Test:** Test with empty input, very long input, non-English text, rude/offensive input
- [ ] **Prompt Injection Test:** Try inputs like "Ignore all previous instructions and..." — the AI must not comply
- [ ] **Output Format Test:** If expecting JSON, does 100% of outputs parse correctly?
- [ ] **Latency Check:** Measure AI response time — must be under 10 seconds for 95% of calls

#### App Quality Checks

- [ ] **Sign-up flow:** A new user can sign up and reach the main feature in under 2 minutes
- [ ] **Core feature:** The #1 feature works correctly end-to-end on desktop
- [ ] **Mobile:** Core feature works on iPhone Safari and Android Chrome
- [ ] **Error states:** Every form shows an error if submitted incorrectly
- [ ] **Empty states:** Every list/table has a friendly message when empty (not just a blank screen)
- [ ] **Loading states:** Every AI call shows a spinner or streaming text while waiting

#### Pre-Launch Final Check

- [ ] No `console.log` of sensitive data in production
- [ ] `robots.txt` is set up correctly (allow indexing of public pages)
- [ ] All external links open in a new tab
- [ ] Favicon is set (not the default browser icon)
- [ ] Page titles are correct for SEO
- [ ] OG image is set (for social media sharing previews)

---

### 8.4 Incident Response Plan

> *What to do when something breaks in production (after launch).*

**Step 1 — Detect:** Set up Sentry alerts. Aim to know about critical errors before users tell you.

**Step 2 — Assess:** Is this affecting 1 user or all users? Is data at risk?

**Step 3 — Communicate:** Post a simple message (e.g., in your app's status banner or on X/Twitter): *"We're aware of an issue with [feature] and are working on a fix. Updates every 30 min."*

**Step 4 — Fix or Rollback:** See rollback plan above.

**Step 5 — Post-Mortem:** Within 48 hours of fixing, write a 1-page summary:
- What broke?
- Why?
- What are we doing so it never happens again?

---

## 9. Go-to-Market & 500-Customer Plan

> **How to fill this:** This section is your marketing and growth game plan. You don't need to do all of this — pick the 2–3 channels that fit you best and go deep on those.

### 9.1 Ideal Customer Profile (ICP)

> **Who is your perfect customer?** Be as specific as possible. The more specific, the easier it is to find them and speak their language.

| Field | Answer |
|---|---|
| **Job title / Role** | *(e.g., "Freelance UX designer with 2–10 years of experience")* |
| **Company size** | *(e.g., "Self-employed or agency with 1–5 people")* |
| **Industry** | *(e.g., "Design, tech, consulting")* |
| **Location** | *(e.g., "English-speaking countries — US, UK, Canada, Australia")* |
| **Age range** | *(e.g., "25–45")* |
| **Where they hang out online** | *(e.g., "Twitter/X, LinkedIn, Dribbble, Product Hunt")* |
| **Their #1 pain point** | *(e.g., "Wasting time on admin tasks instead of design work")* |
| **How they currently solve this** | *(e.g., "Calendly + manual email — takes 20+ minutes per booking")* |

---

### 9.2 Pre-Launch (Before Phase 5)

**Goal: Build an audience before you ship.**

| Tactic | Action | Target | Status |
|---|---|---|---|
| **Waitlist** | Build a landing page with email capture | 100+ signups before launch | 🔲 |
| **Build in public** | Post weekly progress on X / LinkedIn | 50+ followers before launch | 🔲 |
| **Content teaser** | Share 1–2 screenshots or demos in communities | 10+ DMs of interest | 🔲 |
| **Early access offer** | Offer 50% off to first 20 waitlist members | 10+ commitments | 🔲 |

---

### 9.3 Launch Channels

> *Pick 2–3 channels and go ALL IN. Do not spread thin.*

| Channel | Strategy | Target (first 30 days) | Priority |
|---|---|---|---|
| **Product Hunt** | Launch as a product; engage comments all day | 100+ upvotes, 20+ signups | ⭐ High |
| **X / Twitter** | Thread about the problem + solution + demo video | 50+ signups from thread | ⭐ High |
| **Reddit** | Post in relevant subreddits (be helpful, not spammy) | 30+ signups | ⭐ High |
| **LinkedIn** | Personal post story + video demo | 20+ signups | 🔶 Medium |
| **Hacker News (Show HN)** | "Show HN: I built X for Y" post | 50+ signups if featured | 🔶 Medium |
| **YouTube / TikTok** | Demo video or "I built this with AI" video | 20+ signups per video | 🔶 Medium |
| **Cold email / DM** | Reach out to ICP directly with personal message | 5 responses per 20 sent | 🔷 Low |

---

### 9.4 Customer Milestones & Targets

| Milestone | Target Date | Metric | How We'll Get There |
|---|---|---|---|
| First 10 users | Week 1 | Alpha testers converted | Personal outreach to testers |
| First paying customer | Week 1–2 | 1 paying user | Remove free tier early or offer early access |
| 50 customers | Week 4 | 50 active/paying | Product Hunt launch |
| 100 customers | Week 6–8 | 100 active/paying | Community growth + referrals |
| 250 customers | Week 10–12 | 250 active/paying | SEO content + word of mouth |
| **500 customers** | **Week ___** | **500 active/paying** | **Growth loop + retention** |

---

### 9.5 Retention & Churn Prevention

> *Getting a customer is hard. Keeping them is what makes the business work.*

| Tactic | When to Implement | Expected Impact |
|---|---|---|
| Welcome email sequence (3–5 emails) | At launch | Reduces day-1 drop-off by 30–50% |
| In-app onboarding tips | Phase 5–6 | Improves feature activation |
| Weekly product digest email | Phase 6 | Keeps users coming back |
| User feedback loop (👍/👎 on AI) | Phase 2 | Improves AI quality → retention |
| Proactive support for churning users | Phase 6 | Save 20–30% of at-risk users |

---

### 9.6 Key Growth Metrics to Track Weekly

| Metric | Formula | Week 1 | Week 4 | Week 8 | Week 12 |
|---|---|---|---|---|---|
| Total sign-ups | Count | | | | |
| Activation rate | Users who used core feature ÷ sign-ups | | | | |
| Conversion to paid | Paid users ÷ sign-ups | | | | |
| Weekly Active Users (WAU) | Users who used app in last 7 days | | | | |
| Churn rate | Customers who cancelled ÷ total customers | | | | |
| MRR (Monthly Recurring Revenue) | Sum of active subscriptions | $0 | | | |
| AI cost per customer | Total AI spend ÷ paying customers | | | | |

---

## 10. Compliance & Privacy Checklist

> **How to fill this:** Check each box only when you've confirmed it's true — not "I think so." If you're unsure about any legal item, consult a lawyer. This section keeps your users safe and keeps you out of trouble.

### 10.1 Data Privacy

- [ ] **Privacy Policy is live** at `yourapp.com/privacy` — written in plain English, not legalese
- [ ] **Terms of Service is live** at `yourapp.com/terms`
- [ ] **We only collect data we actually use** — no unnecessary tracking
- [ ] **Users can request their data or account deletion** (required by GDPR/CCPA)
- [ ] **We don't store user PII (Personally Identifiable Information) in Claude prompts** *(full name, email, address, etc.)*
- [ ] **We don't use user data to train Claude** (Anthropic's API default: no training on API inputs)
- [ ] **Passwords are never stored in plain text** (handled by auth provider)
- [ ] **Database rows are isolated per user** (RLS or equivalent is enabled)

### 10.2 AI Ethics & Safety

- [ ] **Content moderation:** Users cannot use our product to generate harmful, illegal, or misleading content
- [ ] **Bias review:** We've tested the AI on diverse input types and it doesn't systematically fail for certain groups
- [ ] **Transparency:** Users know they're interacting with AI, not a human
- [ ] **Human override:** For high-stakes outputs (legal, medical, financial), we show a "consult a professional" disclaimer
- [ ] **Prompt injection protection:** User inputs are sanitized before being sent to Claude
- [ ] **Rate limiting:** No single user can abuse the AI at cost to others

### 10.3 Security

- [ ] HTTPS enabled on all pages
- [ ] All API keys stored in environment variables (never in code)
- [ ] Dependency vulnerabilities checked (`npm audit` or equivalent)
- [ ] No sensitive data in error messages shown to users

### 10.4 Business & Legal

- [ ] Business entity registered (LLC, LTD, or solo trader) — *if applicable*
- [ ] Anthropic usage policies reviewed and complied with: `anthropic.com/usage-policy`
- [ ] All third-party API terms of service reviewed
- [ ] Refund policy defined and communicated to users

---

## 11. Milestone Tracker

> **How to fill this:** Update this table every week. Green means on track, yellow means at risk, red means behind. This is your one-page status view.

| Phase | Phase Name | Target Date | Actual Date | Status | Blocker (if any) |
|---|---|---|---|---|---|
| Phase 0 | Discovery & Foundation | | | 🔲 Not started | |
| Phase 1 | Prototype & PoC | | | 🔲 Not started | |
| Phase 2 | MVP Build | | | 🔲 Not started | |
| Phase 3 | Alpha Testing | | | 🔲 Not started | |
| Phase 4 | Hardening & Launch Prep | | | 🔲 Not started | |
| Phase 5 | Public Launch | | | 🔲 Not started | |
| Phase 6 | Growth to 500 Customers | | | 🔲 Not started | |

**Status Key:** 🔲 Not started · 🔄 In progress · 🟢 On track · 🟡 At risk · 🔴 Behind · ✅ Complete

---

### Key Milestones

| Milestone | Target Date | Achieved Date | Notes |
|---|---|---|---|
| ✏️ Implementation Plan finalized | | | |
| 🔧 Dev environment set up | | | |
| 🤖 AI prototype working | | | |
| 🚀 MVP built (end-to-end) | | | |
| 👥 Alpha testing complete | | | |
| 🌐 Public launch | | | |
| 🥇 First paying customer | | | |
| 🎯 10 customers | | | |
| 🎯 100 customers | | | |
| 🏆 500 customers | | | |

---

## 12. Change Log

> **How to fill this:** Every time you make a significant change to this plan, add a row here. This helps you remember why decisions were made.

| Date | Version | What Changed | Why |
|---|---|---|---|
| *(Today's date)* | v1.0 | Created this document | Initial planning |
| | v1.1 | | |
| | v1.2 | | |

---

## 🎉 You Did It!

If you've filled in this document, you now have:
- ✅ A clear picture of what you're building and why
- ✅ A step-by-step plan from zero to 500 customers
- ✅ A risk plan so you're not caught off guard
- ✅ A go-to-market strategy to find your first real customers
- ✅ A compliance checklist to keep you and your users safe

**Now go build it. 🚀**

---

*This template was designed for AI-Native, solo/small-team product development using Anthropic Claude. Version 1.0 — October 2026.*
