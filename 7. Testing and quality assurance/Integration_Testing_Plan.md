# How to Fill This Document (Read This First)

> **Template version 1.0** | Standard Integration Testing Plan template | Copy this file into each new project's `Testing and quality assurance` folder and fill the copy. Never edit the master.

**Who this is for:** Anyone. You do not need to be a tester or a programmer. If you can answer a question in plain words, you can fill this in.

**What this document is:** A plan that says *how we will check that the different parts of our product work correctly together* (for example: "when a customer clicks Pay, does the payment company really get the order, and does the customer really get the receipt?"). That checking is called **integration testing**.

**Where it fits:** This plan covers the AI-Driven Development Life Cycle from the first line of code until **the first 500 customers have used the product**.

## The 6 Simple Rules

1. **Go top to bottom.** Do not skip around. Each part builds on the one before.
2. **Answer every question.** If it truly does not apply, write `N/A - because <short reason>`. Never leave it blank.
3. **If you do not know, write `UNKNOWN - ask <name>`.** An honest "unknown" is better than a guess.
4. **Use the examples as a guide, then delete them.** Examples look like this: `> Example: ...`
5. **Use short sentences and real names.** Write "Stripe", not "the payment thing". Write numbers, not "fast" or "many".
6. **Tick the boxes** `[x]` when something is done. An empty box `[ ]` means not done.

## Legend

| Mark | Meaning |
|---|---|
| `[ ]` | Not done |
| `[x]` | Done |
| `<...>` | Replace this with your answer |
| `> Example:` | A sample answer. Delete it after reading |
| 🤖 | Instruction for AI agents (humans may read it too) |
| ⛔ | Stop. Do not move on until this is done |

## 🤖 Notes for AI Agents

- Treat every `<...>` as a required field. If a field is empty, ask the human the matching question instead of inventing an answer.
- Do not invent facts, names, URLs, numbers, or credentials. Write `UNKNOWN` and ask.
- Use the exact IDs defined in this document (e.g., `INT-001`, `ENV-01`, `DEF-001`) when creating tests, tickets, or reports.
- Tables marked `(machine-readable)` must keep their column names and order unchanged.
- Never place real secrets, passwords, API keys, or real customer data in this file. Write the *name* of where the secret is stored instead.

## Quick Pre-Check (answer in 1 minute)

- [ ] I know the product name and who owns it.
- [ ] I know which parts of the product talk to each other (or I can ask someone).
- [ ] I have access to a test (non-live) version of the product.
- [ ] I know who will approve this plan.

If any box is empty, start with Section 1 and ask for help before continuing.

---

# Integration Testing Plan

## 0. Document Control

**Question: Who wrote this, which version is it, and who approves it?**

| Field | Your Answer |
|---|---|
| Product name | `<>` |
| Project / repository link | `<>` |
| Document version | `<0.1>` (Template version: 1.0) |
| Date created (YYYY-MM-DD) | `<>` |
| Last updated (YYYY-MM-DD) | `<>` |
| Author | `<>` |
| Reviewer(s) | `<>` |
| Approver (final yes/no) | `<>` |
| Status | `<Draft / In Review / Approved / Retired>` |

**Change history**

| Version | Date | Who | What changed |
|---|---|---|---|
| 0.1 | `<>` | `<>` | First draft |

---

## 1. Purpose and Big Picture

**Question 1.1: In one or two sentences, what does the product do, and for whom?**

> Example: "FitTrack is a mobile app that lets runners log workouts and share them with friends."

`<Your answer>`

**Question 1.2: Why are we doing integration testing for this product? What bad thing are we trying to prevent?**

> Example: "Prevent customers being charged but not receiving their subscription."

`<Your answer>`

**Question 1.3: What does "success" look like at the end?**

- [ ] All must-pass integration tests pass before launch
- [ ] No open Critical or High defects at launch
- [ ] First 500 customers complete the main journey without blocking integration failures
- [ ] Other: `<>`

**Question 1.4: Which product type is this?** (tick all that apply)

- [ ] Web app / SaaS
- [ ] Mobile app (iOS)
- [ ] Mobile app (Android)
- [ ] Uses AI/LLM features (models, agents, prompts)
- [ ] Other: `<>`

**Question 1.5: Which industry is this product in?** (Tick one. Then also fill the matching block in **Appendix C**.)

- [ ] General / none of these
- [ ] Fintech / payments
- [ ] Health / wellness
- [ ] E-commerce / marketplace
- [ ] Education / kids
- [ ] Other: `<>`

---

## 2. Scope: What Is and Is Not Being Tested

**Question 2.1: What are the "parts" (components) of the product?** List each part and what it does. Think: screens, servers, databases, outside companies' services.

