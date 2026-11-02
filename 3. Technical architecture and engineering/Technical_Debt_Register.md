# 📋 Technical Debt Register
<!--
  ╔══════════════════════════════════════════════════════════════════════╗
  ║  LIVING DOCUMENT — Update this every sprint or every week.          ║
  ║  Version: 1.0  |  AI-Driven Development Life Cycle (ADLC)           ║
  ║  Optimised for: SaaS / Mobile App · Solo & Small Teams (1–10)       ║
  ║  Tracking tool: GitHub Issues / GitHub Projects                      ║
  ╚══════════════════════════════════════════════════════════════════════╝
-->

---

# 📖 How to Fill This Document — Read This First!

> **🧒 Total beginner?** That's fine. Read this section top to bottom before touching anything else.
> It will take about 10 minutes and will make everything else make sense.

---

## 💡 What Is Technical Debt? (Plain English)

Imagine you are building a LEGO city. You need to finish the fire station today,
so you use sticky tape instead of the proper LEGO bricks because it is faster.
The fire station looks fine — but you know the tape will fall off eventually.
**That sticky-tape shortcut is technical debt.**

In software, technical debt is any shortcut, quick fix, or "good-enough-for-now"
decision that creates extra work later. It is not a sign that you did something
wrong — it is a normal part of building software fast. The danger is **not tracking it.**

This register is your map of every shortcut. Without it, shortcuts pile up silently
until they slow your whole team down or break things for real users.

---

## ✅ 5-Step Quick Start (Do This Now)

### Step 1 — Fill the Project Information Table
Scroll down to the **Project Information** section. Fill in your project name,
GitHub repo URL, your name, and today's date. This takes 2 minutes. Do it once.

### Step 2 — Read the Priority Guide (P0–P4)
Before adding any items, read the **Priority Levels** section. It tells you how
urgent each piece of debt is. You will use these levels every single time you log
an item, so read it carefully.

### Step 3 — Add Your First Debt Item
Find a phase table that matches your current stage (Phase 2 is the most common
starting point). Add a new row at the bottom. Fill in every column. If you do not
know an answer yet, write `TBD`. Give it a unique ID (`TD-001`, `TD-002`, ...).

### Step 4 — Create a GitHub Issue for Every Item
For each debt item you log here, open a GitHub Issue in your repository and paste
the issue number into the `GH Issue` column. This keeps your debt visible in your
normal workflow. See the **GitHub Integration Guide** at the bottom for how to set this up.

### Step 5 — Update This Register Weekly
Every week (or at the start of each sprint), review the register:
- Move items from `🔴 Open` → `🟡 In Progress` → `✅ Resolved` as work progresses.
- Fill in `Resolved On` and `Notes` when an item is closed.
- Recalculate your **Debt Health Score**. Aim to keep it below 25.
- Before every major milestone (launch, 100 users, 500 users), resolve all P0 and P1 items first.

---

## 🟡 The Golden Rules of This Register

| # | Rule | Why It Matters |
|---|------|---------------|
| 1 | **Never delete a row — resolve it.** | Deleted history means you cannot learn from past decisions. |
| 2 | **Be honest about priority.** | Calling a P0 a P2 because it is uncomfortable does not make it less dangerous. |
| 3 | **One debt item per row.** | Do not combine two problems in one row. They may need different owners and timelines. |
| 4 | **Log debt when it is created, not when it is convenient.** | A debt item you forget to log is a debt you cannot pay back. |
| 5 | **AI-generated code is your responsibility.** | If Claude, ChatGPT, or Copilot wrote a line you did not fully review, it belongs in Phase 4. |
| 6 | **20% rule.** | Aim to spend 20% of every sprint resolving existing debt, not just building new features. |

---

## 🗂 Column Definitions (Plain English)

> Every table in this document uses these same columns.
> Read this once — then you will know how to fill every table.

