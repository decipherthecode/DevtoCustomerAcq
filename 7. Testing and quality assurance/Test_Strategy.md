# HOW TO FILL THIS DOCUMENT (Read this first, takes 3 minutes)

**What is this?** A Test Strategy is a plan that answers one big question: *"How will we make sure our product works, is safe, and is ready for real customers?"*
This file covers the whole journey: **building the product, launching it, and serving your first 500 customers**, using AI agents (like Claude) to help.

**Who can fill it?** Anyone, by hand or with an AI agent that interviews you. If you can answer questions in plain words, you can fill this in. A 10-year-old could do it by following the rules below.

## The 7 Simple Rules

1. **Go in order.** Start at Section 1 and move down. Do not skip around.
2. **Every section has the same 4 parts:**
   - **QUESTION**: what we are asking you.
   - **WHY IT MATTERS**: one sentence on why we ask.
   - **EXAMPLE**: a filled-in sample so you can copy the style.
   - **YOUR ANSWER**: the blank spot where you write.
3. **Write in short, plain words.** Short sentences. No jargon. If you use a technical word, check the Glossary (Section 36).
4. **Never leave a blank.** Write one of these instead:
   - `N/A: [reason]` means it does not apply (example: `N/A: we have no mobile app`).
   - `TBD: [owner], [date]` means not decided yet, with a person and a deadline.
   - `UNKNOWN: ask [name]` means you need help.
5. **Use numbers, not feelings.** Write "fewer than 2 seconds", not "fast". Write "0 critical bugs", not "very stable".
6. **Do not guess.** If you are not sure, use `TBD` or `UNKNOWN`. A clear "I don't know yet" is better than a wrong answer.
7. **Delete the help text when done (optional).** Lines starting with `>` are help. Keep the EXAMPLE lines if you like. Remove the rest to shorten the document.

## Two Ways to Fill This In

- **By hand:** Open the file in any text editor and type under each **YOUR ANSWER**.
- **With an AI agent:** Give the agent this file and say: *"Interview me and fill in Test_Strategy.md using Section 34."* The agent will ask one question at a time and write your answers in for you.

**Paste-and-Go Prompt** (copy this into Claude or any AI tool, then attach this file):

```text
You are my QA interview assistant. Read the attached Test_Strategy.md fully,
including the Instructions for AI Agents section (Section 34). Then interview me
to fill in every section, in order, ONE question at a time. Use the Hint lines
and EXAMPLE rows to suggest answers I can accept or change. Never leave a blank
and never invent facts: use N/A, TBD or UNKNOWN as the file explains. Push me for
numbers when I am vague. After every 5 sections, summarize and ask if it is right.
At the end, run the Completeness Checklist (Section 37), list any gaps or
conflicts, and give me the finished file. Start now with Section 0.
```

## Quick Fill Guide: What Should I Spend Time On?

| Project size | Fill these sections fully | Mark the rest as `N/A: [reason]` |
|---|---|---|
| Tiny (1 to 2 people, side project) | 1 to 5, 8 to 11, 23 to 26, 37 | Sections that do not apply |
| Medium (small team, real customers) | 1 to 33, 37 | Only the ones that truly do not apply |
| Large (company, regulated data, payments) | Everything | Nothing; justify every N/A |

## Who is Who (Roles Used in This File)

- **Owner**: the person responsible for the answer.
- **Approver**: the human who says "yes, go ahead."
- **AI Agent**: an AI helper (such as Claude) that does tasks under human rules.
- **Customer**: a real person using the product.

## Naming and Saving

- Save as: `Testing-and-Quality-Assurance/Test_Strategy.md`
- One file per project. Copy this template, rename the title below, then fill it in.
- Update the Change Log (Section 0) every time you edit.

---

# TEST STRATEGY: [PROJECT NAME]

> **Template version:** 1.2 | **Covers:** Web apps / SaaS, Mobile apps, AI / LLM-powered features | **Lifecycle:** Build → First 500 customers

---

## 0. Document Control, Owners and Change Log

**QUESTION:** Who owns this document, who reviews it, and what has changed?
**WHY IT MATTERS:** Old plans that nobody owns cause confusion and wrong decisions.

> **Hint:** Not sure who the final approver is? Pick the one person who can say "stop the launch."

**EXAMPLE:**

| Field | Value |
|---|---|
| Document owner | Priya Shah (QA Lead) |
| Reviewers | Tom Lee (Engineering), Aisha Khan (Product) |
| Final approver | Aisha Khan |
| Review frequency | Every 2 weeks and before each phase gate |

| Version | Date | Author | What changed |
|---|---|---|---|
| 0.1 | 2026-01-05 | Priya | First draft |

**YOUR ANSWER:**

| Field | Value |
|---|---|
| Document owner | |
| Reviewers | |
| Final approver | |
| Review frequency | |

| Version | Date | Author | What changed |
|---|---|---|---|
| | | | |

---

## 1. Project Snapshot

**QUESTION:** What are we building, for whom, and on which platforms?
**WHY IT MATTERS:** Everyone must picture the same product before testing it.

> **Hint:** Can't describe the product in one sentence? Try: "It helps [who] do [what] without [pain]."

**EXAMPLE:**
- Project name: FocusFlow
- One-sentence description: A to-do app that uses AI to plan your day.
- Who uses it: Busy freelancers aged 22 to 45.
- Platforms: Web, iOS, Android.
- Uses AI/LLM features? Yes: daily plan generator.
- Takes payments? Yes: monthly subscription.
- Holds personal data? Yes: email, tasks, calendar.
- Planned public launch date: 2026-06-01
- Target: first 500 paying customers by 2026-09-01

**YOUR ANSWER:**
- Project name:
- One-sentence description:
- Who uses it:
- Platforms (web / iOS / Android):
- Uses AI/LLM features? (yes/no, which):
- Takes payments? (yes/no):
- Holds personal data? (yes/no, which):
- Planned public launch date:
- Target for first 500 customers (date):
- Link to product requirements / design files:
- Link to code repository:

---

## 2. Goals: What Does "Good Quality" Mean Here?

