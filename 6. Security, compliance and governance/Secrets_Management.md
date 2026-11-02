# How to Fill This Document

> **Read this first. It takes 3 minutes and saves hours.**

This file is a **Secrets Management Plan** for one product. Copy it into each new project, fill it in once, and keep it up to date until your first 500 customers are using the product.

## What is a "secret"?
A secret is anything that proves who you are or unlocks something private. Examples: passwords, API keys, database logins, tokens, private certificates, encryption keys, signing keys, webhook signing secrets.

**Simple rule:** if someone who should not have it could use it to get in, it is a secret.

## The 7 rules for filling this document
1. **Answer in plain sentences** under every `Your answer:` line. Short is fine. Full sentences are better than one word.
2. **Never write a real secret in this file.** Write where it lives (for example, "stored in the vault under `prod/payments/stripe-key`"), never the value.
3. **If a question does not apply, write `N/A` and say why** (for example, "N/A: we have no mobile app"). Do not leave anything blank.
4. **If you don't know, write `UNKNOWN: ask <name> by <date>`.** Unknowns are allowed. Hidden unknowns are not.
5. **Use names, not roles, wherever possible** ("Priya Shah", not "the dev lead"). Add a backup person too.
6. **Use real dates** (`2026-11-30`), never "soon" or "later".
7. **Work top to bottom.** Later sections depend on earlier answers.

## How to read the markers
| Marker | Meaning |
|---|---|
| **Question:** | Something you must answer |
| **Example answer:** | A sample so you can see the style. Delete it or replace it with yours |
| **[TECH]** | Extra detail for engineers. Non-technical people can hand these to an engineer |
| **Done when:** | A checklist. Tick `[x]` only when it is really true |
| **STOP:** | Do not continue to the next phase until this is true |

## Who fills what
| Section | Best filled by |
|---|---|
| 1-4 (purpose, roles, rules) | Product owner / founder |
| 5-7 (tools, inventory, environments) | Engineering lead |
| 8 (lifecycle phases) | Whole team, phase by phase |
| 9-16 (technical controls) | Engineers + DevOps |
| 17 (incident runbook) | Engineering lead + whoever answers the pager |
| 18-20 (compliance, QA, launch gate) | QA + security/compliance owner |
| 21 (sign-off) | Approvers |

## Quality check before you call it finished
- [ ] No question left blank
- [ ] No real secret values anywhere in this file
- [ ] Every secret in Section 6 has a named owner and a rotation date
- [ ] Section 17 names real people with real phone/chat contacts
- [ ] Section 21 is signed and dated
- [ ] A person who has never seen the project could follow Section 17 at 3 a.m.

---

# Secrets Management Plan

## 0. Document Control

**Question:** What is the product/project name, and what does it do in one sentence?
- **Your answer:**
- **Example answer:** "InvoiceBuddy: a web app that lets freelancers send invoices and get paid by card."

**Question:** Who owns this document (name and contact)? Who is the backup owner?
- **Your answer:**

**Question:** What is the current version and date of this plan?
- **Your answer:** (Use `v0.1` for the first draft, `v1.0` once approved)

**Question:** Where does the official copy of this file live (link or path)?
- **Your answer:**

**Question:** Which project stage are you in right now? (Phase 1-6, see Section 8)
- **Your answer:**

**Question:** When must this document next be reviewed? (Recommended: every 90 days and before each major launch step)
- **Your answer:**

---

## 1. Purpose and Scope

**Question:** In your own words, why does this product need a secrets plan? What is the worst thing that could happen if a secret leaked?
- **Your answer:**
- **Example answer:** "If our payment key leaked, a stranger could issue refunds or read customer billing data. We could lose customer trust and face fines."

**Question:** What is covered by this plan? List every part of the product (web app, mobile app, backend, database, admin tools, automation, AI features, third-party services).
- **Your answer:**

**Question:** What is NOT covered, and who covers it instead?
- **Your answer:**
- **Example answer:** "Employee laptop passwords are covered by the company IT policy owned by Sam Lee."

**Question:** What kinds of sensitive data does the product handle? (Tick all that apply, then explain.)
- [ ] Customer names/emails
- [ ] Payment card data
- [ ] Health data
- [ ] Children's data
- [ ] Location data
- [ ] Customers' own API keys or credentials
- [ ] Other:
- **Your answer:**

---

## 2. Plain-Language Basics (read once, keep for newcomers)

| Term | What it means in simple words |
|---|---|
| **Secret** | A private key, password or token that unlocks something |
| **Vault / Secrets manager** | A locked digital safe that stores secrets and records who opened it |
| **Rotation** | Changing a secret on a schedule so an old leaked one stops working |
| **Revocation** | Switching a secret off immediately |
| **Least privilege** | Give each person or program only the keys they really need |
| **Environment** | A separate copy of the product: development (practice), staging (rehearsal), production (real customers) |
| **Hard-coded secret** | A secret typed directly into code. This is the most common cause of leaks |
| **Secret sprawl** | Secrets copied into chats, docs, spreadsheets and laptops, so nobody knows where they are |
| **Service account / machine identity** | A login used by a program, not a person |
| **Short-lived credential** | A key that expires by itself in minutes or hours |

