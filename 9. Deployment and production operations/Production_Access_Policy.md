# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

This is a **Production Access Policy template**. It decides **who is allowed to touch your live product, how, when, and who checks on them.** "Production" means the real, live version of your product that real customers use.

You can reuse this file for any project. Copy it, fill it in, save it as `Production_Access_Policy.md` in your project's **Deployment and production operations** folder.

## The 6 steps

1. **Copy** this file into your new project. Never fill in the original template.
2. **Read each question** (marked `Q`). Each question has a plain-language explanation.
3. **Tick one answer** by changing `[ ]` to `[x]`. Pick only one unless it says "pick all that apply".
4. **Not sure? Pick the answer marked ⭐.** That is the safe default.
5. **Type your own answers** wherever you see `➤ FILL:`. Replace everything after the colon. Look at the `📝 Example` to see what a good answer looks like.
6. **Finish with the checklist** in Part 20. If any box is unticked, the document is not done.

## Symbols used in this document

| Symbol | Meaning |
|---|---|
| `[ ]` / `[x]` | Empty / ticked checkbox |
| ⭐ | Recommended default. Pick it if you are unsure |
| `➤ FILL:` | You must type an answer here |
| 📝 Example | A sample answer. Do not copy it blindly; replace it with your own |
| 🔒 FIXED RULE | A rule that applies to everyone on every project. Do not edit it |
| 🧩 OPTIONAL | You may mark it `N/A` and write why. Never delete a section |
| ⚠️ | Pay extra attention |

## Golden rules for filling this in

- **Never write a password, API key, token, or secret in this file.** Write where it is stored (for example "in our password manager"), never what it is.
- **Never leave a `➤ FILL:` blank.** If it truly does not apply, write `N/A - because [reason]`.
- **Use real names or role titles**, not "the team" or "someone".
- **If you do not know an answer, write `UNKNOWN - [name] will find out by [date]`.** Do not guess.
- **Dates use the format `YYYY-MM-DD`** (for example 2026-10-18).
- This document is **not legal advice.** If you handle health, payment or personal data, have a qualified professional review Part 18.

## Tiny glossary (words used below)

| Word | Simple meaning |
|---|---|
| **Production (prod)** | The live product real customers use |
| **Staging** | A practice copy of production used for testing before launch |
| **Access** | Being able to see or change something |
| **Least privilege** | Give people only the access they need, nothing extra |
| **MFA** | Multi-factor authentication: a password plus a second proof, like a phone code or security key |
| **Break-glass** | Emergency access used only when something is badly broken |
| **Secret** | A password, API key, token, or certificate |
| **Audit log** | A diary that records who did what and when, which cannot be edited |
| **PII** | Personal information that identifies a person (name, email, phone) |
| **PHI** | Health information |
| **Cardholder data** | Credit or debit card details |
| **AI agent** | An AI program that can take actions, not just chat |
| **Owner** | The person responsible for the project |

---

# DOCUMENT CONTROL

| Field | Answer |
|---|---|
| Project name | ➤ FILL: |
| Product name (customer-facing) | ➤ FILL: |
| Policy owner (name + role) | ➤ FILL: |
| Backup owner (name + role) | ➤ FILL: |
| Document version | ➤ FILL: `1.0` |
| Date created | ➤ FILL: |
| Last reviewed | ➤ FILL: |
| Next review due | ➤ FILL: (⭐ 90 days after the last review) |
| Status | `[ ]` Draft  `[ ]` In review  `[ ]` Approved |

📝 Example: Project name: `Acme Notes` · Policy owner: `Sam Lee, Founder` · Next review due: `2027-01-16`

---

# PART 1: PROJECT PROFILE

*Why this matters: the answers here decide how strict the rest of the document must be.*

### Q1.1 How many people can reach production today?
- `[ ]` ⭐ 1 to 5 people
- `[ ]` 6 to 25 people
- `[ ]` More than 25 people

➤ FILL: Exact number now: ______   Expected number at 500 customers: ______

### Q1.2 Where does your product live? (pick all that apply)
- `[ ]` AWS
- `[ ]` Google Cloud (GCP)
- `[ ]` Microsoft Azure
- `[ ]` Platform service (for example Vercel, Supabase, Render, Netlify, Heroku, Firebase)
- `[ ]` Other: ➤ FILL:

