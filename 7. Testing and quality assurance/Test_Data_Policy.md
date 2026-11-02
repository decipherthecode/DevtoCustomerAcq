# Test Data Policy — [PROJECT NAME]

> **Template version:** 1.0 | **Template date:** 2026-10-17
> **Covers:** AI-Driven Development Life Cycle, from the first line of code to the first 500 customers.
> **Location:** Testing and quality assurance / Test_Data_Policy.md

---

# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

## What is this document?
"Test data" is the information (names, emails, orders, payments, photos, etc.) we put into our product to check that it works. This document answers one big question:

> **What data are we allowed to use for testing, where, who can touch it, and what happens to it afterwards?**

## Who fills it in?
The Project Owner fills in the blanks. An engineer or QA person reviews the technical parts. If you are unsure, write `UNSURE` and ask the Reviewer (see Part 13). Never guess.

## The 7 simple rules for filling it in
1. **Answer every question.** If something does not apply, write `N/A — because [short reason]`. Never leave a blank.
2. **Use simple words.** Pretend you are explaining to a 10-year-old. Short sentences are good.
3. **Look at the *Example* under each question.** Copy its style, not its content.
4. **Tick boxes like this:** `[x]` = yes, `[ ]` = no.
5. **Never write real secrets here.** No real passwords, API keys, card numbers, or customer data. Describe *where* they live, not *what* they are.
6. **Every rule needs a name.** Wherever it says "Owner", write a real person or role, not "the team".
7. **When done, complete Part 15 (Readiness Checklist).** If any item is `[ ]`, the document is not finished.

## Colour-free status words used in this document
| Word | Meaning |
|---|---|
| **MUST** | Required. No exceptions without written approval. |
| **MUST NOT** | Forbidden. No exceptions without written approval. |
| **SHOULD** | Strongly recommended. Explain if you skip it. |
| **MAY** | Optional. |

## How to know you are done
- [ ] Every question has an answer or `N/A — reason`
- [ ] No `[PLACEHOLDER]` text is left
- [ ] Every Owner is a named person or role
- [ ] Part 15 checklist is fully ticked
- [ ] Reviewer has signed Part 13

## Tips for using the same template in 100s of projects
- Copy this file into each new project. Rename the title. Do **not** edit the "How to fill" section.
- Items marked **(COMPANY DEFAULT)** can be filled once and reused. Keep a master copy.
- Keep one version history entry per change (bottom of document).

---

# PART 0 — DOCUMENT CONTROL

**Q0.1 What is the project called?**
*Example:* `PetPal — dog walking app`
**Your answer:** `[PROJECT NAME]`

**Q0.2 Who owns this policy (one named person)?**
*Example:* `Maria Lopez, Product Owner`
**Your answer:** `[OWNER]`

**Q0.3 Who reviews it (one named person who did not write it)?**
*Example:* `Sam Chen, QA Lead`
**Your answer:** `[REVIEWER]`

**Q0.4 Which date was it last reviewed, and when is the next review?**
*Example:* `Last: 2026-10-17 | Next: 2027-01-17 (every 3 months, and always before launch)`
**Your answer:** `Last: [DATE] | Next: [DATE]`

**Q0.5 Which product stage are we in right now?**
- [ ] Idea / Planning
- [ ] Building (development)
- [ ] Testing
- [ ] Pre-launch
- [ ] Launched, customers 1–500
- [ ] After 500 customers

---

# PART 1 — THE BIG PICTURE

**Q1.1 In one or two sentences, what does the product do?**
*Example:* `PetPal lets dog owners book walkers and pay in the app.`
**Your answer:** `[ANSWER]`

**Q1.2 Why do we need test data?** (tick all that apply)
- [ ] To check features work
- [ ] To check the product is fast enough with many users
- [ ] To check security
- [ ] To train or evaluate an AI / LLM feature
- [ ] To reproduce a bug a customer reported
- [ ] Other: `[ANSWER]`

**Q1.3 What is the golden rule for this project?**
*Example (COMPANY DEFAULT):* `Real customer data is never used for testing unless this document says so, in writing, with a named approver.`
**Your answer:** `[ANSWER]`

