<!--
TEMPLATE VERSION: 2.0
FOLDER: Documentation Management & Institutional Knowledge
FILE: Documentation_Ownership.md
PURPOSE: One file that answers "who is responsible for every document, from first idea to our first 500 customers?"
HOW TO REUSE: Copy this file into docs/ of a new project. Fill it in. Do not edit Part 2 (Rules) unless everyone agrees.
-->

# HOW TO FILL IN THIS DOCUMENT (READ THIS FIRST)

**What is this file?**
A list of *who is responsible for every document* in your project, from the first idea until your first 500 customers are using the product. A document with no owner goes out of date and nobody notices. This file stops that.

**Who can fill it in?** Anyone. You do not need to be a writer, an engineer or a manager. If you can answer "who does what?", you can fill this in.

**How long does it take?** About 90 minutes the first time. After that, 5 to 10 minutes at each phase gate.

**In a hurry? Fast path (15 minutes):**
1. Answer Part 3.1 to 3.4.
2. In Part 6, fill **Owner** and **Backup** for every `Must` document in the phase you are in right now.
3. Come back and finish the rest before the next phase gate.

## The 9 simple steps

1. **Skim Part 1 (Glossary).** Plain-language meanings of the special words.
2. **Answer Part 3 (Project Basics).** Type after every `Your answer:`. Use the *Example* as a guide.
3. **Set your gate dates in Part 4.**
4. **Look at Part 5 (Document Catalogue).** It is already filled in. It tells you which documents exist, when they are due, how risky they are, and how long they take. Do not type here, just read.
5. **Answer Part 9 (Legal and Privacy Questions).** Your answers decide which legal documents are `Must`.
6. **Fill Part 6 (Ownership Sheet).** This is the main job: one **Owner**, one **Backup**, one **Approver** for every document.
7. **Fill Part 7 (AI Governance).** List every AI tool that helps with documents and what it may do.
8. **Fill Parts 8, 10 and 13.** Review schedule, first-500-customers plan, and workload.
9. **Do the Final Check (Part 14).** All boxes ticked = done. Commit the file to Git.

## Writing rules (so nobody has to guess)

| Do | Don't |
|---|---|
| Write a real name or one role (`Priya`, `Founder`) | Write `the team` or `someone` |
| Write a real date: `2026-11-30` | Write `soon`, `later`, `ASAP` |
| Write a real path: `docs/product/PRD.md` | Write `somewhere in the folder` |
| Write `N/A - <reason>` if something does not apply | Delete a row without saying why |
| Write `TBD by <date>` if you don't know yet | Leave a cell empty |

**Status words (use ONLY these):** `Not started` · `Draft` · `In review` · `Approved` · `Needs update` · `Retired`
**Priority words (already set, change only with a written reason):** `Must` = project cannot move on without it · `Should` = important, not blocking · `Could` = nice to have
**AI level words:** `0` · `1` · `2` · `3` (explained in Part 7)

## Rules that are never broken

1. **Every document has exactly ONE owner and ONE backup.** Two different humans.
2. **AI can draft. A human always owns.** Never list an AI as owner, backup or approver.
3. **No document becomes `Approved` until a human has read all of it.**
4. **If an owner is away or leaves, the backup takes over the same day.**
5. **No secrets in documents.** Passwords, keys, tokens and customer personal data never go in any file.

> If you only do ONE thing: fill in Owner and Backup for every `Must` document in Part 6.

---

# DOCUMENTATION OWNERSHIP

## PART 1 - GLOSSARY (plain words)

| Word | What it means |
|---|---|
| **Owner** | The one human who is accountable. If the document is wrong or old, fixing it (or getting it fixed) is their job. |
| **Backup** | A second human who can step in if the owner is away or gone. Never an AI. |
| **Approver** | The human who says "this is good enough to use." On a solo project this can be the owner, except for `High` risk documents (see Part 7). |
| **AI Helper** | An AI tool allowed to draft or update the document. It is never the owner. |
| **AI level** | How much an AI is allowed to do on a document (0 to 3, see Part 7). |
| **Risk** | `Low`, `Medium` or `High`: how much harm a wrong document could cause (money, law, safety, customer trust). |
| **Phase** | A stage of the project, Phase 0 (Discovery) to Phase 11 (Maintain and Improve). |
| **Phase gate** | A checkpoint at the end of a phase: "Are the documents for this phase ready?" |
| **Stale** | A document that no longer matches reality. |
| **Orphan** | A document nobody owns. |
| **Source of truth** | The one place where the correct, latest version lives. Here: Git. |
| **Bus factor** | How many people could disappear before the project is stuck. Owner + backup gives you 2. |
| **ADR** | Architecture Decision Record. A short note: "We chose X because Y." |
| **Runbook** | Step-by-step instructions for running or fixing something, written for a tired person at 3am. |
| **PRD** | Product Requirements Document: what we build and why. |
| **ROPA** | Record of Processing Activities: a list of what personal data you hold, why, where, and who sees it. |
| **DPA** | Data Processing Agreement: a contract with a service that handles your customers' data (payments, email, hosting, analytics). |
| **DPIA** | Data Protection Impact Assessment: a written check of privacy risks for risky data use. |
| **Activation / first win** | The moment a new customer first gets real value from the product. |
| **Time-to-value** | How long it takes a new customer to reach their first win. |
| **Oversight record** | A short log entry proving a human reviewed, changed or rejected something an AI produced. |

---

## PART 2 - THE RULES OF OWNERSHIP (do not edit unless everyone agrees)

1. One document, one owner, one backup, one approver.
2. The owner is accountable even if an AI wrote the words.
3. Documents live in Git (`docs/` folder). The Git version is the source of truth. Copies elsewhere are not official.
4. Every document starts with the small header in Part 11 so anyone can see owner, status and review dates without opening this file.
5. Documents are reviewed at **every phase gate** AND on their **calendar interval** (Parts 5 and 8), whichever comes first.
6. **Docs travel with changes.** If a change alters behaviour, price, data handling, security, legal promises or AI behaviour, the matching document is updated in the same change (or within 2 working days, with a written follow-up task).
7. **Documentation is part of "done."** A feature is not finished until its documents are updated or marked "no docs change needed - because ...".
8. **Orphan rule.** A document with no owner for 30 days is archived (`Retired`), not left to rot. Ownership never transfers by default; it is handed over in writing.
9. **Stale flag.** A document not reviewed for more than its review interval is marked `Needs update` automatically or by the owner within 14 days.
10. **After every incident** (outage, bug, customer complaint, AI mistake) the owner of the related document updates it within the time set in Part 8.
11. **Secrets stay out.** Write *where to find* a secret, never the secret itself.
12. **Nobody carries too much.** No person owns more than 8 `Must` documents (Part 13 checks this).

---

## PART 3 - PROJECT BASICS

*Answer every question. Short answers are fine.*

**3.1 What is the project called?**
Example: `PlantPal`
Your answer:

**3.2 In one sentence, what does it do and for whom?**
Example: `PlantPal reminds busy people when to water their houseplants.`
Your answer:

**3.3 Project ID (3 to 5 capital letters; becomes the start of every document ID)?**
Example: `PLNT` → the PRD becomes `PLNT-PS-05`
Your answer:

**3.4 Who is the Project Lead (the person who makes final decisions)?**
Your answer:

**3.5 Team size right now?** (tick one)
- [ ] Just me (solo)  - [ ] 2 to 5 people  - [ ] 6 to 10 people  - [ ] More than 10 people

**3.6 If solo: who is your trusted backup human?** (friend, co-founder, advisor, contractor)
Example: `Sam (advisor), has read access to the repository`
Your answer:

**3.7 Where does the project live?**
- Repository URL:
- Docs folder path (default `docs/`):
- Task board / issue tracker URL:
- Starter template folder path (default `templates/`, see Part 5):

**3.8 Which phase is the project in today?** (tick one)
- [ ] 0 Discovery  - [ ] 1 Strategy and Planning  - [ ] 2 Design  - [ ] 3 Security and Compliance Setup
- [ ] 4 Build  - [ ] 5 Test and QA  - [ ] 6 Beta  - [ ] 7 Launch Preparation
- [ ] 8 Launch  - [ ] 9 First 500 Customers  - [ ] 10 Post-Launch Review  - [ ] 11 Maintain and Improve

**3.9 Date this file was created:** `YYYY-MM-DD`
Your answer:

**3.10 Who owns THIS file (Documentation_Ownership.md)?**
- Owner:
- Backup:

**3.11 What kind of product is it?** (tick all that apply)
- [ ] Website / web app  - [ ] Mobile app  - [ ] API / developer tool  - [ ] Physical product with software  - [ ] Other: ________

