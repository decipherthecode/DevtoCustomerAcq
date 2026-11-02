# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What is this?** A Regression Test Plan is your promise to yourself and your team: *"Every time we change the product, we will check that the old stuff still works."* This one file covers the whole journey, from building the product to launch and until your first **500 customers** are using it.

**Who can fill it?** Anyone. If you can answer a question in plain words, you can fill this in. No technical background needed.

## The 6 rules

1. **Go top to bottom.** Do the sections in order. Later sections reuse earlier answers.
2. **Each section has the same 5 parts:**
   - 🎯 **Why this matters**: one sentence on why the section exists.
   - 🟦 **Question**: what we are asking, in plain words.
   - 💡 **Example**: a sample answer for a made-up product ("PetPal", a pet-care app). Copy the *style*, not the words.
   - ✍️ **Your answer**: write here. Replace every `[FILL IN]`.
   - ✅ **Done when**: a quick check that your answer is good enough.
3. **Never leave a blank.** If it does not apply, write `N/A, because ...` and give the reason. If you do not know, write `UNKNOWN, ask <name> by <date>`.
4. **Be specific.** Use numbers, names and dates. Write "login works in under 3 seconds", not "login is fast". Write "Priya Shah", not "the QA team".
5. **No guessing words.** Avoid *probably, maybe, etc., as needed, appropriate, ASAP*. Replace them with a number, a name or a date.
6. **Keep the legend.** `[FILL IN]` = you must answer. `[CHOOSE: A / B]` = pick one and delete the rest. `☐` = tick it (`☑`) when true.

## Quick-start (only 15 minutes?)

Fill these first, in this order: **Sections 1, 3, 7, 12, 13.** Then come back and finish the rest before anything goes to real customers.

## How AI agents help (and where humans stay in charge)

AI agents can draft test cases, run tests, and summarize results. **Humans approve every release.** Section 6 sets the exact rules, and **Appendix A** has copy-and-paste instructions for agents.

## Stuck? Look at the finished example

**Appendix B** is a fully filled sample for a made-up app called PetPal. Peek at it whenever you are unsure what a good answer looks like.

---

# REGRESSION TEST PLAN

## 0. Document Control

🎯 **Why this matters:** Without one named owner, plans go stale and nobody knows which version is the real one.

🟦 **Question:** Who owns this document, and which version is it?

💡 **Example:**

| Field | Value |
|---|---|
| Product name | PetPal |
| Plan version | 1.0 |
| Plan owner | Priya Shah (QA Lead) |
| Last updated | 2026-10-17 |
| Status | Draft |

✍️ **Your answer:**

| Field | Value |
|---|---|
| Product name | [FILL IN] |
| Plan version | [FILL IN] |
| Plan owner (one named person) | [FILL IN] |
| Last updated (YYYY-MM-DD) | [FILL IN] |
| Status | [CHOOSE: Draft / In review / Approved / Retired] |

✅ **Done when:** one real person is named as owner, and the date is filled in.

---

## 1. Product Snapshot

🎯 **Why this matters:** Everything else depends on knowing exactly what we are testing and where it runs.

🟦 **Question:** What is the product, who uses it, and where does it run?

💡 **Example:** "PetPal is a subscription app where pet owners book vets and track vaccines. Users: pet owners (web and phone) and vet clinic staff (web only). Runs on Chrome, Safari, iOS 17+, Android 13+. Payments by Stripe. Emails by SendGrid."

✍️ **Your answer:**

- One-sentence description: [FILL IN]
- Product type: [CHOOSE (can pick both): Web app/SaaS / Mobile app]
- Who uses it (list each type of user): [FILL IN]
- Where it runs (browsers, phone systems, versions): [FILL IN]
- Outside services it depends on (payments, email, login, maps, AI models, etc.): [FILL IN]
- Does it contain AI/LLM features? [CHOOSE: Yes (describe) / No]
- Where is the code and the test code kept? (links): [FILL IN]

✅ **Done when:** a stranger could read this and explain the product back to you.

---

## 2. Purpose and Goals

🎯 **Why this matters:** A goal with a number tells us when we are done, so we neither test forever nor stop too early.

🟦 **Question:** Why are we testing again and again? What does "success" look like?

💡 **Example:** "Goal: no change we ship breaks sign-up, booking, or payment. Success: fewer than 2 customer-reported bugs per 100 customers in the first 500."

✍️ **Your answer:**

- Main goal (one sentence): [FILL IN]
- 3 measurable success targets (use numbers):
  1. [FILL IN]
  2. [FILL IN]
  3. [FILL IN]

✅ **Done when:** every target contains a number or a clear yes/no test.

---

## 3. Scope: What We Test and What We Don't

🎯 **Why this matters:** What is not written as in scope usually does not get tested, and that is where surprises hide.

🟦 **Question:** Which parts of the product are covered by regression testing? Which are not, and why?

💡 **Example:**

| In scope | Out of scope (and why) |
|---|---|
| Sign-up, login, booking, payment, vaccine tracker | Vet clinic admin reports (low usage, tested manually once a month) |
| iOS and Android apps, Chrome, Safari | Internet Explorer (not supported) |

✍️ **Your answer:**

| In scope | Out of scope (and why) |
|---|---|
| [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] |

- Features planned for later that are NOT in this plan yet: [FILL IN]

✅ **Done when:** every out-of-scope row has a "because".

---

## 4. Launch Stages (Development to First 500 Customers)

🎯 **Why this matters:** Your first 500 customers are your most fragile and most valuable users. Stricter rules at each stage protect them while the product grows.

🟦 **Question:** What are the 5 stages, who is using the product in each, and how strict is testing in each?

💡 **Example:**

| # | Stage | Who uses it | Regression run | Strictness |
|---|---|---|---|---|
| 1 | Build | Team only | On every code change | Smoke + changed areas |
| 2 | Pre-launch / Beta | 20 invited testers | Nightly + before each beta build | Full regression |
| 3 | Launch day | Public, first customers | Before release + 1 hour after | Full regression + live checks |
| 4 | First 100 customers | Early customers | Every release | Full regression + customer feedback review |
| 5 | Customers 101 to 500 | Growing base | Every release + weekly health run | Full + performance and security extras |

✍️ **Your answer:**

