# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What is this?**
This is a "brain dump" form. It lets anyone take over this project and understand it without calling you. Think of it as a **moving-day box label**: you write what is inside, where it lives, and how to open it.

**Who is it for?** Solo founders and small teams. If you can answer a question in plain words, you can fill this in. No technical background is needed to read it, and every technical word is explained in the Glossary (Section 17).

## The 7 rules

1. **Answer every question.** Never leave a blank. Use one of these instead:
   - `N/A` = does not apply to this project (add a short reason).
   - `UNKNOWN` = nobody knows yet (add who will find out, and by when).
   - `TODO` = known but not written yet (add an owner and a date).
2. **Write in short, plain sentences.** If a 10-year-old could not follow it, simplify it.
3. **Never paste secrets here.** No passwords, API keys, tokens or card numbers. Write only *where* the secret is stored (for example: "1Password vault: Project-X").
4. **Give links, not descriptions.** If something exists elsewhere (a repo, a design, a dashboard), paste the link and one sentence on what it is.
5. **Give examples with real values** (names, numbers, dates), not "various" or "etc."
6. **Mark confidence** on important answers: ✅ Sure | 🟡 Probably | ❌ Guess.
7. **Update the Change Log (Section 18)** every time you edit this file.

## How to use the tags
- **[REQUIRED]** = must be filled for every project.
- **[OPTIONAL]** = fill if it applies; otherwise write `N/A` and a reason.
- **[AI]** = about AI tools, AI agents or AI inside the product.
- **Example:** lines are there to show you the style. Delete them when you fill in your own answers.

## Who answers? (the "Who answers" column)
Each question names the person best placed to answer it. If your team is small, one person can wear several hats.
| Role | Answers about |
|---|---|
| Founder | Why, scope, money, launch, people |
| Developer | Tech, code, access, deployment, operations |
| AI lead | AI tools, prompts, agents, AI inside the product |
| QA | Testing and quality |
| Marketer | Customers, brand, channels, sales |
| Legal / Finance | Contracts, ownership, compliance, taxes |

## Want an AI to fill this in for you? (optional shortcut)
Copy this block into your AI tool together with this file:

> You are my documentation interviewer. Fill in `Technical_Knowledge_Transfer.md` with me. Rules: (1) Work on ONE section at a time, starting at Section 0. (2) Ask me ONE question at a time in plain words, and wait for my answer. (3) If my answer is vague, ask a follow-up for a real name, number, date or link. (4) Never write or ask for passwords or API keys; ask only where they are stored. (5) If I don't know, mark it `UNKNOWN` with an owner and date. (6) After each section, show me what you wrote and ask "Is this correct?" before moving on. (7) At the end, list every `TODO` and `UNKNOWN`, and calculate the completeness percent.

## Which phase is my project in? (fill only the sections you need today)
| Your project is... | Fill these sections |
|---|---|
| Just an idea | 0, 1, 2 |
| Being built | 0 to 7, 12 |
| About to launch | 0 to 11, 12, 13 |
| Live, going for 500 customers | All sections |
| Being handed to someone else | All sections, then Section 16 |

## AI-READY SUMMARY (fill LAST, keep under 15 lines; an AI reads this first)
```
PROJECT: <name> | TYPE: <web/mobile/other> | PHASE: <phase> | UPDATED: <date>
WHAT IT IS: <one sentence from 0.2>
CUSTOMER: <one sentence from 1.2>
STACK: <language, framework, database, hosting>
REPO / MAIN LINKS: <repo, board, dashboard>
HOW TO RUN LOCALLY: <see 6.7>
HOW TO DEPLOY / ROLL BACK: <see 6.4 and 6.5>
AI RULES FILE: <see 4.3>   AI MUST NEVER: <see 4.7>
CURRENT GOAL: <e.g. "reach 100 customers by 2027-01-31">
CUSTOMERS NOW / TARGET: <n> / 500
TOP 3 RISKS: <1> <2> <3>
OPEN TODO/UNKNOWN COUNT: <n>
CONTACT: <owner and backup>
```

