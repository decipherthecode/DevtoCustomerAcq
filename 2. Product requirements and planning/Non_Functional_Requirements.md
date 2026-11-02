# 📖 How to Fill This Document

> **Read this section first — it takes 3 minutes and saves hours of confusion.**

## What are Non-Functional Requirements (NFRs)?

Think of your product like a car. **Functional requirements** describe *what the car does* — it drives, it has a radio, it has seats. **Non-Functional Requirements describe *how well* the car does those things** — it goes 0–60 in 4 seconds, it uses regular fuel, it survives a crash test at 40 mph.

NFRs answer questions like:
- "How fast does the app need to load?"
- "What happens if the server crashes at 2am?"
- "Who is allowed to see patient data?"
- "Can it handle 10,000 users at once?"

Without NFRs, engineers build something that *works* but may be *too slow, not secure, or breaks under pressure.*

---

## How to Fill Each Section

| Symbol | Meaning |
|--------|---------|
| `[ ]` | **Fill this in** — replace the brackets with your answer |
| `(e.g. ...)` | Example — shows you what a good answer looks like |
| `⚠️ Required` | Must be filled. Don't leave blank. |
| `💡 Optional` | Fill if it applies to your project |
| `🤖 AI-Specific` | Only fill if your product uses AI/ML features |
| `🔒 Compliance` | Fill if your product handles personal, medical, or financial data |
| `📏 Measure` | This is how engineers will TEST that the requirement is met |

---

## Step-by-Step Instructions