| # | Stage | Who uses it | Regression run | Strictness |
|---|---|---|---|---|
| 1 | Build | [FILL IN] | [FILL IN] | [FILL IN] |
| 2 | Pre-launch / Beta | [FILL IN] | [FILL IN] | [FILL IN] |
| 3 | Launch day | [FILL IN] | [FILL IN] | [FILL IN] |
| 4 | First 100 customers | [FILL IN] | [FILL IN] | [FILL IN] |
| 5 | Customers 101 to 500 | [FILL IN] | [FILL IN] | [FILL IN] |

- Target date for each stage start: [FILL IN]
- What must be true to move from one stage to the next? [FILL IN]

✅ **Done when:** every stage has a date and a "move on when" rule.

---

## 5. People and Approvers

🎯 **Why this matters:** When something breaks at 2 am, a named person with a backup saves hours.

🟦 **Question:** Who does what? Who has the power to say "ship it" or "stop"?

💡 **Example:**

| Role | Name | Does this | Backup |
|---|---|---|---|
| Plan owner | Priya Shah | Keeps this plan current | Omar Reyes |
| Developer lead | Omar Reyes | Fixes bugs, fixes broken tests | Lena Park |
| QA lead | Priya Shah | Runs/reviews regression | Sam Cole |
| Product owner | Lena Park | Decides what bugs can wait | Priya Shah |
| Release approver (final yes/no) | Lena Park | Signs off the release | Omar Reyes |

✍️ **Your answer:**

| Role | Name | Does this | Backup |
|---|---|---|---|
| Plan owner | [FILL IN] | [FILL IN] | [FILL IN] |
| Developer lead | [FILL IN] | [FILL IN] | [FILL IN] |
| QA lead | [FILL IN] | [FILL IN] | [FILL IN] |
| Product owner | [FILL IN] | [FILL IN] | [FILL IN] |
| Release approver (final yes/no) | [FILL IN] | [FILL IN] | [FILL IN] |
| Support / customer contact | [FILL IN] | [FILL IN] | [FILL IN] |

- If the approver is unreachable for [FILL IN] hours, who decides? [FILL IN]

✅ **Done when:** every role has a real name AND a backup.

---

## 6. AI-Agent Rules (Agents Do the Work, Humans Approve)

🎯 **Why this matters:** Agents are fast but can be confidently wrong. Clear limits keep the speed without losing control.

🟦 **Question:** What can AI agents do on their own, what needs a human, and what is forbidden?

💡 **Example:**

| Task | Agent may do alone? | Human check needed |
|---|---|---|
| Draft new regression test cases | Yes | QA lead reviews before they join the suite |
| Run the test suite | Yes | None |
| Summarize results | Yes | QA lead reads before it is shared |
| Fix a broken test script | Yes, in a branch | Developer approves the merge |
| Mark a bug "won't fix" | **No** | Product owner only |
| Approve a release | **No** | Release approver only |
| Touch real customer data | **No** | Never |

✍️ **Your answer:**

| Task | Agent may do alone? | Human check needed |
|---|---|---|
| Draft new test cases | [CHOOSE: Yes / No] | [FILL IN] |
| Run the test suite | [CHOOSE: Yes / No] | [FILL IN] |
| Summarize results | [CHOOSE: Yes / No] | [FILL IN] |
| Fix a broken test script | [CHOOSE: Yes / No] | [FILL IN] |
| Close or defer a bug | [CHOOSE: Yes / No] | [FILL IN] |
| Approve a release | **No (fixed rule)** | Release approver |
| Access real customer data | **No (fixed rule)** | Never |

- Which AI agents/tools are used (name and version): [FILL IN]
- Where are agent instructions stored? (link): [FILL IN]
- How are agent actions recorded so a human can review them? [FILL IN]
- What happens if an agent gives a result that looks wrong or inconsistent? [FILL IN]
- If the product has AI/LLM features: how do we check answers that change each time (accepted score, sample size, human review rate)? [FILL IN or N/A]

✅ **Done when:** every row is answered and "approve a release" still says human.

---

## 7. What Must Never Break (Critical Features and Risks)

🎯 **Why this matters:** You cannot test everything every time. This list says what to protect first.

🟦 **Question:** If only 5 things could work perfectly, which would they be? What is the worst thing that could go wrong?

💡 **Example:**

| Rank | Feature | If it breaks | Risk level |
|---|---|---|---|
| 1 | Payment | We lose money and trust | Critical |
| 2 | Login | Nobody can use the app | Critical |
| 3 | Book a vet | Core promise fails | High |
| 4 | Vaccine reminders | Pets miss shots | High |
| 5 | Profile photo upload | Annoying, not harmful | Low |

✍️ **Your answer:**

| Rank | Feature | If it breaks | Risk level [Critical/High/Medium/Low] |
|---|---|---|---|
| 1 | [FILL IN] | [FILL IN] | [FILL IN] |
| 2 | [FILL IN] | [FILL IN] | [FILL IN] |
| 3 | [FILL IN] | [FILL IN] | [FILL IN] |
| 4 | [FILL IN] | [FILL IN] | [FILL IN] |
| 5 | [FILL IN] | [FILL IN] | [FILL IN] |

- Rules or laws we must follow (privacy, payments, accessibility, app store rules): [FILL IN]
- Areas that broke before in past releases: [FILL IN]

✅ **Done when:** Critical and High items are tested in *every* release (see Section 9).

---

## 8. Types of Regression Tests

🎯 **Why this matters:** Each test type catches a different kind of problem. Skipping one leaves a blind spot.

🟦 **Question:** For each test type, is it used, what does it check, how often, and who owns it?

💡 **Example:** "Smoke: 10 tests, 5 minutes, checks app opens, login works, one booking can be made. Runs on every build. Owner: Omar."

✍️ **Your answer:**

### 8.1 Smoke and Sanity ("Is the build alive?")
- Use it? [CHOOSE: Yes / No, because ...]
- What it checks (5 to 10 items): [FILL IN]
- Max time allowed: [FILL IN]
- When it runs: [FILL IN]
- Owner: [FILL IN]

### 8.2 Functional and Integration ("Does each feature and each outside service still work?")
- Use it? [CHOOSE: Yes / No, because ...]
- Features covered (link to Section 12 list): [FILL IN]
- Outside services checked (payments, email, login provider, AI model, etc.) and how (real, test mode, or fake): [FILL IN]
- When it runs: [FILL IN]
- Owner: [FILL IN]