**QUESTION:** In 3 to 5 sentences, what must be true for us to call this product "good enough to launch" and "good enough for 500 customers"?
**WHY IT MATTERS:** Without a clear goal, testing never ends or ends too early.

> **Hint:** Finish this sentence three times: "We are happy if a customer can ____ and nothing bad like ____ happens."

**EXAMPLE:**
1. Customers can sign up, pay, and create a plan in under 3 minutes.
2. The app stays online 99.5% of the time.
3. No customer data is ever shown to another customer.
4. The AI gives a harmful or made-up answer in fewer than 1 out of 100 cases.

**YOUR ANSWER:**
1.
2.
3.
4.
5.

---

## 3. Scope: What We Test and What We Do Not

**QUESTION:** List what is IN scope (we will test it) and OUT of scope (we will not test it, and why).
**WHY IT MATTERS:** Saying "no" clearly prevents surprises and wasted work.

> **Hint:** Not sure? Put it OUT of scope for now and write the reason. You can move it in later.

**EXAMPLE:**

| In scope | Out of scope (with reason) |
|---|---|
| Sign-up, login, password reset | Third-party calendar app internals (not ours) |
| AI daily plan generator | Desktop app (not planned for v1) |
| Payments via Stripe | Tax law accuracy for every country (use Stripe Tax) |

**YOUR ANSWER:**

| In scope | Out of scope (with reason) |
|---|---|
| | |

---

## 4. Lifecycle Phases and Testing Focus

**QUESTION:** For each of the 6 phases, what is the main testing goal, who tests, how many users are involved, and when does it end?
**WHY IT MATTERS:** The right kind of testing changes as the product grows from "just built" to "500 customers."

> **Hint:** Not sure about dates? Work backward from your launch date in Section 1. A common split of the time before launch: Build 60%, Alpha 10%, Beta 20%, final checks 10%.

> The 6 phases: **P1 Build → P2 Internal Alpha → P3 Closed Beta → P4 Public Launch → P5 First 100 Customers → P6 First 500 Customers.**

**EXAMPLE:**

| Phase | Main testing goal | Who tests | Number of users | End date |
|---|---|---|---|---|
| P1 Build | Code works piece by piece (unit and integration tests) | Developers + AI agents | 0 | 2026-03-15 |
| P2 Internal Alpha | Whole product works end to end | Our team | 10 | 2026-04-10 |
| P3 Closed Beta | Real people can use it without help | Invited testers | 50 | 2026-05-20 |
| P4 Public Launch | Launch day is stable and safe | Everyone | Open | 2026-06-01 |
| P5 First 100 | Fix what real customers hit | Customers + support | 100 | 2026-07-15 |
| P6 First 500 | Prove it holds up as we grow | Customers + monitoring | 500 | 2026-09-01 |

**YOUR ANSWER:**

| Phase | Main testing goal | Who tests | Number of users | End date |
|---|---|---|---|---|
| P1 Build | | | | |
| P2 Internal Alpha | | | | |
| P3 Closed Beta | | | | |
| P4 Public Launch | | | | |
| P5 First 100 | | | | |
| P6 First 500 | | | | |

---

## 5. Roles and Responsibilities

**QUESTION:** Who does what? Name a real person for every role, including a backup.
**WHY IT MATTERS:** When nobody is named, nobody does it.

> **Hint:** On a small team one person can hold many roles. Just write their name more than once. If you are solo, write your name everywhere.

**EXAMPLE:**

| Role | Person | Backup | Responsible for |
|---|---|---|---|
| Product owner | Aisha | Tom | Says what "done" means |
| QA lead | Priya | Ravi | Owns this strategy |
| Developers | Tom, Ravi | n/a | Write code and unit tests |
| AI agent supervisor | Tom | Priya | Reviews what AI agents did |
| Security contact | Mei | Tom | Security and privacy checks |
| Support lead | Jo | Aisha | Collects customer problems |
| On-call (emergencies) | Tom | Ravi | First responder when production breaks |

**YOUR ANSWER:**

| Role | Person | Backup | Responsible for |
|---|---|---|---|
| Product owner | | | |
| QA lead | | | |
| Developers | | | |
| AI agent supervisor | | | |
| Security contact | | | |
| Support lead | | | |
| On-call (emergencies) | | | |

---

## 6. AI Agents: Rules, Approval Gates and Code Checks

**QUESTION:** What may AI agents do alone, where must a human say "yes," and what extra checks apply to code written by AI?
**WHY IT MATTERS:** AI is fast but can make confident mistakes. Clear limits keep it safe.

> **Hint:** When unsure, choose "AI + human review." It is the safe default. Move a task to "AI alone" only after a month of good results.

> **Always forbidden for AI (copy as is):** touching real customer data, deploying to production without human approval, weakening/skipping/deleting a test just to make it pass, and sharing secrets or passwords.

### 6A. What AI may do

**EXAMPLE:**

| Task | AI alone | AI + human review | Forbidden for AI |
|---|---|---|---|
| Write unit and integration tests | ✔ | | |
| Run the test suite and report results | ✔ | | |
| Auto-fix a failing test or code | | ✔ | |
| Change data in the live database | | | ✔ |
| Decide to launch | | | ✔ |

**YOUR ANSWER:**

| Task | AI alone | AI + human review | Forbidden for AI |
|---|---|---|---|
| Write unit / integration / E2E tests | | | |
| Run test suites | | | |
| Auto-fix failing tests or code | | | |
| Generate test data | | | |
| Triage, label and write bug reports | | | |
| Other: | | | |

- Allowed AI tools/models (name and version):
- Where AI actions are logged (link):

### 6B. Human approval gates

**EXAMPLE:**

| Gate | What the human checks | Approver | Max wait |
|---|---|---|---|
| G1 Code merge | AI-written code reviewed, tests pass | Tom | 1 day |
| G2 Alpha start | Alpha entry criteria met | Priya | 1 day |
| G3 Beta start | Security and privacy checks passed | Mei | 2 days |
| G4 Launch | Go/No-Go checklist (Section 25) | Aisha | 1 day |
| G5 Scale to 500 | First-100 metrics healthy (Section 28) | Aisha | 2 days |

**YOUR ANSWER:**

