# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What is this?** A plan that proves your product works for real people, from the first line of code until your first 500 customers are happily using it. "End to end" means we test the *whole journey* a customer takes (find it, sign up, pay, use it, get help, leave), not just small pieces.

**Who can fill it?** Anyone. If you can answer simple questions, you can fill this in. You do not need to know testing words. Every hard word is explained in the Glossary (Appendix B).

## The 6 rules

1. **Go in order.** Start at Section 1 and move down. Later sections use your earlier answers.
2. **Every section has the same 3 parts:**
   - 💬 **Question**: what we want to know.
   - 💡 **Example**: a sample answer so you can see what "good" looks like. *Never leave the example in your final answer. Replace it.*
   - ✍️ **Your answer**: the place where you write. Replace every `[FILL IN]`.
3. **Never guess.** If you do not know, write `UNKNOWN - ask [name] by [date]`. A visible "unknown" is better than a hidden guess.
4. **Not relevant? Write `N/A - because [reason]`.** Never delete a section. (Example: no payments yet → `N/A - free product until Month 3`.)
5. **Be specific.** Numbers beat feelings. Write "page loads in under 3 seconds," not "page loads fast."
6. **Tick the status box** at the top of each section when done: `☐ Not started` → `◐ In progress` → `☑ Done`. When all boxes are `☑`, go to the Final Self-Check (Section 34).

## Time needed

| If you are… | Do this | Time |
|---|---|---|
| In a hurry | Fill only sections marked ⭐ (the must-haves) | about 2 hours |
| Doing it properly | Fill every section | about 1 to 2 days |
| Using an AI agent | Let the agent draft with the prompts in Appendix A, then a human checks every answer | about 1 hour + review |

## Naming and saving

- Save this file as `End_to_End_Testing_Plan.md` inside the folder `Testing and quality assurance/`.
- Copy this blank template for each new project. Never edit the master copy.
- Version your copy (Section 1) every time you change something important.

## Legend

| Symbol | Meaning |
|---|---|
| ⭐ | Must-have. Do not skip. |
| 🤖 | An AI agent may do the work, but a human must approve. |
| 🧑 | A human must do or decide this. Agents must not. |
| 🚦 | A go/no-go gate. Nobody moves forward without a "yes." |
| ☐ / ◐ / ☑ | Not started / In progress / Done |

---

# END-TO-END TESTING PLAN

**Project name:** `[FILL IN]`
**Plan version:** `[FILL IN, e.g. 0.1]`
**Date created:** `[FILL IN, YYYY-MM-DD]`

---

## Table of Contents

1. Document Control ⭐
2. Product in One Page ⭐
3. Goals and "What Does Success Look Like?" ⭐
4. Scope: What We Test and What We Do Not ⭐
5. Customers and Their Journeys ⭐
6. The Big Picture: Stages from Build to 500 Customers ⭐
7. People and Responsibilities ⭐
8. AI Agent Rules and Guardrails ⭐ 🤖
9. Environments (Where We Test) ⭐
10. Test Data (What We Test With) ⭐
11. Tools and Accounts
12. Links Between Requirements and Tests (Traceability)
13. Test Levels: Small, Medium and Whole-Journey Tests ⭐
14. End-to-End Scenario Catalog ⭐
15. Sign-Up, Login and Account Tests ⭐
16. Payments and Billing Tests ⭐
17. Security and Privacy Tests ⭐
18. Performance and Load Tests ⭐
19. Accessibility Tests
20. Devices, Browsers and App Store Coverage ⭐
21. Data, Backup and Recovery Tests
22. Third-Party Services and Integrations
23. Entry and Exit Rules for Each Stage 🚦 ⭐
24. Bugs: How We Report, Rank and Fix Them ⭐
25. Test Schedule and Effort
26. Stage A: Build and Pre-Release Testing ⭐
27. Stage B: Launch Readiness (Go / No-Go) 🚦 ⭐
28. Stage C: Beta and First 50 Customers ⭐
29. Stage D: Growing to 500 Customers ⭐
30. Monitoring, Alerts and Rollback ⭐
31. Risks and Backup Plans ⭐
32. Reports and Numbers We Track
33. Approvals and Sign-Off 🧑 ⭐
34. Final Self-Check ⭐
35. Change Log

**Appendix A:** AI Agent Prompt Library 🤖
**Appendix B:** Glossary (Hard Words Made Easy)
**Appendix C:** Ready-to-Copy Checklists
**Appendix D:** References and Standards Behind This Template

---

## 1. Document Control ⭐

**Status:** ☐ Not started

> 💬 **Question:** Who owns this plan, who may change it, and what version is this?

| Field | 💡 Example | ✍️ Your answer |
|---|---|---|
| Project name | Acme Notes | `[FILL IN]` |
| Plan owner (one person) | Priya Shah, Product Manager | `[FILL IN]` |
| Reviewers | Dev lead, QA lead, Security lead | `[FILL IN]` |
| Approver (final "yes") | CTO | `[FILL IN]` |
| Version | 1.0 | `[FILL IN]` |
| Last updated | 2026-10-17 | `[FILL IN]` |
| Where is the code? | github.com/acme/notes | `[FILL IN]` |
| Where do bugs live? | Jira project "NOTES" | `[FILL IN]` |
| Where do test results live? | `/Testing and quality assurance/results/` | `[FILL IN]` |
| Next review date | Every 2 weeks, or after any big change | `[FILL IN]` |

---

## 2. Product in One Page ⭐

**Status:** ☐ Not started

> 💬 **Question 2.1:** In 2 sentences, what is your product and who is it for?
> 💡 *Example:* "Acme Notes is a note-taking app for students. It lets them write, search and share class notes on phone and web."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 2.2:** What is the ONE thing a customer must be able to do for the product to be worth anything?
> 💡 *Example:* "Create a note, close the app, reopen it, and find the note still there."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 2.3:** Which type of product is it? (Tick all that apply.)
> - ☐ Website / web app (SaaS)
> - ☐ iOS app
> - ☐ Android app
> - ☐ Has a public API
> - ☐ Has an admin panel for staff
> - ☐ Other: `[FILL IN]`

> 💬 **Question 2.4:** Does it take payments, store personal data, or serve children? (These raise the testing bar.)
> 💡 *Example:* "Takes card payments via Stripe. Stores email and name. Not for children under 13."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 2.5:** Which main features exist? List each in one line.
> 💡 *Example:* "F1 Sign-up, F2 Create note, F3 Search, F4 Share link, F5 Upgrade to Pro."

| ID | Feature | Must be ready for launch? (Yes / No) |
|---|---|---|
| F1 | `[FILL IN]` | `[FILL IN]` |
| F2 | `[FILL IN]` | `[FILL IN]` |
| F3 | `[FILL IN]` | `[FILL IN]` |
| F4 | `[FILL IN]` | `[FILL IN]` |

*(Add rows as needed.)*

> 💬 **Question 2.6:** What is the planned launch date and the date you hope to reach 500 customers?
> 💡 *Example:* "Public launch 2027-02-01. 500 customers by 2027-06-30."
> ✍️ **Your answer:** Launch: `[FILL IN]` | 500 customers: `[FILL IN]`

> 💬 **Question 2.7:** What counts as a "customer" for the number 500?
> 💡 *Example:* "A person who signed up AND completed at least one real action in the last 7 days. Not test accounts, not staff."
> ✍️ **Your answer:** `[FILL IN]`

---

## 3. Goals and "What Does Success Look Like?" ⭐

**Status:** ☐ Not started

> 💬 **Question 3.1:** Why are we testing? Pick the top 3 goals.
> - ☐ Customers can finish the main journey without help
> - ☐ No customer loses data or money
> - ☐ No security or privacy embarrassment
> - ☐ Product stays fast when customers join
> - ☐ We can find and fix problems quickly after launch
> - ☐ We meet legal rules (privacy, payments, accessibility)
> - ☐ Other: `[FILL IN]`

