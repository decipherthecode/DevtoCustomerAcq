# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What is this?** A "retrospective" is a look back at a finished project. You answer questions about what happened, what you learned, and what you will do differently next time. This file covers one product from **the first idea → building with AI → testing → launch → your first 500 customers**.

**Who fills it?** One person (the founder or project owner). AI agents may help by pulling facts from logs, chats, and dashboards, but **a human must read and confirm every answer**.

**How long does it take?** About 2-4 hours if you gather your numbers first (see "Before you start").

## Before you start (gather these 7 things)

- [ ] The project folder or repository link
- [ ] Your original plan or idea notes (even rough ones)
- [ ] Your list of bugs / issues / tasks
- [ ] Your AI tool logs, chat history, or prompt notes
- [ ] Your bills (AI tools, hosting, ads, other tools)
- [ ] Your customer list or analytics dashboard (signup dates, channels)
- [ ] Your support inbox or feedback notes

## The 8 rules

1. **Copy this file first.** Save the copy as `Project_Retrospective_<ProjectName>_<YYYY-MM-DD>.md`. Never type into the blank template.
2. **Go in order.** Fill Part 0, then Parts 1-18. Fill Part 2 (Scorecard) **last**.
3. **Never leave a blank.** If you do not know, write `UNKNOWN` and add how you could find out. If it does not apply, write `N/A` and say why in a few words.
4. **No blame.** Talk about what happened and why, not who is "bad." AI tools and past-you are not villains. Fix the process, not the person.
5. **Use facts first, feelings second.** Numbers, dates, and links beat "I think." Feelings are welcome, but label them: *(Feeling)*.
6. **Dates are written like this:** `2026-10-19` (year-month-day).
7. **Never paste secrets.** No passwords, API keys, customer emails, or private data. Write `[REMOVED]` instead.
8. **Short is fine.** One clear sentence beats a long paragraph.

## How to answer each type of question

| You see this | What to do | Example |
|---|---|---|
| `[ ]` checkbox | Change to `[x]` for every answer that is true | `[x] We wrote a plan` |
| `Score 1-5` | Circle one number by writing it after "Score:" (see score guide below) | `Score: 4` |
| `___` blank or `Your answer:` | Write a short answer (1-3 sentences) | `Your answer: We ran out of time in testing.` |
| Table | Add one row per item. Add more rows if you need them | see tables below |
| `Evidence:` | Paste a link, file name, or number that proves your answer | `Evidence: dashboard link` |

### Score guide (use the same meaning everywhere)

| Score | Meaning |
|---|---|
| 1 | Went badly. We would not repeat this. |
| 2 | Weak. Many problems. |
| 3 | Okay. Some good, some bad. |
| 4 | Good. Small problems only. |
| 5 | Great. We would copy this next time. |

### Example of a filled-in answer

> **Q: Did we write down what "done" looks like before building?**
> `[x] Yes  [ ] Partly  [ ] No`
> Score: 4
> Your answer: We wrote 5 "must-have" features in a note. We forgot to write what "good enough" means for speed.
> Evidence: `notes/scope.md`

## When you are finished (Done check)

- [ ] Every question has an answer, `UNKNOWN`, or `N/A`
- [ ] Part 0 (Metadata) is complete so this file can be found by search
- [ ] Part 2 (Scorecard) is filled in last
- [ ] At least 3 Lessons (Part 15) and 3 Action Items (Part 16) are written
- [ ] No passwords, keys, or private customer data are in the file
- [ ] The file is saved in: `Documentation management and institutional knowledge/Project Retrospectives/`

## Tiny dictionary (plain words)