**Q1.4 What does "done well" look like?**
*Example:* `Nobody's real information ever appears in a test, a log, a screenshot, or an AI prompt.`
**Your answer:** `[ANSWER]`

---

# PART 2 — WHAT KIND OF DATA DO WE HAVE?

## 2A. The four data kinds

| Kind | Plain meaning | Risk |
|---|---|---|
| **Synthetic (fake)** | Made up by us or a tool. Nobody is real. | Lowest |
| **Masked / anonymised** | Real data with names and details scrambled or removed so nobody can be identified. | Medium (can fail if done badly) |
| **Real customer data** | Actual information from actual people. | High |
| **Special sensitive data** | Payments, health, children's data, government IDs, biometrics, precise location. | Highest |

**Q2.1 Which kinds will this project use?**
- [ ] Synthetic (fake)
- [ ] Masked / anonymised
- [ ] Real customer data
- [ ] Special sensitive data

**Q2.2 For each kind ticked, why do we need it?**
*Example:* `Synthetic: day-to-day testing. Masked: performance testing with realistic volume. Real: never. Sensitive: never, we use the payment provider's test cards.`
**Your answer:** `[ANSWER]`

## 2B. List the data fields in our product

**Q2.3 Fill in this table for every type of data the product stores.** Add rows as needed.

| Data field | Example value (FAKE only!) | Sensitivity (Low / Medium / High / Special) | Allowed in tests as | Owner |
|---|---|---|---|---|
| Name | `Alex Example` | Medium | Synthetic only | `[OWNER]` |
| Email | `alex@example.test` | Medium | Synthetic only | `[OWNER]` |
| Phone | `+1-555-0100` | Medium | Synthetic only | `[OWNER]` |
| Home address | `1 Test Street, Sampletown` | High | Synthetic only | `[OWNER]` |
| Password | `(never stored in plain text)` | Special | Test accounts only | `[OWNER]` |
| Payment card | `4242 4242 4242 4242 (provider test card)` | Special | Provider test cards only | `[OWNER]` |
| Health info | `[ANSWER]` | Special | `[ANSWER]` | `[OWNER]` |
| Children's info | `[ANSWER]` | Special | `[ANSWER]` | `[OWNER]` |
| Photos / files | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[OWNER]` |
| Location | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[OWNER]` |
| `[ADD MORE]` | | | | |

**Q2.4 Safe fake values.** Which "safe fake" patterns will everyone use?
*Example (COMPANY DEFAULT):* Emails end in `@example.test` or `@example.com`. Phones use `555-01xx`. Cards use the payment provider's published test numbers only.
**Your answer:** `[ANSWER]`

---

# PART 3 — WHERE TEST DATA LIVES (ENVIRONMENTS) AND WHEN (STAGES)

## 3A. Environments

**Q3.1 Name each place the product runs.**

| Environment | What it is | Who can access | Real data allowed? |
|---|---|---|---|
| **Local** | A developer's own computer | Developer only | MUST NOT |
| **Dev** | Shared place for building | Engineers | MUST NOT |
| **Test / CI** | Automatic checks that run on every change | Engineers + automation | MUST NOT |
| **Staging** | Copy of production for final checks | Engineers + QA | `[ANSWER — usually MUST NOT]` |
| **Production** | The real product customers use | Very few named people | Yes (it is real) |

*Example change:* `Staging: masked data only, refreshed monthly.`
**Your answer (edit the table above if yours differ):** `[ANSWER]`

## 3B. The Stage × Environment Rules Matrix

**Q3.2 For each stage, which data is allowed in which environment?** Write one of: `Synthetic`, `Masked`, `Real (approved)`, `None`.

