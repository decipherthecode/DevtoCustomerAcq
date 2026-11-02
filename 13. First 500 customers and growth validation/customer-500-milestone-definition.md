# How to Fill This Document (Read This First)

**What is this?** This document defines one goal: **"Reach 500 active users."** It makes sure everyone agrees on what that means, how we count it, and how we know we really got there.

**Who can fill it?** Anyone. If you can read and type, you can fill it.

**How to fill it (5 simple rules):**
1. Go top to bottom. Do not skip around.
2. Each section has a **Question**, an **Example**, and an **Answer** box. Read the example, then write your own answer.
3. Replace everything in `[square brackets]` with your own words or numbers.
4. If you do not know an answer, write `UNKNOWN - [name of person who can find out] - [date]`. Never guess and never leave it blank.
5. Use numbers instead of vague words. Write "500 users by 31 March", not "lots of users soon".

**Tick boxes:** change `[ ]` to `[x]` when done.

**Status of this document:** `[Draft / In Review / Approved]`
**Last updated:** `[date]`

> **Tip for AI agents:** Every section ends with an **AI Agent Check**. An AI agent can run that check and report problems. A human must still approve anything marked **HUMAN APPROVAL**.

---

# Part 0: Document Control

| Field | Answer |
|---|---|
| Project name | `[e.g., "PlantPal"]` |
| Product type | `[ ] Web app / SaaS   [ ] Mobile app   [ ] Both` |
| Document owner (one person) | `[name]` |
| Approver (one person who says "yes, this is correct") | `[name]` |
| Version | `[v1.0]` |
| Date created | `[date]` |
| Related documents (links) | `[Product brief, roadmap, analytics dashboard]` |

---

# Part 1: Idea and Requirements

## 1.1 What problem does the product solve?
**Question:** In one or two sentences, what problem do people have that your product fixes?
**Example:** "Busy people forget to water their plants, so the plants die. PlantPal sends reminders and tells them how much water each plant needs."
**Answer:** `[...]`

## 1.2 Who is the product for?
**Question:** Describe your ideal user. Who are they, and what do they do all day?
**Example:** "Adults aged 25-40 who live in apartments and own 3 or more houseplants."
**Answer:** `[...]`

## 1.3 What is the "key action"?
**Question:** What is the ONE thing a user does that shows they are getting real value? (Not "opened the app". Something meaningful.)
**Examples:**
- Project management tool: "Created a task or completed a task"
- Fitness app: "Logged a workout"
- Invoicing SaaS: "Sent an invoice"

**Answer (the key action):** `[...]`

## 1.4 Why 500?
**Question:** Why is 500 active users the right goal for this stage? What will we learn or unlock when we reach it?
**Example:** "At 500 active users we can prove people keep using it, justify hiring a support person, and begin paid advertising."
**Answer:** `[...]`

## 1.5 Requirements snapshot
**Question:** List the must-have features needed before launch. Keep it to 10 or fewer.

| # | Feature | Why it is a must-have | Done? |
|---|---|---|---|
| 1 | `[feature]` | `[reason]` | `[ ]` |
| 2 | `[feature]` | `[reason]` | `[ ]` |
| 3 | `[feature]` | `[reason]` | `[ ]` |

**Question:** What is clearly **NOT** included in the first version? (This stops scope from growing.)
**Answer:** `[...]`

**AI Agent Check:** Confirm 1.3 names a real action (not just a login or page view), and that 1.5 contains 10 or fewer must-haves.

---

# Part 2: The Milestone Definition (The Heart of This Document)

## 2.1 The goal in one sentence
**Question:** Fill in the blanks.
**Template:** "We reach the Customer 500 Milestone when **[500]** unique users have each **[key action from 1.3]** at least **[1]** time(s) in the last **[30]** days, as measured in **[tool name]** and verified by **[person]**."
**Example:** "We reach the Customer 500 Milestone when 500 unique users have each sent at least 1 invoice in the last 30 days, as measured in Mixpanel and verified by Priya."
**Answer:** `[...]`

## 2.2 Definition table (fill every row)

| Item | Default (change only if needed) | Your answer |
|---|---|---|
| Target number | 500 | `[ ]` |
| What counts as a "user" | One unique real person with one account | `[ ]` |
| What counts as "active" | Did the key action at least once in the last 30 days | `[ ]` |
| Free users count? | `[Yes / No]` | `[ ]` |
| Paying users only? | `[Yes / No]` | `[ ]` |
| Target date | `[date]` | `[ ]` |
| Start date of counting | Launch day | `[ ]` |
| Time zone for reporting | `[e.g., UTC]` | `[ ]` |

## 2.3 What does NOT count (exclusion rules)
**Question:** Tick everything we will remove from the count.

- `[ ]` Team members and employees
- `[ ]` Test accounts and demo accounts
- `[ ]` Bots, spam sign-ups, and fake accounts
- `[ ]` Duplicate accounts of the same person
- `[ ]` Users who signed up but never did the key action
- `[ ]` Refunded or cancelled accounts (if paying users matter)
- `[ ]` Other: `[...]`

