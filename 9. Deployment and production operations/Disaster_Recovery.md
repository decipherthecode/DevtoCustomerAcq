# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**Folder:** Deployment and production operations
**File:** `Disaster_Recovery.md`
**Applies to:** Web apps / SaaS and mobile apps (with optional AI features)
**Life-cycle covered:** Development → Staging → Launch → Customer #1 → Customer #500
**Hosting assumption:** Cloud-agnostic (works with any provider)
**Team assumption:** Solo founder or a team of 1-3 people (one person may hold several roles)

## What is this document?

A **disaster** is anything that suddenly breaks your product or loses your data: a server dies, a database is deleted by mistake, a hacker gets in, a cloud provider goes down, an app store removes your app, an AI provider stops working.

**Disaster Recovery (DR)** is your written plan for "what do we do when that happens?" so you fix things fast, calmly, and without guessing.

This file is a **questionnaire**. Answer the questions and by the end you have a complete DR plan.

## The 7 simple rules

1. **Answer every question** under its `Your answer:` line. Do not delete questions.
2. **Suggested defaults are pre-filled** as `Default:`. Keep it if true for you, or replace it. Never keep a default you cannot actually do.
3. **Use the Example** as a guide, then write your real answer.
4. **Never guess.** If you do not know, write `UNKNOWN - ask <name> by <date>`.
5. **Not relevant?** Write `N/A - <one-line reason>`. Never leave a blank.
6. **Never write secrets here.** No passwords, API keys, tokens, or private keys. Write only *where* they are stored.
7. **Use real names, links and dates.** "Someone" or "soon" is not an answer.

## Status markers (put one on every section title when you work on it)

| Marker | Meaning |
|---|---|
| `[TODO]` | Not started |
| `[WIP]` | Partly answered |
| `[DONE]` | Fully answered and reviewed |
| `[N/A]` | Does not apply (reason given) |
| `[BLOCKED]` | Waiting on someone/something (say who) |

## Which sections to fill and when

| Stage | When | Fill these sections |
|---|---|---|
| **S1. Development** | While building | 0, 1, 2, 3, 4, 5 |
| **S2. Staging / Pre-launch** | Before going live | 6 to 16 |
| **S3. Launch day** | Go-live | 17, 18, 21, 23 (sign-off) |
| **S4. Customers 1-100** | First weeks live | 19, 20, 22 (first drill done) |
| **S5. Customers 101-500** | Growth | 20 (review), update 6, 7, 8 targets, repeat drills |

> **No launch without Sections 0-18 marked `[DONE]` and Section 23 signed.**

## Related documents (cross-links)

Fill these links in Section 0. If a document does not exist yet, write `NOT CREATED YET` and note when it will exist.

| Related document | Why it matters to DR |
|---|---|
| Deployment / Release Process | Rollback steps, release freeze rules |
| Monitoring and Alerting | What alerts tell you a disaster started |
| Incident Response | Day-to-day incident handling (DR is for the big ones) |
| Security Policy / Secrets Management | Key rotation, access rules |
| Infrastructure as Code / Environment Setup | How to rebuild everything |
| Data Retention and Privacy Policy | How long backups are kept, deletion rules |
| Runbooks (Operations) | Detailed fix steps shared with DR |
| Vendor and Third-Party List | Who you depend on |
| SLA / Customer Terms | What you promised customers |

## Instructions for AI agents (read before editing this file)

1. **Read the entire file** before changing anything.
2. **Do not invent facts.** If the answer is not in the repo, config, or given by a human, write `UNKNOWN - needs human input`. Never fabricate contacts, RTO/RPO numbers, vendor names, or dates.
3. **Never write secrets** (keys, passwords, tokens, credentialed connection strings) into this file.
4. **Keep structure intact:** do not rename, remove, or reorder sections or question numbers (e.g., `Q6.2`). Other tools and people rely on them.
5. **Defaults are suggestions, not facts.** Do not mark a `Default:` as true for the project unless you verified it from config or a human confirmed it.
6. **Update status markers honestly.** Mark `[DONE]` only when every question in the section has a real answer.
7. **Add a Change Log row** (Appendix C) for every edit: date, author (human or agent name), what changed.
8. **Flag, don't decide** for anything that costs money, changes customer promises (RTO/RPO/SLA), or touches legal/compliance: mark `[BLOCKED] needs human approval`.
9. **Cite evidence:** for each fact (backup schedule, region, retention), reference the file, config, or dashboard where it can be verified.
10. **Never run destructive recovery steps** (restore over production, delete data, failover) unless a named human with authority approved it during the current incident.
11. **At the end, print a gap report** listing every `UNKNOWN`, `[TODO]`, and `[BLOCKED]` item (Appendix D).

