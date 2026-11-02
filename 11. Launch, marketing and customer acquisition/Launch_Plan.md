# HOW TO FILL THIS DOCUMENT (Read this first, 5 minutes)

**What this file is:** one single plan that takes your product from "built with AI" to **"500 real customers are using it."** Fill it top to bottom. Do not skip around.

**Who it is for:** you, a solo builder. You do not need to know marketing, coding or business words. If a question confuses you, do these 3 things: (1) read the *Examples* under it, (2) look up the hard word in the **Dictionary at the bottom**, (3) copy the style of the example and write your own answer. A 10-year-old should be able to fill it in.

**Simple-words promise:** every question is really asking one of four things: *Who is it for? What does it do? Does it work? How will people find it?* If you get lost, come back to those four.

> ⚖️ **Important:** this template gives general guidance, not legal, tax or financial advice. For laws, taxes and contracts, check the official rules for your country or ask a qualified professional.

## The 6 rules

1. **Answer every question.** Write on the line that says `YOUR ANSWER:` or replace the text in `[square brackets]`.
2. **Short is fine.** One sentence is a good answer. Numbers beat feelings ("50 people", not "a lot").
3. **Don't know yet? Write `TBD` plus a date** you will find out (example: `TBD - by 12 Nov`). Never leave a blank. Blanks make people (and AI agents) guess.
4. **Tick the boxes.** `[ ]` = not done. Change it to `[x]` when done.
5. **Update the Status line** at the top of each Part: `Not started` → `In progress` → `Done`.
6. **Never invent numbers.** If you're guessing, write `(guess)` after it.

## Status key

| Symbol | Meaning |
|---|---|
| `[ ]` / `[x]` | Not done / Done |
| `TBD` | I don't know yet (must have a date) |
| `N/A` | Doesn't apply to my product (write one line why) |
| 🛑 | **Gate.** STOP. Do not go on until every box above it is ticked |
| 🤖 | **AI Agent Corner.** What AI may do here and what a human must approve |

## Two example products used in this template

Every question has a **Web example** and a **Mobile example** so you can copy whichever fits you.

| | Web example | Mobile example |
|---|---|---|
| Name | **InvoiceNest** | **PlantPal** |
| What it is | A website where freelancers make and send invoices | A phone app that reminds you to water plants |
| Who uses it | Freelance designers/writers | Busy city plant owners |
| Money | $9/month subscription | Free + $4/month upgrade |

## How to use AI agents with this file

1. Give your AI agent this whole file plus your code/spec/notes.
2. Tell it: *"Fill the `YOUR ANSWER:` lines you can answer from the files. Mark anything unsure as `TBD`. Do not invent numbers. Label your drafts `(AI draft)`."*
3. **A human (you) must approve** every answer in Part 1, Part 2 (pricing), every 🛑 gate, and anything about money, law, or user data.
4. Each Part ends with a 🤖 **AI Agent Corner** with a ready-to-paste prompt.

## The path at a glance

```
PART 0  About this plan
PART 1  Know your product and your customer
PART 2  Pricing & unit economics
PART 3  Build & QA readiness (+ onboarding, accessibility)   -> 🛑 Gate A: "Safe to show people?"
PART 4  Pre-launch & beta                                    -> 🛑 Gate B: "Ready for the public?"
PART 5  Launch day & marketing
PART 6  Post-launch: 0 -> 500 customers                      -> 🛑 Gate C: "500 reached"
PART 7  After 500: next steps
PART 8  Risks, budget & decision log
PART 9  Final sign-off
APPENDIX  Plain-word dictionary
```

## 📊 PROGRESS DASHBOARD (update every time you work on this file)

| Part | Name | Status | % done | Gate | Gate result |
|---|---|---|---|---|---|
| 0 | About this plan | Not started | 0% | - | - |
| 1 | Product & customer | Not started | 0% | - | - |
| 2 | Pricing & unit economics | Not started | 0% | - | - |
| 3 | Build & QA readiness | Not started | 0% | 🛑 A | [ ] GO  [ ] NO-GO |
| 4 | Pre-launch & beta | Not started | 0% | 🛑 B | [ ] GO  [ ] NO-GO |
| 5 | Launch day & marketing | Not started | 0% | - | - |
| 6 | Post-launch 0 → 500 | Not started | 0% | 🛑 C | [ ] Reached  [ ] Not yet |
| 7 | After 500: next steps | Not started | 0% | - | - |
| 8 | Risks, budget, decisions | Not started | 0% | - | - |
| 9 | Final sign-off | Not started | 0% | - | - |

| Live numbers | Now | Goal |
|---|---|---|
| Customers (per Q0.1) | [0] | 500 |
| Days since launch | [ ] | - |
| Money spent so far | [$ ] | [Q8.1 total] |
| Last updated (date) | [ ] | - |
| Next action (one line) | [ ] | - |

---

# PART 0. ABOUT THIS PLAN

**Status:** Not started

