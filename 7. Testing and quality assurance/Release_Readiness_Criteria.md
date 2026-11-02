# HOW TO FILL IN THIS DOCUMENT (READ THIS FIRST)

> **Template version:** 1.0 | **Folder:** Testing and Quality Assurance | **File:** `Release_Readiness_Criteria.md`
> **Covers:** AI-Driven Development Life Cycle, from "code is written" all the way to "our first 500 customers are happily using it."
> **Works for:** Web / SaaS apps and Mobile apps (iOS and Android).

## What is this document?

Think of it as a **pre-flight checklist for a plane**. Before a plane takes off, the pilot checks every important thing. This document does the same for your product. It asks simple questions. You answer them. At the end, the answers tell your team: **GO** (launch!) or **NO-GO** (not yet).

## How do I use it? (7 easy steps)

1. **Copy this file** into your project folder. Rename it: `Release_Readiness_Criteria_<ProjectName>_<Version>.md`. Never fill in the master template itself.
2. **Fill in Part 0** (basic facts about your project). Every `[ ]` square brackets spot is a blank to fill.
3. **Pick your Risk Level in Part 1.** This tells you how strict to be.
4. **Go through the Gates one by one (Gate 1 to Gate 9).** Answer every question in order.
5. **For each question, fill in the 4 answer cells:**

| Cell | What to write |
|---|---|
| **Answer** | Type exactly one of: `YES`, `NO`, or `N/A` |
| **Evidence** | A link or file name that PROVES your answer (test report, screenshot, dashboard link, ticket). No proof = answer is `NO`. |
| **Owner** | One real person's name (not a team name) |
| **Date** | The date you checked it (`YYYY-MM-DD`) |

6. **Count your blockers.** Any question marked **🔴 B** (Blocker) with `NO` means the launch is stopped until fixed, or until a formal Exception is approved (see Appendix A).
7. **Sign at the end (Gate 7)** and record the GO / NO-GO decision. Then keep going: Gates 8 and 9 guide you through your first 500 customers.

## The golden rules

| # | Rule | Why |
|---|---|---|
| 1 | **Never guess.** If you do not know, write `NO` and find out. | A guess can hide a launch-breaking problem. |
| 2 | **No evidence, no YES.** "I think it works" is not evidence. | Proof lets anyone double-check later. |
| 3 | **`N/A` needs a reason** in the Notes column. | Stops people skipping hard questions. |
| 4 | **One owner per question.** A real name, never "everyone". | If everyone owns it, no one does. |
| 5 | **A human signs every gate.** AI agents may collect evidence, but only a named person can approve. | People are accountable; AI is not. |
| 6 | **Do not edit answers after sign-off.** Add a dated note in the Decision Log (Appendix C) instead. | Keeps an honest history. |
| 7 | **Ask for help early.** Stuck on a question for more than 15 minutes? Ask the Release Owner. | Saves days later. |

## Symbols used in this document

| Symbol | Meaning |
|---|---|
| 🔴 **B** | **Blocker**: must be `YES` (or have an approved Exception) before launch |
| 🟡 **S** | **Should-have**: strongly recommended; a `NO` needs a note and a follow-up date |
| 🟢 **C** | **Could-have**: nice to have; no penalty for `NO` |
| `[ ]` | A blank for you to fill in |
| ☐ | A checkbox: replace with ☑ when done |

## Tiny glossary (full one in Appendix E)

- **Release Candidate (RC):** the exact version you plan to launch.
- **Rollback:** going back to the previous working version if the new one breaks.
- **Staged rollout:** letting a few users in first, then more, then more.
- **Go / No-Go:** the final "launch" or "do not launch" decision.
- **Evidence:** something anyone can open to prove your answer.

## Example of a correctly filled row

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 2.1 | Did all automated tests pass on the Release Candidate? | 🔴 B | YES | https://ci.example.com/run/4821 | Priya Shah | 2026-10-18 | 1,204 of 1,204 passed |

---

# PART 0: PROJECT SNAPSHOT

> Fill this in first. Everything below depends on it.

## 0.1 Basic facts

| Question | Your answer |
|---|---|
| What is the product's name? | [ ] |
| In one sentence, what does it do and for whom? | [ ] |
| Product type (tick all) | ☐ Web / SaaS  ☐ iOS  ☐ Android  ☐ Other: [ ] |
| Release Candidate version number | [ ] |
| Target launch date | [ ] |
| Launch region(s) / country(ies) | [ ] |
| Link to the product requirements / scope document | [ ] |
| Link to the code repository | [ ] |
| Link to the project board / ticket tracker | [ ] |

## 0.2 People (use real names)

| Role | What this person does | Name | Contact |
|---|---|---|---|
| **Release Owner** | Runs this checklist; makes sure it gets finished | [ ] | [ ] |
| **Product Owner** | Knows what the product must do; final business say | [ ] | [ ] |
| **Engineering Lead** | Responsible for code quality | [ ] | [ ] |
| **QA Lead** | Responsible for testing proof | [ ] | [ ] |
| **Security Owner** | Responsible for security and privacy | [ ] | [ ] |
| **Operations / On-call Lead** | Keeps the product running after launch | [ ] | [ ] |
| **Support Lead** | Helps customers after launch | [ ] | [ ] |
| **Final Decision Maker** | The ONE person who says GO or NO-GO | [ ] | [ ] |
| **Backup Decision Maker** | Decides if the above is unavailable | [ ] | [ ] |

## 0.3 AI Agent Disclosure (required for AI-driven development)

> Be honest. This is not about blame; it helps reviewers know where to look harder.

