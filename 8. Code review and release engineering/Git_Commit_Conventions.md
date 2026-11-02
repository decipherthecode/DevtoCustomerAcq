# How to Fill This Document

> **Read this box first. It takes 3 minutes.**

## What is this file?
This is your **Git Commit Conventions template**. It is one file that explains *how every change to your product is saved, labeled, reviewed, and released*, from the first idea until your **first 500 customers** are using it.

Think of it like a **video game**. Every time you press "Save", the game stores a **save point**. In Git, a save point is called a **commit**. If every save point has a clear label, like "Level 3: added the shop", you can always find the right one and go back if something breaks. This document teaches everyone (people and AI agents) to write the same kind of clear label.

## How to fill it (4 simple rules)

| # | Rule | What it means |
|---|------|---------------|
| 1 | **Go top to bottom** | Sections are in order. Do not skip ahead. |
| 2 | **Answer every `✍️ YOUR ANSWER`** | Type your answer on that line. Short is fine. |
| 3 | **Keep `🔒 DEFAULT` if you are unsure** | Defaults are already the best-practice choice. Only change one if you have a reason, and write the reason. |
| 4 | **Never leave a blank** | If something does not apply, write `N/A - because ...`. A blank makes the next person guess. |

**Sections that may not apply to you:** Section 18 (many apps or repos), Section 19 (compliance rules), and Section 20 (hosts other than GitHub). Each starts with a **🚦 "Does this section apply to you?"** question. If the answer is NO, write `N/A - because ...` and skip ahead.

## Symbols used in this file

| Symbol | Meaning |
|--------|---------|
| ✍️ | You must type an answer here. |
| 🔒 | Default value. Keep it or change it (and say why). |
| ☐ / ☑ | Checkbox. Change `☐` to `☑` to tick it. |
| ✅ / ❌ | Good example / bad example. |
| 🤖 | Rule that applies to AI agents. |
| 🚦 | Stop and check before continuing. |

## Time needed
- **First-time fill-in:** about 45-60 minutes.
- **Copying to a new project:** about 15 minutes (only Sections 1, 5, 9, and 16 change a lot).

## Using this template across many projects
1. Copy this file into the new repo as `docs/Git_Commit_Conventions.md`.
2. Fill **Section 1** (Project Identity) first.
3. Walk through the rest. Everything marked `🔒 DEFAULT` can stay as is.
4. Get one human to sign **Section 22**. Now it is the official rule for that project.
5. Keep the **master copy** of this template untouched. Fill in copies only.

## If you get stuck
- Jump to **Appendix A: Glossary** for plain-English meanings.
- Jump to **Appendix B: One-Page Cheat Sheet** for the short version.
- Still stuck? Write `❓ QUESTION: ...` on that line and ask your reviewer. **Do not guess.**

---

# Section 1. Project Identity

*Why this matters: so anyone who opens this file knows exactly which product it belongs to.*

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 1.1 What is the product called? | |
| 1.2 In one sentence, what does it do? | |
| 1.3 Repository URL (where the code lives) | |
| 1.4 Who owns this document? (name + contact) | |
| 1.5 Who can approve changes to these rules? | |
| 1.6 Date this document was filled in (YYYY-MM-DD) | |
| 1.7 Document version | `1.0.0` |
| 1.8 Main programming language(s) | |
| 1.9 Package/release type (for the release tool in Section 14: `node`, `python`, `java`, `go`, `simple`, other) | |
| 1.10 Where is the code hosted? (GitHub / GitLab / Bitbucket / other) | 🔒 GitHub |

**Who works on this project?**

| Role | Name(s) | ✍️ Count |
|------|---------|----------|
| Humans who write code | | |
| Humans who review code | | |
| 🤖 AI agents that write code (name each, e.g. Claude Code, Copilot) | | |
| Non-technical contributors (docs, content, design) | | |

---

# Section 2. The Big Picture (read, no typing needed)

## What is a commit?
A commit is **one saved step of work with a label**. Example: "Added the login button."

## Why do we need rules for labels?
- ✅ Anyone can read the history like a story.
- ✅ Tools can **automatically** pick the next version number and write release notes.
- ✅ When something breaks, you can find the cause quickly and undo it safely.
- ✅ AI agents and humans write in the **same style**.

## The journey this document covers

```
Idea -> Plan -> Design -> Build -> Test -> Pre-launch -> Launch -> Growth -> 500 customers
  Every step above is saved with commits that follow the SAME format.
```

## The one-line rule
> **`type(scope): short summary`**, for example `feat(build): add login button`

---

# Section 3. The Golden Format

Every commit message has up to three parts: a **header** (required), a **body** (optional), and **footers** (optional).

```
<type>(<scope>): <subject>          <- HEADER (required, one line)
                                    <- blank line
<body>                              <- BODY (optional: explain WHY)
                                    <- blank line
<footer>                            <- FOOTERS (optional: ticket numbers, breaking changes, AI info)
```

## 3.1 Real example

```
feat(build): add email login for new customers

Customers could only sign up with a phone number, which blocked
people without one. Email login removes that blocker.

Refs: #42
Customer-Impact: medium
Milestone: M2-first-10
```

## 3.2 Header rules (🔒 defaults)

| Rule | 🔒 Default | ✍️ Change? (write new value or "keep") |
|------|-----------|----------------------------------------|
| Maximum header length | 72 characters | |
| Type is written in | lowercase | |
| Scope is written in | lowercase | |
| Subject style | imperative mood ("add", not "added" or "adds") | |
| Subject starts with | lowercase letter | |
| Subject ends with | no period | |
| Language | English | |

**Easy trick:** the subject must finish this sentence: *"If applied, this commit will ______."*
- ✅ "If applied, this commit will **add email login**."
- ❌ "If applied, this commit will **added email login**." (wrong tense)

## 3.3 Body rules
- Leave **one blank line** between the header and body.
- Wrap lines at about **72 characters**.
- Explain **WHY** the change was needed and what changed. The code already shows *how*.
- Use the body when the reason is not obvious. For tiny changes, header-only is fine.

## 3.4 Footer rules
Footers are `Key: value` lines at the very bottom. Allowed footers are listed in Sections 7.3 (`Risk`, `Rollback`), 8.2 (customer tags), 9.2 (AI tags), 18.2 (`Package`), and 19.5 (compliance tags).

---

# Section 4. Types: What KIND of change is it?

Pick **exactly one** type. If you cannot decide, the commit is probably too big. Split it.

| Type | Use it when you... | Version bump (automatic) | Shows in changelog? |
|------|--------------------|--------------------------|---------------------|
| `feat` | add something new customers can use | **MINOR** (1.2.0 -> 1.3.0) | Yes |
| `fix` | repair a bug | **PATCH** (1.2.0 -> 1.2.1) | Yes |
| `perf` | make it faster or lighter | PATCH | Yes |
| `security` | close a security hole | PATCH (or higher if breaking) | Yes |
| `revert` | undo an earlier commit | PATCH | Yes |
| `docs` | change only documents or comments | none | No |
| `style` | change only formatting (spaces, commas), no logic | none | No |
| `refactor` | tidy code without changing what it does | none | No |
| `test` | add or fix tests | none | No |
| `build` | change build tools or dependencies | none | No |
| `ci` | change automated pipelines (GitHub Actions, etc.) | none | No |
| `chore` | do routine housekeeping that fits nowhere else | none | No |