> Example: App screen → Our API → Database → Stripe (payments) → SendGrid (email)

| ID | Part Name | What it does | Owner | Our own or outside company? |
|---|---|---|---|---|
| COMP-01 | `<>` | `<>` | `<>` | `<Ours / Outside>` |
| COMP-02 | `<>` | `<>` | `<>` | `<>` |
| COMP-03 | `<>` | `<>` | `<>` | `<>` |

**Question 2.2: Which connections between parts will we test?** (Each connection is an "integration point".)

> Example: INT-001: Web app sends login details to the Login API. The Login API answers with a session.

| ID (machine-readable) | From | To | What travels between them | Priority (High/Med/Low) | Risk if it breaks |
|---|---|---|---|---|---|
| INT-001 | `<COMP-01>` | `<COMP-02>` | `<>` | `<>` | `<>` |
| INT-002 | `<>` | `<>` | `<>` | `<>` | `<>` |
| INT-003 | `<>` | `<>` | `<>` | `<>` | `<>` |

**Question 2.3: What is IN scope?**

`<List features, flows, and integration points that WILL be tested>`

**Question 2.4: What is OUT of scope, and why?**

> Example: "Testing the internal workings of Stripe. Reason: it is their job, we only test our connection."

`<List what will NOT be tested and the reason>`

**Question 2.5: What do we assume is true? (If an assumption is wrong, the plan may need to change.)**

> Example: "The test version of Stripe behaves like the real one."

`<Your assumptions>`

---

## 3. People and Responsibilities

**Question 3.1: Who does what?**

> Example: QA / test lead = Priya Shah, runs all tests and writes the daily summary. Backup = Tom Lee. AI agent = "TestWriter-Bot", allowed to draft test cases only; its human owner is Priya.

| Role | Name | What they are responsible for | Backup person |
|---|---|---|---|
| Product owner | `<>` | Decides what matters most | `<>` |
| Project manager | `<>` | Schedule and status | `<>` |
| Developer lead | `<>` | Fixes defects | `<>` |
| QA / test lead | `<>` | Runs and reports tests | `<>` |
| Security reviewer | `<>` | Checks safety risks | `<>` |
| Support lead | `<>` | Handles customer issues | `<>` |
| AI agent(s) | `<name/tool>` | `<what the agent is allowed to do>` | `<human owner>` |

**Question 3.2: What are AI agents allowed and NOT allowed to do?**

| Action | Allowed? (Yes / No / Only with human approval) |
|---|---|
| Write test cases | `<>` |
| Run tests in the test environment | `<>` |
| Create and update defect tickets | `<>` |
| Change application code | `<>` |
| Touch live (production) systems | `<No unless stated here>` |
| Use real customer data | `<No unless stated here>` |
| Approve the launch | `<No>` |

---

## 4. Test Environments

**Question 4.1: Where will tests run?** Each place is an environment.

> Example: ENV-02 | Staging | Main integration testing | https://staging.booknook.example | QA team and developers | No (fake data only).

| ID | Environment name | Purpose | Web address / location | Who can use it | Uses real customer data? |
|---|---|---|---|---|---|
| ENV-01 | Local (developer computer) | Early checking | `<>` | Developers | No |
| ENV-02 | Test / Staging | Main integration testing | `<>` | `<>` | No |
| ENV-03 | Pre-production | Final check, looks like live | `<>` | `<>` | `<No / Masked only>` |
| ENV-04 | Production (live) | Real customers, limited safe checks only | `<>` | `<>` | Yes |

**Question 4.2: For each outside service, do we use a test (sandbox) version?**

| Outside service | Sandbox available? | Sandbox account/location (name only, no passwords) | Known differences from the real one |
|---|---|---|---|
| `<e.g., Stripe>` | `<Yes/No>` | `<>` | `<>` |
| `<>` | `<>` | `<>` | `<>` |

**Question 4.3: Which devices and browsers must be covered?**

- Web browsers: `<e.g., Chrome latest, Safari latest, Firefox latest, Edge latest>`
- iOS versions / devices: `<e.g., iOS 17 and 18, iPhone 13 and newer>`
- Android versions / devices: `<e.g., Android 13 and 14, Pixel and Samsung>`
- Screen sizes: `<>`
- Network conditions to simulate: `<e.g., fast Wi-Fi, slow 3G, offline>`

**Question 4.4: Where do secrets (passwords, keys) live? (Write the place, NOT the secret.)**

> Example: "In the team password manager, folder 'Product-X Test'."

`<Your answer>`

⛔ **Stop check:** Is every environment above reachable by the people who need it?
- [ ] Yes
- [ ] No (write who must fix it and by when): `<>`

---

## 5. Test Data

