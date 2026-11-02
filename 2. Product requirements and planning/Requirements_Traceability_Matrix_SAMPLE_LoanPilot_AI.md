# Requirements Traceability Matrix — SAMPLE PROJECT
## LoanPilot AI · Intelligent Personal Loan Origination Platform
> **⚠️ THIS IS A SAMPLE / EXAMPLE FILE** — Use this to understand what a completed RTM looks like.
> All company names, people, dates, and metrics are fictional.
> Copy the blank template (`Requirements_Traceability_Matrix.md`) to start your own project.

---

# SECTION 1 — Document Information

| Field | Value |
|-------|-------|
| **Project / Product Name** | LoanPilot AI — Intelligent Personal Loan Origination Platform |
| **Document Title** | Requirements Traceability Matrix |
| **Document ID** | DOC-RTM-001 |
| **Product Type** | ☑ SaaS / Web App   ☑ Mobile App (iOS)   ☑ Mobile App (Android) |
| **Version** | v1.3 |
| **Status** | ✅ Active |
| **Date Created** | 2026-01-15 |
| **Last Updated** | 2026-10-14 |
| **Project Manager** | Priya Sharma |
| **Product Owner** | Marcus Webb |
| **Tech Lead / Architect** | Elena Kowalski |
| **AI / ML Lead** | Dr. James Okonkwo |
| **QA Lead** | Tomás Rivera |
| **Compliance / Legal Officer** | Fatima Al-Hassan |
| **Chief Risk Officer (CRO)** | David Chen |
| **Data Protection Officer (DPO)** | Sophie Müller |
| **Target Launch Date** | 2026-06-01 |
| **First 500 Customers Goal Date** | 2026-09-01 |
| **AI Governance Framework** | ☑ EU AI Act (Annex III — High Risk: Credit Scoring)   ☑ NIST AI RMF |
| **Data Privacy Regulations** | ☑ GDPR   ☑ SOC 2   ☑ CCPA |
| **Financial Regulations** | ☑ FCRA   ☑ ECOA   ☑ FCA (UK) |
| **AI Risk Category (EU AI Act)** | ☑ High Risk — Annex III Point 5(b): AI used for creditworthiness assessment |

---

# SECTION 3 — Requirements Summary Dashboard

## 3.1 · Requirement Count by Type

| Requirement Type | Total Defined | Approved | In Progress | Testing | Done | Deprecated |
|-----------------|:---:|:---:|:---:|:---:|:---:|:---:|
| Functional (FUNC) | 14 | 14 | 0 | 0 | 12 | 2 |
| Non-Functional (NFR) | 8 | 8 | 0 | 0 | 8 | 0 |
| AI-Specific (AI) | 10 | 10 | 0 | 0 | 9 | 1 |
| Compliance (COMP) | 9 | 9 | 0 | 0 | 9 | 0 |
| **TOTAL** | **41** | **41** | **0** | **0** | **38** | **3** |

## 3.2 · Phase Completion Status

| Phase | Phase Name | Requirements Defined | Requirements Done | % Complete | Phase Sign-Off |
|:-----:|-----------|:---:|:---:|:---:|:---:|
| 1 | Discovery & Ideation | 10 | 10 | 100% | ✅ Signed — 2026-02-12 |
| 2 | Design & Architecture | 8 | 8 | 100% | ✅ Signed — 2026-03-28 |
| 3 | Development & AI Training | 12 | 12 | 100% | ✅ Signed — 2026-05-10 |
| 4 | Testing, QA & AI Validation | 6 | 6 | 100% | ✅ Signed — 2026-05-28 |
| 5 | Launch & Go-to-Market | 5 | 5 | 100% | ✅ Signed — 2026-06-01 |
| 6 | Post-Launch Iteration | 3 | 0 | 0% | ☐ Pending |

## 3.3 · AI Risk Summary

| Risk Level | Count | % of Total |
|:----------:|:-----:|:----------:|
| 🔴 High | 28 | 68% |
| 🟡 Medium | 9 | 22% |
| 🟢 Low | 4 | 10% |

## 3.4 · Compliance Coverage

| Regulation | Requirements Mapped | Requirements Verified | Gap Count |
|------------|:---:|:---:|:---:|
| GDPR | 7 | 7 | 0 |
| SOC 2 | 5 | 5 | 0 |
| EU AI Act (High Risk) | 9 | 9 | 0 |
| NIST AI RMF | 6 | 5 | 1 |
| FCRA | 3 | 3 | 0 |
| ECOA | 4 | 4 | 0 |
| PCI DSS | 2 | 2 | 0 |

---

# SECTION 4.0 — User Story → Requirement Mapping

| US ID | User Story | User Type | Mapped REQ IDs | Primary Phase | Priority | Status |
|-------|-----------|-----------|---------------|:-------------:|:--------:|:------:|
| US-001 | As a first-time loan applicant, I want to apply for a personal loan online so that I can get a credit decision without visiting a bank branch. | Customer | `FUNC-001, NFR-001, FUNC-040` | Phase 1, 5 | 🔴 Critical | ✔️ Done |
| US-002 | As a denied loan applicant, I want to receive a clear explanation of why my application was rejected so that I understand what I need to improve. | Customer | `AI-022, COMP-001, FUNC-021, AI-032` | Phase 1, 3, 4 | 🔴 Critical | ✔️ Done |
| US-003 | As a thin-file applicant with no traditional credit history, I want my alternative financial data (rent, utilities) to be considered so that I am not automatically excluded from credit. | Underserved Customer | `AI-001, AI-020` | Phase 1, 3 | 🔴 Critical | ✔️ Done |
| US-004 | As a bank compliance officer, I want a full audit trail of every AI credit decision so that I can respond to regulatory examinations. | Internal — Compliance | `AI-040, AI-022` | Phase 5 | 🔴 Critical | ✔️ Done |
| US-005 | As a fraud analyst, I want to be alerted in real time when the AI flags suspicious account activity so that I can investigate before money is moved. | Internal — Fraud Team | `AI-002, AI-041, NFR-020` | Phase 1, 5 | 🔴 Critical | ✔️ Done |
| US-006 | As an EU customer, I want to be able to request deletion of all my personal data so that my GDPR rights are respected. | EU Customer | `COMP-030, COMP-010` | Phase 2, 4 | 🔴 Critical | ✔️ Done |
| US-007 | As a mobile banking customer, I want to check my loan application status from my phone so that I can stay informed without logging into a desktop browser. | Mobile Customer | `FUNC-010, NFR-040` | Phase 2, 5 | 🟠 High | ✔️ Done |
| US-008 | As an underwriter, I want the AI to flag applications for human review when its confidence is low so that I can apply my judgement to borderline cases. | Internal — Underwriter | `AI-010, AI-021, FUNC-011` | Phase 2, 3 | 🔴 Critical | ✔️ Done |
| US-009 | As a product manager, I want to see live AI model performance metrics on a dashboard so that I can detect model drift before it affects customers. | Internal — PM | `AI-041, NFR-040` | Phase 5, 6 | 🟠 High | ✔️ Done |
| US-010 | As a returning customer with 12 months of good repayment history, I want a faster repeat-loan application so that loyal customers are rewarded with a smoother experience. | Returning Customer | `FUNC-050` | Phase 6 | 🟡 Medium | 🏗️ In Progress |

