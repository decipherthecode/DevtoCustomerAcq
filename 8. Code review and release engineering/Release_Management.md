# HOW TO FILL IN THIS DOCUMENT (READ THIS FIRST)

> **Template name:** Release_Management.md
> **Folder:** Code review and release engineering
> **Template version:** 1.0
> **Covers:** AI-driven development → code review → testing → release → launch → **your first 500 customers**
> **Built for:** Web apps / SaaS and mobile apps (iOS + Android)
> **AI rule:** AI helps, **humans approve everything**.

## What is this document?

This is **one file** that holds the whole plan for getting your product from "code written" to "500 happy customers using it." You fill in the blanks. When you are done, anyone (a teammate, a manager, or an AI agent) can read it and know **what is shipping, who decides, what "good" looks like, and what to do if something breaks.**

Think of it like a **flight checklist for a plane**. Pilots never trust memory. They read the list.

## The 7 simple rules

1. **Answer every question.** Never leave a blank. If a question does not apply, write `N/A – because <reason>`. If you do not know yet, write `UNKNOWN – <name> will find out by <date>`.
2. **Use plain words and real numbers.** Write "fewer than 1 in 100 users see an error," not "low error rate."
3. **One answer = one line when possible.** Short is good. Details go in the "Notes" line.
4. **Use the example as a guide, not a copy.** The example shows the *style* of a good answer.
5. **If unsure, use the "If unsure" default.** Every question has a safe starting answer. Replace it later when you learn more.
6. **Names beat roles.** Write a real person's name ("Priya Shah"), not "the team."
7. **Dates beat "soon."** Write `2026-11-03`, not "next week." (Format: `YYYY-MM-DD`.)

## Status symbols (use these everywhere)

| Symbol | Meaning |
|---|---|
| ✅ | Done and checked |
| 🟡 | In progress |
| ⬜ | Not started |
| ❌ | Failed / blocked |
| ➖ | Not applicable (write why) |

## How each question looks

```
**Q1.1 – The question in plain words?**
- Why we ask: the reason, in one sentence.
- Example: a sample good answer.
- If unsure: a safe default you can use.
- ✍️ Your answer: ______________________
```

Replace the `______` with your answer. Do not delete the question.

## How long will this take?

| Your goal | What to fill | Time |
|---|---|---|
| **Quick start** (small project, first draft) | Parts 0, 1, 3, 9, 10, 11 only. Mark the rest `⬜`. | ~30 min |
| **Standard** (most projects) | Parts 0–17 | ~2 hours |
| **Full** (launch-ready, audited) | Everything, including Appendices | ~half a day |

## The big picture (the 10 stages of this document)

```
 BUILD → REVIEW → TEST → SECURE → PACKAGE → GO/NO-GO → ROLLOUT → LAUNCH → FIRST 500 → LEARN
 (P4-5)  (P6A)   (P6B)  (P6C)    (P7-9)    (P10)      (P11)     (P12-13)  (P15)      (P17)
```

Also: Part 14 = legal/privacy, Part 16 = when things go wrong, Part 18 = release log, Part 19 = sign-off.

## Who can fill this in?

Anyone. If you are a beginner: read the question, read the example, type your answer. If you get stuck, use the **If unsure** line and leave a note in the *Notes* line so someone can check it later.

## Using an AI agent to help

You may ask an AI agent to **draft** answers, **check** for blanks, or **summarize**. The AI **may not** mark any approval (✅ in a sign-off box) on behalf of a human. See Part 4.

**Ready-to-paste AI prompt (to check your finished document):**

```
Read Release_Management.md. List every question that is blank, says TBD, or has a
vague answer (no number, no name, no date). Do not fix them. Just list them with
their Q-number and tell me what is missing. Do not approve anything.
```

---

# DOCUMENT CONTROL

| Field | Your answer |
|---|---|
| Product name | ______ |
| This release's version number (see Part 8) | ______ |
| Document owner (one person) | ______ |
| Date started (YYYY-MM-DD) | ______ |
| Last updated (YYYY-MM-DD) | ______ |
| Document status | ⬜ Draft / 🟡 In review / ✅ Approved |
| Where this file lives (link or path) | ______ |

**Change history** (add a row every time you change an answer in a meaningful way):

| Date | Who | What changed | Why |
|---|---|---|---|
| ______ | ______ | ______ | ______ |

---

# PART 0 – PRODUCT SNAPSHOT

*Goal: anyone can understand what this product is in 60 seconds.*

**Q0.1 – What does the product do, in one sentence a 10-year-old could understand?**
- Why we ask: if you cannot say it simply, the release plan will be fuzzy too.
- Example: "A phone app that reminds people to water their plants."
- If unsure: ask a friend outside the project to read your answer. If they are confused, rewrite it.
- ✍️ Your answer: ______

**Q0.2 – Who is it for? (your ideal first customer)**
- Why we ask: your first 500 customers should look like this person.
- Example: "Apartment dwellers aged 25–40 with 3+ houseplants."
- If unsure: describe one real person you know who would use it.
- ✍️ Your answer: ______

**Q0.3 – What type of product is it? (tick all that apply)**
- Why we ask: web and mobile releases work very differently.
- If unsure: tick every one you are building.
- ✍️ Your answer:
  - [ ] Web app / SaaS (runs in a browser)
  - [ ] iOS app (Apple App Store)
  - [ ] Android app (Google Play)
  - [ ] Backend / API behind the apps
  - [ ] Uses AI/LLM features inside the product (see Appendix B)
  - [ ] Other: ______

**Q0.4 – Which tools do you use? (fill what exists, write `none` if not used)**
- Why we ask: so nobody guesses where things live.
- If unsure: write `none yet` and fill later.

| Tool job | Tool name | Link |
|---|---|---|
| Code storage (e.g., GitHub, GitLab) | ______ | ______ |
| Task tracking (e.g., Jira, Linear, GitHub Issues) | ______ | ______ |
| Automatic build & test (CI/CD) | ______ | ______ |
| Hosting / cloud (web + backend) | ______ | ______ |
| App store accounts (Apple / Google) | ______ | ______ |
| Error & crash tracking (e.g., Sentry, Crashlytics) | ______ | ______ |
| Monitoring dashboards & alerts | ______ | ______ |
| Feature flags (switches to turn features on/off) | ______ | ______ |
| Customer support inbox | ______ | ______ |
| Team chat for release day | ______ | ______ |
| AI coding / review agents used | ______ | ______ |