| Word | Meaning |
|---|---|
| Retrospective | Looking back on a project to learn from it |
| AI agent | An AI tool that does tasks for you (writes code, tests, researches) |
| Prompt | The instructions you give an AI |
| Hallucination | When AI confidently says something that is not true |
| MVP | Minimum Viable Product: the smallest version that is useful |
| QA | Quality Assurance: checking that the product works |
| Launch | The day real customers can start using the product |
| Activation | A new customer does the first useful thing in your product |
| Retention | Customers keep coming back |
| Churn | Customers who stop using or paying |
| Root cause | The real reason a problem happened |
| CAC | Customer Acquisition Cost: money spent to get one customer |

---

# PART 0: DOCUMENT INFO (FILL FIRST)

> This block lets you search hundreds of retrospectives later. Keep the format exactly.

```yaml
retro_id: RETRO-YYYY-NNN            # example: RETRO-2026-014
project_name: ""
product_type: ""                    # web app / mobile app / AI product / API / other
version_at_retro: ""                # example: v1.3.0
retro_date: YYYY-MM-DD
filled_by: ""
ai_tools_used: []                   # example: [Claude, Cursor, GitHub Copilot]
project_start_date: YYYY-MM-DD
launch_date: YYYY-MM-DD
date_of_500th_customer: YYYY-MM-DD  # or "not reached"
final_status: ""                    # Reached 500 / In progress / Paused / Stopped
overall_score_1_to_5: 0
pricing_model: ""                   # free / one-time / subscription / usage / ads
had_security_incident: false        # true / false
had_major_outage: false             # true / false
tags: []                            # example: [saas, b2c, ai-heavy, solo]
related_docs: []                    # links to plan, spec, dashboards
template_version: 1.1
```

---

# PART 1: PROJECT SNAPSHOT

**Why this matters:** Anyone reading this in two years should understand the project in 60 seconds.

**1.1** In one sentence, what does the product do and for whom?
Your answer:

**1.2** What problem did it solve? (Write it like you are explaining to a friend.)
Your answer:

**1.3** What was the project goal? (Pick one main goal.)
- [ ] Make money
- [ ] Learn / test an idea
- [ ] Solve my own problem
- [ ] Serve a client or employer
- [ ] Other: ___

**1.4** Final result in one line: did we reach 500 customers?
`[ ] Yes  [ ] Not yet  [ ] Stopped before that`
Your answer:

**1.5** Key facts

| Item | Planned | Actual |
|---|---|---|
| Start date | | |
| Launch date | | |
| Date of 500th customer | | |
| Total build time (weeks) | | |
| Total money spent (currency: ___) | | |
| Number of people involved (humans) | | |
| Number of AI agents / tools involved | | |

**1.6** Links (write `N/A` if none): code repo ___ | live product ___ | plan ___ | dashboard ___ | support inbox ___

---

# PART 2: SCORECARD AT A GLANCE (FILL THIS LAST)

> Copy your scores from the later parts. Be honest.

| Area | Score 1-5 | One-line reason |
|---|---|---|
| Part 3: Idea & Planning | | |
| Part 4: Design & AI-Assisted Build | | |
| Part 5: Testing & QA | | |
| Part 6: Launch | | |
| Part 7: First 500 Customers | | |
| Part 8: AI Collaboration | | |
| Part 9: Time & Money | | |
| Part 10: Security & Privacy | | |
| Part 11: Pricing & Revenue | | |
| Part 12: Team & Wellbeing | | |
| Part 13: Post-Launch Incidents | | |
| **Overall** | | |

**2.1** Would we do this project again, knowing what we know now?
`[ ] Yes, same way  [ ] Yes, but differently  [ ] No`
Why:

**2.2** The single biggest win (one sentence):

**2.3** The single biggest problem (one sentence):

**2.4** If a new person only reads this box, the one thing they must know is:

---

# PART 3: PHASE 1, IDEA & PLANNING

**Why this matters:** Most project trouble begins here. Unclear goals become expensive mistakes later.

**3.1** Before building, did we write down these things? (Check all that are true.)
- [ ] Who the customer is
- [ ] What problem we solve
- [ ] A list of must-have features
- [ ] A list of "not now" features
- [ ] What "success" looks like with numbers
- [ ] A deadline
- [ ] A budget
- [ ] The biggest risks

