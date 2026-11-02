# How to Fill This Document

> **Read this first. It takes 3 minutes.**
> This file is a questionnaire. You answer the questions. When you finish, you will have a complete plan to take a product from idea to its first 500 customers, with AI agents helping you along the way.
>
> **Folder location:** `Launch, Marketing and Customer Acquisition/Onboarding_Flow.md`
> **Template version:** 2.0 (master template, locked 2026-10-18)

## ⚠️ Master-copy rules (read before you do anything else)

1. **This is the MASTER template. Never type your answers into the master file.**
2. For every new project, make a copy and rename it: `Onboarding_Flow_[PROJECT-CODE].md`
   - 💡 Example: `Onboarding_Flow_PLANTPAL-01.md`
3. Choose a short **project code** (capital letters, numbers, dashes). Write it in the title block and in A1 below.
4. Keep every project's copy in that project's own folder. Never mix two projects in one file.
5. Improved the template itself? Change the master only, raise the template version, and add a line to the Change Log (Part 11).
6. Old projects keep the template version they started with. Do not update them in the middle of a project.

## The 6 rules

1. **Go in order.** Start at Part A and finish at Part 11. Each part uses answers from the parts before it.
2. **Find every `[FILL: ...]` tag and replace it with your answer.** The text inside the tag tells you what to write. Delete the whole tag, including the brackets, when you are done.
3. **Write on the `Your answer:` line** under each question. One or two sentences is enough.
4. **Do not know the answer yet?** Write `[TBD: name, date]`. Say who will find out and by when. Never leave a question empty.
5. **A question does not apply to you?** Write `N/A - because ...` and give a short reason. Never delete a question.
6. **Be specific.** Numbers, names, and dates are always better than feelings.
   - Weak: "Lots of people will sign up."
   - Strong: "100 people will sign up in the first 14 days."

## What the symbols mean

| Symbol | Meaning |
|---|---|
| `[FILL: ...]` | You must replace this with your answer |
| `[TBD: who, when]` | You will find the answer later (must name a person and a date) |
| `N/A - reason` | This does not apply to my product |
| 🤖 | A ready-made prompt you can copy and paste to an AI agent |
| ✅ | A checkbox. Change `[ ]` to `[x]` when done |
| ⚠️ | A warning. Read it before you answer |
| 💡 | An example to help you |

## How to know you are finished

- Search the file for `[FILL:`. If you find **zero** results, every question is answered.
- Search the file for `[TBD`. Each one must name a person and a date.
- Complete **Part 9, the Completeness Checklist**. If everything is ticked, you are ready to go.

## Which parts take the longest

| Part | What it covers | Time to fill |
|---|---|---|
| A | Project Context, Roles (RACI), Budget Plan | 30 min |
| 1 | Discover and Plan | 45 min |
| 2 | Design the Onboarding Flow (includes accessibility and languages) | 70 min |
| 3 | Build and Test (includes legal basics and payments) | 90 min |
| 4 | Pre-Launch and Launch | 60 min |
| 5 | Growth to 500 Customers | 60 min |
| 6 | Risks and Fallback Plan | 30 min |
| 7 | Filled Example | read only |
| 8 | Glossary | read only |
| 9 | Completeness Checklist | 15 min |
| 10 | Decision Log (keep adding as you go) | 2 min each |
| 11 | Change Log | 2 min |
| Appendix | Sources used for this template | read only |

## Using AI agents with this file

- Each phase has a 🤖 prompt block. Copy it and paste it into your AI agent, together with **Part A** and the answers from the earlier parts.
- Before trusting anything an AI agent writes, **read it yourself** and check it against your answers.
- An AI agent can find unfinished work by searching for `[FILL:` and `[TBD`.
- ⚠️ Never paste passwords, API keys, or customer personal data into this file or into an AI prompt.

---

# Onboarding Flow: [FILL: Product Name]

> **Project code:** [FILL: e.g. PLANTPAL-01]
> **Template version used:** 2.0
> **Document version:** [FILL: 1.0]
> **Last updated:** [FILL: date, YYYY-MM-DD]
> **Filled in by:** [FILL: your name]
> **Overall status:** [FILL: Not started / In progress / Ready to launch / Launched / Reached 500 customers]

---

# Part A: Project Context, Roles, and Budget

> **Why this matters:** This part is the "business card" for your project. Any person or AI agent who reads only this part should understand what you are building, who does what, and what you can spend. Keep every answer short.

## A1. The basics

| Question | Your answer |
|---|---|
| Project code | [FILL: same code as the title, e.g. PLANTPAL-01] |
| Product name | [FILL: the name people will see] |
| One-sentence description (no jargon) | [FILL: "It helps ___ do ___ so they can ___."] |
| Product type | [FILL: Web app / Mobile app / Both / Other] |
| Product website or link (if it exists) | [FILL: URL or TBD] |
| Project owner | [FILL: your name] |
| Start date | [FILL: YYYY-MM-DD] |
| Target launch date | [FILL: YYYY-MM-DD] |
| Target date for first 500 customers | [FILL: YYYY-MM-DD] |
| Main tools you use (code, design, email, analytics) | [FILL: e.g. VS Code, Figma, Mailchimp] |
| AI agents and models you use | [FILL: e.g. Claude, Copilot, Cursor] |

## A2. What counts as a "customer"?

⚠️ This is the most important definition in the file. Everything is counted using it.

**Question A2.1:** What exactly must a person do to count as **1 customer**?
- [ ] They sign up for an account
- [ ] They finish the first-time setup
- [ ] They use the main feature at least once
- [ ] They pay money
- [ ] Other: [FILL: describe]

Your answer: [FILL: choose one and write it as one clear sentence]

> 💡 Example: "A customer is someone who created an account AND completed their first project."
> ⚠️ Onboarding guides agree on one thing: **decide what counts as success before you design any step.** A "customer" is the person who reaches real value, not just the person who clicked "sign up."

**Question A2.2:** Does your product make money?
- [ ] Free forever
- [ ] Free plan plus paid plans (freemium)
- [ ] Free trial, then paid
- [ ] Paid from day one
- [ ] One-time purchase
- [ ] Not decided yet

Your answer: [FILL: choose one and add price if known]

> 💡 Example: "Free plan, plus a paid plan at 3 dollars a month for unlimited plants."

## A3. AI-agent briefing (copy this block into any AI prompt)

```
PROJECT BRIEFING
Project code: [FILL: code]
Product: [FILL: name]
What it does: [FILL: one sentence]
Who it is for: [FILL: one sentence]
Customer definition: [FILL: from A2.1]
Business model: [FILL: from A2.2]
Platform: [FILL: web / mobile / both]
Launch date: [FILL: date]
Goal: first 500 customers by [FILL: date]
Rules for the AI agent:
- Do not invent facts. If information is missing, ask me.
- Use plain English. Explain terms a beginner would not know.
- Show your steps, and tell me what you are unsure about.
- Make small changes I can review. Ask me before anything risky (money, user data, deleting things, publishing).
```

## A4. Roles and responsibilities (RACI)

> **Beginner note:** RACI answers "who does what?" for each job.
> - **R = Responsible:** does the work
> - **A = Accountable:** makes the final decision (only **one** A per row)
> - **C = Consulted:** gives advice before the work is done
> - **I = Informed:** is told after it is done
>
> **Working alone?** Write "Me" as **A** in every row. Write "AI" as **R** where an AI agent does the work. Writing "Me" as **A** means you still check what the AI did.