### 8.3 Performance ("Is it still fast with real crowds?")
- Use it? [CHOOSE: Yes / No, because ...]
- Pages or actions measured and the speed limit for each (e.g. "login under 3 seconds"): [FILL IN]
- Crowd size to simulate (Stage 3: [FILL IN] users, Stage 5: [FILL IN] users): [FILL IN]
- When it runs: [FILL IN]
- Owner: [FILL IN]

### 8.4 Security ("Can someone get in who should not?")
- Use it? [CHOOSE: Yes / No, because ...]
- What is checked (login, permissions, stored data, payment data, secret keys): [FILL IN]
- Tools used: [FILL IN]
- When it runs: [FILL IN]
- Owner: [FILL IN]

### 8.5 Accessibility ("Can everyone use it?")
- Use it? [CHOOSE: Yes / No, because ...]
- Standard followed [CHOOSE: WCAG 2.2 AA / Other: ___]
- What is checked (screen readers, keyboard-only use, colour contrast, text size): [FILL IN]
- When it runs: [FILL IN]
- Owner: [FILL IN]

### 8.6 Cross-Browser and Cross-Device ("Does it work everywhere our customers are?")
- Browsers and versions: [FILL IN]
- Phones/tablets and OS versions (real devices vs emulators): [FILL IN]
- Screen sizes: [FILL IN]
- Why these and not others (e.g. "covers 90% of our users"): [FILL IN]
- When it runs: [FILL IN]
- Owner: [FILL IN]

### 8.7 Upgrade and Data Migration ("Does an update keep customers' stuff safe?")
- Use it? [CHOOSE: Yes / No, because ...]
- Upgrade paths checked (old version to new version): [FILL IN]
- What data must survive (accounts, purchases, settings): [FILL IN]
- App store checks (review rules, update prompts, forced updates): [FILL IN or N/A]
- When it runs: [FILL IN]
- Owner: [FILL IN]

### 8.8 Compliance and Privacy ("Are we following the rules about people's data and money?")

🎯 **Why this matters:** Breaking privacy, payment or app store rules can get you fined, blocked from the app stores, or lose customers' trust, and a normal bug-hunt will not notice it.

💡 **Example:** "Rules: GDPR (EU customers), CCPA (California), PCI DSS (we never store card numbers; Stripe does), Apple and Google store rules. Every release we test: cookie banner works, 'delete my account' removes data within 30 days, 'download my data' works, logs contain no emails or card data. Rule: 0 failed privacy tests allowed. Evidence saved in the release folder. Approver: Lena Park, with legal advice from our lawyer when a rule changes."

✍️ **Your answer:**

- Which rules apply to us? Tick all that fit: ☐ GDPR (EU/UK people) ☐ CCPA/CPRA (California) ☐ PCI DSS (card payments) ☐ COPPA (children under 13) ☐ HIPAA (health data) ☐ App Store / Google Play policies ☐ AI-specific rules (e.g. EU AI Act) ☐ Other: [FILL IN]
- What personal data do we collect, and where is it stored? [FILL IN]
- Privacy checks run every release (edit the list): ☐ Consent/cookie banner works ☐ "Delete my data" works ☐ "Download my data" works ☐ Marketing opt-out is respected ☐ Logs and error reports contain no personal or payment data ☐ Data is only stored in allowed countries/regions ☐ Other: [FILL IN]
- Payment checks (e.g. we never store full card numbers): [FILL IN]
- Pass rule (example: "0 failed privacy or payment-safety tests"): [FILL IN]
- Where is the proof saved for each release? (link): [FILL IN]
- Who checks the rules when they change, and how often? [FILL IN]
- Who is the person with legal or privacy responsibility? [FILL IN]

*This template is not legal advice. Ask a qualified person which rules apply to you.*

✅ **Done when:** every rule you ticked has at least one check, an owner, and a pass rule.

✅ **Done when (whole Section 8):** every sub-section says Yes with an owner, or says No with a reason.

---

## 9. When Do We Run Tests? (Triggers and Selection)

🎯 **Why this matters:** Tests that never run protect nothing. Triggers make sure checks happen at the right moment.

🟦 **Question:** What events start a regression run, and which tests run for each event?

💡 **Example:**

| Trigger | Tests that run | Time limit |
|---|---|---|
| Code saved/merged | Smoke + tests linked to changed files | 15 minutes |
| Every night | Full functional suite | 2 hours |
| Before each release | Full suite + performance + security + devices | 1 day |
| Hotfix | Smoke + the broken area + all Critical items | 1 hour |
| Outside service update (e.g. payment provider) | Integration tests for that service | 1 hour |

✍️ **Your answer:**

| Trigger | Tests that run | Time limit |
|---|---|---|
| Code saved/merged | [FILL IN] | [FILL IN] |
| Every night | [FILL IN] | [FILL IN] |
| Before each release | [FILL IN] | [FILL IN] |
| Hotfix | [FILL IN] | [FILL IN] |
| Outside service or phone-OS update | [FILL IN] | [FILL IN] |
| Weekly health run (Stages 4 to 5) | [FILL IN] | [FILL IN] |

- How do we pick which tests to run when time is short? (Rule: always Critical, then High, then changed areas.) [FILL IN]
- How do we remove or fix tests that fail randomly ("flaky" tests)? How many reruns allowed before we investigate? [FILL IN]

### 9.1 Outside Changes We Must Watch (Vendors, Platforms and AI Models)

🎯 **Why this matters:** Your product can break even when you change nothing. Payment, login, phone-system and AI-model providers change things on their own schedule.

💡 **Example:**

| Outside party | What we use it for | How we hear about changes | Who watches | How often | Tests we run when it changes | Deadline to be ready |
|---|---|---|---|---|---|---|
| Stripe | Payments | Stripe changelog + email alerts | Omar Reyes | Weekly | REG-002 + all payment tests | 5 working days |
| Apple iOS | iPhone app | iOS beta releases + App Store notices | Sam Cole | Every beta release | Smoke + device tests on the new iOS beta | Before public release of the new iOS |
| Google Play | Android app | Play Console notices (e.g. required target version) | Sam Cole | Weekly | Smoke + upgrade tests | Date set by Google |
| AI model provider | Chat helper | Provider release notes + deprecation emails | Priya Shah | Weekly | AI answer quality checks (Section 6) | Before old model is switched off |

✍️ **Your answer:**

| Outside party | What we use it for | How we hear about changes | Who watches | How often | Tests we run when it changes | Deadline to be ready |
|---|---|---|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

