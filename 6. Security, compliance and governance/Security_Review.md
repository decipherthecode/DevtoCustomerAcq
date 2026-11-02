# How to Fill This Document

> **Template version:** 1.1.0 | **Last updated:** 2026-10-17 | **Covers:** Idea → Build → Launch → first 500 customers
> **Time needed:** about 2 hours for the first pass, then 10–15 minutes per phase gate.
> **Golden rule:** If you are not sure, **do not guess**. Write `UNKNOWN` and ask the person named in Part 3.

## What is this document?

This is a **safety checklist for your product**. Think of building a house: before people move in, someone checks that the doors lock, the wiring is safe, and there is a fire exit. This document does that for software, and it covers products that are built with AI or contain AI.

You use **one copy of this file per project**. It follows the project from the first idea until the 500th customer.

## Step-by-step: how to fill it

1. **Copy the file.** Never edit the master template. Save your copy as `Security_Review_[ProjectName].md` inside your project's `Security, compliance and governance` folder.
2. **Replace everything in double brackets.** Anything like `[[Project Name]]` is a blank. Delete the brackets and type your answer.
3. **Fill the document in order.** Parts 1 and 2 come first because they decide which checks apply to you.
4. **Answer every row.** Use only the five status words in the table below. Do not invent new ones.
5. **Add proof ("evidence").** Paste a link, a ticket number, or a file name. *If there is no proof, it did not happen.*
6. **Never paste secrets here.** No passwords, API keys, tokens, or real customer data. Write *where* a secret is stored, never the secret itself.
7. **Stop at each Gate.** A Gate is a checkpoint. You may not start the next phase until the Gate decision box is signed.
8. **Update it as you go.** This is a living document. Add a line to the Change Log (Appendix E) whenever you make a big change.

## The five status words (use only these)

| Status | Meaning | What you must write in "Evidence / Notes" |
|---|---|---|
| `TODO` | Not done yet | Who will do it and by when |
| `PASS` | Done and proven | Link or file name that proves it |
| `FAIL` | Checked, and it is not good enough | Link to the issue in the Findings Register (Part 7) |
| `N/A` | Does not apply to this project | The reason, in one sentence ("We have no payments") |
| `ACCEPTED` | We know the risk and choose to live with it | Entry number in the Risk Acceptance Log (Part 7) |

## What does "Tier" mean in the tables?

In Part 2 you answer a short quiz. It gives your project a **Risk Tier (1, 2, or 3)**. Every check has a **Tier** column:

| Tier column says | Who must do it |
|---|---|
| `1` | **Everyone** (Tier 1, 2 and 3 projects) |
| `2` | Tier 2 and Tier 3 projects |
| `3` | Tier 3 projects only |
| `AI` | Only if your product or your build process uses AI (see Part 2 and Part 4.5) |

Other tiers' checks may be marked `N/A` with the reason "Not required for our tier". Doing more than your tier requires is always welcome.

## How serious is a problem? (Severity)

| Severity | Plain meaning | Example | Must be fixed |
|---|---|---|---|
| **Critical** | Someone could steal data or take over the product right now | Anyone can open another customer's data | **Immediately.** It blocks every Gate and can never be accepted. |
| **High** | Serious weakness that is likely to be abused | Admin page has no second login step | Before the next Gate. **Cannot be accepted before launch.** |
| **Medium** | Real weakness, harder to abuse | Error messages show too much detail | Within 30 days |
| **Low** | Small issue or good-practice gap | Missing security header on a static page | Within 90 days or backlog |

## Who fills what?

| Part | Easiest for | Ask for help from |
|---|---|---|
| Parts 1, 2, 3 (about the project) | Product / project owner | Anyone on the team |
| Part 4 (inventories) | Engineering + product together | Security reviewer |
| Gates 1–6 (checklists) | The person who owns each row (the **Owner** column) | Security reviewer |
| Part 5 (deep dives) | Engineering, privacy/legal contact | Security reviewer |
| Parts 6–8 (incidents, findings, sign-off) | Security reviewer + project owner | Executive sponsor |

## When you are stuck (3-question rescue)

1. **Does this thing touch people's information, money, or login?** If yes, it matters. Do the check.
2. **Could a stranger on the internet reach it?** If yes, treat it as Tier 2 or higher.
3. **Still not sure?** Write `UNKNOWN` in Notes, tag the Security reviewer, and move on. Never write `PASS` to make a row go green.

## Words you will see (short version; full list in Appendix B)

- **Secret:** a password, key, or token that proves who you are to a computer.
- **MFA (multi-factor login):** logging in with a password *plus* a second proof, such as a phone code.
- **Least privilege:** giving each person or program only the keys it needs, and no more.
- **Vulnerability:** a weakness a bad person could use.
- **AI agent:** an AI that can *do* things (run commands, send emails, change files), not just talk.

---

# Security Review: [[Project Name]]

## Part 1: Document Control

| Field | Answer |
|---|---|
| Project name | [[Project Name]] |
| One-sentence description (what does it do, for whom?) | [[e.g., "An app that lets dentists book patients using an AI assistant."]] |
| Project owner (name, role) | [[Name]] |
| Security reviewer (name, role) | [[Name]] |
| Review start date | [[YYYY-MM-DD]] |
| Target launch date | [[YYYY-MM-DD]] |
| Current phase | [[Plan / Build / Test / Pre-launch / Launch / Customers 1–500]] |
| Repository link | [[URL]] |
| Ticket tracker link | [[URL]] |
| Where evidence is stored | [[Folder or link, access-controlled]] |
| Template version used | 1.1.0 |
| This document's status | [[Draft / In review / Approved for next Gate]] |

### Project snapshot (answer in plain words)

| Question | Answer |
|---|---|
| Who are the users? (customers, staff, kids, businesses?) | [[ ]] |
| Which countries or regions are the users in? | [[ ]] |
| Is the product a website, mobile app, API, or desktop app? | [[ ]] |
| Does it take payments? (yes/no, and which provider) | [[ ]] |
| Does it store login accounts? (yes/no) | [[ ]] |
| Does it contain AI that talks to users or takes actions? (yes/no) | [[ ]] |
| Does AI help build it (AI-written code, AI agents in the dev process)? (yes/no) | [[ ]] |
| Where will it run? (cloud name and region) | [[ ]] |
| Which extra modules apply? Tick all: 5E Payments / 5F Mobile app / 5G Cloud and infrastructure / 5H Regulated industries | [[ ]] |
| Does it handle health, school, children's, financial, or government-customer data? (Triggers module 5H) | [[ ]] |
| What is the worst thing that could go wrong? (one sentence) | [[ ]] |

---

## Part 2: Risk Tier Quiz (decides which checks you must do)

Answer each question **Yes** or **No**. Each **Yes** is 1 point, except the "auto-Tier 3" rows.

| # | Question | Yes / No | Points |
|---|---|---|---|
| Q1 | Will strangers on the internet be able to reach it? | [[ ]] | |
| Q2 | Does it store names, emails, phone numbers, or addresses? | [[ ]] | |
| Q3 | Does it store payment info, ID numbers, or government IDs? (**Yes = auto-Tier 3**) | [[ ]] | |
| Q4 | Does it store health, financial, biometric, or children's data? (**Yes = auto-Tier 3**) | [[ ]] | |
| Q5 | Do customers log in? | [[ ]] | |
| Q6 | Does one customer's data sit next to another customer's data (multi-tenant)? | [[ ]] | |
| Q7 | Does it use AI that can read private data or take actions for users? | [[ ]] | |
| Q8 | Does it connect to other companies' systems or APIs? | [[ ]] | |
| Q9 | Would an hour of downtime cost real money or hurt people? | [[ ]] | |
| Q10 | Do you expect big customers (companies) who will send security questionnaires? | [[ ]] | |

**Total points:** [[ ]]

