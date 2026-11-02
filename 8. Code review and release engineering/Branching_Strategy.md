# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**Folder:** Code Review and Release Engineering
**File:** `Branching_Strategy.md`
**Purpose:** Decide, write down, and share exactly how code moves from an idea to a live product, from the first line of code until your first 500 customers are using it. This includes code written by AI agents.
**Reusable:** Copy this file into every new project. Fill it in. Do not edit the questions.

## The 6 rules of filling

1. **Go top to bottom.** Do not skip sections. Each answer helps the next one.
2. **Tick boxes like this:** change `[ ]` to `[x]`. Pick only ONE box unless the question says "pick all that apply".
3. **Every question has three helpers:**
   - 💡 **Example**: a finished answer you can copy.
   - ✅ **Default**: use this if you are not sure. It is always safe.
   - ❓ **Why we ask**: so you understand what the answer is used for.
4. **Write `TBD (owner, date)`** if you truly do not know. Never leave a blank. A blank means someone will guess.
5. **Use real names, not "the usual way".** Write `main`, not "the main one".
6. **When done, run the checklist in Section 20.** If every box is ticked, the document is ready.

## Who can fill this?

Anyone. If you can tick a box and write a short sentence, you can complete this. Where a word is hard, look it up in the **Glossary (Section 22)**.

## Symbols used

| Symbol | Meaning |
|---|---|
| `[ ]` / `[x]` | Empty / chosen box |
| 💡 | Example answer |
| ✅ | Safe default |
| ❓ | Why we ask |
| 🤖 | Rule that applies to AI agents |
| 🛑 | Never do this |
| `<ANGLE_BRACKETS>` | Replace with your own value |

## How AI will use this document

AI coding agents read this file before they create a branch, open a pull request, or touch a release. Write every answer so a machine could follow it without asking you. Be exact: names, numbers, and yes/no.

---

# 1. DOCUMENT CONTROL

| Field | Your answer | 💡 Example |
|---|---|---|
| Project name | | Sunrise App |
| Repository URL | | github.com/acme/sunrise |
| Document owner (one person) | | Priya Sharma |
| Backup owner | | Tom Lee |
| Version of this document | | 1.0 |
| Date created | | 2026-10-18 |
| Date of next review | | 2027-01-18 |
| Status | `[ ] Draft  [ ] In review  [ ] Approved` | Approved |

✅ **Default review date:** 3 months after creation, and again at every customer milestone in Section 13.

---

# 2. PROJECT SNAPSHOT

❓ *Why we ask: these answers pick the right branching model for you in Section 3.*

**2.1 How many people write code (humans only)?**
- [ ] 1 (just me)
- [ ] 2 to 5
- [ ] 6 to 15
- [ ] 16 or more

**2.2 How many AI agents write code or open pull requests?**
- [ ] 0
- [ ] 1 to 3
- [ ] 4 or more

**2.3 Which Git host do you use?**
- [ ] GitHub
- [ ] GitLab
- [ ] Bitbucket
- [ ] Azure DevOps
- [ ] Other: ____________

**2.4 How often do you want to release to users?**
- [ ] Many times a day
- [ ] About once a week
- [ ] About once a month
- [ ] Only when a big thing is finished

✅ **Default:** About once a week.

**2.5 What kind of product is it?**
- [ ] Website or web app (we can update it any time)
- [ ] Mobile app (app stores must approve each version)
- [ ] Desktop or installed software
- [ ] API or backend only
- [ ] Hardware or firmware
- [ ] Other: ____________

**2.6 Do automated tests exist today?**
- [ ] Yes, and they run on every change
- [ ] Yes, but run by hand
- [ ] A few
- [ ] No

**2.7 Are there legal or safety rules? (pick all that apply)**
- [ ] None
- [ ] Handles payments (PCI)
- [ ] Handles health data (HIPAA)
- [ ] Handles EU personal data (GDPR)
- [ ] Needs audit trails (SOC 2, ISO 27001)
- [ ] Other: ____________

**2.8 Where are you in the product's life right now?**
- [ ] Idea or prototype
- [ ] Building the first version (MVP)
- [ ] Private beta
- [ ] Launched, fewer than 500 customers
- [ ] More than 500 customers

---

# 3. CHOOSE YOUR BRANCHING MODEL

## 3.1 Answer these four questions

| # | Question | Yes | No |
|---|---|---|---|
| A | Do you release at least once a week? | +1 Trunk | +1 Release |
| B | Do automated tests run on every change? | +1 Trunk | +1 Release |
| C | Can you switch features on or off without redeploying? | +1 Trunk | +1 Release |
| D | Do you have to support several old versions at once (for example mobile apps or installed software)? | +1 Release | +1 Trunk |

Add the points. **Your score: Trunk = ___ Release = ___**

## 3.2 Pick your model

| If you scored | Choose | In one sentence |
|---|---|---|
| Trunk 3 or 4 | **Trunk-Based Development** | Everyone merges small changes to `main` many times a day. |
| Trunk 2, Release 2 | **GitHub Flow** | Short-lived branches, review, merge to `main`, deploy from `main`. |
| Release 3 or 4 | **Release-Branch Flow (GitFlow-lite)** | `main` plus `develop` plus release branches for stable versions. |

