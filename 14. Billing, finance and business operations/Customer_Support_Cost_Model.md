# How to fill in this document (read this first, 3 minutes)

**What this file is:** one reusable form that works out what customer support will cost you, from the day you start building your product until your **first 500 paying customers**. Copy it once per project. Do not change the section order, so that every project looks the same.

**Who can fill it in:** anyone. If you can answer "How many customers do you expect?" you can do this. You do not need to know finance or support jargon. Every hard word is explained in the Glossary (Section 19).

## The 6 rules

1. **Answer every question.** Never leave a blank. Write a number, `Yes`, `No`, or `N/A - because [reason]`.
2. **Never write "TBD", "later" or "approx."** Write your best guess as a number and mark it 🟡 (see rule 3).
3. **Mark every number with a color dot:**
   - 🟢 **Known**: you have a bill, a contract, a payslip or a real measurement.
   - 🟡 **Guess**: your best estimate. Add one line about it in the Assumptions Log (Section 15).
   - 🔴 **No idea**: write a guess anyway, mark it 🔴, and name who can find out. Fix all 🔴 before launch.
4. **Money is in USD per month** unless a cell says "one-time". If you use another currency, write it in Section 0 and use it everywhere.
5. **Do the math in Section 11, not in your head.** Each formula is written in plain words with an example.
6. **Do not delete any section.** If a section does not apply, write `N/A - because [reason]`.

## How to use the symbols

| Symbol | Meaning |
|---|---|
| `[ ]` | A checkbox. Change it to `[x]` to tick it. |
| `____` | A blank to fill in. Replace the line with your answer. |
| 🟢 🟡 🔴 | How sure you are (see rule 3). |
| ➡️ | "Go to this section next." |
| 💡 | A tip. |
| ⚠️ | A warning. Read it twice. |

## Order of work (about 2 to 4 hours the first time)

1. Section 0 and 1: who you are and what you sell (15 min)
2. Sections 2 to 5: phases, tickets, channels, AI helper (60 min)
3. Sections 6 to 10: what each cost line is (60 min)
4. Section 11 to 14: let the formulas calculate (30 min)
5. Sections 15 to 18: assumptions, risks, check, sign-off (30 min)

💡 **If an AI assistant is filling this in for you:** it must not invent numbers. It must write 🟡 or 🔴 next to anything it guessed, and it must list every guess in Section 15. A person must approve it in Section 18.

💡 **Stuck?** Check the Worked Example (Section 17). It is a fully filled-in fictional project.

---

# Customer Support Cost Model

> **Template version:** 1.0 | **Template last reviewed:** 2026-10-19 | **Scope:** development → launch → first 500 customers

## Section 0. Document control

*Why this matters: so anyone who opens this file knows whose it is and whether it is current.*

| Question | Your answer |
|---|---|
| Project name | ____ |
| Product in one sentence (what does it do, for whom?) | ____ |
| Document owner (one person, name and role) | ____ |
| Person who approves it (name and role) | ____ |
| Date filled in (YYYY-MM-DD) | ____ |
| Version (start at 0.1, use 1.0 once approved) | ____ |
| Status | [ ] Draft  [ ] In review  [ ] Approved |
| Currency used | [ ] USD  [ ] Other: ____ |
| Cost period used | [ ] Per month (default)  [ ] Other: ____ |
| Next review date (suggest: every phase end) | ____ |

---

## Section 1. Project snapshot

*Why this matters: the answers here decide how many support tickets you will get and how expensive each one is.*

**1.1 What kind of product is it?** (tick one)
- [ ] Software / app you pay for monthly (subscription)
- [ ] Software with a one-time purchase
- [ ] Physical product with an app
- [ ] Online marketplace
- [ ] Service with a platform (for example, payments, delivery)
- [ ] Other: ____

**1.2 Who are your customers?** (tick one)
- [ ] Everyday people (consumers)
- [ ] Small businesses
- [ ] Large companies
- [ ] Mixed

**1.3 Numbers about the business**

| Question | Your answer | Sure? |
|---|---|---|
| Price one customer pays per month (USD) | $____ | 🟢🟡🔴 |
| Is there a free plan or free trial? | [ ] Yes, ____ days / forever  [ ] No | 🟢🟡🔴 |
| Out of 100 sign-ups, how many become paying customers? | ____ % | 🟢🟡🔴 |
| Out of 100 paying customers, how many leave each month? | ____ % | 🟢🟡🔴 |
| How complex is the product to use? | [ ] Easy  [ ] Medium  [ ] Hard (needs training) | 🟢🟡🔴 |
| Does the product handle money, health, or personal data? | [ ] Yes  [ ] No | 🟢🟡🔴 |
| In which countries / time zones are your customers? | ____ | 🟢🟡🔴 |
| Languages support must speak | ____ | 🟢🟡🔴 |

⚠️ If you answered "Yes" to money, health or personal data, support is slower and costs more because agents must verify who the customer is. Raise your handle time in Section 6.

**1.4 What does "good support" mean for this project?** (tick up to three)
- [ ] Fast replies
- [ ] Solving the problem in one conversation
- [ ] Lowest possible cost
- [ ] Friendly, human feel
- [ ] Available 24/7
- [ ] Meeting legal or contract requirements

---

## Section 2. Lifecycle phases (development to 500 customers)

*Why this matters: support costs change a lot between "building" and "500 customers". Splitting time into 5 phases stops you from guessing one number for everything.*

**2.1 Fill in the dates and goals.**

