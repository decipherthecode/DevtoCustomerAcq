---
# ===== MACHINE-READABLE HEADER (fill every line; AI agents read this first) =====
document: Growth_Bottleneck_Analysis
template_version: 1.0
project_id: ""            # e.g. PRJ-014 (short, no spaces)
project_name: ""          # e.g. PlantPal
owner: ""                 # one person who is responsible
filled_by: ""             # name(s) of people / agents who wrote answers
current_phase: ""         # one of: BUILD | BETA | LAUNCH | FIRST-100 | 100-TO-500
customers_today: 0        # whole number
target_customers: 500
date_started: ""          # YYYY-MM-DD
last_updated: ""          # YYYY-MM-DD
status: DRAFT             # DRAFT | IN-REVIEW | APPROVED | SUPERSEDED
the_one_bottleneck: ""    # fill in Section 21 (one short sentence)
next_review_date: ""      # YYYY-MM-DD
---

# HOW TO FILL THIS DOCUMENT

Read this part first. It takes 3 minutes. If you can read, you can fill this in.

## What is this document?

Imagine a bottle of water. The neck of the bottle is narrow, so water can only come out slowly, no matter how much water is inside. **A bottleneck is the narrow neck.** For a product, it is the one thing that slows down how fast you get customers.

This document helps you:

1. Find the **one** thing holding your product back from reaching its **first 500 customers**.
2. Prove it with real numbers and real customer words, not guesses.
3. Pick the best fixes, test them, and check if they worked.

You will use this document again and again from the day you start building until you have 500 customers.

## The 6 rules

| # | Rule | Why |
|---|------|-----|
| 1 | **Answer every question.** If a question does not apply, write `N/A because ...` and give a reason. | Blank lines make people guess. |
| 2 | **Use real numbers.** Write `12 people`, not `a few`. If you do not know, write `UNKNOWN` and add it to Section 8. | Guesses hide problems. |
| 3 | **Never delete a question.** Just answer it. | Keeps every project's document the same shape. |
| 4 | **Write short sentences.** One idea per line. | Easier to read, easier for AI to check. |
| 5 | **Put dates on everything.** Use `YYYY-MM-DD` (example: `2026-10-19`). | Numbers change. Dates tell us when. |
| 6 | **Say where you got it.** Write `Source: ...` (analytics tool, survey, interview, your own count). | So anyone can double-check. |

## How each section looks

```
### 7.1 A question written in plain words
Why we ask: (one line that explains why this matters)
Example answer: (a filled-in example so you can copy the style)
Your answer:
> (type here)
```

- **"Example answer"** is just a sample. Do not copy it. Replace it with your own truth.
- **Tick boxes:** change `[ ]` to `[x]` to select.
- **Tables:** fill every empty cell. Use `UNKNOWN` if you do not know.

## Boxes you will see

> **[PHASE TAG]** Some sections say `Do this in: BUILD, BETA ...`. Fill those when you reach that phase. Earlier sections can say `N/A because we are still in BUILD`.

> **[AI-BOX]** Boxes starting with `AI-BOX` are instructions for AI agents (like Claude). **Humans can skip them.** The document still makes sense without them. AI agents must follow them exactly.

> **[HUMAN CHECKPOINT]** A person must read, agree and sign off before moving on. AI agents may draft, but must stop here and wait.

## The 5 phases (where are you?)

| Phase code | Plain meaning | Customers | Main question |
|-----------|---------------|-----------|---------------|
| `BUILD` | We are making the product. | 0 | Are we building the right thing, and can we build it fast and safely? |
| `BETA` | A small group is testing it. | 0 to about 20 | Does it work, and do testers actually use it? |
| `LAUNCH` | We opened the doors to everyone. | about 1 to 10 | Can strangers find us, sign up and get value? |
| `FIRST-100` | We are getting our first 100 real customers. | 10 to 100 | Which channel works, and do people stay? |
| `100-TO-500` | We are growing from 100 to 500. | 100 to 500 | Can we repeat this growth without breaking? |

(The customer counts are guides, not strict rules. Pick the phase that fits best, and write why in Section 3.)

## Step-by-step: what to do

1. Fill the **header** at the very top (project id, owner, phase).
2. Go through **Sections 1 to 8** (setting the scene). Do these once, then update when things change.
3. Go through **Sections 9 to 19** (finding the leaks). Refresh these every review.
4. Do **Sections 20 to 24** (picking the one bottleneck and the fixes).
5. Do **Sections 25 to 29** (checking, deciding, planning the next review).
6. Do the **Final Quality Checklist** (Section 30). Only then change `status` to `IN-REVIEW`.
7. When you review again (every 1 to 2 weeks while growing), **copy the "Review Log" in Section 29**, add a new row, and update numbers. Do not rewrite the whole document.

## Words you need (short list)

| Word | Simple meaning |
|------|----------------|
| Customer | A person or company who **paid** or who **uses it for real** (you define exactly in Section 5). |
| Funnel | The path a person walks: hear about us, visit, sign up, use, pay, stay, tell friends. |
| Conversion | The share of people who move from one step to the next. 10 of 100 = **10%**. |
| Churn | People who leave. |
| Retention | People who stay. |
| Activation | The first time someone gets the main benefit ("aha moment"). |
| CAC | Cost to get one customer (money spent on getting customers ÷ customers gained). |
| Hypothesis | A "we think X will cause Y" statement you can test. |
| Experiment | A small, quick test of a hypothesis. |

More words are in the Glossary at the end.

---

# GROWTH BOTTLENECK ANALYSIS

**Project:** _(copy `project_name` from the header)_
**Goal:** Reach **500 customers** and know exactly what slows us down on the way.

> **[AI-BOX: READ ME FIRST]**
> You are an AI agent helping fill this document. Follow these rules in every section:
> 1. Read the YAML header and Section 3 (phase) before anything else.
> 2. Only write facts the human gave you or that you found with a named source. Never invent numbers. If missing, write `UNKNOWN` and add it to Section 8.
> 3. Ask the human **one clear question at a time** when something is missing. Use simple words.
> 4. At every `[HUMAN CHECKPOINT]`, stop and wait for a clear "yes".
> 5. Do not change another section's answer without saying so and giving the reason.
> 6. After writing a section, re-read it and check it against that section's "Done when" line.

---

## Table of Contents

**Part A: Set the scene**
1. The Project in Simple Words
2. Who Is the Customer?
3. Where Are We Now? (Phase)
4. The Goal and the Finish Line
5. What Counts as a Customer?
6. The Customer Journey Map
7. The Numbers Dashboard
8. Can We Trust Our Numbers? (Data Check)

**Part B: Find the leaks**
9. Funnel Leak Finder
10. Acquisition: Do People Find Us?
11. Activation: Do People Get Value Fast?
12. Retention: Do People Stay?
13. Revenue: Do People Pay (and Is It Worth It)?
14. Referral: Do People Tell Others?
15. Product Bottlenecks
16. Building and AI-Development Bottlenecks
17. People, Time and Money Bottlenecks
18. Trust, Legal and Platform Bottlenecks
19. What Customers Actually Said