**Q A4.1:** List everyone involved (people and AI agents).

| Role | Name (or AI agent) | How to reach them |
|---|---|---|
| Project owner | [FILL] | [FILL] |
| Developer | [FILL] | [FILL] |
| Designer | [FILL] | [FILL] |
| Marketing / content | [FILL] | [FILL] |
| Customer support | [FILL] | [FILL] |
| AI agent(s) | [FILL: names of tools] | [FILL: where you run them] |

**Q A4.2:** Fill in the RACI table. Put one letter (R, A, C, or I) in each cell, or leave a cell empty if that person has no part.

| Job | Owner | Developer | Designer | Marketing | Support | AI agent |
|---|---|---|---|---|---|---|
| Decide who the customer is (Part 1) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Design the onboarding flow (Part 2) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Build the product (Part 3) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Test the product (Part 3) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Say "ready to launch" (Part 3.6) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Write launch posts and emails (Part 4) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Answer users and fix problems (Part 4, 5) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Run the weekly review (Part 5.3) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Approve spending money (A5) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

💡 Solo example for one row: Owner = A, AI agent = R, everyone else empty.

⚠️ Check each row: exactly **one** A, at least one R.

## A5. Budget plan

> **Beginner note:** A budget is a promise to yourself about how much money you will spend. Write amounts in one currency: [FILL: e.g. USD].

**Q A5.1:** Fill in what you expect to spend.

| Cost | One-time | Per month | Notes |
|---|---|---|---|
| Domain name and website hosting | [FILL] | [FILL] | [FILL] |
| Software tools (email, analytics, design) | [FILL] | [FILL] | [FILL] |
| AI tools and subscriptions | [FILL] | [FILL] | [FILL] |
| App store fees (if mobile) | [FILL] | [FILL] | [FILL: Apple and Google fees are set by them; check the current price] |
| Legal documents (Privacy Policy, Terms) | [FILL] | [FILL] | [FILL] |
| Paid ads | [FILL] | [FILL] | [FILL] |
| Freelancers or other help | [FILL] | [FILL] | [FILL] |
| Other | [FILL] | [FILL] | [FILL] |
| **Total** | [FILL] | [FILL] | |

**Q A5.2:** What is the most you will spend before you get your first 500 customers? [FILL: amount]

**Q A5.3:** What is the most you will pay to get **one** customer (your "cost per customer" limit)? [FILL: amount]

> 💡 Example: "I can spend 600 dollars in total. I will stop paid ads if one customer costs more than 8 dollars."

*Your monthly spending is tracked in Part 5.7.*

---

# Part 1: Discover and Plan

> **Goal of this part:** Know exactly who you are helping, what problem you are solving, and how you will know you succeeded.
> **Done when:** Every question in Part 1 is answered, and you can explain your product to a stranger in 30 seconds.

## 1.1 Your customer

**Q1.1.1:** Who is your ideal first customer? Describe **one real type of person**.

| Detail | Your answer |
|---|---|
| Job or role | [FILL: e.g. freelance designer] |
| Age range (optional) | [FILL: e.g. 25-40] |
| Country or region | [FILL: e.g. USA, Europe, worldwide] |
| How comfortable with technology | [FILL: Beginner / Average / Expert] |
| Where they spend time online | [FILL: e.g. LinkedIn, Reddit, YouTube] |

**Q1.1.2:** Who is NOT your customer? (This stops you from wasting time.)
Your answer: [FILL: one or two sentences]

> 💡 Example: "Not for professional botanists or plant shops. They need advanced tools."

**Q1.1.3:** Do you have more than one **type** of user (for example, a person who buys and a person who uses, or an admin and a normal user)?
- [ ] No, only one type
- [ ] Yes. List each type and what they need: [FILL]

> 💡 Why ask? Different user types often need different first steps. One flow for everyone can confuse people and delay their first win.

## 1.2 The problem

**Q1.2.1:** What is the biggest problem your customer has? Use their words, not yours.
Your answer: [FILL: "I am frustrated because ___."]

> 💡 Example: "I am frustrated because I water my plants too much or too little and they die."

**Q1.2.2:** How do they solve this problem today?
Your answer: [FILL: e.g. spreadsheets, a competitor, doing nothing]

> 💡 Example: "They search the internet for each plant, or just guess."

**Q1.2.3:** Why is that not good enough?
Your answer: [FILL: e.g. slow, expensive, confusing]

> 💡 Example: "The advice is scattered, and nothing reminds them at the right time."

**Q1.2.4:** How do you know this problem is real? (Pick all that apply and add details.)
- [ ] I talked to real people. How many? [FILL: number]
- [ ] I saw people complaining online. Where? [FILL: links or places]
- [ ] I have this problem myself
- [ ] I have not checked yet. ⚠️ Do the checking before you build more.

## 1.3 Your solution

**Q1.3.1:** In one sentence, how does your product solve the problem?
Your answer: [FILL: one sentence]

**Q1.3.2:** What are the **3 most important things** your product does? Do not list more than 3.

| # | Feature | Why customers care |
|---|---|---|
| 1 | [FILL: feature] | [FILL: benefit] |
| 2 | [FILL: feature] | [FILL: benefit] |
| 3 | [FILL: feature] | [FILL: benefit] |

> 💡 Example for the table: Feature = "Plant photo identification"; Benefit = "I instantly know what plant I have."

**Q1.3.3:** What will you **not** build before launch? (This protects your schedule.)
Your answer: [FILL: list at least 3 things you are saying "not yet" to]

> 💡 Example: "Social feed, plant shop, web version."

**Q1.3.4:** Who are your 3 closest competitors or alternatives?

| Competitor | What they do well | Where you are better |
|---|---|---|
| [FILL: name] | [FILL: strength] | [FILL: your advantage] |
| [FILL: name] | [FILL: strength] | [FILL: your advantage] |
| [FILL: name] | [FILL: strength] | [FILL: your advantage] |

## 1.4 Success numbers

**Q1.4.1:** Fill in your targets.

| Goal | Number | Date |
|---|---|---|
| People who join the waitlist before launch | [FILL: number] | [FILL: date] |
| Customers by end of launch month | [FILL: number] | [FILL: date] |
| Customers by 100 | [FILL: date] | |
| **Customers by 500** | **500** | [FILL: date] |

**Q1.4.2:** How much time and money can you spend each week?
- Hours per week: [FILL: number]
- Money per month (marketing and tools): [FILL: amount, or 0]

**Q1.4.3:** What is your **"aha moment"**? This is the first time a new user thinks "wow, this works." Describe it.
Your answer: [FILL: "When the user ___, they see that ___."]

> 💡 Example: "When the user uploads a photo and sees their plant identified in 5 seconds."
> ⚠️ This is your **activation event**. Pick one action a user can do and you can count. Many onboarding guides recommend getting new users to their first real value within minutes, not days. Treat that as a goal, not a rule.

**Q1.4.4:** How many minutes should it take from sign-up to the aha moment? [FILL: number]

> 💡 Example: "Under 5 minutes."

## 🤖 AI prompt for Part 1

```
Here is my project briefing: [paste Part A3].
Here are my Part 1 answers: [paste Part 1].
Please: (1) point out any answer that is vague, (2) list questions I should ask 10 real customers,
(3) tell me if my "aha moment" can be reached in under 5 minutes, (4) do NOT change my answers; only give suggestions.
```

✅ **Part 1 check**
- [ ] I can describe my customer in one sentence
- [ ] I have written my "aha moment"
- [ ] My targets contain real numbers and dates