**3.2** Did we talk to real potential customers before building?
`[ ] Yes, 5 or more  [ ] Yes, 1-4  [ ] No`
What did we learn from them?
Your answer:

**3.3** Was the goal clear to everyone (including the AI agents)?
Score: ___
Your answer:

**3.4** Scope check

| Question | Answer |
|---|---|
| How many features did we plan at the start? | |
| How many did we ship at launch? | |
| How many did we add after the plan started? | |
| How many did we cut? | |

**3.5** What was our target for the first 500 customers? (Check what we wrote down before launch.)
- [ ] Number of customers by a date: ___
- [ ] Where customers would come from: ___
- [ ] Price or business model: ___
- [ ] None of these (we guessed)

**3.6** Were our time and money estimates close to reality?
Score: ___
Biggest estimate that was wrong, and why:

**3.7** Which risks did we list, and which of them really happened?

| Risk we listed | Did it happen? (Yes/No) | What we did |
|---|---|---|
| | | |

**3.8** What was a surprise that nobody listed as a risk?
Your answer:

**3.9** Planning verdict
- What worked well:
- What we should change next time:
- Score for Part 3: ___

---

# PART 4: PHASE 2, DESIGN & AI-ASSISTED BUILD

**Why this matters:** This is where AI speed can create fast progress or fast mess.

## 4A. Design and structure

**4.1** Before coding, did we decide these? (Check all that are true.)
- [ ] The main screens or user flow
- [ ] How the system is put together (simple drawing is fine)
- [ ] Which tools / languages / services to use
- [ ] How data is stored
- [ ] How we handle login and private data
- [ ] How the product would grow if many people joined

**4.2** What were the 3 biggest technical or design decisions? Was each one right?

| Decision | Why we chose it | Right call? (Yes/Partly/No) |
|---|---|---|
| 1. | | |
| 2. | | |
| 3. | | |

**4.3** Did we have to rebuild or redo big parts?
`[ ] No  [ ] Small parts  [ ] Big parts`
What caused it?
Your answer:

## 4B. Building with AI

**4.4** How was the work split between humans and AI?

| Task type | Mostly human | Mixed | Mostly AI |
|---|---|---|---|
| Planning / choosing features | [ ] | [ ] | [ ] |
| Design | [ ] | [ ] | [ ] |
| Writing code | [ ] | [ ] | [ ] |
| Writing tests | [ ] | [ ] | [ ] |
| Writing docs | [ ] | [ ] | [ ] |
| Fixing bugs | [ ] | [ ] | [ ] |
| Deploying / hosting | [ ] | [ ] | [ ] |

**4.5** Did we give the AI clear written rules or context? (Check all that are true.)
- [ ] A project instructions file (example: `AGENTS.md` or `CLAUDE.md`)
- [ ] A spec or plan written before asking AI to build
- [ ] Coding style rules
- [ ] A list of things the AI must never do
- [ ] None of these

**4.6** Quality of the code and structure
Score: ___
- Is the code easy for a new person to understand? `[ ] Yes [ ] Somewhat [ ] No`
- Did we leave shortcuts we must fix later ("tech debt")? `[ ] None [ ] A few [ ] Many`
- List the top 3 shortcuts:

**4.7** What slowed building the most? (Pick up to 3.)
- [ ] Unclear requirements
- [ ] AI misunderstood what we wanted
- [ ] AI wrote code that did not work
- [ ] Too many changes of mind
- [ ] Tool or service problems
- [ ] Running out of time or energy
- [ ] Waiting on others
- [ ] Other: ___

**4.8** Build timeline

| Milestone | Planned date | Actual date | Why different? |
|---|---|---|---|
| First working version | | | |
| All must-have features done | | | |
| Ready for testing | | | |

**4.9** Build verdict
- What worked well:
- What we should change next time:
- Score for Part 4: ___

---

