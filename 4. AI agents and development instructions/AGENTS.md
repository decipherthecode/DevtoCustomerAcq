# HOW TO FILL THIS DOCUMENT (READ THIS FIRST, THEN DELETE THIS BOX)

> **What is this file?** It is the instruction book for your AI helper (the "agent"). The agent reads it before it does any work. If something is missing here, the agent has to guess. This file exists so it never has to.
>
> **Template version:** 1.0 | **Standard:** plain Markdown, works with any AI agent
>
> ### The 5 steps
> 1. **Copy** this file into the main (root) folder of your project. Keep the name `AGENTS.md`.
> 2. **Fill** every place that says `[FILL: ...]` by replacing the whole bracket with your answer. Example: `[FILL: product name]` becomes `Tiny Tasks`.
> 3. **Read the hint box** (the indented `HOW TO FILL` box) at the top of each section. It tells you what to write and shows an example. Delete the box when you finish the section.
> 4. **Skip nothing.** If you really don't know an answer, write `UNKNOWN` (not blank). The agent will then ask you instead of guessing.
> 5. **Final check:** go to the very last section ("Final Self-Check") and tick every box.
>
> ### Symbols used in this file
> | Symbol | Meaning |
> |---|---|
> | `[FILL: ...]` | You must write something here |
> | `[PICK: a / b / c]` | Keep one choice, delete the others |
> | `[OPTIONAL]` | Delete the section if it does not apply to you |
> | ✅ | Agent may do this on its own |
> | ⚠️ | Agent must ask a human first |
> | ⛔ | Agent must never do this |
>
> ### Stuck?
> Open `AGENTS-EXAMPLE.md` to see a finished example, and `AGENTS-PROMPTS.md` for sentences you can paste to your agent. Both are optional helpers: copy them next to this file, or delete them.
>
> ### Using Claude Code?
> Claude Code reads a file called `CLAUDE.md`, not `AGENTS.md`. Create a file named `CLAUDE.md` in the same folder with one line: `@AGENTS.md`. Now both are always in sync. Other agents (Codex, Cursor, Copilot, Gemini) read `AGENTS.md` directly.
>
> ### Keep it short once filled
> Delete anything that does not apply. Do not write things like "write clean code" (agents already know). Write only things the agent could not guess. Aim to keep the finished file under 32 KiB.

---

# AGENTS.md: [FILL: product name]

**Last updated:** [FILL: date, e.g. 2026-10-17] | **Owner:** [FILL: your name] | **Status:** [PICK: Idea / Building / Beta / Launched / Growing]

---

## 0. THE GOLDEN RULES (every agent, every task)

> **HOW TO FILL:** Nothing to fill here. Read it once. Only change a rule if you truly mean it.

1. **Read this whole file before doing any work.** Then say back, in 3 lines, what you are about to do.
2. **Never guess.** If a `[FILL: ...]` is still unfilled or says `UNKNOWN`, that is a **blocker**. Stop and ask the human a short, specific question.
3. **Ask before risky actions** (list in Section 2). Everything else you may do without asking.
4. **Smallest change that works.** Do not rewrite, rename or "improve" things you were not asked to touch.
5. **Prove it.** A task is not done until the checks in Section 8 pass and you show the result.
6. **Be honest.** If something failed, say so. Never hide errors, skip tests, or say "should work" without running it.
7. **Write it down.** Record decisions and assumptions in Section 17, not just in chat.
8. **Priority when instructions conflict:** the human's latest chat message > the closest `AGENTS.md` to the file you edit > this root file > your own habits.

---

## 1. PROJECT CARD (the 60-second summary)

> **HOW TO FILL:** Answer in one short sentence each. Pretend you are telling a new friend. Example: *"Tiny Tasks is a to-do app for busy parents. It helps them plan the week in under 2 minutes."*

