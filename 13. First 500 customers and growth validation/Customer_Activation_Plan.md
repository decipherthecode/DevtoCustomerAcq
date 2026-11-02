# HOW TO FILL IN THIS DOCUMENT (READ THIS FIRST)

**What is this file?**
This is a *Customer Activation Plan*. It is one file that walks you from "I have an idea" all the way to "500 real customers are using my product." You fill it in by answering questions. No specialist knowledge is required: each question is written in plain language, with a hint and an example.

**Who is it for?** Solo founders and small teams building a **SaaS / web app**, a **mobile app**, or a **marketplace / community** with AI assisting the build. Copy this file for every new project.

**How long does it take?** About 4-6 hours for a first pass, ideally across several sittings. Version 1 is allowed to be imperfect; it is improved as you learn.

---

**Template version:** 1.0  (this is the version of the blank template, not of your project; your project version goes in Part 0)

**Where to find help while filling:**
- Unsure what a word means: **Appendix A (Glossary)**
- Want to see a finished example for your product type: **Appendix E (Worked Examples)**
- Unsure what number to aim for: **Appendix G (Starting Targets)**
- Using AI to fill or run this plan: **Appendix F (AI-Agent Protocol and Prompt Pack)**
- Short on time: **Appendix B (30-Minute Quick Fill)**

## Words that are easy to misread

| If you read... | It means... | It does NOT mean... |
|---|---|---|
| "Customer" | Whatever you chose in Q5.1 (we recommend *activated* users) | Anyone who merely signed up |
| "Activated" | Reached the aha moment you define in Q6.4 | Created an account, or clicked around |
| "Gate" | A checkpoint with a pass/fail rule | A suggestion you may skip |
| "UNKNOWN" | An honest gap with a plan to close it | A failure |
| "Human approval" | A named person says "yes" in writing | An AI agent approving its own work |
| "Per period" | State the period: day, week, month, year | "Regularly" |

## The 10 Filling Rules

1. **Go in order.** Start at Part 0 and go down. Later parts use your earlier answers.
2. **Answer every question.** Never leave an answer empty. Use one of these three allowed answers:
   - a real answer, or
   - `N/A: <reason>` (for example, `N/A: my product has no free plan`), or
   - `UNKNOWN: I will find out by <date> by doing <action>`.
3. **Write one fact per line.** Short sentences. No paragraphs.
4. **Use numbers, not feelings.** Write "20 customers," not "a lot." Write "within 7 days," not "soon."
5. **Always add units and dates.** Dates look like `2026-10-19`. Money looks like `USD 49/month`.
6. **Mark assumptions.** If you are estimating, put `(GUESS)` after it. Replace guesses with facts as you learn them.
7. **Replace the examples.** Lines marked *Example* only show the style. Do not leave them in your final answer.
8. **Only fill what matches your product.** Sections marked *Conditional* can be skipped with `N/A`.
9. **Do not delete questions.** Write under them. This keeps the template reusable and checkable.
10. **Finish with Part 9 (Final Check).** The document is "done" only when the checklist there is all ticked.

## What the symbols mean

| Label | Meaning |
|---|---|
| **Q#.#** | A numbered question. The number never changes, so other documents can refer to it |
| **Hint** | Guidance if you feel stuck |
| *Example* | A made-up example showing the expected style. Replace it |
| **Your answer** | The place to write your answer |
| `[ ]` / `[x]` | An empty / ticked checkbox. Change `[ ]` to `[x]` to tick |
| **GATE** | A checkpoint: do not move forward until it is passed |
| **AI** | A step an AI agent may perform (a human still approves anything marked "human") |
| **Conditional** | Fill in only if it matches your product type; otherwise write `N/A` |

## How to fill a "pick one" question
Change `[ ]` to `[x]` next to exactly one choice, unless it says "pick all that apply."

## If an AI agent is filling this in for you
- Never invent numbers, quotes, or customer names. Write `UNKNOWN:` and say how to find out.
- Mark every assumption with `(GUESS)`.
- Do not change question IDs (like `Q6.2`). Other documents may point to them.
- Keep the same headings. Only write in the **Your answer:** lines or tables.
- After filling, run Part 9 and report what is still `UNKNOWN`.
- A human must approve anything touching money, legal text, security, or what gets sent to customers.

## How the whole journey fits together

```
PART 1  VALIDATE      Is the problem real and who has it?
PART 2  DEFINE        What does "activated" mean for my product?
PART 3  BUILD WITH AI Which AI agents do what, and where do humans check?
PART 4  PROVE QUALITY Test it, beta it, decide Go / No-Go
PART 5  LAUNCH & GROW Find customers #1 to #500
PART 6  MEASURE       Numbers, experiments, and when to stop or pivot
PART 7  PROTECT       Risks, legal, privacy, support
PART 8  MANAGE        Budget, team roles, decisions, open questions
PART 9  FINAL CHECK   Is this document ready to use?
```

---

# PART 0: DOCUMENT CONTROL

| Field | Your answer |
|---|---|
| Project name | |
| Document version (start at `0.1`) | |
| Owner (one named person) | |
| Other contributors | |
| Date started (`YYYY-MM-DD`) | |
| Date last updated (`YYYY-MM-DD`) | |
| Status (pick one: Draft / In review / Approved / Archived) | |
| Where is the product's code and files kept? (link or folder) | |

**Change log** (add a row every time you edit in a big way)

| Version | Date | Who | What changed |
|---|---|---|---|
| 0.1 | | | First draft |

---

# PART 1: VALIDATE (Is this worth building and who is it for?)

## 1. Project Snapshot

**Q1.1 In one sentence, what does your product do?**
**Hint:** Fill in: "My product helps **[who]** do **[what]** so they can **[result]**."
*Example: "My product helps freelance designers send invoices in 30 seconds so they get paid faster."*
**Your answer:**

**Q1.2 What type of product is it? (pick all that apply)**
- [ ] SaaS / web app
- [ ] Mobile app (iOS / Android)
- [ ] Marketplace / community (two sides: people who give and people who get)

**Q1.3 How will it make money? (pick all that apply)**
- [ ] Free / freemium (free plan, paid upgrades)
- [ ] Free trial, then paid
- [ ] Paid from day one
- [ ] Usage-based or marketplace fees (you earn when people use it or trade)
- [ ] Not decided yet → write `UNKNOWN` and finish Q9.1

**Q1.4 Which stage are you in today? (pick one)**
- [ ] Idea only
- [ ] Prototype or design exists
- [ ] Building with AI now
- [ ] In beta
- [ ] Launched, fewer than 500 customers
- [ ] Other: ______

**Q1.5 What is your target launch date and your target date for customer #500?**
**Your answer:** Launch: `____-__-__`   Customer #500: `____-__-__`

## 2. The Customer

**Q2.1 Who is your *first* ideal customer? Describe ONE type of person or business.**
**Hint:** If you write "everyone," you have not chosen yet. Pick one small group.
*Example: "Solo freelance graphic designers in the US who invoice 5 or more clients per month."*
**Your answer:**

