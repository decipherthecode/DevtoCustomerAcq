---
document: Testing.md
template_version: 1.0.0
project_name: ""            # e.g. "PlantPal"
project_version: ""         # e.g. "0.1.0"
product_type: []            # choose: web_app, saas, mobile_ios, mobile_android
status: draft               # choose: draft | in_review | approved | superseded
owner: ""                   # one person, by name
last_updated: ""            # YYYY-MM-DD
lifecycle_phase: planning   # choose: planning | development | pre_launch | launch | post_launch
launch_goal: "First 500 customers using the product"
---

# How to Fill This Document

**Read this first. It takes 3 minutes.**

## What this document is
This is the one place that says **how we will prove the product works** before real customers use it, and while the first 500 customers use it. People and AI agents both read it. If something is not written here, an agent must **ask a human**, not guess.

## How to fill it, step by step
1. **Fill the top block** (between the `---` lines). Keep the format; agents read it.
2. **Go in order, Part 0 to Part 10.** Each Part is a list of questions.
3. **Write your answer on the line that says `ANSWER:`.** Plain words are fine. Short is good.
4. **Tick boxes** by changing `[ ]` to `[x]`.
5. **Not relevant to your product?** Write `N/A: <one-line reason>`. Never leave a question empty. An empty answer means "not decided yet".
6. **Don't know yet?** Write `TBD: <who will decide>, <by what date>`. Anything still `TBD` blocks the gate that depends on it.
7. **Look for the signs:**
   - 👤 **WHO fills this:** `Founder`, `Dev` (developer / tech lead), `QA`, or `Sec` (security or legal reviewer).
   - 🔒 **HUMAN GATE:** a stop sign. Nobody (human or AI) moves on until the named people sign.
   - 🤖 **AGENT RULE:** what an AI agent must or must not do.
   - 💡 **Example:** shows what a good answer looks like. Delete examples when you are done if you like.
8. **Finish with Part 10**, the completeness check. If any box there is unticked, the document is not ready.

## Golden rules
- **Be specific.** "Fast" is not an answer. "Pages load in under 2 seconds on a phone" is.
- **Use numbers and yes/no** wherever you can.
- **One question, one answer.** If you need two answers, write two lines.
- **If you change an answer later,** add a line to the Change Log at the bottom.

## Words you will see
Tests are small checks that tell us "works" or "broken". Full explanations are in the Glossary at the bottom, so you never need to look anything up elsewhere.

---

# Part 0. Project Snapshot  👤 Founder

**0.1 In one or two sentences, what does the product do, and for whom?**
💡 *"PlantPal reminds home gardeners when to water each plant."*
ANSWER:

**0.2 What are the 3 to 7 most important things a customer must be able to do? (These are your "must-work" journeys.)**
💡 *1. Sign up. 2. Add a plant. 3. Get a reminder. 4. Pay for the premium plan.*
ANSWER:
1.
2.
3.

**0.3 Where does the product run? (tick all)**
- [ ] Website in a browser
- [ ] iPhone / iPad app
- [ ] Android app
- [ ] Backend / API only
- [ ] Other: ____

**0.4 What does the product handle? (tick all that apply; each tick adds required checks later)**
- [ ] Customer logins / passwords → Part 4A
- [ ] Personal data (name, email, location, health) → Part 4A
- [ ] Payments or subscriptions → Part 4B
- [ ] AI-generated content or AI features → Part 4E
- [ ] Children's data (under 13 or 16) → Part 4A, and ask Sec
- [ ] Data from the EU / UK / California → Part 4A, and ask Sec

**0.5 Key dates**
| Milestone | Target date (YYYY-MM-DD) |
|---|---|
| Testing plan approved | |
| Feature complete | |
| Private beta starts | |
| Public launch (first customers) | |
| 500th customer reached (goal) | |

**0.6 Who is on the team? (one name per role; roles can be shared by one person)**
| Role | Name | How to reach them |
|---|---|---|
| Product owner / Founder | | |
| Developer / Tech lead | | |
| QA lead | | |
| Security / legal reviewer | | |
| On-call person at launch | | |

---

# Part 1. Rules for AI Agents  🤖 👤 Dev

> AI agents (coding assistants, test-writing bots) **must read this Part before doing anything**. Humans: confirm these rules by ticking the boxes.