| Question | Your answer |
|---|---|
| Product name | [FILL: name] |
| One-sentence description | [FILL: what it is and who it is for] |
| The problem it solves | [FILL: the pain your customer has today] |
| Who is the customer? | [FILL: e.g. "freelance designers in India who invoice clients"] |
| Platforms | [PICK: Web / iOS / Android / Web + Mobile] |
| Business model | [PICK: Free / Subscription / One-time / Usage-based / Ads / Other: ___] |
| Price (if any) | [FILL: e.g. $9/month, or "free for now"] |
| Main goal for this phase | [FILL: e.g. "Launch and get the first 500 paying users"] |
| Target launch date | [FILL: date or UNKNOWN] |
| Budget limit for tools and services | [FILL: e.g. "$100 per month max"] |
| Repository link | [FILL: URL] |
| Live product link | [FILL: URL or "not live yet"] |

---

## 2. AGENT PERMISSIONS (what you can and cannot do)

> **HOW TO FILL:** The defaults below are safe. Only edit the "Add your own" lines. If you are not sure, leave the defaults.

### ✅ Do without asking (small and safe only)
- Read any file in the project (except secrets, see ⛔).
- Edit code, tests and docs **only in the files the task is about**, on a feature branch (never on main).
- Run the build, lint, type-check and test commands from Section 7.
- Commit to your own feature branch.
- Add your own: [FILL or write "none"]

### ⚠️ Ask a human first (default is ASK, so when in doubt, ask)
- Deleting, renaming or moving any file, folder, branch, data or database table.
- Editing files outside the ones the task is about, or making changes bigger than the task described.
- Adding, removing or upgrading any dependency (library, package, SDK).
- Changing any config: build files, CI/CD pipelines, environment settings, permissions, feature flags.
- Changing the database structure (migrations) or touching real customer data.
- Anything that costs money (paid APIs, new services, ads, upgrades). Check Section 13.4 first.
- Opening or merging a pull request, deploying to staging or production, or publishing to an app store.
- Changing login, payments, permissions, privacy, legal or pricing text.
- Sending email, SMS, push notifications or messages to real people, or posting anything publicly.
- Changing this `AGENTS.md` file.
- Anything you are not sure about.
- Add your own: [FILL or write "none"]

### ⛔ Never do
- Never put passwords, API keys, tokens or personal data in code, logs, chat or commits.
- Never read or change `.env` files, secret stores or real customer records unless the human says so in this chat.
- Never force-push to the main branch or rewrite shared history.
- Never turn off tests, linters, or security checks to make something pass.
- Never copy code you cannot confirm the license for.
- Never invent facts, numbers, customer quotes, reviews or metrics.
- Add your own: [FILL or write "none"]

### How to ask
When you must ask, use this format: **"I need to decide: [thing]. Options: A) ... B) ... My recommendation: [A/B] because [reason]. Which do you want?"**

---

## 3. ROLES (who does what)

> **HOW TO FILL:** If you work alone, put your name in every row. That is normal. The point is that every job has a name next to it.

| Job | Name | What they decide |
|---|---|---|
| Product owner (decides what to build) | [FILL: name] | Scope, priorities, launch go/no-go |
| Builder (writes code) | [FILL: name + "AI agent"] | How to build it |
| Quality checker (tests it) | [FILL: name] | Is it good enough to ship? |
| Launch owner (releases it) | [FILL: name] | When and how it goes live |
| Customer support owner | [FILL: name] | Replies to users |
| Emergency contact (if production breaks) | [FILL: name + phone/email] | Whether to roll back |

---

# PHASE 1: IDEA AND REQUIREMENTS

## 4. WHAT WE ARE BUILDING (and what we are not)

> **HOW TO FILL:** Think "smallest version a stranger would pay for or use happily." Write 3 to 7 must-haves. Everything else goes in "Not now". Example must-have: *"A user can sign up with email and create a task."*

### 4.1 The customer
- **Who:** [FILL: describe one real kind of person]
- **Their situation:** [FILL: when and where they have the problem]
- **How they solve it today:** [FILL: spreadsheet, a competitor, nothing...]
- **Why ours is better:** [FILL: one sentence]

