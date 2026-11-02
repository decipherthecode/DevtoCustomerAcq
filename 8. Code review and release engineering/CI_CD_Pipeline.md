# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

**What is this?** This is the plan for how your product's code travels from an idea on a laptop to real customers, safely and automatically. "CI" (Continuous Integration) means every change is built and tested automatically. "CD" (Continuous Delivery/Deployment) means tested changes are released automatically or with one click. This plan covers the whole life of the product, from the first line of code to your **first 500 customers**.

**Who fills it in?** Anyone. You do not need to be an expert. If you can read a question and type or tick an answer, you can do this.

**Where does this file live?** `Code review and release engineering/CI_CD_Pipeline.md`. Copy it into each new project and fill in your copy. Never edit the master template.

## The 7 rules of filling in

1. **Answer every question.** Never leave a blank.
2. **Tick boxes like this:** change `[ ]` to `[x]`.
3. **Replace every `<<FILL: ...>>`** with your answer. When no `<<FILL>>` is left in the file, the document is complete.
4. **Not relevant to you?** Write `N/A - because <reason>`. Never delete the question.
5. **Don't know yet?** Write `UNKNOWN - owner: <name> - answer by: <date>`. This is allowed. Guessing is not.
6. **Be specific.** Write "Tests must pass and 80% code coverage", not "good quality".
7. **Look at the "Example" under each question** to see what a good answer looks like. Examples are for learning. Delete them or replace them with your real answer.

## Symbols used in this document

| Symbol | Meaning |
|---|---|
| `<<FILL: ...>>` | You must type an answer here |
| `[ ]` / `[x]` | Not chosen / chosen |
| **STOP-AND-CHECK** | Pause. Make sure this is true before you continue |
| **Example** | A sample answer, not your answer |
| 🔴 Must | Required for every project |
| 🟡 Should | Strongly recommended. If skipped, explain why |
| 🟢 Could | Nice to have |

## Defaults baked into this template (change only with a written reason)

- **CI/CD tool:** GitHub Actions
- **Environments:** Dev, Staging, Production (plus optional temporary Preview environments)
- **AI model of work:** AI agents write code, humans approve every merge to the main branch and every Production release
- **Security level:** Standard (secret scan, dependency scan, code scan, container scan, license check, SBOM)
- **Launch model:** Staged cohorts to 500 customers (see Section 15)

## How long will it take?

About 60-90 minutes for a small project, longer for a big one. You can fill it in over several sittings. Save often.

---

# 0. DOCUMENT CONTROL

| Field | Your answer |
|---|---|
| Project name | `<<FILL: e.g., "PlantPal App">>` |
| Document version | `<<FILL: start at 1.0>>` |
| Last updated (YYYY-MM-DD) | `<<FILL>>` |
| Document owner (one person, not a team) | `<<FILL: name + contact>>` |
| Status | [ ] Draft [ ] In review [ ] Approved [ ] Outdated |
| Next review date (recommended: every 90 days) | `<<FILL>>` |
| Repository link | `<<FILL: URL>>` |

---

# 1. PROJECT SNAPSHOT

**Why this matters:** Everyone (including AI agents) must understand what is being built before deciding how to ship it.

### 1.1 What does your product do, in two sentences?
`<<FILL>>`
**Example:** "PlantPal reminds people when to water their plants. It has a phone app and a website."

### 1.2 Who are the customers?
`<<FILL>>`

### 1.3 What type of project is this? (tick all that apply)
- [ ] Website / web app (SaaS)
- [ ] Backend API / microservice
- [ ] Mobile app (iOS / Android)
- [ ] Desktop app
- [ ] AI / machine-learning feature (models, prompts, agents)
- [ ] Data pipeline / analytics
- [ ] Library / SDK / package
- [ ] Infrastructure only (servers, cloud setup)
- [ ] Other: `<<FILL>>`

### 1.4 Main programming languages and frameworks
`<<FILL: e.g., TypeScript, Node.js, React, PostgreSQL>>`

### 1.5 Where does the product run?
- [ ] AWS [ ] Google Cloud [ ] Azure [ ] Vercel / Netlify [ ] Own servers [ ] App stores [ ] Other: `<<FILL>>`

### 1.6 How important is it if the product breaks? (pick one)
- [ ] **Low:** a few people are annoyed (internal tool, hobby project)
- [ ] **Medium:** customers are inconvenienced, revenue may be affected
- [ ] **High:** money, safety, health, legal or privacy harm is possible

> This answer sets how strict your gates are in Section 10. When unsure, pick the higher level.

### 1.7 Does the product handle any of the following? (tick all that apply)
- [ ] Personal data (names, emails, locations)
- [ ] Payment data
- [ ] Health data
- [ ] Children's data
- [ ] None of the above

> If you ticked anything other than "None", complete Section 17 carefully.

**STOP-AND-CHECK:** Could a stranger read 1.1 and understand the product? [ ] Yes

---

# 2. GOALS AND SUCCESS NUMBERS

### 2.1 What do you want from your pipeline? (tick your top 3)
- [ ] Ship faster
- [ ] Break less
- [ ] Catch security problems early
- [ ] Make releases boring and repeatable
- [ ] Let AI agents help safely
- [ ] Pass an audit / satisfy customers' security questions
- [ ] Reduce cost
- [ ] Other: `<<FILL>>`

### 2.2 Pipeline health targets
These four numbers are the industry-standard measures of delivery health (called "DORA metrics"). Set your targets.

| Measure | Plain-English meaning | Target for first 6 months | Target at 500 customers |
|---|---|---|---|
| Deployment frequency | How often you release to Production | `<<FILL: e.g., weekly>>` | `<<FILL: e.g., daily>>` |
| Lead time for changes | Time from "code finished" to "live" | `<<FILL: e.g., under 2 days>>` | `<<FILL: e.g., under 1 day>>` |
| Change failure rate | % of releases that cause a problem | `<<FILL: e.g., under 15%>>` | `<<FILL: e.g., under 10%>>` |
| Time to restore service | How fast you fix a broken release | `<<FILL: e.g., under 4 hours>>` | `<<FILL: e.g., under 1 hour>>` |

### 2.3 Where will you track these numbers?
`<<FILL: e.g., GitHub Insights, a spreadsheet, Grafana dashboard>>`

---

# 3. PEOPLE AND RESPONSIBILITIES

