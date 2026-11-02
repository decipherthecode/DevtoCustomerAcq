# 📋 Acceptance Criteria Template
> **Version:** 1.1.0 | **Last Updated:** `YYYY-MM-DD` | **Template Owner:** `[Your Name or Team]`

---

## 🚀 HOW TO FILL THIS DOCUMENT — START HERE

> **Welcome!** This document helps your team agree on exactly what "done" looks like for every feature you build.
> Think of Acceptance Criteria like a **recipe card** 🍰 — it tells everyone the exact ingredients and steps needed
> so that the final dish always turns out the same, no matter who cooked it.

### 📌 What is Acceptance Criteria?

Acceptance Criteria (AC) is a clear checklist that answers:
- **"What exactly must this feature do before we call it finished?"**
- **"How do we know it's working correctly?"**
- **"What happens when something goes wrong?"**

If a feature passes all the criteria in this document → it is **DONE** ✅  
If even one **MUST** item fails → it is **NOT DONE** ❌

---

### 🎨 How to Read the Priority Labels

| Label | Icon | What it means | Can we launch without it? |
|-------|------|--------------|--------------------------|
| MUST  | 🔴   | Non-negotiable. The feature breaks without this. | ❌ No |
| SHOULD | 🟡  | Important but not a blocker. Aim to include it. | ⚠️ Ideally no |
| NICE  | 🟢   | Great if we have time. Bonus feature. | ✅ Yes |

---

### ✏️ Step-by-Step Instructions

1. **Copy this entire file** and rename it:
   `AC_[FeatureName]_[YYYY-MM-DD].md`
   > Example: `AC_UserLogin_2026-10-14.md`

2. **Fill in every field marked with** `[REPLACE THIS]`