| Gate | What the human checks | Approver | Max wait |
|---|---|---|---|
| G1 Code merge | | | |
| G2 Alpha start | | | |
| G3 Beta start | | | |
| G4 Launch | | | |
| G5 Scale to 500 | | | |

- If the approver is away, the backup is:

### 6C. Checks for AI-written code

**EXAMPLE (tick what applies):**
- [x] A human reads every AI change before merging
- [x] All existing tests still pass; new tests added (target: 80% coverage)
- [x] Security scan finds 0 high-severity issues
- [x] Every imported library really exists and is on the approved list
- [x] No secrets, keys or passwords in the code

**YOUR ANSWER (tick and edit):**
- [ ] Human review of every AI change. Reviewer:
- [ ] Existing tests pass; new tests added. Minimum coverage: ____%
- [ ] Security scan: allowed high-severity issues: ____
- [ ] Libraries checked against approved list (link):
- [ ] Secrets scan passed
- [ ] Other rules:

---

## 7. Risk Assessment

**QUESTION:** What are the top things that could go wrong, and how bad and likely is each?
**WHY IT MATTERS:** We test the scariest things first.

> **Hint:** Ask: "If this went wrong on launch day, how upset would customers be?" Impact 5 = money lost, data leaked, or someone harmed. Common risks: payments, data leaks, wrong AI answers, crashes, app store rejection.

> Score **Likelihood** and **Impact** from 1 (low) to 5 (high). **Priority = Likelihood × Impact.** Test anything 15 or above first.

**EXAMPLE:**

| # | Risk | Likelihood | Impact | Priority | How we reduce it |
|---|---|---|---|---|---|
| 1 | Customer is charged twice | 2 | 5 | 10 | Payment tests + duplicate checks |
| 2 | AI gives harmful advice | 3 | 5 | 15 | Safety evals + human review |
| 3 | App crashes at launch traffic | 3 | 4 | 12 | Load test |

**YOUR ANSWER:**

| # | Risk | Likelihood (1-5) | Impact (1-5) | Priority | How we reduce it |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

---

## 8. Test Levels and Types

**QUESTION:** Which kinds of tests will we do, who does them, and how often?
**WHY IT MATTERS:** Each type catches a different kind of problem.

> **Hint:** Not sure about targets? Start with: unit tests 80% coverage, E2E tests for the top 10 customer journeys, smoke tests 100% pass. Raise them later.

**EXAMPLE:**

| Test type | Plain meaning | Who | When | Target |
|---|---|---|---|---|
| Unit | Tests one tiny piece of code | Developers + AI | Every code change | 80% coverage |
| Integration | Tests pieces working together | Developers + AI | Every code change | All key links covered |
| End-to-end (E2E) | Pretends to be a user, start to finish | QA + AI | Every night | Top 10 journeys pass |
| Smoke | Quick "is it alive?" check | Automatic | After every release | 100% pass |
| Regression | Checks old features still work | Automatic | Every release | 100% pass |
| Exploratory | A human pokes around with no script | QA | Before each phase gate | 2 hours per session |
| User acceptance (UAT) | Real users confirm it solves their problem | Beta testers | Phase 3 | 90% say "yes" |

**YOUR ANSWER:**

| Test type | Plain meaning | Who | When | Target |
|---|---|---|---|---|
| Unit | | | | |
| Integration | | | | |
| End-to-end (E2E) | | | | |
| Smoke | | | | |
| Regression | | | | |
| Exploratory | | | | |
| User acceptance (UAT) | | | | |
| Other: | | | | |

---

## 9. Test Environments

**QUESTION:** Where do we run tests, and how is each place different from the real product?
**WHY IT MATTERS:** Testing in the wrong place gives false comfort.

> **Hint:** Minimum is 3 places: your own computer, a practice copy (staging), and the real product.

**EXAMPLE:**

| Environment | Purpose | Real customer data? | Who can use it | Link |
|---|---|---|---|---|
| Local | Developers build and try | No | Developers | n/a |
| Test (CI) | Automatic test runs | No (fake data) | Machines | ci.example.com |
| Staging | Looks like the real thing, final check | No (fake data) | Team + beta testers | staging.example.com |
| Production | The real product | Yes | Customers | app.example.com |

**YOUR ANSWER:**

| Environment | Purpose | Real customer data? | Who can use it | Link |
|---|---|---|---|---|
| Local | | | | |
| Test (CI) | | | | |
| Staging | | | | |
| Production | | | | |

- How often Staging is refreshed to match Production:
- Who fixes an environment when it breaks:

---

## 10. Test Data

**QUESTION:** What data do we use for testing, where does it come from, and how do we keep it safe?
**WHY IT MATTERS:** Using real people's data in tests can break privacy laws.

> **Hint:** Golden rule: never put real customer data in test places. Fake it.

**EXAMPLE:**
- Source: Fake data generated by a script (never copied from production).
- Reset: Wiped and rebuilt every night.
- Sensitive data: Fake emails use `@example.com`; fake cards use payment-provider test cards only.
- Who owns it: Priya.

**YOUR ANSWER:**
- Source:
- How it is reset/refreshed:
- How sensitive data is protected or faked:
- Who owns it:
- Can AI agents create test data? (yes/no, rules):

---

## 11. Test Automation, Tools and CI/CD

**QUESTION:** Which tools run our tests, and what happens automatically?
**WHY IT MATTERS:** Automation makes testing repeatable and catches problems early.

> **Hint:** Don't know the tools? Ask your developer or AI agent for popular, well-supported options for your tech stack, and write TBD with a name and date.

**EXAMPLE:**

| Need | Tool | Runs when |
|---|---|---|
| Unit tests | Jest | Every code push |
| Web E2E tests | Playwright | Every night |
| Mobile E2E tests | Maestro | Before each release |
| Build and release | GitHub Actions | Every code push |
| Bug tracker | Linear | Always |
| Error monitoring | Sentry | Always (production) |

> **Automatic stop rule example:** If any test marked "critical" fails, the release is blocked automatically.

**YOUR ANSWER:**

| Need | Tool | Runs when |
|---|---|---|
| Unit tests | | |
| Web E2E tests | | |
| Mobile E2E tests | | |
| Build and release (CI/CD) | | |
| Bug tracker | | |
| Error monitoring | | |
| Test reports | | |