| Stage | Local | Dev | Test / CI | Staging | Production |
|---|---|---|---|---|---|
| **1. Idea / Planning** | Synthetic | Synthetic | Synthetic | — | — |
| **2. Building** | Synthetic | Synthetic | Synthetic | Synthetic | — |
| **3. Testing / QA** | Synthetic | Synthetic | Synthetic | Synthetic or Masked | — |
| **4. Pre-launch** | Synthetic | Synthetic | Synthetic | Masked | Test accounts only |
| **5. Launch day** | Synthetic | Synthetic | Synthetic | Masked | Real customers, test accounts clearly labelled |
| **6. Customers 1–100** | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` |
| **7. Customers 101–500** | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` |
| **8. After 500** | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` |

**Q3.3 What event moves us from one stage to the next, and who says "go"?**
*Example:* `Stage 3 → 4 happens when all critical bugs are fixed. QA Lead says go.`

| Move | Trigger | Person who approves |
|---|---|---|
| 1 → 2 | `[ANSWER]` | `[NAME]` |
| 2 → 3 | `[ANSWER]` | `[NAME]` |
| 3 → 4 | `[ANSWER]` | `[NAME]` |
| 4 → 5 | `[ANSWER]` | `[NAME]` |
| 5 → 6 | `[ANSWER]` | `[NAME]` |
| 6 → 7 | `[ANSWER]` | `[NAME]` |
| 7 → 8 | `[ANSWER]` | `[NAME]` |

---

# PART 4 — HOW WE GET TEST DATA

## 4A. Synthetic (fake) data

**Q4.1 What tool or method creates fake data?**
*Example:* `A script using the Faker library, plus a "seed file" in /tests/data/seed.`
**Your answer:** `[ANSWER]`

**Q4.2 Is fake data repeatable (same result each time) or random?**
- [ ] Repeatable (uses a fixed "seed" number) — recommended for automated tests
- [ ] Random
- [ ] Both: `[ANSWER]`

**Q4.3 Does fake data cover tricky cases?** (tick all you will include)
- [ ] Very long names / very short names
- [ ] Special characters (é, ñ, 中文, emoji)
- [ ] Empty fields
- [ ] Dates in the past / future / leap day
- [ ] Huge numbers / zero / negative numbers
- [ ] Different countries, currencies, time zones
- [ ] Attack-style text (e.g. `<script>`, `' OR 1=1`) for security tests
- [ ] Other: `[ANSWER]`

**Q4.4 Where is the fake-data generator stored and who maintains it?**
**Your answer:** `Location: [PATH/LINK] | Owner: [NAME]`

## 4B. Masked / anonymised data

**Q4.5 Will we copy anything from real data? If no, write `N/A — we never copy production data` and skip to 4C.**
**Your answer:** `[ANSWER]`

**Q4.6 If yes, which method hides the real information?** (tick all)
- [ ] **Replace** (swap real name for a fake name)
- [ ] **Shuffle** (mix values between rows)
- [ ] **Scramble / hash** (turn into unreadable code)
- [ ] **Remove** (delete the field)
- [ ] **Generalise** (exact age 34 → age group 30–39)
- [ ] **Tokenise** (swap for a placeholder with a locked key elsewhere)
- [ ] Other: `[ANSWER]`

**Q4.7 How do we PROVE masking worked before anyone uses the data?**
*Example:* `An automatic scan checks for real emails, phones and card patterns. QA Lead signs off. Result saved in the test report.`
**Your answer:** `[ANSWER]`

**Q4.8 Can a person be re-identified by combining fields (e.g. birthday + postcode + job)?**
- [ ] We checked and the risk is low
- [ ] We have not checked yet (MUST be done before use)
**How we checked:** `[ANSWER]`

**Q4.9 Where does masking happen?**
*Example:* `Inside production's secure zone, BEFORE the data is copied out. Never after.`
**Your answer:** `[ANSWER]`

## 4C. Real customer data

**Q4.10 Is real customer data EVER used for testing?**
- [ ] No, never (recommended)
- [ ] Yes, but only in the exceptions listed below

**Q4.11 If yes, list every exception.**

| Reason | Who approved | Date | Data allowed | Where | How long | How deleted |
|---|---|---|---|---|---|---|
| `[ANSWER]` | `[NAME]` | `[DATE]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` | `[ANSWER]` |

**Q4.12 Did customers agree to this use?**
*Example:* `N/A — never used.` or `Terms of Service section 6 + privacy notice updated on 2026-09-01.`
**Your answer:** `[ANSWER]`

## 4D. Test accounts in production (for launch and early customers)

**Q4.13 Will we use test accounts inside the live product?**
- [ ] No
- [ ] Yes. Rules below:

**Q4.14 How are test accounts labelled so nobody confuses them with real customers?**
*Example:* `Email ends with +test@ourcompany.com, and the account has flag is_test = true. They are excluded from all customer counts and reports.`
**Your answer:** `[ANSWER]`

**Q4.15 Who can create and delete test accounts, and how are they removed afterwards?**
**Your answer:** `[ANSWER]`

---

# PART 5 — SPECIAL SENSITIVE DATA (EXTRA CARE)

> If a category does not apply, write `N/A — we do not handle this`.

## 5A. Payments

**Q5.1 Which payment provider do we use, and do we use its test mode?**
*Example:* `Stripe. Test mode only for all non-production use.`
**Your answer:** `[ANSWER]`

**Q5.2 Statements to confirm:**
- [ ] Real card numbers MUST NOT appear in code, tests, logs, screenshots, tickets, chats or AI prompts.
- [ ] Only the provider's published test cards are used.
- [ ] Test and live keys are stored separately and never shared.

## 5B. Health information

**Q5.3 Do we handle health or medical information?**
- [ ] No
- [ ] Yes. How is test health data created? `[ANSWER]`

## 5C. Children's data

**Q5.4 Could anyone under 18 (or under 13 / 16, depending on your country) use the product?**
- [ ] No
- [ ] Yes. What is the rule for test data about children? `[ANSWER]`

*Example rule:* `No real child data in any test, ever. Synthetic children profiles only.`

## 5D. Other special categories

**Q5.5 Do we handle any of these?** (tick all)
- [ ] Government ID numbers
- [ ] Biometrics (fingerprints, face, voice)
- [ ] Precise location
- [ ] Race, religion, politics, sexual orientation
- [ ] Bank account details
- [ ] Private messages or call recordings
- [ ] Photos or videos of people
**Rule for each ticked item:** `[ANSWER]`

---

# PART 6 — LAWS AND STANDARDS

> Tick only what applies. You may need help from a lawyer or privacy expert. Write `UNSURE` if needed. This section is guidance, not legal advice.

**Q6.1 In which countries or regions do our customers live?**
*Example:* `USA, UK, EU`
**Your answer:** `[ANSWER]`

| Rule / standard | Plain meaning | Applies? | What it means for test data | Owner |
|---|---|---|---|---|
| **GDPR** (EU/UK privacy law) | Protect personal data of people in the EU/UK; use only what you need; delete when done; report leaks quickly. | `[ ] Yes [ ] No [ ] Unsure` | Test data must be fake or properly anonymised; masked data that can be re-identified is still personal data. | `[NAME]` |
| **HIPAA** (US health data) | Protect health information tied to a person. | `[ ] Yes [ ] No [ ] Unsure` | No real patient data in test; use synthetic health records. | `[NAME]` |
| **PCI-DSS** (card payments) | Strict rules for storing or handling card data. | `[ ] Yes [ ] No [ ] Unsure` | Never use real card numbers in testing; use provider test cards. | `[NAME]` |
| **SOC 2 / ISO 27001** (security audits) | Prove to customers and auditors that we control access and data. | `[ ] Yes [ ] No [ ] Unsure` | Keep evidence: who accessed what, when, and approvals. | `[NAME]` |
| Other (e.g. CCPA/CPRA, LGPD, PIPEDA) | `[ANSWER]` | `[ ]` | `[ANSWER]` | `[NAME]` |

**Q6.2 Where do we keep proof that we follow these rules?**
*Example:* `Folder /compliance/evidence/ — masking reports, approvals, access logs, deletion confirmations.`
**Your answer:** `[ANSWER]`

---

# PART 7 — KEEPING TEST DATA SAFE

## 7A. Who can access it

**Q7.1 Who can see or change test data in each place?**

| Place | Who | Approved by | Reviewed how often |
|---|---|---|---|
| Fake-data files | `[ANSWER]` | `[NAME]` | `[ANSWER]` |
| Masked data copies | `[ANSWER]` | `[NAME]` | `[ANSWER]` |
| Test databases | `[ANSWER]` | `[NAME]` | `[ANSWER]` |
| Staging | `[ANSWER]` | `[NAME]` | `[ANSWER]` |
| Test accounts in production | `[ANSWER]` | `[NAME]` | `[ANSWER]` |

