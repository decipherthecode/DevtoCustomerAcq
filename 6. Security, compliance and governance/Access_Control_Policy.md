# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

> **Template:** Access Control Policy | **Folder:** Security, Compliance and Governance | **Template version:** 1.0
> **Covers:** AI-Driven Development Life Cycle (AI-DLC), from first idea to your first 500 customers.
> **Default team size:** 1 to 10 people (bigger teams: see the "Scale-up notes" in each section).

## What is this document?

This document is the rulebook for **who is allowed to open what**. "What" means your code, your servers, your customers' information, your tools, and your AI helpers. Written down, these rules keep your product safe, keep your customers' trust, and help you pass audits (SOC 2, ISO 27001, and others).

## The 7 simple rules for filling it out

1. **Work top to bottom.** Do not skip around. Each section builds on the one before.
2. **Find every `[FILL IN: ...]`.** That is a blank you must answer. Replace the whole thing, brackets included.
3. **Every question has an example.** Read the example, then write your own answer in the same style.
4. **Tick boxes like this:** change `[ ]` to `[x]` for every choice that is true for you.
5. **Never guess.** If you do not know an answer, write `UNKNOWN - ask [name] by [date]` and tell your Document Owner. A visible gap is better than a wrong answer.
6. **Never write real secrets here.** No passwords, keys, tokens, or recovery codes in this file. Write *where* a secret is stored, never the secret itself.
7. **When done, run the Final Checklist (Section 21).** Search the file for `FILL IN` and `UNKNOWN`. When neither appears anywhere, you are finished.

## Legend (what the symbols mean)

| Symbol | Meaning |
|---|---|
| `[FILL IN: ...]` | You must write an answer here. |
| `[ ]` / `[x]` | Empty box / ticked box. |
| **Example:** | A sample answer. Do not copy it unless it is true for you. |
| **DEFAULT:** | The recommended answer. Keep it unless you have a reason to change it. |
| **MUST** | A rule you cannot remove. |
| **SHOULD** | A rule you should keep unless you write a reason in the Exceptions Log (Section 16). |
| **Scale-up note** | Extra advice for when your team grows past 10 people. |

## Time needed

| Project size | Time to fill |
|---|---|
| Solo or 2 to 3 people | About 60 to 90 minutes |
| 4 to 10 people | About 2 to 3 hours (include a team meeting) |

## Who does what while filling this

| Job | Who | What they do |
|---|---|---|
| Writer | Anyone on the team | Fills in the answers. |
| Document Owner | One named person | Checks the answers are true and complete. |
| Approver | A leader or founder | Reads and signs in Section 0. |

## A tiny filled-in sample (so you see the idea)

> **Question:** What is the name of your product?
> **Your answer:** `Pawprint, a mobile app that helps people find lost pets.`

---

# 0. DOCUMENT CONTROL (AUDITOR-READY)

| Field | Your answer |
|---|---|
| Policy title | Access Control Policy |
| Product / project name | [FILL IN: Product name. **Example:** Pawprint] |
| Company / team name | [FILL IN: **Example:** Pawprint Labs] |
| Document ID | [FILL IN: **Example:** SEC-POL-001] |
| Version | [FILL IN: **Example:** 1.0] |
| Status | [ ] Draft  [ ] In review  [ ] Approved  [ ] Retired |
| Document Owner (name, role, contact) | [FILL IN: **Example:** Sam Lee, CTO, sam@example.com] |
| Approver (name, role) | [FILL IN: **Example:** Dana Ruiz, CEO] |
| Date created | [FILL IN: YYYY-MM-DD] |
| Date approved | [FILL IN: YYYY-MM-DD] |
| Next review date | [FILL IN: **DEFAULT:** 12 months after approval, or sooner after any security incident or big change] |
| Confidentiality | [ ] Public  [ ] Internal  [ ] Confidential  (**DEFAULT:** Internal) |
| Team size at the time of writing | [FILL IN: number. **Example:** 6] |

## 0.1 Version history

| Version | Date | Author | What changed | Approved by |
|---|---|---|---|---|
| 0.1 | [FILL IN] | [FILL IN] | First draft | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

## 0.2 Sign-off

By signing, you say you read this policy and agree to follow it.

| Name | Role | Signature (type your full name) | Date |
|---|---|---|---|
| [FILL IN] | Document Owner | [FILL IN] | [FILL IN] |
| [FILL IN] | Approver | [FILL IN] | [FILL IN] |

---

# 1. PURPOSE, SCOPE AND KEY WORDS

## 1.1 Purpose

**Q1.1.1: In one or two sentences, why do we need this policy?**
**DEFAULT:** *"To make sure only the right people, and only the right AI agents, can reach our systems and data, and only for as long as they need to, from the first idea until our first 500 customers and beyond."*
Your answer: [FILL IN: keep the default or rewrite it in your own words]

## 1.2 Scope: who and what this policy covers

**Q1.2.1: Who must follow this policy?** (Tick all that apply.)
- [ ] Founders and owners
- [ ] Employees
- [ ] Part-time staff and interns
- [ ] Contractors and freelancers
- [ ] Vendors and partners with access to our systems
- [ ] AI agents, bots and automations we run (see Section 9)

**Q1.2.2: Which things are protected by this policy?** (Tick all that apply.)
- [ ] Source code and code repositories
- [ ] Build and deploy pipelines (CI/CD)
- [ ] Cloud accounts, servers, databases, storage
- [ ] Customer data and support tools
- [ ] Business tools (email, chat, documents, analytics, billing, payments)
- [ ] AI models, prompts, AI agent tools and API keys
- [ ] Laptops, phones and other devices
- [ ] Physical places (office, server room)
- [ ] Other: [FILL IN]

**Q1.2.3: Is anything NOT covered?** If yes, say what and why.
Your answer: [FILL IN: **Example:** "Our public marketing website pages. Anyone may read them. Editing is still covered."]

## 1.3 Key words in plain language