- Do we lock ("pin") the version of each outside service or AI model we use, so it cannot change without us choosing? [CHOOSE: Yes (list them) / No, because ...]
- If an outside service breaks us with no warning, who is told and what is the first action? [FILL IN]
- Who owns the list above and how often is it reviewed? [FILL IN]

✅ **Done when:** every outside service from Section 1 appears in this table.

✅ **Done when (whole Section 9):** each trigger lists tests and a time limit.

---

## 10. Test Environments and Test Data

🎯 **Why this matters:** Tests on messy or real data give false results and can leak customer information.

🟦 **Question:** Where do we test, and what data do we use? (Never real customer data.)

💡 **Example:** "Staging copy of the app at staging.petpal.example. Fake accounts: 50 test users created by a script. Stripe test mode with test card numbers. Reset every night at 2 am."

✍️ **Your answer:**

| Environment | Link | Purpose | Who can use it | Reset how often |
|---|---|---|---|---|
| Development | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Staging / test | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Production (live) | [FILL IN] | Live checks only | [FILL IN] | Never |

- Where does test data come from and how is it created? [FILL IN]
- How do we make sure no real customer data is used? [FILL IN]
- Test accounts (list names only, never passwords): [FILL IN]
- Where are passwords/keys kept safely? [FILL IN]

✅ **Done when:** no password or secret is written anywhere in this file.

---

## 11. Tools and Automation

🎯 **Why this matters:** Automation makes repeating tests cheap, which is the whole point of regression testing.

🟦 **Question:** What tools do we use, and what share of tests is automated?

💡 **Example:** "Playwright for web, Appium for mobile, k6 for speed, GitHub Actions to run on every change, Jira for bugs. Target: 80% of regression tests automated by launch day."

✍️ **Your answer:**

| Purpose | Tool | Owner | Link |
|---|---|---|---|
| Web UI tests | [FILL IN] | [FILL IN] | [FILL IN] |
| Mobile tests | [FILL IN] | [FILL IN] | [FILL IN] |
| API tests | [FILL IN] | [FILL IN] | [FILL IN] |
| Performance tests | [FILL IN] | [FILL IN] | [FILL IN] |
| Security scanning | [FILL IN] | [FILL IN] | [FILL IN] |
| Automatic runs (CI/CD) | [FILL IN] | [FILL IN] | [FILL IN] |
| Bug tracking | [FILL IN] | [FILL IN] | [FILL IN] |
| Test results dashboard | [FILL IN] | [FILL IN] | [FILL IN] |

- Automation target by stage (Stage 2: [FILL IN]%, Stage 3: [FILL IN]%, Stage 5: [FILL IN]%): [FILL IN]
- What stays manual and why: [FILL IN]

✅ **Done when:** every row has a tool name or `N/A, because ...`.

---

## 12. Regression Test Inventory

🎯 **Why this matters:** This list is the actual safety net. The plan is only as good as the tests in it.

🟦 **Question:** What are the actual tests? (This is the list the team runs.)

💡 **Example:**

| ID | Feature | What we check | Type | Priority | Automated? | Last run | Result |
|---|---|---|---|---|---|---|---|
| REG-001 | Login | User with right password gets in | Functional | Critical | Yes | 2026-10-15 | Pass |
| REG-002 | Payment | Test card is charged once, receipt emailed | Integration | Critical | Yes | 2026-10-15 | Pass |
| REG-003 | Booking | Vet slot can be booked and cancelled | Functional | High | Yes | 2026-10-15 | Fail (BUG-88) |

✍️ **Your answer:**

| ID | Feature | What we check | Type | Priority | Automated? | Last run | Result |
|---|---|---|---|---|---|---|---|
| REG-001 | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [Y/N] | [FILL IN] | [FILL IN] |
| REG-002 | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [Y/N] | [FILL IN] | [FILL IN] |
| REG-003 | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [Y/N] | [FILL IN] | [FILL IN] |

*(Add one row per test. For a long list, keep the master list in the link below and keep the Critical and High tests here.)*

- Link to the full test list: [FILL IN]
- When do we add a new test? (Rule suggestion: every bug that reached a customer gets a new test.) [FILL IN]
- When do we retire a test and who approves? [FILL IN]

**Test case writing guide (use for every new test):**
1. *Name it simply:* what is checked.
2. *Steps:* numbered, one action each.
3. *Expected result:* what exactly should happen.
4. *Priority:* Critical, High, Medium, Low (from Section 7).

✅ **Done when:** every Critical item from Section 7 has at least one test here.

---

## 13. Entry Rules, Exit Rules and the Go/No-Go Gate

🎯 **Why this matters:** Numbers agreed in advance stop release-day arguments and pressure-driven guesses.

🟦 **Question:** When can testing start, when is it finished, and what exact numbers decide "ship" or "don't ship"?

💡 **Example:**

**Can start when:** build deployed to staging ☑, smoke tests pass ☑, test data loaded ☑.

**Go only if ALL are true:**

| Rule | Stage 2 Beta | Stage 3 Launch | Stages 4 to 5 |
|---|---|---|---|
| Critical tests pass | 100% | 100% | 100% |
| High tests pass | 95% | 100% | 100% |
| Open Critical (P0) bugs | 0 | 0 | 0 |
| Open High (P1) bugs | ≤ 2 | 0 | 0 |
| Speed limits met | Most | All | All |
| Security scan: serious issues | 0 | 0 | 0 |
| Rollback plan tested | ☑ | ☑ | ☑ |
| Named approver signed | ☑ | ☑ | ☑ |

**Stop immediately if:** payment, login or customer data is broken.

✍️ **Your answer:**

**Testing can start when (tick all that must be true):**
- ☐ Build is on the test environment
- ☐ Smoke tests pass
- ☐ Test data is ready
- ☐ Other: [FILL IN]

**Go only if ALL are true:**

| Rule | Stage 2 Beta | Stage 3 Launch | Stages 4 to 5 |
|---|---|---|---|
| Critical tests pass | [FILL IN]% | [FILL IN]% | [FILL IN]% |
| High tests pass | [FILL IN]% | [FILL IN]% | [FILL IN]% |
| Open Critical (P0) bugs allowed | [FILL IN] | [FILL IN] | [FILL IN] |
| Open High (P1) bugs allowed | [FILL IN] | [FILL IN] | [FILL IN] |
| Speed limits met | [FILL IN] | [FILL IN] | [FILL IN] |
| Security scan: serious issues allowed | [FILL IN] | [FILL IN] | [FILL IN] |
| Accessibility: serious issues allowed | [FILL IN] | [FILL IN] | [FILL IN] |
| Rollback plan tested | [FILL IN] | [FILL IN] | [FILL IN] |
| Named approver signed | [FILL IN] | [FILL IN] | [FILL IN] |