> **Breaking change** (anything that forces users to change how they use the product) triggers a **MAJOR** bump (1.x -> 2.0.0). See Section 7.

> **Note on `security`:** it is not part of the original Conventional Commits list, but this template adds it so security fixes are easy to find. It must also be added to your commitlint type list (Section 13).

## 4.1 Quick decision helper (answer top to bottom, stop at the first "yes")

1. Does it add something a customer will notice? -> `feat`
2. Does it fix something broken? -> `fix`
3. Does it close a security problem? -> `security`
4. Is it faster/lighter with no new feature? -> `perf`
5. Does it only change words in docs? -> `docs`
6. Does it only change tests? -> `test`
7. Does it only change pipelines? -> `ci`
8. Does it change build tools or libraries? -> `build`
9. Does it only rearrange code with the same behavior? -> `refactor`
10. Is it only spacing/format? -> `style`
11. Does it undo something? -> `revert`
12. None of the above? -> `chore`

## 4.2 Customize types (optional)

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 4.2.1 Do you want to **add** any extra types? (list, with meaning) | 🔒 No extra types (except `security`) |
| 4.2.2 Do you want to **remove** any types? (list) | 🔒 None |

---

# Section 5. Scopes: WHICH PART of the journey is it?

The scope is the word in brackets. In this template, **scopes follow the product life cycle** so the history reads like the story of the product.

## 5.1 Lifecycle scopes (🔒 default list)

| Scope | Stage | Typical work | Example |
|-------|-------|--------------|---------|
| `plan` | Idea and planning | requirements, user stories, roadmap | `docs(plan): add MVP requirements` |
| `design` | Design | wireframes, UI, architecture decisions | `docs(design): add checkout wireframe` |
| `build` | Building the product | features, core code | `feat(build): add product search` |
| `test` | Testing and QA | tests, QA scripts, bug bashes | `test(test): add checkout tests` |
| `infra` | Infrastructure | servers, databases, cloud setup | `build(infra): add staging database` |
| `deploy` | Shipping to environments | deploy scripts, pipelines | `ci(deploy): add production pipeline` |
| `launch` | Launch preparation | landing page, pricing, onboarding | `feat(launch): add pricing page` |
| `growth` | After launch, toward 500 customers | analytics, referral, feedback fixes | `feat(growth): add referral link` |
| `support` | Customer support | help docs, support tools | `docs(support): add refund FAQ` |
| `ops` | Running it day to day | monitoring, alerts, backups | `feat(ops): add uptime alert` |
| `deps` | Dependencies | library updates | `build(deps): bump express to 5.1` |
| `repo` | The repo itself | README, templates, config | `chore(repo): add PR template` |

## 5.2 Your own module scopes (optional)
Some teams also want to say *which feature area* changed. Add them here, one per line.

| Module scope | What it covers | ✍️ YOUR ANSWER |
|--------------|----------------|----------------|
| (example) `auth` | login, signup, passwords | |
| | | |
| | | |
| | | |

## 5.3 Scope rules
- Use **one** scope per commit. If a change touches two stages, split it into two commits.
- Scope is **optional** only for repo-wide changes. If you leave it out, write `type: subject`.
- Every scope used in commits **must be listed in 5.1 or 5.2**. The tool in Section 13 will block unknown scopes.

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 5.3.1 Is the scope **required** on every commit? | 🔒 Yes |
| 5.3.2 Can people use scopes not in the list? | 🔒 No (add to the list first) |

---

# Section 6. Writing a Good Message

## 6.1 The seven golden rules

1. **Separate subject from body** with a blank line.
2. **Keep the subject short**: 72 characters or fewer (aim for 50).
3. **Start the subject lowercase** (after the colon).
4. **Do not end the subject with a period.**
5. **Use the imperative mood**: "fix", "add", "remove".
6. **Wrap the body** at about 72 characters.
7. **Explain WHAT and WHY**, not just how.

## 6.2 Good vs bad

| ❌ Bad | Why it is bad | ✅ Good |
|--------|---------------|---------|
| `fixed stuff` | no type, no meaning | `fix(build): stop crash when cart is empty` |
| `feat: Added the new login.` | wrong tense, capital, period | `feat(build): add email login` |
| `update` | says nothing | `docs(plan): update MVP scope with payments` |
| `feat(build): add login, fix cart, update docs, bump libs` | four changes in one | Make four commits |
| `WIP` | unfinished work in history | Finish it or use a draft branch (squashed later) |
| `fix: bug` | which bug? | `fix(build): correct tax rounding on invoices` |

## 6.3 One commit = one idea
- 🚦 **Test:** can you describe the commit without using the word "and"? If not, split it.
- Small commits are easier to review, find bugs in, and undo.

## 6.4 Your project's own rules

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 6.4.1 Is a body required for `feat` and `fix` commits? | 🔒 Required for `feat`, optional otherwise |
| 6.4.2 Is a ticket reference (`Refs:`) required? | 🔒 Required for `feat` and `fix` |
| 6.4.3 Which ticket system do you use? (GitHub Issues / Jira / Linear / other / none) | |
| 6.4.4 Ticket ID format (example: `#123` or `PROJ-123`) | |

---

# Section 7. Breaking Changes, Risky Changes, and Undoing Mistakes

## 7.1 What is a breaking change?
A change that makes **existing users, data, or integrations stop working** unless they change something. Examples: removing a feature, renaming an API field, changing a database column, changing how login works.

## 7.2 How to mark one (use **both** for clarity)
1. Add `!` after the scope: `feat(build)!: rename customer id field`
2. Add a footer that explains it:

```
feat(build)!: rename customer id field

BREAKING CHANGE: the `cid` field is now `customer_id`. Update all API
clients before upgrading. Migration guide: docs/migrations/2.0.md
```

The footer **must** say: (a) what broke, (b) who is affected, (c) what to do.

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 7.1.1 Where do you keep migration guides? | 🔒 `docs/migrations/` |
| 7.1.2 Who must approve a breaking change before merge? | |

## 7.3 Risky but not breaking
Add the footer `Risk: low | medium | high` and a line `Rollback: <how to undo>` for anything touching payments, login, data, or deploys.

## 7.4 Undoing a mistake (pick the right tool)

| Situation | What to do |
|-----------|------------|
| Typo in the **last** commit message, not yet pushed | `git commit --amend` |
| Wrong message several commits back, not yet pushed | `git rebase -i` and choose `reword` |
| Bad commit **already pushed/merged to main** | `git revert <commit-hash>` (creates a new undo commit). **Never rewrite main's history.** |
| A **secret** (password/key) was committed | **Rotate the secret first** (make the old one useless), then follow Section 12.4. |

Revert commit format:

```
revert(build): remove email login

This reverts commit 1a2b3c4. It caused sign-in failures for 12 customers.

Refs: #77
```

---

# Section 8. Customer-Impact Tags (Idea to First 500 Customers)

*Why this matters: when you only have a few hundred customers, **every customer matters**. These optional footers connect your code to real people and milestones.*