---

# Part 2: Design the Onboarding Flow

> **Goal of this part:** Plan what a new user sees and does, from first hearing about you to their "aha moment" and beyond.
> **Done when:** You can draw the journey as a list of steps and each step has an owner, a message, and a success signal.

## 2.1 The user journey (the big picture)

> ⚠️ Design the journey around **first value**, not around "first login." Every step must help the user get closer to the aha moment. If a step does not, remove it or move it until later.

**Q2.1.1:** Fill in the journey. Each row is one step. Add rows if needed.

> 💡 Example row: Step "4. Set up" | User "chooses how many plants they own" | Feels "this is quick" | Could go wrong "too many questions, they quit" | Worked if "setup finished in under 1 minute."

| Step | What the user does | What they see or feel | What could go wrong | How you will know it worked |
|---|---|---|---|---|
| 1. Discover | [FILL: e.g. sees a post] | [FILL] | [FILL] | [FILL: e.g. clicks the link] |
| 2. Land | [FILL: opens website or app store page] | [FILL] | [FILL] | [FILL] |
| 3. Sign up | [FILL: creates an account] | [FILL] | [FILL] | [FILL] |
| 4. Set up | [FILL: first-time setup] | [FILL] | [FILL] | [FILL] |
| 5. First use | [FILL: tries the main feature] | [FILL] | [FILL] | [FILL] |
| 6. Aha moment | [FILL: from Q1.4.3] | [FILL] | [FILL] | [FILL] |
| 7. Come back | [FILL: returns on day 2, 7] | [FILL] | [FILL] | [FILL] |
| 8. Become a customer | [FILL: meets your A2.1 definition] | [FILL] | [FILL] | [FILL] |

**Q2.1.2:** If you listed more than one user type in Q1.1.3, does each type need a different path?
Your answer: [FILL: e.g. "Admins see team setup first; members see the main feature first" or "N/A - one user type"]

## 2.2 Sign-up and login

**Q2.2.1:** How can people create an account? (Tick all that apply.)
- [ ] Email and password
- [ ] Google
- [ ] Apple
- [ ] Magic link by email
- [ ] Phone number
- [ ] No account needed at first
- [ ] Other: [FILL]

**Q2.2.2:** What is the **minimum** information you must ask for at sign-up?
Your answer: [FILL: e.g. only an email]

⚠️ Every extra field makes fewer people finish. Ask for only what you truly need.

> 💡 Example: "Only an email. Name and plant details come later, after the first win."

**Q2.2.3:** Do users need to confirm their email before using the product?
Your answer: [FILL: Yes / No, and why]

> 💡 Example: "No. They can try the app first. I ask them to confirm their email before they save more than 3 plants."

## 2.3 First-time setup

**Q2.3.1:** What does the user have to set up before they get value? List each step.

| Setup step | Required or optional | Can it be skipped? | Time it takes |
|---|---|---|---|
| [FILL] | [FILL] | [FILL] | [FILL: seconds or minutes] |
| [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL] | [FILL] | [FILL] | [FILL] |

**Q2.3.2:** How many minutes from sign-up to the "aha moment" today? How many do you want?
- Now: [FILL: minutes or TBD]
- Target: [FILL: minutes]

**Q2.3.3:** How will you teach new users? (Tick all that apply.)
- [ ] Short welcome screens
- [ ] Interactive checklist
- [ ] Guided tour with highlights
- [ ] Sample data or a template already loaded
- [ ] Short video
- [ ] Help articles
- [ ] Live chat or email help
- [ ] Other: [FILL]

**Q2.3.4:** If you use an onboarding checklist, list **3 to 5 items only**. Each item must lead the user toward the aha moment.

| # | Checklist item | Why it matters |
|---|---|---|
| 1 | [FILL] | [FILL] |
| 2 | [FILL] | [FILL] |
| 3 | [FILL] | [FILL] |
| 4 | [FILL or "none"] | [FILL] |
| 5 | [FILL or "none"] | [FILL] |

> 💡 Example: 1. "Add your first plant." 2. "Photograph it." 3. "Turn on watering reminders."
> ⚠️ Do not put chores in the checklist that the user could do later or that you could fill in for them. Checklist items should be real use of the product, not just setup.

## 2.4 Messages sent to new users

**Q2.4.1:** Plan your first messages. Write the goal and the subject line for each.

| When | Channel | Goal of the message | Subject or headline |
|---|---|---|---|
| Right after sign-up | Email | Welcome and first action | [FILL] |
| 1 hour later if not set up | Email or push | Help them finish setup | [FILL] |
| Day 2 | Email | Show the main feature | [FILL] |
| Day 7 | Email | Ask for feedback | [FILL] |
| When inactive for 14 days | Email | Win them back | [FILL] |

> ⚠️ **Send messages because of what the user did, not only because of the clock.** If a user already reached the aha moment, do **not** send the "help you get started" message.
> 💡 Example subject lines: "Welcome to PlantPal! Add your first plant in 30 seconds." / "Need a hand with your first photo?"

**Q2.4.2:** Which messages are triggered by user behavior, and what is the rule?
Your answer: [FILL: e.g. "If no plant is added within 1 hour, send message 2. If a plant was added, skip it."]

## 2.5 Mobile and web differences

**Q2.5.1:** Does your product exist on web, mobile, or both?
Your answer: [FILL: Web / Mobile / Both]

If **mobile**, answer these:
- App store(s): [FILL: Apple App Store / Google Play / both]
- Who will submit the app and when (reviews can take days): [FILL: name, date]
- When do you ask for permissions (notifications, camera, location)? [FILL: at which step, and with what explanation]

  > 💡 Example: "I ask for camera access only when the user taps 'Photograph a plant', with the sentence: 'We use your camera to identify plants.'"

**Q2.5.2 (mobile only): App store readiness checklist.** The stores publish rules and change them often. Always check the current official guidelines before you submit.
- [ ] Developer accounts created and paid (Apple and/or Google). Owner: [FILL]
- [ ] If users can create an account, they can **delete it from inside the app**
- [ ] A privacy policy link is in the store listing **and** inside the app
- [ ] Store privacy answers (Apple's privacy labels, Google's Data Safety form) match what the app really collects
- [ ] A working **demo account** and review notes are ready for the store reviewers
- [ ] A support link or email works
- [ ] Screenshots, icon, and description are accurate (not advertising features you do not have yet)
- [ ] Google Play: if your account type requires testing before first release, the testing period is in my schedule
- [ ] I planned for **at least two submission rounds** in case of rejection
- Submit for review by: [FILL: date, at least 2 weeks before launch day]

If **web**, answer these:
- Browsers you will support: [FILL: e.g. Chrome, Safari, Edge]
- Does it work on a phone screen? [FILL: Yes / No / Partly]

## 2.6 Help when users are stuck

**Q2.6.1:** Where can a stuck user get help?
Your answer: [FILL: e.g. help@yourproduct.com, answered within 24 hours]

> 💡 Example: "A 'Help' button in the app opens an email to help@plantpal.example. I answer within 24 hours." 

**Q2.6.2:** What are the 5 questions new users will ask most?

| # | Question | Where will the answer live? |
|---|---|---|
| 1 | [FILL] | [FILL: help page, tooltip, email] |
| 2 | [FILL] | [FILL] |
| 3 | [FILL] | [FILL] |
| 4 | [FILL] | [FILL] |
| 5 | [FILL] | [FILL] |

## 2.7 Accessibility and languages