| Word | Plain meaning |
|---|---|
| Access | Being able to see, change, run or delete something. |
| Identity | Who (or what) someone is: a person, a bot, an AI agent. |
| Authentication | Proving who you are (password, passkey, a code on your phone). |
| Authorization | What you are allowed to do after you prove who you are. |
| Least privilege | Getting only the access you need and nothing extra. |
| Need-to-know | You see information only if your job needs it. |
| Role | A named bundle of access, like "Developer". |
| RBAC | Role-Based Access Control: access is given by role, not person by person. |
| MFA | Multi-Factor Authentication: two or more proofs of identity. |
| SSO | Single Sign-On: one login for many tools. |
| Privileged access | Powerful "admin" access that can change or break things. |
| Non-human identity | An account used by software, such as a bot, service or AI agent. |
| Secret | A password, API key, token or certificate. |
| Break-glass | An emergency account used only when normal access fails. |
| Access review | A regular check that everyone's access is still right. |
| Production ("prod") | The live product real customers use. |
| Customer data | Any information about customers or their users. |
| Joiner / Mover / Leaver | A person who joins, changes jobs inside, or leaves the team. |

---

# 2. ROLES AND RESPONSIBILITIES

**Q2.1: Fill the table. One person can hold several jobs on a small team. Never leave a job empty.**

| Job | What this job does | Name | Backup person |
|---|---|---|---|
| Policy Owner | Keeps this policy true and up to date. | [FILL IN] | [FILL IN] |
| Security Lead | Decides security rules, handles incidents. (Solo team: same as Policy Owner.) | [FILL IN] | [FILL IN] |
| Access Approver(s) | Says "yes" or "no" to access requests. | [FILL IN] | [FILL IN] |
| System Owner(s) | Is in charge of one system (for example the cloud account). | [FILL IN] | [FILL IN] |
| Data Owner | Is in charge of customer data and who may see it. | [FILL IN] | [FILL IN] |
| IT / Platform Admin | Actually creates, changes and removes accounts. | [FILL IN] | [FILL IN] |
| HR / People Contact | Tells IT when someone joins, moves or leaves. | [FILL IN] | [FILL IN] |
| AI Agent Owner | Is responsible for each AI agent's access (Section 9). | [FILL IN] | [FILL IN] |
| Everyone | Follows this policy, reports problems. | All | n/a |

**MUST rule:** The person who *requests* access must not be the same person who *approves* it. If your team has only one person, the approval must be written down and reviewed by an outside friend, advisor or by yourself after 24 hours (note it in the Access Log, Appendix C).

**Scale-up note:** Above 10 people, split Security Lead and IT Admin into two different people.

---

# 3. CORE PRINCIPLES (THE GOLDEN RULES)

These rules apply everywhere in this policy. Tick each one to confirm you accept it. If you untick a rule, record the reason in Section 16 (Exceptions).

- [ ] **Default deny:** If nobody said "yes", the answer is "no".
- [ ] **Least privilege:** Give the smallest access that still lets the job get done.
- [ ] **Need-to-know:** Customer and company secrets are only for people whose work needs them.
- [ ] **Separation of duties:** No single person can request, approve, and use dangerous access alone.
- [ ] **Individual accounts:** No shared logins. One person (or one bot) = one account.
- [ ] **Time-limited:** Powerful access expires automatically.
- [ ] **Everything is logged:** We can always answer "who did what, and when?".
- [ ] **Verify, never assume:** Every request is checked, even from inside the team.
- [ ] **Humans stay in charge of AI:** AI agents never approve their own access or take irreversible actions without a human OK (Section 9).

---

# 4. ACCESS MODEL: ROLES (RBAC)

We give access by **role**, not by person. Add a person to a role and they get exactly that role's access.

## 4.1 Access levels used in this policy

| Level | Name | Meaning |
|---|---|---|
| 0 | None | No access. |
| 1 | View | Can look, cannot change. |
| 2 | Edit | Can change things in normal work. |
| 3 | Approve / Deploy | Can approve changes or release to production. |
| 4 | Admin | Can manage accounts, settings and permissions. |

## 4.2 Our role catalog

**Q4.2.1: Keep the default roles that match your team, rename or delete the rest, and add your own.** Fill in the "People in this role" column with names.

