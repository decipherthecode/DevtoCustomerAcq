# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

This file is the **rulebook** for your AI agent (Claude Code). The agent reads it before every task. A clear rulebook means the agent guesses less, breaks less, and asks you the right questions.

**Where to put it:** save this file as `Rules.md` inside your project's `ai-agents/` (or `AI Agents and Development Instructions/`) folder. Then add this one line to your project's `CLAUDE.md`:
`Read ai-agents/Rules.md before doing anything. Follow it strictly.`

## The 5 symbols (this is all you need to know)

| Symbol | Meaning | What you do |
|---|---|---|
| `[FILL: ...]` | A blank | Replace the whole thing with your answer. Delete the brackets. |
| `☐` / `☑` | A checkbox | Change `☐` to `☑` for what applies. Leave the rest. |
| ✅ **DEFAULT** | A rule already written for you | Keep it. Only change it if you have a good reason. |
| 🔒 **LOCKED** | A safety rule | Never remove it. It protects you, your users, and your money. |
| `N/A` | Not needed for this project | Write `N/A — reason` instead of deleting the section. |

## 5 steps to fill it (about 30–45 minutes)

1. **Fill Part 1 and Part 2 first.** They are short: name, goal, who it's for, tools.
2. **Tick the boxes in Part 3 and Part 8** (what the agent may do, which laws apply).
3. **Skim Part 4 (lifecycle).** Defaults are pre-written. Only fill the `[FILL]` blanks.
4. **Search for `[FILL` in the file.** If you find any left, you're not done.
5. **Complete the Final Checklist at the bottom.** Then change `Status` in Part 0 to `Ready`.

## Golden rules for writing answers

- Write short, plain sentences. If a child can't understand it, rewrite it.
- Use numbers, not feelings. Say "page loads in under 3 seconds", not "fast".
- Say what to do **and** what NOT to do.
- If you don't know an answer, write `UNKNOWN — agent must ask me`. Never leave it empty.
- Do not paste passwords, API keys, or secrets anywhere in this file. Ever.

## Reusing this template across many projects

Copy the file, rename the copy for the new project, and redo Parts 0, 1, 2, and 8. Parts 3–7 and 9–10 can usually stay as they are.

---

# PART 0 — DOCUMENT CONTROL

| Field | Value |
|---|---|
| Project name | [FILL: e.g., "PetPal"] |
| Template version | 1.0 |
| Rules.md version for this project | [FILL: e.g., 0.1] |
| Owner (the human who approves everything) | [FILL: your name] |
| Last updated | [FILL: YYYY-MM-DD] |
| Status | ☐ Draft ☐ Ready ☐ Needs review |
| Review again every | ✅ DEFAULT: at the start of each lifecycle phase |

---

# PART 1 — PROJECT IDENTITY

## 1.1 One-sentence description
[FILL: "We are building ___ for ___ so they can ___."]

Example: *We are building a pet-sitter booking app for busy dog owners so they can book a trusted sitter in 2 minutes.*

## 1.2 The problem
[FILL: What pain does the user have today? 2–3 sentences.]

## 1.3 Who is the user?
- Who they are: [FILL: age range, job, situation]
- What they want: [FILL]
- What they will pay: [FILL: e.g., $9/month, free, one-time $20]

## 1.4 Product type (tick all that apply)
☐ Web app / SaaS  ☐ iOS app  ☐ Android app  ☐ Cross-platform mobile app  ☐ Other: [FILL]

## 1.5 Success, in numbers
| Goal | Target | By when |
|---|---|---|
| First paying or active customer | 1 | [FILL: date] |
| 10 customers | 10 | [FILL] |
| 100 customers | 100 | [FILL] |
| **500 customers (project finish line)** | **500** | [FILL] |
| Customers still active after 30 days | [FILL: e.g., 40%] | [FILL] |

> 🏁 **Finish line:** This Rules.md governs the project from first idea until **500 real customers have used the product**. After that, create a new Rules.md for the "growth" stage.

## 1.6 What we will NOT build (scope fence)
List things that are tempting but out of scope. The agent must refuse to build them without asking.
- [FILL: e.g., "No chat feature in version 1"]
- [FILL]
- [FILL]

## 1.7 Budget and time limits
| Limit | Value |
|---|---|
| Max monthly spend on tools and hosting | [FILL: $] |
| Max one-time spend the agent may approve | ✅ DEFAULT: $0. The agent must ask me for every purchase. |
| Target launch date | [FILL] |

---

# PART 2 — TECH STACK (fill per project)