**Part C: Pick the fix**
20. Product-Market Fit Signals
21. Find THE One Bottleneck
22. Find the Root Cause (5 Whys)
23. Fix Ideas and Scoring (ICE / RICE)
24. Experiment Plan

**Part D: Check and decide**
25. Phase Gate Check (Can We Move Forward?)
26. Risks and Assumptions
27. Decision Log
28. Action Plan (Who Does What by When)
29. Review Log (Repeat Every 1 to 2 Weeks)
30. Final Quality Checklist

**Appendices**
- A. Metric Cheat Sheet
- B. Worked Mini-Example
- C. AI Agent Master Prompt
- D. Glossary
- E. Further Reading

---

# PART A: SET THE SCENE

---

## 1. The Project in Simple Words

**Do this in:** all phases. **Done when:** a stranger can understand your product in 30 seconds.

### 1.1 What is the product called?
Why we ask: everyone must use the same name.
Example answer: `PlantPal`
Your answer:
> 

### 1.2 Finish this sentence: "Our product helps ____ do ____ so that ____."
Why we ask: forces you to say it plainly.
Example answer: `Our product helps busy plant owners remember watering so that their plants stay alive.`
Your answer:
> 

### 1.3 What type of product is it? (tick one)
- [ ] Mobile app
- [ ] Website / web app (software you use in a browser)
- [ ] Software for businesses (B2B)
- [ ] Marketplace (connects buyers and sellers)
- [ ] Tool / plugin / extension
- [ ] Content / course / community
- [ ] Physical product with software
- [ ] Other: ________

### 1.4 How do customers pay? (tick all that apply)
- [ ] Free (no payment yet)
- [ ] Free trial then paid
- [ ] Monthly subscription
- [ ] Yearly subscription
- [ ] One-time purchase
- [ ] Pay per use
- [ ] Ads / other: ________

### 1.5 What is the price? (write "none" if free)
Example answer: `$9 per month`
Your answer:
> 

### 1.6 Who built it and how? (tick all that apply)
- [ ] Built by people only
- [ ] Built with AI coding help (people review the code)
- [ ] Built mostly by AI agents (people approve)
- [ ] Bought or customized from another product

### 1.7 Link to the product (or write "not live yet")
Your answer:
> 

---

## 2. Who Is the Customer?

**Do this in:** all phases. **Done when:** you can describe one real person, not "everyone".

### 2.1 Describe your ideal first customer as ONE real-feeling person.
Why we ask: "Everyone" is not a customer. Picking one person makes marketing and fixing much easier.
Example answer: `Maya, 29, works in an office, owns 12 plants, forgets to water them, uses her phone all day.`
Your answer:
> 

### 2.2 What problem do they have today? (in their words)
Example answer: `"I keep killing my plants and I feel bad."`
Your answer:
> 

### 2.3 What do they do right now to solve it? (the "old way")
Why we ask: your real competitor is often "do nothing" or "a spreadsheet".
Example answer: `Sticky notes and phone alarms.`
Your answer:
> 

### 2.4 Where do these people hang out? (websites, groups, places)
Example answer: `r/houseplants, Instagram plant accounts, local garden centers.`
Your answer:
> 

### 2.5 How many such people exist? (rough size, with source)
Example answer: `About 2 million plant owners in our country. Source: industry report 2025.`
Your answer:
> 

### 2.6 Who is NOT our customer? (so we do not waste time)
Example answer: `Farmers and professional gardeners.`
Your answer:
> 

### 2.7 Customer type (tick one)
- [ ] Individuals (B2C)
- [ ] Small businesses
- [ ] Big companies
- [ ] Both people and businesses

### 2.8 If businesses: who decides to buy, and who uses it? (write "N/A" if individuals)
Your answer:
> 

---

## 3. Where Are We Now? (Phase)

**Do this in:** all phases. Update every review. **Done when:** one phase is chosen and a reason is written.

### 3.1 Which phase are we in? (tick one)
- [ ] BUILD (still making it)
- [ ] BETA (small test group)
- [ ] LAUNCH (public, first customers)
- [ ] FIRST-100 (growing to 100)
- [ ] 100-TO-500 (growing to 500)

### 3.2 Why this phase? (one or two sentences with facts)
Example answer: `Public since 2026-09-01. 37 paying customers.`
Your answer:
> 

### 3.3 Dates (fill what you know)
| Event | Date (YYYY-MM-DD) | Done? |
|-------|-------------------|-------|
| Build started | | [ ] |
| First working version | | [ ] |
| Beta started | | [ ] |
| Public launch | | [ ] |
| First paying customer | | [ ] |
| 100th customer | | [ ] |
| 500th customer (goal) | | [ ] |

### 3.4 Customers right now (whole numbers, with date and source)
| Customers who signed up | Customers who are active | Customers who paid | Date | Source |
|-------------------------|--------------------------|--------------------|------|--------|
| | | | | |

> **[AI-BOX]** Copy `current_phase` and `customers_today` into the YAML header. If the phase and the customer count disagree by more than one phase, ask the human why before continuing.

---

## 4. The Goal and the Finish Line

**Do this in:** all phases. **Done when:** everyone can say the goal the same way.

### 4.1 Our goal in one sentence
Example answer: `Get 500 paying customers by 2027-03-31 without spending more than $5,000.`
Your answer:
> 

### 4.2 Deadline (YYYY-MM-DD)
Your answer:
> 

### 4.3 Money limit for getting customers
Your answer:
> 

### 4.4 Time each person can give per week
| Person | Role | Hours per week |
|--------|------|----------------|
| | | |

### 4.5 How many customers do we need each week to hit the goal?
Why we ask: this shows if you are on pace.
How to calculate: `(500 − customers today) ÷ weeks left`
Example answer: `(500 − 37) ÷ 24 weeks = about 19 per week`
Your answer:
> 

### 4.6 What else must be true when we hit 500? (tick all that apply)
- [ ] Most customers are still using it after 30 days
- [ ] Each customer earns us more than they cost us to get
- [ ] Customers come from at least 2 different channels
- [ ] Customers say they would be upset if the product vanished
- [ ] Support and servers still work smoothly
- [ ] Other: ________

---

## 5. What Counts as a Customer?

**Do this in:** all phases. **Done when:** one exact rule is written and everyone agrees. **Why it matters:** if people count customers differently, all your numbers lie.

### 5.1 Our official definition of "customer"
Example answer: `A person who has paid at least once and whose payment was not refunded.`
Your answer:
> 

### 5.2 Who is NOT counted?
Example answer: `Free trial users, our own team, test accounts, refunded accounts.`
Your answer:
> 

### 5.3 Define these words for your product
| Word | Our exact meaning |
|------|-------------------|
| Visitor | |
| Sign-up (lead) | |
| Activated user | |
| Active user | |
| Paying customer | |
| Churned customer | |