| Phase | What happens | Start date | End date | Customers at end of phase | Who does support? |
|---|---|---|---|---|---|
| **P1 Build** | Product is being built. No customers yet. | ____ | ____ | 0 | ____ |
| **P2 Beta / pre-launch** | Small group tests the product. Often free. | ____ | ____ | ____ (suggest 10 to 30) | ____ |
| **P3 Launch** | Product is public. The first paying customers arrive. | ____ | ____ | ____ (suggest 50) | ____ |
| **P4 Customers 1 to 100** | Early growth. Many questions. | ____ | ____ | 100 | ____ |
| **P5 Customers 101 to 500** | Real growth. Support must scale. | ____ | ____ | 500 | ____ |

**2.2 What must be true before moving to the next phase? (the "gate")**

| Phase | Support readiness gate. Tick when true. |
|---|---|
| P1 → P2 | [ ] Help articles drafted for the top 10 questions  [ ] Support email or chat set up  [ ] AI helper tested on 50 sample questions  [ ] Owner of support named |
| P2 → P3 | [ ] Beta questions turned into help articles  [ ] Answers to "who do I call when it breaks" written  [ ] Hand-off from AI to human tested  [ ] Costs in this file updated with real beta data |
| P3 → P4 | [ ] First-response target met for 4 weeks in a row  [ ] Top 5 repeat questions have help articles  [ ] Cost per ticket measured, not guessed |
| P4 → P5 | [ ] A second person (or vendor) trained to cover support  [ ] AI answers checked weekly  [ ] Monthly cost within 20% of this plan |
| P5 done (500 customers) | [ ] Real costs compared with this plan  [ ] A new plan written for the next 500 |

**2.3 How AI-driven development connects to support (answer each)**

| Question | Your answer |
|---|---|
| Will AI tools help write your help articles from your product notes? | [ ] Yes  [ ] No |
| Will AI tools help write, test or fix the product code? | [ ] Yes  [ ] No |
| If code is written or changed by AI, how fast could a bug reach customers? | [ ] Same day  [ ] Within a week  [ ] Slower |
| Who checks that AI-written help articles are true before customers see them? | ____ |
| Who is told when a new product release changes how something works, so support can update help articles? | ____ |

💡 Fast, AI-assisted releases mean help articles go out of date faster. If you ship often, raise the "help article upkeep" hours in Section 6.

---

## Section 3. How many questions will customers ask?

*Why this matters: this is the biggest driver of cost. A "ticket" is one customer request for help, such as an email, chat, call or form.*

**3.1 Tickets per customer per month**

Think: "In one month, how many times will one average customer contact support?" Early customers ask more because the product and help articles are not polished.

| Customers | Tickets per customer per month | Sure? | Why you chose it |
|---|---|---|---|
| 10 | ____ | 🟢🟡🔴 | ____ |
| 50 | ____ | 🟢🟡🔴 | ____ |
| 100 | ____ | 🟢🟡🔴 | ____ |
| 250 | ____ | 🟢🟡🔴 | ____ |
| 500 | ____ | 🟢🟡🔴 | ____ |

💡 Usual pattern: the number goes **down** as you fix the product and write help articles. If yours goes up, write why in the last column.

**3.2 What will customers ask about?** List the top question types. The shares must add up to 100%.

| # | Question type (example: "I forgot my password") | Share of all tickets | Easy / Medium / Hard | Can AI answer it fully? | Needs a human? |
|---|---|---|---|---|---|
| 1 | ____ | ____ % | ____ | [ ] Yes [ ] Partly [ ] No | [ ] Yes [ ] No |
| 2 | ____ | ____ % | ____ | [ ] Yes [ ] Partly [ ] No | [ ] Yes [ ] No |
| 3 | ____ | ____ % | ____ | [ ] Yes [ ] Partly [ ] No | [ ] Yes [ ] No |
| 4 | ____ | ____ % | ____ | [ ] Yes [ ] Partly [ ] No | [ ] Yes [ ] No |
| 5 | ____ | ____ % | ____ | [ ] Yes [ ] Partly [ ] No | [ ] Yes [ ] No |
| 6 | Billing or refund questions | ____ % | ____ | [ ] Yes [ ] Partly [ ] No | [ ] Yes [ ] No |
| 7 | Bugs and "it's broken" reports | ____ % | ____ | [ ] Yes [ ] Partly [ ] No | [ ] Yes [ ] No |
| 8 | Other | ____ % | ____ | [ ] Yes [ ] Partly [ ] No | [ ] Yes [ ] No |
| | **Total** | **100 %** | | | |

**3.3 Busy times**
- Which days or events will cause a spike (launch day, price change, outage, holiday)? ____
- During a spike, how many times more tickets than normal? ____ ×
- Who covers a spike? ____

---

## Section 4. Support channels

*Why this matters: each way of reaching you has a different cost. Chat and phone cost more per contact than email. A help center costs almost nothing per use.*

**4.1 Which channels will you offer, and when?** Tick the first phase in which each is live.

| Channel | Offer it? | Live from phase | Hours | Share of all tickets (all must total 100%) | Reply-time target | Extra cost in plain words |
|---|---|---|---|---|---|---|
| **Email / ticket form** | [ ] Yes [ ] No | P__ | ____ | ____ % | ____ hours | Agent time |
| **Live chat / in-app chat** | [ ] Yes [ ] No | P__ | ____ | ____ % | ____ minutes | Agent time plus chat software |
| **Phone / video calls** | [ ] Yes [ ] No | P__ | ____ | ____ % | ____ seconds to answer | Agent time plus phone software |
| **Self-service and AI agent** (help center, FAQ, chatbot) | [ ] Yes [ ] No | P__ | 24/7 | ____ % | instant | Software and AI fees; humans only for exceptions |
| **Total** | | | | **100 %** | | |

