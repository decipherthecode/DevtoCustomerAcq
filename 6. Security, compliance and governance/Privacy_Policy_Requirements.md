# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

This is a **reusable template**. Copy it for every new project, rename it, and fill it in from top to bottom. You do not need to be a lawyer. If you can read and answer simple questions, you can fill this in.

## The 7 Simple Rules

1. **Work top to bottom.** Sections are in the order you will need them (Idea → Build → Pre-launch → First 500 customers).
2. **Replace every `[TBD]`** with your answer. Nothing should say `[TBD]` when you finish.
3. **Read the hint, then the example, then answer.** Every section has a `Hint` (what it means in plain words) and an `Example` (what a good answer looks like).
4. **Tick boxes like this:** change `[ ]` to `[x]`.
5. **Only three answers are allowed in Yes/No cells:** `Yes`, `No`, or `N/A` (not applicable). If `N/A`, write one short reason. Never leave a cell empty.
6. **If you do not know, do not guess.** Write `UNKNOWN - ask [name] by [date]` and add it to Section 19 (Open Questions). A guess in a privacy document can become a legal problem.
7. **Get it signed.** The document is not "done" until Section 1.4 (Sign-off) is complete.

## Words you will see (full list in the Glossary, Section 23)

| Word | Plain meaning |
|---|---|
| Personal data | Any information that can identify a person, directly or when combined with other info (name, email, phone, IP address, device ID, photo, location). |
| Processing | Anything you do with data: collect, store, read, share, delete. |
| Data subject / user | The person the data is about. |
| Controller / Business / Data Fiduciary | The company that decides *why* and *how* data is used (usually you). |
| Processor / Service Provider | A company that handles data *for* you (hosting, email service, analytics). |
| DPIA | Data Protection Impact Assessment. A written risk check done *before* risky data use. |
| DPA | Data Processing Agreement. The contract with a processor. |

## Status Tags (use in the "Status" columns)

| Tag | Meaning |
|---|---|
| `NOT STARTED` | Nobody has begun. |
| `IN PROGRESS` | Someone is working on it. |
| `DONE` | Finished, and proof (evidence) is attached or linked. |
| `BLOCKED` | Waiting on someone. Say who. |
| `N/A` | Does not apply. Say why. |

## Requirement Priority Tags

| Tag | Meaning |
|---|---|
| **MUST** | Required. You cannot launch without it. |
| **SHOULD** | Strongly recommended. Skipping needs written approval from the Privacy Lead. |
| **MAY** | Optional or nice to have. |

## The 4 Lifecycle Gates

The document follows the product's life. At each **Gate**, you stop and check that required items are `DONE` before moving on.

| Gate | Stage | Question it answers | Sections |
|---|---|---|---|
| **G1** | Idea, Discovery and Design | "What data will we touch, and is it allowed?" | 2 to 6 |
| **G2** | Build and Test (including AI agents) | "Are we building it safely, and are our AI tools safe?" | 7 to 14 |
| **G3** | Pre-launch / Beta | "Is everything public, signed, tested and ready?" | 15 to 18, 20 |
| **G4** | Launch to First 500 Customers | "Are we watching, responding and improving?" | 17, 22 |

## Where to Save and How to Name

- Save in the folder: `Security, Compliance and Governance`.
- File name for each project: `Privacy_Policy_Requirements_[ProjectName]_v[Version].md` (example: `Privacy_Policy_Requirements_PlantPal_v1.0.md`).
- Keep the blank master template untouched. Always copy it first.

## Important Disclaimer

This template is a **working framework, not legal advice**. Laws change. The law summaries in Section 3 and Appendix B are simplified defaults and were written to be checked, not trusted blindly. Before launch, a qualified lawyer or Data Protection Officer (DPO) should review the completed document, especially if you handle children's, health or financial data.

---

# PRIVACY POLICY REQUIREMENTS

> Template version: **1.0** | Folder: Security, Compliance and Governance | Scope: AI-Driven Development Life Cycle, from first idea to the first 500 customers

---

## 1. Document Control

### 1.1 Project Identity

> **Hint:** This tells everyone which product this document is about. **Example:** Project name: `PlantPal`; Product type: `Mobile app + web dashboard`.

| Field | Your Answer |
|---|---|
| Project name | [TBD] |
| One-sentence description (what it does, for whom) | [TBD] |
| Product type (tick all) | [ ] Web app/SaaS  [ ] iOS app  [ ] Android app  [ ] Other: [TBD] |
| Company / legal entity name | [TBD] |
| Company registered address | [TBD] |
| Planned launch date | [TBD] (DD-MMM-YYYY) |
| Document version | 0.1 |
| Document status | [ ] Draft  [ ] In review  [ ] Approved  [ ] Superseded |
| Date created / Last updated | [TBD] / [TBD] |
| Link to product repo / project board | [TBD] |

### 1.2 Roles and Owners

> **Hint:** Every requirement needs a named human owner. A team name is not enough. If one person has two roles, write the name twice. **Example:** Product Owner: `Asha Rao, asha@plantpal.example`.

| Role | What this person does | Name | Email | Backup person |
|---|---|---|---|---|
| Product Owner / Founder | Final accountable owner; approves launch | [TBD] | [TBD] | [TBD] |
| Engineering Lead | Answers technical questions; builds controls | [TBD] | [TBD] | [TBD] |
| Privacy Lead / DPO (may be external) | Reviews legal basis, DPIA, policy text | [TBD] | [TBD] | [TBD] |
| QA / Security Lead | Verifies controls; collects test proof | [TBD] | [TBD] | [TBD] |
| Customer Support Lead | Receives user privacy requests | [TBD] | [TBD] | [TBD] |

Privacy contact shown publicly (must be a monitored inbox, e.g. `privacy@yourcompany.com`): [TBD]

Is a formal DPO legally required? [ ] Yes [ ] No [ ] UNKNOWN. *(Hint: usually required only for large-scale monitoring or large-scale sensitive data. Ask your lawyer.)*

EU/UK representative needed (if you have EU/UK users but no office there)? [ ] Yes: [TBD] [ ] No [ ] N/A

### 1.3 Related Documents

| Document | Link / Location | Status |
|---|---|---|
| Security requirements | [TBD] | [TBD] |
| Terms of Service | [TBD] | [TBD] |
| Cookie Policy | [TBD] | [TBD] |
| Incident Response Plan | [TBD] | [TBD] |
| Data Retention Schedule | [TBD] | [TBD] |
| DPIA report(s) | [TBD] | [TBD] |

### 1.4 Sign-off (complete at each Gate)