- Who may approve an exception to a rule, and where is it written down? [FILL IN]
- What happens after a "No-Go"? (who is told, how fast, who decides next step) [FILL IN]

✅ **Done when:** every cell is a number or a clear Yes/No, and the AI-agent rule from Section 6 is respected (human approves).

---

## 14. Bug Severity and Defect Workflow

🎯 **Why this matters:** Shared definitions of how bad a bug is keep everything from feeling urgent, so real emergencies get fixed first.

🟦 **Question:** How bad is a bug, who fixes it, and how fast?

💡 **Example:**

| Level | Meaning | Example | Fix within | Who decides |
|---|---|---|---|---|
| P0 Critical | Product unusable, money or data at risk | Payment charges twice | 4 hours | Release approver |
| P1 High | Main feature broken, workaround is hard | Cannot book on iPhone | 2 days | Product owner |
| P2 Medium | Feature partly broken, easy workaround | Wrong date format | Next release | Product owner |
| P3 Low | Cosmetic | Button 2 pixels off | When convenient | QA lead |

**Bug life:** Found, Logged, Confirmed, Assigned, Fixed, Retested, Closed (or Deferred with a reason).

✍️ **Your answer:**

| Level | Meaning | Example from our product | Fix within | Who decides |
|---|---|---|---|---|
| P0 Critical | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| P1 High | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| P2 Medium | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| P3 Low | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

- Every bug report must contain (tick or edit): ☐ Title ☐ Steps to repeat ☐ Expected vs actual result ☐ Screenshot/video ☐ Device/browser/version ☐ Severity ☐ Test ID: [FILL IN]
- How are bugs found by a customer treated differently? [FILL IN]
- How is a fixed bug re-checked (the failed test plus related tests)? [FILL IN]

✅ **Done when:** a new teammate could log a bug correctly using only this section.

---

## 15. Schedule and Effort

🎯 **Why this matters:** A plan that does not fit the calendar gets skipped.

🟦 **Question:** How long does a full regression take, and who is needed?

💡 **Example:** "Full regression: 6 hours automated + 4 hours manual by 2 people. Done by 5 pm the day before release. Release freeze starts 24 hours before launch."

✍️ **Your answer:**

| Activity | Duration | People needed | Deadline rule |
|---|---|---|---|
| Smoke run | [FILL IN] | [FILL IN] | [FILL IN] |
| Full regression run | [FILL IN] | [FILL IN] | [FILL IN] |
| Bug fix and retest round | [FILL IN] | [FILL IN] | [FILL IN] |
| Sign-off meeting | [FILL IN] | [FILL IN] | [FILL IN] |

- Release freeze (no new changes after): [FILL IN]
- Planned release dates for Stages 2 to 5: [FILL IN]

✅ **Done when:** total time fits inside the time between code-freeze and release.

---

## 16. Reporting and Metrics

🎯 **Why this matters:** What we do not measure we cannot improve, and leaders need a quick view of health.

🟦 **Question:** What do we report, to whom, and how often?

💡 **Example:** "After each full run: 1-page summary (pass rate, new bugs, blockers) to the release approver within 1 hour. Weekly dashboard to the whole team."

✍️ **Your answer:**

**After each regression run, the report includes:** ☐ Date and build ☐ Tests run/passed/failed/skipped ☐ New and open bugs by severity ☐ Go/No-Go recommendation ☐ Known risks

- Who receives the report and by when: [FILL IN]
- Where reports are stored (link): [FILL IN]

**Metrics we track (set a target for each):**

| Metric | Target | Where we see it |
|---|---|---|
| Pass rate of regression tests | [FILL IN] | [FILL IN] |
| Bugs that escaped to customers per release | [FILL IN] | [FILL IN] |
| Time to fix P0 / P1 bugs | [FILL IN] | [FILL IN] |
| Percent of tests automated | [FILL IN] | [FILL IN] |
| Flaky test rate | [FILL IN] | [FILL IN] |
| Regression run time | [FILL IN] | [FILL IN] |

✅ **Done when:** every metric has a number target.

---

## 17. Rollback, Hotfix and Incident Plan

🎯 **Why this matters:** Every release can go wrong. A rehearsed way back turns a disaster into a short interruption.

🟦 **Question:** If a release hurts customers, how do we undo it or fix it fast?

💡 **Example:** "Trigger: more than 5% of payments fail or crash rate above 2% within 1 hour of release. Action: approver orders rollback; developer lead runs the rollback script (takes 10 minutes). Customers told by email and in-app banner within 30 minutes."

✍️ **Your answer:**

**When do we roll back? (exact triggers with numbers):** [FILL IN]

| Step | Who | How fast | How |
|---|---|---|---|
| Decide to roll back | [FILL IN] | [FILL IN] | [FILL IN] |
| Run the rollback | [FILL IN] | [FILL IN] | [FILL IN] |
| Check that rollback worked (tests to run) | [FILL IN] | [FILL IN] | [FILL IN] |
| Tell customers | [FILL IN] | [FILL IN] | [FILL IN] |
| Write what happened (post-incident review) | [FILL IN] | [FILL IN] | [FILL IN] |

- Can mobile app releases be rolled back? If not, what is the plan (e.g. server switch, forced update, phased rollout)? [FILL IN]
- Hotfix rule: which tests are the minimum before a hotfix goes live? [FILL IN]
- Can the rollback be done without losing customer data? How is that tested? [FILL IN]

✅ **Done when:** the rollback has been practiced at least once on the test environment (date: [FILL IN]).

---

## 18. Customer Feedback Loop (Launch to 500 Customers)

🎯 **Why this matters:** Real customers find problems tests miss. This loop turns their pain into new tests.

🟦 **Question:** How do we learn from real customers and turn that into better regression tests?

💡 **Example:** "Support tickets and app crash reports are reviewed every morning during the first 2 weeks, then twice a week. Every customer-found bug gets a new regression test within 3 days."

✍️ **Your answer:**

