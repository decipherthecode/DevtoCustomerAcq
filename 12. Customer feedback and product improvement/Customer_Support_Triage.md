# HOW TO FILL THIS DOCUMENT (Read this first, 3 minutes)

**What is this?**
This is a *question-and-answer* document. You answer the questions, and at the end you have a complete plan for how your team (and your AI helpers) will sort, answer and learn from customer messages, from the day you start building until your **first 500 customers**.

**"Triage"** means *sorting messages by how urgent they are*, like a nurse deciding who needs help first.

## The 7 simple rules

1. **Go in order.** Start at Part 0 and finish at Part 15. Do not skip around.
2. **Every question has 4 pieces:**
   - **Question:** what we want to know.
   - **Why we ask:** so you understand the reason.
   - **Example:** a filled-in sample. Copy its *style*, not its words.
   - **✏️ Your answer:** type your answer on the line after the pencil.
3. **Short answers are great.** One clear sentence beats a long paragraph.
4. **Never guess silently.** If you do not know, write `TBD (to be decided) | Owner: <name> | Date: <YYYY-MM-DD>`. A `TBD` with an owner and a date is allowed. An empty box is not.
5. **Pick-from-a-list questions:** replace `[ ]` with `[x]` for your choice(s).
6. **Use real names, real numbers, real dates.** Write "Priya, within 4 hours", not "someone soon".
7. **Do not delete questions.** If one does not apply, write `N/A because <reason>`.

## Symbols used in this document

| Symbol | Meaning |
|---|---|
| ✏️ | Your answer goes here |
| 💡 | A helpful hint |
| ⚠️ | Be careful, this prevents a common mistake |
| 🤖 | Rule that your AI helpers will read and follow |
| 👤 | A human must do or approve this |
| [ ] / [x] | Empty box / ticked box |

## What you will have when you finish
A single file that answers: *Who looks at customer messages? How do we decide what is urgent? When do we call for help? How do we turn complaints into a better product? How do we know it is working?*

## How AI agents use this file
🤖 AI agents must treat this file as the **source of truth**. If an answer is missing, marked `TBD`, or unclear, the agent **must not guess**. It must stop and ask the Triage Owner (Part 2).

## Time needed
- First fill-in: about 60 to 90 minutes.
- Re-check: 15 minutes at the start of every phase (see Part 10).

---

# TABLE OF CONTENTS

| Part | Title |
|---|---|
| 0 | Document control |
| 1 | About your product |
| 2 | People and owners |
| 3 | Where customers talk to you (channels) |
| 4 | AI helper rules |
| 5 | Ticket categories and tags |
| 6 | Urgency: severity and priority |
| 7 | The triage steps and the Ticket Card |
| 8 | Escalation: when to ask for help |
| 9 | Reply templates |
| 10 | Life-cycle phases: Build to first 500 customers |
| 11 | Feedback to product improvement loop |
| 12 | Measuring success and milestone tracker |
| 13 | Review rhythm |
| 14 | "What if…" emergency plans |
| 15 | Final checklist and sign-off |
| A | Glossary (plain words) |
| B | Research basis |

---

# PART 0. DOCUMENT CONTROL

**Why:** So anyone opening this file knows whose it is and whether it is current.

| Field | ✏️ Your answer |
|---|---|
| Project / product name | |
| Document owner (one person) | |
| Date first filled (YYYY-MM-DD) | |
| Version (start with 1.0) | |
| Status (Draft / In review / Approved) | |
| Next scheduled review date | |

**Change log** (add a row every time you edit):

| Date | Version | What changed | Who changed it |
|---|---|---|---|
| | 1.0 | First version | |

---

# PART 1. ABOUT YOUR PRODUCT

**Why:** Triage rules depend on what your product does and who pays for it. A cooking app and a banking app need very different rules.

**Q1.1 In one sentence, what does your product do, and for whom?**
*Example:* "A phone app that helps small shops send invoices to customers."
✏️

**Q1.2 What kind of product is it?** (tick one)
- [ ] Mobile app
- [ ] Website or web app
- [ ] Desktop software
- [ ] Physical device plus software
- [ ] API or developer tool
- [ ] Other: ______

**Q1.3 Does your product handle any of these sensitive things?** (tick all that apply)
- [ ] Money or payments
- [ ] Health information
- [ ] Children's information (under 13 or under 18)
- [ ] Personal data such as names, emails, phone numbers
- [ ] Safety (a failure could hurt someone)
- [ ] None of these

💡 Every tick here makes some messages automatically *more urgent* in Part 6.

**Q1.4 Do you have different customer plans?**
*Example:* Free, Pro, Business.
✏️ Plans and what each includes:

**Q1.5 Which stage are you in right now?** (tick one)
- [ ] Building (no users yet)
- [ ] Internal testing (only our team uses it)
- [ ] Beta (a small invited group uses it)
- [ ] Launched, customers 1 to 10
- [ ] Customers 11 to 100
- [ ] Customers 101 to 250
- [ ] Customers 251 to 500

**Q1.6 Key dates.**

| Milestone | ✏️ Planned date |
|---|---|
| Internal test starts | |
| Beta starts | |
| Public launch | |
| Target date for customer #500 | |

**Q1.7 What is the single biggest promise your product makes to customers?**
*Why:* If this promise breaks, that problem is always urgent.
*Example:* "Invoices always reach the customer within one minute."
✏️

---

# PART 2. PEOPLE AND OWNERS

**Why:** A problem with no named owner does not get fixed. Every role needs a **name** and a **backup**.

**Q2.1 Fill in the table.** One person can hold several roles when the team is small. Write the same name again if so.