> **Hint:** Signing means "I read this and the items for this Gate are true." Type full name and date. **Example:** `Asha Rao, 14-Mar-2027`.

| Gate | Product Owner | Engineering Lead | Privacy Lead / DPO | QA / Security Lead |
|---|---|---|---|---|
| G1 Design | [TBD] / [date] | [TBD] / [date] | [TBD] / [date] | [TBD] / [date] |
| G2 Build | [TBD] / [date] | [TBD] / [date] | [TBD] / [date] | [TBD] / [date] |
| G3 Pre-launch | [TBD] / [date] | [TBD] / [date] | [TBD] / [date] | [TBD] / [date] |
| G4 First 500 review | [TBD] / [date] | [TBD] / [date] | [TBD] / [date] | [TBD] / [date] |

---

# GATE G1: IDEA, DISCOVERY AND DESIGN

## 2. Project Snapshot (Quick Facts)

> **Hint:** Answer fast. These answers decide which later sections matter for you.

| # | Question | Yes / No / N/A | Notes |
|---|---|---|---|
| 2.1 | Will users create accounts or log in? | [TBD] | |
| 2.2 | Will we collect names, emails or phone numbers? | [TBD] | |
| 2.3 | Will we collect location (precise GPS or approximate)? | [TBD] | |
| 2.4 | Will we collect photos, audio, video or files from users? | [TBD] | |
| 2.5 | Will we take payments or store payment details? | [TBD] | |
| 2.6 | Could children under 18 use the product? | [TBD] | |
| 2.7 | Will we handle health or medical information? | [TBD] | |
| 2.8 | Will we handle financial account information? | [TBD] | |
| 2.9 | Will we use analytics, ads, cookies or tracking SDKs? | [TBD] | |
| 2.10 | Will data be sent to outside companies (vendors)? | [TBD] | |
| 2.11 | Will data be stored or accessed outside the user's country? | [TBD] | |
| 2.12 | Will AI coding assistants or agents touch our code, data or tickets? | [TBD] | |
| 2.13 | Will the product itself use AI that sees user data? | [TBD] | |
| 2.14 | Will we make automatic decisions about users (e.g. approve/deny)? | [TBD] | |
| 2.15 | Will we sell, rent or share personal data for advertising? | [TBD] | |

**How to read your answers:**
- Any **Yes** on 2.6, 2.7 or 2.8 means **Section 5 (Special Data) is required**.
- Any **Yes** on 2.3, 2.4, 2.6, 2.7, 2.8, 2.13, 2.14 or 2.15 means a **DPIA is likely required** (Section 5.3).
- **Yes** on 2.12 means **Section 8 (AI-Assisted Development Rules) is required**.
- **Yes** on 2.15 means **extra US/California rules apply** (Section 3 and Section 12).
- If 2.13 is **Yes**, the AI-in-product rows in Section 8.3 are required. Otherwise mark them `N/A`.

## 3. Which Privacy Laws Apply?

> **Hint:** Laws usually follow *where your users live*, not where your company sits. Tick every region where you will have users in the first 500 customers. **Example:** `[x] EU/UK - yes, we have users in Germany.`

| Applies? | Region / Law | Applies when... | Decision notes |
|---|---|---|---|
| [ ] | **EU GDPR** (EU/EEA users) | You offer to or monitor people in the EU/EEA | [TBD] |
| [ ] | **UK GDPR + Data Protection Act 2018** | Same, for the UK | [TBD] |
| [ ] | **US California CCPA/CPRA** | You meet a business threshold (revenue, data volume, or share of income from selling/sharing data) and have California residents | [TBD] |
| [ ] | **Other US state laws** (e.g. Virginia, Colorado, Texas, and others) | Thresholds vary by state | [TBD] |
| [ ] | **COPPA (US, children under 13)** | Product is aimed at under-13s or you know you collect their data | [TBD] |
| [ ] | **HIPAA (US health)** | You handle protected health info for a covered healthcare entity | [TBD] |
| [ ] | **India DPDP Act 2023** and its Rules | You process digital personal data of people in India | [TBD] |
| [ ] | **Other country: [TBD]** | [TBD] | [TBD] |
| [ ] | **Industry rules** (e.g. PCI DSS for cards) | [TBD] | [TBD] |

**Baseline rule (important):** When more than one law applies, follow the **strictest** rule for each item unless the Privacy Lead approves otherwise in writing. This keeps one product and one process for all users.

Who confirmed this table (name, date)? [TBD]

## 4. Data Inventory ("What do we collect and why?")

> **Hint:** This is the most important table in the document. One row per kind of data. If you cannot explain *why* you need it, **do not collect it** (this is called data minimization). **Example row:** `Email address | Contact info | Create account, send receipts | User types it in | Users' accounts DB | Yes (email service) | Account life + 30 days | Medium`.

| ID | Data item | Category | Why we need it (purpose) | Where it comes from | Where it is stored | Shared with vendors? (name) | How long we keep it | Sensitivity (Low/Med/High) |
|---|---|---|---|---|---|---|---|---|
| D-01 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| D-02 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| D-03 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| D-04 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| D-05 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

*(Add more rows as needed. Include technical data too: IP address, device ID, cookies, crash logs, usage events.)*

**Category choices:** Contact info, Account/login, Payment, Location, Device/technical, Usage/behaviour, Content created by user, Photos/audio/video, Health, Children's data, Other.

### 4.1 Data Flow Summary

> **Hint:** Describe in 3 to 6 plain sentences how data travels: user → app → server → vendors → deletion. A simple drawing link is also fine.

[TBD]

Link to data-flow diagram (if any): [TBD]

### 4.2 Data Minimization Check

| Check | Yes / No | Notes |
|---|---|---|
| Every item in 4 has a clear purpose | [TBD] | |
| We removed items we could live without | [TBD] | |
| We use anonymous or pseudonymous data where possible | [TBD] | |
| Optional data is clearly marked "optional" in the UI | [TBD] | |

## 5. Special Data: Children, Health, Financial

> **Hint:** If everything in 2.6, 2.7 and 2.8 is "No", write `N/A - no children's, health or financial data` in each sub-section and move on. Otherwise, fill in carefully; mistakes here are the costliest.

### 5.1 Children's Data

| Question | Your Answer |
|---|---|
| Minimum age allowed to use the product | [TBD] |
| How do we check age? (self-declaration, age gate, verification) | [TBD] |
| What happens if we find a user is under the minimum age? | [TBD] |
| Do we need parental consent? (Defaults below) | [TBD] |
| Are ads, tracking or profiling turned off for minors? | [TBD] |