| Column | What to Write | Example |
|--------|--------------|---------|
| **ID** | A unique code. Format: `TD-001`. Increment by 1 for every new item. Never reuse an ID, even after resolving the item. | `TD-007` |
| **Date** | When you first noticed this debt. Format: `YYYY-MM-DD`. | `2026-10-14` |
| **Logged By** | Your name or GitHub username (with `@`). | `@alice` |
| **Category** | Pick one code from the Category table below. | `SEC` |
| **Title** | 5–10 words that name the problem, like a newspaper headline. Specific beats vague. | `JWT token expiry not checked in middleware` |
| **Description** | 1–3 sentences: *What* is wrong? *Where* is it (file/module/screen)? *How* did this happen? | `Auth middleware checks signature but ignores the exp field. Introduced in Sprint 3 during time crunch.` |
| **Impact** | What breaks, slows down, or becomes risky if this is NOT fixed? Be specific. | `Expired tokens still grant access to protected routes indefinitely.` |
| **Affected Area** | File path, module name, service, or screen. Be as specific as possible. | `middleware/auth.ts`, `iOS Login Screen` |
| **Priority** | See the P0–P4 table below. Be honest. | `P0` |
| **Effort** | How hard is the fix? Use: `XS` `S` `M` `L` `XL` (see Effort table below). | `S` |
| **GH Issue** | The GitHub Issue number. Format: `[#45](url)`. Write `—` if not yet created. | `[#45](https://github.com/org/repo/issues/45)` |
| **Status** | `🔴 Open` · `🟡 In Progress` · `✅ Resolved` | `🟡 In Progress` |
| **Target Date** | When do you *plan* to fix this? Use sprint name or date. | `Sprint 5` or `2026-11-01` |
| **Resolved On** | The actual date it was fixed. Leave blank until resolved. | `2026-11-03` |
| **Notes** | Workarounds currently in place, who to ask questions, links to related PRs or decisions. | `Using WAL mode as short-term workaround. PR #47 adds the fix.` |

---

## 🏷 Debt Categories

| Code | Category Name | What Belongs Here |
|------|--------------|-------------------|
| `ARCH` | Architecture & Design | Structural decisions made too quickly — wrong database choice, missing API versioning, a monolith that should be microservices, no domain model |
| `CODE` | Code Quality | Messy, duplicated, or unreadable code; missing inline comments; overly complex functions; copy-pasted logic; dead code; `TODO` / `FIXME` / `HACK` comments |
| `AI` | AI-Generated Code | Any debt introduced specifically by Claude, ChatGPT, Copilot, or another AI coding tool — hallucinated logic, untested generated code, wrong edge-case assumptions |
| `TEST` | Testing & QA | Missing unit tests, missing integration tests, no end-to-end tests, low code coverage, no test data strategy, manual-only QA |
| `SEC` | Security | Hardcoded secrets or API keys, missing authentication, unvalidated user inputs, exposed endpoints, missing rate limiting, OWASP vulnerabilities, GDPR compliance gaps |
| `INFRA` | Infrastructure & DevOps | Manual deployments, missing or broken CI/CD, no monitoring, no alerting, no database backups, over-permissioned IAM roles, no disaster-recovery plan |
| `UX` | UX & Accessibility | Poor user experience, broken mobile layout, missing loading states, no error messages, accessibility (a11y) violations, inconsistent design |
| `DOCS` | Documentation | Missing API docs, no README, outdated architecture diagrams, no onboarding guide, no inline code comments for complex logic |
| `DEP` | Dependencies | Outdated packages, deprecated libraries, unresolved CVEs (public security vulnerabilities), unpinned dependency versions |
| `PERF` | Performance | Slow database queries, unoptimised images, missing pagination, no caching, N+1 query problems, excessive third-party API calls on every page load |
| `DATA` | Data & Analytics | Missing event tracking, broken or absent analytics, no data validation layer, missing audit logs, privacy/GDPR data-retention gaps |

---

## 🚦 Priority Levels: P0 to P4

> **Simple rule:** If your stomach drops when you read it — it is probably P0 or P1.
> If you shrug — it is probably P3 or P4. When in doubt, go one level higher.

| Priority | Name | Plain English Meaning | Fix When? | Real Example |
|----------|----- |----------------------|-----------|-------------|
| **P0** | 🚨 Critical | The app is broken, data is at risk, a security breach is possible, or launch is completely blocked. Drop everything. This is the only thing that matters right now. | **Same day — within hours** | Production is down. A Stripe API key is exposed in a public commit. Login is broken for all users. Database has no backups and data was just deleted. |
| **P1** | 🔴 High | A major feature is broken or significantly broken. Real users are impacted or will be very soon. Cannot wait for next sprint. | **This sprint (1–2 weeks)** | Payments occasionally double-charge. App crashes on iOS 17 for 30% of users. Auth tokens never expire. The signup flow breaks on mobile Safari. |
| **P2** | 🟡 Medium | Something works but not well. Annoying, slow, or technically wrong. A workaround exists but it is not sustainable. | **Next sprint (2–4 weeks)** | Dashboard API takes 4 seconds to load. No pagination on the user list (breaks at 500+ rows). Error messages say "Something went wrong" with no details. |
| **P3** | 🟢 Low | Small issue. A workaround exists. Minimal or no user impact. | **When time allows (this month or next)** | Missing loading spinner on one button. Console.log statements left in production code. Inconsistent button corner radius between screens. |
| **P4** | ⚪ Negligible | Cosmetic, internal-only, or nice-to-have. No real business or user impact. | **Backlog — some day** | A variable named `x` instead of `userId`. A missing JSDoc comment on a helper function. An unused CSS class. |

