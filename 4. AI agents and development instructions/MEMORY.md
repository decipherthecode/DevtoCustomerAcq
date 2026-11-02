# How to Fill This Document (Read This First)

**What is this file?**
MEMORY.md is the "brain notebook" of your project. The AI agent (Claude Code) reads it at the start of every work session so it does not forget what the project is, what was decided, and what to avoid. Think of it as a note you leave for a helper who has forgotten everything since yesterday.

**Who can fill it?** Anyone. You do not need to be technical. If you can answer "what is this project and who is it for?", you can fill this in.

## The 7 Simple Rules

1. **Replace every `[BRACKET]`** with your own words. Brackets look like this: `[WRITE HERE]`.
2. **Read the "Example" under each field.** Copy its style, not its words.
3. **Short and clear beats long and fancy.** One or two sentences per field is enough.
4. **Do not know the answer yet? Write `TBD (to be decided)`** and add the date. Never guess and never leave a field empty.
5. **Never put secrets in this file.** No passwords, API keys, tokens, or customer personal data. Write where the secret lives instead (example: "stored in 1Password vault 'Project X'").
6. **Dates use the format `YYYY-MM-DD`** (example: 2026-10-17).
7. **Agents propose, humans approve.** An AI agent may *suggest* a new entry by writing it under `## Pending Approval`. Only a human moves it into the real sections.

## Status Symbols Used in This File

| Symbol | Meaning |
|---|---|
| ⬜ | Not started |
| 🟦 | In progress |
| ✅ | Done |
| ⛔ | Blocked (write why) |
| TBD | Unknown for now (add date) |

## How to Delete This Section
Once the file is filled in, you may collapse or delete the "How to Fill" part. Keep the rest.

---

# MEMORY.md: [PROJECT NAME]

> **Template version:** 1.0 | **Last updated:** [YYYY-MM-DD] | **Updated by:** [NAME or "Claude Code (approved by NAME)"]

---

## 0. Agent Start-Here Checklist (For the AI Agent)

Before doing any work, the agent must:

1. Read this whole file.
2. Read the **Current Focus** (Section 4) and the **Do / Don't Rules** (Section 9).
3. Check **Known Issues** (Section 11) before touching related code.
4. If something here is `TBD` or unclear, **ask the human. Do not guess.**
5. At the end of the session, write suggested updates under **Pending Approval** (Section 14).

---

## 1. Project Identity (What is this?)

| Field | Your Answer | Example |
|---|---|---|
| Project name | [ ] | Plantly |
| One-sentence description | [ ] | A mobile app that reminds people when to water their plants. |
| Product type | [ ] Web app / SaaS  [ ] Mobile app  [ ] Both | Mobile app (iOS + Android) |
| Project owner (a human) | [ ] | Priya Shah |
| Where the code lives | [ ] | github.com/yourname/plantly |
| Where the main docs live | [ ] | Notion page "Plantly HQ" |
| Project start date | [ ] | 2026-10-17 |
| Target launch date | [ ] | 2027-02-01 |
| Current phase (pick one) | [ ] Discover & Plan / Design & Build / Test & Secure / Launch & Grow | Design & Build |

---

## 2. The Problem and the People (Why does this exist?)

**2.1 The problem in plain words**
[Describe the problem a real person has. No technical words.]
*Example: People buy plants and forget to water them, so the plants die.*

**2.2 Who is the ideal customer?**
[Age, job, or situation. Be specific.]
*Example: City apartment dwellers aged 22-40 who own 3 or more houseplants.*

**2.3 How do they solve it today?**
[What do they use now? Why is it not good enough?]
*Example: Phone reminders and sticky notes. They forget to set them up and they do not know each plant's needs.*

**2.4 Our promise (one sentence)**
[What do we do better?]
*Example: Tell me when to water each plant, with no setup.*

---

## 3. Success Goals (How do we know we won?)

| Goal | Target | Deadline | Status |
|---|---|---|---|
| First paying or active customer | 1 | [YYYY-MM-DD] | ⬜ |
| 10 customers | 10 | [YYYY-MM-DD] | ⬜ |
| 50 customers | 50 | [YYYY-MM-DD] | ⬜ |
| 100 customers | 100 | [YYYY-MM-DD] | ⬜ |
| 250 customers | 250 | [YYYY-MM-DD] | ⬜ |
| **500 customers (project goal)** | 500 | [YYYY-MM-DD] | ⬜ |

**What counts as a "customer"?** [Write ONE clear definition so everyone counts the same way.]
*Example: A person who completed signup AND used the app on at least 3 different days.*

**Other success numbers we care about:**
[e.g., "App crashes under 1% of sessions", "Support replies within 24 hours"]

---

## 4. Current Focus (Update this EVERY session)

| Field | Your Answer |
|---|---|
| What we are working on right now | [ ] |
| Why it matters | [ ] |
| What "done" looks like | [ ] |
| Next 3 steps | 1. [ ] 2. [ ] 3. [ ] |
| Blocked by | [Nothing / write the blocker] |
| Last session summary (2-3 lines) | [ ] |