### Q1.3 What kinds of data does your product hold? (pick all that apply)
- `[ ]` No personal data at all
- `[ ]` Basic personal data (names, emails, phone numbers)
- `[ ]` Sensitive personal data (location, IDs, private messages, children's data)
- `[ ]` Health data (PHI)
- `[ ]` Payment card data
- `[ ]` Business secrets or customer files

⚠️ If you ticked **Health** or **Payment card**, Part 8 and Part 18 are **mandatory**, not optional.

### Q1.4 Which rules must you follow? (pick all that apply)
- `[ ]` None required yet, good practice only
- `[ ]` SOC 2
- `[ ]` ISO 27001
- `[ ]` GDPR or other privacy laws (for example UK GDPR, CCPA/CPRA)
- `[ ]` HIPAA
- `[ ]` PCI-DSS
- `[ ]` Other: ➤ FILL:

### Q1.5 Which life-cycle phase is the project in right now?
- `[ ]` Phase A: Build and staging (nothing is live)
- `[ ]` Phase B: Launch day
- `[ ]` Phase C: Early users (1 to 100 customers)
- `[ ]` Phase D: Growth (100 to 500 customers)
- `[ ]` Past 500 customers (review this document fully, then update it)

➤ FILL: Planned launch date: ______   Current number of customers: ______

### Q1.6 Do AI agents work on this project?
- `[ ]` No
- `[ ]` Yes, as coding helpers only (they never touch live systems)
- `[ ]` Yes, some AI agents can reach staging or production (fill in Part 9)

---

# PART 2: THE UNBREAKABLE RULES 🔒

These apply to **every project, every person, every AI agent, every phase.** They are not questions. Do not edit them.

1. **Least privilege.** Everyone gets the smallest access that lets them do their job.
2. **One person, one account.** No shared logins. No shared passwords. Ever.
3. **MFA is required** for every account that can reach production, with no exceptions.
4. **Access has a reason.** Every grant has a written reason, an approver, and an end date (except the standing roles in Part 5).
5. **Everything is logged.** Production access is recorded, and the log cannot be edited by the people it records.
6. **Secrets stay out of code and chat.** Passwords and keys live only in an approved secrets tool.
7. **Test first.** Changes go to staging before production, unless it is a declared emergency (Part 11).
8. **Real customer data is protected by default.** Seeing it needs a reason and approval (Part 8).
9. **AI agents are treated like people with a badge.** They get their own identity, minimum access, and logs (Part 9).
10. **Remove access fast.** When someone leaves or changes role, access is removed the same day.
11. **Review regularly.** Access lists are checked on a fixed schedule (Part 14).
12. **Report mistakes quickly and without blame.** Reporting early is rewarded; hiding is the real violation.

---

# PART 3: WHO IS WHO

*Why this matters: when something goes wrong, everyone must know who decides.*

### Q3.1 Fill in the people and their roles

| Role | What this person does | Name | Contact (email/phone) |
|---|---|---|---|
| **Project Owner** | Final say on all access decisions | ➤ FILL: | ➤ FILL: |
| **Access Approver** | Says yes or no to access requests | ➤ FILL: | ➤ FILL: |
| **Backup Approver** | Approves when the first approver is away | ➤ FILL: | ➤ FILL: |
| **Security Contact** | Receives security worries and incident reports | ➤ FILL: | ➤ FILL: |
| **On-call Engineer** | First responder for live problems | ➤ FILL: | ➤ FILL: |
| **Privacy / Data Contact** | Handles customer data questions and legal notices | ➤ FILL: | ➤ FILL: |

📝 Example: Access Approver: `Maya Chen` · `maya@acme.com` · Backup: `Sam Lee`

### Q3.2 How is approval handled on this project?
- `[ ]` ⭐ **A second person always approves.** Nobody approves their own access. *(Use this whenever there are 2 or more people.)*
- `[ ]` **Solo exception.** There is only one person. They may approve their own access, but they **must write it in the Access Log (Part 13)** with a reason and review it monthly.
- `[ ]` Other: ➤ FILL:

⚠️ Solo teams: find one trusted outsider (a friend, advisor, or contractor) who reviews your access log once per month. Name them: ➤ FILL:

---

# PART 4: WHAT NEEDS PROTECTING (SYSTEM INVENTORY)

*Why this matters: you cannot protect what you have not listed.*

### Q4.1 List every system where live work happens

| System | What it holds or does | Where it runs | Owner | Sensitivity (Low / Medium / High) |
|---|---|---|---|---|
| ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: |

📝 Example:

| System | What it holds | Where | Owner | Sensitivity |
|---|---|---|---|---|
| Customer database | Names, emails, notes | Supabase | Maya | High |
| Web app hosting | The live website | Vercel | Sam | Medium |
| Payment provider dashboard | Subscriptions | Stripe | Sam | High |
| Error tracking | Crash reports | Sentry | Maya | Low |
| Domain and DNS | Our web address | Cloudflare | Sam | High |
| Code repository | Source code | GitHub | Sam | High |

⚠️ Add these often-forgotten items: **domain/DNS, email sending service, backups, CI/CD pipeline, secrets tool, analytics, customer support tool.**

### Q4.2 Where do backups live and who can reach them?
➤ FILL:

---

# PART 5: ACCESS LEVELS (WHO CAN DO WHAT)

*Why this matters: instead of deciding each person from scratch, use ready-made levels.*

### The five levels 🔒

| Level | Name | What it allows | Typical person |
|---|---|---|---|
| **L0** | No access | Cannot see production | Most people, interns |
| **L1** | View only | See dashboards, logs and metrics. No customer data. No changes | Designers, product, QA, support |
| **L2** | Operate | Restart services, view detailed logs, deploy through the approved pipeline | Developers, on-call engineers |
| **L3** | Data access | See or change real customer data (needs a reason, Part 8) | Support lead, database admin |
| **L4** | Admin | Change permissions, billing, networking, security settings | Project owner, one backup |

### Q5.1 Fill in who holds each level right now

| Person / account | Level | Systems | Reason | Approved by | Start date | End date |
|---|---|---|---|---|---|---|
| ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: |

📝 Example: `Jo Park` · `L2` · `Web hosting, error tracking` · `Developer on call` · `Maya Chen` · `2026-11-01` · `2027-01-31`

### Q5.2 How many people may hold L4 (Admin)?
- `[ ]` ⭐ Exactly 2 (one main, one backup)
- `[ ]` 1 (solo project; you are the backup risk, so write down a recovery plan in Part 11)
- `[ ]` Other: ➤ FILL: *(⚠️ keep it as small as possible)*

### Q5.3 Standing access vs. temporary access
- `[ ]` ⭐ **L0 to L2 may be standing** (stays until reviewed). **L3 and L4 must be temporary** whenever the tools allow it, so access switches on for a few hours and then expires on its own.
- `[ ]` All access is temporary
- `[ ]` Other: ➤ FILL:

**Default time limits ⭐**: L3 up to 8 hours · L4 up to 4 hours · emergency up to 4 hours. ➤ FILL (only if you change them): ______

---

# PART 6: ASKING FOR AND GRANTING ACCESS

*Why this matters: no "just give me the password" moments.*

### Q6.1 Where do access requests go?
- `[ ]` Ticket or issue tracker: ➤ FILL: (link)
- `[ ]` A form: ➤ FILL: (link)
- `[ ]` Email to the Access Approver
- `[ ]` Chat message, **and** the approver writes it in the Access Log

### Q6.2 Every request must contain these 7 things 🔒
1. Who needs access (name, role)
2. Which system
3. Which level (L1 to L4)
4. Why (the task or ticket number)
5. For how long (end date or hours)
6. Who is the backup if this person is away
7. Confirmation that they have MFA turned on

### Q6.3 How fast should requests be answered?
- `[ ]` ⭐ Within 1 working day (L1 and L2), 4 working hours (L3 and L4)
- `[ ]` Other: ➤ FILL:

### Q6.4 The 6-step grant process 🔒
1. Person submits a request with the 7 items above.
2. Approver checks: *Is the reason real? Is this the lowest level that works? Is the end date set?*
3. Approver says **Approved** or **Denied** in writing.
4. An admin grants the access, exactly as approved.
5. The grant is written in the **Access Log** (Part 13).
6. Access ends on the end date and is removed or confirmed during the next review (Part 14).

### Q6.5 When must a request be denied?
Deny and ask for changes when: the reason is vague, the level is higher than needed, there is no end date, MFA is not on, or the requester is not on the approved people list.

---

# PART 7: SIGNING IN SAFELY

### Q7.1 Which MFA methods are allowed?
- `[ ]` ⭐ Authenticator app or passkey for everyone. **Hardware security key for L4 (Admin).**
- `[ ]` Hardware security key for everyone
- `[ ]` Authenticator app or passkey for everyone (no keys)
- ⚠️ **Not allowed:** SMS-only codes for Admin accounts. Shared phones. No MFA.

### Q7.2 Single sign-on (one login for many tools)
- `[ ]` ⭐ We use SSO through: ➤ FILL: (for example Google Workspace, Okta, AWS IAM Identity Center, Microsoft Entra ID)
- `[ ]` Not yet; each tool has its own login (add "set up SSO" to the roadmap before 100 customers)

### Q7.3 Passwords 🔒
- Use a **password manager** for every password.
- Passwords are long (at least 14 characters, ideally a passphrase) and **unique**.
- Never reuse a password from another site.
- Change a password immediately if it may have leaked.

Password manager used: ➤ FILL:

### Q7.4 Device rules (pick all that apply)
- `[ ]` Disk encryption turned on
- `[ ]` Screen lock after 5 minutes or less
- `[ ]` Operating system and browser kept up to date
- `[ ]` Company-approved devices only for L3 and L4
- `[ ]` No production access on public or shared computers
- `[ ]` Other: ➤ FILL:

### Q7.5 Special accounts
- **Root / owner accounts** (cloud "root", domain registrar owner, payment owner): locked away, MFA on, used **only** to create other admins or recover access. Never for daily work. Who holds them: ➤ FILL:
- **Service accounts / machine accounts** (for programs, not people): see Part 12.

---

# PART 8: CUSTOMER DATA ACCESS

*Why this matters: customer trust and the law. Looking at a customer's data is a big deal.*

### Q8.1 Default rule 🔒
Real customer data is **blocked by default.** To see it, a person must have: **(1) a written reason, (2) approval, (3) an end time.** Everything they view is logged.

### Q8.2 When is it OK to view real customer data? (pick all that apply)
- `[ ]` The customer asked for help with their own account
- `[ ]` Fixing a bug that cannot be reproduced without it
- `[ ]` A legal or security investigation
- `[ ]` Fulfilling a customer's data request (copy, correction, deletion)
- `[ ]` Other: ➤ FILL:
- ⚠️ **Never OK:** curiosity, looking up friends, family or celebrities, selling or sharing data, copying it to personal devices or chat.

### Q8.3 Protecting the data when people must work with it
- `[ ]` ⭐ Use **masked or fake data** in staging and development. Real data never goes to staging.
- `[ ]` Hide sensitive fields (card numbers, health notes) even from people with L3 unless they are essential
- `[ ]` Downloads and exports of customer data are blocked unless approved
- `[ ]` Support tools show only the fields needed

### Q8.4 If you ticked Health data (PHI) in Q1.3 🧩
- `[ ]` Each person has a unique user ID (no shared logins)
- `[ ]` A written emergency access procedure exists (Part 11)
- `[ ]` Access to PHI is logged, and the logs are reviewed on a schedule (Part 13)
- `[ ]` Documentation is kept for **6 years**
- `[ ]` Business associate agreements are signed with vendors who touch PHI: ➤ FILL: (list)

### Q8.5 If you ticked Payment card data in Q1.3 🧩
- `[ ]` ⭐ Card details are handled by a payment provider (such as Stripe), so **our systems never store card numbers**
- `[ ]` Anyone with access to the card environment uses MFA
- `[ ]` Card-environment access is limited to need-to-know
- `[ ]` User accounts for the card environment are reviewed at least every **6 months**
- `[ ]` Logs are kept 12 months, with the last 3 months immediately available

### Q8.6 If a privacy law applies (GDPR, CCPA) 🧩
- Privacy contact: ➤ FILL:
- If personal data is exposed by mistake, report it to the Security Contact **right away.** Under GDPR, the authority usually must be told **within 72 hours** of becoming aware of a breach. The Privacy contact decides, but the clock starts when anyone on the team learns of it.
- How customers send data requests: ➤ FILL: (email or form)

---

# PART 9: AI AGENT ACCESS 🧩

*Why this matters: AI agents can act fast and make confident mistakes. Give them a small, safe lane.*

*If you answered "No" in Q1.6, write `N/A - no AI agents` here and skip to Part 10.*

### 🔒 FIXED RULES for AI agents
1. Every AI agent has **its own identity.** It never uses a person's login or personal key.
2. **Least privilege** applies. The agent gets only the access its task needs.
3. Its credentials are **short-lived** and stored in the secrets tool, never typed into prompts or code.
4. **Every action is logged,** with which agent, which task, and who started it.
5. A **named human owner** is responsible for each agent.
6. AI agents **never** approve their own access or another agent's access.
7. AI agents **never** see raw customer data unless Part 8 is followed and the owner approved it.
8. **Delete, destroy, payment, permission change and customer-message actions always need a human to confirm first,** no matter the tier.
9. Treat anything an agent reads (web pages, emails, tickets, files) as **untrusted**. It could contain hidden instructions. The agent must not follow those without human approval.
10. There is a **kill switch**: a way to stop the agent and revoke its access in under 5 minutes.

### Q9.1 Choose the tier for each AI agent

| Tier | What the agent may do | Human involvement |
|---|---|---|
| **T0: No access** | Works only on code and documents. Cannot reach live systems | None needed |
| **T1: Read-only** | Reads logs, metrics, dashboards. Cannot change anything. No raw customer data | Owner reviews monthly |
| **T2: Suggest + staging** | Full access to staging. In production it can only *propose* changes | A human approves every production change |
| **T3: Limited production actions** | Runs a short list of approved, reversible actions in production (for example restart a service, roll back a release) | Human approves in advance; every action is logged; an alert is sent |
| **T4: Autonomous** | Acts in production on its own within strict limits | ⚠️ Only after 500 customers *and* after written approval from the Project Owner and Security Contact *and* a 30-day trial at T3. Not allowed before then |

⭐ **Default for every agent: T1 or T2. Anything higher needs a written reason.**

### Q9.2 Register every AI agent

| Agent name | Purpose | Tier (T0-T4) | Systems it can reach | Human owner | Credential type and expiry | Approved on |
|---|---|---|---|---|---|---|
| ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: |

📝 Example: `LogHelper` · `Reads error logs and summarizes them` · `T1` · `Sentry (read only)` · `Maya Chen` · `Short-lived token, 8 hours` · `2026-11-02`

### Q9.3 Guard rails (pick all that apply)
- `[ ]` Agent actions are rate-limited (maximum actions per hour: ➤ FILL:)
- `[ ]` Agents work in a sandbox or staging first
- `[ ]` Agents have a spending limit: ➤ FILL:
- `[ ]` Agents' prompts and tool lists are saved in version control
- `[ ]` Changes to an agent's permissions follow the same request process as people (Part 6)
- `[ ]` A human reads a weekly summary of what each agent did
- `[ ]` Agents cannot disable logging, alerts or their own limits

### Q9.4 What happens when an agent misbehaves?
1. Stop the agent (kill switch). 2. Revoke its credentials. 3. Tell the Security Contact. 4. Review the logs. 5. Fix and write down what was learned.
Who can press the kill switch: ➤ FILL:

---

# PART 10: RULES FOR EACH PHASE (DEVELOPMENT TO FIRST 500 CUSTOMERS)

*Why this matters: a product with 5 customers needs different care than one with 500.*

Fill in only your **current** phase now and the **next** one. Come back to fill the others later. Move up a phase only when its exit checklist is done.

### PHASE A: BUILD AND STAGING (nothing is live)

**Goal:** Build safely. Practice before it counts.

| Rule | Default ⭐ |
|---|---|
| Production environment exists? | Create it empty, with Admin access locked to 2 people |
| Real customer data allowed in staging? | **No.** Use fake or masked data |
| Who can reach staging? | Developers and AI agents up to T2 |
| Who can reach production? | L4 only (project owner and backup) |
| Secrets | Separate secrets for staging and production, kept in a secrets tool |
| Logging | Turn on audit logs now, before launch |

➤ FILL: People with staging access: ______
➤ FILL: People with production access: ______

**Exit checklist (to move to Phase B):**
- `[ ]` Parts 1 to 9 of this policy are filled in
- `[ ]` MFA is on for every account
- `[ ]` Audit logging is on and tested (do a test action and find it in the log)
- `[ ]` Backups exist and a restore has been tested
- `[ ]` Emergency access is set up and tested (Part 11)
- `[ ]` No secrets in code (run a secret scan)
- `[ ]` Launch roles are assigned (below)

### PHASE B: LAUNCH DAY

**Goal:** Go live calmly, with extra eyes on it and a clear way back.

| Rule | Default ⭐ |
|---|---|
| Launch window | Choose a time when the team is awake and available (not Friday night) |
| Extra access | Temporary L2 for named launch helpers, ending **48 hours after launch** |
| Production changes | Only through the approved pipeline; one person deploys, a second watches |
| Rollback | Written plan and tested before the launch |
| Admin access | Still limited to 2 people |
| AI agents | Maximum T2; no autonomous actions on launch day |
| Communication | One channel for launch issues; one person speaks to customers |

➤ FILL: Launch date and time: ______
➤ FILL: Launch commander (decides go/stop): ______
➤ FILL: Rollback owner: ______
➤ FILL: Where the launch log is kept: ______

**Exit checklist (to move to Phase C):**
- `[ ]` All temporary launch access was removed and logged
- `[ ]` Launch review held within 3 days; problems written down
- `[ ]` No unexplained entries in the audit log
- `[ ]` Monitoring and alerts are working

### PHASE C: EARLY USERS (1 TO 100 CUSTOMERS)

**Goal:** Fix problems quickly without leaving the doors open.

| Rule | Default ⭐ |
|---|---|
| Access review | **Monthly** |
| Customer data viewing | Request, reason, approval, expiry (Part 8). Never "always on" |
| Support access | L1 plus the ability to see a single customer's record after approval |
| Hotfixes | Allowed through the pipeline with one reviewer; write a short note afterwards |
| Access Log check | Owner (or outside reviewer for solo projects) reads it monthly |
| SSO | Set up before reaching 100 customers |
| Vendor review | List every service that holds customer data (Part 16) |

➤ FILL: Support person(s): ______
➤ FILL: Date of the first monthly review: ______

**Exit checklist (to move to Phase D):**
- `[ ]` Three monthly reviews done and recorded
- `[ ]` Every person's access level was re-confirmed
- `[ ]` At least one emergency access drill held (Part 11)
- `[ ]` Secrets rotated at least once
- `[ ]` SSO live (or exception written down)

### PHASE D: GROWTH (100 TO 500 CUSTOMERS)

**Goal:** Grow without growing risk. Move from "everybody knows everybody" to "the process protects us."

| Rule | Default ⭐ |
|---|---|
| Access review | Monthly until 500, then every **quarter** |
| Separation of duties | The person who writes a change should not be the only one to approve and deploy it to production |
| Roles | Split the Admin role from the day-to-day roles; name an official Security Contact |
| New hires and contractors | Follow the joiner process (Part 15) with a written onboarding checklist |
| AI agents | T3 allowed with written approval; T4 only if Part 9 conditions are met |
| Evidence | Keep screenshots or exports of reviews and approvals (for SOC 2 / ISO 27001) |
| Incident practice | Run a tabletop exercise (talk through a made-up incident) every 6 months |

➤ FILL: Date this phase starts: ______
➤ FILL: Planned date for the 500-customer review of this policy: ______

**Exit checklist (at 500 customers):**
- `[ ]` Full review of this document done
- `[ ]` Access list compared with real staff list
- `[ ]` Roles, limits and tiers updated for the next growth stage
- `[ ]` Compliance gaps listed with owners and dates (Part 18)
- `[ ]` Policy version number increased and approved

---

# PART 11: EMERGENCY ACCESS ("BREAK-GLASS") 🧩

*Why this matters: when the site is down at 3 a.m., waiting for permission can cost customers. This lets you move fast and clean up afterward.*

### Q11.1 When can emergency access be used?
Only when **all** are true:
- Customers are being harmed now (outage, data exposure, security attack) **or** are about to be.
- Normal access is too slow or unavailable.
- A person has the skills to fix it.

### Q11.2 How emergency access works 🔒
1. Person declares an emergency in: ➤ FILL: (channel or phone)
2. They use the pre-built emergency account or role: ➤ FILL: (name, where the credentials are kept)
3. Time limit ⭐ **4 hours.** Extend only with a named approver's word.
4. Every action is logged automatically.
5. Alert goes to: ➤ FILL: (Project Owner and Security Contact) the moment emergency access is used.
6. The person writes a short report **within 24 hours** (what happened, what was done, what was touched).
7. The Project Owner or Security Contact **reviews it within 72 hours** ⭐ and signs off.
8. Emergency credentials are **changed after every use.**

### Q11.3 Where are the emergency credentials stored?
- `[ ]` Sealed in the password manager, with alerts on opening
- `[ ]` Printed copy in a locked place: ➤ FILL: (where)
- `[ ]` Other: ➤ FILL:

### Q11.4 Solo project recovery plan
If you are the only admin and lose access: ➤ FILL: (who can help, which recovery codes exist, where they are kept)

### Q11.5 Practice
Test emergency access: `[ ]` ⭐ every 6 months  `[ ]` every year  Last test: ➤ FILL: ______

---

# PART 12: SECRETS, KEYS AND MACHINE ACCOUNTS

### Q12.1 Where do secrets live?
➤ FILL: Approved secrets tool(s): ______
📝 Example: `1Password for people, AWS Secrets Manager for programs`

### Q12.2 Rules 🔒
- Secrets **never** go in code, chat, email, tickets, screenshots or this document.
- Staging and production use **different** secrets.
- Prefer **short-lived** credentials over long-lived keys.
- Each program or AI agent has its **own** machine account with minimal permissions.
- Turn on secret scanning in your code host and fix any alert at once.
- If a secret is exposed: **treat it as stolen.** Rotate it immediately and tell the Security Contact.

### Q12.3 How often do you change (rotate) secrets?
- `[ ]` ⭐ Every 90 days for long-lived keys, **and** immediately after a person with access leaves or a leak is suspected
- `[ ]` Every 180 days
- `[ ]` Other: ➤ FILL:

### Q12.4 Machine accounts list

| Account | Used by | Permissions | Owner | Rotation date |
|---|---|---|---|---|
| ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: | ➤ FILL: |

---

# PART 13: LOGGING, WATCHING AND RECORD KEEPING

### Q13.1 What must be logged? (all required 🔒)
- Logins and failed logins
- Access grants, changes and removals
- Every action by Admin accounts
- Every view or export of real customer data
- Every emergency access use
- Every AI agent action in production
- Changes to logging settings themselves

### Q13.2 Where are logs kept?
➤ FILL: (for example CloudTrail, Google Cloud Audit Logs, Azure Activity Log, platform audit log)

### Q13.3 Who can edit or delete logs?
⭐ **Nobody on the day-to-day team.** Logs go to a place the people being logged cannot change. ➤ FILL: Who holds log admin rights: ______

### Q13.4 How long are logs and access records kept?
- `[ ]` ⭐ **1 year** (3 months easily searchable)
- `[ ]` 2 years
- `[ ]` 6 years (use if HIPAA documentation applies)
- `[ ]` Other: ➤ FILL:

⚠️ If GDPR applies, do not keep personal information in logs longer than needed.

### Q13.5 Alerts: tell someone when:
- `[ ]` An Admin signs in
- `[ ]` Emergency access is used
- `[ ]` Many failed logins happen
- `[ ]` Someone signs in from an unusual place or device
- `[ ]` Access is granted outside the normal process
- `[ ]` Logging is turned off
- `[ ]` An AI agent acts outside its list

➤ FILL: Alerts go to: ______

### Q13.6 The Access Log (copy this table into a sheet or keep it here)

| Date | Person / agent | System | Level | Reason / ticket | Approved by | Start | End | Removed on |
|---|---|---|---|---|---|---|---|---|
| ➤ FILL: | | | | | | | | |

➤ FILL: If the Access Log lives somewhere else, link: ______

### Q13.7 Who reads the logs, and how often?
➤ FILL: Name: ______   `[ ]` ⭐ Weekly skim  `[ ]` Monthly deep check

---

# PART 14: REGULAR ACCESS REVIEWS

*Why this matters: access quietly piles up. Reviews clean it out.*

### Q14.1 How often?
- `[ ]` ⭐ **Monthly** in Phases B, C, and D; **quarterly** once past 500 customers
- `[ ]` Quarterly only
- `[ ]` Other: ➤ FILL:

### Q14.2 The review in 5 steps 🔒
1. Export the list of everyone (people, AI agents, machine accounts) with production access.
2. Compare it with the current team list and the Access Log.
3. For each entry ask: *Still employed or active? Still needs it? Is the level the lowest that works? Has it expired?*
4. Remove or lower anything that fails.
5. Sign and date the review below.

### Q14.3 Review record

| Review date | Reviewer | Entries checked | Removed / lowered | Problems found | Signed |
|---|---|---|---|---|---|
| ➤ FILL: | | | | | |

---

# PART 15: JOINING, MOVING AND LEAVING

### Q15.1 When someone joins 🔒
1. Create their own account (no sharing).
2. Turn on MFA before anything else.
3. Give **L0 or L1** to start; higher levels follow the request process (Part 6).
4. They read and acknowledge this policy (Part 20).
5. Record it in the Access Log.

### Q15.2 When someone changes role
Remove access they no longer need **first**, then request the new access. ⭐ Do this within 1 working day.

### Q15.3 When someone leaves 🔒
- `[ ]` ⭐ **Remove all access the same day** (within 24 hours at most; immediately if the exit is unfriendly)
- Checklist: SSO account · cloud console · code host · database · secrets tool · password manager shared folders · domain/DNS · payment dashboard · support tool · analytics · API keys they created · devices returned.
- Rotate any shared or long-lived secret they knew.
- Record the removal in the Access Log.

➤ FILL: Who runs the leaver checklist: ______

### Q15.4 Contractors and temporary workers
- `[ ]` ⭐ Same rules as employees, plus: a fixed end date, named sponsor, signed confidentiality agreement, and L2 maximum unless the Project Owner approves more
- `[ ]` Other: ➤ FILL:

---

# PART 16: VENDORS AND OUTSIDE SERVICES

### Q16.1 List every outside service that can reach production or customer data

| Vendor | What they can reach | Why | Contract / privacy agreement signed? | Security proof (SOC 2 / ISO report) checked? | Owner |
|---|---|---|---|---|---|
| ➤ FILL: | ➤ FILL: | ➤ FILL: | `[ ]` Yes `[ ]` No | `[ ]` Yes `[ ]` No | ➤ FILL: |

### Q16.2 Rules 🔒
- No vendor gets access without the same request and approval steps as a person.
- Vendor logins are named and have MFA.
- Vendors get the lowest level and an end date.
- Check vendors once a year.

---

# PART 17: BREAKING THE RULES AND ASKING FOR EXCEPTIONS

### Q17.1 What happens if someone breaks this policy?
- Honest mistakes reported quickly: **learn, fix, no blame.**
- Hiding a problem, sharing logins, or misusing customer data: access removed immediately and consequences set by the Project Owner (up to ending employment or contract, and legal action where the law requires).

### Q17.2 Asking for an exception
An exception needs: **what, why, how long (max 90 days ⭐), who approves, how risk is reduced.** The Project Owner and Security Contact must both approve. The exception is logged and reviewed at the next access review.

| Exception | Reason | Approved by | Expires | Risk reducers |
|---|---|---|---|---|
| ➤ FILL: or `None` | | | | |

### Q17.3 If you suspect a security problem
Tell the Security Contact **at once** by: ➤ FILL: (phone or channel). Do not wait. Do not delete evidence.

---

# PART 18: COMPLIANCE CROSSWALK 🧩

*Why this matters: shows which parts of this document help with each rule. This is a helper, not legal advice. Check the current version of each standard and ask a qualified expert before relying on it.*

| Topic | Where covered here | SOC 2 (Trust Services Criteria) | ISO/IEC 27001:2022 (Annex A) | PCI DSS v4.x | HIPAA Security Rule | GDPR |
|---|---|---|---|---|---|---|
| Who can access what | Parts 3, 5, 6 | CC6.1, CC6.2, CC6.3 | A.5.15, A.5.18 | Req. 7 | §164.312(a), §164.308(a)(4) | Art. 5(1)(f), Art. 32 |
| Unique accounts, MFA | Part 7 | CC6.1 | A.5.16, A.5.17, A.8.5 | Req. 8 | §164.312(a)(2)(i), §164.312(d) | Art. 32 |
| Admin / privileged rights | Parts 5, 11 | CC6.1, CC6.3 | A.8.2 | Req. 7, Req. 8 | §164.308(a)(3) | Art. 32 |
| Emergency access | Part 11 | CC7.4 | A.5.24 – A.5.26 | Req. 12.10 | §164.312(a)(2)(ii) | Art. 32 |
| Logging and monitoring | Part 13 | CC7.2 | A.8.15, A.8.16 | Req. 10 | §164.312(b) | Art. 32 |
| Access reviews | Part 14 | CC6.2, CC6.3 | A.5.18 | Req. 7.2.4 | §164.308(a)(4) | Art. 32 |
| Leavers and role changes | Part 15 | CC6.2, CC6.3 | A.5.18, A.6.5 | Req. 8.2 | §164.308(a)(3)(ii)(C) | Art. 32 |
| Vendors | Part 16 | CC9.2 | A.5.19 – A.5.22 | Req. 12.8 | §164.308(b) | Art. 28 |
| Breach reporting | Parts 8.6, 17.3 | CC7.3, CC7.4 | A.5.24 – A.5.26 | Req. 12.10 | §164.404 – §164.408 | Art. 33, Art. 34 |
| Record keeping | Part 13.4 | CC7.2 | A.8.15 | Req. 10.5 | §164.316(b) | Art. 5(2) |

➤ FILL: Rules that apply to this project (from Q1.4): ______
➤ FILL: Gaps we know about, with owner and date: ______

---

# PART 19: TOOL-SPECIFIC SETUP NOTES 🧩

*Tick the platforms you use in Q1.2. Each item is a "do it" checklist. Menu names may change over time; check your provider's current documentation.*

### AWS
- `[ ]` Lock the **root account** (MFA, no access keys, no daily use)
- `[ ]` Use **IAM Identity Center (SSO)** and roles instead of long-lived user keys
- `[ ]` Separate **accounts** for staging and production
- `[ ]` Turn on **CloudTrail** in all regions, stored in a protected bucket
- `[ ]` Use **temporary role access** (assume-role) for L3 and L4
- `[ ]` Turn on alerts (GuardDuty, IAM Access Analyzer, billing alerts)
- `[ ]` Give AI agents their own **IAM role** with limited permissions

### Google Cloud
- `[ ]` Separate **projects** for staging and production
- `[ ]` Use groups and **IAM roles**, not owner permission for everyone
- `[ ]` Turn on **Cloud Audit Logs** (including data access logs where needed)
- `[ ]` Prefer **service account impersonation / short-lived tokens** over downloaded key files
- `[ ]` Use Organization Policies to block risky actions (public storage, key creation)
- `[ ]` Give AI agents their own **service account**

### Microsoft Azure
- `[ ]` Use **Entra ID** with MFA and **Conditional Access**
- `[ ]` Separate **subscriptions or resource groups** for staging and production
- `[ ]` Use **Privileged Identity Management (PIM)** for just-in-time admin access
- `[ ]` Turn on the **Activity Log** and send to a protected workspace
- `[ ]` Use **managed identities** for programs and AI agents

### Platform services (Vercel, Supabase, Render, Netlify, Firebase and similar)
- `[ ]` Turn on MFA for every team member and **require it** if the platform allows
- `[ ]` Use **team roles** (not one shared owner login)
- `[ ]` Keep staging and production as **separate projects**
- `[ ]` Never expose admin or service-role keys in front-end code
- `[ ]` Turn on database access rules (for example row-level security) and test them
- `[ ]` Check audit log availability on your plan; if missing, record changes in the Access Log
- `[ ]` Use platform-provided tokens with the smallest scope for AI agents

### Source code and deployment pipeline (all projects)
- `[ ]` Protected main branch; changes need review
- `[ ]` Only the pipeline deploys to production (no manual uploads)
- `[ ]` Secret scanning turned on
- `[ ]` Pipeline credentials are short-lived and limited to deployment

---

# PART 20: COMPLETION CHECKLIST AND SIGN-OFF

### Checklist: tick every box before approving this document

**Filled in**
- `[ ]` Document Control complete
- `[ ]` Part 1: every question answered
- `[ ]` Part 3: every role has a real name and contact
- `[ ]` Part 4: system inventory lists everything that is live, including domain, backups and pipeline
- `[ ]` Part 5: everyone with production access is in the table with a reason and end date
- `[ ]` Part 9: filled in or marked `N/A - no AI agents`
- `[ ]` Part 10: current and next phase filled in
- `[ ]` Part 11: emergency access is set up and tested once
- `[ ]` Parts 12, 13, 14: tools, schedules and owners named
- `[ ]` Part 18: compliance rows reviewed for every rule ticked in Q1.4

**Checked for safety**
- `[ ]` No passwords, keys or tokens appear anywhere in this file
- `[ ]` Every person, agent and machine account has MFA or short-lived credentials
- `[ ]` No shared logins exist
- `[ ]` Customer data is blocked by default and masked in staging
- `[ ]` Logs are on, protected, and a test action was found in them
- `[ ]` Backups restore correctly (tested)
- `[ ]` Every `➤ FILL:` has an answer, `N/A - because...`, or `UNKNOWN - [name] by [date]`

**Understood by the team**
- `[ ]` Every person with access has read this and signed below
- `[ ]` Everyone knows how to report a problem (Q17.3)
- `[ ]` Next review date is on someone's calendar

### Acknowledgement and signatures

By signing, I confirm I read this policy and will follow it.

| Name | Role | Signature or typed name | Date |
|---|---|---|---|
| ➤ FILL: | Project Owner | | |
| ➤ FILL: | Security Contact | | |
| ➤ FILL: | Access Approver | | |
| ➤ FILL: | Every other person with production access | | |

### Revision history

| Version | Date | Changed by | What changed and why |
|---|---|---|---|
| 1.0 | ➤ FILL: | ➤ FILL: | First version |

---

*End of template. Remember: a policy is only useful if it is true. Update this file whenever your team, tools, or phase changes.*
