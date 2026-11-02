# Dependency Register — Project Nova
### `Dependency_Register_ProjectNova.md` — AI-Driven Development Life Cycle
**Template Version:** 1.0 | **Last Updated:** 2026-10-14 | **Project:** Project Nova

> ⚠️ **This is a filled example file.** It shows you how a real team would complete the blank template (`Dependency_Register.md`). Replace every value with your own project's real data.

---

## 📋 Project & Register Info

| Field | Your Answer |
|---|---|
| **Project Name** | Project Nova |
| **Product Description** | An AI-powered personal assistant available as a web app (Next.js / Vercel) and native mobile apps (iOS + Android via React Native) that helps users manage tasks, draft content, and get answers — powered by Anthropic Claude API. |
| **Project Start Date** | 2026-10-14 |
| **Target Launch Date** | 2027-03-01 |
| **First 500 Users Target Date** | 2027-04-30 |
| **Register Owner (Primary Maintainer)** | Alex Rivera — Product Manager |
| **Register Created Date** | 2026-10-14 |
| **Last Reviewed Date** | 2026-10-14 |
| **Review Cadence** | Every Monday at 10 AM in sprint standup |
| **AI Stack Summary** | LLM: Anthropic Claude API (claude-sonnet-4-5) · Auth + DB: Supabase + PostgreSQL · Hosting: Vercel (web) + AWS (backend APIs + media storage) |
| **Hosting / Infra** | Vercel (Next.js web app) · AWS us-east-1 (Node.js API server, S3 for assets) · Supabase (PostgreSQL DB, Auth, Realtime) · React Native + Expo (iOS + Android) |
| **Regulatory / Compliance Context** | GDPR applicable (EU users) · CCPA applicable (US users) · App Store / Play Store review required for mobile · No medical/financial data — general consumer use |

---

## 📊 Health Dashboard — At-a-Glance Status

> ℹ️ **Example data shown below. Update these numbers every Monday.**

### Overall Counts

| Metric | Count |
|---|---|
| 📦 Total Dependencies Logged | 24 |
| ⚪ Not Started | 11 |
| 🔵 In Progress | 5 |
| 🟢 Resolved | 3 |
| 🔴 Blocked | 4 |
| ⚫ Cancelled | 1 |
| 🚨 Overdue (past Due Date, not Resolved) | 0 |

### By Risk Level

| Risk | Count | IDs |
|---|---|---|
| 🔴 High | 10 | DEP-001, DEP-010, DEP-011, DEP-020, DEP-021, DEP-031, DEP-053, DEP-060, DEP-070, DEP-100 |
| 🟠 Medium | 9 | DEP-002, DEP-030, DEP-032, DEP-041, DEP-052, DEP-061, DEP-071, DEP-091, DEP-111 |
| 🟡 Low | 5 | DEP-033, DEP-092, DEP-102, DEP-110, DEP-112 |

### By Phase

| Phase | Total | Resolved | Open | Blocked |
|---|---|---|---|---|
| Phase 1 — Discovery & Scoping | 6 | 1 | 3 | 2 |
| Phase 2 — Development & Integration | 9 | 2 | 5 | 2 |
| Phase 3 — QA / Testing & Security | 5 | 0 | 4 | 1 |
| Phase 4 — Launch & Post-Launch | 4 | 0 | 3 | 1 |

### By Type

| Type | Count |
|---|---|
| 🔧 Technical | 12 |
| 🤖 Data & AI Model | 7 |
| 📋 Business / Compliance | 5 |

### 🚨 Active Blockers (High-Risk / Unresolved)

