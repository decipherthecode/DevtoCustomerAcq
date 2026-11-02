# 📖 Data Dictionary — [Project Name]

> **Document Type:** Data Dictionary
> **Template Version:** 1.0.0
> **AI-Driven Development Life Cycle (AIDLC) — From First Line of Code to First 500 Customers**

---

<!-- ============================================================
  🧭 HOW TO FILL THIS DOCUMENT — READ THIS FIRST
  ============================================================
  This section is your instruction manual.
  Delete this comment block AFTER the team has read it.
  ============================================================ -->

# 🧭 How to Fill This Document

> 🟢 **You don't need to be a developer to fill this.**
> Read each instruction below and fill in the sections that match your role.
> Every field has an example. Copy the example, change the details, and you're done.

## Step 1 — Fill the Document Header (5 minutes)
Go to the **📋 Document Header** section below.
Replace every `[PLACEHOLDER]` in square brackets with your real project information.
- **Project Name** = the name of the product you are building.
- **Owner** = the person responsible for keeping this document up to date.
- **Status** = `Draft` when you are still writing it. Change to `Active` once the team approves it.

## Step 2 — Add a Changelog Entry (2 minutes every time you update this file)
Go to the **📝 Changelog** section.
Every time someone changes this document, they add ONE row to the changelog table.
- Copy the last row, paste a new row, update the version number, date, name, and what changed.
- **Version rule:** If you add a new entity → increase the MAJOR number (1.0 → 2.0). If you add a new field → increase MINOR (1.0 → 1.1). If you fix a typo → increase PATCH (1.0 → 1.0.1).

## Step 3 — Fill the Glossary (10 minutes)
Go to the **📚 Glossary** section.
Write down any word in this project that might confuse a new team member.
Use plain English — imagine explaining it to a 10-year-old.
Example: "User" = "A person who has created an account in the app."

## Step 4 — Map Your Data Flow (15 minutes)
Go to the **🗺️ Data Flow Map** section.
For every place data travels in your product (e.g., from the app → to your database → to an AI model → back to the user), add one row.

## Step 5 — Define Every Entity (the main work — take your time)
Go to the **🗄️ Data Entities** section.
An "entity" is just a group of related data. Think of it like a spreadsheet tab.
- **SQL Entity** = a database TABLE (e.g., `users`, `orders`, `products`)
- **NoSQL Entity** = a database COLLECTION or DOCUMENT (e.g., `conversations`, `events`)
For EACH entity:
1. Copy the entity template block.
2. Fill in the table — one row per field (column/attribute).
3. Use the filled-in EXAMPLE row as your guide.

## Step 6 — Fill the AI/ML Data Section (if your product uses AI)
Go to the **🤖 AI & Machine Learning Data** section.
If your product sends data to an AI model (like OpenAI, Anthropic, or your own model), fill in:
- What you SEND to the AI (inputs / prompts).
- What the AI SENDS BACK (outputs / completions).
- Any data your AI agent "remembers" between messages (agent memory/state).

## Step 7 — Fill the Compliance Section
Go to the **🔒 Compliance & Data Governance** section.
For every field in your entity tables that contains personal information (name, email, address, health data), mark it in the PII Master List.
This is REQUIRED for GDPR, HIPAA, and SOC 2 compliance.

## Step 8 — Update per Lifecycle Stage
Go to the **📅 Lifecycle Stages** section.
As your product grows from an idea to 500 customers, fill in the relevant stage section.
You do NOT need to fill all stages at once — fill each one when you reach that stage.

## Step 9 — Get Sign-Off
Go to the **✅ Review & Sign-Off** section.
Before going to production, get the required people to sign off on this document.

---
> 🔵 **Tip for teams:** Pin this document in Slack, Notion, or your repo's `/docs` folder.
> 📌 **Rule:** This document is the SINGLE SOURCE OF TRUTH for all data definitions in this project.
---

&nbsp;

---

# 📋 Document Header