---

# SECTION 4 — Requirements Matrix

## Phase 1 — Discovery & Ideation

### 1A · Functional Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-001 | Functional | The system SHALL allow any individual aged 18+ to complete a digital personal loan application from a web browser or mobile app in ≤15 minutes, with AI-assisted document verification for ID and income proof, SO THAT customers can apply for credit of £1,000–£25,000 without visiting a branch. | US-001; Business Case v1.0 | 🔴 Critical | Phase 1 | Priya Sharma (PM) | Application captures all 14 required fields; end-to-end journey tested on 5 devices (iPhone 15, Samsung Galaxy S24, MacBook, Windows laptop, iPad); average completion time ≤15 min in user testing with 20 participants; AI document verification matches manual verification in ≥90% of test cases | N/A | 🟡 Medium | None | TCS-001, TCS-002 | Pass | None | N/A | v1.1 | Added AI document verification scope after UX research — see CHG-001 | Marcus Webb | 2026-02-10 | ✔️ Done |
| FUNC-002 | Functional | The system SHALL send every denied loan applicant an automated FCRA-compliant Adverse Action Notice via email and in-app notification within 3 business days of a credit decision, containing: (a) the top 3 specific reasons for denial, (b) name and contact of the credit bureau used, and (c) the applicant's right to obtain a free credit report within 60 days, SO THAT the company meets FCRA §615(a) requirements for every denied application. | US-002; FCRA §615(a); Legal Review 2026-01-20 | 🔴 Critical | Phase 1 | Fatima Al-Hassan (Compliance) | Adverse action email triggered automatically on 100% of denials in QA test suite of 50 denial scenarios; all 3 FCRA-required elements verified by Legal; delivery within 3 business days confirmed; template approved by external counsel on 2026-02-05 | N/A | 🔴 High | FCRA | TCS-010, TCS-011 | Pass | None | N/A | v1.0 | Initial | Fatima Al-Hassan | 2026-02-10 | ✔️ Done |
| FUNC-003 | Functional | The loan application form SHALL allow applicants to upload supporting documents (government-issued ID, 3 months of pay slips, 3 months of bank statements, utility bill) directly in the browser or mobile app as PDF, JPG, or PNG files up to 10MB each, with automated virus scanning before storage, SO THAT underwriters have all required evidence without requesting documents by post or separate email. | US-001; Underwriter Interviews Jan 2026 | 🟠 High | Phase 1 | Elena Kowalski (Tech Lead) | Upload accepts PDF, JPG, PNG ≤10MB; virus scan (ClamAV) runs on every file before storage; upload confirmation shown to user within 5 seconds; file accessible to underwriter within 60 seconds; tested with 50 document types including edge cases (password-protected PDFs rejected with clear error message) | N/A | 🟢 Low | None | TCS-012, TCS-013 | Pass | None | N/A | v1.0 | Initial | Marcus Webb | 2026-02-10 | ✔️ Done |

### 1B · Non-Functional Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| NFR-001 | Non-Functional | The loan origination system SHALL maintain ≥ 99.95% uptime measured monthly, with a maximum planned maintenance window of 4 hours per month between 02:00–06:00 UTC on Sundays, SO THAT applicants can submit loan applications at any time including UK payday periods (last Friday of each month, when volume spikes 3×). | SLA Policy v2; CRO Mandate 2026-01-10 | 🔴 Critical | Phase 1 | Elena Kowalski + DevOps | Uptime monitoring via Datadog active from Day 1; first 3 monthly SLA reports show ≥99.95%; maintenance windows communicated 72h in advance via status page; load test confirmed system stable at 3× baseline traffic | N/A | 🟡 Medium | SOC2 | TCS-020, TCS-021 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) | 2026-02-10 | ✔️ Done |
| NFR-002 | Non-Functional | All customer PII and financial data SHALL be encrypted at rest using AES-256 and in transit using TLS 1.3 (minimum), with TLS 1.2 and below disabled on all public endpoints, SO THAT customer data is protected against interception and meets GDPR Art. 32 and SOC 2 CC6.7 encryption requirements. | GDPR Art. 32; SOC 2 CC6.7; Security Policy v3 | 🔴 Critical | Phase 1 | Elena Kowalski (Tech Lead) | Encryption verified by CREST pentest firm (Aether Security, report dated 2026-05-20); zero plaintext data exposure in pentest; TLS version confirmed via SSL Labs scan (A+ rating); AES-256 confirmed in infrastructure audit | N/A | 🔴 High | GDPR, SOC2 | TCS-022 | Pass | None | N/A | v1.0 | Initial | Sophie Müller (DPO) | 2026-02-10 | ✔️ Done |

