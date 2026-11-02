# 📋 Definition of Done (DoD) Template
**For AI-Driven Development Life Cycle — From First Line of Code to First 500 Customers**

> **Template Version:** 1.0  
> **Last Updated:** `YYYY-MM-DD` ← Fill this in  
> **Applies To:** SaaS Web Apps · iOS/Android Mobile Apps  
> **Methodology:** Hybrid / Shape Up  

---

## 📖 How to Fill This Document

**What is this document?**

A Definition of Done is your team's shared promise about what "finished" really means. Think of it like a pilot's pre-flight checklist — the plane doesn't take off until every box is ticked. Without this list, two people can finish the same task very differently, which causes bugs, missed deadlines, and unhappy customers.

**Who should fill it?**

Anyone involved in the project: a solo developer, a co-founder, a contractor, or even an AI assistant helping the team. Assign one owner per phase.

**Step-by-step instructions:**

1. **Fill in Section 1** (Project Information) before any work begins.
2. **Read the phase checklist** before starting that phase.
3. **Tick each checkbox** as you complete it: change `[ ]` to `[x]`.
4. **Write your initials + date** in every `Sign-Off` row.
5. **Never skip 🔴 REQUIRED items.** If you truly cannot complete one, log it in the Exception Log (Section 13) with a reason.
6. **🟡 RECOMMENDED** items should be done unless you have a documented reason.
7. **💡 OPTIONAL** items are nice-to-haves — add them when time allows.
8. **Update the version number** at the top every time you revise this document.

**Legend:**

| Symbol | Meaning |
|--------|---------|
| 🔴 | **REQUIRED** — Must be done before moving forward. No exceptions. |
| 🟡 | **RECOMMENDED** — Strong expectation; skip only with a written reason. |
| 💡 | **OPTIONAL** — Nice to have; include when capacity allows. |
| ✅ | Checklist item (tick when done) |
| 📝 | Fill-in field (replace the placeholder text) |
| 🤖 | AI-assisted step — document which AI tool was used |

> **👶 New to tech?** Every technical word in this document is explained in plain English in the **Glossary** (Section 15). If you see a term you don't understand, go there first.

---

## Section 1 · Project Information

> 📝 Fill this section in before any work starts. Update it whenever something changes.

| Field | Your Answer |
|-------|------------|
| **Project Name** | `[Name of your product]` |
| **Project Type** | `[ ] SaaS Web App  [ ] iOS App  [ ] Android App  [ ] All three` |
| **One-Line Description** | `[What does this product do in one sentence?]` |
| **Primary Owner / Lead** | `[Full name]` |
| **Supporting Team / Contractors** | `[Name(s) or "Solo"]` |
| **Project Start Date** | `YYYY-MM-DD` |
| **Target GA (Launch) Date** | `YYYY-MM-DD` |
| **Target: 500th Customer Date** | `YYYY-MM-DD` |
| **Version Control Platform** | `[ ] GitHub  [ ] GitLab  [ ] Bitbucket  [ ] Other: ___` |
| **Primary Cloud** | `[ ] AWS  [ ] Azure  [ ] Cloudflare  [ ] All three` |
| **AI Tools Used in Development** | `[e.g., Claude, ChatGPT, GitHub Copilot, Cursor]` |
| **AI Testing Tools** | `[e.g., Mabl, Testim, AI-powered Playwright scripts]` |
| **Compliance Tier** | `[x] GDPR  [x] SOC 2 / ISO 27001  [x] HIPAA` |

---

## Section 2 · What Is a Definition of Done?

> **Simple version (for anyone):**  
> Imagine you ask someone to "clean the kitchen." Does that mean just washing the dishes? Or does it also mean wiping the counters, taking out the trash, and mopping the floor? Without agreement, you'll both have a different answer — and someone will be disappointed.
>
> A Definition of Done answers: **"How do we all agree that this task is truly finished?"**
>
> In software, "done" is not just "I wrote the code." It means the code works, it's tested, it's secure, it's documented, and it's been reviewed. This document defines exactly what that means for every phase of your project.

---

## Section 3 · Journey Overview: Development → 500 Customers

```
 ┌──────────────────────────────────────────────────────────────────────────┐
 │  PHASE 1        PHASE 2        PHASE 3       PHASE 4     PHASE 5         │
 │  Feature DoD → Cycle DoD → Release DoD → Private β → Public β → GA →500 │
 │                                                                    PHASE 6 PHASE 7
 └──────────────────────────────────────────────────────────────────────────┘
```

| Phase | Name | Trigger to Enter | Key Gate to Exit |
|-------|------|-----------------|-----------------|
| 1 | Feature / Story Done | Story picked up from backlog | All feature-level boxes ticked + code merged |
| 2 | Cycle / Sprint Done | End of shape-up cycle or sprint | All stories in cycle meet Phase 1 DoD |
| 3 | Release Candidate | Cycle complete; release planned | Security scans pass; full regression green |
| 4 | Private Beta | RC approved; beta users invited | Feedback collected; critical bugs resolved |
| 5 | Public Beta | Private beta passed | Load tested; compliance verified |
| 6 | General Availability (GA) | Public beta passed | Launch checklist complete; rollback plan ready |
| 7 | Post-Launch (500 Customers) | First paying/active user onboarded | 500 users active; health metrics in green |

---

## Section 4 · Phase 1: Feature / Story Level DoD

> **What is this?** Every single small piece of work (a "story" or "task") must pass this checklist before it's considered done and merged into the main codebase.
>
> **Who checks it?** The person who built the feature, confirmed by a reviewer (or a second pass by the same person on solo teams).
>
> **Phase Owner:** `📝 [Name / Initials]`  
> **Date Completed:** `📝 YYYY-MM-DD`

### 4.1 · Code & Development

- [ ] 🔴 Code is written and working on the developer's local machine
- [ ] 🔴 Code follows the project's style guide *(see Section 12)*
- [ ] 🔴 No hardcoded secrets, passwords, API keys, or credentials exist in the code
- [ ] 🔴 No `console.log`, `print`, or debug statements left in production code
- [ ] 🔴 All new code has been reviewed — either by a second person or via a structured self-review checklist
- [ ] 🟡 Code is broken into small, readable functions (no single function longer than 50 lines without a comment explaining why)
- [ ] 🟡 Variable and function names are descriptive (e.g., `getUserEmail()` not `func1()`)
- [ ] 💡 Code complexity score checked with a linter or AI assistant (e.g., "Is this function too complex? Ask Claude.")

### 4.2 · AI-Assisted Development Log

> 🤖 Since AI tools are part of your workflow, document how AI was used. This builds an audit trail and improves AI prompts over time.

- [ ] 🟡 If AI (Claude, ChatGPT, Copilot, etc.) generated or suggested any code, that code has been **read, understood, and verified** by a human
- [ ] 🟡 AI-generated code that touches user data, authentication, or payments has been **manually reviewed line-by-line**
- [ ] 🟡 Any AI-generated tests have been checked to ensure they actually test the right behaviour (not just pass trivially)
- [ ] 💡 AI prompt used to generate key code snippets is saved in a `/ai-prompts` folder for future reference

**AI Usage Log for this feature:**

| AI Tool Used | What It Helped With | Verified by Human? |
|-------------|--------------------|--------------------|
| `[e.g., Claude]` | `[e.g., Generated the auth middleware]` | `[ ] Yes  [ ] No` |
| `[e.g., ChatGPT]` | `[e.g., Wrote unit tests for UserService]` | `[ ] Yes  [ ] No` |

