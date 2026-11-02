# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**Template version:** 1.2 · **Folder:** Launch, marketing and customer acquisition · **File:** `Changelog_and_Announcements.md`

## What is this document for?

This document is the single place where one project keeps:

1. **The Changelog**: a dated list of what changed in the product, written for customers.
2. **The Announcements**: the messages you send to tell people about those changes (in-app, email, social, blog, launch sites, docs, status page, app stores).
3. **The Path to 500**: what to announce and learn at each stage, from the first build until your first 500 customers have used the product.
4. **The Toolkit**: ready-made email scripts, offer kits, and AI prompts so nobody starts from a blank page.

It is built for a **solo founder working with AI agents**, but anyone can fill it in, even a 10-year-old. If you can answer a question in plain words, you can fill this in. **Every question has an example right next to it.** Copy the style of the example, not the words.

## The 6 simple rules

1. **Copy this file once per project.** Rename the copy `Changelog_and_Announcements_<ProjectName>.md`. Never edit the blank master.
2. **Go top to bottom.** Each Part builds on the one before it. Do not skip Parts 0 to 2.
3. **Answer every question.** Replace each `[ANSWER: ...]` with your answer. Delete the hint text after you answer.
4. **If you do not know, write `UNKNOWN`.** Never guess and never leave a blank. `UNKNOWN` tells the next person (or AI agent) to go find out.
5. **If something does not apply, write `N/A - because <reason>`.** A reason stops people from wondering whether you forgot.
6. **Write for the customer, not for yourself.** Say what they can now do, not what you built. Short words. Short sentences.

## How to read the symbols

| Symbol | Meaning |
|---|---|
| `[ANSWER: ...]` | Type your answer here, then delete the hint. |
| `[CHOOSE ONE: A / B / C]` | Keep exactly one option and delete the others. |
| `[CHOOSE ANY: A / B / C]` | Keep every option that is true. |
| `- [ ]` / `- [x]` | Unchecked / checked box. Change `[ ]` to `[x]` when done. |
| `UNKNOWN` | You do not know yet. Allowed, but it must be resolved before launch (list it in Part 9.3). |
| `N/A - reason` | Does not apply, with the reason. |
| `(AI)` | An AI agent may fill or draft this. A human must still approve it. |
| `(HUMAN)` | A human must decide this. AI may only suggest. |
| 🔴 **MUST** | Required before you publish anything. |
| 🟡 **SHOULD** | Strongly recommended. |
| 🟢 **COULD** | Nice to have. Skip if you are short on time. |
| **Basic** / **Advanced** | Basic = everyone answers. Advanced = answer when you reach that point or if you have the time; otherwise write `UNKNOWN`. |

## Good answer vs bad answer (learn the pattern once)

| Question | Bad answer (too vague) | Good answer (clear) |
|---|---|---|
| Who is it for? | "Users" | "Freelance designers who send 5+ invoices a month" |
| What changed? | "Improved performance" | "Pages now load in 1 second instead of 4" |
| Why does it matter? | "Better UX" | "You can finish checkout in 2 taps instead of 6" |
| Date | "Soon" | `2026-10-18` (always `YYYY-MM-DD`) |
| Number | "A lot of users" | `37` (use `UNKNOWN` if you do not have it) |
| Owner | "The team" | "Priya (priya@example.com)" |

## The 5-minute quick start (for the impatient)

1. Fill **Part 0** (who, what, where).
2. Fill **Part 1** (your 8 big decisions, made once).
3. Pick your current stage in **Part 2** and read only that stage.
4. Copy the **Release Entry Block** in Part 4 for each release and fill it.
5. Copy the **Announcement Block** in Part 5 for each channel you use.
6. Run the **Pre-Publish Checklist** in Part 7 (also 7.4 QA evidence and 7.5 compliance). Publish only when every 🔴 MUST is checked.
7. Stuck? Look at **Appendix D (a fully filled sample project)** or paste a prompt from **Part 10 (AI Prompt Library)**.

## Golden rules for AI agents reading this file

- Treat every answer in this file as the source of truth. If two answers conflict, **stop and ask the human**. Do not pick one.
- Never invent a number, a customer name, a quote, a date, or a feature. Write `UNKNOWN` and add it to Part 9.3 (Open Questions).
- Never publish, send, post, or schedule anything. Draft it, mark `STATUS: READY FOR HUMAN REVIEW`, and stop.
- Use only the words from the **Voice and Words** table in Part 1.4.
- Full agent rules are in **Part 8**. Ready-made prompts are in **Part 10**.

## Map of this document

| Part | What is inside |
|---|---|
| 0 | Project identity |
| 1 | The 8 big decisions |
| 2 | The path from build to 500 customers (8 stages) |
| 3 | How a change travels from code to customer |
| 4 | The Changelog (rules, block, example, log) |
| 5 | The Announcements (blocks for every channel) |
| 6 | When things go wrong |
| 7 | Checklists (writing, product test, pre-publish, QA evidence, compliance and privacy) |
| 8 | Rules for AI agents |
| 9 | Measure and learn (metrics, retrospective, feedback, analytics and attribution) |
| 10 | AI Prompt Library |
| 11 | Email scripts (waitlist, beta, launch, onboarding, milestones) |
| 12 | Offers, pricing, and referral kit |
| 13 | Final completeness check |
| Appendix A-D | Glossary, cheat sheet, revision history, filled sample project |

---

# PART 0. PROJECT IDENTITY (fill once per project)

## 0.1 Basics

| Question | Example | Your answer |
|---|---|---|
| Q0.1 What is the product's name? (**Basic**) | "InvoiceBuddy" | [ANSWER] |
| Q0.2 Describe it in one sentence a child would understand. (**Basic**) | "It helps freelancers send invoices and get paid faster." | [ANSWER] |
| Q0.3 Who is it for? Name one specific type of person. (**Basic**) | "Freelance designers who send 5+ invoices a month" | [ANSWER] |
| Q0.4 What problem does it solve for them? (**Basic**) | "They waste hours making invoices and chasing late payments." | [ANSWER] |
| Q0.5 Product type (**Basic**) | "Web app" | [CHOOSE ONE: Web app / Mobile app / Desktop app / API or developer tool / Browser extension / Plugin / Physical + software / Other: ___] |
| Q0.6 Where do customers use it? Give links. (**Basic**) | "https://invoicebuddy.example.com" | [ANSWER] |
| Q0.7 Project owner (HUMAN) (**Basic**) | "Priya Shah, priya@example.com" | [ANSWER] |
| Q0.8 Today's date (**Basic**) | `2026-10-18` | [ANSWER: YYYY-MM-DD] |
| Q0.9 Target date for first public launch (**Basic**) | `2027-01-12` | [ANSWER: YYYY-MM-DD or UNKNOWN] |
| Q0.10 Which stage are you in right now? (**Basic**) | "Testing" | [CHOOSE ONE: Idea and Build / Test / Pre-launch / Launch day / Customers 0-10 / 11-50 / 51-200 / 201-500 / 500 reached] |
| Q0.11 What is your single biggest goal for the first 500 customers? (**Basic**) | "500 designers send at least one invoice by 2027-09-30." | [ANSWER] |
| Q0.12 What is your rough budget for marketing per month? (**Advanced**) | "$0 for now" or "$300" | [ANSWER or UNKNOWN] |

## 0.2 Where things live (so nobody has to guess)

| Item | Example | Link or location |
|---|---|---|
| Source code repository | "github.com/priya/invoicebuddy" | [ANSWER: URL] |
| Task or issue tracker | "Linear project IB" | [ANSWER: URL] |
| Public changelog page | "invoicebuddy.example.com/changelog" | [ANSWER: URL, or "will create at ___"] |
| Product docs / help center | "help.invoicebuddy.example.com" | [ANSWER: URL or N/A - reason] |
| Status page | "status.invoicebuddy.example.com" | [ANSWER: URL or N/A - reason] |
| Customer feedback inbox | "hello@invoicebuddy.example.com" | [ANSWER: email, form, or tool] |
| Analytics dashboard | "plausible.io/invoicebuddy" | [ANSWER: URL] |
| Brand assets (logo, colors, screenshots) | "Drive folder /Brand" | [ANSWER: folder link] |
| Email-sending tool | "Resend" or "Mailchimp" | [ANSWER: tool name] |
| Customer-count source of truth | "Admin page > Customers > count where first_invoice_sent = true" | [ANSWER: where the real "number of customers" comes from] |

## 0.3 Document control

| Field | Example | Value |
|---|---|---|
| Document owner (HUMAN) | "Priya" | [ANSWER] |
| Last updated | `2026-10-18` | [ANSWER] |
| Who may edit | "Priya + AI agents" | [ANSWER] |
| Who must approve public messages | "Priya (one person only)" | [ANSWER] |

---

# PART 1. THE 8 BIG DECISIONS (make once, reuse forever)

These choices keep every message consistent. Make them once. Change them only on purpose.

## 1.1 Versioning (how you number releases)

Default is **Semantic Versioning**: `MAJOR.MINOR.PATCH` (example `1.4.2`).

| Part | Increase it when... | Example |
|---|---|---|
| MAJOR (1.x.x → 2.0.0) | Something breaks or works very differently for existing users | Old export format removed |
| MINOR (1.4.x → 1.5.0) | You add a feature and nothing breaks | New "Dark mode" |
| PATCH (1.4.2 → 1.4.3) | You fix a bug and add nothing new | Fixed a crash on login |

| Question | Example | Your answer |
|---|---|---|
| Q1.1 Which versioning do you use? (**Basic**) | "Semantic Versioning" | [CHOOSE ONE: Semantic Versioning (recommended) / Other: ___] |
| Q1.2 What is the first public version number? (**Basic**) | "0.1.0 before launch, 1.0.0 at public launch" | [ANSWER] |
| Q1.3 What counts as a "release"? (**Basic**) | "Every time we deploy to production" | [ANSWER] |
| Q1.4 Pre-release labels you will use (**Advanced**) | "-beta" | [CHOOSE ANY: `-alpha` / `-beta` / `-rc.1` / none] |

## 1.2 Changelog categories (the only labels allowed)

