# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What is this?** A Release Notes document tells everyone, in one place, *what changed, why it is safe, how it is being launched, and what happens if something goes wrong*. One file = one release. It covers the full AI-Driven Development Life Cycle (AI-DLC): from building the release, through review and testing, to launch and growth up to your **first 500 customers**.

**Who reads it?** Four audiences. Write so all four can use it:
| Reader | Looks at |
|---|---|
| Customers / end users | Section 3 (What's New), Section 13 (Help docs), Section 18 (Known Issues), Section 19 (How to Upgrade) |
| Internal team (engineers, QA, support, PM) | Sections 4 to 20 |
| Leadership / investors | Section 2 (Summary), Section 11 (Cost), Section 14 (Marketing), Section 15 (Metrics), Section 16 (Rollout) |
| AI agents | Section 23 (Machine-Readable Summary) and the `▶ Answer:` lines |

### The 7 Golden Rules
1. **Answer every question.** Never delete a question. Never leave a blank.
2. **Don't know yet?** Write `TBD – @owner – by YYYY-MM-DD`. A blank is not allowed; TBD with an owner and date is.
3. **Doesn't apply?** Write `N/A – because <one reason>`.
4. **Use real facts, not feelings.** Write "42 of 42 tests passed", not "testing went well".
5. **Use links.** Every claim should link to proof (pull request, test report, dashboard, ticket).
6. **Use plain words.** If a 10-year-old can't understand a sentence in Sections 2 and 3, rewrite it.
7. **Dates look like this:** `2026-10-18` (year-month-day). **Times** include a time zone: `14:30 UTC`.

### The 4 HARD GATES (no exceptions: if any gate fails, the answer is NO-GO)
| # | Gate | Where to prove it | Pass rule |
|---|---|---|---|
| 1 | **Zero critical bugs and zero critical security issues** | Section 8 (Q8.4) and Section 9 (Q9.2) | Both counts are exactly 0 |
| 2 | **Rollback was practiced** (really tried, not just written down) | Section 17 (Q17.3) and Section 8 (Q8.1) | A date and a proof link are filled in |
| 3 | **A named human approved all AI work** (code, tests, agent actions, AI features) | Section 6 (Q6.8) and Section 21 | A real person's name and date; "the AI checked it" does not count |
| 4 | **Privacy and data-consent check passed** | Section 9 (Q9.3 to Q9.5) and Section 10 | Consent, privacy policy, and delete-my-data are confirmed, or you prove no personal data is touched |

*A hard gate cannot be skipped, waived with "TBD", or marked "N/A" unless you can prove it truly does not apply (example: the product collects no personal data at all).*

### How each question looks
> **Q1.1 – The question in plain words**
> *Why we ask:* the reason, so you are never guessing.
> *Example of a good answer:* a short sample.
> *If unsure:* what to do.
> ▶ **Answer:** `type here`

Replace only what is between the backticks (or tick the box: change `[ ]` to `[x]`).

### Fill-in order (recommended)
1. Fill **Sections 1 and 5** at the start of the release work.
2. Update **Sections 6 to 10** while building, reviewing, and testing.
3. Start **Sections 11 to 14** (cost, accessibility, documentation, marketing) as soon as the plan is known, and finish them before launch.
4. Fill **Sections 15 to 19** before launch.
5. Update **Sections 16, 17, 20** during rollout until you reach 500 customers.
6. Finish with **Section 21 (Sign-offs)**, **Section 22 (Final Checklist)**, and **Section 23 (Machine-Readable Summary)**.

### File naming and location
- Save as `Release_Notes_vX.Y.Z.md` (example: `Release_Notes_v1.2.0.md`) in the **Code Review and Release Engineering** folder of the project.
- Keep this blank template as `Release_Notes.md`. **Copy it; never fill in the original.**

### Document status (update as you go)
▶ **Status:** `[ ] Draft   [ ] In Review   [ ] Approved   [ ] Released   [ ] Rolled Back   [ ] Closed (500 customers reached)`

---

# SECTION 1 – RELEASE IDENTITY ("Who is this release?")

**Q1.1 – What is the project / product name?**
*Why we ask:* So nobody mixes this release up with another project.
*Example:* `PlantPal`
▶ **Answer:** ``

**Q1.2 – What is the version number?** (Use SemVer: `MAJOR.MINOR.PATCH`)
*Why we ask:* The number tells people how big the change is.
*Pick the number with this mini-quiz:*
- Did you change something that **breaks** old usage (old data, old API calls, old settings stop working)? → raise **MAJOR** (1.4.2 → **2**.0.0)
- Did you **add** a new feature that does not break anything old? → raise **MINOR** (1.4.2 → 1.**5**.0)
- Did you only **fix bugs** or make tiny safe tweaks? → raise **PATCH** (1.4.2 → 1.4.**3**)
- Is it a first test version? Use `0.x.x`, or add a tag such as `-beta.1` or `-rc.1`.

*Example:* `1.2.0`
▶ **Answer:** ``

**Q1.3 – What was the previous version?**
*If unsure:* Check your Git tags or last release notes. First release? Write `None (first release)`.
▶ **Answer:** ``

**Q1.4 – Release type?**
▶ **Answer:** `[ ] Major   [ ] Minor   [ ] Patch   [ ] Hotfix (urgent fix)   [ ] Pre-release (alpha/beta/rc)`

**Q1.5 – Release dates**
| Event | Date and time (with time zone) |
|---|---|
| Code freeze (no more new changes) | `` |
| Planned release date | `` |
| Actual release date | `` |

**Q1.6 – Who is responsible?**
| Role | Name | Contact |
|---|---|---|
| Release Owner (one person who answers "is it ready?") | `` | `` |
| Product Owner | `` | `` |
| Engineering Lead | `` | `` |
| QA Lead | `` | `` |
| On-call person during launch | `` | `` |

**Q1.7 – Where is the proof?** (links)
| Item | Link |
|---|---|
| Source code tag / commit | `` |
| Full change list (compare view) | `` |
| Project board / ticket list | `` |
| Build / CI pipeline run | `` |
| Dashboard | `` |

---

# SECTION 2 – SUMMARY ("The 30-second version")

*Write this LAST, but put it here. Leaders and customers often read only this section.*

**Q2.1 – In 2 to 3 simple sentences, what is this release and why does it matter?**
*Example:* `PlantPal 1.2.0 lets users scan a plant with their phone camera and learn how often to water it. This was our most-requested feature. It also fixes the crash that happened when opening the app without internet.`
▶ **Answer:** ``

**Q2.2 – What are the top 3 changes?**
1. `` 
2. `` 
3. `` 

**Q2.3 – How risky is this release?**
▶ **Answer:** `[ ] Low   [ ] Medium   [ ] High`
**In one sentence, why?** `` 

**Q2.4 – Does it require customers to do anything?**
▶ **Answer:** `[ ] No action needed   [ ] Yes, action needed (explain in Section 19)`

**Q2.5 – Final decision** *(Cannot be GO unless all 4 Hard Gates pass. See the Hard Gates table at the top and Section 22.)*
▶ **Answer:** `[ ] GO (ready to launch)   [ ] NO-GO (not ready)   [ ] GO with conditions: ____`

---

# SECTION 3 – WHAT'S NEW (customer-friendly)

*Write for someone who has never seen the code. No jargon. Start each line with a verb. Describe the benefit, not the code.*

**Q3.1 – New features** (things users could not do before)
*Example:* `- Scan a plant with your camera to get watering tips. [#128]`
| Feature | Benefit to the user | Ticket link |
|---|---|---|
| `` | `` | `` |

**Q3.2 – Improvements** (things that already existed but are now better)
| Improvement | Benefit to the user | Ticket link |
|---|---|---|
| `` | `` | `` |

**Q3.3 – Bug fixes**
| What was broken | What happens now | Ticket link |
|---|---|---|
| `` | `` | `` |

**Q3.4 – Things being removed or phased out (deprecations)**
*Why we ask:* Users hate surprises.
| What is going away | Last day it works | What to use instead |
|---|---|---|
| `` | `` | `` |

**Q3.5 – Breaking changes** (things that stop working the old way)
*If none, write `None`.*
▶ **Answer:** ``

**Q3.6 – Anything we deliberately did NOT include this time?** (so people stop asking)
▶ **Answer:** ``

---

# SECTION 4 – TECHNICAL CHANGES (for the internal team)

**Q4.1 – Which parts of the system changed?**
▶ **Answer:** `[ ] Frontend   [ ] Backend   [ ] Database   [ ] APIs   [ ] Infrastructure / Cloud   [ ] Mobile app   [ ] AI models / prompts   [ ] Documentation only   [ ] Other: ____`

**Q4.2 – List the main pull requests / merges**
| PR / Commit link | One-line description | Author (human or AI agent) | Risk (L/M/H) |
|---|---|---|---|
| `` | `` | `` | `` |

**Q4.3 – Database or data changes?**
*Why we ask:* Data changes are the hardest to undo.
▶ **Answer:** `[ ] None   [ ] Yes → Migration name/link: ____   Reversible? [ ] Yes [ ] No   Backup taken? [ ] Yes [ ] No`

**Q4.4 – API changes?**
▶ **Answer:** `[ ] None   [ ] Added: ____   [ ] Changed: ____   [ ] Removed: ____   API docs link: ____`

**Q4.5 – New or changed settings, environment variables, or secrets?**
*Never write the secret value here. Write only the NAME.*
▶ **Answer:** ``

**Q4.6 – Dependencies added, updated, or removed?**
| Package / service | Old version | New version | Why |
|---|---|---|---|
| `` | `` | `` | `` |

**Q4.7 – Performance impact?** (faster / slower / same, with numbers)
*Example:* `Page load went from 2.4s to 1.1s (measured on staging, link).`
▶ **Answer:** ``

**Q4.8 – Infrastructure or cost changes?**
▶ **Answer:** ``

---

# SECTION 5 – AI-DLC PHASE TRACKER ("Where are we in the journey?")

*Why we ask:* This release moves through phases from idea to your first 500 customers. Tick each phase when it is truly done and add proof.

| # | Phase | Done? | Date | Proof (link) |
|---|---|---|---|---|
| 1 | **Plan** – goals, requirements, and "definition of done" written | `[ ]` | `` | `` |
| 2 | **Build** – code written (by humans and/or AI agents) | `[ ]` | `` | `` |
| 3 | **Code Review** – human reviewed all changes (Section 7) | `[ ]` | `` | `` |
| 4 | **Test** – QA test summary complete (Section 8) | `[ ]` | `` | `` |
| 5 | **Security and Legal check** (Sections 9 and 10) | `[ ]` | `` | `` |
| 6 | **Staging rehearsal** – launch practiced in a safe copy | `[ ]` | `` | `` |
| 7 | **Launch** – first real users get it (Section 16) | `[ ]` | `` | `` |
| 8 | **Scale to 50 customers** | `[ ]` | `` | `` |
| 9 | **Scale to 100 customers** | `[ ]` | `` | `` |
| 10 | **Scale to 250 customers** | `[ ]` | `` | `` |
| 11 | **Reach 500 customers** and run the retrospective (Section 20) | `[ ]` | `` | `` |

**Q5.1 – What is the single goal of this release?** (one sentence a child could repeat)
▶ **Answer:** ``

**Q5.2 – What does "done" look like?** (how will you know it worked?)
*Example:* `500 people have signed up, at least 60% use it twice in a week, and fewer than 5 serious bugs are reported.`
▶ **Answer:** ``

---

# SECTION 6 – AI INVOLVEMENT DISCLOSURE ("What did AI do, and who checked it?")

*Why we ask:* Trust. Anyone reading should know exactly which work was done by AI and that a human checked it.

### 6A. AI-written code

**Q6.1 – Was AI used to write code in this release?**
▶ **Answer:** `[ ] No   [ ] Yes, a little (<25%)   [ ] Yes, a lot (25 to 75%)   [ ] Yes, most (>75%)`
*If unsure:* Estimate from commit history or tool reports, and write "estimated".

**Q6.2 – Which parts were AI-generated?**
| Module / file / area | AI tool or agent used | Human who reviewed it | Reviewed? |
|---|---|---|---|
| `` | `` | `` | `[ ]` |

**Q6.3 – Was any AI-generated code copied from a public source or does it resemble known open-source code?**
▶ **Answer:** `[ ] No   [ ] Yes → license check done? [ ] Yes [ ] No   Details: ____   [ ] Not checked yet (TBD)`

### 6B. Models and agents used in each phase

**Q6.4 – Which AI models and agents were used?**
| Phase | Model / agent name and version | What it did | Prompts / config link |
|---|---|---|---|
| Plan | `` | `` | `` |
| Build | `` | `` | `` |
| Review | `` | `` | `` |
| Test | `` | `` | `` |
| Docs / release notes | `` | `` | `` |

**Q6.5 – Did an AI agent take any action on its own (deploy, merge, change data)?**
▶ **Answer:** `[ ] No   [ ] Yes → What: ____   Who approved: ____   Limits/permissions it had: ____`

### 6C. AI review and test results

**Q6.6 – Did AI review the code?** What did it find?
| AI reviewer | Issues found | Issues fixed | Issues accepted (and why) |
|---|---|---|---|
| `` | `` | `` | `` |

**Q6.7 – Were tests written or run by AI?**
▶ **Answer:** `[ ] No   [ ] Yes → How many tests: ____   Human checked they test the right things: [ ] Yes [ ] No`

**Q6.8 – Human sign-off on AI work**
*Rule: AI work is never final until a named human approves it.* **(HARD GATE 3)**
▶ **Answer:** `Approved by: ____   Date: ____`

### 6D. AI features inside the product (skip if the product has no AI features)

**Q6.9 – Does the product itself use AI (chatbot, recommendations, image recognition, etc.)?**
▶ **Answer:** `[ ] No (skip 6D)   [ ] Yes`

**Q6.10 – What can the AI feature do, and what can it NOT do?**
*Example:* `Can identify 3,000 common houseplants. Cannot identify diseases. May be wrong on rare plants.`
▶ **Answer:** ``

**Q6.11 – What are the known risks (wrong answers, bias, unsafe output, leaking private data)?**
| Risk | How likely (L/M/H) | How we reduce it |
|---|---|---|
| `` | `` | `` |

**Q6.12 – How was the AI feature measured (accuracy checks, "evals")?**
| Test name | Score or result | Pass line (minimum) | Pass? |
|---|---|---|---|
| `` | `` | `` | `[ ]` |

**Q6.13 – Does a human or a safety net catch bad AI answers?** (filters, fallback message, report button)
▶ **Answer:** ``

**Q6.14 – Do users know they are talking to AI?** (disclosure label shown?)
▶ **Answer:** `[ ] Yes   [ ] No → why: ____`

---

# SECTION 7 – CODE REVIEW RECORD

**Q7.1 – How many changes (pull requests) are in this release?**
▶ **Answer:** ``

**Q7.2 – Did every change get reviewed by at least one human who did NOT write it?**
▶ **Answer:** `[ ] Yes, all   [ ] No → list exceptions and who approved them: ____`

**Q7.3 – Review summary**
| Item | Count / answer |
|---|---|
| Reviewers involved (names) | `` |
| Comments raised | `` |
| Comments resolved | `` |
| Open comments we chose to accept (explain) | `` |
| Style / lint checks passed? | `[ ] Yes [ ] No` |

**Q7.4 – Was a second, deeper review done on risky areas?** (payments, logins, data deletion, AI actions)
▶ **Answer:** `[ ] N/A   [ ] Yes → areas: ____   reviewer: ____`

**Q7.5 – Branch and merge safety**
▶ **Answer:** `Release branch: ____   Protected branch rules on? [ ] Yes [ ] No   Squash/merge style: ____`

---

# SECTION 8 – QA TEST SUMMARY

**Q8.1 – What kinds of tests were run?**
| Test type | Run? | Total | Passed | Failed | Link to report |
|---|---|---|---|---|---|
| Unit tests | `[ ]` | `` | `` | `` | `` |
| Integration tests | `[ ]` | `` | `` | `` | `` |
| End-to-end / user-flow tests | `[ ]` | `` | `` | `` | `` |
| Performance / load tests | `[ ]` | `` | `` | `` | `` |
| Accessibility checks | `[ ]` | `` | `` | `` | `` |
| Cross-device / cross-browser tests | `[ ]` | `` | `` | `` | `` |
| Manual exploratory testing | `[ ]` | `` | `` | `` | `` |
| Upgrade / migration test | `[ ]` | `` | `` | `` | `` |
| Rollback test (we tried undoing it) | `[ ]` | `` | `` | `` | `` |

**Q8.2 – Code coverage** (the % of code touched by tests)
*If unsure:* write `Not measured`. Don't guess.
▶ **Answer:** ``

**Q8.3 – Can the product handle 500 customers at once?** (load test result)
*Example:* `Simulated 1,000 users: average response 380 ms, 0 errors.`
▶ **Answer:** ``

**Q8.4 – Open bugs at release time**
| Severity | Count | Ticket links | OK to ship? |
|---|---|---|---|
| Critical (data loss, crash, security) | `` | `` | **Must be 0** |
| High | `` | `` | `` |
| Medium | `` | `` | `` |
| Low | `` | `` | `` |

**Q8.5 – QA decision**
▶ **Answer:** `[ ] Pass   [ ] Pass with known issues   [ ] Fail`   **QA Lead:** `` **Date:** ``

---

# SECTION 9 – SECURITY AND PRIVACY CHECKS

**Q9.1 – Security checks done**
| Check | Done? | Result / link |
|---|---|---|
| Dependency vulnerability scan | `[ ]` | `` |
| Secret scan (no passwords/keys in code) | `[ ]` | `` |
| Static code security scan | `[ ]` | `` |
| Login / permission test (can a user see another user's data?) | `[ ]` | `` |
| Penetration test or equivalent | `[ ]` | `` |
| AI-specific checks (prompt injection, data leaks, unsafe output) | `[ ]` | `` |

**Q9.2 – Open security issues**
▶ **Answer:** `Critical: __  High: __  (Critical must be 0: HARD GATE 1)`

**Q9.3 – Does this release collect, store, or share new personal data?** (names, emails, photos, locations, etc.)
▶ **Answer:** `[ ] No   [ ] Yes → what data: ____   why we need it: ____   where stored: ____   how long kept: ____`

**Q9.4 – Is user data sent to any AI provider or third party?**
▶ **Answer:** `[ ] No   [ ] Yes → who: ____   what data: ____   is it used to train their models? [ ] No [ ] Yes [ ] Unknown`

**Q9.5 – Do users have clear consent, a privacy policy, and a way to delete their data?** **(HARD GATE 4)**
▶ **Answer:** `Consent: [ ] Yes [ ] No   Policy updated: [ ] Yes [ ] No [ ] N/A   Delete-my-data works: [ ] Yes [ ] No`

---

# SECTION 10 – LEGAL AND LICENSING

**Q10.1 – New third-party libraries or content, and their licenses**
| Name | License (MIT, Apache, GPL, paid, etc.) | OK for our use? |
|---|---|---|
| `` | `` | `[ ]` |

**Q10.2 – Do we have the right to use all images, fonts, data, and AI-generated content in this release?**
▶ **Answer:** `[ ] Yes   [ ] No → fix: ____   [ ] Needs legal review (TBD)`

**Q10.3 – Did our Terms of Service, Privacy Policy, or pricing change?**
▶ **Answer:** `[ ] No   [ ] Yes → link: ____   Users notified on: ____`

**Q10.4 – Any rules that apply to us?** (e.g., privacy laws, children's data, accessibility, industry rules, AI regulations)
▶ **Answer:** `[ ] None known   [ ] Yes: ____   Compliance check done by: ____`

---

# SECTION 11 – COST AND BUDGET ("What does this release cost?")

*Why we ask:* Every new user costs money (servers, AI usage, support). Knowing the cost before launch prevents nasty surprises at 500 customers.

**Q11.1 – What is the budget for this release?**
| Cost type | Planned (per month) | Actual (per month) | Notes / link to bill |
|---|---|---|---|
| Cloud hosting and storage | `` | `` | `` |
| AI model usage (tokens, API calls, GPUs) | `` | `` | `` |
| Third-party services (email, payments, maps, etc.) | `` | `` | `` |
| Support staff time | `` | `` | `` |
| Marketing and ads | `` | `` | `` |
| Other | `` | `` | `` |
| **Total** | `` | `` | `` |

**Q11.2 – What will it cost per customer when we reach 500?**
*How to calculate:* total monthly cost ÷ number of customers.
*Example:* `$1,200 per month ÷ 500 customers = $2.40 per customer per month.`
▶ **Answer:** ``

**Q11.3 – How much money comes in per customer?** (price, plan, or "free for now")
▶ **Answer:** ``

**Q11.4 – Is there a spending limit with an alarm?** (especially for AI usage, which can grow fast)
*Example:* `AI budget cap $500/month. Alert at 80%. At 100% the AI feature switches to a cheaper model.`
▶ **Answer:** `Cap: ____   Alert at: ____   What happens at the cap: ____`

**Q11.5 – Who can approve extra spending, and how fast can they answer?**
▶ **Answer:** ``

---

# SECTION 12 – ACCESSIBILITY AND LOCALIZATION ("Can everyone use it, everywhere?")

*Why we ask:* People use products with screen readers, keyboards, small screens, and in many languages. If it only works for some people, it is not finished.

**Q12.1 – Accessibility checks** (a common goal is "WCAG 2.2 level AA")
| Check | Done? | Result / link |
|---|---|---|
| Works with a screen reader | `[ ]` | `` |
| Everything works with keyboard only (no mouse) | `[ ]` | `` |
| Text is easy to read (color contrast is strong enough) | `[ ]` | `` |
| Text can be made bigger without breaking the page | `[ ]` | `` |
| Images have text descriptions (alt text); videos have captions | `[ ]` | `` |
| Nothing flashes dangerously and animations can be turned off | `[ ]` | `` |

**Q12.2 – Which languages and regions are supported in this release?**
*Example:* `English (US), Spanish (Mexico). Other languages planned for 1.3.0.`
▶ **Answer:** ``

**Q12.3 – Localization checks**
| Check | Done? | Notes |
|---|---|---|
| All text is translated (no missing words) | `[ ]` | `` |
| Translations checked by a fluent human (not only by AI) | `[ ]` | `` |
| Dates, times, numbers, and currency show correctly | `[ ]` | `` |
| Right-to-left languages work (if supported) | `[ ]` | `` |
| Text still fits on screen in longer languages | `[ ]` | `` |

**Q12.4 – Do any local rules apply in the regions we launch in?** (accessibility laws, language laws, consumer rules)
▶ **Answer:** `[ ] None known   [ ] Yes: ____   Checked by: ____`

**Q12.5 – If the product has an AI feature, does it work equally well in every supported language and for different kinds of users?**
▶ **Answer:** `[ ] N/A (no AI feature)   [ ] Yes → proof: ____   [ ] No → known gaps: ____`

---

# SECTION 13 – DOCUMENTATION AND TRAINING ("Can people learn it?")

*Why we ask:* A great release that nobody understands creates support tickets, not happy customers.

**Q13.1 – Which documents were created or updated for this release?**
| Document | Needed? | Updated? | Owner | Link |
|---|---|---|---|---|
| User guide / help center | `[ ]` | `[ ]` | `` | `` |
| FAQ | `[ ]` | `[ ]` | `` | `` |
| Public changelog / "What's New" page | `[ ]` | `[ ]` | `` | `` |
| In-app tips or onboarding tour | `[ ]` | `[ ]` | `` | `` |
| API / developer docs | `[ ]` | `[ ]` | `` | `` |
| Internal runbook (how to operate and fix it) | `[ ]` | `[ ]` | `` | `` |
| Support answer templates ("macros") | `[ ]` | `[ ]` | `` | `` |
| Guidance on using AI features safely and what they cannot do | `[ ]` | `[ ]` | `` | `` |

**Q13.2 – Was the documentation tested by someone who did NOT write it?**
*Why we ask:* The writer already knows the answer; a fresh reader finds the gaps. A beginner trying the steps is the best test.
▶ **Answer:** `[ ] Yes → who: ____   Problems found and fixed: ____   [ ] No (TBD)`

**Q13.3 – Which teams need training before launch?**
| Team | Training topic | Date | Done? |
|---|---|---|---|
| Support | `` | `` | `[ ]` |
| Sales / customer success | `` | `` | `[ ]` |
| On-call engineers | Rollback and kill switch | `` | `[ ]` |

**Q13.4 – Is there a short "first 10 minutes" guide for brand-new customers?**
▶ **Answer:** `[ ] Yes → link: ____   [ ] No (TBD)`

---

# SECTION 14 – MARKETING AND COMMUNICATIONS PLAN ("How do people hear about it?")

*Why we ask:* To reach 500 customers, the right people must hear the right message at the right time, and every promise must be true.

**Q14.1 – Who is this release for?** (one sentence describing the ideal customer)
*Example:* `Home gardeners aged 25 to 45 who keep forgetting to water their plants.`
▶ **Answer:** ``

**Q14.2 – What is the one message we want people to remember?** (one sentence, plain words)
▶ **Answer:** ``

**Q14.3 – Channels and dates**
| Channel | What we will publish | Date | Owner | Done? |
|---|---|---|---|---|
| Email to waitlist / existing users | `` | `` | `` | `[ ]` |
| In-app announcement | `` | `` | `` | `[ ]` |
| Blog / changelog page | `` | `` | `` | `[ ]` |
| Social media | `` | `` | `` | `[ ]` |
| Communities / forums / partners | `` | `` | `` | `[ ]` |
| Press or influencers (optional) | `` | `` | `` | `[ ]` |

**Q14.4 – Launch assets ready?**
`[ ]` Landing page  `[ ]` Screenshots  `[ ]` Demo video  `[ ]` Email copy  `[ ]` Social posts  `[ ]` Short press note  `[ ]` Sign-up / waitlist form tested  `[ ]` Analytics tracking set up

**Q14.5 – How will we get customers at each rollout stage?** (link to Section 16)
| Stage target | How we will find them | Expected sign-ups | Actual |
|---|---|---|---|
| First 50 | `` | `` | `` |
| 100 | `` | `` | `` |
| 250 | `` | `` | `` |
| 500 | `` | `` | `` |

**Q14.6 – Claims check: is every public statement true and provable?**
*Rule: Never say the product can do something it cannot. Be especially honest about AI ("may make mistakes", "works best for common plants").*
▶ **Answer:** `[ ] Yes, every claim has proof   [ ] No → fix before launch: ____`   **Checked by:** ``

**Q14.7 – Who approves public messages, and who speaks if there is a problem?**
▶ **Answer:** `Approver: ____   Spokesperson in an incident: ____   Incident message template: ____ (see Section 17)`

---

# SECTION 15 – SUCCESS METRICS AND MONITORING

**Q15.1 – What numbers will tell us the release is healthy?**
*Pick a target BEFORE launch, so nobody argues later.*
| Metric | How measured | Target | Alarm line (act if worse than) | Dashboard link |
|---|---|---|---|---|
| Crash-free sessions | `` | `` | `` | `` |
| Error rate | `` | `` | `` | `` |
| Response speed | `` | `` | `` | `` |
| Sign-ups (towards 500) | `` | 500 | `` | `` |
| Activation (users who finish the first key action) | `` | `` | `` | `` |
| Week-1 retention (users who come back) | `` | `` | `` | `` |
| Support tickets per 100 users | `` | `` | `` | `` |
| Customer satisfaction (NPS / rating) | `` | `` | `` | `` |
| AI answer quality (if AI feature) | `` | `` | `` | `` |
| Cost per user (cloud + AI usage) | `` | `` | `` | `` |

**Q15.2 – Who watches the dashboards and how often?**
▶ **Answer:** `Person: ____   Frequency: [ ] hourly on launch day [ ] daily [ ] weekly`

**Q15.3 – Which alerts will wake someone up, and who gets them?**
▶ **Answer:** ``

---

# SECTION 16 – ROLLOUT PLAN (from first user to first 500 customers)

*Why we ask:* Giving the product to everyone at once is risky. We open the door in steps and only move forward when the numbers are good.

**Q16.1 – Rollout stages**
| Stage | Who gets it | Number of users | Start date | Move-forward rule (Go gate) | Status |
|---|---|---|---|---|---|
| 0. Internal | Our own team | `` | `` | No critical bugs | `[ ]` |
| 1. Friends and beta | Invited testers | `` | `` | `` | `[ ]` |
| 2. Launch | First real customers | up to 50 | `` | `` | `[ ]` |
| 3. Grow | Early adopters | up to 100 | `` | `` | `[ ]` |
| 4. Grow | Open invitations | up to 250 | `` | `` | `[ ]` |
| 5. Goal | General availability | **500** | `` | `` | `[ ]` |

*Example Go gate:* `Error rate under 1% and no Critical bugs for 48 hours.`

**Q16.2 – How do we choose who gets it first?** (waitlist, invite code, region, random %)
▶ **Answer:** ``

**Q16.3 – Feature flags / on-off switches**
| Flag name | Controls what | Default (on/off) | Who can switch it | Remove flag by (date) |
|---|---|---|---|---|
| `` | `` | `` | `` | `` |

**Q16.4 – Emergency "kill switch": how do we turn the risky part off in under 5 minutes?**
▶ **Answer:** `Switch name: ____   Where: ____   Who can flip it: ____`

**Q16.5 – Launch-day checklist**
`[ ]` Staging rehearsal passed  `[ ]` Backups taken  `[ ]` Dashboards open  `[ ]` On-call person confirmed  `[ ]` Support team briefed  `[ ]` Announcement ready  `[ ]` Rollback tested  `[ ]` Customers who need to act have been warned

**Q16.6 – How are customers told about the release?**
▶ **Answer:** `[ ] In-app message   [ ] Email   [ ] Blog / changelog page   [ ] Social media   [ ] Support team only   Link: ____`

**Q16.7 – Support readiness**
▶ **Answer:** `FAQ written: [ ] Yes [ ] No   Support trained: [ ] Yes [ ] No   Where do customers ask for help: ____`

---

# SECTION 17 – ROLLBACK AND INCIDENT PLAN ("If something goes wrong")

**Q17.1 – What would make us STOP or UNDO the release?** (be specific)
*Example:* `Error rate above 3% for 10 minutes, any data loss, or any security leak.`
▶ **Answer:** ``

**Q17.2 – How do we undo it?** (step by step, written so a tired person at 3 a.m. can follow it)
1. `` 
2. `` 
3. `` 

**Q17.3 – Rollback facts**
| Question | Answer |
|---|---|
| How long does rollback take? | `` |
| Is data affected by rollback? | `[ ] No [ ] Yes → plan: ____` |
| Was rollback practiced? **(HARD GATE 2: must be Yes)** | `[ ] Yes → date: ____ [ ] No` |
| Who decides to roll back? | `` |

**Q17.4 – Who do we call, in what order?**
| Order | Name | Role | Phone / chat |
|---|---|---|---|
| 1 | `` | `` | `` |
| 2 | `` | `` | `` |
| 3 | `` | `` | `` |

**Q17.5 – How do we tell customers if there is a problem?** (status page, email, in-app)
▶ **Answer:** ``

**Q17.6 – If an AI agent or AI feature misbehaves, how do we stop it?**
▶ **Answer:** ``

---

# SECTION 18 – KNOWN ISSUES AND LIMITATIONS

*Honesty builds trust. List what is imperfect.*

**Q18.1 – Known issues**
| Issue | Who is affected | Workaround | Planned fix (version/date) |
|---|---|---|---|
| `` | `` | `` | `` |

**Q18.2 – Limitations** (what the product cannot do yet)
▶ **Answer:** ``

**Q18.3 – Unsupported devices, browsers, or regions**
▶ **Answer:** ``

---

# SECTION 19 – HOW TO UPGRADE / WHAT CUSTOMERS MUST DO

**Q19.1 – Do customers need to do anything?**
▶ **Answer:** `[ ] No, it updates automatically   [ ] Yes (fill in steps below)`

**Q19.2 – Steps for customers** (numbered, simple, with screenshots or links if possible)
1. `` 
2. `` 
3. `` 

**Q19.3 – Steps for our internal team / self-hosted admins**
1. `` 
2. `` 

**Q19.4 – Minimum requirements**
▶ **Answer:** `Operating system / browser / app version / other: ____`

**Q19.5 – Where is help?** (docs, FAQ, support contact)
▶ **Answer:** ``

---

# SECTION 20 – CUSTOMER FEEDBACK, ADOPTION, AND RETROSPECTIVE (fill during and after rollout)

*Update this section at each stage until you reach 500 customers.*

**Q20.1 – Adoption tracker**
| Date | Total customers | New this period | Active users | Week-1 retention | Support tickets | Rating / NPS | Notes |
|---|---|---|---|---|---|---|---|
| `` | `` | `` | `` | `` | `` | `` | `` |

**Q20.2 – What are customers saying?** (top 5 themes: praise and complaints, with counts)
| Theme | Praise or complaint | How many people | What we will do |
|---|---|---|---|
| `` | `` | `` | `` |

**Q20.3 – Incidents during rollout**
| Date | What happened | Impact | Fix | Lesson |
|---|---|---|---|---|
| `` | `` | `` | `` | `` |

**Q20.4 – Date we reached 500 customers**
▶ **Answer:** ``

**Q20.5 – Retrospective: What went well? What went badly? What will we change next time?**
| Went well | Went badly | Change for next release |
|---|---|---|
| `` | `` | `` |

**Q20.6 – How did AI help or hurt this release?** (time saved, mistakes caught, mistakes introduced)
▶ **Answer:** ``

**Q20.7 – What is next?** (next version, planned date, top 3 items)
▶ **Answer:** ``

---

# SECTION 21 – SIGN-OFFS ("Who said it's OK?")

*A signature means: "I checked the proof and I agree." Type name and date.*

| Role | Name | Decision (Approve / Reject) | Date | Notes |
|---|---|---|---|---|
| Engineering Lead | `` | `` | `` | `` |
| QA Lead | `` | `` | `` | `` |
| Security / Privacy | `` | `` | `` | `` |
| Legal (if needed) | `` | `` | `` | `` |
| Accessibility lead | `` | `` | `` | `` |
| Budget approver | `` | `` | `` | `` |
| Marketing / Communications | `` | `` | `` | `` |
| Product Owner | `` | `` | `` | `` |
| Release Owner | `` | `` | `` | `` |
| Human approver of AI work | `` | `` | `` | `` |

**Hard Gate verdict** (fill in at sign-off; all four must pass)
| Gate | Pass? | Proof link | Verified by |
|---|---|---|---|
| 1. Zero critical bugs and zero critical security issues | `[ ]` | `` | `` |
| 2. Rollback practiced | `[ ]` | `` | `` |
| 3. Named human approved all AI work | `[ ]` | `` | `` |
| 4. Privacy and data-consent check passed | `[ ]` | `` | `` |

---

# SECTION 22 – FINAL CHECKLIST (do not launch unless all are ticked or explained)

- `[ ]` Every question in this file is answered (or TBD with owner/date, or N/A with reason)
- `[ ]` Version number follows the SemVer mini-quiz (Q1.2)
- `[ ]` Summary (Section 2) is written in plain words
- `[ ]` All changes were reviewed by a human who did not write them
- `[ ]` **HARD GATE 1:** 0 Critical bugs and 0 Critical security issues
- `[ ]` **HARD GATE 3:** AI-generated work is disclosed and approved by a named human (Section 6)
- `[ ]` **HARD GATE 4:** Privacy and data-consent check passed (Sections 9 and 10)
- `[ ]` Licenses checked (Section 10)
- `[ ]` Rollout stages and Go gates agreed (Section 16)
- `[ ]` **HARD GATE 2:** Rollback written and practiced (Section 17)
- `[ ]` Dashboards and alerts are live (Section 15)
- `[ ]` Cost per customer and spending cap agreed (Section 11)
- `[ ]` Accessibility and language checks done (Section 12)
- `[ ]` Documentation and training ready (Section 13)
- `[ ]` Marketing plan and claims check approved (Section 14)
- `[ ]` Support team and customers are informed
- `[ ]` All sign-offs collected (Section 21)
- `[ ]` Machine-readable summary (Section 23) matches the rest of this file

---

# SECTION 23 – MACHINE-READABLE SUMMARY (for AI agents and automation)

*Fill this in last, copying from the answers above. Keep the keys exactly as written. Use `null` for unknown.*

```yaml
release:
  project: ""
  version: ""            # SemVer, e.g. 1.2.0
  previous_version: ""
  type: ""               # major | minor | patch | hotfix | pre-release
  status: ""             # draft | in_review | approved | released | rolled_back | closed
  planned_date: ""       # YYYY-MM-DD
  actual_date: ""
  owner: ""
  risk: ""               # low | medium | high
  decision: ""           # go | no-go | conditional
changes:
  features: []
  improvements: []
  fixes: []
  deprecations: []
  breaking_changes: []
  data_migration: false
  api_changed: false
ai_involvement:
  ai_written_code: ""    # none | <25% | 25-75% | >75%
  models_and_agents: []
  autonomous_actions: false
  human_approver: ""
  ai_feature_in_product: false
quality:
  critical_bugs_open: 0
  critical_security_open: 0
  tests_passed: 0
  tests_failed: 0
  human_review_complete: false
rollout:
  current_stage: ""      # internal | beta | 50 | 100 | 250 | 500
  customers_now: 0
  target_customers: 500
  kill_switch: ""
  rollback_tested: false
hard_gates:
  zero_critical_bugs_and_security_issues: false
  rollback_practiced: false
  human_approver_named_for_ai_work: false
  privacy_and_consent_check_passed: false
readiness:
  monthly_cost_total: null
  cost_per_customer_at_500: null
  ai_spend_cap: null
  accessibility_checks_passed: false
  languages: []
  documentation_ready: false
  support_trained: false
  marketing_plan_approved: false
  claims_checked: false
links:
  code_tag: ""
  ci_run: ""
  dashboard: ""
  test_report: ""
  rollback_runbook: ""
```

---

# SECTION 24 – FILLED-IN EXAMPLE (fictional – for learning only, delete in your copy)

**Project:** PlantPal  **Version:** 1.2.0  **Type:** Minor  **Date:** 2026-11-03  **Owner:** Sam Rivera

**Summary (Q2.1):** PlantPal 1.2.0 lets people scan a plant with their phone camera and learn how often to water it. It also fixes a crash that happened when opening the app without internet.

**Top 3 changes (Q2.2):** 1) Scan-a-plant feature. 2) Offline crash fixed. 3) Faster home screen (2.4s down to 1.1s).

