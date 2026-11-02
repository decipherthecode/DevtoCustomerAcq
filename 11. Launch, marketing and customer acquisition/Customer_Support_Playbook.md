# Customer Support Playbook

> **Template version:** 1.1 | **Folder:** Launch, Marketing & Customer Acquisition | **Covers:** Build → Launch → first 500 customers
> **Fits:** Any product (web app, mobile app, AI tool, hardware, service) | **Support model:** Solo founder + AI agents (hybrid)

---

# HOW TO FILL THIS DOCUMENT

Read this section first. It takes 3 minutes.

## What this document is
A Customer Support Playbook is your **rule book for helping customers**. It answers: *Who helps? How fast? Through which door? What do we say? What do we do when something goes wrong?*

After you fill it in, anybody (a teammate, a freelancer, or an AI agent) can read it and know exactly what to do **without guessing**.

## The 9 golden rules
1. **Fill it in order.** Start at Part A and go down. Each phase builds on the one before.
2. **Answer every question.** Write in the `✏️ Your answer:` space. Short is fine. Nothing may be left empty.
3. **Can't answer yet?** Write `TBD – [who] – [date]`. Example: `TBD – Sam – 2026-11-05`. Never leave a blank.
4. **Pre-filled answers are marked `(DEFAULT)`.** They are safe starting points. Keep them or change them. If you keep one, write `Keep`.
5. **Checkboxes:** change `[ ]` to `[x]` when done.
6. **Use real names, numbers, and dates.** Not "soon", "someone", "fast". Write "within 24 hours", "Maria", "Nov 5".
7. **Don't delete questions.** If one doesn't apply, write `N/A – because [reason]`.
8. **Check your answer against Appendix H.** It shows what a *good* answer and a *bad* answer look like for every section. If your answer looks like the bad one, rewrite it.
9. **See a finished example in Appendix K** (a fictional product) if you get stuck. Then track your progress with the **Completion Score** in Appendix J.

## Symbols you will see
| Symbol | Meaning |
|---|---|
| ✏️ | Write your answer here |
| 💡 | Example to copy or learn from |
| ⚠️ | Danger zone: be extra careful |
| 🤖 | Instruction that an AI agent will read and follow |
| 🚦 | Gate: you must pass this before moving to the next phase |
| `(DEFAULT)` | Pre-filled suggestion you can keep or edit |

## Words you might not know
| Word | Plain meaning |
|---|---|
| **Ticket** | One customer problem or question, saved as a record |
| **SLA** | A promise about how fast you will reply |
| **Severity** | How serious a problem is (P1 = worst, P4 = smallest) |
| **Escalation** | Passing a problem to someone more able to fix it |
| **Handoff** | AI passing a conversation to a human |
| **Macro / Canned reply** | A saved answer you reuse |
| **Knowledge base (KB)** | Your help articles |
| **CSAT** | Customer satisfaction score (a happy/unhappy rating) |
| **FRT** | First Response Time: how long until the customer hears from you |
| **TTR** | Time To Resolution: how long until the problem is fixed |
| **Deflection** | Customer solved it themselves from the help articles |
| **Churn** | A customer leaving |
| **Post-mortem** | A "what went wrong and how do we stop it" write-up |
| **PII** | Personal information (name, email, address, payment info) |

## How the phases work
```
Phase 0 BUILD → Phase 1 PRE-LAUNCH → Phase 2 BETA → Phase 3 LAUNCH → Phase 4 CUSTOMERS 1–100 → Phase 5 CUSTOMERS 101–500
```
At the end of each phase is a 🚦 **Gate**. Tick every box before moving on. Phases 0–3 are filled **before** customers arrive. Phases 4–5 are filled **as you grow**, and you revisit the Gate each time you hit a milestone.

## How an AI agent should use this file
🤖 If you are an AI agent reading this: treat every `✏️ Your answer` as the **single source of truth**. If an answer is `TBD` or empty, **ask the human** instead of inventing one. Never contradict this playbook. When this playbook and a customer's request conflict, follow the playbook and escalate.

---

# PART A – DOCUMENT CONTROL

| Field | ✏️ Your answer |
|---|---|
| Product name | |
| One-sentence description of the product | |
| Playbook owner (one person, full name) | |
| Backup owner (if owner is unavailable) | |
| Date created | |
| Last reviewed | |
| Version | 1.0 |
| Where this file lives (link or path) | |
| Review rhythm (DEFAULT: monthly until 500 customers, then quarterly) | |

**Change log** (add a row every time you edit an important rule)

| Date | What changed | Why | Changed by |
|---|---|---|---|
| | | | |

---

# PART B – PROJECT SNAPSHOT

**B1. What type of product is this?** (tick one)
- [ ] Web app / SaaS
- [ ] Mobile app
- [ ] AI tool / agent / copilot
- [ ] API / developer tool
- [ ] Physical product / hardware (also fill **Appendix F: Physical-product add-on**)
- [ ] Service / marketplace
- [ ] Other: ______

**B2. Who is your customer?**
💡 *Example: "Freelance designers in the US who invoice 5+ clients a month."*
✏️ Your answer:

**B3. What are the 3 most likely reasons a customer will contact you?**
💡 *Example: 1) Can't log in 2) Billing question 3) "How do I do X?"*
✏️ 1) …  2) …  3) …

**B4. Pricing model** (tick): [ ] Free [ ] Free trial [ ] Freemium [ ] Paid subscription [ ] One-time purchase [ ] Usage-based

**B5. Who provides support?**
| Role | Name | Hours/week for support | Time zone |
|---|---|---|---|
| Support lead | | | |
| Backup | | | |
| Engineer on call (for bugs) | | | |
| AI agent(s) | (name them, e.g., "SupportBot") | 24/7 | n/a |