⚠️ Every channel you add needs someone to answer it. If you offer phone but have one person, calls will interrupt everything else. Write below how you will cover each channel when the person is sick or on holiday: ____

**4.2 Language and time zones**
- Do you need support outside normal office hours? [ ] Yes [ ] No
- If yes, who covers nights and weekends? [ ] AI only [ ] On-call person [ ] Outsourced team [ ] Not covered, customers are told: ____

---

## Section 5. The AI helper (AI-agent workflow)

*Why this matters: an AI helper can answer simple questions at very low cost, but only if you decide exactly what it may and may not do. Skip nothing here. If you do not use AI, tick the box below and write `N/A` in the rest.*

- [ ] **We will not use an AI helper in any phase.** (Then go to Section 6.)

**5.1 What will the AI helper do?** (tick all that apply)
- [ ] Answer questions from our help articles
- [ ] Look up a customer's account status (read-only)
- [ ] Take actions for the customer (reset password, change plan)
- [ ] Draft replies that a human checks and sends
- [ ] Sort and label tickets
- [ ] Summarize long conversations for humans
- [ ] Translate
- [ ] Other: ____

**5.2 When AI must hand the customer to a human.** Tick every rule that applies and add your own.
- [ ] Customer asks for a human
- [ ] Customer is angry or upset
- [ ] Question is about a refund over $____
- [ ] Question about legal, safety, health or privacy
- [ ] AI is not confident in its answer
- [ ] AI has failed to solve it after ____ tries
- [ ] Customer pays more than $____ per month (VIP)
- [ ] Other: ____

**5.3 What AI must never do.** Tick all you want, and add your own.
- [ ] Never promise refunds or discounts without a human
- [ ] Never share another customer's information
- [ ] Never give legal, medical or financial advice
- [ ] Never make up an answer. If unsure, say so and hand over.
- [ ] Never pretend to be a human (customers are told they are talking to AI)
- [ ] Other: ____

**5.4 How you will check the AI is correct**

| Question | Your answer |
|---|---|
| Who reads a sample of AI answers? | ____ |
| How many AI answers per week are read? (suggest 20 or 10%, whichever is more) | ____ |
| What counts as a wrong answer? | ____ |
| How many wrong answers per 100 is too many? (suggest no more than 2) | ____ |
| What happens if it is too many? | [ ] Turn AI off for that topic  [ ] Fix the help article  [ ] Other: ____ |
| How are customers asked if the AI helped? | ____ |
| Where are AI mistakes recorded? | ____ |

**5.5 How AI is paid for.** Choose the way your vendor charges. This changes the math in Section 8.

| Pricing model | What it means | Tick |
|---|---|---|
| Per resolution | You pay only when the AI fully solves the question. | [ ] |
| Per conversation | You pay every time the AI chats, even if it fails. | [ ] |
| Per seat (add-on) | You pay per human agent using AI features. | [ ] |
| Usage or tokens | You pay for how much text the AI reads and writes. | [ ] |
| Flat fee | One price per month. | [ ] |
| Not decided yet | Use the example price in Section 8 and mark it 🔴. | [ ] |

**5.6 AI performance guesses by phase**

| Question | P2 Beta | P3 Launch | P4 (1-100) | P5 (101-500) | Sure? |
|---|---|---|---|---|---|
| Out of 100 tickets, how many will AI fully solve without a human? (this is the "AI resolution rate") | ____ % | ____ % | ____ % | ____ % | 🟢🟡🔴 |
| Out of 100 AI chats, how many get handed to a human? | ____ % | ____ % | ____ % | ____ % | 🟢🟡🔴 |

💡 Start low. Many teams reach only a minority of tickets at first and grow it as they add help articles. Use your own beta data when you have it.

---

## Section 6. People costs

*Why this matters: people are usually the biggest cost. Include the founder's or team's time even if no one is "paid" for it. Unpaid time is still a cost.*

**6.1 Who does support in each phase?**

| Person or role | Employee / contractor / founder / vendor | Phase they start | Hours per month on support in P3 | P4 | P5 | Pay per hour, all-in (USD) | Sure? |
|---|---|---|---|---|---|---|---|
| ____ | ____ | P__ | ____ | ____ | ____ | $____ | 🟢🟡🔴 |
| ____ | ____ | P__ | ____ | ____ | ____ | $____ | 🟢🟡🔴 |
| ____ | ____ | P__ | ____ | ____ | ____ | $____ | 🟢🟡🔴 |

**How to work out "pay per hour, all-in" (also called fully loaded rate):**
Yearly pay + yearly benefits and taxes + yearly share of equipment and office, then divide by 2,080 hours (a normal work year).
*Example: ($40,000 + $8,000 + $4,000) ÷ 2,080 = $25 per hour.* If you only know monthly pay, multiply by 12 first.

**6.2 How long does one ticket take a human?**

| Question | Your answer | Sure? |
|---|---|---|
| Minutes for an Easy ticket | ____ min | 🟢🟡🔴 |
| Minutes for a Medium ticket | ____ min | 🟢🟡🔴 |
| Minutes for a Hard ticket | ____ min | 🟢🟡🔴 |
| **Average minutes per human ticket** (use your Section 3.2 shares) | ____ min | 🟢🟡🔴 |

*Average = (Easy share × Easy minutes) + (Medium share × Medium minutes) + (Hard share × Hard minutes).*

**6.3 When do you hire or add help?** Write one rule per phase, in the form "When ____ happens, we ____."
- P3: ____
- P4: ____
- P5: ____

💡 Good triggers: "When a person's support time is above 20 hours per week" or "When replies take longer than our target for 2 weeks".