**Default age rules (verify per country):** US COPPA: under 13 needs verifiable parental consent. EU/UK: digital consent age is 13 to 16 depending on country (use 16 as the safe baseline). India DPDP: under 18 needs verifiable parental/guardian consent, with no tracking, behavioural monitoring or targeted ads aimed at children. California: opt-in needed to sell data of users under 16.

### 5.2 Health and Financial Data

| Question | Your Answer |
|---|---|
| What exact health/financial data do we collect? | [TBD] |
| Is explicit consent collected separately from general terms? | [TBD] |
| Extra protections (encryption, restricted access, audit log) | [TBD] |
| Law/standard that applies (HIPAA, PCI DSS, other) | [TBD] |

### 5.3 DPIA (Data Protection Impact Assessment) Decision

> **Hint:** A DPIA is a short written risk check. Do one **before building** when your project is risky. **Example:** `DPIA required: Yes. Reason: precise location of minors. Completed: 02-Feb-2027. Link: ...`.

| Trigger | Applies? (Yes/No) |
|---|---|
| Large-scale personal data | [TBD] |
| Children's, health, financial or precise-location data | [TBD] |
| Profiling or automated decisions that affect people | [TBD] |
| New technology or AI that sees user data | [TBD] |
| Monitoring people in public or at work | [TBD] |

DPIA required? [ ] Yes [ ] No. If **Yes**: Owner [TBD]; Date completed [TBD]; Link [TBD]; Residual risks accepted by [TBD].

## 6. Lawful Basis and Consent

> **Hint:** You must have a *legal reason* for each use of data. Pick one per purpose. **Example:** `Send receipts | Contract | Needed to deliver what the user bought`.

**Allowed reasons (GDPR terms; map to other laws as noted in Appendix B):** Contract (needed to provide the service), Legal obligation, Legitimate interests (you balanced it against user rights), Consent (user clearly said yes), Vital interests, Public task.

| Purpose (copy from Section 4) | Lawful basis | If Consent: how and where collected | Evidence we store |
|---|---|---|---|
| [TBD] | [TBD] | [TBD] | [TBD] |
| [TBD] | [TBD] | [TBD] | [TBD] |
| [TBD] | [TBD] | [TBD] | [TBD] |

### 6.1 Consent Quality Requirements (apply to every consent)

| ID | Requirement | Priority |
|---|---|---|
| PRV-001 | Consent is a **clear, active choice**. No pre-ticked boxes. | MUST |
| PRV-002 | Consent is **separate** from accepting Terms of Service. | MUST |
| PRV-003 | Each purpose has its **own** choice (no bundling analytics with marketing). | MUST |
| PRV-004 | Users can **withdraw** consent as easily as they gave it. | MUST |
| PRV-005 | We **record** who consented, when, to what, and which policy version. | MUST |
| PRV-006 | The consent text is in **plain language** in the user's language. | SHOULD |
| PRV-007 | "Reject all" is as visible as "Accept all" on cookie/tracker banners. | MUST |

---

# GATE G2: BUILD AND TEST

## 7. Privacy-by-Design Build Requirements

> **Hint:** These are the rules developers follow while building. For each, set the Status and give **Evidence** (a link to a ticket, screenshot, test result, or code review). "We did it" without a link does not count as DONE.

| ID | Requirement | Priority | Owner | Status | Evidence link |
|---|---|---|---|---|---|
| PRV-010 | Only the data listed in Section 4 is collected. Anything new requires updating Section 4 first. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-011 | Personal data is **encrypted in transit** (HTTPS/TLS 1.2 or higher). | MUST | [TBD] | [TBD] | [TBD] |
| PRV-012 | Personal data is **encrypted at rest** (database, backups, file storage). | MUST | [TBD] | [TBD] | [TBD] |
| PRV-013 | Passwords are **hashed** with a modern algorithm (e.g. bcrypt/argon2). Never stored in plain text. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-014 | **Least privilege:** each person/system sees only the data needed for their job. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-015 | Multi-factor authentication for admin and production access. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-016 | **No real personal data** in development or test environments. Use fake or masked data. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-017 | **No secrets or personal data in code, logs, URLs or error messages.** | MUST | [TBD] | [TBD] | [TBD] |
| PRV-018 | An **access log** records who viewed or changed personal data in production. | SHOULD | [TBD] | [TBD] | [TBD] |
| PRV-019 | Privacy defaults are the **most protective** (e.g. profile private, marketing off). | MUST | [TBD] | [TBD] | [TBD] |
| PRV-020 | Data can be **exported** and **deleted** per user (supports Section 13). | MUST | [TBD] | [TBD] | [TBD] |
| PRV-021 | Backups follow the retention schedule (Section 14), including deletion after the backup cycle. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-022 | Dependencies and libraries are scanned for known security flaws before each release. | SHOULD | [TBD] | [TBD] | [TBD] |
| PRV-023 | Privacy is part of **code review**: reviewers check new data fields and third-party calls. | SHOULD | [TBD] | [TBD] | [TBD] |

## 8. AI-Assisted Development Rules

> **Hint:** AI coding assistants and agents are powerful but they send text to outside companies. These rules stop personal data and secrets from leaking through them. If row 2.12 was "No", write `N/A` in every row below. **Example:** `Approved AI tools: Claude (company workspace, no training on our data).`

### 8.1 AI Tools Register

| Tool name | Vendor | Used for | Does the vendor train on our inputs? (Yes/No/UNKNOWN) | Data-handling terms checked? | Approved by | Date |
|---|---|---|---|---|---|---|
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

### 8.2 Rules for AI Tools Used to Build the Product

| ID | Requirement | Priority | Owner | Status | Evidence |
|---|---|---|---|---|---|
| PRV-030 | Only tools listed in 8.1 may be used. Unapproved tools are forbidden. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-031 | **Never paste real user data** (names, emails, IDs, customer records) into an AI prompt. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-032 | **Never paste secrets** (API keys, passwords, tokens, private keys) into an AI prompt. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-033 | AI agents get **only the access they need** (read-only where possible; no production database access). | MUST | [TBD] | [TBD] | [TBD] |
| PRV-034 | Business accounts are used where **training on our inputs is disabled**. Personal free accounts are not used for company work. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-035 | **A human reviews all AI-generated code** before it merges. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-036 | AI-generated code is scanned for security and privacy flaws (hidden data collection, unsafe logging, wrong libraries). | MUST | [TBD] | [TBD] | [TBD] |
| PRV-037 | Agent actions are **logged** (what was asked, what changed, who approved). | SHOULD | [TBD] | [TBD] | [TBD] |
| PRV-038 | Destructive agent actions (delete data, change permissions, send messages, deploy) need **human approval**. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-039 | Test data used with AI is **synthetic**. | MUST | [TBD] | [TBD] | [TBD] |
| PRV-040 | AI vendors are treated like any vendor: listed in Section 9 with a signed agreement if personal data could ever reach them. | MUST | [TBD] | [TBD] | [TBD] |