### 4.3 · Testing

> **What is a unit test?** A small automated check that runs your code and verifies it gives the right answer. Like checking "does 2 + 2 = 4?" but for your software.

- [ ] 🔴 Unit tests written for all new logic (functions, methods, utilities)
- [ ] 🔴 All existing tests still pass (nothing you built broke something else)
- [ ] 🔴 Test coverage for new code is **≥ 80%** *(meaning 80 out of every 100 lines of code are tested)*
- [ ] 🟡 Edge cases are tested (e.g., what happens when a user submits an empty form? What if the internet drops?)
- [ ] 🟡 AI testing tool (if used) has generated a test report and it's been reviewed

**Test Results:**

| Test Type | Tool Used | Pass/Fail | Coverage % |
|-----------|-----------|-----------|-----------|
| Unit Tests | `[e.g., Jest, Pytest, XCTest]` | `[ ] Pass  [ ] Fail` | `___%` |
| AI-Generated Tests | `[e.g., Mabl, Testim]` | `[ ] Pass  [ ] Fail` | `___%` |

### 4.4 · Documentation

- [ ] 🔴 Any new or changed API endpoint is documented in the API reference (Swagger / OpenAPI)
- [ ] 🟡 The feature's README section or inline code comments are updated
- [ ] 🟡 If this feature changes the user experience, the user-facing help article is drafted
- [ ] 💡 A short "why I built it this way" comment is added near complex logic

### 4.5 · Version Control

> **GitHub Flow (Recommended for solo/small teams):** Create a branch → write code → open a Pull Request → review → merge to `main` → deploy.

- [ ] 🔴 Code is committed to a feature branch — **never directly to `main`**
- [ ] 🔴 Branch name follows the convention: `feature/short-description` or `fix/short-description`
- [ ] 🔴 A Pull Request (PR) is opened with a description of what changed and why
- [ ] 🔴 PR has been approved before merging (self-approve only if truly solo; add a checklist to the PR template instead)
- [ ] 🟡 Commit messages follow the format: `type: short description` *(e.g., `feat: add user login page`, `fix: correct email validation`)*

**Phase 1 Sign-Off**

| Reviewer | Role | Signature / Initials | Date |
|----------|------|---------------------|------|
| `📝 Name` | `📝 Developer / Owner` | `📝` | `📝 YYYY-MM-DD` |

---

## Section 5 · Phase 2: Build Cycle / Sprint Level DoD

> **What is this?** At the end of each Shape Up cycle (typically 6 weeks) or sprint (1–2 weeks), the entire batch of completed features is checked together before a release candidate is prepared.
>
> **Phase Owner:** `📝 [Name / Initials]`  
> **Cycle / Sprint Name:** `📝 [e.g., Cycle 3 – User Onboarding]`  
> **Date Completed:** `📝 YYYY-MM-DD`

### 5.1 · Completeness

- [ ] 🔴 Every story / task in this cycle meets **Phase 1 DoD** (all Phase 1 boxes are ticked)
- [ ] 🔴 Any story that did not meet Phase 1 DoD is moved back to the backlog — not "mostly done" and shipped
- [ ] 🔴 The product backlog is updated to reflect what was and was not completed this cycle

### 5.2 · Integration Testing

> **What is integration testing?** Testing that all your features work *together*, not just individually. Like checking that the login page actually connects to the user database.

- [ ] 🔴 Integration tests pass for all features completed this cycle
- [ ] 🔴 Key user journeys (login, sign-up, core action, payment if applicable) work end-to-end
- [ ] 🟡 E2E (end-to-end) tests run using Playwright, Cypress, or similar tool
- [ ] 🟡 Mobile-specific flows tested on both iOS and Android simulators/emulators

**Integration Test Results:**

| Journey Tested | Tool | Result | Tester |
|---------------|------|--------|--------|
| `[e.g., User Sign-Up → Dashboard]` | `[e.g., Playwright]` | `[ ] Pass  [ ] Fail` | `📝` |
| `[e.g., Password Reset Flow]` | `[e.g., Cypress]` | `[ ] Pass  [ ] Fail` | `📝` |
| `[e.g., Mobile: Purchase Flow iOS]` | `[e.g., XCUITest]` | `[ ] Pass  [ ] Fail` | `📝` |

### 5.3 · Performance

> **What is a performance benchmark?** A speed target. Like saying "this page must load in under 3 seconds."

- [ ] 🔴 Web page load time is **< 3 seconds** on a standard internet connection (tested with Lighthouse or WebPageTest)
- [ ] 🔴 API response time is **< 200ms** for all critical endpoints (tested with a tool like k6, Postman, or Artillery)
- [ ] 🟡 Mobile app cold-start time (time from tap to usable screen) is **< 2 seconds**
- [ ] 🟡 Lighthouse performance score is **≥ 80** for all key pages

**Performance Results:**

| Page / Endpoint | Load Time | Target | Pass/Fail |
|----------------|-----------|--------|-----------|
| `[e.g., /dashboard]` | `___ms` | `< 3000ms` | `[ ] ✅  [ ] ❌` |
| `[e.g., POST /api/auth/login]` | `___ms` | `< 200ms` | `[ ] ✅  [ ] ❌` |
| `[e.g., Home screen (mobile)]` | `___ms` | `< 2000ms` | `[ ] ✅  [ ] ❌` |

### 5.4 · Accessibility

> **What is accessibility?** Making sure your product can be used by everyone — including people who use screen readers, can't use a mouse, or have colour blindness. **WCAG 2.1 AA** is the international standard for this.

- [ ] 🔴 All new UI pages/screens pass **WCAG 2.1 AA** automated scan (using axe-core, Lighthouse, or similar)
- [ ] 🔴 All images have descriptive `alt` text
- [ ] 🔴 All forms have proper labels (not just placeholder text)
- [ ] 🟡 Keyboard navigation works without a mouse on all new screens
- [ ] 🟡 Colour contrast ratio is at least **4.5:1** for normal text and **3:1** for large text
- [ ] 💡 Manual screen reader test performed on critical flows (VoiceOver on iOS/macOS, TalkBack on Android)

### 5.5 · Cycle Sign-Off

| Reviewer | Role | Signature / Initials | Date |
|----------|------|---------------------|------|
| `📝 Name` | `📝 Lead / Owner` | `📝` | `📝 YYYY-MM-DD` |

---

## Section 6 · Phase 3: Release Candidate (RC) DoD

> **What is a Release Candidate?** A version of the product that *could* be the final version — it's ready for serious testing before going live. Think of it as the "dress rehearsal" before opening night.
>
> **Phase Owner:** `📝 [Name / Initials]`  
> **RC Version Number:** `📝 [e.g., v0.9.0-rc1]`  
> **Date Completed:** `📝 YYYY-MM-DD`

### 6.1 · Full Regression Testing

> **What is regression testing?** Re-testing everything to make sure new code didn't break anything that used to work.

- [ ] 🔴 Full regression test suite executed — all tests pass (0 failures)
- [ ] 🔴 All bugs found in this cycle are resolved or formally deferred with a ticket reference
- [ ] 🔴 No **P0 (Critical)** or **P1 (High)** bugs are open
- [ ] 🟡 Bug triage completed — all P2 (Medium) bugs have a fix timeline before GA

**Open Bugs at RC:**

| Bug ID | Severity | Description | Status | Target Fix |
|--------|----------|-------------|--------|-----------|
| `#___` | `P0/P1/P2` | `[Short description]` | `Open / Deferred` | `YYYY-MM-DD` |

### 6.2 · Security Scans