---

# DISASTER RECOVERY PLAN

## 0. Document Control `[TODO]`

| Field | Your answer |
|---|---|
| Product name | |
| Project / repo link | |
| Document owner (one named person) | |
| Backup owner (if owner is unavailable; for a solo founder, a trusted person) | |
| Version | 0.1 |
| Date created | |
| Last reviewed | |
| Next review due (max 90 days away) | |
| Current life-cycle stage (S1-S5) | |
| Approved by (name, role, date) | |

**Cross-links:** paste links to the related documents listed above.

| Related document | Link or `NOT CREATED YET` |
|---|---|
| Deployment / Release Process | |
| Monitoring and Alerting | |
| Incident Response | |
| Security Policy / Secrets Management | |
| Infrastructure as Code / Environment Setup | |
| Data Retention and Privacy Policy | |
| Operations Runbooks | |
| Vendor and Third-Party List | |
| SLA / Customer Terms | |

**Q0.1. Where is the latest copy of this document? Where is the OFFLINE copy** (your systems may be down when you need this)?

Your answer:
> Example: Main copy at `/docs/Disaster_Recovery.md`. PDF printed and saved on the owner's phone and a USB drive.

---

## 1. Plain-Language Summary `[TODO]`

**Q1.1. In 3-5 sentences: what does your product do, and who uses it?**

Your answer:
> Example: "TaskBuddy is a web and mobile app that helps small teams share to-do lists. Customers are small businesses of 2-20 people."

**Q1.2. What is the single most important thing we must never lose, and what happens to customers and the business if the product is down for one full day?**

Your answer:
> Example: "Customer task data. One day down means refunds, angry reviews, and about $X lost."

---

## 2. Project Snapshot (the map of your system) `[TODO]`

**Q2.1. List every part of your system.** Add rows as needed.

| Part | What it does | Where it runs (provider + region) | Who owns it |
|---|---|---|---|
| Web front-end | | | |
| Mobile app (iOS) | | | |
| Mobile app (Android) | | | |
| Backend / API | | | |
| Database(s) | | | |
| File / image storage | | | |
| Login / authentication | | | |
| Payments | | | |
| Email / SMS / push notifications | | | |
| Background jobs / queues | | | |
| Domain / DNS / SSL certificates | | | |
| Monitoring / alerts | | | |
| Source code hosting + CI/CD | | | |
| AI / model provider (if used) | | | |
| Other: | | | |

**Q2.2. Link or paste a simple architecture picture** (boxes and arrows). If none exists, write `UNKNOWN` and create one before Launch.

Your answer:

**Q2.3. Which environments exist, and does each hold real customer data?**

| Environment | Exists? (Y/N) | Where | Real customer data? (Y/N) |
|---|---|---|---|
| Development | | | |
| Staging / test | | | |
| Production | | | |

---

## 3. Stage Checklist: What "Disaster-Ready" Means at Each Stage `[TODO]`

Tick a box only when it is true.

### S1. Development
- [ ] All code is in Git with a remote copy
- [ ] Infrastructure can be rebuilt from code or written steps
- [ ] No secrets stored in code
- [ ] Database changes are tracked (migrations)
- [ ] README explains setup from scratch

### S2. Staging / Pre-launch
- [ ] Backups configured and **one restore tested successfully**
- [ ] RTO/RPO agreed (Section 6)
- [ ] Monitoring and alerts on and reaching a real human
- [ ] Rollback tested on staging
- [ ] Contacts and escalation list complete
- [ ] Secrets and account recovery path documented

### S3. Launch day
- [ ] Production backup confirmed running *today*
- [ ] Someone named as on-call for launch week
- [ ] Status page ready
- [ ] Rollback plan saved offline
- [ ] Customer message templates ready

### S4. Customers 1-100
- [ ] First DR drill completed and recorded
- [ ] Restore re-tested on real-size data
- [ ] Cost of downtime estimated with real numbers
- [ ] Incident review template used at least once (even for a small incident)

