# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **Who this is for:** Anyone. If you can read and type, you can fill this in. No technical knowledge is needed.
> **What this document is:** The one plan for your **Beta Program**: how you test your product with real people, fix problems, and grow from your first tester to your **first 500 customers**.
> **Where it lives:** `Launch, Marketing and Customer Acquisition/Beta_Program.md`
> **One file rule:** Everything is in this one file. Do not create extra files. If you have a link, paste the link here.

## The 7 simple rules

1. **Go top to bottom.** Do not skip around. Each part builds on the one before it.
2. **Answer every question.** Replace the text `👉 ANSWER HERE` with your answer. Do not leave it blank.
3. **Look at the tag on each question:**
   - `[REQUIRED]` means you must answer before you can start the beta.
   - `[OPTIONAL]` means answer it if it applies. If not, write `N/A` and one short reason.
4. **Look at the example.** Every question has an `Example:` line. Copy the style, not the words.
5. **Tick boxes like this:** change `[ ]` to `[x]`.
6. **Never guess.** If you do not know, write `UNKNOWN - will find out by YYYY-MM-DD` and who will find out. Do not invent a number.
7. **Use numbers, not feelings.** Write "50 testers", not "some testers". Write "by 2026-12-01", not "soon".

## What the symbols mean

| Symbol | Meaning |
|---|---|
| 👉 | This is where you write your answer |
| 🤖 | Instruction for an AI agent helping you fill or check the document |
| ⛔ | Stop point (gate). Do not move on until it is true |
| ✅ | Done |
| ⚠️ | Warning, common mistake |

## How to know you are finished

You are finished when:
- [ ] Every `[REQUIRED]` question has an answer (no `👉 ANSWER HERE` left in required questions)
- [ ] Every `[OPTIONAL]` question has an answer or `N/A` with a reason
- [ ] Part 23 (Final Checklist) is fully ticked
- [ ] A second person (or an AI agent) has read it and found nothing confusing

## 🤖 Instructions for AI agents (read before touching this file)

1. Fill only what the human has told you or what you can verify. **Never invent** names, numbers, dates, links, or legal text. Write `UNKNOWN` instead.
2. Keep question IDs (like `Q2.3`) unchanged. Other documents may refer to them.
3. Do not delete questions. Mark non-applicable ones `N/A - reason`.
4. After filling, run the **Self-Check** in Part 23 and report any gaps as a list.
5. Use plain language (reading age 10). Short sentences. No jargon without a Glossary entry.
6. Write dates as `YYYY-MM-DD`. Write money with currency, e.g. `USD 9.99`.
7. When a number is a target, also write how it will be measured and where.

---

# PART 0. DOCUMENT CONTROL

| Field | Answer |
|---|---|
| Product name `[REQUIRED]` | 👉 ANSWER HERE |
| Beta program name `[REQUIRED]` (Example: "Project Sunrise Beta") | 👉 ANSWER HERE |
| Document owner (one person) `[REQUIRED]` | 👉 ANSWER HERE |
| Date created `[REQUIRED]` | 👉 ANSWER HERE |
| Last updated `[REQUIRED]` | 👉 ANSWER HERE |
| Version `[REQUIRED]` (Example: 0.1, 1.0) | 👉 ANSWER HERE |
| Status `[REQUIRED]` | [ ] Draft  [ ] In review  [ ] Approved  [ ] Running  [ ] Closed |
| Related documents (links) `[OPTIONAL]` (PRD, roadmap, test plan) | 👉 ANSWER HERE |

### Change log
| Date | Who | What changed |
|---|---|---|
| 👉 | 👉 | 👉 |

---

# PART 1. PRODUCT SNAPSHOT

> **Why this matters:** Anyone (or any AI) who reads only this part should understand what you are testing.

**Q1.1 `[REQUIRED]` In one sentence, what does your product do?**
Example: "A phone app that reminds people to water their plants."
👉 ANSWER HERE

**Q1.2 `[REQUIRED]` Who is it for? (Describe one real type of person.)**
Example: "Busy adults aged 25 to 40 who own 3 or more house plants."
👉 ANSWER HERE

**Q1.3 `[REQUIRED]` What problem does it solve for them?**
Example: "Their plants die because they forget to water them."
👉 ANSWER HERE

**Q1.4 `[REQUIRED]` What type of product is it? (Tick all that apply)**
- [ ] Web app / SaaS
- [ ] Mobile app (iOS / Android)
- [ ] Desktop software
- [ ] API / developer tool
- [ ] AI agent / AI-powered product
- [ ] Physical device (hardware)
- [ ] Service / marketplace
- [ ] Other: 👉

**Q1.5 `[REQUIRED]` What are the 3 to 5 most important things a tester can do? (Your "must-work" features)**
| # | Feature | Why it matters |
|---|---|---|
| 1 | 👉 | 👉 |
| 2 | 👉 | 👉 |
| 3 | 👉 | 👉 |

**Q1.6 `[REQUIRED]` What is NOT ready yet or is known to be broken? (Be honest. Testers will find out anyway.)**
👉 ANSWER HERE

**Q1.7 `[REQUIRED]` Where do testers get the product? (Link, app store, TestFlight, invite page, shipping)**
👉 ANSWER HERE

**Q1.8 `[OPTIONAL]` What platforms and versions do you support?**
Example: "Chrome and Safari latest, iOS 16 and up, Android 12 and up."
👉 ANSWER HERE

---

# PART 2. BETA GOALS AND STAGE PLAN

> **Big picture:** Your journey has 4 stages. You must pass a gate (⛔) before moving to the next one.
>
> `Alpha (inside team)` → `Closed Beta (invite only)` → `Open Beta (anyone can join)` → `Public Launch` → `First 500 customers`

## 2A. Goals

**Q2.1 `[REQUIRED]` Why are you running a beta? (Tick all that apply)**
- [ ] Find bugs
- [ ] Check that people understand the product
- [ ] Check that people want it (demand)
- [ ] Test that it works at larger scale
- [ ] Test pricing
- [ ] Collect testimonials and stories
- [ ] Build an early community
- [ ] Other: 👉

**Q2.2 `[REQUIRED]` What is your single most important goal? (Pick ONE)**
👉 ANSWER HERE

**Q2.3 `[REQUIRED]` What does "success" look like at the end of the beta? Write 3 measurable statements.**
Example: "At least 40% of testers are still using the product after 30 days."
1. 👉
2. 👉
3. 👉