- Automatic stop rule(s):
- Flaky test policy (a flaky test passes and fails randomly). What do we do? (example: fix or quarantine within 3 days):

---

## 12. AI / LLM Feature Testing

**QUESTION:** How do we test the parts of the product powered by AI? (Answer `N/A: no AI features` if none.)
**WHY IT MATTERS:** AI can give different answers every time, so normal tests are not enough.

> **Hint:** Start small: 50 test questions beat zero. Get real questions from customer support, beta testers or your own team.

**EXAMPLE:**

| What we check | How | Pass line |
|---|---|---|
| Correct answers | 200 saved test questions with approved answers | 90% correct |
| Made-up facts (hallucination) | Human + automatic check | Under 2% |
| Harmful or unsafe answers | 100 tricky "red team" prompts | 0 unsafe answers |
| Prompt injection (someone tricks the AI) | 50 attack prompts | 0 successes |
| Private data leaks | Prompts asking for other users' data | 0 leaks |
| Speed | Time to first answer | Under 3 seconds (95% of the time) |
| Cost | Cost per customer per day | Under $0.05 |
| Model or prompt change | Re-run all of the above | Required every time |

**YOUR ANSWER:**

| What we check | How | Pass line |
|---|---|---|
| Correct answers | | |
| Made-up facts (hallucination) | | |
| Harmful or unsafe answers | | |
| Prompt injection | | |
| Private data leaks | | |
| Speed | | |
| Cost | | |
| Re-test when model or prompt changes | | |
| Fairness / bias | | |

- Where the saved list of test questions ("eval set") lives (link):
- Who approves changes to prompts or models:
- What the product does when the AI fails or is down (fallback message/behavior):

---

## 13. Security and Privacy Testing

**QUESTION:** How do we make sure customer data and accounts are safe?
**WHY IT MATTERS:** One leak can end a young product.

> **Hint:** If you are unsure which privacy laws apply, write UNKNOWN: ask [lawyer]. Laws depend on where your customers live.

**EXAMPLE:**
- Login tests: wrong password locks the account after 5 tries.
- Customer A can never see Customer B's data (tested every release).
- Automatic scan for known weaknesses (OWASP Top 10) on every code push.
- Outside penetration test before Phase 3.
- Privacy laws that apply: GDPR, CCPA.
- Data deletion request test: customer data fully removed within 30 days.

**YOUR ANSWER:**
- Login and access tests:
- Data separation tests (customer A vs B):
- Automatic security scans (tool, how often):
- Outside penetration test (who, when):
- Privacy laws that apply to us:
- Data export and deletion tests:
- Who is told, and how fast, if a leak happens:

---

## 14. Accessibility Testing

**QUESTION:** How do we make sure people with disabilities can use the product?
**WHY IT MATTERS:** It is the right thing to do, and often required by law.

> **Hint:** Easy start: use the free accessibility tools built into browsers and phones, and try the whole product using only a keyboard.

**EXAMPLE:**
- Standard: WCAG 2.2 level AA.
- Automatic checks: axe on every page, 0 serious issues.
- Manual checks: keyboard-only use, screen reader (VoiceOver, TalkBack), 200% zoom, color contrast.
- Done before: Phase 3.

**YOUR ANSWER:**
- Standard we follow:
- Automatic checks (tool, pass line):
- Manual checks:
- Done before which phase:

---

## 15. Payments and Billing Testing

**QUESTION:** How do we make sure money is handled correctly? (Answer `N/A: no payments` if none.)
**WHY IT MATTERS:** Money mistakes destroy customer trust fast.

> **Hint:** Never use real cards. Every payment company provides fake test cards. Search "[provider name] test cards."

**EXAMPLE (tick what applies):**
- [x] Successful payment, failed card, expired card
- [x] Refunds and cancellations
- [x] Free trial turning into paid
- [x] Upgrade, downgrade, pause
- [x] Duplicate charge protection
- [x] Taxes and currencies
- [x] Invoices and receipts emailed correctly
- Payment provider test mode only. Never real cards.

**YOUR ANSWER:**
- [ ] Successful payment, failed card, expired card
- [ ] Refunds and cancellations
- [ ] Free trial to paid
- [ ] Upgrade, downgrade, pause
- [ ] Duplicate charge protection
- [ ] Taxes and currencies
- [ ] Invoices and receipts
- Payment provider and its test mode:
- Who reconciles money reports and how often:

---

## 16. Localization, Browsers and Devices

**QUESTION:** Which languages, countries, browsers, phones and screens must work?
**WHY IT MATTERS:** Customers use all kinds of devices, and we cannot test them all, so we choose smartly.

> **Hint:** Look at your analytics, your first 50 sign-ups, or competitors' audience. Aim to cover about 90% of the people you expect.

**EXAMPLE:**

| Category | Must work on |
|---|---|
| Languages | English, Spanish |
| Time zones / currencies | US, UK, EU (USD, GBP, EUR) |
| Browsers | Latest 2 versions of Chrome, Safari, Edge, Firefox |
| iPhones | iOS 17 and 18 (iPhone 12 and newer) |
| Android | Android 13 and 14 (Samsung, Pixel) |
| Screen sizes | Phone, tablet, laptop |

> Tip: Pick these using your analytics or target-market data.

**YOUR ANSWER:**

| Category | Must work on |
|---|---|
| Languages | |
| Time zones / currencies | |
| Browsers | |
| iPhones | |
| Android phones | |
| Screen sizes | |
| Slow internet / offline behavior | |

---

## 17. Third-Party Integrations

**QUESTION:** Which outside services does our product depend on (login, email, payments, calendar, analytics, AI model provider), and how do we test them?
**WHY IT MATTERS:** When someone else's service breaks, our customers still blame us.

> **Hint:** List every outside service you log into, pay for, or call from your product code. If you are unsure, ask a developer.

**EXAMPLE:**

| Service | What it does for us | How we test it | If it is down, we... | Owner |
|---|---|---|---|---|
| Stripe | Payments | Test mode + mock | Show "try again later," retry in 1 hour | Tom |
| SendGrid | Emails | Sandbox inbox | Queue emails and resend | Ravi |
| Google Calendar | Sync tasks | Test account | Pause sync, keep app working | Ravi |
| AI model provider | Daily plan | Mock + live check nightly | Show saved plan | Tom |