**B6. Goal:** Reach **500 customers** by (date): ______
**B7. Customers who will be "who counts"?** (DEFAULT: a customer = a person or company that has signed up AND used the product at least once.) ✏️ Keep / Change:

---

# PHASE 0 – BUILD (Product is being made)

**Goal:** Decide the support foundation while building. Cheap to decide now, painful to fix later.

## 0.1 Support promise (your "why")
**0.1.1 Finish this sentence: "When a customer contacts us, they should feel ______."**
✏️ Your answer:

**0.1.2 Write 3 support values.** 💡 *Example: Be honest. Be fast. Never make the customer repeat themselves.*
✏️ 1) …  2) …  3) …

**0.1.3 Voice and tone** (tick all that fit): [ ] Friendly [ ] Professional [ ] Playful [ ] Calm [ ] Short and direct
Words we **always** use: ______ | Words we **never** use: ______
💡 *Never: "Unfortunately that's not possible." Instead: "Here's what I can do…"*

## 0.2 Support doors (channels)
For each channel, decide: **Open at launch? Who answers? Where does it live?**

| Channel | Open at launch? (Y/N) | Who answers (AI / human / both) | Tool or link | Reply target |
|---|---|---|---|---|
| Email (support@…) | | | | 24h (DEFAULT) |
| In-app / live chat | | | | AI instant, human 4h in hours (DEFAULT) |
| Community (Discord / Slack / forum) | | | | 24h (DEFAULT) |
| Social media DMs (X, Instagram, LinkedIn) | | | | 24h (DEFAULT) |
| Phone | (DEFAULT: No. Say "email us" instead) | | | |
| Help center / FAQ (self-service) | Yes (DEFAULT) | AI + you | | n/a |

**0.2.1 Support hours** ✏️ 💡 *Example: Mon–Fri, 9am–5pm Eastern. AI answers outside hours.*
**0.2.2 What does a customer see outside support hours?** ✏️ (auto-reply text)
**0.2.3 Holidays/days off plan** ✏️

## 0.3 Tools (your support tool stack)
| Need | Tool chosen | Cost | Owner | Set up? |
|---|---|---|---|---|
| Ticket inbox (helpdesk) | | | | [ ] |
| Live chat widget | | | | [ ] |
| Knowledge base / help center | | | | [ ] |
| AI support agent | | | | [ ] |
| Status page (shows if product is down) | | | | [ ] |
| Customer survey (CSAT) | | | | [ ] |
| Customer record / CRM (who is this person?) | | | | [ ] |
| Bug tracker (where bugs go) | | | | [ ] |
| Password manager / secure sharing | | | | [ ] |

💡 *Start small. A shared inbox plus a spreadsheet beats a complicated tool you won't use.*
⚠️ Never put customer passwords or card numbers in tickets, chats, or AI prompts.

## 0.4 Severity levels (how serious is the problem?)
Pre-filled with `(DEFAULT)`. Edit to fit your product.

| Level | Meaning | Example | First reply (DEFAULT) | Update every (DEFAULT) | Fix target (DEFAULT) |
|---|---|---|---|---|---|
| **P1 Critical** | Product down, data loss, security issue, or money wrongly taken | Nobody can log in | 1 hour | 2 hours | Same day |
| **P2 High** | Main feature broken for some customers, no workaround | Payment fails for some | 4 hours | 1 business day | 2 business days |
| **P3 Normal** | Problem with a workaround, or a "how do I" question | Export button is slow | 24 hours | 2 business days | 5 business days |
| **P4 Low** | Idea, small cosmetic issue, general feedback | "Please add dark mode" | 48 hours | n/a | Logged for roadmap |

✏️ **Any changes to the table above?** (or write "Keep")
✏️ **Who decides severity when unsure?** (DEFAULT: the support lead; when in doubt, pick the higher level)

## 0.5 Who handles what (hybrid AI + human)
🤖 **AI handles (DEFAULT):** FAQs, "how do I…", order/account status lookups, password-reset guidance, collecting details (screenshots, steps, device), tagging and routing tickets, drafting replies for human review.

👤 **Human handles (DEFAULT):** refunds, billing disputes, angry or upset customers, legal or privacy requests, security reports, accessibility needs, bug confirmation, anything the AI is unsure about, VIP/key customers.

✏️ **Changes to these lists?** (or "Keep")

**AI auto-handoff triggers.** The AI must hand off to a human when ANY box is ticked (DEFAULT all ticked):
- [x] Customer asks for a human (even once)
- [x] AI confidence is low or it isn't sure the answer is correct
- [x] Customer is angry, upset, or sarcastic
- [x] Same problem not solved after 2 AI attempts
- [x] Topic is billing, refund, legal, privacy, security, or safety
- [x] Customer mentions an accessibility need
- [x] Customer mentions cancelling, a chargeback, or a lawsuit
- [x] Customer is a key account (list: ______)
- [ ] Other: ______

**AI rules (DEFAULT):**
- The AI tells the customer **it is an AI** at the start.
- The AI never promises refunds, dates, or features that aren't written in this playbook.
- The AI never guesses. If it doesn't know, it says so and hands off.
- When handing off, the AI passes the **full chat, what the customer wants, and what was already tried**, so the customer never repeats themselves.
- Tell the customer what happens next: "A team member will reply by [time]."

✏️ **Human handoff promise** (when does a human reply after handoff?) (DEFAULT: within the P-level reply target above)

## 0.6 Policies (decide before launch)
⚠️ Not legal advice. Have a professional review refund, privacy, and terms policies.

**0.6.1 Refund policy** ✏️ 💡 *Example: "Full refund within 14 days, no questions asked."*
**0.6.2 Cancellation policy** ✏️
**0.6.3 Free trial / free plan limits** ✏️
**0.6.4 Chargeback / payment dispute: who handles and how?** ✏️
**0.6.5 Fair use / what we won't support (abuse, harassment, illegal use)** ✏️
**0.6.6 What do we do with abusive customers?** (DEFAULT: one polite warning, then end the conversation and log it.) ✏️
**0.6.7 Links:** Terms of Service ______ | Privacy Policy ______ | Refund Policy ______

