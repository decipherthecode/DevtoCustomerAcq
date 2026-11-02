# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

> **Template version:** 1.0 | **Owner of this template:** [Your name/team] | **Reuse across:** web apps, SaaS, mobile apps (iOS / Android)

## What is this document?

This is a **UAT Plan**. UAT means **User Acceptance Testing**. In plain words:

> Before we show our product to the whole world, we let **real people** try it and tell us: *"Yes, this works for me"* or *"No, this is broken or confusing."*

This plan covers the whole journey: **from the day the product is built (development) until the first 500 real customers are happily using it.**

## The 5 simple rules

1. **Answer every question.** Never leave a blank. If something does not apply, write `N/A - because [reason]`. If you do not know yet, write `TBD - [who] will decide by [date]`.
2. **Follow the three-part pattern.** Every section has: a **Question**, an **Example** (so you can see what a good answer looks like), and **YOUR ANSWER** (where you type).
3. **Be specific, use numbers.** Bad: "The app should be fast." Good: "Pages load in under 3 seconds for 95 out of 100 visits."
4. **Do not delete the examples.** Leave them in grey/quote blocks, so the next person can learn from them. Only replace the text under **YOUR ANSWER**.
5. **Fill in order, top to bottom.** Later sections depend on earlier ones. Use the checklist at the bottom of this section.

## Symbols you will see

| Symbol | Meaning |
|---|---|
| `[ ]` | A checkbox. Change to `[x]` when done. |
| `[PLACEHOLDER]` | Replace this with your real information. |
| **Q:** | A question you must answer. |
| **Example:** | A filled-in sample. Do not copy blindly; adapt it. |
| **YOUR ANSWER:** | Type your answer here. |
| `TBD` | "To be decided." Must include who and by when. |
| 🔴 / 🟠 / 🟡 / 🟢 | Critical / High / Medium / Low severity. |

## Words you might not know (mini glossary)

| Word | Simple meaning |
|---|---|
| **UAT** | Real users check that the product does what they need. |
| **Tester** | A person who tries the product and reports what happens. |
| **Scenario** | A short story of something a user does ("Sign up, then create a project"). |
| **Test case** | A scenario broken into exact steps with an expected result. |
| **Defect / Bug** | Something that does not work as it should. |
| **Severity** | How bad the bug is. |
| **Entry criteria** | Things that must be true **before** a testing round starts. |
| **Exit criteria** | Things that must be true **before** a round can end. |
| **Go / No-Go** | The yes-or-no decision to move to the next round or launch. |
| **Sign-off** | A written "yes, approved" from a responsible person. |
| **Closed beta** | Testing with a small, invited group. |
| **Open beta** | Testing with a bigger group anyone can join (with limits). |
| **Rollback** | Undoing a release to go back to the last safe version. |
| **Staging** | A practice copy of the product that is not used by real customers. |
| **Production** | The real, live product. |
| **AI feature** | Any part of the product powered by AI (chat, summaries, recommendations, etc.). |
| **Hallucination** | When AI confidently says something that is false. |

## The 4 testing rounds (the big picture)

```
ROUND 0            ROUND 1             ROUND 2            ROUND 3
Internal Test  ->  Closed Beta     ->  Open Beta      ->  Launch to 500
(our team)         (25 people)         (100 people)       (500 customers)
   |                  |                   |                   |
 GATE 0             GATE 1              GATE 2              GATE 3
(Go/No-Go)         (Go/No-Go)          (Go/No-Go)       (Final report)
```

Nobody moves to the next round until the **gate** is passed. Gates are decided in **Section 9**.

## Who does what when AI agents help (AI-Driven Development Life Cycle)

This template is built for teams where **AI agents help build and test the product**. Use this split:

| AI agents CAN help with | Only HUMANS can do |
|---|---|
| Drafting scenarios and test cases from requirements | Approving scope and exit criteria |
| Running automated checks and regression tests | Deciding Go / No-Go at every gate |
| Summarizing tester feedback and grouping duplicate bugs | Signing the sign-off |
| Drafting daily status reports | Judging whether the product *feels* right |
| Monitoring dashboards and raising alerts | Talking to customers about serious problems |
| Suggesting fixes for bugs | Accepting legal, privacy and safety risks |

> **Rule for AI agents filling this document:** Never invent facts, names, dates or numbers. If information is missing, write `TBD - needs human input from [role]`. Never mark a gate as passed. Only a named human can do that.

## Fill-in order checklist

- [ ] Sections 1-3: Document control, project snapshot, goals
- [ ] Sections 4-6: People and roles, scope, the four rounds
- [ ] Sections 7-9: Testers, entry criteria, exit criteria and gates
- [ ] Sections 10-14: Environment and data, scenarios, AI checks, non-functional checks, feedback
- [ ] Sections 15-19: Bugs, schedule, communication, support, risks
- [ ] Sections 20-23: Metrics, launch readiness, sign-off, lessons learned
- [ ] Appendices: Templates you will copy for daily use
- [ ] Final check: Quality checklist (end of document)

---

# 1. DOCUMENT CONTROL

**Q: Who wrote this, which version is it, and who has approved it?**

> **Example:**
> | Field | Value |
> |---|---|
> | Project name | TaskBuddy |
> | Plan version | 1.0 |
> | Date created | 2026-10-17 |
> | Author | Priya Shah (Project Manager) |
> | Status | Draft |

**YOUR ANSWER:**

| Field | Value |
|---|---|
| Project name | [PLACEHOLDER] |
| Plan version | [e.g. 0.1 Draft, 1.0 Approved] |
| Date created | [YYYY-MM-DD] |
| Last updated | [YYYY-MM-DD] |
| Author (name + role) | [PLACEHOLDER] |
| Status (Draft / In Review / Approved) | [PLACEHOLDER] |
| Where this file lives (link or path) | [PLACEHOLDER] |

**Change history** (add a row every time you change the plan):

| Version | Date | Who changed it | What changed and why |
|---|---|---|---|
| 0.1 | [YYYY-MM-DD] | [Name] | First draft |

---

# 2. PROJECT SNAPSHOT

**Q2.1: What is the product, in one or two simple sentences? Write so a 10-year-old understands.**

> **Example:** "TaskBuddy is an app that helps families share chores. Each person sees their tasks and gets a reminder."

**YOUR ANSWER:**

**Q2.2: Who is the product for? (Your target customer)**

> **Example:** "Parents aged 28-45 with 1-3 kids who use a smartphone every day."

**YOUR ANSWER:**

**Q2.3: What type of product is it? (Tick all that apply)**

