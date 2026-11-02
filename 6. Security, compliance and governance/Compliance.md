<!--
TEMPLATE: Compliance.md  | Template version: 1.0.0 | Location: /Security, compliance and governance/Compliance.md
Copy this file into each project. Do not edit the template itself; edit your project's copy.
-->

# HOW TO FILL THIS DOCUMENT (READ FIRST, DELETE THIS BLOCK WHEN DONE)

This file is the single source of truth for a project's compliance posture, from first line of code to its first 500 customers. Follow these steps in order.

1. **Fill every `[FILL: ...]` field.** Replace the whole bracket, including the word FILL. Example: `[FILL: product name]` becomes `Acme Notes`.
2. **Never leave a field blank and never guess.** If you do not know, write `TBD (owner: <name>, due: <YYYY-MM-DD>)`. A blank field is a defect; a `TBD` with an owner is a tracked task.
3. **Use only these status values** in every Status column: `Not started` | `In progress` | `Done` | `N/A (reason)` | `Blocked (reason)`. `N/A` must always include a reason.
4. **Every `Done` needs evidence.** Put a link or file path in the Evidence column (ticket, policy, screenshot, scan report, signed PDF). No evidence means the item is not Done.
5. **Use ISO dates** (`YYYY-MM-DD`) and full names or role titles, never "me" or "the team".
6. **Work phase by phase.** Sections 8 to 12 are gates. You may not start the next phase until the current gate is signed (Section 13).
7. **Keep the Control reference.** The `Ref` column maps each item to a law or standard so auditors can trace it. Do not delete rows; mark them `N/A (reason)`.
8. **Update this file whenever something changes:** new data collected, new vendor, new country, new AI model, new incident. Log the change in Section 16.
9. **Not legal advice.** This template structures your work. Legal and regulated-industry questions must be confirmed by qualified counsel, and regulatory dates and thresholds must be re-verified at time of use.

**Quick example of a correctly filled row**

| ID | Requirement | Owner | Status | Evidence | Due |
|----|-------------|-------|--------|----------|-----|
| P1-03 | Data inventory completed | Jane Doe (Eng Lead) | Done | /docs/data-inventory.xlsx | 2026-11-01 |

---

# AI AGENT RULES (APPLIES TO ANY AI TOOL EDITING THIS FILE)

If you are an AI agent (for example Claude Code) reading or updating this file, you must follow these rules.

- **R1. Never invent facts.** Do not fabricate evidence links, dates, approvals, certifications, vendor names, or legal conclusions. Write `TBD (owner: <name>, due: <date>)` instead.
- **R2. Human-only fields.** Never set or change: Section 13 sign-offs, any `Approved` / `Accepted` value, risk acceptances (Section 15), legal-basis determinations, breach notification decisions, and DPIA/AI-impact conclusions. Propose text and mark `Pending human review`.
- **R3. You may** fill descriptive fields from verified repository facts (stack, dependencies, endpoints, data fields found in schemas), update statuses to `In progress`, and propose `Done` only when real evidence exists.
- **R4. Cite sources.** For every fact you derive from code or config, add the file path or commit in the Evidence column.
- **R5. Do not weaken controls.** Never change a requirement, mark a row `N/A`, or lower a risk rating to make a gate pass. Flag it for a human.
- **R6. Treat secrets as radioactive.** Never write credentials, tokens, personal data, or customer records into this file.
- **R7. Log every edit** in Section 16 with date, "AI agent: <tool/model>", and a one-line summary.
- **R8. If a requirement conflicts with the task you were given, stop and ask a human.**

---

# COMPLIANCE: [FILL: product name]

## 0. Document control

| Field | Value |
|-------|-------|
| Product / project name | [FILL: name] |
| Repository / workspace | [FILL: URL or path] |
| Document owner | [FILL: name, role] |
| Template version | 1.0.0 |
| Document version | [FILL: e.g. 0.1.0] |
| Created | [FILL: YYYY-MM-DD] |
| Last reviewed | [FILL: YYYY-MM-DD] |
| Next review due | [FILL: YYYY-MM-DD] |
| Current lifecycle phase | [FILL: Phase 1 Build / 2 Test / 3 Pre-launch / 4 Launch / 5 First 500] |
| Customers onboarded so far | [FILL: number, target 500] |
| Overall compliance status | [FILL: Red / Amber / Green, with one-sentence reason] |

---

## 1. Product and scope