**The most common ways secrets leak (keep these in mind):**
1. Pushed to a code repository (even a private one).
2. Pasted into chat, email, tickets or documents.
3. Printed in logs or error messages.
4. Left in old laptops, old containers or old backups.
5. Shared with an AI tool or pasted into a prompt.
6. Kept by a former employee or vendor after they leave.

---

## 3. Roles and Responsibilities (RACI)

**R** = does the work, **A** = final owner (only one per row), **C** = must be asked, **I** = must be told.

**Question:** Fill the table with real names.

| Task | Product Owner | Eng Lead | DevOps / Platform | Security Owner | QA | Developers | Support |
|---|---|---|---|---|---|---|---|
| Approve this plan | A | R | C | R | I | I | I |
| Choose the secrets tool | I | A | R | C | I | I | I |
| Create / store secrets | I | A | R | C | I | R | I |
| Rotate secrets | I | A | R | C | C | R | I |
| Grant / remove access | I | C | R | A | I | I | I |
| Scan code for leaks | I | A | R | C | R | R | I |
| Run the incident runbook | I | A | R | R | C | C | I |
| Notify customers / regulators | A | C | I | R | I | I | R |
| Test controls (QA) | I | C | C | C | A | R | I |
| Review every 90 days | I | R | R | A | C | I | I |

- **Your answer (names):**
  - Product Owner:
  - Engineering Lead (and backup):
  - DevOps / Platform:
  - Security Owner (and backup):
  - QA Lead:
  - Legal / Privacy contact:
  - Customer Support Lead:

**Question:** If a person is on holiday or unreachable, who takes over each role?
- **Your answer:**

---

## 4. Golden Rules (Policy)

These rules apply to everyone. **Edit only to make them stricter, not looser.** Tick to confirm the team agrees.

- [ ] **G1.** No secret is ever written in source code, config files committed to the repo, tickets, chat, email, wikis or screenshots.
- [ ] **G2.** All secrets live in the approved secrets manager (Section 5), and nowhere else.
- [ ] **G3.** Every secret has an **owner**, a **purpose**, a **rotation date** and an **expiry plan**.
- [ ] **G4.** Production secrets are different from development and staging secrets. They are **never** reused across environments.
- [ ] **G5.** People get the minimum access needed, only for as long as needed (least privilege).
- [ ] **G6.** Programs use machine identities and short-lived credentials where possible, not shared long-lived passwords.
- [ ] **G7.** Every secret read, change and failed access attempt is logged.
- [ ] **G8.** Secrets are never printed in logs, error messages, analytics or crash reports.
- [ ] **G9.** AI tools and agents follow Section 15. They never see raw production secrets.
- [ ] **G10.** A leaked or suspected-leaked secret is treated as an incident and **revoked first, investigated second.**
- [ ] **G11.** When someone leaves the team or a vendor contract ends, their access is removed within 24 hours.
- [ ] **G12.** Nothing launches or scales (Phase gates in Section 8) until its "Done when" checklist is complete.

**Question:** Do you need any extra rules for your product? Write them as `G13`, `G14` and so on.
- **Your answer:**

**Question:** What happens when someone breaks a rule by accident? (Recommended: no blame for reporting quickly, and a review to fix the cause.)
- **Your answer:**

---

## 5. Tooling Decisions

**Question:** Which secrets manager will you use as the single source of truth? Pick one primary tool.
- [ ] AWS Secrets Manager / AWS SSM Parameter Store
- [ ] Google Cloud Secret Manager
- [ ] Azure Key Vault
- [ ] HashiCorp Vault / HCP Vault
- [ ] Doppler
- [ ] 1Password (Secrets Automation / Connect)
- [ ] Other:
- **Why did you choose it?**
- **Your answer:**

**Question:** Which key-management service (KMS) encrypts your secrets and data? (Often the same cloud provider.)
- **Your answer:**
- **Example answer:** "AWS KMS with customer-managed keys, one per environment."

**Question:** Where do your apps run, and how do they prove their identity to the vault without a password? (This is the "secret zero" problem.)
- **Your answer:**
- **[TECH] Example answer:** "ECS tasks use IAM roles. GitHub Actions use OIDC to assume a deploy role. No long-lived cloud keys exist."

**Question:** What tools are used for each job below? Write the tool name or `N/A`.

| Job | Tool |
|---|---|
| Store secrets | |
| Encrypt keys (KMS/HSM) | |
| Scan code for leaked secrets (pre-commit) | |
| Scan code for leaked secrets (in CI) | |
| Scan old git history | |
| Scan container images / infrastructure code | |
| Team password manager (for humans) | |
| Certificate management (TLS) | |
| Logging / audit trail | |
| Alerts / paging | |

**[TECH] Suggested options (you may choose others):** gitleaks, trufflehog, GitHub secret scanning with push protection, GitLab secret detection, detect-secrets (pre-commit); cert-manager / ACME for certificates; CloudTrail / Cloud Audit Logs / Azure Monitor for audit logs.

**Question:** What is the plan if the secrets manager is down? Can the product keep running? (For example: apps cache secrets in memory for a short time.)
- **Your answer:**