**Question 5.1: What fake data do we need?**

> Example: Test user accounts | qa.user1@example.com to qa.user20@example.com | Created by a setup script before each run | Priya | Yes, reset every night. Edge cases | a name with 200 letters, an emoji name, an empty phone number.

| Data needed | Example | How we create it | Who owns it | Reset between runs? |
|---|---|---|---|---|
| Test user accounts | `<qa.user1@example.com>` | `<script/manual>` | `<>` | `<Yes/No>` |
| Test payment cards (sandbox only) | `<provider's official test card>` | `<>` | `<>` | `<>` |
| Sample content/files | `<>` | `<>` | `<>` | `<>` |
| Edge cases (empty, very long, special characters, other languages) | `<>` | `<>` | `<>` | `<>` |

**Question 5.2: Rules for data safety**

- [ ] No real customer personal data is used in test environments
- [ ] If copied from live, data is masked (names, emails, phones, cards hidden or scrambled)
- [ ] Test data is deleted after the test cycle
- [ ] Other rule: `<>`

---

## 6. Test Approach and Strategy

**Question 6.1: Which integration style will we use?**

- [ ] Bottom-up (test small connected pieces first, then bigger)
- [ ] Top-down (test the main flow first, fill in details later)
- [ ] Big-bang (connect everything and test at once - use only for small products)
- [ ] Sandwich/hybrid
- Reason for our choice: `<>`

**Question 6.2: What kinds of checks will we do?** (tick all that apply and give a goal)

> Example: `[x]` Error handling | Pass = when the email service is down, the reservation is still saved and the user sees a friendly message within 3 seconds.

| Check type | Use it? | What "pass" means (use numbers) |
|---|---|---|
| Connection check (A can reach B) | `[ ]` | `<e.g., 100% of calls reach the target>` |
| Data check (right information arrives, nothing lost or changed) | `[ ]` | `<>` |
| Error handling (what happens when B is down or slow) | `[ ]` | `<e.g., user sees friendly message within 3 seconds>` |
| Contract check (messages match the agreed format) | `[ ]` | `<>` |
| Security check (only allowed people can reach data) | `[ ]` | `<>` |
| Performance check (speed under normal load) | `[ ]` | `<e.g., 95% of requests under 500 ms>` |
| Compatibility check (browsers/devices) | `[ ]` | `<>` |
| Upgrade/migration check (old data still works after update) | `[ ]` | `<>` |
| Accessibility check | `[ ]` | `<>` |

**Question 6.3: What is automated and what is done by hand?**

| Area | Automated (tool name) | Manual (who) |
|---|---|---|
| API tests | `<>` | `<>` |
| Web UI flows | `<>` | `<>` |
| Mobile flows | `<>` | `<>` |
| Outside-service checks | `<>` | `<>` |
| Exploratory testing (testers explore freely) | N/A | `<>` |

**Question 6.4: AI-specific integration (skip if the product has no AI features: write `N/A`)**

| Question | Your answer |
|---|---|
| Which AI models or services are used? | `<>` |
| What happens if the AI service is slow, down, or returns nonsense? | `<>` |
| How do we check AI answers are acceptable (rules, sample questions, human review)? | `<>` |
| What AI cost limit per day/month triggers an alert? | `<>` |
| What must the AI never do or say (safety rules)? | `<>` |
| How do we test that prompt or model changes did not break other parts? | `<>` |

---

## 6A. Security and Privacy Checks

**Question 6A.1: What sensitive information moves between parts?** (tick all that apply)

- [ ] Names, emails, phone numbers
- [ ] Passwords or login sessions
- [ ] Payment details
- [ ] Health, financial, or children's data
- [ ] Location or device data
- [ ] Other: `<>`

**Question 6A.2: Which rules or standards must we follow?** (tick all that apply)

- [ ] GDPR (people in Europe)
- [ ] CCPA/CPRA (people in California)
- [ ] SOC 2
- [ ] PCI DSS (card payments)
- [ ] HIPAA (US health data)
- [ ] COPPA (children under 13)
- [ ] Other: `<>`
- [ ] None. Reason: `<>`

**Question 6A.3: For each sensitive data flow, what do we check?**

> Example: INT-002 | Member email and address | Only the logged-in member can read their own record; another member's ID returns "not allowed" | INT-002-TC-07 | Pass.

| Integration ID | Sensitive data | Check (what must be true) | Test ID | Pass/Fail |
|---|---|---|---|---|
| `<INT-001>` | `<>` | `<e.g., data is encrypted while travelling; only logged-in owner can read it>` | `<>` | `<>` |
| `<>` | `<>` | `<>` | `<>` | `<>` |

**Question 6A.4: Privacy promises we must be able to prove**