| Role | Who needs it | Typical access (see levels above) | People in this role |
|---|---|---|---|
| Owner / Founder | Business leaders | Billing and ownership: 4. Code: 2. Production: 1. | [FILL IN] |
| Product Manager | Plans features | Planning tools: 2. Code: 1. Production: 0. Customer data: 0 or aggregated only. | [FILL IN] |
| Developer | Builds the product | Code: 2. Test systems: 2. Production: 1 (view logs). Customer data: 0 (use fake data). | [FILL IN] |
| Senior / Release Engineer | Releases the product | Code: 3. Production deploy: 3. | [FILL IN] |
| QA Tester | Tests the product | Test systems: 2. Code: 1. Production: 1 (read-only checks). | [FILL IN] |
| DevOps / Platform Admin | Runs the cloud | Cloud and CI/CD: 4 (time-limited, see Section 7). | [FILL IN] |
| Security Lead | Protects everything | All systems: 1 (audit). Security tools: 4. | [FILL IN] |
| Support Agent | Helps customers | Support tool: 2. Customer data: limited view only (see Section 8.3). | [FILL IN] |
| Marketing / Growth | Gets customers | Analytics: 2. Customer data: aggregated only. | [FILL IN] |
| Contractor | Temporary helper | Only what is listed in their written request. Expires on end date. | [FILL IN] |
| Auditor (read-only) | Reviews our controls | Logs and settings: 1. Time-limited. | [FILL IN] |
| AI Agent (non-human) | Software helper | See Section 9. Never gets Admin. | [FILL IN] |
| Other: [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

## 4.3 Access Matrix (who gets what)

**Q4.3.1: Fill the grid with levels 0 to 4 for each role and system. Use `-` for "not applicable".** The defaults show a safe starting point.

| Role | Source code | CI/CD | Cloud (non-prod) | Production | Customer data | Support tool | Business tools |
|---|---|---|---|---|---|---|---|
| Owner / Founder | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Product Manager | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Developer | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Release Engineer | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| QA Tester | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| DevOps / Platform | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Support Agent | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Marketing | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Contractor | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| AI Agent | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**Example row:** `Developer | 2 | 2 | 2 | 1 | 0 | 0 | 1`

**Scale-up note:** Above 10 people, add attributes (team, device health, location) to decide access in addition to roles.

---

# 5. ACCESS LIFECYCLE: JOINERS, MOVERS, LEAVERS

## 5.1 Requesting access

**Q5.1.1: How does someone ask for access?** (Pick one.)
- [ ] Ticket in our tracker: [FILL IN: tool name and link]
- [ ] Form: [FILL IN: link]
- [ ] Message to the Access Approver in: [FILL IN: tool/channel]

**Every request MUST include:** who needs it, what system, what level, why, how long, and who approved. Use the form in **Appendix A**.

**Q5.1.2: How fast do we answer requests?**
**DEFAULT:** Normal access: 2 business days. Urgent: same day with an Approver's OK.
Your answer: [FILL IN]

## 5.2 Joiners (new people)

**Q5.2.1: What happens on a new person's first day?** Keep the defaults and tick them.
- [ ] Identity check done (government ID or trusted referral) before any access is given
- [ ] Signed confidentiality agreement and read this policy
- [ ] Account created with company email, never a personal one
- [ ] MFA turned on in the first session, before anything else
- [ ] Role assigned from Section 4 (no custom one-off permissions)
- [ ] Security basics training completed within [FILL IN: **DEFAULT:** 7 days]
- [ ] Company device set up (disk encryption, screen lock, updates on)
- [ ] Added to the Access Log (Appendix C)

**Q5.2.2: Who runs the joiner steps?** [FILL IN: name or role]

## 5.3 Movers (people who change jobs inside the team)

**MUST:** When someone changes role, we **remove** the old role's access first, then add the new role's access. Access never just piles up.

**Q5.3.1: How long may old access stay after a move?** **DEFAULT:** 3 business days at most.
Your answer: [FILL IN]

## 5.4 Leavers (people who go away)

**Q5.4.1: How fast do we remove access when someone leaves?**
**DEFAULT:** Friendly leaving: by the end of their last day. Unfriendly or urgent: immediately, before they are told.
Your answer: [FILL IN]

**Leaver checklist (MUST all be done; tick each one in Appendix D):**
- [ ] SSO / main account disabled
- [ ] All app accounts removed or transferred
- [ ] Code repository and CI/CD access removed
- [ ] Cloud and production access removed
- [ ] API keys, tokens and secrets they knew **rotated**
- [ ] Shared secrets and vault entries changed
- [ ] Devices returned and wiped
- [ ] Files and ownership of documents handed to a named person
- [ ] Their AI agents, bots and personal tokens revoked
- [ ] Exit reminder about confidentiality given

## 5.5 Contractors and temporary access

**MUST:** Every contractor account has an **end date** (no more than [FILL IN: **DEFAULT:** 90 days]) and a named **sponsor** (a team member responsible for them).

---

# 6. AUTHENTICATION (PROVING WHO YOU ARE)

**Q6.1: Which login method do we use?**
- [ ] Single Sign-On (SSO) provider: [FILL IN: **Example:** Google Workspace, Okta, Microsoft Entra]
- [ ] Separate logins per tool (only if SSO is not possible; list which tools in Section 6.4)

**Q6.2: Multi-Factor Authentication (MFA)**
**MUST:** MFA is required for **all** accounts that can reach company systems, with no exceptions for founders.
Which MFA types are allowed? (Tick all that apply.)
- [ ] Passkeys / hardware security keys (**best, DEFAULT for admins**)
- [ ] Authenticator app codes
- [ ] Push approval with number matching
- [ ] SMS text message codes (**weakest, avoid; allowed only as a last resort**)

**Q6.3: Passwords** (only where passkeys or SSO are not available)
| Rule | DEFAULT | Your answer |
|---|---|---|
| Minimum length | 14 characters or a long passphrase | [FILL IN] |
| Password manager required | Yes | [FILL IN] |
| Reuse across systems | Never | [FILL IN] |
| Check against leaked-password lists | Yes | [FILL IN] |
| Forced change | Only if leaked or suspected leaked (not on a fixed calendar) | [FILL IN] |
| Lock-out after failed attempts | After 10 tries, with a delay | [FILL IN] |

Password manager we use: [FILL IN: **Example:** 1Password]

**Q6.4: Tools that cannot use SSO or MFA.** List each one and why, and add it to the Exceptions Log (Section 16).
| Tool | Why no SSO/MFA | Extra protection we use | Review date |
|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**Q6.5: Sessions and devices**
- [ ] Screen locks after [FILL IN: **DEFAULT:** 10] minutes
- [ ] Sessions to sensitive tools expire after [FILL IN: **DEFAULT:** 12 hours; admin tools: 1 hour]
- [ ] Only company-managed or checked devices can reach production and customer data
- [ ] Lost device is reported within [FILL IN: **DEFAULT:** 1 hour] to: [FILL IN: contact]

---

# 7. AUTHORIZATION AND PRIVILEGED (ADMIN) ACCESS

## 7.1 Who may be an admin?

**Q7.1.1: Which people may hold admin access, and to which systems?**
| Person | System | Why they need it | Approved by | Expires |
|---|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

## 7.2 Rules for admins (MUST)

- [ ] Admins use **two accounts**: a normal one for daily work and a separate admin one for admin tasks.
- [ ] Admin access is **just-in-time** (given for a short window) wherever the tool allows. Window length: [FILL IN: **DEFAULT:** 4 hours max]
- [ ] Admin accounts use hardware security keys or passkeys.
- [ ] Admin actions are logged and reviewed at least [FILL IN: **DEFAULT:** monthly].
- [ ] Nobody uses root or owner cloud accounts for daily work. Root credentials are locked in a vault and used only for emergencies.

## 7.3 Break-glass (emergency) access

**Q7.3.1: Where are emergency accounts stored and who can use them?**
Your answer: [FILL IN: **Example:** "Two break-glass accounts in the cloud, passwords in a sealed vault entry. Only the CTO or CEO may open it. Every use triggers an alert and a written report within 24 hours."]

**MUST:** After any break-glass use: (1) alert someone, (2) write what was done, (3) change the passwords, (4) review within 2 business days.

## 7.4 Approvals for dangerous actions

**Q7.4.1: Which actions need a second person to approve?** (Tick all that apply.)
- [ ] Deploying to production
- [ ] Changing database schema or deleting data in production
- [ ] Changing access permissions or roles
- [ ] Exporting customer data in bulk
- [ ] Changing billing or payment settings
- [ ] Turning off security tools or logging
- [ ] Other: [FILL IN]

---

# 8. ACCESS RULES BY AREA

## 8.1 Source code and CI/CD

**Q8.1.1: Where does our code live?** [FILL IN: **Example:** GitHub organization "pawprint-labs"]

**Rules to confirm (tick each; untick = write an Exception):**
- [ ] Only company-owned accounts can access the repositories (no personal accounts)
- [ ] The default branch (main) is **protected**: no direct pushes, changes need a reviewed pull request
- [ ] Required reviewers: at least [FILL IN: **DEFAULT:** 1] person other than the author (solo team: automated checks plus a 24-hour wait before merging)
- [ ] Signed commits or verified identities
- [ ] Secret scanning and dependency scanning are turned on
- [ ] CI/CD pipelines run with their own limited identity, not a person's account
- [ ] Deploy keys and tokens are scoped to one repository and expire
- [ ] Production deploys happen only through the pipeline, not from laptops
- [ ] Forks and outside contributors cannot reach secrets

## 8.2 Cloud and production

**Q8.2.1: Which cloud and hosting do we use?** [FILL IN: **Example:** AWS account IDs masked as "prod-01", "staging-01"]

**Environments (MUST be separate):**
| Environment | Purpose | Who can enter | Real customer data allowed? |
|---|---|---|---|
| Development | Building | [FILL IN] | **No** (fake data only) |
| Test / Staging | Testing | [FILL IN] | **No** (fake or masked data) |
| Production | Live customers | [FILL IN] | Yes, with controls |

**Rules to confirm:**
- [ ] No shared cloud logins; every person uses their own SSO identity
- [ ] Production access is read-only by default, with just-in-time elevation for changes
- [ ] Databases are not open to the public internet
- [ ] Secrets live in a secrets manager: [FILL IN: tool], never in code, chat or documents
- [ ] Network access to production is limited to what is needed (VPN, allow-lists or private networking)
- [ ] Backups are encrypted and restore access is limited to: [FILL IN]
- [ ] Cloud audit logging is on in every account and region

## 8.3 Customer data and support access

**Q8.3.1: What kinds of customer data do we hold?** (Tick all that apply.)
- [ ] Names and emails
- [ ] Phone numbers and addresses
- [ ] Payment details (should be held by a payment provider, not by us)
- [ ] Health information
- [ ] Children's data
- [ ] Location data
- [ ] Content customers create or upload
- [ ] Other: [FILL IN]

**Q8.3.2: Data classes.** Keep the default four and fill in your examples.
| Class | Meaning | Who may access | Our examples |
|---|---|---|---|
| Public | Fine for anyone | Everyone | [FILL IN] |
| Internal | For the team | All team members | [FILL IN] |
| Confidential | Business-sensitive or customer personal data | Named roles only | [FILL IN] |
| Restricted | Highly sensitive (passwords, payment, health, keys) | Very few named people, extra approval | [FILL IN] |

**Rules to confirm:**
- [ ] Support agents see only the fields they need (for example, masked emails, hidden payment data)
- [ ] Support "view as customer" or impersonation requires a ticket, a reason and is logged
- [ ] Bulk export of customer data needs second-person approval
- [ ] Customer data is never copied to laptops, personal drives, chat or AI tools that we have not approved
- [ ] Customers' own requests (see my data, delete my data) are handled by: [FILL IN: name/role] within [FILL IN: **DEFAULT:** 30 days]

## 8.4 Business tools and vendors

**Q8.4.1: List every business tool and who administers it.** Add more rows as needed.
| Tool | What it holds | SSO/MFA on? | Admin(s) | Roles allowed |
|---|---|---|---|---|
| [FILL IN: Email] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN: Chat] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN: Docs / Drive] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN: Analytics] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN: Billing / Payments] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN: Support tool] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN: Other] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