**Question:** What does the tool cost per month at 0, 100 and 500 customers? Who approves that budget?
- **Your answer:**

---

## 6. Secret Inventory (the master list)

> **This is the most important table in the document.** If a secret isn't listed here, nobody is protecting it.
> Do **not** write the secret value. Write where it is stored.

**Question:** List every secret the product uses. Add rows as you grow. Update the table every time a new secret is created.

| ID | Name | What it unlocks | Type | Environment | Storage path (not the value) | Owner | Created | Rotation every | Next rotation | Who/what can read it | Impact if leaked (H/M/L) |
|---|---|---|---|---|---|---|---|---|---|---|---|
| S-001 | Example: Payment API key | Charges and refunds | API key | prod | `prod/payments/stripe-key` | Priya Shah | 2026-10-01 | 90 days | 2026-12-30 | payments-service role | High |
| S-002 | | | | | | | | | | | |
| S-003 | | | | | | | | | | | |
| S-004 | | | | | | | | | | | |
| S-005 | | | | | | | | | | | |

**Secret types to look for (tick the ones you use, and make sure each has a row above):**
- [ ] Database usernames/passwords
- [ ] Third-party API keys (payments, email, SMS, maps, analytics)
- [ ] OAuth client secrets
- [ ] JWT / session signing keys
- [ ] Encryption keys (data at rest)
- [ ] TLS/SSL private keys and certificates
- [ ] SSH keys
- [ ] Cloud provider credentials
- [ ] CI/CD tokens (GitHub, GitLab, registry)
- [ ] Webhook signing secrets
- [ ] Mobile app signing keys (Apple/Google)
- [ ] LLM / AI provider API keys
- [ ] Admin/break-glass accounts
- [ ] Customer-provided credentials
- [ ] Other:

**Question:** Is there any secret that cannot be rotated easily (for example, a key built into a shipped mobile app)? What is your plan?
- **Your answer:**

**Question:** Which three secrets would hurt the most if leaked, and why?
- **Your answer:**

---

## 7. Environments and Separation

**Question:** Which environments exist? Fill the table.

| Environment | Purpose | Real customer data? | Who has access | Separate vault / account? |
|---|---|---|---|---|
| Local (laptops) | Developers write code | No (fake data only) | Developers | |
| Development | Shared testing | No | Developers, QA | |
| Staging | Rehearsal before launch | No (masked data only) | Dev, QA, DevOps | |
| Production | Real customers | Yes | Very few people | |

**Question:** How do you make sure production secrets never reach development or staging, and vice versa?
- **Your answer:**
- **[TECH] Example answer:** "Separate cloud accounts per environment. Production vault is reachable only from production network. Names are prefixed `prod/`, `stg/`, `dev/` and policies deny cross-prefix access."

**Question:** How do developers work locally without real secrets?
- **Your answer:**
- **Example answer:** "A `.env.example` file lists variable names with fake values. Each developer receives dev-only keys from the vault through the CLI. `.env` files are in `.gitignore`."

**Question:** What is the naming convention for secrets? (Recommended: `<env>/<service>/<purpose>`)
- **Your answer:**

**Question:** Who may access production secrets, how do they get approved, and for how long? (Recommended: just-in-time access that expires in hours.)
- **Your answer:**

---

## 8. The AI-Driven Development Lifecycle: From First Line of Code to 500 Customers

> Six phases. Each phase has questions, then a **Done when** checklist. **STOP** means do not move on until it is true.
> "AI-driven" means AI assistants and agents help write, test, review or deploy code. Section 15 explains the extra care this needs.

### Phase 1: Plan and Design (Idea to Approved Design)

**Question:** What secrets do you expect the product to need? (A rough list is fine now. Section 6 gets the full list.)
- **Your answer:**

**Question:** What data will you handle, and does any law or standard apply (privacy, health, payments)? (See Section 18.)
- **Your answer:**

**Question:** Which secrets manager, KMS and scanners did you choose (Section 5), and who approved them?
- **Your answer:**

**Question:** What are the top 5 ways an attacker could steal your secrets? (A "threat model" in simple words.)
- **Your answer:**
- **Example answer:** "1) Leaked key in GitHub. 2) Developer laptop stolen. 3) Compromised CI token. 4) AI agent prints a key into a log. 5) Former contractor still has access."

**Done when:**
- [ ] Section 0-5 answered and owner approved
- [ ] Threat list written
- [ ] Secrets tool and budget approved
- [ ] Section 3 roles named
- [ ] AI-tool rules (Section 15) agreed

**STOP:** Do not write production code until the secrets tool is chosen and roles are named.

### Phase 2: Build (Writing the Product)

**Question:** How do developers and AI assistants get the secrets they need while coding? (Never by copy-paste from chat.)
- **Your answer:**

**Question:** How is accidental commit of secrets prevented? Tick all that are in place.
- [ ] `.gitignore` blocks `.env`, key files and credential files
- [ ] Pre-commit secret scanner installed for every developer
- [ ] Push protection enabled on the code host
- [ ] CI secret scan fails the build on any finding
- [ ] Full git-history scan done once at project start
- **Your answer (details):**

**Question:** How does code read secrets? (Recommended: at start-up from the vault or injected as environment variables by the platform; never from files in the repo.)
- **Your answer:**