## 8.1 The milestone ladder (🔒 default, change numbers if you like)

| Code | Milestone | ✍️ Target date |
|------|-----------|----------------|
| `M0-build` | Building, no customers yet | |
| `M1-first-1` | First customer | |
| `M2-first-10` | 10 customers | |
| `M3-first-50` | 50 customers | |
| `M4-first-100` | 100 customers | |
| `M5-first-250` | 250 customers | |
| `M6-first-500` | **500 customers (goal reached)** | |

## 8.2 Footers you can use

| Footer | Allowed values | When to use |
|--------|----------------|-------------|
| `Milestone:` | a code from 8.1 | Work done to reach that milestone |
| `Customer-Impact:` | `none`, `low`, `medium`, `high` | Any `feat`, `fix`, `perf`, `security` commit |
| `Feedback:` | feedback ID or link | The change responds to customer feedback |
| `Refs:` | issue/ticket ID | Always for `feat` and `fix` |
| `Closes:` | issue/ticket ID | The commit fully finishes that ticket |

**Impact scale (so nobody guesses):**
- `none`: customers will never notice.
- `low`: a few customers might notice a small improvement.
- `medium`: many customers will notice, no action needed from them.
- `high`: all customers notice, or some must take action.

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 8.2.1 Where is customer feedback stored? (tool/link) | |
| 8.2.2 Is `Customer-Impact:` required on `feat`/`fix`? | 🔒 Yes |
| 8.2.3 Who counts a "customer"? (paid users, free users, both) | |

---

# Section 9. 🤖 AI-Agent Rules

*This section is for AI coding agents (Claude Code, Copilot, Cursor, and similar) **and** the humans who supervise them.*

## 9.1 The core promise
> **AI writes and commits. A human always reviews before anything reaches `main`.**

## 9.2 Required AI footers

Every commit authored or substantially written by an AI agent **must** end with:

```
AI-Assisted: yes
AI-Agent: <tool name and model, e.g. Claude Code / claude-sonnet-5-5>
Co-Authored-By: <AI name> <noreply email of the tool>
Reviewed-By: <Human Full Name>
```

> `Reviewed-By` is added when the human has actually read the change. An AI must **not** invent this line.

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 9.2.1 Name of each AI tool used and its co-author line | |
| 9.2.2 Who is the default human reviewer for AI commits? | |
| 9.2.3 Is `Reviewed-By` enforced by CI? | 🔒 Yes, on the PR |

## 9.3 Guardrails: AI agents must NEVER

- ❌ Commit directly to `main` (always use a branch and a pull request).
- ❌ Force-push (`git push --force`) or rewrite shared history.
- ❌ Skip checks (`--no-verify`) or disable hooks.
- ❌ Commit secrets, keys, tokens, passwords, or customer personal data.
- ❌ Make one giant commit. Keep each commit to **one idea**.
- ❌ Mark a commit `Reviewed-By` on behalf of a human.
- ❌ Delete or rewrite other people's commits.
- ❌ Invent ticket numbers, customer names, or milestone codes. If unknown, **leave the footer out and ask**.
- ❌ Change this document without a human approving it.

## 9.4 AI agents must ALWAYS

- ✅ Run the tests and the commit-message check before committing.
- ✅ Write messages that follow Sections 3-8 exactly.
- ✅ Stage only the files related to the one idea being committed.
- ✅ Say plainly in the PR description what was done and what was **not** verified.
- ✅ Stop and ask a human when the type, scope, or impact is unclear.

## 9.5 Copy-paste instruction block for your AI agent

Paste this into your agent's instruction file (for example `CLAUDE.md`, `AGENTS.md`, or equivalent):

```
Follow docs/Git_Commit_Conventions.md for every commit.
Format: type(scope): subject  (imperative, lowercase, no period, max 72 chars).
Allowed types and scopes are in Sections 4 and 5. Do not invent new ones.
One idea per commit. Never commit to main. Never use --no-verify or --force.
Never commit secrets or personal data. Add the AI footers from Section 9.2.
If anything is unclear, stop and ask a human instead of guessing.
```

---

# Section 10. Branches, Pull Requests, and Merging

## 10.1 Strategy (🔒 default: trunk-based development with squash merge)

- There is **one main branch**: `main`. It must always work.
- Work happens on **short-lived branches** (aim to merge within 1-3 days).
- Every branch is merged by a **pull request (PR)**.
- PRs are **squash-merged**: all branch commits become **one clean commit** on `main`.
- **The PR title becomes the final commit message**, so the PR title must follow the Golden Format (Section 3).

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 10.1.1 Name of the main branch | 🔒 `main` |
| 10.1.2 Merge method | 🔒 Squash and merge |
| 10.1.3 Is direct push to `main` blocked? | 🔒 Yes |
| 10.1.4 Required number of approvals before merge | 🔒 1 (use `0 + self-review checklist` only for a solo founder) |

> **Setup tip (GitHub):** Settings -> General -> Pull Requests -> "Allow squash merging" -> set the default commit message to **"Pull request title"** (or title plus description). Turn off merge commits and rebase merging if you want squash only.

## 10.2 Branch names

Format: `<type>/<short-description>`, lowercase, words joined with hyphens.

| ✅ Good | ❌ Bad |
|---------|--------|
| `feat/email-login` | `my-branch` |
| `fix/empty-cart-crash` | `Fix_Stuff` |
| `docs/mvp-requirements` | `john-test-2` |

## 10.3 Pull request checklist (paste into your PR template)

```
## What changed?
(1-3 plain sentences)

## Why?
(The reason or the customer problem)

## Checklist
- [ ] PR title follows type(scope): subject
- [ ] Only ONE idea in this PR
- [ ] Tests added or updated, and they pass
- [ ] No secrets or personal data included
- [ ] Docs updated if behavior changed
- [ ] Breaking change? If yes, marked with ! and BREAKING CHANGE footer
- [ ] Customer-Impact and Refs footers added (if feat/fix)
- [ ] AI-assisted? If yes, AI footers added and a human has reviewed
```

---

# Section 11. Code Review Rules for Commits

## 11.1 What a reviewer checks (every PR)

| # | Check | Pass? |
|---|-------|-------|
| 1 | Is the **type** correct? (`feat` vs `fix` vs `chore`) | ☐ |
| 2 | Is the **scope** in the allowed list? | ☐ |
| 3 | Is the subject clear **without opening the code**? | ☐ |
| 4 | Does the body explain **why**? | ☐ |
| 5 | Is it **one idea** only? | ☐ |
| 6 | Are breaking changes marked properly? | ☐ |
| 7 | Are `Refs`, `Customer-Impact`, and `Milestone` correct (not guessed)? | ☐ |
| 8 | If AI wrote it, are the AI footers present and honest? | ☐ |
| 9 | No secrets, tokens, or personal data in the diff or message? | ☐ |
| 10 | Do tests and automated checks pass? | ☐ |

## 11.2 Review etiquette (🔒 defaults)

- Review within **1 working day**. ✍️ Your target: ______
- Be kind and specific. Say *what* to change and *why*.
- Authors must not merge their own PR unless the project is solo (then use the self-review checklist above).
- A reviewer who is unsure **asks a question**. Guessing is not allowed.