Based on the widely used *Keep a Changelog* format. Use **only** these labels:

| Label | Use it for | Customer-friendly example |
|---|---|---|
| **Added** | A brand new thing | "You can now export reports as PDF." |
| **Changed** | Something works differently | "The dashboard now opens on the Invoices tab." |
| **Deprecated** | Something will be removed later | "The old import tool will go away on 2027-01-31." |
| **Removed** | Something is gone | "We removed the legacy theme." |
| **Fixed** | A bug is repaired | "Fixed a bug that logged people out too early." |
| **Security** | A safety or privacy fix | "Fixed a way someone could view another person's invoice." |
| **Performance** (optional) | Faster or lighter | "Reports now load 3x faster." |

| Question | Example | Your answer |
|---|---|---|
| Q1.5 Use the optional **Performance** label? (**Basic**) | "Yes" | [CHOOSE ONE: Yes / No] |

## 1.3 Who reads your messages? (audience)

| Audience | Example answer: gets announcements? | Gets announcements? | What do they care about? (example → yours) |
|---|---|---|---|
| New visitors who have not signed up | "Yes (blog and social only)" | [CHOOSE ONE: Yes / No] | "Is this worth my time?" → [ANSWER] |
| Free users | "Yes" | [CHOOSE ONE: Yes / No] | "What can I do for free?" → [ANSWER] |
| Paying customers | "Yes, first" | [CHOOSE ONE: Yes / No] | "Is it reliable? Did anything break?" → [ANSWER] |
| Developers or API users | "N/A - no API yet" | [CHOOSE ONE: Yes / No / N/A] | "Will my code still work?" → [ANSWER] |
| Press, creators, partners | "No" | [CHOOSE ONE: Yes / No] | "Is there a story?" → [ANSWER] |

## 1.4 Voice and Words

| Question | Example | Your answer |
|---|---|---|
| Q1.6 Pick 3 words that describe how you sound. (**Basic**) | "friendly, clear, honest" | [ANSWER] |
| Q1.7 Pick 3 things you NEVER do. (**Basic**) | "no hype words, no blaming customers, no jargon" | [ANSWER] |
| Q1.8 Reading level target (**Basic**) | "Age 10" | [CHOOSE ONE: Age 10 (recommended) / Age 14 / Professional] |
| Q1.9 Spelling (**Basic**) | "US" | [CHOOSE ONE: US / UK / Other: ___] |
| Q1.10 Emoji use (**Advanced**) | "At most one per social post, none in changelog" | [ANSWER] |

**Word list** (add more rows as you go):

| Instead of this word | Always say this | Why |
|---|---|---|
| "Leverage", "utilize" | "use" | Simpler |
| "Seamless", "revolutionary" | (delete it, show the proof instead) | Hype words are not believed |
| [ANSWER] | [ANSWER] | [ANSWER] |

**Names to spell exactly** — Example: "InvoiceBuddy (one word, capital I and B), Pro plan, Free plan." Yours: [ANSWER]

## 1.5 Channels (where you will talk)

For each channel choose **ON**, **LATER**, or **NEVER**, and name the owner.

| Channel | Example | ON / LATER / NEVER | Owner | Used for |
|---|---|---|---|---|
| In-app notice or "What's new" popup | "ON, Priya" | [ANSWER] | [ANSWER] | Telling current users about changes |
| Email to users | "ON, Priya" | [ANSWER] | [ANSWER] | Bigger news, welcome, milestones |
| Social media (list which: X, LinkedIn, ...) | "ON for LinkedIn, LATER for X" | [ANSWER] | [ANSWER] | Reach and trust |
| Community (Discord, Slack, Reddit, ...) | "LATER" | [ANSWER] | [ANSWER] | Two-way talk |
| Blog post | "ON for size L only" | [ANSWER] | [ANSWER] | Story behind big releases |
| Launch sites (Product Hunt, ...) | "ON for launch day only" | [ANSWER] | [ANSWER] | Launch-day attention |
| Docs / help center | "ON" | [ANSWER] | [ANSWER] | How-to for changes |
| Status page | "LATER" | [ANSWER] | [ANSWER] | Outages and fixes |
| App store release notes | "N/A - no app" | [ANSWER] | [ANSWER] | Store "What's new" text |
| Public changelog page | "ON" | [ANSWER] | [ANSWER] | The permanent record |

## 1.6 How big is this change? (the 4-size rule)

Use this table to decide **how loudly** to announce. It saves you from guessing.

| Size | Looks like | Where to announce |
|---|---|---|
| **XS** | Small fix, no one will notice | Changelog only |
| **S** | Small improvement | Changelog + in-app note |
| **M** | A real new feature | Changelog + in-app + email + 1 social post + docs update |
| **L** | A launch, big redesign, pricing change, or anything that can break things | Everything in M + blog post + launch sites + community + a plan for questions |

| Question | Example | Your answer |
|---|---|---|
| Q1.11 Any change that touches **money, privacy, or deleting data** is automatically size **L**. (**Basic**) | "Agreed" | [CHOOSE ONE: Agreed / Change this rule to: ___] |

## 1.6.1 Who approves and how fast?

| Size | Example | Approver (HUMAN) | Max time to approve |
|---|---|---|---|
| XS | "Priya, same day" | [ANSWER] | [ANSWER] |
| S | "Priya, same day" | [ANSWER] | [ANSWER] |
| M | "Priya, 2 days" | [ANSWER] | [ANSWER] |
| L | "Priya + a friend reads it, 3 days" | [ANSWER] | [ANSWER] |

## 1.7 When do you send? (timing rules)

| Question | Example | Your answer |
|---|---|---|
| Q1.12 Best days and times to send email (**Advanced**) | "Tue-Thu, 10:00, customer's local time" or `UNKNOWN` | [ANSWER] |
| Q1.13 Time zone for all dates in this document (**Basic**) | "UTC" | [ANSWER] |
| Q1.14 Never send on (**Basic**) | "Fridays after 15:00, public holidays" | [ANSWER] |
| Q1.15 Max marketing emails per customer per month (**Basic**) | "4" | [ANSWER: number] |

## 1.8 Rules you must follow (legal and trust)

- [ ] 🔴 MUST: Every marketing email has an unsubscribe link and your postal or business address where the law requires it.
- [ ] 🔴 MUST: Never claim a feature exists before it ships.
- [ ] 🔴 MUST: Never use fake customer counts, fake reviews, or made-up quotes.
- [ ] 🔴 MUST: Get written permission before naming a customer or using their words.
- [ ] 🔴 MUST: Security fixes are described honestly but without giving attackers a recipe.
- [ ] 🟡 SHOULD: Check local rules for your customers' countries (privacy, marketing email, app store, ad claims).

| Question | Example | Your answer |
|---|---|---|
| Q1.16 Which countries or regions do your customers live in? (**Basic**) | "US, UK, Canada" | [ANSWER or UNKNOWN] |
| Q1.17 Special rules for your industry (health, finance, children, ...)? (**Basic**) | "Handles payments, so we must not promise guaranteed income." | [ANSWER or N/A - reason] |

---

# PART 2. THE PATH FROM BUILD TO 500 CUSTOMERS (AI-driven life cycle)

Find your current stage from Q0.10. **Read only that stage now.** Move to the next one when the **Exit test** is true.

> **AI agents:** at every stage, the agent drafts and the human approves. See Part 8.

## Stage map

| Stage | Name | Main goal | Exit test (move on when TRUE) |
|---|---|---|---|
| 1 | Idea and Build | Have something that works | A person can finish the main task start to finish |
| 2 | Test | Find and fix problems | Test checklist (Part 7.2) passes |
| 3 | Pre-launch | People are waiting | At least [ANSWER: number, e.g. 100] people on the waiting list |
| 4 | Launch day | First real users | First active user appears |
| 5 | Customers 0-10 | Learn from each person | 10 customers used the product at least once |
| 6 | Customers 11-50 | Find what works | Same message brought in customers 3 times |
| 7 | Customers 51-200 | Make it repeatable | A weekly routine exists and runs without panic |
| 8 | Customers 201-500 | Prove it grows | 500 customers have used the product |

| Question | Example | Your answer |
|---|---|---|
| Q2.1 What counts as a "customer"? Decide once. (**Basic**) | "Someone who sent their first real invoice" | [CHOOSE ONE: Signed up / Completed first key action / Paid / Other: ___] and write it in words: [ANSWER] |

## Stage 1. Idea and Build

| Question | Example | Your answer |
|---|---|---|
| Q2.2 What are the 3 must-have features for launch? (**Basic**) | "1. Create invoice 2. Send by email 3. See who paid" | [ANSWER] |
| Q2.3 What is deliberately NOT in version 1? (**Basic**) | "No mobile app, no multi-currency" | [ANSWER] |
| Q2.4 Which build work is done by AI agents? (**Basic**) | "Writing code drafts, tests, help articles, changelog drafts" | [ANSWER] |
| Q2.5 What do you write in the changelog while building? (**Basic**) | "One line under `[Unreleased]` after every finished task" | Keep one running `## [Unreleased]` section (see Part 4). |
| Q2.6 Announcements at this stage (**Basic**) | "Build-in-public post every Friday" | [CHOOSE ANY: None yet / Build-in-public posts / "Coming soon" page / Founder diary] |

**AI habit:** after every finished task, the agent adds one plain-language line under `[Unreleased]` in Part 4 and labels it with a Part 1.2 category.

## Stage 2. Test

| Question | Example | Your answer |
|---|---|---|
| Q2.7 Who tests? (**Basic**) | "5 beta users + AI test agent" | [ANSWER] |
| Q2.8 How do testers report problems? (**Basic**) | "A Google Form" | [ANSWER: form or email] |
| Q2.9 How do you tell beta testers about changes? (**Basic**) | "Weekly beta email" | [CHOOSE ONE: Weekly beta changelog email / In-app notes / Private group post] |
| Q2.10 Name of the beta release line (**Advanced**) | `0.9.0-beta.1` | [ANSWER] |

Beta tester message must always contain: **what changed, what to test, how to report a problem, by when.** Script in Part 11.

## Stage 3. Pre-launch