### 4.2 Version 1 must-haves (MVP)
| # | Feature | A user can... | Priority |
|---|---|---|---|
| 1 | [FILL] | [FILL: "A user can ..."] | Must |
| 2 | [FILL] | [FILL] | Must |
| 3 | [FILL] | [FILL] | Must |
| 4 | [FILL] | [FILL] | Should |

### 4.3 Not now (do NOT build these)
- [FILL: e.g. "Team accounts", "Dark mode", "Android app until web is live"]

### 4.4 Success numbers (how we know it works)
| Measure | Target | When |
|---|---|---|
| Sign-ups | [FILL: number] | [FILL: date] |
| People who finish setup (activation) | [FILL: % or number] | [FILL] |
| Paying customers | [FILL: number] | [FILL] |
| Still using after 30 days (retention) | [FILL: %] | [FILL] |

### 4.5 Ready to build? (Definition of Ready)
The agent starts building only when **all** are true:
- [ ] Section 1, 4.1, 4.2 and 4.3 are filled
- [ ] Every feature has an "A user can..." sentence
- [ ] The human wrote "approved to build" in chat or in Section 17

---

# PHASE 2: DESIGN

## 5. LOOK, FEEL AND EASE OF USE

> **HOW TO FILL:** Paste links, not long descriptions. If you have no design yet, write `NO DESIGN YET` and the agent will propose one for your approval. Do not leave it blank.

| Item | Your answer |
|---|---|
| Design files (Figma etc.) | [FILL: link or NO DESIGN YET] |
| Brand colors | [FILL: hex codes or UNKNOWN] |
| Fonts | [FILL: names or UNKNOWN] |
| Tone of voice for text | [PICK: Friendly / Professional / Playful / Calm / Other] |
| Languages supported | [FILL: e.g. English only] |
| Screen sizes to support | [FILL: e.g. phone, tablet, laptop] |
| Main user journey (3-5 steps) | [FILL: e.g. Sign up → Create first task → See weekly plan] |

**Design rules for the agent**
- Reuse existing components before creating new ones.
- Every screen needs: a loading state, an empty state, and an error state.
- Meet basic accessibility: readable contrast, labels on inputs, works with keyboard (web) and screen readers.
- Do not change the look of finished screens unless asked.

---

# PHASE 3: BUILD

## 6. TECH STACK (the tools we use)

> **HOW TO FILL:** List only what is really used. Add the version number. If a row does not apply, write `N/A`. Example: *Language: TypeScript 5.6*.

| Part | Choice and version |
|---|---|
| Language(s) | [FILL] |
| Web framework | [FILL or N/A] |
| Mobile framework | [FILL or N/A: e.g. React Native, Swift, Kotlin, Flutter] |
| Database | [FILL] |
| Login / authentication | [FILL] |
| Payments | [FILL or N/A] |
| Hosting / deployment | [FILL] |
| Email / notifications | [FILL or N/A] |
| Analytics | [FILL or N/A] |
| Error tracking | [FILL or N/A] |
| Package manager | [FILL: npm / pnpm / yarn / pip ...] |

**Stack rule:** Use only the tools above. To add a new one, follow Section 2 (⚠️ ask first) and log it in Section 17.

## 7. COMMANDS (copy-paste exact)

> **HOW TO FILL:** Type the exact command you would type in the terminal. The agent runs these literally. If a command does not exist yet, write `NONE YET`. Example: *Run tests: `npm test`*.

| Job | Command |
|---|---|
| Install everything | `[FILL]` |
| Start the app locally | `[FILL]` |
| Run all tests | `[FILL]` |
| Run one test file | `[FILL]` |
| Check code style (lint) | `[FILL]` |
| Check types | `[FILL or NONE YET]` |
| Build for production | `[FILL]` |
| Start local database | `[FILL or N/A]` |
| Run database migrations | `[FILL or N/A]` ⚠️ ask first |

## 7.1 PROJECT MAP (where things live)

> **HOW TO FILL:** List the main folders in one line each. Example: `src/api/: backend routes`.

```
[FILL: folder/]  : [what lives here]
[FILL: folder/]  : [what lives here]
[FILL: folder/]  : [what lives here]
```

