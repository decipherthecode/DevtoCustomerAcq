# 🛠️ Environment Configuration Template

> **Document Version:** 1.0.0
> **Last Updated:** <!-- 📅 Add today's date, e.g., 2026-10-15 -->
> **Template Version:** AIDLC-ENV-v1.0
> **Status:** <!-- 🔴 Draft | 🟡 In Review | 🟢 Approved | ⚫ Archived -->

---

# 📖 HOW TO FILL THIS DOCUMENT
## (Read this first — even if you're in a hurry!)

Welcome! This document is the **single source of truth** for how your project is configured across every environment — from your laptop to the live product your first 500 customers use. Think of it like a recipe card: fill in the blanks, and anyone on your team (or even you, six months from now!) can recreate the exact setup without guessing.

---

## ✅ Step-by-Step Filling Guide

**Step 1.** Read each section heading — it tells you what kind of information goes there.
**Step 2.** Replace every `<!-- ... -->` comment with your actual value. These are hints telling you what to type.
**Step 3.** Replace every `[PLACEHOLDER]` with the real name, URL, or value for your project.
**Step 4.** Do **NOT** commit real secrets (passwords, API keys, tokens) to Git. Write `[REDACTED]` or point to your secret manager instead.
**Step 5.** Work **top-to-bottom** on your first pass — sections build on each other.
**Step 6.** Mark any section **N/A** if it does not apply. Never delete sections — a future project on this template may need them.
**Step 7.** Ask your AI assistant if you are unsure about any field — every field has a description next to it.

---

## 🔑 Legend

| Symbol | Meaning |
|--------|---------|
| 🔴 | **Required** — must be filled before development starts |
| 🟡 | **Recommended** — fill before staging or QA begins |
| 🟢 | **Optional** — fill before production launch |
| 🔒 | **Secret** — never put the real value in this file or in Git |
| 💡 | **Tip** — a helpful hint for filling this field |
| ✅ | **Checkbox** — tick when the item is done |
| N/A | This section does not apply to this project |

---

## 📋 Fastest Fill Order

For a brand-new project, fill sections in this order:

```
1 → 2 → 3 → 7 → 8 → 11 → 4 → 5 → 6 → 9 → 10 → 12 → 13 → 14 → 15 → 16 → 17 → 18 → 19
```

---

# 1. 📋 PROJECT OVERVIEW
> 🔴 **Fill this first.** This gives everyone the context they need before opening any other section.

| Field | Value |
|-------|-------|
| **Project Name** | <!-- The full name of your product/app, e.g., "SmartBudget AI" --> |
| **Project Code / Slug** | <!-- Short lowercase ID with no spaces, e.g., "smartbudget-ai" — used in config file names and environment variable prefixes --> |
| **Current Version** | <!-- Semantic version of the codebase right now, e.g., "0.1.0" — bump this as you release --> |
| **Project Type** | <!-- e.g., Web App / Mobile App / REST API / CLI Tool / AI Agent / SaaS Platform --> |
| **Primary Language(s)** | <!-- e.g., Python 3.11, TypeScript 5.x --> |
| **Frameworks & Key Libraries** | <!-- e.g., FastAPI, Next.js 14, LangChain, Prisma --> |
| **Repository URL** | <!-- e.g., https://github.com/your-org/your-repo --> |
| **Project Manager / Owner** | <!-- Full name + email, e.g., Jane Smith — jane@yourcompany.com --> |
| **Lead Developer** | <!-- Full name + email --> |
| **AI / LLM Engineer** | <!-- Full name + email (can be the same person as lead developer) --> |
| **Target MVP Launch Date** | <!-- e.g., 2026-12-01 --> |
| **First 500 Customers Goal Date** | <!-- e.g., 2027-02-01 --> |

---

## 1.1 Project Description
> 💡 Write 2–3 sentences. Answer: what does it do, who is it for, and what is the core AI capability?

```
<!--
Example:
"SmartBudget AI is a personal finance web app that uses Claude AI to analyze
spending patterns and give personalized savings advice. It targets millennials
who find traditional budgeting apps too manual to maintain. The core AI feature
automatically categorizes bank transactions and generates a weekly financial
health report with actionable recommendations."
-->
```

---

## 1.2 Key Milestones

| Milestone | Target Date | Status |
|-----------|-------------|--------|
| Local dev environment ready | <!-- YYYY-MM-DD --> | <!-- 🔴 Not Started / 🟡 In Progress / 🟢 Done --> |
| Staging environment deployed | <!-- YYYY-MM-DD --> | <!-- --> |
| Beta launch (internal / invited users) | <!-- YYYY-MM-DD --> | <!-- --> |
| Public production launch | <!-- YYYY-MM-DD --> | <!-- --> |
| First 100 customers | <!-- YYYY-MM-DD --> | <!-- --> |
| First 500 customers | <!-- YYYY-MM-DD --> | <!-- --> |

---

# 2. 🌍 ENVIRONMENT OVERVIEW
> 🔴 **Fill this early.** This is your master map of all environments. Every team member should read it.

> 💡 An **environment** is a separate copy of your app set up for a specific purpose.
> Think of it like having a test kitchen (staging) before you open your real restaurant (production).

| Environment | Purpose | URL / Endpoint | Owner | Current Status |
|-------------|---------|----------------|-------|----------------|
| **Local** | Your laptop — where code is written and first tested | `http://localhost:[PORT]` | Each individual developer | Active |
| **Development** | Optional shared sandbox for the team | <!-- e.g., https://dev.yourapp.com --> | Lead Developer | <!-- 🔴 Not Set Up / 🟢 Active --> |
| **Staging / QA** | Final test run before customers see it | <!-- e.g., https://staging.yourapp.com --> | Dev Lead / QA | <!-- 🔴 Not Set Up / 🟢 Active --> |
| **Production** | What real customers use | <!-- e.g., https://yourapp.com --> | DevOps / Founder | <!-- 🔴 Not Set Up / 🟢 Active --> |

---

## 2.1 Git Branch → Environment Mapping

> 💡 This table tells your CI/CD pipeline which Git branch triggers a deploy to which environment.

| Git Branch | Deploys To | Auto-Deploy? | Approval Required? |
|-----------|------------|-------------|-------------------|
| `feature/*` | Local only (run manually) | No | No |
| `develop` | Development (shared) | <!-- Yes / No --> | <!-- No --> |
| `staging` | Staging / QA | <!-- Yes / No --> | <!-- Yes / No --> |
| `main` / `master` | Production | <!-- Yes, but gated --> | <!-- Yes — requires 2 approvals --> |

---

# 3. 💻 LOCAL DEVELOPMENT ENVIRONMENT
> 🔴 **Required for every developer.** Fill this so that any new team member can set up their laptop in under 30 minutes without asking anyone.

## 3.1 Prerequisites — Software to Install First

> 💡 List every tool someone needs installed BEFORE they can run the project. Be exact with version numbers so there are no compatibility surprises.

| Tool | Required Version | Where to Install |
|------|-----------------|-----------------|
| **Operating System** | <!-- e.g., macOS 14+, Windows 11, Ubuntu 22.04 LTS --> | — |
| **Node.js** | <!-- e.g., v20.x LTS --> | https://nodejs.org |
| **Python** | <!-- e.g., 3.11.x --> | https://python.org |
| **Docker Desktop** | <!-- e.g., v4.x+ --> | https://docker.com |
| **Git** | <!-- e.g., 2.40+ --> | https://git-scm.com |
| **Package Manager** | <!-- e.g., npm / yarn / pnpm / pip / uv --> | — |
| **IDE / Code Editor** | <!-- e.g., VS Code 1.90+ (recommended extensions listed in .vscode/extensions.json) --> | — |
| **Other tools** | <!-- e.g., Terraform CLI 1.9+, kubectl 1.30, Cloudflare CLI --> | — |

---

## 3.2 Local Setup Steps

> 💡 Number each step. A brand-new developer should be able to follow these with zero prior knowledge of this project.

```bash
# Step 1: Clone the repository
git clone [REPOSITORY_URL]
cd [PROJECT_SLUG]

# Step 2: Install dependencies
# <!-- e.g.:
#   npm install
#   OR: pip install -r requirements.txt
#   OR: uv sync
# -->

# Step 3: Copy the sample environment file and fill it in
cp .env.example .env
# Now open .env and fill in YOUR personal values (see Section 3.3 for each field explained)

# Step 4: Start supporting services (database, cache, etc.)
# <!-- e.g.: docker-compose up -d -->

# Step 5: Run database migrations
# <!-- e.g.:
#   npm run db:migrate
#   OR: alembic upgrade head
# -->

# Step 6: (Optional) Seed the database with test data
# <!-- e.g.: npm run db:seed -->

# Step 7: Start the application
# <!-- e.g.:
#   npm run dev
#   OR: python main.py
#   OR: uvicorn app.main:app --reload
# -->

# Step 8: Verify it is running — open your browser and go to:
# <!-- e.g., http://localhost:3000 -->
# You should see: <!-- describe the healthy start screen, e.g., "the login page with the app logo" -->
```

---

## 3.3 Local Environment Variables (.env file)

> 🔒 **NEVER commit your `.env` file to Git.** It is listed in `.gitignore` for this reason.
> 💡 This table explains every variable. The actual `.env.example` file in the repo has safe placeholder values that are safe to commit.

---