### 1C · AI-Specific Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-001 | AI-Specific | The AI credit scoring model SHALL incorporate alternative data sources — specifically 12 months of open banking transaction history (via FCA-regulated Open Banking API), utility bill payment history (3 years where available), and rental payment history (12 months where available) — in addition to Experian bureau data, SO THAT thin-file applicants who have no traditional credit score are assessed on their actual financial behaviour rather than a data absence. | US-003; Financial Inclusion Strategy 2026; ECOA disparate impact analysis | 🔴 Critical | Phase 1 | Dr. James Okonkwo (AI Lead) | Model uses Open Banking data in ≥ 72% of scored applications; approval rate for thin-file applicants (bureau score absent) is within 8% of bureau-scored applicants at equivalent predicted default rate; confirmed in fairness audit report (FinFair Analytics, 2026-04-15) | Thin-file applicant approval rate within 8% of bureau-scored applicants at equivalent predicted default rate | 🔴 High | ECOA, EU-AI-Act | TCS-030, TCS-031 | Pass | None | N/A | v1.2 | Threshold relaxed from 5% to 8% after actuarial analysis showed 5% was statistically infeasible with current data volume — see CHG-003 | David Chen (CRO) | 2026-04-20 | ✔️ Done |
| AI-002 | AI-Specific | The AI fraud detection model SHALL analyse each loan application in real time using 47 behavioural and identity signals (device fingerprint, typing pattern, IP geolocation, document authenticity score, and 43 Open Banking signals) and generate a fraud risk score (0–100) with a corresponding alert to the fraud team within 30 seconds of application submission for any application scoring ≥ 65, SO THAT fraudulent applications are intercepted before underwriter review or fund disbursement. | US-005; Fraud Risk Policy v2.1; Expected annual fraud losses £2.3M without detection | 🔴 Critical | Phase 1 | Dr. James Okonkwo (AI Lead) | Fraud alerts generated within 30 seconds in 100% of 200 simulated fraud test cases; fraud team receives alert via dashboard, PagerDuty, and email; confirmed in fraud test suite run 2026-05-05; production monitoring shows p99 alert latency = 18 seconds in first 30 days live | Alert latency ≤ 30 seconds for 99% of flagged applications; fraud recall ≥ 85% on historical 5,000-case fraud test set | 🔴 High | EU-AI-Act, NIST-AI-RMF | TCS-032, TCS-033 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) | 2026-02-10 | ✔️ Done |

### 1D · Compliance Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| COMP-001 | Compliance | The system SHALL provide every declined applicant with an FCRA-compliant Adverse Action Notice that includes: (a) the 3 most significant model factors contributing to the decline in plain English (not model variable names), (b) name, address, and phone number of the credit bureau(s) used, and (c) a statement of the applicant's right to obtain a free copy of their credit report within 60 days, SO THAT every denial meets FCRA §615(a) requirements and no applicant is denied without a clear legal explanation. | FCRA §615(a); External Counsel Opinion 2026-01-15 | 🔴 Critical | Phase 1 | Fatima Al-Hassan (Compliance) | Notice template approved by external FCRA counsel (Hawkins & Reid LLP, letter dated 2026-02-05); all 3 required elements present in 100% of denial notices tested in QA; automated delivery within 3 business days confirmed across 50 test scenarios; template reviewed annually | N/A | 🔴 High | FCRA | TCS-010, TCS-040 | Pass | None | N/A | v1.0 | Initial | Fatima Al-Hassan | 2026-02-10 | ✔️ Done |
| COMP-002 | Compliance | The AI credit scoring system SHALL be formally classified as a High-Risk AI System under EU AI Act Annex III Point 5(b) and SHALL meet all requirements of Articles 9–15 before processing any EU applicant. A Conformity Assessment shall be completed and the system registered in the EU AI database before EU market launch, SO THAT the company avoids enforcement action and fines of up to €30M or 6% of global annual turnover. | EU AI Act Annex III; Legal Counsel Opinion 2026-02-01 | 🔴 Critical | Phase 1 | Fatima Al-Hassan + Dr. James Okonkwo | EU AI Act compliance checklist (all 23 items) completed and signed off by DPO and Legal on 2026-05-25; Art. 11 technical documentation package archived at /compliance/eu-ai-act/v1.0/; EU AI database registration confirmed (Registration ID: EU-AI-2026-LP-001); no EU applicants processed before registration | N/A | 🔴 High | EU-AI-Act | TCS-041 | Pass | None | N/A | v1.0 | Initial | Fatima Al-Hassan + Sophie Müller | 2026-02-10 | ✔️ Done |

---

## Phase 2 — Design & Architecture

### 2A · Functional Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-010 | Functional | The mobile loan application UI SHALL display a step-progress indicator (e.g., "Step 3 of 5 — Income Verification") and an AI-generated estimated decision time (updated dynamically based on document upload status and queue length) at every step of the application, SO THAT applicants understand exactly where they are in the process and do not abandon the application due to uncertainty. | US-007; UX Research Jan 2026: 61% of abandoners cited "didn't know how long it would take" | 🟠 High | Phase 2 | UX Lead (Anya Singh) | Progress indicator visible at every step in Figma prototype; estimated time accurate within ±2 minutes in user testing (n=15); drop-off rate in usability testing = 11% (vs. 29% in benchmark without progress indicator); tested on iOS 17 and Android 14 | N/A | 🟢 Low | None | TCS-050 | Pass | None | N/A | v1.0 | Initial | Marcus Webb | 2026-03-25 | ✔️ Done |
| FUNC-011 | Functional | The system SHALL include a human underwriter review queue where all applications meeting any of the following criteria are automatically routed for manual review before a final decision: (a) AI credit scoring model confidence score < 72%, (b) fraud risk score ≥ 65, (c) requested loan amount > £15,000, or (d) any data inconsistency flag triggered, SO THAT the bank maintains meaningful human oversight over all borderline, high-value, and suspicious credit decisions as required by EU AI Act Art. 14. | US-008; EU AI Act Art. 14; FCA PS20/16 | 🔴 Critical | Phase 2 | Marcus Webb (PM) + Elena Kowalski | All 4 routing criteria tested with 200 synthetic test applications; 100% of qualifying applications correctly routed to queue; underwriter can approve, deny, request more info, or escalate; decision logged with underwriter name, action taken, and timestamp; queue accessible on desktop and mobile | N/A | 🔴 High | EU-AI-Act, ECOA | TCS-051, TCS-052 | Pass | None | N/A | v1.1 | Confidence threshold changed from 70% to 72% after calibration on validation set — see CHG-002 | David Chen (CRO) | 2026-03-25 | ✔️ Done |