**Q0.5 – What is the one date you are aiming for the public launch?**
- Why we ask: every other date in this document counts back from it.
- Example: `2027-02-15`
- If unsure: pick a date, then change it at the Go/No-Go meeting if needed.
- ✍️ Your answer: ______

---

# PART 1 – GOALS AND "WHAT DOES SUCCESS MEAN?"

*Goal: write down, before launch, what "it worked" looks like. No guessing later.*

**Q1.1 – What are the top 3 things this release must achieve?**
- Why we ask: a release with no goal cannot succeed or fail.
- Example: "1) 500 signed-up customers. 2) At least 40% still active after 7 days. 3) No lost customer data."
- If unsure: use the example and change the numbers.
- ✍️ Your answer: 1) ______ 2) ______ 3) ______

**Q1.2 – What does "launched" mean for you? (pick one)**
- Why we ask: people use the word differently.
- If unsure: pick **B**.
- ✍️ Your answer:
  - [ ] A. Available to anyone in the stores / on the web
  - [ ] B. Available to anyone **and** reached 100% rollout with no open urgent bugs
  - [ ] C. Invite-only
  - [ ] D. Other: ______

**Q1.3 – What is your "first 500 customers" definition?**
- Why we ask: "customer" can mean a sign-up, a paying user, or a daily user.
- Example: "A customer = someone who creates an account AND completes the first task."
- If unsure: use the example.
- ✍️ Your answer: A customer is ______

**Q1.4 – What are your success numbers? (fill the Target; fill Actual later)**
- Why we ask: numbers make decisions easy and arguments short.
- If unsure: use the **Starter Target** column.

| Measure | Starter Target | Your Target | Actual (fill after) |
|---|---|---|---|
| Customers reached | 500 | ______ | ______ |
| Crash-free users (mobile) | ≥ 99.5% | ______ | ______ |
| Web errors (requests that fail) | < 1% | ______ | ______ |
| Page/app speed (95 of 100 users wait less than) | < 3 seconds | ______ | ______ |
| Still using after 7 days | ≥ 30% | ______ | ______ |
| Customer rating (store or survey) | ≥ 4.0 / 5 | ______ | ______ |
| Urgent support tickets per 100 customers | ≤ 5 | ______ | ______ |
| Time to fix a serious problem | < 4 hours | ______ | ______ |

**Q1.5 – What would make us STOP the launch? (a "red line")**
- Why we ask: decide when you are calm, not during a crisis.
- Example: "Any loss or leak of customer data. Any payment charged wrongly."
- If unsure: use the example.
- ✍️ Your answer: ______

---

# PART 2 – SCOPE: WHAT IS (AND IS NOT) IN THIS RELEASE

**Q2.1 – List what is shipping. (one line per feature)**
- Why we ask: "scope creep" (sneaking things in) causes most late-night problems.
- Example: "Sign-up with email; plant list; watering reminders (push)."
- If unsure: copy the "Done" column from your task tracker.

| # | Feature / fix | Task link | Owner | Status |
|---|---|---|---|---|
| 1 | ______ | ______ | ______ | ⬜ |
| 2 | ______ | ______ | ______ | ⬜ |
| 3 | ______ | ______ | ______ | ⬜ |

**Q2.2 – What is NOT shipping this time? (so nobody is surprised)**
- Example: "Dark mode, Spanish language, Android tablets."
- If unsure: write `Nothing else is promised.`
- ✍️ Your answer: ______

**Q2.3 – Does this release change something that already exists for customers (data, prices, logins, files)?**
- Why we ask: changes to existing data are the riskiest and hardest to undo.
- If unsure: write `Yes – assume so` and complete Q9.6.
- ✍️ Your answer: ☐ No  ☐ Yes → what changes: ______

**Q2.4 – What must exist before the first customer can use the product? (tick all that are needed)**
- ✍️ Your answer:
  - [ ] Privacy policy page
  - [ ] Terms of service
  - [ ] Support email or help page
  - [ ] Payment setup (if you charge money)
  - [ ] App store listing (screenshots, description)
  - [ ] Account deletion option (Apple/Google require it for apps with accounts)
  - [ ] Other: ______

---

# PART 3 – PEOPLE AND ROLES

*Goal: for every decision, one named human is in charge.*

**Q3.1 – Who plays each role? (write a real name for every row)**
- Why we ask: when something breaks at 2 a.m., "the team" cannot answer the phone.
- If unsure: one person can hold several roles in a small team. Write their name in each row, and add a backup.

| Role | What this person does | Name | Backup name | How to reach (phone/chat) |
|---|---|---|---|---|
| **Release Manager** | Runs the plan, calls meetings, keeps this document up to date | ______ | ______ | ______ |
| **Product Owner** | Decides what ships and who the customers are | ______ | ______ | ______ |
| **Tech Lead** | Final say on code safety and design | ______ | ______ | ______ |
| **Code Reviewer(s)** | Reads and approves code changes | ______ | ______ | ______ |
| **QA Lead** | Says if testing passed | ______ | ______ | ______ |
| **Security Owner** | Checks for security problems | ______ | ______ | ______ |
| **On-call Engineer** | Fixes problems after release | ______ | ______ | ______ |
| **Support Lead** | Talks to customers with problems | ______ | ______ | ______ |
| **Communications Owner** | Writes release notes and announcements | ______ | ______ | ______ |
| **Final Approver (Go/No-Go)** | One person who says GO or NO-GO | ______ | ______ | ______ |

**Q3.2 – Who decides if two people disagree?**
- Example: "The Final Approver. If they are away, the Product Owner."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q3.3 – What are the team's working hours and time zones? When is the "do not release" time?**
- Why we ask: avoid shipping right before people go to sleep or on holidays.
- Example: "Release Tue–Thu, 10:00–15:00 Eastern. Never Friday after 12:00, weekends, or holidays."
- If unsure: use the example.
- ✍️ Your answer: ______

---

# PART 4 – RULES FOR AI AGENTS (HUMANS APPROVE EVERYTHING)

*Goal: AI makes work faster and safer. Humans stay in charge.*

**The house rule (do not change without a signed decision):**
> AI agents may **draft, suggest, check, summarize, and flag**. AI agents may **not approve, merge to the main branch, release to customers, change production data, change secrets/keys, or sign any gate** in this document. A named human does these.

**Q4.1 – Which AI agents/tools are used, and what is each allowed to do?**
- Why we ask: unclear AI power causes accidents.
- If unsure: allow only the "Allowed" actions below; everything else is "Not allowed."