| Question | Answer |
|----------|--------|
| One-sentence product description | [FILL: what it does and for whom] |
| Customer type | [FILL: consumers / businesses / both / children under 18 possible?] |
| Platforms | [FILL: web / iOS / Android / API / other] |
| Hosting provider(s) and regions | [FILL: e.g. AWS eu-west-1] |
| Countries and regions where customers will be located | [FILL: list; this drives which laws apply] |
| Countries where company and staff operate | [FILL: list] |
| Does the product take payments? | [FILL: Yes / No; processor name] |
| Does the product handle health data? | [FILL: Yes / No] |
| Does the product use AI/ML features? | [FILL: Yes / No; Section 6 is mandatory if Yes] |
| Is any AI used to write code or operate the product? | [FILL: Yes / No; tools named in Section 6.4] |
| Out of scope (explicitly) | [FILL: what this document does not cover and why] |

---

## 2. Roles and accountability

| Role | Name | Contact | Backup | Responsibilities |
|------|------|---------|--------|------------------|
| Product Owner | [FILL] | [FILL] | [FILL] | Accountable for compliance scope, budget, and launch decision |
| Engineering Lead | [FILL] | [FILL] | [FILL] | Implements and evidences technical controls |
| Security / Privacy Officer (DPO if required) | [FILL] | [FILL] | [FILL] | Reviews controls; signs every gate; owns incidents and data subject requests |
| Legal / external counsel | [FILL] | [FILL] | [FILL] | Reviews terms, privacy notice, contracts, regulated-industry obligations |
| AI / ML owner (if AI used) | [FILL] | [FILL] | [FILL] | Model risk, evaluations, AI transparency |

**Escalation path for a compliance problem:** [FILL: who first, who second, maximum response time]

---

## 3. Applicability matrix (what applies to this project)

Mark each row. If `Applies = No`, give the reason. The reason must be factual (e.g. "no EU customers and none planned within 24 months").

| Framework | Applies? (Yes/No/TBD) | Reason | Owner | Ref |
|-----------|-----------------------|--------|-------|-----|
| GDPR / UK GDPR | [FILL] | [FILL] | [FILL] | Reg. (EU) 2016/679 |
| CCPA / CPRA (and other US state privacy laws) | [FILL] | [FILL] | [FILL] | Cal. Civ. Code 1798.100 et seq. |
| Other national privacy laws (India DPDP, Brazil LGPD, etc.) | [FILL] | [FILL] | [FILL] | [FILL: statute] |
| COPPA / children's data rules | [FILL] | [FILL] | [FILL] | 16 CFR Part 312 |
| ePrivacy / cookie and marketing consent | [FILL] | [FILL] | [FILL] | Directive 2002/58/EC; PECR; CAN-SPAM; TCPA |
| SOC 2 (Trust Services Criteria) | [FILL] | [FILL] | [FILL] | AICPA TSC (Security, Availability, Confidentiality, Processing Integrity, Privacy) |
| ISO/IEC 27001 | [FILL] | [FILL] | [FILL] | ISO/IEC 27001:2022, Annex A |
| OWASP ASVS (application security baseline) | [FILL: target level 1/2/3] | [FILL] | [FILL] | OWASP ASVS |
| PCI DSS | [FILL] | [FILL] | [FILL] | PCI DSS v4.0.1 |
| HIPAA | [FILL] | [FILL] | [FILL] | 45 CFR Parts 160, 164 |
| FERPA / education data | [FILL] | [FILL] | [FILL] | 20 U.S.C. 1232g |
| Financial regulation (GLBA, PSD2, AML/KYC, etc.) | [FILL] | [FILL] | [FILL] | [FILL] |
| EU AI Act | [FILL] | [FILL] | [FILL] | Reg. (EU) 2024/1689 |
| NIST AI RMF | [FILL] | [FILL] | [FILL] | NIST AI 100-1 (Govern, Map, Measure, Manage) |
| ISO/IEC 42001 (AI management system) | [FILL] | [FILL] | [FILL] | ISO/IEC 42001:2023 |
| Accessibility | [FILL] | [FILL] | [FILL] | WCAG 2.2 AA; ADA; European Accessibility Act |
| Export controls / sanctions | [FILL] | [FILL] | [FILL] | [FILL] |
| Open-source licence compliance | [FILL] | [FILL] | [FILL] | Licence terms of each dependency |
| Customer contractual requirements | [FILL] | [FILL] | [FILL] | [FILL: contract IDs] |

---

## 4. Data inventory and classification

List every type of data the product collects, stores, or sends. One row per data type. If it is not listed here, the product must not collect it.