## Document status (update at the top every time)
| Field | Answer |
|---|---|
| Document version | v0.1 |
| Last updated (YYYY-MM-DD) | |
| Updated by | |
| Overall completeness | ___ % (count the answered questions, divide by the total) |
| Ready for handover? | ☐ Yes ☐ No (see Section 16 checklist) |

---

# 0. PROJECT IDENTITY [REQUIRED]
*Goal: anyone opening this file knows what this project is in 60 seconds.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 0.1 | Project name (and any old or code names)? | Founder | |
| 0.2 | One-sentence description. Finish this: "This is a ___ that helps ___ do ___." | Founder | |
| 0.3 | Product type? ☐ Web app/SaaS ☐ Mobile app (iOS/Android) ☐ Other: ___ | Founder | |
| 0.4 | Does it use AI inside the product? ☐ Yes ☐ No | Founder | |
| 0.5 | Current phase? ☐ Idea ☐ Building ☐ Testing ☐ Launched ☐ Growing to 500 customers ☐ Maintenance | Founder | |
| 0.6 | Project owner (name, contact)? | Founder | |
| 0.7 | Backup person who can answer questions? | Founder | |
| 0.8 | Start date and target launch date? | Founder | |
| 0.9 | Link to the main folder, repo, or board? | Founder | |
| 0.10 | Where do you officially talk about this project? (Slack, Discord, email list) | Founder | |

---

# 1. THE "WHY": PROBLEM, CUSTOMER, VISION [REQUIRED]
*Goal: explain why this project exists so nobody rebuilds the wrong thing.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 1.1 | What problem are we solving? (1 to 3 sentences) | Founder | |
| 1.2 | Who has this problem? Describe one real, specific person. (Example: "Maria, 34, runs a small bakery, hates doing invoices.") | Founder | |
| 1.3 | How do they solve it today without us? | Founder | |
| 1.4 | Why is our solution better? (Top 3 reasons) | Founder | |
| 1.5 | What does success look like in 12 months? (Use numbers) | Founder | |
| 1.6 | What will we NEVER build? (Anti-goals) | Founder | |
| 1.7 | Who are our top 3 competitors? What do they do better than us? | Founder | |
| 1.8 | Evidence people want this (interviews, waitlist, surveys). Paste links. | Founder | |

---

# 2. SCOPE & REQUIREMENTS [REQUIRED]
*Goal: a clear list of what is in, what is out, and what "done" means.*

## 2A. Feature list
Fill one row per feature. Priority: **P0** = launch cannot happen without it, **P1** = important, **P2** = nice to have.

| Feature | What it does (plain words) | Priority | Status (Not started / Building / Done) | Link to spec or design |
|---|---|---|---|---|
| Example: Sign up | A user creates an account with email | P0 | Done | |
| | | | | |

## 2B. Scope questions
| # | Question | Who answers | Your answer |
|---|---|---|---|
| 2.1 | What is the smallest version we can launch (MVP)? List the features. | Founder | |
| 2.2 | What is explicitly out of scope for launch? | Founder | |
| 2.3 | Rules the product must follow (laws, privacy, age limits, accessibility)? | Founder | |
| 2.4 | Performance promises (example: "page loads in under 3 seconds")? | Founder | |
| 2.5 | What assumptions are we making that could be wrong? | Founder | |
| 2.6 | Definition of Done: what must be true before we call a feature finished? | Founder | |

## 2C. Pre-development planning (budget, team, timeline)
| # | Question | Who answers | Your answer |
|---|---|---|---|
| 2.7 | Total budget for building and launching? Who approves changes to it? | Founder | |
| 2.8 | Budget until the first 500 customers? (Build, tools, AI usage, marketing, legal, support) | Founder | |
| 2.9 | Who is on the team now? Which skills are missing, and how will we fill them? (Hire, freelancer, AI) | Founder | |
| 2.10 | Build or buy: which parts do we build ourselves and which do we buy or use ready-made? Why? | Founder | |
| 2.11 | Timeline: list the main milestones with dates (Plan done, MVP built, Beta, Launch, 100 customers, 500 customers). | Founder | |
| 2.12 | What could delay us most? What is the backup plan? | Founder | |
| 2.13 | How much time per week can each person give? | Founder | |
| 2.14 | How do we decide to continue, change direction, or stop? (Example: "if fewer than 20 sign-ups after 60 days, we rethink") | Founder | |
| 2.15 | Who are the stakeholders (people who care about the result) and how often do we update them? | Founder | |