---

# Section 12. Safety: Secrets, Personal Data, and Signed Commits

## 12.1 What must NEVER be in a commit

- Passwords, API keys, access tokens, private keys, `.env` files
- Customer names, emails, phone numbers, payment details
- Database dumps with real customer data
- Anything marked confidential

Put secrets in a **secrets manager or environment variables**. Add secret files to `.gitignore`.

## 12.2 Block secrets before they are saved

| Tool (pick one) | What it does |
|-----------------|--------------|
| gitleaks | scans staged changes for secrets |
| GitHub secret scanning + push protection | blocks pushes that contain known secret formats |
| detect-secrets | scans and tracks a baseline |

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 12.2.1 Which secret scanner do you use? | 🔒 gitleaks (local) + GitHub push protection |
| 12.2.2 Who is told if a secret is found? | |

## 12.3 Signed commits (proof of who made the change)

🔒 Default: **required on `main`**, using SSH signing (the simplest way).

```
git config --global gpg.format ssh
git config --global user.signingkey ~/.ssh/id_ed25519.pub
git config --global commit.gpgsign true
```

Then add the same public key to your Git host as a **signing key**. For AI agents that commit on their own, use a **dedicated bot account with its own signing key**, never a person's key.

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 12.3.1 Are signed commits required? | 🔒 Yes |
| 12.3.2 Bot/agent account name(s) | |

## 12.4 If a secret was committed (do this in order)

1. **Rotate/revoke the secret immediately** (assume it is stolen).
2. Tell the owner in 1.4.
3. Remove it from history with a tool like `git filter-repo` or BFG, **only after** step 1.
4. Force-push is allowed **only** for this emergency and only by a human maintainer.
5. Write an incident note: what leaked, when, who was told, what was rotated.

---

# Section 13. Tooling: Make the Rules Automatic

*Humans forget. Tools do not. Pick all the boxes you want.*

| Tool | Purpose | ☐ Use it? |
|------|---------|-----------|
| commitlint + Husky | blocks bad messages on your computer | ☑ 🔒 |
| `.gitmessage` template | shows a fill-in guide when you commit | ☑ 🔒 |
| CI check on PR title | blocks bad PR titles on GitHub | ☑ 🔒 |
| release-please (or semantic-release) | automates version, tag, changelog | ☑ 🔒 |
| gitleaks | blocks secrets | ☑ 🔒 |

## 13.1 commitlint + Husky (Node-based setup)

```bash
npm install --save-dev @commitlint/cli @commitlint/config-conventional husky
npx husky init
echo 'npx --no -- commitlint --edit $1' > .husky/commit-msg
```

Create `commitlint.config.js`:

```js
module.exports = {
  extends: ['@commitlint/config-conventional'],
  rules: {
    'type-enum': [2, 'always', [
      'feat', 'fix', 'perf', 'security', 'revert',
      'docs', 'style', 'refactor', 'test', 'build', 'ci', 'chore'
    ]],
    'scope-enum': [2, 'always', [
      'plan', 'design', 'build', 'test', 'infra', 'deploy',
      'launch', 'growth', 'support', 'ops', 'deps', 'repo'
      // add your module scopes from Section 5.2 here
    ]],
    'scope-empty': [2, 'never'],          // scope required (Section 5.3.1)
    'header-max-length': [2, 'always', 72],
    'subject-case': [2, 'never', ['sentence-case', 'start-case', 'pascal-case', 'upper-case']],
    'subject-full-stop': [2, 'never', '.'],
  },
};
```

> Not using Node? Use a language-neutral option such as the `pre-commit` framework with a conventional-commit hook, or only the CI check in 13.3.

## 13.2 Commit message template (guides beginners)

Create a file named `.gitmessage`:

```
# <type>(<scope>): <subject>   (max 72 chars, imperative, lowercase, no period)
#
# Why was this change needed? What changed?
#
# Refs: #
# Customer-Impact: none | low | medium | high
# Milestone: M0-build ... M6-first-500
#
# Types: feat fix perf security revert docs style refactor test build ci chore
# Scopes: plan design build test infra deploy launch growth support ops deps repo
```

Turn it on: `git config commit.template .gitmessage`

## 13.3 GitHub check for pull request titles

Create `.github/workflows/pr-title.yml`:

```yaml
name: PR title check
on:
  pull_request_target:
    types: [opened, edited, synchronize, reopened]
permissions:
  pull-requests: read
jobs:
  lint-title:
    runs-on: ubuntu-latest
    steps:
      - uses: amannn/action-semantic-pull-request@v5
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

> This action only reads the PR title and does not check out your code. Do not add steps that run code from the pull request under `pull_request_target`.

## 13.4 Automatic versions and changelog (release-please)

Create `.github/workflows/release-please.yml`:

```yaml
name: release-please
on:
  push:
    branches: [main]
permissions:
  contents: write
  pull-requests: write
jobs:
  release-please:
    runs-on: ubuntu-latest
    steps:
      - uses: googleapis/release-please-action@v4
        with:
          release-type: node   # change to match your answer in 1.9
```

How it works: after PRs are merged, the tool opens a **"Release PR"** that bumps the version and updates `CHANGELOG.md`. When a human merges that PR, it creates the **tag and GitHub Release**.

## 13.5 Secret scanning hook (gitleaks)

Add to `.husky/pre-commit`:

```bash
gitleaks git --pre-commit --staged
```

> Tool flags change between versions. Check the tool's current documentation if a command fails.

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 13.5.1 Who installs and maintains the tooling? | |
| 13.5.2 If you do not use Node, what replaces commitlint? | |

---

# Section 14. Versions, Changelog, and Releases

## 14.1 How versions work (Semantic Versioning: MAJOR.MINOR.PATCH)

```
   2   .   4   .   1
   |       |       |
 MAJOR   MINOR   PATCH
 (breaking) (new feature) (bug fix)