| Question | Example | Your answer |
|---|---|---|
| Q2.11 Where do people join the waiting list? (**Basic**) | "invoicebuddy.example.com/join" | [ANSWER: link] |
| Q2.12 What do you promise them? (**Basic**) | "Early access and 30% off for the first year." | [ANSWER: one sentence you can truly keep] |
| Q2.13 Teaser dates (**Basic**) | "T-14, T-7, T-1" | [ANSWER] |
| Q2.14 Launch-day checklist owner (HUMAN) (**Basic**) | "Priya" | [ANSWER] |
| Q2.15 Launch site chosen (**Advanced**) | "Product Hunt on a Tuesday" | [ANSWER or N/A - reason] |

**Countdown plan** (fill the dates; example in the last column of the first row):

| When | What goes out | Channel | Owner | Done |
|---|---|---|---|---|
| T-14 days | Teaser: the problem you solve | [ANSWER, e.g. LinkedIn post] | [ANSWER] | - [ ] |
| T-7 days | Sneak peek: screenshot or short video | [ANSWER] | [ANSWER] | - [ ] |
| T-1 day | "Tomorrow" reminder to waiting list | Email | [ANSWER] | - [ ] |
| T-0 (launch) | Main announcement set (Part 5) | All ON channels | [ANSWER] | - [ ] |
| T+1 day | Thank-you + first numbers | [ANSWER] | [ANSWER] | - [ ] |
| T+7 days | "What we learned in week 1" | [ANSWER] | [ANSWER] | - [ ] |

## Stage 4. Launch day

| Question | Example | Your answer |
|---|---|---|
| Q2.16 Release tag for launch (**Basic**) | `1.0.0` | [ANSWER] |
| Q2.17 Who answers questions for the first hours, and for how long? (**Basic**) | "Priya, first 6 hours" | [ANSWER] |
| Q2.18 If something breaks on launch day, who writes the correction notice (Part 6)? (**Basic**) | "Priya, using the Part 6 template" | [ANSWER] |
| Q2.19 Which Part 5 blocks go out on launch day? (**Basic**) | "In-app, email, LinkedIn, Product Hunt, blog" | [ANSWER] |

Every ON channel gets one message from the Part 5 blocks: **same story, different length.**

## Stage 5. Customers 0-10 ("one by one")

| Question | Example | Your answer |
|---|---|---|
| Q2.20 How will you talk to each of the first 10 personally? (**Basic**) | "A personal email within 24 hours, offer a 15-minute call" | [CHOOSE ANY: Personal email / Call / Chat / Other] |
| Q2.21 What 3 questions do you ask every one of them? (**Basic**) | "What nearly stopped you from signing up? What did you try before? What is still annoying?" | [ANSWER] |
| Q2.22 How do you thank them? (**Basic**) | "A handwritten-style email from me, plus free Pro for 3 months" | [ANSWER] |
| Q2.23 Changelog style at this stage (**Basic**) | "Warm and personal, with 'you asked, we built it' lines" | [ANSWER] |

## Stage 6. Customers 11-50 ("find the pattern")

| Question | Example | Your answer |
|---|---|---|
| Q2.24 Which 2 channels brought the most customers? (**Basic**) | "LinkedIn and a freelancer Slack group" | [ANSWER or UNKNOWN] |
| Q2.25 What do customers praise most? (use their words only with permission) (**Basic**) | "'I finally know who paid.'" (with permission from Sam) | [ANSWER] |
| Q2.26 What do customers complain about most? (**Basic**) | "Cannot add my logo" | [ANSWER] |
| Q2.27 What is the next **M**-size release to announce? (**Basic**) | "Logo upload" | [ANSWER] |
| Q2.28 Your regular changelog rhythm (**Basic**) | "Every 2 weeks, on Thursday" | [CHOOSE ONE: Weekly / Every 2 weeks / Monthly / Each release] |

## Stage 7. Customers 51-200 ("make it a routine")

| Question | Example | Your answer |
|---|---|---|
| Q2.29 Weekly announcement routine (who, what day) (**Basic**) | "Priya, Thursday 10:00: changelog + in-app note" | [ANSWER] |
| Q2.30 Do you segment customers (new / active / quiet)? (**Advanced**) | "Yes: new = under 14 days, active = sent 1+ invoice in 30 days, quiet = none in 30 days" | [CHOOSE ONE: Yes, as follows: ___ / Not yet] |
| Q2.31 Do you ask for reviews or testimonials? When? (**Basic**) | "14 days after their first paid invoice" | [ANSWER] |
| Q2.32 Do you have a public roadmap or "vote for features"? (**Advanced**) | "Yes: a public Trello board" | [CHOOSE ONE: Yes: link / No / LATER] |
| Q2.33 Quiet customers: what message wakes them up? (**Basic**) | "A 2-line email with one tip and a link" | [ANSWER] |

## Stage 8. Customers 201-500 ("prove it grows")

| Question | Example | Your answer |
|---|---|---|
| Q2.34 Which message to which customers produced the best results? (**Basic**) | "The 'you asked, we built it' email to quiet customers: 18% came back" | [ANSWER or UNKNOWN] |
| Q2.35 Milestone messages planned (250, 500)? (**Basic**) | "Thank-you email at 250, public post at 500" | [ANSWER] |
| Q2.36 What will you announce at **500 customers**? (**Basic**) | "Thank-you post, a case study, a retrospective, an offer for referrals" | [ANSWER] |
| Q2.37 What do you do next after 500? (**Basic**) | "Start paid ads, add a team plan" | [ANSWER] |

## Milestone tracker (update weekly)

| Customers reached | Date | Release version live | Message that helped most | What we learned |
|---|---|---|---|---|
| 1 | [ANSWER, e.g. 2027-01-12] | [ANSWER, e.g. 1.0.0] | [ANSWER] | [ANSWER] |
| 10 | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| 50 | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| 100 | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| 200 | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| 300 | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| 500 | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |

---

# PART 3. HOW A CHANGE TRAVELS (from code to customer)

Follow this flow for every release. No step may be skipped for size **M** or **L**.

| Step | What happens | Who | Proof (link or note) |
|---|---|---|---|
| 1. Change is made | Code, design, or content change is finished | (AI) + HUMAN | [ANSWER: link to task] |
| 2. Entry written | One line added in Part 4 under `[Unreleased]` | (AI) | [ANSWER] |
| 3. Tested | Passed the checklist in Part 7.2 | HUMAN + (AI) | [ANSWER] |
| 4. Size chosen | XS / S / M / L from Part 1.6 | (HUMAN) | [ANSWER] |
| 5. Drafts written | Part 5 blocks drafted for each channel | (AI) | [ANSWER] |
| 6. Approved | Approver from Part 1.6.1 says yes | (HUMAN) | [ANSWER] |
| 7. Released | Version number set, `[Unreleased]` becomes the new version | HUMAN | [ANSWER] |
| 8. Published | Channels updated in the order in Part 5.1 | HUMAN | [ANSWER] |
| 9. Watched | Feedback and numbers checked (Part 9) | HUMAN + (AI) | [ANSWER] |

---

# PART 4. THE CHANGELOG (the permanent record)

## 4.1 Rules for every line

1. **Start with a verb**: "Added", "You can now", "Fixed".
2. **One change per line.** Do not squeeze two changes into one line.
3. **Say what the customer gets**, then optionally how.
4. **No secret words**: no ticket numbers or code names in the customer text (put them in the "Internal reference" field instead).
5. **Newest release on top.** Dates as `YYYY-MM-DD`.
6. **Never rewrite history.** To correct a mistake, add a new line in a new release.
7. Mark breaking changes with **BREAKING** in capitals and add a "What you need to do" line.

**Rewrite test** (every line must pass):

| Bad line (developer words) | Good line (customer words) |
|---|---|
| "Refactored invoice service, fixed N+1 query" | "Invoices now open about 3x faster." |
| "Fix #482" | "Fixed a bug that showed the wrong total on invoices with discounts." |
| "Updated deps" | (leave it out of the customer changelog unless it changes something they notice) |

## 4.2 The Release Entry Block (copy this block for every release)

```
## [VERSION NUMBER] - YYYY-MM-DD

SIZE: [XS / S / M / L]
RELEASE TYPE: [MAJOR / MINOR / PATCH / PRE-RELEASE]
STATUS: [DRAFT / READY FOR HUMAN REVIEW / APPROVED / PUBLISHED]
ONE-LINE SUMMARY (max 20 words, customer words): [ANSWER]

### Added
- [ANSWER: You can now ... ]

### Changed
- [ANSWER: ...]

### Deprecated
- [ANSWER: ... will be removed on YYYY-MM-DD. Use ... instead.]

### Removed
- [ANSWER: ...]

### Fixed
- [ANSWER: Fixed ...]

### Security
- [ANSWER: Fixed ... (say what is now safe, not how it was broken)]

### Performance (optional)
- [ANSWER: ... now takes X instead of Y]

BREAKING CHANGE?: [Yes / No]
IF YES, WHAT YOU NEED TO DO: [ANSWER: numbered steps]
WHO IS AFFECTED: [ANSWER: e.g. "everyone who used the old export"]
HOW TO TURN BACK / ROLLBACK PLAN: [ANSWER or N/A - reason]
KNOWN ISSUES (be honest): [ANSWER or "None known"]
LEARN MORE LINK (docs or blog): [ANSWER]
THANKS TO (only with permission): [ANSWER or N/A]
INTERNAL REFERENCE (not shown to customers): [ANSWER: task IDs, pull requests, commit range]
TESTED BY / PROOF: [ANSWER: link to test result or checklist]
APPROVED BY: [ANSWER: name + date]
```

Delete any empty category before publishing. Do not leave headings with nothing under them.

## 4.3 The `[Unreleased]` section (always keep this at the top)

```
## [Unreleased]
- Added: [ANSWER]
- Fixed: [ANSWER]
```

## 4.4 Example of a finished entry (copy the style, not the words)