# PART 5: PHASE 3, TESTING & QA

**Why this matters:** Bugs found before launch cost little. Bugs found by customers cost trust.

**5.1** What kinds of testing did we do? (Check all that are true.)
- [ ] We tried it ourselves by hand
- [ ] Automatic tests (code checks itself)
- [ ] Tested on different devices / browsers
- [ ] Tested with slow internet
- [ ] Security check (logins, private data)
- [ ] Speed check with many users at once
- [ ] Real people outside the team tried it
- [ ] AI reviewed the code for problems
- [ ] We did not test enough

**5.2** Bug numbers

| Question | Count |
|---|---|
| Bugs found before launch | |
| Bugs found after launch by customers | |
| Serious bugs (product broken, data lost, or money wrong) | |
| Bugs that AI-written code caused | |
| Bugs still open today | |

**5.3** Which bugs hurt the most? Describe the top 3.

| Bug | Found by (us/AI/customer) | Real cause | How we fixed it |
|---|---|---|---|
| 1. | | | |
| 2. | | | |
| 3. | | | |

**5.4** Did we have a clear "ready to launch" checklist?
`[ ] Yes, and we followed it  [ ] Yes, but we skipped parts  [ ] No`
Which items did we skip, and why?

**5.5** What would have caught our worst bug earlier?
Your answer:

**5.6** Did we ever launch (or deploy) something we were not sure about?
`[ ] No  [ ] Yes`
If yes, what happened?

**5.7** Testing verdict
- What worked well:
- What we should change next time:
- Score for Part 5: ___

---

# PART 6: PHASE 4, LAUNCH

**Why this matters:** Launch day is when the plan meets the real world.

**6.1** Were we ready? (Check all that are true.)
- [ ] The product worked on launch day
- [ ] A way to take payment (if needed) was tested
- [ ] A way for customers to get help was ready
- [ ] A way to see errors and problems was ready
- [ ] A way to go back to the old version was ready
- [ ] Privacy policy and terms were in place
- [ ] A backup of data existed
- [ ] We told people about the launch

**6.2** What launch style did we use?
`[ ] Private test group first  [ ] Small public launch  [ ] Big public launch  [ ] Quiet launch`

**6.3** Launch day and week 1

| Question | Answer |
|---|---|
| Launch date | |
| Visitors in week 1 | |
| Signups in week 1 | |
| Problems on launch day (count) | |
| Time the product was down (minutes) | |
| Biggest launch-day problem | |

**6.4** What went better than expected?
Your answer:

**6.5** What went worse than expected?
Your answer:

**6.6** If we could repeat launch day, what are the first 3 things we would change?
1.
2.
3.

**6.7** Launch verdict
- What worked well:
- What we should change next time:
- Score for Part 6: ___

---

# PART 7: PHASE 5, FIRST 500 CUSTOMERS

**Why this matters:** This part proves whether people actually want the product.

**Definitions (write them here so everyone counts the same way):**
- A "customer" in this project means: ___ (example: "someone who paid at least once" or "someone who signed up and used it once")
- "Activated" means: ___ (example: "created their first project")
- "Active" means: ___ (example: "used the product at least once in 7 days")

## 7A. Milestones

| Milestone | Date | Days since launch | What helped or blocked? |
|---|---|---|---|
| 1st customer | | | |
| 25th customer | | | |
| 100th customer | | | |
| 250th customer | | | |
| 500th customer | | | |

**7.1** Was growth steady or in bursts? What caused the bursts?
Your answer:

**7.2** If we have not reached 500: how many customers do we have, and what is the main thing blocking us?
Your answer:

## 7B. Where customers came from and what they cost

| Channel (example: friends, social media, search, ads, partners, communities, email) | Customers | Money spent | Cost per customer (spent ÷ customers) | Keep, stop, or test more? |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |
| **Total** | | | | |

**7.3** Which channel gave the best customers (not just the most)?
Your answer:

**7.4** Which channel wasted the most time or money?
Your answer:

## 7C. Did customers actually use it and stay?

| Metric | Number | How we counted |
|---|---|---|
| Signups | | |
| Activated customers (did the first useful action) | | |
| Activation % (activated ÷ signups) | | |
| Still active after 7 days % | | |
| Still active after 30 days % | | |
| Customers who left (churned) in first 90 days | | |
| Churn % | | |
| Revenue so far (write `N/A` if free) | | |

**7.5** Where do new customers get stuck or quit? (Name the step.)
Your answer:

**7.6** What did we change to improve activation or retention, and did it work?

| Change | Date | Result |
|---|---|---|
| | | |

## 7D. Support and feedback

| Metric | Number |
|---|---|
| Support requests received | |
| Average time to first reply | |
| Requests solved | |
| Customers who said they love it (count or quotes, no private data) | |

**7.7** Top 5 things customers asked for or complained about

| # | Theme | How many times | What we did |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |

**7.8** What do customers say is the best thing? (Use their words, remove names.)
Your answer:

**7.9** Did we hear anything that proves our original idea was wrong or incomplete?
Your answer:

**7.10** Part 7 verdict
- What worked well:
- What we should change next time:
- Score for Part 7: ___

---

# PART 8: AI COLLABORATION REVIEW

**Why this matters:** This is how you learn to work better with AI on the next project.

## 8A. Tools and agents used

| AI tool or agent | Used for | Worked well? (1-5) | Main problem | Use again? (Y/N) |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

## 8B. Prompts that worked and prompts that failed

> Save only reusable prompts. Remove private data.

**Prompts that worked well (add up to 5):**

| Goal | The prompt (or its short form) | Why it worked |
|---|---|---|
| | | |

**Prompts that failed (add up to 5):**

| Goal | The prompt (or its short form) | What went wrong | Better version |
|---|---|---|---|
| | | | |

**8.1** What kind of instruction gives the best result from AI? (Examples: clear steps, examples, small tasks.)
Your answer:

## 8C. Human review and AI mistakes

**8.2** How often did humans have to fix, check, or reject AI output?
`[ ] Rarely  [ ] Sometimes  [ ] Often  [ ] Almost always`

**8.3** Which AI mistakes happened? (Check all that are true and add a count if you know.)
- [ ] Made-up facts, functions, or files (hallucinations) ___ times
- [ ] Code that looked right but was wrong ___ times
- [ ] Ignored our rules ___ times
- [ ] Changed things we did not ask ___ times
- [ ] Broke something that worked before ___ times
- [ ] Left insecure code or private data exposed ___ times
- [ ] Stopped halfway or claimed "done" when it was not ___ times
- [ ] Other: ___

**8.4** Biggest AI mistake and what it cost us (time, money, trust):
Your answer:

**8.5** Which checks should always be done by a human next time? (Check all that apply.)
- [ ] Security and private data
- [ ] Payments and money maths
- [ ] Deleting or changing real data
- [ ] Customer messages
- [ ] Launch approval
- [ ] Legal and privacy text
- [ ] Other: ___

**8.6** What did the AI do better than we expected?
Your answer:

## 8D. AI cost and time saved

| Item | Number |
|---|---|
| Total AI spend (subscriptions + usage), currency ___ | |
| Estimated hours AI saved us | |
| Estimated hours we lost fixing AI mistakes | |
| Net hours saved (saved − lost) | |
| How we estimated this (one line) | |

**8.7** Was the AI cost worth it?
`[ ] Yes, clearly  [ ] Probably  [ ] Not sure  [ ] No`

**8.8** AI verdict
- What worked well:
- What we should change next time:
- Score for Part 8: ___

---

# PART 9: TIME & MONEY

**9.1** Money: plan versus real

| Cost type | Planned | Actual | Difference |
|---|---|---|---|
| AI tools | | | |
| Hosting / servers | | | |
| Other software and services | | | |
| Marketing / ads | | | |
| People / freelancers | | | |
| Legal / other | | | |
| **Total** | | | |