### 8.3 If the Product Itself Uses AI on User Data (otherwise mark all `N/A`)

| ID | Requirement | Priority | Status | Evidence |
|---|---|---|---|---|
| PRV-045 | The user is **told** when they are interacting with AI or when AI processes their data. | MUST | [TBD] | [TBD] |
| PRV-046 | We state whether user data is used to **train or improve** models. Default is **no training** without explicit consent. | MUST | [TBD] | [TBD] |
| PRV-047 | AI prompts/outputs containing personal data are covered by retention and deletion rules. | MUST | [TBD] | [TBD] |
| PRV-048 | Automated decisions with legal or major effect have **human review** and an explanation path. | MUST | [TBD] | [TBD] |
| PRV-049 | The AI model vendor is listed in Section 9 with a signed DPA. | MUST | [TBD] | [TBD] |

## 9. Third Parties and Vendors

> **Hint:** Any outside company that touches personal data goes here: hosting, email, payments, analytics, crash reporting, support chat, AI services, advertising. **Example:** `SendMail Co | Sends receipts | Email, name | Yes, signed 01-Mar-2027 | USA | SCCs`.

| Vendor | What they do for us | Data they receive (IDs from Section 4) | Role (Processor / Independent controller) | DPA signed? | Country of processing | Transfer protection used | Security reviewed? | Owner |
|---|---|---|---|---|---|---|---|---|
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

| ID | Requirement | Priority | Status | Evidence |
|---|---|---|---|---|
| PRV-050 | Every vendor that handles personal data has a **signed DPA/contract** before launch. | MUST | [TBD] | [TBD] |
| PRV-051 | Each vendor was **security-checked** (certifications, breach history, sub-processors). | SHOULD | [TBD] | [TBD] |
| PRV-052 | Vendors are bound to **notify us of breaches** within [TBD] hours (default: 24 to 48). | MUST | [TBD] | [TBD] |
| PRV-053 | Vendors **delete or return** data when the contract ends. | MUST | [TBD] | [TBD] |
| PRV-054 | We do **not** sell or share personal data for advertising unless Section 2.15 says Yes and opt-out is built. | MUST | [TBD] | [TBD] |

## 10. International Data Transfers

> **Hint:** Moving data from one country to another (even viewing it from abroad) can need extra legal protection. If all data stays in one country with no outside access, write `N/A`.