| Result | Tier |
|---|---|
| 0–3 points and no auto-Tier 3 | **Tier 1** (basic) |
| 4–7 points and no auto-Tier 3 | **Tier 2** (standard) |
| 8–10 points, or any auto-Tier 3 answer | **Tier 3** (strict) |

**Our Risk Tier:** [[1 / 2 / 3]]
**Our OWASP ASVS target level:** [[Tier 1 → ASVS Level 1, Tier 2 → Level 2, Tier 3 → Level 3]]
**Do we use AI in the product or the build process?** [[Yes / No]] (If Yes, every `AI` row is required.)
**Re-take this quiz** at the start of each Gate and at customers 50, 100, 250 and 500. Tiers can go up as you grow.

---

## Part 3: People and Responsibilities

| Role | Name | Contact | What they decide |
|---|---|---|---|
| Project owner | [[ ]] | [[ ]] | Scope, schedule, and who fixes what |
| Security reviewer | [[ ]] | [[ ]] | Whether a check really passes |
| Engineering lead | [[ ]] | [[ ]] | How things are built and fixed |
| Privacy / legal contact | [[ ]] | [[ ]] | Laws, contracts, customer data promises |
| Executive sponsor (risk acceptor) | [[ ]] | [[ ]] | Whether a High risk found **after** launch may be accepted (Critical risks can never be accepted) |
| On-call person for incidents | [[ ]] | [[ ]] | First responder when something breaks |
| Backup for each role above | [[ ]] | [[ ]] | Covers when someone is away |

> **Rule:** The person who builds a thing may not be the only person who approves it. Security reviews need a second set of eyes.

---

## Part 4: Inventories (know what you have)

You cannot protect what you have not listed. Fill these tables before Gate 1.

### 4.1 Data inventory

**Labels:** `Public` (anyone may see), `Internal` (team only), `Confidential` (customers' private info), `Restricted` (would cause serious harm if leaked: passwords, payments, health, IDs, children's data).

| Data type | Label | Why we need it | Where stored | Who can access | How long we keep it | Encrypted? |
|---|---|---|---|---|---|---|
| [[e.g., customer email]] | [[Confidential]] | [[Login and receipts]] | [[Database X, EU region]] | [[Support + app]] | [[Until account deleted + 30 days]] | [[Yes]] |
| [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] |
| [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] |

### 4.2 Systems, vendors, and services inventory

Include cloud providers, databases, email tools, analytics, payment providers, monitoring, and AI model providers.

| Service / vendor | What we use it for | Data it can see | Security proof checked (SOC 2 report, ISO 27001 certificate, privacy terms) | Contract / DPA signed? | Owner |
|---|---|---|---|---|---|
| [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[Yes / No / N/A]] | [[ ]] |
| [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] |

### 4.3 Roles and permissions (who may do what)

| Role (e.g., visitor, customer, admin, support, AI agent) | What they can see | What they can change | What they must never do |
|---|---|---|---|
| [[ ]] | [[ ]] | [[ ]] | [[ ]] |
| [[ ]] | [[ ]] | [[ ]] | [[ ]] |

### 4.4 Secrets inventory (names and locations only, **never the values**)

| Secret name | What it unlocks | Where it is stored | Who can read it | Last rotated | Rotation plan |
|---|---|---|---|---|---|
| [[e.g., PAYMENT_API_KEY]] | [[Payment provider]] | [[Secrets manager name]] | [[Backend service only]] | [[YYYY-MM-DD]] | [[Every 90 days]] |

### 4.5 AI inventory (fill even if you think the answer is "none")

**A. AI used to BUILD the product**

| AI tool (coding assistant, agent, chatbot) | What it may do | What it may NOT do | Can it reach production or real customer data? | Who approved it |
|---|---|---|---|---|
| [[ ]] | [[ ]] | [[ ]] | [[Yes / No]] | [[ ]] |

**B. AI INSIDE the product**

| AI feature | Model and provider | Data it sees | Actions it can take | Human approval needed for | Provider keeps or trains on our data? |
|---|---|---|---|---|---|
| [[e.g., support chatbot]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[Yes / No / Unknown]] |

**C. Tools and connections given to AI (plugins, MCP servers, APIs, file access)**

| Tool / connection | What it can do | Read-only or can change things? | Who vetted it | Date vetted |
|---|---|---|---|---|
| [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] |

### 4.6 Simple threat model ("what could go wrong?")

| What are we protecting? (asset) | Who might attack or misuse it? | How could they do it? | What would happen? | What stops them? (control) | Check ID |
|---|---|---|---|---|---|
| [[Customer accounts]] | [[Stranger, ex-employee, customer A spying on B]] | [[Guess passwords; change an ID in a web address]] | [[Data leak, account takeover]] | [[MFA, permission checks]] | [[G2-14]] |
| [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] |
| [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] |

> **Prompt to get unstuck:** "What if a smart, angry stranger had one hour and my product's web address?" And for AI: "What if someone typed instructions into the chatbot that tell it to ignore its rules?"

---

# Phase Gates

There are **six gates**. Each gate has a checklist and a decision box. Columns:

`ID | Check (answer yes/no) | Tier | Status | Evidence / Notes | Owner | Maps to`

"Maps to" shows the standard behind the check (OWASP Top 10:2025 = `A01`–`A10`, OWASP LLM Top 10 = `LLM01`–`LLM10`, privacy laws = `PRIV`, SOC 2 = `SOC2`, NIST AI RMF = `NIST`, ASVS = `ASVS`). You do not need to read the standards. The check is written in plain words.

---

## Gate 1: Plan and Design

**Goal:** Decide what you are building and what could go wrong, before any code exists.

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G1-01 | Is the project described in plain words (Part 1 complete)? | 1 | TODO | | | SOC2 |
| G1-02 | Is the Risk Tier calculated (Part 2)? | 1 | TODO | | | NIST Map |
| G1-03 | Is there a named owner and reviewer (Part 3)? | 1 | TODO | | | SOC2 |
| G1-04 | Is every kind of data listed and labeled (4.1)? | 1 | TODO | | | PRIV |
| G1-05 | Do we collect only the data we truly need? | 1 | TODO | | | PRIV |
| G1-06 | Is every outside service and vendor listed (4.2)? | 1 | TODO | | | A03 |
| G1-07 | Are roles and permissions designed on paper (4.3)? | 1 | TODO | | | A01 |
| G1-08 | Is a simple threat model written (4.6)? | 1 | TODO | | | A06 |
| G1-09 | Is the ASVS target level chosen (Part 2)? | 1 | TODO | | | ASVS |
| G1-10 | Have we listed which privacy laws apply (GDPR, CCPA/CPRA, others) based on where users live? | 1 | TODO | | | PRIV |
| G1-11 | Is the data storage region decided and allowed by law and contracts? | 1 | TODO | | | PRIV |
| G1-12 | Do we have time and budget for fixing security issues in the plan? | 1 | TODO | | | NIST Govern |
| G1-13 | AI: Is the AI inventory complete (4.5 A, B, C)? | AI | TODO | | | NIST Map |
| G1-14 | AI: Have we written what AI may and may not do, and what needs a human to approve? | AI | TODO | | | LLM06 |
| G1-15 | Did someone *other than the builder* review the design? | 2 | TODO | | | A06 |
| G1-16 | Did we check each vendor that touches Confidential or Restricted data (security report, certificate, or privacy terms)? | 2 | TODO | | | A03, SOC2 |
| G1-17 | Did we write "abuse stories" (how a bad user would misuse each feature)? | 2 | TODO | | | A06 |
| G1-18 | Did we decide whether SOC 2 or ISO 27001 is a goal, and by when? | 2 | TODO | | | SOC2 |
| G1-19 | Was a formal threat-modeling workshop held with an outside or independent expert? | 3 | TODO | | | A06 |
| G1-20 | Is a Data Protection Impact Assessment (DPIA) needed, and if so, started? | 3 | TODO | | | PRIV |
| G1-21 | Have we ticked which extra modules (5E Payments, 5F Mobile, 5G Cloud, 5H Regulated) apply in Part 1? | 1 | TODO | | | NIST Map |