## 8.5 Third parties and vendors

**Q8.5.1: Before a vendor gets access, we MUST check:**
- [ ] What access they need, and the smallest version of it
- [ ] Whether they have a security report (SOC 2, ISO 27001) or answered a short security questionnaire
- [ ] A signed agreement that covers confidentiality and data protection (and a Data Processing Agreement if they touch personal data)
- [ ] A named sponsor and an end date
- [ ] How they will tell us about a breach (within [FILL IN: **DEFAULT:** 72 hours])

**Q8.5.2: Vendor access list**
| Vendor | Access they have | Data they can see | Sponsor | Agreement signed? | Review date |
|---|---|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [ ] Yes [ ] No | [FILL IN] |

---

# 9. AI AGENTS AND NON-HUMAN IDENTITIES

AI helpers (coding assistants, chatbots, automation scripts, background agents) can read, write and act very fast. A mistake or a trick (such as a hidden instruction inside a web page, "prompt injection") can do damage quickly. So they follow stricter rules than people.

## 9.1 AI agent register (MUST keep this list up to date)

**Q9.1.1: List every AI agent, bot, service account and automation we use.**
| Agent / account name | What it does | AI Agent Owner | Systems it can reach | Access level (0 to 4) | Data it can see | Token / key location | Expires / reviewed |
|---|---|---|---|---|---|---|---|
| [FILL IN: **Example:** code-helper] | [FILL IN: writes code suggestions] | [FILL IN] | [FILL IN: repo "app" only] | [FILL IN: 2] | [FILL IN: code only, no customer data] | [FILL IN: secrets manager] | [FILL IN] |