| Role | What this person does | ✏️ Name | ✏️ Backup | ✏️ How to reach (phone / chat) |
|---|---|---|---|---|
| **Triage Owner** 👤 | Makes sure every message is sorted in time. Owns this document. | | | |
| **Approver** 👤 | Approves risky AI replies and all P0/P1 actions (Part 6). | | | |
| **Support Responder** | Writes replies to customers. | | | |
| **Engineering Contact** | Fixes bugs. | | | |
| **Product Owner** | Decides what to build next (Part 11). | | | |
| **Security / Privacy Contact** | Handles data leaks, hacking, legal privacy requests. | | | |
| **Billing Contact** | Handles refunds and payment problems. | | | |
| **Executive Sponsor** | Final say in a crisis. | | | |

**Q2.2 What are your working hours and time zone?**
*Example:* "Mon to Fri, 9:00 to 18:00, India Standard Time."
✏️

**Q2.3 Who is on duty after hours, weekends and holidays?**
*Example:* "Only P0 issues; Ravi is on-call every other weekend."
✏️

**Q2.4 If the Triage Owner and the Backup are both unavailable, who decides?**
✏️

---

# PART 3. WHERE CUSTOMERS TALK TO YOU (CHANNELS)

**Why:** Messages arrive from many places. If nobody watches a place, customers feel ignored. **Pick one "home" for all feedback** so nothing is lost (a shared inbox, a board, a spreadsheet, or a tool).

**Q3.1 Where will ALL messages be collected and stored?** (the "home")
*Example:* "Shared support inbox plus a Notion board called 'Customer Feedback'."
✏️

**Q3.2 Fill in the table for each channel.**

| Channel | In use? (Yes/No) | ✏️ Where exactly (address, link, handle) | ✏️ Who watches it | ✏️ How often they check | ✏️ First-reply promise | Can AI reply alone? |
|---|---|---|---|---|---|---|
| Email and web contact form | | | | | | |
| In-app chat and in-product feedback button | | | | | | |
| Social media and communities (X, Reddit, Discord, forums) | | | | | | |
| App store reviews and surveys (ratings, NPS, CSAT) | | | | | | |
| Other: ______ | | | | | | |

*Example row:* "Email | Yes | help@mycompany.com | Anita | twice a day | within 1 working day | No, a human approves first."

**Q3.3 Do you want a "How to reach us" message published to customers?**
- [ ] Yes, in the app and on the website
- [ ] Yes, on the website only
- [ ] Not yet (TBD with owner and date)

**Q3.4 What do customers see right after they send a message?** (the auto-reply)
*Example:* "Thanks! We got your message and will reply within 1 working day. If your app is completely down, reply with the word URGENT."
✏️

---

# PART 4. AI HELPER RULES 🤖

**Why:** AI can sort fast, but it can be confidently wrong. These rules say what it may do, what it may never do, and when a human must step in.

**Working mode chosen for this template: "AI triages, human approves."** AI reads, tags, rates and drafts. A named person approves anything risky.

**Q4.1 Which AI tools or agents will touch customer messages?**
*Example:* "Claude through our helpdesk; an in-app chatbot."
✏️

**Q4.2 What is the AI ALLOWED to do on its own?** (tick all that apply)
- [ ] Read incoming messages
- [ ] Add a category and tags (Part 5)
- [ ] Suggest a severity and priority (Part 6)
- [ ] Group duplicates ("same problem as ticket #123")
- [ ] Draft a reply for a human to review
- [ ] Send a reply on its own, **only** for these safe topics: ______
- [ ] Summarise weekly feedback themes (Part 11)

**Q4.3 What must the AI NEVER do?** (these are pre-ticked as our recommended safety rules; add your own)
- [x] Never promise refunds, discounts, dates or new features
- [x] Never share one customer's data with another
- [x] Never give legal, medical or financial advice
- [x] Never argue with or blame the customer
- [x] Never close a P0 or P1 ticket
- [x] Never delete tickets or customer data
- [x] Never invent facts. If unsure, say so and escalate
- [ ] Add your own: ______

**Q4.4 When MUST the AI hand the ticket to a human?** (recommended triggers are pre-ticked)
- [x] The AI is not sure what the customer wants (low confidence)
- [x] The message involves money, health, children, safety, legal, or privacy
- [x] The customer is upset, scared, threatening to leave, or mentions a lawyer, the press, or a competitor
- [x] The customer asks for a human
- [x] The same customer wrote 3 or more times about one issue
- [x] The request is outside what the product does
- [x] The AI disagrees with the customer and cannot settle it
- [ ] Add your own: ______

**Q4.5 What confidence level is "sure enough"?**
*Example:* "If the AI is less than 80% sure of the category, a human checks it."
✏️ Number: ______ %

**Q4.6 Who is the human accountable if the AI makes a mistake?**
*Why:* Someone must own the outcome, always.
✏️ Name:

**Q4.7 Do customers get told they are talking to AI?**
- [ ] Yes, clearly, at the start
- [ ] Yes, in the footer of replies
- [ ] No (⚠️ check local laws and your own values before choosing this)

**Q4.8 How does a customer reach a real person?**
*Example:* "Typing 'human' or clicking 'Talk to a person' goes to the Support Responder within 1 hour in working time."
✏️ Maximum wait for a human after the customer asks: ______

**Q4.9 The "kill switch": how do we turn the AI off quickly if it misbehaves?**
*Example:* "Triage Owner toggles 'AI replies' off in settings; everything goes to the human queue."
✏️ Who can press it: ______ How: ______

**Q4.10 How do we keep a record of what the AI did?**
*Example:* "Every AI action is written in the ticket history with the reason."
✏️

---

# PART 5. TICKET CATEGORIES AND TAGS

**Why:** Categories answer "what is this about?" so each message goes to the right person and patterns can be counted later.

**Q5.1 Review the starter categories.** Keep, rename or delete. Add more only if truly needed. **Aim for 6 to 10 categories.**