**Question:** How do you stop secrets appearing in logs, errors and crash reports?
- **Your answer:**
- **[TECH] Example answer:** "Logging library has a redaction filter for keys named `password`, `token`, `secret`, `authorization`. Error pages show generic messages. Request bodies are not logged."

**Done when:**
- [ ] Zero hard-coded secrets (scan is clean)
- [ ] Every secret created so far is in Section 6
- [ ] Pre-commit and CI scanning are working (test by committing a fake key and confirming it is blocked)
- [ ] `.env.example` exists and is accurate
- [ ] Logging redaction is tested

### Phase 3: Test and Harden (Quality Assurance)

**Question:** How will QA prove the controls work? Fill in the results as you go.

| Test | How to check | Passed? (Y/N) | Date | Tester |
|---|---|---|---|---|
| Fake secret commit is blocked | Try committing a dummy key | | | |
| Secret scan of full repo history is clean | Run scanner | | | |
| App starts with secrets from the vault only | Remove `.env`, start app | | | |
| Staging cannot read production secrets | Try it, expect "access denied" | | | |
| Rotation works without downtime | Rotate a staging secret during a test run | | | |
| Revoked secret stops working immediately | Revoke, retry, expect failure | | | |
| Logs contain no secrets | Search logs for test key | | | |
| Failed access attempts raise an alert | Trigger a denied read | | | |
| AI agent cannot read production secrets | Try from agent's identity | | | |
| Leak drill (Section 17) completed | Run a practice incident | | | |

**Question:** What problems did testing find, and what was done about each?
- **Your answer:**

**Done when:**
- [ ] Every row in the table above is `Y`
- [ ] Dependency and container scans show no embedded secrets
- [ ] One leak drill finished in under the target time (Section 17)
- [ ] Security Owner reviewed results

**STOP:** Do not launch with any failed test.

### Phase 4: Launch Readiness (Final Step Before Real Customers)

**Question:** What is the exact list of production secrets, and have they all been created fresh (not copied from staging)?
- **Your answer:**

**Question:** Who has production access on launch day, and what does each person do?
- **Your answer:**

**Question:** What is the rollback plan if a secret fails on launch day?
- **Your answer:**

**Question:** What alerts are switched on for launch? (Failed vault access, unusual secret reads, expiring secrets, scanner alerts.)
- **Your answer:**

**Done when:**
- [ ] Section 20 (Launch Gate) is fully ticked
- [ ] Production secrets are all new and unique
- [ ] Break-glass account is created, tested and stored offline in a sealed, access-controlled place
- [ ] On-call person named for first 7 days
- [ ] Section 21 sign-off complete

**STOP:** Launch only after approvers have signed.

### Phase 5: Launch to First 100 Customers

**Question:** What do you check every day in the first 2 weeks? (Alerts, access logs, expiring secrets, new secrets added.)
- **Your answer:**

**Question:** How will you notice a leak quickly? What would the first sign look like?
- **Your answer:**
- **Example answer:** "Unusual spike in API usage from a new country, or a provider emailing us about leaked-key detection."

**Question:** What new secrets were added since launch? Are they all in Section 6?
- **Your answer:**

**Question:** Did the first real rotation happen, and did it go smoothly?
- **Your answer:**

**Question:** Do customers or support staff ever see secrets (reset links, API keys shown in dashboards)? How are those protected? (Show once, mask afterwards, expire quickly.)
- **Your answer:**

**Done when:**
- [ ] 30 days with no leaked secret, or every incident closed with a written review
- [ ] First scheduled rotation completed on time
- [ ] Section 6 matches reality (spot check by Security Owner)
- [ ] Access list reviewed (remove anyone who does not need production)
- [ ] Support has a script for "customer lost access / key exposed"

### Phase 6: Grow to 500 Customers

**Question:** As you grow, what will change? (More engineers, more services, enterprise customers, more third-party tools.) What does that mean for secrets?
- **Your answer:**

**Question:** Do you need to upgrade? Tick any that are now needed.
- [ ] Move from static keys to dynamic/short-lived credentials
- [ ] Per-customer encryption keys or customer-managed keys
- [ ] Automated rotation for all high-impact secrets
- [ ] Hardware-backed key protection (HSM)
- [ ] Formal access review each quarter
- [ ] Independent security test / penetration test
- [ ] Compliance audit (SOC 2, ISO 27001, others)
- **Your answer (decisions and dates):**

**Question:** How do customers ask security questions about secrets, and who answers them? Is a short, approved answer sheet ready?
- **Your answer:**

**Question:** What is your target for these numbers at customer #500? (See Section 19.)
- **Your answer:**

**Done when:**
- [ ] Quarterly access reviews done and recorded
- [ ] All High-impact secrets rotate automatically or on a tested manual schedule
- [ ] Leak drill repeated in the last 6 months
- [ ] Plan reviewed and version updated (`v1.x`)
- [ ] Customer-facing security answers prepared and reviewed by Security Owner

---

## 9. Creating and Storing Secrets

**Question:** Who may create a new secret, and what must they do right after? (Recommended: add a row in Section 6, then store only in the vault.)
- **Your answer:**