## 9.2 Rules for AI agents (MUST)

- [ ] **Own identity:** Every agent has its own account. It never uses a person's login or a shared key.
- [ ] **Named human owner:** Every agent has a responsible human (AI Agent Owner).
- [ ] **Least privilege:** Agents get the narrowest scope, for one repository, one environment, one task.
- [ ] **No admin:** No AI agent gets Level 4 (Admin) or owner-level access.
- [ ] **No self-approval:** An agent cannot approve its own access, its own code changes, or its own deployments.
- [ ] **Human approval gates:** A human must approve before an agent: deploys to production, deletes data, sends messages to customers, changes permissions, spends money, or exports data.
- [ ] **Short-lived credentials:** Tokens expire (**DEFAULT:** at most 30 days, shorter where possible) and are rotated at least every [FILL IN: **DEFAULT:** 90 days].
- [ ] **No customer data in AI tools** unless the tool is approved in Section 9.3 and the data class allows it.
- [ ] **No real secrets in prompts.** Secrets are never pasted into prompts, chats or agent memory.
- [ ] **Treat outside content as untrusted.** Agents must not follow instructions found inside web pages, emails, documents or tool results unless a human told them to. Their tools are limited so a trick cannot cause big damage.
- [ ] **Sandboxing:** Agents run in limited environments with restricted network access.
- [ ] **Full logging:** Every agent action is logged with the agent's name, the human who started it, the time and what happened. Logs are kept [FILL IN: **DEFAULT:** 1 year].
- [ ] **Kill switch:** We can turn off any agent's access within [FILL IN: **DEFAULT:** 15 minutes]. Who can do it: [FILL IN].
- [ ] **Review:** Agent permissions are reviewed at least [FILL IN: **DEFAULT:** quarterly].

## 9.3 Approved AI tools and models

| AI tool / model / provider | Used for | Data classes allowed (Public / Internal / Confidential / Restricted) | Does the provider train on our data? | Approved by | Date |
|---|---|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [ ] Yes [ ] No [ ] Unknown | [FILL IN] | [FILL IN] |

**Rule:** Any AI tool not on this list is **not allowed** for company work until approved.

## 9.4 AI agent permission template (copy one per agent)

```
Agent name:            [FILL IN]
Purpose:               [FILL IN]
Owner:                 [FILL IN]
Allowed actions:       [FILL IN: read repo X, open pull requests, run tests]
Forbidden actions:     [FILL IN: deploy to prod, delete anything, read customer data]
Needs human approval:  [FILL IN: every merge, every message to customers]
Credential type:       [FILL IN] / Expires: [FILL IN]
Logs located at:       [FILL IN]
Date created / next review: [FILL IN]
```

---

# 10. ACCESS THROUGH THE AI-DRIVEN DEVELOPMENT LIFE CYCLE (AI-DLC)

This section says **who may do what in each phase**, from the first idea to the first 500 customers.

## 10.1 Phase overview

| Phase | Name | Goal | Start date | Done when |
|---|---|---|---|---|
| 1 | Idea and Plan | Decide what to build | [FILL IN] | [FILL IN: Plan approved] |
| 2 | Build | Write the product (people and AI) | [FILL IN] | [FILL IN: Feature complete] |
| 3 | Test and QA | Make sure it works and is safe | [FILL IN] | [FILL IN: Tests and security check passed] |
| 4 | Launch Prep | Get production and support ready | [FILL IN] | [FILL IN: Go/No-Go approved] |
| 5 | Launch | Release to the public | [FILL IN] | [FILL IN: Stable for 7 days] |
| 6 | Growth to 500 customers | Support and improve until the 500th customer | [FILL IN] | [FILL IN: 500 customers reached] |

## 10.2 Phase access plan

**Q10.2.1: For each phase, say who has access, what changes and what MUST be true before moving on.** Defaults are given to help you.

### Phase 1: Idea and Plan
- Who: Founders, Product Manager, and invited advisors.
- Access: Planning tools, shared docs. **No** production systems, **no** customer data.
- AI use: Research and writing only, with only Public or Internal data.
- **Gate to leave Phase 1** (tick all):
  - [ ] This policy is approved and signed (Section 0.2)
  - [ ] Roles and Access Matrix filled in (Section 4)
  - [ ] SSO and MFA are on for every account
  - [ ] Data classes decided (Section 8.3)
- Your notes: [FILL IN]

### Phase 2: Build
- Who: Developers, Senior Engineers, DevOps, AI coding agents.
- Access: Code repositories, development environment. **No real customer data.**
- AI use: AI agents may suggest or write code in branches; humans review every merge.
- **Gate to leave Phase 2:**
  - [ ] Protected main branch and code review are working (Section 8.1)
  - [ ] Secret scanning is on and clean
  - [ ] AI agent register complete (Section 9.1)
  - [ ] Staging environment exists and is separate from production
- Your notes: [FILL IN]

### Phase 3: Test and QA
- Who: QA, Developers, Security Lead.
- Access: Staging environment, test data (fake or masked).
- **Gate to leave Phase 3:**
  - [ ] Access test done: a person with a normal role **cannot** reach things outside their role (test at least 3 roles)
  - [ ] Access test done for AI agents: they cannot exceed their scope
  - [ ] Dependency and vulnerability scan has no unresolved critical issues
  - [ ] Backup and restore tested
  - [ ] Logging and alerts tested (a fake bad login creates an alert)
- Your notes: [FILL IN]

