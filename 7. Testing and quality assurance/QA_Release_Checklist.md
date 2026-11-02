# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **Goal:** Decide, with proof, whether your product is safe to launch, and keep it healthy until your first 500 customers.
> **Who can use it:** Anyone. You do not need to be technical. If a word is new, look it up in the **Glossary** (Part 13).

## Step 1. Copy the file
Copy this file into your project's `Testing and quality assurance/` folder. Keep the name `QA_Release_Checklist.md`. Never edit the original template, only your copy.

## Step 2. Fill Part 1 (Release Basics) first
It tells everyone what is being released, who owns each job, and which parts of the checklist apply.

## Step 3. Work through the Parts in order
Each Part is one phase of life: **Build → Test → Staging → Launch Readiness → Go/No-Go → Launch Day → First Week → First 500 Customers.**
Do not skip ahead. Later Parts depend on earlier ones.

## Step 4. Answer every question with ONE of three answers
Replace `☐` with `☒` in exactly one box per row.

| Answer | Meaning | What you must also write |
|---|---|---|
| ☒ **Yes** | I checked it myself and it works | **Proof** (a link, screenshot name, test report, or ticket number) |
| ☒ **No** | I checked it and it does not work, or it is not done | A **ticket/bug number** in Proof |
| ☒ **N/A** | It does not apply to this product | A **short reason** in Proof (e.g. "No mobile app") |

## Step 5. The golden rules (these remove guessing)
1. **Never guess.** If you do not know, leave all boxes empty and write `ASK: <person's name>` in Proof.
2. **No proof = No.** A "Yes" without proof counts as "No."
3. **Blank = No.** Every row must be answered before the Go/No-Go meeting.
4. **🔴 BLOCKER** rows must be **Yes** (or N/A with a reason approved by the Release Owner) before launch. No exceptions.
5. **🟡 IMPORTANT** rows may be "No" only if a ticket exists and the Release Owner approves it in Part 11.
6. **⚪ NICE** rows are good practice. A "No" is fine but must be written down.
7. **Test the real thing.** Test the release candidate (the exact version you plan to ship), not an older one.
8. **Write dates as** `YYYY-MM-DD` (example: 2026-10-17).
9. **Do not delete rows.** Mark them N/A instead, so the next person sees the row was considered.

## Step 6. A filled-in example row

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| WEB-01 🔴 | Can a new person sign up from start to finish? | ☒ | ☐ | ☐ | Screen recording `signup-2026-10-17.mp4`, test run #482 |

## Step 7. When you are done
1. Count your results in **Part 5**.
2. Hold the **Go/No-Go meeting** and sign.
3. Save the file and tag it with the release version (example: `QA_Release_Checklist_v1.4.0.md`).

---

# QA RELEASE CHECKLIST

**Template version:** 1.1 | **Last updated:** 2026-10-17 | **Applies to:** Web apps / SaaS, Mobile apps, APIs, AI-powered features, and data pipelines, built with AI-assisted development

---

## PART 1. RELEASE BASICS (fill this first)

### 1.1 What are we releasing?

| Question | Your answer |
|---|---|
| Project name | |
| Release name / version (example: v1.0.0) | |
| Release type (pick one): First launch / Major update / Minor update / Hotfix | |
| Planned launch date (YYYY-MM-DD) | |
| Planned launch time and time zone | |
| One sentence: what does this product do and for whom? | |
| What is new or changed in this release? (3 bullets max) | |
| Link to requirements / product spec | |
| Link to code repository and release branch/tag | |
| Link to staging (test) website or build | |
| Link to production (live) website or app store page | |
| Link to bug tracker / ticket board | |

### 1.2 Which parts apply to this release?

| Part | Applies? | If not, why? |
|---|---|---|
| Web app / SaaS (Section 3.1) | ☐ Yes ☐ No | |
| Mobile app (Section 3.2) | ☐ Yes ☐ No | |
| Payments / subscriptions (Section 3.7) | ☐ Yes ☐ No | |
| Users' personal data is collected (Section 3.6) | ☐ Yes ☐ No | |
| AI agents wrote or changed code in this release (Section 2.2) | ☐ Yes ☐ No | |
| The product has AI-powered features, such as a chatbot or smart suggestions (Section 3.8) | ☐ Yes ☐ No | |
| The product has an API or backend service that others connect to (Section 3.9) | ☐ Yes ☐ No | |
| Accessibility deep-dive or multiple languages/regions (Section 3.10) | ☐ Yes ☐ No | |
| The product collects usage data, analytics, or reports (Section 3.11) | ☐ Yes ☐ No | |

### 1.3 Who does what? (Every role needs a name. One person may hold several roles.)

| Role | What this person is responsible for | Name | Contact (email/chat) | Backup person |
|---|---|---|---|---|
| **Release Owner** | Makes the final Go/No-Go call; owns this file | | | |
| **Product Owner** | Confirms the product does what customers need | | | |
| **Engineering Lead** | Confirms the code, build, and deploy are ready | | | |
| **QA Lead** | Confirms testing is complete and honest | | | |
| **Security Owner** | Confirms security and privacy checks | | | |
| **Support Lead** | Confirms customers can get help | | | |
| **On-Call Engineer (launch week)** | Fixes problems fast after launch | | | |

### 1.4 Success targets (write numbers, not feelings)

| Question | Your answer |
|---|---|
| What number of customers counts as success at the end of this checklist? (default: 500) | |
| Target: customers signed up in the first 7 days | |
| Target: percent of new users who finish onboarding | |
| Target: maximum acceptable error rate (example: under 1% of requests) | |
| Target: maximum acceptable page/screen load time (example: under 3 seconds) | |
| Target: maximum time to reply to a support request (example: within 24 hours) | |