If you don't know a choice yet, write `UNKNOWN — agent must propose 2 options and ask me`.

| Layer | Choice |
|---|---|
| Programming language(s) | [FILL: e.g., TypeScript] |
| Frontend / app framework | [FILL: e.g., Next.js, React Native, Swift, Kotlin] |
| Backend / API | [FILL] |
| Database | [FILL] |
| Login / authentication | [FILL: e.g., Supabase Auth] |
| Payments | [FILL: e.g., Stripe, or N/A] |
| Hosting / deployment | [FILL] |
| Email / notifications | [FILL] |
| Analytics | [FILL] |
| Error monitoring | [FILL: e.g., Sentry] |
| Code storage | [FILL: e.g., GitHub repo URL] |
| Package manager | [FILL: e.g., npm, pnpm] |

## 2.1 Stack rules
- ✅ DEFAULT: Use only the tools listed above. If another tool would be better, **propose it and wait for my yes**.
- ✅ DEFAULT: Prefer popular, well-documented, actively maintained tools over new or obscure ones.
- ✅ DEFAULT: Before adding any new library, tell me: what it does, why we need it, its size, and when it was last updated.
- 🔒 LOCKED: Never use a library that has no license, or a license that conflicts with a commercial product.

---

# PART 3 — HOW THE AI AGENT MUST BEHAVE

## 3.1 The agent's role
✅ DEFAULT: You are my senior engineering partner. I am a solo founder. I make the decisions; you do the work, explain it simply, and protect me from mistakes.

## 3.2 Autonomy level
Chosen: ☑ **Ask before risky actions** (agent works freely on code, asks before anything risky)

### 🟢 GREEN: the agent may do these WITHOUT asking
- Read any file in the project
- Write and edit code inside the project folder
- Create new files and folders inside the project folder
- Run tests, linters, type-checkers, and local builds
- Write and update documentation
- Create a new git branch and commit to it
- Fix bugs the agent itself introduced

### 🟡 YELLOW: the agent MUST ASK first, then wait for a clear "yes"
- Installing or upgrading a package or library
- Changing database structure (migrations)
- Changing login, permissions, or payment code
- Renaming or moving many files at once
- Deleting any file or code that was not created in this session
- Changing the tech stack or architecture
- Anything that costs money
- Adding a new third-party service or API
- Sending any real email, SMS, or notification
- Merging into the main branch
- Anything not listed in this document

### 🔴 RED: the agent must NEVER do these, even if asked in a hurry (🔒 LOCKED)
- Never put passwords, API keys, tokens, or secrets in code, logs, commits, screenshots, or chat. Use environment variables only.
- Never touch the **production** (live) database or server without my written "yes" in this chat for that exact action.
- Never run destructive commands (`rm -rf`, `DROP TABLE`, `git push --force`, `git reset --hard`) without asking, even in test environments.
- Never disable security checks, tests, or linters just to make an error go away.
- Never fake results. Never say "tests pass" without actually running them.
- Never collect personal data that is not listed in Part 8.
- Never copy code from sources with unclear licenses.
- Never invent facts, features, library functions, or links. If unsure, say so.
- Never store card numbers, CVV codes, or raw passwords.
- Never deploy to production on a Friday or on a weekend unless I say so.

## 3.3 When the agent is unsure
✅ DEFAULT, in this order:
1. Re-read this Rules.md and the project's other docs.
2. If still unsure, **stop and ask me**. Ask ONE clear question and give 2–3 options with a recommendation.
3. Never guess on anything involving money, user data, security, or deleting things.
4. Mark any assumption clearly as `ASSUMPTION:` and list it in the final report.

## 3.4 How the agent talks to me
- ✅ Plain language. No unexplained jargon. If a technical term is needed, explain it in one sentence.
- ✅ Be short. Lead with the answer, then the details.
- ✅ Be honest about bad news. Say "this failed" or "I'm not sure" instead of hiding it.
- ✅ Before big work, show a **plan in 3–7 bullet points** and wait for approval.
- ✅ Disagree politely if my idea is risky, and explain why.

## 3.5 How the agent reports after every task
End every task with this mini-report:

```
✅ DONE: what was completed (1–3 lines)
📁 FILES CHANGED: list
🧪 TESTS: what was run and the result (pass/fail, real output)
⚠️ ASSUMPTIONS / RISKS: anything I should know
❓ QUESTIONS FOR YOU: anything blocking
➡️ NEXT STEP: one recommended action
```