### Phase 4: Launch Prep
- Who: Release Engineer, DevOps, Support lead, Security Lead.
- Access: Production is created. Access is **read-only** by default. Support tool is set up with masked fields.
- **Gate to leave Phase 4 (Go/No-Go):**
  - [ ] Production access list reviewed and signed by the Approver
  - [ ] Break-glass accounts created, stored and tested (Section 7.3)
  - [ ] Just-in-time admin access works
  - [ ] Support playbook for customer data access written
  - [ ] Incident contacts and breach steps ready (Section 14)
  - [ ] Privacy notice and terms published (if collecting personal data)
  - [ ] All **UNKNOWN** answers in this document resolved
- Your notes: [FILL IN]

### Phase 5: Launch
- Who: Release Engineer deploys. Everyone else stays on their normal role.
- Access changes: Temporary "launch watch" access expires within [FILL IN: **DEFAULT:** 72 hours] after launch.
- **Gate to leave Phase 5:**
  - [ ] No access-related incident in the first 7 days (or incidents resolved and documented)
  - [ ] All temporary launch access removed
  - [ ] First access review scheduled (Section 13)
- Your notes: [FILL IN]

### Phase 6: Growth to the first 500 customers
- Who: Support, Growth, Developers, Release Engineer.
- Access: Support access grows with the customer base, but still follows the "see only what you need" rule.
- **Checkpoints** (do a mini access review at each):
| Customers reached | What to check | Done? |
|---|---|---|
| 10 | Support access works; logs show who touched customer data | [ ] |
| 50 | First formal access review; remove unused accounts | [ ] |
| 100 | Re-check admin list; rotate keys; review AI agents | [ ] |
| 250 | Review vendors and tools added since launch | [ ] |
| 500 | Full access review, update this policy, decide the next-stage plan | [ ] |
- Your notes: [FILL IN]

## 10.3 Environment and data access by phase (summary table)

| Phase | Development | Staging | Production | Real customer data |
|---|---|---|---|---|
| 1 Idea and Plan | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| 2 Build | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| 3 Test and QA | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| 4 Launch Prep | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| 5 Launch | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| 6 Growth | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**Example for Phase 2:** `Developers: Edit | Developers: Edit | None | Never`

---

# 11. ACCESS FOR OUR CUSTOMERS (PRODUCT-LEVEL ACCESS)

This section is about the access **customers** get inside your product.

**Q11.1: How do customers sign in?** (Tick all that apply.)
- [ ] Email and password
- [ ] Social login (Google, Apple, etc.)
- [ ] Magic link / one-time code
- [ ] Passkeys
- [ ] Single Sign-On for business customers
- [ ] No sign-in needed

**Q11.2: Customer MFA**
- [ ] Offered to all customers
- [ ] Required for admins of customer accounts
- [ ] Required for everyone
- [ ] Not offered yet (add to the Exceptions Log)

**Q11.3: Customer roles inside the product**
| Customer role | What it can do | Default for new users? |
|---|---|---|
| [FILL IN: **Example:** Owner] | [FILL IN: manage billing, invite users] | [ ] |
| [FILL IN: **Example:** Member] | [FILL IN: use the product] | [ ] |
| [FILL IN: **Example:** Viewer] | [FILL IN: read-only] | [ ] |

**Rules to confirm:**
- [ ] A customer can see **only their own** data (tenant isolation is tested before launch and re-tested after big changes)
- [ ] API keys for customers are scoped, can be revoked, and are never shown in full after creation
- [ ] Rate limiting and lock-outs protect against password guessing
- [ ] Customers can delete their account and data (Section 8.3)
- [ ] Suspicious activity (many failed logins, logins from far away) triggers an alert

---

# 12. LOGGING AND MONITORING

**Q12.1: What do we log?** (Tick all that apply.)
- [ ] Successful and failed logins
- [ ] Access requests, approvals and rejections
- [ ] Role and permission changes
- [ ] Admin and break-glass actions
- [ ] Access to customer data (who, what, when)
- [ ] AI agent actions (Section 9.2)
- [ ] Production deployments
- [ ] Changes to security settings

**Q12.2: Where are logs stored, and for how long?**
| Log type | Where | Kept for | Who can read | Who can delete |
|---|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN: **DEFAULT:** 12 months] | [FILL IN] | **Nobody** (write-once if possible) |

**Q12.3: Which alerts wake somebody up?** (Tick all that apply.)
- [ ] Login to an admin account from a new country
- [ ] Break-glass account used
- [ ] Many failed logins
- [ ] Bulk download or export of customer data
- [ ] Turning off logging or MFA
- [ ] AI agent acting outside its allowed scope
- [ ] Other: [FILL IN]

Alerts go to: [FILL IN: person and channel]. They must be answered within: [FILL IN: **DEFAULT:** 1 hour on working days].

---

# 13. ACCESS REVIEWS (REGULAR CHECK-UPS)

**Q13.1: How often do we check who has access to what?**
| What is reviewed | How often (**DEFAULT**) | Your answer | Reviewer |
|---|---|---|---|
| Admin and privileged access | Every 1 month | [FILL IN] | [FILL IN] |
| Production and customer data access | Every 3 months | [FILL IN] | [FILL IN] |
| All other access | Every 6 months | [FILL IN] | [FILL IN] |
| AI agents and tokens | Every 3 months | [FILL IN] | [FILL IN] |
| Vendors and contractors | Every 3 months | [FILL IN] | [FILL IN] |
| Dormant accounts (unused) | Disable after 30 days unused, remove after 90 | [FILL IN] | [FILL IN] |

**How to run a review (5 simple steps):**
1. Export the list of accounts and permissions for each system.
2. For each account ask: *Does this person or bot still work here? Do they still need this access?*
3. Mark each as **Keep**, **Reduce** or **Remove**.
4. Make the changes within [FILL IN: **DEFAULT:** 5 business days].
5. Record the result in **Appendix E** and sign it.

**MUST:** A person never reviews their own access.

---

# 14. INCIDENTS INVOLVING ACCESS