**Why this matters:** Most release failures come from "I thought someone else was doing it."

### 3.1 Who does what?

| Role | What they do | Name(s) | Backup person |
|---|---|---|---|
| Product owner | Decides what ships and when | `<<FILL>>` | `<<FILL>>` |
| Tech lead | Approves design and merges | `<<FILL>>` | `<<FILL>>` |
| Developers (human) | Write and review code | `<<FILL>>` | N/A |
| AI agent supervisor | Owns what AI agents are allowed to do (see Section 4) | `<<FILL>>` | `<<FILL>>` |
| QA / tester | Verifies quality before release | `<<FILL>>` | `<<FILL>>` |
| Release manager | Runs the release checklist (Section 14) | `<<FILL>>` | `<<FILL>>` |
| Security owner | Reviews security findings | `<<FILL>>` | `<<FILL>>` |
| On-call engineer | First responder when something breaks | `<<FILL>>` | `<<FILL>>` |
| Customer support lead | Collects customer feedback and problems | `<<FILL>>` | `<<FILL>>` |

### 3.2 Who can approve a Production release? (name at least TWO people)
`<<FILL>>`

> **STOP-AND-CHECK:** The person who wrote a change must not be the only person who approves it. [ ] Confirmed

### 3.3 How do people reach each other during a release or incident?
`<<FILL: e.g., Slack channel #releases, phone tree, PagerDuty>>`

---

# 4. AI AGENT RULES (AI-DRIVEN DEVELOPMENT)

**Model for this template: AI writes, humans approve.** AI agents may write code, tests and docs, and may open pull requests. A human must approve every merge to the main branch and every Production release.

### 4.1 Which AI agents or tools are used?