> 💬 **Question 3.2:** Write measurable pass/fail targets. Use numbers.
> 💡 *Example targets are in the table. Replace with yours.*

| What we measure | 💡 Example target | ✍️ Your target |
|---|---|---|
| Main journey success rate | 98% of test runs finish with no error | `[FILL IN]` |
| Page load time (typical) | Under 3 seconds on normal 4G | `[FILL IN]` |
| App crash-free sessions | 99.5% or higher | `[FILL IN]` |
| Open critical bugs at launch | 0 | `[FILL IN]` |
| Open high bugs at launch | 0 (or each has written approval) | `[FILL IN]` |
| Payment success in tests | 100% of test cards behave as expected | `[FILL IN]` |
| Support questions per 100 customers | Fewer than 10 per week | `[FILL IN]` |
| Time to fix a critical bug in production | Under 4 hours | `[FILL IN]` |

> 💬 **Question 3.3:** What would make us STOP the launch, no matter what?
> 💡 *Example:* "Any bug that loses customer data, charges a customer twice, or exposes one customer's data to another."
> ✍️ **Your answer:** `[FILL IN]`

---

## 4. Scope: What We Test and What We Do Not ⭐

**Status:** ☐ Not started

> 💬 **Question 4.1:** What is **in scope** (we WILL test)?
> 💡 *Example:* "Web app on latest Chrome, Safari, Firefox, Edge. iOS 17 and 18. Android 13 to 15. Sign-up, notes, search, sharing, billing, emails we send."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 4.2:** What is **out of scope** (we will NOT test), and why?
> 💡 *Example:* "Internet Explorer (no longer supported). Tablet layouts (planned for v2). Languages other than English (v2)."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 4.3:** What do we depend on that we do not control, and how will we handle it?
> 💡 *Example:* "Stripe for payments. We use Stripe test mode. We do not test Stripe itself."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 4.4:** What assumptions are we making? (Things we believe are true but have not checked.)
> 💡 *Example:* "Test environment mirrors production. Design is final by Week 4."
> ✍️ **Your answer:** `[FILL IN]`

---

## 5. Customers and Their Journeys ⭐

**Status:** ☐ Not started

> 💬 **Question 5.1:** Who are the different kinds of customers? Give each a name.
> 💡 *Example:* "Sam the Student (free user, phone). Dana the Teacher (paid, laptop). Alex the Admin (staff, admin panel)."

| Persona | Description | Device they use | Free or paid |
|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 5.2:** Write the full life of one customer in order, from first hearing about you to leaving. This becomes your test map.
> 💡 *Example:* "1) Sees ad. 2) Opens website. 3) Signs up. 4) Verifies email. 5) Creates first note. 6) Invites a friend. 7) Hits the free limit. 8) Pays. 9) Gets receipt email. 10) Contacts support. 11) Cancels. 12) Deletes account."

| Step | What the customer does | What should happen | Which feature (ID) |
|---|---|---|---|
| 1 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 2 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 3 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 4 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

*(Keep going until the journey ends.)*

> 💬 **Question 5.3:** Which 3 to 5 steps would hurt the most if they broke? These are your **critical journeys**. Test them first and most often.
> 💡 *Example:* "Sign-up, create note, pay, password reset, delete account."
> ✍️ **Your answer:** `[FILL IN]`

---

## 6. The Big Picture: Stages from Build to 500 Customers ⭐

**Status:** ☐ Not started

> 💬 **Question:** What are the four stages and their dates? (The stage names below are fixed so every project looks the same. Only change the dates and notes.)

| Stage | Plain meaning | Starts | Ends | Who says "go" 🚦 |
|---|---|---|---|---|
| **A. Build and Pre-Release** | We build and test before anyone outside sees it | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| **B. Launch Readiness** | Final check before the doors open | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| **C. Beta and First 50** | A small group tries it. We watch closely | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| **D. Growth to 500** | We grow in steps: 50 → 100 → 250 → 500 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

**Picture of the journey:**

```
 BUILD  ──▶  PRE-RELEASE  ──▶  GO/NO-GO  ──▶  BETA (1-50)  ──▶  100  ──▶  250  ──▶  500
  Unit      Integration       Launch         Watch closely    Check   Check   Done:
  tests     + End-to-End      checklist      fix fast         point   point   review
            + Security etc.
```

> 💬 **Question 6.1:** What AI-driven development steps happen in each stage? (Where do AI agents write code, write tests, run tests, or review?)
> 💡 *Example:* "Stage A: Agent writes code and unit tests from tickets; human reviews every pull request. Stage B: Agent runs full regression and drafts the go/no-go report; human decides. Stage C-D: Agent summarizes bugs and customer feedback daily; human decides fixes."
> ✍️ **Your answer:** `[FILL IN]`

---

## 7. People and Responsibilities ⭐

**Status:** ☐ Not started

> 💬 **Question 7.1:** Who does what? Every row needs ONE name responsible. (R = does the work, A = final say, C = asked for advice, I = told the result.)

| Job | 💡 Example name | R | A | C | I |
|---|---|---|---|---|---|
| Owns this plan | Priya | R | A | | |
| Writes test cases | QA lead + AI agent | R | | C | |
| Runs tests | AI agent + QA | R | | | |
| Approves test results | QA lead | | A | | I |
| Fixes bugs | Developers | R | | | |
| Security checks | Security lead | R | A | | |
| Go / no-go decision | CTO | | A | C | I |
| Talks to beta customers | Customer success | R | | | |
| On-call after launch | Rotating developer | R | | | |

✍️ **Your team:**

| Job | Name | Contact | Backup person |
|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 7.2:** If someone is away, who steps in? Is the plan still safe with only one person knowing something?
> ✍️ **Your answer:** `[FILL IN]`

---

## 8. AI Agent Rules and Guardrails ⭐ 🤖

**Status:** ☐ Not started

**Core rule of this template: AI agents run tests. Humans approve.** An agent can write, run and summarize. A human must sign off at every 🚦 gate.

> 💬 **Question 8.1:** Which AI agents or tools are used, and for what?
> 💡 *Example:* "Claude: writes test cases and test scripts. Playwright agent: runs web tests. Appium agent: runs mobile tests. Triage agent: sorts bugs."

| Agent / tool | Job | Allowed to change code? | Allowed to touch production? |
|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 8.2:** Confirm each safety rule. Change a rule only with a written reason.

| # | Rule | Default | Agree? (Yes / Changed to…) |
|---|---|---|---|
| 1 | Agents test in test environments only. **Never** in production with real customer data, unless Section 30 says so | Yes | `[FILL IN]` |
| 2 | Agents never use real customer data or real payment cards | Yes | `[FILL IN]` |
| 3 | Agents never delete data, send real emails or charge real money | Yes | `[FILL IN]` |
| 4 | Every agent test result must include **evidence** (screenshot, log, or recording). "It passed" with no proof does not count | Yes | `[FILL IN]` |
| 5 | A human reads every failed test and every "skipped" test | Yes | `[FILL IN]` |
| 6 | Agents must say "I do not know" instead of guessing | Yes | `[FILL IN]` |
| 7 | Agents never mark a gate as passed. Only a human signs | Yes | `[FILL IN]` |
| 8 | Secrets (passwords, keys) are never pasted into prompts or saved in this document | Yes | `[FILL IN]` |
| 9 | Agent-written tests are reviewed by a human before they become official | Yes | `[FILL IN]` |
| 10 | Every agent run is logged (what it did, when, which version of the product) | Yes | `[FILL IN]` |

> 💬 **Question 8.3:** What does an agent do when it gets stuck, finds something odd, or sees a possible security problem?
> 💡 *Example:* "Stop. Write what happened. Tag the QA lead. Do not retry more than 3 times. Security issues go to the Security lead immediately, not to the public bug list."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 8.4:** How do we check that the agent itself is doing a good job? (Agents can be wrong.)
> 💡 *Example:* "Each week a human re-runs 10 random agent-passed tests by hand. If 1 or more is wrong, we review the agent's setup."
> ✍️ **Your answer:** `[FILL IN]`