---

## 5. Scope (What are we building, and what are we NOT building?)

**5.1 Must-have features (needed for launch)**

| # | Feature | Plain description | Status |
|---|---|---|---|
| 1 | [ ] | [ ] | ⬜ |
| 2 | [ ] | [ ] | ⬜ |
| 3 | [ ] | [ ] | ⬜ |

**5.2 Nice-to-have features (only after launch)**
- [ ]

**5.3 Out of scope (we are NOT doing these, so the agent must not build them)**
- [ ]
*Example: No social sharing. No plant-selling marketplace.*

---

## 6. Technical Snapshot (What is it built with?)

| Item | Your Answer | Example |
|---|---|---|
| Programming language(s) | [ ] | TypeScript |
| Frontend / app framework | [ ] | React Native (Expo) |
| Backend / API | [ ] | Supabase |
| Database | [ ] | Postgres (Supabase) |
| Login / authentication | [ ] | Supabase Auth (email + Google) |
| Payments (if any) | [ ] | Stripe |
| Hosting / deployment | [ ] | Vercel (web), App Store + Google Play (mobile) |
| Analytics tool | [ ] | PostHog |
| Error tracking | [ ] | Sentry |
| Email / notifications | [ ] | Resend, Expo push |
| Environments | [ ] | dev, staging, production |

**How to run the project on a new computer (step by step):**
1. [ ]
2. [ ]
3. [ ]

**Where secrets live (names only, NEVER the secret itself):**
[ ] *Example: Keys are in `.env.local` (not committed) and in the 1Password vault "Plantly".*

---

## 7. Coding and Quality Standards (How we do things)

| Topic | Our rule | Example |
|---|---|---|
| Folder structure | [ ] | `/src/features/<feature-name>/` |
| Naming style | [ ] | camelCase for variables, PascalCase for components |
| Git branches | [ ] | `feature/short-name`, `fix/short-name` |
| Commit messages | [ ] | "feat: add watering reminder" |
| Code review | [ ] | Human approves every merge to main |
| Tests required? | [ ] | Yes, for all new business logic |
| Minimum quality checks before merging | [ ] | Lint passes, tests pass, app builds |
| Accessibility | [ ] | Text readable at large sizes, buttons labeled |

---

## 8. Test and Security Checklist (Use before every release)

**Quality checks**
- [ ] All automated tests pass
- [ ] Main user journey tested by hand (signup, core action, logout)
- [ ] Tested on the smallest and largest supported screens
- [ ] Tested on slow internet
- [ ] No known "blocker" bugs open (see Section 11)

**Security checks**
- [ ] No secrets or keys in the code or in this file
- [ ] Users can only see their own data
- [ ] Login and password reset tested
- [ ] Payment flow tested in test mode (if applicable)
- [ ] Dependencies updated and checked for known problems
- [ ] Privacy policy and terms pages published
- [ ] Backups confirmed working

**Launch-readiness checks**
- [ ] Error tracking and analytics are turned on
- [ ] Support email or chat is working
- [ ] A rollback plan exists (how to undo a bad release): [WRITE HERE]
- [ ] App store listing ready (mobile) / domain and SSL ready (web)

---

## 9. Do / Don't Rules for AI Agents (Hard boundaries)

**✅ DO**
- Ask the human when something is unclear or marked TBD.
- Make small changes and explain what you changed in plain words.
- Run the tests before saying a task is done.
- Write suggested memory updates under **Pending Approval** (Section 14).
- [Add your own: ]

**⛔ DON'T**
- Do not read, print, copy, or commit secrets, keys, or passwords.
- Do not delete files, data, branches, or database tables without asking first.
- Do not touch production data or the live site without written human approval.
- Do not add new paid services, libraries, or big dependencies without asking.
- Do not build anything listed under **Out of scope** (Section 5.3).
- Do not edit this file's approved sections yourself. Propose changes only.
- Do not make up facts. Say "I don't know" and ask.
- [Add your own: ]

---

## 10. Decision Log (What we decided and why)

> Add a row each time an important choice is made. Never delete old rows. If a decision changes, add a new row and mark the old one "Replaced".

| ID | Date | Decision | Why we chose it | Other options we rejected | Decided by | Status |
|---|---|---|---|---|---|---|
| D-001 | [YYYY-MM-DD] | [ ] | [ ] | [ ] | [ ] | Active |
| D-002 | | | | | | |

*Example row: D-001 | 2026-10-20 | Use Supabase for backend | Fast to set up, includes login | Firebase (more expensive at scale), custom server (too slow to build) | Priya | Active*

---

## 11. Known Issues and Lessons Learned

**11.1 Known issues (open problems)**

| ID | Date found | What is wrong | How serious? (Blocker / High / Medium / Low) | Workaround | Owner | Status |
|---|---|---|---|---|---|---|
| I-001 | [ ] | [ ] | [ ] | [ ] | [ ] | ⬜ |

