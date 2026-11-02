# Requirements Traceability Matrix (RTM)
### AI-Driven Development Life Cycle · Discovery → First 500 Customers
### Domain: FinTech / AI Banking · Credit Scoring · Loan Origination · Fraud Detection
> **Template Version:** 1.2 · **Standard:** Full Audit-Grade (16+ columns) · **Compliance:** EU AI Act · NIST AI RMF · GDPR · SOC 2 · PCI DSS · FCRA · ECOA

---

<!--
╔══════════════════════════════════════════════════════════════════════╗
║                  ⬇  HOW TO FILL THIS DOCUMENT  ⬇                   ║
╚══════════════════════════════════════════════════════════════════════╝

👋 Hello! If you are reading this for the first time — welcome.
This document tracks EVERY requirement your product must meet,
from the first idea all the way to your first 500 real users.
Think of it as your product's "report card" that proves nothing was missed.

You do NOT need to be a developer to fill this in.
Follow the numbered steps below, one section at a time.
-->

---

# 📖 How to Fill This Document
*(Read this first. Yes, really — it will save you hours.)*

## Step 1 — Fill in the Document Header
Go to **Section 1 (Document Information)** right below.
Replace every `[PLACEHOLDER]` with the real value for your project.
Example: Replace `[Project Name]` with `LoanPilot AI — Credit Scoring Platform`.

## Step 2 — Understand the Requirement ID System
Every row in the matrix gets a unique ID so nothing is ever confused with anything else.
Use this pattern:

| Prefix | Meaning | FinTech Example |
|--------|---------|----------------|
| `FUNC-` | Functional requirement (a feature the product must do) | `FUNC-001` — Online loan application flow |
| `NFR-` | Non-Functional requirement (how fast, safe, reliable it must be) | `NFR-001` — 99.99% uptime for payment APIs |
| `AI-` | AI-specific requirement (model accuracy, fairness, fraud detection) | `AI-001` — Credit scoring model AUC ≥ 0.85 |
| `COMP-` | Compliance requirement (GDPR, FCRA, ECOA, EU AI Act) | `COMP-001` — Adverse action notice for denied loans |

> 🧒 **Kid-friendly tip:** Think of IDs like names in a class register.
> Every requirement needs its own unique name so teachers can find it instantly.

## Step 3 — Fill the Requirements Phases in Order
This document is split into **6 SDLC phases**. Fill them in order:
1. **Phase 1 — Discovery & Ideation** (define what the product must do — before any code)
2. **Phase 2 — Design & Architecture** (wireframes, system design, AI pipeline architecture)
3. **Phase 3 — Development & AI Training** (engineers build; data scientists train models)
4. **Phase 4 — Testing, QA & AI Validation** (does it actually work, safely and fairly?)
5. **Phase 5 — Launch & Go-to-Market** (first 500 real customers — the critical window)
6. **Phase 6 — Post-Launch Iteration** (fix, improve, retrain models on real data)

## Step 4 — Write Good Requirement Statements
Every requirement must follow this sentence structure:

> **"The [system / AI model / app] SHALL [do something specific] SO THAT [the user / business / regulator gets a benefit]."**

✅ Good: `The AI credit scoring model SHALL generate a human-readable explanation of the top 5 factors influencing the loan decision SO THAT applicants understand why they were approved or declined.`
❌ Bad: `The AI should explain its decisions.`

> 🧒 **Kid-friendly tip:** Imagine explaining this to a robot. The robot is very literal.
> If you're not specific enough, the robot will do something unexpected — like a vending machine that gives you crisps when you wanted chocolate because you just said "snack".

## Step 5 — Set Priority for Every Requirement
Use these four levels:

| Priority | What It Means | FinTech Example |
|----------|--------------|----------------|
| 🔴 **Critical** | Without this, the product cannot launch. | Fraud detection, regulatory compliance, data encryption |
| 🟠 **High** | Very important, but a workaround exists temporarily. | Multi-currency support |
| 🟡 **Medium** | Valuable, but not blocking launch. | Dashboard analytics |
| 🟢 **Low / Nice-to-Have** | Good to have someday. | Dark mode |

## Step 6 — Assign an AI Risk Level
For each requirement, ask: *"What is the worst thing that could happen if this requirement is NOT met?"*

In FinTech and AI banking, the EU AI Act classifies credit scoring, fraud detection, and loan origination AI as **HIGH RISK** under Annex III. Most AI requirements in this domain will be 🔴 High.

| Risk | Traffic Light | FinTech Example |
|------|:------------:|----------------|
| High Risk | 🔴 | AI credit model denies a loan unfairly due to racial bias — regulatory fine + reputational damage |
| Medium Risk | 🟡 | AI chatbot gives slightly wrong interest rate information — correctable by human |
| Low Risk | 🟢 | AI suggests an account nickname — no financial or legal consequence if wrong |

## Step 7 — Link Every Requirement to a Test Case
Every requirement MUST have at least one test case that proves it was met.
Write the Test Case ID in the `Linked Test Case ID` column using the format `TCS-001`.

In FinTech, test cases for AI requirements must include:
- **Fairness tests** across protected demographic groups (ECOA, EU AI Act Art. 10)
- **Adversarial tests** (e.g., fraudulent inputs designed to fool the model)
- **Regression tests** (ensuring new model versions do not perform worse than the previous one)

## Step 8 — Update Status as Work Progresses

| Status | Meaning |
|--------|---------|
| 📝 Draft | Requirement written, not yet reviewed |
| 🔍 In Review | Being reviewed by the team |
| ✅ Approved | Stakeholders agreed this is correct |
| 🏗️ In Progress | Developers / data scientists are building this |
| 🧪 Testing | In QA / model validation phase |
| ✔️ Done | Tested, passed, signed off — this is verified |
| ❌ Deprecated | No longer needed (reason recorded in Notes) |

## Step 9 — Get Sign-Offs
At the end of each phase, fill in **Section 8 (Sign-Off & Approvals)**.
In FinTech, the **AI system launch approval** panel is especially important — regulators (FCA, EBA, CFPB) may request evidence of this sign-off.

## Step 10 — Log Every Change
Any time a requirement changes AFTER it has been approved, log it in **Section 9 (Change Log)**.
Under the EU AI Act and FCRA, you must be able to prove that AI decisions were made using the version of the model in force at the time. Never delete old requirements — mark them Deprecated.

---

---

# SECTION 1 — Document Information

| Field | Value |
|-------|-------|
| **Project / Product Name** | `[e.g., LoanPilot AI — Intelligent Credit Scoring & Loan Origination Platform]` |
| **Document Title** | Requirements Traceability Matrix |
| **Document ID** | `[e.g., DOC-RTM-001]` |
| **Product Type** | ☐ SaaS / Web App   ☐ Mobile App (iOS)   ☐ Mobile App (Android)   ☐ AI Agent / API |
| **Version** | `[e.g., v1.0]` |
| **Status** | ☐ Draft   ☐ In Review   ☐ Approved   ☐ Active   ☐ Archived |
| **Date Created** | `[YYYY-MM-DD]` |
| **Last Updated** | `[YYYY-MM-DD]` |
| **Project Manager** | `[Full Name]` |
| **Product Owner** | `[Full Name]` |
| **Tech Lead / Architect** | `[Full Name]` |
| **AI / ML Lead** | `[Full Name]` |
| **QA Lead** | `[Full Name]` |
| **Compliance / Legal Officer** | `[Full Name]` |
| **Chief Risk Officer (CRO)** | `[Full Name or N/A]` |
| **Data Protection Officer (DPO)** | `[Full Name — required under GDPR if processing at scale]` |
| **Target Launch Date** | `[YYYY-MM-DD]` |
| **First 500 Customers Goal Date** | `[YYYY-MM-DD]` |
| **AI Governance Framework** | ☑ EU AI Act (Annex III — High Risk: Credit Scoring)   ☑ NIST AI RMF   ☐ ISO 42001 |
| **Data Privacy Regulations** | ☑ GDPR   ☑ SOC 2   ☐ CCPA   ☐ Other: `[specify]` |
| **Financial Regulations** | ☑ FCRA (Fair Credit Reporting Act)   ☑ ECOA (Equal Credit Opportunity Act)   ☐ PCI DSS   ☐ FCA (UK)   ☐ Other |
| **AI Risk Category (EU AI Act)** | ☑ High Risk — Annex III Point 5(b): AI used for creditworthiness assessment |

---

# SECTION 2 — Glossary
*(Reference only — skip when filling in the RTM.)*

