# How to Fill This Document

**Template version:** 1.0 | **Folder:** Security, Compliance and Governance | **Applies to:** every project, from first build to the first 500 customers

## What is this document?
It is a list of **who (or what) can get into which system**, and a record that someone **checked** that each access is still needed. Think of it like a list of who has keys to your house, plus a regular check that nobody has a key they don't need.

## Who fills it in?
- **Owner:** the person responsible for the project. They fill in and keep the document up to date.
- **Reviewer:** a different person who checks the Owner's work. On a solo project, ask a friend or advisor. If that is impossible, write "Self-review" and explain why in the Findings section.
- **Approver:** the person who says "yes, this is OK." This can be the Owner on very small teams.

## The 7 golden rules
1. **Never write passwords, API keys, tokens or secrets in this file.** Write only *where* they are stored (example: "Password manager, vault 'Prod'").
2. **Never leave a cell empty.** Write `N/A` (not needed, and say why) or `TBD` (to be filled by a date, and put the date).
3. **Use real names or role names.** "Everyone" and "the team" are not allowed.
4. **Use dates in this format:** `YYYY-MM-DD` (example: 2026-10-17).
5. **Give every row an Owner.** If nobody owns it, nobody will check it.
6. **Give only the access that is needed (least privilege).** If unsure, give less. Add more later.
7. **Delete the grey *Example* rows** after you understand them.

## How to fill it, step by step
| Step | Do this | Section |
|---|---|---|
| 1 | Fill in the project details | 1-4 |
| 2 | List every system you use | 5 |
| 3 | List every person with access | 6 |
| 4 | List every AI agent, bot and key with access | 7 |
| 5 | Review each row and choose a decision | 6-7 |
| 6 | Record problems and fixes | 11 |
| 7 | Complete the checklist for your phase | 12 |
| 8 | Sign off and log the review | 9, 14 |

## Words you will see (glossary)
| Word | Simple meaning |
|---|---|
| **Access** | Permission to open, read, change or delete something |
| **Least privilege** | Give only the smallest access a person needs to do their job |
| **MFA** | A second proof it is you (such as a code on your phone), on top of your password |
| **Admin / Owner access** | Can change everything, including who else has access. Highest risk |
| **Production (Prod)** | The live product that real customers use |
| **Non-human identity** | A bot, AI agent, service account or API key that acts without a person |
| **API key / token** | A secret "password" a program uses to talk to another program |
| **Rotation** | Replacing a secret with a new one on a schedule |
| **Joiner / Mover / Leaver** | A person who joins, changes role, or leaves |
| **Break-glass access** | Emergency access, used only when something is on fire, and then closed |
| **Evidence** | Proof you checked (screenshot, export, ticket link) |
| **Phase gate** | A "stop and check" before moving to the next phase |
| **Personal data** | Anything that identifies a person (name, email, phone, IP address) |

## Risk levels (pick one per row)
| Level | Choose this when... | Examples |
|---|---|---|
| **High** | It can change or leak live customer data, money, or the whole system | Production admin, database access, payment tools, AI agent with write access to production, owner of the cloud account |
| **Medium** | It can change work but not customer data or live systems | Code repository write access, staging servers, support desk with customer emails |
| **Low** | Read-only, or only affects non-sensitive things | View-only analytics, public docs, read-only dashboards |

If a row sits between two levels, **choose the higher one.**

## Review decisions (pick one per row)
| Decision | Meaning | What happens next |
|---|---|---|
| **Keep** | Still needed, access level is right | Nothing. Note the review date |
| **Reduce** | Still needed, but too much access | Lower it, record the fix date |
| **Remove** | No longer needed | Delete access, record the date |
| **Escalate** | You are unsure or something looks wrong | Add to Findings (Section 11) and tell the Approver |

## Status words (use only these)
`Active` | `Pending` (requested, not yet given) | `Suspended` | `Removed` | `Expired`

## Review rhythm
- **At the end of every phase** (the phase gate in Section 12), and
- **Every month after launch**, until you reach 500 customers, and
- **Immediately** after: a person leaves, a secret leaks, an incident happens, or an AI agent gets new powers.