### 5.4 Where do we count from? (name the tool or file)
Example answer: `Stripe for payments, Mixpanel for usage.`
Your answer:
> 

> **[HUMAN CHECKPOINT]** The owner confirms the definitions above. Do not change them later without writing it in Section 27 (Decision Log), or old numbers will not match new ones.

---

## 6. The Customer Journey Map

**Do this in:** BETA and later (in BUILD, write your best plan). **Done when:** every step from "never heard of us" to "told a friend" has a name and a place to measure it.

### 6.1 Fill the journey, one row per step
| Step # | What the customer does | Where it happens | How we measure it | Who owns it |
|--------|------------------------|------------------|-------------------|-------------|
| 1 | Hears about us | | | |
| 2 | Visits our page / store | | | |
| 3 | Signs up | | | |
| 4 | Sets up / first use | | | |
| 5 | Gets first value ("aha!") | | | |
| 6 | Uses it again | | | |
| 7 | Pays | | | |
| 8 | Keeps using / renews | | | |
| 9 | Tells others | | | |

Example row: `2 | Visits our landing page | plantpal.com | Page views in analytics | Sam`

### 6.2 What is the "aha moment"? (the moment they first feel the value)
Example answer: `They add a plant and get their first watering reminder.`
Your answer:
> 

### 6.3 How long does it take a new person to reach the aha moment? (time, with source)
Example answer: `Median 6 minutes. Source: analytics, 2026-10-10 to 2026-10-17.`
Your answer:
> 

### 6.4 Where do you think people get stuck? (your guess for now, we will check with data in Part B)
Your answer:
> 

---

## 7. The Numbers Dashboard

**Do this in:** BETA and later. Refresh every review. **Done when:** every row has a number or `UNKNOWN`.

### 7.1 Funnel numbers for the last 30 days (or since launch if shorter)
Period: from `____` to `____`

| Stage | What we count | This period | Last period | Change | Source |
|-------|---------------|-------------|-------------|--------|--------|
| Visitors | People who saw our page | | | | |
| Sign-ups | People who made an account | | | | |
| Activated | People who reached the aha moment | | | | |
| Active (repeat use) | People who came back | | | | |
| Paying | People who paid | | | | |
| Retained (30 days) | People still using after 30 days | | | | |
| Referred | New people who came from a friend | | | | |

### 7.2 Money numbers
| Number | How to calculate | Value | Source |
|--------|------------------|-------|--------|
| Money spent on getting customers | Ads + tools + paid help | | |
| CAC (cost per customer) | Money spent ÷ new paying customers | | |
| Average revenue per customer per month | Revenue ÷ customers | | |
| Gross margin | (Revenue − cost to serve) ÷ Revenue | | |
| Payback time | CAC ÷ (monthly revenue × margin) | | |
| Monthly recurring revenue (MRR) | Sum of monthly payments | | |

### 7.3 Product health numbers
| Number | Value | Source |
|--------|-------|--------|
| App/site crashes or errors per 100 sessions | | |
| Page load time (typical) | | |
| Support tickets per week | | |
| Average time to answer a ticket | | |
| Uptime (% of time working) | | |

> **[AI-BOX]** Check each conversion by dividing the lower stage by the stage above it. Re-calculate and flag any number that does not match. Never fill a "Change" cell without both periods filled.

---

## 8. Can We Trust Our Numbers? (Data Check)

**Do this in:** all phases. **Done when:** every `UNKNOWN` has a plan to find it.

### 8.1 Tick what is true
- [ ] We track visitors with a real tool (not guessing)
- [ ] We track sign-ups automatically
- [ ] We track the aha moment automatically
- [ ] We know where each customer came from (channel)
- [ ] Our own team and test accounts are removed from the numbers
- [ ] Payment numbers match our bank / payment tool
- [ ] We checked the numbers within the last 14 days

### 8.2 Missing numbers (one row per UNKNOWN)
| Missing number | Why it matters | How we will get it | Who | Date due |
|----------------|----------------|--------------------|-----|----------|
| | | | | |

### 8.3 How sure are we about our numbers overall? (tick one)
- [ ] High: tools match each other
- [ ] Medium: some gaps
- [ ] Low: mostly guesses (fix this before anything else)

> **[AI-BOX]** If 8.3 is `Low`, set a top-priority action in Section 28 called "Fix tracking" and warn the human that Sections 9 to 24 are provisional.

---

# PART B: FIND THE LEAKS

Think of a bucket with holes. You fill it from the top (visitors). Customers drip out through holes. We now find **where the holes are**.

---

## 9. Funnel Leak Finder

**Do this in:** LAUNCH and later (in BETA use beta testers). **Done when:** every stage has a conversion % and the biggest leak is circled.

### 9.1 Turn Section 7.1 into conversion rates
| From → To | Calculation | Our rate | Healthy rate for us (target) | Gap | Leak size (rank 1 = biggest) |
|-----------|-------------|----------|------------------------------|-----|------------------------------|
| Visitor → Sign-up | Sign-ups ÷ Visitors | % | % | | |
| Sign-up → Activated | Activated ÷ Sign-ups | % | % | | |
| Activated → Paying | Paying ÷ Activated | % | % | | |
| Paying → Still here at 30 days | Retained ÷ Paying | % | % | | |
| Customers → Referral | Referred ÷ Customers | % | % | | |

How to set "target": use your own best past rate, a goal from a similar product (write the source), or write `UNKNOWN - set after 2 weeks of data`. Do **not** copy random internet numbers without a source.

### 9.2 Which stage loses the most people (in absolute numbers)?
Example answer: `Sign-up → Activated: 400 sign-ups, only 80 activated. We lose 320 people here.`
Your answer:
> 

### 9.3 Is the leak the same for every group? Check these splits
| Split by | Best group and rate | Worst group and rate | What it tells us |
|----------|---------------------|----------------------|------------------|
| Where they came from (channel) | | | |
| Device (phone / computer) | | | |
| Country / language | | | |
| New vs returning | | | |
| Customer type | | | |

> **[AI-BOX]** Rank leaks by number of people lost, not just by percentage. A small % drop on a huge stage can lose more people than a large % drop on a tiny stage. Show your arithmetic.

---

## 10. Acquisition: Do People Find Us?

**Do this in:** LAUNCH, FIRST-100, 100-TO-500. (BUILD/BETA: write your plan.) **Done when:** every channel has numbers and a verdict.

### 10.1 List every channel we use
| Channel | Visitors | Sign-ups | Paying customers | Money spent | Cost per customer | Verdict (keep / fix / stop) |
|---------|----------|----------|------------------|-------------|-------------------|-----------------------------|
| Search engines (SEO) | | | | | | |
| Social media (organic) | | | | | | |
| Paid ads | | | | | | |
| Friends and family | | | | | | |
| Communities / forums | | | | | | |
| Email / newsletter | | | | | | |
| Partnerships / affiliates | | | | | | |
| App store search | | | | | | |
| Direct outreach (messages, calls) | | | | | | |
| Press / launch sites | | | | | | |
| Other: | | | | | | |