### 🏗️ App Core Settings

| Variable | Example Value | What It Does |
|----------|--------------|-------------|
| `APP_ENV` | `local` | Tells the app which environment it is in. Always `local` on your laptop. |
| `APP_PORT` | `3000` | The port your app listens on. Change it if 3000 is already used by something else. |
| `APP_DEBUG` | `true` | Shows detailed error messages and stack traces. Always `false` in production. |
| `APP_LOG_LEVEL` | `debug` | How detailed the logs are. `debug` = most detail; `error` = least detail. |
| `APP_SECRET_KEY` | `dev-secret-change-me` | 🔒 A random string used to encrypt sessions and cookies. Generate one with: `openssl rand -hex 32` |
| `APP_ALLOWED_ORIGINS` | `http://localhost:3000` | Which URLs are allowed to call your API (CORS). Comma-separate multiple values. |
| `BASE_URL` | `http://localhost:3000` | The full URL of your app in this environment. Used in emails, redirects, and webhooks. |

---

### 🤖 AI / LLM Settings

| Variable | Example Value | What It Does |
|----------|--------------|-------------|
| `ANTHROPIC_API_KEY` | `sk-ant-api03-...` | 🔒 Your personal Claude API key. Get it from: https://console.anthropic.com |
| `ANTHROPIC_MODEL` | `claude-haiku-4-5` | Which Claude model to use locally. Use a cheaper model for development. See Section 7.1.1. |
| `ANTHROPIC_MAX_TOKENS` | `4096` | Maximum tokens the AI can respond with per request. Higher = longer answers + more cost. |
| `ANTHROPIC_TEMPERATURE` | `0.7` | How creative the AI is: `0` = very predictable, `1` = very creative. |
| `ANTHROPIC_TIMEOUT_MS` | `30000` | How long (in milliseconds) to wait for a Claude response before giving up. 30000 = 30 seconds. |
| `AI_RATE_LIMIT_RPM` | `60` | Maximum AI requests your app can make per minute. Prevents runaway costs. |
| `AI_BUDGET_DAILY_USD` | `5.00` | 💡 Daily spending cap in US dollars. Your app will pause AI features if this is exceeded. |
| `AI_ENABLE_LOGGING` | `true` | Whether to log every AI request and response (useful for debugging locally). Set `false` in prod for privacy. |

---

### 🗄️ Database Settings

| Variable | Example Value | What It Does |
|----------|--------------|-------------|
| `DATABASE_URL` | `postgresql://user:pass@localhost:5432/myapp_local` | 🔒 Full connection string for your primary relational database (PostgreSQL). |
| `DATABASE_POOL_SIZE` | `5` | How many simultaneous database connections to keep open. 5 is fine for local development. |
| `DATABASE_SSL` | `false` | Whether to use SSL for the database connection. Always `true` in staging and production. |
| `MONGO_URI` | `mongodb://localhost:27017/myapp_local` | 🔒 MongoDB connection string (only fill if your project uses MongoDB). |
| `VECTOR_DB_PROVIDER` | `qdrant` | Which vector database you use: `qdrant` / `pinecone` / `weaviate` / `pgvector`. |
| `VECTOR_DB_URL` | `http://localhost:6333` | URL of your local vector database instance (started via Docker). |
| `VECTOR_DB_API_KEY` | `your-key-here` | 🔒 API key for cloud-hosted vector DBs (not needed for local Docker). |
| `VECTOR_DB_COLLECTION` | `myapp_local` | The name of the vector collection/index to use in this environment. |

---

### 💾 Cache & Queue Settings

| Variable | Example Value | What It Does |
|----------|--------------|-------------|
| `REDIS_URL` | `redis://localhost:6379` | 🔒 Connection string for Redis, used for caching and job queues. |
| `CACHE_TTL_SECONDS` | `300` | How long cached data lives before it expires. 300 = 5 minutes. |
| `QUEUE_PROVIDER` | `redis` | Which queue system to use: `redis` / `sqs` / `azure-service-bus` / `pubsub`. |

---

### 📦 File Storage Settings

| Variable | Example Value | What It Does |
|----------|--------------|-------------|
| `STORAGE_PROVIDER` | `local` | Where uploaded files are stored: `local` / `s3` / `azure-blob` / `gcs` / `r2`. |
| `STORAGE_LOCAL_PATH` | `./uploads` | Folder path for local file uploads. Only used when `STORAGE_PROVIDER=local`. |
| `AWS_S3_BUCKET` | `myapp-dev` | 🔒 AWS S3 bucket name (only if using S3). |
| `AWS_S3_REGION` | `us-east-1` | AWS region where your S3 bucket lives. |
| `AWS_ACCESS_KEY_ID` | `AKIA...` | 🔒 AWS access key. Prefer IAM roles in staging/prod instead of keys. |
| `AWS_SECRET_ACCESS_KEY` | `...` | 🔒 AWS secret access key. Keep this extremely private. |
| `CLOUDFLARE_R2_ENDPOINT` | `https://xxx.r2.cloudflarestorage.com` | 🔒 Cloudflare R2 endpoint (if using Cloudflare for storage). |

---

### 📧 Email & Notifications

