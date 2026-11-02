# HOW TO FILL IN THIS DOCUMENT (READ THIS FIRST)

> **Template name:** Unit Testing Plan (Universal Template)
> **Template version:** 1.1.0 (Draft)
> **Folder:** `Testing and Quality Assurance/Unit_Testing_Plan.md`
> **Covers:** Web apps · Mobile apps · AI / LLM features
> **Lifecycle covered:** First line of code → launch day → your first 500 customers
> **Built on:** IEEE 829 test plan structure, ISO/IEC/IEEE 29119 (test documentation, test techniques, agile and AI-testing guidance), and current practice for testing AI features

---

## What is this document?

A **Unit Testing Plan** is a written promise about how you will check that every small piece of your product works **before** a customer ever touches it.

- A **unit** is the smallest piece of your product that does one job (for example, "add two prices together" or "check an email address is valid").
- A **unit test** is a tiny automatic check that runs that piece and says **PASS** or **FAIL**.
- This plan decides **what** you will test, **how**, **when**, **who** does it, and **how you know you are done**.

You will copy this file once per project, fill it in, and keep it up to date until your product has served its first 500 customers.

## Who can fill this in?

Anyone, including a beginner working alone with AI helpers. Every section asks plain questions. You never have to invent the structure. You only answer the questions.

## The 7 rules (simple and strict)

1. **Copy first.** Copy this file into your project. Never fill in the master template.
2. **Answer every question.** Every question has a ✍️ **Your answer** spot. Fill it in.
3. **Use the examples as a guide, not as answers.** 💡 examples show what a good answer looks like. Delete them or leave them. Never leave an example as your answer.
4. **Don't know yet? Write `TBD – owner: <name> – date: <YYYY-MM-DD>`.** Never leave a blank and never guess silently.
5. **Pick from menus.** Where you see ☐ boxes, change `☐` to `☑` for every option that applies. Write your own choice in the "Other" line if needed.
6. **Be specific.** "Test everything" is not an answer. "Test the 12 functions listed in Section 4.2" is.
7. **Finish with the checklist.** Section 25 tells you whether the plan is ready.

## The symbols used in this document

| Symbol | Meaning |
|---|---|
| ❓ | A question you must answer |
| 💡 | An example answer (for guidance only) |
| ✍️ | The place where you write your answer |
| ☐ / ☑ | Empty checkbox / ticked checkbox |
| 🟢 | Easy – takes under 5 minutes |
| 🟡 | Medium – needs a little thinking |
| 🔴 | Important – needs care, because mistakes here are costly |
| `[[like this]]` | A blank to fill. When you finish the document, **no `[[ ]]` may remain** (search the file for `[[` to check). |

## How long will this take?

| Your situation | Estimated time |
|---|---|
| New project, you know your features | 2–4 hours |
| Existing project, code already written | 4–8 hours (you must list existing units first) |
| Each later update (per phase gate) | 15–30 minutes |

## How to fill it in with an AI assistant

1. Give the AI this entire file plus a short description of your product.
2. Say: *"Interview me one section at a time. Ask the ❓ questions in plain language. Write my answers under ✍️. Do not guess. Mark anything unknown as TBD."*
3. At the end, say: *"Run the Section 25 checklist and list anything missing."*
4. You, the human, **read and approve every answer**. AI drafts. You decide.

## Mini dictionary (plain words)

| Word | Plain meaning |
|---|---|
| Unit | The smallest piece of code that does one job |
| Unit test | A tiny automatic check of one unit |
| Mock / stub / fake | A pretend version of something slow or risky (like a payment service or an AI model) so your test stays fast and safe |
| Coverage | The percentage of your code that your tests actually run |
| Regression | Something that used to work and then broke after a change |
| Flaky test | A test that sometimes passes and sometimes fails for no real reason |
| CI | A robot that runs all your tests every time you save changes |
| Eval | A test for AI output, which can differ every time, so it is scored instead of checked for an exact match |
| Gate | A checkpoint. You may not move to the next phase until the gate's rules are met |
| Go / No-Go | The decision to continue (Go) or to stop and fix (No-Go) |
| Severity | How bad a bug is (1 = disaster, 4 = tiny) |

---
---

# UNIT TESTING PLAN

---

## 0. Document Control 🟢

**Why this matters:** Without an ID and version, two people end up using two different "final" plans.

❓ **0.1 Fill in the identity table.**

💡 *Example: ID `UTP-ACME-WEB-001`, Version `1.0.0`, Status `Draft`.*

| Field | Your answer ✍️ |
|---|---|
| Plan ID (format: `UTP-<PROJECT>-<PLATFORM>-<NUMBER>`) | `[[ ]]` |
| Project name | `[[ ]]` |
| Plan version (`major.minor.patch`) | `[[ ]]` |
| Status (☐ Draft ☐ In review ☐ Approved ☐ Superseded) | `[[ ]]` |
| Plan owner (one named person) | `[[ ]]` |
| Date created (YYYY-MM-DD) | `[[ ]]` |
| Last updated (YYYY-MM-DD) | `[[ ]]` |
| Next review date (suggested: every phase gate, or every 30 days) | `[[ ]]` |
| Where is the code stored? (link) | `[[ ]]` |
| Where are test results stored? (link) | `[[ ]]` |

❓ **0.2 Version history.** Add one row every time you change the plan in a meaningful way.

| Version | Date | Author | What changed and why |
|---|---|---|---|
| 0.1.0 | `[[ ]]` | `[[ ]]` | First draft |
| `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |

❓ **0.3 Who must approve this plan?** (A solo builder may hold several roles, but must still sign once per role.)

| Role | Name | Decision (☐ Approved ☐ Changes needed) | Date | Signature / initials |
|---|---|---|---|---|
| Plan author | `[[ ]]` | ☐ ☐ | `[[ ]]` | `[[ ]]` |
| Product owner (decides what is built) | `[[ ]]` | ☐ ☐ | `[[ ]]` | `[[ ]]` |
| Engineering lead (decides how it is built) | `[[ ]]` | ☐ ☐ | `[[ ]]` | `[[ ]]` |
| Quality owner (decides if quality is good enough) | `[[ ]]` | ☐ ☐ | `[[ ]]` | `[[ ]]` |
| Security / privacy reviewer | `[[ ]]` | ☐ ☐ | `[[ ]]` | `[[ ]]` |
| Final approver | `[[ ]]` | ☐ ☐ | `[[ ]]` | `[[ ]]` |

---

## 1. Purpose and Plain-English Summary 🟢

**Why this matters:** If you cannot explain the plan in a few sentences, nobody else will follow it.

❓ **1.1 In 2–4 sentences, what does this plan protect?**

💡 *Example: "This plan makes sure every calculation, form check and AI prompt wrapper in the Bakery Orders app is tested automatically before each release, so the first 500 customers never see wrong prices or broken checkout."*

✍️ **Your answer:** `[[ ]]`

❓ **1.2 What is the single biggest thing that must never break?**

💡 *Example: "A customer is charged the wrong amount."*

✍️ **Your answer:** `[[ ]]`

❓ **1.3 What does "success" look like at 500 customers?** (Give numbers.)

💡 *Example: "Fewer than 2 customer-reported bugs per week that a unit test could have caught; all unit tests pass on every release; checkout code at 95% coverage."*

✍️ **Your answer:** `[[ ]]`

---

## 2. Product Snapshot 🟢

**Why this matters:** The kind of product decides which tests matter most.

❓ **2.1 What does your product do, in one sentence?**

✍️ **Your answer:** `[[ ]]`

❓ **2.2 Which platforms does it run on?** (tick all)

- ☐ Website / web app (runs in a browser)
- ☐ iOS app
- ☐ Android app
- ☐ Cross-platform mobile (one codebase for both)
- ☐ Backend / server / API
- ☐ Database or data processing
- ☐ Other: `[[ ]]`

❓ **2.3 Does your product contain AI / LLM features?**

- ☐ No → skip Section 7.3 and the AI rows in later tables (write "N/A – no AI")
- ☐ Yes → fill in the table below

| AI feature name | What it does | Which AI model / provider | Can it take actions (send emails, spend money, change data)? ☐ Yes ☐ No |
|---|---|---|---|
| `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ |

❓ **2.4 What programming languages and frameworks do you use?**

💡 *Example: "TypeScript, React, Node.js; Swift for iOS; Python for AI scripts."*

✍️ **Your answer:** `[[ ]]`

❓ **2.5 How will the lifecycle be run?** (tick one)

- ☐ AI-assisted: a human writes, AI helps
- ☐ AI-driven: AI agents write most code, a human reviews and decides
- ☐ Human-only

❓ **2.6 Key dates.**

| Milestone | Target date |
|---|---|
| Start of build | `[[ ]]` |
| Pre-launch freeze (no new features) | `[[ ]]` |
| Launch day | `[[ ]]` |
| Customer #50 (expected) | `[[ ]]` |
| Customer #500 (expected) | `[[ ]]` |

---