---

## 📏 Effort Estimates

| Size | Time to Fix | What It Looks Like |
|------|-------------|-------------------|
| `XS` | Under 1 hour | Rename a variable, remove dead code, fix a typo, update one env var |
| `S` | 1–4 hours | Add a unit test, rotate an API key, fix a small UI bug, update one dependency |
| `M` | 1–2 days | Refactor a module, add authentication to a route, write API docs for one service |
| `L` | 3–5 days | Redesign a database schema, add test coverage to a whole service, set up CI/CD |
| `XL` | 1+ week | Architectural refactor, migrate database, rewrite a core module from scratch |

---

---

# 📊 Project Information

> Fill this in once when you start. Update `Last Updated` and `Current Phase` as the project evolves.

| Field | Your Answer |
|-------|------------|
| **Project Name** | `[Replace with your project name]` |
| **Product Type** | `SaaS Web App / Mobile App (iOS) / Mobile App (Android) / All of the above` |
| **GitHub Repository** | `[https://github.com/your-org/your-repo]` |
| **Register Owner** | `[Your name or @github-username]` |
| **Team Members** | `[List names or @usernames of everyone who may log items]` |
| **Date Register Created** | `[YYYY-MM-DD]` |
| **Last Updated** | `[YYYY-MM-DD]` |
| **Current Version** | `v1.0` |
| **Current SDLC Phase** | `☐ Ideation  ☐ MVP Build  ☐ Beta / QA  ☐ Launch  ☐ Post-Launch (0–500 users)` |
| **Current Customer Milestone** | `☐ 0 users  ☐ 1–50  ☐ 51–200  ☐ 201–500` |
| **AI Tools in Use** | `Claude / ChatGPT / GitHub Copilot / Cursor / Other: ___` |

---

---

# 📈 Debt Health Dashboard

> Update this every Friday (or at the start of every sprint).
> It gives you a 10-second snapshot of your project's debt health — no deep reading required.

---

## 🧮 How to Calculate Your Debt Health Score

> **This is just simple maths — no coding required.**

**The Formula:**

```
Health Score = (Open P0s × 10) + (Open P1s × 5) + (Open P2s × 3) + (Open P3s × 1) + (Open P4s × 0.5)
```

**Worked Example:**
You have 0 P0s, 2 P1s, 4 P2s, 3 P3s, and 1 P4 open right now.

```
Score = (0 × 10) + (2 × 5) + (4 × 3) + (3 × 1) + (1 × 0.5)
      =     0    +    10   +    12   +    3    +   0.5
      = 25.5  →  🟡 Monitor
```

---

## 🎯 Score Interpretation

| Score | Status | What to Do |
|-------|--------|-----------|
| **0 – 10** | 🟢 **Healthy** | Excellent shape. Keep logging and resolving as you build. Maintain the habit. |
| **11 – 25** | 🟡 **Monitor** | Debt is building. Dedicate at least 20% of every sprint to paydown. |
| **26 – 50** | 🟠 **Concerning** | Red flag. Pause new feature work. Run a dedicated Debt Paydown Sprint. |
| **51 +** | 🔴 **Critical** | Emergency. Stop all new features. Resolve every P0 and P1 before anything else. |

---

## 📋 Weekly Snapshot Table

> **How to fill this:** Count all items in each phase table below by their status and priority.
> Replace the `0`s with your real counts each week.

| Priority | 🔴 Open | 🟡 In Progress | ✅ Resolved (all-time) | Weighted Score (open items only) |
|----------|---------|---------------|----------------------|----------------------------------|
| **P0 🚨** | `0` | `0` | `0` | `0 × 10 = 0` |
| **P1 🔴** | `0` | `0` | `0` | `0 × 5 = 0` |
| **P2 🟡** | `0` | `0` | `0` | `0 × 3 = 0` |
| **P3 🟢** | `0` | `0` | `0` | `0 × 1 = 0` |
| **P4 ⚪** | `0` | `0` | `0` | `0 × 0.5 = 0` |
| **TOTAL** | **0** | **0** | **0** | **🟢 Score: 0 — Healthy** |

> **📅 Last calculated:** `[YYYY-MM-DD]` by `[@your-username]`

---

---

# 🗃 Technical Debt Register

> **Which table do I use?**
> Log each debt item in the table that matches *when the debt was created* — not when you discovered it.
> Not sure? Default to **Phase 2 — MVP & Sprint Debt**.

---

## Phase 1 — Ideation & Architecture Debt 🏗

> **When does debt go here?**
> Design and architecture decisions made before or during the earliest sprints — choosing the wrong
> database, skipping Architecture Decision Records (ADRs), building a monolith that will need to be
> broken apart later, or picking a tech stack under time pressure without evaluating long-term fit.