### 10.2 Which ONE channel gives us the most customers for the least money?
Your answer:
> 

### 10.3 Tick the problems that apply
- [ ] Too few people see us (not enough visitors)
- [ ] People see us but do not click
- [ ] People click but leave the page fast
- [ ] The page does not clearly say what we do
- [ ] The wrong kind of people arrive
- [ ] Our best channel is too small to reach 500
- [ ] Our channels cost too much per customer
- [ ] We rely on only one channel
- [ ] We stopped posting / outreach for a while
- [ ] Other: ________

### 10.4 Can our best channel reach 500 customers? Do the math
Why we ask: a channel can be great and still too small.
How: `Customers per week from channel × weeks left = customers we can expect`
Example answer: `6 per week × 20 weeks = 120. Not enough. Need 380 more from other channels.`
Your answer:
> 

---

## 11. Activation: Do People Get Value Fast?

**Do this in:** BETA and later. **Done when:** you know the % who reach "aha", how long it takes, and where the rest quit.

### 11.1 What % of sign-ups reach the aha moment? Time to get there?
Your answer:
> 

### 11.2 List each step in the first-use experience and how many people finish it
| Step | People who started | People who finished | Drop % | Why do they quit? (evidence) |
|------|--------------------|---------------------|--------|-------------------------------|
| Create account | | | | |
| Verify email / phone | | | | |
| Set up profile / settings | | | | |
| First main action | | | | |
| Aha moment | | | | |

### 11.3 Tick the problems that apply
- [ ] Too many steps before value
- [ ] Sign-up asks for too much information
- [ ] People do not understand what to do first
- [ ] The product is slow or buggy at first use
- [ ] Emails or notifications do not bring people back
- [ ] The product needs data the person does not have yet (empty screen)
- [ ] Needs a call or demo that people skip
- [ ] Other: ________

### 11.4 What is the single easiest way to cut the time-to-value in half?
Your answer:
> 

---

## 12. Retention: Do People Stay?

**Do this in:** LAUNCH and later (BETA: use tester return rates). **Done when:** you have a return rate for day 1, day 7, day 30 (or week 1, 4, 8 if you ship weekly products).

### 12.1 Fill the retention table (share of a group of new users who come back)
| Group (who joined in) | Size | Day 1 | Day 7 | Day 30 | Day 60 | Day 90 |
|-----------------------|------|-------|-------|--------|--------|--------|
| Week of ____ | | % | % | % | % | % |
| Week of ____ | | % | % | % | % | % |
| Week of ____ | | % | % | % | % | % |

### 12.2 Does the line level off or keep falling?
Why we ask: if the line levels off above zero, you have a core of people who keep using it. If it keeps sliding down to zero, you do not have a lasting habit yet. This is one of the most important signals in this document.
Tick one:
- [ ] Levels off at about ____ % (good sign)
- [ ] Keeps falling toward 0 (serious problem)
- [ ] Not enough data yet

### 12.3 Why do people leave? (from cancellations, exit surveys, interviews)
| Reason given | How many people | Source |
|--------------|-----------------|--------|
| | | |

### 12.4 Tick the problems that apply
- [ ] Product solves the problem only once
- [ ] Missing an important feature
- [ ] Too hard to use
- [ ] Too expensive for the value
- [ ] Bugs or slowness
- [ ] Forgot about us (no reminders)
- [ ] Competitor is better
- [ ] Bad customer support
- [ ] Other: ________

---

## 13. Revenue: Do People Pay (and Is It Worth It)?

**Do this in:** LAUNCH and later. **Done when:** you know cost per customer, money per customer, and payback time.

### 13.1 Do people who try it become paying customers? Where do payers drop?
| Step | People | Drop % | Evidence for the drop |
|------|--------|--------|------------------------|
| Saw the price | | | |
| Started checkout | | | |
| Finished payment | | | |
| Payment failed / retried | | | |

### 13.2 Is each customer worth more than they cost us?
Calculate: `Money we make from a customer over their life` minus `cost to get and serve them`.
Example answer: `They pay $9/month for about 8 months = $72. Cost to get them: $25. We keep $47 before serving costs.`
Your answer:
> 

### 13.3 Tick the problems that apply
- [ ] Price too high for what we show
- [ ] Price too low to survive
- [ ] People do not see why to pay (free is enough)
- [ ] Checkout is confusing or broken
- [ ] Payment methods missing for our customers' country
- [ ] Failed card payments lose customers
- [ ] Refunds are high
- [ ] We take too long to charge (no clear moment to pay)
- [ ] Other: ________

---

## 14. Referral: Do People Tell Others?

**Do this in:** FIRST-100 and 100-TO-500. (Earlier: write `N/A because ...` or your plan.) **Done when:** you know how many customers came from other customers.

### 14.1 How many new customers came from a friend or share? (number, % of all new customers, source)
Your answer:
> 

### 14.2 How do customers share us now?
- [ ] Share button inside the product
- [ ] Invite link / code
- [ ] Reward for inviting
- [ ] Public profiles or shared results
- [ ] Reviews / ratings requests
- [ ] Nothing yet
- [ ] Other: ________

### 14.3 Would customers recommend us? Ask 10 customers: "How likely are you to recommend us, 0 to 10?"
| Score 9 to 10 | Score 7 to 8 | Score 0 to 6 |
|---------------|--------------|--------------|
| ___ people | ___ people | ___ people |

(Net score = % who answered 9 to 10 minus % who answered 0 to 6.) Our score: ____

### 14.4 What stops people from sharing?
Your answer:
> 

---

## 15. Product Bottlenecks

**Do this in:** all phases. **Done when:** you checked every item.

### 15.1 Does the product do the main job well? Tick honestly
- [ ] The main feature works every time
- [ ] The main feature is easy to find
- [ ] The main feature is better than the old way (Section 2.3)
- [ ] We know the top 3 missing features, and customers named them
- [ ] We removed features nobody uses
- [ ] It works on the devices our customers use
- [ ] It is fast enough (see Section 7.3)
- [ ] It is accessible (readable text, works with a keyboard / screen reader)

### 15.2 Top 5 product problems
| # | Problem | How many customers hit it | Evidence | Fix size (small / medium / big) |
|---|---------|---------------------------|----------|----------------------------------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

### 15.3 What do customers ask for that we do not have? (top 3, with counts)
Your answer:
> 

---

## 16. Building and AI-Development Bottlenecks

**Do this in:** all phases, especially BUILD and BETA. **Why this section exists:** sometimes growth is slow because shipping is slow, buggy or risky, not because marketing is bad.

### 16.1 How fast can we ship a fix?
| Question | Our answer |
|----------|-----------|
| Time from "we found a problem" to "customers have the fix" | |
| How many releases per week | |
| How often a release breaks something | |
| Time to undo a bad release | |