| DEP-ID | Name | Owner | Due Date | Impact if Not Resolved |
|---|---|---|---|---|
| DEP-020 | GDPR / CCPA Legal Review | Sarah Park — Legal | 2026-11-01 | Cannot use any real user data with Claude API; cannot onboard EU/US users |
| DEP-021 | Anthropic Data Processing Agreement | Sarah Park — Legal | 2026-11-08 | Cannot process real user prompts through Claude API legally |
| DEP-031 | Apple Developer Account Approved | Jordan Lee — Mobile Lead | 2026-11-15 | iOS app cannot be submitted to App Store |
| DEP-011 | Supabase Production Project Provisioned | Marcus Chen — DevOps | 2026-10-28 | No production database; blocks all backend API development |

---

## 📦 Phase 1 — Discovery & Scoping

### 🔧 Phase 1 — Technical Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-001 | Development Environment Setup | Technical | N/A | All 6 engineers need Node.js v20+, Python 3.11, Docker, Expo CLI, and Android Studio installed and configured before any coding begins. Without a consistent environment, bugs that only appear on one machine will waste hours. | Internal | Marcus Chen — DevOps | 🟢 Resolved | 🔴 High | 2026-10-14 | 2026-10-18 | 2026-10-17 | — | Use GitHub Codespaces as fallback if local setup fails for any team member. | [2026-10-17] All 6 developers confirmed setup complete. Android emulator working on Windows and Mac. Expo Go confirmed on iOS and Android test devices. ✅ |
| DEP-002 | AWS Account + IAM Roles Configured | Technical | N/A | A shared AWS account with correct IAM roles for developers, CI/CD pipeline, and production services must be configured before any backend infrastructure is provisioned. Wrong IAM setup causes security risks and deployment failures. | Cloud Provider | Marcus Chen — DevOps | 🔵 In Progress | 🟠 Medium | 2026-10-14 | 2026-10-21 | — | — | Use Vercel for all hosting temporarily; defer AWS-specific services (S3, Lambda) until account is ready. | [2026-10-14] Account created. IAM role definitions drafted. [2026-10-17] Waiting on finance team to attach payment method and raise service limits. |

---

### 🤖 Phase 1 — Data & AI Model Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-010 | Anthropic Claude API — Proof of Concept | Data & AI Model | LLM | We must validate that Claude API (claude-sonnet-4-5) meets our quality, latency, and cost requirements for the core AI assistant feature during scoping. A 2-day technical spike is planned. Output: go/no-go decision on model selection. | External Vendor | Priya Nair — AI Lead | 🟢 Resolved | 🔴 High | 2026-10-14 | 2026-10-21 | 2026-10-20 | — | If Claude API fails requirements, evaluate OpenAI GPT-4o and Google Gemini 1.5 Pro as alternatives in the same spike. | [2026-10-20] Spike complete. Claude Sonnet 4.5 selected. Avg latency: 1.2s for 500-token response. Cost per 1K requests estimated at $0.43. Quality score: 4.4/5 on 30 test prompts. Decision: APPROVED. ✅ |

---

### 📋 Phase 1 — Business / Compliance Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-020 | GDPR / CCPA Legal Review | Business / Compliance | N/A | Legal must confirm exactly what user data can be stored in Supabase, what can be sent to Anthropic's Claude API, and what disclosures must be shown to EU and US users. This is the single most critical blocker — it gates dataset use, DPA signing, and user onboarding. | Internal Legal / External GDPR Counsel | Sarah Park — Legal | 🔴 Blocked | 🔴 High | 2026-10-14 | 2026-11-01 | — | — | Use only synthetic (fake) user data and engineer-owned test accounts during development until legal review is complete. | [2026-10-14] Engaged external GDPR counsel. Questionnaire sent. [2026-10-20] Counsel requests Anthropic's sub-processor list and DPA template — requested from Anthropic. |
| DEP-021 | Anthropic Data Processing Agreement (DPA) | Business / Compliance | N/A | A signed DPA with Anthropic is required before any real user-generated content (prompts, tasks, notes) can be processed through the Claude API. Anthropic provides DPAs on all API plans — must be formally signed and filed. | External Vendor | Sarah Park — Legal | 🔴 Blocked | 🔴 High | 2026-10-14 | 2026-11-08 | — | DEP-020 | Use synthetic prompts only in development. Do not onboard any paying or real users until DPA is signed. | [2026-10-14] Anthropic DPA template downloaded from docs.anthropic.com. Sent to legal for review. Blocked on DEP-020 completing first. |
| DEP-022 | Project Budget Approved | Business / Compliance | N/A | Finance sign-off required on total 6-month project budget: $18K cloud/API costs + $24K tooling + $6K contractor costs. Required before any paid contracts or subscriptions are activated. | Internal | Alex Rivera — PM | 🟢 Resolved | 🔴 High | 2026-10-14 | 2026-10-18 | 2026-10-16 | — | Start with existing team discretionary budget ($2K) for PoC costs only while awaiting formal approval. | [2026-10-16] Board approved $52K total project budget. PO numbers issued. Finance confirmed AWS and Anthropic vendor accounts can be opened. ✅ |

