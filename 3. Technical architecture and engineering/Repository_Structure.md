<!--
════════════════════════════════════════════════════════════════════════════════
  HOW TO FILL THIS DOCUMENT  ✍️
════════════════════════════════════════════════════════════════════════════════

WELCOME! This file is your project's "map" — it tells anyone (including AI
tools like Claude) exactly how this repository is laid out, why it's laid out
that way, and how to work inside it safely.

GOLDEN RULES BEFORE YOU START:
  1. Read every instruction comment (the grey text between <!-- and -->).
  2. Replace every [PLACEHOLDER] with your real information.
  3. Delete the instruction comment AFTER you fill in that section.
  4. If a section doesn't apply to your project → write "N/A – [reason]".
  5. Keep this file at the ROOT of your repository (same level as package.json
     or pyproject.toml).
  6. Update this file every time you add a new folder or change the structure.

WHO SHOULD FILL THIS?
  → You: the person who created or owns this project.
  → Takes about 30–60 minutes the first time.
  → After that, updates take only 5 minutes.

STUCK? Look for the 💡 TIP lines — they show real examples.
════════════════════════════════════════════════════════════════════════════════
-->

# 📁 Repository Structure

> **One-liner about this document:**
> This file is the single source of truth for how this repository is organized.
> It tells every human and every AI agent where things live, why they live
> there, and what the rules are.

---

## 🗂️ Table of Contents