**Do-not-touch areas:** [FILL: e.g. `generated/`, `vendor/`, `legacy-billing/`, or "none"]

## 7.2 CODE RULES

> **HOW TO FILL:** Write only rules that are *different* from normal. If you have none, keep the defaults.

- Follow the style of the surrounding code. Match naming, folder layout and patterns already used.
- Keep files and functions small and focused.
- No secrets in code. Read settings from environment variables listed in `.env.example`.
- Every new feature gets tests (Section 8).
- Handle errors out loud: show the user a helpful message and log details privately.
- Comment the *why*, not the *what*.
- Our special rules: [FILL or "none"]

## 7.3 GIT AND CHANGE RULES

| Item | Rule |
|---|---|
| Main branch name | [FILL: main] |
| Branch naming | [FILL: e.g. `feature/short-name`, `fix/short-name`] |
| Commit message format | [FILL: e.g. `feat: add signup form`] |
| Who reviews changes | [FILL: name, or "self-review with checklist"] |
| Merge only when | Tests pass, lint passes, and the Definition of Done (Section 8.3) is ticked |

- One task = one branch = one pull request. Keep each change small.
- In every pull request write: **what changed, why, how it was tested, anything risky.**

## 7.4 SETTINGS AND SECRETS

> **HOW TO FILL:** List the *names* of settings, never the secret values. Example: `STRIPE_SECRET_KEY`: payments, test key locally.

| Setting name | What it is for | Where the real value lives |
|---|---|---|
| [FILL] | [FILL] | [FILL: e.g. hosting dashboard, password manager] |

## 7.5 WEB-ONLY NOTES [OPTIONAL]
- Browsers to support: [FILL]
- Performance goal: [FILL: e.g. main page loads in under 3 seconds on mobile data]
- SEO needed: [PICK: Yes / No]

## 7.6 MOBILE-ONLY NOTES [OPTIONAL]
- Minimum OS versions: [FILL: e.g. iOS 16, Android 10]
- Developer accounts: [FILL: Apple / Google account owner name]
- App identifiers: [FILL: bundle id / package name]
- Permissions the app asks for (camera, location...): [FILL or "none"]
- Offline behavior: [FILL: works offline? / needs internet]
- Store review rules to respect: do not use private APIs, explain every permission, include a privacy policy link.

## 7.7 AI-POWERED FEATURES [OPTIONAL]
- Model/provider used: [FILL]
- Monthly spend cap: [FILL]
- Rules: never send personal data to a model without approval; test prompts with a fixed set of examples; log failures; show users a fallback if the AI is down.

## 7.8 DEEP CHECKLISTS [OPTIONAL: delete what you don't need]

> **HOW TO FILL:** Tick a box only after it is really true and checked. Leave the rest unticked so the agent knows what is still open.

### Accessibility (everyone can use it)
- [ ] Text contrast is readable (aim for WCAG AA: 4.5:1 for normal text)
- [ ] Every image has a text description; every button and input has a label
- [ ] Everything works with keyboard only (web) and with VoiceOver/TalkBack (mobile)
- [ ] Text can be enlarged without breaking the layout
- [ ] Nothing depends on color alone; no flashing content
- [ ] Error messages say what went wrong and how to fix it

### Localization (other languages and regions)
- Languages at launch: [FILL] | Added later: [FILL or "none"]
- [ ] No text is typed directly inside code; all text lives in translation files
- [ ] Dates, times, numbers and currency use the user's local format
- [ ] Layout survives long words and right-to-left languages (if needed)
- [ ] A human who speaks the language reviews every translation (not only a machine)

### App store readiness [mobile only]
- [ ] Developer accounts are paid and active (owner: [FILL])
- [ ] App name, subtitle, description, keywords, icon and screenshots for every required device size
- [ ] Privacy policy URL, and privacy "nutrition label" / data safety answers are accurate
- [ ] Every permission has a clear reason shown to the user
- [ ] Test login given to reviewers (if the app needs login), with no real customer data
- [ ] Age rating, content rating and export/encryption questions answered
- [ ] Release notes written; staged rollout planned [PICK: Yes / No]
- [ ] Plan for review time and possible rejection (allow several days before the target date)