| Field                    | Value                                                                 |
|--------------------------|-----------------------------------------------------------------------|
| **Project Name**         | [e.g., MediAssist AI — Healthcare Appointment Booking App]            |
| **Document Title**       | Data Dictionary                                                       |
| **Document Status**      | `Draft` / `Under Review` / `Active` / `Deprecated`                   |
| **Current Version**      | 1.0.0                                                                 |
| **Created By**           | [Full Name, Role — e.g., Priya Sharma, Senior Engineer]               |
| **Document Owner**       | [Full Name, Role — person responsible for keeping this up to date]    |
| **Last Updated**         | [YYYY-MM-DD — e.g., 2026-10-14]                                       |
| **Reviewed By**          | [Full Name(s), Role(s)]                                               |
| **Approved By**          | [Full Name, Role]                                                     |
| **Project Repository**   | [GitHub / GitLab URL — e.g., https://github.com/your-org/your-repo]  |
| **Linked Documents**     | [PRD link], [Architecture Doc link], [API Docs link]                  |
| **Target Audience**      | Engineers · PMs · Data Scientists · QA · DevOps · Stakeholders       |
| **Deployment Platforms** | [e.g., Web (Next.js) + iOS + Android]                                 |
| **Primary Databases**    | [e.g., PostgreSQL (main), MongoDB (events), Pinecone (vectors)]       |
| **AI Providers Used**    | [e.g., Anthropic Claude 3.5, OpenAI GPT-4o, Self-hosted Llama 3]     |
| **Compliance Standards** | GDPR · CCPA · HIPAA · SOC 2 Type II · ISO 27001                      |

---

&nbsp;

---

# 📝 Changelog

> 📌 **Rule:** Add a new row EVERY TIME you change anything in this document.
> Never delete old rows — they are your audit trail.

| Version | Date       | Author               | Change Type              | What Changed                                                   |
|---------|------------|----------------------|--------------------------|----------------------------------------------------------------|
| 1.0.0   | 2026-10-14 | [Your Name]          | 🆕 Initial Creation      | Created document structure and first entity definitions        |
| 1.1.0   | [Date]     | [Name]               | ➕ New Entity Added      | Added `sessions` entity for AI agent conversation tracking     |
| 1.1.1   | [Date]     | [Name]               | ✏️ Field Update          | Updated `user.email` — added `UNIQUE` constraint note          |
| 1.2.0   | [Date]     | [Name]               | 🔒 Compliance Update     | Marked `user.date_of_birth` as PHI (HIPAA) in PII Master List  |
| 2.0.0   | [Date]     | [Name]               | 🏗️ Major Restructure     | Added `payments` entity; updated data flow map for Stripe      |

> **Change Types:** `🆕 Initial Creation` · `➕ New Entity` · `✏️ Field Update` · `🗑️ Field Removed` · `🔒 Compliance Update` · `🏗️ Major Restructure` · `🐛 Bug/Error Fix` · `📦 Migration Note`

---

&nbsp;

---

# 📚 Glossary of Terms

> 📌 **How to fill:** Add any word or phrase that might confuse a new team member, junior developer, or non-technical stakeholder. Write the definition in plain English — no jargon allowed in definitions!

| Term                  | Definition                                                                                                       | Used In               |
|-----------------------|------------------------------------------------------------------------------------------------------------------|-----------------------|
| **Entity**            | A group of related data stored together — like a table in a spreadsheet (e.g., `users`, `orders`)               | Entire document       |
| **Field / Attribute** | A single piece of information within an entity (e.g., `first_name` is a field inside the `users` entity)       | Entire document       |
| **PII**               | Personally Identifiable Information — any data that could identify a real person (name, email, phone, SSN)      | Compliance section    |
| **PHI**               | Protected Health Information — health-related data protected by HIPAA (diagnoses, prescriptions, test results)  | HIPAA section         |
| **Primary Key (PK)**  | A unique ID for every row in a table — no two rows can have the same PK (e.g., `user_id`)                       | SQL entities          |
| **Foreign Key (FK)**  | A field that points to the Primary Key of another table, linking two tables together (e.g., `order.user_id`)    | SQL entities          |
| **Index**             | A special lookup list the database uses to find records faster — like a book's index                            | SQL entities          |
| **Schema**            | The complete blueprint of a database — which entities exist, which fields each has, and how they relate         | Entire document       |
| **Embedding**         | A list of numbers (a "vector") that represents text/image meaning — used by AI for semantic search              | AI/ML section         |
| **Token**             | A chunk of text (roughly 4 characters) — AI models measure their input/output size in tokens                    | AI/ML section         |
| **Context Window**    | The maximum amount of text (in tokens) an AI model can read in one message                                      | AI/ML section         |
| **Agent Memory**      | Data an AI agent saves between turns in a conversation so it "remembers" earlier messages                       | AI/ML section         |
| **Data Lineage**      | The complete history of where a piece of data came from, how it was changed, and where it went                  | Data Flow section     |
| **Soft Delete**       | Marking a record as "deleted" without actually removing it — the row stays in the database with `deleted_at` set| Entity definitions    |
| **Idempotent**        | An operation that produces the same result no matter how many times you repeat it (safe to retry)               | API/integration notes |
| **Enum**              | A field that can only contain one of a fixed list of values (e.g., `status` can only be `active` or `inactive`)| Field definitions     |
| **[Add your term]**   | [Write a plain-English definition here]                                                                          | [Where it's used]     |

---

&nbsp;

---

# 🗺️ Data Flow Map

> 📌 **How to fill:** Trace the path of data through your product. Start from where data is CREATED, follow every step where it is READ, CHANGED, or COPIED, and end at where it is STORED or DISPLAYED. One row per data flow path.

> 💡 **Think of it like water pipes:** Where does the water come from? Which pipes does it travel through? Where does it end up?

| Flow ID | Flow Name                        | Data Source              | Trigger / Event           | Transformation / AI Step                              | Destination                   | Frequency      | Owner           | Notes / Risks                          |
|---------|----------------------------------|--------------------------|---------------------------|--------------------------------------------------------|-------------------------------|----------------|-----------------|----------------------------------------|
| DF-001  | User Registration                | Mobile App (signup form) | User submits signup form  | Validate email format → Hash password (bcrypt)        | `users` table (PostgreSQL)    | On event       | Auth Team       | Password never stored in plain text    |
| DF-002  | AI Chat Message Processing       | Web App (chat input)     | User sends a message      | Retrieve agent memory → Append context → Call LLM API | `messages` collection (Mongo) | On event       | AI Team         | Tokens counted before API call         |
| DF-003  | Feature Extraction for AI Model  | `users` + `events` tables| Nightly cron job (2am UTC)| Aggregate events → Normalize → Create feature vector  | `user_features` table (Postgres)| Daily batch   | Data Eng. Team  | Depends on DF-001 completing first     |
| DF-004  | User Deletion (GDPR/Right to Erase) | User request via app  | User clicks "Delete My Account" | Soft-delete user → Queue anonymization job        | All user-linked tables        | On event       | Privacy Team    | Must complete within 30 days per GDPR  |
| DF-005  | Analytics Event Ingestion        | Web + Mobile SDKs        | Any user interaction      | Enrich with session data → Deduplicate                | `events` collection (Mongo)   | Real-time      | Analytics Team  | Max latency: 2 seconds                 |
| [DF-XXX]| [Flow Name]                     | [Source]                 | [What triggers it]        | [What changes or processes the data]                  | [Where data lands]            | [How often]    | [Team/Person]   | [Risks, edge cases, dependencies]      |

---

&nbsp;

---

# 🗄️ Data Entities

> 📌 **How to fill this section:**
> - Copy the **Entity Template Block** below for EACH entity (table / collection) in your product.
> - Fill in the field table — one row per field.
> - The first row in each table is a **filled example** — use it as your guide, then delete it when done.
> - Sections marked `(SQL)` are for PostgreSQL/MySQL. Sections marked `(NoSQL)` are for MongoDB/DynamoDB/Firestore.

---

## Entity Template Block

> ⬇️ **COPY EVERYTHING BELOW THIS LINE for each new entity. Paste it at the bottom of this section.**

---

### 🟦 Entity: `entity_name`

> **Plain-English Description:** Write 1–2 sentences explaining what this entity is and why it exists. Example: "Stores every registered user in the system. One record = one person."

| Property               | Value                                                                 |
|------------------------|-----------------------------------------------------------------------|
| **Entity Name**        | `entity_name`                                                         |
| **Database Type**      | SQL (PostgreSQL) / NoSQL (MongoDB) / NoSQL (DynamoDB)                 |
| **Database Name**      | [e.g., `app_db`]                                                      |
| **Table / Collection** | [e.g., `users`]                                                       |
| **Environment**        | Development · Staging · Production                                    |
| **Estimated Row Count**| [e.g., 10,000 rows at launch; 500,000 at scale]                      |
| **Lifecycle Stage**    | Planning · Development · Launch · Post-Launch                         |
| **Primary Key**        | `[field_name]` (e.g., `id` — UUID)                                    |
| **Indexes**            | [e.g., `email` (UNIQUE), `created_at` (B-tree), `user_id` (FK index)]|
| **Relationships**      | [e.g., `users.id` → `orders.user_id` (one-to-many)]                  |
| **Entity Owner**       | [Team or Person responsible for this entity]                          |
| **Data Retention**     | [e.g., Keep indefinitely / Delete 7 years after account closure]      |
| **Soft Delete?**       | Yes (uses `deleted_at` field) / No (hard delete)                      |
| **Partitioning Key**   | [For NoSQL/DWH — e.g., `user_id`, `created_at`]                      |

#### 📊 Field Definitions

> **Column Guide:**
> - **Required?** → `✅ Yes` = must always have a value · `⚠️ Conditional` = required only in some cases · `❌ No` = optional
> - **PII/PHI?** → `🔴 PII` = personal data (GDPR/CCPA) · `🟣 PHI` = health data (HIPAA) · `⬜ None` = not personal
> - **AI Used?** → Does your AI model READ or WRITE this field? `✅ Yes` / `❌ No`
> - **Encrypted?** → Is this field encrypted at rest? `✅ Yes` / `❌ No`

| # | Field Name         | Data Type        | Required? | Default Value    | Constraints / Rules                          | Example Value              | Plain-English Description                                         | PII / PHI? | AI Used? | Encrypted? | Field Owner    | Last Updated |
|---|--------------------|------------------|-----------|------------------|----------------------------------------------|----------------------------|--------------------------------------------------------------------|------------|----------|------------|----------------|--------------|
| 1 | `id`               | UUID / ObjectId  | ✅ Yes    | Auto-generated   | PRIMARY KEY, UNIQUE, NOT NULL                | `a1b2-c3d4-e5f6-g7h8`     | The unique identifier for this record. Auto-created by the system. | ⬜ None    | ❌ No    | ❌ No      | [Team/Person]  | [Date]       |
| 2 | `created_at`       | TIMESTAMP        | ✅ Yes    | `NOW()`          | NOT NULL, auto-set on insert                 | `2026-10-14T09:00:00Z`    | The exact date and time this record was first created.             | ⬜ None    | ❌ No    | ❌ No      | [Team/Person]  | [Date]       |
| 3 | `updated_at`       | TIMESTAMP        | ✅ Yes    | `NOW()`          | NOT NULL, auto-updated on every change       | `2026-10-14T10:30:00Z`    | The last time any field in this record was changed.                | ⬜ None    | ❌ No    | ❌ No      | [Team/Person]  | [Date]       |
| 4 | `deleted_at`       | TIMESTAMP        | ❌ No     | `NULL`           | NULL = not deleted; set to soft-delete       | `NULL` or `2026-12-01`    | If set, this record is considered deleted but kept for audit.      | ⬜ None    | ❌ No    | ❌ No      | [Team/Person]  | [Date]       |
| 5 | `[field_name]`     | [Type]           | [?]       | [Default]        | [Rules]                                      | [Example]                  | [What does this field mean in plain English?]                      | [?]        | [?]      | [?]        | [Team/Person]  | [Date]       |

> **Supported Data Types:** `UUID` · `ObjectId` · `String (VARCHAR)` · `Text` · `Integer (INT)` · `BigInteger` · `Float` · `Decimal` · `Boolean` · `TIMESTAMP` · `DATE` · `JSON / JSONB` · `Array` · `Enum` · `Binary / BLOB`

---

## 📂 SQL Entities (PostgreSQL / MySQL)

---

### 🟦 Entity: `users`

> **Plain-English Description:** Stores every person who has registered an account in the application. One row = one user. This is the central entity — almost every other entity links back to `users` via a foreign key.

| Property               | Value                                                                          |
|------------------------|--------------------------------------------------------------------------------|
| **Entity Name**        | `users`                                                                        |
| **Database Type**      | SQL (PostgreSQL)                                                               |
| **Database Name**      | `app_db`                                                                       |
| **Table / Collection** | `users`                                                                        |
| **Environment**        | Development · Staging · Production                                             |
| **Estimated Row Count**| 500 rows at launch; ~10,000 at 500-customer milestone                         |
| **Lifecycle Stage**    | Planning → Development → Launch → Post-Launch                                 |
| **Primary Key**        | `id` (UUID v4)                                                                  |
| **Indexes**            | `email` (UNIQUE), `created_at` (B-tree), `deleted_at` (partial index)         |
| **Relationships**      | `users.id` → `sessions.user_id` (one-to-many) · `users.id` → `orders.user_id` |
| **Entity Owner**       | Backend Engineering Team                                                       |
| **Data Retention**     | Active accounts: indefinitely. Deleted accounts: anonymize after 90 days.     |
| **Soft Delete?**       | Yes — sets `deleted_at`; hard delete runs after 90-day anonymization window   |
| **Partitioning Key**   | N/A (SQL table)                                                                |

#### 📊 Field Definitions — `users`

| # | Field Name           | Data Type         | Required?        | Default Value    | Constraints / Rules                                     | Example Value                     | Plain-English Description                                                            | PII / PHI?  | AI Used? | Encrypted? | Field Owner   | Last Updated |
|---|----------------------|-------------------|------------------|------------------|---------------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------|-------------|----------|------------|---------------|--------------|
| 1 | `id`                 | UUID              | ✅ Yes           | Auto-generated   | PK, UNIQUE, NOT NULL                                    | `9c83-f21a-4e67-ba12-000c`       | The unique ID for this user. Auto-created when the account is made.                  | ⬜ None     | ❌ No    | ❌ No      | Auth Team     | 2026-10-14   |
| 2 | `email`              | VARCHAR(320)      | ✅ Yes           | —                | UNIQUE, NOT NULL, valid email format, lowercase stored  | `priya@example.com`              | The user's email address. Used to log in and receive notifications.                  | 🔴 PII      | ❌ No    | ✅ Yes     | Auth Team     | 2026-10-14   |
| 3 | `password_hash`      | VARCHAR(255)      | ✅ Yes           | —                | NOT NULL, bcrypt hash (cost factor ≥ 12), never plain   | `$2b$12$abc...xyz`               | The user's password stored as a secure hash. Never store or log plain-text passwords. | 🔴 PII     | ❌ No    | ✅ Yes     | Auth Team     | 2026-10-14   |
| 4 | `first_name`         | VARCHAR(100)      | ✅ Yes           | —                | NOT NULL, max 100 chars, trimmed                        | `Priya`                          | The user's given (first) name.                                                       | 🔴 PII      | ✅ Yes   | ❌ No      | Auth Team     | 2026-10-14   |
| 5 | `last_name`          | VARCHAR(100)      | ✅ Yes           | —                | NOT NULL, max 100 chars, trimmed                        | `Sharma`                         | The user's family (last) name.                                                       | 🔴 PII      | ✅ Yes   | ❌ No      | Auth Team     | 2026-10-14   |
| 6 | `phone_number`       | VARCHAR(20)       | ❌ No            | `NULL`           | E.164 format (+12345678900), nullable                   | `+14155551234`                   | The user's mobile phone number for 2FA and SMS notifications.                        | 🔴 PII      | ❌ No    | ✅ Yes     | Auth Team     | 2026-10-14   |
| 7 | `date_of_birth`      | DATE              | ⚠️ Conditional   | `NULL`           | Required for HIPAA-regulated flows; ISO 8601 format     | `1990-05-15`                     | The user's date of birth. Required only if the product offers health features.       | 🟣 PHI      | ❌ No    | ✅ Yes     | Auth Team     | 2026-10-14   |
| 8 | `role`               | ENUM              | ✅ Yes           | `'customer'`     | Values: `admin`, `customer`, `provider`, `analyst`      | `customer`                       | What permission level the user has in the app.                                       | ⬜ None     | ✅ Yes   | ❌ No      | Auth Team     | 2026-10-14   |
| 9 | `status`             | ENUM              | ✅ Yes           | `'pending'`      | Values: `pending`, `active`, `suspended`, `deleted`     | `active`                         | Whether the account can currently be used. Pending = email not verified yet.         | ⬜ None     | ❌ No    | ❌ No      | Auth Team     | 2026-10-14   |
| 10 | `email_verified_at` | TIMESTAMP         | ❌ No            | `NULL`           | Set when user clicks verification link; NULL = unverified| `2026-10-14T09:05:00Z`          | The date and time the user confirmed their email address is real.                    | ⬜ None     | ❌ No    | ❌ No      | Auth Team     | 2026-10-14   |
| 11 | `gdpr_consent_at`   | TIMESTAMP         | ✅ Yes           | —                | NOT NULL for EU users; must be set at registration      | `2026-10-14T09:00:00Z`           | When the user agreed to the privacy policy and data processing terms. (GDPR required) | 🔴 PII     | ❌ No    | ❌ No      | Legal/Auth    | 2026-10-14   |
| 12 | `gdpr_consent_version`| VARCHAR(10)     | ✅ Yes           | —                | Must match current policy version at time of consent    | `v3.2`                           | Which version of the privacy policy the user agreed to.                              | ⬜ None     | ❌ No    | ❌ No      | Legal/Auth    | 2026-10-14   |
| 13 | `avatar_url`         | TEXT              | ❌ No            | `NULL`           | Must be an HTTPS URL; max 2000 chars                    | `https://cdn.app.com/img/a1.png` | The web address of the user's profile picture.                                       | ❌ No       | ❌ No    | ❌ No      | Media Team    | 2026-10-14   |
| 14 | `timezone`           | VARCHAR(50)       | ❌ No            | `'UTC'`          | Must be a valid IANA timezone string                    | `America/New_York`               | The user's timezone, used to show dates/times in their local time.                   | ⬜ None     | ✅ Yes   | ❌ No      | Product Team  | 2026-10-14   |
| 15 | `created_at`         | TIMESTAMP         | ✅ Yes           | `NOW()`          | NOT NULL, auto-set                                      | `2026-10-14T09:00:00Z`           | The exact moment this user's account was created.                                    | ⬜ None     | ❌ No    | ❌ No      | Backend       | 2026-10-14   |
| 16 | `updated_at`         | TIMESTAMP         | ✅ Yes           | `NOW()`          | NOT NULL, auto-updated on change                        | `2026-10-14T10:30:00Z`           | The last time any field in this user record was changed.                             | ⬜ None     | ❌ No    | ❌ No      | Backend       | 2026-10-14   |
| 17 | `deleted_at`         | TIMESTAMP         | ❌ No            | `NULL`           | Set on soft delete; records with value are "deleted"    | `NULL`                           | If set, this account has been deactivated. The record is kept for legal/audit reasons.| ⬜ None    | ❌ No    | ❌ No      | Backend       | 2026-10-14   |

---

### 🟦 Entity: `sessions`

> **Plain-English Description:** Tracks every login session a user creates. Used to manage authentication tokens and detect suspicious activity. One row = one login.

| Property               | Value                                                                          |
|------------------------|--------------------------------------------------------------------------------|
| **Entity Name**        | `sessions`                                                                     |
| **Database Type**      | SQL (PostgreSQL)                                                               |
| **Primary Key**        | `id` (UUID v4)                                                                  |
| **Indexes**            | `user_id` (FK index), `token` (UNIQUE), `expires_at` (B-tree)                 |
| **Relationships**      | `sessions.user_id` → `users.id` (many-to-one)                                 |
| **Data Retention**     | Delete expired sessions after 30 days                                          |
| **Entity Owner**       | Auth / Security Team                                                           |

#### 📊 Field Definitions — `sessions`

| # | Field Name      | Data Type    | Required? | Default Value    | Constraints / Rules                        | Example Value                         | Plain-English Description                                                            | PII / PHI?  | AI Used? | Encrypted? | Field Owner  | Last Updated |
|---|-----------------|--------------|-----------|------------------|--------------------------------------------|---------------------------------------|---------------------------------------------------------------------------------------|-------------|----------|------------|--------------|--------------|
| 1 | `id`            | UUID         | ✅ Yes    | Auto-generated   | PK, UNIQUE, NOT NULL                       | `3e7c-a8b1-...`                      | The unique ID for this session.                                                       | ⬜ None     | ❌ No    | ❌ No      | Auth Team    | 2026-10-14   |
| 2 | `user_id`       | UUID         | ✅ Yes    | —                | FK → `users.id`, NOT NULL, cascade delete  | `9c83-f21a-...`                      | The ID of the user who created this session (who logged in).                          | 🔴 PII      | ❌ No    | ❌ No      | Auth Team    | 2026-10-14   |
| 3 | `token`         | VARCHAR(512) | ✅ Yes    | —                | UNIQUE, NOT NULL, hashed (SHA-256)         | `ab12cd34...` (hashed JWT)           | A secret token that proves the user is logged in. Like a temporary key card.         | 🔴 PII      | ❌ No    | ✅ Yes     | Auth Team    | 2026-10-14   |
| 4 | `device_type`   | ENUM         | ❌ No     | `'unknown'`      | Values: `web`, `ios`, `android`, `unknown` | `ios`                                | What kind of device the user was using when they logged in.                          | ⬜ None     | ❌ No    | ❌ No      | Auth Team    | 2026-10-14   |
| 5 | `ip_address`    | VARCHAR(45)  | ❌ No     | `NULL`           | IPv4 or IPv6 format                        | `192.168.1.1`                        | The internet address of the device that logged in. Used for security monitoring.      | 🔴 PII      | ❌ No    | ✅ Yes     | Auth Team    | 2026-10-14   |
| 6 | `user_agent`    | TEXT         | ❌ No     | `NULL`           | Max 1000 chars; browser/OS info            | `Mozilla/5.0 (iPhone; CPU iPhone OS 17...)` | Technical info about the browser or app used to log in.                   | ⬜ None     | ❌ No    | ❌ No      | Auth Team    | 2026-10-14   |
| 7 | `expires_at`    | TIMESTAMP    | ✅ Yes    | `NOW() + 30 days`| NOT NULL; must be in the future on create  | `2026-11-13T09:00:00Z`              | The date/time this session will automatically expire. After this, user must log in again.| ⬜ None   | ❌ No    | ❌ No      | Auth Team    | 2026-10-14   |
| 8 | `created_at`    | TIMESTAMP    | ✅ Yes    | `NOW()`          | NOT NULL, auto-set                         | `2026-10-14T09:00:00Z`              | The exact moment this session (login) was created.                                    | ⬜ None     | ❌ No    | ❌ No      | Auth Team    | 2026-10-14   |

---

### 🟦 Entity: `[add_your_entity_here]`

> ⬆️ Copy the Entity Template Block from the top of this section and paste here.

---

## 📂 NoSQL Entities (MongoDB / DynamoDB / Firestore)

> 💡 **Note for NoSQL:** NoSQL documents don't enforce a schema — fields can be missing or vary between records. The definitions below represent the EXPECTED structure. Add a `schema_version` field to every document so you can detect and handle old-format records.

---

### 🟩 Entity: `messages` (MongoDB Collection)

> **Plain-English Description:** Stores every message sent in AI chat conversations. One document = one message (either from a user or from the AI). Organized into "conversations" using the `conversation_id` field.

| Property               | Value                                                                          |
|------------------------|--------------------------------------------------------------------------------|
| **Entity Name**        | `messages`                                                                     |
| **Database Type**      | NoSQL (MongoDB)                                                                |
| **Database Name**      | `app_db`                                                                       |
| **Collection**         | `messages`                                                                     |
| **Partitioning Key**   | `conversation_id` (shard key for horizontal scaling)                          |
| **Indexes**            | `conversation_id` (ascending), `user_id` (ascending), `created_at` (descending)|
| **Relationships**      | `messages.user_id` → `users.id` (reference); `messages.conversation_id` → `conversations._id`|
| **Data Retention**     | 3 years; archived to cold storage after 1 year                                |
| **Entity Owner**       | AI Engineering Team                                                            |

#### 📊 Field Definitions — `messages`

| # | Field Name          | Data Type      | Required?       | Default Value    | Constraints / Rules                                          | Example Value                     | Plain-English Description                                                               | PII / PHI?  | AI Used? | Encrypted? | Field Owner   | Last Updated |
|---|---------------------|----------------|-----------------|------------------|--------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------------------------------|-------------|----------|------------|---------------|--------------|
| 1 | `_id`               | ObjectId       | ✅ Yes          | Auto-generated   | MongoDB primary key; auto-created                            | `507f1f77bcf86cd799439011`       | The unique ID MongoDB auto-creates for each message document.                            | ⬜ None     | ❌ No    | ❌ No      | AI Team       | 2026-10-14   |
| 2 | `conversation_id`   | ObjectId       | ✅ Yes          | —                | NOT NULL; must reference a valid `conversations._id`         | `507f1f77bcf86cd799439000`       | Which conversation thread this message belongs to.                                       | ⬜ None     | ✅ Yes   | ❌ No      | AI Team       | 2026-10-14   |
| 3 | `user_id`           | UUID           | ✅ Yes          | —                | NOT NULL; references `users.id` in PostgreSQL                | `9c83-f21a-4e67-ba12-000c`       | The ID of the user who sent or received this message.                                    | 🔴 PII      | ✅ Yes   | ❌ No      | AI Team       | 2026-10-14   |
| 4 | `role`              | String (Enum)  | ✅ Yes          | —                | Values: `user`, `assistant`, `system`, `tool`                | `user`                           | Who sent this message. `user` = human, `assistant` = AI, `system` = background instruction.| ⬜ None  | ✅ Yes   | ❌ No      | AI Team       | 2026-10-14   |
| 5 | `content`           | String         | ✅ Yes          | —                | Max 32,000 chars; trimmed; never empty                       | `"What is my appointment date?"` | The actual text of the message — what was said.                                          | ⚠️ Maybe PII| ✅ Yes   | ✅ Yes     | AI Team       | 2026-10-14   |
| 6 | `token_count`       | Integer        | ✅ Yes          | —                | NOT NULL; computed before storage; min 1                     | `47`                             | How many AI tokens this message used. Used to track AI API costs.                        | ⬜ None     | ✅ Yes   | ❌ No      | AI Team       | 2026-10-14   |
| 7 | `model_used`        | String         | ⚠️ Conditional  | `NULL`           | Required when `role = 'assistant'`; format: `provider/model`| `anthropic/claude-3-5-sonnet`   | Which AI model generated this response. Blank for user messages.                         | ⬜ None     | ✅ Yes   | ❌ No      | AI Team       | 2026-10-14   |
| 8 | `latency_ms`        | Integer        | ⚠️ Conditional  | `NULL`           | Required when `role = 'assistant'`; milliseconds             | `842`                            | How long the AI took to generate this response (in milliseconds).                        | ⬜ None     | ❌ No    | ❌ No      | AI Team       | 2026-10-14   |
| 9 | `metadata`          | Object (BSON)  | ❌ No           | `{}`             | Free-form JSON; must be a valid object                       | `{"source": "web", "version": 2}`| Extra context attached to the message — flexible and can vary per use case.              | ⬜ None     | ❌ No    | ❌ No      | AI Team       | 2026-10-14   |
| 10| `schema_version`    | Integer        | ✅ Yes          | `1`              | NOT NULL; increment when document shape changes              | `1`                              | Tracks which version of this document structure was used. Helps handle old records safely.| ⬜ None   | ❌ No    | ❌ No      | AI Team       | 2026-10-14   |
| 11| `created_at`        | ISODate        | ✅ Yes          | `new Date()`     | NOT NULL; auto-set at insert                                 | `2026-10-14T09:05:00.000Z`      | The exact moment this message was sent.                                                  | ⬜ None     | ❌ No    | ❌ No      | AI Team       | 2026-10-14   |

---

### 🟩 Entity: `[add_your_nosql_entity]` (MongoDB / DynamoDB)

> ⬆️ Copy the Entity Template Block and paste here.

---

&nbsp;

---

# 🤖 AI & Machine Learning Data

> 📌 **How to fill:** This section defines the data structures that are specific to your AI features. If your product uses an AI model (ChatGPT, Claude, a custom model, etc.), fill in each sub-section below.

---

## 🔵 AI Model Inputs & Outputs

> **What this is:** Every time your product calls an AI model, you send it data (the INPUT) and it sends data back (the OUTPUT). Define what that data looks like here.

| # | Name                 | Direction | Data Type    | Max Size       | Required? | Description                                                                          | PII Risk?         | Notes                                               |
|---|----------------------|-----------|--------------|----------------|-----------|--------------------------------------------------------------------------------------|-------------------|-----------------------------------------------------|
| 1 | `system_prompt`      | → Input   | String       | 4,096 tokens   | ✅ Yes    | The background instruction that tells the AI how to behave (e.g., "You are a helpful medical assistant...") | ⚠️ Review carefully | Never include user PII in system prompt             |
| 2 | `user_message`       | → Input   | String       | 8,000 tokens   | ✅ Yes    | The message the human typed into the chat                                            | ⚠️ May contain PII | Log with user consent only                          |
| 3 | `conversation_history`| → Input  | Array of Objects| 64,000 tokens total | ⚠️ Conditional | Previous messages in the conversation, included to give the AI memory | ⚠️ May contain PII | Truncate oldest messages first when near token limit|
| 4 | `retrieved_context`  | → Input   | String       | 16,000 tokens  | ❌ No     | Relevant documents retrieved from a vector database (RAG pattern) to help the AI answer | ⚠️ Review content | Content from knowledge base — verify licensing      |
| 5 | `ai_completion`      | ← Output  | String       | 4,096 tokens   | ✅ Yes    | The AI's response/answer to the user's message                                       | ⚠️ May reflect PII | Must be reviewed for hallucination in regulated domains|
| 6 | `tool_calls`         | ← Output  | Array (JSON) | Varies         | ❌ No     | Structured JSON commands the AI wants to execute (e.g., "search_database", "send_email") | ⚠️ Review params | Validate ALL tool call parameters before executing  |
| 7 | `finish_reason`      | ← Output  | String (Enum)| —              | ✅ Yes    | Why the AI stopped generating. Values: `stop`, `max_tokens`, `tool_use`, `error`    | ⬜ None            | Log for debugging and cost analysis                 |
| 8 | `usage_tokens`       | ← Output  | Object (JSON)| —              | ✅ Yes    | Token counts: `{"input": 1200, "output": 300, "total": 1500}`. Used for billing.   | ⬜ None            | Store for cost dashboards at 500-customer milestone |
| [#]| `[field_name]`      | [→/←]     | [Type]       | [Limit]        | [?]       | [Description]                                                                        | [Risk]             | [Notes]                                             |

---

## 🧠 AI Agent State & Memory

> **What this is:** If your AI agent needs to "remember" things between conversations (like a user's name, preferences, or what they were working on), that memory is stored in your database. Define those memory fields here.

> 💡 **Analogy:** This is like the AI's notebook — everything it writes down so it doesn't forget.

| Property               | Value                                                                          |
|------------------------|--------------------------------------------------------------------------------|
| **Memory Entity Name** | `agent_memory` / `user_profiles`                                               |
| **Database Type**      | SQL (PostgreSQL) / NoSQL (MongoDB) / Redis (for short-term cache)              |
| **Scope**              | `per_user` / `per_conversation` / `global` / `per_tenant`                     |
| **Max Memory Size**    | [e.g., 50,000 tokens per user or 10MB per user]                                |
| **TTL (Time to Live)** | [e.g., Short-term: 24 hours in Redis; Long-term: indefinite in PostgreSQL]     |
| **Eviction Policy**    | [e.g., LRU (Least Recently Used) — oldest facts removed when limit reached]    |
| **User Control**       | [Can users view/delete their agent memory? Yes/No + how]                       |

#### 📊 Memory Field Definitions

| # | Memory Key              | Type     | Scope           | Example Value                        | Description                                                             | PII? | Retention    |
|---|-------------------------|----------|-----------------|--------------------------------------|-------------------------------------------------------------------------|------|--------------|
| 1 | `preferred_name`        | String   | Per User        | `"Priya"`                           | What the user prefers to be called. AI uses this to personalize responses| 🔴 PII | Until user deletes |
| 2 | `last_topic_discussed`  | String   | Per Conversation| `"appointment scheduling"`          | The main topic of the most recent conversation. Used for continuity.    | ⚠️   | 7 days      |
| 3 | `user_goals`            | Array    | Per User        | `["lose weight", "track sleep"]`    | Goals the user has shared with the AI over time.                        | ⚠️   | Indefinite  |
| 4 | `interaction_count`     | Integer  | Per User        | `42`                                 | Total number of messages the user has sent. Used for analytics.         | ⬜ None| Indefinite |
| 5 | `last_active_at`        | Timestamp| Per User        | `2026-10-14T09:00:00Z`              | When the user last interacted with the AI agent.                        | ⬜ None| Indefinite |
| 6 | `fact_store`            | JSON     | Per User        | `{"city": "NYC", "age": 34}`        | Arbitrary facts the AI has learned about the user during conversations. | 🔴 PII | Until user deletes |
| [#]| `[key]`                | [Type]   | [Scope]         | [Example]                            | [Description]                                                           | [?]  | [Retention]  |

---

## ⚙️ Feature Engineering & Data Pipelines

> **What this is:** If you process raw data to create AI-ready features (e.g., calculating a "user engagement score" from event logs), define those derived fields here.

| # | Feature Name           | Input Fields                      | Computation / Logic                                     | Output Type | Update Frequency | Used By                      | Notes                                       |
|---|------------------------|-----------------------------------|---------------------------------------------------------|-------------|------------------|------------------------------|---------------------------------------------|
| 1 | `user_engagement_score`| `events.user_id`, `events.type`, `events.created_at` | Count events in last 30 days, weighted by type       | Float (0–1) | Daily (2am UTC)  | Recommendation model, PM dashboard | Normalized 0–1; 1 = highly engaged        |
| 2 | `session_duration_avg` | `sessions.created_at`, `sessions.last_active_at` | Mean of (last_active - created) per user over 30 days  | Integer (seconds) | Daily     | Churn prediction model       | Excludes sessions > 8 hours (outliers)      |
| 3 | `message_sentiment`    | `messages.content`               | Run through sentiment model (positive/neutral/negative) | Enum        | On message create| Escalation alerts            | Uses internal sentiment classifier v2.1     |
| 4 | `predicted_churn_risk` | Multiple features above           | ML model (XGBoost) output: 0=low risk, 1=high risk     | Float (0–1) | Weekly           | CS Team dashboard, AI agent  | Retrain monthly; bias review required       |
| [#]| `[feature]`           | [Input fields]                    | [How it is computed]                                    | [Type]      | [How often]      | [Who consumes this]          | [Edge cases, bias, limitations]             |

---

&nbsp;

---

# 🔒 Compliance & Data Governance

> 📌 **How to fill:** This section tracks every field that contains personal or sensitive data. It is REQUIRED for GDPR, CCPA, HIPAA, and SOC 2 compliance audits. If you are unsure whether a field is PII, mark it as PII to be safe.

---

## 🔴 PII & PHI Master List

> **PII** = Personally Identifiable Information (e.g., name, email, phone, IP address)
> **PHI** = Protected Health Information under HIPAA (e.g., diagnoses, medication, appointment reason)

| # | Entity        | Field Name            | Classification | Regulation        | Collected At | Storage Location       | Encrypted? | Can User Delete? | Retention Period    | Responsible Team |
|---|---------------|-----------------------|----------------|-------------------|----|------------------------|------------|------------------|---------------------|------------------|
| 1 | `users`       | `email`               | 🔴 PII         | GDPR, CCPA        | Registration | PostgreSQL (app_db)    | ✅ Yes     | ✅ Yes (anonymize)| Until deletion + 90d | Auth Team |
| 2 | `users`       | `first_name`          | 🔴 PII         | GDPR, CCPA        | Registration | PostgreSQL (app_db)    | ❌ No      | ✅ Yes (anonymize)| Until deletion + 90d | Auth Team |
| 3 | `users`       | `last_name`           | 🔴 PII         | GDPR, CCPA        | Registration | PostgreSQL (app_db)    | ❌ No      | ✅ Yes (anonymize)| Until deletion + 90d | Auth Team |
| 4 | `users`       | `phone_number`        | 🔴 PII         | GDPR, CCPA        | Profile setup | PostgreSQL (app_db)   | ✅ Yes     | ✅ Yes (nullify)  | Until deletion + 90d | Auth Team |
| 5 | `users`       | `date_of_birth`       | 🟣 PHI + 🔴 PII| GDPR, CCPA, HIPAA | Health flow  | PostgreSQL (app_db)    | ✅ Yes     | ✅ Yes (nullify)  | Until deletion + 90d | Auth Team |
| 6 | `sessions`    | `ip_address`          | 🔴 PII         | GDPR              | Login        | PostgreSQL (app_db)    | ✅ Yes     | ✅ Yes (nullify)  | 90 days              | Auth Team |
| 7 | `messages`    | `content`             | ⚠️ Potential PII| GDPR, CCPA, HIPAA| Chat         | MongoDB (messages)     | ✅ Yes     | ✅ Yes (anonymize)| 3 years              | AI Team   |
| [#]| [Entity]    | [Field]               | [🔴/🟣/⚠️]   | [Regulation]      | [When]       | [Where stored]         | [?]        | [?]              | [How long]          | [Team]    |

---

## 🟢 GDPR & CCPA Compliance Checklist

> Tick each item off as you implement it.

| # | Requirement                                         | Status     | Implementation Notes                                                | Owner       | Target Date |
|---|-----------------------------------------------------|------------|---------------------------------------------------------------------|-------------|-------------|
| 1 | **Lawful Basis for Processing** documented          | ⬜ Pending | Document the legal basis for each type of data processing           | Legal       | [Date]      |
| 2 | **Privacy Policy** written and published            | ⬜ Pending | Must be plain English, linked from signup and app footer            | Legal       | [Date]      |
| 3 | **Consent Collected** at registration               | ⬜ Pending | `users.gdpr_consent_at` + `gdpr_consent_version` fields populated  | Auth Team   | [Date]      |
| 4 | **Right to Access** — user can download their data  | ⬜ Pending | Build data export feature; response within 30 days                  | Engineering | [Date]      |
| 5 | **Right to Erasure** — user can delete their account| ⬜ Pending | Soft delete + 90-day anonymization pipeline (see DF-004)            | Engineering | [Date]      |
| 6 | **Right to Correction** — user can edit their data  | ⬜ Pending | Profile edit page covers core PII fields                            | Product     | [Date]      |
| 7 | **Data Minimization** — only collect what's needed  | ⬜ Pending | Review all fields; remove any that aren't actively used             | Arch. Review| [Date]      |
| 8 | **Third-Party Processors** listed in DPA            | ⬜ Pending | Document all services that receive user data (e.g., AI APIs, analytics) | Legal  | [Date]      |
| 9 | **Cross-Border Transfers** SCCs / adequacy decision | ⬜ Pending | Required if sending EU user data to non-EU AI providers             | Legal       | [Date]      |
| 10| **Breach Notification** process documented          | ⬜ Pending | Must notify regulators within 72 hours; users within reasonable time| Security    | [Date]      |

---

## 🟣 HIPAA Compliance Checklist

> Complete only if your product processes health information (PHI).

| # | Requirement                                         | Status     | Implementation Notes                                                | Owner       | Target Date |
|---|-----------------------------------------------------|------------|---------------------------------------------------------------------|-------------|-------------|
| 1 | **PHI Fields Identified** in PII Master List above  | ⬜ Pending | All 🟣 PHI rows in the PII table above are your scope              | Compliance  | [Date]      |
| 2 | **Encryption at Rest** for all PHI fields           | ⬜ Pending | AES-256; verify at DB and backup level                              | DevOps      | [Date]      |
| 3 | **Encryption in Transit** (TLS 1.2+) for all PHI   | ⬜ Pending | HTTPS only; verify mobile app uses certificate pinning              | DevOps      | [Date]      |
| 4 | **Access Controls** — minimum necessary access      | ⬜ Pending | Role-based access; no dev/analyst access to prod PHI                | Security    | [Date]      |
| 5 | **Audit Logs** for all PHI access                   | ⬜ Pending | Log WHO accessed WHICH PHI record, WHEN, and WHY                    | Engineering | [Date]      |
| 6 | **Business Associate Agreements (BAA)** signed      | ⬜ Pending | Required with any 3rd party receiving PHI (AI providers, analytics) | Legal       | [Date]      |
| 7 | **Breach Notification** — notify HHS & users        | ⬜ Pending | Within 60 days of discovery for breaches ≥ 500 individuals         | Legal       | [Date]      |
| 8 | **Workforce Training** completed                    | ⬜ Pending | All staff with PHI access trained annually                          | HR/Legal    | [Date]      |

---

## 🔵 SOC 2 & ISO 27001 Key Controls

| # | Control Area          | Control Description                                           | Status     | Evidence / Notes                                      | Owner    | Review Date |
|---|-----------------------|---------------------------------------------------------------|------------|-------------------------------------------------------|----------|-------------|
| 1 | **Access Control**    | MFA required for all production system access                 | ⬜ Pending | Enforce in SSO/IdP settings                           | DevOps   | [Date]      |
| 2 | **Encryption**        | All data encrypted at rest (AES-256) and in transit (TLS 1.3)| ⬜ Pending | DB encryption + HTTPS certificate audit               | DevOps   | [Date]      |
| 3 | **Audit Logging**     | All CRUD operations on sensitive data logged with user context| ⬜ Pending | Use structured logs → SIEM; retain 12 months minimum  | Security | [Date]      |
| 4 | **Incident Response** | Documented IR plan; tabletop exercise completed               | ⬜ Pending | Link IR plan: [URL]                                   | Security | [Date]      |
| 5 | **Vendor Risk**       | All third-party vendors assessed for security posture         | ⬜ Pending | Vendor register maintained in [tool/location]         | Security | [Date]      |
| 6 | **Change Management** | All production changes require PR review + change ticket      | ⬜ Pending | Git branch protection + deployment approval gates     | DevOps   | [Date]      |
| 7 | **Availability**      | SLA defined and uptime monitoring in place                    | ⬜ Pending | Target: 99.9% uptime; PagerDuty configured            | DevOps   | [Date]      |

---

&nbsp;

---

# 📅 Lifecycle Stages

> 📌 **How to use this section:** As your product progresses through development, fill in each stage. Use the checkboxes and tables to track what data exists, where it lives, and any issues found. You do NOT need to fill all stages before you start — fill each one as you enter that phase.

---

## 🌱 Phase 1: Planning & Discovery

> **When:** Before any code is written. During requirements gathering, PRD writing, and architecture design.
> **Goal:** Identify WHAT data the product will need, even if the schema is not finalized.

| Item                         | Details                                                                                   |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Product Goal**             | [e.g., Help patients book doctor appointments using AI chat]                              |
| **Core Entities Identified** | [e.g., `users`, `appointments`, `providers`, `messages`, `agent_memory`]                 |
| **Data Sensitivity Level**   | `Low` / `Medium` / `High` / `Critical` — [justify your choice]                          |
| **Compliance Scope**         | [e.g., HIPAA applies because we process appointment + health data]                        |
| **Data Volume Estimate**     | [e.g., 1,000 users at launch; 50,000 records in year 1]                                  |
| **External Data Sources**    | [e.g., EHR system API, Insurance verification API, Address validation API]                |
| **Open Questions**           | [e.g., "Where do we store conversation history — SQL or NoSQL?", "Do we need a CDN for avatars?"] |

### Proposed Entity List (Planning Phase)

| Entity Name         | Type    | Purpose                                          | Priority     | Status        |
|---------------------|---------|--------------------------------------------------|--------------|---------------|
| `users`             | SQL     | Store all registered accounts                    | 🔴 Must-Have | ⬜ Proposed   |
| `messages`          | NoSQL   | AI conversation history                          | 🔴 Must-Have | ⬜ Proposed   |
| `appointments`      | SQL     | Appointment bookings                             | 🔴 Must-Have | ⬜ Proposed   |
| `providers`         | SQL     | Healthcare provider profiles                     | 🟡 Should-Have| ⬜ Proposed  |
| `agent_memory`      | NoSQL   | AI agent user fact store                         | 🟡 Should-Have| ⬜ Proposed  |
| `events`            | NoSQL   | User analytics events                            | 🟢 Nice-to-Have| ⬜ Proposed |
| `[entity_name]`     | [Type]  | [Purpose]                                        | [Priority]   | ⬜ Proposed   |

---

## 🔨 Phase 2: Development & Testing

> **When:** While the product is being built. Dev and staging environments are active.
> **Goal:** Lock down schemas for dev/staging, run migrations, and catch data issues before production.

| Item                          | Details                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------|
| **Dev DB Connection String**  | `[Store in .env only — NEVER write credentials in this document]`                         |
| **Staging DB Connection String**| `[Store in .env only — NEVER write credentials in this document]`                       |
| **Migration Tool**            | [e.g., Alembic (Python), Flyway (Java), Knex (Node.js), Prisma (TypeScript)]             |
| **Seed / Test Data Available?**| Yes / No — [link to seed file or data generator]                                         |
| **Test Data Anonymization**   | [Are real user emails/names used in dev? They should NOT be — use fake/anonymized data]  |
| **Schema Review Completed?**  | ⬜ Pending / ✅ Done — [link to review PR or notes]                                       |
| **Data Dictionary Reviewed?** | ⬜ Pending / ✅ Done — [names of reviewers]                                               |

### Environment Schema Status

| Entity          | Dev Schema Status | Staging Schema Status | Notes                                          |
|-----------------|-------------------|-----------------------|------------------------------------------------|
| `users`         | ✅ Created        | ✅ Created            | Migration v3 applied                           |
| `messages`      | ✅ Created        | ⬜ Pending            | Waiting on MongoDB Atlas staging cluster setup |
| `sessions`      | ✅ Created        | ✅ Created            | —                                              |
| `[entity_name]` | [Status]          | [Status]              | [Notes]                                        |

### Known Data Issues (Dev/Staging)

| Issue ID | Entity        | Field           | Issue Description                                    | Severity | Status     | Assigned To | Fixed In    |
|----------|---------------|-----------------|------------------------------------------------------|----------|------------|-------------|-------------|
| D-001    | `users`       | `phone_number`  | E.164 validation not enforced in dev — accepts `123` | 🟡 Medium | 🔧 In Progress | [Name]   | v1.1 (est.) |
| D-002    | `messages`    | `token_count`   | Count is 0 for all messages in staging               | 🔴 High  | ⬜ Open    | [Name]      | —           |
| [D-XXX]  | [Entity]      | [Field]         | [Description]                                        | [Level]  | [Status]   | [Name]      | [Version]   |

---

## 🚀 Phase 3: Launch & Production

> **When:** Product is live. Real users are signing up and using the product.
> **Goal:** Ensure data integrity, performance, and compliance in production.

| Item                           | Details                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| **Production DB Provider**     | [e.g., AWS RDS (PostgreSQL 16), MongoDB Atlas M30, DynamoDB on-demand]                   |
| **Backup Frequency**           | [e.g., Full backup daily at 3am UTC; point-in-time recovery enabled with 7-day window]   |
| **Backup Tested?**             | ⬜ Not yet / ✅ Restored and verified on [Date]                                            |
| **Monitoring Tool**            | [e.g., Datadog, AWS CloudWatch, Grafana + Prometheus]                                     |
| **Alerting Thresholds**        | [e.g., Alert if DB CPU > 80%, query latency > 500ms, error rate > 1%]                    |
| **Read Replicas?**             | Yes — [count and regions] / No                                                            |
| **Data Encryption at Rest**    | ✅ Verified / ⬜ Pending — [Key management tool: e.g., AWS KMS, HashiCorp Vault]          |
| **Production Data Access**     | [List who has direct prod DB access — should be minimal: e.g., "2 senior engineers + DBA"]|
| **Runbook Location**           | [Link to database runbook — what to do if the DB goes down]                              |

### Production Entity Checklist

| Entity         | Created in Prod? | Indexes Applied? | Encryption Verified? | Backup Tested? | Monitoring Live? |
|----------------|-----------------|------------------|----------------------|----------------|------------------|
| `users`        | ✅ Yes          | ✅ Yes           | ✅ Yes               | ✅ Yes         | ✅ Yes           |
| `sessions`     | ✅ Yes          | ✅ Yes           | ✅ Yes               | ✅ Yes         | ✅ Yes           |
| `messages`     | ✅ Yes          | ⬜ Pending       | ✅ Yes               | ⬜ Pending     | ✅ Yes           |
| `[entity]`     | [?]             | [?]              | [?]                  | [?]            | [?]              |

---

## 📈 Phase 4: Post-Launch & Growth (First 500 Customers)

> **When:** Product is live and growing. First real customers are onboarded.
> **Goal:** Monitor data health, validate AI model performance, identify scaling bottlenecks, and prepare for growth past 500 customers.

| Milestone                    | Target Date | Status     | Notes                                          |
|------------------------------|-------------|------------|------------------------------------------------|
| First 10 customers onboarded | [Date]      | ⬜ Pending | Manually monitor all data flows                |
| First 100 customers          | [Date]      | ⬜ Pending | Check DB query performance; add indexes if slow|
| First 500 customers          | [Date]      | ⬜ Pending | Full compliance audit; scale review            |

### Data Health KPIs at 500 Customers

> Track these metrics weekly in your analytics dashboard.

| Metric                              | Definition                                                   | Target           | Current Value | Alert Threshold |
|-------------------------------------|--------------------------------------------------------------|------------------|---------------|-----------------|
| **DB Query P95 Latency**            | 95th percentile query response time                          | < 100ms          | [measure]     | > 500ms         |
| **AI Token Cost per User / Month**  | Total tokens used ÷ active users                             | < $2.00/user/mo  | [measure]     | > $5.00         |
| **Data Error Rate**                 | % of writes that fail validation or throw errors             | < 0.1%           | [measure]     | > 1%            |
| **AI Response Latency (P95)**       | Time from user message to AI reply displayed                 | < 2,000ms        | [measure]     | > 5,000ms       |
| **Null Field Rate (Required fields)**| % of required fields that are unexpectedly null in prod     | 0%               | [measure]     | > 0.01%         |
| **Agent Memory Hit Rate**           | % of AI calls where user memory was successfully retrieved   | > 95%            | [measure]     | < 80%           |
| **GDPR Deletion SLA Met**           | % of deletion requests completed within 30-day legal window  | 100%             | [measure]     | < 100%          |
| **Backup Recovery Time (RTO)**      | Time to restore DB from backup in a disaster scenario        | < 4 hours        | [test result] | > 8 hours       |

### Scaling Issues Discovered at This Stage

| Issue ID | Area           | Description                                                      | Impact    | Resolution Plan      | Status     |
|----------|----------------|------------------------------------------------------------------|-----------|----------------------|------------|
| S-001    | [DB/AI/Pipeline]| [What slowed down or broke at scale?]                           | [High/Med/Low]| [How will you fix it?] | [Status]  |

---

&nbsp;

---

# ✅ Review & Sign-Off

> 📌 **How to fill:** Before this document is marked `Active` and before any schema goes to production, get the required sign-offs. Each approver confirms they've reviewed their relevant sections.

| Role                     | Name                | Sections Reviewed                             | Signature / Approval Date | Status      |
|--------------------------|---------------------|-----------------------------------------------|---------------------------|-------------|
| Technical Lead / Architect | [Name]            | All Entities, Data Flow, AI/ML Section        | [Date or "Approved via PR #XX"] | ⬜ Pending |
| Product Manager            | [Name]            | Document Header, Lifecycle Stages, Glossary   | [Date or "Approved in Notion"] | ⬜ Pending |
| Data / AI Engineer         | [Name]            | AI/ML Section, Feature Engineering, KPIs     | [Date]                    | ⬜ Pending |
| Legal / Compliance Officer | [Name]            | Compliance Section (GDPR, HIPAA, SOC 2)      | [Date]                    | ⬜ Pending |
| QA Lead                    | [Name]            | Data Issues Log, Dev/Staging Schema Status   | [Date]                    | ⬜ Pending |
| Security Team              | [Name]            | Compliance Controls, PII Master List         | [Date]                    | ⬜ Pending |
| Executive Sponsor          | [Name]            | Full document (high-level review)            | [Date]                    | ⬜ Pending |

---

> 🔏 **Once all sign-offs are received, change Document Status (in the header) from `Under Review` to `Active`.**

---

&nbsp;

---

# 📎 Appendix

## A. Field Type Reference Card

| Type Name        | What It Stores                                  | Example Value                   | When to Use It                                     |
|------------------|-------------------------------------------------|---------------------------------|----------------------------------------------------|
| `UUID`           | A unique ID (32 hex chars + dashes)             | `9c83-f21a-4e67-ba12-000c`     | Primary keys in SQL; user IDs, order IDs           |
| `VARCHAR(n)`     | Short text, max n characters                    | `"Priya Sharma"`               | Names, emails, short labels — when max length known|
| `TEXT`           | Long text, no practical limit                   | `"Dear Priya, your appointment..."` | Message bodies, long descriptions              |
| `INTEGER`        | Whole numbers (–2 billion to +2 billion)        | `42`, `500`, `-1`              | Counts, ages, quantities, scores                   |
| `BIGINT`         | Very large whole numbers                        | `1728000000000`                | Unix timestamps, very large IDs                    |
| `DECIMAL(p,s)`   | Exact decimal numbers (precision, scale)        | `99.99`, `0.005`               | Money amounts — never use FLOAT for money!         |
| `FLOAT / DOUBLE` | Approximate decimal numbers                     | `3.14159`, `0.9843`            | AI scores, probabilities — not for money           |
| `BOOLEAN`        | True or False only                              | `true`, `false`                | Flags: is_active, email_verified, is_admin         |
| `DATE`           | A calendar date (no time)                       | `2026-10-14`                   | Birthdays, appointment dates, expiry dates         |
| `TIMESTAMP`      | An exact point in time (date + time + timezone) | `2026-10-14T09:00:00Z`        | Created/updated timestamps; always store in UTC    |
| `ENUM`           | One value from a fixed list                     | `"active"`, `"pending"`        | Status fields, role fields, category fields        |
| `JSON / JSONB`   | A nested object with key-value pairs            | `{"key": "value", "n": 1}`    | Flexible metadata; avoid for frequently queried data|
| `ARRAY`          | A list of values of the same type               | `["tag1", "tag2", "tag3"]`    | Tags, permissions lists, small sets                |
| `ObjectId`       | MongoDB's built-in unique ID (12 bytes)         | `507f1f77bcf86cd799439011`    | Primary keys in MongoDB collections                |
| `Binary / BLOB`  | Raw binary data (files, images)                 | `<binary data>`                | Store file REFERENCES (URLs), not files themselves |

---

## B. Naming Conventions

> Follow these rules consistently. Inconsistent naming is the #1 cause of bugs and confusion.

| Rule                               | ✅ Correct                         | ❌ Incorrect                       |
|------------------------------------|------------------------------------|------------------------------------|
| Table/Collection names             | `snake_case`, plural              | `users`, `order_items`            | `User`, `OrderItem`, `orderitems`  |
| Field/Column names                 | `snake_case`, descriptive         | `first_name`, `created_at`        | `firstName`, `name1`, `f`          |
| Primary key                        | `id`                              | `id`                              | `userId`, `_ID`, `pkUser`          |
| Foreign key                        | `{referenced_table}_id`           | `user_id`, `order_id`             | `userId`, `userFK`, `refUser`      |
| Boolean fields                     | Prefix with `is_`, `has_`, `can_` | `is_active`, `has_paid`           | `active`, `paid`, `enabled`        |
| Timestamp fields                   | Suffix with `_at`                 | `created_at`, `deleted_at`        | `created`, `timestamp`, `date`     |
| Enum values                        | `lowercase_with_underscores`      | `in_progress`, `email_verified`   | `InProgress`, `EMAIL_VERIFIED`     |
| AI-specific fields                 | Prefix with `ai_` or suffix `_embedding` | `ai_summary`, `text_embedding` | `embedding1`, `result`         |

---

## C. Related Documents

| Document Name              | Location / Link                              | Description                                          |
|----------------------------|----------------------------------------------|------------------------------------------------------|
| Product Requirements Doc   | [Link]                                       | What the product does and why                        |
| System Architecture Doc    | [Link]                                       | How the system is structured technically             |
| API Documentation          | [Link]                                       | All API endpoints and their request/response schemas |
| AI Model Card              | [Link]                                       | AI model behavior, limitations, and bias notes       |
| Runbook / Incident Playbook| [Link]                                       | What to do when things break                         |
| Data Flow Diagrams         | [Link]                                       | Visual diagrams of how data moves (if using ext tool)|
| Privacy Policy             | [Link]                                       | Public-facing data use policy                        |
| Security Whitepaper        | [Link]                                       | How user data is secured                             |

---

## D. Quick-Reference: Who Fills What

| Your Role                  | Sections You Own                                                                           |
|----------------------------|--------------------------------------------------------------------------------------------|
| **Developer / Engineer**   | Entity Field Definitions, Data Flow Map, Dev/Staging Status, Naming Conventions           |
| **Product Manager**        | Document Header, Glossary, Lifecycle Phases, KPIs, Sign-Off                               |
| **Data / AI Engineer**     | AI Model Inputs & Outputs, Agent Memory, Feature Engineering, Scaling KPIs                |
| **QA Engineer**            | Data Issues Log (Phase 2), Production Entity Checklist (Phase 3)                          |
| **Legal / Compliance**     | GDPR Checklist, HIPAA Checklist, SOC 2 Controls, PII Master List                         |
| **DevOps / SRE**           | Phase 3 Production items (backups, encryption, monitoring, access controls)               |
| **Anyone**                 | Glossary (add any confusing term), Changelog (add a row when you change anything)         |

---

*— End of Data Dictionary Template —*

*Template authored for AI-Driven Development Life Cycle (AIDLC) | Version 1.0.0 | 2026-10-14*
*Designed to be shared across 100s of projects. Modify the entities — keep the structure.*