---

## 9. Environments (Where We Test) ⭐

**Status:** ☐ Not started

> 💬 **Question 9.1:** List every place the product runs. Each has a purpose and a rule about real data.

| Environment | 💡 Example purpose | URL / location | Real customer data allowed? | Who can change it? | Reset how often? |
|---|---|---|---|---|---|
| Local (developer laptop) | Build and quick checks | localhost | No | Developers | Anytime |
| Test / QA | Full testing | `[FILL IN]` | No | `[FILL IN]` | `[FILL IN]` |
| Staging (copy of production) | Final rehearsal | `[FILL IN]` | No (fake copy only) | `[FILL IN]` | `[FILL IN]` |
| Production (live) | Real customers | `[FILL IN]` | Yes | `[FILL IN]` | Never |

> 💬 **Question 9.2:** How is staging different from production? List every difference. Each one is a risk.
> 💡 *Example:* "Staging uses a smaller database. Stripe is in test mode. Emails go to a mailbox catcher."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 9.3:** How do we put a new version into the test environment, and how do we know which version is there?
> 💡 *Example:* "Merge to main → automatic deploy to Test. Version shown in footer of the site and in Settings > About of the app."
> ✍️ **Your answer:** `[FILL IN]`

---

## 10. Test Data (What We Test With) ⭐

**Status:** ☐ Not started

> 💬 **Question 10.1:** What fake accounts and fake data do we need?
> 💡 *Example:* "10 free users, 5 paid users, 1 admin, 1 user with 10,000 notes, 1 user with no verified email."

| Data set | Purpose | How created | How reset |
|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 10.2:** Which test payment cards, phone numbers and emails do we use? (Use only the official test values from your payment provider. **Never write real card numbers or passwords here.**)
> ✍️ **Your answer (where they are stored, not the values):** `[FILL IN]`

> 💬 **Question 10.3:** If we copy real data to test, how do we remove names, emails and other personal details?
> 💡 *Example:* "We never copy real data. We generate fake data with a script."
> ✍️ **Your answer:** `[FILL IN]`

---

## 11. Tools and Accounts

**Status:** ☐ Not started

> 💬 **Question:** Which tools do we use? (Write the tool name, or `N/A`.)

| Need | 💡 Example | ✍️ Your tool | Who has access |
|---|---|---|---|
| Web browser automation | Playwright, Cypress | `[FILL IN]` | `[FILL IN]` |
| Mobile automation | Appium, Detox, Maestro | `[FILL IN]` | `[FILL IN]` |
| Real-device cloud | BrowserStack, Sauce Labs | `[FILL IN]` | `[FILL IN]` |
| API testing | Postman, REST Assured | `[FILL IN]` | `[FILL IN]` |
| Load testing | k6, JMeter, Locust | `[FILL IN]` | `[FILL IN]` |
| Security scanning | OWASP ZAP, Snyk | `[FILL IN]` | `[FILL IN]` |
| Accessibility checks | axe, Lighthouse, screen readers | `[FILL IN]` | `[FILL IN]` |
| Bug tracking | Jira, Linear, GitHub Issues | `[FILL IN]` | `[FILL IN]` |
| Automatic test runs (CI/CD) | GitHub Actions, GitLab CI | `[FILL IN]` | `[FILL IN]` |
| Error and crash monitoring | Sentry, Crashlytics | `[FILL IN]` | `[FILL IN]` |
| Product analytics | PostHog, Amplitude | `[FILL IN]` | `[FILL IN]` |
| Uptime monitoring | Better Stack, Pingdom | `[FILL IN]` | `[FILL IN]` |
| Customer feedback | Intercom, Typeform | `[FILL IN]` | `[FILL IN]` |
| Test case storage | This repo, TestRail, Xray | `[FILL IN]` | `[FILL IN]` |

---

## 12. Links Between Requirements and Tests (Traceability)

**Status:** ☐ Not started

> 💬 **Question:** For every feature, which tests prove it works? This stops anything being forgotten.
> 💡 *Example row:* "F1 Sign-up → E2E-001, E2E-002, SEC-004, A11Y-001 → Status: Passed."

| Feature ID | Requirement in plain words | Test IDs that cover it | Latest result | Gap? |
|---|---|---|---|---|
| F1 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| F2 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| F3 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

**Rule:** a feature with an empty "Test IDs" cell cannot go live.

---

## 13. Test Levels: Small, Medium and Whole-Journey Tests ⭐

**Status:** ☐ Not started

**Simple picture:** Test like building a house. Check each brick (unit), then walls fit together (integration), then live in the house for a weekend (end to end).

| Level | Plain meaning | How many (guide) | Who/what runs it | When |
|---|---|---|---|---|
| Unit | One small piece in isolation | Many (hundreds+) | Developers + AI agent, automatic | Every code change |
| Integration | Pieces talking to each other (app ↔ database ↔ payment) | Some | Automatic | Every merge |
| **End-to-end (E2E)** | A full customer journey in a real-like setup | Few but important | Automatic + manual | Every release |
| Exploratory | A human pokes around, tries odd things | Time-boxed sessions | Human | Before each stage gate |
| Acceptance (UAT) | The business owner confirms "this is what I wanted" | One per release | Human 🧑 | Before launch |

> 💬 **Question 13.1:** Set targets for your project.
> 💡 *Example:* "Unit: 80% of code covered. Integration: every API endpoint. E2E: all critical journeys, run on every release. Exploratory: 2 hours per release."

| Level | ✍️ Your target |
|---|---|
| Unit | `[FILL IN]` |
| Integration | `[FILL IN]` |
| E2E | `[FILL IN]` |
| Exploratory | `[FILL IN]` |
| Acceptance | `[FILL IN]` |

> 💬 **Question 13.2:** Which tests run automatically, and which stay manual? Why?
> 💡 *Example:* "Login, notes, billing: automatic. Look and feel on a new phone: manual."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 13.3:** What do we do about "flaky" tests (tests that sometimes pass and sometimes fail for no clear reason)?
> 💡 *Example:* "A test that flips 2 times in 20 runs is quarantined and fixed within 5 working days. Flaky tests never count as a pass."
> ✍️ **Your answer:** `[FILL IN]`

---

## 14. End-to-End Scenario Catalog ⭐

**Status:** ☐ Not started

> 💬 **Question:** List every whole-journey test. Start with the critical journeys from Section 5.3. Use one row per scenario. **Write steps so simple anyone could follow them.**

**How to write a scenario (💡 example):**

| Field | Example |
|---|---|
| ID | E2E-001 |
| Name | New customer signs up and creates first note |
| Priority | Critical / High / Medium / Low |
| Persona | Sam the Student |
| Device | Chrome on laptop; iPhone 15 |
| Before we start | Test email address not used before |
| Steps | 1) Open site. 2) Click "Sign up". 3) Enter email and password. 4) Click link in email. 5) Click "New note". 6) Type "Hello". 7) Click Save. |
| Expected result | Note appears in list. Reload page. Note is still there. |
| Evidence needed | Screenshot of list before and after reload |
| Automated? | Yes |
| Last run / result | 2026-10-17 / Pass |

**✍️ Your scenarios:**

| ID | Name | Priority | Persona | Device | Steps (short) | Expected result | Automated? | Last result |
|---|---|---|---|---|---|---|---|---|
| E2E-001 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| E2E-002 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| E2E-003 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

*(Add rows. Full step-by-step detail can live in your test tool. Link it here: `[FILL IN]`.)*