```

| Commit contains | Version changes |
|-----------------|-----------------|
| `feat` | 1.4.0 -> **1.5.0** |
| `fix`, `perf`, `security`, `revert` | 1.4.0 -> **1.4.1** |
| `!` or `BREAKING CHANGE:` | 1.4.0 -> **2.0.0** |
| docs, test, ci, chore, refactor, style, build | no new version |

**Before launch (0.x.y):** breaking changes may bump MINOR instead of MAJOR. 🔒 Default: **first public launch is `1.0.0`**.

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 14.1.1 Starting version | 🔒 `0.1.0` |
| 14.1.2 Which release brings the first paying/real customers? | 🔒 `1.0.0` |
| 14.1.3 Tag format | 🔒 `v1.2.3` |

## 14.2 Release checklist (copy for each release)

```
- [ ] All checks on main are green
- [ ] Release PR reviewed (version and changelog make sense)
- [ ] Breaking changes have migration guides
- [ ] Rollback plan written (how to go back to the last good version)
- [ ] Customers who need to know have been told
- [ ] Release PR merged by a human
- [ ] Tag and GitHub Release created
- [ ] Deployment verified in production (smoke test)
- [ ] Monitoring watched for the first 24 hours
```

## 14.3 Hotfix (urgent bug in production)

1. Branch from `main`: `fix/short-description`.
2. Make the smallest possible fix, with a test.
3. PR with title `fix(<scope>): <subject>` and a `Rollback:` line.
4. Fast review (target: ______ minutes ✍️).
5. Merge -> the release tool creates a PATCH release.

## 14.4 Rollback rule
If a release harms customers, **revert first, investigate second**. Use `git revert` and ship a PATCH release. Write down what happened.

---

# Section 15. Life Cycle Map: Which Commits Appear When?

Use this to see what "normal" looks like at each stage. ✍️ Fill in the last column with your real plan.

| Stage | Typical commits | Typical release | ✍️ Your start date | ✍️ Done when... |
|-------|-----------------|-----------------|---------------------|------------------|
| 1. Idea and plan | `docs(plan): ...` | none | | |
| 2. Design | `docs(design): ...`, `feat(design): ...` | none | | |
| 3. Build the MVP | `feat(build): ...`, `test(test): ...`, `build(infra): ...` | `0.x.0` | | |
| 4. Test and QA | `fix(build): ...`, `test(test): ...` | `0.x.y` | | |
| 5. Pre-launch | `feat(launch): ...`, `docs(support): ...`, `ci(deploy): ...` | `1.0.0-rc` or `0.9.0` | | |
| 6. Launch | `feat(launch): ...`, `fix(...)` hotfixes | **`1.0.0`** | | |
| 7. Growth (1 -> 500 customers) | `feat(growth): ...`, `fix(...)`, `perf(...)`, `feat(ops): ...` | `1.x.0` weekly or biweekly | | |
| 8. 500 customers reached | Review: what worked? Update this document. | | | |

## 15.1 Example story (what a healthy history looks like)

```
docs(plan): add MVP requirements and user stories
docs(design): add onboarding wireframes
build(infra): add staging database
feat(build): add email login
test(test): add login tests
fix(build): stop crash when cart is empty
feat(launch): add pricing page
ci(deploy): add production pipeline
feat(growth): add referral link          <- Milestone: M3-first-50
fix(build): correct tax rounding         <- Customer-Impact: high
```

---

# Section 16. Examples Gallery

## 16.1 ✅ Good examples

```
feat(build): add email login for new customers
```

```
fix(build): stop crash when the cart is empty

The checkout page read the first item without checking the list.
It now shows "Your cart is empty" instead of failing.

Refs: #58
Customer-Impact: high
Milestone: M2-first-10
```

```
feat(build)!: rename customer id field

BREAKING CHANGE: `cid` is now `customer_id` in all API responses.
Affects: mobile app < 2.0 and partner integrations.
Action: update clients before upgrading. See docs/migrations/2.0.md.

Refs: #91
Customer-Impact: high
```

```
docs(plan): add refund policy to MVP scope
```

```
feat(growth): add referral link to account page

Refs: #120
Customer-Impact: medium
Milestone: M3-first-50
Feedback: FB-34
AI-Assisted: yes
AI-Agent: Claude Code
Co-Authored-By: Claude <noreply@anthropic.com>
Reviewed-By: Jordan Lee
```

## 16.2 ❌ Bad examples and fixes

| ❌ Bad | ✅ Fixed |
|--------|----------|
| `Updated files` | `docs(repo): update contributing guide` |
| `fix: fixed the bug.` | `fix(build): handle empty search query` |
| `feat(Build): Add Login` | `feat(build): add login` |
| `feat(payments): add card` (scope not in list) | add `payments` to Section 5.2 first, or use `feat(build): add card payments` |
| `feat(build): add login and fix cart and update docs` | three separate commits |
| `chore: api key = sk-live-...` | **Never commit secrets.** Rotate the key (Section 12.4). |

## 16.3 Your project's examples (fill 3 real ones)

| # | ✍️ A real commit message from this project |
|---|---------------------------------------------|
| 1 | |
| 2 | |
| 3 | |

---

# Section 17. FAQ and Troubleshooting

| Problem | Answer |
|---------|--------|
| "My commit was rejected." | Read the error. It names the broken rule. Fix the message and run `git commit` again. |
| "I do not know which type to use." | Use the helper in 4.1. Still unsure? Ask. Do not guess. |
| "My change fits two scopes." | Split into two commits. |
| "I have many tiny messy commits on my branch." | Fine. Squash merge will combine them, but your **PR title** must be perfect. |
| "Can I use emoji in messages?" | 🔒 Default: no. Keep messages plain text. |
| "Can I write in another language?" | 🔒 Default: English only, for tool and team compatibility. |
| "Do I need a body for every commit?" | No. Only where Section 6.4 says so. |
| "AI wrote my commit message wrong." | Fix it before merging. A human owns every merge. |
| "Hooks are slow or broken." | Tell the owner (1.4). **Never** bypass hooks with `--no-verify`. |
| "Can I change these rules?" | Yes, through a PR that edits this file, approved by the person in 1.5. Add a line in Section 22.2. |

---

# Section 18. Monorepo and Multi-Repo Rules

*Why this matters: when one product is split into many apps or many repos, labels can get confusing. These rules keep the history readable and the releases independent.*

## 18.0 🚦 Does this section apply to you?

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 18.0.1 Does this project have more than one app, package, or service? (YES / NO) | |
| 18.0.2 If NO, write `N/A - single app` here and **skip to Section 19**. | |

## 18.1 Pick your layout

| Layout | What it means | ☑ Pick one |
|--------|---------------|------------|
| Single repo, single app | One product, one repo. | ☐ |
| **Monorepo** | Many apps/packages live in **one** repo. | ☐ |
| **Multi-repo** | Many repos, each with its own history. | ☐ |

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 18.1.1 Which layout does this project use? | |

## 18.2 Monorepo rules (use only if you picked Monorepo)

**Step 1: choose how a commit says WHICH package it touched.**

| Option | How it looks | Good for |
|--------|--------------|----------|
| **A (🔒 default)**: lifecycle scope + `Package:` footer | `feat(build): add product search` + footer `Package: apps/web` | Keeping the story-of-the-product style from Section 5 |
| **B**: package name is the scope | `feat(web): add product search` | Big monorepos where the package matters more than the stage |

If you pick **B**, add every package name to the scope list in Section 5.2 and to `scope-enum` in Section 13.1.

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 18.2.1 Option A or B? | 🔒 A |

Example (Option A):

```
feat(build): add product search