| AI tool / agent | Allowed (tick) | Not allowed |
|---|---|---|
| ______ | ☐ Write code ☐ Write tests ☐ Review code (comments only) ☐ Draft release notes ☐ Summarize logs ☐ Check this document for blanks | Approve, merge, deploy, touch production, see passwords/keys |
| ______ | ☐ Write code ☐ Write tests ☐ Review code (comments only) ☐ Draft release notes ☐ Summarize logs ☐ Check this document for blanks | Approve, merge, deploy, touch production, see passwords/keys |

**Q4.2 – Who is the human responsible for each AI agent's output?**
- Example: "All code from the coding agent is owned by whoever opened the change request (pull request)."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q4.3 – What must a human check on AI-written work? (tick all you will do)**
- Why we ask: AI can write confident but wrong code.
- If unsure: tick all.
- ✍️ Your answer:
  - [ ] A human read every changed line (not just the summary)
  - [ ] Tests were run and passed, and a human saw the result
  - [ ] No secrets, passwords, or customer data are in the code or prompts
  - [ ] New libraries added by AI were checked (real, maintained, safe license)
  - [ ] The change does what the task asked and nothing extra
  - [ ] AI-written code is labeled in the change request (e.g., "AI-assisted")

**Q4.4 – What data is AI never allowed to see?**
- Example: "Real customer data, passwords, API keys, payment info, private keys."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q4.5 – How do we record what AI did? (audit trail)**
- Example: "Each AI-assisted change request has the tag `ai-assisted` and links the AI chat or log."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q4.6 – What happens if an AI agent does something it should not (e.g., tries to deploy)?**
- Example: "Stop the agent, tell the Release Manager, review the log, rotate any exposed keys, write a note in Part 18."
- If unsure: use the example.
- ✍️ Your answer: ______

---

# PART 5 – ENVIRONMENTS AND CODE BRANCHES

*Goal: know where code lives at every step, and keep the customer-facing place safe.*

**Q5.1 – What "places" does your code run in?**
- Why we ask: code should be proven in a safe place before customers see it.
- If unsure: use the three-row starter and delete what you do not need.