> **Beginner note:** Accessibility means people with different abilities can use your product (for example, people who cannot see well, cannot use a mouse, or cannot hear). It also helps everyone else. ⚠️ This section is general guidance. Check the current rules for your country and platform.

**Q2.7.1:** Which languages will you support?
- At launch: [FILL: e.g. English]
- Later (and when): [FILL: e.g. Spanish after 100 customers, or "none planned"]

**Q2.7.2:** Is your wording simple enough? Tick what is true.
- [ ] Buttons and messages use short, everyday words
- [ ] Error messages say what happened **and** what to do next
- [ ] Dates, times, and money show in a format your users expect: [FILL: e.g. "MM/DD/YYYY, USD"]

**Q2.7.3:** Accessibility checks. Tick what you have tested yourself.
- [ ] Text is easy to read against its background (strong contrast)
- [ ] Text can be made bigger without breaking the screen
- [ ] The whole sign-up and first-use flow works with a keyboard only (web)
- [ ] Buttons, images, and icons have text labels that a screen reader can read
- [ ] Nothing depends on color alone (for example, "red means error" also has a word or icon)
- [ ] Videos have captions
- [ ] I tried a screen reader (or the phone's built-in one) on the onboarding flow. Result: [FILL]

**Q2.7.4:** What is the biggest accessibility gap you know about, and when will you fix it?
Your answer: [FILL: or "none found, tested on DATE"]

> 💡 Example: "Plant photos have no text description. I will add labels before launch."

## 🤖 AI prompt for Part 2

```
Here is my project briefing: [paste Part A3].
Here is my onboarding journey: [paste Part 2.1 to 2.4].
Please: (1) find any step where a new user could get lost, (2) suggest ways to remove steps before the "aha moment",
(3) draft the 5 messages in 2.4 in plain, friendly English, (4) keep my product details exactly as I wrote them.
```

✅ **Part 2 check**
- [ ] Every step in the journey has a success signal
- [ ] I know how long it takes to reach the "aha moment"
- [ ] I have written all 5 new-user messages, or assigned them to someone with a date
- [ ] Accessibility checks in Q2.7.3 are done or scheduled

---

# Part 3: Build and Test (AI-Driven Development)

> **Goal of this part:** Build the product safely with AI help, and prove it works before real people use it.
> **Done when:** All "must have" items work, tests pass, and nobody needs to guess what "finished" means.

## 3.1 What you are building first (the smallest useful version)

**Q3.1.1:** List everything the first version must do. Use the 3 features from Q1.3.2 and add the onboarding steps from Part 2.

| # | Task | Who builds it | AI agent used | Due date | Status |
|---|---|---|---|---|---|
| 1 | [FILL] | [FILL: me / AI / other] | [FILL] | [FILL] | Not started / In progress / Done |
| 2 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| 3 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| 4 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| 5 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

## 3.2 How AI helps you build

**Q3.2.1:** Which jobs will AI agents do? Which jobs will you do yourself?

| Job | AI does it | I do it | I check the AI's work by |
|---|---|---|---|
| Write code | [ ] | [ ] | [FILL: e.g. running tests] |
| Write tests | [ ] | [ ] | [FILL] |
| Design screens | [ ] | [ ] | [FILL] |
| Write help articles and emails | [ ] | [ ] | [FILL] |
| Review code for mistakes | [ ] | [ ] | [FILL] |

**Q3.2.2:** Write 3 rules AI agents must follow when working on your product.
1. [FILL: e.g. "Never change the database without asking me."]
2. [FILL: e.g. "Always write a test for new code."]
3. [FILL: e.g. "Never store passwords in plain text."]

**Q3.2.3 (rules file for AI agents):** Keep one short file in your project (many teams call it `AGENTS.md`) that tells AI agents what the product is, how to run the tests, and the house rules. Update it every time an agent keeps making the same mistake.
- File location: [FILL: e.g. /AGENTS.md, or TBD with date]
- It includes: what the product is [ ], how to run and test it [ ], my 3 rules from Q3.2.2 [ ], "ask before risky actions" [ ]

**Q3.2.4 (the working loop):** For every task, the AI agent follows this loop. Tick what you agree to.
- [ ] **Explore:** the agent reads the code and my notes first
- [ ] **Plan:** the agent writes a plan **before** writing code, and I read the plan
- [ ] **Code:** the agent makes small changes I can review (not huge rewrites)
- [ ] **Verify:** the agent runs the tests and shows me the results
- [ ] **Approve:** I (a human) approve before anything is published

**Q3.2.5 (risky actions need a human):** Which actions must **always** wait for your approval?
- [ ] Changing or deleting the database
- [ ] Touching passwords, payments, or personal data
- [ ] Adding new software packages
- [ ] Publishing or deploying to real users
- [ ] Spending money
- [ ] Other: [FILL]

**Q3.2.6:** How will you mark changes made by AI, so you can find them later?
Your answer: [FILL: e.g. "Commit messages start with [AI]" or "Pull requests are labeled AI-assisted"]

> 💡 Why? If something breaks, you can quickly see which changes came from AI and review them first.

**Q3.2.7:** Where is your code stored, and do you have a backup?
Your answer: [FILL: e.g. GitHub, private repository, daily backup]

## 3.3 Testing: does everything work?

**Q3.3.1:** Test the whole onboarding journey from Part 2. Tick each box only after you personally tried it on a **new account**.

- [ ] I can sign up with every method I listed in Q2.2.1
- [ ] I got the confirmation email, and it did not land in spam
- [ ] I can finish first-time setup
- [ ] I can reach the "aha moment" in the target time from Q2.3.2
- [ ] Every message in 2.4 sends at the right time
- [ ] I can log out and back in
- [ ] "Forgot password" works
- [ ] I can delete my account (mobile apps with sign-up need this **inside the app**; for web, at least a working request to support)
- [ ] When I tapped "Help," I reached a real person or a real help page
- [ ] It works on the browsers or devices from Q2.5.1
- [ ] Error messages are in plain English (not codes)

**Q3.3.2:** Log the problems you found.

| # | Problem | How bad (High / Medium / Low) | Fixed? | Date fixed |
|---|---|---|---|---|
| 1 | [FILL or "None found"] | [FILL] | [ ] | [FILL] |
| 2 | [FILL] | [FILL] | [ ] | [FILL] |

⚠️ Do not launch with any **High** problem that is not fixed.

**Q3.3.3:** Get 3 to 5 outside testers. Who are they?

| Tester | How they will test | Got stuck at | Date |
|---|---|---|---|
| [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL] | [FILL] | [FILL] | [FILL] |

## 3.4 Safety, privacy, and legal basics

**Q3.4.1:** Tick everything that is true.
- [ ] Passwords are protected by a trusted login service or are encrypted
- [ ] The site uses HTTPS (the lock icon in the browser)
- [ ] Secret keys are not written in the code or in this file
- [ ] I have a Privacy Policy page
- [ ] I have Terms of Service
- [ ] I tell users what data I collect and why
- [ ] I have a cookie notice if my users are in places that require it
- [ ] I know what to do if user data leaks (see Part 6)

**Q3.4.2:** What personal data do you collect?
Your answer: [FILL: e.g. email, name. Write "none" if none]

**Q3.4.3 (where your users live):** Rules change by place. Tick every place where you expect real users.
- [ ] United States  - [ ] California  - [ ] European Union or UK  - [ ] Canada  - [ ] Other: [FILL]

> ⚠️ **Reminder list, not legal advice.** Founders often need to look up: GDPR (EU and UK), CCPA/CPRA (California), rules for marketing emails (for example CAN-SPAM in the US), and rules for children's data (for example COPPA in the US). Laws change. Confirm what applies to you.

**Q3.4.4 (marketing emails):** How do people agree to get emails from you?
- [ ] They tick a box or press a button that says so
- [ ] Every marketing email has a working "unsubscribe" link
- [ ] My email includes my real sender name and address
Your answer: [FILL: describe how consent is collected, or "no marketing emails"]

**Q3.4.5 (children):** Could anyone under 18 use your product?
- [ ] No. How do I make sure? [FILL: e.g. age question, terms]
- [ ] Yes. ⚠️ Special rules usually apply. Plan to get professional legal advice before launch. Owner and date: [FILL]

**Q3.4.6 (who else sees your users' data):** List every outside service that receives user data.

| Service | What data it gets | Is it named in my Privacy Policy? |
|---|---|---|
| [FILL: e.g. analytics tool] | [FILL] | [ ] |
| [FILL: e.g. email tool] | [FILL] | [ ] |
| [FILL: e.g. AI provider] | [FILL] | [ ] |

**Q3.4.7 (AI inside your product):** Does your product use AI that users talk to, or that creates content for them?
- [ ] No, N/A
- [ ] Yes. Users are clearly told when they are dealing with AI: [ ]
- [ ] Yes. I know what user data is sent to the AI provider: [FILL]
- [ ] Yes. I checked whether the provider may keep or learn from that data, and my Privacy Policy matches: [ ]
- [ ] Yes. A human can step in when the AI gives a wrong or harmful answer: [FILL: how]

**Q3.4.8 (user data rights):** How can a user ask to see, download, correct, or delete their data?
Your answer: [FILL: e.g. "Email privacy@yourproduct.com. I reply within 30 days."]
Who answers: [FILL]

**Q3.4.9 (who checked your legal pages):**
- [ ] A lawyer reviewed my Privacy Policy and Terms. Name and date: [FILL]
- [ ] I started from a trusted template and edited it to match what I really do
- [ ] Not reviewed yet. ⚠️ Owner and date: [FILL]

## 3.5 Measuring (set this up before launch)

**Q3.5.1:** Which tool will count your numbers?
Your answer: [FILL: e.g. Google Analytics, PostHog, Mixpanel, or a spreadsheet]

**Q3.5.2:** Which events will you track? Each one should match a step in Part 2.1.

| Event name | Triggered when | Working? |
|---|---|---|
| visited_site | A person opens the page | [ ] |
| signed_up | An account is created | [ ] |
| finished_setup | First-time setup is done | [ ] |
| reached_aha | The aha moment from Q1.4.3 happens | [ ] |
| returned_day_7 | They come back after 7 days | [ ] |
| became_customer | They meet the A2.1 definition | [ ] |

## 3.6 "Done" means done

**Q3.6.1:** Write your own definition of "ready to launch." It must be checkable (yes or no).
- [ ] [FILL: e.g. "All tasks in Q3.1.1 say Done"]
- [ ] [FILL: e.g. "No High problems open"]
- [ ] [FILL: e.g. "3 testers reached the aha moment without my help"]

## 3.7 Pricing and payments setup

> **Skip this section?** If your answer to A2.2 is "Free forever," write `N/A - free forever` on Q3.7.1 and move on.
> ⚠️ Never write card numbers, bank details, or secret payment keys in this file or in an AI prompt.

**Q3.7.1:** List your plans and prices.

| Plan name | Price | Billing (monthly / yearly / one-time) | What is included |
|---|---|---|---|
| [FILL: e.g. Free] | [FILL] | [FILL] | [FILL] |
| [FILL: e.g. Plus] | [FILL] | [FILL] | [FILL] |

**Q3.7.2:** Which tool takes the payments?
Your answer: [FILL: e.g. Stripe, Paddle, Apple and Google in-app billing]

> ⚠️ Mobile apps selling digital features often must use the store's own billing. Rules differ by store and country, and they change. Check the current store rules before choosing.

**Q3.7.3 (free trial or free plan rules):**
- Length of free trial: [FILL: days, or "no trial"]
- Is a card needed to start? [FILL: Yes / No]
- What happens when the trial ends? [FILL]
- Will users get a reminder before they are charged? [FILL: Yes / No, when]

**Q3.7.4 (taxes and business basics):**
- Who is the seller (business or person, and country)? [FILL]
- Who handles sales tax or VAT? [FILL: e.g. payment tool handles it, or accountant]
- Who do I ask if I am unsure? [FILL: name or TBD with date]

**Q3.7.5 (refunds and cancelling):**
- My refund policy in one sentence: [FILL]
- Users can cancel without contacting me: [ ] Yes [ ] No
- The policy is easy to find (at checkout and on the website): [ ]

**Q3.7.6:** Test the money flow in the payment tool's **test mode** before real customers. Tick each box.
- [ ] A test payment succeeds
- [ ] The customer gets a receipt or confirmation
- [ ] A failed payment shows a clear message and a way to retry
- [ ] Upgrading, downgrading, and cancelling work
- [ ] A refund can be issued
- [ ] The `became_customer` event (Q3.5.2) fires only after a real purchase, if "pays" is part of my customer definition

## 🤖 AI prompt for Part 3

```
Here is my project briefing: [paste Part A3].
Here are my Part 3 answers: [paste Part 3].
Please: (1) check that my test list covers every step in my onboarding journey, (2) list test cases I forgot,
(3) review my safety checklist and tell me what is missing for a [web / mobile] product, (4) never mark anything as done for me; tell me how I can check it myself.
```

✅ **Part 3 check**
- [ ] The full journey works on a brand-new account
- [ ] No High problems remain
- [ ] Tracking works for every event in Q3.5.2
- [ ] My "ready to launch" list is fully ticked
- [ ] Legal items in Q3.4.3 to Q3.4.9 are answered or have an owner and date
- [ ] Payments tested in test mode (Q3.7.6), or N/A

---

# Part 4: Pre-Launch and Launch

> **Goal of this part:** Get people waiting for you, then open the doors on a planned day.
> **Done when:** Launch day is on the calendar, every channel has a message, and someone owns every task.

## 4.1 Your launch message

**Q4.1.1:** Fill in the blanks.
- **Headline (under 10 words):** [FILL]
- **One sentence explaining the product:** [FILL: copy from A1]
- **Three benefits (not features):** 1. [FILL] 2. [FILL] 3. [FILL]
- **The one action you want people to take:** [FILL: e.g. "Join the free beta"]

## 4.2 Pre-launch checklist (4 weeks before)

| When | Task | Owner | Done |
|---|---|---|---|
| 4 weeks before | Landing page live with a sign-up form | [FILL] | [ ] |
| 4 weeks before | Welcome email for the waitlist ready | [FILL] | [ ] |
| 3 weeks before | Post about the product 2 or 3 times a week | [FILL] | [ ] |
| 3 weeks before | Reach out to 20 people who match your customer | [FILL] | [ ] |
| 2 weeks before | Invite the first beta users | [FILL] | [ ] |
| 2 weeks before | Collect and fix beta feedback | [FILL] | [ ] |
| 2 weeks before | **Mobile only:** app submitted for store review (see Q2.5.2) | [FILL] | [ ] |
| 1 week before | Final test of the full journey (Part 3.3) | [FILL] | [ ] |
| 1 week before | Prepare all launch posts and emails | [FILL] | [ ] |
| 1 day before | Tell the waitlist the launch time | [FILL] | [ ] |

## 4.3 Plan your channels

**Q4.3.1:** Tick the channels you will really use. **Choose 2 to 4. Doing everything badly is worse than doing a few well.**

| Channel | Use it? | What you will do | Posts or actions per week | Owner | Goal (sign-ups) |
|---|---|---|---|---|---|
| Waitlist and email | [ ] | [FILL] | [FILL] | [FILL] | [FILL] |
| Social and content (X, LinkedIn, YouTube, blog) | [ ] | [FILL] | [FILL] | [FILL] | [FILL] |
| Communities and launch sites (Product Hunt, Reddit, Discord, Hacker News) | [ ] | [FILL] | [FILL] | [FILL] | [FILL] |
| Direct outreach (emails, messages, partnerships) | [ ] | [FILL] | [FILL] | [FILL] | [FILL] |
| Paid ads | [ ] | [FILL] | [FILL] | [FILL] | [FILL] |
| Other | [ ] | [FILL] | [FILL] | [FILL] | [FILL] |

⚠️ Read each community's rules before you post. Many ban self-promotion.

**Q4.3.2:** If you use paid ads, how much will you spend, and what is the most you will pay for one sign-up?
Your answer: [FILL: amount, or "no paid ads"]

**Q4.3.3 (only if you chose a launch site such as Product Hunt):**
- Launch site: [FILL]
- Launch date and time: [FILL]
  - 💡 Product Hunt launch days start at 12:01 am Pacific Time. Many guides suggest Tuesday to Thursday, but Product Hunt's own guide says the best day is the day you are most prepared.
- My first comment (who it is for, why I built it, what feedback I want): [FILL]
- I will be online and answer every comment on launch day: [ ] Yes
- ⚠️ Do **not** ask people directly for upvotes. Product Hunt's community rules discourage it. Ask for **feedback** instead.
- ⚠️ Never use fake accounts, fake reviews, or paid votes.

**Q4.3.4:** How will you turn launch-day visitors into a lasting audience?
Your answer: [FILL: e.g. "Every visitor is invited to my email list and a small Discord."]

## 4.4 Launch day plan

**Q4.4.1:** Launch day: [FILL: YYYY-MM-DD], at [FILL: time and time zone]

| Time | Action | Owner |
|---|---|---|
| [FILL] | Switch the product on for everyone | [FILL] |
| [FILL] | Email the waitlist | [FILL] |
| [FILL] | Post on every chosen channel | [FILL] |
| [FILL] | Watch for errors every hour | [FILL] |
| [FILL] | Answer every comment and message | [FILL] |
| [FILL] | Write down the numbers at the end of the day | [FILL] |

## 4.5 The first 7 days after launch

**Q4.5.1:** What will you do each day?

| Day | Action |
|---|---|
| Day 1 | [FILL: e.g. personally welcome every new user] |
| Day 2 | [FILL] |
| Day 3 | [FILL] |
| Day 4 | [FILL] |
| Day 5 | [FILL] |
| Day 6 | [FILL] |
| Day 7 | [FILL: review numbers, decide what to fix first] |

## 🤖 AI prompt for Part 4

```
Here is my project briefing: [paste Part A3].
Here are my launch answers: [paste Part 4].
Please: (1) draft a landing page headline and 3 alternatives, (2) draft one post per chosen channel in a different style,
(3) check my pre-launch checklist for missing tasks, (4) warn me about the rules of each community I picked. Do not post anything for me.
```

✅ **Part 4 check**
- [ ] Launch day and time are decided
- [ ] I have chosen 2 to 4 channels, with an owner for each
- [ ] The launch message is written
- [ ] The first 7 days after launch are planned

---

# Part 5: Growth to 500 Customers

> **Goal of this part:** Reach your first 500 customers in clear steps, and learn from each step.
> **Done when:** You have a target, a plan, and a review habit for every milestone.

## 5.1 Milestone map

**Q5.1.1:** Set your date for each milestone and decide what you will focus on.

| Milestone | Target date | Main focus | How you will get these customers |
|---|---|---|---|
| 1 to 10 customers | [FILL] | Learn, do things by hand, talk to every user | [FILL: e.g. personal outreach] |
| 11 to 50 customers | [FILL] | Fix onboarding problems | [FILL] |
| 51 to 100 customers | [FILL] | Find the channel that works best | [FILL] |
| 101 to 250 customers | [FILL] | Repeat what works, automate small tasks | [FILL] |
| 251 to 500 customers | [FILL] | Grow steadily, improve retention | [FILL] |

## 5.2 The funnel numbers (AARRR)

> **Beginner note:** A funnel counts people at each stage. Fewer people reach each next stage. Your job is to lose fewer of them.

**Q5.2.1:** Set your targets for each stage. Write today's real number when you have it.

| Stage | Question it answers | What you count | Target | Real number |
|---|---|---|---|---|
| **Acquisition** | How many people find me? | Visitors or installs | [FILL] | [FILL] |
| **Activation** | How many reach the "aha moment"? | % of sign-ups who reach it | [FILL: %] | [FILL] |
| **Retention** | How many come back? | % active on day 7 and day 30 | [FILL: %] | [FILL] |
| **Referral** | How many tell others? | Invites sent or friends referred | [FILL] | [FILL] |
| **Revenue** | How many pay (if you charge)? | Paying customers and money per month | [FILL] | [FILL] |

**Q5.2.2:** Which stage is your biggest worry right now?
Your answer: [FILL: Acquisition / Activation / Retention / Referral / Revenue, and why]

> 💡 Rule of thumb: fix **activation** before spending more on **acquisition**. Bringing more people into a leaky funnel wastes effort.
> ⚠️ Reference points only: one 2024 analysis of 62 B2B SaaS companies reported average activation near 37.5 percent, and many guides suggest first value within minutes. Your product and audience may differ. Use these only to sanity-check your targets, and trust your own numbers once you have them.

## 5.3 Weekly review (do this every week)

**Q5.3.1:** Set a fixed time: every [FILL: day] at [FILL: time], for [FILL: 30] minutes.

Copy this table once per week.

| Week of | Visitors | Sign-ups | Reached aha | Active on day 7 | Paying | Customers total |
|---|---|---|---|---|---|---|
| [FILL: date] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL: date] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL: date] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

