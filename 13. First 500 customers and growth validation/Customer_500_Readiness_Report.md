# How to Fill This Document (Read This First)

**What this is:** A single report that tells you, and anyone you share it with, whether your product is ready for its first 500 customers, and whether it is working once they arrive. It follows the whole journey: idea, build with AI, test, launch, then customers 1 to 500.

**Who can fill it:** Anyone. If you can answer a question in a few plain words, you can fill this in.

## The 7 Rules

1. **Answer every question in plain words.** Short is fine. One honest sentence beats a fancy paragraph.
2. **Find every `[FILL IN]`.** Replace it with your answer. When a section is finished, no `[FILL IN]` should be left in it.
3. **Use the examples as a guide only.** Look at the *Example* line, then write your own answer. Never copy the example.
4. **Do not guess.** If you do not know something, write `UNKNOWN`, and add a line to Section 12 (Risks) saying who will find out and by when.
5. **Use numbers whenever you can.** Write "42 customers", not "a few". Write "$12 per month", not "cheap". Always include the unit (dollars, days, percent, people).
6. **Set the Status tag for every section.** Pick one: `Not Started`, `In Progress`, `Done`. Only mark `Done` when nothing in the section says `[FILL IN]` or `UNKNOWN` without an owner.
7. **Add proof.** When a question asks for evidence, paste a link, a file name, or a screenshot name. A claim without proof counts as `UNKNOWN`.

## Suggested Order

1. Fill the **Document Control** table.
2. Fill Sections **1 to 11** in order. Each takes 15 to 30 minutes.
3. Fill Section **12 (Risks)** and Section **13 (Lessons and Next Steps)**.
4. Fill Section **14 (Score and Go / No-Go)** last, using your earlier answers.
5. Fill the **Quick Snapshot** at the very top of the report body, then ask someone else to read it.

## Words You Might Not Know

| Word | Meaning in plain English |
|---|---|
| **Gate** | A must-pass check. If a gate fails, the answer is No-Go, no matter how good everything else looks. |
| **AI agent** | An AI tool that does multi-step work for you, such as writing code or running tests. |
| **Human review** | A real person checks what the AI produced before it is used. |
| **MVP** | The smallest version of your product that real people can use. |
| **Retention** | How many customers keep using your product after they start. |
| **Churn** | The share of customers who stop using or paying. The opposite of retention. |
| **PMF (product-market fit)** | Customers want your product badly enough to keep using it and to pay. |
| **Unit economics** | Whether you make more money from a customer than it costs to win and serve them. |
| **CAC** | Customer acquisition cost. What it costs you to win one customer. |
| **LTV** | Lifetime value. How much money one customer pays you over their whole time with you. |
| **NPS** | A 0 to 10 survey question: "Would you recommend us?" |
| **Rollback** | Going back to the previous working version if a release breaks things. |

## Instructions for AI Agents Filling This File

If an AI agent helps fill this document, it must follow these rules:

- Fill only what is supported by files, data, or messages it can actually see. Never invent numbers, dates, names, or links.
- Mark anything it could not verify as `UNKNOWN` and add a row to Section 12.
- Put the source (file, link, or message) next to every number.
- Never change a Score, a Gate result, or the Go / No-Go decision in Section 14. Those belong to the human owner.
- Leave the `Approved by` lines in Section 15 empty.

---

# Customer 500 Readiness Report

## Document Control

| Field | Your answer |
|---|---|
| **Product name** | [FILL IN] |
| **Project or folder name** | [FILL IN] |
| **Report version** (example: v0.1) | [FILL IN] |
| **Date started** (YYYY-MM-DD) | [FILL IN] |
| **Last updated** (YYYY-MM-DD) | [FILL IN] |
| **Report owner** (one person) | [FILL IN] |
| **Reviewer** (a different person, if possible) | [FILL IN] |
| **Current stage** (pick one: Building / Testing / Pre-launch / Launched / Growing to 500 / Reached 500) | [FILL IN] |
| **Report type** (pick one: Pre-launch check / Mid-growth check / Final 500-customer review) | [FILL IN] |

