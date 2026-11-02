# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

> **Template version:** 1.1 | **Folder:** `Deployment and production operations/` | **File:** `Backup_and_Restore_Plan.md`
> **Covers:** AI-driven development, from the first line of code to your first 500 customers.

## What this document is, in one sentence
A **backup** is a safe copy of your important stuff. A **restore** is using that copy to get everything back after something goes wrong. This document is your written promise of **what you copy, how often, where it lives, and exactly how you bring it back**.

## Who can fill this out
Anyone. You do not need to be a programmer. If you can answer a question like "What is your favorite game?", you can answer these questions. If a word is new, look in the **Glossary (Section 18)**.

## The 7 rules
1. **Answer every question.** Write your answer on the line marked `ANSWER:` or fill in the table cell. Tick a box by changing `[ ]` to `[x]`.
2. **Never leave a blank.** If something does not apply, write `N/A - because <reason>`. If you do not know, write `UNKNOWN - owner: <name> - due: <date>`. Do not guess.
3. **Never write secrets here.** No passwords, API keys, tokens, or private keys. Write *where* the secret is stored (for example "in our password manager, vault: Ops") instead.
4. **Use real names and real dates.** Write "Priya Shah" not "the team". Write `2026-11-03` not "soon". Use the format `YYYY-MM-DD`.
5. **Use numbers, not feelings.** Write "every 15 minutes", not "often". Write "30 days", not "a while".
6. **Look for the status tags.** Each section starts with a tag:
   - `[REQUIRED]` must be filled before launch.
   - `[RECOMMENDED]` should be filled; skip only with a written reason.
   - `[IF APPLICABLE]` fill only when it applies to your project; otherwise write `N/A - because ...`.
7. **A backup you never tested is only a hope.** Section 9 forces you to prove your restores work.

## Example of a good answer vs. a bad answer
| Question | Bad answer | Good answer |
|---|---|---|
| How often is the database backed up? | "Regularly" | "Continuous log backup, plus a full snapshot every day at 02:00 UTC" |
| Who restores the data? | "DevOps" | "Primary: Sam Lee (sam@example.com). Backup: Ana Cruz." |
| Where are backups stored? | "In the cloud" | "Provider B, region eu-west-1, bucket `acme-prod-backups`, separate account from production" |

## How to know you are done
- Run the **Completion Score** in Section 19. You need **100% of `[REQUIRED]` items** answered and **no unexplained `UNKNOWN`**.
- Section 16 (Launch Readiness Checklist) must be fully ticked before you go live.
- Have **one other person** read it and try to follow a restore runbook (Section 8) using only this document.

## Instructions for AI agents filling this out
If you are an AI agent helping with this document:
- Ask the human the questions one section at a time. **Do not invent answers.**
- Pull facts from repos, infrastructure files, and cloud consoles when you have read access; cite the source next to the answer (`SOURCE: terraform/main.tf`).
- Mark anything you inferred with `[AI-INFERRED - human must confirm]`.
- Never read, copy, or write secret values. Record only the secret's location.
- Never run a restore against **production** unless a named human approves in writing (Section 13).
- Keep a change line in Section 17 each time you edit.

## Working alone? Solo-founder rules
If you are a team of one, you may fill several roles yourself, **but**:
1. Name **one trusted outside person** (co-founder, advisor, family member, lawyer, or a sealed emergency envelope) who can reach your recovery info (Section 6.5) if you are unavailable.
2. You cannot approve your own production restore. Wait 15 minutes, re-read the safety checklist (Section 8.0), and write the approval line (Section 13.4) in your own words before acting.
3. Pick a second "backup contact" for every role in Section 11, even if that person is outside the company.

## Machine-readable summary (AI agents and tools read this block)
*Fill this in last, after the rest of the document is complete. Keep it in sync with the sections named in the comments.*

```yaml
backup_restore_plan:
  template_version: "1.1"
  project_name: ""              # Section 0
  owner: ""                     # Section 0
  lifecycle_stage: ""           # Section 2.1: build | staging | pre-launch | launch | customers-1-50 | customers-51-500
  environments: []              # Section 1.4
  team_mode: ""                 # solo | team
  data_items:                   # Section 3.2, one entry per row
    - name: ""
      system: ""
      tier: ""                  # tier-1 | tier-2 | tier-3 | tier-4
      rpo_target: ""            # e.g. "15m"
      rto_target: ""            # e.g. "4h"
      backup_method: ""         # Section 5.3
      frequency: ""
      primary_location: ""      # Section 6.1
      second_location: ""
      immutable_copy: false
      encrypted_at_rest: false
      retention: ""             # Section 7.1
      owner: ""
  restore_approver: ""          # Section 8 / 13.4
  last_full_restore_drill: ""   # YYYY-MM-DD, Section 9.2
  last_drill_passed: false
  next_review_due: ""           # YYYY-MM-DD
  compliance_frameworks: []     # Section 12.1
  launch_go_no_go: ""           # GO | NO-GO, Section 16
```

---

# 0. DOCUMENT CONTROL `[REQUIRED]`

| Field | ANSWER |
|---|---|
| Project name | |
| Project code / repo URL | |
| Document owner (one named person) | |
| Reviewer (a different person) | |
| Date created (`YYYY-MM-DD`) | |
| Last reviewed (`YYYY-MM-DD`) | |
| Next review due (must be within 90 days of last review) | |
| Document status | [ ] Draft  [ ] In review  [ ] Approved  [ ] Retired |
| Approved by (name + date) | |

---

# 1. PROJECT SNAPSHOT `[REQUIRED]`
*Goal: anyone reading this should understand your product in 60 seconds.*

**1.1 In one or two sentences, what does your product do?**
ANSWER:

**1.2 Who uses it?** [ ] Public customers  [ ] Businesses (B2B)  [ ] Internal staff only  [ ] Children / minors  [ ] Other: ______

**1.3 Where does it run?** (tick all that apply)
- [ ] Web app  [ ] Mobile app  [ ] API only  [ ] Desktop app  [ ] AI/LLM features  [ ] Background jobs  [ ] IoT/hardware