| Tool / agent | What it is used for | Who owns it |
|---|---|---|
| `<<FILL: e.g., Claude Code>>` | `<<FILL: e.g., writes features, opens PRs>>` | `<<FILL>>` |
| `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |

### 4.2 What may AI agents do? (tick all that apply)
- [ ] Create branches
- [ ] Write and edit code
- [ ] Write and run tests
- [ ] Open pull requests
- [ ] Respond to review comments
- [ ] Update documentation
- [ ] Propose dependency upgrades
- [ ] Fix failing CI checks
- [ ] Draft release notes
- [ ] Other: `<<FILL>>`

### 4.3 What must AI agents NEVER do? (🔴 Must keep all ticked)
- [x] Merge their own pull requests without human approval
- [x] Deploy to Production without human approval
- [x] Access, print or commit secrets, passwords or API keys
- [x] Disable, skip or weaken tests, security scans or branch protections
- [x] Change pipeline files (`.github/workflows/`), access rules or secrets settings without a human reviewing that file specifically
- [x] Delete data, databases or backups
- [x] Use real customer data for testing
- [ ] Add your own rule: `<<FILL>>`

### 4.4 How do you know a change was written by AI?
- [ ] PR label `ai-generated`
- [ ] Commit message trailer (e.g., `Co-authored-by: <agent>`)
- [ ] Agent uses its own named account
- [ ] Other: `<<FILL>>`

### 4.5 Extra human review for AI-written code (tick all that apply)
- [ ] Reviewer must read every changed line, not only the summary
- [ ] AI changes to security, payments, login or data deletion require a second reviewer
- [ ] AI-added dependencies must be checked by a human (do they exist? are they trustworthy? are they maintained?)
- [ ] AI-written tests must be checked to confirm they test real behavior, not just pass
- [ ] Other: `<<FILL>>`

### 4.6 What access do AI agents have?
Rule of thumb: give the least access that gets the job done.

| Resource | Allowed access | Why |
|---|---|---|
| Source code | [ ] Read [ ] Write to branches [ ] Write to main (🔴 never) | `<<FILL>>` |
| Dev environment | [ ] None [ ] Read [ ] Deploy | `<<FILL>>` |
| Staging | [ ] None [ ] Read [ ] Deploy | `<<FILL>>` |
| Production | [ ] None (recommended) [ ] Read-only logs | `<<FILL>>` |
| Secrets | [ ] None (🔴 recommended) | `<<FILL>>` |

### 4.7 If your product itself uses AI (prompts, models, agents)
- [ ] N/A - our product has no AI features
- [ ] Prompts are stored in the repository and reviewed like code
- [ ] Model name and version are pinned (e.g., `model-x-2026-01`), never "latest"
- [ ] An evaluation test set checks answer quality before each release
- [ ] Evaluations check for harmful, wrong or private-data-leaking answers
- [ ] A cost cap and rate limit are set per customer and overall
- [ ] There is a documented way to switch to a backup model or turn the AI feature off
- [ ] Other: `<<FILL>>`

### 4.8 Instructions given to AI agents (rules files, system prompts, skills)
Agents follow written instructions. Those instructions are as important as code.
- Where are they stored? `<<FILL: e.g., /AGENTS.md or /.claude/ in the repository>>`
- [ ] Reviewed through pull requests like code
- [ ] Each instruction file has a named owner: `<<FILL>>`
- [ ] Agents cannot change their own instruction files without a human approving that change
- [ ] Reviewed every `<<FILL: e.g., 90 days>>` and after any agent mistake

### 4.9 Trust levels: how much freedom for which kind of change

| Change risk | Examples | Agent may | Human review needed |
|---|---|---|---|
| Low | Docs, comments, tests, formatting | `<<FILL: e.g., open PR>>` | `<<FILL: e.g., 1 reviewer>>` |
| Medium | New features, bug fixes | `<<FILL>>` | `<<FILL: e.g., 1 reviewer + QA>>` |
| High | Login, payments, personal data, pipeline files, infrastructure, deletion | `<<FILL: e.g., propose only>>` | `<<FILL: e.g., 2 reviewers incl. security owner>>` |

### 4.10 Agent limits (stops runaway behavior)
- Maximum PR size an agent may open: `<<FILL: e.g., 400 lines>>`
- Maximum number of open agent PRs at once: `<<FILL>>`
- Maximum run time per task: `<<FILL>>`
- Stop and ask a human after `<<FILL: e.g., 3>>` failed attempts at the same problem
- Monthly spend cap per agent / tool: `<<FILL>>`; alert at `<<FILL>>`

### 4.11 Audit trail (what did the agent do?)
- [ ] Agent actions, prompts and tool calls are logged
- [ ] Logs link each PR to the task or ticket that started it
- [ ] Logs are kept for `<<FILL: e.g., 1 year>>` and contain no secrets
- Where to find them: `<<FILL>>`

### 4.12 Untrusted input (prompt injection safety)
Text in issues, web pages, emails, code comments, dependency documentation and customer messages can contain hidden instructions aimed at the agent.
- [x] Agents treat that text as information, never as commands (🔴 Must)
- [ ] Agents never send code, secrets or customer data to outside websites they found on their own
- [ ] Agents cannot install new tools or dependencies without human approval
- [ ] Other: `<<FILL>>`

### 4.13 When an agent makes a mistake
1. **Stop it:** who can pause all agents immediately (the "kill switch")? `<<FILL>>`
2. **Undo it:** revert the change using the Section 12 rollback steps.
3. **Learn from it:** write down what happened and update the instruction file (4.8) and tests so it cannot repeat.
4. **Tell people:** who is informed? `<<FILL>>`

---

# 5. CODE, BRANCHES AND CODE REVIEW

### 5.1 Branching style (pick one)
- [ ] **Trunk-based (recommended):** short-lived branches merged into `main` frequently
- [ ] GitHub Flow: feature branches and pull requests into `main`
- [ ] Release branches: `main` plus `release/x.y` branches
- [ ] Other: `<<FILL>>`

Main branch name: `<<FILL: main>>`

### 5.2 Branch naming
`<<FILL: e.g., feature/short-name, fix/short-name, ai/short-name>>`

### 5.3 Commit message style
- [ ] Conventional Commits (`feat:`, `fix:`, `docs:`)
- [ ] Other: `<<FILL>>`

### 5.4 Protect the main branch (🔴 Must tick all in GitHub settings)
- [ ] Direct pushes to `main` are blocked
- [ ] Pull request required before merging
- [ ] At least `<<FILL: 1 or 2>>` human approval(s) required
- [ ] New commits dismiss old approvals
- [ ] All required CI checks must pass before merge
- [ ] Branch must be up to date before merge
- [ ] Conversations must be resolved before merge
- [ ] Force-push and branch deletion blocked
- [ ] Rules apply to admins too
- [ ] Signed commits required (🟢 Could)

### 5.5 Code owners (CODEOWNERS file)
Which folders need approval from which people or teams?

| Folder / file | Owner(s) |
|---|---|
| `.github/workflows/` (pipeline files) | `<<FILL>>` |
| `/infrastructure/` | `<<FILL>>` |
| `/src/auth/` or payments or other sensitive areas | `<<FILL>>` |
| Everything else | `<<FILL>>` |

### 5.6 Pull request (PR) rules
- Maximum recommended PR size: `<<FILL: e.g., 400 changed lines>>`
- Every PR must include (tick all):
  - [ ] What changed and why
  - [ ] How it was tested
  - [ ] Screenshots for visible changes
  - [ ] Linked ticket or issue
  - [ ] Note about database or config changes
  - [ ] Rollback plan for risky changes
  - [ ] AI-generated label if applicable
- Reviewers must respond within: `<<FILL: e.g., 1 business day>>`

### 5.7 Code review checklist (reviewers tick every item)
- [ ] Does it do what the ticket says?
- [ ] Is it easy to read and maintain?
- [ ] Are there tests for new behavior and edge cases?
- [ ] No secrets, passwords or tokens in code?
- [ ] No unnecessary new dependencies?
- [ ] Errors handled sensibly? Logs free of personal data?
- [ ] Is it safe for existing customers' data (migrations, compatibility)?
- [ ] Documentation updated?

---

# 6. ENVIRONMENTS

An environment is a separate copy of your product where code runs.

### 6.1 Describe each environment

| | Dev | Staging | Production |
|---|---|---|---|
| Purpose | Developers try things | Final rehearsal that mirrors Production | Real customers |
| URL / location | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| Who can deploy | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| Data used | Fake only | Fake or anonymized copy | Real |
| Deploys automatically? | [ ] Yes [ ] No | [ ] Yes [ ] No | [ ] Yes [ ] No (🔴 human approval) |
| Approval needed | None | `<<FILL>>` | `<<FILL: min. 2 names from 3.2>>` |
| Monitoring on? | [ ] Yes [ ] No | [ ] Yes [ ] No | [ ] Yes (🔴 Must) |

### 6.2 Preview environments (temporary copy per pull request)
- [ ] Yes, created for each PR and deleted when PR closes
- [ ] No
- [ ] N/A - because `<<FILL>>`

### 6.3 Staging must match Production. Tick what matches:
- [ ] Same operating system / runtime versions
- [ ] Same configuration structure
- [ ] Same database type and version
- [ ] Same deployment method
- [ ] Known differences: `<<FILL>>`

### 6.4 How is configuration handled differently per environment?
`<<FILL: e.g., environment variables stored in GitHub Environments; no config values hard-coded>>`

---

# 7. CONTINUOUS INTEGRATION (CI): AUTOMATIC CHECKS ON EVERY CHANGE

### 7.1 When does CI run?
- [ ] On every pull request
- [ ] On every merge to `main`
- [ ] Nightly (full test run)
- [ ] On a schedule for security scans
- [ ] Manually on demand

### 7.2 CI stages
Mark each stage 🔴/🟡/🟢 for your project. "Blocks merge?" means a failure stops the change.

| # | Stage | What it checks | Tool you will use | Blocks merge? | Max run time |
|---|---|---|---|---|---|
| 1 | Checkout and setup | Get code, install tools | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 2 | Install dependencies (with cache) | Everything needed is available | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 3 | Lint and format | Code style, typos | `<<FILL: e.g., ESLint, Prettier>>` | [ ] Yes | `<<FILL>>` |
| 4 | Type check / compile | Code is valid | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 5 | Unit tests | Small pieces work | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 6 | Integration tests | Pieces work together | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 7 | End-to-end (E2E) tests | Real user journeys work | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 8 | Build the app / container | Product can be packaged | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 9 | Secret scan | No passwords or keys in code | `<<FILL: e.g., GitHub secret scanning, Gitleaks>>` | [ ] Yes | `<<FILL>>` |
| 10 | Dependency scan | No known-vulnerable libraries | `<<FILL: e.g., Dependabot, npm audit>>` | [ ] Yes | `<<FILL>>` |
| 11 | Code security scan (SAST) | Risky code patterns | `<<FILL: e.g., CodeQL>>` | [ ] Yes | `<<FILL>>` |
| 12 | Container / image scan | Vulnerabilities in the package | `<<FILL: e.g., Trivy>>` | [ ] Yes | `<<FILL>>` |
| 13 | License check | Libraries' licenses are allowed | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 14 | SBOM (software bill of materials) | List of every ingredient is created | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| 15 | Infrastructure-as-code scan | Cloud setup files are safe | `<<FILL or N/A>>` | [ ] Yes | `<<FILL>>` |
| 16 | Accessibility and performance check | Usable, fast | `<<FILL or N/A>>` | [ ] Yes | `<<FILL>>` |
| 17 | Database migration test | Changes to data structure work on a copy | `<<FILL or N/A>>` | [ ] Yes | `<<FILL>>` |

### 7.3 Test rules
- Minimum code coverage to merge: `<<FILL: e.g., 80%>>`
- What happens to a "flaky" test (sometimes passes, sometimes fails)? `<<FILL: e.g., quarantine within 24h, fix within 1 week>>`
- Are tests allowed to be skipped? [ ] No (recommended) [ ] Yes, with written approval from: `<<FILL>>`
- Maximum acceptable total CI time: `<<FILL: e.g., 15 minutes>>`

### 7.4 What happens when a check fails?
`<<FILL: e.g., author fixes within 1 business day; broken main branch is fixed or reverted within 1 hour>>`

### 7.5 Testing strategy: what kinds of tests, and how many

Aim for many small fast tests, fewer slow big tests (the "test pyramid").

| Test type | Goal share of all tests | Runs when | Owner |
|---|---|---|---|
| Unit | `<<FILL: e.g., 70%>>` | Every PR | `<<FILL>>` |
| Integration | `<<FILL: e.g., 20%>>` | Every PR | `<<FILL>>` |
| End-to-end (user journeys) | `<<FILL: e.g., 10%>>` | Every merge and before release | `<<FILL>>` |
| Performance / load | n/a | `<<FILL: e.g., weekly and before each launch stage>>` | `<<FILL>>` |
| Security tests | n/a | `<<FILL>>` | `<<FILL>>` |
| Manual / exploratory | n/a | `<<FILL: e.g., before each launch stage>>` | `<<FILL>>` |

### 7.6 The 5 most important user journeys that must always work
These become the end-to-end tests and the smoke tests (Section 9.7).
1. `<<FILL: e.g., sign up>>`
2. `<<FILL: e.g., log in>>`
3. `<<FILL: e.g., create a plant profile>>`
4. `<<FILL: e.g., receive a reminder>>`
5. `<<FILL: e.g., pay for a subscription>>`

### 7.7 Test data rules
- [ ] Test data is fake or fully anonymized. Real customer data is never used (🔴 Must)
- [ ] Test data is created automatically and cleaned up after tests
- [ ] Tests do not depend on each other or on the order they run
- [ ] Tests do not call real payment, email or SMS services, or use their test mode: `<<FILL>>`

### 7.8 Bug and regression rules
- [ ] Every bug fix includes a test that fails without the fix
- [ ] Bugs found by customers are added to the regression test list
- [ ] Reviewers check that AI-written tests would actually fail if the code were wrong

### 7.9 Performance and load testing
- Target speed (e.g., 95% of requests under 500 ms): `<<FILL>>`
- Load to test for before each launch stage: `<<FILL: e.g., 2x the expected users>>`
- Tool: `<<FILL or N/A>>`

**STOP-AND-CHECK:** Every 🔴 stage above has a named tool or an `N/A` with a reason. [ ] Yes

---

# 8. BUILD OUTPUTS AND VERSIONING

### 8.1 What does your pipeline produce? (tick all that apply)
- [ ] Container image
- [ ] Web bundle
- [ ] Mobile app file (.ipa / .aab)
- [ ] Package (npm, PyPI, Maven, etc.)
- [ ] Binary / installer
- [ ] Infrastructure plan
- [ ] AI model or prompt bundle
- [ ] Other: `<<FILL>>`

### 8.2 Where is it stored?
`<<FILL: e.g., GitHub Container Registry, App Store Connect>>`

### 8.3 Version numbering
- [ ] Semantic Versioning `MAJOR.MINOR.PATCH` (e.g., `2.4.1`)
  - MAJOR = breaking change; MINOR = new feature; PATCH = bug fix
- [ ] Other: `<<FILL>>`

### 8.4 Build once, deploy many (🔴 Must)
- [ ] The exact same build that passed Staging is the one promoted to Production (never rebuilt)

### 8.5 Build trust (🟡 Should)
- [ ] Builds are tagged with the Git commit ID
- [ ] Builds are signed
- [ ] Build provenance (proof of where it was built) is recorded
- [ ] Old builds are kept for at least `<<FILL: e.g., 90 days>>` so you can roll back

### 8.6 Release notes
Who writes them? `<<FILL>>` Where are they published? `<<FILL>>`
- [ ] AI may draft; a human must check before publishing

---

# 9. CONTINUOUS DELIVERY (CD): GETTING CODE TO CUSTOMERS

### 9.1 Deployment flow (confirm or edit)
```
Pull Request -> CI checks -> Human review -> Merge to main
   -> Auto-deploy to Dev -> Auto-deploy to Staging + smoke tests
   -> Human approval -> Production release (chosen strategy below) -> Monitor