- [ ] Web app / SaaS (used in a browser)
- [ ] Mobile app - iOS
- [ ] Mobile app - Android
- [ ] Has AI-powered features
- [ ] Takes payments
- [ ] Stores personal data (names, emails, photos, etc.)
- [ ] Other: [PLACEHOLDER]

**Q2.4: Where is the product in its life right now?**

- [ ] Still being built (development)
- [ ] Development finished, internal testing starting
- [ ] Already in beta
- [ ] Other: [PLACEHOLDER]

**Q2.5: Important links**

| What | Link |
|---|---|
| Requirements / PRD (what we promised to build) | [PLACEHOLDER] |
| Design files (Figma etc.) | [PLACEHOLDER] |
| Bug tracker (Jira, GitHub Issues, etc.) | [PLACEHOLDER] |
| Test environment (staging) address | [PLACEHOLDER] |
| Feedback form | [PLACEHOLDER] |
| Analytics / monitoring dashboard | [PLACEHOLDER] |
| Project chat channel | [PLACEHOLDER] |
| Technical test plan (QA / system testing) | [PLACEHOLDER] |

---

# 3. WHY ARE WE DOING UAT? (GOALS)

**Q3.1: What are the 3-5 big things UAT must prove? Start each with a verb (Confirm, Prove, Check...).**

> **Example:**
> 1. Confirm a new user can sign up and complete their first task in under 5 minutes.
> 2. Confirm parents and kids can both use the app without help.
> 3. Confirm payments work and nobody is charged twice.
> 4. Confirm the AI task-suggestion feature gives useful, safe answers.
> 5. Confirm the product is stable enough for 500 customers.

**YOUR ANSWER:**

1.
2.
3.
4.
5.

**Q3.2: What are the business goals behind the launch?**

> **Example:** "Get 500 active customers in 60 days. At least 40% still using the app after 14 days."

**YOUR ANSWER:**

**Q3.3: What does "success" look like for this UAT in one sentence?**

> **Example:** "500 customers are using TaskBuddy, fewer than 2% report a serious problem, and the business owner has signed off."

**YOUR ANSWER:**

---

# 4. PEOPLE AND ROLES

**Q4.1: Who is on the team? Fill every role. If one person has two roles, write the name twice.**

> **Example:** UAT Lead = Priya Shah. Business Owner = Sam Ortiz (CEO).

**YOUR ANSWER:**

| Role | What this person does | Name | Contact | Backup person |
|---|---|---|---|---|
| **Business Owner / Sponsor** | Final yes/no on launch. Signs off. | [ ] | [ ] | [ ] |
| **UAT Lead** | Runs the whole UAT. Owns this plan. | [ ] | [ ] | [ ] |
| **Product Owner** | Decides what is a bug versus a new idea. | [ ] | [ ] | [ ] |
| **Development Lead** | Fixes bugs, deploys builds. | [ ] | [ ] | [ ] |
| **QA Lead** | Confirms the product passed technical testing first. | [ ] | [ ] | [ ] |
| **Support Lead** | Handles customer questions during beta/launch. | [ ] | [ ] | [ ] |
| **Security / Privacy Owner** | Checks data safety and legal rules. | [ ] | [ ] | [ ] |
| **AI / Prompt Owner** | Owns AI feature quality and safety (skip if no AI). | [ ] | [ ] | [ ] |
| **Mobile Release Owner** | Handles App Store / Google Play (skip if no mobile). | [ ] | [ ] | [ ] |
| **Communications Owner** | Sends messages to testers and customers. | [ ] | [ ] | [ ] |
| **AI agents used** (list each agent and its job) | [e.g. "Test-writer agent drafts scenarios"] | [ ] | [ ] | [ ] |

**Q4.2: Who makes the decisions?**

> **Example:** "Dev Lead decides bug fixes. Product Owner decides scope changes. Business Owner decides Go/No-Go. If the Business Owner is away, the CTO decides."

**YOUR ANSWER:**

**Q4.3: If people disagree, who has the final word, and how fast must they answer?**

> **Example:** "Business Owner. Must answer within 1 working day."

**YOUR ANSWER:**

---

# 5. SCOPE: WHAT WE WILL AND WILL NOT TEST

**Q5.1: List every feature that WILL be tested. Give each a priority: 🔴 Must work, 🟠 Should work, 🟡 Nice to have.**

> **Example:**
> | ID | Feature | Priority | Platforms |
> |---|---|---|---|
> | F-01 | Sign up and log in | 🔴 | Web, iOS, Android |
> | F-02 | Create and share a task | 🔴 | Web, iOS, Android |
> | F-03 | Reminder notifications | 🟠 | iOS, Android |
> | F-04 | AI task suggestions | 🟠 | Web, iOS, Android |
> | F-05 | Dark mode | 🟡 | Web |

**YOUR ANSWER:**

| ID | Feature | Priority | Platforms | Linked requirement |
|---|---|---|---|---|
| F-01 | | | | |
| F-02 | | | | |
| F-03 | | | | |
| F-04 | | | | |
| F-05 | | | | |

**Q5.2: List what is NOT being tested and why. (This prevents "but I thought you tested that!")**

> **Example:** "Admin dashboard - internal only, tested in QA. Hindi language - planned for version 2."

**YOUR ANSWER:**

| Not tested | Why | Who accepts this risk |
|---|---|---|
| | | |

**Q5.3: What user types (roles) will be tested?**

> **Example:** "New user, returning user, parent (admin), child (limited), customer-support agent."

**YOUR ANSWER:**

**Q5.4: What are the acceptance criteria? Write each as: "Given [situation], when [action], then [result]."**

> **Example:** "Given a new user on the sign-up page, when they enter a valid email and password, then they see the welcome screen within 3 seconds."

**YOUR ANSWER:**

| ID | Given | When | Then | Feature |
|---|---|---|---|---|
| AC-01 | | | | F-01 |
| AC-02 | | | | |

**Q5.5: What assumptions are we making? (Things we believe are true but have not proven.)**

> **Example:** "Testers have a smartphone from the last 4 years. The payment provider test mode matches live mode."

**YOUR ANSWER:**

**Q5.6: What limits do we have (time, money, people, rules)?**

> **Example:** "Budget for 4 weeks. Only 2 developers available. Must follow GDPR."

**YOUR ANSWER:**

---

# 6. THE FOUR ROUNDS (DETAILED PLAN)

**Q6.1: Fill in one row per round. Keep the suggested numbers unless you have a good reason to change them.**

> **Example (Round 1):** Closed beta, 25 invited testers, 2 weeks, goal: "find the biggest problems with sign-up and core tasks."

**YOUR ANSWER:**