**1.4 Where is it hosted?**
| Item | ANSWER |
|---|---|
| Hosting provider(s) | |
| Region(s) / country | |
| Environments that exist | [ ] Development  [ ] Staging  [ ] Production  [ ] Other: ____ |

**1.5 What happens to your business if ALL data disappears today?**
- [ ] Nothing serious  [ ] Annoying, recoverable by hand  [ ] We lose customers  [ ] We lose money fast  [ ] Legal or safety harm  [ ] The company could not survive

ANSWER (explain in 1-3 sentences):

---

# 2. WHERE ARE YOU IN THE LIFECYCLE? `[REQUIRED]`
*Backups should get stronger as your product grows. Find your stage, then meet **at least** that stage's minimum.*

**2.1 Tick your CURRENT stage (tick one):**
- [ ] Stage 1: Build (writing code, no real users)
- [ ] Stage 2: Staging / Test (testers only)
- [ ] Stage 3: Pre-launch (final checks, real data may be loaded)
- [ ] Stage 4: Launch day and first 2 weeks
- [ ] Stage 5: Customers 1-50
- [ ] Stage 6: Customers 51-500

**2.2 The Maturity Ladder: minimum backup rules by stage**

| Stage | Minimum data protection | Minimum restore proof | Who signs off |
|---|---|---|---|
| 1. Build | Code in version control (Git), pushed to a remote. Dev data is disposable and rebuildable by script. | Rebuild dev environment from scratch once. | Developer |
| 2. Staging | Daily automatic backup of any shared database. Infrastructure written as code/config files and saved in Git. | Restore staging DB to a scratch copy once. | Tech lead |
| 3. Pre-launch | Production backups switched ON before the first real customer record. Encryption ON. Backups stored in a **separate account/location** from production. Secrets recovery path documented. | Full restore drill in a non-production copy; record actual time taken (Section 9). | Tech lead + Owner |
| 4. Launch & first 2 weeks | Everything in Stage 3, plus automatic failure alerts and a named on-call person. Point-in-time recovery enabled if the database supports it. | Restore test within the first 7 days live. | Owner |
| 5. Customers 1-50 | Everything above, plus **off-site/second-provider copy** of critical data, and customer-uploaded files protected. | Monthly restore test. | Owner |
| 6. Customers 51-500 | Everything above, plus restore drills against realistic data volume, written customer-facing recovery commitments, and an annual disaster-recovery exercise. | Monthly restore test + one full "disaster day" simulation every 6 months. | Owner + Reviewer |

**2.3 Is your project currently meeting the minimum for its stage?** [ ] Yes  [ ] No
If No, list gaps and who fixes them by when:

| Gap | Owner | Due date |
|---|---|---|
| | | |

---

# 3. WHAT MUST BE BACKED UP? (THE DATA MAP) `[REQUIRED]`
*Goal: a complete list of everything you would be sad to lose. If it is not on this list, it will not be backed up.*

**3.1 Tick every kind of thing your project has, then fill the table below.**

| Tick | Category | Examples |
|---|---|---|
| [ ] | Source code | App code, scripts, AI agent configs |
| [ ] | Databases | Customer accounts, orders, settings |
| [ ] | File storage | Uploads, images, invoices, exports |
| [ ] | Infrastructure setup | Server config, cloud setup files, DNS records, certificates |
| [ ] | Secrets and keys | Where passwords/API keys live (not the secrets themselves) |
| [ ] | CI/CD pipelines | Build and deploy definitions |
| [ ] | AI assets | Prompts, system instructions, fine-tuned models, embeddings/vector database, evaluation datasets |
| [ ] | Logs and audit trails | Security logs, billing logs |
| [ ] | Third-party SaaS data | Payments, email provider, CRM, analytics, support desk |
| [ ] | Documentation | Runbooks, wiki, this document |
| [ ] | Messaging/queues | Pending jobs, event streams |
| [ ] | Analytics/data warehouse | Reports, dashboards |
| [ ] | Other: ______ | |

**3.2 Data inventory table** (one row per item; add rows as needed)

| # | Data item | Where it lives (system) | Type | Size now | Growth/month | Contains personal data? | Criticality (see 4.1) | Owner |
|---|---|---|---|---|---|---|---|---|
| 1 | Example: Customer database | Managed Postgres, prod | Database | 2 GB | +300 MB | Yes | Tier 1 | Sam Lee |
| 2 | | | | | | | | |
| 3 | | | | | | | | |

**3.3 Is anything deliberately NOT backed up?** (for example caches, temp files, rebuildable data)

| Item | Why it is safe not to back it up | How it is rebuilt |
|---|---|---|
| | | |

**3.4 Third-party services: do THEY back up your data, and can you get it out?**

| Service | What data they hold | Do they back it up? | Can we export it ourselves? | How/how often we export |
|---|---|---|---|---|
| | | | | |

> Warning: "The vendor handles it" is not an answer until you have read their backup policy and confirmed you can export your data.

---

# 4. HOW MUCH LOSS CAN YOU SURVIVE? (RPO AND RTO) `[REQUIRED]`

**Plain-English definitions:**
- **RPO (Recovery Point Objective)** = the **most data you can afford to lose**, measured in time. RPO of 15 minutes means "if disaster strikes, we may lose up to the last 15 minutes of data."
- **RTO (Recovery Time Objective)** = the **longest you can be down** before it seriously hurts. RTO of 4 hours means "we must be working again within 4 hours."

**4.1 Criticality tiers (use these to fill the table in 4.2):**

| Tier | Meaning | Suggested RPO | Suggested RTO |
|---|---|---|---|
| Tier 1: Critical | Business stops without it (customer data, payments, auth) | 0-15 minutes | 1-4 hours |
| Tier 2: Important | Painful to lose; workarounds exist | 1-24 hours | 4-24 hours |
| Tier 3: Useful | Nice to have back | 24 hours-7 days | 1-7 days |
| Tier 4: Rebuildable | Can be regenerated by script | Not needed | As needed |

**4.2 Your targets**