> **💡 Beginner tip:** If you ever said *"We'll redesign this later"* or *"This won't scale but it's
> fine for now"* — that shortcut belongs in this table.

| ID | Date | Logged By | Category | Title | Description | Impact | Affected Area | Priority | Effort | GH Issue | Status | Target Date | Resolved On | Notes |
|----|------|-----------|----------|-------|-------------|--------|---------------|----------|--------|----------|--------|-------------|-------------|-------|
| TD-001 *(example)* | 2026-10-14 | @alice | `ARCH` | SQLite used instead of PostgreSQL for MVP database | Chose SQLite to start fast. Does not support concurrent writes well and will block scaling beyond a small number of simultaneous users. | Will break under ~50 concurrent users. Migration to PostgreSQL requires a multi-day effort and careful data migration. | `database/config.ts`, `database/migrations/` | P1 🔴 | L | [#12](https://github.com/your-org/repo/issues/12) | 🟡 In Progress | Sprint 5 | — | Using SQLite WAL mode as short-term workaround. Migration planned before 100-user milestone. |
| TD-002 *(example)* | 2026-10-14 | @alice | `ARCH` | No API versioning strategy — all routes are unversioned | All API routes use `/api/resource` instead of `/api/v1/resource`. Any breaking change to the API will immediately break existing mobile app clients. | Cannot update API without breaking all mobile app users simultaneously. Especially critical once the app is in the App Store. | `src/routes/`, `src/api/` | P2 🟡 | M | [#18](https://github.com/your-org/repo/issues/18) | 🔴 Open | Sprint 6 | — | — |
| `TD-XXX` | `YYYY-MM-DD` | `@you` | `ARCH` | *Short title of the problem* | *What is wrong, where is it, how did it happen?* | *What breaks or becomes risky if this is not fixed?* | *File, module, or service* | `PX` | `M` | `#000` | 🔴 Open | `Sprint X` | — | — |

---

## Phase 2 — MVP & Sprint Debt 💨

> **When does debt go here?**
> Shortcuts taken during fast MVP or sprint work to ship features quickly — hardcoded values,
> duplicated logic, missing input validation, commented-out code, functions that do too many
> things at once, or features merged without code review.

> **💡 Beginner tip:** Open your code editor and search for `// TODO`, `// FIXME`, `// HACK`,
> or `// temp`. Every result is almost certainly a debt item that should be logged here.

| ID | Date | Logged By | Category | Title | Description | Impact | Affected Area | Priority | Effort | GH Issue | Status | Target Date | Resolved On | Notes |
|----|------|-----------|----------|-------|-------------|--------|---------------|----------|--------|----------|--------|-------------|-------------|-------|
| TD-003 *(example)* | 2026-10-15 | @alice | `CODE` | Hardcoded role checks copy-pasted across 14 files | Instead of a central permissions module, the check `if (user.role === 'admin')` is duplicated in 14 different components and API routes. Added during MVP sprint under deadline. | Adding a new user role requires finding and updating 14 locations. High risk of missing one and introducing an access-control bug. | `src/components/`, `src/api/routes/` | P2 🟡 | M | [#27](https://github.com/your-org/repo/issues/27) | 🔴 Open | Sprint 7 | — | Stub for `utils/permissions.ts` created in commit `b8f2a1c`. Needs to be wired up and tested. |
| `TD-XXX` | `YYYY-MM-DD` | `@you` | `CODE` | *Short title of the problem* | *What is wrong, where is it, how did it happen?* | *What breaks or becomes risky if this is not fixed?* | *File, module, or service* | `PX` | `S` | `#000` | 🔴 Open | `Sprint X` | — | — |

---

## Phase 3 — QA / Testing / Security Debt 🔐

> **When does debt go here?**
> Missing or skipped tests, low code coverage, security vulnerabilities, hardcoded secrets committed
> to git, unvalidated user inputs, missing rate limiting on public APIs, or features shipped without
> QA sign-off.

> **💡 Security is the most dangerous debt category.** A P0 security issue can destroy user trust
> overnight. Run `npm audit` or `pip-audit` regularly to catch dependency vulnerabilities.
> Use tools like [GitGuardian](https://www.gitguardian.com) or GitHub's Secret Scanning to catch
> committed secrets automatically.

| ID | Date | Logged By | Category | Title | Description | Impact | Affected Area | Priority | Effort | GH Issue | Status | Target Date | Resolved On | Notes |
|----|------|-----------|----------|-------|-------------|--------|---------------|----------|--------|----------|--------|-------------|-------------|-------|
| TD-004 *(example)* | 2026-10-16 | @alice | `SEC` | Stripe test API key committed to git history | A Stripe test key was accidentally pushed to `main` in commit `a3f91c2`. The key has been rotated immediately, but it still exists in git history and could be found by scanning `git log`. | If git history is ever made public or cloned by an attacker, the pattern can be exploited. The specific rotated key is no longer functional, but the practice of committing keys must be fixed. | `.env.example`, commit `a3f91c2` | P1 🔴 | S | [#33](https://github.com/your-org/repo/issues/33) | 🟡 In Progress | 2026-10-21 | — | Key rotated within 10 minutes of discovery. BFG Repo-Cleaner scheduled to purge git history. Pre-commit hooks (`git-secrets`) being added this sprint. |
| TD-005 *(example)* | 2026-10-16 | @alice | `TEST` | Zero unit or integration tests for entire payment module | The `payments/` module was shipped during MVP sprint with no automated tests of any kind. The module handles all billing logic including subscription creation, upgrades, and cancellations. | Any payment bug ships undetected into production. Very high business risk — financial errors or double-charges are possible. | `src/payments/`, `src/api/billing/` | P1 🔴 | L | [#41](https://github.com/your-org/repo/issues/41) | 🔴 Open | Sprint 6 | — | Using Stripe test mode only until resolved. Real billing is feature-flagged off. |
| `TD-XXX` | `YYYY-MM-DD` | `@you` | `SEC` | *Short title of the problem* | *What is wrong, where is it, how did it happen?* | *What breaks or becomes risky if this is not fixed?* | *File, module, or service* | `PX` | `M` | `#000` | 🔴 Open | `Sprint X` | — | — |

---

## Phase 4 — AI-Generated Code Debt 🤖

> **When does debt go here?**
> Any shortcut or mistake introduced specifically by AI coding tools such as Claude, ChatGPT,
> GitHub Copilot, Cursor, or similar assistants. This includes:
> - Generated code that was merged without line-by-line review
> - Logic that looks correct but contains subtle bugs or wrong assumptions
> - AI-written tests that cover only the happy path and miss edge cases
> - Functions generated with hallucinated library APIs that do not actually exist
> - Code that works today but relies on deprecated or undocumented behaviours

> **⚠️ The Golden Rule of AI Code:** AI tools are a fast first draft — not a finished product.
> Every line generated by an AI must be read, understood, and truly owned by a human developer
> before it is merged. If you merged without fully reviewing, log it here.

> **💡 Beginner tip:** Go through every PR from the past month where you used Claude, ChatGPT,
> or Copilot. For any function you accepted without fully reading every line — add a row here.

| ID | Date | Logged By | AI Tool Used | Category | Title | Description | Impact | Affected Area | Was Code Reviewed Line-by-Line? | Priority | Effort | GH Issue | Status | Target Date | Resolved On | Notes |
|----|------|-----------|-------------|----------|-------|-------------|--------|---------------|-------------------------------|----------|--------|----------|--------|-------------|-------------|-------|
| TD-006 *(example)* | 2026-10-17 | @alice | Claude 3.7 | `AI` + `SEC` | AI-generated JWT middleware ignores token expiry field | Claude generated a JWT authentication middleware in Sprint 3. The middleware correctly verifies the token's signature but does NOT check the `exp` (expiry) field. Merged directly under deadline pressure. | Any user with an expired JWT can access all protected routes indefinitely. Critical authentication bypass vulnerability. | `middleware/auth.ts` | ❌ No — merged directly | P0 🚨 | S | [#45](https://github.com/your-org/repo/issues/45) | 🟡 In Progress | 2026-10-17 (hotfix) | — | HOTFIX DEPLOYED same day. Expiry check added. Full middleware audit scheduled for Sprint 5. Pre-commit checklist added: "Did you verify all generated auth code manually?" |
| TD-007 *(example)* | 2026-10-18 | @alice | ChatGPT-4o | `AI` + `TEST` | AI-generated tests cover only happy path — all edge cases missing | ChatGPT generated 12 unit tests for `UserService`. All tests use perfectly formatted inputs (valid email, valid name, valid password). Zero tests for null inputs, empty strings, invalid email formats, duplicate emails, or concurrent registrations. | Creates a false sense of security. Code coverage dashboard shows 87%, but all critical failure paths are entirely untested. | `tests/unit/UserService.test.ts` | ✅ Reviewed, but coverage gaps were missed | P2 🟡 | M | [#52](https://github.com/your-org/repo/issues/52) | 🔴 Open | Sprint 7 | — | Action: Audit all AI-generated test files for negative-path coverage. Add coverage thresholds to CI pipeline. |
| `TD-XXX` | `YYYY-MM-DD` | `@you` | `Claude / ChatGPT / Copilot / Other` | `AI` | *Short title of the problem* | *What the AI generated that is now a problem and how it was introduced* | *What breaks or becomes risky if this is not fixed?* | *File or module* | `✅ Yes / ❌ No` | `PX` | `S` | `#000` | 🔴 Open | `Sprint X` | — | — |

---

## Phase 5 — Deployment, Scaling & Post-Launch Debt 🚀

> **When does debt go here?**
> Infrastructure shortcuts taken to ship fast — manual deployments, missing monitoring and alerting,
> no database backups, hardcoded environment configuration, no rate limiting on public APIs, fragile
> mobile build processes, or missing analytics. This phase covers everything from your first deploy
> through your first 500 customers.

> **💡 Customer Milestone Awareness:** The extra `Acceptable Until` column tracks how many users
> you can safely have before this debt becomes critical. Some items are fine at 10 users but
> become P0 at 200. Be realistic — it is better to fix early than to scramble during a crisis.

| ID | Date | Logged By | Category | Title | Description | Impact | Affected Area | Priority | Effort | GH Issue | ⚠️ Acceptable Until | Status | Target Date | Resolved On | Notes |
|----|------|-----------|----------|-------|-------------|--------|---------------|----------|--------|----------|---------------------|--------|-------------|-------------|-------|
| TD-008 *(example)* | 2026-10-19 | @alice | `INFRA` | No error monitoring in production — errors are invisible | Errors thrown in production are only discovered when a user reports them via email or social media. No Sentry, Datadog, Rollbar, or equivalent is configured. | Bugs can exist for hours or days without the team knowing. Mean Time to Detect (MTTD) is currently measured in days, not minutes. | All services, all environments | P1 🔴 | S | [#61](https://github.com/your-org/repo/issues/61) | **50 users** | 🔴 Open | Sprint 5 | — | Sentry free tier is sufficient for current scale. Setup time: ~2 hours. Budget: $0. |
| TD-009 *(example)* | 2026-10-19 | @alice | `INFRA` | No automated database backup strategy — complete data loss risk | The production database has never been backed up. No automated backup schedule has been configured. There is no tested restore process. | A single corrupt migration, accidental deletion, or cloud provider outage could result in permanent and total loss of all user data. Existential risk to the business. | PostgreSQL on Railway | P0 🚨 | S | [#62](https://github.com/your-org/repo/issues/62) | **Never — fix before first real user** | 🟡 In Progress | 2026-10-20 | — | Railway daily automated backups enabled 2026-10-20. Point-in-time recovery to be evaluated. Restore test to be run before launch. |
| TD-010 *(example)* | 2026-10-20 | @alice | `PERF` | Dashboard stats API runs full DB aggregation on every request with no caching | The `/api/dashboard/stats` endpoint is called on every page load and executes a full database aggregation query each time. No caching layer exists. Currently takes ~800ms per call. | As user count grows, this will cause database CPU spikes and degraded response times for all users. At 100 concurrent users this query will likely timeout. | `src/api/dashboard.ts`, PostgreSQL | P2 🟡 | M | [#70](https://github.com/your-org/repo/issues/70) | **100 users** | 🔴 Open | Sprint 8 | — | Evaluate Redis or simple in-memory caching with a 60-second TTL as first step. |
| `TD-XXX` | `YYYY-MM-DD` | `@you` | `INFRA` | *Short title of the problem* | *What is wrong, where is it, how did it happen?* | *What breaks or becomes risky if this is not fixed?* | *File, module, or infra component* | `PX` | `M` | `#000` | `X users` | 🔴 Open | `Sprint X` | — | — |

---

---

# 🗺 Remediation Roadmap

> **Purpose:** The register tells you *what* the debt is. The roadmap tells you *when* you will fix it.
> Update this section at every sprint planning session.

> **Why this matters:** A list of problems without a plan is just a worry list. This roadmap turns
> debt awareness into debt action. Without it, P2 items sit unresolved for months.

---

## 📌 Current Sprint Debt Focus

> List every debt item you have committed to resolving in the current sprint.
> Be realistic — do not over-commit.

| Sprint / Week | Debt ID | Item Title | Priority | Owner | Effort | Notes |
|---------------|---------|-----------|----------|-------|--------|-------|
| Sprint 5 (Oct 21 – Nov 4) | TD-006 | AI auth middleware ignores token expiry | P0 🚨 | @alice | S | Hotfix deployed. Full middleware audit this sprint. |
| Sprint 5 (Oct 21 – Nov 4) | TD-009 | No automated database backups | P0 🚨 | @alice | S | Backups enabled. Run restore test before end of sprint. |
| Sprint 5 (Oct 21 – Nov 4) | TD-008 | No error monitoring in production | P1 🔴 | @alice | S | Sentry free tier. ~2 hours setup. |
| `Sprint X (dates)` | `TD-XXX` | *Item title* | `PX` | `@you` | `M` | *notes* |

---

## 📅 Must-Resolve Before Each Customer Milestone

> This table is your non-negotiable checklist. Before reaching each milestone, every item
> in that row must be ✅ Resolved. No exceptions for P0 items.

| Customer Milestone | Debt Items That MUST Be Resolved | Priority | Why It Cannot Wait |
|-------------------|----------------------------------|----------|-------------------|
| **Before any real user (Beta launch)** | TD-006, TD-009 | P0 🚨, P0 🚨 | Authentication bypass + data loss risk. Both are existential. |
| **Before 50 users** | TD-004, TD-005, TD-008 | P1, P1, P1 | Security, payment safety, and production visibility. |
| **Before 100 users** | TD-001, TD-002, TD-010 | P1, P2, P2 | Database concurrency will break. API versioning blocks mobile updates. Performance will degrade. |
| **Before 200 users** | TD-003, TD-007 | P2, P2 | Role management bugs become likely. False test coverage will hide real bugs. |
| **Before 500 users** | All remaining P3s | P3 🟢 | Clean up the backlog. Prepare for the next growth phase. |

---

## ✅ Resolved Debt Archive

> When an item is resolved, move it here from its phase table.
> **Never delete resolved items** — they are your audit trail and your project history.
> Future team members will want to know why certain decisions were made.

| ID | Title | Category | Priority | Phase | Resolved On | Resolved By | How It Was Fixed | Time Taken |
|----|-------|----------|----------|-------|-------------|-------------|-----------------|-----------|
| — | *No resolved items yet — you are just getting started!* | — | — | — | — | — | — | — |

---

---

# 🔗 GitHub Integration Guide

> This section shows you how to connect every debt item in this register to a GitHub Issue,
> so debt is visible in your normal development workflow — not buried in a separate document.

---

## ⚙️ One-Time Setup (5 minutes)

### Step 1 — Create the `technical-debt` Label
1. Go to your GitHub repository
2. Click **Issues** → **Labels** → **New label**
3. Name: `technical-debt` | Color: `#e4a400` (gold/yellow)
4. Click **Create label**

### Step 2 — Create Priority Labels (Optional but Recommended)
Create these additional labels for fast filtering in GitHub:

| Label Name | Color Hex | What It Means |
|-----------|-----------|--------------|
| `P0-critical` | `#B60205` (dark red) | Drop everything |
| `P1-high` | `#E4491C` (orange-red) | Fix this sprint |
| `P2-medium` | `#FBCA04` (yellow) | Fix next sprint |
| `P3-low` | `#0E8A16` (green) | Fix when time allows |
| `P4-negligible` | `#C5DEF5` (light blue) | Someday backlog |

### Step 3 — Create a GitHub Project Board (Optional but Recommended)
1. Go to your GitHub org or repo → **Projects** → **New project**
2. Choose **Board** layout
3. Create these columns:
   - `📋 Debt Backlog` (for all Open items)
   - `🟡 In Progress` (for items being actively worked on)
   - `✅ Resolved` (for closed items)
4. Add every debt issue to this board for a visual kanban view

---

## 📝 How to Create a Debt Issue Correctly

When logging a new debt item, create the GitHub Issue like this:

**Issue Title Format:**
```
[TD-XXX] Short title matching this register
```
*Example:* `[TD-005] Zero unit tests for payment module`

**Issue Description Template (paste this into every new debt issue):**
```markdown
## Technical Debt Item

**Register ID:** TD-005
**Category:** TEST — Testing & QA
**Priority:** P1 🔴 (High)
**Effort:** L (3–5 days)
**Phase:** Phase 3 — QA / Testing / Security
**Logged By:** @alice
**Date Logged:** 2026-10-16

## Description
The entire `payments/` module was shipped with no unit or integration tests during the MVP sprint.

## Impact
Any payment bug ships undetected into production. Risk of double-charges or failed subscription logic going unnoticed.

## Affected Area
`src/payments/`, `src/api/billing/`

## Acceptance Criteria (Definition of Done)
- [ ] Minimum 80% line coverage on all files in `src/payments/`
- [ ] Integration test for happy-path subscription creation
- [ ] Integration test for subscription cancellation
- [ ] Integration test for failed payment retry
- [ ] All tests pass in CI pipeline

## Links
- 📋 Technical Debt Register: [Link to this file or Notion page]
- Related PR: #___
```

**Labels to apply:** `technical-debt` + `P1-high`

---

## 🔗 Linking Issues Back in This Register

In the `GH Issue` column of the register tables, use this format:

```markdown
[#45](https://github.com/your-org/your-repo/issues/45)
```

This creates a clickable link directly to the issue when this file is viewed on GitHub.

---

---

# 🧠 Do's and Don'ts

> Quick reference for anyone using this register for the first time.

| ✅ Do This | ❌ Never Do This |
|-----------|----------------|
| Log debt the moment you create it | Wait until "later" to log debt — later never comes |
| Be honest about priority levels | Downgrade a P0 to P2 to feel better |
| Create a GitHub Issue for every item | Leave the `GH Issue` column blank for more than 24 hours |
| Write one item per row | Combine two different problems in one row |
| Keep resolved items in the archive | Delete resolved rows |
| Review this register every sprint | Only look at this when something breaks |
| Dedicate 20% of every sprint to debt | Spend 100% of every sprint on new features |
| Use specific file paths in Affected Area | Write "the whole backend" — be specific |
| Review AI-generated code line by line | Merge AI output directly without reading every line |
| Run `npm audit` or `pip-audit` every sprint | Ignore dependency vulnerabilities |

---

---

# 📚 Glossary

> New to software development? These definitions will help. Even experienced developers should
> read this — teams often use these terms differently.

| Term | Simple Definition |
|------|------------------|
| **Technical Debt** | A shortcut taken now that creates extra work later. Like using sticky tape instead of proper glue — it holds today but you will have to redo it properly eventually. |
| **Debt Register** | This document. A centralised list of all known shortcuts and quick fixes, with enough detail to track, prioritise, and plan the work to fix them. |
| **Remediation** | The act of fixing a debt item. "Remediating TD-005" means working on it until it is resolved and the `Status` can be set to `✅ Resolved`. |
| **Debt Paydown** | Deliberately spending development time fixing existing debt instead of building new features. Like paying off a credit card instead of buying more things. |
| **Sprint** | A fixed period of focused work (usually 1 or 2 weeks). At the end of each sprint, the team ships something and plans the next sprint. |
| **SDLC** | Software Development Life Cycle. The full journey from idea → design → build → test → deploy → maintain. |
| **ADLC** | AI-Driven Development Life Cycle. An SDLC where AI tools (like Claude, Copilot, or Cursor) are used to accelerate coding, testing, and review. |
| **CI/CD** | Continuous Integration / Continuous Deployment. Automated pipelines that run tests and deploy code every time you push to GitHub. |
| **ADR** | Architecture Decision Record. A short document explaining *why* a major technical choice was made, written at the time of the decision. |
| **CVE** | Common Vulnerabilities and Exposures. A publicly known security vulnerability in a software package or library. Found via `npm audit` or similar. |
| **MTTD** | Mean Time to Detect. The average time between when a bug is introduced and when the team realises it exists. Good monitoring reduces MTTD. |
| **Happy Path** | The scenario where everything goes perfectly — valid input, user does the expected thing, no errors. Bugs hide off the happy path. |
| **Refactor** | Rewriting existing code to be cleaner, simpler, or better-structured — without changing what the code actually does for the user. |
| **P0 / P4** | Priority labels. P0 = most urgent (fix immediately). P4 = least urgent (someday). See the Priority Levels table for full descriptions. |
| **GitHub Issue** | A task card in GitHub where you track a bug, feature, or debt item. Each issue has a number (e.g., #45) and can have labels, assignees, and comments. |
| **JWT** | JSON Web Token. A secure string passed between a client (browser/app) and a server to prove who a user is. Must be validated carefully. |
| **WAL Mode** | Write-Ahead Logging. A performance mode for SQLite that partially reduces the concurrency limitation. A workaround, not a full solution. |
| **OWASP** | Open Web Application Security Project. A non-profit that publishes the [Top 10 most common web security vulnerabilities](https://owasp.org/www-project-top-ten/). |
| **GDPR** | General Data Protection Regulation. EU law governing how software products collect, store, and use personal data about users. |

---

---

# 📋 Template Version History

> Track changes to this template itself here (not changes to individual debt items).

| Version | Date | Changed By | What Changed |
|---------|------|------------|-------------|
| v1.0 | 2026-10-14 | *(Register Owner)* | Initial template created |
| `v1.X` | `YYYY-MM-DD` | `@you` | *Describe your change — e.g., "Added mobile-specific columns to Phase 5"* |

---

*📄 Template type: **SaaS Web App + Mobile App (iOS & Android)***
*👤 Optimised for: **Solo founders and small teams (1–10 people)***
*🔗 Issue tracking: **GitHub Issues + GitHub Projects***
*📏 Priority system: **P0 (Critical) → P4 (Negligible)***
*🤖 Includes: **Dedicated AI-generated code debt tracking (Phase 4)***
*📈 Coverage: **Ideation → MVP → QA → Launch → First 500 customers***
*🗓 Template version: **v1.0 — 2026-10-14***

---

> **🧠 Remember:** Technical debt is not a sign of failure.
> It is a sign that you shipped something real under real constraints.
> The sign of failure is not tracking it — and being surprised when it bites.
>
> *Every great product has a debt register. Now yours does too.*