Package: apps/web
Refs: #140
Customer-Impact: medium
```

**Step 2: follow these rules (🔒 defaults).**

- One commit touches **one package** whenever possible.
- A change that would **break if split** (for example, an API change plus the app that calls it) may touch several packages. List all of them: `Package: apps/web, apps/api`. Explain why in the body.
- If you change a **shared library**, name every app that depends on it in the body when the change is breaking.
- Each package is **versioned and released on its own** (see the tooling below).
- Reviewers come from the package owners (use a `CODEOWNERS` file).

**Step 3: list your packages (fill this table).**

| ✍️ Folder path | ✍️ Package name | ✍️ Owner | ✍️ Release type (`node`, `python`, `go`, `simple`...) |
|----------------|-----------------|----------|--------------------------------------------------------|
| (example) `apps/web` | `web` | Jordan | `node` |
| | | | |
| | | | |

**Tooling: independent releases with release-please.**
Create `release-please-config.json`:

```json
{
  "packages": {
    "apps/web": { "release-type": "node" },
    "apps/api": { "release-type": "python" }
  }
}
```

Create `.release-please-manifest.json` (the current version of each package):

```json
{
  "apps/web": "0.1.0",
  "apps/api": "0.1.0"
}
```

The workflow from Section 13.4 keeps working. Release-please reads the files each commit changed to decide which package gets a new version. Tags are usually named like `web-v1.2.3` (package name plus version).

**Tooling: review owners.** Create `.github/CODEOWNERS`:

```
/apps/web/   @your-github-name
/apps/api/   @another-github-name
/docs/       @your-github-name
```

## 18.3 Multi-repo rules (use only if you picked Multi-repo)

- **Same labels everywhere.** Every repo uses the same types, scopes, and footers. Copy this template into each repo. Keep the master in one "standards" repo.
- **Share one commitlint config.** Publish it once as a package (for example `@your-org/commitlint-config`) and have every repo `extends` it. This stops the rules from drifting apart.
- **Link across repos.** Use the full name: `Refs: your-org/other-repo#12`.
- **Breaking change that hits another repo?** Open an issue in **each** affected repo **before** you merge, and link them all in the footer.
- **Track which versions work together** (fill this table):

| ✍️ Repo A version | ✍️ Repo B version | ✍️ Works together? | ✍️ Notes |
|-------------------|-------------------|--------------------|----------|
| (example) `web 1.4.x` | `api 2.1.x` | Yes | |
| | | | |

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 18.3.1 Where does the master standards repo live? | |
| 18.3.2 Who updates all repos when the master template changes? | |

---

# Section 19. Compliance and Audit Trail (SOC 2, GDPR, and Similar)

> **Important:** this section is **engineering guidance**, not legal advice. Ask your compliance lead, auditor, or lawyer which rules truly apply to you.

*Why this matters: auditors and enterprise customers will ask, "Who changed what, who approved it, and when?" Good commits make that answer easy.*

## 19.0 🚦 Does this section apply to you?

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 19.0.1 Which rules must you follow? Tick all that apply: ☐ SOC 2 ☐ GDPR ☐ ISO 27001 ☐ HIPAA ☐ PCI DSS ☐ Other: ____ ☐ None yet | |
| 19.0.2 Do you expect to need one of them within 12 months (for example, because a customer asks)? | |
| 19.0.3 If you ticked "None yet" and answered "No" above, write `N/A - because ...` and skip to Section 20. (Still read 19.3: it is good practice for everyone.) | |

## 19.1 The chain of evidence (idea -> customer)

Every change should be traceable end to end:

```
Ticket -> Branch -> Commit -> Pull request -> Review/approval -> Automated checks -> Release -> Deployment
```

| Link | Where the proof lives | This template covers it in |
|------|-----------------------|----------------------------|
| Why was it requested? | Ticket (`Refs:` footer) | Sections 6.4, 8 |
| Who wrote it? | Commit author + signature | Sections 9, 12.3 |
| Who reviewed and approved it? | PR approval record | Sections 10, 11 |
| Was it tested? | CI results attached to the PR | Section 13 |
| What was released and when? | Tag, release notes, changelog | Section 14 |
| Who can bypass the rules? | Branch protection settings | Section 10.1 |

## 19.2 What auditors usually want to see (and where to find it)

| Typical expectation | How this template helps | ✍️ Where is the evidence stored? |
|---------------------|-------------------------|----------------------------------|
| Changes are **authorized** before release | PR + required approval | |
| Changes are **tested** | CI checks must pass before merge | |
| Changes are **documented** | Conventional commit + changelog | |
| **Separation of duties** (author is not the only approver) | Section 10.1.4: at least 1 approval | |
| **Emergency changes** are controlled | Section 19.4 | |
| Access to `main` is **restricted** | Protected branch | |
| Secrets are **kept out of code** | Section 12 | |

## 19.3 Privacy rules for commits (GDPR-friendly habits)

Git history is **very hard to erase**, so keep personal data out of it from the start.

- ❌ Never put customer names, emails, phone numbers, or IDs that point to a real person in a commit message, branch name, or code.
- ✅ Use **neutral references**: ticket numbers (`Refs: #58`), not "fixed bug for John Smith".
- ✅ Use test data that is **fake**, never a copy of production data.
- ⚠️ **Commit authors' names and emails are personal data too.** Decide how your team handles this:

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 19.3.1 Will staff commit with a private "no-reply" email address provided by the Git host? | 🔒 Yes |
| 19.3.2 Who handles a request to remove personal data that landed in history? | |
| 19.3.3 If personal data does leak into history, follow the same steps as Section 12.4 and also tell: ✍️ (name/role) | |

## 19.4 Emergency changes (production is broken and you cannot wait)

1. A human maintainer **approves in writing** (chat or ticket) before the change is merged.
2. The PR still exists (no skipping the PR).
3. Add the footer `Emergency: yes` and `Approved-By: <Full Name>`.
4. Within **2 working days**, a second person reviews the change **after the fact** and records it. ✍️ Your deadline: ______
5. Add a short note in the incident log: what happened, why it could not wait.

## 19.5 Extra footers for compliance (use only if Section 19.0 applies)

| Footer | Allowed values | When to use |
|--------|----------------|-------------|
| `Data-Impact:` | `none`, `personal-data`, `schema-change` | Any change touching stored customer data |
| `Emergency:` | `yes` | Only for Section 19.4 changes |
| `Approved-By:` | A human's full name | Emergency changes and any rule exceptions |
| `Security-Review:` | `not-needed`, `done`, `pending` | Changes to login, payments, permissions, or encryption |

Example:

```
fix(build): block access to other customers' invoices

Refs: #301
Customer-Impact: high
Data-Impact: personal-data
Security-Review: done
Emergency: yes
Approved-By: Priya Shah
```

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 19.5.1 Who owns compliance for this project? (name + contact) | |
| 19.5.2 How long are PR records, CI logs, and release notes kept? | |
| 19.5.3 Who is your auditor or compliance advisor (if any)? | |
| 19.5.4 Are the extra footers in 19.5 required? | 🔒 Only if you ticked SOC 2, ISO 27001, HIPAA, or PCI DSS in 19.0.1 |

---

# Section 20. Git Hosting Variants (GitHub, GitLab, Bitbucket)

*Why this matters: Sections 10 and 13 show GitHub steps. If you use another host, find your column below. **Menu names change often, so always check your host's current documentation.***

## 20.0 🚦 Does this section apply to you?

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 20.0.1 Which host do you use? (same as answer 1.10) | |
| 20.0.2 If GitHub, write `N/A - GitHub` and **skip to Section 21**. | |

## 20.1 Same goal, different button names