**Step 1** — Fill in the **Document Information** section at the top (your project name, who you are, and today's date).

**Step 2** — Go section by section. Don't skip — even writing "Not applicable for this project" is better than leaving it blank.

**Step 3** — For every requirement you write, ask yourself: *"How would we know if this was broken?"* That answer goes in the `📏 How We Measure It` field.

**Step 4** — When you're done, share with your tech lead or senior engineer. They will tell you if anything needs to be more specific.

**Step 5** — Keep this document updated every time requirements change. It lives in your Git repo alongside the code.

---

## Golden Rules

1. **Be specific.** "The app should be fast" is useless. "The home page loads in under 2 seconds on a 4G mobile connection" is perfect.
2. **Use numbers wherever possible.** Instead of "the system should handle many users," write "the system must handle 500 concurrent users."
3. **If you don't know a number yet, write `TBD` and flag it.** Never leave a blank.
4. **Every requirement needs an owner.** Someone must be responsible for delivering it.
5. **This is a living document.** Update it — don't let it go stale.

---
---

<!-- ============================================================ -->
<!-- START OF THE ACTUAL DOCUMENT                                 -->
<!-- ============================================================ -->

# Non-Functional Requirements (NFR)

---

## 📄 Document Information

> ⚠️ **Required** — Fill this out before sharing with your team.

| Field | Your Answer |
|-------|------------|
| **Project / Product Name** | `[ ]` *(e.g., MediConnect Patient Portal)* |
| **Product Version** | `[ ]` *(e.g., v1.0 — Initial Launch)* |
| **Document Version** | `[ ]` *(e.g., v0.1 — Draft / v1.0 — Approved)* |
| **Date Created** | `[ ]` *(e.g., 2026-10-14)* |
| **Last Updated** | `[ ]` |
| **Document Owner** | `[ ]` *(Full name + role, e.g., Jane Smith — Product Manager)* |
| **Reviewed By** | `[ ]` *(Full name + role, e.g., Ahmed Khan — Lead Engineer)* |
| **Approved By** | `[ ]` *(Full name + role, e.g., CEO / CTO)* |
| **Target Launch Date** | `[ ]` *(e.g., Q1 2027)* |
| **First 500 Customers Goal Date** | `[ ]` *(e.g., Q2 2027)* |
| **Linked PRD / Feature Spec** | `[ ]` *(Link to your Product Requirements Document)* |
| **Linked Architecture Doc** | `[ ]` *(Link to technical design doc)* |
| **Status** | `[ ]` *(Draft / In Review / Approved / Superseded)* |

---

## 🗺️ Revision History

> Track every change. Engineers need to know what changed and when.

| Version | Date | Changed By | What Changed |
|---------|------|-----------|-------------|
| v0.1 | `[ ]` | `[ ]` | Initial draft |
| `[ ]` | `[ ]` | `[ ]` | `[ ]` |

---

## 🏗️ Section 1 — Project Overview & Context

> ⚠️ **Required** — Helps everyone reading this document understand *what* is being built and *for whom*.

### 1.1 Product Description

**In plain English, what does this product do?**

```
[ ] Write 2–4 sentences describing your product.

e.g., "MediConnect is a web and mobile platform that allows patients to 
book appointments, access their health records, and message their doctors. 
It is used by hospitals, clinics, and individual practitioners in North 
America and the EU."
```

### 1.2 Target Users

**Who will use this product?**

```
Primary Users:   [ ]  (e.g., Patients aged 18–70, low-to-medium tech literacy)
Secondary Users: [ ]  (e.g., Doctors, Nurses, Hospital Admins)
Admin Users:     [ ]  (e.g., Internal ops team, support agents)
```

### 1.3 Deployment Environment

**Where will the product run?**

- **Cloud Provider:** `[ ]` *(e.g., AWS / GCP / Azure / Multi-cloud)*
- **Regions:** `[ ]` *(e.g., US-East, EU-West — this matters for privacy law)*
- **Deployment Model:** `[ ]` *(e.g., SaaS / On-premise / Hybrid)*
- **Client Platforms:** `[ ]` *(e.g., Web browser + iOS + Android)*
- **Minimum Supported OS/Browser:** `[ ]` *(e.g., iOS 15+, Android 10+, Chrome 110+, Safari 16+)*

### 1.4 NFR Priority Key

> Use this scale consistently throughout the document.

| Priority Level | Meaning |
|---------------|---------|
| 🔴 **P1 — Critical** | Product cannot launch without this. No exceptions. |
| 🟠 **P2 — High** | Must be done before launch. Exceptions need exec sign-off. |
| 🟡 **P3 — Medium** | Important, but can be deferred to next sprint/release. |
| 🟢 **P4 — Low** | Nice to have. Does not block launch. |

---

## ⚡ Section 2 — Performance Requirements

> **Plain English:** How *fast* and *responsive* must the product be?
>
> Bad performance kills products. Studies show 53% of users abandon a mobile site if it takes longer than 3 seconds to load. Be specific here.

### 2.1 Page / Screen Load Time

| Requirement | Target | Worst Acceptable | Priority | 📏 How We Measure It |
|-------------|--------|-----------------|----------|----------------------|
| **First page load (web)** | `[ ]` *(e.g., < 2 sec)* | `[ ]` *(e.g., < 4 sec)* | `[ ]` | Lighthouse score, WebPageTest on a simulated 4G connection |
| **First screen load (mobile app)** | `[ ]` *(e.g., < 3 sec)* | `[ ]` *(e.g., < 5 sec)* | `[ ]` | Firebase Performance Monitoring |
| **Subsequent page navigation** | `[ ]` *(e.g., < 1 sec)* | `[ ]` *(e.g., < 2 sec)* | `[ ]` | In-app timing measurements |
| **API response time (95th percentile)** | `[ ]` *(e.g., < 300 ms)* | `[ ]` *(e.g., < 1 sec)* | `[ ]` | APM tool (e.g., Datadog, New Relic) |
| **API response time (99th percentile)** | `[ ]` *(e.g., < 800 ms)* | `[ ]` *(e.g., < 2 sec)* | `[ ]` | APM tool |
| **Search / Query response** | `[ ]` *(e.g., < 500 ms)* | `[ ]` *(e.g., < 1.5 sec)* | `[ ]` | Load test with realistic data volume |
| **File upload (per MB)** | `[ ]` *(e.g., < 2 sec per MB)* | `[ ]` | `[ ]` | Manual + automated test |
| **Report / Data export generation** | `[ ]` *(e.g., < 10 sec)* | `[ ]` *(e.g., < 30 sec)* | `[ ]` | Automated test with max dataset size |

### 2.2 🤖 AI / LLM Performance

> Only fill if your product uses AI features (chatbots, copilots, agents, recommendations).

| Requirement | Target | Worst Acceptable | Priority | 📏 How We Measure It |
|-------------|--------|-----------------|----------|----------------------|
| **AI response — time to first token** | `[ ]` *(e.g., < 1.5 sec)* | `[ ]` *(e.g., < 3 sec)* | `[ ]` | Latency monitoring on LLM API calls |
| **AI response — full response time** | `[ ]` *(e.g., < 8 sec)* | `[ ]` *(e.g., < 20 sec)* | `[ ]` | End-to-end timing per session |
| **AI agent task completion time** | `[ ]` *(e.g., < 30 sec for a 3-step workflow)* | `[ ]` | `[ ]` | Workflow execution logs |
| **AI availability (uptime)** | `[ ]` *(e.g., 99.5%)* | `[ ]` | `[ ]` | Uptime monitoring with fallback alerts |
| **Fallback if AI provider is down** | `[ ]` *(e.g., Show cached response / degrade gracefully)* | — | `[ ]` | Circuit breaker test |
| **Max tokens per request (cost control)** | `[ ]` *(e.g., 4,000 tokens per user query)* | — | `[ ]` | Token logging per API call |

### 2.3 Background / Async Jobs

| Job Type | Max Execution Time | Priority |
|----------|-------------------|---------|
| `[ ]` *(e.g., Email notifications)* | `[ ]` *(e.g., < 5 min)* | `[ ]` |
| `[ ]` *(e.g., PDF report generation)* | `[ ]` *(e.g., < 2 min)* | `[ ]` |
| `[ ]` *(e.g., Data sync with EHR)* | `[ ]` *(e.g., < 15 min)* | `[ ]` |

---

## 📈 Section 3 — Scalability Requirements

> **Plain English:** Can the system grow as more people use it — without breaking?
>
> Think of a restaurant: a great chef can cook for 10 people. But can the kitchen handle 500 people on a Friday night? Scalability planning answers that question before it becomes a crisis.

### 3.1 Current & Target Load

| Metric | At Launch | At 500 Customers | Peak Load (Worst Case) |
|--------|-----------|-----------------|----------------------|
| **Concurrent users** | `[ ]` | `[ ]` | `[ ]` |
| **Registered users (total)** | `[ ]` | `[ ]` | `[ ]` |
| **API requests per second** | `[ ]` | `[ ]` | `[ ]` |
| **Data stored (GB/TB)** | `[ ]` | `[ ]` | `[ ]` |
| **File uploads per day** | `[ ]` | `[ ]` | `[ ]` |
| **AI/LLM API calls per day** | `[ ]` | `[ ]` | `[ ]` |

### 3.2 Scaling Strategy

**How will the system scale when load increases?**

- **Horizontal Scaling (add more servers):** `[ ]` *(Yes / No / Not decided yet)*
- **Vertical Scaling (upgrade existing servers):** `[ ]` *(Yes / No)*
- **Auto-scaling enabled:** `[ ]` *(Yes / No — which service?)*
- **Database scaling approach:** `[ ]` *(e.g., Read replicas, sharding, caching layer)*
- **CDN for static assets:** `[ ]` *(Yes / No — which CDN?)*
- **Caching strategy:** `[ ]` *(e.g., Redis cache for sessions and API responses)*

### 3.3 Growth Assumptions

```
Expected monthly user growth rate:     [ ]  (e.g., 20% month-over-month for 6 months)
Peak usage time of day:                [ ]  (e.g., 9am–12pm local user timezone)
Seasonal spikes expected:              [ ]  (e.g., Yes — end-of-year reports in December)
Spike handling plan:                   [ ]  (e.g., Pre-scale 2x capacity before known spikes)
```

---

## 🛡️ Section 4 — Availability & Reliability

> **Plain English:** How often must the system be working — and what happens when it breaks?
>
> "99% uptime" sounds great. But that still means 3.65 days of downtime per year. "99.9% uptime" means 8.7 hours. Know what you need before you build.

### 4.1 Uptime & SLA Targets

| Environment | Uptime Target | Allowed Downtime / Month | Priority |
|-------------|-------------|--------------------------|---------|
| **Production** | `[ ]` *(e.g., 99.9%)* | `[ ]` *(e.g., ~43 min/month)* | `[ ]` |
| **Staging / Pre-prod** | `[ ]` *(e.g., 99%)* | `[ ]` | `[ ]` |
| **Development** | `[ ]` *(e.g., Best effort)* | — | `[ ]` |

> 💡 **Uptime Reference Table**

| Uptime % | Downtime / Month | Downtime / Year |
|----------|-----------------|----------------|
| 99% | ~7.2 hours | ~3.65 days |
| 99.5% | ~3.6 hours | ~1.83 days |
| 99.9% | ~43 minutes | ~8.7 hours |
| 99.95% | ~22 minutes | ~4.4 hours |
| 99.99% | ~4 minutes | ~52 minutes |

### 4.2 Recovery Targets

> If something goes wrong, how fast must it be fixed?

| Metric | Definition | Target |
|--------|-----------|--------|
| **RTO — Recovery Time Objective** | Maximum time the system can be down before it must be back up | `[ ]` *(e.g., 1 hour)* |
| **RPO — Recovery Point Objective** | Maximum amount of data we can afford to lose (measured in time) | `[ ]` *(e.g., 15 minutes of data)* |
| **MTTR — Mean Time to Restore** | Average time to fix an incident once it's detected | `[ ]` *(e.g., < 30 minutes)* |
| **MTBF — Mean Time Between Failures** | Average time between system failures | `[ ]` *(e.g., > 30 days)* |

### 4.3 Maintenance Windows

```
Scheduled maintenance allowed:         [ ]  (Yes / No)
Preferred maintenance window:          [ ]  (e.g., Sundays 2am–5am UTC)
Advance notice to users required:      [ ]  (e.g., 48 hours via email + in-app banner)
Zero-downtime deployment required:     [ ]  (Yes / No)
```

### 4.4 Failure & Incident Response

```
On-call rotation set up:               [ ]  (Yes / No — who is primary on-call?)
Alerting tool:                         [ ]  (e.g., PagerDuty / OpsGenie / Slack alerts)
Incident severity definitions:         [ ]  (Link to runbook / incident management doc)
Status page for users:                 [ ]  (Yes / No — link: ___)
```

---

## 🔒 Section 5 — Security Requirements

> **Plain English:** How do we make sure only the right people see the right data — and no one can hack, steal, or tamper with it?
>
> Security is not a feature — it is the foundation. One breach can destroy years of trust.

### 5.1 Authentication & Identity

| Requirement | Decision | Notes |
|-------------|---------|-------|
| **Login method** | `[ ]` *(e.g., Email + password, Google SSO, Magic link)* | |
| **Multi-Factor Authentication (MFA)** | `[ ]` *(Required / Optional / Not supported)* | `[ ]` *(Who must use MFA? e.g., All admin accounts)* |
| **Single Sign-On (SSO)** | `[ ]` *(Yes / No — which provider? e.g., Okta, Azure AD)* | |
| **Session timeout (idle)** | `[ ]` *(e.g., 30 minutes of inactivity)* | |
| **Session timeout (absolute)** | `[ ]` *(e.g., Force re-login after 8 hours)* | |
| **Max failed login attempts before lockout** | `[ ]` *(e.g., 5 attempts, then 15-minute lockout)* | |
| **Password policy** | `[ ]` *(e.g., Min 12 chars, 1 uppercase, 1 number, 1 symbol)* | |
| **Password storage** | Must use bcrypt or Argon2 hashing — never plain text | ⚠️ Non-negotiable |

### 5.2 Authorization & Access Control

```
Authorization model used:             [ ]  (e.g., Role-Based Access Control — RBAC)
Roles defined:                        [ ]  (e.g., Super Admin / Admin / Doctor / Patient / Guest)
Principle of least privilege applied: [ ]  (Yes / No — users get minimum access needed)
Admin actions require re-auth:        [ ]  (Yes / No)
API access requires token:            [ ]  (Yes — JWT / OAuth 2.0 / API Key)
Token expiry:                         [ ]  (e.g., Access token 15 min, Refresh token 7 days)
```

### 5.3 Data Encryption

| Where | Encryption Required | Standard |
|-------|---------------------|---------|
| **Data at rest (databases, files)** | `[ ]` *(Yes / No)* | `[ ]` *(e.g., AES-256)* |
| **Data in transit (network)** | `[ ]` *(Yes / No)* | `[ ]` *(e.g., TLS 1.2 minimum, TLS 1.3 preferred)* |
| **Backups** | `[ ]` *(Yes / No)* | `[ ]` *(e.g., Encrypted S3 backups)* |
| **Sensitive fields (e.g., SSN, card numbers)** | `[ ]` *(Yes / No)* | `[ ]` *(e.g., Column-level encryption)* |
| **Mobile app local storage** | `[ ]` *(Yes / No)* | `[ ]` *(e.g., iOS Keychain / Android Keystore)* |

### 5.4 Vulnerability & Threat Management

```
Dependency vulnerability scanning:    [ ]  (e.g., Snyk / GitHub Dependabot — run on every PR)
Static code analysis (SAST):          [ ]  (e.g., SonarQube / Semgrep)
Penetration testing:                  [ ]  (Yes / No — frequency: e.g., Annually, Before launch)
Bug bounty program:                   [ ]  (Yes / No)
Security headers enforced:            [ ]  (e.g., CSP, HSTS, X-Frame-Options)
SQL injection protection:             [ ]  (e.g., Parameterized queries / ORM — no raw SQL)
XSS protection:                       [ ]  (e.g., Input sanitization + output encoding)
CSRF protection:                      [ ]  (e.g., CSRF tokens on all state-changing requests)
Rate limiting on APIs:                [ ]  (Yes — how many req/min per user? e.g., 100/min)
DDoS protection:                      [ ]  (e.g., Cloudflare / AWS Shield)
```

### 5.5 🤖 AI-Specific Security

> Only fill if your product includes AI/LLM features.

```
Prompt injection protection:          [ ]  (e.g., Input validation, sandboxed prompts, output filtering)
LLM output sanitization:              [ ]  (Yes — all AI output is filtered before displaying to users)
Sensitive data in prompts:            [ ]  (Policy: Never send PII/PHI to LLM providers? Yes / No)
AI provider data retention policy:    [ ]  (e.g., OpenAI API — zero data retention confirmed?)
Model access restricted to backend:   [ ]  (Yes — users cannot call LLM APIs directly)
AI audit logging:                     [ ]  (Yes — all prompts and responses are logged with user ID)
Jailbreak / misuse prevention:        [ ]  (e.g., Content moderation layer, usage policies enforced)
```

---

## 📜 Section 6 — Compliance & Regulatory Requirements

> **Plain English:** Laws and regulations that tell us *what we must do* — or face fines, lawsuits, or shutdown.
>
> This is not optional. Ignoring compliance requirements is how startups get sued out of existence.

### 6.1 Applicability

> Check which regulations apply to your product:

| Regulation | Applies? | Geographic Scope | Notes |
|-----------|---------|-----------------|-------|
| **GDPR** *(EU data protection)* | `[ ]` *(Yes / No / TBD)* | EU + EEA users | |
| **CCPA** *(California privacy)* | `[ ]` | California residents | |
| **HIPAA** *(US healthcare data)* | `[ ]` | USA | Required if handling PHI |
| **SOC 2 Type I / II** *(Security certification)* | `[ ]` | USA (used globally) | |
| **ISO 27001** *(Security management)* | `[ ]` | International | |
| **PCI DSS** *(Payment card data)* | `[ ]` | All regions | Required if handling card payments |
| **WCAG 2.1 AA** *(Accessibility)* | `[ ]` | International | |
| **Other:** `[ ]` | `[ ]` | `[ ]` | |

### 6.2 🔒 GDPR Requirements

> Required if your product is used by people in the EU, UK, or EEA — or if you store any EU citizen data.

```
Data Protection Officer (DPO) appointed:         [ ]  (Yes / No — name if yes)
Privacy Policy published:                        [ ]  (Yes / No — link)
Cookie consent banner implemented:               [ ]  (Yes / No)
Legal basis for processing documented:           [ ]  (e.g., Consent / Legitimate Interest / Contract)
User rights supported:
  • Right to Access (download my data):          [ ]  (Yes / No)
  • Right to Erasure (delete my account):        [ ]  (Yes / No)
  • Right to Rectification (correct my data):    [ ]  (Yes / No)
  • Right to Portability (export my data):       [ ]  (Yes / No)
  • Right to Object (stop processing):           [ ]  (Yes / No)
Data retention policy defined:                   [ ]  (e.g., Delete inactive accounts after 3 years)
Data breach notification SLA:                    [ ]  (Must notify authorities within 72 hours of discovery)
Sub-processors list documented:                  [ ]  (Yes — link to list)
Data Processing Agreements (DPAs) signed:        [ ]  (Yes — with which vendors?)
Cross-border data transfer mechanism:            [ ]  (e.g., Standard Contractual Clauses / EU-US DPF)
```

### 6.3 🔒 HIPAA Requirements

> Required if your product stores, transmits, or processes Protected Health Information (PHI) in the USA.

```
PHI data identified and documented:              [ ]  (Yes — what types? e.g., Diagnosis codes, prescriptions)
Business Associate Agreements (BAAs) signed:     [ ]  (Yes — with all vendors handling PHI)
PHI encrypted at rest and in transit:            [ ]  (Yes — AES-256 / TLS 1.2+)
PHI access logs maintained:                     [ ]  (Yes — who accessed what, when, from where)
PHI minimum necessary policy enforced:           [ ]  (Users only see PHI they need)
PHI stored in US-only regions:                  [ ]  (Yes / No — specify regions)
Audit trail for all PHI access:                 [ ]  (Yes — retained for how long? e.g., 6 years)
Breach notification plan:                        [ ]  (Yes — notify affected patients within 60 days)
Employee HIPAA training:                         [ ]  (Yes — all staff with PHI access trained)
```

### 6.4 🔒 SOC 2 Requirements

```
Trust Service Criteria targeted:                 [ ]  (e.g., Security + Availability + Confidentiality)
SOC 2 Type:                                      [ ]  (Type I — point-in-time / Type II — 6–12 month audit)
Target audit date:                               [ ]  
Audit firm selected:                             [ ]  (e.g., Vanta-managed / Drata / direct auditor)
Security policies documented:                    [ ]  (Yes — link to policy library)
Access review frequency:                         [ ]  (e.g., Quarterly access reviews)
Change management process in place:              [ ]  (Yes — link to change management runbook)
```

---

## ♿ Section 7 — Accessibility Requirements

> **Plain English:** Can people with disabilities use our product? This is both a legal requirement in many countries and the right thing to do.

```
Accessibility standard targeted:       [ ]  (e.g., WCAG 2.1 Level AA — recommended minimum)
Screen reader compatible:              [ ]  (Yes — tested with VoiceOver / TalkBack / NVDA)
Keyboard navigation supported:         [ ]  (Yes — all features accessible without a mouse)
Color contrast ratio:                  [ ]  (e.g., Minimum 4.5:1 for normal text, per WCAG AA)
Text resize support:                   [ ]  (Yes — up to 200% zoom without content breaking)
Alt text for all images:               [ ]  (Yes — implemented in code review checklist)
Video captions:                        [ ]  (Yes / No — if product includes video content)
Focus indicator visible:               [ ]  (Yes — keyboard focus is always visible)
Accessibility audit tool:              [ ]  (e.g., axe DevTools, Lighthouse, manual audit)
Audit frequency:                       [ ]  (e.g., Before every major release)
```

---

## 🌍 Section 8 — Usability & User Experience Requirements

> **Plain English:** How easy is the product to use? How should it feel?
>
> A product that works but is confusing will lose customers. Usability requirements keep the team aligned on experience quality.

### 8.1 General UX Standards

```
Time to complete key user task:        [ ]  (e.g., New user books first appointment in < 3 minutes)
User onboarding completion target:     [ ]  (e.g., 80% of new users complete onboarding in < 5 min)
Error message clarity:                 [ ]  (All error messages explain what went wrong AND what to do next)
Mobile-first design:                   [ ]  (Yes / No — mobile vs desktop priority)
Offline mode support:                  [ ]  (Yes / No — which features work offline?)
Multi-language support (i18n):         [ ]  (Yes / No — which languages at launch?)
RTL (right-to-left) language support:  [ ]  (Yes / No — e.g., Arabic, Hebrew)
```

### 8.2 Feedback & Satisfaction

```
In-app feedback mechanism:             [ ]  (e.g., Thumbs up/down on AI responses, NPS survey)
Target CSAT score:                     [ ]  (e.g., ≥ 4.0 out of 5.0)
Target NPS score:                      [ ]  (e.g., ≥ 40)
User error rate target:                [ ]  (e.g., < 5% of sessions encounter a blocking error)
Support ticket SLA:                    [ ]  (e.g., First response within 4 business hours)
```

---

## 🔧 Section 9 — Maintainability & Code Quality

> **Plain English:** How easy is it for engineers to update, fix, or improve the product over time?
>
> A codebase that's hard to maintain slows down every future feature and makes bugs harder to fix.

```
Test coverage minimum:                 [ ]  (e.g., 80% unit test coverage on all new code)
Code review policy:                    [ ]  (e.g., All PRs require 2 approvals before merging)
CI/CD pipeline required:               [ ]  (Yes — automated tests must pass before deployment)
Deployment frequency target:           [ ]  (e.g., Can deploy to production daily)
Max deployment time (CI/CD pipeline):  [ ]  (e.g., < 15 minutes from commit to production)
Feature flags used:                    [ ]  (Yes / No — for safe rollouts without redeployment)
Technical debt tracking:               [ ]  (e.g., Tracked in Jira / Linear with a monthly review)
Logging standard:                      [ ]  (e.g., Structured JSON logs — no plain text logs)
Documentation required for:            [ ]  (e.g., All APIs, all environment variables, all runbooks)
Dependency update policy:              [ ]  (e.g., Monthly review, security patches within 48 hours)
Secrets management:                    [ ]  (e.g., No secrets in code — use AWS Secrets Manager / Vault)
```

---

## 🔌 Section 10 — Compatibility & Portability

> **Plain English:** What devices, browsers, and environments does the product need to work on?

### 10.1 Browser Support (Web)

| Browser | Minimum Version | Support Level |
|---------|----------------|--------------|
| Google Chrome | `[ ]` *(e.g., v110+)* | `[ ]` *(Full / Partial)* |
| Mozilla Firefox | `[ ]` *(e.g., v110+)* | `[ ]` |
| Apple Safari | `[ ]` *(e.g., v16+)* | `[ ]` |
| Microsoft Edge | `[ ]` *(e.g., v110+)* | `[ ]` |
| Internet Explorer | Not supported | N/A |

### 10.2 Mobile Device Support

| Platform | Minimum OS | Device Types |
|----------|-----------|-------------|
| iOS | `[ ]` *(e.g., iOS 15+)* | `[ ]` *(e.g., iPhone 11+, iPad)* |
| Android | `[ ]` *(e.g., Android 10+)* | `[ ]` *(e.g., Mid-range and above)* |

### 10.3 Responsive Design

```
Breakpoints supported:                 [ ]  (e.g., Mobile 375px, Tablet 768px, Desktop 1280px+)
Minimum screen width:                  [ ]  (e.g., 320px)
Tablet layout:                         [ ]  (Separate / Same as mobile / Same as desktop)
Print stylesheet needed:               [ ]  (Yes / No — e.g., for printable reports)
```

---

## 📊 Section 11 — Observability, Monitoring & Alerting

> **Plain English:** How do we know the product is healthy — and get woken up when it's not?
>
> You cannot fix what you cannot see. Every production system needs eyes.

### 11.1 Monitoring Stack

```
Application Performance Monitoring:    [ ]  (e.g., Datadog / New Relic / Dynatrace)
Error tracking:                        [ ]  (e.g., Sentry / Bugsnag)
Log aggregation:                       [ ]  (e.g., Datadog Logs / AWS CloudWatch / ELK Stack)
Uptime monitoring:                     [ ]  (e.g., Pingdom / Better Uptime / Datadog Synthetics)
Infrastructure monitoring:             [ ]  (e.g., Grafana + Prometheus)
Real User Monitoring (RUM):            [ ]  (Yes / No — e.g., Datadog RUM for front-end experience)
Mobile crash reporting:                [ ]  (e.g., Firebase Crashlytics)
```

### 11.2 Key Metrics to Monitor

| Metric | Alert Threshold | Alert Channel | Severity |
|--------|---------------|---------------|---------|
| API error rate | `[ ]` *(e.g., > 1% over 5 min)* | `[ ]` *(e.g., PagerDuty)* | 🔴 P1 |
| API p95 latency | `[ ]` *(e.g., > 1 sec)* | `[ ]` | `[ ]` |
| Database CPU | `[ ]` *(e.g., > 80%)* | `[ ]` | `[ ]` |
| Disk usage | `[ ]` *(e.g., > 85%)* | `[ ]` | `[ ]` |
| AI/LLM error rate | `[ ]` *(e.g., > 5%)* | `[ ]` | `[ ]` |
| Failed login rate | `[ ]` *(e.g., > 50/min — possible attack)* | `[ ]` | 🔴 P1 |
| `[ ]` | `[ ]` | `[ ]` | `[ ]` |

### 11.3 Dashboards

```
Operations dashboard created:          [ ]  (Yes / No — shows live system health)
Business metrics dashboard:            [ ]  (Yes / No — shows user growth, feature usage, revenue)
AI / LLM usage dashboard:             [ ]  (Yes / No — shows token usage, latency, cost)
Dashboard link:                        [ ]  
```

---

## 💾 Section 12 — Data Management & Backup

> **Plain English:** How do we safely store data, how long do we keep it, and what happens if data is lost?

### 12.1 Backup Policy

```
Database backup frequency:             [ ]  (e.g., Every 6 hours — automated)
Backup retention period:               [ ]  (e.g., Keep daily backups for 30 days, weekly for 1 year)
Backup storage location:               [ ]  (e.g., Encrypted S3 in a separate AWS region)
Backup tested / restore drill:         [ ]  (Yes — frequency: e.g., Monthly restore test)
Point-in-time recovery (PITR):         [ ]  (Yes / No — up to how many hours back?)
```

### 12.2 Data Retention

| Data Type | Retention Period | Deletion Method |
|-----------|----------------|----------------|
| User accounts (active) | While account is active | Soft delete → hard delete after `[ ]` days |
| User accounts (deleted) | `[ ]` *(e.g., 30 days grace period)* | Hard delete |
| Application logs | `[ ]` *(e.g., 90 days)* | Auto-purge |
| Audit logs | `[ ]` *(e.g., 7 years — HIPAA requirement)* | Archived, not deleted |
| AI prompt/response logs | `[ ]` *(e.g., 12 months)* | Auto-purge |
| Payment records | `[ ]` *(e.g., 7 years)* | Archive |
| `[ ]` | `[ ]` | `[ ]` |

### 12.3 Data Classification

| Classification Level | Examples | Who Can Access | Protection Level |
|---------------------|---------|---------------|-----------------|
| 🔴 **Restricted** | PHI, PII, passwords, payment data | Named individuals only | Encrypted + audit-logged |
| 🟠 **Confidential** | Business data, internal docs | Employees only | Encrypted |
| 🟡 **Internal** | Product analytics, logs | Employees + contractors | Access-controlled |
| 🟢 **Public** | Marketing content, public docs | Anyone | Standard |

---

## 🆘 Section 13 — Disaster Recovery Plan

> **Plain English:** What do we do when things go seriously wrong — a server dies, a database gets corrupted, a security breach happens, or a whole cloud region goes offline?
>
> A Disaster Recovery (DR) plan is your team's emergency playbook. Writing it *before* a disaster is the only time you'll think clearly enough to write it well.

### 13.1 Disaster Recovery Overview

```
DR Plan Owner:                         [ ]  (Person responsible for this plan — name + role)
DR Plan Last Tested:                   [ ]  (Date of last full DR drill)
DR Plan Next Scheduled Test:           [ ]  (e.g., Every 6 months — next: Q1 2027)
DR Contact List:                       [ ]  (Link to on-call contact sheet — keep it updated)
Incident War Room:                     [ ]  (e.g., Slack #incident-response channel)
Customer Communication Lead:           [ ]  (Who sends status updates to customers during DR?)
Executive Notification Required:       [ ]  (e.g., Notify CTO within 15 minutes of P1 incident)
```

### 13.2 Recovery Objectives (Repeat from Section 4 — confirmed for DR context)

| Metric | Target | What It Means |
|--------|--------|--------------|
| **RTO** (Recovery Time Objective) | `[ ]` *(e.g., ≤ 1 hour)* | System must be back online within this time |
| **RPO** (Recovery Point Objective) | `[ ]` *(e.g., ≤ 15 minutes of data loss)* | Maximum data we can afford to lose |
| **MTTR** (Mean Time to Restore) | `[ ]` *(e.g., ≤ 30 minutes)* | Average time to restore service once team is engaged |

### 13.3 Disaster Scenarios & Response Playbooks

> For each scenario, document the steps the team follows. Link to detailed runbooks where they exist.

#### Scenario A — Database Failure / Corruption

```
Trigger:           Database goes offline or data is corrupted
Detection:         [ ]  (e.g., Automated alert via Datadog within 2 minutes)
Response Steps:
  1. [ ]  (e.g., Page on-call engineer via PagerDuty)
  2. [ ]  (e.g., Verify backup exists and last backup time)
  3. [ ]  (e.g., Initiate point-in-time restore from latest backup)
  4. [ ]  (e.g., Validate data integrity after restore)
  5. [ ]  (e.g., Re-enable traffic and verify application health)
  6. [ ]  (e.g., Post-incident review within 48 hours)
Target Recovery Time:  [ ]  (e.g., < 1 hour)
Runbook Link:          [ ]
```

#### Scenario B — Cloud Region / Zone Outage

```
Trigger:           Entire AWS/GCP/Azure region goes down
Detection:         [ ]  (e.g., Cloud provider health dashboard + uptime monitoring alert)
Failover Strategy: [ ]  (e.g., Multi-region active-passive / active-active setup)
Failover Steps:
  1. [ ]  (e.g., Confirm outage via cloud provider status page)
  2. [ ]  (e.g., Activate failover to secondary region — automated or manual?)
  3. [ ]  (e.g., Verify DNS failover has propagated — typically 1–5 min with low TTL)
  4. [ ]  (e.g., Validate application is healthy in failover region)
  5. [ ]  (e.g., Notify customers via status page)
Multi-region enabled:  [ ]  (Yes / No — if No, document the manual steps and accepted RTO)
Secondary region:      [ ]  (e.g., AWS us-west-2 as failover for us-east-1)
Target Recovery Time:  [ ]  (e.g., < 30 minutes with automated DNS failover)
Runbook Link:          [ ]
```

#### Scenario C — Security Breach / Data Exposure

```
Trigger:           Unauthorized access detected; data potentially exfiltrated
Detection:         [ ]  (e.g., Anomaly detection alert / third-party report / security scan)
Immediate Steps:
  1. [ ]  (e.g., Isolate affected systems — revoke compromised credentials immediately)
  2. [ ]  (e.g., Preserve logs — do NOT delete anything until forensics complete)
  3. [ ]  (e.g., Notify Security Lead and Legal team within 30 minutes)
  4. [ ]  (e.g., Assess scope — what data, how many users, since when?)
  5. [ ]  (e.g., Patch the vulnerability before restoring service)
  6. [ ]  (e.g., Regulatory notification — GDPR: 72 hrs; HIPAA: 60 days)
  7. [ ]  (e.g., Notify affected users — template link: ___)
  8. [ ]  (e.g., External communication — press statement if > X users affected)
Legal notification SLA (GDPR):   72 hours from discovery
Legal notification SLA (HIPAA):  60 days from discovery
Breach notification template:     [ ]  (Link to pre-written user notification email)
Forensics firm on retainer:       [ ]  (Yes / No — firm name if yes)
Runbook Link:                     [ ]
```

#### Scenario D — Application / Code Deployment Failure

```
Trigger:           Bad deploy causes errors, crashes, or data issues in production
Detection:         [ ]  (e.g., Error rate spike > 5% within 2 minutes of deployment)
Response Steps:
  1. [ ]  (e.g., Automated rollback triggered — verify it completed)
  2. [ ]  (e.g., If auto-rollback fails: manual rollback via CI/CD pipeline)
  3. [ ]  (e.g., Confirm application is healthy after rollback)
  4. [ ]  (e.g., Investigate root cause — review deployment diff)
  5. [ ]  (e.g., Fix and re-test before re-deploying)
Rollback time target:   [ ]  (e.g., < 5 minutes — automated)
Rollback tool:          [ ]  (e.g., GitHub Actions / ArgoCD / Kubernetes rollback)
Runbook Link:           [ ]
```

#### Scenario E — Third-Party / LLM API Outage

```
Trigger:           Critical third-party service (e.g., Stripe, LLM provider) goes down
Affected Features: [ ]  (List all features that depend on this vendor)
Fallback Behavior:
  • LLM provider down:    [ ]  (e.g., Switch to backup provider / show graceful error message)
  • Payment provider down:[ ]  (e.g., Queue transactions / disable checkout with user message)
  • Email provider down:  [ ]  (e.g., Queue emails and retry when restored)
Detection:         [ ]  (e.g., Vendor status page monitoring + application-level error alerts)
User Communication:[ ]  (e.g., In-app banner: "Some features are temporarily unavailable")
Runbook Link:      [ ]
```

#### Scenario F — Mass Data Deletion (Accidental or Malicious)

```
Trigger:           Significant data deleted — by accident, rogue employee, or attacker
Detection:         [ ]  (e.g., Anomalous DELETE query volume alert)
Response Steps:
  1. [ ]  (e.g., Immediately revoke access credentials of suspected actor)
  2. [ ]  (e.g., Freeze further deletions — read-only mode if possible)
  3. [ ]  (e.g., Identify scope — how much data, which tables, since when?)
  4. [ ]  (e.g., Restore from most recent backup prior to deletion event)
  5. [ ]  (e.g., Validate restored data integrity)
  6. [ ]  (e.g., Notify affected users if their data was impacted)
Soft-delete used (recoverable):    [ ]  (Yes / No — grace period before hard delete?)
Backup restore time target:        [ ]  (e.g., < 2 hours for full restore)
Runbook Link:                      [ ]
```

### 13.4 DR Testing Schedule

| DR Test Type | Frequency | Last Completed | Next Scheduled | Owner |
|-------------|-----------|--------------|---------------|-------|
| **Backup restore drill** | `[ ]` *(e.g., Monthly)* | `[ ]` | `[ ]` | `[ ]` |
| **Failover test (region)** | `[ ]` *(e.g., Quarterly)* | `[ ]` | `[ ]` | `[ ]` |
| **Full DR simulation (tabletop exercise)** | `[ ]` *(e.g., Bi-annually)* | `[ ]` | `[ ]` | `[ ]` |
| **Security breach simulation** | `[ ]` *(e.g., Annually)* | `[ ]` | `[ ]` | `[ ]` |
| **Rollback test on staging** | `[ ]` *(e.g., Every deploy)* | `[ ]` | `[ ]` | `[ ]` |

### 13.5 DR Communication Plan

```
Internal communication channel:        [ ]  (e.g., Slack #incident-response — bridge call if > 30 min)
Customer status page:                  [ ]  (Yes — URL: ___)
Status page tool:                      [ ]  (e.g., Statuspage.io / BetterStack / Atlassian)
Customer notification SLA:             [ ]  (e.g., Notify within 15 minutes of confirmed P1 outage)
Pre-written incident templates:        [ ]  (Yes — link to template library)
Executive escalation path:             [ ]  (e.g., On-call Eng → Eng Manager → CTO → CEO)
PR / Media contact for major incidents:[ ]  (Name + contact — for breaches affecting > 1,000 users)
Post-incident report (PIR) SLA:        [ ]  (e.g., Published within 5 business days of resolution)
```

### 13.6 DR Readiness Checklist

> Check this before every major release and quarterly thereafter.

- [ ] All runbooks are written and accessible (not just in one person's head)
- [ ] Backup restore was tested successfully in the last `[ ]` days
- [ ] On-call rotation is up to date and all members have been briefed
- [ ] Cloud failover has been verified to work
- [ ] All team members know where the status page is and how to update it
- [ ] Regulatory notification templates are pre-written and approved by Legal
- [ ] Secrets/credentials are rotatable within 15 minutes if compromised
- [ ] DR contact list is current (no outdated phone numbers / emails)
- [ ] DR plan has been reviewed and updated in the last `[ ]` months

---

## 🤖 Section 14 — AI / ML Specific Requirements

> **Plain English:** Special quality, safety, and governance rules that apply only to AI-powered features.
>
> AI is powerful — but it can also hallucinate, discriminate, or be misused. These requirements keep it safe and trustworthy.

### 13.1 AI Model Quality

```
AI model accuracy baseline:            [ ]  (e.g., > 85% accuracy on core task — how measured?)
Hallucination rate threshold:          [ ]  (e.g., < 5% of responses contain factually wrong info)
Confidence threshold for display:      [ ]  (e.g., Only show AI output if confidence > 70%)
Human-in-the-loop for high-risk tasks: [ ]  (e.g., AI suggests; human must confirm before action)
AI output review / QA process:         [ ]  (e.g., Weekly red-team testing of 50 sample outputs)
Model version control:                 [ ]  (Yes — all model versions tagged and logged)
Model rollback plan:                   [ ]  (Yes — can revert to previous model in < 15 minutes)
```

### 13.2 AI Ethics & Fairness

```
Bias testing conducted:                [ ]  (Yes / No — on which demographic groups?)
Bias testing frequency:                [ ]  (e.g., Before every model update)
Explainability required:               [ ]  (e.g., AI must provide a reason for its decision)
AI-generated content labeled:          [ ]  (Yes — users can see when content is AI-generated)
Prohibited AI use cases:               [ ]  (e.g., No AI in hiring decisions / no medical diagnosis)
AI safety policy documented:           [ ]  (Yes — link to AI usage policy)
```

### 13.3 AI Cost Management

```
AI API cost budget (monthly):          [ ]  (e.g., < $500/month at launch)
Cost per user action target:           [ ]  (e.g., < $0.05 per AI query)
Token usage monitored:                 [ ]  (Yes — alerts if monthly cost exceeds 80% of budget)
Cost optimization strategy:            [ ]  (e.g., Prompt caching, smaller model for simple tasks)
AI provider SLA:                       [ ]  (e.g., OpenAI / Anthropic — uptime SLA is ___ %)
Fallback model if primary is down:     [ ]  (e.g., Switch from Claude to GPT-4o automatically)
```

### 13.4 AI Agent Governance (if using agents)

```
Agent action scope defined:            [ ]  (e.g., Agent can only read and write within user's data)
Dangerous actions require confirmation:[ ]  (e.g., Agent cannot delete data without human approval)
Agent execution time limit:            [ ]  (e.g., Max 60 seconds per agent run)
Agent memory / context window managed: [ ]  (e.g., Max 32k tokens per session)
Agent step limit:                      [ ]  (e.g., Max 10 tool calls per workflow)
Agent actions fully logged:            [ ]  (Yes — every tool call logged with input/output)
Rollback / undo for agent actions:     [ ]  (Yes / No — which actions are reversible?)
```

---

## 🚀 Section 15 — Deployment & Release Requirements

> **Plain English:** How do we ship new features safely — without breaking what's already working?

```
Deployment strategy:                   [ ]  (e.g., Blue/Green / Canary / Rolling update)
Feature rollout approach:              [ ]  (e.g., Feature flags — 5% → 20% → 100% rollout)
Smoke tests on deployment:             [ ]  (Yes — automated smoke tests run after every deploy)
Rollback time if deploy fails:         [ ]  (e.g., < 5 minutes — automated rollback)
Deployment approval required:          [ ]  (e.g., 1 senior engineer must approve production deploy)
Production deploy freeze:              [ ]  (e.g., No deploys Friday 5pm → Monday 9am)
Environment parity (staging = prod):   [ ]  (Yes — staging mirrors production data and config)
Secrets and config managed by:         [ ]  (e.g., AWS Secrets Manager / HashiCorp Vault)
Infrastructure as Code (IaC):         [ ]  (Yes — Terraform / Pulumi / CloudFormation)
```

---

## 📱 Section 16 — Mobile-Specific Requirements

> Only fill if your product includes a mobile app (iOS / Android).

```
App store submission target:           [ ]  (e.g., Apple App Store + Google Play Store)
App review timeline buffer:            [ ]  (e.g., 1–2 weeks for App Store review)
Push notification support:             [ ]  (Yes / No — what for? e.g., Appointment reminders)
Offline functionality:                 [ ]  (e.g., View last-synced data offline; sync on reconnect)
Deep linking supported:                [ ]  (Yes / No — e.g., Notification → specific screen)
App size limit:                        [ ]  (e.g., < 50 MB initial download)
Battery usage:                         [ ]  (e.g., App does not drain > 5% battery per hour of use)
Mobile data usage:                     [ ]  (e.g., < 1 MB per typical user session)
App update strategy:                   [ ]  (e.g., Force update for security releases, optional for features)
Crash-free session rate target:        [ ]  (e.g., > 99.5% crash-free sessions)
```

---

## 💸 Section 17 — Cost & Resource Constraints

> **Plain English:** What is the budget for running this product? Cost surprises kill startups.

```
Monthly infrastructure budget:         [ ]  (e.g., < $1,000/month at launch)
Infrastructure budget at 500 customers:[ ]  (e.g., < $5,000/month)
AI/LLM monthly budget:                 [ ]  (e.g., < $500/month)
Cost monitoring tool:                  [ ]  (e.g., AWS Cost Explorer / Infracost)
Budget alert threshold:                [ ]  (e.g., Alert when monthly spend > 80% of budget)
Cost per customer target:              [ ]  (e.g., < $2/customer/month infrastructure cost)
Reserved capacity (cost savings):      [ ]  (e.g., Reserve 1-year EC2 instances after 3 months stable)
```

---

## 🧪 Section 18 — Testing & Quality Assurance Requirements

> **Plain English:** How do we make sure the product actually works — before real users find out it doesn't?

### 17.1 Test Types Required

| Test Type | Required? | Tool | Coverage Target | When Run |
|-----------|---------|------|----------------|---------|
| Unit Tests | `[ ]` | `[ ]` *(e.g., Jest, pytest)* | `[ ]` *(e.g., 80%)* | Every commit |
| Integration Tests | `[ ]` | `[ ]` | `[ ]` *(e.g., Critical paths)* | Every PR |
| End-to-End (E2E) Tests | `[ ]` | `[ ]` *(e.g., Playwright, Cypress)* | `[ ]` *(e.g., All user journeys)* | Pre-deploy |
| Performance / Load Tests | `[ ]` | `[ ]` *(e.g., k6, Locust)* | `[ ]` *(e.g., 500 concurrent users)* | Monthly + pre-launch |
| Security Tests | `[ ]` | `[ ]` *(e.g., OWASP ZAP, Burp Suite)* | — | Quarterly + before launch |
| Accessibility Tests | `[ ]` | `[ ]` *(e.g., axe DevTools)* | — | Pre-release |
| AI / LLM Quality Tests | `[ ]` | `[ ]` *(e.g., Eval framework, human review)* | `[ ]` *(e.g., 100-case golden dataset)* | Before model update |
| Mobile App Tests | `[ ]` | `[ ]` *(e.g., Detox, Appium)* | `[ ]` | Pre-release |

### 17.2 Defect Management

```
Bug tracking tool:                     [ ]  (e.g., Jira / Linear / GitHub Issues)
Bug severity definitions:              [ ]  (Link to severity guide)
P1 bug fix SLA:                        [ ]  (e.g., Fixed and deployed within 4 hours)
P2 bug fix SLA:                        [ ]  (e.g., Fixed within 24 hours)
P3 bug fix SLA:                        [ ]  (e.g., Fixed within the current sprint)
Regression test on every fix:          [ ]  (Yes — automated where possible)
```

---

## 📋 Section 19 — Documentation Requirements

> **Plain English:** What documentation must exist for this product to be considered "done"?

```
API documentation:                     [ ]  (e.g., OpenAPI/Swagger — auto-generated and published)
User documentation / help center:      [ ]  (Yes — link: ___)
Admin / operator runbook:              [ ]  (Yes — link: ___)
Architecture decision records (ADRs):  [ ]  (Yes — stored in /docs/adr in the repo)
Onboarding guide for new developers:   [ ]  (Yes — README + Getting Started guide in repo)
Incident runbook:                      [ ]  (Yes — in Notion / Confluence)
Data flow diagrams:                    [ ]  (Yes — for compliance and architecture reviews)
AI model cards:                        [ ]  (Yes — documents model purpose, limitations, and risks)
Changelog maintained:                  [ ]  (Yes — CHANGELOG.md updated on every release)
```

---

## 🎯 Section 20 — NFR Sign-Off & Acceptance Criteria

> **Plain English:** How do we know all these requirements are actually met? Who signs off?

### 19.1 Acceptance Criteria Summary

> For each section, summarize the "done" bar.

| Section | Acceptance Condition | Owner | Status |
|---------|---------------------|-------|--------|
| Performance | All API p95 < defined target under load test | `[ ]` | `[ ]` |
| Scalability | Load test passes with `[ ]` concurrent users | `[ ]` | `[ ]` |
| Availability | Uptime monitoring shows ≥ `[ ]`% over 30 days | `[ ]` | `[ ]` |
| Security | Pentest complete, no Critical/High open findings | `[ ]` | `[ ]` |
| GDPR | DPA signed, all user rights testable | `[ ]` | `[ ]` |
| HIPAA | BAAs signed, PHI audit logging verified | `[ ]` | `[ ]` |
| SOC 2 | Evidence collection complete for audit scope | `[ ]` | `[ ]` |
| Accessibility | axe DevTools: zero critical violations | `[ ]` | `[ ]` |
| AI Quality | Eval dataset: accuracy ≥ threshold | `[ ]` | `[ ]` |
| Backup | Restore drill completed successfully | `[ ]` | `[ ]` |
| Disaster Recovery | All DR runbooks written; DR drill completed; RTO/RPO verified | `[ ]` | `[ ]` |

### 19.2 Sign-Off

| Role | Name | Signature / Approval | Date |
|------|------|---------------------|------|
| Product Manager | `[ ]` | `[ ]` | `[ ]` |
| Tech Lead / Architect | `[ ]` | `[ ]` | `[ ]` |
| QA Lead | `[ ]` | `[ ]` | `[ ]` |
| Security Lead | `[ ]` | `[ ]` | `[ ]` |
| Legal / Compliance | `[ ]` | `[ ]` | `[ ]` |
| Executive Sponsor | `[ ]` | `[ ]` | `[ ]` |

---

## 📌 Section 21 — Open Items & Decisions Pending

> Track everything that isn't decided yet. Don't leave it floating in your head.

| # | Open Question / Risk | Owner | Due Date | Status |
|---|---------------------|-------|---------|--------|
| 1 | `[ ]` | `[ ]` | `[ ]` | 🔴 Open |
| 2 | `[ ]` | `[ ]` | `[ ]` | 🔴 Open |
| 3 | `[ ]` | `[ ]` | `[ ]` | 🔴 Open |

---

## 📚 Appendix A — Glossary

> Plain-English definitions of technical terms used in this document.

| Term | What It Means (in simple words) |
|------|---------------------------------|
| **NFR** | Non-Functional Requirement — describes *how well* the product works, not *what* it does |
| **SLA** | Service Level Agreement — a promise about how good the service will be (e.g., 99.9% uptime) |
| **RTO** | Recovery Time Objective — max time the system can be down after a failure |
| **RPO** | Recovery Point Objective — max amount of data we can afford to lose (measured in time) |
| **Concurrent users** | Users actively using the app at the same moment |
| **p95 / p99 latency** | The response time that 95% / 99% of requests are faster than |
| **RBAC** | Role-Based Access Control — users get permissions based on their role (e.g., Admin, Viewer) |
| **JWT** | JSON Web Token — a secure way to prove who you are to an API |
| **TLS** | Transport Layer Security — encryption for data traveling over the internet |
| **PII** | Personally Identifiable Information — any data that can identify a person (name, email, etc.) |
| **PHI** | Protected Health Information — medical/health data protected by HIPAA |
| **LLM** | Large Language Model — the AI brain behind features like chatbots (e.g., GPT, Claude) |
| **Token** | The unit LLMs use to process text (roughly 1 token ≈ ¾ of a word) |
| **Hallucination** | When an AI confidently states something false |
| **SAST** | Static Application Security Testing — scanning code for security issues before it runs |
| **WCAG** | Web Content Accessibility Guidelines — international standard for accessible websites |
| **CDN** | Content Delivery Network — serves website files from servers close to the user |
| **CI/CD** | Continuous Integration / Continuous Deployment — automatically testing and shipping code |
| **IaC** | Infrastructure as Code — managing servers and cloud resources with code (not clicking) |
| **MTTR** | Mean Time to Restore — average time to fix a production issue |
| **DPA** | Data Processing Agreement — legal contract with vendors who handle your users' data |
| **BAA** | Business Associate Agreement — HIPAA-specific contract for vendors handling health data |

---

## 📚 Appendix B — NFR Checklist (Use Before Launch)

> Print this or paste it into your ticket tracker. Every checkbox must be ✅ before going live.

### Pre-Launch NFR Checklist

**Performance**
- [ ] Load test run with target concurrent users
- [ ] API p95 latency verified under load
- [ ] Mobile app load time measured on real devices
- [ ] AI response latency tested at scale

**Security**
- [ ] Penetration test complete — no Critical/High findings open
- [ ] All API endpoints have authentication
- [ ] HTTPS enforced everywhere
- [ ] Secrets removed from codebase — stored in secrets manager
- [ ] Rate limiting enabled on all public APIs
- [ ] MFA enabled for admin accounts

**Compliance**
- [ ] Privacy Policy and Terms of Service published
- [ ] Cookie consent implemented (if GDPR applies)
- [ ] DPAs signed with all data processors
- [ ] BAAs signed with all PHI-handling vendors (if HIPAA applies)
- [ ] User data rights mechanisms tested (export, delete, access)

**Reliability**
- [ ] Uptime monitoring is live and alerting works
- [ ] On-call rotation documented and tested
- [ ] Disaster recovery plan tested (restore drill completed)
- [ ] Rollback procedure documented and tested

**AI / ML**
- [ ] AI output quality eval passed (golden dataset score ≥ target)
- [ ] AI fallback tested (what happens when LLM API is down)
- [ ] Prompt injection protection verified
- [ ] AI cost monitoring active with budget alerts

**Observability**
- [ ] Error tracking live (e.g., Sentry)
- [ ] Key dashboards built and visible to the team
- [ ] Alert thresholds set for all P1 metrics
- [ ] Log retention policy configured

**Data**
- [ ] Automated backups running and verified
- [ ] Data retention policies configured and automated
- [ ] PII/PHI data classified and documented

**Accessibility**
- [ ] WCAG 2.1 AA automated scan — zero critical violations
- [ ] Keyboard navigation tested on all critical flows
- [ ] Screen reader test completed

**Documentation**
- [ ] API documentation published
- [ ] Incident runbook written and accessible
- [ ] Architecture diagram up to date

---

*Template Version: 1.1 | Last Updated: 2026-10-14 | Maintained by: [Your Team Name]*
*This template is designed for AI-Driven Development Life Cycle from development to first 500 customers.*
*Sections: 21 core sections + 2 appendices | Covers: Performance, Scalability, Security, GDPR, HIPAA, SOC 2, Accessibility, Usability, Maintainability, Compatibility, Observability, Data Management, Disaster Recovery, AI/ML, Deployment, Mobile, Cost, Testing, Documentation, Sign-Off, Open Items.*