> Tip: set a repeating calendar reminder titled "Access review - [Project name]".

## "Done when..." check for this whole file
- [ ] No empty cells and no secrets written anywhere
- [ ] Every row has an Owner, a Risk level, and a Decision
- [ ] Every High-risk row has Evidence
- [ ] Every Remove / Reduce decision has a fix date and a completion date
- [ ] Section 12 checklist for the current phase is fully ticked
- [ ] Section 14 sign-off is complete

---
---

# Access Review Register

## 1. Project Details
> **Questions to answer:** What is this project called? Who owns it? Where is it right now?

| Field | Your answer |
|---|---|
| Project name | |
| Project ID / code | |
| Project Owner (name, role) | |
| Reviewer (name, role) | |
| Approver (name, role) | |
| Current phase *(pick one: 1 Build / 2 Test / 3 Pre-launch / 4 Launch / 5 Customers 1-500)* | |
| Current customer count | |
| Launch date (planned or actual) | |
| Date of last review | |
| Date of next review | |
| Where this project's secrets are stored *(tool name only, never the secrets)* | |

## 2. Data Types Handled
> **Question:** What kinds of information does this product touch? Tick all that apply. More ticks mean stricter rules.

| Tick | Data type | Rules that may apply |
|---|---|---|
| [ ] | Names, emails, phone numbers (personal data) | GDPR, local privacy laws |
| [ ] | Health information | HIPAA (US) and similar |
| [ ] | Payment card information | PCI DSS |
| [ ] | Children's data | Extra privacy laws |
| [ ] | Company secrets / source code / AI prompts and models | SOC 2, ISO 27001 |
| [ ] | None of the above (explain): | |

## 3. Linked Documents
> **Question:** Where are the other documents related to this one? Paste the link or file name.

| Document | Link or location |
|---|---|
| Risk Register | |
| Incident Response Plan | |
| Data Protection / Privacy Document | |
| Asset or Systems List | |
| Onboarding / Offboarding Checklist | |

## 4. Version and Change History
> **Question:** What changed in this document, who changed it, and when?

| Version | Date | Changed by | What changed |
|---|---|---|---|
| 0.1 | *Example:* 2026-10-17 | *Example:* Sam Lee | *Example:* First draft created |
| | | | |

## 5. Systems Inventory
> **Questions to answer:** What systems does this project use? Where is the code, the servers, the data, the AI tools, the business tools? Add a row for each. If you don't list it here, you can't review it.

**Categories:** `Cloud/Server/Database` | `Code/CI-CD` | `AI tool/LLM` | `Business/SaaS` | `Customer/Production data`

| System ID | System name | Category | What it is used for | System Owner | Holds customer data? (Y/N) | Login uses MFA? (Y/N) | Where admin console is |
|---|---|---|---|---|---|---|---|
| S-001 | *Example:* Main database (Postgres) | Cloud/Server/Database | Stores customer accounts | Sam Lee | Y | Y | Cloud console, project "prod" |
| S-002 | | | | | | | |

**Done when:** [ ] every cloud, code, AI, business and data system is listed, and [ ] every system shows whether MFA is on. *(If MFA is "N" on a High-risk system, add it to Section 11.)*

## 6. People Access Register
> **Questions to answer for each person:** Who is this? What can they open? Why do they need it? Is that the *least* they need? Can they still prove they should have it?