## 0.7 Privacy and data rules (GDPR / CCPA)
| Question | ✏️ Your answer |
|---|---|
| Which regions will your customers live in? | |
| Where is customer data stored (tools + country)? | |
| Who can see customer data? | |
| How can a customer ask to **see**, **fix**, or **delete** their data? (give an email or form) | |
| Who handles these requests? | |
| Deadline to answer (DEFAULT: 30 days for GDPR requests, 45 days for CCPA requests; confirm with a professional) | |
| How do you confirm the person is who they say they are before sharing data? | |
| What customer info may the AI see? What is it NOT allowed to see? | |

⚠️ Never send customer personal info into an AI tool that is not approved for it.

## 0.8 Accessibility
**0.8.1 Can customers who use screen readers, need larger text, or can't use chat get support another way?** ✏️ (DEFAULT: yes, via email, and a human replies in plain text.)
**0.8.2 Is the help center readable (headings, alt text on images, good colour contrast)?** [ ] Yes [ ] No [ ] Not checked yet

## 0.9 AI agent governance 🤖 (keeping the AI safe and correct)
| Question | ✏️ Your answer |
|---|---|
| **0.9.1** Who owns the AI agent? (one named person) | |
| **0.9.2** Which AI tool/model is used, and what is the version/date of the current instructions? | |
| **0.9.3** What is the AI allowed to read? (help articles, order data, etc.) Where is that stored? | |
| **0.9.4** Who updates the AI's knowledge, and how soon after a product change? (DEFAULT: within 2 business days) | |
| **0.9.5** What customer data is sent to the AI vendor? Is it set so the vendor does not train on it? | |
| **0.9.6** How do we keep a record of AI conversations, who can read them, and for how long? (confirm length with a professional) | |
| **0.9.7** **Kill switch:** how do we turn the AI off in under 5 minutes, who can do it, and what do customers see then? | |
| **0.9.8** Does the AI always say it's an AI? (DEFAULT: Yes) | |

**0.9.9 Golden questions test.** Write 20 questions where you know the correct answer. Re-run them **every time** the AI's instructions or knowledge change. (Start with 10 now; reach 20 by Phase 2.)
| # | Question a customer would ask | Correct answer (short) | Must hand off? (Y/N) | Last tested | Pass? |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

**0.9.10 If the AI gives a wrong or harmful answer (DEFAULT steps):**
1. Correct it with the customer: apologise, give the right answer (human does this).
2. Log it: date, what was said, why wrong.
3. Fix the cause (article missing? instruction unclear?).
4. Add that question to the golden test list and re-test.
5. If the customer lost money, data, or safety was at risk → treat as **P1/P2** and use the incident plan (1.6).

**0.9.11 AI monitoring routine (DEFAULT):** spot-check 5 conversations/week in Phases 3–4 and 20/month in Phase 5. Always read: conversations with low CSAT, handoffs, and any with words like *refund, lawyer, cancel, hurt, scam*. ✏️ Changes: ______

**0.9.12 AI instruction version log**
| Date | Version | What changed | Tested with golden questions? | Changed by |
|---|---|---|---|---|
| | | | [ ] | |

## 0.10 Languages and time zones
| Question | ✏️ Your answer |
|---|---|
| **0.10.1** Which languages do you support at launch? | |
| **0.10.2** If a customer writes in another language, what happens? (DEFAULT: reply in English, offer translation; reply in their language only for languages a human has checked) | |
| **0.10.3** Who checks translated help articles and AI answers in each language? | |
| **0.10.4** Which time zones are most of your customers in? | |
| **0.10.5** Which time zone are "business hours" and SLA timers measured in? | |
| **0.10.6** Do SLA timers run 24/7 or only in business hours? (DEFAULT: P1 = 24/7 clock; P2–P4 = business hours) | |
| **0.10.7** What is the plan for hours when no human is awake (AI + auto-reply + P1 phone/pager route)? | |
| **0.10.8** Currency, date format, and local rules to remember (e.g., VAT, local refund law) | |

## 0.11 Budget and tool costs
| Item | Monthly cost now | Est. at 100 customers | Est. at 500 customers | Who approves |
|---|---|---|---|---|
| Helpdesk / inbox | | | | |
| Live chat | | | | |
| AI agent (usage costs) | | | | |
| Knowledge base | | | | |
| Status page | | | | |
| Survey tool | | | | |
| Freelancer / part-time help | | | | |
| Other | | | | |
| **Total** | | | | |

✏️ **Support time budget** (hours/week × your hourly value): ______
✏️ **Maximum we will spend on support per customer per month:** ______
✏️ **Formula we use for cost per ticket:** (tool costs + support time cost) ÷ number of tickets = ______

## 🚦 PHASE 0 GATE – Foundation ready?
- [ ] 0.1 Promise and tone written
- [ ] 0.2 Channels, hours, and reply targets chosen
- [ ] 0.3 Tools picked and at least ticket inbox + AI agent set up
- [ ] 0.4 Severity table agreed
- [ ] 0.5 AI vs. human rules and handoff triggers agreed
- [ ] 0.6 Refund, cancellation, and abuse policies written
- [ ] 0.7 Privacy request process written
- [ ] 0.8 Accessibility route exists
- [ ] 0.9 AI owner named, kill switch written, first 10 golden questions tested
- [ ] 0.10 Languages and time-zone rules decided
- [ ] 0.11 Budget and cost-per-ticket formula written
**Gate approved by:** ______ **Date:** ______

---

# PHASE 1 – PRE-LAUNCH (Product works; get support ready)

**Goal:** Be ready for the first real person before they arrive.