**Q2.4 `[REQUIRED]` What would make you STOP or pause the beta? (Your emergency brakes)**
Example: "Any data loss, any security leak, or crash rate above 5%."
👉 ANSWER HERE

## 2B. The stage plan

**Q2.5 `[REQUIRED]` Fill in the plan for each stage.**

| | Alpha | Closed Beta | Open Beta | Public Launch |
|---|---|---|---|---|
| Who is in? | 👉 | 👉 | 👉 | 👉 |
| Number of users (target) | 👉 | 👉 | 👉 | 👉 |
| Start date | 👉 | 👉 | 👉 | 👉 |
| End date | 👉 | 👉 | 👉 | 👉 |
| Main question we answer | 👉 | 👉 | 👉 | 👉 |

Example row "Main question": Alpha = "Does it run without crashing?", Closed = "Do real users get value?", Open = "Can it handle many people?", Launch = "Will people pay?"

## 2C. The 500-customer ladder

> **What this is:** You do not jump from 0 to 500. You climb a ladder. At every step you check that things are healthy before climbing higher.

**Q2.6 `[REQUIRED]` Define what counts as a "customer" for you.**
- [ ] Signed up
- [ ] Signed up AND completed first key action (activated)
- [ ] Paying customer
- [ ] Other: 👉

⚠️ Pick ONE definition and use it everywhere in this document.
My definition: 👉 ANSWER HERE

**Q2.7 `[REQUIRED]` Fill in the ladder.**

| Step | Total users | Target date | How will you find them? | Health check to pass before climbing |
|---|---|---|---|---|
| 1 | 10 | 👉 | 👉 | 👉 |
| 2 | 50 | 👉 | 👉 | 👉 |
| 3 | 100 | 👉 | 👉 | 👉 |
| 4 | 250 | 👉 | 👉 | 👉 |
| 5 | 500 | 👉 | 👉 | 👉 |

Example health check: "Fewer than 3 open critical bugs and day-7 retention above 30%."

⛔ **Gate:** Do not climb to the next step until the health check is passed and written in Part 18.

---

# PART 3. READINESS: AI-DRIVEN DEVELOPMENT TO BETA

> **Why this matters:** Beta is not the first time anyone tests the product. This part proves the product is ready for real people. It follows your development life cycle.

**Q3.1 `[REQUIRED]` Which development stages are complete? Tick and add a link or note as proof.**

| Stage | Done? | Proof (link / note) |
|---|---|---|
| Idea and problem defined | [ ] | 👉 |
| Requirements written (what to build) | [ ] | 👉 |
| Design done (screens / flows / architecture) | [ ] | 👉 |
| Code built for all must-work features (Q1.5) | [ ] | 👉 |
| Automated tests written and passing | [ ] | 👉 |
| Code reviewed (by a person or AI agent) | [ ] | 👉 |
| Manual testing by the team (alpha) | [ ] | 👉 |
| Security check done | [ ] | 👉 |
| Performance check done | [ ] | 👉 |
| Staging / test environment working | [ ] | 👉 |
| Production environment working | [ ] | 👉 |
| Backups set up and restore tested | [ ] | 👉 |
| Monitoring and alerts set up | [ ] | 👉 |
| Rollback plan (how to undo a bad release) written | [ ] | 👉 |

**Q3.2 `[REQUIRED]` How was AI used to build and check this product?**
Example: "AI agent wrote 60% of the code; a human reviewed all of it; AI generated test cases."
👉 ANSWER HERE

**Q3.3 `[REQUIRED]` What is the quality bar for entering Closed Beta?**

| Check | Target | Actual | Pass? |
|---|---|---|---|
| Open critical bugs (Severity 1) | 0 | 👉 | [ ] |
| Open high bugs (Severity 2) | 👉 (Example: 3 or fewer) | 👉 | [ ] |
| Automated test pass rate | 👉 (Example: 95%+) | 👉 | [ ] |
| Crash-free sessions | 👉 (Example: 98%+) | 👉 | [ ] |
| Main user flow works start to finish | Yes | 👉 | [ ] |

**Q3.4 `[REQUIRED]` Who said "yes, it is ready"? Write name and date.**
👉 ANSWER HERE

⛔ **Gate 0 (Alpha to Closed Beta):** All boxes in Q3.1 and Q3.3 ticked, and Q3.4 filled.

---

# PART 4. WHO DOES WHAT (ROLES)

> 💡 **Why this matters:** When a problem happens, nobody should ask "who is doing this?" Every job needs a name.
> **Solo founder?** Put your name next to "You" and "AI agent". Delete extra rows or write N/A.

**Q4.1 `[REQUIRED]` Fill in the roles.**

| Job | Person or AI agent | How to reach them | Backup |
|---|---|---|---|
| Beta owner (makes final decisions) | 👉 | 👉 | 👉 |
| Product (decides what to fix first) | 👉 | 👉 | 👉 |
| Engineering (fixes bugs) | 👉 | 👉 | 👉 |
| QA (checks fixes work) | 👉 | 👉 | 👉 |
| Support (answers testers) | 👉 | 👉 | 👉 |
| Marketing (finds testers, shares news) | 👉 | 👉 | 👉 |
| Data (reads numbers) | 👉 | 👉 | 👉 |
| Legal / privacy (checks rules) | 👉 | 👉 | 👉 |

**Q4.2 `[REQUIRED]` What decisions can the AI agent make alone, and what must a human approve?**

| Task | AI alone | Human must approve |
|---|---|---|
| Reply to common tester questions | [ ] | [ ] |
| Label and sort bug reports | [ ] | [ ] |
| Fix a bug in code | [ ] | [ ] |
| Release a fix to testers | [ ] | [ ] |
| Send a message to ALL testers | [ ] | [ ] |
| Spend money / change pricing | [ ] | [ ] |
| Remove a tester from the beta | [ ] | [ ] |
| Handle a privacy or security issue | [ ] | [ ] |

---

# PART 5. WHO ARE YOUR TESTERS AND WHERE DO THEY COME FROM

> 💡 **Why this matters:** Ten testers who truly need your product teach you more than a thousand who are just curious. Pick the right people, not the most people.

## 5A. The right tester

**Q5.1 `[REQUIRED]` Describe your ideal tester. (Age, job, habits, tools they use, problem they have.)**
👉 ANSWER HERE