**3.12 Does the product handle personal data?** (names, emails, payments, location, health, children's data)
- [ ] No  - [ ] Yes, basic (name, email)  - [ ] Yes, sensitive (payments, health, location, children, biometrics)
*(More legal questions are in Part 9.)*

**3.13 Does the product use AI inside the product itself (not just to build it)?**
- [ ] No  - [ ] Yes
*(If Yes, every document marked "AI in product" in Part 5 becomes `Must`.)*

**3.14 How many hours per week can the whole team spend on documents?**
Your answer:

---

## PART 4 - THE PROJECT PHASES (the map)

The journey has 12 phases. The final milestone is **500 customers actively using the product**.

| Phase | Name | Question this phase answers | Gate question (ask before moving on) |
|---|---|---|---|
| 0 | Discovery | Is this problem real and worth solving? | Do we have evidence people want this? |
| 1 | Strategy and Planning | What exactly will we build, in what order? | Is scope written down and agreed? |
| 2 | Design | What will it look like and how will it work? | Can a builder start without asking "what do you mean?" |
| 3 | Security and Compliance Setup | What rules and risks must we respect? | Do we know what data we touch and which laws apply? |
| 4 | Build | Are we building it correctly? | Do setup, architecture and API docs match the code? |
| 5 | Test and QA | Does it actually work? | Are test results recorded and known bugs listed? |
| 6 | Beta | Do real users succeed with it? | Is feedback captured and acted on? |
| 7 | Launch Preparation | Are we ready to go live safely? | Are help, support, rollback, and legal pages ready? |
| 8 | Launch | Is it live and stable? | Are release notes, status page and incident process live? |
| 9 | First 500 Customers | Are customers arriving, succeeding and staying? | See the milestones in Part 10 |
| 10 | Post-Launch Review | What did we learn? | Is the lessons-learned document filed? |
| 11 | Maintain and Improve | How do we keep it healthy? | Is every document still owned and fresh? |

**4.1 Which phases apply to this project?** (cross out any that do not, and say why)
Your answer:

**4.2 Target date for each gate:**

| Phase | Target gate date | Gate approver (human) | Gate passed on (date) |
|---|---|---|---|
| 0 | | | |
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 | | | |
| 7 | | | |
| 8 | | | |
| 9 (500 customers) | | | |
| 10 | | | |
| 11 | | | |

**4.3 Gate checklist (copy and tick at EVERY gate):**
- [ ] Every `Must` document due in this phase is `Approved`.
- [ ] Every document touched in this phase has a review date in the future.
- [ ] No `Must` document has an empty Owner, Backup or Approver.
- [ ] Documents that became wrong during this phase are marked `Needs update` with a date.
- [ ] AI oversight records (Part 7.5) are up to date.
- [ ] This file's change log (Part 12.4) has a new line.

---

## PART 5 - DOCUMENT CATALOGUE (already filled in, read only)

### How to read this table

| Column | Meaning |
|---|---|
| **ID** | Short code. Full ID = Project ID + `-` + this code (e.g. `PLNT-PS-05`). |
| **Phase** | Phase by which the first approved version must exist. |
| **Priority** | `Must` / `Should` / `Could`. |
| **Applies if** | `Always` or a condition from Parts 3 and 9. If the condition is false, write `N/A - <reason>` in Part 6. |
| **Risk** | `Low` / `Medium` / `High`. Controls how much AI may do (Part 7) and how careful review must be. |
| **Starter template** | A reusable blank for this document. Keep all in one master folder and copy into the project. If a starter doesn't exist yet, write `TBD by <date>` in Part 6 notes and build one the first time you write it. |
| **Write (h)** | Rough hours to write the first version. |
| **Keep (h/mo)** | Rough hours per month to keep it fresh. |
| **Review every (days)** | Maximum days between reviews. `Release` = every release. `Each` = each time the thing happens. |

*Hours are starting guesses for a small product. After your first project, correct them here once and reuse across all projects.*

### 5A. Product and Strategy

| ID | Document | Phase | Priority | Applies if | Risk | Starter template | Write (h) | Keep (h/mo) | Review every (days) |
|---|---|---|---|---|---|---|---|---|---|
| PS-01 | Problem statement and research notes | 0 | Must | Always | Medium | `templates/PS-01.md` | 3 | 0.5 | 90 |
| PS-02 | Target users / personas | 0 | Should | Always | Low | `templates/PS-02.md` | 2 | 0.5 | 90 |
| PS-03 | Competitor and market notes | 0 | Could | Always | Low | `templates/PS-03.md` | 3 | 1 | 90 |
| PS-04 | Vision, goals and success numbers | 1 | Must | Always | Medium | `templates/PS-04.md` | 3 | 0.5 | 90 |
| PS-05 | PRD (Product Requirements) incl. scope and non-goals | 1 | Must | Always | Medium | `templates/PS-05.md` | 8 | 2 | 90 |
| PS-06 | Roadmap and release plan | 1 | Must | Always | Medium | `templates/PS-06.md` | 3 | 1 | 90 |
| PS-07 | Metrics and KPIs (including the 500-customer goal) | 1 | Must | Always | Medium | `templates/PS-07.md` | 3 | 1 | 90 |
| PS-08 | Risks and assumptions register | 1 | Should | Always | Medium | `templates/PS-08.md` | 2 | 1 | 30 |
| PS-09 | Pricing and packaging | 7 | Should | Paid product | High | `templates/PS-09.md` | 3 | 0.5 | 90 |
| PS-10 | Go-to-market and launch plan | 7 | Must | Always | Medium | `templates/PS-10.md` | 6 | 1 | 30 |
| PS-11 | Lessons learned (post-launch review) | 10 | Must | Always | Low | `templates/PS-11.md` | 4 | 0 | Each |

### 5B. Design, Technical and Quality

| ID | Document | Phase | Priority | Applies if | Risk | Starter template | Write (h) | Keep (h/mo) | Review every (days) |
|---|---|---|---|---|---|---|---|---|---|
| TQ-01 | UX flows, wireframes and design system | 2 | Should | Has screens | Low | `templates/TQ-01.md` | 8 | 1 | 90 |
| TQ-02 | Architecture overview (diagram + plain-words explanation) | 2 | Must | Always | Medium | `templates/TQ-02.md` | 6 | 1 | 90 |
| TQ-03 | Decision log (ADRs) | 2 | Must | Always | Medium | `templates/TQ-03.md` | 0.5 per decision | 0.5 | 90 |
| TQ-04 | Data model / database schema | 2 | Must | Stores data | Medium | `templates/TQ-04.md` | 4 | 1 | 90 |
| TQ-05 | Developer setup guide (zero to running in under 30 minutes) | 4 | Must | Always | Low | `templates/TQ-05.md` | 3 | 0.5 | 30 |
| TQ-06 | Coding standards and contribution rules | 4 | Should | Always | Low | `templates/TQ-06.md` | 2 | 0.25 | 180 |
| TQ-07 | API reference | 4 | Must | Has an API | Medium | `templates/TQ-07.md` | 6 | 2 | 30 |
| TQ-08 | Environment and configuration guide (no secrets inside) | 4 | Must | Always | High | `templates/TQ-08.md` | 3 | 0.5 | 30 |
| TQ-09 | Release checklist and Definition of Done (includes "docs updated?") | 4 | Must | Always | Low | `templates/TQ-09.md` | 2 | 0.25 | 90 |
| TQ-10 | Test plan and test results | 5 | Must | Always | Medium | `templates/TQ-10.md` | 5 | 2 | Release |
| TQ-11 | Known issues and bug triage rules | 5 | Should | Always | Low | `templates/TQ-11.md` | 2 | 1 | 30 |
| TQ-12 | Deployment and rollback runbook | 7 | Must | Always | High | `templates/TQ-12.md` | 4 | 0.5 | 90 |
| TQ-13 | Monitoring, alerts and on-call guide | 7 | Must | Always | High | `templates/TQ-13.md` | 4 | 0.5 | 90 |
| TQ-14 | Incident response plan | 7 | Must | Always | High | `templates/TQ-14.md` | 4 | 0.5 | 90 |
| TQ-15 | Incident reports (one per incident) | 8 | Must | Always | High | `templates/TQ-15.md` | 2 per incident | 0 | Each |
| TQ-16 | Backup and disaster recovery plan | 7 | Should | Stores data | High | `templates/TQ-16.md` | 4 | 0.5 | 90 |
| TQ-17 | Performance and capacity notes (can we handle 500 customers?) | 7 | Should | Always | Medium | `templates/TQ-17.md` | 3 | 1 | 90 |

### 5C. Launch and Customers

| ID | Document | Phase | Priority | Applies if | Risk | Starter template | Write (h) | Keep (h/mo) | Review every (days) |
|---|---|---|---|---|---|---|---|---|---|
| LC-01 | Beta plan and feedback log | 6 | Should | Has a beta | Low | `templates/LC-01.md` | 3 | 2 | 14 |
| LC-02 | Onboarding milestone map (sign-up to first win to regular use) | 7 | Must | Always | Medium | `templates/LC-02.md` | 3 | 1 | 30 |
| LC-03 | Getting-started guide | 7 | Must | Always | Low | `templates/LC-03.md` | 4 | 1 | 30 |
| LC-04 | Help centre / FAQ | 7 | Must | Always | Low | `templates/LC-04.md` | 8 | 2 | 30 |
| LC-05 | Support playbook (who answers, how fast, what to say) | 7 | Must | Always | Medium | `templates/LC-05.md` | 4 | 1 | 30 |
| LC-06 | Release notes and public changelog | 8 | Must | Always | Low | `templates/LC-06.md` | 0.5 per release | 0.5 | Release |
| LC-07 | Status page and outage message templates | 8 | Should | Always | Medium | `templates/LC-07.md` | 2 | 0.25 | 90 |
| LC-08 | Customer feedback log and themes | 9 | Must | Always | Low | `templates/LC-08.md` | 1 | 2 | 14 |
| LC-09 | Docs-gap log (questions customers ask that our docs don't answer) | 9 | Must | Always | Low | `templates/LC-09.md` | 0.5 | 1 | 14 |
| LC-10 | Cancellation and churn notes (why people leave) | 9 | Should | Always | Low | `templates/LC-10.md` | 1 | 1 | 30 |
| LC-11 | Marketing messages and approved claims | 7 | Could | Always | Medium | `templates/LC-11.md` | 3 | 0.5 | 90 |
| LC-12 | Milestone reports (1, 10, 50, 100, 250, 500 customers) | 9 | Must | Always | Low | `templates/LC-12.md` | 2 per milestone | 0 | Each |

### 5D. Legal, Privacy, Security and Compliance

*Not legal advice. Have a qualified lawyer check anything marked `High` that you publish or sign.*

| ID | Document | Phase | Priority | Applies if | Risk | Starter template | Write (h) | Keep (h/mo) | Review every (days) |
|---|---|---|---|---|---|---|---|---|---|
| LG-01 | Data inventory / records of processing (ROPA) | 3 | Must | Personal data | High | `templates/LG-01.md` | 4 | 1 | 90 |
| LG-02 | Legal basis and consent records | 3 | Must | Personal data | High | `templates/LG-02.md` | 3 | 0.5 | 90 |
| LG-03 | Security checklist and threat notes | 3 | Must | Always | High | `templates/LG-03.md` | 4 | 1 | 90 |
| LG-04 | DPIA (privacy risk assessment) | 3 | Should | Sensitive data or AI | High | `templates/LG-04.md` | 6 | 1 | 180 |
| LG-05 | Children's data rules | 3 | Must | Users under 18 | High | `templates/LG-05.md` | 3 | 0.5 | 180 |
| LG-06 | Cross-border data transfer notes | 3 | Should | Data leaves home region | High | `templates/LG-06.md` | 2 | 0.25 | 180 |
| LG-07 | Access control list (who can touch what; no passwords) | 4 | Must | Always | High | `templates/LG-07.md` | 1 | 0.5 | 90 |
| LG-08 | Third-party services, processors and signed DPAs | 4 | Must | Always | High | `templates/LG-08.md` | 3 | 0.5 | 90 |
| LG-09 | Open-source and software licence list | 4 | Must | Always | Medium | `templates/LG-09.md` | 2 | 0.5 | 90 |
| LG-10 | Privacy policy (public) | 7 | Must | Personal data | High | `templates/LG-10.md` | 4 | 0.5 | 180 |
| LG-11 | Cookie and tracking notice, with consent records | 7 | Must | Cookies or analytics | High | `templates/LG-11.md` | 2 | 0.5 | 180 |
| LG-12 | Terms of service (public) | 7 | Must | Always | High | `templates/LG-12.md` | 4 | 0.5 | 180 |
| LG-13 | Accessibility statement and checks | 7 | Should | Public site or app | High | `templates/LG-13.md` | 3 | 0.5 | 180 |
| LG-14 | Customer data requests process (see my data, delete my data, opt out) | 7 | Must | Personal data | High | `templates/LG-14.md` | 3 | 0.5 | 90 |
| LG-15 | Data retention and deletion schedule | 7 | Should | Personal data | High | `templates/LG-15.md` | 2 | 0.5 | 180 |
| LG-16 | Breach and security incident notification plan | 7 | Must | Personal data | High | `templates/LG-16.md` | 3 | 0.5 | 90 |

### 5E. AI documents

*"AI in product" = you answered Yes to 3.13. If No, those rows are `N/A - no AI in product`. AI-01 to AI-04 always apply if you use AI to build or document the project.*

| ID | Document | Phase | Priority | Applies if | Risk | Starter template | Write (h) | Keep (h/mo) | Review every (days) |
|---|---|---|---|---|---|---|---|---|---|
| AI-01 | AI usage rules for this project (what AI may and may not do) | 1 | Must | Uses AI at all | High | `templates/AI-01.md` | 2 | 0.5 | 30 |
| AI-02 | AI asset list: models, tools, providers, versions, cost, data sent | 4 | Must | Uses AI at all | Medium | `templates/AI-02.md` | 2 | 0.5 | 30 |
| AI-03 | Prompt and agent-instruction library (versioned) | 4 | Should | Uses AI at all | Medium | `templates/AI-03.md` | 3 | 1 | 30 |
| AI-04 | AI oversight records (human review log) | 4 | Must | Uses AI at all | High | `templates/AI-04.md` | 0.25 per review | 0.5 | 30 |
| AI-05 | AI risk register (what could go wrong, how bad, how we check) | 1 | Must | AI in product | High | `templates/AI-05.md` | 3 | 1 | 30 |
| AI-06 | AI test set and quality results (wrong answers, bias, unsafe output) | 5 | Must | AI in product | High | `templates/AI-06.md` | 6 | 2 | Release |
| AI-07 | System / model card (what the AI feature does, limits, data used) | 7 | Should | AI in product | High | `templates/AI-07.md` | 4 | 0.5 | 90 |
| AI-08 | Customer-facing AI notice and limits wording | 7 | Must | AI in product | High | `templates/AI-08.md` | 2 | 0.25 | 90 |
| AI-09 | Human override and "turn the AI off" plan | 7 | Must | AI in product | High | `templates/AI-09.md` | 2 | 0.25 | 90 |
| AI-10 | AI incident log (bad AI behaviour in production) | 8 | Must | AI in product | High | `templates/AI-10.md` | 1 | 0.5 | 30 |

### 5F. My own extra documents

*Anything specific to this project. Give each a code like `EX-01` and fill the same columns.*

| ID | Document | Phase | Priority | Applies if | Risk | Starter template | Write (h) | Keep (h/mo) | Review every (days) |
|---|---|---|---|---|---|---|---|---|---|
| EX-01 | | | | | | | | | |
| EX-02 | | | | | | | | | |

---

## PART 6 - OWNERSHIP SHEET (YOU FILL THIS IN)

### How to fill the sheet

| Column | What to write |
|---|---|
| **Applies?** | `Yes`, or `N/A - <reason>` (see "Applies if" in Part 5). |
| **Owner** | ONE human name or role. |
| **Backup** | ONE different human. Never an AI. |
| **Approver** | The human who signs it off. Solo: may equal Owner, except for `High` risk documents (see Part 7.2). |
| **AI Helper** | AI tool name allowed to help, or `None`. Must match Part 7.4. |
| **AI level** | `0` to `3` (Part 7.1). Must not exceed the maximum for the document's risk. |
| **Path** | Real file path, e.g. `docs/product/PRD.md`. |
| **Status** | One status word. |
| **Last reviewed** | `YYYY-MM-DD` or `Never`. |
| **Next review** | `YYYY-MM-DD` = Last reviewed + "Review every" days from Part 5. |

### 6.1 Product and Strategy

| ID | Document | Applies? | Owner | Backup | Approver | AI Helper | AI level | Path | Status | Last reviewed | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| PS-01 | Problem statement and research notes | | | | | | | | Not started | Never | |
| PS-02 | Target users / personas | | | | | | | | Not started | Never | |
| PS-03 | Competitor and market notes | | | | | | | | Not started | Never | |
| PS-04 | Vision, goals and success numbers | | | | | | | | Not started | Never | |
| PS-05 | PRD | | | | | | | | Not started | Never | |
| PS-06 | Roadmap and release plan | | | | | | | | Not started | Never | |
| PS-07 | Metrics and KPIs | | | | | | | | Not started | Never | |
| PS-08 | Risks and assumptions register | | | | | | | | Not started | Never | |
| PS-09 | Pricing and packaging | | | | | | | | Not started | Never | |
| PS-10 | Go-to-market and launch plan | | | | | | | | Not started | Never | |
| PS-11 | Lessons learned | | | | | | | | Not started | Never | |

### 6.2 Design, Technical and Quality

| ID | Document | Applies? | Owner | Backup | Approver | AI Helper | AI level | Path | Status | Last reviewed | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| TQ-01 | UX flows, wireframes, design system | | | | | | | | Not started | Never | |
| TQ-02 | Architecture overview | | | | | | | | Not started | Never | |
| TQ-03 | Decision log (ADRs) | | | | | | | | Not started | Never | |
| TQ-04 | Data model / schema | | | | | | | | Not started | Never | |
| TQ-05 | Developer setup guide | | | | | | | | Not started | Never | |
| TQ-06 | Coding standards | | | | | | | | Not started | Never | |
| TQ-07 | API reference | | | | | | | | Not started | Never | |
| TQ-08 | Environment and configuration guide | | | | | | | | Not started | Never | |
| TQ-09 | Release checklist and Definition of Done | | | | | | | | Not started | Never | |
| TQ-10 | Test plan and results | | | | | | | | Not started | Never | |
| TQ-11 | Known issues and triage rules | | | | | | | | Not started | Never | |
| TQ-12 | Deployment and rollback runbook | | | | | | | | Not started | Never | |
| TQ-13 | Monitoring, alerts, on-call guide | | | | | | | | Not started | Never | |
| TQ-14 | Incident response plan | | | | | | | | Not started | Never | |
| TQ-15 | Incident reports | | | | | | | | Not started | Never | |
| TQ-16 | Backup and disaster recovery plan | | | | | | | | Not started | Never | |
| TQ-17 | Performance and capacity notes | | | | | | | | Not started | Never | |

### 6.3 Launch and Customers

| ID | Document | Applies? | Owner | Backup | Approver | AI Helper | AI level | Path | Status | Last reviewed | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| LC-01 | Beta plan and feedback log | | | | | | | | Not started | Never | |
| LC-02 | Onboarding milestone map | | | | | | | | Not started | Never | |
| LC-03 | Getting-started guide | | | | | | | | Not started | Never | |
| LC-04 | Help centre / FAQ | | | | | | | | Not started | Never | |
| LC-05 | Support playbook | | | | | | | | Not started | Never | |
| LC-06 | Release notes and public changelog | | | | | | | | Not started | Never | |
| LC-07 | Status page and outage templates | | | | | | | | Not started | Never | |
| LC-08 | Customer feedback log | | | | | | | | Not started | Never | |
| LC-09 | Docs-gap log | | | | | | | | Not started | Never | |
| LC-10 | Cancellation and churn notes | | | | | | | | Not started | Never | |
| LC-11 | Marketing messages and approved claims | | | | | | | | Not started | Never | |
| LC-12 | Milestone reports | | | | | | | | Not started | Never | |

### 6.4 Legal, Privacy, Security and Compliance

| ID | Document | Applies? | Owner | Backup | Approver | AI Helper | AI level | Path | Status | Last reviewed | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| LG-01 | Data inventory / ROPA | | | | | | | | Not started | Never | |
| LG-02 | Legal basis and consent records | | | | | | | | Not started | Never | |
| LG-03 | Security checklist and threat notes | | | | | | | | Not started | Never | |
| LG-04 | DPIA | | | | | | | | Not started | Never | |
| LG-05 | Children's data rules | | | | | | | | Not started | Never | |
| LG-06 | Cross-border transfer notes | | | | | | | | Not started | Never | |
| LG-07 | Access control list | | | | | | | | Not started | Never | |
| LG-08 | Third-party services and DPAs | | | | | | | | Not started | Never | |
| LG-09 | Open-source and licence list | | | | | | | | Not started | Never | |
| LG-10 | Privacy policy | | | | | | | | Not started | Never | |
| LG-11 | Cookie notice and consent records | | | | | | | | Not started | Never | |
| LG-12 | Terms of service | | | | | | | | Not started | Never | |
| LG-13 | Accessibility statement | | | | | | | | Not started | Never | |
| LG-14 | Customer data requests process | | | | | | | | Not started | Never | |
| LG-15 | Data retention and deletion schedule | | | | | | | | Not started | Never | |
| LG-16 | Breach notification plan | | | | | | | | Not started | Never | |

### 6.5 AI documents

| ID | Document | Applies? | Owner | Backup | Approver | AI Helper | AI level | Path | Status | Last reviewed | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| AI-01 | AI usage rules for this project | | | | | | | | Not started | Never | |
| AI-02 | AI asset list | | | | | | | | Not started | Never | |
| AI-03 | Prompt and agent-instruction library | | | | | | | | Not started | Never | |
| AI-04 | AI oversight records | | | | | | | | Not started | Never | |
| AI-05 | AI risk register | | | | | | | | Not started | Never | |
| AI-06 | AI test set and quality results | | | | | | | | Not started | Never | |
| AI-07 | System / model card | | | | | | | | Not started | Never | |
| AI-08 | Customer-facing AI notice | | | | | | | | Not started | Never | |
| AI-09 | Human override and AI-off plan | | | | | | | | Not started | Never | |
| AI-10 | AI incident log | | | | | | | | Not started | Never | |

### 6.6 My own extra documents

| ID | Document | Applies? | Owner | Backup | Approver | AI Helper | AI level | Path | Status | Last reviewed | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| EX-01 | | | | | | | | | Not started | Never | |
| EX-02 | | | | | | | | | Not started | Never | |

### 6.7 Questions to check the sheet

**6.7.1 Count your documents.** Must: ___  Should: ___  Could: ___  N/A: ___
**6.7.2 Does any person own more than 8 `Must` documents?**
- [ ] No  - [ ] Yes, so I will move these: ______________________
**6.7.3 Is any person the only Backup for more than 5 documents?** (risky)
- [ ] No  - [ ] Yes, I will fix it by: `YYYY-MM-DD`
**6.7.4 Is any `High` risk document approved by the same person who owns it?**
- [ ] No  - [ ] Yes, so I will add a second human check (Part 7.2) by: `YYYY-MM-DD`
**6.7.5 Is a document the team needs missing?** Add it in 6.6 and Part 5F.
Your answer:

---

## PART 7 - AI GOVERNANCE

*Rule: AI drafts, a human always owns. But "a human checks it" must be real: someone specific, looking at specific evidence, who can say no.*

### 7.1 AI levels (what an AI is allowed to do on a document)

| Level | Name | What the AI may do | What the human does |
|---|---|---|---|
| **0** | No AI | Nothing | Writes everything |
| **1** | AI suggests | Suggests ideas, outlines, wording | Writes the document |
| **2** | AI drafts (default) | Writes a draft or an update | Reads all of it, edits, approves |
| **3** | AI maintains | Makes routine updates only: typos, links, version numbers, changelog lines | Spot-checks within 2 working days |

### 7.2 Maximum AI level by risk

| Document risk | Highest AI level allowed | Extra rule |
|---|---|---|
| **Low** | 3 | Owner spot-checks. |
| **Medium** | 2 | Owner reads all of it before `Approved`. |
| **High** | 2 | A second human check is needed: the Approver should be a different person from the Owner. If solo, ask your backup or advisor, or wait 24 hours and re-read with the checklist in 7.6. Legal documents also get a lawyer's eyes before publishing. |

### 7.3 Questions

**7.3.1 Which AI tools do you use to write or change documents?**
Example: `Claude, GitHub Copilot, ChatGPT`
Your answer:

**7.3.2 Which human checks AI-written text? (Name one person.)**
Your answer:

**7.3.3 What must that person compare the AI text against?** (tick all that apply)
- [ ] The actual code  - [ ] Test results  - [ ] The live product  - [ ] A trusted source / the law text  - [ ] Other: ________

**7.3.4 Who has the authority to reject or roll back AI-written text?**
Your answer:

**7.3.5 May AI change an `Approved` document by itself?**
- [ ] No. It must open a change request for a human (recommended)
- [ ] Only for Level 3 routine fixes on `Low` risk documents

**7.3.6 What must AI never put in documents?** (tick all that apply)
- [x] Passwords, keys, tokens
- [x] Customer personal data
- [x] Made-up facts, numbers, quotes, links or legal claims
- [ ] Other: ______________________

**7.3.7 Where are prompts and agent instructions stored?** (path, ideally in Git)
Your answer:

**7.3.8 How will AI-assisted changes be labelled in Git?**
Example: commit message ends with `AI-assisted: <tool + model>; reviewed-by: <name>`
Your answer:

**7.3.9 What data may be sent to AI tools?** (be specific, e.g. "public docs yes, customer emails never")
Your answer:

**7.3.10 If AI is inside the product: what is the "turn AI off" switch, and who may flip it?**
Your answer:

### 7.4 AI agent register

| AI tool / agent | Version or model | Allowed to do | NOT allowed to do | Document IDs it may help with | Max AI level | Human who checks it | Last reviewed |
|---|---|---|---|---|---|---|---|
| Example: Claude | Latest | Draft, summarise, rewrite, build tables | Approve, delete, publish, see secrets or customer data | PS-01, TQ-07, LC-04 | 2 | Priya | 2026-10-19 |
| | | | | | | | |
| | | | | | | | |
| | | | | | | | |

### 7.5 Oversight record (one line every time a human reviews AI work on a `Medium` or `High` document)

| Date | Document ID | AI tool + version | What the AI did | What the human checked it against | Decision (`Accepted` / `Edited` / `Rejected`) | Reviewer |
|---|---|---|---|---|---|---|
| | | | | | | |

*(For `Low` risk Level 3 changes, a Git label from 7.3.8 is enough.)*

### 7.6 Human check before accepting AI text (tick all before `Approved`)

- [ ] I read the whole text, not just the top.
- [ ] Every fact, number, name and link is real and I checked it.
- [ ] It matches what the code or product really does today.
- [ ] No secrets or personal data are inside.
- [ ] It is in plain words a new person could follow.
- [ ] The header (Part 11) and the oversight record (7.5) are updated.

### 7.7 How this connects to common AI-governance frameworks (for reference)

| Idea in the frameworks | Where it lives in this file |
|---|---|
| Govern: roles, rules, accountability | Parts 2 and 7, AI-01 |
| Map: know your AI, its context and risks | AI-02, AI-05, LG-04 |
| Measure: test and monitor quality and safety | AI-06 |
| Manage: respond, override, improve | AI-09, AI-10, Part 8 |
| Traceability and human oversight records | 7.3.8, 7.5, AI-04 |

*Frameworks referenced: NIST AI Risk Management Framework, ISO/IEC 42001, EU AI Act. This table is a map, not a compliance claim. If your AI makes decisions about people (jobs, credit, education, health, safety), ask a lawyer which rules apply to you.*

---

## PART 8 - REVIEW AND FRESHNESS RULES

Documents are reviewed in **two** ways, whichever comes first:
1. **Phase gate:** when the project moves to the next phase.
2. **Calendar interval:** the maximum time a document may go unreviewed (column "Review every" in Part 5).

### 8.1 Also review immediately when

| Event | Documents to review |
|---|---|
| Any change in behaviour, price, data handling or AI behaviour | The matching documents in the same change |
| Any release | TQ-10, LC-06, LC-04, LC-03 if screens changed |
| Any incident | TQ-14, TQ-15, TQ-12, TQ-13; AI-10 if AI was involved |
| Anyone joins or leaves | LG-07, Part 6 owners/backups |
| New third-party service or new AI model | LG-08, LG-09, AI-02, LG-10 |
| New country or new type of customer | Part 9, LG-01, LG-10, LG-12 |
| A law or a provider's terms change | Every `High` risk legal document |

### 8.2 Questions

**8.2.1 Do you want shorter or longer intervals for any document?** (which and why)
Your answer:

**8.2.2 Who gets the reminder when a review is due?**
Your answer:

**8.2.3 Where is the reminder set up?** (calendar, task board, automatic issue; give a link or `TBD by <date>`)
Your answer:

**8.2.4 When a document is more than 14 days overdue, what happens?**
- [ ] Status becomes `Needs update` and the Owner is told
- [ ] Backup is told as well
- [ ] Project Lead is told
- [ ] Other: ______________________

**8.2.5 How fast must the owner update documents after an incident?**
- [ ] 2 working days  - [ ] 5 working days  - [ ] Other: ________

### 8.3 Review log (one line per review)

| Date | Document ID | Reviewed by | Result (`Fine` / `Updated` / `Retired`) | Notes |
|---|---|---|---|---|
| | | | | |

---

## PART 9 - LEGAL AND PRIVACY QUESTIONS (decide which legal documents are `Must`)

*This is a planning aid, not legal advice. Laws change and differ by country. Have a qualified lawyer check your Privacy Policy, Terms of Service and any High risk legal document before you publish it.*

Tick what is true, then mark the listed documents `Must` in Part 6.

| # | Question | If you ticked Yes, these become `Must` |
|---|---|---|
| 9.1 | Will you have customers in the EU or UK? - [ ] Yes - [ ] No | LG-01, LG-02, LG-08 (signed DPAs), LG-10, LG-11, LG-14, LG-15, LG-16, LG-06 |
| 9.2 | Will you have customers in California or other US states with privacy laws? - [ ] Yes - [ ] No | LG-10, LG-14 (including opt-out of sale/sharing where it applies), LG-16 |
| 9.3 | Customers in Canada, Brazil, Australia or elsewhere? - [ ] Yes (list: ________) - [ ] No | LG-10, LG-14; ask a lawyer about local rules |
| 9.4 | Could any user be under 18? - [ ] Yes - [ ] No | LG-05, LG-04 |
| 9.5 | Do you use cookies, analytics, ads or trackers? - [ ] Yes - [ ] No | LG-11 (with consent records), LG-10 |
| 9.6 | Do you take payments? - [ ] Yes - [ ] No | LG-08 (payment provider), LG-12, LG-03 |
| 9.7 | Do you handle sensitive data (health, biometrics, precise location, finances, children)? - [ ] Yes - [ ] No | LG-04 (DPIA), LG-03, LG-16 |
| 9.8 | Does your product use AI that produces content or decisions for customers? - [ ] Yes - [ ] No | AI-05 to AI-10, LG-04, LG-10 (mention AI use) |
| 9.9 | Does your AI affect decisions about people (hiring, credit, school, health, safety)? - [ ] Yes - [ ] No | Stop and ask a lawyer before launch. Mark AI-05, AI-06, AI-07, AI-09 as `Must` with the highest care. |
| 9.10 | Is your site or app public? - [ ] Yes - [ ] No | LG-13 (accessibility statement and checks) |
| 9.11 | Do you use third-party services that touch customer data (hosting, email, analytics, payments)? - [ ] Yes - [ ] No | LG-08, LG-09 |

**9.12 Which lawyer or legal service will review your High risk documents?**
Your answer:

**9.13 Date the lawyer last reviewed them:** `YYYY-MM-DD` or `Not yet`
Your answer:

---

## PART 10 - FIRST 500 CUSTOMERS: DOCUMENTATION PLAN

*As customers arrive, different documents become urgent. Also: when many customers get stuck at the same step, a document is usually missing or unclear. This part makes you notice.*

### 10.1 Define your words exactly

**10.1.1 What counts as "a customer using the product"?**
Example: `Someone who finished onboarding AND used the product at least twice in the last 30 days.`
Your answer:

**10.1.2 What is the "first win" (activation)?**
Example: `Added their first plant and received their first watering reminder.`
Your answer:

**10.1.3 Target time-to-value?**
Example: `Under 10 minutes from sign-up.`
Your answer:

**10.1.4 Where is the live customer count shown?** (dashboard link)
Your answer:

**10.1.5 Who updates this part?**
Your answer:

### 10.2 Onboarding milestone map (fill in; this is document LC-02 in short form)

| Step | What the customer does | Which document helps them here | Doc owner | How we measure it | Target |
|---|---|---|---|---|---|
| 1. Sign up | | | | | |
| 2. First login | | | | | |
| 3. Set up | | | | | |
| 4. First win | | | | | |
| 5. Comes back (second use within 7 days) | | | | | |
| 6. Becomes regular (e.g. 3 uses in 30 days) | | | | | |

### 10.3 Milestones from customer 1 to customer 500

| Customers | Documents that must be fresh | Numbers to write down | Question to answer | Owner | Date reached | Done? |
|---|---|---|---|---|---|---|
| **1** | LC-03, LC-04, LC-05, LG-10, LG-12, LG-14 (if personal data), TQ-14 | Time from sign-up to first win | Could the customer succeed with no help from us? | | | [ ] |
| **10** | LC-08, LC-09, LC-04, LC-05 | Top 5 questions asked; % who reached first win | Which 5 questions go into the FAQ this week? | | | [ ] |
| **50** | LC-06, LC-07, TQ-14, TQ-13, LC-05 | Support response time; number of incidents; docs-related tickets % | Was the incident plan tested at least once? | | | [ ] |
| **100** | PS-07, LC-10, AI-10 (if AI), LC-02 | Activation rate; 30-day return rate; reasons for leaving | Where do people drop off, and is a document the cause? | | | [ ] |
| **250** | TQ-17, TQ-16, LG-07, PS-09, LG-08 | Load and cost per customer; backup test date; access list changes | Can the system and the support process handle 500? | | | [ ] |
| **500** | **All `Must` documents**, LC-12, PS-11 | Final milestone numbers | Is every `Must` document reviewed within the last 30 days? | | | [ ] |

### 10.4 The docs-gap rule

If **3 or more** customers ask the same question, or **many** customers stop at the same onboarding step:
1. Add a line to the docs-gap log (below) the same day.
2. The owner of the related document fixes or creates it within **5 working days**.
3. Check two weeks later: did the questions stop?

| Date found | Question or step where customers get stuck | How many customers | Document ID (new or existing) | Owner | Fixed on | Questions stopped? |
|---|---|---|---|---|---|---|
| | | | | | | |

### 10.5 Questions

**10.5.1 Who answers customer questions?**
Your answer:

**10.5.2 Target first-reply time?**
Example: `Within 1 working day`
Your answer:

**10.5.3 Where are questions and complaints recorded?** (tool / link)
Your answer:

**10.5.4 How often is customer feedback reviewed, and by whom?**
Your answer:

---

## PART 11 - HEADER AND AUTOMATION

### 11.1 Required header for every document

*Copy to the top of every document so ownership is visible without opening this file.*

```markdown
---
doc_id: PLNT-PS-05
title: Product Requirements Document
risk: Medium                # Low | Medium | High
owner: <name or role>
backup: <name or role>
approver: <name or role>
ai_helper: <tool name or None>
ai_level: 2                 # 0 | 1 | 2 | 3
phase_due: 1
status: Draft               # Not started | Draft | In review | Approved | Needs update | Retired
last_reviewed: YYYY-MM-DD
next_review: YYYY-MM-DD
source_of_truth: docs/product/PRD.md
---
```

**11.1.1 Do all existing documents have this header?**
- [ ] Yes  - [ ] No, I will add it by `YYYY-MM-DD`

### 11.2 Optional level-up: make ownership automatic

*Skip this at first. Come back when the basics work.*

**Pull request / change checklist** (paste into your change template):

```markdown
## Documentation impact (required)
- [ ] No docs change needed, because: ______
- [ ] Docs updated: IDs ______
- [ ] Docs need follow-up (link to task): ______
- [ ] AI helped with docs in this change; reviewed by: ______
```

**Code ownership rule for docs** (example, in a `CODEOWNERS` file; replace names):

```text
/docs/product/    @product-owner
/docs/technical/  @tech-owner
/docs/legal/      @legal-owner
/docs/ai/         @ai-owner
```

**Stale check:** once a week, list every document whose `next_review` date is in the past or whose `status` is `Needs update`, and send the list to its owner. Anything with no owner after 30 days is archived (Part 2, rule 8).

**11.2.1 Which of these will you set up?** (tick)
- [ ] Change checklist  - [ ] Code ownership rule  - [ ] Weekly stale check  - [ ] None yet
**Date to set them up:** `YYYY-MM-DD`

---

## PART 12 - HANDOVER, ESCALATION AND CHANGES

### 12.1 If an owner is away or leaves

**Before leaving, the owner must:** (all of these)
- [ ] Tell the Project Lead at least 14 days ahead (or as soon as possible)
- [ ] Write a handover note for each document they own
- [ ] Walk the backup through each `Must` document
- [ ] Update Owner and Backup in Part 6 and in each document header
- [ ] Hand over or remove access (update LG-07)

**If the owner disappears suddenly:** the backup takes over the same day. If the backup is also unavailable, the Project Lead decides within 2 working days.

**12.1.1 Who is the Project Lead's backup?**
Your answer:

### 12.2 How to change an owner

1. Change Owner/Backup/Approver in Part 6.
2. Change the header in the document.
3. Add a line to the change log (12.4).
4. Tell the new owner in writing and make sure they accept.

### 12.3 Who to tell when something is wrong

| Problem | First, tell | If no answer in 2 working days, tell |
|---|---|---|
| Document is wrong or out of date | The owner | The backup, then the Project Lead |
| Nobody owns a document | The Project Lead | N/A - Project Lead assigns an owner within 2 working days |
| Two documents disagree | Both owners | The Project Lead decides which is right |
| AI wrote something false | The human checker (7.3.2) | The Project Lead |
| A legal document may be outdated | The owner and the lawyer (9.12) | The Project Lead |

### 12.4 Change log for THIS file

| Date | Who changed it | What changed | Why |
|---|---|---|---|
| | | Created from template v2.0 | |

---

## PART 13 - WORKLOAD AND EFFORT CHECK

*Add up the hours from Part 5 for every document a person owns. This shows who is overloaded before it becomes a problem.*

| Person | Number of `Must` documents owned | Hours to write (total) | Hours per month to keep fresh | Hours per week they have for docs | OK? |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

**13.1 Rules of thumb:**
- More than 8 `Must` documents for one person: move some.
- Monthly upkeep hours greater than 4 times their weekly hours: move some or reduce the review frequency, with a written reason.

**13.2 Total hours to write everything that applies:** ______  **Total per month to keep fresh:** ______

**13.3 What will you do if the hours do not fit?** (e.g. cut `Could` documents, use AI Level 2 more, extend the date)
Your answer:

---

## PART 14 - FINAL CHECK (tick every box before this file is "done")

**Completeness**
- [ ] Every document that applies has ONE Owner, ONE Backup and ONE Approver.
- [ ] Owner and Backup are two different humans for every row.
- [ ] No cell in Part 6 is empty. Unknowns say `TBD by <date>`.
- [ ] Every AI Helper named in Part 6 is listed in Part 7.4, and no AI level is above the maximum for its risk.
- [ ] Every document has a real Path and a real Next review date.
- [ ] Part 4.2 has target dates for every gate.
- [ ] Part 9 is answered and the matching legal documents are marked `Must`.
- [ ] Part 10.1 defines exactly what a "customer" and a "first win" are.

**Safety**
- [ ] No passwords, keys, tokens or customer data are written anywhere in this file.
- [ ] No AI is listed as owner, backup or approver.
- [ ] Every `High` risk document has a second human check planned.
- [ ] A lawyer will review the public legal documents before launch (Part 9.12).

**Workload**
- [ ] Nobody owns more than 8 `Must` documents (Part 13).
- [ ] Hours fit the time available, or the plan in 13.3 is written.

**Readiness**
- [ ] A new person could find the owner of any document in under 1 minute.
- [ ] The file is committed to Git as `docs/Documentation_Ownership.md`.
- [ ] A review reminder for THIS file is set (Part 8.2.3).

**Sign-off**

| Role | Name | Date | Signature (type your name) |
|---|---|---|---|
| Project Lead | | | |
| Owner of this file | | | |
| Backup of this file | | | |

---

## PART 15 - QUICK ANSWERS (FAQ for the person filling this in)

**"I'm working alone. Do I really need a backup?"**
Yes. It can be a friend, advisor or contractor who knows where the files are. It protects the project from illness, travel or burnout. It can never be an AI.

**"I don't know who should own a document."**
Ask: "Who will be most upset if this is wrong?" That person is the owner. Still unsure? Write `TBD by <date>`.

**"What's the difference between Owner and Approver?"**
The Owner keeps it true and up to date. The Approver says "yes, this is good enough to use." On a solo project they can be the same person, except for `High` risk documents.

**"Do I have to write all these documents?"**
No. This is a *list of owners*, not a to-do list for today. Only `Must` documents are needed for the phase you are in. Mark what does not apply `N/A - <reason>`. Never remove Owner and Backup from a `Must` row.

**"Can AI fill in this file for me?"**
AI may draft answers. You read every answer and confirm it. You remain the owner of this file.

**"What if my project is tiny?"**
Keep it short: mark most `Should` and `Could` rows `N/A - project too small`. Keep the `Must` rows.

**"When do I update this file?"**
At every phase gate, when anyone joins or leaves, when you add or retire a document, and when you add or change an AI tool or a third-party service.

**"What is a 'starter template'?"**
A reusable blank document (headings and questions only) for one document type, kept in one master folder. You copy it into each new project instead of starting from an empty page.

---

## APPENDIX A - A FILLED-IN EXAMPLE (PlantPal)

*Look at this if you are unsure how to answer. It is made up.*

**Part 3 answers:** Name `PlantPal` · One sentence `PlantPal reminds busy people when to water their houseplants.` · Project ID `PLNT` · Project Lead `Priya` · Team `Just me (solo)` · Backup human `Sam (advisor)` · Phase today `2 Design` · Personal data `Yes, basic (name, email)` · AI in product `No` · Hours per week for docs `4`.

**Part 6 sample rows:**

| ID | Document | Applies? | Owner | Backup | Approver | AI Helper | AI level | Path | Status | Last reviewed | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|
| PS-05 | PRD | Yes | Priya | Sam | Priya | Claude | 2 | `docs/product/PRD.md` | Draft | 2026-10-19 | 2027-01-17 |
| TQ-07 | API reference | Yes | Priya | Sam | Priya | Claude | 2 | `docs/technical/api.md` | Not started | Never | 2026-12-15 |
| LC-06 | Release notes | Yes | Priya | Sam | Priya | Claude | 3 | `docs/customer/release-notes.md` | Not started | Never | TBD by 2026-12-01 |
| LG-10 | Privacy policy | Yes | Priya | Sam | Sam (second human check) | Claude | 2 | `docs/legal/privacy.md` | Not started | Never | TBD by 2027-01-15 |
| LG-05 | Children's data rules | N/A - no users under 18 | - | - | - | None | 0 | - | Retired | - | - |
| AI-05 | AI risk register | N/A - no AI in product | - | - | - | None | 0 | - | Retired | - | - |

**Part 7.5 sample oversight record:**

| Date | Document ID | AI tool + version | What the AI did | What the human checked it against | Decision | Reviewer |
|---|---|---|---|---|---|---|
| 2026-10-19 | LG-10 | Claude (latest) | Drafted first privacy policy | Data inventory LG-01 and the real sign-up form; lawyer to review before launch | Edited | Sam |

**Part 10.1 sample answers:** Customer = `finished setup AND got at least 2 reminders in 30 days` · First win = `added first plant and received first reminder` · Target time-to-value = `under 10 minutes`.

---

## APPENDIX B - IDEAS THIS TEMPLATE IS BUILT ON

- **Docs-as-code:** keep documents in version control next to the code, review them like code, update them in the same change.
- **Single named owner per document, with a defined substitute and explicit handover.**
- **Documentation in the "definition of done"** and a documentation-impact decision on every change.
- **Review cadence by document type, plus review on trigger events;** stale documents get flagged and orphaned ones archived.
- **Human oversight of AI that is real:** a named reviewer, defined evidence, authority to overrule, and a record of each review (ideas common to NIST AI RMF, ISO/IEC 42001 and the EU AI Act).
- **Privacy basics for launch:** data inventory, legal basis and consent records, processor agreements, privacy policy, cookie notice, data-request process, breach plan, accessibility statement (ideas common to GDPR, CCPA/CPRA and similar laws).
- **Onboarding milestones** (first login, first win, return visit) and using drop-off points to find documentation gaps.

*End of template. Version 2.0.*