| Promise | How we test it | Done |
|---|---|---|
| Customer can delete their data and it disappears from every connected part, including outside services | `<>` | `[ ]` |
| Customer can download their data | `<>` | `[ ]` |
| Customer consent choices (e.g., marketing emails) are respected by every part | `<>` | `[ ]` |
| Data is not sent to outside companies without a legal reason or consent | `<>` | `[ ]` |
| Logs do not contain passwords, card numbers, or full personal data | `<>` | `[ ]` |

---

## 6B. Performance and Load Targets

**Question 6B.1: How many people do we expect?** (Be realistic. Write numbers.)

| Measure | Day 1 | End of first month | When we hit 500 customers | Safety margin (e.g., 3x) |
|---|---|---|---|---|
| Customers signed up | `<>` | `<>` | `500` | N/A |
| Customers using it at the same time (peak) | `<>` | `<>` | `<>` | `<>` |
| Requests per second between parts (peak) | `<>` | `<>` | `<>` | `<>` |

**Question 6B.2: What speed is "good enough"?**

> Example: INT-001 | Press Reserve | 95% of requests under 500 ms | Never slower than 3 seconds | INT-001-TC-09.

| Integration ID | Action | Target (e.g., 95% under 500 ms) | Maximum allowed (e.g., 3 seconds) | Test ID |
|---|---|---|---|---|
| `<INT-001>` | `<>` | `<>` | `<>` | `<>` |
| `<>` | `<>` | `<>` | `<>` | `<>` |

**Question 6B.3: Which load tests will we run?**

- [ ] Normal load (expected number of customers)
- [ ] Peak load (busiest moment, e.g., launch announcement)
- [ ] Stress (push beyond limits to see how it fails)
- [ ] Soak (run for hours to find slow leaks)
- [ ] Outside-service limits (their rate limits, quotas, or costs)

**Question 6B.4: What happens when we hit a limit?** (Queue, slow down politely, show a message, switch off a feature?)

`<Your answer>`

---

## 6C. Contracts and API Versioning

**Question 6C.1: Where are the agreed message formats (contracts) written down?**

> Example: INT-001 | https://github.com/example/booknook/api/openapi.yaml | REST (OpenAPI) | v1 | Backend team | Web app and mobile app.

| Integration ID | Contract location (link) | Format (REST/GraphQL/events/other) | Version | Owner (provider) | Users (consumers) |
|---|---|---|---|---|---|
| `<INT-001>` | `<>` | `<>` | `<v1>` | `<>` | `<>` |
| `<>` | `<>` | `<>` | `<>` | `<>` | `<>` |

**Question 6C.2: How do we make sure a change does not break the other side?**

- [ ] Contracts are checked automatically on every code change
- [ ] A change that removes or renames something is blocked until the other side agrees
- [ ] Old versions keep working until `<date/rule>`
- [ ] Mobile apps: we assume old app versions stay in use for `<N>` months and still test against them
- [ ] Outside services: we are subscribed to their change/deprecation notices (where: `<>`)

**Question 6C.3: Who is told, and how, when a contract changes?**

`<Your answer>`

---

## 6D. AI-Agent Run Logs and Traceability

(Skip with `N/A` only if no AI agent or AI feature touches testing or the product.)

**Question 6D.1: What must be recorded every time an AI agent writes, runs, or changes anything?**

> Example: "Instructions (prompt) it was given" | Saved in the `agent-logs` folder as `2026-11-05_TestWriter_run03.md` | Kept for 12 months.

| Item | Where it is stored | Kept for |
|---|---|---|
| Date and time | `<>` | `<>` |
| Which agent and which model/version | `<>` | `<>` |
| Instructions (prompt) it was given | `<>` | `<>` |
| What it did (tests written, run, tickets changed) | `<>` | `<>` |
| Results and evidence | `<>` | `<>` |
| Which human approved it, if approval was needed | `<>` | `<>` |

**Question 6D.2: Which agent actions always need a human to approve first?**

`<e.g., closing a Critical defect, changing code, anything touching live systems>`

**Question 6D.3: How do we notice if an agent's work is wrong?**

- [ ] A human reviews a sample of agent work: `<N%>` every `<period>`
- [ ] Agent-written tests are checked against a known-broken build to confirm they can fail
- [ ] A change in model or prompt triggers a re-check of agent-written tests
- [ ] Other: `<>`

---

## 7. Test Cases

**Question 7.1: For each integration point in Section 2.2, what exact steps do we check?**

> Example: INT-001-TC-01. Steps: 1) Open login page. 2) Enter a valid test email and password. 3) Press Login. Expected result: Home page opens within 2 seconds and the user's name is shown.