---

# PHASE 4: TEST AND QUALITY

## 8. HOW WE CHECK QUALITY

> **HOW TO FILL:** Keep the defaults and only fill the "must always work" list: the 3 to 5 things that, if broken, would make customers leave. Example: *sign up, log in, pay, main feature, delete account.*

### 8.1 Must always work (critical paths)
1. [FILL]
2. [FILL]
3. [FILL]

### 8.2 Test layers
| Layer | What it checks | When to run |
|---|---|---|
| Unit tests | One small piece of code | Every change |
| Integration tests | Pieces working together (e.g. app + database) | Every pull request |
| End-to-end tests | A real user journey, start to finish | Before every release |
| Manual check | A human tries it on real devices | Before every release |

### 8.3 Definition of Done (a task is finished only when all are ticked)
- [ ] It does what the "A user can..." sentence says
- [ ] New and old tests pass
- [ ] Lint and type checks pass
- [ ] Loading, empty and error states are handled
- [ ] No secrets, no debug leftovers, no commented-out code
- [ ] Docs, changelog and this file updated if behavior changed
- [ ] The agent has shown the proof (test output or screenshot)

### 8.4 Bug severity (how urgent is it?)
| Level | Meaning | Action |
|---|---|---|
| S1 Critical | App down, data loss, payment or security problem | Stop everything, tell the human now |
| S2 High | Main feature broken for many users | Fix before next release |
| S3 Medium | Annoying, has a workaround | Schedule it |
| S4 Low | Cosmetic | Backlog |

---

## 9. SECURITY, PRIVACY AND LEGAL

> **HOW TO FILL:** Answer honestly. "Personal data" means anything that identifies a person: name, email, phone, photos, location. If you collect any, you need a privacy policy.

| Question | Your answer |
|---|---|
| What personal data do we collect? | [FILL or "none"] |
| Where is it stored? | [FILL] |
| Countries our users live in | [FILL: affects laws such as GDPR, CCPA, India DPDP] |
| Do kids under 13 or 16 use it? | [PICK: Yes / No / Maybe] |
| Privacy policy link | [FILL or NOT YET] |
| Terms of service link | [FILL or NOT YET] |
| Payment data handled by | [FILL: e.g. Stripe (we never store card numbers)] |

**Security rules (always on)**
- Ask for the minimum data needed. Do not collect "just in case".
- Passwords must be hashed by the auth provider, never stored plain.
- Check every input from users. Never trust it.
- Keep dependencies updated; run the security audit command before each release: `[FILL or NONE YET]`.
- Backups: [FILL: what, how often, who restores]
- If a leak or attack is suspected: stop, do not delete evidence, tell the human immediately.

⚠️ This file is not legal advice. A human should have a lawyer or trusted expert review privacy and terms before launch.

---

# PHASE 5: RELEASE AND LAUNCH

## 10. ENVIRONMENTS AND RELEASING

> **HOW TO FILL:** An *environment* is a copy of your product. Fill in the links. If you only have "my laptop" and "live", write `N/A` for staging.

| Environment | Purpose | Link | Who may deploy |
|---|---|---|---|
| Local | Building on your computer | localhost | Agent ✅ |
| Staging (test copy) | Final check before customers see it | [FILL or N/A] | Agent ⚠️ ask first |
| Production (live) | Real customers | [FILL] | Human only |

**How a release works (fill the real steps):**
1. [FILL: e.g. merge to main → automatic deploy to staging]
2. [FILL: e.g. human tests staging with checklist 10.1]
3. [FILL: e.g. human clicks "promote to production"]

**Rollback (undo a bad release):** [FILL: exact steps or command. Example: "In hosting dashboard click Previous deployment → Redeploy."] Agents must **never** deploy to production without a rollback plan written here.