---

## PART 2. PHASE 1: BUILD (is the product finished and clean?)

### 2.1 Code and build health

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| BLD-01 🔴 | Is all code for this release merged into the release branch, with nothing half-finished? | ☐ | ☐ | ☐ | |
| BLD-02 🔴 | Does the project build successfully from a clean start (no leftover files)? | ☐ | ☐ | ☐ | |
| BLD-03 🔴 | Did every automated test pass in the last run on the release branch? | ☐ | ☐ | ☐ | |
| BLD-04 🟡 | Did a second person review every code change (pull request)? | ☐ | ☐ | ☐ | |
| BLD-05 🟡 | Are there zero open "critical" or "high" severity bugs for this release? | ☐ | ☐ | ☐ | |
| BLD-06 🟡 | Are the "tests cover enough" targets met? (write the % in Proof; suggested minimum 70% of important code) | ☐ | ☐ | ☐ | |
| BLD-07 🟡 | Has the code been checked by a style/quality tool (linter) with no errors? | ☐ | ☐ | ☐ | |
| BLD-08 🟡 | Are all temporary code, debug messages, and "TODO: remove" notes removed? | ☐ | ☐ | ☐ | |
| BLD-09 🔴 | Is the release version number set correctly (app, API, database, store listing)? | ☐ | ☐ | ☐ | |
| BLD-10 ⚪ | Is the change log (list of what is new) written in plain language? | ☐ | ☐ | ☐ | |

### 2.2 AI-assisted development checks (skip with N/A if no AI wrote code)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| AID-01 🔴 | Did a human read and approve every piece of AI-written code before merging? | ☐ | ☐ | ☐ | |
| AID-02 🔴 | Did you check that every software package/library the AI added is real, trusted, and needed? (AI sometimes invents package names) | ☐ | ☐ | ☐ | |
| AID-03 🔴 | Did you confirm no secrets (passwords, keys, tokens) were pasted into prompts, code, or AI chat logs? | ☐ | ☐ | ☐ | |
| AID-04 🟡 | Does every important AI-written feature have a test written or reviewed by a human? | ☐ | ☐ | ☐ | |
| AID-05 🟡 | Did you run the product and try the feature yourself, not just trust the AI's "it works"? | ☐ | ☐ | ☐ | |
| AID-06 🟡 | Is it recorded which parts were AI-generated (for example in commit messages or the pull request)? | ☐ | ☐ | ☐ | |
| AID-07 🟡 | Did you check that AI-written code does not copy licensed code that conflicts with your license? | ☐ | ☐ | ☐ | |
| AID-08 ⚪ | Are the prompts or agent instructions that built this release saved in the repository? | ☐ | ☐ | ☐ | |

### 2.3 Security basics in the code

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| SEC-01 🔴 | Did an automated scan find zero secrets (keys/passwords) in the code and its history? | ☐ | ☐ | ☐ | |
| SEC-02 🔴 | Did a dependency scan find zero known **critical/high** vulnerabilities? (or each has an approved exception ticket) | ☐ | ☐ | ☐ | |
| SEC-03 🟡 | Did a code security scan (static analysis) find zero **critical/high** issues? | ☐ | ☐ | ☐ | |
| SEC-04 🟡 | Are all software licenses of the libraries you use allowed for commercial use? | ☐ | ☐ | ☐ | |
| SEC-05 🔴 | Do all secrets live in a safe secret store, not in files in the repository? | ☐ | ☐ | ☐ | |

---

## PART 3. PHASE 2: QUALITY ASSURANCE TESTING (does it actually work?)

### 3.0 Test environment

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| ENV-01 🔴 | Are you testing the exact release candidate (same version that will ship)? Write the version in Proof | ☐ | ☐ | ☐ | |
| ENV-02 🟡 | Is the test environment set up like the live one (same settings, similar data size)? | ☐ | ☐ | ☐ | |
| ENV-03 🔴 | Is test data clearly separate from real customer data? | ☐ | ☐ | ☐ | |
| ENV-04 🟡 | Do you have test accounts for every user type (new user, normal user, admin, blocked user)? | ☐ | ☐ | ☐ | |