**Each week answer these 4 questions:**
1. What went better than expected? [FILL]
2. What went worse than expected? [FILL]
3. Where do new users get stuck? [FILL]
4. What is the **one** thing I will change next week? [FILL]

## 5.4 Learning from customers

**Q5.4.1:** How will you collect feedback?
- [ ] A short survey after the "aha moment"
- [ ] A question in the Day 7 email
- [ ] 15-minute calls with [FILL: number] customers per week
- [ ] A feedback button inside the product
- [ ] Other: [FILL]

**Q5.4.2:** What will you ask every new customer?
1. [FILL: e.g. "What almost stopped you from signing up?"]
2. [FILL: e.g. "What do you use this for?"]
3. [FILL: e.g. "What is one thing we should fix?"]

**Q5.4.3:** How will you ask happy customers to bring others (reviews, referrals, sharing)?
Your answer: [FILL]

## 5.5 Decision rules (so you never have to guess)

**Q5.5.1:** Write your own rules. Each rule has an "if" and a "then".

| If this happens | Then I will |
|---|---|
| Fewer than [FILL: %] of sign-ups reach the aha moment | [FILL: e.g. watch 5 new users and fix the biggest block] |
| Fewer than [FILL: %] come back on day 7 | [FILL] |
| A channel gives fewer than [FILL: number] sign-ups in [FILL: weeks] | [FILL: e.g. stop and move time to the best channel] |
| More than [FILL: number] support questions are about the same thing | [FILL: e.g. change the product or write a help article] |
| I reach 500 customers | [FILL: e.g. review this document and write the next plan] |