**Q7.2 Principle of "least access": does each person get only what their job needs?**
- [ ] Yes
- [ ] No (fix this before launch)

## 7B. Protection

**Q7.3 Tick every protection in place.**
- [ ] Data is encrypted when stored
- [ ] Data is encrypted when moving (HTTPS/TLS)
- [ ] Logins need two-step verification
- [ ] Secrets (passwords, keys) live in a secret manager, never in code
- [ ] Test and production databases are separated and cannot connect to each other
- [ ] Test environments are not visible on the public internet, or are password-protected
- [ ] Access is logged
- [ ] Backups of test data follow the same rules as the data itself

**Q7.4 Where do secrets live?**
*Example:* `Company secret manager. Nothing in GitHub, chats, or documents.`
**Your answer:** `[ANSWER]`

## 7C. Places data can sneak into

**Q7.5 Confirm we have rules for each leak path.**

| Leak path | Rule | Done? |
|---|---|---|
| Logs and error messages | Never print personal data | `[ ]` |
| Screenshots and screen recordings | Blur or use fake data only | `[ ]` |
| Bug tickets and chat messages | No real data pasted | `[ ]` |
| Analytics and monitoring tools | Test traffic is labelled and filtered | `[ ]` |
| Email and SMS tests | Sent only to safe test addresses or a sandbox mail catcher | `[ ]` |
| Code repository | No data dumps committed | `[ ]` |
| Laptops and USB drives | No copies of masked/real data on personal devices | `[ ]` |
| Cloud storage and shared drives | Access restricted and labelled | `[ ]` |

---

# PART 8 — THIRD PARTIES AND SERVICES

**Q8.1 List every outside company or tool that touches test data.**

| Tool / vendor | What it does | Data it receives | Real data? | Contract / privacy agreement signed? | Owner |
|---|---|---|---|---|---|
| e.g. Stripe | Payments | Test card numbers | No | `[ ]` | `[NAME]` |
| e.g. Email provider | Sends emails | Fake emails | No | `[ ]` | `[NAME]` |
| e.g. Error monitor | Tracks errors | Test errors | No | `[ ]` | `[NAME]` |
| `[ADD MORE]` | | | | | |

**Q8.2 Rule for new tools.**
*Example (COMPANY DEFAULT):* `No new tool receives data until the Owner and Reviewer approve and add it to this table.`
**Your answer:** `[ANSWER]`

---

# PART 9 — AI AGENT RULES (STRICT)

> "AI agent" means any AI tool that reads, writes, tests or changes our code or data (coding assistants, test generators, chatbots, automation agents, LLM features inside the product).

## 9A. Which AI tools do we use?

**Q9.1 List each AI tool, its job, and the data it can see.**

| AI tool | Job | Can see what data? | Where does data go (company-only, or vendor servers)? | Does the vendor train on our data? | Owner |
|---|---|---|---|---|---|
| `[TOOL]` | `[JOB]` | `[ANSWER]` | `[ANSWER]` | `[ ] Yes [ ] No [ ] Unsure` | `[NAME]` |

## 9B. The rules (copy these into each agent's instructions)

**AI agents MUST:**
1. Use only synthetic or approved masked data when writing or running tests.
2. Use the safe fake patterns from Q2.4 whenever it creates example data.
3. Stop and ask a human if it finds data that looks real (real emails, phone numbers, card numbers, IDs, addresses).
4. Label every test record it creates (for example `is_test = true`).
5. Clean up the test data it created when the task ends, unless told to keep it.
6. Record what data it used, where, and when, so a human can check.
7. Work only inside the environment it was assigned.

**AI agents MUST NOT:**
1. Read, copy, export or summarise production or real customer data for testing.
2. Paste real customer data, secrets, keys, or passwords into prompts, logs, tickets, commits, or outputs.
3. Send test data to any tool or service not listed in Part 8.
4. Connect test environments to production databases.
5. Disable masking, logging, access controls, or safety checks.
6. Change this policy or approve its own exceptions.
7. Keep data after the task ends, or copy it to places not approved here.

**Q9.2 Which rules do we ADD for our project?**
*Example:* `The support-chat AI may never be given real chat transcripts, even for evaluation.`
**Your answer:** `[ANSWER]`

