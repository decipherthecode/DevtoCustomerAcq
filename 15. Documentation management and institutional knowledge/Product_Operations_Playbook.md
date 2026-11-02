# How to Fill This Document

> **Read this whole box first. It takes 3 minutes and saves hours.**

## What is this file?

This is your **Product Operations Playbook**. It is a single file that walks you, one question at a time, from **"I have an idea"** all the way to **"500 people actively use my product."**

Think of it like a recipe card for building and launching a product with the help of Claude (an AI helper). If you fill in every blank, you will always know what to do next, and nobody has to guess.

**One copy of this file = one product.** Make a fresh copy for every new project.

## The 7 simple rules

1. **Go in order.** Do Part 1, then Part 2, then Part 3, and so on. Do not skip ahead.
2. **Every question has 4 pieces.** The question, *why it matters*, an *example answer*, and a **[FILL IN]** blank. Replace the words `[FILL IN]` with your real answer.
3. **Mark the status.** Under each question you will see three boxes. Change `[ ]` to `[x]` on one of them.
   - `[ ] Not started` means you have not looked at it yet.
   - `[ ] In progress` means you have started but are not finished.
   - `[ ] Done` means the answer is complete and you would be happy to show it to someone.
4. **Never guess silently.** If you do not know an answer, write `UNKNOWN`, then write **who** can find out and **by when**. Example: `UNKNOWN. I will ask 5 customers by Friday.` An honest "unknown" is better than a made-up answer. Also copy it into the **Unanswered Questions Register** (Appendix G) so nothing is forgotten. Want to see what finished answers look like? Read the **Worked Example** (Appendix D).
5. **Short answers are fine.** One or two plain sentences are enough. Do not write essays.
6. **Stop at every Gate.** At the end of each Part there is a **Gate Checklist**. Every box must be ticked before you move on. If a box cannot be ticked, fix it first. This is what keeps you from building the wrong thing.
7. **Update it as you go.** This file is alive. When something changes, change the answer and write a line in the **Change Log** (Appendix E).

## Words you might not know

Hard words are explained the first time they appear, and again in the **Glossary** (Appendix A) at the end. If a word confuses you, look it up there.

## How to use Claude with this file

You do not have to fill this in alone. Try this:

1. Give Claude this file.
2. Say: *"Interview me one question at a time from Part 1 of this playbook. Wait for my answer. Write my answer into the file. Tell me if an answer is too vague."*
3. Repeat for each Part.

Anything Claude writes is **a draft, not the truth.** You are the boss. Wherever you see **🛑 HUMAN CHECK**, a real person (you) must read and approve before moving on.

## How long will this take?

| Part | What it covers | Time to fill in |
|---|---|---|
| Part 0 | Project basics | 15 minutes |
| Part 1 | Idea and validation | 1-3 hours |
| Part 2 | Spec and design | 2-4 hours |
| Part 3 | Build and QA | 2-3 hours to plan, then ongoing |
| Part 4 | Launch and growth to 500 | 2-3 hours to plan, then ongoing |
| Part 5 | Support, metrics, legal, incidents, pricing, budget | 3-4 hours |
| Part 6 | Claude toolkit | 1-2 hours |
| Part 7 | Learning and memory | 30 minutes per review |

## What "finished" looks like

You are finished with this file when:
- No `[FILL IN]` remains (each is either answered or marked `UNKNOWN` with an owner and date).
- All four Gate Checklists are ticked.
- A stranger could open this file and understand what the product is, who it is for, how it was built, and how it is doing.

## What is an "Expert Check" box?

Some sections (legal, security, money, and AI safety) carry a line that says **Expert Check**. It looks like this:

`Expert Check: Checked by [name or "nobody yet"] on [date]`

This template can give you a good checklist, but it cannot replace a qualified person. Write the name of the lawyer, accountant, security-minded friend, or official guide that checked the section, and the date. If nobody has checked it yet, write `nobody yet`. That is honest, and it reminds you to find someone before you rely on the answer.

## Quick Start Path (in a hurry?)

Fill in **only** the questions marked ⭐ first. These are the absolute must-haves. Come back for the rest later. Anything not marked ⭐ is "should have", not "must have".

---

# Product Operations Playbook

| | |
|---|---|
| **Template version** | 1.1 |
| **Template last updated** | 2026-10-19 |
| **Built for** | Solo founders building web or mobile products with AI help (Claude-centered) |
| **Covers** | Idea, then build, then launch, then the first 500 active users |

---

# Part 0: Project Basics

> Fill this in first. It takes 15 minutes. It is the "name tag" for your project.

**Q0.1 ⭐ What is the product called?**
- *Why it matters:* A name lets everyone (including Claude) talk about the same thing.
- *Example:* `PlantPal`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q0.2 ⭐ In one sentence, what does it do, and for whom?**
- *Why it matters:* If you cannot say it in one sentence, it is not clear yet.
- *Example:* `PlantPal reminds busy people when to water each of their houseplants.`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q0.3 ⭐ What kind of product is it?**
Pick one by writing an `x`.
- `[ ]` Web app (opens in a browser)
- `[ ]` Mobile app (iPhone, Android, or both)
- `[ ]` Both web and mobile
- **Other / notes:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q0.4 ⭐ Who is the owner (the one person who makes final decisions)?**
- *Example:* `Sam Lee, sam@example.com`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q0.5 What is the start date and your target launch date?**
- *Example:* `Start: 2026-11-01. Target launch: 2027-02-01.`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q0.6 How many hours per week can you work on this?**
- *Why it matters:* It keeps your plan honest. A plan for 40 hours a week is useless if you only have 8.
- *Example:* `10 hours per week (evenings and Saturday).`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q0.7 What is your budget (money you can spend) until launch, and per month after launch?**
- *Example:* `$500 until launch. $150 per month after.`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q0.8 ⭐ How will you define a "customer" for the goal of 500?**
For this playbook, a customer is an **Active User**: a real person who used the product's main feature in a set period. You must say exactly what that means.
- *Example:* `An Active User is someone who logs at least one plant watering in the last 28 days.`
- **Your definition of "Active User":** **[FILL IN]**
- **Time window (7, 14, or 28 days):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q0.9 Where will the project files live?**
- *Example:* `Code: GitHub repo "plantpal". Docs: Google Drive folder "Documentation management and institutional knowledge / PlantPal".`
- **Code location:** **[FILL IN]**
- **Documents location:** **[FILL IN]**
- **Design files location:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

---

# Part 1: Idea and Validation

> **Goal:** Prove that real people have a real problem, before you build anything.
> **Rule:** Do not write code in this Part.

## 1A. The Problem

**Q1.1 ⭐ What problem are you solving? Say it like a person would, not like a company.**
- *Why it matters:* Products that solve no real problem get no users.
- *Example:* `I forget to water my plants and they die. I do not know which plant needs water when.`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q1.2 ⭐ Who has this problem? Describe one typical person.**
- *Why it matters:* "Everybody" is not an answer. Pick one kind of person to start.
- *Example:* `Anna, 29, lives in a city flat, owns 8 houseplants, works long hours, uses an iPhone.`
- **Who they are:** **[FILL IN]**
- **What they do today to solve the problem:** **[FILL IN]**
- **Why that is not good enough:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q1.3 How big and how painful is the problem?**
- *Example:* `Painful: people spend $30-$100 a year replacing dead plants. Many people: millions of urban plant owners.`
- **How often does it happen?** **[FILL IN]**
- **How much does it cost them (time, money, stress)?** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 1B. Proof That People Care

**Q1.4 ⭐ How many real people have you talked to about this problem?**
Your target: **at least 10 conversations** before you move on.
- *Why it matters:* Your friends saying "nice idea" is not proof. Strangers describing the problem in their own words is proof.
- *Example:* `12 conversations. 9 said they had killed a plant in the last year. 4 said they would pay.`

| # | Who (first name or role) | Date | What they said (one line) | Would they pay or use it? |
|---|---|---|---|---|
| 1 | **[FILL IN]** | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |
| 9 | | | | |
| 10 | | | | |

- **Total conversations:** **[FILL IN]**
- **How many said the problem is real and painful:** **[FILL IN]**
- **What surprised you most:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q1.5 What do people use today instead? (Your competitors)**
Include free tools, spreadsheets, and "doing nothing."

| Alternative | What it does well | What it does badly | Price |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |
| | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q1.6 ⭐ Why would someone pick YOUR product instead? (Your edge)**
- *Example:* `Photo-based plant recognition plus automatic reminder schedule. Competitors need manual setup.`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 1C. The Business Side