### 16.2 Tick what is true about our build process
- [ ] We have automatic tests for the main customer path (sign-up, aha, pay)
- [ ] A person reviews every AI-written change before it goes live
- [ ] We can turn off a new feature quickly without a full release
- [ ] We have a staging / test copy of the product
- [ ] We get an alert when something breaks
- [ ] We keep a list of known bugs ranked by customer impact
- [ ] Our setup is written down so a new person can run it
- [ ] Backups exist and we tested restoring one

### 16.3 AI-assisted development check (skip with `N/A` if no AI is used)
| Question | Yes / No | Note |
|----------|----------|------|
| Do AI agents have written rules for what they may and may not change? | | |
| Is every AI change reviewed by a human before release? | | |
| Do we keep the AI's instructions (prompts) saved and versioned? | | |
| Do AI tools ever touch customer data or secrets? If yes, how is that controlled? | | |
| Have AI-written parts caused customer-facing bugs? How many? | | |
| Is the AI cost per month known and inside budget? | | |

### 16.4 What in the build or release process slows growth the most?
Example answer: `Every release needs 2 days of manual testing, so we ship fixes only on Fridays.`
Your answer:
> 

> **[HUMAN CHECKPOINT]** An engineer or technical owner signs off that 16.1 to 16.3 are true. Name: ________ Date: ________

---

## 17. People, Time and Money Bottlenecks

**Do this in:** all phases. **Done when:** you named which limit hurts most.

### 17.1 Tick what is true
- [ ] One person is doing too many jobs
- [ ] Nobody owns marketing / customer conversations
- [ ] Nobody owns customer support
- [ ] We run out of money before 500 customers at the current pace
- [ ] We lack a skill (name it): ________
- [ ] Decisions wait too long for approval
- [ ] Our team works in different time zones and misses handoffs
- [ ] We are overbuilding instead of talking to customers

### 17.2 Money runway
| Item | Amount |
|------|--------|
| Cash we have | |
| Money spent per month (all costs) | |
| Months we can keep going | Cash ÷ monthly spend = ___ |
| Will we hit 500 before the money ends? | Yes / No / Unsure |

### 17.3 Hours check: where do the team's hours go each week?
| Activity | Hours |
|----------|-------|
| Building the product | |
| Talking to customers | |
| Marketing / outreach | |
| Support | |
| Admin / meetings | |
| Other | |

---

## 18. Trust, Legal and Platform Bottlenecks

**Do this in:** all phases. **Done when:** each item is Yes, No or N/A with a reason.

### 18.1 Tick what is true
- [ ] Our privacy policy and terms are published
- [ ] We follow the privacy rules of countries where customers live (GDPR, etc.)
- [ ] We ask permission before sending marketing emails
- [ ] Customers can delete their data
- [ ] Payments use a trusted payment provider
- [ ] People can find real reviews, proof or examples that we are real
- [ ] App store / platform rules are met and no approvals are stuck
- [ ] Our email lands in the inbox, not spam
- [ ] We depend on one platform that could block us (name it): ________

### 18.2 Anything waiting on someone else? (approval, review, partner, bank)
| What | Waiting on | Since (date) | Impact on customers |
|------|-----------|--------------|---------------------|
| | | | |

### 18.3 Do customers trust us enough to give us their money or data? Evidence:
Your answer:
> 

---

## 19. What Customers Actually Said

**Do this in:** BETA and later. **Done when:** at least **10 real customer or tester conversations** are summarized (more is better).

### 19.1 Who we talked to
| # | Name or ID | Customer type | Date | How (call / chat / survey) | Did they pay? |
|---|------------|---------------|------|-----------------------------|---------------|
| 1 | | | | | |
| 2 | | | | | |

### 19.2 What did they say? (use their words in quotes)
| Theme | Exact words | How many people said it |
|-------|-------------|-------------------------|
| What they love | | |
| What confused them | | |
| What stopped them from paying | | |
| Why they left (if they did) | | |
| What they would use instead | | |

### 19.3 People who did NOT sign up or left: did we ask them why?
- [ ] Yes (how many: ____)
- [ ] No (add to Section 28)

### 19.4 The top 3 things we learned that surprised us
Your answer:
> 

> **[AI-BOX]** Never invent quotes. Only copy words from the human's notes, surveys or transcripts, and cite where they came from. If fewer than 10 conversations exist, write `Evidence is thin` at the top of Section 21.

---

# PART C: PICK THE FIX

---

## 20. Product-Market Fit Signals

**Do this in:** BETA and later. **Done when:** every signal is marked, and the overall verdict is chosen.

Product-market fit means: a good number of the right people want your product badly enough to keep using it and to pay.

### 20.1 The "How disappointed would you be?" test
Ask active users (people who used it at least twice): **"How would you feel if you could no longer use this?"**
Options: Very disappointed / Somewhat disappointed / Not disappointed / I no longer use it.

| Answer | People | % |
|--------|--------|---|
| Very disappointed | | |
| Somewhat disappointed | | |
| Not disappointed | | |
| No longer use it | | |
| **Total** | | 100% |

A commonly used rule of thumb is that **about 40% or more "very disappointed"** suggests you may have fit. Treat this as a hint, not proof, especially with fewer than 40 answers. Number of answers: ____

### 20.2 Mark each signal
| Signal | Yes | Partly | No | Evidence |
|--------|-----|--------|----|----------|
| Retention line levels off (Section 12.2) | [ ] | [ ] | [ ] | |
| Customers return without us nagging | [ ] | [ ] | [ ] | |
| Customers pay without big discounts | [ ] | [ ] | [ ] | |
| Customers bring friends on their own | [ ] | [ ] | [ ] | |
| Customers describe the problem the way we do | [ ] | [ ] | [ ] | |
| Customers complain loudly when something breaks | [ ] | [ ] | [ ] | |
| Sales or sign-ups are getting easier, not harder | [ ] | [ ] | [ ] | |

### 20.3 Overall verdict (tick one)
- [ ] **Strong fit**: most signals are Yes. Focus on growth (Acquisition).
- [ ] **Early fit**: mixed. Focus on retention and activation before spending on growth.
- [ ] **No fit yet**: mostly No. Go back to customers and the problem. Do not scale ads.
- [ ] **Too early to tell**: not enough data (say what data is needed).

> **[AI-BOX]** If the verdict is `No fit yet` or `Early fit`, do **not** recommend an Acquisition bottleneck in Section 21 unless the human explicitly overrides with a written reason. Pouring visitors into a leaky product wastes money.

---

## 21. Find THE One Bottleneck

**Do this in:** all phases (after Part B). **Done when:** ONE bottleneck is named, with evidence and a way to know it is fixed.

The rule: **at any time, only one thing is the biggest limit.** Fix it, then look for the next one. This is the "Theory of Constraints", used in factories and growth teams.

