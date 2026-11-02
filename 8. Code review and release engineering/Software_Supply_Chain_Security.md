# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **Template version:** 0.2 (DRAFT for review) | **Folder:** Code review and release engineering | **File:** `Software_Supply_Chain_Security.md`
> **Covers:** AI-driven development life cycle, from the first idea to your first 500 customers.

## What is this document?

Imagine you are baking a cake to sell. You need to know:
- **Where every ingredient came from** (flour, eggs, sugar).
- **That nobody added something bad** to the ingredients or the kitchen.
- **That the box is sealed** when it reaches the customer.

Software works the same way. Your product is made of ingredients (code other people wrote, tools, AI helpers, and cloud services). **"Software supply chain security" means knowing your ingredients, keeping your kitchen safe, and sealing the box.**

This document is a **questionnaire**. You answer questions in plain words. At the end you will know whether your product is safe enough to move to the next stage.

## Who can fill this in?

Anyone. You do **not** need to be technical. If a question feels too technical, use the **"In plain words"** line under it. If you still do not know, follow Rule 3.

## The 7 Golden Rules

1. **One question at a time.** Start at Part A. Go in order. Do not skip.
2. **Write real answers.** Replace every `👉 ANSWER:` with your words. Short is fine ("Yes, we use GitHub").
3. **Never guess.** If you do not know, write `UNKNOWN` and put a **name** and a **date** next to it. Example: `UNKNOWN. Ask Priya by 2026-11-01.`
4. **Never leave a blank.** Blank = unfinished. `NOT APPLICABLE (because ...)` is allowed, but always give the reason.
5. **Show proof.** When a question asks for **Evidence**, paste a link, a file name, or a screenshot name. "Trust me" is not evidence.
6. **Never paste secrets.** Do **not** write passwords, keys, or tokens in this file. Write where they are stored (for example, "in our password manager"), not what they are.
7. **Stop at the gate.** At the end of each Stage, there is a **GATE**. If any ❌ is left, you do **not** move on, unless a named person signs the **Exception** box.

## Status symbols (use these everywhere)

| Symbol | Meaning |
|---|---|
| ✅ | Done, and I have proof |
| 🟡 | Started, not finished |
| ❌ | Not done |
| ➖ | Not applicable (reason written) |
| ❓ | UNKNOWN (name and date written) |

To tick a box, change `[ ]` to `[x]`.

## How long will it take?

| Part | First time | Next projects (copy and reuse) |
|---|---|---|
| Part A: About your product | 30 min | 15 min |
| Part B: Stage Gates 0 to 6 | 3 to 6 hours total (spread over the project) | 1 to 3 hours |
| Part C: AI section | 45 min | 20 min |
| Part D: Problem-response plan | 30 min | 10 min |
| Part E and F: Scorecard and sign-off | 20 min | 10 min |

## When do I fill which Stage?

Fill each Stage **at the time you reach it**, not all at once. Part A and Part C are filled **once at the start**, then revisited at every gate.

## Example of a good answer

```
B2.3  Where is our code stored, and who can change it?
👉 ANSWER: On GitHub, in the "acme-app" repository. 4 people can change it: Sam, Priya, Lee, Ana.
Evidence: screenshot "github-members-2026-10-18.png"
Status: ✅
```

## Example of a bad answer (do NOT do this)

```
B2.3  👉 ANSWER: Somewhere safe, I think.
Status: ✅
```
(Why bad: no place, no names, no proof, and "I think" means guessing. It should be `❓ UNKNOWN. Ask Sam by Friday.`)

## Map of this document

| Part | What it is | Must I fill it? |
|---|---|---|
| Document Control | Name, owner, dates | Yes |
| **A** | About your product, roles (RACI) | Yes |
| **B** | 7 Stage Gates, Stage 0 to 6 | Yes, one stage at a time |
| **C** | AI rules | Yes (short path for 🟢 Basic) |
| **D** | "What if something goes wrong?" plan | Yes, before launch |
| **D2** | Add-ons: Mobile, Containers, Web/API, Library, Device | Only the ones that match your product |
| **E** | Standards map for auditors | **Optional.** Skip unless someone asks |
| **F** | Score, exceptions, sign-off, evidence list | Yes |
| **G** | Glossary | Read when stuck |
| **H** | Reuse guide for the template owner | Template owner only |
| **I** | A finished example (fictional project) | Read once, so you see what "good" looks like |

## How to read the tags on each question

Every question has a small tag like `⚡ Quick · Engineer`. It tells you **how long it takes** and **who usually answers it**. Use it to hand questions to the right person.

| Tag | Meaning |
|---|---|
| ⚡ Quick | About 10 minutes or less |
| ⏳ Medium | About 10 to 60 minutes |
| 🧱 Long | More than 1 hour, or needs a meeting |
| Owner | Founder, project owner, or manager |
| Product | Product or project manager |
| Engineer | Developer or technical lead |
| Security | Security contact (or the most careful engineer, if you have no specialist) |
| Legal | Lawyer or whoever handles contracts and rules |

> The role is a **suggestion**. The person named in the RACI table (A13) can always reassign it. The **Accountable** person must still confirm every answer.

## Words you may not know

Look in **Part G: Glossary** at the end. Every hard word has a one-line kid-friendly meaning.

---

# DOCUMENT CONTROL (fill once)

| Field | 👉 Your answer |
|---|---|
| Project name | |
| Project code / ID (example: PRJ-0042) | |
| Product one-sentence description | |
| Document owner (one person, not a team) | |
| Security contact (name + email) | |
| Date started (YYYY-MM-DD) | |
| Current stage (0 to 6) | |
| Version of this filled document | |
| Template version used | 0.2 |
| Where this file lives (link) | |

### Change log (add a row every time you edit meaningfully)

| Date | Who | What changed | Why |
|---|---|---|---|
| | | | |

---

# PART A: ABOUT YOUR PRODUCT (fill once at the start)

> **Why:** You cannot protect something you have not described. These answers decide which later questions apply to you.

**A1. `⚡ Quick · Product` What does your product do, in one sentence a 10-year-old would understand?**
👉 ANSWER:

**A2. `⚡ Quick · Product` What type of product is it?** (tick all that apply)
- [ ] Website or web app
- [ ] Mobile app (iPhone / Android)
- [ ] Desktop app
- [ ] API or backend service
- [ ] Software library or package others install
- [ ] Device with software inside (a "digital product" you ship)
- [ ] AI-powered product (uses an AI model inside the product)
- [ ] Other: ______

> *In plain words:* This tells us how your software reaches customers, because each type has different risks.

**A3. `⚡ Quick · Legal` Where will customers be? (countries or regions)**
👉 ANSWER:
- [ ] European Union / EU customers → **EU Cyber Resilience Act (CRA) may apply.** See Part E.
- [ ] United States government customers → **NIST SSDF attestation may be requested.**
- [ ] Other regulated areas (health, money, children): ______

**A4. `⚡ Quick · Product` What kind of data will the product handle?** (tick all that apply)
- [ ] No personal data
- [ ] Names / emails
- [ ] Payment or money data
- [ ] Health data
- [ ] Children's data
- [ ] Company secrets of customers
- [ ] Other: ______

**A5. `⏳ Medium · Owner` If the worst happened (a hacker poisoned your software), who would be hurt and how badly?**
- [ ] Low (annoyance only)
- [ ] Medium (customers lose time or privacy)
- [ ] High (customers lose money, health data, or safety)

👉 ANSWER (explain in 2 sentences):

**A6. `🧱 Long · Engineer` Which tools and places make your software? (list them all, even small ones)**

| Purpose | Tool / service name | Who owns the account? | Turned on 2-step login? (Y/N) |
|---|---|---|---|
| Stores the code (example: GitHub) | | | |
| Builds / tests the code automatically (CI/CD) | | | |
| Stores finished software (registry) | | | |
| Runs the product (cloud / hosting) | | | |
| Stores passwords and keys (secrets) | | | |
| Tracks tasks (example: Jira) | | | |
| AI coding helpers | | | |
| Other | | | |

> **Rule:** Any "N" in the last column = ❌ to fix before Gate 1.

**A7. `⏳ Medium · Owner` Who is on the team?**