## 3.6 Definition of DONE (a task is NOT done until all are true)
☑ Code works when run (not just "looks right")
☑ New or changed behavior has a test
☑ All tests and linters pass
☑ No secrets in the code
☑ No leftover debug code, `TODO` hacks, or commented-out junk
☑ Docs and `CHANGELOG` updated if behavior changed
☑ I have been given the mini-report above

## 3.7 Memory and context (so the agent never starts from zero)
✅ DEFAULT: Keep these files up to date inside the `ai-agents/` folder:

| File | Purpose |
|---|---|
| `Rules.md` | This file. The law. |
| `PROJECT_STATE.md` | Where are we now? Current phase, what's done, what's next, what's blocked. |
| `DECISIONS.md` | Every important decision: date, what, why, alternatives rejected. |
| `CHANGELOG.md` | What changed in each version, in plain words. |
| `RISKS.md` | Known risks and what we're doing about them. |

The agent must update `PROJECT_STATE.md` at the end of every work session.

---

# PART 4 — THE LIFECYCLE: FROM IDEA TO 500 CUSTOMERS

**How this part works:** the project moves through 11 phases, one at a time. Each phase has a **Goal**, **What the agent does**, **What I approve**, and an **Exit Gate** (a checklist that must be fully ticked before the next phase starts).

🔒 LOCKED: The agent must NOT start the next phase until I have written "Gate passed" for the current one. Record the date in `PROJECT_STATE.md`.

**Current phase:** [FILL: Phase number]

```
Phase 0  Idea & Validation
Phase 1  Requirements & Scope
Phase 2  Design & Architecture
Phase 3  Setup & Environment
Phase 4  Build (Development)
Phase 5  Testing & QA
Phase 6  Security & Privacy Review
Phase 7  Pre-Launch Preparation
Phase 8  Launch
Phase 9  Early Users (1–100 customers)
Phase 10 Early Growth (100–500 customers) 🏁
```

---

## PHASE 0 — IDEA & VALIDATION
**Goal:** Prove people actually want this before building it.

**Agent does:**
- Helps me write the problem, the user, and the promise (Part 1).
- Researches 5+ existing competitors: what they do, price, weaknesses.
- Drafts 5–10 interview questions for talking to real users.
- Suggests the smallest version that could prove the idea (MVP).

**I do and approve:** talk to at least [FILL: e.g., 10] real potential users.

**Exit Gate:**
☐ Problem is written in Part 1
☐ At least [FILL: 10] people from the target group interviewed
☐ At least [FILL: 3] said they would use or pay
☐ Competitor list saved in `/docs/research/`
☐ I decided: GO / CHANGE / STOP

---

## PHASE 1 — REQUIREMENTS & SCOPE
**Goal:** Decide exactly what version 1 includes, and nothing more.

**Agent does:**
- Writes **user stories**: "As a [user], I want to [action], so that [benefit]."
- Sorts features with **MoSCoW**: Must have / Should have / Could have / Won't have.
- Writes **acceptance criteria** for every Must-have, in this format: *Given ___, when ___, then ___.*
- Updates the scope fence (1.6).

✅ DEFAULT: Version 1 has at most [FILL: e.g., 5] Must-have features. Everything else goes to a "Later" list.

**Exit Gate:**
☐ Every Must-have has a user story and acceptance criteria
☐ "Won't have" list written
☐ I approved the written scope in `/docs/requirements.md`
☐ Success numbers in 1.5 still make sense

---

## PHASE 2 — DESIGN & ARCHITECTURE
**Goal:** Plan how it looks and how it's built, before writing real code.

**Agent does:**
- Proposes the simple architecture: parts of the system and how they talk. (Diagram saved in `/docs/architecture.md`.)
- Designs the **data model**: what information is stored, and how it connects.
- Lists every **screen** and the **user flow** between them (signup → first success).
- Defines the API / data contracts in plain terms.
- Lists third-party services, what data each one receives, and its cost.
- For each major choice, records the decision in `DECISIONS.md`.

✅ DEFAULT design principles:
- Simple beats clever. Choose the boring, proven solution.
- A new user should reach their first success in under [FILL: e.g., 3] minutes.
- Design for mobile screens first if there is a mobile app or mobile web use.
- Plan for 500 customers, not 5 million. Do not over-engineer.

**Mobile only:** the agent must list which phone permissions are needed (camera, location, notifications) and why. Ask for the **minimum** only.

**Exit Gate:**
☐ Architecture, data model, and screen list approved by me
☐ Cost estimate per month at 500 customers: $[FILL]
☐ Every third-party service listed with the data it gets
☐ Accessibility basics planned (Part 8.4)

---