| Test ID (machine-readable) | Integration ID | Title | Starting situation | Steps | Expected result | Priority | Auto/Manual | Status |
|---|---|---|---|---|---|---|---|---|
| INT-001-TC-01 | INT-001 | `<>` | `<>` | `<1... 2... 3...>` | `<>` | `<High/Med/Low>` | `<>` | `<Not run / Pass / Fail / Blocked>` |
| INT-001-TC-02 | INT-001 | `<error case>` | `<>` | `<>` | `<>` | `<>` | `<>` | `<>` |
| INT-002-TC-01 | INT-002 | `<>` | `<>` | `<>` | `<>` | `<>` | `<>` | `<>` |

**Question 7.2: Have we covered the "what if it goes wrong" cases for each integration point?**

For every integration point, ask: what if the other side is...

- [ ] Slow (timeout)
- [ ] Down (not reachable)
- [ ] Sending wrong or incomplete data
- [ ] Sending the same message twice
- [ ] Sending messages in the wrong order
- [ ] Rejecting our login/permission
- [ ] Changed to a new version

**Question 7.3: Which journeys must work from start to finish? (End-to-end customer journeys)**

> Example: Sign up → Verify email → Choose plan → Pay → Receive receipt → Use main feature.

| Journey ID | Journey description | Integration points touched | Must pass before launch? |
|---|---|---|---|
| JRN-01 | `<>` | `<INT-001, INT-002...>` | `<Yes/No>` |
| JRN-02 | `<>` | `<>` | `<>` |

---

## 8. Entry and Exit Rules (When to Start and When to Stop)

**Question 8.1: Before testing starts, what must be true? (Entry criteria)**

- [ ] Each part has passed its own smaller checks (unit tests)
- [ ] Test environment is working (Section 4)
- [ ] Test data is ready (Section 5)
- [ ] Test cases are written and reviewed (Section 7)
- [ ] Build/version to test is named: `<version/build number>`
- [ ] Other: `<>`

**Question 8.2: When can we say testing is finished? (Exit criteria, use numbers)**

> Example: `[x]` 100% of High-priority tests run and 100% passed. `[x]` 95% of all tests passed. `[x]` Open Critical defects: 0. `[x]` Open Medium defects: max 5, each with a workaround and an owner.

- [ ] `<e.g., 100%>` of High-priority tests run and `<e.g., 100%>` passed
- [ ] `<e.g., 95%>` of all tests passed
- [ ] Open Critical defects: `<0>`
- [ ] Open High defects: `<0>`
- [ ] Open Medium defects: `<max N, each has a workaround and an owner>`
- [ ] All must-pass journeys (Section 7.3) passed
- [ ] Other: `<>`

**Question 8.3: When must we pause testing? (Suspension rules)**

> Example: "Pause if the test environment is down for more than 2 hours, or a Critical defect blocks 30% of tests."

`<Your answer>`

---

## 9. Defect (Bug) Handling

**Question 9.1: How serious is a problem? (Severity levels)**

| Level | Meaning | Example | Fix within |
|---|---|---|---|
| Critical | Product unusable, data loss, money or safety issue | Customers charged twice | `<e.g., 24 hours>` |
| High | Main feature broken, no workaround | Cannot log in | `<>` |
| Medium | Feature partly broken, workaround exists | Receipt email delayed | `<>` |
| Low | Small or cosmetic | Typo in a message | `<>` |

**Question 9.2: Where do we record defects, and what must every defect include?**

> Example: DEF-014 | "Receipt email missing after payment" | Severity High | Test INT-003-TC-02 | ENV-02, build 1.4.2 | Steps: pay with the sandbox card, wait 5 minutes | Expected: email arrives | Actual: no email | Owner: Tom | Screenshot attached.

- Defect tracker name and link: `<>`
- Every defect must have (tick to confirm the rule):
  - [ ] ID (e.g., DEF-001)
  - [ ] Related test ID and integration ID
  - [ ] Environment and build/version
  - [ ] Steps to repeat it
  - [ ] What happened vs. what should have happened
  - [ ] Screenshot, video, or log
  - [ ] Severity and owner

**Question 9.3: Defect life cycle**

`New → Assigned → In Progress → Fixed → Re-tested → Closed` (or `Reopened`, `Deferred`, `Won't Fix` with a written reason). Change this if your team uses different steps: `<>`

**Defect log (machine-readable)**

| ID | Title | Severity | Related test | Environment | Status | Owner | Date opened | Date closed |
|---|---|---|---|---|---|---|---|---|
| DEF-001 | `<>` | `<>` | `<>` | `<>` | `<>` | `<>` | `<>` | `<>` |

---

## 10. Schedule and Milestones (Development to First 500 Customers)