**Q14.1: What counts as an access incident?** (Tick all that apply.)
- [ ] Stolen or lost laptop or phone
- [ ] Stolen password, token or key (including a key pasted into a public place)
- [ ] Someone saw data they should not have
- [ ] A former team member still has access
- [ ] An AI agent did something it was not allowed to do
- [ ] Unusual logins or data downloads
- [ ] Other: [FILL IN]

**Q14.2: First 5 steps when it happens (edit if needed).**
1. **Tell** [FILL IN: name and contact] immediately.
2. **Stop the damage:** disable the account or token, rotate the secret.
3. **Save the evidence:** do not delete logs.
4. **Decide** if customers or authorities must be told. Legal deadline notes: [FILL IN: **Example:** GDPR: 72 hours to the regulator; HIPAA: 60 days; check your own laws]
5. **Learn:** within [FILL IN: **DEFAULT:** 5 business days] write what happened, why, and what we will change.

**Q14.3: Emergency contacts**
| Who | Phone / channel | Backup |
|---|---|---|
| Security Lead | [FILL IN] | [FILL IN] |
| Cloud provider support | [FILL IN] | [FILL IN] |
| Legal advisor | [FILL IN] | [FILL IN] |
| Insurance / outside incident help (if any) | [FILL IN] | [FILL IN] |

---

# 15. TRAINING AND AWARENESS

**Q15.1: Who is trained on what, and when?**
| Training | Who | When | How we track it |
|---|---|---|---|
| Security basics (passwords, MFA, phishing) | Everyone | Within 7 days of joining, then yearly | [FILL IN] |
| This policy | Everyone | Within 7 days of joining and after each update | [FILL IN] |
| Handling customer data | Support, Developers, anyone with data access | Before access is given | [FILL IN] |
| Safe use of AI tools and agents | Everyone using AI | Before using AI tools | [FILL IN] |
| Admin and incident duties | Admins, Security Lead | Before getting admin access, then yearly | [FILL IN] |

---

# 16. EXCEPTIONS LOG

If you cannot follow a rule, you MUST write it here, get it approved, and give it an end date. An exception can last no longer than [FILL IN: **DEFAULT:** 6 months].

| ID | Date | Rule not followed | Why | Extra protection used instead | Approved by | Ends on | Closed? |
|---|---|---|---|---|---|---|---|
| EX-001 | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [ ] |

---

# 17. ENFORCEMENT AND CHANGES TO THIS POLICY

- Breaking this policy can lead to loss of access, and for team members, further action as allowed by our agreements and local law.
- Anyone may report a concern without fear of punishment. Report to: [FILL IN: name or confidential channel].
- This policy is reviewed at least every [FILL IN: **DEFAULT:** 12 months] and after: a security incident, a big system change, a new law, reaching 500 customers, or growing past 10 team members.
- Changes are recorded in Section 0.1 and approved by the Approver.

---

# 18. COMPLIANCE MAPPING (FOR AUDITORS)

This table shows where each framework's access-control expectations are met in this document. Control numbers are guides to help find the right idea. Always check them against the current official text of each framework before an audit.

| Topic | This document | SOC 2 (Trust Services Criteria) | ISO/IEC 27001:2022 (Annex A) | NIST CSF 2.0 / SP 800-53 | GDPR / HIPAA / PCI DSS |
|---|---|---|---|---|---|
| Access policy and roles | Sections 2, 3, 4 | CC6.1 | A.5.15, A.5.2 | PR.AA, AC-1, AC-2 | GDPR Art. 25, 32; HIPAA 164.308(a)(4); PCI DSS Req. 7 |
| Joiners, movers, leavers | Section 5 | CC6.2, CC6.3 | A.5.16, A.5.18, A.6.5 | PR.AA-05, AC-2 | HIPAA 164.308(a)(3); PCI DSS Req. 8 |
| Authentication and MFA | Section 6 | CC6.1 | A.5.17, A.8.5 | PR.AA-03, IA-2, IA-5 | HIPAA 164.312(d); PCI DSS Req. 8 |
| Privileged access | Section 7 | CC6.1, CC6.3 | A.8.2 | AC-6 | PCI DSS Req. 7, 8 |
| Source code and production | Section 8.1, 8.2 | CC6.1, CC8.1 | A.8.3, A.8.4, A.8.31, A.8.32 | PR.AA, AC-3, CM-5 | PCI DSS Req. 6 |
| Customer data | Section 8.3 | CC6.1, C1.1, P-series | A.5.12, A.5.13, A.5.34 | PR.DS, AC-3 | GDPR Art. 5, 25, 32; HIPAA 164.312(a) |
| Vendors | Section 8.5 | CC9.2 | A.5.19 to A.5.22 | GV.SC | GDPR Art. 28; HIPAA 164.308(b); PCI DSS Req. 12.8 |
| AI agents and non-human identities | Section 9 | CC6.1, CC6.6 | A.5.15, A.8.2, A.8.9 | PR.AA-01, AC-2, AC-6 | Same as above, plus the EU AI Act where it applies |
| Logging and monitoring | Section 12 | CC7.2 | A.8.15, A.8.16 | DE.CM, AU-2, AU-6 | HIPAA 164.312(b); PCI DSS Req. 10 |
| Access reviews | Section 13 | CC6.2, CC6.3 | A.5.18 | AC-2(j), PR.AA | PCI DSS Req. 7.2.4 |
| Incidents | Section 14 | CC7.3, CC7.4 | A.5.24 to A.5.27 | RS, IR-4 | GDPR Art. 33, 34; HIPAA Breach Rule |
| Training | Section 15 | CC1.4, CC2.2 | A.6.3 | PR.AT | PCI DSS Req. 12.6 |

**Q18.1: Which frameworks actually apply to *this* project?** (Tick all that apply; delete unused columns.)
- [ ] SOC 2  [ ] ISO 27001  [ ] NIST CSF / 800-53  [ ] GDPR  [ ] HIPAA  [ ] PCI DSS  [ ] Other: [FILL IN]