**YOUR ANSWER:**

| Service | What it does for us | How we test it | If it is down, we... | Owner |
|---|---|---|---|---|
| | | | | |

- How we find out an outside service changed or is failing (alerts, status pages):
- Contract/version check frequency:

---

## 18. App Store and Release Readiness

**QUESTION:** What must be ready so the web app and mobile apps can actually be released without delays or rejections? (Answer `N/A: [reason]` for platforms you do not have.)
**WHY IT MATTERS:** Apple and Google can reject an app, and review can take days. A rejection can wreck a launch date.

> **Hint:** Apple and Google reviews can take hours to several days, and rejections happen. Submit early and keep spare days in your schedule.

**EXAMPLE (tick what applies):**
- [x] Test builds shared via TestFlight (iOS) and Play Internal Testing (Android)
- [x] Privacy details and permission texts match what the app really does
- [x] Screenshots, description, age rating, support link ready
- [x] Store review rules checked (Apple App Store, Google Play)
- [x] Version numbers and release notes ready
- [x] Submitted at least 7 days before launch date
- [x] Staged rollout planned (10% → 50% → 100%)
- [x] Plan to force old app versions to update if a serious bug appears
- Web release: deploys at 10:00 on weekdays only, never Friday afternoon.

**YOUR ANSWER:**
- [ ] Test build channels (TestFlight / Play Internal Testing / other):
- [ ] Privacy details and permission texts match the app
- [ ] Store listing assets ready (screenshots, description, age rating, support link)
- [ ] Store rules checked (who, when):
- [ ] Version numbering and release notes owner:
- [ ] Submit by (days before launch):
- [ ] Staged rollout plan:
- [ ] Force-update plan for old versions:
- Web release rules (days/times, who clicks deploy):

---

## 19. Data Migration and Backward Compatibility

**QUESTION:** When we change the product (new version, database changes, new app version), how do we make sure old customers, old data and old app versions keep working?
**WHY IT MATTERS:** Customers do not update on your schedule, and a bad data change often cannot be undone.

> **Hint:** Ask: "If we ship version 2 tomorrow, who still has version 1?" The answer shows what to test.

**EXAMPLE:**
- Oldest app version we still support: 2 versions back (iOS 3.1 and Android 3.1).
- Database changes are tested on a copy of staging data first, can be reversed, and run at a quiet time.
- After a migration we check: number of records before = after (0 lost).
- Old app version talking to the new server: tested every release.
- If a migration fails: stop, restore from backup, tell customers (Section 27).
- Importing data from other tools (CSV): tested with 5 sample files, including a broken one.

**YOUR ANSWER:**
- Oldest app/web version we still support:
- How database or data changes are tested and reversed:
- What we check after every migration (and the pass line):
- How old app versions are tested against the new server:
- Import / export features to test (formats, sample files):
- What we do if a migration fails:

---

## 20. Legal, Terms and Consent Testing

**QUESTION:** Do all the legal screens and promises in the product really work (terms, privacy policy, consent, cookie banners, marketing opt-in, age checks, unsubscribe)?
**WHY IT MATTERS:** A broken consent or unsubscribe link can bring fines, angry customers and app store rejection. (QA checks that these things work. A lawyer decides what is required. This template is not legal advice.)

> **Hint:** Not sure what you need? Write UNKNOWN: ask [lawyer] and still test every consent and unsubscribe button you already have.

**EXAMPLE (tick what applies):**
- [x] Customer must accept Terms and Privacy Policy at sign-up, and we store when they accepted
- [x] Cookie banner: "Reject all" really stops non-essential tracking
- [x] Marketing emails only go to people who said yes
- [x] Every email has a working unsubscribe link (works within 10 days at most)
- [x] Age check or age rating matches who is allowed to use the product
- [x] Changed terms: customers are asked to accept again
- [x] Delete-my-account and download-my-data buttons work

**YOUR ANSWER:**
- [ ] Terms and Privacy acceptance recorded (what, when):
- [ ] Cookie / tracking consent works (tool, how tested):
- [ ] Marketing opt-in and unsubscribe work:
- [ ] Age check or age rating matches the audience:
- [ ] Re-acceptance when terms change:
- [ ] Delete-account and data-download work:
- Who from legal reviews the texts (name, date):

---

## 21. Analytics and Tracking Checks

**QUESTION:** How do we make sure the numbers we use to judge success (sign-ups, payments, crashes, AI usage) are counted correctly?
**WHY IT MATTERS:** Wrong numbers lead to wrong decisions, such as scaling from 100 to 500 customers when the product is not ready (Section 28).

> **Hint:** Pick 5 to 10 events that decide success (sign-up, payment, first key action, crash). Start there, not with everything.

**EXAMPLE:**

| Event we track | Fires when | How we check it | Owner |
|---|---|---|---|
| sign_up_completed | Customer finishes sign-up | Test account + compare with database | Priya |
| payment_succeeded | Payment goes through | Test card + compare with payment provider | Tom |
| ai_plan_created | AI plan shown | Test run + compare with logs | Ravi |
| app_crash | App closes unexpectedly | Forced test crash | Ravi |

- Rule: no personal data in analytics unless the customer consented (Section 20).
- Dashboards are checked against the real database once a week during Phases 3 to 6.

**YOUR ANSWER:**

| Event we track | Fires when | How we check it | Owner |
|---|---|---|---|
| | | | |

- Analytics tools used:
- Personal data rules for analytics:
- How often dashboards are checked against real data:

---

## 22. Performance, Load and Reliability

**QUESTION:** How fast and how stable must the product be, and with how many users at once?
**WHY IT MATTERS:** Launch day and growth to 500 customers put real pressure on the system.

> **Hint:** Not sure about numbers? Use: page load under 2 seconds, uptime 99.5%, error rate under 1%. Adjust with real data in Phase 5.

**EXAMPLE:**