**Risk (Q2.3):** Medium, because it adds a new AI photo-recognition feature.

**What's New (Q3.1):** Scan a plant with your camera to get watering tips [#128].

**AI involvement (Q6.1 to Q6.8):** About 40% of the code was written with an AI coding assistant (the camera upload module and 120 unit tests). Every AI-written file was reviewed by Priya N. on 2026-10-27. AI code review found 9 issues; 8 fixed, 1 accepted (cosmetic). No AI agent deployed or merged anything on its own.

**AI feature (Q6.10 to Q6.12):** Identifies 3,000 common houseplants. Cannot identify plant diseases. Accuracy test: 93% on 500 test photos (minimum allowed: 90%) → Pass. If confidence is under 70%, the app says "I'm not sure" instead of guessing.

**Code review (Q7):** 14 pull requests, all reviewed by a second human, 0 open comments.

**QA (Q8):** 212 of 212 tests passed. Load test with 1,000 simulated users: average response 380 ms, 0 errors. Critical bugs open: 0.

**Security (Q9):** Dependency and secret scans clean. New data: plant photos, stored 30 days, deletable by user. Photos are NOT sent to third parties.

**Cost (Q11):** About $1,200 per month at 500 customers = $2.40 per customer. AI budget cap $500 per month, alert at 80%.