**Classification key:** `Public` | `Internal` | `Confidential` | `Restricted` (personal data, secrets, payment, health, children's data).

| Data type | Examples | Class | Purpose | Legal basis (GDPR Art. 6) | Where stored | Retention | Shared with | Encrypted at rest / in transit |
|-----------|----------|-------|---------|---------------------------|--------------|-----------|-------------|-------------------------------|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL: consent / contract / legitimate interest / legal obligation / other] | [FILL] | [FILL: e.g. 24 months after account closure] | [FILL] | [FILL: Yes/Yes] |

**Special-category or high-risk data present?** [FILL: Yes / No; if Yes, list and cite the extra legal basis (GDPR Art. 9), HIPAA safeguards, or COPPA parental consent mechanism]

**Cross-border transfers:**

| From | To | Mechanism | Evidence |
|------|----|-----------|----------|
| [FILL] | [FILL] | [FILL: adequacy decision / SCCs / UK IDTA / DPF certification / not applicable] | [FILL] |

Ref: GDPR Arts. 5, 6, 9, 30, 44 to 49; CCPA 1798.100, 1798.130; SOC 2 P1 to P8, C1.

---

## 5. Core control baseline (all projects)

Status values per instruction 3. Every `Done` needs Evidence.

### 5.1 Governance and policy

| ID | Requirement | Owner | Status | Evidence | Due | Ref |
|----|-------------|-------|--------|----------|-----|-----|
| G-01 | Information security policy approved and communicated | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.5.1; SOC 2 CC1, CC5 |
| G-02 | Privacy policy / privacy notice published and matches Section 4 | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Arts. 12 to 14; CCPA 1798.130 |
| G-03 | Terms of service and acceptable use policy published | [FILL] | [FILL] | [FILL] | [FILL] | Contract law |
| G-04 | Records of processing activities maintained | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 30 |
| G-05 | Staff and contractor confidentiality and security training done | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.6.3; SOC 2 CC1.4 |
| G-06 | Background checks where permitted and relevant | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.6.1 |
| G-07 | DPO appointed or documented decision that one is not required | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Arts. 37 to 39 |
| G-08 | Local representative appointed if required (EU/UK) | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 27 |

### 5.2 Access control and identity

| ID | Requirement | Owner | Status | Evidence | Due | Ref |
|----|-------------|-------|--------|----------|-----|-----|
| A-01 | Multi-factor authentication on all staff, cloud, and source-control accounts | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.5; SOC 2 CC6.1; PCI 8.4 |
| A-02 | Least-privilege roles; access reviewed at least quarterly | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.5.15, A.5.18; SOC 2 CC6.2 to 6.3 |
| A-03 | Joiner / mover / leaver process; access removed within 24 hours of departure | [FILL] | [FILL] | [FILL] | [FILL] | SOC 2 CC6.2 |
| A-04 | No shared accounts; no production access from personal devices without controls | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.1 |
| A-05 | Customer password policy and brute-force protection | [FILL] | [FILL] | [FILL] | [FILL] | OWASP ASVS V2 |

### 5.3 Application and infrastructure security

| ID | Requirement | Owner | Status | Evidence | Due | Ref |
|----|-------------|-------|--------|----------|-----|-----|
| S-01 | Encryption in transit (TLS 1.2 or higher) everywhere | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 32; ISO 27001 A.8.24; PCI 4.2 |
| S-02 | Encryption at rest for all Restricted data; keys managed in a KMS | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 32; PCI 3.5 |
| S-03 | Secrets in a secrets manager; none in code, logs, or this file; secret scanning on | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.4; OWASP ASVS V6 |
| S-04 | Secure development lifecycle: code review required, protected main branch | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.25; SOC 2 CC8.1 |
| S-05 | SAST, dependency (SCA), container, and IaC scanning in CI; findings triaged | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.8, A.8.28 |
| S-06 | Software bill of materials (SBOM) generated per release | [FILL] | [FILL] | [FILL] | [FILL] | Good practice; EO 14028 for US federal supply chain |
| S-07 | Independent penetration test; critical and high findings fixed before launch | [FILL] | [FILL] | [FILL] | [FILL] | SOC 2 CC4.1; PCI 11.4 |
| S-08 | Vulnerability patch SLAs defined (e.g. Critical 7 days, High 30 days) | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.8; PCI 6.3 |
| S-09 | Network segmentation, WAF, rate limiting, DDoS protection | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.20 to 8.23 |
| S-10 | Separate dev / staging / production; no real customer data in non-production | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.31, A.8.33 |
| S-11 | Logging and monitoring with alerting; logs exclude Restricted data; retained [FILL] days | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.15, A.8.16; SOC 2 CC7.2 |
| S-12 | Backups encrypted, restore tested, RPO / RTO defined | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.8.13; SOC 2 A1.2, A1.3 |
| S-13 | Business continuity and disaster recovery plan tested | [FILL] | [FILL] | [FILL] | [FILL] | ISO 27001 A.5.29, A.5.30 |
| S-14 | OWASP ASVS target level achieved for web and API | [FILL] | [FILL] | [FILL] | [FILL] | OWASP ASVS |
| S-15 | Secure data deletion on retention expiry and on request | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Arts. 5(1)(e), 17; ISO 27001 A.8.10 |
| S-16 | Accessibility conformance (WCAG 2.2 AA) audited | [FILL] | [FILL] | [FILL] | [FILL] | WCAG 2.2; ADA; EAA |