| Measure | Target |
|---|---|
| Page load time | Under 2 seconds (95% of users) |
| Users at the same time (launch test) | 1,000 |
| Uptime | 99.5% |
| Error rate | Under 1% of requests |
| Data backup restore test | Works within 1 hour, tested before launch |

**YOUR ANSWER:**

| Measure | Target |
|---|---|
| Page / screen load time | |
| App start time (mobile) | |
| Users at the same time (test size) | |
| Uptime | |
| Error rate | |
| Backup and restore test | |

---

## 23. Bug Management

**QUESTION:** How do we label, track and fix bugs?
**WHY IT MATTERS:** Everyone must agree what "critical" means.

> **Hint:** Use the same words for severity everywhere. Rule of thumb: money, security, data loss or "product is down" = Critical.

**EXAMPLE:**

| Severity | Meaning | Fix within |
|---|---|---|
| Critical | Data loss, security hole, payments broken, product down | 24 hours |
| High | Main feature broken, no workaround | 3 days |
| Medium | Feature broken, workaround exists | Next release |
| Low | Small visual or wording issue | When time allows |

- Where bugs are reported: Linear, label `bug`.
- Every bug report must include: steps, what happened, what should happen, screenshot/video, device and version.
- Who decides severity: Priya.

**YOUR ANSWER:**

| Severity | Meaning | Fix within |
|---|---|---|
| Critical | | |
| High | | |
| Medium | | |
| Low | | |

- Where bugs are reported:
- Required details in every bug report:
- Who decides severity:
- Can AI agents file or label bugs? (rules):

---

## 24. Entry and Exit Criteria for Each Phase

**QUESTION:** What must be true to START a phase (entry) and to FINISH it (exit)?
**WHY IT MATTERS:** It stops us from moving forward too soon.

> **Hint:** Copy entry and exit rules into Section 25 (Go/No-Go) as numbers. Keep both sections consistent.

**EXAMPLE:**

| Phase | Entry (can we start?) | Exit (can we finish?) |
|---|---|---|
| P2 Alpha | All main features built, unit tests pass | 0 critical bugs, 90% E2E tests pass |
| P3 Beta | Alpha exit met, security scan clean | 0 critical, under 5 high bugs, 80% of testers satisfied |
| P4 Launch | Beta exit met, Go/No-Go passed | Launch day stable for 24 hours |
| P5 First 100 | Launch stable | 0 critical open, support replies under 24 hours |
| P6 First 500 | First-100 healthy | See Section 28 |

**YOUR ANSWER:**

| Phase | Entry (can we start?) | Exit (can we finish?) |
|---|---|---|
| P1 Build | | |
| P2 Alpha | | |
| P3 Beta | | |
| P4 Launch | | |
| P5 First 100 | | |
| P6 First 500 | | |

---

## 25. Go / No-Go Launch Checklist

**QUESTION:** What exact numbers must we hit before we launch publicly?
**WHY IT MATTERS:** It replaces "I think we're ready" with facts.

> **Hint:** Each line must be provable with a number or a yes/no. If you cannot measure it, rewrite it until you can.

> One failed "must pass" item = **No-Go**. The approver decides in writing.

**EXAMPLE:**

| Check | Must pass | Result | Pass? |
|---|---|---|---|
| Critical bugs open | 0 | 0 | ✔ |
| High bugs open | 3 or fewer | 2 | ✔ |
| Automated tests passing | 95% or more | 97% | ✔ |
| Security scan high issues | 0 | 0 | ✔ |
| Load test at 1,000 users | Passed | Passed | ✔ |
| AI safety test unsafe answers | 0 | 0 | ✔ |
| Payments tested end to end | Passed | Passed | ✔ |
| Accessibility serious issues | 0 | 0 | ✔ |
| App store submissions approved | Approved | Approved | ✔ |
| Backup restore tested | Passed | Passed | ✔ |
| Rollback plan tested | Passed | Passed | ✔ |
| Support team trained | Yes | Yes | ✔ |

**Decision:** GO. **Approver:** Aisha. **Date:** 2026-05-30.

**YOUR ANSWER:**

| Check | Must pass | Result | Pass? |
|---|---|---|---|
| Critical bugs open | | | |
| High bugs open | | | |
| Automated tests passing | | | |
| Security scan high issues | | | |
| Load test | | | |
| AI safety (unsafe answers) | | | |
| Payments tested end to end | | | |
| Accessibility serious issues | | | |
| App store submissions approved | | | |
| Backup restore tested | | | |
| Rollback plan tested | | | |
| Support team trained | | | |
| Other: | | | |

- Decision (GO / NO-GO):
- Approver:
- Date:
- Reason in 2 sentences:

---

## 26. Rollback and Kill Switch Plan

**QUESTION:** If launch goes wrong, how do we undo it fast, and how do we turn off a risky feature (especially AI)?
**WHY IT MATTERS:** Every launch needs an emergency exit.

> **Hint:** Ask: "Can we undo this in under 10 minutes?" If not, make a smaller release or add a feature flag.

**EXAMPLE:**
- Rollback: One-click return to the previous version, takes under 10 minutes.
- Kill switch: Feature flag `ai_plan_generator` can be turned off in 1 minute.
- Triggers: Error rate above 5% for 10 minutes, any data leak, any double-charge bug.
- Who can press the button: Tom or Aisha (phone list in Section 5).
- Customer message ready: Yes, link:

**YOUR ANSWER:**
- Rollback method and time:
- Kill switch(es) and time to use:
- Triggers (when we must roll back):
- Who can press the button:
- Customer message ready? (link):
- Date rollback was last practiced:

---

## 27. Incident Response and Disaster Recovery

**QUESTION:** When something breaks in production (outage, data leak, bad AI answer, payment bug), who does what, how fast, and how do we recover?
**WHY IT MATTERS:** Problems will happen. Customers remember how fast and honestly you fixed them.

> **Hint:** Pretend it is 3 a.m. and the product is down. Who is woken up, and what do they do first? Write that.

**EXAMPLE:**

| Incident level | Example | First response in | Who leads | Customers told in |
|---|---|---|---|---|
| Level 1 (worst) | Data leak, product down, wrong charges | 15 minutes | Tom | 1 hour |
| Level 2 | Main feature broken for many | 1 hour | Ravi | 4 hours |
| Level 3 | Small group affected | 1 working day | Support | Only if asked |