**Accessibility and languages (Q12):** Screen reader, keyboard-only, and contrast checks passed. English and Spanish supported; the Spanish text was checked by a fluent reviewer.

**Docs and training (Q13):** Help center, FAQ, and changelog updated. Support trained on 2026-10-31. A new teammate followed the "first 10 minutes" guide without help.

**Marketing (Q14):** For home gardeners who forget to water plants. Message: "Know exactly when to water." Waitlist email on 2026-11-03, blog post on 2026-11-05. Claims checked: the app says it may be wrong on rare plants.

**Rollout (Q16.1):** Internal (10 people, 2026-11-03) → Beta (40 people, 2026-11-05) → 50 customers (2026-11-10) → 100 (2026-11-17) → 250 (2026-11-24) → 500 (2026-12-01). Go gate for each step: error rate under 1% and no Critical bugs for 48 hours.

**Kill switch (Q16.4):** Flag `scan_plant_enabled` in the admin console; Sam or Priya can switch it off in under 2 minutes.

**Rollback (Q17):** Roll back if error rate is above 3% for 10 minutes or any photo is shown to the wrong user. Rollback takes about 8 minutes; practiced on 2026-10-30. First call: Sam Rivera.

**Known issues (Q18.1):** Scanning is slow on phones older than 2019. Workaround: type the plant name. Fix planned in 1.2.1.