### Section Progress Tracker

Update this table as you go.

| # | Section | Status |
|---|---|---|
| 1 | Product in Plain Words | Not Started |
| 2 | Customers and the Problem | Not Started |
| 3 | AI-Driven Development | Not Started |
| 4 | Build Readiness | Not Started |
| 5 | Testing and Quality | Not Started |
| 6 | Security, Privacy, and Legal | Not Started |
| 7 | Launch Readiness | Not Started |
| 8 | Customer Milestones (1 to 500) | Not Started |
| 9 | Product-Market Fit | Not Started |
| 10 | Revenue and Costs | Not Started |
| 11 | Support and Operations | Not Started |
| 12 | Risks, Unknowns, and Open Issues | Not Started |
| 13 | Lessons Learned and Next Steps | Not Started |
| 14 | Readiness Score and Go / No-Go | Not Started |
| 15 | Sign-Off | Not Started |

---

## Quick Snapshot (Fill This Last)

Write these after finishing every other section. A busy reader should understand your whole report from this box alone.

| Question | Your answer |
|---|---|
| **One-sentence summary of the product** | [FILL IN] |
| **Customers right now** (number) | [FILL IN] |
| **Goal** (number and date) | [FILL IN] |
| **Overall Readiness Score** (from Section 14, out of 100) | [FILL IN] |
| **Decision** (Go / Conditional Go / No-Go) | [FILL IN] |
| **Top 3 reasons for this decision** | 1. [FILL IN] 2. [FILL IN] 3. [FILL IN] |
| **Biggest risk** | [FILL IN] |
| **The next action, who owns it, and the date** | [FILL IN] |

---

## 1. Product in Plain Words

**Status:** `Not Started`

*Goal: explain the product so anyone could repeat it correctly.*

**1.1 What does your product do? Use one or two sentences, no jargon.**
*Example:* "It helps small bakeries track daily orders so they never run out of flour."
**Your answer:** [FILL IN]

**1.2 What is the one main thing a customer can do with it?**
*Example:* "Add an order and see what ingredients are needed."
**Your answer:** [FILL IN]

**1.3 What makes it different from what people use today?**
*Example:* "Others need a spreadsheet. Ours works from a phone in 30 seconds."
**Your answer:** [FILL IN]

**1.4 What is included in the first version, and what is NOT included yet?**

| Included now | Not included yet (planned later) |
|---|---|
| [FILL IN] | [FILL IN] |

**1.5 Where can people find or use it?** (website, app store, link)
**Your answer:** [FILL IN]

**1.6 Links to your key project material** (code, designs, plans, dashboards)
**Your answer:** [FILL IN]

---

## 2. Customers and the Problem

**Status:** `Not Started`

*Goal: prove you know who the product is for and why they care.*

**2.1 Who is your ideal customer? Describe one real type of person or business.**
*Example:* "Owners of bakeries with 1 to 5 staff in small cities."
**Your answer:** [FILL IN]

**2.2 What problem do they have? What do they do today to cope?**
*Example:* "They guess ingredient needs and lose about $200 a month to waste."
**Your answer:** [FILL IN]

**2.3 How do you know this problem is real? Add proof.**
*Example:* "Interviewed 15 owners; 11 said it was a top-3 problem. Notes in `interviews.md`."
**Your answer:** [FILL IN]

**2.4 How many people or businesses are in your target group?** (best honest estimate, with source)
**Your answer:** [FILL IN]

**2.5 Why will the first 500 customers come from this group?** (Where do they gather? How will you reach them?)
**Your answer:** [FILL IN]

**2.6 Who are your 3 closest competitors or alternatives?**

| Competitor or alternative | What they do well | Where we are better |
|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] |

---

## 3. AI-Driven Development

**Status:** `Not Started`

*Goal: show how AI helped build the product and how you made sure it can be trusted.*

**3.1 Which AI tools and models did you use, and for what?**