> 💬 **Question 14.2:** Have we covered the "unhappy paths"? (What happens when things go wrong?) Tick what you have tests for.
> - ☐ Wrong password
> - ☐ Internet drops halfway through a task
> - ☐ Customer double-clicks "Pay"
> - ☐ Customer uses the Back button in the middle of a flow
> - ☐ Very long text, special characters, emojis
> - ☐ Empty fields
> - ☐ Same account on two devices at once
> - ☐ Session expires while customer is working
> - ☐ Server is slow or down
> - ☐ Customer uploads wrong or huge file
> - ☐ Customer with no permission tries admin page
> - ☐ Email never arrives / link expired
> - ☐ Time zones and date changes
> - ☐ Low battery / low storage / low memory (mobile)
> - ☐ App in background, then reopened (mobile)
> - ☐ Notification permission denied (mobile)

---

## 15. Sign-Up, Login and Account Tests ⭐

**Status:** ☐ Not started

> 💬 **Question:** Which of these checks are done? Mark ✅ Pass, ❌ Fail, ➖ N/A.

| # | Check | Web | iOS | Android | Notes |
|---|---|---|---|---|---|
| 15.1 | Sign up with email works | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.2 | Sign up with Google / Apple / other (if offered) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.3 | Email verification link works and expires correctly | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.4 | Cannot sign up with weak password or invalid email | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.5 | Login and logout work | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.6 | "Forgot password" email arrives and link works once only | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.7 | Too many wrong passwords is blocked or slowed | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.8 | Change email / password works | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.9 | Two-step login (if offered) works | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.10 | Delete account removes the data it promised to | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.11 | One customer can never see another customer's data | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |
| 15.12 | Roles work (free, paid, admin) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | |

---

## 16. Payments and Billing Tests ⭐

**Status:** ☐ Not started

*If you take no payments: write `N/A - [reason]` and the date payments are planned.* `[FILL IN]`

> 💬 **Question 16.1:** Which payment provider(s) and plans do you have?
> 💡 *Example:* "Stripe. Free plan, Pro $9/month, Pro $90/year. 14-day trial."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 16.2:** Mark each check.

| # | Check | Result | Evidence link |
|---|---|---|---|
| 16.1 | Successful payment with a test card | `[FILL IN]` | `[FILL IN]` |
| 16.2 | Card declined shows a clear message and no access is granted | `[FILL IN]` | `[FILL IN]` |
| 16.3 | Card needing extra bank approval (3-D Secure) works | `[FILL IN]` | `[FILL IN]` |
| 16.4 | Double-click on "Pay" charges only once | `[FILL IN]` | `[FILL IN]` |
| 16.5 | Upgrade, downgrade and cancel work, with correct partial charges | `[FILL IN]` | `[FILL IN]` |
| 16.6 | Free trial ends and charges correctly (or does not, if cancelled) | `[FILL IN]` | `[FILL IN]` |
| 16.7 | Renewal charge works. Failed renewal triggers retry emails | `[FILL IN]` | `[FILL IN]` |
| 16.8 | Refund works and customer loses access as promised | `[FILL IN]` | `[FILL IN]` |
| 16.9 | Receipts and invoices arrive with right amount, tax and date | `[FILL IN]` | `[FILL IN]` |
| 16.10 | Tax / VAT and currency correct for each country sold in | `[FILL IN]` | `[FILL IN]` |
| 16.11 | Promo codes work, expire, and cannot be reused wrongly | `[FILL IN]` | `[FILL IN]` |
| 16.12 | Payment events (webhooks) arrive late, twice or out of order and the product copes | `[FILL IN]` | `[FILL IN]` |
| 16.13 | App Store / Google Play in-app purchase rules followed (mobile) | `[FILL IN]` | `[FILL IN]` |
| 16.14 | Our records match the payment provider's records (reconciliation) | `[FILL IN]` | `[FILL IN]` |

🧑 **A human must verify rows 16.4, 16.8 and 16.14.**

---

## 17. Security and Privacy Tests ⭐

**Status:** ☐ Not started

> 💬 **Question 17.1:** What sensitive data do we hold, and where is it stored?
> 💡 *Example:* "Email, name, notes text. Stored in database in EU region. Passwords stored hashed, never plain."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 17.2:** Which privacy laws or rules apply?
> - ☐ GDPR (Europe)
> - ☐ CCPA / CPRA (California)
> - ☐ COPPA (children under 13, USA)
> - ☐ HIPAA (health data, USA)
> - ☐ PCI DSS (card payments)
> - ☐ Other: `[FILL IN]`
> - ☐ Not sure → ask Legal: `[name, date]`

> 💬 **Question 17.3:** Mark each check.

| # | Check | Result | Done by (agent / human) |
|---|---|---|---|
| 17.1 | Whole site uses secure connection (HTTPS) only | `[FILL IN]` | `[FILL IN]` |
| 17.2 | Passwords stored safely, never visible in logs | `[FILL IN]` | `[FILL IN]` |
| 17.3 | A logged-in customer cannot read or change another customer's data by changing numbers in the web address or app requests | `[FILL IN]` | `[FILL IN]` |
| 17.4 | Common attacks tried: injected code in text boxes, forms and uploads | `[FILL IN]` | `[FILL IN]` |
| 17.5 | Automatic security scan run on code and on the live-like site | `[FILL IN]` | `[FILL IN]` |
| 17.6 | Known-vulnerable software parts (dependencies) checked and updated | `[FILL IN]` | `[FILL IN]` |
| 17.7 | Secrets (keys, tokens) are not in the code or in the mobile app files | `[FILL IN]` | `[FILL IN]` |
| 17.8 | Login sessions expire and log out everywhere when asked | `[FILL IN]` | `[FILL IN]` |
| 17.9 | Rate limits stop spam and brute-force attempts | `[FILL IN]` | `[FILL IN]` |
| 17.10 | Cookie / consent banner works and honors "No" | `[FILL IN]` | `[FILL IN]` |
| 17.11 | Customer can export and delete their data as law requires | `[FILL IN]` | `[FILL IN]` |
| 17.12 | Privacy policy and terms match what the product really does | `[FILL IN]` | `[FILL IN]` |
| 17.13 | Backups are encrypted and access is limited | `[FILL IN]` | `[FILL IN]` |
| 17.14 | Admin panel is not reachable by normal customers | `[FILL IN]` | `[FILL IN]` |
| 17.15 | Mobile: data stored on phone is protected, certificate checks are on | `[FILL IN]` | `[FILL IN]` |
| 17.16 | Independent security review or penetration test done before launch | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 17.4:** What is our plan if someone reports a security problem or data leaks?
> 💡 *Example:* "Security lead is told within 1 hour. Affected customers told within 72 hours as GDPR requires. Contact: security@acme.com."
> ✍️ **Your answer:** `[FILL IN]`

---

## 18. Performance and Load Tests ⭐

**Status:** ☐ Not started

> 💬 **Question 18.1:** How many customers do we expect at the same time?
> 💡 *Example:* "500 customers total, about 50 online at once at peak. Test for 5 times that (250) to have a safety margin."

| Item | ✍️ Your number |
|---|---|
| Customers at launch week | `[FILL IN]` |
| Peak customers online at once (expected) | `[FILL IN]` |
| Peak we will test for (suggest 5x expected) | `[FILL IN]` |
| Biggest burst (e.g. launch email or press mention) | `[FILL IN]` |

> 💬 **Question 18.2:** What speed is "good enough"?

| Measure | 💡 Example | ✍️ Your target |
|---|---|---|
| Main page loads | Under 3 s on 4G | `[FILL IN]` |
| Typical action responds (save, search) | Under 1 s | `[FILL IN]` |
| Slowest 5% of actions | Under 3 s | `[FILL IN]` |
| App cold start (mobile) | Under 3 s | `[FILL IN]` |
| Errors under load | Under 1% | `[FILL IN]` |

> 💬 **Question 18.3:** Which performance tests are done?