| Question | Your answer |
|---|---|
| Which AI tools / agents helped build this product? (names and versions) | [ ] |
| Roughly what percentage of the code was written by AI? | [ ] % |
| Which parts were AI-written? (e.g., UI, API, database, tests) | [ ] |
| Which parts were written fully by humans? | [ ] |
| Which AI agents ran tests or checks? | [ ] |
| Does the product itself contain an AI/LLM feature (chatbot, summarizer, recommender)? | ☐ Yes  ☐ No |
| If Yes: complete **Appendix F (AI Feature Add-on)** as well. | ☐ Done  ☐ N/A |
| Which optional modules apply? (see the table before Appendix H) | ☐ H Data Migration  ☐ I Accessibility/Localization  ☐ J Vendor Risk  ☐ K Marketing/Growth  ☐ None |

---

# PART 1: RISK LEVEL AND SCOPE

## 1.1 Choose your Risk Level

Answer these questions. **Count your YES answers, then use the rule right below the table.**

| # | Question | Yes / No |
|---|---|---|
| a | Will the product collect personal data (names, emails, phone numbers, location)? | [ ] |
| b | Will it handle money, payments, or subscriptions? | [ ] |
| c | Will it handle health, financial, legal, or children's information? | [ ] |
| d | Could a bug cause real harm (loss of money, safety, privacy, reputation)? | [ ] |
| e | Will customers depend on it for their daily work? | [ ] |
| f | Is it hard to undo a release (database changes, app store approval delays)? | [ ] |

**Rule:** 0 YES answers = Level 1. 1 or 2 YES answers = Level 2. 3 or more YES answers = Level 3. **Shortcut:** if (b) money or (c) health/financial/legal/children's data is YES, it is **always Level 3**.

| Level | Name | Meaning | How strict? |
|---|---|---|---|
| **1** | Low | Small, internal, or experimental. Mistakes are easy to fix. | Answer all 🔴 B questions. 🟡 S and 🟢 C are optional. |
| **2** | Medium | Real customers, some personal data, normal business use. | Answer all 🔴 B and 🟡 S questions. |
| **3** | High | Money, health, children, or sensitive data. Mistakes are costly. | Answer **everything**. Second reviewer required at every gate. |

**Our Risk Level is:** ☐ 1  ☐ 2  ☐ 3  **Why:** [ ]

## 1.2 Scope: what is and is not being launched

| Question | Your answer |
|---|---|
| List the 3 to 7 most important things a user must be able to do (critical user journeys). | 1. [ ]  2. [ ]  3. [ ] |
| What is deliberately NOT in this launch? | [ ] |
| Who are the launch users? (e.g., invite-only, one country, everyone) | [ ] |
| What is the maximum number of customers allowed in this phase? | 500 |
| What is the one number that tells us the launch is going well? (e.g., 70% finish sign-up) | [ ] |

## 1.3 Thresholds: write the numbers BEFORE testing

> Agree these numbers **now**. Do not pick them after seeing the results. Suggested defaults are shown; change them if your team agrees.

| Measure | Level 1 default | Level 2 default | Level 3 default | **Our number** |
|---|---|---|---|---|
| Automated tests passing | 95% | 98% | 100% of critical tests | [ ] |
| Open Critical bugs (app crashes, data loss, security hole) | 0 | 0 | 0 | [ ] |
| Open High bugs (major feature broken, no workaround) | ≤ 3 | ≤ 1 | 0 | [ ] |
| Code covered by automated tests | 60% | 70% | 80% | [ ] |
| Page / screen loads in (95% of the time) | < 4 sec | < 3 sec | < 2 sec | [ ] |
| Crash-free sessions (mobile) | 98% | 99% | 99.5% | [ ] |
| Error rate allowed after launch | < 3% | < 1% | < 0.5% | [ ] |
| Uptime goal | 99% | 99.5% | 99.9% | [ ] |
| Time to roll back | < 60 min | < 30 min | < 15 min | [ ] |

## 1.4 Gate Summary (fill in as you go)

| Gate | Name | Total 🔴 B | B answered YES | Gate status | Signed by | Date |
|---|---|---|---|---|---|---|
| 1 | Build Complete | | | ☐ Pass ☐ Fail | | |
| 2 | Quality and Testing | | | ☐ Pass ☐ Fail | | |
| 3 | Security and Privacy | | | ☐ Pass ☐ Fail | | |
| 4 | Operations and Recovery | | | ☐ Pass ☐ Fail | | |
| 5 | Legal, Compliance and Store Rules | | | ☐ Pass ☐ Fail | | |
| 6 | Customer and Business Readiness | | | ☐ Pass ☐ Fail | | |
| 7 | Go / No-Go Decision | | | ☐ GO ☐ NO-GO | | |
| 8 | Staged Rollout to First 500 Customers | | | ☐ Done | | |
| 9 | Post-Launch Review and Closure | | | ☐ Closed | | |

---