### 5.4 Privacy engineering

| ID | Requirement | Owner | Status | Evidence | Due | Ref |
|----|-------------|-------|--------|----------|-----|-----|
| PV-01 | Data minimisation reviewed: every field has a purpose in Section 4 | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 5(1)(c), Art. 25 |
| PV-02 | Privacy by default settings (least-invasive option preselected) | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 25(2) |
| PV-03 | Consent captured, versioned, provable, and withdrawable as easily as given | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Arts. 7, 8; ePrivacy |
| PV-04 | Cookie / SDK consent banner; no non-essential trackers before consent | [FILL] | [FILL] | [FILL] | [FILL] | ePrivacy Art. 5(3) |
| PV-05 | Data protection impact assessment (DPIA) done where high risk | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 35 |
| PV-06 | Do Not Sell / Share and Limit Sensitive Data signals honoured (incl. Global Privacy Control) | [FILL] | [FILL] | [FILL] | [FILL] | CCPA 1798.120, 1798.121, 1798.135 |
| PV-07 | Age gate and parental consent flow if children can use the product | [FILL] | [FILL] | [FILL] | [FILL] | COPPA; GDPR Art. 8 |
| PV-08 | Analytics, crash, and advertising SDKs reviewed for data leakage | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 25, 28 |

### 5.5 Third parties and vendors

| Vendor | Service | Data shared | DPA / BAA signed? | Security evidence (SOC 2 / ISO cert) | Region | Sub-processors reviewed | Review date | Owner |
|--------|---------|-------------|-------------------|--------------------------------------|--------|------------------------|-------------|-------|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

Ref: GDPR Art. 28; HIPAA 164.308(b) (Business Associate Agreement); SOC 2 CC9.2; ISO 27001 A.5.19 to 5.22.

### 5.6 Open-source and licensing

| ID | Requirement | Owner | Status | Evidence | Due |
|----|-------------|-------|--------|----------|-----|
| L-01 | Licence inventory of all dependencies; no incompatible copyleft in distributed code | [FILL] | [FILL] | [FILL] | [FILL] |
| L-02 | Third-party content, fonts, images, datasets, and model weights have verified rights | [FILL] | [FILL] | [FILL] | [FILL] |
| L-03 | Attribution notices shipped where required | [FILL] | [FILL] | [FILL] | [FILL] |

---

## 6. AI governance (mandatory if the product uses AI/ML or AI-assisted development; otherwise write `N/A (no AI used, confirmed by <name> on <date>)`)

### 6.1 AI system register

| System | Purpose | Model / vendor | Version | Trained or fine-tuned on | Input data | Output used for | Human oversight | Risk tier (Section 6.2) |
|--------|---------|----------------|---------|--------------------------|------------|-----------------|-----------------|--------------------------|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

### 6.2 Risk classification (EU AI Act logic; apply even outside the EU as best practice)

| Question | Answer | Consequence |
|----------|--------|-------------|
| Does any feature fall under a prohibited practice (e.g. social scoring, manipulative techniques, untargeted facial-image scraping, emotion inference in workplace or school)? | [FILL] | If Yes: stop. Do not build or launch. Escalate to counsel. (Art. 5) |
| Is it a high-risk use (e.g. hiring, credit, education scoring, essential services, biometric identification, safety component)? | [FILL] | If Yes: conformity obligations apply (risk management, data governance, logging, human oversight, accuracy and robustness, technical documentation). (Arts. 6 to 15, Annex III) |
| Does it interact directly with people, generate synthetic content, or recognise emotions? | [FILL] | Transparency duties: disclose AI interaction and label synthetic content. (Art. 50) |
| Is a general-purpose AI model built or fine-tuned by us, or only used via API? | [FILL] | Provider vs deployer duties differ. (Arts. 53 to 55) |
| Final tier | [FILL: Prohibited / High-risk / Limited-risk / Minimal-risk] | [FILL] |

Dates and obligations under the EU AI Act phase in over several years and have been subject to amendment proposals. Counsel must confirm the dates in force when you use this template. [FILL: date verified and by whom]