### 10.1 Go / No-Go checklist (all must be ✅ to launch)
- [ ] All Version 1 must-haves (4.2) work
- [ ] Critical paths (8.1) tested on real devices/browsers
- [ ] No open S1 or S2 bugs
- [ ] Privacy policy and terms are live
- [ ] Payments tested with a real small purchase and a refund (if applicable)
- [ ] Error tracking and analytics are receiving data
- [ ] Backups exist and a restore was tried once
- [ ] Support email/chat is working and monitored
- [ ] Rollback steps tested
- [ ] Store listing ready (mobile): name, description, screenshots, icon, age rating, privacy answers
- [ ] Launch announcement drafted and channels chosen (Section 13.1)
- [ ] Human wrote "GO" for launch in Section 17

---

## 11. WATCHING THE PRODUCT (monitoring and emergencies)

> **HOW TO FILL:** Say where you look when something is wrong. Example: *"Sentry for errors, UptimeRobot pings every 5 minutes."*

| Item | Your answer |
|---|---|
| Where errors show up | [FILL] |
| Uptime check | [FILL or NONE YET] |
| Who gets alerts and how | [FILL: name + email/phone] |
| Check-in schedule after launch | [FILL: e.g. every day for 2 weeks] |

**If something breaks (S1):** 1) Tell the human. 2) Stop new releases. 3) Roll back (Section 10). 4) Tell affected users honestly if needed. 5) Write what happened and how to prevent it in Section 17.

---

# PHASE 6: ONBOARDING AND SUPPORT

## 12. FIRST-USER EXPERIENCE AND SUPPORT

> **HOW TO FILL:** "Onboarding" is how a new user gets their first win. Write the *first win* in plain words. Example: *"A new user creates their first task within 2 minutes."*

| Item | Your answer |
|---|---|
| The "first win" (aha moment) | [FILL] |
| Max time to first win | [FILL: e.g. 2 minutes] |
| Welcome message / email | [FILL: link or NOT YET] |
| Help center / FAQ | [FILL: link or NOT YET] |
| Support channel | [PICK: Email / Chat / WhatsApp / Discord / Other] |
| Support reply target | [FILL: e.g. within 24 hours] |
| How feedback is collected | [FILL: in-app form / email / interviews] |

**Rules for the agent about users**
- Never message real users without human approval (Section 2).
- Turn repeated support questions into FAQ drafts and show them to the human.
- Summarize feedback into themes, never invent quotes.

---

# PHASE 7: GROWTH TO THE FIRST 500 CUSTOMERS

## 13. THE ROAD TO 500

> **HOW TO FILL:** Fill the "How we will find them" and "Date goal" columns. A *customer* means: [PICK: someone who signed up / someone who is active / someone who paid]. Write that choice once and keep it the same all the way.

**Our definition of "customer":** [FILL: pick one and write it clearly]

| Milestone | Date goal | How we will find them | What we must learn | Gate to move on |
|---|---|---|---|---|
| **0 → 10** (friends, early fans) | [FILL] | [FILL: personal outreach, communities] | Do they get the first win? Why do they leave? | 7 of 10 reach the first win |
| **10 → 50** (early adopters) | [FILL] | [FILL] | What do they ask for most? Will they pay? | [FILL: e.g. 5 paying or 40% return weekly] |
| **50 → 100** | [FILL] | [FILL] | Which channel brings the best users? | [FILL] |
| **100 → 250** | [FILL] | [FILL] | What breaks as we grow? What does support cost? | [FILL] |
| **250 → 500** | [FILL] | [FILL] | Can we repeat what works without extra effort? | 500 reached and retention is stable |

### 13.1 Channels
| Channel | Plan | Owner | Cost |
|---|---|---|---|
| [FILL: e.g. Reddit/communities, SEO, social, email, partners, ads] | [FILL] | [FILL] | [FILL] |

### 13.2 The numbers we track (every week)
| Metric | Meaning | This week | Target |
|---|---|---|---|
| Visitors | People who found us | | |
| Sign-ups | People who joined | | |
| Activation | People who got the first win | | |
| Retention | People who came back | | |
| Revenue | Money earned | | |
| Support tickets | Problems reported | | |
| Cost per customer | Money spent ÷ customers | | |