| | **Round 0: Internal** | **Round 1: Closed Beta** | **Round 2: Open Beta** | **Round 3: Launch to 500** |
|---|---|---|---|---|
| **Who tests** | Our own team and friendly colleagues | Invited people who match our target customer | Sign-up list; anyone allowed in, up to the cap | Real customers; paid or free |
| **Number of people** | [e.g. 10] | **25** | **100** | **500** |
| **Start date** | | | | |
| **End date** | | | | |
| **Length** | [e.g. 1 week] | [e.g. 2 weeks] | [e.g. 2 weeks] | [e.g. 4 weeks] |
| **Main goal** | Catch obvious bugs fast | Prove core journeys work for strangers | Prove it holds up with more people and devices | Prove it works at launch scale |
| **Environment** | Staging | Staging or limited production | Production (feature-flagged) | Production |
| **Do testers pay?** | No | [ ] | [ ] | [ ] |
| **Is it secret?** (NDA needed?) | Yes | [ ] | [ ] | No |
| **How people join** | Added by team | Personal invitation | Waitlist / sign-up form | Marketing / open sign-up with a cap |
| **Gate to leave round** | Gate 0 | Gate 1 | Gate 2 | Gate 3 |

**Q6.2: What if a round goes badly? (Repeat the round, pause, or cancel?)**

> **Example:** "If Gate 1 fails, we fix the problems and repeat Round 1 with the same 25 people for 1 more week. We repeat at most twice. After that, the Business Owner decides whether to cancel or restructure."

**YOUR ANSWER:**

**Q6.3: How do we control how many people get in? (Invite codes, feature flags, waitlist, cap on sign-ups?)**

> **Example:** "Invite codes for Rounds 1-2. A hard cap in the sign-up system at 500 in Round 3. A feature flag lets us switch a feature off for everyone in under 5 minutes."

**YOUR ANSWER:**

---

# 7. TESTERS: WHO, HOW MANY, AND HOW TO ONBOARD THEM

**Q7.1: Describe your ideal tester. What types of people do you NEED to have?**

> **Example:** "10 parents with young kids, 5 grandparents (not tech-savvy), 5 teenagers, 5 people who use screen readers or have accessibility needs."

**YOUR ANSWER:**

| Tester type | Why we need them | Round 1 count | Round 2 count |
|---|---|---|---|
| | | | |

**Q7.2: Where will we find them?**

> **Example:** "Our email list (30 people), a parent forum post, 5 friends of the team."

**YOUR ANSWER:**

**Q7.3: What do we tell testers before they start? (Fill the welcome message.)**

> **Example:** "Welcome! You're helping us test TaskBuddy before launch. Please use it normally for 2 weeks. It may have bugs. Tell us anything confusing, not just broken things. This takes about 15 minutes a day. Questions? Email beta@taskbuddy.com."

**YOUR ANSWER:**

**Q7.4: What must testers agree to? (Tick all that apply.)**

- [ ] NDA / confidentiality
- [ ] Beta terms and conditions
- [ ] Privacy notice (what data we collect)
- [ ] Permission to record screens or sessions
- [ ] Permission to contact them for follow-up
- [ ] Other: [PLACEHOLDER]

**Q7.5: How will we thank testers? (Free months, gift card, early access, shout-out?)**

**YOUR ANSWER:**

**Q7.6: How many testers do we expect to drop out, and what is the plan?**

> **Example:** "Expect 30% to stop responding. Invite 35 to end up with 25 active testers."

**YOUR ANSWER:**

**Q7.7: How do testers get help if they are stuck?**

> **Example:** "Email beta@taskbuddy.com, answered within 4 working hours. A tester chat group is monitored 9am-6pm."

**YOUR ANSWER:**

---

# 8. ENTRY CRITERIA: "ARE WE READY TO START THIS ROUND?"

> **Rule:** Every box must be ticked **before** a round starts. If any box is not ticked, the round does not start. No exceptions without written approval from the Business Owner.

**Q8.1: What must be true before Round 0 (Internal) starts? Keep the standard rows and add your own.**

**YOUR ANSWER:**

- [ ] Development is "feature complete" for everything marked 🔴 in Section 5
- [ ] QA / system testing is finished and the QA Lead has approved the build
- [ ] No open 🔴 Critical bugs from QA
- [ ] Test environment is working and matches production setup
- [ ] Test data is loaded (see Section 10)
- [ ] Bug tracker is set up and the team knows how to use it
- [ ] Requirements and acceptance criteria (5.4) are approved
- [ ] This UAT Plan is approved by the Business Owner
- [ ] Other: [PLACEHOLDER]

**Q8.2: What extra must be true before Round 1 (Closed Beta) starts?**

- [ ] Gate 0 passed and signed
- [ ] 25 testers recruited, agreed to terms (7.4), and told when to start
- [ ] Feedback form and bug-reporting steps are tested and working
- [ ] Support channel is staffed (Section 18)
- [ ] Monitoring and error alerts are switched on (Section 20)
- [ ] Backup and rollback plan is written and tested (Section 21)
- [ ] Privacy and security checks passed (Section 13)
- [ ] Mobile test builds delivered (TestFlight / Play internal track), if applicable
- [ ] Other: [PLACEHOLDER]

**Q8.3: What extra must be true before Round 2 (Open Beta)?**

- [ ] Gate 1 passed and signed
- [ ] All 🔴 Critical and 🟠 High bugs from Round 1 fixed and re-tested
- [ ] Support team trained on the top 10 questions from Round 1
- [ ] Servers tested for 100+ people at the same time
- [ ] Sign-up waitlist and invite system working
- [ ] Other: [PLACEHOLDER]

**Q8.4: What extra must be true before Round 3 (Launch to 500)?**

- [ ] Gate 2 passed and signed
- [ ] Zero open 🔴 Critical bugs; any remaining 🟠 High bugs have a written workaround and a fix date
- [ ] Servers tested for at least 1,000 people at the same time (2x our goal)
- [ ] Billing and refunds tested with real (small) payments, if applicable
- [ ] App Store / Google Play approvals received, if applicable
- [ ] Help articles, FAQs and onboarding emails ready
- [ ] Legal pages ready: Terms of Service, Privacy Policy, Cookie notice
- [ ] 24/7 or agreed-hours on-call person named for the first 2 weeks
- [ ] Rollback plan practiced at least once
- [ ] Other: [PLACEHOLDER]

---

# 9. EXIT CRITERIA AND GO / NO-GO GATES

> **Rule:** Exit criteria must use **numbers**. "UAT is successful" is not a criterion. "At least 95% of 🔴 scenarios pass" is.
> **Important:** Agree on these numbers **now**, before testing starts, so nobody argues later.

