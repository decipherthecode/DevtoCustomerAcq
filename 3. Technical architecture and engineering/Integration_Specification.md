# 📘 Integration Specification Template
**File:** `Integration_Specification.md`
**Version:** 1.0
**Designed for:** AI-Driven Development Lifecycle · SaaS & Mobile Products · Solo Founders to Small Teams

---

# 🧭 HOW TO FILL THIS DOCUMENT
> **Read this section first — before you touch anything else.**

## What is this document?
This is your **Integration Specification** — a single source of truth that describes every external service, API, database, and AI system your product connects to. Think of it as the "wiring diagram" of your app. Without it, bugs are mysterious, teammates get confused, and handoffs break.

## Who should fill it?
Anyone building the product — developer, founder, freelancer, or even a non-technical PM. Every section has instructions and examples written in plain English.

## When should you fill it?
- **Start:** Fill out Sections 1–3 before writing a single line of code.
- **Continue:** Fill each Integration Card (Sections 4–7) as you add each new integration.
- **Update:** Every time an API key changes, a new endpoint is added, or a pricing tier changes.
- **Review:** Before each major milestone (Alpha, Beta, General Availability, 500 Customers).

## How to use the instructions?
Every field looks like this:

```
**Field Name**
💡 *Instruction: Explains what to put here, with an example.*
Your answer goes here.
```

Replace the placeholder text `[like this]` with your real information. Delete the 💡 instruction lines when you're done — they're guides, not content.

## Step-by-step: How to complete this document
1. **Fill the Document Meta block** right below.
2. **Write the Project Overview** (2–3 sentences is enough).
3. **Draw the Architecture Diagram** by editing the Mermaid code block.
4. **Complete the Integration Inventory table** with every service you plan to use.
5. **Copy and fill an Integration Card** for each row in the inventory.
6. **Complete Sections 8–11** (Security, Errors, Cost, Testing).
7. **Update the Readiness Tracker** as you build.
8. **Walk the Launch Checklist** before going live.

> 💡 **Tip for beginners:** Don't try to fill everything at once. Fill the sections you know today. Come back and fill the rest tomorrow. A 70% complete spec is infinitely better than none.

---

## 📋 Document Meta

> 💡 *Fill this table in 2 minutes. It tells anyone reading this doc exactly what product it covers and who owns it.*

| Field                  | Value |
|------------------------|-------|
| **Project / Product Name** | `[e.g., Nexus — AI-powered CRM for freelancers]` |
| **Document Owner**     | `[Your name or GitHub handle]` |
| **Tech Lead / Reviewer** | `[Name or "TBD"]` |
| **Created Date**       | `[YYYY-MM-DD]` |
| **Last Updated**       | `[YYYY-MM-DD]` |
| **Document Version**   | `[1.0]` |
| **Product Stage**      | `[ ] Dev  [ ] Alpha  [ ] Beta  [ ] GA  [ ] Post-Launch` |
| **Target: First 500 Customers Date** | `[YYYY-MM-DD or "Unknown"]` |
| **Repository URL**     | `[https://github.com/your-org/your-repo]` |
| **Primary Tech Stack** | `[e.g., Next.js 14, Supabase, Python FastAPI, React Native]` |
| **Deployment Platform**| `[e.g., Vercel + Railway + AWS S3]` |

---

## 1. 🏗️ Project Overview

> 💡 *In 3–5 sentences, describe what the product does, who it's for, and why it needs these integrations. You're setting context so anyone reading this doc understands the "why" before the "what."*
>
> **Example:**
> *"Nexus is a SaaS CRM built for freelancers to track clients, invoices, and projects in one place. It integrates with Stripe for payments, OpenAI for AI-generated proposals, Supabase for data storage, and Twilio for SMS reminders. These integrations are core to the product — removing any one of them would break key user workflows."*

**Product Description:**
[Write 3–5 sentences here.]

**Why integrations are critical:**
[List 2–3 sentences explaining what breaks without these integrations.]

**Key user workflows that depend on integrations:**

| User Action | Integration Required |
|-------------|---------------------|
| `[e.g., User signs up with Google]` | `[e.g., Google OAuth]` |
| `[e.g., User pays for subscription]` | `[e.g., Stripe Billing]` |
| `[e.g., AI generates a proposal]` | `[e.g., OpenAI GPT-4o]` |
| `[Add more rows as needed]` | |

---

## 2. 🗺️ Integration Architecture Diagram