### 6.3 AI control checklist

| ID | Requirement | Owner | Status | Evidence | Due | Ref |
|----|-------------|-------|--------|----------|-----|-----|
| AI-01 | AI use policy approved (allowed tools, forbidden data, review rules) | [FILL] | [FILL] | [FILL] | [FILL] | ISO 42001 5.2; NIST Govern |
| AI-02 | Intended purpose and known limitations documented (model card / system card) | [FILL] | [FILL] | [FILL] | [FILL] | NIST Map; EU AI Act Art. 11, 13 |
| AI-03 | Training / fine-tuning / retrieval data provenance, consent, and licence verified | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 5, 6; EU AI Act Art. 10 |
| AI-04 | Customer data is not used to train third-party models unless contractually and legally permitted | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 5(1)(b); vendor terms |
| AI-05 | Evaluation suite for accuracy, bias, toxicity, hallucination, and robustness; pass thresholds defined | [FILL] | [FILL] | [FILL] | [FILL] | NIST Measure; EU AI Act Art. 15 |
| AI-06 | Red-teaming, prompt-injection, jailbreak, data-exfiltration, and tool-abuse testing done | [FILL] | [FILL] | [FILL] | [FILL] | OWASP Top 10 for LLM Applications |
| AI-07 | Human oversight and override defined; no solely automated significant decisions without legal basis | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 22; EU AI Act Art. 14 |
| AI-08 | Users told when they interact with AI; synthetic content labelled | [FILL] | [FILL] | [FILL] | [FILL] | EU AI Act Art. 50 |
| AI-09 | AI inputs and outputs logged with privacy safeguards; retention set | [FILL] | [FILL] | [FILL] | [FILL] | EU AI Act Art. 12; GDPR Art. 5 |
| AI-10 | Agent permissions are least-privilege; destructive and financial actions need human approval | [FILL] | [FILL] | [FILL] | [FILL] | NIST Manage; SOC 2 CC6 |
| AI-11 | Model, prompt, and guardrail changes go through change control and re-evaluation | [FILL] | [FILL] | [FILL] | [FILL] | ISO 42001 8; SOC 2 CC8 |
| AI-12 | AI incident process (harmful output, leak, bias complaint) with owner and SLA | [FILL] | [FILL] | [FILL] | [FILL] | NIST Manage; EU AI Act Art. 73 |
| AI-13 | Cost, rate-limit, and abuse controls on AI endpoints | [FILL] | [FILL] | [FILL] | [FILL] | OWASP LLM10 |
| AI-14 | Vendor AI terms reviewed (data retention, training use, region, sub-processors) | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 28 |

### 6.4 AI-assisted development controls

| ID | Requirement | Owner | Status | Evidence | Due |
|----|-------------|-------|--------|----------|-----|
| AD-01 | Approved AI coding tools list: [FILL: tools, versions, account type] | [FILL] | [FILL] | [FILL] | [FILL] |
| AD-02 | No secrets, personal data, or customer data pasted into AI tools unless the tool is approved for it | [FILL] | [FILL] | [FILL] | [FILL] |
| AD-03 | All AI-generated code passes the same review, tests, SAST, SCA, and licence checks as human code | [FILL] | [FILL] | [FILL] | [FILL] |
| AD-04 | AI agent credentials are scoped, short-lived, and cannot access production data or deploy without approval | [FILL] | [FILL] | [FILL] | [FILL] |
| AD-05 | Commits made by AI agents are identifiable (commit trailer or bot account) | [FILL] | [FILL] | [FILL] | [FILL] |
| AD-06 | Dependencies suggested by AI are verified to exist and be legitimate (guard against hallucinated or typosquatted packages) | [FILL] | [FILL] | [FILL] | [FILL] |

---

## 7. Data subject rights and customer requests

| Right | Where in product / process | SLA | Owner | Tested on | Evidence | Ref |
|-------|----------------------------|-----|-------|-----------|----------|-----|
| Access / know | [FILL] | [FILL: GDPR 1 month; CCPA 45 days] | [FILL] | [FILL] | [FILL] | GDPR Art. 15; CCPA 1798.110 |
| Rectification / correct | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 16; CCPA 1798.106 |
| Erasure / delete | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 17; CCPA 1798.105 |
| Restriction and objection | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Arts. 18, 21 |
| Portability | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 20 |
| Opt-out of sale / sharing / targeted ads | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | CCPA 1798.120 |
| Withdraw consent | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 7(3) |
| Challenge automated decisions | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | GDPR Art. 22 |

Identity verification method for requests: [FILL]. Request log location: [FILL].

---