| Stage | Where feedback comes from | Who reviews | How often |
|---|---|---|---|
| 2 Beta | [FILL IN] | [FILL IN] | [FILL IN] |
| 3 Launch day | [FILL IN] | [FILL IN] | [FILL IN] |
| 4 First 100 | [FILL IN] | [FILL IN] | [FILL IN] |
| 5 Customers 101 to 500 | [FILL IN] | [FILL IN] | [FILL IN] |

**Customer health signals we watch (with alarm level):**

| Signal | Normal | Alarm level | Action when alarm |
|---|---|---|---|
| Crash-free sessions | [FILL IN] | [FILL IN] | [FILL IN] |
| Failed sign-ups / payments | [FILL IN] | [FILL IN] | [FILL IN] |
| Support tickets per 100 customers | [FILL IN] | [FILL IN] | [FILL IN] |
| App store / review rating | [FILL IN] | [FILL IN] | [FILL IN] |
| Page speed in real use | [FILL IN] | [FILL IN] | [FILL IN] |

- Customer counter: how do we count customers toward 500, and where is the count shown? [FILL IN]
- When we reach 500 customers, what do we review and decide? [FILL IN]

✅ **Done when:** every customer-found bug has a rule that makes it a new test.

---

## 19. Assumptions, Dependencies and Risks to This Plan

🎯 **Why this matters:** Writing risks down early costs minutes. Finding them late costs launches.

🟦 **Question:** What are we assuming, what do we depend on, and what could make this plan fail?

💡 **Example:**

| Item | Type | If it goes wrong | What we do |
|---|---|---|---|
| Stripe test mode is available | Dependency | Payment tests stop | Use a payment fake and re-test later |
| Only 1 QA person | Risk | Slow regression | AI agent runs nightly; cross-train a developer |

✍️ **Your answer:**

| Item | Type [Assumption/Dependency/Risk] | If it goes wrong | What we do |
|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

✅ **Done when:** every risk has an action.

---

## 20. Sign-Off

🎯 **Why this matters:** Sign-off makes the plan a team agreement, not one person's opinion.

🟦 **Question:** Who agrees that this plan is ready to use?

✍️ **Your answer:**

| Role | Name | Decision [Approved / Needs changes] | Date | Comments |
|---|---|---|---|---|
| Plan owner | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| QA lead | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Developer lead | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Product owner | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Release approver | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

✅ **Done when:** every row says Approved.

---

## 21. Change History

🎯 **Why this matters:** Plans change. A history shows why, and prevents re-arguing old decisions.

🟦 **Question:** What changed in this plan and when?

💡 **Example:** `1.1 | 2026-11-03 | Omar Reyes | Added Android 14 to device list`

✍️ **Your answer:**

| Version | Date | Who | What changed and why |
|---|---|---|---|
| 1.0 | [FILL IN] | [FILL IN] | First version |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**Review rhythm:** This plan is reviewed [CHOOSE: before each stage change / monthly / after each incident], and always after any rollback.

---

## 22. Glossary (Plain-English Words)

🎯 **Why this matters:** Shared words prevent misunderstandings between developers, testers and non-technical people.

| Word | What it means |
|---|---|
| **Regression** | Something that used to work and now is broken because of a new change |
| **Regression testing** | Re-checking old features after every change to catch regressions |
| **Smoke test** | A very quick check that the product turns on and the main things work |
| **Sanity test** | A quick check that a specific fix or change works |
| **Test case** | One check written as steps plus an expected result |
| **Test suite** | A group of test cases run together |
| **Automated test** | A test a computer runs by itself |
| **Manual test** | A test a person does by hand |
| **Flaky test** | A test that sometimes passes and sometimes fails for no clear reason |
| **Environment** | A copy of the product used for a purpose (building, testing, live) |
| **Staging** | The practice copy that looks like the real product |
| **Production / Live** | The real product that real customers use |
| **Bug / Defect** | A mistake in the product |
| **P0 to P3** | Bug seriousness levels (P0 = worst) |
| **Go / No-Go** | The final yes or no on releasing |
| **Rollback** | Going back to the last good version |
| **Hotfix** | A very fast fix for a serious problem |
| **Integration** | Our product talking to another service (payments, email, etc.) |
| **CI/CD** | A system that builds and tests automatically each time code changes |
| **Entry / Exit criteria** | Rules for when testing may start / may stop |
| **Accessibility** | Making the product usable by people with different abilities |
| **WCAG** | The international rulebook for accessibility |
| **AI agent** | A computer program using AI that can do tasks (like running tests) with limited human help |
| **Escaped bug** | A bug a customer found before we did |
| **Vendor / Third party** | An outside company whose service our product uses (payments, email, AI models, app stores) |
| **Pinning a version** | Locking an outside service or AI model to one version so it cannot change without us choosing |
| **Model drift** | An AI model giving different or worse answers over time or after an update |
| **GDPR / CCPA** | Privacy laws for people in the EU/UK and California |
| **PCI DSS** | The security rulebook for handling card payments |
| **Evidence** | Saved proof (reports, screenshots, logs) that a check was done |
| **Prompt** | The written instruction given to an AI agent |

---

## 23. Final Checklist (Tick Everything Before Using This Plan)

🎯 **Why this matters:** A last check catches forgotten blanks before the plan is used.

- ☐ No `[FILL IN]` or `[CHOOSE]` left in the document
- ☐ Every name is a real person with a backup
- ☐ Every target has a number or a clear Yes/No
- ☐ Every Critical feature (Section 7) has a test (Section 12)
- ☐ Go/No-Go numbers are set for every stage (Section 13)
- ☐ Rollback has been practiced (Section 17)
- ☐ No passwords, keys or real customer data are written in this file
- ☐ AI agents cannot approve a release or access real customer data (Section 6)
- ☐ Privacy and payment rules have checks, owners and pass rules (Section 8.8)
- ☐ Every outside service is on the watch list (Section 9.1)
- ☐ All approvers signed (Section 20)

---

# APPENDIX A: AI AGENT PROMPT LIBRARY (COPY, PASTE, FILL)

🎯 **Why this matters:** Good instructions make agents repeatable. Anyone on any of your projects gets the same quality of help.

**How to use:**
1. Copy the **Safety Block (A.1)** and paste it at the top of every prompt.
2. Copy the prompt you need (A.2 to A.10).
3. Replace every `{{double-brace item}}` with your own words or links.
4. Never paste passwords, keys or real customer data into any prompt.
5. A human reads the result before anyone acts on it (Section 6).

### A.1 Safety Block (paste at the top of every prompt)