| # | Category | Plain meaning | ✏️ Keep? (Y/N) | ✏️ Owner who handles it | Goes to roadmap? |
|---|---|---|---|---|---|
| C1 | **Bug / Not working** | Something is broken or wrong | | | Yes, as a fix |
| C2 | **How-to question** | "How do I do X?" | | | Only if many ask (docs gap) |
| C3 | **Feature request** | "Please add X" | | | Yes, as an idea |
| C4 | **Usability complaint** | "It's confusing or slow" | | | Yes |
| C5 | **Account and login** | Cannot sign in, password, access | | | Sometimes |
| C6 | **Billing and refunds** | Charges, invoices, plan changes | | | Rarely |
| C7 | **Security and privacy** | Possible hack, data leak, "delete my data" | | | Yes, urgent |
| C8 | **Praise / Testimonial** | Happy customer | | | No, but share with the team |
| C9 | **Spam / Not for us** | Irrelevant or junk | | | No |
| C10 | **Other / Unclear** | Cannot tell yet | | | Review weekly |

**Q5.2 Which "tags" do you want to add on top?** Tags give extra detail. Starter list, edit freely:

| Tag type | Starter values | ✏️ Your values |
|---|---|---|
| **Source** | email, chat, social, review, survey, call | |
| **Phase** | build, internal-test, beta, launch, customers-1-10, 11-100, 101-250, 251-500 | |
| **Product area** | login, onboarding, dashboard, payments, settings, (add your own) | |
| **Customer plan** | free, pro, business | |
| **Feeling** | happy, neutral, frustrated, angry | |
| **Platform** | iOS, Android, web, other | |
| **Needs** | needs-info, needs-engineer, needs-approval | |

**Q5.3 Tag naming rule.** Use lowercase words joined with dashes, like `product-area:payments`. Do you agree?
- [ ] Yes
- [ ] No, we will use: ______

⚠️ **Do not make more than one category per ticket.** Use tags for extra details.

---

# PART 6. URGENCY: SEVERITY AND PRIORITY

**Why:** Two different ideas are often mixed up:

- **Severity = how bad is the problem?** (how much it breaks the product)
- **Priority = how fast must we act?** (severity plus customer type, deadlines and mood)

Example: A spelling mistake on the home page is *low severity*, but if the CEO's biggest customer is about to sign up, the fix may be *high priority*.

💡 **Keep it simple:** use **4 levels only**. Too many levels confuse everyone.

**Severity scale (used on the Ticket Card).** Rate *how broken it is*, before thinking about customer type or mood:

| Severity | Plain meaning | ✏️ Your own example |
|---|---|---|
| **S1** | Product down or unusable, or data, money or safety at risk | |
| **S2** | A main feature is broken, no good workaround | |
| **S3** | Partly broken or annoying, a workaround exists | |
| **S4** | Cosmetic, a question, or an idea | |

*Start with S1 = P0, S2 = P1, S3 = P2, S4 = P3, then apply the boosts and drops in Q6.4 and Q6.5 to get the final priority.*

**Q6.1 Review and edit the 4 priority levels.** Replace the grey example times with your real promises. Write in plain words so a customer would understand them too.

| Level | Name | Plain meaning | Examples | ✏️ First reply within | ✏️ Fix or plan within | 👤 Who is alerted |
|---|---|---|---|---|---|---|
| **P0** | **Emergency** | Product is down or unusable for many people, money or data is at risk, or safety is at risk | Nobody can log in; payments charge twice; personal data exposed | e.g. 30 minutes, 24/7 | e.g. same day, updates every 2 hours | |
| **P1** | **Urgent** | A main feature is broken for some people, no good workaround | Invoices will not send for the Pro plan; app crashes on one phone model | e.g. 2 working hours | e.g. 2 working days | |
| **P2** | **Normal** | Something is annoying or partly broken, a workaround exists | Button misaligned; slow report; export missing a column | e.g. 1 working day | e.g. next planned release | |
| **P3** | **Low** | Question, idea, praise, small wish | "Can you add dark mode?"; "How do I change my photo?" | e.g. 2 working days | Reviewed in the weekly meeting (Part 11) | |

✏️ **Edit the table above directly**, then answer:

**Q6.2 In your own words, finish this sentence for P0:** "We treat something as an emergency when ______."
✏️

**Q6.3 Which messages are ALWAYS at least P1, whatever else is true?** (tick all that apply, add your own)
- [ ] Anything about a possible data leak or hacking (**always P0**)
- [ ] Customer was charged wrongly
- [ ] Customer cannot log in at all
- [ ] Anything touching safety
- [ ] Anything touching children's data
- [ ] Legal threat or official request
- [ ] Add your own: ______

**Q6.4 "Boosts": what moves a ticket UP one level?** (tick all that apply)
- [ ] 3 or more customers report the same problem within 24 hours
- [ ] Customer is on the highest plan: ______
- [ ] Customer is a beta partner or one of the first 100 customers
- [ ] Customer is very upset, mentions leaving, a competitor, or the press
- [ ] A contract or renewal is within 30 days
- [ ] The issue is on the "biggest promise" from Q1.7
- [ ] Add your own: ______

**Q6.5 What moves a ticket DOWN one level?** (tick all that apply)
- [ ] A good, easy workaround exists
- [ ] Only one person is affected, and it is cosmetic
- [ ] Customer says it is not urgent
- [ ] Add your own: ______

**Q6.6 Who has the final say if the AI and a human disagree on priority?**
✏️ (Recommended: the human Triage Owner.)

**Q6.7 How often will you re-check these definitions?**
*Why:* They go out of date as you grow.
✏️ (Recommended: at every phase change in Part 10, and every 3 months.)

---

# PART 7. THE TRIAGE STEPS AND THE TICKET CARD

**Why:** Everyone (and every AI) should follow the same six steps, in the same order, every time.

## The 6 steps