### S5. Customers 101-500
- [ ] RTO/RPO re-checked against customer promises
- [ ] Second DR drill (different scenario)
- [ ] Single points of failure reduced
- [ ] Vendor risks reviewed (Section 10)
- [ ] Compliance reviewed (Section 19)
- [ ] Whole document reviewed and re-approved

---

## 4. Assets, Data and Criticality `[TODO]`

**Tiers:** **Tier 1 Critical** (product unusable or data lost without it) · **Tier 2 Important** (workaround exists) · **Tier 3 Can wait** (days).

**Q4.1. Rank every part from Section 2.**

| Part | Tier (1/2/3) | Why | Recovery order (1 = first) |
|---|---|---|---|
| | | | |

> Example: "Database | Tier 1 | holds all customer data | 1"

**Q4.2. What data do you store?**

| Data type | Stored? (Y/N) | Where | Sensitive? (Y/N) |
|---|---|---|---|
| Names and emails | | | |
| Passwords (hashed) | | | |
| Payment details (ideally only at the payment provider) | | | |
| User content / files / photos | | | |
| AI prompts, chat history, embeddings (if any) | | | |
| Logs | | | |
| Other: | | | |

---

## 5. Disaster Scenarios `[TODO]`

**Q5.1. For each scenario: Could it happen to us? Likelihood (L/M/H), Impact (L/M/H), and which runbook (Section 17) handles it?**

| # | Scenario | Likely? | Impact? | Runbook |
|---|---|---|---|---|
| 5.1 | Bad code release breaks the product | | | R1 |
| 5.2 | Database deleted or corrupted by mistake | | | R2 |
| 5.3 | Cloud region or provider outage (including data-center events) | | | R3 |
| 5.4 | Hacker breach, ransomware, or malicious deletion | | | R4 |
| 5.5 | Leaked secret or API key | | | R5 |
| 5.6 | Third-party service down (payments, login, email) | | | R6 |
| 5.7 | Domain, DNS or SSL certificate expired or hijacked | | | R7 |
| 5.8 | Traffic spike or DDoS attack | | | R8 |
| 5.9 | Lost account access (2FA lost, billing suspended, owner unavailable) | | | R9 |
| 5.10 | Mobile app broken or removed from a store | | | R10 |
| 5.11 | Code repository lost or locked | | | R11 |
| 5.12 | Key person unavailable (illness, quits) | | | R12 |
| 5.13 | AI provider outage, model removed/changed, or runaway AI bill | | | R13 |
| 5.14 | Other: | | | |

**Q5.2. Which TOP 3 scenarios worry you most, and why?**

Your answer:

---

## 6. Recovery Targets: RTO and RPO `[TODO]`

- **RTO** (Recovery Time Objective): how long can we be down before it is unacceptable?
- **RPO** (Recovery Point Objective): how much recent data can we afford to lose?

**Q6.1. Targets by stage and tier.** Lower numbers cost more. Only keep numbers you can really achieve.

Default (typical for a solo/small team):

| Stage | Tier 1 RTO | Tier 1 RPO | Tier 2 RTO / RPO | Tier 3 RTO / RPO |
|---|---|---|---|---|
| Launch (0 customers) | 8 hours | 24 hours | 48 hours / 24 hours | 7 days / 7 days |
| Up to 100 customers | 4 hours | 1 hour | 24 hours / 24 hours | 3 days / 7 days |
| Up to 500 customers | 2 hours | 15 minutes | 12 hours / 4 hours | 3 days / 24 hours |

Your answer (copy the table and change the numbers, or write `Default accepted` with the date):

**Q6.2. Can we actually achieve these today?** (Y / N / UNKNOWN. If N, what is missing?)

Your answer:

**Q6.3. Have we promised customers any uptime or recovery numbers (SLA, contract, website)?** If yes, targets above must meet them.

Your answer:
> Example: "No formal SLA. Website says 99.9% uptime goal."

**Q6.4. What does one hour of downtime cost us?** (lost sales, refunds, support time)

Your answer:

---

## 7. Backup Strategy `[TODO]`

**Q7.1. What is backed up?** Defaults are shown in italics.