### 21.1 Collect the top suspect from each area
| Area | Biggest problem found (from Part B) | Numbers that prove it | How many people it affects |
|------|-------------------------------------|----------------------|----------------------------|
| Finding us (Acquisition, Sec 10) | | | |
| First value (Activation, Sec 11) | | | |
| Staying (Retention, Sec 12) | | | |
| Paying (Revenue, Sec 13) | | | |
| Sharing (Referral, Sec 14) | | | |
| Product (Sec 15) | | | |
| Building / shipping (Sec 16) | | | |
| People / time / money (Sec 17) | | | |
| Trust / legal / platform (Sec 18) | | | |

### 21.2 Test each suspect with this question
"If we fixed ONLY this, would we reach 500 customers noticeably faster?"

| Suspect | Would fixing it speed us up? (Big / Some / None) | Why |
|---------|--------------------------------------------------|-----|
| | | |

### 21.3 Pick the one bottleneck (write it in ONE sentence)
Format: `Because of ____ , we lose ____ people (____ %) at ____ , which is stopping us from reaching 500 customers.`
Example answer: `Because new users cannot add their first plant, we lose 320 of 400 sign-ups (80%) before the aha moment, which is stopping us from reaching 500 customers.`
Your answer:
> 

### 21.4 How confident are we? (tick one)
- [ ] High: numbers and customer words agree
- [ ] Medium: numbers or words, not both
- [ ] Low: mostly a hunch (collect more data first, then come back)

### 21.5 The runner-up bottleneck (we fix this next)
Your answer:
> 

### 21.6 "Fixed" means... (a number and a date)
Example answer: `Activation rises from 20% to 45% by 2026-11-30, measured in analytics.`
Your answer:
> 

> **[AI-BOX]** Copy the sentence from 21.3 into `the_one_bottleneck` in the YAML header. Refuse to pick more than one. If two seem equal, pick the one earlier in the customer journey and put the other in 21.5.

> **[HUMAN CHECKPOINT]** The owner agrees this is THE bottleneck. Name: ________ Date: ________ ☐ Agreed

---

## 22. Find the Root Cause (5 Whys)

**Do this in:** all phases. **Done when:** the last "why" points to something we can actually change.

Keep asking "Why?" until you reach a cause you can fix. Usually 3 to 5 times.

### 22.1 Fill the chain
| Level | Question | Answer (with evidence) |
|-------|----------|------------------------|
| Problem | What is the bottleneck? (from 21.3) | |
| Why 1 | Why does this happen? | |
| Why 2 | Why does that happen? | |
| Why 3 | Why does that happen? | |
| Why 4 | Why does that happen? | |
| Why 5 | Why does that happen? | |
| **Root cause** | The thing we can change | |

Example:
- Problem: people do not add their first plant.
- Why 1: The "Add plant" button is on the third screen.
- Why 2: We built the settings screen first.
- Why 3: We copied another app's layout without testing.
- Root cause: We never watched a new user try it.

### 22.2 How do we know this is the real cause? (not just a guess)
Tick what you have:
- [ ] Data shows it (graphs / counts)
- [ ] We watched real people struggle (screen recordings or live)
- [ ] Customers told us directly
- [ ] We tried a quick fix and saw a change
- [ ] Only a guess (go and collect evidence before Section 23)

---

## 23. Fix Ideas and Scoring (ICE / RICE)

**Do this in:** all phases. **Done when:** at least 8 ideas are scored, top 3 chosen.

### 23.1 Brainstorm: list fix ideas for THE one bottleneck (at least 8). No idea is silly.
| ID | Idea (one line) | Type: Quick fix / Feature / Message / Price / Channel / Process |
|----|-----------------|--------------------------------------------------------------------|
| I1 | | |
| I2 | | |
| I3 | | |
| I4 | | |
| I5 | | |
| I6 | | |
| I7 | | |
| I8 | | |

### 23.2 Score with ICE (fast, good for early stages)
Give each a score from **1 (low) to 10 (high)**:
- **Impact**: if it works, how much does it move our number?
- **Confidence**: how sure are we it will work? (evidence raises this)
- **Ease**: how easy and quick is it? (10 = a day, 1 = months)

**ICE score = (Impact + Confidence + Ease) ÷ 3**   (or multiply the three: pick one method and use it every time; write it here: ________)

| ID | Impact | Confidence | Ease | ICE score | Rank |
|----|--------|------------|------|-----------|------|
| I1 | | | | | |
| I2 | | | | | |
| I3 | | | | | |

### 23.3 Optional, RICE (use from FIRST-100 onward when you have counts)
**RICE = (Reach × Impact × Confidence) ÷ Effort**
- **Reach**: how many people per month it touches (a number)
- **Impact**: 3 = huge, 2 = high, 1 = medium, 0.5 = low, 0.25 = tiny
- **Confidence**: 100% = strong evidence, 80% = some, 50% = hunch
- **Effort**: person-weeks to do it

| ID | Reach | Impact | Confidence | Effort | RICE | Rank |
|----|-------|--------|-----------|--------|------|------|
| | | | | | | |

### 23.4 Our top 3 picks, and why
| Rank | Idea ID | Why this one |
|------|---------|--------------|
| 1 | | |
| 2 | | |
| 3 | | |

> **[AI-BOX]** Show the arithmetic for every score. Do not let all ideas score the same. If three ideas tie, break the tie with "cheapest to test first." Flag any score of Confidence ≥ 8 that has no evidence listed.

---

## 24. Experiment Plan

**Do this in:** all phases. **Done when:** each top idea has a test with a pass/fail rule written **before** you run it.

### 24.1 One experiment card per idea (copy this card for each)

**Experiment ID:** E1   **Idea ID:** ____   **Owner:** ____

| Question | Answer |
|----------|--------|
| What do we believe? ("If we ____, then ____ will go from ____ to ____ because ____.") | |
| Who is in the test? (which people, how many) | |
| What exactly will we change? | |
| What number decides success? (metric name) | |
| Success looks like (write a number) | |
| Failure looks like (write a number) | |
| Start date → End date | |
| How long do we need to run? (enough people, not just days) | |
| What could go wrong? Safety limit (when we stop early) | |
| Cost (money and hours) | |
| Tool / where we measure | |
| Result (fill after the test) | |
| What we learned | |
| Decision (Keep / Change / Drop / Run again) | |

Example "What do we believe?": `If we move "Add plant" to the first screen, then activation will go from 20% to 40% because users will reach the aha moment in under 2 minutes.`

### 24.2 Experiment list
| ID | Idea | Metric | Start | End | Result | Decision |
|----|------|--------|-------|-----|--------|----------|
| E1 | | | | | | |
| E2 | | | | | | |
| E3 | | | | | | |

### 24.3 Rules for fair tests
- [ ] Change **one thing at a time** where possible
- [ ] Write the success number **before** you start
- [ ] Do not stop early just because it looks good or bad (unless the safety limit is hit)
- [ ] Count only real customers (no test accounts)
- [ ] Record the result even when the test fails (failures teach us)