| Test | Plain meaning | Done? | Result |
|---|---|---|---|
| Load test | Normal-to-busy day | `[FILL IN]` | `[FILL IN]` |
| Stress test | Push until it breaks. How does it fail? | `[FILL IN]` | `[FILL IN]` |
| Spike test | Sudden jump in visitors | `[FILL IN]` | `[FILL IN]` |
| Soak test | Run for many hours to find slow leaks | `[FILL IN]` | `[FILL IN]` |
| Slow network test | 3G or poor Wi-Fi | `[FILL IN]` | `[FILL IN]` |
| Battery / memory use (mobile) | Does the app drain the phone? | `[FILL IN]` | `[FILL IN]` |
| Cost check | What does the cloud bill look like at 500 customers? | `[FILL IN]` | `[FILL IN]` |

---

## 19. Accessibility Tests

**Status:** ☐ Not started

> 💬 **Question 19.1:** Which accessibility standard are we aiming for?
> 💡 *Example:* "WCAG 2.2 Level AA."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 19.2:** Mark each check.

| # | Check | Result |
|---|---|---|
| 19.1 | Everything can be used with keyboard only (no mouse) | `[FILL IN]` |
| 19.2 | Screen reader (VoiceOver, TalkBack, NVDA) can read and use the main journey | `[FILL IN]` |
| 19.3 | Text has enough contrast against background | `[FILL IN]` |
| 19.4 | Pictures have text descriptions; videos have captions | `[FILL IN]` |
| 19.5 | Page works when text is made 200% bigger | `[FILL IN]` |
| 19.6 | Forms have clear labels and clear error messages | `[FILL IN]` |
| 19.7 | Touch targets are big enough (mobile) | `[FILL IN]` |
| 19.8 | Nothing flashes dangerously; motion can be reduced | `[FILL IN]` |
| 19.9 | Automatic accessibility scan has no serious issues | `[FILL IN]` |
| 19.10 | A human has tried it with assistive tools | `[FILL IN]` |

---

## 20. Devices, Browsers and App Store Coverage ⭐

**Status:** ☐ Not started

> 💬 **Question 20.1:** Which browsers and versions do we support? (Check your analytics or target audience first.)

| Browser | Versions | Tested by | Result |
|---|---|---|---|
| Chrome | Latest 2 | `[FILL IN]` | `[FILL IN]` |
| Safari | Latest 2 | `[FILL IN]` | `[FILL IN]` |
| Firefox | Latest 2 | `[FILL IN]` | `[FILL IN]` |
| Edge | Latest 2 | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 20.2:** Which phones and operating systems? Pick a spread: small and big screens, old and new, popular brands.

| Device | OS version | Screen size | Real device or simulator? | Result |
|---|---|---|---|---|
| iPhone (newest) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| iPhone (older, small screen) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Android (popular brand, new) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Android (budget phone) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Tablet (if supported) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 20.3:** Mobile app store checks.

| # | Check | Result |
|---|---|---|
| 20.1 | App passes Apple App Store review rules | `[FILL IN]` |
| 20.2 | App passes Google Play review rules | `[FILL IN]` |
| 20.3 | Privacy labels / data safety forms are filled in correctly | `[FILL IN]` |
| 20.4 | Install, update from old version, and uninstall all work | `[FILL IN]` |
| 20.5 | Beta channel works (TestFlight, Google Play testing track) | `[FILL IN]` |
| 20.6 | Push notifications arrive, open the right screen, and respect settings | `[FILL IN]` |
| 20.7 | Rotate screen, dark mode, large font, different language all look right | `[FILL IN]` |
| 20.8 | Old app versions: what happens when we force an update? | `[FILL IN]` |
| 20.9 | Deep links and share links open the right screen | `[FILL IN]` |

> 💬 **Question 20.4:** Screen sizes for the website: which widths do we test?
> 💡 *Example:* "360, 768, 1280 and 1920 pixels wide."
> ✍️ **Your answer:** `[FILL IN]`

---

## 21. Data, Backup and Recovery Tests

**Status:** ☐ Not started

| # | Check | Result |
|---|---|---|
| 21.1 | Data saved today is still there after a restart | `[FILL IN]` |
| 21.2 | Backups run automatically and we know when | `[FILL IN]` |
| 21.3 | We have **actually restored** a backup in a test and it worked | `[FILL IN]` |
| 21.4 | Database changes (migrations) work on a copy of real-size data | `[FILL IN]` |
| 21.5 | We can undo (roll back) a release in under `[FILL IN]` minutes | `[FILL IN]` |
| 21.6 | If the main server fails, the product recovers within `[FILL IN]` minutes | `[FILL IN]` |
| 21.7 | Old customer data still works with the new version | `[FILL IN]` |

> 💬 **Question 21.8:** How much data can we afford to lose, and how long can we be down? (Both must be answered.)
> 💡 *Example:* "Lose at most 1 hour of data. Down at most 4 hours."
> ✍️ **Your answer:** Data loss: `[FILL IN]` | Downtime: `[FILL IN]`

---

## 22. Third-Party Services and Integrations

**Status:** ☐ Not started

> 💬 **Question:** List every outside service the product needs. What happens if each one fails?

| Service | What it does for us | If it is down, what do we do? | Tested with fake / real? | Result |
|---|---|---|---|---|
| 💡 Stripe | Payments | Show "Try again later", keep cart | Fake (test mode) | Pass |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

*Common ones to remember: email sender, SMS, login providers, maps, analytics, file storage, search, AI model providers.*

---

## 23. Entry and Exit Rules for Each Stage 🚦 ⭐

**Status:** ☐ Not started

**Meaning:** *Entry rules* = what must be true BEFORE a stage may start. *Exit rules* = what must be true BEFORE we leave it. If any rule fails, we do not move forward until a human approves in writing.

| Stage | Entry rules (💡 examples) | ✍️ Your entry rules | Exit rules (💡 examples) | ✍️ Your exit rules |
|---|---|---|---|---|
| A. Build and Pre-Release | Requirements written. Test environment ready. | `[FILL IN]` | All critical journeys pass. 0 open critical/high bugs. Security scan clean. | `[FILL IN]` |
| B. Launch Readiness | Stage A exit met. Staging mirrors production. | `[FILL IN]` | Go/no-go checklist (Section 27) all ✅. Signed by approver. | `[FILL IN]` |
| C. Beta (1-50) | Monitoring and rollback tested. Support channel open. | `[FILL IN]` | 50 customers reached. Crash-free 99%+. 0 open critical bugs. Feedback reviewed. | `[FILL IN]` |
| D. Growth (to 500) | Stage C exit met. | `[FILL IN]` | Each checkpoint (100, 250, 500) passed. Final review held. | `[FILL IN]` |

> 💬 **Question 23.1:** Who can approve an exception, and how is it written down?
> 💡 *Example:* "Only the CTO. Written in Section 33 with the reason, the risk and an expiry date."
> ✍️ **Your answer:** `[FILL IN]`

---

## 24. Bugs: How We Report, Rank and Fix Them ⭐

**Status:** ☐ Not started

> 💬 **Question 24.1:** What does a good bug report contain? (Copy this list into your bug tool.)
> 1. Short title
> 2. Steps to repeat it (numbered)
> 3. What you expected
> 4. What really happened
> 5. Screenshot, recording or log
> 6. Device, browser or phone, and product version
> 7. Does it happen every time or sometimes?
> 8. Severity and priority (below)

> 💬 **Question 24.2:** How serious is a bug? Confirm or change the scale.

| Severity | Plain meaning | 💡 Example | Fix within (✍️ your time) |
|---|---|---|---|
| **Critical** | Data loss, money wrong, security hole, product down | Customer charged twice | `[FILL IN, e.g. 4 hours]` |
| **High** | Main journey broken, no workaround | Cannot log in on Android | `[FILL IN, e.g. 1 day]` |
| **Medium** | Feature broken but a workaround exists | Search slow on long notes | `[FILL IN, e.g. 1 week]` |
| **Low** | Small, cosmetic | Button 2 pixels off | `[FILL IN, e.g. next release]` |