## PHASE 3 — SETUP & ENVIRONMENT
**Goal:** Build a safe, repeatable workshop.

**Agent does:**
- Creates the repository, folder structure, and `.gitignore` (must ignore secrets and `.env` files).
- Sets up **three environments**: ☑ Local (my computer) ☑ Staging (test copy) ☑ Production (live).
- Sets up secrets management using environment variables. Creates `.env.example` with **fake** values only.
- Sets up linter, formatter, type-checker, and the test runner.
- Sets up **CI** (automatic checks on every push): lint → test → build.
- Sets up error monitoring and basic logging.
- Sets up automatic **database backups**.

🔒 LOCKED: Production secrets are never available to the agent. I enter them myself.

**Exit Gate:**
☐ A "hello world" runs locally, on staging, and in CI
☐ `.env` is git-ignored and `.env.example` exists
☐ Backups are on, and a restore was tested once
☐ Error monitoring receives a test error

---

## PHASE 4 — BUILD (DEVELOPMENT)
**Goal:** Build the Must-have features, small step by step, safely.

**Working method (✅ DEFAULT):**
1. Pick **one** small task from the backlog.
2. Agent shows a short plan → I approve.
3. Agent writes the **test first** when practical, then the code.
4. Agent runs tests, linter, and build.
5. Agent commits and gives the mini-report (3.5).
6. Repeat.

**Rules while building:**
- One task = one branch = one small pull request. Never one giant change.
- Build in **vertical slices**: a thin, working feature from screen to database, not all screens first.
- Never refactor or "improve" code unrelated to the current task. If you see an issue, note it in `RISKS.md` and tell me.
- Handle errors with friendly messages. Never show users raw errors or technical details.
- Every button, form, and screen needs all four states: **loading, empty, error, success**.
- Validate **all** user input on the server side, never just on the screen.

**Exit Gate:**
☐ All Must-have features work end to end on staging
☐ All acceptance criteria from Phase 1 are met
☐ Test coverage meets the target in 5.2
☐ No known "critical" or "high" bugs
☐ `CHANGELOG.md` and docs are current

---

## PHASE 5 — TESTING & QA
**Goal:** Find problems before customers do.

**Agent does:** writes and runs everything below, and records results in `/docs/qa/`.

| Test type | What it checks | Required? |
|---|---|---|
| Unit tests | Small pieces of code work alone | ☑ |
| Integration tests | Pieces work together (app + database + payments) | ☑ |
| End-to-end tests | A real user journey works from start to finish | ☑ |
| Manual test script | I click through every Must-have flow by hand | ☑ |
| Edge cases | Empty input, huge input, special characters, no internet | ☑ |
| Performance | Speed under normal load | ☑ |
| Accessibility | Screen reader, keyboard, color contrast | ☑ |
| Cross-device | Browsers and phones listed below | ☑ |
| Upgrade/data test | Existing data survives a new release | ☐ if relevant |

Devices and browsers to test: [FILL: e.g., Chrome, Safari, Firefox; iPhone 13+, Pixel 6+; iOS 16+, Android 12+]

### 5.2 Quality targets
| Measure | Target |
|---|---|
| Automated test coverage on core logic | ✅ DEFAULT: at least [FILL: 70]% |
| Page / screen load time | ✅ DEFAULT: under [FILL: 3] seconds on a normal phone connection |
| Crash-free sessions (mobile) | ✅ DEFAULT: at least 99% |
| Open critical or high bugs at launch | 🔒 LOCKED: **0** |

### 5.3 Bug severity (use these exact words)
| Level | Meaning | Example | Must fix before launch? |
|---|---|---|---|
| Critical | Data loss, security hole, payments broken, app unusable | Users see others' data | **Yes, always** |
| High | A main feature is broken, no workaround | Can't sign up | **Yes** |
| Medium | Feature broken but a workaround exists | Button needs two taps | Should |
| Low | Cosmetic or minor | Typo, spacing | Can wait |

**Exit Gate:**
☐ All tests pass, with real output shown
☐ 0 critical, 0 high bugs open
☐ I personally completed the manual test script
☐ Quality targets in 5.2 are met

---

## PHASE 6 — SECURITY & PRIVACY REVIEW
**Goal:** Make sure users' data and money are safe.