✅ **Default if unsure or if the project has 1 to 5 people:** **GitHub Flow.**

**Our chosen model (tick one):**
- [ ] Trunk-Based Development
- [ ] GitHub Flow
- [ ] Release-Branch Flow (GitFlow-lite)

**Reason in one sentence:** ______________________________________________

💡 *Example: "GitHub Flow, because we are 4 people, release weekly, and have tests on every change."*

## 3.3 What this model looks like (keep ONLY the one you chose, delete the other two)

### Model A: Trunk-Based Development
- One long-lived branch: `main`.
- Branches live **less than 1 day** (maximum 2).
- Unfinished work is hidden behind **feature flags**.
- Every merge to `main` must keep `main` deployable.

### Model B: GitHub Flow
- One long-lived branch: `main`. It is always deployable.
- Create a short branch from `main`, open a pull request (PR), get review, pass checks, merge, delete the branch.
- Branches live **less than 5 days**.

### Model C: Release-Branch Flow (GitFlow-lite)
- Long-lived branches: `main` (what customers have) and `develop` (what we are building next).
- Short-lived: `feature/*` from `develop`; `release/*` from `develop` when ready to ship; `hotfix/*` from `main`.
- After a release, merge back into **both** `main` and `develop`.

---

# 4. BRANCH TYPES AND NAMES

❓ *Why we ask: a clear name tells everyone, human or AI, what the branch is for and who owns it.*

## 4.1 Long-lived branches (they never get deleted)

| Branch | Used? | Purpose |
|---|---|---|
| `main` | `[x]` Always | Production-ready code. What customers get. |
| `develop` | `[ ] Yes  [ ] No` | Next-release work. Only for Model C. |
| `staging` | `[ ] Yes  [ ] No` | Optional. A copy for final testing. |

## 4.2 Short-lived branches (delete after merging)

| Type | Name pattern | Created from | Merges into | Lifetime limit |
|---|---|---|---|---|
| Feature | `feature/<ticket-id>-<short-words>` | | | ___ days |
| Bug fix | `fix/<ticket-id>-<short-words>` | | | ___ days |
| Hotfix (emergency) | `hotfix/<ticket-id>-<short-words>` | `main` | `main` (+ `develop` in Model C) | 1 day |
| Release | `release/<version>` | | | ___ days |
| Documentation | `docs/<short-words>` | | | ___ days |
| Chore (tools, cleanup) | `chore/<short-words>` | | | ___ days |
| Experiment | `exp/<name>` | | Never merged directly | 14 days |
| 🤖 AI agent | `ai/<agent-name>/<ticket-id>-<short-words>` | | | ___ days |

✅ **Defaults:** feature/fix = 3 days, release = 7 days, docs/chore = 2 days, AI = 2 days. Created from `main` (Models A and B) or `develop` (Model C).

💡 *Examples: `feature/SUN-142-login-page`, `fix/SUN-201-crash-on-save`, `ai/claude/SUN-310-add-search`.*

## 4.3 Naming rules

- [ ] All lowercase
- [ ] Words separated with hyphens, never spaces
- [ ] A ticket ID is required in every branch name (use `NOTICKET` only for docs and chores)
- [ ] Maximum length: ___ characters (✅ default 60)

🛑 **Never use:** `test`, `new`, `final`, `temp`, `my-branch`, a person's name alone.

**Where do ticket IDs come from?**
- [ ] Jira  [ ] GitHub Issues  [ ] Linear  [ ] Other: ________

---

# 5. PROTECTED BRANCHES (THE LOCKS)

❓ *Why we ask: locks stop accidents. A locked `main` cannot be broken by one bad push.*

Tick every rule you turn ON for `main`. ✅ Recommended rules are marked.

| Rule | `main` | `develop` | Recommended |
|---|---|---|---|
| No direct pushes, PRs only | `[ ]` | `[ ]` | ✅ Yes |
| Require at least ___ approvals | `[ ]` | `[ ]` | ✅ 1 (2 after launch) |
| Dismiss approvals when new code is pushed | `[ ]` | `[ ]` | ✅ Yes |
| Require all CI checks to pass | `[ ]` | `[ ]` | ✅ Yes |
| Require branch to be up to date before merge | `[ ]` | `[ ]` | ✅ Yes |
| Require all comments resolved | `[ ]` | `[ ]` | ✅ Yes |
| Require signed commits | `[ ]` | `[ ]` | Optional |
| Require linear history | `[ ]` | `[ ]` | ✅ Yes |
| Block force-push | `[ ]` | `[ ]` | ✅ Yes |
| Block branch deletion | `[ ]` | `[ ]` | ✅ Yes |
| Admins must follow the rules too | `[ ]` | `[ ]` | ✅ Yes |
| Code owners must approve their files | `[ ]` | `[ ]` | ✅ Yes after 3+ people |

**Who can bypass the locks in a real emergency?** (name or role): ____________
**How is a bypass recorded?** ____________ (✅ default: a comment on the incident ticket within 24 hours)