> 💬 **Question 24.3:** How does a bug travel from found to closed?
> 💡 *Example:* "New → Triaged (within 1 day) → Assigned → Fixed → Re-tested by a different person or agent → Closed. If the re-test fails → Re-opened."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 24.4:** Who decides what to fix first, and how often do we meet?
> 💡 *Example:* "QA lead + Product Manager. Daily 15-minute bug review during Stages B and C."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 24.5:** What happens to bugs we choose NOT to fix before launch?
> 💡 *Example:* "Written into Section 33 as 'known issues' with owner, reason, and target fix date. Customer-facing ones are added to the help page."
> ✍️ **Your answer:** `[FILL IN]`

---

## 25. Test Schedule and Effort

**Status:** ☐ Not started

> 💬 **Question:** When does each testing activity happen, and who does it?

| Activity | Start | End | Owner | Effort (hours or days) | Depends on |
|---|---|---|---|---|---|
| Write E2E scenarios | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Build automatic tests | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Security review | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Load testing | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Accessibility testing | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Device testing | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Full regression (re-test everything) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Go/no-go meeting | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Beta monitoring | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 25.2:** What happens if the schedule slips? What do we cut, and what is **never** cut?
> 💡 *Example:* "Never cut: critical journeys, payments, security, backup restore test. Can cut: tablet layout, low-priority cosmetic checks."
> ✍️ **Your answer:** `[FILL IN]`

---

## 26. Stage A: Build and Pre-Release Testing ⭐

**Status:** ☐ Not started

> 💬 **Question 26.1:** How does a code change travel from idea to test environment? (This is your AI-driven development loop.)
> 💡 *Example:* "Ticket written → AI agent drafts code and tests → developer reviews → automatic tests run → merge → deploy to Test → agent runs E2E → human reviews failures."
> ✍️ **Your answer (draw your own loop):** `[FILL IN]`

> 💬 **Question 26.2:** Checklist. Tick when true.

- ☐ Every feature has acceptance rules written in plain words ("done means…")
- ☐ Unit and integration tests run automatically on every change
- ☐ E2E critical journeys pass in the Test environment
- ☐ Agent-written code and tests were read by a human
- ☐ Security scan has no open critical or high findings
- ☐ Accessibility scan has no serious issues
- ☐ First load test completed
- ☐ Every feature has at least one test in Section 12
- ☐ Exploratory testing session held (min `[FILL IN]` hours)
- ☐ Test results are saved with evidence

> 💬 **Question 26.3:** How often do we run the full E2E suite?
> 💡 *Example:* "Critical journeys on every merge. Full suite nightly. Full suite plus manual checks before each release candidate."
> ✍️ **Your answer:** `[FILL IN]`

> 🚦 **Stage A sign-off:** see Section 33.

---

## 27. Stage B: Launch Readiness (Go / No-Go) 🚦 ⭐

**Status:** ☐ Not started

> 💬 **Question 27.1:** Complete this checklist. **One ❌ on a "Must" row = No-Go.**

| # | Check | Must / Should | Result (✅ / ❌ / ➖) | Evidence | Checked by |
|---|---|---|---|---|---|
| 27.1 | All critical journeys pass on staging | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.2 | 0 open critical bugs; 0 open high bugs (or approved exceptions) | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.3 | Payment flows verified with test mode, plus one real low-value live transaction (refunded) | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.4 | Security scan and review complete, no open critical or high | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.5 | Privacy policy, terms and cookie banner live and accurate | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.6 | Load test passed at `[FILL IN]` times expected peak | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.7 | Backup restore tested successfully | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.8 | Rollback tested and takes under `[FILL IN]` minutes | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.9 | Monitoring and alerts live and tested (Section 30) | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.10 | On-call person named and reachable for launch week | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.11 | Support channel open; help page and contact email work | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.12 | Mobile apps approved in both stores, or release date confirmed | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.13 | Real emails (welcome, reset, receipt) send from the real domain and avoid spam folder | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.14 | Accessibility checks passed for main journey | Should | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.15 | Device and browser matrix passed | Should | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.16 | Known issues list written and shared with support | Should | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.17 | Launch-day plan written: who does what hour by hour | Should | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 27.18 | User acceptance (UAT) approved by business owner | Must | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 27.2:** Final decision. 🧑 *A human fills this in.*
> - ☐ **GO**
> - ☐ **GO with conditions:** `[FILL IN]`
> - ☐ **NO-GO. Reasons and next review date:** `[FILL IN]`
>
> Decided by: `[name]` Date: `[date]`

---

## 28. Stage C: Beta and First 50 Customers ⭐

**Status:** ☐ Not started

> 💬 **Question 28.1:** Who are the first 50 and how do we choose them?
> 💡 *Example:* "Invite-only. 50 people from our waiting list, mixed phone and laptop, mix of free and paid."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 28.2:** How do we turn customers on gradually?
> 💡 *Example:* "Day 1: 5 people. Day 3: 15. Day 7: 30. Day 14: 50. We pause at each step for 24 hours and check the numbers."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 28.3:** What do we watch every day? (Keep this tiny and visible.)

| Daily check | Target | Where to look | Owner |
|---|---|---|---|
| Errors and crashes | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Sign-up to first-success rate | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Payment failures | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Support messages and common questions | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Speed and uptime | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Bugs found by customers (not by us) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 28.4:** How do we ask beta customers for feedback, and how fast do we reply?
> 💡 *Example:* "In-app 2-question survey after first note. Direct email at day 3 and day 14. We reply within 24 hours."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 28.5:** In beta, can we test using real customer sessions? What is allowed?
> 💡 *Example:* "Yes, with a feature flag and only for customers who agreed. We never record screens without consent."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 28.6:** What makes us pause or roll back during beta?
> 💡 *Example:* "Any critical bug, crash-free rate below 99%, or payment error rate above 2%."
> ✍️ **Your answer:** `[FILL IN]`

**Stage C exit (50 customers) 🚦:**
- ☐ 50 real customers have used the product
- ☐ 0 open critical bugs; high bugs have a fix date
- ☐ Crash-free rate at or above `[FILL IN]`
- ☐ Feedback summarized and top 5 problems are decided on
- ☐ Support load is manageable
- ☐ Human sign-off recorded in Section 33

---

## 29. Stage D: Growing to 500 Customers ⭐

**Status:** ☐ Not started

> 💬 **Question 29.1:** What checkpoints do we use? At each one, we pause, look at the numbers and decide to continue.

| Checkpoint | Date reached | Health numbers OK? | New problems found | Fixed? | Approved to continue (name) |
|---|---|---|---|---|---|
| 50 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 100 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 250 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| 500 customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 29.2:** What extra tests do we run at each checkpoint?
> 💡 *Example:* "At 100: re-run load test at 5x. At 250: re-run security scan and review cloud costs. At 500: full regression, backup restore test, accessibility recheck, review all customer-reported bugs."

| Checkpoint | ✍️ Extra tests |
|---|---|
| 100 | `[FILL IN]` |
| 250 | `[FILL IN]` |
| 500 | `[FILL IN]` |

> 💬 **Question 29.3:** After launch, how do we avoid breaking things when we ship updates?
> 💡 *Example:* "Every release runs the full regression automatically. New features go behind a feature flag. Big changes are shown to 10% of customers first."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 29.4:** Which customer problems get turned into new tests?
> 💡 *Example:* "Every bug a customer finds gets a test so it can never return. A human checks the test exists before the bug is closed."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 29.5:** Customer health at 500. What do we measure?