## 8. Incident and breach response

| Item | Answer | Ref |
|------|--------|-----|
| Incident response plan location | [FILL] | ISO 27001 A.5.24 to 5.28; SOC 2 CC7.3 to 7.5 |
| Severity levels and response times | [FILL: e.g. SEV1 acknowledged in 15 min] | |
| 24/7 on-call contact | [FILL] | |
| Regulator notification deadline(s) that apply | [FILL: GDPR 72 hours to authority from awareness; HIPAA up to 60 days to individuals; US state laws vary; PCI per card brand] | GDPR Arts. 33, 34; HIPAA 164.400 to 414 |
| Customer notification template location | [FILL] | |
| Who decides whether a breach is notifiable | [FILL: name, role; human decision only] | |
| Last tabletop exercise date | [FILL] | SOC 2 CC7.4 |
| Post-incident review required within | [FILL: e.g. 5 business days] | |

**Incident register:**

| Date | ID | Severity | Summary | Data affected | Notified whom / when | Root cause | Fix | Status |
|------|----|----------|---------|---------------|----------------------|------------|-----|--------|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

---

# LIFECYCLE GATES (development to first 500 customers)

Each phase has a checklist and a gate. Items marked **MUST** block the gate. Items marked **SHOULD** need either completion or a documented exception in Section 15.

## 9. PHASE 1: BUILD (planning, design, development)

| ID | Item | Level | Owner | Status | Evidence | Due |
|----|------|-------|-------|--------|----------|-----|
| P1-01 | Sections 0 to 4 completed | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-02 | Applicability matrix (Section 3) approved by Security/Privacy Officer and Legal | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-03 | Data inventory complete; legal basis recorded for each data type | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-04 | Threat model completed (STRIDE or equivalent) for core flows | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-05 | DPIA / AI impact assessment started if high risk | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-06 | AI risk tier set (Section 6.2) | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-07 | Secure-by-default architecture reviewed; authentication and authorisation design approved | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-08 | CI pipeline has SAST, SCA, secret scanning, branch protection (S-03 to S-05) | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-09 | Vendors shortlisted with DPA and security evidence requested (Section 5.5) | SHOULD | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-10 | AI-assisted development controls active (Section 6.4) | MUST if AI used | [FILL] | [FILL] | [FILL] | [FILL] |
| P1-11 | Draft privacy notice, terms, and cookie plan prepared | SHOULD | [FILL] | [FILL] | [FILL] | [FILL] |

**Gate 1 exit criteria:** every MUST is Done with evidence; no open Critical risk in Section 15.

## 10. PHASE 2: TEST (verification and hardening)

| ID | Item | Level | Owner | Status | Evidence | Due |
|----|------|-------|-------|--------|----------|-----|
| P2-01 | Security test results: SAST, SCA, DAST clean of Critical/High, or exceptions logged | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-02 | Penetration test completed; Critical/High remediated and retested | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-03 | Privacy test: consent flows, cookie blocking, deletion, export, and opt-out verified end-to-end | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-04 | No real personal data in test environments (S-10) | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-05 | AI evaluation results meet thresholds (AI-05, AI-06) | MUST if AI used | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-06 | Backup restore and failover test executed (S-12, S-13) | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-07 | Accessibility audit done (S-16) | SHOULD | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-08 | SBOM and licence scan clean (S-06, L-01) | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-09 | DPIA / AI impact assessment completed and approved by humans | MUST if required | [FILL] | [FILL] | [FILL] | [FILL] |
| P2-10 | Logging and alerting verified with a simulated incident | MUST | [FILL] | [FILL] | [FILL] | [FILL] |

**Gate 2 exit criteria:** every MUST Done; test reports attached in Section 14.

## 11. PHASE 3: PRE-LAUNCH (readiness)

| ID | Item | Level | Owner | Status | Evidence | Due |
|----|------|-------|-------|--------|----------|-----|
| P3-01 | Privacy notice, terms, cookie policy, and AI disclosures published and match the real product | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-02 | All vendors in Section 5.5 have signed DPA/BAA and approved security review | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-03 | Production secrets rotated; no test credentials remain | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-04 | Incident response plan, on-call rota, and customer notice templates ready (Section 8) | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-05 | Data subject request process tested with a dry run (Section 7) | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-06 | Support team trained on privacy requests, security reports, and escalation | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-07 | Vulnerability disclosure contact published (security.txt or equivalent) | SHOULD | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-08 | Payment compliance validated (PCI SAQ type [FILL] completed) if payments | MUST if payments | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-09 | Regulated-industry requirements closed (HIPAA risk analysis, COPPA mechanism, financial licences) | MUST if applicable | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-10 | Open exceptions and risks reviewed; no Critical or High unaccepted | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-11 | Rollback plan and kill switch (including for AI features) tested | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P3-12 | Marketing claims reviewed (no false "secure", "compliant", "certified", or "AI-powered" claims) | MUST | [FILL] | [FILL] | [FILL] | [FILL] |