**Question:** What minimum strength do you require?
- **Your answer:**
- **[TECH] Recommended:** Generate randomly using a cryptographically secure generator. At least 32 random characters (or 256 bits) for tokens and keys. Never invent passwords by hand for machines.

**Question:** How are secrets shared with a person who legitimately needs one? (Recommended: grant vault access. Never send the value through chat or email.)
- **Your answer:**

**Question:** What do you do with temporary secrets for one-off tasks? (Recommended: expire within 24 hours and delete afterwards.)
- **Your answer:**

**Question:** How are secrets encrypted at rest and in transit?
- **Your answer:**
- **[TECH] Recommended:** AES-256 at rest through the KMS. TLS 1.2 or higher in transit. Use current, well-reviewed algorithms only.

**Question:** What rules apply to encryption keys (not just passwords)? Who can use them, and who can manage them? (Recommended: different people for each.)
- **Your answer:**

---

## 10. Rotation and Expiry

**Question:** What is the rotation schedule for each type? Adjust the suggestions to your needs, and write why if you pick a longer period.

| Secret type | Suggested rotation | Your choice | Automatic or manual? | Who does it |
|---|---|---|---|---|
| Database passwords | Dynamic/short-lived, or every 90 days | | | |
| Third-party API keys | Every 90 days | | | |
| OAuth client secrets | Every 180 days | | | |
| JWT / signing keys | Every 6-12 months, with overlap period | | | |
| Encryption keys (KMS) | Yearly, with automatic key rotation where supported | | | |
| TLS certificates | Automatic, renewed well before expiry (follow current maximum lifetimes) | | | |
| CI/CD tokens | Every 90 days, or use short-lived OIDC | | | |
| SSH keys | Every 12 months, or use short-lived certificates | | | |
| Admin / break-glass | After every use, plus every 90 days | | | |

**Question:** How do you rotate without downtime? (Recommended: two valid versions at once during a short overlap, switch apps over, then retire the old one.)
- **Your answer:**

**Question:** Who gets a reminder before a secret expires, how many days ahead, and what happens if nobody acts?
- **Your answer:**
- **Example answer:** "Owner and backup are alerted 30, 14 and 7 days ahead. If not rotated 3 days before, the Security Owner escalates to the Eng Lead."

**Question:** When must you rotate immediately (outside the schedule)? (Recommended triggers: suspected leak, person with access leaves, vendor breach, device lost.)
- **Your answer:**

---

## 11. Access Control

**Question:** How do people sign in to the secrets manager? (Recommended: company single sign-on with multi-factor authentication. No shared accounts.)
- **Your answer:**

**Question:** What groups or roles exist, and what can each do?

| Role / Group | Can read | Can create/change | Can delete | Needs approval? |
|---|---|---|---|---|
| Developer | dev only | dev only | No | No |
| QA | stg only | No | No | No |
| DevOps | stg, prod (limited) | Yes | No | Yes for prod |
| Security Owner | audit logs, all metadata | policy | No | Yes |
| Break-glass | all | all | all | Two people, logged |

- **Your answer (adjust the table to match your team):**

**Question:** How often do you review who has access? (Recommended: every quarter, and immediately when roles change.)
- **Your answer:**

**Question:** What is the exact "leaver checklist" for removing access when someone leaves?
- **Your answer:**

**Question:** How do you handle contractors and vendors? (Recommended: named accounts, time-limited access, removed on contract end.)
- **Your answer:**

---

## 12. CI/CD and Deployment Pipelines

**Question:** Which CI/CD system do you use, and how do pipeline jobs get secrets?
- **Your answer:**
- **[TECH] Recommended:** Use OIDC federation so the pipeline gets short-lived cloud credentials without stored keys. Use environment-scoped secrets with required approvals for production. Pin third-party actions/plugins to a specific commit.

**Question:** Which pipeline jobs may access production secrets? Which may not?
- **Your answer:**
- **Example answer:** "Only the `deploy-prod` job on the `main` branch after manual approval. Pull requests from forks never get secrets."

**Question:** How do you stop secrets printing in build logs?
- **Your answer:**

**Question:** How do you protect build artifacts and container images from embedding secrets?
- **Your answer:**

**Question:** How do you control who can change pipeline files (since changing them could steal secrets)?
- **Your answer:**

---

## 13. Developer Workstations and Code Repositories

**Question:** What rules apply to laptops? (Recommended: disk encryption, screen lock, no secrets stored in plain-text files, no long-lived production credentials on laptops.)
- **Your answer:**

**Question:** How is the repository protected? Tick all that apply.
- [ ] Branch protection on main
- [ ] Required code reviews
- [ ] Secret scanning with push protection turned on
- [ ] Access limited to people who need it
- [ ] Signed commits
- **Your answer (notes):**

**Question:** What do you do if a secret is found in git history? (Recommended: revoke and rotate first. Rewriting history is secondary because the secret must be treated as exposed.)
- **Your answer:**

**Question:** How are secrets kept out of screenshots, screen recordings, support tickets and demo videos?
- **Your answer:**

---

## 14. Third-Party Services, Customer Secrets and Data

**Question:** Which outside services receive or issue secrets for you (payments, email, SMS, analytics, cloud, AI providers)? For each, say who owns the account and what happens if the vendor is breached.