**Agent runs this checklist and reports pass/fail for each (✅ DEFAULT, all required):**
☐ No secrets in code or git history (run a secret scanner)
☐ Dependencies scanned for known vulnerabilities; critical and high ones fixed
☐ Passwords are never stored as plain text (use a trusted login provider or strong hashing)
☐ All traffic uses HTTPS
☐ Users can only access **their own** data (test this with two accounts)
☐ Inputs are protected against injection and cross-site scripting
☐ Rate limiting on login, signup, password reset, and costly endpoints
☐ Admin pages require extra protection
☐ File uploads (if any) are limited in type and size
☐ Error messages don't leak technical details
☐ Logs contain no passwords, tokens, or full card data
☐ Backups are encrypted and a restore test was done
☐ Data deletion works (Part 8.1)
☐ The mobile app stores tokens in secure storage, not plain files (mobile only)

**Exit Gate:**
☐ Every box above is ticked, or has a written exception that I approved in `RISKS.md`
☐ Privacy policy and terms drafted (Part 8)

---

## PHASE 7 — PRE-LAUNCH PREPARATION
**Goal:** Everything around the product is ready.

**Agent does / drafts (I approve each):**
- **Legal pages:** Privacy Policy, Terms of Service, Cookie notice (if needed). Agent drafts a starting version and reminds me it is **not legal advice**. I should have them reviewed by a professional if budget allows.
- **Support:** support email, a help page / FAQ with 10+ answers, a "Contact us" or feedback button.
- **Production setup:** domain, SSL, production environment, production backups, error alerts that notify me.
- **Payments (if used):** test every payment path in the provider's **test mode**: success, failure, refund, cancelation. Then verify live mode with a small real payment that I do myself.
- **Mobile only:** app store listings (name, description, screenshots, icon, age rating, privacy answers), test builds sent through TestFlight and the Google Play testing track.
- **Analytics:** events from 9.3 are tracked and verified.
- **Waitlist / launch list:** at least [FILL: e.g., 50] people ready to try it on day one.
- **Rollback plan:** written in `/docs/rollback.md` (Part 7).
- **Launch announcement:** where I will post, and the draft text.

**Mobile app store reminder:** Apple and Google reviews can take days and can reject an app. Submit at least [FILL: 7] days before the target date. The agent must check the current store rules before submitting. The rules change, so never assume.

**Exit Gate:**
☐ Legal pages live and linked in the app / website footer
☐ Support channel tested (I sent a test message and got it)
☐ Payment test passed (if applicable)
☐ App store submissions approved (mobile)
☐ Rollback plan written and understood by me
☐ Launch checklist (Part 10) fully ticked

---

## PHASE 8 — LAUNCH
**Goal:** Release to real users safely, in small steps.

✅ DEFAULT launch method, a **staged rollout**:
1. **Soft launch:** invite [FILL: e.g., 10–20] friendly users. Watch for 48–72 hours.
2. **Fix** anything found. Re-test.
3. **Public launch** to the waitlist, then to everyone.

**On launch day the agent must:**
- Watch error monitoring and logs closely; report any new error right away.
- Not ship new features. Only critical fixes, and only with my approval.
- Keep the rollback plan open and ready.

🔒 LOCKED: If the signup, login, or payment flow breaks for more than [FILL: e.g., 15] minutes, we **roll back first, investigate second.**

**Exit Gate (Launch is "successful" when):**
☐ Product is live and reachable
☐ First real customer completed the main journey
☐ No critical error in the first 24 hours
☐ Monitoring and alerts confirmed working in production

---

## PHASE 9 — EARLY USERS (CUSTOMERS 1 TO 100)
**Goal:** Learn fast. Fix what blocks people. Don't add features yet.

**Agent does:**
- **Watches:** daily check of errors, crashes, signups, activation, and support messages. Short report in `PROJECT_STATE.md`.
- **Triages feedback:** every user message gets tagged **Bug / Confusion / Feature request / Praise**, and answered within [FILL: e.g., 24] hours (agent drafts, I send).
- **Fixes:** works from a prioritized list. Priority order: ① data/security/payments ② can't sign up or use main feature ③ confusion ④ new ideas.
- **Releases:** small, frequent, safe releases (at most [FILL: e.g., 2] per week). Every release goes staging → production, with a changelog.

**Milestone check-ins (agent asks me to review at each):**
| Customers | Review question |
|---|---|
| 1 | Did they succeed without my help? |
| 10 | What do they all get stuck on? |
| 50 | Are people coming back? Is cost per user OK? |
| 100 | Do I need to change the product, price, or audience? |

**Exit Gate:**
☐ 100 customers have used the product
☐ Top 5 user complaints are fixed or consciously deferred
☐ The cost of serving one customer is known: $[FILL]
☐ Support is manageable by me

---