## 1.1 Source of truth
- Agents treat **this file as the source of truth** for what "tested" means.
- If this file and an agent's idea disagree, **this file wins**.
- If an answer is empty, `TBD`, or unclear: **stop and ask a human.** Do not invent an answer.

## 1.2 What agents MAY do without asking
- [ ] Write new tests for features listed in Part 2
- [ ] Run tests in the **test** and **staging** environments (Part 2.6)
- [ ] Fix a failing test **only if the product code is wrong**, and report what changed
- [ ] Open bug reports in the format of Part 7.3
- [ ] Write results in the format of Part 8

## 1.3 What agents MUST NEVER do
- [ ] Never delete, disable, skip, or weaken a test just to make it pass
- [ ] Never touch **production** data or production settings
- [ ] Never use real customer data in tests (use fake data from Part 2.7)
- [ ] Never type real passwords, card numbers, or secret keys into tests or files
- [ ] Never move past a 🔒 HUMAN GATE without a recorded human "yes"
- [ ] Never mark a test "passed" that was not actually run
- [ ] Never change this file's answers without a human approving (propose edits instead)

## 1.4 When an agent must stop and ask a human
- [ ] A **Critical** or **High** bug is found (Part 7)
- [ ] A test fails twice after a fix attempt
- [ ] A requirement is unclear or contradicts another
- [ ] The agent needs access to something not listed here
- [ ] Any security, privacy, or payment doubt

**1.5 Which AI tools/agents are used on this project?**
ANSWER:

**1.6 Where do agents write their results?** (path or tool)
💡 *`/qa/reports/` folder and the #qa-reports channel*
ANSWER:

---

# Part 2. Planning & Requirements  👤 Founder + QA

## 2.1 Scope: what are we testing?
**In scope (we WILL test):**
ANSWER:

**Out of scope (we will NOT test, and why):**
ANSWER:

## 2.2 Features and "done" rules (acceptance criteria)

For each must-work journey from 0.2, write what "working" means. Use this sentence shape:

> **Given** (starting situation) **When** (customer does something) **Then** (what must happen)

💡 *Given I am a new visitor, When I enter a valid email and password and press Sign up, Then I see my dashboard within 3 seconds and receive a welcome email within 1 minute.*

| ID | Journey / Feature | Given | When | Then (must happen) | Priority (Must / Should / Could) |
|---|---|---|---|---|---|
| F-01 | | | | | Must |
| F-02 | | | | | Must |
| F-03 | | | | | Must |

🤖 **AGENT RULE:** every test an agent writes must name the ID it checks (for example `F-01`). No ID, no test.

## 2.3 What could go wrong? (risk list)

List the scariest things. Rate each: **Chance** (Low / Med / High) and **Damage** (Low / Med / High). Test High/High first.