| Tool or model | Used for (planning, coding, testing, writing, design, support) | Version or date | Who controls it |
|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**3.2 Roughly what share of the code, content, or tests was written by AI?** (example: about 60% of code)
**Your answer:** [FILL IN]

**3.3 Does the product itself use AI for customers?** (If NO, write "No" and skip to 3.8.)
**Your answer:** [FILL IN]

**3.4 What does the AI feature do, and what can it NOT be trusted to do?**
*Example:* "Writes order summaries. Must not give legal or medical advice."
**Your answer:** [FILL IN]

**3.5 How do you check the AI's answers are good?** (test questions, sample reviews, scoring)

| Check | How often | Result (number) | Proof |
|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**3.6 What happens when the AI is wrong or fails?** (fallback, message to the user, human takeover)
**Your answer:** [FILL IN]

**3.7 What does the AI cost per customer per month?** (number with unit)
**Your answer:** [FILL IN]

**3.8 Where did a human review AI-made work before it shipped?**

| What was reviewed | Who reviewed | Date | Problems found and fixed |
|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**3.9 Do you keep a record of your important prompts, instructions, and agent settings?** (Where are they stored?)
**Your answer:** [FILL IN]

**3.10 What customer data is sent to AI services? Do customers know about it?**
**Your answer:** [FILL IN]

**3.11 What happens if your AI provider changes price, quality, or shuts down?**
**Your answer:** [FILL IN]

---

## 4. Build Readiness

**Status:** `Not Started`

*Goal: confirm the product is actually built, stable, and can be fixed fast.*

**4.1 Which features are finished, and which are not?**

| Feature | Status (Done / Partly / Not started) | Needed for launch? (Yes / No) |
|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] |

**4.2 Can the product handle 500 customers at once?** What did you test, and what was the result?
*Example:* "Simulated 600 users on 2026-09-01. Pages loaded in under 2 seconds."
**Your answer:** [FILL IN]

**4.3 Where does the product run, and what does it cost per month?**
**Your answer:** [FILL IN]

**4.4 Is your code saved safely with a history of changes?** (where, and who has access)
**Your answer:** [FILL IN]

**4.5 Can you go back to the last working version within 15 minutes if a release breaks things?** (describe how)
**Your answer:** [FILL IN]

**4.6 Are customer data backups running, and have you tested restoring one?** (date of last restore test)
**Your answer:** [FILL IN]

**4.7 How will you know if the product breaks?** (alerts, monitoring, who gets notified)
**Your answer:** [FILL IN]

**4.8 Is there someone besides you who can fix the product if you are unavailable?**
**Your answer:** [FILL IN]

---

## 5. Testing and Quality

**Status:** `Not Started`

*Goal: show the product works the way real people use it.*

**5.1 Which tests did you run?**

| Test type | What it checks | Done? (Yes / No) | Result | Proof |
|---|---|---|---|---|
| Does it work? (feature tests) | Every main feature does what it should | [FILL IN] | [FILL IN] | [FILL IN] |
| Does it break? (bug hunting) | Strange or wrong inputs | [FILL IN] | [FILL IN] | [FILL IN] |
| Is it fast? (speed tests) | Loading time under normal use | [FILL IN] | [FILL IN] | [FILL IN] |
| Does it work on different devices? | Phone, tablet, computer, browsers | [FILL IN] | [FILL IN] | [FILL IN] |
| Can everyone use it? (accessibility) | Readable text, keyboard use, screen readers | [FILL IN] | [FILL IN] | [FILL IN] |
| Can real people use it? (user testing) | Strangers complete the main task | [FILL IN] | [FILL IN] | [FILL IN] |

**5.2 How many serious bugs (stops people from using the product) are still open?** (number, with list link)
**Your answer:** [FILL IN]

**5.3 How many minor bugs are still open, and when will they be fixed?**
**Your answer:** [FILL IN]

**5.4 How many people outside your team tried it before launch, and what did they say?**
**Your answer:** [FILL IN]

**5.5 Did anyone other than the builder (or the AI that built it) test it?**
**Your answer:** [FILL IN]