| Term | Plain-English Definition |
|------|--------------------------|
| **Requirement** | A thing the product MUST do, or a quality it MUST have. |
| **Traceability** | Being able to prove that every requirement was designed, built, and tested. |
| **Acceptance Criteria** | The exact conditions that prove a requirement is truly finished. |
| **AI Credit Scoring** | An AI model that analyses applicant data and gives a score predicting their likelihood of repaying a loan. |
| **AUC-ROC** | Area Under the Curve — a performance metric for classification models. Higher is better. 0.85+ is generally good for credit scoring. |
| **Adverse Action Notice** | A legal letter sent to loan applicants who are denied, explaining why. Required by FCRA. |
| **Bias (AI)** | When an AI model unfairly favours or harms certain groups — e.g., denying more loans to women than men with identical credit profiles. |
| **ECOA** | Equal Credit Opportunity Act — US law that prohibits discrimination in credit decisions. |
| **FCRA** | Fair Credit Reporting Act — US law governing how credit information is used and shared. |
| **EU AI Act** | European Union law that classifies credit-scoring AI as HIGH RISK and requires strict governance, auditability, and human oversight. |
| **NIST AI RMF** | A US framework that helps organisations manage AI risks responsibly. |
| **GDPR** | A European law protecting people's personal data and privacy. |
| **SOC 2** | A security certification proving a company handles customer data responsibly. |
| **PCI DSS** | Payment Card Industry Data Security Standard — required if storing or processing card data. |
| **Thin-File Applicant** | Someone with little or no traditional credit history — e.g., a recent graduate or immigrant. |
| **Hallucination (AI)** | When an AI confidently states something false — dangerous in financial advice contexts. |
| **Guardrail** | A rule or filter that prevents an AI from producing harmful or incorrect outputs. |
| **Model Drift** | When a deployed AI model's accuracy degrades over time as real-world data patterns change. |
| **Explainability (XAI)** | The ability to explain, in plain language, why an AI model made a specific decision. Required under EU AI Act Art. 13. |
| **Red-Teaming** | Deliberately trying to break or fool an AI model to expose weaknesses before launch. |
| **NFR** | Non-Functional Requirement — how the system BEHAVES (speed, security, uptime, scalability). |
| **Sign-Off** | Formal approval by a named person that something is done and correct. |

---

# SECTION 3 — Requirements Summary Dashboard
*(Update at the end of each phase. Gives leadership an instant health check.)*

## 3.1 · Requirement Count by Type

| Requirement Type | Total Defined | Approved | In Progress | Testing | Done | Deprecated |
|-----------------|:---:|:---:|:---:|:---:|:---:|:---:|
| Functional (FUNC) | `0` | `0` | `0` | `0` | `0` | `0` |
| Non-Functional (NFR) | `0` | `0` | `0` | `0` | `0` | `0` |
| AI-Specific (AI) | `0` | `0` | `0` | `0` | `0` | `0` |
| Compliance (COMP) | `0` | `0` | `0` | `0` | `0` | `0` |
| **TOTAL** | **`0`** | **`0`** | **`0`** | **`0`** | **`0`** | **`0`** |

## 3.2 · Phase Completion Status

| Phase | Phase Name | Requirements Defined | Requirements Done | % Complete | Phase Sign-Off |
|:-----:|-----------|:---:|:---:|:---:|:---:|
| 1 | Discovery & Ideation | `0` | `0` | `0%` | ☐ Pending |
| 2 | Design & Architecture | `0` | `0` | `0%` | ☐ Pending |
| 3 | Development & AI Training | `0` | `0` | `0%` | ☐ Pending |
| 4 | Testing, QA & AI Validation | `0` | `0` | `0%` | ☐ Pending |
| 5 | Launch & Go-to-Market | `0` | `0` | `0%` | ☐ Pending |
| 6 | Post-Launch Iteration | `0` | `0` | `0%` | ☐ Pending |

## 3.3 · AI Risk Summary

| Risk Level | Count | % of Total |
|:----------:|:-----:|:----------:|
| 🔴 High | `0` | `0%` |
| 🟡 Medium | `0` | `0%` |
| 🟢 Low | `0` | `0%` |

> ⚠️ **FinTech note:** Expect most AI requirements to be 🔴 High under EU AI Act Annex III (credit scoring = High-Risk AI).

## 3.4 · Compliance Coverage

| Regulation | Requirements Mapped | Requirements Verified | Gap Count |
|------------|:---:|:---:|:---:|
| GDPR | `0` | `0` | `0` |
| SOC 2 | `0` | `0` | `0` |
| EU AI Act (High Risk) | `0` | `0` | `0` |
| NIST AI RMF | `0` | `0` | `0` |
| FCRA | `0` | `0` | `0` |
| ECOA | `0` | `0` | `0` |
| PCI DSS | `0` | `0` | `0` |

---

---

# SECTION 4.0 — User Story → Requirement Mapping
*(Bridge table: maps product user stories to RTM requirement IDs. Fill this as you write user stories.)*

> 💡 **What is this section for?** In product management, we often write "user stories" to describe
> features from a customer's point of view. This table connects each user story to the formal
> requirements it generates — so nothing falls through the cracks.
>
> **Format:** User Story → one or more REQ IDs → Phase where those requirements are delivered.

> 📝 **How to write a User Story:**
> `"As a [type of user], I want to [do something] so that [I get a benefit]."`

| US ID | User Story | User Type | Mapped REQ IDs | Primary Phase | Priority | Status |
|-------|-----------|-----------|---------------|:-------------:|:--------:|:------:|
| US-001 | *As a first-time loan applicant, I want to apply for a personal loan online so that I can get a credit decision without visiting a bank branch.* | Customer | `FUNC-001, NFR-001, FUNC-040` | Phase 1, 5 | 🔴 Critical | 📝 Draft |
| US-002 | *As a denied loan applicant, I want to receive a clear explanation of why my application was rejected so that I understand what I need to improve.* | Customer | `AI-023, COMP-001, AI-030` | Phase 1, 3, 4 | 🔴 Critical | 📝 Draft |
| US-003 | *As a thin-file applicant with no traditional credit history, I want my alternative financial data (rent, utilities) to be considered so that I am not automatically excluded from credit.* | Underserved Customer | `AI-001, AI-020` | Phase 1, 3 | 🔴 Critical | 📝 Draft |
| US-004 | *As a bank compliance officer, I want a full audit trail of every AI credit decision so that I can respond to regulatory examinations.* | Internal — Compliance | `AI-040, AI-023` | Phase 5 | 🔴 Critical | 📝 Draft |
| US-005 | *As a fraud analyst, I want to be alerted in real time when the AI flags suspicious account activity so that I can investigate before money is moved.* | Internal — Fraud Team | `AI-041, NFR-020` | Phase 5 | 🔴 Critical | 📝 Draft |
| US-006 | *As an EU customer, I want to be able to request deletion of all my personal data so that my GDPR rights are respected.* | EU Customer | `COMP-030, COMP-010` | Phase 2, 4 | 🔴 Critical | 📝 Draft |
| US-007 | *As a mobile banking customer, I want to check my loan application status from my phone so that I can stay informed without logging into a desktop browser.* | Mobile Customer | `FUNC-010, NFR-040` | Phase 2, 5 | 🟠 High | 📝 Draft |
| US-008 | *As an underwriter, I want the AI to flag applications for human review when its confidence is low so that I can apply my judgement to borderline cases.* | Internal — Underwriter | `AI-010, AI-021` | Phase 2, 3 | 🔴 Critical | 📝 Draft |
| US-009 | *As a product manager, I want to see live AI model performance metrics on a dashboard so that I can detect model drift before it affects customers.* | Internal — PM | `AI-041, NFR-040` | Phase 5, 6 | 🟠 High | 📝 Draft |
| US-010 | *As a returning customer with 12 months of good repayment history, I want a faster repeat-loan application so that loyal customers are rewarded with a smoother experience.* | Returning Customer | `FUNC-050` | Phase 6 | 🟡 Medium | 📝 Draft |
| `US-NNN` | *[Add your own user story here]* | | | | | 📝 Draft |

---

---

# SECTION 4 — Requirements Matrix (All Phases)

> **📌 Column Guide**
>
> | Column | What to write |
> |--------|--------------|
> | **REQ ID** | Unique ID (e.g. `FUNC-001`). Never reuse or delete IDs. |
> | **Type** | `Functional` / `Non-Functional` / `AI-Specific` / `Compliance` |
> | **Requirement Statement** | Full "SHALL" sentence. Be specific. No vague words like "fast" or "good". |
> | **Source** | Who asked for this? (e.g., `US-001`, `FCRA §611`, `User Research Round 2`) |
> | **Priority** | `🔴 Critical` / `🟠 High` / `🟡 Medium` / `🟢 Low` |
> | **Phase** | Which SDLC phase this requirement belongs to |
> | **Owner** | Name or role responsible for delivering this |
> | **Acceptance Criteria** | Exact conditions for "done". Write them as bullet points. |
> | **AI Success Metric** | Only for AI-type reqs. Define your measurable threshold. Write `N/A` for others. |
> | **AI Risk** | `🔴 High` / `🟡 Medium` / `🟢 Low` — risk if this req is NOT met |
> | **Compliance Tag** | `GDPR` / `SOC2` / `EU-AI-Act` / `NIST-AI-RMF` / `FCRA` / `ECOA` / `None` |
> | **Linked Test Case ID** | e.g. `TCS-007`. Write `TBD` if test case not yet written. |
> | **Test Result** | `Pass` / `Fail` / `Blocked` / `Not Tested` |
> | **Defect ID** | Bug ID if test failed (e.g. `BUG-042`). Write `None` if passed. |
> | **Retest Status** | `Pass` / `Fail` / `Pending` / `N/A` |
> | **Req Version** | Start at `v1.0`. Bump to `v1.1` each time the requirement changes. |
> | **Change Reason** | Why did this requirement change? Write `Initial` for the first version. |
> | **Approved By** | Full name of the person who approved this requirement as complete. |
> | **Approval Date** | Date the approver signed off (`YYYY-MM-DD`). |
> | **Status** | `📝 Draft` / `🔍 In Review` / `✅ Approved` / `🏗️ In Progress` / `🧪 Testing` / `✔️ Done` / `❌ Deprecated` |