---

## 🔧 Phase 2 — Development & Integration

### 🔧 Phase 2 — Technical Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-011 | Supabase Production Project Provisioned | Technical | N/A | A production-grade Supabase project (PostgreSQL DB + Auth + Realtime + Storage) must be created with correct region (eu-west-1 for GDPR), row-level security enabled, and connection pooling configured before any backend API dev begins. | Cloud Provider | Marcus Chen — DevOps | 🔴 Blocked | 🔴 High | 2026-10-14 | 2026-10-28 | — | DEP-020 | Use a temporary Supabase free-tier project in any region for local development only. No real user data stored here. | [2026-10-14] Supabase account created. Waiting on GDPR legal review to confirm EU region requirement before provisioning production project. |
| DEP-030 | Anthropic Claude API Key — Team Shared | Technical | N/A | A team shared Anthropic API key with sufficient rate limits for 6 concurrent developers must be set up and stored securely in the project's secret manager (AWS Secrets Manager). Each developer must NOT use personal API keys in the shared codebase. | External Vendor | Priya Nair — AI Lead | 🔵 In Progress | 🟠 Medium | 2026-10-14 | 2026-10-25 | — | DEP-021 | Each developer uses their own personal Anthropic API key in local .env file (never committed to Git) until team key is provisioned. | [2026-10-20] Team API key created in Anthropic console. Pending DPA sign-off before storing in AWS Secrets Manager. Rate limit: 100K tokens/min (Tier 3). |
| DEP-031 | Apple Developer Account Approved | Technical | N/A | An Apple Developer Program account ($99/year) must be approved before any iOS build can be submitted to TestFlight or the App Store. Approval can take 2–7 business days and requires a valid D-U-N-S number for business accounts. | External Vendor | Jordan Lee — Mobile Lead | 🔴 Blocked | 🔴 High | 2026-10-14 | 2026-11-15 | — | DEP-022 | Develop and test exclusively on Android (Google Play has faster review) while Apple account is pending. Prioritise iOS submission once approved. | [2026-10-14] Applied for Apple Developer account. D-U-N-S number submitted. [2026-10-20] Status: "Under Review". Estimated 5 more business days. |
| DEP-032 | Google Play Developer Account Approved | Technical | N/A | A Google Play Developer account ($25 one-time fee) must be created and verified before any Android app can be submitted for review. Verification typically takes 2–3 business days. | External Vendor | Jordan Lee — Mobile Lead | 🔵 In Progress | 🟠 Medium | 2026-10-14 | 2026-10-28 | — | DEP-022 | Use internal Expo Go app for Android testing during the approval window. | [2026-10-14] Account created, payment made. [2026-10-17] Identity verification email sent. Awaiting confirmation. |
| DEP-033 | Expo EAS Build + Submission Configured | Technical | N/A | Expo Application Services (EAS) must be configured for automated iOS and Android builds and store submissions before mobile CI/CD can run. This includes App Store Connect and Google Play API keys stored in EAS secrets. | External Vendor | Jordan Lee — Mobile Lead | ⚪ Not Started | 🟡 Low | 2026-10-14 | 2026-11-20 | — | DEP-031 | Use local `eas build` with manual upload until automated submission is configured. | — |
| DEP-034 | Database Schema Frozen (v1) | Technical | N/A | The core Supabase/PostgreSQL schema (users, sessions, ai_messages, user_preferences, billing) must be agreed, reviewed, and frozen before backend API development begins. Schema migrations mid-sprint cause merge conflicts and data loss risk. | Internal | Marcus Chen — DevOps | ⚪ Not Started | 🔴 High | 2026-10-14 | 2026-11-01 | — | DEP-011 | Use a flexible JSONB metadata column in all tables as an escape hatch during early development until schema is final. | [2026-10-14] Draft schema doc shared in Notion. Team review scheduled for 2026-10-28. |