---

# 6. COMMITS AND PULL REQUESTS

## 6.1 Commit message format

- [ ] Conventional Commits: `type(scope): short summary`  (✅ default)
- [ ] Other: ____________

💡 *Examples: `feat(search): add filter by date`, `fix(login): stop crash on empty email`.*

Allowed types: `feat`, `fix`, `docs`, `chore`, `refactor`, `test`, `perf`, `ci`, `revert`.
Summary: 72 characters or fewer, present tense, no full stop.

## 6.2 Pull request rules

| Question | Your answer | ✅ Default |
|---|---|---|
| Maximum size of a PR (lines changed) | | 400 |
| Must link to a ticket? | `[ ] Yes [ ] No` | Yes |
| PR title follows commit format? | `[ ] Yes [ ] No` | Yes |
| Draft PRs allowed? | `[ ] Yes [ ] No` | Yes |
| Must have a description with "What, Why, How tested"? | `[ ] Yes [ ] No` | Yes |
| Must include screenshots for visible changes? | `[ ] Yes [ ] No` | Yes |

## 6.3 PR template (paste this into `.github/pull_request_template.md` or your host's equivalent)

```
## What changed?
## Why?
## How was it tested?
## Ticket link:
## Screenshots (if visible):
## Risk level: [ ] Low  [ ] Medium  [ ] High
## Rollback plan (one line):
## Checklist
- [ ] Tests added or updated
- [ ] Docs updated
- [ ] No secrets or keys in the code
- [ ] Feature flag used if unfinished
```

---

# 7. CODE REVIEW RULES

| Question | Your answer | ✅ Default |
|---|---|---|
| Who may review? | | Any teammate except the author |
| Number of approvals needed before launch | | 1 |
| Number of approvals needed after launch | | 2 for high-risk changes, 1 otherwise |
| Reviewer must reply within | ___ working hours | 24 |
| If no reply, escalate to | | Document owner |
| Can authors approve their own PR? | `[ ] Yes [x] No` | No |

**What reviewers must check (tick to keep):**
- [ ] It does what the ticket says
- [ ] Tests exist and pass
- [ ] No secrets, passwords, or keys
- [ ] No obvious security problem
- [ ] Easy to read and understand
- [ ] Database changes are safe (Section 17)
- [ ] 🤖 If AI wrote it: a human has read **every line**

**High-risk changes always need 2 approvals (tick all that apply):**
- [ ] Payments or billing  [ ] Login or permissions  [ ] Personal data
- [ ] Database structure  [ ] Deployment or infrastructure  [ ] Other: ______

---

# 8. AUTOMATED CHECKS (QUALITY GATES)

❓ *Why we ask: a machine checks every change the same way, every time, so people can focus on thinking.*

Tick the checks that **must pass** before merging.

| Check | Required on PR? | Tool name | ✅ Default |
|---|---|---|---|
| Build succeeds | `[ ]` | | Yes |
| Unit tests | `[ ]` | | Yes |
| Integration tests | `[ ]` | | Yes after MVP |
| Linting and formatting | `[ ]` | | Yes |
| Type checking | `[ ]` | | Yes if language supports it |
| Test coverage at least ___% | `[ ]` | | 70% |
| Dependency vulnerability scan | `[ ]` | | Yes |
| Secret scanning | `[ ]` | | Yes |
| Static security scan (SAST) | `[ ]` | | Yes after launch |
| License check | `[ ]` | | Optional |
| Performance check | `[ ]` | | After 100 customers |
| Preview deployment | `[ ]` | | Yes for web |

**Maximum time allowed for all checks:** ___ minutes (✅ default 10)
**What if a check is flaky (fails randomly)?** (✅ default: open a ticket within 1 day and fix within 1 week; never just re-run forever)

---

# 9. HOW TO MERGE

| Target branch | Merge method | ✅ Default |
|---|---|---|
| Feature or fix into `main` / `develop` | `[ ] Squash  [ ] Rebase  [ ] Merge commit` | Squash |
| `release/*` into `main` | `[ ] Squash  [ ] Rebase  [ ] Merge commit` | Merge commit |
| `main` back into `develop` (Model C) | `[ ] Squash  [ ] Rebase  [ ] Merge commit` | Merge commit |
| `hotfix/*` into `main` | `[ ] Squash  [ ] Rebase  [ ] Merge commit` | Squash |

**Delete the branch after merge?** `[x] Yes, automatically`

**If there is a conflict:** the **author** fixes it by updating their branch from `main` (or `develop`). The reviewer never resolves it for them.

---

# 10. 🤖 AI AGENT RULES

❓ *Why we ask: AI agents are fast and tireless, but they can be confidently wrong. These rules keep humans in charge.*

## 10.1 Which AI agents work in this project?

| Agent name | What it may do | Owner (human) |
|---|---|---|
| | | |
| | | |

💡 *Example: Claude Code, may write code on `ai/*` branches and open PRs, owner Priya.*

## 10.2 What AI agents may do (tick to allow)