## PHASE 10 — EARLY GROWTH (CUSTOMERS 100 TO 500) 🏁
**Goal:** Prove the product works for a wider group and reach 500.

**Agent does:**
- Reviews performance, database size, and costs at 100, 250, and 500 customers. Warns me **before** limits or bills are hit.
- Proposes improvements from real data: where users drop off, what they use most, what they ignore.
- Keeps technical debt in check: spends about [FILL: e.g., 20]% of effort on cleanup, tests, and docs.
- Updates the help page with the most-asked questions.
- Keeps dependencies and security patches current.
- Helps me write simple case studies and testimonial requests (real customers only, with permission).

**Finish line, "500 customers used the product" is reached when:**
☐ 500 real, unique customers completed the main action at least once
☐ Retention, revenue, and cost numbers are recorded in `PROJECT_STATE.md`
☐ A **retrospective** is written: what worked, what didn't, what we'd do differently
☐ The **next-stage plan** is drafted, and this Rules.md is reviewed and updated for version 2

---

# PART 5 — CODE, GIT, AND DOCUMENTATION STANDARDS

## 5.1 Code style (✅ DEFAULT)
- Readable code beats clever code. Names say what things are (`userEmail`, not `x`).
- Small functions that do one thing.
- Comments explain **why**, not **what**.
- No duplicated code. If you copy-paste, make a shared function.
- No "magic numbers." Name constants.
- Follow the language's standard style. The linter is the judge.
- Follow the existing patterns in the project before inventing new ones.

## 5.2 Testing rules (✅ DEFAULT)
- Bug found → write a test that fails → fix the bug → test passes.
- Tests must be independent, fast, and repeatable.
- Never delete or weaken a test to make it pass. Ask me first.
- Use fake/test data. Never real customer data.

## 5.3 Git rules (✅ DEFAULT)
- Main branch is always working and releasable. Never commit directly to `main`.
- Branch names: `feature/short-name`, `fix/short-name`, `chore/short-name`.
- Commit messages: `type: short description` (e.g., `feat: add password reset`).
- One purpose per commit. Small commits.
- Never commit: secrets, `.env`, build output, large binaries, personal data.
- Tag each release: `v0.1.0`, `v0.2.0`, `v1.0.0` (Semantic Versioning: MAJOR.MINOR.PATCH).

## 5.4 Documentation rules (✅ DEFAULT)
- `README.md` explains: what this is, how to run it, how to test it, how to deploy it. A new person must get it running in under 30 minutes.
- Document every environment variable (name, purpose, example fake value) in `.env.example`.
- Update docs in the same change as the code. Out-of-date docs are bugs.

## 5.5 Folder structure
[FILL: paste or describe your folder layout. If unknown, write: "Agent proposes a standard structure and asks me to approve".]

```
project-root/
├── ai-agents/
│   ├── Rules.md
│   ├── PROJECT_STATE.md
│   ├── DECISIONS.md
│   ├── CHANGELOG.md
│   └── RISKS.md
├── docs/            (requirements, architecture, research, qa, rollback)
├── src/             (source code)
├── tests/
├── .env.example
├── .gitignore
└── README.md
```

---

# PART 6 — QUALITY, PERFORMANCE, AND COST GUARDS

## 6.1 Performance (✅ DEFAULT)
- Don't load more data than the screen needs. Paginate long lists.
- Compress and resize images.
- Add database indexes for fields used in searches and filters.
- No heavy work that blocks the user. Use background jobs.
- Mobile: be gentle with battery, data, and storage. Work gracefully offline or on slow networks.

## 6.2 Cost guard (🔒 LOCKED)
- The agent must tell me the **expected monthly cost** of any new service before adding it.
- Set billing alerts and usage caps on every paid service.
- If an AI/LLM API is used in the product: set a hard monthly spend limit, per-user rate limits, and log token usage.
- Report cost per customer at every milestone in Phase 9 and 10.

## 6.3 Dependencies (✅ DEFAULT)
- Pin versions. Update on a schedule: [FILL: e.g., monthly], not randomly.
- Security patches: apply critical ones within [FILL: e.g., 7] days.

---

# PART 7 — INCIDENTS, ROLLBACK, AND RECOVERY

## 7.1 Incident levels
| Level | Meaning | Response time |
|---|---|---|
| SEV 1 | App down, data leak, payments broken | Immediately; stop everything |
| SEV 2 | Main feature broken for many users | Same day |
| SEV 3 | Minor problem, few users | Within the week |