**9.2** Time: plan versus real (in weeks)

| Phase | Planned | Actual |
|---|---|---|
| Idea & planning | | |
| Design & build | | |
| Testing | | |
| Launch | | |
| Reaching customer #500 | | |

**9.3** Biggest reason time or money went off plan:
Your answer:

**9.4** If we do this again, what is the realistic cost and time?
Your answer:

**9.5** Verdict: Score for Part 9: ___ Why:

---

# PART 10: SECURITY & PRIVACY REVIEW

**Why this matters:** One leak or hack can end a young product. AI-written code makes this check more important, not less.

**10.1** What private data does the product handle? (Check all that are true.)
- [ ] Names and emails
- [ ] Passwords or logins
- [ ] Payment details (handled by a payment company, not us)
- [ ] Health, children's, or other sensitive data
- [ ] Customer files or messages
- [ ] Data customers type into AI features
- [ ] None of these

**10.2** Which protections did we put in place before launch? (Check all that are true.)
- [ ] Logins are protected (no passwords stored in plain text)
- [ ] Secret keys are stored safely, not inside the code
- [ ] Each customer can only see their own data
- [ ] Data is encrypted when sent and when stored
- [ ] Regular backups exist and we tested restoring one
- [ ] We checked tools and libraries for known weak spots
- [ ] A human reviewed AI-written code that touches private data
- [ ] We have a privacy policy and terms people can read
- [ ] We know which laws apply (example: GDPR, CCPA, children's privacy)
- [ ] We can delete a customer's data if they ask

**10.3** Did we ever find any of these problems? (Check all that are true and describe.)
- [ ] A secret key or password was exposed by mistake
- [ ] A customer could see another customer's data
- [ ] Private data was sent to an AI tool that should not have received it
- [ ] A weak spot was found by us, AI, or an outsider
- [ ] None
Your answer:

**10.4** Security score and review

| Question | Answer |
|---|---|
| Date of our last security check | |
| Who did it (us / AI / outside expert) | |
| Serious weaknesses found | |
| Weaknesses still open today | |

**10.5** What is the biggest privacy or security risk we are still carrying?
Your answer:

**10.6** Security verdict
- What worked well:
- What we should change next time:
- Score for Part 10: ___

---

# PART 11: PRICING & REVENUE

> If the product is free, write `N/A: free product` for the questions that do not apply, but still answer 11.1, 11.6, and 11.7.

**Why this matters:** Customers who pay tell you the truth about your product's value.

**11.1** How did we decide the price?
- [ ] Looked at competitors
- [ ] Asked customers what they would pay
- [ ] Calculated our costs and added profit
- [ ] Guessed
- [ ] The product is free (reason: ___)

**11.2** Pricing summary

| Item | Answer |
|---|---|
| Business model (one-time, monthly, usage-based, ads, free) | |
| Price at launch | |
| Price today | |
| Free trial or free plan? (Yes/No, how long) | |

**11.3** Pricing changes and tests

| Date | What we changed | Why | What happened |
|---|---|---|---|
| | | | |

**11.4** Money numbers (first 500 customers period)

| Metric | Number |
|---|---|
| Customers who paid | |
| Signup-to-paid % | |
| Average revenue per paying customer | |
| Total revenue so far | |
| Refunds and failed payments | |
| Money left after costs (profit or loss) | |
| Average cost to get one customer (from Part 7) | |
| Did each customer earn back what they cost to get? (Yes/No/Not yet) | |

**11.5** What did customers say about the price? (Use their words, remove names.)
Your answer:

**11.6** Was the price too low, about right, or too high? What is our proof?
Your answer:

**11.7** What would we try next time on pricing?
Your answer:

**11.8** Pricing verdict
- What worked well:
- What we should change next time:
- Score for Part 11: ___

---

# PART 12: TEAM & WELLBEING

> There are no wrong answers. This part protects the most important tool you have: you.

**Why this matters:** Tired builders make worse choices. Working all day with AI has its own kind of tiredness.

**12.1** How did we feel at each stage? (Score 1 = drained, 5 = energized.)

| Phase | Energy 1-5 | Stress 1-5 (5 = very stressed) | One-line note |
|---|---|---|---|
| Planning | | | |
| Building | | | |
| Testing | | | |
| Launch | | | |
| Growing to 500 | | | |

**12.2** What drained energy most? (Pick up to 3.)
- [ ] Constant checking of AI output
- [ ] Unclear priorities
- [ ] Too much work at once
- [ ] Working alone with no one to talk to
- [ ] Customer pressure or complaints
- [ ] Money worries
- [ ] Long hours or no breaks
- [ ] Other: ___

**12.3** What gave energy? (Pick up to 3.)
- [ ] Seeing the first customers
- [ ] Positive feedback
- [ ] Fast progress with AI
- [ ] Learning something new
- [ ] Working with others
- [ ] Other: ___

**12.4** Working patterns

| Question | Answer |
|---|---|
| Average hours per week during the build | |
| Did we take regular days off? (Yes/Sometimes/No) | |
| Did we need to ask others for help? (Yes/No) | |
| Who could we have asked sooner? | |

**12.5** If more than one human worked on this: how was teamwork?
`[ ] N/A, solo project`
- Roles were clear: Score ___
- Decisions were made quickly: Score ___
- People felt safe to say "I disagree": Score ___
Your answer:

**12.6** What would make the next project healthier to run? (Example: set a stop time, plan breaks, find a partner, review AI output in batches.)
Your answer:

**12.7** Wellbeing verdict
- What worked well:
- What we should change next time:
- Score for Part 12: ___

---

# PART 13: POST-LAUNCH INCIDENTS

> An "incident" is anything that broke or went wrong for customers after launch: outage, wrong data, bad update, payment error, or a security scare. If none happened, check the box below and skip to 13.6.

- [ ] No incidents happened after launch (skip to 13.6)

**13.1** Incident log (add one row per incident; also list near-misses)

| # | Date | What customers saw | How long it lasted | How many customers were affected | How we found out (monitor / customer / luck) |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

**13.2** Deep dive on the worst incident

| Question | Answer |
|---|---|
| What happened (short story) | |
| Real root cause (use "5 Whys" in Part 14 if helpful) | |
| Was AI-written code or an AI tool part of the cause? (Yes/No/Unsure) | |
| Time from start to us noticing | |
| Time from noticing to fix | |
| How we fixed it | |
| How we told customers | |
| What it cost us (money, customers, trust) | |

**13.3** How did we handle it? (Check all that are true.)
- [ ] We noticed quickly
- [ ] We knew who was in charge
- [ ] We could go back to the working version
- [ ] We told customers honestly and quickly
- [ ] We wrote down what happened
- [ ] We fixed the cause, not just the symptom
- [ ] We were calm and clear-headed

**13.4** What would have prevented it or made it smaller?
Your answer:

**13.5** What new alarm, test, or rule did we add afterward?
Your answer:

**13.6** Are we ready for the next incident? (Check all that are true.)
- [ ] We get alerts when the product breaks
- [ ] We have a written "what to do when it breaks" list
- [ ] We know how to roll back
- [ ] We have a way to message all customers
- [ ] We tested our backup restore

**13.7** Incident verdict
- What worked well:
- What we should change next time:
- Score for Part 13: ___

---

# PART 14: SURPRISES, DECISIONS & ROOT CAUSES

**14.1** The 3 best decisions we made

| Decision | Why it was good |
|---|---|
| | |

**14.2** The 3 decisions we would change

| Decision | What happened | What we would do instead |
|---|---|---|
| | | |

**14.3** Root cause check ("5 Whys") for our biggest problem
> Ask "why?" five times. Each answer becomes the next question.

- Problem: ___
- Why 1: ___
- Why 2: ___
- Why 3: ___
- Why 4: ___
- Why 5 (the root cause): ___

**14.4** Was this problem caused mostly by... (pick one)
`[ ] Unclear plan  [ ] Missing skill  [ ] Bad tool choice  [ ] Rushing  [ ] AI misuse  [ ] Bad luck  [ ] Other: ___`

**14.5** What luck helped or hurt us? (Be honest: do not copy luck as a strategy.)
Your answer:

---

# PART 15: LESSONS LEARNED

**Why this matters:** This part is what you will reuse across projects. Write each lesson so a stranger could follow it.

**15.1** Keep, Stop, Start

| KEEP doing (worked well) | STOP doing (hurt us) | START doing (we never tried) |
|---|---|---|
| | | |
| | | |
| | | |

**15.2** Top lessons (minimum 3, maximum 10). Use this sentence shape: *"When ___ happens, do ___ because ___."*

| # | Lesson | Phase (Plan / Build / Test / Launch / Customers / AI) | Confidence (High / Medium / Low) |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

**15.3** What advice would we give to our past selves on day 1?
Your answer:

**15.4** What would we tell another person starting a similar project?
Your answer:

---

# PART 16: ACTION ITEMS

> A lesson without an action is just a nice sentence. Every action needs one owner and one date.

| # | Action (start with a verb) | Owner | Due date | Priority (High/Med/Low) | Status (Not started / Doing / Done) |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

**16.1** Which action will make the biggest difference?
Your answer:

**16.2** When will we check that these actions were done? (Write a date.)
Your answer:

---

# PART 17: REUSABLE CHECKLIST FOR THE NEXT PROJECT

> Turn this project's lessons into a short checklist. Next time, copy it into the new project's plan.

**Before we build**
- [ ] ___
- [ ] ___
- [ ] ___

**While we build with AI**
- [ ] ___
- [ ] ___
- [ ] ___

**Before we launch**
- [ ] ___
- [ ] ___
- [ ] ___

**After launch, on the way to 500 customers**
- [ ] ___
- [ ] ___
- [ ] ___

**17.1** Should any of these items be added to our permanent standard process or default AI instructions?
`[ ] Yes  [ ] No`
If yes, which ones and where will they be saved?
Your answer:

---

# PART 18: FINAL SIGN-OFF

- [ ] I checked that every question has an answer, `UNKNOWN`, or `N/A`
- [ ] I removed all passwords, keys, and private customer data
- [ ] I filled in the Scorecard (Part 2) last
- [ ] I saved the file in the correct folder and used the correct file name
- [ ] I shared the top lessons with the people who need them

| Field | Value |
|---|---|
| Filled by | |
| Reviewed by (if any) | |
| Date completed | |
| Next retrospective review date | |

## Appendix A: Evidence list

| # | What it is | Link or file name |
|---|---|---|
| 1 | | |

## Appendix B: Change log of this document

| Date | Who | What changed |
|---|---|---|
| | | |

## Appendix C: Optional AI helper prompt (humans stay in charge)

> Copy this into your AI tool along with your logs, dashboards, and notes. The AI drafts; **you** check every answer and correct it before saving.

```text
You are helping me fill in my project retrospective. I am attaching Project_Retrospective.md and my source material
(project notes, issue list, chat or prompt history, bills, analytics export, support notes).

Rules:
1. Fill in only what the sources clearly show. Never invent numbers, dates, quotes, or links.
2. If the sources do not show it, write UNKNOWN and say what source would answer it.
3. Under each answer, add "Evidence:" with the file name or link you used.
4. Keep blame out. Describe causes in the process, not in people.
5. Do not copy passwords, keys, or customer personal data. Write [REMOVED].
6. Leave all scores (1-5) and the Lessons, Action Items, and Scorecard for me to decide. Suggest options only.
7. At the end, list every answer you were unsure about.
```