**11.2 Lessons learned (mistakes we must not repeat)**

| Date | What happened | What we learned | New rule (if any) |
|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] |

*Example: 2026-11-02 | Agent changed the database without a backup | Always back up before schema changes | Added to Section 9 DON'T list*

---

## 12. Lifecycle Tracker (Idea to First 500 Customers)

> Mark each item ✅ when finished. Do not skip a phase unless you write a reason in the Decision Log.

### Phase 1: Discover and Plan
- [ ] Problem and ideal customer written down (Section 2)
- [ ] At least 5 real people talked to about the problem (write who/when: [ ])
- [ ] Competitors listed: [ ]
- [ ] Must-have features chosen (Section 5)
- [ ] Success goals set (Section 3)
- [ ] Budget and time limits: [ ]
- **Phase exit rule:** a human confirms "We are building the right thing." Date: [ ]

### Phase 2: Design and Build
- [ ] Screens or wireframes made (link: [ ])
- [ ] Tech choices made and logged (Section 6, Section 10)
- [ ] Project set up and runs on a new computer (Section 6)
- [ ] Core feature 1 built, tested, reviewed
- [ ] Core feature 2 built, tested, reviewed
- [ ] Core feature 3 built, tested, reviewed
- [ ] Analytics and error tracking installed
- **Phase exit rule:** all must-have features work end to end. Date: [ ]

### Phase 3: Test and Secure
- [ ] Section 8 checklists fully completed
- [ ] Beta test with at least [NUMBER] people (names or group: [ ])
- [ ] Beta feedback reviewed and top issues fixed
- [ ] Performance acceptable (page/app opens in under [NUMBER] seconds)
- **Phase exit rule:** zero Blocker issues open. Date: [ ]

### Phase 4: Launch and Grow to 500
- [ ] Launch plan written: [ ]
- [ ] Landing page or store listing live
- [ ] Onboarding (first 5 minutes experience) tested with a new person
- [ ] Support channel ready and tested
- [ ] Launch day completed. Date: [ ]
- [ ] Weekly customer review started (Section 13)
- [ ] 1 / 10 / 50 / 100 / 250 / 500 milestones tracked (Section 3)
- **Project finish line:** 500 customers reached AND the review below is written. Date: [ ]

**Final review at 500 customers (fill in at the end):**
- What worked best: [ ]
- What we would do differently: [ ]
- Top 3 things to build next: [ ]

---

## 13. Customer and Metrics Tracker (Update weekly after launch)

**13.1 Weekly numbers**

| Week starting | New signups | Total customers | Active customers | Cancelled / left | Support requests | Notes |
|---|---|---|---|---|---|---|
| [YYYY-MM-DD] | | | | | | |

**13.2 Where customers come from**

| Source (e.g., friends, social media, search, ads) | Customers so far | Cost (if any) | Keep, change, or stop? |
|---|---|---|---|
| [ ] | | | |

**13.3 What customers say (feedback themes)**

| Date | Theme (short) | How many people said it | What we will do | Status |
|---|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] | ⬜ |

**13.4 Why customers leave (add every time you learn one)**
- [ ]

> **Privacy reminder:** Never write customer names, emails, or private details here. Use counts and themes only.

---

## 14. Pending Approval (Agent writes here. Human decides.)

> The agent may add suggestions here at the end of a session. The human then chooses **Approve** (move to the right section), **Edit**, or **Reject**.

| Date | Suggested by | Suggested entry | Which section it belongs in | Human decision | Decided on |
|---|---|---|---|---|---|
| [ ] | Claude Code | [ ] | [ ] | ⬜ Approve / Edit / Reject | |

---

## 15. People, Contacts, and Links

| Role | Name | How to reach them | Notes |
|---|---|---|---|
| Project owner | [ ] | [ ] | Makes final decisions |
| Developer(s) | [ ] | [ ] | |
| Designer | [ ] | [ ] | |
| Customer support | [ ] | [ ] | |

**Important links**

| What | Link |
|---|---|
| Code repository | [ ] |
| Task board | [ ] |
| Design files | [ ] |
| Analytics dashboard | [ ] |
| Error tracker | [ ] |
| Customer feedback form | [ ] |

---

## 16. Glossary (Words used in this project)

| Word | Plain-English meaning |
|---|---|
| [e.g., "Active customer"] | [e.g., "Someone who used the app on 3+ days"] |
| [ ] | [ ] |

---

## 17. Change History of This File

| Date | Who | What changed |
|---|---|---|
| [YYYY-MM-DD] | [ ] | Created from template v1.0 |

---

## Final Self-Check (Before you call this file "done")

- [ ] No `[BRACKETS]` left. Everything is filled or says `TBD (date)`.
- [ ] No passwords, keys, or customer personal data anywhere.
- [ ] Section 4 (Current Focus) was updated today.
- [ ] A person who has never seen the project could explain it after reading Sections 1-3.
- [ ] Do / Don't rules (Section 9) match what you actually want.