**Customer action (Q19.1):** None, updates automatically.

**Hard Gates:** All 4 passed (0 critical issues, rollback practiced 2026-10-30, Priya N. approved the AI work, privacy and consent check passed).

**Sign-offs (Q21):** Approved by Engineering, QA, Security, Product, and Release Owner on 2026-11-02.

---

# GLOSSARY (words in plain English)

| Word | Meaning |
|---|---|
| **Release** | A new version of the product given to users |
| **SemVer** | A numbering system: MAJOR.MINOR.PATCH |
| **Pull request (PR)** | A proposed code change waiting for review |
| **CI pipeline** | A robot that builds and tests the code automatically |
| **Staging** | A safe practice copy of the product |
| **Feature flag** | An on/off switch for one feature |
| **Kill switch** | An emergency switch that turns a feature off fast |
| **Rollback** | Going back to the previous working version |
| **Go gate** | A check that must pass before moving to the next stage |
| **Hotfix** | An urgent small fix released outside the normal schedule |
| **Retention** | The share of users who come back |
| **NPS** | Net Promoter Score: "Would you recommend us?" |
| **Eval** | A test that measures how good an AI's answers are |
| **Prompt injection** | A trick that makes an AI ignore its rules |
| **AI agent** | An AI that can take actions (write code, run tools) by itself |
| **AI-DLC** | AI-Driven Development Life Cycle: building software with AI helping at every step |
| **Breaking change** | A change that makes the old way stop working |

---
*Template version: 1.1 – Keep this footer. When you improve the template, raise this number and write what changed.*
*Changes in 1.1: added Sections 11 to 14 (Cost, Accessibility and Localization, Documentation and Training, Marketing and Communications); added the 4 Hard Gates; renumbered later sections.*