| What you need | GitHub (default) | GitLab | Bitbucket Cloud |
|---------------|------------------|--------|-----------------|
| Review request is called | Pull request (PR) | Merge request (MR) | Pull request (PR) |
| Squash merge | Settings -> Pull Requests -> allow squash merging | Settings -> Merge requests -> Squash commits (set to **Require** or **Encourage**) | Repository settings -> Merge strategies -> enable squash |
| Final commit message comes from the PR/MR title | Set default to "Pull request title" | Squash commit message template: `%{title}` | Check the message at merge time. Bitbucket may prefill from the branch's commits |
| Protect `main` | Branch protection or rulesets | Settings -> Repository -> Protected branches | Repository settings -> Branch restrictions |
| Check the PR/MR title automatically | GitHub Action (Section 13.3) | CI job (see 20.2) | Pipelines step that checks commits (see 20.3) |
| Automated version, tag, changelog | release-please (Section 13.4) | semantic-release with its GitLab plugin | semantic-release in a Pipelines step (check plugin support for your plan) |
| Secret scanning | Secret scanning + push protection | GitLab Secret Detection (check which features your plan includes) | gitleaks in Pipelines (Section 13.5) |
| Require signed commits | Branch protection rule | Push rule "Reject unsigned commits" (plan-dependent) | Check current docs. If it cannot be enforced, enforce in CI or mark "recommended" and write the reason below |

| Question | ✍️ YOUR ANSWER |
|----------|----------------|
| 20.1.1 Any rule from this template you cannot enforce on your host? (list + reason) | |
| 20.1.2 What replaces it? (CI check, manual reviewer step, other) | |

> **Note:** release-please's ready-made action is built for GitHub. On other hosts use **semantic-release** (it reads the same Conventional Commits) or a manual release step with the same rules from Section 14.

## 20.2 GitLab recipe: check the MR title

Add to `.gitlab-ci.yml`:

```yaml
commitlint-mr-title:
  image: node:22
  stage: test
  rules:
    - if: $CI_PIPELINE_SOURCE == "merge_request_event"
  script:
    - npm ci
    - echo "$CI_MERGE_REQUEST_TITLE" | npx commitlint
```

This uses the same `commitlint.config.js` from Section 13.1. Also set **Squash commit message template** to `%{title}` so the MR title becomes the final commit message.

## 20.3 Bitbucket recipe: check commits in the pull request

Add to `bitbucket-pipelines.yml`:

```yaml
pipelines:
  pull-requests:
    '**':
      - step:
          name: Check commit messages
          image: node:22
          script:
            - git fetch origin main
            - npm ci
            - npx commitlint --from origin/main --to HEAD --verbose
```

> If this step cannot see enough history, increase the clone depth in your pipeline settings. Because Bitbucket may build the squash message from the branch's commits, the **reviewer also checks the final merge message** (Section 11.1).

---

# Section 21. Onboarding Exercise (5 Minutes)

*Why this matters: reading rules is not the same as using them. Everyone (people who write code, people who review, and non-technical contributors) takes this short practice before their first commit. **Do not look at the answer key until you finish.***

## 21.1 Who took it?

| ✍️ Name | ✍️ Role | ✍️ Date | ✍️ Score (out of 31) | ✍️ Passed? (25 or more = Yes) |
|---------|---------|---------|----------------------|--------------------------------|
| | | | | |
| | | | | |

## Part A. Pick the type (1 point each, 10 points)

Choose from: `feat fix perf security revert docs style refactor test build ci chore`

| # | What happened | ✍️ Type |
|---|---------------|---------|
| A1 | You added a "Share" button that customers can click. | |
| A2 | You fixed a page that crashed when a name had an apostrophe. | |
| A3 | You fixed spacing and commas in the code. Nothing works differently. | |
| A4 | You wrote setup steps in the README. | |
| A5 | You upgraded a library to its new version. | |
| A6 | You made the search page load twice as fast. | |
| A7 | You fixed a hole that let people see other customers' invoices. | |
| A8 | You undid yesterday's pricing commit. | |
| A9 | You added tests for the checkout page. | |
| A10 | You changed the pipeline that deploys the product. | |

## Part B. Fix the bad message (1 point each, 5 points)

Rewrite each one so it follows the Golden Format. Any rule-following answer is correct.

| # | ❌ Bad message | ✍️ Your fixed version |
|---|----------------|-----------------------|
| B1 | `Fixed login bug.` | |
| B2 | `feat(Build): Added Referral Link` (it is a post-launch growth feature) | |
| B3 | `update stuff and fix cart and add docs` | |
| B4 | `docs: README` | |
| B5 | `WIP` | |

## Part C. Write the full message (2 points each, 6 points)

Write the **complete** commit message, including body and footers where the rules need them.

| # | Situation | ✍️ Your message |
|---|-----------|-----------------|
| C1 | After launch you added an "Export my data" button. Ticket #210. Many customers will notice. You are working toward the 50-customer milestone. | |
| C2 | You renamed the API field `userName` to `user_name`. Old apps will stop working. Ticket #215. | |
| C3 | An AI agent fixed a typo on the pricing page. A human has **not** read the change yet. Ticket #220. | |

## Part D. True or false (1 point each, 8 points)

| # | Statement | ✍️ T or F |
|---|-----------|-----------|
| D1 | With squash merge, the PR title becomes the commit message on `main`. | |
| D2 | It is fine to use `--no-verify` when you are in a hurry. | |
| D3 | If a password was committed, deleting the file fixes the problem. | |
| D4 | An AI agent may add `Reviewed-By` itself to save time. | |
| D5 | One commit should contain one idea. | |
| D6 | Tiny changes may be pushed straight to `main`. | |
| D7 | A `feat` commit causes a MINOR version bump. | |
| D8 | The subject line should end with a period. | |

## Part E. What would you do? (1 point each, 2 points)

| # | Situation | ✍️ Your answer (one sentence) |
|---|-----------|-------------------------------|
| E1 | You find an API key in a commit from last week. What is your **first** step? | |
| E2 | You are an AI agent and cannot tell which scope fits the change. What do you do? | |

## 21.2 Answer key (scroll down only after you finish)

<details>
<summary>Click to open the answer key</summary>

**Part A:** A1 `feat` - A2 `fix` - A3 `style` - A4 `docs` - A5 `build` - A6 `perf` - A7 `security` - A8 `revert` - A9 `test` - A10 `ci`

**Part B (example answers; yours may differ if it follows the rules):**
- B1 `fix(build): handle empty password on login`
- B2 `feat(growth): add referral link`
- B3 Three separate commits, for example `fix(build): update cart total`, `docs(repo): add usage notes`, and one for "stuff" once you know what it was.
- B4 `docs(repo): add setup steps to README`
- B5 Finish the work first, then give it a real message, for example `feat(build): add order history page`.

**Part C (example answers):**

C1:
```
feat(growth): add export-my-data button

Customers asked for a way to download their own data. The button
creates a file of their orders and profile.

Refs: #210
Customer-Impact: medium
Milestone: M3-first-50
```
(2 points if the type, scope, `Refs`, `Customer-Impact`, and `Milestone` are all correct. 1 point if one is missing.)

C2:
```
feat(build)!: rename userName field to user_name

BREAKING CHANGE: the `userName` field is now `user_name` in all API
responses. Affects all API clients. Update clients before upgrading.

Refs: #215
Customer-Impact: high
```
(2 points if it has both `!` and a `BREAKING CHANGE:` footer that says what broke, who is affected, and what to do. 1 point if one is missing.)