| Vendor | What secret they issue | Account owner | Alerts on breach? | Replacement plan |
|---|---|---|---|---|
| | | | | |

**Question:** Do customers give you their own credentials or keys (for example, to connect their accounts)? If yes, how are these stored, encrypted and deleted?
- **Your answer:**

**Question:** Does your product issue secrets to customers (API keys, tokens)? How are they shown, stored (hashed), limited and revoked?
- **Your answer:**
- **[TECH] Recommended:** Show the key once. Store only a hash. Allow customers to rotate and revoke. Support scoped permissions. Detect and auto-revoke leaked keys where possible.

**Question:** Do you have a process for customers who want to use their own encryption keys or ask for key deletion when they leave?
- **Your answer:**

---

## 15. AI Agent and AI Assistant Rules

> AI coding assistants, chat tools and autonomous agents can read files, run commands and call tools. If they can see a secret, assume the secret can leak (through prompts, logs, memory, or an attacker's instructions hidden in a web page or file).

**Question:** Which AI tools and agents are used in this project, and what can each do? (Writing code, running commands, deploying, reading data, calling services.)

| AI tool / agent | What it can do | What it can access | Who approved it |
|---|---|---|---|
| | | | |

**Question:** How does each AI tool get the access it needs? (Recommended: its own identity, narrow permissions, short-lived credentials, development environment only.)
- **Your answer:**

**Rules (tick to confirm):**
- [ ] **AI-1.** Never paste a real secret into a prompt, chat, issue or file that an AI can read.
- [ ] **AI-2.** AI agents never receive production secrets. If production work is needed, a human approves each action.
- [ ] **AI-3.** Each agent has its own identity, not a developer's personal login or a shared key.
- [ ] **AI-4.** Agent permissions are the smallest possible and expire (hours, not months).
- [ ] **AI-5.** AI-generated code is scanned for hard-coded secrets like any other code.
- [ ] **AI-6.** Agent actions (commands run, files read, calls made) are logged and reviewed.
- [ ] **AI-7.** Agents treat instructions found in files, web pages, emails and tool results as untrusted data. They do not follow them without a human saying so.
- [ ] **AI-8.** Agents never print, summarise or copy secret values into outputs, commits, logs or tickets.
- [ ] **AI-9.** AI tools that send data to outside providers are approved first, and the data sent is checked for secrets and customer data.
- [ ] **AI-10.** Agents cannot make irreversible changes (delete data, change access, publish) without human approval.
- [ ] **AI-11.** LLM provider API keys are in Section 6, rotated, usage-limited and budget-capped.

**Question:** How will you check that these rules are followed? (For example: scan agent logs, review pull requests, test that the agent is denied production access.)
- **Your answer:**

**Question:** What do you do if an AI tool saw or printed a real secret? (Recommended: treat it as a leak and follow Section 16.)
- **Your answer:**

**Question:** Does the product itself contain AI features that handle secrets or customer credentials (for example, an AI assistant that calls customer systems)? How are those secrets isolated from the model?
- **Your answer:**
- **[TECH] Recommended:** Keep secrets in the tool layer outside the model. The model never sees raw credentials. Tools use scoped, short-lived tokens, and every call is logged.

---

## 16. Monitoring, Logging and Alerts

**Question:** What is logged about secrets? (Recommended: every read, create, update, delete, permission change and failed attempt, with who, what, when and from where.)
- **Your answer:**

**Question:** Where are logs kept, who can read them, can anyone edit or delete them, and how long are they kept?
- **Your answer:**
- **[TECH] Recommended:** Send to a separate, write-once log store. Keep at least 12 months (check your compliance needs).

**Question:** Which events trigger an alert, who receives it, and how fast must they respond?

| Event | Alert to | Response time |
|---|---|---|
| Secret read from unusual place/time | | |
| Many failed vault logins | | |
| Secret scanner finds a key | | |
| Secret about to expire | | |
| Break-glass account used | | |
| Access policy changed | | |
| Spike in third-party API usage | | |

**Question:** Who reviews audit logs, and how often? (Recommended: weekly spot check, monthly full review.)
- **Your answer:**

---

## 17. Incident Runbook: "A Secret Has Leaked"

> **Print this section or keep a copy outside the vault.** Revoke first, investigate second.

**Question:** Who is the incident lead, and how do you reach them at any hour? List backups.
- **Your answer (names, phones, chat handles):**

**Question:** What is the target time to revoke a leaked High-impact secret after discovery? (Recommended: under 1 hour.)
- **Your answer:**

### Steps

**Step 1: Confirm and call it.** Anyone who suspects a leak says so in the incident channel and names the secret ID from Section 6. No blame.

**Step 2: Contain (within the target time).**
- [ ] Revoke or disable the secret right now, or rotate it immediately.
- [ ] Remove it from any public place you can (repo, paste, chat) after revoking. Revoking matters more than deleting.
- [ ] Block related sessions/tokens if relevant.

**Step 3: Replace.**
- [ ] Create the new secret in the vault.
- [ ] Update dependent apps and confirm they work.
- [ ] Record the change in Section 6.

**Step 4: Investigate.**
- [ ] Check audit logs from the time of exposure until revocation: who used it, from where, what was accessed.
- [ ] Check the vendor's logs and dashboards where possible.
- [ ] Decide what data or systems may have been touched.

**Step 5: Decide who must be told.**
- [ ] Internal leaders
- [ ] Affected customers
- [ ] Regulators, if personal data may be affected (many privacy laws have strict deadlines, for example 72 hours under GDPR; check Section 18 and ask Legal)
- [ ] Payment, cloud or other vendors as required by contract

**Step 6: Recover and learn.**
- [ ] Write a short review within 5 working days: what happened, how it was found, how long it took, what fixes will stop it happening again.
- [ ] Add fixes to the backlog with owners and dates.
- [ ] Update this document if a gap was found.

### Quick contact table
| Who | Name | Phone / chat | Backup |
|---|---|---|---|
| Incident lead | | | |
| Security Owner | | | |
| Cloud / DevOps | | | |
| Legal / Privacy | | | |
| Customer comms | | | |
| Vendor security contacts | | | |

### Practice drill
**Question:** When was the last leak drill, how long did revocation take, and what did you fix? (Run one before launch and at least every 6 months.)
- **Your answer:**

### Incident log (add one row per incident)
| Date | Secret ID | How found | Time to revoke | Data affected? | Review link | Fixes done? |
|---|---|---|---|---|---|---|
| | | | | | | |

---

## 18. Backup, Recovery and Offboarding

**Question:** How is the secrets manager itself backed up, and how do you recover if it is lost? Has recovery been tested?
- **Your answer:**

**Question:** Where is the break-glass (emergency) access stored, who can open it, and how do you know when it was used?
- **Your answer:**

**Question:** What happens to secrets when a project is retired or a customer leaves? (Recommended: delete or disable all related secrets and record it.)
- **Your answer:**

**Question:** How do you destroy old secrets and keys safely when they are retired? (Recommended: disable, wait a safe period, then delete, and log it.)
- **Your answer:**

---

## 19. Compliance and Governance Mapping

> This table is a helper, not legal advice. Confirm exact requirements with your auditor or legal advisor. Tick only what applies to you.

**Question:** Which of these apply to your product?
- [ ] SOC 2
- [ ] ISO/IEC 27001
- [ ] GDPR and other privacy laws (name them: )
- [ ] HIPAA
- [ ] PCI DSS
- [ ] Other:
- **Your answer:**

| Topic | What this plan covers | Where | Typical references (verify) |
|---|---|---|---|
| Access control and least privilege | Roles, reviews, leaver process | Sections 3, 11 | SOC 2 CC6; ISO 27001 Annex A access control and access rights; PCI DSS Req. 7, 8 |
| Authentication information | Strong generation, storage, rotation | Sections 9, 10 | ISO 27001 Annex A authentication information; PCI DSS Req. 8 |
| Cryptography and key management | KMS, key rotation, key custody | Sections 5, 9, 10 | ISO 27001 Annex A use of cryptography; PCI DSS Req. 3 (key management); HIPAA technical safeguards |
| No hard-coded credentials | Scanning, code rules | Sections 4, 8, 13 | PCI DSS Req. 8.6 (application/system account passwords) |
| Logging and monitoring | Audit trail, alerts | Section 16 | SOC 2 CC7; ISO 27001 Annex A logging; PCI DSS Req. 10; HIPAA audit controls |
| Incident response and breach notice | Runbook, notification | Section 17 | SOC 2 CC7; GDPR Art. 33-34; HIPAA breach rules; PCI DSS Req. 12.10 |
| Data protection by design | Separation, minimization, encryption | Sections 7, 9, 14 | GDPR Art. 25 and 32 |
| Supplier / vendor security | Vendor secrets, offboarding | Sections 11, 14 | SOC 2 CC9; ISO 27001 supplier relationships |
| Change and configuration management | Pipeline controls, approvals | Section 12 | SOC 2 CC8; ISO 27001 configuration/change management |

**Question:** What evidence will you keep to prove each control works? (Screenshots, exported access reviews, rotation logs, drill reports, scan results.) Where is it stored and for how long?
- **Your answer:**

**Question:** Who is the compliance contact and when is the next audit or assessment?
- **Your answer:**

---

## 20. Launch Gate Checklist (Final "Go / No-Go" Before Customers)

Every box must be ticked. Any unticked box needs an approved written exception (Section 21).

**People and process**
- [ ] Sections 0-18 answered, no blanks
- [ ] All roles named with backups
- [ ] Incident runbook tested in a drill
- [ ] On-call schedule covers launch week

**Secrets**
- [ ] Section 6 inventory complete and checked against the real systems
- [ ] Every production secret created fresh and unique to production
- [ ] No secret older than its rotation period
- [ ] Break-glass access created, tested and protected

**Code and pipeline**
- [ ] Full repo and history scan clean
- [ ] Pre-commit, push protection and CI scanning on
- [ ] Pipeline uses short-lived credentials where possible
- [ ] Production deploy needs human approval

**Access and monitoring**
- [ ] Production access limited to named people with MFA
- [ ] Audit logging and alerts working (tested)
- [ ] Expiry reminders working

**AI**
- [ ] Section 15 rules in force and checked
- [ ] No AI agent has production secrets

**Compliance**
- [ ] Section 19 evidence collected
- [ ] Legal/privacy contact confirmed breach notification steps

**Question:** Are there any exceptions (a box you could not tick)? For each, explain the risk, who accepted it, and the date it will be fixed.
- **Your answer:**

---

## 21. Metrics (Know If This Is Working)

**Question:** What are your targets, and what are the current numbers? Review monthly.

| Measure | Target | Current |
|---|---|---|
| Secrets found in code (should always be 0 in main) | 0 | |
| Time to revoke a leaked High-impact secret | < 1 hour | |
| Secrets past their rotation date | 0 | |
| Secrets with no named owner | 0 | |
| People with production access who no longer need it | 0 | |
| Percent of High-impact secrets rotated automatically | 100% by customer #500 | |
| Quarterly access reviews completed on time | 100% | |
| Leak drills done in the last 6 months | 1+ | |
| Scanner alerts closed within 3 days | 100% | |

---

## 22. Approval and Sign-Off

**Question:** Who approves this plan? Each person confirms they have read and agree.

| Role | Name | Decision (Approve / Reject) | Date | Notes |
|---|---|---|---|---|
| Product Owner | | | | |
| Engineering Lead | | | | |
| Security Owner | | | | |
| QA Lead | | | | |
| Legal / Privacy (if needed) | | | | |

**Question:** When is the next scheduled review? (No later than 90 days from the last one.)
- **Your answer:**

---

## 23. Frequently Asked Questions

**Can I put a secret in a private repository?** No. Private repositories get shared, copied and breached. Use the vault.

**I accidentally committed a key. Am I in trouble?** No. Report it right away. Revoke the key, then follow Section 17. Speed matters, blame does not.

**Can I send a password to a teammate in chat?** No. Give them vault access instead.

**Can an AI assistant see my `.env` file?** Only if it contains dev-only fake or low-risk values. Real or production secrets must never be readable by AI tools.

**Do test keys count as secrets?** Yes, treat them carefully. They are lower risk but can still be misused.

**What if the vault goes down?** See Section 5. Plan this before launch, not during an outage.

**We are tiny. Is this too much?** Start with Sections 4, 6, 8 (Phases 1-4), 10 and 17. Add the rest as you grow, and write `N/A: not yet, revisit on <date>` instead of leaving blanks.

**When do I update this document?** When you add a secret, tool, vendor, AI agent, environment or team member, after any incident, and at every review date.

---

## 24. Glossary

| Term | Meaning |
|---|---|
| **API key** | A password-like string a program uses to talk to a service |
| **Audit log** | A record of who did what and when |
| **Break-glass account** | Emergency access, rarely used, tightly watched |
| **CI/CD** | Automated build, test and deploy pipeline |
| **HSM** | Special hardware that protects encryption keys |
| **JWT** | A signed token that proves a user is logged in |
| **KMS** | Key Management Service: creates and guards encryption keys |
| **MFA** | Multi-factor authentication: a second proof besides a password |
| **OIDC federation** | A way for pipelines to get temporary access without stored passwords |
| **Principle of least privilege** | Only the minimum access needed |
| **Rotation** | Replacing a secret on a schedule |
| **Secret zero** | The first secret a program needs to reach the vault, which should be replaced by a machine identity |
| **Short-lived credential** | A key that expires quickly on its own |
| **Threat model** | A list of how things could go wrong and how you will prevent it |

---

## 25. Appendix A: Quick-Start Commands (for engineers) [TECH]

Examples only. Check each tool's current documentation before use.

```bash
# Scan the current repo and its full git history for secrets (gitleaks)
gitleaks detect --source . --log-opts="--all" --redact

# Scan only staged changes before committing
gitleaks protect --staged --redact

# Scan a repo's history (trufflehog), showing only verified findings
trufflehog git file://. --only-verified

# Pre-commit hook config snippet (.pre-commit-config.yaml)
# repos:
#   - repo: https://github.com/gitleaks/gitleaks
#     rev: <pin a specific release>
#     hooks:
#       - id: gitleaks
```

Suggested `.gitignore` lines:

```
.env
.env.*
!.env.example
*.pem
*.key
*.p12
*.pfx
credentials.json
service-account*.json
```

## 26. Appendix B: Filled-In Mini Example (so you can see the style)

> **Product:** InvoiceBuddy
> **Section 6 row:** S-001, Payment API key, unlocks charges and refunds, prod, `prod/payments/stripe-key`, owner Priya Shah, rotates every 90 days, next rotation 2026-12-30, readable only by the payments service role, impact High.
> **Section 12 answer:** "GitHub Actions gets short-lived cloud access through OIDC. Only the `deploy-prod` job on `main`, after manual approval by the Eng Lead, can read production secrets. Pull requests from forks get none."
> **Section 15 answer:** "Our coding assistant works in dev only with a dev-scoped token that expires after 8 hours. It cannot reach the production vault. Its command log is reviewed weekly."

## 27. Change Log

| Version | Date | Author | What changed | Approved by |
|---|---|---|---|---|
| v0.1 | | | First draft | |
| | | | | |