| Data item (from 3.2) | Tier | Target RPO | Target RTO | Proven RPO (from last drill) | Proven RTO (from last drill) | Target met? |
|---|---|---|---|---|---|---|
| | | | | | | [ ] Yes [ ] No |

**4.3 What do customers expect or are promised?** (SLAs, contracts, marketing pages)
- [ ] No promises made  [ ] Promised in contract/SLA  [ ] Stated on website
ANSWER (quote the promise and where it is written):

**4.4 What disasters are you protecting against?** (tick all you are planning for)

| Tick | Disaster | Likelihood (L/M/H) | Impact (L/M/H) | Covered in runbook # |
|---|---|---|---|---|
| [ ] | Someone deletes data by accident | | | |
| [ ] | Bad deploy or bad database migration corrupts data | | | |
| [ ] | AI agent or automation deletes/overwrites something | | | |
| [ ] | Ransomware or hacker deletes/encrypts data | | | |
| [ ] | Insider misuse | | | |
| [ ] | Hosting provider outage (one zone) | | | |
| [ ] | Hosting provider outage (whole region) | | | |
| [ ] | Provider account suspended or locked out | | | |
| [ ] | Lost access to credentials/MFA | | | |
| [ ] | Expired domain or certificate | | | |
| [ ] | Third-party service shuts down or loses our data | | | |
| [ ] | Hardware failure or storage corruption | | | |
| [ ] | Natural disaster/power loss at provider site | | | |
| [ ] | Key person unavailable (illness, leaves company) | | | |
| [ ] | Other: ______ | | | |

---

# 5. BACKUP STRATEGY (HOW YOU COPY THINGS) `[REQUIRED]`

**5.1 The golden rule: "3-2-1-1-0"**
Aim for: **3** copies of your data, on **2** different kinds of storage, **1** copy off-site, **1** copy that cannot be changed or deleted (immutable/offline), and **0** errors when you test restoring.

**Check where you stand:**
- [ ] 3+ copies exist (the live data counts as one)
- [ ] At least 2 different storage types or services
- [ ] At least 1 copy in a different location/account/provider than production
- [ ] At least 1 copy is immutable (write-once, object lock, or offline)
- [ ] Restore tested with zero errors (Section 9)

For anything unchecked, write your reason or plan:
ANSWER:

**5.2 Backup methods used** (tick all that apply)
- [ ] Full backup (a complete copy)
- [ ] Incremental backup (only what changed since last backup)
- [ ] Differential backup (what changed since last full)
- [ ] Continuous / log shipping / point-in-time recovery
- [ ] Storage snapshots
- [ ] Logical export (for example a SQL dump or JSON export)
- [ ] Versioning on file storage
- [ ] Replication to another region (note: replication is **not** a backup on its own, because it copies mistakes too)
- [ ] Git mirror
- [ ] Vendor-managed backups
- [ ] Other: ______

**5.3 Backup schedule: fill one row per data item**

| Data item | Method | Frequency | Time (with time zone) | Tool/service doing it | Backup location | Backup owner |
|---|---|---|---|---|---|---|
| Example: Customer DB | Continuous log + daily full | Continuous / daily | 02:00 UTC | Managed DB backups | Provider B, bucket X | Sam Lee |
| | | | | | | |

**5.4 Does the backup need to be "application-consistent"?** (the database and files must match each other)
- [ ] Not needed  [ ] Yes. We pause writes or use a consistent snapshot. Explain how:

ANSWER:

**5.5 Everything-as-code check** (can you rebuild the whole system from files in Git?)
- [ ] Infrastructure as code exists  [ ] Config as code exists  [ ] Build/deploy pipeline as code  [ ] Documented manual steps only
ANSWER (where in Git):

**5.6 AI-specific backups** `[IF APPLICABLE]`
| Asset | Where stored | Version-controlled? | Backup frequency | Can it be recreated if lost? |
|---|---|---|---|---|
| Prompts and system instructions | | | | |
| Agent/skill/workflow definitions | | | | |
| Vector database / embeddings | | | | |
| Fine-tuned model files or adapters | | | | |
| Evaluation datasets and test cases | | | | |
| Conversation / memory stores | | | | |

---

# 6. STORAGE, SECURITY AND ACCESS `[REQUIRED]`

**6.1 Where backups live**
| Question | ANSWER |
|---|---|
| Primary backup location (provider, region, bucket/vault name) | |
| Second copy location (different provider/region/account) | |
| Immutable or offline copy location | |
| Is the backup account **separate** from the production account? | [ ] Yes  [ ] No |
| Distance/independence from production (same region? same provider?) | |

**6.2 Encryption**
- [ ] Backups encrypted **in transit** (while moving)  Method: ______
- [ ] Backups encrypted **at rest** (while stored)  Method: ______
- Where are the **encryption keys** stored? ______
- Who can access the keys (names/roles)? ______
- [ ] Keys are themselves backed up separately from the data
- [ ] Key rotation schedule: every ______ months

> If you lose the encryption key, the backup is useless. Test key recovery.

**6.3 Who can touch backups?**
| Person / role | Can create | Can read | Can restore | Can delete | Needs 2nd person approval to delete? |
|---|---|---|---|---|---|
| | | | | | |

- [ ] Multi-factor authentication (MFA) required for backup access
- [ ] Production credentials cannot delete backups (separation of duties)
- [ ] Access reviewed every ______ months; last review: `YYYY-MM-DD`
- [ ] Break-glass (emergency) access exists. Where is it documented? ______

**6.4 Ransomware and tampering protection**
- [ ] Immutable/write-once storage with a lock period of ______ days
- [ ] Backup deletion requires a delay or second approval
- [ ] Backups are not mounted or writable from production servers
- [ ] Anomaly alerts (mass deletion, sudden size drops)

**6.5 Secrets and access recovery** (can you get back in if everything is gone?)
| Item | Where the recovery info is kept (NOT the secret itself) | Who can access | Last tested |
|---|---|---|---|
| Cloud provider root/admin account | | | |
| Domain registrar and DNS | | | |
| Password manager master recovery | | | |
| MFA recovery codes | | | |
| Source control admin | | | |
| Payment provider account | | | |
| Code signing / app store accounts | | | |