---

# 3. ARCHITECTURE & TECH STACK [REQUIRED]
*Goal: a map of how the pieces fit together. "If I were new, where would I look first?"*

## 3A. Tech stack
| Layer | What we use | Version | Why we chose it | Who knows it best |
|---|---|---|---|---|
| Programming language(s) | | | | |
| Front end (what users see) | | | | |
| Back end (the "engine") | | | | |
| Database | | | | |
| Hosting / cloud | | | | |
| Login / authentication | | | | |
| Payments | | | | |
| Email / notifications | | | | |
| Analytics | | | | |
| Mobile framework [OPTIONAL] | | | | |

## 3B. Architecture questions
| # | Question | Who answers | Your answer |
|---|---|---|---|
| 3.1 | Paste or link an architecture diagram. (No diagram? Describe the flow: "User clicks → website → server → database → back to user.") | Developer | |
| 3.2 | What are the main parts (services/modules) and what does each do? | Developer | |
| 3.3 | Which third-party services do we depend on? (Name, what for, monthly cost, what breaks if it goes down) | Developer | |
| 3.4 | Where is the code? (Repo links, branch rules, main branch name) | Developer | |
| 3.5 | How is the code organized? (List the top-level folders and what each holds) | Developer | |
| 3.6 | What shortcuts or hacks exist (technical debt)? Which ones are dangerous? | Developer | |
| 3.7 | Biggest known weak spot of the system? | Developer | |
| 3.8 | How many users can it handle today? What breaks first when it grows? | Developer | |

---

# 4. AI-DRIVEN DEVELOPMENT SETUP [REQUIRED] [AI]
*Goal: record how AI helps build this product, so someone else can work the same way and get the same results.*

## 4A. AI tools used
| Tool (Claude, Copilot, Cursor, etc.) | Used for | Who has access | Monthly cost | Settings that matter |
|---|---|---|---|---|
| | | | | |

## 4B. AI workflow questions
| # | Question | Who answers | Your answer |
|---|---|---|---|
| 4.1 | What does AI do in our development? ☐ Writes code ☐ Writes tests ☐ Reviews code ☐ Writes docs ☐ Plans tasks ☐ Fixes bugs ☐ Deploys ☐ Other: ___ | Developer / AI lead | |
| 4.2 | What must a human ALWAYS check before AI work is accepted? | Developer / AI lead | |
| 4.3 | Where are the AI rules file(s) stored? (Example: `CLAUDE.md`, `.cursorrules`, `AGENTS.md`). Paste the link. | Developer / AI lead | |
| 4.4 | Where do our best prompts live? (Link to the prompt library) | Developer / AI lead | |
| 4.5 | Paste your 3 most useful prompts and say when to use each. | Developer / AI lead | |
| 4.6 | What has AI got wrong before? (Mistakes to watch for) | Developer / AI lead | |
| 4.7 | What must AI NEVER do on this project? (Example: "never touch the production database") | Developer / AI lead | |
| 4.8 | How do we keep AI-written code consistent? (Style guide, linter, templates) | Developer / AI lead | |
| 4.9 | What context does AI need at the start of every session? (Files, links, rules) | Developer / AI lead | |
| 4.10 | How much of the code is AI-written versus human-written? (Rough percent) | Developer / AI lead | |
| 4.11 | Who reviews AI output, and how long does a review take? | Developer / AI lead | |
| 4.12 | Where do we record AI decisions or things AI got wrong so we learn from them? | Developer / AI lead | |

## 4C. AI agents and automations [OPTIONAL]
| Agent / automation name | Job (1 sentence) | Trigger (when it runs) | Tools it can use | Can it change things? (Yes/No) | Human approval needed? | Where is it defined? | Owner |
|---|---|---|---|---|---|---|---|
| | | | | | | | |

---

# 5. ENVIRONMENTS, ACCESS & SECRETS MAP [REQUIRED]
*Goal: know every "place" the software runs and who can get in. **Do not write real passwords or keys.***