## 1.1 Knowledge base (help articles)
**1.1.1 List the first 10–20 articles to write.** (Cover your top 3 reasons from B3, plus sign-up, login, billing, cancel, and delete account.)

| # | Article title | Written? | Reviewed by | Link |
|---|---|---|---|---|
| 1 | Getting started in 5 minutes | [ ] | | |
| 2 | How to reset my password | [ ] | | |
| 3 | How billing works | [ ] | | |
| 4 | How to cancel or get a refund | [ ] | | |
| 5 | How to delete my account and data | [ ] | | |
| 6 | | [ ] | | |
| 7 | | [ ] | | |

**1.1.2 Article format rule** (DEFAULT): Title is a question or task → 1 sentence answer → numbered steps → screenshot → "Still stuck? Contact us."
**1.1.3 Who updates articles when the product changes, and how soon?** ✏️ (DEFAULT: within 2 business days of any release.)

🤖 **The AI agent may only answer using these articles and this playbook.** Where is the AI's source material kept? ✏️ ______

## 1.2 Saved replies (macros)
Write these first (use **Appendix B** for ready-made wording):
- [ ] Welcome / first reply
- [ ] "We're looking into it"
- [ ] Need more info (what to ask for)
- [ ] Bug confirmed
- [ ] Feature request received
- [ ] Refund approved / refund declined
- [ ] Apology for a mistake
- [ ] Out-of-hours auto-reply
- [ ] Closing / "did this fix it?"
✏️ Where are macros stored? ______

## 1.3 Ticket rules
**Every ticket must have (DEFAULT):** customer name/email · channel · severity (P1–P4) · category tag · owner · status · date opened.

**Status list (DEFAULT):** `New → In progress → Waiting on customer → Waiting on engineering → Solved → Closed`
**Category tags (DEFAULT):** `Bug · How-to · Billing · Account · Feature request · Feedback · Security · Privacy · Other`
✏️ **Add tags specific to your product:** ______
✏️ **When do we auto-close "Waiting on customer" tickets?** (DEFAULT: 7 days, after one reminder on day 3)

## 1.4 Escalation map (who to call when)
| Problem type | First person | If no answer in… | Then |
|---|---|---|---|
| Bug / product broken | | 2 hours (P1) / 1 day (P2) | |
| Security issue | | 30 minutes | |
| Billing / payment error | | 1 day | |
| Privacy / data request | | 1 day | |
| Legal threat / press inquiry | | Immediately | |
| AI behaving badly | | Immediately | |

**Escalation note (DEFAULT contents):** what the customer said · steps to reproduce · what was already tried · device/browser/version · screenshots · severity · customer impact (how many people?)

## 1.5 Bug handoff (support → engineering)
✏️ Where do bugs get logged? ______
✏️ Who reads that list and how often? ______
✏️ How does support learn the bug is fixed so it can tell the customer? ______

## 1.6 Incident plan (if the product breaks)
- [ ] Status page created at: ______
- [ ] Draft "we know about the problem" message ready (see **Appendix C**)
- [ ] One person decides when an incident is declared: ______
- [ ] One person writes customer updates: ______
- [ ] "All clear" message ready
- [ ] Post-mortem template ready (**Appendix D**)

## 1.7 Security issue playbook ⚠️
**1.7.1 Where do customers or researchers report security problems?** ✏️ (email/form)
**1.7.2 First action when a report arrives** (DEFAULT: escalate to the security owner within 30 minutes; do NOT discuss details publicly or with the AI.)
**1.7.3 Who decides whether customers must be told?** ✏️
**1.7.4 Legal deadlines for telling people/regulators** (GDPR example: 72 hours for certain personal-data breaches; confirm with a professional) ✏️

## 1.8 Test it before real customers do
- [ ] Send a test email → ticket appears → reply works
- [ ] Open the chat widget → AI answers a known question correctly
- [ ] Ask the AI something it should NOT answer → it hands off
- [ ] Type "I want a human" → handoff works and passes context
- [ ] Ask the AI for a refund → it does NOT promise one
- [ ] Ask for another customer's data → it refuses
- [ ] Out-of-hours auto-reply shows
- [ ] Test survey (CSAT) sends and records
- [ ] A friend or teammate tries to break it and writes down what failed

## 1.9 Special cases: VIPs, contracts, press, legal, and safety ⚠️
| Situation | ✏️ Who handles it | ✏️ What we do (DEFAULT shown) |
|---|---|---|
| **VIP / key customer** (define: ______) | | Reply within half the normal target; owner named; contact directly |
| **Enterprise contract or custom SLA** | | Check the contract first; log promised times and credits |
| **SLA missed** | | Apologise, explain, offer credit only if the contract/policy says so |
| **Press / media question** | | Nobody replies except the named person; send nothing until reviewed |
| **Regulator / government request** | | Don't reply alone; forward to the named legal contact the same day |
| **Legal threat or court paper** | | Stop discussing the issue; forward to counsel within 1 business day |
| **Police or law-enforcement request** | | Never share data by chat/email; verify through the legal contact |
| **Chargeback / payment dispute** | | Collect proof (ticket history, usage, policy) within the processor's deadline |
| **Harassment or threats toward staff** | | Stop replying, save evidence, escalate; see 0.6.6 |
| **Customer mentions harming themselves or others** | | **Human takes over immediately.** Respond with care and point to local emergency services. The AI does not handle this. |
| **Public complaint / viral post** | | Reply publicly with empathy, move details to a private channel, tell the owner |

✏️ **Legal contact (name, email, phone):** ______
✏️ **Press contact:** ______

## 🚦 PHASE 1 GATE – Ready for first users?
- [ ] 10+ help articles live and checked
- [ ] Saved replies written
- [ ] Ticket statuses, tags, and owners set up
- [ ] Escalation map has real names and contacts
- [ ] Incident + security plans written
- [ ] Special-case table (1.9) has real names
- [ ] All tests in 1.8 passed
**Gate approved by:** ______ **Date:** ______