> **[AI-BOX]** Never mark an experiment as `success` unless the result cell has a measured number and its source. With very small samples (for example under 30 people per group), say so and recommend longer testing instead of declaring victory.

---

# PART D: CHECK AND DECIDE

---

## 25. Phase Gate Check (Can We Move Forward?)

**Do this in:** at the end of every phase. **Done when:** a clear GO / HOLD / STOP decision is written.

A "gate" is a door. You only move to the next phase when the checklist is ready.

### 25.1 BUILD → BETA
- [ ] The main journey works start to finish (sign-up → aha → pay or save)
- [ ] 5 to 10 target customers agreed to test it
- [ ] Tracking is set up (Section 8.1 mostly ticked)
- [ ] Known serious bugs are fixed
- [ ] Privacy basics are done (Section 18)
- [ ] A way exists to collect feedback

### 25.2 BETA → LAUNCH
- [ ] Most testers reached the aha moment without our help
- [ ] At least a few testers came back on their own
- [ ] Top 3 problems from testers are fixed or planned
- [ ] Payments work and were tested with a real small payment
- [ ] Support process exists (who answers, how fast)
- [ ] The product can handle our expected first-week visitors
- [ ] A rollback plan exists

### 25.3 LAUNCH → FIRST-100
- [ ] Strangers (not friends) signed up
- [ ] At least one channel brought strangers
- [ ] We have real funnel numbers (Section 7.1 filled)
- [ ] We talked to at least 10 real users (Section 19)
- [ ] The one bottleneck is named (Section 21)

### 25.4 FIRST-100 → 100-TO-500
- [ ] We reached about 100 customers by our definition (Section 5)
- [ ] Retention line is flat or rising at some level (Section 12.2)
- [ ] At least one channel is repeatable (we can say what to do to get more)
- [ ] Cost per customer is lower than what a customer pays us over time (Section 13.2)
- [ ] Support and servers handle double the current load
- [ ] PMF verdict is "Strong fit" or "Early fit" (Section 20.3)

### 25.5 100-TO-500 → DONE (500 customers)
- [ ] 500 customers counted by our exact definition and verified against payment records
- [ ] Retention, revenue and channel mix still healthy
- [ ] Lessons are written down (Section 27 and the Review Log)
- [ ] Next goal chosen (for example 5,000) and a new copy of this document started

### 25.6 Decision for this gate
| Gate | Date | Decision (GO / HOLD / STOP) | Reason | Approved by |
|------|------|----------------------------|--------|-------------|
| | | | | |

> **[HUMAN CHECKPOINT]** Only a human may write GO. AI agents may recommend, not decide.

---

## 26. Risks and Assumptions

**Do this in:** all phases. **Done when:** top 5 risks each have an owner and a plan.

### 26.1 Our assumptions (things we believe but have not proven)
| # | Assumption | How we will test it | Tested? Result |
|---|------------|---------------------|----------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |

### 26.2 Risk list
Score likelihood and damage from 1 (low) to 5 (high). **Risk score = Likelihood × Damage.**

| # | What could go wrong | Likelihood | Damage | Score | What we will do to prevent or reduce it | Owner |
|---|---------------------|------------|--------|-------|------------------------------------------|-------|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

### 26.3 What would make us stop or change direction? (write number-based "tripwires")
Example answer: `If day-30 retention is under 10% after 3 weekly groups, we pause paid ads and fix the product.`
Your answer:
> 

---

## 27. Decision Log

**Do this in:** all phases. Add a row any time a decision changes the plan. **Done when:** future-you can see what changed and why.

| ID | Date | Decision | Why (evidence) | Alternatives we rejected | Who decided |
|----|------|----------|----------------|--------------------------|-------------|
| D1 | | | | | |
| D2 | | | | | |

---

## 28. Action Plan (Who Does What by When)

**Do this in:** all phases. **Done when:** every action has one owner and one date.

| # | Action (start with a verb) | Linked to (Section / Experiment) | Owner | Due date | Status (To do / Doing / Done / Blocked) |
|---|----------------------------|----------------------------------|-------|----------|------------------------------------------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

### 28.1 What is blocked, and who can unblock it?
Your answer:
> 

### 28.2 What will we **stop** doing to make room for the above?
Your answer:
> 

---

## 29. Review Log (Repeat Every 1 to 2 Weeks)

**Do this in:** all phases from LAUNCH. Copy a new row each review. **Done when:** every review has numbers, a verdict and a next step.

| Review date | Phase | Customers (total) | New since last review | On pace for goal? (Yes / No) | Biggest bottleneck now | Last experiment result | What changed | Next review date | Reviewer |
|-------------|-------|-------------------|-----------------------|------------------------------|------------------------|------------------------|--------------|------------------|----------|
| | | | | | | | | | |
| | | | | | | | | | |
| | | | | | | | | | |

### 29.1 Review questions (answer each time, keep it to 5 minutes)
1. Did the number we wanted to move actually move? By how much?
2. Is the bottleneck still the same? If not, what is it now?
3. What did we learn from customers this week?
4. What will we do differently next week?
5. Is the YAML header up to date? (phase, customers, bottleneck, dates)

> **[AI-BOX]** When asked to run a review: (1) read the last row of this table, (2) ask the human for the new numbers, (3) recompute Sections 7 and 9 only, (4) re-check Section 21 and say if the bottleneck moved, (5) append a new row, (6) update the YAML header. Do not rewrite other sections.

---

## 30. Final Quality Checklist

Do this **before** setting `status: IN-REVIEW`. An AI agent should run it and report which boxes fail.

### Completeness
- [ ] The YAML header is fully filled
- [ ] No section is blank (each has an answer, `UNKNOWN` plus a plan, or `N/A because ...`)
- [ ] Every number has a date and a source
- [ ] Every `UNKNOWN` appears in Section 8.2 with an owner and a due date

### Correctness
- [ ] Conversion math was re-checked (Section 7 and 9)
- [ ] "Customer" is defined once (Section 5) and used the same everywhere
- [ ] No quote is invented; each came from a real conversation or survey (Section 19)
- [ ] Targets and goals have a number and a date

### Clarity
- [ ] A person who has never seen this project can read Sections 1 to 4 and understand it
- [ ] Short sentences, no unexplained jargon
- [ ] Only ONE bottleneck is named in Section 21 (a runner-up is allowed in 21.5)

### Action
- [ ] Top 3 ideas have experiment cards with success numbers written **before** the test
- [ ] Every action in Section 28 has one owner and one date
- [ ] A review date is set in the header and in Section 29

### Sign-off
| Role | Name | Date | Approved |
|------|------|------|----------|
| Document owner | | | [ ] |
| Product / growth lead | | | [ ] |
| Technical owner (Section 16) | | | [ ] |
| Final approver | | | [ ] |

> **[HUMAN CHECKPOINT]** Do not set `status: APPROVED` until all four sign-offs above are ticked.