| Environment | Who uses it | Real customer data? | Link/address |
|---|---|---|---|
| **Development** (each developer's machine) | Developers | Never | ______ |
| **Staging / Test** (copy of production) | Team + testers | Never (use fake data) | ______ |
| **Production** (live) | Customers | Yes | ______ |

**Q5.2 – What are your code branches (lanes) called, and what are the rules?**
- Example: `main` = always ready to release. Short-lived `feature/*` branches. `release/x.y.z` for release candidates. `hotfix/*` for urgent fixes.
- If unsure: use the example.
- ✍️ Your answer: ______

**Q5.3 – What must be true before code can enter `main`?**
- Why we ask: this is the first safety gate.
- If unsure: tick all.
- ✍️ Your answer:
  - [ ] At least ___ human reviewer(s) approved (starter: 1; 2 for risky areas)
  - [ ] All automatic checks passed (build, tests, style, security scan)
  - [ ] The branch is up to date with `main`
  - [ ] The author is **not** the only approver
  - [ ] No one can push directly to `main` (branch protection is ON)

**Q5.4 – Who can approve a merge into `main`? Who can release to production?**
- Example: "Approve merge: any reviewer in Q3.1. Release to production: Release Manager, after Final Approver says GO."
- If unsure: use the example.
- ✍️ Your answer: ______

---

# PART 6 – QUALITY GATES (REVIEW → TEST → SECURE)

*Goal: find problems early, when they are cheap to fix.*

## 6A – Code review

**Q6A.1 – What does a reviewer check? (tick all)**
- ✍️ Your answer:
  - [ ] Does it do what the task says?
  - [ ] Is it easy to read and understand?
  - [ ] Are there tests for the new/changed behavior?
  - [ ] Could it break something that already works?
  - [ ] Are errors handled (what happens when something goes wrong)?
  - [ ] Does it handle personal data safely?
  - [ ] Does the change include a way to undo it (rollback / switch off)?
  - [ ] Is it small enough to review well? (starter: under ~400 changed lines)

**Q6A.2 – How fast must reviews happen?**
- Example: "First response within 1 business day."
- If unsure: use the example.
- ✍️ Your answer: ______

## 6B – Testing

**Q6B.1 – Which tests will you run? Fill the "Pass rule" and who runs it.**
- Why we ask: different tests catch different problems.
- If unsure: use the starter pass rules.

| Test type | What it checks (plain words) | Pass rule (starter) | Who/what runs it | Status |
|---|---|---|---|---|
| Unit tests | Small pieces of code | 100% of tests pass | Automatic | ⬜ |
| Integration tests | Pieces working together (app ↔ server ↔ database) | 100% pass | Automatic | ⬜ |
| End-to-end tests | A full user journey (sign up → use → log out) | Top 5 journeys pass | Automatic + QA | ⬜ |
| Manual exploratory testing | A human tries to break it | No open "Critical/High" bugs | QA Lead | ⬜ |
| Performance / load test | Many users at once | Meets Q1.4 speed target at 2× expected users | QA/Tech Lead | ⬜ |
| Compatibility test | Different browsers / phones / OS versions | Works on the devices in Q6B.2 | QA | ⬜ |
| Accessibility test | Usable with screen readers, large text, color contrast | No major blockers | QA | ⬜ |
| Upgrade test (mobile) | Old app version → new version keeps data | Passes | QA | ⬜ |
| Data migration test | Database changes work **and can be undone** | Passes forward and backward | Engineer | ⬜ |
| Beta / real-user test | Friendly users try it | See Parts 11 and 15 | Product Owner | ⬜ |

**Q6B.2 – Which browsers and devices MUST work?**
- Example: "Chrome, Safari, Edge (latest 2 versions); iPhone 12 and newer on the last 2 iOS versions; Android 10+ on Pixel and Samsung mid-range."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q6B.3 – How do we rate bugs, and what blocks a release?**
- If unsure: use this scale.

| Level | Meaning | Example | Blocks release? |
|---|---|---|---|
| **Critical (Sev 1)** | Data loss, security hole, app cannot open, money wrong | App crashes on launch | **Yes, always** |
| **High (Sev 2)** | Main feature broken, no workaround | Cannot save a plant | **Yes** |
| **Medium (Sev 3)** | Feature broken but workaround exists | Wrong icon after refresh | Only if Product Owner says so |
| **Low (Sev 4)** | Cosmetic | Text slightly misaligned | No |

- ✍️ Your changes (if any): ______

## 6C – Security and supply-chain checks

*Why: the National Institute of Standards and Technology (NIST) "Secure Software Development Framework" asks teams to keep proof of what is inside each release (such as a software bill of materials, or SBOM) and a way for others to verify it.*

**Q6C.1 – Which security checks will you run? (tick all)**
- If unsure: tick all.
- ✍️ Your answer:
  - [ ] Scan for secrets (passwords/keys) in code
  - [ ] Scan libraries for known vulnerabilities
  - [ ] Scan our own code for common flaws (static analysis)
  - [ ] Test the running app for common flaws (dynamic/pen test) before launch
  - [ ] Check licenses of libraries (can we legally use them?)
  - [ ] Create a **software bill of materials (SBOM)** – a list of every ingredient in this release
  - [ ] Sign the release files so no one can swap them in secret
  - [ ] Keep the build record (who built it, from which code, when) – "provenance"
  - [ ] Check login, permissions, and "can user A see user B's data?" tests

**Q6C.2 – What security problems block release?**
- Example: "Any known Critical or High vulnerability with a fix available; any secret found in code."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q6C.3 – Where do we store the SBOM, build record, and signatures for each release?**
- Example: "In the release folder at `<link>`, kept for at least 2 years."
- If unsure: attach them to the release in your code host.
- ✍️ Your answer: ______

**Q6C.4 – How are secrets (passwords, keys, certificates) stored and who can use them?**
- Example: "In the secrets vault. Only the CI system and Release Manager can read them. App signing keys are backed up offline."
- If unsure: use the example. **Never paste a secret into this document.**
- ✍️ Your answer: ______

---

# PART 7 – PACKAGING THE RELEASE CANDIDATE

*A "release candidate" (RC) is the exact build you plan to ship. After it is chosen, **nothing changes** unless you build a new RC.*

**Q7.1 – When do we "freeze" (stop adding features)?**
- Example: "Code freeze 5 working days before launch. Only Critical/High bug fixes after that."
- If unsure: use the example.
- ✍️ Your answer: Freeze date ______  Rules after freeze: ______

**Q7.2 – What proves the release candidate is the right one?**
- If unsure: tick all.
- ✍️ Your answer:
  - [ ] Built automatically by the CI system (not on someone's laptop)
  - [ ] Version number set (Part 8)
  - [ ] Same build file was tested in staging and is the one to ship
  - [ ] Checksum (digital fingerprint) recorded: ______
  - [ ] SBOM and build record attached

**Q7.3 – Mobile only: what is needed for the store?**
- Why we ask: stores have review times you cannot control.
- If unsure: submit for review at least **5 working days** before launch.
- ✍️ Your answer:
  - [ ] Apple: app uploaded, review notes written, test login provided to reviewers, privacy "nutrition labels" filled in
  - [ ] Apple: **Phased Release** option turned ON for this version (may not be available for an app's very first release)
  - [ ] Google: release created in the Production track with a **staged rollout percentage**
  - [ ] Google: Data safety form and content rating completed
  - [ ] Store listing text and screenshots approved
  - [ ] Submitted for review on (date): ______  Expected approval: ______
  - [ ] Plan for what we do if review is rejected: ______

**Q7.4 – Web only: how is the release deployed?**
- Example: "Automatic deploy from the `release` branch to production by the CI system, behind feature flags, to 1% of users first."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q7.5 – Which features are hidden behind a "feature flag" (an on/off switch) so we can turn them off without a new release?**
- Why we ask: switching off is much faster than shipping a fix, especially on mobile where stores take days.
- Example: "New onboarding screen (`flag: new_onboarding`), push reminders (`flag: push_reminders`)."
- If unsure: put every risky new feature behind a flag.

| Flag name | What it controls | Default at launch | Owner | Planned removal date |
|---|---|---|---|---|
| ______ | ______ | Off / On | ______ | ______ |

---

# PART 8 – VERSION NUMBERS, NAMES, AND RELEASE NOTES

**Q8.1 – What is the version number of this release?**
- Why we ask: a version number tells everyone exactly which build they are talking about. We use **Semantic Versioning: MAJOR.MINOR.PATCH**.
  - **MAJOR** (1.0.0 → 2.0.0): big or breaking change
  - **MINOR** (1.2.0 → 1.3.0): new feature, nothing breaks
  - **PATCH** (1.2.3 → 1.2.4): bug fix only
- Example: first public launch = `1.0.0`. First hotfix = `1.0.1`.
- If unsure: first launch `1.0.0`.
- ✍️ Your answer: ______

**Q8.2 – Mobile build numbers**
- Why we ask: stores require every upload to have a higher build number than the last.
- Example: "Version 1.0.0, build 42. Each upload adds 1."
- If unsure: use the example.
- ✍️ Your answer: iOS build ______  Android versionCode ______

**Q8.3 – How are release candidates and hotfixes named?**
- Example: `1.0.0-rc.1`, `1.0.0-rc.2`, hotfix `1.0.1`.
- If unsure: use the example.
- ✍️ Your answer: ______

**Q8.4 – Release notes (what changed). Write for customers, not engineers.**
- Why we ask: customers and support need to know what is new.
- Example: "New: reminders now tell you which plant is thirsty. Fixed: app no longer closes when you add a photo."
- If unsure: draft with AI, then a human edits and approves.
- ✍️ Your answer:
  - **Added:** ______
  - **Changed:** ______
  - **Fixed:** ______
  - **Removed:** ______
  - **Known issues (be honest):** ______
  - **Where published (store, website, in-app, email):** ______

---

# PART 9 – CHANGE RISK AND ROLLBACK PLAN

*Goal: every release must be reversible before go-live. Practice undoing it **before** you need to.*

**Q9.1 – How risky is this release? (pick one)**
- If unsure: pick **Medium** and ask the Tech Lead to confirm.
- ✍️ Your answer: ☐ Low (small fix) ☐ Medium (new feature) ☐ High (data, payments, logins, big change)

**Q9.2 – List the biggest things that could go wrong and how we would notice and fix them.**
- If unsure: copy these starter rows and add your own.

| What could go wrong | How likely (L/M/H) | How bad (L/M/H) | How we'd notice | What we'd do | Owner |
|---|---|---|---|---|---|
| App crashes on start | ______ | ______ | Crash dashboard | Halt rollout, flag off, hotfix | ______ |
| Customers can't log in | ______ | ______ | Login error alert | Roll back server change | ______ |
| Slow or down servers | ______ | ______ | Uptime & speed alerts | Scale up / roll back | ______ |
| Wrong data shown or lost | ______ | ______ | Support tickets, data checks | Stop release, restore backup | ______ |
| Payment errors | ______ | ______ | Payment alerts | Switch off payments flag | ______ |
| Store rejects the app | ______ | ______ | Store email | Fix and resubmit; delay launch | ______ |
| ______ | ______ | ______ | ______ | ______ | ______ |

**Q9.3 – Rollback: how do we go back?**
- If unsure: fill all four rows.

| Part | How to undo it | Who does it | Time it takes | Tested on (date) |
|---|---|---|---|---|
| Web/server code | Example: redeploy previous version `x.y.z` | ______ | ______ | ______ |
| Feature (flag) | Example: turn off flag in dashboard | ______ | ______ | ______ |
| Mobile app | Example: **halt** staged rollout; ship fixed build; turn off flags. (You cannot force-remove an app from customers' phones.) | ______ | ______ | ______ |
| Database / data | Example: restore from backup; reverse migration script | ______ | ______ | ______ |

**Q9.4 – What numbers trigger a rollback or a pause? ("tripwires")**
- Why we ask: decide the numbers now, so nobody argues at 2 a.m.
- If unsure: use the starter values.

| Signal | Pause rollout if… (starter) | Roll back if… (starter) | Your values |
|---|---|---|---|
| Crash-free users | below 99.5% | below 99.0% | ______ |
| Server/web error rate | 1.5× normal | 3× normal or above 5% | ______ |
| Speed (95th percentile) | 20% slower than before | 50% slower | ______ |
| Urgent support tickets | 2× normal | 5× normal | ______ |
| Any Critical (Sev 1) bug | **Pause immediately** | Roll back or flag off | ______ |
| Payments/data wrong | **Pause immediately** | Roll back | ______ |

**Q9.5 – Is a backup taken before release, and who checked a restore works?**
- Example: "Full database backup at T-1 hour; restore test done on 2027-02-10 by Sam."
- If unsure: do not release until this is answered.
- ✍️ Your answer: ______

**Q9.6 – Database or data changes: are they safe? (answer only if Q2.3 = Yes)**
- If unsure: use the "expand, then contract" way: add the new thing first, switch over, remove the old thing in a later release.
- ✍️ Your answer:
  - [ ] Change works with **both** old and new app versions at the same time
  - [ ] Can be reversed
  - [ ] Tested on a copy of real-sized data
  - [ ] Backup taken

---

# PART 10 – GO / NO-GO MEETING (THE BIG GATE)

*Rule: **every row must be GO.** If any row is NO-GO, the release does not ship. The checklist is a gate, not a suggestion.*

**Q10.1 – When is the Go/No-Go meeting, and who must attend?**
- Example: "T-2 working days, 30 minutes. All people in Q3.1 must attend or send their backup."
- If unsure: use the example.
- ✍️ Your answer: Date/time ______ Attendees ______

**Q10.2 – Fill the checklist. Evidence = a link, screenshot, or test result. No evidence = NO-GO.**

| # | Check | Owner | Evidence (link) | GO / NO-GO |
|---|---|---|---|---|
| 1 | Scope matches Part 2 (nothing sneaked in) | Product Owner | ______ | ______ |
| 2 | All code reviewed and merged by humans (Part 5) | Tech Lead | ______ | ______ |
| 3 | All automatic checks pass on the release candidate | Engineer | ______ | ______ |
| 4 | Testing in Part 6B passed; no open Critical/High bugs | QA Lead | ______ | ______ |
| 5 | Security checks in Part 6C passed; SBOM and signatures saved | Security Owner | ______ | ______ |
| 6 | Release candidate frozen and fingerprint recorded | Release Manager | ______ | ______ |
| 7 | Mobile: store review approved; phased/staged rollout set | Release Manager | ______ | ______ |
| 8 | Rollback plan written **and tested** (Q9.3) | Tech Lead | ______ | ______ |
| 9 | Backup taken; restore tested (Q9.5) | Engineer | ______ | ______ |
| 10 | Monitoring dashboards and alerts ready (Part 12) | On-call | ______ | ______ |
| 11 | On-call person named and available for launch + 48 hours | Release Manager | ______ | ______ |
| 12 | Support team trained; help articles and replies ready | Support Lead | ______ | ______ |
| 13 | Release notes approved by a human | Comms Owner | ______ | ______ |
| 14 | Legal items done (privacy, terms, store rules) – Part 14 | Product Owner | ______ | ______ |
| 15 | Stakeholders told the release window (Part 13) | Release Manager | ______ | ______ |
| 16 | No holiday/blackout conflict (Q3.3) | Release Manager | ______ | ______ |
| 17 | Every AI-assisted change was human-checked (Q4.3) | Tech Lead | ______ | ______ |
| 18 | Every question in this document is answered (no blanks/TBD) | Document owner | ______ | ______ |

**Q10.3 – DECISION (a human fills this in)**
- ✍️ Your answer: ☐ GO  ☐ NO-GO  ☐ GO with conditions → conditions: ______
- Decided by (name): ______ Date/time: ______
- If NO-GO: what must be fixed, by whom, by when, and new meeting date: ______

---

# PART 11 – STAGED ROLLOUT: FROM A FEW PEOPLE TO 100%

*Goal: show the release to a small group first. If something is wrong, only a few people are hurt. Increase slowly only when numbers look healthy.*

**Q11.1 – Fill in your rollout stages.**
- Why we ask: "staged" or "phased" rollouts are offered by Google Play (you pick the percentages) and Apple App Store (a fixed 7-day schedule: about 1% → 2% → 5% → 10% → 20% → 50% → 100%, which can be paused for up to 30 days). Web and backend you control yourself with feature flags.
- If unsure: use the starter table, then change dates.

| Stage | Who sees it | Starter size | Minimum time before next step | Go to next stage only if… | Planned date | Actual date | Result |
|---|---|---|---|---|---|---|---|
| **S0 – Team only** | Our own people | ~5–20 | 1–2 days | No Sev 1/2 bugs found | ______ | ______ | ⬜ |
| **S1 – Beta / friends** | Invited testers (TestFlight, Google internal/closed test, or beta list) | 20–100 | 3–7 days | Tripwires (Q9.4) not hit; feedback reviewed | ______ | ______ | ⬜ |
| **S2 – Tiny public slice** | First public users | 1% | 24 hours | Healthy numbers | ______ | ______ | ⬜ |
| **S3 – Small slice** | Public | 5–10% | 24–48 hours | Healthy numbers | ______ | ______ | ⬜ |
| **S4 – Half** | Public | 25–50% | 48 hours | Healthy numbers | ______ | ______ | ⬜ |
| **S5 – Everyone** | Public | 100% | – | Healthy for 7 days | ______ | ______ | ⬜ |

**Q11.2 – Who decides to move to the next stage, and how do they decide?**
- Example: "Release Manager checks the dashboard at each step; Final Approver says OK in the release chat. Both names are written in the log (Part 18)."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q11.3 – What exactly do we look at before each step up? (tick all that apply)**
- ✍️ Your answer:
  - [ ] Crash-free users, error rate, speed (Q9.4)
  - [ ] New sign-ups and sign-up completion rate
  - [ ] Support tickets and app store reviews
  - [ ] Business numbers (payments, sign-ups, main task completed)
  - [ ] Logs show nothing new or scary
  - [ ] Other: ______

**Q11.4 – Are there regions, devices, or customer types we exclude at first?**
- Example: "Start in one country; exclude Android 9 and below."
- If unsure: write `None.`
- ✍️ Your answer: ______

---

# PART 12 – LAUNCH DAY AND MONITORING

## 12A – The launch-day plan (clock times)

**Q12A.1 – Write the launch day schedule.**
- If unsure: use this starter, replacing times with real ones.

| When | What happens | Who | Done |
|---|---|---|---|
| T-7 days | Announce launch window to team & partners | Comms Owner | ⬜ |
| T-2 days | Go/No-Go meeting (Part 10) | Release Manager | ⬜ |
| T-1 day | Final backup; dashboards open; support briefed | On-call, Support | ⬜ |
| T-1 hour | Confirm on-call ready; last check of tripwires | Release Manager | ⬜ |
| **T-0** | **Start rollout (Stage S2)** | Release Manager | ⬜ |
| T+30 min | First health check: crashes, errors, speed, sign-ups | On-call | ⬜ |
| T+2 hours | Second health check; post status in team chat | On-call | ⬜ |
| T+24 hours | Review all numbers; decide next stage | Release Manager | ⬜ |
| T+48 hours | End of intensive watch; short written summary | Release Manager | ⬜ |

## 12B – Monitoring

**Q12B.1 – Where do we look, and how do we get alerted?**
- Why we ask: "A deploy that works can still be a bad release." Watch what customers feel, not only whether servers are up.
- If unsure: fill all rows.

| What we watch | Tool/dashboard link | Alert goes to (name/chat) | Alert when… |
|---|---|---|---|
| App crashes (mobile) | ______ | ______ | Below Q9.4 values |
| Server errors & speed | ______ | ______ | Above Q9.4 values |
| Uptime (is it up?) | ______ | ______ | Down > 1 minute |
| Sign-ups & key actions | ______ | ______ | Drop of 30% vs. expected |
| Payments (if any) | ______ | ______ | Any failure spike |
| Customer support inbox | ______ | ______ | Ticket spike |
| App store reviews | ______ | ______ | Rating drop |
| Security alerts | ______ | ______ | Any |
| Cost (cloud bill) | ______ | ______ | 2× expected |

**Q12B.2 – Who is on-call, and for how long?**
- Example: "On-call engineer is awake and reachable from T-1 hour to T+48 hours. Backup: Alex."
- If unsure: use the example.
- ✍️ Your answer: ______

---

# PART 13 – COMMUNICATION PLAN

**Q13.1 – Who needs to hear what, and when?**
- Why we ask: nobody should hear bad news from a customer first.
- If unsure: use the starter.

| Who | What they need to know | When | Channel | Owner |
|---|---|---|---|---|
| Team | Release window, roles, rules | T-7 days | Chat/email | Release Manager |
| Leaders/partners | Date, goals, risks | T-7 and T+1 days | Email | Product Owner |
| Support team | New features, known issues, reply templates | T-2 days | Meeting + doc | Support Lead |
| Customers | What is new | Launch day | Release notes / in-app / email | Comms Owner |
| Customers (if problem) | What happened, what we are doing | Within 1 hour of confirming | Status page / email / in-app | Comms Owner |

**Q13.2 – Do we have a public "status page" or a place to tell customers about problems?**
- Example: "Status page at `<link>`; in-app banner for mobile."
- If unsure: write `Not yet – ______ will create by ______.`
- ✍️ Your answer: ______

**Q13.3 – Draft the "something went wrong" message now (fill the blanks later).**
- Example: "We found a problem with ___ that affects ___. We have ___. Next update at ___."
- ✍️ Your answer: ______

---

# PART 14 – LEGAL, PRIVACY, AND STORE RULES

*Not legal advice. Ask a qualified person if unsure.*

**Q14.1 – What personal information do we collect? (tick all)**
- ✍️ Your answer:
  - [ ] Name / email / phone
  - [ ] Location
  - [ ] Photos / files
  - [ ] Payment info (handled by a payment provider)
  - [ ] Usage data / analytics
  - [ ] Children's data (under 13 or under 16 in some regions) → **extra rules apply; ask a legal expert**
  - [ ] Health or other sensitive data → **extra rules apply**
  - [ ] None

**Q14.2 – Which rules apply to us? (tick all that apply; unsure = tick and ask)**
- ✍️ Your answer:
  - [ ] GDPR (people in the EU/UK)
  - [ ] CCPA/CPRA (California)
  - [ ] COPPA (children in the US)
  - [ ] Apple App Store rules (including account-deletion and privacy-label requirements)
  - [ ] Google Play rules (including Data safety form)
  - [ ] Payment card rules (PCI DSS) if you handle cards
  - [ ] Accessibility laws/standards (WCAG)
  - [ ] Industry rules (health, finance, education): ______
  - [ ] Other: ______

**Q14.3 – Are these done?**
- ✍️ Your answer:
  - [ ] Privacy policy published and linked in the app and store
  - [ ] Terms of service published
  - [ ] Cookie/consent banner (web) if needed
  - [ ] Customers can delete their account and data
  - [ ] Process to answer data requests (who, how fast): ______
  - [ ] Open-source library licenses checked
  - [ ] Legal/privacy review by: ______ on ______

---

# PART 15 – THE FIRST 500 CUSTOMERS PLAN

*Goal: grow carefully, learn fast, and protect early customers. Each cohort teaches you something before you open the door wider.*

**Q15.1 – How do customers arrive? (pick all that apply)**
- Example: "Invite list → waitlist → public sign-up."
- If unsure: use the example.
- ✍️ Your answer:
  - [ ] Invite only
  - [ ] Waitlist (let in a few at a time)
  - [ ] Open to everyone
  - [ ] Paid ads or marketing push (date: ______)
  - [ ] Partner/community launch (who: ______)

**Q15.2 – Fill the customer growth plan.**
- Why we ask: the first 10, 50, and 150 customers find different problems.
- If unsure: use the starter.

| Cohort | Customers (running total) | What we want to learn | How we talk to them | Do not grow past here until… | Target date | Actual date |
|---|---|---|---|---|---|---|
| **A – First 10** | 1–10 | Can they sign up and do the main thing without help? | Personal calls/messages | No one is blocked on the main task | ______ | ______ |
| **B – First 50** | 11–50 | What confuses people? What breaks? | Short survey + personal follow-ups | Top 5 problems fixed or planned | ______ | ______ |
| **C – First 150** | 51–150 | Do they come back after 7 days? | Survey + analytics | 7-day return rate ≥ Q1.4 target | ______ | ______ |
| **D – First 500** | 151–500 | Does it hold up at size? Is support manageable? | Survey + reviews + support data | Q1.4 targets met for 14 days | ______ | ______ |

**Q15.3 – How do we collect feedback?**
- Example: "In-app 'Send feedback' button, 3-question survey after day 3, a support email, store reviews checked daily."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q15.4 – How fast do we answer customers?**
- Example: "First reply within 4 working hours; urgent problems (can't log in, lost data, wrong charge) within 1 hour."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q15.5 – How often do we ship fixes during the first 500?**
- Example: "Fix releases (patch) any day if urgent; planned updates every 2 weeks, each using Part 11."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q15.6 – What do we do if we get more sign-ups than we can handle?**
- Example: "Pause invites, turn on waitlist, add a banner, and tell Support."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q15.7 – What is the "we hit 500" moment, and what happens next?**
- Example: "Hold a review meeting within 3 days; write the summary in Part 17; decide to grow, fix, or pause."
- If unsure: use the example.
- ✍️ Your answer: ______

---

# PART 16 – WHEN THINGS GO WRONG (HOTFIX AND INCIDENT PLAN)

**Q16.1 – How do we decide how serious a live problem is?**
- If unsure: use this scale.

| Level | Meaning | Response time (starter) | Who is woken up |
|---|---|---|---|
| **Sev 1** | Data loss, security breach, app down for many, money wrong | Start within 15 min | On-call + Tech Lead + Release Manager + Product Owner |
| **Sev 2** | Main feature broken for many | Start within 1 hour | On-call + Tech Lead |
| **Sev 3** | Problem with a workaround | Next working day | On-call |
| **Sev 4** | Cosmetic | Normal planning | Product Owner |

**Q16.2 – What are the steps when a live problem happens?**
- Starter (replace names/links):
  1. **Stop the spread** – pause rollout (Apple/Google) and/or turn off the feature flag.
  2. **Tell people** – post in the team chat; tell Support; update the status page (Q13.2).
  3. **Decide** – roll back, flag off, or hotfix? (Release Manager + Tech Lead).
  4. **Fix and test** – small fix only, reviewed by a human.
  5. **Re-release carefully** – use Part 11 again (small stage first).
  6. **Tell customers** – use message in Q13.3.
  7. **Write it down** – log in Part 18; hold a "what did we learn" meeting within 5 working days.
- ✍️ Your changes: ______

**Q16.3 – Hotfix rules: how is an urgent fix different?**
- Example: "Branch `hotfix/*` from the released version; 1 reviewer minimum; Sev 1 can ship after tests pass and Tech Lead approves; always staged for mobile unless Sev 1 security (then 100% with Final Approver sign-off)."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q16.4 – Security problems: who do we call, and who may talk to the public?**
- Example: "Security Owner leads; Product Owner approves public statements; legal contacted within 24 hours if customer data may be affected."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q16.5 – Which customer-facing contact will we publish for reporting security issues?**
- Example: "security@yourcompany.com"
- ✍️ Your answer: ______

---

# PART 17 – AFTER THE RELEASE: LEARN AND IMPROVE

**Q17.1 – When do we review how it went?**
- Example: "T+7 days after 100% rollout, and again after the 500th customer."
- If unsure: use the example.
- ✍️ Your answer: ______

**Q17.2 – Release health numbers (fill after each release)**
- Why we ask: these four numbers (from the DORA research program) describe speed and stability together. A fifth one, "rework," shows how many unplanned fixes you needed.

| Measure | Plain meaning | Starter goal | This release | Last release |
|---|---|---|---|---|
| Deployment frequency | How often we ship | At least every 2 weeks | ______ | ______ |
| Lead time for changes | Time from "code finished" to "customers have it" | Under 7 days | ______ | ______ |
| Change failure rate | Share of releases that caused a problem needing a fix | Under 15% | ______ | ______ |
| Time to recover | How long to fix a failed release | Under 1 hour (web), under 24 hours (mobile) | ______ | ______ |
| Rework rate | Unplanned fix releases ÷ all releases | Under 15% | ______ | ______ |
| Rollbacks / pauses | How many times we backed out | 0 | ______ | ______ |
| Post-release incidents (48 h) | Problems after launch | 0 Sev 1/2 | ______ | ______ |

**Q17.3 – "What did we learn?" (no blame; focus on fixing the system)**
- Example format: "What went well? What went badly? What surprised us? What will we change? Who does it by when?"
- ✍️ Your answer:
  - Went well: ______
  - Went badly: ______
  - Surprised us: ______
  - Actions (what / who / by when): ______

**Q17.4 – What do we update in this template or our process because of what we learned?**
- ✍️ Your answer: ______

**Q17.5 – Clean-up after launch**
- ✍️ Your answer:
  - [ ] Old feature flags removed (dates in Q7.5)
  - [ ] Old test accounts/data removed
  - [ ] Temporary alerts or access removed
  - [ ] Documentation updated
  - [ ] Release files and evidence archived (Q6C.3)

---

# PART 18 – RELEASE LOG (WRITE AS YOU GO)

*Copy a row each time something happens. This is your single truth of "what actually happened."*

| Date/time | Version | Stage | What happened | Decision | Decided by | Numbers at the time |
|---|---|---|---|---|---|---|
| ______ | ______ | ______ | ______ | ______ | ______ | ______ |
| ______ | ______ | ______ | ______ | ______ | ______ | ______ |

---

# PART 19 – SIGN-OFF (HUMANS ONLY)

*Each person signs by typing their name and date. AI agents may not sign.*

| Role | Name | Decision (Approve / Reject) | Date | Notes |
|---|---|---|---|---|
| Product Owner | ______ | ______ | ______ | ______ |
| Tech Lead | ______ | ______ | ______ | ______ |
| QA Lead | ______ | ______ | ______ | ______ |
| Security Owner | ______ | ______ | ______ | ______ |
| Support Lead | ______ | ______ | ______ | ______ |
| Final Approver | ______ | ______ | ______ | ______ |

---

# APPENDIX A – COMPLETED EXAMPLE (SHORT)

*A tiny made-up project so you can see the style. Do not copy the numbers.*

**Product:** LeafPal – phone app that reminds people to water plants.

- **Q0.1:** A phone app that tells you when to water each plant.
- **Q1.3:** A customer is someone who creates an account and adds at least one plant.
- **Q3.1 Release Manager:** Priya Shah (backup: Marco Diaz, phone +1-555-0100).
- **Q4.1:** Coding agent may write code and tests and comment on reviews. It may not merge or deploy.
- **Q5.3:** 1 human reviewer; all tests pass; no direct pushes to `main`.
- **Q8.1:** Version `1.0.0`; iOS build 12; Android versionCode 12.
- **Q9.4:** Pause if crash-free users below 99.5%. Roll back if below 99.0%.
- **Q11.1:** S0 team (10 people, 2 days) → S1 beta (60 people, 5 days) → 1% (24 h) → 10% (48 h) → 50% (48 h) → 100%.
- **Q15.2:** Cohort A: 10 friends, personal calls. Cohort B: next 40 via waitlist. Cohort C: reach 150 before marketing. Cohort D: reach 500 with Q1.4 targets met for 14 days.
- **Q10.3:** GO, decided by Final Approver Jamie Lee on 2027-02-12 at 15:00.

---

# APPENDIX B – EXTRA QUESTIONS FOR AI-POWERED PRODUCTS

*Fill only if you ticked "Uses AI/LLM features inside the product" in Q0.3.*

**QB.1 – Which AI model(s) power the product, and which exact version?**
- Why we ask: model updates can change behavior without any code change.
- ✍️ Your answer: ______

**QB.2 – How do we test AI answers before each release?**
- Example: "A fixed set of 100 test questions with expected good answers; release only if ≥ 95% pass and no harmful answers."
- ✍️ Your answer: ______

**QB.3 – What happens when the AI is wrong, slow, or down?**
- Example: "Show a friendly message and fallback to a simple answer; alert on-call if failures exceed 2%."
- ✍️ Your answer: ______

**QB.4 – What safety limits exist?**
- ✍️ Your answer: ______

**QB.5 – How do we change prompts or model versions safely? (treat like code)**
- Example: "Prompts live in the code repository, reviewed by a human, tested with QB.2, rolled out behind a flag."
- ✍️ Your answer: ______

**QB.6 – What customer data goes to the AI provider, and is it allowed (Part 14)?**
- ✍️ Your answer: ______

**QB.7 – How do we watch cost and misuse?**
- Example: "Daily cost report; alert at 2× expected; rate limit per user."
- ✍️ Your answer: ______

---

# APPENDIX C – FINAL "IS THIS DOCUMENT READY?" CHECK

Tick every box before the Go/No-Go meeting.

- [ ] No question is blank, and none says only "TBD"
- [ ] Every person named in Part 3 knows they are named
- [ ] Every number has a unit (%, seconds, hours, customers)
- [ ] Every date is in `YYYY-MM-DD` format
- [ ] Rollback was practiced, not just written (Q9.3)
- [ ] Tripwire numbers are agreed (Q9.4)
- [ ] The Go/No-Go checklist (Part 10) has evidence links
- [ ] A human, not an AI, filled in every approval and signature
- [ ] No passwords, keys, or customer data are written in this file
- [ ] Someone who did **not** write this file read it and could explain the plan back to you

---

# APPENDIX D – PLAIN-WORDS GLOSSARY

| Word | Simple meaning |
|---|---|
| **Release** | Giving a new version of the product to customers |
| **Deploy** | Putting the code on the servers or in the store (not always the same moment customers see it) |
| **Release candidate (RC)** | The exact version we plan to ship |
| **Staged / phased rollout** | Giving the new version to a few people first, then more |
| **Feature flag** | An on/off switch for a feature without a new release |
| **Rollback** | Going back to the last good version |
| **Hotfix** | A small, urgent fix |
| **Go/No-Go** | The meeting where a named human says "ship" or "stop" |
| **Tripwire** | A number that, if crossed, makes us pause or roll back |
| **CI/CD** | Automatic building, testing, and delivering of code |
| **Pull request / change request** | A proposal to add code, which others review |
| **Branch** | A separate lane of code work |
| **Staging** | A practice copy of the live product |
| **SBOM** | A list of every ingredient (library) inside the software |
| **Provenance** | Proof of who built the software, from what, and when |
| **On-call** | The person who must answer if something breaks |
| **Sev (severity)** | How bad a problem is |
| **DORA metrics** | Widely used numbers for delivery speed and stability |
| **Semantic Versioning** | Version numbers like 1.4.2 where each part has a meaning |

---

# APPENDIX E – WHERE THIS TEMPLATE'S IDEAS COME FROM

- DORA software delivery metrics (deployment frequency, lead time, change failure rate, recovery time, rework) – used in Part 17.
- Semantic Versioning (semver.org) – used in Part 8.
- Keep a Changelog style for release notes (Added / Changed / Fixed / Removed) – used in Q8.4.
- NIST Secure Software Development Framework (SP 800-218), practices PS.2 and PS.3 on release integrity, archiving, and provenance/SBOM – used in Part 6C.
- SLSA (Supply-chain Levels for Software Artifacts) for build provenance – used in Part 6C.
- Apple App Store "Phased Release" and Google Play "Staged rollout" documentation – used in Parts 7 and 11. **Check the stores' current rules before each launch; they change.**
- Go/No-Go checklists, rollback tripwires, and communication timelines (T-7 / T-1 / T-0 / T+1) common in release-management guidance – used in Parts 9, 10, 12, 13.

*End of template. Save a **copy** per project, rename it (e.g., `Release_Management_LeafPal_v1.0.0.md`), and fill in the copy. Keep this original clean.*