**6.4 One-time people costs (training, hiring, writing help articles)**

| Item | Hours | Pay per hour | One-time cost | Phase |
|---|---|---|---|---|
| Write the first help articles | ____ | $____ | $____ | P1 |
| Train support people | ____ | $____ | $____ | P1-P2 |
| Hiring (ads, interviews) | ____ | $____ | $____ | P__ |
| Other: ____ | ____ | $____ | $____ | P__ |

**6.5 Ongoing upkeep (monthly)**

| Item | Hours per month | Pay per hour | Monthly cost |
|---|---|---|---|
| Keep help articles up to date | ____ | $____ | $____ |
| Read and fix AI answers | ____ | $____ | $____ |
| Team meetings and coaching on support | ____ | $____ | $____ |

---

## Section 7. Tools and software costs

*Why this matters: small monthly fees add up. List every tool, even free ones. Free tools can have limits that force an upgrade at 100 or 500 customers.*

| Tool | What it does | Price now | Price at 50 customers | At 100 | At 250 | At 500 | Free limit (when you must pay) | Sure? |
|---|---|---|---|---|---|---|---|---|
| Help desk (tickets, shared inbox) | ____ | $____ | $____ | $____ | $____ | $____ | ____ | 🟢🟡🔴 |
| Chat widget | ____ | $____ | $____ | $____ | $____ | $____ | ____ | 🟢🟡🔴 |
| Phone / video | ____ | $____ | $____ | $____ | $____ | $____ | ____ | 🟢🟡🔴 |
| Help center / knowledge base | ____ | $____ | $____ | $____ | $____ | $____ | ____ | 🟢🟡🔴 |
| Reports and customer survey tool | ____ | $____ | $____ | $____ | $____ | $____ | ____ | 🟢🟡🔴 |
| Other: ____ | ____ | $____ | $____ | $____ | $____ | $____ | ____ | 🟢🟡🔴 |
| **Total tools per month** | | $____ | $____ | $____ | $____ | $____ | | |

**One-time tool costs** (setup, connecting to your product, data import): $____ (phase P__)

⚠️ Check: do any tools charge **per human agent seat**? If yes, how many seats do you need at each milestone? ____

---

## Section 8. AI usage costs

*Why this matters: AI costs are small per ticket but grow with volume. They are billed in a different way from people. Use the pricing model you ticked in Section 5.5. If you chose "No AI", write `N/A` and put $0 in Section 11.*

**8.1 AI price**

| Question | Your answer | Sure? |
|---|---|---|
| AI vendor or product name | ____ | 🟢🟡🔴 |
| Price per resolution (or per conversation, or per 1,000 tokens) | $____ | 🟢🟡🔴 |
| Monthly platform or seat fee, if any | $____ | 🟢🟡🔴 |
| Minimum monthly bill, if any | $____ | 🟢🟡🔴 |
| Extra costs: voice, translation, other products | $____ | 🟢🟡🔴 |
| Does the price change at higher volume? | [ ] Yes, how: ____  [ ] No | 🟢🟡🔴 |

⚠️ **Convert the price before comparing.** If a vendor charges per conversation but the AI only solves half of them, your price per *solved* ticket is **double** the sticker price. Formula: *price per resolution = price per conversation ÷ share of conversations the AI solves.*

**8.2 AI cost that is not on the invoice (monthly)**

| Item | Hours or amount | Pay per hour | Monthly cost |
|---|---|---|---|
| Person who checks AI answers (from Section 5.4) | ____ h | $____ | $____ |
| Extra help article writing for AI | ____ h | $____ | $____ |
| Engineering time to connect or fix AI | ____ h | $____ | $____ |

**8.3 One-time AI setup cost:** $____ (writing prompts, connecting tools, testing)

---

## Section 9. Outsourcing and engineering escalations

*Why this matters: some tickets cannot be solved by support. A developer must look at them. That developer's time is a support cost too, and it is the one most often forgotten.*

**9.1 Escalations to engineers**

| Question | Your answer | Sure? |
|---|---|---|
| Out of 100 human-handled tickets, how many need an engineer? | ____ % | 🟢🟡🔴 |
| Hours an engineer spends per escalated ticket | ____ h | 🟢🟡🔴 |
| Engineer's pay per hour, all-in | $____ | 🟢🟡🔴 |

**9.2 Outsourcing** (a company that answers customers for you)

| Question | Your answer |
|---|---|
| Will you outsource any support? | [ ] Yes  [ ] No  (if No, write N/A and go to Section 10) |
| From which phase? | P__ |
| What do they handle? | [ ] Nights and weekends  [ ] Easy tickets  [ ] All tickets  [ ] Other: ____ |
| How are they paid? | [ ] Per ticket $____  [ ] Per hour $____  [ ] Monthly minimum $____ |
| Contract length and exit rules | ____ |
| Who checks the quality of their work? | ____ |

---

## Section 10. Other costs and one-time launch costs

| Item | One-time or monthly | Amount | Phase | Sure? |
|---|---|---|---|---|
| Customer surveys, gifts, apology credits | ____ | $____ | P__ | 🟢🟡🔴 |
| Refunds caused by support problems (average per month) | ____ | $____ | P__ | 🟢🟡🔴 |
| Legal / privacy review of support data | ____ | $____ | P__ | 🟢🟡🔴 |
| Security and access control for support tools | ____ | $____ | P__ | 🟢🟡🔴 |
| Backup plan if the support tool is down | ____ | $____ | P__ | 🟢🟡🔴 |
| Other: ____ | ____ | $____ | P__ | 🟢🟡🔴 |