```
Edits: `<<FILL or "none">>`

### 9.2 Which release strategy will you use? (pick the default; note exceptions)

| Strategy | Plain English | Best when | Chosen? |
|---|---|---|---|
| All-at-once | Everyone gets the new version at once | Low-risk, small projects | [ ] |
| Canary / gradual | Start with 1-5% of users, widen if healthy | Medium to high-risk changes | [ ] |
| Blue-green | Two identical Production copies; switch traffic instantly; switch back to roll back | You need instant rollback | [ ] |
| Feature flags | Code ships switched off; turn on for chosen users | You want to separate "deploy" from "release" | [ ] |

Default for this project: `<<FILL>>`
Exceptions (when and why you use another one): `<<FILL>>`

### 9.3 Canary rules (skip if not used)
- Starting percentage: `<<FILL>>`
- Steps: `<<FILL: e.g., 1% -> 5% -> 25% -> 50% -> 100%>>`
- Wait at each step: `<<FILL: e.g., 30 minutes>>`
- Auto-stop and roll back if: `<<FILL: e.g., error rate above 1% or response time above 2 seconds>>`

### 9.4 Feature flag rules (skip if not used)
- Tool: `<<FILL>>`
- Every flag has an owner and a removal date: [ ] Yes
- Maximum flag lifetime: `<<FILL: e.g., 60 days>>`
- Flag changes in Production are logged and need approval: [ ] Yes

### 9.5 Database and data changes (migrations)
- [ ] N/A - no database
- [ ] Migrations are version-controlled and run by the pipeline
- [ ] Migrations are backward compatible (old code still works during the release)
- [ ] Big changes use "expand, migrate, contract" (add new, move data, remove old later)
- [ ] A backup is taken before each Production migration
- [ ] Migrations tested on a copy of Staging data first
- [ ] Rollback or "forward-fix" plan: `<<FILL>>`

### 9.6 Infrastructure as code
- [ ] N/A
- [ ] Cloud setup is written in code (Terraform, Pulumi, CloudFormation, etc.): tool `<<FILL>>`
- [ ] Changes show a "plan" for human review before applying
- [ ] No manual changes in the cloud console in Production (🔴 recommended)

### 9.7 After every deployment, automatic "smoke tests" must check:
`<<FILL: e.g., homepage loads, login works, health endpoint returns OK, one test purchase succeeds>>`

### 9.8 Release windows
- Allowed days/times for Production releases: `<<FILL: e.g., Mon-Thu 10:00-16:00>>`
- Frozen periods (no releases): `<<FILL: e.g., big marketing launch days>>`
- Emergency (hotfix) releases allowed? [ ] Yes, with approval from `<<FILL>>` and a follow-up review within `<<FILL>>`

### 9.9 Project-type extras (fill only what applies; mark the rest N/A)

**Web / SaaS**
- CDN cache clearing: `<<FILL or N/A>>`
- Browser support: `<<FILL or N/A>>`

**API**
- Versioning (e.g., `/v1/`): `<<FILL or N/A>>`
- Old versions retired after: `<<FILL or N/A>>`
- Backward compatibility test: `<<FILL or N/A>>`

**Mobile app**
- Signing keys stored in: `<<FILL or N/A>>`
- Beta channel (TestFlight / Play internal testing): `<<FILL or N/A>>`
- Store review time included in the schedule (allow several days): `<<FILL or N/A>>`
- Phased rollout used: [ ] Yes [ ] No [ ] N/A
- Minimum supported OS versions: `<<FILL or N/A>>`
- Remote kill switch or force-update for bad versions: [ ] Yes [ ] No [ ] N/A

**AI / ML**
- Model registry: `<<FILL or N/A>>`
- Evaluation pass mark to ship: `<<FILL or N/A>>`
- Shadow or A/B testing: `<<FILL or N/A>>`

### 9.10 Accessibility and languages (localization)

**Accessibility** (can people with disabilities use the product?)
- [ ] N/A - no user interface
- [ ] Automatic accessibility checks run in CI (tool: `<<FILL>>`)
- [ ] Manual check with keyboard only and a screen reader before big releases
- [ ] Standard targeted: `<<FILL: e.g., WCAG 2.2 AA>>`
- Blocks release if: `<<FILL: e.g., any new critical accessibility failure>>`

**Localization** (more than one language or region)
- [ ] N/A - one language only
- Languages at launch: `<<FILL>>`
- [ ] All text is kept in translation files, not typed into code
- [ ] Missing translations are caught by a CI check
- [ ] Dates, currencies, number formats and right-to-left languages tested
- [ ] Who approves translations: `<<FILL>>`

---

# 10. QUALITY GATES (THE "NO-GO" RULES)

A gate is a hard rule: if it fails, the change does not move forward.

### 10.1 Set your gate strictness (from Section 1.6)
Criticality: [ ] Low [ ] Medium [ ] High

### 10.2 Gate table

| Gate | Where it applies | Pass condition | Who can override | Override must be logged? |
|---|---|---|---|---|
| All required CI checks green | Before merge | `<<FILL>>` | Nobody (🔴 recommended) | [ ] Yes |
| Human approval of PR | Before merge | `<<FILL>>` | Nobody | [ ] Yes |
| No critical/high security findings | Before merge / release | `<<FILL: e.g., zero critical, zero high older than 7 days>>` | `<<FILL>>` | [ ] Yes |
| Coverage threshold | Before merge | `<<FILL>>` | `<<FILL>>` | [ ] Yes |
| Staging smoke tests pass | Before Production | `<<FILL>>` | `<<FILL>>` | [ ] Yes |
| QA sign-off | Before Production | `<<FILL>>` | `<<FILL>>` | [ ] Yes |
| Performance check | Before Production | `<<FILL: e.g., page loads under 2s>>` | `<<FILL>>` | [ ] Yes |
| Rollback plan written | Before Production | Yes | Nobody | [ ] Yes |
| Production approval by 2 named people | Before Production | Yes | Nobody | [ ] Yes |

### 10.3 Security finding rules

| Severity | Must be fixed within |
|---|---|
| Critical | `<<FILL: e.g., 24 hours or release blocked>>` |
| High | `<<FILL: e.g., 7 days>>` |
| Medium | `<<FILL: e.g., 30 days>>` |
| Low | `<<FILL: e.g., next planned cycle>>` |

---

# 11. SECRETS, ACCESS AND PIPELINE SECURITY (GITHUB ACTIONS)

### 11.1 Where are secrets stored?
- [ ] GitHub Actions secrets (repository or organization)
- [ ] GitHub Environments secrets (separate for Dev / Staging / Production)
- [ ] Cloud secret manager: `<<FILL>>`
- [x] Never in code, never in logs, never in chat with AI tools (🔴 Must)

### 11.2 Pipeline hardening (tick all that apply; 🔴 first four)
- [ ] Workflows have the least permission needed (`permissions:` set explicitly, read-only by default)
- [ ] Third-party Actions are pinned to a full commit ID, not a moving tag
- [ ] Production deploys use a protected GitHub Environment with required reviewers
- [ ] Cloud access uses short-lived credentials (OIDC) instead of stored long-lived keys
- [ ] Pull requests from forks cannot access secrets
- [ ] Pipeline files are reviewed by CODEOWNERS (Section 5.5)
- [ ] Dependabot keeps Actions and libraries updated
- [ ] Self-hosted runners (if any) are isolated and cleaned after each job: `<<FILL or N/A>>`

### 11.3 Secret rotation
- How often are secrets changed? `<<FILL: e.g., every 90 days>>`
- What do you do if a secret leaks? `<<FILL: e.g., revoke immediately, rotate, check logs, tell the security owner>>`

### 11.4 Who can change pipeline settings and secrets?
`<<FILL: names/roles>>`

---

# 12. ROLLBACK, INCIDENTS AND RECOVERY

### 12.1 How do you undo a bad release? (tick all that apply)
- [ ] Redeploy previous build (one click)
- [ ] Switch traffic back (blue-green)
- [ ] Turn off the feature flag
- [ ] Stop canary at 0%
- [ ] Revert the commit and release again
- [ ] Restore from backup (data problems)
- [ ] Other: `<<FILL>>`

### 12.2 Time targets
- Decide to roll back within: `<<FILL: e.g., 15 minutes of detecting a problem>>`
- Rollback completed within: `<<FILL: e.g., 30 minutes>>`

### 12.3 Rollback triggers (any ONE means roll back)
`<<FILL: e.g., error rate above 2%, payments failing, security issue, data loss risk, more than 3 customer complaints about the same problem within 1 hour>>`

### 12.4 Who has the authority to roll back without asking?
`<<FILL: on-call engineer, release manager>>`

### 12.5 Backups
- What is backed up: `<<FILL>>`
- How often: `<<FILL>>`
- Last time a restore was tested (YYYY-MM-DD): `<<FILL>>`
- Restore test frequency: `<<FILL: e.g., every quarter>>`

### 12.6 Incident severity levels

| Level | Meaning | Response time | Who is told |
|---|---|---|---|
| SEV1 | Product down or data at risk | `<<FILL>>` | `<<FILL>>` |
| SEV2 | Major feature broken | `<<FILL>>` | `<<FILL>>` |
| SEV3 | Minor problem | `<<FILL>>` | `<<FILL>>` |

### 12.7 After every SEV1/SEV2, hold a "blameless review" within `<<FILL: e.g., 5 working days>>` covering what happened, why, what was good, and what changes (with owners and dates).

---

# 13. MONITORING AND ALERTS

### 13.1 What do you watch? (tick all that apply)
- [ ] Errors and crashes
- [ ] Response time / speed
- [ ] Uptime
- [ ] Traffic and sign-ups
- [ ] Payments / key business actions
- [ ] Server health (CPU, memory, disk)
- [ ] Cost
- [ ] AI answer quality and cost (if AI is used)
- [ ] Customer-reported problems
- [ ] Other: `<<FILL>>`

### 13.2 Tools
`<<FILL: e.g., Sentry, Datadog, Grafana, CloudWatch, UptimeRobot>>`

### 13.3 Alert rules

| What | Alert when | Sent to | Wake someone at night? |
|---|---|---|---|
| `<<FILL: e.g., error rate>>` | `<<FILL: e.g., above 2% for 5 min>>` | `<<FILL>>` | [ ] Yes [ ] No |
| `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | [ ] Yes [ ] No |