**Q1.7 ⭐ How will you make money? (Or if you will not, say so.)**
- `[ ]` Subscription (monthly or yearly)
- `[ ]` One-time purchase
- `[ ]` Free with ads
- `[ ]` Free for now, decide later
- `[ ]` Other: **[FILL IN]**
- **Planned price and why:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q1.8 Rough math: what does it cost to run, and what must you earn?**
- *Example:* `Cost: $120 per month (hosting, AI, tools). Break-even at 20 paying users at $6 per month.`
- **Monthly running cost:** **[FILL IN]**
- **Break-even number of users:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q1.9 ⭐ What are the 3 biggest risks that could make this fail?**
- *Example:* `1. People forget to open the app. 2. Plant recognition is wrong too often. 3. App Store rejects it.`
- **Risk 1:** **[FILL IN]**
- **Risk 2:** **[FILL IN]**
- **Risk 3:** **[FILL IN]**
- **What you will do to reduce each:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q1.10 ⭐ What is the very first small version (MVP) you will build?**
MVP means **Minimum Viable Product**: the smallest version that still solves the main problem. Smaller is better.
- *Example:* `Add plants by photo, get a watering reminder. Nothing else.`
- **MVP in one sentence:** **[FILL IN]**
- **Things you will NOT build yet (the "not now" list):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 1D. Success Targets

**Q1.11 ⭐ What does success look like at each customer milestone?**
Fill the targets that fit your product. Example numbers are shown. Replace them.

| Milestone (Active Users) | Target date | What you want to learn or prove |
|---|---|---|
| 10 | **[FILL IN]** | *Example: The core flow works for real strangers* |
| 50 | | *Example: People come back after a week* |
| 100 | | *Example: One channel reliably brings users* |
| 250 | | *Example: Support load is manageable* |
| 500 | | *Example: Retention holds, ready to plan next stage* |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 🚦 GATE 1: Idea Approved

Every box must be ticked before you start Part 2.

- [ ] I have talked to at least 10 real people (not just friends who want to be nice).
- [ ] I can state the problem and the person in one sentence each (Q1.1, Q1.2).
- [ ] At least some of them said they would use or pay for it (Q1.4).
- [ ] I know what people use today and why mine is better (Q1.5, Q1.6).
- [ ] I know roughly how I will make money, or I have decided to wait (Q1.7).
- [ ] I have listed 3 risks and a plan for each (Q1.9).
- [ ] I have a tiny MVP with a "not now" list (Q1.10).
- [ ] I defined "Active User" (Q0.8).
- [ ] 🛑 **HUMAN CHECK:** The owner has read Part 1 and says "GO".

**Decision:** `[ ] GO` `[ ] CHANGE THE IDEA` `[ ] STOP`
**Decided by / date:** **[FILL IN]**
**Why (one or two sentences):** **[FILL IN]**

---

# Part 2: Spec and Design

> **Goal:** Describe exactly what you will build, so that Claude (and you) are never guessing.
> **Rule:** The clearer this Part, the better the AI-built code will be. Vague specs make vague software.

## 2A. The Product Requirements (PRD)

PRD means **Product Requirements Document**: a plain list of what the product must do.

**Q2.1 ⭐ List the "user stories" for the MVP.**
A user story is one sentence: *"As a [person], I want to [do something], so that [I get a benefit]."*
- *Example:* `As a plant owner, I want to add a plant by taking a photo, so that I do not have to type its name.`

| ID | User story | Priority (Must / Should / Could) |
|---|---|---|
| US-1 | **[FILL IN]** | Must |
| US-2 | | |
| US-3 | | |
| US-4 | | |
| US-5 | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.2 ⭐ For each Must story, how will you know it works? (Acceptance checks)**
Write checks that a person can answer with only **Yes** or **No**.
- *Example for US-1:* `Taking a photo shows a plant name within 5 seconds. The user can correct the name. The plant appears in "My Plants".`

| Story ID | Check 1 | Check 2 | Check 3 |
|---|---|---|---|
| US-1 | **[FILL IN]** | | |
| US-2 | | | |
| US-3 | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.3 What are the non-negotiables for quality?**
Fill in a number for each, or write `Not needed yet`.
- *Example:* `Page loads in under 3 seconds. Works on the last 2 versions of iOS and Android. Works on a slow phone connection.`
- **Speed:** **[FILL IN]**
- **Devices, browsers, phone versions supported:** **[FILL IN]**
- **Accessibility (easy to use for people with disabilities, for example readable text size and screen-reader support):** **[FILL IN]**
- **Languages supported:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.4 What is explicitly OUT of scope for now?**
- *Example:* `No social features. No web version yet. No payments in v1.`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 2B. The Design

**Q2.5 ⭐ Describe the main path a user takes, step by step. (User flow)**
A user flow is the path from "opens the product" to "gets the value."
- *Example:* `1. Open app. 2. Sign up with email. 3. Tap "Add plant". 4. Take photo. 5. Confirm name. 6. See reminder date.`
- **Step 1:** **[FILL IN]**
- **Step 2:**
- **Step 3:**
- **Step 4:**
- **Step 5:**
- **The "aha moment" (the step where the user first feels the value):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.6 List every screen or page you need.**

| Screen / page name | What the user does here | Sketch or link |
|---|---|---|
| **[FILL IN]** | | |
| | | |
| | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.7 What should it look and feel like?**
- *Example:* `Calm, green, friendly. Large rounded buttons. Plain words, no jargon.`
- **Colors (names or codes):** **[FILL IN]**
- **Fonts:** **[FILL IN]**
- **Tone of words (friendly, serious, playful):** **[FILL IN]**
- **Example products you like the look of:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.8 What do empty, loading, and error screens say?**
Every screen needs three extra versions: when there is nothing yet (empty), while waiting (loading), and when something goes wrong (error).
- *Example:* `Empty: "No plants yet. Tap + to add your first one!" Error: "Oops, something broke. Your plants are safe. Try again."`
- **Empty screen words:** **[FILL IN]**
- **Loading screen words:** **[FILL IN]**
- **Error screen words:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 2C. The Technical Plan

**Q2.9 ⭐ Which tools and technologies will you use?**
Do not know? Ask Claude: *"Recommend the simplest, cheapest tools for [my product], for a solo founder. Explain each in plain words."* Then fill in the answer.

*Beginner starting suggestions (you may accept them, or swap any one). These are only popular starting points. Tools, prices, and free limits change, so check the current price and fit before you commit.*

| Job | If you are building a **web app** | If you are building a **mobile app** |
|---|---|---|
| Screens (front end) | Next.js (React) | Expo (React Native), one codebase for iPhone and Android |
| Behind-the-scenes (back end) | Next.js server routes, or Supabase functions | Supabase functions |
| Database and sign-in | Supabase | Supabase |
| Hosting | Vercel | Expo build service, plus the app stores |
| Payments | Stripe | RevenueCat (handles app store subscriptions) or the stores' own billing |
| Emails | Resend | Resend |
| Analytics | PostHog | PostHog |
| Error tracking | Sentry | Sentry |

*Rule of thumb:* choose boring, popular tools. Fewer tools means fewer things to break and a better chance Claude knows them well. App stores often require their own billing for digital goods in the app, so check the current store rules before choosing payments.

| Job | Tool chosen | Why | Monthly cost |
|---|---|---|---|
| Screens the user sees (front end) | **[FILL IN]** | | |
| Behind-the-scenes logic (back end) | | | |
| Where data is stored (database) | | | |
| Sign-in and accounts (authentication) | | | |
| Hosting (where it runs online) | | | |
| Payments (if any) | | | |
| Emails and notifications | | | |
| Analytics (counting what users do) | | | |
| Error tracking (tells you when it breaks) | | | |
| AI features (if any) | | | |

- *Example row:* `Database | Supabase | Easy, free tier, built-in sign-in | $0 to start`
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.10 What data will you collect and store about users?**
- *Why it matters:* More data means more risk and more legal duties. Collect only what you need.
- *Example:* `Email, plant photos, watering dates. No phone numbers. No location.`
- **Data collected:** **[FILL IN]**
- **Why each piece is needed:** **[FILL IN]**
- **Sensitive data (health, money, children, location)? Yes or no, and what:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.11 Which outside services does your product depend on?**
If one of them breaks or changes its price, what happens?

| Service | What you use it for | If it fails, what happens? | Backup plan |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.12 Draw the big picture. (Architecture sketch)**
Write boxes and arrows in plain text, or paste a link to a picture. Show: user, app, server, database, outside services.
- *Example:* `User phone -> App -> Server -> Database. Server -> Plant-ID service.`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q2.13 ⭐ If the product uses AI features, how will you keep them safe and useful?**
Skip if there are no AI features, and write `No AI features`.
- **What the AI does for the user:** **[FILL IN]**
- **What happens when the AI is wrong (it will be sometimes):** **[FILL IN]**
- **What the AI must never say or do:** **[FILL IN]**
- **How you test the AI's answers (a list of 20 test questions and the right answers is a good start):** **[FILL IN]**
- **Monthly AI cost cap:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 2D. Break It Into Small Jobs

**Q2.14 ⭐ Break the MVP into small tasks, each doable in 1 to 2 hours.**
Small tasks are easier for Claude to build correctly and easier for you to check.
- *Example:* `T-1: Create sign-up screen. T-2: Connect sign-up to database. T-3: Add "Add plant" screen.`

