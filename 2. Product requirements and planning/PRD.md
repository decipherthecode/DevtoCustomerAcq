# 📋 Product Requirements Document (PRD)
### AI-Driven Development · Web & Mobile · From First Line of Code to First 500 Customers

---

> **👋 How to Use This Template**
>
> This document is your single source of truth for everything about your product.
> Fill it out from top to bottom — skip nothing, even if your answer is "TBD" or "Not sure yet."
> A short honest answer beats a long guess every time.
>
> **Tip for Beginners:** Every section has a 📝 instruction block (like this one).
> Read the instruction, then replace it with your real answer. Delete the instruction block when done.
> If a question feels hard, just write what you know — you can refine it later.
>
> **AI Shortcut:** Paste any section's instruction block into Claude or ChatGPT and say:
> *"Help me fill this out for my product, which is [describe your product in 2 sentences]."*

---

## 🗂️ Document Control

<!-- ============================================================
📝 HOW TO FILL: Update this table every time you change the document.
Format: | Date | Version | What changed | Your name |
Use v0.1 for drafts, v1.0 for the first approved version.
============================================================ -->

| Date       | Version | Change Summary                         | Author       | Status    |
|------------|---------|----------------------------------------|--------------|-----------|
| YYYY-MM-DD | v0.1    | Initial draft created                  | [Your Name]  | 🟡 Draft  |
| YYYY-MM-DD | v0.2    | Added user stories and tech stack      | [Your Name]  | 🟡 Draft  |
| YYYY-MM-DD | v1.0    | Approved for development               | [Your Name]  | 🟢 Active |

**Status Legend:** 🔴 Not Started · 🟡 Draft · 🟠 Review · 🟢 Active · ⚫ Archived

---

## 🏷️ Document Metadata

<!-- ============================================================
📝 HOW TO FILL: Fill in each row. If you don't know something yet, write "TBD".
"Product Type" — is it a web app? Mobile app? Both?
"Confidentiality" — is this doc private or can anyone see it?
============================================================ -->