---

# 7. HOW LONG DO YOU KEEP BACKUPS? (RETENTION) `[REQUIRED]`

**7.1 Retention schedule** (a common starting point is shown in the example row)

| Data item | Hourly kept for | Daily kept for | Weekly kept for | Monthly kept for | Yearly kept for | Reason for these numbers |
|---|---|---|---|---|---|---|
| Example: Customer DB | 48 hours | 30 days | 12 weeks | 12 months | 7 years | Contract + tax law |
| | | | | | | |

**7.2 Legal or contractual retention requirements**
- [ ] None  [ ] Tax/financial records  [ ] Healthcare  [ ] Education/children's data  [ ] Customer contract  [ ] Other: ______
ANSWER (name the law/contract and the number of years):

**7.3 Deletion promises: privacy law and customer requests**
- Can a customer ask you to delete their data? [ ] Yes  [ ] No
- When they do, how long until it also leaves **backups**? ______ days
- How do you stop deleted data from coming back after a restore? (for example "re-apply deletion log after every restore")
ANSWER:

**7.4 Legal hold** `[IF APPLICABLE]`
How do you pause deletion of backups if a lawsuit or investigation requires it? Who decides?
ANSWER:

---

# 8. RESTORE RUNBOOKS (HOW TO BRING THINGS BACK) `[REQUIRED]`
*Write these so a tired, stressed person at 3 a.m. who did not build the system can follow them. One runbook per scenario. Copy the template below as many times as needed.*

**8.0 Before ANY restore: the safety checklist**
- [ ] Stop and breathe. Do not delete anything yet.
- [ ] Write down the time and what you believe went wrong.
- [ ] Tell the incident lead (Section 11).
- [ ] **Take a fresh copy of the current broken state** before overwriting it (evidence + safety net).
- [ ] Decide the **restore point** (the moment in time you want to return to).
- [ ] Restore into a **new, separate location first**, check it, and only then switch over, whenever possible.
- [ ] Get written approval from the named approver before touching production.

**8.1 Runbook index**

| # | Scenario | Severity | Owner | Last tested |
|---|---|---|---|---|
| R1 | Restore one deleted record or file | Low | | |
| R2 | Restore a whole table or folder | Medium | | |
| R3 | Restore the full production database (point-in-time) | High | | |
| R4 | Restore file/object storage | High | | |
| R5 | Rebuild the entire environment from code (infrastructure + app) | Critical | | |
| R6 | Recover after ransomware/security breach | Critical | | |
| R7 | Recover from provider/region outage (failover) | Critical | | |
| R8 | Recover lost accounts, credentials, domain or DNS | Critical | | |
| R9 | Recover AI assets (prompts, vector DB, models) | Medium | | |
| R10 | Recover third-party SaaS data | Medium | | |
| R11 | Undo a bad deploy or bad migration | High | | |
| R12 | Other: ______ | | | |

**8.2 Runbook template (copy for each scenario)**

### Runbook R__: <Scenario name>

| Field | ANSWER |
|---|---|
| When to use this runbook (trigger) | |
| Who may start it / approver | |
| Estimated time to finish | |
| What you need before starting (access, tools, links) | |
| Restore point decision (how to choose the time/version) | |

**Step-by-step (write numbered, copy-paste-able steps; one action per step):**
1. 
2. 
3. 

**Verify it worked: ALL must be ticked:**
- [ ] Row counts / file counts match expectation: ______
- [ ] App starts and passes the smoke tests: ______
- [ ] A sample of real records opens correctly: ______
- [ ] No errors in logs for 15 minutes
- [ ] Data between systems is consistent (database vs files vs search index)
- [ ] Deleted-customer data was NOT resurrected (Section 7.3)

**If it fails:** what is the fallback or rollback step? ______
**Who to call next:** ______
**After the restore:** update Section 17 incident log; schedule a "what happened" review within 5 working days.

---

# 9. TESTING: PROVE YOUR BACKUPS WORK `[REQUIRED]`

**9.1 Test schedule** (minimums by stage are in Section 2.2)

| Test type | What it proves | How often | Last done | Next due | Owner |
|---|---|---|---|---|---|
| Backup success check (automatic) | Backups are running | Every run | | | |
| Backup integrity check (checksum/readable) | Files are not corrupt | Weekly | | | |
| Partial restore test (one table/folder) | You can restore small things | Monthly | | | |
| Full restore test (non-production) | You can rebuild everything | Quarterly (monthly from Stage 5) | | | |
| Disaster-day simulation (surprise scenario) | The people and process work | Every 6 months (from Stage 6) | | | |
| Credential/key recovery test | You can still get in | Every 6 months | | | |

**9.2 Restore drill result log** (add a row after every drill)

| Date | Runbook # | Who did it | Restore point used | Time it actually took (RTO) | Data lost (RPO) | Passed? | Problems found | Fix owner + due date |
|---|---|---|---|---|---|---|---|---|
| | | | | | | [ ] Yes [ ] No | | |

**9.3 Pass/fail rule:** a drill **fails** if (tick the rules you adopt)
- [ ] Actual RTO is greater than target RTO
- [ ] Actual RPO is greater than target RPO
- [ ] Any step in the runbook was wrong or missing
- [ ] Restored data failed verification
- [ ] Only one person could do it
A failed drill must be fixed and **re-run** within ______ days.

---

# 10. MONITORING AND ALERTS `[REQUIRED]`

| What to watch | Alert when | Sent to (person/channel) | Response time target |
|---|---|---|---|
| Backup job failed or did not run | Any failure or missed schedule | | 1 hour |
| Backup size changed suddenly | Size changes more than ____% | | 1 day |
| Backup age (newest backup is too old) | Older than ______ | | 1 hour |
| Storage nearly full | Over ____% | | 1 day |
| Replication/log shipping lag | Over ______ | | 1 hour |
| Unusual deletion or access to backups | Any | | Immediate |
| Restore test overdue | Past due date | | 1 week |
| Backup encryption key or credential expiry | ____ days before | | 1 week |