## 7.2 When something goes wrong (✅ DEFAULT, in this order)
1. **Stop the bleeding.** Roll back or switch the feature off.
2. **Tell me immediately** in plain words: what happened, who is affected, what's already done.
3. **Do not delete evidence.** Keep logs.
4. **Fix** on a branch, test on staging, then release.
5. **Write a short post-mortem** in `DECISIONS.md`: what happened, why, how we prevent it.

## 7.3 Data breach or privacy incident (🔒 LOCKED)
If personal data may have been exposed: stop, tell me instantly, and do not attempt to hide or quietly fix it. Laws like GDPR require notifying authorities within **72 hours** in many cases. I may need to contact users and a lawyer.

## 7.4 Rollback plan (fill once, keep updated)
- How to undo the last release: [FILL: e.g., "Redeploy previous version in hosting dashboard"]
- How to restore the database: [FILL]
- Who has access: [FILL]

---

# PART 8 — LAW, PRIVACY, PAYMENTS, STORES, ACCESSIBILITY

> ⚠️ The agent is **not a lawyer**. It must flag legal questions and recommend a professional for contracts, privacy policies, and any real-world legal risk. Laws change and differ by country. The agent must check current rules instead of trusting memory.

## 8.1 Privacy (GDPR / CCPA and similar) — 🔒 LOCKED