## 9C. AI-feature data (if the product contains AI)

**Q9.3 Does the product use AI / LLMs inside it?**
- [ ] No — write `N/A`
- [ ] Yes. Answer below:

**Q9.4 What data is used to test or evaluate the AI?**
- [ ] Hand-written test prompts and answers
- [ ] Synthetic conversations
- [ ] Masked real conversations (approved)
- [ ] Public datasets (license checked)
- [ ] Other: `[ANSWER]`

**Q9.5 Who checks that the AI does not leak private data or repeat sensitive training information?**
**Your answer:** `[NAME / METHOD]`

**Q9.6 Are AI test sets saved, versioned, and re-run before every release?**
- [ ] Yes, stored at: `[PATH/LINK]`
- [ ] No (fix before launch)

## 9D. Human checkpoint

**Q9.7 Which actions need a human to approve before an AI agent proceeds?**
*Example:* `Anything involving production, deleting data, creating more than 1,000 records, or new data sources.`
**Your answer:** `[ANSWER]`

---

# PART 10 — LAUNCH AND THE FIRST 500 CUSTOMERS

> The early customers are special: they are real people, and you may be tempted to use their data to fix bugs fast. This part sets the guardrails.

**Q10.1 How will we find bugs after launch without copying customer data into test places?**
*Example:* `We reproduce bugs using synthetic data that mimics the shape of the problem. Logs never contain personal data.`
**Your answer:** `[ANSWER]`

**Q10.2 Can support staff or engineers see customer data to fix problems?**
- [ ] No
- [ ] Yes, only with: `[ANSWER — e.g. customer's permission, ticket number, time limit, logged access]`

**Q10.3 Do we run any beta, early-access or pilot program?**
- [ ] No
- [ ] Yes. Rules for their data: `[ANSWER]`

**Q10.4 How do we keep test traffic out of customer numbers (so "500 customers" is true)?**
*Example:* `Test accounts carry is_test = true and are excluded from dashboards.`
**Your answer:** `[ANSWER]`

**Q10.5 Milestone checks.** Fill in who checks and how.

| Milestone | Check | Who | Date done |
|---|---|---|---|
| Before launch | No real data in any non-production place | `[NAME]` | `[DATE]` |
| Customer 10 | Logs and monitoring contain no personal data | `[NAME]` | `[DATE]` |
| Customer 100 | Access list reviewed; test accounts cleaned | `[NAME]` | `[DATE]` |
| Customer 250 | Privacy and retention rules reviewed; vendors rechecked | `[NAME]` | `[DATE]` |
| Customer 500 | Full policy review; update this document for the next growth stage | `[NAME]` | `[DATE]` |

**Q10.6 What will change when we grow past 500?**
*Example:* `Add a dedicated privacy officer, automatic masking pipeline, yearly audit.`
**Your answer:** `[ANSWER]`

---

# PART 11 — HOW LONG WE KEEP TEST DATA, AND HOW WE DELETE IT

**Q11.1 Fill in the keep-and-delete schedule.**

| Data | Keep for | Delete how | Who deletes | Proof of deletion |
|---|---|---|---|---|
| Fake data (local/dev) | Until no longer needed | Reset database | Engineer | Not required |
| Automated test data (CI) | Deleted after each run | Automatic cleanup | Automation | CI log |
| Masked data in staging | `[ANSWER, e.g. 30 days]` | `[ANSWER]` | `[NAME]` | `[ANSWER]` |
| Test accounts in production | `[ANSWER]` | `[ANSWER]` | `[NAME]` | `[ANSWER]` |
| Approved real-data exceptions | `[ANSWER, shortest possible]` | `[ANSWER]` | `[NAME]` | `[ANSWER]` |
| Logs, backups, screenshots | `[ANSWER]` | `[ANSWER]` | `[NAME]` | `[ANSWER]` |
| AI prompts and outputs | `[ANSWER]` | `[ANSWER]` | `[NAME]` | `[ANSWER]` |

**Q11.2 Is deletion complete, including backups, caches, and copies on other systems?**
- [ ] Yes
- [ ] Not yet. Plan: `[ANSWER]`