**Q2.2 Fill in this card for that customer.**

| Item | Your answer |
|---|---|
| Job or role | |
| Age range / company size (if a business) | |
| Country or region | |
| Tools they use today | |
| Where they spend time online (sites, groups, apps) | |
| Who decides to buy? Who pays? | |

**Q2.3 What are their top 3 problems, in their own words?**
**Hint:** Use real words people said, not words you invented.
1. **Your answer:**
2. **Your answer:**
3. **Your answer:**

**Q2.4 What do they do today instead of using your product?** (spreadsheet, a competitor, nothing, asking friends…)
**Your answer:**

**Q2.5 How painful is the problem? (pick one)**
- [ ] Mild: they complain but live with it
- [ ] Medium: they lose time or money every week
- [ ] Severe: they are actively searching for a fix right now

## 3. Problem and Promise

**Q3.1 State the problem in one sentence a 10-year-old could understand.**
**Your answer:**

**Q3.2 State your promise: what changes for the customer after using your product?**
*Example: "Before: 20 minutes per invoice. After: 30 seconds."*
**Your answer:** Before: &nbsp; After:

**Q3.3 Why now? What changed that makes this possible or needed today?**
**Your answer:**

**Q3.4 Who are your 3 closest alternatives or competitors, and why would customers pick you?**

| Alternative | Their weakness | Your advantage |
|---|---|---|
| | | |
| | | |
| | | |

## 4. Validation Evidence

**GATE 1: Do not start building until this section is complete, or you have written a reason to skip it.**

**Q4.1 How many real customer conversations have you had? (Friends being polite do not count.)**
**Your answer:** Number: ____  Goal before building: at least **10**

**Q4.2 Log your conversations.**

| # | Date | Who (role, not private name) | Biggest pain they said | Would they use/pay? (Yes / Maybe / No) | Quote (short) |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |
| 9 | | | | | |
| 10 | | | | | |

**Q4.3 Any other proof of demand?** (waitlist signups, pre-orders, survey results, search volume)
**Your answer:** Type and number:

**Q4.4 Gate 1 result (pick one)**
- [ ] PASS: at least 5 of 10 said "Yes" and the pain is Medium or Severe
- [ ] PARTIAL: talk to more people and fix the idea (date to retry: ______)
- [ ] FAIL: change the customer or the problem (write what you will change: ______)

## 5. Success Definition and the 500 Goal

**Q5.1 What does "customer" mean in this plan? (pick one)**
- [ ] Someone who signed up
- [ ] Someone who is **activated** (reached the "aha" moment in Part 2)
- [ ] Someone who paid
- [ ] Other: ______

**Hint:** We strongly recommend **activated**. Signups alone can fool you.

**Q5.2 Your North Star metric: the ONE number that shows customers are getting real value.**
*Examples: "invoices sent per week," "rides completed," "workouts logged," "successful trades per month."*
**Your answer:**

**Q5.3 What will be true when you hit 500 customers?** (revenue, retention, reviews, anything else)
**Your answer:**

---

# PART 2: DEFINE "ACTIVATED" (the most important part)

> **Plain-English idea:** A person is *activated* when they get the **first real taste of the value you promised**. Not when they sign up. Not when they click around. When the promise (Q3.2) comes true for them.

## 6. Define Your Three Moments

```
Sign up  →  SETUP moment  →  AHA moment  →  HABIT moment  →  Loyal customer
```

**6A. SETUP moment: "I am ready to try it."**
**Q6.1 What is the smallest set of steps a new person MUST do before they can get value?**
**Hint:** Fewer is better. Anything not needed for the first win can wait until later.
*Example: "Create account → add 1 client."*
**Your answer:**

**Q6.2 Which setup steps can you remove, delay, or do for them automatically?**
**Your answer:**

**6B. AHA moment: "Wow, this works!"**
**Q6.3 Pick the example closest to your product, or write your own.**

| Product type | Menu of example aha moments (pick one or adapt) |
|---|---|
| SaaS / web app | [ ] Sent first invoice  [ ] Created and shared first report  [ ] Finished first project  [ ] Invited first teammate AND used it together  [ ] Connected a data source and saw results |
| Mobile app | [ ] Completed first workout / lesson / order  [ ] Got first useful notification AND acted on it  [ ] Finished first session of 3+ minutes of real use |
| Marketplace / community | **Buyer side:** [ ] Completed first purchase/booking  **Seller/provider side:** [ ] Got first order/booking  [ ] First successful match |
| Other | [ ] ______ |

**Q6.4 Write your final activation event as ONE exact sentence a computer could count.**
(See Appendix E for finished examples for SaaS, mobile, and marketplace products.)
**Hint:** Format: "A user is activated when they **[action]** within **[X days]** of signing up."
*Example: "A user is activated when they send 1 invoice within 7 days of signing up."*
**Your answer:**

**Q6.5 What is your time limit for becoming activated? (pick one)**
- [ ] Same session (under 10 minutes)
- [ ] Within 24 hours
- [ ] Within 7 days
- [ ] Within 14 days
- [ ] Within 30 days
- [ ] Other: ______

**Q6.6 Is this event easy to measure in your product data? (pick one)**
- [ ] Yes, I can count it today
- [ ] Not yet, I must add tracking (add to Part 3, Section 14)
- [ ] I'm not sure → ask a developer or AI agent to check

**6C. HABIT moment: "I keep coming back."**
**Q6.7 What repeated behavior shows someone is making this part of their routine?**
**Hint:** Format: "A user has a habit when they **[action]** at least **[N times]** in **[period]**."
*Example: "Sends 3+ invoices in each of 2 consecutive weeks."*
**Your answer:**

**6D. Prove it with data (do this after you have users)**
**Q6.8 Plan to check that your aha moment really predicts people staying.**
**Hint:** Compare people who did the aha event with those who did not. Do the first group stay longer? If not, pick a different aha event.
**Your answer:** When will I check? (date or "after 50 signups"): ______
**Your answer:** What result will make me change my definition?: ______

## 7. Activation Journey Map

**Q7.1 Fill in each step of the new customer's journey.**

| Step | What the customer does | What could make them quit? | What will you do to help? | How you will measure it |
|---|---|---|---|---|
| 1. Hears about you | | | | |
| 2. Arrives (site / store page) | | | | |
| 3. Signs up | | | | |
| 4. Finishes setup | | | | |
| 5. Reaches AHA | | | | |
| 6. Forms a habit | | | | |
| 7. Pays (if you charge) | | | | |
| 8. Tells others | | | | |

## 8. Onboarding Design (the first session)

**Q8.1 What does a brand-new user see first?** (describe the first screen in one or two lines)
**Your answer:**

**Q8.2 List your setup checklist (3 to 5 steps maximum) that ends at the aha moment.**
1. **Your answer:**
2. **Your answer:**
3. **Your answer:**
4. **Your answer:**
5. **Your answer:**