### Gate 1 decision

- [ ] All required rows are `PASS`, `N/A` (with reason), or `ACCEPTED`.
- [ ] No open Critical findings.
- [ ] Reviewer signed below.

| Decision | Name | Date | Notes |
|---|---|---|---|
| `GO` / `GO WITH CONDITIONS` / `NO-GO` | [[ ]] | [[YYYY-MM-DD]] | [[Conditions, if any]] |

---

## Gate 2: Build

**Goal:** Build it safely from day one. Fixing security later costs much more.

### 2A. Code and secrets

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G2-01 | Is the code in a **private** repository where every member uses MFA? | 1 | TODO | | | A07, SOC2 |
| G2-02 | Is the main branch protected (no direct pushes, at least one review required)? | 1 | TODO | | | A08, SOC2 |
| G2-03 | Is automatic secret scanning turned on for the repo? | 1 | TODO | | | A02 |
| G2-04 | Are all secrets stored in a secrets manager (not in code, chat, or this doc)? | 1 | TODO | | | A02, A04 |
| G2-05 | Do dev, test, and production use **different** secrets? | 1 | TODO | | | A02 |
| G2-06 | Is there a written plan for what to do if a secret leaks (rotate it, check logs)? | 1 | TODO | | | A02 |
| G2-07 | Are dependencies scanned for known problems, with lockfiles committed? | 1 | TODO | | | A03 |
| G2-08 | Is every new package checked to be real and trusted before use? (AI tools sometimes invent package names that attackers then register.) | 1 | TODO | | | A03, LLM03 |
| G2-09 | Does code analysis (SAST) run on every pull request? | 2 | TODO | | | ASVS |
| G2-10 | Is the build pipeline locked down (limited permissions, protected build secrets, only trusted build steps)? | 2 | TODO | | | A03, A08 |
| G2-11 | Is a software bill of materials (SBOM, a list of all parts inside) produced for every release? | 3 | TODO | | | A03 |
| G2-12 | Are release builds signed or otherwise verifiable? | 3 | TODO | | | A08 |

### 2B. Login, permissions, and customer separation

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G2-13 | Does the **server** check permission on every request (not just hiding buttons)? | 1 | TODO | | | A01 |
| G2-14 | Is each customer blocked from seeing other customers' data? (Test: change an ID in the address bar.) | 1 | TODO | | | A01 |
| G2-15 | Do we use a trusted login provider or modern password hashing (never plain-text passwords)? | 1 | TODO | | | A07 |
| G2-16 | Is MFA available to customers, and **required** for admins and staff? | 1 | TODO | | | A07 |
| G2-17 | Do sessions and tokens expire, and are cookies set `Secure` and `HttpOnly`? | 1 | TODO | | | A07 |
| G2-18 | Are login attempts rate-limited and account lockout or slow-down in place? | 1 | TODO | | | A07 |
| G2-19 | Do admin functions have extra protection and a separate permission? | 2 | TODO | | | A01 |
| G2-20 | Are "forgot password" and email-change flows safe against takeover? | 2 | TODO | | | A07 |

### 2C. Data handling

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G2-21 | Is all user input checked, and are database queries parameterized (no building queries from text)? | 1 | TODO | | | A05 |
| G2-22 | Is output safe against script injection (output encoding, Content Security Policy)? | 1 | TODO | | | A05 |
| G2-23 | Is data encrypted in transit (TLS 1.2 or newer) and at rest? | 1 | TODO | | | A04 |
| G2-24 | Are personal data and secrets kept **out of logs and error messages**? | 1 | TODO | | | A09, PRIV |
| G2-25 | Does the app fail safely (errors never expose internals or leave things open)? | 1 | TODO | | | A10 |
| G2-26 | Are security events logged (logins, failed logins, permission changes, admin actions, data exports)? | 1 | TODO | | | A09, SOC2 |
| G2-27 | Is rate limiting on every public endpoint? | 1 | TODO | | | A06 |
| G2-28 | Are automatic backups set up, encrypted, and stored separately? | 1 | TODO | | | SOC2 |
| G2-29 | Are file uploads limited by type and size, scanned, and stored outside the web root? | 2 | TODO | | | A05 |
| G2-30 | Are encryption keys managed (rotated, access-limited, never hard-coded)? | 2 | TODO | | | A04 |
| G2-31 | Is the most sensitive data additionally protected (field-level encryption or tokenization)? | 3 | TODO | | | A04 |

### 2D. Building with AI (coding assistants and agents)

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G2-32 | Does a human read and approve **every** AI-written change before it is merged? | AI | TODO | | | A06, NIST Manage |
| G2-33 | Do AI coding tools have least privilege (limited folders, no production passwords, risky commands need approval, runs in a sandbox)? | AI | TODO | | | LLM06 |
| G2-34 | Is it forbidden to paste secrets or real customer data into AI tools, unless the tool is approved for that data? | AI | TODO | | | LLM02, PRIV |
| G2-35 | Is there an approved list of AI tools, plugins, and connectors (MCP servers), each vetted before use? | AI | TODO | | | LLM03 |
| G2-36 | Are the instruction files that steer AI tools (rules, memory, config) stored in the repo and reviewed like code? | AI | TODO | | | LLM01 |
| G2-37 | Is AI-written code for logins, payments, encryption, or permissions reviewed by a **second** human with security knowledge? | AI | TODO | | | A01, A04, A07 |
| G2-38 | Are AI agents' actions logged so we can see what they changed? | AI | TODO | | | A09, LLM06 |
| G2-39 | Do we run the same tests, scans, and reviews on AI-written code as on human-written code? | AI | TODO | | | ASVS |

### Gate 2 decision

- [ ] All required rows are `PASS`, `N/A` (with reason), or `ACCEPTED`.
- [ ] No open Critical or High findings from Build.
- [ ] Reviewer signed below.

| Decision | Name | Date | Notes |
|---|---|---|---|
| `GO` / `GO WITH CONDITIONS` / `NO-GO` | [[ ]] | [[YYYY-MM-DD]] | [[ ]] |

---

## Gate 3: Test and Verify

**Goal:** Try to break your own product before a real attacker does.

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G3-01 | Do automated tests include "this should be **denied**" tests (wrong user, wrong role)? | 1 | TODO | | | A01 |
| G3-02 | Was a vulnerability scan of the running staging app done? | 1 | TODO | | | ASVS |
| G3-03 | Was the OWASP Top 10:2025 walkthrough (Part 5A) completed? | 1 | TODO | | | A01–A10 |
| G3-04 | Was a manual security review done by someone who did not write the code? | 1 | TODO | | | ASVS |
| G3-05 | Are **all** Critical and High findings fixed **and retested**? | 1 | TODO | | | SOC2 |
| G3-06 | Does test data contain **no** real customer data? | 1 | TODO | | | PRIV |
| G3-07 | Was a backup **restore** tested (not just backup creation)? | 1 | TODO | | | SOC2 |
| G3-08 | Do data export and data deletion for a user work end to end? | 1 | TODO | | | PRIV |
| G3-09 | AI: Were prompt-injection tests run (direct and hidden-in-documents)? | AI | TODO | | | LLM01 |
| G3-10 | AI: Were tests run to try to make the AI reveal private data or its hidden instructions? | AI | TODO | | | LLM02, LLM07 |
| G3-11 | AI: Were AI features tested to make sure AI output cannot run commands or code without checks? | AI | TODO | | | LLM05 |
| G3-12 | AI: Does an agent test prove it cannot go beyond its allowed tools and data? | AI | TODO | | | LLM06 |
| G3-13 | AI: Were wrong or made-up answers tested, and do we warn users where it matters? | AI | TODO | | | LLM09 |
| G3-14 | AI: Do spending, token, and request limits stop runaway use? | AI | TODO | | | LLM10 |
| G3-15 | Are infrastructure-as-code and container images scanned? | 2 | TODO | | | A02 |
| G3-16 | Was an abuse and load test done (many requests, many logins, many uploads)? | 2 | TODO | | | A06 |
| G3-17 | Is the ASVS verification record filled in for our target level? | 2 | TODO | | | ASVS |
| G3-18 | Was an **independent penetration test** done? (Required for Tier 3 before launch. Strongly advised for Tier 2 by customer 100.) | 3 | TODO | | | ASVS, SOC2 |
| G3-19 | AI: Was an AI red-team exercise (people deliberately trying to trick the AI) performed? | AI + 3 | TODO | | | LLM01–LLM10 |