| ID | What could go wrong | Chance | Damage | How we will check it (Part #) |
|---|---|---|---|---|
| R-01 | 💡 Customer charged twice | Med | High | Part 4B |
| R-02 | | | | |
| R-03 | | | | |

## 2.4 Test strategy: how much of each kind of testing?

| Kind of test | What it checks (plain words) | Done by | Used for this product? (Y/N) | Target |
|---|---|---|---|---|
| **Unit** | One tiny piece of code works alone | Agent + Dev | | 💡 70% of code lines covered |
| **Integration** | Pieces work together (app ↔ database ↔ email) | Agent + Dev | | 💡 Every API endpoint has ≥1 test |
| **End-to-end (E2E)** | A whole journey, like a real customer | Agent + QA | | 💡 All "Must" journeys |
| **Manual / exploratory** | A human clicks around and tries to break it | QA | | 💡 2 hours per release |
| **Regression** | Old features still work after changes | Agent (automatic) | | 100% of earlier-fixed bugs |
| **Security** | Hackers cannot get in or steal data | Sec + Agent | | Part 4A |
| **Performance / load** | Fast enough, even when busy | Dev + Agent | | Part 4D |
| **Accessibility** | Usable by people with disabilities | QA + Agent | | Part 4C |
| **Usability / user acceptance (UAT)** | Real people can use it without help | Founder + beta users | | Part 5.4 |
| **AI quality checks (evals)** | AI answers are correct, safe, and consistent | Dev + QA | | Part 4E |

## 2.5 Entry and exit rules for each phase

| Phase | We may START when… | We may FINISH when… |
|---|---|---|
| Development testing | Acceptance criteria (2.2) are approved | All Part 3 targets are met |
| Pre-launch testing | Feature complete; Part 3 gate signed | Part 5 go/no-go gate signed |
| Launch testing | Part 5 gate signed | 500 customers reached AND Part 6.9 met |

## 2.6 Environments (the places the product runs)

| Environment | What it is for | Real customer data? | Who may change it | Web address / app build |
|---|---|---|---|---|
| **Local** | Developer's own computer | Never | Dev, agents | n/a |
| **Test** | Automatic tests run here | Never | Agents, Dev | |
| **Staging** | A copy of the real product for final checks | Never (fake only) | Dev | |
| **Production** | What real customers use | Yes | Humans only | |

🤖 **AGENT RULE:** agents may only act in Local, Test, and Staging.

## 2.7 Test data (fake people and fake money)
**Where does fake test data come from, and how is it reset?**
ANSWER:

**Test accounts (never write real passwords here; point to where they are stored securely):**
| Account type | Email (fake) | Where the password is stored |
|---|---|---|
| New customer | | |
| Paying customer | | |
| Admin | | |

**Test payment cards** (use only the official test cards from your payment provider's documentation):
ANSWER:

## 2.8 Tools (tool-neutral: write the one you actually use)

| Job | Popular examples | Our choice |
|---|---|---|
| Unit tests | Jest, Vitest, pytest, JUnit, XCTest | |
| Browser E2E tests | Playwright, Cypress, Selenium | |
| Mobile E2E tests | Appium, Detox, Maestro, XCUITest, Espresso | |
| API tests | Postman, REST-assured, Supertest | |
| Automatic checks on every change (CI) | GitHub Actions, GitLab CI, CircleCI | |
| Performance tests | k6, JMeter, Locust | |
| Security scans | OWASP ZAP, Snyk, Dependabot, SonarQube | |
| Accessibility checks | axe, Lighthouse, WAVE | |
| Bug tracker | GitHub Issues, Jira, Linear | |
| Error monitoring | Sentry, Datadog, Crashlytics | |
| Analytics | PostHog, Mixpanel, Amplitude, GA4 | |

---

# Part 3. Development & Automatic Checks (CI)  👤 Dev

## 3.1 What must pass automatically before any code is accepted?
- [ ] The code builds with no errors
- [ ] All unit tests pass
- [ ] All integration tests pass
- [ ] Code style / lint check passes
- [ ] Security scan finds no Critical or High issues
- [ ] Test coverage stays at or above the target in 2.4
- [ ] A human reviewed the change (not only the AI that wrote it)

**3.2 Which of the above are missing or different for this project, and why?**
ANSWER:

**3.3 Our "Definition of Done" for any feature (all must be true):**
- [ ] Acceptance criteria (2.2) are met
- [ ] Tests exist, are named after the feature ID, and pass
- [ ] No open Critical or High bugs on this feature
- [ ] Works on the devices/browsers in Part 5.2
- [ ] Error messages are clear and written for customers
- [ ] Logging/monitoring added for failures
- [ ] Documentation updated

**3.4 How fast must the automatic checks finish?** (so people don't skip them)
💡 *Under 10 minutes.*
ANSWER:

**3.5 How are flaky tests handled?** (tests that sometimes fail for no reason)
💡 *Retry once; if it fails again, a human looks; it is fixed within 3 days; it is never silently skipped.*
ANSWER:

🔒 **HUMAN GATE 1: Ready for Pre-Launch Testing**
Allowed to continue only if 3.1 and 3.3 are met for every "Must" feature (2.2) and no Critical/High bugs are open.
Sign-off is recorded in Part 9.

---

# Part 4. Risk Areas (fill in only what Part 0.4 turned on)

## 4A. Security & Privacy  👤 Sec + Dev

*Skip with `N/A` only if 0.4 has no logins, no personal data, and no payments.*

| # | Question | Answer (Y / N / N/A + note) |
|---|---|---|
| 1 | Are passwords stored scrambled (hashed), never as plain text? | |
| 2 | Is all traffic encrypted (HTTPS)? | |
| 3 | Is there a limit on wrong-password attempts? | |
| 4 | Can a customer see only their own data (try it with two test accounts)? | |
| 5 | Are secret keys kept out of the code and out of this file? | |
| 6 | Is the code checked for known weak spots (OWASP Top 10 list)? | |
| 7 | Are third-party libraries scanned for known problems? | |
| 8 | Can a customer download or delete their data on request? | |
| 9 | Is there a privacy policy and cookie notice, and do tests check they appear? | |
| 10 | Is there a written plan for a data leak (who is told, how fast)? | |
| 11 | Mobile only: is stored data on the phone encrypted, and are app permissions minimal? | |

**Laws and rules that apply (tick, and ask Sec if unsure):**
- [ ] GDPR (EU/UK)  - [ ] CCPA/CPRA (California)  - [ ] COPPA (children, US)  - [ ] HIPAA (health, US)  - [ ] Other: ____

**Who performed the security review, and on what date?**
ANSWER:

## 4B. Payments & Billing  👤 Dev + Sec

*Skip with `N/A` only if the product takes no money.*

| # | Question | Answer |
|---|---|---|
| 1 | Which payment provider do we use? (We never store card numbers ourselves.) | |
| 2 | Successful payment: does the customer get access and a receipt? | |
| 3 | Declined card: is the message clear, and no access given? | |
| 4 | Double-click or page refresh: is the customer charged only once? | |
| 5 | Refunds and cancellations: tested end to end? | |
| 6 | Free trial → paid and renewal: tested with test clocks/dates? | |
| 7 | Failed renewal: what happens, and is the customer emailed? | |
| 8 | Tax, currency, and invoices: correct for every country we sell in? | |
| 9 | App stores only: do in-app purchases pass Apple/Google review rules? | |
| 10 | Do we compare our records to the payment provider's records daily? | |

## 4C. Accessibility  👤 QA

**Target standard:** WCAG 2.2 Level AA (the common international rule). Change only with Founder approval.
ANSWER (target):

| # | Check | Result (Pass / Fail / N/A) |
|---|---|---|
| 1 | Everything can be used with the keyboard only | |
| 2 | Screen reader (VoiceOver, TalkBack, NVDA) reads pages in a sensible order | |
| 3 | Pictures have text descriptions | |
| 4 | Text and background colours have enough contrast | |
| 5 | Text can be enlarged to 200% without breaking | |
| 6 | Form fields have labels; errors say what to fix | |
| 7 | Videos have captions | |
| 8 | Touch targets are big enough on phones | |

## 4D. Performance & Scale  👤 Dev

| # | Question | Target | Result |
|---|---|---|---|
| 1 | Main page/screen load time (normal phone, normal internet) | 💡 under 2 s | |
| 2 | Server answer time for key actions | 💡 under 500 ms (95% of the time) | |
| 3 | How many customers using it at the same moment must it handle? | 💡 3× expected peak at 500 customers | |
| 4 | What happens when it is overloaded? (slows down vs crashes) | 💡 slows, never loses data | |
| 5 | Mobile only: app start time, battery use, and size | | |
| 6 | Mobile only: does it work on slow or lost connection? | | |
| 7 | Can the database and servers grow past 500 customers without a rewrite? | | |

## 4E. AI Features (only if 0.4 says the product uses AI)  👤 Dev + QA

| # | Question | Answer |
|---|---|---|
| 1 | What does the AI do for the customer? | |
| 2 | What is a "good answer"? Write 20+ example questions with the correct or acceptable answer (the "eval set"). Where is it stored? | |
| 3 | What score counts as passing? | 💡 90% of eval answers acceptable |
| 4 | What must the AI never say or do? (unsafe, private, off-topic, false claims) | |
| 5 | Have we tried to trick it (prompt-injection and misuse tests)? | |
| 6 | What does the customer see when the AI is wrong, slow, or down? | |
| 7 | Are results re-checked whenever the AI model or prompt changes? | |
| 8 | Is a human able to review AI output samples after launch? How often? | |

---

# Part 5. Pre-Launch & Beta Testing  👤 QA + Founder

## 5.1 Full-journey tests (E2E)
List every "Must" journey and its result in the final build.

| Journey (from 0.2) | Environment | Tester (human or agent) | Date | Result (Pass / Fail) | Bug ID if failed |
|---|---|---|---|---|---|
| | Staging | | | | |
| | Staging | | | | |

## 5.2 Which devices and browsers must work?

**Web:**
| Browser | Versions | Required? |
|---|---|---|
| Chrome (desktop, Android) | latest 2 | Yes |
| Safari (Mac, iPhone) | latest 2 | Yes |
| Firefox | latest 2 | |
| Edge | latest 2 | |

**Mobile (list real devices you will test on):**
| Device | OS version | Tested on real device? | Result |
|---|---|---|---|
| | | | |

**Screen sizes (tick):** - [ ] Small phone  - [ ] Large phone  - [ ] Tablet  - [ ] Laptop  - [ ] Big monitor

## 5.3 Install, update, and recovery
- [ ] A new customer can install or open the product from scratch
- [ ] An existing customer can update without losing data
- [ ] Customers can recover a lost password
- [ ] Customers can delete their account
- [ ] We have **practised** restoring from a backup (date: ____)
- [ ] Mobile only: store listing, screenshots, and age rating are ready

## 5.4 Beta and user acceptance (real people, real tasks)
**How many beta testers, and who are they?**
ANSWER:

**Tasks you will ask beta testers to do (no hints):**
ANSWER:

**What counts as "beta passed"?**
💡 *80% finish the main journey without help; average satisfaction ≥ 4 of 5; no new Critical bugs for 7 days.*
ANSWER:

## 5.5 Pre-launch quality scoreboard (fill in just before the gate)

| Measure | Target | Actual |
|---|---|---|
| "Must" feature tests passing | 100% | |
| All automated tests passing | ≥ 98% | |
| Open Critical bugs | 0 | |
| Open High bugs | 0 | |
| Open Medium bugs | ≤ 💡 10, each with a plan | |
| Security scan: Critical/High findings | 0 | |
| Accessibility: Fail items | 0 for "Must" journeys | |
| Performance targets (4D) | all met | |

🔒 **HUMAN GATE 2: Go / No-Go for Launch**
Launch is allowed only if every row above is met (or has a written exception signed below) and Parts 4A to 4E are complete. Record Go / No-Go and reasons in Part 9.

---

# Part 6. Launch to the First 500 Customers  👤 Founder + Dev + QA

## 6.1 Rollout stages
We grow in steps. Each step has a "stop sign" and a "green light".

| Stage | Customers | How they get in | Hold at this stage for | Green light to go on (all true) |
|---|---|---|---|---|
| 0 | Team only | Invite | 💡 2 days | No Critical/High bugs |
| 1 | up to 10 | Invite | 💡 3 days | Error rate under target (6.2); main journey works |
| 2 | up to 50 | Invite / waitlist | 💡 5 days | Feedback reviewed; top 3 issues fixed |
| 3 | up to 100 | Waitlist | 💡 5 days | Support load is manageable |
| 4 | up to 250 | Open sign-up with cap | 💡 7 days | Retention target met (6.2) |
| 5 | up to 500 | Open sign-up | until goal met | Part 6.9 met |

*Edit numbers and days to fit your product.*

## 6.2 Numbers we watch (the "dashboard")
Fill in a target and a "stop and fix" line for each. Check **daily** during Stages 1 to 3, then **twice a week**.

| Measure | How we count it | Healthy target | 🛑 Stop-and-fix line |
|---|---|---|---|
| Crash-free sessions (mobile) / error-free page views (web) | Error monitoring tool | 💡 ≥ 99.5% | 💡 below 98% |
| Errors per 1,000 actions | Error monitoring tool | 💡 under 5 | 💡 over 20 |
| New Critical bugs reported | Bug tracker | 0 | 1 or more |
| Open High bugs | Bug tracker | ≤ 💡 3 | 💡 over 5 |
| Page / app speed (4D #1) | Monitoring | within target | 💡 50% slower than target |
| Sign-up completion rate | Analytics (signed up ÷ started) | 💡 ≥ 60% | 💡 under 30% |
| Activation: finished first key task | Analytics | 💡 ≥ 50% | 💡 under 25% |
| Day-7 retention: came back after a week | Analytics | 💡 ≥ 30% | 💡 under 15% |
| Customer satisfaction (survey 1 to 5) | In-app survey | 💡 ≥ 4.0 | 💡 under 3.5 |
| Support tickets per 100 customers | Support tool | 💡 under 15 | 💡 over 40 |
| Payment failures (if paid) | Payment provider | 💡 under 3% | 💡 over 8% |

## 6.3 Monitoring and alerts
- [ ] Errors alert a human within 5 minutes (who? ____ )
- [ ] "Site down" check runs every minute
- [ ] Payment failures raise an alert
- [ ] A dashboard link is shared with the team: ____
- [ ] Someone is named on-call for the first 14 days after launch (see 0.6)

## 6.4 How we hear from customers
- [ ] In-app feedback button   - [ ] Email address: ____   - [ ] Survey after first task
- [ ] Short interviews with ____ customers per stage   - [ ] App store reviews checked daily

**Who reads feedback, how often, and where is it summarised?**
ANSWER:

## 6.5 Bug triage during launch
- Every report is read within **💡 4 hours** on weekdays.
- Each gets a severity from Part 7.1 and an owner.
- Critical bugs trigger the stop-and-fix rule (6.6).
ANSWER (changes to the above):

## 6.6 Stop, roll back, or keep going?

| If this happens | Do this | Who decides |
|---|---|---|
| A Critical bug (data loss, security hole, wrong payments, product unusable) | **Pause new sign-ups immediately.** Fix or roll back. | Dev + Founder |
| Any measure at its 🛑 line (6.2) | Pause at the current stage; find the cause | Dev + QA |
| New release makes things worse | **Roll back** to last good version | Dev |
| Suspected data leak | Follow the plan in 4A #10 | Sec + Founder |

**How exactly do we roll back, and how long does it take?** (Practised before launch: Y / N)
ANSWER:

## 6.7 Releasing fixes during launch
- [ ] Every fix has a new test proving it
- [ ] The full automatic test run (Part 3.1) passes first
- [ ] Release time avoids Fridays and late evenings
- [ ] Customers are told about important changes: how? ____

🤖 **AGENT RULE:** an agent may prepare a fix and its test, but a human approves every release to production.

## 6.8 Learning loop (after each stage)
Write what we learned and which tests we will add so it never happens again.

| Stage | What went wrong or surprised us | New test or check added | Done? |
|---|---|---|---|
| | | | |

🔒 **HUMAN GATE 3: Move to the Next Stage** (repeat for stages 1 to 5)
Allowed only if the green-light column (6.1) is true and no 🛑 line in 6.2 is crossed. Record in Part 9.

## 6.9 What does "first 500 customers: success" mean?
**All must be true:**
- [ ] 500 customers have signed up and used the product at least once
- [ ] No open Critical bugs; High bugs ≤ ____
- [ ] Every 6.2 measure is at or better than target for 14 days in a row
- [ ] The learning loop (6.8) is complete for every stage
- [ ] The Testing.md for the next phase (growth) is started

🔒 **HUMAN GATE 4: Launch Phase Closed.** Recorded in Part 9.

---

# Part 7. Bugs  👤 QA + Dev

## 7.1 How serious is a bug?

| Severity | Plain-English meaning | Examples | Fix within | Can we launch / grow with it open? |
|---|---|---|---|---|
| **Critical** | Customers lose data or money, security is broken, or the product cannot be used | Data leak; charged twice; app crashes at start | Immediately (💡 24 h) | **No** |
| **High** | A main journey is broken or badly hurt, but a workaround exists | Cannot reset password; reminder not sent | 💡 3 days | **No** |
| **Medium** | A normal feature is wrong, but customers can still do their job | Wrong date format; slow screen | 💡 2 weeks | Yes, with a plan |
| **Low** | Small, cosmetic, or rare | Typo; misaligned icon | Backlog | Yes |

**7.2 Changes to this table for this project:**
ANSWER:

## 7.3 How to report a bug (humans and agents use the same format)

```
ID:            BUG-###
Title:         (short, specific)
Severity:      Critical | High | Medium | Low
Related ID:    (feature F-## or risk R-##)
Environment:   (Local | Test | Staging | Production) + version/build
Device/Browser:
Steps to reproduce:
  1.
  2.
Expected result:
Actual result:
Proof:         (screenshot, video, log link)
Reported by:   (name or agent) on (YYYY-MM-DD)
Owner:
Status:        Open | In progress | Fixed | Verified | Won't fix (reason)
```

🤖 **AGENT RULE:** never close a bug yourself. A human verifies and sets "Verified".

---

# Part 8. Reporting Test Results  🤖 👤 QA

## 8.1 Standard report (every run, same shape)

```
Run ID:         RUN-YYYYMMDD-##
Date and time:
Environment:    Test | Staging
Build/version:
Run by:         (human or agent name)
What was tested: (feature IDs / Parts)
Total tests:    N
Passed:         N
Failed:         N   (list test names + BUG IDs)
Skipped:        N   (list each, with human-approved reason)
Coverage:       N%
New bugs:       (BUG IDs)
Anything unclear that needs a human: (list)
Recommendation: Continue | Stop and ask a human
```

**8.2 How often are reports produced, and who reads them?**
ANSWER:

---

# Part 9. Sign-offs and Decisions (the gate log)  🔒

A gate is passed only when **every required name** has signed. Type the name and date; do not edit past rows.

| Gate | Required sign-offs | Product owner / Founder | Dev / Tech lead | QA lead | Security / legal | Result (Go / No-Go) | Date | Notes / exceptions |
|---|---|---|---|---|---|---|---|---|
| Testing plan approved | Founder, Dev, QA | | | | n/a | | | |
| Gate 1: Ready for pre-launch testing | Founder, Dev, QA | | | | n/a | | | |
| Gate 2: Go / No-Go for launch | All four | | | | | | | |
| Gate 3, Stage 1 → 2 | Founder, Dev, QA | | | | n/a | | | |
| Gate 3, Stage 2 → 3 | Founder, Dev, QA | | | | n/a | | | |
| Gate 3, Stage 3 → 4 | Founder, Dev, QA | | | | n/a | | | |
| Gate 3, Stage 4 → 5 | Founder, Dev, QA, Sec | | | | | | | |
| Gate 4: Launch phase closed | All four | | | | | | | |

**Exceptions:** if we launch or continue with a rule not met, write what, why, who accepted the risk, and when it will be fixed.
| Date | Rule not met | Why we accept the risk | Accepted by | Fix by |
|---|---|---|---|---|
| | | | | |

---

# Part 10. Final Completeness Check  👤 QA + Founder

Tick when true. **If any box is unticked, this document is not ready.**

- [ ] The top block (YAML) is filled in
- [ ] Every question has an answer, `N/A: reason`, or `TBD: who, by when`
- [ ] No `TBD` remains on anything required for the current gate
- [ ] Every "Must" journey has an ID and a "Given / When / Then" (2.2)
- [ ] Every High/High risk has a test plan (2.3)
- [ ] Environments, test data, and tools are named (2.6 to 2.8)
- [ ] Part 4 sections that apply are complete
- [ ] Rollout stages, numbers to watch, and stop lines have real numbers (6.1, 6.2)
- [ ] Rollback was practised at least once (6.6)
- [ ] Someone who did **not** write this document read it and could answer: "What do we test? Who decides? When do we stop?"
- [ ] AI-agent rules (Part 1) are confirmed by a human

---

# Glossary (plain words)

| Word | Meaning |
|---|---|
| **Acceptance criteria** | The exact "done" rules for a feature, written so anyone can check them |
| **Agent (AI agent)** | A computer program driven by AI that can write code, run tests, and report results |
| **API** | The doorway apps use to talk to a server |
| **Backup** | A saved copy of data, used to recover after a problem |
| **Beta** | A trial run with a small group of real people before everyone |
| **Build** | One packaged version of the product |
| **CI (continuous integration)** | Automatic checks that run every time someone changes the code |
| **Coverage** | The share of the code that tests actually run |
| **Critical bug** | A bug that loses data or money, breaks security, or makes the product unusable |
| **E2E (end to end)** | A test that follows a whole customer journey from start to finish |
| **Eval set (AI)** | A fixed list of questions and good answers used to grade an AI feature |
| **Flaky test** | A test that sometimes passes and sometimes fails for no real reason |
| **Gate** | A stop sign where named people must say yes before moving on |
| **Hash (password)** | Scrambling a password so even we cannot read it |
| **Integration test** | A test that checks that several parts work together |
| **Production** | The live product that real customers use |
| **Regression** | An old feature that breaks after a new change |
| **Retention** | How many customers come back after some days |
| **Rollback** | Going back to the last version that worked |
| **Staging** | A practice copy of production used for final checks |
| **UAT (user acceptance testing)** | Real users confirm the product does what they need |
| **Unit test** | A test that checks one tiny piece of code |
| **WCAG** | The international rules for making products usable by people with disabilities |

---

# Change Log

| Date | Part changed | What changed and why | Changed by | Approved by |
|---|---|---|---|---|
| | | Created from the Testing.md template v1.0.0 | | |