**Question 10.1: What are the dates for each stage?**

> Example: Stage 3 Integrate | Join the parts together | Main integration test cycle | 2026-11-02 | 2026-11-20 | Priya | `[ ]`.

| Stage | What happens | Integration testing focus | Start | End | Owner | Done |
|---|---|---|---|---|---|---|
| 1. Plan and design | Decide what to build | Identify parts and integration points | `<>` | `<>` | `<>` | `[ ]` |
| 2. Build | Write code (humans and AI agents) | Early connection checks, contract checks | `<>` | `<>` | `<>` | `[ ]` |
| 3. Integrate | Join the parts together | Main integration test cycle | `<>` | `<>` | `<>` | `[ ]` |
| 4. Stabilize | Fix defects, re-test | Regression runs until exit criteria met | `<>` | `<>` | `<>` | `[ ]` |
| 5. Pre-launch | Final checks, launch decision | Full journey checks in pre-production, performance and security | `<>` | `<>` | `<>` | `[ ]` |
| 6. Launch | Product goes live | Safe live smoke checks | `<>` | `<>` | `<>` | `[ ]` |
| 7. First 500 customers | Watch, learn, fix | Live monitoring and fast fixes (see Section 12) | `<>` | `<>` | `<>` | `[ ]` |

**Question 10.2: What could delay us, and what is the backup plan?**

| Risk | How likely (L/M/H) | Impact (L/M/H) | Backup plan | Owner |
|---|---|---|---|---|
| `<e.g., outside service sandbox is unreliable>` | `<>` | `<>` | `<>` | `<>` |
| `<>` | `<>` | `<>` | `<>` | `<>` |

---

## 11. Launch Readiness (Go / No-Go)

**Question 11.1: Answer each line honestly before launch day.**

> Example: "Monitoring and alerts are switched on" | Yes | Alert test sent 2026-12-01, phone buzzed for Priya and Tom (screenshot in the team folder).

| Check | Yes / No | Proof (link or note) |
|---|---|---|
| All exit criteria in Section 8.2 are met | `<>` | `<>` |
| Must-pass journeys passed in pre-production | `<>` | `<>` |
| Performance targets met | `<>` | `<>` |
| Security checks passed | `<>` | `<>` |
| Outside services confirmed ready for real traffic (limits, billing, live keys installed by the right person) | `<>` | `<>` |
| Monitoring and alerts are switched on (Section 12) | `<>` | `<>` |
| Rollback plan written and tested (Question 11.2) | `<>` | `<>` |
| Support team trained and knows who to call | `<>` | `<>` |
| Remaining known problems are listed with owners | `<>` | `<>` |

**Question 11.2: If launch goes wrong, how do we go back?**

| Question | Your answer |
|---|---|
| What triggers a rollback? (use numbers) | `<e.g., error rate above 5% for 10 minutes>` |
| Who decides? | `<>` |
| Exact steps to go back | `<>` |
| How long does it take? | `<>` |
| How do we tell customers? | `<>` |

**Question 11.3: Launch decision**

| Decision | Name | Date | Notes |
|---|---|---|---|
| `<GO / NO-GO / GO with conditions>` | `<>` | `<>` | `<>` |

---

## 12. After Launch: Protecting the First 500 Customers

**Question 12.1: How do we count the first 500 customers?**

- What counts as a "customer"? `<e.g., a person who completed sign-up and used the main feature once>`
- Where is the count visible? `<dashboard/report link>`
- Launch style: `<Invite-only / Waitlist / Gradual rollout (e.g., 10%, 25%, 50%, 100%) / Open to all>`

**Question 12.2: What do we watch live? (Integration health signals)**

> Example: Failed payments | Payments dashboard | Under 2% | Above 2% for 15 minutes | Priya and Tom (phone alert) | Check the payment provider status page, then pause new sign-ups if it is down.

| Signal | Where to see it | Normal range | Alert when | Who is alerted | What they do |
|---|---|---|---|---|---|
| Errors between parts | `<>` | `<>` | `<>` | `<>` | `<>` |
| Slow responses | `<>` | `<>` | `<>` | `<>` | `<>` |
| Failed payments or sign-ups | `<>` | `<>` | `<>` | `<>` | `<>` |
| Outside service outages | `<>` | `<>` | `<>` | `<>` | `<>` |
| Failed or duplicated messages/emails | `<>` | `<>` | `<>` | `<>` | `<>` |
| AI errors, cost, or unsafe answers (if AI used) | `<>` | `<>` | `<>` | `<>` | `<>` |
| Customer complaints that mention "not working" | `<>` | `<>` | `<>` | `<>` | `<>` |

**Question 12.3: Safe live checks (smoke checks) after every release**