- Recovery goals: restore service within 1 hour (RTO); lose at most 15 minutes of data (RPO).
- Backups: automatic every 15 minutes, restore tested every quarter.
- Where customers see status: status.example.com.
- After every Level 1 or 2 incident: write a "what happened and how we prevent it" review within 3 days, with no blame.
- Practice drill: once before launch, then every 6 months.

**YOUR ANSWER:**

| Incident level | Example | First response in | Who leads | Customers told in |
|---|---|---|---|---|
| Level 1 (worst) | | | | |
| Level 2 | | | | |
| Level 3 | | | | |

- Recovery goals (time to restore, max data loss):
- Backups (how often, last restore test date):
- Where customers see status:
- Review after incidents (who writes, within how many days):
- Practice drill (date of last, date of next):

---

## 28. Beta, First 100 and First 500 Customer Validation

**QUESTION:** How do we learn from real customers and decide when we are ready to grow from 100 to 500?
**WHY IT MATTERS:** Real customers find problems no test can.

> **Hint:** Move from 100 to 500 only when the numbers are healthy for at least 2 weeks in a row. Growth hides problems.

**EXAMPLE:**

| Measure | Beta (50) | First 100 | First 500 |
|---|---|---|---|
| Customers who finish sign-up | 70% | 75% | 80% |
| Crash-free sessions | 98% | 99% | 99.5% |
| Support tickets per customer per month | under 1 | under 0.7 | under 0.5 |
| Customer satisfaction (1 to 10) | 7 | 8 | 8 |
| Critical bugs found by customers | under 3 | under 2 | under 1 |

- How we collect feedback: in-app form, weekly 15-minute calls with 5 customers.
- How we roll out: 10% of customers first, then 50%, then 100% (staged rollout).
- Rule to move from 100 to 500: all P5 targets met for 2 weeks in a row.

**YOUR ANSWER:**

| Measure | Beta | First 100 | First 500 |
|---|---|---|---|
| Sign-up completion | | | |
| Crash-free sessions | | | |
| Support tickets per customer per month | | | |
| Customer satisfaction | | | |
| Critical bugs found by customers | | | |
| Other: | | | |

- How we collect feedback:
- How we roll out gradually (staged rollout):
- Rule to move from 100 to 500:
- Who watches the live product and where (dashboard link):

---

## 29. Metrics and Reporting

**QUESTION:** Which numbers do we track, who sees them, and how often?
**WHY IT MATTERS:** What is measured gets managed.

> **Hint:** Pick 5 to 8 numbers. Too many numbers means nobody reads them.

**EXAMPLE:**

| Metric | Goal | Reported to | How often |
|---|---|---|---|
| Test pass rate | 95% or more | Whole team | Daily |
| Open bugs by severity | See Section 25 | Product owner | Weekly |
| Test coverage | 80% or more | Engineering | Weekly |
| Time to fix critical bugs | Under 24 h | Product owner | Weekly |
| AI answer quality score | 90% or more | Product + QA | Every AI change |
| Escaped bugs (found by customers) | Falling each week | Everyone | Weekly |

**YOUR ANSWER:**

| Metric | Goal | Reported to | How often |
|---|---|---|---|
| Test pass rate | | | |
| Open bugs by severity | | | |
| Test coverage | | | |
| Time to fix critical bugs | | | |
| AI answer quality score | | | |
| Escaped bugs | | | |

- Where the report is kept (link):

---

## 30. Testing Cost and Budget

**QUESTION:** How much will testing cost (tools, devices, outside experts, AI usage), and what do we cut first if money runs short?
**WHY IT MATTERS:** Testing that runs out of money mid-project leaves gaps exactly when risk is highest.

> **Hint:** Not sure about costs? Write TBD: [owner], [date] and ask your tool vendors for price pages. Always set a cap for AI usage.

**EXAMPLE:**

| Cost item | Monthly cost | Notes |
|---|---|---|
| Test tools and CI minutes | $300 | Playwright, GitHub Actions |
| Device lab (real phones) | $250 | Cloud device service |
| AI tokens for running evals and AI agents | $400 | Cap: $500; alert at $400 |
| Outside penetration test | $5,000 (one time) | Before Beta |
| Total | about $950/month + $5,000 once | |

- Cut first if over budget: nightly full E2E → weekly; keep security and payments tests no matter what.
- Budget owner: Aisha.

**YOUR ANSWER:**

| Cost item | Monthly cost | Notes |
|---|---|---|
| Test tools and CI | | |
| Device lab | | |
| AI tokens (evals + agents), with cap and alert | | |
| Outside security / accessibility experts | | |
| Other: | | |
| Total | | |

- What we cut first if over budget (and what we never cut):
- Budget owner:

---

## 31. Schedule and Milestones

**QUESTION:** When does each testing activity happen?
**WHY IT MATTERS:** Testing squeezed into the last week always fails.

> **Hint:** Work backward from launch day and the app store submission date. Add a buffer of at least one week.

**EXAMPLE:**

| Activity | Start | End | Owner |
|---|---|---|---|
| Write tests alongside code | 2026-01-10 | 2026-03-15 | Developers |
| Security penetration test | 2026-04-15 | 2026-04-30 | Mei |
| Load test | 2026-05-10 | 2026-05-15 | Tom |
| App store submission | 2026-05-18 | 2026-05-25 | Ravi |
| Go/No-Go meeting | 2026-05-30 | 2026-05-30 | Aisha |

**YOUR ANSWER:**

| Activity | Start | End | Owner |
|---|---|---|---|
| | | | |

---

## 32. Assumptions, Dependencies and Constraints

**QUESTION:** What are we assuming is true, what do we depend on, and what limits us?
**WHY IT MATTERS:** Hidden assumptions are the top cause of surprises.

> **Hint:** Write down anything you hope is true but have not checked. That is an assumption.

**EXAMPLE:**
- Assumption: Payment provider test mode behaves like real mode.
- Dependency: AI model provider stays available and keeps pricing the same.
- Constraint: Only 2 QA people; budget as in Section 30.

**YOUR ANSWER:**
- Assumptions:
- Dependencies (other teams, vendors):
- Constraints (time, money, people):