| Item | Backed up? (Y/N) | How often | Kept how long | Stored where | Different region/provider? (Y/N) | Encrypted? (Y/N) |
|---|---|---|---|---|---|---|
| Production database | | *Default: daily + point-in-time recovery* | *Default: 30 days* | | | |
| User-uploaded files | | *Default: daily* | *Default: 30 days* | | | |
| Source code | | *Default: every push (remote Git)* | *Forever* | | | |
| Infrastructure config | | *Default: in Git* | *Forever* | | | |
| Secrets vault / password manager | | *Default: monthly export, encrypted* | *Default: 12 copies* | | | |
| Mobile signing keys + certificates | | *Default: once, then on every change* | *Forever* | | | |
| AI data (prompts, embeddings, fine-tunes), if any | | *Default: weekly* | *Default: 30 days* | | | |
| This document + runbooks | | *Default: on every change* | *Forever* | | | |

**Q7.2. Follow the 3-2-1 rule?** *3 copies, on 2 kinds of storage, 1 copy somewhere else.*

Your answer:
> Example: "Live DB + automated snapshot in same cloud + weekly export copied to a different provider."

**Q7.3. Can someone who can delete production also delete the backups?** (They should not be able to.)

Your answer:

**Q7.4. How do we know a backup failed, and who is alerted?**

Your answer:

**Q7.5. Restore test log.** A backup that was never restored is only a hope. Default: test monthly.

| Date | What was restored | Time taken | Who | Result |
|---|---|---|---|---|
| | | | | |

---

## 8. Data and Database Recovery `[TODO]`

**Q8.1. Which database(s), and is each managed by a provider or run by us? Is point-in-time recovery on? Is there a replica in another zone/region?**

Your answer:

**Q8.2. Step-by-step: restore the database into a NEW place first (never over live data), verify, then switch.**

Your answer (numbered steps):
1.
2.
3.

**Q8.3. How do we confirm restored data is correct?** (row counts, a test login, newest order exists)

Your answer:

**Q8.4. How do we handle data lost between the last backup and the disaster?** (replay logs, import from payment provider, ask customers to re-enter)

Your answer:

**Q8.5. Are protections against accidental deletion on?** (deletion protection, soft-delete, restricted production access)

Your answer:

---

## 9. Infrastructure, Deployment and Rollback `[TODO]`

**Q9.1. Can we rebuild production from scratch using only written code/steps? How long would it take, and who can do it?**

Your answer (Y / Partly / N + link + time):

**Q9.2. How do we roll back a bad release?**

| Part | Rollback steps | Time | Tested? (date) |
|---|---|---|---|
| Web / API | | | |
| Database migration | | | |
| Mobile app | | | |
| Feature flag (turn a feature off) | | | |

**Q9.3. Are migrations reversible? Do we use safe release methods** (staged rollout, canary, feature flags)? **Do we have a release freeze rule** (e.g., no releases on Fridays)?

Your answer:

**Q9.4. Region and failover setup**

| Question | Your answer |
|---|---|
| Primary region | |
| Standby region (or `none`) | |
| Failover type (none / manual / automatic) | |
| Who can trigger failover | |
| Failover time | |
| How we return to normal (failback) | |

---

## 10. Third-Party and Vendor Dependencies `[TODO]`

**Q10.1. List every outside service we rely on.**

| Vendor | What for | Tier | Status page link | Support contact / plan | Workaround if down | Alternative vendor |
|---|---|---|---|---|---|---|
| Hosting / cloud | | | | | | |
| Database provider | | | | | | |
| Login / authentication | | | | | | |
| Payments | | | | | | |
| Email / SMS / push | | | | | | |
| DNS / domain registrar | | | | | | |
| CDN | | | | | | |
| Apple App Store | | | | | | |
| Google Play | | | | | | |
| Monitoring / error tracking | | | | | | |
| AI / model provider (if used) | | | | | | |
| Other: | | | | | | |

**Q10.2. Which vendor is a single point of failure, and what is our plan?** Are all vendor accounts registered to a team/role email rather than a personal one?

Your answer:

---

## 11. Secrets, Access and Identity Recovery `[TODO]`

**Q11.1. Where are secrets stored?** (Only the *place*, never the values.)

Your answer:
> Example: "Team password manager, vault 'Production'. App secrets in the cloud secret manager."

**Q11.2. Break-glass access (emergency entry if the password manager or login provider is down)**