---

### 🤖 Phase 2 — Data & AI Model Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-050 | Claude System Prompt v1 — Approved | Data & AI Model | LLM | The core system prompt that defines Nova's AI assistant persona, tone, guardrails, and response format must be written, tested, and signed off by Product + Legal before any feature is built on top of it. Changes after this point require a new approval cycle. | Internal | Priya Nair — AI Lead + Alex Rivera — PM | 🔵 In Progress | 🔴 High | 2026-10-14 | 2026-11-01 | — | DEP-010 | Use a placeholder system prompt ("You are Nova, a helpful personal assistant. Be concise and friendly.") so frontend development can proceed while the final prompt is drafted. | [2026-10-20] First draft written by Priya. 3 persona options being A/B tested on synthetic prompts. Legal review of prompt guardrails scheduled for 2026-10-28. |
| DEP-051 | Claude Model Version Pinned in Config | Data & AI Model | LLM | The specific Claude model version (e.g., claude-sonnet-4-5-20261001) must be pinned as a named constant in the config file — not referenced by an alias like "claude-sonnet-4-5". Provider aliases can silently update, causing unexpected behaviour changes in production. | Internal | Priya Nair — AI Lead | ⚪ Not Started | 🟠 Medium | 2026-10-14 | 2026-11-08 | — | DEP-030 | Use alias temporarily in local dev; switch to pinned version before first staging deploy. | — |
| DEP-052 | Token Budget + Cost Per User Defined | Data & AI Model | LLM | Maximum input + output token budget per user request must be agreed by Product and Engineering and hard-coded as constants. This directly controls cost per user, response latency, and rate limit headroom. Undefined budgets cause cost overruns. | Internal | Priya Nair — AI Lead | ⚪ Not Started | 🟠 Medium | 2026-10-14 | 2026-11-08 | — | DEP-050 | Use conservative 4,096 input / 1,024 output as default while cost modelling is finalised. | [2026-10-14] Initial cost model: at 4K/1K token budget + $0.003/1K input tokens (Claude Sonnet), estimated cost per conversation session = $0.014. At 500 daily active users: ~$7/day. Acceptable. |
| DEP-053 | Content Moderation Layer Implemented | Data & AI Model | LLM | Before any user-typed input is forwarded to the Claude API, a content moderation check must run. This can be Claude's own system prompt guardrails + an additional classification call. Required to prevent the product being used for harmful content generation — both a legal and brand risk. | Internal / External | Priya Nair — AI Lead | 🔴 Blocked | 🔴 High | 2026-10-14 | 2026-11-15 | — | DEP-050 | Restrict early beta to invited users only (friends + family) with manual content monitoring while automated layer is built. | [2026-10-14] Evaluating three approaches: (1) Claude system prompt guardrails only, (2) Separate moderation API call before main call, (3) LlamaGuard model. Decision needed by 2026-11-01. |

---