**Q11.3 What happens if a customer asks us to delete their data?**
*Example:* `We delete it from production within 30 days and check no copy exists in staging, logs or AI test sets.`
**Your answer:** `[ANSWER]`

---

# PART 12 — WHAT TO DO IF SOMETHING GOES WRONG

> Real data in a test place is a mistake, not a crime, if reported fast. Hiding it makes it worse.

**Q12.1 Examples of a "data mistake" for us:**
- Real customer data found in staging, a log, a screenshot, a ticket, or an AI prompt
- A masked file that can still identify people
- A real card number in code
- A test account that emailed a real customer
- A secret key shared in chat

**Q12.2 Who do I tell first, and how fast?**
*Example:* `Tell the Project Owner and Security Contact immediately (within 1 hour) via [CHANNEL]. Do not try to fix it quietly.`
**Your answer:** `Who: [NAME / CHANNEL] | Time limit: [ANSWER]`

**Q12.3 Our response steps (fill in the owner of each).**

| Step | What happens | Owner |
|---|---|---|
| 1. Stop | Stop the test; stop the AI agent; lock access | `[NAME]` |
| 2. Tell | Notify Owner and Security Contact | `[NAME]` |
| 3. Contain | Delete or isolate the data; rotate any exposed keys | `[NAME]` |
| 4. Assess | Whose data? How many people? How sensitive? Who saw it? | `[NAME]` |
| 5. Decide | Do laws require telling authorities or customers? (e.g. GDPR requires notice to the regulator within 72 hours in many cases.) | `[NAME]` |
| 6. Fix | Remove the cause; add a check so it cannot repeat | `[NAME]` |
| 7. Record | Write a short report: what, when, who, how fixed | `[NAME]` |
| 8. Learn | Update this policy if needed | `[NAME]` |

**Q12.4 Who decides whether to notify customers or regulators?**
**Your answer:** `[NAME / ROLE, with legal advisor if any]`

**Q12.5 Where are incident reports kept?**
**Your answer:** `[PATH/LINK]`

**Q12.6 Is there a "no blame" promise for people who report quickly?**
- [ ] Yes
- [ ] No

---

# PART 13 — WHO DOES WHAT, AND WHO SIGNS

## 13A. Roles

**Q13.1 Fill in a named person for each role.**

| Role | What they do in this policy | Name |
|---|---|---|
| **Project Owner** | Owns the policy; answers questions; approves exceptions | `[NAME]` |
| **QA / Test Lead** | Makes sure tests use only allowed data; checks masking | `[NAME]` |
| **Engineering Lead** | Builds data generators, masking, cleanup, access controls | `[NAME]` |
| **Security / Privacy Contact** | Reviews risk; handles incidents; advises on laws | `[NAME]` |
| **AI Workflow Owner** | Controls what AI agents can access and do | `[NAME]` |
| **Reviewer** | Independent check of this document | `[NAME]` |
| **Every team member** | Follows the rules; reports mistakes fast | Everyone |

## 13B. Exceptions

**Q13.2 How does someone ask for an exception to a rule?**
*Example:* `Write a request with: what, why, how long, how risk is reduced. Project Owner and Security Contact must both approve in writing. Max 30 days; review before renewal.`
**Your answer:** `[ANSWER]`

**Q13.3 Where are approved exceptions recorded?**
**Your answer:** `[PATH/LINK]`

## 13C. Training

**Q13.4 How does a new person learn this policy?**
*Example:* `Read it in the first week, answer 5 questions, sign below.`
**Your answer:** `[ANSWER]`

## 13D. Sign-off

| Role | Name | Signature / approval | Date |
|---|---|---|---|
| Project Owner | `[NAME]` | `[ ]` | `[DATE]` |
| Reviewer | `[NAME]` | `[ ]` | `[DATE]` |
| Security / Privacy Contact | `[NAME]` | `[ ]` | `[DATE]` |

---

# PART 14 — HOW WE CHECK THE POLICY IS WORKING

**Q14.1 How often do we audit?**
*Example:* `Monthly quick scan; quarterly full review; extra review before launch and at customers 100, 250 and 500.`
**Your answer:** `[ANSWER]`