## 3. Reference Documents 🟢

**Why this matters:** Tests are only as good as the requirements they check.

❓ **3.1 List every document this plan depends on.** If a document does not exist, write "Does not exist – owner/date".

| Document | Link or location | Version | Exists? |
|---|---|---|---|
| Product requirements / feature list | `[[ ]]` | `[[ ]]` | ☐ Yes ☐ No |
| Architecture / design notes | `[[ ]]` | `[[ ]]` | ☐ Yes ☐ No |
| Coding standards | `[[ ]]` | `[[ ]]` | ☐ Yes ☐ No |
| Overall test strategy (if one exists) | `[[ ]]` | `[[ ]]` | ☐ Yes ☐ No |
| Integration / end-to-end test plan | `[[ ]]` | `[[ ]]` | ☐ Yes ☐ No |
| Security and privacy policy | `[[ ]]` | `[[ ]]` | ☐ Yes ☐ No |
| AI usage / safety policy | `[[ ]]` | `[[ ]]` | ☐ Yes ☐ No |

---

## 4. Scope: What We Test and What We Don't 🔴

**Why this matters:** The most common testing failure is not knowing what was never tested.

### 4.1 Scope statement

❓ **4.1.1 Which parts of the product does this plan cover?**

💡 *Example: "All code we wrote ourselves in the `/src` and `/app` folders, including prompt-building code and AI response parsers."*

✍️ **Your answer:** `[[ ]]`

❓ **4.1.2 What is deliberately NOT covered, and why? Where is it covered instead?**

💡 *Example: "Third-party payment SDK internals – covered by the vendor. Full screen-to-screen flows – covered by the End-to-End Test Plan."*

✍️ **Your answer:** `[[ ]]`

### 4.2 Unit inventory (the list of things to test)

❓ **4.2.1 List every unit (function, class, component, screen logic, prompt builder) that needs a test.** Add rows until nothing is missing. For existing code, scan the project to build the list.

**Risk rating:** 3 = customer harm or money lost if broken, 2 = feature breaks, 1 = minor annoyance.

| Unit ID | Unit name | Where it lives (file/folder) | Platform (Web/Mobile/Backend/AI) | Risk (1–3) | Priority (Must / Should / Could) |
|---|---|---|---|---|---|
| U-001 | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| U-002 | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| U-003 | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |

💡 *Example row: `U-014 | calculateOrderTotal | src/pricing/total.ts | Web+Backend | 3 | Must`.*

### 4.3 Features to be tested vs. not tested

| Feature | Tested at unit level? | If no, why not? |
|---|---|---|
| `[[ ]]` | ☐ Yes ☐ No | `[[ ]]` |

---

## 5. Risk Assessment 🔴

**Why this matters:** You cannot test everything equally. Spend most effort where failure hurts most.

❓ **5.1 What could go wrong, how likely is it, and how bad would it be?**

Score **Likelihood (1–3)** × **Impact (1–3)** = **Risk score (1–9)**. Test highest scores first.