**Q5.2 `[REQUIRED]` Who should NOT be in the beta?**
Example: "Competitors, people who never use apps like this, anyone under 18."
👉 ANSWER HERE

**Q5.3 `[REQUIRED]` Which mix of testers do you want?**
| Type | Why | % of testers |
|---|---|---|
| Perfect-fit users (your target customer) | 👉 | 👉 |
| Power users (find edge cases) | 👉 | 👉 |
| Beginners (find confusing parts) | 👉 | 👉 |
| Friendly experts (give deep feedback) | 👉 | 👉 |

**Q5.4 `[REQUIRED]` Do you need testers on different devices, countries or languages?**
👉 ANSWER HERE

## 5B. Finding them

**Q5.5 `[REQUIRED]` Where will you find testers? (Tick all and write the target number from each)**

| Source | Use? | Target number | Link / details |
|---|---|---|---|
| Friends, family, personal network | [ ] | 👉 | 👉 |
| Existing email list | [ ] | 👉 | 👉 |
| Waitlist page | [ ] | 👉 | 👉 |
| Social media (X, LinkedIn, Instagram, TikTok) | [ ] | 👉 | 👉 |
| Communities (Reddit, Discord, Slack, Facebook groups) | [ ] | 👉 | 👉 |
| Product Hunt / BetaList / similar sites | [ ] | 👉 | 👉 |
| Partners or other businesses | [ ] | 👉 | 👉 |
| Paid ads | [ ] | 👉 | 👉 |
| Referrals from other testers | [ ] | 👉 | 👉 |
| Other | [ ] | 👉 | 👉 |

**Q5.6 `[REQUIRED]` What is the sign-up / application form? Which questions will it ask?**
Example questions: name, email, device, how they heard about us, what problem they have, do they agree to the terms.
👉 ANSWER HERE

**Q5.7 `[REQUIRED]` How will you choose who gets in?**
- [ ] First come, first served
- [ ] Hand-picked by us
- [ ] Scored by form answers
- [ ] Random draw
- [ ] Other: 👉

**Q5.8 `[REQUIRED]` Do you have a waiting list when there are more applicants than spots? What happens to them?**
👉 ANSWER HERE

---

# PART 6. ONBOARDING (THE FIRST 15 MINUTES)

> **Why this matters:** If testers get lost in the first 15 minutes, you lose them forever.

**Q6.1 `[REQUIRED]` What does a tester receive right after they are accepted? (Tick all)**
- [ ] Welcome email
- [ ] Access link / invite code / download link
- [ ] Quick start guide (1 page)
- [ ] Short intro video
- [ ] Link to feedback channel
- [ ] Link to known issues list
- [ ] Rules and terms to accept
- [ ] Other: 👉

**Q6.2 `[REQUIRED]` Write the welcome message (short and friendly).**
Example: "Hi {Name}! Thanks for joining the Sunrise beta. Here is your link: {link}. Your first mission: add one plant and set a reminder. It takes 3 minutes. Stuck? Reply to this email."
👉 ANSWER HERE

**Q6.3 `[REQUIRED]` What is the "first mission" you give every tester?**
👉 ANSWER HERE

**Q6.4 `[REQUIRED]` What is the "aha moment"? (The moment the tester first feels the value.)**
Example: "When they get their first reminder and water the plant."
👉 ANSWER HERE

**Q6.5 `[REQUIRED]` How many days should it take a tester to reach the aha moment? 👉**

**Q6.6 `[OPTIONAL]` What is your plan if a tester has not started after 3 days?**
Example: "Send a friendly reminder on day 3 and day 7."
👉 ANSWER HERE

---

# PART 7. ADD-ON QUESTIONS BY PRODUCT TYPE

> Only answer the block(s) that match what you ticked in Q1.4. Write `N/A - not this type` for the others.

### 7A. Software / web / mobile / API `[OPTIONAL]`
- Which browsers, devices, operating systems must work? 👉
- How will you ship updates to testers (auto-update, new link, new build)? 👉
- How will you track crashes and errors (tool name)? 👉
- If an API: how will testers get keys, and what are the usage limits? 👉

### 7B. AI-powered product or AI agent `[OPTIONAL]`
- Which AI model(s) power it? 👉
- How do you check answer quality (a test set, human review, both)? 👉
- What must the AI NEVER do? (List clear rules.) 👉
- How do testers report a wrong, harmful, or strange AI answer? 👉
- Do you store testers' conversations? For how long? Do you use them to improve the AI? Do testers know? 👉
- How do you control AI cost per tester (limits, caps)? 👉
- Is there always a human who can take over? 👉

### 7C. Physical hardware `[OPTIONAL]`
- How many units are ready? Who pays for shipping? 👉
- What happens if a device is broken on arrival? 👉
- How do testers return devices at the end? 👉
- Are safety or regulatory rules involved (batteries, radio, certifications)? 👉

### 7D. Service or marketplace `[OPTIONAL]`
- Do you need both sides (buyers and sellers) in the beta? How will you balance them? 👉
- What happens if a transaction goes wrong? 👉

---

# PART 8. COLLECTING FEEDBACK

> **Rule:** Make it very easy to give feedback. If it takes more than 1 minute, people will not do it.

**Q8.1 `[REQUIRED]` Where can testers send feedback? (Tick all that you will use)**
| Channel | Use? | Link / name | Who watches it | Checked how often |
|---|---|---|---|---|
| In-product feedback button | [ ] | 👉 | 👉 | 👉 |
| Bug report form | [ ] | 👉 | 👉 | 👉 |
| Email | [ ] | 👉 | 👉 | 👉 |
| Community (Discord / Slack) | [ ] | 👉 | 👉 | 👉 |
| Surveys | [ ] | 👉 | 👉 | 👉 |
| 1-on-1 calls | [ ] | 👉 | 👉 | 👉 |
| Other | [ ] | 👉 | 👉 | 👉 |

**Q8.2 `[REQUIRED]` What should a good bug report include? (Paste this into your bug form.)**
- [ ] What did you try to do?
- [ ] What did you expect to happen?
- [ ] What actually happened?
- [ ] Steps to repeat it
- [ ] Screenshot or video
- [ ] Device, browser, version
- [ ] Date and time