| Item | Your answer |
|---|---|
| Who holds it | |
| Where it is kept (securely) | |
| Who approves its use | |
| How use is logged and reviewed | |

**Q11.3. How do we rotate (replace) ALL secrets after a leak?** Write the steps and order.

Your answer:

**Q11.4. Is 2FA on for all critical accounts? Where are recovery codes kept? Who is the backup owner for each account?**

| Account | Primary owner | Backup owner | 2FA on? | Recovery method |
|---|---|---|---|---|
| Cloud provider | | | | |
| Domain registrar | | | | |
| Source code host | | | | |
| Apple Developer | | | | |
| Google Play Console | | | | |
| Payment provider | | | | |
| AI provider (if used) | | | | |

**Q11.5. When someone leaves the team, who removes their access, and how quickly?**

Your answer:

---

## 12. Mobile App Recovery `[TODO]`

*(Write `N/A - no mobile app` if it does not apply.)*

**Q12.1. Where are signing keys, certificates and push keys stored and backed up? Who renews them, and when do they expire?** (Lost keys can block all app updates.)

Your answer:

**Q12.2. If a broken version is already in users' hands, what can we do?**

| Option | Available? (Y/N) | How |
|---|---|---|
| Halt staged rollout in the store | | |
| Remote kill switch / feature flags | | |
| Force-update prompt for old versions | | |
| Server-side fix that works with old app | | |

**Q12.3. How fast can we ship an emergency fix, including store review time** (hours to days)?

Your answer:

**Q12.4. Does the app behave gracefully when the server is down** (offline mode, friendly error)? **If a store removes the app, what is our plan** (appeal steps, web fallback)?

Your answer:

---

## 13. AI / LLM Features Recovery `[TODO]`

*(Write `N/A - no AI features` if it does not apply. If AI tools only help you build the product and are not part of the live product, answer Q13.6 only.)*

**Q13.1. Which AI features exist, which provider/model does each use, and what happens to the product if AI stops working?**

| AI feature | Provider and model name | Required for core function? (Y/N) | What users see if it fails |
|---|---|---|---|
| | | | |

**Q13.2. Fallback plan if the AI provider has an outage, rate limits us, or removes/changes the model.**

| Option | Available? (Y/N) | Details |
|---|---|---|
| Second provider or model ready | | |
| Cached or last-known-good answers | | |
| Graceful message and feature turned off | | |
| Queue requests and retry later | | |

**Q13.3. Version control for AI behavior.** Are prompts, system instructions, model versions, settings, and evaluation tests kept in Git? Can we roll back to the previous prompt/model version within the RTO?

Your answer:

**Q13.4. Are vector databases, embeddings, knowledge bases, and fine-tuned models backed up, and can we rebuild them from source data? How long would a rebuild take?**

Your answer:

**Q13.5. Cost and abuse protection.** Do we have spending limits, per-user rate limits, and alerts for sudden AI bill spikes or prompt-abuse attacks? Who can switch AI features off in an emergency?

Your answer:

**Q13.6. AI coding agents (used while building).** Which agents have access to production, databases or secrets? Confirm they have **no ability to delete production data or backups** without a human approval step, and that their actions are logged.

Your answer:

**Q13.7. Privacy.** What user data is sent to the AI provider, and is it covered by the provider's data terms? If the provider has a breach or incident, what do we tell customers?

Your answer:

---

## 14. People, Roles and Contacts `[TODO]`

**Q14.1. Who does what in an incident?** For a solo founder or a team of 1-3, one person can hold many roles. Write it down anyway, and name an outside backup (advisor, contractor, friend with access to the break-glass instructions).

| Role | What they do | Primary person | Backup person |
|---|---|---|---|
| Incident Commander | Leads, decides, stays calm | | |
| Technical Lead | Fixes the problem | | |
| Communications Lead | Updates customers | | |
| Decision maker (money, legal, customer promises) | Approves costly or legal choices | | |
| Security / Privacy contact | Handles breaches | | |

**Q14.2. Contact list** (keep a copy offline).

| Name | Role | Phone | Email | Backup contact method | Availability / time zone |
|---|---|---|---|---|---|
| | | | | | |

**Q14.3. On-call:** Who is on-call, how are they alerted, and who is called next if they do not answer within 15 minutes? Where do we talk if our usual chat tool is down?