### 13.4 Logs
- Where do logs go? `<<FILL>>`
- Kept for: `<<FILL>>`
- No passwords, tokens or personal data in logs: [ ] Confirmed

### 13.5 Deployments appear on dashboards as markers so you can see "what changed right before it broke": [ ] Yes

---

# 14. RELEASE CHECKLIST (USE FOR EVERY PRODUCTION RELEASE)

Copy this section into the release ticket and tick as you go.

**Before the release**
- [ ] All CI checks are green on the exact commit being released
- [ ] Release notes written and checked by a human
- [ ] Staging deployment tested; smoke tests pass
- [ ] QA sign-off received (if required)
- [ ] Database migrations tested and backup confirmed
- [ ] Feature flags set correctly
- [ ] Rollback plan written and the previous build is available
- [ ] Monitoring dashboards and alerts are working
- [ ] Support team told what is changing
- [ ] Two approvers have approved
- [ ] Release window is allowed (Section 9.8)

**During the release**
- [ ] Release started at: `<<FILL: time>>` by `<<FILL: name>>`
- [ ] Canary / gradual steps followed (if used)
- [ ] Smoke tests pass in Production
- [ ] Dashboards watched for `<<FILL: e.g., 30 minutes>>`

**After the release**
- [ ] No alert or rollback trigger fired
- [ ] Release announced to the team (and customers if needed)
- [ ] Release notes published
- [ ] Release ticket closed; deployment recorded
- [ ] Anything learned is written down: `<<FILL>>`