---

# PHASE 2 – BETA (Small group of early users)

**Goal:** Learn what confuses people. Beta users forgive rough edges; use them to find the holes.

## 2.1 Beta setup
| Question | ✏️ Your answer |
|---|---|
| How many beta users? (DEFAULT: 10–50) | |
| How do you pick them? | |
| How do they contact you? (best: one direct channel) | |
| What do you tell them up front? ("This is early; expect bugs; here's how to reach us.") | |
| Dates (start–end) | |

## 2.2 Beta support style (DEFAULT)
- Reply personally, not with robotic text.
- Ask for feedback in every conversation.
- Founder reads **every** ticket.
- Log every question to the "Things that confused people" list (2.3).

## 2.3 Learning log
| Date | What the customer asked | What was confusing | Fix (article / product / reply) | Done? |
|---|---|---|---|---|
| | | | | [ ] |

## 2.4 Weekly beta review (15 minutes, every week)
Answer in writing:
1. How many tickets this week? ______
2. Top 3 contact reasons: ______
3. What did the AI answer well? ______ What did it get wrong? ______
4. Which help articles do we need to add or fix? ______
5. Any bug that came up 3+ times? ______

## 2.5 AI quality check
✏️ Read **20 AI conversations** from beta. Fill in:
| Question | Answer |
|---|---|
| Correct answers (out of 20) | |
| Wrong answers (out of 20) | |
| Handoffs that should have happened but didn't | |
| Handoffs that happened but weren't needed | |
| Anything the AI promised that it shouldn't have | |
| Changes we made to the AI's instructions | |

**Ready-to-scale rule (DEFAULT):** at least **18 of 20** AI answers correct, with zero promises about refunds/dates/features that aren't in this playbook.

## 2.6 Beta customer feedback
**Survey question (DEFAULT):** "How easy was it to get help? (1–5)" + "What would make support better?"
✏️ Average score: ______ | Top comment: ______

## 🚦 PHASE 2 GATE – Ready to launch?
- [ ] Top 5 contact reasons each have a help article
- [ ] No unresolved P1 or P2 issues
- [ ] AI passes the 18/20 check
- [ ] Beta feedback reviewed and acted on
- [ ] Support hours and reply targets still realistic for the launch size
**Gate approved by:** ______ **Date:** ______

---

# PHASE 3 – LAUNCH (Public release)

**Goal:** Survive the first rush of attention and learn fast.

## 3.1 Launch-day plan
| Question | ✏️ Your answer |
|---|---|
| Launch date and time (with time zone) | |
| Where are you announcing it? | |
| How many sign-ups do you expect on day 1? (best, normal, worst case) | |
| Who is watching support all day? | |
| Who is on call for engineering? | |
| Which channel do you check first, every hour? | |
| Is the status page live? | [ ] Yes |
| Are the macros and help articles live? | [ ] Yes |

## 3.2 Launch-day rules (DEFAULT)
- Check the queue **every 30 minutes** during the first 4 hours, then **hourly**.
- Answer every P1 in **under 1 hour**, every P2 in **under 4 hours**.
- If more than **5 customers** report the same problem, call it an **incident** and post on the status page.
- Post a thank-you / "known issues" update at the end of the day.
- Write down every surprise in the **Learning log** (2.3).

## 3.3 Launch surge plan
**If tickets are 3× more than normal, what do we do?** (tick what applies)
- [ ] Turn on a banner: "We're getting lots of messages; replies may take up to ___ hours"
- [ ] Let the AI handle more, with more careful handoffs
- [ ] Pause non-urgent channels (e.g., social DMs)
- [ ] Ask a friend or freelancer to help (name: ______)
- [ ] Write a quick "known issue" article and link it in auto-replies

## 3.4 Day 1, Day 3, Day 7 check-ins
| When | Questions | ✏️ Answers |
|---|---|---|
| End of Day 1 | Tickets? Biggest problem? Anything broken? | |
| Day 3 | Which article gets the most views? What's missing? | |
| Day 7 | Reply times met? CSAT? Top 5 reasons? | |

## 🚦 PHASE 3 GATE – Stable after launch?
- [ ] Reply targets met for 7 days in a row (or reasons written down)
- [ ] No open P1
- [ ] Top 5 reasons have articles
- [ ] First weekly metrics report written (see 4.3)
**Gate approved by:** ______ **Date:** ______

---

# PHASE 4 – CUSTOMERS 1–100 (High-touch learning)

**Goal:** Treat every customer like a VIP. Your first 100 teach you everything.

## 4.1 Daily routine (DEFAULT, 30–60 minutes)
1. Check all channels
2. Reply to P1/P2
3. Review what the AI answered (spot-check 5 conversations)
4. Tag every ticket
5. Add new questions to the "Things that confused people" list
6. Update at least one help article if needed

## 4.2 Onboarding help
**4.2.1 What does a new customer get after signing up?** ✏️ (welcome email? checklist? personal message?)
**4.2.2 Do you personally greet the first 100 customers?** (DEFAULT: Yes) ✏️
**4.2.3 What is the "aha moment" (when the customer first gets value)?** ✏️
**4.2.4 If a customer hasn't reached it after 3 days, what do we send?** ✏️

## 4.3 Weekly numbers (fill every week)
| Metric | Meaning | Target (DEFAULT) | This week | Last week |
|---|---|---|---|---|
| Customers so far | | toward 100 | | |
| Tickets opened | | | | |
| Tickets per 100 customers | Are people confused? | falling over time | | |
| First Response Time | How fast we reply | meets SLA 90%+ | | |
| Time To Resolution | How fast it's fixed | meets SLA 90%+ | | |
| CSAT | Happy customers | 85%+ | | |
| AI resolved without human | AI success | track only | | |
| AI handoff rate | How often AI passes it on | track; discuss if much lower than expected | | |
| Reopened tickets | Fix didn't work | under 10% | | |
| Open P1/P2 | | 0 | | |
| Top 3 contact reasons | | | | |