- Where is the backup dashboard/status page? ______
- Who checks it, and how often? ______
- What happens if the person receiving alerts is on vacation? (backup contact): ______

---

# 11. PEOPLE, ROLES AND COMMUNICATION `[REQUIRED]`

**11.1 Who does what**

| Role | Name | Phone/contact | Backup person | Time zone/hours |
|---|---|---|---|---|
| Incident lead (decides) | | | | |
| Restore operator (does the work) | | | | |
| Approver for production restores | | | | |
| Security contact | | | | |
| Communications lead (talks to customers) | | | | |
| Executive/owner to inform | | | | |
| Legal/privacy contact | | | | |
| Vendor/provider support contact | | | | |

- Team mode: [ ] Solo (see "Solo-founder rules" at the top)  [ ] Team
- [ ] No role depends on only one person (each has a named backup)
- [ ] Contacts work **outside** the system that may be down (for example personal phone, not only company chat)

**11.2 Severity levels and who gets told**

| Severity | Example | Tell internally within | Tell customers within |
|---|---|---|---|
| SEV1 | Data lost/unavailable for all customers | 15 minutes | 1 hour |
| SEV2 | Part of data affected | 1 hour | 4 hours |
| SEV3 | Small/internal impact | 1 working day | Not needed |

**11.3 Customer message templates** (write them now, not during a crisis)
- Status page used: ______
- Draft "we have a problem" message:

ANSWER:

- Draft "we are fixed, here is what happened" message:

ANSWER:

**11.4 Mandatory legal notifications** `[IF APPLICABLE]`
If personal data is lost or exposed, who must be told, and how fast? (for example regulators within 72 hours under GDPR)
ANSWER:

---

# 12. COMPLIANCE AND AUDIT (ENTERPRISE-GRADE) `[IF APPLICABLE]`
*Tick the frameworks that apply to you. For each ticked row, complete the evidence columns. If none apply, tick "None" and explain why.*

- [ ] None apply because: ______

**12.1 Applicable frameworks**

| Tick | Framework | Why it applies | Backup-related controls to satisfy | Evidence we keep | Evidence location | Owner |
|---|---|---|---|---|---|---|
| [ ] | GDPR / UK GDPR | EU/UK personal data | Availability and resilience, ability to restore access to personal data, erasure handling in backups, breach notice | | | |
| [ ] | CCPA / CPRA | California residents | Deletion/retention handling, reasonable security | | | |
| [ ] | SOC 2 | Customers demand it | Availability and backup/restore testing evidence | | | |
| [ ] | ISO 27001 | Certification target | Backup policy, tested recovery, access control | | | |
| [ ] | HIPAA | Health data (US) | Data backup plan, disaster recovery plan, emergency mode plan | | | |
| [ ] | PCI DSS | Card data handled | Secure backup storage, no sensitive card data kept improperly | | | |
| [ ] | COPPA / child-data rules | Users under 13/18 | Retention limits, deletion | | | |
| [ ] | Industry rule (finance, education, government): ______ | | | | | |
| [ ] | Regional data-residency rule: ______ | Data must stay in a country/region | Backup locations must also comply | | | |

**12.2 Audit evidence checklist** (keep these for auditors)
- [ ] This signed document with review history
- [ ] Backup job logs (retained ______ months)
- [ ] Restore drill reports (Section 9.2)
- [ ] Access review records (Section 6.3)
- [ ] Encryption configuration proof
- [ ] Immutable-storage configuration proof
- [ ] Vendor backup/DR reports (SOC 2 or equivalent) for third parties in Section 3.4
- [ ] Incident log (Section 17)

**12.3 Data residency**
| Question | ANSWER |
|---|---|
| Must data stay in a specific country/region? | |
| Do any backup copies cross borders? | |
| Legal mechanism for cross-border copies (if any) | |

---

# 13. AI-AGENT WORKFLOW AND GUARDRAILS `[REQUIRED for AI-driven development]`
*AI agents and automations can write code, run commands, and change data. This section sets the safety rules.*

**13.1 Which AI tools/agents touch this project?**

| Agent / tool | What it can do | Environments it can access | Can it delete or overwrite data? | Human approval needed for |
|---|---|---|---|---|
| | | | [ ] Yes [ ] No | |

**13.2 Guardrails: tick every rule you adopt**
- [ ] Agents work only in dev/staging by default; **no write access to production** without named human approval
- [ ] Agents never receive credentials that can delete backups
- [ ] Destructive commands (delete, drop, truncate, force-push, overwrite) require explicit human approval
- [ ] Every agent action on data is logged (who/what/when/why)
- [ ] A fresh backup or snapshot is taken **before** any agent-run migration or bulk data change
- [ ] Agents work on copies of real data (masked/anonymized) where possible
- [ ] Agent-generated code goes through review and tests before reaching production
- [ ] Prompts, agent definitions, and skills are version-controlled (Section 5.6)
- [ ] An "undo plan" is written **before** any agent task that changes data

**13.3 AI-assisted restore: what the AI may and may not do**
| Task | AI may do alone | AI may do with approval | AI must never do |
|---|---|---|---|
| Read backup logs and report status | | | |
| Run restore into a scratch/non-production copy | | | |
| Run restore into production | | | |
| Delete/expire backups | | | |
| Change retention or encryption settings | | | |

**13.4 Approval record format** (use for every production restore or destructive change)
`APPROVED: <name> | DATE/TIME: <> | ACTION: <> | SCOPE: <> | ROLLBACK PLAN: <>`

---

# 14. THE CUSTOMER-GROWTH LADDER: WHAT CHANGES AT 0, 50, 200 AND 500 CUSTOMERS `[RECOMMENDED]`
*Use this to plan ahead. Fill the "Our current setting" column honestly; the other columns are the goals.*