---

## 6. Security, Privacy, and Legal

**Status:** `Not Started`

*Goal: protect customers and protect you.*

**6.1 What personal or private information do you collect?** (names, emails, payments, files, anything else)
**Your answer:** [FILL IN]

**6.2 Where is this data stored, and who can see it?**
**Your answer:** [FILL IN]

**6.3 Check each item (Yes / No / Not needed):**

| Check | Answer | Proof or note |
|---|---|---|
| Passwords and keys are stored safely, never inside the code | [FILL IN] | [FILL IN] |
| Customer logins are protected (strong passwords or secure sign-in) | [FILL IN] | [FILL IN] |
| Data is encrypted when sent and stored | [FILL IN] | [FILL IN] |
| Payments go through a trusted payment provider (you never store card numbers) | [FILL IN] | [FILL IN] |
| Someone has tried to break in on purpose, or a security scan was run | [FILL IN] | [FILL IN] |
| A Privacy Policy is published | [FILL IN] | [FILL IN] |
| Terms of Service are published | [FILL IN] | [FILL IN] |
| Customers can ask you to delete their data | [FILL IN] | [FILL IN] |
| Cookie or tracking notices are in place (if needed) | [FILL IN] | [FILL IN] |
| AI-generated code and content were checked for copied or unlicensed material | [FILL IN] | [FILL IN] |

**6.4 Which laws or rules apply to you?** (examples: GDPR, CCPA, HIPAA, local business rules, industry rules)
**Your answer:** [FILL IN]

**6.5 What is your plan if customer data leaks?** (who is told, how fast, who fixes it)
**Your answer:** [FILL IN]

**6.6 Did a lawyer or expert review your legal pages?** (Yes / No / Not needed, and why)
**Your answer:** [FILL IN]

---

## 7. Launch Readiness

**Status:** `Not Started`

*Goal: be sure launch day will not be a surprise.*

**7.1 What is your launch date (or what was it)?** (YYYY-MM-DD)
**Your answer:** [FILL IN]

**7.2 Launch checklist (Yes / No):**

| Item | Answer | Owner |
|---|---|---|
| Website or app store page is live and correct | [FILL IN] | [FILL IN] |
| Sign-up works from start to finish | [FILL IN] | [FILL IN] |
| Payment works from start to finish (test purchase done) | [FILL IN] | [FILL IN] |
| Welcome email or first-use guide is ready | [FILL IN] | [FILL IN] |
| Help pages or FAQ are ready | [FILL IN] | [FILL IN] |
| Support contact is visible and monitored | [FILL IN] | [FILL IN] |
| Analytics are installed and showing real data | [FILL IN] | [FILL IN] |
| Rollback plan is written and tested | [FILL IN] | [FILL IN] |
| Launch announcement is ready (post, email, message) | [FILL IN] | [FILL IN] |

**7.3 How will the first 50 customers find you?** (list your channels, and the number you expect from each)

| Channel | Expected customers | Cost | Proof it can work |
|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**7.4 What will you do in the first 24 hours after launch?** (hour by hour, if possible)
**Your answer:** [FILL IN]

**7.5 What would make you pause or undo the launch?** (clear triggers with numbers)
*Example:* "More than 5% of sign-ups fail, or any payment error."
**Your answer:** [FILL IN]

---

## 8. Customer Milestones (1 to 500)

**Status:** `Not Started`

*Goal: track the journey to 500 and know what to check at each stage.*

**8.1 Milestone tracker.** Fill the Planned column before launch, and the Actual column as you go.

| Milestone | Planned date | Actual date | Customers (actual) | What we must check at this stage |
|---|---|---|---|---|
| First 1 customer | [FILL IN] | [FILL IN] | [FILL IN] | Can a stranger sign up and succeed without help? |
| 10 customers | [FILL IN] | [FILL IN] | [FILL IN] | What confuses people? What do they ask first? |
| 50 customers | [FILL IN] | [FILL IN] | [FILL IN] | Do people come back in week 2? |
| 100 customers | [FILL IN] | [FILL IN] | [FILL IN] | Is support manageable? Are costs as expected? |
| 250 customers | [FILL IN] | [FILL IN] | [FILL IN] | Is growth repeatable, or was it a one-time bump? |
| 500 customers | [FILL IN] | [FILL IN] | [FILL IN] | Is the business healthy, and what breaks at 1,000? |