> **What is a security scan?** An automated tool that reads your code and looks for known security weaknesses — like a spell-checker, but for vulnerabilities.

- [ ] 🔴 **SAST scan** (Static Application Security Testing) run with zero Critical or High findings *(e.g., Snyk, SonarQube, Semgrep)*
- [ ] 🔴 **DAST scan** (Dynamic Application Security Testing) run against the staging environment with zero Critical findings *(e.g., OWASP ZAP, Burp Suite)*
- [ ] 🔴 **Dependency audit** run — no packages with Critical CVEs (known vulnerabilities) *(e.g., `npm audit`, `pip-audit`, `snyk test`)*
- [ ] 🔴 **Secret scan** run — no API keys, passwords, or tokens found in the codebase *(e.g., Gitleaks, GitHub Secret Scanning, truffleHog)*
- [ ] 🟡 All security findings logged with severity, owner, and resolution date
- [ ] 🔴 **Penetration test** scheduled or completed *(for HIPAA + SOC 2 projects, a pen test is required before GA)*

**Security Scan Results:**

| Scan Type | Tool Used | Critical Findings | High Findings | Status |
|-----------|-----------|------------------|---------------|--------|
| SAST | `[e.g., Snyk Code]` | `___` | `___` | `[ ] Pass  [ ] Fail` |
| DAST | `[e.g., OWASP ZAP]` | `___` | `___` | `[ ] Pass  [ ] Fail` |
| Dependency Audit | `[e.g., npm audit]` | `___` | `___` | `[ ] Pass  [ ] Fail` |
| Secret Scan | `[e.g., Gitleaks]` | `___` | `___` | `[ ] Pass  [ ] Fail` |
| Pen Test | `[Tool / Vendor]` | `___` | `___` | `[ ] Pass  [ ] Scheduled: DATE` |

### 6.3 · Documentation Complete

- [ ] 🔴 API documentation (Swagger / OpenAPI) is up to date with every endpoint in this release
- [ ] 🔴 Architecture decision records (ADRs) updated for any significant technical choices made this cycle
- [ ] 🟡 Deployment runbook (step-by-step deploy guide) written or updated
- [ ] 🟡 User-facing help articles drafted for all new features
- [ ] 🟡 CHANGELOG updated with a human-readable summary of what changed in this version
- [ ] 💡 Internal system diagram (showing how services connect) updated

### 6.4 · Environment & Infrastructure

- [ ] 🔴 Staging environment is a **production-like copy** — same cloud services, same configuration
- [ ] 🔴 All environment variables and secrets are stored in a secrets manager *(e.g., AWS Secrets Manager, Azure Key Vault)* — not in `.env` files committed to git
- [ ] 🔴 Infrastructure-as-Code (IaC) files are up to date *(e.g., Terraform, Pulumi, Bicep)*
- [ ] 🟡 Database migrations tested on staging and rollback tested
- [ ] 🟡 Cloudflare rules, WAF settings, and CDN configuration verified

### 6.5 · RC Sign-Off

| Reviewer | Role | Signature / Initials | Date |
|----------|------|---------------------|------|
| `📝 Name` | `📝 Lead / Owner` | `📝` | `📝 YYYY-MM-DD` |

---

## Section 7 · Phase 4: Private Beta DoD

> **What is Private Beta?** An invite-only version of your product given to a small, trusted group of real users before the public sees it. Goal: catch real-world bugs and collect feedback without risking reputation at scale.
>
> **Beta Cohort Size Target:** `📝 [e.g., 10–50 users]`  
> **Phase Owner:** `📝 [Name / Initials]`  
> **Beta Start Date:** `📝 YYYY-MM-DD`  
> **Beta End Date (planned):** `📝 YYYY-MM-DD`

### 7.1 · Beta Environment Ready

- [ ] 🔴 A dedicated **beta/staging environment** is live on production infrastructure (AWS / Azure / Cloudflare)
- [ ] 🔴 Beta environment URL / app build is separate from production — beta users cannot affect production data
- [ ] 🔴 **Feature flags** are configured — you can turn individual features on/off without redeploying code
- [ ] 🔴 Beta user accounts created and tested before inviting real users
- [ ] 🟡 Data seeded in beta environment to give users a realistic starting experience (e.g., sample data, demo content)

### 7.2 · User Onboarding

- [ ] 🔴 Onboarding flow (sign-up → first value moment) works without errors
- [ ] 🔴 Beta invite emails sent with clear instructions (including what to do if something breaks)
- [ ] 🔴 Feedback channel set up and communicated to beta users *(e.g., Slack, Discord, Typeform, in-app widget)*
- [ ] 🟡 Welcome email / in-app tour explains what's new and what you want users to try
- [ ] 🟡 NPS (Net Promoter Score) or satisfaction survey scheduled to send after 7 days

### 7.3 · Monitoring Active

> **Why monitor during beta?** Real users do unexpected things. Monitoring lets you see crashes, errors, and slow pages *in real time* before they reach thousands of users.

- [ ] 🔴 **Error tracking** active and alerting *(e.g., Sentry, Datadog)* — errors send a notification within 5 minutes
- [ ] 🔴 **Uptime monitoring** active *(e.g., Pingdom, Better Uptime)* — alerts fire if the app goes down
- [ ] 🔴 **Analytics** tracking user behaviour in the beta environment *(e.g., PostHog, Mixpanel, GA4)*
- [ ] 🔴 **Log aggregation** collecting all server logs *(e.g., CloudWatch, Azure Monitor)*
- [ ] 🟡 Alerts configured for: error rate > 1%, p99 API latency > 500ms, uptime < 99.5%
- [ ] 🟡 Daily monitoring review scheduled during beta period

**Monitoring Dashboard:**

| Tool | What It Monitors | Alert Threshold | Configured? |
|------|-----------------|-----------------|-------------|
| `[e.g., Sentry]` | `Error rate` | `> 1% of sessions` | `[ ] Yes  [ ] No` |
| `[e.g., Pingdom]` | `Uptime` | `< 99.5%` | `[ ] Yes  [ ] No` |
| `[e.g., PostHog]` | `User funnels` | `Conversion drop > 20%` | `[ ] Yes  [ ] No` |
| `[e.g., CloudWatch]` | `Server logs` | `5xx errors > 0.5%` | `[ ] Yes  [ ] No` |

### 7.4 · Beta Exit Criteria

> **You may exit Private Beta when ALL of these are true:**

- [ ] 🔴 Beta ran for at least **`📝 [e.g., 2–4 weeks]`** or **`📝 [minimum user count]`** users have used the product
- [ ] 🔴 All **P0 and P1** bugs reported by beta users are resolved
- [ ] 🔴 Feedback has been reviewed and a decision made on each item (fix now, fix later, or not a bug)
- [ ] 🟡 Average session length or core action completion rate meets your target *(e.g., "80% of users complete onboarding")*
- [ ] 💡 Testimonial or quote collected from at least one beta user (useful for launch marketing)

### 7.5 · Private Beta Sign-Off

| Reviewer | Role | Signature / Initials | Date |
|----------|------|---------------------|------|
| `📝 Name` | `📝 Lead / Owner` | `📝` | `📝 YYYY-MM-DD` |

---

## Section 8 · Phase 5: Public Beta DoD

> **What is Public Beta?** The product is open to anyone who wants to join, but you're transparent that it's still in beta. You're widening the audience to stress-test the system and validate product-market fit before the official launch.
>
> **Phase Owner:** `📝 [Name / Initials]`  
> **Target Public Beta User Count:** `📝 [e.g., 100–300 users]`  
> **Date Started:** `📝 YYYY-MM-DD`