### 📋 Phase 2 — Business / Compliance Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-041 | Terms of Service + Privacy Policy Drafted | Business / Compliance | N/A | Legally reviewed Terms of Service, Privacy Policy, and AI Disclosure notice must be published at nova.app/legal before any external user creates an account. These documents must reflect the GDPR and CCPA findings from DEP-020 and the DPA from DEP-021. | Internal Legal / External Lawyer | Sarah Park — Legal | 🔴 Blocked | 🔴 High | 2026-10-14 | 2026-11-15 | — | DEP-020 | Run waitlist-only sign-ups (email capture only, no account creation) to build the user list while legal docs are being drafted. | [2026-10-14] External lawyer engaged. Template ToS sent. Blocked on GDPR review completing first (DEP-020). |

---

## 🧪 Phase 3 — QA, Testing & Security Review

### 🔧 Phase 3 — Technical Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-060 | Staging Environment Live (Web + API + DB) | Technical | N/A | A fully isolated staging environment mirroring production must be running on Vercel (web), AWS (API server), and a separate Supabase project (DB). All QA, load, and security tests must run against staging — never production. | Internal / Cloud Providers | Marcus Chen — DevOps | ⚪ Not Started | 🔴 High | 2026-10-14 | 2027-01-15 | — | DEP-011 | Run QA tests against a Docker Compose local stack if staging infra is delayed by more than 1 week. | — |
| DEP-061 | Automated Test Suite — Core Flows | Technical | N/A | Unit and integration tests covering the 5 core user flows (sign-up, AI message send/receive, task creation, settings change, billing) must be written and passing with >80% coverage before any release candidate is tagged. | Internal | Marcus Chen — DevOps | ⚪ Not Started | 🟠 Medium | 2026-10-14 | 2027-01-22 | — | DEP-060 | Manual QA sign-off by 2 team members on all 5 flows as minimum viable gate if automated suite is not complete at launch. | — |
| DEP-062 | Error Monitoring Live (Sentry) | Technical | N/A | Sentry must be integrated into the Next.js web app, Node.js API, and React Native mobile apps with alerts routed to the team Slack channel #nova-alerts before go-live. Without error monitoring we are blind to production crashes. | Cloud Provider | Marcus Chen — DevOps | ⚪ Not Started | 🔴 High | 2026-10-14 | 2027-01-29 | — | — | Use Vercel's built-in error logs as minimum visibility at launch if Sentry integration is delayed. | — |

---

### 🤖 Phase 3 — Data & AI Model Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-070 | AI Red-Teaming — 50 Adversarial Test Cases | Data & AI Model | LLM | The Claude system prompt and content moderation layer must be tested against 50 adversarial inputs (prompt injection attempts, requests for harmful content, data extraction probes) before launch. All High-severity failures must be fixed. | Internal | Priya Nair — AI Lead | ⚪ Not Started | 🔴 High | 2026-10-14 | 2027-01-29 | — | DEP-053 | Add a prominent "Report harmful output" button in both web and mobile UIs so early users can flag issues post-launch as a compensating control. | — |
| DEP-071 | LLM Quality Eval — 100 Benchmark Queries | Data & AI Model | LLM | A structured eval set of 100 queries covering Nova's core use cases (task management, content drafting, Q&A, scheduling) must be run against the production prompt and model. Pass threshold: ≥85% rated "satisfactory" by two independent reviewers. | Internal | Priya Nair — AI Lead | ⚪ Not Started | 🟠 Medium | 2026-10-14 | 2027-01-22 | — | DEP-050 | Use a 30-query minimum eval set if the full 100 cannot be reviewed before launch date. Document the gap and commit to full eval by 2 weeks post-launch. | — |

---

## 🚀 Phase 4 — Launch & Post-Launch (First 500 Users)