**Data we collect** (list every item; if it's not here, the agent must not collect it):

| Data | Why we need it | Where it's stored | How long we keep it |
|---|---|---|---|
| [FILL: e.g., email] | [FILL: login] | [FILL] | [FILL] |
| [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL] | [FILL] | [FILL] | [FILL] |

Where our users live: ☐ EU/UK (GDPR) ☐ California/US (CCPA/CPRA) ☐ Other: [FILL]

Rules:
- Collect the **minimum** data needed. If we don't need it, we don't ask for it.
- Get clear **consent** before tracking or marketing. Privacy-friendly defaults (decline non-essential cookies and tracking by default).
- Users must be able to **see, export, and delete** their data. Build and test this before launch.
- Privacy Policy must match what the product **actually** does.
- List every third-party service that receives personal data, and keep this list current.
- Children: ☐ Product is NOT for children under 13 (or 16 in some regions) and signup must block them. ☐ Product IS for children → stop, the agent must ask me; special laws apply (COPPA, etc.).
- Never use real customer data in tests, screenshots, or AI prompts.

## 8.2 Payments (Stripe / PCI) — 🔒 LOCKED (skip if no payments, write `N/A`)
- Use a hosted payment provider (e.g., Stripe Checkout or Elements). **Card numbers must never touch our servers or logs.**
- Never store card numbers, CVV, or full card data. Store only the provider's customer and payment IDs.
- Use the provider's **test mode** and test cards for all development. Live keys are entered by me only.
- Handle provider **webhooks** carefully: verify signatures, handle repeated events safely (idempotency), and handle failed payments.
- Show clear pricing, taxes where required, receipts, and an easy way to cancel.
- Define refund policy: [FILL: e.g., "14 days, no questions asked"]
- Subscriptions: test renewal, failed card, upgrade, downgrade, and cancel.
- Tax/VAT: [FILL: e.g., "Stripe Tax enabled" or "UNKNOWN — agent must ask me"]

## 8.3 App store rules (mobile only; skip if web-only)
- Before building, the agent checks the **current** Apple App Store Review Guidelines and Google Play policies. Never rely on memory.
- Common rejection causes to prevent: crashes, broken links, missing privacy policy, asking for permissions without a clear reason, no way to delete account, misleading screenshots, incomplete demo login for reviewers.
- Account deletion must be possible **inside the app** if users can create accounts.
- Digital goods or subscriptions sold inside the app usually must follow the store's own payment rules. The agent must check and ask me before choosing a payment method.
- Prepare: app name, subtitle, description, keywords, screenshots, icon, privacy "nutrition label" answers, age rating, support URL, privacy policy URL, and a **demo account** for reviewers.
- Release builds are signed with keys I own. Signing keys are never given to the agent or committed to git.

## 8.4 Accessibility (WCAG) — ✅ DEFAULT target: WCAG 2.2 level AA
- Text contrast is strong enough to read (at least 4.5:1 for normal text).
- Everything works with a **keyboard only** (web) and with screen readers (VoiceOver, TalkBack).
- Every image has alt text; every button and field has a clear label.
- Never use color as the only way to show meaning.
- Text can be enlarged without breaking the layout.
- Tap targets on mobile are large enough (at least 44×44 px / 48×48 dp).
- No flashing content.
- Forms show clear, helpful error messages.

## 8.5 Other rules that apply to this project
☐ Email marketing rules (CAN-SPAM, consent to send) ☐ Open-source licenses ☐ Industry rules (health, finance, education): [FILL or N/A]

---

# PART 9 — SUPPORT, ANALYTICS, AND CUSTOMER LEARNING

## 9.1 Support (✅ DEFAULT)
- Support channel: [FILL: e.g., support@yourdomain.com]
- Reply target: within [FILL: 24 hours]
- Agent drafts replies; **I review and send** (🔒 LOCKED: the agent never sends messages to customers itself).
- Be kind, plain, and honest. Never blame the user. Never promise features or dates I haven't approved.
- Every reply that fixes a problem should become a help-page article if it's asked more than twice.

## 9.2 Feedback loop
Weekly (✅ DEFAULT): the agent summarizes support messages and feedback into the top 5 themes, and recommends what to fix or build next.

## 9.3 Analytics: the minimum to track (✅ DEFAULT)
| Question | Event to track |
|---|---|
| Are people finding us? | Visits / installs |
| Do they sign up? | Signup completed |
| Do they get value? | **Activation:** [FILL: the key action, e.g., "booked first sitter"] |
| Do they come back? | Return visits at day 1, 7, 30 |
| Do they pay? | Subscription started / purchase made |
| Do they leave? | Cancelation, account deletion |
| What breaks? | Errors, crashes, slow screens |

Rules: track **behavior, not identity**, wherever possible. No personal data in analytics events. Analytics must respect user consent (Part 8.1).

## 9.4 North Star number
The one number that shows we're succeeding: [FILL: e.g., "Weekly active customers who booked a sitter"]

---

# PART 10 — FINAL LAUNCH CHECKLIST (all must be ☑ before Phase 8)

**Product**
☐ All Must-have features work on staging and production
☐ 0 critical / 0 high bugs
☐ Tested on all devices and browsers listed in Phase 5

**Safety**
☐ Security checklist (Phase 6) complete
☐ Backups on and a restore tested
☐ Error monitoring and alerts reach me
☐ Rollback plan written

**Legal & trust**
☐ Privacy Policy and Terms live
☐ Data export and deletion work
☐ Payment flow tested in test mode and verified live (if applicable)
☐ App store approvals received (mobile)
☐ Accessibility check done

**Business**
☐ Support email works
☐ Help page / FAQ live
☐ Analytics events verified
☐ Billing alerts and spending caps set
☐ Waitlist or launch audience ready

**People**
☐ I know exactly what I'll do in the first hour after launch
☐ I know who to call if something breaks: [FILL]

---

# PART 11 — GLOSSARY (plain words)

| Word | Meaning |
|---|---|
| **Agent** | The AI that helps you build (here: Claude Code) |
| **API** | A way for two programs to talk to each other |
| **Backend** | The behind-the-scenes part that stores data and does the work |
| **Branch** | A separate copy of code to work on safely |
| **CI** | Robot that automatically checks your code on every change |
| **Commit** | A saved snapshot of your code |
| **Environment** | A place where the app runs: local, staging, or production |
| **Environment variable** | A secret setting kept outside the code |
| **Frontend** | The part users see and touch |
| **MVP** | Smallest version that proves the idea |
| **Migration** | A planned change to the database structure |
| **Production** | The real, live version customers use |
| **Staging** | A practice copy of production |
| **Rollback** | Going back to the last working version |
| **Webhook** | A message another service sends your app when something happens |
| **Technical debt** | Shortcuts taken now that make work harder later |
| **WCAG** | The international rules for making products usable for everyone |
| **GDPR / CCPA** | Privacy laws (Europe / California) |
| **PCI** | Rules for handling payment cards safely |
| **Activation** | The moment a new user first gets real value |
| **Retention** | Whether users come back |

---

# PART 12 — CHANGE LOG FOR THIS FILE

| Date | Version | What changed | Why | Approved by |
|---|---|---|---|---|
| [FILL] | 0.1 | First version | Project start | [FILL] |

---

# FINAL CHECKLIST: IS THIS RULES.MD READY?

☐ I searched for `[FILL` and found none left
☐ No passwords, keys, or secrets are in this file
☐ Parts 0, 1, 2, 7.4, and 8 are completed
☐ I read the 🔒 LOCKED rules and agree with them
☐ I added the "Read Rules.md" line to `CLAUDE.md`
☐ I set Status in Part 0 to **Ready**

**Agent's first reply must be:** a 5-line summary of this project and its current phase, followed by any questions about unfilled or unclear parts. The agent must not begin any work until I reply "Approved."