Your answer:
> Example: "Alerts go to the founder's phone. If no reply in 15 min, call contractor Ana. Backup chat: phone call."

---

## 15. Detecting and Declaring a Disaster `[TODO]`

**Q15.1. What do we monitor, which tool, who is alerted?** Tick what exists.

| What is monitored | Tool | Alert goes to | Exists? (Y/N) |
|---|---|---|---|
| Website / API up | | | |
| Error rate and slow responses | | | |
| Database health and disk space | | | |
| Backup success | | | |
| Payment failures | | | |
| Security alerts / unusual logins | | | |
| Certificate and domain expiry | | | |
| Cloud and AI bill spikes | | | |

**Q15.2. Severity levels** (defaults; adjust to fit).

| Level | Meaning | Example | Response time |
|---|---|---|---|
| SEV1 | Product down or data at risk for many customers | Database deleted | 15 minutes |
| SEV2 | Major feature broken or many users affected | Login failing for some | 30 minutes |
| SEV3 | Minor issue, workaround exists | One page slow | Same business day |
| SEV4 | No real impact | Typo | Normal backlog |

**Q15.3. Who may declare "DISASTER MODE"? What are the first 5 things anyone does when they spot a problem?**

Your answer:
> Example: 1) Check vendor status pages. 2) Check the last release. 3) Alert on-call. 4) Open an incident log. 5) Do NOT make random changes.

---

## 16. Communication Plan `[TODO]`

**Q16.1. Who must be told, how, and when?**

| Audience | Channel | When | Who sends |
|---|---|---|---|
| Internal team | | | |
| Customers | Status page / email / in-app banner | Default: within 30 min of a SEV1 | |
| Mobile users | In-app message / push | | |
| Partners / vendors | | | |
| Regulators / authorities (if data breach) | | Default: check legal deadline | |

**Q16.2. Where is our public status page?** (It must be hosted separately from the main product.)

Your answer:

**Q16.3. Message templates (edit them now, not during a crisis).**

**A. First notice**
> We are aware of a problem affecting [what]. Our team is investigating. Next update by [time]. We apologize for the trouble.

**B. Progress update**
> Update [time]: The cause is [plain description]. We are [action]. Expected recovery: [estimate, or "next update by X"].

**C. Resolved**
> The issue was resolved at [time]. [What customers should do, if anything.] A summary will follow within [N] days.

**D. Data incident**
> We detected [what happened] on [date]. Affected information may include [data types]. We have [actions taken]. You should [recommended actions]. Contact: [email/phone].

**Q16.4. Who approves messages before sending, and what should support say or not say during an incident?**

Your answer:

---

## 17. Recovery Runbooks (step-by-step) `[TODO]`

Write **exact steps a tired, stressed person can follow.** Each runbook answers: *Who? What exactly? How do we know it worked? What if it fails?*

Use this format for each runbook:

```
RUNBOOK ID / NAME:
TRIGGER (when to use):
WHO CAN RUN IT:
TIME ESTIMATE:
PRE-CHECKS (access, approvals):
STEPS:
  1.
  2.
  3.
HOW TO VERIFY IT WORKED:
IF IT FAILS (next option / who to call):
AFTER (cleanup, communication, notes):
LAST TESTED (date + result):
```

| ID | Scenario | Written? | Link or text |
|---|---|---|---|
| R1 | Bad release (web/API) | | |
| R2 | Database corruption or accidental deletion | | |
| R3 | Region or cloud provider outage | | |
| R4 | Security breach / ransomware (isolate, preserve evidence, rotate secrets, restore clean, notify) | | |
| R5 | Leaked secret or key | | |
| R6 | Third-party service failure | | |
| R7 | Domain, DNS or SSL problem | | |
| R8 | Traffic spike / DDoS | | |
| R9 | Lost account access or suspended billing | | |
| R10 | Mobile app broken or removed from store | | |
| R11 | Code repository lost or locked | | |
| R12 | Key person unavailable | | |
| R13 | AI provider outage / model change / runaway AI cost | | |
| R14 | Other: | | |

**Q17.1. Recovery order and health check.** In what order do we bring things back (copy from Section 4), and what quick checks prove the product is healthy afterwards?

Your answer:
> Example order: 1) Database 2) Backend 3) Login 4) Web 5) Payments 6) Email and push. Health check: log in, create an item, pay, open mobile app, receive an email.