### Gate 3 decision

- [ ] All required rows are `PASS`, `N/A` (with reason), or `ACCEPTED`.
- [ ] Zero open Critical or High findings. No exceptions.
- [ ] Reviewer signed below.

| Decision | Name | Date | Notes |
|---|---|---|---|
| `GO` / `GO WITH CONDITIONS` / `NO-GO` | [[ ]] | [[YYYY-MM-DD]] | [[ ]] |

---

## Gate 4: Pre-Launch

**Goal:** Make sure production is locked down, people know what to do if something goes wrong, and the legal basics are in place.

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G4-01 | Is production hardened (no default passwords, debug mode off, unused ports and features closed)? | 1 | TODO | | | A02 |
| G4-02 | Do all admins use named accounts with MFA (no shared logins)? | 1 | TODO | | | A07, SOC2 |
| G4-03 | Was every secret used in development replaced before launch? | 1 | TODO | | | A02 |
| G4-04 | Are monitoring and alerts live, and does a named person get paged? | 1 | TODO | | | A09, SOC2 |
| G4-05 | Is the Incident Response Plan (Part 6) written, with the contact list filled in? | 1 | TODO | | | SOC2 |
| G4-06 | Are privacy policy and terms of service published, and are cookie/consent rules followed? | 1 | TODO | | | PRIV |
| G4-07 | Are data-retention and deletion schedules set and built into the product? | 1 | TODO | | | PRIV |
| G4-08 | Is there a way to handle customer requests to see, fix, or delete their data, with a named owner and deadline tracking? | 1 | TODO | | | PRIV |
| G4-09 | Are data-processing agreements signed with vendors that handle personal data? | 1 | TODO | | | PRIV |
| G4-10 | Is there a public way to report security problems (a security@ email, `security.txt`, short disclosure policy)? | 1 | TODO | | | SOC2 |
| G4-11 | Is a rollback plan written and tested? | 1 | TODO | | | SOC2 |
| G4-12 | If we take payments: does a PCI-compliant provider handle card data, and do we store **no** card numbers? (Details: Part 5E) | 1 | TODO | | | PRIV |
| G4-13 | Do we know how to remove access when someone leaves (offboarding checklist)? | 1 | TODO | | | SOC2 |
| G4-14 | Are cost and usage alerts set for cloud and AI bills? | 1 | TODO | | | LLM10 |
| G4-15 | AI: Is there a **kill switch** that turns off AI features or agents within minutes? | AI | TODO | | | LLM06, NIST Manage |
| G4-16 | AI: Do users see clear notice that they are talking to AI, and what it does with their data? | AI | TODO | | | NIST Govern, PRIV |
| G4-17 | AI: Is the model version pinned, with a plan for reviewing changes when the provider updates it? | AI | TODO | | | LLM03, NIST Manage |
| G4-18 | Is every open finding in the Findings Register (Part 7) with an owner and due date? | 1 | TODO | | | SOC2 |
| G4-19 | Is there protection against floods of traffic (WAF or DDoS protection)? | 2 | TODO | | | A06 |
| G4-20 | Was an incident drill (tabletop exercise: "pretend it happened") held? | 2 | TODO | | | SOC2 |
| G4-21 | Did privacy/legal sign off? | 2 | TODO | | | PRIV |
| G4-22 | Are security logs kept in a place admins cannot edit, for a set time? | 3 | TODO | | | A09, SOC2 |
| G4-23 | Is a DPIA completed and filed (if needed per G1-20)? | 3 | TODO | | | PRIV |
| G4-24 | Is every applicable extra module (5E–5H) finished with `PASS` or `N/A` plus reason? | 1 | TODO | | | SOC2 |

### Gate 4 decision (launch approval)

- [ ] All required rows are `PASS`, `N/A` (with reason), or `ACCEPTED`.
- [ ] Zero open Critical or High findings. No exceptions.
- [ ] Every applicable extra module (5E–5H) is complete (`PASS` or `N/A` with reason).
- [ ] Reviewer and Executive sponsor signed below.

| Decision | Name | Date | Notes |
|---|---|---|---|
| `GO` / `GO WITH CONDITIONS` / `NO-GO` | [[ ]] | [[YYYY-MM-DD]] | [[ ]] |

---

## Gate 5: Launch (Day 0 to Day 7)

**Goal:** Launch carefully and watch closely during the first week.

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G5-01 | Is the launch **staged** (invite-only or small group first, then wider)? | 1 | TODO | | | NIST Manage |
| G5-02 | Is a named person watching the dashboards and alerts during the launch window? | 1 | TODO | | | A09 |
| G5-03 | Was a test alert fired in production and received by the on-call person? | 1 | TODO | | | SOC2 |
| G5-04 | Is support trained to **verify identity** before changing accounts, and to **never ask for passwords**? | 1 | TODO | | | A07 |
| G5-05 | Are changes frozen during launch week, except through the emergency process? | 1 | TODO | | | A08 |
| G5-06 | Are logs reviewed **daily** for week 1 (failed logins, odd traffic, errors, odd AI behavior)? | 1 | TODO | | | A09 |
| G5-07 | Did we tune rate limits and alert thresholds using real traffic? | 1 | TODO | | | A06 |
| G5-08 | Did we confirm that backups ran and certificates auto-renew? | 1 | TODO | | | SOC2 |
| G5-09 | AI: Are AI conversations and actions sampled and reviewed by a human during week 1? | AI | TODO | | | LLM09, NIST Measure |
| G5-10 | Is a public security/trust page live (what we protect, how to report issues, list of vendors)? | 2 | TODO | | | SOC2 |
| G5-11 | Did we hold a Day-7 review (what we saw, what we fixed, what we will change)? | 2 | TODO | | | NIST Manage |

### Gate 5 decision (to open to everyone)

| Decision | Name | Date | Notes |
|---|---|---|---|
| `GO` / `GO WITH CONDITIONS` / `NO-GO` | [[ ]] | [[YYYY-MM-DD]] | [[ ]] |

---

## Gate 6: Customers 1 to 500

**Goal:** Stay safe while you grow. Each step has its own mini-checklist. **Re-take the Part 2 quiz at every step.**

Customer count at last update: [[ ]]  |  Date: [[YYYY-MM-DD]]

### 6A. Customers 1 to 10

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G6-01 | Using real accounts, did we confirm customers cannot see each other's data? | 1 | TODO | | | A01 |
| G6-02 | Did we read logs by hand for each of the first 10 sign-ups to spot strange behavior? | 1 | TODO | | | A09 |
| G6-03 | Did we successfully delete one real test account and all its data end to end? | 1 | TODO | | | PRIV |
| G6-04 | Do we have **one** official support channel, and do customers know we never ask for passwords? | 1 | TODO | | | A07 |
| G6-05 | AI: Did we read the first real AI conversations for leaks, surprises, or misuse? | AI | TODO | | | LLM02, LLM09 |