**8.2 Definition check: what counts as a "customer" for you?** (example: "someone who paid at least once and used the product in the last 30 days")
**Your answer:** [FILL IN]

**8.3 Where did each group of customers come from?**

| Source (example: friends, social media, ads, search, referrals) | Customers | Cost to win one (CAC) |
|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] |

**8.4 What were the biggest surprises at each milestone?**
**Your answer:** [FILL IN]

**8.5 What problems appeared as you grew, and how were they fixed?**
**Your answer:** [FILL IN]

---

## 9. Product-Market Fit

**Status:** `Not Started`

*Goal: find out whether customers truly want this, using numbers rather than feelings.*

**9.1 Fill in your numbers.** Always write the date range these numbers cover.

| Measure | What it means | Your number | Healthy target (you set it) | On track? |
|---|---|---|---|---|
| Sign-ups | People who joined | [FILL IN] | [FILL IN] | [FILL IN] |
| Activation rate | % who finish the first key action | [FILL IN] | [FILL IN] | [FILL IN] |
| Week-4 retention | % still active after 4 weeks | [FILL IN] | [FILL IN] | [FILL IN] |
| Monthly churn | % who left this month | [FILL IN] | [FILL IN] | [FILL IN] |
| NPS score | "Would you recommend us?" (0 to 10) | [FILL IN] | [FILL IN] | [FILL IN] |
| Referral rate | % who brought a friend | [FILL IN] | [FILL IN] | [FILL IN] |

**9.2 The "Very Disappointed" question.** Ask customers: *"How would you feel if you could no longer use this product?"*

| Answer | Number of customers |
|---|---|
| Very disappointed | [FILL IN] |
| Somewhat disappointed | [FILL IN] |
| Not disappointed | [FILL IN] |

*A common rule of thumb: product-market fit is likely when about 40% or more say "very disappointed". Add how many people you asked.*
**Number of people asked:** [FILL IN]

**9.3 What do customers say they love? Add 3 real comments (with date and source).**
**Your answer:** [FILL IN]

**9.4 What do customers complain about most?** (top 3, with how many people mentioned each)
**Your answer:** [FILL IN]

**9.5 What features do customers use the most, and which do they ignore?**
**Your answer:** [FILL IN]

**9.6 Which customers got the most value? What do they have in common?**
**Your answer:** [FILL IN]

**9.7 Which customers left, and why? Add at least 5 real reasons.**
**Your answer:** [FILL IN]

**9.8 Based on the evidence, do you have product-market fit?** (Yes / Partly / Not yet) Explain in 2 sentences, with proof.
**Your answer:** [FILL IN]

---

## 10. Revenue and Costs

**Status:** `Not Started`

*Goal: be sure you can afford to keep serving customers as you grow.*

**10.1 How do you charge?** (free, subscription, one-time, usage-based) and what is the price?
**Your answer:** [FILL IN]

**10.2 Why did you pick this price? What proof says customers will pay it?**
**Your answer:** [FILL IN]

**10.3 Money in and out (fill in per month, using the same currency throughout).**

| Item | Amount per month | Notes |
|---|---|---|
| Revenue (money in) | [FILL IN] | [FILL IN] |
| Hosting and infrastructure | [FILL IN] | [FILL IN] |
| AI services (models, APIs, tools) | [FILL IN] | [FILL IN] |
| Other software and tools | [FILL IN] | [FILL IN] |
| Marketing and ads | [FILL IN] | [FILL IN] |
| Support costs | [FILL IN] | [FILL IN] |
| Payment fees | [FILL IN] | [FILL IN] |
| People (including your own time, if paid) | [FILL IN] | [FILL IN] |
| **Profit or loss** (money in minus money out) | [FILL IN] | [FILL IN] |