C3:
```
fix(launch): correct typo on pricing page

Refs: #220
Customer-Impact: low
AI-Assisted: yes
AI-Agent: Claude Code
Co-Authored-By: Claude <noreply@anthropic.com>
```
(2 points. It must **not** include `Reviewed-By`, because no human has read it yet. 1 point if the AI footers are missing.)

**Part D:** D1 True - D2 False - D3 False (rotate the secret first, Section 12.4) - D4 False - D5 True - D6 False - D7 True - D8 False

**Part E:**
- E1 Rotate or revoke the key immediately (Section 12.4).
- E2 Stop and ask a human. Do not guess.

**Scoring:** Part A 10 + Part B 5 + Part C 6 + Part D 8 + Part E 2 = **31 points**. The pass mark is **25 (about 80%)**. If someone scores below 25, they re-read Sections 3-9 and try again before their first commit.

</details>

---

# Section 22. Final Check and Sign-Off

## 22.1 🚦 Before you call this document "done"

- [ ] Section 1 is fully filled (no blank answers).
- [ ] Every `✍️` field has an answer or `N/A - because ...`.
- [ ] Every `🔒` I changed has a written reason.
- [ ] Section 5 lists every scope people will use.
- [ ] Section 13 tools are installed and I **tested one bad commit** (it was blocked).
- [ ] Section 9 instruction block is pasted into the AI agent's instruction file.
- [ ] PR template from 10.3 exists in the repo.
- [ ] A second person read this document and could follow it without asking me questions.
- [ ] Secrets scanning is on (Section 12).
- [ ] Section 18 is filled, or says `N/A - because ...`.
- [ ] Section 19 is filled, or says `N/A - because ...`.
- [ ] Section 20 is filled, or says `N/A - GitHub`.
- [ ] Every person who will commit has taken the Section 21 exercise and passed.

## 22.2 Change log for this document

| Date | Version | What changed | Who | Approved by |
|------|---------|--------------|-----|-------------|
| ✍️ | 1.0.0 | First version | | |
| | | | | |

## 22.3 Sign-off

| Role | Name | Date | Signature/Approval |
|------|------|------|--------------------|
| Document owner | | | |
| Reviewer | | | |

## 22.4 Open questions (write every doubt here, do not hide it)

| # | ✍️ Question | Who answers? | Answer | Date |
|---|-------------|--------------|--------|------|
| 1 | | | | |
| 2 | | | | |

---

# Appendix A. Glossary (Plain English)

| Word | Simple meaning |
|------|----------------|
| **Repository (repo)** | The folder where all your project's files and history live. |
| **Commit** | One saved step of work with a label. |
| **Branch** | A separate copy of the work where you can try things safely. |
| **Pull request (PR)** | A request to add your branch's work to the main project, so someone can review it. |
| **Merge** | Combining work from one branch into another. |
| **Squash merge** | Combining all of a branch's commits into **one** commit when merging. |
| **Main** | The official, always-working branch. |
| **Type** | The kind of change (`feat`, `fix`, ...). |
| **Scope** | The part of the product or journey the change belongs to. |
| **Subject** | The short summary line. |
| **Body** | The longer explanation of why. |
| **Footer** | Extra labeled lines at the bottom (`Refs:`, `Milestone:` ...). |
| **Breaking change** | A change that makes existing users or systems stop working unless they update. |
| **Semantic versioning** | Version numbers `MAJOR.MINOR.PATCH` that tell you how big a change is. |
| **Changelog** | A list of what changed in each version. |
| **Tag** | A permanent bookmark on one commit, such as `v1.2.0`. |
| **Revert** | Make a new commit that undoes an old one. |
| **Hook** | A small program Git runs automatically (for example, checking your message). |
| **CI** | Robots that automatically test and check your work on every PR. |
| **Secret** | A password, key, or token that must stay private. |
| **PII** | Personal data about a real person (name, email, phone...). |
| **AI agent** | A program that writes or changes code by itself, under human supervision. |
| **MVP** | Minimum Viable Product: the smallest version that real customers can use. |
| **Milestone** | A goal marker, such as "50 customers". |
| **Rollback** | Going back to the last version that worked. |
| **Monorepo** | One repository that holds many apps or packages. |
| **Multi-repo** | Many separate repositories, each with its own history. |
| **Package** | One separately releasable piece of a bigger product. |
| **CODEOWNERS** | A file that names who must review changes to each folder. |
| **Audit trail** | The proof of who changed what, who approved it, and when. |
| **SOC 2** | A security report that shows customers you handle data and changes carefully. |
| **GDPR** | A European privacy law about how personal data is collected, kept, and erased. |
| **Trailer / footer** | A `Key: value` line at the end of a commit message. |
| **Merge request (MR)** | GitLab's name for a pull request. |

---

# Appendix B. One-Page Cheat Sheet (print this)

```
FORMAT      type(scope): subject
RULES       imperative - lowercase - no period - max 72 chars - one idea

TYPES       feat fix perf security revert docs style refactor test build ci chore
SCOPES      plan design build test infra deploy launch growth support ops deps repo

VERSION     feat = MINOR   fix/perf/security/revert = PATCH   ! = MAJOR

BREAKING    feat(build)!: subject
            BREAKING CHANGE: what broke, who is hit, what to do

FOOTERS     Refs: #123
            Customer-Impact: none|low|medium|high
            Milestone: M0-build ... M6-first-500
            Feedback: FB-12
            (AI) AI-Assisted: yes / AI-Agent: / Co-Authored-By: / Reviewed-By:
            (Monorepo) Package: apps/web
            (Compliance) Data-Impact: none|personal-data|schema-change
                         Security-Review: not-needed|done|pending
                         Emergency: yes + Approved-By: Full Name

NEVER       commit to main - force-push - --no-verify - commit secrets - guess
ALWAYS      branch - PR - squash merge - human review - tests green
```

---

# Appendix C. Standards and References This Template Follows

| Source | Used for |
|--------|----------|
| Conventional Commits 1.0.0 (conventionalcommits.org) | Header, body, footer format; `!` and `BREAKING CHANGE` |
| Semantic Versioning 2.0.0 (semver.org) | MAJOR.MINOR.PATCH rules |
| Angular commit guidelines | Type list and subject conventions |
| Git documentation (`git-commit`, `git-interpret-trailers`) | Footer (trailer) format |
| Chris Beams, "How to Write a Git Commit Message" | The seven rules and imperative mood |
| Keep a Changelog (keepachangelog.com) | Changelog structure |
| commitlint, Husky, release-please, gitleaks docs | Tooling in Section 13 |
| GitHub docs on protected branches, squash merging, secret scanning, commit signing | Sections 10 and 12 |
| release-please documentation (manifest / monorepo mode) and GitHub CODEOWNERS docs | Section 18 |
| AICPA Trust Services Criteria (SOC 2) and the EU GDPR text | Section 19 (guidance only, not legal advice) |
| GitLab docs (merge requests, push rules, CI/CD) and Bitbucket docs (merge strategies, branch restrictions, Pipelines) | Section 20 |
| semantic-release documentation | Sections 13 and 20 |

> Tool versions and flags change over time. When a command in this file fails, check that tool's current documentation, then update this file through a PR.