**Q8.3 `[REQUIRED]` What surveys will you send, and when?**
| Survey | When | Questions (max 5-10) | Tool |
|---|---|---|---|
| Welcome survey | Day 0 | 👉 | 👉 |
| First-experience survey | Day 1-3 | 👉 | 👉 |
| Mid-beta check-in | Week 2 | 👉 | 👉 |
| Product-market-fit survey | Week 3-4 | "How disappointed would you be if you could no longer use this?" (Very / Somewhat / Not) + why | 👉 |
| Exit survey | End of beta | 👉 | 👉 |

**Q8.4 `[REQUIRED]` Where does ALL feedback end up? (One master list)**
Example: "A GitHub Issues board" or "A Notion database".
👉 ANSWER HERE

**Q8.5 `[REQUIRED]` How do you decide what to build or fix first?**
Simple scoring: **Impact** (how many people, how bad) × **Effort** (how long) → fix high-impact, low-effort things first.
My method: 👉 ANSWER HERE

**Q8.6 `[REQUIRED]` How will you tell testers "we heard you" and what you changed?**
Example: "A weekly 'You said, we did' email."
👉 ANSWER HERE

---

# PART 9. BUG TRIAGE AND FIXING

> 💡 **Why this matters:** You will get more problems than you can fix. Triage means deciding which ones to fix first, like a doctor who treats the most serious patient first. If unsure about a level, choose the higher one.

**Q9.1 `[REQUIRED]` Confirm or edit the severity levels.**

| Level | Name | Meaning | Example | Reply within | Fix within |
|---|---|---|---|---|---|
| S1 | Critical | Data loss, security leak, product unusable for many | App deletes user data | 👉 (Suggest: 1 hour) | 👉 (Suggest: 24 hours) |
| S2 | High | Main feature broken, no workaround | Cannot save a plant | 👉 (Suggest: 4 hours) | 👉 (Suggest: 3 days) |
| S3 | Medium | Feature broken but workaround exists | Button needs two taps | 👉 (Suggest: 1 day) | 👉 (Suggest: 2 weeks) |
| S4 | Low | Small or cosmetic | Typo, misaligned icon | 👉 (Suggest: 3 days) | 👉 (Suggest: backlog) |

**Q9.2 `[REQUIRED]` What are the steps of a bug's life?**
Suggested: `New → Confirmed → Prioritized → In progress → In review → Fixed → Verified by tester → Closed`
My steps: 👉 ANSWER HERE

**Q9.3 `[REQUIRED]` How often do you review new bugs? (Example: every weekday at 10:00)**
👉 ANSWER HERE

**Q9.4 `[REQUIRED]` How do fixes reach testers? How often? (Example: every Tuesday, or immediately for S1.)**
👉 ANSWER HERE

**Q9.5 `[REQUIRED]` Who checks that a fix really works before it is closed?**
👉 ANSWER HERE

**Q9.6 `[REQUIRED]` Emergency plan: what happens if something S1 happens at 2 a.m.?**
Who is alerted, how, and what is the first action? (Pause sign-ups? Switch off a feature? Roll back?)
👉 ANSWER HERE

**Q9.7 `[OPTIONAL]` Where is the public "known issues" list so testers do not report the same bug again?**
👉 ANSWER HERE

---

# PART 10. COMMUNICATION PLAN

> 💡 **Why this matters:** Testers who hear from you stay. Silence makes them leave. Ready-made message texts are in Appendix C.

**Q10.1 `[REQUIRED]` Plan your messages.**

| When | Message | Channel | Who sends |
|---|---|---|---|
| Accepted | Welcome + first mission | Email | 👉 |
| Day 3 | Tips + reminder | 👉 | 👉 |
| Weekly | "You said, we did" update | 👉 | 👉 |
| New version | What's new | 👉 | 👉 |
| Incident | Honest explanation + fix time | 👉 | 👉 |
| Week before end | "Beta is ending" | 👉 | 👉 |
| End | Thank you + next steps + offer | 👉 | 👉 |

**Q10.2 `[REQUIRED]` What tone will you use? (Example: friendly, honest, short.)**
👉 ANSWER HERE

**Q10.3 `[REQUIRED]` How do you tell testers about an outage or a mistake?**
Example: "Within 1 hour, say what happened, who is affected, and when we will update next."
👉 ANSWER HERE

---

# PART 11. KEEPING TESTERS ENGAGED (INCENTIVES)

> 💡 **Why this matters:** Testers give you their time. A clear, fair thank-you keeps them active. Never promise a reward you cannot give.

**Q11.1 `[REQUIRED]` What do testers get for helping? (Tick all)**
- [ ] Free access during beta
- [ ] Discount or free months after launch
- [ ] Lifetime deal or "founding member" status
- [ ] Name in credits / badge
- [ ] Early access to new features
- [ ] Gift card or prize
- [ ] Direct line to the team
- [ ] Nothing (the product itself is the reward)
- [ ] Other: 👉

**Q11.2 `[REQUIRED]` What exactly must a tester do to earn it?**
Example: "Use the product 3 times a week and fill 2 surveys."
👉 ANSWER HERE

**Q11.3 `[OPTIONAL]` How will you thank your top 10 testers?**
👉 ANSWER HERE

**Q11.4 `[REQUIRED]` What happens to inactive testers?**
Example: "After 14 days, send one reminder; after 28 days, free the spot."
👉 ANSWER HERE

---

# PART 12. LEGAL, PRIVACY AND SECURITY

> ⚠️ **Important:** This part is a guide, not legal advice. For anything unclear, ask a qualified lawyer. Write `UNKNOWN - ask lawyer by YYYY-MM-DD` if you do not know.

## 12A. Agreements

**Q12.1 `[REQUIRED]` Which agreements do testers accept before joining?**
- [ ] Beta terms of use (says the product may have bugs, may change, may be removed)
- [ ] Privacy policy
- [ ] Confidentiality / NDA (only if you need secrecy)
- [ ] Feedback license (you may use their ideas)
- [ ] Age confirmation (18+ or your minimum age)
- [ ] Recording / screen-share consent (if you record sessions)
- [ ] Other: 👉

Link to each agreement: 👉 ANSWER HERE

**Q12.2 `[REQUIRED]` How is acceptance recorded (checkbox, e-signature)? Where is the proof stored?**
👉 ANSWER HERE

**Q12.3 `[REQUIRED]` Will testers be allowed to talk publicly about the beta?**
- [ ] Yes, freely
- [ ] Yes, but not about certain things: 👉
- [ ] No (confidential)

## 12B. Data and privacy