## 5.6 Celebrate and record

**Q5.6.1:** When you reach each milestone, write the date and one lesson.

| Milestone | Date reached | Biggest lesson |
|---|---|---|
| 10 customers | [FILL] | [FILL] |
| 50 customers | [FILL] | [FILL] |
| 100 customers | [FILL] | [FILL] |
| 250 customers | [FILL] | [FILL] |
| 500 customers | [FILL] | [FILL] |

## 5.7 Budget tracker (update every month)

> **How to use:** Add one row per month. **Cost per customer = money spent ÷ new customers.** Compare it with your limit from A5.3.
> 💡 Example: spent 120, got 30 new customers, so 120 ÷ 30 = 4 per customer.

| Month | Planned spend | Actual spend | New customers | Cost per customer | Over my A5.3 limit? |
|---|---|---|---|---|---|
| [FILL: YYYY-MM] | [FILL] | [FILL] | [FILL] | [FILL] | [ ] Yes [ ] No |
| [FILL: YYYY-MM] | [FILL] | [FILL] | [FILL] | [FILL] | [ ] Yes [ ] No |
| [FILL: YYYY-MM] | [FILL] | [FILL] | [FILL] | [FILL] | [ ] Yes [ ] No |

**Q5.7.1:** What will you do if you are over the limit two months in a row?
Your answer: [FILL: e.g. "Pause paid ads and move the money into talking to customers."]