### 8.1 · Stability & Performance at Scale

- [ ] 🔴 **Load test** performed simulating at least **`📝 [e.g., 500]` concurrent users** — all performance targets still met
- [ ] 🔴 Auto-scaling configured: if traffic spikes, the system automatically adds capacity
- [ ] 🔴 No P0 or P1 bugs are open from private beta
- [ ] 🟡 Database query performance verified — no queries taking > 1 second
- [ ] 🟡 CDN (Content Delivery Network via Cloudflare) verified for static assets

### 8.2 · Compliance Verification

> **Why compliance now?** Before real users give you their data at scale, you must ensure you are legally handling it correctly.

**GDPR (General Data Protection Regulation — required if any EU users):**
- [ ] 🔴 Privacy Policy published and linked from sign-up page and footer
- [ ] 🔴 Cookie consent banner implemented — non-essential cookies are opt-in, not opt-out
- [ ] 🔴 Users can request their data be deleted ("Right to Erasure") — process documented
- [ ] 🔴 Data Processing Agreement (DPA) signed with all third-party services that handle user data (e.g., Sentry, PostHog, email provider)
- [ ] 🟡 Data retention policy defined (e.g., "We delete inactive accounts after 2 years")

**HIPAA (if handling health data):**
- [ ] 🔴 Business Associate Agreements (BAA) signed with all cloud providers that store/process PHI *(Personal Health Information)* — AWS, Azure, and Cloudflare all offer BAAs
- [ ] 🔴 PHI is encrypted **at rest** (stored securely) and **in transit** (during transfer)
- [ ] 🔴 Access to PHI is role-based and logged — only people who need it can see it
- [ ] 🔴 Audit logs for all PHI access are retained for a minimum of **6 years**
- [ ] 🔴 Breach notification process documented (you know what to do if data is exposed)

**SOC 2 / ISO 27001 (Security Standards):**
- [ ] 🔴 Access control policy documented — who has access to what, and why
- [ ] 🔴 Multi-Factor Authentication (MFA) enforced for all internal team access to cloud and production systems
- [ ] 🔴 Incident response plan documented *(what do you do if you get hacked?)*
- [ ] 🟡 Vendor security review completed for all critical third-party tools
- [ ] 💡 SOC 2 Type I or ISO 27001 gap analysis scheduled if pursuing formal certification

### 8.3 · Support & Legal Readiness

- [ ] 🔴 Terms of Service (ToS) published and agreed to during sign-up
- [ ] 🔴 Support channel is live and monitored *(e.g., email, Intercom, Zendesk, Discord)*
- [ ] 🔴 Response SLA defined and communicated *(e.g., "We respond to all support requests within 24 hours")*
- [ ] 🟡 FAQ or help centre populated with answers to the top 10 questions from private beta
- [ ] 💡 Status page live so users can check if there's an outage *(e.g., statuspage.io, Instatus)*

### 8.4 · Mobile-Specific (if applicable)

- [ ] 🔴 App tested on latest 2 major versions of iOS (e.g., iOS 17, iOS 18)
- [ ] 🔴 App tested on latest 2 major versions of Android
- [ ] 🔴 App tested on at least 3 different screen sizes
- [ ] 🟡 App Store / Google Play listing content (screenshots, description, keywords) drafted
- [ ] 🟡 App reviewed for App Store / Play Store guidelines compliance before submission

### 8.5 · Public Beta Sign-Off

| Reviewer | Role | Signature / Initials | Date |
|----------|------|---------------------|------|
| `📝 Name` | `📝 Lead / Owner` | `📝` | `📝 YYYY-MM-DD` |

---

## Section 9 · Phase 6: General Availability (GA) / Launch DoD

> **What is GA?** The official, public launch of your product. After this, you are open for business. This is the point of no return — make sure every box is ticked.
>
> **Phase Owner:** `📝 [Name / Initials]`  
> **Launch Version:** `📝 [e.g., v1.0.0]`  
> **Launch Date:** `📝 YYYY-MM-DD`

### 9.1 · Production Environment Verified

- [ ] 🔴 Production environment is fully deployed and smoke-tested *(a quick manual check that the critical pages/screens work)*
- [ ] 🔴 Production uses **different** credentials, databases, and API keys from staging — never shared
- [ ] 🔴 Backup system verified: database backups run automatically and a restoration test has been performed
- [ ] 🔴 **Rollback plan documented and tested** *(you know exactly how to go back to the previous version if something breaks)*
- [ ] 🔴 All DNS records correct — your domain points to the right servers
- [ ] 🔴 SSL/TLS certificate valid and auto-renewing *(HTTPS padlock shows in browser)*
- [ ] 🟡 Cloudflare WAF (Web Application Firewall) rules active and verified

**Rollback Runbook:**

> 📝 Fill this in BEFORE launch, not after.

```
If production breaks after launch:
1. Who to call first:    [Name + Contact]
2. How to roll back:     [e.g., Re-deploy previous Docker image tag: v0.9.5]
3. How to roll back DB:  [e.g., Restore from latest RDS snapshot taken at YYYY-MM-DD HH:MM]
4. Estimated time:       [e.g., ~15 minutes]
5. Communication plan:   [e.g., Post to Status Page + email registered users]
```

### 9.2 · Launch Readiness

- [ ] 🔴 Landing page / marketing site is live, accurate, and loads quickly
- [ ] 🔴 Pricing page is accurate and payment processing is tested end-to-end in production (use a real card for a $0.01 test charge if safe to do so)
- [ ] 🔴 All onboarding emails send correctly from a properly authenticated domain (SPF, DKIM, DMARC configured)
- [ ] 🟡 App Store / Google Play submission approved *(for mobile)*
- [ ] 🟡 Product Hunt, social media, or press announcement scheduled
- [ ] 🟡 Referral or waitlist mechanism live (to capture early growth)

### 9.3 · All Prior Phases Verified

- [ ] 🔴 Phase 1 DoD: All features confirmed done
- [ ] 🔴 Phase 3 DoD: Security scans passed (RC gate)
- [ ] 🔴 Phase 4 DoD: Private beta completed
- [ ] 🔴 Phase 5 DoD: Public beta completed + compliance verified
- [ ] 🔴 No P0 or P1 bugs are open

### 9.4 · GA Sign-Off

| Reviewer | Role | Signature / Initials | Date |
|----------|------|---------------------|------|
| `📝 Name` | `📝 Lead / Owner` | `📝` | `📝 YYYY-MM-DD` |

---

## Section 10 · Phase 7: Post-Launch — First 500 Customers DoD

> **What is this?** The work doesn't stop at launch. This checklist ensures your product remains healthy and your users are succeeding as you grow from customer #1 to customer #500.
>
> **Phase Owner:** `📝 [Name / Initials]`  
> **Customer #1 Date:** `📝 YYYY-MM-DD`  
> **Customer #500 Target Date:** `📝 YYYY-MM-DD`  
> **Customer #500 Actual Date:** `📝 YYYY-MM-DD`

### 10.1 · Health Metrics (Monitored Daily)

> ✅ Review these metrics every day. Set a 15-minute calendar block for it.