**Q9.1: What numbers must be true to pass each gate? Suggested numbers are shown. Change them only for a good reason and write the reason.**

> **Example reason for change:** "We lowered the Round 0 pass rate to 90% because Round 0 is meant to find problems, not prove perfection."

**YOUR ANSWER:**

| Measure | Gate 0 (Internal) | Gate 1 (Closed, 25) | Gate 2 (Open, 100) | Gate 3 (500 customers) |
|---|---|---|---|---|
| 🔴 Must-work scenarios passed | 100% | 100% | 100% | 100% |
| 🟠 Should-work scenarios passed | 90% | 95% | 95% | 98% |
| Open 🔴 Critical bugs | 0 | 0 | 0 | 0 |
| Open 🟠 High bugs | Max 3 | Max 2 | Max 0 | Max 0 |
| Testers who finished the main journey | n/a | 80%+ | 85%+ | 90%+ |
| Crash-free sessions (mobile) | 97%+ | 98%+ | 99%+ | 99.5%+ |
| Page load / app response (95th percentile) | [e.g. under 4 s] | [e.g. under 3 s] | [e.g. under 3 s] | [e.g. under 2.5 s] |
| Tester satisfaction (1-5 average) | n/a | 3.8+ | 4.0+ | 4.2+ |
| Share of testers who would recommend it (NPS or yes/no) | n/a | [e.g. 40%+] | [e.g. 50%+] | [e.g. 55%+] |
| AI answers rated "good" by reviewers (skip if no AI) | 85%+ | 90%+ | 92%+ | 95%+ |
| AI answers flagged unsafe or harmful | 0 | 0 | 0 | 0 |
| Support tickets answered within target | n/a | 90%+ | 95%+ | 95%+ |
| Written sign-off obtained | Yes | Yes | Yes | Yes |
| **Your own extra measure:** | | | | |

**Q9.2: What is our rule for "suspending" testing? (Stop everything right away.)**

> **Example:** "We stop and tell everyone if: a bug exposes someone else's personal data; customers are charged wrongly; the app crashes for more than 10% of testers; the AI gives dangerous advice."

**YOUR ANSWER:**

**Q9.3: When can testing restart after a suspension?**

> **Example:** "After the Dev Lead fixes the cause, the QA Lead re-tests it, and the Business Owner approves the restart in writing."

**YOUR ANSWER:**

**Q9.4: What is the final launch success target, measured when the 500th customer joins?**

> **Example:** "500 customers signed up. 60%+ active in the last 7 days. Fewer than 2% raised a serious problem. Average rating 4.2+. Zero data leaks."

**YOUR ANSWER:**

---

# 10. TEST ENVIRONMENT AND TEST DATA

**Q10.1: Where will each round run?**

> **Example:** "Round 0: staging server. Rounds 1-3: real production with a feature flag so only invited people see it."

**YOUR ANSWER:**

| Item | Details |
|---|---|
| Web address(es) for testing | [PLACEHOLDER] |
| Is the environment separate from live? | [Yes / No - explain] |
| Which version/build is being tested? | [e.g. v1.0.0-rc2] |
| How do we deploy a fix? How long does it take? | [e.g. "Automatic pipeline, about 30 minutes"] |
| Who can change the environment? | [PLACEHOLDER] |
| Third-party services in test mode (payments, email, SMS, maps, AI model) | [PLACEHOLDER] |
| Is the environment stable enough to start? (Dev Lead confirms) | [ ] Yes |

**Q10.2: What test data do we need? (Fake users, sample products, sample files, etc.)**

> **Example:** "20 fake family accounts, 100 sample tasks, 5 expired accounts, 1 account with no data, 1 account with 10,000 tasks."

**YOUR ANSWER:**

**Q10.3: Are we using real customer data in testing? (Strongly prefer NO.)**

- [ ] No, only fake or anonymised data
- [ ] Yes: explain why, how it is protected and who approved: [PLACEHOLDER]

**Q10.4: What devices, browsers and operating systems must work? Pick the ones your real customers use.**

> **Example:** "Based on our analytics: Chrome (60%), Safari (30%), Edge (10%). iPhone 12 and newer, iOS 16+. Android: Samsung and Pixel, Android 12+."

**YOUR ANSWER (Web):**

| Browser | Minimum version | Desktop | Mobile | Priority |
|---|---|---|---|---|
| Chrome | | [ ] | [ ] | |
| Safari | | [ ] | [ ] | |
| Firefox | | [ ] | [ ] | |
| Edge | | [ ] | [ ] | |

**YOUR ANSWER (Mobile):**

| Platform | Device models to test | OS versions | Screen sizes | Priority |
|---|---|---|---|---|
| iOS | | | | |
| Android | | | | |

**Q10.5: What network conditions must be tested?**

> **Example:** "Fast Wi-Fi, slow 3G, going offline then back online, switching between Wi-Fi and mobile data."

**YOUR ANSWER:**

---

# 11. TEST SCENARIOS (WHAT TESTERS WILL ACTUALLY DO)

**Q11.1: List the user journeys testers must try. Think of the real stories of customers. Start with the "happy path" (everything goes right), then add "what if" paths.**

> **Example:**
> | ID | Journey | Type | Priority | Round |
> |---|---|---|---|---|
> | S-01 | New user signs up with email | Happy | 🔴 | 0,1,2,3 |
> | S-02 | User signs up with a wrong email format | Error | 🟠 | 0,1 |
> | S-03 | User forgets password and resets it | Happy | 🔴 | 0,1,2,3 |
> | S-04 | User loses internet while saving a task | Edge | 🟠 | 1,2 |
> | S-05 | User deletes account and data | Happy | 🔴 | 1,2,3 |

**YOUR ANSWER:**

| ID | Journey (plain words) | Type (Happy / Error / Edge) | Priority | Platform | Round(s) | Linked feature |
|---|---|---|---|---|---|---|
| S-01 | | | | | | |
| S-02 | | | | | | |
| S-03 | | | | | | |
| S-04 | | | | | | |
| S-05 | | | | | | |

**Minimum journeys to cover (tick the ones that apply, and add each to the table above):**

- [ ] Discover and sign up (including social login if offered)
- [ ] Verify email / phone
- [ ] First-time use and onboarding tutorial
- [ ] Main "core value" action of the product (the reason people use it)
- [ ] Create, edit, delete, search, share content
- [ ] Notifications and emails
- [ ] Settings and profile changes
- [ ] Payment, upgrade, downgrade, cancel, refund (if applicable)
- [ ] Log out and log in on another device
- [ ] Forgot password / account recovery
- [ ] Delete account and export my data
- [ ] Contact support / get help
- [ ] Uninstall and reinstall (mobile)
- [ ] Update the app to a newer version (mobile)
- [ ] Use with a screen reader, large text, or keyboard only
- [ ] Use in another language or region (if supported)