| Name | Role | Can change code? | Can release to customers? | Is a person / contractor / AI agent? |
|---|---|---|---|---|
| | | | | |

**A8. `⚡ Quick · Engineer` Which programming languages and package systems do you use?** (example: JavaScript with npm, Python with pip)
👉 ANSWER:

**A9. `⚡ Quick · Product` Does the product use AI inside it (an AI model that your customers' data goes through)?**
- [ ] Yes → fill **Part C, Section C4** too.
- [ ] No

**A10. `⚡ Quick · Owner` Who is the ONE person who can say "stop the release"?**
👉 ANSWER (name + backup name):

**A11. `⚡ Quick · Owner` How strict do you need to be? (choose a level, you can raise it later)**

| Level | Pick this if... | Tick |
|---|---|---|
| 🟢 **Basic** | Small product, low risk, no sensitive data | [ ] |
| 🟡 **Standard** | Real customers, some personal data | [ ] |
| 🔴 **Strict** | Money, health, children, government, or EU legal duty | [ ] |

> Questions marked **🔴** below are required at Strict, **🟡** at Standard and Strict, and unmarked ones at every level.

**A13. `⏳ Medium · Owner` Who does what? (RACI: fill one row per stage)**

> **R** = Responsible (does the work) | **A** = Accountable (final yes/no, only ONE person per row) | **C** = Consulted (asked first) | **I** = Informed (told after)
> Write a **name** in each cell, not a team.

| Stage | R (does it) | A (decides, only one) | C (asked) | I (told) |
|---|---|---|---|---|
| 0 Plan | | | | |
| 1 Design (including suppliers) | | | | |
| 2 Build | | | | |
| 3 Review and Test | | | | |
| 4 Release | | | | |
| 5 Launch | | | | |
| 6 First 500 customers | | | | |
| Emergency response (Part D) | | | | |
| AI helpers (Part C) | | | | |

> **Check:** Every "A" cell has exactly one name. Two names = nobody is truly in charge ❌.

**A12. `⚡ Quick · Legal` Which outside rules do you follow or promise to follow?** (tick all)
- [ ] NIST SSDF
- [ ] SLSA (target level: __ )
- [ ] EU CRA
- [ ] SOC 2
- [ ] ISO 27001
- [ ] OWASP CI/CD Top 10
- [ ] OpenSSF Scorecard
- [ ] Customer contract requires: ______
- [ ] None yet

---

# PART B: STAGE GATES (from idea to your first 500 customers)

> **How stage gates work:** Think of 7 doors in a hallway. You may only open the next door when the checklist for the current door is all ✅. Every stage has: **Questions**, **Checklist**, **Evidence**, and a **GATE decision**.

```
Stage 0 Plan → 1 Design → 2 Build → 3 Review & Test → 4 Release → 5 Launch → 6 First 500 Customers
```

---

## STAGE 0: PLAN (before any code)

**Goal in one sentence:** Decide what you are protecting, from whom, and who is responsible.

**B0.1 `⚡ Quick · Owner` Who is responsible for supply chain security on this project?**
👉 ANSWER (name, role, backup):
Evidence:
Status:

**B0.2 `⏳ Medium · Security` What are the top 3 bad things that could happen to your software supply chain?** (use these ideas or write your own)
- A hacker slips bad code into our code
- A package we use is secretly poisoned
- Our build machine is hacked and the finished app is changed
- Our AI helper installs a fake package
- Someone steals our keys or passwords
- A customer receives a changed copy of our app

👉 ANSWER (pick 3, in your words):
1.
2.
3.

**B0.3 `⚡ Quick · Owner` What is your security goal for the first 500 customers?** (tick one)
- [ ] 🟢 "We know what's inside our product and can fix problems fast."
- [ ] 🟡 "Plus: our releases are signed and proven to come from us."
- [ ] 🔴 "Plus: independent check (audit) and legal readiness."

**B0.4 `⚡ Quick · Owner` What is your budget and time for security work?**
👉 ANSWER (hours per week / money, owner):

**B0.5 `⚡ Quick · Owner` Rules for choosing tools. Who approves a NEW tool, service, or AI helper before the team uses it?**
👉 ANSWER (name, how to ask):

**B0.6 `⏳ Medium · Owner` Do you have a written list of "approved tools"?**
- [ ] Yes, link: ______
- [ ] No → create one now (use the table in A6)

**B0.7 `⚡ Quick · Owner` What happens if someone leaves the team?** (Who removes their access, how fast?)
👉 ANSWER (name, within how many hours):

### Stage 0 Checklist
- [ ] A named owner exists (B0.1)
- [ ] Top 3 risks written (B0.2)
- [ ] Goal level chosen (B0.3)
- [ ] Tool approval process written (B0.5)
- [ ] Leaving-team process written (B0.7)
- [ ] Part A fully answered (no blanks)
- [ ] Part C (AI rules) sections C1 to C3 answered

### 🚪 GATE 0 DECISION
| Result | Tick |
|---|---|
| ✅ PASS: every box above ticked | [ ] |
| ❌ FAIL: items left (list them): | [ ] |
| ⚠️ EXCEPTION: allowed to continue with risk (fill the Exception box in Part F) | [ ] |

Decided by: ______ Date: ______

---

## STAGE 1: DESIGN (decide how it will be built)

**Goal in one sentence:** Choose safe ingredients and safe ways of working before you build.

**B1.1 `🧱 Long · Engineer` List the BIG building blocks you plan to use** (frameworks, databases, cloud services, AI models, payment tools).

| Building block | What for | Who makes it | Open source or paid? | License (if known) | Approved by | Date |
|---|---|---|---|---|---|---|
| | | | | | | |

> *In plain words:* These are the big "ingredients." Later, tools will list the small ones automatically.

**B1.2 `🧱 Long · Engineer` For each big building block, did you check these?** (tick all that you did)
- [ ] Is it actively maintained? (updated within the last 12 months)
- [ ] Does it have many users / a real team behind it?
- [ ] Are there known big problems? (search its name + "vulnerability")
- [ ] Is the license OK for our product? (ask legal if unsure)
- [ ] Is there a safer or simpler choice?

👉 ANSWER (summary, any worries):

**B1.3 `⏳ Medium · Engineer` How will code get from a developer's laptop to customers? Draw or describe the path.**
```
Developer / AI helper → ______ → ______ → ______ → Customer
```
👉 ANSWER (name every step and tool):

**B1.4 `⚡ Quick · Engineer` Where will secrets live?** (passwords, API keys, signing keys)
- [ ] In a secrets manager / password manager: ______
- [ ] In code files (NOT allowed ❌)
- [ ] In chat or email (NOT allowed ❌)
- [ ] UNKNOWN

👉 ANSWER (name the tool, who can see them):

**B1.5 `⏳ Medium · Owner` What is your plan for "who can do what"? (least access)**
👉 ANSWER (example: "Only 2 people can release. Everyone else can only suggest changes."):

**B1.6 `🧱 Long · Security` 🟡 Did you do a "what could go wrong" talk (threat modeling) for the build and release path?**
- [ ] Yes, date: ______, notes link: ______
- [ ] No

**B1.7 `⏳ Medium · Engineer` 🟡 Which signing method will you use to prove "this really came from us"?**
- [ ] Keyless signing (example: Sigstore / cosign)
- [ ] Key-based signing (keys stored safely at: ______)
- [ ] Platform-provided signing (name): ______
- [ ] Not decided yet ❓ (owner and date)

**B1.8 `⚡ Quick · Security` 🔴 What is your target SLSA level for releases at launch?** (SLSA is a ladder of build-safety levels)
- [ ] Level 1: build is scripted and leaves a record
- [ ] Level 2: built on a trusted hosted service; record is signed
- [ ] Level 3: the build machine itself is hardened
- [ ] Not decided ❓

> **Checked against the SLSA v1.1 spec: Build track Levels 1 to 3.**

**B1.9 `⏳ Medium · Engineer` How will you keep a "list of ingredients" (SBOM) for every release?**
- [ ] Auto-generated in the build (tool: ______)
- [ ] Manual (not recommended)
- [ ] Not decided ❓
- Format chosen: [ ] CycloneDX [ ] SPDX

**B1.10 `⚡ Quick · Security` Who is in charge of handling security reports from outsiders (people who find problems)?**
👉 ANSWER (name, email, plan to publish a `SECURITY.md` file):

### 1B. Suppliers, vendors, agencies, and contractors

> *In plain words:* If someone outside your team writes code, hosts your product, or holds your data, **their mistakes become your mistakes.** List them and check them.

**B1.11 `⏳ Medium · Owner` List every outside company or person who writes code, builds, hosts, or handles data for you.**

| Name | What they do | Can they change our code? | Can they see customer data? | Contract signed? (Y/N) | Security terms in contract? (Y/N) | Reviewed on (date) |
|---|---|---|---|---|---|---|
| | | | | | | |

**B1.12 `⏳ Medium · Legal` Before you start with a supplier, did you ask these?** (tick all you asked)
- [ ] Do you use 2-step login for everyone?
- [ ] Do you keep an ingredient list (SBOM) for what you give us?
- [ ] How fast do you tell us if you are hacked? (hours: ___)
- [ ] Do you let your people use AI helpers on our code? What rules?
- [ ] Can we see a recent security report (SOC 2, ISO 27001, or a questionnaire)?
- [ ] What happens to our data and code if we leave?

**B1.13 `⚡ Quick · Engineer` Do contractors work in YOUR accounts with their own named login (never shared logins)?**
- [ ] Yes   - [ ] No ❌   - [ ] N/A

**B1.14 `⚡ Quick · Owner` When a contractor's work ends, who removes their access, and within how many hours?**
👉 ANSWER (name, hours):

**B1.15 `⚡ Quick · Legal` 🟡 Does the contract say who must fix security problems in their work, and how fast?**
- [ ] Yes   - [ ] No   - [ ] N/A

### Stage 1 Checklist
- [ ] Big building blocks listed and checked (B1.1 and B1.2)
- [ ] Suppliers listed and checked (B1.11 to B1.14)
- [ ] Delivery path drawn (B1.3)
- [ ] Secrets storage chosen (B1.4)
- [ ] Access plan written (B1.5)
- [ ] 🟡 Threat talk done (B1.6)
- [ ] 🟡 Signing method chosen (B1.7)
- [ ] 🔴 SLSA target chosen (B1.8)
- [ ] SBOM plan chosen (B1.9)
- [ ] Security contact named (B1.10)

### 🚪 GATE 1 DECISION
| Result | Tick |
|---|---|
| ✅ PASS | [ ] |
| ❌ FAIL (list): | [ ] |
| ⚠️ EXCEPTION (see Part F) | [ ] |

Decided by: ______ Date: ______

---

## STAGE 2: BUILD (writing the code, with humans and AI)

**Goal in one sentence:** Make sure only trusted people, trusted tools, and trusted packages touch the code.

> ### 🚀 Beginner shortcut: the "Big 8" for Stage 2
> Stage 2 is the longest stage. **If you feel lost, answer these 8 questions first.** They give you the biggest safety gain for the least work. Then continue with the rest.
>
> | # | Question | What it protects you from |
> |---|---|---|
> | 1 | B2.1 2-step login on everything | Stolen passwords |
> | 2 | B2.2 Main branch locked | Sneaky changes to your code |
> | 3 | B2.6 Secret scanning on | Leaked keys |
> | 4 | B2.7 Lock files | Surprise package changes |
> | 5 | B2.8 Automatic problem warnings | Known-bad ingredients |
> | 6 | B2.9 New-package rule | Fake or poisoned packages (also AI-invented ones) |
> | 7 | B2.14 Build runs only trusted code | A hacked assembly line |
> | 8 | B2D Automatic checks table | Mistakes slipping through |
>
> **Tag guide for the rest of Stage 2:** 🟢 Basic projects may mark 🟡 and 🔴 questions as `➖ (level: Basic)`.

### 2A. Protect the code storage

**B2.1 `⚡ Quick · Engineer` Is 2-step login (MFA) turned on for EVERY person and service that can touch the code?**
- [ ] Yes, all
- [ ] Some (who is missing?): ______
- [ ] No ❌
Evidence:

**B2.2 `⚡ Quick · Engineer` Branch protection: can anyone push straight to the main code branch?**
- [ ] No. All changes need a review request (pull request / PR) and at least ___ approval(s)
- [ ] Yes ❌ (fix before Gate 2)
Evidence (screenshot of settings):

> *In plain words:* "Main branch" is the master recipe. Nobody should change it without a second person checking.

**B2.3 `⚡ Quick · Engineer` Who can change the code? (paste the list or a screenshot name)**
👉 ANSWER:

**B2.4 `⚡ Quick · Engineer` Do you remove access for people who left, within ___ hours?**
👉 ANSWER (proof of last removal):

**B2.5 `⚡ Quick · Engineer` Are commits signed or tied to verified people?** (🟡)
- [ ] Yes   - [ ] No   - [ ] N/A

**B2.6 `⏳ Medium · Engineer` Is secret-scanning turned on to catch passwords accidentally saved in code?**
- [ ] Yes, tool: ______
- [ ] No ❌
- If a secret is found: who is told, and in how many hours?  👉 ______

### 2B. Protect the ingredients (dependencies)

**B2.7 `⚡ Quick · Engineer` Does every package version get "locked" (a lock file)?**
- [ ] Yes, lock file name: ______
- [ ] No ❌

**B2.8 `⏳ Medium · Engineer` Is there an automatic tool that warns about packages with known problems?**
- [ ] Yes, tool: ______ (examples: Dependabot, Renovate, OSV-Scanner, Snyk)
- [ ] No ❌

**B2.9 `⏳ Medium · Engineer` What is your rule for adding a NEW package?** (tick all that you really do)
- [ ] A human checks the package name is spelled right
- [ ] Check it is real, popular, and maintained
- [ ] Check when it was first published (very new = suspicious)
- [ ] Check what it runs when installing (install scripts)
- [ ] Only use packages from approved sources (registries)
- [ ] A second person approves

**B2.10 `🧱 Long · Engineer` 🟡 Do you use a private or "mirror" source for packages, rather than downloading from anywhere?**
- [ ] Yes: ______   - [ ] No

**B2.11 `⏳ Medium · Engineer` 🟡 Are your package names protected against "confusion" attacks?** (an attacker publishes a public package with the same name as your private one)
- [ ] Yes, how: ______   - [ ] No ❌   - [ ] N/A

**B2.12 `⏳ Medium · Legal` How do you check licenses?**
👉 ANSWER (tool or person):

### 2C. Protect the build machine (CI/CD)

**B2.13 `⚡ Quick · Engineer` What system builds your software automatically?**
👉 ANSWER (name):

**B2.14 `⏳ Medium · Engineer` Does the build run only from trusted code, and NOT from random outside contributors' changes with secrets available?**
- [ ] Yes
- [ ] No ❌
- [ ] UNKNOWN ❓

> **OWASP CI/CD Top 10 link:** This is the "poisoned pipeline" risk (CICD-SEC-4).

**B2.15 `⏳ Medium · Engineer` Do build jobs get only the permissions they truly need?**
- [ ] Yes (describe): ______
- [ ] No ❌

**B2.16 `⏳ Medium · Engineer` Are outside add-ons used in your build pinned to an exact version (not "latest")?**
- [ ] Yes   - [ ] No ❌   - [ ] N/A

**B2.17 `⚡ Quick · Engineer` Are build logs kept for at least ___ days, and do they hide secrets?**
👉 ANSWER:

**B2.18 `⚡ Quick · Engineer` 🟡 Is each build done in a fresh, throwaway environment?**
- [ ] Yes   - [ ] No

**B2.19 `🧱 Long · Engineer` 🔴 Can you prove, for any release, exactly which source code and which steps made it? (build "provenance")**
- [ ] Yes, produced automatically by: ______
- [ ] No

### 2D. Automatic safety checks while building

| Check | Tool name | Runs on every change? (Y/N) | Blocks the release if it fails? (Y/N) |
|---|---|---|---|
| Scan our code for mistakes (SAST) | | | |
| Scan packages for known problems (SCA) | | | |
| Scan for leaked secrets | | | |
| Scan containers / images (if used) | | | |
| Scan infrastructure settings (if used) | | | |
| Automated tests | | | |

### Stage 2 Checklist
- [ ] MFA on for all (B2.1)
- [ ] Main branch protected (B2.2)
- [ ] Access list correct and current (B2.3, B2.4)
- [ ] Secret scanning on (B2.6)
- [ ] Lock files in place (B2.7)
- [ ] Vulnerability warnings on (B2.8)
- [ ] New-package rule being followed (B2.9)
- [ ] Build protected (B2.14 to B2.17)
- [ ] 🟡 Fresh build environment (B2.18)
- [ ] 🔴 Provenance produced (B2.19)
- [ ] Safety checks table filled (2D)

### 🚪 GATE 2 DECISION
| Result | Tick |
|---|---|
| ✅ PASS | [ ] |
| ❌ FAIL (list): | [ ] |
| ⚠️ EXCEPTION (see Part F) | [ ] |

Decided by: ______ Date: ______

---

## STAGE 3: REVIEW AND TEST (checking the work before release)

**Goal in one sentence:** Make sure every change was looked at by a second pair of eyes and tested.

**B3.1 `⏳ Medium · Engineer` What does a "code review" look like on your team?** (who reviews, how fast, what they look for)
👉 ANSWER:

**B3.2 `⏳ Medium · Engineer` Reviewer checklist. Does the reviewer confirm each of these for every change?** (tick what is required)
- [ ] The change does what the request says (nothing extra)
- [ ] No passwords, keys, or personal data in the change
- [ ] No new package added without approval
- [ ] No changes to build or release files without extra approval
- [ ] Tests were added or updated
- [ ] If AI wrote it: the human understands it and has said so (see Part C)

**B3.3 `⚡ Quick · Owner` Special rule: changes to build files, release files, or permissions need approval from: ______ (name or group).**

**B3.4 `⚡ Quick · Engineer` Is the person who wrote a change ever the only person who approves it?**
- [ ] Never (good)
- [ ] Sometimes ❌

**B3.5 `⏳ Medium · Engineer` Testing: what kinds of tests run before release?** (tick all)
- [ ] Unit tests
- [ ] Integration tests
- [ ] Security tests (SAST / dependency / secrets)
- [ ] 🟡 Dynamic tests of the running app (DAST)
- [ ] 🔴 Penetration test by an outside expert (date: ______)
- [ ] Manual "try to break it" session

**B3.6 `⏳ Medium · Security` What happens to problems found?** (use this table)

| Severity | Examples | Must be fixed before release? | Max days to fix |
|---|---|---|---|
| Critical | Customers' data exposed; bad code in release | Yes | |
| High | Serious flaw, hard to exploit | Yes (or written exception) | |
| Medium | Limited impact | Decide case by case | |
| Low | Minor | No | |

**B3.7 `⏳ Medium · Engineer` 🟡 Are the "list of ingredients" (SBOM) files generated and checked for completeness for this version?**
- [ ] Yes, file name: ______
- [ ] No ❌

**B3.8 `⏳ Medium · Legal` Did you review the licenses of everything inside this version?**
- [ ] Yes, notes: ______   - [ ] No

**B3.9 `⏳ Medium · Security` 🔴 Did an independent person (not the builder) review the release plan?**
- [ ] Yes, name: ______   - [ ] No

### Stage 3 Checklist
- [ ] Review rules written and followed (B3.1 to B3.4)
- [ ] Tests run and results saved (B3.5)
- [ ] All Critical and High problems closed or excepted (B3.6)
- [ ] 🟡 SBOM generated and checked (B3.7)
- [ ] Licenses reviewed (B3.8)
- [ ] 🔴 Independent review done (B3.9)

### 🚪 GATE 3 DECISION
| Result | Tick |
|---|---|
| ✅ PASS | [ ] |
| ❌ FAIL (list): | [ ] |
| ⚠️ EXCEPTION (see Part F) | [ ] |

Decided by: ______ Date: ______

---

## STAGE 4: RELEASE (sealing the box)

**Goal in one sentence:** Ship software that is signed, traceable, and easy to roll back.

**B4.1 `⏳ Medium · Engineer` How exactly does a release happen?** (step by step, who clicks what)
👉 ANSWER:

**B4.2 `⚡ Quick · Owner` Who is allowed to release? How many people must approve?**
👉 ANSWER:

**B4.3 `⏳ Medium · Engineer` Are release files signed so customers can check they are real?**
- [ ] Yes, method: ______ (where customers can check: ______)
- [ ] No ❌

**B4.4 `⚡ Quick · Engineer` Where are the final files stored, and who can change them after release?**
👉 ANSWER (name, "nobody" is a good answer):

**B4.5 `⚡ Quick · Engineer` Are the final files protected from being replaced after publishing?**
- [ ] Yes (versions are fixed / immutable)
- [ ] No ❌

**B4.6 `⚡ Quick · Engineer` What accompanies every release?** (tick all that you produce)
- [ ] List of ingredients (SBOM)
- [ ] Signature
- [ ] Build record (provenance)
- [ ] Release notes (plain language)
- [ ] Known-issues list
- [ ] Security fixes mentioned clearly

**B4.7 `⏳ Medium · Engineer` Can you "undo" a release quickly?** (rollback)
- [ ] Yes, takes about ___ minutes. Practiced on: ______
- [ ] No ❌

**B4.8 `⚡ Quick · Engineer` 🟡 Do you release to a small group first (a "canary" or "staged rollout")?**
- [ ] Yes, ___% first
- [ ] No

**B4.9 `⏳ Medium · Engineer` How do customers receive updates, and can attackers fake an update?**
👉 ANSWER (how updates are checked and signed):

**B4.10 `⏳ Medium · Security` Are release keys backed up safely, and what if one is lost or stolen?**
👉 ANSWER (plan):

**B4.11 `⏳ Medium · Engineer` 🔴 Is every release automatically blocked if signing, SBOM, or provenance is missing?**
- [ ] Yes   - [ ] No

### Stage 4 Checklist
- [ ] Release steps written (B4.1, B4.2)
- [ ] Release is signed (B4.3)
- [ ] Final files protected (B4.4, B4.5)
- [ ] Release package complete (B4.6)
- [ ] Rollback tested (B4.7)
- [ ] Key plan written (B4.10)
- [ ] 🔴 Automatic block on missing proof (B4.11)

### 🚪 GATE 4 DECISION
| Result | Tick |
|---|---|
| ✅ PASS | [ ] |
| ❌ FAIL (list): | [ ] |
| ⚠️ EXCEPTION (see Part F) | [ ] |

Decided by: ______ Date: ______

---

## STAGE 5: LAUNCH (first customers arrive)

**Goal in one sentence:** Be ready to notice and fix problems within hours, not weeks.

**B5.1 `⚡ Quick · Product` Launch date and what "launch" means for you.**
👉 ANSWER:

**B5.2 `⏳ Medium · Engineer` Monitoring: how will you know something is wrong?** (tick all that are live)
- [ ] Alerts for errors / crashes
- [ ] Alerts for new known problems in our ingredients (SBOM watching)
- [ ] Alerts for strange logins or changes to code, build, or release settings
- [ ] Alerts for leaked secrets
- [ ] Customer report channel (email or form)

**B5.3 `⚡ Quick · Owner` Who is "on call" during launch week? (name, phone or chat, backup)**
👉 ANSWER:

**B5.4 `⚡ Quick · Security` Is the "if something goes wrong" plan (Part D) written, shared, and practiced at least once?**
- [ ] Yes, practiced on: ______
- [ ] No ❌

**B5.5 `⚡ Quick · Security` Is a public security page and contact available?** (for example `SECURITY.md` and a "Report a problem" email)
- [ ] Yes, link: ______   - [ ] No ❌

**B5.6 `⏳ Medium · Product` What do you tell customers about your security?** (claims must be true, and have evidence)

| Claim in marketing / website | Evidence it is true |
|---|---|
| | |

> **Rule:** If there is no evidence, remove the claim.

**B5.7 `⚡ Quick · Product` 🟡 If customers ask for your security paperwork (questionnaires, SBOM), who answers and how fast?**
👉 ANSWER:

**B5.8 `⏳ Medium · Legal` 🔴 EU customers: is the vulnerability-reporting process ready?** (The EU CRA requires manufacturers to report actively exploited vulnerabilities and severe incidents on a staged 24-hour / 72-hour / final-report schedule. These duties started **11 September 2026**. Most other CRA duties apply from **11 December 2027**.)
- [ ] Yes, process owner: ______
- [ ] No ❌   - [ ] Not applicable (no EU customers)

> Not legal advice. Ask a lawyer to confirm which duties apply to you.

### Stage 5 Checklist
- [ ] Monitoring live (B5.2)
- [ ] On-call named (B5.3)
- [ ] Response plan practiced (B5.4)
- [ ] Public contact page live (B5.5)
- [ ] Marketing claims checked (B5.6)
- [ ] 🟡 Paperwork owner named (B5.7)
- [ ] 🔴 EU reporting ready (B5.8)

### 🚪 GATE 5 DECISION (LAUNCH GO / NO-GO)
| Result | Tick |
|---|---|
| ✅ GO | [ ] |
| ❌ NO-GO (list): | [ ] |
| ⚠️ EXCEPTION (see Part F) | [ ] |

Decided by: ______ Date: ______

---

## STAGE 6: FIRST 500 CUSTOMERS (growing safely)

**Goal in one sentence:** Keep everything above true while you grow, and fix problems fast.

**B6.1 `⚡ Quick · Product` Customer count tracking** (update at each milestone)

| Milestone | Date reached | Open security problems at that time | New things we changed because of growth |
|---|---|---|---|
| 10 customers | | | |
| 50 customers | | | |
| 100 customers | | | |
| 250 customers | | | |
| 500 customers | | | |

**B6.2 `⚡ Quick · Owner` Monthly health check. Answer each month (copy this block each time).**

```
Month: ______
- Tools with 2-step login still all ON?                 [ ] Yes [ ] No
- Access list reviewed (leavers removed)?               [ ] Yes [ ] No
- Dependency problems older than the allowed days?      Count: ___
- Releases this month: ___   Signed: ___   With SBOM: ___
- Secrets found in code: ___   Fixed in time: ___
- AI-assisted changes reviewed by a human: ___ of ___
- Security reports from outsiders: ___   Answered in time: ___
- Practice drill done this quarter?                     [ ] Yes [ ] No
Notes / actions (name + date):
```

**B6.3 `⚡ Quick · Engineer` How fast do you fix problems now?**

| Severity | Target time to fix | Actual average last 3 months |
|---|---|---|
| Critical | | |
| High | | |

**B6.4 `⚡ Quick · Engineer` Do you keep SBOMs for EVERY past version still in use by customers?**
- [ ] Yes   - [ ] No ❌

**B6.5 `⚡ Quick · Product` How long will you support each version with security fixes, and do customers know?**
👉 ANSWER:

**B6.6 `⚡ Quick · Owner` Have you added any NEW tools, AI helpers, or contractors since launch? Were they approved (B0.5)?**
👉 ANSWER (list):

**B6.7 `⏳ Medium · Engineer` 🟡 Scorecard check: run the OpenSSF Scorecard (or similar) on your repository and record the result.**
👉 ANSWER (date, score, 3 lowest checks, plan):

**B6.8 `🧱 Long · Legal` 🔴 Audit readiness: Do you have the evidence a SOC 2 / ISO 27001 auditor would ask for? (Part E mapping)**
- [ ] Yes   - [ ] Partly   - [ ] No

**B6.9 `⏳ Medium · Owner` What would you change next, based on what you learned in the first 500 customers?**
👉 ANSWER (top 3):

### Stage 6 Checklist (before declaring "first 500 customers done")
- [ ] Monthly health checks done every month (B6.2)
- [ ] No Critical problem open beyond the allowed days (B6.3)
- [ ] SBOMs kept for all live versions (B6.4)
- [ ] Support period shared with customers (B6.5)
- [ ] New tools approved (B6.6)
- [ ] Lessons written (B6.9)

### 🚪 GATE 6 DECISION (Review at 500 customers)
| Result | Tick |
|---|---|
| ✅ Healthy: continue as is | [ ] |
| 🟡 Needs work (list): | [ ] |
| ❌ Pause growth until fixed | [ ] |

Decided by: ______ Date: ______

---

# PART C: AI-DRIVEN DEVELOPMENT RULES (fill at the start, revisit at every gate)

> **Why this part exists:** AI helpers now write code, pick packages, and even run commands. That is powerful, but they can also invent packages that do not exist, follow tricked instructions hidden in text, or do too much. Attackers know this and are targeting AI helpers directly. Treat an AI helper like a **very fast new intern**: useful, but it needs supervision.

> ### ⚡ Short path (use this if your level is 🟢 Basic)
> Answer **only** these 6 questions: **C1** (the table), **C2.1**, **C2.2**, **C3.1**, **C3.2**, **C3.4**.
> Mark all other C questions `➖ (level: Basic)`.
> **🟡 Standard** adds: C2.4, C3.3, C3.5, C3.6.
> **🔴 Strict** answers everything, including C4 if your product contains AI.

## C1. Which AI helpers are used? (Be complete)

| AI tool / agent | What it does for us | Who approved it | Can it run commands? | Can it install packages? | Can it push or release code? | Which accounts / keys can it see? |
|---|---|---|---|---|---|---|
| | | | | | | |

## C2. Rules for AI-written code

**C2.1 `⚡ Quick · Engineer` Is every AI-written change reviewed and understood by a human before it merges?**
- [ ] Always   - [ ] Sometimes ❌   - [ ] Never ❌
👉 ANSWER (how do you track which changes are AI-assisted?):

**C2.2 `⚡ Quick · Engineer` When AI suggests a NEW package, do humans verify it is real before installing?** (AI tools sometimes make up package names, and attackers can register those fake names with harmful code. This is called "slopsquatting.")
- [ ] Yes, process: ______   - [ ] No ❌

**C2.3 `⚡ Quick · Engineer` Is AI told which packages and sources are allowed?** (an approved list or private registry)
- [ ] Yes   - [ ] No

**C2.4 `⏳ Medium · Legal` Is any customer data, secrets, or private code sent to an AI service?**
- [ ] No
- [ ] Yes, what is sent and where: ______ Allowed by: ______ Terms checked: [ ] Yes [ ] No

**C2.5 `⏳ Medium · Legal` Who owns responsibility if AI-written code is wrong or copied from someone else?**
👉 ANSWER (name, and legal review date for code licenses):

## C3. Rules for AI agents that act on their own

**C3.1 `⚡ Quick · Engineer` What is the MOST an AI agent is allowed to do without asking a human?** (tick the highest allowed)
- [ ] Read files only
- [ ] Edit files in a safe copy
- [ ] Run tests
- [ ] Install packages
- [ ] Create change requests (PRs)
- [ ] Merge to main ❌ (not recommended)
- [ ] Release to customers ❌ (not recommended)

**C3.2 `⚡ Quick · Engineer` Does the AI agent run in a sandbox (a safe room) with no access to real secrets?**
- [ ] Yes   - [ ] No ❌

**C3.3 `⏳ Medium · Engineer` Are the AI agent's keys short-lived and limited to one job?**
- [ ] Yes   - [ ] No

**C3.4 `⏳ Medium · Security` "Hidden instructions" risk (prompt injection):** AI agents read text from issues, web pages, emails, and files. Attackers hide instructions inside them.
Do you treat text from outside people (issues, comments, web pages, documents) as **untrusted**, and stop the agent from running risky actions based on it?
- [ ] Yes, how: ______   - [ ] No ❌

**C3.5 `⏳ Medium · Engineer` Is every action an AI agent takes recorded (who, what, when)?**
- [ ] Yes, where: ______   - [ ] No ❌

**C3.6 `⚡ Quick · Owner` What is the "kill switch"? Who can instantly switch the AI agent off, and how?**
👉 ANSWER:

**C3.7 `⏳ Medium · Engineer` Extra tools plugged into AI (such as MCP servers, plugins, skills): who approves them, and are they version-pinned?**
👉 ANSWER (list, approver):

## C4. If AI is INSIDE your product (skip if A9 = No)

**C4.1 `⏳ Medium · Engineer` Which AI models does the product use? (name, version, where it comes from)**

| Model | Version | Source / vendor | License / terms | Checked by | Date |
|---|---|---|---|---|---|
| | | | | | |

**C4.2 `⏳ Medium · Engineer` Do you download model files from public places? Do you check they are what they claim to be (signature or checksum)?**
- [ ] Yes   - [ ] No ❌   - [ ] N/A

**C4.3 `⏳ Medium · Engineer` Do you keep an AI "ingredient list" (AI-BOM: models, datasets, prompts) next to the software one?**
- [ ] Yes, format: ______   - [ ] No

**C4.4 `⏳ Medium · Engineer` Where does training or tuning data come from? Could it have been tampered with?**
👉 ANSWER:

**C4.5 `⏳ Medium · Legal` Can customers' data end up used to train a model? Did customers agree?**
👉 ANSWER:

**C4.6 `⏳ Medium · Product` What happens if the AI vendor changes the model or has an outage or breach?**
👉 ANSWER (fallback plan):

## C5. AI rules checklist (every Gate)
- [ ] All AI helpers are in the table (C1)
- [ ] Human review always happens (C2.1)
- [ ] New packages from AI are verified (C2.2)
- [ ] Agents cannot release or touch real secrets (C3.1, C3.2)
- [ ] Outside text is treated as untrusted (C3.4)
- [ ] Agent actions are logged (C3.5)
- [ ] Kill switch is known (C3.6)
- [ ] 🟡 AI model list is kept up to date (C4.1), if applicable

---

# PART D: "WHAT IF SOMETHING GOES WRONG?" PLAN (fill before Gate 5)

> **Why:** In an emergency nobody thinks clearly. Write the plan now, when you are calm.

**D1. `⏳ Medium · Owner` Who is in the response team?**

| Role | Name | Phone / chat | Backup |
|---|---|---|---|
| Boss of the emergency (incident lead) | | | |
| Technical fixer | | | |
| Person who talks to customers | | | |
| Person who talks to lawyers / regulators | | | |

**D2. `⚡ Quick · Security` What counts as an emergency?** (tick all that apply for you)
- [ ] A poisoned package is found in our ingredients
- [ ] Our build system or accounts may be hacked
- [ ] A secret (key or password) was leaked
- [ ] A customer says our software was changed
- [ ] An AI helper did something it should not have
- [ ] A known problem in our ingredients is being actively attacked

**D3. `⏳ Medium · Security` The first 60 minutes (write what you will do, in order)**
1. Stop: ______ (example: pause releases)
2. Protect: ______ (example: change leaked keys)
3. Find out: ______ (which versions, which customers)
4. Tell: ______ (who must be told, how fast)
👉 ANSWER (your real steps):

**D4. `⏳ Medium · Legal` Clock for telling people (fill what applies to you)**

| Who | When | How |
|---|---|---|
| Our boss / management | within ___ hours | |
| Affected customers | within ___ hours | |
| 🔴 EU authorities (CRA, actively exploited vulnerabilities) | early warning within 24 hours, more details by 72 hours, final report later | Through the official EU reporting platform |
| Other regulators / insurers | | |

> Ask a lawyer to confirm exact duties. This is not legal advice.

**D4a. `⚡ Quick · Security` Which of these must you ALWAYS keep a record of?** (tick the ones you will keep)
- [ ] Time of discovery
- [ ] What was affected
- [ ] What we did and when
- [ ] Who we told and when
- [ ] What we changed to prevent it again

**D5. `⚡ Quick · Engineer` Can you quickly answer: "Which of our releases contain package X?"**
- [ ] Yes (we search our SBOMs in about ___ minutes)
- [ ] No ❌

**D6. `⏳ Medium · Security` Practice drill. Do a pretend emergency at least once a year.**

| Date | What we practiced | What went wrong | What we fixed |
|---|---|---|---|
| | | | |

**D7. `⚡ Quick · Owner` After an emergency, we write a blame-free summary within ___ days. Where do they live?**
👉 ANSWER:

---

# PART D2: PRODUCT-TYPE ADD-ONS (fill ONLY the modules that match your answer to A2)

> Skip every module that does not match your product. Mark the whole module `➖ NOT APPLICABLE (not this product type)`.

## Module M1: Mobile apps (iPhone / Android)

**M1.1 `⚡ Quick · Owner` Who holds the app-store developer accounts, and is 2-step login on?**
👉 ANSWER (names, accounts):

**M1.2 `⏳ Medium · Engineer` Where are app signing keys / certificates kept? Who can use them? What if they are lost?**
👉 ANSWER:

**M1.3 `⏳ Medium · Engineer` Are third-party SDKs (ready-made add-ons like ads or analytics) listed with version, owner, and what data they collect?**

| SDK name | Version | What data it collects | Approved by |
|---|---|---|---|
| | | | |

**M1.4 `⚡ Quick · Engineer` Does every app-store build come from your automated build, not from a developer's laptop?**
- [ ] Yes   - [ ] No ❌

**M1.5 `⏳ Medium · Engineer` Do you check the final app file for hidden secrets (keys inside the app)?**
- [ ] Yes   - [ ] No ❌

**M1.6 `⚡ Quick · Engineer` Can you force old, unsafe app versions to update? How?**
👉 ANSWER:

## Module M2: Containers, cloud images, and infrastructure files

**M2.1 `⏳ Medium · Engineer` What base images do you start from, and are they from trusted sources and pinned to an exact version?**
👉 ANSWER:

**M2.2 `⚡ Quick · Engineer` Are images scanned for known problems before they are stored?**
- [ ] Yes, tool: ______   - [ ] No ❌

**M2.3 `⏳ Medium · Engineer` Are images signed, and does the cloud accept only signed images?**
- [ ] Yes   - [ ] No

**M2.4 `⚡ Quick · Engineer` Who can push images to your registry? Is 2-step login on?**
👉 ANSWER:

**M2.5 `⚡ Quick · Engineer` Do containers run with the fewest permissions possible (not as "admin/root")?**
- [ ] Yes   - [ ] No ❌   - [ ] UNKNOWN ❓

**M2.6 `⏳ Medium · Engineer` Are infrastructure files (Terraform, Kubernetes settings, etc.) reviewed like code and scanned for risky settings?**
- [ ] Yes   - [ ] No

**M2.7 `⚡ Quick · Engineer` Is there a list of ingredients (SBOM) for each image?**
- [ ] Yes   - [ ] No

## Module M3: Web apps and APIs

**M3.1 `⏳ Medium · Engineer` Are outside scripts loaded in your web pages (ads, chat, analytics) listed and approved?**
👉 ANSWER:

**M3.2 `⚡ Quick · Engineer` Do you have rules on which outside sites your web pages may load from?** (Content Security Policy)
- [ ] Yes   - [ ] No

**M3.3 `⚡ Quick · Engineer` Are API keys given to customers or partners limited, rotatable, and revocable?**
- [ ] Yes   - [ ] No

## Module M4: Libraries and packages that OTHER people install

**M4.1 `⚡ Quick · Engineer` Is your package published through a trusted automated process, not from a laptop?**
- [ ] Yes   - [ ] No ❌

**M4.2 `⚡ Quick · Engineer` Do you protect your publishing account and package name (2-step login, limited maintainers)?**
- [ ] Yes   - [ ] No ❌

**M4.3 `⚡ Quick · Engineer` Does your package avoid scripts that run automatically at install time? If it has them, are they justified in the docs?**
👉 ANSWER:

**M4.4 `⚡ Quick · Engineer` Do you publish a signed release, SBOM, and clear security contact?**
- [ ] Yes   - [ ] Partly   - [ ] No

## Module M5: Devices with software inside (firmware and updates)

**M5.1 `⚡ Quick · Engineer` Can the device accept ONLY signed updates?**
- [ ] Yes   - [ ] No ❌

**M5.2 `⚡ Quick · Engineer` Can a bad update be undone safely?**
- [ ] Yes   - [ ] No ❌

**M5.3 `⚡ Quick · Product` How long will you provide security updates, and is it written on the box or website?**
👉 ANSWER:

**M5.4 `⚡ Quick · Engineer` Is there a list of ingredients (SBOM) for the firmware?**
- [ ] Yes   - [ ] No

### Add-on checklist
- [ ] Every module that matches A2 is answered
- [ ] Every module that does not match is marked NOT APPLICABLE

---

# PART E: STANDARDS MAP (OPTIONAL APPENDIX, for auditors, lawyers, and enterprise customers)

> **Beginner note:** You do **not** need to fill this part to be safe. **Skip it unless someone asks.** It shows which of your answers prove which outside rule. Fill the "Where is our proof?" column only when needed.
> **Part F (sign-off) can be completed without Part E.**
> Standards change. Re-check the latest version before you promise compliance. Mappings below are a guide, not legal or audit advice.

| Topic | Questions in this doc | SLSA | NIST SSDF (SP 800-218) | EU CRA | OWASP CI/CD Top 10 | OpenSSF Scorecard checks | SOC 2 / ISO 27001 (guide) | Where is our proof? |
|---|---|---|---|---|---|---|---|---|
| Roles and responsibility | B0.1, A10 | n/a | PO (prepare the organization) | Manufacturer duties | n/a | n/a | SOC 2 CC1 (control environment); ISO A.5.2 | |
| Who can change code | B2.1 to B2.4 | Source integrity ideas | PS (protect the software) | Secure by design | CICD-SEC-2 (identity and access), CICD-SEC-5 | Branch-Protection, Code-Review | SOC 2 CC6; ISO A.8.2, A.8.3 | |
| Code review | B3.1 to B3.4 | n/a | PW (produce well-secured software) | Secure by design | CICD-SEC-1 (flow control) | Code-Review | SOC 2 CC8.1; ISO A.8.32 | |
| Dependencies | B1.1, B1.2, B2.7 to B2.12 | n/a | PW.4 (reuse secure software) | SBOM and vulnerability handling | CICD-SEC-3 (dependency chain abuse) | Pinned-Dependencies, Dependency-Update-Tool, Vulnerabilities | SOC 2 CC9.2 (vendors); ISO A.5.19 to A.5.22 | |
| Build system safety | B2.13 to B2.19 | Build L1 to L3 | PS, PW | Secure by design | CICD-SEC-4, 5, 7, 8 | Dangerous-Workflow, Token-Permissions | SOC 2 CC6, CC7; ISO A.8.25, A.8.31 | |
| Secrets | B1.4, B2.6 | n/a | PS | Secure by design | CICD-SEC-6 (credential hygiene) | n/a (secret scanning is separate) | SOC 2 CC6.1; ISO A.8.24 | |
| Testing | B2D, B3.5 to B3.6 | n/a | PW.7, PW.8 | Essential requirements | n/a | SAST, Fuzzing, CI-Tests | SOC 2 CC7.1; ISO A.8.29 | |
| SBOM (ingredient list) | B1.9, B3.7, B4.6, B6.4 | n/a | PS.3, PW.4 | SBOM required in technical documentation | CICD-SEC-9 (artifact integrity) | n/a | SOC 2 CC9.2; ISO A.5.21 | |
| Signing and provenance | B1.7, B1.8, B2.19, B4.3 to B4.5 | Build L2, L3 | PS.2, PS.3 | Integrity of product | CICD-SEC-9 | Signed-Releases | SOC 2 CC8.1; ISO A.8.24 | |
| Releases and updates | B4.1 to B4.11 | Build track | PS.3, PW.10 (draft v1.2 adds update-related practices) | Security updates during support period | CICD-SEC-1, 9 | Packaging, Signed-Releases | SOC 2 CC8.1; ISO A.8.32 | |
| Logging and monitoring | B2.17, B5.2 | n/a | RV.1 | Vulnerability handling | CICD-SEC-10 (logging and visibility) | n/a | SOC 2 CC7.2; ISO A.8.15, A.8.16 | |
| Outside reports and fixing | B1.10, B5.5, D-part | n/a | RV (respond to vulnerabilities) | Vulnerability disclosure and reporting | n/a | Security-Policy | SOC 2 CC7.3 to CC7.5; ISO A.5.24 to A.5.27 | |
| AI helpers and AI in product | Part C | emerging area | emerging; NIST SP 800-218A for AI model development | Depends on product | emerging | n/a | SOC 2 / ISO: covered under vendor and change management | |

### Key dates (checked October 2026; verify before relying)

| Date | What | Why it matters to you |
|---|---|---|
| 10 Dec 2024 | EU CRA entered into force | Start preparing if you sell to the EU |
| 11 Sep 2026 | CRA: manufacturers must report actively exploited vulnerabilities and severe incidents | Response plan must exist (Part D) |
| 11 Dec 2027 | CRA: main obligations apply (SBOM, conformity, support-period updates) | Make SBOM and updates part of every release now |
| SSDF v1.2 | NIST published a public draft (SP 800-218r1) in Dec 2025 | Check whether it is final when you read this |
| SLSA | Current spec v1.1 (Build track L1 to L3) | Pick your target in B1.8 |

---

# PART F: SCORECARD, EXCEPTIONS, AND SIGN-OFF

## F1. Quick score (count your ✅)

| Stage | Total questions that apply | ✅ | 🟡 | ❌ | ❓ | Score (✅ divided by total) |
|---|---|---|---|---|---|---|
| Part A | | | | | | |
| Stage 0 | | | | | | |
| Stage 1 | | | | | | |
| Stage 2 | | | | | | |
| Stage 3 | | | | | | |
| Stage 4 | | | | | | |
| Stage 5 | | | | | | |
| Stage 6 | | | | | | |
| Part C (AI) | | | | | | |
| Part D | | | | | | |
| Part D2 (only modules that apply) | | | | | | |

**How to read your score:**
- **90% or more ✅ and no ❌ on a "must fix" item** → Healthy
- **70% to 89%** → Needs work; set dates for each ❌
- **Below 70%** → Stop and fix the basics before moving on

## F2. Exceptions (when you must move on with something not finished)

> Allowed only if a named person accepts the risk in writing, with an end date. Never leave an exception without an expiry.

| # | Question ID | What is not done | Risk if we continue (plain words) | Plan to fix | Fix-by date | Approved by (name) | Approval date |
|---|---|---|---|---|---|---|---|
| E1 | | | | | | | |

## F3. Top 5 open items (everything ❌ or ❓ goes here with an owner and date)

| # | Item | Owner | Due date | Status |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

## F4. Final launch sign-off (before Gate 5)

| Role | Name | Decision (GO / NO-GO) | Date | Signature or approval link |
|---|---|---|---|---|
| Document owner | | | | |
| Engineering lead | | | | |
| Security contact | | | | |
| Product owner | | | | |
| Business / legal (if Strict) | | | | |

## F5. Evidence list (every proof you mention, in one place)

| Evidence ID | What it proves | Question ID | File name or link | Date captured | Who captured it |
|---|---|---|---|---|---|
| EV-001 | | | | | |

---

# PART G: GLOSSARY (hard words, made simple)

| Word | Simple meaning |
|---|---|
| **Supply chain (software)** | Everything that goes into making and delivering your software: code, other people's packages, tools, machines, and people |
| **Dependency / package** | Code written by someone else that your product uses, like buying ready-made flour |
| **SBOM** | "Software Bill of Materials": the ingredient list of your software |
| **CI/CD / pipeline** | The robot assembly line that tests, builds, and ships your software automatically |
| **Build** | The step where code is turned into the final app |
| **Artifact** | The finished file you give to customers |
| **Registry** | A warehouse where packages or finished software are stored |
| **Provenance** | A receipt that says "this exact file was made from this exact code, by this machine, on this date" |
| **Signing** | A tamper-proof seal on your software that proves it came from you |
| **SLSA** | A ladder of levels that shows how well your build process is protected (we use Build levels 1 to 3) |
| **NIST SSDF** | A US government guide to safe software-making habits |
| **EU CRA** | A European law that makes companies that sell digital products responsible for their security |
| **OWASP** | A non-profit community that publishes security lists and guides |
| **Scorecard (OpenSSF)** | A free tool that grades the safety habits of a code project |
| **MFA / 2-step login** | Logging in with a password plus a second proof, like a code on your phone |
| **Branch protection** | A lock that stops people from changing the main code without review |
| **Pull request (PR)** | A "please check my change" request before it joins the main code |
| **Secret** | A password, key, or token that must never be public |
| **Vulnerability** | A weak spot that an attacker can use |
| **CVE** | A public ID number for a known vulnerability |
| **SAST / SCA / DAST** | Three kinds of automatic checks: scan your code, scan other people's packages, and test the running app |
| **Typosquatting** | A fake package with a name almost like a real one |
| **Slopsquatting** | A fake package named after something an AI helper invented |
| **Dependency confusion** | Tricking a build into downloading a public package instead of your private one |
| **Prompt injection** | Hidden instructions in text that trick an AI into doing the wrong thing |
| **MCP / plugin** | An add-on that gives an AI helper extra abilities |
| **Sandbox** | A safe room where a tool can work without touching anything important |
| **Rollback** | Going back to the last safe version |
| **Least access** | Giving each person or tool only the permissions they truly need |
| **Threat modeling** | A "what could go wrong?" brainstorm before you build |
| **Canary / staged rollout** | Giving a new version to a few customers first, to catch problems early |
| **Incident** | A security emergency |
| **PSIRT** | The team that handles security problems in a product |
| **AI-BOM** | An ingredient list for AI parts: models, data, prompts |

---

# PART H: HOW TO REUSE THIS TEMPLATE ACROSS PROJECTS (for the template owner)

1. **Copy** this file for each new project. Name it `Software_Supply_Chain_Security.md` inside that project's "Code review and release engineering" folder.
2. **Do not edit the original.** Keep it as the master. Fix master problems in the Template Change Log below.
3. **Fill the Document Control table** first, then Part A.
4. **Review cadence:** every Stage Gate, every quarter, and whenever a standard or law changes.
5. **Never store secrets here.**
6. **Audit by sampling:** once per quarter, pick 5 answers at random and confirm the Evidence is real.

### Template change log (master only)

| Version | Date | Change | Author |
|---|---|---|---|
| 0.1 | 2026-10-18 | First draft for review | |
| 0.2 | 2026-10-18 | Added RACI (A13), supplier checks (1B), Stage 2 "Big 8" shortcut, AI short path, product-type add-ons (D2), standards map made optional, effort and role tags, worked example (Part I) | |

---

# PART I: WORKED EXAMPLE (FICTIONAL, to show what "good" looks like)

> **This is a made-up project called "PlantPal"** (an app that reminds people to water their plants). Every name, link, and date below is invented. **Do not copy these answers.** Copy the *style*: short, specific, with named people, dates, and proof.

## Example Document Control

| Field | 👉 Answer |
|---|---|
| Project name | PlantPal |
| Project code / ID | PRJ-0042 |
| One-sentence description | A phone app and website that reminds you when to water each of your plants. |
| Document owner | Priya Shah |
| Security contact | Sam Lee, sam@plantpal.example |
| Date started | 2026-10-18 |
| Current stage | 2 (Build) |
| Template version used | 0.2 |

## Example Part A answers

**A2. Product type:** [x] Mobile app  [x] Website or web app  [x] API or backend service
**A3. Customers:** [x] European Union. **Note:** EU Cyber Resilience Act may apply, so we mark every 🔴 question that touches EU duties as required.
**A4. Data:** [x] Names / emails. No payment data (payments handled by an outside payment company).
**A5. Worst case:** [x] Medium. *"A poisoned update could steal users' emails. No money or health data is involved."*
**A11. Level:** [x] 🟡 Standard (real customers, some personal data), with 🔴 for EU reporting (B5.8) and Part D4.

**A6. Tools (excerpt)**

| Purpose | Tool | Account owner | 2-step login? |
|---|---|---|---|
| Stores code | GitHub (org "plantpal-app") | Priya Shah | Y |
| Builds and tests | GitHub Actions | Sam Lee | Y |
| Hosting | Example Cloud Provider | Priya Shah | Y |
| Secrets | Team password manager | Priya Shah | Y |
| AI coding helpers | Coding assistant "Helper-X" | Lee Tran | N ← ❌ fix before Gate 1 |

**A13. RACI (excerpt)**

| Stage | R | A | C | I |
|---|---|---|---|---|
| 2 Build | Lee Tran | Sam Lee | Priya Shah | Ana Cruz |
| 4 Release | Lee Tran | Priya Shah | Sam Lee | Ana Cruz |

## Example Stage 2 answers (the "Big 8")

**B2.1 `⚡ Quick · Engineer` 2-step login on everything?**
👉 ANSWER: Some. All 4 people use it on GitHub and the cloud. Helper-X account does not yet. Owner: Lee Tran, due 2026-10-25.
Evidence: screenshot `github-2fa-report-2026-10-18.png`
Status: 🟡

**B2.2 `⚡ Quick · Engineer` Branch protection?**
👉 ANSWER: No one can push straight to `main`. Every change needs 1 approval from someone other than the author.
Evidence: screenshot `branch-protection-settings.png`
Status: ✅

**B2.6 `⏳ Medium · Engineer` Secret scanning?**
👉 ANSWER: Yes, GitHub secret scanning is on. If one is found, Sam Lee is alerted by email and changes the key within 4 hours.
Evidence: link to settings page, test alert on 2026-10-17
Status: ✅

**B2.7 `⚡ Quick · Engineer` Lock files?**
👉 ANSWER: Yes. `package-lock.json` (website) and `Podfile.lock` (iPhone app) are saved in the repository.
Status: ✅

**B2.9 `⏳ Medium · Engineer` New-package rule?**
👉 ANSWER: We tick 5 of 6 boxes. We do **not** yet require a second approver. Plan: add a rule "new package = second approval" by 2026-11-01 (Sam).
Status: 🟡

**B2.14 `⏳ Medium · Engineer` Build runs only trusted code?**
👉 ANSWER: ❓ UNKNOWN. We have not checked whether outside contributors' changes can start builds with secrets. Ask Sam to check the Actions settings by 2026-10-22.
Status: ❓

## Example Part C answers (AI short path)

**C1. AI helpers:** Helper-X (writes code). Approved by Priya on 2026-09-02. Can run commands: **No**. Can install packages: **No** (suggests only). Can push or release: **No**. Sees accounts: none.
**C2.1:** Always. Every change needs a human reviewer who writes "I understand this change" in the review. We mark AI-assisted changes with the label `ai-assisted`.
**C2.2:** Yes. Rule: when AI suggests a new package, Lee checks the registry page (publish date, downloads, owner) before installing.
**C3.1:** Highest allowed: **Create change requests (PRs).**
**C3.4:** Yes. The assistant is not allowed to act on text from issues or web pages without a human approving.

## Example Gate decision

### 🚪 GATE 2 DECISION (PlantPal)
| Result | Tick |
|---|---|
| ✅ PASS | [ ] |
| ❌ FAIL (list): B2.1 (Helper-X login), B2.9 (second approver), B2.14 (unknown) | [x] |
| ⚠️ EXCEPTION | [ ] |

Decided by: Priya Shah. Date: 2026-10-18.
**Result:** We do **not** move to Stage 3 until the three open items are ✅. Each has an owner and a date in F3.

## Example Part F3 (open items)

| # | Item | Owner | Due date | Status |
|---|---|---|---|---|
| 1 | Turn on 2-step login for Helper-X | Lee Tran | 2026-10-25 | 🟡 |
| 2 | Check build trigger settings (B2.14) | Sam Lee | 2026-10-22 | ❓ |
| 3 | Add second approver rule for new packages | Sam Lee | 2026-11-01 | 🟡 |

## What makes the PlantPal answers good (use this as your self-check)

- Every answer has a **name** and a **date** when something is not done.
- Every ✅ has **evidence** (a screenshot name or link).
- The one thing nobody knew is marked **❓ UNKNOWN**, not guessed.
- The gate says **FAIL** honestly, and the fix list has owners.
- No passwords or keys appear anywhere.