- [Project Identity](#-1-project-identity)
- [Repository Layout Strategy](#-2-repository-layout-strategy)
- [Complete Folder Tree](#-3-complete-folder-tree)
- [Folder-by-Folder Breakdown](#-4-folder-by-folder-breakdown)
- [File Naming Conventions](#-5-file-naming-conventions)
- [Environment & Secrets Management](#-6-environment--secrets-management)
- [Branch Strategy & Git Conventions](#-7-branch-strategy--git-conventions)
- [AI-Driven Workflow (Claude & Agents)](#-8-ai-driven-workflow-claude--agents)
- [Development Lifecycle Phases](#-9-development-lifecycle-phases)
- [Onboarding: Up & Running in 10 Minutes](#-10-onboarding-up--running-in-10-minutes)
- [Post-Launch: Road to 500 Customers](#-11-post-launch-road-to-500-customers)
- [Maintenance & Governance](#-12-maintenance--governance)
- [Glossary for Beginners](#-13-glossary-for-beginners)

---

## 🪪 1. Project Identity

<!--
INSTRUCTION: Fill in every field below. These 10 lines are what an AI model
or a new teammate reads FIRST to understand what this project is.
💡 TIP — Example filled version:
  Project Name   : TaskPilot AI
  Tagline        : AI-powered task manager that turns chaos into clarity
  Version        : 0.3.1 (MVP)
  Status         : 🔨 In Development
  Owner          : Jane Doe <jane@taskpilot.io>
  Repository URL : https://github.com/taskpilot/taskpilot-app
  Live URL       : https://app.taskpilot.io
  Docs URL       : https://docs.taskpilot.io
  License        : MIT
  Created On     : 2026-01-15
-->

| Field              | Value                                                  |
|--------------------|--------------------------------------------------------|
| **Project Name**   | [REPLACE: Your Project Name]                           |
| **Tagline**        | [REPLACE: One sentence — what does this do and for whom?] |
| **Current Version**| [REPLACE: e.g., 0.1.0-alpha / 1.0.0 / MVP]            |
| **Status**         | [REPLACE: 🌱 Idea / 🔨 In Development / 🚀 Launched / 📈 Growing] |
| **Owner / Author** | [REPLACE: Full Name \<email@example.com\>]             |
| **Repository URL** | [REPLACE: https://github.com/your-org/your-repo]       |
| **Live URL**       | [REPLACE: https://yourapp.com — or "Not deployed yet"] |
| **Docs URL**       | [REPLACE: https://docs.yourapp.com — or "Same repo /docs"] |
| **License**        | [REPLACE: MIT / Apache-2.0 / Proprietary]              |
| **Created On**     | [REPLACE: YYYY-MM-DD]                                  |
| **Last Updated**   | [REPLACE: YYYY-MM-DD — update this every time you edit] |

---

## 🏗️ 2. Repository Layout Strategy

<!--
INSTRUCTION: Choose ONE layout and DELETE the other section.
If you're just starting out, pick MONOREPO — it's simpler for solo developers.
-->

### Which layout does this repo use?

- [ ] **Monorepo** — Everything lives in this single repository
- [ ] **Polyrepo** — This is ONE of several separate repositories

<!--
If MONOREPO → fill in the Monorepo section below and delete the Polyrepo one.
If POLYREPO → fill in the Polyrepo section and delete the Monorepo one.
-->

---

### 📦 Option A — Monorepo Layout

<!--
INSTRUCTION (Monorepo): List every major "app" or "package" that lives inside
this single repo. Think of an app as something a user opens (website, mobile
app, admin dashboard) and a package as shared code (UI components, utilities).

💡 TIP:
  Apps     : web-app, mobile-app, admin-dashboard
  Packages : ui-kit, api-client, shared-types, email-templates
-->

**Why monorepo?**
[REPLACE: e.g., "Solo developer, easier to share types and utilities across
web and mobile without publishing to npm."]

**Apps inside this repo:**

| App Folder           | What It Is                              | Port / URL              |
|----------------------|-----------------------------------------|-------------------------|
| `apps/web`           | [REPLACE: e.g., Next.js marketing site] | [REPLACE: localhost:3000] |
| `apps/mobile`        | [REPLACE: e.g., React Native iOS/Android app] | [REPLACE: Expo Go] |
| `apps/api`           | [REPLACE: e.g., FastAPI backend]        | [REPLACE: localhost:8000] |
| `apps/admin`         | [REPLACE: e.g., Internal admin panel]  | [REPLACE: localhost:3001] |

<!-- Add or remove rows as needed. Delete rows that don't exist yet. -->

**Shared packages inside this repo:**

| Package Folder         | What It Contains                         |
|------------------------|------------------------------------------|
| `packages/ui`          | [REPLACE: e.g., Shared React components] |
| `packages/types`       | [REPLACE: e.g., TypeScript interfaces shared across apps] |
| `packages/utils`       | [REPLACE: e.g., Date formatting, validation helpers] |
| `packages/config`      | [REPLACE: e.g., ESLint, Prettier, TSConfig base files] |

<!-- Add or remove rows as needed. -->

**Monorepo tool used:**
[REPLACE: Turborepo / Nx / pnpm workspaces / Yarn workspaces / None yet]

---

### 🔗 Option B — Polyrepo Layout

<!--
INSTRUCTION (Polyrepo): This file lives in ONE repo. List all the OTHER repos
that make up the full system here so anyone reading this knows where to go.

💡 TIP:
  Repo                          | What it does
  taskpilot-web                 | Next.js frontend
  taskpilot-api                 | FastAPI backend
  taskpilot-mobile              | React Native app
  taskpilot-infra               | Terraform / cloud config
-->

**This repository:** [REPLACE: What this specific repo contains]

**All other repos in the system:**

| Repository URL                          | Role / Purpose                    |
|-----------------------------------------|-----------------------------------|
| [REPLACE: https://github.com/org/repo1] | [REPLACE: e.g., Frontend web app] |
| [REPLACE: https://github.com/org/repo2] | [REPLACE: e.g., Backend API]      |
| [REPLACE: https://github.com/org/repo3] | [REPLACE: e.g., Infrastructure]   |

---

## 🌳 3. Complete Folder Tree

<!--
INSTRUCTION: Draw your actual folder tree here. This is the most important
section — it's the "map" of your project.

HOW TO GENERATE THIS AUTOMATICALLY:
  In your terminal, run:
    tree -L 3 --dirsfirst -I "node_modules|.git|__pycache__|.next|dist|build"
  Then paste the output below and add a comment after each item.

If you don't have `tree` installed:
  macOS  → brew install tree
  Linux  → sudo apt install tree
  Windows → winget install tree-extended

💡 TIP — Example for a full-stack monorepo:

  your-project/
  ├── apps/
  │   ├── web/          ← Next.js frontend
  │   ├── api/          ← FastAPI or Node.js backend
  │   └── mobile/       ← React Native app
  ├── packages/
  │   ├── ui/           ← Shared UI components
  │   └── types/        ← Shared TypeScript types
  ├── ai/
  │   ├── prompts/      ← Reusable prompt templates
  │   ├── agents/       ← AI agent configs
  │   └── decisions/    ← AI decision log
  ├── docs/
  │   ├── architecture/ ← System design docs, ADRs
  │   ├── api/          ← API reference docs
  │   └── runbooks/     ← How to do operational tasks
  ├── infrastructure/
  │   ├── docker/       ← Dockerfiles
  │   ├── terraform/    ← Cloud infra as code
  │   └── k8s/          ← Kubernetes configs
  ├── tests/
  │   ├── e2e/          ← End-to-end tests
  │   └── load/         ← Performance / load tests
  ├── scripts/          ← Dev and deployment helper scripts
  ├── .github/
  │   ├── workflows/    ← CI/CD pipelines
  │   └── ISSUE_TEMPLATE/ ← Issue and PR templates
  ├── CLAUDE.md         ← AI context file for Claude
  ├── README.md         ← Project overview (public-facing)
  ├── Repository_Structure.md ← THIS FILE
  ├── .env.example      ← Safe template of env variables
  ├── .gitignore        ← Files Git should never track
  └── package.json / pyproject.toml ← Project root config
-->

```
[REPLACE: Paste your folder tree here]
[REPLACE: Add a short comment after each folder — see the tip above]
```

---

## 📂 4. Folder-by-Folder Breakdown

<!--
INSTRUCTION: For EVERY folder in your tree above, fill in one row of the table
below. If a folder doesn't exist yet but is planned, mark it as [PLANNED].

Column explanations:
  Folder Path     → The exact path from repo root  (e.g., apps/web/components)
  Purpose         → What lives here in plain English (1–2 sentences max)
  Key Files       → The 2–3 most important files inside this folder
  Who Touches It  → Developer / AI Agent / CI/CD / Everyone / No one yet
  Status          → ✅ Active / 🔨 WIP / 📋 Planned / 🗄️ Legacy
-->

### Root-Level Files

| File / Folder                | Purpose                                                   | Status |
|------------------------------|-----------------------------------------------------------|--------|
| `README.md`                  | Public-facing intro: what the project is and how to run it | ✅ Active |
| `CLAUDE.md`                  | AI context file — tells Claude how to work in this repo   | [REPLACE] |
| `Repository_Structure.md`    | This file — the map of the entire project                 | ✅ Active |
| `.env.example`               | A safe, committed template of all env variable names (no real values) | [REPLACE] |
| `.gitignore`                 | List of files/folders Git must never track                | [REPLACE] |
| `package.json` / `pyproject.toml` | Project metadata and root-level scripts             | [REPLACE] |
| `turbo.json` / `nx.json`     | Monorepo task runner config (delete if not using one)     | [REPLACE] |
| `docker-compose.yml`         | Runs the full local dev environment with one command      | [REPLACE] |

---

### `/apps` — Deployable Applications

<!--
INSTRUCTION: Fill one sub-section per app. Copy the template block and
paste it for each app you have (web, api, mobile, admin, etc.).
-->

#### `apps/web` — [REPLACE: e.g., Customer-facing Next.js Web App]

<!--
💡 TIP: "This is the website customers visit. Built with Next.js 14 (App Router).
Talks to apps/api for all data. Deployed to Vercel."
-->

| Property         | Detail                                                        |
|------------------|---------------------------------------------------------------|
| **Framework**    | [REPLACE: e.g., Next.js 14 / Vite + React / Vue 3]           |
| **Language**     | [REPLACE: TypeScript / JavaScript / Python]                   |
| **Runs on**      | [REPLACE: e.g., localhost:3000]                               |
| **Deployed to**  | [REPLACE: e.g., Vercel / Netlify / AWS / Not yet]             |
| **Talks to**     | [REPLACE: e.g., apps/api at localhost:8000]                   |
| **Start command**| [REPLACE: e.g., `pnpm dev` from repo root or `cd apps/web && npm run dev`] |

Key sub-folders inside `apps/web`:

| Sub-folder               | What lives here                                       |
|--------------------------|-------------------------------------------------------|
| `app/` or `src/`         | [REPLACE: e.g., Page routes and layouts (App Router)] |
| `components/`            | [REPLACE: e.g., Reusable UI components (Buttons, Cards, Modals)] |
| `lib/` or `utils/`       | [REPLACE: e.g., Helper functions, API client wrappers] |
| `hooks/`                 | [REPLACE: e.g., Custom React hooks]                   |
| `styles/`                | [REPLACE: e.g., Global CSS, Tailwind config]          |
| `public/`                | [REPLACE: e.g., Static assets: images, icons, fonts]  |
| `__tests__/`             | [REPLACE: e.g., Unit tests for components]            |

---

#### `apps/api` — [REPLACE: e.g., Backend REST API]

| Property         | Detail                                                        |
|------------------|---------------------------------------------------------------|
| **Framework**    | [REPLACE: e.g., FastAPI / Express / NestJS / Hono]            |
| **Language**     | [REPLACE: Python 3.12 / TypeScript]                           |
| **Runs on**      | [REPLACE: e.g., localhost:8000]                               |
| **Deployed to**  | [REPLACE: e.g., Railway / Fly.io / AWS Lambda / Not yet]      |
| **Database**     | [REPLACE: e.g., PostgreSQL via Supabase / MongoDB / SQLite]   |
| **Auth method**  | [REPLACE: e.g., JWT / Supabase Auth / Clerk / NextAuth]       |
| **Start command**| [REPLACE: e.g., `uvicorn main:app --reload`]                  |

Key sub-folders inside `apps/api`:

| Sub-folder          | What lives here                                            |
|---------------------|------------------------------------------------------------|
| `routes/` or `routers/` | [REPLACE: e.g., API route handlers grouped by feature] |
| `models/`           | [REPLACE: e.g., Database models / ORM schemas]             |
| `services/`         | [REPLACE: e.g., Business logic, third-party integrations]  |
| `middleware/`       | [REPLACE: e.g., Auth checks, logging, rate limiting]       |
| `schemas/`          | [REPLACE: e.g., Pydantic / Zod request & response schemas] |
| `migrations/`       | [REPLACE: e.g., Database migration files]                  |
| `tests/`            | [REPLACE: e.g., API unit and integration tests]            |

---

#### `apps/mobile` — [REPLACE: e.g., iOS & Android Mobile App]

<!--
INSTRUCTION: Delete this section if you don't have a mobile app yet.
-->

| Property         | Detail                                                        |
|------------------|---------------------------------------------------------------|
| **Framework**    | [REPLACE: e.g., React Native (Expo) / Flutter]               |
| **Language**     | [REPLACE: TypeScript / Dart]                                  |
| **Runs on**      | [REPLACE: e.g., Expo Go app on physical device / iOS Simulator] |
| **Deployed to**  | [REPLACE: e.g., App Store / Google Play / TestFlight]        |
| **Talks to**     | [REPLACE: e.g., Same apps/api backend]                       |
| **Start command**| [REPLACE: e.g., `npx expo start`]                            |

---

### `/packages` — Shared Code Libraries

<!--
INSTRUCTION: Fill one row per shared package. These are NOT deployed directly —
they are imported by the apps above.
Delete this section if you are NOT using a monorepo.
-->

| Package              | What It Exports                                           | Imported By              |
|----------------------|-----------------------------------------------------------|--------------------------|
| `packages/ui`        | [REPLACE: e.g., Button, Card, Modal, Form components]     | [REPLACE: apps/web, apps/admin] |
| `packages/types`     | [REPLACE: e.g., User, Product, Order TypeScript interfaces] | [REPLACE: All apps]    |
| `packages/utils`     | [REPLACE: e.g., formatDate(), truncateText(), slugify()]  | [REPLACE: apps/web, apps/api] |
| `packages/config`    | [REPLACE: e.g., Shared ESLint rules, Prettier config, tsconfig.base.json] | [REPLACE: All apps] |
| `packages/email`     | [REPLACE: e.g., React Email templates for transactional emails] | [REPLACE: apps/api] |

---

### `/ai` — AI & Agent Workflow Files

<!--
INSTRUCTION: This is the most unique section of an AI-driven project.
These files exist to make Claude and other AI tools work better with your code.
Fill in every sub-section carefully.
-->

#### `ai/prompts/` — Prompt Library

<!--
INSTRUCTION: List every reusable prompt file you have.
Naming convention: use kebab-case, suffix with the prompt's purpose.
💡 TIP:
  system-prompt-api.md       ← The system prompt for your API AI features
  user-onboarding-email.md   ← Prompt for generating onboarding emails
  code-review-checklist.md   ← Prompt Claude uses when reviewing PRs
-->

| Prompt File                  | When / How It's Used                                       |
|------------------------------|------------------------------------------------------------|
| `system-prompt-[feature].md` | [REPLACE: e.g., System prompt for the chat assistant feature] |
| `code-review.md`             | [REPLACE: e.g., Given to Claude when reviewing PRs]        |
| `test-generator.md`          | [REPLACE: e.g., Claude uses this to auto-generate unit tests] |
| `user-research.md`           | [REPLACE: e.g., Summarising user interviews into insights] |

---

#### `ai/agents/` — Agent Configuration Files

<!--
INSTRUCTION: If you use AI agents (Claude agents, LangChain, CrewAI, AutoGen,
or custom agentic pipelines), list them here.
💡 TIP:
  ci-code-reviewer/   ← Agent that auto-reviews every PR
  content-generator/  ← Agent that writes marketing copy
  test-runner/        ← Agent that writes and fixes tests
-->

| Agent Folder / File          | Role / What It Does                                        | Trigger                  |
|------------------------------|------------------------------------------------------------|--------------------------|
| `agents/[agent-name]/`       | [REPLACE: e.g., Reviews every pull request for bugs]       | [REPLACE: e.g., On every PR open] |
| `agents/[agent-name]/`       | [REPLACE: e.g., Generates weekly changelog from commits]   | [REPLACE: e.g., Every Monday 9am] |

---

#### `ai/decisions/` — AI Decision Log

<!--
INSTRUCTION: Every time you (or Claude) make a significant architectural or
product decision, add an entry here. This is your project's memory.
File naming: YYYY-MM-DD-short-title.md
💡 TIP:
  2026-01-15-chose-supabase-over-firebase.md
  2026-02-03-switched-to-monorepo.md
  2026-03-20-added-stripe-for-payments.md
-->

| Decision File                          | Summary of Decision                               |
|----------------------------------------|---------------------------------------------------|
| `YYYY-MM-DD-[short-title].md`          | [REPLACE: e.g., Why we chose PostgreSQL over MongoDB] |

**Format of each decision file:**
```markdown
# Decision: [Title]
Date: YYYY-MM-DD
Made By: [Human name] + [AI tool used, if any]

## Context
[What problem were we solving?]

## Decision
[What did we decide?]

## Alternatives Considered
[What else did we look at?]

## Consequences
[What does this decision mean going forward?]
```

---

### `/docs` — Project Documentation

<!--
INSTRUCTION: Your docs folder is your project's knowledge base.
Fill in what documentation you have (or plan to have) in each sub-folder.
-->

| Sub-folder              | What Lives Here                                           | Status          |
|-------------------------|-----------------------------------------------------------|-----------------|
| `docs/architecture/`    | [REPLACE: e.g., System design diagrams, data flow charts, ERDs] | [REPLACE] |
| `docs/api/`             | [REPLACE: e.g., API reference, endpoint docs (or link to Swagger)] | [REPLACE] |
| `docs/adr/`             | [REPLACE: e.g., Architecture Decision Records (ADRs)]     | [REPLACE]       |
| `docs/runbooks/`        | [REPLACE: e.g., How to deploy, rollback, handle incidents] | [REPLACE]      |
| `docs/user-research/`   | [REPLACE: e.g., Interview notes, survey results, personas] | [REPLACE]      |
| `docs/product/`         | [REPLACE: e.g., PRD, feature specs, roadmap]              | [REPLACE]       |
| `docs/changelog/`       | [REPLACE: e.g., What changed in each version / release]   | [REPLACE]       |

---

### `/tests` — Test Suite

<!--
INSTRUCTION: List your testing strategy. Even if you have no tests yet,
PLAN where they will live. This signals good intent to future contributors.
-->

| Sub-folder            | Test Type        | What It Tests                                              | Tool Used               |
|-----------------------|------------------|------------------------------------------------------------|-------------------------|
| `tests/unit/`         | Unit             | [REPLACE: e.g., Individual functions and components]       | [REPLACE: e.g., Vitest / Jest / pytest] |
| `tests/integration/`  | Integration      | [REPLACE: e.g., API endpoints with a real test database]   | [REPLACE: e.g., Supertest / httpx] |
| `tests/e2e/`          | End-to-End       | [REPLACE: e.g., Full user flows in the browser]            | [REPLACE: e.g., Playwright / Cypress] |
| `tests/load/`         | Performance      | [REPLACE: e.g., API under 1000 concurrent users]           | [REPLACE: e.g., k6 / Locust] |

**Test coverage goal:** [REPLACE: e.g., Minimum 80% unit coverage on the API layer]

**Run all tests command:**
```bash
[REPLACE: e.g., pnpm test  OR  pytest  OR  npm run test:all]
```

---

### `/infrastructure` — Cloud & Deployment Config

<!--
INSTRUCTION: Fill in what infrastructure tools you use.
Delete sub-folders that don't apply. Add ones that do.
-->

| Sub-folder                 | Tool / Purpose                                             | Status          |
|----------------------------|------------------------------------------------------------|-----------------|
| `infrastructure/docker/`   | [REPLACE: e.g., Dockerfiles for each app + docker-compose] | [REPLACE]       |
| `infrastructure/terraform/`| [REPLACE: e.g., AWS / GCP / Azure resources as code]       | [REPLACE]       |
| `infrastructure/k8s/`      | [REPLACE: e.g., Kubernetes deployment manifests]           | [REPLACE]       |
| `infrastructure/nginx/`    | [REPLACE: e.g., Nginx reverse proxy config]                | [REPLACE]       |
| `infrastructure/certs/`    | [REPLACE: e.g., SSL/TLS certificate renewal scripts]       | [REPLACE]       |

**Cloud provider(s):** [REPLACE: e.g., AWS + Vercel + Supabase / GCP / Not decided]

---

### `/.github` — GitHub Automation

<!--
INSTRUCTION: List your GitHub Actions workflows and other GitHub config.
If you use GitLab, rename this section to /.gitlab.
-->

| File / Folder                          | What It Does                                        |
|----------------------------------------|-----------------------------------------------------|
| `.github/workflows/ci.yml`             | [REPLACE: e.g., Runs lint, type-check, and tests on every push] |
| `.github/workflows/deploy-staging.yml` | [REPLACE: e.g., Deploys to staging on push to `develop`] |
| `.github/workflows/deploy-prod.yml`    | [REPLACE: e.g., Deploys to production on push to `main`] |
| `.github/workflows/ai-review.yml`      | [REPLACE: e.g., Triggers Claude to auto-review every PR] |
| `.github/ISSUE_TEMPLATE/`              | [REPLACE: e.g., Bug report & feature request templates] |
| `.github/PULL_REQUEST_TEMPLATE.md`     | [REPLACE: e.g., PR checklist every contributor fills out] |
| `.github/CODEOWNERS`                   | [REPLACE: e.g., Who must review changes in each folder] |

---

### `/scripts` — Helper Scripts

<!--
INSTRUCTION: List useful scripts in this folder — things your team runs
manually to set up, seed, migrate, or deploy the project.
-->

| Script File                  | What It Does                                               | Run Command              |
|------------------------------|------------------------------------------------------------|--------------------------|
| `scripts/setup.sh`           | [REPLACE: e.g., Installs all dependencies and creates .env] | `bash scripts/setup.sh` |
| `scripts/seed-db.ts`         | [REPLACE: e.g., Fills the database with realistic test data] | `pnpm run seed`         |
| `scripts/migrate.sh`         | [REPLACE: e.g., Runs pending database migrations]          | `bash scripts/migrate.sh` |
| `scripts/generate-types.sh`  | [REPLACE: e.g., Auto-generates TypeScript types from DB schema] | `bash scripts/generate-types.sh` |

---

## ✏️ 5. File Naming Conventions

<!--
INSTRUCTION: These are the rules for naming files and folders.
Consistent naming makes Claude and teammates faster. Fill in your rules below.
-->

### General Rules

| Rule                          | Correct ✅                        | Wrong ❌                     |
|-------------------------------|-----------------------------------|-----------------------------|
| Folders                       | `user-profile/`                   | `UserProfile/`, `userProfile/` |
| Component files (React)       | `user-card.tsx`                   | `UserCard.tsx`, `usercard.tsx` |
| Utility / helper files        | `format-date.ts`                  | `FormatDate.ts`, `formatdate.ts` |
| Test files                    | `user-card.test.tsx`              | `UserCard.test.tsx`         |
| API route files               | `get-user.ts`, `create-order.ts`  | `getUser.ts`, `GET.ts`      |
| Environment files             | `.env`, `.env.example`, `.env.local` | `.ENV`, `env.js`          |
| Documentation files           | `system-design.md`                | `SystemDesign.md`           |
| AI prompt files               | `code-review.md`                  | `CodeReview.txt`            |
| Database migration files      | `20260115_add_users_table.sql`    | `migration1.sql`            |
| AI decision files             | `2026-01-15-chose-postgres.md`    | `postgres-decision.md`      |

### Specific Conventions

<!--
INSTRUCTION: Fill in any project-specific rules below.
Delete lines that don't apply, add your own.
-->

- **React components:** [REPLACE: e.g., Files use `kebab-case.tsx`, the component function inside uses `PascalCase`]
- **API endpoints:** [REPLACE: e.g., Always `kebab-case`, plural nouns (e.g., `/api/users`, `/api/blog-posts`)]
- **Database tables:** [REPLACE: e.g., `snake_case`, plural (e.g., `users`, `blog_posts`)]
- **Environment variables:** [REPLACE: e.g., `SCREAMING_SNAKE_CASE` (e.g., `DATABASE_URL`, `STRIPE_SECRET_KEY`)]
- **Git branches:** [REPLACE: e.g., `type/short-description` (e.g., `feat/user-auth`, `fix/login-crash`)]
- **Commit messages:** [REPLACE: e.g., Conventional Commits — see Section 7]

---

## 🔐 6. Environment & Secrets Management

<!--
INSTRUCTION: This section is CRITICAL. It tells everyone what env variables
exist, where they go, and — most importantly — what NEVER gets committed.
Read every line carefully before filling it in.
-->

### The Golden Rule of Secrets

> ❌ **NEVER commit a real secret to Git. Ever.**
> Real API keys, database passwords, private keys, and tokens go ONLY in
> `.env` files that are listed in `.gitignore`.
> If you accidentally commit a secret → treat it as compromised immediately
> and rotate it in the service that issued it.

---

### Environment Files in This Project

<!--
INSTRUCTION: List every .env file your project uses.
💡 TIP — Common pattern:
  .env              → Local dev secrets (gitignored, never committed)
  .env.example      → Safe template showing all variable NAMES (committed)
  .env.test         → Values used during automated testing (committed — only use fake values)
  .env.staging      → Staging values (gitignored, stored in CI/CD secrets)
  .env.production   → Prod values (gitignored, stored in CI/CD secrets)
-->

| File               | Committed to Git? | Who Fills It In               | Purpose                           |
|--------------------|-------------------|-------------------------------|-----------------------------------|
| `.env`             | ❌ NO (gitignored) | You — copy from .env.example  | Local development secrets         |
| `.env.example`     | ✅ YES             | You — update when adding vars | Template showing all variable names |
| `.env.test`        | ✅ YES (fake values only) | You                    | Values for automated test runs    |
| `.env.staging`     | ❌ NO (gitignored) | CI/CD secrets manager         | Staging environment config        |
| `.env.production`  | ❌ NO (gitignored) | CI/CD secrets manager         | Production environment config     |

---

### Environment Variable Catalog

<!--
INSTRUCTION: List EVERY environment variable your project needs.
Group them by category. This is what goes in your .env.example file.
💡 TIP — Example variables:
  # Database
  DATABASE_URL=postgresql://localhost:5432/myapp_dev
  # Auth
  JWT_SECRET=your-256-bit-secret-here
  # Third-party
  STRIPE_SECRET_KEY=sk_test_...
  OPENAI_API_KEY=sk-...
-->

```env
# ─────────────────────────────────────────────
# APPLICATION
# ─────────────────────────────────────────────
APP_NAME=[REPLACE: e.g., my-app]
APP_ENV=[REPLACE: development | staging | production]
APP_PORT=[REPLACE: e.g., 3000]
APP_URL=[REPLACE: e.g., http://localhost:3000]

# ─────────────────────────────────────────────
# DATABASE
# ─────────────────────────────────────────────
DATABASE_URL=[REPLACE: e.g., postgresql://user:pass@localhost:5432/dbname]
DATABASE_POOL_SIZE=[REPLACE: e.g., 10]

# ─────────────────────────────────────────────
# AUTHENTICATION
# ─────────────────────────────────────────────
JWT_SECRET=[REPLACE: A long random string — generate with: openssl rand -hex 32]
JWT_EXPIRY=[REPLACE: e.g., 7d]
# OR if using Supabase/Clerk/Auth0:
AUTH_PROVIDER_URL=[REPLACE: e.g., https://your-project.supabase.co]
AUTH_PROVIDER_KEY=[REPLACE: your-anon-key]

# ─────────────────────────────────────────────
# AI & LANGUAGE MODELS
# ─────────────────────────────────────────────
ANTHROPIC_API_KEY=[REPLACE: sk-ant-...]
OPENAI_API_KEY=[REPLACE: sk-... — only if used]

# ─────────────────────────────────────────────
# PAYMENTS
# ─────────────────────────────────────────────
STRIPE_SECRET_KEY=[REPLACE: sk_test_... or sk_live_...]
STRIPE_WEBHOOK_SECRET=[REPLACE: whsec_...]
STRIPE_PUBLISHABLE_KEY=[REPLACE: pk_test_... or pk_live_...]

# ─────────────────────────────────────────────
# EMAIL
# ─────────────────────────────────────────────
EMAIL_PROVIDER=[REPLACE: e.g., Resend / SendGrid / Postmark]
EMAIL_API_KEY=[REPLACE: your-email-api-key]
EMAIL_FROM=[REPLACE: hello@yourapp.com]

# ─────────────────────────────────────────────
# STORAGE
# ─────────────────────────────────────────────
STORAGE_PROVIDER=[REPLACE: e.g., AWS S3 / Cloudflare R2 / Supabase Storage]
STORAGE_BUCKET=[REPLACE: your-bucket-name]
STORAGE_ACCESS_KEY=[REPLACE: your-access-key]
STORAGE_SECRET_KEY=[REPLACE: your-secret-key]

# ─────────────────────────────────────────────
# MONITORING & ANALYTICS
# ─────────────────────────────────────────────
SENTRY_DSN=[REPLACE: https://...@sentry.io/...]
POSTHOG_KEY=[REPLACE: phc_... — for product analytics]
LOGTAIL_TOKEN=[REPLACE: your-logtail-token — for structured logging]

# ─────────────────────────────────────────────
# FEATURE FLAGS
# ─────────────────────────────────────────────
FEATURE_NEW_DASHBOARD=[REPLACE: true | false]
FEATURE_AI_ASSISTANT=[REPLACE: true | false]
```

---

### Secrets Storage by Environment

| Environment    | Where Secrets Are Stored                                             |
|----------------|----------------------------------------------------------------------|
| Local Dev      | `.env` file on your machine (gitignored)                            |
| CI/CD Pipeline | [REPLACE: e.g., GitHub Actions Secrets / GitLab CI Variables]       |
| Staging        | [REPLACE: e.g., Vercel Environment Variables / Railway Variables]   |
| Production     | [REPLACE: e.g., AWS Secrets Manager / Doppler / 1Password Secrets Automation] |

---

## 🌿 7. Branch Strategy & Git Conventions

<!--
INSTRUCTION: Define exactly how branches are named and how commits are written.
This prevents chaos in the Git history and makes AI tools (like Claude Code)
much better at generating meaningful commit messages.
-->

### Branch Structure

<!--
INSTRUCTION: Choose ONE branching model and delete the other.
Most solo developers and small teams: Git Flow Simplified (Option A).
Very fast-moving teams: Trunk-Based (Option B).
-->

**Branching model used:** [REPLACE: Git Flow Simplified / Trunk-Based / GitHub Flow]

| Branch Name      | Purpose                                            | Deploys To    | Who Pushes Directly? |
|------------------|----------------------------------------------------|---------------|----------------------|
| `main`           | Stable, production-ready code                     | Production    | CI/CD only           |
| `develop`        | Integration branch — all features merge here first | Staging       | CI/CD only           |
| `feat/*`         | New feature in progress (e.g., `feat/user-auth`)  | Nothing       | You                  |
| `fix/*`          | Bug fix (e.g., `fix/login-redirect-loop`)         | Nothing       | You                  |
| `chore/*`        | Config, dependency, or tooling updates             | Nothing       | You                  |
| `docs/*`         | Documentation updates only                        | Nothing       | You                  |
| `ai/*`           | Branches created or suggested by AI agents        | Nothing       | Claude / AI agent    |
| `hotfix/*`       | Critical production bug fix (bypasses develop)    | Production    | You + review         |
| `release/*`      | Preparing a release (e.g., `release/v1.2.0`)      | Staging       | You                  |

---

### Commit Message Format

<!--
INSTRUCTION: We use Conventional Commits — a simple standard that tools like
semantic-release, changelog generators, and Claude can understand.

FORMAT:
  <type>(<scope>): <short description>
  [blank line]
  [optional longer description]
  [optional footer: BREAKING CHANGE or closes #123]

TYPES:
  feat     → New feature for the user
  fix      → Bug fix for the user
  docs     → Documentation changes only
  style    → Formatting, missing semicolons (no logic change)
  refactor → Refactoring code (no new feature or bug fix)
  test     → Adding or fixing tests
  chore    → Build process, dependency updates, CI config
  perf     → Performance improvement
  ai       → Code or config generated/reviewed by an AI tool

SCOPES (fill in your project's scopes):
-->

**Commit format:** `<type>(<scope>): <description>`

**Examples:**
```
feat(auth): add Google OAuth login
fix(api): handle null user ID in profile endpoint
docs(repo): update folder structure diagram
chore(deps): bump next.js from 14.1.0 to 14.2.3
ai(tests): claude-generated unit tests for payment service
refactor(ui): extract Button into packages/ui
perf(db): add index on users.email for faster lookup
```

**Scopes used in this project:**

| Scope       | What It Refers To                                       |
|-------------|---------------------------------------------------------|
| `auth`      | [REPLACE: e.g., Authentication and authorization logic] |
| `api`       | [REPLACE: e.g., Backend API routes and controllers]     |
| `ui`        | [REPLACE: e.g., Frontend components and pages]          |
| `db`        | [REPLACE: e.g., Database models and migrations]         |
| `infra`     | [REPLACE: e.g., Docker, CI/CD, cloud config]            |
| `ai`        | [REPLACE: e.g., AI prompts, agent configs, AI features] |
| `docs`      | [REPLACE: e.g., Documentation files]                   |
| `[feature]` | [REPLACE: e.g., Your main feature names]                |

---

### Pull Request Rules

<!--
INSTRUCTION: List the rules every PR (Pull Request) must follow before merging.
-->

- [ ] **Branch name** follows the naming convention above
- [ ] **Commit messages** follow Conventional Commits format
- [ ] **All CI checks pass** (lint, type-check, tests)
- [ ] **No secrets or real credentials** in the diff
- [ ] **Self-review completed** — read your own diff before requesting review
- [ ] **PR description filled in** — what changed and why
- [ ] **Linked issue** — references the issue or task it closes (`Closes #123`)
- [ ] **AI review completed** — [REPLACE: e.g., Claude Code review passes / N/A]
- [ ] **Screenshots / recordings** attached for UI changes

**Minimum reviewers before merge:** [REPLACE: e.g., 1 (solo dev: self-review) / 2]

---

## 🤖 8. AI-Driven Workflow (Claude & Agents)

<!--
INSTRUCTION: This section explains how AI tools are woven into your development
process. Fill it in so that any AI agent reading this file knows exactly how to
behave in this project.
-->

### `CLAUDE.md` — AI Context File

<!--
INSTRUCTION: CLAUDE.md is a special file that Claude reads automatically when
you open this project in Claude Code. Think of it as a "briefing document"
for your AI pair-programmer.

Your CLAUDE.md should include:
  1. What this project does (1 paragraph)
  2. How to run it locally (exact commands)
  3. The tech stack (so Claude doesn't guess)
  4. Rules Claude must follow (coding style, what NOT to touch, etc.)
  5. Common tasks and how to do them (e.g., "to add a new API route, do X")

The CLAUDE.md in the root handles the whole monorepo.
Each app can also have its own CLAUDE.md for app-specific instructions.
-->

**Location of CLAUDE.md files:**

| File                   | Scope                                          |
|------------------------|------------------------------------------------|
| `/CLAUDE.md`           | Whole repository — read first on every session |
| `apps/web/CLAUDE.md`   | [REPLACE: Frontend-specific rules / Delete if not needed] |
| `apps/api/CLAUDE.md`   | [REPLACE: Backend-specific rules / Delete if not needed] |
| `apps/mobile/CLAUDE.md`| [REPLACE: Mobile-specific rules / Delete if not needed] |

---

### AI Tools Configured in This Project

<!--
INSTRUCTION: List every AI tool that has a config file in this repo.
-->

| AI Tool          | Config File Location              | What It's Used For                         |
|------------------|-----------------------------------|--------------------------------------------|
| Claude Code      | `CLAUDE.md`                       | [REPLACE: e.g., Coding assistant, PR review, test generation] |
| [REPLACE: Tool]  | [REPLACE: config file path]       | [REPLACE: What it does]                    |

---

### How AI Agents Interact With This Repository

<!--
INSTRUCTION: Describe the rules for AI agents so they don't cause havoc.
These rules also guide Claude when it runs in agentic mode.
-->

**What AI agents ARE allowed to do in this repo:**

- [REPLACE: e.g., ✅ Create and modify files inside `/apps`, `/packages`, `/ai/prompts`, `/tests`]
- [REPLACE: e.g., ✅ Write and run test commands]
- [REPLACE: e.g., ✅ Open pull requests to `develop`]
- [REPLACE: e.g., ✅ Add entries to `ai/decisions/`]

**What AI agents are NOT allowed to do:**

- [REPLACE: e.g., ❌ Push directly to `main` or `develop`]
- [REPLACE: e.g., ❌ Modify `.env` files or any secrets]
- [REPLACE: e.g., ❌ Delete files without creating a PR]
- [REPLACE: e.g., ❌ Deploy to production without human approval]
- [REPLACE: e.g., ❌ Modify `infrastructure/terraform/` without human review]

---

### AI-Generated Code Marking Convention

<!--
INSTRUCTION: When Claude or another AI generates a significant block of code,
mark it so future maintainers know it was AI-generated and should be reviewed.
-->

```typescript
// ⚡ AI-GENERATED — Generated by Claude on 2026-01-15
// Review before shipping to production.
// Original prompt: "Generate a function that validates email addresses"
function validateEmail(email: string): boolean {
  // ...
}
```

**Rule:** AI-generated code gets a `⚡ AI-GENERATED` comment on the first line,
with the date, tool, and the prompt that generated it.
Remove the comment once the code has been human-reviewed.

---

## 📅 9. Development Lifecycle Phases

<!--
INSTRUCTION: This section documents WHERE in the repository each phase of
development lives. Update it as you move through each phase.
-->

### Phase 1 — Idea → Spec → Architecture 🌱

<!--
INSTRUCTION: This phase is about capturing the "why" before writing any code.
Fill in where your planning documents live.
-->

**Status:** [REPLACE: ✅ Complete / 🔨 In Progress / 📋 Planned]

| Document                          | Location                                   | Description                              |
|-----------------------------------|--------------------------------------------|------------------------------------------|
| Product Requirements Doc (PRD)    | `docs/product/prd.md`                      | What we're building, for whom, and why   |
| User Stories / Job-to-be-done     | `docs/product/user-stories.md`             | "As a [user], I want to [do X] so that [Y]" |
| System Architecture Diagram       | `docs/architecture/system-design.md`       | High-level view of all components        |
| Database Schema / ERD             | `docs/architecture/database-schema.md`     | Tables, relationships, indexes           |
| API Contract                      | `docs/api/openapi.yaml` or Swagger URL     | Every endpoint, request, and response    |
| ADR #001 (first big decision)     | `docs/adr/001-initial-tech-stack.md`       | Why we picked this tech stack            |
| Competitive Research              | `docs/product/competitive-research.md`     | What alternatives exist, how we differ  |

**Key milestone:** When all documents above exist and are reviewed → move to Phase 2.

---

### Phase 2 — Development → Testing 🔨

<!--
INSTRUCTION: This is where code gets written. Fill in your source directories
and testing strategy.
-->

**Status:** [REPLACE: ✅ Complete / 🔨 In Progress / 📋 Planned]

**Development happens in:** `apps/`, `packages/`

**Feature development workflow:**
```
1. Create branch:    git checkout -b feat/feature-name
2. Write code:       Edit files in apps/ or packages/
3. Write tests:      Mirror structure in tests/ folder
4. Run locally:      [REPLACE: your start command]
5. Run tests:        [REPLACE: your test command]
6. Open PR:          To develop branch
7. AI review:        [REPLACE: e.g., Claude Code reviews automatically]
8. Merge:            After all checks pass
```

**Definition of "Done" for a feature:**
- [ ] Feature works end-to-end locally
- [ ] Unit tests written and passing (>= [REPLACE: e.g., 80%] coverage)
- [ ] Integration tests passing
- [ ] No TypeScript errors / no Python type errors
- [ ] Linter passes with zero warnings
- [ ] PR description written with "how to test" section
- [ ] Tested on mobile screen sizes (for UI features)
- [ ] AI code review passed
- [ ] Human self-review completed

---

### Phase 3 — CI/CD → Infrastructure → Deployment 🚀

<!--
INSTRUCTION: Describe exactly how code gets from your laptop to production.
Even if it's just one person, writing this down prevents mistakes.
-->

**Status:** [REPLACE: ✅ Complete / 🔨 In Progress / 📋 Planned]

#### Deployment Environments

| Environment | URL / Access                                         | Deploys When                           | Deployed By       |
|-------------|------------------------------------------------------|----------------------------------------|-------------------|
| Local Dev   | `localhost:[port]`                                   | You run `dev` command                  | You               |
| Preview     | [REPLACE: e.g., Auto-generated Vercel preview URL]   | Every PR opened                        | CI/CD             |
| Staging     | [REPLACE: e.g., https://staging.yourapp.com]         | Merge to `develop`                     | CI/CD             |
| Production  | [REPLACE: e.g., https://yourapp.com]                 | Merge to `main` + manual approval      | CI/CD + You       |

#### CI/CD Pipeline Steps

```
Push to branch
    ↓
[GitHub Actions / GitLab CI triggers]
    ↓
1. 📦 Install dependencies
2. 🔍 Run linter (ESLint / Ruff / Pylint)
3. 🏷️  Run type checker (tsc / mypy)
4. 🧪 Run unit tests
5. 🧪 Run integration tests
6. 🏗️  Build production bundle
7. 🤖 AI code review (Claude)    ← AI-specific step
8. ✅ All checks passed?
    → YES: Deploy to environment
    → NO:  Block merge, notify author
```

#### Infrastructure Overview

| Service / Resource          | Provider                      | Purpose                                    |
|-----------------------------|-------------------------------|--------------------------------------------|
| Frontend hosting            | [REPLACE: e.g., Vercel]       | [REPLACE: Hosts the Next.js web app]       |
| Backend hosting             | [REPLACE: e.g., Railway]      | [REPLACE: Hosts the API server]            |
| Database                    | [REPLACE: e.g., Supabase]     | [REPLACE: PostgreSQL + Auth + Storage]     |
| File storage                | [REPLACE: e.g., Cloudflare R2]| [REPLACE: User uploads, images]            |
| Email                       | [REPLACE: e.g., Resend]       | [REPLACE: Transactional emails]            |
| CDN                         | [REPLACE: e.g., Cloudflare]   | [REPLACE: Edge caching, DDoS protection]  |
| Monitoring / Errors         | [REPLACE: e.g., Sentry]       | [REPLACE: Error tracking and alerting]    |
| Analytics                   | [REPLACE: e.g., PostHog]      | [REPLACE: Product analytics, funnels]     |
| Feature flags               | [REPLACE: e.g., PostHog / GrowthBook] | [REPLACE: Control feature rollout] |

---

### Phase 4 — Post-Launch → Monitoring → Growth 📈

<!--
INSTRUCTION: This phase covers everything AFTER your first deployment.
It's often neglected but critical for reaching your first 500 customers.
-->

**Status:** [REPLACE: ✅ Complete / 🔨 In Progress / 📋 Planned]

**Launch date:** [REPLACE: YYYY-MM-DD — or "Not launched yet"]
**Current customer count:** [REPLACE: e.g., 0 / 47 / 312]
**Target:** 500 paying customers

#### Monitoring & Alerting Setup

| What We Monitor               | Tool / Location                              | Alert When                                 |
|-------------------------------|----------------------------------------------|--------------------------------------------|
| Application errors            | [REPLACE: e.g., Sentry]                      | [REPLACE: e.g., Error rate > 1% in 5 min] |
| API response times            | [REPLACE: e.g., Grafana / Datadog]           | [REPLACE: e.g., p99 latency > 2 seconds]  |
| Server uptime                 | [REPLACE: e.g., Better Uptime / UptimeRobot] | [REPLACE: e.g., Downtime > 1 minute]      |
| Database query performance    | [REPLACE: e.g., Supabase Dashboard]          | [REPLACE: e.g., Slow query > 500ms]       |
| User funnel drop-off          | [REPLACE: e.g., PostHog]                     | [REPLACE: e.g., Signup-to-activation < 30%] |
| Revenue & churn               | [REPLACE: e.g., Stripe Dashboard]            | [REPLACE: e.g., New failed payments]      |

#### Feedback & Iteration Loop

```
User uses product
    ↓
Feedback collected via: [REPLACE: e.g., in-app widget / Typeform / email]
    ↓
Feedback lands in: [REPLACE: e.g., Notion database / Linear / GitHub Issues]
    ↓
AI summarizes feedback weekly (Claude agent) → docs/user-research/
    ↓
Prioritized in: [REPLACE: e.g., Linear / GitHub Projects / Notion roadmap]
    ↓
New feature spec written → docs/product/
    ↓
Back to Phase 2 (Development)
```

#### Changelog

All changes visible to users are documented in `docs/changelog/`:

```
docs/changelog/
├── v1.0.0.md    ← Initial launch
├── v1.1.0.md    ← First batch of bug fixes
└── v1.2.0.md    ← First feature from user feedback
```

**Format of each changelog entry:**
```markdown
# v1.1.0 — 2026-02-01

## ✨ New
- Added dark mode support
- Exported data as CSV

## 🐛 Fixed
- Login redirect loop on Safari
- Email confirmation link expiry extended to 48h

## 🗑️ Removed
- Legacy onboarding wizard (replaced by new flow)
```

#### Road to 500 Customers — Milestone Tracker

| Milestone                  | Target Date           | Status         | Notes                        |
|----------------------------|-----------------------|----------------|------------------------------|
| First internal demo ready  | [REPLACE: YYYY-MM-DD] | [REPLACE: ⬜/✅] | [REPLACE]                    |
| Private beta (10 users)    | [REPLACE: YYYY-MM-DD] | [REPLACE: ⬜/✅] | [REPLACE]                    |
| Public beta launch         | [REPLACE: YYYY-MM-DD] | [REPLACE: ⬜/✅] | [REPLACE]                    |
| First paying customer      | [REPLACE: YYYY-MM-DD] | [REPLACE: ⬜/✅] | [REPLACE]                    |
| 50 customers               | [REPLACE: YYYY-MM-DD] | [REPLACE: ⬜/✅] | [REPLACE]                    |
| 100 customers              | [REPLACE: YYYY-MM-DD] | [REPLACE: ⬜/✅] | [REPLACE]                    |
| 250 customers              | [REPLACE: YYYY-MM-DD] | [REPLACE: ⬜/✅] | [REPLACE]                    |
| **500 customers** 🎉        | [REPLACE: YYYY-MM-DD] | [REPLACE: ⬜/✅] | [REPLACE]                    |

---

## 🔧 10. Onboarding: Up & Running in 10 Minutes

<!--
INSTRUCTION: This is the MOST IMPORTANT section for anyone (human or AI)
who is new to this project. Write it assuming the reader has never seen this
codebase before. Be specific with every command.
-->

### Prerequisites

Before you start, install these on your machine:

| Tool           | Minimum Version    | Install Guide                                    | Check Installed         |
|----------------|--------------------|--------------------------------------------------|-------------------------|
| Node.js        | [REPLACE: e.g., 20.x LTS] | https://nodejs.org                        | `node --version`        |
| pnpm / npm     | [REPLACE: e.g., pnpm 9.x] | `npm install -g pnpm`                    | `pnpm --version`        |
| Python         | [REPLACE: e.g., 3.12+] | https://python.org — or use pyenv          | `python --version`      |
| Docker Desktop | [REPLACE: e.g., 4.x] | https://www.docker.com/products/docker-desktop | `docker --version`    |
| Git            | 2.x+               | https://git-scm.com                              | `git --version`         |
| [REPLACE]      | [REPLACE]          | [REPLACE]                                        | [REPLACE]               |

---

### Step-by-Step Setup

<!--
💡 TIP: Every command below should work EXACTLY as written.
Test them yourself on a clean machine before finalizing this document.
-->

**Step 1 — Clone the repository**
```bash
git clone [REPLACE: https://github.com/your-org/your-repo.git]
cd [REPLACE: your-repo-name]
```

**Step 2 — Install dependencies**
```bash
[REPLACE: e.g., pnpm install   OR   npm install   OR   pip install -r requirements.txt]
```

**Step 3 — Set up environment variables**
```bash
# Copy the example env file — then open .env and fill in real values
cp .env.example .env

# Open the file and fill in your values:
# → Get your DATABASE_URL from: [REPLACE: e.g., Supabase dashboard → Settings → Database]
# → Get your ANTHROPIC_API_KEY from: https://console.anthropic.com
# → Leave STRIPE_* keys empty if you're not testing payments yet
```

**Step 4 — Start the database**
```bash
[REPLACE: e.g., docker-compose up -d db   OR   supabase start   OR   N/A — using hosted DB]
```

**Step 5 — Run database migrations**
```bash
[REPLACE: e.g., pnpm db:migrate   OR   python manage.py migrate   OR   supabase db push]
```

**Step 6 — Seed with test data (optional but recommended)**
```bash
[REPLACE: e.g., pnpm db:seed   OR   python scripts/seed.py   OR   Skip if not available]
```

**Step 7 — Start the development server**
```bash
[REPLACE: e.g., pnpm dev   OR   npm run dev   OR   uvicorn main:app --reload]
```

**Step 8 — Open in your browser**
```
Web app:   http://localhost:[REPLACE: 3000]
API docs:  http://localhost:[REPLACE: 8000]/docs
Admin:     http://localhost:[REPLACE: 3001]
```

**Step 9 — Run the test suite to verify everything works**
```bash
[REPLACE: e.g., pnpm test   OR   pytest   OR   npm run test]
```

**✅ You're ready!** All tests should pass. If something fails, check:
1. Is Docker running? (`docker ps`)
2. Are all env variables filled in? (check `.env`)
3. Did you run migrations? (Step 5)
4. See [REPLACE: link to troubleshooting doc or issue tracker]

---

### First Things to Read

When you're up and running, read these files in order:

1. `README.md` — Project overview
2. `CLAUDE.md` — How AI tools work in this project
3. `docs/architecture/system-design.md` — How everything connects
4. `docs/api/` — API documentation
5. This file — You're already here! ✅

---

## 🛡️ 11. Post-Launch: Road to 500 Customers

<!--
INSTRUCTION: This section is a living document. Update it as you grow.
It captures the operational knowledge your future self (or a new hire) will need.
-->

### Runbooks — "What Do I Do When X Happens?"

<!--
INSTRUCTION: A runbook is a step-by-step guide for handling a specific
operational situation. Even if you're solo, writing these saves you at 2am
when something breaks.
Runbooks live in: docs/runbooks/
-->

| Situation                        | Runbook File                                    | Last Tested         |
|----------------------------------|-------------------------------------------------|---------------------|
| Production is down               | `docs/runbooks/production-outage.md`            | [REPLACE: YYYY-MM-DD] |
| Database is slow / full          | `docs/runbooks/database-emergency.md`           | [REPLACE: YYYY-MM-DD] |
| Roll back a bad deployment       | `docs/runbooks/rollback-deployment.md`          | [REPLACE: YYYY-MM-DD] |
| Rotate a compromised secret      | `docs/runbooks/rotate-secrets.md`               | [REPLACE: YYYY-MM-DD] |
| User reports data issue          | `docs/runbooks/user-data-incident.md`           | [REPLACE: YYYY-MM-DD] |
| Scale up for traffic spike       | `docs/runbooks/scale-up.md`                     | [REPLACE: YYYY-MM-DD] |

---

### Key Metrics We Track

<!--
INSTRUCTION: Define the metrics that tell you if the product is healthy.
These drive every product decision from 0 to 500 customers.
-->

| Metric                      | Definition                                           | Where to Find It      | Current Value   |
|-----------------------------|------------------------------------------------------|-----------------------|-----------------|
| MRR (Monthly Recurring Revenue) | Total monthly subscription revenue                | [REPLACE: Stripe]     | [REPLACE: $0]   |
| Activation rate             | % of signups who complete the core action within 7d  | [REPLACE: PostHog]    | [REPLACE: —%]   |
| Churn rate                  | % of customers who cancel each month                 | [REPLACE: Stripe]     | [REPLACE: —%]   |
| NPS                         | Net Promoter Score from in-app survey                | [REPLACE: Typeform]   | [REPLACE: —]    |
| API p95 latency             | 95th percentile API response time                    | [REPLACE: Grafana]    | [REPLACE: —ms]  |
| Weekly active users (WAU)   | Unique users who take a core action in 7 days        | [REPLACE: PostHog]    | [REPLACE: 0]    |
| Support ticket volume       | New support tickets per week                         | [REPLACE: Linear]     | [REPLACE: 0]    |

---

## 📐 12. Maintenance & Governance

<!--
INSTRUCTION: Who owns this repo? How are decisions made? How is this file kept up to date?
-->

### Ownership

| Role                      | Person / Team                   | Responsibilities                             |
|---------------------------|---------------------------------|----------------------------------------------|
| Repository Owner          | [REPLACE: Name / Email]         | Final say on architecture and structure      |
| AI Workflow Owner         | [REPLACE: Name / "Same as above"] | Manages CLAUDE.md, prompts, agent configs  |
| Infrastructure Owner      | [REPLACE: Name / "Same as above"] | Cloud config, secrets, deployments         |
| Documentation Owner       | [REPLACE: Name / "Same as above"] | Keeps this file and /docs up to date       |

---

### How to Keep This Document Current

This document MUST be updated when:

- [ ] A new folder is added to the repository
- [ ] A folder is renamed or deleted
- [ ] A new environment variable is added
- [ ] The deployment process changes
- [ ] A new AI tool or agent is added
- [ ] The team composition changes
- [ ] A major dependency is added or removed
- [ ] The branch strategy changes

**Update cadence:** [REPLACE: e.g., Reviewed and updated every sprint (2 weeks) / On every structural change]

**Who reviews this document:** [REPLACE: e.g., Repository owner on every PR that changes the structure]

---

### Dependency Upgrade Policy

| Dependency Type           | How Often to Update              | Who Does It                     |
|---------------------------|----------------------------------|---------------------------------|
| Security patches          | Within 48 hours of disclosure    | [REPLACE: You / Automated PR]   |
| Minor versions            | [REPLACE: e.g., Monthly]         | [REPLACE: You]                  |
| Major versions            | [REPLACE: e.g., Quarterly, after testing in staging] | [REPLACE: You] |
| AI model versions         | [REPLACE: e.g., When new stable version is released] | [REPLACE: You] |

---

## 📖 13. Glossary for Beginners

<!--
INSTRUCTION: Keep this section! It makes the document friendly to anyone —
including a 10-year-old or someone brand new to software development.
Add any project-specific terms below the general ones.
-->

| Term                 | Plain English Explanation                                                         |
|----------------------|-----------------------------------------------------------------------------------|
| **Repository (repo)**| The folder that holds all your project's code and history. Like a super-powered folder on GitHub. |
| **Monorepo**         | One big folder that contains ALL parts of your project (website, app, backend, etc.) |
| **Polyrepo**         | Each part of your project lives in its own separate folder on GitHub.             |
| **Branch**           | A safe copy of the code where you can make changes without breaking the main version. |
| **PR (Pull Request)**| A request to merge your branch's changes into the main code. Like asking for approval. |
| **CI/CD**            | Automatic robots that test your code and deploy it to the internet when you push changes. |
| **Environment variables** | Secret settings your app needs to run (like passwords). Stored in `.env` files. |
| **`.gitignore`**     | A list of files Git should NEVER track or upload (like your `.env` with real passwords). |
| **API**              | A way for two parts of an app to talk to each other. Like a waiter taking orders between you (frontend) and the kitchen (backend). |
| **Migration**        | A script that changes the shape of your database (adds a column, creates a table). |
| **ADR**              | Architecture Decision Record — a document explaining WHY a technical choice was made. |
| **Linter**           | A tool that reads your code and tells you about style mistakes before they cause bugs. |
| **CLAUDE.md**        | A special file that tells the Claude AI assistant everything it needs to know about your project. |
| **Prompt**           | The instructions you give to an AI tool to get it to do something specific.       |
| **Agent**            | An AI tool that can do multiple steps on its own without you asking for each step. |
| **Staging**          | A test version of your app that looks exactly like production but is used for testing. |
| **Production (prod)**| The real, live version of your app that customers actually use.                   |
| **Seed data**        | Fake but realistic data loaded into your database for development and testing.    |
| **Runbook**          | A step-by-step guide for doing a specific operational task (like fixing a crash). |
| **MRR**              | Monthly Recurring Revenue — how much money you make from subscriptions per month. |
| **NPS**              | Net Promoter Score — a number (−100 to 100) that shows how much users love your product. |
| **WAU**              | Weekly Active Users — how many unique people use your product in a given week.    |
| **p95 / p99 latency**| How long the slowest 5% (or 1%) of requests take. A health check for your API speed. |
| **[REPLACE: term]**  | [REPLACE: Add your project-specific jargon here]                                  |

---

<!--
════════════════════════════════════════════════════════════════════════════════
  🎉 CONGRATULATIONS — YOU MADE IT TO THE END!
════════════════════════════════════════════════════════════════════════════════

If you filled out every [REPLACE] field above, you now have a world-class
repository structure document that:

  ✅ Any teammate can read and understand in 10 minutes
  ✅ Claude and other AI tools can use as a project briefing
  ✅ Covers your project from first idea to 500 customers
  ✅ Serves as a living contract for how this repo works

NEXT STEPS:
  1. Commit this file to the root of your repo
  2. Create a CLAUDE.md file (the AI context file referenced above)
  3. Create the folders listed in Section 3 that don't exist yet
  4. Share this file with your first collaborator or with Claude Code

REVIEW REMINDER:
  Update this file whenever the structure changes.
  Stale documentation is worse than no documentation.
════════════════════════════════════════════════════════════════════════════════
-->

---

*Template version: 1.0.0 · Last updated: 2026-10-14 · Maintained by: [REPLACE: Your Name]*
*Generated with the AI-Driven Development Life Cycle framework · Compatible with Claude Code*