| Field | YOUR ANSWER |
|---|---|
| Product name | [InvoiceNest / PlantPal] |
| Plan owner (you) | [your name] |
| Plan version | [v1.0] |
| Date started | [YYYY-MM-DD] |
| Target public launch date | [YYYY-MM-DD] |
| Target date to reach 500 customers | [YYYY-MM-DD] |
| Product type | [ ] Web app / SaaS  [ ] Mobile app  [ ] Other: ____ |
| Where is the project folder / repo? | [link or path] |
| Which AI tools help build this? | [e.g., Claude, Cursor, Copilot] |
| Hours per week I can give this | [e.g., 15] |

**Related documents.** (Link the other files in your project so nothing is guessed. Write `N/A` if you don't have it.)

| Document | Link / path | Used for in this plan |
|---|---|---|
| Product Requirements / Spec (PRD) | [../Product/PRD.md] | Features (Q3.1), aha moment (Q1.6) |
| Roadmap | [../Product/Roadmap.md] | After-500 plan (Part 7) |
| Test Plan / QA report | [../Quality/Test_Plan.md] | Quality checks (Q3.4) |
| Architecture / Tech Design | [../Engineering/Architecture.md] | Hosting, spike check (Q4.11) |
| Security & Privacy notes | [../Legal/Privacy_Security.md] | Legal & compliance (Q3.9-3.9d) |
| Brand & Messaging guide | [../Marketing/Brand_Guide.md] | Messages (Q5.1) |
| Support / FAQ doc | [../Support/FAQ.md] | Support plan (Q6.4) |
| Analytics / Metrics plan | [../Data/Metrics.md] | Scorecard (Q6.2) |

> If a linked document disagrees with this plan, write the conflict in the Decision Log (Q8.4) and decide which one wins.

**Q0.1. What is a "customer" for this plan?** (This decides when we count to 500. Pick ONE and never change it.)
- [ ] Someone who **signed up** (made an account)
- [ ] Someone who **activated** (reached the "aha moment", see Q1.6)
- [ ] Someone who **paid** at least once
- [ ] Someone who **came back** at least 2 times in 14 days (active)

*Web example (InvoiceNest): "A customer is someone who signed up AND sent at least one real invoice."*
*Mobile example (PlantPal): "A customer is someone who installed the app AND added a plant AND opened the app again within 7 days."*

YOUR ANSWER:

---

# PART 1. KNOW YOUR PRODUCT AND YOUR CUSTOMER

**Status:** Not started
*If you can't answer these, no launch plan will save you.*

**Q1.1. In one sentence, what does your product do, and for whom?**
Fill this sentence: *"[Product] helps [who] to [do what] so that [good result]."*
*Web: "InvoiceNest helps freelancers send professional invoices in 2 minutes so that they get paid faster."*
*Mobile: "PlantPal helps busy people remember to water plants so that their plants stop dying."*

YOUR ANSWER:

**Q1.2. What painful problem do people have today?** (What do they do now? Why is it annoying?)
*Web: "They use Word templates and spreadsheets. It's slow, looks unprofessional, and they forget to chase late payments."*
*Mobile: "They set phone alarms or forget. Alarms don't say which plant needs what."*

YOUR ANSWER:

**Q1.3. Who is your ONE ideal first customer?** ("Everyone" is not allowed.)

| Question | YOUR ANSWER |
|---|---|
| Who are they? (job, age range, situation) | [Web: freelance designers, 25-45 / Mobile: apartment dwellers, 25-40] |
| Where do they hang out online? | [Web: Reddit r/freelance, LinkedIn / Mobile: r/houseplants, Instagram] |
| How do they solve it today? | [Web: Word + spreadsheet / Mobile: phone alarms] |
| What would make them switch or pay? | [Web: getting paid faster / Mobile: never killing another plant] |
| How many of them exist? (best guess + where you found it) | |

**Q1.4. Who are your alternatives (competitors or workarounds), and why are you better?**

| Alternative they use today | Their weakness | Why yours is better (1 line) |
|---|---|---|
| [competitor/workaround 1] | | |
| [competitor/workaround 2] | | |
| [competitor/workaround 3] | | |

**Q1.5. Headline test.** Write the headline for your website or store page in 10 words or fewer. Read it to one stranger. Do they understand it in 5 seconds?
*Web: "Send professional invoices in 2 minutes." Mobile: "Never forget to water your plants again."*

YOUR ANSWER:   Stranger understood it? [ ] Yes  [ ] No → rewrite.

**Q1.6. What is the ONE "aha moment"?** (The first moment a new user thinks "oh, this is useful!")
*Web: "They send their first invoice and see it arrive as a clean PDF." Mobile: "They add their first plant and see tomorrow's reminder."*

YOUR ANSWER:

**Q1.7. What 3 numbers prove this is working?** (Fill the targets.)

| Number | Plain-word meaning | Target |
|---|---|---|
| Visitors | People who see your site / store page | [e.g., 8,000] |
| Sign-ups / installs | People who create an account or install | [e.g., 1,200] |
| Activated | People who reach the aha moment (Q1.6) | [e.g., 600] |
| Customers | Per your Q0.1 definition | **500** |
| Come-back rate | % returning after 7 days | [e.g., 30%] |

> **Reverse-math helper (do this):** 500 customers ÷ (% of sign-ups who become customers) ÷ (% of visitors who sign up) = visitors you need.
> *Example: 500 ÷ 0.40 ÷ 0.05 = 25,000 visitors.* Your math: [  ]

**Q1.8. Success and failure line.** At what numbers will you say *"it's working, keep going"* and at what numbers *"change something"*?
- Keep going if: [e.g., 5% of visitors sign up and 40% of those activate]
- Change something if: [e.g., under 2% sign up after 1,000 visitors]

### 🤖 AI Agent Corner: Part 1

| AI may do | Human must approve |
|---|---|
| Draft answers from your README/spec | The one-sentence promise (Q1.1) and ideal customer (Q1.3) |
| Research competitors (with links) | Any market-size number (ask for the source link) |
| Suggest headlines (give 10 options) | The final headline and the "aha moment" |

**Paste this prompt:**
> *"Read my project files. Fill Part 1 of Launch_Plan.md. For every competitor or number, give a source link. If you can't find evidence, write TBD. Give me 10 headline options under Q1.5 and don't pick for me."*

---

# PART 2. PRICING & UNIT ECONOMICS

**Status:** Not started
*"Unit economics" just means: does one customer bring in more money than they cost you?*

**Q2.1. How will you make money?**
- [ ] Free forever (no money plan yet; skip to Q2.6)  [ ] Free + paid upgrade (freemium)  [ ] Free trial then paid  [ ] Monthly subscription  [ ] One-time payment  [ ] Ads  [ ] Other: ____

**Q2.2. Your price.**

| Plan name | Price | What's included | Who it's for |
|---|---|---|---|
| [Free] | [$0] | [Web: 3 invoices/month / Mobile: 5 plants] | |
| [Pro] | [Web: $9/mo / Mobile: $4/mo] | [unlimited, reminders, export] | |

Price is a guess or tested? [ ] Guess  [ ] Tested with real people (see Q4.10)

**Q2.3. Cost to serve one customer (per month).** Ask your AI to help estimate hosting, AI/API usage, email, support time.

| Cost | Per customer per month |
|---|---|
| Hosting / servers | [$ ] |
| AI/API usage (if your product calls AI) | [$ ] |
| Payment fees (e.g., ~3% + fixed fee) | [$ ] |
| App store cut (mobile: often 15-30%) | [$ ] |
| Support/other | [$ ] |
| **Total cost per customer** | **[$ ]** |

**Q2.4. Profit math.**
- Price per month: [A]  Cost per month: [B]  Profit per month = A − B = [C]
- Is C above zero? [ ] Yes  [ ] No → change price or reduce cost.

**Q2.5. Cost to get a customer (CAC) and break-even.**
- Money I plan to spend getting the first 500 customers: [$ ] ÷ 500 = **CAC [$ ]**
- Months until one customer pays back CAC = CAC ÷ C = [ ] months. (Under 12 is healthy for a beginner.)
- Expected customer lifetime (months they stay): [guess]

**Q2.6. Free vs paid rules.** What does the free user get, what is the paywall, and when will you show the upgrade? [  ]

**Q2.7. Payments setup.**
- [ ] Payment provider chosen: [Stripe / Paddle / Lemon Squeezy / App Store / Play Store]
- [ ] Taxes (VAT/sales tax) handled by the provider or I know how: [  ]
- [ ] Refund policy written: [e.g., 14 days, no questions]
- [ ] Test payment worked; test refund worked

### 🤖 AI Agent Corner: Part 2

| AI may do | Human must approve |
|---|---|
| Calculate break-even, build a price table | Final price |
| Estimate hosting/API cost from usage logs | Any tax, legal or refund wording |
| Compare competitor prices (with links) | Turning on real payments |

> *"Using my usage data and Part 2 of Launch_Plan.md, calculate cost per customer and break-even for 3 prices. Show formulas. Mark guesses as (guess). Do not choose the price."*

---

# PART 3. BUILD & QA READINESS (Development → "Safe to show people")

**Status:** Not started
*AI writes a lot of code. Humans must still check that it's safe, works, and is honest.*

## 3A. Scope: what's in version 1

**Q3.1. MUST-HAVE features** (without these the product is useless). Max 5.

| # | Feature (plain words) | Built? | Tested by a human? |
|---|---|---|---|
| 1 | [Web: create invoice / Mobile: add a plant] | [ ] | [ ] |
| 2 | [Web: send by email / Mobile: daily reminder] | [ ] | [ ] |
| 3 | | [ ] | [ ] |
| 4 | | [ ] | [ ] |
| 5 | | [ ] | [ ] |

**Q3.2. What are you deliberately NOT building yet?** (This stops endless adding.)
*Web: "Team accounts, recurring invoices." Mobile: "Social sharing, Android version."*

YOUR ANSWER:

## 3B. AI-development hygiene

**Q3.3. Tick each that is true.**
- [ ] Code is in version control (e.g., GitHub) and backed up
- [ ] A human (me or a friend) reviewed AI-written code for login, payments and user data
- [ ] A README explains how to run the product
- [ ] Secrets (passwords, API keys) are NOT in the code; they're stored safely
- [ ] Packages/dependencies were checked for known security problems
- [ ] Parts of AI code I don't understand are listed: [  ]
- [ ] Code, images, fonts and text I used have licenses that allow it
- [ ] There's a rollback (undo a bad release). How: [e.g., redeploy previous version]
- [ ] Staging copy exists (a safe place to test before real users): [URL / N/A]

## 3C. Quality checks (QA)

**Q3.4. Run these tests. Tick each and write what you found.**

| Check | Done | What I found / fixed |
|---|---|---|
| Walk the "aha moment" path (Q1.6) like a new user | [ ] | |
| Sign-up, log in, log out, forgot password | [ ] | |
| Test payment with a test card (if you charge) | [ ] | |
| Phone AND laptop (web) / 2+ real devices (mobile) | [ ] | |
| 2+ browsers (web) / small and large screens (mobile) | [ ] | |
| Bad input (empty fields, very long text, weird symbols) | [ ] | |
| Slow or no internet | [ ] | |
| Watch 1 stranger use it, silently | [ ] | |
| Automated tests/checks run (if any) | [ ] | |
| Loads in about 3 seconds or less | [ ] | |
| Security check: can someone see another user's data? | [ ] | |

**Q3.5. Bug list.**

| Bug | Severity (Blocker / Major / Minor) | Fixed? |
|---|---|---|
| [e.g., can't log in on iPhone] | Blocker | [ ] |

> **Rule:** All Blockers fixed. Majors fixed OR the risk is accepted in writing in Part 8. Minors can wait.

## 3D. Onboarding & activation flow

*Onboarding = what a brand-new user sees from first click until the aha moment. This is the biggest lever for getting to 500.*

**Q3.6. Write the first-use journey, step by step (max 6 steps).**

| Step | What the user sees/does | What could confuse them | How I'll fix it |
|---|---|---|---|
| 1 | [Web: lands on page, clicks "Start free" / Mobile: opens app] | | |
| 2 | [Sign-up] | | |
| 3 | | | |
| 4 | **[Aha moment from Q1.6]** | | |

**Q3.7. Time to aha moment.** How many minutes from first click to aha? Now: [  ] Goal: [e.g., under 3]

**Q3.8. Welcome messages.**
- [ ] Welcome email/notification sent right after sign-up
- [ ] Reminder if they didn't reach the aha moment in 24 hours
- [ ] Day-3 and Day-7 tips message
- [ ] Empty screens explain what to do next (no blank pages)
- [ ] Easy way to ask for help from inside the product

## 3E. Safety, privacy & legal basics (do not skip)

**Q3.9. Tick each or write N/A.**
- [ ] Privacy Policy page (says what data you collect and why)
- [ ] Terms of Service page
- [ ] Cookie/consent notice for EU/UK visitors (or N/A)
- [ ] Users can delete their account and data (or you know how on request)
- [ ] Passwords not stored in plain text (use a trusted login service)
- [ ] Card data handled only by the payment provider
- [ ] Children: if under-13/under-16 users are possible, rules checked (or "adults only" stated)
- [ ] Mobile: store rules checked (age rating, privacy labels, permissions explained)
- [ ] If the product uses AI features: users are told, and limits are stated
- [ ] Support email exists: [address]
- [ ] Names, logos, trademarks checked so I'm not copying someone else

**Q3.9b. Privacy laws (data rules).** *Answer for every country where your users live.*

| Question | YOUR ANSWER |
|---|---|
| Which countries/regions will my users be in? | [e.g., USA, UK, EU] |
| What personal data do I collect? (email, name, location, photos, payment info, device ID) | [  ] |
| Why do I need each one? (If you can't say why, don't collect it.) | [  ] |
| Where is the data stored (which country/provider)? | [  ] |
| Who else gets the data? (analytics, email tool, payment provider, AI provider) | [  ] |
| Do I need to ask permission first (consent) for cookies/tracking/emails? | [ ] Yes  [ ] No  [ ] Not sure → TBD |
| Can a user download or delete their data? How fast do I reply? | [e.g., within 30 days] |
| Which rules might apply? | [ ] GDPR (EU/UK)  [ ] CCPA/CPRA (California)  [ ] Other: ____ |
| What if there's a data leak? Who do I tell and how fast? | [ ] Plan written |

**Q3.9c. Store, platform & AI rules.**
- [ ] Mobile: I read the current App Store Review Guidelines / Google Play policies and fixed anything that could get me rejected
- [ ] Mobile: Privacy labels / "Data safety" form filled in honestly
- [ ] Mobile: Every permission I ask for (camera, location, notifications) is explained to the user
- [ ] Mobile: Subscriptions use the store's billing where required, and "Restore purchases" works
- [ ] Web: I read the rules of every platform I'll promote on (Product Hunt, Reddit, ad networks)
- [ ] AI features: users are told when they talk to AI or get AI-made content
- [ ] AI features: I checked my AI provider's usage rules allow my product
- [ ] AI features: the product doesn't claim to be a doctor, lawyer or financial advisor
- [ ] AI features: I have a way for users to report wrong or harmful AI answers

**Q3.9d. Marketing & money rules.**
- [ ] Marketing emails have an unsubscribe link and my real business address (anti-spam laws, e.g., CAN-SPAM, GDPR/PECR)
- [ ] Every claim on my site is true and provable ("fastest", "#1", "saves 10 hours" need proof)
- [ ] Testimonials are real, with permission; no fake reviews; paid or free-product reviews are disclosed
- [ ] Prices show the full cost (taxes, fees, renewal price, how to cancel)
- [ ] Free trials explain exactly when billing starts
- [ ] Sales tax/VAT: provider handles it, or I know the rules: [  ]
- [ ] Business is registered / I know whether I need to be: [  ]
- [ ] Open-source licenses I use allow commercial use: [ ]

> ⚖️ If you ticked "Not sure" on anything in Q3.9b-3.9d, write `TBD - by [date]` and check official sources or ask a professional **before Gate A**.

## 3F. Accessibility & localization

**Q3.10. Accessibility (can everyone use it?).**
- [ ] Text is readable (good contrast, not tiny)
- [ ] Can use with keyboard only (web) / large text setting (mobile)
- [ ] Images have text descriptions (alt text)
- [ ] Buttons are big enough to tap
- [ ] Doesn't rely on color alone to show meaning
- [ ] Ran a free checker (e.g., browser accessibility audit, built-in phone accessibility scanner)

**Q3.11. Languages and regions.**
- Launch language(s): [English]  Later: [  ]
- Countries I'll sell in: [  ]  Currency: [  ]  Date/time/number formats checked: [ ]
- Any country I will block or not serve (law/tax reasons)? [  ]

## 3G. Tracking & setup

**Q3.12. Can you SEE what users do?**
- [ ] Analytics installed (e.g., Plausible, PostHog, Google Analytics, Firebase)
- [ ] Events tracked: visit, sign-up, aha moment, payment
- [ ] Tested that events actually appear in the dashboard
- [ ] Error monitoring on (e.g., Sentry) or I check logs daily
- [ ] Domain bought: [name]  [ ] Custom email works  [ ] HTTPS works (web)
- [ ] Database backups on  [ ] Uptime alert on (tells me if site is down)

### 🛑 GATE A: "Safe to show people?"
Move to Part 4 only if ALL are true:
- [ ] All Must-Have features work (Q3.1)
- [ ] Zero Blocker bugs (Q3.5)
- [ ] First-use journey reaches aha moment (Q3.6)
- [ ] Legal basics and compliance done (Q3.9, 3.9b, 3.9c, 3.9d), no "Not sure" left
- [ ] I can see user actions in analytics (Q3.12)
- [ ] I can roll back a bad release (Q3.3)

Gate A decision: [ ] GO  [ ] NO-GO (fix list: ____)  Date: [  ]

### 🤖 AI Agent Corner: Part 3

| AI may do | Human must approve |
|---|---|
| Write and run tests, list likely bugs | Which bugs are Blockers |
| Scan code for leaked secrets and weak spots | Every security fix on login, payments, user data |
| Draft Privacy Policy / Terms (as a starting point) | Final legal text (get a lawyer/template service to check) |
| Run accessibility checks | Gate A decision |

> *"Review my repo against Part 3 of Launch_Plan.md. List every unticked item you can verify, with evidence (file/line or test output). Don't tick anything you can't prove. List all security risks. Don't change code without telling me."*

---

# PART 4. PRE-LAUNCH & BETA (First 10-50 users: learn and fix)

**Status:** Not started

## 4A. Landing page / store page

**Q4.1. A simple page exists** with: the headline (Q1.5), 3 benefits, picture/demo, ONE button.
- [ ] Live: [URL]  [ ] Email collection works (tested)  [ ] Looks fine on a phone  [ ] Loads fast

**Q4.2. Waitlist goal before launch:** [e.g., 200]  Now: [  ]

## 4B. Finding beta testers

**Q4.3. Where will you find 20-50 beta testers?** (Name real places.)

| Where | How I'll ask (1 line) | Goal # | Done |
|---|---|---|---|
| [Web: r/freelance, LinkedIn / Mobile: r/houseplants] | [honest "I built this, want feedback?" post] | [10] | [ ] |
| [Friends/family who match Q1.3] | [direct message] | [5] | [ ] |
| [Discord/Slack/Facebook groups] | | | [ ] |
| [BetaList, Product Hunt Upcoming, Indie Hackers] | | | [ ] |
| Mobile only: [TestFlight / Play Console testing track] | | | [ ] |

> Rules: be honest, follow each community's self-promotion rules, never spam, never fake accounts or reviews.

**Q4.4. What do testers get?** [e.g., free for 3 months, name in credits, direct line to me]

## 4C. Feedback loop

**Q4.5. How do testers send feedback?** (Pick at least one easy way.)
- [ ] In-app button  [ ] Short form: [link]  [ ] Email  [ ] Group chat  [ ] 15-min calls (goal: [5])

**Q4.6. Ask every tester these 5 questions:**
1. What were you trying to do?
2. What was confusing or hard?
3. What did you like most?
4. How disappointed would you be if this disappeared? (Very / Somewhat / Not)
5. Would you tell a friend? Who and why?

**Q4.7. Feedback log.**

| Date | Who | Feedback | Fix now / Later / Ignore | Done |
|---|---|---|---|---|
| | | | | [ ] |

**Q4.8. Product-market-fit signal.** Of testers who answered Q4.6 #4, `[ ]%` said "Very disappointed." (Rule of thumb: 40%+ is a strong sign.) My honest read: [  ]

## 4D. Launch assets

**Q4.9. Prepare these (tick when ready).**
- [ ] Logo & app icon  [ ] 3-5 screenshots or a 60-second demo video
- [ ] Short (1 line) and long (1 paragraph) descriptions
- [ ] 3 real testimonials *(with permission)*
- [ ] Press/social kit folder: [link]
- [ ] FAQ / help page with top 5 questions
- [ ] Mobile: store listing drafted, screenshots sized, **submitted for review at least 7 days before launch** (reviews can fail or be slow)

**Q4.10. Price check.** Ask 5 testers: "At what price is this too cheap, a bargain, getting expensive, too expensive?" Final price: [  ] Changed from Part 2? [ ] Yes [ ] No. Why: [  ]

**Q4.11. Can it handle a spike?** Estimate how many people could arrive on launch day: [  ]. Can your hosting and payment/API limits handle 10× that? [ ] Yes  [ ] Not sure → ask AI to check limits: [result]

### 🛑 GATE B: "Ready for the public?"
- [ ] At least [10] testers reached the aha moment
- [ ] Top 3 problems from feedback are fixed
- [ ] Landing page, analytics, support email all work
- [ ] Store listing approved (mobile) or domain/hosting ready (web)
- [ ] At least [3] testimonials or real usage numbers
- [ ] Spike check done (Q4.11)

Gate B decision: [ ] GO  [ ] NO-GO (why: ____)  Date: [  ]

### 🤖 AI Agent Corner: Part 4

| AI may do | Human must approve |
|---|---|
| Draft landing-page copy, FAQ, outreach posts | Everything posted publicly under your name |
| Summarize feedback and group it into themes | Which fixes you do |
| Draft interview questions | Using any tester's quote (permission) |

> *"Here is my feedback log. Group it into the top 5 themes with counts. Suggest 1 fix each and its effort (small/medium/large). Do not delete any feedback."*

---

# PART 5. LAUNCH DAY & MARKETING

**Status:** Not started

## 5A. Message

**Q5.1. Core messages.**

| Message | YOUR ANSWER |
|---|---|
| Headline (≤10 words) | |
| One-liner ("What is it?") | |
| 3 benefits (not features) | 1. 2. 3. |
| Proof (numbers, quotes, demo) | |
| Call to action ("Do this now") | [Web: "Send your first invoice free" / Mobile: "Download and add your first plant"] |

## 5B. Channels (where customers come from)

**Q5.2. Pick 3-5 channels only.** Doing everything = doing nothing.

| Channel | Why it fits my customer | What I'll do | Goal (visitors / sign-ups) | Cost |
|---|---|---|---|---|
| [ ] Product Hunt | | | | |
| [ ] Reddit / online communities | | | | |
| [ ] X / LinkedIn / Instagram / TikTok / YouTube | | | | |
| [ ] Email to my waitlist | | | | |
| [ ] SEO / blog / how-to articles | | | | |
| [ ] Hacker News / Indie Hackers | | | | |
| [ ] Direct messages / personal outreach | | | | |
| [ ] Partners, newsletters, influencers | | | | |
| [ ] Paid ads (only if budget in Part 8) | | | | |
| [ ] App Store / Play Store optimization (mobile) | | | | |
| [ ] Other: ____ | | | | |

> **Honest rule:** Write like a human. AI is for first drafts. No fake reviews, fake urgency, or spam. Follow advertising and disclosure laws.

## 5C. Launch-day schedule

**Q5.3. Launch date:** [YYYY-MM-DD]  **Time zone:** [  ]  (Avoid Fridays/holidays if your audience is business users.)

| Time | Action | Owner | Done |
|---|---|---|---|
| [08:00] | Final check: site/app up, payments work, analytics on | me | [ ] |
| [09:00] | Publish launch post on channel 1: [  ] | me | [ ] |
| [09:30] | Email the waitlist | me | [ ] |
| [10:00] | Post on channel 2: [  ] | me | [ ] |
| All day | Reply to every comment/message within [1 hour] | me | [ ] |
| [18:00] | Check numbers: visitors, sign-ups, bugs | me | [ ] |
| Night | Write quick notes (Q6.8) | me | [ ] |

**Q5.4. Launch-day safety.**
- [ ] I'm free all day  [ ] If the product breaks I will: [roll back / post status update]
- [ ] Outage message ready: [  ]  [ ] Support inbox watched

**Q5.5. First 7 days after launch.** Write the plan for each day: [Day 1: ___ Day 2: ___ ... Day 7: ___]

### 🤖 AI Agent Corner: Part 5

| AI may do | Human must approve |
|---|---|
| Draft posts, emails, titles (give 5 versions each) | Every post/email before sending |
| Make a calendar of posts | Any paid ad spend |
| Monitor mentions and summarize | Replying to people (reply as yourself) |

> *"Using Parts 1 and 5 of Launch_Plan.md, draft launch posts for each channel in my plan following each community's rules. Give 3 versions each in a human tone. No fake claims. Don't post anything."*

---

# PART 6. POST-LAUNCH: FROM 0 TO 500 CUSTOMERS

**Status:** Not started
*Weekly cycle: **Look at numbers → Pick ONE problem → Fix/test it → Repeat.***

## 6A. Milestones

**Q6.1. Path to 500** (use your Q0.1 definition).

| Milestone | Customers | Target date | Reached on | Main source |
|---|---|---|---|---|
| First customer | 1 | | | |
| Early traction | 10 | | | |
| | 50 | | | |
| | 100 | | | |
| | 250 | | | |
| **Goal** | **500** | | | |

## 6B. Weekly check-in

**Q6.2. Weekly scorecard.** *(Copy this table each week into the weekly log.)*

| Week of | Visitors | Sign-ups | Activated | Customers (total) | Come-back % | Money in ($) | New bugs |
|---|---|---|---|---|---|---|---|
| [date] | | | | | | | |

**Q6.3. Each week answer:**
1. Which channel gave the most customers? [  ]
2. Where do people quit? (Sign-up / first use / payment) [  ]
3. What is the ONE thing I'll change this week? [  ]
4. What did customers complain about most? [  ]
5. Did last week's change help? [Yes / No / Too early]

**Weekly log (paste copies here):**
```
Week of: ____
Scorecard: ____
Q6.3 answers: ____
Decision: ____
```

## 6C. Support & retention

**Q6.4. Support plan.**
- Support channel(s): [email / chat / Discord]   Reply-time promise: [24 hours]
- Top 5 questions saved in FAQ: [ ]   Bug-fix promise: [Blockers within 48 hours]
- Refund process: [policy]   Cancel process is easy and clear: [ ]
- Ask happy users for a review or testimonial: [ ]   Referral idea: [e.g., "invite a friend, both get a free month"]
- Win-back message to people who left: [ ]

**Q6.5. Retention.** Of people who joined in week 1, `[ ]%` were still active in week 4. Goal: [  ]. If low: why do I think they left? [  ]

## 6D. When growth stalls

**Q6.6. If growth stalls for 2 weeks, check in this order:**
1. [ ] Can strangers understand the product in 5 seconds? (rewrite headline)
2. [ ] Are the right people seeing it? (change channel)
3. [ ] Do people reach the aha moment? (fix onboarding)
4. [ ] Is the price/offer right? (test)
5. [ ] Talk to 5 people who left. Ask why.

**Q6.7. Customer interviews.** Talk to at least [10] real customers by customer #100. Written notes saved at: [link]

**Q6.8. Launch retrospective (write within 3 days of launch).**
- What went well: [  ]
- What went badly: [  ]
- What surprised me: [  ]
- Next 3 actions: [  ]

### 🛑 GATE C: "500 customers reached"
- [ ] 500 customers by my Q0.1 definition (proof: [screenshot/export])
- [ ] I know my top 2 channels and cost per customer: [  ]
- [ ] I wrote what worked / what didn't (Part 9)
- [ ] I picked my next move in Part 7

### 🤖 AI Agent Corner: Part 6

| AI may do | Human must approve |
|---|---|
| Pull numbers into the weekly scorecard from analytics | Reading the numbers: is it truly working? |
| Find where users drop off | Which ONE change to test |
| Draft support replies and FAQ updates | Anything sent to customers, refunds, account changes |

> *"Here is this week's analytics export. Fill the Q6.2 table, find the biggest drop-off step, and suggest 3 tests ranked by effort. Show your calculations."*

---

# PART 7. AFTER 500: NEXT STEPS

**Status:** Not started

**Q7.1. What is my decision?** (Pick one.)
- [ ] **Scale:** acquire more customers using what worked
- [ ] **Improve:** fix retention/onboarding first
- [ ] **Pivot:** change the customer, product or price (explain below)
- [ ] **Pause/Stop:** (explain below)

Why: [  ]

**Q7.2. Next goal.** [e.g., 2,000 customers by ___ / $5,000 per month by ___]

**Q7.3. Double down.** Which 1-2 channels worked best? [  ] What will I do 3× more of? [  ]

**Q7.4. Stop doing.** What didn't work and I'll stop? [  ]

**Q7.5. Product roadmap (next 90 days).** Top 3 things customers asked for most:
1. [  ]  2. [  ]  3. [  ]

**Q7.6. Help I might need.** [ ] Part-time support person  [ ] Developer/designer  [ ] Accountant/lawyer  [ ] Marketing helper  [ ] None yet

**Q7.7. Systems to build.** [ ] Automated onboarding emails  [ ] Public help center  [ ] Public status page  [ ] Customer community  [ ] Reviews/case studies page

**Q7.8. Reuse this template.** Copy lessons into the master template (Part 9, Q9.3).

### 🤖 AI Agent Corner: Part 7

> *"Read my Part 6 weekly logs and Part 9 summary. Suggest 3 possible next-90-day plans (scale / improve / pivot) with risks of each. Don't choose; I decide."*

---

# PART 8. RISKS, BUDGET & DECISION LOG

**Status:** Not started

**Q8.1. Money and time budget.**

| Item | Planned | Actual |
|---|---|---|
| Domain & hosting | | |
| AI tools / subscriptions | | |
| Ads / promotion | | |
| Design / assets | | |
| Legal / accounting | | |
| Store fees (Apple/Google developer accounts, etc.) | | |
| My hours per week on launch | | |
| **Total** | | |

**Q8.2. Top risks.**

| Risk | Likelihood (Low/Med/High) | Impact | My plan if it happens |
|---|---|---|---|
| Nobody signs up | | | Change channel, talk to users |
| Big bug on launch day | | | Roll back, post status |
| Server overloaded or API limits hit | | | Scale plan / waitlist |
| Store rejects my app (mobile) | | | Fix, resubmit, have web fallback |
| AI-written code has a security hole | | | Review, security scan |
| Data leak | | | Tell users, fix, follow the law |
| Competitor copies me | | | Focus on customers & speed |
| I burn out | | | Reduce scope, set rest days |

**Q8.3. Risks I accept (known bugs/limits and why).** [  ]

**Q8.4. Decision log.** Write important decisions so nobody (including AI agents) has to guess later.

| Date | Decision | Why | Who decided (me / AI suggested, I approved) |
|---|---|---|---|
| | | | |

**Q8.5. Open questions.**

| Question | Who/what can answer it | Due date |
|---|---|---|
| | | |

---

# PART 9. FINAL SIGN-OFF

**Q9.1. Completeness check.** Every `YOUR ANSWER:` and `[bracket]` is filled (or `TBD` with date, or `N/A` with reason)? [ ] Yes  [ ] No → go back

**Q9.2. Stranger test.** Could a friend run this launch from this file without asking you anything? [ ] Yes  [ ] No → what's unclear: [  ]

**Q9.3. Final summary (fill after reaching 500).**

| Item | YOUR ANSWER |
|---|---|
| Date 500 reached | |
| Total time taken | |
| Total money spent | |
| Cost per customer (CAC) | |
| #1 channel | |
| Biggest mistake | |
| Biggest win | |
| What I'll do differently next project | |
| Lessons added to the master template | [ ] Done |

**Sign-off**

| Role | Name | Date |
|---|---|---|
| Plan owner | | |
| Reviewer (friend/mentor, human) | | |

---

# APPENDIX: PLAIN-WORD DICTIONARY

| Word | Meaning |
|---|---|
| Launch | Opening your product to the public |
| Beta | A test version used by a small group before launch |
| Waitlist | People who asked to hear when you launch |
| Aha moment | The first time a user feels "this is useful" |
| Activation | A new user reaching the aha moment |
| Onboarding | The first-use steps that guide a new user |
| Retention | People who keep coming back |
| Churn | People who leave or cancel |
| Funnel | Steps people take: Visit → Sign up → Use → Pay |
| Channel | A place where you find customers |
| Conversion | % of people who do the next step |
| CAC | Customer acquisition cost: money spent ÷ customers gained |
| Unit economics | Does one customer earn more than they cost? |
| Break-even | The point where money earned equals money spent |
| Freemium | Free plan plus paid upgrade |
| Rollback | Going back to the last working version |
| Staging | A safe practice copy of your product |
| Blocker bug | A bug that stops people from using the product |
| Go / No-Go | Decision to continue, or stop and fix |
| Accessibility | Making the product usable by people with different abilities |
| Localization | Adapting language, currency and formats for a region |