```text
You are helping with regression testing for {{product name}}.
Follow these rules at all times:
1. You may draft, run and summarize tests. You may NOT approve a release, close or defer a bug, or change the Go/No-Go rules.
2. Never use, request or output real customer data, passwords, API keys or secrets. Use only the test data described in the plan.
3. Only act in the environments allowed in the plan: {{allowed environments}}. Never act on production unless the task says "live check" and a named human has approved it.
4. If something is unclear, missing or looks wrong, stop and list your questions. Do not guess.
5. Show your evidence: test IDs, links, logs or screenshots. Say "not verified" for anything you did not actually run.
6. Keep a log of every action you took so a human can review it.
```

### A.2 Draft new test cases for a feature

```text
Feature: {{feature name and short description}}
Who uses it: {{user types}}
Priority from the plan: {{Critical / High / Medium / Low}}
Platforms: {{browsers, phones, OS versions}}

Write regression test cases. For each one give:
- ID (continue from {{last ID}}), short name, priority
- Numbered steps (one action per step)
- Expected result (exact and checkable)
- Test data needed (fake data only)
- Whether it can be automated (Yes/No, and why)
Include: the normal path, at least 3 failure cases (wrong input, no internet, slow response), and one check for each rule in Section 8.8 that touches this feature.
Do not duplicate existing tests: {{link to the test list}}.
Output as a table I can paste into Section 12.
```

### A.3 Run the suite and summarize

```text
Run this suite: {{suite name or link}} on build {{build number}} in {{environment}}.
Then report:
1. Totals: run / passed / failed / skipped
2. Every failed test: ID, name, one-line reason, link to log or screenshot
3. Pass rates for Critical and High tests compared with the Go/No-Go rules in Section 13
4. Anything that ran slower than its speed limit
5. Anything you could not run, and why
End with "Evidence complete: Yes/No". Do not recommend release; the human approver decides.
```

### A.4 Triage failed tests (real bug, flaky test, or environment problem?)

```text
These tests failed: {{list of IDs and logs}}.
Rerun each failed test up to {{number from Section 9}} times.
For each one, classify as:
- REAL BUG (fails every time, with a clear cause)
- FLAKY (passes sometimes)
- ENVIRONMENT (service down, bad data, network)
- TEST IS OUT OF DATE (feature changed on purpose)
Give your evidence and your confidence (High/Medium/Low) for each. Do not delete or edit any test. Suggest the next step and who should do it.
```

### A.5 Write a bug report

```text
Failed test: {{ID}}. Evidence: {{logs, screenshot links}}.
Write a bug report with: title, steps to repeat, expected vs actual result, device/browser/version, build number, test data used, severity suggestion (P0 to P3 using Section 14) with a one-sentence reason, and the affected Critical feature from Section 7 if any.
Mark the severity as "suggested". A human sets the final severity.
```

### A.6 Prepare the Go/No-Go evidence pack (recommend only)

```text
Prepare the evidence pack for releasing {{version}} at Stage {{stage number}}.
Compare the real numbers with the Go/No-Go table in Section 13:
{{paste the filled Stage table}}
Show each rule as MET / NOT MET / NOT VERIFIED with a link to evidence.
Include: open bugs by severity, Section 8.8 compliance results, outside changes from Section 9.1, rollback readiness (Section 17), and known risks.
Finish with a plain recommendation ("meets all rules" or "does not meet: <list>"). Do NOT say "approved". The release approver {{name}} decides.
```

### A.7 Turn a customer-found bug into a regression test

```text
A customer found this bug: {{description, ticket link}}.
1. Write the exact steps that repeat it, using only fake data.
2. Write a regression test case (steps and expected result) in the Section 12 format.
3. Say which Critical or High feature in Section 7 it touches.
4. Say why our tests missed it and what other nearby area might have the same problem.
5. Suggest where this test should run (smoke, nightly or release).
```

### A.8 Check the impact of an outside change (vendor, phone OS, AI model)

```text
Outside change: {{party and what changed, with link to notes}}.
Using Sections 1, 7, 9.1 and 12, list:
- Which features of ours could be affected, ranked by risk
- Which existing tests to run (IDs)
- Which new tests are needed
- The deadline from Section 9.1 and what happens if we miss it
- Questions you cannot answer from the release notes
Do not assume what the notes do not say. Mark guesses as "guess".
```

### A.9 Weekly customer-health summary (Stages 4 and 5)

```text
Period: {{dates}}. Customers so far: {{number}} of 500.
Using the health signals and alarm levels in Section 18, summarize:
- Each signal: value, normal, alarm level, status (OK / WATCH / ALARM)
- New customer-reported bugs and whether each has a new regression test
- Trends compared with last week
- The top 3 things the team should do this week
Do not contact customers. Flag anything that needs a human decision.
```

### A.10 Check this plan for gaps (before sign-off)

```text
Read the Regression Test Plan below and check it against the Final Checklist (Section 23).
List: every remaining [FILL IN] or [CHOOSE], every vague word (probably, maybe, ASAP, etc.), every missing name, number or date, every Critical feature in Section 7 with no test in Section 12, and any place where an AI agent is allowed to approve a release or touch real customer data.
Do not fix anything. Give a numbered list of problems with the section number for each.
{{paste the plan}}
```

---

# APPENDIX B: FILLED SAMPLE (FICTIONAL PRODUCT "PETPAL")

🎯 **Why this matters:** A finished example shows beginners what "good enough" looks like. All names, numbers and links are made up. Copy the style, not the content.