**Access level words:** `View` (read only) | `Edit` (can change) | `Admin` (can change everything and others' access) | `Owner` (full control, including billing)

| Access ID | Person (full name) | Role / team | Employee or contractor? | System ID | Access level | Why they need it | Date granted | Approved by | MFA on? (Y/N) | Risk (L/M/H) | Last review date | Decision | Evidence link | Fix due | Fix done | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| A-001 | *Example:* Jo Park | Developer | Contractor | S-001 | Admin | Fixing database bugs | 2026-08-01 | Sam Lee | Y | High | 2026-10-17 | Reduce | link to screenshot | 2026-10-24 | 2026-10-20 | Active |
| A-002 | | | | | | | | | | | | | | | | |

**Questions to ask yourself in every review:**
1. Does this person still work on this project? (If no, **Remove**.)
2. Did their job change since access was given? (If yes, re-check.)
3. Do they use this access at least once a month? (If no, consider **Remove**.)
4. Could a lower level (like View) do the job? (If yes, **Reduce**.)
5. Is MFA on? (If no, fix immediately for High risk.)
6. Do two people share one login? (If yes, **Escalate**. Every person needs their own login.)

**Done when:** [ ] every person with access to any system in Section 5 is listed, and [ ] every row has a Decision and Last review date.

## 7. AI Agents and Automated Accounts (Non-Human Identities)
> **Why this section exists:** In AI-driven development, AI agents, bots and API keys can read code, change servers and touch customer data, often faster than a person. They need the same checking as people, and more.

### 7A. Register of AI agents, bots, service accounts and API keys
> **Questions to answer for each one:** What is it? Who is responsible for it? What can it touch? Can it change or delete things? When does its secret expire? How do we switch it off fast?

**Type words:** `AI coding agent` | `AI assistant/chatbot` | `Automation/bot` | `Service account` | `API key` | `Integration/webhook`
**Power words:** `Read only` | `Can write` | `Can delete` | `Can deploy to production` | `Can spend money`

| Agent ID | Name | Type | Who built or set it up | **Human Owner** (a real person) | System ID(s) it touches | Power (see words above) | Can it see customer data? (Y/N) | Where its secret is stored | Secret created | Rotate by (date) | Switch-off method | Risk (L/M/H) | Last review | Decision | Evidence link | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| N-001 | *Example:* Code assistant bot | AI coding agent | Jo Park | Sam Lee | S-002 (code repo) | Can write | N | Password manager, vault "Dev" | 2026-08-01 | 2026-11-01 | Revoke token in repo settings | Medium | 2026-10-17 | Keep | link | Active |
| N-002 | | | | | | | | | | | | | | | | |

### 7B. AI agent safety checklist (tick for each agent in 7A)
> **Question:** For every agent above, can you answer YES to each line?

| Check | N-001 | N-002 | N-003 |
|---|---|---|---|
| It has its own identity and secret (not borrowed from a person) | [ ] | [ ] | [ ] |
| It has a named human owner | [ ] | [ ] | [ ] |
| Its power is the smallest needed (see "Power" in 7A) | [ ] | [ ] | [ ] |
| It can NOT deploy to production without a human approval step | [ ] | [ ] | [ ] |
| Its secret is not in code, chat, or this file | [ ] | [ ] | [ ] |
| Its secret has a rotation date | [ ] | [ ] | [ ] |
| Its actions are logged and someone can look at the log | [ ] | [ ] | [ ] |
| Someone has tried the switch-off method and it worked | [ ] | [ ] | [ ] |
| Customer data is not sent to an outside AI service unless approved and listed in Section 2 | [ ] | [ ] | [ ] |
| Unused agents and keys have been removed | [ ] | [ ] | [ ] |

**Done when:** [ ] every bot, agent, service account and API key is listed, [ ] every one has a human owner, and [ ] any "No" above is in Section 11.

## 8. Exceptions and Temporary Access
> **Questions to answer:** Did anyone get extra access for a short time (emergency or special job)? When does it end? Who said yes?

**Rule:** Temporary access **must have an end date**. No end date = not temporary.

| Exception ID | Who (person or agent ID) | System ID | What extra access | Reason | Approved by | Start date | **End date** | Removed on (date) | Evidence link | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| E-001 | *Example:* Jo Park | S-001 | Admin on database | Urgent bug on launch day | Sam Lee | 2026-10-17 | 2026-10-18 | 2026-10-18 | ticket link | Removed |
| E-002 | | | | | | | | | | |

**Break-glass (emergency) use:** if emergency access is used, write who used it, when, why, and when it was switched off again.

## 9. Review Log
> **Question:** Every time you do a review, write one line here. This is your proof the reviews happened.

**Review types:** `Phase gate` | `Monthly` | `Event-based` (someone left, secret leaked, incident) | `Audit prep`

| Review ID | Date | Review type | Phase | Customer count | Reviewer | Rows checked (people / agents) | Keep | Reduce | Remove | Escalate | Findings opened | Evidence link | Reviewer signed |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R-001 | *Example:* 2026-10-17 | Phase gate | 2 Test | 0 | Alex Kim | 6 / 2 | 5 | 2 | 1 | 0 | 2 | folder link | Yes |
| R-002 | | | | | | | | | | | | | |

## 10. Joiner / Mover / Leaver (JML) Log
> **Questions to answer:** Who joined, changed role, or left? Did their access change **the same day**?

**Targets:** Joiners get only role-based access. Movers have old access removed within **3 working days**. Leavers lose **all** access within **1 working day** (same day for High risk).

| JML ID | Person | Event (Joiner / Mover / Leaver) | Event date | Access added | Access removed | Date access changed | Done within target? (Y/N) | Checked by | Evidence link |
|---|---|---|---|---|---|---|---|---|---|
| J-001 | *Example:* Jo Park | Leaver | 2026-10-10 | None | All (S-001, S-002) | 2026-10-10 | Y | Sam Lee | ticket link |
| J-002 | | | | | | | | | |

**Leaver checklist (tick for each leaver):**
- [ ] Cloud and server accounts disabled
- [ ] Code repository access removed
- [ ] Business tools (email, support, payments, analytics) removed
- [ ] Any AI agent or API key they created is reassigned to a new owner or removed
- [ ] Shared secrets they knew have been rotated
- [ ] Company devices and tokens returned

## 11. Findings and Fix Tracker
> **Questions to answer:** What went wrong or looked risky? Who will fix it? By when? Is it fixed?

**Severity:** `High` (fix within 1 day) | `Medium` (fix within 7 days) | `Low` (fix within 30 days)
**Status:** `Open` | `In progress` | `Fixed - waiting check` | `Closed` | `Accepted risk` *(needs Approver name and reason)*

| Finding ID | Date found | Found in (Review ID) | What is the problem? (plain words) | Related ID (A- / N- / S-) | Severity | Fix owner | Due date | Date fixed | Checked by | Status | Evidence link |
|---|---|---|---|---|---|---|---|---|---|---|---|
| F-001 | *Example:* 2026-10-17 | R-001 | Contractor had Admin on database but only needs View | A-001 | High | Sam Lee | 2026-10-18 | 2026-10-18 | Alex Kim | Closed | link |
| F-002 | | | | | | | | | | | |

**Done when:** [ ] every Escalate decision has a finding, and [ ] no High finding is open past its due date.

## 12. Phase Gate Checklists (Go / No-Go)
> **How to use:** Before you move to the next phase, tick every box for your **current** phase. If any box is not ticked, the answer is **No-Go**: fix it first, or write an Approver-signed exception in Section 8.

### Phase 1: Build (development)
- [ ] Sections 1-5 are filled in
- [ ] Every developer, AI coding agent and key is in Sections 6-7
- [ ] MFA is on for all cloud, code and AI accounts
- [ ] No real customer data is in development systems (use fake data)
- [ ] No secrets stored in code or chat
- **Gate decision:** Go / No-Go | **Approver:** | **Date:**

### Phase 2: Test
- [ ] Test and staging systems are listed in Section 5
- [ ] Testers have View/Edit only on test systems (not production)
- [ ] AI agents cannot reach production
- [ ] A full review (Sections 6-7) is done and logged in Section 9
- [ ] All High findings are closed
- **Gate decision:** Go / No-Go | **Approver:** | **Date:**

### Phase 3: Pre-launch
- [ ] Production systems are listed and each has a named Owner
- [ ] Production Admin/Owner access is limited to the fewest people (write the number: ___)
- [ ] Break-glass (emergency) access is set up, tested, and documented
- [ ] Every secret has a rotation date, and development secrets are NOT reused in production
- [ ] Logs are on for production access and AI agent actions
- [ ] Leaver and Mover steps (Section 10) are tested once
- [ ] Section 2 data types are confirmed with the Approver
- **Gate decision:** Go / No-Go | **Approver:** | **Date:**

### Phase 4: Launch
- [ ] Review done on launch day or the day before, and logged in Section 9
- [ ] All launch-day temporary access has an end date in Section 8
- [ ] AI agents with "Can deploy to production" need human approval
- [ ] Support staff can see only the customer data they need
- [ ] Monthly review reminder is set in the calendar
- **Gate decision:** Go / No-Go | **Approver:** | **Date:**

### Phase 5: Customers 1-500 (run monthly)
Repeat each month and also at **10, 100, 250 and 500 customers**.

| Customer milestone | Date reached | Review done (Review ID) | New systems / people / agents added since last review | All High findings closed? |
|---|---|---|---|---|
| 10 | | | | |
| 100 | | | | |
| 250 | | | | |
| 500 | | | | |

- [ ] All temporary access has expired and been removed
- [ ] Unused accounts (no activity in 30+ days) are removed or suspended
- [ ] All secrets past their rotation date have been replaced
- [ ] Customer-support and admin access to customer data is still the minimum
- [ ] Any incident in the month had an event-based review
- **After 500 customers:** hand this register to the ongoing security process and continue at least quarterly (some frameworks, such as PCI DSS, expect user-account reviews at least every 6 months; check yours).

## 13. Standards Mapping (for auditors)
> **Question:** Which official rule does each part of this document help to prove?
> *This is a general guide to help you explain your controls. Confirm exact requirements with your auditor or legal advisor, since versions and local laws change.*

| This document section | Helps show... | Framework area (typical) |
|---|---|---|
| Sections 5-6 (inventory, people access) | Access is given on a need-to-have basis | SOC 2 CC6.1-CC6.3; ISO 27001 Annex A 5.15, 5.18; PCI DSS Req. 7; HIPAA access control (45 CFR 164.312(a)) |
| Section 6 MFA columns | Strong sign-in for users | SOC 2 CC6.1; ISO 27001 Annex A 8.5; PCI DSS Req. 8 |
| Section 7 (AI agents, keys) | Machine and service accounts are controlled | SOC 2 CC6.1-CC6.2; ISO 27001 Annex A 5.16, 8.2 |
| Section 9 (review log) | Access is reviewed regularly | SOC 2 CC6.3; ISO 27001 Annex A 5.18; PCI DSS 7.2.4; HIPAA 164.308(a)(3)-(4) |
| Section 10 (JML) | Access removed when people leave or change roles | SOC 2 CC6.2-CC6.3; ISO 27001 Annex A 5.18 |
| Sections 2, 6 (data types, least privilege) | Only needed personal data is accessed | GDPR Art. 5(1)(c), 25, 32 |
| Section 11 (findings) | Problems are tracked and fixed | SOC 2 CC4.2; ISO 27001 clause 10.2 |

## 14. Final Sign-Off
> **Question:** Do you (the Owner), the Reviewer and the Approver all agree this register is complete and true?

| Role | Name | Statement | Signature or "I approve" message link | Date |
|---|---|---|---|---|
| Project Owner | | "I confirm this register is complete and accurate." | | |
| Reviewer | | "I checked the evidence and agree with the decisions." | | |
| Approver | | "I accept any remaining risks listed above." | | |

## 15. Is This Document Ready? (final self-check)
Answer **Yes / No** to each. Every answer must be **Yes** before you sign.

| # | Question | Yes / No |
|---|---|---|
| 1 | Can I name every system that holds our code, servers, data, AI tools and business tools? | |
| 2 | Can I name every person and every AI agent or key that can get into them? | |
| 3 | Does every row have a real owner, risk level and decision? | |
| 4 | Did I search this file for passwords, keys and tokens and find none? | |
| 5 | Are there any shared logins? (answer **Yes** only if none) | |
| 6 | Did everyone who left lose access on time (Section 10)? | |
| 7 | Do all temporary access rows have an end date, and are expired ones removed? | |
| 8 | Is every High finding closed or formally accepted? | |
| 9 | Did the Reviewer see real evidence for High-risk rows? | |
| 10 | Is the next review date in my calendar and written in Section 1? | |

---
*End of template. Copy this file for each new project, rename it `Access_Review_Register_[ProjectName].md`, and keep the original unchanged.*