### 2C · AI-Specific Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-010 | AI-Specific | The AI credit scoring pipeline SHALL use a Gradient Boosted Tree model (XGBoost v2.1) with SHAP (SHapley Additive exPlanations) for individual decision explanation, rather than a neural network or other black-box architecture, SO THAT every credit decision can be explained to the applicant, underwriter, and regulator at the individual level, satisfying EU AI Act Art. 13 and ECOA Regulation B adverse action explanation requirements. | US-002; EU AI Act Art. 13; ECOA Reg. B; CRO Mandate — no black-box credit models | 🔴 Critical | Phase 2 | Dr. James Okonkwo (AI Lead) | Model architecture decision document signed off by CRO (2026-03-20), Legal (2026-03-21), and AI Lead (2026-03-18); XGBoost + SHAP architecture confirmed; per-decision SHAP breakdown available for 100% of scored applications in QA validation | SHAP / feature importance available for 100% of scored applications; SHAP computation time < 200ms per application | 🔴 High | EU-AI-Act, ECOA | TCS-053 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) | 2026-03-25 | ✔️ Done |

### 2D · Compliance Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| COMP-010 | Compliance | A GDPR Data Protection Impact Assessment (DPIA) SHALL be completed using the ICO DPIA template, covering all AI credit scoring and fraud detection processing activities, reviewed by the DPO, and approved before Phase 3 development begins, SO THAT GDPR Art. 35 obligations are met given the high-risk nature of automated credit decision-making affecting individuals' access to credit. | GDPR Art. 35; ICO Guidance on DPIAs; EU AI Act Art. 9 | 🔴 Critical | Phase 2 | Sophie Müller (DPO) | DPIA completed using ICO template (all 9 sections); reviewed and signed by DPO on 2026-03-15; one medium-risk item identified (retention of Open Banking data) — mitigated by 90-day auto-deletion policy added to NFR-002; DPIA archived at /compliance/gdpr/dpia-v1.0.pdf | N/A | 🔴 High | GDPR | TCS-054 | Pass | None | N/A | v1.0 | Initial | Sophie Müller (DPO) | 2026-03-25 | ✔️ Done |

---

## Phase 3 — Development & AI Training

### 3A · Functional Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-020 | Functional | The user authentication module SHALL implement Multi-Factor Authentication (MFA) using TOTP (Google Authenticator or equivalent) as the primary second factor and SMS OTP as a fallback, enforced at every login from a new device or after 30 days of inactivity, and SHALL lock accounts after 5 consecutive failed authentication attempts (with 30-minute lockout and email notification to the account holder), SO THAT unauthorised access to customer financial accounts is prevented even if passwords are compromised. | SOC 2 CC6.1; FCA COBS 2.1; Security Policy v3 | 🔴 Critical | Phase 3 | Backend — Raj Patel | TOTP and SMS OTP both functional across iOS 17, Android 14, Chrome 125, Safari 17; brute-force lockout triggers correctly at 5th failed attempt; lockout email sent within 60 seconds; account unlocks after 30 minutes; tested with 30 edge cases including SIM-swap simulation | N/A | 🔴 High | SOC2 | TCS-060, TCS-061, TCS-062 | Pass | None | N/A | v1.0 | Initial | Elena Kowalski (Tech Lead) | 2026-05-08 | ✔️ Done |
| FUNC-021 | Functional | The loan decision screen SHALL display within 2 seconds of the AI making a decision: (a) the credit decision — Approved, Referred, or Declined, (b) if Approved: the approved loan amount, annual interest rate (APR), monthly repayment amount, and total cost of credit, (c) if Declined: the top 3 reasons for the decline in plain English (not model feature names), SO THAT applicants immediately and clearly understand their outcome and have the information required by ECOA Regulation B and the FCRA adverse action notice requirements. | US-002; ECOA Reg. B; EU AI Act Art. 13; FUNC-011 | 🔴 Critical | Phase 3 | Frontend — Zara Ahmed + Dr. James Okonkwo | Decision screen renders within 2 seconds in all 200 test scenarios; all 3 display elements present; declined reasons plain-English verified by 3 underwriters (100% rated understandable); APR calculation correct in 100% of 50 financial calculation tests | N/A | 🔴 High | EU-AI-Act, ECOA, FCRA | TCS-063, TCS-064 | Pass | None | N/A | v1.0 | Initial | Marcus Webb | 2026-05-08 | ✔️ Done |