### 🔧 Phase 4 — Technical Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-090 | Production Infra Provisioned & Scaled | Technical | N/A | Production Vercel deployment (web), AWS EC2/ECS (API server), and production Supabase project must be live with auto-scaling enabled and capacity validated for 500 concurrent users before the first public user is onboarded. | Cloud Provider | Marcus Chen — DevOps | ⚪ Not Started | 🔴 High | 2026-10-14 | 2027-02-22 | — | DEP-011 | Hard-cap public signups at 50 users at launch and only open the cap once load testing confirms 500-user headroom. | — |
| DEP-091 | Cloudflare CDN + DDoS Protection | Technical | N/A | Cloudflare must be configured in front of the Vercel web app and AWS API server before public launch. Required to absorb traffic spikes from Product Hunt / App Store launch day and protect against basic DDoS. | Cloud Provider | Marcus Chen — DevOps | ⚪ Not Started | 🟠 Medium | 2026-10-14 | 2027-02-25 | — | DEP-090 | Enable Cloudflare Free tier DNS proxy as minimum DDoS protection. Upgrade to Pro if launch day traffic exceeds 10K requests/hour. | — |
| DEP-092 | On-Call Rotation + Runbooks Established | Technical | N/A | A minimum 2-person on-call rotation (Priya + Marcus) with PagerDuty alerts and documented incident runbooks for the top 5 failure scenarios (Claude API outage, DB connection failure, auth failure, mobile crash, billing failure) must be ready before go-live. | Internal | Alex Rivera — PM | ⚪ Not Started | 🟡 Low | 2026-10-14 | 2027-02-25 | — | DEP-062 | Founders take all on-call manually in launch week with Slack DM escalation. Formalise PagerDuty setup in week 2 post-launch. | — |

---

### 🤖 Phase 4 — Data & AI Model Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-100 | Claude API Cost Monitoring Dashboard | Data & AI Model | LLM | A real-time dashboard showing Claude API token usage and USD cost per user, per day, and total must be live before launch. Without it, a bug causing runaway API calls could generate hundreds of dollars in unexpected costs before anyone notices. | Internal / Anthropic Console | Priya Nair — AI Lead | ⚪ Not Started | 🔴 High | 2026-10-14 | 2027-02-22 | — | DEP-090 | Set a $50/day spend alert in the Anthropic console as a manual safety net. Check the console daily during launch week. | — |
| DEP-101 | LLM Fallback / Circuit Breaker Live | Data & AI Model | LLM | If the Anthropic Claude API returns 5xx errors or rate-limit 429s, the system must gracefully degrade: queue the request with a retry, show a "Nova is taking a short break — your request will be answered shortly" message, and alert the on-call engineer. | Internal | Priya Nair — AI Lead | ⚪ Not Started | 🔴 High | 2026-10-14 | 2027-02-25 | — | DEP-030 | Show a static friendly error message ("Nova is briefly unavailable") as minimum graceful degradation if circuit breaker is not implemented before launch. | — |

---

### 📋 Phase 4 — Business / Compliance Dependencies

| DEP-ID | Name | Type | AI Sub-Type | Description | Source | Owner | Status | Risk | Identified Date | Due Date | Resolved Date | Blocked By | Workaround Plan | Notes / Updates |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DEP-110 | App Store + Play Store Listings Approved | Business / Compliance | N/A | Both the iOS App Store and Google Play listings (screenshots, description, privacy label, category) must be reviewed and approved before launch day. Apple review typically takes 1–3 days; Google Play 3–7 days for new apps. Submit 2 weeks before target launch. | External (Apple / Google) | Jordan Lee — Mobile Lead | ⚪ Not Started | 🔴 High | 2026-10-14 | 2027-02-15 | — | DEP-031 | Launch web app only on launch day if app store approvals are delayed. Mobile app follows within days. Communicate clearly in launch email. | — |
| DEP-111 | SLA & Incident Response Policy Defined | Business / Compliance | N/A | A written uptime commitment (99.5% monthly target) and incident response policy (P0: 30-min response; P1: 2-hour response) must be documented before any enterprise or team-plan customers are onboarded. Not needed for free-tier consumer users. | Internal | Alex Rivera — PM | ⚪ Not Started | 🟠 Medium | 2026-10-14 | 2027-03-15 | — | — | Communicate "best effort" SLA verbally to first 500 consumer users. Formalise SLA for enterprise tier in Q2. | — |
| DEP-112 | 500-User Milestone Tracking Confirmed | Business / Compliance | N/A | PostHog or Supabase auth table query must accurately count monthly active users (MAU). This count is needed to confirm the 500-user milestone for investor reporting and to trigger the Phase 4 retrospective. | Internal | Alex Rivera — PM | ⚪ Not Started | 🟡 Low | 2026-10-14 | 2027-03-01 | — | — | Use Supabase auth.users table COUNT query as manual fallback user count. | — |

