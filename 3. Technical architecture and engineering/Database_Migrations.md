# 📋 Database Migrations Template
> **Project:** `[PROJECT_NAME]` · **Version:** `1.0` · **Last Updated:** `[DATE]`

---

<!-- ============================================================
  👋 HOW TO FILL THIS DOCUMENT — READ THIS FIRST!
  ============================================================
  
  Hi! Welcome to the Database Migrations Template.
  
  This document helps your team safely change the database as your
  product grows — from the very first line of code all the way to 
  your first 500 real customers.

  📌 A "database migration" is simply a change to how your database
     is organized — like adding a new column, renaming a table, or 
     deleting old data you no longer need.

  📌 Think of it like renovating a house while people are living in it.
     You need a plan, a safety net, and someone to double-check your work.

  ✅ HOW TO USE THIS TEMPLATE:
  1. Replace every [PLACEHOLDER_IN_BRACKETS] with your actual information.
  2. Check off every ☐ checkbox as you complete each step.
  3. Never skip the "Pre-Migration Checklist" — it protects real data.
  4. Get the right people to sign off before running in Staging or Production.
  5. Fill in the "Lessons Learned" section AFTER the migration — future you will thank you!

  🤖 If an AI agent (like Claude, Copilot, or Cursor) is helping you:
     Jump straight to Section 10 — AI Agent Guardrails — and read it first.

  💡 GOLDEN RULE: When in doubt, ask your Tech Lead before running anything.
  ============================================================ -->

---

## 📑 Table of Contents