### 3C · AI-Specific Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-020 | AI-Specific | The LoanPilot Credit Scoring Model training dataset (600,000 historical UK personal loan applications, 2017–2025) SHALL undergo a formal demographic bias audit by an independent third party (FinFair Analytics Ltd.) before model training begins, confirming: (a) dataset representation within ±5% of UK adult population by gender, age band, and UK region, (b) no proxy variables for protected characteristics (e.g., postcode used as racial proxy), and (c) historical discriminatory lending decisions are identified and corrected via resampling, SO THAT the trained model does not inherit or amplify historical discriminatory lending patterns. | US-003; EU AI Act Art. 10; ECOA; NIST AI RMF GOVERN 6.2; CRO mandate | 🔴 Critical | Phase 3 | Dr. James Okonkwo (AI Lead) + FinFair Analytics | FinFair Analytics bias audit report (dated 2026-04-15) confirms: dataset representation within ±3.8% across all demographic dimensions; 2 proxy variables identified (postcode and mobile phone model) and removed; 12% of historical denial records relabelled via counterfactual fairness correction; report signed off by DPO and CRO on 2026-04-20; archived at /compliance/ai/bias-audit-v1.0.pdf | Demographic representation within ±5% of UK population; 0 proxy variables remaining; corrected dataset used for final model training | 🔴 High | EU-AI-Act, ECOA, NIST-AI-RMF | TCS-070 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) | 2026-04-22 | ✔️ Done |
| AI-021 | AI-Specific | The LoanPilot Credit Scoring Model v1.0 SHALL achieve an AUC-ROC of ≥ 0.85 and a Gini coefficient of ≥ 0.70 on a held-out test set of 60,000 applications (not used in training or validation) before any model version is approved for production, SO THAT only models with statistically proven discriminatory power are used in live credit decisions. | AI Model Performance Policy v1.0; CRO mandate; Basel II/III model governance expectations | 🔴 Critical | Phase 3 | Dr. James Okonkwo (AI Lead) | Model evaluation report (LoanPilot-AI-Eval-v1.0, dated 2026-05-01) shows: AUC-ROC = 0.873; Gini = 0.746; 60,000 held-out test set; report reviewed and signed off by AI Lead (2026-05-02) and CRO (2026-05-03); archived at /compliance/ai/model-eval-v1.0.pdf | AUC-ROC = 0.873 (threshold ≥ 0.85 ✅); Gini = 0.746 (threshold ≥ 0.70 ✅) | 🔴 High | EU-AI-Act | TCS-071 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) | 2026-05-03 | ✔️ Done |
| AI-022 | AI-Specific | The LoanPilot Credit Scoring Model SHALL produce a SHAP feature importance breakdown for every individual credit decision, and the system SHALL automatically map the top 5 SHAP features to plain-English adverse action reason codes (from a pre-approved library of 28 reason codes reviewed by Legal and FCRA counsel), SO THAT every denied applicant automatically receives an accurate, legally compliant, human-readable explanation of their decline without manual underwriter intervention. | US-002; ECOA Reg. B; EU AI Act Art. 13; FCRA §615; Legal Counsel review | 🔴 Critical | Phase 3 | Dr. James Okonkwo + Zara Ahmed | SHAP values generated for 100% of scored applications in QA; top 5 features correctly mapped to reason codes in 100% of 500 test cases; 28 reason codes reviewed and approved by Hawkins & Reid LLP (letter 2026-04-30); underwriter panel (3 underwriters) confirmed explanations accurate in 97.2% of 200 sampled decisions | SHAP explanation available for 100% of decisions; SHAP-to-reason-code mapping accuracy ≥ 95% in human review | 🔴 High | EU-AI-Act, ECOA, FCRA | TCS-072, TCS-073 | Pass | None | N/A | v1.0 | Initial | Fatima Al-Hassan (Legal) | 2026-05-05 | ✔️ Done |
| AI-023 | AI-Specific | The AI fraud detection model SHALL maintain a false positive rate (legitimate applications incorrectly flagged as fraudulent) of ≤ 0.5% overall AND ≤ 0.5% within each demographic group (gender, age band, UK region) tested SO THAT genuine customers of all backgrounds are not disproportionately blocked from accessing credit due to disparate fraud model performance. | US-005; Fraud Policy; ECOA disparate impact; EU AI Act Art. 10 | 🔴 Critical | Phase 3 | Dr. James Okonkwo (AI Lead) | Model evaluation on 80,000 historical applications: overall FPR = 0.42% (✅ ≤ 0.5%); FPR by gender: Male 0.41%, Female 0.44% (✅ within ±0.1%); FPR by age band: 18-25: 0.48%, 26-45: 0.40%, 46-65: 0.39%, 65+: 0.46% (✅ all ≤ 0.5%); report signed off by CRO 2026-05-06 | Overall FPR ≤ 0.5%; FPR within ±0.1% across all demographic groups (no disparate impact) — Result: ✅ All groups pass | 🔴 High | ECOA, EU-AI-Act | TCS-074 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) | 2026-05-06 | ✔️ Done |

---

## Phase 4 — Testing, QA & AI Validation