**Gate 3 exit criteria (LAUNCH DECISION):** every MUST Done, with all four sign-offs in Section 13.

## 12. PHASE 4: LAUNCH (go-live to customer 50) and PHASE 5: FIRST 500 CUSTOMERS

### 12.1 Phase 4: launch window (customers 1 to 50)

| ID | Item | Level | Owner | Status | Evidence | Due |
|----|------|-------|-------|--------|----------|-----|
| P4-01 | Staged rollout (beta, allow-list, or percentage ramp) with named cohorts | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P4-02 | Daily review of security alerts, error logs, and abuse reports for the first 14 days | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P4-03 | Verify real production data flows match the data inventory (Section 4); update if drift | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P4-04 | First privacy request and first support security report handled within SLA | MUST | [FILL] | [FILL] | [FILL] | [FILL] |
| P4-05 | AI output sampling by humans (sample size [FILL]) and complaint triage | MUST if AI used | [FILL] | [FILL] | [FILL] | [FILL] |
| P4-06 | Consent records and cookie behaviour spot-checked in production | MUST | [FILL] | [FILL] | [FILL] | [FILL] |

### 12.2 Phase 5: growth to 500 customers

Track by milestone. Complete the reviews when the customer count crosses each threshold, or on the date shown, whichever comes first.

| Milestone | Required review | Owner | Date done | Evidence | Result |
|-----------|-----------------|-------|-----------|----------|--------|
| 50 customers | Gate 4 review: launch-window findings closed; updated risk register | [FILL] | [FILL] | [FILL] | [FILL] |
| 100 customers | Access review (A-02), vendor list review, DSR log review, patch SLA audit | [FILL] | [FILL] | [FILL] | [FILL] |
| 250 customers | Re-run key tests: dependency scan, restore test, consent test, AI evaluation. Reassess whether SOC 2 / ISO 27001 readiness work should begin | [FILL] | [FILL] | [FILL] | [FILL] |
| 500 customers | Gate 5 review: full recheck of Sections 3 to 8, retest of Critical controls, lessons learned, decision on certification and next-stage roadmap | [FILL] | [FILL] | [FILL] | [FILL] |

**Ongoing monthly review (every month until customer 500, then per Section 16 cadence):**

| Check | Done? | Evidence |
|-------|-------|----------|
| New data fields collected since last month? Section 4 updated | [FILL] | [FILL] |
| New vendors, regions, or sub-processors? Section 5.5 updated | [FILL] | [FILL] |
| New or changed AI models, prompts, or tools? Section 6 updated and re-evaluated | [FILL] | [FILL] |
| Open vulnerabilities past SLA | [FILL: number] | [FILL] |
| Security incidents or near misses | [FILL: number] | [FILL] |
| Privacy requests received / closed within SLA | [FILL: n / n] | [FILL] |
| Customer complaints about privacy, security, or AI | [FILL: number] | [FILL] |
| Changes to laws or contracts affecting the product | [FILL] | [FILL] |

**Compliance metrics to track:**

| Metric | Target | Current | Date |
|--------|--------|---------|------|
| Critical vulnerabilities open > 7 days | 0 | [FILL] | [FILL] |
| High vulnerabilities open > 30 days | 0 | [FILL] | [FILL] |
| Privacy requests closed within legal deadline | 100% | [FILL] | [FILL] |
| Staff with completed security training | 100% | [FILL] | [FILL] |
| MFA coverage on staff accounts | 100% | [FILL] | [FILL] |
| Mean time to acknowledge SEV1 | [FILL] | [FILL] | [FILL] |
| AI outputs flagged as harmful or wrong per 1,000 | [FILL] | [FILL] | [FILL] |

---

## 13. Gate sign-offs (HUMANS ONLY; AI agents must never fill this section)

A signature means: "I reviewed the evidence, not just the checkboxes."

| Gate | Product Owner | Engineering Lead | Security / Privacy Officer | Legal / counsel | Decision (Pass / Pass with exceptions / Fail) | Date |
|------|---------------|------------------|----------------------------|-----------------|-----------------------------------------------|------|
| Gate 1: Build complete | [FILL: name, date] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Gate 2: Test complete | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Gate 3: Launch approved | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Gate 4: 50-customer review | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Gate 5: 500-customer review | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