**Q17.2. How do we return to normal (failback), and how do we reconcile data created during the emergency?**

Your answer:

---

## 18. Launch-Day Readiness Check `[TODO]`

Every line needs `YES` plus date and initials.

| Check | YES/NO | Date | Initials |
|---|---|---|---|
| Latest production backup exists and is under 24 hours old | | | |
| A restore from backup was tested successfully | | | |
| Rollback steps ready and tested | | | |
| Alerts are on and reach a human | | | |
| On-call person named and reachable | | | |
| Status page live and tested | | | |
| Customer message templates approved | | | |
| Break-glass access verified | | | |
| Every critical account has a backup owner | | | |
| Contact list tested | | | |
| AI spending limits and kill switch set (if AI used) | | | |
| Offline copy of this document available | | | |

---

## 19. Security, Privacy and Compliance `[TODO]`

**Q19.1. Which rules apply to us?** Tick all that apply or write `UNKNOWN` (ask a qualified legal adviser).

- [ ] GDPR (EU users)
- [ ] CCPA/CPRA (California users)
- [ ] HIPAA (health data)
- [ ] PCI-DSS (card data; usually handled by payment provider)
- [ ] SOC 2 / ISO 27001 (customer requirement)
- [ ] Children's data rules (COPPA etc.)
- [ ] Data-residency rules (data must stay in a country)
- [ ] Other:
- [ ] None

**Q19.2. If customer data is lost or stolen, what are our notification duties and deadlines?**

Your answer:
> Example: "GDPR: notify authority within 72 hours of becoming aware. Legal contact: ___." (Confirm with a legal adviser.)

**Q19.3. Evidence and backups.** How do we preserve logs before cleaning up after a security incident? Are backups encrypted, and do they respect "delete my data" requests? Do we have cyber insurance?

Your answer:

---

## 20. Growth Milestones: Customers 1 to 500 and Costs `[TODO]`

| Milestone | What to review | Done (date) | Notes |
|---|---|---|---|
| Launch (0 customers) | Sections 0-18 done; restore test passed | | |
| Customer #1 | Alerts reach a human; status page live | | |
| 10 customers | Support script ready; incident review practised | | |
| 50 customers | Backups verified at real data size; costs checked | | |
| 100 customers | First full drill; RTO/RPO reviewed; vendor limits checked | | |
| 250 customers | Scale limits tested; standby plan reviewed | | |
| 500 customers | Full document review; second drill; compliance reviewed; consider formal SLA | | |

**Q20.1. At what customer count does our current setup stop being safe, and what is the biggest DR upgrade to make before 500 customers?**

Your answer:
> Example: "A single database instance gets risky above 300 customers. Upgrade: add a standby replica."

**Q20.2. Monthly cost of our DR setup** (backups, standby, monitoring, status page, drills), **and who can approve emergency spending (up to what amount)?**

| Item | Monthly cost |
|---|---|
| Backups and storage | |
| Standby / replica | |
| Monitoring and status page | |
| Other | |
| **Total** | |

Emergency spending approver and limit:

---

## 21. Testing and Drills `[TODO]`

*A plan nobody has practised is a guess.*

**Q21.1. Drill schedule** (defaults for a small team).

| Drill | What we do | Default frequency | First planned date |
|---|---|---|---|
| Backup restore test | Restore latest backup to a test place and verify | Monthly | |
| Tabletop exercise | Talk through one scenario on paper | Quarterly | |
| Rollback drill | Roll back a release on staging | Quarterly | |
| Failover drill (if standby exists) | Switch to the standby | Twice a year | |
| Contact + break-glass test | Call contacts; prove emergency access works | Twice a year | |

**Q21.2. Drill log** (fill after every drill).

| Date | Drill | Result (Pass/Fail) | Time to recover | Problems found | Fix owner + due date |
|---|---|---|---|---|---|
| | | | | | |

---

## 22. After a Disaster: Review and Learning `[TODO]`

**Q22.1. When must a review happen?** Default: within 5 business days for SEV1 and SEV2.

Your answer:

**Q22.2. Blameless incident report** (we fix systems, not blame people). Copy for each serious incident.