- [ ] Create branches named `ai/<agent>/...`
- [ ] Commit to its own branch
- [ ] Open pull requests
- [ ] Respond to review comments
- [ ] Update documentation
- [ ] Run tests and fix failing ones
- [ ] Update dependencies (✅ default: only patch versions)

## 10.3 🛑 What AI agents must NEVER do

- Push directly to `main`, `develop`, `staging`, or any `release/*` or `hotfix/*` branch
- Approve or merge its own pull request
- Force-push, delete protected branches, or rewrite shared history
- Change CI settings, branch protection, or permissions
- Add, read, or print secrets, keys, tokens, or customer data
- Create or publish a release tag or deploy to production
- Run database migrations against production
- Disable or delete tests to make them pass

## 10.4 Human-in-the-loop

| Question | Your answer | ✅ Default |
|---|---|---|
| Who reviews AI-written PRs? | | A human who did not prompt it |
| Mark AI-written commits with | | `Co-authored-by:` line or `[ai]` label |
| Max size of an AI PR (lines) | | 300 |
| Max open AI PRs at once per agent | | 3 |
| AI work on high-risk areas (Section 7) | `[ ] Allowed  [ ] Needs extra approval  [ ] Forbidden` | Needs extra approval |
| Where is the agent's instruction file? | | `AGENTS.md` or `CLAUDE.md` at repo root |

## 10.5 Agent handoff note (agent adds this to every PR)

```
Agent: <name and version>
Task given: <the ticket or prompt>
What I changed: <files and reason>
What I did NOT change: <anything skipped or uncertain>
How I tested: <commands run and results>
Things a human must double-check: <list>
```

---

# 11. ENVIRONMENTS AND WHICH BRANCH GOES WHERE

| Environment | Branch or tag that deploys here | Deploys how? | Who can approve? |
|---|---|---|---|
| Local / preview | any PR branch | `[ ] Auto  [ ] Manual` | Anyone |
| Development | `develop` or `main` | `[ ] Auto  [ ] Manual` | |
| Staging | `main` or `release/*` | `[ ] Auto  [ ] Manual` | |
| Production | tag `vX.Y.Z` | `[ ] Auto  [ ] Manual` | |

✅ **Default:** previews and development deploy automatically; staging deploys automatically; production needs one named human to press the button.

**Name the person or role who may deploy to production:** ____________
**Allowed deploy days and times:** ____________ (✅ default: Monday to Thursday, 10:00 to 15:00 local time; never Friday afternoon or before a holiday)

---

# 12. VERSIONS, TAGS AND RELEASES

## 12.1 Version numbers

- [ ] Semantic Versioning `MAJOR.MINOR.PATCH` (✅ default)
  - MAJOR = breaking change, MINOR = new feature, PATCH = bug fix
- [ ] Calendar versioning `YYYY.MM.DD`
- [ ] Other: ____________

**First public version number:** ____________ (✅ default `1.0.0`; use `0.x.y` before launch)

## 12.2 Tags

- Tag format: `v<VERSION>` (💡 `v1.4.2`)
- Who creates tags? ____________ (🤖 never an AI agent)
- Tags are protected from deletion? `[x] Yes`

## 12.3 Release checklist (every release)

- [ ] All planned tickets merged
- [ ] All CI checks green on the release commit
- [ ] Release notes / changelog written
- [ ] Database migrations tested on staging (Section 17)
- [ ] Rollback plan written and tested
- [ ] Support team told
- [ ] Monitoring dashboard open during release
- [ ] Tag created and release published
- [ ] Post-release check done (Section 15)

## 12.4 Feature flags

| Question | Your answer | ✅ Default |
|---|---|---|
| Do we use feature flags? | `[ ] Yes [ ] No` | Yes |
| Flag tool | | |
| Every unfinished feature hidden behind a flag? | `[ ] Yes [ ] No` | Yes |
| Maximum life of a flag before it must be removed | ___ days | 30 after full rollout |
| Who owns flag cleanup? | | The feature's author |

---

# 13. THE JOURNEY: DEVELOPMENT TO YOUR FIRST 500 CUSTOMERS

❓ *Why we ask: the right rules change as you grow. Few customers means move fast. More customers means protect them. Fill in each phase so everyone knows which rules are active today.*

**Tick the phase you are in today:** `[ ] 1  [ ] 2  [ ] 3  [ ] 4  [ ] 5  [ ] 6`

## Phase table (edit the numbers, keep the shape)

| Phase | Name | Customers | Branching rules that apply | ✅ Default exit rule |
|---|---|---|---|---|
| 1 | **Build the MVP** | 0 | Short branches, 1 approval, CI required, no release branches | MVP features done and tested |
| 2 | **Private beta** | 1 to 20 | Same, plus feature flags, staging deploy, tags `v0.x` | 20 customers and no critical bugs for 7 days |
| 3 | **Launch** | 20 to 50 | Release freeze 24 hours before launch, tag `v1.0.0`, rollback tested | Launch done and stable for 7 days |
| 4 | **Early growth** | 50 to 150 | 2 approvals for high-risk, staged rollout (10% to 50% to 100%), hotfix process live | 150 customers and 14 days stable |
| 5 | **Scale-up** | 150 to 350 | Code owners required, SAST scans, performance checks, on-call rota | 350 customers |
| 6 | **Milestone: 500** | 350 to 500+ | All rules in this document, quarterly branch audit, release train | 500 paying or active customers |

