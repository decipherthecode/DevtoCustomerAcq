# 📖 How to Fill This User Story Template

> **Who is this for?** Anyone on the team — designer, developer, AI agent, tester, or even a first-time contributor.
> **Goal:** Make sure *every single person* (and every AI tool) knows exactly what to build, why to build it, and how to know when it is finished.

---

## 🧭 Before You Start: Read This First

A **User Story** answers three simple questions:

| Question | Example |
|---|---|
| **WHO** needs something? | "A new customer visiting for the first time" |
| **WHAT** do they want to do? | "Sign up with their email" |
| **WHY** does it matter to them? | "So they can save their progress and come back later" |

One story = one small piece of working software that delivers real value to a real person. If your story feels too big (takes longer than one sprint ≈ 2 weeks), split it into smaller stories.

---

## ✏️ Step-by-Step Filling Guide

| Step | Section | Time needed | Tip |
|---|---|---|---|
| 1 | Quick Info | 2 min | Copy the Story ID from your backlog |
| 2 | Story Statement | 5 min | Read it aloud — if it sounds weird, rewrite it |
| 3 | Background | 5 min | Pretend you're explaining it to a friend |
| 4 | INVEST Check | 2 min | If you check fewer than 5 boxes, rewrite first |
| 5 | Acceptance Criteria | 10 min | Start with the happy path, then add "what if…" scenarios |
| 6 | AI Instructions | 5 min | Fill in only the AI tools your team uses |
| 7 | Design & Tech Notes | 5 min | Links to Figma/designs or technical constraints |
| 8 | Sprint Planning | 2 min | Use the table — every field matters for AI agents |
| 9 | Security & Compliance | 5 min | Fill every row — skip nothing even if "N/A" |
| 10 | QA Notes | 5 min | List the test cases so the QA AI agent can auto-generate them |
| 11 | Definition of Done | 1 min | Tick boxes as you complete each one |
| 12 | Post-Launch Tracking | 5 min | Fill this *before* you build, not after |

### 📄 Template Variants (at the end of this file)

| Variant | When to use it |
|---|---|
| **Standard User Story** | A new feature or improvement — use the main template above |
| **Bug Report Story** | A defect found in production or testing — use the Bug variant |
| **Spike / Research Story** | Time-boxed investigation with no code shipped — use the Spike variant |

---

## 🔑 Glossary (Plain English)

| Term | Plain English Meaning |
|---|---|
| **User Story** | A short description of a feature, written from the user's point of view |
| **Epic** | A big theme that groups many small stories together |
| **Acceptance Criteria (AC)** | The checklist that proves the story is done |
| **Gherkin** | A way to write AC in "Given / When / Then" sentences |
| **Story Points** | A number that shows how hard a story is (1 = easy, 13 = very hard) |
| **P0 / P1 / P2 / P3** | Priority levels — P0 means "drop everything, fix this now" |
| **Sprint** | A fixed work period, usually 2 weeks |
| **Feature Flag** | A switch that turns a feature ON or OFF without redeploying code |
| **DoD** | Definition of Done — the final checklist before calling a story complete |
| **KPI** | A number you track to see if the feature is working (e.g. "500 sign-ups in 30 days") |
| **Observability** | Logs, dashboards, and alerts that let you see what the app is doing in real time |
| **INVEST** | A quality checklist for user stories (see Section 4 below) |
| **AI Agent** | An AI tool (like Claude, Cursor, Copilot) that can read this story and act on it |

---
---

# 🗂️ USER STORY

<!-- ════════════════════════════════════════════════════
     HOW TO USE: Copy everything below this line into a
     new file named  US-XXX-short-title.md  for each story.
     Replace every [PLACEHOLDER] with your real content.
     Delete any section that does not apply.
═════════════════════════════════════════════════════ -->

---

# [US-XXX] 📝 Story Title — Write a Short, Action-Oriented Title Here

> **💡 Naming Tip:** Use the format `Verb + Noun` — e.g. *"Reset Password via Email"* or *"Export Invoice as PDF"*.
> Keep it under 10 words. Avoid vague words like "improve", "fix", or "update".

---

## 1️⃣ Quick Info

> **💡 Filling Tip:** Fill every row. Blank fields confuse AI agents and create delays during sprint planning.

| Field | Your Answer |
|---|---|
| **Story ID** | `US-XXX` ← Replace XXX with the next number in your backlog |
| **Epic** | [Name of the larger theme this story belongs to, e.g. "User Onboarding"] |
| **Feature Area** | [e.g. Authentication / Dashboard / Payments / Notifications] |
| **Platform** | ☐ Web App &nbsp;&nbsp; ☐ iOS &nbsp;&nbsp; ☐ Android &nbsp;&nbsp; ☐ All Platforms |
| **Created By** | [Your full name or @handle] |
| **Date Created** | [YYYY-MM-DD] |
| **Last Updated** | [YYYY-MM-DD] |
| **Story Version** | v1.0 ← Increment each time you make a significant change |
| **Status** | ☐ Draft &nbsp;&nbsp; ☐ In Refinement &nbsp;&nbsp; ☐ Ready for Dev &nbsp;&nbsp; ☐ In Progress &nbsp;&nbsp; ☐ In Review &nbsp;&nbsp; ☐ Done |
| **Assigned AI Agent(s)** | ☐ Code Gen &nbsp;&nbsp; ☐ QA Agent &nbsp;&nbsp; ☐ PM Agent &nbsp;&nbsp; ☐ DevOps Agent |

---

## 2️⃣ Sprint Planning

> **💡 Filling Tip:** These four fields drive your sprint board and velocity tracking.
> Fill them during **Backlog Refinement** with the whole team.