> 💡 *This diagram shows how your app connects to everything else. It's the first thing any developer, investor, or auditor looks at.*
>
> **How to edit it:** This uses [Mermaid](https://mermaid.js.org/) — a text-based diagramming language that renders automatically on GitHub. Change the node names to match your real services. Add or remove lines (`-->`) to show connections.*
>
> **Shapes guide:**
> - `[Box]` = service/system
> - `(Rounded)` = user/actor
> - `{Diamond}` = decision
> - `-->` = data flows this direction
> - `-- label -->` = labeled connection

```mermaid
graph LR
    User("👤 User")
    MobileApp["📱 Mobile App\n(iOS / Android)"]
    WebApp["🌐 Web App\n(Next.js)"]
    Backend["⚙️ Backend API\n(Your Server)"]

    subgraph "Auth & Identity"
        Auth["🔐 Auth Provider\n(e.g., Supabase Auth / Auth0)"]
    end

    subgraph "AI / LLM"
        AI["🤖 LLM Provider\n(e.g., OpenAI / Claude)"]
    end

    subgraph "Database & Storage"
        DB["🗄️ Database\n(e.g., Supabase PostgreSQL)"]
        Storage["📦 File Storage\n(e.g., AWS S3 / Supabase Storage)"]
    end

    subgraph "Third-Party APIs"
        Payments["💳 Payments\n(e.g., Stripe)"]
        Email["📧 Email\n(e.g., SendGrid / Resend)"]
        SMS["📱 SMS\n(e.g., Twilio)"]
    end

    User --> MobileApp
    User --> WebApp
    MobileApp --> Backend
    WebApp --> Backend
    Backend --> Auth
    Backend --> AI
    Backend --> DB
    Backend --> Storage
    Backend --> Payments
    Backend --> Email
    Backend --> SMS
```

> ✏️ **Customise the diagram above to match your actual services. Delete services you don't use. Add new boxes for services not listed.**

---

## 3. 📦 Integration Inventory

> 💡 *List EVERY external service your app talks to — even ones used only in development (like a mock email service). If your app calls it, it belongs here. Fill this table first, then create an Integration Card for each row below.*

| # | Integration Name | Category | Provider / Service | Status | Phase Introduced | Owner | Card Link |
|---|-----------------|----------|--------------------|--------|-----------------|-------|-----------|
| 1 | `[e.g., User Auth]` | Auth & Identity | `[e.g., Supabase Auth]` | `[ ] Planned` `[ ] In Dev` `[ ] Live` | `[e.g., Dev]` | `[Name]` | `[#auth-supabase]` |
| 2 | `[e.g., Primary DB]` | Database | `[e.g., Supabase PostgreSQL]` | `[ ] Planned` `[ ] In Dev` `[ ] Live` | `[e.g., Dev]` | `[Name]` | |
| 3 | `[e.g., File Storage]` | Storage | `[e.g., Supabase Storage]` | `[ ] Planned` `[ ] In Dev` `[ ] Live` | `[e.g., Dev]` | `[Name]` | |
| 4 | `[e.g., AI Proposals]` | AI / LLM | `[e.g., OpenAI GPT-4o]` | `[ ] Planned` `[ ] In Dev` `[ ] Live` | `[e.g., Alpha]` | `[Name]` | |
| 5 | `[e.g., Payments]` | Third-Party API | `[e.g., Stripe]` | `[ ] Planned` `[ ] In Dev` `[ ] Live` | `[e.g., Beta]` | `[Name]` | |
| 6 | `[e.g., Transactional Email]` | Third-Party API | `[e.g., Resend]` | `[ ] Planned` `[ ] In Dev` `[ ] Live` | `[e.g., Alpha]` | `[Name]` | |
| 7 | `[e.g., SMS Alerts]` | Third-Party API | `[e.g., Twilio]` | `[ ] Planned` `[ ] In Dev` `[ ] Live` | `[e.g., Beta]` | `[Name]` | |
| 8 | `[Add more]` | | | | | | |

**Status Key:** `Planned` = not started · `In Dev` = being built · `Live` = working in at least one environment

---

## 4. 🔐 Auth & Identity Integrations

> 💡 *Copy the card below for each Auth/Identity integration in your inventory. Authentication is the first thing users hit — get this wrong and nothing works.*

---

### 🔐 Auth Card: [Integration Name, e.g., "Supabase Auth"]

> 💡 *Replace "[Integration Name]" in the header above with your actual service name (e.g., "Google OAuth", "Auth0", "Firebase Auth", "Custom JWT").*

#### 📌 Overview

| Field | Value |
|-------|-------|
| **Integration Name** | `[e.g., Supabase Auth]` |
| **Provider** | `[e.g., Supabase]` |
| **Auth Type** | `[ ] OAuth 2.0  [ ] JWT  [ ] Magic Link  [ ] API Key  [ ] SSO/SAML  [ ] Custom` |
| **Purpose** | `[e.g., Handles user signup, login, session management, and password reset]` |
| **Official Docs** | `[https://supabase.com/docs/guides/auth]` |
| **SDK / Library Used** | `[e.g., @supabase/supabase-js v2]` |
| **Owner** | `[Name or GitHub handle]` |
| **Last Verified** | `[YYYY-MM-DD]` |

#### 🔑 Credentials & Configuration

> 💡 *Never write actual secret values here. Write the NAME of the environment variable instead (e.g., `SUPABASE_ANON_KEY`, not the actual key). Store real values in your `.env` file, which should NEVER be committed to git.*

| Credential | Env Variable Name | Where to Get It | Notes |
|------------|------------------|-----------------|-------|
| `[e.g., Project URL]` | `SUPABASE_URL` | `[Supabase Dashboard → Settings → API]` | `[Safe to expose in frontend]` |
| `[e.g., Anon/Public Key]` | `SUPABASE_ANON_KEY` | `[Supabase Dashboard → Settings → API]` | `[Safe to expose in frontend]` |
| `[e.g., Service Role Key]` | `SUPABASE_SERVICE_KEY` | `[Supabase Dashboard → Settings → API]` | `[⚠️ NEVER expose in frontend]` |

#### 🌐 Endpoints Used

> 💡 *List every Auth endpoint your app uses. Even if a library handles it internally, knowing the underlying endpoints helps with debugging.*

| Method | Endpoint | What It Does |
|--------|----------|-------------|
| `POST` | `/auth/v1/signup` | `[Creates a new user account]` |
| `POST` | `/auth/v1/token?grant_type=password` | `[Signs in with email + password]` |
| `POST` | `/auth/v1/logout` | `[Ends the user session]` |
| `GET`  | `/auth/v1/user` | `[Fetches the logged-in user's profile]` |
| `POST` | `/auth/v1/recover` | `[Triggers password reset email]` |
| `[Add more]` | | |

#### 🔄 Auth Flow (Sequence)

> 💡 *This diagram shows what happens step-by-step when a user logs in. Edit the steps to match your actual flow.*

```mermaid
sequenceDiagram
    participant U as 👤 User
    participant App as 📱 Your App
    participant Auth as 🔐 Auth Provider

    U->>App: Enters email + password
    App->>Auth: POST /auth/v1/token
    Auth-->>App: Returns JWT access_token + refresh_token
    App->>App: Stores tokens (securely)
    App-->>U: User is now logged in ✅

    Note over App,Auth: On subsequent requests
    App->>Auth: Sends Bearer token in Authorization header
    Auth-->>App: Validates token
```

#### ⚙️ Environment Configuration

| Environment | Value / Note |
|-------------|-------------|
| **Development** | `[e.g., Uses Supabase local dev with supabase start]` |
| **Staging** | `[e.g., Uses separate Supabase project: nexus-staging]` |
| **Production** | `[e.g., Uses production Supabase project: nexus-prod]` |

#### ⚠️ Error Handling

> 💡 *List the most common auth errors and what your app does when they occur. This prevents blank screens and confused users.*

| Error Code / Type | Meaning | What Your App Does |
|-------------------|---------|-------------------|
| `invalid_grant` | Wrong password | `[Show "Incorrect email or password" — do NOT say which is wrong]` |
| `email_not_confirmed` | User hasn't verified email | `[Show banner: "Please check your inbox to verify your email"]` |
| `JWT expired` | Session timed out | `[Auto-refresh token silently; if refresh also expired, redirect to login]` |
| `too_many_requests` | Rate limit hit | `[Show: "Too many attempts. Try again in X minutes"]` |
| `[Add more]` | | |

#### 🔒 Security Rules

> 💡 *Document any Row Level Security (RLS) policies or access rules that depend on this auth system.*

- [ ] Row Level Security (RLS) enabled on all database tables? `[Yes / No / N/A]`
- [ ] JWT secrets rotated on a schedule? Rotation schedule: `[e.g., Every 90 days]`
- [ ] Refresh tokens stored securely (httpOnly cookie or encrypted storage)? `[Yes / No]`
- [ ] Magic links expire within: `[e.g., 1 hour]`
- [ ] Password policy enforced: `[e.g., Min 8 chars, 1 uppercase, 1 number]`

#### 📊 Phase Readiness

| Phase | Status | Notes |
|-------|--------|-------|
| 🛠️ Development | `[ ] Not Started  [ ] In Progress  [x] Done` | `[e.g., Working locally with Supabase CLI]` |
| 🔬 Staging | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🧪 Alpha / Beta | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🚀 General Availability | `[ ] Not Started  [ ] In Progress  [ ] Done` | |

---

> **➕ Copy the card above for each Auth integration.** Common examples: `Google OAuth`, `Apple Sign In`, `Auth0`, `Clerk`, `Firebase Auth`, `Custom JWT`.

---

## 5. 🗄️ Database & Storage Integrations

> 💡 *Copy the card below for each database or file storage service. Your database is the most critical integration — treat it with the most care.*

---

### 🗄️ DB/Storage Card: [Integration Name, e.g., "Supabase PostgreSQL"]

#### 📌 Overview

| Field | Value |
|-------|-------|
| **Integration Name** | `[e.g., Primary Application Database]` |
| **Provider** | `[e.g., Supabase / MongoDB Atlas / PlanetScale / AWS RDS]` |
| **Database Type** | `[ ] PostgreSQL  [ ] MySQL  [ ] MongoDB  [ ] Redis  [ ] SQLite  [ ] Other: ___` |
| **Purpose** | `[e.g., Stores all user data, projects, invoices, and application state]` |
| **ORM / Query Layer** | `[e.g., Prisma ORM / Drizzle ORM / Supabase JS Client / Raw SQL]` |
| **Official Docs** | `[https://supabase.com/docs/guides/database]` |
| **Owner** | `[Name]` |
| **Last Verified** | `[YYYY-MM-DD]` |

#### 🔑 Credentials & Connection

| Credential | Env Variable Name | Notes |
|------------|------------------|-------|
| `Connection String` | `DATABASE_URL` | `[e.g., postgresql://user:pass@host:5432/db — NEVER commit this]` |
| `Host` | `DB_HOST` | |
| `Port` | `DB_PORT` | `[Default: 5432 for PostgreSQL]` |
| `Database Name` | `DB_NAME` | |
| `Pool Size` | `DB_POOL_SIZE` | `[e.g., 10 connections for small apps]` |

#### 🗂️ Core Data Models / Tables

> 💡 *List the main tables/collections in your database. You don't need to list every column — just the key ones. Link to your full schema file if it exists.*

| Table / Collection | Purpose | Key Fields | Relationships |
|--------------------|---------|-----------|---------------|
| `users` | `[Stores user accounts]` | `id, email, created_at, plan_id` | `[Has many: projects, invoices]` |
| `projects` | `[Stores freelancer projects]` | `id, user_id, name, status, deadline` | `[Belongs to: users]` |
| `invoices` | `[Stores billing records]` | `id, user_id, amount, status, stripe_id` | `[Belongs to: users]` |
| `[Add more]` | | | |

**Full schema file location:** `[e.g., /prisma/schema.prisma or /db/migrations/]`

#### 🌐 Environments & Connection Strings

| Environment | Connection Config | Notes |
|-------------|-----------------|-------|
| **Development** | `[e.g., localhost:5432/nexus_dev or supabase start]` | `[Never use production data locally]` |
| **Staging** | `[e.g., staging-db.supabase.co]` | `[Use anonymized/seeded test data]` |
| **Production** | `[e.g., db.xxxx.supabase.co]` | `[SSL required. Connection pooling via pgBouncer]` |

#### 📦 Backups & Data Retention

| Policy | Value |
|--------|-------|
| Backup Frequency | `[e.g., Daily automated backups by Supabase]` |
| Retention Period | `[e.g., 7 days on free tier, 30 days on Pro]` |
| Manual Backup Process | `[e.g., pg_dump command or Supabase dashboard download]` |
| Data Deletion Policy | `[e.g., Soft delete (deleted_at column) — hard delete after 90 days]` |

#### ⚠️ Error Handling

| Error | Meaning | What Your App Does |
|-------|---------|-------------------|
| `Connection timeout` | DB unreachable | `[Retry 3× with 1s backoff; log error; show "Service temporarily unavailable"]` |
| `Unique constraint violation` | Duplicate record | `[Return 409 Conflict with field name]` |
| `Foreign key violation` | Referenced record doesn't exist | `[Return 422 Unprocessable Entity]` |
| `Max connections reached` | Connection pool exhausted | `[Queue requests; alert via monitoring]` |
| `[Add more]` | | |

#### 📊 Phase Readiness

| Phase | Status | Notes |
|-------|--------|-------|
| 🛠️ Development | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🔬 Staging | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🧪 Alpha / Beta | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🚀 General Availability | `[ ] Not Started  [ ] In Progress  [ ] Done` | |

---

### 📦 Storage Card: [Integration Name, e.g., "Supabase Storage / AWS S3"]

#### 📌 Overview

| Field | Value |
|-------|-------|
| **Integration Name** | `[e.g., User File Storage]` |
| **Provider** | `[e.g., Supabase Storage / AWS S3 / Cloudflare R2 / Uploadthing]` |
| **Purpose** | `[e.g., Stores user-uploaded profile pictures, invoice PDFs, and contract files]` |
| **Official Docs** | `[https://supabase.com/docs/guides/storage]` |
| **Owner** | `[Name]` |

#### 🔑 Credentials

| Credential | Env Variable Name | Notes |
|------------|------------------|-------|
| `Bucket Name` | `STORAGE_BUCKET` | `[e.g., nexus-user-files]` |
| `Region` | `STORAGE_REGION` | `[e.g., us-east-1]` |
| `Access Key` | `STORAGE_ACCESS_KEY` | `[⚠️ Backend only — never expose in frontend]` |
| `Secret Key` | `STORAGE_SECRET_KEY` | `[⚠️ Backend only — never expose in frontend]` |

#### 📂 Folder / Bucket Structure

| Folder Path | Contents | Access |
|------------|----------|--------|
| `/avatars/{user_id}/` | `[Profile pictures]` | `[Public read / Authenticated write]` |
| `/invoices/{user_id}/` | `[Generated PDFs]` | `[Private — owner only]` |
| `/contracts/{user_id}/` | `[Uploaded contracts]` | `[Private — owner only]` |
| `[Add more]` | | |

#### ⚙️ File Policies

| Policy | Value |
|--------|-------|
| Max File Size | `[e.g., 10MB per file]` |
| Allowed MIME Types | `[e.g., image/jpeg, image/png, application/pdf]` |
| Virus Scanning | `[e.g., Not implemented / Using ClamAV / Cloudflare WAF]` |
| CDN / Public URL Pattern | `[e.g., https://storage.supabase.co/nexus/avatars/{user_id}/avatar.jpg]` |

#### 📊 Phase Readiness

| Phase | Status | Notes |
|-------|--------|-------|
| 🛠️ Development | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🔬 Staging | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🧪 Alpha / Beta | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🚀 General Availability | `[ ] Not Started  [ ] In Progress  [ ] Done` | |

---

## 6. 🤖 AI / LLM Integrations

> 💡 *This section is dedicated to AI/LLM integrations because they have unique concerns: token limits, hallucination risks, cost spikes, prompt versioning, and model deprecation. Each AI feature your app offers should have its own card below.*
>
> **Key AI terms you need to know:**
> - **Token** = a chunk of text (~4 characters or ¾ of a word). AI APIs charge per token.
> - **Context Window** = max tokens the model can "see" at once (your prompt + the response).
> - **System Prompt** = instructions you give the AI before the user speaks (sets behavior/persona).
> - **Temperature** = how "creative" the AI is. 0 = very predictable, 1 = very creative.
> - **Streaming** = sending the AI response word-by-word as it's generated (better UX).
> - **Fallback Model** = a cheaper/simpler model used if the primary model fails or is overloaded.

---

### 🤖 AI Card: [Feature Name, e.g., "AI Proposal Generator"]

> 💡 *Create one card per AI-powered FEATURE, not per model. If you use GPT-4o for three features, create three cards.*

#### 📌 Overview

| Field | Value |
|-------|-------|
| **Feature Name** | `[e.g., AI Proposal Generator]` |
| **AI Provider** | `[e.g., OpenAI / Anthropic / Google / Mistral / Local (Ollama)]` |
| **Primary Model** | `[e.g., gpt-4o-mini / claude-3-5-haiku / gemini-2.0-flash]` |
| **Fallback Model** | `[e.g., gpt-3.5-turbo / claude-3-haiku]` |
| **Official Docs** | `[https://platform.openai.com/docs]` |
| **SDK / Library** | `[e.g., openai v4 (Node.js) / anthropic-sdk / LangChain]` |
| **Purpose** | `[e.g., Generates a professional project proposal from user-provided project details]` |
| **User-Facing or Internal?** | `[e.g., User-facing — shown directly in the UI]` |
| **Owner** | `[Name]` |
| **Last Verified** | `[YYYY-MM-DD]` |

#### 🔑 Credentials

| Credential | Env Variable Name | Notes |
|------------|------------------|-------|
| `API Key` | `OPENAI_API_KEY` | `[⚠️ Backend only — NEVER send this to the frontend]` |
| `Organization ID` | `OPENAI_ORG_ID` | `[Optional — for team accounts]` |
| `[Custom endpoint]` | `AI_BASE_URL` | `[Only if using a custom gateway/proxy]` |

#### ⚙️ Model Configuration

> 💡 *These settings control how the AI behaves. Copy the exact values into your code — don't leave them as magic numbers with no documentation.*

| Parameter | Value | Why This Value? |
|-----------|-------|----------------|
| `model` | `[e.g., gpt-4o-mini]` | `[e.g., Cheaper than GPT-4o; quality is good enough for proposals]` |
| `temperature` | `[e.g., 0.7]` | `[e.g., Some creativity needed; 0.7 = professional but not robotic]` |
| `max_tokens` | `[e.g., 1500]` | `[e.g., Proposals don't need to be longer than ~1200 words]` |
| `top_p` | `[e.g., 1.0]` | `[e.g., Default — only change if testing output quality]` |
| `stream` | `[e.g., true]` | `[e.g., Stream for better UX — user sees text appear word by word]` |
| `response_format` | `[e.g., { type: "text" } or { type: "json_object" }]` | `[e.g., JSON mode when structured output is required]` |
| `timeout` | `[e.g., 30 seconds]` | `[e.g., Abort if no response after 30s — show error to user]` |

#### 📝 Prompt Design

> 💡 *Document your prompts here — they are as important as your code. When the AI behaves unexpectedly, this is the first place to look. Store the actual prompt files at the path listed below.*

**Prompt file location:** `[e.g., /lib/prompts/proposal-generator.ts or /prompts/proposal.txt]`

**System Prompt Summary:**
```
[Paste a short summary or the actual system prompt here. Example:]

You are a professional proposal writer for freelancers.
Your job is to write clear, concise, and persuasive project proposals
based on the details provided by the user.
- Use formal but friendly language.
- Maximum 4 paragraphs.
- Do not invent details not provided by the user.
- Format the output in Markdown.
```

**User Prompt Template:**
```
[Paste your user message template. Use {curly_braces} for variables. Example:]

Write a project proposal for the following:
- Project Name: {project_name}
- Client: {client_name}
- Scope: {scope}
- Timeline: {timeline}
- Budget: {budget}
```

**Variables passed to the prompt:**

| Variable | Source | Example Value |
|----------|--------|--------------|
| `{project_name}` | `[User input form]` | `"Brand Identity Redesign"` |
| `{client_name}` | `[User's saved client record]` | `"Acme Corp"` |
| `{scope}` | `[User input form]` | `"Logo, colors, typography, and brand guide"` |
| `[Add more]` | | |

#### 💰 Cost & Token Management

> 💡 *Token costs add up fast. Fill this table so you know your cost per call and can set a monthly budget. Check the provider's pricing page for current rates.*

| Metric | Value |
|--------|-------|
| **Input Token Price** | `[e.g., $0.00015 per 1K tokens for GPT-4o-mini]` |
| **Output Token Price** | `[e.g., $0.00060 per 1K tokens for GPT-4o-mini]` |
| **Est. Tokens per Call (Input)** | `[e.g., ~600 tokens (system + user prompt)]` |
| **Est. Tokens per Call (Output)** | `[e.g., ~1200 tokens (proposal response)]` |
| **Est. Cost per Call** | `[e.g., ~$0.0008 — under $0.001 per proposal]` |
| **Est. Calls per Day (at 500 users)** | `[e.g., ~250 calls/day (50% of users generate 1 proposal/day)]` |
| **Est. Monthly Cost at 500 Users** | `[e.g., ~$6/month — very affordable]` |
| **Monthly Budget Alert Threshold** | `[e.g., Alert at $50/month]` |
| **Budget Hard Cap** | `[e.g., Cut off at $200/month to prevent runaway costs]` |

**Rate Limits (from provider's docs):**

| Limit Type | Free Tier | Paid Tier |
|------------|-----------|-----------|
| Requests per Minute (RPM) | `[e.g., 3 RPM]` | `[e.g., 500 RPM]` |
| Tokens per Minute (TPM) | `[e.g., 40,000 TPM]` | `[e.g., 200,000 TPM]` |
| Max Context Window | `[e.g., 128,000 tokens]` | `[Same]` |

**How rate limits are handled:** `[e.g., Exponential backoff with 3 retries; queue requests during peak load; fall back to cheaper model if primary is rate-limited]`

#### 🔄 AI Request Flow

```mermaid
sequenceDiagram
    participant U as 👤 User
    participant App as ⚙️ Backend API
    participant Cache as 📦 Cache (Redis/Memory)
    participant AI as 🤖 AI Provider

    U->>App: POST /api/generate-proposal (with project details)
    App->>App: Validate input & sanitize PII
    App->>Cache: Check if identical prompt was recently cached
    alt Cache Hit
        Cache-->>App: Return cached response
        App-->>U: Return proposal (instant ⚡)
    else Cache Miss
        App->>AI: POST /chat/completions (stream: true)
        AI-->>App: Stream tokens back
        App-->>U: Stream tokens to UI in real-time
        App->>Cache: Store response (TTL: 1 hour)
    end
```

#### 🛡️ Safety & Content Policy

> 💡 *AI can generate harmful content if not properly controlled. Document how you prevent this.*

| Concern | Your Approach |
|---------|--------------|
| **PII in prompts** | `[e.g., Strip emails/phone numbers from user input before sending to AI]` |
| **Prompt injection** | `[e.g., Validate that user input doesn't contain instruction-like text; use system prompt to set hard boundaries]` |
| **Harmful content** | `[e.g., Enable provider's content filtering (OpenAI moderation API); add keyword blocklist]` |
| **Data sent to AI** | `[e.g., Only project metadata sent — no passwords, payment info, or sensitive PII]` |
| **AI output validation** | `[e.g., Validate JSON output schema before saving to DB; display disclaimer to users]` |
| **Model training opt-out** | `[e.g., Opted out of OpenAI model training via org settings]` |

#### ⚠️ Error Handling

| Error | Meaning | What Your App Does |
|-------|---------|-------------------|
| `429 Too Many Requests` | Rate limit hit | `[Wait and retry with exponential backoff (1s, 2s, 4s); after 3 tries, fall back to simpler model]` |
| `500 Server Error` | AI provider is down | `[Retry once; if still failing, show: "AI is temporarily unavailable. Please try again in a moment."]` |
| `context_length_exceeded` | Input too long | `[Truncate the longest input field and retry; log which field was truncated]` |
| `content_filter_triggered` | Blocked content | `[Show: "Your request couldn't be completed. Please rephrase and try again."]` |
| `Request timeout` | AI took too long | `[Cancel after 30s; show timeout message; log for monitoring]` |
| `[Add more]` | | |

#### 🧪 Testing & Mocking

| Approach | Details |
|----------|---------|
| **Unit tests** | `[e.g., Mock the OpenAI client using jest.mock(); test with fixed JSON responses]` |
| **Integration tests** | `[e.g., Run against real API in staging with test API key; assert response shape matches schema]` |
| **Mock file location** | `[e.g., /tests/mocks/openai.ts]` |
| **Recorded fixtures** | `[e.g., Save real API responses to /tests/fixtures/proposal-response.json for replay]` |
| **Cost guard** | `[e.g., Tests only call real API when explicitly flagged with LIVE_AI_TESTS=true env var]` |

#### 📊 Phase Readiness

| Phase | Status | Notes |
|-------|--------|-------|
| 🛠️ Development | `[ ] Not Started  [ ] In Progress  [ ] Done` | `[e.g., Using mocked responses; real API calls only when needed]` |
| 🔬 Staging | `[ ] Not Started  [ ] In Progress  [ ] Done` | `[e.g., Real API calls with test data; budget cap at $10]` |
| 🧪 Alpha / Beta | `[ ] Not Started  [ ] In Progress  [ ] Done` | `[e.g., Monitor cost/user; add rate limiting per user]` |
| 🚀 General Availability | `[ ] Not Started  [ ] In Progress  [ ] Done` | `[e.g., Full monitoring + budget alerts enabled]` |

---

> **➕ Copy the AI Card for each AI feature.** Common examples: `AI Chatbot`, `Auto-Tagging`, `Summarization`, `Embedding / Semantic Search`, `Code Generation`, `Image Analysis`.

---

## 7. 🔌 Third-Party API Integrations

> 💡 *These are the external services that handle payments, messaging, analytics, etc. Copy the card template below for each.*

---

### 🔌 API Card: [Integration Name, e.g., "Stripe Billing"]

#### 📌 Overview

| Field | Value |
|-------|-------|
| **Integration Name** | `[e.g., Stripe Billing]` |
| **Provider** | `[e.g., Stripe]` |
| **Purpose** | `[e.g., Handles subscription billing, one-time payments, invoicing, and refunds]` |
| **Integration Type** | `[ ] REST API  [ ] SDK  [ ] Webhook  [ ] Both API + Webhook` |
| **Official Docs** | `[https://stripe.com/docs]` |
| **SDK / Library** | `[e.g., stripe v14 (Node.js)]` |
| **API Version** | `[e.g., 2024-09-30.acacia]` |
| **Owner** | `[Name]` |
| **Last Verified** | `[YYYY-MM-DD]` |

#### 🔑 Credentials

| Credential | Env Variable Name | Where to Get It |
|------------|------------------|-----------------|
| `Publishable Key` | `STRIPE_PUBLISHABLE_KEY` | `[Stripe Dashboard → Developers → API keys]` |
| `Secret Key` | `STRIPE_SECRET_KEY` | `[Stripe Dashboard → Developers → API keys]` |
| `Webhook Secret` | `STRIPE_WEBHOOK_SECRET` | `[Stripe Dashboard → Webhooks → Signing secret]` |

> ⚠️ **Test vs. Live keys:** Stripe gives you TWO sets of keys — test and live. Use `sk_test_...` keys in development/staging. Only use `sk_live_...` keys in production. Mixing them up causes real charges on fake data.

#### 🌐 Base URL & Key Endpoints

| Environment | Base URL |
|-------------|---------|
| Test (Dev/Staging) | `https://api.stripe.com` (using test keys) |
| Production | `https://api.stripe.com` (using live keys) |

| Method | Endpoint / SDK Call | What It Does |
|--------|---------------------|-------------|
| `POST` | `stripe.customers.create()` | `[Creates a Stripe customer when user signs up]` |
| `POST` | `stripe.subscriptions.create()` | `[Starts a subscription when user upgrades]` |
| `POST` | `stripe.billingPortal.sessions.create()` | `[Opens Stripe's hosted billing management page]` |
| `Webhook` | `checkout.session.completed` | `[Fires when a payment succeeds — update user plan in DB]` |
| `Webhook` | `customer.subscription.deleted` | `[Fires when subscription is cancelled — downgrade user]` |
| `Webhook` | `invoice.payment_failed` | `[Fires on failed payment — send dunning email]` |
| `[Add more]` | | |

#### 🔄 Integration Flow

```mermaid
sequenceDiagram
    participant U as 👤 User
    participant App as ⚙️ Your App
    participant Stripe as 💳 Stripe

    U->>App: Clicks "Upgrade to Pro"
    App->>Stripe: Create Checkout Session (customer_id, price_id)
    Stripe-->>App: Returns checkout_url
    App-->>U: Redirect to Stripe Checkout page
    U->>Stripe: Enters card details & confirms payment
    Stripe-->>App: Sends webhook: checkout.session.completed
    App->>App: Verify webhook signature (STRIPE_WEBHOOK_SECRET)
    App->>App: Update user.plan = "pro" in database
    Stripe-->>U: Redirects back to your app (success_url)
    App-->>U: Shows "Welcome to Pro! 🎉"
```

#### ⚠️ Error Handling

| Error Code / Type | Meaning | What Your App Does |
|-------------------|---------|-------------------|
| `card_declined` | Payment declined | `[Show Stripe's decline message; do not downgrade user yet]` |
| `insufficient_funds` | Card has no money | `[Show: "Payment failed. Please use a different card."]` |
| `webhook signature mismatch` | Possible fake webhook | `[Reject immediately; log security alert]` |
| `rate_limit_error` | Too many Stripe API calls | `[Retry after 1 second; implement request queue]` |
| `api_connection_error` | Stripe unreachable | `[Retry 3× with backoff; show "Payment service temporarily unavailable"]` |
| `[Add more]` | | |

#### 💰 Cost & Rate Limits

| Metric | Value |
|--------|-------|
| **Transaction Fee** | `[e.g., 2.9% + $0.30 per transaction]` |
| **Monthly Cost at 500 Customers** | `[e.g., ~$X if avg. subscription is $Y/month]` |
| **API Rate Limit** | `[e.g., 100 read operations/second in test; 200 in live]` |
| **Webhook Retry Policy** | `[e.g., Stripe retries failed webhooks for 3 days, up to 15 attempts]` |

#### 🧪 Testing & Mocking

| Approach | Details |
|----------|---------|
| **Test Card Numbers** | `[e.g., 4242 4242 4242 4242 (always succeeds), 4000 0000 0000 0002 (always declines)]` |
| **Local Webhook Testing** | `[e.g., Use Stripe CLI: stripe listen --forward-to localhost:3000/api/webhooks/stripe]` |
| **Mock in Unit Tests** | `[e.g., Mock stripe SDK; return fixed PaymentIntent objects]` |
| **Test Scenarios** | `[e.g., Successful payment, declined card, subscription cancellation, refund]` |

#### 📊 Phase Readiness

| Phase | Status | Notes |
|-------|--------|-------|
| 🛠️ Development | `[ ] Not Started  [ ] In Progress  [ ] Done` | `[Use test keys + Stripe CLI]` |
| 🔬 Staging | `[ ] Not Started  [ ] In Progress  [ ] Done` | |
| 🧪 Alpha / Beta | `[ ] Not Started  [ ] In Progress  [ ] Done` | `[Switch to live keys after QA approval]` |
| 🚀 General Availability | `[ ] Not Started  [ ] In Progress  [ ] Done` | |

---

> **➕ Copy the API Card for each third-party integration.** Common examples: `Resend (Email)`, `Twilio (SMS)`, `SendGrid`, `Intercom`, `HubSpot`, `Segment`, `Mixpanel`, `Google Analytics`, `Sentry`.

---

## 8. 🔒 Security & Secrets Management

> 💡 *This section documents how ALL secrets (API keys, database passwords, tokens) are stored, used, and protected across your entire project. A single leaked secret can compromise your users' data, cause unexpected charges, or destroy your reputation.*

### 8.1 Secrets Inventory

> 💡 *List every secret your app uses. Never write the actual value here — only the variable name.*

| Secret Name (Env Variable) | Used By | Exposure Risk | Storage Method | Rotation Schedule |
|---------------------------|---------|--------------|----------------|------------------|
| `DATABASE_URL` | `[Backend only]` | `[Critical]` | `[.env + Vercel Environment Variables]` | `[Rotate if compromised]` |
| `OPENAI_API_KEY` | `[Backend only]` | `[High]` | `[.env + Vercel Environment Variables]` | `[Every 90 days]` |
| `STRIPE_SECRET_KEY` | `[Backend only]` | `[Critical]` | `[.env + Vercel Environment Variables]` | `[Every 90 days]` |
| `STRIPE_WEBHOOK_SECRET` | `[Backend only]` | `[High]` | `[.env + Vercel Environment Variables]` | `[When endpoint changes]` |
| `SUPABASE_SERVICE_KEY` | `[Backend only]` | `[Critical]` | `[.env + Vercel Environment Variables]` | `[Every 90 days]` |
| `SUPABASE_ANON_KEY` | `[Frontend safe]` | `[Low]` | `[Public env var — safe to expose]` | `[N/A]` |
| `[Add more]` | | | | |

### 8.2 Secrets Storage Rules

| Rule | Status |
|------|--------|
| `.env` file is in `.gitignore` | `[ ] Yes  [ ] No — FIX THIS NOW` |
| `.env.example` file exists with placeholder values (no real secrets) | `[ ] Yes  [ ] No` |
| Secrets are stored in platform env vars (Vercel, Railway, etc.) for deployment | `[ ] Yes  [ ] No` |
| No API keys are hardcoded in source code | `[ ] Yes  [ ] No — scan with git-secrets` |
| No secrets are logged to console or error tracking | `[ ] Yes  [ ] No` |
| Secrets management tool used (e.g., Doppler, Infisical, AWS Secrets Manager) | `[ ] Yes — Tool: ___ [ ] No — using .env only` |

### 8.3 Environment Separation

> 💡 *Each environment should have its OWN set of credentials. Never use production keys in development.*

| Service | Dev Key/Config | Staging Key/Config | Prod Key/Config |
|---------|---------------|-------------------|-----------------|
| `Database` | `[Local Supabase]` | `[nexus-staging project]` | `[nexus-prod project]` |
| `AI Provider` | `[Same key, $10 budget cap]` | `[Same key, $50 budget cap]` | `[Same key, $500 budget cap]` |
| `Stripe` | `[Test keys (sk_test_...)]` | `[Test keys]` | `[Live keys (sk_live_...)]` |
| `Email` | `[Resend test mode or Mailtrap]` | `[Resend — real sends]` | `[Resend — real sends]` |

### 8.4 Security Checklist

- [ ] All external inputs are validated and sanitized before use
- [ ] SQL injection is prevented (parameterized queries / ORM used)
- [ ] XSS is prevented (output escaping in frontend)
- [ ] CORS is configured to only allow trusted origins
- [ ] HTTPS is enforced on all environments (including local dev if possible)
- [ ] Webhook payloads are signature-verified before processing
- [ ] User-uploaded files are virus-scanned before storage
- [ ] Admin-only endpoints require additional authorization checks
- [ ] Dependency vulnerabilities are scanned (`npm audit` or Dependabot)
- [ ] Error messages don't leak stack traces or internal details to users

---

## 9. ⚠️ Error Handling & Retry Strategy

> 💡 *This section defines the global rules for how your app handles failures. Think of it as your "what to do when things go wrong" playbook. Without it, errors cause blank screens, lost data, or angry users.*

### 9.1 Error Response Standard

> 💡 *Define a consistent format for all API error responses. Consistency makes debugging much easier.*

**All API errors should return this JSON structure:**

```json
{
  "error": {
    "code": "STRIPE_PAYMENT_FAILED",
    "message": "Your payment could not be processed. Please try a different card.",
    "details": "Card declined by issuer.",
    "requestId": "req_abc123xyz",
    "timestamp": "2026-10-14T09:30:00Z"
  }
}
```

| Field | Description |
|-------|-------------|
| `code` | `[Machine-readable error code — used for logging and localization]` |
| `message` | `[Human-readable message safe to show users]` |
| `details` | `[More technical detail — show only in dev/staging, hide in production]` |
| `requestId` | `[Unique ID for this request — helps with support tickets]` |
| `timestamp` | `[When the error occurred — ISO 8601 format]` |

### 9.2 HTTP Status Code Reference

| Status Code | When to Use | Example |
|-------------|------------|---------|
| `200 OK` | Request succeeded | Returning user data |
| `201 Created` | Resource created | New user registered |
| `400 Bad Request` | Invalid input from client | Missing required field |
| `401 Unauthorized` | Not logged in | No auth token provided |
| `403 Forbidden` | Logged in but no permission | User accessing another user's data |
| `404 Not Found` | Resource doesn't exist | Invoice ID not found |
| `409 Conflict` | Duplicate/conflict | Email already registered |
| `422 Unprocessable` | Valid format but bad logic | Start date after end date |
| `429 Too Many Requests` | Rate limit hit | Too many login attempts |
| `500 Internal Server Error` | Your server crashed | Unhandled exception |
| `502/503 Service Unavailable` | External service is down | Stripe/OpenAI down |

### 9.3 Retry Strategy (Global Rules)

> 💡 *"Exponential backoff" means waiting longer and longer between retries: 1s → 2s → 4s → give up. This avoids hammering a struggling service.*

| Rule | Value |
|------|-------|
| **Max Retry Attempts** | `[e.g., 3 retries]` |
| **Initial Wait** | `[e.g., 1 second]` |
| **Backoff Multiplier** | `[e.g., 2× (so: 1s, 2s, 4s)]` |
| **Max Wait Between Retries** | `[e.g., 30 seconds]` |
| **Jitter** | `[e.g., Add ±0-500ms random delay to prevent thundering herd]` |
| **Which errors to retry** | `[e.g., Network errors, 429, 502, 503, 504]` |
| **Which errors NOT to retry** | `[e.g., 400, 401, 403, 404, 422 — retrying won't fix these]` |

### 9.4 Circuit Breaker (for AI / High-Frequency Integrations)

> 💡 *A circuit breaker "opens" (stops sending requests) when too many failures occur, giving the failing service time to recover. This prevents your app from being overwhelmed by cascading failures.*

| Setting | Value |
|---------|-------|
| **Failure Threshold to Open** | `[e.g., 5 failures in 60 seconds]` |
| **How Long Circuit Stays Open** | `[e.g., 30 seconds]` |
| **Recovery Test Request** | `[e.g., Send 1 request after 30s; if it succeeds, close circuit]` |
| **Applies to** | `[e.g., OpenAI, Stripe API calls]` |
| **Fallback Behavior** | `[e.g., Show cached response or "Service temporarily unavailable" message]` |

### 9.5 User-Facing Error Messages

> 💡 *Never show technical errors to users. Map every technical error to a friendly message.*

| Technical Error | User-Facing Message |
|----------------|---------------------|
| `Database connection failed` | `"Something went wrong on our end. Our team has been notified. Please try again in a moment."` |
| `AI provider timeout` | `"Our AI assistant is taking longer than usual. Please try again."` |
| `Stripe card_declined` | `"Your payment couldn't be processed. Please check your card details or try a different card."` |
| `JWT expired` | `"Your session has expired. Please log in again."` |
| `File too large` | `"This file is too large. Please upload a file under 10MB."` |
| `Rate limit exceeded` | `"You're doing that too fast! Please wait a moment and try again."` |

---

## 10. 💰 Cost & Rate Limit Management

> 💡 *This section tracks the financial and usage costs of all your integrations. As you grow from 0 → 500 customers, costs scale — and surprises here can sink a startup.*

### 10.1 Cost Summary Table

> 💡 *Estimate costs at different growth milestones. Update this table monthly once you have real usage data.*

| Integration | Pricing Model | Est. Cost/Month (10 users) | Est. Cost/Month (100 users) | Est. Cost/Month (500 users) |
|-------------|--------------|---------------------------|-----------------------------|-----------------------------|
| `[e.g., Supabase]` | `[Free tier / Pro $25/mo]` | `[$0 (free tier)]` | `[$25]` | `[$25-$100]` |
| `[e.g., OpenAI GPT-4o-mini]` | `[Pay-per-token]` | `[~$1]` | `[~$10]` | `[~$50]` |
| `[e.g., Stripe]` | `[2.9% + $0.30/txn]` | `[~$15]` | `[~$150]` | `[~$750]` |
| `[e.g., Resend Email]` | `[3,000/mo free; then $20/mo]` | `[$0]` | `[$0]` | `[$20]` |
| `[e.g., Twilio SMS]` | `[$0.0079/message]` | `[~$2]` | `[~$20]` | `[~$100]` |
| **TOTAL** | | `[~$18]` | `[~$205]` | `[~$995]` |

### 10.2 Rate Limit Reference

| Service | Free Limit | Paid Limit | How to Check | What Happens if Exceeded |
|---------|-----------|------------|--------------|--------------------------|
| `[OpenAI]` | `[3 RPM / 40K TPM]` | `[500 RPM / 200K TPM]` | `[x-ratelimit-* headers]` | `[429 error — retry with backoff]` |
| `[Stripe]` | `[100 read/s]` | `[200 read/s]` | `[Stripe Dashboard]` | `[429 error]` |
| `[Supabase Auth]` | `[100 emails/hour]` | `[Configurable]` | `[Dashboard → Auth → Settings]` | `[Silently drops emails — very dangerous!]` |
| `[Add more]` | | | | |

### 10.3 Budget Alerts & Controls

| Control | Configuration |
|---------|--------------|
| **AI Spending Alert** | `[e.g., OpenAI Dashboard → Billing → Set $50/month usage alert]` |
| **AI Hard Cap** | `[e.g., OpenAI Dashboard → Billing → Set $200/month hard limit]` |
| **Per-User AI Limit** | `[e.g., Max 10 AI requests/user/day — tracked in Redis]` |
| **Monitoring Tool** | `[e.g., Sentry + custom Slack alert when spend > threshold]` |
| **Review Schedule** | `[e.g., Check costs every Monday morning]` |

---

## 11. 🧪 Testing & Mocking Strategy

> 💡 *Testing your integrations is how you catch bugs BEFORE they hit real users. This section explains how to test each type of integration safely and affordably (without making real API calls every time).*

### 11.1 Testing Levels Explained

| Test Type | What It Tests | Makes Real API Calls? | When to Run |
|-----------|--------------|----------------------|-------------|
| **Unit Test** | A single function in isolation | No (mocked) | On every code change |
| **Integration Test** | Your code + the real external service | Yes (using test keys/sandboxes) | Before merging to main branch |
| **End-to-End (E2E) Test** | Complete user flow from UI to database | Sometimes | Before every release |
| **Manual QA** | Human tester follows a test script | Yes (staging environment) | Before major milestones |

### 11.2 Mocking Strategy per Integration Type

| Integration Type | Mocking Approach | Tools Used |
|-----------------|-----------------|------------|
| **Auth (Supabase/Auth0)** | `[Mock the auth client; return a fake session object with a test user]` | `[jest.mock, msw]` |
| **Database** | `[Use a local SQLite or in-memory DB for unit tests; real staging DB for integration tests]` | `[Prisma + SQLite, or Supabase local]` |
| **AI / LLM (OpenAI)** | `[Mock openai client in unit tests; use real API in integration tests with LIVE_AI_TESTS=true flag]` | `[jest.mock, msw (Mock Service Worker)]` |
| **Stripe** | `[Use Stripe test keys + test card numbers; mock SDK in unit tests; Stripe CLI for webhook testing]` | `[stripe-mock, Stripe CLI]` |
| **Email (Resend)** | `[Use Resend's sandbox domain in dev/staging; emails go to a test inbox, not real users]` | `[Resend sandbox, Mailtrap]` |
| **SMS (Twilio)** | `[Use Twilio test credentials — messages are validated but not actually sent]` | `[Twilio test creds]` |

### 11.3 Test Environment Configuration

```
# .env.test — values for automated test runs
DATABASE_URL=postgresql://localhost:5432/nexus_test
OPENAI_API_KEY=sk-test-... # Only real if LIVE_AI_TESTS=true
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_test_...
RESEND_API_KEY=re_test_...
SUPABASE_URL=http://localhost:54321
SUPABASE_ANON_KEY=test-anon-key
```

### 11.4 Test Scenarios per Integration

> 💡 *For each integration, define the "happy path" (everything works) and "sad paths" (various failures). A QA tester or automation script should be able to run through this list.*

#### Auth Tests
- [ ] User signs up with valid email/password → account created, email sent ✅
- [ ] User signs up with duplicate email → 409 error with friendly message ✅
- [ ] User logs in with wrong password → 401 error, no lockout on first attempt ✅
- [ ] User logs in after 5 wrong attempts → account locked / rate limited ✅
- [ ] Token expiry → silent refresh works; if refresh fails, redirect to login ✅
- [ ] Password reset flow → email received within 60s, link works once only ✅

#### Payment Tests
- [ ] Checkout with test card `4242 4242 4242 4242` → payment succeeds, plan upgraded ✅
- [ ] Checkout with declining card `4000 0000 0000 0002` → payment fails, plan unchanged ✅
- [ ] Webhook: `checkout.session.completed` → user's plan updated in DB ✅
- [ ] Webhook with invalid signature → request rejected (401) ✅
- [ ] Subscription cancellation → plan downgraded at period end ✅

#### AI Tests
- [ ] Generate proposal with valid input → response received within 30s ✅
- [ ] Generate proposal with empty input → validation error before API call ✅
- [ ] AI provider returns 429 → retry with backoff; fallback model used if all retries fail ✅
- [ ] AI response is malformed JSON → handled gracefully; no crash ✅
- [ ] AI prompt contains PII → PII stripped before sending ✅

---

## 12. 📊 Integration Readiness Tracker

> 💡 *This table gives you a bird's-eye view of every integration's readiness across your product lifecycle. Update it every sprint or before each milestone review. It's your "dashboard" for launch readiness.*

| Integration | Dev 🛠️ | Staging 🔬 | Alpha 🧪 | Beta 🚀 | GA ✅ | Owner | Last Updated |
|------------|--------|------------|---------|--------|------|-------|-------------|
| `Auth (Supabase)` | `✅` | `✅` | `⏳` | `⬜` | `⬜` | `[Name]` | `[Date]` |
| `Database (Postgres)` | `✅` | `✅` | `⏳` | `⬜` | `⬜` | `[Name]` | `[Date]` |
| `File Storage` | `✅` | `⬜` | `⬜` | `⬜` | `⬜` | `[Name]` | `[Date]` |
| `AI - Proposal Generator` | `⏳` | `⬜` | `⬜` | `⬜` | `⬜` | `[Name]` | `[Date]` |
| `Stripe Billing` | `⬜` | `⬜` | `⬜` | `⬜` | `⬜` | `[Name]` | `[Date]` |
| `Email (Resend)` | `⬜` | `⬜` | `⬜` | `⬜` | `⬜` | `[Name]` | `[Date]` |
| `SMS (Twilio)` | `⬜` | `⬜` | `⬜` | `⬜` | `⬜` | `[Name]` | `[Date]` |
| `[Add more]` | `⬜` | `⬜` | `⬜` | `⬜` | `⬜` | | |

**Legend:** `✅` = Complete · `⏳` = In Progress · `⬜` = Not Started · `❌` = Blocked

---

## 13. 🚀 Launch Readiness Checklist

> 💡 *Walk through this checklist before each milestone. Your goal is to reach ✅ on every item before you call yourself "launched." Items marked 🔴 are critical — do NOT go live without them.*

### Phase 1: Development Complete

- [ ] 🔴 All integration cards in this document are filled out
- [ ] 🔴 No secrets are committed to the git repository
- [ ] 🔴 `.env.example` file exists with all required variable names
- [ ] 🔴 All integrations work locally (Development environment)
- [ ] 🔴 Basic error handling implemented for every integration
- [ ] Unit tests written for core business logic
- [ ] README explains how to set up integrations locally

### Phase 2: Alpha (Internal Testing, ~5–20 Users)

- [ ] 🔴 Staging environment is set up and all integrations work there
- [ ] 🔴 All credentials in staging are different from production
- [ ] 🔴 Webhook endpoints are live and verified (use real webhook delivery)
- [ ] 🔴 Auth flow tested end-to-end (signup → login → logout → password reset)
- [ ] 🔴 Payment flow tested with Stripe test cards
- [ ] AI rate limits and cost caps are configured
- [ ] Error monitoring is set up (e.g., Sentry) and catching real errors
- [ ] Logs are being collected and are readable
- [ ] Integration test suite passes in CI/CD pipeline

### Phase 3: Beta (Closed Beta, ~20–100 Users)

- [ ] 🔴 Production environment is set up (separate from staging)
- [ ] 🔴 Stripe live keys are configured in production ONLY
- [ ] 🔴 All API keys in production are live (not test) — EXCEPT intentionally staged ones
- [ ] 🔴 SSL/TLS certificates are valid on all domains
- [ ] 🔴 CORS is configured to only allow your domains
- [ ] 🔴 Webhook signature verification is active for all webhooks
- [ ] 🔴 Per-user rate limiting is implemented for AI features
- [ ] Budget alerts are configured for all paid services
- [ ] Customer support email or chat is connected (e.g., Intercom)
- [ ] Privacy Policy and Terms of Service mention all third-party services used
- [ ] GDPR/data processing compliance reviewed (if applicable)
- [ ] Load testing done (can the system handle 100 concurrent users?)

### Phase 4: General Availability (GA, Public Launch)

- [ ] 🔴 All integrations are live and battle-tested in production
- [ ] 🔴 Monitoring dashboards are live and tracked daily
- [ ] 🔴 On-call alerting is set up (e.g., PagerDuty or Slack alerts for downtime)
- [ ] 🔴 API key rotation schedule is documented and calendar reminders set
- [ ] 🔴 Incident response plan exists (who to call if Stripe/OpenAI goes down?)
- [ ] Backup and disaster recovery tested
- [ ] Integration cost projections updated for 500-user scale
- [ ] Runbook documented: how to disable or swap an integration if it fails

### Phase 5: First 500 Customers

- [ ] 🔴 All paid API tiers upgraded to match usage (no more free tier limits)
- [ ] 🔴 Database connection pooling is configured for scale
- [ ] 🔴 AI costs are within budget; per-user limits are effective
- [ ] 🔴 Zero P0/P1 (critical) integration bugs open
- [ ] Performance benchmarks: 95th percentile API response time < 500ms
- [ ] Customer-impacting integrations have SLA/uptime commitments reviewed
- [ ] Integration changelog is up to date (see Appendix)

---

## 14. 📎 Appendices

### A. Glossary

> 💡 *Defines any technical term used in this document. Add terms specific to your product here.*

| Term | Definition |
|------|-----------|
| **API** | Application Programming Interface — a way for two software systems to talk to each other over the internet |
| **Webhook** | A message that an external service sends to your app when something happens (e.g., Stripe tells you when a payment succeeds) |
| **JWT** | JSON Web Token — a secure, encoded string that proves a user is logged in |
| **OAuth** | An industry standard for "Sign in with Google/GitHub/Apple" — lets users log in without sharing their password |
| **Rate Limit** | A cap on how many API requests you can make in a given time period (e.g., 100 requests per minute) |
| **Exponential Backoff** | A retry strategy that waits longer after each failure: 1s → 2s → 4s → give up |
| **Environment Variable** | A configuration value stored outside your code, like a password — used so secrets aren't in your source code |
| **Mocking** | Replacing a real API call with a fake one during testing, so tests run fast and don't cost money |
| **Circuit Breaker** | A pattern that stops sending requests to a failing service until it recovers, preventing cascading failures |
| **Token (AI)** | The basic unit of text that AI models process — roughly 4 characters or ¾ of a word |
| **PII** | Personally Identifiable Information — data that can identify a specific person (e.g., name, email, phone number) |
| **SDK** | Software Development Kit — a library provided by a service (e.g., `stripe` npm package) to make integration easier |
| **CORS** | Cross-Origin Resource Sharing — a browser security rule that controls which domains can call your API |
| **Webhook Secret / Signing Secret** | A key used to verify that a webhook actually came from the claimed service, not a hacker |
| **Idempotency** | Processing the same request multiple times produces the same result — critical for payment webhooks to prevent double-charging |
| **[Add more]** | |

### B. Integration Change Log

> 💡 *Track every meaningful change to an integration — a version upgrade, a new endpoint added, a pricing change, a credential rotation. This log is invaluable when debugging "it used to work before X date."*

| Date | Integration | Change | Made By | Reason |
|------|-------------|--------|---------|--------|
| `[YYYY-MM-DD]` | `[e.g., OpenAI]` | `[e.g., Upgraded from gpt-3.5-turbo to gpt-4o-mini]` | `[Name]` | `[e.g., Better quality, similar cost]` |
| `[YYYY-MM-DD]` | `[e.g., Stripe]` | `[e.g., Rotated webhook secret after key was accidentally logged]` | `[Name]` | `[e.g., Security incident response]` |
| `[Add rows]` | | | | |

### C. Useful Tools & Resources

| Category | Tool / Link |
|----------|------------|
| **Secrets Management** | [Doppler](https://doppler.com) · [Infisical](https://infisical.com) · [1Password Secrets](https://1password.com/secrets) |
| **API Testing** | [Postman](https://postman.com) · [Insomnia](https://insomnia.rest) · [Hoppscotch](https://hoppscotch.io) |
| **Webhook Testing** | [Stripe CLI](https://stripe.com/docs/stripe-cli) · [ngrok](https://ngrok.com) · [Webhook.site](https://webhook.site) |
| **Error Monitoring** | [Sentry](https://sentry.io) · [LogRocket](https://logrocket.com) · [Datadog](https://datadoghq.com) |
| **Uptime Monitoring** | [Betterstack](https://betterstack.com) · [UptimeRobot](https://uptimerobot.com) |
| **AI Cost Tracking** | [OpenAI Usage Dashboard](https://platform.openai.com/usage) · [Helicone](https://helicone.ai) |
| **Load Testing** | [k6](https://k6.io) · [Artillery](https://artillery.io) |
| **Diagram Tool** | [Mermaid Live](https://mermaid.live) · [Excalidraw](https://excalidraw.com) |

### D. Integration Support Contacts

> 💡 *When an integration breaks at 2am, you need to know who to call. Fill this before launch.*

| Service | Support URL | Slack/Discord Community | Status Page |
|---------|------------|------------------------|-------------|
| `[e.g., Supabase]` | `https://supabase.com/support` | `https://discord.supabase.com` | `https://status.supabase.com` |
| `[e.g., OpenAI]` | `https://help.openai.com` | N/A | `https://status.openai.com` |
| `[e.g., Stripe]` | `https://support.stripe.com` | N/A | `https://status.stripe.com` |
| `[Add more]` | | | |

---

*End of Integration Specification Template*

---

> **📌 Reminder:** This document is a living artifact. Update it whenever an integration changes. An outdated spec is worse than no spec — set a calendar reminder to review this every month.

> **🔒 Security reminder:** This file may be committed to your git repository. It must NEVER contain actual secret values — only environment variable names. Real secrets live in your `.env` file (gitignored) and your deployment platform's environment variables.