| Topic | 0 customers (pre-launch) | 1-50 customers | 51-200 customers | 201-500 customers | Our current setting |
|---|---|---|---|---|---|
| Database backup | Daily | Daily + point-in-time recovery | Continuous + point-in-time recovery | Continuous + cross-region copy | |
| Customer file backup | Versioning on | Versioning + off-site copy | Versioning + immutable copy | Versioning + immutable + cross-provider | |
| Restore testing | Once before launch | Monthly | Monthly + realistic data size | Monthly + disaster-day every 6 months | |
| Alerts | Email | Email + chat, named on-call | On-call rotation | On-call rotation + escalation policy | |
| Target RPO (Tier 1) | 24 hours | 1 hour | 15 minutes | 5-15 minutes | |
| Target RTO (Tier 1) | 24 hours | 8 hours | 4 hours | 1-4 hours | |
| Status page / customer comms | None | Simple status page | Status page + templates ready | Status page + SLA wording | |
| Compliance evidence | Notes | Basic logs | Organized evidence folder | Audit-ready evidence | |
| Cost review | Not needed | Quarterly | Quarterly | Monthly | |

**14.1 Growth triggers: when do you upgrade early?** (tick the ones you will watch)
- [ ] First paying customer
- [ ] First customer with regulated data
- [ ] First enterprise contract or security questionnaire
- [ ] Data size doubles
- [ ] Any failed drill
- [ ] Any real incident
- [ ] Hitting 50 / 200 / 500 customers
ANSWER (who watches these and how):

---

# 15. COST AND CAPACITY `[RECOMMENDED]`

| Item | Monthly cost now | Expected at 500 customers | Budget owner | Approved? |
|---|---|---|---|---|
| Backup storage | | | | |
| Second-provider/off-site copy | | | | |
| Restore testing environments | | | | |
| Backup tools/licenses | | | | |
| Data transfer/egress when restoring | | | | |
| Monitoring | | | | |
| **Total** | | | | |

- Storage growth forecast (next 12 months): ______
- Cost of **one hour of downtime** to us (estimate): ______
- Is the backup spending proportionate to that cost? [ ] Yes  [ ] No  [ ] Unsure
- Backup storage lifecycle (move old backups to cheaper tiers after ______ days): ______

---

# 16. LAUNCH READINESS CHECKLIST (GO / NO-GO) `[REQUIRED]`
*Every box must be ticked before real customer data is stored. A single unticked box means NO-GO unless the owner signs a written exception.*

**Before first real data**
- [ ] Section 3 data inventory is complete
- [ ] RPO and RTO targets are written and approved (Section 4)
- [ ] Production backups are running **and** verified at least once
- [ ] Backups are encrypted and stored in a separate account/location
- [ ] At least one immutable or offline copy exists
- [ ] Access to backups follows least-privilege and MFA
- [ ] Retention schedule is configured (Section 7)

**Before launch day**
- [ ] A full restore drill passed within the last 30 days (Section 9.2)
- [ ] Runbooks R1-R5 are written and were followed by someone who did not write them
- [ ] Alerts are on and a real alert was received at least once
- [ ] Named on-call person and backup contact exist (Section 11)
- [ ] Credential/domain/DNS recovery is documented and tested (Section 6.5)
- [ ] Customer message templates are written (Section 11.3)
- [ ] AI-agent guardrails are active (Section 13)
- [ ] Compliance evidence folder exists, if applicable (Section 12)

**After launch: schedule these now**
- [ ] First live restore test within 7 days
- [ ] Review of this document within 30 days
- [ ] Re-run readiness at 50, 200, and 500 customers (Section 14)

| Go / No-Go decision | |
|---|---|
| Decision | [ ] GO  [ ] NO-GO |
| Decided by (name) | |
| Date | |
| Exceptions granted (what, why, expiry date) | |

---

# 17. LOGS: KEEP THESE UP TO DATE `[REQUIRED]`

**17.1 Incident log**

| Date | What happened | Data affected | Runbook used | Actual RPO / RTO | Root cause | Lessons and fixes (owner, due) |
|---|---|---|---|---|---|---|
| | | | | | | |

**17.2 Change log for this document**

| Date | Changed by (human or AI agent) | What changed | Why |
|---|---|---|---|
| | | | |

**17.3 Review history**

| Date | Reviewer | Result | Next review due |
|---|---|---|---|
| | | | |

**17.4 When this document MUST be updated** (tick triggers you adopt)
- [ ] New database, storage, or third-party service added
- [ ] Hosting provider or region changed
- [ ] New regulation or customer contract requirement
- [ ] Any incident or failed drill
- [ ] Team member with a named role leaves
- [ ] Every 90 days even if nothing changed

---

# 18. GLOSSARY (PLAIN ENGLISH)

| Word | Meaning |
|---|---|
| Backup | A saved copy of your data you can use to get things back |
| Restore | Using a backup to bring data or systems back |
| RPO | The most data (in time) you can afford to lose |
| RTO | The longest you can afford to be down |
| Full backup | A complete copy of everything |
| Incremental backup | Copies only what changed since the last backup |
| Point-in-time recovery | Rewinding data to an exact moment, such as 10:42 a.m. yesterday |
| Snapshot | A frozen picture of a disk or database at one moment |
| Replication | Live copying to a second place; protects against hardware failure but **also copies mistakes** |
| Immutable | Cannot be changed or deleted for a set time |
| Off-site | Stored somewhere separate from your main system |
| 3-2-1-1-0 | 3 copies, 2 media types, 1 off-site, 1 immutable, 0 restore errors |
| Runbook | Step-by-step instructions anyone can follow |
| Failover | Switching to a standby system when the main one fails |
| Disaster recovery (DR) | The overall plan to recover after a major failure |
| Encryption | Scrambling data so only people with the key can read it |
| MFA | A second proof of identity (like a code on your phone) |
| Least privilege | Giving people only the access they truly need |
| Retention | How long you keep backups |
| Legal hold | A pause on deleting data because of legal reasons |
| On-call | The person who must respond to alerts right now |
| SLA | A written promise to customers about service |
| IaC (Infrastructure as Code) | Setting up servers and services using files instead of clicking by hand |
| CI/CD | Automatic building, testing, and releasing of software |
| Migration | A change to the database structure or data |
| Smoke test | A quick check that the main things still work |
| Egress | Fees or process for moving data out of a service |