## 🤖 AI prompt for Part 5

```
Here is my project briefing: [paste Part A3].
Here is my growth plan and weekly numbers: [paste Part 5].
Please: (1) tell me which funnel stage is weakest using my numbers, (2) give 3 small experiments to try this week,
(3) write 5 questions for customer calls, (4) never invent numbers; if data is missing, ask me for it.
```

✅ **Part 5 check**
- [ ] Every milestone has a date and a focus
- [ ] All 5 funnel stages have a target
- [ ] The weekly review is in my calendar
- [ ] I wrote my decision rules
- [ ] I update the budget tracker every month

---

# Part 6: Risks and Fallback Plan

> **Goal of this part:** Decide what to do before something goes wrong, so you do not panic later.

## 6.1 What could go wrong?

**Q6.1.1:** Fill in each row. The first rows are examples to keep. Add your own below them.

| Risk | How likely (Low / Medium / High) | What would happen | What I will do (fallback) | Who does it |
|---|---|---|---|---|
| Few people sign up | [FILL] | Slow growth | [FILL: e.g. talk to 10 people, change the message, try another channel] | [FILL] |
| People sign up but leave quickly | [FILL] | Weak activation | [FILL: e.g. watch 5 sessions, shorten setup] | [FILL] |
| The product crashes on launch day | [FILL] | Bad first impression | [FILL: e.g. status message, rollback to last working version] | [FILL] |
| Too many users at once | [FILL] | Slow or down | [FILL: e.g. pause the invites, add server capacity] | [FILL] |
| An AI agent makes a harmful change | [FILL] | Broken or insecure product | [FILL: e.g. restore from backup, review all changes first] | [FILL] |
| User data is exposed | [FILL] | Legal and trust problems | [FILL: e.g. lock access, tell users, get legal advice] | [FILL] |
| I run out of time or money | [FILL] | Project stops | [FILL: e.g. cut scope, pause paid ads] | [FILL] |
| [FILL: your own risk] | [FILL] | [FILL] | [FILL] | [FILL] |

## 6.2 Emergency contacts

**Q6.2.1:** Who can you contact if there is an emergency?

| For | Name | How to reach them |
|---|---|---|
| Server or hosting problem | [FILL] | [FILL] |
| Legal or privacy question | [FILL] | [FILL] |
| Money or payment problem | [FILL] | [FILL] |
| Backup person if I am unavailable | [FILL] | [FILL] |

## 6.3 Stop and rethink rule

**Q6.3.1:** After [FILL: number] weeks, if I have fewer than [FILL: number] customers, I will [FILL: e.g. pause building, interview 15 people, decide whether to change direction].

---

# Part 7: Filled Example (read only)

> **Do not copy these answers.** They are here so you can see what good answers look like. The fictional product is **PlantPal**.

## Example Part A and Part 1

| Question | Example answer |
|---|---|
| Product | PlantPal, a mobile app |
| One sentence | "It helps new plant owners keep their plants alive by telling them when and how to water." |
| Customer definition (A2.1) | "Someone who added at least one plant and turned on watering reminders." |
| Business model (A2.2) | Free plan plus paid plan at 3 dollars a month |
| Ideal customer (Q1.1.1) | City apartment dwellers, 22 to 35, beginner gardeners, on Instagram and TikTok |
| Problem (Q1.2.1) | "I keep killing my plants and I don't know why." |
| Aha moment (Q1.4.3) | "When the user photographs a plant and instantly sees its name and a watering schedule." |
| Not building yet (Q1.3.3) | Social features, plant shop, web version |

## Example Part 2 journey (shortened)

| Step | What the user does | Success signal |
|---|---|---|
| Discover | Sees a short plant-care video | Taps the link in the bio |
| Sign up | Signs in with Apple | Account created in under 20 seconds |
| Set up | Chooses how many plants they own | Setup finished in under 1 minute |
| Aha | Photographs a plant | Plant identified and schedule shown |
| Come back | Gets a "time to water" notification | Opens the app on day 2 |
| Customer | Adds a plant and turns on reminders | `became_customer` event recorded |

## Example Part A roles and budget

- **RACI (solo founder):** Owner = **A** on every row. AI agent = **R** on "Write launch posts and emails." Owner = **R and A** on "Say ready to launch."
- **Budget:** 600 dollars total for the first 500 customers. Cost-per-customer limit: 8 dollars.
- **Decision Log row:** D-001, "Launch on iPhone first," because most interviewed customers use iPhone.

## Example Part 4 channels

- **Chosen:** Waitlist and email, short videos, one Reddit community (after reading its rules).
- **Not chosen:** Paid ads (no budget), Hacker News (audience does not fit).

## Example Part 5 milestone and decision rule

- 1 to 10 customers by 2 weeks after launch, found by messaging 30 plant lovers directly.
- Rule: "If fewer than 40 percent of sign-ups add a plant, I will watch 5 new users and shorten setup."

---

# Part 8: Glossary (plain English)