3. **Delete any section** that does not apply to this feature (e.g., if there's no AI agent involved, delete Part 4).

4. **Add your own rows** to any table or checklist — the template is a starting point, not a prison.

5. **Review with your team** before development starts (Sprint Planning or Backlog Refinement).

6. **Sign off** in Part 10 before the feature goes to QA.

> 💡 **Tip for first-timers:** Fill one section at a time. Don't rush.
> Each section has a filled-in example in *italics* — use it as a guide, then replace it.

---

## 📂 PART 0: Document Identity
> *Think of this like a book cover — it tells everyone at a glance what this document is about and who owns it.*

| Field | Your Answer |
|-------|-------------|
| **Feature Name** | `[REPLACE: e.g., "User Login with Google OAuth"]` |
| **Feature ID / Ticket #** | `[REPLACE: e.g., "PROJ-42" or "Sprint 3 – Story 7"]` |
| **Epic / Parent Feature** | `[REPLACE: e.g., "Authentication & Onboarding"]` |
| **Product** | `[REPLACE: e.g., "HealthAI Web App" / "HealthAI iOS App"]` |
| **Platform** | `☐ Web (SaaS)` `☐ iOS` `☐ Android` `☐ API` `☐ All` |
| **Sprint / Release** | `[REPLACE: e.g., "Sprint 5" or "v1.2.0"]` |
| **Document Author** | `[REPLACE: Your full name]` |
| **Date Created** | `[REPLACE: YYYY-MM-DD]` |
| **Last Updated** | `[REPLACE: YYYY-MM-DD]` |
| **Status** | `☐ Draft` `☐ In Review` `☐ Approved` `☐ Done` |
| **Priority** | `☐ Critical` `☐ High` `☐ Medium` `☐ Low` |

---

## 🧩 PART 1: Feature Overview
> *This is the "elevator pitch" of the feature. Explain it so clearly that anyone — even someone not on the team —
> understands what it is, why it exists, and who it helps.*

### 1.1 Plain English Summary
> ✏️ **Example:** *"The login feature lets users sign in to the app using their Google account. This removes the need to remember passwords and reduces friction at sign-up."*

```
[REPLACE: Write 2–4 sentences explaining what this feature does and why we're building it.
No technical jargon. Imagine explaining it to a friend who has never used computers before.]
```

### 1.2 Problem Being Solved
> ✏️ **Example:** *"Currently, users have to create a separate password just for our app. Many forget it and never return. Google sign-in reduces this drop-off."*

```
[REPLACE: What frustration, inefficiency, or gap does this feature fix?]
```

### 1.3 User Story (Who, What, Why)
> *Fill in the blanks:*

```
As a [REPLACE: type of user, e.g., "first-time visitor"],
I want to [REPLACE: action, e.g., "log in using my Google account"],
So that [REPLACE: benefit, e.g., "I can access the app without creating a new password"].
```

### 1.4 Feature Scope (What's IN and OUT)

| | Description |
|-|-------------|
| ✅ **In Scope** (we WILL build this) | `[REPLACE: List what this feature includes, one per line]` |
| ❌ **Out of Scope** (we will NOT build this now) | `[REPLACE: List what is intentionally excluded to avoid confusion]` |

> ✏️ **Example In Scope:** Google OAuth login, session token generation, "Remember Me" checkbox
> ✏️ **Example Out of Scope:** Facebook login, Apple Sign-In, 2FA (planned for v2)

### 1.5 Dependencies
> *What other features, services, or teams must be ready BEFORE this can work?*

- [ ] `[REPLACE: e.g., "Google Cloud project must be configured with OAuth credentials"]`
- [ ] `[REPLACE: e.g., "User database table must exist with email field"]`
- [ ] `[REPLACE: e.g., "AI Agent X must return a session token on successful auth"]`

### 1.6 Linked Resources

| Resource | Link |
|----------|------|
| Figma / Design Mockup | `[REPLACE: URL or "N/A"]` |
| API Documentation | `[REPLACE: URL or "N/A"]` |
| Related Tickets | `[REPLACE: PROJ-40, PROJ-41]` |
| Claude / AI Prompt Doc | `[REPLACE: URL or "N/A"]` |

---

## 👥 PART 2: Who Uses This Feature? (Personas)
> *Before writing criteria, we need to know WHO will be using this feature. Different people have different needs.*
> *Think of these like the different "players" in a video game — each has different abilities and goals.*

### 2.1 Persona Definitions for THIS Feature

| Persona | Who Are They? | What They Need from This Feature |
|---------|---------------|----------------------------------|
| 👤 **End User** | `[REPLACE: e.g., "A patient using the mobile app to book appointments"]` | `[REPLACE: e.g., "Fast, simple login. Must work offline."]` |
| 🛡️ **Admin** | `[REPLACE: e.g., "A clinic manager who manages user accounts"]` | `[REPLACE: e.g., "Ability to revoke access and view login logs"]` |
| 🤖 **AI Agent** | `[REPLACE: e.g., "Claude-powered scheduling assistant that acts on behalf of user"]` | `[REPLACE: e.g., "Must receive authenticated session token to call API on user's behalf"]` |

> 💡 **Tip:** Only keep the rows that apply. Delete any persona not involved in this feature.

---

## ✅ PART 3: Acceptance Criteria by Role
> *This is the heart of the document. For each persona, we list exactly what must be true for this feature to be accepted.*
>
> **How to read the checkboxes:**
> - `- [ ]` = Not done yet (leave it like this when filling the template)
> - `- [x]` = Done and verified ✅ (check it off during QA)

---

### 3.1 👤 End User Criteria

> ✏️ **Context:** *What the end user must be able to do, see, or feel when using this feature.*

#### 🔴 MUST (Non-negotiable — feature is broken without these)

- [ ] 🔴 MUST: `[REPLACE: e.g., "User can complete the login flow in fewer than 3 taps/clicks on both web and mobile"]`
- [ ] 🔴 MUST: `[REPLACE: e.g., "User sees a clear error message if login fails, not a blank screen or crash"]`
- [ ] 🔴 MUST: `[REPLACE: e.g., "User is redirected to their last visited page after logging in successfully"]`
- [ ] 🔴 MUST: `[REPLACE: e.g., "Session lasts 30 days if 'Remember Me' is checked, 1 hour if not"]`
- [ ] 🔴 MUST: `[REPLACE: Add more MUST criteria here]`

#### 🟡 SHOULD (Important — include unless time/resources don't allow)

- [ ] 🟡 SHOULD: `[REPLACE: e.g., "Login page loads within 2 seconds on a standard 4G connection"]`
- [ ] 🟡 SHOULD: `[REPLACE: e.g., "User receives a welcome email within 60 seconds of first login"]`
- [ ] 🟡 SHOULD: `[REPLACE: Add more SHOULD criteria here]`

#### 🟢 NICE (Bonus — great if we have time)

- [ ] 🟢 NICE: `[REPLACE: e.g., "User sees a personalized greeting using their first name after login"]`
- [ ] 🟢 NICE: `[REPLACE: e.g., "Biometric login (Face ID / fingerprint) is offered on mobile after first sign-in"]`
- [ ] 🟢 NICE: `[REPLACE: Add more NICE criteria here]`

---

### 3.2 🛡️ Admin Criteria

> ✏️ **Context:** *What the admin or back-office user must be able to do to manage, monitor, or control this feature.*

#### 🔴 MUST

- [ ] 🔴 MUST: `[REPLACE: e.g., "Admin can view a log of all login attempts (successful and failed) in the admin dashboard"]`
- [ ] 🔴 MUST: `[REPLACE: e.g., "Admin can deactivate a user account and immediately invalidate their session"]`
- [ ] 🔴 MUST: `[REPLACE: e.g., "Admin receives an alert if more than 5 failed login attempts occur for one account within 10 minutes"]`
- [ ] 🔴 MUST: `[REPLACE: Add more MUST criteria here]`

#### 🟡 SHOULD

- [ ] 🟡 SHOULD: `[REPLACE: e.g., "Admin can export login logs as a CSV file for compliance reporting"]`
- [ ] 🟡 SHOULD: `[REPLACE: e.g., "Admin dashboard shows login activity chart (daily/weekly/monthly)"]`
- [ ] 🟡 SHOULD: `[REPLACE: Add more SHOULD criteria here]`

#### 🟢 NICE

- [ ] 🟢 NICE: `[REPLACE: e.g., "Admin can bulk-reset passwords for a selected group of users"]`
- [ ] 🟢 NICE: `[REPLACE: Add more NICE criteria here]`

---

### 3.3 🤖 AI Agent Criteria

> ✏️ **Context:** *What the AI Agent (Claude or other LLM-powered component) must be able to do as part of this feature.*
> *This section only applies if an AI agent is involved. If not, delete it.*

#### 🔴 MUST

- [ ] 🔴 MUST: `[REPLACE: e.g., "AI Agent receives a valid, scoped session token before making any API call on behalf of the user"]`
- [ ] 🔴 MUST: `[REPLACE: e.g., "AI Agent cannot access any resource that the logged-in user does not have permission to view"]`
- [ ] 🔴 MUST: `[REPLACE: e.g., "AI Agent gracefully handles an expired token by notifying the user to re-authenticate, not by crashing"]`
- [ ] 🔴 MUST: `[REPLACE: Add more MUST criteria here]`

#### 🟡 SHOULD

- [ ] 🟡 SHOULD: `[REPLACE: e.g., "AI Agent caches the session token securely and does not request a new one on every API call"]`
- [ ] 🟡 SHOULD: `[REPLACE: Add more SHOULD criteria here]`

#### 🟢 NICE

- [ ] 🟢 NICE: `[REPLACE: e.g., "AI Agent surfaces login anomaly alerts to the user in natural language (e.g., 'I noticed someone tried to access your account from a new device')"]`
- [ ] 🟢 NICE: `[REPLACE: Add more NICE criteria here]`

---

## 🤖 PART 4: AI-Specific Acceptance Criteria
> *This section is for any feature that uses an AI model (like Claude) to generate responses, make decisions,
> or automate tasks. Think of the AI like a very smart assistant — we need to make sure it answers correctly,
> quickly, and safely.*

> 💡 **Tip:** If this feature has no AI component, delete this entire section.

### 4.1 Prompt Quality

| # | Criterion | Priority | Pass/Fail |
|---|-----------|----------|-----------|
| P1 | The AI prompt clearly defines the task, context, role, and output format before any user input is processed. | 🔴 MUST | `[ ]` |
| P2 | The prompt includes at least 1 example of expected output (few-shot). | 🟡 SHOULD | `[ ]` |
| P3 | The prompt instructs the AI to say "I don't know" rather than guess when data is missing. | 🔴 MUST | `[ ]` |
| P4 | `[REPLACE: Add your own prompt quality criterion]` | 🔴 / 🟡 / 🟢 | `[ ]` |

### 4.2 Response Quality

| # | Criterion | Priority | Pass/Fail |
|---|-----------|----------|-----------|
| R1 | AI responses are factually consistent with the data provided in the context window (no hallucinations). | 🔴 MUST | `[ ]` |
| R2 | AI does not generate toxic, harmful, biased, or discriminatory content under any tested input. | 🔴 MUST | `[ ]` |
| R3 | AI responses stay within the defined scope — it does not attempt tasks it was not asked to do. | 🔴 MUST | `[ ]` |
| R4 | Response length is appropriate — not too short to be useless, not too long to be unreadable. | 🟡 SHOULD | `[ ]` |
| R5 | `[REPLACE: Add your own response quality criterion]` | 🔴 / 🟡 / 🟢 | `[ ]` |

### 4.3 Performance & Latency

| # | Criterion | Target | Priority | Pass/Fail |
|---|-----------|--------|----------|-----------|
| L1 | First token appears in the UI within | `≤ 1.5 seconds` | 🔴 MUST | `[ ]` |
| L2 | Full response delivered within | `≤ 8 seconds` for ≤500 words | 🟡 SHOULD | `[ ]` |
| L3 | AI feature remains functional under load | `100 concurrent users` | 🟡 SHOULD | `[ ]` |
| L4 | `[REPLACE: Your own latency requirement]` | `[REPLACE: target]` | 🔴 / 🟡 / 🟢 | `[ ]` |

### 4.4 Fallback & Safety Behaviour

- [ ] 🔴 MUST: If the AI model is unavailable (API timeout, error), the user sees a friendly message and can retry or contact support — the app does NOT crash.
- [ ] 🔴 MUST: If the AI returns a response flagged as harmful or off-topic, it is filtered before reaching the user.
- [ ] 🟡 SHOULD: If the AI is uncertain, it indicates uncertainty (e.g., "I'm not fully sure, but...") rather than presenting a guess as fact.
- [ ] 🟡 SHOULD: A human override or escalation path is available if the AI cannot complete the task.
- [ ] `[REPLACE: Add your own fallback criterion]`

### 4.5 Claude Tool-Use / Function-Calling Criteria
> *This section applies when Claude is given access to external tools (functions, APIs, databases) it can call
> on its own to complete a task — for example, looking up a patient record, booking a calendar slot, or
> running a database query.*

> 💡 **Plain English:** Claude "tool-use" is like giving the AI a smartphone with specific apps it can open.
> This section checks that it only opens the right apps, at the right time, with the right data.

#### 🔴 MUST

- [ ] 🔴 MUST: Claude only calls tools that are explicitly listed in the system prompt — it cannot discover or call unlisted tools.
- [ ] 🔴 MUST: Every tool call is logged with: timestamp, tool name, input parameters, output, and the user session that triggered it.
- [ ] 🔴 MUST: Claude validates required parameters before calling a tool — it does not call a tool with missing or null required fields.
- [ ] 🔴 MUST: If a tool call fails (timeout, error, invalid response), Claude catches the error gracefully and either retries once or informs the user — it does not enter an infinite retry loop.
- [ ] 🔴 MUST: Claude does not pass sensitive data (PHI, PII, credentials) as tool call parameters unless the tool is explicitly designed and approved to receive that data.
- [ ] 🔴 MUST: Tool outputs are validated before Claude uses them in a response — Claude does not blindly trust or repeat a tool's output as fact.
- [ ] `[REPLACE: Add your own tool-use MUST criterion]`

#### 🟡 SHOULD

- [ ] 🟡 SHOULD: Claude confirms with the user before calling a tool that performs a write, update, or delete operation (e.g., "I'm about to book this appointment — shall I proceed?").
- [ ] 🟡 SHOULD: Tool call latency is monitored separately from AI generation latency — slow tool calls are flagged in observability dashboards.
- [ ] 🟡 SHOULD: A maximum number of tool calls per user turn is enforced (e.g., no more than `[REPLACE: e.g., 5]` tool calls in a single response chain) to prevent runaway loops.
- [ ] `[REPLACE: Add your own tool-use SHOULD criterion]`

#### 🟢 NICE

- [ ] 🟢 NICE: Claude explains to the user which tool it is about to use and why (transparent agentic behaviour), e.g., "I'll look that up in your medical records now."
- [ ] 🟢 NICE: Tool-use audit trail is available to admins in a dedicated dashboard view.
- [ ] `[REPLACE: Add your own tool-use NICE criterion]`

#### Tool Registry (List every tool Claude can call in this feature)

| Tool Name | What It Does | Can Read? | Can Write? | PHI/PII? | Approved? |
|-----------|-------------|-----------|-----------|----------|-----------|
| `[REPLACE: e.g., get_patient_record]` | `[REPLACE: e.g., Fetches patient record by ID]` | ✅ Yes | ❌ No | ✅ Yes | `☐ Pending` |
| `[REPLACE: e.g., book_appointment]` | `[REPLACE: e.g., Creates a new appointment slot]` | ✅ Yes | ✅ Yes | ✅ Yes | `☐ Pending` |
| `[REPLACE: e.g., search_knowledge_base]` | `[REPLACE: e.g., Searches FAQ articles]` | ✅ Yes | ❌ No | ❌ No | `☐ Pending` |
| `[Add more rows as needed]` | | | | | |

---

### 4.6 AI Model Configuration (document the exact settings used)

| Setting | Value |
|---------|-------|
| **AI Provider** | `[REPLACE: e.g., "Anthropic Claude"]` |
| **Model Version** | `[REPLACE: e.g., "claude-opus-4-5"]` |
| **Temperature** | `[REPLACE: e.g., "0.3 (low = more predictable)"]` |
| **Max Tokens** | `[REPLACE: e.g., "1024"]` |
| **System Prompt Version** | `[REPLACE: e.g., "v2.1 — stored in /prompts/login_assistant.txt"]` |
| **Context Window Used** | `[REPLACE: e.g., "Last 10 messages + user profile summary"]` |

---

## ⚠️ PART 5: Edge Cases & Failure Scenarios
> *An edge case is something unusual that most users won't do — but someone will.*
> *Think of it like asking: "What if a toddler got hold of this? What could go wrong?"*
> *We need to make sure the app handles weird situations gracefully, not by crashing.*

### 5.1 Edge Case Table

> Fill in one row per edge case. Be specific about what the user does and what the system should do.

| # | Edge Case Description | Expected System Behaviour | Priority | Tested? |
|---|-----------------------|---------------------------|----------|---------|
| E1 | User submits the login form with an empty email field | Show inline error: "Please enter your email address." Button stays disabled. | 🔴 MUST | `[ ]` |
| E2 | User's Google account is suspended during an active session | Session is invalidated immediately. User is shown: "Your account access has changed. Please contact support." | 🔴 MUST | `[ ]` |
| E3 | User logs in from two devices simultaneously | Both sessions remain active (or specify: only the latest session is kept — document your policy). | 🟡 SHOULD | `[ ]` |
| E4 | User loses internet connection mid-login flow | Display offline banner. Retry automatically when connection returns. Data is not lost. | 🟡 SHOULD | `[ ]` |
| E5 | AI Agent receives a malformed or empty API response | Log the error silently. Show user: "Something went wrong. Please try again." Never show raw error code. | 🔴 MUST | `[ ]` |
| E6 | User inputs special characters or emojis in a name field | Field accepts them without crashing. Data is stored and displayed correctly. | 🟡 SHOULD | `[ ]` |
| E7 | `[REPLACE: Your custom edge case]` | `[REPLACE: Expected behaviour]` | 🔴 / 🟡 / 🟢 | `[ ]` |
| E8 | `[REPLACE: Your custom edge case]` | `[REPLACE: Expected behaviour]` | 🔴 / 🟡 / 🟢 | `[ ]` |

### 5.2 Negative Scenarios (What the Feature Must NEVER Do)

- [ ] 🔴 MUST NEVER: `[REPLACE: e.g., "Expose raw error stack traces to the end user"]`
- [ ] 🔴 MUST NEVER: `[REPLACE: e.g., "Store passwords in plain text"]`
- [ ] 🔴 MUST NEVER: `[REPLACE: e.g., "Allow an unauthenticated user to access a protected route by guessing a URL"]`
- [ ] 🔴 MUST NEVER: `[REPLACE: e.g., "Send PHI (health data) to an AI model without explicit user consent"]`
- [ ] `[REPLACE: Add your own]`

---

## 🔒 PART 6: Compliance Checklist
> *Laws and regulations are rules set by governments and industry bodies that your product MUST follow.*
> *Think of them like the health-and-safety rules for a kitchen — not optional.*
> *Check off each item BEFORE the feature is released.*

### 6.1 GDPR & CCPA (Data Privacy — for users in EU and California)

- [ ] 🔴 MUST: Users are clearly informed about what personal data is collected and why (Privacy Notice shown at sign-up).
- [ ] 🔴 MUST: Users can request deletion of their account and all associated data ("Right to be Forgotten").
- [ ] 🔴 MUST: Explicit consent is obtained before collecting any non-essential data (e.g., analytics, marketing).
- [ ] 🔴 MUST: Personal data is not transferred outside the user's region without appropriate safeguards.
- [ ] 🟡 SHOULD: Users can download a copy of all their data ("Data Portability").
- [ ] 🟡 SHOULD: Cookie consent banner is shown to EU/CA users before any tracking scripts load.
- [ ] `[REPLACE: Any additional GDPR/CCPA requirement specific to your product]`

### 6.2 HIPAA (Healthcare Data — if your product handles health information)

- [ ] 🔴 MUST: No Protected Health Information (PHI) is stored in logs, analytics events, or error reports.
- [ ] 🔴 MUST: All PHI is encrypted at rest (AES-256 or equivalent) and in transit (TLS 1.2+).
- [ ] 🔴 MUST: Access to PHI is role-based — only users with explicit permission can view it.
- [ ] 🔴 MUST: A Business Associate Agreement (BAA) is signed with all third-party vendors that may touch PHI (including AI providers).
- [ ] 🔴 MUST: All access to PHI is logged with timestamp, user ID, and action type (audit trail).
- [ ] 🟡 SHOULD: Automatic session timeout after 15 minutes of inactivity for any screen displaying PHI.
- [ ] `[REPLACE: Any additional HIPAA requirement]`

> ⚠️ **Important:** If you are sending patient data to an AI model (e.g., Claude), verify your BAA covers this use case BEFORE go-live.

### 6.3 SOC 2 / ISO 27001 (Security Standards)

- [ ] 🔴 MUST: Authentication tokens are signed, time-limited, and stored securely (not in localStorage for web).
- [ ] 🔴 MUST: All API endpoints require authentication — no unprotected routes in production.
- [ ] 🔴 MUST: Penetration test or security review completed before GA launch.
- [ ] 🔴 MUST: Secrets (API keys, DB passwords) are stored in a secrets manager (not in code or .env files committed to Git).
- [ ] 🟡 SHOULD: Dependency scanning is part of the CI/CD pipeline (no known critical CVEs in production).
- [ ] 🟡 SHOULD: Security incident response runbook is documented and shared with the team.
- [ ] `[REPLACE: Any additional security requirement]`

---

## 🧪 PART 7: Testing Requirements
> *Testing is how we prove the feature works. Think of it like taste-testing a dish at every stage of cooking —
> not just at the end.*

### 7.1 Unit Tests (individual code pieces)

> Developer-owned. Written during development. Automated and run on every code push.

- [ ] 🔴 MUST: All new functions/methods have at least 1 unit test covering the "happy path" (normal use).
- [ ] 🔴 MUST: All new functions/methods have at least 1 unit test covering a failure or invalid input.
- [ ] 🟡 SHOULD: Code coverage for this feature is ≥ `[REPLACE: e.g., 80%]`.
- [ ] `[REPLACE: Any additional unit test requirement]`

**Files to test:** `[REPLACE: e.g., auth.service.ts, token.utils.ts, login.component.ts]`

### 7.2 Integration Tests (multiple pieces working together)

> Developer or QA-owned. Run in CI/CD before merge.

- [ ] 🔴 MUST: The full login API flow is tested end-to-end (request → auth check → token generation → response).
- [ ] 🔴 MUST: Integration test covers the failure path (wrong credentials → expected error response).
- [ ] 🟡 SHOULD: Database write after login (session record) is verified in integration test.
- [ ] `[REPLACE: Any additional integration test requirement]`

### 7.3 End-to-End (E2E) / UI Tests (full user journey)

> QA-owned. Run against a staging environment before release.

| Test Case | Steps | Expected Result | Priority |
|-----------|-------|-----------------|----------|
| TC-001: Happy path login | 1. Open app → 2. Tap "Sign in with Google" → 3. Authorize → 4. Land on home | User lands on home screen. Name is shown. | 🔴 MUST |
| TC-002: Failed login | 1. Open app → 2. Enter invalid credentials → 3. Submit | Error message shown. No crash. | 🔴 MUST |
| TC-003: Session persistence | 1. Login → 2. Close app → 3. Reopen | User stays logged in (if "Remember Me" was checked). | 🟡 SHOULD |
| `[TC-00X: Your test case]` | `[Steps]` | `[Expected result]` | 🔴 / 🟡 / 🟢 |

**Test environment:** `[REPLACE: e.g., "Staging — https://staging.myapp.com"]`  
**Test tool:** `[REPLACE: e.g., "Playwright", "Cypress", "Maestro (mobile)"]`

### 7.4 AI Output / Hallucination Tests

> QA or AI Engineer-owned. Must be run before any AI feature goes live.

| Test Case | Input | Expected AI Behaviour | Priority | Tested? |
|-----------|-------|-----------------------|----------|---------|
| AT-001: Normal question | A valid question within scope | Accurate, relevant answer | 🔴 MUST | `[ ]` |
| AT-002: Out-of-scope question | "What is the weather today?" | AI declines politely and redirects to its purpose | 🔴 MUST | `[ ]` |
| AT-003: Prompt injection | User tries to override the system prompt in their message | AI ignores the injection and stays on task | 🔴 MUST | `[ ]` |
| AT-004: Empty input | User sends a blank message | AI asks for clarification, does not crash | 🟡 SHOULD | `[ ]` |
| AT-005: PHI in input | User includes a patient name/DOB | AI does NOT echo PHI back in response (if applicable) | 🔴 MUST | `[ ]` |
| `[AT-00X: Your test case]` | `[Input]` | `[Expected]` | 🔴 / 🟡 / 🟢 | `[ ]` |

**Test data set:** `[REPLACE: Link to your test prompt set or describe it here]`

---

## ✅ PART 8: Definition of Done (DoD)
> *The Definition of Done is the final checklist. A feature is only "Done" when EVERY item below is checked off.*
> *Think of it as the final inspection before a car leaves the factory.*

> ⚠️ **Rule:** If even ONE 🔴 MUST item is unchecked, the feature cannot move to QA or production.

### 8.1 Development Complete

- [ ] 🔴 MUST: Code is written and pushed to the feature branch.
- [ ] 🔴 MUST: All unit and integration tests are passing locally.
- [ ] 🔴 MUST: No new linting errors or compiler warnings introduced.
- [ ] 🔴 MUST: Code is peer-reviewed and approved by at least **1 other developer**.
- [ ] 🟡 SHOULD: Code is documented with inline comments for complex logic.
- [ ] 🟡 SHOULD: API changes are reflected in the API documentation.

### 8.2 QA Complete

- [ ] 🔴 MUST: All 🔴 MUST acceptance criteria from Parts 3–5 are verified and passing.
- [ ] 🔴 MUST: All E2E test cases are passing in the staging environment.
- [ ] 🔴 MUST: All AI output tests are passing (if applicable).
- [ ] 🔴 MUST: No open critical (P0/P1) bugs related to this feature.
- [ ] 🟡 SHOULD: All 🟡 SHOULD criteria are verified or a documented exception is approved.
- [ ] 🟡 SHOULD: Regression testing completed — existing features are not broken.

### 8.3 Compliance & Security Complete

- [ ] 🔴 MUST: All applicable 🔴 MUST compliance checklist items from Part 6 are verified.
- [ ] 🔴 MUST: Security review completed (or exception documented with approval).
- [ ] 🔴 MUST: No secrets, PHI, or PII are committed to the codebase or exposed in logs.

### 8.4 Stakeholder & PM Sign-Off

- [ ] 🔴 MUST: Product Manager (or Product Owner) has reviewed the feature in staging and given written approval.
- [ ] 🔴 MUST: Any known limitations or deferred items are documented in the ticket and acknowledged by the PM.
- [ ] 🟡 SHOULD: A demo has been shown to at least 1 stakeholder (investor, client, or business owner).

### 8.5 Ready for Release

- [ ] 🔴 MUST: Feature flag is configured (if applicable — feature can be toggled off without a deploy).
- [ ] 🔴 MUST: Rollback plan is documented (how to undo this release if something breaks in production).
- [ ] 🟡 SHOULD: Monitoring and alerting are set up for this feature (error rate, latency, AI response quality).
- [ ] 🟡 SHOULD: Analytics events are firing correctly in staging (track what users do with this feature).

---

## 🚀 PART 9: Launch Phase Gates
> *Before we let the world use this feature, it must pass through launch gates. Think of these like airport security —
> each gate checks something different before you can board the plane.*

---

### 9.1 General Availability (GA) Gate
> *This is the checklist that must be GREEN before we flip the switch and make the feature public.*

**Launch Date Target:** `[REPLACE: YYYY-MM-DD]`  
**Launch Decision Owner:** `[REPLACE: e.g., "CEO / Head of Product"]`

#### Pre-Launch Checks

| # | Check | Owner | Status |
|---|-------|-------|--------|
| G1 | All Definition of Done items (Part 8) are complete | Product Manager | `☐ Pending` / `☑ Done` |
| G2 | Infrastructure scaled to handle expected launch traffic | Engineering Lead | `☐ Pending` / `☑ Done` |
| G3 | Error monitoring (e.g., Sentry) is live and alerting the right people | DevOps / Eng | `☐ Pending` / `☑ Done` |
| G4 | AI model API rate limits are confirmed sufficient for launch day volume | AI Engineer / PM | `☐ Pending` / `☑ Done` |
| G5 | Customer support team has been briefed on the new feature | CS Lead | `☐ Pending` / `☑ Done` |
| G6 | Legal has reviewed AI output for compliance (HIPAA / GDPR as applicable) | Legal / PM | `☐ Pending` / `☑ Done` |
| G7 | App store submission approved (if mobile feature) | Mobile Lead | `☐ Pending` / `☑ Done` / `☐ N/A` |
| G8 | `[REPLACE: Your own GA gate]` | `[Owner]` | `☐ Pending` / `☑ Done` |

#### GA Launch Checklist (Day-Of)

- [ ] Production environment health check passed (all systems green).
- [ ] Feature flag turned ON in production.
- [ ] Announcement sent (to email list, in-app notification, or social media).
- [ ] Team is on standby for first 2 hours after launch to monitor and respond to issues.
- [ ] Rollback procedure is ready to execute within `[REPLACE: e.g., "15 minutes"]` if critical bug is found.

---

### 9.2 First 500 Customers Milestone
> *After launch, we track specific outcomes to confirm the feature is working in the real world —
> not just in testing. The First 500 Customers Milestone is our first major proof point.*
> *Think of it like a restaurant checking reviews after the first 500 dinners.*

**Milestone Target Date:** `[REPLACE: YYYY-MM-DD]`  
**Milestone Owner:** `[REPLACE: e.g., "Head of Growth / PM"]`

#### 9.2.1 Success Metrics (We Win If...)

> ✏️ **Example:** *"80% of users who try the login feature complete it successfully on their first attempt."*

| Metric | Target | How We Measure It | Current Value |
|--------|--------|-------------------|---------------|
| **Feature Activation Rate** | `[REPLACE: e.g., ≥ 70% of new signups use this feature]` | Analytics event `feature_activated` | `[Auto-filled]` |
| **Task Completion Rate** | `[REPLACE: e.g., ≥ 85% of users who start, finish]` | Funnel analysis | `[Auto-filled]` |
| **Error Rate** | `[REPLACE: e.g., < 1% of sessions hit an error]` | Error monitoring tool | `[Auto-filled]` |
| **AI Response Quality Score** | `[REPLACE: e.g., ≥ 4.0/5.0 user rating]` | In-app thumbs up/down | `[Auto-filled]` |
| **AI Hallucination Rate** | `[REPLACE: e.g., < 0.5% of responses flagged by moderators]` | AI output monitoring | `[Auto-filled]` |
| **Support Ticket Volume** | `[REPLACE: e.g., < 5 tickets per 100 users]` | CRM / help desk | `[Auto-filled]` |
| **Net Promoter Score (NPS)** | `[REPLACE: e.g., ≥ 40]` | In-app NPS survey | `[Auto-filled]` |
| `[REPLACE: Custom metric]` | `[Target]` | `[How measured]` | `[Auto-filled]` |

#### 9.2.2 Failure Signals (We Escalate If...)

> *These are early warning signs that something is wrong. If any of these trigger, the team must meet within 24 hours.*

- [ ] Error rate exceeds `[REPLACE: e.g., 5%]` within the first week.
- [ ] AI model generates a harmful or wildly inaccurate response that reaches a real user.
- [ ] More than `[REPLACE: e.g., 10]` support tickets about the same issue within 48 hours.
- [ ] Feature activation rate is below `[REPLACE: e.g., 20%]` after 7 days (users are ignoring it).
- [ ] A compliance violation is reported (GDPR, HIPAA, etc.).
- [ ] `[REPLACE: Your own failure signal]`

#### 9.2.3 Post-Milestone Review (After 500 Customers)

Once 500 customers have used this feature, schedule a **retrospective meeting** and answer:

| Question | Your Answer (fill after milestone) |
|----------|-----------------------------------|
| Did we hit our success metrics? | `[To be filled]` |
| What surprised us (good or bad)? | `[To be filled]` |
| What is the top user complaint? | `[To be filled]` |
| What is the top thing users loved? | `[To be filled]` |
| What will we improve in v2? | `[To be filled]` |
| Should the AI prompt be updated based on real usage? | `[To be filled]` |

---

## 📝 PART 10: Sign-Off
> *This section is the official record that the feature has been reviewed and approved by the right people.*
> *It is the legal/professional equivalent of signing a contract.*

> ⚠️ **Rule:** This section must be filled in BEFORE the feature is deployed to production.

### 10.1 Approval Signatures

| Role | Name | Decision | Date | Notes |
|------|------|----------|------|-------|
| **Product Manager / Owner** | `[REPLACE]` | `☐ Approved` / `☐ Rejected` / `☐ Conditional` | `YYYY-MM-DD` | `[REPLACE: Any conditions or notes]` |
| **Engineering Lead** | `[REPLACE]` | `☐ Approved` / `☐ Rejected` / `☐ Conditional` | `YYYY-MM-DD` | `[REPLACE]` |
| **QA Lead** | `[REPLACE]` | `☐ Approved` / `☐ Rejected` / `☐ Conditional` | `YYYY-MM-DD` | `[REPLACE]` |
| **AI / ML Engineer** (if AI involved) | `[REPLACE]` | `☐ Approved` / `☐ Rejected` / `☐ Conditional` | `YYYY-MM-DD` | `[REPLACE]` |
| **Security / Compliance Lead** | `[REPLACE]` | `☐ Approved` / `☐ Rejected` / `☐ Conditional` | `YYYY-MM-DD` | `[REPLACE]` |
| **Legal / Data Privacy** (if HIPAA/GDPR applies) | `[REPLACE]` | `☐ Approved` / `☐ Rejected` / `☐ Conditional` | `YYYY-MM-DD` | `[REPLACE]` |
| **Executive Sponsor** (for GA launches only) | `[REPLACE]` | `☐ Approved` / `☐ Rejected` / `☐ Conditional` | `YYYY-MM-DD` | `[REPLACE]` |

> 💡 **Tip:** "Conditional Approval" means: *"I'll approve it once [specific thing] is fixed."*
> Document the condition clearly in the Notes column.

### 10.2 Open Issues / Parking Lot
> *Any known issue, risk, or deferred item that the team agreed to accept and address later.*

| # | Issue Description | Owner | Target Resolution Date | Status |
|---|-------------------|-------|------------------------|--------|
| OI-1 | `[REPLACE: e.g., "Biometric login deferred to Sprint 8"]` | `[REPLACE]` | `YYYY-MM-DD` | `☐ Open` |
| OI-2 | `[REPLACE]` | `[REPLACE]` | `YYYY-MM-DD` | `☐ Open` |

### 10.3 Revision History

| Version | Date | Changed By | What Changed |
|---------|------|------------|--------------|
| 1.0 | `YYYY-MM-DD` | `[Author]` | Initial draft |
| 1.1 | `YYYY-MM-DD` | `[Author]` | `[Describe change]` |

---

## 📚 APPENDIX A: Quick Glossary
> *New to software development? Here are plain-English definitions for the terms used in this document.*

| Term | What it means in plain English |
|------|-------------------------------|
| **Acceptance Criteria** | The exact checklist that decides if a feature is done or not. |
| **Agile / Scrum** | A way of working in short cycles (sprints) to build things step by step. |
| **AI Agent** | A program powered by an AI model that can take actions on your behalf (like booking a meeting or answering questions). |
| **API** | A bridge between two software applications that lets them talk to each other. |
| **BAA (Business Associate Agreement)** | A legal contract that says a third-party company (like an AI provider) will handle your health data safely. |
| **CI/CD Pipeline** | An automated system that tests and deploys code every time a developer makes a change. |
| **Definition of Done** | The final checklist a feature must pass before it's considered complete. |
| **Edge Case** | An unusual or unexpected situation that doesn't happen often but still needs to be handled. |
| **E2E Test** | A test that simulates a real user going through an entire feature from start to finish. |
| **Feature Flag** | A switch that lets you turn a feature on or off without deploying new code. |
| **GA (General Availability)** | When a feature or product is released to all users publicly. |
| **GDPR** | A European law that protects people's personal data and privacy. |
| **Gherkin** | A plain-English format for writing test scenarios: "Given [situation], When [action], Then [result]." |
| **Hallucination** | When an AI makes up information that sounds true but isn't. |
| **HIPAA** | A US law that protects patients' health information. |
| **PHI** | Protected Health Information — any data that can identify a patient (name, DOB, diagnosis, etc.). |
| **PM / PO** | Product Manager or Product Owner — the person responsible for deciding what gets built and why. |
| **Prompt** | The instruction you give to an AI model. |
| **Regression** | When a new change accidentally breaks something that was already working. |
| **Rollback** | Reversing a release to go back to the previous version when something breaks. |
| **SOC 2** | A security standard that proves a company handles customer data responsibly. |
| **Sprint** | A fixed period (usually 1–2 weeks) during which a team builds a specific set of features. |
| **Staging Environment** | A copy of the production system used for testing — real users never see it. |
| **TLS** | A security protocol that encrypts data while it travels over the internet (https). |
| **Unit Test** | A small automated test that checks one specific piece of code works correctly. |

---

## 📚 APPENDIX B: Template Checklist (Fill This First!)
> *Before you start filling the full document, use this quick checklist to make sure you have everything you need.*

- [ ] I know the exact name and ID of the feature I'm documenting.
- [ ] I have read the design mockups (if they exist).
- [ ] I know which user personas interact with this feature.
- [ ] I have spoken with at least one developer to understand technical constraints.
- [ ] I know the target launch date.
- [ ] I know which regulations apply to this feature (GDPR, HIPAA, SOC 2).
- [ ] I have identified the top 3–5 things that could go wrong (edge cases).
- [ ] I know who needs to sign off on this document.

---

---

## ♿ APPENDIX C: Accessibility Checklist (WCAG 2.1 / ADA)
> *Accessibility means making sure people with disabilities can use your product too — including people who are
> blind, have low vision, are deaf, or have limited motor control.*
> *In the US, ADA compliance is a legal requirement for many digital products. WCAG 2.1 Level AA is the
> internationally recognised standard.*
>
> 🧠 **Think of it like:** Building a ramp next to stairs. The stairs work for most people.
> The ramp makes it work for everyone.

> 💡 **Tip:** Delete criteria that don't apply to this feature (e.g., no video? Skip the captions row).

### C.1 Visual Accessibility

- [ ] 🔴 MUST: All text has a colour contrast ratio of at least **4.5:1** against its background (WCAG AA).
- [ ] 🔴 MUST: No information is conveyed by colour alone (e.g., error states also show an icon or text label).
- [ ] 🔴 MUST: All UI is usable when the browser/OS text size is increased to 200% — no content is cut off or overlapping.
- [ ] 🟡 SHOULD: Focus indicators (keyboard focus rings) are visible and have a contrast ratio of at least **3:1**.
- [ ] 🟡 SHOULD: All images have descriptive `alt` text. Decorative images have `alt=""`.
- [ ] 🟢 NICE: Dark mode is supported and all accessibility criteria still pass in dark mode.

### C.2 Screen Reader & Keyboard Accessibility

- [ ] 🔴 MUST: Every interactive element (buttons, links, form fields) is reachable and operable using only a keyboard (Tab, Enter, Space, arrow keys).
- [ ] 🔴 MUST: Screen readers (VoiceOver on iOS/macOS, TalkBack on Android, NVDA/JAWS on Windows) can read all meaningful content in logical order.
- [ ] 🔴 MUST: All form fields have a visible label associated via `<label>` or `aria-label`. Placeholder text alone is NOT a label.
- [ ] 🔴 MUST: Error messages are announced to screen readers automatically when they appear (not just shown visually).
- [ ] 🟡 SHOULD: Modal dialogs trap focus inside them when open and return focus to the trigger element when closed.
- [ ] 🟡 SHOULD: Skip-navigation link is present at the top of each web page (lets keyboard users jump past repetitive navigation).
- [ ] 🟢 NICE: ARIA live regions are used to announce dynamic content updates (e.g., new AI response appearing).

### C.3 Motion & Sensory

- [ ] 🟡 SHOULD: Animations and transitions respect the user's OS-level "Reduce Motion" setting.
- [ ] 🟡 SHOULD: No content flashes more than 3 times per second (prevents seizure risk).
- [ ] 🟢 NICE: Video content includes closed captions or subtitles.

### C.4 Accessibility Testing

| Method | Tool / Standard | Completed? |
|--------|-----------------|------------|
| Automated scan | `[REPLACE: e.g., axe DevTools, Lighthouse, Wave]` | `[ ]` |
| Manual keyboard navigation test | Test with Tab / Shift+Tab / Enter / Space | `[ ]` |
| Screen reader test (web) | `[REPLACE: e.g., NVDA + Firefox, VoiceOver + Safari]` | `[ ]` |
| Screen reader test (mobile) | `[REPLACE: e.g., VoiceOver (iOS), TalkBack (Android)]` | `[ ]` |
| Colour contrast audit | `[REPLACE: e.g., Colour Contrast Analyser, axe]` | `[ ]` |

---

## 🌍 APPENDIX D: Localisation / Internationalisation (i18n) Checklist
> *Localisation means adapting your product for different languages, countries, and cultures.*
> *i18n is the technical term (the "18" stands for the 18 letters between "i" and "n" in "internationalisation").*
>
> 🧠 **Think of it like:** Translating a menu at a restaurant, but also making sure the prices are in the right
> currency and the dates are in the right format for each country.

> 💡 **Tip:** Only complete this appendix for features that will be used in multiple countries or languages.
> If your product is English-only for now, you can keep this as a future planning checklist.

### D.1 Text & Content

- [ ] 🔴 MUST: All user-facing strings are stored in a translation file (e.g., `en.json`, `es.json`) — no hard-coded text in the UI code.
- [ ] 🔴 MUST: The UI layout handles text expansion gracefully — some languages (e.g., German) are 30–40% longer than English. Nothing is cut off.
- [ ] 🔴 MUST: Right-to-left (RTL) languages (Arabic, Hebrew) are supported in layout if those markets are targeted.
- [ ] 🟡 SHOULD: Translated strings have been reviewed by a native speaker, not just Google Translate.
- [ ] 🟡 SHOULD: AI-generated content is in the user's preferred language — Claude is prompted to respond in `[user's language]`.

### D.2 Dates, Numbers & Currency

- [ ] 🔴 MUST: Dates are displayed in the user's local format (e.g., `MM/DD/YYYY` for US, `DD/MM/YYYY` for UK, `YYYY-MM-DD` for ISO).
- [ ] 🔴 MUST: Currency amounts are shown in the user's local currency with the correct symbol and decimal format.
- [ ] 🟡 SHOULD: Numbers use the local thousands separator (e.g., `1,000` in US vs `1.000` in Germany).
- [ ] 🟡 SHOULD: Phone number fields accept international formats.

### D.3 Supported Languages (for this feature)

| Language | Locale Code | Status | Translator / Owner |
|----------|-------------|--------|--------------------|
| English (US) | `en-US` | ✅ Default | `[REPLACE]` |
| `[REPLACE: e.g., Spanish]` | `[e.g., es-ES]` | `☐ Planned` / `☑ Done` | `[REPLACE]` |
| `[REPLACE]` | `[REPLACE]` | `☐ Planned` / `☑ Done` | `[REPLACE]` |

### D.4 Localisation Testing

- [ ] Feature has been tested in at least `[REPLACE: e.g., 2]` non-English languages before GA.
- [ ] All UI strings display correctly with no truncation, overlap, or `[missing_key]` errors in any tested language.
- [ ] Date and currency formatting is correct for each tested locale.
- [ ] AI responses are correctly generated in the user's selected language.

---

## ⚡ APPENDIX E: Performance & Load Testing SLAs
> *Performance criteria define HOW FAST and HOW RELIABLY your product must work.*
> *SLA stands for "Service Level Agreement" — it's a promise about performance that you make to your users.*
>
> 🧠 **Think of it like:** A pizza delivery guarantee. "30 minutes or it's free" is an SLA.
> If the pizza takes 45 minutes, you've broken your promise.

> 💡 **Tip:** Fill in the targets that matter for your product. Leave the rest as placeholders.

### E.1 Page & Screen Load Times

| Page / Screen | Target Load Time | Measurement Method | Priority |
|---------------|-----------------|-------------------|---------|
| App home / dashboard | `[REPLACE: e.g., ≤ 2.5 seconds]` | Lighthouse / WebPageTest | 🔴 MUST |
| Login / sign-up flow | `[REPLACE: e.g., ≤ 1.5 seconds]` | Lighthouse | 🔴 MUST |
| AI response — first token visible | `[REPLACE: e.g., ≤ 1.5 seconds]` | Custom timer in code | 🔴 MUST |
| AI response — full completion | `[REPLACE: e.g., ≤ 8 seconds]` for ≤500 word response | Custom timer | 🟡 SHOULD |
| Data-heavy screen (lists, tables) | `[REPLACE: e.g., ≤ 3 seconds]` | Browser DevTools | 🟡 SHOULD |
| Mobile (low-end device, 4G) | All of the above + `[REPLACE: 20% buffer]` | Real device testing | 🟡 SHOULD |
| `[REPLACE: Custom screen]` | `[Target]` | `[Method]` | 🔴 / 🟡 / 🟢 |

### E.2 API Response Time SLAs

| Endpoint / API | Target p95 Response Time | Target p99 | Priority |
|---------------|--------------------------|------------|---------|
| `POST /auth/login` | `[REPLACE: e.g., ≤ 300ms]` | `[REPLACE: e.g., ≤ 800ms]` | 🔴 MUST |
| `GET /users/me` | `[REPLACE: e.g., ≤ 100ms]` | `[REPLACE: e.g., ≤ 300ms]` | 🔴 MUST |
| `POST /ai/chat` (Claude API call) | `[REPLACE: e.g., ≤ 2000ms]` | `[REPLACE: e.g., ≤ 5000ms]` | 🟡 SHOULD |
| `[REPLACE: Custom endpoint]` | `[Target]` | `[Target]` | 🔴 / 🟡 / 🟢 |

> 💡 **p95 / p99 explained:** p95 means "95% of requests are faster than this." p99 means "99% of requests are faster than this." These are better measures than "average" because the average hides slow outliers.

### E.3 Availability & Uptime

| Metric | Target | Notes |
|--------|--------|-------|
| **Uptime (monthly)** | `[REPLACE: e.g., 99.9% = allows ~43 mins downtime/month]` | Measured by uptime monitor (e.g., Pingdom, Better Uptime) |
| **Planned maintenance window** | `[REPLACE: e.g., Sundays 2–4 AM UTC]` | Notify users 24 hours in advance |
| **Recovery Time Objective (RTO)** | `[REPLACE: e.g., "Service restored within 1 hour of outage"]` | How fast can we recover? |
| **Recovery Point Objective (RPO)** | `[REPLACE: e.g., "No more than 1 hour of data loss"]` | How much data can we afford to lose? |

### E.4 Load & Stress Testing

| Scenario | Target | Tool | Tested? |
|----------|--------|------|---------|
| Normal load | `[REPLACE: e.g., 500 concurrent users]` — system responds within SLA | `[REPLACE: e.g., k6, Locust, JMeter]` | `[ ]` |
| Peak / launch day load | `[REPLACE: e.g., 2,000 concurrent users]` — no errors, graceful degradation if over capacity | Same tool | `[ ]` |
| AI endpoint under load | `[REPLACE: e.g., 100 simultaneous Claude API calls]` — rate limiting and queuing work correctly | Custom script | `[ ]` |
| Database under load | `[REPLACE: e.g., 10,000 reads/sec]` — query times stay within p95 SLA | `[REPLACE: e.g., pgbench]` | `[ ]` |

### E.5 Performance Monitoring (Ongoing — post-launch)

- [ ] 🔴 MUST: Real User Monitoring (RUM) is set up to measure actual load times for real users post-launch.
- [ ] 🔴 MUST: Alerts fire automatically if p95 API response time exceeds the SLA target for more than `[REPLACE: e.g., 5 minutes]`.
- [ ] 🟡 SHOULD: A performance budget is set — no new code is merged if it causes page load time to increase by more than `[REPLACE: e.g., 10%]`.
- [ ] 🟡 SHOULD: Claude API token usage is monitored per user per day to control costs and detect abuse.
- [ ] `[REPLACE: Add your own monitoring criterion]`

**Monitoring tool(s) used:** `[REPLACE: e.g., "Datadog, Sentry, New Relic, CloudWatch"]`

---

*© Template created for AI-Driven Development Life Cycle — reusable across all projects.*  
*Maintained by: `[REPLACE: Your team or company name]`*