**Total one-time costs (add up every "one-time" amount in Sections 6, 7, 8, 10):** $____

---

## Section 11. The calculation (let the formulas do the work)

*Why this matters: here you turn your answers into one monthly total at each milestone. Do each row in order. Use a calculator or a spreadsheet. The Worked Example (Section 17) shows every row filled in.*

**Step 0. Copy your numbers.**

| Milestone (customers) | 10 | 50 | 100 | 250 | 500 |
|---|---|---|---|---|---|
| **A.** Tickets per customer per month (Section 3.1) | ____ | ____ | ____ | ____ | ____ |
| **B.** AI resolution rate % (Section 5.6; use 0 if no AI yet) | ____ | ____ | ____ | ____ | ____ |
| **C.** Average human minutes per ticket (Section 6.2) | ____ | ____ | ____ | ____ | ____ |
| **D.** Human pay per hour (Section 6.1) | ____ | ____ | ____ | ____ | ____ |
| **E.** % of human tickets sent to engineers (Section 9.1) | ____ | ____ | ____ | ____ | ____ |
| **F.** Engineer hours per escalation × engineer pay per hour (Section 9.1) | ____ | ____ | ____ | ____ | ____ |

**Step 1. Count tickets.**

| Row | Formula in plain words | 10 | 50 | 100 | 250 | 500 |
|---|---|---|---|---|---|---|
| **1. Total tickets per month** | customers × A | ____ | ____ | ____ | ____ | ____ |
| **2. AI-solved tickets** | row 1 × B ÷ 100 | ____ | ____ | ____ | ____ | ____ |
| **3. Human-handled tickets** | row 1 − row 2 | ____ | ____ | ____ | ____ | ____ |
| **4. Escalated to engineers** | row 3 × E ÷ 100 | ____ | ____ | ____ | ____ | ____ |

**Step 2. Add up the monthly costs (USD).**

| Row | Formula in plain words | 10 | 50 | 100 | 250 | 500 |
|---|---|---|---|---|---|---|
| **5. Human support cost** | row 3 × C ÷ 60 × D | ____ | ____ | ____ | ____ | ____ |
| **6. Engineering cost** | row 4 × F | ____ | ____ | ____ | ____ | ____ |
| **7. Tool cost** | Section 7 total at that milestone | ____ | ____ | ____ | ____ | ____ |
| **8. AI usage cost** | row 2 × AI price per resolution + monthly AI fees (Section 8.1) | ____ | ____ | ____ | ____ | ____ |
| **9. AI checking cost** | Section 8.2 total | ____ | ____ | ____ | ____ | ____ |
| **10. Upkeep (help articles, coaching)** | Section 6.5 total | ____ | ____ | ____ | ____ | ____ |
| **11. Outsourcing cost** | Section 9.2 amount (0 if none) | ____ | ____ | ____ | ____ | ____ |
| **12. Other monthly costs** | Section 10 monthly items | ____ | ____ | ____ | ____ | ____ |
| **13. TOTAL SUPPORT COST PER MONTH** | add rows 5 to 12 | ____ | ____ | ____ | ____ | ____ |

**Step 3. Turn it into unit costs.**

| Row | Formula in plain words | 10 | 50 | 100 | 250 | 500 |
|---|---|---|---|---|---|---|
| **14. Cost per customer per month** | row 13 ÷ customers | ____ | ____ | ____ | ____ | ____ |
| **15. Cost per ticket** | row 13 ÷ row 1 | ____ | ____ | ____ | ____ | ____ |
| **16. Cost per human ticket** | (row 5 + row 6 + row 11) ÷ row 3 | ____ | ____ | ____ | ____ | ____ |

**Step 4. Total cost from now until 500 customers.**

| Row | Formula | Your answer |
|---|---|---|
| **17. Total one-time costs** | from Section 10 | $____ |
| **18. Estimated monthly cost for each phase** | use the row 13 value of the nearest milestone (P3 → 50, P4 → 100, P5 → 250 to 500) | P3 $____  P4 $____  P5 $____ |
| **19. Months in each phase** | from Section 2.1 dates | P3 ____  P4 ____  P5 ____ |
| **20. Total ongoing cost to 500 customers** | sum of (row 18 × row 19) for each phase | $____ |
| **21. Grand total (row 17 + row 20)** | | $____ |

⚠️ **Check your math:** row 15 should not be below $1 or above $60 for most products. If it is, re-check Section 3.1 and 6.2 before moving on.

---

## Section 12. Three scenarios (what if I am wrong?)

*Why this matters: one guess is dangerous. Show a better case, the plan, and a worse case at 500 customers.*

| Input | Better case | **Plan (from Section 11)** | Worse case |
|---|---|---|---|
| Tickets per customer per month | ____ | **____** | ____ |
| AI resolution rate % | ____ | **____** | ____ |
| Average human minutes per ticket | ____ | **____** | ____ |
| Human pay per hour | ____ | **____** | ____ |
| Engineer escalation % | ____ | **____** | ____ |
| **Total support cost per month at 500 customers** | $____ | **$____** | $____ |
| **Cost per customer per month** | $____ | **$____** | $____ |
| **Cost per ticket** | $____ | **$____** | $____ |

💡 How to build the better and worse cases: change tickets per customer by about ±25%, AI resolution rate by about ±15 points, and handle time by about ±20%, then redo Section 11 for 500 customers only.

**What would make the worse case happen?** ____
**What will you do if it starts to happen?** ____

---

## Section 13. Money in versus support cost

*Why this matters: support must make sense next to what customers pay you. This is where finance people look first.*