**Q11.2: Write the exact steps for each important scenario. Use the test-case card below. Copy it once per scenario, or keep one table.**

> **Example:**
> | Field | Value |
> |---|---|
> | Test case ID | TC-001 |
> | Scenario | S-01 New user signs up with email |
> | Priority | 🔴 |
> | Before you start | You have a new email address never used with TaskBuddy |
> | Steps | 1. Open the app. 2. Tap "Sign up". 3. Type your email and a password. 4. Tap "Create account". 5. Open the email we sent you. 6. Tap "Verify". |
> | Expected result | You see "Welcome!" and your empty task list within 3 seconds. |
> | Actual result | (tester fills this in) |
> | Pass / Fail | (tester fills this in) |
> | Bug ID if failed | (tester fills this in) |
> | Tester / Date / Device | (tester fills this in) |

**YOUR ANSWER (copy this card for each test case):**

| Field | Value |
|---|---|
| Test case ID | TC-[000] |
| Scenario ID | S-[00] |
| Priority | 🔴 / 🟠 / 🟡 |
| Before you start (needs) | |
| Steps (numbered, one action per step) | |
| Expected result (what should happen) | |
| Actual result (tester fills in) | |
| Pass / Fail (tester fills in) | |
| Bug ID if failed (tester fills in) | |
| Tester / Date / Device (tester fills in) | |

**Q11.3: How will we track progress of all test cases?**

> **Example:** "A spreadsheet with one row per test case and columns: ID, status (Not started / Passed / Failed / Blocked), tester, date. Updated daily by the UAT Lead."

**YOUR ANSWER:**

**Q11.4: Besides following steps, will testers be allowed to explore freely?**

> **Example:** "Yes. In Rounds 1-2, testers spend 30 minutes using the app any way they like and report anything odd."

**YOUR ANSWER:**

---

# 12. SPECIAL CHECKS FOR AI-POWERED FEATURES

> **Skip this section only if the product has no AI features.** Then write: `N/A - no AI features`.

**Q12.1: List every AI feature and what it is supposed to do.**

> **Example:** "AI Task Helper: suggests 3 tasks based on the family's calendar. Must never suggest anything unsafe for children."

**YOUR ANSWER:**

| AI feature | What it should do | What it must NEVER do | Model / vendor | Owner |
|---|---|---|---|---|
| | | | | |

**Q12.2: How will we judge whether AI answers are good? Define a simple score.**

> **Example:** "Reviewers read 100 AI answers and mark each: Good (helpful and correct), OK (usable), Bad (wrong, confusing or unsafe). Goal: 90%+ Good, 0 unsafe."

**YOUR ANSWER:**

**Q12.3: Which AI risks will we test? Tick each and describe how.**

| Risk | Tested? | How we test it | Pass rule |
|---|---|---|---|
| Wrong or made-up facts (hallucination) | [ ] | | |
| Harmful, rude or biased answers | [ ] | | |
| Leaking private data or hidden instructions | [ ] | | |
| Tricked by users ("ignore your rules") | [ ] | | |
| Answers in the wrong language / tone | [ ] | | |
| Gives different answers to the same question (inconsistent) | [ ] | | |
| Too slow (response time) | [ ] | | |
| Too costly (cost per user per day) | [ ] | | |
| What happens when the AI service is down | [ ] | | |
| Users can report a bad AI answer easily | [ ] | | |
| Clear message that the answer is AI-generated | [ ] | | |

**Q12.4: What is our "AI test set"? (A fixed list of questions we ask after every change to compare results.)**

> **Example:** "A file called ai_test_set.csv with 100 questions: 60 normal, 20 tricky, 20 attempts to break the rules. Expected answers written by the Product Owner."

**YOUR ANSWER:**

**Q12.5: What is the fallback if AI fails or behaves badly?**

> **Example:** "The feature is switched off by a feature flag within 5 minutes. Users see 'Suggestions are resting. Add tasks yourself.'"

**YOUR ANSWER:**

**Q12.6: Who is allowed to change AI prompts, models or settings during UAT?**

> **Example:** "Only the AI Owner, with a note in the change log. Every change means we re-run the AI test set."

**YOUR ANSWER:**

---

# 13. NON-FUNCTIONAL ACCEPTANCE: SPEED, SAFETY, ACCESS, PRIVACY

**Q13.1: For each topic, what must be true, and who checks it? Replace the example numbers with yours.**

> **Example (speed):** "Pages load in under 3 seconds for 95% of visits. Checked by the Dev Lead using a load tool."

**YOUR ANSWER:**