**Q12.4 `[REQUIRED]` What personal data do you collect?**
| Data | Why you need it | Where it is stored | How long you keep it |
|---|---|---|---|
| Name | 👉 | 👉 | 👉 |
| Email | 👉 | 👉 | 👉 |
| Usage data | 👉 | 👉 | 👉 |
| Payment data | 👉 | 👉 | 👉 |
| Other: 👉 | 👉 | 👉 | 👉 |

**Q12.5 `[REQUIRED]` Which privacy rules apply to your testers? (Tick all that might apply; ask a lawyer if unsure)**
- [ ] GDPR (Europe/UK)
- [ ] CCPA / CPRA (California)
- [ ] COPPA (children under 13, USA)
- [ ] HIPAA (health data, USA)
- [ ] Other country rules: 👉
- [ ] UNKNOWN - ask lawyer by: 👉

**Q12.6 `[REQUIRED]` How can a tester see, export, or delete their data? Who handles the request and how fast?**
👉 ANSWER HERE

**Q12.7 `[REQUIRED]` What happens to tester data when the beta ends?**
- [ ] Moved to the live product
- [ ] Deleted after 👉 days
- [ ] Kept only if tester agrees
- [ ] Other: 👉

## 12C. Security

**Q12.8 `[REQUIRED]` Security checklist**
- [ ] Passwords and secrets are never stored in code or in this document
- [ ] Connections use HTTPS
- [ ] Data is backed up and restore was tested
- [ ] Only people who need access have access
- [ ] Two-step login is on for admin accounts
- [ ] Known security issues were checked (dependency and vulnerability scan)
- [ ] There is a plan for what to do after a data leak (who, what, how fast to tell people)

**Q12.9 `[REQUIRED]` Where do testers report a security problem? 👉**

---

# PART 13. SUCCESS METRICS (HOW YOU KNOW IT IS WORKING)

> **Rule:** Pick few numbers and watch them every week. For each one write the target, where the number comes from, and who checks it.

## 13A. Activation and retention

| Metric | Plain meaning | Target | Where measured | Owner |
|---|---|---|---|---|
| Sign-up to activated | % of sign-ups who reach the "aha moment" (Q6.4) | 👉 | 👉 | 👉 |
| Time to first value | Minutes/days until aha | 👉 | 👉 | 👉 |
| Day-1 retention | % who come back after 1 day | 👉 | 👉 | 👉 |
| Day-7 retention | % who come back after 7 days | 👉 | 👉 | 👉 |
| Day-30 retention | % who come back after 30 days | 👉 | 👉 | 👉 |
| Weekly active testers | Testers who used it this week | 👉 | 👉 | 👉 |

## 13B. Quality

| Metric | Plain meaning | Target | Where measured | Owner |
|---|---|---|---|---|
| Crash-free sessions | % of sessions with no crash | 👉 | 👉 | 👉 |
| Open bugs by severity | Count of S1/S2/S3/S4 | 👉 | 👉 | 👉 |
| Time to fix S1 / S2 | Hours or days | 👉 | 👉 | 👉 |
| Uptime | % of time product is working | 👉 | 👉 | 👉 |
| Support first-reply time | Hours | 👉 | 👉 | 👉 |
| Support resolved rate | % of tickets solved | 👉 | 👉 | 👉 |

## 13C. Satisfaction

| Metric | Plain meaning | Target | Where measured | Owner |
|---|---|---|---|---|
| PMF score | % who say "very disappointed" if product vanished (40%+ is a common good sign) | 👉 | 👉 | 👉 |
| NPS | "Would you recommend us?" 0-10 score | 👉 | 👉 | 👉 |
| CSAT | "How satisfied are you?" 1-5 | 👉 | 👉 | 👉 |
| Feedback response rate | % of testers who answered a survey | 👉 | 👉 | 👉 |

## 13D. Revenue and conversion

| Metric | Plain meaning | Target | Where measured | Owner |
|---|---|---|---|---|
| Beta to paid | % of testers who become paying | 👉 | 👉 | 👉 |
| Willingness to pay | Price testers say they would pay | 👉 | 👉 | 👉 |
| Referral rate | % of testers who invite someone | 👉 | 👉 | 👉 |
| Cost to get one customer | Money spent ÷ customers gained | 👉 | 👉 | 👉 |

**Q13.1 `[REQUIRED]` Which tools collect these numbers?**
Example: "PostHog for usage, Sentry for crashes, Typeform for surveys."
👉 ANSWER HERE

**Q13.2 `[REQUIRED]` Where is the dashboard? (Link) 👉**

**Q13.3 `[REQUIRED]` When do you review numbers? (Example: every Monday at 09:00) 👉**

---

# PART 14. MARKETING AND CUSTOMER ACQUISITION

> 💡 **Why this matters:** Marketing is just telling the right people, in simple words, why your product helps them. Start with 2 or 3 ways to find people and do them well. Do not try everything.

> **Goal:** Turn happy testers into your first 500 customers, and tell the world.

## 14A. Message and positioning

**Q14.1 `[REQUIRED]` Complete this sentence: "For [who], who [problem], [product name] is a [category] that [main benefit]. Unlike [alternative], we [difference]."**
👉 ANSWER HERE

**Q14.2 `[REQUIRED]` Who are your top 3 competitors or alternatives (including "doing nothing")?**
| Alternative | What they do well | Where we are better |
|---|---|---|
| 👉 | 👉 | 👉 |
| 👉 | 👉 | 👉 |
| 👉 | 👉 | 👉 |

**Q14.3 `[REQUIRED]` Write your 3 key messages (short enough to fit in a tweet).**
1. 👉
2. 👉
3. 👉

## 14B. Assets to prepare

**Q14.4 `[REQUIRED]` Tick what is READY and add the link.**
- [ ] Landing page with sign-up: 👉
- [ ] Waitlist: 👉
- [ ] Demo video or GIF: 👉
- [ ] Screenshots: 👉
- [ ] FAQ page: 👉
- [ ] Press / media kit (logo, description, photos): 👉
- [ ] Social media accounts: 👉
- [ ] Email tool set up: 👉
- [ ] Analytics on landing page: 👉

## 14C. Growth engines

**Q14.5 `[REQUIRED]` How will you grow from 10 to 500? Pick your top 2 or 3 and describe the plan.**