> Example: A test account signs in and completes a free action every 15 minutes. It never touches real customer data.

`<Your answer>`

**Question 12.4: Checkpoints along the way**

| Milestone | Date reached | What we review | Decision (continue / slow down / pause) | Owner |
|---|---|---|---|---|
| First 10 customers | `<>` | `<>` | `<>` | `<>` |
| First 50 customers | `<>` | `<>` | `<>` | `<>` |
| First 100 customers | `<>` | `<>` | `<>` | `<>` |
| First 250 customers | `<>` | `<>` | `<>` | `<>` |
| First 500 customers | `<>` | `<>` | `<>` | `<>` |

**Question 12.5: How do customer problems turn into new tests?**

> Example: "Every customer-reported integration bug becomes a new test case within 2 working days."

`<Your answer>`

---

## 13. Reporting and Communication

**Question 13.1: Who gets updates, how often, and in what form?**

| Audience | What they receive | How often | Channel | Sender |
|---|---|---|---|---|
| Team | Test progress, new defects | `<Daily>` | `<>` | `<>` |
| Managers/Owners | Summary and risks | `<Weekly>` | `<>` | `<>` |
| Everyone (at launch) | Go / No-Go result | `<Once>` | `<>` | `<>` |

**Question 13.2: Test summary report (fill at the end of each test cycle)**

| Item | Result |
|---|---|
| Build/version tested | `<>` |
| Test cycle dates | `<>` |
| Tests planned / run / passed / failed / blocked | `<>` |
| Defects found (Critical / High / Medium / Low) | `<>` |
| Defects still open | `<>` |
| Exit criteria met? | `<Yes / No>` |
| Recommendation | `<>` |

---

## 14. Tools and Access

**Question 14.1: What tools do we use?**

| Purpose | Tool name | Link | Who has access | Who to ask for access |
|---|---|---|---|---|
| Test cases and tracking | `<>` | `<>` | `<>` | `<>` |
| Defect tracking | `<>` | `<>` | `<>` | `<>` |
| Automated tests | `<>` | `<>` | `<>` | `<>` |
| Build and release (CI/CD) | `<>` | `<>` | `<>` | `<>` |
| Monitoring and alerts | `<>` | `<>` | `<>` | `<>` |
| Device/browser testing | `<>` | `<>` | `<>` | `<>` |
| Communication | `<>` | `<>` | `<>` | `<>` |

---

## 15. Rules for Keeping This Plan Up to Date

**Question 15.1: When must this document be updated?**

- [ ] A new part or integration point is added
- [ ] An outside service changes or is replaced
- [ ] A Critical defect reaches live customers (add lessons learned)
- [ ] Launch date moves
- [ ] Every `<N>` weeks at minimum

**Question 15.2: Lessons learned (fill after launch and after the first 500 customers)**

| What went well | What went badly | What we will change next time | Owner |
|---|---|---|---|
| `<>` | `<>` | `<>` | `<>` |

---

## 16. Final Self-Check (Before You Share This Document)

- [ ] No `<...>` placeholders remain (all replaced, or marked `N/A` / `UNKNOWN` with a reason)
- [ ] All examples (`> Example:`) are deleted
- [ ] Every integration point (INT-xxx) has at least one test case
- [ ] Every test case has an expected result with a number or a clear, checkable outcome
- [ ] Every exit rule uses a number
- [ ] Every risk and defect has an owner
- [ ] No passwords, keys, or real customer data appear anywhere
- [ ] Someone who did not write this has read it and understood it
- [ ] Sections 6A to 6D are filled (or marked `N/A` with a reason)
- [ ] The matching industry block in Appendix C is filled
- [ ] The Reviewer Checklist (Section 17) has been handed to the reviewer
- [ ] The approver in Section 0 has signed off

---

## 17. Reviewer Checklist (For the Approver, Not the Author)

The reviewer fills this in after the author finishes Section 16. Mark each line **Pass**, **Fix**, or **N/A**.

| # | Check | Pass / Fix / N/A | Reviewer comment |
|---|---|---|---|
| 1 | Every question is answered, or marked `N/A` / `UNKNOWN` with a reason | `<>` | `<>` |
| 2 | Parts and integration points are complete (nothing important missing from Section 2) | `<>` | `<>` |
| 3 | Every High-priority integration point has success, error, and timeout tests | `<>` | `<>` |
| 4 | Exit criteria use numbers and are realistic | `<>` | `<>` |
| 5 | Security and privacy rules match the real data and laws that apply (Section 6A) | `<>` | `<>` |
| 6 | Performance numbers cover 500 customers with a safety margin (Section 6B) | `<>` | `<>` |
| 7 | Contracts and versions are linked and owned (Section 6C) | `<>` | `<>` |
| 8 | AI agent limits and logs are clear (Sections 3.2 and 6D) | `<>` | `<>` |
| 9 | Rollback plan is specific and has an owner (Section 11.2) | `<>` | `<>` |
| 10 | First-500 monitoring has owners, alert limits, and checkpoints (Section 12) | `<>` | `<>` |
| 11 | Industry add-on block in Appendix C is filled if an industry was ticked | `<>` | `<>` |
| 12 | No secrets or real customer data in the file | `<>` | `<>` |
| 13 | A newcomer could follow this plan without asking the author | `<>` | `<>` |