| Question | 10 | 50 | 100 | 250 | 500 |
|---|---|---|---|---|---|
| **A.** Monthly revenue = customers × price (Section 1.3) | $____ | $____ | $____ | $____ | $____ |
| **B.** Support cost per month (row 13) | $____ | $____ | $____ | $____ | $____ |
| **C.** Support cost as % of revenue = B ÷ A × 100 | ____ % | ____ % | ____ % | ____ % | ____ % |
| **D.** Left over after support = A − B | $____ | $____ | $____ | $____ | $____ |

| Question | Your answer |
|---|---|
| What % of revenue are you willing to spend on support? (your limit) | ____ % |
| At which milestone does support cost fall below that limit? | ____ customers |
| What do you do if it never falls below the limit? | [ ] Raise price  [ ] Raise AI share  [ ] Cut channels  [ ] Other: ____ |
| Does any plan promise a certain response time or support level to customers? | [ ] Yes, ____  [ ] No |
| Will support be free for all customers, or is there a paid support tier? | ____ |

💡 Some benchmarks say software companies often spend a high single-digit percentage of revenue on support and customer success. Treat that as a loose reference, not a target (see Section 20).

---

## Section 14. Measures and targets (how you know it is working)

*Why this matters: you cannot manage cost without also watching quality. Cheap support that makes customers leave is not cheap.*

**14.1 Pick targets for each phase.** Use the suggested numbers if you have no baseline, then replace them with your own after P3.

| Measure | What it means in plain words | Suggested start | P3 target | P4 target | P5 target | Who checks it | How often |
|---|---|---|---|---|---|---|---|
| **First response time** | How long a customer waits for the first real reply | Email: under 1 business day; chat: under a few minutes | ____ | ____ | ____ | ____ | Daily |
| **First contact resolution** | % of problems solved in one conversation and not reopened in 72 hours | Aim for 70% or higher | ____ % | ____ % | ____ % | ____ | Weekly |
| **CSAT** | % of customers who say they were happy after a conversation | About 75 to 85% is common | ____ % | ____ % | ____ % | ____ | Weekly |
| **AI resolution rate** | % of tickets AI solves without a human | Use your Section 5.6 numbers | ____ % | ____ % | ____ % | ____ | Weekly |
| **Cost per ticket** | Total support cost ÷ tickets | Use your row 15 | $____ | $____ | $____ | ____ | Monthly |
| **Cost per resolved ticket** | Total support cost ÷ tickets that were actually solved | Row 13 ÷ solved tickets | $____ | $____ | $____ | ____ | Monthly |
| **Repeat contact rate** | % of customers who come back about the same problem | Lower is better | ____ % | ____ % | ____ % | ____ | Monthly |
| **Backlog** | Tickets waiting more than 2 days | Aim for 0 | ____ | ____ | ____ | ____ | Daily |
| **Support cost as % of revenue** | Row C in Section 13 | Use your limit | ____ % | ____ % | ____ % | ____ | Monthly |

**14.2 "If this happens, do that" rules**

| If this happens | Then we | Who decides |
|---|---|---|
| CSAT falls below ____ % for 2 weeks | ____ | ____ |
| Cost per ticket is more than 20% above plan for 2 months | ____ | ____ |
| AI wrong-answer rate is above the Section 5.4 limit | ____ | ____ |
| First response time target is missed for 2 weeks | ____ | ____ |
| Ticket volume doubles in one week | ____ | ____ |

---

## Section 15. Assumptions log

*Why this matters: every 🟡 and 🔴 above is a guess. Write each one here so nobody mistakes a guess for a fact. Review it at the end of each phase.*

| # | Assumption (one sentence) | Where used (section) | Sure? | Who can check it | How to check it | Check by (date) | Result |
|---|---|---|---|---|---|---|---|
| A1 | ____ | ____ | 🟡🔴 | ____ | ____ | ____ | ____ |
| A2 | ____ | ____ | 🟡🔴 | ____ | ____ | ____ | ____ |
| A3 | ____ | ____ | 🟡🔴 | ____ | ____ | ____ | ____ |
| A4 | ____ | ____ | 🟡🔴 | ____ | ____ | ____ | ____ |
| A5 | ____ | ____ | 🟡🔴 | ____ | ____ | ____ | ____ |

*(Add rows as needed. Every 🔴 must have a "Check by" date before launch.)*

## Section 16. Risks log

| # | What could go wrong | How likely (Low / Medium / High) | How bad (Low / Medium / High) | What we do to prevent it | What we do if it happens | Owner |
|---|---|---|---|---|---|---|
| R1 | Ticket volume is much higher than planned | ____ | ____ | ____ | ____ | ____ |
| R2 | AI gives a wrong or harmful answer | ____ | ____ | ____ | ____ | ____ |
| R3 | The one support person leaves or is sick | ____ | ____ | ____ | ____ | ____ |
| R4 | AI or tool price rises, or a free plan ends | ____ | ____ | ____ | ____ | ____ |
| R5 | A bug in a new release floods support | ____ | ____ | ____ | ____ | ____ |
| R6 | Customer data leaks through a support tool | ____ | ____ | ____ | ____ | ____ |
| R7 | Help articles are out of date after a release | ____ | ____ | ____ | ____ | ____ |
| R8 | Other: ____ | ____ | ____ | ____ | ____ | ____ |

---

## Section 17. Worked example (a fully filled-in fictional project)

> **This is made-up data to show you how the form looks when finished. Do not copy these numbers. Delete this section in your project copy only if your team prefers, but never edit the template original.**

**Project:** Acme Notes, a note-taking app for small teams. Price: **$30 per customer per month**. Launch: January. 5 phases, ending at 500 customers. Support: founder in P1-P3, one part-time contractor from P4. AI helper starts in P3 and is paid **$1.00 per AI-solved ticket** (🟡).

