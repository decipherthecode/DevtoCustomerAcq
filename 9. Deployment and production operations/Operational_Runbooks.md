# How to Fill This Document

**Read this first. It takes 3 minutes.**

## What is this document?

An **Operational Runbook** is a "what to do when..." guide. It tells anyone on your team (or any AI agent) exactly how to run, fix, and protect your product after it is built. Think of it like the instruction card in an airplane seat: you hope you never need it, but when you do, you need clear steps right away.

This template covers the full journey: **build, pre-launch, launch day, your first 500 customers, and steady everyday operations.**

## The 5 steps

1. **Copy this file** into your project's `Deployment and production operations/` folder. Keep the name `Operational_Runbooks.md`.
2. **Fill the Quick Start (Section 0) first.** That is the minimum for a safe launch. About 20 minutes.
3. **Go section by section.** Each question has a blank to fill, an example, and an "If unsure" safe default.
4. **Never leave a blank.** Write one of these instead:
   - `N/A: [reason]` (does not apply to us)
   - `TBD: [owner name] by [date]` (we will find out)
5. **Run the Self-Check (Section 26)** before you call the document done.

## Which sections do I fill, and when?

You do **not** have to fill everything on day one. Use this table.

| When | Fill these sections |
|---|---|
| **Before you build much (Phase A)** | 0, 1, 2, 3, 17, 18 |
| **Before launch (Phase B), must be done** | 4 to 15 (all 🟥 items), 19, 21 (🟥 items), plus the Go/No-Go checklist (15) |
| **Before 50 customers** | All 🟨 items, 20, 22 |
| **Before 250 customers** | 23, 24, plus a full review of everything |
| **When something ends** | 25 (retiring a feature, a customer, or the product) |

**Optional sections:** if a section does not apply to you, write `N/A: [reason]` at the top of that section and move on.

**Example blocks:** some sections have a collapsed "Example for your stack" box. Click it open if it helps. Ignore it if you use different tools. Always check your provider's current documentation, because tools change their menus and features.

## How each question looks

> **Q: The question in plain words**
> - **Your answer:** write here
> - **Example:** a sample so you know what "good" looks like
> - **If unsure:** a safe default you can copy

Delete the "Example" and "If unsure" lines when you are finished if you want a cleaner document. Keep them if the next person may need them.

## Symbols used

| Symbol | Meaning |
|---|---|
| 🟥 | **Required.** Do not launch without it. |
| 🟨 | **Recommended.** Fill before 50 customers. |
| ⬜ | **Optional.** Fill when you grow or if it applies. |
| 👤 | A **human** must do or approve this. |
| 🤖 | An **AI agent** may do this (within the rules in Section 13). |
| ✅ | A checkbox. Change `[ ]` to `[x]` when done. |

## Golden rules for writing

- **Write short sentences.** One action per step. Start steps with a verb ("Click", "Run", "Check").
- **Use real names, not "the team".** Write who, by name or role.
- **Use real links and exact commands.** Not "go to the dashboard"; write the actual URL or command.
- **Never paste passwords, API keys, or tokens in this file.** Write *where they are stored* instead (for example, "in the password manager, vault: Production").
- **Write the "expected result" for every step**, so the reader knows it worked.
- **Date everything.** Use `YYYY-MM-DD` (for example, 2026-10-18).
- **If a step is dangerous, mark it ⚠️ and say who must approve it.**

## Tiny glossary (more in Appendix B)

| Word | Meaning |
|---|---|
| **Production ("prod")** | The real product that real customers use |
| **Staging** | A practice copy of production for testing |
| **Deploy** | Putting new code live |
| **Rollback** | Going back to the last version that worked |
| **Incident** | Something is broken or at risk and customers may be affected |
| **On-call** | The person responsible for responding right now |
| **Runbook** | Step-by-step instructions (this document) |
| **AI agent** | An AI tool that can take actions, not just chat |

---

# Operational Runbook: [PROJECT NAME]

## Document Control 🟥

| Field | Your answer |
|---|---|
| Project name | `[ ]` |
| Runbook version | `1.0` |
| Template version this was copied from | `2.0` *(see Section 24 for how to upgrade)* |
| Last updated (YYYY-MM-DD) | `[ ]` |
| Document owner (one named person) | `[ ]` |
| Reviewer / approver | `[ ]` |
| Current lifecycle phase (pick one) | ☐ A. Build ☐ B. Pre-launch ☐ C. Launch day ☐ D. Growth (up to 500) ☐ E. Steady state |
| Current customer count | `[ ]` |
| Next scheduled review date | `[ ]` *(If unsure: 30 days from today, then monthly until 500 customers.)* |

**Change log** (add a row every time you edit):

| Date | Who | What changed | Why |
|---|---|---|---|
| `[ ]` | `[ ]` | Created first version | New project |

---

## Table of Contents