# GATE 1: BUILD COMPLETE
**The big question: Is the product finished, frozen, and traceable?**

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 1.1 | Is every planned feature either finished or formally removed from this launch? | 🔴 B | | | | | |
| 1.2 | Is the Release Candidate frozen (no new changes without Release Owner approval)? | 🔴 B | | | | | |
| 1.3 | Can we point to the exact code version (commit / tag) of the Release Candidate? | 🔴 B | | | | | |
| 1.4 | Was every code change reviewed by a human who did NOT write or prompt it? | 🔴 B | | | | | |
| 1.5 | Did a human read and understand all AI-written code in critical areas (login, payments, data, permissions)? | 🔴 B | | | | | |
| 1.6 | Are all third-party packages real, approved, and free of known serious vulnerabilities? (AI tools sometimes invent package names.) | 🔴 B | | | | | |
| 1.7 | Are software licenses of all packages and AI-generated code checked and acceptable? | 🟡 S | | | | | |
| 1.8 | Are AI prompts, agent instructions, and agent settings saved and versioned along with the code? | 🟡 S | | | | | |
| 1.9 | Do we have a log of what AI agents changed (who/what/when)? | 🟡 S | | | | | |
| 1.10 | Were AI agents' access rights limited (no access to production data or secrets unless needed)? | 🔴 B | | | | | |
| 1.11 | Are all secrets (passwords, API keys) kept out of the code and out of AI prompts? | 🔴 B | | | | | |
| 1.12 | Are all settings (config, environment variables) for production written down and reviewed? | 🔴 B | | | | | |
| 1.13 | Are database changes (migrations) written, tested on a copy of real-like data, and reversible? | 🔴 B | | | | | |
| 1.14 | Can the exact same Release Candidate be built again from scratch by someone else? | 🟡 S | | | | | |
| 1.15 | Is there a short document describing how the system is built (architecture sketch)? | 🟡 S | | | | | |
| 1.16 | Are unfinished or half-done pieces (TODO notes, test code, fake data, debug switches) removed? | 🔴 B | | | | | |
| 1.17 | Are new features hidden behind on/off switches (feature flags) where possible? | 🟡 S | | | | | |
| 1.18 | Is there a Release Notes draft listing what's new, changed, and known issues? | 🟡 S | | | | | |

**Gate 1 sign-off:** I confirm the answers above are true and backed by evidence.
Name: [ ] Role: Engineering Lead  Date: [ ]  ☐ PASS  ☐ FAIL

---

# GATE 2: QUALITY AND TESTING
**The big question: Does it work, and can we prove it?**

## 2A. Core testing

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 2.1 | Did the automated tests run on the exact Release Candidate (not an older version) and meet our threshold in 1.3? | 🔴 B | | | | | |
| 2.2 | Does each critical user journey (1.2) have at least one test that passed? | 🔴 B | | | | | |
| 2.3 | Did a human also try each critical user journey by hand on a real, production-like setup? | 🔴 B | | | | | |
| 2.4 | Are there zero open Critical bugs? | 🔴 B | | | | | |
| 2.5 | Is the number of open High bugs within our threshold, and is each one listed with a workaround or an approved Exception? | 🔴 B | | | | | |
| 2.6 | Are all other open bugs listed in the Known Issues Register (Appendix B)? | 🟡 S | | | | | |
| 2.7 | Did the regression tests (checking old features still work) pass? | 🔴 B | | | | | |
| 2.8 | Are the tests real? (A human spot-checked that AI-written tests truly check behavior, and do not just "pass" automatically.) | 🔴 B | | | | | |
| 2.9 | Did we test bad inputs and weird actions (empty fields, huge files, emojis, double-clicks, no internet)? | 🟡 S | | | | | |
| 2.10 | Did we test every "what if it fails?" message (error screens are clear and kind)? | 🟡 S | | | | | |
| 2.11 | Did real users or friendly testers (UAT / beta) try the product and approve it? | 🟡 S | | | | | |
| 2.12 | Were bugs found in the last test round fixed AND re-tested? | 🔴 B | | | | | |
| 2.13 | Is our test code coverage at or above our threshold? | 🟡 S | | | | | |

## 2B. Performance and reliability

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 2.14 | Did we test with the number of users we expect at peak (and 2x more)? What was the peak number? | 🔴 B (L2-3) | | | | | |
| 2.15 | Do pages / screens load within our time threshold? | 🟡 S | | | | | |
| 2.16 | Did the product stay stable when run for many hours (no slow leaks, no growing memory)? | 🟡 S | | | | | |
| 2.17 | Does the product handle things breaking nicely (a service is down, slow network, full disk)? | 🟡 S | | | | | |
| 2.18 | Are costs predictable? (cloud bill, AI usage fees, email/SMS fees at 500 users and at 5x that) | 🟡 S | | | | | |

## 2C. Web-specific (mark N/A for mobile-only)

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 2.19 | Tested on the latest 2 versions of Chrome, Safari, Firefox, and Edge? | 🔴 B | | | | | |
| 2.20 | Works on phone, tablet, and desktop screen sizes? | 🔴 B | | | | | |
| 2.21 | Did the production web page pass a smoke test (home page, login, key page load) after deploy to a staging copy? | 🟡 S | | | | | |
| 2.22 | Do web search/sharing basics work (page titles, links, icons)? | 🟢 C | | | | | |

## 2D. Mobile-specific (mark N/A for web-only)

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 2.23 | Tested on real devices (not just simulators): at least one old, one mid-range, one new phone for each platform? List them in Notes. | 🔴 B | | | | | |
| 2.24 | Tested on the oldest operating system version we promise to support, and the newest? | 🔴 B | | | | | |
| 2.25 | Does the app handle interruptions (phone call, low battery, going offline, app in background, rotating screen)? | 🟡 S | | | | | |
| 2.26 | Did we test installing fresh, updating from the previous version, and uninstalling? | 🔴 B | | | | | |
| 2.27 | Does the crash-free rate on test devices meet our threshold? | 🟡 S | | | | | |
| 2.28 | Do push notifications arrive, open the right screen, and respect user permission choices? | 🟡 S | | | | | |
| 2.29 | Is battery, data, and storage use reasonable? | 🟢 C | | | | | |

## 2E. Accessibility and usability

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 2.30 | Can the main journeys be completed using only a keyboard (web) or screen reader (web and mobile)? | 🟡 S (🔴 B for L3) | | | | | |
| 2.31 | Are text size, color contrast, and tap targets readable and easy to use? | 🟡 S | | | | | |
| 2.32 | Did a first-time person finish the main journey without help? | 🟡 S | | | | | |
| 2.33 | Are texts free of spelling errors, and are languages / date / currency formats right for launch regions? | 🟡 S | | | | | |