| Field                   | Value                                                   |
|-------------------------|---------------------------------------------------------|
| **Product Name**        | [Name of your product]                                  |
| **Tagline**             | [One sentence: what it does + who it's for]             |
| **Product Type**        | ☐ Web App  ☐ Mobile App (iOS)  ☐ Mobile App (Android)  ☐ All |
| **Version This PRD Describes** | v[X.X] — [e.g., MVP / Beta / v1.0]            |
| **PRD Owner**           | [Your name and role]                                    |
| **Primary Stakeholders**| [List names or roles of anyone who needs to approve this]|
| **Start Date**          | YYYY-MM-DD                                              |
| **Target Launch Date**  | YYYY-MM-DD                                              |
| **Confidentiality**     | ☐ Public  ☐ Internal Only  ☐ Strictly Confidential      |
| **Related Documents**   | [Links to design files, tech specs, pitch deck, etc.]   |

---

# PART 1 · PRODUCT FOUNDATION
*Why does this product exist and who is it for?*

---

## 1. Product Overview

<!-- ============================================================
📝 HOW TO FILL: Imagine you're explaining your product to a friend at a coffee shop.
What does it do? Who uses it? Why does it matter?
Write 3–5 sentences. No jargon. No buzzwords.

EXAMPLE:
"TaskFlow is a web app that helps freelance designers track their client projects,
deadlines, and invoices in one place. Right now, most freelancers juggle Notion,
spreadsheets, and email — and miss deadlines or forget to invoice clients.
TaskFlow replaces all of that with a clean, simple dashboard built just for them."
============================================================ -->

### 1.1 Elevator Pitch
> *[Write 2–3 sentences: What is it? Who uses it? What problem does it solve?]*

### 1.2 Product Vision (Long-Term)
> *[What does the world look like in 3–5 years if this product succeeds? What big change does it create?]*
> 
> **Example:** *"Every freelancer in the world manages their business without needing an accountant or a project manager — because TaskFlow handles it automatically."*

### 1.3 What This Product is NOT
> *[List 3–5 things your product deliberately does NOT do. This prevents scope creep.]*
>
> - This is not a [thing]
> - This is not meant to replace [thing]
> - We will not support [use case] in v1

---

## 2. Problem Statement

<!-- ============================================================
📝 HOW TO FILL: Describe the pain, not the solution.
Answer these three questions:
  (a) What is the painful situation people are in right now?
  (b) How do they currently try to solve it (and why does that fail)?
  (c) What does that failure cost them (time, money, stress, etc.)?

Be specific. "People waste time" is vague. "Freelancers spend 3 hours per week
chasing invoices by email" is specific and powerful.
============================================================ -->

### 2.1 The Core Problem
> *[Describe the problem in plain language. Start with "Right now, [user type] struggles with..."]*

### 2.2 Current Solutions & Why They Fail

| Current Solution     | Why It Falls Short                              | Pain Level (1–10) |
|----------------------|-------------------------------------------------|:-----------------:|
| [Solution A]         | [What's wrong with it]                          | [e.g., 8]         |
| [Solution B]         | [What's wrong with it]                          | [e.g., 6]         |
| [Solution C]         | [What's wrong with it]                          | [e.g., 7]         |

### 2.3 The Cost of the Problem
> *[What does this problem cost users — in time, money, stress, missed opportunities?]*
>
> **Example:** *"Freelancers lose an average of $2,400/year in unpaid invoices due to poor follow-up."*

### 2.4 The Opportunity
> *[Why is NOW the right time to solve this? What's changed in the market, technology, or behaviour?]*

---

## 3. Target Users & Personas

<!-- ============================================================
📝 HOW TO FILL: A "persona" is a made-up but realistic description of your ideal user.
Give them a name, a job, a frustration, and a goal.
You need at least 1 persona. 3 is ideal (primary, secondary, edge-case).

You don't need real people — just realistic ones.
Think about who you most want to help with this product.
============================================================ -->

### 3.1 Primary User Persona (Your #1 Customer)

```
Name:           [Fictional name, e.g., "Sarah the Freelancer"]
Age:            [e.g., 28–35]
Job / Role:     [e.g., Freelance UX Designer]
Location:       [e.g., Remote, US-based]
Tech Comfort:   ☐ Beginner  ☐ Intermediate  ☐ Advanced
Device Usage:   ☐ Mostly Phone  ☐ Mostly Desktop  ☐ Both

Their Day:      [2–3 sentences describing a typical work day]

Their #1 Pain:  [The biggest frustration your product solves for them]
Their Goal:     [What success looks like for them]
Their Fear:     [What they're afraid of when trying a new tool]

Quote:          "[Write a quote they might actually say about their problem]"
```

### 3.2 Secondary User Persona

```
Name:           [Fictional name]
Role:           [Job / role]
Why They Use It: [Different reason than primary persona]
Key Difference:  [What's different about how they use the product]
```

### 3.3 Who We Are NOT Building For (Anti-Persona)
> *[Describe a type of user you are explicitly NOT targeting, and why. This keeps you focused.]*
>
> **Example:** *"We are not building for enterprise companies with 500+ employees. They need custom procurement, SSO, and compliance features that would bloat our MVP."*

### 3.4 User Journey Map (Before Your Product)

```
Step 1 → [What user does first to solve their problem today]
Step 2 → [Next action — often painful or manual]
Step 3 → [Another step — often a workaround]
Step 4 → [The moment of maximum frustration]
Step 5 → [How they eventually "solve" it — even if poorly]
```

---

## 4. Market Context

<!-- ============================================================
📝 HOW TO FILL: You don't need a full market research report here.
Just answer: How big is the opportunity? Who are the competitors?
Where is the market headed? 3–5 bullet points per sub-section is enough.
============================================================ -->

### 4.1 Market Size Estimate

| Metric | Estimate | Source / Notes |
|--------|----------|----------------|
| Total Addressable Market (TAM) | $[X]B | [How you estimated this] |
| Serviceable Addressable Market (SAM) | $[X]M | [Your realistic slice] |
| Serviceable Obtainable Market (SOM) | $[X]M | [What you can realistically win in Year 1] |

### 4.2 Competitive Landscape

| Competitor | Their Strength | Their Weakness | Our Advantage |
|------------|---------------|----------------|---------------|
| [Name]     | [e.g., Brand recognition] | [e.g., Too complex] | [e.g., 10x simpler] |
| [Name]     | [Strength]    | [Weakness]     | [Advantage]   |
| [Name]     | [Strength]    | [Weakness]     | [Advantage]   |

### 4.3 Our Unique Value Proposition (UVP)
> *[One powerful sentence: "Unlike [competitor], we [do X] so that [user] can [get result] without [pain]."]*
>
> **Example:** *"Unlike Asana, we auto-generate invoices from completed tasks — so freelancers get paid without doing admin work."*

### 4.4 Market Trends Supporting This Product
> - *[Trend 1 — e.g., "Remote work grew 300% since 2020, creating 59M freelancers in the US alone"]*
> - *[Trend 2]*
> - *[Trend 3]*

---

## 5. Assumptions, Risks & Constraints

<!-- ============================================================
📝 HOW TO FILL: What are you assuming is true that hasn't been proven yet?
What could go wrong? What are you NOT allowed to do (budget, time, regulations)?
Being honest here saves you months of wasted work.
============================================================ -->

### 5.1 Key Assumptions

| # | Assumption | Risk if Wrong | How to Validate |
|---|------------|---------------|-----------------|
| 1 | [e.g., Users will pay $29/month for this] | Low revenue | Run a pricing survey |
| 2 | [Assumption] | [Risk] | [Validation method] |
| 3 | [Assumption] | [Risk] | [Validation method] |

### 5.2 Known Risks

| Risk | Likelihood | Impact | Mitigation Plan |
|------|:----------:|:------:|-----------------|
| [e.g., Key competitor copies us] | Medium | High | Move fast, build moat with data |
| [Risk] | Low/Med/High | Low/Med/High | [Plan] |

### 5.3 Constraints

```
Budget:         $[Amount] total / $[Amount] per month
Timeline:       Must launch by [Date] — reason: [Why this date matters]
Team Size:      [Number] people (including AI tools as force multipliers)
Regulatory:     [Any laws or platform rules you must follow — e.g., App Store guidelines]
Technical:      [Any hard technical limits — e.g., "must run on free-tier cloud services"]
```

---

# PART 2 · PRODUCT DESIGN
*What are we building, exactly?*

---

## 6. Goals & Success Metrics

<!-- ============================================================
📝 HOW TO FILL: Goals are the big outcomes you want.
Metrics are the specific numbers that tell you if you got there.

OKR format: "We will [Objective] measured by [Key Result]"
KPI: A number you track every week/month

Set goals for: 30 days after launch, 90 days, and 6 months.
============================================================ -->

### 6.1 Product Goals (OKRs)

#### 🎯 Objective 1: [Your first big goal]
| Key Result | Target | Measurement Method |
|------------|--------|-------------------|
| KR1: [e.g., 100 signups in first 30 days] | 100 | [e.g., Posthog / Analytics dashboard] |
| KR2: [e.g., 40% of signups complete onboarding] | 40% | [Funnel tracking] |
| KR3: [e.g., NPS score ≥ 50] | ≥ 50 | [In-app NPS survey] |

#### 🎯 Objective 2: [Your second goal]
| Key Result | Target | Measurement Method |
|------------|--------|-------------------|
| KR1: | | |
| KR2: | | |

### 6.2 North Star Metric
> *[The ONE number that, if it goes up, means everything is working. Examples: DAU, MRR, tasks completed, invoices sent.]*
>
> **Our North Star Metric:** `[Metric name]` — measured weekly via `[tool]`

### 6.3 KPI Dashboard (Track Weekly)

| KPI | Week 1 Goal | Month 1 Goal | Month 3 Goal | Current |
|-----|:-----------:|:------------:|:------------:|:-------:|
| Signups | | | | — |
| Active Users (DAU/WAU) | | | | — |
| Activation Rate | | | | — |
| Retention (Day 7) | | | | — |
| MRR | | | | — |
| Churn Rate | | | | — |
| NPS Score | | | | — |

### 6.4 Definition of Done (for This Version)
> *[List 3–5 bullet points that describe when this version is "complete" and ready to ship.]*
> - ✅ [e.g., Core feature works end-to-end without errors]
> - ✅ [e.g., At least 5 beta users have used it and given positive feedback]
> - ✅ [e.g., Page load time < 2 seconds]

---

## 7. User Stories & Use Cases

<!-- ============================================================
📝 HOW TO FILL: A "user story" describes what a user wants to do and why.
Format: "As a [persona], I want to [do something] so that I can [get a result]."

Write one story per feature. Start with the most important ones.
Then write the "acceptance criteria" — the rules that prove the story is done.
============================================================ -->

### 7.1 Epic Map (Feature Groups)

```
Epic 1: [e.g., Onboarding]
  └── Story 1.1: Sign up with email
  └── Story 1.2: Complete profile setup
  └── Story 1.3: Create first project

Epic 2: [e.g., Core Feature]
  └── Story 2.1: [Feature]
  └── Story 2.2: [Feature]

Epic 3: [e.g., Billing & Payments]
  └── Story 3.1: [Feature]
  └── Story 3.2: [Feature]
```

### 7.2 User Stories (Detailed)

---

**Story ID:** US-001  
**Epic:** [e.g., Onboarding]  
**Priority:** 🔴 Must Have (MVP)

> **As a** [persona name],  
> **I want to** [action],  
> **So that** [the outcome/benefit].

**Acceptance Criteria:**
- [ ] Given [context], when [action], then [expected result]
- [ ] Given [context], when [action], then [expected result]
- [ ] Edge case: [What happens when something goes wrong?]

**AI Prompt (for building this story):**
```
[Optional: Write the exact prompt you'll give Claude/ChatGPT to build this feature]
```

---

**Story ID:** US-002  
**Epic:** [Epic name]  
**Priority:** 🟠 Should Have

> **As a** [persona name],  
> **I want to** [action],  
> **So that** [benefit].

**Acceptance Criteria:**
- [ ] [Criterion 1]
- [ ] [Criterion 2]

---

*[Copy the story block above for each feature. Use this priority scale:]*
> 🔴 **Must Have (MVP)** — Can't launch without it  
> 🟠 **Should Have** — Important but not launch-blocking  
> 🟡 **Nice to Have** — Do after launch if time allows  
> ⚫ **Won't Have (v1)** — Explicitly out of scope

---

## 8. Feature Specifications

<!-- ============================================================
📝 HOW TO FILL: For each major feature, describe:
- What it is (plain English)
- How it works (step by step)
- What it looks like (or link to a design)
- What happens when things go wrong (error states)

Think of this section as instructions for a new hire on Day 1.
They should be able to build this feature from your description alone.
============================================================ -->

### 8.1 Feature List & Status

| Feature | Priority | Status | Assigned To | Sprint |
|---------|:--------:|--------|-------------|:------:|
| [Feature name] | 🔴 MVP | 🔴 Not Started | [Name / AI] | Sprint 1 |
| [Feature name] | 🟠 Should | 🟡 In Progress | [Name / AI] | Sprint 2 |
| [Feature name] | 🟡 Nice | ⚫ Backlog | — | TBD |

### 8.2 Feature Deep-Dive

---

#### Feature: [Feature Name]

**What it is:**
> *[1–2 sentences. What does this feature do? Explain it like the user is 10 years old.]*

**How it works (step by step):**
1. User does [action]
2. System responds with [behavior]
3. User sees [result]
4. If error: [what happens]

**Inputs:**
- [What data the user provides or the system receives]

**Outputs:**
- [What the user sees, gets, or can do after this feature runs]

**Business Rules:**
- [Any logic, limits, or conditions — e.g., "max 5 projects on free plan"]
- [Rule 2]

**Error States & Edge Cases:**
| Scenario | What Happens | Message Shown to User |
|----------|-------------|----------------------|
| [e.g., Network fails] | [e.g., Show retry button] | "Something went wrong. Try again." |
| [Edge case] | [Behavior] | [User-facing message] |

**Design Reference:**
> [Link to Figma / screenshot / sketch — or describe the layout in words]

**AI Build Prompt:**
```
[The exact prompt you'll paste into Claude/ChatGPT to build this feature.
Be specific: include the tech stack, the inputs, the outputs, and any rules.]
```

---

*[Repeat the Feature Deep-Dive block for each major feature.]*

---

## 9. User Experience (UX) & Design

<!-- ============================================================
📝 HOW TO FILL: Describe how the product looks and feels.
You don't need design skills — just describe it in words.
Link to Figma or wireframes if you have them.
If you don't, write a rough description and use AI to generate them.
============================================================ -->

### 9.1 Design Principles

> *[3–5 words or phrases that describe how your product should feel. Examples below:]*
> - **Simple over Powerful** — One action per screen; no feature soup
> - **Mobile-first** — Looks great on a phone before a desktop
> - **[Your principle]** — [Why it matters]

### 9.2 Design System

| Element | Decision | Notes |
|---------|----------|-------|
| Primary Color | `#[hex]` | [e.g., Trustworthy blue] |
| Secondary Color | `#[hex]` | |
| Font (Headings) | [e.g., Inter Bold] | |
| Font (Body) | [e.g., Inter Regular] | |
| Border Radius | [e.g., 8px — rounded, friendly] | |
| Icon Set | [e.g., Lucide Icons] | |
| Component Library | [e.g., shadcn/ui, Tailwind UI] | |

### 9.3 Screen Inventory

| Screen Name | Description | Priority | Design Link |
|-------------|-------------|:--------:|------------|
| Landing Page | First thing visitors see | 🔴 MVP | [Link] |
| Sign Up / Login | Create account or log in | 🔴 MVP | [Link] |
| Onboarding Flow | Steps 1–3 after signup | 🔴 MVP | [Link] |
| Dashboard / Home | Main screen after login | 🔴 MVP | [Link] |
| [Feature Screen] | [Description] | [Priority] | [Link] |
| Settings | Account, billing, notifications | 🟠 Should | [Link] |
| 404 / Error Page | When something breaks | 🟠 Should | [Link] |

### 9.4 Accessibility Requirements
> - Minimum contrast ratio: **4.5:1** (WCAG AA)
> - All interactive elements keyboard-navigable
> - Screen reader labels on all icons and images
> - ☐ Target platforms for accessibility testing: [iOS VoiceOver / Android TalkBack / NVDA]

---

## 10. Information Architecture & Navigation

<!-- ============================================================
📝 HOW TO FILL: Draw (in text) how screens are connected.
Think of it like a map of your app — where does the user go from where?
============================================================ -->

```
[App Entry]
├── Landing Page
│   ├── → Sign Up → Onboarding → Dashboard
│   └── → Log In → Dashboard
│
├── Dashboard (Main Hub)
│   ├── → [Feature A Screen]
│   ├── → [Feature B Screen]
│   └── → Settings
│       ├── → Profile
│       ├── → Billing / Upgrade
│       └── → Notifications
│
└── [Other top-level flow]
    └── [Sub-screens]
```

---

# PART 3 · AI ARCHITECTURE
*How does the AI in your product work?*

---

## 11. AI Agent Design & Prompt Architecture

<!-- ============================================================
📝 HOW TO FILL: This section is for products that use AI (LLMs, ML, automation).
If your product has NO AI features, write "N/A — No AI components" and skip to Part 4.

For each AI feature, fill out one "AI Component" block below.
Think of each AI component like an employee with a specific job description.
============================================================ -->

### 11.1 AI Component Inventory

| Component ID | Name | Purpose | Model | Trigger |
|:------------:|------|---------|-------|---------|
| AI-001 | [e.g., Invoice Generator] | [Auto-drafts invoices from tasks] | [e.g., Claude 3.5 Sonnet] | [User clicks "Generate Invoice"] |
| AI-002 | [Component name] | [Purpose] | [Model] | [What triggers it] |

---

### 11.2 AI Component Deep-Dive

#### Component: AI-001 — [Component Name]

**What it does (plain English):**
> *[Describe this AI feature as if explaining to someone who has never used AI.
> Example: "This AI reads your completed task list and writes a professional invoice for you automatically."]*

**Model Selection:**

| Setting | Choice | Reason |
|---------|--------|--------|
| Provider | ☐ Anthropic (Claude)  ☐ OpenAI (GPT)  ☐ Google (Gemini)  ☐ Other: ___ | |
| Model | [e.g., claude-3-5-sonnet-20241022] | [e.g., Best balance of speed and quality] |
| Temperature | [0.0–1.0, e.g., 0.3] | [Low = consistent; High = creative] |
| Max Tokens | [e.g., 2048] | [Output length limit] |
| Context Window Used | [e.g., 8k of 200k] | |

**System Prompt:**
```
[ROLE]
You are [describe the AI's role and personality].

[CONTEXT]
You are given: [describe what input data the AI receives]

[TASK]
Your job is to: [describe exactly what the AI must do]

[OUTPUT FORMAT]
Always respond in: [e.g., JSON / Markdown / plain text]
Output structure:
{
  "field1": "...",
  "field2": "..."
}

[RULES & CONSTRAINTS]
- Always [rule]
- Never [rule]
- If you don't know something, say: "[Specific fallback phrase]"

[EXAMPLES]
Input: [example input]
Output: [example output]
```

**User Prompt Template:**
```
[The dynamic part of the prompt that changes per user request.
Use {{variables}} for things that get filled in at runtime.]

Example:
"Generate an invoice for the following completed tasks: {{task_list}}
Client name: {{client_name}}
Hourly rate: ${{rate}}/hr"
```

**Input Data:**
| Field | Type | Required | Where It Comes From |
|-------|------|:--------:|---------------------|
| [e.g., task_list] | Array of strings | ✅ Yes | User's task database |
| [e.g., client_name] | String | ✅ Yes | User's client record |
| [Field] | [Type] | ☐ Optional | [Source] |

**Output Data:**
| Field | Type | Used For |
|-------|------|---------|
| [e.g., invoice_text] | String (Markdown) | Displayed in invoice preview |
| [Field] | [Type] | [Use] |

**Tool Calls / Function Calling:**
```json
{
  "tools": [
    {
      "name": "[tool_name]",
      "description": "[What this tool does]",
      "parameters": {
        "[param1]": "[description]",
        "[param2]": "[description]"
      }
    }
  ]
}
```
> *[If no tool calls needed, write "None — single-shot completion only"]*

**Guardrails & Safety:**
| Risk | Guardrail Applied |
|------|------------------|
| Hallucinated invoice amounts | Amounts pulled only from database, not generated |
| PII in logs | Strip all user data before logging AI calls |
| [Risk] | [Guardrail] |

**Evaluation Criteria (How to know if the AI is working well):**
- [ ] Output passes format validation (e.g., valid JSON)
- [ ] Human review: output is accurate > [X]% of the time
- [ ] Latency: response in < [X] seconds
- [ ] [Other success criterion]

**Fallback Behavior (when AI fails or is unavailable):**
> *[What does the product do if the AI call fails? Example: "Show a pre-built template the user can edit manually."]*

---

*[Repeat the AI Component block for each AI feature.]*

---

# PART 4 · TECHNICAL SPECIFICATION
*How is this product built?*

---

## 12. Tech Stack

<!-- ============================================================
📝 HOW TO FILL: List every technology you're using or planning to use.
If you're not sure yet, write "TBD" — but try to decide early.
Your tech stack affects everything: cost, speed, who can help you.
============================================================ -->

### 12.1 Stack Overview

| Layer | Technology | Why This Choice |
|-------|-----------|----------------|
| **Frontend (Web)** | [e.g., Next.js 14 / React] | [Reason] |
| **Frontend (Mobile)** | [e.g., React Native / Flutter / None] | [Reason] |
| **UI Components** | [e.g., shadcn/ui + Tailwind CSS] | [Reason] |
| **Backend / API** | [e.g., Next.js API Routes / FastAPI / Supabase] | [Reason] |
| **Database** | [e.g., PostgreSQL via Supabase] | [Reason] |
| **Authentication** | [e.g., Clerk / Supabase Auth / NextAuth] | [Reason] |
| **AI Provider** | [e.g., Anthropic Claude API] | [Reason] |
| **File Storage** | [e.g., Supabase Storage / S3 / Cloudflare R2] | [Reason] |
| **Email** | [e.g., Resend / SendGrid] | [Reason] |
| **Payments** | [e.g., Stripe] | [Reason] |
| **Analytics** | [e.g., PostHog / Mixpanel / Plausible] | [Reason] |
| **Error Tracking** | [e.g., Sentry] | [Reason] |
| **Hosting / Deployment** | [e.g., Vercel / Railway / Fly.io] | [Reason] |
| **CI/CD** | [e.g., GitHub Actions] | [Reason] |
| **Version Control** | [e.g., GitHub] | [Reason] |

### 12.2 Architecture Diagram

```
[User Browser / Mobile App]
        ↓ HTTPS
[Frontend: Next.js on Vercel]
        ↓ API calls
[Backend API: Next.js API Routes]
    ↙           ↘         ↘
[Database]   [AI Provider] [Storage]
[Supabase]   [Claude API]  [S3/R2]
    ↓
[Authentication: Clerk]

External services:
  → [Stripe] for payments
  → [Resend] for email
  → [PostHog] for analytics
```

### 12.3 Environments

| Environment | URL | Purpose | Who Has Access |
|-------------|-----|---------|----------------|
| Development | localhost:3000 | Local coding | Developer only |
| Staging | staging.[yourdomain].com | Testing before launch | Team + beta users |
| Production | [yourdomain].com | Live product | Everyone |

---

## 13. Data Model & Schema

<!-- ============================================================
📝 HOW TO FILL: Describe the main "things" your app stores in the database.
Each "table" is a type of thing (users, projects, invoices, etc.).
List the important fields for each one.
============================================================ -->

### 13.1 Core Entities

```
users
  ├── id (UUID, primary key)
  ├── email (string, unique)
  ├── full_name (string)
  ├── plan (enum: free | pro | enterprise)
  ├── created_at (timestamp)
  └── [other fields]

[entity_2]
  ├── id (UUID, primary key)
  ├── user_id (foreign key → users.id)
  ├── [field]
  ├── [field]
  └── created_at (timestamp)

[entity_3]
  ├── [fields]
```

### 13.2 Relationships
> *[Describe how entities relate to each other. Example: "One user can have many projects. One project can have many tasks."]*

---

## 14. API Design

<!-- ============================================================
📝 HOW TO FILL: List the main API endpoints your backend will have.
Format: METHOD /path — what it does
============================================================ -->

### 14.1 Core Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|:-------------:|
| POST | /api/auth/signup | Create new account | ❌ No |
| POST | /api/auth/login | Log in | ❌ No |
| GET | /api/[resource] | List user's [resources] | ✅ Yes |
| POST | /api/[resource] | Create a [resource] | ✅ Yes |
| PUT | /api/[resource]/:id | Update a [resource] | ✅ Yes |
| DELETE | /api/[resource]/:id | Delete a [resource] | ✅ Yes |
| POST | /api/ai/[feature] | Trigger AI feature | ✅ Yes |

### 14.2 API Standards
- Auth method: `[e.g., Bearer token in Authorization header]`
- Rate limiting: `[e.g., 100 requests/minute per user]`
- Response format: `JSON`
- Error format: `{ "error": "message", "code": "ERROR_CODE" }`
- API versioning: `[e.g., /api/v1/...]`

---

## 15. Integrations & Third-Party Services

| Service | Purpose | Plan/Cost | Integration Method |
|---------|---------|:---------:|--------------------|
| [Stripe] | Payments | $0 + % | Stripe SDK + webhooks |
| [Resend] | Transactional email | Free tier | REST API |
| [PostHog] | Analytics | Free tier | JS snippet |
| [Service] | [Purpose] | [Cost] | [Method] |

---

## 16. Security & Performance Requirements

### 16.1 Security Checklist
- [ ] All passwords hashed with bcrypt / Argon2
- [ ] HTTPS enforced on all environments
- [ ] Input sanitization on all user inputs
- [ ] SQL injection prevention (parameterized queries)
- [ ] Rate limiting on auth endpoints
- [ ] AI prompt injection prevention (user input never injected directly into system prompt)
- [ ] API keys stored in environment variables (never in code)
- [ ] CORS configured correctly
- [ ] [Platform-specific: App Store data security guidelines met]

### 16.2 Performance Targets

| Metric | Target | Measurement Tool |
|--------|--------|-----------------|
| Page Load Time (LCP) | < 2.5s | Lighthouse / Vercel Analytics |
| API Response Time | < 500ms (p95) | Sentry / Datadog |
| AI Response Time | < 5s | Custom logging |
| Uptime | > 99.5% | UptimeRobot |
| Mobile App Launch Time | < 2s | [Tool] |

---

# PART 5 · DEVELOPMENT PLAN
*When and how are we building this?*

---

## 17. Milestone Structure

<!-- ============================================================
📝 HOW TO FILL: Choose ONE milestone style, or use a mix.
Delete the sections you don't need.
Fill in your specific dates and deliverables.
============================================================ -->

### Option A: Phase-Gate Model (Recommended for First-Time Builders)

```
PHASE 0 — DISCOVERY (Week 1–2)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Goal:    Validate the problem before writing a single line of code
Activities:
  • 5–10 user interviews with target persona
  • Competitive analysis
  • Define North Star Metric
  • Finalize tech stack
Exit Criteria (must be true before moving to Phase 1):
  ☐ At least 5 users confirmed they have this problem
  ☐ At least 3 users said they'd pay for a solution
  ☐ PRD v1.0 approved
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PHASE 1 — MVP BUILD (Week 3–8)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Goal:    Build the smallest version that delivers the core value
Features: [List only MUST HAVE features from Section 8.1]
AI Tools: Use Claude/ChatGPT for all feature coding
Exit Criteria:
  ☐ Core user journey works end-to-end
  ☐ No critical bugs (crash, data loss, broken auth)
  ☐ Deployed to staging environment
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PHASE 2 — PRIVATE BETA (Week 9–12)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Goal:    Get 10–50 real users and gather feedback
Activities:
  • Invite waitlist / friends / communities
  • Weekly feedback calls
  • Bug fix sprints
  • Instrument analytics
Exit Criteria:
  ☐ 10+ active beta users
  ☐ Activation rate > 50%
  ☐ No P0/P1 bugs open
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PHASE 3 — PUBLIC LAUNCH (Week 13–14)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Goal:    Open to the public and acquire first paying customers
Activities:
  • Product Hunt launch
  • Social media announcement
  • Enable Stripe billing
  • Set up support channel
Exit Criteria:
  ☐ Product live on production
  ☐ First 10 paying customers
  ☐ Support response time < 24h
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PHASE 4 — GROWTH (Month 4–6)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Goal:    Scale to 500 customers
Activities:
  • Run AARRR funnel analysis (see Part 9)
  • Optimize conversion and activation
  • Add top-requested features
  • Build referral program
Exit Criteria:
  ☐ 500 total customers
  ☐ MRR growing > 10% week-over-week
  ☐ Churn < [X]%
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Option B: Sprint-Based (2-Week Sprints)

| Sprint | Dates | Goal | Key Deliverables |
|--------|-------|------|-----------------|
| Sprint 0 | [Start] → [End] | Setup & foundations | Repo, CI/CD, auth, database |
| Sprint 1 | [Start] → [End] | [Core feature] | [Deliverables] |
| Sprint 2 | [Start] → [End] | [Core feature] | [Deliverables] |
| Sprint 3 | [Start] → [End] | [Feature + fixes] | [Deliverables] |
| Launch | [Date] | Ship it! | Production deployment |

### Option C: OKR-Based (Ship When the Metric Moves)

| Outcome Target | Metric | Current | Target | Timeline |
|---------------|--------|:-------:|:------:|----------|
| [e.g., Users love the core feature] | Day-7 retention | 0% | 40% | Before adding new features |
| [e.g., Product is monetizing] | Paying customers | 0 | 10 | Before scaling marketing |
| [Outcome] | [Metric] | — | [Target] | [When] |

---

## 18. AI-Assisted Development Workflow

<!-- ============================================================
📝 HOW TO FILL: Describe how you'll use AI (Claude, ChatGPT) to build the product.
This is your personal coding process, powered by AI.
============================================================ -->

### 18.1 AI Development Process (Per Feature)

```
Step 1 — WRITE THE SPEC
  └── Fill out the Feature Deep-Dive in Section 8.2
  └── Write the "AI Build Prompt" at the bottom of each feature

Step 2 — GENERATE WITH AI
  └── Paste the AI Build Prompt into Claude/ChatGPT
  └── Review the output before pasting into your codebase
  └── Ask AI to explain anything you don't understand

Step 3 — TEST IMMEDIATELY
  └── Run the code as soon as it's added
  └── Check against Acceptance Criteria in the user story
  └── Ask AI to fix bugs: "This is the error I got: [paste error]. Fix it."

Step 4 — COMMIT TO GIT
  └── Commit working code with a clear message: "feat: add [feature name]"
  └── Never commit broken code to main branch

Step 5 — REPEAT
  └── Move to next feature on the list
```

### 18.2 Standard AI Prompt Patterns (Save These!)

**Pattern 1 — Build a new feature:**
```
Tech stack: [your stack]
I need to build: [feature description]
The input is: [what data goes in]
The output should be: [what the user sees]
Business rules: [any constraints]
Please write the complete code for this, including the frontend component, 
backend API route, and any database queries needed.
```

**Pattern 2 — Fix a bug:**
```
I'm getting this error: [paste full error message]
Here is the relevant code: [paste code]
What's causing it and how do I fix it?
```

**Pattern 3 — Improve existing code:**
```
Here is my current code for [feature]: [paste code]
Please improve it to: [what you want improved — e.g., better performance, 
add error handling, make it work on mobile]
```

**Pattern 4 — Write test cases:**
```
Here is the function I need to test: [paste function]
Write comprehensive test cases for this, covering:
- Happy path (normal use)
- Edge cases (unusual inputs)
- Error cases (what can go wrong)
Use [your test framework, e.g., Jest / Vitest / Pytest].
```

---

# PART 6 · QUALITY ASSURANCE
*How do we make sure it actually works?*

---

## 19. Acceptance Criteria Master List

<!-- ============================================================
📝 HOW TO FILL: List every feature and its acceptance criteria here.
A feature is DONE only when ALL its criteria are checked off.
Never ship a feature with unchecked criteria.
============================================================ -->

### Feature Acceptance Checklist

| Feature | Criteria Met | Tested By | Date |
|---------|:------------:|-----------|------|
| [Feature name] | ☐ All ☐ Partial | [Name / AI] | |
| [Feature name] | ☐ All ☐ Partial | [Name / AI] | |

---

## 20. AI-Generated Test Suite

<!-- ============================================================
📝 HOW TO FILL: Use Claude/ChatGPT to generate test cases for each feature.
Use the prompt pattern in Section 18.2 (Pattern 4).
Paste the generated tests here for reference.
============================================================ -->

### 20.1 Test Coverage Targets

| Test Type | Coverage Target | Tool |
|-----------|:--------------:|------|
| Unit Tests (functions) | > 70% | [e.g., Jest / Vitest] |
| Integration Tests (API) | > 50% | [e.g., Supertest] |
| End-to-End Tests (UI flows) | Core journeys | [e.g., Playwright / Cypress] |
| AI Output Tests | Manual spot check | Human review |

### 20.2 Test Plan (Per Feature)

---

**Feature:** [Feature Name]  
**AI Prompt Used to Generate Tests:**
```
[Paste the exact prompt you gave Claude/ChatGPT to generate these tests]
```

**Generated Test Cases:**
```javascript
// Paste AI-generated tests here
// Example:
describe('[Feature Name]', () => {
  test('should [expected behavior] when [condition]', () => {
    // ...
  });
});
```

**Manual Test Cases (Human-Verified):**
| Test Case | Steps | Expected Result | Pass/Fail |
|-----------|-------|-----------------|:---------:|
| [Test name] | 1. [Step] 2. [Step] | [What should happen] | ☐ |
| [Test name] | 1. [Step] | [Expected] | ☐ |

---

## 21. User Acceptance Testing (UAT)

<!-- ============================================================
📝 HOW TO FILL: Before public launch, get 5–10 real people to test your product.
Give them tasks to complete (not instructions!). Watch what they do.
Write down what confused them or broke.
============================================================ -->

### 21.1 UAT Plan

| Tester Type | # of Testers | Recruitment Method | Testing Period |
|-------------|:------------:|-------------------|----------------|
| Target persona (primary) | 5 | [e.g., Personal network, Twitter DM] | [Dates] |
| Target persona (secondary) | 3 | [e.g., Community slack] | [Dates] |
| Non-technical user | 2 | [e.g., Family / friends] | [Dates] |

### 21.2 UAT Task Script

> *[Give testers these tasks without helping them. Observe what they do.]*

**Task 1:** "Without me helping you, please try to [core action the user would do]."  
**Task 2:** "Now try to [second important action]."  
**Task 3:** "Find [specific thing] and do [action]."

**What to observe:**
- Where do they hesitate or get confused?
- What do they click that isn't clickable?
- What do they say out loud ("I expected...", "That's weird...")?

### 21.3 UAT Feedback Log

| Tester | Task | Issue Found | Severity | Fixed? |
|--------|------|-------------|:--------:|:------:|
| [Name] | [Task] | [What went wrong] | P0/P1/P2 | ☐ |

**Bug Severity:**
> - **P0 (Blocker)** — Cannot launch without fixing. App crashes, data lost, auth broken.  
> - **P1 (Critical)** — Core feature broken. Must fix before launch.  
> - **P2 (Major)** — Important but has a workaround. Fix in first patch.  
> - **P3 (Minor)** — Small issue. Fix when time allows.

---

# PART 7 · LEGAL, COMPLIANCE & PRIVACY
*Protecting your users and your business*

---

## 22. Data Privacy & Compliance

<!-- ============================================================
📝 HOW TO FILL: This section protects you legally and builds user trust.
Check off what applies to your product.
If you sell to EU users → GDPR applies.
If you sell to California users → CCPA applies.
When in doubt, follow both — it's better to be safe.
============================================================ -->

### 22.1 Data Inventory

| Data Collected | Why Collected | Stored Where | Retention Period | Shared With |
|----------------|--------------|--------------|:----------------:|-------------|
| Email address | Auth + communication | Supabase | Until account deleted | Email provider |
| [Data type] | [Purpose] | [Location] | [Period] | [Third parties] |
| AI conversation logs | Product improvement | [Location] | [Period] | [AI provider] |

### 22.2 GDPR Compliance Checklist (EU Users)
- [ ] Privacy policy published and accessible before signup
- [ ] Cookie consent banner implemented (non-essential cookies require opt-in)
- [ ] Users can request data export (Right to Portability)
- [ ] Users can request account deletion (Right to be Forgotten)
- [ ] Data breach notification process documented (72-hour rule)
- [ ] Data Processing Agreement (DPA) signed with all third-party processors
- [ ] Legal basis for processing documented for each data type
- [ ] If using AI: users informed that AI processes their data

### 22.3 CCPA Compliance Checklist (California Users)
- [ ] "Do Not Sell My Personal Information" option available
- [ ] Privacy policy includes California-specific disclosures
- [ ] Users can request what data you hold about them
- [ ] Users can opt out of data sale/sharing

### 22.4 AI Ethics & Responsible AI

| Risk | Status | Mitigation |
|------|:------:|-----------|
| AI generates harmful/biased content | ☐ Addressed | [e.g., Content filters, output validation] |
| User data used to train AI without consent | ☐ Addressed | [e.g., Opt-in only, clear disclosure] |
| AI decisions affect users without transparency | ☐ Addressed | [e.g., Always show AI attribution] |
| AI hallucinations presented as facts | ☐ Addressed | [e.g., Confidence scores, source links] |
| AI used for surveillance or profiling | N/A | Not applicable |

**AI Transparency Statement:**  
> *[Write 2–3 sentences explaining to users how AI is used in your product, what data is shared with AI providers, and how they can opt out. This goes in your Privacy Policy.]*

### 22.5 Legal Documents Checklist

| Document | Status | Link |
|----------|:------:|------|
| Privacy Policy | ☐ Draft ☐ Legal Review ☐ Published | [Link] |
| Terms of Service | ☐ Draft ☐ Legal Review ☐ Published | [Link] |
| Cookie Policy | ☐ Draft ☐ Published | [Link] |
| AI Usage Disclosure | ☐ Draft ☐ Published | [Link] |
| DPA (for EU B2B) | ☐ N/A ☐ Draft ☐ Signed | [Link] |

> 💡 **Tip:** Use Termly, Iubenda, or TermsFeed to generate policy templates. Have a lawyer review before launch if you're handling payments or sensitive data.

---

# PART 8 · LAUNCH & GO-TO-MARKET
*Getting the product into the world*

---

## 23. Pre-Launch Checklist

<!-- ============================================================
📝 HOW TO FILL: Go through this list the week before you launch.
Do not launch until everything critical (🔴) is checked off.
============================================================ -->

### 🔴 MUST COMPLETE BEFORE LAUNCH

**Product:**
- [ ] All MVP features working (tested against acceptance criteria)
- [ ] No P0 or P1 bugs open
- [ ] Production environment deployed and stable
- [ ] Custom domain configured and SSL active
- [ ] Error monitoring live (Sentry or equivalent)
- [ ] Analytics tracking live and verified (PostHog / Mixpanel)
- [ ] AI rate limits and cost caps configured

**Business:**
- [ ] Stripe payments tested in production
- [ ] Pricing page live and accurate
- [ ] Support email / channel set up (respond within 24h)
- [ ] Privacy Policy and Terms of Service published
- [ ] Feedback collection mechanism in place (e.g., Typeform, Canny)

**Marketing:**
- [ ] Landing page live with clear value proposition
- [ ] Signup / waitlist form working
- [ ] Welcome email sequence set up (at least Day 0 and Day 3)
- [ ] Social profiles created and consistent
- [ ] Launch announcement drafted and reviewed

### 🟠 COMPLETE WITHIN FIRST WEEK

- [ ] Onboarding email sequence complete (Day 0, 3, 7, 14)
- [ ] User documentation / help center basic articles live
- [ ] First 5 beta testers invited and onboarded
- [ ] Weekly metrics review process started

---

## 24. Go-To-Market Strategy

<!-- ============================================================
📝 HOW TO FILL: How will people find your product?
Pick 1–2 primary channels for launch. Going wide too early = spreading thin.
Answer: Where do your personas hang out online?
============================================================ -->

### 24.1 Launch Channels

| Channel | Strategy | Target Reach | Owner | Launch Date |
|---------|----------|:------------:|-------|-------------|
| [e.g., Product Hunt] | [e.g., Full PH launch with hunter] | [e.g., 1,000 visitors] | [Name] | [Date] |
| [e.g., Twitter/X] | [e.g., Build-in-public thread] | [e.g., 500 impressions] | [Name] | [Date] |
| [Channel] | [Strategy] | [Target] | [Owner] | [Date] |

### 24.2 Content & Marketing Plan (First 90 Days)

| Week | Activity | Channel | Goal |
|------|----------|---------|------|
| Week 1 | [e.g., Product Hunt launch] | PH + Twitter | [e.g., 200 signups] |
| Week 2 | [e.g., Post in 5 relevant communities] | Reddit, Discord | [e.g., 100 signups] |
| Week 3–4 | [e.g., Demo video published] | YouTube + LinkedIn | [e.g., 50 trials] |
| Month 2 | [e.g., SEO content — 4 articles] | Blog | [e.g., Organic traffic] |
| Month 3 | [e.g., Referral program launch] | In-app | [e.g., 20% referral signups] |

### 24.3 Pricing & Packaging

| Plan Name | Price | What's Included | Target Persona |
|-----------|:-----:|-----------------|---------------|
| Free | $0/mo | [Features] | [Who this is for] |
| [Plan name] | $[X]/mo | [Features] | [Who this is for] |
| [Plan name] | $[X]/mo | [Features] | [Who this is for] |

**Pricing Rationale:**
> *[Why did you choose these prices? What research supports them? Competitor prices? Willingness-to-pay surveys?]*

### 24.4 Distribution Channels

| Channel | Status | Notes |
|---------|:------:|-------|
| ☐ Direct (website) | Active / Planned | |
| ☐ App Store (iOS) | Active / Planned | [App Store category: ] |
| ☐ Google Play | Active / Planned | |
| ☐ Browser Extension | Active / Planned | |
| ☐ API / Marketplace | Active / Planned | |
| ☐ Partner integrations | Active / Planned | [Partners: ] |

---

# PART 9 · FIRST 500 CUSTOMERS (AARRR FUNNEL)
*From stranger to loyal customer — the full journey*

---

> **What is AARRR?**  
> AARRR (called "Pirate Metrics") is a framework for tracking how users move from
> discovering your product to becoming loyal, paying fans who refer others.
>
> **A** — Acquisition: How do strangers find you?  
> **A** — Activation: Do they have a great first experience?  
> **R** — Retention: Do they come back?  
> **R** — Referral: Do they tell their friends?  
> **R** — Revenue: Do they pay you?

---

## 25. Acquisition — How Strangers Find You

<!-- ============================================================
📝 HOW TO FILL: List every channel where potential users will discover your product.
For each channel, write your strategy and the target number for this period.
============================================================ -->

| Channel | Tactic | Goal (Month 1) | Goal (Month 3) | Tracking Method |
|---------|--------|:--------------:|:--------------:|----------------|
| [e.g., Product Hunt] | [e.g., Featured launch] | [e.g., 500 visitors] | — | UTM links |
| [Channel] | [Tactic] | [Goal] | [Goal] | [Method] |
| [Channel] | [Tactic] | [Goal] | [Goal] | [Method] |

**Acquisition Target:**

| Milestone | Goal | Date |
|-----------|:----:|------|
| First 100 website visitors | 100 | [Date] |
| First 100 signups | 100 | [Date] |
| First 500 signups | 500 | [Date] |

---

## 26. Activation — Their First "Wow" Moment

<!-- ============================================================
📝 HOW TO FILL: Activation = the first time a user gets real value from your product.
This is the moment they go "Oh! This is amazing."
Define that moment specifically. What action must they complete?
Then design everything to get them there as fast as possible.
============================================================ -->

**Activation Event (the "Aha! Moment"):**
> *[Define the exact action a user takes that means they've experienced real value.]*  
> **Example:** *"User creates their first invoice and clicks 'Send' — within 5 minutes of signup."*  
> **Our activation event:** [Define yours]

**Activation Funnel:**

```
Step 1: User signs up
         ↓ [X]% complete this
Step 2: User completes onboarding (e.g., connects their account / adds first item)
         ↓ [X]% complete this
Step 3: User performs core action (your activation event)
         ↓ [X]% complete this
ACTIVATED ✅
```

**Activation Targets:**

| Metric | Baseline | Month 1 Target | Month 3 Target |
|--------|:--------:|:--------------:|:--------------:|
| Activation rate (% who reach step 3) | 0% | 30% | 50% |
| Time to activation | — | < 10 min | < 5 min |

**Tactics to Improve Activation:**
- [ ] Reduce steps in onboarding to [X] or fewer
- [ ] Add progress indicator during onboarding
- [ ] Send "getting started" email if user doesn't activate within 24h
- [ ] [Other tactic]

---

## 27. Retention — Do They Come Back?

<!-- ============================================================
📝 HOW TO FILL: Retention tells you if your product is actually valuable.
If users don't come back, no amount of acquisition will save you.
Track retention by cohort (everyone who signed up in Week X).
============================================================ -->

**Retention Targets:**

| Cohort Retention | Target |
|-----------------|:------:|
| Day 1 (came back the next day) | > 40% |
| Day 7 (still using after 1 week) | > 25% |
| Day 30 (still using after 1 month) | > 15% |
| Month 3 (still active / paying) | > 10% |

**Retention Tactics:**

| Tactic | Description | Launch Date |
|--------|-------------|-------------|
| [e.g., Weekly email digest] | [Send users their weekly summary every Monday] | [Date] |
| [e.g., In-app notifications] | [Remind users of incomplete actions] | [Date] |
| [e.g., Progress tracking] | [Show users a streak or usage milestone] | [Date] |
| [Tactic] | [Description] | [Date] |

**Churn Analysis Process:**
> *[What will you do when a user churns? How will you learn from it?]*  
> Example: "Send a 2-question exit survey. Call every churned paying customer. Review in monthly metrics meeting."

---

## 28. Referral — Do They Tell Their Friends?

<!-- ============================================================
📝 HOW TO FILL: Referral is how you grow without spending money on ads.
Design a referral loop where existing users bring in new users.
============================================================ -->

**Referral Mechanism:**
> *[How will users refer others? What's the incentive?]*  
>
> **Example:** *"Users get 1 free month for every paying friend they refer. Friend gets 20% off their first month."*

| Element | Design |
|---------|--------|
| Referral trigger (when to ask) | [e.g., After user activates / after 7 days] |
| Sharing method | [e.g., Unique link, email invite, social share] |
| Referrer reward | [e.g., 1 free month / $X credit / free feature] |
| Referee reward | [e.g., 20% off / free trial extension] |
| Tracking | [e.g., PostHog referral tracking / ReferralHero] |

**Referral Target:**

| Metric | Goal |
|--------|:----:|
| Viral coefficient (K-factor) | > 0.5 (every 2 users bring 1 new user) |
| % of users who refer someone | > 15% |
| Signups from referral (Month 3) | > 20% of all signups |

---

## 29. Revenue — Are They Paying?

<!-- ============================================================
📝 HOW TO FILL: Track revenue metrics weekly.
MRR = Monthly Recurring Revenue (sum of all active subscriptions)
ARPU = Average Revenue Per User
LTV = Lifetime Value (how much a customer pays before they leave)
CAC = Customer Acquisition Cost (how much it costs to get 1 customer)
============================================================ -->

**Revenue Targets:**

| Metric | Month 1 | Month 3 | Month 6 (500 customers) |
|--------|:-------:|:-------:|:------------------------:|
| Paying customers | [#] | [#] | 500 |
| MRR | $[X] | $[X] | $[X] |
| ARPU | $[X]/mo | $[X]/mo | $[X]/mo |
| Conversion rate (free→paid) | [X]% | [X]% | [X]% |
| Churn rate (monthly) | < [X]% | < [X]% | < [X]% |
| LTV | $[X] | $[X] | $[X] |
| CAC | $[X] | $[X] | $[X] |
| LTV : CAC ratio | > 3:1 | > 3:1 | > 3:1 |

---

## 30. Customer Milestone Tracker 🎯

<!-- ============================================================
📝 HOW TO FILL: Record these milestones as they happen.
These are your wins — celebrate them!
============================================================ -->

| Milestone | Date Achieved | How They Found Us | Notes |
|-----------|:-------------:|-------------------|-------|
| 🥇 1st user signed up | | | |
| 💰 1st paying customer | | | |
| 🎉 10th customer | | | |
| 🚀 50th customer | | | |
| 💯 100th customer | | | |
| 🌟 250th customer | | | |
| 🏆 500th customer | | | |

---

# PART 10 · POST-LAUNCH OPERATIONS
*Keeping it running and making it better*

---

## 31. Feedback Loop System

<!-- ============================================================
📝 HOW TO FILL: How will you collect, organize, and act on user feedback?
Great products improve constantly. Design your feedback system before you launch.
============================================================ -->

### 31.1 Feedback Channels

| Channel | Tool | Frequency | Owner |
|---------|------|:---------:|-------|
| In-app NPS survey | [e.g., Delighted / Typeform] | Monthly | [Name] |
| Support tickets | [e.g., Email / Crisp / Intercom] | Ongoing | [Name] |
| User interviews | [e.g., Cal.com + Zoom] | Bi-weekly | [Name] |
| Feature requests | [e.g., Canny / Linear] | Ongoing | [Name] |
| Social listening | [e.g., Mentions, hashtags] | Weekly | [Name] |

### 31.2 Weekly Metrics Review

> Every [day of week], review:
> - [X] new signups vs. target
> - Activation rate this week
> - Churn (cancellations or churned users)
> - Top support issues
> - AI feature usage and errors
> - Revenue vs. target

### 31.3 Iteration Principles
> - **Ship small, ship often.** A 1-hour improvement shipped beats a 3-day improvement delayed.
> - **Fix bugs before features.** A broken product repels more users than a new feature attracts.
> - **Listen more than you build.** 30 minutes of user calls > 3 hours of guessing.

---

## 32. Product Roadmap (Next 90 Days Post-Launch)

<!-- ============================================================
📝 HOW TO FILL: After launch, plan your next 90 days of improvements.
Focus on what will most improve retention and conversion — not what's most exciting.
============================================================ -->

| Quarter | Theme | Key Features / Changes | Success Metric |
|---------|-------|----------------------|----------------|
| Month 1 | Stabilize & Fix | [Bug fixes, onboarding improvements] | Activation > 40% |
| Month 2 | Grow | [Top requested features, referral program] | MRR doubles |
| Month 3 | Retain | [Engagement features, integrations] | Day-30 retention > 20% |

---

# APPENDICES

---

## A. Glossary

<!-- ============================================================
📝 HOW TO FILL: Define any words or terms specific to your product or industry.
If a team member or user might not know what a word means, define it here.
============================================================ -->

| Term | Definition |
|------|------------|
| [Term] | [Plain-English definition] |
| MRR | Monthly Recurring Revenue — the predictable income from subscriptions each month |
| LLM | Large Language Model — the AI technology (like Claude or GPT) that powers AI features |
| AARRR | Acquisition, Activation, Retention, Referral, Revenue — a framework for growth |
| [Term] | [Definition] |

---

## B. Open Questions & Decisions Needed

<!-- ============================================================
📝 HOW TO FILL: Log anything that's unresolved here.
Assign each question to someone and set a "decide by" date.
Don't let open questions block progress — set a deadline and decide.
============================================================ -->

| # | Question | Owner | Decide By | Decision Made |
|---|---------|-------|:---------:|--------------|
| 1 | [e.g., Should we support Google login at launch?] | [Name] | [Date] | [TBD / Yes / No] |
| 2 | [Question] | [Owner] | [Date] | [TBD] |

---

## C. Decision Log

<!-- ============================================================
📝 HOW TO FILL: Record every major decision you make and WHY.
Future-you will thank present-you for writing these down.
============================================================ -->

| Date | Decision | Rationale | Made By |
|------|---------|-----------|---------|
| [Date] | [e.g., We chose Supabase over Firebase] | [e.g., Postgres is more familiar + open source] | [Name] |
| [Date] | [Decision] | [Why] | [Who] |

---

## D. References & Resources

<!-- ============================================================
📝 HOW TO FILL: Link to everything relevant — designs, docs, repos, research.
This document should be the hub that connects all other documents.
============================================================ -->

| Resource | Link | Notes |
|----------|------|-------|
| GitHub Repository | [Link] | Main codebase |
| Figma Design File | [Link] | UI designs and prototypes |
| Architecture Diagram | [Link] | System design |
| Analytics Dashboard | [Link] | PostHog / Mixpanel |
| Staging Environment | [Link] | For testing |
| Support Channel | [Link] | Customer support |
| Competitor Research | [Link] | Market analysis notes |
| User Interview Notes | [Link] | Raw feedback from users |
| [Resource] | [Link] | [Notes] |

---

## E. Change Request Log

<!-- ============================================================
📝 HOW TO FILL: When someone asks to change the scope of this PRD
(add a feature, remove one, change a requirement), log it here.
Decide: is this a v1 change, or something for a future version?
============================================================ -->

| Date | Requested By | Change Requested | Decision | Impact |
|------|-------------|-----------------|:--------:|--------|
| [Date] | [Name] | [e.g., Add dark mode] | ✅ Approved / ❌ Deferred | [e.g., +3 days] |
| [Date] | [Name] | [Change] | [Decision] | [Impact] |

---

<br>

---

> ## ✅ PRD Completion Checklist
>
> Before sharing this PRD with anyone, make sure every section is filled:
>
> **Part 1 — Foundation**
> - [ ] Section 1: Product Overview ✓
> - [ ] Section 2: Problem Statement ✓
> - [ ] Section 3: User Personas ✓
> - [ ] Section 4: Market Context ✓
> - [ ] Section 5: Assumptions & Risks ✓
>
> **Part 2 — Design**
> - [ ] Section 6: Goals & Metrics ✓
> - [ ] Section 7: User Stories ✓
> - [ ] Section 8: Feature Specs ✓
> - [ ] Section 9: UX & Design ✓
> - [ ] Section 10: Navigation ✓
>
> **Part 3 — AI Architecture**
> - [ ] Section 11: AI Component Specs ✓
>
> **Part 4 — Technical**
> - [ ] Section 12: Tech Stack ✓
> - [ ] Section 13: Data Model ✓
> - [ ] Section 14: API Design ✓
> - [ ] Section 15: Integrations ✓
> - [ ] Section 16: Security & Performance ✓
>
> **Part 5 — Development Plan**
> - [ ] Section 17: Milestones ✓
> - [ ] Section 18: AI Dev Workflow ✓
>
> **Part 6 — QA**
> - [ ] Section 19: Acceptance Criteria ✓
> - [ ] Section 20: Test Suite ✓
> - [ ] Section 21: UAT Plan ✓
>
> **Part 7 — Legal**
> - [ ] Section 22: Privacy & Compliance ✓
>
> **Part 8 — Launch**
> - [ ] Section 23: Launch Checklist ✓
> - [ ] Section 24: GTM Strategy ✓
>
> **Part 9 — Growth**
> - [ ] Sections 25–30: AARRR Funnel + 500 Customers ✓
>
> **Part 10 — Post-Launch**
> - [ ] Sections 31–32: Feedback + Roadmap ✓
>
> **When everything is checked, change Document Status to 🟢 Active.**

---

*PRD Template v1.0 · AI-Driven Development Life Cycle*  
*Built for solo founders, indie hackers, and hybrid teams using AI-assisted development*  
*From first commit → first 500 customers*