---

# 15. THE JOURNEY TO YOUR FIRST 500 CUSTOMERS

**Why this matters:** Launching to everyone at once is risky. Instead, you let in small groups, check that things are healthy, then open the door wider.

### 15.1 Launch dates and owners
- Planned first customer access date: `<<FILL>>`
- Target date for 500 customers: `<<FILL>>`
- Launch owner: `<<FILL>>`

### 15.2 Definition of "a customer"
`<<FILL: e.g., someone who signed up AND completed the first key action, such as creating a plant profile>>`

### 15.3 Stages (staged cohorts)

| Stage | Who is let in | Customer count | How people join | Minimum time at this stage | Go/no-go decider |
|---|---|---|---|---|---|
| 0. Internal | Team only | up to `<<FILL: e.g., 10>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 1. Friendly pilot | Invited friends and trusted users | 10 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 2. Private beta | Waitlist | 50 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 3. Extended beta | Waitlist + referrals | 100 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 4. Early access | Open sign-up with limits | 250 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 5. Public launch | Everyone | 500 and beyond | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |

### 15.4 Go / no-go checks before opening each next stage
Fill the numbers. "Go" only if every line is met.

| Check | Required result |
|---|---|
| Crash-free sessions / error rate | `<<FILL: e.g., above 99% crash-free>>` |
| Page / API speed | `<<FILL>>` |
| Uptime during the stage | `<<FILL>>` |
| Open critical or high bugs | `<<FILL: e.g., zero>>` |
| Customer satisfaction | `<<FILL: e.g., 7 out of 10 or higher>>` |
| Customers completing the first key action | `<<FILL: e.g., 60%>>` |
| Support questions per customer | `<<FILL>>` |
| Cost per customer | `<<FILL>>` |
| Security and privacy review | `<<FILL: e.g., passed>>` |
| Team capacity to support the next group | `<<FILL: e.g., yes, confirmed by support lead>>` |

### 15.5 Stop-and-roll-back triggers during the launch
Pause new sign-ups if: `<<FILL: e.g., SEV1 incident, data exposure, payment failures, more than 10% of customers report the same problem>>`

### 15.6 How do you control who gets in? (tick all that apply)
- [ ] Invite codes
- [ ] Waitlist release
- [ ] Feature flags by user group
- [ ] Region-based release
- [ ] Sign-up cap number
- [ ] Other: `<<FILL>>`

### 15.7 Capacity and cost
- Expected maximum concurrent users at 500 customers: `<<FILL>>`
- Load test completed? [ ] Yes, date `<<FILL>>` [ ] No
- Monthly budget limit for cloud / AI / tools: `<<FILL>>`
- Alert when spend reaches: `<<FILL>>`

### 15.8 Collecting customer feedback
- Channels: [ ] In-app form [ ] Email [ ] Chat [ ] Interviews [ ] Reviews [ ] Other: `<<FILL>>`
- Who reads feedback and how often: `<<FILL>>`
- How feedback becomes tickets: `<<FILL>>`
- How fast must you answer a customer: `<<FILL>>`

### 15.9 Communication
- Status page: `<<FILL: URL or N/A>>`
- How customers are told about problems and releases: `<<FILL>>`
- Legal pages ready (Terms, Privacy Policy): [ ] Yes

### 15.10 Launch-day readiness (all must be ticked before Stage 1)
- [ ] Rollback tested in Staging
- [ ] On-call schedule published
- [ ] Support team trained and knows the escalation path
- [ ] Backups and restores tested
- [ ] Monitoring and alerts proven (a test alert was received)
- [ ] Payment flow tested with test data (if applicable)
- [ ] Analytics tracking verified
- [ ] Legal and privacy requirements checked (Section 17)

### 15.11 After the 500th customer: moving from launch to normal operations

**Success numbers to measure for the first 90 days after reaching 500**

| Measure | Plain-English meaning | Target |
|---|---|---|
| Activation rate | % of sign-ups who complete the first key action | `<<FILL>>` |
| Retention (day 7 / day 30) | % of customers still using it after 7 / 30 days | `<<FILL>>` |
| Churn | % of customers who leave each month | `<<FILL>>` |
| Customer satisfaction | Survey score | `<<FILL>>` |
| Support load | Tickets per 100 customers | `<<FILL>>` |
| Cost per customer | Total running cost / customers | `<<FILL>>` |

### 15.12 Scaling plan
- What breaks first if customers double? `<<FILL: e.g., database connections, AI cost>>`
- Limits to raise before reaching `<<FILL: e.g., 1,000>>` customers: `<<FILL>>`
- Who decides to scale up, and based on which numbers? `<<FILL>>`

### 15.13 Handover to everyday operations
- [ ] Launch rollout controls (invite codes, caps) removed or relaxed on `<<FILL: date>>`
- [ ] Temporary feature flags removed or given owners
- [ ] On-call schedule and incident process now permanent
- [ ] Release cadence (Section 2.2) moved to the "500 customers" targets
- [ ] Runbooks (step-by-step fix guides) written for the 5 most likely incidents

### 15.14 Launch retrospective
Within `<<FILL: e.g., 2 weeks>>` of reaching 500: what went well, what hurt, what we change in this template. Update the master template with lessons learned: [ ] Done

---

# 16. PIPELINE HEALTH AND MAINTENANCE

### 16.1 How will you keep the pipeline healthy?
- [ ] Review pipeline speed and failure rate every `<<FILL: e.g., month>>`
- [ ] Fix flaky tests within `<<FILL>>`
- [ ] Update Actions, runtimes and dependencies every `<<FILL>>`
- [ ] Remove unused workflows and old secrets every `<<FILL>>`
- [ ] Review cost of CI minutes and storage every `<<FILL>>`
- [ ] Re-run this document's review every 90 days

### 16.2 Who owns the pipeline?
`<<FILL>>`

### 16.3 Where do people get help if the pipeline breaks?
`<<FILL>>`

### 16.4 Cost and budget tracking

| Cost area | Monthly budget | Alert at | Owner | Where to see it |
|---|---|---|---|---|
| CI minutes and storage (GitHub) | `<<FILL>>` | `<<FILL: e.g., 80%>>` | `<<FILL>>` | `<<FILL>>` |
| Cloud hosting | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| AI coding agents | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| AI features inside the product | `<<FILL or N/A>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| Monitoring, logging, security tools | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| Third-party services | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |

- [ ] Resources are tagged by project and environment so costs can be split
- [ ] Preview and Dev environments shut down automatically when idle
- What happens when a budget is reached? `<<FILL: e.g., alert owner, pause non-essential jobs, never stop Production without approval>>`
- Cost review every `<<FILL: e.g., month>>` by `<<FILL>>`

---

# 17. PRIVACY AND COMPLIANCE BASICS

Only fill in if you ticked anything other than "None" in Section 1.7. Otherwise write `N/A - no sensitive data`.

- Rules that apply (tick): [ ] GDPR [ ] CCPA/CPRA [ ] HIPAA [ ] PCI-DSS [ ] Children's privacy law (e.g., COPPA) [ ] Other: `<<FILL>>`
- Where is customer data stored (country/region)? `<<FILL>>`
- Is test data free of real customer information? [ ] Yes
- Who is responsible for privacy? `<<FILL>>`
- How can a customer ask for their data to be deleted? `<<FILL>>`
- Evidence kept for audits (e.g., approvals, deployment history, scan results): `<<FILL>>`
- This is a planning aid, not legal advice. Have a qualified person confirm: [ ] Done on `<<FILL: date>>`

---

# 18. RISKS, ASSUMPTIONS AND OPEN QUESTIONS

### 18.1 Top 5 risks