### 6B. Customers 11 to 50

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G6-06 | Did we do our first **access review** (who has access to what, remove what is not needed)? | 1 | TODO | | | SOC2 |
| G6-07 | Is a monthly dependency-update routine running? | 1 | TODO | | | A03 |
| G6-08 | Did we start a "security questions" answer bank for customers' questionnaires? | 2 | TODO | | | SOC2 |
| G6-09 | Did we review the top alerts and tune out the noise without silencing real problems? | 1 | TODO | | | A09 |
| G6-10 | Did any vendor change terms, owners, or location? Did we re-check? | 1 | TODO | | | A03, PRIV |
| G6-11 | Did we answer every customer privacy request within the legal time limit? (GDPR: one month. CCPA/CPRA: 45 days.) | 1 | TODO | | | PRIV |

### 6C. Customers 51 to 100

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G6-12 | Was an independent penetration test done by customer 100 (Tier 2) or already done (Tier 3)? | 2 | TODO | | | ASVS |
| G6-13 | Did we run an incident drill using a real scenario from our own logs or alerts? | 2 | TODO | | | SOC2 |
| G6-14 | Did we look for fraud, spam, or abuse patterns and add controls? | 1 | TODO | | | A06 |
| G6-15 | AI: Did we review all AI-related incidents, complaints, and odd outputs and add tests for each? | AI | TODO | | | NIST Measure |
| G6-16 | Did we re-take the Part 2 quiz and update the Tier? | 1 | TODO | | | NIST Map |

### 6D. Customers 101 to 250

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G6-17 | Did we rotate important secrets and keys on schedule? | 1 | TODO | | | A02, A04 |
| G6-18 | Did we test disaster recovery (rebuild from backups in a clean environment)? | 2 | TODO | | | SOC2 |
| G6-19 | Is the list of vendors that handle customer data (sub-processors) published and kept current? | 2 | TODO | | | PRIV |
| G6-20 | Did we run a SOC 2 / ISO 27001 gap assessment, if big customers are asking? | 2 | TODO | | | SOC2 |
| G6-21 | Are reports from outside researchers triaged, answered, and tracked? | 1 | TODO | | | SOC2 |
| G6-22 | Did we re-check cost limits and abuse limits at current traffic? | 1 | TODO | | | LLM10 |

### 6E. Customers 251 to 500

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G6-23 | Did we repeat the **whole** review: this document, threat model (4.6), and inventories (Part 4)? | 1 | TODO | | | NIST Govern |
| G6-24 | Do we keep an "evidence folder" with proof for every PASS (screenshots, tickets, reports)? | 2 | TODO | | | SOC2 |
| G6-25 | Did we decide whether to move to the next level (ASVS Level 3, SOC 2 Type I or II, ISO 27001)? | 2 | TODO | | | SOC2, ASVS |
| G6-26 | Did we retest permission checks and tenant separation at current scale? | 1 | TODO | | | A01 |
| G6-27 | AI: Did we re-run AI red-team and prompt-injection tests against the current model and tools? | AI | TODO | | | LLM01, NIST Measure |
| G6-28 | Did we hold a **Customer 500 retrospective** (what went wrong, what went right, what we change for the next product)? | 1 | TODO | | | NIST Manage |

### Ongoing rhythm (repeat after launch)

| How often | What to do | Owner |
|---|---|---|
| Daily | Glance at alerts and security dashboards | [[ ]] |
| Weekly | Review failed logins, odd traffic, and open Critical/High findings | [[ ]] |
| Monthly | Update dependencies; check vendor news; review new AI tools or connectors | [[ ]] |
| Quarterly | Access review; incident drill; re-take Part 2 quiz; restore-from-backup test | [[ ]] |
| Yearly | Penetration test; full re-review of this document; policy and training refresh | [[ ]] |

### Gate 6 decision (at customer 500)

| Decision | Name | Date | Notes |
|---|---|---|---|
| `CLOSE REVIEW` / `CONTINUE ON ROUTINE` / `RE-OPEN` | [[ ]] | [[YYYY-MM-DD]] | [[ ]] |

---

# Part 5: Deep-Dive Checklists

Use these as detailed worksheets. Gate rows point here.

Parts 5A–5D apply to everyone (5C and parts of 5B only if they apply). **Parts 5E–5H are optional modules.** Do them only if they apply to your project, and write `N/A` plus the reason at the top of any module you skip.

## 5A. OWASP Top 10:2025 walkthrough (web and API risks)