## 5A. Environments
| Environment | Purpose | URL | How it is updated | Who can deploy |
|---|---|---|---|---|
| Local (your computer) | Building | | | |
| Development / staging | Testing before launch | | | |
| Production (live) | Real customers | | | |

## 5B. Access list
| System | What it is for | Who has access | Access level (Admin/Edit/View) | How to request access |
|---|---|---|---|---|
| Example: GitHub | Code | Alex, Sam | Admin | Ask Alex |
| | | | | |

## 5C. Secrets map (WHERE secrets are stored, never the secrets themselves)
| Secret | Where stored | Who can see it | How to rotate (change) it | Last rotated |
|---|---|---|---|---|
| Example: Payment API key | 1Password → "ProjectX" vault | Owner only | Dashboard → API keys → Roll | 2026-09-01 |
| | | | | |

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 5.1 | How do we set up a brand-new computer to work on this? (Step by step, tested by someone new) | Developer | |
| 5.2 | What accounts are registered in the company name versus a personal name? (Risk if a person leaves) | Developer | |
| 5.3 | Domain name: where registered, expiry date, who controls DNS? | Developer | |

---

# 6. BUILD, CODE & DELIVERY PROCESS [REQUIRED]
*Goal: describe exactly how an idea becomes live software.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 6.1 | Step by step: how does a change go from idea to live? (Write numbered steps) | Developer | |
| 6.2 | How do we name and organize branches and commits? | Developer | |
| 6.3 | What is the code review rule? (Who reviews, how many approvals) | Developer | |
| 6.4 | How do we deploy? ☐ Automatic ☐ Manual. Paste the exact steps or the pipeline link. | Developer | |
| 6.5 | How do we undo (roll back) a bad release? Exact steps. | Developer | |
| 6.6 | How often do we release? | Developer | |
| 6.7 | How do we run the project on a local computer? (Commands, in order) | Developer | |
| 6.8 | Where do we track tasks and bugs? (Link) | Developer | |
| 6.9 | How do we version the product? (Example: v1.4.2) | Developer | |
| 6.10 | For mobile apps [OPTIONAL]: how do we submit to the App Store / Google Play? Who owns the developer accounts? | Developer | |

---