| Measure | Target | Actual at 500 |
|---|---|---|
| Customers still active after 7 days | `[FILL IN]` | `[FILL IN]` |
| Main journey success rate | `[FILL IN]` | `[FILL IN]` |
| Crash-free sessions | `[FILL IN]` | `[FILL IN]` |
| Support tickets per 100 customers | `[FILL IN]` | `[FILL IN]` |
| Time to fix critical bugs | `[FILL IN]` | `[FILL IN]` |
| Uptime | `[FILL IN]` | `[FILL IN]` |
| Payment success rate | `[FILL IN]` | `[FILL IN]` |
| Customer satisfaction score | `[FILL IN]` | `[FILL IN]` |

**Stage D exit 🚦 (500 customers reached):**
- ☐ 500 real customers (as defined in Section 2.7)
- ☐ All numbers above are at target, or explained and approved
- ☐ Lessons-learned meeting held and written (see below)
- ☐ Test plan updated for the next phase

> 💬 **Question 29.6 (Lessons learned):** What worked, what didn't, what do we change in the *master template*?
> ✍️ **Your answer:** What worked: `[FILL IN]` | What didn't: `[FILL IN]` | Changes for the template: `[FILL IN]`

---

## 30. Monitoring, Alerts and Rollback ⭐

**Status:** ☐ Not started

> 💬 **Question 30.1:** What alerts wake someone up? Keep it to the few that really matter.

| Alert | Trigger (💡 example) | ✍️ Your trigger | Who is alerted | How fast must they react |
|---|---|---|---|---|
| Site down | Not reachable for 2 minutes | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| High errors | More than 2% of requests fail for 5 minutes | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Payment failures | More than 3 failed payments in a row | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| App crash spike | Crash-free rate below 99% | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Slow | Main page over 5 seconds for 10 minutes | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Unusual cloud cost | Daily cost 2x normal | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Security alert | Many failed logins from one place | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 30.2:** Is an alert tested? (An untested alert is a guess.)
> ✍️ **Your answer:** Last test date: `[FILL IN]` | Result: `[FILL IN]`

> 💬 **Question 30.3:** How do we undo a bad release? Write the exact steps in plain words.
> 💡 *Example:* "1) On-call person opens deploy page. 2) Clicks 'Roll back to previous version'. 3) Checks the home page and login. 4) Posts in #incidents. Takes about 10 minutes."
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 30.4:** Who tells customers when something is wrong, where, and in what words?
> 💡 *Example:* "Customer success posts on status page within 30 minutes. Template: 'We are aware of X. We are working on it. Next update at HH:MM.'"
> ✍️ **Your answer:** `[FILL IN]`

> 💬 **Question 30.5:** After any serious incident, what do we do?
> 💡 *Example:* "Blameless review within 3 days. Write: what happened, why, what we changed, and which new test will catch it."
> ✍️ **Your answer:** `[FILL IN]`

---

## 31. Risks and Backup Plans ⭐

**Status:** ☐ Not started

> 💬 **Question:** What could go wrong with the testing or the launch? For each, what do we do to stop it, and what do we do if it happens anyway?

| # | Risk | 💡 Example | Chance (L/M/H) | Damage (L/M/H) | Prevention | If it happens | Owner |
|---|---|---|---|---|---|---|---|
| R1 | Staging differs from production | Bug appears only live | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R2 | AI agent reports false passes | Test "passes" but nothing was checked | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R3 | App store rejects the app | Launch delayed | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R4 | Surge of visitors | Press mention crashes site | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R5 | Key person unavailable | Only one person knows deploy | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R6 | Third-party outage | Payment provider down | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R7 | Data leak | Customer sees other's data | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R8 | Schedule pressure skips testing | "Ship it anyway" | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R9 | Cloud bill shock | Cost grows faster than customers | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| R10 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

---

## 32. Reports and Numbers We Track

**Status:** ☐ Not started

> 💬 **Question 32.1:** What reports do we create, how often, and for whom?

| Report | Who reads it | How often | Made by | Where saved |
|---|---|---|---|---|
| Test run summary (pass / fail / skipped) | Team | Every run | Agent, checked by QA | `[FILL IN]` |
| Bug status report | Product + Dev lead | Daily in Stage B/C, weekly after | `[FILL IN]` | `[FILL IN]` |
| Go/no-go report | Approver | Once per gate | `[FILL IN]` | `[FILL IN]` |
| Beta health report | Everyone | Daily in Stage C | `[FILL IN]` | `[FILL IN]` |
| Checkpoint report (100 / 250 / 500) | Approver | Per checkpoint | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 32.2:** Which numbers prove quality? Tick what you will track.
> - ☐ Test pass rate and number skipped
> - ☐ Test coverage of features (Section 12)
> - ☐ Bugs found, fixed and open, by severity
> - ☐ Bugs that escaped to customers (found after release)
> - ☐ Time to fix by severity
> - ☐ Flaky test count
> - ☐ Crash-free rate and error rate
> - ☐ Speed and uptime
> - ☐ Customer satisfaction and support volume
> - ☐ Agent accuracy (Section 8.4 spot-check results)

---

## 33. Approvals and Sign-Off 🧑 ⭐

**Status:** ☐ Not started

**Rule:** Only humans sign. An AI agent can prepare the report but never signs.

> 💬 **Question 33.1:** Sign each gate. Write the exact date and attach evidence.

| Gate | Decision (Go / Go with conditions / No-Go) | Conditions | Name | Role | Date | Evidence link |
|---|---|---|---|---|---|---|
| Plan approved | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Stage A exit | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Stage B: Launch | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Stage C exit (50) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Checkpoint 100 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Checkpoint 250 | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Stage D exit (500) | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

> 💬 **Question 33.2:** Known issues accepted at launch (exceptions). Each needs an owner and an expiry date.