| Metric | Target | Current | Status |
|--------|--------|---------|--------|
| Uptime | ≥ 99.5% | `___%` | `[ ] ✅  [ ] ❌` |
| Error Rate | < 1% of sessions | `___%` | `[ ] ✅  [ ] ❌` |
| API p99 Latency | < 500ms | `___ms` | `[ ] ✅  [ ] ❌` |
| Daily Active Users (DAU) | `📝 [Your target]` | `___` | `[ ] ✅  [ ] ❌` |
| Onboarding Completion Rate | ≥ `📝 [Your target]%` | `___%` | `[ ] ✅  [ ] ❌` |
| Support Ticket Volume | < `📝 [Your threshold]` per day | `___` | `[ ] ✅  [ ] ❌` |
| Churn Rate (monthly) | < `📝 [Your target]%` | `___%` | `[ ] ✅  [ ] ❌` |

### 10.2 · Customer Milestones

- [ ] 🔴 **Customer #1:** Personal outreach done — understand exactly why they signed up and what they need
- [ ] 🔴 **Customer #10:** 10 users interviewed or surveyed — top 3 pain points documented
- [ ] 🟡 **Customer #50:** NPS score collected — score is > 30
- [ ] 🟡 **Customer #100:** First case study or testimonial collected
- [ ] 🟡 **Customer #250:** Pricing validated — revenue covers basic operating costs
- [ ] 🔴 **Customer #500:** Full product review conducted — roadmap updated based on real usage data

### 10.3 · Incident Management

- [ ] 🔴 Incident response plan is in place — documented and accessible *(link:* `📝 [URL or file path]`*)*
- [ ] 🔴 Every incident (outage, data issue, security event) is logged in an **Incident Log** with: date, duration, root cause, resolution, and prevention plan
- [ ] 🟡 Post-mortem written within 48 hours for any P0 incident
- [ ] 🟡 Customers affected by incidents are notified within `📝 [e.g., 2 hours]`

**Incident Log:**

| Date | Duration | Severity | Root Cause (short) | Status | Post-Mortem? |
|------|----------|----------|-------------------|--------|-------------|
| `YYYY-MM-DD` | `___min` | `P0/P1/P2` | `[One sentence]` | `Resolved` | `[ ] Yes  [ ] No` |

### 10.4 · Security Hygiene (Ongoing)

- [ ] 🔴 Dependency security audit run **monthly** — no critical CVEs go unpatched for > 30 days
- [ ] 🔴 Access review done **quarterly** — remove any accounts of people who no longer work on the project
- [ ] 🟡 Second penetration test scheduled within 6 months of GA
- [ ] 🟡 SSL certificates verified to not expire within the next 60 days

### 10.5 · 500-Customer Milestone Review

> **Complete this when you reach customer #500 — a moment worth celebrating and reviewing! 🎉**

- [ ] 🔴 Retrospective held: what went well, what didn't, and what to do differently
- [ ] 🔴 Updated roadmap published for the next phase of growth
- [ ] 🔴 Compliance status reviewed — are GDPR, HIPAA, and SOC 2 obligations still being met at the new scale?
- [ ] 🟡 Unit economics calculated: Customer Acquisition Cost (CAC) and Lifetime Value (LTV)
- [ ] 🟡 Team/contractor needs assessed: does the team need to grow?
- [ ] 💡 Start of Series A preparation, or next funding milestone, if applicable

### 10.6 · Post-Launch Sign-Off

| Reviewer | Role | Signature / Initials | Date |
|----------|------|---------------------|------|
| `📝 Name` | `📝 Lead / Owner` | `📝` | `📝 YYYY-MM-DD` |

---

## Section 11 · Universal Quality Checklists

> These checklists apply **at every phase**. Use them as a reference when you're not sure if a specific item has been covered.

### 11.1 · Code Quality Standards

- [ ] 🔴 Linter configured and passing with zero errors *(e.g., ESLint for JS/TS, Flake8/Ruff for Python, SwiftLint for iOS)*
- [ ] 🔴 Code formatter applied consistently *(e.g., Prettier, Black, gofmt)*
- [ ] 🔴 No TODO or FIXME comments left in code going to production *(convert them to tickets first)*
- [ ] 🟡 Cyclomatic complexity score acceptable *(functions are not too tangled — most linters report this)*
- [ ] 🟡 Dependencies reviewed — no unnecessary packages added

### 11.2 · AI-Assisted Development Standards

- [ ] 🔴 AI-generated code is treated like third-party code: **always reviewed, never blindly trusted**
- [ ] 🔴 AI tools are **not used** to generate or suggest solutions to security-sensitive problems without a subsequent security review
- [ ] 🔴 AI prompts that generated key architectural decisions are documented
- [ ] 🟡 AI-generated tests are verified to fail when the tested code is intentionally broken (proving they actually test something)
- [ ] 🟡 AI-assisted code review run on every PR *(e.g., using Claude, CodeRabbit, or GitHub Copilot PR Review)*
- [ ] 💡 A "lessons learned from AI" log is maintained to improve future prompts

### 11.3 · Testing Standards Summary

| Test Type | When Required | Minimum Coverage | Tool Examples |
|-----------|--------------|-----------------|--------------|
| Unit Tests | Every feature | ≥ 80% of new code | Jest, Pytest, XCTest, JUnit |
| Integration Tests | Every cycle | All critical paths | Playwright, Cypress, Supertest |
| E2E Tests | Every release | Top 5 user journeys | Playwright, Detox (mobile) |
| Performance Tests | Pre-beta, pre-GA | Pages < 3s, APIs < 200ms | Lighthouse, k6, Artillery |
| Accessibility Tests | Every cycle | WCAG 2.1 AA | axe-core, Lighthouse, WAVE |
| Security Scans | Every RC | 0 Critical/High findings | Snyk, SonarQube, OWASP ZAP |
| AI-Generated Tests | Every feature (if AI used) | Verified by human | Mabl, Testim, custom |

### 11.4 · Documentation Standards

| Document | Owner | When Updated | Where Stored |
|----------|-------|-------------|-------------|
| API Reference (Swagger / OpenAPI) | Developer | Every feature that touches API | `/docs/api/` or Swagger Hub |
| Architecture Diagram | Lead | Every major structural change | `/docs/architecture/` |
| Deployment Runbook | Lead | Every release | `/docs/ops/deploy-runbook.md` |
| CHANGELOG | Lead | Every release | `/CHANGELOG.md` |
| User Help Articles | Owner | Every user-facing feature | Help centre / Notion |
| Privacy Policy | Legal / Owner | Every change in data handling | Website footer |
| Incident Log | Owner | Every incident | `/docs/ops/incidents/` |

---

## Section 12 · Version Control Standards

> **Since no formal branching strategy is defined yet, the following GitHub Flow is recommended for solo/1–2 person teams. Update this section once agreed.**

### Recommended: GitHub Flow

```
main ──────────────────────────────────────────────────► (always deployable)
  │
  ├── feature/user-login ──────────► [PR] ──► merge ──► deploy
  ├── fix/email-validation ────────► [PR] ──► merge ──► deploy
  └── hotfix/critical-crash ──────► [PR] ──► merge ──► deploy
```

**Rules:**

1. `main` is **always** in a deployable state
2. **Never commit directly to `main`** — always use a branch + PR
3. Branches are short-lived (merged within 1–3 days maximum)
4. One PR per logical change (not "everything I did this week")

### Branch Naming Convention

| Type | Format | Example |
|------|--------|---------|
| New feature | `feature/short-description` | `feature/user-login-page` |
| Bug fix | `fix/short-description` | `fix/email-validation-crash` |
| Urgent fix | `hotfix/short-description` | `hotfix/payment-gateway-error` |
| Infrastructure | `infra/short-description` | `infra/add-cloudflare-rules` |
| Documentation | `docs/short-description` | `docs/update-api-reference` |