## 4.4 Feedback loop (support → product)
**4.4.1 How do customer requests reach the product plan?** ✏️ (DEFAULT: weekly 15-minute review of tags "Bug" and "Feature request".)
**4.4.2 How do you tell a customer when their idea ships?** ✏️
**4.4.3 Top 5 requests so far:** 1) … 2) … 3) … 4) … 5) …

## 4.5 Reviews and testimonials
**Do you ask happy customers for a review?** ✏️ When and how: ______
⚠️ Never invent, buy, or write fake reviews. Only share real ones, with permission.

## 4.6 Churn and cancellation
**When someone cancels, do we ask why?** (DEFAULT: yes, one question.) ✏️ Question: ______
**Save-offer rules** (what can we offer before they go?) ✏️

## 4.7 Support → marketing and customer acquisition link
Support is where you hear customers' real words and where happy customers bring in friends.

| Moment | Question | ✏️ Your answer |
|---|---|---|
| **Onboarding emails** | What 3 emails go out in the first 7 days, and what questions do they answer before customers ask? | |
| **Customer language** | Where do you save phrases customers use to describe their problem? (use them in website and ads) | |
| **Reviews** | When do you ask for a review, on which site, and who asks? | |
| **Testimonials / case studies** | How do you ask permission, and where is permission recorded? | |
| **Referrals** | Is there a "invite a friend" offer? What is it, and who handles questions about it? | |
| **Community** | Which community channel opens, who hosts it, and what are the rules? | |
| **Launch announcements** | How are customers who reported a bug or idea told when it ships? | |
| **Help content as marketing** | Which help articles can also be public guides that bring in new visitors? | |
| **Churn voice** | Where do cancellation reasons go so marketing and product see them? | |
| **Handoff to sales** | If a customer asks about a bigger plan, who gets the lead within how long? | |

⚠️ Reviews, testimonials, and referral claims must be real, with permission. Never fake or pay for fake ones.

## 🚦 PHASE 4 GATE – First 100 done?
- [ ] 100 customers reached (date: ______)
- [ ] 4+ weeks of metrics recorded
- [ ] Top 10 contact reasons each have an article or product fix
- [ ] CSAT at or above target for 4 weeks
- [ ] Repeat questions are now handled mostly by AI/help center
- [ ] Support hours or help planned for the next stage
**Gate approved by:** ______ **Date:** ______

---

# PHASE 5 – CUSTOMERS 101–500 (Systemise and scale)

**Goal:** Keep the quality, lose the chaos. The same question should never be answered by hand 20 times.

## 5.1 Find what's repeating
✏️ **List the top 10 contact reasons this month and what you'll do about each.**
| Rank | Reason | # tickets | Fix (article / product change / AI answer / process) | Owner | Date |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |

## 5.2 Level up the AI (monthly)
- [ ] Review 20 AI conversations, including ones with low CSAT
- [ ] Add answers for repeated questions
- [ ] Fix every wrong answer found (write what changed)
- [ ] Re-test handoff triggers (Phase 1.8 tests)
- [ ] Check handoff rate: too low = AI guessing; too high = AI under-trained
✏️ **AI change log:**
| Date | What went wrong | What we changed | Result |
|---|---|---|---|

## 5.3 When to get help (hiring or outsourcing triggers)
Tick and date the ones that happen:
- [ ] Reply times missed on 3+ days in a week
- [ ] Support takes more than ___ hours/week (DEFAULT: 15)
- [ ] Backlog above ___ tickets for 3 days (DEFAULT: 20)
- [ ] Founder can't focus on product because of support
**If 2+ are ticked → decide:** hire part-time support / use a freelancer / add more automation. ✏️ Decision and date: ______

**Hand-over kit for a new helper:** this playbook · tool logins (via password manager) · macros · escalation map · 5 example great replies · first-week plan.

## 5.4 Customer groups (optional but useful)
| Group | How we spot them | Special care |
|---|---|---|
| Key / high-value customers | | |
| Free users | | |
| Customers at risk of leaving | | |

## 5.5 Monthly business review (60 minutes, once a month)
1. Numbers table (see 4.3), compared to last month
2. Top 10 reasons and their fixes
3. Best and worst conversations (human + AI)
4. Policy changes needed (refund, hours, SLA)
5. Incidents this month and lessons (Appendix D)
6. Goals for next month: ______

## 5.6 Milestone checkpoints
| Customers | Date reached | What we learned | What we changed |
|---|---|---|---|
| 100 | | | |
| 250 | | | |
| 500 | | | |

## 5.7 Support cost review (monthly)
| Item | This month | Last month |
|---|---|---|
| Total support cost (tools + time + help) | | |
| Tickets | | |
| **Cost per ticket** | | |
| **Support cost per customer** | | |
| Savings from AI/help center (tickets avoided × cost per ticket; estimate) | | |

✏️ Is cost per customer below the maximum set in 0.11? [ ] Yes [ ] No. If no, what's the fix? ______

## 5.8 Referral and growth loop check
✏️ How many new customers this month came from referrals/reviews/community? ______
✏️ What support moment (4.7) worked best? ______ What will we try next? ______

## 🚦 PHASE 5 GATE – 500 customers: done well?
- [ ] 500 customers reached (date: ______)
- [ ] SLA targets met 90%+ for last 4 weeks
- [ ] CSAT at or above target
- [ ] AI correct-answer check passed this month
- [ ] Hiring/outsourcing decision made
- [ ] Cost per customer within budget (5.7)
- [ ] Next-stage plan written (what changes after 500?)
**Sign-off by:** ______ **Date:** ______

---

# APPENDICES (copy, paste, and edit)