**How we find and remove them:** `[e.g., filter out emails ending @ourcompany.com; remove accounts flagged "test"]`

## 2.4 Quality bar: "500 real, healthy users"
**Question:** Reaching 500 is not enough if they all leave next week. Set the minimum health numbers.

| Health check | Example target | Your target |
|---|---|---|
| Users still active after 4 weeks (retention) | At least 30% | `[ ]%` |
| Monthly churn (users who leave) | No more than 10% | `[ ]%` |
| Users who finished onboarding | At least 60% | `[ ]%` |
| Average satisfaction (survey or rating) | At least 4.0 out of 5 | `[ ]` |
| Support tickets per 100 users per month | No more than 15 | `[ ]` |

## 2.5 Where the numbers come from (single source of truth)
**Question:** Which ONE tool or report is the official count? If two tools disagree, which one wins?

| Item | Answer |
|---|---|
| Official tool (e.g., Mixpanel, Amplitude, Google Analytics, database query) | `[ ]` |
| Link to dashboard or report | `[ ]` |
| Who checks the number | `[name]` |
| How often it is checked | `[Daily / Weekly]` |
| Tiebreaker if tools disagree | `[ ]` |

## 2.6 Milestone checkpoints
**Question:** Break 500 into smaller steps so we can see if we are on track.

| Checkpoint | Active users | Target date | Reached? |
|---|---|---|---|
| First 10 (friends, testers) | 10 | `[date]` | `[ ]` |
| First 50 | 50 | `[date]` | `[ ]` |
| First 100 | 100 | `[date]` | `[ ]` |
| First 250 | 250 | `[date]` | `[ ]` |
| **500 (goal)** | **500** | `[date]` | `[ ]` |

**HUMAN APPROVAL:** The approver in Part 0 must agree to Part 2 before building continues. Approved by: `[name]` on `[date]`

**AI Agent Check:** Verify that 2.1 matches the table in 2.2 exactly, that every exclusion in 2.3 has a method, and that 2.5 names exactly one source of truth.

---

# Part 3: Build with AI Agents

## 3.1 Who does what?
**Question:** List each AI agent (or AI tool) and each human. Say what each one is allowed to do.

| Role | AI agent or human | Allowed to | NOT allowed to |
|---|---|---|---|
| Writes code | `[e.g., Claude Code]` | `[write and edit code in feature branches]` | `[push straight to production]` |
| Reviews code | `[ ]` | `[ ]` | `[ ]` |
| Writes tests | `[ ]` | `[ ]` | `[ ]` |
| Writes docs | `[ ]` | `[ ]` | `[ ]` |
| Approves releases | `[human name]` | `[final yes or no]` | `[ ]` |

## 3.2 Human approval points
**Question:** Tick the steps where a human MUST say "yes" before moving on.

- `[ ]` Feature list is final
- `[ ]` Design is final
- `[ ]` Code merged into the main branch
- `[ ]` Anything touching payments, passwords, or personal data
- `[ ]` Release to real users
- `[ ]` Other: `[...]`

## 3.3 Tracking for the milestone (build it in from day one)
**Question:** Make sure the product can actually count the milestone. Tick when built and tested.

- `[ ]` The key action from 1.3 is recorded as an event (name it: `[event_name]`)
- `[ ]` Each user has a unique ID
- `[ ]` Test accounts are labeled so they can be excluded
- `[ ]` Dashboard shows the live active-user count
- `[ ]` Retention (2.4) can be viewed on the dashboard
- `[ ]` Privacy rules followed (users agreed to tracking where the law requires it)

## 3.4 AI work log
**Question:** How do we keep a record of what AI agents did?
**Example:** "Every AI change goes in a pull request with the prompt used, and a human reviews it."
**Answer:** `[...]`

**Risks to watch:** AI code that looks right but is wrong, leaked secrets or passwords, and made-up features. Write how you will guard against each:
**Answer:** `[...]`

**AI Agent Check:** Confirm every item in 3.3 is ticked, and that no AI role in 3.1 can release to real users without human approval.

---

# Part 4: Quality Assurance and Release Readiness

## 4.1 Quality gates (all must be ticked before launch)

| Gate | Example target | Your target | Passed? |
|---|---|---|---|
| All must-have features (1.5) work | 100% | `[ ]` | `[ ]` |
| Critical bugs open | 0 | `[ ]` | `[ ]` |
| Major bugs open | 3 or fewer | `[ ]` | `[ ]` |
| Automated tests passing | 95% or more | `[ ]` | `[ ]` |
| Page or app load time | Under 3 seconds | `[ ]` | `[ ]` |
| Works on target devices/browsers | `[list them]` | `[ ]` | `[ ]` |
| Security check done | Yes | `[ ]` | `[ ]` |
| Sign-up to key action tested end to end | Yes | `[ ]` | `[ ]` |
| Tracking numbers match real actions | Yes | `[ ]` | `[ ]` |

## 4.2 Mobile-only checks (skip if web only)
- `[ ]` Works on `[list phone models / OS versions]`
- `[ ]` App store listing, screenshots, and privacy details ready
- `[ ]` App store review submitted, with time allowed for approval