---

## 🗺️ Dependency Map (Who Blocks Whom)

| Upstream Dependency (Must Be Done First) | Downstream Dependency (Waiting on It) | Impact if Upstream Is Late |
|---|---|---|
| DEP-020 (GDPR / CCPA Legal Review) | DEP-011 (Supabase Prod Project), DEP-021 (DPA), DEP-041 (ToS + Privacy Policy) | All real user data handling and user onboarding blocked |
| DEP-021 (Anthropic DPA) | DEP-030 (Team API Key) | Cannot use Claude API with real user data in any environment |
| DEP-022 (Budget Approved) | DEP-031 (Apple Dev Account), DEP-032 (Google Play Account) | Cannot pay for developer accounts; mobile launch delayed |
| DEP-010 (Claude API PoC) | DEP-050 (System Prompt v1) | Prompt must be tuned to the selected model's specific behaviour |
| DEP-050 (System Prompt v1) | DEP-053 (Content Moderation), DEP-070 (Red-Teaming), DEP-071 (Evals) | Cannot test AI safety or quality without the final production prompt |
| DEP-011 (Supabase Prod Project) | DEP-034 (Schema Frozen), DEP-060 (Staging Env), DEP-090 (Production Infra) | No database; all backend and infrastructure work halted |
| DEP-031 (Apple Dev Account) | DEP-033 (EAS Build Config), DEP-110 (App Store Listing) | iOS app cannot be built, tested via TestFlight, or submitted |
| DEP-060 (Staging Environment) | DEP-061 (Automated Tests), DEP-062 (Sentry), DEP-070 (Red-Teaming), DEP-071 (Evals) | No safe environment for any testing |
| DEP-053 (Content Moderation) | DEP-070 (Red-Teaming) | Cannot accurately test adversarial inputs without the full moderation layer |
| DEP-090 (Production Infra) | DEP-091 (Cloudflare), DEP-092 (On-Call), DEP-100 (Cost Monitoring) | Cannot launch; no environment to serve public traffic |

---

## 📝 Changelog

| # | Date | Changed By | What Changed |
|---|---|---|---|
| 1 | 2026-10-14 | Alex Rivera — PM | Template created. Project metadata filled in. 24 dependencies added across all 4 phases. |
| 2 | 2026-10-17 | Marcus Chen — DevOps | DEP-001 marked Resolved — all dev environments confirmed working. |
| 3 | 2026-10-20 | Priya Nair — AI Lead | DEP-010 marked Resolved — Claude API PoC complete, claude-sonnet-4-5 selected. DEP-050 status updated to In Progress. |
| 4 | 2026-10-20 | Alex Rivera — PM | DEP-022 marked Resolved — $52K budget approved by board. |
| 5 | 2026-10-20 | Sarah Park — Legal | DEP-020 and DEP-021 notes updated — GDPR counsel engaged, Anthropic DPA requested. Both remain Blocked pending legal review. |

---

*Template maintained by: Alex Rivera — PM · Review: Every Monday 10 AM · Questions? Ping #nova-deps in Slack*

---

> **📌 Reminder:** This is a filled example. The blank template is in `Dependency_Register.md`. Copy the blank template for each new project and use this file only as a reference for how to fill it in.