| Engine | Use? | Plan (what, how often, who) | Target users from it |
|---|---|---|---|
| Referral program (tester invites a friend) | [ ] | 👉 | 👉 |
| Content (blog, video, tutorials) | [ ] | 👉 | 👉 |
| Social media | [ ] | 👉 | 👉 |
| Communities | [ ] | 👉 | 👉 |
| Email to waitlist | [ ] | 👉 | 👉 |
| Launch sites (Product Hunt etc.) | [ ] | 👉 | 👉 |
| Partnerships / influencers | [ ] | 👉 | 👉 |
| Direct outreach (personal messages) | [ ] | 👉 | 👉 |
| Paid ads | [ ] | 👉 | 👉 |
| Press | [ ] | 👉 | 👉 |

**Q14.6 `[REQUIRED]` What is your budget for acquisition during beta? (Write 0 if none.) 👉**

**Q14.7 `[OPTIONAL]` Referral program details: what does the inviter get? What does the friend get? How is it tracked?**
👉 ANSWER HERE

## 14D. Proof and stories

**Q14.8 `[REQUIRED]` How will you collect testimonials, reviews, and case studies?**
Example: "Ask the happiest 20 testers at week 3, with written permission to use their name and quote."
👉 ANSWER HERE

⚠️ **Honesty rule:** Only publish real quotes from real testers with their permission. Never invent reviews.

## 14E. Public launch moment

**Q14.9 `[REQUIRED]` What is your launch plan?**
| Item | Date | Owner |
|---|---|---|
| Announcement post / email | 👉 | 👉 |
| Launch-site listing | 👉 | 👉 |
| Press outreach | 👉 | 👉 |
| Launch-day support coverage | 👉 | 👉 |

---

# PART 15. PRICING AND MONEY

> 💡 **Why this matters:** "Free" teaches you whether people like it. Money teaches you whether people value it. You need both answers before you launch.

**Q15.1 `[REQUIRED]` Will the beta be free, paid, or mixed?**
- [ ] Free for all
- [ ] Free at first, paid later
- [ ] Paid from day 1
- [ ] Different by stage: 👉

**Q15.2 `[REQUIRED]` What price(s) do you plan after launch? (Write UNKNOWN if still testing.)**
👉 ANSWER HERE

**Q15.3 `[OPTIONAL]` How will you test the price during beta? (Ask directly, show two prices, pre-orders, etc.)**
👉 ANSWER HERE

**Q15.4 `[REQUIRED]` What happens to free testers when the beta ends?**
- [ ] They keep free access for 👉 days/months
- [ ] They get a discount: 👉
- [ ] They must start paying on 👉
- [ ] Other: 👉

**Q15.5 `[OPTIONAL]` Payment tool and refund rule. 👉**

---

# PART 16. SUPPORT AND OPERATIONS

> 💡 **Why this matters:** Growth can break things. Before you invite more people, check that your servers, costs, and support time can handle them.

**Q16.1 `[REQUIRED]` How can testers get help? (Link / email / chat) 👉**

**Q16.2 `[REQUIRED]` Support hours and time zone. 👉**

**Q16.3 `[REQUIRED]` Prepare answers for the top 10 questions you expect.**
| # | Question | Answer |
|---|---|---|
| 1 | 👉 | 👉 |
| 2 | 👉 | 👉 |
| 3 | 👉 | 👉 |

**Q16.4 `[REQUIRED]` Can the system handle the next ladder step? (Servers, limits, AI costs, support time.)**
| Ladder step | Capacity checked? | Limit found | Action if over limit |
|---|---|---|---|
| 50 | [ ] | 👉 | 👉 |
| 100 | [ ] | 👉 | 👉 |
| 250 | [ ] | 👉 | 👉 |
| 500 | [ ] | 👉 | 👉 |

**Q16.5 `[REQUIRED]` Monthly cost of running the beta (hosting, tools, AI usage, support). 👉**

---

# PART 17. AI-AGENT WORKFLOW (HOW AI HELPS RUN THE BETA)

> **Skip with `N/A` if you do not use AI agents.** If you do, write clear rules so the AI is helpful and safe.

**Q17.1 `[REQUIRED]` Which beta jobs will AI agents do?**
| Job | Agent / tool | What it can read | What it can change | Human check |
|---|---|---|---|---|
| Sort and label feedback | 👉 | 👉 | 👉 | 👉 |
| Draft support replies | 👉 | 👉 | 👉 | 👉 |
| Summarize weekly feedback | 👉 | 👉 | 👉 | 👉 |
| Triage bugs / suggest severity | 👉 | 👉 | 👉 | 👉 |
| Write fixes / tests | 👉 | 👉 | 👉 | 👉 |
| Watch metrics and alert | 👉 | 👉 | 👉 | 👉 |
| Draft updates and posts | 👉 | 👉 | 👉 | 👉 |

**Q17.2 `[REQUIRED]` Hard limits for agents (never do without a human): 👉**
Example: "Never send emails to all testers, never delete data, never change prices, never see passwords."

**Q17.3 `[REQUIRED]` How will you know an agent made a mistake? Who reviews its work and how often? 👉**

**Q17.4 `[OPTIONAL]` Weekly agent routine.**
Example: "Monday 09:00: summarize last week's feedback into 5 themes, list top 10 bugs, flag any metric below target."
👉 ANSWER HERE

---

# PART 18. GO / NO-GO GATES

> **How to use:** Before moving to the next stage or ladder step, tick every box. If one box cannot be ticked, you do NOT go. Write the reason and the fix date.

## ⛔ Gate 1: Closed Beta to Open Beta
- [ ] Target number of Closed Beta users reached (Q2.5)
- [ ] 0 open S1 bugs and no more than 👉 open S2 bugs
- [ ] Day-7 retention is at least 👉
- [ ] Main user flow works for at least 90% of testers (or your number: 👉)
- [ ] Support can keep up with the reply times in Q9.1
- [ ] Capacity checked for the next step (Q16.4)
- [ ] Legal and privacy items in Part 12 complete
- [ ] Decision by (name): 👉   Date: 👉

## ⛔ Gate 2: Open Beta to Public Launch
- [ ] Target user number reached
- [ ] PMF score is at least 👉
- [ ] 0 open S1 and 👉 or fewer S2 bugs
- [ ] Price decided (Part 15)
- [ ] Launch assets ready (Q14.4)
- [ ] Rollback plan tested
- [ ] Decision by (name): 👉   Date: 👉