**Fill in YOUR numbers:**

| Phase | Starts when | Ends when | Owner |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 | | | |

**What counts as a "customer" for us?** (✅ one clear sentence)
- [ ] A person who signed up
- [ ] A person who used the product at least once in 30 days
- [ ] A person or company who paid
- [ ] Other: ____________

**Which tighter rules switch on at each milestone? (tick all that apply)**

| Milestone | Rule that switches on |
|---|---|
| 1st customer | `[ ] Protected main  [ ] Rollback plan in every PR  [ ] Monitoring alerts` |
| 20 customers | `[ ] Feature flags required  [ ] Staging environment  [ ] Release notes` |
| 50 customers | `[ ] Freeze before releases  [ ] Hotfix process  [ ] On-call person named` |
| 100 customers | `[ ] 2 approvals for high-risk  [ ] Staged rollouts  [ ] Status page` |
| 250 customers | `[ ] Code owners  [ ] Security scans  [ ] Quarterly access review` |
| 500 customers | `[ ] Full audit of branches, tags and access  [ ] Review this document` |

**Phase-change rule:** The document owner updates the "Phase today" tick and adds a line in the Change Log (Section 23). Changes to rules take effect on the **next business day**.

---

# 14. HOTFIXES (EMERGENCY FIXES)

❓ *Why we ask: when customers are hurt, people panic. A written path prevents mistakes under stress.*

**14.1 What counts as an emergency? (tick all that apply)**
- [ ] The product is down for many customers
- [ ] Customers lose data or money
- [ ] A security hole is being exploited
- [ ] A legal or privacy problem
- [ ] A key feature is broken for more than ___% of customers (✅ default 10%)
- [ ] Other: ____________

**14.2 Who may declare an emergency?** ____________ (✅ default: the on-call person or document owner)

**14.3 Hotfix steps (edit if needed)**

1. Open an incident ticket. Write the time.
2. Create `hotfix/<ticket>-<words>` from `main` (or from the production tag).
3. Make the **smallest possible** fix. No extras.
4. Run the fast checks (✅ default: build, unit tests, secret scan).
5. Get **1 approval** from a person who is not the author.
6. Merge into `main` (and into `develop` in Model C).
7. Tag a PATCH version (💡 `v1.4.3`) and deploy.
8. Check the product works. Watch the dashboard for 30 minutes.
9. Write a short incident note within 48 hours.
10. Delete the hotfix branch.

🤖 **AI agents may draft a hotfix branch and PR, but a human must review, merge, tag, and deploy.**

---

# 15. ROLLBACK (UNDOING A BAD RELEASE)

| Question | Your answer | ✅ Default |
|---|---|---|
| Fastest way to undo | `[ ] Redeploy previous tag  [ ] Turn off feature flag  [ ] Revert commit  [ ] Restore backup` | Turn off flag, else redeploy previous tag |
| Time allowed to start rollback after a problem is confirmed | ___ minutes | 15 |
| Who decides to roll back? | | On-call person |
| Is the previous version always kept ready? | `[ ] Yes [ ] No` | Yes, last 3 tags |
| Who tells customers? | | Support lead |
| Reverting a commit: use | | `git revert`, never `git reset` on shared branches |

**Post-release health check (do it every release):**
- [ ] Error rate is normal
- [ ] Page or API speed is normal
- [ ] Login and main action work
- [ ] No spike in support messages
- [ ] Checked at 5 minutes, 30 minutes, and 24 hours

**Watch these numbers:** ____________ (💡 error rate, response time, sign-ups per hour)

---

# 16. LONG-LIVED BRANCH HYGIENE AND CLEANUP

| Rule | Your answer | ✅ Default |
|---|---|---|
| Warn if a branch has no activity for | ___ days | 7 |
| Auto-delete stale branches after | ___ days | 30 |
| Who checks old branches? | | Document owner, every month |
| Delete merged branches automatically? | `[ ] Yes [ ] No` | Yes |
| Keep release branches for | | Until the version is no longer supported |
| Which old versions do we still support? | | Latest only |

**Quarterly audit checklist:**
- [ ] No stray long-lived branches
- [ ] Protection rules still match Section 5
- [ ] Access list is correct (people who left are removed)
- [ ] AI agent permissions still match Section 10

---

# 17. DATABASE, CONFIG AND SECRETS

**17.1 Database changes**

| Question | Your answer | ✅ Default |
|---|---|---|
| Do we use migrations (versioned database changes)? | `[ ] Yes [ ] No` | Yes |
| Migration lives in the same PR as the code? | `[ ] Yes [ ] No` | Yes |
| Must be backward compatible with the previous release? | `[ ] Yes [ ] No` | Yes |
| Tested on a copy of production data shape first? | `[ ] Yes [ ] No` | Yes |
| Destructive changes (drop column or table) | | Two releases: stop using it, then remove it |
| Who runs production migrations? | | A human, never an AI agent |