```
## 1.4.0 - 2026-10-18

SIZE: M
RELEASE TYPE: MINOR
STATUS: PUBLISHED
ONE-LINE SUMMARY: You can now send invoices in 12 languages and fix a login bug.

### Added
- You can now send invoices in 12 languages. Pick one when you create an invoice.

### Fixed
- Fixed a bug that signed people out after 5 minutes. It now takes 30 days.

BREAKING CHANGE?: No
KNOWN ISSUES: Arabic invoices do not yet right-align the totals. We are fixing it.
LEARN MORE LINK: https://example.com/blog/languages
```

## 4.5 THE CHANGELOG LOG (newest on top, paste each release block below this line)

[ANSWER: paste your `## [Unreleased]` block first, then each release block, newest to oldest]

---

# PART 5. THE ANNOUNCEMENTS

## 5.1 What goes out, in what order

1. **Publish the changelog entry first** (it is the permanent record and the link everything else points to).
2. **Update docs/help center** so links in messages work.
3. **In-app notice**, then **email**, then **social and community**, then **blog and launch sites** (as chosen in Part 1.6).
4. **Status page / app store text** if the change affects them.
5. Post **one** reply thread for questions. Say where people can ask.

## 5.2 The 5 questions every announcement must answer

1. **What is new?** (one sentence)
2. **Who is it for?**
3. **Why should they care?** (what gets easier, faster, cheaper, safer)
4. **What do they do next?** (one button or link)
5. **Where do they get help?**

If a draft does not answer all five, it is not ready.

## 5.3 The Master Announcement Brief (fill once per release; all channels copy from this)

```
RELEASE VERSION: [ANSWER, e.g. 1.5.0]
SIZE: [XS / S / M / L]
ONE-SENTENCE NEWS: [ANSWER, e.g. "You can now add your logo to every invoice."]
WHO IS IT FOR: [ANSWER, e.g. "Freelancers who want invoices that look professional."]
WHY THEY SHOULD CARE (3 bullets max):
- [ANSWER, e.g. "Clients trust branded invoices more."]
- [ANSWER]
- [ANSWER]
PROOF (a real number, screenshot, or short demo; no made-up proof): [ANSWER or UNKNOWN]
THE ONE ACTION WE WANT THEM TO TAKE: [ANSWER, e.g. "Upload your logo."]
LINK FOR THAT ACTION: [ANSWER]
HELP LINK: [ANSWER]
WHAT WE MUST NOT SAY (risky claims): [ANSWER, e.g. "Do not say this makes clients pay faster."]
ASSETS READY (image, GIF, video): [ANSWER: link or "none"]
PUBLISH DATE AND TIME: [ANSWER: YYYY-MM-DD HH:MM + time zone]
```

## 5.4 Channel blocks (copy only the ones you marked ON in Part 1.5)

### A. In-app "What's new" notice (keep it tiny)

```
TITLE (max 6 words): [ANSWER, e.g. "Add your logo"]
BODY (max 25 words, 1 sentence): [ANSWER, e.g. "Upload your logo once and it shows on every invoice."]
BUTTON TEXT (2-3 words): [ANSWER, e.g. "Upload logo"]
BUTTON LINK: [ANSWER]
SHOW TO: [CHOOSE ANY: All users / Paying users / New users only]
SHOW WHEN: [ANSWER: e.g. next login, once only]
CAN THE USER DISMISS IT?: Yes (always)
```

### B. Email

```
SEGMENT (who gets it): [ANSWER, e.g. "All active users"]
FROM NAME AND ADDRESS: [ANSWER, e.g. "Priya from InvoiceBuddy <hello@...>"]
SUBJECT LINE (max 50 characters): [ANSWER, e.g. "Your logo, on every invoice"]
SUBJECT LINE ALTERNATIVE FOR TESTING: [ANSWER or N/A]
PREVIEW TEXT (max 90 characters): [ANSWER]
GREETING: [ANSWER: e.g. "Hi {first_name},"]
PARAGRAPH 1 (the news, 2 sentences max): [ANSWER]
PARAGRAPH 2 (why it matters, 2 sentences max): [ANSWER]
BULLETS (max 3): [ANSWER]
BUTTON TEXT AND LINK: [ANSWER]
SIGN-OFF AND NAME: [ANSWER]
FOOTER (unsubscribe link + business address): [ANSWER]
SEND TIME: [ANSWER]
TEST SENT TO MYSELF AND LINKS CHECKED: - [ ]
```

### C. Social post (write one short version per network you use)

```
NETWORK: [X / LinkedIn / Facebook / Instagram / TikTok / YouTube / Other: ___]
POST TEXT (stay within the network's limit): [ANSWER]
IMAGE OR VIDEO: [ANSWER: link + alt text describing it for blind readers]
LINK: [ANSWER]
HASHTAGS (max 3): [ANSWER or N/A]
WHO WILL REPLY TO COMMENTS AND WHEN: [ANSWER]
POST TIME: [ANSWER]
```

### D. Community post (Discord, Slack, Reddit, forum)

```
COMMUNITY AND CHANNEL: [ANSWER]
READ THE RULES ON SELF-PROMOTION? [CHOOSE ONE: Yes, it is allowed / No, ask a moderator first]
TITLE: [ANSWER: honest, not clickbait]
BODY (tell a short story: problem, what you built, what you want feedback on): [ANSWER]
ASK FOR FEEDBACK ON: [ANSWER]
```

### E. Blog post (for size L, or a story worth telling)

```
TITLE (max 60 characters): [ANSWER]
URL SLUG: [ANSWER]
INTRO (the 5 answers from 5.2 in 3 sentences): [ANSWER]
SECTION 1: THE PROBLEM IN CUSTOMER WORDS: [ANSWER]
SECTION 2: WHAT'S NEW (with a screenshot or short video each): [ANSWER]
SECTION 3: HOW TO TRY IT IN 3 STEPS: [ANSWER]
SECTION 4: WHAT'S NEXT (only promises you can keep): [ANSWER]
CALL TO ACTION: [ANSWER]
SEARCH DESCRIPTION (max 155 characters): [ANSWER]
IMAGE ALT TEXTS FILLED IN: - [ ]
```

### F. Launch site listing (Product Hunt, directories, Show HN, etc.)

```
SITE: [ANSWER]
NAME (exact): [ANSWER]
TAGLINE (max 60 characters, plain words): [ANSWER]
DESCRIPTION: [ANSWER: what it is, who it is for, why now]
FIRST COMMENT FROM THE MAKER (a short personal story): [ANSWER]
GALLERY ITEMS (images, GIF, video): [ANSWER]
LAUNCH DATE AND TIME: [ANSWER]
WHO ANSWERS COMMENTS ALL DAY: [ANSWER]
SPECIAL OFFER (if any, true and clear): [ANSWER or N/A]
RULES CHECKED (no vote begging, no fake accounts): - [ ]
```

### G. Docs / help center update

```
PAGES TO ADD OR EDIT: [ANSWER: links]
NEW "HOW TO" STEPS: [ANSWER]
SCREENSHOTS REPLACED: [CHOOSE ONE: Yes / No / N/A]
OLD INSTRUCTIONS REMOVED OR MARKED OUTDATED: - [ ]
```

### H. Status page note (only for outages or maintenance)

```
TYPE: [CHOOSE ONE: Planned maintenance / Incident / Resolved]
WHAT IS HAPPENING (plain words): [ANSWER]
WHO IS AFFECTED: [ANSWER]
NEXT UPDATE BY: [ANSWER: time]
```

### I. App store "What's new" text

```
STORE: [CHOOSE ANY: Apple App Store / Google Play / Chrome Web Store / Other / N/A - no app]
TEXT (max 4 short lines, no version-number-only text): [ANSWER]
STORE LIMITS AND RULES CHECKED (no pricing talk or competitor names where banned): - [ ]
```

## 5.5 Special announcement types (use the matching mini-form)

| Type | When | Must include |
|---|---|---|
| **Launch** | First public release | The 5 answers, a thank-you, a link to try, the offer if any |
| **Feature release** | New thing, size M | What, why, how to try, where to give feedback |
| **Improvement / fix roundup** | Many small items | A short bullet list plus a "see everything" link |
| **Breaking change / deprecation** | Something will stop working | Date, who is affected, exact steps, a way to ask for help, at least [ANSWER: 30] days notice |
| **Price or plan change** | Money changes | Old vs new, start date, what happens to current customers, how to cancel; always size L |
| **Security notice** | Safety fix | What was fixed, whether data was affected, what customers should do, honest timing |
| **Outage / correction** | Something went wrong | Say sorry in one line, what happened, what is fixed, how you will prevent it |
| **Milestone** | 10, 50, 100, 250, 500 customers | A real thank-you, a real number, what is next |
| **Sunset / shutdown** | A feature or product ends | Date, reason, how to export data, alternatives |

---

# PART 6. WHEN THINGS GO WRONG (corrections, rollbacks, incidents)

| Question | Example | Your answer |
|---|---|---|
| Q6.1 Who decides to roll back a release? (HUMAN) (**Basic**) | "Priya" | [ANSWER] |
| Q6.2 How fast must customers hear about a serious problem? (**Basic**) | "Within 1 hour" | [ANSWER] |
| Q6.3 Where will you post the first notice? (**Basic**) | "Status page, then email, then in-app banner" | [ANSWER] |
| Q6.4 Who writes the "we're sorry" message? (**Basic**) | "Priya, using the template below" | [ANSWER] |

**Correction message template** (copy):

```
WHAT HAPPENED (1 sentence, no excuses): [ANSWER, e.g. "Some invoices showed the wrong total between 9:00 and 10:30."]
WHO WAS AFFECTED: [ANSWER, e.g. "About 14 customers."]
WHAT WE FIXED OR ARE FIXING: [ANSWER]
WHAT YOU NEED TO DO (if anything): [ANSWER, e.g. "Resend the invoice from the Invoices page."]
WHEN WE WILL UPDATE YOU AGAIN: [ANSWER]
HOW WE WILL STOP THIS HAPPENING AGAIN: [ANSWER]
```

**Rules:** Own the problem. Do not blame customers, vendors, or AI. Fix the changelog by adding a new entry, not by deleting the old one.

---

# PART 7. CHECKLISTS (quality gates)

## 7.1 Writing quality checklist (for every message)