## ⛔ Gate 3: Each Ladder Step (50 / 100 / 250 / 500)
Copy this box for every step.
- [ ] Health check from Q2.7 passed
- [ ] Capacity for the next step confirmed
- [ ] No unresolved S1 bugs
- [ ] Support backlog under control
- [ ] Decision by (name): 👉   Date: 👉

**Gate decision log**
| Date | Gate | Result (Go / No-go / Go with conditions) | Reason | Who decided |
|---|---|---|---|---|
| 👉 | 👉 | 👉 | 👉 | 👉 |

---

# PART 19. RISKS

> 💡 **Why this matters:** A risk is something that might go wrong. Thinking about it now means you have a plan instead of a panic later.

**Q19.1 `[REQUIRED]` List the top 5 things that could go wrong and your plan.**

| # | Risk | How likely (Low/Med/High) | How bad (Low/Med/High) | What we will do |
|---|---|---|---|---|
| 1 | Too few testers sign up | 👉 | 👉 | 👉 |
| 2 | Testers sign up but never use it | 👉 | 👉 | 👉 |
| 3 | Serious bug or data loss | 👉 | 👉 | 👉 |
| 4 | Product costs too much to run | 👉 | 👉 | 👉 |
| 5 | 👉 | 👉 | 👉 | 👉 |

---

# PART 20. ENDING THE BETA AND LAUNCHING

> 💡 **Why this matters:** A beta needs a clear ending. Without one, testers are confused about what happens to their access and data.

**Q20.1 `[REQUIRED]` How do you decide the beta is over? (Date, numbers, or both.) 👉**

**Q20.2 `[REQUIRED]` What happens on the last day? Tick and assign.**
- [ ] Send thank-you message and rewards
- [ ] Move testers to live product / paid plan
- [ ] Remove "beta" labels
- [ ] Turn off beta-only features or flags
- [ ] Publish final known-issues list and release notes
- [ ] Archive feedback and data per Q12.7
- [ ] Announce publicly

**Q20.3 `[REQUIRED]` Plan for customers 100 to 500 after public launch.**
Example: "Keep the referral loop, publish 2 case studies, post weekly updates, email waitlist."
👉 ANSWER HERE

**Q20.4 `[REQUIRED]` Which testers become your first advocates (customers who tell others)? How will you stay in touch? 👉**

---

# PART 21. RETROSPECTIVE (FILL AT THE END)

**Q21.1 What went well? 👉**
**Q21.2 What went badly? 👉**
**Q21.3 What surprised us? 👉**
**Q21.4 Did we hit the goals in Q2.3? (Show the numbers.) 👉**
**Q21.5 What will we change next time? 👉**
**Q21.6 What should be updated in this template for future projects? 👉**

---

# PART 22. WEEKLY TRACKER

> Copy one row per week. Keep it short.

| Week | Date | Total users | New | Active | Day-7 retention | Open S1/S2 | PMF / NPS | Top issue | Next week's focus |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 |
| 2 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 |
| 3 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 |
| 4 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 | 👉 |

---

# PART 23. FINAL CHECKLIST AND SELF-CHECK

## 23A. Before you start the beta
- [ ] Parts 0 to 6 complete
- [ ] Part 3 readiness gate (Gate 0) passed
- [ ] Parts 8 to 12 complete
- [ ] Metrics and dashboard working (Part 13)
- [ ] Emergency plan written and shared (Q9.6)
- [ ] Welcome message tested by sending it to yourself
- [ ] Sign-up form tested end to end
- [ ] Someone else read this document and understood it

## 23B. Self-check for the person or AI agent
Answer YES or NO. Every NO needs a fix before you start.
1. Did I answer every `[REQUIRED]` question? 👉
2. Are there any made-up numbers? (Should be NO.) 👉
3. Does every target have a date, an owner, and a way to measure it? 👉
4. Is there one clear definition of "customer" used everywhere? 👉
5. Could a stranger run this beta using only this file? 👉
6. Are all legal items checked or marked UNKNOWN with a date? 👉
7. Is every link working? 👉
8. Are there any passwords, keys, or private data in this file? (Should be NO.) 👉

## 23C. Approval
| Name | Role | Date | Approved? |
|---|---|---|---|
| 👉 | Owner | 👉 | [ ] |
| 👉 | Reviewer | 👉 | [ ] |

---

# GLOSSARY (SIMPLE WORDS)

| Word | Meaning |
|---|---|
| Beta | A test version of your product used by real people before the official launch |
| Alpha | The first test, done by your own team |
| Closed beta | Only invited people can join |
| Open beta | Anyone can join |
| Tester | A person who tries the product and gives feedback |
| Bug | Something that does not work as it should |
| Severity | How serious a bug is |
| Triage | Sorting problems by how urgent they are |
| Gate | A checkpoint you must pass before moving on |
| Activation | The moment a user first gets real value |
| Retention | People who come back |
| NPS | A score for "would you recommend us?" |
| PMF | Product-market fit: people really want your product |
| Rollback | Going back to the previous working version |
| Waitlist | A list of people waiting to get in |
| Referral | A tester inviting a friend |
| NDA | A promise to keep things secret |
| GDPR / CCPA | Privacy laws in Europe/UK and California |
| AI agent | A computer program that does tasks for you using AI |

---

# APPENDIX A. WORKED EXAMPLE (A FILLED-IN MINI VERSION)

> **How to use:** This shows what good answers look like. It is a made-up product. Never copy it as your own answers.

**Product:** "LeafBuddy", a phone app that reminds people to water their plants.