```
INCIDENT ID:
START / END / TOTAL DOWNTIME:
SEVERITY:
WHO WAS INVOLVED:
CUSTOMER IMPACT (how many, what):
DATA LOSS (what, how much):
TIMELINE:
ROOT CAUSE (the real reason, not the symptom):
WHAT WENT WELL:
WHAT WENT BADLY:
WHERE WE GOT LUCKY:
RTO TARGET vs ACTUAL:      RPO TARGET vs ACTUAL:
ACTION ITEMS (what / who / due date):
DOCUMENT UPDATES MADE (sections changed):
```

**Q22.3. Incident log**

| ID | Date | Severity | Summary | Downtime | Report link | Actions closed? |
|---|---|---|---|---|---|---|
| | | | | | | |

---

## 23. Sign-Off and Maintenance `[TODO]`

**Q23.1. Review schedule** (defaults)

| When | What |
|---|---|
| Every 90 days | Owner checks contacts, vendors, backups, RTO/RPO |
| After every drill | Update Sections 17 and 21 |
| After every serious incident | Update affected sections within 5 business days |
| After any big change (new vendor, region, database, payment method, AI model) | Update Sections 2, 4, 7-13 |
| Before launch and at 500 customers | Full review and re-approval |

**Q23.2. Final "Is this plan ready?" test.** All must be ticked.

- [ ] A new person could follow any runbook without asking questions
- [ ] No section still says `[TODO]`, `[WIP]` or `UNKNOWN` (or each has an owner and date)
- [ ] No secrets appear anywhere in this file
- [ ] Every contact was verified in the last 90 days
- [ ] At least one restore test and one drill are completed and logged
- [ ] Cross-links in Section 0 are filled
- [ ] An offline copy exists and we know where it is

**Q23.3. Approval**

| Name | Role | Decision (Approved / Changes needed) | Date | Initials |
|---|---|---|---|---|
| | Document owner | | | |
| | Engineering lead | | | |
| | Business / product owner | | | |
| | Security / compliance (if any) | | | |

---

# APPENDIX

## Appendix A. Glossary (plain words)

| Term | Simple meaning |
|---|---|
| Disaster | Anything that suddenly breaks the product or loses data |
| DR | Disaster Recovery: the plan to get back to working |
| BCP | Business Continuity Plan: keeping the business running (people, sales, support) while systems recover |
| RTO | How long we can be down |
| RPO | How much recent data we can lose |
| Backup / Restore | A saved copy of data / putting it back |
| Failover / Failback | Switching to a spare system / switching back |
| Rollback | Going back to the previous working version |
| Replica | A live copy of the database kept in sync |
| Single point of failure | One thing that, if it breaks, breaks everything |
| Runbook | Step-by-step instructions for one problem |
| SLA | A promise to customers about uptime or response |
| Root cause | The real reason it happened |
| Break-glass access | Emergency access used only when normal access is gone |
| Tabletop exercise | Talking through a disaster as practice |
| Staged rollout | Releasing to a small percentage of users first |
| Feature flag | A switch that turns a feature on/off without a new release |
| LLM / model API | The AI service your product calls |
| Embeddings / vector DB | Stored numbers that let AI search your content |
| Blameless review | Learning from failure without blaming people |

## Appendix B. Good vs Bad Answers

| Question | Bad answer | Good answer |
|---|---|---|
| Who restores the database? | "The team" | "Sam Lee (primary), Ana Ruiz (backup). Runbook R2." |
| How often are backups taken? | "Regularly" | "Daily plus point-in-time recovery; 30 days kept; weekly copy in another provider." |
| Where are secrets? | "In the code" | "Team password manager, vault 'Production'; app secrets in the cloud secret manager." |
| When was the restore tested? | "It should work" | "2026-10-02, restored 12 GB in 18 min by Sam, all checks passed." |
| What if the AI provider is down? | "It won't be" | "Fallback to provider B; if both fail, AI features show a friendly message. Runbook R13." |

## Appendix C. Change Log

| Date | Version | Author (human or agent) | What changed | Sections |
|---|---|---|---|---|
| | 0.1 | | Initial draft from template | All |

## Appendix D. Gap Report (fill or auto-generate before sign-off)

| Section / Question | Problem (TODO / UNKNOWN / BLOCKED) | Owner | Due date |
|---|---|---|---|
| | | | |

---
*End of template. No secrets in this file. Keep an offline copy. Review every 90 days.*