| Variable | Example Value | What It Does |
|----------|--------------|-------------|
| `EMAIL_PROVIDER` | `smtp` | Which email service to use: `smtp` / `sendgrid` / `ses` / `resend` / `mailgun`. |
| `SMTP_HOST` | `localhost` | SMTP server address. Use `localhost` + MailHog for local testing (emails don't actually send). |
| `SMTP_PORT` | `1025` | SMTP port. 1025 is MailHog's default test port. |
| `SMTP_FROM_EMAIL` | `noreply@myapp.local` | The "From" address on all outbound emails. |
| `SMTP_USER` | `` | 🔒 SMTP username (leave blank for MailHog). |
| `SMTP_PASS` | `` | 🔒 SMTP password (leave blank for MailHog). |
| `SENDGRID_API_KEY` | `SG.xxx` | 🔒 SendGrid API key (only if using SendGrid). |

---

### 🔐 Authentication Settings

| Variable | Example Value | What It Does |
|----------|--------------|-------------|
| `JWT_SECRET` | `dev-jwt-secret-change-me` | 🔒 Secret string used to sign login tokens. Generate: `openssl rand -hex 32`. Rotate in prod. |
| `JWT_EXPIRES_IN` | `7d` | How long a login session lasts before the user must log in again. |
| `OAUTH_GOOGLE_CLIENT_ID` | `xxx.apps.googleusercontent.com` | 🔒 Google OAuth app client ID (only if using Google login). |
| `OAUTH_GOOGLE_CLIENT_SECRET` | `GOCSPX-xxx` | 🔒 Google OAuth app client secret. |
| `AUTH_CALLBACK_URL` | `http://localhost:3000/auth/callback` | The URL that OAuth providers redirect back to. Must exactly match what you set in the provider's dashboard. |

---

## 3.4 Local Docker Services (docker-compose)

> 💡 If your project uses `docker-compose` to run supporting services locally, document what each container does. Run all of them with: `docker-compose up -d`

```yaml
# docker-compose.yml — summary of local services
# (the actual file is in the root of the repository)

services:
  #
  # List each service here in this format:
  #   service-name:   short description — what it provides and what port it runs on
  #
  # Examples:
  #   db:        PostgreSQL 16 — main relational database (localhost:5432)
  #   redis:     Redis 7 — caching and background job queue (localhost:6379)
  #   qdrant:    Qdrant — vector database for AI embeddings (localhost:6333, UI at localhost:6334)
  #   mailhog:   MailHog — catches all outbound emails for local inspection (UI at localhost:8025)
```

---

# 4. 🧪 STAGING / QA ENVIRONMENT
> 🟡 **Fill before your first external test.** Staging must behave identically to production so that bugs caught here stay caught here.

## 4.1 Staging Overview

| Field | Value |
|-------|-------|
| **URL** | <!-- e.g., https://staging.yourapp.com --> |
| **Cloud Provider** | <!-- AWS / Azure / GCP / Cloudflare --> |
| **Region** | <!-- e.g., us-east-1, East US, europe-west1 --> |
| **Deploy Trigger** | <!-- e.g., Merge PR to `staging` branch → GitHub Actions auto-deploys --> |
| **Who Has Access** | <!-- e.g., Internal team only / Invited beta testers with magic link --> |
| **Data Source** | <!-- e.g., Anonymized copy of production data / Synthetic test data only --> |
| **Data Reset Schedule** | <!-- e.g., Resets to clean state every Monday 00:00 UTC / Never resets --> |

---

## 4.2 Staging-Specific Variables

> 💡 Only list variables that **differ** from production. Everything else should match prod exactly.

| Variable | Staging Value | Why It Differs |
|----------|--------------|---------------|
| `APP_ENV` | `staging` | Identifies the environment in logs and feature flags |
| `APP_DEBUG` | `false` | Matches production behaviour to catch prod-only bugs |
| `APP_LOG_LEVEL` | `info` | Less verbose than local; still captures useful events |
| `ANTHROPIC_MODEL` | <!-- e.g., claude-haiku-4-5 --> | Cheaper model to reduce testing costs |
| `AI_BUDGET_DAILY_USD` | <!-- e.g., 10.00 --> | Tighter cap for non-revenue environment |
| `DATABASE_URL` | 🔒 `[See Vault: staging/database_url]` | Separate staging database — never share with prod |
| `EMAIL_PROVIDER` | `sendgrid` with sandbox mode | Real emails only sent to allow-listed test addresses |
| `FEATURE_FLAGS_ENV` | `staging` | Allows staging-only feature flags to be enabled |

---

## 4.3 QA Test Accounts

> 💡 Pre-created accounts for testing all user journeys. Never use real user data.

| Role | Email | Password Location | Notes |
|------|-------|------------------|-------|
| Admin Tester | `qa-admin@yourapp.com` | 🔒 Vault: `staging/qa-admin-password` | Full admin permissions |
| Standard User | `qa-user@yourapp.com` | 🔒 Vault: `staging/qa-user-password` | Regular paid plan |
| Free Tier User | `qa-free@yourapp.com` | 🔒 Vault: `staging/qa-free-password` | Tests free plan limitations |

---

# 5. 🚀 PRODUCTION ENVIRONMENT
> 🟡 **Fill before public launch.** This is what real customers use. Every field here matters.

## 5.1 Production Overview

| Field | Value |
|-------|-------|
| **Primary URL** | <!-- e.g., https://yourapp.com --> |
| **API Base URL** | <!-- e.g., https://api.yourapp.com --> |
| **CDN URL** | <!-- e.g., https://cdn.yourapp.com --> |
| **Status Page** | <!-- e.g., https://status.yourapp.com --> |
| **Cloud Provider(s)** | <!-- AWS / Azure / GCP / Cloudflare (or combination) --> |
| **Primary Region** | <!-- e.g., us-east-1 --> |
| **Failover Region** | <!-- e.g., us-west-2 — only needed for high availability setups --> |
| **Deploy Trigger** | <!-- e.g., Manual approval required, then merge to `main` --> |
| **Rollback Strategy** | <!-- e.g., Re-deploy previous GitHub release tag via GitHub Actions "Rollback" workflow --> |
| **Maintenance Window** | <!-- e.g., Sundays 02:00–04:00 UTC — communicate to users beforehand --> |

---

## 5.2 Production Infrastructure

> 💡 Document what you are actually running. This is your single source of truth during an incident.

### Compute

| Service | Provider | Specification | Instance Count | Auto-Scales? |
|---------|----------|--------------|---------------|-------------|
| App Server | <!-- e.g., AWS ECS, Azure App Service, Vercel, Railway --> | <!-- e.g., 2 vCPU / 4 GB RAM --> | <!-- e.g., 2 --> | <!-- Yes / No --> |
| Background Workers | <!-- e.g., ECS Fargate, Lambda --> | <!-- --> | <!-- --> | <!-- --> |
| AI Agent Runner | <!-- e.g., ECS Fargate, Google Cloud Run --> | <!-- --> | <!-- --> | <!-- --> |

### Networking

| Resource | Value |
|----------|-------|
| **Domain Registrar** | <!-- e.g., Cloudflare, Namecheap, Route 53, Google Domains --> |
| **DNS Provider** | <!-- e.g., Cloudflare, Route 53, Azure DNS --> |
| **SSL/TLS Certificate** | <!-- e.g., Cloudflare auto-managed / Let's Encrypt via Certbot / AWS ACM --> |
| **Load Balancer** | <!-- e.g., AWS ALB, Cloudflare, Azure Front Door, Nginx --> |
| **DDoS Protection** | <!-- e.g., Cloudflare Pro, AWS Shield Standard --> |
| **WAF (Web Application Firewall)** | <!-- e.g., Cloudflare WAF, AWS WAF with OWASP rule set --> |

---

## 5.3 Production Variables — Location Reference

> 🔒 **All production secret values live in your secret manager (HashiCorp Vault), NOT in this file.**
> 💡 Only document the variable NAME and WHERE its value lives. Never write the actual value here.

| Variable | Where the Value Lives | Rotation Frequency |
|----------|-----------------------|--------------------|
| `APP_ENV` | `production` (hardcoded in deploy config) | Never |
| `APP_SECRET_KEY` | 🔒 Vault: `prod/app_secret_key` | Every 90 days |
| `ANTHROPIC_API_KEY` | 🔒 Vault: `prod/anthropic_api_key` | Quarterly |
| `DATABASE_URL` | 🔒 Vault: `prod/database_url` | When password changes |
| `REDIS_URL` | 🔒 Vault: `prod/redis_url` | When password changes |
| `JWT_SECRET` | 🔒 Vault: `prod/jwt_secret` | Every 30 days |
| `SENDGRID_API_KEY` | 🔒 Vault: `prod/sendgrid_api_key` | Annually |
| <!-- Add all prod secrets --> | | |

---

# 6. 🏗️ CLOUD INFRASTRUCTURE
> 🟡 **Fill before staging deployment.**

## 6.1 Multi-Cloud Service Map

> 💡 Which cloud provider handles which part of your infrastructure?

| Cloud Provider | Services Used in This Project | Account ID / Project ID |
|---------------|-------------------------------|------------------------|
| **AWS** | <!-- e.g., S3 (file storage), SES (email), CloudFront (CDN), RDS (database) --> | <!-- AWS Account ID: 123456789012 --> |
| **Azure** | <!-- e.g., Azure AD B2C (auth), Azure Monitor (logs), Azure OpenAI (fallback LLM) --> | <!-- Subscription ID: xxx-xxx --> |
| **GCP** | <!-- e.g., Firestore (NoSQL), BigQuery (analytics), GCS (backup storage) --> | <!-- Project ID: myapp-prod --> |
| **Cloudflare** | <!-- e.g., DNS, CDN, WAF, R2 (object storage), Pages (frontend hosting), Workers (edge functions) --> | <!-- Zone ID: xxx / Account ID: xxx --> |

---

## 6.2 Infrastructure as Code (IaC)

| Field | Value |
|-------|-------|
| **IaC Tool** | <!-- e.g., Terraform, Pulumi, AWS CDK, Azure Bicep, CloudFormation --> |
| **IaC Files Location** | <!-- e.g., `/infra` folder in this repo / separate repo: https://github.com/org/infra --> |
| **State Backend** | <!-- e.g., Terraform Cloud / AWS S3 bucket `myapp-tf-state` + DynamoDB lock table --> |
| **How to Apply Changes** | <!-- e.g., Open PR → CI runs `terraform plan` → team reviews plan → manual `terraform apply` after approval --> |
| **Who Can Apply to Prod?** | <!-- e.g., DevOps engineer or founder only --> |

---

# 7. 🤖 AI & LLM CONFIGURATION
> 🔴 **Core section for this project.** Fill this carefully — it controls the behaviour, cost, and safety of every AI feature.

## 7.1 Primary LLM Provider: Anthropic Claude

| Field | Local | Staging | Production |
|-------|-------|---------|-----------|
| **API Key Location** | 🔒 `.env` file | 🔒 Vault: `staging/anthropic_api_key` | 🔒 Vault: `prod/anthropic_api_key` |
| **Model Used** | <!-- claude-haiku-4-5 --> | <!-- claude-haiku-4-5 --> | <!-- claude-opus-4-5 or claude-sonnet-4-5 --> |
| **Max Response Tokens** | `4096` | `2048` | <!-- match your longest expected output --> |
| **Temperature** | `0.7` | `0.5` | <!-- tune per feature: 0.2 for factual, 0.8 for creative --> |
| **Daily Cost Budget (USD)** | `$5.00` | `$10.00` | <!-- Set after measuring avg cost per user --> |
| **Rate Limit (requests/min)** | `60` | `100` | <!-- Check your Anthropic plan tier limits --> |
| **API Base URL** | `https://api.anthropic.com` | same | same |
| **API Version** | <!-- e.g., 2023-06-01 --> | same | same |

---

### 7.1.1 Claude Model Selection Guide

> 💡 Use this table to pick the right model for each feature in your app. The right choice saves real money.

| Model | Best Used For | Relative Cost | Speed |
|-------|--------------|--------------|-------|
| `claude-opus-4-5` | Complex reasoning, long documents, high-stakes decisions, multi-step agent tasks | 💰💰💰 | Slower |
| `claude-sonnet-4-5` | Balanced everyday tasks — the recommended default for most features | 💰💰 | Medium |
| `claude-haiku-4-5` | High-volume simple tasks, quick classifications, testing, development | 💰 | Fastest |

---

### 7.1.2 Fallback Strategy — What Happens If Claude API Is Down?

| Scenario | Fallback Action |
|---------|----------------|
| Rate limit reached (429 error) | Queue the request; retry with exponential backoff (1s → 2s → 4s → 8s); alert if queue > 100 |
| Request timeout (> 30s) | Return cached response if available; otherwise show user-friendly error message |
| API outage (5xx errors for > 2 min) | Switch to secondary LLM (see Section 7.2) OR disable AI feature and show maintenance message |
| Daily budget cap hit | Pause AI features for that day; send alert to engineering team Slack channel |

---

## 7.2 Secondary / Fallback LLM (Optional but Recommended)

> 💡 A backup AI provider gives you resilience. Fill this in if you want zero-downtime AI features.

| Field | Value |
|-------|-------|
| **Provider** | <!-- e.g., OpenAI, Azure OpenAI, Ollama (self-hosted), Mistral API --> |
| **Model** | <!-- e.g., gpt-4o-mini, llama-3.1-70b, mistral-small --> |
| **Trigger Condition** | <!-- e.g., Anthropic API returns error 529 (overloaded) OR latency > 15s for 3 consecutive requests --> |
| **API Key Location** | 🔒 <!-- Vault: prod/fallback_llm_api_key --> |
| **Limitations vs. Claude** | <!-- e.g., Smaller context window, different output format — describe any prompt adjustments needed --> |

---

## 7.3 Token Budget Management

> 💡 "Tokens" are the units the AI reads and writes — roughly 1 token ≈ 0.75 words. More tokens = higher cost. Budget them carefully!

| Setting | Value | Explanation |
|---------|-------|-------------|
| **Input Token Limit (per request)** | <!-- e.g., 100,000 --> | Maximum tokens you will send TO the AI in a single request (includes conversation history + context). |
| **Output Token Limit (per request)** | <!-- e.g., 4,096 --> | Maximum tokens you allow Claude to respond with. |
| **Context Window Strategy** | <!-- e.g., Sliding window: keep last 20 messages / Summarize old messages when context > 50k tokens --> | How to handle very long conversations without hitting limits. |
| **Daily Token Budget (total, all users)** | <!-- e.g., 10,000,000 tokens/day --> | Soft cap across your entire user base for the day. |
| **Per-User Daily Token Limit (free tier)** | <!-- e.g., 50,000 tokens/day --> | Prevents a single user from consuming your entire budget. |
| **Per-User Daily Token Limit (paid tier)** | <!-- e.g., 500,000 tokens/day --> | Higher limit for paying customers. |
| **Token Cost Alert Threshold** | <!-- e.g., Alert team when daily spend reaches $80 (80% of $100 budget) --> | When to send a cost alert before the cap is hit. |

---

## 7.4 Embedding Configuration (for RAG and Semantic Search)

> 💡 **RAG = Retrieval-Augmented Generation.** This is how you make Claude answer questions using YOUR own data (documents, knowledge base, product catalogue, etc.).
> Without RAG, Claude only knows what it was trained on. With RAG, it can search your content first, then answer using it.

| Field | Value |
|-------|-------|
| **Embedding Model** | <!-- e.g., text-embedding-3-small (OpenAI), voyage-3 (Voyage AI), cohere-embed-v3 --> |
| **Embedding Dimensions** | <!-- e.g., 1536 for text-embedding-3-small --> |
| **Embedding API Key Location** | 🔒 <!-- Vault: prod/embedding_api_key --> |
| **Vector Database Provider** | <!-- Qdrant / Pinecone / Weaviate / pgvector / Chroma --> |
| **Index / Collection Name (prod)** | <!-- e.g., myapp_prod_knowledge_base --> |
| **Similarity Metric** | <!-- cosine (most common) / dot product / euclidean --> |
| **Top-K Results to Retrieve** | <!-- e.g., 5 — how many document chunks to fetch and pass to Claude --> |
| **Chunk Size (tokens)** | <!-- e.g., 512 tokens per document chunk --> |
| **Chunk Overlap (tokens)** | <!-- e.g., 50 tokens overlap between consecutive chunks --> |
| **Re-ranking Model** | <!-- e.g., Cohere Rerank / None --> |

---

# 8. 🧠 AI AGENT ORCHESTRATION
> 🔴 **Fill this if your product includes AI agents** — software that takes actions autonomously (e.g., searches the web, reads a database, sends messages, writes files).

## 8.1 Agent Architecture Overview

| Field | Value |
|-------|-------|
| **Orchestration Framework** | <!-- e.g., LangChain, LangGraph, AutoGen, CrewAI, Anthropic Tool Use (native), Custom --> |
| **Agent Pattern** | <!-- e.g., ReAct (reason + act loops), Tool-calling, Supervisor-worker multi-agent, Plan-and-execute --> |
| **Number of Agents** | <!-- e.g., 3 agents: Planner, Executor, Reviewer --> |
| **Max Agent Iterations** | <!-- e.g., 10 — agent is force-stopped after this many steps to prevent infinite loops --> |
| **Agent Execution Timeout** | <!-- e.g., 120 seconds — max wall-clock time for a single agent run --> |
| **Human-in-the-Loop** | <!-- Yes — e.g., agent pauses and asks for approval before sending emails / No — fully autonomous --> |
| **Agent Memory Strategy** | <!-- e.g., Short-term: conversation buffer / Long-term: vector store / No memory --> |

---

## 8.2 Agent Registry

> 💡 Document each AI agent like a team member profile. Copy this block for each additional agent.

---

### Agent: [AGENT_NAME]

> 💡 Give your agent a clear, descriptive name. Example: `transaction-categorizer`, `support-responder`, `report-generator`.

| Field | Value |
|-------|-------|
| **Agent ID** | <!-- e.g., `research-agent-v1` — use lowercase with hyphens, add version --> |
| **Purpose** | <!-- Plain English: what does this agent do? e.g., "Searches the web for competitor pricing and summarizes findings" --> |
| **Trigger** | <!-- What starts this agent? e.g., "User clicks 'Generate Report'" / "Cron job runs daily at 06:00 UTC" / "Webhook from Stripe payment event" --> |
| **LLM Model** | <!-- Which Claude model? e.g., claude-opus-4-5 for complex reasoning tasks --> |
| **Max Tokens per Run** | <!-- e.g., 20,000 --> |
| **Tools Available** | <!-- List every tool this agent can call. See Section 8.3. --> |
| **Output Format** | <!-- e.g., JSON object with fields: {summary, actions_taken, confidence_score} --> |
| **Output Destination** | <!-- e.g., Saved to database table `agent_reports` / Sent to user via email / Shown in dashboard --> |
| **Error Behaviour** | <!-- What happens if the agent fails? e.g., Retry up to 3 times, then alert user and log to Sentry --> |
| **Audit Log** | <!-- Every action logged to: e.g., database table `agent_audit_log` with timestamp, input, output, cost --> |

---

### Agent: [SECOND_AGENT_NAME]
> 💡 Copy and fill this block for each additional agent.

| Field | Value |
|-------|-------|
| **Agent ID** | <!-- --> |
| **Purpose** | <!-- --> |
| **Trigger** | <!-- --> |
| **LLM Model** | <!-- --> |
| **Max Tokens per Run** | <!-- --> |
| **Tools Available** | <!-- --> |
| **Output Format** | <!-- --> |
| **Output Destination** | <!-- --> |
| **Error Behaviour** | <!-- --> |
| **Audit Log** | <!-- --> |

---

## 8.3 Tool Registry — What the AI Agents Can Do

> 💡 A "tool" is an action an AI agent can call to interact with the outside world. List every tool so the team knows what the AI has access to.

| Tool Name | What It Does | Auth Method | Rate Limit | Safe to Use in Prod? |
|-----------|-------------|------------|-----------|---------------------|
| <!-- `web_search` --> | <!-- Searches the internet for current information --> | <!-- API key (Serper / Brave / Tavily) --> | <!-- 10 calls/min --> | <!-- ✅ Yes --> |
| <!-- `database_read` --> | <!-- Reads records from the app database (read-only) --> | <!-- Read-only DB credentials --> | <!-- 100 calls/min --> | <!-- ✅ Yes --> |
| <!-- `database_write` --> | <!-- Creates or updates records in the database --> | <!-- DB credentials --> | <!-- 50 calls/min --> | <!-- ⚠️ Requires approval rule --> |
| <!-- `send_email` --> | <!-- Sends an email to a user or address --> | <!-- SendGrid API key --> | <!-- 5 calls/min --> | <!-- ⚠️ Requires human-in-loop approval --> |
| <!-- `file_reader` --> | <!-- Reads the content of a file (PDF, DOCX, etc.) --> | <!-- Internal service key --> | <!-- 20 calls/min --> | <!-- ✅ Yes --> |
| <!-- `code_executor` --> | <!-- Runs Python code in an isolated sandbox --> | <!-- Sandbox service auth --> | <!-- 5 calls/min --> | <!-- ⚠️ Sandboxed environment only --> |
| <!-- `calendar_create` --> | <!-- Creates a calendar event --> | <!-- OAuth token --> | <!-- 10 calls/min --> | <!-- ⚠️ Requires human-in-loop approval --> |
| <!-- Add more tools --> | | | | |

---

## 8.4 Agent Safety & Guardrails

> 🔴 **Critical section.** Define what your AI is NOT allowed to do, and how you stop it from causing harm.

| Guardrail | Enabled? | How It Works |
|-----------|----------|-------------|
| **Content output filter** | <!-- Yes / No --> | <!-- e.g., All AI responses run through Llama Guard or custom classifier to block harmful content before showing to user --> |
| **Action blocklist (hard rules)** | <!-- Yes / No --> | <!-- e.g., Agent can NEVER delete database records / NEVER send emails without user confirmation / NEVER access external URLs outside allow-list --> |
| **Daily cost circuit breaker** | <!-- Yes / No --> | <!-- e.g., Agent runs pause automatically if daily AI spend exceeds $X --> |
| **Infinite loop / max-step limit** | <!-- Yes / No --> | <!-- e.g., Hard limit of 10 iterations; agent throws controlled error and logs on iteration 11 --> |
| **PII detection and redaction** | <!-- Yes / No --> | <!-- e.g., User inputs scanned for SSN, email, phone patterns before sending to LLM — found values replaced with [REDACTED] --> |
| **Prompt injection detection** | <!-- Yes / No --> | <!-- e.g., Input scanned for injection patterns like "ignore previous instructions"; suspicious inputs rejected and flagged --> |
| **Full audit trail** | <!-- Yes / No --> | <!-- e.g., Every agent action recorded in `agent_audit_log` table: timestamp, user_id, tool_called, input, output, token_count, cost_usd --> |
| **Rollback / undo capability** | <!-- Yes / No --> | <!-- e.g., All agent write actions create a reversible record — admin can undo last N actions --> |

---

# 9. 📝 PROMPT VERSIONING & MANAGEMENT
> 🟡 **Fill before staging.** Prompts change just like code — track them so you can roll back when something breaks.

## 9.1 Prompt Storage Strategy

| Field | Value |
|-------|-------|
| **Where prompts are stored** | <!-- e.g., `/prompts` folder in Git repo / PostgreSQL `prompts` table / Anthropic Console / LangSmith / Braintrust --> |
| **Versioning approach** | <!-- e.g., Semantic versioning (v1.0.0) tied to Git tags / Auto-incremented database row ID / Environment-specific prompt IDs --> |
| **Who can edit prompts?** | <!-- e.g., Any developer via PR / Only the AI engineer / Requires 2-person PR review for prod prompts --> |
| **Promotion process** | <!-- e.g., local → pass unit eval → staging → pass full eval suite → prod --> |
| **A/B testing prompts?** | <!-- Yes — e.g., 50/50 split in staging, measure quality score before promoting winner / No --> |

---

## 9.2 Prompt Registry

> 💡 Document every important system prompt and its current version in each environment.

| Prompt ID | Purpose | Local Version | Staging Version | Prod Version |
|-----------|---------|--------------|----------------|-------------|
| `system-prompt-main` | Core AI persona, tone, and rules | <!-- v1.2.0 --> | <!-- v1.1.0 --> | <!-- v1.1.0 --> |
| `rag-context-injector` | How to use retrieved document context | <!-- v1.0.0 --> | <!-- v1.0.0 --> | <!-- v1.0.0 --> |
| `onboarding-welcome` | First message to new users | <!-- v0.3.0 --> | <!-- v0.2.0 --> | <!-- v0.2.0 --> |
| `error-recovery` | What the AI says when it cannot complete a task | <!-- v1.0.0 --> | <!-- v1.0.0 --> | <!-- v1.0.0 --> |
| <!-- Add more --> | | | | |

---

## 9.3 Prompt Evaluation

| Field | Value |
|-------|-------|
| **Evaluation Tool** | <!-- e.g., LangSmith, Braintrust, PromptFoo, custom Python scripts --> |
| **Eval Dataset Location** | <!-- e.g., `/tests/prompt-evals/` in this repo --> |
| **Eval Runs When?** | <!-- e.g., In CI on every change to `/prompts` folder / Before every staging deploy --> |
| **Key Metrics** | <!-- e.g., Accuracy %, Hallucination rate %, Latency (p95), Cost per prompt run --> |
| **Minimum Pass Threshold for Prod Promotion** | <!-- e.g., >90% accuracy on eval dataset, 0 hallucinations on factual questions --> |

---

# 10. 🗄️ DATABASE CONFIGURATION
> 🔴 **Fill before any data is written.**

## 10.1 Primary Relational Database

| Field | Local | Staging | Production |
|-------|-------|---------|-----------|
| **Engine** | <!-- PostgreSQL --> | <!-- PostgreSQL --> | <!-- PostgreSQL --> |
| **Version** | <!-- 16.x --> | <!-- 16.x --> | <!-- 16.x --> |
| **Host** | `localhost` | 🔒 Vault: `staging/db_host` | 🔒 Vault: `prod/db_host` |
| **Port** | `5432` | `5432` | `5432` |
| **Database Name** | `[project]_local` | `[project]_staging` | `[project]_prod` |
| **SSL Mode** | `disable` | `require` | `require` |
| **Connection Pool Size** | `5` | `20` | <!-- tune based on max concurrent requests --> |
| **Migration Tool** | <!-- e.g., Prisma Migrate, Alembic, Flyway, Liquibase --> | same | same |
| **Migration Run When?** | Manual: `npm run db:migrate` | Auto on deploy | Manual with approval required |

---

## 10.2 NoSQL Database (if used)

| Field | Local | Staging | Production |
|-------|-------|---------|-----------|
| **Engine** | <!-- e.g., MongoDB / Firestore --> | same | same |
| **Version** | <!-- e.g., 7.x --> | same | same |
| **Connection / URI** | `mongodb://localhost:27017/[project]_local` | 🔒 Vault: `staging/mongo_uri` | 🔒 Vault: `prod/mongo_uri` |
| **Database Name** | `[project]_local` | `[project]_staging` | `[project]_prod` |

---

## 10.3 Vector Database (for AI / RAG)

| Field | Local | Staging | Production |
|-------|-------|---------|-----------|
| **Provider** | <!-- Qdrant (Docker) --> | <!-- Qdrant Cloud / Pinecone --> | <!-- Pinecone / Weaviate Cloud --> |
| **URL / Endpoint** | `http://localhost:6333` | 🔒 Vault: `staging/vector_db_url` | 🔒 Vault: `prod/vector_db_url` |
| **API Key** | N/A (local Docker) | 🔒 Vault: `staging/vector_db_key` | 🔒 Vault: `prod/vector_db_key` |
| **Collection Name** | `[project]_local` | `[project]_staging` | `[project]_prod` |
| **Dimensions** | <!-- e.g., 1536 --> | same | same |

---

## 10.4 Cache (Redis)

| Field | Local | Staging | Production |
|-------|-------|---------|-----------|
| **Provider** | Local Redis (Docker) | <!-- Redis Cloud / ElastiCache --> | <!-- Redis Cloud / ElastiCache --> |
| **URL** | `redis://localhost:6379` | 🔒 Vault: `staging/redis_url` | 🔒 Vault: `prod/redis_url` |
| **Default TTL** | `300` seconds | `300` seconds | <!-- tune per use case --> |
| **Max Memory Policy** | `allkeys-lru` | `allkeys-lru` | `allkeys-lru` |

---

## 10.5 Database Backup Policy

| Field | Value |
|-------|-------|
| **Backup Frequency** | <!-- e.g., Daily automated backup at 03:00 UTC + manual snapshot before every release --> |
| **Backup Retention Period** | <!-- e.g., 30 days rolling retention --> |
| **Backup Storage Location** | <!-- e.g., AWS S3 bucket: myapp-prod-backups (versioned, encrypted) --> |
| **Restore Procedure** | <!-- e.g., See runbook: /docs/runbooks/database-restore.md --> |
| **Restore Last Tested** | <!-- Date: YYYY-MM-DD / Not yet tested --> |
| **RTO — Recovery Time Objective** | <!-- e.g., < 4 hours — maximum acceptable time to restore service --> |
| **RPO — Recovery Point Objective** | <!-- e.g., < 1 hour — maximum acceptable data loss window --> |

---

# 11. 🔐 SECRETS MANAGEMENT
> 🔴 **Critical. A single leaked API key can cause significant financial damage and data breaches.**

## 11.1 Secrets Strategy by Environment

> 💡 This table shows WHERE secrets live in each environment and WHO can access them.

| Environment | Storage Method | Access Control |
|------------|---------------|---------------|
| **Local** | `.env` file on developer's machine (never committed to Git) | Individual developer only |
| **CI/CD (GitHub Actions)** | GitHub Actions Secrets (encrypted at rest) | Repo admins only |
| **Staging** | HashiCorp Vault — `staging/` namespace | Development team |
| **Production** | HashiCorp Vault — `prod/` namespace | DevOps + founders only (MFA required) |

---

## 11.2 GitHub Actions Secrets

> 💡 Set these in: GitHub Repo → Settings → Secrets and Variables → Actions → New repository secret

| Secret Name | What It Is | Rotation Schedule |
|------------|------------|------------------|
| `ANTHROPIC_API_KEY_STAGING` | Claude API key used during staging deploys | Quarterly |
| `ANTHROPIC_API_KEY_PROD` | Claude API key used during production deploys | Quarterly |
| `DATABASE_URL_STAGING` | Full staging database connection string | When password changes |
| `DATABASE_URL_PROD` | Full production database connection string | When password changes |
| `VAULT_TOKEN_STAGING` | HashiCorp Vault token for staging secrets access | Monthly |
| `VAULT_TOKEN_PROD` | HashiCorp Vault token for production secrets access | Monthly |
| `DOCKER_REGISTRY_TOKEN` | Token to push Docker images to container registry | Annually |
| <!-- Add more as needed --> | | |

---

## 11.3 Secret Rotation Schedule

> 💡 Schedule a recurring calendar event for each rotation. Do not let these expire without rotating.

| Secret | Rotation Frequency | Last Rotated | Next Due Date | Responsible Person |
|--------|------------------|-------------|--------------|-------------------|
| `APP_SECRET_KEY` (prod) | Every 90 days | <!-- YYYY-MM-DD --> | <!-- YYYY-MM-DD --> | <!-- name --> |
| `JWT_SECRET` (prod) | Every 30 days | <!-- YYYY-MM-DD --> | <!-- YYYY-MM-DD --> | <!-- name --> |
| `ANTHROPIC_API_KEY` (prod) | Quarterly | <!-- YYYY-MM-DD --> | <!-- YYYY-MM-DD --> | <!-- name --> |
| `DATABASE_URL` (prod) | On-demand (when password changes) | <!-- YYYY-MM-DD --> | On-demand | <!-- name --> |
| `VAULT_TOKEN` | Monthly | <!-- YYYY-MM-DD --> | <!-- YYYY-MM-DD --> | <!-- name --> |

---

## 11.4 The Never-Commit List

> 🔴 **Check this list before every Git commit and every pull request.**

Things that must NEVER appear in any Git commit, PR, or code review:

- ❌ API keys of any kind (Anthropic, OpenAI, AWS, Stripe, etc.)
- ❌ Database passwords or full connection strings
- ❌ JWT secrets or session secrets
- ❌ OAuth client secrets
- ❌ Your actual `.env` file (only `.env.example` with fake placeholder values)
- ❌ SSL/TLS private keys or certificate files
- ❌ HashiCorp Vault tokens
- ❌ Docker registry credentials
- ❌ SSH private keys

> 💡 **Automate this check:** Add `trufflehog` or `git-secrets` as a pre-commit hook so your tools catch leaks before they reach GitHub.

---

# 12. ⚙️ CI/CD PIPELINE
> 🟡 **Fill before staging deployment.**

## 12.1 Pipeline Overview

| Field | Value |
|-------|-------|
| **CI/CD Platform** | GitHub Actions |
| **Workflow Files Location** | `.github/workflows/` in this repository |
| **Container Registry** | <!-- e.g., GitHub Container Registry (ghcr.io) / AWS ECR / Docker Hub --> |
| **Deployment Tool** | <!-- e.g., Helm + kubectl / Terraform / Serverless Framework / Railway CLI / Vercel CLI --> |
| **Notification Channel** | <!-- e.g., Slack #deployments channel / Email to engineering@yourapp.com --> |

---

## 12.2 Workflow Files

| File | Trigger | Purpose |
|------|---------|---------|
| `ci.yml` | Every push and every PR | Run tests, linting, type-checking, security scans |
| `deploy-staging.yml` | Merge to `staging` branch | Build Docker image → push → deploy to staging |
| `deploy-prod.yml` | Manual trigger only, after `main` merge | Deploy to production with approval gate |
| `prompt-eval.yml` | Any change inside `/prompts/` folder | Run the full AI prompt evaluation suite |
| `security-scan.yml` | Weekly on schedule + every PR | Scan dependencies and code for vulnerabilities |
| `backup-verify.yml` | Weekly on schedule | Verify database backup is restorable |

---

## 12.3 Quality Gates — Must All Pass Before Any Deploy

> 🔴 **All gates in the "Required" column must pass before code can be deployed to staging or production.**

| Check | Tool | Required? | Pass Threshold |
|-------|------|-----------|---------------|
| Unit tests | <!-- Jest / Pytest / Vitest --> | 🔴 Yes | All tests pass |
| Integration tests | <!-- Playwright / Supertest / Pytest --> | 🔴 Yes | All tests pass |
| Code coverage | <!-- Istanbul / Coverage.py --> | 🟡 Recommended | > 80% lines covered |
| Linting | <!-- ESLint / Ruff / Pylint --> | 🔴 Yes | 0 errors |
| Type checking | <!-- TypeScript / mypy --> | 🟡 Recommended | 0 type errors |
| Dependency vulnerability scan | <!-- Snyk / Trivy / Dependabot --> | 🔴 Yes | 0 critical or high severity CVEs |
| Secret scan | <!-- trufflehog / git-secrets --> | 🔴 Yes | 0 secrets detected |
| AI prompt eval suite | <!-- LangSmith / PromptFoo / custom --> | 🟡 Recommended | > 90% accuracy on eval dataset |
| Docker image build | Docker | 🔴 Yes | Build succeeds with 0 errors |

---

## 12.4 Rollback Procedure

> 💡 Write this so that anyone — even someone who has never done it before — can roll back a bad deploy in under 15 minutes. Practice this during staging!

```
Step 1 — DETECT: How to know a rollback is needed
         e.g., Sentry error rate > 1%, or Datadog shows API success rate < 99%,
               or users report critical functionality broken.

Step 2 — DECIDE: Who calls the rollback
         e.g., On-call engineer or CTO makes the decision.
               Post "🚨 Rollback initiated — [reason]" in #incidents Slack channel.

Step 3 — EXECUTE: How to roll back
         e.g., Go to GitHub → Actions → "Deploy Production" → find last successful run
               → click "Re-run all jobs" on the previous successful deploy.
         OR: Trigger a new deploy with the previous Git release tag:
               git checkout v1.4.2 && git push origin main --force-with-lease

Step 4 — VERIFY: How to confirm the rollback worked
         e.g., Hit the /health endpoint → check status: 200 OK
               Monitor Sentry for 5 minutes → error rate drops back to baseline.

Step 5 — COMMUNICATE: Notify affected users and team
         e.g., Post update in #incidents: "✅ Rollback complete. Service restored."
               Update status page at https://status.yourapp.com
               If users were affected > 5 minutes: send in-app notification.
```

---

# 13. 📊 OBSERVABILITY & MONITORING
> 🟡 **Fill before staging.** 🔴 **Required before production launch.**

## 13.1 Logging Strategy

| Field | Value |
|-------|-------|
| **Log Format** | <!-- JSON structured logging (recommended — easily searchable) / Plain text --> |
| **Log Aggregation Tool** | <!-- Datadog Log Management / Grafana Loki / CloudWatch Logs / Azure Monitor --> |
| **Log Retention (Production)** | <!-- e.g., 90 days (SOC 2 requires minimum 1 year for access logs) --> |
| **Log Retention (Staging)** | <!-- e.g., 14 days --> |
| **PII in Logs?** | <!-- No — all PII redacted before logging (email, name, phone replaced with [REDACTED]) --> |
| **Log Sampling (high-traffic endpoints)** | <!-- e.g., Log 100% of errors, 10% of successful requests for /api/chat --> |

### Log Level Guide

| Level | When to Use It | Example Message |
|-------|---------------|----------------|
| `DEBUG` | Detailed dev info — local only, never in prod | `"Processing chunk 42 of 100"` |
| `INFO` | Normal business events worth recording | `"User signed up"`, `"AI report generated"` |
| `WARN` | Something unexpected but the app keeps running | `"AI rate limit at 80%"`, `"Slow DB query: 1.2s"` |
| `ERROR` | Something failed and needs attention | `"Payment failed: Stripe 402"`, `"AI API timeout"` |
| `FATAL` | App cannot continue; restart required | `"Database connection pool exhausted"` |

---

## 13.2 Key Metrics & Alert Thresholds

> 💡 Set alerts in Datadog or Grafana for each of these. The "Alert Threshold" column is the value that wakes someone up.

| Metric | Monitoring Tool | Alert Threshold | Who Gets Alerted |
|--------|----------------|----------------|-----------------|
| API response time (p95) | <!-- Datadog / Grafana --> | <!-- > 2,000 ms --> | <!-- Engineering on-call --> |
| API error rate (5xx) | <!-- Datadog --> | <!-- > 1% over 5-minute window --> | <!-- Engineering on-call --> |
| AI API response time (p95) | <!-- Datadog --> | <!-- > 5,000 ms --> | <!-- AI engineer --> |
| AI daily cost spend | <!-- Custom metric → Datadog --> | <!-- > 80% of daily budget --> | <!-- Engineering lead --> |
| AI token usage rate | <!-- Custom metric --> | <!-- > 80% of daily token limit --> | <!-- AI engineer --> |
| Database query time (p99) | <!-- Datadog / Grafana --> | <!-- > 500 ms --> | <!-- Engineering on-call --> |
| Database connection pool usage | <!-- Datadog --> | <!-- > 80% of pool size --> | <!-- Engineering on-call --> |
| Disk usage | <!-- Datadog / Grafana --> | <!-- > 80% full --> | <!-- DevOps --> |
| Memory usage | <!-- Datadog / Grafana --> | <!-- > 85% of allocated RAM --> | <!-- DevOps --> |

---

## 13.3 Error Tracking (Sentry)

| Field | Local | Staging | Production |
|-------|-------|---------|-----------|
| **Sentry DSN** | Not used (or personal test DSN) | 🔒 Vault: `staging/sentry_dsn` | 🔒 Vault: `prod/sentry_dsn` |
| **Sample Rate** | N/A | `1.0` (100% of errors) | `1.0` (100% of errors) |
| **Alert email** | — | <!-- e.g., engineering@yourapp.com --> | <!-- e.g., oncall@yourapp.com --> |
| **Ignored error patterns** | — | <!-- e.g., 404 on /favicon.ico --> | <!-- e.g., Known bot traffic 404s --> |

---

## 13.4 Uptime Monitoring

| Field | Value |
|-------|-------|
| **Tool** | <!-- e.g., Better Uptime, Checkly, UptimeRobot, Datadog Synthetics --> |
| **Health Check Endpoint** | <!-- e.g., https://yourapp.com/health → returns {status: "ok", version: "1.2.0"} --> |
| **Check Frequency** | <!-- e.g., Every 60 seconds from 3 global regions --> |
| **Alert Contact** | <!-- e.g., PagerDuty → on-call engineer / SMS to founder's phone --> |
| **Escalation (no response in 10 min)** | <!-- e.g., Page secondary on-call / Call CTO --> |
| **Public Status Page URL** | <!-- e.g., https://status.yourapp.com --> |

---

## 13.5 AI-Specific Observability

> 💡 These metrics are unique to AI-powered products. Standard APM tools will not capture them by default — you may need custom code to track them.

| Metric | How It Is Tracked | Alert Threshold |
|--------|------------------|----------------|
| LLM response quality score | <!-- e.g., LangSmith auto-evaluation after each response --> | <!-- < 0.80 average (5-min window) --> |
| Hallucination rate | <!-- e.g., Custom fact-checking tool on every AI response --> | <!-- > 5% of responses flagged --> |
| Prompt injection attempts | <!-- e.g., Custom input guard logs flagged inputs --> | <!-- Any detected → immediate alert --> |
| RAG retrieval precision | <!-- e.g., LangSmith / custom eval on sampled queries --> | <!-- < 85% precision on eval set --> |
| Agent task success rate | <!-- e.g., Custom metric: completed/total agent runs --> | <!-- < 90% success rate --> |
| AI cost per active user per day | <!-- e.g., Custom metric: daily_ai_spend / daily_active_users --> | <!-- > $1.00 per user per day --> |
| Context window utilization | <!-- e.g., Log token count per request --> | <!-- > 80% of context limit on avg --> |

---

# 14. 🔒 SECURITY & COMPLIANCE
> 🔴 **Review this section carefully if your product handles any personal or financial data.**

## 14.1 Authentication & Authorization

| Field | Value |
|-------|-------|
| **Authentication Method** | <!-- e.g., JWT + refresh token rotation / Session cookies / API keys for B2B / OAuth 2.0 --> |
| **Identity Provider** | <!-- e.g., Auth0, Clerk, Supabase Auth, AWS Cognito, Firebase Auth, Custom --> |
| **MFA (Multi-Factor Authentication)** | <!-- Required for all admin accounts / Optional for regular users / Not implemented yet --> |
| **Password Policy** | <!-- e.g., Min 12 characters, 1 uppercase, 1 number, 1 symbol / Managed by identity provider --> |
| **Session Timeout** | <!-- e.g., Auto-logout after 7 days of inactivity --> |
| **Role-Based Access Control (RBAC)** | <!-- Yes — roles: [admin, editor, viewer, api-consumer] / No --> |

---

## 14.2 Data Privacy (GDPR & HIPAA)

| Requirement | Implemented? | How / Where |
|-------------|-------------|------------|
| User data export (portability) | <!-- ✅ Yes / 🚧 In Progress / ❌ Not yet --> | <!-- e.g., "Download my data" button in Account Settings → downloads JSON file --> |
| User data deletion (right to erasure) | <!-- ✅ / 🚧 / ❌ --> | <!-- e.g., Support request via email → 30-day deletion schedule → confirmation email --> |
| Consent recorded for data processing | <!-- ✅ / 🚧 / ❌ --> | <!-- e.g., T&C checkbox on signup; acceptance stored with timestamp in `users.consent_date` --> |
| PII encrypted at rest | <!-- ✅ / 🚧 / ❌ --> | <!-- e.g., AES-256 on database-level for columns: email, name, address --> |
| PII encrypted in transit | <!-- ✅ / 🚧 / ❌ --> | <!-- HTTPS everywhere; TLS 1.2 minimum; enforced by Cloudflare --> |
| Data residency requirement | <!-- e.g., EU-only storage required / US-only / No restriction --> | <!-- e.g., All data stored in eu-west-1 (Ireland) / us-east-1 --> |
| Anthropic AI training opt-out | <!-- ✅ Confirmed (Anthropic does not train on API data by default) --> | <!-- Confirm via Anthropic's privacy policy and your API usage agreement --> |
| Data breach notification procedure | <!-- ✅ / ❌ --> | <!-- e.g., Notify affected users within 72 hours per GDPR — see /docs/incident-response.md --> |

---

## 14.3 API Security Controls

| Control | Implemented? | Implementation Detail |
|---------|-------------|----------------------|
| Rate limiting | <!-- ✅ / ❌ --> | <!-- e.g., 100 API requests/minute per authenticated user via Redis rate limiter --> |
| Input validation | <!-- ✅ / ❌ --> | <!-- e.g., Zod schemas on all request bodies / Pydantic models on all FastAPI endpoints --> |
| SQL injection protection | <!-- ✅ / ❌ --> | <!-- e.g., Prisma ORM with parameterized queries — no raw SQL in application code --> |
| Prompt injection protection | <!-- ✅ / ❌ --> | <!-- e.g., User input sanitized and wrapped in XML tags before inserting into prompts --> |
| CORS policy | <!-- ✅ / ❌ --> | <!-- e.g., Only domains listed in APP_ALLOWED_ORIGINS can call the API --> |
| Security headers | <!-- ✅ / ❌ --> | <!-- e.g., Helmet.js on Node / Django security middleware / Cloudflare security headers rule --> |
| Dependency vulnerability scanning | <!-- ✅ / ❌ --> | <!-- e.g., Dependabot + Snyk on every PR; block merge if critical CVEs found --> |

---

## 14.4 Compliance Checklist

### SOC 2
- [ ] Access logs retained for minimum 1 year
- [ ] MFA enabled for all admin and privileged accounts
- [ ] Vendor security assessments documented for key third parties (Anthropic, cloud providers)
- [ ] Written incident response plan exists
- [ ] Annual security review date scheduled

### GDPR
- [ ] Privacy policy written, reviewed by lawyer, and published on website
- [ ] Cookie consent banner implemented (granular opt-in/opt-out)
- [ ] Data Processing Agreement (DPA) with Anthropic reviewed and accepted
- [ ] Right to erasure (delete account + data) implemented and tested
- [ ] Right to export (download all my data) implemented and tested
- [ ] Data breach notification procedure documented and rehearsed

### ISO 27001
- [ ] Information security policy document written and approved
- [ ] Risk register created and reviewed quarterly
- [ ] IT asset inventory maintained and up to date
- [ ] Annual security training completed by all team members

---

# 15. 🚩 FEATURE FLAGS
> 🟢 **Optional but strongly recommended** for safe launches and gradual rollouts to your first 500 customers.

> 💡 A feature flag is a on/off switch for a feature that you can flip without deploying new code.
> Use them to: release features gradually (10% → 50% → 100%), A/B test, or kill a broken feature instantly.

| Flag Name | Purpose | Local | Staging | Production (current) |
|-----------|---------|-------|---------|---------------------|
| `ai_assistant_enabled` | Main AI chat feature | `true` | `true` | `false` → flip to `true` on launch day |
| `rag_search_enabled` | AI-powered document search | `true` | `true` | Roll out: 10% → 25% → 50% → 100% |
| `agent_mode_enabled` | Autonomous AI agent feature | `true` | `false` | `false` — coming in v2.0 |
| `new_dashboard_ui` | Redesigned dashboard layout | `true` | `true` | A/B test: 50% see new, 50% see old |
| `export_to_pdf` | Export reports as PDF | `true` | `false` | `false` — pending QA |
| <!-- Add your flags --> | | | | |

| Field | Value |
|-------|-------|
| **Feature Flag Tool** | <!-- e.g., LaunchDarkly / PostHog flags / GrowthBook / Flagsmith / Simple env variables --> |
| **Flag Management Dashboard** | <!-- URL of the flag management UI --> |
| **Emergency Kill Switch Process** | <!-- e.g., Go to LaunchDarkly → toggle `ai_assistant_enabled` to OFF → takes effect in < 1 minute --> |

---

# 16. 🚨 INCIDENT RESPONSE
> 🟡 **Fill this before production.** You do not want to figure this out for the first time during a live outage.

## 16.1 Severity Levels

| Level | What It Means | Response Time Target | Example |
|-------|--------------|---------------------|---------|
| 🔴 **P0 — Critical** | Complete outage; all users affected | Page on-call in < 15 minutes | Database down, app returns 500 to all users |
| 🟠 **P1 — High** | Core feature broken for all users | Respond in < 1 hour | AI chat not responding, payments failing |
| 🟡 **P2 — Medium** | Feature broken for some users | Respond in < 4 hours | Slow response times, export failing for some |
| 🟢 **P3 — Low** | Minor cosmetic or edge-case issue | Fix in next sprint | Button text incorrect, minor UI misalignment |

---

## 16.2 On-Call & Escalation

| Role | Name | Contact | When to Escalate |
|------|------|---------|-----------------|
| Primary On-Call Engineer | <!-- name --> | <!-- phone / Slack handle --> | 15 min no response → escalate |
| Secondary On-Call Engineer | <!-- name --> | <!-- phone / Slack handle --> | — |
| Engineering Lead / CTO | <!-- name --> | <!-- phone --> | All P0 incidents, always |
| Product Owner / CEO | <!-- name --> | <!-- phone --> | P0 + P1 incidents |
| AI/LLM Specialist | <!-- name --> | <!-- phone --> | Any AI-related P0 or P1 |

---

## 16.3 AI-Specific Incident Playbooks

| Incident Type | How It Is Detected | Immediate Response |
|--------------|-------------------|-------------------|
| AI generating harmful/inappropriate content | Sentry alert + content filter flag | Immediately flip `ai_assistant_enabled` flag to `false`; investigate and fix before re-enabling |
| Prompt injection attack detected | Security alert from input guard | Block the user account; log full request for forensic analysis; notify security team |
| AI cost spike (> 2× daily average) | Budget alert from Datadog | Pause AI features via feature flag; investigate which endpoint is driving usage |
| AI response quality drops (score < 0.8) | LangSmith / eval alert | Roll back to previous prompt version; run full eval suite on current version |
| Anthropic API outage | Uptime monitor + API error rate > 5% | Auto-switch to fallback LLM (Section 7.2) OR disable AI and show: "AI features temporarily unavailable" |
| User reports AI gave factually wrong answer | User support ticket | Log the query and response; flag for prompt eval review; respond to user within 24h |

---

# 17. 🚀 LAUNCH READINESS: FIRST 500 CUSTOMERS
> 🔴 **Complete every item on this checklist before going live.** Do not skip items — each one has caught a real production incident.

## 17.1 Pre-Launch Checklist

### 🏗️ Infrastructure
- [ ] All production environment variables set, reviewed, and verified with a test request
- [ ] SSL certificate installed, valid, and auto-renewal confirmed
- [ ] Domain DNS configured and fully propagated (verify at dnschecker.org)
- [ ] CDN enabled, tested, and cache-purge process documented
- [ ] Auto-scaling policy configured and tested (simulate 10× normal traffic)
- [ ] Database backup tested: backup taken AND successfully restored to a test instance
- [ ] Redis / cache configured and connected in production

### 🤖 AI & LLM
- [ ] Production Anthropic API key activated and end-to-end tested
- [ ] AI rate limits and daily cost budgets set and tested (simulate hitting the limit)
- [ ] Fallback LLM strategy tested (simulated Anthropic API outage)
- [ ] All AI guardrails and content filters active and tested
- [ ] Prompt evaluation suite passes > 90% threshold on production prompt versions
- [ ] PII redaction tested — confirmed user data is stripped before sending to LLM
- [ ] Per-user token budget enforced and tested for both free and paid tiers
- [ ] AI cost alerting configured and alert tested (manually trigger threshold)

### 🔐 Security
- [ ] All secrets rotated to unique production values (not the same as staging)
- [ ] `.env.example` reviewed by a second person — confirmed no real secrets
- [ ] Security headers score: A or A+ on securityheaders.com
- [ ] CORS restricted to production domain(s) only
- [ ] Rate limiting active and tested on all public API endpoints
- [ ] Dependency scan: 0 critical or high CVEs
- [ ] Secret scan (trufflehog) on entire repository history: 0 secrets found
- [ ] At least one security review or pen test completed

### 📊 Observability
- [ ] Sentry configured in production and receiving a test event
- [ ] Datadog or Grafana dashboards live and displaying real data
- [ ] Uptime monitor active and alert tested (manually take down service, verify alert fires)
- [ ] Log aggregation working and logs appearing in Datadog/Loki
- [ ] AI-specific metrics dashboard live (token usage, cost, quality score)
- [ ] On-call rotation scheduled and all team members have been paged at least once in staging

### 🧪 Testing
- [ ] All unit tests passing on `main` branch
- [ ] All integration and E2E tests passing on `main` branch
- [ ] Load test completed — confirmed system handles target concurrent users (e.g., 500 simultaneously)
- [ ] Staging fully signed off by the team (or founder) after manual testing
- [ ] Happy path tested end-to-end by at least one person with no technical background

### 📋 Business & Legal
- [ ] Privacy policy written, reviewed, and published on website
- [ ] Terms of service written, reviewed, and published on website
- [ ] Cookie consent banner live and saving preferences correctly
- [ ] Payment integration end-to-end tested with real card in production
- [ ] Welcome / onboarding email sending correctly from production domain
- [ ] Email domain SPF, DKIM, and DMARC records configured (check at mail-tester.com)
- [ ] Support contact channel ready (email, live chat, or helpdesk)
- [ ] Public status page live and linked from the website footer

---

## 17.2 Post-Launch Monitoring Schedule

| Timeframe | Monitoring Actions |
|-----------|-------------------|
| **Day 1** | Check Sentry/Datadog every 30 minutes; watch AI cost in real time; read every support message within 1 hour |
| **Days 2–7** | Daily review: new signups, error rate, AI quality score, support ticket themes |
| **Week 2** | First cost analysis: actual AI spend per user vs. budget estimate — adjust tier limits if needed |
| **Week 3** | First prompt quality review: are eval scores holding? Any new failure patterns? |
| **Month 1** | Full system review + capacity planning: can current infra handle 5× current users? |
| **Reaching 500 customers** | Security review, cost renegotiation with Anthropic if needed, performance audit |

---

## 17.3 Capacity Estimate for 500 Customers

> 💡 Fill this in before launch so you know what to expect on your bill and when to upgrade infrastructure.

| Resource | Estimated Usage / Day at 500 Customers | Current Capacity | Action Required? |
|----------|----------------------------------------|-----------------|-----------------|
| AI tokens (total) | <!-- e.g., 25,000,000 tokens/day --> | <!-- e.g., Anthropic plan limit: 50M/day --> | <!-- No / Upgrade plan --> |
| Database storage | <!-- e.g., 50 GB --> | <!-- e.g., 100 GB allocated --> | <!-- No --> |
| Compute (CPU / RAM avg) | <!-- e.g., 4 vCPU, 8 GB RAM --> | <!-- current spec --> | <!-- --> |
| File storage (uploads) | <!-- e.g., 200 GB total --> | <!-- --> | <!-- --> |
| Outbound emails | <!-- e.g., 5,000 / day --> | <!-- plan limit --> | <!-- --> |
| Estimated total monthly cloud bill | <!-- e.g., $800 / month --> | — | — |
| Estimated Anthropic API monthly cost | <!-- e.g., $300 / month --> | — | — |

---

# 18. 📚 THIRD-PARTY SERVICES & INTEGRATIONS
> 🟡 **Document every external service your product depends on.** This is your vendor inventory.

| Service | Purpose | Account / Login Email | Dashboard URL | Status Page |
|---------|---------|----------------------|--------------|------------|
| **Anthropic** | Primary LLM — Claude API | <!-- --> | https://console.anthropic.com | https://anthropic.com/status |
| <!-- Stripe / Paddle --> | <!-- Payments --> | <!-- --> | <!-- --> | <!-- --> |
| <!-- SendGrid / Resend --> | <!-- Transactional email --> | <!-- --> | <!-- --> | <!-- --> |
| <!-- Cloudflare --> | <!-- DNS, CDN, WAF, R2 Storage --> | <!-- --> | https://dash.cloudflare.com | https://www.cloudflarestatus.com |
| <!-- GitHub --> | <!-- Code hosting, CI/CD --> | <!-- --> | https://github.com | https://githubstatus.com |
| <!-- Datadog --> | <!-- Application monitoring, alerts --> | <!-- --> | https://app.datadoghq.com | https://status.datadoghq.com |
| <!-- Sentry --> | <!-- Error tracking --> | <!-- --> | https://sentry.io | https://status.sentry.io |
| <!-- Grafana Cloud --> | <!-- Metrics and dashboards --> | <!-- --> | <!-- --> | <!-- --> |
| <!-- HashiCorp Vault --> | <!-- Secrets management --> | <!-- --> | <!-- Self-hosted URL or HCP URL --> | <!-- --> |
| <!-- Auth0 / Clerk --> | <!-- Authentication --> | <!-- --> | <!-- --> | <!-- --> |
| <!-- Pinecone / Qdrant Cloud --> | <!-- Vector database for AI --> | <!-- --> | <!-- --> | <!-- --> |
| <!-- Add more rows --> | | | | |

---

# 19. 📜 DOCUMENT HISTORY
> 💡 Track every meaningful change to this document. This is your audit trail — required for SOC 2.

| Version | Date | Author | Summary of Changes |
|---------|------|--------|--------------------|
| 1.0.0 | <!-- YYYY-MM-DD --> | <!-- Name --> | Initial document created |
| <!-- 1.1.0 --> | <!-- --> | <!-- --> | <!-- e.g., Added vector DB config for RAG feature --> |
| <!-- --> | <!-- --> | <!-- --> | <!-- --> |

---

# ✅ DOCUMENT SIGN-OFF

> 💡 Before changing the document Status from "Draft" to "Approved" (at the top of this file), get a review signature from each of these roles.

| Role | Name | Date Reviewed | Approved? |
|------|------|--------------|-----------|
| Lead Developer | <!-- --> | <!-- YYYY-MM-DD --> | <!-- ✅ Yes / 🔴 Changes Requested --> |
| DevOps / Infrastructure | <!-- --> | <!-- YYYY-MM-DD --> | <!-- ✅ Yes / 🔴 Changes Requested --> |
| Security Reviewer | <!-- --> | <!-- YYYY-MM-DD --> | <!-- ✅ Yes / 🔴 Changes Requested --> |
| Product Owner | <!-- --> | <!-- YYYY-MM-DD --> | <!-- ✅ Yes / 🔴 Changes Requested --> |

---

> 📌 **This document is a living artifact.**
> Update it every time an environment changes, a new service is added, or a secret is rotated.
> A stale configuration document is more dangerous than having none — it gives your team false confidence.
>
> *Template: AIDLC-ENV-v1.0 | Generated: 2026-10-15 | Framework: AI-Driven Development Life Cycle*