### 3.1 Web app / SaaS (N/A if no web app)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| WEB-01 🔴 | Can a new person sign up from start to finish? | ☐ | ☐ | ☐ | |
| WEB-02 🔴 | Can a person log in, log out, and reset a forgotten password? | ☐ | ☐ | ☐ | |
| WEB-03 🔴 | Can a person complete the main task of your product (the #1 reason people use it)? | ☐ | ☐ | ☐ | |
| WEB-04 🔴 | Does every important button, link, and form work, with no dead ends or blank pages? | ☐ | ☐ | ☐ | |
| WEB-05 🟡 | Do forms show clear, kind messages when something is typed wrong? | ☐ | ☐ | ☐ | |
| WEB-06 🟡 | Does it work in the latest Chrome, Safari, Firefox, and Edge? (write which you tested) | ☐ | ☐ | ☐ | |
| WEB-07 🟡 | Does it look and work correctly on a phone, a tablet, and a laptop screen? | ☐ | ☐ | ☐ | |
| WEB-08 🟡 | Do empty states (no data yet), loading states, and error pages look friendly? | ☐ | ☐ | ☐ | |
| WEB-09 🟡 | Do emails and notifications the product sends arrive, look correct, and have working links? | ☐ | ☐ | ☐ | |
| WEB-10 🟡 | Does the back button, refresh, and opening a second tab not break anything? | ☐ | ☐ | ☐ | |
| WEB-11 🟡 | Do user roles work (can an ordinary user NOT see admin pages)? | ☐ | ☐ | ☐ | |
| WEB-12 ⚪ | Does the site have a correct title, icon, and share preview (for search and social links)? | ☐ | ☐ | ☐ | |

### 3.2 Mobile app (N/A if no mobile app)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| MOB-01 🔴 | Does a fresh install open, sign up, and complete the main task on a real iPhone? | ☐ | ☐ | ☐ | |
| MOB-02 🔴 | Does a fresh install open, sign up, and complete the main task on a real Android phone? | ☐ | ☐ | ☐ | |
| MOB-03 🔴 | Does the app not crash during a 15-minute normal-use session? | ☐ | ☐ | ☐ | |
| MOB-04 🟡 | Did you test at least one older and one newer OS version, and one small and one large screen? (list devices) | ☐ | ☐ | ☐ | |
| MOB-05 🟡 | Does the app handle bad internet (offline, slow, switching Wi-Fi to mobile data) without losing data? | ☐ | ☐ | ☐ | |
| MOB-06 🟡 | Does the app ask for permissions (camera, location, notifications) only when needed, with a clear reason? | ☐ | ☐ | ☐ | |
| MOB-07 🟡 | Do push notifications arrive and open the right screen? | ☐ | ☐ | ☐ | |
| MOB-08 🟡 | Does updating from the previous version keep the user's data and login? | ☐ | ☐ | ☐ | |
| MOB-09 🟡 | Does the app behave well when interrupted (phone call, switching apps, locking screen, rotating)? | ☐ | ☐ | ☐ | |
| MOB-10 🔴 | Does the app meet current App Store and Google Play rules (privacy labels, data-safety form, age rating, required account-deletion option)? | ☐ | ☐ | ☐ | |
| MOB-11 🔴 | Are the store listing items ready (name, description, screenshots, icon, support link, privacy policy link)? | ☐ | ☐ | ☐ | |
| MOB-12 🟡 | Is the build signed with the correct release keys, and are the keys backed up safely? | ☐ | ☐ | ☐ | |
| MOB-13 🟡 | Was the app submitted for store review early enough (allow several days for review and a possible rejection)? | ☐ | ☐ | ☐ | |

### 3.3 Core testing types

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| TST-01 🔴 | Did you run a **smoke test** (quick check that the most important things work) on the release candidate? | ☐ | ☐ | ☐ | |
| TST-02 🔴 | Did you run a **regression test** (old features still work after the new changes)? | ☐ | ☐ | ☐ | |
| TST-03 🟡 | Did you test the **unhappy paths** (wrong passwords, empty fields, huge files, special characters, double-clicks)? | ☐ | ☐ | ☐ | |
| TST-04 🟡 | Did someone who did NOT build the product try it with no help (a fresh-eyes test)? | ☐ | ☐ | ☐ | |
| TST-05 🟡 | Did you retest every bug that was fixed during this release? | ☐ | ☐ | ☐ | |
| TST-06 🟡 | Are the connections to other services (login providers, email, payments, maps, analytics) tested with real test accounts? | ☐ | ☐ | ☐ | |
| TST-07 ⚪ | Did you test with different languages, dates, time zones, and currencies, if you serve more than one region? | ☐ | ☐ | ☐ | |

### 3.4 Performance and reliability

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| PRF-01 🟡 | Are page/screen load times within the target in Part 1.4? | ☐ | ☐ | ☐ | |
| PRF-02 🔴 | Did a load test with at least **2× your expected busiest hour** pass? (write the number of simulated users) | ☐ | ☐ | ☐ | |
| PRF-03 🟡 | Does the product recover by itself after a short outage of the database or a service it depends on? | ☐ | ☐ | ☐ | |
| PRF-04 🟡 | Are there no signs of slowing down or running out of memory during a long test (1+ hour)? | ☐ | ☐ | ☐ | |
| PRF-05 🟡 | Are limits in place so one user cannot overload the system (rate limits)? | ☐ | ☐ | ☐ | |
| PRF-06 ⚪ | Is the mobile app's battery, data use, and download size acceptable? | ☐ | ☐ | ☐ | |

### 3.5 Security and access

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| SCT-01 🔴 | Is the whole site/API only reachable over secure connections (HTTPS)? | ☐ | ☐ | ☐ | |
| SCT-02 🔴 | Can user A NOT see or change user B's data? (test by trying) | ☐ | ☐ | ☐ | |
| SCT-03 🔴 | Are passwords stored safely (hashed), and does the login block repeated guessing? | ☐ | ☐ | ☐ | |
| SCT-04 🟡 | Did you test common attacks (injecting code into forms, cross-site scripting, broken access)? Use a checklist like OWASP Top 10 | ☐ | ☐ | ☐ | |
| SCT-05 🟡 | Are admin tools protected with a second login step (two-factor) and limited to the right people? | ☐ | ☐ | ☐ | |
| SCT-06 🟡 | Do error messages avoid showing secrets, file paths, or technical details to users? | ☐ | ☐ | ☐ | |
| SCT-07 🟡 | Are uploaded files checked (type, size, safe storage)? | ☐ | ☐ | ☐ | |
| SCT-08 ⚪ | Has an outside expert or tool done a penetration test? (strongly recommended before the first 500 customers) | ☐ | ☐ | ☐ | |

### 3.6 Privacy, legal, and accessibility

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| LGL-01 🔴 | Are the Privacy Policy and Terms of Service published and linked from sign-up and the footer/app? | ☐ | ☐ | ☐ | |
| LGL-02 🔴 | Can a user delete their account and data, and can a user export their data, if the law in your markets requires it? | ☐ | ☐ | ☐ | |
| LGL-03 🔴 | Is consent asked for cookies, tracking, and marketing emails where the law requires it? | ☐ | ☐ | ☐ | |
| LGL-04 🟡 | Do you know exactly what personal data you collect, where it is stored, and who can see it? | ☐ | ☐ | ☐ | |
| LGL-05 🟡 | Do all emails have a working unsubscribe link and your company address? | ☐ | ☐ | ☐ | |
| LGL-06 🟡 | Can a person who uses a keyboard only, or a screen reader, finish sign-up and the main task? | ☐ | ☐ | ☐ | |
| LGL-07 🟡 | Is text readable (good contrast, resizable) and do images have descriptions? | ☐ | ☐ | ☐ | |
| LGL-08 ⚪ | Have you checked rules that apply in your markets (for example GDPR, CCPA, children's privacy)? Name them in Proof | ☐ | ☐ | ☐ | |

### 3.7 Payments and subscriptions (N/A if you do not charge money)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| PAY-01 🔴 | Does a test purchase work from start to finish in the payment provider's **test mode**? | ☐ | ☐ | ☐ | |
| PAY-02 🔴 | Do failed, cancelled, and refunded payments behave correctly and tell the user clearly? | ☐ | ☐ | ☐ | |
| PAY-03 🔴 | Do upgrades, downgrades, cancellations, and renewals charge the right amount at the right time? | ☐ | ☐ | ☐ | |
| PAY-04 🟡 | Do receipts/invoices and taxes appear correctly? | ☐ | ☐ | ☐ | |
| PAY-05 🔴 | Are live payment keys ready, stored safely, and the test keys NOT used in production? | ☐ | ☐ | ☐ | |
| PAY-06 🟡 | Does the product avoid storing raw card numbers? (the payment provider should hold them) | ☐ | ☐ | ☐ | |

### 3.8 AI features inside the product (N/A if the product has no AI-powered features)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| AIF-01 🔴 | Is there a written list of what the AI feature is allowed to do and NOT allowed to do? | ☐ | ☐ | ☐ | |
| AIF-02 🔴 | Did you test at least 50 realistic questions/inputs (include tricky, rude, empty, and very long ones) and record the results? | ☐ | ☐ | ☐ | |
| AIF-03 🔴 | Did you test attempts to trick the AI (prompt injection, "ignore your rules", getting it to reveal hidden instructions or other users' data)? | ☐ | ☐ | ☐ | |
| AIF-04 🔴 | Does the AI refuse or safely redirect harmful, illegal, or self-harm-related requests, with a kind message and help links where right? | ☐ | ☐ | ☐ | |
| AIF-05 🔴 | Are users told clearly when they are talking to AI or seeing AI-generated content? | ☐ | ☐ | ☐ | |
| AIF-06 🟡 | Did you measure how often the AI gives wrong or made-up answers (hallucinations) on important topics, and is the rate acceptable? Write the % | ☐ | ☐ | ☐ | |
| AIF-07 🟡 | Does the product show a warning or a way to double-check when the AI's answer could affect health, money, or legal matters? | ☐ | ☐ | ☐ | |
| AIF-08 🟡 | Is the AI model name and version, plus the prompts/instructions, saved and tied to this release? | ☐ | ☐ | ☐ | |
| AIF-09 🟡 | Is there a set of "golden" test questions that you re-run before every release to catch quality drops? | ☐ | ☐ | ☐ | |
| AIF-10 🟡 | Are users' private data kept out of AI providers' training, per your agreement, and is this mentioned in your privacy policy? | ☐ | ☐ | ☐ | |
| AIF-11 🔴 | Are spending limits, usage limits, and alerts set so one user or a bug cannot create a huge AI bill? | ☐ | ☐ | ☐ | |
| AIF-12 🟡 | Does the product behave nicely if the AI provider is slow, down, or rate-limited (friendly message, retry, fallback)? | ☐ | ☐ | ☐ | |
| AIF-13 🟡 | Can the AI feature be turned off quickly without a new release (feature flag or kill switch)? | ☐ | ☐ | ☐ | |
| AIF-14 🟡 | Can users report a bad or harmful AI answer, and does someone review those reports? | ☐ | ☐ | ☐ | |
| AIF-15 ⚪ | Did you check the AI's answers for bias or unfair treatment across different groups of users? | ☐ | ☐ | ☐ | |
| AIF-16 ⚪ | If the AI can take actions (send emails, delete data, make purchases), does a human confirm risky actions first? | ☐ | ☐ | ☐ | |

### 3.9 API / backend service (N/A if there is no API or backend others connect to)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| API-01 🔴 | Is the API documented (every endpoint, inputs, outputs, error codes) and does the documentation match the real behavior? | ☐ | ☐ | ☐ | |
| API-02 🔴 | Did you check that this release does NOT break existing users of the API (backward compatibility)? | ☐ | ☐ | ☐ | |
| API-03 🔴 | Does every endpoint require the right login/permission, and are the "who can see what" rules tested? | ☐ | ☐ | ☐ | |
| API-04 🟡 | Does the API return clear, consistent error messages and correct status codes (not just "500 error")? | ☐ | ☐ | ☐ | |
| API-05 🟡 | Does the API reject bad or missing inputs safely (wrong types, too large, special characters)? | ☐ | ☐ | ☐ | |
| API-06 🟡 | Are rate limits and size limits in place and tested, and are they documented? | ☐ | ☐ | ☐ | |
| API-07 🟡 | Is the API versioned (for example /v1/) and is there a written plan for retiring old versions? | ☐ | ☐ | ☐ | |
| API-08 🟡 | Did automated contract tests pass, so the API matches its published specification (for example OpenAPI)? | ☐ | ☐ | ☐ | |
| API-09 🟡 | Are API keys and tokens created, rotated, and revoked in a safe, tested way? | ☐ | ☐ | ☐ | |
| API-10 🟡 | Do health-check endpoints exist so monitoring can tell if the service is alive? | ☐ | ☐ | ☐ | |
| API-11 🟡 | Are repeated requests safe (for example, sending "create order" twice does not charge twice)? | ☐ | ☐ | ☐ | |
| API-12 ⚪ | Have the teams or customers that use the API been told about this release ahead of time? | ☐ | ☐ | ☐ | |

### 3.10 Accessibility and localization deep-dive (N/A if you only serve one language and have already completed LGL-06 and LGL-07 fully)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| ACC-01 🟡 | Did an automated accessibility scan (for example Lighthouse or axe) find zero serious issues on the key screens? | ☐ | ☐ | ☐ | |
| ACC-02 🟡 | Did a person test the key screens with a screen reader (VoiceOver, TalkBack, or NVDA)? | ☐ | ☐ | ☐ | |
| ACC-03 🟡 | Can every action be done using only a keyboard, with a visible focus outline and a logical order? | ☐ | ☐ | ☐ | |
| ACC-04 🟡 | Does the product meet WCAG 2.2 level AA on key screens (contrast, text size, labels, error help)? | ☐ | ☐ | ☐ | |
| ACC-05 🟡 | Does it work with text enlarged to 200%, with reduced motion turned on, and in dark mode if offered? | ☐ | ☐ | ☐ | |
| ACC-06 🟡 | Do videos have captions and audio have transcripts? | ☐ | ☐ | ☐ | |
| LOC-01 🟡 | Are all visible words (including errors, emails, store listing, and legal pages) translated and reviewed by a fluent person? | ☐ | ☐ | ☐ | |
| LOC-02 🟡 | Do longer translated texts fit without cutting off or breaking layouts? | ☐ | ☐ | ☐ | |
| LOC-03 🟡 | Are dates, times, numbers, currencies, and addresses shown in each region's usual format? | ☐ | ☐ | ☐ | |
| LOC-04 ⚪ | If you support right-to-left languages (for example Arabic or Hebrew), is the layout mirrored and tested? | ☐ | ☐ | ☐ | |
| LOC-05 ⚪ | Do names, phone numbers, and addresses from other countries save and display correctly (accents, long names, emoji)? | ☐ | ☐ | ☐ | |
| LOC-06 ⚪ | Do the legal pages and consent rules match each region where you launch? | ☐ | ☐ | ☐ | |

### 3.11 Data and analytics (N/A if the product collects no usage data and has no reports)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| DAT-01 🔴 | Is there a written list of every kind of data collected, why, where it is stored, and how long it is kept? | ☐ | ☐ | ☐ | |
| DAT-02 🔴 | Do tracking tools only start after consent, where the law requires it? | ☐ | ☐ | ☐ | |
| DAT-03 🔴 | Are data deletion and export requests also applied to analytics tools, backups (on their normal schedule), and third-party services? | ☐ | ☐ | ☐ | |
| DAT-04 🟡 | Did you test that each key event (sign-up, first success, purchase, cancel) is recorded once, with the right details? | ☐ | ☐ | ☐ | |
| DAT-05 🟡 | Do dashboard numbers match a manual count for a small sample? | ☐ | ☐ | ☐ | |
| DAT-06 🟡 | Is personal information kept out of analytics, logs, and error reports, or properly masked? | ☐ | ☐ | ☐ | |
| DAT-07 🟡 | Are data pipelines/jobs (imports, exports, reports) monitored, and do they alert when they fail or run late? | ☐ | ☐ | ☐ | |
| DAT-08 🟡 | Are access rules set so only the right people can see raw data and reports? | ☐ | ☐ | ☐ | |
| DAT-09 ⚪ | Are data retention limits enforced automatically (old data deleted on schedule)? | ☐ | ☐ | ☐ | |
| DAT-10 ⚪ | Is each key metric clearly defined in writing, so everyone counts the same way (for example, "active customer")? | ☐ | ☐ | ☐ | |

### 3.12 Open bugs summary (fill after testing)

| Severity | Meaning | Count open | Allowed to launch with? |
|---|---|---|---|
| **S1 Critical** | Data loss, security hole, or main task broken for everyone | | **No. Never.** |
| **S2 High** | Main task broken for some people, or no workaround | | Only with Release Owner approval and a ticket |
| **S3 Medium** | Annoying, but a workaround exists | | Yes, with a ticket |
| **S4 Low** | Cosmetic (looks, wording) | | Yes, with a ticket |

---

## PART 4. PHASE 3: STAGING AND RELEASE CANDIDATE (are we ready to ship?)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| STG-01 🔴 | Was the release candidate deployed to staging using the same steps you will use for production? | ☐ | ☐ | ☐ | |
| STG-02 🔴 | Did the smoke test pass again on staging? | ☐ | ☐ | ☐ | |
| STG-03 🔴 | Have database changes (migrations) been tested on a copy of real-size data, and can they be undone? | ☐ | ☐ | ☐ | |
| STG-04 🔴 | Are all production settings and secrets prepared and double-checked (right addresses, keys, email sender, payment keys)? | ☐ | ☐ | ☐ | |
| STG-05 🔴 | Is there a recent backup of production data, and did you test that a restore actually works? | ☐ | ☐ | ☐ | |
| STG-06 🔴 | Is there a written **rollback plan** (Part 10) and did someone rehearse it? | ☐ | ☐ | ☐ | |
| STG-07 🟡 | Are risky new features behind an on/off switch (feature flag) so they can be turned off without a new release? | ☐ | ☐ | ☐ | |
| STG-08 🟡 | Are domain name, security certificate (SSL), and email sending records (SPF/DKIM) set up and not expiring soon? | ☐ | ☐ | ☐ | |
| STG-09 🟡 | Is production sized for the expected traffic (servers, database, third-party plan limits)? | ☐ | ☐ | ☐ | |
| STG-10 🟡 | Are third-party accounts upgraded from free/test plans where needed (email, maps, AI/API usage quotas)? | ☐ | ☐ | ☐ | |
| STG-11 🟡 | Is a **code freeze** declared (no new changes except approved fixes) from now until launch? | ☐ | ☐ | ☐ | |
| STG-12 ⚪ | Did a small trusted group (beta testers) use staging or a beta build and give feedback? | ☐ | ☐ | ☐ | |

---

## PART 5. PHASE 4: LAUNCH READINESS AND GO/NO-GO (the decision)

### 5.1 Can we see and fix problems? (Monitoring)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| MON-01 🔴 | Will we be alerted automatically (phone/chat) if the site is down or error rates jump? | ☐ | ☐ | ☐ | |
| MON-02 🔴 | Is error tracking turned on for web and mobile (crashes reported with details)? | ☐ | ☐ | ☐ | |
| MON-03 🟡 | Is there a simple dashboard showing: visitors, sign-ups, errors, speed, and (if relevant) payments? | ☐ | ☐ | ☐ | |
| MON-04 🟡 | Are logs saved so we can investigate (without storing passwords or sensitive data in them)? | ☐ | ☐ | ☐ | |
| MON-05 🟡 | Is product analytics set up for the key steps (visit → sign-up → first success → return)? | ☐ | ☐ | ☐ | |
| MON-06 🟡 | Is there a public or private status page, and do we know who updates it? | ☐ | ☐ | ☐ | |
| MON-07 🟡 | Are cost alerts set (cloud bill, AI/API usage) so a surprise bill is caught early? | ☐ | ☐ | ☐ | |

### 5.2 Can customers get help? (Support and communication)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| SUP-01 🔴 | Is there a clear way for customers to contact support (email, form, or chat) that someone actually reads? | ☐ | ☐ | ☐ | |
| SUP-02 🟡 | Has the support team been trained and given a list of known issues and answers to common questions? | ☐ | ☐ | ☐ | |
| SUP-03 🟡 | Is a help page / FAQ / getting-started guide published? | ☐ | ☐ | ☐ | |
| SUP-04 🟡 | Is there a way to report a bug or send feedback from inside the product? | ☐ | ☐ | ☐ | |
| SUP-05 🟡 | Is the launch announcement (email, post, press note) written, checked for accuracy, and scheduled? | ☐ | ☐ | ☐ | |
| SUP-06 🟡 | Is a template ready to tell customers about an outage or a mistake honestly? | ☐ | ☐ | ☐ | |

### 5.3 Are people ready? (Team)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| TEAM-01 🔴 | Is a named **on-call engineer** available (with a backup) for at least 7 days after launch? | ☐ | ☐ | ☐ | |
| TEAM-02 🔴 | Does everyone know who decides to roll back, and how to reach them quickly? | ☐ | ☐ | ☐ | |
| TEAM-03 🟡 | Is the launch not scheduled right before a weekend, holiday, or people's time off? | ☐ | ☐ | ☐ | |
| TEAM-04 🟡 | Is there a shared chat channel for launch day? | ☐ | ☐ | ☐ | |

### 5.4 Count your results (fill after answering Parts 2 to 5.3)

| Group | Total rows | Yes | No | N/A | Blank |
|---|---|---|---|---|---|
| 🔴 BLOCKER | | | | | |
| 🟡 IMPORTANT | | | | | |
| ⚪ NICE | | | | | |

**Decision rules (apply them exactly):**

| Situation | Decision |
|---|---|
| Any 🔴 BLOCKER is **No** or **Blank** | 🛑 **NO-GO.** Fix, retest, recount. |
| Any open **S1 Critical** bug | 🛑 **NO-GO.** |
| All 🔴 are Yes/approved N/A, but any 🟡 is **No** without a ticket and approval | 🟠 **NO-GO until ticketed and approved** |
| All 🔴 Yes, all 🟡 Yes or approved with tickets | ✅ **GO** |

### 5.5 Final Go/No-Go sign-off

| Role | Name | Decision (GO / NO-GO) | Reason, if No-Go | Date | Signature (type your name) |
|---|---|---|---|---|---|
| Release Owner | | | | | |
| Product Owner | | | | | |
| Engineering Lead | | | | | |
| QA Lead | | | | | |
| Security Owner | | | | | |
| Support Lead | | | | | |

**Final decision:** ☐ GO ☐ NO-GO  **Date/time:** ________

---

## PART 6. LAUNCH DAY

### 6.1 Launch steps (write the real steps for your project. Keep each step small.)

| Step | What to do | Who | Planned time | Done at | Notes |
|---|---|---|---|---|---|
| 1 | Announce in the launch channel: "Launch starting" | | | | |
| 2 | Confirm a fresh backup finished | | | | |
| 3 | Deploy the release to production | | | | |
| 4 | Run database changes (if any) | | | | |
| 5 | Run the production smoke test (Section 6.2) | | | | |
| 6 | Turn on feature flags / open the doors to users | | | | |
| 7 | Publish store releases (mobile) | | | | |
| 8 | Send the launch announcement | | | | |
| 9 | Announce in the launch channel: "Launch complete" | | | | |

### 6.2 Production smoke test (do it yourself, on the live product, right after deploying)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| LCH-01 🔴 | Does the live site/app open, and does it show the correct version number? | ☐ | ☐ | ☐ | |
| LCH-02 🔴 | Can you sign up with a brand-new account on the live product? | ☐ | ☐ | ☐ | |
| LCH-03 🔴 | Can you complete the main task on the live product? | ☐ | ☐ | ☐ | |
| LCH-04 🔴 | (If paid) Does one real, small purchase work and can it be refunded? | ☐ | ☐ | ☐ | |
| LCH-05 🔴 | Do alerts, error tracking, and dashboards show live data? | ☐ | ☐ | ☐ | |
| LCH-06 🟡 | Did the welcome email arrive within 2 minutes? | ☐ | ☐ | ☐ | |
| LCH-07 🟡 | Does the mobile app download and install from the store link? | ☐ | ☐ | ☐ | |

### 6.3 Watch window: first 4 hours

Check every **30 minutes** and write the numbers.

| Time | Errors (%) | Speed OK? | New sign-ups | Support messages | Anything strange? | Who checked |
|---|---|---|---|---|---|---|
| | | | | | | |
| | | | | | | |
| | | | | | | |
| | | | | | | |

**Roll back immediately if (edit these numbers to fit your project):** error rate above ______%, OR main task broken for users, OR any data loss or security problem, OR payments failing for more than ______ minutes.

---

## PART 7. FIRST WEEK (DAY 1 TO DAY 7)

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| WK-01 🔴 | Was the product checked at least 3 times on Day 1 (morning, midday, evening) with numbers recorded? | ☐ | ☐ | ☐ | |
| WK-02 🔴 | Was every support request answered within the promised time during the first 7 days? | ☐ | ☐ | ☐ | |
| WK-03 🔴 | Were all S1/S2 bugs found after launch fixed or rolled back within 24 hours? | ☐ | ☐ | ☐ | |
| WK-04 🟡 | Did you review daily: errors, crashes, sign-ups, drop-off points, and cost? | ☐ | ☐ | ☐ | |
| WK-05 🟡 | Did you read every piece of customer feedback and sort it (bug / confusing / request / praise)? | ☐ | ☐ | ☐ | |
| WK-06 🟡 | Did you check store reviews and ratings daily (mobile) and reply to them? | ☐ | ☐ | ☐ | |
| WK-07 🟡 | Were hotfixes tested with a smoke test and regression test before shipping (no "quick untested fixes")? | ☐ | ☐ | ☐ | |
| WK-08 ⚪ | Was a short "Week 1 report" shared with the team (Section 9.3)? | ☐ | ☐ | ☐ | |

### Daily log (Week 1)

| Day | Date | Total users | New sign-ups | Error rate | Open S1/S2 bugs | Support tickets (open) | Cost today | Notes |
|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | |
| 2 | | | | | | | | |
| 3 | | | | | | | | |
| 4 | | | | | | | | |
| 5 | | | | | | | | |
| 6 | | | | | | | | |
| 7 | | | | | | | | |

---

## PART 8. GROWING TO YOUR FIRST 500 CUSTOMERS

Do these checks when the customer count reaches each milestone. Write the date you reached it.

| Milestone | Date reached | Check done? |
|---|---|---|
| First 1 real (non-team) customer | | ☐ |
| 10 customers | | ☐ |
| 50 customers | | ☐ |
| 100 customers | | ☐ |
| 250 customers | | ☐ |
| 500 customers 🎉 | | ☐ |

### 8.1 At 1 and 10 customers: "Does it really work for strangers?"

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| G10-01 🔴 | Did you personally talk to or message at least 5 early customers? | ☐ | ☐ | ☐ | |
| G10-02 🟡 | Can customers finish the main task without your help? Write where they got stuck | ☐ | ☐ | ☐ | |
| G10-03 🟡 | Did you watch at least 3 people use the product (recording or live) and note confusion? | ☐ | ☐ | ☐ | |
| G10-04 🟡 | Is the onboarding completion rate close to the target in Part 1.4? | ☐ | ☐ | ☐ | |
| G10-05 🟡 | Is every customer-reported bug logged with a ticket? | ☐ | ☐ | ☐ | |

### 8.2 At 50 and 100 customers: "Is it stable and sustainable?"

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| G100-01 🔴 | Is the error rate and crash rate still within the target? | ☐ | ☐ | ☐ | |
| G100-02 🔴 | Did you run a restore test of the backup again? | ☐ | ☐ | ☐ | |
| G100-03 🟡 | Is the cost per customer known and acceptable (cloud, AI/API, payments, support)? | ☐ | ☐ | ☐ | |
| G100-04 🟡 | Are the top 3 customer complaints known, and is each one planned or fixed? | ☐ | ☐ | ☐ | |
| G100-05 🟡 | Do you know how many customers come back after 1 day and 7 days (retention)? Write the numbers | ☐ | ☐ | ☐ | |
| G100-06 🟡 | Was an automated regression test suite run for every release since launch? | ☐ | ☐ | ☐ | |
| G100-07 🟡 | Are support answers saved as help articles so the same question is not answered by hand again? | ☐ | ☐ | ☐ | |
| G100-08 ⚪ | Were the dependency and security scans re-run in the last 30 days? | ☐ | ☐ | ☐ | |

### 8.3 At 250 and 500 customers: "Are we ready to grow beyond this?"

| ID | Question | Yes | No | N/A | Proof |
|---|---|---|---|---|---|
| G500-01 🔴 | Did a new load test pass at **3× the current busiest hour**? | ☐ | ☐ | ☐ | |
| G500-02 🔴 | Is there a tested incident response plan (who does what if something breaks at 3 a.m.)? | ☐ | ☐ | ☐ | |
| G500-03 🟡 | Did any customer data requests (delete/export) get handled correctly and on time? | ☐ | ☐ | ☐ | |
| G500-04 🟡 | Has a full security review or penetration test been done since launch? | ☐ | ☐ | ☐ | |
| G500-05 🟡 | Are third-party plans and limits (email, AI/API, database, app stores) enough for 2× more customers? | ☐ | ☐ | ☐ | |
| G500-06 🟡 | Are all S3 and S4 bugs from earlier either fixed or consciously accepted in writing? | ☐ | ☐ | ☐ | |
| G500-07 🟡 | Did you update this checklist with lessons learned (Part 12)? | ☐ | ☐ | ☐ | |
| G500-08 ⚪ | Did you publish a customer-facing "what we learned and what's next" update? | ☐ | ☐ | ☐ | |

### 8.4 Growth tracker

| Date | Total customers | New this week | Active this week | Cancelled / left | Error rate | Avg. support reply time | Cost per customer | Top problem right now |
|---|---|---|---|---|---|---|---|---|
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |

---

## PART 9. WHAT-IF PLANS

### 9.1 When something breaks: severity and response speed

| Severity | Example | Who to tell | Fix or roll back within |
|---|---|---|---|
| **S1 Critical** | Site down, data lost, security leak, payments wrong | Whole team + Release Owner immediately | **1 hour** (roll back first, investigate later) |
| **S2 High** | Main task fails for some users | Engineering Lead + Support Lead | 24 hours |
| **S3 Medium** | Feature wrong, workaround exists | Ticket + next release | Within 2 weeks |
| **S4 Low** | Typo, small visual issue | Ticket | When convenient |

### 9.2 If a data leak or security problem happens

| Question | Your answer |
|---|---|
| Who decides it is a security incident? | |
| Who contacts affected customers, and using which template? | |
| Who contacts authorities, if the law requires it (and within how many hours)? | |
| Who can shut the product or a feature off quickly, and how? | |

### 9.3 Week 1 report (fill after Day 7)

| Question | Your answer |
|---|---|
| Total customers at Day 7 | |
| What went well? (3 bullets) | |
| What went wrong? (3 bullets) | |
| Bugs found after launch (count and worst severity) | |
| Top 3 things to fix next | |

---

## PART 10. ROLLBACK PLAN (write BEFORE launch, test it, keep it short)

| Question | Your answer |
|---|---|
| Who is allowed to press the "roll back" button? | |
| Exactly how do we go back to the last good version? (numbered steps) | |
| Which version is the "last good" one? (version number / link) | |
| Do database changes need to be undone? How? | |
| How long does a rollback take? (tested time) | |
| How do mobile users get fixed if an app update must be reversed? (turn off feature flag / force update / server-side fix / emergency store update) | |
| Who tells customers and where? | |
| Date and result of the last rollback rehearsal | |

---

## PART 11. KNOWN ISSUES AND APPROVED EXCEPTIONS

Every "No" on a 🟡 row, and every launched-with bug, goes here.

| # | Checklist ID or bug # | What is wrong? | Severity (S2/S3/S4) | Who is affected? | Workaround for users | Ticket link | Fix by (date) | Approved by (Release Owner) |
|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | |
| 2 | | | | | | | | |
| 3 | | | | | | | | |

---

## PART 12. RETROSPECTIVE AND TEMPLATE IMPROVEMENT

| Question | Your answer |
|---|---|
| Which checklist rows caught a real problem? | |
| Which rows were confusing? (write the ID and how to reword it) | |
| Which problem happened that no row asked about? (add a new row) | |
| Which rows are never useful for our type of project? | |
| Did we launch on time? If not, what slowed us down? | |
| What will we do differently next release? | |

### Version history of this filled-in file

| Date | Version | Changed by | What changed |
|---|---|---|---|
| | | | |

---

## PART 13. GLOSSARY (plain-language words)

| Word | What it means |
|---|---|
| **Release / Release candidate** | A version of the product you plan to ship. The "candidate" is the exact one being tested. |
| **Staging** | A practice copy of the live product used for final testing. |
| **Production** | The live product that real customers use. |
| **Blocker** | A problem or missing item that stops the launch. |
| **Smoke test** | A quick check that the most important things work, like checking a machine turns on. |
| **Regression test** | Checking that old features still work after new changes. |
| **Rollback** | Going back to the previous working version. |
| **Feature flag** | An on/off switch for a feature, so you can turn it off without a new release. |
| **Hotfix** | A small, urgent fix released outside the normal schedule. |
| **Code freeze** | A pause on new changes so the tested version stays the same. |
| **Migration** | A change to the database structure or data. |
| **Load test** | Pretending many users visit at once to see if the product copes. |
| **Linter** | A tool that checks code for mistakes and style problems. |
| **Dependency** | Another piece of software that your product uses. |
| **Secret** | A password, key, or token that must never be shared or stored in code. |
| **OWASP Top 10** | A well-known list of the most common website security problems. |
| **Penetration test** | A permitted, controlled attempt to break into your product to find weaknesses. |
| **Two-factor login (2FA)** | Logging in with a password plus a second proof, such as a phone code. |
| **Monitoring / Alert** | Watching the product's health automatically and sending a message when something is wrong. |
| **On-call** | The person who must respond quickly if something breaks. |
| **Retention** | The share of customers who come back after a day, week, or month. |
| **Onboarding** | The first steps a new customer takes to get value from the product. |
| **S1 / S2 / S3 / S4** | Bug severity levels from Critical (S1) to Low (S4). |
| **AI-assisted development** | Building software with help from AI tools or agents that write or change code. |

---

*End of template. Remember: no proof means no. Blank means no. Blockers must be Yes. When in doubt, ask. Never guess.*