**Q8.3 Which help options will you give? (tick all that apply)**
- [ ] A "do it for me" path (template, sample data, auto-fill)
- [ ] A "do it myself" path
- [ ] A short welcome video or tour (under 2 minutes)
- [ ] Empty-state tips (helpful message when a screen is blank)
- [ ] Live chat or a personal welcome message from the founder
- [ ] Progress bar showing steps left

**Q8.4 Nudge plan: what happens if a user does NOT reach aha?**

| Trigger (what they did or didn't do) | Message | Channel (email / push / in-app / SMS) | When |
|---|---|---|---|
| Signed up, did nothing for 24 hours | | | |
| Finished setup but no aha after 3 days | | | |
| Reached aha | (celebrate and show the next step) | | |
| Went quiet for 7 days | | | |

**Q8.5 How will you speak to new users in the first 14 days?**
**Your answer:** Friendly / Professional / Playful / Other: ______  Max messages per week: ____

## 9. Revenue Model, Pricing and Packaging

**Q9.1 For the money model(s) you picked in Q1.3, define what happens at each stage.**

| Model | What "activated" means here | Moment you ask for money | Price (with currency & period) |
|---|---|---|---|
| Free / freemium | Used the core feature, not just signed up | When they hit [limit or feature]: ______ | Free + paid plan: ______ |
| Free trial → paid | Reached aha during the trial | Day ____ of ____-day trial | |
| Paid from day one | First successful use AFTER purchase | At sign-up | |
| Usage-based / fees | First paid transaction or usage | Each use / each deal | % or unit price: ______ |

**Q9.2 What is your "free to paid" or "trial to paid" target?**
**Your answer:** Target: ____ % of activated users pay within ____ days (GUESS if you have no data yet)

**Q9.3 How did you choose your price?** (competitors, customer interviews, cost, test)
**Your answer:**

**Q9.4 What is your *value metric*: the thing the customer pays for? (pick one)**
- [ ] Per user / seat
- [ ] Per project, store, or workspace
- [ ] Per usage (calls, messages, rides, orders)
- [ ] Flat fee per month or year
- [ ] Percentage commission or "take rate" (marketplace)
- [ ] One-time purchase
- [ ] Other: ______
**Hint:** A good value metric grows when the customer gets more value from you.
**Your answer:** Why this one:

**Q9.5 Define your plans (packaging).** Keep it to 1 to 3 plans at launch.

| Plan name | Price (currency, per period) | Billing (monthly / annual / one-time) | Who it is for | What is included | Limits (users, usage, storage) | Upgrade trigger |
|---|---|---|---|---|---|---|
| | | | | | | |
| | | | | | | |
| | | | | | | |

**Q9.6 Test willingness to pay with real prospects (ask at least 10).**
**Hint:** Ask four questions: At what price is it so cheap you doubt the quality? A bargain? Getting expensive but you'd still consider it? Too expensive to consider?

| # | Role | Too cheap | Bargain | Getting expensive | Too expensive |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

**Your answer:** Price range that most people accept: ______ to ______

**Q9.7 Discounts and promotions policy**

| Item | Your answer |
|---|---|
| Early-customer offer (what, how many, until when) | |
| Annual-plan discount | |
| Refund / cancellation policy | |
| Who may approve exceptions | |
| Store or payment-platform fees to factor in (check current rules) | |

**Q9.8 When will you review pricing?**
**Your answer:** Review at customer #50 on ______ and at #100 on ______. Signs to raise the price: ______  Signs to lower or repackage: ______

---

# PART 3: BUILD WITH AI (Development Lifecycle)

## 10. The AI-Driven Development Workflow

**Q10.1 Which tools will you use? (write real names)**

| Job | Tool name | Who/what controls it |
|---|---|---|
| AI coding assistant / agents | | |
| Where code lives (e.g. Git host) | | |
| Task tracker | | |
| Design tool | | |
| Hosting / app stores | | |
| Analytics tool | | |
| Customer messaging / email tool | | |
| Payments (if any) | | |

**Q10.2 Describe the build steps you will repeat for every feature.** (Edit the default below if needed.)

| # | Step | Done by | Output | Human must approve? |
|---|---|---|---|---|
| 1 | Write what to build and what "done" means | Human + AI | A short spec | Yes |
| 2 | Break it into small tasks | AI | Task list | Quick check |
| 3 | Write the code | AI | Code change | No (but gets reviewed) |
| 4 | Write automatic tests | AI | Tests | Quick check |
| 5 | Check security and quality automatically | AI | Report | Yes if any problem found |
| 6 | Human reviews the change | Human | Approve / reject | **Yes (required)** |
| 7 | Test on a staging copy | AI + Human | Pass / fail | Yes |
| 8 | Release | Human | Live feature | **Yes (required)** |
| 9 | Watch the numbers after release | AI | Alert / summary | Review weekly |

**Q10.3 What is your "Definition of Done" for any feature?** (tick all that apply)
- [ ] Works on the happy path
- [ ] Works when users make mistakes (errors handled)
- [ ] Automatic tests pass
- [ ] Reviewed by a human
- [ ] Tracking events added (Section 14)
- [ ] Help text / docs updated
- [ ] Works on the devices I promised (Q15.2)
- [ ] Other: ______

**Q10.4 Which actions must ALWAYS need a human "yes"?**
**Hint:** Recommended: releasing to customers, anything about money, changing the database, security settings, legal text, messages sent to customers.
**Your answer:**

## 11. AI Agent Roles

**Q11.1 List each AI agent (or AI helper) and its exact job.**
(See Appendix F for a recommended starting set of agents and their limits.)

| Agent name | Its ONE job | What it can see | What it may do alone | What needs a human OK | Who owns it |
|---|---|---|---|---|---|
| Example: *Spec Writer* | Turns ideas into specs | Notes, research | Draft specs | Approving the spec | |
| Example: *Builder* | Writes code for approved tasks | Code, specs | Write code in a test branch | Merging | |
| Example: *Tester* | Writes and runs tests | Code, specs | Run tests | Ignoring a failed test | |
| Example: *Reviewer* | Checks quality and security | Code changes | Comment, flag | Passing risky changes | |
| Example: *Growth Analyst* | Reads metrics, suggests experiments | Analytics (no personal data) | Draft reports | Launching experiments | |
| | | | | | |
| | | | | | |

**Q11.2 What are the safety rules for your agents?** (tick all that apply)
- [ ] Agents never see real customer passwords or payment details
- [ ] Agents work on copies, not on the live product
- [ ] Every agent change is saved with a record of who/what made it
- [ ] Agents cannot spend money or send messages to customers without approval
- [ ] I can switch agents off immediately. How: ______

## 12. Prompt Library (reusable instructions to give your AI)

**Q12.1 Save your best prompts here so you can reuse them across projects.**

| Prompt name | When to use | The prompt text (use [BRACKETS] for the parts to change) | Last tested (`YYYY-MM-DD`) |
|---|---|---|---|
| Example: Spec from idea | Starting a feature | "Write a one-page spec for [FEATURE]. Include who it is for, the problem, what 'done' means, and what is NOT included." | |
| Example: Activation check | Before launch | "Using this activation definition: [PASTE Q6.4], list every screen and step a new user takes and flag anything that slows them down." | |
| Example: Test plan | Before beta | "Write test cases for [FEATURE] covering normal use, mistakes, and edge cases." | |
| Example: Weekly metrics summary | Every week | "Here are this week's numbers: [PASTE]. Explain what changed, the top 3 reasons, and 2 experiments to try." | |
| | | | |
| | | | |

## 13. Build Plan and MVP Scope

**Q13.1 List every feature and sort it.**

| Feature | Must have / Should have / Won't have (yet) | Needed for aha? (Yes/No) | Size (S / M / L) | Target date |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

**Hint:** **Rule:** If a feature is not needed for the aha moment and not needed for safety or legal reasons, it is NOT in the first version.

**Q13.2 What will you NOT build before customer #100?**
**Your answer:**

**Q13.3 Build milestones**

| Milestone | Done means | Date | Done? |
|---|---|---|---|
| Prototype clickable | | | ☐ |
| Aha path works end to end | A tester can reach aha unaided | | ☐ |
| Tracking works | Every event in Section 14 shows in analytics | | ☐ |
| Private beta ready | Passes Section 15 gates | | ☐ |
| Public launch ready | Passes Section 17 Go/No-Go | | ☐ |

## 14. Tracking Plan (what you will measure from day one)

**GATE 2: Tracking must work BEFORE beta. If you cannot measure activation, you are guessing.**

**Q14.1 List the events your product must record.**

| Event name (simple, past tense) | When it fires | Which journey step (Section 7) | Properties to save (no private data) | Working? ☐ |
|---|---|---|---|---|
| Example: `signed_up` | Account created | 3 | source channel | ☐ |
| Example: `setup_completed` | Last setup step done | 4 | time taken | ☐ |
| Example: `activated` | **Q6.4 event happens** | 5 | days since signup | ☐ |
| Example: `habit_reached` | **Q6.7 happens** | 6 | | ☐ |
| Example: `paid` | First payment | 7 | plan, amount | ☐ |
| Example: `referral_sent` | Invite shared | 8 | | ☐ |
| | | | | ☐ |

**Q14.2 Where can you see these numbers every week?** (dashboard link / spreadsheet)
**Your answer:**

---

# PART 4: PROVE QUALITY (QA, Beta, Launch Readiness)

## 15. QA Plan and Quality Gates

**Q15.1 What types of testing will you do? (tick all that apply)**
- [ ] Automatic tests on every code change
- [ ] Manual "click everything" test of the aha path
- [ ] Mistake testing (wrong passwords, empty fields, bad internet)
- [ ] Speed test (how fast pages/screens load)
- [ ] Security check
- [ ] Accessibility check (works for people with different needs)
- [ ] Test with real, new users who have never seen it

**Q15.2 Which devices, browsers, or app versions must work?**
**Your answer:** *Example: Chrome and Safari (latest 2), iPhone iOS 17+, Android 13+*

**Q15.3 Quality gates** (all required before beta)

| Gate | Pass rule | Result (Pass / Fail) |
|---|---|---|
| Aha path | 5 out of 5 test users reach aha without help | |
| Serious bugs | 0 open "blocker" bugs | |
| Automatic tests | All pass | |
| Speed | Main screen loads in under ____ seconds | |
| Security | No known serious issues open | |
| Tracking | All Section 14 events verified | |

**Q15.4 How will you handle bugs?** Write your levels:

| Level | Meaning | Fix within |
|---|---|---|
| Blocker | Nobody can reach aha, or data is lost/unsafe | |
| Major | Some people can't finish a task | |
| Minor | Annoying but there is a workaround | |

## 16. Beta Plan

**Q16.1 How many beta testers, and who are they?**
**Your answer:** Number: ____ (suggested: 10 to 50)  Who and where from:

**Q16.2 What do you want to learn in beta? (maximum 3 questions)**
1. **Your answer:**
2. **Your answer:**
3. **Your answer:**

**Q16.3 How will testers give feedback?** (form, calls, in-app button, group chat)
**Your answer:**

**Q16.4 Beta exit rules (all must be true to leave beta)**

| Rule | Target | Actual |
|---|---|---|
| Activation rate | at least ____ % | |
| Time to reach aha | under ____ minutes/days | |
| Testers who would be "very disappointed" if the product disappeared | at least 40 % | |
| Blocker bugs | 0 | |
| Number of testers who finished the full journey | at least ____ | |

**Hint:** The "very disappointed" question: *"How would you feel if you could no longer use this product? Very disappointed / Somewhat disappointed / Not disappointed."* It is a popular check of product fit.

## 17. Launch Readiness and Go / No-Go

**GATE 3: The Go/No-Go call.** "No-Go" is a success of the process, not a failure.

**Q17.1 Check each item. Every row needs an owner, a date, and proof.**

| Area | Check | Owner | Date | Proof (link/screenshot) | Done |
|---|---|---|---|---|---|
| Product | Aha path works for new users | | | | ☐ |
| Product | Empty, error, and offline screens exist | | | | ☐ |
| Quality | All Section 15 gates passed | | | | ☐ |
| Tracking | Dashboard shows live numbers | | | | ☐ |
| Money | Pricing page and payments tested with test money | | | | ☐ |
| Marketing | Website / store page ready with clear promise | | | | ☐ |
| Marketing | First message to the audience written | | | | ☐ |
| Support | Help page and contact method live | | | | ☐ |
| Legal | Privacy policy and terms published (Section 18) | | | | ☐ |
| Operations | Backups, monitoring, and alerts on | | | | ☐ |
| Marketplace (Conditional) | Enough supply to serve the first buyers (Section 22) | | | | ☐ |
| Mobile (Conditional) | Store listing approved or submitted (Section 22) | | | | ☐ |

**Q17.2 Rollback plan: if launch goes wrong, how do you go back safely?**
**Your answer:** Who decides: ______  Steps:

**Q17.3 Final decision (pick one)**
- [ ] GO
- [ ] CONDITIONAL GO (list what must be fixed and by when): ______
- [ ] NO-GO (new review date): ______
**Your answer:** Decided by: ______  Date: ______

## 18. Legal, Privacy, and Security

> **Note:** This template is not legal advice. For legal text, ask a qualified professional in your country.

**Q18.1 What personal data do you collect?** (tick all)
- [ ] Name  [ ] Email  [ ] Phone  [ ] Location  [ ] Payment info (usually held by your payment company)
- [ ] Photos / files  [ ] Messages  [ ] Children's data (under 13 or under 16 where you operate)  [ ] Other: ______

**Q18.2 Rules checklist**

| Item | Needed? | Done? |
|---|---|---|
| Privacy policy page | | ☐ |
| Terms of service | | ☐ |
| Cookie / tracking consent (where required) | | ☐ |
| Users can delete their account and data | | ☐ |
| Data stored safely (passwords never saved in plain text) | | ☐ |
| App store privacy answers filled in (Conditional) Mobile | | ☐ |
| Rules for what users can post or do (Conditional) Marketplace / community | | ☐ |
| Payments and payouts compliance reviewed (Conditional) Marketplace | | ☐ |

**Q18.3 Which countries or regions will you serve first, and what rules apply there?**
**Your answer:**

## 19. Support Plan

**Q19.1 How will customers reach you?** (email, chat, form, community)
**Your answer:**

**Q19.2 Promise times**

| Situation | You reply within |
|---|---|
| Normal question | |
| Something is broken | |
| Money problem | |

**Q19.3 List your top 10 expected questions with answers (start with guesses, update weekly).**

| # | Question | Short answer | Help article link |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

**Q19.4 Escalation: who gets called when something serious happens?**
**Your answer:** Name and contact: ______

---

# PART 5: LAUNCH AND GROW (Customer #1 to #500)

## 20. Acquisition Channels and Budget

**Q20.1 Where will your first customers come from? Rank your top channels.**

| Rank | Channel (examples below) | Why it fits your customer | First test (what and when) | Cost per week | Result goal |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

**Hint:** Examples: one-to-one outreach to people you know, talking in communities where your customer already hangs out, helpful posts or videos, partnerships, referrals from early customers, directories and launch sites, app store search, small paid ads (later).

**Hint:** **Rule of thumb for the first 100:** do things by hand. Talk to people. Help before you pitch. Do not buy a complicated growth stack yet.

**Q20.2 Your cost limits**
**Your answer:** Max cost to win one customer (CAC target): ______
**Your answer:** Total budget for acquisition until customer #500: ______

**Q20.3 How will you track where each customer came from?** (links with tags, "how did you hear about us" question)
**Your answer:**

## 21. Customer Milestone Roadmap (Customers 1 to 500)

**Q21.1 Fill in each stage. Each stage has a gate you must pass before moving on.**

| Stage | Main goal | Main tactic | Gate to move on | Target date | Actual date |
|---|---|---|---|---|---|
| **1 → 10** | Learn. Get hand-picked customers | Personally invite and onboard each one | At least ____ of 10 activated; you know why the others did not | | |
| **11 → 50** | Make onboarding smooth | Fix the top 3 drop-off points weekly | Activation rate at least ____ % | | |
| **51 → 100** | Find a repeatable channel | Double down on the best 1 or 2 channels | One channel brings at least ____ customers per week | | |
| **101 → 250** | Retention and referrals | Habit emails, referral ask, success stories | Week-4 retention at least ____ % | | |
| **251 → 500** | Scale what works | Add a second channel, light automation | CAC under target and retention holding | | |
| **500 reached** | Review | Write a 1-page lessons summary | Part 6 review done | | |

**Q21.2 For stage 1 → 10, list the first 10 specific people or companies you will invite.**
**Hint:** Use roles if names are private.

| # | Who (role / company type) | Where to find them | Invited on | Status |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

## 22. Product-Type Add-Ons (Conditional: fill in only those that match; write `N/A` for the rest)

### 22A. Conditional: only if you have a MARKETPLACE or COMMUNITY
**Q22A.1 Which side do you grow first, and why?** (pick one)
- [ ] Supply side (sellers / providers / creators)
- [ ] Demand side (buyers / customers / members)
**Your answer:** Reason:

**Q22A.2 How many of the first side do you need before inviting the second side?**
**Your answer:** Number: ____  Why this number:

**Q22A.3 Define "activated" separately for each side.**
**Your answer:** Buyer/member: ______  Seller/provider: ______

**Q22A.4 Trust and safety: how do you prevent bad behavior and settle disputes?**
**Your answer:**

### 22B. Conditional: only if you have a MOBILE APP
**Q22B.1 App store plan**

| Item | Your answer |
|---|---|
| Store name and keywords | |
| Screenshots and short video ready? | |
| Review submission date (allow extra days for review) | |
| Age rating and privacy labels done? | |
| Push notification permission: when and how will you ask? | |
| Update plan (how often) | |

### 22C. Conditional: only if you have a SaaS / WEB APP
**Q22C.1 Do users need to invite a teammate or connect another tool to get value?**
**Your answer:** Yes / No. If yes, how will you make it easy?

## 23. Metrics Dashboard (the AARRR view)

**Q23.1 Pick ONE main number per stage. Give each an owner and a target.**
(If you have no data yet, use the method in Appendix G to set a first target.)

| Stage | Question it answers | Your ONE metric | Formula | Target | Owner | Where to see it |
|---|---|---|---|---|---|---|
| **Acquisition** | Are people finding us? | | | | | |
| **Activation** | Do they get value fast? | Activation rate | activated ÷ signups in the same group within the time limit (Q6.5) | ____ % | | |
| **Retention** | Do they come back? | | | ____ % | | |
| **Revenue** | Do they pay? | | | | | |
| **Referral** | Do they tell others? | | | | | |

**Q23.2 Extra activation numbers**

| Metric | How to measure | Goal |
|---|---|---|
| Time to aha | Time from signup to aha event | |
| Setup completion rate | Finished setup ÷ signups | |
| Drop-off step | The journey step (Section 7) where most people leave | |
| Activation by channel | Activation rate for each acquisition channel | |

**Q23.3 How often will you look at the numbers?**
**Your answer:** Every ______ (suggested: weekly)  Meeting or check at: ______

## 24. Experiments (small tests that improve activation)

**Q24.1 How will you run experiments?**
**Your answer:** Rules: one change at a time, one main metric, a written guess before you start, a fixed end date.

**Q24.2 Experiment backlog**

| # | Idea | Which stage / metric it should improve | Guess (what will happen?) | Effort (S/M/L) | Impact guess (1-5) | Start | End | Result | Keep? |
|---|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | | |
| 2 | | | | | | | | | |
| 3 | | | | | | | | | |

**Q24.3 Weekly operating rhythm (fill in the days)**

| Day | What happens |
|---|---|
| | Look at numbers (Section 23) |
| | Talk to 3 customers or users |
| | Pick this week's experiment |
| | Ship improvements (via Section 10 workflow) |
| | Write a 5-line update (what worked, what didn't, what's next) |

## 25. Retention, Customer Success and Referral

**Q25.1 What do you do for users who activated, so they keep coming back?**
**Your answer:**

**Q25.2 Win-back: what message do you send to someone who left?**
**Your answer:**

**Q25.3 How do you ask happy customers to refer others?**
**Hint:** Ask at a moment of success. Reward status or early access, not just discounts.
**Your answer:** When/where you ask: ______  Reward: ______

**Q25.4 How will you collect stories and reviews from happy customers?**
**Your answer:**

**Q25.5 Customer success touchpoints: when will you personally check in?**

| Moment | Action | Channel | Who |
|---|---|---|---|
| Day 0 (signup) | Welcome message | | |
| After aha | Congratulate and suggest the next step | | |
| Day 14 | Ask "What almost stopped you?" | | |
| Day 30 | Ask for feedback and a possible referral | | |
| Before renewal or trial end | Check value received | | |

**Q25.6 Customer health score: which signals mean a customer is healthy or at risk?**

| Signal | Healthy (green) | Watch (yellow) | At risk (red) |
|---|---|---|---|
| Logins or sessions per week | | | |
| North Star metric (Q5.2) | | | |
| Support tickets | | | |
| Payment status | | | |

**Q25.7 What will you do when a customer turns red?**
**Your answer:** Action: ______  Within: ______

**Q25.8 Growth from existing customers: what signals show a customer is ready for more?** (upgrade, add users, add features)
**Your answer:**

**Q25.9 How do you measure satisfaction?** (pick all that apply)
- [ ] "Very disappointed" survey (Q16.4)
- [ ] Net Promoter Score (NPS)
- [ ] Customer satisfaction after support (CSAT)
- [ ] Short customer interviews (target: ____ per month)
**Your answer:** Who reads the results, and how often:

---

# PART 6: MEASURE (Stop, Pivot, or Keep Going)

## 26. Kill, Pivot, or Persevere Criteria

> Decide the rules NOW, while you are calm, not later when you are emotional.

**Q26.1 Fill in your review checkpoints.**

| Checkpoint | Date | Keep going if... | Change plan (pivot) if... | Stop if... |
|---|---|---|---|---|
| After beta | | | | |
| At customer #50 | | | | |
| At customer #100 | | | | |
| At customer #250 | | | | |
| At customer #500 | | | | |

**Q26.2 What would you change first if activation is low?** (pick in order of your plan)
- [ ] Remove setup steps
- [ ] Add a template or "do it for me" option
- [ ] Improve the first-screen message
- [ ] Add personal outreach
- [ ] Re-check who the customer is (go back to Part 1)
- [ ] Re-check the aha definition (Q6.8)

**Q26.3 What would you change first if people activate but do NOT stay?**
**Your answer:**

**Q26.4 What would you change first if people stay but do NOT pay?**
**Your answer:**

---

# PART 7: PROTECT (Risks)

## 27. Risk Register

**Q27.1 List what could go wrong. Think about the customer, the technology, the AI, the law, and the money.**

| # | Risk | Chance (L/M/H) | Damage (L/M/H) | What I will do to prevent it | If it happens, I will... | Owner |
|---|---|---|---|---|---|---|
| 1 | Example: AI-written code has a security hole | | | Human review + automatic security scan | Pause release, fix, tell users if needed | |
| 2 | Example: Signups come but nobody activates | | | Fix onboarding first, track drop-offs | Pause paid acquisition | |
| 3 | Example: Only one channel works and it stops | | | Test a second channel by customer #100 | | |
| 4 | Example: Key tool or service shuts down | | | | | |
| 5 | | | | | | |

---

# PART 8: MANAGE (Budget, Decisions, Questions)

## 28. Budget, Resources and Team Roles

**Q28.1 Money plan (use one currency)**

| Item | Monthly cost | One-time cost | Notes |
|---|---|---|---|
| AI tools and usage | | | |
| Hosting / servers / app store fees | | | |
| Analytics and messaging tools | | | |
| Marketing / acquisition | | | |
| Support tools | | | |
| Legal / accounting | | | |
| Other | | | |
| **TOTAL** | | | |

**Q28.2 How many months can you pay for this before you need revenue?**
**Your answer:**

**Q28.3 How many hours per week can you work on this?**
**Your answer:**

**Q28.4 Who is responsible for what? (RACI)**
**Hint:** **R** = does the work. **A** = accountable (final say; exactly ONE per row). **C** = consulted before. **I** = informed after. If you work alone, put your name in every cell; this still shows which hats you wear. AI agents may be **R** but never **A**.

| Activity | Owner / founder | Builder (human or lead) | Designer | Growth / marketing | Support | Legal / finance advisor | AI agents |
|---|---|---|---|---|---|---|---|
| Customer research and validation (Part 1) | | | | | | | |
| Activation definition (Part 2) | | | | | | | |
| Pricing and packaging (Section 9) | | | | | | | |
| Building and code review (Part 3) | | | | | | | |
| QA and beta (Part 4) | | | | | | | |
| Go / No-Go decision (Section 17) | | | | | | | |
| Legal and privacy (Section 18) | | | | | | | |
| Acquisition and campaigns (Section 20) | | | | | | | |
| Customer support and success (Sections 19, 25) | | | | | | | |
| Metrics and experiments (Sections 23, 24) | | | | | | | |
| Budget (Section 28) | | | | | | | |

**Q28.5 Who makes the final call if two people disagree?**
**Your answer:**

## 29. Decision Log, Assumptions, and Open Questions

**Q29.1 Decision log** (write every big choice so you never forget why)

| Date | Decision | Why | Who decided | Can it be undone? |
|---|---|---|---|---|
| | | | | |

**Q29.2 Assumptions I am making that might be wrong**

| # | Assumption | How I will check | By when | Status (Open / Confirmed / Wrong) |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |

**Q29.3 Open questions (anything marked `UNKNOWN` above)**

| # | Question | Where it appears (Q number) | Who will find out | By when |
|---|---|---|---|---|
| 1 | | | | |

---

# PART 9: FINAL CHECK (Is this document ready?)

## 30. Completeness Checklist
Tick every box. If you cannot tick one, go back and fix it.

**Clarity**
- [ ] Every question has a real answer, `N/A: reason`, or `UNKNOWN: plan`
- [ ] No *Example* text is left in my answers
- [ ] A new person could read this and not need to ask me what anything means

**Customer and proof**
- [ ] I named ONE first customer type (Q2.1)
- [ ] I had at least 10 real conversations, or wrote why not (Q4.1)
- [ ] Gate 1 result is filled in (Q4.4)

**Activation**
- [ ] My activation event is ONE exact sentence with a time limit (Q6.4, Q6.5)
- [ ] I can measure it, or I have a task to add tracking (Q6.6, Section 14)
- [ ] My journey map and onboarding are filled in (Sections 7 and 8)
- [ ] Pricing and plans are defined and tested with real prospects (Q9.4 to Q9.6)

**Build and quality**
- [ ] Every AI agent has one job and a human approval rule (Section 11)
- [ ] Tracking works (Gate 2)
- [ ] QA gates have pass/fail results (Section 15)
- [ ] Beta exit rules are numbers (Q16.4)
- [ ] Go/No-Go decision recorded with owner and date (Q17.3)

**Growth**
- [ ] I have a top 3 channel list and a CAC limit (Section 20)
- [ ] Every stage from 1 to 500 has a goal and gate (Q21.1)
- [ ] I have ONE metric per AARRR stage with an owner (Q23.1)
- [ ] Customer success touchpoints and health signals are defined (Q25.5, Q25.6)
- [ ] Stop/pivot/keep-going rules are written (Section 26)

**Safety and money**
- [ ] Legal, privacy, and support are covered (Sections 18 and 19)
- [ ] Top risks have plans (Section 27)
- [ ] Budget, runway, and RACI roles are filled in (Section 28)

**Housekeeping**
- [ ] Part 0 version, owner, and dates are updated
- [ ] Decision log and open questions are up to date (Section 29)

## 31. Readiness Score
Count your ticked boxes in Section 30.
**Your answer:** Ticked: ____ of 26

| Score | What it means |
|---|---|
| 26 of 26 | **Ready.** Approve it and start executing |
| 21 to 25 | **Nearly ready.** Fix the missing items this week |
| Under 21 | **Not ready.** Finish the missing parts before building or launching |

## 32. Sign-off

| Role | Name | Decision (Approved / Needs changes) | Date |
|---|---|---|---|
| Owner | | | |
| Reviewer (a second person, or an AI reviewer plus the owner) | | | |

---

# APPENDIX A: Plain-English Glossary

| Word | What it means (simple) |
|---|---|
| **Activation** | The first time a customer gets the real value you promised |
| **Aha moment** | The "wow, this works!" moment |
| **Setup moment** | The point where the user is ready to try the product |
| **Habit moment** | When the user keeps coming back on their own |
| **Acquisition** | How people find you |
| **Retention** | How many people keep using it over time |
| **Churn** | How many people leave |
| **Referral** | When a customer brings in a new customer |
| **AARRR** | Five steps: Acquisition, Activation, Retention, Revenue, Referral |
| **North Star metric** | The one number that shows real value to customers |
| **CAC** | Cost to win one customer |
| **Cohort** | A group of people who started in the same week or month |
| **MVP** | The smallest version good enough to test your idea |
| **Beta** | A trial with a small group before everyone can use it |
| **Go / No-Go** | The final yes-or-no decision before launch |
| **Gate** | A checkpoint you must pass before moving on |
| **Rollback** | Safely going back to the last working version |
| **Staging** | A safe copy of your product used for testing |
| **AI agent** | An AI helper with one specific job and limited permissions |
| **Prompt** | The instruction you give to an AI |
| **Funnel** | The steps customers go through, with some leaving at each step |
| **Empty state** | A screen with nothing on it yet; use it to guide the user |
| **TTV (time to value)** | How long it takes a new user to reach the aha moment |
| **Value metric** | The thing the customer pays for (seats, usage, projects) |
| **Packaging** | How features and limits are grouped into plans |
| **Take rate** | The percentage a marketplace keeps from each transaction |
| **Health score** | A simple signal (green / yellow / red) of whether a customer is likely to stay |
| **NPS / CSAT** | Standard satisfaction surveys (likelihood to recommend / satisfaction after an interaction) |
| **RACI** | Who is Responsible, Accountable, Consulted, and Informed for each activity |

# APPENDIX B: One-Page Quick Fill (if you only have 30 minutes)

Answer just these, in this order, then come back for the rest:
1. Q1.1 What does it do?
2. Q2.1 Who is the first customer?
3. Q3.2 What is the promise (before and after)?
4. Q6.4 What exact event means "activated"?
5. Q8.2 What are the 3 to 5 setup steps to aha?
6. Q10.4 What always needs a human "yes"?
7. Q14.1 What events must be tracked?
8. Q20.1 What are the top 3 channels?
9. Q21.1 What are the gates from 1 to 500?
10. Q26.1 When do I stop, pivot, or keep going?

# APPENDIX C: Common Mistakes (avoid these)

- Counting signups as customers. Count **activated** ones.
- Choosing "everyone" as the customer.
- Building features that are not needed for the aha moment.
- Launching before tracking works, then guessing what happened.
- Counting polite friends as proof of demand.
- Letting AI agents release changes or contact customers without a human "yes".
- Tracking ten numbers per stage. Pick one.
- Buying advanced growth tools before you have 100 customers.
- Changing many things at once so you cannot tell what worked.
- Forgetting to write down why you made a decision.
- Setting prices by guessing instead of asking real prospects.
- Ignoring customers who activated but have gone quiet.
- Leaving two people "in charge" of the same decision.

# APPENDIX D: Sources of the ideas used in this template
The structure combines widely used practices: setup / aha / habit activation moments and time-to-value; the AARRR "pirate metrics" growth framework; beta and launch go/no-go readiness checklists; hand-built first-100-customers playbooks; and human-in-the-loop guardrails for AI-agent development. Adapt every number to your own product.

# APPENDIX E: WORKED EXAMPLES (one per product type)

> These are fictional and shortened. They show the *level of detail* expected. Do not copy them; write your own.

## E1. SaaS / web app: "InvoiceQuick" (fictional invoicing tool for freelance designers)

| Item | Example answer |
|---|---|
| Q1.1 What it does | Helps freelance designers send professional invoices in 30 seconds so they get paid faster |
| Q2.1 First customer | Solo freelance graphic designers in the US who invoice 5 or more clients per month |
| Q3.2 Promise | Before: about 20 minutes per invoice. After: about 30 seconds |
| Q5.2 North Star | Invoices sent per active user per week |
| Q6.1 Setup | Create account, add 1 client |
| Q6.4 Activation | A user is activated when they send 1 invoice within 7 days of signing up |
| Q6.7 Habit | Sends 3 or more invoices in each of 2 consecutive weeks |
| Q8.2 Setup checklist | 1. Create account. 2. Add a client. 3. Choose a template. 4. Send first invoice |
| Q9.1 Revenue | Free trial for 14 days, then USD 12 per month |
| Q20.1 Channels | 1. Personal outreach to designers in 2 communities. 2. Helpful posts on invoicing mistakes. 3. Referrals |
| Q21.1 Gate 1 to 10 | At least 7 of 10 activated; reasons for the other 3 documented |

## E2. Mobile app: "StepStreak" (fictional walking-habit app)

| Item | Example answer |
|---|---|
| Q1.1 What it does | Helps busy office workers build a daily walking habit with short challenges |
| Q2.1 First customer | Office workers aged 25 to 45 who sit 6 or more hours a day, in one city |
| Q5.2 North Star | Days per week with at least 20 minutes of tracked walking |
| Q6.1 Setup | Allow step tracking, pick a daily goal |
| Q6.4 Activation | A user is activated when they complete 1 walking challenge within 3 days of installing |
| Q6.7 Habit | Completes a challenge on 4 or more days in each of 2 consecutive weeks |
| Q22B.1 Push permission | Ask after the first completed challenge, never on first launch |
| Q9.1 Revenue | Free with a paid premium plan; upgrade prompt after the 7th completed challenge |
| Q20.1 Channels | 1. Employer wellness groups. 2. App store search. 3. Short walking-tip videos |

## E3. Marketplace: "LocalTutor" (fictional tutor-student marketplace)

| Item | Example answer |
|---|---|
| Q1.1 What it does | Connects high-school students with vetted local tutors for one-hour sessions |
| Q22A.1 Grow first | Supply side (tutors), because students will not stay if no tutor is available |
| Q22A.2 Number needed | 15 tutors across 3 subjects before inviting students |
| Q22A.3 Activation | Tutor: has a complete profile and receives a first booking within 14 days. Student: completes a first paid session within 14 days of signing up |
| Q5.2 North Star | Completed tutoring sessions per week |
| Q9.4 Value metric | Percentage commission per completed session |
| Q22A.4 Trust and safety | Identity check for tutors, session reviews, a clear dispute process |
| Q21.1 Gate 1 to 10 | 10 tutors onboarded and 10 students complete a first session |

---

# APPENDIX F: AI-AGENT PROTOCOL AND PROMPT PACK

## F1. Protocol when an AI agent fills in or updates this document

1. Read Parts 0 to 2 first. Do not fill later parts until the customer and activation event are defined.
2. Never invent facts, numbers, quotes, customers, prices, or legal terms. Use `UNKNOWN: <plan>` instead.
3. Mark every estimate with `(GUESS)` and every source with a link or note.
4. Keep question numbers and headings unchanged. Write only in answer lines and tables.
5. After each Part, list assumptions made and questions for the human.
6. Do not send anything to customers, change prices, change legal text, or release software. Prepare drafts and request human approval.
7. At the end, run Part 9 and report the Readiness Score plus every remaining `UNKNOWN`.

## F2. Recommended starting agents

| Agent | Single job | Inputs | Must never | Human approval needed for |
|---|---|---|---|---|
| Research Summarizer | Turn interview notes into themes | Anonymized notes | Invent quotes | Conclusions that change the target customer |
| Spec Writer | Write specs from approved ideas | Parts 1 and 2 | Add features outside the aha path without flagging | Spec approval |
| Builder | Implement approved tasks | Spec, code | Touch production data or secrets | Merge and release |
| Test Writer | Create and run tests | Spec, code | Delete failing tests to pass | Waiving any failed test |
| Security and Quality Reviewer | Flag security and quality issues | Code changes | Approve its own fixes | Passing any high-severity finding |
| Onboarding Auditor | Check the first-session flow against Q6.4 | Screens, flow | Change copy that makes legal or price claims | Customer-facing copy |
| Growth Analyst | Summarize metrics, propose experiments | Aggregated analytics | Access personal data | Starting any experiment |
| Support Drafter | Draft replies and help articles | Support questions | Promise refunds or fixes | Anything sent to a customer |

## F3. Extra prompts for the Prompt Library (Section 12)

| Name | Prompt |
|---|---|
| Activation definition review | "Here is my activation definition: [PASTE Q6.4]. Check that it is a single observable action, has a time limit, reflects real value rather than a vanity click, and can be measured with my events in [PASTE Section 14]. List problems and suggest two alternatives." |
| First-session teardown | "Walk through my onboarding steps [PASTE Q8.2] as a brand-new user who knows nothing. List every point of confusion, every unnecessary step, and what could be delayed until after the aha moment." |
| Release gate check | "Here is the change summary [PASTE] and my quality gates [PASTE Q15.3]. State which gates are met, which are unproven, and what evidence is missing. Do not approve; recommend." |
| Experiment design | "I want to improve [METRIC]. Current value: [X]. Propose 3 single-change experiments, each with a hypothesis, success metric, required sample size or duration, and a stop condition." |
| Experiment readout | "Experiment: [DESCRIBE]. Data: [PASTE]. State what happened, whether the difference is likely meaningful given the sample size, what we cannot conclude, and the next step." |
| Weekly decision memo | "Using this week's numbers [PASTE] and my kill/pivot rules [PASTE Q26.1], state whether we are on track, the biggest drop-off, and the one decision for the owner." |
| Churn-risk review | "Here are customer health signals [PASTE Q25.6 and data]. Group customers into green, yellow, and red, and draft a short personal message for each red customer for my approval." |

---

# APPENDIX G: STARTING TARGETS AND HOW TO SET YOUR OWN

> **Important:** The values below are *starting heuristics*, not guarantees or industry benchmarks. Results vary widely by product, price, and audience. Replace every one with your own data as soon as you have it.

## G1. Method for setting a target when you have no history

1. **Measure a baseline** with your first 30 to 50 users (or beta testers).
2. **Set a stretch target** that is a clear improvement over the baseline for your next cohort (for example, a relative increase you consider meaningful and achievable in 4 weeks).
3. **Re-set the target** after each stage gate (customers 10, 50, 100, 250).
4. **Compare cohorts, not totals.** Group users by signup week and compare like with like.

## G2. Metrics and how to calculate them

| Metric | Formula | Notes |
|---|---|---|
| Activation rate | Users who reach the aha event within the time limit ÷ users who signed up in the same period | Use the exact event from Q6.4 |
| Time to value (TTV) | Time of aha event minus time of signup, per user; report the median | Report by channel |
| Setup completion rate | Users who finish setup ÷ signups | Find the step where most users leave |
| Retention at day N | Users active on day N (or in week N) ÷ users in the starting cohort | Pick N to match how often the product should be used |
| Churn | Users or customers lost in a period ÷ users or customers at the start | Track logos and revenue separately for paid products |
| Trial-to-paid or free-to-paid | Paying users ÷ users who reached aha (or started trial) | Measure by cohort |
| CAC | Total acquisition spend in a period ÷ new activated customers in that period | Include your own time as a cost for honesty |
| Referral rate | Customers who invited at least one person ÷ activated customers | |
| "Very disappointed" score | Share of surveyed users who would be very disappointed without the product | A commonly used threshold for product-market fit is 40 percent |

## G3. Commonly used rules of thumb (verify for your business)

| Rule | Use it to | Caution |
|---|---|---|
| "Very disappointed" at least 40 percent | Decide whether to exit beta | Needs enough responses (aim for 30 or more) |
| Customer lifetime value at least 3 times CAC | Judge whether paid acquisition is sustainable | Needs real retention data; unreliable early on |
| CAC payback within about 12 months | Check cash efficiency for subscription products | Shorter is safer if cash is tight |
| One channel producing a steady flow before adding a second | Decide when to expand channels | Do not scale spend before activation is healthy |
| Fix activation before spending on acquisition | Avoid paying for users who leave | If activation is low, more traffic wastes money |

## G4. Starting targets table (fill with your own numbers)

| Stage | Activation rate target | Time to aha target | Week-4 retention target | CAC limit | How you will know it is working |
|---|---|---|---|---|---|
| Beta | ____ % (baseline) | | | n/a | Testers reach aha without help |
| Customers 1 to 50 | ____ % (beat baseline) | | | | You can explain why each person did or did not activate |
| Customers 51 to 100 | ____ % | | | | One channel brings customers repeatedly |
| Customers 101 to 250 | ____ % | | ____ % | | Retention holds while you grow |
| Customers 251 to 500 | ____ % | | ____ % | | CAC stays under the limit |

*End of template. Save a copy of this file for each new project and rename it with the project name.*