- [ ] 🔴 MUST: It answers the 5 questions in Part 5.2.
- [ ] 🔴 MUST: Every fact, number, and date has been checked against the source.
- [ ] 🔴 MUST: No feature is promised that has not shipped.
- [ ] 🔴 MUST: Links open the right page (click every one).
- [ ] 🔴 MUST: Names, versions, and plan names are spelled exactly as in Part 1.4.
- [ ] 🟡 SHOULD: A 10-year-old could read it and say what changed.
- [ ] 🟡 SHOULD: Sentences are 20 words or fewer; paragraphs are 3 lines or fewer.
- [ ] 🟡 SHOULD: Images have alt text.
- [ ] 🟢 COULD: Read it out loud once.

## 7.2 Product test checklist (before any M or L release)

- [ ] 🔴 MUST: The main task works start to finish on a clean account.
- [ ] 🔴 MUST: New feature tested on [ANSWER: devices/browsers, e.g. Chrome, Safari, iPhone, Android].
- [ ] 🔴 MUST: Old data still works (nothing lost or broken).
- [ ] 🔴 MUST: Sign-up, login, and payment (if any) were tested.
- [ ] 🔴 MUST: Security and privacy impact checked.
- [ ] 🟡 SHOULD: Error messages are friendly and tell people what to do.
- [ ] 🟡 SHOULD: Speed is acceptable: [ANSWER: e.g. pages load in under 3 seconds].
- [ ] 🟡 SHOULD: Accessibility basics checked (keyboard use, contrast, alt text).
- [ ] 🟢 COULD: A real customer tried it first.

## 7.3 Pre-publish checklist (final gate)

- [ ] 🔴 MUST: Changelog entry is complete, with the correct version and date.
- [ ] 🔴 MUST: STATUS is `APPROVED` and the approver is named.
- [ ] 🔴 MUST: Size (XS/S/M/L) was chosen and the right channels are prepared.
- [ ] 🔴 MUST: Legal and trust rules in Part 1.8 are followed.
- [ ] 🔴 MUST: Test email or preview was sent and looked correct on phone and computer.
- [ ] 🔴 MUST: Someone is available to answer replies after publishing.
- [ ] 🔴 MUST: A rollback or correction plan exists for M and L releases.
- [ ] 🟡 SHOULD: Docs and help links are live.
- [ ] 🟡 SHOULD: Analytics tags or tracking links are added (rules in Part 9.5).

## 7.4 QA and test evidence (fill for every M and L release; XS and S need only the first two rows)

**Why:** "It works" is not proof. Proof is a link, a screenshot, or a note someone else can open. An AI agent may run tests and fill the table, but a human signs the Go/No-go at the bottom.

**Bug severity (use these words only):**

| Level | Meaning | Example | Can we release with it open? |
|---|---|---|---|
| **S1 Critical** | Data loss, security hole, payments broken, nobody can use the product | Customers cannot log in | **No** |
| **S2 Major** | Main task is broken or very painful for many people | "Send invoice" fails for Safari users | **No** |
| **S3 Minor** | Annoying but there is an easy workaround | Button color is wrong | Yes, list it under Known Issues |
| **S4 Tiny** | Typos, cosmetic | Misaligned icon | Yes |

**Evidence table (copy per release):**

| Test area | What to check (example) | Result | Evidence (link / screenshot) | Tester | Date |
|---|---|---|---|---|---|
| Main flow on a clean account | "Sign up, create, send, see paid" | [PASS / FAIL / N/A - reason] | [ANSWER] | [ANSWER] | [ANSWER] |
| The new or changed thing | "Logo upload works with PNG and JPG" | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| Old features still work (regression) | "Old invoices still open" | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| Devices and browsers (Q7.2 list) | "Chrome, Safari, iPhone, Android" | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| Sign-up, login, password reset | "Reset email arrives in under 1 minute" | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| Payments and billing (if any) | "Test card works; refund works" | [ANSWER or N/A - reason] | [ANSWER] | [ANSWER] | [ANSWER] |
| Emails and in-app notices look right | "Rendered on phone and desktop; links click" | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| Speed | "Pages load in under 3 seconds" | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| Security and privacy check | "No private data visible to others" | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| Accessibility basics | "Keyboard only; text is readable" | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| Rollback rehearsal (size L only) | "We practiced going back to 1.3.2" | [ANSWER or N/A - reason] | [ANSWER] | [ANSWER] | [ANSWER] |

**Release readiness (Go / No-go):**

```
OPEN S1 BUGS: [ANSWER: number + links, must be 0]
OPEN S2 BUGS: [ANSWER: number + links, must be 0]
OPEN S3 / S4 BUGS LISTED UNDER KNOWN ISSUES?: [Yes / No / None]
ALL FAILED ROWS ABOVE FIXED OR EXPLAINED?: [Yes / No]
WHO RAN THE TESTS (HUMAN / AI AGENT NAME): [ANSWER]
DECISION: [GO / NO-GO]
DECIDED BY (HUMAN) AND DATE: [ANSWER]
```

If the decision is **NO-GO**, do not send announcements. Fix, retest, and update the date.

## 7.5 Compliance and privacy checklist (run for every M and L release and before the first launch)

> **Not legal advice.** Rules differ by country and by product. This list helps you remember the usual checks. For anything marked "ask a professional", ask a lawyer or privacy expert in the regions you serve (your answer to Q1.16).

| Check | Why it matters | Applies? (Yes / No / UNKNOWN) | Done | Evidence (link or note) |
|---|---|---|---|---|
| **Email: unsubscribe link and business address** in every marketing email | Required by many laws (for example CAN-SPAM in the US) | [ANSWER] | - [ ] | [ANSWER] |
| **Email: honest sender name and subject line** (no tricks, no fake "Re:") | Trust and legal rules | [ANSWER] | - [ ] | [ANSWER] |
| **Email: permission (consent) recorded** where the law needs it (EU/UK, Canada) | Prove people said yes: when, where, how | [ANSWER] | - [ ] | [ANSWER] |
| **Unsubscribes honored quickly** (for example within 10 days or sooner) | Law and trust | [ANSWER] | - [ ] | [ANSWER] |
| **Product emails vs marketing emails kept separate** (receipts, security notices are not marketing) | Avoid sending marketing to people who opted out | [ANSWER] | - [ ] | [ANSWER] |
| **Privacy policy still true** after this release (new data collected? new tools? new sharing?) | You must not collect or use data in ways the policy does not say | [ANSWER] | - [ ] | [ANSWER] |
| **Cookie / tracking consent** works for the regions that need it | Needed for analytics and ad tags in some regions | [ANSWER] | - [ ] | [ANSWER] |
| **Customers can export or delete their data** | Privacy rights (for example GDPR/CCPA) | [ANSWER] | - [ ] | [ANSWER] |
| **No personal data in changelog, posts, screenshots, or AI prompts** | Customer names, emails, invoices must be hidden or fake | [ANSWER] | - [ ] | [ANSWER] |
| **Children** (if under-age users are possible, extra rules apply, for example COPPA) | Ask a professional | [ANSWER] | - [ ] | [ANSWER] |
| **Testimonials and names: written permission saved** | Part 1.8 | [ANSWER] | - [ ] | [ANSWER] |
| **Reviews and endorsements: free gifts or rewards are disclosed** | Disclosure rules for endorsements | [ANSWER] | - [ ] | [ANSWER] |
| **Claims can be proven** ("3x faster", "saves 5 hours") with a real measurement | Advertising rules and trust | [ANSWER] | - [ ] | [ANSWER] |
| **Prices, renewals, trials, and refunds stated clearly** (auto-renew, when the charge happens, how to cancel) | Consumer protection rules | [ANSWER] | - [ ] | [ANSWER] |
| **Referral rewards and discounts: terms stated in the message** | Fairness and honesty (Part 12) | [ANSWER] | - [ ] | [ANSWER] |
| **App store rules checked** (release notes, pricing talk, review prompts, data labels) | Stores can reject updates | [ANSWER or N/A - no app] | - [ ] | [ANSWER] |
| **Security notices: data affected, who, what to do, and legal breach-notice timing considered** | Some laws require fast notice. Ask a professional | [ANSWER] | - [ ] | [ANSWER] |
| **Third-party names, logos, and quotes used with permission** | Copyright and trademark | [ANSWER] | - [ ] | [ANSWER] |
| **Accessibility of messages** (alt text, readable contrast, captions on videos) | Fairness and some legal rules | [ANSWER] | - [ ] | [ANSWER] |

```
COMPLIANCE CHECK DONE BY (HUMAN): [ANSWER]
DATE: [ANSWER]
ITEMS MARKED UNKNOWN (copy to Part 9.3): [ANSWER or None]
NEEDS A PROFESSIONAL OPINION BEFORE PUBLISHING?: [Yes: topic ___ / No]
```

**Rule for AI agents:** you may fill "Applies?" and suggest evidence, but never write "Done" for a legal item. Only a human ticks the Done box.

---

# PART 8. RULES FOR AI AGENTS (how to help without causing harm)

## 8.1 What the agent may do (AI)

- Read this file and the code or task history for the release.
- Draft changelog lines, announcement drafts, email subject options, and social posts.
- Check drafts against Part 1.4 (voice), Part 7.1 (quality) and Part 4.1 (rules).
- Summarize customer feedback.
- Suggest a size (XS/S/M/L) and explain why.

## 8.2 What the agent must NEVER do

- Publish, send, schedule, post, or reply publicly.
- Invent customer quotes, reviews, numbers, dates, names, or promises.
- Change Part 0, Part 1, or Part 6 answers without the human saying yes.
- Include secrets, internal URLs, API keys, private customer data, or security details that help attackers.
- Write about a feature it has not seen proof of (a merged change, a passing test, a live link).

## 8.3 Agent input and output contract

**Inputs the agent needs:** a list of merged changes since the last release, the release version, the test results, and Parts 0 to 2 of this file.

**Output format (always):**

```
STATUS: READY FOR HUMAN REVIEW
SUGGESTED VERSION AND WHY: ...
SUGGESTED SIZE AND WHY: ...
CHANGELOG ENTRY: (Part 4.2 block, filled)
ANNOUNCEMENT DRAFTS: (Part 5.4 blocks, only for ON channels)
THINGS I COULD NOT CONFIRM: (list, or "None")
QUESTIONS FOR THE HUMAN: (list, or "None")
```