**Inputs used (all 🟡 unless stated):**
- Human pay: $25/hour all-in (🟢 from contractor invoice).
- Average human handle time: **20 minutes** per ticket.
- Engineering escalations: **10%** of human tickets, **1 hour each at $60/hour**, so **$60 per escalation**.
- Tools: help desk $0 / $55 / $55 / $110 / $110 and help-center-plus-chat $0 / $30 / $30 / $30 / $30 at 10 / 50 / 100 / 250 / 500 customers.
- Upkeep (help articles): **2 hours/month at $25 = $50**, from 50 customers upward.
- AI answer checking: **10% of AI-solved tickets checked, 5 minutes each, at $25/hour.**
- One-time setup: help articles 40 h × $25 = $1,000; help-desk setup 8 h × $25 = $200; AI setup and testing 30 h × $60 = $1,800; training 10 h × $25 = $250. **Total one-time = $3,250.**

**Section 11 calculation, filled in:**

| Row | 10 | 50 | 100 | 250 | 500 |
|---|---|---|---|---|---|
| A. Tickets per customer per month | 1.0 | 0.8 | 0.6 | 0.4 | 0.4 |
| B. AI resolution rate | 0% | 30% | 40% | 50% | 55% |
| 1. Total tickets | 10 | 40 | 60 | 100 | 200 |
| 2. AI-solved tickets | 0 | 12 | 24 | 50 | 110 |
| 3. Human tickets | 10 | 28 | 36 | 50 | 90 |
| 4. Escalated to engineers | 1.0 | 2.8 | 3.6 | 5.0 | 9.0 |
| 5. Human support cost | $83.33 | $233.33 | $300.00 | $416.67 | $750.00 |
| 6. Engineering cost | $60.00 | $168.00 | $216.00 | $300.00 | $540.00 |
| 7. Tools | $0.00 | $85.00 | $85.00 | $140.00 | $140.00 |
| 8. AI usage | $0.00 | $12.00 | $24.00 | $50.00 | $110.00 |
| 9. AI checking | $0.00 | $2.50 | $5.00 | $10.42 | $22.92 |
| 10. Upkeep | $0.00 | $50.00 | $50.00 | $50.00 | $50.00 |
| 11. Outsourcing | $0.00 | $0.00 | $0.00 | $0.00 | $0.00 |
| 12. Other monthly | $0.00 | $0.00 | $0.00 | $0.00 | $0.00 |
| **13. TOTAL per month** | **$143.33** | **$550.83** | **$680.00** | **$967.09** | **$1,612.92** |
| 14. Cost per customer per month | $14.33 | $11.02 | $6.80 | $3.87 | $3.23 |
| 15. Cost per ticket | $14.33 | $13.77 | $11.33 | $9.67 | $8.06 |
| 16. Cost per human ticket | $14.33 | $14.33 | $14.33 | $14.33 | $14.33 |

*(Example of one row: row 5 at 100 customers = 36 human tickets × 20 minutes ÷ 60 × $25 = 12 hours × $25 = $300.00.)*

**Section 13 for the example:**

| | 10 | 50 | 100 | 250 | 500 |
|---|---|---|---|---|---|
| Revenue | $300 | $1,500 | $3,000 | $7,500 | $15,000 |
| Support cost | $143.33 | $550.83 | $680.00 | $967.09 | $1,612.92 |
| Support as % of revenue | 47.8% | 36.7% | 22.7% | 12.9% | 10.8% |
| Left over | $156.67 | $949.17 | $2,320.00 | $6,532.91 | $13,387.08 |

**Section 12 for the example (500 customers):**

| | Better case | **Plan** | Worse case |
|---|---|---|---|
| Tickets per customer | 0.3 | **0.4** | 0.6 |
| AI resolution rate | 60% | **55%** | 35% |
| Total cost per month | $1,158.75 | **$1,612.92** | $3,166.88 |
| Cost per customer per month | $2.32 | **$3.23** | $6.33 |
| Cost per ticket | $7.73 | **$8.06** | $10.56 |

**What the example teaches:**
1. Cost per customer drops from about $14 to about $3 as help articles and AI improve. That is the point of the model.
2. The worse case is almost **double** the plan, mostly because tickets are higher and the AI solves fewer. So Acme Notes must watch "tickets per customer" and "AI resolution rate" every week.
3. Engineering time (row 6) is a large slice early on. Many teams forget it.

---

## Section 18. Quality checklist and sign-off

**18.1 "Is this document ready to use?" checklist.** Every box must be ticked before approval.

*Complete*
- [ ] Every question in Sections 0 to 16 has an answer (or `N/A - because ...`)
- [ ] No cell says TBD, later or approx.
- [ ] Every number has a 🟢, 🟡 or 🔴 next to it

*Correct*
- [ ] Ticket shares in Section 3.2 add up to 100%
- [ ] Channel shares in Section 4.1 add up to 100%
- [ ] Every row in Section 11 was calculated with the formula, not typed from memory
- [ ] The example rows were checked once with a calculator
- [ ] Cost per ticket (row 15) is between about $1 and $60, or a reason is written
- [ ] People cost includes unpaid founder or team time

*Honest*
- [ ] Every 🟡 and 🔴 is listed in the Assumptions Log (Section 15)
- [ ] No 🔴 remains without an owner and a date
- [ ] Better and worse cases in Section 12 were filled in
- [ ] AI limits and hand-off rules in Section 5 were approved by a human