| Issue | Severity | Why accepted | Owner | Fix by | Approved by |
|---|---|---|---|---|---|
| `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

---

## 34. Final Self-Check ⭐

**Status:** ☐ Not started

Read this list before sharing the plan. Tick each box. If you cannot tick one, go back to that section.

**Completeness**
- ☐ No `[FILL IN]` left anywhere (each is answered, `UNKNOWN - ask …` or `N/A - because …`)
- ☐ No 💡 example text is left in a ✍️ answer
- ☐ All ⭐ sections are `☑ Done`
- ☐ Every feature in Section 2.5 has a test in Section 12
- ☐ Every critical journey in Section 5.3 is in Section 14

**Clarity**
- ☐ A new team member could run a test from this plan without asking anyone
- ☐ Every target uses a number
- ☐ Every name, date and link is real and works
- ☐ Every hard word is in the Glossary

**Safety**
- ☐ No real passwords, keys, card numbers or customer data are in this file
- ☐ Agent rules in Section 8 are confirmed
- ☐ Every gate has a named human approver
- ☐ Rollback and backup restore have been tried at least once

**Ready**
- ☐ Plan approved in Section 33
- ☐ A copy saved to `Testing and quality assurance/`
- ☐ Next review date is in the calendar

---

## 35. Change Log

| Version | Date | Who | What changed | Why |
|---|---|---|---|---|
| 0.1 | `[FILL IN]` | `[FILL IN]` | First draft | New project |
| | | | | |

---

# APPENDIX A: AI Agent Prompt Library 🤖

**How to use:** Copy a prompt, replace anything in `{CURLY BRACKETS}`, and paste it into your AI agent. **A human must read the answer before it is used.** Never paste passwords, keys or real customer data.

### A.0 Master prompt (paste this first, every time)

```
You are a QA assistant on the project "{PROJECT NAME}".
Rules:
1. Use ONLY the information I give you and the files in this project. If you do not know something, say "I do not know" and list what you need. Never guess.
2. Test only in {TEST ENVIRONMENT URL}. Never touch production. Never use real customer data or real payment cards.
3. For every result, give evidence: a screenshot, log line or recording path.
4. Report failures, skipped tests and anything odd. Do not hide them.
5. Never say a gate has passed. Prepare the report. A human signs.
6. Keep answers short and in plain words a 10-year-old could follow.
Product version under test: {VERSION}. Today's date: {DATE}.
```

### A.1 Draft the plan from my notes
```
Read the notes below and fill in Sections {SECTION NUMBERS} of End_to_End_Testing_Plan.md.
Keep the question, example and answer format. Replace [FILL IN] only when my notes give a clear answer.
Where my notes are silent, write "UNKNOWN - ask {who}" and list the question for me.
Notes: {PASTE NOTES}
```

### A.2 Write end-to-end scenarios
```
Using the customer journey in Section 5 and the features in Section 2.5, write end-to-end scenarios in the Section 14 format.
Cover the happy path and at least 5 unhappy paths per critical journey.
Each scenario needs: ID, name, priority, persona, device, setup, numbered steps, expected result, evidence needed.
Do not invent features that are not in Section 2.5.
```

### A.3 Run the tests and report
```
Run the end-to-end scenarios {IDs} in {ENVIRONMENT} on {BROWSERS/DEVICES}.
For each: Pass / Fail / Skipped, evidence link, and time taken.
Then list: (a) every failure with steps to repeat, (b) every skipped test and why, (c) anything unexpected, even if the test passed.
Do not retry a failing test more than 3 times. Mark it "possibly flaky" if results differ.
```

### A.4 Write a bug report
```
Turn this failure into a bug report using Section 24.1.
Suggest a severity from Section 24.2 and explain why in one sentence. A human will confirm.
Failure details: {PASTE LOG / SCREENSHOT DESCRIPTION}
```

### A.5 Triage bugs
```
Here is the list of open bugs: {LIST}.
Group by severity, find duplicates, and flag any that block a launch gate in Section 23.
Output a table: ID, title, severity, blocks which gate?, suggested owner, suggested next step. Mark all suggestions as "for human review".
```

### A.6 Security smoke test
```
Run the automatic checks in Section 17 rows {ROWS} against {TEST URL}. Test only what I list.
Report each finding with severity and steps to repeat. Send any serious security finding only to {SECURITY CONTACT}, not to the public bug list.
```

### A.7 Prepare the go/no-go report
```
Fill the Section 27 checklist using the latest test results and evidence in {RESULTS FOLDER}.
For each row give: ✅ / ❌ / ➖, and the evidence link. If evidence is missing, mark the row ❌ "no evidence".
Do NOT write the final decision. End with a summary: number of Must rows passed, number failed, and the top 3 risks.
```

### A.8 Daily beta health summary
```
From the monitoring data and support messages for {DATE}, fill the Section 28.3 table.
Highlight anything outside the targets, the top 3 customer complaints, and any bug that customers found before we did.
Recommend "continue / pause / roll back" using Section 28.6. A human decides.
```

### A.9 Check the plan for gaps
```
Review End_to_End_Testing_Plan.md. List: unanswered [FILL IN] items, example text left in answers, targets without numbers, features without tests, gates without named approvers, and contradictions between sections.
Do not fix anything. Just list the problems with section numbers.
```

### A.10 Check the agent (spot check)
```
Re-run these {N} previously passed tests: {IDs}. Compare to the earlier evidence. Report any difference. This is a check on the earlier agent's work.
```

---

# APPENDIX B: Glossary (Hard Words Made Easy)

| Word | Plain meaning |
|---|---|
| **Acceptance test (UAT)** | The person who asked for the product checks it is what they wanted |
| **Accessibility** | Making the product usable by people with disabilities (blind, deaf, limited movement, etc.) |
| **Agent (AI agent)** | A computer helper that can do steps on its own, like writing or running tests |
| **API** | A doorway that lets programs talk to each other |
| **Automated test** | A test a computer runs by itself |
| **Backup** | A saved copy of data in case something is lost |
| **Beta** | A trial period with a small group before everyone gets the product |
| **Bug** | A mistake in the product |
| **CI/CD** | Robots that automatically test and deliver each code change |
| **Crash-free rate** | The share of app sessions that did not crash |
| **Critical journey** | A path through the product that must work or the product is worthless |
| **Dependency** | Another piece of software or service we rely on |
| **E2E (end to end)** | Testing a whole customer journey from start to finish |
| **Entry / exit rules** | What must be true to start / finish a stage |
| **Environment** | A place the product runs (test, staging, production) |
| **Evidence** | Proof, like a screenshot or log, that a test really ran |
| **Exploratory testing** | A human tries things freely to find surprises |
| **Feature flag** | An on/off switch to show a feature to only some customers |
| **Flaky test** | A test that sometimes passes and sometimes fails for no clear reason |
| **Go / no-go** | The final yes-or-no before launch |
| **Integration test** | Checks that parts of the system work together |
| **Known issue** | A bug we know about and decided to ship with, written down |
| **Load test** | Checks how the product behaves with many customers at once |
| **Migration** | Changing the structure of stored data |
| **Monitoring** | Watching the live product for problems |
| **On-call** | The person ready to react if something breaks |
| **Persona** | A made-up but realistic customer used for planning |
| **Production** | The live product real customers use |
| **Regression test** | Re-testing old features to be sure new changes did not break them |
| **Rollback** | Going back to the previous working version |
| **Severity** | How bad a bug is |
| **Soak test** | Running for many hours to find slow-building problems |
| **Staging** | A near-copy of production used for a final rehearsal |
| **Stress test** | Pushing the product past its limit to see how it fails |
| **Traceability** | A map linking each requirement to its tests |
| **Unit test** | Checks one small piece of code on its own |
| **Webhook** | A message one system sends another when something happens (e.g., "payment done") |
| **WCAG** | The international rules for accessible websites |

---

# APPENDIX C: Ready-to-Copy Checklists

### C.1 Before every release (10-minute check)
- ☐ Version number written down: `[FILL IN]`
- ☐ All automatic tests green
- ☐ Critical journeys passed (evidence attached)
- ☐ No new critical or high bugs
- ☐ Rollback steps are ready and a person is named
- ☐ Release notes written for customers and support
- ☐ Monitoring open on a screen during release

### C.2 After every release (first hour)
- ☐ Home page, login, main journey checked by a human
- ☐ Error rate normal
- ☐ Payments working
- ☐ No spike in support messages
- ☐ Post "released OK" or "rolled back" in the team channel

### C.3 Weekly during Stages C and D
- ☐ Bug review held
- ☐ Customer feedback read
- ☐ Agent spot check done (Section 8.4)
- ☐ Flaky tests list reviewed
- ☐ Plan changes recorded in Change Log

---

# APPENDIX D: References and Standards Behind This Template

This template draws on widely used, public good practice. Use them as further reading; check each for the current edition before citing.

| Topic | Source |
|---|---|
| Test planning and documentation | ISO/IEC/IEEE 29119 (Software Testing) and the older IEEE 829 test plan structure |
| Testing vocabulary and levels | ISTQB Glossary and Foundation syllabus |
| Quality characteristics | ISO/IEC 25010 (product quality model) |
| Web security checks | OWASP Application Security Verification Standard (ASVS), OWASP Top 10, OWASP Web Security Testing Guide |
| Mobile security checks | OWASP Mobile Application Security (MASVS / MASTG) |
| Accessibility | W3C Web Content Accessibility Guidelines (WCAG 2.2) |
| Payment card security | PCI DSS |
| Privacy | GDPR, CCPA/CPRA, COPPA (as they apply to you) |
| Reliability and monitoring | Google SRE Book (error budgets, monitoring, incident review) |
| Release safety | DORA / Accelerate research metrics (change failure rate, time to restore) |
| App stores | Apple App Store Review Guidelines, Google Play Developer Policy |
| AI-assisted testing | Treat AI output as a draft that humans verify; keep evidence and logs |

*This template is guidance, not legal advice. Ask a qualified person about privacy, payment and accessibility law for your country.*

---

*End of template. When copying for a new project, change only the `[FILL IN]` items, never the structure, so every project stays comparable.*