| Risk ID | What could go wrong | Likelihood (1–3) | Impact (1–3) | Score | Which units / tests reduce it |
|---|---|---|---|---|---|
| R-01 | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| R-02 | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` |

💡 *Example: "R-01 | Wrong tax calculated | 2 | 3 | 6 | U-014, U-015, tests T-120 to T-135".*

❓ **5.2 Common risks to check.** Tick every risk that applies, then add it to the table above.

- ☐ Money, pricing, discounts, tax
- ☐ Login, passwords, permissions
- ☐ Personal or private data (names, emails, health, payment)
- ☐ Dates, times, time zones
- ☐ Data loss or data corruption
- ☐ Offline or bad-network behaviour (mobile)
- ☐ Different screen sizes / devices / browsers
- ☐ AI gives wrong, unsafe, biased or made-up answers
- ☐ AI is manipulated by hostile input (prompt injection)
- ☐ AI costs spiral (too many calls, too many tokens)
- ☐ Third-party service goes down or changes
- ☐ Other: `[[ ]]`

---

## 6. Test Approach (How We Test) 🟡

**Why this matters:** Everybody must write tests in the same way, or the test suite becomes a mess.

### 6.1 Definition and rules

❓ **6.1.1 In your project, what exactly counts as a "unit test"?** Tick the rules you agree with.

- ☐ Tests one unit at a time
- ☐ Runs in under 1 second (fast)
- ☐ Never touches the real internet, real database, real payment system or real AI model (these are replaced by mocks)
- ☐ Gives the same answer every time it runs
- ☐ Can run in any order, alone or together
- ☐ Cleans up after itself
- ☐ Other rule: `[[ ]]`

❓ **6.1.2 What is NOT a unit test in your project?** (so nobody mislabels slower tests)

💡 *Example: "Anything that opens a real browser, calls the real AI model or needs a network is an integration test or eval, and lives in a different folder."*

✍️ **Your answer:** `[[ ]]`

### 6.2 Test design techniques

❓ **6.2.1 Which techniques will you use?** (tick all that fit; this list follows standard test techniques)

- ☐ **Normal cases:** the expected, everyday inputs
- ☐ **Boundary cases:** the edges (0, 1, maximum, one over maximum, empty, very long)
- ☐ **Equivalence groups:** one test per group of similar inputs (for example valid email / invalid email)
- ☐ **Error cases:** what happens when things go wrong
- ☐ **Null / empty / missing input**
- ☐ **Decision tables:** for rules with many conditions (for example discount rules)
- ☐ **State changes:** for things that move through steps (for example order: placed → paid → shipped)
- ☐ **Property-based tests:** generate hundreds of random inputs and check rules that must always be true
- ☐ **Branch / statement coverage checks:** make sure every `if` path was run
- ☐ **Mutation testing (advanced):** deliberately break code to prove the tests notice
- ☐ Other: `[[ ]]`

### 6.3 How each test is written

❓ **6.3.1 Which test structure will you use?** (recommended: Arrange → Act → Assert)

- ☐ **Arrange** (set up the input), **Act** (run the unit), **Assert** (check the result): recommended
- ☐ Given / When / Then
- ☐ Other: `[[ ]]`

❓ **6.3.2 Naming rule for tests.**

💡 *Example: `calculateOrderTotal_withTenPercentCoupon_returnsDiscountedTotal`*

✍️ **Your rule:** `[[ ]]`

❓ **6.3.3 Where do test files live, and what are they called?**

💡 *Example: "Next to the code, named `total.test.ts`" or "In `/tests/unit/`, named `test_total.py`".*

✍️ **Your answer:** `[[ ]]`

### 6.4 Mocks, test data and fakes

❓ **6.4.1 What will be replaced with a pretend version in unit tests?**

| Real thing | Pretend version we use | Where it lives |
|---|---|---|
| Database | `[[ ]]` | `[[ ]]` |
| Payment provider | `[[ ]]` | `[[ ]]` |
| Email / SMS | `[[ ]]` | `[[ ]]` |
| Clock / current time | `[[ ]]` | `[[ ]]` |
| AI model | `[[ ]]` | `[[ ]]` |
| Other: `[[ ]]` | `[[ ]]` | `[[ ]]` |

❓ **6.4.2 Where does test data come from?** (tick all)

- ☐ Hand-written small samples
- ☐ Generated fake data
- ☐ Copies of real data with all personal details removed
- ☐ **Never** real customer data (this box must stay ticked: ☐ I confirm)

---

## 7. Platform-Specific Testing 🟡

Fill in **only** the parts that match your Section 2.2 answer. Mark the others "N/A".

### 7.1 Web apps

❓ **7.1.1 What kinds of web units will you test?** (tick all)

- ☐ Pure functions (formatting, calculations, validation)
- ☐ UI components in isolation (buttons, forms, cards)
- ☐ State management (stores, reducers, hooks)
- ☐ API route handlers / controllers
- ☐ Data-access layer (queries) against a fake or in-memory database
- ☐ Form validation rules
- ☐ Accessibility rules at component level (labels, roles, keyboard focus)
- ☐ Browser-specific logic
- ☐ Other: `[[ ]]`

❓ **7.1.2 Which browsers and screen sizes matter?** `[[ ]]`

### 7.2 Mobile apps

❓ **7.2.1 What kinds of mobile units will you test?** (tick all)

- ☐ Business logic (no screen needed)
- ☐ View models / presenters / state holders
- ☐ Screen components in isolation
- ☐ Local storage and caching logic
- ☐ Offline / slow-network handling (using a fake network)
- ☐ Permissions logic (camera, location, notifications)
- ☐ App-version upgrade logic (old saved data → new format)
- ☐ Push notification handling
- ☐ Other: `[[ ]]`

❓ **7.2.2 Which OS versions and device types are supported?**

💡 *Example: "iOS 17+, Android 12+, phones only."*

✍️ **Your answer:** `[[ ]]`

### 7.3 AI / LLM features

**Why this is different:** AI answers can change every time. So we split the testing into **two parts**:

- **Part A – Unit tests (exact):** test the code *around* the AI, with the AI replaced by a pretend model. These always give the same answer.
- **Part B – Evals (scored):** run the real AI on a fixed set of example questions and *score* the answers. These give a score like "92% good", not an exact match.

❓ **7.3.1 Part A: which surrounding code will you unit test?** (tick all; use a pretend model)

- ☐ Prompt-building code (does the right text get assembled?)
- ☐ Response parsing (does bad or broken AI output get handled safely?)
- ☐ Output format checks (is the JSON valid, are required fields present?)
- ☐ Tool / function-call argument checks (right format, for example dates)
- ☐ Safety filters and blocklists
- ☐ Retry, timeout and fallback logic
- ☐ Token and cost limiters
- ☐ Caching logic
- ☐ "Forbidden action never runs" guards (for example AI may never delete data)
- ☐ Other: `[[ ]]`

❓ **7.3.2 Part B: what will your evals check?** (tick all)

- ☐ Correct answer / correct label on known examples
- ☐ Stays on topic
- ☐ Never makes up facts (hallucination check against known sources)
- ☐ Follows the required format
- ☐ Refuses unsafe requests
- ☐ Resists hostile instructions hidden in user input (prompt injection)
- ☐ Tone and brand voice
- ☐ Same meaning when the question is reworded (metamorphic check)
- ☐ Other: `[[ ]]`

❓ **7.3.3 Eval rules.**

| Question | Your answer ✍️ |
|---|---|
| How many example inputs are in the eval set at launch? (suggested minimum: 30 per AI feature) | `[[ ]]` |
| Who writes and approves the examples? | `[[ ]]` |
| What score counts as PASS? (suggested start: 90%; write your own) | `[[ ]]` |
| How many times is each example run to handle randomness? (suggested: 3–5) | `[[ ]]` |
| Which model version is pinned for testing? | `[[ ]]` |
| If a judge AI scores answers: which model, and where is the scoring rubric stored? | `[[ ]]` |
| Where are eval examples and prompts stored in version control? | `[[ ]]` |
| What is the maximum money you will spend per eval run? | `[[ ]]` |
| What happens when the AI vendor updates the model? | `[[ ]]` |

### 7.4 Performance and accessibility at unit level 🟡

**Why this matters:** A feature that works but is painfully slow, or that some people cannot use, is still broken. Unit tests can catch many of these early, cheaply.

> Full speed tests of the whole system (load tests) and full screen-reader walkthroughs belong in your integration / end-to-end plan. Here we only cover what a single unit can prove.

❓ **7.4.1 Performance: which unit-level checks will you use?** (tick all)

- ☐ **Time budget:** important functions must finish within a set time on a typical input
- ☐ **Big-input check:** the function still works on very large input (for example 10,000 list items)
- ☐ **Query-count check:** a screen or endpoint must not ask the (fake) database more times than allowed (this catches the "N+1 queries" mistake)
- ☐ **Memory / size limit:** lists, caches and images stay under a set size
- ☐ **No repeated heavy work:** a cached result is reused, not recalculated
- ☐ **AI token and cost budget:** prompt-building code never exceeds a set number of tokens
- ☐ **Timeout behaviour:** slow dependencies are cut off and handled safely
- ☐ Other: `[[ ]]`

❓ **7.4.2 Performance budgets.** *(Suggested starts shown; replace them with your own.)*

| What is measured | Suggested start | Your budget ✍️ |
|---|---|---|
| Time for a pure calculation / formatting function, typical input | under 50 ms | `[[ ]]` |
| Time for the same function on the big input | under 500 ms | `[[ ]]` |
| Database queries for one list screen or API call (with fake database) | no more than `[[ ]]` | `[[ ]]` |
| Largest prompt sent to the AI (tokens) | `[[ ]]` | `[[ ]]` |
| Maximum AI calls per user action | `[[ ]]` | `[[ ]]` |

> Timing tests can be flaky on slow machines. Use generous limits, or count operations (for example "number of queries") instead of seconds wherever you can.

❓ **7.4.3 Accessibility: which standard are you aiming for?**

- ☐ WCAG 2.2 Level AA (recommended for most products)
- ☐ WCAG 2.2 Level A (minimum)
- ☐ A legal or customer requirement applies: `[[ name it ]]`
- ☐ Not decided yet: `TBD – owner: [[ ]] – date: [[ ]]`

❓ **7.4.4 Which accessibility checks will be unit tests?** (tick all that fit your platforms)

| Check | Web | Mobile |
|---|---|---|
| Every button, icon and image has a text label for screen readers | ☐ | ☐ |
| Form fields have labels and clear error messages | ☐ | ☐ |
| Roles and states are correct (button, checkbox, expanded / collapsed) | ☐ | ☐ |
| Keyboard use works: focus order is logical, nothing traps focus | ☐ | n/a |
| Colour pairs in your design settings meet contrast rules (suggested: 4.5:1 for normal text) | ☐ | ☐ |
| Touch targets are big enough (suggested: 44×44 points on iOS, 48×48 dp on Android) | n/a | ☐ |
| Text still fits when the user makes text larger | ☐ | ☐ |
| Animations can be turned off ("reduce motion") | ☐ | ☐ |
| AI answers that include lists, links or images keep labels and structure | ☐ | ☐ |

❓ **7.4.5 Who checks what tests cannot?** (Some accessibility problems need a human. Name who and when.)

✍️ **Your answer:** `[[ ]]`

---

## 8. Tools and Environment 🟡

**Why this matters:** If the test setup differs between machines, results cannot be trusted.

❓ **8.1 Pick your tools.** Tick one per row, or write your own. *(Suggestions are examples, not requirements.)*

| Need | Options | Your choice ✍️ |
|---|---|---|
| Test runner (JavaScript / TypeScript) | ☐ Jest ☐ Vitest ☐ Mocha ☐ Other | `[[ ]]` |
| Test runner (Python) | ☐ Pytest ☐ unittest ☐ Other | `[[ ]]` |
| Test runner (Swift / iOS) | ☐ XCTest ☐ Swift Testing ☐ Other | `[[ ]]` |
| Test runner (Kotlin / Android) | ☐ JUnit ☐ Kotest ☐ Other | `[[ ]]` |
| Test runner (Dart / Flutter) | ☐ flutter_test ☐ Other | `[[ ]]` |
| UI component testing | ☐ Testing Library ☐ Storybook tests ☐ Other | `[[ ]]` |
| Mocking | ☐ Built-in mocks ☐ Mockito ☐ MSW ☐ Other | `[[ ]]` |
| Coverage report | ☐ Istanbul / c8 ☐ coverage.py ☐ JaCoCo ☐ Xcode coverage ☐ Other | `[[ ]]` |
| AI evals | ☐ Promptfoo ☐ LangSmith ☐ Custom scripts ☐ Other | `[[ ]]` |
| Automatic runner (CI) | ☐ GitHub Actions ☐ GitLab CI ☐ Other | `[[ ]]` |
| Bug tracker | ☐ GitHub Issues ☐ Jira ☐ Linear ☐ Other | `[[ ]]` |

❓ **8.2 Test environment.**

| Question | Your answer ✍️ |
|---|---|
| Where do tests run? (☐ my computer ☐ CI robot ☐ both) | `[[ ]]` |
| Exact versions of language and tools (so everyone matches) | `[[ ]]` |
| How does a new person run all tests? (write the exact command) | `[[ ]]` |
| How does a person run one test? (exact command) | `[[ ]]` |
| Are secrets (passwords, API keys) kept out of test code? ☐ Yes (required) | `[[ ]]` |

---

## 9. Quality Targets 🔴

**Why this matters:** "Good enough" needs numbers, or it becomes an argument.

❓ **9.1 Set your targets.** *(Suggested starting values are shown. Change them if you have a reason and write the reason.)*

| Measure | Plain meaning | Suggested start | Your target ✍️ |
|---|---|---|---|
| Pass rate | % of tests passing before any release | 100% | `[[ ]]` |
| Line coverage, all code | % of code lines run by tests | 70–80% | `[[ ]]` |
| Line coverage, risk-3 units (money, security, privacy) | Same, for the dangerous parts | 90–100% | `[[ ]]` |
| Branch coverage, risk-3 units | Every `if` path run | 85–95% | `[[ ]]` |
| Max time to run all unit tests | Fast = people actually run them | under 5 minutes | `[[ ]]` |
| Flaky tests allowed | Tests that randomly fail | 0 | `[[ ]]` |
| AI eval pass score | See 7.3.3 | 90% | `[[ ]]` |
| Max AI cost per eval run | See 7.3.3 | `[[ ]]` | `[[ ]]` |

❓ **9.2 Why these numbers?**

✍️ **Your answer:** `[[ ]]`

> ⚠️ Coverage is a **floor**, not a goal. 100% coverage with weak checks is worse than 70% with strong checks. Every test must check something meaningful.

---

## 10. AI Coding Agents in Testing 🔴

**Why this matters:** AI agents write fast, and they can also write tests that prove nothing, or "fix" a test by changing it so it passes. This section sets the safety rules.

❓ **10.1 Which AI agents or assistants write code or tests in this project?**

| Agent / tool | What it is allowed to do | What it is NOT allowed to do |
|---|---|---|
| `[[ ]]` | `[[ ]]` | `[[ ]]` |

❓ **10.2 Rules for AI-written tests.** Tick every rule you adopt. *(Recommended: all.)*

- ☐ AI may write new unit tests, but a human reads each one before it is merged
- ☐ AI may **not** delete, skip or weaken an existing test just to make it pass
- ☐ AI may **not** change the expected answer in a test without a human-approved reason
- ☐ AI must run the full unit test suite and show the result before saying "done"
- ☐ AI must say which units it tested and which it did not
- ☐ AI must not invent requirements; if unclear it must ask or mark TBD
- ☐ AI must not touch the "do not touch" list below
- ☐ Tests written by AI must also be checked for meaning, not just passing (spot-check with deliberately broken code)
- ☐ Other: `[[ ]]`

❓ **10.3 "Do not touch" list.** Which files or folders must AI never change on its own?

💡 *Example: "Payment code, security rules, the eval pass-score file, this plan."*

✍️ **Your answer:** `[[ ]]`

❓ **10.4 What must a human always review?** (tick all)

- ☐ Tests for risk-3 units
- ☐ Any change to coverage targets
- ☐ Any change to eval examples or scoring rubric
- ☐ Any test that was deleted, skipped or marked "ignore"
- ☐ All mocks of payment, security and AI services
- ☐ Other: `[[ ]]`

❓ **10.5 Starter instruction to give an AI agent.** Copy, adjust and keep it in your repository.

```text
You are helping with the unit tests of [[PROJECT NAME]].
Read Unit_Testing_Plan.md fully before starting.
For each unit I name: write Arrange-Act-Assert tests that cover normal,
boundary, empty and error cases.
Never delete, skip or weaken existing tests. Never edit files on the
"do not touch" list. Replace real network, database, payment and AI model
calls with fakes.
When done, run the full unit test suite, paste the pass/fail summary and the
coverage result, and list any unit you did not cover and why.
If something is unclear, ask me; do not guess.
```

### 10.6 Agent workflow: who does what in each phase 🔴

**Why this matters:** In an AI-driven lifecycle, work passes back and forth between you and AI agents. Clear handoffs and a clear "done" stop work from being half-finished or silently wrong.

❓ **10.6.1 Handoff table.** Confirm or edit each row. Each handoff needs **proof** (a link, a report or a screenshot).

| Phase | Human does | AI agent does | Handoff proof | Agent task is "done" when… |
|---|---|---|---|---|
| P0 Plan | Answers the ❓ questions, approves scope and risks | Interviews the human, drafts unit inventory (Prompt D1), sets up test tooling | Signed plan; sample test passing in CI | The sample test passes on a clean machine and the unit list is human-approved |
| P1 Build | Writes or approves requirements; reviews every risk-3 test | Writes code and unit tests together (Prompt D2); runs the suite after every change | Test run summary + coverage report attached to each change | New code has tests, suite is 100% pass, coverage target met, uncovered units listed |
| P1 Build (AI features) | Writes and approves eval examples and rubric | Drafts eval examples (Prompt D4); runs evals; reports scores | Eval report with model version, scores, and cost | Scores meet 7.3.3 and every example is human-approved |
| P2 Pre-launch | Decides what to accept or fix; runs the rollback rehearsal | Hunts for weak tests (Prompt D3); expands eval set; fixes flaky tests | Gap list, review notes, clean-machine run | Gaps listed and signed, no flaky tests, deliberate-break check done on risk-3 units |
| P3 Launch day | Makes Go / No-Go; owns the stop button | Summarises errors and AI quality; drafts failing tests for new bugs | Launch log with times and decisions | Each launch bug has a failing test written before the fix |
| P4 Customers 1–50 | Chooses which feedback to act on; handles private data | Turns reports into failing tests (Prompt D5); proposes eval additions | Bug report + failing test + fix link | Failing test now passes, nothing else broke, bug labelled "escaped" |
| P5 Customers 51–500 | Monthly review; approves plan changes | Re-runs all evals after changes; prunes outdated tests (human approves) | Monthly health report | Report delivered; every proposed deletion approved by a human |

❓ **10.6.2 Definition of Done for ANY agent task.** Tick every item you require. *(Recommended: all.)*

- ☐ The agent restated the task in its own words before starting
- ☐ The agent ran the **full** unit suite, not just the new tests
- ☐ The agent pasted the real pass / fail numbers (no "should pass")
- ☐ The agent listed every file it changed
- ☐ The agent listed what it did **not** do and what it is unsure about
- ☐ No test was deleted, skipped or loosened (or each one is listed with a human-approved reason)
- ☐ No file on the "do not touch" list (10.3) changed
- ☐ A human opened and read the result
- ☐ Other: `[[ ]]`

❓ **10.6.3 When must the agent STOP and ask a human?** Tick all you require.

- ☐ A test fails and the "fix" would be to change the test
- ☐ The requirement is unclear or two requirements conflict
- ☐ The change touches payments, login, permissions or private data
- ☐ The task needs real customer data, real money or a real external service
- ☐ An eval score drops by more than `[[ number ]]` points
- ☐ The agent has tried the same fix `[[ number, suggested 3 ]]` times without success
- ☐ Other: `[[ ]]`

❓ **10.6.4 Agent run log.** Where will you keep a record of each agent task (what was asked, what was done, what was reviewed)?

✍️ **Your answer:** `[[ ]]`

---

## 11. Lifecycle Phase Gates: From First Code to 500 Customers 🔴

**Why this matters:** A gate is a checkpoint. You do not move forward until the gate is passed. This stops "we'll fix it later" from becoming "customers found it."

**The six phases:**

| Phase | Name | Plain meaning |
|---|---|---|
| P0 | Plan | Decide what to test and set up tools |
| P1 | Build | Write the product and its unit tests together |
| P2 | Pre-launch | Freeze features, harden, fix, rehearse |
| P3 | Launch day | Release carefully and watch closely |
| P4 | Customers 1–50 | Watch real usage; every bug becomes a test |
| P5 | Customers 51–500 | Scale safely; keep tests healthy |

For **every phase** answer the same four questions. Tick a gate item only when you have proof (a link, a screenshot or a report).

### 11.0 Phase dates

| Phase | Start date | Planned end date | Actual end date | Gate decision (☐ Go ☐ No-Go) |
|---|---|---|---|---|
| P0 Plan | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ |
| P1 Build | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ |
| P2 Pre-launch | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ |
| P3 Launch day | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ |
| P4 Customers 1–50 | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ |
| P5 Customers 51–500 | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ |

### 11.1 Phase P0: Plan

❓ **What must be true before we start building?** *(Gate: all boxes ticked with proof)*

- ☐ Sections 0–10 of this plan are filled in and signed (Section 0.3)
- ☐ Unit inventory (4.2) lists every planned unit
- ☐ Risks (Section 5) are scored
- ☐ Test tools are installed and one sample test passes on a clean machine
- ☐ CI robot runs the sample test automatically
- ☐ AI agent rules (Section 10) are saved where agents can read them
- ☐ For AI features: 10+ draft eval examples exist

**Proof (link):** `[[ ]]` **Decision:** ☐ Go ☐ No-Go **Date:** `[[ ]]`

### 11.2 Phase P1: Build

❓ **What happens during build?**

- ☐ Every new unit gets tests **in the same change** as the code (no "tests later")
- ☐ Tests run automatically on every save to the shared code
- ☐ A change cannot be merged if any unit test fails
- ☐ Coverage reports are checked weekly
- ☐ Bugs found go into the Defect Log (Section 16) with a new test that reproduces them

❓ **Gate to leave P1** *(all must be true)*

- ☐ 100% of "Must" units in 4.2 have tests
- ☐ Pass rate is 100%
- ☐ Coverage meets targets in Section 9 (or a written, approved exception exists)
- ☐ No open Severity 1 or Severity 2 bugs
- ☐ Zero skipped or disabled tests without a written reason
- ☐ Traceability table (Section 13) is complete for all Must features
- ☐ AI evals meet the Section 7.3.3 pass score on the full example set

**Proof (link):** `[[ ]]` **Decision:** ☐ Go ☐ No-Go **Date:** `[[ ]]`

### 11.3 Phase P2: Pre-launch

❓ **What happens before launch?**

- ☐ Feature freeze: only bug fixes allowed
- ☐ Full unit suite run on a clean machine from scratch
- ☐ "Should" units have tests; remaining gaps are listed and accepted in writing
- ☐ Mutation or deliberate-break check on risk-3 units (try breaking the code; tests must fail)
- ☐ Flaky tests fixed or removed with a reason
- ☐ Eval set expanded (suggested: 100+ examples per AI feature, including nasty and hostile ones)
- ☐ Rollback plan written: how to undo the release quickly
- ☐ Test results archived for this release version

❓ **Gate to launch (Go / No-Go)** *(all must be true)*

- ☐ 100% pass rate, 0 flaky
- ☐ Coverage targets met
- ☐ 0 open Severity 1–2 bugs; Severity 3 bugs have a decision (fix / accept / later)
- ☐ Rollback plan tested once
- ☐ Performance budgets and accessibility checks (7.4) pass
- ☐ If a regulated area applies (14.3), every extra rule is adopted and evidenced
- ☐ Product owner and quality owner have both signed

**Proof (link):** `[[ ]]` **Decision:** ☐ Go ☐ No-Go **Date:** `[[ ]]`

### 11.4 Phase P3: Launch day

❓ **What happens on launch day?**

- ☐ Release only from a version where all unit tests passed
- ☐ Someone named is watching errors and AI quality during the first hours: `[[ name ]]`
- ☐ A "stop button" exists (turn off a feature or roll back) and the person watching knows how to use it
- ☐ Every production error or complaint is logged with a timestamp
- ☐ AI cost and AI failure rate are watched live

❓ **Gate to leave P3** *(within 72 hours of launch)*

- ☐ No Severity 1 incident, or one that was fixed and has a regression test
- ☐ Every launch-day bug has a new unit test or a written reason why not
- ☐ Unit suite still 100% pass after hotfixes

**Proof (link):** `[[ ]]` **Decision:** ☐ Go ☐ No-Go **Date:** `[[ ]]`

### 11.5 Phase P4: Customers 1–50

❓ **What happens while the first 50 customers arrive?**

- ☐ Every customer-reported bug becomes a failing unit test **first**, then gets fixed
- ☐ Weekly review of: bugs found by customers that unit tests missed ("escaped bugs")
- ☐ Real, anonymised AI conversations that went wrong are added to the eval set (with consent and privacy rules followed)
- ☐ Test suite speed and flaky-test count checked weekly

❓ **Gate to leave P4**

- ☐ Escaped bugs per week is falling or below target: `[[ number ]]`
- ☐ Every Severity 1–2 escaped bug has a regression test
- ☐ Eval set grew by at least `[[ number ]]` real-world examples
- ☐ No unreviewed AI-written test remains in risk-3 areas

**Proof (link):** `[[ ]]` **Decision:** ☐ Go ☐ No-Go **Date:** `[[ ]]`

### 11.6 Phase P5: Customers 51–500

❓ **What happens while growing to 500?**

- ☐ Each new feature follows the P1 → P2 mini-gate before release
- ☐ Monthly test health check (speed, flakiness, coverage drift, outdated tests)
- ☐ Re-run AI evals after **every** model, prompt or provider change
- ☐ Remove or update tests that no longer match product behaviour
- ☐ Review the risk table (Section 5) monthly

❓ **Gate to declare "500-customer milestone complete"**

- ☐ Unit pass rate 100% on every release since launch
- ☐ Coverage has not dropped below targets
- ☐ Escaped bugs below target for 4 weeks in a row
- ☐ Lessons-learned review done (Section 23)
- ☐ Plan updated to version `[[ ]]` for the next stage of growth

**Proof (link):** `[[ ]]` **Decision:** ☐ Go ☐ No-Go **Date:** `[[ ]]`

---

## 12. Entry, Exit, Suspension and Resumption Rules 🟡

**Why this matters:** These rules answer "when do we start testing, when are we done, and when do we stop?"

❓ **12.1 Entry rules: what must exist before unit testing a unit?** (tick all)

- ☐ Requirement or user story is written
- ☐ Code compiles / builds
- ☐ Test environment works
- ☐ Test data is ready
- ☐ Other: `[[ ]]`

❓ **12.2 Exit rules: when is unit testing "done" for a release?**

✍️ **Your answer** *(reuse the P2 gate list if it fits)*: `[[ ]]`

❓ **12.3 Suspension rules: when do we STOP testing and fix first?**

💡 *Example: "More than 10% of tests fail, the build is broken, the test environment is down, or a Severity 1 bug is found."*

✍️ **Your answer:** `[[ ]]`

❓ **12.4 Resumption rules: what must be fixed before we start again?**

✍️ **Your answer:** `[[ ]]`

---

## 13. Test Case Catalog and Traceability 🔴

**Why this matters:** Traceability proves every requirement has at least one test, and no test exists for no reason.

❓ **13.1 Requirement-to-test table.** One row per requirement or feature. Every "Must" requirement needs at least one test.

| Requirement ID | Requirement (plain words) | Unit ID(s) from 4.2 | Test ID(s) | Test status (☐ Written ☐ Passing) | Notes |
|---|---|---|---|---|---|
| REQ-001 | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ | `[[ ]]` |
| REQ-002 | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ ☐ | `[[ ]]` |

❓ **13.2 Test case list.** For each important test, fill one row. Use Appendix B for the long form.

| Test ID | Unit ID | What it checks | Input | Expected result | Technique (Section 6.2) | Priority | Automated? |
|---|---|---|---|---|---|---|---|
| T-001 | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ Yes ☐ No |

💡 *Example: `T-120 | U-014 | Ten percent coupon applied | price 100.00, coupon TEN | total 90.00 | Equivalence | Must | Yes`.*

---

## 14. Test Data, Privacy and Security 🔴

**Why this matters:** Tests must never leak customer information or secrets.

❓ **14.1 Answer each line.**

| Question | Your answer ✍️ |
|---|---|
| Does any test use real customer data? (must be "No") | `[[ ]]` |
| How is personal data removed or faked? | `[[ ]]` |
| Where are test secrets and keys kept? (never in the code) | `[[ ]]` |
| How are test accounts and fake cards named so they can't be confused with real ones? | `[[ ]]` |
| Who may see test results that contain sensitive examples? | `[[ ]]` |
| For AI evals: do the examples sent to the AI provider contain private data? (must be "No") | `[[ ]]` |
| Which privacy laws apply? (☐ GDPR ☐ CCPA ☐ HIPAA ☐ None ☐ Other) | `[[ ]]` |

❓ **14.2 Security checks at unit level.** Tick all that apply.

- ☐ Input validation (reject dangerous text, oversize input)
- ☐ Permission checks (user A cannot read user B's data)
- ☐ Passwords and tokens never appear in logs
- ☐ Safe handling of injection attacks (SQL, script, prompt injection)
- ☐ Rate limits and lockouts
- ☐ Other: `[[ ]]`

### 14.3 Optional: regulated-industry add-ons 🔴

**Why this matters:** Some products carry extra legal duties and extra harm if they fail. If none of the boxes below apply, tick "None" and move on.

> This section helps you plan testing. It is **not legal advice**. If any box other than "None" is ticked, ask a qualified compliance or legal professional which rules apply to you.

❓ **14.3.1 Does your product fall into any of these areas?** (tick all)

- ☐ None of these
- ☐ Health or medical (patient data, symptoms, medication, wellbeing advice)
- ☐ Finance (payments, lending, investing, accounting, insurance)
- ☐ Children or teenagers as users (or likely users)
- ☐ Education with student records
- ☐ Employment, hiring or other decisions that affect people's rights
- ☐ Other regulated area: `[[ ]]`

❓ **14.3.2 Extra unit-test rules.** For every area you ticked, the rows below are **required** (write N/A for areas you did not tick).

| Area | Extra rules to adopt | Adopted? | Your notes ✍️ |
|---|---|---|---|
| Health | Calculations and thresholds (doses, scores, alerts) have tests reviewed by a qualified person | ☐ | `[[ ]]` |
| Health | Health data is never written to logs, test reports or AI prompts sent to outside providers without a written basis | ☐ | `[[ ]]` |
| Health | AI health answers always include the required safety wording; a test fails if it is missing | ☐ | `[[ ]]` |
| Finance | Money uses exact decimal types, never floating-point; rounding rules are written down and tested at boundaries | ☐ | `[[ ]]` |
| Finance | Tests use only published test card numbers and test accounts from the payment provider | ☐ | `[[ ]]` |
| Finance | Every money-changing unit has tests for duplicates, retries and partial failures | ☐ | `[[ ]]` |
| Finance | Audit records (who, what, when) are created and cannot be edited, and tests prove it | ☐ | `[[ ]]` |
| Children | Age-gating and consent logic has tests for every branch, including "age unknown" | ☐ | `[[ ]]` |
| Children | Tracking and data collection switch off for under-age users, with tests | ☐ | `[[ ]]` |
| Children | AI output filters are evaluated with child-safety examples, reviewed by a human | ☐ | `[[ ]]` |
| All ticked areas | A second person (not the author) reviews every risk-3 test | ☐ | `[[ ]]` |
| All ticked areas | Test evidence (results, reviews, approvals) is kept for `[[ number ]]` years | ☐ | `[[ ]]` |
| All ticked areas | Full traceability (13.1) for **every** requirement, not only "Must" ones | ☐ | `[[ ]]` |

❓ **14.3.3 Who is the named compliance or legal contact?** `[[ ]]`

---

## 15. Automation and CI 🟡

**Why this matters:** Tests that nobody runs protect nothing.

❓ **15.1 When do the tests run automatically?** (tick all)

- ☐ On every save / commit on my computer
- ☐ On every shared code change (pull request)
- ☐ Before every release
- ☐ Nightly
- ☐ After every AI model or prompt change (evals)

❓ **15.2 What happens when a test fails?**

- ☐ The change is blocked from merging
- ☐ I get a message (where? `[[ ]]`)
- ☐ Other: `[[ ]]`

❓ **15.3 Who may bypass a failing test, and how is it recorded?**

💡 *Example: "Nobody. If a test is wrong, fix the test in a separate reviewed change."*

✍️ **Your answer:** `[[ ]]`

❓ **15.4 Where are results and coverage reports stored, and for how long?** `[[ ]]`

---

## 16. Defect Management 🟡

**Why this matters:** A bug that is not written down will return.

❓ **16.1 Severity scale.** Edit if needed.

| Severity | Meaning | Example | Fix deadline |
|---|---|---|---|
| 1 – Critical | Money lost, data lost, security hole, product unusable | Wrong charge | Stop everything: `[[ ]]` |
| 2 – High | Main feature broken, no workaround | Cannot log in | `[[ ]]` |
| 3 – Medium | Feature works badly, workaround exists | Wrong date format | `[[ ]]` |
| 4 – Low | Cosmetic | Typo | `[[ ]]` |

❓ **16.2 Bug rule.** Tick all you adopt (recommended: all).

- ☐ Every bug gets a written report (Appendix C)
- ☐ Every bug gets a test that fails **before** the fix and passes **after**
- ☐ Bugs are reviewed weekly
- ☐ Bugs that escaped to customers are labelled "escaped" and counted

❓ **16.3 Defect log location (link):** `[[ ]]`

---

## 17. Flaky and Broken Tests Policy 🟡

**Why this matters:** One test that randomly fails teaches everyone to ignore failures.

❓ **17.1 What happens to a flaky test?**

💡 *Example: "Quarantine it within 24 hours (moved to a separate folder, still run nightly), then fix or delete within 7 days."*

✍️ **Your answer:** `[[ ]]`

❓ **17.2 For AI evals only: a score that wobbles by a few points is normal.** What wobble is allowed before it counts as a failure? (Example: "±3 points across 5 runs.")

✍️ **Your answer:** `[[ ]]`

---

## 18. Metrics and Reporting 🟡

**Why this matters:** What you measure, you can improve.

❓ **18.1 Which numbers will you track?** (tick all; write the target)

| Metric | Track? | Target | How often reported |
|---|---|---|---|
| Unit test pass rate | ☐ | `[[ ]]` | `[[ ]]` |
| Coverage (overall and risk-3) | ☐ | `[[ ]]` | `[[ ]]` |
| Number of tests | ☐ | n/a | `[[ ]]` |
| Time to run all tests | ☐ | `[[ ]]` | `[[ ]]` |
| Flaky test count | ☐ | `[[ ]]` | `[[ ]]` |
| Bugs found before release vs. after (escaped bugs) | ☐ | `[[ ]]` | `[[ ]]` |
| Eval pass score per AI feature | ☐ | `[[ ]]` | `[[ ]]` |
| AI cost per eval run | ☐ | `[[ ]]` | `[[ ]]` |
| Time to fix a failing test | ☐ | `[[ ]]` | `[[ ]]` |

❓ **18.2 Who reads the report and what do they do with it?** `[[ ]]`

---

## 19. Roles and Responsibilities 🟡

**Why this matters:** Work with no named owner does not get done. A solo builder holds every role: write your name in each row.

| Role | Person | What they are responsible for |
|---|---|---|
| Plan owner | `[[ ]]` | Keeps this plan current |
| Test writer(s) | `[[ ]]` | Writes and maintains unit tests |
| Code reviewer | `[[ ]]` | Checks code **and** tests |
| AI-test reviewer | `[[ ]]` | Reviews tests written by AI (Section 10) |
| Eval owner | `[[ ]]` | Owns AI examples, scores and rubric |
| Release decider | `[[ ]]` | Makes the Go / No-Go call |
| Launch-day watcher | `[[ ]]` | Monitors the first hours |
| Backup person if the owner is unavailable | `[[ ]]` | Takes over |

---

## 20. Schedule and Effort 🟡

❓ **20.1 How much work will testing take?**

| Task | Estimated hours | Who | Due date |
|---|---|---|---|
| Set up tools and CI | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| Write tests for Must units | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| Write tests for Should units | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| Build AI eval set | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| Review tests (human review of AI work) | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| Pre-launch hardening | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| Launch-day monitoring | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| Weekly upkeep during P4–P5 | `[[ ]]` | `[[ ]]` | `[[ ]]` |

---

## 21. Deliverables 🟢

❓ **21.1 What will this plan produce?** Tick all and add the location.

- ☐ This plan (signed)
- ☐ Unit test code, kept in the repository: `[[ location ]]`
- ☐ Eval examples and scoring rubric: `[[ location ]]`
- ☐ Coverage report for every release: `[[ location ]]`
- ☐ Test results for every release: `[[ location ]]`
- ☐ Defect log: `[[ location ]]`
- ☐ Go / No-Go record for each gate: `[[ location ]]`
- ☐ Test summary report at the end of each phase: `[[ location ]]`
- ☐ Lessons-learned note (Section 23): `[[ location ]]`

---

## 22. Customer Feedback Loop (Customers 1–500) 🔴

**Why this matters:** Your first 500 customers will find things you never imagined. This section turns each discovery into a permanent test.

❓ **22.1 How do customer problems reach you?** (tick all)

- ☐ Support email / chat
- ☐ In-app feedback button
- ☐ Crash and error reporting tool
- ☐ App store reviews
- ☐ AI thumbs-up / thumbs-down on answers
- ☐ Other: `[[ ]]`

❓ **22.2 What is the exact path from "customer reports a problem" to "new test exists"?**

💡 *Example: "Report → log in Defect Log within 1 day → write failing test → fix → test passes → mention in weekly review."*

✍️ **Your answer:** `[[ ]]`

❓ **22.3 How do you protect privacy when turning real problems into test examples?**

✍️ **Your answer:** `[[ ]]`

---

## 23. Maintaining and Retiring Tests 🟡

❓ **23.1 How often is the test suite cleaned up?** (suggested: monthly)

✍️ **Your answer:** `[[ ]]`

❓ **23.2 When is a test deleted?**

💡 *Example: "Only when the feature it tests is removed, or the requirement changed, approved by a human and noted in the version history."*

✍️ **Your answer:** `[[ ]]`

❓ **23.3 Lessons learned (fill at the end of P3, P4, and P5).**

| Phase | What worked | What failed | What we change in this plan |
|---|---|---|---|
| P3 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| P4 | `[[ ]]` | `[[ ]]` | `[[ ]]` |
| P5 | `[[ ]]` | `[[ ]]` | `[[ ]]` |

---

## 24. Assumptions, Dependencies, Open Questions 🟢

| ID | Type (☐ Assumption ☐ Dependency ☐ Open question) | Description | Owner | Due date | Resolved? |
|---|---|---|---|---|---|
| A-01 | ☐ ☐ ☐ | `[[ ]]` | `[[ ]]` | `[[ ]]` | ☐ |

---

## 25. Final Completeness Checklist ✅

Do not approve this plan until **every** box is ticked.

**Fill-in quality**

- ☐ No `[[ ]]` remains anywhere (search the file for `[[`)
- ☐ No example text was left as an answer
- ☐ Every "TBD" has an owner and a date
- ☐ Sections that do not apply say "N/A" with a reason

**Content quality**

- ☐ Scope (4.1) states what is **not** tested
- ☐ Unit inventory (4.2) is complete and has risk ratings
- ☐ Every "Must" requirement appears in the traceability table (13.1)
- ☐ Coverage targets have numbers (Section 9)
- ☐ Every phase gate (Section 11) has dates and proof links
- ☐ AI rules (Section 10) saved where agents can read them
- ☐ AI features (if any) have a pinned model, eval set, score and cost limit (7.3.3)
- ☐ No test uses real customer data (Section 14)
- ☐ Every role in Section 19 has a name
- ☐ Performance and accessibility (7.4) answered, or marked N/A with a reason
- ☐ Agent handoffs, Definition of Done and stop-and-ask rules (10.6) are filled in
- ☐ Regulated-industry options (14.3) answered; if any area was ticked, a compliance contact is named

**Approval**

- ☐ Sign-offs in Section 0.3 are complete
- ☐ Version history (0.2) is updated
- ☐ Plan stored in the project's `Testing and Quality Assurance` folder

---
---

# APPENDICES

## Appendix A. Short Example of a Filled-In Answer

*Want to see a whole plan filled in from start to finish? Go to **Appendix F**.*

**Product:** "Bakery Orders" web + iOS app with an AI helper that suggests cake messages.

| Section | Filled example |
|---|---|
| 1.2 Must never break | "A customer is charged the wrong amount." |
| 4.2 Unit | `U-014 calculateOrderTotal | src/pricing/total.ts | Web+Backend | Risk 3 | Must` |
| 5.1 Risk | `R-01 Wrong tax | L2 × I3 = 6 | tests T-120–T-135` |
| 7.3.3 AI | 40 eval examples, pass score 90%, 3 runs each, model pinned to a named version, max $5 per run |
| 9.1 Targets | Overall 80%, risk-3 units 95% line coverage, 0 flaky |
| 10.3 Do not touch | `/src/payments/`, `/evals/pass_score.json` |

## Appendix B. Long-Form Test Case Template

Copy one block per important test.

```text
Test ID:               T-[[ ]]
Unit under test:       U-[[ ]]
Related requirement:   REQ-[[ ]]
Risk level (1-3):      [[ ]]
Title (plain words):   [[ ]]
Technique:             [[normal / boundary / equivalence / error / state / property]]
Preconditions:         [[what must be true before]]
Arrange (setup):       [[ ]]
Act (action):          [[ ]]
Expected result:       [[ ]]
Mocks used:            [[ ]]
Automated?:            [[Yes: file path / No: why]]
Last run result:       [[PASS / FAIL / date]]
Notes:                 [[ ]]
```

## Appendix C. Bug Report Template

```text
Bug ID:                BUG-[[ ]]
Date found:            [[ ]]
Found by:              [[☐ developer ☐ AI agent ☐ CI ☐ customer]]
Severity (1-4):        [[ ]]
Unit(s) affected:      U-[[ ]]
What I did:            [[steps, in order]]
What I expected:       [[ ]]
What happened instead: [[ ]]
Evidence:              [[screenshot / log / link]]
Regression test added: [[Test ID, written BEFORE the fix]]
Fixed in version:      [[ ]]
Escaped to customers?: [[Yes / No]]
```

## Appendix D. Ready-to-Use Prompts for AI Agents

**D1. Build the unit inventory**
```text
Scan the project folders. List every function, class, component and prompt
builder that contains logic. Output a table with: unit name, file path,
platform, and a suggested risk rating (1-3) with a one-line reason. Do not
write tests yet. Mark anything unclear as TBD.
```

**D2. Write tests for one unit**
```text
Write unit tests for [[UNIT]] using the Arrange-Act-Assert pattern.
Include normal, boundary, empty/missing and error cases. Use fakes for all
network, database, payment and AI calls. Follow the naming rule in Section 6.3.
Run the tests and show the result. Do not modify any other file.
```

**D3. Review AI-written tests for weakness**
```text
Review these tests. For each, tell me: what real mistake in the code would
this test catch? Flag tests that cannot fail, that repeat the code's own logic,
or that check nothing meaningful. Suggest one deliberate code break per
risky unit that should make a test fail.
```

**D4. Build AI evals**
```text
For the AI feature [[NAME]], draft 30 eval examples: 15 normal, 8 tricky,
4 hostile (prompt injection or unsafe requests), 3 empty/odd input. For each give
input, what a good answer must contain, and what it must never contain.
Mark every example "needs human approval".
```

**D5. Turn a customer bug into a test**
```text
Here is a customer bug report: [[PASTE, with personal data removed]].
Write the smallest failing unit test that reproduces it. Do not fix the code
yet. Show me the failing result first.
```

## Appendix E. Standards and Sources This Template Follows

| Source | How it is used here |
|---|---|
| IEEE 829 (test documentation), the historical test-plan section list | Plan identity, scope, items, approach, pass/fail, suspension/resumption, deliverables, schedule, risks, approvals |
| ISO/IEC/IEEE 29119-2 and -3 | Test process and documentation (plans, test cases, reports) |
| ISO/IEC/IEEE 29119-4 | Test design techniques in Section 6.2 |
| ISO/IEC TR 29119-6 | Lightweight, agile-friendly use of the plan |
| ISO/IEC TR 29119-11 | Guidance for testing AI-based systems (Section 7.3) |
| Current AI-feature testing practice (deterministic tests around the model, scored evals for model output, pinned model versions, regression sets) | Sections 7.3, 10, 17.2 |
| WCAG 2.2 and the iOS / Android touch-target guidelines | Accessibility checks in Section 7.4 |

*Standards are referenced for structure and terminology only. Check the official documents if you need formal compliance.*

## Appendix F. Complete Worked Example (A Whole Plan, Filled In)

> **How to use this appendix:** It shows what a finished plan looks like for a made-up product. Copy the *style* of the answers, never the content. All names, dates and numbers are invented. Section numbers match the template above.

**The made-up product:** *Bakery Orders*, a website and an iPhone app where customers order cakes, plus an AI helper that suggests short messages to write on the cake. One person (Sam) is building it with AI coding agents. Today in this example is 2026-10-19.

### F.0 Document control (Section 0)

| Field | Answer |
|---|---|
| Plan ID | `UTP-BAKERY-WEBIOS-001` |
| Version / status | `1.0.0` / Approved |
| Plan owner | Sam Rivera |
| Created / updated | 2026-10-19 / 2026-10-19 |
| Next review | 2026-11-16 (pre-launch gate) |
| Code location | the project's shared code repository, `main` branch |
| Results location | CI run history plus a `/reports` folder for each release |

Sign-offs: Sam Rivera signed all six roles on 2026-10-19. A friend, Priya Shah, also signed as an independent quality reviewer.

### F.1 Purpose (Section 1)

- **1.1:** "This plan makes sure every price calculation, order rule, form check and AI message helper in Bakery Orders is tested automatically before each release, so early customers never see wrong prices or broken orders."
- **1.2 Must never break:** "A customer is charged the wrong amount."
- **1.3 Success at 500 customers:** "All unit tests pass on every release. Fewer than 2 customer-reported bugs per week that a unit test could have caught. Checkout and pricing code at 95% line coverage. AI message helper scores 90% or higher on its eval set."

### F.2 Product snapshot (Section 2)

- **What it does:** "Lets customers pick a cake, choose a pickup time and pay online."
- **Platforms:** ☑ Website ☑ iOS app ☑ Backend / API ☑ Database ☐ Android
- **AI feature:** "Message Helper | suggests a 40-character cake message from the occasion and name | provider's general-purpose chat model | cannot take actions: ☑ No"
- **Stack:** "TypeScript, React, Node.js, Swift, a hosted SQL database."
- **Lifecycle style:** ☑ AI-driven: agents write most code, Sam reviews and decides.
- **Dates:** build starts 2026-10-19; feature freeze 2026-11-16; launch 2026-12-01; customer 50 expected 2026-12-22; customer 500 expected 2027-03-15.

### F.3 References (Section 3)

Requirements doc (exists, v0.3); architecture notes (exists); coding standards (does not exist: owner Sam, due 2026-10-26); integration test plan (does not exist: owner Sam, due 2026-11-02); AI usage policy (exists, one page).

### F.4 Scope and unit inventory (Section 4)

- **4.1.1 Covered:** "All code written by us in `/src`, `/app` and `/ios`, including prompt builders and AI response parsers."
- **4.1.2 Not covered:** "Payment provider internals (vendor's job). Full screen-to-screen journeys (integration plan). Visual design polish (manual review)."

| Unit ID | Unit | File | Platform | Risk | Priority |
|---|---|---|---|---|---|
| U-001 | calculateOrderTotal | src/pricing/total.ts | Web + Backend | 3 | Must |
| U-002 | applyCoupon | src/pricing/coupon.ts | Web + Backend | 3 | Must |
| U-003 | calculateTax | src/pricing/tax.ts | Backend | 3 | Must |
| U-004 | validatePickupTime | src/orders/pickup.ts | Web + Backend | 2 | Must |
| U-005 | validateEmail | src/forms/email.ts | Web | 1 | Should |
| U-006 | OrderViewModel | ios/Orders/OrderViewModel.swift | iOS | 2 | Must |
| U-007 | OfflineOrderQueue | ios/Sync/OfflineQueue.swift | iOS | 3 | Must |
| U-008 | buildMessagePrompt | src/ai/prompt.ts | AI | 2 | Must |
| U-009 | parseMessageReply | src/ai/parse.ts | AI | 2 | Must |
| U-010 | blockUnsafeMessage | src/ai/safety.ts | AI | 3 | Must |

### F.5 Risks (Section 5)

| ID | What could go wrong | L | I | Score | Reduced by |
|---|---|---|---|---|---|
| R-01 | Wrong total or tax charged | 2 | 3 | 6 | U-001, U-002, U-003 |
| R-02 | Pickup time accepted when bakery is closed | 2 | 2 | 4 | U-004 |
| R-03 | Offline order lost or sent twice | 2 | 3 | 6 | U-007 |
| R-04 | AI suggests a rude or unsafe message | 2 | 3 | 6 | U-010, evals |
| R-05 | AI cost spirals | 1 | 2 | 2 | prompt-size budget, call limiter |
| R-06 | Time-zone mix-up on pickup | 2 | 2 | 4 | U-004 |

### F.6 Approach (Section 6)

- **Unit test rules ticked:** one unit at a time; under 1 second; no real network, database, payment or AI; same answer every run; any order; cleans up.
- **Not a unit test:** "Anything that opens a browser, calls the real AI or needs a network lives in `/tests/integration` or `/evals`."
- **Techniques:** normal, boundary, equivalence, error, null/empty, decision table (coupon rules), state changes (order status), property-based (pricing never negative).
- **Structure:** Arrange → Act → Assert.
- **Naming rule:** `unit_condition_expectedResult`, for example `applyCoupon_expiredCode_returnsError`.
- **Location:** TypeScript tests beside the code as `*.test.ts`; Swift tests in the `OrdersTests` target.
- **Mocks:** database → in-memory fake; payment → provider's test mode stub; email → recorder fake; clock → fixed test clock; AI model → scripted fake replies.
- **Test data:** hand-written samples and generated fake data; ☑ never real customer data.

### F.7 Platform details (Section 7)

- **7.1 Web:** pure functions, form validation, API handlers, accessibility rules on components. Browsers: latest two versions of Chrome, Safari, Firefox.
- **7.2 Mobile:** view models, offline queue, local storage upgrade logic. Support: iOS 17+, iPhone only.
- **7.3.1 AI Part A:** prompt builder, reply parser, JSON format check, safety blocklist, retry and timeout, token limiter, "AI can never place an order" guard.
- **7.3.2 AI Part B:** on-topic, no made-up details, 40-character limit, refuses rude requests, resists "ignore your instructions" tricks, reworded-question check.

| 7.3.3 Question | Answer |
|---|---|
| Eval examples at launch | 40 (15 normal, 10 tricky, 8 hostile, 7 odd input) |
| Who writes and approves | AI drafts; Sam approves each one |
| Pass score | 90% |
| Runs per example | 3 |
| Pinned model | the exact provider model version recorded in `/evals/config.json` |
| Judge model and rubric | A separate model version with a rubric in `/evals/rubric.md`; Sam spot-checks 10% of scores |
| Where stored | `/evals` folder in version control |
| Max spend per eval run | $5 |
| When the vendor updates the model | Pin stays; run the full eval on the new version in a test branch; switch only if the score is at least 90% |

**7.4 Performance and accessibility:**
- Time budget: pricing functions under 50 ms typical, under 500 ms on a 10,000-line order.
- Query-count check: the "my orders" API call must make no more than 3 fake-database queries.
- AI prompt must not exceed 600 tokens; one AI call per click, maximum.
- Accessibility target: WCAG 2.2 Level AA. Unit tests check labels, roles, contrast pairs in the design settings (4.5:1) and 44-point touch targets.
- Human check: Priya tests the iPhone app with the screen reader before the pre-launch gate.

### F.8 Tools (Section 8)

Jest (TypeScript), XCTest (Swift), Testing Library (components), Istanbul (coverage), Promptfoo (evals), GitHub Actions (CI), GitHub Issues (bugs). **Run all tests:** `npm test`. **Run one test:** `npm test -- total.test.ts`. Secrets live in the CI vault, never in code.

### F.9 Quality targets (Section 9)

| Measure | Target | Reason |
|---|---|---|
| Pass rate | 100% | No exceptions |
| Line coverage, all code | 80% | Strong but realistic for one builder |
| Line coverage, risk-3 units | 95% | Money, offline orders and safety |
| Branch coverage, risk-3 | 90% | Every `if` in money code is run |
| Max run time | 3 minutes | Fast enough to run on every save |
| Flaky tests | 0 | One flaky test teaches people to ignore failures |
| AI eval score | 90% | Matches Section 7.3.3 |

### F.10 AI agents (Section 10)

- **Agents:** a coding agent (writes code and tests) and a review agent (looks for weak tests).
- **Rules ticked:** all of 10.2.
- **Do not touch:** `/src/payments/`, `/evals/pass_score.json`, `/evals/rubric.md`, `Unit_Testing_Plan.md`.
- **Human always reviews:** risk-3 tests, coverage-target changes, eval examples, any deleted or skipped test, mocks of payment, security and AI.
- **Stop and ask:** a test fails and the "fix" would be to change the test; the task touches payments or private data; an eval score drops by more than 3 points; the same fix has failed 3 times.
- **Run log:** `/reports/agent-log.md`, one entry per agent task.

### F.11 Phase gates (Section 11)

| Phase | Planned end | Key gate evidence |
|---|---|---|
| P0 Plan | 2026-10-23 | Plan signed, sample test passing in CI, 12 draft eval examples |
| P1 Build | 2026-11-16 | All 9 Must units tested, 100% pass, coverage targets met, eval score 93% |
| P2 Pre-launch | 2026-11-27 | 100+ eval examples, deliberate-break check on U-001 to U-003, U-007, U-010; rollback rehearsed; Priya's accessibility check done |
| P3 Launch day | 2026-12-04 | Launch log, no Severity 1 incident, every launch bug has a test |
| P4 Customers 1–50 | 2026-12-22 | Escaped bugs below 3 per week; 15 real-world cases added to evals |
| P5 Customers 51–500 | 2027-03-15 | 100% pass on every release, coverage held, four weeks below target for escaped bugs, lessons learned recorded |

### F.12 Entry / exit / suspension (Section 12)

- **Entry:** requirement written, code builds, test data ready.
- **Exit:** the P2 gate list is satisfied.
- **Suspension:** "More than 10% of tests failing, a broken build, or a Severity 1 bug."
- **Resumption:** "Build is green and the Severity 1 bug has a failing test and a fix."

### F.13 Traceability (Section 13)

| Requirement | Plain words | Unit | Tests | Status |
|---|---|---|---|---|
| REQ-001 | Customer sees the correct total with tax | U-001, U-003 | T-001 to T-014 | Written, passing |
| REQ-002 | A valid coupon lowers the price; an expired one is refused | U-002 | T-020 to T-031 | Written, passing |
| REQ-003 | Pickup only during opening hours, in the bakery's time zone | U-004 | T-040 to T-049 | Written, passing |
| REQ-004 | An order placed offline is sent once when the network returns | U-007 | T-060 to T-068 | Written, passing |
| REQ-005 | AI cake messages are short, polite and safe | U-008, U-009, U-010 | T-080 to T-095, evals E-001 to E-040 | Written, passing |

Sample test row: `T-020 | U-002 | Ten percent coupon applied | price 100.00, code TEN | total 90.00 | Equivalence | Must | Automated`.

### F.14 Privacy and security (Section 14)

No test uses real customer data. Fake customers use names like "Test Customer 001" and emails ending in `@example.test`. Payment tests use only the provider's published test cards. Eval examples never contain real names. Applicable privacy law: GDPR. Regulated areas (14.3): ☑ None. Security checks ticked: input validation, permission checks, no passwords in logs, prompt-injection handling.

### F.15 – F.19 Automation, defects, flaky tests, metrics, roles

- **CI:** tests run on every commit and every shared code change; evals run after any prompt or model change; a failing test blocks merging. Nobody may bypass a failing test; a wrong test is fixed in a separate reviewed change. Results are kept for 12 months.
- **Severity deadlines:** Severity 1 same day; Severity 2 within 2 days; Severity 3 within 2 weeks; Severity 4 when convenient.
- **Flaky policy:** quarantined within 24 hours, fixed or deleted within 7 days. AI eval wobble allowed: ±3 points across 5 runs.
- **Metrics reported weekly:** pass rate, coverage, run time, flaky count, escaped bugs, eval score and cost.
- **Roles:** Sam is plan owner, test writer, eval owner, release decider and launch-day watcher. Priya is code reviewer for risk-3 tests and backup person.

### F.20 – F.24 Schedule, deliverables, feedback loop, upkeep, assumptions

- **Effort (hours):** tooling and CI 6; Must-unit tests 24; Should-unit tests 8; eval set 10; human review 12; pre-launch hardening 16; launch-day monitoring 8; weekly upkeep 3 per week.
- **Deliverables:** signed plan, test code, eval set, coverage report and test results per release, defect log, Go / No-Go record per gate, phase summary reports, lessons-learned note.
- **Feedback loop:** support email and in-app feedback button feed one inbox. Path: report → logged within 1 day → failing test written → fix → test passes → weekly review. Real AI conversations are added to evals only after removing names and contact details and with the customer's consent.
- **Upkeep:** monthly clean-up; a test is deleted only when its feature is removed or its requirement changes, with a human note in the version history.
- **Assumption A-01:** "The AI provider keeps the pinned model version available until at least 2027-03-31." Owner: Sam. Due: 2026-11-30.

---

**END OF DOCUMENT.** Template version 1.1.0 (Draft). Keep the `Template version` line at the top unchanged in project copies, and track your own changes in Section 0.2.