---

## Phase 1 — Discovery & Ideation
*Goal: Define what the banking/fintech product must do and why, before any code is written.*
*Typical owners: Product Manager, Chief Risk Officer, Legal/Compliance, AI Lead.*

> 💡 **When to add rows here:** At the very start of the project.
> FinTech tip: start with regulatory requirements (FCRA, ECOA, GDPR, EU AI Act) and work backward to product features.

### 1A · Functional Requirements — Discovery

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-001 | Functional | *[e.g., The system SHALL allow any individual aged 18+ to complete a digital loan application from a web browser or mobile app in ≤15 minutes SO THAT customers can apply for credit without visiting a branch.]* | *[US-001; Business Case v1.0]* | 🔴 Critical | Phase 1 | Product Manager | *[Application form captures all required fields; end-to-end journey tested on 5 devices; average completion time ≤15 min in user testing]* | N/A | 🟡 Medium | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| FUNC-002 | Functional | *[e.g., The system SHALL send every denied loan applicant an automated Adverse Action Notice via email within 3 business days of the decision SO THAT the bank complies with FCRA §615(a).]* | *[US-002; FCRA §615(a)]* | 🔴 Critical | Phase 1 | Product Manager | *[Adverse action email triggered automatically on every denial; email contains all FCRA-required elements; delivered within 3 business days in QA simulation]* | N/A | 🔴 High | FCRA | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| FUNC-003 | Functional | *[e.g., The loan application form SHALL allow applicants to upload supporting documents (pay slips, bank statements, utility bills) directly in the app SO THAT underwriters have all required evidence without requesting documents by post.]* | *[US-001; Underwriter Interviews]* | 🟠 High | Phase 1 | Product Manager | *[Upload accepts PDF, JPG, PNG up to 10MB; virus scan runs on every file; upload confirmation shown to user; file accessible to underwriter within 60 seconds]* | N/A | 🟢 Low | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 1B · Non-Functional Requirements — Discovery

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| NFR-001 | Non-Functional | *[e.g., The loan origination system SHALL maintain ≥ 99.95% uptime measured monthly SO THAT applicants can submit applications at any time, including peak periods such as financial year-end.]* | *[SLA Policy; CRO Mandate]* | 🔴 Critical | Phase 1 | Tech Lead / DevOps | *[Uptime monitoring in place from Day 1; monthly SLA report reviewed by CTO; 99.95% met for 3 consecutive months]* | N/A | 🟡 Medium | SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| NFR-002 | Non-Functional | *[e.g., All personal and financial data SHALL be encrypted at rest using AES-256 and in transit using TLS 1.3 SO THAT customer data is protected against interception and breach.]* | *[GDPR Art. 32; SOC 2 CC6.7; PCI DSS Req. 4]* | 🔴 Critical | Phase 1 | Security Lead | *[Encryption verified by security audit; penetration test confirms no plaintext data exposure; TLS version confirmed in network inspection]* | N/A | 🔴 High | GDPR, SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 1C · AI-Specific Requirements — Discovery

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-001 | AI-Specific | *[e.g., The AI credit scoring model SHALL incorporate alternative data sources (12 months of bank transaction history, utility bill payment history, rent payment history) in addition to bureau data SO THAT thin-file applicants with no traditional credit history are assessed fairly.]* | *[US-003; Financial Inclusion Strategy; ECOA]* | 🔴 Critical | Phase 1 | AI/ML Lead | *[Model uses alternative data in ≥70% of scored applications; thin-file applicant approval rate comparable to bureau-scored applicants at equivalent risk levels; confirmed in fairness audit]* | *[Thin-file applicant approval rate within 5% of bureau-scored applicants at equivalent predicted default rate]* | 🔴 High | ECOA, EU-AI-Act | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| AI-002 | AI-Specific | *[e.g., The AI fraud detection model SHALL flag potentially fraudulent loan applications in real time, generating a risk score and alert to the fraud team within 30 seconds of submission SO THAT fraudulent applications are intercepted before funds are disbursed.]* | *[US-005; Fraud Risk Policy v2.1]* | 🔴 Critical | Phase 1 | AI/ML Lead + Fraud Team | *[Fraud alerts generated within 30 seconds in all test scenarios; fraud team receives alert via dashboard and email; confirmed in simulated fraud test suite of 200 cases]* | *[Alert latency ≤ 30 seconds for 99% of flagged applications; fraud recall ≥ 85% on historical fraud test set]* | 🔴 High | EU-AI-Act, NIST-AI-RMF | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 1D · Compliance Requirements — Discovery

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| COMP-001 | Compliance | *[e.g., The system SHALL provide every declined applicant with an FCRA-compliant Adverse Action Notice that includes: (a) the specific reasons for denial, (b) name and contact of the credit reporting agency used, and (c) the applicant's right to obtain a free credit report within 60 days SO THAT the bank meets FCRA §615(a) requirements.]* | *[FCRA §615(a); Legal Review 2026-Q1]* | 🔴 Critical | Phase 1 | Legal + PM | *[Adverse action notice template approved by Legal; all 3 required elements present; automated delivery within 3 business days confirmed in QA]* | N/A | 🔴 High | FCRA | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| COMP-002 | Compliance | *[e.g., The AI credit scoring system SHALL be classified as a High-Risk AI System under EU AI Act Annex III Point 5(b) and SHALL meet all associated requirements (risk management, data governance, transparency, human oversight, accuracy) before processing any EU applicant SO THAT the bank is compliant with EU AI Act obligations before launch in EU markets.]* | *[EU AI Act Annex III; Legal Counsel Opinion 2026-03-15]* | 🔴 Critical | Phase 1 | Compliance Officer + AI Lead | *[EU AI Act compliance checklist completed and signed off by DPO and Legal; technical documentation conforming to Art. 11 in place; CE marking process initiated if applicable]* | N/A | 🔴 High | EU-AI-Act | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

---

## Phase 2 — Design & Architecture
*Goal: Translate requirements into system design, UX wireframes, AI pipeline architecture, and data models.*
*Typical owners: Tech Lead, UX Designer, AI/ML Architect, DPO.*

> 💡 **When to add rows here:** After Phase 1 sign-off. In FinTech, key design decisions include:
> model architecture (black-box vs. explainable), data segregation (EU vs. non-EU), human-in-the-loop placement.

### 2A · Functional Requirements — Design

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-010 | Functional | *[e.g., The mobile loan application UI SHALL display the applicant's real-time application progress (step 1 of 5, step 2 of 5, etc.) and an estimated decision time SO THAT customers know exactly where they are in the process and do not abandon the application out of uncertainty.]* | *[US-007; UX Research Round 1]* | 🟠 High | Phase 2 | UX Lead | *[Progress indicator visible at every step; estimated time displayed; tested on iOS 17 and Android 14; drop-off rate in prototype testing < 15%]* | N/A | 🟢 Low | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| FUNC-011 | Functional | *[e.g., The system SHALL include a human underwriter review queue where applications flagged by the AI (confidence score < 70% OR fraud risk score > 60) are routed for manual review SO THAT the bank maintains meaningful human oversight over borderline credit decisions as required by EU AI Act Art. 14.]* | *[US-008; EU AI Act Art. 14; ECOA]* | 🔴 Critical | Phase 2 | PM + Tech Lead | *[All AI-flagged applications appear in underwriter queue within 5 minutes; underwriter can approve, deny, or request more information; decision logged with underwriter name and timestamp]* | N/A | 🔴 High | EU-AI-Act, ECOA | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 2B · Non-Functional Requirements — Design

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| NFR-010 | Non-Functional | *[e.g., The system architecture SHALL be designed to separate EU customer data into an EU-hosted data region (AWS eu-west-1 or equivalent) SO THAT GDPR cross-border transfer restrictions (Chapter V) are respected from the first EU customer.]* | *[GDPR Chapter V; DPO Mandate]* | 🔴 Critical | Phase 2 | Tech Lead + DPO | *[Architecture diagram reviewed by DPO; EU data confirmed to reside in EU-hosted infrastructure; data flow diagram shows no EU PII leaving EU region without SCCs]* | N/A | 🔴 High | GDPR | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 2C · AI-Specific Requirements — Design

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-010 | AI-Specific | *[e.g., The AI credit scoring pipeline architecture SHALL use an inherently interpretable model class (e.g., Gradient Boosted Trees with SHAP explanations, Logistic Regression with feature coefficients) rather than a black-box model SO THAT individual credit decisions can be explained to applicants and regulators as required by EU AI Act Art. 13 and ECOA.]* | *[US-002; EU AI Act Art. 13; ECOA; CRO Mandate]* | 🔴 Critical | Phase 2 | AI Architect | *[Model architecture decision document reviewed and approved by CRO, Legal, and AI Lead; selected model class produces per-decision feature importance scores; approved architecture documented]* | *[SHAP / equivalent feature importance available for 100% of scored applications]* | 🔴 High | EU-AI-Act, ECOA | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 2D · Compliance Requirements — Design

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| COMP-010 | Compliance | *[e.g., A Data Protection Impact Assessment (DPIA) SHALL be completed and approved by the DPO before development begins on any component that processes applicant PII SO THAT GDPR Art. 35 obligations are met, given the high-risk nature of AI-based credit scoring.]* | *[GDPR Art. 35; EU AI Act Art. 9]* | 🔴 Critical | Phase 2 | DPO + PM | *[DPIA document completed using ICO template; reviewed and signed off by DPO before Phase 3 begins; DPO sign-off date recorded in this RTM]* | N/A | 🔴 High | GDPR | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

---

## Phase 3 — Development & AI Training
*Goal: Build the product. Train, fine-tune, and validate AI models. Engineer prompts and credit scoring pipelines.*
*Typical owners: Software Engineers, AI/ML Engineers, Data Scientists, Fraud Analysts.*

> 💡 **FinTech tip for this phase:** AI model training in credit scoring has specific legal requirements.
> Under ECOA and EU AI Act Art. 10, training data must be audited for demographic bias.
> Retain full documentation of training data, model versions, and evaluation results — regulators can ask for these.

### 3A · Functional Requirements — Development

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-020 | Functional | *[e.g., The user authentication module SHALL implement Multi-Factor Authentication (MFA) using TOTP (Authenticator app) or SMS OTP for all customer accounts SO THAT unauthorised access to financial accounts is prevented even if passwords are compromised.]* | *[SOC 2 CC6.1; PCI DSS Req. 8.4; Security Policy]* | 🔴 Critical | Phase 3 | Backend Engineer | *[MFA required at every new device login; TOTP and SMS OTP both functional; tested on iOS, Android, Chrome, Safari; brute-force lockout after 5 failed attempts]* | N/A | 🔴 High | SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| FUNC-021 | Functional | *[e.g., The loan decision screen SHALL display the applicant's credit decision (Approved / Referred / Declined), the approved loan amount and interest rate if approved, and the top 3 reasons for the decision SO THAT applicants immediately understand their outcome and the primary factors that influenced it.]* | *[US-002; EU AI Act Art. 13; ECOA Reg. B]* | 🔴 Critical | Phase 3 | Frontend + AI Engineer | *[Decision screen renders within 2 seconds of AI decision; all 3 elements present in 100% of test scenarios; reasons are plain-language, not model jargon; verified in QA regression suite]* | N/A | 🔴 High | EU-AI-Act, ECOA, FCRA | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 3B · Non-Functional Requirements — Development

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| NFR-020 | Non-Functional | *[e.g., The AI credit scoring API SHALL return a credit decision and explanation within 3 seconds at the 99th percentile under a load of 500 concurrent scoring requests SO THAT applicants receive a real-time decision experience and underwriters are not blocked waiting for AI output.]* | *[NFR-001; UX Research: applicants abandon after 8 seconds]* | 🔴 Critical | Phase 3 | Backend / MLOps | *[Load test at 500 concurrent requests: p99 latency < 3 seconds; error rate < 0.01%; tested with k6 or equivalent load testing tool; results documented]* | N/A | 🟡 Medium | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 3C · AI-Specific Requirements — Development & AI Training

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-020 | AI-Specific | *[e.g., The AI credit scoring model training dataset SHALL undergo a formal demographic bias audit by a qualified third party before training begins, confirming that the dataset is representative of the applicant population by gender, age group, ethnicity, and geography SO THAT the trained model does not inherit historical discriminatory lending patterns.]* | *[US-003; EU AI Act Art. 10; ECOA; NIST AI RMF GOVERN 6.2]* | 🔴 Critical | Phase 3 | AI/ML Lead + Compliance | *[Third-party bias audit report completed; dataset representation confirmed for all 4 demographic dimensions; any identified bias corrected via resampling or re-labelling before training; audit report archived and signed off by DPO and CRO]* | *[Demographic representation within ±5% of applicant population distribution for all protected groups]* | 🔴 High | EU-AI-Act, ECOA, NIST-AI-RMF | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| AI-021 | AI-Specific | *[e.g., The AI credit scoring model SHALL achieve an AUC-ROC score of ≥ 0.85 and a Gini coefficient of ≥ 0.70 on the held-out test set before any model version is approved for production deployment SO THAT only models with proven discriminatory power are used in live credit decisions.]* | *[AI Model Performance Policy v1.0; CRO Mandate]* | 🔴 Critical | Phase 3 | AI/ML Lead | *[Model evaluation report shows AUC-ROC ≥ 0.85 and Gini ≥ 0.70; report reviewed and signed off by AI Lead and CRO; report archived with model version ID]* | *[AUC-ROC ≥ 0.85; Gini coefficient ≥ 0.70 on held-out test set (minimum 10,000 examples)]* | 🔴 High | EU-AI-Act | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| AI-022 | AI-Specific | *[e.g., The AI credit scoring model SHALL produce a SHAP (SHapley Additive exPlanations) feature importance breakdown for every individual credit decision SO THAT the system can generate plain-language explanations of the top 5 contributing factors for every applicant, supporting ECOA Adverse Action Notice requirements.]* | *[US-002; ECOA Reg. B; EU AI Act Art. 13; FUNC-021]* | 🔴 Critical | Phase 3 | AI/ML Engineer | *[SHAP values generated for 100% of scored applications in QA; top 5 features correctly mapped to plain-language explanations; underwriter confirmed explanations are accurate in review of 100 sample cases]* | *[SHAP explanation available for 100% of decisions; human underwriter accuracy check: ≥ 95% of explanations rated accurate]* | 🔴 High | EU-AI-Act, ECOA, FCRA | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| AI-023 | AI-Specific | *[e.g., The AI fraud detection model SHALL maintain a false positive rate (legitimate transactions incorrectly flagged as fraud) of ≤ 0.5% SO THAT genuine customers are not blocked from accessing credit, causing unnecessary inconvenience and potential fair-lending risk.]* | *[US-005; Fraud Policy; ECOA — disparate impact]* | 🔴 Critical | Phase 3 | AI/ML Lead + Fraud Team | *[Model evaluation on 50,000 historical transactions confirms FPR ≤ 0.5%; false positive rates reviewed separately by demographic group to confirm no disparate impact; report approved by CRO]* | *[Overall FPR ≤ 0.5%; FPR within ±0.1% across gender and ethnicity groups (no disparate impact)]* | 🔴 High | ECOA, EU-AI-Act | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 3D · Compliance Requirements — Development

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| COMP-020 | Compliance | *[e.g., The system SHALL implement Role-Based Access Control (RBAC) with least-privilege principles, ensuring that customer PII and credit data are only accessible to roles that have a documented business need SO THAT SOC 2 CC6.3 and GDPR Art. 32 access control requirements are met.]* | *[SOC 2 CC6.3; GDPR Art. 32]* | 🔴 Critical | Phase 3 | Security Engineer | *[RBAC matrix reviewed and approved by CISO; penetration test confirms no privilege escalation; SOC 2 auditor reviewed access control design; no finding]* | N/A | 🔴 High | SOC2, GDPR | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

---

## Phase 4 — Testing, QA & AI Validation
*Goal: Prove every requirement is met. Credit models, fraud models, features, security, fairness, and compliance — all validated.*
*Typical owners: QA Lead, AI Evaluation Team, CRO, Compliance Officer, External Pentest Firm.*

> ⚠️ **Critical FinTech note:** For EU AI Act High-Risk AI systems (credit scoring), this phase generates the
> technical documentation required by Art. 11. Keep all evaluation reports — regulators can request them.

### 4A · AI-Specific Requirements — AI Validation

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-030 | AI-Specific | *[e.g., The AI credit scoring model SHALL be evaluated on a fairness benchmark dataset of ≥ 5,000 applications with known demographic labels (gender, age band, ethnicity) by an independent third-party reviewer, confirming that demographic parity difference is < 5% across all protected groups SO THAT ECOA and EU AI Act Art. 10 obligations are demonstrably met before launch.]* | *[EU AI Act Art. 10; ECOA; NIST AI RMF MAP 5.1]* | 🔴 Critical | Phase 4 | AI Eval Team + Compliance | *[Third-party fairness evaluation report completed; demographic parity difference < 5% for gender, age, and ethnicity; report signed off by CRO, DPO, and AI Lead; archived as EU AI Act Art. 11 technical documentation]* | *[Demographic parity difference ≤ 5% across all protected groups in fairness benchmark]* | 🔴 High | EU-AI-Act, ECOA, NIST-AI-RMF | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| AI-031 | AI-Specific | *[e.g., The AI credit scoring model SHALL undergo structured adversarial testing with at least 500 crafted test cases designed to expose potential model gaming, bias amplification, or data leakage SO THAT attack vectors and failure modes are documented and remediated before any live applicant is scored.]* | *[EU AI Act Art. 9; NIST AI RMF MAP 5.1; CRO Mandate]* | 🔴 Critical | Phase 4 | AI Safety Lead + Red Team | *[Adversarial test report completed; all Critical and High findings remediated before launch; remaining Medium findings risk-accepted by CRO with documented rationale; report archived]* | *[0 critical model failures on adversarial test suite; model gaming attempt success rate = 0% on 500-case test]* | 🔴 High | EU-AI-Act, NIST-AI-RMF | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| AI-032 | AI-Specific | *[e.g., The plain-language explanation system SHALL be validated by 3 qualified underwriters who independently confirm that the AI-generated explanations for a sample of 200 credit decisions are accurate, actionable, and free from financial jargon SO THAT explanations provided to applicants and on adverse action notices are legally defensible.]* | *[US-002; ECOA Reg. B; EU AI Act Art. 13; FCRA §615]* | 🔴 Critical | Phase 4 | QA Lead + Underwriter Panel | *[3 underwriters each review 200 decisions independently; ≥ 95% of explanations rated accurate and actionable; any systematic inaccuracy fixed and re-reviewed; validation report signed off]* | *[Underwriter accuracy rating ≥ 95% on 200-case validation sample; inter-rater agreement ≥ 0.80 (Cohen's κ)]* | 🔴 High | EU-AI-Act, ECOA, FCRA | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 4B · Non-Functional Requirements — Security Testing

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| NFR-030 | Non-Functional | *[e.g., The system SHALL pass an external penetration test conducted by a CREST-accredited firm with no Critical or High severity findings remaining open before launch SO THAT the platform's security posture meets SOC 2, PCI DSS, and regulatory expectations.]* | *[SOC 2 CC7.1; PCI DSS Req. 11.3]* | 🔴 Critical | Phase 4 | CISO | *[Pentest report from CREST-accredited firm received; all Critical/High findings resolved and re-tested; report and resolution evidence archived; CISO sign-off obtained]* | N/A | 🔴 High | SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 4C · Compliance Requirements — QA Verification

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| COMP-030 | Compliance | *[e.g., The GDPR Right to Erasure workflow SHALL delete all PII associated with a customer — including from the AI model's training data pipeline and scoring logs — within 30 days of a verified deletion request SO THAT GDPR Art. 17 obligations are met and no PII leaks into future model training runs.]* | *[GDPR Art. 17; DPO Mandate]* | 🔴 Critical | Phase 4 | Engineering + DPO | *[QA test confirms PII deletion from all systems (database, logs, model pipeline) within 30 days; DPO reviews and signs off; deletion audit log maintained; tested with 10 synthetic customer profiles]* | N/A | 🔴 High | GDPR | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| COMP-031 | Compliance | *[e.g., The EU AI Act technical documentation package (Art. 11) SHALL be completed, reviewed by Legal, and archived before the product processes any live EU applicant SO THAT the bank can demonstrate conformity to market surveillance authorities on request.]* | *[EU AI Act Art. 11; Legal Counsel]* | 🔴 Critical | Phase 4 | AI Lead + Legal | *[Art. 11 technical documentation checklist completed; all 9 required sections present; reviewed by Legal; archived in compliance folder; DPO and AI Lead signatures obtained]* | N/A | 🔴 High | EU-AI-Act | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

---

## Phase 5 — Launch & Go-to-Market (First 500 Customers)
*Goal: Deploy to production. Monitor AI model performance, credit decisions, and fraud detection in real time.*
*Typical owners: PM, DevOps/SRE, AI Monitoring Engineer, Fraud Team, Customer Success.*

> ⚠️ **Regulatory reminder:** From your first live EU customer, you are subject to EU AI Act obligations.
> Ensure audit logging (AI-040) is active from Day 1.

### 5A · Functional Requirements — Launch

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-040 | Functional | *[e.g., The loan onboarding flow SHALL guide a first-time applicant from account creation to loan decision in ≤12 minutes with AI-assisted document verification (OCR for ID and pay slips) SO THAT the application experience is fast enough to prevent drop-off and competitive with market leaders.]* | *[US-001; Competitive Analysis: market average 18 min; Growth OKR Q1]* | 🔴 Critical | Phase 5 | PM + Growth | *[A/B test with first 100 applicants: median application time ≤ 12 min; completion rate ≥ 65%; OCR auto-fill accuracy ≥ 90% for ID fields; measured in product analytics]* | N/A | 🟡 Medium | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 5B · Non-Functional Requirements — Launch SLAs

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| NFR-040 | Non-Functional | *[e.g., The production credit scoring and loan origination system SHALL maintain ≥ 99.95% monthly uptime for the first 90 days post-launch SO THAT applicants can access the service reliably and the bank meets its SLA commitments to distribution partners.]* | *[SLA Commitments; SOC 2 A1.2; Regulator Expectations]* | 🔴 Critical | Phase 5 | DevOps / SRE | *[Uptime monitoring (e.g., Datadog, PagerDuty) active from Day 1; monthly SLA report reviewed by CTO and PM; 99.95% achieved for first 3 months; incident log maintained]* | N/A | 🟡 Medium | SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 5C · AI-Specific Requirements — Live AI Monitoring

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-040 | AI-Specific | *[e.g., The AI credit scoring system SHALL record an immutable audit log entry for every credit decision containing: model version ID, input features used (excluding raw PII), output score, SHAP explanation, human override flag, and final decision SO THAT any individual credit decision can be reconstructed and explained to the applicant or regulator within 24 hours of request.]* | *[EU AI Act Art. 12; FCRA §607; DPO Mandate]* | 🔴 Critical | Phase 5 | AI Monitoring Lead + Engineering | *[All 7 fields present in 100% of logged decisions; log is append-only and tamper-evident (cryptographic hash chain); reconstruction test passes for 10 sample decisions; active from Day 1 of launch]* | N/A | 🔴 High | EU-AI-Act, FCRA | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| AI-041 | AI-Specific | *[e.g., The AI model monitoring system SHALL send an automated alert to the AI Lead and CRO within 15 minutes if the live credit scoring model's AUC-ROC on a rolling 7-day sample drops more than 3 percentage points below the launch baseline SO THAT model drift is detected and the CRO can decide whether to trigger a model rollback or expedited retraining before customers are materially harmed.]* | *[US-009; NIST AI RMF MEASURE 2.6; AI Monitoring Policy v1.0]* | 🔴 Critical | Phase 5 | AI Monitoring Lead | *[Alert fires within 15 minutes in 3 synthetic drift simulations run pre-launch; alert routes to AI Lead and CRO via PagerDuty and email; false positive rate < 5% in first 30-day post-launch monitoring window]* | *[Alert latency ≤ 15 min; false positive rate < 5% in first 30 days live]* | 🔴 High | NIST-AI-RMF, EU-AI-Act | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 5D · Compliance Requirements — Launch

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| COMP-040 | Compliance | *[e.g., All EU applicants SHALL see a GDPR-compliant consent banner on first visit with separate consent toggles for analytics cookies, marketing cookies, and functional cookies SO THAT no non-essential cookies are set before explicit consent, and the bank is not subject to ePrivacy Directive enforcement action.]* | *[GDPR Art. 6; ePrivacy Directive; DPO Mandate]* | 🔴 Critical | Phase 5 | Legal + Frontend | *[Consent banner reviewed and approved by DPO; analytics cookies absent until consent given (confirmed via network inspection in QA); live on Day 1 for all EU traffic]* | N/A | 🔴 High | GDPR | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

---

## Phase 6 — Post-Launch Iteration
*Goal: Improve the product based on real applicant data. Retrain AI models. Fix bugs. Hit 500-customer milestone.*
*Typical owners: PM, AI/ML Lead, Growth Lead, Customer Success, CRO.*

> 💡 **FinTech iteration tip:** Every new model version must clear ALL fairness and performance thresholds
> from Phase 4 before replacing the live model. Never deploy a new model without sign-off.

### 6A · Functional Requirements — Iteration

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-050 | Functional | *[e.g., Based on feedback from the first 100 customers, the mobile app SHALL be updated to support document upload via smartphone camera with automatic OCR extraction of key fields (name, address, income, employer) SO THAT applicants can complete the application without scanning documents on a separate device, reducing the drop-off rate at the document step.]* | *[US-010; User Feedback Batch 1; Drop-off analysis: 34% abandon at document upload step]* | 🟠 High | Phase 6 | PM + Mobile Engineer | *[Camera upload functional on iOS 16+ and Android 13+; OCR accuracy ≥ 90% for name, address, income fields on a 50-document test set; document step drop-off rate reduces by ≥ 15% in A/B test]* | N/A | 🟡 Medium | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 6B · AI-Specific Requirements — Model Retraining & Continuous Improvement

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-050 | AI-Specific | *[e.g., After processing 20,000 real loan applications, the AI credit scoring model SHALL be retrained on the updated production dataset, re-evaluated against ALL Phase 4 fairness and performance validation criteria, and formally re-approved by the AI Lead and CRO before the updated model version is deployed to production SO THAT model quality improves on real data without regressing on fairness or accuracy.]* | *[US-009; NIST AI RMF MANAGE 4.1; Continuous Improvement Policy v1.0; EU AI Act Art. 9]* | 🔴 Critical | Phase 6 | AI/ML Lead + CRO | *[Retrained model achieves AUC-ROC ≥ launch baseline; demographic parity difference ≤ 5% for all groups; adversarial test suite re-run with ≥ same results; updated model card published; CRO and AI Lead sign-off obtained before deployment; model version change logged in this RTM Change Log]* | *[Retrained model AUC-ROC ≥ v1.0 baseline; demographic parity ≤ 5%; no regression on any Phase 4 metric]* | 🔴 High | EU-AI-Act, ECOA, NIST-AI-RMF | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

---

## Phase 7 — Mobile App Requirements (iOS & Android)
*Goal: Capture requirements that are specific to the iOS and Android mobile apps, in addition to the web platform.*
*Typical owners: Mobile Lead Engineer, UX Designer, PM, Security Lead, App Store Compliance.*

> 💡 **Why a separate mobile section?** Mobile apps have unique requirements around:
> - **App Store policies** (Apple App Store Review Guidelines; Google Play Policy) — violating these can result in rejection or removal from the store
> - **Device permissions** (camera, biometrics, notifications) — users must explicitly grant these; the app must work if they don't
> - **Sensitive data on device** (no plaintext financial data stored locally)
> - **Offline behaviour** (what happens when the applicant loses signal mid-application?)
> - **Biometric authentication** (Face ID, Touch ID) — stronger than passwords, preferred by FCA
>
> Add a row for every mobile-specific requirement. If a requirement already exists in Phases 1–6 AND applies identically on mobile, you do NOT need to duplicate it here — just add a `MOBILE` tag in its Compliance Tag column.

### 7A · Mobile Functional Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| MOB-001 | Functional | *[e.g., The iOS and Android apps SHALL support biometric authentication (Face ID on iOS 16+; fingerprint on Android 10+) as an alternative to PIN/password for returning users, with automatic fallback to PIN/password if biometric authentication fails 3 times SO THAT users benefit from a fast, secure login experience preferred by FCA Consumer Duty guidelines.]* | *[US-001; FCA Consumer Duty; Apple App Store Review Guideline 5.1.1]* | 🔴 Critical | Phase 7 | Mobile Lead | *[Face ID functional on iPhone 12–16 Pro; fingerprint functional on 5 Samsung and Google Pixel test devices; fallback to PIN triggers after 3 failed biometric attempts; biometric data never leaves device (no server-side storage confirmed in security audit)]* | N/A | 🟡 Medium | SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| MOB-002 | Functional | *[e.g., The mobile app SHALL request the device camera permission only when the user reaches the document upload step and SHALL provide a clear plain-English explanation of why the permission is needed ("We need camera access to photograph your documents — this is optional; you can upload files instead") SO THAT users understand and consent to each permission request, and the app complies with Apple App Store Guideline 5.1.1 and Google Play Permissions Policy.]* | *[Apple App Store Review Guideline 5.1.1; Google Play Permissions Policy; GDPR Art. 6]* | 🔴 Critical | Phase 7 | Mobile Lead + Legal | *[Camera permission requested only at document upload step (confirmed in app flow audit); permission dialogue includes purpose string exactly as specified; app fully functional if user declines camera (file upload alternative visible); tested on iOS 17 and Android 14]* | N/A | 🟢 Low | GDPR | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| MOB-003 | Functional | *[e.g., The mobile app SHALL send a push notification to the applicant's device within 5 minutes of a credit decision being made (Approved / Referred / Declined) with a personalised message that does NOT contain the loan decision outcome in the notification preview SO THAT applicants are notified promptly without exposing sensitive financial information on their lock screen where other people could see it.]* | *[US-001; FCA Consumer Duty; GDPR Art. 5(1)(f) — data integrity and confidentiality]* | 🟠 High | Phase 7 | Mobile Lead + PM | *[Push notification delivered within 5 minutes in 100% of 50 test scenarios; notification preview text confirmed to not contain decision outcome (tested on iOS Lock Screen and Android notification shade); notifications link to in-app decision screen behind authentication]* | N/A | 🟡 Medium | GDPR | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| MOB-004 | Functional | *[e.g., The mobile app SHALL handle loss of network connectivity gracefully: if the user loses signal mid-application, all completed form data SHALL be preserved locally in encrypted temporary storage (AES-256), and the user SHALL see a clear "Connection lost — your progress is saved" message SO THAT applicants do not lose their work and are not forced to restart the application from the beginning.]* | *[US-001; UX Research: 22% of mobile users reported connectivity issues during application]* | 🟠 High | Phase 7 | Mobile Lead | *[Simulated offline scenario: all form data preserved after 10-minute offline period; user shown correct offline message; data restored correctly on reconnection; encrypted storage confirmed (no plaintext in app sandbox inspection); tested on iOS and Android with airplane mode simulation]* | N/A | 🟢 Low | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| MOB-005 | Functional | *[e.g., The mobile app SHALL prevent screenshots, screen recordings, and screen sharing on all screens that display sensitive financial information (loan amount, credit decision, account details, income data) by enabling the operating system's secure flag (FLAG_SECURE on Android; UIScreen.isCaptureProtected on iOS 17+) SO THAT customer financial data is not inadvertently shared or captured.]* | *[SOC 2 CC6.7; GDPR Art. 5(1)(f); FCA COBS 2.1; Mobile Security Best Practice]* | 🔴 Critical | Phase 7 | Mobile Lead + Security | *[Screenshot attempt on decision screen on Android 14 produces blank/black capture (confirmed in testing); iOS 17 screen recording shows blank on sensitive screens; tested across 8 devices; does not block screenshots on non-sensitive screens (e.g., FAQ, marketing)]* | N/A | 🔴 High | GDPR, SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 7B · Mobile Non-Functional Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| MOB-010 | Non-Functional | *[e.g., The mobile app SHALL NOT store any customer PII or financial data (credit score, income, loan amount, bank account details) in plaintext on the device local storage, SQLite database, or shared clipboard SO THAT a device theft, cloud backup, or forensic examination does not expose customer financial data.]* | *[GDPR Art. 25; SOC 2 CC6.7; OWASP Mobile Top 10 M2]* | 🔴 Critical | Phase 7 | Mobile Lead + Security | *[Static analysis (MobSF scan) confirms no PII in local storage; dynamic analysis (Burp Suite) confirms no sensitive data in local database files; keychain/keystore used for session tokens only; all financial data fetched from API on-demand, never cached locally; no sensitive data in clipboard]* | N/A | 🔴 High | GDPR, SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| MOB-011 | Non-Functional | *[e.g., The mobile app SHALL be compatible with and tested on: (iOS) iPhone XR and above running iOS 15.0+; (Android) devices running Android 10 (API 29)+ with minimum 3GB RAM SO THAT the app reaches ≥95% of the UK smartphone market and is not rejected by the App Store or Google Play for compatibility reasons.]* | *[App Store Compatibility Requirements; Market Research: UK smartphone OS distribution 2026]* | 🟠 High | Phase 7 | Mobile Lead | *[App tested on iOS: iPhone XR, 12 mini, 13, 14 Pro, 15, 15 Pro Max; Android: Samsung Galaxy A54, S23, Google Pixel 7, OnePlus 11 (all on Android 10–14); zero crashes on any test device; App Store and Google Play technical requirements met before submission]* | N/A | 🟢 Low | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| MOB-012 | Non-Functional | *[e.g., The mobile app SHALL achieve WCAG 2.1 Level AA accessibility compliance for all screens, including: support for Dynamic Type (iOS) and font scaling up to 200% (Android), full VoiceOver / TalkBack compatibility on all interactive elements, and a minimum touch target size of 44×44 points SO THAT the app is usable by customers with visual or motor impairments and complies with the UK Equality Act 2010 and FCA Consumer Duty accessibility requirements.]* | *[UK Equality Act 2010; FCA Consumer Duty; WCAG 2.1 Level AA; Apple HIG; Android Accessibility Guidelines]* | 🟠 High | Phase 7 | Mobile Lead + UX | *[Automated accessibility scan (Axe Mobile, Deque) passes with zero Level AA violations; manual VoiceOver test by accessibility tester confirms all interactive elements labelled; font scaling to 200% tested without layout breakage; minimum touch target confirmed in UI audit]* | N/A | 🟡 Medium | None | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

### 7C · App Store Compliance Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| MOB-020 | Compliance | *[e.g., The iOS app SHALL include a complete and accurate App Privacy Nutrition Label in App Store Connect, declaring all data types collected (Name, Email, Financial Info, Device ID, Usage Data), the purpose of each collection, and whether each is linked to the user's identity, SO THAT the app passes Apple App Store Review and GDPR transparency obligations under Art. 13 are met for iOS users.]* | *[Apple App Store Review Guideline 5.1.2; GDPR Art. 13]* | 🔴 Critical | Phase 7 | Legal + Mobile Lead | *[Privacy Nutrition Label reviewed by DPO and Legal before App Store submission; all data types accurately declared; submission not rejected for privacy reasons; label matches the Privacy Policy published on the website]* | N/A | 🔴 High | GDPR | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |
| MOB-021 | Compliance | *[e.g., The Android app SHALL implement a mandatory in-app update flow using the Google Play In-App Update API (Immediate update type) for any update that patches a Critical or High severity security vulnerability, SO THAT customers with unpatched security vulnerabilities are required to update before using the app and the bank minimises liability from known unpatched vulnerabilities in the wild.]* | *[Google Play Policy; SOC 2 CC7.4; Security Incident Response Policy]* | 🔴 Critical | Phase 7 | Mobile Lead | *[Immediate update flow tested with internal test track; app cannot proceed past the update screen until update is installed; tested on Android 10, 12, and 14; update successfully delivered within 15 minutes of Play Store publication in test]* | N/A | 🟡 Medium | SOC2 | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

---

---

# SECTION 5 — Compliance Traceability Matrix

> 💡 **How to fill this section:** For each regulation, list the specific article or control,
> describe what it requires, then list the REQ IDs that address it.
> If any row has no mapped REQ IDs — that is a compliance gap. Add a requirement.

## 5.1 · GDPR (General Data Protection Regulation)

| GDPR Article | Title | What It Requires (Plain English) | Mapped REQ IDs | Verification Status |
|-------------|-------|----------------------------------|---------------|---------------------|
| Art. 5(1)(a) | Lawfulness, fairness, transparency | Collect and process applicant data lawfully and tell users exactly how their credit data is used. | `COMP-001` | ☐ Pending |
| Art. 6 | Lawfulness of processing | Have a valid legal basis (consent, contract, legitimate interest) before processing PII. | `COMP-040` | ☐ Pending |
| Art. 9 | Special categories of data | Obtain explicit consent before processing sensitive data (health, biometrics). | `[REQ ID]` | ☐ Pending |
| Art. 13 / 14 | Transparency & information | Tell applicants what data you collect and why, in plain language, at the point of collection. | `FUNC-021` | ☐ Pending |
| Art. 17 | Right to erasure | Delete all customer PII — including from AI training pipelines — within 30 days of a verified request. | `COMP-030` | ☐ Pending |
| Art. 20 | Right to data portability | Let customers download all their application and scoring data in a machine-readable format. | `[REQ ID]` | ☐ Pending |
| Art. 25 | Data protection by design | Build privacy protections (data minimisation, encryption) into the architecture from day one. | `NFR-002, NFR-010` | ☐ Pending |
| Art. 32 | Security of processing | Implement encryption at rest and in transit; access controls; security monitoring. | `NFR-002, COMP-020, NFR-030` | ☐ Pending |
| Art. 35 | Data Protection Impact Assessment | Complete a DPIA before processing high-risk data — mandatory for AI credit scoring. | `COMP-010` | ☐ Pending |

## 5.2 · SOC 2 (Service Organization Control 2)

| SOC 2 Criteria | Category | What It Requires (Plain English) | Mapped REQ IDs | Verification Status |
|---------------|----------|----------------------------------|---------------|---------------------|
| CC6.1 | Logical Access | Implement controls to prevent unauthorised access to systems and financial data. | `FUNC-020, COMP-020` | ☐ Pending |
| CC6.3 | Access Provisioning | Follow least-privilege when granting user access to customer credit data. | `COMP-020` | ☐ Pending |
| CC6.7 | Data Transmission | Encrypt data in transit and at rest to protect against interception. | `NFR-002` | ☐ Pending |
| CC7.1 | Security Monitoring | Monitor systems for security threats and vulnerabilities continuously. | `NFR-030` | ☐ Pending |
| CC9.2 | Incident Response | Have a documented and tested incident response plan for security breaches. | `[REQ ID]` | ☐ Pending |
| A1.2 | Availability Monitoring | Monitor system availability and report against SLA commitments. | `NFR-040` | ☐ Pending |

## 5.3 · EU AI Act (High-Risk AI — Annex III, Credit Scoring)

| EU AI Act Article | Title | What It Requires (Plain English) | Mapped REQ IDs | Verification Status |
|------------------|-------|----------------------------------|---------------|---------------------|
| Art. 9 | Risk Management System | Identify, analyse, and mitigate AI risks continuously across the model life cycle. | `AI-002, AI-031` | ☐ Pending |
| Art. 10 | Data Governance | Training data must be representative, free from errors, and audited for bias. | `AI-020, AI-030` | ☐ Pending |
| Art. 11 | Technical Documentation | Maintain full technical documentation proving conformity — regulators can request this. | `COMP-031` | ☐ Pending |
| Art. 12 | Record Keeping | Log AI system inputs and outputs automatically for auditability. | `AI-040` | ☐ Pending |
| Art. 13 | Transparency | Inform users clearly that they are interacting with an AI system and explain decisions. | `FUNC-021, AI-022` | ☐ Pending |
| Art. 14 | Human Oversight | Humans must be able to review, override, or shut down the AI credit scoring system. | `FUNC-011` | ☐ Pending |
| Art. 15 | Accuracy, Robustness, Cybersecurity | AI systems must meet accuracy and robustness standards through their full life cycle. | `AI-021, AI-050` | ☐ Pending |

## 5.4 · NIST AI RMF (AI Risk Management Framework)

| NIST Function | Sub-Category | What It Requires (Plain English) | Mapped REQ IDs | Verification Status |
|--------------|-------------|----------------------------------|---------------|---------------------|
| GOVERN 1.1 | Policy & Accountability | Establish organisational policies for responsible AI in credit decisions. | `COMP-002` | ☐ Pending |
| GOVERN 6.2 | Fairness & Bias | Address fairness and bias in AI design and deployment. | `AI-020, AI-030` | ☐ Pending |
| MAP 5.1 | AI Risk Identification | Identify and document AI-specific risks before deployment. | `AI-031` | ☐ Pending |
| MEASURE 2.6 | Performance Monitoring | Monitor AI system performance in production for drift. | `AI-041` | ☐ Pending |
| MANAGE 4.1 | Continuous Improvement | Implement processes for ongoing AI system improvement and retraining. | `AI-050` | ☐ Pending |

## 5.5 · FCRA (Fair Credit Reporting Act) & ECOA (Equal Credit Opportunity Act)

| Regulation | Section | What It Requires (Plain English) | Mapped REQ IDs | Verification Status |
|-----------|---------|----------------------------------|---------------|---------------------|
| FCRA §615(a) | Adverse Action Notices | Send a written notice to every denied applicant listing the reasons for denial and the credit bureau used. | `FUNC-002, COMP-001, AI-022` | ☐ Pending |
| FCRA §607 | Permissible Purpose | Only access credit data for a permissible purpose (e.g., a completed credit application). | `COMP-020` | ☐ Pending |
| ECOA Reg. B | Anti-Discrimination | Never discriminate based on race, colour, religion, national origin, sex, marital status, or age. | `AI-020, AI-023, AI-030` | ☐ Pending |
| ECOA — Disparate Impact | Fairness | Even neutral-seeming criteria are unlawful if they cause a disparate impact on a protected class. | `AI-020, AI-023, AI-030` | ☐ Pending |

---

---

# SECTION 6 — AI Model Card
*(Complete one Model Card per AI model. Duplicate this section for each model — e.g., one for credit scoring, one for fraud detection.)*

> 💡 **What is a Model Card?** A short technical summary of an AI model — what it does, how it was trained,
> how it performs, and what its limitations are. Required by EU AI Act Art. 11 for High-Risk AI systems.

## 6.1 · Model Card — `[Model Name / Version]` (e.g., Credit Scoring Model v1.0)

| Field | Value |
|-------|-------|
| **Model Name** | `[e.g., LoanPilot Credit Scoring Model v1.0]` |
| **Model Type** | `[e.g., Gradient Boosted Trees (XGBoost) with SHAP explanations]` |
| **Primary Use Case** | `[e.g., Assess creditworthiness of personal loan applicants aged 18+ and generate a probability of default score]` |
| **Out-of-Scope Uses** | `[e.g., Must NOT be used for mortgage decisions, insurance underwriting, or employment screening]` |
| **Training Data Summary** | `[Source, size (e.g., 500,000 historical loan applications), date range (2019–2025), demographic coverage]` |
| **Training Data Bias Audit** | ☐ Completed by Third Party   ☐ Completed Internally   ☐ In Progress   ☐ Not Started |
| **Performance — AUC-ROC** | `[e.g., 0.87 on held-out test set of 50,000 applications]` |
| **Performance — Gini Coefficient** | `[e.g., 0.74]` |
| **Fairness — Demographic Parity Difference** | `[e.g., 0.032 across gender groups; 0.041 across age bands — all within ≤ 5% threshold]` |
| **False Positive Rate (Fraud Model)** | `[e.g., 0.38% — within ≤ 0.5% threshold; no disparate impact across demographic groups]` |
| **Known Limitations** | `[List known failure modes: e.g., performance degrades on applicants with < 12 months of banking history; not validated on applicants over 75 years old]` |
| **Guardrails & Safety Mechanisms** | `[e.g., Confidence threshold < 70% → automatic referral to human underwriter; outlier detection flags anomalous input vectors; model output capped between 0 and 1000]` |
| **Human Oversight Mechanism** | `[Describe: underwriter review queue for low-confidence decisions; CRO can trigger model rollback; emergency kill switch documented in runbook]` |
| **Explainability Method** | `[e.g., SHAP values for all decisions; top 5 features mapped to plain-language adverse action reasons]` |
| **Model Owner** | `[Full Name + Role]` |
| **Last Evaluation Date** | `[YYYY-MM-DD]` |
| **Next Scheduled Re-evaluation** | `[YYYY-MM-DD — or after 20,000 live applications, whichever comes first]` |
| **EU AI Act Risk Category** | ☑ High Risk — Annex III Point 5(b): Creditworthiness Assessment |
| **NIST AI RMF Risk Level** | `[e.g., Tier 3 — High]` |
| **Model Card Version** | `[e.g., v1.0]` |
| **Model Card Sign-Off** | `[AI Lead Name, CRO Name, DPO Name + Dates]` |

## 6.2 · Model Card — `[Model Name / Version]` (e.g., Fraud Detection Model v1.0)

*(Duplicate Section 6.1 fields here for each additional AI model.)*

---

---

# SECTION 7 — First 500 Customers Tracker

## 7.1 · Customer Milestone Tracker

| Milestone | Target Date | Actual Date | Customer Count | Key Metric to Confirm | Status |
|-----------|------------|------------|:--------------:|----------------------|:------:|
| First 10 approved loans disbursed | `[Date]` | | 10 | Zero fraud incidents; adverse action notices sent | ☐ |
| First 50 customers (onboarding NPS) | `[Date]` | | 50 | NPS ≥ 40; application completion rate ≥ 65% | ☐ |
| First 100 customers (AI fairness check) | `[Date]` | | 100 | Demographic parity difference still ≤ 5% on live data | ☐ |
| First 250 customers (30-day repayment) | `[Date]` | | 250 | Early repayment rate within 3% of model prediction | ☐ |
| First 500 customers (milestone celebration) | `[Date]` | | 500 | Monthly churn < 3%; NPS ≥ 40; 0 regulatory complaints | ☐ |

## 7.2 · Live AI Model Performance (Post-Launch Monitoring)

| Metric | Launch Baseline | Current Value | Target | Drift Alert Threshold | Status |
|--------|:--------------:|:-------------:|:------:|:--------------------:|:------:|
| Credit Model AUC-ROC | `[e.g., 0.87]` | `[Update monthly]` | `≥ 0.85` | Drop > 3pp | ☐ OK |
| Gini Coefficient | `[e.g., 0.74]` | | `≥ 0.70` | Drop > 4pp | ☐ OK |
| Demographic Parity Difference | `[e.g., 0.032]` | | `≤ 0.05` | Rise > 0.02 | ☐ OK |
| Fraud Model FPR | `[e.g., 0.38%]` | | `≤ 0.5%` | Rise > 0.1pp | ☐ OK |
| Fraud Recall | `[e.g., 87%]` | | `≥ 85%` | Drop > 5pp | ☐ OK |
| Credit Scoring Latency (p99) | `[e.g., 2.1s]` | | `< 3s` | Rise > 0.5s | ☐ OK |
| Adverse Action Notice Delivery | `100%` | | `100%` | Any miss | 🔴 Alert |
| SHAP Explanation Coverage | `100%` | | `100%` | Any gap | 🔴 Alert |

## 7.3 · Open Issues & Compliance Gaps (Post-Launch)

| Issue ID | Affected REQ ID | Description | Severity | Owner | Target Fix Date | Status |
|----------|-----------------|-------------|:--------:|-------|:--------------:|:------:|
| `ISS-001` | `[REQ ID]` | `[What the issue is]` | 🔴 Critical | `[Name]` | `[YYYY-MM-DD]` | Open |

---

---

# SECTION 8 — Phase Sign-Off & Approvals

> 💡 **FinTech note:** These sign-offs are legal records. In the event of a regulatory investigation
> (e.g., FCA, CFPB, or EU market surveillance authority), sign-off dates and named approvers
> demonstrate that governance processes were followed.

| Phase | Phase Name | Sign-Off By (Name) | Role | Signature / Initials | Date | Comments |
|:-----:|-----------|-------------------|------|:-------------------:|:----:|---------|
| 1 | Discovery & Ideation | | | | | |
| 2 | Design & Architecture | | | | | |
| 3 | Development & AI Training | | | | | |
| 4 | Testing, QA & AI Validation | | | | | |
| 5 | Launch & Go-to-Market | | | | | |
| 6 | Post-Launch Iteration (Cycle 1) | | | | | |

### AI Credit System Launch Approval Panel
> *This approval certifies that the AI credit scoring system is safe, fair, compliant, and ready for live applicants.*

| Approver Role | Full Name | Signature / Initials | Date | Certification Statement |
|--------------|-----------|:-------------------:|:----:|------------------------|
| AI / ML Lead | | | | I confirm the AI models meet all Phase 4 performance, fairness, and robustness criteria. |
| Chief Risk Officer (CRO) | | | | I confirm the AI credit risk is within approved limits and model governance is in place. |
| QA Lead | | | | I confirm all test cases have passed or been formally risk-accepted. |
| Compliance / Legal Officer | | | | I confirm all legal and regulatory obligations (FCRA, ECOA, GDPR, EU AI Act) are met. |
| Data Protection Officer (DPO) | | | | I confirm GDPR and DPIA obligations are satisfied. |
| CISO / Security Lead | | | | I confirm the security posture is acceptable for processing live customer financial data. |
| Product Owner | | | | I confirm the product is ready to serve real customers and meets the business requirements. |

---

---

# SECTION 9 — Change Log

> 💡 **Why this matters in FinTech:** FCRA §607 requires that credit decisions are made using accurate,
> current information. Under the EU AI Act, you must be able to show which model version was in use at
> any given time. The Change Log is your proof. Never delete a row. Never reuse an old REQ ID.

| Change ID | Date | REQ ID Affected | Old Version | New Version | What Changed | Reason for Change | Impact on Tests | Approved By | Approval Date |
|-----------|------|----------------|:-----------:|:-----------:|-------------|------------------|----------------|-------------|:------------:|
| CHG-001 | `[YYYY-MM-DD]` | `[e.g., AI-021]` | v1.0 | v1.1 | `[What specifically changed in the requirement or threshold]` | `[e.g., Regulator guidance updated minimum AUC threshold / User feedback / Model performance data]` | `[Which test cases must be rerun]` | `[Name + Role]` | `[YYYY-MM-DD]` |

---

---

# SECTION 10 — Document Control

| Field | Value |
|-------|-------|
| **Document Owner** | `[Full Name — typically Product Manager or Compliance Officer]` |
| **Review Frequency** | At end of every phase; after every AI model update; after any regulatory change |
| **Storage Location** | `[e.g., /docs/compliance/RTM/ in version-controlled project repository]` |
| **Access Control** | `[e.g., View: All team members. Edit: PM, AI Lead, Legal. Approve: CRO, DPO]` |
| **Related Documents** | Test Plan · Risk Register · AI Model Cards · Data Processing Agreement · DPIA · System Architecture Doc · Bias Audit Reports · Adverse Action Notice Templates · EU AI Act Technical Documentation (Art. 11) |
| **Next Scheduled Review** | `[YYYY-MM-DD]` |
| **Retention Policy** | `[e.g., Retain for 7 years from last credit decision made using this model version — FCRA and GDPR requirements]` |

---

*Requirements Traceability Matrix · AI-Driven Development Life Cycle*
*Template Version 1.2 · FinTech / AI Banking Edition*
*Covers: EU AI Act (High-Risk, Annex III) · NIST AI RMF · GDPR · SOC 2 · FCRA · ECOA · PCI DSS*
*Last Updated: 2026-10-14*