### 13.3 The weekly loop (run every week)
1. **Measure:** update 13.2 using real data only.
2. **Listen:** read feedback and support tickets; list the top 3 problems.
3. **Decide:** pick at most 3 things to change. Log them in Section 17.
4. **Build or fix:** follow Phases 3 and 4.
5. **Release safely:** follow Section 10.
6. **Repeat.**

### 13.4 Money tracker (budget and spending caps)

> **HOW TO FILL:** List every paid thing, even small ones. "Cap" is the most you will allow per month. The agent must not push any item past its cap and must ask first (Section 2) before adding a new paid item.

| Item | Provider | Cost per month | Monthly cap | Owner | Renewal date |
|---|---|---|---|---|---|
| Hosting | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Database | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| AI / API usage | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Email / SMS | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Domain and app-store fees | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Marketing / ads | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| **Total** | | [FILL] | [FILL: must be ≤ budget in Section 1] | | |

- If spending reaches **80% of any cap**, the agent must tell the human right away.
- Update this table in the first week of every month.

**Growth rules for the agent**
- Never buy followers, fake reviews or fake testimonials. Never fake numbers.
- Never send marketing messages without consent and an unsubscribe option.
- Test one change at a time so we know what worked.
- Never spend money, run ads or post publicly without approval.

---

# KEEPING THIS FILE HEALTHY

## 14. WHEN SOMETHING IS UNCLEAR

If the file does not answer your question: (1) look in the closest nested `AGENTS.md`, (2) look in the project docs: [FILL: link or "none"], (3) **ask the human.** Do not guess.

## 15. BIGGER PROJECTS (more than one app or package) [OPTIONAL]
Put a smaller `AGENTS.md` inside each sub-folder (for example `web/` and `mobile/`). The one closest to the file you are editing wins. Add one line at the top of each: *"Also read the root AGENTS.md."*

## 16. KNOWLEDGE LINKS [OPTIONAL]
| Topic | Link |
|---|---|
| Completed example of this file | `AGENTS-EXAMPLE.md` (see how a real project fills it) |
| Ready-to-paste prompts for each phase | `AGENTS-PROMPTS.md` |
| Product requirements | [FILL or none] |
| Design system | [FILL or none] |
| API docs | [FILL or none] |
| Analytics dashboard | [FILL or none] |
| Customer feedback board | [FILL or none] |

## 17. DECISIONS, ASSUMPTIONS AND OPEN QUESTIONS

> **HOW TO FILL:** Add a row whenever something is decided, assumed or unclear. The agent also writes here. Newest on top.

| Date | Type (Decision / Assumption / Question / Approval) | What | Who | Status |
|---|---|---|---|---|
| [FILL] | [FILL] | [FILL] | [FILL] | [Open / Done] |

## 18. GLOSSARY (words with special meaning here) [OPTIONAL]
| Word | Meaning in this project |
|---|---|
| [FILL] | [FILL] |

## 19. CHANGELOG OF THIS FILE
| Date | What changed | By |
|---|---|---|
| [FILL: date] | Created from template v1.0 | [FILL: name] |

**Maintenance rules:** Review this file at every phase change and after any mistake the agent makes twice. If you tell the agent the same thing two times, add it here. Delete rules that are old or never used.

---

## 20. FINAL SELF-CHECK (tick before you share this file)

- [ ] No `[FILL: ...]` or `[PICK: ...]` is left. Unknowns say `UNKNOWN`.
- [ ] Every command in Section 7 was run once by a human and works
- [ ] No passwords, keys or private data are anywhere in this file
- [ ] Sections 2 and 10 clearly say what needs human approval
- [ ] The rollback plan is written (Section 10)
- [ ] The definition of "customer" in Section 13 is chosen
- [ ] Unused `[OPTIONAL]` sections are deleted
- [ ] I asked the agent: *"Summarize this file in 5 lines and list anything you would have to guess."* and fixed the gaps
- [ ] `CLAUDE.md` with `@AGENTS.md` exists (if using Claude Code)