---

## 33. Open Questions and Decision Log

**QUESTION:** What have we not decided yet, and what did we decide along the way?
**WHY IT MATTERS:** Prevents re-arguing old decisions and forgetting open ones.

> **Hint:** Log decisions as soon as you make them. Future you will forget why.

**EXAMPLE:**

| # | Question / Decision | Owner | Due | Status |
|---|---|---|---|---|
| 1 | Which device lab to rent? | Priya | 2026-03-01 | Open |
| 2 | Chose Playwright for web E2E | Tom | 2026-01-15 | Decided |

**YOUR ANSWER:**

| # | Question / Decision | Owner | Due | Status |
|---|---|---|---|---|
| | | | | |

---

## 34. Instructions for AI Agents (Machine-Readable Block)

**QUESTION:** What must an AI agent read and obey when it helps fill this document or follows it during testing?
**WHY IT MATTERS:** AI agents work best with clear, explicit rules and no room for guessing.

> Copy this block as is, then edit the project-specific lines under YOUR ANSWER.

```text
ROLE
  You are a QA assistant for [PROJECT NAME]. This file (Test_Strategy.md) is the
  single source of truth. If a chat message conflicts with it, ask a human.

MODE 1: INTERVIEW (when asked to fill in this template)
  1. Read "HOW TO FILL THIS DOCUMENT" first.
  2. Go section by section, in order (0 to 37). Do not skip.
  3. For each section: show the QUESTION in plain words and the EXAMPLE, then
     ask ONE question at a time. Offer 2 to 4 suggested answers when possible.
  4. Write the person's answer under YOUR ANSWER. Do not edit QUESTION, WHY IT
     MATTERS, or EXAMPLE text. Use the Hint lines to suggest answers.
  5. If an answer is vague ("fast", "good", "soon"), ask for a number or date.
  6. If the person does not know: write TBD: [owner], [date] or UNKNOWN: ask [name].
     If it does not apply: write N/A: [reason]. Never leave a blank. Never invent facts.
  7. After every 5 sections, summarize what was filled and ask "Is this right?"
  8. At the end, run Section 37 (Completeness Checklist), list gaps, and ask the
     person to fix or approve each one.
  9. Check for conflicts: dates in Section 4 vs Section 31, owners in Section 5 vs
     later sections, numbers in Section 24 vs Section 25. Point out every mismatch.

MODE 2: TESTING (when helping test the product)
  - Obey Section 6A (what AI may do), 6B (approval gates), 6C (code checks).
  - Never touch production or real customer data.
  - Never weaken, skip, or delete a test only to make it pass.
  - Never share secrets, keys, or passwords.
  - Log every action and result to the location in Section 6A.

STOP AND ASK A HUMAN WHEN
  - A critical or security issue is found.
  - A gate in Section 6B is reached.
  - Requirements are unclear or conflict.
  - A change affects payments, privacy, or AI safety.
  - You are about to do something outside Section 6A.

REPORT FORMAT
  What I did / What passed / What failed / What I need from a human.

STYLE
  Plain words. Short sentences. Numbers instead of adjectives. One question at a time.
```

**YOUR ANSWER (project-specific edits):**
- Project name:
- Log location:
- Extra rules:

---

## 35. Sign-Off

**QUESTION:** Who agrees this strategy is ready to follow?
**WHY IT MATTERS:** Shared agreement means shared responsibility.

| Name | Role | Decision (Approve / Changes needed) | Date |
|---|---|---|---|
| | Product owner | | |
| | QA lead | | |
| | Engineering lead | | |
| | Security contact | | |

---

## 36. Glossary (Plain-English Definitions)

| Word | Simple meaning |
|---|---|
| **Test strategy** | The big-picture plan for how we check quality |
| **Unit / integration / E2E test** | Test one piece / pieces together / the whole thing like a user |
| **Smoke test** | A fast check that the product is alive |
| **Regression test** | Checks old features did not break |
| **Staging / Production** | A practice copy / the real product customers use |
| **CI/CD** | Robots that build, test and release automatically |
| **Flaky test** | A test that passes and fails randomly |
| **Severity** | How bad a bug is |
| **Entry / exit criteria** | Rules to start / finish a phase |
| **Go / No-Go** | The decision to launch or not |
| **Rollback / kill switch** | Go back to the previous version / turn a risky feature off |
| **Staged rollout** | Give the product to a few people first, then more |
| **LLM / hallucination** | The AI "brain" / AI confidently saying something false |
| **Prompt injection** | Someone tricking the AI with sneaky instructions |
| **Eval set / red teaming** | A saved list of questions that scores the AI / trying on purpose to make it fail |
| **WCAG / OWASP** | World standard for accessible websites / list of common web security problems |
| **RTO / RPO** | How fast we recover / how much data we can afford to lose |
| **Escaped bug** | A bug customers found instead of us |

---

## 37. Completeness Checklist (Do This Last)

Tick every box. If any is unticked, go back and fix it.

**Filled in**
- [ ] No section is blank. Every blank is `N/A: reason`, `TBD: owner, date`, or `UNKNOWN: ask name`.
- [ ] Every role in Section 5 has a real name and a backup.
- [ ] Every gate in Section 6B has an approver and a backup.
- [ ] All 6 phases have dates and numbers (Sections 4 and 24).

**Clear**
- [ ] Every target is a number (no "fast", "stable", "good").
- [ ] Every link works.
- [ ] Dates in Sections 4 and 31 agree. Numbers in Sections 24 and 25 agree.
- [ ] A new person could read this and know what to do without asking you.

**Safe**
- [ ] AI limits, approval gates and code checks are written (Section 6).
- [ ] Rollback, kill switch and incident response are written and practiced (Sections 26 and 27).
- [ ] Security, privacy, payments, accessibility, integrations, app store readiness, data migration, legal/consent and analytics are covered or marked N/A with a reason.
- [ ] Budget and a "never cut" list exist (Section 30).

**Final**
- [ ] Go/No-Go checklist numbers are set (Section 25).
- [ ] Change log updated (Section 0).
- [ ] Sign-off collected (Section 35).

**Completed by:** ______________  **Date:** ______________