**Q14.2 What do we measure?** (tick all you will track)
- [ ] Number of real-data incidents (target: 0)
- [ ] Time to report incidents
- [ ] Masking scan pass rate
- [ ] Number of open exceptions
- [ ] Number of people with access vs. the number who need it
- [ ] Test accounts left behind in production
- [ ] Other: `[ANSWER]`

**Q14.3 Which automated checks run?**
*Example:* `Pre-commit scan for secrets; CI scan for real-looking emails/cards; weekly scan of staging.`
**Your answer:** `[ANSWER]`

---

# PART 15 — FINAL READINESS CHECKLIST (GO / NO-GO)

> Tick every item. Any `[ ]` left = do not launch.

## Document
- [ ] Every question is answered or marked `N/A — reason`
- [ ] No `[PLACEHOLDER]` text is left
- [ ] Every Owner is a named person or role
- [ ] Reviewer signed Part 13

## Data
- [ ] All data fields listed and rated (Q2.3)
- [ ] Safe fake patterns defined (Q2.4)
- [ ] Stage × Environment matrix complete (Q3.2)
- [ ] Masking is proven before use (Q4.7) or masking is not used
- [ ] No real customer data in non-production, except approved exceptions (Q4.11)

## Safety
- [ ] Access is least-needed and logged (Part 7)
- [ ] Secrets are in a secret manager
- [ ] Test and production are separated
- [ ] Logs, screenshots, tickets and chats are covered (Q7.5)
- [ ] Every vendor is listed and approved (Part 8)

## AI
- [ ] Every AI tool is listed (Q9.1)
- [ ] Strict AI rules are copied into each agent's instructions (Part 9B)
- [ ] Human approval points defined (Q9.7)
- [ ] AI test sets are saved and versioned, if the product has AI

## Laws
- [ ] Applicable laws and standards identified (Part 6)
- [ ] Evidence location defined (Q6.2)

## Launch and growth
- [ ] Test accounts are labelled and excluded from customer counts
- [ ] Support access rules defined (Q10.2)
- [ ] Milestone checks scheduled for customers 10 / 100 / 250 / 500 (Q10.5)

## Cleanup and response
- [ ] Retention and deletion schedule complete (Part 11)
- [ ] Incident steps and contacts are known to everyone (Part 12)
- [ ] Team has read and understood this policy (Q13.4)

**Final decision:**
- [ ] GO — all items ticked
- [ ] NO-GO — open items: `[LIST]`

**Signed:** `[NAME]` **Date:** `[DATE]`

---

# GLOSSARY (PLAIN-ENGLISH WORDS)

| Word | Simple meaning |
|---|---|
| **Test data** | Information we use to check the product works |
| **Synthetic data** | Made-up data; nobody is real |
| **Masking** | Hiding or scrambling real details so people cannot be identified |
| **Anonymisation** | Changing data so a person can never be found again |
| **Pseudonymisation** | Swapping names for codes; with a key, the person can be found, so it is still protected data |
| **Personal data (PII)** | Anything that identifies a person: name, email, phone, address, ID, photo |
| **Sensitive data** | Extra-risky personal data: health, payments, children, biometrics, etc. |
| **Environment** | A place where the product runs (local, dev, staging, production) |
| **Staging** | A practice copy of the real product used for final checks |
| **Production** | The real product that customers use |
| **CI (Continuous Integration)** | Robots that automatically run checks when code changes |
| **Seed** | A fixed starting number that makes "random" data repeat the same way |
| **Test account** | A fake user account used to check the live product |
| **Secret** | A password, key or token that must never be shared |
| **Least access** | Giving people only the access they need |
| **Encryption** | Locking data so only authorised people can read it |
| **Retention** | How long we keep data |
| **Incident** | A mistake or leak involving data |
| **AI agent** | An AI tool that can read, write, test or change our code or data |
| **LLM** | A large language model; the kind of AI that chats and writes |
| **GDPR / HIPAA / PCI-DSS / SOC 2 / ISO 27001** | See Part 6 |

---

# REVISION HISTORY

| Version | Date | Changed by | What changed | Approved by |
|---|---|---|---|---|
| 1.0 | `[DATE]` | `[NAME]` | First version | `[NAME]` |
| | | | | |