| Step | Name | What to do | Done by |
|---|---|---|---|
| 1 | **Receive** | Message arrives at the "home" (Q3.1). Send the auto-reply. | Automatic |
| 2 | **Understand** | Read it. What is the customer trying to do? What went wrong? | 🤖 draft, 👤 confirm |
| 3 | **Label** | Choose one **category** (Part 5) and add **tags**. Look for duplicates. | 🤖 draft, 👤 confirm |
| 4 | **Rate** | Choose **severity and priority** (Part 6). Apply boosts. | 🤖 suggest, 👤 decide |
| 5 | **Route** | Send to the right owner. Escalate if a trigger in Part 8 applies. | 👤 |
| 6 | **Reply and log** | Send a reply (Part 9). Record what happened. Keep the ticket open until fixed. | 👤 approves |

**Q7.1 Do these 6 steps fit how you work?**
- [ ] Yes, as written
- [ ] With changes: ______

**Q7.2 What does "done" mean for a ticket?** (tick all that must be true)
- [ ] The customer got an answer or a fix
- [ ] The customer confirmed it works, or we waited ______ days with no reply
- [ ] The cause is written down
- [ ] If it was a bug or idea, it is linked to a roadmap item (Part 11)
- [ ] Add your own: ______

**Q7.3 How long do you wait before reminding a customer who has not replied?**
✏️ (Example: remind after 3 days, close after 7.)

## The Ticket Card (copy this for every ticket, or build it into your tool)

```
TICKET ID:
DATE / TIME RECEIVED:
CHANNEL:                 (email / chat / social / review / survey / other)
CUSTOMER (name or ID):
CUSTOMER PLAN:
PHASE:                   (build / internal-test / beta / launch / 1-10 / 11-100 / 101-250 / 251-500)

WHAT THE CUSTOMER SAID (1-3 sentences, their words):
WHAT THEY ARE TRYING TO DO:
WHAT WENT WRONG:
STEPS TO MAKE IT HAPPEN AGAIN:
DEVICE / BROWSER / APP VERSION:
SCREENSHOT OR LINK:

CATEGORY (one):
TAGS:
SEVERITY (S1-S4):        PRIORITY (P0-P3):
WHY THIS PRIORITY (one line):
BOOSTS APPLIED:

DUPLICATE OF TICKET:
OWNER:
NEXT STEP AND DATE:
ESCALATED TO:            (name + time)
AI INVOLVED? (Y/N):      HUMAN WHO APPROVED:

FIRST REPLY SENT AT:
RESOLVED AT:
CUSTOMER MOOD AT END:    (happy / neutral / unhappy)
LINKED ROADMAP ITEM:
```

**Q7.4 Do you want to add or remove any fields from the Ticket Card?**
✏️

---

# PART 8. ESCALATION: WHEN TO ASK FOR HELP

**Why:** Escalation is the "ladder" you climb when the problem is bigger than the person holding it. Customers lose trust when nobody takes over and they must repeat themselves.

**Q8.1 Fill in the escalation ladder.**

| Rung | Who | ✏️ Name | ✏️ Climb to the next rung when… |
|---|---|---|---|
| 1 | AI helper | | It is unsure, or a trigger from Q4.4 appears |
| 2 | Support Responder | | |
| 3 | Triage Owner | | |
| 4 | Engineering Contact or Product Owner | | |
| 5 | Executive Sponsor | | |

*Example "climb when":* "P0 not acknowledged by engineering in 15 minutes", "P1 not fixed in 1 working day."

**Q8.2 Who owns each special case?** (a name is required for each)

| Special case | ✏️ Owner | ✏️ First action | ✏️ Deadline |
|---|---|---|---|
| Possible data leak or hacking | | | |
| "Delete my data" or other privacy request | | | |
| Legal letter, police or official request | | | |
| Safety concern (someone could be hurt) | | | |
| Payment error or refund over ______ | | | |
| Angry customer or public complaint (social media, reviews) | | | |
| Journalist or press question | | | |
| Message that threatens harm (customer or others) | | | |

⚠️ For safety or threat messages: a **human must read the message immediately**. The AI must not reply alone.

**Q8.3 When you hand a ticket over, what must be written so the customer never repeats themselves?** (tick all; these are our recommended "handoff pack")
- [x] The customer's full message and history
- [x] What was already tried
- [x] Category, priority, and why
- [x] Customer plan and mood
- [x] The promise made to the customer and the deadline
- [ ] Add your own: ______

**Q8.4 How do we alert people?** (tick all that apply)
- [ ] Phone call (P0 only)
- [ ] Text message
- [ ] Chat message in channel: ______
- [ ] Email
- [ ] Other: ______

**Q8.5 During a P0, how often do we update the customer?**
✏️ (Example: every 2 hours until fixed, then a final "all clear" message.)

**Q8.6 After a P0 or P1 is fixed, do you write a short "what happened and how we prevent it" note?**
- [ ] Yes, within ______ days, saved at: ______
- [ ] No (⚠️ we recommend yes; it is where the best learning is)

---

# PART 9. REPLY TEMPLATES

**Why:** Good replies are *fast, kind, clear and honest*. Templates save time but must be personalised.

**Q9.1 Choose your voice.**
- [ ] Friendly and casual
- [ ] Warm and professional
- [ ] Formal
✏️ Words we always use: ______ Words we never use: ______

**Q9.2 Fix the example templates so they sound like you.** Replace the `<…>` blanks when sending.

**Template A. "We got it" (first reply)**
> Hi <name>, thanks for telling us. I understand you're trying to <what they want>, and <what went wrong>. I'm looking into it now and will update you by <time/date>.

**Template B. "We need more information"**
> Hi <name>, to help quickly, could you tell me: 1) <question 1>, 2) <question 2>? A screenshot helps too. Thank you!