**Reviewer decision:** `<Approved / Approved with changes / Rejected>`  **Name:** `<>`  **Date:** `<>`

---

## Appendix A: Glossary (Plain-Language Words)

| Word | Simple meaning |
|---|---|
| Integration | Two or more parts of the product talking to each other |
| Integration test | A check that the parts work correctly together |
| API | A doorway that lets one program ask another program for something |
| Environment | A separate copy of the product used for a specific purpose (testing, final check, live) |
| Sandbox | A safe pretend version of an outside service used only for testing |
| Staging | A test copy that looks like the real product |
| Production / Live | The real product that real customers use |
| Defect / Bug | Something that does not work as expected |
| Severity | How serious a defect is |
| Regression | Something that used to work and broke after a change |
| Smoke check | A very quick check that the most important things still work |
| Rollback | Going back to the previous working version |
| Entry / Exit criteria | Rules for when to start / when you may stop testing |
| Go / No-Go | The final decision to launch or not |
| Timeout | When one part waits too long for another and gives up |
| Contract | The agreed format of messages between two parts |
| Test data | Fake information used during testing |
| Masking | Hiding or scrambling real data so nobody can identify a person |

## Appendix C: Industry Add-On Blocks (Fill Only the Block That Matches Question 1.5)

### C1. Fintech / Payments

| Question | Your answer |
|---|---|
| What happens if a payment succeeds at the provider but our system never hears about it? | `<>` |
| How do we avoid charging twice if a message is repeated? | `<>` |
| How do we check money records match between us and the provider (reconciliation)? | `<>` |
| Which refunds, disputes, and failed-card cases are tested? | `<>` |
| Which financial rules apply (PCI DSS, local licensing, KYC/AML)? | `<>` |

### C2. Health / Wellness

| Question | Your answer |
|---|---|
| Which health data moves between parts, and who may see it? | `<>` |
| What happens if a reminder, alert, or data sync fails? Could that harm someone? | `<>` |
| Which health rules apply (HIPAA, local rules)? | `<>` |
| Who is told if there is a safety-related failure? | `<>` |

### C3. E-commerce / Marketplace

| Question | Your answer |
|---|---|
| How do stock levels stay correct across store, warehouse, and shipping services? | `<>` |
| What happens if two customers buy the last item at the same time? | `<>` |
| How are taxes, shipping prices, and discounts checked end to end? | `<>` |
| What happens on order cancel, return, and partial refund? | `<>` |

### C4. Education / Kids

| Question | Your answer |
|---|---|
| How is a child's age checked, and what data is blocked for children? | `<>` |
| How are parent permissions passed to every connected part? | `<>` |
| What content filters apply to any AI or user-written content? | `<>` |
| Which rules apply (COPPA, GDPR-K, school privacy rules)? | `<>` |

### C5. Other Industry

| Question | Your answer |
|---|---|
| What is the worst thing that could go wrong for a customer in this industry? | `<>` |
| Which laws or standards apply? | `<>` |
| Which integration points carry the most risk because of this? | `<>` |

---

## Appendix B: Filled-In Mini Example (Delete Before Use)

**Product:** BookNook, a web app where people reserve books at a local library.

| ID | From | To | What travels | Priority |
|---|---|---|---|---|
| INT-001 | Web app | Reservation API | Book ID + member ID | High |
| INT-002 | Reservation API | Database | Reservation record | High |
| INT-003 | Reservation API | Email service | Confirmation email request | Medium |

| Test ID | Steps | Expected result |
|---|---|---|
| INT-001-TC-01 | 1) Log in as test member. 2) Open book "Test Book 1". 3) Press Reserve. | Message "Reserved" appears within 2 seconds. |
| INT-003-TC-02 | 1) Switch email service to "down" in the test environment. 2) Reserve a book. | Reservation is still saved. User sees "Reserved. Your email may be delayed." Failed email is retried later. |

**Exit rule example:** 100% of High tests passed, 0 open Critical or High defects, all journeys passed.

**First-500 example:** Alert if more than 2% of reservations fail in any 15-minute window. A support person reviews every failure the same day.