**10.4 Unit economics.**

| Measure | Your number | Formula or how you worked it out |
|---|---|---|
| Cost to win one customer (CAC) | [FILL IN] | Total marketing and sales cost divided by new customers |
| Average revenue per customer per month | [FILL IN] | Revenue divided by customers |
| Cost to serve one customer per month | [FILL IN] | Hosting + AI + support + fees divided by customers |
| Lifetime value (LTV) | [FILL IN] | Average monthly profit per customer times average months they stay |
| LTV divided by CAC | [FILL IN] | A common healthy target is 3 or higher |
| Months to earn back CAC | [FILL IN] | CAC divided by monthly profit per customer |

**10.5 How many months can you keep going at your current spending?** (money you have divided by monthly loss)
**Your answer:** [FILL IN]

**10.6 If you reach 500 customers, what happens to your costs?** (do they stay flat, grow slowly, or grow fast?)
**Your answer:** [FILL IN]

**10.7 What is your plan if AI or infrastructure costs double?**
**Your answer:** [FILL IN]

---

## 11. Support and Operations

**Status:** `Not Started`

*Goal: be sure you can look after customers without burning out.*

**11.1 How can customers get help?** (email, chat, help page, community)
**Your answer:** [FILL IN]

**11.2 Support numbers (use your latest period).**

| Measure | Your number |
|---|---|
| Support requests per week | [FILL IN] |
| Time to first reply (average) | [FILL IN] |
| Time to solve (average) | [FILL IN] |
| Customer satisfaction with support (score or %) | [FILL IN] |
| Hours per week you spend on support | [FILL IN] |

**11.3 What are the top 5 questions or problems customers raise?** Could the product, help pages, or AI remove them?
**Your answer:** [FILL IN]

**11.4 If support requests tripled, what would you do?**
**Your answer:** [FILL IN]

**11.5 Do you have a written plan for outages and urgent problems?** (who does what, how customers are told)
**Your answer:** [FILL IN]

**11.6 Uptime (how often the product was working).** Write the percentage and the date range.
**Your answer:** [FILL IN]

**11.7 Which repeated tasks could be automated by AI or tools, and which must stay human?**
**Your answer:** [FILL IN]

---

## 12. Risks, Unknowns, and Open Issues

**Status:** `Not Started`

*Goal: list everything that could go wrong or is not yet known. Honest risks make the report more trustworthy.*

Add every `UNKNOWN` from earlier sections here. Add more rows if you need them.

| # | Risk, issue, or unknown | How likely? (Low / Medium / High) | How bad if it happens? (Low / Medium / High) | What will we do about it? | Owner | Due date | Status (Open / Fixed) |
|---|---|---|---|---|---|---|---|
| 1 | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| 2 | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| 3 | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

**12.1 Which single risk could stop the whole project, and what is your backup plan?**
**Your answer:** [FILL IN]

---

## 13. Lessons Learned and Next Steps

**Status:** `Not Started`

*Goal: capture what you learned so the next project (or the next 500 customers) goes better.*

**13.1 What went well? Name 3 things.**
**Your answer:** 1. [FILL IN] 2. [FILL IN] 3. [FILL IN]

**13.2 What went badly or took longer than expected? Name 3 things.**
**Your answer:** 1. [FILL IN] 2. [FILL IN] 3. [FILL IN]

**13.3 What did AI help with the most, and where did it let you down?**
**Your answer:** [FILL IN]

**13.4 What would you do differently if you started again?**
**Your answer:** [FILL IN]

**13.5 Next 30 days: what are the 3 most important actions?**

| Action | Owner | Due date |
|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] |

**13.6 What should you do next after 500 customers?** (grow to 1,000, fix retention, raise money, change price, or stop)
**Your answer:** [FILL IN]

---

## 14. Readiness Score and Go / No-Go

**Status:** `Not Started`