| Section | PetPal's filled answer |
|---|---|
| **0 Document control** | Product: PetPal. Version 1.0. Owner: Priya Shah. Updated 2026-10-17. Status: In review. |
| **1 Product snapshot** | Subscription app where pet owners book vets and track vaccines. Users: pet owners (web, iOS, Android) and clinic staff (web). Runs on Chrome and Safari (latest 2 versions), iOS 17+, Android 13+. Outside services: Stripe (payments), SendGrid (email), Auth0 (login), an AI model for the symptom helper. AI feature: Yes (symptom helper). Code: github.example/petpal. |
| **2 Goals** | Goal: no release breaks sign-up, booking or payment. Targets: (1) fewer than 2 customer-reported bugs per 100 customers; (2) 100% Critical tests pass before every release; (3) rollback done in under 15 minutes. |
| **3 Scope** | In: sign-up, login, booking, payment, vaccine reminders, symptom helper, iOS/Android/web. Out: clinic admin reports (low use, checked by hand monthly), Internet Explorer (unsupported), Windows Phone (unsupported). Later: video calls with vets. |
| **4 Stages** | 1 Build (team, every code change, smoke + changed areas) · 2 Beta (20 testers, nightly, full) · 3 Launch day (public, before and 1 hour after release, full + live checks) · 4 First 100 (every release, full + feedback review) · 5 Customers 101 to 500 (every release + weekly health run, full + performance and security extras). Move on when Go rules (Sec. 13) are met and no P0 bug has been open for 7 days. |
| **5 People** | Owner/QA lead: Priya Shah (backup Sam Cole). Dev lead: Omar Reyes (backup Lena Park). Product owner and release approver: Lena Park (backup Omar Reyes). Support: Dana Wu (backup Sam Cole). If approver unreachable for 4 hours: Omar Reyes decides for hotfixes only. |
| **6 AI-agent rules** | Agents draft tests (QA lead reviews), run suites (no review), summarize (QA lead reads first), fix broken test scripts in a branch (Omar approves). Agents never approve releases, close bugs, or touch real customer data. Agent log stored in /qa/agent-logs. Wrong-looking result: rerun once, then Priya reviews. Symptom helper: 200 sample questions per release, at least 95% pass the safety checklist, 10% reviewed by a human. |
| **7 Never break** | 1 Payment (Critical) · 2 Login (Critical) · 3 Booking (High) · 4 Vaccine reminders (High) · 5 Photo upload (Low). Rules: GDPR, CCPA, PCI DSS, Apple/Google policies. Broke before: double charge in v0.9. |
| **8 Test types** | Smoke: 10 tests, 5 minutes, every build, Omar. Functional/integration: REG list, every night, Priya. Performance: login under 3 s, booking page under 2 s, 500 simulated users at Stage 5, before each release, Omar. Security: scan + permission checks, before each release, Omar. Accessibility: WCAG 2.2 AA, before each release, Sam. Devices: 3 browsers, 6 phones (covers about 90% of expected users), before each release, Sam. Upgrade: v(n-1) to v(n) keeps accounts and bookings, before each app release, Priya. Compliance: cookie banner, delete/download my data, no personal data in logs, 0 failed allowed, proof in the release folder, Lena approves. |
| **9 Triggers** | Code merged: smoke + related tests (15 min) · Nightly: full functional (2 h) · Release: everything (1 day) · Hotfix: smoke + broken area + all Critical (1 h) · Outside update: related integration tests (1 h) · Weekly health run: smoke + payment + login. Short on time: Critical, then High, then changed areas. Flaky: rerun up to 3 times, then Priya investigates within 2 days. |
| **9.1 Outside changes** | Stripe (Omar, weekly, payment tests, 5 working days) · Apple iOS (Sam, every beta, smoke + devices) · Google Play (Sam, weekly, smoke + upgrade) · AI provider (Priya, weekly, symptom helper checks). Versions pinned: Stripe API and the AI model. Surprise break: Omar paged, Priya told, first action is feature flag off. |
| **10 Environments** | Dev (developers, resets on demand) · Staging at staging.petpal.example (QA, resets nightly 2 am) · Production (live checks only). Test data: 50 fake users made by a script. Stripe test mode. Keys held in the company password manager. |
| **11 Tools** | Playwright (web), Appium (mobile), Postman (API), k6 (performance), OWASP ZAP (security), GitHub Actions (CI/CD), Jira (bugs), Grafana (dashboard). Automation: 60% Stage 2, 80% Stage 3, 90% Stage 5. Manual: first-time visual checks and screen-reader review. |
| **12 Inventory** | REG-001 Login (Critical, auto) · REG-002 Payment (Critical, auto) · REG-003 Booking (High, auto) · REG-004 Vaccine reminder email (High, auto) · REG-005 Delete my data (Critical, auto). Full list in Jira. Rule: every customer-found bug gets a test within 3 days. |
| **13 Go/No-Go** | Critical pass 100% at every stage · High pass 95% (Stage 2) then 100% · Open P0: 0 · Open P1: at most 2 (Stage 2), then 0 · Speed limits: all met from Stage 3 · Serious security or accessibility issues: 0 · Rollback tested · Lena signs. Exceptions: Lena only, written in the release ticket. No-Go: Priya tells the team within 1 hour, Omar proposes a fix plan the same day. |
| **14 Severity** | P0 = payment or data harm, fix in 4 hours (Lena decides) · P1 = main feature broken, fix in 2 days · P2 = partial problem, next release · P3 = cosmetic, when convenient. Customer-found bugs start one level higher than they would otherwise. |
| **15 Schedule** | Full run: 6 h automated + 4 h manual (2 people). Freeze 24 h before release. Sign-off meeting 30 minutes at 4 pm the day before. Releases: Beta 2026-11-15, Launch 2026-12-10, then every 2 weeks. |
| **16 Reporting** | One-page report within 1 hour of each full run to Lena. Weekly dashboard in Grafana. Targets: pass rate 98%, escaped bugs under 2 per 100 customers, P0 fixed within 4 h, flaky rate under 2%. |
| **17 Rollback** | Trigger: more than 5% payments fail or crash-free sessions below 98% within 1 hour. Lena orders, Omar runs script (10 min), Priya runs smoke + payment tests, Dana emails customers within 30 minutes, review within 3 days. Mobile: phased rollout at 10% then 50% then 100%, and server switch ready. Rehearsed on 2026-11-20. |
| **18 Feedback loop** | Beta: tester form, daily. Launch: tickets and crash reports, every morning for 2 weeks. First 100: twice weekly. 101 to 500: weekly. Alarms: crash-free below 98%, failed payments above 2%, tickets above 10 per 100 customers. The count of paying accounts in Grafana is the customer counter. At 500: review all escaped bugs and re-rank Section 7. |
| **19 Risks** | One QA person: AI agent runs nightly, Omar cross-trained. Stripe test mode downtime: use payment fake and rerun later. App store review delay: submit 7 days before target date. |
| **20 Sign-off** | All five roles signed on 2026-10-30. |
| **21 Change history** | 1.0 first version (Priya, 2026-10-17). 1.1 added Android 14 (Omar, 2026-11-03). Reviewed before every stage change. |

---

**Congratulations. Your Regression Test Plan is ready. Review it before every stage change, and update it after every rollback.**