## 8.4 Agent self-check before handing over

- [ ] Every claim has a source (task, merge, test, or the human's note).
- [ ] Every number is either from the source of truth in Q0 or marked `UNKNOWN`.
- [ ] Voice rules and word list were applied.
- [ ] No text promises something not yet shipped.
- [ ] Breaking changes and security items are clearly flagged for the human.

---

# PART 9. MEASURE, LEARN, REPEAT

## 9.1 What to measure (pick up to 5, decide once)

| Metric (simple name) | What it tells you | Where to find it | Target (example → yours) |
|---|---|---|---|
| Customers reached (by your Q2.1 definition) | Progress to 500 | [ANSWER] | 500 |
| Email open and click rate | Do people care? | [ANSWER] | "40% open, 5% click" → [ANSWER] |
| Changelog page visits | Do people read updates? | [ANSWER] | "30% of active users per month" → [ANSWER] |
| New sign-ups after an announcement | Did it bring people in? | [ANSWER] | "10 in 3 days" → [ANSWER] |
| Support questions after a release | Was the message clear? | [ANSWER] | Fewer is better |
| Unsubscribes or "mute" rate | Are you annoying people? | [ANSWER] | "Under 1% per email" → [ANSWER] |
| Feature use after announcement | Did they try it? | [ANSWER] | "20% try it in 7 days" → [ANSWER] |

## 9.2 After every M or L release (fill within 7 days)

```
RELEASE: [ANSWER, e.g. 1.5.0 Logo upload]
WHAT WE EXPECTED: [ANSWER, e.g. "20% of users upload a logo in 7 days"]
WHAT REALLY HAPPENED (numbers): [ANSWER or UNKNOWN]
WHAT CUSTOMERS SAID (summary, no names without permission): [ANSWER]
WHAT WORKED: [ANSWER]
WHAT DID NOT: [ANSWER]
ONE THING WE WILL DO DIFFERENTLY NEXT TIME: [ANSWER]
```

## 9.3 Open questions (anything marked UNKNOWN goes here)

| # | Question | Who will find the answer | Due date | Answer |
|---|---|---|---|---|
| 1 | [ANSWER, e.g. "What is the best time to send email?"] | [ANSWER] | [ANSWER] | [ANSWER] |

## 9.4 Feedback intake

| Question | Example | Your answer |
|---|---|---|
| Q9.1 Where do customers send feedback? (**Basic**) | "hello@ email and an in-app form" | [ANSWER] |
| Q9.2 How often do you read it? (**Basic**) | "Every Friday" | [ANSWER] |
| Q9.3 How do you tell customers "we heard you"? (**Basic**) | "A 'You asked, we built it' line in the changelog" | [ANSWER] |

## 9.5 Analytics and attribution (where did each of the 500 come from?)

**Why:** If you do not know where customers come from, you cannot repeat what works. This part is simple on purpose: one naming rule, one tracker, one question at sign-up.

### Step 1. Decide your tracking questions (once)

| Question | Example | Your answer |
|---|---|---|
| Q9.4 Which analytics tool counts visits and sign-ups? (**Basic**) | "Plausible" | [ANSWER] |
| Q9.5 Where do you record each customer's source? (**Basic**) | "A 'source' column in the customers table, plus the Part 9.5 tracker" | [ANSWER] |
| Q9.6 Do you ask "How did you hear about us?" at sign-up? (**Basic**) | "Yes, a dropdown with 8 choices plus 'Other'" | [CHOOSE ONE: Yes, the choices are: ___ / No / LATER] |
| Q9.7 Who checks the numbers, and when? (**Basic**) | "Priya, every Friday" | [ANSWER] |
| Q9.8 Do you track people across other websites? (**Basic**) | "No. Only our own links and sign-up answers." | [ANSWER] (keep this minimal and match your privacy policy and Part 7.5) |

### Step 2. The link-naming rule (UTM tags)

Every link you put in a message gets four tags at the end. Use **lowercase, no spaces, hyphens only**. Never put a customer's name or email in a link.

| Tag | Means | Allowed values (pick your own list once and stick to it) | Example |
|---|---|---|---|
| `utm_source` | Where the person saw the link | `newsletter`, `linkedin`, `x`, `producthunt`, `blog`, `in-app`, `reddit`, `discord`, `partner-name` | `linkedin` |
| `utm_medium` | The kind of channel | `email`, `social`, `community`, `referral`, `launch-site`, `app`, `organic` | `social` |
| `utm_campaign` | Which release or push | `launch-2027-01`, `logo-upload-1-1-0`, `referral-2027-04` | `logo-upload-1-1-0` |
| `utm_content` | Which version of the message | `post-a`, `post-b`, `subject-a`, `button-top` | `post-a` |

**Finished link example:** `https://invoicebuddy.example.com/settings/brand?utm_source=linkedin&utm_medium=social&utm_campaign=logo-upload-1-1-0&utm_content=post-a`

**Your allowed list (fill once and keep it short):**

```
ALLOWED SOURCES: [ANSWER]
ALLOWED MEDIUMS: [ANSWER]
CAMPAIGN NAME FORMAT: [ANSWER, e.g. <feature>-<version> or launch-YYYY-MM]
```

**Never:** invent a new spelling ("LinkedIn", "linked-in" and "li" are three different sources to a computer). Use only the allowed list.

### Step 3. The "Source of the 500" tracker (update weekly)

One row per **week**, not per person (keep customers' names out of this file).

| Week starting | New customers (Q2.1 definition) | By source: email | linkedin | blog | producthunt | referral | direct / unknown | Best message this week | Notes |
|---|---|---|---|---|---|---|---|---|---|
| [ANSWER, e.g. 2027-01-11] | [ANSWER, e.g. 18] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |
| [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] | [ANSWER] |

**Running totals to the 500 (update each row above):**

```
CUSTOMERS SO FAR: [ANSWER] of 500
TOP 3 SOURCES BY COUNT: [ANSWER]
SHARE OF "DIRECT / UNKNOWN" (if over 40%, improve tagging or add the sign-up question): [ANSWER %]
SOURCE THAT GAVE CUSTOMERS WHO DID THE KEY ACTION (not just sign-ups): [ANSWER]
```

### Step 4. Turn numbers into decisions

| If you see this | Then do this |
|---|---|
| One source brings most customers | Write a better message for that source; plan more content there |
| Many sign-ups but few key actions | Improve the welcome emails (11.6, 11.7) and the first-use steps |
| Many visits to the changelog but few sign-ups | Add a clear "Try it" button at the top of the changelog page |
| High unsubscribes after a release email | Send fewer emails; make the subject more honest (Part 7.1) |
| "Direct / unknown" is large | Check that every link has UTM tags; add the sign-up question (Q9.6) |

**Rules for AI agents:** compute only from numbers the human gives you or from the tracker. Never estimate missing numbers. If a source is missing, write `UNKNOWN`. Never include customer names or emails in this table or in prompts.

---

# PART 10. AI PROMPT LIBRARY (copy, paste, send to your AI agent)

**How to use:** Paste this file (or the parts named) into your AI agent, then paste one prompt. Replace the `{curly brackets}`. Every prompt ends with the same safety line so the agent drafts but never publishes.

**Safety line (already included at the end of each prompt):** *"Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW."*

### P1. Fill Part 0 and Part 1 from my project notes

```
You are a senior technical writer and product architect. Read the attached Changelog_and_Announcements.md and my project notes below. Fill every [ANSWER] in Part 0 and Part 1 using only my notes. Where my notes do not say, write UNKNOWN and add the question to Part 9.3. Keep my wording simple (age 10 reading level). Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.

MY NOTES:
{paste notes}
```

### P2. Turn my merged changes into a changelog entry

```
Act as a technical writer and QA specialist. Using Part 1.2 (categories), Part 4.1 (rules) and the Part 4.2 block, write the changelog entry for version {version} dated {YYYY-MM-DD}. Rewrite every developer-style line into customer words using the "rewrite test" table in Part 4.1. Suggest SIZE (XS/S/M/L) with a one-line reason using Part 1.6. Flag any BREAKING or Security item for the human. Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.

MERGED CHANGES (task titles, pull-request titles, commit messages):
{paste list}
```

### P3. Write the Master Announcement Brief

```
Act as a product marketing writer. From the changelog entry below, fill the Master Announcement Brief in Part 5.3. Answer the 5 questions in Part 5.2. Use the voice rules and word list in Part 1.4. List "WHAT WE MUST NOT SAY" for any claim I cannot prove. Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.

CHANGELOG ENTRY:
{paste entry}
```

### P4. Draft all channel messages for a release

```
Using the Master Announcement Brief below, draft the blocks in Part 5.4 for only the channels marked ON in Part 1.5 and allowed for this SIZE in Part 1.6. Same story, different length. Follow the character limits in each block. Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.

BRIEF:
{paste brief}
```

### P5. Check my draft against the rules (quality-assurance pass)

```
Act as a QA specialist and editor. Review the draft below against Part 7.1 (writing checklist) and Part 1.8 (legal and trust). Return a table: Rule | Pass/Fail | Exact fix. Then give a corrected version. Check reading level (age 10), word list, spelling, and that no unshipped feature is promised. Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.

DRAFT:
{paste draft}
```

### P6. Plan my next stage on the path to 500

```
Act as a project manager and growth advisor. I am at Stage {stage} with {number} customers (definition in Q2.1). Read Part 2 and Part 9. List the 5 most useful announcements or messages to send in the next 14 days, with channel, owner, date, and why. Do not suggest paid ads unless Q0.12 allows a budget. Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.
```

### P7. Write the correction notice after a problem

```
Act as a calm, honest customer-communications lead. Using the Part 6 template, write a correction notice for this problem: {describe what happened, who was affected, what is fixed}. One-line apology, no excuses, no blame on customers, vendors or AI. Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.
```

### P8. Summarize customer feedback into the next changelog ideas

```
Act as a research analyst. Read the feedback below and list the top 5 themes, how many people mentioned each (count only what is really in the text), and one customer-friendly changelog line per theme that we could write once it ships. Do not name or quote customers unless the text says they gave permission. Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.

FEEDBACK:
{paste feedback}
```

### P9. Make this document ready (final audit)

```
Act as a QA specialist. Audit the attached document with Part 13 (final completeness check). List every remaining [ANSWER], [CHOOSE], conflicting answers, and missing owners. Do not fix anything unless I say so. Do not publish or send anything. Do not invent facts. Mark anything you cannot confirm as UNKNOWN. Finish with STATUS: READY FOR HUMAN REVIEW.
```

---

# PART 11. EMAIL SCRIPTS (waitlist, beta, launch, onboarding, milestones)

**How to use:** Copy the script for your stage. Replace everything in `{curly brackets}`. Keep it short. Always add the footer (unsubscribe link + business address) from Part 5.4-B. Every script already answers the 5 questions in Part 5.2.

## 11.1 Waitlist: welcome (send right after sign-up)

```
Subject: You're on the list
Preview: Here's what happens next.

Hi {first_name},

Thanks for joining the {Product} waiting list. {Product} helps {who} {do what}.

Here's what happens next:
- We'll email you when early access opens (we expect {month}).
- You'll hear from us about once a {week/month}.
- {The promise from Q2.12, e.g. "You'll get 30% off your first year."}

Tell us one thing: what is the hardest part of {the problem} for you? Just reply to this email. I read every answer.

{Your name}
{Footer}
```

## 11.2 Waitlist: teasers (T-14, T-7, T-1)

```
Subject (T-14): The problem we're fixing
Hi {first_name}, {one sentence about the customer's problem}. We've been building {Product} to fix it. In 2 weeks you'll get early access. Reply and tell me if I got your problem right. {Your name}

Subject (T-7): A first look
Hi {first_name}, here's a quick look at {Product}: {screenshot or short video link}. Early access opens on {date}. {Your name}

Subject (T-1): Tomorrow
Hi {first_name}, early access opens tomorrow at {time + time zone}. Here's your link: {link}. {Offer reminder}. {Your name}
```

## 11.3 Beta testers: invitation

```
Subject: Want to test {Product} first?

Hi {first_name},

Would you try an early version of {Product} and tell me what's confusing or broken? It takes about {15} minutes.

What to do:
1. Go to {link} and {first task}.
2. Try to {main task}.
3. Tell me what felt hard: {form link or reply to this email}.

Please send feedback by {date}. Thank you! As a thank-you, you'll get {reward}.

{Your name}
```

## 11.4 Beta testers: weekly update

```
Subject: Beta update {number}: what changed

Hi {first_name},

What changed this week:
- {Added/Changed/Fixed line in customer words}
- {line}

Please test: {one specific thing}.
Known problems: {honest list or "none known"}.
Send feedback by {date}: {link}.

Thanks, {Your name}
```

## 11.5 Launch day (to the waiting list)

```
Subject: {Product} is open: here's your link
Preview: Early access starts now.

Hi {first_name},

{Product} is live. It helps {who} {do what}, so you can {benefit}.

{Primary button: Start now → link}

What you can do today:
- {Feature 1 in customer words}
- {Feature 2}
- {Feature 3}

{Offer and its end date, if any}

Stuck? Reply to this email or visit {help link}. I'll answer personally.

Thank you for waiting. {Your name}
```

## 11.6 Welcome and first-success email (new customer, day 0)

```
Subject: Welcome to {Product}: your first win in 5 minutes

Hi {first_name},

Welcome! The fastest way to see {Product} work is to {first key action}:
1. {step 1}
2. {step 2}
3. {step 3}

{Button: Do it now → link}

If anything is confusing, just reply. {Your name}
```

## 11.7 Day-3 nudge (customer has not done the key action)

```
Subject: Need a hand with {first key action}?

Hi {first_name},

I noticed you haven't {key action} yet. Most people get stuck on {common blocker}. Here's a 1-minute guide: {link}.

Reply "help" and I'll do it with you. {Your name}
```

## 11.8 "You asked, we built it" (when a request ships)

```
Subject: You asked for {feature}. It's here.

Hi {first_name},

You told us {their request in your words, with permission}. Today we shipped it: {one sentence}.

{Button: Try it → link}

Thank you for helping us build {Product}. {Your name}
```

## 11.9 Review and testimonial request (after a success moment)

```
Subject: Would you share one sentence about {Product}?

Hi {first_name},

You {did a success action} on {date}, which is great to see. Would you write one or two sentences about your experience? {link}

I'll only use your words and name if you tick the box that says it's OK. {Your name}
```

## 11.10 Quiet-customer win-back

```
Subject: One quick tip for {Product}

Hi {first_name},

Since you last visited, we added: {1 or 2 changes in customer words}. Here's a 1-minute tip to {benefit}: {link}.

If {Product} isn't right for you, tell me why by replying. It helps a lot. {Your name}
```

## 11.11 Milestone emails (50, 100, 250, 500)

```
Subject: {Number} customers. Thank you.

Hi {first_name},

This week {number} people have used {Product}. {One real thing you learned or changed because of them.}

What's next: {1-2 promises you can keep}.

Want to help? {Ask: reply with feedback / share / refer a friend: link}

Thank you. {Your name}
```

---

# PART 12. OFFERS, PRICING, AND REFERRAL KIT

**Why this part exists:** Money messages are the riskiest messages. Anything about price, discounts, refunds, or referrals is size **L** (Q1.11).

## 12.1 Decide your offers once

| Question | Example | Your answer |
|---|---|---|
| Q12.1 What are your plans and prices? (**Basic**) | "Free: 3 invoices a month. Pro: $12 a month." | [ANSWER] |
| Q12.2 Launch offer (if any) (**Basic**) | "30% off Pro for the first year, for the first 100 customers" | [ANSWER or N/A] |
| Q12.3 When does the offer end? (**Basic**) | `2027-02-12` or "when 100 people claimed it" | [ANSWER: date or count] |
| Q12.4 How can we count real remaining spots? (**Basic**) | "Admin page counter; never show a fake counter" | [ANSWER] |
| Q12.5 Refund rule (**Basic**) | "Full refund within 14 days, no questions" | [ANSWER] |
| Q12.6 Early-customer thank-you (**Advanced**) | "First 10 customers keep the price for life" | [ANSWER or N/A] |

**Honesty rules:**
- [ ] 🔴 MUST: Never show fake countdown timers, fake "only 3 left", or fake discounts (a "was" price must have been a real price).
- [ ] 🔴 MUST: Say the end date or the limit **in the message itself**.
- [ ] 🔴 MUST: Say what happens when the offer ends and what happens to existing customers.
- [ ] 🟡 SHOULD: Have someone else check the maths (for example, is 30% off $12 equal to $8.40?).

## 12.2 Offer announcement block

```
OFFER NAME: [ANSWER, e.g. "Founding Customer Offer"]
WHAT YOU GET: [ANSWER, e.g. "30% off Pro for 12 months"]
WHO CAN GET IT: [ANSWER, e.g. "The first 100 customers"]
HOW TO CLAIM: [ANSWER, e.g. "Use code FOUNDER30 at checkout"]
ENDS: [ANSWER: date and time + time zone, or count]
WHAT HAPPENS AFTER IT ENDS: [ANSWER, e.g. "Price goes to $12 a month; your first year stays at $8.40"]
REFUND RULE: [ANSWER]
MESSAGE (3 sentences max, plain words): [ANSWER]
```

## 12.3 Price or plan change block (size L)

```
OLD PRICE AND PLAN: [ANSWER]
NEW PRICE AND PLAN: [ANSWER]
START DATE (at least {30} days away): [ANSWER]
WHAT HAPPENS TO CURRENT CUSTOMERS: [ANSWER, e.g. "Locked at the old price until 2027-12-31"]
WHY (honest, one sentence, no blame): [ANSWER]
HOW TO CANCEL OR CHANGE PLAN: [ANSWER]
WHO WE EMAIL AND WHEN: [ANSWER, e.g. "All paying customers: 30 days before, 7 days before, on the day"]
```

## 12.4 Referral program (start at Stage 7 or later)

| Question | Example | Your answer |
|---|---|---|
| Q12.7 Do you run a referral program? (**Basic**) | "Yes, from Stage 7" | [CHOOSE ONE: Yes / No / LATER] |
| Q12.8 What does the person who refers get? (**Basic**) | "1 free month of Pro per friend who sends an invoice" | [ANSWER] |
| Q12.9 What does the friend get? (**Basic**) | "30 days of Pro free" | [ANSWER] |
| Q12.10 What stops abuse? (**Advanced**) | "Max 12 free months per person; the friend must be a new email" | [ANSWER] |
| Q12.11 Where does the referral link live? (**Basic**) | "Settings > Invite friends" | [ANSWER] |

**Referral invitation (to existing customers):**

```
Subject: Give a friend 30 days free

Hi {first_name},

Know someone who {fits Q0.3}? Send them your link: {link}.
They get {friend reward}. You get {your reward} when they {action}.

{Rules in one sentence, e.g. "Up to 12 free months per person."}

Thanks for spreading the word. {Your name}
```

## 12.5 Launch-offer timeline (fill the dates)

| When | What | Channel | Owner |
|---|---|---|---|
| T-0 | Offer announced | Email, in-app, social | [ANSWER] |
| T+{7} | Reminder: {X} spots or days left (**real number only**) | Email | [ANSWER] |
| T+{last-2 days} | Final reminder | Email, in-app | [ANSWER] |
| T+{end} | Offer closed; thank-you message | Email, social | [ANSWER] |

---

# PART 13. FINAL COMPLETENESS CHECK (is this document ready?)

Tick every line. If any 🔴 box is unchecked, the document is **not** ready.

- [ ] 🔴 Part 0 has no blank answers.
- [ ] 🔴 Part 1 decisions are made (versioning, categories, voice, channels, sizes, approvals).
- [ ] 🔴 Part 2 current stage is selected and its questions answered.
- [ ] 🔴 At least one Release Entry Block (or the `[Unreleased]` section) exists in Part 4.
- [ ] 🔴 Every ON channel in Part 1.5 has an owner.
- [ ] 🔴 Approver is named in Part 1.6.1.
- [ ] 🔴 If you have any offer or price message, Part 12 honesty rules are checked.
- [ ] 🔴 Part 7.4 QA evidence table and Go/No-go are filled for every M and L release.
- [ ] 🔴 Part 7.5 compliance and privacy checklist is done by a human for every M and L release.
- [ ] 🟡 Part 9.5 allowed UTM list is filled and the weekly tracker is running.
- [ ] 🔴 No `[ANSWER: ...]` or `[CHOOSE ...]` text remains in the parts you use (only `UNKNOWN` or `N/A - reason`).
- [ ] 🟡 Every `UNKNOWN` is listed in Part 9.3.
- [ ] 🟡 Someone else (or an AI agent) read the file and could use it without asking you anything.

**Sign-off:** Name: [ANSWER] · Date: [ANSWER: YYYY-MM-DD]

---

# APPENDIX A. SIMPLE WORD HELP (glossary)

| Word | Means |
|---|---|
| Changelog | A dated list of what changed in your product |
| Release | A new version of your product that customers can use |
| Version | The number of a release, like 1.4.0 |
| Breaking change | A change that can stop old things from working |
| Deprecated | "Still works, but will be removed soon" |
| Rollback | Going back to the previous version after a problem |
| Channel | A place where you talk to customers (email, social, in-app...) |
| Segment | A group of customers, like "paying customers" |
| Stage | Where you are on the path to 500 customers |
| Source of truth | The one place the real number or fact lives |
| AI agent | A computer helper that drafts work for you; a human still approves |
| Waitlist | People who asked to hear when you launch |
| Beta | An early version given to a few testers |
| Referral | A customer inviting a friend |
| UNKNOWN | "I don't know yet. Please find out." |

# APPENDIX B. ONE-PAGE CHEAT SHEET

1. Write every change as one customer-friendly line under `[Unreleased]`.
2. Pick a size: XS, S, M, L.
3. Pick a version: patch (fix), minor (new), major (breaks).
4. Fill the Release Entry Block. Get approval.
5. Publish the changelog first, then in-app, email, social, blog.
6. Answer questions. Measure. Write down what you learned.
7. Count customers. Celebrate 10, 50, 100, 250, and **500**.

# APPENDIX C. REVISION HISTORY OF THIS DOCUMENT

| Template version | Date | What changed | By |
|---|---|---|---|
| 1.0 | 2026-10-18 | First draft of the master template | [ANSWER] |
| 1.1 | 2026-10-18 | Examples under every question, Basic/Advanced tags, AI prompt library, email scripts, offers kit, filled sample project | [ANSWER] |
| 1.2 | 2026-10-18 | Added QA and test evidence (7.4), compliance and privacy checklist (7.5), analytics and attribution (9.5) | [ANSWER] |

---

# APPENDIX D. A FULLY FILLED SAMPLE PROJECT ("InvoiceBuddy", build to 500 customers)

> This is **fictional**. Names, numbers, dates, and links are made up so you can see what "done" looks like. Do not copy them into a real project.

## D.1 Part 0 and Part 1, filled (short form)

| Item | Filled answer |
|---|---|
| Product | InvoiceBuddy. Web app that helps freelancers send invoices and get paid faster. |
| For whom | Freelance designers who send 5+ invoices a month |
| Owner | Priya Shah (priya@example.com) |
| First launch target | 2027-01-12 |
| Customer definition (Q2.1) | A person who sent their first real invoice |
| Versioning | Semantic Versioning, public launch `1.0.0`, beta line `0.9.0-beta.N` |
| Channels ON | Public changelog, in-app, email, LinkedIn, blog (size L only), Product Hunt (launch day only) |
| Channels LATER | Discord, X, status page |
| Voice | Friendly, clear, honest. Never: hype words, blaming customers, jargon. Reading level: age 10 |
| Approver | Priya (all sizes); size L also read by a friend (Dana) |
| Timing | Email Tue-Thu 10:00 local time. Max 4 marketing emails a month. Dates in UTC. |
| Plans | Free (3 invoices a month), Pro ($12 a month) |
| Launch offer | 30% off Pro for 12 months, first 100 customers, claim code FOUNDER30 |

## D.2 Stage by stage: what happened and what was announced

| Stage | Dates | What the team did | What was announced (and where) | Exit test result |
|---|---|---|---|---|
| 1. Idea and Build | 2026-08-01 to 2026-10-15 | Built create, send, and "who paid" features. AI agent drafted tests and help articles. | Weekly "build in public" LinkedIn post. Every finished task added one line under `[Unreleased]`. | A tester finished invoice start to end on 2026-10-14 ✔ |
| 2. Test | 2026-10-16 to 2026-11-30 | 5 beta users + AI test agent. Google Form for bugs. | Weekly beta email (script 11.4). Releases `0.9.0-beta.1` to `0.9.0-beta.6`. | Part 7.2 checklist passed on 2026-11-28 ✔ |
| 3. Pre-launch | 2026-12-01 to 2027-01-11 | Waitlist page live. Product Hunt page prepared. | Welcome email (11.1). Teasers at T-14, T-7, T-1 (11.2). | 126 people on the waitlist (goal 100) ✔ |
| 4. Launch day | 2027-01-12 | Release `1.0.0`. Priya answered questions for 6 hours. | Changelog, in-app, email to waitlist (11.5), LinkedIn, Product Hunt, blog "Why I built InvoiceBuddy". | First invoice sent at 09:41 ✔ |
| 5. Customers 0-10 | 2027-01-12 to 2027-01-31 | Personal email to each new customer; offered 15-minute calls. | Warm changelog; first "You asked, we built it" email (11.8) for "duplicate invoice". | 10th customer on 2027-01-29 ✔ |
| 6. Customers 11-50 | 2027-02-01 to 2027-03-20 | Found that LinkedIn and a freelancer Slack group brought most customers. Most-requested feature: logo upload. | Release `1.1.0` (logo upload, size M): in-app, email, LinkedIn post, docs. Changelog every 2 weeks. | Same LinkedIn message brought 3 customers three times ✔ |
| 7. Customers 51-200 | 2027-03-21 to 2027-06-30 | Thursday routine: changelog + in-app note. Segments: new, active, quiet. Review requests at day 14. Referral program launched. | Release `1.3.0` (referrals, size L): blog, email, in-app, LinkedIn. Quiet-customer win-back email (11.10). | Routine ran 6 weeks without panic ✔ |
| 8. Customers 201-500 | 2027-07-01 to 2027-09-20 | Best result: win-back email to quiet customers, 18% returned. | 250-customer thank-you email (11.11). Release `1.6.0` (multi-currency, size L). | 500th customer on 2027-09-20 ✔ |
| 500 reached | 2027-09-20 | Retrospective written (Part 9.2). | "500 customers: what we learned" blog post and email. Case study with Sam's written permission. | Done ✔ |

## D.3 A filled Release Entry Block (size M)

```
## 1.1.0 - 2027-02-18

SIZE: M
RELEASE TYPE: MINOR
STATUS: PUBLISHED
ONE-LINE SUMMARY: You can now add your logo to every invoice.

### Added
- You can now upload your logo once and it shows on every invoice.
- You can pick a color for your invoice header.

### Fixed
- Fixed a bug that showed the wrong total on invoices with discounts.

BREAKING CHANGE?: No
KNOWN ISSUES: Logos bigger than 2 MB are rejected. We will raise the limit soon.
LEARN MORE LINK: https://invoicebuddy.example.com/help/logo
THANKS TO: Sam (with permission) for asking for this.
INTERNAL REFERENCE: IB-212, IB-219, IB-224
TESTED BY / PROOF: Checklist 7.2 passed 2027-02-16, notes in Linear IB-230
APPROVED BY: Priya Shah, 2027-02-17
```

## D.4 A filled Master Announcement Brief for that release

```
RELEASE VERSION: 1.1.0
SIZE: M
ONE-SENTENCE NEWS: You can now add your logo to every invoice.
WHO IS IT FOR: Freelancers who want invoices that look professional.
WHY THEY SHOULD CARE:
- Your invoices look like your business.
- Upload once, no more editing every invoice.
- It takes about 30 seconds.
PROOF: Screenshot of an invoice with a logo (assets/logo-demo.png)
THE ONE ACTION WE WANT THEM TO TAKE: Upload your logo.
LINK FOR THAT ACTION: https://invoicebuddy.example.com/settings/brand
HELP LINK: https://invoicebuddy.example.com/help/logo
WHAT WE MUST NOT SAY: "Clients pay faster with a logo" (we have no proof).
ASSETS READY: assets/logo-demo.png, assets/logo-demo.gif
PUBLISH DATE AND TIME: 2027-02-18 10:00 UTC
```

## D.5 Filled channel messages for that release

**In-app notice**

```
TITLE: Add your logo
BODY: Upload your logo once and it shows on every invoice.
BUTTON TEXT: Upload logo
BUTTON LINK: https://invoicebuddy.example.com/settings/brand
SHOW TO: All users
SHOW WHEN: Next login, once only
```

**Email**

```
SEGMENT: All active users
SUBJECT LINE: Your logo, on every invoice
PREVIEW TEXT: Upload it once. It takes 30 seconds.
BODY:
Hi {first_name},
You can now add your logo to every invoice. Upload it once in Settings and you're done.
- Pick your logo and header color.
- Every new invoice uses them.
- Change them any time.
[Upload my logo]
Questions? Reply to this email. Priya
```

**LinkedIn post**

```
You asked for it, so I built it: you can now add your logo to every InvoiceBuddy invoice. Upload it once, and it appears on all of them. Takes about 30 seconds. {link}
```

## D.6 A filled 9.2 retrospective

```
RELEASE: 1.1.0 Logo upload
WHAT WE EXPECTED: 20% of users upload a logo in 7 days
WHAT REALLY HAPPENED: 34% uploaded a logo in 7 days (17 of 50 users)
WHAT CUSTOMERS SAID: Many said invoices feel more professional; 3 asked for custom fonts
WHAT WORKED: Putting the screenshot in the in-app notice
WHAT DID NOT: The email subject line had a low open rate (31%)
ONE THING WE WILL DO DIFFERENTLY NEXT TIME: Test two subject lines before sending
```