*Goal: turn your answers into a clear decision. Fill this section after finishing Sections 1 to 13. Be honest. Scores that are too high only hurt you later.*

### Step 1: Must-Pass Gates

A gate is a must-pass check. **If ANY gate says FAIL, the decision is No-Go**, even when the score is high.

| # | Gate (answer Pass or Fail) | Result | Evidence (section or link) |
|---|---|---|---|
| G1 | The main feature works for a real person from start to finish | [FILL IN] | [FILL IN] |
| G2 | No serious bugs are open (Section 5.2 is 0) | [FILL IN] | [FILL IN] |
| G3 | Customer data is protected and backups can be restored | [FILL IN] | [FILL IN] |
| G4 | Privacy Policy and Terms are published | [FILL IN] | [FILL IN] |
| G5 | A tested rollback plan exists | [FILL IN] | [FILL IN] |
| G6 | Someone watches for problems and answers customers | [FILL IN] | [FILL IN] |
| G7 | A human reviewed all AI-made work that touches customer data, money, or safety | [FILL IN] | [FILL IN] |
| G8 | You can pay for hosting, AI, and support for at least 3 more months | [FILL IN] | [FILL IN] |

### Step 2: Score Each Area

Give each area a score from 0 to 10 using the guide below, then total them.

| Score | Meaning |
|---|---|
| 0 to 3 | Missing or unproven. Many `[FILL IN]` or `UNKNOWN`. |
| 4 to 6 | Partly done. Some proof, but important gaps. |
| 7 to 8 | Good. Proof is there, with small gaps. |
| 9 to 10 | Excellent. Proven with numbers and evidence. |

| Area | Section | Score (0 to 10) | One-line reason |
|---|---|---|---|
| Product clarity | 1 | [FILL IN] | [FILL IN] |
| Customer and problem understanding | 2 | [FILL IN] | [FILL IN] |
| AI-driven development quality | 3 | [FILL IN] | [FILL IN] |
| Build readiness | 4 | [FILL IN] | [FILL IN] |
| Testing and quality | 5 | [FILL IN] | [FILL IN] |
| Security, privacy, and legal | 6 | [FILL IN] | [FILL IN] |
| Launch readiness | 7 | [FILL IN] | [FILL IN] |
| Customer growth toward 500 | 8 | [FILL IN] | [FILL IN] |
| Product-market fit | 9 | [FILL IN] | [FILL IN] |
| Revenue and costs | 10 | [FILL IN] | [FILL IN] |
| **Total (out of 100)** | | [FILL IN] | |

*Support and Operations (Section 11) and Risks (Section 12) are checked through gates G6 and G8 and through the decision below.*

### Step 3: Make the Decision

| Situation | Decision |
|---|---|
| Any gate failed | **No-Go.** Fix the failed gate, then re-check. |
| All gates passed and score is 85 or higher | **Go.** |
| All gates passed and score is 70 to 84 | **Conditional Go.** Go only after the listed conditions are done. |
| All gates passed and score is below 70 | **No-Go.** |

**Final decision:** [FILL IN]

**If Conditional Go or No-Go, what must be fixed first, who owns it, and by when?**

| Condition | Owner | Due date | Done? |
|---|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

---

## 15. Sign-Off

**Status:** `Not Started`

By signing, each person confirms they read this report and believe it is honest and complete. AI agents must not sign.

| Role | Name | Decision (Approve / Approve with conditions / Reject) | Date | Comments |
|---|---|---|---|---|
| Report owner | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Reviewer | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| Final approver | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

---

## Change History

| Version | Date | Who | What changed |
|---|---|---|---|
| v0.1 | [FILL IN] | [FILL IN] | First draft |

## Final Check Before Sharing

- [ ] No `[FILL IN]` is left anywhere in the report body.
- [ ] Every `UNKNOWN` appears in Section 12 with an owner and a date.
- [ ] Every number has a unit and a source.
- [ ] Every Status tag and the Section Progress Tracker are up to date.
- [ ] The Quick Snapshot matches Section 14.
- [ ] Someone other than the owner has read the report.