| # | What could go wrong | How likely (Low/Med/High) | How bad (Low/Med/High) | What we do about it | Owner |
|---|---|---|---|---|---|
| 1 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 2 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 3 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 4 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |
| 5 | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` |

### 18.2 Assumptions (things we believe but haven't proven)
`<<FILL>>`

### 18.3 Open questions

| Question | Owner | Answer by |
|---|---|---|
| `<<FILL or "none">>` | `<<FILL>>` | `<<FILL>>` |

### 18.4 Third-party and vendor risk
List every outside service the product or pipeline depends on (payment, email, hosting, AI model provider, login provider, analytics, GitHub Actions marketplace tools).

| Service | What it does for us | What breaks if it goes down | Backup or workaround | Data we send it | Contract / terms reviewed? | Owner |
|---|---|---|---|---|---|---|
| `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | [ ] Yes | `<<FILL>>` |
| `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | `<<FILL>>` | [ ] Yes | `<<FILL>>` |

- [ ] Each vendor's status page is monitored
- [ ] Vendor version changes and shutdown notices are tracked
- [ ] Customer data is only sent to vendors that are approved (Section 17)
- [ ] Marketplace Actions and libraries come from trusted, maintained sources

---

# 19. FINAL COMPLETENESS CHECK (DO THIS BEFORE SIGN-OFF)

- [ ] Search this file for `<<FILL`. **Zero results remain.**
- [ ] Every `N/A` has a reason
- [ ] Every `UNKNOWN` has an owner and a date
- [ ] All Examples were replaced or removed
- [ ] Sections 3, 4, 10, 12 and 15 were reviewed by a second person
- [ ] The Production approvers (3.2) have read the document
- [ ] Branch protection (5.4) and environment protection (11.2) are actually switched on in GitHub, not just written here
- [ ] A test release has been run end to end in Staging using this plan
- [ ] The rollback steps in Section 12 were practiced once

### Sign-off

| Name | Role | Decision (Approve / Changes needed) | Date |
|---|---|---|---|
| `<<FILL>>` | Product owner | | |
| `<<FILL>>` | Tech lead | | |
| `<<FILL>>` | Security owner | | |
| `<<FILL>>` | QA | | |

---

# APPENDIX A: PLAIN-ENGLISH DICTIONARY

| Word | What it means |
|---|---|
| Pipeline | A conveyor belt of automatic steps your code rides on |
| CI | Automatic building and testing every time code changes |
| CD | Automatic or one-click delivery of tested code to environments |
| Repository (repo) | The folder where all your code lives, with history |
| Branch | A separate copy of the code to work on safely |
| Pull request (PR) | A request to add your change to the main code, so others can review it |
| Merge | Combining a branch into the main code |
| Environment | A separate place where your product runs (Dev, Staging, Production) |
| Production | The real product that customers use |
| Staging | A rehearsal copy of Production |
| Artifact / build | The packaged product that gets deployed |
| Deploy | Put a build into an environment |
| Release | Make a feature available to customers |
| Rollback | Go back to the last good version |
| Hotfix | A fast, urgent fix for a Production problem |
| Canary release | Try the new version on a few users first |
| Blue-green | Two identical copies; you switch between them |
| Feature flag | An on/off switch for a feature |
| Smoke test | A quick check that the basics work |
| Flaky test | A test that sometimes passes and sometimes fails for no clear reason |
| SAST | Automatic scan of your code for risky patterns |
| SBOM | A list of every ingredient (library) inside your product |
| Secret | A password, key or token that must stay private |
| OIDC | A safe way for the pipeline to get temporary access without storing passwords |
| Migration | A change to the structure of the database |
| DORA metrics | Four standard numbers that show how healthy your delivery is |
| On-call | The person who must respond when something breaks |
| Blameless review | A meeting that finds out what went wrong without blaming people |
| Cohort | A group of customers let in together |
| Go / no-go | The decision to continue or to stop |
| AI agent | An AI tool that can take actions (write code, open PRs), not only chat |

---

# APPENDIX B: STARTER GITHUB ACTIONS SKELETON

Use this as a starting point and adapt to your tools. Replace placeholders. Pin each third-party Action to a full commit ID in your real file.

```yaml
# .github/workflows/ci.yml
name: CI

on:
  pull_request:
  push:
    branches: [main]

permissions:
  contents: read            # least privilege by default

concurrency:
  group: ci-${{ github.ref }}
  cancel-in-progress: true  # stop old runs when new code is pushed

jobs:
  build-and-test:
    runs-on: ubuntu-latest
    timeout-minutes: 20
    steps:
      - uses: actions/checkout@<FULL_COMMIT_SHA>
      # - set up your language/runtime here
      # - install dependencies (with cache)
      # - lint, type check
      # - unit tests with coverage
      # - build

  security:
    runs-on: ubuntu-latest
    timeout-minutes: 20
    permissions:
      contents: read
      security-events: write
    steps:
      - uses: actions/checkout@<FULL_COMMIT_SHA>
      # - secret scan
      # - dependency scan
      # - code scan (SAST)
      # - license check
      # - generate SBOM
```

```yaml
# .github/workflows/deploy.yml
name: Deploy

on:
  push:
    branches: [main]

permissions:
  contents: read
  id-token: write           # needed for OIDC cloud login

jobs:
  deploy-dev:
    runs-on: ubuntu-latest
    environment: dev
    steps:
      - run: echo "deploy the build to Dev"

  deploy-staging:
    needs: deploy-dev
    runs-on: ubuntu-latest
    environment: staging
    steps:
      - run: echo "deploy the SAME build to Staging, then run smoke tests"

  deploy-production:
    needs: deploy-staging
    runs-on: ubuntu-latest
    environment: production   # configure required reviewers in GitHub settings
    steps:
      - run: echo "release using the chosen strategy, then run smoke tests"
```

---

# APPENDIX C: EXAMPLE OF A WELL-FILLED ANSWER

**Question 12.3: Rollback triggers**

- Weak answer: "If something goes wrong."
- Good answer: "Roll back if the error rate is above 2% for 5 minutes, if login or payment fails for more than 1% of attempts, if any security issue or data exposure is suspected, or if the on-call engineer or release manager decides it is unsafe. Rollback is performed by redeploying the previous build and turning off new feature flags."

**Rule:** A good answer has a **number**, a **name**, or a **clear yes/no test**.

---

# APPENDIX D: CHANGE LOG FOR THIS DOCUMENT

| Version | Date | Who | What changed and why |
|---|---|---|---|
| 1.0 | `<<FILL>>` | `<<FILL>>` | Initial version |
| Template 1.1 | 2026-10-18 | Template author | Added AI agent governance (4.8-4.13), testing strategy (7.5-7.9), accessibility and localization (9.10), post-launch plan (15.11-15.14), cost tracking (16.4), vendor risk (18.4) |