0. [Quick Start (Minimum Safe Launch)](#0-quick-start-minimum-safe-launch)
1. [Project Snapshot](#1-project-snapshot)
2. [People, Roles & Contacts](#2-people-roles--contacts)
3. [Systems Map & Environments](#3-systems-map--environments)
4. [Lifecycle Phases & Gates (Build to 500 Customers)](#4-lifecycle-phases--gates-build-to-500-customers)
5. [Access, Secrets & Security](#5-access-secrets--security)
6. [Deploy / Release Runbook](#6-deploy--release-runbook)
7. [Rollback Runbook](#7-rollback-runbook)
8. [Monitoring, Alerts & Health Checks](#8-monitoring-alerts--health-checks)
9. [Incident Response](#9-incident-response)
10. [Backup, Restore & Disaster Recovery](#10-backup-restore--disaster-recovery)
11. [Customer Support & Communication](#11-customer-support--communication)
12. [Cost, Scaling & Capacity](#12-cost-scaling--capacity)
13. [AI-Agent Operations & Guardrails](#13-ai-agent-operations--guardrails)
14. [Routine Maintenance Calendar](#14-routine-maintenance-calendar)
15. [Go / No-Go Launch Checklist](#15-go--no-go-launch-checklist)
16. [First 500 Customers: Milestone Reviews](#16-first-500-customers-milestone-reviews)
17. [Change Management & Approvals](#17-change-management--approvals)
18. [Environment & Infrastructure Setup](#18-environment--infrastructure-setup)
19. [Testing & QA in Production](#19-testing--qa-in-production)
20. [Vendor & Third-Party Management](#20-vendor--third-party-management)
21. [Compliance, Privacy & Data Requests](#21-compliance-privacy--data-requests)
22. [Product Analytics, Metrics & Customer Health](#22-product-analytics-metrics--customer-health)
23. [Handover & Onboarding](#23-handover--onboarding)
24. [Documentation & Knowledge Base Upkeep](#24-documentation--knowledge-base-upkeep)
25. [Decommissioning & Shutdown](#25-decommissioning--shutdown)
26. [Self-Check: Is This Runbook Ready?](#26-self-check-is-this-runbook-ready)
- [Appendix A: One-Procedure Runbook Card](#appendix-a-one-procedure-runbook-card-copy-for-each-new-procedure)
- [Appendix B: Glossary](#appendix-b-glossary)
- [Appendix C: Post-Incident Review Template](#appendix-c-post-incident-review-template)
- [Appendix D: Recommended Reading](#appendix-d-recommended-reading)
- [Appendix E: Ready-Made Quick-Fix Cards](#appendix-e-ready-made-quick-fix-cards)

---

## 0. Quick Start (Minimum Safe Launch)

**Fill only these 10 answers first.** If you can answer all 10, you can launch safely. Fill the rest of the document afterwards, before you reach 50 customers.

| # | Question | Your answer |
|---|---|---|
| 1 🟥 | What does the product do, in one sentence? | `[ ]` |
| 2 🟥 | Where does it run (platform name and URL of dashboard)? | `[ ]` |
| 3 🟥 | Who is the **first person to call** when it breaks? (name, phone, chat handle) | `[ ]` |
| 4 🟥 | Who is the **backup person** if #3 does not answer in 15 minutes? | `[ ]` |
| 5 🟥 | How do I **deploy** a new version? (one-line summary, details in Section 6) | `[ ]` |
| 6 🟥 | How do I **go back** to the last working version? (one-line summary, details in Section 7) | `[ ]` |
| 7 🟥 | How will I **know** if the product is down? (tool name, who gets the alert) | `[ ]` |
| 8 🟥 | Where are **backups**, and did I test restoring one? | `[ ]` |
| 9 🟥 | Where are **passwords and keys** stored? (name of the vault, NOT the secrets) | `[ ]` |
| 10 🟥 | How do customers **reach us** for help, and who answers? | `[ ]` |

---

## 1. Project Snapshot

> **Purpose of this section:** so a stranger understands your product in 2 minutes.

**Q1.1 🟥 What does the product do, and for whom?**
- **Your answer:** `[ ]`
- **Example:** "BookBuddy is a web app that helps small bakeries take online orders."
- **If unsure:** Finish this sentence: "[Product] helps [type of customer] to [do what]."

**Q1.2 🟥 What are the 3 most important things the product must NEVER stop doing?** (These are your "critical functions". Protect them first.)
- **Your answer:** 1. `[ ]` 2. `[ ]` 3. `[ ]`
- **Example:** 1. Customers can log in. 2. Customers can pay. 3. Orders are saved.
- **If unsure:** Ask: "If this stopped for one hour, which part would make customers angry or lose money?"

**Q1.3 🟥 What type of product is it?**
- **Your answer:** ☐ Website ☐ Mobile app ☐ API/backend only ☐ Desktop app ☐ AI-powered product ☐ Other: `[ ]`

**Q1.4 🟨 Does the product handle sensitive data?** (tick all that apply)
- ☐ Customer names/emails ☐ Payments/cards ☐ Health data ☐ Children's data ☐ Location ☐ Uploaded files ☐ None
- **If unsure:** Assume yes for names/emails and treat them as sensitive.

**Q1.5 🟨 Which rules or laws apply?** (privacy, payments, industry)
- **Your answer:** `[ ]`
- **Example:** "GDPR (EU customers), PCI via payment provider, no health data."
- **If unsure:** Write `TBD: [owner] by [date]` and check with a lawyer or the payment provider's guidance before launch.

**Q1.6 🟥 What is the promise to customers about uptime and speed?** (your "service level goal")
- **Your answer:** Available `[ ]`% of the time. Main pages load in under `[ ]` seconds.
- **Example:** 99.5% available per month (about 3.6 hours of downtime allowed). Pages load in under 3 seconds.
- **If unsure:** Use 99.5% and 3 seconds until you have real data.

**Q1.7 🟥 What are your links?**

| Item | Link |
|---|---|
| Live product (production) | `[ ]` |
| Practice copy (staging) | `[ ]` |
| Code repository | `[ ]` |
| Hosting dashboard | `[ ]` |
| Monitoring dashboard | `[ ]` |
| Status page | `[ ]` |
| Support inbox / helpdesk | `[ ]` |
| Team chat channel for incidents | `[ ]` |
| Project plan / task board | `[ ]` |

---

## 2. People, Roles & Contacts

> **Purpose:** nobody should ever wonder "whose job is this?"

**Q2.1 🟥 Who holds each role?** (One person can hold several roles in a tiny team, but write it down.)

| Role | What they do | Name | Contact (phone / chat) | Backup person |
|---|---|---|---|---|
| **Owner / Decision maker** | Final say on risky choices (launch, shutdown, spending) | `[ ]` | `[ ]` | `[ ]` |
| **On-call responder** | First to act when an alert fires | `[ ]` | `[ ]` | `[ ]` |
| **Release manager** | Approves and runs deployments | `[ ]` | `[ ]` | `[ ]` |
| **Incident commander** | Leads during an incident (can be the on-call person) | `[ ]` | `[ ]` | `[ ]` |
| **Communications lead** | Tells customers what is happening | `[ ]` | `[ ]` | `[ ]` |
| **Support lead** | Answers customer questions | `[ ]` | `[ ]` | `[ ]` |
| **Security contact** | Handles leaks, suspicious access | `[ ]` | `[ ]` | `[ ]` |
| **AI-agent supervisor** 👤 | Responsible for what AI agents do (see Section 13) | `[ ]` | `[ ]` | `[ ]` |

- **If unsure:** In a one-person team, you are every role. Write your name in each row, and name a trusted friend or advisor as the backup.

**Q2.2 🟥 How do we reach people, and in what order?** (escalation ladder)

| Step | Who | How | Wait before moving on |
|---|---|---|---|
| 1 | On-call responder | `[ ]` | 10 minutes |
| 2 | Backup responder | `[ ]` | 10 minutes |
| 3 | Owner | `[ ]` | 15 minutes |
| 4 | External help (hosting support, contractor) | `[ ]` | n/a |

**Q2.3 🟨 What are the working hours and the "after hours" promise?**
- **Your answer:** `[ ]`
- **Example:** "Support Mon-Fri 9am-6pm local time. Critical outages (customers cannot log in or pay) are handled 24/7 by on-call."
- **If unsure:** Say honestly what you can cover. Under-promise.

**Q2.4 🟨 Who can approve spending money in an emergency?** (extra servers, paid support)
- **Your answer:** `[ ]` up to `[ ]` per incident.

---

## 3. Systems Map & Environments

> **Purpose:** a simple picture of "what parts exist and how they connect."

**Q3.1 🟥 List every part of the system.**

| Part | What it does | Provider / tool | Who owns it | Critical? (Y/N) |
|---|---|---|---|---|
| Frontend (what customers see) | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Backend / API | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Database | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| File storage | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Login / accounts | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Payments | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Email / notifications | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| AI model / AI provider | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Domain & DNS | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Monitoring & alerts | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Other third-party services | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

- **If unsure:** Open your hosting dashboard and your code's settings file; list every service name you see.

**Q3.2 🟥 Draw or describe how the parts connect.**
- **Your answer:** (paste a simple diagram, an image link, or write arrows)
- **Example:** `Customer → Website → API → Database` and `API → Payment provider` and `API → AI provider`.
- **If unsure:** Write one line per arrow, "A talks to B".

**Q3.3 🟥 What environments exist?**

| Environment | Purpose | URL | Who can change it | Uses real customer data? |
|---|---|---|---|---|
| Local / development | Building and trying things | n/a | Developers | No |
| Staging / test | Final check before going live | `[ ]` | `[ ]` | **Never** |
| Production | Real customers | `[ ]` | `[ ]` (approval needed) | Yes |

**Q3.4 🟨 What does the product depend on that we do not control?** (and what happens if it fails)

| Dependency | If it fails, what breaks? | Our workaround |
|---|---|---|
| `[ ]` | `[ ]` | `[ ]` |

- **Example:** "Payment provider down → customers cannot pay → show message 'Payments are temporarily unavailable, try again in 30 min' and queue orders."

---

## 4. Lifecycle Phases & Gates (Build to 500 Customers)

> **Purpose:** know which phase you are in, what "done" means, and when you may move to the next one. A **gate** is a checkpoint you must pass before moving on.

### The journey at a glance

| Phase | Customers | Main goal | Gate to leave this phase |
|---|---|---|---|
| **A. Build** | 0 | Make it work, with AI agents and humans building safely | Features done, tests pass, staging works |
| **B. Pre-launch** | 0 | Make it safe and ready | Section 15 Go/No-Go checklist passed |
| **C. Launch day** | 1 to 50 | Watch closely, fix fast, learn | 7 days with no major incident, support under control |
| **D. Early growth** | 50 to 500 | Stay stable while usage grows | Milestone reviews (Section 16) done at 100, 250, 500 |
| **E. Steady state** | 500+ | Run smoothly, improve calmly | Ongoing routine (Section 14) |

**Q4.1 🟥 Which phase are we in today, and what is the next gate?**
- **Your answer:** `[ ]`

### Phase A: Build (AI-driven development)

**Q4.2 🟥 How do we keep AI-written code safe before it reaches customers?** (tick what you do)
- ☐ A human reviews every change before it goes live 👤
- ☐ Automatic tests run on every change
- ☐ Automatic security/secret scan on every change
- ☐ Changes go to staging first, never straight to production
- ☐ Every change is saved in version control with a clear message
- **If unsure:** Tick all five. Do not skip the human review for anything that touches login, payments, or customer data.

**Q4.3 🟨 What is our "Definition of Done" for a feature?**
- **Your answer:** `[ ]`
- **Example:** "Works on staging, tests pass, reviewed by a human, documented, rollback possible, monitoring added."

### Phase B: Pre-launch

**Q4.4 🟥 What must be true before the first customer arrives?**
- **Answer:** Complete the **Go / No-Go Checklist in Section 15.** Record the date and decision there.

### Phase C: Launch day and first 50 customers

**Q4.5 🟥 Launch plan.**

| Question | Your answer |
|---|---|
| Launch date and time (with time zone) | `[ ]` *(If unsure: pick a weekday morning, never a Friday or before a holiday.)* |
| Who is watching during the first 4 hours? | `[ ]` |
| Is it a soft launch (invite-only) or open to everyone? | `[ ]` *(If unsure: soft launch to 10-50 people first.)* |
| Maximum number of customers allowed in week 1 | `[ ]` *(If unsure: 50.)* |
| How do we pause sign-ups if things go wrong? | `[ ]` |
| Where do we record issues in the first week? | `[ ]` |

**Daily check during first 7 days** (copy and tick each day):

- ☐ Product is up and the critical functions (Q1.2) work
- ☐ Errors in last 24 hours reviewed
- ☐ Support messages answered within target time
- ☐ Costs checked against budget
- ☐ Any new customer feedback recorded

### Phase D: Early growth (50 to 500)

**Q4.6 🟨 What are our scaling "tripwires"?** (a tripwire is a number that tells you to act BEFORE something breaks)

| Tripwire | Our number | Action when reached |
|---|---|---|
| Customers reach | `[ ]` | Run milestone review (Section 16) |
| Server/database usage above | `[ ]`% | Increase capacity (Section 12) |
| Support messages per day above | `[ ]` | Add helper or auto-replies (Section 11) |
| Monthly cost above | `[ ]` | Review spending (Section 12) |
| Error rate above | `[ ]`% | Pause new releases, investigate |

- **If unsure:** Use 70% for usage, and 80% of your monthly budget for cost.

### Phase E: Steady state

**Q4.7 🟨 After 500 customers, what changes?**
- **Your answer:** `[ ]`
- **Example:** "Move from daily checks to weekly. Add a second on-call person. Review this runbook quarterly."

---

## 5. Access, Secrets & Security

> **Purpose:** the right people can get in; nobody else can. **Never write real passwords or keys here.**

**Q5.1 🟥 Where are secrets stored?** (passwords, API keys, tokens, certificates)
- **Your answer:** Tool name: `[ ]` Vault/folder: `[ ]` Who can open it: `[ ]`
- **If unsure:** Use a reputable password manager or your platform's built-in secrets feature. Never store secrets in code, chat, email, or this file.

**Q5.2 🟥 Who has access to production, and at what level?**

| Person / agent | System | Access level (read / change / admin) | Date granted | Reviewed on |
|---|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

- **If unsure:** Give the **least** access that lets the person do their job. Use two-step login (2FA) on every account that supports it.

**Q5.3 🟥 What happens when someone leaves the team or a contractor finishes?** (offboarding)
- ☐ Remove their access the same day ☐ Change any shared passwords ☐ Collect devices/files ☐ Update Section 2
- **Owner of this task:** `[ ]`

**Q5.4 🟥 How often do we change (rotate) secrets, and how do we do it?**
- **Your answer:** Every `[ ]` months, and immediately if a leak is suspected. Steps: `[ ]`
- **If unsure:** Every 90 days; immediately after any suspected leak.

**Q5.5 🟥 What do we do if a secret or customer data leaks?**
1. Stop the leak (disable the key, close the access). 👤
2. Change the exposed secrets.
3. Tell the Security contact and Owner right away.
4. Write down what happened and when.
5. Follow legal rules for telling customers or authorities: `[ ]` *(If unsure: contact a lawyer; many laws require notice within 72 hours.)*

**Q5.6 🟨 What routine security checks do we run?**
- ☐ Software updates/patches monthly ☐ Dependency vulnerability scan on every release ☐ Review of who has access monthly ☐ Check for exposed secrets in code on every change

---

## 6. Deploy / Release Runbook

> **Purpose:** a repeatable, boring, safe way to put new code live.

**Q6.1 🟥 Release rules.**

| Question | Your answer |
|---|---|
| When are we allowed to deploy? | `[ ]` *(If unsure: weekdays, daytime, never Friday afternoon.)* |
| When are we NOT allowed to deploy? (freeze periods) | `[ ]` |
| Who must approve a production deploy? | `[ ]` 👤 |
| Can an AI agent deploy to production? | ☐ No ☐ Yes, only with approval from `[ ]` *(If unsure: No, unless a human approves each time.)* |

**Q6.2 🟥 Pre-deploy checklist.**
- ☐ Change reviewed by a human 👤
- ☐ All automatic tests pass
- ☐ Tested on staging, and it works
- ☐ Database changes (if any) are safe to undo, or a backup was taken first
- ☐ Rollback plan is ready (Section 7)
- ☐ Team knows a deploy is happening
- ☐ Nobody is out of reach for the next 1 hour

**Q6.3 🟥 Step-by-step deploy.** (write the real steps with exact commands/buttons)

| Step | Action | Expected result | If it does not match |
|---|---|---|---|
| 1 | `[ ]` | `[ ]` | Stop. Go to Section 7. |
| 2 | `[ ]` | `[ ]` | `[ ]` |
| 3 | `[ ]` | `[ ]` | `[ ]` |
| 4 | `[ ]` | `[ ]` | `[ ]` |

- **Example step:** "Click 'Deploy to production' in [platform]. Expected: status turns green in under 5 minutes."

<details>
<summary><strong>Example for your stack (click to open, optional)</strong></summary>

| If you use... | A safe way to deploy |
|---|---|
| **GitHub + GitHub Actions** | Merge to the main branch. The pipeline runs tests, deploys to staging, then **waits for a named reviewer to approve** (use an "environment" with required reviewers) before deploying to production. |
| **Vercel / Netlify / Render (managed platforms)** | Every change gets a preview link. Test the preview, then merge or promote it to production. Keep "auto-deploy to production" off if more than one person commits. |
| **AWS / Google Cloud / Azure** | Build a container or package once, deploy the **same build** to staging and then production. Use the platform's rolling or blue-green deploy option so old and new run side by side briefly. |
| **Mobile apps** | Release through the store's staged rollout (for example 5%, then 20%, then 100%). You cannot instantly undo an app already installed, so keep a server-side feature switch. |

Always check your provider's current documentation, because menus and features change.
</details>

**Q6.4 🟥 After-deploy check (do within 15 minutes).**
- ☐ Open the live product; the home page loads
- ☐ Test each critical function from Q1.2
- ☐ Look at the error dashboard; no new spike
- ☐ Check response speed looks normal
- ☐ Post "Deploy done" in `[team channel]`

**Q6.5 🟨 How do we handle database changes?**
- **Your answer:** `[ ]`
- **If unsure:** Always back up first, make changes in small steps, test on staging with a copy of realistic fake data.

**Q6.6 🟨 How do we release risky features safely?**
- ☐ Feature switch (turn on for few users first) ☐ Release to 10% then 50% then 100% ☐ Not used yet
- **If unsure:** For anything touching payments or login, release to a small group first.

**Q6.7 🟨 How do we record each release?**
- **Where is the release log?** `[ ]` Record: date, version, who deployed, what changed, result.

---

## 7. Rollback Runbook

> **Purpose:** the "undo button" plan. Decide BEFORE you need it.

**Q7.1 🟥 When do we roll back?** (tick the triggers)
- ☐ A critical function from Q1.2 is broken after a deploy
- ☐ Error rate is above `[ ]`% for more than `[ ]` minutes
- ☐ Customers report the same problem repeatedly
- ☐ Data looks wrong or is being lost
- **Rule of thumb:** If unsure, **roll back first, investigate later.**

**Q7.2 🟥 Who may decide to roll back?**
- **Your answer:** Anyone on-call may roll back without asking. 👤 / `[ ]`
- **If unsure:** Allow the on-call person to roll back immediately and tell the Owner afterwards.

**Q7.3 🟥 Step-by-step rollback.**

| Step | Action | Expected result |
|---|---|---|
| 1 | Announce in `[channel]`: "Rolling back [version]." | Message posted |
| 2 | `[ ]` (command or button to return to the previous version) | Previous version live |
| 3 | `[ ]` (undo database change, if any) | Data matches previous version |
| 4 | Run the after-deploy check (Q6.4) | All critical functions work |
| 5 | Announce "Rollback complete." and create an issue to investigate | Issue link recorded |

<details>
<summary><strong>Example for your stack (click to open, optional)</strong></summary>

| If you use... | A typical rollback |
|---|---|
| **Managed platforms (Vercel, Netlify, Render, Heroku-style)** | Open the list of past deployments and promote or redeploy the last good one. Usually under 2 minutes. |
| **Containers / Kubernetes** | Redeploy the previous image tag, or use the platform's "rollout undo" feature. |
| **Git-based pipelines** | Revert the bad change in version control and let the pipeline redeploy (slower, but leaves a clear record). |
| **Database changes** | Prefer "forward-fix" migrations that are safe to leave in place. Only restore from backup (Section 10) if data is wrong. |
</details>

**Q7.4 🟥 What can NOT be rolled back?** (for example: deleted data, emails already sent, payments already taken)
- **Your answer:** `[ ]`
- **What do we do instead?** `[ ]`

**Q7.5 🟨 How long should a rollback take?**
- **Target:** `[ ]` minutes. *(If unsure: under 15 minutes.)* Practice it on staging once before launch. ☐ Practiced on `[date]`.

---

## 8. Monitoring, Alerts & Health Checks

> **Purpose:** find problems before customers tell you.

**Q8.1 🟥 What do we watch?** (the "four golden signals" in plain words)

| What | Plain meaning | Tool | Normal value | Alert when |
|---|---|---|---|---|
| **Uptime** | Is it reachable? | `[ ]` | Up | Down for more than 2 minutes |
| **Errors** | How often does something fail? | `[ ]` | `[ ]`% | Above `[ ]`% |
| **Speed** | How fast does it respond? | `[ ]` | `[ ]` sec | Above `[ ]` sec |
| **Usage / load** | How busy is it? | `[ ]` | `[ ]` | Above `[ ]`% of capacity |
| **Money-path health** | Do sign-up, login, and payment work? | `[ ]` | Working | Any failure |
| **AI quality & cost** | Is the AI answering well and within budget? | `[ ]` | `[ ]` | `[ ]` |

- **If unsure:** At minimum set up a free uptime check on your home page and your login page, plus email/phone alerts.

<details>
<summary><strong>Example for your stack (click to open, optional)</strong></summary>

| Need | Tool types (pick one per row) |
|---|---|
| Uptime checks from outside | Hosted uptime monitors (many have free tiers) |
| Error tracking | Error-tracking services such as Sentry-style tools |
| Logs and metrics | Your cloud provider's built-in monitoring, or a hosted logging/metrics service, or Grafana-style dashboards |
| Phone / SMS paging | On-call paging tools, or at minimum SMS/phone alerts from your monitor |
| Status page | Hosted status page tools (many have free tiers) |
| AI usage and cost | Your AI provider's usage dashboard plus a spending cap |

Tip: set up alerts for **symptoms customers feel** (site down, login failing) before alerts for causes (high CPU).
</details>

**Q8.2 🟥 Who gets which alert, and how?**

| Alert type | Who | How (phone, SMS, chat, email) | Hours |
|---|---|---|---|
| Critical (customers affected now) | `[ ]` | `[ ]` | 24/7 |
| Warning (might become critical) | `[ ]` | `[ ]` | Working hours |
| Info (good to know) | `[ ]` | Dashboard or weekly email | n/a |

**Q8.3 🟥 Daily 5-minute health check.** (do it every morning during phases C and D)
- ☐ Status page and uptime checks are green
- ☐ Error dashboard has no unusual spike
- ☐ Backups ran successfully last night
- ☐ Disk, memory, database usage below 70%
- ☐ Costs are on track
- ☐ Support inbox has no unanswered urgent messages

**Q8.4 🟨 Avoid alert fatigue.**
- **Rule:** Every alert must have a clear action. If you keep ignoring an alert, fix it or delete it. Review alerts monthly. Owner: `[ ]`

**Q8.5 🟨 Where are logs kept, and for how long?**
- **Your answer:** Tool: `[ ]` Kept for `[ ]` days. *(If unsure: 30 days.)* **Never log passwords, full card numbers, or private customer details.**

---

## 9. Incident Response

> **Purpose:** stay calm, follow steps, fix fast, learn.

**Q9.1 🟥 How serious is it? (Severity levels.)** Adjust the numbers to fit your product.

| Level | Meaning | Example | Response target | Customer update |
|---|---|---|---|---|
| **SEV-1 Critical** | Product down, or data lost/leaked, or payments broken for many | Nobody can log in | Start in 15 min, 24/7 | Every 30 min |
| **SEV-2 Major** | Important feature broken, workaround exists | Search is broken | Start in 1 hour, 24/7 or next morning `[ ]` | Every 2 hours |
| **SEV-3 Minor** | Small problem, few customers | A button looks wrong | Next working day | When fixed |
| **SEV-4 Cosmetic** | Annoying but harmless | Typo | Weekly planning | Not needed |

- **If unsure about severity, choose the higher one.** You can lower it later.

**Q9.2 🟥 The incident steps** (follow in order)

1. **Notice.** An alert fires or a customer reports a problem.
2. **Claim it.** The on-call person writes in `[incident channel]`: "I'm on it. Severity: [level]." 👤
3. **Stop the bleeding.** Fastest safe fix first: roll back (Section 7), turn off the broken feature, pause sign-ups, or switch to a backup. *Do not hunt for the root cause yet.*
4. **Tell people.** Internal team now; customers using Section 11 messages.
5. **Escalate** using the ladder in Q2.2 if you are stuck for 15 minutes.
6. **Fix and verify.** Run the after-deploy check (Q6.4).
7. **Declare resolved.** Post "Resolved" internally and publicly.
8. **Learn.** Complete a Post-Incident Review within 5 working days (Appendix C) for every SEV-1 and SEV-2.

**Q9.3 🟥 Quick-fix cards for our most likely problems.** (write at least 3; start from the ready-made cards in Appendix E, and use Appendix A for the full format)

| Problem | First thing to check | Quick fix | Link to detailed card |
|---|---|---|---|
| Site is down | `[ ]` | `[ ]` | `[ ]` |
| Login is failing | `[ ]` | `[ ]` | `[ ]` |
| Payments are failing | `[ ]` | `[ ]` | `[ ]` |
| Database full or slow | `[ ]` | `[ ]` | `[ ]` |
| Third-party service down | `[ ]` | `[ ]` | `[ ]` |
| AI provider down or giving bad answers | `[ ]` | `[ ]` | `[ ]` |
| Suspected security breach | See Q5.5 | | |

**Q9.4 🟥 Where do we write the incident notes while it is happening?**
- **Your answer:** `[ ]` *(If unsure: one chat thread per incident, with times for every action.)*

**Q9.5 🟨 Do we run practice drills?**
- **Your answer:** Every `[ ]` months, we pretend something breaks and follow this runbook. Last drill: `[date]`. *(If unsure: once before launch, then every 6 months.)*

---

## 10. Backup, Restore & Disaster Recovery

> **Purpose:** if the worst happens, you can get customers' data back.
> **A backup you have never restored is only a hope.**

**Q10.1 🟥 What data must be backed up?**

| Data | Where it lives | Backup method | How often | Kept for | Stored where (different place than the original) |
|---|---|---|---|---|---|
| Main database | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Uploaded files | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Settings / configuration | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Code | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

- **If unsure:** Back up the database daily, keep 30 days, and store copies in a separate account or region. Follow the "3-2-1 rule": 3 copies, 2 different types of storage, 1 off-site.

<details>
<summary><strong>Example for your stack (click to open, optional)</strong></summary>

| If you use... | Backup ideas |
|---|---|
| **Managed database (Supabase, cloud-managed Postgres/MySQL)** | Turn on automatic backups, check how many days are kept on your plan, and whether point-in-time recovery is available or needs an add-on. Also take your own scheduled export to a **separate** account. |
| **Cloud file storage** | Turn on versioning and copy important buckets to a second location or account. |
| **Self-managed servers** | Scheduled database dumps plus server snapshots, stored off the server. |
| **Code and config** | Your code host is not your only copy; mirror or export it regularly. |

Remember: a provider's backup feature protects against some failures, not against mistakes like a wrong delete command or a compromised account. Keep an independent copy.
</details>

**Q10.2 🟥 How much can we afford to lose or wait?** (two key numbers)

| Term | Plain meaning | Our number |
|---|---|---|
| **RPO** (recovery point goal) | "At most how much recent data can we lose?" | `[ ]` hours |
| **RTO** (recovery time goal) | "At most how long can we be down?" | `[ ]` hours |

- **If unsure:** RPO 24 hours, RTO 4 hours for the first 500 customers. Tighten later.

**Q10.3 🟥 Step-by-step restore.**

| Step | Action | Expected result |
|---|---|---|
| 1 | Decide what to restore and to what time (Owner approves) 👤 | Decision written down |
| 2 | `[ ]` Restore into a **new, separate** place first (never overwrite production blindly) | Copy restored |
| 3 | `[ ]` Check the data looks right (count of records, newest record time) | Matches expectation |
| 4 | `[ ]` Switch production to the restored copy | Product works |
| 5 | Run critical-function checks (Q1.2) | All pass |
| 6 | Tell customers what data, if any, was lost (Section 11) | Message sent |

**Q10.4 🟥 Restore test.**
- ☐ I restored a backup on `[date]` and it worked. It took `[ ]` minutes.
- **Repeat every:** `[ ]` months. *(If unsure: every 3 months, and before launch.)*

**Q10.5 🟨 Disaster plan: what if our whole hosting provider or region is gone?**
- **Our plan:** `[ ]`
- **If unsure:** Write "Restore from off-site backup to a new account with [provider]. Expected time: [ ] hours." and review again at 250 customers.

---

## 11. Customer Support & Communication

> **Purpose:** customers forgive problems; they do not forgive silence.

**Q11.1 🟥 How can customers get help, and how fast do we answer?**

| Channel | Where | Hours | First-reply target |
|---|---|---|---|
| Email / helpdesk | `[ ]` | `[ ]` | `[ ]` hours |
| Chat | `[ ]` | `[ ]` | `[ ]` |
| Social / community | `[ ]` | `[ ]` | `[ ]` |

- **If unsure:** One email address, reply within 1 working day (4 hours during launch week).

**Q11.2 🟥 Where do we tell everyone when something is wrong?**
- **Status page link:** `[ ]` **Who updates it:** `[ ]`
- **If unsure:** Use a free status page tool and link it from the website footer.

**Q11.3 🟥 Message templates.** Fill in once; copy-paste during an incident. Keep them honest, short, and free of blame.

**Investigating:**
> "We are aware of a problem with [what customers see]. We are investigating and will update you by [time]. Sorry for the trouble."

**Update / fix in progress:**
> "Update [time]: We found the cause and are working on a fix. [What customers can do meanwhile]. Next update by [time]."

**Resolved:**
> "Resolved [time]: [Feature] is working again. The problem lasted from [start] to [end]. [What we are doing to prevent it]. Thank you for your patience."

**Data or privacy issue** (get the Owner's and a lawyer's approval first):
> "We found that [what happened] affected [who]. [What data]. [What we did]. [What you should do]. Contact us at [address]."

**Your own versions (paste here):** `[ ]`

**Q11.4 🟨 How do we sort support requests?**

| Type | Example | Who handles it | When to escalate to engineering |
|---|---|---|---|
| How-to question | "Where do I click?" | `[ ]` | Never; answer from the help guide |
| Bug | "It crashed" | `[ ]` | If 3+ customers report the same thing |
| Billing | "I was charged twice" | `[ ]` | Immediately if money is wrong |
| Account / data request | "Delete my data" | `[ ]` | Follow privacy rules (Q1.5) |

**Q11.5 🟨 How do we collect and use feedback from the first 500 customers?**
- **Your answer:** `[ ]` *(If unsure: tag every message, review the top 5 themes each week.)*

**Q11.6 🟨 Do we have a help guide or FAQ?**
- ☐ Yes, link: `[ ]` ☐ Not yet; we will write the top 10 questions by `[date]`

---

## 12. Cost, Scaling & Capacity

> **Purpose:** no surprise bills, no surprise crashes.

**Q12.1 🟥 What is our monthly budget for running the product?**
- **Total:** `[ ]` **Alert at 50%, 80%, 100%.** **Who is notified:** `[ ]`

**Q12.2 🟥 What are our biggest costs?**

| Cost | Provider | Estimated per month | Grows with... (customers, data, AI usage) |
|---|---|---|---|
| Hosting | `[ ]` | `[ ]` | `[ ]` |
| Database | `[ ]` | `[ ]` | `[ ]` |
| AI model usage | `[ ]` | `[ ]` | `[ ]` |
| Email / SMS | `[ ]` | `[ ]` | `[ ]` |
| Monitoring tools | `[ ]` | `[ ]` | `[ ]` |
| Other | `[ ]` | `[ ]` | `[ ]` |

**Q12.3 🟥 Spending limits and safety brakes.**
- ☐ Billing alerts turned on in every provider
- ☐ Hard spending cap set where possible, especially for AI usage
- ☐ Rate limits (maximum requests per user) on public features
- **Who can raise a limit?** `[ ]` 👤

**Q12.4 🟨 How much can the system handle today?**
- **Our tested limit:** `[ ]` customers / `[ ]` requests per minute. **Tested on:** `[date]`
- **If unsure:** Run a simple load test on staging before launch and again at 100 customers.

**Q12.5 🟨 Capacity plan by customer count.**

| Customers | What we expect to need | Action to prepare | Done? |
|---|---|---|---|
| 50 | `[ ]` | `[ ]` | ☐ |
| 100 | `[ ]` | `[ ]` | ☐ |
| 250 | `[ ]` | `[ ]` | ☐ |
| 500 | `[ ]` | `[ ]` | ☐ |

**Q12.6 🟨 How do we add capacity in a hurry?**
- **Steps:** `[ ]` **Who approves:** `[ ]`

---

## 13. AI-Agent Operations & Guardrails

> **Purpose:** AI agents are powerful helpers, but they need clear limits. **Principle: agents act, humans approve anything risky.** Every agent action must be traceable.

**Q13.1 🟥 List every AI agent or AI tool that touches the project.**

| Agent / tool name | What it does | Where it runs | Owner (human) | Date approved |
|---|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q13.2 🟥 What may each agent do? (Permission levels)**

| Level | Meaning | Examples | Approval needed |
|---|---|---|---|
| **L0: Read and advise** | Looks, explains, suggests | Read logs, summarize an incident | None |
| **L1: Safe actions** | Reversible, low risk | Restart a staging service, draft a status message, open a ticket | None, but logged |
| **L2: Controlled actions** | Affects production but can be undone | Deploy to production, roll back, change a setting | 👤 Named human approves each time |
| **L3: Forbidden without special approval** | Hard or impossible to undo, or touches money/data | Delete data, change payments, change access rights, send messages to all customers, spend money | 👤 Owner approves in writing, every time |

**Assign levels:**

| Agent | Maximum level | Allowed systems | Forbidden systems |
|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` |

- **If unsure:** Start every agent at **L0 or L1**. Raise the level only after it has behaved well for 30 days.

**Q13.3 🟥 What must an agent do before a risky step?**
1. Say what it plans to do and why, in plain words.
2. Say what could go wrong and how to undo it.
3. Wait for a human "yes" if the step is L2 or L3.
4. Take a backup or snapshot first when data could change.

**Q13.4 🟥 Logs and traceability.**
- **Where are agent actions logged?** `[ ]`
- **Each log entry must show:** time, which agent, which instruction, what it did, which human approved, result.
- **Logs kept for:** `[ ]` days. *(If unsure: 90 days.)*

**Q13.5 🟥 Emergency stop (kill switch).**
- **How do we immediately stop all agents?** `[ ]`
- **Who may do it?** Anyone on the team. **Tested on:** `[date]`
- ☐ Agents' credentials can be revoked in under 5 minutes.

**Q13.6 🟥 What do agents never receive?**
- ☐ Real passwords or master keys (use limited, temporary access instead)
- ☐ Unnecessary customer personal data
- ☐ Permission to change their own permissions
- ☐ Permission to approve their own work

**Q13.7 🟨 How do we change prompts, models, or instructions safely?** (AI changes can break things quietly)
- ☐ Every change to prompts/instructions/model version is saved with a date and reason
- ☐ Tested on a fixed set of sample questions before going live
- ☐ Rolled out to a small group first
- ☐ Rollback = restore previous prompt/model version. **Where is it stored?** `[ ]`

**Q13.8 🟨 If the product itself uses AI (answers customers), how do we keep it safe and good?**

| Question | Your answer |
|---|---|
| What must the AI never say or do? | `[ ]` |
| How do we check answer quality? (sample review each week) | `[ ]` |
| How can a customer report a bad AI answer? | `[ ]` |
| What happens if the AI provider is down or too slow? | `[ ]` |
| Is there a human fallback for important cases? | `[ ]` |
| Are customers told they are talking to AI? | ☐ Yes ☐ No *(If unsure: Yes.)* |
| Is customer data sent to the AI provider, and is that allowed by our privacy promise? | `[ ]` |

**Q13.9 🟨 AI incident types and responses.**

| Problem | Example | First action |
|---|---|---|
| Wrong or harmful answers | AI gives dangerous advice | Switch to safe fallback message; L2 approval to disable feature |
| Agent took an unexpected action | Deleted a file | Press the kill switch (Q13.5); restore from backup; start incident |
| Cost spike | AI bill jumps 10x | Hit the spending cap; rate-limit; investigate |
| Data exposure | Private data appeared in an answer | Treat as security incident (Q5.5) |

---

## 14. Routine Maintenance Calendar

> **Purpose:** small regular chores prevent big emergencies. Assign each to a named person.

| How often | Task | Owner | Done last on |
|---|---|---|---|
| **Daily** (launch and growth) | Health check (Q8.3) | `[ ]` | `[ ]` |
| **Daily** | Check backups succeeded | `[ ]` | `[ ]` |
| **Daily** | Answer support inbox | `[ ]` | `[ ]` |
| **Weekly** | Review errors, slow pages, top support themes | `[ ]` | `[ ]` |
| **Weekly** | Review AI agent logs and AI answer quality | `[ ]` | `[ ]` |
| **Weekly** | Check costs vs budget | `[ ]` | `[ ]` |
| **Monthly** | Install software updates and security patches | `[ ]` | `[ ]` |
| **Monthly** | Review who has access (Q5.2) | `[ ]` | `[ ]` |
| **Monthly** | Review alerts: remove noisy ones | `[ ]` | `[ ]` |
| **Quarterly** | Test restoring a backup (Q10.4) | `[ ]` | `[ ]` |
| **Quarterly** | Rotate secrets (Q5.4) | `[ ]` | `[ ]` |
| **Quarterly** | Run an incident drill (Q9.5) | `[ ]` | `[ ]` |
| **Quarterly** | Re-read and update this runbook | `[ ]` | `[ ]` |
| **Weekly** | Review customer and delivery metrics (Section 22) | `[ ]` | `[ ]` |
| **Quarterly** | Review vendors, contracts, and exit plans (Section 20) | `[ ]` | `[ ]` |
| **Quarterly** | Collect compliance evidence and review data retention (Section 21) | `[ ]` | `[ ]` |
| **Quarterly** | Find outdated docs ("last tested" older than 90 days) (Section 24) | `[ ]` | `[ ]` |
| **Yearly** | Review domain, certificates, and contracts expiry dates | `[ ]` | `[ ]` |

**Important expiry dates** (domain, security certificates, licenses, API plans):

| Item | Expires on | Renewal owner | Reminder set? |
|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | ☐ |

---

## 15. Go / No-Go Launch Checklist

> **Purpose:** the final gate before the first customer. **Every 🟥 item must be ✅ to launch.** If any is not, the answer is **NO-GO** until fixed or the Owner accepts the risk in writing.

### Product readiness
- ☐ 🟥 All critical functions (Q1.2) work on production
- ☐ 🟥 Tests pass; no known SEV-1 or SEV-2 bugs
- ☐ 🟥 AI-written code was reviewed by a human 👤
- ☐ 🟨 Tested on the devices and browsers customers will use
- ☐ 🟨 Sign-up, login, password reset, and payment tested end to end

### Operations readiness
- ☐ 🟥 Deploy steps tested (Section 6)
- ☐ 🟥 Smoke test list ready and passing on production (Q19.2)
- ☐ 🟥 Changes are approved and logged using our change process (Section 17)
- ☐ 🟥 Rollback practiced on staging (Section 7)
- ☐ 🟥 Monitoring and alerts tested: someone actually received a test alert (Section 8)
- ☐ 🟥 Backup taken **and restore tested** (Section 10)
- ☐ 🟥 On-call person and backup named, and they have read this runbook (Section 2)
- ☐ 🟥 Incident steps and message templates ready (Sections 9 and 11)
- ☐ 🟨 Load test done and tripwires set (Section 12)

### Security and legal readiness
- ☐ 🟥 Secrets stored safely; none in code or in this file (Section 5)
- ☐ 🟥 Two-step login turned on for all admin accounts
- ☐ 🟥 Privacy policy and terms published `[link]`
- ☐ 🟥 Required laws and rules checked (Q1.5, Section 21)
- ☐ 🟥 We know how to handle a customer request to see, export, or delete their data (Q21.4)
- ☐ 🟨 Access list reviewed; test accounts removed

### AI-agent readiness
- ☐ 🟥 Every agent listed with permission level and human owner (Section 13)
- ☐ 🟥 Kill switch tested
- ☐ 🟥 Agent actions are logged
- ☐ 🟨 AI answer quality checked on sample questions

### Customer readiness
- ☐ 🟥 Support channel is live and someone is assigned (Section 11)
- ☐ 🟥 Status page is live
- ☐ 🟨 Help guide or FAQ published
- ☐ 🟨 Spending caps and billing alerts set (Section 12)

### Decision

| Field | Your answer |
|---|---|
| Decision | ☐ **GO** ☐ **NO-GO** |
| Date and time | `[ ]` |
| Decided by (Owner) | `[ ]` |
| Risks accepted (if any) and why | `[ ]` |
| Items to finish within 7 days after launch | `[ ]` |

---

## 16. First 500 Customers: Milestone Reviews

> **Purpose:** at each milestone, stop for 30 minutes, look at the facts, and decide what to fix before the next jump. Copy the table for each milestone.

**Milestones to review:** 🟥 First customer, 🟥 10, 🟥 50, 🟥 100, 🟨 250, 🟥 500.

### Milestone review form (copy for each)

| Question | Your answer |
|---|---|
| Milestone reached (customer count) and date | `[ ]` |
| How many incidents since last review? (by severity) | `[ ]` |
| Did we meet our uptime goal (Q1.6)? | `[ ]` |
| Average support reply time vs target | `[ ]` |
| Top 3 customer complaints or requests | 1. `[ ]` 2. `[ ]` 3. `[ ]` |
| Cost vs budget | `[ ]` |
| Highest system usage reached (%) | `[ ]` |
| Did any tripwire (Q4.6) fire? What did we do? | `[ ]` |
| Key metrics: activation, retention, churn, customer health (Section 22) | `[ ]` |
| Delivery health: deploy frequency, failed changes, time to restore (Q22.3) | `[ ]` |
| Any customer data requests or privacy issues? (Section 21) | `[ ]` |
| Did any AI agent do something unexpected? | `[ ]` |
| Is any step in this runbook wrong, missing, or confusing? | `[ ]` |
| Do we need to change anything before the next milestone? | `[ ]` |
| Decision: ☐ Continue ☐ Pause sign-ups and fix first | `[ ]` |
| Owner and date | `[ ]` |

### Milestone-specific focus

| Milestone | Special focus |
|---|---|
| **1st customer** | Watch everything live. Be ready to help by hand. Confirm the whole journey (sign-up, use, support) works. |
| **10** | Are people finishing the main task? Any repeated confusion? Fix the top issue. |
| **50** | Do the tripwires make sense? Is support manageable for the team? Review costs honestly. |
| **100** | Test a restore again. Review access list. Run a load test. Is one person doing too much? |
| **250** | Review the capacity plan (Q12.5). Consider a second on-call person and a clear support process. |
| **500** | Full runbook review. Decide steady-state routine (Q4.7). Celebrate, then write what you learned. |

---

## 17. Change Management & Approvals

> **Purpose:** every change to production is requested, judged for risk, approved by the right person, and written down. This is what keeps AI-speed development from turning into AI-speed accidents.

**Q17.1 🟥 What counts as a "change"?** (tick all that apply to you)
- ☐ New code or a new version ☐ Settings or configuration ☐ Database structure changes ☐ Hosting or infrastructure changes
- ☐ Access or permission changes ☐ Changes to AI prompts, models, or agent instructions ☐ Vendor or plan changes ☐ DNS / domain changes
- **If unsure:** If it can change what customers experience or what data is stored, it is a change.

**Q17.2 🟥 How risky is it? (Risk levels and who approves.)**

| Risk | Meaning | Examples | Who approves | Extra safety |
|---|---|---|---|---|
| **Low** | Small, easy to undo, few customers affected | Text change, small bug fix | Reviewer 👤 | Normal tests |
| **Medium** | Affects an important feature or many customers, undoable | New feature, setting change | Release manager 👤 | Test on staging; deploy in quiet hours |
| **High** | Touches money, login, customer data, access, or cannot be undone | Payment change, database restructure, delete data | Owner 👤 in writing | Backup first; rollback rehearsed; small-group release; two people present |

- **If unsure:** Pick the higher level.

**Q17.3 🟥 What does a change request contain?** (copy this form; use your task board or a document)

| Field | Your answer |
|---|---|
| Change title and ID | `[ ]` |
| Requested by / date | `[ ]` |
| What is changing and why? | `[ ]` |
| Risk level (Q17.2) | `[ ]` |
| Who/what could be affected? | `[ ]` |
| Test evidence (link) | `[ ]` |
| Rollback plan (link to Section 7 steps) | `[ ]` |
| Planned date, time, and duration | `[ ]` |
| Approved by (name, date) | `[ ]` |
| Done by (name or agent) and result | `[ ]` |

**Q17.4 🟥 What is the rule for emergency changes?** (a fix needed right now to stop an incident)
- **Your answer:** The on-call person may make the smallest safe fix without waiting for normal approval. They must (1) tell the Owner at once, (2) write down what they did, and (3) complete the change request form within 1 working day.
- **AI agents:** may **not** make emergency changes above Level L1 without a human "yes" (Section 13).

**Q17.5 🟥 Where are all changes recorded?**
- **Your answer:** `[ ]` *(If unsure: your task board plus the release log from Q6.7. One list, one place.)*

**Q17.6 🟨 Change freeze calendar.** (times when only emergency changes are allowed)

| Period | Reason | From | To |
|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` |

- **Example:** "Launch week", "Black Friday", "Owner on holiday".

---

## 18. Environment & Infrastructure Setup

> **Purpose:** be able to build (and rebuild) every environment the same way each time. Fill this during Phase A and update it whenever infrastructure changes.

**Q18.1 🟥 Setup checklist for each environment.** (tick per environment)

| Step | Dev | Staging | Production |
|---|---|---|---|
| Accounts created with 2FA and the right owners (Q5.2) | ☐ | ☐ | ☐ |
| Hosting project/app created | ☐ | ☐ | ☐ |
| Database created and connected | ☐ | ☐ | ☐ |
| File storage created | ☐ | ☐ | ☐ |
| Secrets stored in the vault, not in code (Q5.1) | ☐ | ☐ | ☐ |
| Domain name bought and DNS records set | n/a | ☐ | ☐ |
| Security certificate (HTTPS) active and auto-renewing | n/a | ☐ | ☐ |
| Email sending set up with sender checks (SPF, DKIM, DMARC) | n/a | ☐ | ☐ |
| Monitoring and alerts connected (Section 8) | n/a | ☐ | ☐ |
| Backups turned on (Section 10) | n/a | ☐ | ☐ |
| Billing alerts and spending caps set (Q12.3) | ☐ | ☐ | ☐ |
| Error tracking connected | ☐ | ☐ | ☐ |

**Q18.2 🟥 Describe the automatic pipeline that moves code from a developer's computer to customers (CI/CD).**

| Stage | What happens | Tool | Stops the pipeline if it fails? |
|---|---|---|---|
| 1. Save change | Code saved in version control with a clear message | `[ ]` | n/a |
| 2. Automatic tests | Unit and integration tests run | `[ ]` | ☐ Yes |
| 3. Security scan | Scan for exposed secrets and risky libraries | `[ ]` | ☐ Yes |
| 4. Build | Package the product | `[ ]` | ☐ Yes |
| 5. Deploy to staging | Practice copy updated | `[ ]` | ☐ Yes |
| 6. Human approval 👤 | Named person says yes | `[ ]` | n/a |
| 7. Deploy to production | Customers get the new version | `[ ]` | ☐ Yes |
| 8. Smoke test | Quick check that critical functions work (Q19.2) | `[ ]` | ☐ Yes |

- **If unsure:** Stages 2, 3, and 6 are the minimum. Never let anyone (or any AI agent) push straight to production without them.

**Q18.3 🟥 What is different between staging and production on purpose?** (settings, keys, data, size)
- **Your answer:** `[ ]`
- **Rule:** Staging must be **as similar to production as possible**, but must **never** hold real customer data or real payment keys.

**Q18.4 🟥 Can we rebuild production from scratch?**
- ☐ Yes, steps are written in: `[ ]` (setup scripts or "infrastructure as code")
- ☐ Partly: the missing pieces are `[ ]`
- ☐ No. **Action:** list every manual setting you ever clicked and save it as written steps by `[date]`.
- **Rebuilt and tested on:** `[date]`

**Q18.5 🟥 Domain, DNS, and certificates register.**

| Item | Where managed | Login owner | Expires / renews on | Auto-renew on? |
|---|---|---|---|---|
| Domain name | `[ ]` | `[ ]` | `[ ]` | ☐ |
| DNS records | `[ ]` | `[ ]` | n/a | n/a |
| HTTPS certificate | `[ ]` | `[ ]` | `[ ]` | ☐ |

**Q18.6 🟨 Configuration list.** (write the setting names, never the secret values)

| Setting name | What it does | Where it is set | Secret? | Different per environment? |
|---|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | ☐ | ☐ |

---

## 19. Testing & QA in Production

> **Purpose:** catch problems before customers do, and keep catching them after launch.

**Q19.1 🟥 What kinds of testing do we do?**

| Test type | What it checks | When it runs | Tool | Owner |
|---|---|---|---|---|
| **Unit / component** | Small pieces work | Every change | `[ ]` | `[ ]` |
| **Integration** | Pieces work together | Every change | `[ ]` | `[ ]` |
| **End-to-end** | A pretend user completes real journeys | Before each release | `[ ]` | `[ ]` |
| **Smoke test** | Critical functions work right now | After each deploy | `[ ]` | `[ ]` |
| **Load test** | System copes with many users | Before launch, at 100, at 250 | `[ ]` | `[ ]` |
| **Security test** | Known weaknesses are absent | Every release; deeper check before launch | `[ ]` | `[ ]` |
| **AI quality test** | AI answers stay good and safe | Every prompt/model change; weekly | `[ ]` | `[ ]` |

- **If unsure:** Start with end-to-end tests for your 3 critical functions (Q1.2) and a smoke test. Add the rest over time.

**Q19.2 🟥 Smoke test list (run after every production deploy, takes under 10 minutes).**

| # | Check | Expected result | Pass? |
|---|---|---|---|
| 1 | Open the home page | Loads in under `[ ]` seconds | ☐ |
| 2 | Sign up with a test account | Account created, welcome message arrives | ☐ |
| 3 | Log in and log out | Works | ☐ |
| 4 | Do the main task of the product | `[ ]` | ☐ |
| 5 | Make a test payment (using a test/sandbox method or a refundable small amount) | Payment recorded | ☐ |
| 6 | Check the error dashboard | No new spike | ☐ |
| 7 | (If product uses AI) Ask 3 known questions | Answers are correct and safe | ☐ |

**Q19.3 🟨 Synthetic checks: a robot user that runs on a schedule.**
- **Which journeys does it run?** `[ ]` **How often?** Every `[ ]` minutes *(If unsure: every 5 minutes for login, every 15 for the main task.)*
- **Who is alerted if it fails?** `[ ]`

**Q19.4 🟥 How do we sort and fix bugs?**

| Bug type | Example | Fix within |
|---|---|---|
| **Blocker** | Critical function broken (this is a SEV-1, go to Section 9) | Immediately |
| **High** | Important feature broken, workaround exists | 2 working days |
| **Medium** | Annoying but not blocking | Within 2 weeks |
| **Low** | Cosmetic | When convenient |

- **Where are bugs recorded?** `[ ]` **Who sorts new bugs, and how often?** `[ ]` *(If unsure: one person, daily during phases C and D.)*

**Q19.5 🟥 Test data rules.**
- ☐ Test accounts are clearly named (for example `test+001@yourdomain`) and removed or marked before launch reports
- ☐ Real customer data is **never** copied to staging or to developer computers
- ☐ Test payments use sandbox/test modes only
- ☐ Tests in production only use test accounts and never change real customers' data

**Q19.6 🟨 Every fixed bug gets a test.**
- **Rule:** when we fix a bug, we add a test so it cannot quietly return. ☐ Agreed

**Q19.7 🟨 If the product uses AI: the "golden question set".**
- **Where is the list of 20+ example questions with good answers?** `[ ]`
- **How often is it run?** `[ ]` *(If unsure: after every prompt or model change and weekly.)*
- **What score is "good enough"?** `[ ]` **What do we do if the score drops?** `[ ]`

---

## 20. Vendor & Third-Party Management

> **Purpose:** every outside service you depend on is listed, understood, and replaceable. AI providers, payment providers, and hosting can change prices, terms, or models.

**Q20.1 🟥 Vendor register.** (one row per outside service)

| Vendor | What we use it for | Plan and monthly cost | Contract / renewal date | Support contact | Their status page | Data we send them | Critical? (Y/N) | Owner |
|---|---|---|---|---|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q20.2 🟥 Before we adopt a new vendor, did we check:**
- ☐ Price now and price at 500 customers ☐ Uptime promise and past outages ☐ Where our data is stored
- ☐ Security and privacy information (certifications, data protection terms) ☐ Can we export our data easily?
- ☐ Limits and rate limits ☐ How good is their support? ☐ What happens to our service if they raise prices or shut down?
- **If unsure:** Ask the vendor these questions in writing and keep the answers.

**Q20.3 🟥 Exit plan for each critical vendor.**

| Vendor | How do we export our data? | What could replace them? | How long would switching take? | Last reviewed |
|---|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q20.4 🟨 What do we do if a vendor...**

| Situation | Our plan |
|---|---|
| ...has an outage | Follow Q3.4 workaround; check their status page; tell customers (Section 11) |
| ...raises prices a lot | `[ ]` |
| ...retires a feature or an AI model version we use | `[ ]` *(If unsure: keep a list of retirement dates; test the replacement on staging before the deadline.)* |
| ...is bought, changes its terms, or shuts down | `[ ]` |
| ...has a security breach | Treat as an incident (Section 9, Q5.5). Rotate any keys shared with them. |

**Q20.5 🟨 How do we contact vendor support in an emergency?**
- **Your answer:** `[ ]` *(Write the exact steps, the support plan we pay for, and the account number or ID, never the password.)*

---

## 21. Compliance, Privacy & Data Requests

> **Purpose:** respect customers' data and the rules. **This section helps you organize; it is not legal advice.** Laws differ by country, state, and industry, and change often. Ask a qualified lawyer before launch, especially for payments, health data, children's data, or customers in the EU/UK or California.

**Q21.1 🟥 Which rules apply to us?**

| Framework | In one line | Applies? | Owner | Notes |
|---|---|---|---|---|
| **GDPR / UK GDPR** | Privacy law for people in the EU/UK: lawful reason to use data, user rights (see, fix, delete, export), breach notice | ☐ Yes ☐ No ☐ Unsure | `[ ]` | `[ ]` |
| **CCPA / CPRA** | California privacy law: right to know, delete, correct, and opt out of "sale/sharing" of data | ☐ Yes ☐ No ☐ Unsure | `[ ]` | `[ ]` |
| **SOC 2 / ISO 27001** | Security standards that business customers often ask for; need written proof that you follow your own rules | ☐ Yes ☐ No ☐ Later | `[ ]` | `[ ]` |
| **PCI DSS** | Rules for handling card payments | ☐ Yes ☐ No ☐ Unsure | `[ ]` | `[ ]` |
| **HIPAA** | US rules for health information | ☐ Yes ☐ No ☐ Unsure | `[ ]` | `[ ]` |
| **COPPA / children's privacy** | Extra rules if children (in the US, under 13) may use the product | ☐ Yes ☐ No ☐ Unsure | `[ ]` | `[ ]` |
| Other (industry, country) | `[ ]` | ☐ Yes ☐ No ☐ Unsure | `[ ]` | `[ ]` |

- **If unsure:** Mark "Unsure", assign an owner, and set a date to get advice **before** launch.

**Q21.2 🟥 Data map: what personal data do we hold?**

| Data type | Why we need it | Where it is stored | Who can see it | Sent to which vendors | How long we keep it |
|---|---|---|---|---|---|
| Name and email | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Payment info | `[ ]` | Payment provider only (never our own database) | `[ ]` | `[ ]` | `[ ]` |
| Usage / analytics data | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Uploaded files or content | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Logs | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Support messages | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

- **Rule:** collect only what you really need ("data minimization").

**Q21.3 🟥 Keep and delete schedule.**
- **Customer account data is deleted:** `[ ]` days after account closure. **Backups containing it expire after:** `[ ]` days.
- **Logs deleted after:** `[ ]` days. **Support messages deleted after:** `[ ]`.
- **If unsure:** Keep data only as long as you need it, write the number down, and make sure backups follow it too.

**Q21.4 🟥 What do we do when a customer asks about their data?** (see it, correct it, export it, delete it, or stop us selling/sharing it)

| Step | Action | Who |
|---|---|---|
| 1 | Log the request: date received, name, what was asked | `[ ]` |
| 2 | **Verify identity** (for example, reply to the account's email) so we never give data to the wrong person | `[ ]` |
| 3 | Find all their data using the data map (Q21.2) | `[ ]` |
| 4 | Do it: export, correct, or delete (including vendors and, in time, backups) | `[ ]` |
| 5 | Reply to the customer and record the date done | `[ ]` |

- **Time limits:** Privacy laws set deadlines, commonly about **one month** under GDPR and about **45 days** under CCPA/CPRA, sometimes extendable. **Confirm current deadlines with your lawyer.** Our internal target: `[ ]` days.
- **Where requests are logged:** `[ ]`

**Q21.5 🟥 If personal data is breached or lost (extends Q5.5).**
- ☐ Contain it (Section 9) ☐ Record what data, whose, when ☐ Tell the Owner and Security contact immediately
- ☐ Ask the lawyer **within hours** about notice duties. Some laws require telling the regulator quickly (GDPR: generally within 72 hours of becoming aware, where required) and affected people; US state laws and HIPAA have their own rules.
- **Breach notice deadline we follow:** `[ ]` **Who decides to notify:** `[ ]` 👤

**Q21.6 🟥 Public documents and consent.**
- ☐ Privacy policy published `[link]` and matches what we really do ☐ Terms of service published `[link]`
- ☐ Cookie/tracking consent set up where required ☐ Marketing emails have an unsubscribe link
- ☐ We record consent (who agreed, when, to what) where required

**Q21.7 🟥 Payments (PCI DSS).**
- ☐ We use a payment provider's hosted checkout or fields, so card numbers **never touch our servers or logs**
- ☐ We never store full card numbers, security codes (CVV), or paste them anywhere
- ☐ Payment provider's compliance information saved: `[link]`

**Q21.8 🟨 Health data (HIPAA), children's data (COPPA), other special data.**
- **Do we handle any?** ☐ No ☐ Yes
- **If yes:** list the extra rules we follow and the vendor agreements signed: `[ ]`
- **If unsure:** do **not** collect it until you get legal advice. Add an age check if children might sign up.

**Q21.9 🟨 AI and privacy.**

| Question | Your answer |
|---|---|
| Which customer data is sent to AI providers? | `[ ]` |
| Does the AI provider keep it or train on it? What is their setting/contract? | `[ ]` |
| Do customers know their data is processed by AI? | ☐ Yes ☐ No |
| Do AI agents or developers see real customer data? (They should not by default.) | `[ ]` |
| Can customers opt out of AI processing? | `[ ]` |

**Q21.10 🟨 Security-audit readiness (SOC 2 / ISO 27001 style).** Start collecting proof from day one. Auditors want to see that you *did* what you *said*.

| Evidence | Where in this runbook | Where we save the proof | Frequency |
|---|---|---|---|
| Access reviews | Q5.2, Section 14 | `[ ]` | Monthly |
| Change approvals | Section 17 | `[ ]` | Every change |
| Backup restore tests | Q10.4 | `[ ]` | Quarterly |
| Incident records and reviews | Section 9, Appendix C | `[ ]` | Every incident |
| Vendor reviews | Section 20 | `[ ]` | Quarterly |
| Security training / awareness for the team | `[ ]` | `[ ]` | Yearly |
| Onboarding and offboarding records | Section 23, Q5.3 | `[ ]` | Each time |
| AI agent logs and approvals | Section 13 | `[ ]` | Continuous |

---

## 22. Product Analytics, Metrics & Customer Health

> **Purpose:** know whether customers are succeeding and whether your delivery is healthy, using a few numbers rather than a hundred.

**Q22.1 🟥 What is our one "north-star" number?** (the best sign that customers get value)
- **Your answer:** `[ ]`
- **Example:** "Number of orders placed per week", "Customers who finish setup".
- **If unsure:** Ask, "What is the one action that proves a customer got value?"

**Q22.2 🟥 Customer journey numbers.**

| Stage | Plain meaning | How we measure it | Where to see it | Our target |
|---|---|---|---|---|
| **Sign-up** | People who create an account | `[ ]` | `[ ]` | `[ ]` |
| **Activation** | People who do the key first action | `[ ]` | `[ ]` | `[ ]`% of sign-ups |
| **Retention** | People who come back | `[ ]` | `[ ]` | `[ ]`% after 7 / 30 days |
| **Revenue** | Money coming in (if paid) | `[ ]` | `[ ]` | `[ ]` |
| **Churn** | People who leave or cancel | `[ ]` | `[ ]` | Under `[ ]`% per month |
| **Support load** | Support requests per customer | `[ ]` | `[ ]` | Under `[ ]` per customer per month |
| **Satisfaction** | How happy people are (rating or short survey) | `[ ]` | `[ ]` | `[ ]` |

**Q22.3 🟨 Delivery health (are we shipping safely?).** These four are widely used measures of software delivery performance.

| Measure | Plain meaning | Our value now | Our goal |
|---|---|---|---|
| **Deploy frequency** | How often we release | `[ ]` | `[ ]` |
| **Lead time for changes** | Time from finished change to live | `[ ]` | `[ ]` |
| **Change failure rate** | Share of releases that cause a problem or rollback | `[ ]`% | Under `[ ]`% |
| **Time to restore** | How long it takes to recover from an incident | `[ ]` | Under `[ ]` |

- **If unsure:** Just count them in a simple list each month. Trends matter more than perfect numbers.

**Q22.4 🟨 Customer health traffic lights.**

| Colour | Meaning | Our rule (example in brackets) | Action |
|---|---|---|---|
| 🟢 **Healthy** | Using it and happy | `[ ]` (used 3+ times this week) | Ask for feedback or a review |
| 🟡 **At risk** | Usage dropping or confused | `[ ]` (no login for 14 days; 2+ support tickets) | Reach out with help |
| 🔴 **Likely to leave** | Stopped using or unhappy | `[ ]` (no login for 30 days; asked to cancel) | Personal message from `[owner]` |

**Q22.5 🟨 Targets at each milestone.**

| Customers | Activation target | Retention target | Support load target | Incident target |
|---|---|---|---|---|
| 10 | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 50 | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 100 | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 250 | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 500 | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q22.6 🟨 Where is the dashboard, and who reviews it?**
- **Dashboard link:** `[ ]` **Reviewed by:** `[ ]` **How often:** weekly *(If unsure: every Monday, 20 minutes.)*

**Q22.7 🟨 Analytics privacy.**
- ☐ We track the minimum needed ☐ No private content in analytics ☐ Tracking follows our privacy policy and consent rules (Q21.6)

---

## 23. Handover & Onboarding

> **Purpose:** a new person, a new agent, or a replacement owner can safely run the product within days. It also protects you when someone is ill or on holiday.

**Q23.1 🟥 New human team member: Day 1 checklist.**
- ☐ Read this runbook (assign: Sections 0 to 3, 6 to 9, 11) ☐ Accounts created with least access and 2FA (Q5.2)
- ☐ Added to incident channel, alerts, and escalation ladder (Q2.2) ☐ Shown the dashboards (Sections 8, 22)
- ☐ Introduced to the on-call person and the Owner ☐ Signed any confidentiality or data-handling agreement required (Section 21)

**Q23.2 🟨 First week plan.**

| Day | Learn or do | Done |
|---|---|---|
| 1 | Read, get access, join channels | ☐ |
| 2 | Deploy a harmless change to staging with a buddy | ☐ |
| 3 | Practice a rollback on staging (Section 7) | ☐ |
| 4 | Walk through an old incident review (Appendix C) | ☐ |
| 5 | Shadow the on-call person; ask 5 questions; update the runbook where it was unclear | ☐ |

**Q23.3 🟨 When do they join the on-call rotation?**
- **Your answer:** After `[ ]` weeks **and** after one shadow shift. *(If unsure: 4 weeks.)*

**Q23.4 🟥 Onboarding a new AI agent.**
- ☐ Listed in Section 13 (Q13.1) with a human owner ☐ Starts at the lowest permission level (L0 or L1)
- ☐ Given its instructions in a saved, version-controlled file (Q13.7) ☐ Tested on staging and on the golden question set where relevant
- ☐ Logging works (Q13.4) ☐ Kill switch tested ☐ 30-day "probation": the owner reviews logs weekly before raising its level

**Q23.5 🟥 When the Owner, on-call person, or key engineer changes: the handover checklist.**
- ☐ Written handover meeting held; this runbook walked through together ☐ All accounts and vaults transferred, old access removed (Q5.3)
- ☐ Section 2 contacts and Document Control updated ☐ Vendor accounts and billing owners updated (Section 20)
- ☐ Domain, DNS, and certificate owners updated (Q18.5) ☐ New person successfully performed a deploy, a rollback, and a restore test

**Q23.6 🟨 Single points of failure ("What if only one person knows?").**

| Knowledge or access that only one person has | Who | How we spread it | By when |
|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` |

---

## 24. Documentation & Knowledge Base Upkeep

> **Purpose:** documentation that is wrong is worse than none. Make keeping it correct part of the work, not an extra chore.

**Q24.1 🟥 Where does each kind of document live?**

| Document | Location (link) | Owner |
|---|---|---|
| This runbook | `Deployment and production operations/Operational_Runbooks.md` | `[ ]` |
| Architecture / system diagram | `[ ]` | `[ ]` |
| Procedure cards (Appendix A format) | `[ ]` | `[ ]` |
| Customer help guide / FAQ | `[ ]` | `[ ]` |
| Decision log (Q24.4) | `[ ]` | `[ ]` |
| Post-incident reviews | `[ ]` | `[ ]` |

**Q24.2 🟥 The update rule.**
- **Our rule:** If a change affects how we deploy, roll back, monitor, back up, or get help, **we update this runbook the same day** and add a row to the change log. The change request (Section 17) must tick: ☐ "Runbook updated or not needed."
- **AI agents:** an agent that changes infrastructure or a procedure must also propose the matching document update for human review.

**Q24.3 🟨 How do we find out-of-date pages?**
- **Rule:** every procedure shows "last tested on `[date]`". Anything not tested in `[ ]` days (*If unsure: 90*) gets flagged and reviewed. **Who checks:** `[ ]`

**Q24.4 🟨 Decision log: why did we choose what we chose?**

| Date | Decision | Options considered | Why we chose this | Who decided | Review again on |
|---|---|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Q24.5 🟨 Keeping this template consistent across many projects.**

| Question | Your answer |
|---|---|
| Where is the master (blank) copy of this template? | `[ ]` |
| Who owns the master template? | `[ ]` |
| How does a project upgrade to a newer template version? | ☐ Compare the new template with the project copy, copy over new sections, record in change log |
| What may a project change? | Answers, extra sections, and company-specific examples |
| What may a project NOT change? | The 🟥 required questions, the severity levels' meaning, and the AI-agent permission levels, unless the master owner approves |
| How often is the master reviewed? | `[ ]` *(If unsure: twice a year, plus after every serious incident that exposed a gap.)* |

**Q24.6 🟨 Writing style rules.**
- ☐ Short sentences ☐ One action per step ☐ Exact names, links, and commands ☐ Expected result for every step ☐ Dates as `YYYY-MM-DD` ☐ No secrets

---

## 25. Decommissioning & Shutdown

> **Purpose:** ending things safely: a feature, a customer, or the whole product. Plan the exit so no data is left exposed and no bills keep running. Fill this before launch only if it is simple; update it at 250 customers.

**Q25.1 🟨 Which kind of ending is this?**
- ☐ Retire a feature ☐ A customer leaves or deletes their account ☐ Pause the product ☐ Shut down the whole product ☐ Replace a vendor or system

**Q25.2 🟨 Retiring a feature: steps.**

| Step | Action | Owner | Done |
|---|---|---|---|
| 1 | Decide and record why (decision log, Q24.4) | `[ ]` | ☐ |
| 2 | Check who still uses it (analytics, Section 22) | `[ ]` | ☐ |
| 3 | Tell customers early, with the date and an alternative | `[ ]` | ☐ |
| 4 | Turn it off with a feature switch first (easy to undo) | `[ ]` | ☐ |
| 5 | After `[ ]` days with no problems, delete code, data, and scheduled jobs | `[ ]` | ☐ |
| 6 | Remove from docs, alerts, tests, and costs | `[ ]` | ☐ |

**Q25.3 🟥 A customer leaves: account closure steps.** (links to Q21.4)
- ☐ Offer a data export ☐ Confirm identity ☐ Cancel billing and handle refunds as promised ☐ Delete or anonymize data on the schedule in Q21.3
- ☐ Remove them from marketing lists ☐ Confirm to the customer in writing ☐ Record the date done

**Q25.4 🟨 Pause or full shutdown plan.**

| Step | Action | Owner | Target date |
|---|---|---|---|
| 1 | Owner makes and records the decision 👤 | `[ ]` | `[ ]` |
| 2 | Check contract terms, refunds, and legal duties (ask a lawyer) | `[ ]` | `[ ]` |
| 3 | Announce to customers with enough notice: `[ ]` days | `[ ]` | `[ ]` |
| 4 | Let customers export their data | `[ ]` | `[ ]` |
| 5 | Stop sign-ups and new charges | `[ ]` | `[ ]` |
| 6 | Take a final backup and decide how long to keep it (legal reasons) | `[ ]` | `[ ]` |
| 7 | Delete customer data, including backups and vendor copies, following Section 21 | `[ ]` | `[ ]` |
| 8 | Revoke all access: people, AI agents, API keys (Section 5, Section 13) | `[ ]` | `[ ]` |
| 9 | Cancel vendors, subscriptions, and spending (Section 20) | `[ ]` | `[ ]` |
| 10 | Redirect or retire domains; show a shutdown page if needed | `[ ]` | `[ ]` |
| 11 | Archive code, docs, decisions, and this runbook | `[ ]` | `[ ]` |
| 12 | Write a final review: what we learned (use Appendix C style) | `[ ]` | `[ ]` |

**Q25.5 🟨 Proof of deletion.**
- **How do we prove data was deleted?** `[ ]` *(If unsure: keep a dated checklist and screenshots or vendor confirmations.)*

**Q25.6 🟨 "Stop the bills" checklist.**
- ☐ Hosting ☐ Database ☐ Storage ☐ Domain (or choose to keep) ☐ AI usage ☐ Monitoring tools ☐ Email/SMS ☐ Paid licenses ☐ Scheduled jobs

---

## 26. Self-Check: Is This Runbook Ready?

> Give this document to someone who did **not** write it. Ask them to answer these questions using **only** this file. If they get stuck, the runbook needs work.

- ☐ **Test 1:** "Something is broken at 2 a.m. Who do you call and what do you do first?" Answered in under 2 minutes.
- ☐ **Test 2:** "Deploy the next version." Done with no questions to the author.
- ☐ **Test 3:** "Undo the last deploy." Done in under 15 minutes.
- ☐ **Test 4:** "Where is the latest backup, and how do you restore it?" Answered correctly.
- ☐ **Test 5:** "What may the AI agent do alone, and what needs approval?" Answered correctly.
- ☐ **Test 6:** "What do you tell customers during an outage?" Message ready to send.
- ☐ **Test 7:** "A customer asks us to delete their data. What do you do?" Steps followed correctly (Q21.4).
- ☐ **Test 8:** "A change is needed on production today. Who approves it and what must be recorded?" Answered correctly (Section 17).
- ☐ **Test 9:** "Our payment provider (or AI provider) is down. What happens?" Answered from Q3.4 and Q20.4.
- ☐ **Test 10:** "You are the new teammate. What do you do on Day 1?" Answered from Section 23.

**Quality checklist (the author ticks these):**

- ☐ No `[ ]` blanks left; everything is filled, `N/A`, or `TBD` with an owner and date
- ☐ Every step has an **expected result**
- ☐ Every procedure has a **named owner** and a **backup person**
- ☐ All links open and go to the right place
- ☐ Commands were copy-pasted and tested, not typed from memory
- ☐ No passwords, keys, or private customer data in this file
- ☐ Dates are `YYYY-MM-DD`
- ☐ Document control and change log updated
- ☐ The reader test above passed

**If any item fails:** fix it, update the change log, and re-test.

---

## Appendix A: One-Procedure Runbook Card (copy for each new procedure)

> Use this when you need a detailed step-by-step for one specific task or problem (for example, "Restart the database" or "Fix failed payments"). Save each card as its own section below, or link to it.

### Card: [Procedure name]

| Field | Your answer |
|---|---|
| **Purpose** (one sentence) | `[ ]` |
| **When to use it** (trigger: alert name, symptom, or schedule) | `[ ]` |
| **When NOT to use it** | `[ ]` |
| **Owner / backup** | `[ ]` / `[ ]` |
| **Who may perform it** | ☐ Human only ☐ AI agent (level: `[ ]`) with approval from `[ ]` |
| **Risk level** | ☐ Low ☐ Medium ☐ High (⚠️ needs approval) |
| **Time needed** | `[ ]` minutes |
| **Before you start** (access, tools, backups needed) | `[ ]` |
| **Last tested on** | `[ ]` |

**Steps:**

| # | Action (exact command, button, or link) | Expected result | If it does not match |
|---|---|---|---|
| 1 | `[ ]` | `[ ]` | `[ ]` |
| 2 | `[ ]` | `[ ]` | `[ ]` |
| 3 | `[ ]` | `[ ]` | `[ ]` |

**How to confirm it worked:** `[ ]`
**How to undo it:** `[ ]`
**Who to tell afterwards:** `[ ]`
**Related cards / sections:** `[ ]`

---

## Appendix B: Glossary

| Word | Simple meaning |
|---|---|
| **AI agent** | An AI that can take actions (run commands, change settings), not only answer questions |
| **Alert** | An automatic message saying something needs attention |
| **API** | A way for programs to talk to each other |
| **Backup** | A saved copy of data you can restore |
| **CI/CD** | Automatic tools that test and deliver code changes |
| **Critical function** | Something the product must never stop doing |
| **Dependency** | Something your product relies on, like a payment provider |
| **Deploy** | Put a new version live |
| **Disaster recovery (DR)** | Plan to get back to normal after a very big failure |
| **Escalate** | Ask someone with more skill or authority to help |
| **Feature switch / flag** | An on/off button for a feature without redeploying |
| **Gate** | A checkpoint you must pass to move forward |
| **Incident** | Unplanned problem that affects (or may affect) customers |
| **Incident commander** | Person leading the response to an incident |
| **Kill switch** | A fast way to stop something immediately |
| **Least access** | Giving people only the access they need |
| **Load test** | Practice run with lots of fake users to see what breaks |
| **Monitoring** | Watching the product's health automatically |
| **On-call** | Person responsible for responding right now |
| **Production / Staging** | Real product / practice copy |
| **Rate limit** | Maximum requests allowed in a time period |
| **Rollback** | Return to the previous working version |
| **RPO** | Recovery Point Objective: how much recent data you can afford to lose |
| **RTO** | Recovery Time Objective: how long you can afford to be down |
| **Runbook** | Step-by-step operating instructions |
| **Secret** | A password, key, or token that must be kept private |
| **Severity (SEV)** | How serious an incident is |
| **SLA / SLO** | A promise / goal about availability and speed |
| **Status page** | A public page showing whether the product is working |
| **Tripwire** | A warning number that tells you to act before trouble |
| **2FA** | Two-step login: password plus a code or device |

---

## Appendix C: Post-Incident Review Template

> **Do this within 5 working days of every SEV-1 and SEV-2.** The goal is to learn, not to blame. Ask "what let this happen?", not "who did this?".

| Field | Your answer |
|---|---|
| Incident title and ID | `[ ]` |
| Severity | `[ ]` |
| Date, start time, end time, total duration | `[ ]` |
| Incident commander and responders | `[ ]` |
| Customers affected (number or %) | `[ ]` |
| Data lost or exposed? | ☐ No ☐ Yes: `[ ]` |
| Money or reputation impact | `[ ]` |

**Summary (3 sentences, plain words):** `[ ]`

**Timeline** (what happened and when):

| Time | Event |
|---|---|
| `[ ]` | Problem started |
| `[ ]` | We noticed (how?) |
| `[ ]` | First action taken |
| `[ ]` | Customers told |
| `[ ]` | Fixed / resolved |

**Root causes** (ask "why?" five times): `[ ]`
**What went well:** `[ ]`
**What went badly or was lucky:** `[ ]`
**Did any AI agent take part? What did it do? Was it within its permission level?** `[ ]`
**Did this runbook help? What was missing or wrong?** `[ ]`

**Action items:**

| Action | Owner | Due date | Done? |
|---|---|---|---|
| `[ ]` | `[ ]` | `[ ]` | ☐ |

**Update the runbook:** ☐ Done on `[date]` (add a row in the change log).

---

## Appendix D: Recommended Reading

These established guides shaped the structure of this template. Use them when you want to go deeper.

- Google, *Site Reliability Engineering* books (incident response, monitoring, postmortems)
- Atlassian Incident Management Handbook (roles, severity levels, communication)
- PagerDuty Incident Response documentation (open-source guide to on-call and response)
- AWS, Google Cloud, and Microsoft Azure Well-Architected Frameworks (reliability, security, cost)
- NIST Cybersecurity Framework and NIST SP 800-61 (security incident handling)
- OWASP guidance (application security)
- NIST AI Risk Management Framework (governing AI systems)
- *Accelerate* / DORA research (deployment and stability measures)

*Verify the current versions of these resources before you rely on them; links and guidance change.*

- Privacy regulators' guidance for GDPR / UK GDPR and the California privacy agency's guidance for CCPA/CPRA
- AICPA SOC 2 resources and ISO/IEC 27001 (security management standards)
- PCI Security Standards Council guidance (payments)

---

## Appendix E: Ready-Made Quick-Fix Cards

> **How to use:** copy a card into Section 9 (Q9.3) or into its own page. Replace every `[ ]` with your real names, links, and commands. Test each card on staging and write the date. **A card is only ready when someone other than the author has followed it successfully.** Cards use the format from Appendix A in short form.

### Card E1: Site is down or not loading

| Field | Your answer |
|---|---|
| **Trigger** | Uptime alert fires, or customers report "cannot open the site" |
| **Severity** | Start as SEV-1 |
| **Owner / backup** | `[ ]` / `[ ]` |
| **Last tested** | `[ ]` |

| # | Action | Expected result |
|---|---|---|
| 1 | Post "Investigating site down" in `[incident channel]`; claim the incident | Team knows you are on it |
| 2 | Check the vendors' status pages: hosting `[link]`, domain/DNS `[link]` | Shows whether the problem is theirs |
| 3 | Check: did we deploy in the last hour? If yes, **roll back now** (Section 7) | Site recovers |
| 4 | Check the hosting dashboard: is the app running? Restart it: `[command/button]` | App shows running |
| 5 | Check domain name and HTTPS certificate not expired: `[link]` | Both valid |
| 6 | Check the database is reachable and not full: `[link]` | Database healthy |
| 7 | Update the status page; use the "Investigating" template (Q11.3) | Customers informed |
| 8 | Still down after 15 minutes: escalate (Q2.2) | Next person engaged |

**Verify fixed:** run the smoke test (Q19.2). **Afterwards:** Post-Incident Review (Appendix C).

### Card E2: Login or sign-up is failing

| Field | Your answer |
|---|---|
| **Trigger** | Login-check fails, spike in login errors, or "I can't log in" tickets |
| **Severity** | SEV-1 if most users, SEV-2 if some |

| # | Action | Expected result |
|---|---|---|
| 1 | Try logging in yourself with a test account | Confirms the problem |
| 2 | Check the login provider's status page `[link]` | Their outage, or ours |
| 3 | Check for a recent deploy or setting change; roll back if found | Login works |
| 4 | Check the email/SMS provider (codes and password-reset emails) `[link]` | Messages are being sent |
| 5 | Check for expired keys or certificates (Q5.4, Q18.5) | None expired |
| 6 | If a login-provider outage: show a clear message and update the status page | Customers informed |
| 7 | Watch for unusual login attempts (possible attack). If suspected, follow Q5.5 | Security contact informed |

### Card E3: Payments are failing

| Field | Your answer |
|---|---|
| **Trigger** | Payment errors rise, payment provider alert, "I was not able to pay" tickets |
| **Severity** | SEV-1 (money path) |

| # | Action | Expected result |
|---|---|---|
| 1 | Make a test payment | Confirms the problem |
| 2 | Check the payment provider's status page and dashboard `[link]` | Their issue, or ours |
| 3 | Check for a recent deploy or key change; roll back if found | Payments work |
| 4 | Check that the payment keys in production are the **live** keys and not expired or wrong | Keys valid |
| 5 | If the provider is down: show "Payments are temporarily unavailable. Please try again in 30 minutes." and queue or hold orders if possible | No lost orders |
| 6 | **Do not** change prices, refund in bulk, or edit payment records without Owner approval 👤 (L3, Section 13) | Money safe |
| 7 | After recovery: list the customers who were affected and contact them; check for double charges | Customers made whole |

### Card E4: Database is full, slow, or not reachable

| Field | Your answer |
|---|---|
| **Trigger** | Slow-page alert, database storage above `[ ]`%, connection errors |
| **Severity** | SEV-1 if the product is down; SEV-2 if only slow |

| # | Action | Expected result |
|---|---|---|
| 1 | Check the database dashboard: storage, connections, CPU `[link]` | Find which is high |
| 2 | **Take a backup/snapshot now** if possible | Safe copy exists |
| 3 | If storage is nearly full: increase storage `[steps]` (approve spending per Q2.4); do not delete data to "make room" | Space available |
| 4 | If too many connections or very busy: pause heavy background jobs; restart the app to reset connections; consider capacity increase (Q12.6) | Load drops |
| 5 | If a recent deploy started it: roll back (Section 7) | Normal speed returns |
| 6 | Record the cause and add or adjust the tripwire (Q4.6) | Warned earlier next time |

### Card E5: A third-party service we depend on is down

| Field | Your answer |
|---|---|
| **Trigger** | Vendor status page shows an incident, or our errors point to their API |
| **Severity** | Based on the critical function that is affected (Q1.2) |

| # | Action | Expected result |
|---|---|---|
| 1 | Confirm it is them: check their status page and test their API `[link]` | Cause confirmed |
| 2 | Look up the workaround in Q3.4 and apply it | Customers have a fallback |
| 3 | Turn off or hide the affected feature if needed (feature switch) | No confusing errors |
| 4 | Tell customers (Section 11) and subscribe to the vendor's updates | Informed |
| 5 | Open a support ticket with the vendor if our plan allows (Q20.5) | Ticket recorded |
| 6 | When they recover: check queued work, failed messages, and missed payments; retry safely | Data consistent |

### Card E6: AI provider is down, slow, or giving bad answers

| Field | Your answer |
|---|---|
| **Trigger** | AI errors or slow responses; bad-answer reports; unusual cost spike |
| **Severity** | SEV-2 normally; SEV-1 if answers are harmful or private data may be exposed |

| # | Action | Expected result |
|---|---|---|
| 1 | Check the AI provider's status page `[link]` | Their issue, or ours |
| 2 | Check recent changes to prompts, model version, or agent instructions (Q13.7); **roll back the change** | Quality or speed returns |
| 3 | If answers are harmful or wrong: switch the feature to the safe fallback message or human fallback (Q13.8), with approval 👤 | Harm stopped |
| 4 | If an agent behaved unexpectedly: press the kill switch (Q13.5) | Agents stopped |
| 5 | If cost spiked: check the spending cap and rate limits (Q12.3) and lower them | Bills controlled |
| 6 | If private data may have appeared in an answer: treat as a security incident (Q5.5, Q21.5) | Security contact and Owner informed |
| 7 | Add the bad example to the golden question set (Q19.7) | Cannot quietly return |

### Card E7: Suspected security breach or leaked key

| # | Action | Expected result |
|---|---|---|
| 1 | Do not delete evidence; write down time and what you saw | Record exists |
| 2 | Disable the exposed key, account, or access immediately 👤 | Leak stopped |
| 3 | Rotate affected secrets (Q5.4) | New secrets in use |
| 4 | Tell the Security contact and Owner now | Informed |
| 5 | Check logs for what was accessed | Scope known |
| 6 | Follow Q5.5 and Q21.5 for customer and legal notice; talk to the lawyer | Duties met |
| 7 | Post-Incident Review (Appendix C) | Lessons recorded |