# 7. DATA, PRIVACY & SECURITY [REQUIRED]
*Goal: know what private information we hold and how we protect it.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 7.1 | What customer data do we collect? (List every type: email, name, payment, files, usage...) | Developer | |
| 7.2 | Where is it stored, and in which country/region? | Developer | |
| 7.3 | Who can see it? | Developer | |
| 7.4 | How long do we keep it, and how can a user delete theirs? | Developer | |
| 7.5 | Are backups on? How often? Where? Have we TESTED restoring one? (Date) | Developer | |
| 7.6 | Which privacy laws apply? (GDPR, CCPA, children's privacy, health, etc.) Which are done? | Developer | |
| 7.7 | Link to the Privacy Policy and Terms of Service. | Developer | |
| 7.8 | What security steps are done? ☐ HTTPS ☐ Strong passwords/2FA ☐ Secrets stored safely ☐ Dependencies updated ☐ Input checked ☐ Logs reviewed | Developer | |
| 7.9 | Has anyone tried to break into it (security test)? Results? | Developer | |
| 7.10 | What do we do if data leaks? (Who to call, what to say, within how many hours) | Developer | |
| 7.11 | [AI] Do we send customer data to AI providers? Which data? Is training on it disabled? | Developer | |

## 7B. Legal, ownership & compliance
*This is a knowledge record, not legal advice. Ask a qualified lawyer for decisions.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 7.12 | Which legal entity owns the product? (Company name, country, registration number) | Legal / Founder | |
| 7.13 | Who owns the code, designs and content? Do contractors and freelancers have signed agreements that give us ownership? Link them. | Legal / Founder | |
| 7.14 | Which open-source libraries do we use, and what are their licenses? (Link to the license list) Any that restrict commercial use? | Legal / Founder | |
| 7.15 | Which AI-generated parts (code, text, images) do we have, and do our AI tools' terms allow commercial use? [AI] | Legal / Founder | |
| 7.16 | Trademark, logo and domain: are they registered? Where, and when do they expire? | Legal / Founder | |
| 7.17 | Which contracts exist with vendors and customers? (Name, link, renewal date, cancel notice period) | Legal / Founder | |
| 7.18 | Terms of Service, Privacy Policy, Cookie notice, Refund policy: link each and its last review date. | Legal / Founder | |
| 7.19 | Payment rules: tax collection (sales tax / VAT), invoices, payment-provider terms, who handles them? | Legal / Founder | |
| 7.20 | App-store or platform rules we must follow (Apple, Google, marketplace policies)? Any past rejections? | Legal / Founder | |
| 7.21 | Industry rules that apply? (Health, finance, education, children, accessibility laws) Which are done? | Legal / Founder | |
| 7.22 | Do we need insurance, or is any license required to operate? | Legal / Founder | |
| 7.23 | Marketing laws followed? (Email opt-in/unsubscribe, ad disclosures, review and testimonial rules) | Legal / Founder | |
| 7.24 | Who is the legal contact (lawyer or advisor)? | Legal / Founder | |

---

# 8. QUALITY ASSURANCE & TESTING [REQUIRED]
*Goal: prove the product works and show how to prove it again.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 8.1 | What kinds of tests exist? ☐ Unit ☐ Integration ☐ End-to-end ☐ Manual ☐ Performance ☐ Security ☐ Accessibility | QA / Developer | |
| 8.2 | How do we run all tests? (Exact command) | QA / Developer | |
| 8.3 | What percent of the code is covered by tests? What is not covered? | QA / Developer | |
| 8.4 | What are the 10 most important things to check by hand before every release? (Smoke test list) | QA / Developer | |
| 8.5 | Which devices, browsers and screen sizes do we support? | QA / Developer | |
| 8.6 | Where do we log bugs, and how do we rank them? (Critical / High / Medium / Low) | QA / Developer | |
| 8.7 | What is the rule for blocking a launch? (Example: "no open Critical bugs") | QA / Developer | |
| 8.8 | Known bugs we accepted for launch? (List with reason) | QA / Developer | |
| 8.9 | [AI] How do we test AI-written code differently? | QA / Developer | |

## 8A. Pre-launch quality checklist
- [ ] All P0 features work end to end
- [ ] Sign up, log in, log out, reset password tested
- [ ] Payments tested with real small amounts and with failed cards (if payments exist)
- [ ] Works on mobile and desktop
- [ ] Empty states and error messages are friendly
- [ ] Speed checked under load
- [ ] Backups restore successfully
- [ ] No secrets in code or logs
- [ ] Legal pages published (Privacy, Terms)
- [ ] Someone who did NOT build it tried it, with no help

---

# 9. LAUNCH [REQUIRED]
*Goal: a calm, repeatable launch day.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 9.1 | Launch date and time (with time zone)? | Founder | |
| 9.2 | Who does what on launch day? (Name → task) | Founder | |
| 9.3 | Launch type? ☐ Private beta ☐ Public beta ☐ Full public launch ☐ Phased rollout | Founder | |
| 9.4 | Go / No-Go: who decides, and by when? | Founder | |
| 9.5 | Rollback plan: at what point do we pull the plug, and how? | Founder | |
| 9.6 | Where will we announce it? (Channels, dates) | Founder | |
| 9.7 | Who is on call during the first 72 hours? (Names, phone, hours) | Founder | |
| 9.8 | What numbers do we watch hourly on launch day? | Founder | |

## 9A. Launch day checklist
- [ ] Production environment verified
- [ ] Monitoring and alerts on
- [ ] Support inbox ready and staffed
- [ ] Pricing and billing live
- [ ] Analytics tracking confirmed
- [ ] Announcement ready to publish
- [ ] Rollback steps tested
- [ ] Team knows who to call

---

# 10. OPERATIONS, MONITORING & INCIDENTS [REQUIRED]
*Goal: when something breaks at 3 a.m., a stranger can fix it.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 10.1 | How do we know if the product is down? (Tool, link, alert destination) | Developer | |
| 10.2 | Where are logs and errors? (Links) | Developer | |
| 10.3 | Which alerts exist and who gets them? | Developer | |
| 10.4 | Monthly running costs, itemized? (Hosting, tools, AI usage) | Developer | |
| 10.5 | What happens if a cost spikes? Is there a spending limit or alert? | Developer | |

## 10A. Runbook (one row per problem)
| Problem | How to spot it | First thing to try | If that fails | Who to call |
|---|---|---|---|---|
| Example: Site is down | Uptime alert fires | Restart the server | Roll back last release | Owner |
| Example: Users can't log in | Support tickets mention login | Check the auth service status page | Ask auth provider for help | Owner |
| | | | | |

## 10B. Incident log
| Date | What happened | Cause | How we fixed it | How we prevent it |
|---|---|---|---|---|
| | | | | |

---

# 11. THE FIRST 500 CUSTOMERS [REQUIRED]
*Goal: a map from "launched" to "500 real people using it", and a record of what we learned.*

## 11A. Target and definitions
| # | Question | Who answers | Your answer |
|---|---|---|---|
| 11.1 | What counts as a "customer"? ☐ Signed up ☐ Used it once ☐ Used it 3+ times ☐ Paid | Founder | |
| 11.2 | Target date for 500 customers? | Founder | |
| 11.3 | Who is the ideal first customer? (Reuse Section 1.2) | Founder | |
| 11.4 | Where do those people hang out online or offline? | Founder | |
| 11.5 | What is our pricing? Why? Is there a free trial or free plan? | Founder | |

## 11B. Customer journey (what a customer goes through)
Fill each stage with how it works today.
| Stage | What happens | Where it lives (link) | Problems seen |
|---|---|---|---|
| 1. Discover (how they find us) | | | |
| 2. Sign up | | | |
| 3. First success ("aha moment": when they first feel the value) | | | |
| 4. Come back (habit) | | | |
| 5. Pay (if applicable) | | | |
| 6. Tell others (referral) | | | |

## 11C. Acquisition channels (one row per channel tried)
| Channel (example: friends, social posts, communities, cold email, ads, partners) | Start date | Effort / cost | Customers gained | Keep, change or stop? | Notes |
|---|---|---|---|---|---|
| | | | | | |

## 11D. Milestone tracker
| Milestone | Target date | Actual date | What worked | What did not | What changed because of it |
|---|---|---|---|---|---|
| First 1 customer | | | | | |
| 10 customers | | | | | |
| 50 customers | | | | | |
| 100 customers | | | | | |
| 250 customers | | | | | |
| 500 customers | | | | | |

## 11E. Onboarding, support & feedback
| # | Question | Who answers | Your answer |
|---|---|---|---|
| 11.6 | How does a new user learn the product? (Tour, email, help docs, video) Links. | Marketer / Founder | |
| 11.7 | Where do customers ask for help? (Email, chat, form) How fast do we reply? | Marketer / Founder | |
| 11.8 | Top 10 questions customers ask, with the answers (or a link to the FAQ). | Marketer / Founder | |
| 11.9 | How do we collect feedback? (Survey, calls, in-app) How often? | Marketer / Founder | |
| 11.10 | Where do we store feedback and who reads it? | Marketer / Founder | |
| 11.11 | Top 5 requests from customers so far. Which will we build? | Marketer / Founder | |
| 11.12 | Why do people stop using us? How do we find out? | Marketer / Founder | |

## 11F. Numbers we track
| Metric (plain words) | How it is calculated | Where to see it (link) | Today | Goal |
|---|---|---|---|---|
| Visitors per week | | | | |
| Sign-ups per week | | | | |
| % who reach the "aha moment" | | | | |
| % still active after 7 days / 30 days | | | | |
| Paying customers | | | | |
| Revenue per month | | | | |
| Cost to get one customer | | | | |
| Customers lost per month | | | | |
| Support tickets per week | | | | |
| Customer happiness score (1-10 or NPS) | | | | |

## 11G. Marketing & sales playbook
| # | Question | Who answers | Your answer |
|---|---|---|---|
| 11.13 | Brand basics: name meaning, tone of voice (3 words), logo and color links. | Marketer / Founder | |
| 11.14 | Positioning: finish this sentence: "For ___ who ___, our product is a ___ that ___, unlike ___." | Marketer / Founder | |
| 11.15 | Our one-line pitch (under 15 words) and our 30-second pitch? | Marketer / Founder | |
| 11.16 | Where do we send people first? (Landing page link) What action do we want them to take? | Marketer / Founder | |
| 11.17 | Content plan: what do we publish, where, and how often? Link to the calendar. | Marketer / Founder | |
| 11.18 | Email plan: welcome, onboarding, win-back emails. Where are they written, and which tool sends them? | Marketer / Founder | |
| 11.19 | Do we sell directly (talking to people)? If yes, link the sales script, demo steps and common objections with answers. | Marketer / Founder | |
| 11.20 | How do we collect testimonials and reviews honestly (real customers only)? | Marketer / Founder | |
| 11.21 | Referral or partner plan: what do we offer and how is it tracked? | Marketer / Founder | |
| 11.22 | Marketing budget per channel and the rule for when to spend more or stop. | Marketer / Founder | |
| 11.23 | Which tools do we use for marketing, CRM and tracking? (Name, purpose, owner) | Marketer / Founder | |
| 11.24 | What is our customer list's source and consent status (permission to contact)? | Marketer / Founder | |

### Sales pipeline (one row per prospect group, or link to your CRM)
| Stage | Meaning | How many people now | Next action | Owner |
|---|---|---|---|---|
| Lead | Showed interest | | | |
| Trial / demo | Is trying it | | | |
| Customer | Paid or active | | | |
| Lost | Said no or left (note why) | | | |

## 11H. Scaling check (what must be ready before we hit 500)
- [ ] Servers and database can handle 5x today's users
- [ ] Support can handle the ticket volume
- [ ] Billing, refunds and invoices work smoothly
- [ ] Cost per customer is below price per customer
- [ ] Onboarding works without us holding hands
- [ ] Automated alerts catch problems before customers do

---

# 12. AI INSIDE THE PRODUCT [OPTIONAL: fill if 0.4 = Yes] [AI]
*Goal: if the product itself uses AI, record everything about it. AI behavior can change without code changes, so this matters.*

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 12.1 | What does the AI do for the customer? (Plain words) | AI lead / Developer | |
| 12.2 | Which AI model(s) and provider(s) do we use? Exact model names and versions. | AI lead / Developer | |
| 12.3 | Where are the prompts (instructions to the AI) stored? Paste or link them. | AI lead / Developer | |
| 12.4 | What data is sent to the AI? What is never sent? | AI lead / Developer | |
| 12.5 | How do we know the AI answers are good? (Test set, scores, human review) Link to the evaluations. | AI lead / Developer | |
| 12.6 | What are the known failure types? (Wrong facts, unsafe output, refusing, slow, too costly) | AI lead / Developer | |
| 12.7 | What guardrails exist? (Filters, limits, human approval, fallback answer) | AI lead / Developer | |
| 12.8 | What happens when the AI provider is down or slow? | AI lead / Developer | |
| 12.9 | Cost per customer for AI usage? Monthly cap and alert? | AI lead / Developer | |
| 12.10 | How do we change a model or a prompt safely? (Test, roll out, roll back) | AI lead / Developer | |
| 12.11 | How do customers report a bad AI answer? | AI lead / Developer | |
| 12.12 | Do we tell customers they are talking to AI? Where? | AI lead / Developer | |

---

# 13. DECISIONS, RISKS & OPEN QUESTIONS [REQUIRED]
*Goal: remember WHY things are the way they are.*

## 13A. Decision log
| Date | Decision | Options we considered | Why we chose this | Who decided | Would we change it? |
|---|---|---|---|---|---|
| | | | | | |

## 13B. Risk register
| Risk | How likely (Low/Med/High) | How bad (Low/Med/High) | What we do about it | Owner |
|---|---|---|---|---|
| Example: Key developer leaves | Med | High | Keep this document updated, share access | Owner |
| | | | | |

## 13C. Open questions
| Question | Who can answer | Due date | Answer (when found) |
|---|---|---|---|
| | | | |

---

# 14. PEOPLE, ROLES & CONTACTS [REQUIRED]

| Name | Role | What they know best | Contact | Available hours / time zone | Backup person |
|---|---|---|---|---|---|
| | | | | | |

| # | Question | Who answers | Your answer |
|---|---|---|---|
| 14.1 | Which areas have only ONE person who understands them? (Single point of failure) | Founder | |
| 14.2 | Which vendors or freelancers help, and who is their contact? | Founder | |
| 14.3 | Who approves money spending, and up to what amount? | Founder | |

---

# 15. LINKS & ASSETS INDEX [REQUIRED]
*One place for every important link.*

| What | Link | Owner | Last checked |
|---|---|---|---|
| Code repository | | | |
| Design files | | | |
| Task board | | | |
| Product requirements / specs | | | |
| Architecture diagram | | | |
| API documentation | | | |
| Hosting dashboard | | | |
| Monitoring dashboard | | | |
| Analytics dashboard | | | |
| Customer support inbox | | | |
| Prompt library [AI] | | | |
| AI rules file [AI] | | | |
| Brand assets (logo, colors) | | | |
| Legal documents | | | |
| Finance / billing dashboard | | | |

---

# 16. HANDOVER SIGN-OFF [REQUIRED]
*Goal: prove the knowledge was really transferred, not just written.*

## 16A. Final checklist
- [ ] Every question is answered (or marked N/A / UNKNOWN / TODO with an owner)
- [ ] No passwords, keys or secrets are written in this file
- [ ] All links open and work
- [ ] The setup steps (5.1, 6.7) were followed by a new person, and it worked
- [ ] The rollback steps (6.5) were tested
- [ ] A backup restore was tested (7.5)
- [ ] The receiver gave a 15-minute walkthrough back to the owner
- [ ] The receiver has access to every system in Section 5B
- [ ] The receiver knows who to call (Section 14)
- [ ] Open questions (13C) have owners and dates

## 16B. Receiver's test (the receiver answers WITHOUT looking at the document)
| Question | Receiver's answer | Correct? |
|---|---|---|
| What does this product do, and for whom? | | ☐ Yes ☐ No |
| How do we deploy a change? | | ☐ Yes ☐ No |
| What do we do if the site goes down? | | ☐ Yes ☐ No |
| Where are the secrets stored? | | ☐ Yes ☐ No |
| How many customers do we have, and what is the next milestone? | | ☐ Yes ☐ No |

## 16C. Sign-off
| Role | Name | Date | Signature / "Approved" |
|---|---|---|---|
| Handing over (owner) | | | |
| Receiving | | | |
| Reviewer (optional) | | | |

---

# 17. GLOSSARY (plain-English dictionary)

| Word | Simple meaning |
|---|---|
| API | A door that lets one program talk to another program |
| Backup | A safety copy of your data |
| Branch | A separate copy of the code where you try changes safely |
| Bug | A mistake in the software |
| CI/CD | Robots that automatically test and release your code |
| Deploy | Putting new code live where customers can use it |
| Environment | A place where the software runs (your computer, test, live) |
| MVP | The smallest version that still helps real customers |
| Production | The live version real customers use |
| Prompt | The instructions you give to an AI |
| Repo (repository) | The folder where all the code and its history lives |
| Rollback | Going back to the last version that worked |
| Secret / API key | A password that programs use. Never share it in documents |
| Staging | A practice copy of the live product |
| Technical debt | Shortcuts taken now that will cost extra work later |
| Uptime | The share of time the product is working |
| Agent (AI) | An AI that can take actions and use tools on its own, not just chat |
| Evaluation (eval) | A test that checks whether AI answers are good |
| NPS | A happiness score: "How likely are you to recommend us?" |
| Churn | Customers who stop using or paying |

---

# 18. CHANGE LOG [REQUIRED]

| Version | Date | Who | What changed |
|---|---|---|---|
| v0.1 | | | Created from template (template v1.2: planning 2C, legal 7B, marketing 11G, AI interview block, Who answers column, AI-ready summary) |

---

# TEMPLATE MAINTAINER NOTES (delete in project copies)
- Copy this file for each new project and rename it `Technical_Knowledge_Transfer.md` inside the project's `Documentation/Institutional_Knowledge/` folder.
- Review the template itself every quarter; add questions that people repeatedly asked after past handovers.
- Keep it as ONE file. Link out to other documents instead of splitting this one.
