# Dependency Register
### `Dependency_Register.md` — AI-Driven Development Life Cycle
**Template Version:** 1.0 | **Last Updated:** _(fill in date)_ | **Project:** _(fill in project name)_

---

> **🧭 Navigation Quick-Links**
> - [📖 How to Fill This Document](#-how-to-fill-this-document)
> - [📋 Project & Register Info](#-project--register-info)
> - [📊 Health Dashboard](#-health-dashboard--at-a-glance-status)
> - [🔑 Field Reference Guide](#-field-reference-guide)
> - [📦 Phase 1 — Discovery & Scoping](#-phase-1--discovery--scoping)
> - [🔧 Phase 2 — Development & Integration](#-phase-2--development--integration)
> - [🧪 Phase 3 — QA, Testing & Security Review](#-phase-3--qa-testing--security-review)
> - [🚀 Phase 4 — Launch & Post-Launch (First 500 Users)](#-phase-4--launch--post-launch-first-500-users)
> - [🗺️ Dependency Map (Who Blocks Whom)](#️-dependency-map-who-blocks-whom)
> - [🤖 AI Prompt Helpers](#-ai-prompt-helpers)
> - [📝 Changelog](#-changelog)

---

## 📖 How to Fill This Document

### What Is This Document?

Imagine your project is like building a Lego castle. Some Lego pieces are in your hands right now. But some pieces are still being shipped from the factory, some are being painted by another team, and some need the manager's approval before you can even order them. A **Dependency Register** is simply your **list of all those missing pieces** — what they are, who is getting them, when they need to arrive, and what happens if they don't.

**This document tracks every single thing your project is waiting on from outside your team** — whether that's a tool, a data set, an AI model, a vendor contract, a legal sign-off, or a team handoff.

---

### Who Should Fill It?

| Role | Responsibility |
|---|---|
| **Product Manager / Project Lead** | Create the file, maintain the Dashboard, escalate blockers |
| **AI / ML Engineer** | Add AI model, dataset, and pipeline dependencies |
| **Software Developer** | Add technical library, API, and integration dependencies |
| **Designer / UX** | Add design tool, asset, and brand approval dependencies |
| **QA / Security Engineer** | Add testing tool and compliance dependencies |
| **Business / Legal / Finance** | Add approval, contract, and budget dependencies |
| **Anyone on the team** | If you spot something the team is waiting on — add a row! |

---

### Step-by-Step: How to Add a Dependency

Follow these 9 simple steps every time you add a new row to the register.

**Step 1 → Assign a Unique ID**
Each dependency gets a unique ID in the format `DEP-XXX` where `XXX` is a 3-digit number. Start at `DEP-001` and count up. Never reuse an ID, even if a dependency is cancelled.
> 🧒 *Think of it like a locker number at school. Each locker has one number, and that number never changes.*

**Step 2 → Write a Short, Clear Name**
Keep it under 6 words. Someone reading it for the first time should instantly know what it is.
> ✅ Good: `OpenAI GPT-4o API Key`
> ❌ Too vague: `API stuff`

**Step 3 → Pick the Type**
Choose one of the three types below. If it fits two, pick the most important one:
- 🔧 **Technical** — A software library, API, cloud service, or tool your code needs to run
- 🤖 **Data & AI Model** — A dataset, AI model version, embedding, or AI pipeline the product uses
- 📋 **Business / Compliance** — A contract, legal approval, licence, security review, or budget sign-off

**Step 4 → Write a Plain-English Description**
Explain what this dependency is and why the project needs it. Write it so a new team member reading it for the first time understands immediately. One or two sentences is perfect.

**Step 5 → Name an Owner**
The Owner is **one specific person** (not a team name) who is responsible for chasing and resolving this dependency. If you don't know yet, write `Unassigned` — but try to assign it within 24 hours.

**Step 6 → Set the Phase**
Which phase of the project does this dependency need to be resolved in? Pick from:
- `Phase 1` — Discovery & Scoping
- `Phase 2` — Development & Integration
- `Phase 3` — QA / Testing & Security
- `Phase 4` — Launch & Post-Launch

**Step 7 → Set Status**
Use one of these five statuses only. Be honest — it helps the team plan accurately.

| Status | Emoji | What it means |
|---|---|---|
| `Not Started` | ⚪ | We know about it but haven't begun chasing it yet |
| `In Progress` | 🔵 | Someone is actively working on getting or resolving this |
| `Resolved` | 🟢 | Done! The dependency is confirmed and available |
| `Blocked` | 🔴 | Something else is preventing this from moving forward |
| `Cancelled` | ⚫ | No longer needed (explain why in Notes) |

**Step 8 → Set Risk Level**
If this dependency is not resolved by the Due Date, how bad is it for the project?

| Risk | Emoji | What it means |
|---|---|---|
| `Low` | 🟡 | Inconvenient but we can work around it easily |
| `Medium` | 🟠 | Causes a delay of days or a week; needs attention soon |
| `High` | 🔴 | Stops us from shipping on time or causes a serious problem |

**Step 9 → Fill in Dates, Blocked By, and Workaround**
- **Due Date**: The latest date this dependency must be resolved. If you're unsure, estimate.
- **Blocked By**: If this dependency can't start because another dependency (`DEP-XXX`) isn't resolved yet, write that ID here. Otherwise write `—`.
- **Workaround Plan**: What will the team do if this dependency is NOT resolved by the Due Date? Even one sentence helps.

---

### ⚠️ Important Rules

1. **One row per dependency.** Don't bundle two separate things into one row.
2. **Update status every week.** Stale statuses are worse than no status.
3. **Never delete a row.** If a dependency is cancelled, change Status to `Cancelled` and explain in Notes.
4. **Own your dependencies.** If you are listed as Owner, you are responsible for providing weekly updates in the Notes column.
5. **Due Date ≠ Nice to Have.** If the Due Date passes with no resolution, escalate immediately.

---

## 📋 Project & Register Info

> **How to fill this section:** Complete every field before you add your first dependency row. This metadata makes the register usable across 100s of projects.

| Field | Your Answer |
|---|---|
| **Project Name** | _(e.g., "Nova AI — Customer Churn Predictor")_ |
| **Product Description** | _(One sentence: what does this product do and who is it for?)_ |
| **Project Start Date** | _(e.g., 2026-10-14)_ |
| **Target Launch Date** | _(e.g., 2027-03-01)_ |
| **First 500 Users Target Date** | _(e.g., 2027-04-30)_ |
| **Register Owner (Primary Maintainer)** | _(Full name + role, e.g., "Alice Chen — Product Manager")_ |
| **Register Created Date** | _(e.g., 2026-10-14)_ |
| **Last Reviewed Date** | _(Update every time you review this file)_ |
| **Review Cadence** | _(e.g., "Every Monday at 10 AM in sprint standup")_ |
| **AI Stack Summary** | _(e.g., "LLM: GPT-4o via OpenAI API · Vector DB: Pinecone · Orchestration: LangChain")_ |
| **Hosting / Infra** | _(e.g., "AWS us-east-1 · Vercel for frontend · Supabase for DB")_ |
| **Regulatory / Compliance Context** | _(e.g., "GDPR applicable — EU user data · SOC 2 Type II required by enterprise customers")_ |

---

## 📊 Health Dashboard — At-a-Glance Status

> **How to fill this section:** Update these numbers every time you review the register. It takes 2 minutes and gives everyone a project health snapshot in 5 seconds.

### Overall Counts

| Metric | Count |
|---|---|
| 📦 Total Dependencies Logged | _0_ |
| ⚪ Not Started | _0_ |
| 🔵 In Progress | _0_ |
| 🟢 Resolved | _0_ |
| 🔴 Blocked | _0_ |
| ⚫ Cancelled | _0_ |
| 🚨 Overdue (past Due Date, not Resolved) | _0_ |

### By Risk Level

| Risk | Count | IDs |
|---|---|---|
| 🔴 High | _0_ | _(e.g., DEP-003, DEP-007)_ |
| 🟠 Medium | _0_ | _(e.g., DEP-001)_ |
| 🟡 Low | _0_ | — |

### By Phase

| Phase | Total | Resolved | Open | Blocked |
|---|---|---|---|---|
| Phase 1 — Discovery & Scoping | _0_ | _0_ | _0_ | _0_ |
| Phase 2 — Development & Integration | _0_ | _0_ | _0_ | _0_ |
| Phase 3 — QA / Testing & Security | _0_ | _0_ | _0_ | _0_ |
| Phase 4 — Launch & Post-Launch | _0_ | _0_ | _0_ | _0_ |

### By Type

| Type | Count |
|---|---|
| 🔧 Technical | _0_ |
| 🤖 Data & AI Model | _0_ |
| 📋 Business / Compliance | _0_ |

### 🚨 Active Blockers (High-Risk / Unresolved)

> List any High-risk or Blocked dependencies here so they are impossible to miss.

| DEP-ID | Name | Owner | Due Date | Impact if Not Resolved |
|---|---|---|---|---|
| _(e.g., DEP-003)_ | _(e.g., OpenAI Enterprise Agreement)_ | _(e.g., Sarah — Legal)_ | _(e.g., 2026-11-01)_ | _(e.g., Cannot process user data without data processing agreement)_ |

---

## 🔑 Field Reference Guide

> Quick cheat-sheet. Paste this into your team onboarding doc so everyone fills columns consistently.

| Column Header | What to Write | Example |
|---|---|---|
| **DEP-ID** | `DEP-` + 3-digit number, counting up | `DEP-007` |
| **Name** | Short name, max 6 words | `Stripe Payment API Key` |
| **Type** | `Technical` / `Data & AI Model` / `Business / Compliance` | `Technical` |
| **AI Sub-Type** | Fill only if Type = Data & AI Model: `LLM` / `Vector DB` / `Dataset` / `Pipeline` / `Embedding Model` / `N/A` | `LLM` |
| **Description** | Plain English: what it is + why we need it | `GPT-4o API key to power the chat assistant feature. Without this the AI chatbot cannot function.` |
| **Source** | Where it comes from: `Internal` / `External Vendor` / `Open-Source` / `Cloud Provider` / `Regulatory Body` / `Partner` | `External Vendor` |
| **Owner** | One person's name who chases this | `James (Dev Lead)` |
| **Phase** | `Phase 1` / `Phase 2` / `Phase 3` / `Phase 4` | `Phase 2` |
| **Status** | `Not Started` / `In Progress` / `Resolved` / `Blocked` / `Cancelled` | `In Progress` |
| **Risk** | `Low` / `Medium` / `High` | `High` |
| **Identified Date** | Date you first noticed this dependency (`YYYY-MM-DD`) | `2026-10-14` |
| **Due Date** | Latest date it must be resolved (`YYYY-MM-DD`) | `2026-11-15` |
| **Resolved Date** | Date it was confirmed resolved; leave blank if not yet | `—` |
| **Blocked By** | DEP-ID of the dependency blocking this one; otherwise `—` | `DEP-002` |
| **Workaround Plan** | One sentence: what do we do if this isn't resolved in time? | `Use Claude API as fallback LLM provider while OpenAI agreement is pending.` |
| **Notes / Updates** | Latest update with date prefix, e.g. `[2026-10-20] Sent contract to legal review.` | See rows below |

---

## 📦 Phase 1 — Discovery & Scoping

> **Goal of this phase:** Confirm what we're building, who it's for, what tools and data we need, and whether the project is feasible.
> **Typical duration:** Week 1–3 of a project.
> **Who owns dependencies here:** Product Manager, AI Architect, Legal, Data team.

> 💡 **Tip:** At this phase, it's normal to have lots of unknowns. Log the dependency even if you don't have all the details yet. Fill in the gaps as you learn more.

---

### 🔧 Phase 1 — Technical Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-001 | _(e.g., Development Environment Setup)_ | Technical | N/A | _(e.g., All developers need Node.js v20+, Python 3.11+, and Docker installed and working before any coding can begin.)_ | Internal | _(e.g., DevOps Lead)_ | ⚪ Not Started | 🟡 Low | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use GitHub Codespaces as fallback cloud dev environment.)_ | _(e.g., [2026-10-14] Added to register.)_ |
| DEP-002 | _(e.g., Cloud Provider Account & Credits)_ | Technical | N/A | _(e.g., AWS account with production-grade limits. Needed before any infrastructure can be provisioned.)_ | Cloud Provider | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use personal AWS free tier temporarily for initial spikes.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

### 🤖 Phase 1 — Data & AI Model Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-010 | _(e.g., LLM Provider Selection & Proof-of-Concept)_ | Data & AI Model | LLM | _(e.g., We must select and validate our primary LLM provider (e.g., OpenAI GPT-4o, Anthropic Claude) during scoping. The choice affects architecture, cost model, and compliance posture for the entire project.)_ | External Vendor | _(e.g., AI Lead)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Build provider-agnostic abstraction layer so we can swap LLMs without re-architecting.)_ | _(e.g., [2026-10-14] Shortlist: OpenAI GPT-4o, Anthropic Claude 3.5 Sonnet, Google Gemini 1.5 Pro. Spike scheduled for Week 2.)_ |
| DEP-011 | _(e.g., Training / Evaluation Dataset Access)_ | Data & AI Model | Dataset | _(e.g., Access to 6 months of historical customer interaction data needed to evaluate LLM quality on our domain. Data must be anonymised before use.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-020 | _(e.g., Use publicly available benchmark datasets (MMLU, HellaSwag) as proxy during discovery.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

### 📋 Phase 1 — Business / Compliance Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-020 | _(e.g., Data Privacy Legal Review (GDPR / CCPA))_ | Business / Compliance | N/A | _(e.g., Legal team must confirm which user data can be stored, processed, and sent to external AI APIs under GDPR. This gates dataset preparation and LLM API usage.)_ | Regulatory Body / Internal Legal | _(e.g., Legal Counsel)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use synthetic data only during development until legal review is complete.)_ | — |
| DEP-021 | _(e.g., LLM Provider Data Processing Agreement (DPA))_ | Business / Compliance | N/A | _(e.g., A signed DPA with OpenAI / Anthropic is required before any real user data can be sent to the API. Enterprise plans typically include DPAs; consumer plans may not.)_ | External Vendor | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-020 | _(e.g., Use Anthropic API (which offers DPA on all plans) as interim fallback.)_ | — |
| DEP-022 | _(e.g., Project Budget Approval)_ | Business / Compliance | N/A | _(e.g., Finance sign-off on total project budget including cloud infra, LLM API costs, and tooling licences. Required before any paid contracts are signed.)_ | Internal | _(e.g., CFO / Finance Lead)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use existing team's expense accounts for small PoC costs under $500 approval threshold.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

## 🔧 Phase 2 — Development & Integration

> **Goal of this phase:** Build the product features, integrate external APIs and AI models, and wire up the data pipeline.
> **Typical duration:** Weeks 4–12 (varies by product size).
> **Who owns dependencies here:** Developers, AI Engineers, Data Engineers, DevOps.

> 💡 **Tip:** This is usually where the most dependencies pile up. Review this section at every sprint planning meeting.

---

### 🔧 Phase 2 — Technical Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-030 | _(e.g., LLM API Key — Production Tier)_ | Technical | N/A | _(e.g., A production-grade API key (not a free-tier key) from OpenAI with sufficient rate limits for development load testing. Free tier limits will throttle testing above 3 requests/min.)_ | External Vendor | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-021 | _(e.g., Cap concurrent users in dev/staging to stay within free-tier rate limits temporarily.)_ | — |
| DEP-031 | _(e.g., Authentication Service (e.g., Auth0, Supabase Auth))_ | Technical | N/A | _(e.g., User login, session management, and JWT token generation. The product cannot onboard any user without this.)_ | Cloud Provider | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use a simple email + magic-link flow in early beta; full OAuth added in Phase 4.)_ | — |
| DEP-032 | _(e.g., Payment Gateway Integration (e.g., Stripe))_ | Technical | N/A | _(e.g., Stripe API keys and webhook setup needed to charge users at launch. Requires business bank account to be linked first.)_ | External Vendor | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-040 | _(e.g., Launch free/beta tier at first — add payment later once Stripe account is verified.)_ | — |
| DEP-033 | _(e.g., Frontend Design System / Component Library)_ | Technical | N/A | _(e.g., Shared UI component library (e.g., Shadcn/UI, Material UI) must be selected and configured before any frontend screens are built to avoid rework.)_ | Open-Source | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use plain Tailwind CSS components if library decision is delayed.)_ | — |
| DEP-034 | _(e.g., Database Schema Finalised)_ | Technical | N/A | _(e.g., The core database schema (users, sessions, AI interactions, billing) must be agreed and frozen before backend API development starts. Schema changes mid-sprint are expensive.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use a draft schema with liberal use of JSONB columns to allow flexibility until schema is frozen.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

### 🤖 Phase 2 — Data & AI Model Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-050 | _(e.g., System Prompt / Prompt Template v1 Approved)_ | Data & AI Model | LLM | _(e.g., The core system prompt that defines the AI assistant's persona, guardrails, and instructions must be written, tested, and approved by Product + Legal before development integrates it.)_ | Internal | _(e.g., AI Lead + PM)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-010 | _(e.g., Use a placeholder "You are a helpful assistant" prompt so dev work can proceed while the real prompt is finalised.)_ | — |
| DEP-051 | _(e.g., LLM Model Version Pinned)_ | Data & AI Model | LLM | _(e.g., The specific model version (e.g., gpt-4o-2024-08-06) must be pinned in config to prevent unexpected behaviour changes if the provider updates the default model pointer.)_ | External Vendor | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-030 | _(e.g., Use model alias with version pinning env variable; update when new stable version is confirmed.)_ | — |
| DEP-052 | _(e.g., Context Window & Token Budget Defined)_ | Data & AI Model | LLM | _(e.g., Maximum context window size and per-request token budget (input + output) must be defined and coded as constants. This controls cost and latency for every API call.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-050 | _(e.g., Use conservative 4K token budget as default until benchmarking is complete.)_ | — |
| DEP-053 | _(e.g., AI Guardrails & Content Moderation Layer)_ | Data & AI Model | LLM | _(e.g., A content moderation layer (either API-level filtering or a separate moderation model call) must be implemented before any user-generated input is processed by the LLM. Legal and safety requirement.)_ | Internal / External Vendor | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-020 | _(e.g., Use OpenAI Moderation API endpoint as stopgap; replace with custom solution in Phase 4.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

### 📋 Phase 2 — Business / Compliance Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-040 | _(e.g., Business Bank Account Linked to Payment Provider)_ | Business / Compliance | N/A | _(e.g., The company's business bank account must be verified and linked to Stripe before Stripe can pay out collected revenue. This is a Stripe onboarding requirement that can take 3–5 business days.)_ | External Vendor | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use Stripe test mode for all payment flows until live account is verified.)_ | — |
| DEP-041 | _(e.g., Terms of Service & Privacy Policy — Legal Draft)_ | Business / Compliance | N/A | _(e.g., Legally reviewed Terms of Service, Privacy Policy, and AI Disclosure notice must be ready before any public beta users are onboarded. Required by law in most jurisdictions.)_ | Internal Legal / External Lawyer | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-020 | _(e.g., Use a waitlist-only access form (no account creation) to collect interest without onboarding users until docs are ready.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

## 🧪 Phase 3 — QA, Testing & Security Review

> **Goal of this phase:** Validate that the product works correctly, safely, and securely before launch. Fix all High-risk issues.
> **Typical duration:** Weeks 13–16.
> **Who owns dependencies here:** QA Engineers, Security team, AI Safety reviewers, DevOps.

> 💡 **Tip:** Security and AI safety dependencies often take longer than expected. Log them early — don't wait until the end of development.

---

### 🔧 Phase 3 — Technical Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-060 | _(e.g., Staging Environment Provisioned)_ | Technical | N/A | _(e.g., A fully isolated staging environment (mirroring production) must be running before QA testing begins. All QA tests must run on staging — never on production.)_ | Internal / Cloud Provider | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-002 | _(e.g., Run QA on local Docker compose setup if staging infra is delayed.)_ | — |
| DEP-061 | _(e.g., Automated Test Suite (Unit + Integration))_ | Technical | N/A | _(e.g., Core unit and integration tests covering the main user flows and AI response pipeline must be written and passing before any release candidate is approved for launch.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-060 | _(e.g., Manual QA sign-off as minimum viable gate; automated tests added before v1.1.)_ | — |
| DEP-062 | _(e.g., Monitoring & Alerting Setup (e.g., Sentry, Datadog))_ | Technical | N/A | _(e.g., Error monitoring and performance alerting must be configured and sending to the on-call channel before launch. Without it, we're blind to production issues.)_ | Cloud Provider | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use free Sentry tier and basic Vercel analytics as minimum monitoring at launch.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

### 🤖 Phase 3 — Data & AI Model Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-070 | _(e.g., AI Prompt Red-Teaming / Adversarial Testing)_ | Data & AI Model | LLM | _(e.g., The system prompt and AI pipeline must be tested against adversarial inputs (prompt injection, jailbreaks, harmful content requests) before launch. A minimum of 50 adversarial test cases required.)_ | Internal | _(e.g., AI Safety Lead)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-050 | _(e.g., Add a "report harmful output" button in the UI so users can flag issues post-launch as additional safety layer.)_ | — |
| DEP-071 | _(e.g., LLM Output Quality Evaluation (Evals))_ | Data & AI Model | LLM | _(e.g., A structured eval suite measuring accuracy, helpfulness, tone, and safety of LLM responses across at least 100 benchmark queries. Pass threshold: >85% satisfactory on human review.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-011 | _(e.g., Use a smaller 30-query eval set as minimum viable eval if full dataset isn't ready in time.)_ | — |
| DEP-072 | _(e.g., AI Cost & Rate Limit Load Test)_ | Data & AI Model | LLM | _(e.g., Load testing to verify that at peak expected load (500 concurrent users), LLM API costs stay within budget and rate limits are not exceeded. Must be run on staging with production API keys.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-060 | _(e.g., Cap registered users at 100 at launch and increase gradually while monitoring costs.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

### 📋 Phase 3 — Business / Compliance Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-080 | _(e.g., Security Penetration Test)_ | Business / Compliance | N/A | _(e.g., An external or internal security pen test covering authentication, data storage, API endpoints, and AI input/output handling. Any Critical or High findings must be resolved before launch.)_ | External Vendor / Internal | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-060 | _(e.g., Run OWASP ZAP automated scanner as minimum viable security check if full pen test timeline slips.)_ | — |
| DEP-081 | _(e.g., AI Ethics & Bias Review)_ | Business / Compliance | N/A | _(e.g., Internal review of the AI system for potential biases, discriminatory outputs, or accessibility issues. Required for any AI product touching sensitive topics (health, finance, HR, legal).)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-070 | _(e.g., Add clear AI disclosure notice and human escalation option as minimum bias mitigation at launch.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

## 🚀 Phase 4 — Launch & Post-Launch (First 500 Users)

> **Goal of this phase:** Ship the product, onboard the first real users safely, monitor performance, and close any remaining gaps identified in live use.
> **Typical duration:** Week 17 onwards — ongoing until 500 users milestone is confirmed.
> **Who owns dependencies here:** DevOps, PM, Customer Support, Finance, AI Engineer.

> 💡 **Tip:** At this phase, new dependencies pop up fast because real users find edge cases your team didn't anticipate. Review this section every 2–3 days at launch.

---

### 🔧 Phase 4 — Technical Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-090 | _(e.g., Production Infrastructure Provisioned & Scaled)_ | Technical | N/A | _(e.g., Production cloud infrastructure must be provisioned with auto-scaling enabled before the first public user is onboarded. Initial capacity target: handle 500 concurrent sessions without degradation.)_ | Cloud Provider | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-002 | _(e.g., Hard-cap registration at 50 users at launch and expand capacity before removing the cap.)_ | — |
| DEP-091 | _(e.g., CDN & DDoS Protection Enabled)_ | Technical | N/A | _(e.g., A CDN (e.g., Cloudflare) must be in front of the application at launch to absorb traffic spikes and protect against basic DDoS attacks.)_ | Cloud Provider | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-090 | _(e.g., Enable Cloudflare free tier as minimum DDoS protection.)_ | — |
| DEP-092 | _(e.g., On-Call Rotation Established)_ | Technical | N/A | _(e.g., A minimum 2-person on-call rotation with documented escalation path and runbooks must be in place before go-live. Engineers need to be reachable within 15 minutes for P0 incidents.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-062 | _(e.g., Founder + lead engineer takes all on-call in week 1 as a manual stopgap.)_ | — |
| DEP-093 | _(e.g., Customer Support Channel Live)_ | Technical | N/A | _(e.g., A support channel (e.g., Intercom, email, Discord) must be open and monitored before users are onboarded. First 500 users will have questions and bugs to report.)_ | External Vendor | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use a dedicated support@[company].com email as minimum viable support channel.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

### 🤖 Phase 4 — Data & AI Model Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-100 | _(e.g., LLM Cost Monitoring Dashboard Live)_ | Data & AI Model | LLM | _(e.g., A real-time dashboard tracking LLM token usage and cost per user, per day, and per feature must be live before launch. Without it, a runaway prompt could generate thousands of dollars in unexpected API costs.)_ | Internal / Cloud Provider | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-062 | _(e.g., Set daily spend alert at $50 threshold in OpenAI dashboard as minimum cost guard.)_ | — |
| DEP-101 | _(e.g., LLM Fallback / Circuit Breaker Implemented)_ | Data & AI Model | LLM | _(e.g., If the primary LLM API returns an error or exceeds rate limits, the system must gracefully degrade (show friendly error message, queue request, or fall back to a secondary model) rather than crash.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🔴 High | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | DEP-030 | _(e.g., Show a "Service temporarily busy — please try again in 30 seconds" message as minimum graceful degradation.)_ | — |
| DEP-102 | _(e.g., User Feedback Loop on AI Responses)_ | Data & AI Model | LLM | _(e.g., A thumbs up / thumbs down (or similar) feedback mechanism on AI responses must be live by the time 100 users are onboarded. This data is critical for future prompt iteration and model evaluation.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Manual user interviews with first 10 users if in-product feedback is delayed.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

### 📋 Phase 4 — Business / Compliance Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-110 | _(e.g., Launch Announcement / Press Kit Ready)_ | Business / Compliance | N/A | _(e.g., Marketing launch materials (product announcement, screenshots, demo video, press release) must be ready and approved before go-live for coordinated launch.)_ | Internal Marketing | _(Owner name)_ | ⚪ Not Started | 🟡 Low | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Soft-launch to waitlist without public announcement; formal launch delayed until materials are ready.)_ | — |
| DEP-111 | _(e.g., SLA / Uptime Commitment Defined)_ | Business / Compliance | N/A | _(e.g., A defined uptime target (e.g., 99.5% monthly) and incident response SLA (e.g., P0 resolved within 2 hours) must be documented and agreed internally before enterprise customers are onboarded.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🟠 Medium | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Communicate "best effort" SLA verbally to first 500 users; formalise for enterprise tier.)_ | — |
| DEP-112 | _(e.g., 500-User Milestone Tracking Confirmed)_ | Business / Compliance | N/A | _(e.g., Analytics or CRM tracking must be live and confirmed to accurately count active registered users. Required to know when the 500-user milestone is reached for internal reporting and investor updates.)_ | Internal | _(Owner name)_ | ⚪ Not Started | 🟡 Low | _(YYYY-MM-DD)_ | _(YYYY-MM-DD)_ | — | — | _(e.g., Use Supabase auth table row count as manual user count proxy.)_ | — |
| _(Add more rows as needed)_ | | | | | | | | | | | | | | |

---

## 🗺️ Dependency Map (Who Blocks Whom)

> **How to fill this section:** Update this table whenever you add a "Blocked By" value in any row above. It gives a quick visual of the critical path — which dependencies must be resolved first so others can start.
>
> 🧒 *Think of it like a relay race. Runner B can't start until Runner A hands them the baton. This table shows all the baton handoffs.*

| Upstream Dependency (Must Be Done First) | Downstream Dependency (Waiting on It) | Impact if Upstream Is Late |
|---|---|---|
| DEP-020 (GDPR Legal Review) | DEP-011 (Dataset Access), DEP-021 (DPA), DEP-041 (ToS & Privacy Policy) | No user data can be processed; no real users can be onboarded |
| DEP-021 (LLM Provider DPA) | DEP-030 (LLM API Key — Production) | Cannot use real user data with LLM |
| DEP-010 (LLM Provider Selection) | DEP-050 (System Prompt v1) | Prompt must be tuned to specific model |
| DEP-050 (System Prompt v1) | DEP-070 (Red-Teaming), DEP-071 (Evals) | Cannot test AI safety without final prompt |
| DEP-060 (Staging Environment) | DEP-061 (Automated Tests), DEP-080 (Pen Test), DEP-072 (Load Test) | No safe environment to run tests against |
| DEP-002 (Cloud Account & Credits) | DEP-060 (Staging Env), DEP-090 (Production Infra) | No infrastructure can be provisioned |
| DEP-090 (Production Infra) | DEP-091 (CDN / DDoS), DEP-092 (On-Call) | Cannot safely serve production traffic |
| _(Add more rows as you discover blocking relationships)_ | | |

---

## 🤖 AI Prompt Helpers

> **What is this section?**
> Copy-paste these prompts into Claude, ChatGPT, or any other AI assistant to speed up filling in this register. Replace the `[bracketed]` parts with your real project details. Each prompt is designed to output content you can paste directly into the relevant section above.
>
> 🧒 *Think of it like asking a smart friend to help you fill out a form. You give them the details, they write the draft, and you review and correct it.*

---

### 🤖 Prompt 1 — Identify Dependencies for Your Project

Use this at the very beginning to quickly generate a starter list of dependencies.

```
You are a Senior Technical Architect and AI Project Manager.

My project: [Describe your product in 2-3 sentences. What it does, who uses it, what tech stack you plan to use.]

Generate a comprehensive Dependency Register for this project covering all four phases:
1. Discovery & Scoping
2. Development & Integration
3. QA / Testing & Security
4. Launch & Post-Launch (First 500 Users)

For each dependency, provide:
- A unique DEP-ID (DEP-001, DEP-002, ...)
- Name (max 6 words)
- Type (Technical / Data & AI Model / Business Compliance)
- Description (2 sentences, plain English)
- Suggested Owner role (not a person's name)
- Risk Level (Low / Medium / High)
- Which phase it belongs to
- Whether it blocks any other dependency

Focus especially on AI-specific dependencies: LLM provider selection, API rate limits, model version pinning, prompt engineering, content moderation, cost monitoring, and AI safety testing.

Format the output as a Markdown table.
```

---

### 🤖 Prompt 2 — Write a Workaround Plan for a Specific Dependency

Use this when you're stuck thinking of a fallback for a specific dependency.

```
I am building: [1-sentence product description]

I have this dependency:
Name: [Dependency Name]
Description: [What it is and why we need it]
Type: [Technical / Data & AI Model / Business Compliance]
Phase: [Phase 1 / 2 / 3 / 4]
Risk: [Low / Medium / High]

Write 3 possible workaround plans if this dependency is not resolved on time.
For each workaround, state:
1. What the team does instead
2. What capability or quality is sacrificed
3. For how long this workaround is sustainable

Keep each workaround to 2-3 sentences. Plain English. Beginner-friendly.
```

---

### 🤖 Prompt 3 — Update the Health Dashboard

Use this at your weekly team review to quickly compute dashboard numbers.

```
Here is my current Dependency Register data:

[Paste all your DEP rows here, or summarise: "I have 23 dependencies: 8 Resolved, 9 In Progress, 3 Blocked, 2 Not Started, 1 Cancelled"]

Please:
1. Compute the Health Dashboard summary (totals by status, risk level, and phase)
2. List all High-risk unresolved dependencies with their owner and due date
3. List all Blocked dependencies and what they're blocked by
4. Highlight any dependencies that are past their due date
5. Suggest the top 3 dependencies the team should focus on this week

Format as Markdown tables.
```

---

### 🤖 Prompt 4 — Generate AI-Specific Dependencies for an LLM-Powered Feature

Use this when adding a new AI feature to check you haven't missed any dependencies.

```
I am adding the following AI feature to my product: [Describe the feature in 2-3 sentences]

The feature uses: [e.g., OpenAI GPT-4o API, LangChain orchestration, Pinecone vector DB]

Generate a complete list of AI-specific dependencies I need to log in my Dependency Register for this feature, covering:
- LLM model selection and version pinning
- API key management and rate limits
- Prompt engineering and system prompt approval
- Content moderation and AI safety guardrails
- Token budget and cost monitoring
- Evaluation / testing of AI output quality
- Fallback behaviour if the AI API is unavailable
- Data privacy requirements for user inputs sent to the AI

For each dependency, provide: Name, Type, Description (2 sentences), Phase, Risk (Low/Medium/High), Workaround Plan.
```

---

### 🤖 Prompt 5 — Write Impact Statement for a Blocked Dependency

Use this when escalating a blocker to leadership or stakeholders.

```
I need to communicate the business impact of an unresolved dependency to my project stakeholders.

Dependency: [Name and description]
Due Date: [Date]
Days Overdue / At Risk: [Number of days]
Downstream Dependencies Blocked: [List them]
Team Members Impacted: [List roles]

Write a clear, non-technical 3-paragraph escalation note explaining:
1. What the dependency is (in plain business language)
2. What happens to the project if it isn't resolved in the next [X] days
3. What we need from stakeholders to resolve it

Tone: professional but urgent. No jargon.
```

---

## 📝 Changelog

> **How to fill this section:** Add one row every time you make a significant change to this document. Small typo fixes don't need a row. Significant changes = adding/removing a dependency, changing an owner, updating a risk level, or closing a blocker.

| # | Date | Changed By | What Changed |
|---|---|---|---|
| 1 | _(e.g., 2026-10-14)_ | _(e.g., Alice Chen — PM)_ | _(e.g., Template created. Project metadata filled in. 22 starter dependencies added across Phases 1–4.)_ |
| 2 | _(e.g., 2026-10-21)_ | _(e.g., James Liu — Dev Lead)_ | _(e.g., DEP-030 status updated to In Progress. DEP-033 owner assigned to Sarah.)_ |
| 3 | | | |
| _(Add a new row each time you review and update)_ | | | |

---

## 🏁 Quick-Start Checklist

> Use this checklist the first time you use this template on a new project.

- [ ] Fill in all fields in **Section 2 (Project & Register Info)**
- [ ] Schedule a weekly **Dependency Review** in your calendar (15 minutes is enough)
- [ ] Assign at least one person as **Register Owner** — they keep it up to date
- [ ] Use **Prompt 1** from the AI Prompt Helpers to generate your first list of dependencies
- [ ] Make sure every dependency has an **Owner** and a **Due Date** within 48 hours of being added
- [ ] Update the **Health Dashboard** before every sprint planning / team standup
- [ ] Add a **Changelog entry** every time you make a significant update
- [ ] Share this file in your team's main project folder so everyone can access it

---

*Template maintained by: [Register Owner Name] · Review schedule: [e.g., Every Monday] · Questions? Ping [Slack handle / email]*