---

# 19. COMPLETION SCORE `[REQUIRED]`
*Count your answers. Be honest.*

| Check | Result |
|---|---|
| Number of `[REQUIRED]` sections (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 13, 16, 17, 19) | 16 |
| `[REQUIRED]` sections fully answered | ___ / 16 |
| Remaining `UNKNOWN` items | ___ (each needs an owner + due date) |
| `[IF APPLICABLE]` sections marked N/A with a reason | ___ |
| Latest restore drill passed? | [ ] Yes  [ ] No |
| Second person walked through a runbook successfully? | [ ] Yes  [ ] No |
| Overall status | [ ] Ready  [ ] Not ready |

**Final sign-off**

| Role | Name | Signature/approval | Date |
|---|---|---|---|
| Document owner | | | |
| Reviewer | | | |
| Executive/product owner | | | |

---

# APPENDIX A: FILLED EXAMPLE (FICTIONAL PROJECT: "PETPAL")
*Copy the style, not the answers. This is a made-up project showing what good answers look like.*

**Project:** PetPal, a mobile app where pet owners book dog walkers. **Stage:** 5 (Customers 1-50). **Team:** Solo founder (Maya Torres) plus a part-time contractor (Leo Kim).

| Section | Example answer |
|---|---|
| 1.1 What it does | "PetPal lets pet owners in one city book and pay dog walkers. It stores accounts, bookings, payments references, and walk photos." |
| 1.5 If all data vanished | "We would lose customers and money fast, because bookings and payouts would be unknown." |
| 3.2 Data item #1 | Customer and booking database, managed Postgres (prod), 1.2 GB, +150 MB/month, contains personal data: Yes, Tier 1, owner Maya Torres |
| 3.2 Data item #2 | Walk photos, object storage bucket `petpal-prod-photos`, 40 GB, +6 GB/month, personal data: Yes, Tier 2, owner Maya Torres |
| 3.2 Data item #3 | Search index, rebuilt nightly from the database, Tier 4 (rebuildable), owner Leo Kim |
| 3.4 Third party | Payment provider holds card data; we cannot export cards but we export a monthly transaction report to storage and keep it 7 years |
| 4.2 Targets (Tier 1 DB) | RPO 15 minutes, RTO 4 hours. Proven in last drill: RPO 5 minutes, RTO 2 hours 40 minutes. Target met: Yes |
| 5.3 Schedule (DB) | Continuous log backup plus full snapshot daily at 02:00 UTC, using the managed database backup feature, stored in a separate account at Provider B |
| 5.3 Schedule (photos) | Versioning always on; copy to second provider nightly at 03:00 UTC |
| 6.2 Encryption | In transit: TLS. At rest: provider-managed encryption. Keys: in the cloud key service, key recovery documented in the password manager vault "Ops". Rotation every 12 months |
| 6.5 Recovery access | Password manager emergency kit sealed with Maya's co-founder friend Dana Ruiz; MFA recovery codes in the same sealed kit; registrar recovery email is a shared alias owned by two people |
| 7.1 Retention (DB) | Hourly kept 48 hours, daily 30 days, weekly 12 weeks, monthly 12 months, yearly 7 years. Reason: tax rules for payment records |
| 7.3 Deletion promise | Deleted customers leave backups within 35 days. After every restore, Leo re-applies the deletion log |
| 9.1 Testing | Partial restore monthly; full restore quarterly (next: 2026-12-01) |
| 9.2 Latest drill | 2026-09-14, runbook R3, restore point 2026-09-14 01:55 UTC, took 2h 40m, data lost 5m, Passed. Problem found: step 6 missing the cache flush command. Fixed by Leo on 2026-09-16 |
| 10 Alerts | "Newest DB backup older than 26 hours" alerts Maya by SMS and Leo by email within 1 hour |
| 11.1 Roles | Incident lead: Maya Torres. Restore operator: Leo Kim. Approver: Maya Torres (backup: Dana Ruiz). Comms: Maya Torres |
| 13.2 AI guardrail | "The coding agent has read-only database access in production and cannot delete backups. Migrations run in staging first, with a snapshot taken before each production run." |
| 16 Go/No-Go | GO on 2026-06-30 by Maya Torres. Exception: second-provider copy for photos delayed to 2026-07-15 (signed, expires 2026-07-15) |

---

# APPENDIX B: PRE-WRITTEN RUNBOOK STARTERS FOR COMMON STACKS
*These are starting points. **Edit every placeholder** (`<LIKE_THIS>`), confirm each command against your provider's current documentation, and test in non-production before trusting any step. Delete the stacks you do not use.*