**Template C. "Confirmed bug"**
> Hi <name>, you were right, this is a problem on our side. We're working on it. I'll update you by <date>. Meanwhile, you can <workaround, if any>.

**Template D. "Thanks for the idea"**
> Hi <name>, thank you for this suggestion. I've added it to our ideas list. I can't promise a date, but I will tell you if we decide to build it.

**Template E. "Fixed"**
> Hi <name>, good news: <what was fixed>. Could you try again and tell me if it works for you?

**Template F. "Apology"**
> Hi <name>, I'm sorry about <what happened>. That's not the experience we want you to have. Here's what we're doing: <action>.

**Template G. "Handing over to a person"**
> Hi <name>, I'm bringing in <person's name> from our team. They have all the details, so you don't need to repeat anything.

**Q9.3 Write 1 extra template you will need often.**
✏️

**Q9.4 Reply rules** (recommended are pre-ticked)
- [x] Always use the customer's name
- [x] Say what we know, what we don't, and when we'll update next
- [x] Never promise a date unless an engineer confirmed it
- [x] Thank customers for bad news; it helps us improve
- [x] Use simple words; no technical jargon
- [ ] Add your own: ______

---

# PART 10. LIFE-CYCLE PHASES: BUILD TO FIRST 500 CUSTOMERS

**Why:** What you need from support at day 1 of building is not what you need at customer 400. Fill in **one block per phase**. At the end of each phase, finish the **exit checklist** before moving on, and re-read Parts 5, 6 and 8.

**Phase map**

```
 PHASE 1      PHASE 2          PHASE 3     PHASE 4      PHASE 5 (customers 1 to 500)
 BUILD  -->   INTERNAL   -->   BETA   -->  LAUNCH  -->  1-10 --> 11-100 --> 101-250 --> 251-500
              TEST                         WEEK
```

## PHASE 1. BUILD (no outside users yet)

**Goal:** Be ready to hear customers before the first one arrives.

**Q10.1.1 Who are your first 5 to 10 target customers (real people, not types)?**
✏️

**Q10.1.2 What are the 3 questions you want early users to answer?**
*Example:* "What were you trying to do? What got in your way? What would you pay for?"
✏️

**Q10.1.3 Where will "pre-launch" feedback be kept (interviews, prototype tests, waiting list)?**
✏️

**Q10.1.4 Is the feedback "home" (Q3.1) ready and tested?** (send a test message, see if it arrives)
- [ ] Yes, tested on: ______
- [ ] No

**Q10.1.5 Has the AI been tested on 20 pretend messages (mix of easy, hard, angry, risky)?**
- [ ] Yes. Wrong or unsafe answers found: ______  How many: ______
- [ ] No

**Q10.1.6 Does the product have an in-app way to send feedback or a bug report?**
- [ ] Yes   - [ ] Planned for: ______

**Exit checklist, Phase 1** (all must be ticked before Phase 2)
- [ ] Parts 0 to 9 completed (no empty boxes; `TBD` has owner and date)
- [ ] Triage Owner and Backup named and know their job
- [ ] Ticket Card tested once with a pretend ticket
- [ ] Kill switch for AI tested (Q4.9)
- [ ] Phase 1 date signed off: ______

## PHASE 2. INTERNAL TEST (only your own team uses it)

**Goal:** Find problems before outsiders do, and practise triage using friendly, safe users.

**Q10.2.1 Who is testing and for how many days?**
✏️

**Q10.2.2 How do testers report problems?** (must use the real Ticket Card)
✏️

**Q10.2.3 Is the team actually using the severity levels? Do 3 testers agree on priority for the same 5 sample problems?**
- [ ] Yes, they agree on ______ of 5
- [ ] No. Fix the wording in Part 6

**Q10.2.4 Which P0 and P1 problems must be fixed BEFORE any outside person sees the product?**
✏️ (This list becomes your "launch blockers".)

**Q10.2.5 Do the answers for "How-to questions" exist yet (help page, FAQ)?**
- [ ] Yes, at: ______   - [ ] Not yet

**Exit checklist, Phase 2**
- [ ] At least ______ test tickets triaged end to end
- [ ] No unresolved P0 or P1 launch blockers
- [ ] Reply templates (Part 9) edited after real use
- [ ] AI mistakes reviewed and rules in Part 4 updated
- [ ] Phase 2 date signed off: ______

## PHASE 3. BETA (small invited group)

**Goal:** Learn from real customers who forgive rough edges. **Treat beta users as partners.**

**Q10.3.1 How many beta users, and how were they chosen?**
✏️

**Q10.3.2 How do we thank beta users and keep them involved?**
*Example:* "Weekly short email, a private chat group, a free year at launch."
✏️

**Q10.3.3 Will we call or meet each beta user once?**
*Why:* In the early days, a 15-minute conversation can teach more than 100 survey answers.
- [ ] Yes, each beta user, within ______ days of joining
- [ ] Only some: ______

**Q10.3.4 Beta triage rules: is anything handled differently from Part 6?**
*Example:* "Every beta bug report gets a reply the same day; everything is at least P2."
✏️

**Q10.3.5 What do we tell beta users we will do with their feedback?**
✏️

**Q10.3.6 What is the "go / no-go" rule to leave beta?**
*Example:* "Zero open P0, no more than 2 open P1, 8 of 10 testers say they would recommend us."
✏️

**Exit checklist, Phase 3**
- [ ] Every beta ticket is closed or linked to a roadmap item
- [ ] Top 5 recurring problems written in Part 12 and decided on
- [ ] Beta users told what changed because of them
- [ ] Go / no-go rule (Q10.3.6) met
- [ ] Phase 3 date signed off: ______

## PHASE 4. LAUNCH WEEK (first public days)

**Goal:** Stay calm when volume and attention spike.

**Q10.4.1 Who is on watch, hour by hour, in launch week?**
✏️ (Make a simple schedule: name, day, hours.)

