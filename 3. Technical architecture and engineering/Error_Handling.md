# Error_Handling.md

> **📌 How to Fill This Document**
>
> Welcome! This template helps you document every possible error your product might encounter — from the first line of code all the way to your first 500 customers.
>
> **Step-by-step instructions:**
> 1. Read every section heading before writing anything.
> 2. Wherever you see `[SQUARE BRACKETS]` → replace it with your own information.
> 3. Wherever you see `<!-- comment like this -->` → it's a hint to guide you. Delete the comment after filling it in.
> 4. Wherever you see a ✏️ icon → that field is required. Do not skip it.
> 5. Wherever you see a 💡 icon → it's a tip or example to help you understand what to write.
> 6. If you don't know an answer yet, write `TBD` and come back to it. Never leave a field blank.
> 7. Update the **Version History** section every time you change this document.
>
> **Who should fill this?** The person who built (or is building) the feature that can fail.
> **When should this be filled?** Before any feature goes to staging — not after it breaks in production.

---

## 📋 Table of Contents

1. [Document Overview](#1-document-overview)
2. [Error Code Naming Convention](#2-error-code-naming-convention)
3. [Severity Matrix (P0–P4)](#3-severity-matrix-p0p4)
4. [Error Categories & Registry](#4-error-categories--registry)
   - 4.1 Authentication & Authorization
   - 4.2 API & Network
   - 4.3 AI / LLM Errors *(AI-specific)*
   - 4.4 AI Agent & Tool Use Errors *(AI-specific)*
   - 4.5 Custom ML Model Errors *(AI-specific)*
   - 4.6 Database & Storage
   - 4.7 Frontend / UI
   - 4.8 Payment & Billing
   - 4.9 Third-Party Integrations
   - 4.10 Infrastructure & System
5. [AI-Specific Error Handling Playbook](#5-ai-specific-error-handling-playbook)
6. [Retry & Fallback Strategy](#6-retry--fallback-strategy)
7. [Error Handling by ADLC Stage](#7-error-handling-by-adlc-stage)
   - 7.1 Development & Local Testing
   - 7.2 CI/CD & Staging
   - 7.3 Production Launch
   - 7.4 Post-Launch (First 500 Users)
8. [User-Facing Error Messages](#8-user-facing-error-messages)
9. [Logging Standards](#9-logging-standards)
10. [Monitoring & Alerting Setup](#10-monitoring--alerting-setup)
11. [On-Call & Escalation Runbook](#11-on-call--escalation-runbook)
12. [Error Handling Checklist](#12-error-handling-checklist)
13. [Version History](#13-version-history)

---

## 1. Document Overview

<!-- Fill in the basic facts about this document. Think of it like a label on a box. -->

| Field | Details |
|---|---|
| ✏️ **Project Name** | `[e.g., AcmeSaaS — AI Writing Assistant]` |
| ✏️ **Product Type** | `[e.g., Web App (SaaS) / Mobile App / API Service]` |
| ✏️ **Document Owner** | `[Full Name — the person responsible for keeping this up to date]` |
| ✏️ **Last Updated** | `[YYYY-MM-DD]` |
| ✏️ **Version** | `[e.g., v1.0]` |
| **Tech Stack** | `[e.g., Next.js 14 / FastAPI / PostgreSQL / OpenAI GPT-4o]` |
| **AI Provider(s)** | `[e.g., OpenAI, Anthropic Claude, Hugging Face, Custom]` |
| **Target Audience** | `[e.g., B2B SaaS customers — marketing teams]` |
| **Related Documents** | `[Links to API_Contracts.md, Incident_Response.md, etc.]` |

### 1.1 Purpose

<!-- One or two sentences explaining WHY this document exists. -->

> ✏️ **Write 1–2 sentences here.**
>
> 💡 Example: *"This document defines how [Project Name] detects, handles, logs, and communicates every category of error — from a failed LLM call to a payment timeout — ensuring consistent behaviour across all environments and team members."*

### 1.2 Scope

<!-- Tell the reader WHAT this document covers and what it does NOT cover. -->

**In scope:**
- All errors that can occur in `[list your features, e.g., AI chat, user auth, billing]`
- Error handling from `[first commit date]` through post-launch (first 500 users)
- All environments: local dev → staging → production

**Out of scope:**
- `[e.g., Security penetration testing — see Security_Policy.md]`
- `[e.g., Data loss / disaster recovery — see DR_Runbook.md]`

---

## 2. Error Code Naming Convention

<!-- This section defines the "language" for all your errors. Every error in section 4 must follow this pattern. -->

### 2.1 Format

```
ERR-[CATEGORY]-[NNNN]
```

| Part | Meaning | Example |
|---|---|---|
| `ERR` | Fixed prefix — tells anyone reading logs this is an application error | `ERR` |
| `CATEGORY` | Short uppercase label for the error domain | `AUTH`, `LLM`, `DB`, `PAY` |
| `NNNN` | 4-digit zero-padded number unique within the category | `0001`, `0042`, `0100` |

**Full example:** `ERR-AUTH-0042` = Authentication error number 42.

### 2.2 Category Abbreviations

<!-- Add or remove rows to match your product. -->

| Code | Category | Description |
|---|---|---|
| `AUTH` | Authentication & Authorization | Login, session, permissions |
| `API` | API & Network | External/internal HTTP failures |
| `LLM` | AI / Large Language Model | LLM provider calls |
| `AGENT` | AI Agent & Tool Use | Multi-step agent failures |
| `ML` | Custom ML Model | Self-hosted / fine-tuned models |
| `DB` | Database & Storage | SQL, NoSQL, file storage |
| `UI` | Frontend / UI | Client-side rendering errors |
| `PAY` | Payment & Billing | Stripe, payment gateway |
| `INT` | Third-Party Integrations | Slack, email, CRM, etc. |
| `SYS` | Infrastructure & System | Server, memory, CPU, network |
| `[XXX]` | `[Add your own]` | `[Describe it]` |

### 2.3 Rules

1. **Never reuse** a code once assigned — even if the feature is deleted.
2. **Never skip** numbers in a sequence. Go 0001 → 0002 → 0003.
3. **Document every code** in Section 4 before shipping the feature.
4. When in doubt, pick the category that describes **where** the error originated, not where it was caught.

---

## 3. Severity Matrix (P0–P4)

<!-- This tells everyone: "How bad is this?" and "How fast do we need to fix it?" -->

> 💡 **How to use this matrix:**
> 1. Look at the error that just happened.
> 2. Find the row that best describes the impact.
> 3. Follow the **Response Time** and **Who Handles It** columns exactly.

| Priority | Name | Impact | Example | Max Response Time | Who Handles It | Communication |
|---|---|---|---|---|---|---|
| **P0** | 🔴 Critical | **Entire product is down** or data is being corrupted. No user can do anything. | Payment processing completely offline; production database unreachable | **15 minutes** | Founder / Lead Dev on-call immediately | Post in `#incidents` channel; email all affected customers within 1 hour |
| **P1** | 🟠 High | **Core AI feature is broken** for all/most users. Product is partially usable. | LLM API returns 500 for all users; login broken for a user segment | **1 hour** | Founder / Lead Dev | Post in `#incidents`; update status page |
| **P2** | 🟡 Medium | **One feature is broken** for some users. Workaround exists. | AI suggestions slow (>10s); file upload failing for specific file types | **4 hours** (business hours) | Developer assigned to the sprint | Comment on the bug ticket; notify affected users if >5% impacted |
| **P3** | 🔵 Low | **Minor inconvenience**. Feature works but not perfectly. | Typo in error message; wrong icon displayed on error screen | **Next sprint** | Any available developer | Bug ticket created and prioritised |
| **P4** | ⚪ Trivial | Cosmetic or very rare edge case. Almost nobody notices. | Error tooltip slightly misaligned; 404 on a legacy redirect | **Backlog** | Developer during downtime | Logged in backlog only |

### 3.1 How to Assign Severity — Decision Guide

<!-- Use this flowchart logic to assign P-levels quickly. -->

```
Is the entire product / all core features down for ALL users?
  └── YES → P0

Is a core AI feature or login broken for MOST users (>20%)?
  └── YES → P1

Is ONE feature broken, but others still work?
  └── YES → P2

Is the feature working but behaving oddly or slowly?
  └── YES → P3

Is it purely cosmetic / affects <1% of users?
  └── YES → P4
```

---

## 4. Error Categories & Registry

<!-- This is your master error list. One row per unique error. Fill in every column.
     The columns are: Code | HTTP Status | Description | Root Cause | Severity | User Message | Dev Action -->

> 💡 **Tip for beginners:** Start with errors you've already seen. Then add errors that COULD happen even if they haven't yet. Real engineers plan for failure before it happens.

---

### 4.1 Authentication & Authorization Errors (`AUTH`)

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-AUTH-0001` | 401 | User not logged in (no session token) | Token missing or not sent in request header | P2 | "Please sign in to continue." | Redirect to login page; clear local session data |
| `ERR-AUTH-0002` | 401 | Session token expired | JWT or cookie TTL elapsed | P2 | "Your session has expired. Please sign in again." | Issue a silent refresh token; if fails → logout |
| `ERR-AUTH-0003` | 403 | User does not have permission for this action | Role/permission mismatch in database | P2 | "You don't have permission to do that." | Log user ID + attempted action; do NOT reveal permission details |
| `ERR-AUTH-0004` | 429 | Too many login attempts (rate limited) | Brute-force or automated login attempt | P1 | "Too many attempts. Please wait 15 minutes and try again." | Lock account temporarily; alert on >10 failures in 60 sec |
| `ERR-AUTH-0005` | 401 | OAuth provider returned an error | Google/GitHub OAuth misconfiguration or user denied | P2 | "Sign-in failed. Please try a different method or contact support." | Log OAuth error_description; check provider dashboard |
| `[ERR-AUTH-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

### 4.2 API & Network Errors (`API`)

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-API-0001` | 400 | Malformed request body | Missing required field or wrong data type sent by client | P3 | "Something went wrong with your request. Please try again." | Validate input schema before sending; log the malformed payload |
| `ERR-API-0002` | 404 | Resource not found | Wrong ID, deleted record, or stale client cache | P3 | "We couldn't find what you're looking for." | Return clear 404; do NOT expose database structure |
| `ERR-API-0003` | 408 | Request timeout | Slow database query or downstream API took too long | P2 | "This is taking longer than expected. Please try again." | Set explicit timeouts on all outbound calls; add to slow-query log |
| `ERR-API-0004` | 429 | Rate limit exceeded | Too many requests from a single user/IP | P2 | "You're going too fast! Please slow down and try again shortly." | Return `Retry-After` header; implement token bucket algorithm |
| `ERR-API-0005` | 500 | Unhandled server exception | Unhandled exception in application code | P1 | "Something went wrong on our end. We're looking into it." | Log full stack trace to Sentry/Datadog; alert on-call |
| `ERR-API-0006` | 503 | Service unavailable / dependency down | Third-party service or internal microservice is offline | P1 | "We're experiencing temporary issues. Please try again in a few minutes." | Trigger circuit breaker; page on-call if > 5 min |
| `[ERR-API-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

### 4.3 AI / LLM Errors (`LLM`) ⚡ AI-Specific

<!-- These errors are unique to products that call AI APIs like OpenAI, Anthropic, Google Gemini, etc. -->

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-LLM-0001` | 503 | LLM provider API is unreachable | Provider outage or network partition | P1 | "Our AI assistant is temporarily unavailable. Please try again in a moment." | Retry 3× with exponential back-off (1s → 2s → 4s); then degrade gracefully |
| `ERR-LLM-0002` | 429 | LLM rate limit or quota exceeded | Too many tokens/requests per minute | P1 | "Our AI is busy right now. We're queuing your request." | Implement request queue; alert when >80% of quota used |
| `ERR-LLM-0003` | 400 | Prompt too long (exceeds context window) | Input + history exceeds model's token limit | P2 | "Your input is too long. Please shorten it and try again." | Truncate conversation history; summarise older context automatically |
| `ERR-LLM-0004` | 400 | Content policy violation (prompt blocked) | User input triggered safety filter | P2 | "We couldn't process that request. Please rephrase and try again." | Log sanitised version of prompt; do NOT log the full blocked text |
| `ERR-LLM-0005` | 200* | Empty or null response from LLM | Model returned blank output (finish_reason: null) | P2 | "The AI couldn't generate a response. Please try rephrasing." | Validate response before sending to user; auto-retry once |
| `ERR-LLM-0006` | 200* | LLM response timeout (stream hung) | Streaming response stalled mid-generation | P2 | "The AI response stopped unexpectedly. Please try again." | Implement stream timeout (e.g., 30 sec no token → abort) |
| `ERR-LLM-0007` | 401 | Invalid or expired API key | Rotated key not updated in environment | P0 | "Our AI service is currently unavailable." | Alert immediately; trigger key rotation runbook |
| `ERR-LLM-0008` | 200* | Hallucinated / factually wrong output | Model behaviour — cannot always detect | P3 | `(no user message — this is a quality issue, not a crash)` | Log output samples; add fact-checking layer or RAG grounding |
| `[ERR-LLM-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

> ⚠️ `*` HTTP 200 means the API call "succeeded" but the response content was bad. These are the trickiest AI errors — your code must validate the content, not just the HTTP status.

---

### 4.4 AI Agent & Tool Use Errors (`AGENT`) ⚡ AI-Specific

<!-- These errors apply when your AI makes decisions and calls tools (web search, code execution, APIs, etc.) -->

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-AGENT-0001` | 500 | Agent stuck in infinite loop | Prompt design flaw; agent keeps re-calling the same tool | P1 | "The AI couldn't complete this task. We've stopped it to protect your account." | Set max iteration limit (e.g., 10 steps); log full agent trace |
| `ERR-AGENT-0002` | 400 | Tool call failed — invalid parameters | Agent generated malformed function arguments | P2 | "Something went wrong while the AI was working on your request." | Validate tool inputs before execution; provide corrective feedback to agent |
| `ERR-AGENT-0003` | 403 | Agent attempted an unauthorised action | Prompt injection or scope escape | P1 | "The AI tried to do something it's not allowed to. Your account is safe." | Log full agent trace; suspend session; investigate for prompt injection |
| `ERR-AGENT-0004` | 408 | Agent task timeout | Long-running task exceeded time budget | P2 | "This task is taking too long. We've paused it — you can resume it later." | Implement async task queue with resumable state |
| `ERR-AGENT-0005` | 500 | Agent tool returned unexpected data format | External API schema changed; tool response parsing failed | P2 | "The AI encountered an unexpected response. Please try again." | Add schema validation on all tool outputs; version tool integrations |
| `[ERR-AGENT-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

### 4.5 Custom ML Model Errors (`ML`) ⚡ AI-Specific

<!-- These apply to self-hosted or fine-tuned models you run (e.g., on AWS SageMaker, Hugging Face Endpoints, etc.) -->

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-ML-0001` | 503 | Model server is down | Container crashed; GPU out of memory; cold start | P1 | "Our AI model is temporarily offline. We're restarting it now." | Restart container; set up auto-scaling and health checks |
| `ERR-ML-0002` | 408 | Model inference timeout | Input too complex; GPU bottleneck | P2 | "The AI is taking longer than expected. Please try a shorter request." | Set inference timeout; queue requests; scale up GPU instances |
| `ERR-ML-0003` | 500 | Model returned NaN / null / malformed tensor | Training data issue; model corruption | P1 | "Our AI encountered an error. We're looking into it." | Alert ML engineer immediately; roll back to previous model version |
| `ERR-ML-0004` | 400 | Input failed pre-processing validation | Wrong image format, text encoding, or dimension | P3 | "We couldn't read your input. Please check the format and try again." | Return specific format requirements in the error response |
| `ERR-ML-0005` | 500 | Model version mismatch | Deployed model version doesn't match API contract | P1 | "Something went wrong on our end. We're fixing it." | Pin model versions in deployment config; add version check on startup |
| `[ERR-ML-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

### 4.6 Database & Storage Errors (`DB`)

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-DB-0001` | 503 | Database connection failed | Connection pool exhausted; DB server down | P0 | "We're having trouble accessing your data. Please try again." | Alert on-call immediately; check connection pool limits |
| `ERR-DB-0002` | 409 | Unique constraint violation | Duplicate record insert (e.g., email already exists) | P3 | "That [email/username] is already taken. Please choose another." | Validate uniqueness before insert; handle at application layer |
| `ERR-DB-0003` | 500 | Query timeout | Slow or missing index; large table scan | P2 | "This is taking longer than expected. Please try again." | Add query timeout; log slow queries; add missing index |
| `ERR-DB-0004` | 507 | Storage quota exceeded | File/object storage full | P1 | "We've run out of storage space. Please contact support." | Alert at 80% capacity; auto-archive old files |
| `ERR-DB-0005` | 500 | Failed database migration | Schema migration broke existing data | P0 | "We're undergoing maintenance. We'll be back shortly." | Rollback migration immediately; notify affected users |
| `[ERR-DB-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

### 4.7 Frontend / UI Errors (`UI`)

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-UI-0001` | N/A | JavaScript runtime crash | Unhandled exception in browser/React Native | P2 | "Something went wrong. Please refresh the page." | Catch with Error Boundary (React); log to Sentry |
| `ERR-UI-0002` | N/A | Asset / chunk load failed | CDN outage; deployment in progress; cache mismatch | P1 | "We couldn't load the app. Please refresh or clear your cache." | Add retry logic for chunk loading; invalidate CDN cache on deploy |
| `ERR-UI-0003` | N/A | Form validation failed client-side | User submitted invalid data | P4 | `[Inline field-level message, e.g., "Email is required."]` | Show inline error next to the field; never show "Error: null" |
| `ERR-UI-0004` | N/A | Mobile app crash on launch | Incompatible OS version; missing permissions | P1 | `[App store review note — not a user message]` | Log crash report to Sentry/Firebase Crashlytics; test on min OS version |
| `[ERR-UI-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

### 4.8 Payment & Billing Errors (`PAY`)

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-PAY-0001` | 402 | Card declined | Insufficient funds; card blocked by bank | P2 | "Your card was declined. Please use a different payment method." | Do NOT log card details; direct user to update payment method |
| `ERR-PAY-0002` | 503 | Payment gateway unavailable | Stripe/payment provider outage | P1 | "Payments are temporarily unavailable. Please try again shortly." | Retry after delay; alert on-call; display status page link |
| `ERR-PAY-0003` | 400 | Webhook signature invalid | Webhook secret rotated or man-in-the-middle | P1 | `(Internal only — no user message)` | Reject webhook; alert security; rotate secret |
| `ERR-PAY-0004` | 402 | Subscription payment failed | Expired card; bank rejection on renewal | P2 | "We couldn't renew your subscription. Please update your payment details." | Send automated email; grace period 7 days; downgrade after |
| `[ERR-PAY-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

### 4.9 Third-Party Integration Errors (`INT`)

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-INT-0001` | 503 | Email delivery service down | SendGrid / Postmark / SES outage | P2 | `(Queue emails; user sees nothing unusual)` | Queue emails; retry; alert if queue > 500 |
| `ERR-INT-0002` | 401 | Third-party OAuth token expired | User's connected account needs re-auth | P2 | "Your [Slack/Google] connection needs to be refreshed. Click here to reconnect." | Store token expiry; proactively refresh before expiry |
| `ERR-INT-0003` | 429 | Third-party API rate limit hit | Too many calls to Slack, HubSpot, etc. | P2 | "We're syncing your data — this may take a few extra minutes." | Implement queue with rate-limit awareness; use webhooks over polling |
| `[ERR-INT-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

### 4.10 Infrastructure & System Errors (`SYS`)

| Error Code | HTTP Status | Description | Common Root Cause | Severity | User-Facing Message | Developer Action |
|---|---|---|---|---|---|---|
| `ERR-SYS-0001` | 503 | Server out of memory (OOM) | Memory leak; traffic spike | P0 | "We're experiencing high load. Please try again in a moment." | Auto-restart container; alert on-call; scale horizontally |
| `ERR-SYS-0002` | 503 | CPU throttling | Compute-heavy AI workload peak | P1 | "Our service is under heavy load. Please try again shortly." | Scale up compute; queue AI jobs; alert at >80% CPU |
| `ERR-SYS-0003` | N/A | Failed health check | Service not responding to `/health` endpoint | P0 | `(Internal — load balancer routes around unhealthy node)` | Auto-remove from load balancer; page on-call |
| `ERR-SYS-0004` | N/A | Disk space critically low | Logs or uploads filling disk | P1 | `(Internal only)` | Alert at 85% disk; auto-rotate logs; archive old data |
| `[ERR-SYS-XXXX]` | `[code]` | `[Your error]` | `[Cause]` | `[Px]` | `[Message]` | `[Action]` |

---

## 5. AI-Specific Error Handling Playbook

<!-- This section is your "recipe book" for handling AI failures gracefully.
     The strategies here apply to all LLM, Agent, and ML errors above. -->

### 5.1 LLM Call Failure — Standard Decision Tree

```
LLM API Call Made
      │
      ▼
Did it succeed (HTTP 200 + non-empty content)?
  ├── YES → Validate content quality (not empty, not truncated) → Serve to user
  └── NO  → What was the error?
                │
                ├── 429 Rate Limit → Queue request → Retry after Retry-After header
                │
                ├── 503 / 500 → Retry 3× with exponential back-off:
                │                 Attempt 1: wait 1 sec
                │                 Attempt 2: wait 2 sec
                │                 Attempt 3: wait 4 sec
                │               Still failing? → Show friendly error → Log to monitoring
                │
                ├── 400 (prompt too long) → Truncate / summarise context → Retry once
                │
                ├── 401 (bad API key) → P0 alert → Do NOT retry → Page on-call
                │
                └── Content blocked (policy) → Show guidance message → Log (no raw prompt)
```

### 5.2 Exponential Back-Off Configuration

<!-- Fill in the values your team agrees on. These are sensible defaults. -->

| Parameter | Default Value | Notes |
|---|---|---|
| ✏️ Max retries | `3` | After 3 failures, stop and show error |
| ✏️ Base delay | `1000 ms` | First retry waits 1 second |
| ✏️ Multiplier | `2×` | Each retry doubles the wait |
| ✏️ Max delay cap | `30,000 ms` | Never wait more than 30 seconds |
| ✏️ Jitter | `±20%` random | Prevents thundering herd (many users retrying at once) |

**Pseudocode:**
```python
for attempt in range(1, max_retries + 1):
    try:
        response = call_llm(prompt)
        return response
    except RateLimitError:
        wait = min(base_delay * (2 ** attempt) + random_jitter(), max_delay)
        sleep(wait)
raise FriendlyError("ERR-LLM-0001", user_message="Our AI is temporarily unavailable.")
```

### 5.3 Graceful Degradation Levels

<!-- When AI fails, what does the user see? Define your degradation ladder here. -->

| Level | Trigger | What the User Experiences | What the System Does |
|---|---|---|---|
| **Level 0 — Full AI** | All systems normal | Full AI experience | Normal operation |
| **Level 1 — Slow AI** | LLM latency > 5 sec | Typing indicator / progress bar; AI still working | Stream response with heartbeat |
| **Level 2 — Cached Response** | LLM fails after retries; cached result available | Slightly older AI response; banner: "Using saved result" | Serve cache; log cache hit |
| **Level 3 — Disabled AI Feature** | LLM completely unavailable | AI feature hidden; rest of app works normally | Circuit breaker open; display status message |
| **Level 4 — Maintenance Mode** | P0 — Full outage | Maintenance page with status link | Kill switch enabled; redirect all traffic |

### 5.4 Prompt Injection — Detection & Response

<!-- Prompt injection = a user tries to trick your AI into doing things it shouldn't. -->

| Threat | Detection Method | Response |
|---|---|---|
| User tries to override system prompt | Check for phrases like "ignore previous instructions", "you are now..." | Reject input; log attempt; send user a warning |
| Agent accesses out-of-scope tool | Validate allowed tools list before execution | Block action; log full agent trace; escalate to P1 |
| Malicious data in retrieved context (RAG) | Sanitize and escape all retrieved content before injecting into prompt | Strip dangerous sequences; log the source document |

---

## 6. Retry & Fallback Strategy

<!-- A one-page reference for any developer on your team. -->

### 6.1 When to Retry vs. When to Fail Fast

| HTTP Status / Error | Retry? | How Many Times? | Strategy |
|---|---|---|---|
| 429 Rate Limit | ✅ Yes | Honour `Retry-After` header | Wait exactly as long as the header says |
| 500 Internal Server Error | ✅ Yes | 3× max | Exponential back-off |
| 503 Service Unavailable | ✅ Yes | 3× max | Exponential back-off |
| 408 Timeout | ✅ Yes | 2× max | Retry with shorter prompt if possible |
| 400 Bad Request | ❌ No | 0 | Fix the input; do not retry |
| 401 Unauthorized | ❌ No | 0 | Refresh token; if fails → re-auth |
| 403 Forbidden | ❌ No | 0 | User does not have access; show message |
| 404 Not Found | ❌ No | 0 | Resource gone; show "not found" |

### 6.2 Circuit Breaker Settings

<!-- A circuit breaker "trips" after too many failures, stopping calls to a broken service.
     This prevents your app from hammering a failing AI provider and slowing everything down. -->

| Parameter | Value | Meaning |
|---|---|---|
| ✏️ Failure threshold | `5 failures` | Trip after 5 consecutive failures |
| ✏️ Reset timeout | `60 seconds` | Try the service again after 60 sec |
| ✏️ Half-open probe | `1 request` | Let 1 request through to test if service is back |

**States:**
- 🟢 **Closed** (normal) → requests flow through
- 🔴 **Open** (tripped) → all requests fail immediately with cached/degraded response
- 🟡 **Half-open** (testing) → one probe request sent; if it succeeds → back to Closed

---

## 7. Error Handling by ADLC Stage

<!-- ADLC = AI-Driven Development Life Cycle. Each stage has different priorities for error handling. -->

---

### 7.1 Development & Local Testing

> 🎯 **Goal at this stage:** Catch errors early and loudly. In dev, you WANT errors to be verbose and visible.

| Practice | Implementation |
|---|---|
| **Verbose logging** | Log ALL errors to console with full stack trace. No silent failures. |
| **Error boundary testing** | Deliberately trigger each error code from Section 4 and confirm the right message appears. |
| **LLM mock mode** | Use mock/stub LLM responses in unit tests so tests don't cost money or fail due to network. |
| **Environment variable checks** | On startup, validate that all required keys (LLM API key, DB URL, etc.) are present. Crash loudly if missing. |
| **Error code registry check** | Before committing, confirm every new error has a code in Section 4. No undocumented errors. |

**Local Error Log Format:**
```json
{
  "timestamp": "2026-10-14T09:32:00Z",
  "level": "ERROR",
  "error_code": "ERR-LLM-0001",
  "message": "LLM provider unreachable after 3 retries",
  "context": {
    "user_id": "dev_test_user",
    "feature": "ai_chat",
    "attempt": 3,
    "latency_ms": 4250
  },
  "stack_trace": "..."
}
```

**Developer Checklist — Before Moving to Staging:**
- [ ] All new errors are documented in Section 4
- [ ] Every LLM call has retry logic implemented
- [ ] Every LLM response is validated (not just HTTP 200 check)
- [ ] No raw error messages (stack traces) are visible to the user
- [ ] Unit tests exist for each error path

---

### 7.2 CI/CD & Staging

> 🎯 **Goal at this stage:** Verify error handling works in a production-like environment before real users see it.

| Practice | Implementation |
|---|---|
| **Automated error injection tests** | CI pipeline runs tests that simulate ERR-LLM-0001, ERR-DB-0001, ERR-AUTH-0002, etc. |
| **Error rate gate** | Deployment is blocked if error rate > `[X]`% in staging smoke test. |
| **Staging monitoring** | Connect staging to `[your monitoring tool]` with a separate "staging" project. |
| **Real LLM calls in staging** | Use real (but cheap) AI calls in staging to catch integration errors missed by mocks. |
| **Log drain validation** | Confirm structured logs appear correctly in your log aggregator before promoting. |

**CI/CD Error Gate Configuration:**
```yaml
# Example: GitHub Actions error gate
- name: Check error rate
  run: |
    ERROR_RATE=$(curl -s "$MONITORING_API/error-rate?env=staging" | jq '.rate')
    if (( $(echo "$ERROR_RATE > 0.05" | bc -l) )); then
      echo "Error rate $ERROR_RATE exceeds 5% threshold. Blocking deploy."
      exit 1
    fi
```

**Staging Checklist — Before Going Live:**
- [ ] All P0 and P1 error scenarios tested in staging
- [ ] User-facing error messages reviewed by someone who is NOT the developer
- [ ] Monitoring alerts configured for production (see Section 10)
- [ ] Rollback procedure tested and documented in Section 11
- [ ] AI fallback / degradation modes confirmed working

---

### 7.3 Production Launch

> 🎯 **Goal at this stage:** Detect and fix errors before they reach most users. Launch slowly.

**Launch Strategy: Staged Rollout**

| Phase | User % | Duration | What to Watch |
|---|---|---|---|
| **Canary** | 1–5% of users | 30–60 minutes | P0/P1 error rate; LLM failure rate |
| **Early access** | 10–20% | 2–4 hours | Error rate by feature; user feedback |
| **Full launch** | 100% | — | All error rates; latency; AI quality |

**Launch Day Error Monitoring — Dashboard Metrics:**
- [ ] Overall error rate (target: <`[X]`% — fill in your threshold)
- [ ] LLM call success rate (target: >`[Y]`% — fill in your target)
- [ ] P99 response latency (target: <`[Z]` ms)
- [ ] Authentication error rate
- [ ] Payment error rate

**Rollback Trigger Conditions:**
<!-- Define EXACTLY when you will roll back. Remove ambiguity. -->

| Condition | Action |
|---|---|
| P0 error rate > `[X]`% for 5 consecutive minutes | Immediately roll back + page on-call |
| LLM unavailability > 15 minutes | Enable Level 3 degradation (Section 5.3) + roll back if persists |
| Payment processing down > 5 minutes | Roll back + open Stripe support ticket |
| Any data corruption detected | Immediate rollback + database snapshot restore |

---

### 7.4 Post-Launch (First 500 Users)

> 🎯 **Goal at this stage:** Listen carefully. Your first users will find errors you never imagined.

**User Feedback → Error Triage Pipeline:**

```
User reports a problem
        │
        ▼
Support team tags it with error code (if known)
        │
        ▼
Developer confirms in logs (search by user_id + timestamp)
        │
        ▼
Assign severity (P0–P4)
        │
        ▼
Fix → Deploy → Confirm in logs → Close ticket → Update Section 4 if new error
```

**Weekly Error Review Meeting (First 500 Users Phase):**

Run a 30-minute weekly review covering:
1. Top 5 most frequent errors this week (by count)
2. Top 5 most impactful errors (by severity × frequency)
3. New error codes discovered and not yet in Section 4
4. AI quality issues (hallucinations, unhelpful responses)
5. Error rate trend: getting better or worse?

**KPIs to Track:**

| Metric | Target | How to Measure |
|---|---|---|
| ✏️ Weekly error rate | < `[X]`% of sessions | `[Monitoring tool]` → error rate dashboard |
| ✏️ LLM success rate | > `[Y]`% | Log `ERR-LLM-*` count / total LLM calls |
| ✏️ Mean time to resolve P1 | < 4 hours | Time from alert → fix deployed |
| ✏️ User-reported bug rate | < `[Z]` bugs per 100 users | Support tickets / active users |
| ✏️ User satisfaction (post-error) | > `[N]`/10 | In-app survey after error screen |

---

## 8. User-Facing Error Messages

<!-- The words a real user reads when something goes wrong. 
     The #1 rule: never show technical errors (stack traces, SQL errors, "undefined") to users. -->

### 8.1 Writing Good Error Messages — 4-Part Formula

Every user-facing error message should have:

```
[What happened] + [Why (optional, if not scary)] + [What to do next] + [Support link]
```

| Part | Bad Example ❌ | Good Example ✅ |
|---|---|---|
| What happened | "Error 500" | "Something went wrong on our end." |
| Why (optional) | "Unhandled exception in LLM pipeline" | "Our AI hit an unexpected issue." |
| What to do next | "Retry" | "Please try again — it usually works on the second attempt." |
| Support link | None | "Still stuck? [Contact support →]" |

### 8.2 Standard Error Message Library

<!-- Copy-paste these into your UI. Edit the [placeholders] for your product. -->

| Scenario | Message |
|---|---|
| Generic server error | "Something went wrong on our end. We've been notified and are looking into it. Please try again in a moment." |
| AI temporarily unavailable | "Our AI assistant is taking a short break. Please try again in a minute — it's usually quick to recover." |
| Not logged in | "Please sign in to continue. [Sign in →]" |
| Session expired | "Your session has expired for security reasons. [Sign in again →]" |
| No permission | "You don't have permission to do that. If you think this is a mistake, [contact your admin]." |
| Rate limited | "You're moving fast! Please wait a moment before trying again." |
| Offline (mobile) | "You appear to be offline. Check your connection and try again." |
| Feature in maintenance | "[Feature name] is undergoing maintenance. We'll be back shortly. [Check status →]" |
| Payment failed | "We couldn't process your payment. Please check your card details and try again. [Update payment →]" |

### 8.3 Error Message Tone Rules

- ✅ **Simple words** — write at a Grade 6 reading level
- ✅ **We, not You** — say "We couldn't load" not "You failed to load"
- ✅ **Always give a next step** — never leave the user stranded
- ✅ **Never blame the user** — even if the error is caused by bad input
- ❌ **Never show** error codes, stack traces, or database errors to users
- ❌ **Never use** words like "fatal", "crash", "exception", "null", "undefined"

---

## 9. Logging Standards

<!-- How errors are recorded so you can diagnose them later. Think of logs like a flight recorder. -->

### 9.1 Required Log Fields

Every error log entry **must** include these fields:

| Field | Type | Required | Description | Example |
|---|---|---|---|---|
| `timestamp` | ISO 8601 string | ✅ Yes | When the error occurred | `"2026-10-14T09:32:00.123Z"` |
| `level` | string | ✅ Yes | `ERROR`, `WARN`, `INFO`, `DEBUG` | `"ERROR"` |
| `error_code` | string | ✅ Yes | From Section 4 | `"ERR-LLM-0001"` |
| `message` | string | ✅ Yes | Human-readable description | `"LLM API unreachable"` |
| `service` | string | ✅ Yes | Which service threw the error | `"ai-chat-service"` |
| `environment` | string | ✅ Yes | `dev`, `staging`, `production` | `"production"` |
| `user_id` | string | ✅ Yes | Anonymised or hashed user ID | `"u_abc123"` |
| `session_id` | string | ✅ Yes | Current session identifier | `"sess_xyz789"` |
| `request_id` | string | ✅ Yes | Unique ID for this request (for tracing) | `"req_def456"` |
| `severity` | string | ✅ Yes | P0–P4 from Section 3 | `"P1"` |
| `stack_trace` | string | ⚠️ Prod: omit from user-facing logs | Full exception trace | `"TypeError at line 42..."` |
| `context` | object | ✅ Yes | Feature-specific metadata | `{"feature": "ai_chat", "model": "gpt-4o"}` |
| `latency_ms` | number | If applicable | How long the failed operation took | `4250` |

### 9.2 Log Levels — When to Use Each

| Level | Use For | Stored In Prod? |
|---|---|---|
| `ERROR` | Something broke and needs fixing | ✅ Always |
| `WARN` | Something unusual but not broken (e.g., slow response) | ✅ Always |
| `INFO` | Normal operations (user logged in, AI call completed) | ✅ Yes (rotate after `[X]` days) |
| `DEBUG` | Detailed trace for diagnosing issues | ❌ Dev/Staging only |

### 9.3 What NEVER to Log

- ❌ Passwords, API keys, tokens
- ❌ Full credit card numbers or CVVs
- ❌ SSN, passport numbers, or government IDs
- ❌ Full LLM prompts that contain user PII
- ❌ Raw webhook payloads from payment providers

---

## 10. Monitoring & Alerting Setup

<!-- Where errors are sent, who gets notified, and how. -->

### 10.1 Monitoring Tools Setup

<!-- Fill in the tools you actually use. Delete rows for tools you don't use. -->

| Tool | Purpose | Environment | Dashboard Link | Owner |
|---|---|---|---|---|
| `[e.g., Sentry]` | Error tracking & stack traces | Production + Staging | `[URL]` | ✏️ `[Your name]` |
| `[e.g., Datadog]` | Metrics, logs, APM | Production | `[URL]` | ✏️ `[Your name]` |
| `[e.g., CloudWatch]` | Cloud infrastructure logs | Production | `[URL]` | ✏️ `[Your name]` |
| `[e.g., Custom dashboard]` | AI-specific metrics | Production | `[URL]` | ✏️ `[Your name]` |

### 10.2 Alert Configuration

<!-- Define exactly which alerts are set up, what triggers them, and who gets the notification. -->

| Alert Name | Trigger Condition | Notification Channel | Who Gets Paged | Action |
|---|---|---|---|---|
| 🔴 P0 — Production Down | Error rate > `[X]`% for 3 min | PagerDuty + SMS + Slack `#incidents` | ✏️ `[Name]` | Immediate response |
| 🔴 P0 — LLM API Key Invalid | `ERR-LLM-0007` detected | PagerDuty + SMS | ✏️ `[Name]` | Rotate key now |
| 🟠 P1 — LLM Failure Spike | LLM error rate > `[Y]`% for 5 min | Slack `#incidents` + Email | ✏️ `[Name]` | Investigate + degrade |
| 🟠 P1 — DB Connection Failed | `ERR-DB-0001` > 3 times in 1 min | PagerDuty | ✏️ `[Name]` | Check DB health |
| 🟡 P2 — Payment Errors | `ERR-PAY-*` > `[Z]`/hr | Slack `#alerts` | ✏️ `[Name]` | Check Stripe dashboard |
| 🟡 P2 — High Latency | P99 response time > `[ms]` | Slack `#alerts` | ✏️ `[Name]` | Profile slow calls |
| ⚪ Daily Error Summary | Every day at 09:00 | Email to `[team@company.com]` | Whole team | Review and triage |

### 10.3 Status Page

<!-- A public or internal page that tells users the current system health. -->

| Field | Details |
|---|---|
| ✏️ Status page URL | `[e.g., status.yourproduct.com]` |
| ✏️ Tool used | `[e.g., Instatus, Atlassian Statuspage, custom]` |
| **What to update** | Update status page within 15 minutes of any P0 or P1 incident |
| **Who updates it** | ✏️ `[Your name / on-call person]` |

---

## 11. On-Call & Escalation Runbook

<!-- This section tells you EXACTLY what to do when something breaks at 2am. -->

### 11.1 On-Call Rotation

| Role | Person | Contact | Coverage |
|---|---|---|---|
| ✏️ Primary on-call | `[Name]` | `[Phone / Slack]` | `[Hours/days]` |
| ✏️ Secondary on-call | `[Name]` | `[Phone / Slack]` | `[When primary unreachable]` |
| ✏️ Executive escalation | `[Name]` | `[Phone]` | `[P0 only, if unresolved after 1 hour]` |

### 11.2 Incident Response Steps

<!-- Follow these steps IN ORDER when a P0 or P1 error occurs. -->
<!-- Even if you're a solo founder, this keeps you calm and systematic under pressure. -->

```
STEP 1 — DETECT (0–5 min)
  - Receive alert (PagerDuty / SMS / Slack)
  - Confirm the alert is real (check monitoring dashboard)
  - Assign severity: P0 or P1?

STEP 2 — COMMUNICATE (5–10 min)
  - Post in #incidents: "🔴 Incident started: [brief description]. Investigating."
  - Update status page: "Investigating — [feature] is experiencing issues."

STEP 3 — INVESTIGATE (10–30 min)
  - Search logs for the error code (e.g., ERR-LLM-0001)
  - Identify: When did it start? What changed? (recent deploy? Provider outage?)
  - Check provider status pages (OpenAI, Anthropic, AWS, Stripe)

STEP 4 — MITIGATE (ASAP)
  - Apply temporary fix: rollback / enable fallback / circuit breaker
  - Confirm error rate is dropping on the monitoring dashboard

STEP 5 — RESOLVE (When stable)
  - Post in #incidents: "✅ Resolved: [what was done]. Root cause: [brief description]."
  - Update status page: "Resolved — [feature] is back to normal."

STEP 6 — POST-MORTEM (Within 48 hours)
  - Write a short post-mortem (see template below)
  - Update Section 4 if a new error type was discovered
  - Add a new test to prevent recurrence
```

### 11.3 Post-Mortem Template

```markdown
## Incident Post-Mortem

**Incident Date:** [YYYY-MM-DD]
**Severity:** [P0 / P1]
**Error Code(s):** [e.g., ERR-LLM-0001]
**Duration:** [e.g., 47 minutes]
**Users Affected:** [e.g., ~130 users (26% of active users)]

### What Happened
[2–3 sentences describing the incident in plain English]

### Root Cause
[The actual technical reason — be specific]

### Timeline
| Time | Event |
|------|-------|
| 14:03 | Alert fired in Slack |
| 14:08 | On-call developer acknowledged |
| 14:22 | Root cause identified |
| 14:50 | Fix deployed and confirmed |

### What We'll Do to Prevent This
1. [Action item 1 — assign to a person with a due date]
2. [Action item 2]
3. [Action item 3]
```

---

## 12. Error Handling Checklist

<!-- Use this checklist before every feature ships. Print it, paste it in your PR template. -->

### 12.1 Developer Checklist (Before Every Pull Request)

- [ ] Every new error has a code in Section 4 of this document
- [ ] All LLM calls have: retry logic + response validation + fallback
- [ ] All agent tool calls have: scope check + iteration limit + timeout
- [ ] No raw error messages / stack traces can reach the user
- [ ] User-facing error messages follow the 4-part formula (Section 8.1)
- [ ] All error log entries include the required fields (Section 9.1)
- [ ] No PII, passwords, or API keys are being logged
- [ ] Unit tests exist for the main error paths
- [ ] Error monitoring alert is configured (Section 10.2)

### 12.2 Pre-Launch Checklist (Before Going to Production)

- [ ] All P0 and P1 errors have been manually triggered and confirmed in staging
- [ ] Monitoring dashboards reviewed and showing correct data
- [ ] Status page connected and tested
- [ ] On-call person identified and confirmed reachable
- [ ] Rollback procedure documented and tested
- [ ] User-facing error messages reviewed by a non-technical person
- [ ] AI degradation modes (Section 5.3) tested
- [ ] Circuit breaker settings configured (Section 6.2)

### 12.3 First 500 Users Checklist (Post-Launch)

- [ ] Weekly error review meeting scheduled
- [ ] User feedback → error triage pipeline working (Section 7.4)
- [ ] KPIs being tracked (Section 7.4)
- [ ] New errors discovered since launch added to Section 4
- [ ] At least one post-mortem completed (Section 11.3)
- [ ] Error rate trend is flat or decreasing week-over-week

---

## 13. Version History

<!-- Update this table every time you change this document. -->

| Version | Date | Author | What Changed |
|---|---|---|---|
| `v1.0` | `[YYYY-MM-DD]` | `[Your name]` | Initial draft |
| `[v1.1]` | `[YYYY-MM-DD]` | `[Name]` | `[What you added or changed]` |

---

*This document is a living record. It should grow every time your product grows.*
*If an error happens that isn't in here — add it before you close the ticket.*