| Topic | What must be true (use numbers) | Who checks | Done |
|---|---|---|---|
| **Speed** | | | [ ] |
| **Handles many users** (how many at the same time?) | | | [ ] |
| **Security** (login safe, no one sees others' data, no known serious weaknesses) | | | [ ] |
| **Privacy** (consent, data deletion, only collect what we need) | | | [ ] |
| **Legal** (terms, privacy policy, age limits, regional rules like GDPR/CCPA) | | | [ ] |
| **Accessibility** (screen reader, colour contrast, keyboard use, large text) | | | [ ] |
| **Reliability** (uptime goal, e.g. 99.5%) | | | [ ] |
| **Backup and restore** (can we restore data? how fast?) | | | [ ] |
| **Compatibility** (devices, browsers, OS versions in 10.4) | | | [ ] |
| **Payments** (correct charge, refund, failed card, tax) | | | [ ] |
| **Mobile store rules** (App Store / Google Play review guidelines) | | | [ ] |
| **Language and content** (spelling, wording, local formats) | | | [ ] |
| **Battery / data use** (mobile) | | | [ ] |

---

# 14. HOW WE COLLECT FEEDBACK

**Q14.1: How can a tester report a problem or an idea? Make it as easy as possible: one tap or one link.**

> **Example:** "A 'Send feedback' button in the app opens a form with 4 fields (what happened, what you expected, a screenshot, how bad it is). A shake gesture on mobile opens the same form."

**YOUR ANSWER:**

**Q14.2: What do we ask in the daily/weekly survey? Keep it under 2 minutes. Examples are given; replace them.**

> **Example questions:**
> 1. What did you try today?
> 2. Did you get stuck anywhere? (Yes/No, describe)
> 3. How easy was it to use? (1 = very hard, 5 = very easy)
> 4. What is ONE thing we should fix first?
> 5. How would you feel if you could not use this tomorrow? (Very upset / A bit upset / Not bothered)

**YOUR ANSWER:**

**Q14.3: What information MUST every bug report contain?**

- [ ] What did you do? (steps)
- [ ] What did you expect?
- [ ] What actually happened?
- [ ] Screenshot or screen recording
- [ ] Device, browser or phone model, and OS version
- [ ] App/build version
- [ ] Date and time
- [ ] How bad is it for you? (Blocks me / Annoying / Small)
- [ ] Other: [PLACEHOLDER]

**Q14.4: Who reads the feedback, how often, and how do we answer testers?**

> **Example:** "Support Lead reads new feedback twice a day. Every report gets a 'Thanks, we got it' within 1 working day. Fixed items are announced in the weekly tester newsletter."

**YOUR ANSWER:**

**Q14.5: How do we separate "bug" from "new idea"?**

> **Example:** "A bug = it does not do what the requirements say. A new idea = it works as written, but someone wants something different. Ideas go to the 'Later' backlog; the Product Owner reviews them every Friday."

**YOUR ANSWER:**

---

# 15. DEFECT (BUG) MANAGEMENT

**Q15.1: How bad is each bug? Confirm or change the standard definitions.**

**YOUR ANSWER:**

| Severity | Meaning | Real examples | Must be fixed by |
|---|---|---|---|
| 🔴 **Critical** | Product unusable, data lost or leaked, money wrong, safety risk | App crashes at launch; double charges; users see others' data | Before the next gate. Testing may pause. Start fixing right away. |
| 🟠 **High** | A main feature is broken and there is no easy workaround | Cannot create a task; reminders never arrive | Before the next gate, or written workaround approved by Product Owner |
| 🟡 **Medium** | A feature is partly broken but there is a workaround | Search is slow; one screen layout is off on small phones | Before launch if possible, else the first update |
| 🟢 **Low** | Small or cosmetic problem | Typo; slightly wrong colour | When time allows |

**Q15.2: How fast must each severity be answered and fixed? (Service targets)**

> **Example:** "Critical: acknowledge in 1 hour, fix in 24 hours. High: acknowledge in 4 hours, fix in 3 days."

**YOUR ANSWER:**

| Severity | Acknowledge within | Fix within | Re-test within |
|---|---|---|---|
| 🔴 Critical | | | |
| 🟠 High | | | |
| 🟡 Medium | | | |
| 🟢 Low | | | |

**Q15.3: What are the steps a bug travels through?**

> **Example:** "New -> Confirmed -> Assigned -> Fixed -> Ready to re-test -> Verified (closed) OR Reopened. Also: Won't fix (with reason) or Duplicate."

**YOUR ANSWER:**

**Q15.4: Who decides to NOT fix a bug? What do they write down?**

> **Example:** "Product Owner decides. They write: the bug ID, why we won't fix it, the risk, and the date. The Business Owner is told about any 🟠 High bug we leave open."

**YOUR ANSWER:**

**Q15.5: Bug log template (copy one row per bug).**

| Bug ID | Date | Reported by | Round | Feature / Scenario | Summary | Steps | Expected | Actual | Severity | Priority | Owner | Status | Fix build | Verified by | Date closed |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| BUG-001 | | | | | | | | | | | | | | | |

**Q15.6: How do we handle duplicates, "cannot reproduce" and "works for me" bugs?**

> **Example:** "Duplicates are merged into the oldest bug; the reporter is thanked. 'Cannot reproduce' bugs go back to the reporter with a request for a recording. If there is no reply in 5 days, we close them with a note."

**YOUR ANSWER:**

---

# 16. SCHEDULE

**Q16.1: What are the key dates? Work backwards from the launch date and add buffer time (at least 20% extra).**

> **Example:** "Launch to 500: 2027-01-12. Round 2 must end 2027-01-05. Buffer of 3 days at each gate."

**YOUR ANSWER:**

| Milestone | Start | End | Owner | Depends on |
|---|---|---|---|---|
| UAT Plan approved | | | | |
| Test environment ready | | | | |
| Test cases written and reviewed | | | | |
| Round 0: Internal | | | | |
| **Gate 0 decision meeting** | | | | |
| Recruit and onboard 25 testers | | | | |
| Round 1: Closed Beta (25) | | | | |
| Fix and re-test Round 1 bugs | | | | |
| **Gate 1 decision meeting** | | | | |
| Open waitlist, onboard 100 testers | | | | |
| Round 2: Open Beta (100) | | | | |
| Fix and re-test Round 2 bugs | | | | |
| **Gate 2 decision meeting** | | | | |
| Launch readiness check (Section 21) | | | | |
| Round 3: Launch to 500 | | | | |
| **Gate 3 final review and sign-off** | | | | |
| Lessons-learned meeting | | | | |

**Q16.2: What fixed dates cannot move? (Holidays, store review time, marketing events, contracts)**

**YOUR ANSWER:**

**Q16.3: How often will the team meet during testing?**

> **Example:** "Daily 15-minute stand-up during Rounds 1-3. Weekly review with the Business Owner on Fridays."

**YOUR ANSWER:**

---

# 17. HOW WE TALK TO EACH OTHER (COMMUNICATION PLAN)

**Q17.1: Who gets which update, how often, and from whom?**

> **Example:** "Daily status to the team via chat at 5pm. Weekly summary to the Business Owner every Friday. Immediate alert to the Business Owner for any Critical bug."

**YOUR ANSWER:**

| What | To whom | Channel | How often | Sent by |
|---|---|---|---|---|
| Daily status | Project team | | Daily | |
| Weekly summary | Business Owner and sponsors | | Weekly | |
| Critical-problem alert | Business Owner, Dev Lead, Support Lead | | Immediately | |
| Tester newsletter | Testers | | Weekly | |
| Gate decision announcement | Everyone involved | | At each gate | |
| Customer notice (e.g. outage) | Affected customers | | When needed | |

**Q17.2: If something serious happens, who is called first, second and third?**

> **Example:** "1. On-call developer. 2. Dev Lead. 3. Business Owner. Phone first, then chat."

**YOUR ANSWER:**

| Order | Name | Phone / contact | When to call |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

# 18. SUPPORT PLAN FOR TESTERS AND CUSTOMERS

**Q18.1: Who answers questions, at what hours, and how fast?**

> **Example:** "Two support staff, 9am-6pm weekdays. First reply within 4 working hours. After hours: auto-reply with help link; Critical issues call the on-call developer."

**YOUR ANSWER:**

**Q18.2: What help material must exist before Round 3?**

- [ ] FAQ (top 10 questions)
- [ ] "Getting started" guide or video
- [ ] Known-issues page
- [ ] Contact page and support email
- [ ] In-app help or tips
- [ ] Support team cheat sheet with standard answers
- [ ] Other: [PLACEHOLDER]

**Q18.3: How many support requests do we expect per 100 users per week? (Estimate, then compare with real numbers.)**

> **Example:** "About 15 per 100 users in the first week, falling to 5."

**YOUR ANSWER:**

---

# 19. RISKS AND WHAT WE WILL DO ABOUT THEM

**Q19.1: What could go wrong? List at least 8. For each, rate the Chance (Low / Medium / High) and the Impact (Low / Medium / High), then write what we will do to prevent it and what we will do if it happens anyway.**

> **Example:**
> | Risk | Chance | Impact | Prevent | If it happens |
> |---|---|---|---|---|
> | Not enough testers sign up | Medium | High | Recruit 40% extra; ask friends and early fans | Extend recruitment by one week; Business Owner informed |
> | App Store review is slower than planned | High | High | Submit builds 3 weeks early | Launch web first; mobile later |

**YOUR ANSWER:**

| # | Risk | Chance | Impact | How we prevent it | Plan if it happens | Owner |
|---|---|---|---|---|---|---|
| 1 | Not enough testers | | | | | |
| 2 | Critical bug found late | | | | | |
| 3 | Test environment unstable | | | | | |
| 4 | Key person unavailable | | | | | |
| 5 | Servers cannot handle the load | | | | | |
| 6 | Data leak or privacy mistake | | | | | |
| 7 | Store (App Store / Google Play) rejection or delay | | | | | |
| 8 | AI gives unsafe or wrong answers | | | | | |
| 9 | Testers give feedback too slowly or not at all | | | | | |
| 10 | Third-party service (payments, email, AI model) fails | | | | | |
| 11 | Scope grows during testing ("one more feature") | | | | | |
| 12 | Add your own: | | | | | |

---

# 20. HOW WE WATCH THE PRODUCT (METRICS AND MONITORING)

**Q20.1: Which numbers do we watch every day? Choose from the list and add a "warning level" (when we get worried) and a "stop level" (when we pause).**

> **Example:** "Crash-free sessions: warning below 99%, stop below 97%."

**YOUR ANSWER:**

| Metric | Where we see it | Target | Warning level | Stop level | Checked by |
|---|---|---|---|---|---|
| Sign-ups completed (of those started) | | | | | |
| Users who finish the main journey | | | | | |
| Active users (daily / weekly) | | | | | |
| Came back after 1 day / 7 days / 14 days | | | | | |
| Crash-free sessions | | | | | |
| Error rate (server) | | | | | |
| Page / app speed (95th percentile) | | | | | |
| Server uptime | | | | | |
| Support tickets per 100 users | | | | | |
| Bugs open by severity | | | | | |
| Tester / customer satisfaction | | | | | |
| Payment failures (if applicable) | | | | | |
| AI answer quality and cost (if applicable) | | | | | |
| App-store rating (if applicable) | | | | | |
| Cost per user | | | | | |

**Q20.2: Which automatic alerts are set up, and who receives them?**

> **Example:** "Alert to the on-call phone if the error rate is above 2% for 5 minutes."

**YOUR ANSWER:**

**Q20.3: How do we count to 500? (Define what counts as "a customer who used the product".)**

> **Example:** "A customer = a person who signed up, verified their email, and completed the main journey at least once. Internal team members and test accounts are NOT counted."

**YOUR ANSWER:**

**Q20.4: How will we track the number of customers over time?**

> **Example:** "Dashboard 'Customer count' updated hourly. UAT Lead posts the number each morning."

**YOUR ANSWER:**

---

# 21. LAUNCH READINESS, ROLLBACK AND "WHAT IF IT GOES WRONG"

**Q21.1: Final launch checklist. Tick each item the day before Round 3. Add your own.**

- [ ] Gate 2 signed by the Business Owner
- [ ] Production environment matches the tested environment
- [ ] All 🔴 and 🟠 bugs closed or accepted in writing
- [ ] Load test passed at 2x expected users (1,000 or more)
- [ ] Security and privacy checks signed off
- [ ] Backups run and a test restore succeeded
- [ ] Monitoring dashboards live; alerts tested
- [ ] On-call schedule for the first 14 days published
- [ ] Support team trained; help articles live
- [ ] Legal pages live (Terms, Privacy, Cookies)
- [ ] Payments tested with real small charges and refunds (if applicable)
- [ ] App Store / Google Play listings approved (if applicable)
- [ ] Feature flags tested (we can switch features off)
- [ ] Communication messages ready (launch email, outage notice, apology template)
- [ ] Rollback rehearsed
- [ ] Team knows the stop levels (20.1)
- [ ] Other: [PLACEHOLDER]

**Q21.2: What is the rollback plan? (How do we go back to the safe version?)**

> **Example:** "Web: redeploy the last good version with one click (about 10 minutes). Mobile: switch off new features by feature flag; if needed, pause the staged rollout in the store and publish a fix. Database changes are reversible: the Dev Lead has a tested undo script."

**YOUR ANSWER:**

| Question | Answer |
|---|---|
| Who may order a rollback? | |
| How long does it take? | |
| What happens to new data created since the release? | |
| How do we tell customers? | |
| Who confirms the rollback worked? | |

**Q21.3: How do we release to the 500 slowly and safely? (Staged rollout)**

> **Example:** "Day 1: 50 customers. Day 3: 150. Day 7: 300. Day 14: 500. We only move to the next step if the numbers in 20.1 are above the warning level."

**YOUR ANSWER:**

| Step | Customers allowed | Date | Condition to move on |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 (final) | 500 | | |

**Q21.4: What is the plan for the first 48 hours and first 14 days after launch to 500?**

> **Example:** "First 48 hours: two developers online, check dashboards every hour, daily stand-up at 9am. Days 3-14: check dashboards twice daily, weekly review."

**YOUR ANSWER:**

---

# 22. SIGN-OFF (FORMAL APPROVAL)

> **Why this matters:** A spoken "looks good" is not proof. A signed record protects everybody.

**Q22.1: Who must sign at each gate? (At minimum the Business Owner.)**

**YOUR ANSWER:**

| Gate | Signer name | Role | Must sign? |
|---|---|---|---|
| Gate 0 | | Business Owner | Yes |
| Gate 0 | | QA Lead | Yes |
| Gate 1 | | Business Owner | Yes |
| Gate 1 | | Product Owner | Yes |
| Gate 2 | | Business Owner | Yes |
| Gate 2 | | Dev Lead | Yes |
| Gate 3 | | Business Owner | Yes |
| Gate 3 | | Security / Privacy Owner | Yes |
| Gate 3 | | Support Lead | Yes |

**Q22.2: What does each signer confirm? Copy this form for every gate. (Humans only, never AI agents.)**

> **Example statement:** "I confirm that Round 1 is complete, the results are shown below, the open issues are listed and accepted, and we may move to Round 2."

**YOUR ANSWER (copy once per gate):**

**GATE [0 / 1 / 2 / 3] SIGN-OFF FORM**

| Item | Details |
|---|---|
| Round name | |
| Dates | From [ ] to [ ] |
| Build / version tested | |
| Test cases: planned / run / passed / failed / blocked | [ ] / [ ] / [ ] / [ ] / [ ] |
| Pass rate for 🔴 and 🟠 scenarios | |
| Bugs found / fixed / still open (by severity) | |
| Open bugs we accept, with reasons and workarounds | |
| Exit criteria from Section 9 met? | [ ] Yes, all  [ ] Partly (list what is missing)  [ ] No |
| Number of active testers and key feedback summary | |
| Known risks going forward | |
| **Decision** | [ ] GO   [ ] GO with conditions (list)   [ ] NO-GO |
| Conditions or next steps | |

| Name | Role | Decision | Signature | Date |
|---|---|---|---|---|
| | | | | |
| | | | | |

**Q22.3: How is sign-off stored? (Where? Who can see it?)**

> **Example:** "Signed PDFs in the shared drive folder 'UAT / Sign-offs'. Link posted in the project channel."

**YOUR ANSWER:**

---

# 23. AFTER THE FIRST 500: FINAL REPORT AND LESSONS LEARNED

**Q23.1: When do we write the final UAT report? (Suggested: within 5 working days of reaching 500 customers.)**

**YOUR ANSWER:**

**Q23.2: What goes into the final report?**

- [ ] Summary of all four rounds
- [ ] Number of testers and customers reached
- [ ] Test cases planned / run / passed
- [ ] All bugs found, fixed and still open
- [ ] Results against every exit-criteria number in Section 9
- [ ] Customer satisfaction and retention numbers
- [ ] Support ticket summary
- [ ] AI quality results (if applicable)
- [ ] Incidents and rollbacks (what happened and how we fixed it)
- [ ] Top 5 things that went well
- [ ] Top 5 things to improve
- [ ] Recommendations for the next release and for the next 500 customers
- [ ] Final sign-off

**Q23.3: Lessons-learned meeting. Answer these after the launch.**

| Question | Answer |
|---|---|
| What went better than we expected? | |
| What was harder than we expected? | |
| Which bugs should we have found earlier? Why did we miss them? | |
| Were our exit-criteria numbers realistic? | |
| Was the number of testers right? | |
| Did the schedule have enough buffer? | |
| What would we change in this template? | |
| What should we automate next time (including with AI agents)? | |

**Q23.4: When does UAT officially end, and what happens to the testers and test accounts?**

> **Example:** "UAT ends when the final report is signed. Testers are thanked and moved to the normal customer base. Test accounts are deleted within 30 days."

**YOUR ANSWER:**

---

# APPENDIX A: DAILY STATUS REPORT (COPY EVERY DAY DURING TESTING)

```
UAT DAILY STATUS: [DATE]
Round: [0 / 1 / 2 / 3]        Day [x] of [y]

OVERALL MOOD:  [GREEN = on track | AMBER = at risk | RED = blocked]

PEOPLE
- Active testers today: [n] of [n] invited
- Customers in product (Round 3): [n] / 500

PROGRESS
- Test cases: planned [n] | run [n] | passed [n] | failed [n] | blocked [n]
- Pass rate for must-work (🔴) scenarios: [n]%

BUGS TODAY
- New: 🔴 [n]  🟠 [n]  🟡 [n]  🟢 [n]
- Fixed and verified: [n]
- Still open: 🔴 [n]  🟠 [n]  🟡 [n]  🟢 [n]

KEY NUMBERS (from Section 20)
- Crash-free sessions: [n]%   Error rate: [n]%   Speed (95th pct): [n]s
- Support tickets: [n]   Satisfaction: [n]/5

TOP 3 PROBLEMS RIGHT NOW
1.
2.
3.

BLOCKERS AND WHO CAN UNBLOCK THEM
-

PLAN FOR TOMORROW
-

DECISIONS NEEDED FROM A HUMAN
-
```

---

# APPENDIX B: GATE DECISION MEETING AGENDA (30 MINUTES)

1. (5 min) UAT Lead presents results against the Section 9 numbers
2. (5 min) Dev Lead presents open bugs and fix plans
3. (5 min) Support Lead presents tester/customer feedback
4. (5 min) Security / Privacy and AI Owners report any concerns
5. (5 min) Risks for the next round
6. (5 min) Business Owner decides: **GO / GO with conditions / NO-GO**. Decision is written in the sign-off form (Section 22).

---

# APPENDIX C: TESTER WELCOME CHECKLIST (SEND TO EACH TESTER)

- [ ] I understand this is a test and there may be bugs
- [ ] I agreed to the terms (7.4)
- [ ] I installed the app / opened the web link
- [ ] I know how to send feedback
- [ ] I know who to contact for help
- [ ] I know how long to test and when the round ends
- [ ] I tried the first 3 scenarios

---

# APPENDIX D: SIMPLE CHANGE-CONTROL LOG

Use this when scope, dates, exit criteria or AI settings change during UAT.

| # | Date | What changed | Why | Who approved | Impact on schedule / risk |
|---|---|---|---|---|---|
| 1 | | | | | |

---

# FINAL QUALITY CHECK: IS THIS PLAN READY TO USE?

Tick every box. If you cannot tick one, go back and fix it.

- [ ] No `[PLACEHOLDER]` text is left
- [ ] Every question has an answer, `N/A - reason`, or `TBD - who, by when`
- [ ] Every number has a unit (seconds, %, people)
- [ ] Every role has a named person AND a backup
- [ ] Scope has both "tested" and "not tested" lists
- [ ] Every 🔴 feature has at least one scenario and one test case
- [ ] Exit criteria use numbers, not feelings
- [ ] Dates include buffer time
- [ ] Rollback plan exists and someone has practiced it
- [ ] AI risks are covered (or marked N/A)
- [ ] Privacy and legal items are covered
- [ ] A 10-year-old (or a new team member) could read this and understand what to do next
- [ ] The Business Owner has read and approved this plan
- [ ] This plan is saved in the shared folder: `Testing and quality assurance/UAT_Plan.md`

---

*End of UAT Plan template. Version 1.0. Update the version number in Section 1 whenever you change this document.*