| Field | Your Answer | Options / Examples |
|---|---|---|
| **Priority** | [P?] | `P0` = Fix right now (system is broken) · `P1` = This sprint · `P2` = Next sprint · `P3` = Backlog |
| **Story Points** | [?] | Fibonacci: `1` · `2` · `3` · `5` · `8` · `13` — if >8, split the story |
| **Sprint / Milestone** | [Sprint # or Milestone name] | e.g. "Sprint 4" or "Beta Launch – Nov 2026" |
| **Target Release** | [vX.X.X or date] | e.g. "v1.2.0" or "2026-12-01" |

### Dependencies

> **💡 Filling Tip:** A story **blocks** another if that other story cannot start until this one is done.
> A story is **blocked by** another if it cannot start until the other is done.

| Relationship | Story ID | Short description of why |
|---|---|---|
| ⛔ **Blocks** | `US-XXX` | [What cannot start until this story is done?] |
| ⛔ **Blocked by** | `US-XXX` | [What must finish before this story can start?] |
| 🔗 **Related to** | `US-XXX` | [Similar or overlapping stories worth knowing about] |

---

## 3️⃣ The User Story Statement

> **💡 Filling Tip:** This is the most important sentence in the whole document.
> Read it aloud. If a 10-year-old would understand who, what, and why — you're done.
> **Do NOT mention technology** here (no "API", "database", "React"). Keep it human.

```
As a     [WHO — describe the type of user, e.g. "a first-time visitor",
                 "a logged-in team admin", "a mobile user on a slow connection"],

I want   [WHAT — the action or goal, e.g. "to reset my password using my email address"],

so that  [WHY / BENEFIT — the real value, e.g. "I can get back into my account
                           without contacting support"].
```

**Filled-in example (delete this before using):**
> As a **first-time customer who forgot their password**,
> I want to **receive a password-reset link in my email**,
> so that **I can regain access to my account in under 2 minutes, on my own**.

---

## 4️⃣ Background & Context

> **💡 Filling Tip:** Imagine you are handing this story to someone who has never heard of your product.
> Give them enough context to understand *why this matters* without a meeting.

### 4a. Why Does This Story Exist?

[Write 2–4 sentences explaining the problem this story solves. What is broken, missing, or painful for the user right now?]

**Example:** *"Currently, users who forget their password have no self-service recovery option. They must email support, wait up to 48 hours, and then manually reset their credentials. This creates churn at the top of the funnel and costs the support team ~15 hours per week."*

### 4b. User Persona

> **💡 Filling Tip:** Be specific. "Any user" is not a persona.

| Field | Answer |
|---|---|
| **Who are they?** | [Job title, role, or description — e.g. "Solo founder, non-technical, age 28–45"] |
| **Technical level** | ☐ Beginner (needs hand-holding) &nbsp; ☐ Intermediate &nbsp; ☐ Advanced (power user) |
| **Device they use most** | ☐ Desktop browser &nbsp; ☐ iPhone &nbsp; ☐ Android &nbsp; ☐ Tablet |
| **When does this problem hit them?** | [e.g. "On a Monday morning when they're rushing to log in"] |
| **How often do they face this?** | [e.g. "Once per month on average, but it feels catastrophic every time"] |

### 4c. Business & Product Impact

| Question | Answer |
|---|---|
| **What happens if we DON'T build this?** | [e.g. "~12% of new sign-ups never complete onboarding"] |
| **What OKR / goal does this support?** | [e.g. "Q4 OKR: Reduce onboarding drop-off by 20%"] |
| **Linked product requirement / PRD** | [Link or filename — e.g. `docs/PRD-Authentication.md`] |
| **Customer request / feedback link** | [Link to Intercom ticket, support thread, or research note] |

---

## 5️⃣ INVEST Quality Check

> **💡 What is INVEST?** It's a 6-point quality checklist invented in 2003. Every good story passes all 6.
> If your story fails any check, fix it **before** moving to Acceptance Criteria.
> (**Tip for beginners:** Read each question aloud and answer honestly. One word answers work fine.)

| ✅ | Letter | Question to ask yourself | Your quick answer |
|---|---|---|---|
| ☐ | **I — Independent** | Can this story be built without waiting for another unfinished story? | |
| ☐ | **N — Negotiable** | Are the details flexible (only the user goal is fixed)? | |
| ☐ | **V — Valuable** | Does a real user or the business get something useful from this? | |
| ☐ | **E — Estimable** | Does the team have enough info to put a number of story points on it? | |
| ☐ | **S — Small** | Can it be completed in one sprint (≤ 2 weeks)? If not → split it | |
| ☐ | **T — Testable** | Can we write a pass/fail test for each Acceptance Criterion? | |

**INVEST Score: [ ] / 6** — Target: 6/6 before the story is marked *Ready for Dev*.

---

## 6️⃣ Acceptance Criteria (AC)

> **💡 What is this section?** These are the rules. If the software meets every rule below, the story is done.
> We write them in **Gherkin** format: `Given` (starting condition) → `When` (action) → `Then` (result).
>
> **Rules for writing good AC:**
> - Write at least **3 scenarios**: Happy Path · Edge Case · Error State
> - Keep each `Then` statement **measurable** (not "it works" — say *exactly* what happens)
> - Avoid saying *how* to build it (no React, no SQL) — just what the user sees or experiences
> - Aim for **3–7 scenarios** per story. More than 7 = split the story.

---

### ✅ Scenario 1 — Happy Path (Things Go Right)

> *The most common, successful flow. Always write this one first.*

```gherkin
Feature: [Short feature name — e.g. "Password Reset"]

  Scenario: [Name this scenario — e.g. "User successfully resets password via email"]
    Given [Starting condition — e.g. "the user is on the login page and has an existing account"]
    When  [Action taken — e.g. "they click 'Forgot Password' and enter their registered email"]
    Then  [Expected result — e.g. "a password-reset email is sent within 30 seconds"]
    And   [Additional result — e.g. "the email contains a link that expires in 60 minutes"]
    And   [Optional — e.g. "the user sees a confirmation message: 'Check your inbox'"]
```

---

### ⚠️ Scenario 2 — Edge Case (Unusual but Valid Situation)

> *What if the user does something valid but unusual? e.g. uses uppercase email, slow network, mobile device.*

```gherkin
  Scenario: [Name — e.g. "User enters email with uppercase letters"]
    Given [Starting condition]
    When  [Unusual but valid action — e.g. "they enter 'USER@EXAMPLE.COM' instead of 'user@example.com'"]
    Then  [Expected result — e.g. "the system treats it as case-insensitive and sends the reset email"]
```

---

### ❌ Scenario 3 — Error State (Things Go Wrong)

> *What does the user see when they do something wrong? The error message must be clear and helpful.*

```gherkin
  Scenario: [Name — e.g. "User enters an email that is not registered"]
    Given [Starting condition]
    When  [Wrong action — e.g. "they enter an email that does not exist in the system"]
    Then  [Expected error — e.g. "they see the message: 'No account found. Try a different email or sign up.'"]
    And   [e.g. "no email is sent — to prevent email enumeration attacks"]
```

---

### ➕ Scenario 4 — [Add more as needed]

> *Copy and paste a scenario block above. Common additional scenarios:*
> - *Mobile / small screen behavior*
> - *Accessibility (screen reader, keyboard-only navigation)*
> - *Slow network / timeout*
> - *Rate limiting (too many attempts)*
> - *Already-expired or already-used link*

```gherkin
  Scenario: [Name]
    Given [Condition]
    When  [Action]
    Then  [Result]
```

---

### 📋 Non-Functional Requirements (NFRs)

> **💡 What are NFRs?** Rules about *how* the system should behave — speed, security, accessibility — not *what* it does.

| # | Requirement | Measure |
|---|---|---|
| NFR-1 | **Performance** | [e.g. "The reset email must be sent within 30 seconds of the request, under normal load"] |
| NFR-2 | **Security** | [e.g. "Reset links must be single-use tokens, expire in 60 min, and use HTTPS only"] |
| NFR-3 | **Accessibility** | [e.g. "All form fields must have visible labels and pass WCAG 2.1 AA contrast ratio"] |
| NFR-4 | **Mobile** | [e.g. "The reset flow must work on screens as small as 375px (iPhone SE)"] |
| NFR-5 | **Localization** | [e.g. "Error messages must support English and French at launch"] |

---

## 7️⃣ 🤖 AI Agent Instructions

> **💡 What is this section?** This section is written *for the AI tools* on your team — not for humans.
> Think of it as giving a very precise briefing to a robot colleague.
> Fill in only the AI roles that apply to this story (delete the rest).

---

### 🔵 For the AI Code Generator (Claude / Cursor / Copilot)

> **Role:** Reads this story and writes or reviews code accordingly.

```
STORY CONTEXT FOR CODE GENERATION:
- Story ID      : US-XXX
- Story Title   : [Paste the story title]
- Platform      : [Web App / iOS / Android / All]
- Story Statement: As a [WHO], I want [WHAT], so that [WHY].

IMPLEMENTATION SCOPE:
- Build only what the Acceptance Criteria describe. Nothing more.
- Do NOT add unrequested features ("gold plating").
- Platform-specific notes: [e.g. "On mobile: use bottom sheet for the reset form. On web: use modal dialog."]
- Files likely to be created or modified: [e.g. "auth/reset-password.ts, components/ResetModal.tsx"]
- Known constraints: [e.g. "Must use the existing email service (SendGrid). No new dependencies without PM approval."]
- Edge cases to handle in code: [List the edge case scenarios from Section 6]

DEFINITION OF DONE FOR CODE:
- All Acceptance Criteria scenarios pass
- TypeScript / linting errors: zero
- Tests written for each scenario
- No hardcoded credentials or secrets
```

---

### 🟢 For the AI QA / Test Generator Agent

> **Role:** Reads the Acceptance Criteria and auto-generates test cases, edge cases, and regression tests.

```
STORY CONTEXT FOR QA:
- Story ID     : US-XXX
- Story Title  : [Paste the story title]
- Platform     : [Web App / iOS / Android / All]
- AC Scenarios : [Count] scenarios defined in Section 6

TEST GENERATION INSTRUCTIONS:
- Generate test cases for every Gherkin scenario in Section 6 (happy path + edge + error).
- Add at least 2 additional edge cases not listed in Section 6 (think: rate limits, session expiry, concurrent requests).
- For mobile: test on minimum screen size 375px and on both iOS and Android gesture models.
- Regression areas to re-test when this story ships: [e.g. "Login flow, Sign-up flow, Session management"]
- Performance threshold: [e.g. "Email delivery p95 < 30 seconds"]
- Accessibility checks required: [e.g. "Screen reader labels, tab order, color contrast"]
- Security test cases: [e.g. "Attempt token replay, expired token use, cross-account token swap"]
- Test file location: [e.g. "tests/auth/reset-password.test.ts"]
```

---

### 🟡 For the AI PM / Story Writer Agent

> **Role:** Validates the story quality, checks INVEST compliance, and can help refine or split stories.

```
STORY REVIEW INSTRUCTIONS:
- Story ID     : US-XXX
- Review this story against the INVEST criteria (Section 5).
- Flag any Acceptance Criterion that is vague, unmeasurable, or implementation-specific.
- Check: is the story small enough for one sprint (≤ 8 story points)? If not, suggest a split.
- Check: are there missing edge cases in the AC?
- Suggest improvements to the Story Statement if the WHO, WHAT, or WHY is unclear.
- Output format: bullet list of issues found, followed by suggested rewrites.
```

---

### 🔴 For the AI DevOps / Release Agent

> **Role:** Handles CI/CD pipeline configuration, feature flag setup, deployment, and rollout decisions.

```
DEPLOYMENT INSTRUCTIONS:
- Story ID            : US-XXX
- Feature Flag name   : [e.g. "feature_password_reset_v2"] ← use snake_case
- Initial rollout     : [e.g. "5% of users — internal team + beta list only"]
- Full rollout target : [e.g. "100% after 72 hours with zero P0 incidents"]
- Rollback trigger    : [e.g. "If error rate > 2% or p95 latency > 5s for 10 minutes"]
- Environment order   : dev → staging → canary → production
- Required env vars   : [e.g. "SENDGRID_API_KEY, RESET_TOKEN_TTL_MINUTES"]
- Infrastructure changes: [e.g. "None — uses existing email service"]
- Post-deploy smoke test: [e.g. "Trigger one real reset email from staging; verify delivery < 30s"]
- Monitoring dashboard: [Link to Datadog / Grafana / CloudWatch panel]
```

---

## 8️⃣ Design & UX Notes

> **💡 Filling Tip:** Paste links to Figma or screenshots. Describe anything that differs between Web and Mobile.
> The goal: a developer should never have to *guess* what something looks like.

| Field | Answer |
|---|---|
| **Figma / Design Link** | [URL to the exact frame or prototype] |
| **Design Status** | ☐ Not started &nbsp; ☐ Wireframe only &nbsp; ☐ High-fidelity ready &nbsp; ☐ Approved |
| **Brand / Style Guide** | [Link or filename] |

### Web App — Specific Notes

> *Breakpoints, modals, keyboard behavior, hover states, browser compatibility.*

- **Layout:** [e.g. "Centered modal on desktop (max-width 480px). Full-screen on screens < 768px."]
- **Keyboard navigation:** [e.g. "Tab order: Email field → Submit button → Cancel link"]
- **Loading state:** [e.g. "Show spinner on Submit button; disable button while request is in-flight"]
- **Browser support:** [e.g. "Chrome 100+, Firefox 110+, Safari 16+, Edge 100+"]
- **Empty states / zero data:** [e.g. "N/A for this story"]

### Mobile App — Specific Notes

> *iOS vs Android differences, gestures, bottom sheets, system notifications.*

- **iOS:** [e.g. "Use native UIAlertController for confirmation dialog. Support Face ID / Touch ID re-auth after reset."]
- **Android:** [e.g. "Use Material Design Bottom Sheet. Support biometric re-auth after reset."]
- **Gesture model:** [e.g. "Swipe-down to dismiss the reset sheet on both platforms"]
- **Offline behavior:** [e.g. "If offline, show: 'No internet connection. Try again when connected.'"]
- **Push notification:** [e.g. "Not applicable — only email is used for reset"]

### Accessibility (A11y)

- [ ] All form inputs have visible labels (not placeholder-only)
- [ ] Error messages are announced by screen readers (`role="alert"`)
- [ ] Color is not the only way to convey information
- [ ] Minimum tap target: 44×44pt (iOS) / 48×48dp (Android) / 44×44px (Web)
- [ ] WCAG 2.1 AA color contrast ratio met (4.5:1 for normal text)

---

## 9️⃣ Technical Notes

> **💡 Filling Tip:** This section is for developers and AI code agents.
> Write what constraints exist — not how to solve them. Let the engineer decide the solution.

| Field | Answer |
|---|---|
| **API contract / endpoints affected** | [e.g. "`POST /api/v1/auth/reset-request` — see `api/auth.yaml`"] |
| **Database changes required** | [e.g. "New `password_reset_tokens` table — see migration `0024_add_reset_tokens.sql`"] |
| **External services / 3rd parties** | [e.g. "SendGrid for email delivery; Twilio if we add SMS later"] |
| **Security considerations** | [e.g. "Tokens must be hashed (bcrypt) before storage. Never store plaintext."] |
| **Performance constraints** | [e.g. "Email queue must not block the main API thread — use background worker"] |
| **Known technical debt** | [e.g. "Current auth module lacks token expiry — must be added as part of this story"] |
| **Data privacy / GDPR notes** | [e.g. "Reset token logs must be deleted after 24 hours per data retention policy"] |
| **Mobile-specific** | [e.g. "Use Keychain (iOS) / Keystore (Android) for storing session token after reset"] |

---

## 🔟 QA & Testing Notes

> **💡 Filling Tip:** List what to test. The AI QA agent will use this to auto-generate test scripts.
> Think: "What could go wrong?" and "What does the QA agent need to know that isn't in the AC?"

### Test Environments

| Environment | URL / Endpoint | Test Credentials |
|---|---|---|
| Development | [URL] | [Link to secure credential store — never write passwords here] |
| Staging | [URL] | [Link to secure credential store] |
| Mobile (Device/Emulator) | [Device model or emulator spec] | [Link to secure credential store] |

### Test Cases Checklist

> *(AI QA Agent: expand each item below into a full test script)*

- [ ] **TC-1 — Happy Path:** User receives reset email within 30 seconds
- [ ] **TC-2 — Invalid Email:** User sees helpful error message; no email sent
- [ ] **TC-3 — Case-Insensitive Email:** Uppercase email is treated the same as lowercase
- [ ] **TC-4 — Expired Token:** User clicks link after 60 min → sees "link expired" page
- [ ] **TC-5 — Already-Used Token:** Second click on the same link → shows "link already used"
- [ ] **TC-6 — Rate Limiting:** 5 failed attempts in 10 min → user is temporarily blocked
- [ ] **TC-7 — Mobile Web (iOS Safari):** Full flow works on iPhone with iOS Safari
- [ ] **TC-8 — Mobile App (Android):** Full flow works on Android 13+ native app
- [ ] **TC-9 — Slow Network (3G simulation):** Graceful loading state; no silent failure
- [ ] **TC-10 — Accessibility:** Screen reader announces all states correctly
- [ ] **TC-[N] — Add more:** [Describe additional test]

### Regression Areas

> *What existing features must be re-tested to make sure this story didn't break them?*

- [ ] [e.g. "Login flow — standard username/password"]
- [ ] [e.g. "Sign-up flow — new account creation"]
- [ ] [e.g. "Session persistence — user stays logged in after tab refresh"]
- [ ] [Add more as needed]

---

## 1️⃣1️⃣ Definition of Done (DoD)

> **💡 What is this?** The final checklist. The story is ONLY done when every box is ticked.
> "Almost done" is not done. "Works on my machine" is not done.

### Code & Development
- [ ] All Acceptance Criteria scenarios from Section 6 pass
- [ ] Code reviewed and approved by at least one other developer (or AI Code Review agent)
- [ ] No linting errors, no TypeScript errors, no console errors
- [ ] No hardcoded secrets, API keys, or environment-specific values in code
- [ ] Code merged to the `main` / `develop` branch via pull request

### Testing
- [ ] All test cases from Section 10 pass in staging
- [ ] All regression tests pass
- [ ] Tested on both Web (desktop + mobile browser) and Native Mobile (iOS + Android)
- [ ] Accessibility checks from Section 8 pass
- [ ] Performance thresholds from NFRs pass under simulated load

### Design & UX
- [ ] UI matches the approved Figma design (pixel-perfect or signed off by designer)
- [ ] Mobile and Web layouts both verified against designs
- [ ] All empty states, loading states, and error states are implemented and match designs

### AI Agents Sign-Off
- [ ] AI Code Generator has reviewed the implementation against the story
- [ ] AI QA Agent has run all generated test cases and they pass
- [ ] AI DevOps Agent has confirmed feature flag and deployment config is ready
- [ ] AI PM Agent has validated the story against INVEST and AC coverage

### Documentation & Observability
- [ ] Feature flag created and confirmed OFF in production (for gradual rollout)
- [ ] Monitoring dashboard updated with new metrics for this feature
- [ ] Alerts configured per Section 12 (Observability)
- [ ] In-app help / tooltip text updated if the UI changed
- [ ] Changelog / release notes entry written

### Stakeholder Sign-Off
- [ ] Product Manager (or Story Owner) has verified all AC in staging
- [ ] Story status changed to **Done** in the backlog

---

## 1️⃣2️⃣ Rollout Plan

> **💡 Why do this?** Shipping to all users at once is risky.
> A phased rollout means if something goes wrong, only a small % of users are affected.

| Phase | Who sees it | When | Condition to advance |
|---|---|---|---|
| **Phase 0 — Internal** | Dev team + QA only (0.1%) | Day 0 — deploy to production | Zero P0 bugs in 24 hours |
| **Phase 1 — Beta** | Invited beta users (5%) | Day 1–3 | Error rate < 1%, positive feedback |
| **Phase 2 — Ramp** | 25% of all users | Day 4–7 | KPIs trending toward targets |
| **Phase 3 — General** | 100% of users | Day 8+ | All success metrics met |
| **Rollback trigger** | — | Any phase | Error rate > 2% OR p95 latency > [X]s for 10 min |

**Feature Flag name:** `[feature_name_here]`
**Flag tool used:** [e.g. LaunchDarkly / Flagsmith / Custom / Environment variable]

---

## 1️⃣3️⃣ Observability & Alerts

> **💡 Filling Tip:** "Observability" means: if something breaks at 3am, your monitoring system wakes someone up.
> Fill this BEFORE shipping. It's much harder to add after.

### Metrics to Track

| Metric | What it measures | Alert threshold | Dashboard link |
|---|---|---|---|
| `reset_email_sent_total` | How many reset emails were triggered | — | [Link] |
| `reset_email_delivery_p95_seconds` | How long email delivery takes at the 95th percentile | Alert if > 30s | [Link] |
| `reset_link_clicked_rate` | % of sent emails where user clicked the link | Alert if < 40% | [Link] |
| `reset_token_error_rate` | % of reset attempts that fail | Alert if > 2% | [Link] |
| `reset_flow_completion_rate` | % of users who complete the full reset | Track for KPI | [Link] |
| [Add metric] | [Description] | [Threshold] | [Link] |

### Log Events (for AI DevOps Agent to implement)

```
Events to emit:
- password_reset_requested  { user_id, email_hash, timestamp, platform }
- reset_email_sent          { user_id, email_hash, timestamp, delivery_ms }
- reset_link_clicked        { user_id, token_id, timestamp }
- reset_completed           { user_id, timestamp, platform }
- reset_token_expired       { user_id, token_id, timestamp }
- reset_rate_limit_hit      { ip_address, timestamp }
```

### Alert Rules

| Alert | Condition | Severity | Who gets notified |
|---|---|---|---|
| High error rate | `reset_token_error_rate` > 2% for 10 min | 🔴 P1 | On-call engineer |
| Slow email delivery | p95 delivery > 30s for 5 min | 🟡 P2 | On-call engineer |
| Zero completions | 0 `reset_completed` events in 1 hour during business hours | 🟡 P2 | PM + On-call |

---

## 1️⃣4️⃣ Success Metrics & KPIs

> **💡 Why this matters:** Success Metrics tell you if the feature actually solved the user's problem.
> Define them BEFORE building. Otherwise you won't know if it worked.

| KPI | Target | Measured how | Time frame | Status |
|---|---|---|---|---|
| **Primary — Feature Adoption** | [e.g. "≥ 80% of users who hit 'Forgot Password' complete the reset flow"] | Funnel analytics | First 30 days post-launch | ⬜ Not started |
| **Customer Satisfaction** | [e.g. "Support tickets tagged 'can't log in' drop by 50%"] | Support dashboard | 30 days post-launch | ⬜ Not started |
| **Performance** | [e.g. "Reset email delivered in < 30s for 95% of requests"] | APM / observability | Ongoing | ⬜ Not started |
| **Error Rate** | [e.g. "< 1% of reset attempts end in an unhandled error"] | Error monitoring | Ongoing | ⬜ Not started |
| **Journey to 500 Customers** | [e.g. "This story is a blocker for onboarding — removing it unblocks 12% of stuck users"] | Funnel analytics | Until customer 500 | ⬜ Not started |
| [Add KPI] | [Target] | [How] | [When] | ⬜ Not started |

### 🎯 Milestone: First 500 Customers

> *Track these milestones from launch to your first 500 customers using this product feature.*

| Milestone | Target date | Status | Notes |
|---|---|---|---|
| Feature shipped to 100% of users | [Date] | ⬜ | |
| First 100 customers use this feature | [Date] | ⬜ | |
| First 250 customers use this feature | [Date] | ⬜ | |
| First 500 customers use this feature | [Date] | ⬜ | |
| Feature learnings documented | [Date] | ⬜ | |

---

## 1️⃣4️⃣b 🔒 Security & Compliance

> **💡 Why this matters:** Security and compliance issues caught in a story cost 10x less to fix than issues found in production.
> Fill every row — even if the answer is "N/A", writing it proves you thought about it.

### Privacy & Data

| Field | Answer |
|---|---|
| **Does this story collect new personal data?** | ☐ Yes &nbsp; ☐ No — If Yes, describe what data: [e.g. "email address for password reset"] |
| **Is any personal data stored?** | ☐ Yes &nbsp; ☐ No — If Yes: where, for how long, and under what encryption? |
| **Is this feature subject to GDPR / CCPA / PIPEDA?** | ☐ Yes &nbsp; ☐ No &nbsp; ☐ Unsure — loop in Legal |
| **Right to deletion — does this data need a delete path?** | ☐ Yes &nbsp; ☐ No &nbsp; ☐ Handled elsewhere (link: ) |
| **Consent required before collecting data?** | ☐ Yes &nbsp; ☐ No |

### Authentication & Authorization

| Field | Answer |
|---|---|
| **Who is allowed to trigger this feature?** | [e.g. "Any authenticated user / Admin only / Public"] |
| **What happens if an unauthenticated user hits this endpoint?** | [e.g. "Return 401 Unauthorized — redirect to login page"] |
| **Are there role-based access controls (RBAC) to enforce?** | ☐ Yes &nbsp; ☐ No — If Yes: [describe roles] |
| **Can one user access another user's data through this feature?** | ☐ Yes (risk — block this) &nbsp; ☐ No |

### Security Threat Model

> *Think like an attacker for 5 minutes. What could go wrong?*

| Threat | Mitigation | Owner |
|---|---|---|
| [e.g. "Token replay — attacker reuses a stolen reset link"] | [e.g. "Tokens are single-use; mark as consumed on first click"] | [Dev name] |
| [e.g. "Email enumeration — attacker discovers which emails are registered"] | [e.g. "Return the same response regardless of whether email exists"] | [Dev name] |
| [e.g. "Brute-force token guessing"] | [e.g. "Rate-limit to 5 attempts per IP per 10 minutes"] | [Dev name] |
| [Add threat] | [Mitigation] | [Owner] |

### Compliance Checklist

| Standard | Applies? | Notes / Evidence |
|---|---|---|
| **GDPR (EU)** | ☐ Yes &nbsp; ☐ No &nbsp; ☐ N/A | [e.g. "Data processed under legitimate interest — no additional consent needed"] |
| **CCPA (California)** | ☐ Yes &nbsp; ☐ No &nbsp; ☐ N/A | |
| **SOC 2 Type II** | ☐ Yes &nbsp; ☐ No &nbsp; ☐ N/A | [e.g. "Audit log of all reset events required by CC7.2"] |
| **HIPAA** | ☐ Yes &nbsp; ☐ No &nbsp; ☐ N/A | |
| **PCI-DSS** | ☐ Yes &nbsp; ☐ No &nbsp; ☐ N/A | |
| **WCAG 2.1 AA** | ☐ Yes &nbsp; ☐ No &nbsp; ☐ N/A | [Accessibility — always Yes for customer-facing features] |
| **Legal / ToS review required?** | ☐ Yes &nbsp; ☐ No | [e.g. "No new terms introduced by this story"] |

---

## 1️⃣5️⃣ Customer Feedback Loop

> **💡 Why this matters:** The first real users will find problems you didn't predict.
> This section captures those learnings so the story can be improved or a follow-up story created.

### Feedback Collection Methods

- [ ] **In-app prompt:** [e.g. "Show a 1–5 star rating prompt after the user completes the reset flow — once per user"]
- [ ] **Support ticket tagging:** [e.g. "All Intercom tickets tagged with `password-reset` are reviewed weekly"]
- [ ] **Analytics funnel:** [e.g. "Review drop-off points in the reset funnel every sprint"]
- [ ] **User interviews:** [e.g. "Interview 5 users who dropped off in Phase 1 rollout"]

### Feedback Log

> *Add a new row each time a significant piece of feedback is received.*

| Date | Source | Customer segment | Feedback summary | Action taken | Follow-up story? |
|---|---|---|---|---|---|
| [YYYY-MM-DD] | [Intercom / Interview / Analytics] | [e.g. "Mobile, first-time user"] | [Summary] | [e.g. "Fixed in PR #123"] | [US-XXX / None] |

### Lessons Learned (fill after reaching 500 customers)

> *After 500 customers have used this feature, write 3–5 sentences here about what worked, what didn't, and what you'd do differently.*

[Write your reflection here after launch.]

---

## 1️⃣6️⃣ Open Questions & Risks

> **💡 Filling Tip:** If you're unsure about something, write it here so the team can discuss it.
> Don't leave questions hidden in Slack threads. Unresolved questions = bugs and missed deadlines.

| # | Question / Risk | Owner | Due date | Status |
|---|---|---|---|---|
| Q1 | [e.g. "Do we send an email if the account is locked? Or silently fail?"] | [PM name] | [Date] | ⬜ Open |
| Q2 | [e.g. "Should we support SMS as an alternative reset method in v1?"] | [PM name] | [Date] | ⬜ Open |
| R1 | **Risk:** [e.g. "SendGrid has a 99.5% SLA — if it's down, no resets work. Mitigation: fallback to Mailgun?"] | [Dev name] | [Date] | ⬜ Open |

---

## 1️⃣7️⃣ Revision History

> **💡 Filling Tip:** Every time you make a significant change to this story, add a row here.
> This helps the team understand *why* the story changed and prevents re-work.

| Version | Date | Changed by | What changed | Reason |
|---|---|---|---|---|
| v1.0 | [YYYY-MM-DD] | [Name] | Initial draft | Story created |
| v1.1 | [YYYY-MM-DD] | [Name] | [e.g. "Added Scenario 4 for rate limiting"] | [e.g. "Security review flagged this gap"] |
| v2.0 | [YYYY-MM-DD] | [Name] | [Major change description] | [Reason] |

---

<!-- ════════════════════════════════════════════════════
     END OF STANDARD STORY TEMPLATE
     Filename convention: US-XXX-short-title.md
     e.g. US-042-reset-password-via-email.md
═════════════════════════════════════════════════════ -->

---
---

# 🐛 VARIANT A — BUG REPORT STORY

<!-- ════════════════════════════════════════════════════
     USE THIS VARIANT when a defect is found in production
     or testing that needs to be tracked as a story.
     Filename convention: BUG-XXX-short-description.md
     e.g. BUG-017-reset-link-not-expiring.md
═════════════════════════════════════════════════════ -->

> **💡 When to use this:** A bug is unexpected behavior that broke something that was previously working.
> If it's brand-new behavior that was never built, use the standard User Story template instead.

---

# [BUG-XXX] 🐛 Bug Title — Short Description of What Is Broken

---

## Quick Info

| Field | Your Answer |
|---|---|
| **Bug ID** | `BUG-XXX` |
| **Related Story** | `US-XXX` ← The story that originally built this feature |
| **Severity** | ☐ S1-Critical (system down / data loss) &nbsp; ☐ S2-Major (core feature broken) &nbsp; ☐ S3-Minor (workaround exists) &nbsp; ☐ S4-Cosmetic |
| **Priority** | ☐ P0 &nbsp; ☐ P1 &nbsp; ☐ P2 &nbsp; ☐ P3 |
| **Platform affected** | ☐ Web &nbsp; ☐ iOS &nbsp; ☐ Android &nbsp; ☐ All |
| **Environment found in** | ☐ Development &nbsp; ☐ Staging &nbsp; ☐ Production |
| **First reported** | [YYYY-MM-DD] |
| **Reported by** | [Name / team / customer] |
| **Assigned to** | [Developer / AI Code Agent] |
| **Sprint** | [Sprint # or Milestone] |
| **Story Points** | [1 / 2 / 3 / 5 / 8] |
| **Status** | ☐ New &nbsp; ☐ Confirmed &nbsp; ☐ In Fix &nbsp; ☐ In Review &nbsp; ☐ Fixed &nbsp; ☐ Closed |

---

## 🔍 Bug Description

### What is happening? (Actual Behavior)

> *Describe exactly what the system does wrong. Be specific.*

[Write 2–4 sentences. e.g. "When a user clicks the password-reset link after 61 minutes, they see a generic 500 error page instead of a user-friendly 'Link expired' message."]

### What should happen instead? (Expected Behavior)

[Write 2–4 sentences. e.g. "The system should display a clear message: 'This link has expired. Request a new one.' with a button to restart the reset flow."]

---

## 🔁 Steps to Reproduce

> *Write these so precisely that a 10-year-old could follow them and see the bug every time.*

1. [e.g. "Open the app in an Incognito / Private browser window"]
2. [e.g. "Go to the login page and click 'Forgot Password'"]
3. [e.g. "Enter a valid registered email address and click 'Send Reset Link'"]
4. [e.g. "Wait 61 minutes (or manually expire the token in the database)"]
5. [e.g. "Click the link in the reset email"]
6. **→ Bug appears here:** [e.g. "A generic 500 error page loads instead of the expiry message"]

**Reproducibility:** ☐ Always &nbsp; ☐ Sometimes (___% of the time) &nbsp; ☐ Rarely &nbsp; ☐ Could not reproduce

---

## 📸 Evidence

| Type | Link / Description |
|---|---|
| **Screenshot / Screen recording** | [Link or drag-and-drop image here] |
| **Error log / Stack trace** | [Paste log excerpt or link to log dashboard] |
| **Browser / Device info** | [e.g. "Chrome 128 on macOS 14 / iPhone 15 iOS 18"] |
| **App version** | [e.g. "v1.3.2 (build 2024.10.13)"] |
| **User affected** | [e.g. "Specific user ID: U-10482 — anonymized OK for ticket"] |
| **Number of users affected** | [e.g. "Estimated 200 users in the last 7 days based on error logs"] |

---

## 🩺 Root Cause Analysis

> *Fill this after investigation — before writing the fix.*

| Field | Answer |
|---|---|
| **Root cause** | [e.g. "The token expiry check compares timestamps in different timezones (UTC vs. local). Off-by-one-hour error."] |
| **Why was this not caught in testing?** | [e.g. "The TC for expired tokens used a mocked clock that didn't simulate timezone differences"] |
| **Code location** | [e.g. "`src/auth/reset-token.ts` — line 142, `isTokenExpired()` function"] |
| **Regression risk** | [e.g. "Fix may affect other token-based flows: email verification, magic links"] |

---

## ✅ Fix Acceptance Criteria

```gherkin
Scenario: User is shown a clear message when clicking an expired reset link
  Given the user has a reset link that expired 1 minute ago
  When they click the link
  Then they see the message: "This link has expired. Request a new one."
  And they see a "Send new link" button
  And no 500 error page is shown

Scenario: Valid link still works after the fix
  Given the user has a reset link that is 30 minutes old (within the 60-min window)
  When they click the link
  Then they are taken to the password-reset form as before (regression check)
```

---

## 🏁 Definition of Done (Bug Fix)

- [ ] Root cause identified and documented above
- [ ] Fix implemented and peer-reviewed
- [ ] All AC scenarios above pass in staging
- [ ] Original story regression tests still pass
- [ ] Additional test case written to prevent recurrence
- [ ] Fix deployed to production and verified
- [ ] Affected users notified if the bug caused data issues
- [ ] Bug closed in backlog; related monitoring alert added if applicable

---

## 🔒 Security & Compliance Check (Bug)

| Question | Answer |
|---|---|
| Did this bug expose any personal or sensitive data? | ☐ Yes (escalate immediately to security team) &nbsp; ☐ No |
| Does the fix change any auth / access control logic? | ☐ Yes (security review required) &nbsp; ☐ No |
| Is a breach notification legally required? | ☐ Yes &nbsp; ☐ No &nbsp; ☐ Legal review needed |

---

## 🤖 AI Agent Instructions (Bug Fix)

**For AI Code Generator:**
```
BUG CONTEXT: BUG-XXX
Root cause: [paste from Root Cause section]
Files to change: [list files]
Fix scope: Change only what is needed to fix this bug. Do not refactor unrelated code.
After fixing: run all tests in [test file paths] and confirm they pass.
```

**For AI QA Agent:**
```
BUG CONTEXT: BUG-XXX
Write a regression test that would have caught this bug.
Test location: [test file path]
Also verify that the fix does not break these related flows: [list flows]
```

---
---

# 🔬 VARIANT B — SPIKE / RESEARCH STORY

<!-- ════════════════════════════════════════════════════
     USE THIS VARIANT when the team needs to investigate
     a question or explore options BEFORE writing a real
     User Story. A Spike has a time-box and produces a
     recommendation or prototype — NOT shipping code.
     Filename convention: SPIKE-XXX-short-topic.md
     e.g. SPIKE-003-evaluate-payment-providers.md
═════════════════════════════════════════════════════ -->

> **💡 When to use this:** Use a Spike when the team cannot estimate a story because there's a known unknown.
> Examples: "We don't know which email provider to use." / "We need to test if the AI model is fast enough."
> A Spike always has a time-box (max days to spend) and a clear question to answer.

---

# [SPIKE-XXX] 🔬 Spike Title — The Question We Are Investigating

---

## Quick Info

| Field | Your Answer |
|---|---|
| **Spike ID** | `SPIKE-XXX` |
| **Type** | ☐ Technical Feasibility &nbsp; ☐ Architecture Decision &nbsp; ☐ AI/LLM Evaluation &nbsp; ☐ UX Research &nbsp; ☐ Vendor Evaluation &nbsp; ☐ Compliance Research |
| **Parent Epic** | [Epic name] |
| **Stories this Spike unblocks** | `US-XXX`, `US-XXX` |
| **Assigned to** | [Developer / Designer / AI Research Agent] |
| **Sprint** | [Sprint # — a Spike is never longer than 1 sprint] |
| **⏱️ Time-box** | [e.g. "Maximum 3 days / 1.5 story points — stop and report findings even if unresolved"] |
| **Status** | ☐ Open &nbsp; ☐ In Progress &nbsp; ☐ Results Ready &nbsp; ☐ Closed |

---

## ❓ The Research Question

> *One clear question. If you have multiple questions, create multiple Spikes.*

**We need to answer:** [e.g. "Which email delivery provider (SendGrid vs. Postmark vs. AWS SES) gives us the best deliverability, pricing, and reliability for 10,000–500,000 sends/month with minimal engineering effort?"]

**Why we don't know yet:** [e.g. "We haven't sent transactional email at scale before. Each provider claims 99%+ deliverability, but we need evidence specific to our use case."]

**What happens if we skip this Spike:** [e.g. "We'll pick a provider blindly and may need to migrate mid-launch, which is expensive and risky."]

---

## 🎯 Success Criteria (How We Know the Spike is Done)

> *A Spike is done when you can answer the research question with enough confidence to write and estimate the real User Story.*

- [ ] The research question is answered with a clear recommendation
- [ ] The recommendation is backed by evidence (benchmarks, PoC, vendor docs, expert consultation)
- [ ] At least one follow-up User Story or Architecture Decision Record (ADR) is drafted
- [ ] The time-box was respected (work stopped at the deadline regardless of completion)
- [ ] Findings are documented in the Results section below

---

## 🔎 Investigation Plan

> *How will you find the answer? List the research methods.*

| Method | What you'll do | Owner | Time budget |
|---|---|---|---|
| [e.g. Vendor docs review] | [e.g. Read SendGrid, Postmark, and AWS SES documentation for pricing, limits, and APIs] | [Name] | [1 day] |
| [e.g. Proof of Concept (PoC)] | [e.g. Build a minimal PoC that sends 100 emails via each provider and measures delivery time] | [Name] | [1 day] |
| [e.g. Expert consultation] | [e.g. Ask #engineering-infra Slack channel for team experience with each provider] | [Name] | [2 hours] |
| [e.g. AI-assisted research] | [e.g. Ask AI agent to summarize recent developer community reviews of each provider] | [AI PM Agent] | [1 hour] |

---

## 🤖 AI Agent Instructions (Spike)

**For AI PM / Research Agent:**
```
SPIKE CONTEXT: SPIKE-XXX
Research question: [paste from above]
Your task:
  1. Search for developer community reviews, benchmarks, and incident reports for each option being evaluated.
  2. Summarize pricing models at the scale of 10,000 / 100,000 / 500,000 emails/month.
  3. List the top 3 risks or complaints raised by users of each option.
  4. Produce a side-by-side comparison table.
  5. Recommend the best option for our constraints: [list constraints here].
Time-box: complete your research in under 2 hours.
```

---

## 📊 Results & Findings

> *Fill this DURING and AFTER the investigation. Write findings as you go — don't wait until the end.*

### Option Comparison

| Criterion | [Option A] | [Option B] | [Option C] |
|---|---|---|---|
| [e.g. Deliverability rate] | | | |
| [e.g. Pricing at 100k/month] | | | |
| [e.g. API setup complexity] | | | |
| [e.g. Time to integrate] | | | |
| [e.g. Support quality] | | | |
| [e.g. Compliance certs] | | | |

### Key Findings

1. [Finding 1 — with evidence link]
2. [Finding 2 — with evidence link]
3. [Finding 3 — with evidence link]

### Risks & Unknowns Remaining

| Risk | Likelihood | Impact | How to mitigate |
|---|---|---|---|
| [e.g. Provider X changes pricing mid-contract] | Medium | High | [e.g. Negotiate annual pricing lock-in] |

---

## ✅ Recommendation

> *After the time-box, write your recommendation here — even if uncertain.*

**We recommend:** [e.g. "Use **Postmark** for transactional email (password reset, invoices) and **SendGrid** for marketing bulk email. Reasoning: Postmark has superior deliverability for transactional sends (98.7% vs. SendGrid's 96.2% in our PoC), and its pricing is predictable. SendGrid's marketing features justify the cost for bulk sends."]

**Confidence level:** ☐ High (PoC validated) &nbsp; ☐ Medium (docs + community evidence) &nbsp; ☐ Low (time-boxed, more research needed)

**Next steps:**
- [ ] [e.g. "Write `US-XXX — Set up Postmark for transactional email`"]
- [ ] [e.g. "Write ADR-005 documenting this decision"]
- [ ] [e.g. "Share findings in Sprint Review"]

---

## 📝 References

| Source | Link | Summary |
|---|---|---|
| [Vendor docs] | [URL] | |
| [Community post / benchmark] | [URL] | |
| [PoC repository] | [Link] | |
| [Expert input] | [Slack thread / meeting notes] | |

---

<!-- ════════════════════════════════════════════════════
     END OF FILE
     This file contains THREE templates:
     1. Standard User Story    → US-XXX-title.md
     2. Bug Report Story       → BUG-XXX-title.md
     3. Spike / Research Story → SPIKE-XXX-title.md

     Recommended folder structure for your repo:
     docs/
       user-stories/
         _template/
           User_Stories.md          ← this master file
         stories/
           US-001-user-signup.md
           US-002-reset-password.md
         bugs/
           BUG-001-token-expiry.md
         spikes/
           SPIKE-001-email-provider.md
═════════════════════════════════════════════════════ -->