---

## 14. Evidence register

Every Evidence link used above must also appear here, so auditors find everything in one place.

| Evidence ID | Title | Type (policy / report / screenshot / contract / log) | Location (link or path) | Created | Owner | Contains personal data? | Retention |
|-------------|-------|------------------------------------------------------|-------------------------|---------|-------|-------------------------|-----------|
| E-001 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL: Yes/No] | [FILL] |

---

## 15. Risk register and exceptions

**Risk rating:** Likelihood (1 to 5) x Impact (1 to 5). 1 to 6 = Low, 7 to 12 = Medium, 13 to 19 = High, 20 to 25 = Critical. A Critical risk blocks any gate. High needs a written mitigation plan.

| Risk ID | Description | Likelihood | Impact | Score | Level | Mitigation | Owner | Due | Status | Accepted by (human) |
|---------|-------------|------------|--------|-------|-------|------------|-------|-----|--------|---------------------|
| R-001 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

**Exceptions (a control not met, with approval):**

| Exception ID | Control ID | Reason | Compensating control | Approved by | Expires | Status |
|--------------|-----------|--------|----------------------|-------------|---------|--------|
| X-001 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL: max 90 days] | [FILL] |

Seed risks to consider (delete those that do not apply, never delete without a reason): customer data leak via misconfigured storage; prompt injection leading to data exfiltration; vendor breach; unlawful transfer of EU data; consent records missing; model producing harmful or biased output; AI agent taking destructive action; secrets committed to repository; hallucinated dependency introduced; unable to meet DSR deadline; key person unavailable; claim of certification not yet held.

---

## 16. Review cadence and change log

| Cadence | What |
|---------|------|
| Monthly until customer 500 | Section 12.2 monthly review |
| Quarterly | Access review, vendor review, risk register, applicability matrix, policy review |
| Annually | Full document review, penetration test, tabletop exercise, training refresh, DPIA refresh |
| On trigger (within 10 business days) | New country, new data type, new vendor, new AI model or use, security incident, law change, merger, major release |

**Change log:**

| Date | Version | Author (human, or "AI agent: tool/model") | Section(s) | Summary of change | Reviewed by |
|------|---------|-------------------------------------------|------------|-------------------|-------------|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

---

## 17. Glossary

| Term | Plain meaning |
|------|---------------|
| Personal data | Any information about an identifiable person (name, email, IP address, device ID, photo, voice) |
| Special-category data | Extra-sensitive personal data: health, biometrics, religion, ethnicity, sexual orientation, political views, union membership |
| Controller / Processor | Controller decides why and how data is used. Processor handles it on the controller's behalf (for example your cloud host) |
| DPA | Data Processing Agreement, the contract between controller and processor |
| BAA | Business Associate Agreement, the HIPAA equivalent of a DPA |
| DPIA | Data Protection Impact Assessment, a written risk review required for high-risk processing |
| DPO | Data Protection Officer |
| DSR / DSAR | Data subject (access) request: a person asking to see, fix, delete, or move their data |
| SCCs | Standard Contractual Clauses, a legal tool for transferring EU data abroad |
| SOC 2 | An independent audit report on a company's security and privacy controls |
| ISO 27001 | International certification standard for an information security management system |
| ASVS | OWASP Application Security Verification Standard, a checklist for secure applications |
| SAST / SCA / DAST | Code scanning / dependency scanning / running-app scanning |
| SBOM | Software Bill of Materials, an ingredient list of all software components |
| MFA | Multi-factor authentication |
| KMS | Key Management Service, a secure store for encryption keys |
| RPO / RTO | Maximum tolerable data loss / maximum tolerable downtime |
| High-risk AI | AI uses the EU AI Act regulates most strictly (hiring, credit, education, and similar) |
| Prompt injection | An attack where hidden instructions in input make an AI do something unintended |
| Human in the loop | A person reviews or approves the AI's output before it takes effect |
| Gate | A checkpoint you cannot pass until required items are Done and signed |
| Evidence | Proof that a control exists and works: a link, file, screenshot, or report |

---

## 18. Pre-handoff self-check (complete before declaring this document ready)

- [ ] No `[FILL: ...]` remains anywhere in the file
- [ ] No row is blank; every unknown has a `TBD (owner, due)`
- [ ] Every `Done` has an evidence link, and it is listed in Section 14
- [ ] Every `N/A` has a reason
- [ ] Section 3 matches the countries and data in Sections 1 and 4
- [ ] Privacy notice matches Section 4 exactly
- [ ] Section 13 was signed by humans only
- [ ] No secrets or personal data exist in this file
- [ ] Next review date is set in Section 0