## Appendix A – Master Readiness Checklist (one-page summary)
| Phase | Gate passed? | Date |
|---|---|---|
| 0 Build | [ ] | |
| 1 Pre-launch | [ ] | |
| 2 Beta | [ ] | |
| 3 Launch | [ ] | |
| 4 Customers 1–100 | [ ] | |
| 5 Customers 101–500 | [ ] | |

## Appendix B – Reply templates
Replace `[brackets]`.

**B1. First reply**
> Hi [Name], thanks for reaching out. I'm [Your name] from [Product]. I understand you're [problem in your own words]. [Answer or next step]. I'll check back by [time]. If it's urgent, just reply here.

**B2. Need more info**
> Thanks, [Name]. To help faster, could you share: (1) what you were trying to do, (2) what happened instead, (3) a screenshot if possible, (4) your device and browser/app version? Please don't send passwords or card numbers.

**B3. Bug confirmed**
> You're right, [Name], that's a bug, and I'm sorry for the trouble. Our team is working on it. [Workaround if any]. I'll update you by [date].

**B4. Feature request**
> Thanks for the idea, [Name]. I've added it to our list. I can't promise a date, but I'll tell you if it's planned.

**B5. Refund approved / declined**
> Approved: "I've refunded [amount]. It should reach you in [timeframe]."
> Declined: "I looked carefully. Unfortunately [reason, based on policy]. Here's what I can do instead: [option]."

**B6. Apology (when we made a mistake)**
> I'm sorry, [Name]. We got this wrong: [what happened]. Here's what we did to fix it: [action]. Here's how we'll prevent it: [action].

**B7. Closing**
> Glad that's sorted, [Name]. If anything else comes up, reply anytime. Would you rate your support experience? [link]

**B8. AI handoff message (customer sees this)**
> I'm passing you to [Name/our team] so you get the best help. I've shared everything you told me, so you won't need to repeat it. You'll hear back by [time].

## Appendix C – Incident messages
**Starting:** "We're aware that [what's affected]. We're investigating. Next update by [time]. Status: [link]."
**Update:** "Update [time]: [what we know]. [What we're doing]. Next update by [time]."
**Resolved:** "Fixed as of [time]. Cause: [plain words]. What we're doing to prevent it: [action]. Sorry for the trouble."

## Appendix D – Post-mortem template (after any P1 or serious P2)
| Question | ✏️ Answer |
|---|---|
| What happened (timeline)? | |
| Who/how many customers were affected? | |
| How did we find out? | |
| What was the root cause? | |
| What went well? | |
| What went badly? | |
| 3 actions to stop it happening again (owner + date) | |
| Did customers get told on time? | |

(Keep it about fixing the system, not blaming a person.)

## Appendix E – AI Support Agent instruction template 🤖
Copy this into your AI agent's instructions and fill in the brackets from this playbook.

```
ROLE: You are [AgentName], the support assistant for [Product]. You help [customer type].
DISCLOSURE: Start by saying you are an AI assistant. Offer a human at any time.
TONE: [from 0.1.3]. Short, clear, kind.
SOURCES: Answer ONLY from [help center link / KB location] and the Customer Support Playbook.
  If the answer isn't there, say you're not sure and hand off to a human.
YOU MAY: answer FAQs, explain how-tos, check order/account status, collect details
  (what happened, device, screenshot), tag tickets, draft replies for human review.
YOU MUST NEVER: promise refunds, dates, discounts, or features; give legal, medical, or
  financial advice; share another customer's data; ask for passwords or card numbers;
  argue with the customer; invent information.
HAND OFF TO A HUMAN IF: customer asks for a human; you're unsure; customer is angry;
  2 failed attempts; topic is billing/refund/legal/privacy/security/accessibility/cancellation/
  chargeback; key account.
HANDOFF FORMAT: summary of the issue · what customer wants · what was tried · severity (P1–P4)
  · customer sentiment · customer's contact details.
AFTER HANDOFF: tell the customer a human will reply by [time per severity].
LOGGING: tag every conversation: category, severity, resolved-by (AI/human), handoff reason.
```

## Appendix F – Physical-product add-on (skip if not physical)
| Question | ✏️ Your answer |
|---|---|
| Shipping times and carriers | |
| What if the package is late or lost? | |
| Return window and who pays return shipping | |
| Damaged or wrong item process (photo needed?) | |
| Warranty length and what's covered | |
| Replacement vs. refund rule | |
| Safety recall process (who decides, how customers are told) | |

## Appendix G – Final Quality Review ("is this document ready?")
Before using this playbook, check:
- [ ] No empty answers (every blank has an answer, `TBD – who – date`, or `N/A – because…`)
- [ ] Every person named has contact details
- [ ] All dates are real dates
- [ ] A stranger could follow it without asking you anything
- [ ] The AI instructions (Appendix E) match Phase 0.5
- [ ] A second person has read it and noted anything confusing
**Reviewed by:** ______ **Date:** ______

## Appendix H – Good answer vs. bad answer (anti-guessing rules)
Compare each answer you wrote with this table.

| Section | ✅ Good answer looks like | ❌ Bad answer looks like |
|---|---|---|
| Names / owners | "Maria Lopez, maria@…" | "The team", "someone", "TBD" with no name/date |
| Reply times | "P2: first reply within 4 business hours" | "ASAP", "quickly" |
| Channels | "Email: support@acme.com, checked 9am–5pm ET" | "We'll see what customers prefer" |
| Policies | "Full refund within 14 days of purchase, via original card" | "Case by case" |
| AI rules | "AI never promises refunds; hands off on billing" | "AI uses good judgement" |
| Handoff | "After 2 failed answers or any anger word" | "When it can't help" |
| Dates | "2026-11-05" | "Soon", "next quarter" |
| Metrics targets | "CSAT ≥ 85% over 4 weeks" | "High satisfaction" |
| Privacy | "Data deletion within 30 days; request via privacy@acme.com" | "We respect privacy" |
| Costs | "$49/month helpdesk; $30 AI usage at 100 customers" | "Cheap" |
| Escalation | "Security issue → Sam (+1-555-0100); no answer in 30 min → Jo" | "Tell an engineer" |
| Help articles | "Article 'Reset password', reviewed 2026-11-01, link ___" | "Docs exist" |