### 4A · AI-Specific Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-030 | AI-Specific | The LoanPilot Credit Scoring Model SHALL be evaluated by FinFair Analytics Ltd. (independent third party) on a demographically labelled fairness benchmark dataset of 8,000 UK loan applications with known outcomes, confirming that demographic parity difference < 5% across gender, age band (18–25, 26–45, 46–65, 65+), and UK region SO THAT EU AI Act Art. 10 and ECOA fairness obligations are demonstrably met before any live applicant is scored. | EU AI Act Art. 10; ECOA; NIST AI RMF MAP 5.1 | 🔴 Critical | Phase 4 | Dr. James Okonkwo + FinFair Analytics | FinFair Analytics fairness report (dated 2026-05-22): Demographic parity difference — Gender: 0.031 (✅ < 0.05); Age bands: max 0.044 (✅ < 0.05); UK Region: max 0.038 (✅ < 0.05); Report signed off by CRO (2026-05-23), DPO (2026-05-23), AI Lead (2026-05-22); archived as EU AI Act Art. 11 technical documentation | Demographic parity difference ≤ 5% across all protected groups — Result: ✅ All groups pass (max observed: 0.044) | 🔴 High | EU-AI-Act, ECOA, NIST-AI-RMF | TCS-080 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) + Sophie Müller (DPO) | 2026-05-23 | ✔️ Done |
| AI-031 | AI-Specific | The LoanPilot Credit Scoring Model SHALL undergo structured adversarial testing conducted by the internal AI Safety team and 2 external red-teamers (contracted from FinSec Consulting), consisting of 600 crafted test cases covering: model gaming (falsifying income/employment data), bias probing (same financials, different names), data poisoning scenarios, and input manipulation attacks, SO THAT all attack vectors and failure modes are documented and remediating actions taken before any live applicant is scored. | EU AI Act Art. 9; NIST AI RMF MAP 5.1; CRO mandate | 🔴 Critical | Phase 4 | AI Safety Lead (Kenji Tanaka) + FinSec Consulting | Adversarial test report (FinSec Consulting, 2026-05-24): 600 test cases; 2 Critical findings (model gaming via falsified Open Banking data) — both fixed and re-tested (✅ pass); 5 High findings — all resolved; 3 Medium findings — 2 resolved, 1 risk-accepted by CRO (documented); report archived | Model gaming success rate = 0% after fixes; 0 Critical or High findings remaining unresolved | 🔴 High | EU-AI-Act, NIST-AI-RMF | TCS-081 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) | 2026-05-25 | ✔️ Done |
| AI-032 | AI-Specific | The plain-language adverse action explanation system SHALL be validated by an independent panel of 3 qualified underwriters (from LoanPilot's underwriting team, not involved in system development) who each independently review 250 credit decisions and rate the AI-generated explanations on: accuracy (does the reason reflect the actual decision driver?), actionability (can the applicant act on this information?), and clarity (is it free from jargon?), SO THAT the explanation system is legally defensible under ECOA Reg. B and FCRA §615 before launch. | US-002; ECOA Reg. B; EU AI Act Art. 13; FCRA §615 | 🔴 Critical | Phase 4 | Tomás Rivera (QA Lead) | Underwriter panel review complete (2026-05-26): Accuracy: 97.2% rated accurate (✅ ≥ 95%); Actionability: 96.4% rated actionable (✅ ≥ 95%); Clarity: 98.8% rated clear (✅ ≥ 95%); Inter-rater agreement: Cohen's κ = 0.84 (✅ ≥ 0.80); 14 explanations identified as needing improvement — all updated; re-reviewed and confirmed by 2 underwriters | Underwriter accuracy rating ≥ 95%; Cohen's κ ≥ 0.80 — Result: ✅ Accuracy 97.2%; κ = 0.84 | 🔴 High | EU-AI-Act, ECOA, FCRA | TCS-082 | Pass | None | N/A | v1.0 | Initial | Fatima Al-Hassan (Legal) | 2026-05-27 | ✔️ Done |

### 4C · Compliance Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| COMP-030 | Compliance | The GDPR Right to Erasure workflow SHALL delete all PII associated with a customer from all systems — including production database, data warehouse, AI training data pipeline, credit decision audit logs, and backup systems (within the next backup rotation cycle, max 30 days) — within 30 days of a verified deletion request, SO THAT GDPR Art. 17 obligations are met and no deleted customer's data influences future AI model training runs. | GDPR Art. 17; DPO mandate 2026-02-01 | 🔴 Critical | Phase 4 | Engineering (Raj Patel) + DPO | QA test with 10 synthetic customer profiles: all PII deleted from all 7 identified data stores within 30 days (confirmed by DPO audit); training data pipeline purge confirmed by running next training iteration without deleted profiles; deletion audit log maintained (proves deletion without retaining PII); DPO sign-off 2026-05-27 | N/A | 🔴 High | GDPR | TCS-090 | Pass | None | N/A | v1.0 | Initial | Sophie Müller (DPO) | 2026-05-27 | ✔️ Done |
| COMP-031 | Compliance | The EU AI Act technical documentation package (Art. 11) covering the LoanPilot Credit Scoring Model SHALL be completed, reviewed by Legal and the DPO, and archived before the first EU applicant is scored, containing all required elements: general description, intended purpose, development process, training methodology, validation results, risk management measures, and human oversight procedures, SO THAT LoanPilot can demonstrate conformity to EU market surveillance authorities on request. | EU AI Act Art. 11; Legal Counsel Opinion | 🔴 Critical | Phase 4 | Fatima Al-Hassan (Legal) + Dr. James Okonkwo | Art. 11 documentation package (23 sections, 87 pages) completed 2026-05-25; reviewed by Legal (2026-05-26) and DPO (2026-05-27); all 9 required document categories present; archived at /compliance/eu-ai-act/technical-doc-v1.0/; EU AI database registration confirmed (ID: EU-AI-2026-LP-001); signed by AI Lead and Legal on 2026-05-28 | N/A | 🔴 High | EU-AI-Act | TCS-091 | Pass | None | N/A | v1.0 | Initial | Fatima Al-Hassan + Sophie Müller | 2026-05-28 | ✔️ Done |

---

## Phase 5 — Launch & Go-to-Market (First 500 Customers)

### 5C · AI-Specific Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-040 | AI-Specific | The LoanPilot credit scoring system SHALL record an immutable audit log entry in the decision audit database for every credit decision within 5 seconds of the decision being made, containing: (a) model version ID, (b) anonymised applicant reference ID, (c) the 15 most influential input features and their values, (d) raw model output score (0–1000), (e) SHAP explanation JSON, (f) human override flag and underwriter ID (if applicable), and (g) final decision (Approved/Referred/Declined), SO THAT any individual credit decision can be reconstructed and its rationale explained to the applicant or FCA/ICO regulator within 24 hours of request. | US-004; EU AI Act Art. 12; FCRA §607; DPO mandate; FCA PS20/16 | 🔴 Critical | Phase 5 | AI Monitoring Lead (Ben Carter) + Engineering | All 7 fields present in 100% of 1,000 logged decisions in pre-launch testing; log stored in append-only PostgreSQL schema with cryptographic hash chain (each row hashes previous row); reconstruction test passes for 10 sample decisions reviewed by Compliance; active from Day 1 of launch (confirmed by Compliance team) | N/A | 🔴 High | EU-AI-Act, FCRA | TCS-100 | Pass | None | N/A | v1.0 | Initial | Fatima Al-Hassan (Compliance) | 2026-06-01 | ✔️ Done |
| AI-041 | AI-Specific | The LoanPilot AI model monitoring system (built on Evidently AI) SHALL send an automated PagerDuty alert and email to the AI Lead (Dr. James Okonkwo) and CRO (David Chen) within 15 minutes if the rolling 7-day AUC-ROC on live scored applications drops more than 3 percentage points below the launch baseline (0.873), SO THAT model drift is detected promptly and the CRO can invoke the model rollback procedure before a material number of customers are affected by degraded credit decisions. | US-009; NIST AI RMF MEASURE 2.6; AI Monitoring Policy v1.0 | 🔴 Critical | Phase 5 | Ben Carter (AI Monitoring) | Alert fires within 15 minutes in 3 pre-launch synthetic drift simulations (AUC drop of 4pp, 6pp, and 8pp respectively); PagerDuty + email delivery confirmed; false positive rate in first 30 days live = 1.3% (✅ < 5%); monitoring dashboard live at /internal/ai-monitor from Day 1 | Alert latency ≤ 15 min in 3 simulations ✅; false positive rate 1.3% in first 30 days ✅ | 🔴 High | NIST-AI-RMF, EU-AI-Act | TCS-101 | Pass | None | N/A | v1.0 | Initial | David Chen (CRO) | 2026-06-01 | ✔️ Done |

---

## Phase 6 — Post-Launch Iteration

### 6A · Functional Requirements — Iteration

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| FUNC-050 | Functional | Based on analytics showing 34% drop-off at the document upload step and feedback from first 150 customers, the mobile app SHALL be updated to support document upload via smartphone camera with automatic AI-powered OCR extraction of key fields (full name, date of birth, address, employer name, annual income) from: (a) UK driving licence, (b) UK passport, and (c) most recent pay slip, SO THAT applicants can complete the application without scanning documents on a separate device, targeting a reduction in document step drop-off rate from 34% to < 15%. | US-010; User Feedback Batch 1 (Jul 2026); Drop-off analytics report 2026-07-15 | 🟠 High | Phase 6 | PM + Mobile Lead | Camera upload functional on iOS 16+ and Android 13+; OCR accuracy ≥ 90% for all 5 target fields on 50-document test set; document step drop-off rate reduces from 34% to < 15% measured in A/B test over 2 weeks with 200 applicants | N/A | 🟡 Medium | None | TBD | Not Tested | None | N/A | v1.0 | Initial | Marcus Webb | | 🏗️ In Progress |

### 6B · AI-Specific Requirements

| REQ ID | Type | Requirement Statement | Source | Priority | Phase | Owner | Acceptance Criteria | AI Success Metric | AI Risk | Compliance Tag | Linked Test Case ID | Test Result | Defect ID | Retest Status | Req Version | Change Reason | Approved By | Approval Date | Status |
|--------|------|-----------------------|--------|----------|-------|-------|--------------------|--------------------|---------|---------------|--------------------|-----------|-----------|----|---------|--------------|-------------|--------------|--------|
| AI-050 | AI-Specific | After processing 25,000 live loan applications (estimated September 2026), the LoanPilot Credit Scoring Model SHALL be retrained on the updated production dataset, re-evaluated by FinFair Analytics against ALL Phase 4 fairness and performance validation criteria (AI-030: demographic parity, AI-021: AUC-ROC ≥ 0.85, AI-031: adversarial tests, AI-032: explanation accuracy), and formally re-approved by the AI Lead and CRO before the updated model version (v2.0) is deployed to production, SO THAT model quality improves on real UK applicant data without regressing on fairness, accuracy, or robustness. | US-009; NIST AI RMF MANAGE 4.1; Continuous Improvement Policy v1.0; EU AI Act Art. 9 | 🔴 Critical | Phase 6 | Dr. James Okonkwo (AI Lead) | Retrained model v2.0 achieves AUC-ROC ≥ 0.873 (launch baseline); demographic parity difference ≤ 5% for all groups; adversarial test suite re-run (≥ same results); updated model card v2.0 published; CRO and AI Lead sign-off obtained before any production deployment; model version change logged in this RTM Change Log (CHG-XXX) | Retrained model AUC-ROC ≥ v1.0 baseline (0.873); demographic parity ≤ 5%; no regression on any Phase 4 metric | 🔴 High | EU-AI-Act, ECOA, NIST-AI-RMF | TBD | Not Tested | None | N/A | v1.0 | Initial | | | 📝 Draft |

---

# SECTION 7 — First 500 Customers Tracker

## 7.1 · Customer Milestone Tracker (as of 2026-10-14)

| Milestone | Target Date | Actual Date | Customer Count | Key Metric | Status |
|-----------|------------|------------|:--------------:|-----------|:------:|
| First 10 approved loans disbursed | 2026-06-08 | 2026-06-06 | 10 | 0 fraud incidents; 100% adverse action notices sent; avg APR 12.4% | ✅ |
| First 50 customers (onboarding NPS) | 2026-06-30 | 2026-06-27 | 50 | NPS = 47 ✅; Application completion rate = 68% ✅ | ✅ |
| First 100 customers (AI fairness check) | 2026-07-15 | 2026-07-18 | 100 | Dem. parity on live data: 0.034 ✅ (≤ 0.05 threshold); 3-day late | ✅ |
| First 250 customers (30-day repayment) | 2026-08-15 | 2026-08-20 | 250 | Early repayment rate 98.4% vs. 97.1% predicted ✅ (within 3%) | ✅ |
| First 500 customers (milestone) | 2026-09-01 | *In progress* | 387 (as of Oct 14) | NPS = 51; Churn 1.8% ✅; 0 regulatory complaints | 🏗️ On track |

## 7.2 · Live AI Model Performance

| Metric | Launch Baseline (Jun 1) | Oct 14 Value | Target | Drift Alert Threshold | Status |
|--------|:---:|:---:|:------:|:--------------------:|:------:|
| Credit Model AUC-ROC (7-day rolling) | 0.873 | 0.869 | ≥ 0.85 | Drop > 3pp | 🟢 OK |
| Gini Coefficient | 0.746 | 0.738 | ≥ 0.70 | Drop > 4pp | 🟢 OK |
| Demographic Parity Difference (max) | 0.031 | 0.034 | ≤ 0.05 | Rise > 0.02 | 🟢 OK |
| Fraud Model FPR | 0.42% | 0.38% | ≤ 0.5% | Rise > 0.1pp | 🟢 OK |
| Fraud Recall | 87.2% | 89.1% | ≥ 85% | Drop > 5pp | 🟢 OK |
| Credit Scoring Latency (p99) | 2.1s | 2.3s | < 3s | Rise > 0.5s | 🟢 OK |
| Adverse Action Notice Delivery | 100% | 100% | 100% | Any miss | 🟢 OK |
| SHAP Explanation Coverage | 100% | 100% | 100% | Any gap | 🟢 OK |

---

# SECTION 8 — Phase Sign-Off & Approvals

| Phase | Phase Name | Sign-Off By | Role | Initials | Date | Comments |
|:-----:|-----------|------------|------|:--------:|:----:|---------|
| 1 | Discovery & Ideation | David Chen | CRO | DC | 2026-02-12 | All 10 Phase 1 requirements approved. DPIA to begin Phase 2. |
| 2 | Design & Architecture | Sophie Müller | DPO | SM | 2026-03-28 | DPIA completed. Architecture approved. AI model class decision documented. |
| 3 | Development & AI Training | David Chen | CRO | DC | 2026-05-10 | AI models pass all performance and fairness thresholds. Training sign-off granted. |
| 4 | Testing, QA & AI Validation | Fatima Al-Hassan | Legal/Compliance | FAH | 2026-05-28 | All Phase 4 criteria met. EU AI Act Art. 11 documentation archived. Go/No-Go: GO. |
| 5 | Launch & Go-to-Market | Marcus Webb | Product Owner | MW | 2026-06-01 | System launched. All monitoring active. First customers onboarded successfully. |
| 6 | Post-Launch Iteration | — | — | — | — | In progress — Phase 6 Cycle 1 ongoing. |

### AI Credit System Launch Approval Panel — Signed 2026-05-29

| Approver Role | Full Name | Initials | Date | Certification |
|--------------|-----------|:---:|:----:|--------------|
| AI / ML Lead | Dr. James Okonkwo | JO | 2026-05-29 | ✅ Models meet all Phase 4 performance, fairness, and robustness criteria. |
| Chief Risk Officer | David Chen | DC | 2026-05-29 | ✅ AI credit risk within approved limits. Model governance in place. |
| QA Lead | Tomás Rivera | TR | 2026-05-29 | ✅ All test cases passed. 1 medium-risk finding risk-accepted (see COMP-031 notes). |
| Compliance / Legal | Fatima Al-Hassan | FAH | 2026-05-29 | ✅ FCRA, ECOA, GDPR, EU AI Act obligations met. External counsel confirmed. |
| Data Protection Officer | Sophie Müller | SM | 2026-05-29 | ✅ GDPR Art. 35 DPIA complete. EU data residency confirmed. Right-to-erasure tested. |
| CISO | Yuki Tanaka | YT | 2026-05-29 | ✅ Pentest passed (Aether Security, zero Critical/High remaining). SOC 2 controls verified. |
| Product Owner | Marcus Webb | MW | 2026-05-30 | ✅ Product ready for live customers. Business requirements met. LAUNCH APPROVED. |

---

# SECTION 9 — Change Log

| Change ID | Date | REQ ID | Old Version | New Version | What Changed | Reason | Test Cases Affected | Approved By | Date |
|-----------|------|--------|:-----------:|:-----------:|-------------|--------|-------------------|-------------|:----:|
| CHG-001 | 2026-02-20 | FUNC-001 | v1.0 | v1.1 | Added AI-assisted document verification (OCR) to scope of FUNC-001 requirement. Original requirement only covered manual document upload. | User research (Round 2, n=25) showed 78% of users expected automatic document recognition. Competitive analysis confirmed all 3 market leaders offer OCR. | TCS-001 updated to include OCR accuracy test (≥90% on 50-document test set) | Marcus Webb (PM) | 2026-02-22 |
| CHG-002 | 2026-03-22 | FUNC-011 | v1.0 | v1.1 | AI confidence threshold for human review referral changed from < 70% to < 72%. | Model calibration analysis on validation set showed 70% threshold resulted in 31% referral rate (too high for underwriter capacity). 72% reduces referral rate to 18% while maintaining appropriate oversight for genuinely borderline cases. CRO reviewed and approved. | TCS-051 threshold value updated | David Chen (CRO) | 2026-03-25 |
| CHG-003 | 2026-04-18 | AI-001 | v1.1 | v1.2 | Thin-file approval rate parity threshold relaxed from ±5% to ±8% vs. bureau-scored applicants. | Actuarial analysis by FinFair Analytics showed ±5% was statistically infeasible with current thin-file dataset size (n=12,000). ±8% achieves meaningful financial inclusion improvement while remaining statistically valid. DPO and CRO reviewed and approved; documented in fairness audit report. | TCS-030 and TCS-031 thresholds updated | David Chen (CRO) + Sophie Müller (DPO) | 2026-04-20 |

---

# SECTION 10 — Document Control

| Field | Value |
|-------|-------|
| **Document Owner** | Priya Sharma (Project Manager) — with DPO co-ownership for compliance sections |
| **Review Frequency** | End of every phase; after every AI model version update; after any regulatory change |
| **Storage Location** | /docs/compliance/RTM/RTM-LoanPilot-AI-v1.3.md (GitHub main branch, protected) |
| **Access Control** | View: All team members and approved contractors. Edit: PM, AI Lead, Legal. Approve: CRO, DPO. |
| **Related Documents** | Test Plan v2.1 · Credit Risk Register v1.3 · AI Model Card v1.0 · DPIA v1.0 · EU AI Act Technical Documentation v1.0 · Adverse Action Notice Templates · FinFair Analytics Fairness Report · Aether Security Pentest Report · Data Processing Agreement v2.0 |
| **Next Scheduled Review** | 2026-11-01 (post-Phase 6 Cycle 1 completion) |
| **Retention Policy** | Retain for 7 years from the date of the last credit decision made using the model version documented here (FCRA record-keeping and GDPR Art. 5(1)(e) storage limitation). |

---

*LoanPilot AI — SAMPLE Requirements Traceability Matrix*
*⚠️ FICTIONAL SAMPLE — For Training and Template Reference Only*
*Version 1.3 · Last Updated: 2026-10-14*