**Gate 2 sign-off:** Name: [ ] Role: QA Lead  Date: [ ]  ☐ PASS  ☐ FAIL

---

# GATE 3: SECURITY AND PRIVACY
**The big question: Is customer data safe, and can bad people get in?**

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 3.1 | Was a security review done for this Risk Level? (L1: self-check; L2: a second person; L3: independent expert) | 🔴 B | | | | | |
| 3.2 | Did automated security scans (code, packages, and the running app) find zero Critical and zero High issues still open? | 🔴 B | | | | | |
| 3.3 | Do logins use safe methods (strong passwords or trusted sign-in, limited login attempts, safe password reset)? | 🔴 B | | | | | |
| 3.4 | Does each user only see and change their OWN data? (Tried logging in as user A and opening user B's data.) | 🔴 B | | | | | |
| 3.5 | Is all data traveling over the internet encrypted (HTTPS / TLS)? | 🔴 B | | | | | |
| 3.6 | Is sensitive stored data encrypted (passwords hashed, personal data protected)? | 🔴 B | | | | | |
| 3.7 | Are secrets stored in a proper secret vault and not in code, logs, or chat tools? Were any old/leaked secrets replaced? | 🔴 B | | | | | |
| 3.8 | Is user input checked everywhere (protection against injection, script attacks, forged requests)? | 🔴 B | | | | | |
| 3.9 | Are admin tools and internal pages locked away from normal users? | 🔴 B | | | | | |
| 3.10 | Are logs free of passwords, card numbers, and other private data? | 🔴 B | | | | | |
| 3.11 | Is there rate-limiting / abuse protection (bots, spam, scraping)? | 🟡 S | | | | | |
| 3.12 | (Mobile) Is sensitive data stored safely on the phone, and is the app protected from tampering? | 🟡 S | | | | | |
| 3.13 | Did we list personal data we collect, why, where it's stored, and how long we keep it? | 🔴 B | | | | | |
| 3.14 | Can a user see, export, and delete their data if the law requires it? | 🔴 B (if law applies) | | | | | |
| 3.15 | Do we only collect the data we really need? | 🟡 S | | | | | |
| 3.16 | Do we have a plan for what to do if there's a data leak (who to tell, how fast, by law)? | 🔴 B | | | | | |
| 3.17 | Did a person (not only an AI) review the security of AI-written code in login, payments, and data handling? | 🔴 B | | | | | |
| 3.18 | Are payment details handled only by a certified payment provider (we never store card numbers ourselves)? | 🔴 B (if payments) | | | | | |

**Gate 3 sign-off:** Name: [ ] Role: Security Owner  Date: [ ]  ☐ PASS  ☐ FAIL

---

# GATE 4: OPERATIONS AND RECOVERY
**The big question: When something goes wrong, will we know fast and fix fast?**

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 4.1 | Is there a written rollback plan with exact steps, and did someone practice it successfully? Time it took: [ ] min | 🔴 B | | | | | |
| 4.2 | Can we turn off the new features quickly (feature flag, kill switch, or stop the rollout)? | 🔴 B | | | | | |
| 4.3 | (Mobile) Do we have a plan if a bad app version is already on phones (force-update message, server-side disable, quick patch release)? | 🔴 B | | | | | |
| 4.4 | Do we watch errors, speed, and traffic on a live dashboard? Link in Evidence. | 🔴 B | | | | | |
| 4.5 | Do alerts go to a real person's phone when something breaks? Did we test an alert? | 🔴 B | | | | | |
| 4.6 | Are alerts useful (not so noisy that people ignore them)? | 🟡 S | | | | | |
| 4.7 | Are crashes and errors automatically collected with enough detail to fix them? | 🔴 B | | | | | |
| 4.8 | Is there an on-call schedule for launch week with names, phone numbers, and a backup person? | 🔴 B | | | | | |
| 4.9 | Is there a written "what to do when X breaks" guide (runbook) for the 5 most likely problems? | 🔴 B | | | | | |
| 4.10 | Are backups running automatically, and did we practice restoring one? Restore time: [ ] min | 🔴 B | | | | | |
| 4.11 | Do we know the server / cloud limits and have headroom for 5x the expected launch users? | 🟡 S | | | | | |
| 4.12 | Do we know every outside service we depend on (payments, email, login, maps, AI provider), and what happens if each one goes down? | 🟡 S | | | | | |
| 4.13 | Is the test environment (staging) similar enough to production that tests mean something? | 🟡 S | | | | | |
| 4.14 | Is there a status page or other way to tell customers about problems? | 🟡 S | | | | | |
| 4.15 | Are cost alerts set so a surprise bill is caught early? | 🟡 S | | | | | |
| 4.16 | Is there a plan for incidents: who leads, how we talk, how we write a "what happened" report afterwards? | 🟡 S | | | | | |
| 4.17 | Can the people who must respond actually log in and use all tools today (access tested)? | 🔴 B | | | | | |

**Gate 4 sign-off:** Name: [ ] Role: Operations / On-call Lead  Date: [ ]  ☐ PASS  ☐ FAIL

---

# GATE 5: LEGAL, COMPLIANCE AND STORE RULES
**The big question: Are we allowed to launch?**

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 5.1 | Are the Terms of Service and Privacy Policy written, reviewed (by a qualified person), and linked in the product? | 🔴 B | | | | | |
| 5.2 | Are cookie / tracking consent rules handled for launch regions? | 🔴 B (web) | | | | | |
| 5.3 | Do we follow the privacy and data laws in each launch region (e.g., GDPR, CCPA, or local law)? List them in Notes. | 🔴 B | | | | | |
| 5.4 | If children may use the product, are age rules and parental consent handled? | 🔴 B (if applicable) | | | | | |
| 5.5 | Do we have the legal rights to all images, fonts, music, text, and data we use? | 🔴 B | | | | | |
| 5.6 | Are industry rules checked (health, finance, education, etc.)? | 🔴 B (if applicable) | | | | | |
| 5.7 | If the product shows AI-created content, are users told clearly that it is AI-made, as required? | 🟡 S | | | | | |
| 5.8 | (Apple App Store) Is the app submitted, passed review, and set to release manually? Privacy labels done? Test login given to reviewers? | 🔴 B (iOS) | | | | | |
| 5.9 | (Google Play) Is the build uploaded and approved? Data safety form done? Required test tracks completed? | 🔴 B (Android) | | | | | |
| 5.10 | (Mobile) Are app-store listing text, screenshots, icon, age rating, and support link ready? | 🟡 S | | | | | |
| 5.11 | Are payment, tax, and refund rules set up (if we charge money)? | 🔴 B (if payments) | | | | | |
| 5.12 | Is accessibility law considered for our regions (if it applies)? | 🟡 S | | | | | |

**Gate 5 sign-off:** Name: [ ] Role: Product Owner (with legal advisor)  Date: [ ]  ☐ PASS  ☐ FAIL

---

# GATE 6: CUSTOMER AND BUSINESS READINESS
**The big question: Are the people around the product ready for real customers?**

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 6.1 | Is there a help center, FAQ, or guide for the main journeys? | 🔴 B | | | | | |
| 6.2 | Is there a clear way to reach support (email, chat, form), and is someone staffed to answer during launch week? | 🔴 B | | | | | |
| 6.3 | Has the support team been trained and given the Known Issues Register (Appendix B)? | 🔴 B | | | | | |
| 6.4 | Do we have a target answer time for support (e.g., reply within 24 hours)? | 🟡 S | | | | | |
| 6.5 | Is there a way for users to report bugs and give feedback inside the product? | 🟡 S | | | | | |
| 6.6 | Do analytics measure our one success number (1.2) and the main user journey steps? Tested to be accurate? | 🔴 B | | | | | |
| 6.7 | Does the sign-up / onboarding work end to end, including emails, texts, and confirmation messages? | 🔴 B | | | | | |
| 6.8 | Do billing, plans, invoices, and cancellation work end to end (if used)? | 🔴 B (if payments) | | | | | |
| 6.9 | Is the launch announcement and customer message approved and scheduled? | 🟡 S | | | | | |
| 6.10 | Is there a message ready for problems ("We are aware of an issue…")? | 🟡 S | | | | | |
| 6.11 | Do leadership and affected teams know the launch date, the plan, and the rollback rules? | 🟡 S | | | | | |
| 6.12 | Is there a plan for who builds fixes during the first 500 customers' period, and how fast fixes can ship? | 🔴 B | | | | | |
| 6.13 | Is a "what we learned" meeting booked for after launch? | 🟢 C | | | | | |

**Gate 6 sign-off:** Name: [ ] Role: Product Owner  Date: [ ]  ☐ PASS  ☐ FAIL

---

# GATE 7: GO / NO-GO DECISION
**The big question: Based on the evidence, do we launch?**

## 7.1 Final check

| Check | Result |
|---|---|
| Gates 1-6 all signed? | ☐ Yes  ☐ No |
| Total 🔴 B questions answered `NO` and NOT covered by an approved Exception | [ ] (must be **0**) |
| Number of approved Exceptions (Appendix A) | [ ] |
| Number of open Known Issues (Appendix B) | [ ] |
| Was the checklist filled with the Release Candidate version in 0.1? | ☐ Yes  ☐ No |
| Is the rollback plan tested within the last 14 days? | ☐ Yes  ☐ No |
| Is the launch window safe? (not on a holiday / late Friday / when key people are away) | ☐ Yes  ☐ No |
| Do we have an on-call person on duty for the next 7 days? | ☐ Yes  ☐ No |

## 7.2 Instant NO-GO rules (if any are true, the answer is NO-GO)

- ☐ Any Critical bug is open.
- ☐ Any Blocker is `NO` with no approved Exception.
- ☐ Rollback has not been tested.
- ☐ No one is on call.
- ☐ A security Critical or High issue is open.
- ☐ Legal or store approval is missing.
- ☐ The version being launched differs from the version that was tested.

## 7.3 Decision

| Item | Answer |
|---|---|
| **Decision** | ☐ GO   ☐ GO with conditions   ☐ NO-GO |
| Conditions (if any) | [ ] |
| Reason for the decision (2-3 plain sentences) | [ ] |
| If NO-GO: what must happen, who does it, new review date | [ ] |

## 7.4 Signatures (humans only)

| Role | Name | Decision (GO / NO-GO) | Date and time |
|---|---|---|---|
| Final Decision Maker | | | |
| Product Owner | | | |
| Engineering Lead | | | |
| QA Lead | | | |
| Security Owner | | | |
| Operations / On-call Lead | | | |
| Support Lead | | | |
| Second reviewer (Level 3 only) | | | |

---

# GATE 8: STAGED ROLLOUT TO THE FIRST 500 CUSTOMERS
**The big question: As more people join, is everything still healthy?**

> Do not open the doors to everyone at once. Let people in slowly, and check health before letting more in. Stages below are suggestions; edit if needed.

## 8.1 Rules before starting

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 8.1 | Do we have a way to limit how many people can join (invite list, waitlist, flag, or percentage rollout)? | 🔴 B | | | | | |
| 8.2 | Did we agree on the STOP triggers (8.3) in writing before starting? | 🔴 B | | | | | |
| 8.3 | Is someone responsible for watching the dashboard at each stage and for how long? | 🔴 B | | | | | |

## 8.2 Health numbers to watch at every stage

| What we watch | Healthy range | Danger line (STOP) | Where to look |
|---|---|---|---|
| Error rate | [ ] | [ ] | [ ] |
| Crash-free sessions (mobile) | [ ] | [ ] | [ ] |
| Speed (95% of loads under) | [ ] | [ ] | [ ] |
| Sign-up completed | [ ] | [ ] | [ ] |
| Our success number (1.2) | [ ] | [ ] | [ ] |
| Support tickets per 100 users | [ ] | [ ] | [ ] |
| Payment failures (if used) | [ ] | [ ] | [ ] |
| Server and cloud cost per user | [ ] | [ ] | [ ] |
| Customer happiness (rating / survey) | [ ] | [ ] | [ ] |

## 8.3 STOP triggers (any one means pause the rollout and investigate)

- ☐ Any data loss, wrong data shown to another user, or a security problem.
- ☐ Error rate or crash rate crosses the danger line in 8.2.
- ☐ Payments charged wrongly.
- ☐ Support tickets jump above [ ] per 100 users.
- ☐ A new Critical bug appears.
- ☐ A key outside service (payment, login, AI provider) fails with no fallback.
- ☐ Other: [ ]

## 8.4 Stage tracker (fill one row per stage)

| Stage | Users allowed | Start date | Watch time before next stage | Key numbers healthy? | New bugs found | STOP trigger fired? | Decision to continue (name, date) |
|---|---|---|---|---|---|---|---|
| **A. Internal team** | ~10 | | 1-2 days | | | | |
| **B. Friendly beta** | up to 50 | | 2-3 days | | | | |
| **C. First wave** | up to 100 | | 3-5 days | | | | |
| **D. Second wave** | up to 250 | | 3-5 days | | | | |
| **E. Milestone: 500 customers** | 500 | | 7 days | | | | |

## 8.5 Questions to answer at EACH stage

| Question | A | B | C | D | E |
|---|---|---|---|---|---|
| Are all health numbers inside the healthy range? | | | | | |
| Did we fix or log every new bug found? | | | | | |
| Did support answer within our target time? | | | | | |
| Did customers complete the main journey? | | | | | |
| Did we read real customer feedback this stage? | | | | | |
| Are costs still within budget? | | | | | |
| Is the rollback plan still valid for the latest version? | | | | | |
| Did anything surprising happen that we should write down? | | | | | |

## 8.6 Changes during the rollout

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 8.4 | Is every fix released during the rollout tested and reviewed by a human (even AI-written fixes), and logged in the Decision Log? | 🔴 B | | | | | |
| 8.5 | Do we re-run the critical tests (2.2) before each new version goes out? | 🔴 B | | | | | |
| 8.6 | Do we avoid big new features until 500 customers are reached (fixes first)? | 🟡 S | | | | | |

**Gate 8 sign-off (when 500 customers are reached healthily):** Name: [ ] Role: Product Owner  Date: [ ]  ☐ DONE

---

# GATE 9: POST-LAUNCH REVIEW AND CLOSURE
**The big question: What did we learn, and what's still open?**

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| 9.1 | Did we hold a review meeting within 7 days of reaching 500 customers? | 🔴 B | | | | | |
| 9.2 | Did we compare what we expected (Part 1.2 and 1.3) with what really happened? | 🔴 B | | | | | |
| 9.3 | Are all incidents written up with cause, fix, and follow-up owner? | 🔴 B | | | | | |
| 9.4 | Does every open Known Issue now have an owner and a fix date? | 🔴 B | | | | | |
| 9.5 | Are all Exceptions (Appendix A) closed, renewed, or expired on purpose? | 🔴 B | | | | | |
| 9.6 | Were launch alerts and runbooks fixed where they were wrong or too noisy? | 🟡 S | | | | | |
| 9.7 | Was the cost per customer in line with plan? | 🟡 S | | | | | |
| 9.8 | Did the AI-driven process help or hurt? (What did AI do well? Where did human review catch problems?) | 🟡 S | | | | | |
| 9.9 | Did we update THIS template with lessons learned (see Appendix D)? | 🟡 S | | | | | |
| 9.10 | Did we hand the product over to the normal long-term support and release routine? | 🔴 B | | | | | |

## 9.1 Review summary

| Question | Your answer |
|---|---|
| Did the launch meet its goal? | ☐ Yes  ☐ Partly  ☐ No |
| Top 3 things that went well | 1. [ ]  2. [ ]  3. [ ] |
| Top 3 things to improve | 1. [ ]  2. [ ]  3. [ ] |
| Most surprising thing | [ ] |
| Suggested template changes | [ ] |

**Launch closed by:** Name: [ ] Role: Release Owner  Date: [ ]  ☐ CLOSED

---

# APPENDIX A: EXCEPTION REGISTER

> Use this ONLY when a Blocker (🔴 B) cannot be met but the team still wants to launch. An exception must be approved by the Final Decision Maker. Exceptions always expire.

| Exception ID | Question ID skipped | Why it cannot be met now | Risk if we launch (what could go wrong) | Safety step (mitigation) | Fix plan and owner | Approved by | Expiry date | Re-check trigger |
|---|---|---|---|---|---|---|---|---|
| EX-1 | | | | | | | | |
| EX-2 | | | | | | | | |

# APPENDIX B: KNOWN ISSUES REGISTER

| Issue ID | Short description | Severity (Critical / High / Medium / Low) | Who is affected | Workaround for users | Owner | Fix date | Status |
|---|---|---|---|---|---|---|---|
| KI-1 | | | | | | | |
| KI-2 | | | | | | | |

# APPENDIX C: DECISION LOG

> Any change after sign-off goes here. Never erase an old answer.

| Date and time | What changed | Why | Who decided | Gates re-checked |
|---|---|---|---|---|
| | | | | |

# APPENDIX D: HOW TO KEEP THIS TEMPLATE HEALTHY

- After every launch, copy lessons from Gate 9 into the master template.
- If a question never changes any decision across many projects, consider removing it.
- If a problem escaped to customers, add a question that would have caught it.
- Review the master template at least every 6 months.

**Template change history**

| Version | Date | Change | By |
|---|---|---|---|
| 1.0 | 2026-10-18 | First version | [ ] |

# APPENDIX E: GLOSSARY (SIMPLE WORDS)

| Word | Plain meaning |
|---|---|
| **AI agent** | A computer helper that can do tasks (like writing or testing code) on its own steps. |
| **Alert** | An automatic warning sent to a person when something is wrong. |
| **Backup** | A saved copy of data so we can get it back if it's lost. |
| **Blocker** | A problem so serious that we must not launch until it's fixed. |
| **Bug** | A mistake in the product. |
| **Canary / staged rollout** | Letting a few people use the new version first, to spot problems early. |
| **Crash-free sessions** | The share of app uses that did not crash. |
| **Dashboard** | A screen with live charts showing how healthy the product is. |
| **Evidence** | Proof anyone can open and check (link, screenshot, report). |
| **Exception** | A written, approved permission to skip a rule for a short time. |
| **Feature flag** | An on/off switch for a feature, so we can turn it off without a new release. |
| **Go / No-Go** | Final decision: launch or don't. |
| **Known issue** | A bug we know about and have written down. |
| **Migration** | A change to the database structure or data. |
| **On-call** | The person who must answer if something breaks. |
| **Regression** | An old feature that stopped working after a new change. |
| **Release Candidate (RC)** | The exact version we plan to launch. |
| **Rollback** | Going back to the last good version. |
| **Runbook** | A step-by-step guide for fixing a known problem. |
| **Staging** | A practice copy of the product that looks like the real one. |
| **UAT** | User Acceptance Testing: real users or business owners confirm it works for them. |

# APPENDIX F: AI FEATURE ADD-ON (ONLY if the product has an AI / LLM feature inside it)

> Use this ONLY if you ticked "Yes" in 0.3. Add these rules on top of Gates 1-9.

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| F.1 | Did we write down what the AI feature must do, and what it must NEVER do? | 🔴 B | | | | | |
| F.2 | Do we have a test set of real-like questions (including tricky and attack examples) with the right answers or rules? | 🔴 B | | | | | |
| F.3 | Does the AI meet our agreed quality numbers on that test set (correct answers, made-up answers rate, safe behavior)? Numbers: [ ] | 🔴 B | | | | | |
| F.4 | Did we try to trick the AI (prompt attacks, asking for harmful or private content)? | 🔴 B | | | | | |
| F.5 | Are users told they're using AI, and are limits explained? | 🟡 S | | | | | |
| F.6 | Is the model name, version, and prompt locked and versioned? | 🔴 B | | | | | |
| F.7 | What happens if the AI provider is down, slow, or too expensive? (fallback plan) | 🔴 B | | | | | |
| F.8 | Is a sample of real AI answers checked regularly by a human after launch? | 🟡 S | | | | | |
| F.9 | Can users report a bad AI answer easily? | 🟡 S | | | | | |
| F.10 | Is the AI cost per user tracked and capped? | 🟡 S | | | | | |
| F.11 | Is private user data kept from being used to train outside models unless allowed? | 🔴 B | | | | | |
| F.12 | Is there a human review step for high-risk AI answers (health, money, legal)? | 🔴 B (L3) | | | | | |

# APPENDIX G: COMMON MISTAKES

| Mistake | Better way |
|---|---|
| Filling the checklist the night before launch | Start at the beginning of testing; fill as you go. |
| Writing YES because "it should work" | Attach proof or write NO. |
| Testing an older version than the one we launch | Always note the version number and re-test if it changes. |
| Trusting AI-written tests without reading them | A human spot-checks that tests really test something. |
| Never practicing rollback | Practice it before launch and time it. |
| Launching to everyone on day one | Use the stages in Gate 8. |
| Launching on Friday evening | Pick a day when the whole team is around. |
| No one owns a question | One named person per row. |

# OPTIONAL MODULES (H to K): USE ONLY WHAT APPLIES

> Tick the modules your project needs. Each module's rows work exactly like the Gates: Answer, Evidence, Owner, Date. A skipped module needs one line of reason.

| Module | Use it when... | Needed? |
|---|---|---|
| **H. Data Migration / Existing Users** | You are moving customers or data from an older system | ☐ Yes  ☐ No: [ ] |
| **I. Accessibility and Localization Deep-Dive** | You serve many languages or regions, or accessibility rules strictly apply | ☐ Yes  ☐ No: [ ] |
| **J. Third-Party / Vendor Risk** | You depend on outside services (payments, login, email, maps, AI provider) | ☐ Yes  ☐ No: [ ] |
| **K. Marketing and Growth Readiness** | You are actively attracting the first 500 customers | ☐ Yes  ☐ No: [ ] |

## APPENDIX H: DATA MIGRATION / EXISTING USERS

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| H.1 | Is there a written list of what data moves, what is left behind, and what is deleted? | 🔴 B | | | | | |
| H.2 | Was the migration rehearsed on a full copy of real-like data at least twice? | 🔴 B | | | | | |
| H.3 | After the rehearsal, do record counts and spot-checked records match between old and new? | 🔴 B | | | | | |
| H.4 | Is there a verified backup of the old system taken right before the real migration? | 🔴 B | | | | | |
| H.5 | Can we go back to the old system if the migration fails, and for how long will the old system stay available? | 🔴 B | | | | | |
| H.6 | Do we know how long the migration takes, and what users see during it (downtime or read-only message)? | 🟡 S | | | | | |
| H.7 | Were existing users told in advance, with a clear date and what they need to do (new password, re-login, new app version)? | 🔴 B | | | | | |
| H.8 | Do old logins, passwords, subscriptions, and permissions work after migration? | 🔴 B | | | | | |
| H.9 | Are old links, bookmarks, and API addresses redirected or supported for a set time? | 🟡 S | | | | | |
| H.10 | Is personal data in old systems handled by law (kept, moved, or deleted)? | 🔴 B | | | | | |
| H.11 | Are existing users counted separately from "new" customers in the first-500 numbers? | 🟡 S | | | | | |
| H.12 | Is the date when the old system is shut down decided, and who approves it? | 🟡 S | | | | | |

## APPENDIX I: ACCESSIBILITY AND LOCALIZATION DEEP-DIVE

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| I.1 | Which accessibility standard and level are we aiming for (e.g., WCAG 2.2 AA)? Write it in Notes. | 🟡 S | | | | | |
| I.2 | Did an automated accessibility scan pass, AND did a person test with a screen reader on the main journeys? | 🟡 S (🔴 B for L3) | | | | | |
| I.3 | Do images have text descriptions, forms have labels, and videos have captions? | 🟡 S | | | | | |
| I.4 | Does everything still work with text zoomed to 200% and with reduced motion turned on? | 🟡 S | | | | | |
| I.5 | (Mobile) Do Dynamic Type / font scaling, TalkBack, VoiceOver, and dark mode work? | 🟡 S | | | | | |
| I.6 | List supported languages in Notes. Is every screen, email, and error message translated (no missing or mixed text)? | 🔴 B (per language launched) | | | | | |
| I.7 | Was the translation checked by a fluent person (not only by a machine)? | 🟡 S | | | | | |
| I.8 | Do dates, times, numbers, currencies, units, names, and addresses follow each region's format? | 🟡 S | | | | | |
| I.9 | Do languages that read right-to-left display correctly (if supported)? | 🔴 B (if supported) | | | | | |
| I.10 | Do longer translated words fit the buttons and screens without breaking the layout? | 🟡 S | | | | | |
| I.11 | Is support available in the supported languages, or is it clear which language support is in? | 🟡 S | | | | | |
| I.12 | Are the legal texts (Terms, Privacy) available in the required languages? | 🔴 B (if required) | | | | | |

## APPENDIX J: THIRD-PARTY / VENDOR RISK

> Fill one block per important outside service. Copy the table for each vendor.

**Vendor name:** [ ]  **What we use it for:** [ ]  **Owner:** [ ]

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| J.1 | Is there a signed contract or accepted terms covering our use, and has someone read the important parts? | 🔴 B | | | | | |
| J.2 | Do we know the vendor's promised uptime, support hours, and response times? | 🟡 S | | | | | |
| J.3 | Does the vendor's usage limit (requests, users, messages) cover 5x our expected launch volume? | 🔴 B | | | | | |
| J.4 | Do we know the cost at 500 users and at 5x that? Is there a spending cap or alert? | 🟡 S | | | | | |
| J.5 | Does the vendor protect our data (security certificates, data location, how they use our data)? | 🔴 B | | | | | |
| J.6 | Is there a signed data-processing agreement if personal data is shared (as required by law)? | 🔴 B (if applicable) | | | | | |
| J.7 | What happens to our product if this vendor goes down? Is there a fallback or a friendly error message? | 🔴 B | | | | | |
| J.8 | Can we leave this vendor? (We can export our data and have a rough replacement plan.) | 🟡 S | | | | | |
| J.9 | Have we subscribed to the vendor's status page or alerts? | 🟡 S | | | | | |
| J.10 | Are the vendor's API keys stored safely, separate for test and production, and can they be replaced quickly? | 🔴 B | | | | | |
| J.11 | Is the vendor's version pinned, and do we know when they plan to retire or change what we use? | 🟡 S | | | | | |
| J.12 | Did we test the vendor's production setup (real payment test, real email delivery, real login) before launch? | 🔴 B | | | | | |

## APPENDIX K: MARKETING AND GROWTH READINESS

| ID | Question | Level | Answer | Evidence | Owner | Date | Notes |
|---|---|---|---|---|---|---|---|
| K.1 | Is the target customer described in one sentence, and does the landing page speak to them? | 🟡 S | | | | | |
| K.2 | Does the landing page work on phone and desktop, load fast, and have a clear sign-up or download button? | 🔴 B | | | | | |
| K.3 | Do the sign-up and download buttons lead to the right place (right app store link, right region)? | 🔴 B | | | | | |
| K.4 | Is pricing (or "free") clear, and does it match what billing really charges? | 🔴 B | | | | | |
| K.5 | Does every channel (email, social, ads, partners) use tracking links so we can see where customers came from? | 🟡 S | | | | | |
| K.6 | Do the welcome emails or messages arrive (not in spam) and link to the right help pages? | 🔴 B | | | | | |
| K.7 | Is the plan to reach 500 customers written down (channels, budget, weekly goal)? | 🟡 S | | | | | |
| K.8 | Is the speed of marketing matched to the rollout stages in Gate 8? (We do not send more people than the stage allows.) | 🔴 B | | | | | |
| K.9 | Are all marketing claims true and provable (no promises the product cannot keep)? | 🔴 B | | | | | |
| K.10 | Are testimonials, logos, and screenshots real and used with permission? | 🔴 B | | | | | |
| K.11 | Is there a way to ask happy customers for ratings or reviews at the right moment? | 🟢 C | | | | | |
| K.12 | Do we track the funnel (visit, sign up, first use, return) so we can see where people drop off? | 🟡 S | | | | | |

---
*End of Release Readiness Criteria template. Keep this file together with the test reports, dashboards, and tickets it links to.*