---

# 19. METRICS (HOW WE KNOW IT IS WORKING)

**Q19.1: Pick the numbers we watch and how often.**
| Number | Goal (**DEFAULT**) | Our goal | How often checked |
|---|---|---|---|
| % of accounts with MFA | 100% | [FILL IN] | [FILL IN] |
| Average time to remove a leaver's access | Under 1 business day | [FILL IN] | [FILL IN] |
| Admin accounts with no recent use | 0 | [FILL IN] | [FILL IN] |
| Access reviews finished on time | 100% | [FILL IN] | [FILL IN] |
| Open exceptions past their end date | 0 | [FILL IN] | [FILL IN] |
| AI agents with a named owner and current review | 100% | [FILL IN] | [FILL IN] |
| Secrets older than the rotation limit | 0 | [FILL IN] | [FILL IN] |

---

# 20. HOW TO REUSE THIS TEMPLATE ON A NEW PROJECT

1. Copy this file. Rename it `Access_Control_Policy.md` inside the new project's **Security, Compliance and Governance** folder.
2. Reset **Section 0** (title, owner, dates, version 0.1) and clear the version history.
3. Delete every previous answer (replace with `[FILL IN: ...]`) except the default text you decide to keep.
4. Fill in the document from the top, with a team meeting for Sections 2, 4, 8 and 10.
5. Run the **Final Checklist** below.
6. Get it signed, then store it where the whole team can read it, but only the Policy Owner can edit.

---

# 21. FINAL CHECKLIST (ARE WE DONE?)

Tick everything. Any unticked box means the document is **not ready**.

**Completeness**
- [ ] Searching for `FILL IN` finds **zero** results
- [ ] Searching for `UNKNOWN` finds **zero** results
- [ ] Every checkbox section has been ticked or deliberately left unticked with an Exception
- [ ] Every table row either has real content or has been deleted
- [ ] Every name in the document is a real, reachable person

**Safety**
- [ ] No passwords, keys, tokens or recovery codes appear anywhere in this file
- [ ] No real customer data appears anywhere in this file

**Truth check**
- [ ] A different team member read it and agreed it is true
- [ ] We tested at least 3 roles and at least 1 AI agent against the Access Matrix (Section 10, Phase 3)
- [ ] Break-glass access was tested (Section 7.3)

**Governance**
- [ ] Sections 0.1 and 0.2 are complete and signed
- [ ] Next review date is in the calendar
- [ ] Exceptions Log is complete

---

# APPENDICES

## Appendix A: Access Request Form (copy one per request)

```
Request date:              [FILL IN]
Who needs access:          [FILL IN: name or AI agent name]
Role:                      [FILL IN]
System(s):                 [FILL IN]
Access level (0-4):        [FILL IN]
Why they need it:          [FILL IN]
How long (end date):       [FILL IN]
Requested by:              [FILL IN]
Approved by (different person): [FILL IN]
Approval date:             [FILL IN]
Done by (IT/Admin):        [FILL IN]   Date done: [FILL IN]
```

## Appendix B: Role and Permission Change Form

```
Person / agent:            [FILL IN]
Old role -> new role:      [FILL IN]
Access to REMOVE:          [FILL IN]
Access to ADD:             [FILL IN]
Reason:                    [FILL IN]
Approved by:               [FILL IN]   Date: [FILL IN]
```

## Appendix C: Access Log (who has access now)

| Date | Person / agent | Role | System | Level | Action (Granted / Changed / Removed) | Approved by | Done by |
|---|---|---|---|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

## Appendix D: Leaver Checklist (copy one per person)

```
Name:                      [FILL IN]       Last day: [FILL IN]
[ ] SSO / main account disabled             Done by / date: [FILL IN]
[ ] App accounts removed or transferred     Done by / date: [FILL IN]
[ ] Repository and CI/CD access removed     Done by / date: [FILL IN]
[ ] Cloud and production access removed     Done by / date: [FILL IN]
[ ] Secrets they knew rotated               Done by / date: [FILL IN]
[ ] AI agents / tokens they owned revoked or reassigned  Done by / date: [FILL IN]
[ ] Devices returned and wiped              Done by / date: [FILL IN]
[ ] Documents handed over                   Done by / date: [FILL IN]
[ ] Confirmed by a second person            Name / date: [FILL IN]
```

## Appendix E: Access Review Record

| Review date | System | Reviewer | Accounts checked | Kept | Reduced | Removed | Follow-ups done by | Signed |
|---|---|---|---|---|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

## Appendix F: Quick Reference Card (print this and share it with the team)

1. **MFA on everything. No exceptions.**
2. **One person = one account.** Never share logins.
3. **Ask before you get access. Say why. Say for how long.**
4. **Only take what you need.** Give back what you do not.
5. **Secrets never go in chat, email, code or prompts.**
6. **No real customer data in dev, test, or AI tools that are not approved.**
7. **AI agents get their own account, a small scope, an owner, and a human gate for risky actions.**
8. **Lost a device or saw something odd?** Tell [FILL IN: contact] within 1 hour.
9. **Leaving or changing jobs?** Access is removed the same day.

## Appendix G: Glossary of extra words

| Word | Plain meaning |
|---|---|
| API key | A secret code that lets software talk to a service. |
| Branch protection | A rule that stops people from changing the main code without a review. |
| Pull request | A request to add your code changes to the main code, so others can check them. |
| Just-in-time access | Admin access that is switched on only when needed and turns off by itself. |
| Tenant isolation | Making sure one customer cannot see another customer's data. |
| Prompt injection | A trick where hidden instructions in content make an AI do something unwanted. |
| Rotation | Replacing an old secret with a new one. |
| Service account | An account for software instead of a person. |
| Vault / secrets manager | A safe digital box for passwords and keys. |
| Passkey | A modern, phishing-resistant login that replaces passwords. |

---
*End of template. Template version 1.0. Review it yearly and share improvements with the template owner.*