**Quick test for every answer:** *Could a stranger or an AI agent act on this answer without asking me a question?* If no, make it more specific.

## Appendix I – Metric formulas and monthly report

**Formulas (simple version)**
| Metric | Formula |
|---|---|
| First Response Time (FRT) | Time of first reply − time ticket arrived (average and the slowest 10%) |
| Time To Resolution (TTR) | Time ticket solved − time ticket arrived |
| SLA met % | Tickets answered within target ÷ all tickets × 100 |
| CSAT % | Happy ratings (4–5) ÷ all ratings × 100 |
| AI resolution rate | Conversations solved with no human ÷ all AI conversations × 100 |
| AI handoff rate | Conversations passed to a human ÷ all AI conversations × 100 |
| Wrong-AI-answer rate | Wrong answers found in spot-checks ÷ conversations checked × 100 |
| Reopen rate | Tickets reopened ÷ tickets solved × 100 |
| Tickets per 100 customers | Tickets ÷ customers × 100 |
| Backlog | Open tickets older than the SLA target |
| Cost per ticket | (Tool costs + support time cost) ÷ tickets |

💡 A handoff rate near zero can mean the AI is guessing, not succeeding. Always read some conversations, not just the numbers.

**Monthly report (copy each month)**
| Item | ✏️ Answer |
|---|---|
| Month | |
| Customers (start → end) | |
| Tickets and tickets per 100 customers | |
| FRT / TTR vs. targets | |
| SLA met % | |
| CSAT % and top comment | |
| AI resolution, handoff, and wrong-answer rates | |
| Top 5 contact reasons | |
| Incidents (count, worst severity) | |
| Cost per ticket and per customer | |
| 3 wins | |
| 3 problems | |
| 3 actions for next month (owner + date) | |

## Appendix J – Completion Score
How to score: count the `✏️` questions and tables in each phase. Count how many have a real answer (not blank, not vague `TBD`). Divide answered ÷ total × 100.

| Part | Total questions | Answered | % complete | Required to pass |
|---|---|---|---|---|
| A–B Document control & snapshot | | | | 100% |
| Phase 0 Build | | | | 100% |
| Phase 1 Pre-launch | | | | 100% |
| Phase 2 Beta | | | | 100% before launch |
| Phase 3 Launch | | | | 100% before launch day |
| Phase 4 Customers 1–100 | | | | 90%+ by customer 100 |
| Phase 5 Customers 101–500 | | | | 90%+ by customer 500 |
| Appendices used | | | | as needed |

**Overall rule (DEFAULT):** Do not launch (Phase 3) until Parts A–B and Phases 0–2 are **100%**. Items marked `TBD` count as unanswered until they have a real answer.

## Appendix K – Worked example (fictional product "PlantPal")
This shows what a filled-in answer looks like. Copy the style, not the words.

| Question | Example answer |
|---|---|
| B1 Product type | Mobile app |
| B2 Customer | Busy city workers aged 25–40 with 5+ houseplants |
| B3 Top 3 reasons | 1) Reminders not arriving 2) Billing/subscription 3) "How do I add a plant?" |
| B5 Support lead | Maria Lopez, 10 hrs/week, Eastern Time |
| 0.2 Email | support@plantpal.example, checked Mon–Fri 9am–5pm ET, reply within 24 hours |
| 0.2.2 Out-of-hours text | "Thanks! Our team is offline. We'll reply by 5pm ET next business day. Meanwhile, our AI assistant can help." |
| 0.4 Edited P1 | "App crashes on open for all users, or wrong charge to any customer. First reply 1 hour, 24/7." |
| 0.5 Human-only | Refunds, billing disputes, any message with "lawyer" or "scam", accessibility needs |
| 0.6.1 Refund policy | "Full refund within 14 days of purchase via the original payment method; after that, no refund unless the app didn't work." |
| 0.7 Data request | privacy@plantpal.example; Maria answers within 30 days after checking ID by replying from the account email |
| 0.9.1 AI owner | Sam Chen |
| 0.9.7 Kill switch | Sam turns off the chat widget in the admin panel (2 minutes); customers see "Chat is paused. Email us." |
| 0.9.9 Golden question #1 | Q: "How do I cancel?" → A: "Settings > Subscription > Cancel; you keep access until the period ends." Hand off? No |
| 0.10.1 Languages | English at launch; Spanish by Dec 15 (Maria's cousin checks articles) |
| 0.11 Helpdesk cost | $29/month now; ~$49/month at 500 customers |
| 1.4 Security escalation | Sam (+1-555-0100) → if no answer in 30 minutes → Maria |
| 1.9 VIP definition | Anyone on the Team plan ($99+/month) |
| 2.5 AI quality check | 19/20 correct; 1 wrong (said annual plan refund was 30 days; fixed article 3) |
| 3.1 Launch time | 2026-12-01 at 10:00 ET on Product Hunt |
| 4.3 Weekly row | Customers 62 · tickets 41 · FRT 3h 10m · CSAT 88% · AI handoff rate 22% |
| 4.7 Referral | "Give a month, get a month." Maria handles questions; tracked in the sheet "Referrals" |
| 5.3 Hiring trigger | Tickets over 20 backlog 3 days running → hire 10 hrs/week freelancer |
| 5.7 Cost per ticket | ($49 tools + $400 time) ÷ 180 tickets = $2.49 |

---
*End of Customer Support Playbook. Copy this file for each new project and fill it in from the top.*