**17.2 Secrets and settings**
- 🛑 Never commit passwords, API keys, tokens, or private keys, even in a private repository or an old commit.
- Where secrets live: ____________ (💡 GitHub Secrets, Vault, AWS Secrets Manager)
- If a secret leaks: rotate it **first**, then clean the history, then write an incident note.

---

# 18. WHO DOES WHAT (ROLES)

| Role | Name | Can do |
|---|---|---|
| Document owner | | Edit this document, approve exceptions |
| Repo admin | | Change branch protection |
| Release manager | | Create tags, approve production deploys |
| Reviewer(s) | | Approve PRs |
| On-call person | | Declare emergencies, roll back |
| AI agent owner | | Manage agent permissions and instructions |

✅ **Default for a team of 1 to 3:** one person may hold several roles, but the author of a change must never be its only approver. If working alone, wait for checks to pass and use a 10-minute self-review checklist plus an AI review as a second pair of eyes.

---

# 19. EXCEPTIONS AND DISPUTES

**Can rules be broken?** `[ ] Never  [ ] Only in emergencies  [ ] With written approval` (✅ default: only in emergencies, with approval recorded within 24 hours)

**Exception log (add a row every time):**

| Date | Rule broken | Why | Approved by | Follow-up done? |
|---|---|---|---|---|
| | | | | |

**If two people disagree about a rule:** the document owner decides within ___ working days (✅ default 2) and records it in the Change Log.

---

# 20. FINAL CHECKLIST: IS THIS DOCUMENT READY?

Tick every box. If one is empty, go back to that section.

- [ ] Section 1: every field filled, owner named
- [ ] Section 2: all eight questions answered
- [ ] Section 3: one model chosen, other two models deleted
- [ ] Section 4: every branch type has a name pattern and a time limit
- [ ] Section 5: protection rules switched on in the Git host (not just written here)
- [ ] Section 6: PR template added to the repository
- [ ] Section 7: reviewer rules and high-risk list filled
- [ ] Section 8: automated checks set up and required
- [ ] Section 9: merge methods chosen
- [ ] Section 10: AI agents listed with a human owner and never-do rules copied into `AGENTS.md` or `CLAUDE.md`
- [ ] Section 11: every environment has a branch and an approver
- [ ] Section 12: version style, tag rule and release checklist set
- [ ] Section 13: current phase ticked, "customer" defined, milestones filled
- [ ] Section 14: hotfix steps and emergency definition agreed
- [ ] Section 15: rollback method tested at least once on staging
- [ ] Section 16: cleanup rules set
- [ ] Section 17: database and secrets rules set
- [ ] Section 18: every role has a name
- [ ] Section 19: exception and dispute rules set
- [ ] Appendices A to D: each one filled in, or marked `Not applicable`
- [ ] Appendix D configs copied into the repository and match the answers above
- [ ] No blank answers, only `TBD (owner, date)`
- [ ] A person who did not fill the document read it and understood it
- [ ] The team has been told where this file lives

**Final sign-off**

| Role | Name | Date | Signature or approval link |
|---|---|---|---|
| Document owner | | | |
| Engineering lead | | | |
| Product or business owner | | | |

---

# 21. QUICK REFERENCE CARD (print this, pin it up)

```
1. Start from:      main  (or develop in Model C)
2. Name it:         type/TICKET-short-words
3. Keep it small:   under 400 lines, under the day limit
4. Open a PR:       use the template
5. Wait for green:  all checks must pass
6. Get a review:    1 approval (2 if high-risk)
7. Merge:           squash, delete the branch
8. Release:         tag vX.Y.Z, human deploys
9. Trouble?         roll back first, fix second
10. AI agent?       ai/<agent>/... branch, human reviews every line, never touches main
```

---

# 22. GLOSSARY (PLAIN WORDS)

| Word | What it means |
|---|---|
| **Repository (repo)** | The folder where all your project's code and its history live. |
| **Branch** | A separate copy of the code where you can work without breaking the main one. |
| **main** | The branch that holds the real, working product. |
| **Commit** | A saved step of your work with a short note about it. |
| **Pull request (PR)** | A request to add your branch's changes into another branch, so others can check it first. |
| **Merge** | Combining one branch into another. |
| **Squash** | Folding many small commits into one tidy commit. |
| **Rebase** | Replaying your commits on top of newer code to keep history straight. |
| **Conflict** | Two people changed the same line and Git needs a human to choose. |
| **Tag** | A permanent label on one exact moment of code, like `v1.0.0`. |
| **Release** | A version of the product that customers receive. |
| **Hotfix** | A tiny, fast fix for an emergency in production. |
| **Rollback** | Going back to the last version that worked. |
| **CI (Continuous Integration)** | A robot that builds and tests every change automatically. |
| **CD (Continuous Delivery or Deployment)** | A robot that carries tested code to the environments. |
| **Feature flag** | An on/off switch that hides unfinished features from customers. |
| **Protected branch** | A branch with locks so nobody can break it by accident. |
| **Code owner** | The person responsible for approving changes to certain files. |
| **Environment** | A place where the product runs: preview, development, staging, production. |
| **Staging** | A practice copy of production used for final testing. |
| **Production** | The real product that customers use. |
| **Migration** | A saved, repeatable change to the database structure. |
| **Semantic Versioning** | Version numbers MAJOR.MINOR.PATCH that tell you how big a change is. |
| **AI agent** | A program driven by AI that can write code, run commands, and open PRs on its own. |
| **Human in the loop** | A real person must check and approve before something important happens. |
| **MVP** | Minimum Viable Product: the smallest version worth giving to real users. |
| **On-call** | The person responsible for answering emergencies this week. |