**Q10.4.2 How many messages per day will be too many for us to handle?**
✏️ Number: ______   What we do when it is passed (Part 14): ______

**Q10.4.3 Where will launch-day public comments be watched (social, app stores, communities)?**
✏️

**Q10.4.4 Is there a short public "status" or "known issues" page or post?**
- [ ] Yes at: ______   - [ ] No, we'll post updates in: ______

**Q10.4.5 Daily 10-minute launch check-in: who attends and when?**
✏️

**Q10.4.6 Is a quick rollback or pause available if something big breaks?**
- [ ] Yes. Who decides: ______  How: ______
- [ ] No (⚠️ write what you will do instead)

**Exit checklist, Phase 4**
- [ ] All P0 and P1 from launch week fixed or have a dated plan
- [ ] No ticket waiting longer than its promised time for more than ______ hours
- [ ] Launch learnings written in Part 11
- [ ] Phase 4 date signed off: ______

## PHASE 5. CUSTOMERS 1 TO 500 (four stages)

💡 Use the same questions at each stage. Answer **once per stage** by copying the block. The table below tells you what usually changes.

| Stage | Customers | Typical focus | What usually changes |
|---|---|---|---|
| 5A | 1 to 10 | Talk to every customer personally | Founders reply to many messages themselves |
| 5B | 11 to 100 | Find the repeating problems | Tags and counts become useful |
| 5C | 101 to 250 | Make support repeatable | Saved answers, help pages, and clear owners matter |
| 5D | 251 to 500 | Prepare to scale beyond 500 | Automation, trend reports, and capacity planning |

**Fill in this block for each stage (5A, 5B, 5C, 5D):**

| Question | ✏️ 5A (1-10) | ✏️ 5B (11-100) | ✏️ 5C (101-250) | ✏️ 5D (251-500) |
|---|---|---|---|---|
| Who reads every message? | | | | |
| Do we personally contact each new customer? (Y/N, how) | | | | |
| Expected messages per day | | | | |
| P0 promise (first reply) | | | | |
| P1 promise (first reply) | | | | |
| Can AI reply alone to any topics? Which? | | | | |
| Main feedback sources this stage | | | | |
| What we want to learn most this stage | | | | |
| What we will stop doing by hand | | | | |
| Date we reached the end of this stage | | | | |

**Exit checklist, each stage**
- [ ] Customer count reached: 10 / 100 / 250 / 500 (circle one)
- [ ] Milestone row in Part 12 filled in
- [ ] Top 5 recurring issues reviewed and decided on
- [ ] Customer satisfaction measured (Part 12)
- [ ] Rules in Parts 4, 6, 8 re-read and updated
- [ ] Stage date signed off: ______

**Final exit, customer 500 reached**
- [ ] Summary of what we learned written in Part 12
- [ ] Decision made: what changes in support at "the next level" (more people? more automation? new tools?)
✏️

---

# PART 11. FEEDBACK TO PRODUCT IMPROVEMENT LOOP

**Why:** Support is not only about fixing today's problem. Every message is a clue about how to make the product better. But a loop that sends *everything* to the roadmap makes a product that tries to please everyone. **You decide what to learn from and what to politely decline.**

## The 6-step loop

```
1 COLLECT  ->  2 GROUP  ->  3 SCORE  ->  4 DECIDE  ->  5 BUILD  ->  6 TELL CUSTOMERS
   ^                                                                         |
   +-------------------------------------------------------------------------+
```

**Q11.1 Who is the "Feedback Keeper" (the person who looks after steps 1 to 4 every week)?**
✏️ Name: ______ Backup: ______

**Q11.2 Where is feedback grouped?** (one place only)
*Example:* "Notion board 'Feedback' with columns: New, Grouped, Scored, Decided."
✏️

**Q11.3 How are similar messages grouped?**
*Example:* "AI suggests a group name; the Feedback Keeper confirms. One 'theme' = one problem or one wish."
✏️

**Q11.4 How do we score each theme?** The starter formula is below. Edit if you like.

| Question | Score 1 (low) to 5 (high) |
|---|---|
| **How many customers asked?** | |
| **How painful is it** for them? | |
| **How important** is it to our biggest promise (Q1.7)? | |
| **How much effort** to build? (reverse: 5 = small effort) | |

*Theme score = add the four numbers. Highest first.* ✏️ Do you want to change this?

**Q11.5 Every roadmap item must point back to the customer feedback that caused it.**
*Example:* "Roadmap item 'Export to PDF' links to tickets #41, #77, #102 (3 customers)."
✏️ How will you link them?

**Q11.6 The decision rules.** For each theme, we choose exactly one:
- **Do now:** fix or build soon
- **Plan:** on the roadmap with a quarter or month
- **Park:** good idea, not now (review again in ______ months)
- **Decline:** not a fit (we kindly tell the customer why)

✏️ Who makes the final decision? ______

**Q11.7 Weekly feedback meeting.**

| Question | ✏️ Your answer |
|---|---|
| Day and time | |
| How long (recommended 30 minutes) | |
| Who must attend (Product Owner, Feedback Keeper, Engineering Contact, Support Responder) | |
| Standard agenda | *Recommended: 1) top 5 recurring issues 2) new P0/P1 learnings 3) scores and decisions 4) customers to update* |
| Where notes are kept | |

**Q11.8 How do we "close the loop"?** Tell customers when we acted on their feedback.
*Why:* Customers who see their ideas used become your best fans, and tell others.
- [ ] Personal message to each customer who asked
- [ ] "What's new" or changelog page at: ______
- [ ] In-app announcement
- [ ] Public roadmap at: ______
- [ ] Other: ______

**Template: "We built it"**
> Hi <name>, you asked for <idea>. We've just released it: <what it does>. Thank you for helping us improve. I'd love to hear what you think.