| Task ID | Task (one sentence) | Linked story | Who does it (You / Claude) | Done when... |
|---|---|---|---|---|
| T-1 | **[FILL IN]** | US-1 | | |
| T-2 | | | | |
| T-3 | | | | |
| T-4 | | | | |
| T-5 | | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 🚦 GATE 2: Spec Approved

- [ ] Every Must story has Yes/No acceptance checks (Q2.2).
- [ ] The "not now" and out-of-scope lists exist (Q1.10, Q2.4).
- [ ] The main user flow and "aha moment" are written (Q2.5).
- [ ] Every screen has a purpose, and empty, loading, and error words (Q2.6, Q2.8).
- [ ] Tools and monthly costs are chosen and fit the budget (Q2.9, Q0.7).
- [ ] I know what user data I collect and why (Q2.10).
- [ ] AI risks are handled or marked not applicable (Q2.13).
- [ ] The work is split into small tasks (Q2.14).
- [ ] 🛑 **HUMAN CHECK:** The owner read the whole spec and nothing in it is a surprise.

**Decision:** `[ ] GO` `[ ] FIX THE SPEC` `[ ] STOP`
**Decided by / date:** **[FILL IN]**

---

# Part 3: Build and QA

> **Goal:** Build the MVP in small, checked steps and make sure it works before anyone outside sees it.
> **Rule:** Claude writes the first draft. A human reads the evidence before anything is accepted.
> QA means **Quality Assurance**: making sure the product works properly.

## 3A. Setup

**Q3.1 ⭐ Is your project set up for safe building?**
Tick each one when done.
- `[ ]` Code is saved in a version-control tool (like Git/GitHub) so every change is recorded and can be undone.
- `[ ]` There is a **test** copy of the product (for trying things) and a **live** copy (for real users). They are kept separate.
- `[ ]` Secrets (passwords, keys) are stored in a safe place and **never** pasted into code or chat.
- `[ ]` Automatic backups of the database are on.
- `[ ]` The `CLAUDE.md` project brief exists (fill in Part 6, Section 6A).
- **Notes:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.2 What is your "definition of done" for ONE task?**
A task is done only when all of these are true. Edit the list to fit your product.
- `[ ]` The code does what the task said.
- `[ ]` Tests were written and they pass.
- `[ ]` The automatic checks (formatting, errors, security scan) pass.
- `[ ]` A human read the summary and the evidence.
- `[ ]` Notes were updated (`CLAUDE.md` or docs) if anything important changed.
- **Anything to add for your project:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 3B. The Build Loop

For every task from Q2.14, repeat this loop.

1. **Plan.** Ask Claude to explain its plan in plain words *before* writing code. 🛑 Read the plan.
2. **Write a test first.** The test describes what "working" means (a failing test).
3. **Build.** Claude writes just enough code to pass the test.
4. **Check.** Run the automatic checks.
5. **Review.** Read the summary of what changed and what was tested. Look at evidence, not just "it says it works."
6. **Save.** Save the change with a clear label. Update your notes.
7. **Start fresh.** Begin the next task in a **new** Claude session so old clutter does not confuse it.

**Q3.3 Where will you keep the task board? (To-do, Doing, Done)**
- *Example:* `A Notion board with columns To do / Doing / Review / Done.`
- **[FILL IN]:**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.4 How big can one Claude job be before you check it?**
- *Why it matters:* AI can write code faster than you can read it. Small jobs keep you in control.
- *Example:* `At most 1 task and about 200 changed lines per review.`
- **Your limit:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 3C. Quality Checks (QA)

Think of these as **layers of safety nets**. Each layer catches different problems.

**Q3.5 ⭐ Which automatic checks run on every change?**
- `[ ]` Formatting and style check
- `[ ]` Error and type check
- `[ ]` Unit tests (check small pieces of code)
- `[ ]` Security scan for known weaknesses and leaked secrets
- `[ ]` Build check (does the app still build?)
- **Tool names you use:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.6 ⭐ Which checks does a HUMAN always do?**
Some things should never be left to the machine. Tick the ones you will always check yourself.
- `[ ]` Anything about **login, passwords, or user accounts**
- `[ ]` Anything about **payments or money**
- `[ ]` Anything that **deletes or changes saved user data**
- `[ ]` Anything about **privacy** (what is collected, who can see it)
- `[ ]` Database changes
- `[ ]` Anything that changes what the AI is allowed to do
- **Other always-human checks:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.7 ⭐ How will you test the full product, start to finish?**
This is the "walk the whole path like a real user" test.

| Test | Steps | Expected result | Passed? |
|---|---|---|---|
| Sign-up | **[FILL IN]** | | `[ ]` |
| Main flow (Q2.5) | | | `[ ]` |
| Sign-out and sign-in again | | | `[ ]` |
| Forgot password | | | `[ ]` |
| Bad input (empty fields, huge text) | | | `[ ]` |
| No internet or slow internet | | | `[ ]` |
| Delete account | | | `[ ]` |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.8 Which devices and browsers did you test on?**

| Device or browser | Version | Tested by | Result |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.9 Did real people try it before launch?**
Your target: **at least 5 people** from your target group, watched while they use it, without you helping.
- *Why it matters:* You will find problems in 10 minutes that you missed in 10 days.