### Commit Message Format

```
type: short description (under 72 characters)

[Optional: longer explanation if needed]
[Optional: Closes #issue-number]
```

**Types:** `feat` · `fix` · `docs` · `test` · `refactor` · `infra` · `chore`

**Examples:**
```
feat: add user email verification flow
fix: correct timezone handling in date picker
docs: update deployment runbook for Azure
test: add unit tests for AuthService
```

---

## Section 13 · DoD Exception Log

> **How to use this:** If you cannot complete a Required item, you must log it here. Never just skip it silently. An exception is acceptable; an unexplained skip is not.

| Date | Phase | Item Skipped | Reason | Risk Level | Compensating Action | Owner | Target Resolution Date |
|------|-------|-------------|--------|-----------|---------------------|-------|----------------------|
| `YYYY-MM-DD` | `📝` | `[Exact item text]` | `[Why it can't be done now]` | `🔴 High / 🟡 Med / 🟢 Low` | `[What you're doing instead]` | `📝` | `YYYY-MM-DD` |

---

## Section 14 · Sign-Off Matrix

> This table shows who must sign off at each phase. For solo teams, one person signs all roles — but signing each one separately forces a deliberate check.

| Phase | Technical Review | Security Review | Compliance Review | Product / Owner Sign-Off |
|-------|-----------------|----------------|------------------|--------------------------|
| Phase 1 – Feature | `📝` | — | — | `📝` |
| Phase 2 – Cycle | `📝` | — | — | `📝` |
| Phase 3 – RC | `📝` | `📝` | — | `📝` |
| Phase 4 – Private Beta | `📝` | `📝` | — | `📝` |
| Phase 5 – Public Beta | `📝` | `📝` | `📝` | `📝` |
| Phase 6 – GA | `📝` | `📝` | `📝` | `📝` |
| Phase 7 – 500 Customers | `📝` | `📝` | `📝` | `📝` |

---

## Section 15 · Glossary

> **This section explains every technical term in plain English. If you're new to tech, read this before filling out the document.**