**Q11.9 What do we promise customers about their ideas?**
*Example:* "We read every one. We can't build everything. We'll tell you either way."
✏️

**Q11.10 Special channels for deeper learning.** Which will you use?
- [ ] 15-minute customer calls when someone joins, hits a milestone, or goes quiet for 2 weeks
- [ ] Short in-app surveys at key moments
- [ ] NPS or CSAT survey (see Part 12)
- [ ] Customer advisory group of 5 to 10 people
- [ ] Other: ______

---

# PART 12. MEASURING SUCCESS AND MILESTONE TRACKER

**Why:** If you cannot see it, you cannot improve it. Keep to a few numbers you will actually read. **Review them in the weekly meeting (Part 11).**

## 12A. The numbers we track

**Q12.1 Fill in your targets. Update "Actual" each review.**

| Measure | Plain meaning | ✏️ Target | ✏️ Actual (latest) | How measured / by whom |
|---|---|---|---|---|
| **First reply time** (by priority) | How long a customer waits for the first answer | P0: ___ P1: ___ P2: ___ P3: ___ | | |
| **Resolution time** (by priority) | How long until it's really fixed | P0: ___ P1: ___ P2: ___ P3: ___ | | |
| **Tickets answered on time** | % that met the promise in Part 6 | ____ % | | |
| **Time to reach a human** | How long after a customer asks for a person | ____ min | | |
| **Customer satisfaction (CSAT)** | "How happy were you with this help?" (1 to 5) | ____ out of 5 | | |
| **Recommend score (NPS)** *(optional)* | "How likely are you to recommend us?" (0 to 10) | | | |
| **Reopened tickets** | % of tickets customers had to reopen | below ____ % | | |
| **AI sorted correctly** | % of AI categories/priorities humans agreed with | ____ % | | |
| **AI replies needing big edits** | % of AI drafts a human rewrote | below ____ % | | |

**Q12.2 How and when do we ask for satisfaction?**
*Example:* "A one-click thumbs up or down at the bottom of every resolved reply; NPS survey once at day 14."
✏️

## 12B. Top recurring issues (update every week)

**Why:** The same problem repeated by many customers is the clearest signal of what to fix first.

| Rank | ✏️ Issue (plain words) | ✏️ Category | ✏️ How many tickets (this month) | ✏️ Decision (Do now / Plan / Park / Decline) | ✏️ Owner | ✏️ Linked roadmap item |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

## 12C. Customer milestone tracker

**Fill in a row the day you reach each customer count.**

| Milestone | ✏️ Date reached | ✏️ Tickets so far | ✏️ Avg first reply | ✏️ CSAT | ✏️ #1 recurring issue | ✏️ Biggest lesson | ✏️ One thing we will change |
|---|---|---|---|---|---|---|---|
| Customer 1 | | | | | | | |
| Customer 10 | | | | | | | |
| Customer 50 | | | | | | | |
| Customer 100 | | | | | | | |
| Customer 250 | | | | | | | |
| Customer 500 | | | | | | | |

**Q12.3 What does "this is working" look like at customer 500?** (write 3 measurable sentences)
*Example:* "9 of 10 P1 tickets answered in 2 hours. CSAT 4.5 or higher. Top 3 repeating issues from month 1 are fixed."
✏️

---

# PART 13. REVIEW RHYTHM

**Why:** A document nobody revisits becomes wrong. Put a rhythm in the calendar.

| How often | What we check | ✏️ Who | ✏️ When (day and time) |
|---|---|---|---|
| **Every day** (10 min) | Any untriaged or overdue tickets? Any P0 or P1 open? | | |
| **Every week** (30 min) | Top 5 recurring issues, scores, decisions, AI mistakes (Part 11) | | |
| **Every month** (60 min) | Metrics in Part 12; are targets being met? Are categories right? | | |
| **Every 3 months** (90 min) | Re-read this whole document. Update severity rules and escalation names. | | |
| **At every phase change** | Phase exit checklist in Part 10 | | |

**Q13.1 Who has the job of keeping this document up to date?**
✏️

**Q13.2 Where is the latest copy stored, and how does everybody find it?**
✏️

---

# PART 14. "WHAT IF…" EMERGENCY PLANS

**Why:** The best time to decide is *before* the bad day. Write a one-line plan for each.

| What if… | ✏️ Who decides | ✏️ What we do first | ✏️ What we tell customers |
|---|---|---|---|
| …messages suddenly triple (launch, press, viral post) | | | |
| …our helpdesk or inbox stops working | | | |
| …the AI sends a wrong or harmful reply | *(use kill switch, Q4.9)* | | |
| …a wave of 1-star reviews arrives | | | |
| …a customer posts publicly that we leaked their data | | | |
| …the whole product is down | | | |
| …the Triage Owner suddenly leaves or is unreachable | | | |
| …a customer is abusive to our team | | | |
| …we receive a message that suggests someone may be in danger | *(human reads immediately; Part 8)* | | |

---

# PART 15. FINAL CHECKLIST AND SIGN-OFF

**Before you call this document "ready", tick every box.**

**Completeness**
- [ ] Every question has an answer, `N/A because…`, or `TBD | Owner | Date`
- [ ] No placeholder text like `<name>` or `______` is left in the sections you use
- [ ] All people in Part 2 have a name **and** a backup
- [ ] Phone numbers or chat handles in Part 2 have been checked

**Clarity**
- [ ] A new teammate could read Parts 5 to 8 and triage a ticket without asking anyone
- [ ] Priority levels (P0 to P3) have real times, not "ASAP"
- [ ] Someone who is not on the team (or a 10-year-old) understood the Part 6 examples

**Safety**
- [ ] AI "never do" list (Q4.3) and handoff triggers (Q4.4) reviewed by a human
- [ ] Kill switch tested
- [ ] Security, privacy, legal and safety owners are named (Q8.2)