---

# 23. CHANGE LOG

| Version | Date | Changed by | What changed and why |
|---|---|---|---|
| 1.0 | | | First version of this document |

---

# 24. OPEN QUESTIONS (WRITE `TBD` ITEMS HERE)

| # | Question | Owner | Due date | Answer |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |

---

# OPTIONAL APPENDICES (FILL ONLY THE ONES THAT APPLY TO YOU)

Each appendix starts with a **"Does this apply to me?"** question. If the answer is No, write `Not applicable` and move on.

---

# APPENDIX A: MONOREPO AND MULTI-REPO

**A.1 Does this apply to me?**
- [ ] No, one repository with one product → write `Not applicable`
- [ ] Yes, one repository holding several apps or packages (monorepo)
- [ ] Yes, several repositories that work together (multi-repo)

**A.2 If monorepo**

| Question | Your answer | ✅ Default |
|---|---|---|
| List each app or package and its folder | | |
| One version number for everything, or one per package? | `[ ] One  [ ] Per package` | One while under 5 packages |
| Run tests only for changed folders? | `[ ] Yes [ ] No` | Yes |
| Tag format for per-package versions | | `<package>@v<VERSION>` (💡 `web@v1.2.0`) |
| Who owns each folder (CODEOWNERS)? | | See Appendix D |
| Can one PR change several packages? | `[ ] Yes [ ] No` | Yes if they must change together |

**A.3 If multi-repo**

| Question | Your answer | ✅ Default |
|---|---|---|
| List all repositories and what each one does | | |
| Does every repo follow THIS document? | `[ ] Yes [ ] No` | Yes |
| Where do shared libraries live? | | Own repo, versioned with tags |
| How do repos depend on each other? | `[ ] Version number  [ ] Git submodule  [ ] Package registry` | Version number via package registry |
| Release order when several repos change | | Shared libraries first, then services, then front ends |
| Branch names must match across repos for one feature? | `[ ] Yes [ ] No` | Yes (same ticket ID) |

🤖 **AI agents:** an agent working across several repos opens **one PR per repo**, links them to each other, and states the merge order in each PR.

---

# APPENDIX B: MOBILE APP RELEASES

**B.1 Does this apply to me?**
- [ ] No → write `Not applicable`
- [ ] Yes, iOS  [ ] Yes, Android  [ ] Yes, both

❓ *Why we ask: app stores must approve every version, so you cannot fix a mistake in minutes. Old versions stay on people's phones for months.*

| Question | Your answer | ✅ Default |
|---|---|---|
| Release branch for every store submission? | `[ ] Yes [ ] No` | Yes: `release/<version>` |
| Build number rule | | Goes up by 1 on every build, never reused |
| Time reserved for store review | ___ days | iOS 3, Android 2 |
| Code freeze before submitting | ___ hours | 48 |
| Phased rollout steps | | 1% → 10% → 50% → 100% |
| Pause rollout if crash-free users falls below | ___% | 99% |
| Hotfix for mobile | | Branch from the release tag, submit as expedited review, also ship a server-side fix or feature flag where possible |
| Oldest app version we still support | | Last 3 versions |
| Can we force users to update? | `[ ] Yes [ ] No` | Yes, for security or breaking-API fixes |
| Server must stay compatible with old apps for | ___ months | 6 |
| Who owns store accounts and signing keys? | | Release manager, keys in secrets vault, never in the repo |

**Mobile release checklist**
- [ ] Version and build numbers bumped
- [ ] Tested on at least ___ real devices (✅ default 3)
- [ ] Store notes and screenshots ready
- [ ] Remote feature flags set for risky parts
- [ ] Crash reporting working
- [ ] Rollout plan and pause plan agreed

---

# APPENDIX C: COMPLIANCE AND AUDIT

**C.1 Does this apply to me?**
- [ ] No → write `Not applicable`
- [ ] Yes, we need to show auditors or customers how code reaches production

Tick the standards you follow: `[ ] SOC 2  [ ] ISO 27001  [ ] PCI DSS  [ ] HIPAA  [ ] GDPR  [ ] Other: ________`

❓ *Why we ask: auditors want proof that no single person can push untested code to production. This section gathers that proof in one place.*