| From (user's region) | To (storage / vendor country) | Legal mechanism | Evidence |
|---|---|---|---|
| [TBD] | [TBD] | [TBD] | [TBD] |

**Common mechanisms:** adequacy decision (the destination is recognised as safe), Standard Contractual Clauses (SCCs) or UK IDTA/Addendum, approved certification frameworks (e.g. the EU-US Data Privacy Framework, if the vendor is certified), India DPDP rules on permitted countries (verify current list).
- [ ] A transfer risk assessment was done where needed. Link: [TBD]
- [ ] Data storage region is chosen deliberately (e.g. EU region for EU users). Region: [TBD]

## 11. Security Controls That Protect Privacy (Short Checklist)

> **Hint:** Detailed security lives in your Security Requirements document. This is the privacy-relevant minimum. Tick when verified.

- [ ] Regular, tested backups exist and are encrypted
- [ ] Production access list reviewed (who has it, why) and reviewed every [TBD] months (default: 3)
- [ ] Former team members' access removed within 24 hours of leaving
- [ ] Vulnerability scan and basic penetration test done before launch
- [ ] Rate limiting and account lockout protect login
- [ ] Monitoring and alerts for unusual data access or large exports
- [ ] Staff with data access completed privacy training. Date: [TBD]

## 12. Cookies, Trackers, SDKs and Mobile Permissions

> **Hint:** List everything that follows users around: cookies, analytics scripts, ad pixels, mobile SDKs. If you cannot name it, you cannot disclose it. **Example:** `Google Analytics | Analytics | Consent required | Banner blocks until accepted`.

### 12.1 Tracker Register

| Name | Type (cookie / pixel / SDK) | Purpose (Essential / Analytics / Marketing) | Vendor | Needs consent? | Loads only after consent? |
|---|---|---|---|---|---|
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

| ID | Requirement | Priority | Status | Evidence |
|---|---|---|---|---|
| PRV-060 | Non-essential cookies/SDKs **do not run** until the user opts in (where law requires). | MUST | [TBD] | [TBD] |
| PRV-061 | Cookie banner has Accept, Reject and Manage choices, equally visible. | MUST | [TBD] | [TBD] |
| PRV-062 | The product honours **Global Privacy Control (GPC)** or similar opt-out signals where US state law requires. | MUST | [TBD] | [TBD] |
| PRV-063 | If selling/sharing data: "Do Not Sell or Share My Personal Information" link is visible. | MUST (if applicable) | [TBD] | [TBD] |
| PRV-064 | If using sensitive personal information beyond permitted uses: "Limit the Use of My Sensitive Personal Information" option exists (California). | MUST (if applicable) | [TBD] | [TBD] |

### 12.2 Mobile App Requirements (mark `N/A` for web-only)

| ID | Requirement | Priority | Status | Evidence |
|---|---|---|---|---|
| PRV-065 | Device permissions (camera, mic, location, contacts, notifications) are asked **only when needed**, with a plain explanation first. | MUST | [TBD] | [TBD] |
| PRV-066 | The app works as far as possible when a permission is **denied**. | SHOULD | [TBD] | [TBD] |
| PRV-067 | **Apple App Store privacy "nutrition label"** answers match Section 4 and the SDK register. | MUST | [TBD] | [TBD] |
| PRV-068 | **Google Play Data Safety** form matches Section 4 and the SDK register. | MUST | [TBD] | [TBD] |
| PRV-069 | A privacy policy link is inside the app (settings screen) and on each store page. | MUST | [TBD] | [TBD] |
| PRV-070 | Account and data **deletion can be started inside the app** (store rules require it). | MUST | [TBD] | [TBD] |

## 13. User Rights Handling

> **Hint:** People can ask what you hold about them, fix it, delete it, or object to uses. You need a **working process** before launch, not after the first request arrives. **Example:** `Requests arrive at privacy@plantpal.example; Support logs in tracker; Engineering exports data via admin tool; reply within 30 days.`

### 13.1 Which Rights Must We Support?

| Right | Plain meaning | EU/UK | California | India DPDP | We support it? | How (button, email, form) |
|---|---|---|---|---|---|---|
| Access | "Show me my data" | Yes | Yes | Yes | [TBD] | [TBD] |
| Correction | "Fix wrong data" | Yes | Yes | Yes | [TBD] | [TBD] |
| Deletion | "Erase my data" | Yes | Yes | Yes | [TBD] | [TBD] |
| Portability | "Give me my data in a usable file" | Yes | Yes | Not stated as a standalone right (verify) | [TBD] | [TBD] |
| Object / restrict | "Stop using my data for this" | Yes | Opt-out of sale/sharing | Withdraw consent | [TBD] | [TBD] |
| Withdraw consent | "I changed my mind" | Yes | Yes (opt-out) | Yes | [TBD] | [TBD] |
| Not be subject to solely automated decisions | "A human must decide" | Yes | Rules on automated decision-making technology (verify) | N/A | [TBD] | [TBD] |
| Nominate someone (e.g. in case of death) | | N/A | N/A | Yes | [TBD] | [TBD] |
| Grievance redressal | "I want to complain" | Yes (authority) | Yes | Yes | [TBD] | [TBD] |
| Non-discrimination | "Don't punish me for asking" | Implied | Yes | N/A | [TBD] | [TBD] |

### 13.2 Request Handling Rules (editable defaults)

| Item | Default | Your value |
|---|---|---|
| Where requests arrive | Public privacy email + in-app/account page | [TBD] |
| Acknowledge request within | 5 business days | [TBD] |
| Complete request within | 30 days (GDPR: 1 month; California: 45 days, extendable once; strictest wins) | [TBD] |
| Identity check method | Match email on account; extra check for sensitive requests | [TBD] |
| Cost to user | Free (reasonable fee only if requests are clearly excessive) | [TBD] |
| Who decides refusals | Privacy Lead | [TBD] |
| Request log kept at | [TBD] | [TBD] |
| Request log kept for | 24 months | [TBD] |

| ID | Requirement | Priority | Status | Evidence |
|---|---|---|---|---|
| PRV-080 | A **written procedure** exists with named owners (Section 1.2). | MUST | [TBD] | [TBD] |
| PRV-081 | Support staff are **trained** to recognise a privacy request in any channel (email, chat, social). | MUST | [TBD] | [TBD] |
| PRV-082 | **Test run:** at least one fake export request and one fake deletion request completed before launch. | MUST | [TBD] | [TBD] |
| PRV-083 | Deletion reaches **all** copies: database, backups (per schedule), vendors, analytics, logs. | MUST | [TBD] | [TBD] |
| PRV-084 | Every request is **logged** with date received, type, outcome and date answered. | MUST | [TBD] | [TBD] |
| PRV-085 | Users can **appeal** a refusal and are told how to contact the regulator. | SHOULD | [TBD] | [TBD] |

## 14. Data Retention and Deletion

> **Hint:** "Keep data only as long as you need it." For each data group, set a time limit and say what happens at the end. **Example:** `Account data | Life of account + 30 days | Auto-delete job | Backups purge after 35 days`.

| Data group (from Section 4) | Keep for | Reason for that period | Deleted by (method) | Backup purge time | Owner |
|---|---|---|---|---|---|
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

| ID | Requirement | Priority | Status | Evidence |
|---|---|---|---|---|
| PRV-090 | Every data group in Section 4 has a retention time. "Forever" is not allowed unless the law requires it. | MUST | [TBD] | [TBD] |
| PRV-091 | Deletion is **automatic** (scheduled job) where possible. | SHOULD | [TBD] | [TBD] |
| PRV-092 | Inactive accounts are handled (warn then delete after [TBD] months). | SHOULD | [TBD] | [TBD] |
| PRV-093 | Retention periods are **stated in the public policy** (California requires this). | MUST | [TBD] | [TBD] |
| PRV-094 | Legal holds (e.g. tax records) are documented as the only exceptions. | MUST | [TBD] | [TBD] |

---

# GATE G3: PRE-LAUNCH / BETA

## 15. Incident and Breach Response

> **Hint:** A "breach" means personal data was lost, stolen, leaked or accessed by someone who should not have it. Plan **before** it happens. Clocks start when you become *aware*. **Example:** `Detect Tue 10:00 → Privacy Lead informed 10:30 → Authority notified within 72h → Users told without undue delay.`

### 15.1 Deadlines (editable defaults; strictest wins)

| Who must be told | Default deadline | Source |
|---|---|---|
| Internal Privacy Lead and Engineering Lead | Within **1 hour** of suspicion | Internal rule |
| EU/UK regulator | Within **72 hours** of becoming aware (unless unlikely to risk people) | GDPR / UK GDPR |
| Affected people | **Without undue delay** when risk to them is high | GDPR; US state laws vary |
| India Data Protection Board and each affected person | **Without delay**; detailed report to the Board within **72 hours** (verify current Rules) | DPDP Rules |
| US states / California | Varies by state; some have fixed deadlines | State breach laws |
| Vendors to us | Within [TBD] hours (default 24 to 48) | Contract |

### 15.2 Response Plan Basics

| Item | Your Answer |
|---|---|
| Incident commander (name, backup) | [TBD] |
| How staff report a suspected incident (email, chat channel, phone) | [TBD] |
| Where incident notes are kept | [TBD] |
| Pre-written notification templates exist? Link | [TBD] |
| Law firm / DPO / insurer to call | [TBD] |

| ID | Requirement | Priority | Status | Evidence |
|---|---|---|---|---|
| PRV-100 | A written **Incident Response Plan** names roles, steps and deadlines. | MUST | [TBD] | [TBD] |
| PRV-101 | A **practice drill** was held (30-minute tabletop exercise) before launch. | MUST | [TBD] | [TBD] |
| PRV-102 | A **breach register** records every incident, even minor ones. | MUST | [TBD] | [TBD] |
| PRV-103 | After each incident, a **lessons-learned** review is done within 14 days. | SHOULD | [TBD] | [TBD] |

## 16. Public Privacy Policy Requirements

> **Hint:** The public policy must be easy to find, easy to read and **true**. Every claim in it must match this document. If the policy says "we delete after 30 days", Section 14 must say the same. Use the skeleton in Appendix A.

| ID | Requirement | Priority | Status | Evidence |
|---|---|---|---|---|
| PRV-110 | Policy is linked from: website footer, sign-up screen, app settings, app store pages, checkout. | MUST | [TBD] | [TBD] |
| PRV-111 | **Notice at collection:** short notice shown at the moment data is collected (what, why, link to the full policy). | MUST | [TBD] | [TBD] |
| PRV-112 | Written in **plain language**, at a reading level a teenager can follow, with headings. | MUST | [TBD] | [TBD] |
| PRV-113 | Covers **every item** in the Appendix A skeleton. | MUST | [TBD] | [TBD] |
| PRV-114 | Lists categories of data collected in the **last 12 months**, sources, purposes, recipients, and whether data is sold/shared (California). | MUST | [TBD] | [TBD] |
| PRV-115 | Shows **contact details** for privacy questions and, where required, DPO and EU/UK representative. | MUST | [TBD] | [TBD] |
| PRV-116 | Shows **effective date** and **version history**. | MUST | [TBD] | [TBD] |
| PRV-117 | **Material changes** are announced to users before they take effect (email or in-app). | MUST | [TBD] | [TBD] |
| PRV-118 | Previous versions are **archived** (consent records point to the version users saw). | SHOULD | [TBD] | [TBD] |
| PRV-119 | Available in each language we market in. | SHOULD | [TBD] | [TBD] |
| PRV-120 | Accessible (screen-reader friendly, readable on mobile). | SHOULD | [TBD] | [TBD] |

Policy URL: [TBD] | Policy owner: [TBD] | Published on: [TBD]

## 17. Verification Matrix (QA Proof)

> **Hint:** QA tests that the requirements really work. For each key area, record what was tested, who tested, the result and the proof link. **Example:** `PRV-082 | Request 'delete me' test | Test user deleted from DB, backups flagged, vendor API called | PASS | link | Rahul, 02-Apr-2027`.

| Requirement ID(s) | Test performed | Expected result | Actual result | Pass / Fail | Evidence link | Tester | Date |
|---|---|---|---|---|---|---|---|
| PRV-011/012 | Check TLS and encryption at rest | All traffic and storage encrypted | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-016/039 | Scan test environment for real data | No real data found | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-017 | Search logs/code for personal data and secrets | None found | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-031/032 | Spot check AI prompt history for personal data or secrets | None found | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-060/061 | Open site fresh; confirm no trackers fire before consent | Trackers blocked until opt-in | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-062 | Send GPC signal; confirm opt-out honoured | Opt-out applied | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-065/070 | Mobile: permission prompts; in-app deletion | Works as written | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-082/083 | Fake access, export and deletion request | Done within deadline; all copies handled | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-101 | Tabletop breach drill | Roles and deadlines followed | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-110/113 | Check every policy link and section | All present and working | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| PRV-067/068 | Compare app-store privacy labels to Section 4 | Exact match | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

## 18. Privacy Risk Register

> **Hint:** List things that could go wrong with personal data and what you will do about them. **Example:** `Risk: analytics SDK collects device ID without consent | Likelihood: Medium | Impact: High | Fix: load only after opt-in | Owner: Engineering Lead`.

| ID | Risk | Likelihood (L/M/H) | Impact (L/M/H) | Plan to reduce it | Owner | Status |
|---|---|---|---|---|---|---|
| R-01 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| R-02 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| R-03 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

## 19. Open Questions, Assumptions and Exceptions

> **Hint:** Anything you could not answer goes here with a deadline. Nothing marked `UNKNOWN` may stay open past Gate G3.

| ID | Question / assumption / exception | Owner | Due date | Resolution | Approved by (for exceptions) |
|---|---|---|---|---|---|
| Q-01 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |
| Q-02 | [TBD] | [TBD] | [TBD] | [TBD] | [TBD] |

## 20. Pre-Launch GO / NO-GO Checklist

> **Hint:** One page. **Every** MUST item must be ticked, or the launch is **NO-GO**. If any box cannot be ticked, record it in Section 19 and get written approval from the Product Owner **and** the Privacy Lead.

**Data and legal**
- [ ] Data inventory (Section 4) is complete and matches the real product
- [ ] Applicable laws chosen and confirmed (Section 3)
- [ ] Lawful basis set for every purpose (Section 6)
- [ ] DPIA done where required (Section 5.3)
- [ ] Children's/health/financial rules applied or marked N/A (Section 5)
- [ ] Lawyer or DPO reviewed this document and the policy. Name/date: [TBD]

**Build and AI**
- [ ] All Section 7 MUST items are DONE with evidence
- [ ] AI tools register approved and AI rules followed (Section 8)
- [ ] No real personal data or secrets in dev, test, code, logs or AI prompts

**Vendors and transfers**
- [ ] All vendor DPAs signed (Section 9)
- [ ] International transfer protection in place (Section 10)

**Users**
- [ ] Consent and cookie banner work and are tested (Sections 6.1 and 12)
- [ ] App store privacy labels match reality (mobile)
- [ ] In-app account deletion works (mobile)
- [ ] User rights process tested end to end (Section 13)
- [ ] Retention and auto-deletion working (Section 14)

**Safety nets**
- [ ] Incident plan written and drill held (Section 15)
- [ ] Public privacy policy live, linked everywhere, and matches this document (Section 16)
- [ ] QA verification matrix complete with no failed MUST rows (Section 17)
- [ ] No open `UNKNOWN` items (Section 19)
- [ ] Gate G1, G2 and G3 sign-offs complete (Section 1.4)

**Decision:** [ ] GO  [ ] NO-GO  [ ] GO WITH APPROVED EXCEPTIONS (list in Section 19)

Decision by: [TBD] Date: [TBD]

---

# GATE G4: LAUNCH TO FIRST 500 CUSTOMERS

## 21. Customer Milestone Reviews

> **Hint:** Privacy does not stop at launch. At each customer milestone, pause for a short check. Milestones are counted by **registered users** (or paying customers; choose one and write it here: [TBD]). **Example at 50 users:** `Request log reviewed: 0 requests. Trackers unchanged. No incidents. Policy still accurate.`

### 21.1 What to Check at Every Milestone

| Check | Milestone 1 (first 50) | Milestone 2 (100) | Milestone 3 (250) | Milestone 4 (500) |
|---|---|---|---|---|
| Date reviewed | [TBD] | [TBD] | [TBD] | [TBD] |
| New data collected that is not in Section 4? | [TBD] | [TBD] | [TBD] | [TBD] |
| New vendors/SDKs/AI tools added? Section 9/12/8 updated? | [TBD] | [TBD] | [TBD] | [TBD] |
| User rights requests received (number) / answered on time (number) | [TBD] | [TBD] | [TBD] | [TBD] |
| Complaints received about privacy | [TBD] | [TBD] | [TBD] | [TBD] |
| Incidents or near misses | [TBD] | [TBD] | [TBD] | [TBD] |
| Consent opt-in rate (%) and any consent issues | [TBD] | [TBD] | [TBD] | [TBD] |
| Is the public policy still 100% accurate? | [TBD] | [TBD] | [TBD] | [TBD] |
| Retention jobs ran and deleted what they should | [TBD] | [TBD] | [TBD] | [TBD] |
| Access list reviewed (who can see production data) | [TBD] | [TBD] | [TBD] | [TBD] |
| New markets/countries where users appear? Section 3 updated? | [TBD] | [TBD] | [TBD] | [TBD] |
| Legal thresholds near? (e.g. California business thresholds; need for DPO/representative) | [TBD] | [TBD] | [TBD] | [TBD] |
| Reviewer name | [TBD] | [TBD] | [TBD] | [TBD] |

### 21.2 Launch Window Operating Requirements

| ID | Requirement | Priority | Owner | Status |
|---|---|---|---|---|
| PRV-130 | Privacy inbox is **monitored every business day**. | MUST | [TBD] | [TBD] |
| PRV-131 | **Weekly** check of logs and alerts for unusual data access during the first 30 days after launch. | SHOULD | [TBD] | [TBD] |
| PRV-132 | **No new data field, vendor, tracker or AI tool** goes live before Sections 4, 8, 9 and 12 are updated and the Privacy Lead approves. | MUST | [TBD] | [TBD] |
| PRV-133 | Policy changes follow PRV-117 (notify before effect). | MUST | [TBD] | [TBD] |
| PRV-134 | At the 500-customer mark, a **full re-review** of this whole document is done and a decision made on whether a lawyer/DPO audit is needed. | MUST | [TBD] | [TBD] |

### 21.3 Escalation Triggers (do these immediately)

| If this happens... | Then... |
|---|---|
| A suspected data leak or loss | Start Section 15 at once. |
| A regulator, lawyer or journalist contacts you about privacy | Tell the Privacy Lead and Product Owner the same day. Do not reply alone. |
| A user says they are under the minimum age | Follow Section 5.1 (stop collecting; delete as required). |
| A vendor tells you they were breached | Start Section 15 and check which Section 4 items were sent to them. |
| A request cannot be completed within the deadline | Tell the user before the deadline with a reason and a new date (if the law allows extension). |

## 22. Review Schedule and Change Log

### 22.1 Review Schedule (editable defaults)

| Review | Frequency | Next due | Owner |
|---|---|---|---|
| Full document review | Every 6 months, at 500 customers, and before any major feature | [TBD] | [TBD] |
| Vendor and SDK register review | Every 3 months | [TBD] | [TBD] |
| Access list review | Every 3 months | [TBD] | [TBD] |
| Law changes check | Every 6 months | [TBD] | [TBD] |
| Incident drill | Every 12 months | [TBD] | [TBD] |

**Triggers for an immediate review:** new data type, new country, new vendor, new AI feature, incident, regulator guidance, acquisition, or change of purpose for existing data.

### 22.2 Change Log

| Version | Date | Author | What changed | Approved by |
|---|---|---|---|---|
| 0.1 | [TBD] | [TBD] | First draft from template v1.0 | [TBD] |
| 1.0 | [TBD] | [TBD] | Approved for launch | [TBD] |

---

## 23. Glossary (Plain-English)

| Term | Meaning |
|---|---|
| Anonymous data | Data that can never be linked back to a person. Not personal data. |
| Pseudonymous data | Data with names removed but can still be linked back with extra info. Still personal data. |
| Consent | A clear, free, informed "yes" from the user, which they can take back. |
| Controller / Business / Data Fiduciary | The company that decides why and how data is used (GDPR / CCPA / DPDP terms). |
| Processor / Service Provider / Data Processor | A company that handles data on your behalf under your instructions. |
| Data minimization | Collect only what you truly need. |
| DPIA | A written risk check before risky data use. |
| DPO | Data Protection Officer: a privacy expert with a protected role. |
| DPA | The contract with a processor about handling data. |
| GPC | Global Privacy Control: a browser signal that says "do not sell or share my data". |
| Lawful basis | The legal reason that allows you to use personal data. |
| Legitimate interests | A business reason you balanced against the user's rights. |
| PII / Personal data | Information about an identifiable person. |
| Sensitive personal data | Extra-protected data (health, finance, children, precise location, biometrics, beliefs, sexual orientation, and so on). |
| Retention | How long you keep data. |
| SCCs | Standard Contractual Clauses: pre-approved contract terms for sending data abroad. |
| SDK | A software kit from another company inside your app (often collects data). |
| Sub-processor | A company your vendor uses to help them serve you. |
| Tabletop exercise | A practice drill where the team talks through a pretend incident. |

---

# APPENDIX A: PRIVACY POLICY SKELETON TEXT (ADAPT, DO NOT COPY BLINDLY)

> **How to use:** Copy this into your website, replace every `[BRACKET]` using the answers above, delete sections that do not apply, and send the result to your lawyer/DPO. Every sentence must be **true** for your product.

---

**Privacy Policy for [PRODUCT NAME]**
**Effective date:** [DATE]  |  **Version:** [VERSION]

**1. Who we are**
[COMPANY NAME], [ADDRESS], is responsible for your personal data. Contact us at [PRIVACY EMAIL]. [DPO / EU-UK REPRESENTATIVE DETAILS IF ANY.]

**2. What data we collect**
We collect: [LIST FROM SECTION 4 BY CATEGORY]. We get it from: [YOU / YOUR DEVICE / PARTNERS].

**3. Why we use your data, and our legal reason**
| What we do | Why | Legal reason |
|---|---|---|
| [PURPOSE] | [WHY] | [CONTRACT / CONSENT / LEGITIMATE INTERESTS / LEGAL OBLIGATION] |

**4. Who we share it with**
We share data with: [VENDOR CATEGORIES, EXAMPLES]. They may only use it to serve us. [WE DO / DO NOT SELL OR SHARE PERSONAL DATA FOR ADVERTISING.]

**5. Cookies, trackers and similar tools**
We use [LIST]. You can change your choices at [LINK/SETTINGS]. We respond to [GPC/OPT-OUT SIGNALS].

**6. Sending data to other countries**
Your data may be processed in [COUNTRIES]. We protect it using [MECHANISM].

**7. How long we keep your data**
[DATA GROUP]: [PERIOD]. After that we [DELETE/ANONYMISE].

**8. Your rights**
You can ask to see, correct, delete, or receive a copy of your data, to object or withdraw consent, and to complain. [CALIFORNIA: DO-NOT-SELL/SHARE AND LIMIT-USE RIGHTS.] [INDIA: RIGHT TO NOMINATE.] Use [HOW TO ASK]. We answer within [30] days. You will not be treated worse for using your rights. You can also complain to your local data protection authority [NAME/LINK] [INDIA: DATA PROTECTION BOARD].

**9. Children**
[PRODUCT] is [NOT FOR / FOR] children under [AGE]. [WHAT WE DO IF WE LEARN A CHILD'S DATA WAS COLLECTED.]

**10. How we protect your data**
We use [ENCRYPTION, ACCESS CONTROLS, ETC. TRUTHFULLY]. If a breach affects you, we will tell you [AS REQUIRED BY LAW].

**11. Automated decisions and AI**
[IF NONE: "We do not make decisions about you solely by automated means."] [IF AI USED: WHAT IT DOES, WHETHER YOUR DATA TRAINS MODELS, HOW TO ASK FOR HUMAN REVIEW.]

**12. Changes to this policy**
We will tell you before important changes take effect, by [EMAIL/IN-APP]. Past versions: [LINK].

**13. Contact and complaints**
[PRIVACY EMAIL], [POSTAL ADDRESS], [GRIEVANCE OFFICER IF REQUIRED].

---

# APPENDIX B: LAW QUICK-REFERENCE (SIMPLIFIED; VERIFY WITH A LAWYER)

> Laws change often. Treat this table as a **starting map**, and confirm each item before relying on it. Last reviewed by: [TBD] on [TBD].

| Topic | EU/UK GDPR | California CCPA/CPRA | India DPDP Act 2023 (and Rules) |
|---|---|---|---|
| Who it protects | People in the EU/UK | California residents | People in India (digital personal data) |
| Legal reason needed | Yes (6 bases) | Notice at collection plus opt-out of sale/sharing and limits on sensitive data | Consent or listed "legitimate uses" |
| Children | Digital consent age 13 to 16 | Opt-in for sale/sharing of data of under-16s | Under 18: verifiable parental consent; no tracking or targeted ads to children |
| Request deadline | 1 month (extendable) | 45 days (extendable once) | Grievance response timelines set by the Rules (verify) |
| Breach notice | Regulator within 72 hours; users if high risk | State breach laws apply | Board and affected persons; detailed report to Board within 72 hours (verify Rules) |
| Impact assessment | DPIA for high risk | Risk assessments and audits for some activities (verify current regulations) | Significant Data Fiduciaries: DPIA and audits |
| Transfers abroad | Need a transfer mechanism | Not restricted in the same way; contract terms needed | Allowed except to countries the government restricts (verify) |
| Fines (maximums) | Up to 4% of global turnover or EUR 20M | Per-violation civil penalties | Up to INR 250 crore for the most serious breaches |
| Timing note | In force | In force; regulations evolving | Rules notified in late 2025 with obligations phased in over roughly 12 to 18 months. Check which parts are in force on your launch date |

---

# APPENDIX C: FILLED EXAMPLE (FICTIONAL PRODUCT, FOR LEARNING ONLY)

> **Do not copy these answers.** This shows how a finished document *feels*: short, specific, with owners and evidence.

**Project:** PlantPal, a mobile app (iOS + Android) and web dashboard that reminds people to water their plants.
**Launch date:** 15-Jun-2027. **Users:** US, UK, India, Germany.

**Roles (1.2):** Product Owner: Asha Rao. Engineering Lead: Ben Ortiz. Privacy Lead: external consultant, Priya Nair. QA/Security: Rahul Mehta.

**Snapshot highlights (2):** accounts: Yes. Email: Yes. Approximate location (for weather): Yes. Photos of plants: Yes. Payments: Yes (via payment vendor; we store no card numbers). Children: No (age gate 16+). Health/financial: No. Analytics: Yes. Vendors: Yes. AI coding assistants: Yes. AI in product: No.

**Laws (3):** [x] GDPR, [x] UK GDPR, [x] California (we plan for it from day one), [x] India DPDP. Strictest-wins baseline adopted.

**Data inventory (4), sample rows:**

| ID | Data | Category | Purpose | Source | Stored | Vendor | Keep | Sensitivity |
|---|---|---|---|---|---|---|---|---|
| D-01 | Email | Contact | Login, reminders, receipts | User | Accounts DB (EU region) | SendMail Co | Account + 30 days | Medium |
| D-02 | City (not GPS) | Location | Weather-based reminders | User picks | Accounts DB | Weather API (city name only) | Account + 30 days | Low |
| D-03 | Plant photos | User content | Identify plant health | User uploads | Encrypted storage | None | 90 days after delete request | Medium |
| D-04 | App usage events | Usage | Improve features | App | Analytics vendor | AnalyticsCo | 14 months | Low |

**Lawful basis (6):** D-01 Contract. D-02 Contract. D-03 Contract. D-04 **Consent** (opt-in banner; consent stored with policy version).

**DPIA (5.3):** Not required (no minors, no sensitive data, no profiling). Decision recorded by Priya Nair, 10-Jan-2027.

**AI tools register (8.1):** Claude (team workspace, training on our inputs off, terms checked 20-Jan-2027, approved by Asha). Rule: no real customer data in prompts; agents have read-only repo access; all merges need a human review.

**Sample requirement rows:**

| ID | Requirement | Owner | Status | Evidence |
|---|---|---|---|---|
| PRV-016 | No real personal data in dev/test | Ben | DONE | Link to seeded fake-data script and scan report, 18-Mar-2027 |
| PRV-060 | Trackers wait for consent | Ben | DONE | Screen recording of fresh install, 02-Apr-2027 |
| PRV-070 | In-app account deletion | Ben | DONE | Test account deleted; DB + vendor confirmations, 05-Apr-2027 |
| PRV-101 | Breach tabletop drill | Priya | DONE | Drill notes, 20-Apr-2027 |

**Go/No-Go (20):** GO WITH APPROVED EXCEPTION: the German-language privacy policy will follow within 30 days after launch (Q-01, approved by Asha and Priya on 10-Jun-2027).

**Milestone 1 (50 users):** 0 rights requests, 0 incidents, opt-in rate 62%, policy still accurate, no new vendors. Reviewer: Rahul, 02-Jul-2027.

---

*End of template. Before sharing a completed copy, search the whole file for `[TBD]` and `UNKNOWN`. Both should return zero results.*