| Question | Example answer |
|---|---|
| Q1.1 One sentence | A phone app that reminds people when to water each of their plants. |
| Q1.2 Who is it for | Busy adults aged 25 to 40 who own 3 or more house plants. |
| Q1.5 Must-work features | 1. Add a plant. 2. Get a watering reminder. 3. Mark "watered". |
| Q1.6 Known broken | Plant photo recognition is slow. Android 11 is not supported. |
| Q2.2 Main goal | Prove that people keep using it after 30 days. |
| Q2.3 Success | 1. 40% still active on day 30. 2. PMF score of 40% or more. 3. 100 testers by 2026-12-15. |
| Q2.4 Emergency brakes | Any data loss, crash-free sessions below 95%, or any privacy leak. |
| Q2.6 "Customer" means | Signed up AND added one plant AND got one reminder. |
| Q2.7 Ladder step 1 | 10 testers, friends and family, by 2026-11-01. Health check: all 10 finish the first mission with no S1 bug. |
| Q4.1 Roles | Founder = owner, product, support. AI agent = triage and drafts. Freelancer = QA. |
| Q5.5 Sources | Friends 10, waitlist 40, Reddit plant community 30, referrals 20. |
| Q6.3 First mission | Add one plant and set a reminder (3 minutes). |
| Q6.4 Aha moment | The first reminder arrives and the tester waters the plant. |
| Q9.6 2 a.m. S1 | Alert goes to the founder's phone. First action: pause new sign-ups, then roll back to last build. |
| Q11.1 Reward | Founding member badge and 6 months free after launch. |
| Q12.7 Data after beta | Moved to the live app. Testers can delete their data any time via Settings. |
| Q13A Day-7 retention target | 50%, measured in PostHog, checked every Monday by the founder. |
| Q14.6 Budget | USD 0. Only free channels. |
| Q15.4 After beta | Testers keep a 30% discount for the first year. |
| Q17.2 Agent limits | Never emails all testers, never deletes data, never changes prices. |

---

# APPENDIX B. AI-AGENT PROMPTS (COPY, PASTE, RUN)

> Replace the `{curly brackets}` with your real details. Always read what the AI gives you before accepting it.

**B1. Fill a part from my notes**
```
You are helping fill Beta_Program.md. Here are my notes: {paste notes}.
Fill only Part {number}. Keep the question IDs. Use plain language.
If my notes do not answer a question, write "UNKNOWN - needs: {what is missing}". Never invent numbers, dates, names, or links.
```

**B2. Find gaps**
```
Read Beta_Program.md. List every [REQUIRED] question that is still "👉 ANSWER HERE" or UNKNOWN.
Group the list by Part. For each, say in one sentence what information I need to provide.
```

**B3. Check for contradictions**
```
Read Beta_Program.md. Check that: (1) my definition of "customer" in Q2.6 is used consistently; (2) dates in Q2.5, Q2.7 and Part 20 do not clash; (3) targets in Parts 2, 13 and 18 agree; (4) severity times in Q9.1 match the support hours in Q16.2. Report each conflict with the question IDs.
```

**B4. Beginner-readability test**
```
Read Beta_Program.md as if you are a 10-year-old. Point to every sentence or word that is hard to understand and suggest a simpler version. Do not change the structure.
```

**B5. Weekly feedback summary**
```
Here is this week's feedback: {paste or link}. Group it into at most 5 themes. For each theme give: how many testers mentioned it, one short example (anonymous), a suggested severity (S1-S4), and a suggested next step. Mark anything about safety, privacy, or data loss as URGENT at the top.
```

**B6. Bug triage**
```
Here is a bug report: {paste}. Suggest a severity using the table in Q9.1, say if it duplicates a known issue in {link}, list the missing information I should ask the tester for, and draft a short friendly reply. Do not send anything.
```

**B7. Gate review**
```
Read Part 18 and my latest numbers: {paste or link}. For Gate {1, 2 or 3}, mark each box as PASS, FAIL, or NOT ENOUGH DATA with the number you used. Give a final recommendation (Go / No-go / Go with conditions) and the reason. A human makes the final decision.
```

**B8. Final audit before launch**
```
Run the Self-Check in Part 23B on Beta_Program.md. Answer each of the 8 items with YES or NO and evidence. Also scan for passwords, keys, or private personal data and report anything found.
```

---

# APPENDIX C. READY-TO-USE MESSAGE AND SURVEY COPY

> Change the words in `{curly brackets}`. Keep the tone friendly and honest.

### C1. Welcome email
**Subject:** Welcome to the {Product} beta!
Hi {Name},
Thank you for joining the {Product} beta. You are one of our first {number} testers.
**Your link:** {link}
**Your first mission (about {minutes} minutes):** {first mission from Q6.3}
Things to know: this is an early version, so something may break. That is why we need you. If you find a problem, tell us here: {feedback link}. You will find known issues here: {link}.
Need help? Just reply to this email.
Thanks,
{Your name}

### C2. Day-3 nudge (if not started)
**Subject:** Need a hand getting started?
Hi {Name}, we noticed you have not tried {Product} yet. It takes about {minutes} minutes: {first mission}. Stuck on something? Reply and we will help.

### C3. Weekly "You said, we did" update
**Subject:** What we changed this week
Hi {Name},
**You said:** {feedback 1}. **We did:** {fix 1}.
**You said:** {feedback 2}. **We did:** {fix 2}.
**Coming next:** {next focus}.
**Still broken (we know!):** {known issue}.
Thank you for helping. Reply anytime with your ideas.

### C4. Incident message
**Subject:** Update on {issue}
Hi {Name}, on {date} at {time} {what happened in plain words}. It affected {who}. {Data was / was not affected.} We are {doing what}. Our next update will be at {time}. We are sorry, and thank you for your patience.

### C5. Beta ending
**Subject:** The {Product} beta is ending on {date}
Hi {Name}, thank you for being part of it. Here is what happens next: {Q15.4 answer}. Your data will {Q12.7 answer}. As a thank-you: {reward from Q11.1}. One last favor: {exit survey link}, it takes {minutes} minutes.

### C6. Referral invite (tester shares with a friend)
"I have been testing {Product}, it helps with {problem}. You can join here: {referral link}. You get {friend reward}."

### C7. Testimonial permission request
Hi {Name}, may we share your comment: "{quote}" on our website? We would show {first name and city / full name / anonymous}. Reply YES to agree or NO to decline. You can change your mind any time.

### C8. Survey question bank (pick 5 to 10 per survey)
**Welcome survey:** What problem made you sign up? How do you solve it today? What would make this a success for you?
**First-experience survey:** Were you able to finish the first mission? (Yes / Partly / No) What was confusing? Rate setup from 1 (hard) to 5 (easy).
**Mid-beta check-in:** What do you use most? What do you never use? What is missing? What is the most annoying thing?
**PMF survey:** How would you feel if you could no longer use {Product}? (Very disappointed / Somewhat disappointed / Not disappointed). What is the main benefit you get? Who do you think would benefit most? How can we improve it for you?
**NPS:** How likely are you to recommend {Product} to a friend? (0-10). What is the main reason for your score?
**Exit survey:** Did you get value? What made you stay or stop? What would you pay for it, if anything? May we contact you for a short chat? (Yes / No)

---
*End of template. Template version: 1.1 (added worked example, AI prompts, message copy)*