| Control | Your answer | ✅ Default |
|---|---|---|
| Two different people for author and approver | `[ ] Yes [ ] No` | Yes, enforced by branch protection |
| Signed commits required | `[ ] Yes [ ] No` | Yes |
| Admins can bypass? | `[ ] Yes [ ] No` | No; bypass needs a written record |
| Every change linked to a ticket | `[ ] Yes [ ] No` | Yes |
| Evidence kept in | | Git host history, ticket system, CI logs |
| How long evidence is kept | ___ months | 12 (check your standard; some need longer) |
| Separation of duties (the person who writes cannot also deploy to production) | `[ ] Yes [ ] No` | Yes |
| Access reviews | | Every quarter |
| Emergency change record | | Incident ticket plus follow-up review within 48 hours |
| Release approvals recorded where? | | Deployment tool approval log |
| Who talks to auditors? | | |

**Evidence pack (collect before every audit):**
- [ ] Screenshot or export of branch protection settings
- [ ] List of people with write and admin access
- [ ] Sample of 10 recent PRs showing ticket, review, passing checks
- [ ] Exception log (Section 19)
- [ ] Incident notes for every hotfix (Section 14)
- [ ] Access review sign-offs

🤖 **AI agents in audited projects:** record the agent name and version in every PR, and keep the agent handoff note (Section 10.5) as evidence.

---

# APPENDIX D: COPY-PASTE CONFIGS

⚠️ These are starting points. Replace anything in `<ANGLE_BRACKETS>`, and check each one against your own answers above. They assume GitHub; ask for equivalents if you use another host.

## D.1 CODEOWNERS (file: `.github/CODEOWNERS`)

```
# Everything needs the document owner by default
*                       @<DOC_OWNER_HANDLE>

# High-risk areas (see Section 7)
/payments/              @<PAYMENTS_OWNER> @<SECOND_REVIEWER>
/auth/                  @<SECURITY_OWNER> @<SECOND_REVIEWER>
/db/migrations/         @<DATABASE_OWNER> @<SECOND_REVIEWER>
/.github/               @<REPO_ADMIN>
/infrastructure/        @<INFRA_OWNER>
/Branching_Strategy.md  @<DOC_OWNER_HANDLE>
/AGENTS.md              @<DOC_OWNER_HANDLE>
```

## D.2 Branch protection for `main` (GitHub REST API body)

Send with `PUT /repos/<OWNER>/<REPO>/branches/main/protection`. Match the check names to your CI job names.

```json
{
  "required_status_checks": {
    "strict": true,
    "contexts": ["build", "test", "lint", "secret-scan"]
  },
  "enforce_admins": true,
  "required_pull_request_reviews": {
    "required_approving_review_count": 1,
    "dismiss_stale_reviews": true,
    "require_code_owner_reviews": false
  },
  "restrictions": null,
  "required_linear_history": true,
  "allow_force_pushes": false,
  "allow_deletions": false,
  "required_conversation_resolution": true
}
```

After launch (Phase 3 onward) change `required_approving_review_count` to `2` for high-risk paths and set `require_code_owner_reviews` to `true`.

## D.3 CI workflow that enforces naming (file: `.github/workflows/pr-checks.yml`)

```yaml
name: pr-checks
on:
  pull_request:
    branches: [main, develop]

jobs:
  branch-name:
    runs-on: ubuntu-latest
    steps:
      - name: Check branch name
        env:
          BRANCH: ${{ github.head_ref }}
        run: |
          # Matches Section 4.2: type/TICKET-short-words (lowercase, hyphens)
          # AI branches look like ai/<agent>/TICKET-short-words
          if [[ ! "$BRANCH" =~ ^(feature|fix|hotfix|docs|chore|exp|release)/[A-Za-z0-9._-]+$ \
             && ! "$BRANCH" =~ ^ai/[a-z0-9-]+/[A-Za-z0-9._-]+$ ]]; then
            echo "Branch name '$BRANCH' does not follow Section 4 of Branching_Strategy.md"
            exit 1
          fi

  pr-title:
    runs-on: ubuntu-latest
    permissions:
      pull-requests: read
    steps:
      - uses: amannn/action-semantic-pull-request@v5
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      # Add your language setup here (setup-node, setup-python, ...)
      - run: <YOUR_BUILD_COMMAND>

  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: <YOUR_TEST_COMMAND>

  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: <YOUR_LINT_COMMAND>
```

## D.4 Release tagging (what a human types)

```
git checkout main
git pull
git tag -a v1.0.0 -m "Release 1.0.0"
git push origin v1.0.0
```

## D.5 Rollback by reverting (what a human types)

```
git checkout main
git pull
git revert <BAD_COMMIT_ID>      # for a merge commit use: git revert -m 1 <MERGE_COMMIT_ID>
git push origin HEAD            # goes through a PR if main is protected
```

## D.6 Agent instruction file (file: `AGENTS.md` or `CLAUDE.md` at repo root)

```
# Rules for AI agents in this repository
Read Branching_Strategy.md before doing any work.

- Create branches only as: ai/<your-name>/<TICKET>-<short-words>
- Start from: <main or develop>
- Open a pull request; never push to main, develop, release/*, or hotfix/*
- Never approve or merge your own PR
- Never force-push, change CI or branch protection, or touch secrets
- Never tag, deploy, or run production migrations
- Keep PRs under <300> changed lines and have at most <3> open at once
- Put the agent handoff note (Section 10.5) in every PR description
- If a task needs something forbidden above, stop and ask a human
```