*Useful*
- [ ] Phase dates in Section 2 match the real project plan
- [ ] "If this happens, do that" rules in Section 14.2 have a named decider
- [ ] The next review date is written in Section 0
- [ ] A person who did not write the document read it and could follow it without asking questions

**18.2 Reviewers and approval**

| Role | Name | Date | Decision (Approve / Changes needed) | Comments |
|---|---|---|---|---|
| Document owner | ____ | ____ | ____ | ____ |
| Support lead | ____ | ____ | ____ | ____ |
| Finance reviewer | ____ | ____ | ____ | ____ |
| Product or engineering lead | ____ | ____ | ____ | ____ |
| Final approver | ____ | ____ | ____ | ____ |

**18.3 Change log**

| Version | Date | Who | What changed and why |
|---|---|---|---|
| 0.1 | ____ | ____ | First draft |
| ____ | ____ | ____ | ____ |

---

## Section 19. Glossary (plain-English words)

| Word | What it means |
|---|---|
| **AI agent / AI helper** | Software that answers customers by itself, using your help articles and rules. |
| **AI resolution rate** | Out of 100 tickets, how many the AI fully solved without a human. |
| **Assumption** | A guess you are treating as true until you check it. |
| **Average handle time (AHT)** | The average total time a human spends on one ticket, including notes after the chat. |
| **Backlog** | Tickets waiting for an answer. |
| **Channel** | A way customers reach you: email, chat, phone, help center. |
| **Containment rate** | Of the chats the AI started, how many ended without needing a human. |
| **Cost per customer** | Total support cost in a month ÷ number of customers. |
| **Cost per resolution** | Total support cost ÷ tickets that were truly solved. Honest, because unsolved tickets do not count. |
| **Cost per ticket** | Total support cost ÷ all tickets. |
| **CSAT** | Customer satisfaction. A short question after support: "Were you happy?" Shown as a %. |
| **Deflection** | A customer solved the problem alone (help article, AI) and never reached a human. |
| **Escalation** | A ticket passed to someone with more skill, such as an engineer. |
| **First contact resolution (FCR)** | % of problems solved in the first conversation and not reopened soon after. |
| **First response time (FRT)** | How long a customer waits before getting the first real reply. |
| **Fully loaded cost** | Pay plus taxes, benefits, equipment and overhead. The true price of an hour of work. |
| **Gate** | A checklist you must pass before moving to the next phase. |
| **Hand-off** | The moment AI passes the customer to a human. |
| **Help center / knowledge base** | A website of help articles customers can read themselves. |
| **Milestone** | A customer count where you check the math: 10, 50, 100, 250, 500. |
| **One-time cost** | Paid once (setup, training). Not repeated monthly. |
| **Phase** | A stretch of the project (P1 to P5). |
| **Re-contact / repeat contact** | A customer asks again about the same problem. |
| **SLA** | A written promise about reply speed or support level. |
| **Ticket** | One customer request for help. |
| **Token** | A small piece of text an AI reads or writes. Some AI tools bill by tokens. |
| **TCO** | Total cost of ownership: everything you really pay, not just the sticker price. |

---

## Section 20. Reference ranges and sources (use only as a sanity check)

*These are public figures from vendor and industry articles seen in October 2026. Vendors have reasons to publish flattering numbers. Always prefer your own data, and re-check this table at each review.*

| Topic | Rough reference | Source |
|---|---|---|
| Blended cost per human-handled ticket | Often cited around $8 to $20, with complex B2B or healthcare tickets much higher | [Stealth Agents, 2026](https://stealthagents.com/blog/customer-support-cost-per-ticket-benchmarks-2026) |
| Email / ticket cost per case | About $6 to $11 | [Office Gurus, 2026](https://www.theofficegurus.com/customer-support-cost-benchmarks/) |
| Outsourced Tier 1 vs in-house | Outsourced often cited at $6 to $13 per contact vs about $22 fully loaded in-house | [Stealth Agents, 2026](https://stealthagents.com/research/customer-support-outsourcing-roi-data-2026) |
| AI price per resolution (list price) | Median about $1 across eight vendors, from about $0.45 to $1.50 | [Macha pricing index, Sept 2026](https://www.getmacha.com/blog/how-much-does-an-ai-support-agent-cost-per-resolution) |
| AI pricing models | Per resolution, per conversation, per seat, usage-based, or flat | [Intercom, 2026](https://www.intercom.com/learning-center/ai-customer-service-agent-pricing-comparison) |
| Per-conversation vs per-resolution | A per-conversation fee costs more per solved ticket if the AI solves only part of the chats | [Macha pricing index](https://www.getmacha.com/blog/ai-customer-support-pricing-index-2026) |
| Cost per contact vs cost per resolution | Cost per resolution is the honest number once AI carries volume | [Voiceflow, 2026](https://www.voiceflow.com/blog/customer-service-metrics) |
| Metric targets (FRT, FCR, CSAT) | FCR about 70%+ is strong; CSAT about 75-85% typical; email first reply within about an hour for strong teams | [Groove, 2026](https://www.groovehq.com/blog/customer-service-metrics), [Telnyx](https://telnyx.com/resources/customer-service-metrics) |
| Deflection and containment | Not the same: containment counts only bot chats; deflection counts the whole queue | [Outlearn](https://outlearn.com/blog/customer-service-metrics) |
| Hourly cost formula | Pay ÷ 2,080 hours; cost per ticket = hours × hourly cost ÷ tickets | [HumCommerce, 2026](https://humcommerce.com/?p=18267) |

**Template owner's note:** replace or add rows when you learn better figures for your industry. Do not use these ranges to fill blanks in Sections 3 to 10. Use your own data or an honest 🟡 guess.