## 4.3 Go / No-Go decision
**Question:** On launch day, who decides, and what makes the answer "No-Go"?
**Example:** "Any open critical bug, or the tracking test failing, means No-Go."
**Decision maker:** `[name]`
**No-Go triggers:** `[...]`
**Decision:** `[Go / No-Go]` on `[date]`
**HUMAN APPROVAL:** `[name]`

## 4.4 Rollback plan
**Question:** If launch goes badly, how do we undo it, and who does it?
**Answer:** `[...]`

**AI Agent Check:** Recount the gates, list any unticked ones, and flag any gate with no number.

---

# Part 5: Launch and Growth to 500

## 5.1 Launch plan
| Item | Answer |
|---|---|
| Launch date | `[ ]` |
| Launch type | `[ ] Private beta  [ ] Public launch  [ ] Gradual rollout` |
| First 10 users come from | `[e.g., friends, waitlist, beta testers]` |
| Launch message (one sentence) | `[ ]` |

## 5.2 Where users will come from

| Channel | Example | Goal (users) | Budget | Owner |
|---|---|---|---|---|
| Waitlist or email list | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Social media / communities | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Referrals / word of mouth | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Paid ads | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| Partnerships | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| App store / search | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

**Cost per active user limit:** `[e.g., no more than $15]`
**Total budget for reaching 500:** `[ ]`

## 5.3 Onboarding (getting new users to the key action fast)
**Question:** How many steps from sign-up to the key action? What is the target time?
**Example:** "3 steps, under 2 minutes."
**Answer:** `[...]`

## 5.4 Support and feedback
| Item | Answer |
|---|---|
| Where users ask for help | `[email, chat, form]` |
| Reply time promised | `[e.g., within 24 hours]` |
| How we collect feedback | `[survey, interviews, in-app form]` |
| Who reads feedback | `[name]` |

## 5.5 Weekly check-in
**Question:** Every week, fill this in.

| Week | Active users | Change vs last week | Retention | Top problem | Action decided |
|---|---|---|---|---|---|
| 1 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 2 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |
| 3 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[ ]` |

## 5.6 If we are off track
**Question:** What do we do if we are behind schedule?
**Example:** "If under 50% of the checkpoint by its date, pause paid ads, interview 10 users, and fix the biggest drop-off before spending more."
**Answer:** `[...]`

**AI Agent Check:** Each week, compare the dashboard count to 5.5, flag differences over 2%, and draft a summary for the owner.

---

# Part 6: Final Verification (Did We Really Reach 500?)

**Question:** Complete this when the dashboard first shows 500.

| Step | Done? | Who | Date |
|---|---|---|---|
| Pull the count from the official source (2.5) | `[ ]` | `[ ]` | `[ ]` |
| Apply all exclusion rules (2.3) | `[ ]` | `[ ]` | `[ ]` |
| Count after exclusions is 500 or more | `[ ]` | `[ ]` | `[ ]` |
| Quality bar (2.4) met | `[ ]` | `[ ]` | `[ ]` |
| Spot-check 20 random users are real and active | `[ ]` | `[ ]` | `[ ]` |
| Save a screenshot or export as proof | `[ ]` | `[ ]` | `[ ]` |

**Final count after exclusions:** `[ ]`
**Date reached:** `[ ]`
**Days from launch to 500:** `[ ]`
**Total spend:** `[ ]`  **Cost per active user:** `[ ]`

**HUMAN APPROVAL:** "Milestone reached." Approved by `[name]` on `[date]`

---

# Part 7: Lessons Learned and Next Milestone

1. What worked best? `[...]`
2. What surprised us? `[...]`
3. What would we do differently? `[...]`
4. Which channel gave the best users? `[...]`
5. Next milestone (e.g., 1,000 active users or first revenue goal): `[...]`

---

# Part 8: Final Self-Check (Is This Document Ready?)

- `[ ]` No `[brackets]` left unfilled (or each says UNKNOWN with a name and date)
- `[ ]` Every goal has a number and a date
- `[ ]` One owner and one approver are named
- `[ ]` The key action is specific and measurable
- `[ ]` Exclusion rules and the official data source are written down
- `[ ]` Quality gates and Go/No-Go are agreed
- `[ ]` A stranger could read this and count to 500 the same way we do

---

# Appendix A: Glossary (Simple Words)

- **Active user:** Someone who recently did the key action.
- **Key action:** The meaningful thing that shows a user is getting value.
- **Retention:** The share of users who come back after a period.
- **Churn:** The share of users who leave.
- **Onboarding:** The first steps a new user takes.
- **Quality gate:** A test that must pass before moving forward.
- **Go / No-Go:** The final yes or no on launching.
- **Single source of truth:** The one official place a number comes from.
- **AI agent:** A software helper powered by AI that does tasks such as writing or testing code.

# Appendix B: Change Log

| Version | Date | Who | What changed |
|---|---|---|---|
| v0.1 | `[ ]` | `[ ]` | First draft |