| Term | Plain English Explanation |
|------|--------------------------|
| **API** | A way for two software systems to talk to each other. Like a waiter who carries your order to the kitchen and brings food back. |
| **CHANGELOG** | A running list of "what changed" in each version of your product. Like a ship's log. |
| **CDN** | Content Delivery Network. A network of servers worldwide that stores copies of your website's files so they load faster for users everywhere. Cloudflare is one. |
| **CVE** | Common Vulnerabilities and Exposures. A publicly known software security flaw. A "critical CVE" is a serious one that hackers can exploit. |
| **DAST** | Dynamic Application Security Testing. An automated tool that attacks your running app to find security holes — like a security guard testing your locks while the store is open. |
| **DPA** | Data Processing Agreement. A legal contract between you and a vendor who handles your users' data on your behalf. Required by GDPR. |
| **E2E Test** | End-to-End Test. A test that simulates a real user going through an entire flow, like signing up, adding an item to a cart, and checking out. |
| **Feature Flag** | A switch in your code that lets you turn a feature on or off without releasing new code. Like a light switch for software features. |
| **GDPR** | General Data Protection Regulation. EU law that gives people rights over their personal data and requires companies to handle it carefully. |
| **HIPAA** | Health Insurance Portability and Accountability Act. US law that protects the privacy and security of health information. |
| **IaC** | Infrastructure as Code. Writing the setup of your servers and cloud resources as code files, so you can recreate them reliably. |
| **Incident** | When something goes wrong in production — an outage, a bug affecting many users, or a security event. |
| **Integration Test** | Testing that different parts of your system work together correctly (not just individually). |
| **Linter** | A tool that automatically checks your code for style errors and common mistakes — like a grammar checker for code. |
| **MFA** | Multi-Factor Authentication. Logging in with more than just a password — usually a password plus a code from your phone. Much more secure. |
| **P0 / P1 / P2 Bug** | Bug severity levels. P0 = Critical (app is broken for everyone). P1 = High (major feature is broken). P2 = Medium (minor issue). |
| **Pen Test** | Penetration Testing. Hiring a security expert (or using a tool) to try to hack your product to find weaknesses before criminals do. |
| **PHI** | Protected Health Information. Any data about a person's health that can identify them. Protected by HIPAA. |
| **PR (Pull Request)** | A request to merge your code changes into the main codebase. It's a way to share, review, and discuss code before it becomes official. |
| **Regression Test** | Re-running all your tests after making changes, to make sure nothing that used to work is now broken. |
| **RC (Release Candidate)** | A version of software that is nearly ready to ship. "This could be the final version — let's test it thoroughly." |
| **Rollback** | Going back to the previous working version of your software if the new version has a serious problem. |
| **SAST** | Static Application Security Testing. An automated tool that reads your source code to find security vulnerabilities — like a spell-checker for security bugs. |
| **SLA** | Service Level Agreement. A commitment about how good your service will be — e.g., "99.5% uptime" or "respond to support in 24 hours." |
| **SOC 2** | Service Organization Control 2. A security certification that proves you handle data safely and securely. Common in B2B SaaS. |
| **Smoke Test** | A quick, basic check after deployment: "Does the app load? Can someone log in?" Like starting a car just to make sure it turns on. |
| **SSL/TLS** | The technology that creates the padlock 🔒 in your browser. It encrypts data between the user and your server. |
| **Unit Test** | A small automated test that checks one specific piece of code (one function) in isolation. |
| **WCAG 2.1 AA** | Web Content Accessibility Guidelines — the international standard for making websites usable by people with disabilities. AA is the middle level (between A and AAA). |
| **WAF** | Web Application Firewall. A security tool (like Cloudflare's) that blocks malicious traffic before it reaches your server. |

---

## 📌 Quick Reference Card

> **Cut this out and pin it somewhere visible. These are the 10 rules that summarise this entire document.**

```
┌─────────────────────────────────────────────────────────────────────┐
│            ✅ DEFINITION OF DONE – 10 GOLDEN RULES                  │
│                                                                     │
│  1. Code is written, reviewed, and on a branch (never on main).    │
│  2. Tests pass. 80%+ coverage. AI-generated tests verified.        │
│  3. No secrets in code. Secret scan passed.                        │
│  4. Security scans run before every release.                       │
│  5. Pages load in < 3s. APIs respond in < 200ms.                   │
│  6. WCAG 2.1 AA accessibility passes on all new screens.           │
│  7. Docs are updated before marking anything done.                 │
│  8. Compliance (GDPR/HIPAA/SOC2) is checked, not assumed.          │
│  9. Monitoring is watching before users arrive.                    │
│ 10. A rollback plan exists before every production deployment.     │
└─────────────────────────────────────────────────────────────────────┘
```

---

---

## Appendix A · Mobile App Store Submission Checklist

> **When to use this:** Complete this checklist before submitting to the Apple App Store or Google Play Store. App stores can reject apps that skip these requirements, causing delays of days or weeks.
>
> **Important:** App store review is not instant. Apple typically takes **1–3 business days**; Google Play typically takes **1–7 days**. Plan your launch timeline accordingly.

### A.1 · Apple App Store (iOS)

**App Content & Metadata:**
- [ ] 🔴 App name (≤ 30 characters) is set and does not infringe on trademarks
- [ ] 🔴 App subtitle (≤ 30 characters) accurately describes the app
- [ ] 🔴 App description (≤ 4,000 characters) is accurate, grammatically correct, and does not mention competitor apps by name
- [ ] 🔴 Keywords (≤ 100 characters total) chosen to maximise search visibility — no spam or irrelevant terms
- [ ] 🔴 Support URL (links to a real working support page) provided
- [ ] 🔴 Privacy Policy URL provided and links to a live, accurate policy

**Screenshots & Previews:**
- [ ] 🔴 Screenshots provided for required device sizes:
  - 6.9" display (iPhone 16 Pro Max) — **Required**
  - 6.5" display (iPhone 14 Plus / 15 Plus) — **Required**
  - 12.9" iPad Pro — Required if app supports iPad
- [ ] 🟡 App preview video (up to 30 seconds) created — shows real in-app functionality, not a marketing video
- [ ] 🔴 Screenshots show actual app UI — no mockups of hardware Apple doesn't make

**Privacy & Data (App Privacy Labels):**
- [ ] 🔴 App Privacy section in App Store Connect completed — every category of data your app collects is declared
  - *(Examples: Name, Email, Health Data, Usage Data, Device ID)*
- [ ] 🔴 Data linked to user identity declared correctly
- [ ] 🔴 Tracking usage declared — if you use ATT (App Tracking Transparency), the prompt is implemented correctly
- [ ] 🔴 If app collects health/fitness data: HealthKit usage is justified and the privacy policy mentions it

**Age Rating:**
- [ ] 🔴 Age rating questionnaire completed in App Store Connect
- [ ] 🔴 Age rating accurately reflects the content *(e.g., apps with user-generated content must account for potential mature content)*

**Technical:**
- [ ] 🔴 App does not crash on launch on any supported device/OS version
- [ ] 🔴 All app functionality works without an internet connection OR a clear error is shown when offline
- [ ] 🔴 App does not reference other platforms (e.g., no mention of "Android" or "Google Play" in the iOS app)
- [ ] 🔴 In-app purchases use Apple's IAP system — no linking to external payment for digital goods
- [ ] 🔴 App has been tested on TestFlight with external testers before submission
- [ ] 🟡 App targets the latest iOS SDK (within 1 year of current)
- [ ] 🟡 App supports latest 2 major iOS versions (e.g., iOS 17 and iOS 18)

**TestFlight Pre-Submission:**
- [ ] 🔴 TestFlight build uploaded and at least `📝 [e.g., 5]` external testers have tested it
- [ ] 🔴 No crashes reported in TestFlight Crash Reports
- [ ] 🔴 All TestFlight feedback reviewed and addressed

**App Store Connect Submission:**
- [ ] 🔴 Build uploaded via Xcode or Transporter
- [ ] 🔴 App submitted for review with release option: `[ ] Manual release  [ ] Automatic after approval`
- [ ] 🟡 Phased release enabled (gradually rolls out to 1% → 100% of users over 7 days — allows quick rollback)

---

### A.2 · Google Play Store (Android)

**App Content & Metadata:**
- [ ] 🔴 App title (≤ 30 characters) set — accurate and trademark-safe
- [ ] 🔴 Short description (≤ 80 characters) written
- [ ] 🔴 Full description (≤ 4,000 characters) written — accurate, no spam
- [ ] 🔴 App category selected correctly
- [ ] 🔴 Email address for support provided

**Screenshots & Visuals:**
- [ ] 🔴 Feature graphic (1024 × 500 px) designed — shown at top of listing
- [ ] 🔴 Screenshots provided for:
  - Phone: minimum 2, maximum 8 (16:9 or 9:16 ratio)
  - 7" tablet: recommended
  - 10" tablet: recommended if app supports tablets
- [ ] 🟡 Promo video (YouTube link) added

**Data Safety Section:**
- [ ] 🔴 Data Safety form completed in Google Play Console — all data types collected declared:
  - *(Location, Personal info, Health & Fitness, Financial info, etc.)*
- [ ] 🔴 Data shared with third parties declared (e.g., analytics SDKs, ad networks)
- [ ] 🔴 Data encryption in transit declared if applicable

**Content Rating:**
- [ ] 🔴 Content rating questionnaire completed — IARC rating generated and accurate

**Target Audience:**
- [ ] 🔴 Target age group declared — if app targets children (under 13), complies with COPPA and Families Policy
- [ ] 🔴 App does not contain ads if targeting children under 13

**Technical:**
- [ ] 🔴 App targets Android API level within Google's requirements *(check current minimum target API at developer.android.com — updated annually)*
- [ ] 🔴 App tested on Android 10, 11, 12, 13, and 14 (or latest 4 versions)
- [ ] 🔴 64-bit APK/AAB (Android App Bundle) used — 32-bit only is not accepted
- [ ] 🔴 Signed with an upload key *(Google manages the final signing via Play App Signing)*
- [ ] 🔴 In-app billing uses Google Play Billing Library for digital goods
- [ ] 🟡 Internal / closed testing track used before open testing — minimum `📝 [e.g., 10]` testers

**Release:**
- [ ] 🔴 Production release created in Play Console
- [ ] 🔴 Rollout percentage set: `[ ] 10%  [ ] 20%  [ ] 100%` *(staged rollout recommended — start at 10–20%)*
- [ ] 🟡 Pre-launch report reviewed in Play Console (Google auto-tests your app on real devices)

---

## Appendix B · AI Prompt Library

> **What is this?** A reusable library of prompts that work well for common AI-assisted development tasks. Copy a prompt, fill in the `[PLACEHOLDERS]`, and paste it into Claude, ChatGPT, or your AI tool of choice.
>
> **How to maintain this:** Add a new row to the table whenever you discover a prompt that saves significant time. Mark it with a ⭐ if it's been used on 3+ projects.

### B.1 · Prompt Library Table

| ID | Category | Task | Prompt Template | Works Well With | Rating |
|----|----------|------|----------------|----------------|--------|
| P001 | Code Review | General code review | `Review this [LANGUAGE] code for: (1) security issues, (2) performance problems, (3) readability. List findings by severity. Code: [PASTE CODE]` | Claude, ChatGPT, Copilot | `📝 ⭐` |
| P002 | Testing | Generate unit tests | `Write comprehensive unit tests for this [LANGUAGE] function. Include: happy path, edge cases, error cases, and boundary values. Use [TEST FRAMEWORK]. Function: [PASTE CODE]` | Claude, Copilot | `📝` |
| P003 | Security | Security review | `Perform a security review of this code. Look specifically for: SQL injection, XSS, CSRF, insecure deserialization, improper authentication, and exposed secrets. Explain each finding in plain English and provide a fix. Code: [PASTE CODE]` | Claude, ChatGPT | `📝` |
| P004 | Documentation | Write inline comments | `Add clear, concise inline comments to this code. Comments should explain *why* the code does something, not just *what* it does. Keep comments under 1 line where possible. Code: [PASTE CODE]` | Claude, Copilot | `📝` |
| P005 | Documentation | Write API docs | `Write OpenAPI 3.0 documentation for this API endpoint. Include: description, request parameters, request body schema, response schemas (200, 400, 401, 500), and one example each. Endpoint details: [PASTE DETAILS]` | Claude, ChatGPT | `📝` |
| P006 | Debugging | Explain error | `I'm getting this error: [PASTE ERROR]. My code is: [PASTE CODE]. Explain what's causing this in plain English and give me the fix. Also tell me how to prevent this error in future.` | Claude, ChatGPT | `📝` |
| P007 | Architecture | Design review | `Review this system architecture for a [DESCRIBE PRODUCT]. Look for: single points of failure, scalability bottlenecks, security gaps, and missing components for a production system. Diagram/description: [PASTE]` | Claude | `📝` |
| P008 | Compliance | GDPR check | `Review this feature description and identify all GDPR implications: what personal data is collected, how it should be handled, what user rights apply, and what we need to add (consent, retention policy, deletion mechanism). Feature: [DESCRIBE FEATURE]` | Claude, ChatGPT | `📝` |
| P009 | Performance | Optimise code | `This code is running too slowly. Analyse it and suggest specific optimisations. Show before/after code. Explain the performance improvement for each change. Code: [PASTE CODE]` | Claude, ChatGPT | `📝` |
| P010 | Testing | Generate E2E test | `Write a Playwright end-to-end test for this user journey: [DESCRIBE JOURNEY]. Include: setup, navigation steps, assertions for success state, and assertions that verify no errors occurred. Base URL: [URL]` | Claude | `📝` |
| P011 | AI Audit | Review AI-generated code | `I used an AI tool to generate this code. Before I use it in production, please: (1) identify anything the AI might have hallucinated or gotten wrong, (2) flag any security issues typical of AI-generated code, (3) check that it actually does what the comment says it does. Code: [PASTE CODE]` | Claude | `📝` |

### B.2 · How to Add a New Prompt

When you find a prompt that works well, add it to the table above using this format:

```
| P0XX | [Category] | [Task in 4 words] | `[Your prompt with [PLACEHOLDERS] in capitals]` | [AI tool it works with] | `📝` |
```

**Categories available:** `Code Review` · `Testing` · `Security` · `Documentation` · `Debugging` · `Architecture` · `Compliance` · `Performance` · `AI Audit` · `Planning`

---

## Appendix C · Sprint / Cycle Planning Template

> **When to use this:** Fill this out at the **start** of each Shape Up cycle or sprint, before any development begins. This is the companion to your Definition of Done — it defines what you're attempting; the DoD defines when it's finished.
>
> **Keep one copy of this per cycle.** Name the file: `cycles/cycle-[number]-[short-name].md`  
> *(Example: `cycles/cycle-03-user-onboarding.md`)*

---

### Cycle / Sprint Header

| Field | Value |
|-------|-------|
| **Cycle Number** | `📝 [e.g., Cycle 3]` |
| **Cycle Name** | `📝 [e.g., User Onboarding & Email Flow]` |
| **Start Date** | `📝 YYYY-MM-DD` |
| **End Date** | `📝 YYYY-MM-DD` |
| **Cycle Length** | `📝 [e.g., 6 weeks / 2 weeks]` |
| **Lead** | `📝 [Name]` |
| **Goal in one sentence** | `📝 [What is the single most important outcome of this cycle?]` |

---

### C.1 · Cycle Goal & Success Metrics

> **The Cycle Goal** is the one thing that, if achieved, makes this cycle a success even if nothing else gets done.

**Cycle Goal:**
```
📝 [Write 1-2 sentences. Example: "Users can sign up, verify their email, and reach the dashboard in under 2 minutes without any help."]
```

**How we will measure success:**

| Metric | Target | How Measured |
|--------|--------|-------------|
| `📝 [e.g., Onboarding completion rate]` | `📝 [e.g., ≥ 70%]` | `📝 [e.g., PostHog funnel]` |
| `📝` | `📝` | `📝` |
| `📝` | `📝` | `📝` |

---

### C.2 · Planned Work (Scope)

> List every story, task, or feature you plan to complete this cycle. Be specific — vague tasks lead to vague "done."

| ID | Story / Task | Priority | Estimated Effort | Assigned To | Status |
|----|-------------|----------|-----------------|-------------|--------|
| `S01` | `📝 [e.g., Build email verification flow]` | `🔴 Must` | `📝 [e.g., 3 days]` | `📝` | `[ ] Not started` |
| `S02` | `📝` | `🟡 Should` | `📝` | `📝` | `[ ] Not started` |
| `S03` | `📝` | `💡 Nice` | `📝` | `📝` | `[ ] Not started` |
| `S04` | `📝` | `📝` | `📝` | `📝` | `[ ] Not started` |
| `S05` | `📝` | `📝` | `📝` | `📝` | `[ ] Not started` |

**Priority Key:** 🔴 Must complete this cycle · 🟡 Should complete if time allows · 💡 Nice to have

**Total estimated effort this cycle:** `📝 [e.g., ~18 developer-days]`  
**Available capacity:** `📝 [e.g., ~20 developer-days after meetings, bugs, and buffer]`

---

### C.3 · Out of Scope (Intentional Exclusions)

> List things you are **deliberately NOT doing** this cycle, even if someone might expect them. This prevents scope creep.

- `📝 [e.g., Social login (Google/Apple Sign-In) — planned for Cycle 4]`
- `📝 [e.g., Admin dashboard — separate project]`
- `📝`

---

### C.4 · Dependencies & Risks

**Dependencies:** Things you need from outside this cycle before you can complete work.

| Dependency | Owner | Needed By | Status |
|-----------|-------|-----------|--------|
| `📝 [e.g., Transactional email provider API keys]` | `📝 [e.g., Ops / Founder]` | `📝 YYYY-MM-DD` | `[ ] ✅ Ready  [ ] ⏳ Pending` |
| `📝` | `📝` | `📝` | `[ ] ✅  [ ] ⏳` |

**Risks:** Things that might stop this cycle from succeeding.

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|-----------|
| `📝 [e.g., Email deliverability issues delay testing]` | `🟡 Medium` | `🔴 High` | `📝 [e.g., Test with Mailtrap early; have SendGrid backup ready]` |
| `📝` | `📝` | `📝` | `📝` |

---

### C.5 · AI Usage Plan for This Cycle

> Plan how you will use AI tools this cycle. This makes AI assistance deliberate, not accidental.

| Task | AI Tool | How AI Will Help | Human Review Step |
|------|---------|-----------------|------------------|
| `📝 [e.g., Write unit tests for AuthService]` | `📝 [e.g., Claude]` | `📝 [e.g., Generate test cases from function signatures]` | `📝 [e.g., Review each test manually; run against intentionally broken code]` |
| `📝` | `📝` | `📝` | `📝` |
| `📝` | `📝` | `📝` | `📝` |

---

### C.6 · Cycle Retrospective

> **Fill this in at the END of the cycle, not the beginning.** Honest retrospectives make every future cycle better.

**Date of Retrospective:** `📝 YYYY-MM-DD`

**What went well?**
```
📝 [List 2–4 things. Be specific. "Tests were fast to write" not "things went fine."]
```

**What didn't go well?**
```
📝 [List 2–4 things. Be honest. This is private — it's for improvement, not blame.]
```

**What will we do differently next cycle?**
```
📝 [List 1–3 specific, actionable changes. Each one should start with a verb: "Write", "Stop", "Start", "Add".]
```

**Stories completed vs. planned:**

| Planned Stories | Completed | Not Completed (moved to backlog) |
|----------------|-----------|--------------------------------|
| `📝 [Total]` | `📝 [Total]` | `📝 [Total + IDs]` |

**Cycle Goal achieved?** `[ ] ✅ Yes  [ ] ❌ No  [ ] 🟡 Partially`

**If partially or not achieved — why?**
```
📝 [One paragraph, no blame. What can be changed?]
```

---

*This document is a living agreement. Review and update it at the start of every major cycle or whenever your team, tech stack, or compliance requirements change.*

**Document Owner:** `📝 [Name]`  
**Review Frequency:** `📝 [e.g., Every 6-week cycle / Quarterly]`  
**Next Scheduled Review:** `📝 YYYY-MM-DD`
