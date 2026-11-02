<!-- ═══════════════════════════════════════════════════════════════════════
     📋 TASK_BACKLOG.md — AI-Driven Development Lifecycle Template
     Version: 1.0  |  Compatible With: GitHub · GitLab · Notion · Obsidian · VS Code
     Designed for: Solo AI-Assisted Development (Claude + Agile Sprints)
     Lifecycle: Idea → MVP → QA → Beta → Launch → First 500 Customers
     ═══════════════════════════════════════════════════════════════════════ -->

---

# 🧭 HOW TO FILL THIS DOCUMENT — READ THIS FIRST

> 👋 **Welcome!** This guide takes about **5 minutes** to read.
> Read it once — then scroll past it every time after that.
> The instructions live inside the document on purpose, so the document teaches itself.

---

## 📚 What Is a Task Backlog?

A **Task Backlog** is your master to-do list — the single place where every piece of
work for your product is written down, tracked, and updated.

Think of it like a scoreboard for your project:

| 🟢 A Task Backlog IS | 🔴 A Task Backlog is NOT |
|---|---|
| Every task, in one place, before work starts | A daily diary or meeting notes doc |
| A living document updated every single day | Something you fill in once and forget |
| A communication tool for your future self | A replacement for code documentation |
| A planning tool used BEFORE writing any code | A post-mortem written after the project |

---

## 👶 Who Can Fill This? Anyone!

This template is designed so that even someone with **zero technical background**
(yes, including a curious 10-year-old!) can:

- ✅ Add a new task
- ✅ Update a task's status
- ✅ Understand what's being built and why
- ✅ Know exactly what "done" looks like for every task

**What you need:** A text editor (Notion, VS Code, Obsidian, GitHub, even Notepad).
**Time to set up:** ~30 minutes the first time. ~5-10 minutes per day to keep it updated.

---

## 📖 Step-by-Step Setup Guide

### 📌 Step 1 — Fill In the Project Header
Scroll to **"📊 PROJECT OVERVIEW"** below and replace every `[PLACEHOLDER]`
with your real project details. Don't skip the "AI Tools Used" row.

> ✏️ **Example:**
> `| **🏷️ Project Name** | Nova Health App |`

---

### 📌 Step 2 — Set Your Milestone Dates
Scroll to **"🗺️ MILESTONE MAP"** and write a realistic target date for each phase.
Estimates are fine — you can change dates as you learn more.

> 📏 **Rule of Thumb for Timeline Estimates:**
> - Phase 1 (Planning): 1–2 weeks
> - Phase 2 (Development): 4–12 weeks (depends on product size)
> - Phase 3 (QA + Beta): 2–4 weeks
> - Phase 4 (Launch → 500 Customers): 4–12 weeks

---

### 📌 Step 3 — Understand the Two Parts of Every Phase
Each phase has two parts you fill in:

**Part A — Task Summary Table:** One short row per task (fill this first).
**Part B — Task Detail Cards:** The full details for each task (fill when the task is about to start).

> 💡 **Pro Tip:** You don't need to fill ALL task details upfront.
> Add the summary row first. Then fill the detail card when the task enters your sprint.

---

### 📌 Step 4 — Fill Each Task Card
Every task card has these sections. Here's what to put in each:

| Section | What to Write | Example |
|---|---|---|
| **Task ID** | Phase code + number (increment by 1) | `PLAN-001`, `DEV-003`, `QA-007` |
| **Title** | Short action phrase. Start with a verb. | `"Build user login screen"` NOT `"Login"` |
| **Status** | One emoji from the Status Key below. Update daily! | `⬜ To Do` |
| **Priority** | MoSCoW label + urgency level | `🔴 Must Have · High` |
| **Effort** | Your honest time estimate | `M — ~4-8 hours` |
| **Executor** | Who does this? AI, You, or Both? | `🔀 Hybrid` |
| **Description** | 1–3 sentences: what needs to be done AND why it matters | Clear, specific sentences |
| **Acceptance Criteria** | A checklist: done means EVERY box is checked | `- [ ] User can log in with email + password` |
| **Claude Prompt** | Copy-paste the exact prompt you gave Claude | Paste the full prompt text |
| **AI Output / Notes** | Results, links, decisions after the task is done | Links, summaries, key decisions |

---

### 📌 Step 5 — Write Great Acceptance Criteria
When a task is ✅ Done, **every checkbox must be checked**. If even one is unchecked — it's not done.

> ✅ **Good Acceptance Criteria (specific and testable):**
> - [ ] User can sign up with email and password
> - [ ] Password must be at least 8 characters — shows error if shorter
> - [ ] Welcome email is sent within 60 seconds of successful signup
> - [ ] User is redirected to the dashboard after signup

> ❌ **Bad Acceptance Criteria (too vague):**
> - [ ] Login works
> *(Who decides what "works" means? Write it so that ANY person could verify it.)*

---

### 📌 Step 6 — Document Every Claude Prompt
Every time Claude helped you plan, write code, design, or analyze —
**paste that prompt into the task card.** This gives you:

- 🔁 The ability to re-run the same prompt on a future project
- 📖 A record of HOW the product was built with AI
- 🧠 A library of prompts that actually worked

> 💡 **Workflow: AI-Spec-Driven Development**
> 1. Write the task card (Description + Acceptance Criteria)
> 2. Give Claude the task card and ask for an **implementation plan**
> 3. Review and approve the plan before Claude writes any code
> 4. Claude executes — you review the output
> 5. Check off Acceptance Criteria, mark task Done

---

### 📌 Step 7 — Run Sprints (2-Week Cycles)