1. [Migration Identity Card](#1-migration-identity-card)
2. [What This Migration Does](#2-what-this-migration-does)
3. [Tech Stack & Tools](#3-tech-stack--tools)
4. [File Naming Convention](#4-file-naming-convention)
5. [Risk Classification](#5-risk-classification)
6. [Pre-Migration Safety Checklist](#6-pre-migration-safety-checklist)
7. [Environment Journey: Dev → QA → Staging → Production](#7-environment-journey-dev--qa--staging--production)
8. [Migration Scripts](#8-migration-scripts)
9. [Rollback Plan](#9-rollback-plan)
10. [🤖 AI Agent Guardrails](#10--ai-agent-guardrails)
11. [Approval Sign-Off](#11-approval-sign-off)
12. [Customer Milestone Gates](#12-customer-milestone-gates)
13. [Post-Migration Verification](#13-post-migration-verification)
14. [Lessons Learned](#14-lessons-learned)
15. [Appendix: Quick Reference](#15-appendix-quick-reference)

---

## 1. Migration Identity Card

> 📝 **Fill this in first.** This is your migration's "ID badge" — it tells everyone at a glance what this migration is, who owns it, and when it happened.

| Field | Value |
|---|---|
| **Migration ID** | `[YYYYMMDD_NNN]` — e.g., `20241014_001` |
| **Migration Name** | `[short_snake_case_description]` — e.g., `add_users_email_index` |
| **Full File Name** | `[YYYYMMDD_NNN_short_description.sql]` — e.g., `20241014_001_add_users_email_index.sql` |
| **Project Name** | `[PROJECT_NAME]` |
| **Product Phase** | ☐ Pre-Launch ☐ Beta ☐ Live — 0 customers ☐ Live — 1–10 ☐ Live — 11–100 ☐ Live — 101–500 |
| **Author** | `[Your Full Name]` |
| **Reviewer** | `[Reviewer's Full Name]` |
| **Date Created** | `[YYYY-MM-DD]` |
| **Target Environment** | ☐ Development ☐ QA ☐ Staging ☐ Production |
| **Related Ticket / Issue** | `[TICKET-123]` — link to GitHub Issue, Jira, Linear, etc. |
| **Related PR / Branch** | `[https://github.com/your-org/your-repo/pull/NNN]` |

---

## 2. What This Migration Does

> 📝 **Explain this like you're talking to a friend, not a computer.** If someone woke you up at 3 AM and asked "what did this migration do?" you should be able to answer in 2 sentences using this section.

### 2.1 Plain-English Summary

```
[Write 2–4 sentences describing what this migration changes and WHY.
 No technical jargon needed here.

 Example:
 "This migration adds an email index to the users table so that 
  login lookups are faster. Without it, searching for a user by 
  email was scanning the entire table, which would slow down as 
  we grow past 1,000 users."]
```

### 2.2 What Changes in the Database?

> ✅ Check ALL that apply. Be specific — "added" is not enough, say WHAT was added.

| Change Type | Affected Table / Collection | Column / Field | Notes |
|---|---|---|---|
| ☐ Add table | `[table_name]` | — | `[why?]` |
| ☐ Drop table | `[table_name]` | — | `[⚠️ DANGER: confirm data is safe to delete]` |
| ☐ Add column | `[table_name]` | `[column_name]` | `[data type, nullable?]` |
| ☐ Drop column | `[table_name]` | `[column_name]` | `[⚠️ DANGER: confirm no app code reads this]` |
| ☐ Rename column | `[table_name]` | `[old_name → new_name]` | `[update app code first!]` |
| ☐ Change column type | `[table_name]` | `[column_name]` | `[from type → to type]` |
| ☐ Add index | `[table_name]` | `[column(s)]` | `[unique? concurrent?]` |
| ☐ Drop index | `[table_name]` | `[index_name]` | `[why no longer needed?]` |
| ☐ Add foreign key | `[table_name]` | `[column_name → ref_table.id]` | `[cascade delete?]` |
| ☐ Add constraint | `[table_name]` | `[constraint details]` | `[not null? unique? check?]` |
| ☐ Seed / insert data | `[table_name]` | — | `[how many rows?]` |
| ☐ Update existing data | `[table_name]` | `[column_name]` | `[how many rows affected?]` |
| ☐ Delete existing data | `[table_name]` | — | `[⚠️ DANGER: is backup confirmed?]` |

### 2.3 Why Is This Migration Needed Now?

```
[Explain the business or technical reason driving this change.

 Examples:
 • "The new authentication feature requires storing OAuth tokens."
 • "Performance is degrading at 500 rows — we need an index now."
 • "GDPR requires we add a data_deleted_at soft-delete column."]
```

### 2.4 What Happens If We Skip or Delay This Migration?

```
[This helps prioritize urgency. Be honest.

 Examples:
 • "App will crash on login for new users — ship blocker."
 • "Queries will be slow but app still works — can delay 1 sprint."
 • "Reporting will be inaccurate — medium business risk."]
```

---

## 3. Tech Stack & Tools

> 📝 **Specify the exact tools used for THIS project.** This section helps any team member (or AI agent) run the migration correctly without guessing.

### 3.1 Database

| Field | Value |
|---|---|
| **Database Engine** | ☐ PostgreSQL `[version]` ☐ SQLite ☐ Supabase ☐ Cloud SQL ☐ Other: `[name]` |
| **Database Name** | `[db_name]` |
| **Host / Connection** | See `.env` → `DATABASE_URL` *(never paste credentials here)* |
| **ORM / Query Builder** | ☐ Prisma `[version]` ☐ SQLAlchemy / Alembic ☐ None (raw SQL) ☐ Other: `[name]` |

### 3.2 Migration Tool

| Field | Value |
|---|---|
| **Tool** | ☐ Prisma Migrate ☐ Alembic ☐ Raw SQL scripts ☐ Other: `[name]` |
| **Tool Version** | `[x.y.z]` |
| **Migrations Folder** | `[./prisma/migrations/]` or `[./alembic/versions/]` or `[./db/migrations/]` |
| **Run Command (Up)** | `[npx prisma migrate deploy]` or `[alembic upgrade head]` or `[psql -f migration.sql]` |
| **Run Command (Down / Rollback)** | `[npx prisma migrate diff]` or `[alembic downgrade -1]` or `[psql -f rollback.sql]` |

### 3.3 CI/CD Pipeline

| Field | Value |
|---|---|
| **CI/CD Tool** | ☐ GitHub Actions ☐ GitLab CI ☐ Bitbucket Pipelines ☐ Other: `[name]` |
| **Workflow File** | `[.github/workflows/migrate.yml]` |
| **Migration Runs On** | ☐ Every PR merge to `main` ☐ Manual trigger only ☐ Tagged release only |
| **Auto-Rollback Enabled?** | ☐ Yes — pipeline reverts on failure ☐ No — manual only |

### 3.4 AI Agent Involvement

| Field | Value |
|---|---|
| **AI Tool Used** | ☐ Claude / Claude Code ☐ GitHub Copilot ☐ Cursor ☐ None |
| **AI Role** | ☐ Wrote the migration script ☐ Reviewed the script ☐ Running the migration ☐ None |
| **Human Override Required?** | ☐ Yes — human must approve before AI executes ☐ No — AI can auto-run low-risk only |

> ⚠️ **See Section 10 for full AI Agent rules before proceeding.**

---

## 4. File Naming Convention

> 📝 **Every migration file MUST follow this naming format exactly.** This keeps 100s of projects consistent and prevents ordering conflicts.

### 4.1 Standard Format

```
YYYYMMDD_NNN_what_it_does.{sql|py|prisma}
```

| Part | Meaning | Example |
|---|---|---|
| `YYYYMMDD` | Date the migration was created | `20241014` |
| `NNN` | 3-digit sequence number for that day (001, 002…) | `001` |
| `what_it_does` | Short snake_case description (max 5 words) | `add_users_email_index` |
| `.sql` / `.py` | File extension matching your migration tool | `.sql` for raw, `.py` for Alembic |

### 4.2 Good vs. Bad Examples

| ✅ GOOD | ❌ BAD | Why Bad |
|---|---|---|
| `20241014_001_add_users_email_index.sql` | `migration1.sql` | Not sortable, no date |
| `20241015_001_drop_legacy_sessions_table.py` | `drop_sessions.py` | No date, no sequence |
| `20241015_002_add_stripe_customer_id_column.sql` | `AddStripeColumn_FINAL.sql` | No date, vague naming |

### 4.3 This Migration's File Name

```
[FILL IN HERE — e.g., 20241014_001_add_users_email_index.sql]
```

---

## 5. Risk Classification

> 📝 **Classify this migration honestly.** Higher risk = more approvals needed + mandatory backup. When unsure, go one level HIGHER.

### 5.1 Risk Level Guide

| Risk Level | What It Means | Examples | Required Actions |
|---|---|---|---|
| 🟢 **LOW** | Reversible. No data loss possible. App still works if migration fails. | Add index, add nullable column, add new table | Dry-run + Tech Lead review |
| 🟡 **MEDIUM** | Potentially disruptive. Some data could be affected. App may degrade. | Rename column, change data type, add NOT NULL constraint | Backup + DBA review + QA sign-off |
| 🔴 **HIGH** | Irreversible or destructive. Data loss possible. App may break. | Drop table, drop column, delete rows, change primary key | Full backup + DBA + Tech Lead + QA + rollback script tested |

### 5.2 This Migration's Risk Level

**Selected Risk Level:** ☐ 🟢 LOW &nbsp;&nbsp; ☐ 🟡 MEDIUM &nbsp;&nbsp; ☐ 🔴 HIGH

**Justification:**
```
[Explain WHY you chose this risk level in 1–2 sentences.

 Example: "MEDIUM — renaming a column requires updating app code in the same
 PR, and if code is deployed without the migration, queries will fail."]
```

### 5.3 Is This Migration Reversible?

| Question | Answer |
|---|---|
| Can this migration be undone without data loss? | ☐ Yes ☐ No ☐ Partially — `[explain]` |
| Is a rollback script written and tested? | ☐ Yes — see Section 9 ☐ No — explain: `[reason]` |
| Has the rollback script been tested in Development? | ☐ Yes ☐ No ☐ Not applicable |

---

## 6. Pre-Migration Safety Checklist

> 📝 **Do NOT skip this section.** Every single checkbox must be completed before running the migration in any environment beyond Development. These steps protect real data.

> 💡 **Tip:** Think of this like the pre-flight checklist pilots do. Even experienced pilots follow it every time — no exceptions.

### 6.1 Universal Pre-Flight Checks (All Environments)

| # | Check | Owner | Done? |
|---|---|---|---|
| 1 | Migration file follows naming convention (Section 4) | Author | ☐ |
| 2 | Migration script reviewed by at least one other person | Reviewer | ☐ |
| 3 | Dry-run executed — output reviewed and looks correct | Author | ☐ |
| 4 | Migration is idempotent (safe to run twice without breaking things) | Author | ☐ |
| 5 | No hardcoded environment values (no IDs, secrets, or env-specific paths) | Author | ☐ |
| 6 | App code changes and migration are in the **same PR** (if they're coupled) | Author | ☐ |
| 7 | Rollback script exists and has been tested in Development (🔴 HIGH risk only) | Author | ☐ |
| 8 | Related ticket / issue linked in Section 1 | Author | ☐ |

### 6.2 Backup & Snapshot (Required for MEDIUM and HIGH Risk)

| # | Check | Owner | Done? |
|---|---|---|---|
| 9 | Full database backup taken and confirmed restorable | DBA / DevOps | ☐ |
| 10 | Backup storage location documented below | DBA / DevOps | ☐ |
| 11 | Snapshot or export taken of ALL affected tables | Author | ☐ |
| 12 | Affected table row count recorded (before state) | Author | ☐ |

**Backup Details:**

| Field | Value |
|---|---|
| Backup Taken At | `[YYYY-MM-DD HH:MM UTC]` |
| Backup Storage Location | `[s3://bucket/path/backup_name.dump]` or `[describe location]` |
| Backup Verified Restorable? | ☐ Yes — restored to test instance ☐ No *(explain why)* |
| Affected Table Row Counts | `[table_name: NNN rows, table2: NNN rows]` |

### 6.3 Zero-Downtime Checklist (Required for Production)

> 💡 Zero-downtime means your users never see an error or outage while the migration runs.

| # | Check | Done? |
|---|---|---|
| 13 | Migration uses `CONCURRENTLY` for index creation (PostgreSQL) | ☐ |
| 14 | New columns are added as NULLABLE first, then constrained in a follow-up migration | ☐ |
| 15 | No table-level locks that would block reads or writes for > 1 second | ☐ |
| 16 | Large table migrations (> 100K rows) use batching — not a single UPDATE | ☐ |
| 17 | App can handle BOTH old and new schema simultaneously during deploy window | ☐ |
| 18 | Estimated migration duration: `[X minutes]` — confirmed acceptable | ☐ |

### 6.4 Dry-Run Results

> Run the migration in `--dry-run` or `--preview` mode and paste the output here.

```sql
-- PASTE DRY-RUN OUTPUT HERE
-- Command used: [npx prisma migrate diff --preview-feature] OR [alembic upgrade head --sql]
-- Date/Time: [YYYY-MM-DD HH:MM]
-- Environment: [Development]

[paste output here]
```

**Dry-Run Assessment:**

| Question | Answer |
|---|---|
| Any unexpected changes shown? | ☐ No ☐ Yes — `[describe]` |
| Any warnings in the output? | ☐ No ☐ Yes — `[describe and resolution]` |
| Estimated execution time from dry-run | `[X seconds / minutes]` |

---

## 7. Environment Journey: Dev → QA → Staging → Production

> 📝 **Migrations must travel through ALL 4 environments in order.** Never skip straight to Production. Each environment is a safety gate.

> 🗺️ **The journey:** `Development` → `QA` → `Staging` → `Production`

---

### 7.1 🔵 DEVELOPMENT

> This is where you write and first test the migration. Nothing here is real data.

| Field | Value |
|---|---|
| **Status** | ☐ Not Started ☐ In Progress ☐ ✅ Complete ☐ ❌ Failed |
| **Executed By** | `[Name]` |
| **Executed At** | `[YYYY-MM-DD HH:MM UTC]` |
| **Command Used** | `[exact command]` |
| **Duration** | `[X seconds]` |
| **Result** | ☐ Success ☐ Failed — see notes |

**Dev Checklist:**

| Check | Done? |
|---|---|
| Migration runs without errors in local dev environment | ☐ |
| App starts and basic functions work after migration | ☐ |
| Rollback (down migration) tested successfully | ☐ |
| Unit / integration tests pass | ☐ |

**Notes / Issues Found in Dev:**
```
[Any problems encountered and how they were resolved.]
```

---

### 7.2 🟡 QA (Quality Assurance)

> QA tests that the migration works correctly and the app behaves as expected.

| Field | Value |
|---|---|
| **Status** | ☐ Not Started ☐ Waiting for Dev ☐ In Progress ☐ ✅ Complete ☐ ❌ Failed |
| **Executed By** | `[Name]` |
| **Executed At** | `[YYYY-MM-DD HH:MM UTC]` |
| **Command Used** | `[exact command]` |
| **Duration** | `[X seconds]` |
| **Result** | ☐ Success ☐ Failed — see notes |

**QA Checklist:**

| Check | QA Owner | Done? |
|---|---|---|
| Migration runs without errors on QA database | QA Engineer | ☐ |
| All automated test suites pass | QA Engineer | ☐ |
| Manual smoke test of affected features completed | QA Engineer | ☐ |
| Data integrity verified — no unexpected data changes | QA Engineer | ☐ |
| Performance tested — no significant query slowdowns | QA Engineer | ☐ |
| Rollback tested on QA database (MEDIUM/HIGH risk only) | QA Engineer | ☐ |

**QA Sign-Off:**

> QA must sign off before migration can proceed to Staging.

- **QA Engineer Name:** `[Name]`
- **Sign-Off Date:** `[YYYY-MM-DD]`
- **QA Decision:** ☐ ✅ Approved to proceed ☐ ❌ Blocked — reason: `[explain]`

**Notes / Issues Found in QA:**
```
[Bugs, unexpected behaviors, or data issues found. Include resolution.]
```

---

### 7.3 🟠 STAGING

> Staging is a production-like environment. Treat it with the same care as Production.

| Field | Value |
|---|---|
| **Status** | ☐ Not Started ☐ Waiting for QA ☐ In Progress ☐ ✅ Complete ☐ ❌ Failed |
| **Executed By** | `[Name]` |
| **Executed At** | `[YYYY-MM-DD HH:MM UTC]` |
| **Command Used** | `[exact command]` |
| **Duration** | `[X seconds]` |
| **Result** | ☐ Success ☐ Failed — see rollback log |

**Staging Checklist:**

| Check | Owner | Done? |
|---|---|---|
| Staging database backed up before migration | DBA | ☐ |
| Migration runs on staging production-like dataset | DevOps | ☐ |
| Full regression test suite passes | QA Engineer | ☐ |
| Performance metrics within acceptable range | QA Engineer | ☐ |
| Zero-downtime checklist (Section 6.3) confirmed | Tech Lead | ☐ |
| Rollback verified possible from this state | DBA | ☐ |

**Staging Sign-Off:**

- **Tech Lead Name:** `[Name]`
- **DBA Name:** `[Name]`
- **Sign-Off Date:** `[YYYY-MM-DD]`
- **Decision:** ☐ ✅ Approved for Production ☐ ❌ Blocked — reason: `[explain]`

**Notes / Issues Found in Staging:**
```
[Any issues found and resolved before proceeding.]
```

---

### 7.4 🔴 PRODUCTION

> ⚠️ **Real users. Real data. No second chances on destructive operations.** 

> 🚨 **STOP:** Has the "First Customer Gate" in Section 12 been reviewed? Check before proceeding.

| Field | Value |
|---|---|
| **Status** | ☐ Not Started ☐ Waiting for Staging ☐ Scheduled ☐ In Progress ☐ ✅ Complete ☐ ❌ Failed + Rolled Back |
| **Scheduled For** | `[YYYY-MM-DD HH:MM UTC]` — prefer low-traffic windows |
| **Executed By** | `[Name]` |
| **Executed At** | `[YYYY-MM-DD HH:MM UTC]` |
| **Command Used** | `[exact command]` |
| **Duration** | `[X seconds / minutes]` |
| **Result** | ☐ Success ☐ Failed — rollback executed |

**Production Execution Plan:**

| Step | Action | Owner | Time |
|---|---|---|---|
| 1 | Confirm all approvals collected (Section 11) | Tech Lead | T-30 min |
| 2 | Notify team in Slack / communication channel | Tech Lead | T-15 min |
| 3 | Confirm production backup is current (< 1 hour old) | DBA | T-10 min |
| 4 | Put app in maintenance mode (HIGH risk only) | DevOps | T-5 min |
| 5 | Execute migration | DevOps / CI/CD | T=0 |
| 6 | Monitor logs for errors (first 5 minutes) | DevOps | T+5 min |
| 7 | Run post-migration verification (Section 13) | Author + QA | T+10 min |
| 8 | Remove maintenance mode (if applied) | DevOps | T+15 min |
| 9 | Notify team — success or rollback | Tech Lead | T+15 min |

**Production Communication Log:**

| Time | Who | What Was Said / Done |
|---|---|---|
| `[HH:MM]` | `[Name]` | `[e.g., "Migration started"]` |
| `[HH:MM]` | `[Name]` | `[e.g., "Migration complete — monitoring"]` |
| `[HH:MM]` | `[Name]` | `[e.g., "All checks green — closed"]` |

---

## 8. Migration Scripts

> 📝 **Paste your actual migration code here.** This is the "recipe" for what changes in the database. Always include BOTH the "up" (apply) and "down" (undo) scripts.

### 8.1 Up Migration (Apply Changes)

> **File:** `[YYYYMMDD_NNN_description.sql]`

```sql
-- ============================================================
-- UP MIGRATION
-- Project:     [PROJECT_NAME]
-- Migration:   [YYYYMMDD_NNN_description]
-- Author:      [Your Name]
-- Date:        [YYYY-MM-DD]
-- Description: [One-line summary of what this does]
-- Risk Level:  [LOW / MEDIUM / HIGH]
-- ============================================================

-- [PASTE YOUR UP MIGRATION SQL HERE]

-- Example (replace with your actual code):
-- BEGIN;
--
--   ALTER TABLE users
--     ADD COLUMN email_verified_at TIMESTAMPTZ;
--
--   CREATE INDEX CONCURRENTLY idx_users_email
--     ON users (email);
--
-- COMMIT;
```

> **Or for Prisma (`schema.prisma` changes):**

```prisma
// PASTE RELEVANT PRISMA SCHEMA CHANGES HERE
// Example:
// model User {
//   id               Int       @id @default(autoincrement())
//   email            String    @unique
//   emailVerifiedAt  DateTime?
// }
```

> **Or for Alembic (Python):**

```python
# PASTE YOUR ALEMBIC UPGRADE FUNCTION HERE
# def upgrade():
#     op.add_column('users', sa.Column('email_verified_at', sa.DateTime(), nullable=True))
#     op.create_index('idx_users_email', 'users', ['email'], unique=True)
```

### 8.2 Down Migration (Rollback / Undo)

> **File:** `[YYYYMMDD_NNN_description_rollback.sql]` or same file with `downgrade()` function

```sql
-- ============================================================
-- DOWN MIGRATION (ROLLBACK)
-- Reverses the changes made by the UP migration above.
-- Test this in Development BEFORE running UP in Production.
-- ============================================================

-- [PASTE YOUR DOWN / ROLLBACK SQL HERE]

-- Example:
-- BEGIN;
--
--   DROP INDEX CONCURRENTLY IF EXISTS idx_users_email;
--
--   ALTER TABLE users
--     DROP COLUMN IF EXISTS email_verified_at;
--
-- COMMIT;
```

### 8.3 Data Verification Queries

> Run these AFTER the migration to confirm it worked correctly.

```sql
-- ============================================================
-- VERIFICATION QUERIES
-- Run these after the migration to confirm success.
-- ============================================================

-- [PASTE VERIFICATION QUERIES HERE]

-- Examples:
-- 1. Confirm new column exists:
--    SELECT column_name, data_type, is_nullable
--    FROM information_schema.columns
--    WHERE table_name = 'users' AND column_name = 'email_verified_at';

-- 2. Confirm index exists:
--    SELECT indexname FROM pg_indexes WHERE tablename = 'users';

-- 3. Confirm row count is unchanged (for non-data migrations):
--    SELECT COUNT(*) FROM users;
```

---

## 9. Rollback Plan

> 📝 **Every migration needs an exit plan.** This section answers: "What do we do if things go wrong?"

> 💡 **Analogy:** This is your emergency parachute. You hope you never need it, but it MUST be packed before the jump.

### 9.1 Rollback Strategy

**Selected Strategy:** ☐ Automated CI/CD Rollback ☐ Manual Rollback Script ☐ Database Snapshot Restore ☐ Forward Fix Only

**Automated CI/CD Rollback Configuration:**
```yaml
# GitHub Actions example — paste your workflow snippet here
# on:
#   workflow_run:
#     workflows: ["Run Migrations"]
#     types: [completed]
# jobs:
#   rollback-on-failure:
#     if: ${{ github.event.workflow_run.conclusion == 'failure' }}
#     steps:
#       - run: npx prisma migrate resolve --rolled-back [migration_name]
```

### 9.2 Rollback Decision Matrix

| Situation | Action | Who Decides | Time Limit |
|---|---|---|---|
| Migration fails mid-run (CI/CD catches it) | Auto-rollback triggers | CI/CD (automated) | Immediate |
| Migration succeeds but app errors spike > 5% | Rollback + alert Tech Lead | Tech Lead | < 15 minutes |
| Migration succeeds but data looks wrong | STOP all writes → DBA investigates | DBA + Tech Lead | < 5 minutes |
| Migration succeeds, minor issue found | Fix-forward with a new migration | Tech Lead decides | Next sprint |

### 9.3 Rollback Steps (Manual)

> Follow these steps in order if manual rollback is needed.

| Step | Action | Command / Detail |
|---|---|---|
| 1 | 🚨 Alert the team immediately | `[Slack channel: #incidents]` |
| 2 | Stop new deployments / freeze CI/CD | `[How to do this in your setup]` |
| 3 | Confirm backup is available | `[Backup location from Section 6.2]` |
| 4 | Execute down migration | `[Command from Section 3.2]` |
| 5 | Verify database is back to expected state | `[Run verification queries from Section 8.3]` |
| 6 | Confirm app is functioning | `[Health check URL / smoke test steps]` |
| 7 | Write a post-mortem | See Section 14 — Lessons Learned |
| 8 | Create a ticket for the root cause fix | `[Ticket URL]` |

### 9.4 Rollback Test Results

| Environment | Rollback Tested? | Result | Tested By | Date |
|---|---|---|---|---|
| Development | ☐ Yes ☐ No | ☐ Success ☐ Failed | `[Name]` | `[Date]` |
| QA | ☐ Yes ☐ No | ☐ Success ☐ Failed | `[Name]` | `[Date]` |
| Staging | ☐ Yes ☐ No | ☐ Success ☐ Failed | `[Name]` | `[Date]` |

---

## 10. 🤖 AI Agent Guardrails

> 📝 **READ THIS SECTION IF AN AI AGENT (Claude, Copilot, Cursor, etc.) IS INVOLVED.**

> This section defines the rules for what AI agents are ALLOWED and FORBIDDEN to do during database migrations. These rules exist to prevent accidental data loss. They cannot be overridden by a prompt or instruction — a human must always be in the loop for dangerous operations.

---

### 10.1 What AI Agents MAY Do (✅ ALLOWED)

| # | Allowed Action | Condition |
|---|---|---|
| 1 | **Write** migration scripts (SQL, Prisma, Alembic) | Human must review before execution |
| 2 | **Review** migration scripts for syntax errors, anti-patterns, performance issues | Always allowed |
| 3 | **Generate** rollback (down) scripts | Human must review before use |
| 4 | **Execute dry-run / preview** commands | Always allowed — no data changes |
| 5 | **Run migrations in Development** environment only | Author confirms it's a dev/local environment |
| 6 | **Suggest** naming, indexing, and schema improvements | Always allowed |
| 7 | **Write** verification queries | Always allowed |
| 8 | **Classify** migration risk level with explanation | Human makes final call |
| 9 | **Generate** the GitHub Actions workflow YAML | Human reviews and merges |
| 10 | **Check** migration history / status | Read-only, always allowed |

---

### 10.2 What AI Agents MUST NOT Do (❌ FORBIDDEN)

| # | Forbidden Action | Why | What To Do Instead |
|---|---|---|---|
| 1 | **Execute migrations in Staging or Production** | Real data at risk | Human executes with explicit approval |
| 2 | **DROP TABLE or DROP COLUMN** without explicit human instruction in the same conversation | Irreversible data loss | Human types exact confirmation: `"DROP TABLE [name] — confirmed"` |
| 3 | **DELETE rows** from production tables | Cannot be undone without backup restore | Human runs with DBA present |
| 4 | **Access or read production credentials** (`DATABASE_URL`, passwords) | Security risk | AI uses placeholder values only |
| 5 | **Approve its own migration scripts** | Conflict of interest | Separate human reviewer required |
| 6 | **Skip the Pre-Migration Safety Checklist** | Bypasses data protection | Checklist must always be completed |
| 7 | **Run a migration without confirming a backup exists** (MEDIUM/HIGH risk) | No recovery path if failure | Verify backup first, then proceed |
| 8 | **Modify migration files already applied** to any environment | Breaks migration history | Create a new migration instead |
| 9 | **Auto-merge a PR** containing a HIGH risk migration | Too dangerous for automation | Two human approvals required |
| 10 | **Invent or guess column names, types, or table relationships** without asking | Can corrupt data model | Always ask the human to clarify |

---

### 10.3 AI Agent Confirmation Protocol

> For any action that is ambiguous or could have irreversible consequences, the AI agent MUST follow this protocol:

```
BEFORE executing any migration in a non-Development environment, the AI agent 
must display the following and wait for explicit human confirmation:

┌─────────────────────────────────────────────────────────┐
│  ⚠️  MIGRATION EXECUTION CONFIRMATION REQUIRED          │
│                                                         │
│  Migration:   [YYYYMMDD_NNN_description]               │
│  Environment: [QA / Staging / Production]              │
│  Risk Level:  [LOW / MEDIUM / HIGH]                    │
│  Action:      [Describe what will happen]              │
│                                                         │
│  ✅ Backup confirmed:   [YES / NO]                      │
│  ✅ Dry-run complete:   [YES / NO]                      │
│  ✅ Human approvals:    [Names]                         │
│                                                         │
│  Type CONFIRM to proceed or CANCEL to abort.           │
└─────────────────────────────────────────────────────────┘
```

### 10.4 AI Agent Audit Log

> Every significant AI action must be logged here for traceability.

| Timestamp | AI Tool | Action Taken | Human Who Approved | Output / Result |
|---|---|---|---|---|
| `[YYYY-MM-DD HH:MM]` | `[Claude / Copilot / Cursor]` | `[Generated up migration SQL]` | `[Author Name]` | `[Reviewed and approved]` |
| `[YYYY-MM-DD HH:MM]` | `[Claude / Copilot / Cursor]` | `[Generated rollback script]` | `[Reviewer Name]` | `[Tested in Dev — passed]` |

---

## 11. Approval Sign-Off

> 📝 **Collect signatures here before running in Staging or Production.** No migration runs in production without all required approvals for its risk level.

### 11.1 Approval Requirements by Risk Level

| Approver | 🟢 LOW Risk | 🟡 MEDIUM Risk | 🔴 HIGH Risk |
|---|---|---|---|
| **Author (self-review)** | ✅ Required | ✅ Required | ✅ Required |
| **Tech Lead / Senior Dev** | ✅ Required | ✅ Required | ✅ Required |
| **QA Engineer** | Optional | ✅ Required | ✅ Required |
| **Database Administrator (DBA)** | Not required | ✅ Required | ✅ Required |
| **Second Tech Lead / Peer** | Not required | Not required | ✅ Required |

### 11.2 Approval Table

> Approvers: Add your name, date, and decision. Use `✅ Approved`, `❌ Blocked`, or `⏳ Pending`.

| Role | Name | Decision | Date | Notes |
|---|---|---|---|---|
| **Author** | `[Your Name]` | ☐ ✅ ☐ ❌ | `[Date]` | `[Confirm checklist complete]` |
| **Tech Lead** | `[Name]` | ☐ ✅ ☐ ❌ | `[Date]` | `[Concerns / conditions]` |
| **QA Engineer** | `[Name]` | ☐ ✅ ☐ ❌ | `[Date]` | `[Test results summary]` |
| **DBA** | `[Name]` | ☐ ✅ ☐ ❌ | `[Date]` | `[Schema review notes]` |
| **Second Approver** | `[Name]` | ☐ ✅ ☐ ❌ | `[Date]` | `[HIGH risk only]` |

### 11.3 Final Go / No-Go Decision

| Field | Value |
|---|---|
| **Final Decision** | ☐ 🟢 GO — All approvals collected, migration may proceed ☐ 🔴 NO-GO — See blocked notes above |
| **Decided By** | `[Tech Lead Name]` |
| **Decision Date** | `[YYYY-MM-DD]` |
| **Scheduled Production Window** | `[YYYY-MM-DD HH:MM – HH:MM UTC]` |

---

## 12. Customer Milestone Gates

> 📝 **As real customers use your product, database migrations carry more risk.** These gates ensure you pause and think harder as your user base grows.

> 💡 **Why does this matter?** When you have 0 users, a broken migration is just inconvenient. When you have 500 real users, it could mean lost data, outages, and reputation damage.

### 12.1 Milestone Gate: First Customer in Production 🚨

> **This gate is MANDATORY.** The moment your first real customer's data enters production, all future migrations require the full checklist — no shortcuts.

| Question | Answer | Required Action |
|---|---|---|
| Is this the first migration AFTER the first real customer signed up? | ☐ Yes ☐ No | If YES → full review required |
| Has production database been confirmed as having real customer data? | ☐ Yes ☐ No | If YES → DBA must be present |
| Has the team been notified this is a "live data" migration? | ☐ Yes ☐ No | Slack / standup announcement |

**First Customer Gate Sign-Off:**

- **Confirmed By:** `[Name]`
- **Date:** `[YYYY-MM-DD]`
- **Notes:** `[Any special considerations for this first real-data migration]`

### 12.2 Migration History by Customer Milestone

> Track migrations across your journey to 500 customers.

| Milestone | Migration Count | Risk Profile | Key Lessons |
|---|---|---|---|
| Pre-launch (0 customers) | `[N]` | Mostly schema setup | `[Notes]` |
| Beta / First customer | `[N]` | Careful — real data begins | `[Notes]` |
| 10 customers | `[N]` | Performance indexes needed? | `[Notes]` |
| 100 customers | `[N]` | Review migration timing (off-peak) | `[Notes]` |
| 500 customers | `[N]` | Zero-downtime mandatory | `[Notes]` |

---

## 13. Post-Migration Verification

> 📝 **The migration ran — now verify it actually worked correctly.** Don't close the ticket until all checks pass.

### 13.1 Automated Checks

| Check | Tool / Method | Expected Result | Actual Result | Pass? |
|---|---|---|---|---|
| Migration status shows as applied | `prisma migrate status` / `alembic current` | Latest migration listed | `[output]` | ☐ |
| App health endpoint returns 200 | `curl https://[app]/health` | `{"status": "ok"}` | `[output]` | ☐ |
| CI/CD pipeline shows green | GitHub Actions | All jobs pass | `[link]` | ☐ |
| Error rate in logs | Monitoring dashboard | < baseline | `[value]` | ☐ |
| Query performance for affected tables | EXPLAIN ANALYZE / APM | Within 10% of baseline | `[value]` | ☐ |

### 13.2 Data Integrity Checks

> Run the verification queries from Section 8.3 and record results.

| Query | Expected | Actual | Match? |
|---|---|---|---|
| Row count: `[table_name]` | `[N rows]` | `[N rows]` | ☐ Yes ☐ No |
| New column exists: `[column_name]` | Column present, type `[type]` | `[result]` | ☐ Yes ☐ No |
| Index exists: `[index_name]` | Index active | `[result]` | ☐ Yes ☐ No |
| Sample data spot check | `[describe what correct data looks like]` | `[result]` | ☐ Yes ☐ No |

### 13.3 Final Sign-Off

| Field | Value |
|---|---|
| **All verification checks passed?** | ☐ Yes — migration is complete ☐ No — see issues below |
| **Migration Closed By** | `[Name]` |
| **Closed At** | `[YYYY-MM-DD HH:MM UTC]` |
| **Issues Found Post-Migration** | `[None / describe issues and resolution]` |
| **Ticket / Issue Updated?** | ☐ Yes — marked Done ☐ No — still open |

---

## 14. Lessons Learned

> 📝 **Fill this in AFTER the migration is complete.** This is the most valuable section for your team's future migrations. Be honest — what went well and what didn't.

> 💡 Even if everything went perfectly, write it down! "It went smoothly because we did X" is just as valuable as "it failed because of Y."

### 14.1 What Went Well?

```
[List 2–5 things that worked perfectly.

 Example:
 • "The dry-run caught a typo in the column name before it hit QA."
 • "Automated rollback triggered correctly when we tested failure in Staging."
 • "Zero-downtime index creation with CONCURRENTLY worked flawlessly."]
```

### 14.2 What Could Be Improved?

```
[List 2–5 things that were harder than expected or could be better.

 Example:
 • "The backup took 20 minutes — we should move this to a pre-scheduled job."
 • "We forgot to update the app code alongside the column rename."
 • "QA approval took 3 days — need async review process."]
```

### 14.3 Surprises or Unexpected Issues

```
[Anything that caught you off guard — even small things.

 Example:
 • "Adding an index on a 500K row table took 8 minutes, not 30 seconds."
 • "Supabase required a specific permission to run CONCURRENTLY."]
```

### 14.4 Action Items for the Team

| Action Item | Owner | Due Date | Status |
|---|---|---|---|
| `[e.g., Add backup automation to CI/CD pipeline]` | `[Name]` | `[Date]` | ☐ Open |
| `[e.g., Update migration checklist based on learnings]` | `[Name]` | `[Date]` | ☐ Open |
| `[e.g., Document Supabase permission requirements]` | `[Name]` | `[Date]` | ☐ Open |

### 14.5 Template Improvement Suggestions

```
[Suggest any changes to THIS template that would make it better for the next migration.
 These suggestions may be incorporated into the next version of Database_Migrations.md.]
```

---

## 15. Appendix: Quick Reference

> 📝 **Cheat sheet for the most common tasks. Bookmark this!**

### 15.1 Migration Commands Quick Reference

| Action | Prisma | Alembic | Raw SQL (psql) |
|---|---|---|---|
| Create new migration | `npx prisma migrate dev --name [name]` | `alembic revision -m "[name]"` | Create `.sql` file manually |
| Apply all pending | `npx prisma migrate deploy` | `alembic upgrade head` | `psql -U user -d db -f file.sql` |
| Dry-run / preview | `npx prisma migrate diff` | `alembic upgrade head --sql` | Review SQL manually |
| Check status | `npx prisma migrate status` | `alembic current` | Query `schema_migrations` table |
| Rollback one step | `npx prisma migrate resolve --rolled-back [name]` | `alembic downgrade -1` | Run rollback `.sql` file |
| Rollback to specific | N/A | `alembic downgrade [revision]` | Run rollback `.sql` file |

### 15.2 Risk Level Quick Lookup

| Operation | Risk Level |
|---|---|
| Add new table | 🟢 LOW |
| Add nullable column | 🟢 LOW |
| Add index (concurrent) | 🟢 LOW |
| Add foreign key | 🟡 MEDIUM |
| Rename column | 🟡 MEDIUM |
| Add NOT NULL constraint | 🟡 MEDIUM |
| Change column data type | 🟡 MEDIUM |
| Backfill data (large table) | 🟡 MEDIUM |
| Drop column | 🔴 HIGH |
| Drop table | 🔴 HIGH |
| Delete rows | 🔴 HIGH |
| Change primary key | 🔴 HIGH |
| Truncate table | 🔴 HIGH |

### 15.3 PostgreSQL Zero-Downtime Patterns

```sql
-- ✅ Safe: Add column as nullable first
ALTER TABLE users ADD COLUMN phone VARCHAR(20);

-- ✅ Safe: Create index without locking (CONCURRENTLY)
CREATE INDEX CONCURRENTLY idx_users_phone ON users (phone);

-- ✅ Safe: Add NOT NULL in 3 steps (never in one ALTER)
-- Step 1: Add nullable column
ALTER TABLE users ADD COLUMN status VARCHAR(20);
-- Step 2: Backfill
UPDATE users SET status = 'active' WHERE status IS NULL;
-- Step 3: Add constraint (new migration)
ALTER TABLE users ALTER COLUMN status SET NOT NULL;

-- ❌ Dangerous in Production: Locks entire table
ALTER TABLE users ADD COLUMN status VARCHAR(20) NOT NULL DEFAULT 'active';
```

### 15.4 Supabase-Specific Notes

```sql
-- Supabase uses PostgreSQL — all psql commands work.
-- Run migrations via: Supabase Dashboard → SQL Editor
-- Or via CLI: supabase db push
-- Enable Row Level Security (RLS) after schema changes if using Supabase Auth:
ALTER TABLE your_table ENABLE ROW LEVEL SECURITY;
```

### 15.5 Environment Variables (Never Hardcode)

```bash
# Always use environment variables for database connections.
# Development
DATABASE_URL="postgresql://localhost:5432/myapp_dev"

# Never paste these into this document!
# Store in: .env (local), GitHub Actions Secrets (CI/CD), 
#           Vault / AWS Secrets Manager (production)
```

### 15.6 Glossary (Plain English)

| Term | What It Means |
|---|---|
| **Migration** | A versioned change to the database structure or data |
| **Schema** | The "blueprint" of your database — what tables and columns exist |
| **Rollback** | Undoing a migration to go back to the previous state |
| **Idempotent** | Safe to run multiple times — same result every time |
| **Dry-run** | Previewing what a migration WILL do, without actually doing it |
| **Index** | Like a book's index — helps the database find data faster |
| **Foreign key** | A link between two tables (like a "belongs to" relationship) |
| **NOT NULL** | A rule that says a column must always have a value |
| **CONCURRENTLY** | PostgreSQL keyword that adds an index without locking the table |
| **CI/CD** | Automated system that tests and deploys code changes |
| **DBA** | Database Administrator — the expert who manages database safety |

---

<!-- ============================================================
  📌 DOCUMENT METADATA
  ============================================================ -->

---

**Document Version:** `1.0`  
**Template Author:** `[Your Organization Name]`  
**Created:** `2024-10-14`  
**Last Updated:** `[YYYY-MM-DD]`  
**Next Review:** `[YYYY-MM-DD — recommended: after every 10 migrations or every quarter]`  

**Changelog:**

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | `2024-10-14` | `[Author]` | Initial template created |
| `[1.1]` | `[Date]` | `[Author]` | `[What changed]` |

---

*This template is designed for the AI-Driven Development Life Cycle — from the first line of code to your first 500 customers. When in doubt, go slower, ask for help, and always back up first.*