## B1. Relational database (PostgreSQL / MySQL), point-in-time restore
**Use for:** Runbook R3 (full production database restore) or R2 (table restore).
1. Declare an incident. Tell the incident lead. Pause scheduled jobs and writers if safe (maintenance mode on).
2. Safety copy: take a snapshot or dump of the **current** (broken) database named `pre-restore-<YYYYMMDD-HHMM>`.
3. Decide the restore point: the last known good moment (`<YYYY-MM-DD HH:MM UTC>`). Find it from logs, deploy times, or the first bad record.
4. Create a **new, separate** database instance from the backup at that point in time (use your provider's point-in-time restore or restore the base backup and replay logs to the target time). Name it `restore-<YYYYMMDD-HHMM>`.
5. Wait for the instance to be ready. Confirm version and extensions match production.
6. Verify (Section 8.2 checklist): compare row counts of key tables to the expected numbers, spot-check 10 recent records, run the app's smoke tests against the restored instance.
7. If only part of the data is needed (R2): export just those tables/rows from the restored instance and import them into production after checking for conflicts. Otherwise continue to step 8.
8. Switch the app to the restored instance (change connection string/DNS in the approved way) **or** swap names per your provider's procedure. Record the time.
9. Re-apply the deletion log (Section 7.3) and re-run any jobs that missed the gap window.
10. Turn maintenance mode off. Watch errors and latency for 15 minutes.
11. Keep the safety copy for `<N>` days; then delete only with written approval.
12. Log the incident (Section 17.1) and schedule a review in 5 working days.

## B2. Object/file storage (S3-compatible buckets, cloud storage)
**Use for:** Runbook R4.
1. Identify what is missing: list affected paths and the time range.
2. If **versioning** is on: restore previous versions of the affected objects (or remove "delete markers"). Do this for a small sample first.
3. If versioning is off or the data is gone: restore from the second copy/immutable bucket `<BACKUP_BUCKET>` by copying objects back into a **new** prefix `restore-<YYYYMMDD>/`.
4. Verify: object counts, total size, checksums on a sample of `<N>` files, open 5 real files.
5. Point the app at the restored prefix, or copy files back to their original paths after verification.
6. Check that the database references (file paths/URLs) still match the files.
7. Log the incident and fix the cause (accidental deletion, bad script, permissions).

## B3. Backend-as-a-service (Supabase / Firebase and similar managed platforms)
**Use for:** Runbook R3/R4/R8 on managed platforms.
1. Open the provider dashboard with the emergency (break-glass) account; confirm MFA works.
2. Check the backup/PITR page for available restore points. Confirm which plan tier and retention you actually have (Section 6.1).
3. **Do not restore over production first.** Create a new project/branch from the backup if the platform supports it (or restore into a copy).
4. Re-link what the backup may not include: authentication provider settings, storage buckets/files, edge functions, secrets, API keys, webhooks, and scheduled jobs. Use your list from Section 3.1 and Section 5.5.
5. Verify the restored project (counts, sample logins, file access, smoke tests).
6. Update app configuration (project URL, keys stored in your secret manager) and redeploy.
7. Rotate any keys that may have been exposed (Runbook R6 if a breach is suspected).
8. Log the incident.

## B4. Kubernetes / containers / infrastructure as code
**Use for:** Runbook R5 (rebuild everything) or R7 (region failover).
1. Confirm you can reach the **source code repository**, **infrastructure-as-code repo**, and **container registry**. If not, go to Runbook R8 first.
2. Create the new environment from code in the target region/account: network, cluster, storage classes. Use the same code version tag as production: `<GIT_TAG>`.
3. Restore cluster state items you backed up: namespaces, secrets references, config maps, persistent volume snapshots (`<TOOL_NAME>`), and certificates.
4. Restore the **database** (B1) and **file storage** (B2) into the new environment.
5. Deploy the application images by version tag; run database migrations only if the version requires them.
6. Run smoke tests; confirm health checks are green.
7. Move traffic: lower DNS TTL in advance, then change DNS/load balancer to the new environment in small steps (for example 10%, 50%, 100%).
8. Keep the old environment (if it still exists) read-only until you finish the review.
9. Log time taken for the full rebuild: this is your real RTO for R5.

## B5. Lost accounts, credentials, domain, DNS
**Use for:** Runbook R8.
1. Contact the outside trusted person (Solo rules) or the backup contact (Section 11).
2. Open the recovery items in Section 6.5, one at a time: password manager recovery, MFA recovery codes, registrar, DNS provider, cloud root account.
3. For each locked account, start the provider's official recovery process and note the ticket number and expected time.
4. While waiting: publish a status message (Section 11.3), switch to read-only mode if useful, and check whether a second admin exists.
5. After access returns: rotate passwords, API keys, and tokens; re-enroll MFA; review the audit log for unknown activity.
6. Update Section 6.5 with what was learned.

## B6. AI assets (prompts, agents, vector database, models)
**Use for:** Runbook R9.
1. Restore prompts, system instructions, and agent/skill definitions from the Git repository at tag `<GIT_TAG>`.
2. Restore the vector database from its snapshot; if there is none, **rebuild embeddings** from source documents using the stored script and model version `<EMBEDDING_MODEL_VERSION>`.
3. Restore fine-tuned model files/adapters from `<MODEL_STORAGE>`; verify checksums.
4. Run the saved evaluation set (Section 5.6) and compare scores to the last good run. Stop and investigate if quality drops by more than `<THRESHOLD>`.
5. Confirm agent permissions and guardrails (Section 13) are still in place before re-enabling agents.

---

# APPENDIX C: TABLETOP DISASTER EXERCISE (60 MINUTES)
*Use for the "disaster-day simulation" in Section 9.1. No real systems are touched. Everyone reads only this document, as in a real emergency.*

**Setup (5 minutes)**
- Pick a facilitator (not the person who wrote the plan) and a note-taker.
- Invite every named role in Section 11.1. Solo founders: invite your outside trusted person.
- Rules: use only this document; say out loud what you would do; do not run real commands.

**Scenario script. Read one "inject" at a time and pause for answers.**

| Time | Inject (facilitator reads) | Questions to answer |
|---|---|---|
| 0:05 | "At 09:12 on a Tuesday, customers report missing bookings. Monitoring shows nothing unusual." | Who is told first? Which runbook applies? Where is it? |
| 0:15 | "You discover an AI agent ran a bad data cleanup at 08:40. About 10% of customer records are gone." | Which restore point do you pick and why? Who approves? What do you do with the broken state first? |
| 0:25 | "The newest backup is from 02:00. The continuous log backup shows a gap between 07:50 and 08:10." | What data can you recover? What is the real RPO? What do you tell customers? |
| 0:35 | "Your lead engineer's laptop and phone are unavailable. The password manager asks for a recovery code." | Who has access? Where is the recovery info? |
| 0:45 | "A customer asks you to delete their data today and has just emailed their lawyer." | How do you stop their data from being restored? Who handles legal contact? |
| 0:55 | "The restore finished. How do you know it worked?" | Walk through the verification checklist (Section 8.2). |

**Debrief (last 10 minutes), then record in Sections 9.2 and 17**
1. What step was unclear, missing, or wrong in this document?
2. What took longest to find?
3. Which person or access was a single point of failure?
4. List each fix with an **owner** and **due date**.
5. Score: [ ] Passed  [ ] Passed with fixes  [ ] Failed (re-run within ______ days)