Each sprint should have:
- A **Sprint Goal** (1 sentence — what the user gains by end of sprint)
- A list of tasks **pulled from the backlog** into that sprint
- A **Sprint Retrospective** written at the end (what worked, what didn't)

> ⏱️ **2-Week Sprint Rhythm:**
> - **Day 1:** Sprint Planning — pick tasks, set goal, break large tasks down
> - **Days 2–13:** Build daily, update task statuses every day
> - **Day 14:** Sprint Review — what shipped? what carries over? write retro

---

### 📌 Step 8 — Update Statuses Daily (2 Minutes)
Every day, ask yourself three questions:
1. Did anything move from To Do → In Progress today?
2. Did anything move from In Progress → Done today?
3. Is anything blocked? Write the blocker reason in the task Notes.

That's it. Two minutes. Every day. A stale backlog is worse than no backlog.

---

### 📌 Step 9 — Review & Improve Weekly
Every Friday (or end of sprint), run the **Backlog Health Checklist** in the Appendix.
This keeps your backlog clean, accurate, and trustworthy.

---

### 📌 Step 10 — Celebrate Your Milestones 🎉
When you hit a milestone (MVP done, first beta user, first paying customer, 500 customers!),
mark it in the Milestone Map. Add a note about what you learned.
Your future self — and anyone you share this with — will love reading it.

---

## ⚠️ GOLDEN RULES — NEVER BREAK THESE

```
1. 📝 WRITE BEFORE YOU BUILD   — Every task must be in the backlog before work starts.
2. ✅ DONE = ALL CRITERIA CHECKED — If any acceptance criterion box is unchecked, it's NOT done.
3. ✂️ BREAK BIG TASKS DOWN      — Any task bigger than 3 days must be split into smaller ones.
4. 🤖 DOCUMENT EVERY AI PROMPT  — Paste every Claude prompt into the task. No exceptions.
5. 🔄 UPDATE STATUSES DAILY     — Even if only moving To Do → In Progress. 2 minutes. Every day.
6. 🚫 NEVER DELETE CANCELLED    — Mark tasks ❌ Cancelled and keep them. History matters.
7. 🎯 ONE AI TASK AT A TIME     — Give Claude one task card at a time. Don't batch tasks.
8. 🔗 LIST ALL DEPENDENCIES     — If Task B can't start until Task A finishes, write it down.
```

---

# 🔑 QUICK REFERENCE LEGEND

## Status Icons (copy-paste these)

| Icon | Status | Meaning |
|:---:|---|---|
| ⬜ | **To Do** | Task exists, not started yet |
| 🟡 | **In Progress** | Actively being worked on RIGHT NOW |
| 🔁 | **In Review** | AI output or code is being reviewed / tested by you |
| ✅ | **Done** | Every acceptance criterion is checked ✓ |
| ⛔ | **Blocked** | Cannot proceed — waiting on a dependency or a decision |
| ❌ | **Cancelled** | No longer needed — keep it, don't delete it |
| 🔜 | **Next Sprint** | Planned for the next sprint (queued from backlog) |

## Priority Labels (copy-paste these)

| Label | When to Use |
|---|---|
| 🔴 **Must Have · High** | Product literally cannot launch without this |
| 🟠 **Must Have · Medium** | Critical, but can wait until end of sprint |
| 🟡 **Should Have · High** | Delivers strong value — do it soon |
| 🟢 **Could Have · Low** | Nice to have — deliver if time allows |
| ⚫ **Won't Have (This Version)** | Out of scope for v1 — revisit in v2 |

## Effort Sizes (copy-paste these)

| Size | Time | Use When... |
|:---:|---|---|
| **XS** | ~1 hour | Tiny: fix a typo, update a config value, write one function |
| **S** | 2–4 hours | Small: one UI component, one API endpoint, one bug fix |
| **M** | 4–8 hours | Medium: a full feature (UI + API + database) |
| **L** | 1–3 days | Large: a complete user flow (auth, payments, onboarding) |
| **XL** | 3+ days | 🚨 STOP — this is too big. Break it into smaller tasks. |

## Executor Tags (copy-paste these)

| Tag | Meaning |
|:---:|---|
| 🤖 **AI** | Claude or another AI agent handles this task end-to-end |
| 👤 **Human** | You handle this manually — no significant AI assistance |
| 🔀 **Hybrid** | You and Claude collaborate: Claude drafts, you review and refine |

---
---

# 📊 PROJECT OVERVIEW

> 📝 **HOW TO FILL:** Replace every `[PLACEHOLDER]` with your actual project details.
> Use "N/A" for anything that doesn't apply yet. Use `YYYY-MM-DD` for all dates.

| Field | Your Answer |
|---|---|
| **🏷️ Project Name** | [Your Product Name Here] |
| **🌐 Product Type** | [e.g., SaaS Web App / Mobile App (iOS + Android) / AI Tool / API] |
| **🎯 Problem Being Solved** | [One sentence: what pain point does this solve for real people?] |
| **👥 Target Users** | [Who are your users? e.g., "Freelance designers aged 25–40 who struggle with invoicing"] |
| **💡 Core Value Proposition** | [Why would someone choose this over every other solution that exists?] |
| **📅 Project Start Date** | [YYYY-MM-DD] |
| **🚀 Target MVP Date** | [YYYY-MM-DD] |
| **🌟 Target Public Launch Date** | [YYYY-MM-DD] |
| **🎉 500 Customers Goal Date** | [YYYY-MM-DD] |
| **📍 Current Phase** | [Phase 1 / Phase 2 / Phase 3 / Phase 4] |
| **🏃 Current Sprint** | [Sprint 0 / Sprint 1 / Sprint 2 / ...] |
| **👤 Product Owner** | [Your Name] |
| **🤖 Primary AI Tool** | [Claude (Anthropic)] |
| **🔗 Repository URL** | [GitHub/GitLab URL — or "Local, not yet published"] |
| **📁 Tech Stack** | [e.g., Next.js · Supabase · React Native · Claude API · Stripe] |
| **💰 Pricing Model** | [e.g., Freemium / Subscription $X/mo / One-time purchase] |

---

# 🗺️ MILESTONE MAP

> 📝 **HOW TO FILL:** Set a realistic target date for each milestone.
> Update the Status column as you hit each milestone. Never skip a milestone — note it even if late.

| # | 🏆 Milestone | 🎯 Target Date | 📍 Status | 🗒️ Notes / Learnings |
|:---:|---|:---:|:---:|---|
| 1 | 🌱 **Phase 1 Complete** — Plan is locked, no more scope changes before build | [YYYY-MM-DD] | ⬜ Not Started | |
| 2 | 🏗️ **First Working Build** — Core features run locally without crashing | [YYYY-MM-DD] | ⬜ Not Started | |
| 3 | 🚢 **MVP Deployed** — Live on the internet, accessible via URL | [YYYY-MM-DD] | ⬜ Not Started | |
| 4 | 🧪 **Zero Critical Bugs** — All P0/P1 issues fixed, passes test suite | [YYYY-MM-DD] | ⬜ Not Started | |
| 5 | 👥 **First Beta User** — First real human (not you) uses the product | [YYYY-MM-DD] | ⬜ Not Started | |
| 6 | 🚀 **Public Launch** — Product is live and open to new signups | [YYYY-MM-DD] | ⬜ Not Started | |
| 7 | 💰 **First Paying Customer** — First transaction successfully processed | [YYYY-MM-DD] | ⬜ Not Started | |
| 8 | 📈 **100 Active Users** — 100 users have logged in at least once | [YYYY-MM-DD] | ⬜ Not Started | |
| 9 | 🎉 **500 Customers** — 500 customers using the product 🥳 | [YYYY-MM-DD] | ⬜ Not Started | |

---

# 🏃 SPRINT TRACKER

> 📝 **HOW TO FILL:** Add one row per sprint. Update "Completed/Total" at end of each sprint.
> A sprint = a 2-week work cycle. Sprint 0 = setup sprint (before feature development).

| Sprint | 🎯 Goal (One Sentence) | 📅 Start | 📅 End | 📍 Status | ✅ Done/Total |
|:---:|---|:---:|:---:|:---:|:---:|
| **Sprint 0** | Dev environment running, project deployed, database live | [YYYY-MM-DD] | [YYYY-MM-DD] | ⬜ Not Started | 0 / 0 |
| **Sprint 1** | [Write your sprint 1 goal here] | [YYYY-MM-DD] | [YYYY-MM-DD] | ⬜ Not Started | 0 / 0 |
| **Sprint 2** | [Write your sprint 2 goal here] | [YYYY-MM-DD] | [YYYY-MM-DD] | ⬜ Not Started | 0 / 0 |

> ➕ Add a new row each time you plan a new sprint.

---
---

# 🌱 PHASE 1: IDEA → MVP PLANNING

> **🎯 Phase Goal:** Turn your idea into a clear, detailed, buildable plan — before writing a single line of code.
> **📍 When Is Phase 1 Done?** Every task below is ✅ Done.
> **⏱️ Expected Duration:** 1–2 weeks.
> **🤖 Who Does This:** Mostly 🔀 Hybrid (You + Claude).

---

## 📋 Phase 1 — Task Summary Table

> 📝 **HOW TO FILL:** Add one row per task. Fill in the full task card below when the task is about to start.

| Task ID | Task Title | Status | Priority | Effort | Executor |
|:---:|---|:---:|---|:---:|:---:|
| PLAN-001 | Define product vision & problem statement | ⬜ To Do | 🔴 Must Have · High | S | 🔀 Hybrid |
| PLAN-002 | Create user personas (who are your customers?) | ⬜ To Do | 🔴 Must Have · High | S | 🔀 Hybrid |
| PLAN-003 | Write Product Requirements Document (PRD) | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |
| PLAN-004 | Create feature list & prioritize with MoSCoW | ⬜ To Do | 🔴 Must Have · High | S | 🔀 Hybrid |
| PLAN-005 | Define tech stack & system architecture | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |
| PLAN-006 | Design database schema (first draft) | ⬜ To Do | 🟠 Must Have · Medium | M | 🔀 Hybrid |
| PLAN-007 | Set up project repository & folder structure | ⬜ To Do | 🔴 Must Have · High | XS | 👤 Human |
| PLAN-008 | Create CLAUDE.md — AI development context file | ⬜ To Do | 🟡 Should Have · High | S | 🔀 Hybrid |

---

## 🗂️ Phase 1 — Task Detail Cards

---

### PLAN-001: Define Product Vision & Problem Statement

| Field | Details |
|---|---|
| **📍 Phase** | Phase 1: Idea → MVP Planning |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | S — ~2–4 hours |
| **🤖 Executor** | 🔀 Hybrid (You + Claude) |
| **🏃 Sprint** | Sprint 0 — Planning |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | None — this is the first task |
| **⛓️ Blocks** | PLAN-003, PLAN-004 |

**📝 Description**
> Define what your product does, who it's for, and what single problem it solves better than anything else.
> This is the north star that guides every decision for the life of the project.
> If you can't describe it in one sentence, you're not ready to build it yet.

**🎯 Acceptance Criteria**
- [ ] Product name is decided and written down
- [ ] One-sentence problem statement is written (format: `"[User type] struggle with [problem] because [root cause]"`)
- [ ] One-sentence vision statement is written (format: `"We help [user] to [outcome] by [unique approach]"`)
- [ ] 3–5 key outcomes the product delivers to users are listed
- [ ] 3 measurable success metrics are defined for the first 90 days post-launch
- [ ] 2–3 key risks or early assumptions to validate are identified
- [ ] Document is saved and the file link is added to the Output section below

**🤖 Claude Prompt / AI Instructions**
```
You are an experienced product strategist. Help me define the core vision for my product.

Product name: [your product name, or "working title: [name]"]
What I'm building: [describe your idea in 2-3 sentences]
Who I think my users are: [describe your target users]
The main problem I'm solving: [describe the pain point]

Please output:
1. A refined one-sentence problem statement
   Format: "[User type] struggle with [problem] because [root cause]"
2. A one-sentence product vision statement
   Format: "We help [user] to [outcome] by [unique approach]"
3. 5 key outcomes this product delivers to users (bullet list)
4. 3 measurable success metrics for the first 90 days after launch
5. 3 risks or assumptions I need to validate before building

Keep language simple — no jargon. Aim for clarity a non-technical person would understand.
```

**📎 AI Output / Notes**
> - **Problem Statement:** [paste result here after completing]
> - **Vision Statement:** [paste result here after completing]
> - **Success Metrics:** [paste result here]
> - **Document Link:** [add link to your saved notes or PRD file]

---

### PLAN-002: Create User Personas

| Field | Details |
|---|---|
| **📍 Phase** | Phase 1: Idea → MVP Planning |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | S — ~2–4 hours |
| **🤖 Executor** | 🔀 Hybrid (You + Claude) |
| **🏃 Sprint** | Sprint 0 — Planning |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-001 |
| **⛓️ Blocks** | PLAN-003, PLAN-004, GTM-001 |

**📝 Description**
> Create 1–3 fictional but realistic characters who represent your ideal customers.
> A persona is built from research, not guesses. The better you understand your user,
> the better every product decision becomes — features, design, pricing, marketing, everything.

**🎯 Acceptance Criteria**
- [ ] Primary Persona (Persona 1) is fully defined: name, age range, job title, goals, frustrations, tech literacy level
- [ ] Each persona has 3+ "Jobs To Be Done" (specific tasks they need your product to help with)
- [ ] Each persona has 3+ frustrations with existing solutions (what they dislike about alternatives)
- [ ] A fictional but realistic quote captures each persona's mindset
- [ ] A description of how they solve this problem TODAY (before your product) is included
- [ ] Personas are saved in a document and linked below

**🤖 Claude Prompt / AI Instructions**
```
You are a UX researcher. Help me create detailed, realistic user personas for my product.

My product: [product name] — [one-sentence description]
What I believe about my target users: [describe who you think uses this]

For each persona, please provide:
1. Name (fictional), Age range, Job title
2. Goals: What are they trying to achieve in work/life related to this product?
3. Frustrations: What are their top 3 pain points with current solutions?
4. Tech literacy: Beginner / Intermediate / Advanced — and what tools they use daily
5. Jobs To Be Done: 3 specific tasks they're trying to accomplish that my product can help with
6. A fictional quote that captures their mindset and relationship to the problem
7. How they currently solve this problem today (before my product exists)

Create 2 distinct personas that represent meaningfully different user types.
Keep language concrete and specific — avoid vague generalizations.
```

**📎 AI Output / Notes**
> - **Persona 1:** [name, title, age — e.g., "Alex, 32, Freelance Designer"]
> - **Persona 2:** [name, title, age — e.g., "Maria, 45, Small Business Owner"]
> - **Personas Document:** [link to saved document]

---

### PLAN-003: Write Product Requirements Document (PRD)

| Field | Details |
|---|---|
| **📍 Phase** | Phase 1: Idea → MVP Planning |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | M — ~4–8 hours |
| **🤖 Executor** | 🔀 Hybrid (You + Claude) |
| **🏃 Sprint** | Sprint 0 — Planning |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-001, PLAN-002 |
| **⛓️ Blocks** | PLAN-004, PLAN-005, DEV-001 |

**📝 Description**
> The PRD is your product's blueprint. It describes every feature, user flow, and
> requirement your product must have to launch. It's the "instruction manual" written
> before the product exists. Anyone who reads it should understand what's being built and why.

**🎯 Acceptance Criteria**
- [ ] PRD includes: executive summary, problem statement, user personas (summary)
- [ ] PRD includes: all MVP features with user stories in `"As a [user], I want [action], so that [outcome]"` format
- [ ] PRD includes: user flows (numbered steps showing how users move through key workflows)
- [ ] PRD includes: non-functional requirements (performance, security, mobile responsiveness, accessibility)
- [ ] PRD includes: out-of-scope section (explicitly states what is NOT in v1)
- [ ] PRD includes: open questions and risks section
- [ ] PRD has been read aloud — it makes sense to a non-technical person
- [ ] PRD is saved as a separate file and linked below

**🤖 Claude Prompt / AI Instructions**
```
You are a senior product manager. Help me write a complete Product Requirements Document (PRD).

Product: [name]
Vision: [paste vision statement from PLAN-001]
Personas: [paste Persona 1 and Persona 2 summaries from PLAN-002]
MVP Features I want to include:
- [Feature 1]
- [Feature 2]
- [Feature 3 — add as many as you have]

Please write a complete PRD with these sections:
1. Executive Summary (3-4 sentences)
2. Problem Statement & Background
3. User Personas (brief summary)
4. Goals & Success Metrics
5. Feature Requirements — for each feature: user story, description, and acceptance criteria
6. Key User Flows — numbered steps for: signup, core feature, and [your key workflow]
7. Non-Functional Requirements (performance, security, mobile support, accessibility)
8. Out of Scope for v1 (be explicit about what you're NOT building)
9. Open Questions & Risks
10. Appendix (any additional notes or references)

Use simple, clear language. Avoid jargon. Assume the reader might be non-technical.
```

**📎 AI Output / Notes**
> - **PRD Document:** [link to PRD file]
> - **PRD Version:** v1.0
> - **Last Updated:** [YYYY-MM-DD]
> - **Open Questions to Resolve:** [list any unresolved questions from the PRD]

---

### PLAN-004: Create Feature List & Prioritize with MoSCoW

| Field | Details |
|---|---|
| **📍 Phase** | Phase 1: Idea → MVP Planning |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | S — ~2–4 hours |
| **🤖 Executor** | 🔀 Hybrid (You + Claude) |
| **🏃 Sprint** | Sprint 0 — Planning |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-001, PLAN-002, PLAN-003 |
| **⛓️ Blocks** | DEV-001 |

**📝 Description**
> List every feature you want to build and sort them by importance using MoSCoW.
> This is how you decide what's in the MVP (v1) and what waits for v2, v3, and beyond.
> The goal: build the smallest possible product that delivers real value to real users.
> Ruthless prioritization is how solo developers ship on time.

**🎯 Acceptance Criteria**
- [ ] Every feature idea is listed (even the wild ones — don't filter yet)
- [ ] Every feature has a MoSCoW label: Must Have / Should Have / Could Have / Won't Have
- [ ] "Must Have" features alone form a working, valuable MVP
- [ ] No single "Must Have" feature takes longer than 1 sprint to build (if so, break it down)
- [ ] "Won't Have" features are moved to a "Future Features" section
- [ ] Feature list is saved in the PRD (PLAN-003) or linked separately

**🤖 Claude Prompt / AI Instructions**
```
You are a product strategist helping me cut my feature list down to an MVP.

My product: [name and one-sentence description]
Target users: [paste Persona 1 and 2 from PLAN-002]
Full feature list I'm considering:
[paste every feature idea here — don't filter, just list them all]

Please:
1. Apply MoSCoW prioritization to every feature:
   - Must Have: MVP cannot launch without this
   - Should Have: Strong value, do in first month after launch
   - Could Have: Nice-to-have, do if ahead of schedule
   - Won't Have (v1): Explicitly out of scope for now

2. For each Must Have feature: explain in one sentence WHY it's critical for launch

3. For each Won't Have feature: suggest when it might be added (v1.1, v2, v3)

4. Flag any feature that seems too large for one sprint and should be broken down further

5. Suggest 2-3 features I might have overlooked based on my user personas

Goal: Must Have list should be buildable by 1 developer in 8-12 weeks maximum.
```

**📎 AI Output / Notes**
> - **Must Have Features Count:** [number] features
> - **MVP Summary:** [one sentence describing what the MVP does]
> - **Feature List Document:** [link]
> - **Future Features (Won't Have v1):** [list or link]

---

### PLAN-005: Define Tech Stack & System Architecture

| Field | Details |
|---|---|
| **📍 Phase** | Phase 1: Idea → MVP Planning |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | M — ~4–8 hours |
| **🤖 Executor** | 🔀 Hybrid (You + Claude) |
| **🏃 Sprint** | Sprint 0 — Planning |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-003, PLAN-004 |
| **⛓️ Blocks** | PLAN-006, PLAN-007, DEV-001 |

**📝 Description**
> Decide what technologies, frameworks, databases, and external services you'll use to build
> the product. This decision affects everything downstream — choose based on your skill level,
> the product's requirements, and how fast you can ship with AI assistance.
> Wrong tech choices early create painful refactoring later.

**🎯 Acceptance Criteria**
- [ ] Frontend framework is decided and documented (e.g., Next.js, React Native, Flutter, SwiftUI)
- [ ] Backend approach is decided (e.g., Next.js API routes, Node/Express, FastAPI, Supabase Edge Functions)
- [ ] Database is decided (e.g., PostgreSQL/Supabase, Firebase, PlanetScale)
- [ ] Authentication method is decided (e.g., Supabase Auth, Clerk, Auth0)
- [ ] AI/LLM integration is defined (e.g., Claude API via Anthropic SDK — which model, how called)
- [ ] Cloud hosting is decided (e.g., Vercel, Railway, Expo EAS for mobile)
- [ ] Third-party services are listed (payments, email, analytics, push notifications, etc.)
- [ ] Architecture is documented as a diagram or clear written description
- [ ] Tech stack decision is added to the Project Overview table

**🤖 Claude Prompt / AI Instructions**
```
You are a senior software architect. Help me choose the right tech stack for my product.

My product: [description]
Must Have features: [list from PLAN-004]
My current skill level: [Beginner / Intermediate / Advanced]
Languages I know: [list them]
Platform: [Web App / Mobile App (iOS + Android) / Both]

My constraints:
- Budget: [e.g., free tier tools first, then under $100/mo]
- Timeline: [e.g., want to ship MVP in 8 weeks]
- Team: Solo developer using Claude as my AI coding partner

Please recommend:
1. Frontend framework — best choice for my needs + 2-sentence reason
2. Backend approach — best choice for my needs + 2-sentence reason
3. Database — best option + 2-sentence reason
4. Authentication — best service for my budget + reason
5. AI integration — how to connect Claude API to my app (which SDK, which model)
6. Hosting — where to deploy + estimated monthly cost
7. Key third-party services I'll need (payments, email, analytics, etc.)
8. Top 3 technical risks I should know about before starting

Assume I'll use Claude heavily to help write code. Factor that in.
```

**📎 AI Output / Notes**
> - **Tech Stack Summary:** [paste the final decisions here]
> - **Architecture Diagram / Description:** [link or paste]
> - **Key Technical Risks:** [list them]

---

### PLAN-006: Design Database Schema (First Draft)

| Field | Details |
|---|---|
| **📍 Phase** | Phase 1: Idea → MVP Planning |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🟠 Must Have · Medium |
| **⏱️ Effort** | M — ~4–8 hours |
| **🤖 Executor** | 🔀 Hybrid (You + Claude) |
| **🏃 Sprint** | Sprint 0 — Planning |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-004, PLAN-005 |
| **⛓️ Blocks** | DEV-005 |

**📝 Description**
> Design the data model — what information the product needs to store and how it's organized.
> A good schema designed upfront saves weeks of painful refactoring later.
> This is a first draft — it will evolve, but starting with a solid foundation matters.

**🎯 Acceptance Criteria**
- [ ] All key data entities (tables) are identified and named clearly
- [ ] Each entity has its fields listed with data types and constraints
- [ ] Relationships between entities are defined (one-to-many, many-to-many, etc.)
- [ ] Schema is reviewed by Claude for missing fields, normalization issues, and scaling risks
- [ ] Schema is documented as a table or ERD diagram
- [ ] SQL migration (or equivalent) is written and saved

**🤖 Claude Prompt / AI Instructions**
```
You are a senior database engineer. Help me design the database schema for my product.

My product: [name and description]
Must Have features: [list from PLAN-004]
Database choice: [from PLAN-005]
Expected scale: reaching 500 users in first 3-6 months

Please provide:
1. A list of all data entities (tables/collections) I need
2. For each entity: fields with data types, constraints (NOT NULL, UNIQUE, etc.), and purpose
3. Relationships between entities (describe each relationship clearly)
4. Any potential scaling issues to watch for at 500+ users
5. Recommended indexes for performance
6. The SQL CREATE TABLE statements (or equivalent for my database type)
7. A seed data script for local development testing

Format: Show the entity relationship description first, then the SQL.
```

**📎 AI Output / Notes**
> - **Entities Created:** [list them, e.g., users, projects, tasks, subscriptions]
> - **Schema Document:** [link]
> - **Migration File Location:** [e.g., `/db/migrations/001_initial_schema.sql`]

---

### PLAN-007: Set Up Project Repository & Folder Structure

| Field | Details |
|---|---|
| **📍 Phase** | Phase 1: Idea → MVP Planning |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | XS — ~1 hour |
| **🤖 Executor** | 👤 Human (with Claude for file content) |
| **🏃 Sprint** | Sprint 0 — Planning |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-005 |
| **⛓️ Blocks** | PLAN-008, DEV-001 |

**📝 Description**
> Create the project repository and establish the initial folder structure, README, gitignore,
> and environment file template. Getting this right from day one prevents messy reorganization later.
> Everything lives in version control from the very first commit.

**🎯 Acceptance Criteria**
- [ ] Repository created on GitHub/GitLab and set to private (until ready for public)
- [ ] README.md written with: project name, description, setup instructions, and tech stack
- [ ] `.gitignore` configured for the chosen tech stack (no secrets or node_modules committed)
- [ ] `.env.example` file created with all environment variable NAMES (no values — just keys)
- [ ] Initial folder structure created and documented in README
- [ ] First commit pushed to `main` branch
- [ ] Repository URL added to the Project Overview table at the top of this document
- [ ] Branch strategy documented (e.g., `main` → `develop` → `feature/[name]`)

**🤖 Claude Prompt / AI Instructions**
```
Help me set up the initial project structure for a [tech stack] project.

Project name: [name]
Tech stack: [from PLAN-005]
Key features to account for in structure: [from PLAN-004]

Please provide:
1. The recommended folder structure as a file tree (comment each folder's purpose)
2. README.md template for this project type
3. .gitignore content optimized for [tech stack]
4. .env.example with all environment variable keys I'll need (no values — just descriptive key names)
5. Any initial config files needed (e.g., next.config.js, tsconfig.json, tailwind.config.js)
6. My recommended branch strategy (main, develop, feature branches)
```

**📎 AI Output / Notes**
> - **Repository URL:** [link]
> - **Branch Strategy:** [e.g., main → develop → feature/[name]]
> - **Initial Files Created:** README.md, .gitignore, .env.example

---

### PLAN-008: Create CLAUDE.md — AI Development Context File

| Field | Details |
|---|---|
| **📍 Phase** | Phase 1: Idea → MVP Planning |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🟡 Should Have · High |
| **⏱️ Effort** | S — ~2–4 hours |
| **🤖 Executor** | 🔀 Hybrid (You + Claude) |
| **🏃 Sprint** | Sprint 0 — Planning |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-005, PLAN-006, PLAN-007 |
| **⛓️ Blocks** | All Phase 2 tasks (indirectly improves every AI interaction) |

**📝 Description**
> Create a `CLAUDE.md` file in the root of your repository. Claude reads this file before
> helping with any coding task — it gives Claude the context it needs to write code that
> fits YOUR project's patterns, naming conventions, and tech stack.
> Without this, Claude writes generic code. With it, Claude writes YOUR code.

**🎯 Acceptance Criteria**
- [ ] `CLAUDE.md` file created at the project root `/CLAUDE.md`
- [ ] File includes: project overview, tech stack summary, folder structure explanation
- [ ] File includes: coding conventions (naming, file structure, patterns used)
- [ ] File includes: what Claude should always do (e.g., always add TypeScript types, always add error handling)
- [ ] File includes: what Claude should never do (e.g., never use `any` type, never hardcode secrets)
- [ ] File includes: how errors are handled in this codebase
- [ ] File includes: list of key dependencies and what each one is used for
- [ ] File has been tested: Claude was given this file as context and produced fitting code

**🤖 Claude Prompt / AI Instructions**
```
Help me write a CLAUDE.md context file for my project.
This file will be read by Claude at the start of every coding session to understand my project.

My project: [name and description]
Tech stack: [from PLAN-005]
Database schema summary: [from PLAN-006]
Folder structure: [from PLAN-007]
My coding preferences:
- Language: [TypeScript / JavaScript / Python / etc.]
- Style: [functional components? classes? async/await? etc.]
- Testing: [what testing framework I use or plan to use]

Please write a CLAUDE.md that includes:
1. Project overview (what we're building and why)
2. Tech stack with key libraries and their purpose
3. Folder structure with explanation of each directory
4. Coding conventions and style guide
5. Common patterns used throughout the codebase
6. Things Claude should ALWAYS do (non-negotiable standards)
7. Things Claude should NEVER do (anti-patterns to avoid)
8. Error handling approach for this project
9. How to add a new feature (the standard workflow)
10. Key environment variables and what they connect to
```

**📎 AI Output / Notes**
> - **CLAUDE.md Location:** `/CLAUDE.md`
> - **Last Updated:** [YYYY-MM-DD]
> - **Test Result:** [Did Claude produce fitting code when given this context? Note improvements needed]

---
---

# 🏗️ PHASE 2: DEVELOPMENT SPRINTS

> **🎯 Phase Goal:** Build the product, one sprint at a time, using Claude to accelerate every step.
> **📍 When Is Phase 2 Done?** Every Must Have feature from PLAN-004 is built and working.
> **⏱️ Expected Duration:** 4–12 weeks (2-week sprints).
> **🤖 Who Does This:** Mostly 🔀 Hybrid and 🤖 AI.

> 📝 **HOW TO USE PHASE 2:**
> 1. Sprint 0 (below) is your setup sprint — complete these first.
> 2. For each new sprint, copy the **Sprint Template** at the bottom of this phase.
> 3. Task IDs use format: `DEV-###` — increment from DEV-001 upward across ALL sprints.
> 4. At sprint end, always write a 3-line retrospective before starting the next sprint.

---

## 🏃 SPRINT 0: SETUP SPRINT
> **Goal:** Dev environment is fully running. First build is deployed. Database is live.
> **Duration:** [YYYY-MM-DD] → [YYYY-MM-DD]

### Sprint 0 Retrospective *(Fill in at sprint end)*
- ✅ **What went well:** [1–2 sentences]
- ⚠️ **What was hard:** [1–2 sentences]
- 💡 **What I'll do differently in Sprint 1:** [1 sentence]

### Sprint 0 — Task Summary

| Task ID | Task Title | Status | Priority | Effort | Executor |
|:---:|---|:---:|---|:---:|:---:|
| DEV-001 | Scaffold project with chosen tech stack | ⬜ To Do | 🔴 Must Have · High | S | 🔀 Hybrid |
| DEV-002 | Set up local development environment | ⬜ To Do | 🔴 Must Have · High | S | 👤 Human |
| DEV-003 | Set up CI/CD pipeline (auto-test + auto-deploy) | ⬜ To Do | 🟡 Should Have · High | M | 🔀 Hybrid |
| DEV-004 | Deploy "Hello World" to production | ⬜ To Do | 🔴 Must Have · High | S | 🔀 Hybrid |
| DEV-005 | Set up database & run first migration | ⬜ To Do | 🔴 Must Have · High | S | 🔀 Hybrid |

### Sprint 0 — Task Detail Cards

---

### DEV-001: Scaffold Project with Chosen Tech Stack

| Field | Details |
|---|---|
| **📍 Phase** | Phase 2: Development — Sprint 0 |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | S — ~2–4 hours |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | Sprint 0 |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-005, PLAN-007, PLAN-008 |
| **⛓️ Blocks** | DEV-002, DEV-003 |

**📝 Description**
> Use the tech stack from PLAN-005 to create the initial project scaffold.
> Install all core dependencies, configure TypeScript/linting/formatting, and
> verify the project runs locally without errors.

**🎯 Acceptance Criteria**
- [ ] Project scaffolded using the chosen framework's official CLI tool
- [ ] All core dependencies installed with no critical security vulnerabilities
- [ ] Project runs locally without errors (e.g., `npm run dev` works)
- [ ] TypeScript / linting / formatting configured and working
- [ ] Environment variables load from `.env.local`
- [ ] Folder structure matches PLAN-007
- [ ] Code committed to the repository main branch

**🤖 Claude Prompt / AI Instructions**
```
Help me scaffold and configure a new [tech stack] project from scratch.

Project: [name]
Tech stack: [from PLAN-005]
Integrations needed from day one: [e.g., Supabase, Stripe, Claude API, Tailwind CSS]
My CLAUDE.md for context: [paste the content of CLAUDE.md from PLAN-008]

Please provide:
1. The exact terminal commands to scaffold the project (step-by-step)
2. All npm/pip packages to install, with a one-line explanation of what each does
3. TypeScript configuration (tsconfig.json) if using TypeScript
4. Linting + formatting configuration (ESLint + Prettier or equivalent)
5. The initial app entry point (e.g., app/page.tsx for Next.js)
6. How to verify everything is working correctly after setup
```

**📎 AI Output / Notes**
> - **Commands Run:** [list key terminal commands used]
> - **Major Packages:** [list: Next.js, Tailwind, Supabase, etc.]
> - **Working Locally:** ✅ Yes / ❌ No (if No: describe the issue)

---

### DEV-004: Deploy "Hello World" to Production

| Field | Details |
|---|---|
| **📍 Phase** | Phase 2: Development — Sprint 0 |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | S — ~2–4 hours |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | Sprint 0 |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | DEV-001, DEV-003 |
| **⛓️ Blocks** | DEV-005, all Sprint 1 tasks |

**📝 Description**
> Get a live, accessible URL on the internet — even if it just shows a landing page or "Coming Soon."
> This validates your entire deployment pipeline works before building real features.
> **Rule:** Deploy early and often. Every sprint should produce something deployable.

**🎯 Acceptance Criteria**
- [ ] Production URL is live and accessible from any browser / device
- [ ] App displays something visible (placeholder page is fine)
- [ ] HTTPS / SSL is working (green padlock shows in browser)
- [ ] No critical errors appear in the hosting platform's log dashboard
- [ ] Automatic deployment triggers when code is pushed to `main`
- [ ] Custom domain is configured (or noted as "to be added later")
- [ ] Production URL is added to the Project Overview table at the top

**🤖 Claude Prompt / AI Instructions**
```
Help me deploy my [tech stack] project to [hosting platform] for the first time.

Project: [name — brief description]
Hosting platform: [Vercel / Railway / Expo EAS / AWS Amplify / etc.]
Repository: [GitHub URL from PLAN-007]

Please walk me through:
1. Exact steps to connect my GitHub repo to [hosting platform]
2. Environment variables to set in the production dashboard (with descriptions)
3. Custom domain setup (if applicable)
4. How to verify the deployment succeeded
5. How to check production logs when something goes wrong
6. How automatic deploys work (when does production update?)
```

**📎 AI Output / Notes**
> - **Production URL:** [your live URL — add here AND in Project Overview]
> - **Deployment Date:** [YYYY-MM-DD]
> - **Auto-deploy Working:** ✅ Yes / ❌ No
> - **Custom Domain:** [domain / "Not yet configured"]

---

### DEV-005: Set Up Database & Run First Migration

| Field | Details |
|---|---|
| **📍 Phase** | Phase 2: Development — Sprint 0 |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | S — ~2–4 hours |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | Sprint 0 |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | PLAN-006, DEV-001 |
| **⛓️ Blocks** | All feature development tasks |

**📝 Description**
> Create the database in your cloud provider, apply the schema from PLAN-006,
> and confirm the application can read and write data successfully.
> Without a working database, no features can be built or tested.

**🎯 Acceptance Criteria**
- [ ] Database instance created in cloud provider
- [ ] Schema from PLAN-006 applied — all tables exist in the database
- [ ] Application connects to database without connection errors
- [ ] A test record can be written to the database and read back correctly
- [ ] Database connection string is stored in environment variables (never hardcoded in code)
- [ ] Seed data script runs successfully (creates test data for local development)
- [ ] Database backup / point-in-time recovery is enabled or noted as needed

**🤖 Claude Prompt / AI Instructions**
```
Help me set up and initialize my database for the first time.

Database: [Supabase PostgreSQL / PlanetScale / MongoDB Atlas / etc.]
ORM or client: [Prisma / Drizzle / Supabase client / etc.]
Schema from PLAN-006: [paste your schema here]

Please provide:
1. Step-by-step instructions to create the database instance in [platform]
2. The migration file(s) to create all tables from my schema
3. The exact commands to run the migration
4. A simple test script to verify: insert a test row, read it back, delete it
5. A seed script to populate development data for local testing
6. How to reset the database and re-run migrations during development
7. How to make the database URL available as an environment variable safely
```

**📎 AI Output / Notes**
> - **Database Platform:** [Supabase / PlanetScale / etc.]
> - **Migration Status:** ✅ Run / ❌ Not run
> - **Tables Created:** [list: users, projects, tasks...]
> - **Seed Script:** ✅ Working / ❌ Not yet / N/A

---

## 📐 SPRINT TEMPLATE — Copy This for Every New Sprint

> 📝 **HOW TO USE:** Copy everything between the two dashed lines below.
> Paste it at the bottom of Phase 2. Replace all `[N]` with your sprint number.
> Fill in the Goal before the sprint starts. Fill in the Retrospective at sprint end.

---

## 🏃 SPRINT [N]: [SPRINT THEME — e.g., "User Auth + Onboarding"]

> **Goal:** [One sentence — what does a user gain by the end of this sprint?]
> **Duration:** [YYYY-MM-DD] → [YYYY-MM-DD]

### Sprint [N] Retrospective *(Fill in at sprint end — takes 5 minutes)*
- ✅ **What went well:** [1–2 sentences]
- ⚠️ **What was hard:** [1–2 sentences]
- 🔁 **Tasks carrying over to next sprint:** [list task IDs, or "None"]
- 💡 **What I'll do differently next sprint:** [1 sentence]

### Sprint [N] — Task Summary

| Task ID | Task Title | Status | Priority | Effort | Executor |
|:---:|---|:---:|---|:---:|:---:|
| DEV-[###] | [Task title — start with a verb] | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |
| DEV-[###] | [Task title] | ⬜ To Do | 🟡 Should Have · High | S | 🤖 AI |

### Sprint [N] — Task Detail Cards

---

### DEV-[###]: [Task Title — Start With a Verb]

| Field | Details |
|---|---|
| **📍 Phase** | Phase 2: Development — Sprint [N] |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | [🔴 Must Have · High / 🟡 Should Have · High / etc.] |
| **⏱️ Effort** | [XS / S / M / L] — ~[estimated hours] |
| **🤖 Executor** | [🤖 AI / 👤 Human / 🔀 Hybrid] |
| **🏃 Sprint** | Sprint [N] |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | [Task ID — or "None"] |
| **⛓️ Blocks** | [Task ID — or "None"] |

**📝 Description**
> [What needs to be built and why it matters to the user — 1–3 specific sentences.
> Avoid vague words like "improve," "fix," or "handle." Be concrete.]

**🎯 Acceptance Criteria**
- [ ] [Specific, testable criterion — any person can verify this is true]
- [ ] [Specific, testable criterion]
- [ ] [Specific, testable criterion]
- [ ] [Add more as needed]

**🤖 Claude Prompt / AI Instructions**
```
[Paste the exact Claude prompt you used or plan to use for this task.
Start with context: "You are a [role]. My project is [description]. My CLAUDE.md is at [location]."
Then describe exactly what you need Claude to build or produce.
If this task was done manually with no AI help, write: "👤 Completed manually — no AI prompt."]
```

**📎 AI Output / Notes**
> - [Add output links, file paths, key decisions, or observations AFTER the task is completed]
> - [If Claude produced code: note the file it was written to]
> - [If a decision was made during this task: document it here]

---

*(End of Sprint Template — copy everything above this line for each new sprint)*

---
---

# 🧪 PHASE 3: QA / TESTING → BETA LAUNCH

> **🎯 Phase Goal:** Find and fix all critical bugs, then launch to real users for the first time.
> **📍 When Is Phase 3 Done?** Zero critical bugs AND at least 5 beta users have actively used the product.
> **⏱️ Expected Duration:** 2–4 weeks.
> **🤖 Who Does This:** Mostly 🔀 Hybrid + 👤 Human (Claude helps write test cases and fix bugs).

---

## 📋 Phase 3 — Task Summary Table

| Task ID | Task Title | Status | Priority | Effort | Executor |
|:---:|---|:---:|---|:---:|:---:|
| QA-001 | Write test plan & define test cases for all features | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |
| QA-002 | Set up automated tests (unit + integration) | ⬜ To Do | 🟡 Should Have · High | L | 🔀 Hybrid |
| QA-003 | Manual end-to-end testing of all user flows | ⬜ To Do | 🔴 Must Have · High | M | 👤 Human |
| QA-004 | Security & performance review | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |
| QA-005 | Fix all Critical and High severity bugs | ⬜ To Do | 🔴 Must Have · High | L | 🔀 Hybrid |
| QA-006 | Set up beta feedback system | ⬜ To Do | 🟠 Must Have · Medium | S | 🔀 Hybrid |
| QA-007 | Recruit 5–20 beta users | ⬜ To Do | 🔴 Must Have · High | M | 👤 Human |
| QA-008 | Onboard beta users & collect structured feedback | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |

---

## 🗂️ Phase 3 — Task Detail Cards

---

### QA-001: Write Test Plan & Define Test Cases

| Field | Details |
|---|---|
| **📍 Phase** | Phase 3: QA / Testing |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | M — ~4–8 hours |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | QA Sprint |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | All Phase 2 Must Have tasks ✅ Done |
| **⛓️ Blocks** | QA-002, QA-003 |

**📝 Description**
> Before testing, you need a plan. Define exactly what will be tested, how it will be tested,
> and what "pass" vs "fail" looks like for each scenario.
> Testing without a plan means you'll miss important cases — especially edge cases.

**🎯 Acceptance Criteria**
- [ ] Test plan document created with scope, approach, and timeline
- [ ] Every Must Have feature has at least 3 test cases defined
- [ ] Happy path tests defined (what happens when users do everything correctly)
- [ ] Edge case tests defined (unusual but valid inputs: empty fields, very long text, special characters)
- [ ] Error case tests defined (what happens when things fail: network errors, invalid data, timeouts)
- [ ] Test priority list created (most critical features tested first)
- [ ] Test environment configured (separate from production — never test on production data)

**🤖 Claude Prompt / AI Instructions**
```
You are a senior QA engineer. Write a comprehensive test plan for my product.

My product: [name and description]
Must Have features from PLAN-004: [list features]
Tech stack: [from PLAN-005]
User flows to test: signup, [core feature], [payment if applicable], logout

For each feature, please create:
1. Happy Path Test Case: user does everything correctly — what should happen?
2. Edge Case Tests: unusual but valid inputs — what should happen?
3. Error Case Tests: things go wrong — what should the user experience?
4. Pass/Fail criteria: how do I know if the test passed or failed?

Also provide:
- A prioritized list: which tests to run first (most business-critical first)
- A security testing checklist for a web + mobile app
- Performance benchmarks to check (page load time, API response time)
- Accessibility checklist (keyboard navigation, screen reader basics, color contrast)
```

**📎 AI Output / Notes**
> - **Test Plan Document:** [link]
> - **Total Test Cases:** [number]
> - **Test Environment URL:** [separate staging URL, not production]

---

### QA-004: Security & Performance Review

| Field | Details |
|---|---|
| **📍 Phase** | Phase 3: QA / Testing |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | M — ~4–8 hours |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | QA Sprint |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | QA-003 |
| **⛓️ Blocks** | QA-005 |

**📝 Description**
> Review the product for security vulnerabilities and performance issues before exposing
> it to real users. No product should go live with known security holes.
> Users trust you with their data — take that seriously before launch.

**🎯 Acceptance Criteria**
- [ ] No API keys or secrets exposed in client-side code or public repository
- [ ] All user-submitted data is validated and sanitized before use
- [ ] Authentication tokens expire appropriately and refresh correctly
- [ ] Common vulnerabilities checked: SQL injection, XSS, CSRF, broken auth
- [ ] Web: Lighthouse performance score > 80 / Mobile: app starts in < 3 seconds
- [ ] All API error messages don't expose sensitive system information
- [ ] Rate limiting is in place for sensitive endpoints (login, signup, API calls)
- [ ] Environment variables confirmed — none leaked to the frontend

**🤖 Claude Prompt / AI Instructions**
```
You are a security engineer. Review my [tech stack] product for security and performance issues.

Key areas to review:
- User authentication and session management
- User-submitted data handling (form inputs, file uploads)
- API endpoint authorization
- Database query construction
- Environment variables and secret management
- Frontend bundle (any secrets accidentally included?)

Please provide:
1. Security audit checklist for a [web app / mobile app] built with [tech stack]
2. OWASP Top 10 vulnerabilities mapped to my specific stack — which ones apply?
3. A code review of these specific files/functions I'm concerned about:
   [paste the code snippets here]
4. Performance checklist: what to check before going live
5. Free tools to run automated security scans on my app
6. For each issue found: severity (Critical/High/Medium/Low) and exact fix
```

**📎 AI Output / Notes**
> - **Critical Issues Found & Fixed:** [number]
> - **High Issues Found & Fixed:** [number]
> - **Performance Score:** [Lighthouse score / app startup time]
> - **Security Review Complete:** ✅ Yes / ❌ No

---

### QA-007: Recruit 5–20 Beta Users

| Field | Details |
|---|---|
| **📍 Phase** | Phase 3: Beta Launch |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | M — ~4–8 hours |
| **🤖 Executor** | 👤 Human (Claude helps write outreach copy) |
| **🏃 Sprint** | QA Sprint |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | QA-005 (all critical bugs fixed) |
| **⛓️ Blocks** | QA-008 |

**📝 Description**
> Find real people who match your user personas and invite them to try the product.
> Beta users give you the real-world feedback that internal testing can never surface.
> Quality beats quantity — 5 deeply engaged beta users are worth more than 50 passive sign-ups.

**🎯 Acceptance Criteria**
- [ ] Ideal beta user profile defined (must match at least one of your user personas)
- [ ] At least 5 beta users confirmed, onboarded, and actively using the product
- [ ] Beta user expectations set: "this is a beta — bugs are possible, your feedback shapes the product"
- [ ] A feedback channel is set up (Slack/Discord invite, or dedicated email thread)
- [ ] A structured feedback form is ready (5–10 questions max — short enough to actually fill)
- [ ] A schedule for 1:1 calls with beta users is set (even 15-minute calls are gold)

**🤖 Claude Prompt / AI Instructions**
```
Help me recruit beta users for my product.

My product: [name and one-sentence description]
Target users: [paste persona descriptions from PLAN-002]
What beta users get: [free access / exclusive early pricing / direct founder access / etc.]
What I'm asking from beta users: [fill a feedback form / 15-min call / use it for 2 weeks]
Where my target users hang out: [e.g., specific subreddits, LinkedIn groups, Twitter communities]

Please write:
1. A personal beta invitation email — short, warm, one clear ask
2. A Twitter/X post announcing the beta — conversational, not salesy
3. A LinkedIn post — slightly more professional tone
4. A Reddit post for [relevant subreddit] — community-first, not promotional
5. A beta feedback survey with 8 questions (mix of scale ratings and open text)
6. A 3-email beta onboarding sequence:
   - Email 1: Welcome + how to get started
   - Email 2 (Day 3): Tips + key features to try
   - Email 3 (Day 7): Feedback request + thank you
```

**📎 AI Output / Notes**
> - **Beta Users Recruited:** [number]
> - **Beta Period:** [YYYY-MM-DD] → [YYYY-MM-DD]
> - **Channels Used:** [e.g., Twitter DMs, Reddit, LinkedIn, personal network]
> - **Beta Feedback Summary:** [fill in AFTER beta ends — key themes and top 3 insights]

---

## 🐛 BUG TRACKER

> 📝 **HOW TO FILL:** Log every bug here as soon as it's found.
> Update Status as bugs are fixed. Never delete a bug row — mark it ✅ Fixed.
>
> **Severity Guide:**
> 🔴 **Critical** — Product is broken / data is lost / security issue (fix TODAY)
> 🟠 **High** — A major feature doesn't work correctly (fix this sprint)
> 🟡 **Medium** — Feature works but the experience is poor (fix before launch)
> 🟢 **Low** — Cosmetic issue or minor annoyance (fix when time allows)

| Bug ID | Description | Severity | Status | Found By | Sprint Found | Fixed In Task | Steps to Reproduce |
|:---:|---|:---:|:---:|---|:---:|:---:|---|
| BUG-001 | [Brief description — what's broken and what was expected] | 🔴 Critical | ⬜ Open | [Tester / Beta User / You] | [Sprint #] | [DEV-###] | [1. Go to X. 2. Click Y. 3. See Z error] |
| BUG-002 | [Description] | 🟠 High | ⬜ Open | | | | |

> ➕ Add a new row for every bug found. Keep all rows — closed bugs are history.

---
---

# 🚀 PHASE 4: LAUNCH → FIRST 500 CUSTOMERS

> **🎯 Phase Goal:** Ship to the world, grow to 500 active customers, and establish a repeatable growth engine.
> **📍 When Is Phase 4 Done?** 500 customers are using the product and have been active for at least 30 days.
> **⏱️ Expected Duration:** 4–16 weeks (ongoing growth work).
> **🤖 Who Does This:** 👤 Human-led (Claude assists with content, copy, analysis, and automation).

---

## 📋 Phase 4 — Task Summary Table

| Task ID | Task Title | Status | Priority | Effort | Executor |
|:---:|---|:---:|---|:---:|:---:|
| GTM-001 | Build public landing page | ⬜ To Do | 🔴 Must Have · High | L | 🔀 Hybrid |
| GTM-002 | Set up payment processing (Stripe or equivalent) | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |
| GTM-003 | Install product analytics & error tracking | ⬜ To Do | 🔴 Must Have · High | S | 🔀 Hybrid |
| GTM-004 | Build user onboarding flow | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |
| GTM-005 | Set up customer support system | ⬜ To Do | 🟡 Should Have · High | S | 🔀 Hybrid |
| GTM-006 | Write launch announcement content for all channels | ⬜ To Do | 🔴 Must Have · High | M | 🔀 Hybrid |
| GTM-007 | Execute public launch | ⬜ To Do | 🔴 Must Have · High | L | 👤 Human |
| GTM-008 | Set up email marketing & retention sequences | ⬜ To Do | 🟡 Should Have · High | M | 🔀 Hybrid |
| GTM-009 | Weekly KPI review & growth iteration (recurring) | ⬜ To Do | 🔴 Must Have · High | S | 🔀 Hybrid |
| GTM-010 | 500 Customers retrospective & v2 planning | ⬜ To Do | 🟡 Should Have · High | M | 🔀 Hybrid |

---

## 🗂️ Phase 4 — Task Detail Cards

---

### GTM-001: Build Public Landing Page

| Field | Details |
|---|---|
| **📍 Phase** | Phase 4: Launch |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | L — ~1–3 days |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | Launch Sprint |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | QA-005 (critical bugs fixed), QA-008 (beta feedback collected) |
| **⛓️ Blocks** | GTM-006, GTM-007 |

**📝 Description**
> Build the public-facing page that sells the product to visitors 24/7.
> It should clearly communicate: what the product does, who it's for, and why they should sign up now.
> Your landing page is your most important sales tool — it works while you sleep.

**🎯 Acceptance Criteria**
- [ ] Hero: clear headline (under 8 words) + subheadline + one prominent CTA button
- [ ] Problem / Solution section: shows the pain and how the product solves it
- [ ] Features section: 3–5 key features with icons, titles, and 2-sentence descriptions
- [ ] Social proof: at least 3 testimonials or beta user quotes (with permission)
- [ ] Pricing section: clear plans, what's included, and a free trial or freemium option
- [ ] FAQ section: answers the top 5 questions a first-time visitor would have
- [ ] Footer: Privacy Policy link, Terms of Service link, contact email
- [ ] Page loads in < 3 seconds on a standard connection
- [ ] Fully responsive — looks correct on mobile phone and desktop
- [ ] Analytics tracking is installed and firing (see GTM-003)
- [ ] Signup CTA creates an account in the database

**🤖 Claude Prompt / AI Instructions**
```
You are a conversion copywriter. Write the landing page copy for my product.

Product: [name]
Problem it solves: [from PLAN-001]
Target user: [Persona 1 from PLAN-002]
Must Have features: [from PLAN-004]
Key differentiator: [why this beats alternatives]
Pricing: [your pricing tiers]
Beta user feedback quotes: [paste 3-5 real quotes from QA-008 — with permission]

Please write the complete landing page copy:
1. Hero Section: Headline (≤8 words) + Subheadline (≤25 words) + CTA button text
2. Problem Section: 2 short paragraphs — describe the pain before your product
3. Solution Section: 3 key features (icon description, title, 2-sentence explanation each)
4. Social Proof: 3 testimonials in the voice of real users from [persona backgrounds]
5. Pricing Section: for each plan — name, price, 5 bullet-point features, CTA text
6. FAQ: 5 questions + answers (address the real objections buyers have)
7. Final CTA Section: closing headline + button text

Tone: [e.g., friendly and confident / calm and professional / bold and disruptive]
```

**📎 AI Output / Notes**
> - **Landing Page URL:** [link]
> - **Conversion Rate (this week):** [signups ÷ visitors — update weekly]
> - **Top-performing CTA text:** [which button text gets most clicks]

---

### GTM-002: Set Up Payment Processing

| Field | Details |
|---|---|
| **📍 Phase** | Phase 4: Launch |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | M — ~4–8 hours |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | Launch Sprint |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | DEV-001 |
| **⛓️ Blocks** | GTM-007 |

**📝 Description**
> Integrate a payment provider so customers can subscribe or make one-time purchases.
> Test every payment scenario thoroughly with test cards before going live.
> A broken payment flow is the fastest way to lose a customer forever.

**🎯 Acceptance Criteria**
- [ ] Payment provider chosen and account created (Stripe recommended for SaaS)
- [ ] Subscription plans / price IDs created in the payment provider dashboard
- [ ] Checkout flow integrated — user can complete payment without leaving the app
- [ ] Webhook handler set up for key events: `checkout.session.completed`, `customer.subscription.deleted`, `invoice.payment_failed`
- [ ] Test payment succeeds with provider's test card numbers
- [ ] Failed payment handled gracefully — user sees a clear error message, not a crash
- [ ] Subscription status is synced to user's account in the database after payment
- [ ] Customer billing portal works — user can update card, view invoices, cancel subscription
- [ ] Tested with a real $1 charge to your own account before announcing live

**🤖 Claude Prompt / AI Instructions**
```
Help me integrate [Stripe / Paddle / LemonSqueezy] into my [tech stack] application.

Subscription plans:
- Plan 1: [name, price, billing period (monthly/annual), what features it includes]
- Plan 2: [name, price, billing period, features]

Please provide:
1. Step-by-step Stripe setup guide for [tech stack]
2. Server-side checkout session creation code
3. Webhook handler for: checkout.session.completed, customer.subscription.deleted, invoice.payment_failed
4. Database update logic when subscription status changes
5. How to check a user's subscription status before showing premium features
6. Customer billing portal integration (so users can self-manage their subscription)
7. Test card numbers for: successful payment, declined card, 3D Secure flow
8. Checklist before switching from test mode to live mode
```

**📎 AI Output / Notes**
> - **Payment Provider:** [Stripe / Paddle / LemonSqueezy]
> - **Test Payment Confirmed:** ✅ Yes / ❌ No
> - **Live $1 Test Confirmed:** ✅ Yes / ❌ No (do this before launch!)
> - **Webhook Endpoint URL:** [your endpoint — saved in .env, not here]

---

### GTM-004: Build User Onboarding Flow

| Field | Details |
|---|---|
| **📍 Phase** | Phase 4: Launch |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | M — ~4–8 hours |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | Launch Sprint |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | All core feature DEV tasks complete |
| **⛓️ Blocks** | GTM-007 |

**📝 Description**
> Design and build the experience that takes a new user from "just signed up"
> to "I understand this product and I just got my first piece of value from it."
> Great onboarding is the single biggest lever for early retention.
> The "aha moment" — when a user first feels the product's value — must happen within minutes.

**🎯 Acceptance Criteria**
- [ ] Welcome email sent automatically within 60 seconds of signup
- [ ] In-app onboarding checklist or guided tour implemented (3–5 steps maximum)
- [ ] New user reaches their first "aha moment" within 5 minutes of signup (test this yourself!)
- [ ] Empty state screens are friendly and actionable (new users see a guide, not a blank page)
- [ ] Onboarding completion rate is tracked in analytics (from GTM-003)
- [ ] Day 3 follow-up email sent automatically if user hasn't completed key onboarding actions
- [ ] Onboarding flow tested by at least 2 people who have never seen the product before

**🤖 Claude Prompt / AI Instructions**
```
You are a product growth expert. Design the complete onboarding experience for my product.

Product: [name — what it does]
Primary persona: [from PLAN-002]
The "aha moment" — when a user first feels the value — happens when: [describe it]
Email provider: [Resend / SendGrid / Postmark / etc.]

Please design:
1. Onboarding checklist: 3–5 steps that lead directly to the aha moment
2. Welcome email: subject line + body (personal, warm, one clear next step)
3. Day 3 email: gentle nudge if key action hasn't happened yet
4. Day 7 email: check-in, tips, and a feedback ask
5. Empty state copy for the main dashboard (what do new users see before adding any data?)
6. In-app tooltip copy for the 3 most important UI elements
7. The exact sequence of clicks a user should make in their first 5 minutes

For all copy: match the tone [e.g., friendly and encouraging / professional and confident].
```

**📎 AI Output / Notes**
> - **Onboarding Completion Rate:** [track from analytics — update weekly]
> - **Avg. Time to "Aha Moment":** [measure from analytics]
> - **Day 3 Email Open Rate:** [track from email provider]

---

### GTM-007: Execute Public Launch

| Field | Details |
|---|---|
| **📍 Phase** | Phase 4: Launch |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | L — ~1–3 days |
| **🤖 Executor** | 👤 Human (Claude prepares all content beforehand) |
| **🏃 Sprint** | Launch Sprint |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | GTM-001, GTM-002, GTM-003, GTM-004, QA-005 |
| **⛓️ Blocks** | GTM-008, GTM-009 |

**📝 Description**
> The big day. Go live and tell the world. This is a coordinated effort — you publish the
> landing page, post across all channels, send launch emails, and monitor closely
> for the first 48 hours. Be present and responsive. This day only happens once.

**🎯 Acceptance Criteria**
- [ ] Pre-launch checklist confirmed complete (all above GTM tasks ✅ Done)
- [ ] Product publicly accessible — new users can sign up without an invite code
- [ ] Launch posts published on all planned channels (list below)
- [ ] ProductHunt submission is live (if applicable)
- [ ] Launch announcement email sent to beta users and any waitlist
- [ ] Monitoring active for the first 48 hours: new signups, errors, support requests
- [ ] All critical bugs reported post-launch addressed within 24 hours
- [ ] Day 1 and Week 1 metrics recorded in the Customer Milestone Tracker

**🤖 Claude Prompt / AI Instructions**
```
Help me write all the content I need for my product launch day.

Product: [name and one-sentence description]
Target users: [from personas]
Key differentiator: [what makes this unique]
Pricing: [your plans and a free trial detail]
Beta user quotes: [paste 2-3 real feedback quotes from QA-008]
Launch channels: [list where you'll post: Twitter/X, LinkedIn, Reddit, ProductHunt, HackerNews, etc.]

Please write:
1. ProductHunt tagline (under 60 characters)
2. ProductHunt short description (under 260 characters)
3. Twitter/X launch thread: hook tweet + 5 thread tweets + closing CTA tweet
4. LinkedIn post (professional tone, slightly longer, story-first)
5. Reddit post for [r/specific subreddit]: community-first, genuinely helpful, not promotional
6. Hacker News "Show HN" post: honest, technical context, invites real feedback
7. Launch email to beta users and waitlist: personal tone, celebrate them first
8. Response templates for: positive comments, feature requests, bug reports, negative feedback
9. Launch day monitoring checklist: what to check every 2 hours on launch day
```

**📎 AI Output / Notes**
> - **Launch Date:** [YYYY-MM-DD]
> - **Channels Posted To:** [list]
> - **Day 1 Signups:** [number]
> - **Week 1 Signups:** [number]
> - **ProductHunt Rank:** [if applicable]
> - **Most Surprising Reaction:** [write it down — you'll want to remember this]

---

### GTM-009: Weekly KPI Review & Growth Iteration (Recurring)

| Field | Details |
|---|---|
| **📍 Phase** | Phase 4: Growth → 500 Customers |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | 🔴 Must Have · High |
| **⏱️ Effort** | XS — ~1 hour per week |
| **🤖 Executor** | 🔀 Hybrid |
| **🏃 Sprint** | Recurring — every Friday |
| **📅 Due Date** | Every Friday (recurring) |
| **🔗 Depends On** | GTM-003, GTM-007 |
| **⛓️ Blocks** | Nothing — this informs all future tasks |

**📝 Description**
> Every week, review the key product metrics to understand what's growing, where users drop off,
> and what to prioritize next. This is how you go from launch day to 500 customers.
> Data without action is just numbers. Action without data is just guessing.

**🎯 Acceptance Criteria**
- [ ] Weekly KPI review completed every Friday (block 60 minutes — don't skip)
- [ ] All metrics logged in the Customer Milestone Tracker below
- [ ] Top 1–3 priorities for next week decided based on the data, not on gut feel
- [ ] Any metric that dropped more than 20% week-over-week is investigated before next sprint

**🤖 Claude Prompt / AI Instructions**
```
Help me analyze my weekly product metrics and identify the highest-leverage action for next week.

This week's numbers:
- New signups: [number]
- Active users (used the product at least once): [number]
- Paying customers (total): [number]
- New paying customers (this week): [number]
- Churned customers (cancelled this week): [number]
- MRR (Monthly Recurring Revenue): $[amount]
- Top 3 features used this week: [list them]
- Top 3 support issues / complaints this week: [list them]
- NPS or satisfaction score: [number / "not yet measured"]
- Onboarding completion rate: [%]

User feedback themes from this week:
[paste any notable feedback quotes or themes here]

Please:
1. What's going well? What's at risk? (brief honest assessment)
2. What is the single biggest lever I can pull to move toward 500 customers?
3. Suggest 3 specific tasks for next week, ordered by expected impact
4. Flag any metric that needs immediate investigation
5. Should I focus on acquisition (getting new users) or retention (keeping existing users) right now?
```

**📎 AI Output / Notes**
> - **Log metrics in the Milestone Tracker below every week ↓**

---

## 📊 CUSTOMER MILESTONE TRACKER

> 📝 **HOW TO FILL:** Update this table every Friday after your GTM-009 KPI review.
> Be honest with the numbers — a correct tracker tells the truth. Update "Key Win" and "Key Issue" weekly.

| Week | Total Signups | Active Users | Paying Customers | MRR | Churned | Key Win This Week | Key Issue This Week |
|:---:|:---:|:---:|:---:|:---:|:---:|---|---|
| 🚀 Launch Week | — | — | — | $0 | — | | |
| Week 1 | 0 | 0 | 0 | $0 | 0 | | |
| Week 2 | | | | | | | |
| Week 3 | | | | | | | |
| Week 4 | | | | | | | |
| Week 5 | | | | | | | |
| Week 6 | | | | | | | |
| Week 7 | | | | | | | |
| Week 8 | | | | | | | |
| Week 9 | | | | | | | |
| Week 10 | | | | | | | |
| Week 11 | | | | | | | |
| Week 12 | | | | | | | |
| **🎯 Goal** | | | **500** | | | | |

> ➕ Add more rows as weeks pass. Keep this table going until you hit 500 customers.

---

## 🎉 500 CUSTOMERS — CLOSING CHECKLIST

> You made it. 500 real customers use your product. Here's what to do next.

- [ ] **Document what worked:** Write a 1-page summary of your top 3 growth strategies that actually moved the number
- [ ] **Identify your best customers:** Who are your top 10% most engaged users? What do they share in common?
- [ ] **Capture case studies:** Reach out to 3–5 power users for a testimonial or a short case study
- [ ] **Analyze churn:** Who left, when, and why? What pattern do you see?
- [ ] **Plan v2:** What features do your best customers want most? Add them to a new Phase 2 sprint
- [ ] **Improve the prompt library:** Review the Claude prompts in this backlog — which produced the best results? Save them
- [ ] **Archive this backlog:** Save a timestamped copy of this file as `Task_Backlog_v1_Complete.md`
- [ ] **Celebrate!** 🥳 You had an idea. You planned it. You built it. You shipped it. Real people pay for it. That is genuinely hard, and you did it.

---
---

# 📎 APPENDIX

---

## A. BLANK TASK TEMPLATE — Copy This for Every New Task

> 📝 **HOW TO USE:** Copy everything between `COPY START` and `COPY END`.
> Paste it where you need a new task. Fill in every field before starting work.
> Tip: Fill the Summary Table row first. Fill the Detail Card when the sprint begins.

<!--- COPY START --->

### [PHASE]-[###]: [Task Title — Start With a Verb, Be Specific]

| Field | Details |
|---|---|
| **📍 Phase** | [Phase 1 / Phase 2 / Phase 3 / Phase 4] |
| **🔖 Status** | ⬜ To Do |
| **⚡ Priority** | [🔴 Must Have · High / 🟠 Must Have · Medium / 🟡 Should Have · High / 🟢 Could Have · Low / ⚫ Won't Have (This Version)] |
| **⏱️ Effort** | [XS / S / M / L] — ~[X] hours |
| **🤖 Executor** | [🤖 AI / 👤 Human / 🔀 Hybrid] |
| **🏃 Sprint** | [Sprint 0 / Sprint 1 / Sprint N / QA Sprint / Launch Sprint] |
| **📅 Due Date** | [YYYY-MM-DD] |
| **🔗 Depends On** | [Task ID, Task ID — or "None"] |
| **⛓️ Blocks** | [Task ID, Task ID — or "None"] |

**📝 Description**
> [What needs to be done AND why it matters — 1–3 sentences. Be concrete and specific.
> Avoid vague words: "improve," "fix," "handle," "update." Say exactly what the output is.]

**🎯 Acceptance Criteria**
- [ ] [Specific, testable criterion — any person could verify this is true without asking you]
- [ ] [Specific, testable criterion]
- [ ] [Specific, testable criterion]
- [ ] [Add as many as needed — more is better than fewer]

**🤖 Claude Prompt / AI Instructions**
```
[Paste the exact Claude prompt you used or plan to use for this task here.
Always start with context: "You are a [role]. My project is [description]."
Then describe exactly what you need.
If done manually: write "👤 Completed manually — no AI prompt used."]
```

**📎 AI Output / Notes**
> - [Add output links, file paths, key decisions, or observations AFTER completing this task]
> - [Link to any files, documents, or PRs created by this task]

---

<!--- COPY END --->

---

## B. FREQUENTLY ASKED QUESTIONS

**Q: Do I have to fill every field in the task card?**
> The minimum required before you start a task: **Status**, **Priority**, **Description**, and at least **1 Acceptance Criterion**.
> A task with no acceptance criteria is unfinishable — there's no definition of "done."

**Q: What if my task doesn't fit neatly into one phase?**
> Put it in the phase where the work STARTS. If it spans multiple phases, put it in the earlier phase.

**Q: What do I do with a task that's bigger than 3 days?**
> Stop. Break it into 2–5 smaller tasks. An XL task almost always hides hidden complexity.
> If you can't break it down, you don't understand the task well enough yet — ask Claude to help you break it down.

**Q: Can I add new columns to the task summary tables?**
> Yes! Common additions: `GitHub Issue #`, `Tag` (Frontend / Backend / AI / Design), `Label`.
> Keep it consistent across all tables.

**Q: What's the difference between "Blocked" ⛔ and "Depends On"?**
> **Depends On** = a planned dependency you knew about before starting. Task B waits for Task A.
> **Blocked** = an unexpected obstacle discovered while working. Write the blocker reason in the Notes field.

**Q: I finished a task but I couldn't check 1 acceptance criterion. Can I mark it Done?**
> No. Either update the acceptance criterion to reflect the real outcome, or create a follow-up task
> for what's still outstanding. "Close enough" is not Done.

**Q: How much detail should be in the Claude Prompt section?**
> Paste the full prompt you actually used — even if it's long. Future-you will be grateful.
> A prompt that produced great code is worth documenting. If you only asked a quick question and didn't use the answer, skip it.

**Q: When should I move a task to "Won't Have (This Version)"?**
> When it's a valid idea but not needed for the current phase goal.
> Parking lot ideas here prevents scope creep while making sure nothing is forgotten.

---

## C. BACKLOG HEALTH CHECKLIST — Run Every Week

> 📝 **HOW TO USE:** Run this every Friday alongside your GTM-009 KPI review.
> It takes 5 minutes and keeps your backlog clean, honest, and useful.

- [ ] Every 🟡 In Progress task has been updated within the last 2 days
- [ ] No task has been "In Progress" for more than 2 sprints without an explanation
- [ ] All ⛔ Blocked tasks have the blocker written in the Notes field
- [ ] New ideas are added as ⚫ Won't Have tasks — not immediately put into the active sprint
- [ ] Every completed sprint has a Retrospective written (3 bullets minimum)
- [ ] The Customer Milestone Tracker is updated with this week's real numbers
- [ ] The Bug Tracker has no unacknowledged 🔴 Critical bugs
- [ ] The Project Overview table has accurate current phase and current sprint
- [ ] Any task in the sprint that won't finish on time has been flagged and discussed with yourself

---

## D. AI PROMPT LIBRARY — Best Prompts This Project

> 📝 **HOW TO USE:** When a Claude prompt produces an exceptional output — code, copy, analysis —
> save it here. This becomes your personal prompt library across 100s of projects.

| # | Task Type | Short Description | Where Full Prompt Lives |
|:---:|---|---|---|
| 1 | [e.g., PRD Writing] | [e.g., Generated complete PRD from 5 bullet points] | [PLAN-003 task card] |
| 2 | | | |
| 3 | | | |

---

## E. FUTURE FEATURES (Won't Have — Version 1)

> 📝 **HOW TO USE:** Any feature idea that's out of scope for v1 lives here — never deleted, just parked.
> Review this list when planning v2. The best v2 features almost always come from this list.

| Feature Idea | Why Parked | Target Version | Votes / Interest |
|---|---|:---:|:---:|
| [Feature idea] | [One sentence reason it's not in v1] | v2 | [# of users who requested it] |
| | | | |

---

## F. DOCUMENT CHANGELOG

> 📝 **HOW TO FILL:** Add a row every time you make a significant change to this document.
> Small status updates don't need a row. New tasks, scope changes, and template changes do.

| Date | Version | Change Description | Updated By |
|:---:|:---:|---|---|
| [YYYY-MM-DD] | v1.0 | Initial backlog created from template | [Your Name] |
| | | | |

---

*Template v1.0 · AI-Driven Development Lifecycle · Solo + Claude Edition*
*Compatible with: GitHub · GitLab · Notion · Obsidian · VS Code · Any Markdown Editor*
*Built using Claude (Anthropic) as co-architect 🤖*