| Tester | Could they finish the main flow? | Where did they get stuck? | What will you change? |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |
| | | | |
| | | | |
| | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.10 Speed and capacity check.**
- **How fast is the main screen on a normal phone and connection?** **[FILL IN]**
- **What happens if 100 people use it at once? (Ask Claude to help you test, or write "not tested" and why.)** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.11 Security basics. Tick each.**
- `[ ]` Passwords are never stored as plain text (use a trusted sign-in service).
- `[ ]` The product only works over secure connections (HTTPS).
- `[ ]` Each user can only see their own data (tested by trying to open another user's data).
- `[ ]` No secrets are stored in the code.
- `[ ]` Tools and libraries used are up to date (no known serious problems).
- `[ ]` Claude's permissions are limited to what it needs (it cannot touch live data without your OK).
- **Anything else found:** **[FILL IN]**
- **Expert Check:** Checked by **[FILL IN]** on **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.12 Bug list. Where do you keep it, and how do you rank bugs?**

| Level | Meaning | Rule |
|---|---|---|
| **Blocker** | Cannot use the product, or data is lost, or it is unsafe | Must fix before launch |
| **Major** | Main feature is broken for some people | Fix before launch if possible |
| **Minor** | Annoying but there is a workaround | Can wait, write it down |
| **Cosmetic** | Looks off, works fine | Can wait |

- **Where bugs are tracked:** **[FILL IN]**
- **Open Blockers right now:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 3D. AI Quality Tests (only if your product has AI features)

Skip this section if there are no AI features, and write `No AI features` here: **[FILL IN]**

AI answers can be wrong, odd, or different each time. Normal tests are not enough. You need a **test set**: a list of questions with known good answers that you run again after every change.

**Q3.13 ⭐ Build your AI test set.**
Start with **at least 20** realistic questions. Include normal cases, tricky cases, and "bad" cases (rude users, nonsense, attempts to make the AI misbehave).
- *Example:* `Question: "Can I water a cactus every day?" Good answer: says no, explains cactus needs little water. Bad answer: says yes.`

| # | Type (normal / tricky / bad) | Question or input | What a good answer must include | What a bad answer looks like |
|---|---|---|---|---|
| 1 | **[FILL IN]** | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

- **Where the full test set is saved:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.14 ⭐ How do you score the AI's answers?**
- *Example:* `Each answer gets Pass or Fail against the "must include" list. I need 90 percent Pass on normal cases and 100 percent Pass on "bad" cases.`
- **Scoring method (a person, an AI judge that a person spot-checks, or both):** **[FILL IN]**
- **Minimum score to launch:** **[FILL IN]**
- **Latest score and date:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.15 When do you re-run the test set?**
- `[ ]` After changing any AI instruction (prompt)
- `[ ]` After changing the AI model or provider
- `[ ]` Before each release
- `[ ]` Every month (answers can drift when a provider updates a model)
- **Alert plan if the score drops:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q3.16 Safety checks for the AI.**
- `[ ]` The AI cannot reveal other users' data.
- `[ ]` The AI says "I am not sure" when it is not sure (tested).
- `[ ]` The AI refuses harmful requests (tested with at least 5 examples).
- `[ ]` Users can report a bad answer in one tap or click.
- `[ ]` There is a spending cap so a bug cannot create a huge AI bill (see Q2.13).
- `[ ]` I read 20 real AI answers myself each week after launch.
- **Expert Check:** Checked by **[FILL IN]** on **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 3E. Store and Platform Rules (mobile apps)

Skip this section if you are web only, and write `Web only` here: **[FILL IN]**

**Q3.17 Are you ready for the app stores?**
Apple App Store and Google Play both review apps before they go live. Reviews can take days, and rejections are common the first time. Plan extra time.
- `[ ]` Developer account created and paid for (Apple: **[FILL IN]**, Google: **[FILL IN]**)
- `[ ]` App name, icon, screenshots, and description prepared
- `[ ]` Privacy policy link ready (see Part 5, Section 5C)
- `[ ]` The store "privacy questions" answered truthfully (what data you collect)
- `[ ]` Test login given to the store reviewers (if sign-in is needed)
- `[ ]` Age rating filled in
- `[ ]` Plan for beta testing before public release (for example TestFlight for Apple, or a closed test for Google)
- **Submission date and result:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## ⏩ Before You Reach Gate 3: Do These Parts First

Gate 3 needs answers from parts that appear **later** in this file. Before you try to pass Gate 3, go and fill in:

1. **Part 4, Section 4A** (launch preparation) and **Section 4E** (marketing and content plan)
2. **Part 5, all of 5A to 5F** (support, metrics, legal, incidents, pricing, budget)
3. **Part 6, Sections 6A and 6C** (project brief and human approval points)

Then come back here and tick Gate 3. Part 4 Sections 4B to 4D and Part 7 are done **after** launch.

## 🚦 GATE 3: Ready to Launch

- [ ] Every Must story passes its acceptance checks (Q2.2).
- [ ] The full start-to-finish test passed (Q3.7).
- [ ] At least 5 real people tried it, and the serious problems they found are fixed (Q3.9).
- [ ] There are **zero open Blockers** (Q3.12).
- [ ] Security basics are ticked (Q3.11).
- [ ] The human-only checks were done (Q3.6).
- [ ] The live and test copies are separate, and backups are on (Q3.1).
- [ ] AI features only: the test set meets my minimum score and safety checks are ticked (Q3.13 to Q3.16).
- [ ] Mobile only: store requirements are ready (Q3.17).
- [ ] Pricing and billing work end to end in test mode (Part 5, Section 5E).
- [ ] My budget and hours tracker is started (Part 5, Section 5F).
- [ ] Part 4 (launch plan and marketing, Sections 4A and 4E) and Part 5 (support, metrics, legal, incidents, pricing, budget) are filled in.
- [ ] 🛑 **HUMAN CHECK:** The owner used the live-ready product personally from start to finish.

**Decision:** `[ ] GO LIVE` `[ ] FIX FIRST` `[ ] DELAY`
**Decided by / date:** **[FILL IN]**

---

# Part 4: Launch and Growth to 500 Active Users

> **Goal:** Get your first real users, help them succeed, and learn fast, until **500 people** are active (as you defined in Q0.8).
> **Big idea:** Launch day is not the finish line. Keeping people coming back matters more than signing them up.

## 4A. Before Launch

**Q4.1 ⭐ Where will your first 100 users come from?**
Pick 2 or 3 places, not 10. Go deep in a few places.
- *Example:* `Plant groups on Reddit and Facebook. A TikTok account showing real plant rescue stories. 20 friends who own plants.`

| Channel | Why your users are there | What exactly you will do | How many users you expect |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |
| | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.2 Do you have a waiting list or early-interest list?**
- **Where do people sign up?** **[FILL IN]**
- **How many people are on it now? (Target before launch: as many as you can; 100+ is a good start)** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.3 ⭐ What is your launch page or store page saying?**
- **Headline (what it does, in under 10 words):** **[FILL IN]**
- **3 benefits (not features):** **[FILL IN]**
- **Button text and where it goes:** **[FILL IN]**
- **Screenshots or short video:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.4 ⭐ Is tracking set up BEFORE launch?**
You cannot learn from what you did not count. Tick each event you will track.
- `[ ]` Visited the page
- `[ ]` Signed up
- `[ ]` Finished onboarding (the first-time setup)
- `[ ]` **Activation event** (the "aha moment" from Q2.5). Name: **[FILL IN]**
- `[ ]` Returned on day 1 / day 7 / day 28
- `[ ]` Became an Active User (Q0.8)
- `[ ]` Paid (if you charge)
- `[ ]` Cancelled or deleted account
- **Tool used:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.5 Does the first-time experience (onboarding) get people to the "aha moment" quickly?**
- *Example:* `3 steps. User sees their first plant reminder in under 2 minutes.`
- **Number of steps before the aha moment:** **[FILL IN]**
- **Time to reach it:** **[FILL IN]**
- **Welcome message or email:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.6 Launch-day readiness checklist.**
- `[ ]` Someone (you) is free for the first 48 hours to answer questions and fix problems.
- `[ ]` Alerts are on, so you hear about breakages before users tell you (Part 5, Section 5D).
- `[ ]` The launch message or post is already written.
- `[ ]` The launch email to the waiting list is scheduled.
- `[ ]` Support email or chat is working and tested.
- `[ ]` Terms and privacy policy are live (Part 5, Section 5C).
- `[ ]` A way to go back to the previous version is ready (Part 5, Section 5D).
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.7 Will you launch to everyone at once or in small steps?**
- `[ ]` **Small steps (recommended):** first 10 people, then 50, then open to all.
- `[ ]` Everyone at once.
- **Your plan and dates:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 4B. Launch Day and Week 1

**Q4.8 Launch-day log. Fill in as it happens.**

| Time | What you did | What happened | Anything broken? |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |

- **Sign-ups on day 1:** **[FILL IN]**
- **Users who reached the aha moment on day 1:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 4C. Growing From 0 to 500

For each milestone, answer the same five questions. Copy the block for each milestone.

### Milestone Block: 10 Active Users

- **Date reached:** **[FILL IN]**
- **Where did they come from?** **[FILL IN]**
- **Did they reach the aha moment? How many percent?** **[FILL IN]**
- **What are the top 3 complaints or questions?** **[FILL IN]**
- **What will you change next because of this?** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

### Milestone Block: 50 Active Users

- **Date reached:** **[FILL IN]**
- **Where did they come from?** **[FILL IN]**
- **How many came back after 7 days?** **[FILL IN]**
- **What are the top 3 complaints or questions?** **[FILL IN]**
- **What will you change next because of this?** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

### Milestone Block: 100 Active Users

- **Date reached:** **[FILL IN]**
- **Which channel worked best, and which did not?** **[FILL IN]**
- **How many came back after 7 and 28 days?** **[FILL IN]**
- **What are the top 3 complaints or questions?** **[FILL IN]**
- **What will you change next because of this?** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

### Milestone Block: 250 Active Users

- **Date reached:** **[FILL IN]**
- **Is support still manageable by you? How many hours per week?** **[FILL IN]**
- **What does each new user cost you (time, money)?** **[FILL IN]**
- **What are the top 3 complaints or questions?** **[FILL IN]**
- **What will you change next because of this?** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

### Milestone Block: 500 Active Users 🎉

- **Date reached:** **[FILL IN]**
- **Retention (percent still active after 28 days):** **[FILL IN]**
- **Revenue so far (if any):** **[FILL IN]**
- **Total cost so far:** **[FILL IN]**
- **What worked best:** **[FILL IN]**
- **What was the biggest mistake:** **[FILL IN]**
- **What is the plan for the next stage (1,000 users and beyond)?** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 4D. Weekly Growth Rhythm

**Q4.9 ⭐ Every week, spend 30 to 60 minutes on this routine.**

| Step | What to do | Done this week? |
|---|---|---|
| 1 | Open your dashboard and write down the numbers (Part 5, Section 5B). | `[ ]` |
| 2 | Read every piece of customer feedback from this week. | `[ ]` |
| 3 | Look at 3 users who left. Why did they leave? | `[ ]` |
| 4 | Pick the **ONE** thing most likely to help. Write it down. | `[ ]` |
| 5 | Ask Claude to build or fix it (using the Build Loop in Part 3). | `[ ]` |
| 6 | Write one sentence in the Learning Log (Part 7). | `[ ]` |

- **Your weekly routine day and time:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.10 What will make you stop, pause, or change direction?**
Decide this now, while you are calm.
- *Example:* `If after 8 weeks fewer than 20 people are active and 7-day retention is under 10 percent, I will pause growth work and fix onboarding for 2 weeks.`
- **Your "pause" rule:** **[FILL IN]**
- **Your "stop" rule:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 4E. Marketing and Content Plan

> **Fill this in during Section 4A, before launch.** Marketing is how strangers find out you exist. Keep it small and steady.

**Q4.11 ⭐ How will you explain what your product is? (Positioning)**
- *Example:* `For busy plant owners who forget to water, PlantPal is a reminder app that learns each plant's schedule. Unlike a calendar, it knows each plant.`
- **For (who):** **[FILL IN]**
- **Who have this problem:** **[FILL IN]**
- **[Product name] is a (type of product):** **[FILL IN]**
- **That (main benefit):** **[FILL IN]**
- **Unlike (what they use now):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.12 ⭐ What will you share, how often, and where?**
Pick a rhythm you can keep for 12 weeks. Steady beats loud.
- *Example:* `2 short videos per week on TikTok. 1 helpful post per week in plant groups. 1 email per month to the list.`

| Where | What you will post | How often | Who creates it (You / Claude draft + you approve) |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |
| | | | |

- 🛑 **HUMAN CHECK:** You read and approve every public post before it goes out.
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.13 Can people find you by searching? (SEO)**
SEO means **Search Engine Optimization**: helping search sites like Google show your pages.
- **3 phrases your customers would type into a search box:** **[FILL IN]**
- **Pages or articles you will write for them:** **[FILL IN]**
- **Store listing keywords (mobile):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.14 Email plan.**
- `[ ]` Welcome email (sent right after sign-up)
- `[ ]` "You have not tried [aha moment] yet" nudge (sent after 2 days of silence)
- `[ ]` "We miss you" email (sent after 14 days of silence)
- `[ ]` Launch announcement
- **Email tool:** **[FILL IN]**
- `[ ]` Every marketing email has an easy unsubscribe link and follows the email rules where your users live (check Q5.10).
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q4.15 Community and word of mouth.**
- **Where will you answer questions and be useful (not just advertise)?** **[FILL IN]**
- **How will you ask happy users for a review, a referral, or a quote?** **[FILL IN]**
- **Rule:** Read each group's rules before posting. Never fake reviews or fake accounts.
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 🚦 GATE 4: Milestone 500 Reached and Reviewed

- [ ] 500 Active Users reached by my own definition in Q0.8.
- [ ] I filled in every Milestone Block.
- [ ] I know the retention rate at 7 and 28 days.
- [ ] I know the cost and revenue per user.
- [ ] I wrote down what worked, what failed, and what is next.
- [ ] The Final Review in Part 7 is complete.
- [ ] 🛑 **HUMAN CHECK:** The owner decided: scale, change, or stop.

**Decision:** `[ ] SCALE UP` `[ ] CHANGE DIRECTION` `[ ] STOP`
**Decided by / date:** **[FILL IN]**

---

# Part 5: The Operations Engines (Support, Metrics, Legal, Incidents, Pricing, Budget)

> These six run alongside Parts 3 and 4. Fill them in before launch (Gate 3).

## 5A. Support and Feedback

**Q5.1 ⭐ How can a customer ask for help?**
- *Example:* `Email support@plantpal.com, plus a "Help" button inside the app.`
- **Contact method(s):** **[FILL IN]**
- **Promised reply time (be realistic):** **[FILL IN]**
- **Support hours:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.2 ⭐ How do you sort what comes in?**

| Type | Example | What you do | Within how long |
|---|---|---|---|
| **Urgent** | Cannot sign in, data lost, charged wrongly | Drop everything | **[FILL IN]** |
| **Bug** | Something is broken | Add to bug list (Q3.12) | **[FILL IN]** |
| **Question** | "How do I...?" | Answer, then ask if the app can explain it better | **[FILL IN]** |
| **Idea** | "Please add..." | Save to the idea list | **[FILL IN]** |
| **Praise** | "I love this!" | Say thanks, save the quote (with permission) | **[FILL IN]** |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.3 Ready-made replies (templates) for common questions.**
Ask Claude to draft them, then 🛑 read and edit every one. Keep them kind, short, and human.

| Situation | Your reply template |
|---|---|
| Cannot sign in | **[FILL IN]** |
| Found a bug | |
| Wants a refund | |
| Asks for a feature | |
| Wants their data deleted | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.4 ⭐ How will you collect feedback on purpose, not just wait for it?**
- `[ ]` A one-question survey after the aha moment (for example, "How easy was that? 1 to 5")
- `[ ]` A short message to users who stopped coming ("What made you stop?")
- `[ ]` A 15-minute call with 1 to 2 active users every week
- **Where all feedback is saved in one place:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.5 How do you decide what to build next?**
- *Example:* `I rank ideas by: how many users asked, how much it helps the aha moment, how hard it is. I only do one at a time.`
- **Your rule:** **[FILL IN]**
- **Where the idea list lives:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 5B. Metrics and Dashboard

**Q5.6 ⭐ Which numbers will you watch? Fill in your targets.**
*Metric* means a number that tells you how you are doing. Example targets are rough starting guesses; real products vary a lot. Replace them with targets you believe in after a few weeks of real data.

| Metric | Plain meaning | How to calculate | Your target |
|---|---|---|---|
| **Sign-ups** | New accounts | Count per week | **[FILL IN]** |
| **Activation rate** | Out of everyone who signed up, how many reached the aha moment | People who did the aha event divided by people who signed up, times 100 | *Example: 40% or more* |
| **Time to first value** | How long until the aha moment | Median minutes from sign-up to aha | *Example: under 5 minutes* |
| **Day 1 / Day 7 / Day 28 retention** | How many come back | People active on that day divided by people who signed up | **[FILL IN]** |
| **Active Users** | Your main number (Q0.8) | Count in your time window | 500 |
| **Churn** | How many leave | Users lost this period divided by users at the start | **[FILL IN]** |
| **Conversion to paid** | Out of free users, how many pay (if you charge) | Paying divided by total, times 100 | **[FILL IN]** |
| **Cost per user** | Your spend to get one user | Total spend divided by new users | **[FILL IN]** |
| **Monthly revenue** | Money coming in (if any) | Sum of payments | **[FILL IN]** |
| **Support load** | Messages per week and hours spent | Count and hours | **[FILL IN]** |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.7 Where is your dashboard, and who looks at it when?**
- **Dashboard link:** **[FILL IN]**
- **Looked at: daily during launch week, then weekly.** Your plan: **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.8 A rule to avoid fooling yourself.**
Total sign-ups can look great while nobody comes back. Always put **Active Users** and **retention** on the dashboard next to sign-ups.
- `[ ]` I agree. My dashboard shows both.
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 5C. Legal, Privacy, and Security

> ⚠️ **Important:** This section is a checklist to prompt your thinking. It is **not legal advice.** Laws differ by country and by what you build. For anything involving payments, children, health, or other sensitive data, ask a qualified lawyer.

**Expert Check for all of Section 5C:** Checked by **[FILL IN]** on **[FILL IN]**

**Q5.9 ⭐ Which legal pages do you need, and are they live?**
- `[ ]` **Privacy Policy** (says what data you collect, why, and who sees it). Link: **[FILL IN]**
- `[ ]` **Terms of Service** (the rules for using your product). Link: **[FILL IN]**
- `[ ]` **Cookie notice** (if your website uses cookies or tracking). Link: **[FILL IN]**
- `[ ]` Refund policy (if you charge). Link: **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.10 ⭐ Where will your users live, and which privacy laws might apply?**
- *Example:* `Users in the US and EU. EU means GDPR (a European data-protection law) may apply. California users mean CCPA/CPRA may apply.`
- **Countries or regions of users:** **[FILL IN]**
- **Laws I need to check:** **[FILL IN]**
- **Who I asked (lawyer, advisor, official guide):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.11 Can users control their own data?**
- `[ ]` Users can see what you store about them.
- `[ ]` Users can delete their account and data.
- `[ ]` Users can export their data (if required where they live).
- `[ ]` Users can turn off marketing emails.
- **How a user does each of these:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.12 Are children likely to use your product?**
Rules for under-13s (and in some places under-16s or under-18s) are much stricter.
- `[ ]` No, and I say so in my Terms.
- `[ ]` Yes. My plan: **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.13 Payments (if any).**
- **Payment provider:** **[FILL IN]**
- `[ ]` I never store card numbers myself. The payment provider does.
- `[ ]` Refunds and cancellations are easy and written down.
- `[ ]` Taxes: I checked what applies (or will ask an accountant). Notes: **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.14 Third-party licenses and AI rules.**
- `[ ]` I checked that the code libraries I use allow commercial use.
- `[ ]` I checked that the images, fonts, and icons I use allow commercial use.
- `[ ]` If I use AI services, I read their rules for what is allowed, and what happens to my users' data.
- `[ ]` I did **not** paste real customer data or secrets into AI tools unless I understand how that data is handled.
- **Notes:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 5D. Incidents and Rollback

An **incident** is any time the product breaks in a way users can notice. Plan **now**, so you do not panic later.

**Q5.15 ⭐ How will you find out something is broken?**
- `[ ]` Automatic alert when the product is down (tool: **[FILL IN]**)
- `[ ]` Automatic alert for errors (tool: **[FILL IN]**)
- `[ ]` Alert goes to: **[FILL IN]** (phone push, email, or text; pick something you will actually see)
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.16 ⭐ How serious is it? (Severity levels)**

| Level | What it means | Example | What you do |
|---|---|---|---|
| **SEV 1** | Everyone is blocked, data is lost or leaked, or money is wrong | Site is down. Data exposed. | Drop everything. Fix or roll back now. Tell users. |
| **SEV 2** | Main feature broken for many | Cannot add plants | Fix today. Tell affected users. |
| **SEV 3** | Small or limited problem | One screen looks wrong | Fix in the normal weekly work. |

- **Anything you want to change in this table:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.17 ⭐ How do you go back to the last working version? (Rollback)**
- *Example:* `In my hosting tool, I click "Redeploy previous version". For the database, I restore last night's backup.`
- **Steps to roll back the app:** **[FILL IN]**
- **Steps to restore the database:** **[FILL IN]**
- **Last time I practiced this:** **[FILL IN]** *(Practice at least once before launch.)*
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.18 What do you say to users during a problem?**
Be fast, honest, and plain. Say what happened, who is affected, what you are doing, and when you will update again.
- **Where you post updates (status page, social media, email):** **[FILL IN]**
- **A template message:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.19 ⭐ If user data might have leaked.**
- **First 3 things I do (example: lock access, stop the leak, write down what happened):** **[FILL IN]**
- **Who I must tell, and how fast (laws can set deadlines; check Q5.10):** **[FILL IN]**
- **Expert Check:** Checked by **[FILL IN]** on **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.20 After every SEV 1 or SEV 2: write a short "what we learned" note.**
Blame is not the point. Fixing the cause is.

| Date | What happened | Why it happened | What we changed so it cannot happen again |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 5E. Pricing and Billing

**Q5.21 ⭐ What are your plans and prices?**
- *Example:* `Free: up to 3 plants. Plus: $4 per month or $36 per year, unlimited plants.`

| Plan name | Price (monthly / yearly) | What is included | Who it is for |
|---|---|---|---|
| **[FILL IN]** | | | |
| | | | |
| | | | |

- **Why these prices (cost to serve, what alternatives charge, what customers said):** **[FILL IN]**
- **Break-even check (from Q1.8):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.22 How do people try before they pay?**
- `[ ]` Free plan forever (limited)
- `[ ]` Free trial (how many days: **[FILL IN]**)
- `[ ]` Money-back period (how many days: **[FILL IN]**)
- `[ ]` No free option
- **When the user is asked to pay (which moment, which screen):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.23 ⭐ How will you test your price?**
Do not guess forever. Try 2 or 3 prices with different groups of early users, one change at a time.
- *Example:* `First 50 users see $4. Next 50 see $6. I compare how many pay.`
- **Test plan:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.24 ⭐ What happens when things go wrong with money?**

| Situation | What the user sees | What you do |
|---|---|---|
| Card is declined or expires | **[FILL IN]** | |
| User wants to cancel | | |
| User wants a refund | | |
| User is charged twice | | |
| User wants to change plan | | |

- `[ ]` Cancelling is as easy as signing up.
- `[ ]` I tested every payment case in **test mode** (fake cards) before launch.
- **Expert Check (payments, taxes, refund rules):** Checked by **[FILL IN]** on **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 5F. Budget and Time Tracking

**Q5.25 ⭐ Track what you spend and what you earn, every month.**
- *Why it matters:* Many small costs (tools, AI usage, ads) add up quietly.

| Month | Hosting and tools | AI usage | Ads and marketing | Other | Total spent | Revenue | Net (revenue minus spent) |
|---|---|---|---|---|---|---|---|
| **[FILL IN]** | | | | | | | |
| | | | | | | | |
| | | | | | | | |

- **Alert level (the monthly total at which you stop and check):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.26 Track where your hours go.**

| Week | Building | Support | Marketing | Learning or fixing | Total hours | Matches Q0.6? |
|---|---|---|---|---|---|---|
| **[FILL IN]** | | | | | | |
| | | | | | | |
| | | | | | | |

- **What you learned from the hours (for example, "support takes more time than I planned"):** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q5.27 Cost per milestone.**
At each Active User milestone (Q1.11), write the total spent so far and the cost per active user. This shows if growth is affordable.

| Milestone | Total spent so far | Cost per active user | Still within budget (Q0.7)? |
|---|---|---|---|
| 10 | **[FILL IN]** | | |
| 50 | | | |
| 100 | | | |
| 250 | | | |
| 500 | | | |

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

---

# Part 6: The Claude Toolkit

> This Part holds the pieces that make Claude work well for you: the project brief, the helper roles, the approval points, and ready-to-use prompts.
> **Golden rule:** Claude is a fast, helpful, and sometimes overconfident helper. You are the owner.

## 6A. The Project Brief (`CLAUDE.md`)

`CLAUDE.md` is a plain text file in your project that Claude Code reads at the start of every session. It is Claude's memory of your project. Keep it **short** (aim for under 200 lines), **specific**, and **testable**. "Write clean code" is useless. "Run `npm test` before saying a task is done" is useful. Only include things Claude cannot work out by reading the code.

**Q6.1 ⭐ Fill in the brief. Then copy the finished text into a file called `CLAUDE.md` at the top of your project.**

```markdown
# Project: [FILL IN: product name from Q0.1]

## What this is
[FILL IN: one sentence from Q0.2]

## Who it is for
[FILL IN: person from Q1.2]

## Current stage
[FILL IN: Idea / Spec / Build / Launch / Growth]

## How to run it
- Install: [FILL IN: command]
- Start: [FILL IN: command]
- Test: [FILL IN: command]
- Check for errors and style: [FILL IN: command]
- Build: [FILL IN: command]

## Folder map
[FILL IN: 5 to 10 lines. Example: "/app = screens, /api = server code, /docs = documents"]

## Tools and technology
[FILL IN: list from Q2.9]

## Rules Claude must follow
- Work on ONE task at a time from the task list in this playbook (Q2.14).
- Explain your plan in plain words and wait for approval before writing code.
- Write a failing test first, then the code. Show me the test result.
- Keep each change small (about [FILL IN: limit from Q3.4] changed lines).
- [FILL IN: your own rule, for example "Use plain function names, no clever tricks"]
- [FILL IN: your own rule]

## Things Claude must NEVER do without my explicit OK
- Delete or change real user data.
- Change login, password, or payment code.
- Change the database structure.
- Add new paid services or new code libraries.
- Touch the live (production) copy.
- Paste or store secrets (passwords, keys) anywhere in code or chat.

## Known traps and quirks
[FILL IN: things that surprised you. Example: "Database migrations: always run the 'db:push' command, never edit SQL by hand"]

## Done means
[FILL IN: copy your definition of done from Q3.2]

## Where to find more
- Full plan: Product_Operations_Playbook.md
- Requirements: [FILL IN: link]
- Design: [FILL IN: link]
```

- **Date the brief was created / last reviewed:** **[FILL IN]**
- **Rule:** Review `CLAUDE.md` after every milestone and whenever Claude repeats the same mistake. If Claude keeps ignoring a rule, the file is probably too long. Shorten it.
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 6B. Helper Roles and Handoffs

Even if you only use one Claude, it helps to ask it to play **one role at a time**. Different roles catch different mistakes. A review done in a separate, fresh session from the build is more trustworthy.

**Q6.2 ⭐ Review the roles. Edit what you need.**

| Role | Job | Receives | Hands over | Human check? |
|---|---|---|---|---|
| **Researcher** | Finds facts, competitors, and risks | Your questions | A short research note with sources | 🛑 Yes: check the sources |
| **Planner** | Turns ideas into stories, checks, and small tasks | Part 1 answers | Part 2 stories and task list | 🛑 Yes: approve the plan |
| **Builder** | Writes the code for one task | One task plus `CLAUDE.md` | Code, tests, a summary | Automatic checks first |
| **Tester** | Writes and runs tests, tries to break things | Finished code and acceptance checks | Test report, bug list | 🛑 Yes: read failures |
| **Reviewer** | Reads changes with fresh eyes, looks for bugs, security, and unclear code | The change and its evidence | A list of problems and risk level | 🛑 Yes for risky changes |
| **Writer** | Drafts help text, emails, release notes, support replies | Facts and tone from you | Draft text | 🛑 Yes: you approve all public words |
| **Analyst** | Reads metrics and feedback, proposes the next step | Dashboard numbers and feedback | A short "what I see, what I suggest" | 🛑 Yes: you decide |

- **Roles you will not use:** **[FILL IN]**
- **Roles you added:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q6.3 What gets handed from one role to the next?**
Each stage should leave a written note, so the next stage never has to guess. Tick what you will keep for every feature.
- `[ ]` Intent note: why this feature exists (one paragraph)
- `[ ]` Spec: what it must do and its acceptance checks
- `[ ]` Plan: how it will be built
- `[ ]` Changes plus tests
- `[ ]` Review note
- `[ ]` Release note
- **Where these notes are stored:** **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 6C. Human Approval Points

Claude does the first pass. You own the gates. "A human reviews" is too vague, so name **what** you review and **when**.

**Q6.4 ⭐ Review the approval table and change it to match your comfort level.**

| Moment | What you must look at | Can Claude go ahead without you? |
|---|---|---|
| End of Part 1 | The research and the GO decision | **No** |
| End of Part 2 | The spec, the screens, the plan | **No** |
| Before each build task | Claude's plan in plain words | **No** (for risky tasks). Low-risk: your choice. |
| After each build task | Summary, tests, and checks result | **No.** Read the evidence. |
| Anything in the "human-only" list (Q3.6) | The actual change | **No, ever** |
| Before going live | Everything in Gate 3 | **No** |
| Messages to customers | Every word | **No** |
| Spending money or adding a paid tool | Cost and reason | **No** |
| Reading dashboards | Claude can summarize | **Yes**, but you decide what to do |

- **Your changes:** **[FILL IN]**
- **Risk levels:** *Low* = looks, wording, small text changes. *Medium* = normal features. *High* = login, payments, user data, database, AI behavior. High always means a human reads the change.
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

**Q6.5 What are the warning signs that Claude's work should not be trusted yet?**
- `[ ]` Claude says "done" but shows no test results.
- `[ ]` Claude changed files that were not part of the task.
- `[ ]` Claude changed or deleted tests to make them pass.
- `[ ]` Claude added a new code library without saying so.
- `[ ]` Claude's explanation does not match what the code does.
- `[ ]` Claude says "this should work" instead of showing it working.
- **Your response when you see these:** *Example: stop, start a fresh session, give a smaller task.* **[FILL IN]**
- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

## 6D. Prompt Library

Copy, paste, then replace the parts in `[brackets]`. Save your best prompts here so you can reuse them across projects.

**Q6.6 ⭐ Check each prompt. Add your own at the bottom.**

**Research**
```
Act as a researcher. I am building [product, one sentence]. Find the 5 most
important alternatives people use today. For each, tell me what it does well,
what users complain about, and the price. Give a link for every claim. If you
are not sure about something, say "not sure". Do not make anything up.
```

**Interview me (fills this playbook)**
```
Open Product_Operations_Playbook.md. Interview me one question at a time,
starting at [Question number]. Wait for my answer. Then write my answer into
the file. If my answer is vague, ask one follow-up. If I say I do not know,
write UNKNOWN with an owner and a date. Do not move to the next question until
I say "next".
```

**Write user stories**
```
Using Part 1 of my playbook, write user stories in the form "As a [person], I
want to [action], so that [benefit]". For each Must story, add 3 acceptance
checks I can answer with Yes or No. Keep it to the MVP only.
```

**Break into tasks**
```
Split these user stories into tasks that each take 1 to 2 hours. Order them so
that each task can be tested on its own. For each, write "done when..." in one
sentence.
```

**Plan before coding**
```
Read CLAUDE.md. Your task is [task ID and sentence]. Before writing any code,
explain in plain words: what you will change, which files, what could go
wrong, and how you will test it. Wait for my OK.
```

**Build with tests first**
```
Task: [task]. Write one failing test that shows what "working" means. Show me
it fails. Then write the smallest code to pass it. Run all checks. Give me a
summary: what changed, which files, test results, and anything you are unsure
about. Do not change anything outside this task.
```

**Fresh-eyes review**
```
You are a careful reviewer who did not write this code. Review this change
for: bugs, security problems, anything that exposes user data, anything
confusing, and anything that does more than the task asked. List problems by
how serious they are. Say "no problems found" only if you really checked.
```

**Break my product (QA)**
```
Act as a tester trying to break [feature]. List 15 unusual things a user could
do (empty fields, very long text, double-tapping, no internet, wrong order of
steps). For each, say what should happen. Then help me test them one by one.
```

**Explain it simply**
```
Explain what this code or error does as if I am a smart 10-year-old. Then tell
me what I should do next. Do not use jargon without explaining it.
```

**Customer support reply**
```
Draft a short, kind reply to this customer message: "[paste message]". Our
tone is [tone]. Do not promise anything we have not decided. If it is a bug,
say sorry and say we are looking into it. Keep it under 100 words.
```

**Release note**
```
Write a release note for users from this list of changes: [list]. Use plain
words. Group it as "New", "Better", and "Fixed". Keep it under 120 words. Do
not mention anything that is not in the list.
```

**Weekly metrics check**
```
Here are this week's numbers: [paste]. Compare them to my targets in Q5.6.
Tell me: (1) what changed, (2) what I should NOT conclude from so little data,
(3) the one thing most worth trying next week. Do not invent numbers.
```

**Incident help**
```
Something is broken: [what users see]. Started at [time]. Help me: (1) decide
if I should roll back, (2) list the 3 most likely causes, (3) draft a short,
honest message to users. Ask me for any logs you need. Do not run anything on
the live system without my OK.
```

**My own prompts:** **[FILL IN]**

- Status: `[ ] Not started` `[ ] In progress` `[ ] Done`

---

# Part 7: Learning and Memory

> **Goal:** Keep what you learn, so the next project is faster and you never solve the same problem twice. This is your **institutional knowledge** (the useful things your team or you know, saved in writing).

## 7A. Decision Log

Write down every important decision, and the reason. Future you will forget why.

| Date | Decision | Options considered | Why this one | Who decided |
|---|---|---|---|---|
| **[FILL IN]** | | | | |
| | | | | |
| | | | | |

*Example:* `2026-11-10 | Use Supabase for database | Firebase, Supabase, own server | Free to start, built-in sign-in, I know SQL | Sam`

## 7B. Learning Log

One or two lines per week. What did you learn about users, the product, or yourself?

| Week | What I learned | What I will do differently |
|---|---|---|
| **[FILL IN]** | | |
| | | |
| | | |

## 7C. Mistakes and Fixes

| Date | What went wrong | What I changed (rule, check, or note) |
|---|---|---|
| **[FILL IN]** | | |
| | | |

## 7D. Final Review (after Gate 4)

Complete this after you reach 500 Active Users, or after you decide to stop.

- **Did we solve the problem in Q1.1? How do we know?** **[FILL IN]**
- **What was the best decision?** **[FILL IN]**
- **What was the costliest mistake?** **[FILL IN]**
- **Which part of this playbook helped the most?** **[FILL IN]**
- **Which question was confusing or missing? (Use this to improve the template.)** **[FILL IN]**
- **What would I do differently next time with a brand-new project?** **[FILL IN]**
- **Reusable things to save for the next project (prompts, checklists, design, code):** **[FILL IN]**
- **Where those things are saved:** **[FILL IN]**

---

# Appendix A: Glossary (Plain-English Word List)

| Word | What it means |
|---|---|
| **Acceptance check** | A Yes/No test that proves a feature works. |
| **Active User** | A person who really used your main feature recently. You define it in Q0.8. |
| **Activation / Aha moment** | The first time a user feels the product's value. |
| **Agent (AI agent)** | An AI helper that can do several steps on its own, like reading files and writing code. |
| **App Store review** | Apple's and Google's check before your app is allowed in their store. |
| **Architecture** | The big-picture map of how the parts of your product connect. |
| **Backup** | A saved copy of your data, in case something breaks. |
| **Back end** | The behind-the-scenes part of a product that users do not see. |
| **Blocker** | A bug so serious you cannot launch until it is fixed. |
| **Churn** | The share of users who leave in a period. |
| **CLAUDE.md** | A file in your project that tells Claude Code about your project and your rules. |
| **Database** | Where your product saves its information. |
| **Definition of done** | The list that must be true before a task counts as finished. |
| **Front end** | The part of a product that users see and tap. |
| **Gate** | A checkpoint between Parts. You may only continue when every box is ticked. |
| **GDPR / CCPA** | Privacy laws (Europe / California). Check which apply to your users. |
| **Human check (🛑)** | A moment where a real person must read and approve. |
| **Incident** | A time when your product breaks in a way users can notice. |
| **Metric** | A number that tells you how you are doing. |
| **MVP** | Minimum Viable Product: the smallest version that solves the main problem. |
| **Onboarding** | The first-time experience that helps a new user reach the aha moment. |
| **PRD** | Product Requirements Document: a plain list of what the product must do. |
| **Production / Live** | The real version that real users use. |
| **QA** | Quality Assurance: making sure the product works properly. |
| **Retention** | How many users come back after some time. |
| **Rollback** | Going back to the last version that worked. |
| **Secret** | A password, key, or token. Never put it in code or chat. |
| **Severity (SEV)** | How serious a problem is. SEV 1 is the worst. |
| **Test copy (staging)** | A practice copy of your product used for trying things safely. |
| **User flow** | The path a user takes from opening the product to getting value. |
| **User story** | A sentence: "As a [person], I want [action], so that [benefit]." |
| **Version control (Git)** | A tool that records every change to your files and lets you undo. |

---

# Appendix B: Working With More Than One Person (Optional)

> Skip this if you work alone. Come back when a second person (helper, partner, contractor, or reviewer) joins.

**Q-B.1 Who is on the project, and what do they own?**
Use **R / A / C / I** for each row:
- **R (Responsible):** does the work
- **A (Accountable):** makes the final decision (only **one** A per row)
- **C (Consulted):** gives advice before the decision
- **I (Informed):** is told afterwards

| Area | Name 1 | Name 2 | Name 3 | Claude (AI helper) |
|---|---|---|---|---|
| Idea and validation (Part 1) | **[FILL IN]** | | | C |
| Spec and design (Part 2) | | | | R (draft) |
| Building (Part 3) | | | | R (draft) |
| Reviewing and approving changes | | | | I |
| Launch and marketing (Part 4) | | | | R (draft) |
| Support (5A) | | | | R (draft replies) |
| Legal, privacy, security (5C) | | | | C |
| Money, pricing, budget (5E, 5F) | | | | C |
| Final GO / NO-GO at every Gate | | | | I |

*Rule:* Claude is never the **A** (accountable) for anything. A person always is.

**Q-B.2 How do people add their own answers to this file?**
- **Add a column or a line saying "Owner" and "Reviewer" to any question that needs one.** Example: `Owner: Maya. Reviewer: Sam.`
- **Only the Accountable person changes a Gate decision.**
- **Every change goes in the Change Log (Appendix E).**
- **Notes on how this team works (meetings, chat channel, who answers what, by when):** **[FILL IN]**

---

# Appendix C: Starting a New Project With This Template (Reuse Guide)

> Use this every time you start project number 2, 3, ... 100.

## C1. New-Project Checklist

- [ ] 1. **Copy** the original, clean template file. Never work in the master copy.
- [ ] 2. **Rename** the copy so people can find it later. Suggested name: `Product_Operations_Playbook_[ProductName].md`
- [ ] 3. **Fill in Part 0** (basics) first.
- [ ] 4. **Add a row** for the project in the Portfolio Tracker (C2).
- [ ] 5. **Set a weekly day and time** for your routine (Q4.9).
- [ ] 6. **Copy over** anything reusable from earlier projects: your best prompts (Part 6D), legal pages, your `CLAUDE.md` rules, your tool choices (Q2.9).
- [ ] 7. **Do not copy** answers about customers, prices, or risks from another project. Each product has its own answers.
- [ ] 8. When the project ends (or after 500 users), complete the **Final Review (7D)** and send the good parts back to the master template.

## C2. Portfolio Tracker (keep one copy of this table for all your projects)

| Project name | Current Part | Last Gate passed | Active Users now | Monthly spend | Monthly revenue | Next action | Next review date |
|---|---|---|---|---|---|---|---|
| **[FILL IN]** | | | | | | | |
| | | | | | | | |
| | | | | | | | |

**How to read it:** Look at this table once a week. If a project has no "next action" or its review date has passed, that project is **stuck**. Decide: continue, pause, or stop (see your rules in Q4.10).

## C3. Improving the Master Template

Every time you finish a project, answer these and update the master template.
- **Which question did people find confusing?** **[FILL IN]**
- **Which question was missing?** **[FILL IN]**
- **Which question was never used? (Consider marking it optional.)** **[FILL IN]**
- **New template version number and date:** **[FILL IN]**

---

# Appendix D: Worked Example (PlantPal, Short Version)

> This shows what **good** answers look like. Your answers should be this short and this clear. This is **made-up sample data**. Do not copy it into your own file.

## Part 0

- **Product name:** PlantPal
- **One sentence:** PlantPal reminds busy people when to water each of their houseplants.
- **Type:** Mobile app (iPhone and Android)
- **Owner:** Sam Lee
- **Active User means:** Someone who logs at least one plant watering in the last 28 days.

## Part 1 (Idea and Validation)

- **Problem:** I forget to water my plants and they die. I do not know which plant needs water when.
- **Typical person:** Anna, 29, city flat, 8 houseplants, long work hours, iPhone user.
- **Conversations held:** 12. Nine said they killed a plant in the last year. Four said they would pay.
- **Alternatives:** Phone calendar (manual and boring), a paper notebook, plant-care blogs (not personal).
- **Our edge:** Photo recognition plus an automatic watering schedule.
- **Money:** Free for up to 3 plants. $4 per month for unlimited plants.
- **Top 3 risks:** (1) People forget to open the app. (2) Plant recognition is wrong too often. (3) App store rejects the app.
- **MVP:** Add a plant by photo and get a watering reminder. Nothing else.
- **Not now:** Social features, web version, shop.
- **Gate 1 decision:** GO (Sam Lee, 2026-11-01). Reason: 9 of 12 people had the problem, and the idea is small enough to build in 8 weeks.

## Part 2 (Spec and Design)

- **Story US-1:** As a plant owner, I want to add a plant by taking a photo, so that I do not have to type its name.
- **Acceptance checks for US-1:** (1) A plant name shows within 5 seconds. (2) The user can correct the name. (3) The plant appears in "My Plants".
- **Main flow:** Open app, sign up, tap "Add plant", take photo, confirm name, see reminder date.
- **Aha moment:** The user sees their first watering reminder date.
- **Empty screen words:** "No plants yet. Tap + to add your first one!"
- **Tools:** Expo (mobile app), Supabase (database and sign-in), RevenueCat (payments), PostHog (analytics), Sentry (errors).
- **Data collected:** Email, plant photos, watering dates. No location, no phone number.
- **Task T-1:** Create the sign-up screen. **Done when:** a new user can create an account and see an empty "My Plants" screen.

## Part 3 (Build and QA)

- **Task size limit:** One task and about 200 changed lines per review.
- **Human-only checks:** Login, payments, deleting data, database changes.
- **Real testers:** 6 plant owners. Four finished the main flow. Two got stuck on the photo screen. We changed the button text and retested.
- **AI test set:** 25 questions. Score: 92 percent Pass on normal cases, 100 percent on safety cases.
- **Gate 3 decision:** GO LIVE (Sam Lee, 2027-01-20).

## Part 4 (Launch and Growth)

- **First 100 users:** Plant groups on Reddit and Facebook, plus short plant-rescue videos on TikTok.
- **Milestone 10 users:** Reached on day 3. Top complaint: reminder time cannot be changed. Next: add a reminder-time setting.
- **Milestone 50 users:** Reached in week 2. 7-day retention: 28 percent.
- **Milestone 500 users:** Reached in week 17. 28-day retention: 31 percent. Cost per active user: $2.10.

## Part 5 (Operations Engines)

- **Support:** support@plantpal.example. Reply within 24 hours on weekdays.
- **SEV 1 rule:** Anything that blocks sign-in or loses data. Fix or roll back within 1 hour.
- **Rollback:** In the hosting tool, click "Redeploy previous version". Restore last night's backup for the database.
- **Pricing test:** First 50 users saw $4. Next 50 saw $6. We kept $4 because 11 percent paid at $4 versus 6 percent at $6.
- **Expert Check (privacy pages):** Checked by a local lawyer on 2027-01-12.

## Part 7 (Learning)

- **Decision log:** 2026-11-10: Use Supabase. Options: Firebase, Supabase, own server. Reason: free to start, built-in sign-in, I know SQL.
- **Biggest lesson:** People did not come back until we added a reminder-time setting. Onboarding mattered less than the reminder.

---

# Appendix E: Change Log

Every time you change an important answer in this file, add a line.

| Date | Section changed | What changed | Why | Who |
|---|---|---|---|---|
| **[FILL IN]** | | | | |
| | | | | |

---

# Appendix F: Master Progress Tracker

Tick as you go. This gives you the whole journey on one screen.

| Part | Status | Gate passed? | Date |
|---|---|---|---|
| Part 0: Project Basics | `[ ]` | n/a | |
| Part 1: Idea and Validation | `[ ]` | `[ ]` Gate 1 | |
| Part 2: Spec and Design | `[ ]` | `[ ]` Gate 2 | |
| Part 3: Build and QA | `[ ]` | `[ ]` Gate 3 | |
| Part 4: Launch and Growth to 500 | `[ ]` | `[ ]` Gate 4 | |
| Part 5: Operations Engines (5A to 5F) | `[ ]` | (needed for Gate 3) | |
| Part 6: Claude Toolkit | `[ ]` | (needed for Gate 3) | |
| Part 7: Learning and Memory | `[ ]` | n/a | |

---

# Appendix G: Unanswered Questions Register

Every `UNKNOWN` goes here so nothing is forgotten.

| Question number | What we do not know | Who will find out | By when | Answer (when found) |
|---|---|---|---|---|
| **[FILL IN]** | | | | |
| | | | | |

---

# Appendix H: Where This Template Comes From

This template combines widely used practice from: product-operations and product-playbook templates (process, roles, tools, templates, and metrics in one place), AI-native software development guidance (small reviewable steps, written hand-off notes at each stage, automated checks first, human review focused on risky changes), SaaS launch checklists (pre-launch, launch day, post-launch, activation and retention tracking set up before launch, five or more real-user tests), and Claude Code guidance (a short, specific `CLAUDE.md`, plan before code, fresh sessions per task). Numbers shown in examples are **starting guesses only**. Replace them with your own data.

*End of Product Operations Playbook template, version 1.1*
