# 📖 HOW TO FILL THIS DOCUMENT
> **Read this section first before touching anything else.**

This is your team's **living Coding Standards document**. It tells every developer (and every AI tool)
exactly how code should be written, reviewed, committed, secured, and shipped in your projects.

### ✅ Step-by-Step Filling Guide

| Step | What to Do | Where |
|------|------------ |-------|
| 1 | Replace every `[BRACKETED PLACEHOLDER]` with your real value | Throughout the doc |
| 2 | Delete any section that does NOT apply to your project | Whole section |
| 3 | Keep every `<!-- NOTE: -->` comment while filling — delete them after | Inline in sections |
| 4 | Run a search for `TODO:` before your first commit — every TODO must be resolved | Your text editor |
| 5 | Tag this file in GitHub as a **Required Read** for all new contributors | GitHub repo settings |
| 6 | Review and update this document at the start of every sprint / major milestone | Calendar reminder |

> 💡 **Beginner tip:** Anything inside `[square brackets]` is a blank you must fill in.
> Anything inside `<!-- HTML comments -->` is a hint just for you — it won't show in rendered Markdown.

---

# Coding Standards
<!-- NOTE: This is the official coding standards document. Version-control it alongside your source code. -->

| Field | Value |
|-------|-------|
| **Document Version** | `[e.g., v1.0.0]` |
| **Last Updated** | `[YYYY-MM-DD]` |
| **Author(s)** | `[Your Name / Handle]` |
| **Applies To** | `[Project Name(s) or "All Projects"]` |
| **Status** | `[ ] Draft  [ ] Under Review  [x] Active  [ ] Deprecated` |

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Tech Stack Declaration](#2-tech-stack-declaration)
3. [AI-Assisted Development Policy](#3-ai-assisted-development-policy)
4. [Naming Conventions](#4-naming-conventions)
5. [Code Structure & Architecture](#5-code-structure--architecture)
6. [Git & Branching Strategy](#6-git--branching-strategy)
7. [Code Review Standards](#7-code-review-standards)
8. [Testing Standards](#8-testing-standards)
9. [Security & Secrets Handling](#9-security--secrets-handling)
10. [Environment Configuration](#10-environment-configuration)
11. [Documentation Standards](#11-documentation-standards)
12. [Error Handling & Logging](#12-error-handling--logging)
13. [Performance Standards](#13-performance-standards)
14. [Accessibility Standards](#14-accessibility-standards)
15. [Dependencies & Package Management](#15-dependencies--package-management)
16. [Deployment & Release Process](#16-deployment--release-process)
17. [Monitoring & Observability](#17-monitoring--observability)
18. [First 500 Customers — Quality Gates](#18-first-500-customers--quality-gates)
19. [Compliance & Audit Trail](#19-compliance--audit-trail)
20. [Appendix & References](#20-appendix--references)

---

## 1. Project Overview

<!-- NOTE: Describe your project in plain English. A new team member (or an AI agent) reading this should
     understand what the product does, who it's for, and why these standards exist — within 2 minutes. -->

### 1.1 What We're Building

> **Product Name:** `[e.g., "Acme Finance App"]`
>
> **One-line description:** `[e.g., "A mobile-first personal finance tracker for Gen Z users."]`
>
> **Who uses it:** `[e.g., "End consumers aged 18–30 on iOS and Android"]`
>
> **Current phase:** `[ ] Idea  [ ] MVP  [ ] Beta  [x] Production  [ ] Growth`

### 1.2 Why This Document Exists

This document ensures that:
- Every developer (human or AI agent) writes code that looks and behaves consistently.
- Security, performance, and quality are never an afterthought.
- The codebase remains maintainable as the team or AI tooling scales.
- We can onboard a new contributor in under 30 minutes.

### 1.3 Scope

<!-- NOTE: List every repository or sub-project that follows this standard. -->

| Repository | Description | Primary Language |
|------------|-------------|-----------------|
| `[repo-name-1]` | `[e.g., "Next.js web app"]` | `[TypeScript]` |
| `[repo-name-2]` | `[e.g., "React Native mobile app"]` | `[TypeScript / Swift / Kotlin]` |
| `[repo-name-3]` | `[e.g., "Python API service"]` | `[Python]` |

---

## 2. Tech Stack Declaration

<!-- NOTE: Fill in ONLY the technologies you actually use. Delete rows that don't apply. -->

### 2.1 Frontend (Web)

| Layer | Technology | Version |
|-------|-----------|---------|
| Framework | `[React / Next.js / Vue]` | `[e.g., Next.js 14+]` |
| Language | TypeScript | `[e.g., 5.x]` |
| Styling | `[Tailwind CSS / CSS Modules / styled-components]` | `[version]` |
| State Management | `[Zustand / Redux / Jotai / React Query]` | `[version]` |
| UI Component Library | `[shadcn/ui / Radix / MUI]` | `[version]` |
| Testing | `[Vitest / Jest + React Testing Library]` | `[version]` |
| Bundler | `[Vite / Webpack / Turbopack]` | `[version]` |

### 2.2 Mobile

| Layer | Technology | Version |
|-------|-----------|---------|
| Framework | `[React Native / Flutter / Native Swift + Kotlin]` | `[version]` |
| Language (iOS) | Swift | `[e.g., 5.9+]` |
| Language (Android) | Kotlin | `[e.g., 1.9+]` |
| Navigation | `[React Navigation / Expo Router]` | `[version]` |
| Testing | `[Detox / XCTest / Espresso]` | `[version]` |

### 2.3 Backend & APIs

| Layer | Technology | Version |
|-------|-----------|---------|
| Runtime | `[Node.js / Python]` | `[e.g., Node 20 LTS]` |
| Framework | `[Fastify / NestJS / FastAPI]` | `[version]` |
| Language | `[TypeScript / Python 3.11+]` | `[version]` |
| ORM / Query Builder | `[Prisma / Drizzle / SQLAlchemy]` | `[version]` |
| API Style | `[REST / GraphQL / tRPC]` | — |

### 2.4 BaaS & Infrastructure

| Service | Purpose | Provider |
|---------|---------|---------|
| `[Supabase / Firebase]` | Auth, DB, Storage | `[Supabase / Google]` |
| `[Cloudflare Workers / Pages]` | Edge compute / CDN | Cloudflare |
| `[AWS S3 / GCP Cloud Storage]` | File storage | `[AWS / GCP / Azure]` |
| `[Vercel / Netlify]` | Frontend deployment | `[Vercel]` |
| `[App Store Connect / Google Play Console]` | Mobile distribution | Apple / Google |

### 2.5 AI Tooling

| Tool | Role | Model |
|------|------|-------|
| Claude (Anthropic) | Primary coding assistant, code review, doc generation | `[claude-opus-5-5 / claude-sonnet-5-5]` |
| `[Other tool if any]` | `[Role]` | `[Model]` |

---

## 3. AI-Assisted Development Policy

<!-- NOTE: This is one of the most important sections for 2024+ projects. Fill it carefully.
     It protects you legally, keeps quality high, and makes AI a reliable teammate — not a liability. -->

### 3.1 Guiding Principle

> **AI writes first drafts. Humans own the final code.**
>
> Every line of AI-generated code that enters `main` or `production` has been read, understood,
> and approved by a human developer. "AI wrote it" is never a defence for a bug, security hole, or poor design.

### 3.2 Approved AI Tools

| Tool | Allowed For | NOT Allowed For |
|------|------------|----------------|
| Claude (claude.ai / API) | Scaffolding, refactoring, docs, test generation, code review | Committing unreviewed code, storing secrets, accessing production DBs |
| `[GitHub Copilot]` | In-editor suggestions | Auto-accepting multi-file changes without review |

### 3.3 Prompt Standards

When using Claude or any LLM for code generation, always include the following in your prompt:

```
CONTEXT:
- Project: [Project Name]
- Stack: [e.g., Next.js 14, TypeScript, Supabase]
- File being modified: [path/to/file.ts]
- Our coding standard doc: [link or paste relevant section]

TASK:
[Describe exactly what you want the AI to do]

CONSTRAINTS:
- Follow our naming conventions (see §4 of Coding_Standards.md)
- No inline secrets or hardcoded values
- Must include JSDoc / TSDoc comments
- Output only the changed code block, not the whole file unless asked
```

<!-- NOTE: Save your best prompts in a /prompts directory at the root of your repo.
     Name them: [feature]_[purpose].md, e.g., auth_generate_login_flow.md -->

### 3.4 AI Code Review Checklist

Before merging ANY AI-generated code, the human reviewer must check:

- [ ] **Understood** — I have read every line and understand what it does.
- [ ] **Logic verified** — The logic is correct and not just plausible-sounding.
- [ ] **No hallucinated imports** — Every import/package actually exists in `package.json` / `requirements.txt`.
- [ ] **No secrets** — No API keys, tokens, passwords, or PII in the diff.
- [ ] **Tests added** — AI-generated logic has at least one unit test written or reviewed by a human.
- [ ] **Edge cases handled** — Null/undefined, empty arrays, 0, negative numbers, long strings considered.
- [ ] **Error handling present** — try/catch or equivalent is in place where needed.
- [ ] **Consistent style** — Naming, formatting, and structure match §4 of this document.
- [ ] **No over-engineering** — The simplest solution is preferred over a clever one.

### 3.5 AI Code Attribution

<!-- NOTE: Pick one attribution style and stick with it across all repos. -->

Every function, class, or module that was substantially written by AI must include an attribution comment:

```typescript
/**
 * @ai-generated Claude (claude-sonnet-5-5) — [YYYY-MM-DD]
 * @reviewed-by [Your Name / GitHub handle]
 * @review-date [YYYY-MM-DD]
 * @prompt-ref prompts/[prompt-file-name].md
 */
```

### 3.6 AI Agent Autonomy Levels

<!-- NOTE: Define how much autonomy AI agents are allowed. This prevents surprises. -->

| Level | What the AI Can Do | Human Gate Required? |
|-------|--------------------|----------------------|
| **L1 — Read** | Read files, answer questions | No |
| **L2 — Suggest** | Propose code changes, write to a draft branch | No |
| **L3 — Commit** | Commit code to a feature branch | PR review required |
| **L4 — Deploy** | Deploy to staging | Approval required |
| **L5 — Production** | Any production action | 🚫 NEVER without explicit human approval |

> **Default level for Claude in this project:** `[L2 / L3]`

---

## 4. Naming Conventions

<!-- NOTE: Consistency here saves hours of debugging. Pick ONE option per row and delete the others.
     Then document why — future-you will thank present-you. -->

### 4.1 Universal Rules

1. **No abbreviations** unless they are universally understood (e.g., `url`, `id`, `api`, `db`).
2. **No single-letter variables** except in loops (`i`, `j`, `k`) or math-heavy functions.
3. **No magic numbers** — replace `86400` with a constant `SECONDS_IN_A_DAY`.
4. **English only** — All identifiers, comments, and commit messages must be in English.
5. **Be descriptive** — `getUserByEmailAndStatus` is better than `getUser2`.

### 4.2 JavaScript / TypeScript

| Construct | Convention | ✅ Good | ❌ Bad |
|-----------|-----------|--------|--------|
| Variables | `camelCase` | `userProfile` | `UserProfile`, `user_profile` |
| Functions | `camelCase` | `fetchUserData()` | `FetchUserData()`, `fetch_user_data()` |
| Classes | `PascalCase` | `UserAuthService` | `userAuthService`, `user_auth_service` |
| Constants | `SCREAMING_SNAKE_CASE` | `MAX_RETRY_COUNT` | `maxRetryCount`, `Max_Retry` |
| Interfaces | `PascalCase` (no `I` prefix) | `UserProfile` | `IUserProfile`, `userProfile` |
| Types | `PascalCase` | `ApiResponse<T>` | `apiResponse`, `api_response` |
| Enums | `PascalCase` (members in `SCREAMING_SNAKE_CASE`) | `enum Role { ADMIN, USER }` | `enum role { admin, user }` |
| React Components | `PascalCase` | `UserProfileCard` | `userProfileCard` |
| React Hooks | `camelCase` prefixed with `use` | `useAuthState` | `AuthState`, `authState` |
| Event Handlers | `camelCase` prefixed with `handle` | `handleSubmitForm` | `onSubmit`, `submitHandler` |
| Boolean variables | Start with `is`, `has`, `can`, `should` | `isLoading`, `hasPermission` | `loading`, `permission` |
| Async functions | No special prefix (avoid `async` suffix) | `fetchUserById` | `asyncFetchUser`, `getUserAsync` |

### 4.3 Python

| Construct | Convention | ✅ Good | ❌ Bad |
|-----------|-----------|--------|--------|
| Variables | `snake_case` | `user_profile` | `userProfile`, `UserProfile` |
| Functions | `snake_case` | `fetch_user_data()` | `fetchUserData()` |
| Classes | `PascalCase` | `UserAuthService` | `user_auth_service` |
| Constants | `SCREAMING_SNAKE_CASE` | `MAX_RETRY_COUNT` | `max_retry_count` |
| Private methods | `_single_leading_underscore` | `_validate_token()` | `validateToken()` |
| Module-private | `__double_leading_underscore` | `__secret_key` | `secretKey` |
| Type hints | Always required on public functions | `def get_user(id: str) -> User:` | `def get_user(id):` |

### 4.4 Swift (iOS)

| Construct | Convention | ✅ Good | ❌ Bad |
|-----------|-----------|--------|--------|
| Variables & Properties | `camelCase` | `userProfile` | `UserProfile` |
| Functions & Methods | `camelCase` | `fetchUserData()` | `FetchUserData()` |
| Classes / Structs / Enums | `PascalCase` | `UserProfileView` | `userProfileView` |
| Protocols | `PascalCase` + describe capability | `UserFetchable` | `IUserFetch`, `UserFetch` |
| Constants | `camelCase` (module-level: `PascalCase`) | `let maxRetryCount = 3` | `let MAX_RETRY_COUNT = 3` |
| SwiftUI Views | `PascalCase` ending with `View` | `UserProfileView` | `UserProfile`, `ProfileScreen` |

### 4.5 Kotlin (Android)

| Construct | Convention | ✅ Good | ❌ Bad |
|-----------|-----------|--------|--------|
| Variables | `camelCase` | `userProfile` | `UserProfile`, `user_profile` |
| Functions | `camelCase` | `fetchUserData()` | `FetchUserData()` |
| Classes | `PascalCase` | `UserRepository` | `userRepository` |
| Constants | `SCREAMING_SNAKE_CASE` in companion object | `companion object { const val MAX = 3 }` | `val max = 3` |
| Composables | `PascalCase` | `UserProfileCard` | `userProfileCard` |

### 4.6 Files & Folders

| Item | Convention | ✅ Good | ❌ Bad |
|------|-----------|--------|--------|
| React component files | `PascalCase.tsx` | `UserProfileCard.tsx` | `userProfileCard.tsx`, `user-profile-card.tsx` |
| Utility / helper files | `camelCase.ts` | `formatDate.ts` | `FormatDate.ts`, `format-date.ts` |
| Config / env files | `kebab-case` or `UPPER_SNAKE_CASE` | `.env.local`, `next.config.ts` | `NextConfig.ts` |
| Test files | Same name as source + `.test` or `.spec` | `UserProfileCard.test.tsx` | `test_UserProfileCard.tsx` |
| API route files (Next.js) | `route.ts` inside `[resource]/` folder | `app/users/[id]/route.ts` | `userRoute.ts` |
| Python modules | `snake_case.py` | `user_service.py` | `UserService.py` |
| Swift files | `PascalCase.swift` | `UserProfileView.swift` | `userProfileView.swift` |
| Folders | `kebab-case` | `user-profile/` | `UserProfile/`, `userProfile/` |
| Environment files | `.env.[environment]` | `.env.local`, `.env.staging` | `env.txt`, `config.js` |

### 4.7 Database & API

| Item | Convention | ✅ Good | ❌ Bad |
|------|-----------|--------|--------|
| Table names | `snake_case`, plural | `user_profiles` | `UserProfiles`, `userProfile` |
| Column names | `snake_case` | `created_at`, `user_id` | `createdAt`, `UserID` |
| Primary keys | `id` (UUID preferred) | `id UUID DEFAULT gen_random_uuid()` | `userId`, `pk` |
| Foreign keys | `[table_singular]_id` | `user_id`, `order_id` | `userId`, `fkUser` |
| API endpoints (REST) | `kebab-case`, plural nouns | `GET /user-profiles/{id}` | `GET /getUser`, `GET /UserProfiles` |
| GraphQL types | `PascalCase` | `type UserProfile { ... }` | `type userProfile` |
| GraphQL fields | `camelCase` | `firstName`, `createdAt` | `first_name`, `created_at` |
| Event / message names | `SCREAMING_SNAKE_CASE` | `USER_PROFILE_UPDATED` | `userProfileUpdated` |

---

## 5. Code Structure & Architecture

<!-- NOTE: Pick the folder structure that matches your chosen framework. Delete the others. -->

### 5.1 Next.js (App Router) Folder Structure

```
[project-name]/
├── app/                        # Next.js App Router
│   ├── (auth)/                 # Route group: authentication pages
│   │   ├── login/page.tsx
│   │   └── register/page.tsx
│   ├── (dashboard)/            # Route group: protected pages
│   │   └── profile/page.tsx
│   ├── api/                    # API routes
│   │   └── users/
│   │       └── [id]/route.ts
│   ├── layout.tsx              # Root layout
│   └── globals.css
├── components/
│   ├── ui/                     # Reusable, dumb UI components (shadcn etc.)
│   └── features/               # Feature-specific smart components
│       └── auth/
│           └── LoginForm.tsx
├── lib/                        # Shared utilities, helpers, configs
│   ├── utils.ts
│   ├── validations.ts
│   └── constants.ts
├── hooks/                      # Custom React hooks
├── services/                   # External API calls, BaaS wrappers
│   ├── supabase.ts
│   └── userService.ts
├── store/                      # Global state (Zustand slices etc.)
├── types/                      # TypeScript types & interfaces
├── prompts/                    # 🤖 AI prompt library (see §3.3)
├── __tests__/                  # Test files (mirror src structure)
├── .env.local                  # Local secrets (NEVER committed)
├── .env.example                # Template for env vars (ALWAYS committed)
├── Coding_Standards.md         # This file
└── README.md
```

### 5.2 React Native / Expo Folder Structure

```
[mobile-project-name]/
├── app/                        # Expo Router screens
│   ├── (tabs)/
│   │   ├── index.tsx
│   │   └── profile.tsx
│   └── _layout.tsx
├── components/
│   ├── ui/
│   └── features/
├── hooks/
├── services/
├── store/
├── types/
├── prompts/                    # 🤖 AI prompt library
├── __tests__/
├── .env.local
├── .env.example
└── app.config.ts
```

### 5.3 Python API Service Folder Structure

```
[api-service-name]/
├── app/
│   ├── api/
│   │   └── v1/
│   │       └── users.py
│   ├── core/
│   │   ├── config.py           # Pydantic settings
│   │   └── security.py
│   ├── models/                 # Database models
│   ├── schemas/                # Pydantic request/response schemas
│   ├── services/               # Business logic
│   └── main.py
├── tests/
├── prompts/                    # 🤖 AI prompt library
├── .env.example
├── requirements.txt
└── Dockerfile
```

### 5.4 Component Rules

1. **One component per file.** No exceptions.
2. **Smart vs. Dumb components:**
   - `components/ui/` — presentational only, no data fetching, no business logic.
   - `components/features/` — can fetch data, use hooks, contain business logic.
3. **Max component length:** 200 lines. If longer, split into sub-components.
4. **Props interface** must be declared immediately above the component:

```typescript
// ✅ Correct
interface UserProfileCardProps {
  userId: string;
  showEmail?: boolean;
  onEditClick: (userId: string) => void;
}

export function UserProfileCard({ userId, showEmail = false, onEditClick }: UserProfileCardProps) {
  // ...
}
```

5. **Default exports** only for page-level components (Next.js pages). Everything else uses **named exports**.

---

## 6. Git & Branching Strategy

<!-- NOTE: This section defines how ALL code changes flow from idea → production.
     Following this prevents losing work, merge conflicts, and broken main branches. -->

### 6.1 Branch Model

We use a simplified **GitHub Flow** (suitable for 1–2 dev teams):

```
main              ← Always deployable to production
  └── feature/[ticket-id]-short-description    ← Feature work
  └── fix/[ticket-id]-short-description        ← Bug fixes
  └── chore/short-description                  ← Tooling, CI, docs
  └── hotfix/short-description                 ← Emergency production fixes
  └── release/v[major.minor.patch]             ← Release candidates (optional)
```

### 6.2 Branch Naming Rules

| Prefix | Use When | Example |
|--------|---------|---------|
| `feature/` | Adding new functionality | `feature/42-user-profile-page` |
| `fix/` | Fixing a bug (non-urgent) | `fix/87-login-redirect-loop` |
| `chore/` | Tooling, CI, documentation, refactor | `chore/update-eslint-config` |
| `hotfix/` | Emergency fix on production | `hotfix/payment-null-pointer` |
| `release/` | Preparing a versioned release | `release/v1.2.0` |

**Rules:**
- Always branch off `main` (not off another feature branch).
- Branch names are lowercase `kebab-case`.
- Include the ticket/issue number when one exists.
- Max 5 words after the prefix.

### 6.3 Commit Message Format

We follow the **Conventional Commits** specification:

```
<type>(<scope>): <short summary in imperative mood>

[optional body: explain WHY, not WHAT]

[optional footer: BREAKING CHANGE: ..., Closes #42]
```

**Types:**

| Type | When to Use | Example |
|------|-------------|---------|
| `feat` | New feature | `feat(auth): add Google OAuth login` |
| `fix` | Bug fix | `fix(cart): prevent duplicate item addition` |
| `docs` | Documentation only | `docs(readme): update setup instructions` |
| `style` | Formatting, no logic change | `style(button): apply consistent padding` |
| `refactor` | Code restructure, no behaviour change | `refactor(user-service): extract email validation` |
| `test` | Adding or fixing tests | `test(auth): add unit tests for JWT expiry` |
| `chore` | Build, CI, tooling | `chore(deps): upgrade Next.js to 15` |
| `perf` | Performance improvement | `perf(images): lazy-load below-fold images` |
| `security` | Security fix | `security(api): add rate limiting to login endpoint` |
| `ai` | AI-generated code that passed human review | `ai(user-service): Claude-generated email validator (reviewed)` |

**Commit message rules:**
- Summary line: max **72 characters**.
- Use **imperative mood**: "add feature" not "added feature" or "adding feature".
- No period at the end of the summary line.
- Always reference an issue number if one exists: `Closes #42`.
- **Never commit directly to `main`.**

### 6.4 Pull Request (PR) Standards

**Every PR must:**
- [ ] Have a clear title following commit message format
- [ ] Have the PR description template filled out (see below)
- [ ] Target `main` (or `release/` branch during release week)
- [ ] Pass all CI checks before requesting review
- [ ] Have at least **1 human approval** before merge
- [ ] Be **squash-merged** (keeps `main` history clean)
- [ ] Be linked to the relevant GitHub Issue

**PR Description Template** (save as `.github/PULL_REQUEST_TEMPLATE.md`):

```markdown
## Summary
<!-- What does this PR do? (2-3 sentences max) -->

## Type of Change
- [ ] feat: New feature
- [ ] fix: Bug fix
- [ ] chore: Tooling / CI / docs
- [ ] refactor: Code restructure
- [ ] security: Security fix

## AI Assistance Used?
- [ ] No AI assistance used
- [ ] AI-generated code present → AI Review Checklist (§3.4) completed ✅

## How to Test
<!-- Step-by-step instructions to manually verify this change -->
1.
2.

## Screenshots / Demo (if UI change)
<!-- Attach before/after screenshots or screen recording -->

## Checklist
- [ ] Self-reviewed my own diff
- [ ] Tests added / updated
- [ ] Documentation updated if needed
- [ ] No secrets in the diff
- [ ] Linked to GitHub Issue #___
```

### 6.5 Protected Branch Rules (GitHub Settings)

Configure these in **GitHub → Settings → Branches → Branch protection rules** for `main`:

| Rule | Setting |
|------|---------|
| Require PR before merging | ✅ ON |
| Required approvals | `[1]` (or `2` for teams > 3) |
| Dismiss stale approvals | ✅ ON |
| Require status checks to pass | ✅ ON |
| Require branches to be up to date | ✅ ON |
| Restrict direct pushes | ✅ ON |
| Require signed commits | `[Optional — enable for high-security projects]` |

### 6.6 Commit Frequency

- Commit **small, logical units** of work — one concern per commit.
- Commit **at least once per working session** (don't hoard changes).
- A PR should represent **one feature, fix, or chore** — not a week of mixed work.

---

## 7. Code Review Standards

<!-- NOTE: Code review is where quality is actually enforced. Be specific, kind, and fast. -->

### 7.1 Review SLA (Service Level Agreement)

| Priority | Response Time |
|----------|--------------|
| `hotfix/` or `security` PR | ≤ 2 hours |
| Standard feature PR | ≤ 1 business day |
| Chore / docs PR | ≤ 2 business days |

### 7.2 What Reviewers Must Check

**Correctness**
- [ ] Does the code do what the PR description says?
- [ ] Are edge cases handled (null, empty, large input)?
- [ ] Are error states handled gracefully?

**Security**
- [ ] No secrets, tokens, or PII in the diff (see §9)
- [ ] Input is validated before use
- [ ] Auth/permission checks in place where needed

**Code Quality**
- [ ] Follows naming conventions (§4)
- [ ] No dead code, commented-out blocks, or TODO without a ticket reference
- [ ] Functions are small and do one thing
- [ ] No unnecessary complexity

**Tests**
- [ ] New logic has tests
- [ ] Tests actually test the right thing (not just line coverage)

**AI Code** (if applicable)
- [ ] AI Review Checklist (§3.4) was completed
- [ ] Attribution comment is present (§3.5)

### 7.3 Review Comment Etiquette

Prefix comments with a label to make intent clear:

| Label | Meaning |
|-------|---------|
| `[blocker]` | Must be fixed before merge |
| `[suggestion]` | Optional improvement, author decides |
| `[question]` | Seeking understanding, not blocking |
| `[nitpick]` | Minor style issue, not blocking |
| `[praise]` | Acknowledge good work |

---

## 8. Testing Standards

### 8.1 Testing Philosophy

> **Test behaviour, not implementation.**
> Tests should verify *what* the code does for a user, not *how* it does it internally.

### 8.2 Test Coverage Targets

| Layer | Minimum Coverage | Target Coverage |
|-------|-----------------|----------------|
| Business logic / services | 80% | 90%+ |
| UI components | 60% | 80% |
| API endpoints / routes | 75% | 90% |
| Utility functions | 90% | 100% |
| AI-generated code | 80% (human-written tests) | 90% |

<!-- NOTE: Coverage is a guide, not a religion. 80 lines of meaningful tests beat 200 lines that just check
     that a function was called. -->

### 8.3 Test Types & When to Use Them

| Type | Tool | When to Write | What It Tests |
|------|------|--------------|--------------|
| **Unit** | Vitest / Jest / Pytest | Always for pure functions & services | Single function in isolation |
| **Integration** | Vitest / Pytest | For service + DB or service + API combos | Multiple units working together |
| **Component** | React Testing Library / XCTest | For every non-trivial UI component | Component renders & responds correctly |
| **E2E** | `[Playwright / Cypress / Detox]` | For critical user flows | Full stack from UI to DB |
| **Snapshot** | Jest | Sparingly — for stable, pure UI | HTML/JSON structure hasn't changed unexpectedly |

### 8.4 Test File Conventions

```typescript
// File: UserProfileCard.test.tsx

import { render, screen, userEvent } from '@testing-library/react';
import { UserProfileCard } from './UserProfileCard';

describe('UserProfileCard', () => {
  // Group by scenario, not by method name
  describe('when user data is loaded', () => {
    it('displays the user full name', () => {
      // Arrange
      const user = { id: '1', name: 'Jane Doe', email: 'jane@example.com' };
      // Act
      render(<UserProfileCard user={user} />);
      // Assert
      expect(screen.getByText('Jane Doe')).toBeInTheDocument();
    });
  });

  describe('when user data fails to load', () => {
    it('shows an error message', () => {
      // ...
    });
  });
});
```

**Rules:**
- Use **Arrange / Act / Assert** (AAA) pattern.
- Test description reads like a sentence: `it('displays the user full name')`.
- No production code logic in test files.
- Mock external services (network, DB, Auth) — never hit real APIs in unit tests.

---

## 9. Security & Secrets Handling

<!-- NOTE: One leaked API key can cost thousands in cloud bills or compromise user data.
     Read this section carefully and follow it without exception. -->

### 9.1 The Golden Rule

> **Never commit secrets to Git. Not once. Not "just temporarily". Never.**

### 9.2 What Counts as a Secret

- API keys (OpenAI, Stripe, SendGrid, Twilio, etc.)
- Database connection strings / credentials
- JWT / session secrets
- OAuth client secrets
- AWS / GCP / Azure credentials
- Supabase / Firebase service role keys
- Any password
- PII (email, phone, government ID, etc.) used as config

### 9.3 Environment Variable Rules

```bash
# ✅ CORRECT: .env.local (never committed)
SUPABASE_URL=https://xxx.supabase.co
SUPABASE_ANON_KEY=eyJhbGc...
STRIPE_SECRET_KEY=sk_live_...

# ✅ CORRECT: .env.example (always committed — no real values)
SUPABASE_URL=your_supabase_project_url
SUPABASE_ANON_KEY=your_supabase_anon_key
STRIPE_SECRET_KEY=your_stripe_secret_key
```

**Rules:**
- Every secret lives in a `.env.*` file that is listed in `.gitignore`.
- Always maintain a `.env.example` with blank or fake values so contributors know what to set.
- Access env vars only through a **typed config module** — never `process.env.X` scattered across files:

```typescript
// lib/config.ts  ← single source of truth for all env vars
import { z } from 'zod';

const configSchema = z.object({
  SUPABASE_URL: z.string().url(),
  SUPABASE_ANON_KEY: z.string().min(1),
  STRIPE_SECRET_KEY: z.string().startsWith('sk_'),
});

export const config = configSchema.parse(process.env);
// App fails immediately at startup if any required env var is missing or invalid ✅
```

### 9.4 Secret Management in Production

| Environment | Secret Storage | Do NOT Use |
|-------------|---------------|-----------|
| Local dev | `.env.local` | Hardcoded values |
| CI/CD (GitHub Actions) | GitHub Secrets | `.env` files in repo |
| Staging / Production | `[AWS Secrets Manager / Doppler / Vault]` | `.env` files in containers |
| Cloudflare Workers | Cloudflare Secrets (`wrangler secret put`) | Wrangler config files |
| Mobile (iOS/Android) | `[e.g., iOS Keychain / Android Keystore]` | `Info.plist` / `AndroidManifest.xml` |

### 9.5 Secret Scanning

- Enable **GitHub Secret Scanning** on all repositories (GitHub → Settings → Security → Secret scanning).
- Enable **GitHub Push Protection** to block commits containing detected secrets.
- Install `[gitleaks]` as a pre-commit hook:

```bash
# Install gitleaks pre-commit hook (one-time setup)
brew install gitleaks
gitleaks protect --staged -v
```

### 9.6 Principle of Least Privilege

- Service accounts and API keys should have **only the permissions they need** — nothing more.
- Use **read-only** keys where write access is not required.
- Rotate all API keys and secrets every **`[90 days / 180 days]`**.
- Revoke unused keys immediately.

### 9.7 Security Checklist Before Launch

- [ ] All secrets removed from code history (use `git-filter-repo` if needed)
- [ ] `.env.example` committed, `.env.*` files in `.gitignore`
- [ ] GitHub Secret Scanning enabled
- [ ] All API keys scoped to minimum required permissions
- [ ] HTTPS enforced on all endpoints
- [ ] Authentication required on all private endpoints
- [ ] Rate limiting enabled on all public-facing APIs
- [ ] Input validation on all user-controlled fields
- [ ] SQL injection protection (parameterised queries / ORM)
- [ ] CORS configured correctly (not `*` in production)
- [ ] Security headers set (`Content-Security-Policy`, `X-Frame-Options`, etc.)
- [ ] Dependencies scanned for CVEs (`npm audit` / `pip-audit`)

---

## 10. Environment Configuration

### 10.1 Environment Tiers

| Tier | Purpose | Who Has Access | Data |
|------|---------|---------------|------|
| `local` | Individual developer's machine | Developer only | Fake / seeded data |
| `test` | Automated CI/CD test runs | CI system | Isolated test DB |
| `staging` | Pre-production validation | Team + QA | Anonymised production-like data |
| `production` | Live product | Approved deployers only | Real user data |

### 10.2 Environment Variable Naming

Prefix all environment variables with the service name:

```bash
# ✅ Correct
SUPABASE_URL=
STRIPE_WEBHOOK_SECRET=
NEXT_PUBLIC_APP_URL=        # NEXT_PUBLIC_ prefix = safe to expose to browser
OPENAI_API_KEY=

# ❌ Wrong
DATABASE=                   # Too vague
key=                        # Not descriptive
```

**Rule:** Anything prefixed `NEXT_PUBLIC_` (Next.js) or `EXPO_PUBLIC_` (Expo) is **visible in the browser / app bundle**. Never put secrets there.

---

## 11. Documentation Standards

### 11.1 Code Comments — When to Write Them

**Write a comment when:**
- The *why* is not obvious from the code.
- A workaround exists due to a known library bug (include the issue URL).
- A complex algorithm is implemented.
- A regulatory or business rule is enforced.

**Do NOT write a comment when:**
- The code already explains itself (`// increment i by 1 → i++`).
- To explain what a function does — use a docstring instead.
- To keep commented-out code. Delete it; Git has history.

### 11.2 JSDoc / TSDoc (TypeScript)

Every **exported** function, class, and type must have a TSDoc comment:

```typescript
/**
 * Fetches a user record by ID from the database.
 *
 * @param userId - The UUID of the user to fetch.
 * @param options - Optional query configuration.
 * @returns The user profile, or `null` if not found.
 * @throws {DatabaseError} When the database query fails.
 *
 * @example
 * const user = await getUserById('abc-123');
 */
export async function getUserById(
  userId: string,
  options?: QueryOptions
): Promise<UserProfile | null> {
  // ...
}
```

### 11.3 Python Docstrings (Google Style)

```python
def get_user_by_id(user_id: str, include_deleted: bool = False) -> UserProfile | None:
    """Fetch a user record by ID from the database.

    Args:
        user_id: The UUID of the user to fetch.
        include_deleted: Whether to include soft-deleted users. Defaults to False.

    Returns:
        The UserProfile object, or None if not found.

    Raises:
        DatabaseError: When the database query fails.

    Example:
        user = get_user_by_id("abc-123")
    """
```

### 11.4 README Requirements

Every repository must have a `README.md` that includes:

- [ ] Project name and one-line description
- [ ] Tech stack badges
- [ ] Prerequisites (Node version, Python version, etc.)
- [ ] Local setup instructions (step by step, beginner-friendly)
- [ ] Environment variables — link to `.env.example`
- [ ] How to run tests
- [ ] How to deploy
- [ ] Link to this `Coding_Standards.md`
- [ ] Contact / ownership information

---

## 12. Error Handling & Logging

### 12.1 Error Handling Rules

1. **Never swallow errors silently:**

```typescript
// ❌ Wrong — error disappears
try {
  await fetchUser(id);
} catch (_e) {}

// ✅ Correct — error is logged and re-thrown or handled
try {
  await fetchUser(id);
} catch (error) {
  logger.error('Failed to fetch user', { userId: id, error });
  throw new ServiceError('USER_FETCH_FAILED', { cause: error });
}
```

2. **Use typed, structured errors:**

```typescript
// Create a base error class for your project
export class AppError extends Error {
  constructor(
    public readonly code: string,
    public readonly statusCode: number = 500,
    public readonly context?: Record<string, unknown>,
    options?: ErrorOptions
  ) {
    super(code, options);
    this.name = 'AppError';
  }
}
```

3. **Always handle promise rejections.** No bare `await` without try/catch in production paths.

4. **Show user-friendly messages** — never expose internal error messages or stack traces to end users.

### 12.2 Logging Standards

Use a structured logger (e.g., `pino` for Node.js, `structlog` for Python):

```typescript
import { logger } from '@/lib/logger';

// ✅ Structured log — searchable in your observability platform
logger.info('User login succeeded', {
  userId: user.id,
  method: 'google_oauth',
  timestamp: new Date().toISOString(),
});

// ❌ Plain string log — not searchable
console.log('user logged in');
```

**Log Levels:**

| Level | When to Use | Example |
|-------|------------|---------|
| `debug` | Detailed flow info (dev only) | `debug('Cache miss for key', { key })` |
| `info` | Normal app events | `info('User registered', { userId })` |
| `warn` | Unexpected but recoverable events | `warn('Rate limit approaching', { remaining: 5 })` |
| `error` | Failures that need attention | `error('Payment failed', { orderId, reason })` |
| `fatal` | App cannot continue | `fatal('Database connection lost')` |

**Logging Rules:**
- Log at `info` level for all significant business events.
- **Never log secrets, passwords, or PII** (even at debug level).
- Always log in structured JSON format in production.
- Include a `correlationId` / `requestId` in every log for traceability.

---

## 13. Performance Standards

### 13.1 Web Performance Targets (Core Web Vitals)

| Metric | Target | Tool |
|--------|--------|------|
| LCP (Largest Contentful Paint) | < 2.5s | Lighthouse, Vercel Analytics |
| INP (Interaction to Next Paint) | < 200ms | Chrome DevTools |
| CLS (Cumulative Layout Shift) | < 0.1 | Lighthouse |
| TTFB (Time to First Byte) | < 800ms | WebPageTest |
| Bundle size (initial JS) | < 200KB gzipped | `next build` output |

### 13.2 Mobile Performance Targets

| Metric | Target | Tool |
|--------|--------|------|
| App startup time (cold) | < 2s | Xcode Instruments / Android Profiler |
| Frame rate (animations) | 60 fps (120 fps on capable devices) | — |
| Memory usage (foreground) | < 150MB | — |
| API response time (p95) | < 500ms | — |

### 13.3 Performance Rules

- **Images:** Always use next/image (Next.js) or optimised image components. Specify `width` and `height`.
- **Fonts:** Use `font-display: swap`. Load only the weights you use.
- **Code splitting:** Use dynamic imports (`next/dynamic`, `React.lazy`) for non-critical components.
- **Lists:** Virtualise lists longer than 50 items (e.g., `react-virtual`, `FlashList` for RN).
- **Memoisation:** Use `useMemo`, `useCallback`, `React.memo` — but only after measuring that they help.
- **Database queries:** Avoid N+1 queries. Use `select` to fetch only needed columns.

---

## 14. Accessibility Standards

### 14.1 Target Compliance Level

> **Target: WCAG 2.1 Level AA**

### 14.2 Accessibility Checklist

**Web:**
- [ ] All images have descriptive `alt` text (or `alt=""` for decorative images)
- [ ] All form inputs have associated `<label>` elements
- [ ] Colour contrast ratio ≥ 4.5:1 for normal text, ≥ 3:1 for large text
- [ ] All interactive elements are keyboard-reachable (Tab order is logical)
- [ ] Focus indicators are visible
- [ ] ARIA roles used correctly (don't override native semantics unless necessary)
- [ ] Page works without JavaScript for critical paths
- [ ] `lang` attribute set on `<html>`

**Mobile:**
- [ ] All interactive elements have `accessibilityLabel` (RN) / `contentDescription` (Android) / `accessibilityLabel` (iOS)
- [ ] Minimum tap target size: 44×44 pt (iOS) / 48×48 dp (Android)
- [ ] Dynamic text size supported (don't use fixed pixel font sizes)
- [ ] Screen reader tested (VoiceOver / TalkBack)

---

## 15. Dependencies & Package Management

### 15.1 Adding a New Dependency

Before adding any package, ask:

1. **Do we really need it?** Can this be done in < 20 lines of vanilla code?
2. **Is it maintained?** Last commit < 6 months ago? > 100 GitHub stars?
3. **Is it secure?** Run `npm audit` / `pip-audit` after installing.
4. **What's the bundle cost?** Check bundlephobia.com for JS packages.
5. **Is the licence compatible?** MIT, Apache 2.0, BSD — generally fine. GPL — check with legal.

### 15.2 Package Manager Rules

| Platform | Package Manager | Lock File |
|----------|----------------|-----------|
| Node.js | `[npm / pnpm / yarn]` — pick ONE, never mix | `package-lock.json` / `pnpm-lock.yaml` |
| Python | `pip` + `pip-compile` or `Poetry` | `requirements.txt` / `poetry.lock` |
| iOS | Swift Package Manager | `Package.resolved` |
| Android | Gradle | `gradle/verification-metadata.xml` |

**Rules:**
- Always commit lock files.
- Run `npm ci` (not `npm install`) in CI.
- Pin major versions in `package.json` — avoid `*` or `latest`.
- Review `npm audit` / Dependabot alerts at least weekly.

---

## 16. Deployment & Release Process

### 16.1 Deployment Pipeline Overview

```
Developer pushes to feature branch
    ↓
GitHub Actions: lint + type-check + unit tests (auto)
    ↓
PR opened → human code review
    ↓
PR merged to main
    ↓
GitHub Actions: full test suite (auto)
    ↓
Auto-deploy to STAGING (Vercel preview / TestFlight internal)
    ↓
Manual QA + smoke test on staging
    ↓
Manual trigger: deploy to PRODUCTION
    ↓
Post-deploy: run smoke tests + monitor error rate for 30 min
```

### 16.2 Deployment Checklist (Every Release)

**Before deploying:**
- [ ] All tests pass in CI
- [ ] Security checklist (§9.7) complete
- [ ] `.env.example` up to date
- [ ] Database migrations tested on staging (if applicable)
- [ ] Release notes drafted
- [ ] Rollback plan documented

**After deploying:**
- [ ] Smoke-tested the critical user path (login → core feature → sign out)
- [ ] Error rate within normal range (check Sentry / Cloudflare analytics)
- [ ] Performance metrics not degraded
- [ ] Team notified in `[#deployments Slack channel / team chat]`

### 16.3 Versioning

We follow **Semantic Versioning (SemVer)**:

```
MAJOR.MINOR.PATCH  →  e.g., 2.4.1

MAJOR: Breaking change (existing users notice something broken or gone)
MINOR: New feature added (backward compatible)
PATCH: Bug fix (backward compatible)
```

- Version is tracked in `package.json` (web) and `app.config.ts` / `pubspec.yaml` (mobile).
- Every production release gets a **Git tag**: `git tag -a v1.2.3 -m "Release v1.2.3"`.
- Every release gets a **GitHub Release** with auto-generated or manually written release notes.

### 16.4 Mobile App Release Process

| Step | iOS | Android |
|------|-----|---------|
| Build | Xcode Archive / EAS Build | Gradle bundle / EAS Build |
| Test | TestFlight (internal → external) | Internal track → Production track |
| Review | Apple App Review | Google Play Review |
| Release | Phased rollout | Staged rollout |
| Rollback | Submit previous build | Halt rollout in Play Console |

---

## 17. Monitoring & Observability

### 17.1 Required Monitoring Stack

| Category | Tool | What It Monitors |
|----------|------|-----------------|
| Error tracking | `[Sentry / Bugsnag]` | Exceptions, crashes, error rates |
| Web analytics | `[Vercel Analytics / Plausible]` | Page views, Core Web Vitals |
| API performance | `[Cloudflare Analytics / Datadog]` | Latency, error rates, uptime |
| Uptime monitoring | `[Betteruptime / UptimeRobot]` | Endpoint availability |
| Mobile crash reporting | `[Sentry / Firebase Crashlytics]` | App crashes by OS/device |
| Log aggregation | `[Axiom / Logtail / CloudWatch]` | Structured log search & alerts |

### 17.2 Alert Thresholds

Define alerts so you know before your users do:

| Metric | Warning | Critical |
|--------|---------|---------|
| API error rate | > 1% | > 5% |
| API p95 latency | > 1s | > 3s |
| App crash rate | > 0.5% | > 2% |
| CPU utilisation | > 70% | > 90% |
| Memory utilisation | > 75% | > 90% |
| Failed login attempts | > 50/min | > 200/min |

### 17.3 On-Call & Incident Response

<!-- NOTE: Even as a solo dev, define how you respond to outages. -->

| Severity | Definition | Response Time | Action |
|----------|------------|---------------|--------|
| P1 — Critical | Production down, data loss, security breach | Immediate | Page on-call, start incident channel |
| P2 — High | Core feature broken for > 10% of users | < 1 hour | Notify team, start fix |
| P3 — Medium | Feature degraded, workaround exists | < 4 hours | Add to current sprint |
| P4 — Low | Minor bug, cosmetic issue | Next sprint | File GitHub Issue |

---

## 18. First 500 Customers — Quality Gates

<!-- NOTE: This section is specifically for the growth phase from launch to 500 active customers.
     It defines the quality bar you must hit before acquiring more users. -->

### 18.1 Pre-Launch Gate (0 → 1)

Must ALL pass before accepting the first paying customer:

- [ ] **Security:** All items in §9.7 Security Checklist complete
- [ ] **Performance:** Core Web Vitals pass (LCP < 2.5s, CLS < 0.1)
- [ ] **Accessibility:** WCAG 2.1 AA Lighthouse score ≥ 90
- [ ] **Error tracking:** Sentry (or equivalent) live and sending alerts
- [ ] **Uptime monitoring:** At least one uptime check configured
- [ ] **Backups:** Database backup confirmed working (test restore)
- [ ] **Privacy policy & Terms:** Published and linked in app
- [ ] **Analytics:** Basic product analytics live
- [ ] **Support channel:** At least one customer support contact method published
- [ ] **Payments:** If charging money — Stripe integration tested end-to-end in live mode
- [ ] **Critical user flow test:** Sign up → use core feature → sign out — works on iOS, Android, and web

### 18.2 0 → 100 Customers Gate

Must resolve before customer 100:

- [ ] **User feedback loop:** In-app feedback or user interview process in place
- [ ] **Error budget:** Error rate consistently < 1%
- [ ] **On-call process:** Defined (even if it's just "my personal phone gets paged")
- [ ] **Runbook:** Documented steps for the top 3 most likely failure scenarios
- [ ] **Data deletion:** Users can request account + data deletion (GDPR / CCPA)
- [ ] **Mobile crash rate:** < 1%

### 18.3 100 → 500 Customers Gate

Must resolve before customer 500:

- [ ] **Load testing:** System tested at 10× current peak traffic
- [ ] **DR (Disaster Recovery) plan:** Documented and tested
- [ ] **Incident post-mortems:** Written for every P1/P2 incident
- [ ] **Changelog:** Public-facing changelog live
- [ ] **Automated e2e tests:** Cover at least the top 3 user flows
- [ ] **API rate limiting:** Implemented and tuned
- [ ] **Multi-region or CDN:** Static assets served via CDN (Cloudflare)
- [ ] **Mobile app review responses:** Responding to App Store / Google Play reviews within 48h
- [ ] **Zero known P1/P2 bugs:** Before scaling marketing spend

---

## 19. Compliance & Audit Trail

### 19.1 Data Privacy Compliance

| Regulation | Applies If | Required Actions |
|-----------|------------|-----------------|
| GDPR | Any EU/UK user | Privacy policy, data processing records, right to deletion, breach notification |
| CCPA | Any California user | Privacy policy, opt-out of sale, right to deletion |
| COPPA | Users under 13 | No collection of data from minors — block under-13 sign-up |
| App Store Privacy | iOS app | App Privacy Nutrition Label accurate in App Store Connect |
| Google Play Data Safety | Android app | Data safety form completed in Play Console |

### 19.2 AI Compliance

- **AI-generated user-facing content** must be labelled if required by local law.
- **LLM API calls** must not send PII to third-party models without user consent and data processing agreement.
- **Prompts to Claude or any LLM** must NOT include raw user PII (hash/anonymise where possible).
- Document all AI model usage in your privacy policy.

### 19.3 Change Log & Audit

- Every production deployment must be logged with: deployer, timestamp, version, and change summary.
- Keep a `CHANGELOG.md` in each repository following [Keep a Changelog](https://keepachangelog.com) format.
- Database schema changes must include a migration file with author and date.

---

## 20. Appendix & References

### 20.1 Quick-Reference Cheat Sheet

```
Branch naming:   feature/[id]-short-name
Commit format:   type(scope): summary (max 72 chars)
PR merge style:  Squash merge only
Env files:       .env.local (secret), .env.example (committed)
Test pattern:    Arrange / Act / Assert
Log format:      Structured JSON in production
Versioning:      SemVer — MAJOR.MINOR.PATCH
AI attribution:  @ai-generated + @reviewed-by in every AI-assisted function
```

### 20.2 Tooling Setup Checklist (New Contributor)

- [ ] Clone repo and copy `.env.example` → `.env.local`
- [ ] Install dependencies (`npm ci` or `pnpm install`)
- [ ] Install `gitleaks` for secret scanning pre-commit hook
- [ ] Set up editor config (`.editorconfig`) and ESLint / Prettier extensions
- [ ] Read `README.md` end-to-end
- [ ] Read this `Coding_Standards.md` end-to-end
- [ ] Run tests locally: `npm run test`
- [ ] Run linter: `npm run lint`
- [ ] Ask a question in `[#dev Slack / team chat]` if anything is unclear

### 20.3 External References

| Resource | URL | Why It Matters |
|----------|-----|---------------|
| Conventional Commits | https://www.conventionalcommits.org | Commit message format |
| Keep a Changelog | https://keepachangelog.com | Changelog format |
| SemVer | https://semver.org | Versioning standard |
| WCAG 2.1 | https://www.w3.org/TR/WCAG21 | Accessibility guidelines |
| OWASP Top 10 | https://owasp.org/www-project-top-ten | Security vulnerabilities to prevent |
| Google TypeScript Style Guide | https://google.github.io/styleguide/tsguide.html | TS style reference |
| PEP 8 | https://pep8.org | Python style reference |
| Swift API Design Guidelines | https://swift.org/documentation/api-design-guidelines | Swift style reference |
| Android Kotlin Style | https://developer.android.com/kotlin/style-guide | Kotlin style reference |

### 20.4 Document Change History

| Version | Date | Author | Summary of Changes |
|---------|------|--------|-------------------|
| v1.0.0 | `[YYYY-MM-DD]` | `[Your Name]` | Initial version |
| | | | |

---

*This document is version-controlled. Propose changes via a PR to `main` with the label `docs: coding-standards`.*
*Last reviewed by: `[Name]` on `[YYYY-MM-DD]`*