---

# APPENDICES

---

## Appendix A: Metric Cheat Sheet

| Metric | Formula | What it tells you |
|--------|---------|-------------------|
| Conversion rate | People who moved to next step ÷ people at this step | Where the leak is |
| Activation rate | Activated users ÷ sign-ups | Do people get value fast? |
| Time to value | Time from sign-up to aha moment | How quickly we deliver |
| Retention (day N) | Users still active on day N ÷ users who started | Do people stay? |
| Churn rate | Customers lost in a period ÷ customers at start of period | How fast people leave |
| CAC | Money spent on getting customers ÷ new customers | Cost to win one customer |
| ARPU | Revenue ÷ customers | Average money per customer |
| Gross margin | (Revenue − cost to serve) ÷ Revenue | How much we keep |
| LTV (simple) | ARPU × gross margin ÷ monthly churn rate | Rough lifetime value of a customer |
| LTV : CAC | LTV ÷ CAC | Is a customer worth the cost? A commonly quoted rule of thumb is about 3 or higher, but check what fits your business |
| CAC payback | CAC ÷ (monthly revenue per customer × margin) | Months to earn back the cost; shorter is safer |
| Net promoter score | % answering 9 to 10 minus % answering 0 to 6 | Would people recommend us? |
| Viral coefficient | Invites sent per customer × share of invites that convert | Do customers bring customers? |
| Pace to goal | (Goal − customers today) ÷ weeks left | Customers needed per week |

> Benchmark numbers vary a lot by product type, price and country. Always compare to **your own past numbers first**, and write the source of any outside number you use.

---

## Appendix B: Worked Mini-Example (shortened, fictional)

**Product:** PlantPal, a phone app that reminds people to water plants. Goal: 500 paying customers by 2027-03-31. Phase: FIRST-100, 37 paying customers.

**Section 7.1 (last 30 days):** Visitors 4,000 → Sign-ups 400 → Activated 80 → Paying 37 → Still here at 30 days 22.

**Section 9.1:**
- Visitor → Sign-up: 400 ÷ 4,000 = 10%
- Sign-up → Activated: 80 ÷ 400 = 20% (lose 320 people)
- Activated → Paying: 37 ÷ 80 = 46%
- Paying → 30 days: 22 ÷ 37 = 59%

**Biggest leak by people lost:** Sign-up → Activated (320 lost).

**Section 21.3 (bottleneck):** Because new users cannot add their first plant easily, we lose 320 of 400 sign-ups (80%) before the aha moment, which is stopping us from reaching 500 customers.

**Section 22 (root cause):** We never watched a new user try the app.

**Section 23 (top idea):** Move "Add plant" to the first screen and add a sample plant. Impact 8, Confidence 7, Ease 8 → ICE ≈ 7.7.

**Section 24 (experiment):** If we move "Add plant" to the first screen, activation goes from 20% to 40% within 2 weeks. Success = at least 35% with at least 200 new sign-ups. Failure = under 25%.

**Section 29 (review):** After 2 weeks, activation rose to 38%. Decision: keep. New bottleneck: payment drop at checkout.

This shows the loop: **measure → find the leak → find the cause → test a fix → measure again.**

---

## Appendix C: AI Agent Master Prompt

Copy and paste this to an AI agent (like Claude) along with this document:

```
You are helping me fill out Growth_Bottleneck_Analysis.md for my project.

Rules:
1. Read the whole document first, then the YAML header.
2. Work one section at a time, in order, starting from the section I name.
3. Ask me ONE question at a time, in simple words, using the questions in the document.
4. Never invent numbers, quotes or sources. If I do not know, write UNKNOWN and add it to Section 8.2.
5. Show your arithmetic for every conversion, score and total.
6. Stop at every [HUMAN CHECKPOINT] and wait for my yes.
7. After each section, check it against its "Done when" line and tell me what is missing.
8. Keep the document structure unchanged. Do not delete or rename sections.
9. When I say "run a review", follow the AI-BOX in Section 29.
10. At the end, run Section 30 and list every box that fails.
```

### What an AI agent may do and may not do

| May | May not |
|-----|---------|
| Draft answers from facts I give | Invent customer quotes or numbers |
| Calculate rates, scores and totals | Approve a phase gate or sign-off |
| Point out missing or inconsistent data | Pick more than one bottleneck |
| Suggest experiments and ideas | Run experiments or spend money without my approval |
| Summarize interview notes I provide | Change the definition of "customer" without logging it in Section 27 |

---

## Appendix D: Glossary

| Word | Meaning |
|------|---------|
| A/B test | Show two versions to two groups and compare results |
| Activation | The first time a person gets the main value |
| Acquisition | Getting people to find and try the product |
| AARRR | A funnel in five parts: Acquisition, Activation, Retention, Revenue, Referral |
| Bottleneck | The one limit that slows everything else down |
| Channel | A place where customers come from (search, ads, social, etc.) |
| Churn | Customers who leave |
| Cohort | A group of people who started in the same period |
| Conversion rate | Share of people who go to the next step |
| CAC | Customer acquisition cost |
| Funnel | The path from stranger to loyal customer |
| Gate | A checklist you pass before moving to the next phase |
| ICE | A simple score: Impact, Confidence, Ease |
| Leak | A step where many people quit |
| LTV | Lifetime value: total money a customer brings |
| MRR | Monthly recurring revenue |
| Product-market fit | The right people want your product badly enough to keep it and pay |
| RICE | A score: Reach, Impact, Confidence, Effort |
| Retention | People who keep coming back |
| Rollback | Going back to the last working version |
| Root cause | The deepest cause you can actually fix |
| Theory of Constraints | Find the one biggest limit, fix it, then find the next |
| Time to value | How long until the person feels the benefit |

---

## Appendix E: Further Reading

Frameworks used in this template: AARRR "pirate metrics" (Dave McClure), Theory of Constraints (Eliyahu Goldratt), the "very disappointed" product-market fit survey (Sean Ellis), ICE scoring (Sean Ellis) and RICE scoring (Intercom), and the "5 Whys" (Toyota).

Pages found while preparing this template (read them to go deeper; check the date on each):
- [AARRR Pirate Metrics: The Complete Framework for Startup Growth (2026 guide)](https://www.koji.so/docs/aarrr-pirate-metrics-framework)
- [What is the AARRR funnel? (Uxcel)](https://uxcel.com/glossary/aarrr-funnel)
- [Which Metric Should You Use to Calculate Product-Market Fit? (Built In)](https://builtin.com/product-management/product-market-fit)
- [The SaaS Metrics That Actually Matter for Early Founders](https://site.cut-the-saas.com/guides/saas-metrics-to-track)
- [GTM Metrics That Actually Matter: A Founder's Dashboard](https://upgrowth.in/gtm-metrics-that-actually-matter-a-founders-dashboard/)

---

*End of template. Version 1.0. Copy this file for each new project, keep the structure, and fill it in from the top.*