| ID | Risk | Plain question | Status | Evidence / Notes |
|---|---|---|---|---|
| A01 | Broken Access Control | Can anyone see or do something they should not (other users' data, admin pages)? | TODO | |
| A02 | Security Misconfiguration | Are any settings left open, default, or too generous (cloud storage, debug mode, admin panels)? | TODO | |
| A03 | Software Supply Chain Failures | Do we trust and verify every library, tool, build step, and vendor we depend on? | TODO | |
| A04 | Cryptographic Failures | Is sensitive data encrypted well, with keys kept safe? | TODO | |
| A05 | Injection | Can someone type text that tricks a database, browser, or system command? | TODO | |
| A06 | Insecure Design | Did we think about abuse before building, and set limits and checks? | TODO | |
| A07 | Authentication Failures | Can someone guess, steal, reuse, or bypass logins? | TODO | |
| A08 | Software or Data Integrity Failures | Can someone sneak in changed code, updates, or data without us noticing? | TODO | |
| A09 | Security Logging and Alerting Failures | Would we notice an attack, and could we investigate it afterwards? | TODO | |
| A10 | Mishandling of Exceptional Conditions | When something goes wrong, does the app stay safe and quiet about details? | TODO | |

## 5B. Privacy and data protection checklist (GDPR, CCPA/CPRA, and similar)

> This is a practical checklist, **not legal advice**. Have a privacy or legal professional confirm which laws apply to you.

| ID | Check | Tier | Status | Evidence / Notes |
|---|---|---|---|---|
| PR-01 | Do we know **why** we collect each piece of personal data, and the legal basis (consent, contract, legitimate interest)? | 1 | TODO | |
| PR-02 | Does the privacy policy say, in plain words, what we collect, why, who we share it with, and how long we keep it? | 1 | TODO | |
| PR-03 | Is consent asked for (and easy to withdraw) wherever it is required (cookies, marketing, tracking)? | 1 | TODO | |
| PR-04 | Can people **see, fix, download, and delete** their data? | 1 | TODO | |
| PR-05 | Do we have a "Do Not Sell or Share My Personal Information" option if CCPA/CPRA applies? | 1 | TODO | |
| PR-06 | Is there a signed data-processing agreement with each vendor that handles personal data? | 1 | TODO | |
| PR-07 | Do we know where data is stored, and are cross-border transfers covered by an approved legal method? | 2 | TODO | |
| PR-08 | Do we know how to report a data breach to regulators and customers on time (GDPR: within **72 hours** of becoming aware, where required)? | 1 | TODO | |
| PR-09 | Do we avoid collecting children's data, or have special protections and parental consent? | 1 | TODO | |
| PR-10 | Do we have a record of what personal data we process and why? | 2 | TODO | |
| PR-11 | Is a DPIA done for high-risk processing (large-scale sensitive data, profiling, AI decisions about people)? | 3 | TODO | |
| PR-12 | AI: Do we know if our AI provider stores or trains on our users' data, and did we choose settings or contracts that match our promises? | AI | TODO | |
| PR-13 | AI: Do we tell people when decisions about them are made or influenced by AI, where laws require it? | AI | TODO | |

## 5C. AI risk checklist (OWASP Top 10 for LLM Applications 2025 and NIST AI RMF)

### 5C-1. LLM Top 10 (for products that contain AI)

| ID | Risk | Plain question | Status | Evidence / Notes |
|---|---|---|---|---|
| LLM01 | Prompt Injection | Can someone type (or hide in a document, web page, or email) instructions that make the AI break its rules? | TODO | |
| LLM02 | Sensitive Information Disclosure | Can the AI reveal private data, secrets, or other users' information? | TODO | |
| LLM03 | Supply Chain | Do we trust the models, datasets, plugins, and libraries we use, and can we prove where they came from? | TODO | |
| LLM04 | Data and Model Poisoning | Could bad or planted data change how the AI behaves (training, fine-tuning, or search data)? | TODO | |
| LLM05 | Improper Output Handling | Do we treat AI output as **untrusted** before showing it or passing it to other systems (no automatic running of code or commands)? | TODO | |
| LLM06 | Excessive Agency | Does the AI have **more** tools, permissions, or freedom than it needs? Do risky actions need a human to approve? | TODO | |
| LLM07 | System Prompt Leakage | Are secrets or security rules hidden inside the AI's instructions (they should not be, because instructions can leak)? | TODO | |
| LLM08 | Vector and Embedding Weaknesses | Does search over our documents respect who is allowed to see what, and keep customers separate? | TODO | |
| LLM09 | Misinformation | What happens when the AI is wrong or makes things up? Are users warned, and are high-stakes answers checked? | TODO | |
| LLM10 | Unbounded Consumption | Can one user (or attacker) run up huge cost or take the service down by overusing the AI? | TODO | |

### 5C-2. AI agent permission matrix

List every action an AI agent can take. Decide the rule for each **before** launch.

| Agent / feature | Action (read file, send email, run command, change data, spend money) | Allowed? | Needs human approval? | Logged? | Can it be undone? |
|---|---|---|---|---|---|
| [[ ]] | [[ ]] | [[Yes / No]] | [[Yes / No]] | [[Yes / No]] | [[Yes / No]] |
| [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] |

> **Rule of thumb:** If an action cannot be undone (delete data, send money, email customers), a human approves it. No exceptions without an entry in the Risk Acceptance Log.

### 5C-3. Extra checks for autonomous agents

| ID | Check | Tier | Status | Evidence / Notes |
|---|---|---|---|---|
| AG-01 | Does each agent have its **own** identity and limited keys (not an admin's keys)? | AI | TODO | |
| AG-02 | Is untrusted content (web pages, emails, uploaded files) kept separate from instructions the agent obeys? | AI | TODO | |
| AG-03 | Are the tools an agent can call limited to an approved list, each vetted? | AI | TODO | |
| AG-04 | Is there a cap on steps, time, and spend per task, with a stop button? | AI | TODO | |
| AG-05 | Can we replay what an agent did (inputs, tool calls, outputs)? | AI | TODO | |
| AG-06 | Did we test what happens if two agents or tools give conflicting instructions? | AI | TODO | |

### 5C-4. NIST AI Risk Management Framework quick map

| Function | Plain meaning | Where in this document | Done? |
|---|---|---|---|
| Govern | Who is responsible; what rules we follow | Part 3, Gate 1, Gate 4 | TODO |
| Map | What the AI does, who it affects, what could go wrong | Part 4.5, Part 4.6, Gate 1 | TODO |
| Measure | Test how well and how safely it works | Gate 3, Gate 5, Gate 6 | TODO |
| Manage | Fix problems, respond, and keep improving | Gate 4–6, Parts 6–7 | TODO |

## 5D. Compliance evidence (SOC 2 / ISO 27001 readiness)

You do not need these certificates on day one. Collecting proof **as you go** makes them far easier later.

| ID | Habit | Tier | Status | Evidence / Notes |
|---|---|---|---|---|
| CE-01 | Do we write down security rules (access, passwords, backups, incidents, vendors) in short policies? | 2 | TODO | |
| CE-02 | Do we keep dated proof of key activities (access reviews, test results, drills, training, change approvals)? | 2 | TODO | |
| CE-03 | Does every production change have a ticket, a reviewer, and a record? | 2 | TODO | |
| CE-04 | Do all staff and contractors get basic security training, with records? | 2 | TODO | |
| CE-05 | Are employees' devices protected (disk encryption, screen lock, updates)? | 2 | TODO | |
| CE-06 | Is there a vendor review each year? | 2 | TODO | |
| CE-07 | Do we know which SOC 2 areas matter to customers (Security is always included; Availability, Confidentiality, Processing Integrity, and Privacy are optional)? | 3 | TODO | |
| CE-08 | Is there a target date and budget for an audit, if customers need one? | 3 | TODO | |

## 5E. Module: Payments and money (use if you take card payments or move money)

> **Module applies?** [[Yes / N/A (reason)]]  |  **Payment provider:** [[ ]]  |  **PCI DSS self-assessment type (ask your provider, e.g., SAQ A when card entry is fully outsourced):** [[ ]]

| ID | Check | Tier | Status | Evidence / Notes |
|---|---|---|---|---|
| PY-01 | Is card entry done on the payment provider's hosted page or fields, so card numbers never touch our servers? | 1 | TODO | |
| PY-02 | Do we know which PCI DSS self-assessment applies to us, and is it filled in and filed? | 1 | TODO | |
| PY-03 | Are payment provider notifications (webhooks) verified by signature and safe to receive twice? | 1 | TODO | |
| PY-04 | Are prices, discounts, and totals calculated on the **server**, never trusted from the browser or app? | 1 | TODO | |
| PY-05 | Are card numbers and security codes kept **out** of logs, support tickets, chats, and screenshots? | 1 | TODO | |
| PY-06 | Are live payment keys in the secrets manager and test keys blocked in production? | 1 | TODO | |
| PY-07 | Is there protection against card-testing (many tiny tries) and fraud (rate limits, checks, alerts)? | 1 | TODO | |
| PY-08 | Is there a written chargeback and refund process, with a named owner? | 1 | TODO | |
| PY-09 | Do refunds, payouts, and price changes need MFA and a second person's approval? | 2 | TODO | |
| PY-10 | Are payments compared with our own records every day, with differences investigated? | 2 | TODO | |
| PY-11 | Do wallets, stored balances, or payouts to others get an independent review and a legal license check? | 3 | TODO | |

## 5F. Module: Mobile apps (use if you ship an iOS or Android app; based on OWASP MASVS)

> **Module applies?** [[Yes / N/A (reason)]]  |  **Platforms:** [[iOS / Android / both]]

| ID | Check | Tier | Status | Evidence / Notes |
|---|---|---|---|---|
| MB-01 | Are personal data and tokens kept out of plain files, logs, backups, and screenshots, using the phone's secure storage? | 1 | TODO | |
| MB-02 | Are **no secrets or private keys** inside the app file? (Assume anything shipped can be pulled out.) | 1 | TODO | |
| MB-03 | Do we use the phone's standard encryption tools instead of homemade ones? | 1 | TODO | |
| MB-04 | Does the server check every request, even if the app has a fingerprint or face unlock? | 1 | TODO | |
| MB-05 | Does all network traffic use TLS, with no way to turn it off? | 1 | TODO | |
| MB-06 | Are app permissions the minimum needed, and are deep links and incoming data checked? | 1 | TODO | |
| MB-07 | Are third-party SDKs (analytics, ads, crash reports) reviewed for what data they collect? | 1 | TODO | |
| MB-08 | Do the app store privacy labels and data-safety forms match what the app really does? | 1 | TODO | |
| MB-09 | Are app signing keys protected and store accounts using MFA? | 1 | TODO | |
| MB-10 | Can we force old, unsafe app versions to update? | 2 | TODO | |
| MB-11 | Was the app tested on real devices with a mobile security test? | 2 | TODO | |
| MB-12 | For high-risk apps: are extra protections added (certificate pinning, root/jailbreak detection, code hardening)? These are extra layers, never the main defence. | 3 | TODO | |

## 5G. Module: Cloud and infrastructure (use if you run anything in a cloud or on servers)

> **Module applies?** [[Yes / N/A (reason)]]  |  **Cloud provider(s):** [[ ]]  |  **Recovery goals:** Can be down for at most [[ ]] (RTO). Can lose at most [[ ]] of data (RPO).

| ID | Check | Tier | Status | Evidence / Notes |
|---|---|---|---|---|
| CL-01 | Does the cloud owner (root) account use MFA, stay unused day to day, and trigger an alert when used? | 1 | TODO | |
| CL-02 | Do people use named accounts with MFA and least-privilege roles, and avoid long-lived access keys? | 1 | TODO | |
| CL-03 | Is everything private by default, with databases never reachable directly from the internet? | 1 | TODO | |
| CL-04 | Are storage buckets private unless a reviewed reason makes them public? | 1 | TODO | |
| CL-05 | Is encryption at rest on, with keys held in the cloud key service? | 1 | TODO | |
| CL-06 | Is the cloud audit log on, stored where admins cannot edit it, with alerts on risky changes? | 1 | TODO | |
| CL-07 | Are backups stored in a separate account or region, protected from deletion, and restore-tested? | 1 | TODO | |
| CL-08 | Are budget alerts and quotas set so abuse (like crypto-mining) is noticed fast? | 1 | TODO | |
| CL-09 | Are dev, test, and production separated (different accounts or projects)? | 2 | TODO | |
| CL-10 | Is infrastructure defined as code, reviewed like code, with manual production changes recorded? | 2 | TODO | |
| CL-11 | Are servers and container images patched, minimal, and not run as the all-powerful user? | 2 | TODO | |
| CL-12 | Does a regular scan look for cloud misconfiguration, with findings tracked? | 2 | TODO | |
| CL-13 | Are RTO and RPO written above, and has a recovery test proven we can meet them? | 2 | TODO | |
| CL-14 | Is outside access (contractors, vendors) time-limited and reviewed? | 2 | TODO | |
| CL-15 | If using Kubernetes: are roles least-privilege, network rules restrictive, and secrets kept out of plain config? | 2 | TODO | |

## 5H. Module: Regulated industries (use if any row below matches; confirm with legal)

> This module is a **starter map**, not legal advice. For every row that matches, name the legal owner and write down which rules apply.

**Module applies?** [[Yes / N/A (reason)]]

| If you handle... | Rule families to check (examples) | Starter checks | Matches us? | Legal owner | Status | Evidence / Notes |
|---|---|---|---|---|---|---|
| US health information | HIPAA | Signed business associate agreements with vendors; access logging; only the minimum data; breach notification plan | [[Y/N]] | [[ ]] | TODO | |
| Card payments | PCI DSS | See Part 5E | [[Y/N]] | [[ ]] | TODO | |
| Children's data (US, under 13) | COPPA | Parental consent flow; minimal data; deletion on request | [[Y/N]] | [[ ]] | TODO | |
| Student records | FERPA and local education rules | School agreements; access limits; deletion terms | [[Y/N]] | [[ ]] | TODO | |
| Financial customer data (US) | GLBA Safeguards, state rules | Written security program; vendor oversight; incident reporting | [[Y/N]] | [[ ]] | TODO | |
| EU customers and AI features | EU AI Act | Decide your AI risk class; tell users they are talking to AI; extra duties if the AI affects hiring, credit, education, or essential services | [[Y/N]] | [[ ]] | TODO | |
| EU financial or critical services | DORA, NIS2 | Check whether you are in scope; incident reporting duties; supplier risk | [[Y/N]] | [[ ]] | TODO | |
| Government customers | FedRAMP, StateRAMP, local equivalents | Check if authorization is needed before selling | [[Y/N]] | [[ ]] | TODO | |
| Other regulated field | [[name it]] | [[ ]] | [[Y/N]] | [[ ]] | TODO | |

| ID | Check | Tier | Status | Evidence / Notes |
|---|---|---|---|---|
| RG-01 | Have legal and the Security reviewer confirmed in writing which rules apply, and is the list saved in the evidence folder? | 1 | TODO | |
| RG-02 | AI: For AI sold or used in the EU, is the AI risk class decided and written down? | AI | TODO | |
| RG-03 | Is each rule's required contract, notice, or registration done before launch? | 1 | TODO | |
| RG-04 | Is there a calendar of renewals, audits, and reporting deadlines with an owner? | 2 | TODO | |

---

# Part 6: Incident Response Plan (one page)

An **incident** is anything that harms or could harm customers, data, or the product: a leak, a break-in, a stolen laptop, a runaway AI, or a long outage.

### 9.1 Who to call

| Situation | Call first | Backup | How (phone, chat) |
|---|---|---|---|
| Suspected break-in or data leak | [[ ]] | [[ ]] | [[ ]] |
| Outage | [[ ]] | [[ ]] | [[ ]] |
| AI behaving dangerously | [[ ]] | [[ ]] | [[ ]] |
| Legal or press questions | [[ ]] | [[ ]] | [[ ]] |
| Cloud / key vendor contacts | [[ ]] | [[ ]] | [[ ]] |

### 9.2 Five steps (follow in order)

1. **Detect and declare.** Anyone can declare an incident. Write the time and what you saw. Do not delete evidence.
2. **Contain.** Stop the harm: disable the account, turn off the AI feature (kill switch), block the address, rotate leaked secrets.
3. **Understand.** What happened, since when, which data, which customers? Preserve logs.
4. **Recover and tell people.** Restore safe service. Tell affected customers and regulators when required (GDPR: within 72 hours of becoming aware, where required; confirm other laws with legal).
5. **Learn.** Within 5 working days, write a short "what happened, why, what we change" report. No blame. Add new checks to this document.

### 9.3 Incident log template (copy for each incident)

| Field | Answer |
|---|---|
| Incident ID | [[INC-001]] |
| Date and time found | [[ ]] |
| Declared by | [[ ]] |
| Severity (Critical / High / Medium / Low) | [[ ]] |
| What happened (plain words) | [[ ]] |
| Data or customers affected | [[ ]] |
| Containment actions and times | [[ ]] |
| Customers / regulators notified? When? | [[ ]] |
| Root cause | [[ ]] |
| Fixes and follow-ups (with owners and dates) | [[ ]] |
| New checks added to this document | [[ ]] |

---

# Part 7: Findings Register and Risk Acceptance

### 10.1 Findings Register (every `FAIL` goes here)

| Finding ID | Found on | Check ID | What is wrong (plain words) | Severity | Owner | Fix due | Status (Open / Fixed / Retested / ACCEPTED) | Proof of fix |
|---|---|---|---|---|---|---|---|---|
| F-001 | [[YYYY-MM-DD]] | [[G2-14]] | [[ ]] | [[High]] | [[ ]] | [[YYYY-MM-DD]] | [[Open]] | [[ ]] |
| F-002 | | | | | | | | |
| F-003 | | | | | | | | |

### 10.2 Risk Acceptance Log (when we choose to live with a risk)

> **Who may accept what:** Low and Medium: Project owner (maximum 90 days). **High: only after launch (Gates 5–6), only by the Executive sponsor, maximum 30 days.** **Critical: never.** Before Gate 4, neither High nor Critical may be accepted: fix it or do not ship.
> Every acceptance **must** have an expiry date and a plan.

| Entry # | Finding ID | Why we accept it | What could happen | What reduces the risk meanwhile | Accepted by (name, role) | Date | Expires | Re-review owner |
|---|---|---|---|---|---|---|---|---|
| RA-001 | [[F-00x]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] | [[ ]] |

---

# Part 8: Final Sign-Off

Complete this at **Gate 4 (before launch)** and again at **Gate 6 (customer 500)**.

### Summary

| Item | Gate 4 | Gate 6 |
|---|---|---|
| Date | [[ ]] | [[ ]] |
| Risk Tier | [[ ]] | [[ ]] |
| Required checks | [[ ]] | [[ ]] |
| `PASS` | [[ ]] | [[ ]] |
| `N/A` (reasons written) | [[ ]] | [[ ]] |
| `ACCEPTED` | [[ ]] | [[ ]] |
| `FAIL` / `TODO` (must be 0 to sign) | [[ ]] | [[ ]] |
| Open Critical findings (must be 0) | [[ ]] | [[ ]] |
| Open High findings (must be 0 at Gate 4) | [[ ]] | [[ ]] |
| Known risks the sponsor is aware of | [[ ]] | [[ ]] |

### Signatures

| Role | Name | Decision (Approve / Approve with conditions / Reject) | Date | Conditions |
|---|---|---|---|---|
| Project owner | [[ ]] | [[ ]] | [[ ]] | [[ ]] |
| Security reviewer | [[ ]] | [[ ]] | [[ ]] | [[ ]] |
| Engineering lead | [[ ]] | [[ ]] | [[ ]] | [[ ]] |
| Privacy / legal contact | [[ ]] | [[ ]] | [[ ]] | [[ ]] |
| Executive sponsor | [[ ]] | [[ ]] | [[ ]] | [[ ]] |

> By signing, each person confirms they read the Findings Register and Risk Acceptance Log and that the evidence links work.

---

# Appendices

## Appendix A: Example of a correctly filled row

| ID | Check | Tier | Status | Evidence / Notes | Owner | Maps to |
|---|---|---|---|---|---|---|
| G2-14 | Is each customer blocked from seeing other customers' data? | 1 | PASS | Test `tenant_isolation_spec` in repo, run #482, all 14 cases denied. Report: `evidence/G2-14-run482.pdf` | Priya (Eng lead) | A01 |
| G2-29 | Are file uploads limited by type and size, scanned, and stored outside the web root? | 2 | N/A | We have no file uploads in this product. Revisit if we add avatars. | Marco (PM) | A05 |
| G2-18 | Are login attempts rate-limited and lockout in place? | 1 | FAIL | Login accepts unlimited tries. Logged as F-004 (High), due before Gate 3. | Priya | A07 |

**What makes these good:** clear status word, a link or file as proof, a named owner, and a reason for every `N/A` and `FAIL`.

## Appendix B: Glossary (plain words)

| Word | Plain meaning |
|---|---|
| Access control | Rules about who can see or do what |
| Agent (AI agent) | An AI that can take actions, not just answer |
| API | A door that lets programs talk to each other |
| Authentication | Proving who you are (logging in) |
| Authorization | Checking what you are allowed to do after logging in |
| Backup | A safe copy you can restore from |
| Breach | When private data gets out or is taken |
| DPIA | A written risk check for risky uses of personal data |
| DPA | A contract that says how a vendor must protect personal data |
| Encryption | Scrambling data so only people with the key can read it |
| Evidence | Proof you can show (link, screenshot, report) |
| Incident | Anything that harms or could harm people, data, or service |
| Injection | Tricking a system by typing text it mistakes for commands |
| Least privilege | Only the keys you need, nothing extra |
| LLM | Large language model, the kind of AI behind chatbots |
| MCP | A standard way to plug tools and data into AI |
| MFA | A password plus a second proof, like a phone code |
| Multi-tenant | Many customers sharing one system |
| Penetration test | Hired experts safely try to break in, then report |
| Personal data | Anything that identifies a person |
| Prompt injection | Hidden or typed instructions that trick an AI into breaking its rules |
| RAG | AI that looks up your documents before answering |
| Rate limit | A cap on how many times something can be tried |
| Risk acceptance | A signed decision to live with a known risk |
| SAST / DAST | Scanning code (SAST) or the running app (DAST) for weaknesses |
| SBOM | A list of every part inside your software |
| Secret | A password, key, or token |
| SOC 2 / ISO 27001 | Well-known security audits and certificates customers ask for |
| Sub-processor | A vendor your vendor uses to handle data |
| Tenant | One customer inside a shared system |
| TLS | The lock icon: protects data traveling over the internet |
| Vulnerability | A weakness someone could use |
| WAF | A filter in front of your website that blocks bad traffic |
| BAA | Business associate agreement: a contract needed when a vendor handles US health data |
| IAM | Identity and access management: who gets which keys in your cloud |
| MASVS | OWASP's security checklist for mobile apps |
| PCI DSS | The rulebook for handling payment cards |
| RTO / RPO | How long you can be down (RTO) and how much data you can lose (RPO) |
| SAQ | The self-assessment form for PCI DSS |

## Appendix C: Standards behind this template

| Standard | Used for | Where it appears |
|---|---|---|
| OWASP Top 10:2025 (web) | Common web and API risks | Part 5A, "Maps to" column |
| OWASP ASVS 5.0 (Levels 1–3) | Depth of testing by tier | Part 2, Gate 3 |
| OWASP Top 10 for LLM Applications 2025 | AI product risks | Part 5C |
| NIST AI RMF 1.0 (Govern, Map, Measure, Manage) and Generative AI Profile (AI 600-1) | AI governance process | Part 5C-4 |
| GDPR and CCPA/CPRA | Privacy duties | Part 5B, Gate 4, 6 |
| SOC 2 Trust Services Criteria, ISO/IEC 27001 | Audit readiness | Part 5D |
| PCI DSS (through your payment provider) | Card payments | G4-12, Part 5E |
| OWASP MASVS | Mobile app security | Part 5F |
| Cloud provider security guidance and CIS benchmarks | Cloud and infrastructure | Part 5G |
| HIPAA, COPPA, FERPA, GLBA, EU AI Act, DORA, NIS2 | Regulated industries (starter map) | Part 5H |

Tier to ASVS level: Tier 1 → Level 1, Tier 2 → Level 2, Tier 3 → Level 3.

## Appendix D: Guide for the template owner (not for project teams)

1. **Never fill in the master.** Projects copy it and rename it `Security_Review_[ProjectName].md`.
2. **Review the master every quarter** and after any major standards change (new OWASP list, new laws). Update the version number and the Change Log.
3. **Keep row IDs stable.** Never reuse an old ID for a different check, so past reviews stay comparable. Add new rows at the end of a section with the next number.
4. **Add company-specific rows** in a clearly marked "Company additions" block rather than rewriting standard rows.
5. **Track template feedback.** After every project's Gate 6, collect: rows that confused people, rows that never applied, and incidents the template did not catch.
6. **Version history:** 1.0.0 first release. 1.1.0 stricter rule (no open High findings at launch, High acceptable only after launch for 30 days) and added modules 5E to 5H.
7. **Optional automation:** AI assistants can pre-fill evidence links and draft findings, but a human reviewer must confirm every `PASS`.

## Appendix E: Change Log

| Date | Version / Gate | Who | What changed and why |
|---|---|---|---|
| [[YYYY-MM-DD]] | [[1.0.0 / Gate 1]] | [[ ]] | Created from template |
| | | | |

## Appendix F: Sources and further reading

- OWASP Top 10:2025: https://owasp.org/Top10/2025/
- OWASP Application Security Verification Standard: https://owasp.org/www-project-application-security-verification-standard/
- OWASP GenAI Security Project (Top 10 for LLM Applications 2025): https://genai.owasp.org/
- NIST AI Risk Management Framework: https://www.nist.gov/itl/ai-risk-management-framework
- GDPR official text: https://gdpr-info.eu/
- California Consumer Privacy Act (California Attorney General): https://oag.ca.gov/privacy/ccpa
- OWASP Mobile Application Security (MASVS): https://mas.owasp.org/MASVS/
- PCI Security Standards Council: https://www.pcisecuritystandards.org/
- US HHS HIPAA guidance: https://www.hhs.gov/hipaa/
- EU AI Act overview: https://artificialintelligenceact.eu/