**Learning loop**
- [ ] Weekly feedback meeting is in calendars
- [ ] Feedback Keeper is named
- [ ] Ways to tell customers what we built (Q11.8) are ready

**Test it**
- [ ] We tested the Ticket Card with 3 pretend tickets: one easy, one angry, one risky
- [ ] We tested one pretend P0 end to end, including the alert and customer update

**Sign-off**

| Role | ✏️ Name | ✏️ Date | ✏️ Signature or "Approved in chat" |
|---|---|---|---|
| Document owner | | | |
| Triage Owner | | | |
| Product Owner | | | |
| Executive Sponsor | | | |

---

# APPENDIX A. GLOSSARY (PLAIN WORDS)

| Word | Meaning |
|---|---|
| **Triage** | Sorting messages by how urgent they are |
| **Ticket** | One customer message (or one problem), tracked until it's solved |
| **Severity** | How badly something is broken |
| **Priority** | How fast we must act |
| **P0, P1, P2, P3** | Priority levels. P0 is the most urgent |
| **Escalate** | Pass a problem to someone with more power or skill |
| **Triage Owner** | The person responsible for sorting and speed |
| **Approver** | The person who must say "OK" before something risky goes out |
| **Workaround** | A temporary way around a problem |
| **Bug** | Something that does not work as it should |
| **Feature request** | A customer asking for something new |
| **Roadmap** | The list of things we plan to build and when |
| **Beta** | A trial with a small invited group before everyone |
| **CSAT** | A "how happy were you?" score |
| **NPS** | A "would you recommend us?" score from 0 to 10 |
| **Duplicate** | A ticket about a problem we already have |
| **Backup** | The person who takes over when the main person is away |
| **Kill switch** | A way to switch something off immediately |
| **Human-in-the-loop** | A person checks or approves what the AI does |
| **Handoff** | Passing a ticket to another person, with all the details |
| **Changelog** | A public list of "what's new or fixed" |
| **Recurring issue** | The same problem reported again and again |
| **TBD** | "To be decided": allowed only with an owner and a date |

---

# APPENDIX B. RESEARCH BASIS

This template combines widely used practices from support, product and AI-governance writing. Each design choice and its reason:

| Design choice in this template | Reason (summarised from public guidance) |
|---|---|
| Only 4 priority levels (Part 6) | Guides on triage warn that too many levels confuse teams; 3 to 4 is the recommended maximum. |
| Severity separated from priority | Severity measures the effect on the product; priority measures urgency for users and the business. They are often different. |
| Plain-language names and examples for each level | Vague words like "High/Medium/Low" or "Level 2" confuse customers and staff. Specific criteria help both. |
| Boosts for customer type, mood, repeat reports and deadlines | Customer tier, frustration signals, and contract timing are common reasons to raise priority beyond the technical issue. |
| Re-checking definitions regularly (Part 13) | Teams are advised to revisit priority matrices roughly quarterly. |
| Human approves AI work; clear triggers; kill switch; named accountable person (Part 4, 8) | 2026 guidance on AI in support stresses guardrails, defined escalation paths, visible human options, and clear ownership when AI errs. |
| Full-context handoff (Q8.3) | Escalation often fails when customers must repeat themselves. |
| Feedback in one home, grouped, scored, linked to roadmap items, then reported back to customers (Part 11) | Early-stage feedback-loop guidance recommends one central place, explicit links from roadmap to feedback, and closing the loop with customers. |
| Personal calls and heavy human contact for the first customers (Phases 3 and 5A) | Guidance for products under about 500 customers favours low-tech, high-signal methods such as short calls over big surveys. |
| Not routing every request to the roadmap (Q11.6 "Park / Decline") | A loop that builds everything asked for becomes a feature factory rather than a product strategy. |

**Sources consulted (October 2026):**
- TeamSupport, "5 Tips for Defining Support Ticket Severity": https://www.teamsupport.com/blog/5-tips-for-defining-support-ticket-severity
- The CTO Club, "Ticket Prioritization Strategies for Customer Support Teams": https://thectoclub.com/it-service-management/ticket-prioritization-strategies-for-customer-support-teams/
- Halo Agents, "How to Build a Better Triage System for Your Support Team": https://haloagents.ai/blog/support-team-needs-better-triage-system
- Halo Agents, "7 Strategies to Overcome Support Ticket Prioritization Challenges": https://haloagents.ai/blog/support-ticket-prioritization-challenges
- Plane, "What is issue triage? Process and priority levels": https://plane.so/blog/what-is-issue-triage-process-and-priority-levels
- Startup Fortune, "Build a SaaS Customer Feedback Loop That Actually Moves Your Roadmap": https://startupfortune.com/build-a-saas-customer-feedback-loop-that-actually-moves-your-roadmap/
- Pendo, "How to Implement Customer Feedback into Your Product Roadmap": https://www.pendo.io/pendo-blog/how-to-implement-customer-feedback-into-your-product-roadmap/
- Indie Hackers, "How early-stage startups can build a strong customer feedback loop": https://www.indiehackers.com/post/how-early-stage-startups-can-build-a-strong-customer-feedback-loop-04c3dc0a97
- CX Today, "Is Your AI Escalation Strategy Breaking Customer Trust?" (April 2026): https://www.cxtoday.com/contact-center/is-your-ai-escalation-strategy-breaking-customer-trust/
- DesignRush, "3 Critical Limits of AI in Customer Support" (2026): https://news.designrush.com/3-ai-limits-customer-support-must-plan-2026
- Cogent, "AI's Next Act: 4 AI Trends That Will Redefine 2026": https://cogentinfo.com/resources/ais-next-act-4-ai-trends-that-will-redefine-2026

---

*End of document. Remember: an honest `TBD | Owner | Date` is better than a confident guess.*