| Word | What it means |
|---|---|
| **Onboarding** | Everything that helps a new user get from "I just signed up" to "this is useful" |
| **Activation** | The moment a new user reaches the "aha moment" |
| **Aha moment** | The first time the user clearly sees the product's value |
| **Retention** | How many users come back after their first visit |
| **Churn** | Users who leave and stop using the product |
| **Funnel** | The steps people go through, with fewer people at each step |
| **AARRR** | Acquisition, Activation, Retention, Referral, Revenue: five stages to measure |
| **Acquisition** | How people find your product |
| **Referral** | When one customer tells others |
| **Waitlist** | A list of people who asked to hear when you launch |
| **Beta** | An early version given to a small group to test |
| **MVP** | "Minimum viable product": the smallest version that is still useful |
| **Landing page** | The web page whose only job is to make visitors take one action |
| **Conversion** | A person doing the action you wanted (sign up, pay) |
| **ICP** | "Ideal customer profile": a description of your best-fit customer |
| **Freemium** | Free plan with optional paid upgrades |
| **Analytics** | Tools that count what people do in your product |
| **Event** | One action that analytics records, like "signed_up" |
| **AI agent** | An AI tool that can do multi-step tasks for you, like writing code or drafting plans |
| **Prompt** | The instructions you give to an AI |
| **Rollback** | Going back to the last working version |
| **HTTPS** | The secure connection shown as a lock in the browser |
| **Privacy Policy** | A page that tells users what data you collect and why |
| **Support ticket** | A question or problem sent to you by a user |
| **KPI** | A number you watch to know if you are succeeding |
| **Activation event** | The one countable action that shows a user got real value |
| **Time to value** | How long it takes a new user to reach the aha moment |
| **RACI** | A table showing who is Responsible, Accountable, Consulted, and Informed for each job |
| **AGENTS.md** | A short file that tells AI agents the rules and how to work on your project |
| **Decision log** | A diary of big choices and why you made them |
| **Cost per customer** | Money spent divided by new customers gained |
| **Accessibility** | Making the product usable by people with different abilities |
| **Screen reader** | Software that reads the screen out loud for people who cannot see it well |
| **GDPR** | A European privacy law about how personal data is collected and used |
| **CCPA/CPRA** | California privacy laws about personal data |
| **Test mode** | A safe mode in a payment tool where no real money moves |
| **Refund policy** | The rules for when you give money back |

---

# Part 9: Completeness Checklist (do this before you start building or launching)

> **Rule:** Every box must be ticked. If a box cannot be ticked, write why in the notes column.

## Document quality

| Check | Done | Notes |
|---|---|---|
| I filled in a **copy** with a project code, not the master | [ ] | |
| Searching for `[FILL:` finds nothing | [ ] | |
| Every `[TBD` names a person and a date | [ ] | |
| Every `N/A` has a reason | [ ] | |
| Customer definition (A2.1) is one clear sentence | [ ] | |
| All numbers have dates | [ ] | |
| Nobody reading this needs to ask "what did you mean?" | [ ] | |

## Plan quality

| Check | Done | Notes |
|---|---|---|
| I can describe my customer in one sentence | [ ] | |
| The "aha moment" is reachable in the target time | [ ] | |
| Each onboarding step has a success signal | [ ] | |
| Tracking events are working | [ ] | |
| Privacy Policy and Terms exist, and I know who reviewed them (Q3.4.9) | [ ] | |
| Third-party services that get user data are listed in my Privacy Policy (Q3.4.6) | [ ] | |
| Accessibility checks done (Q2.7.3) | [ ] | |
| Pricing, trial, and refund rules are written (Q3.7), or marked N/A | [ ] | |
| 2 to 4 channels are chosen, each with an owner | [ ] | |
| Launch day and time are in the calendar | [ ] | |
| All 5 funnel stages have targets | [ ] | |
| Weekly review is in the calendar | [ ] | |
| Fallback plan exists for the top 5 risks | [ ] | |
| Every RACI row has exactly one A | [ ] | |
| Budget limits (A5.2, A5.3) are written | [ ] | |
| Big choices are in the Decision Log (Part 10) | [ ] | |

## AI workflow quality

| Check | Done | Notes |
|---|---|---|
| The Part A3 briefing is accurate and current | [ ] | |
| AI rules (Q3.2.2) are written | [ ] | |
| The AI rules file exists and is current (Q3.2.3) | [ ] | |
| Risky actions need my approval (Q3.2.5) | [ ] | |
| A human reviews every AI-written message before it is sent | [ ] | |
| No secrets or private customer data were pasted into AI tools | [ ] | |

## Final sign-off

- Reviewed by: [FILL: name]
- Date: [FILL: YYYY-MM-DD]
- Decision: [FILL: Ready to build / Ready to launch / Needs more work]

---

# Part 10: Decision Log

> **Beginner note:** A decision log is a diary of big choices. Write one row each time you make a choice you do not want to forget or argue about later. AI agents and teammates read it so they never have to guess why something is the way it is.
> **Rule:** If this log and an older answer in the file disagree, **the log wins**. Then go back and fix the older answer.

**Which decisions must be logged? (tick what applies to you)**
- [ ] Who the customer is, or what counts as a customer
- [ ] Features cut or added
- [ ] A channel started or stopped
- [ ] Price or business model changes
- [ ] A new launch date
- [ ] A platform added or dropped (web, iPhone, Android)
- [ ] A risky action you approved for an AI agent (see Q3.2.5)

| ID | Date | Decision | Why | Options I rejected | Decided by | Review again on |
|---|---|---|---|---|---|---|
| D-001 | 2026-01-10 | *(Example)* Launch on iPhone first | Most customers I interviewed use iPhone | Android first; both at once | Me | After 100 customers |
| D-002 | [FILL: date] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| D-003 | | | | | | |
| D-004 | | | | | | |

---

# Part 11: Change Log

> Add one row each time you change this document in a meaningful way.

| Version | Date | What changed | Who changed it |
|---|---|---|---|
| 1.0 | [FILL: date] | First version filled in | [FILL: name] |
| | | | |
| | | | |

---

# Appendix: Sources Used for This Template

> Checked on 2026-10-18. Rules of stores and sites change, so always check the current official pages before you act. Figures quoted from these sources are reference points, not promises.
>
> **Not researched this round:** Sections 2.7 (accessibility), 3.4.3 to 3.4.9 (legal), and 3.7 (payments) are general guidance, not checked against current laws or store policies. They are reminders to look things up, not legal or tax advice. Check them with official sources or a professional before launch.

| Topic | What it informed | Source |
|---|---|---|
| Onboarding: define the activation event first, measure time to value | Parts A2, 1.4, 2 | https://www.guideflow.com/et-ee/blog/user-onboarding-best-practices |
| Onboarding: 3 to 5 item checklists, separate flows for different users | Q1.1.3, Q2.1.2, Q2.3.4 | https://www.saashero.net/design/saas-onboarding-ux-best-practices/ |
| Onboarding: behavior-triggered messages, activation reference points | Q2.4, Part 5.2 | https://fungies.io/?p=40371 |
| Product Hunt official launch guide | Q4.3.3 | https://www.producthunt.com/protips |
| Product Hunt launch checklists (no direct upvote requests, first comment) | Q4.3.3 | https://zeda.io/blog/producthunt-launch-guide-checklist |
| Turning launch visitors into an email or community loop | Q4.3.4 | https://www.under30ceo.com/guide-to-launching-on-product-hunt/ |
| AI agent workflow (explore, plan, code, verify; AGENTS.md; human approval for risky actions) | Q3.2.3 to Q3.2.5 | https://docs.factory.ai/agent-driven-development |
| Tagging AI-assisted changes, shared instruction files | Q3.2.6 | https://jellyfish.co/?p=35649 |
| App store requirements (account deletion, privacy policy, demo account) | Q2.5.2 | https://techsy.io/en/blog/mobile-app-checklist-for-startups and https://bilt.me/blog/how-to-never-get-rejected-by-app-store-review |
| Google Play first-release testing; planning for more than one submission | Q2.5.2 | https://adapty.io/docs/prepare-your-app-for-store-review and https://forasoft.com/blog/article/how-to-get-you-app-approved-on-google-play-and-app-store |
| Frameworks used | AARRR funnel (Part 5.2), RACI (A4) | Widely used product and project-management methods |
