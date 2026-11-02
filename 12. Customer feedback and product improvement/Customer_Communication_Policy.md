---
# ============================================================
# MACHINE-READABLE VARIABLES (for AI agents and scripts)
# Fill these in FIRST. Humans: just replace the text after the colon.
# AI agents: read these values and use them whenever you see {{variable_name}} in this document.
# ============================================================
template_name: "Customer Communication Policy"
template_version: "1.0"
folder: "Customer feedback and product improvement"
file_name: "Customer_Communication_Policy.md"

product_name: "{{FILL_IN}}"            # Example: "PlantPal"
product_type: "{{FILL_IN}}"            # Choose one: web-saas | mobile-app | both
product_one_line: "{{FILL_IN}}"        # Example: "An app that reminds you when to water your plants"
policy_owner_name: "{{FILL_IN}}"       # Example: "Sam Rivera"
policy_owner_contact: "{{FILL_IN}}"    # Example: "sam@plantpal.com"
support_email: "{{FILL_IN}}"           # Example: "help@plantpal.com"
status_page_url: "{{FILL_IN_OR_NONE}}" # Example: "https://status.plantpal.com"
community_url: "{{FILL_IN_OR_NONE}}"   # Example: "https://discord.gg/plantpal"
main_language: "{{FILL_IN}}"           # Example: "English"
main_time_zone: "{{FILL_IN}}"          # Example: "America/New_York"
support_hours: "{{FILL_IN}}"           # Example: "Mon-Fri, 9:00-17:00"
ai_autonomy_level: "draft-human-approves"  # DO NOT CHANGE unless you rewrite Part 7
current_phase: "{{FILL_IN}}"           # Choose one: 1-build | 2-private-beta | 3-launch | 4-first-100 | 5-customers-101-500
policy_status: "draft"                 # draft | approved | retired
last_reviewed: "{{YYYY-MM-DD}}"
---

# How to Fill This Document

> **Read this whole box first. It takes 2 minutes.**

## What is this document?

This is a **Customer Communication Policy**. It is a single page-set that answers one big question:

> **"When we talk to our customers, who says what, when, how, and in what voice?"**

It covers the whole life of your product, from the first day you build it until your **first 500 customers** are using it. It is written for software products (websites, web apps, mobile apps) built with the help of AI tools.

## Who is this for?

Anyone. If you can read and write, you can fill this in. You do **not** need to be a lawyer, writer, or engineer. A solo founder can finish the Quick Start in about **15 minutes** and the full document in about **2-3 hours**.

## The 5 rules of filling this in

1. **Answer every question.** Do not skip. If you truly do not know, write `TBD — owner: [name] — by: [date]`. Never leave a blank and never guess silently.
2. **Replace everything that looks like `[FILL IN: ...]`.** When you are done, no `[FILL IN` should remain anywhere in the file. (Search for the word `FILL` to check.)
3. **Use the examples as a guide, not as the answer.** Lines that start with `> Example:` show what a good answer looks like. Copy the style, not the words.
4. **Keep sentences short.** One idea per sentence. If a 10-year-old could not understand it, rewrite it.
5. **Use numbers, not feelings.** Write "within 4 hours", not "quickly". Write "every Friday", not "regularly".

## What the symbols mean

| Symbol | Meaning |
|---|---|
| `[FILL IN: ...]` | You must type your own answer here. |
| `> Example:` | A sample answer. Do not copy blindly. |
| `> Tip:` | A helpful hint. |
| `> Warning:` | A common trap. Read carefully. |
| `- [ ]` | A checkbox. Change `[ ]` to `[x]` when done or chosen. |
| `{{variable}}` | A value from the top of this file. Replace it, or let your AI agent do it. |
| ⭐ | A **Quick Start** question. Answer these first. |
| 🔒 | A **safety rule**. Do not delete or weaken it. |

## Suggested order

1. Fill in the **variables at the very top** of this file.
2. Answer the **10 Quick Start questions** (right below). This gives you a working "minimum policy".
3. Go through **Parts 1-14** in order. Skip nothing, but you may write short answers.
4. Finish with **Part 15 (Checklist)** and **Part 16 (Sign-off)**.
5. Re-read **Part 17 (Common Mistakes)** before you launch.
6. Unknown word? Look in **Part 18 (Glossary)**.

## Using this template for many projects

- **Copy this file** into each new project's `Customer feedback and product improvement` folder. Never edit the master copy.
- Fill in the top variables and answer every question again for each project.
- Keep the file name exactly `Customer_Communication_Policy.md` so people and AI agents can always find it.
- Save a new row in **Part 16 (Version History)** every time you change the file.

> **Not legal advice.** This template gives general good-practice guidance. The privacy and legal parts (Part 11) are reminders, not legal advice. If your product handles children's data, payments, health data, or customers in regulated places, ask a qualified professional to check them.

---

# ⭐ Quick Start: 10 Must-Answer Questions

> Answer these 10 and you already have a **minimum working policy**. Everything after this makes it stronger.

### ⭐ Q1. What is your product, in one sentence?
[FILL IN: ]
> Example: "PlantPal is a mobile app that reminds people when to water their plants."

### ⭐ Q2. Who is allowed to speak to customers on behalf of the product?
[FILL IN: names or roles]
> Example: "Only Sam (founder). The AI assistant may write drafts, but Sam sends them."

### ⭐ Q3. Where can customers contact you? (tick all that apply and add the address)
- [ ] Email → [FILL IN: address]
- [ ] In-app chat or help button → [FILL IN: where it appears]
- [ ] Community or social (Discord, Slack, Reddit, X, etc.) → [FILL IN: link]
- [ ] Phone or video call → [FILL IN: how to book]

### ⭐ Q4. What is the longest a customer should wait for a first human reply?
[FILL IN: a number of hours, plus working days or every day]
> Example: "1 business day (24 hours on weekdays) for normal questions."

### ⭐ Q5. What counts as an emergency (a "Critical" problem)?
[FILL IN: 2-3 situations]
> Example: "Nobody can log in. Customer data is wrong or exposed. Customers are being charged incorrectly."

### ⭐ Q6. How fast will you reply to an emergency?
[FILL IN: a number of minutes or hours]
> Example: "Within 1 hour, every day of the week."

### ⭐ Q7. How should your replies sound? Pick 3 words.
[FILL IN: three words]
> Example: "Friendly, clear, honest."

### ⭐ Q8. Where will you tell customers when something is broken?
[FILL IN: status page link, email, in-app banner, etc.]
> Example: "A banner inside the app and a post on status.plantpal.com."

### ⭐ Q9. Where will all feedback be collected in one place?
[FILL IN: tool or document name and link]
> Example: "One spreadsheet called 'Feedback Log' in Google Sheets."

### ⭐ Q10. What will AI be allowed to do with customer messages? 🔒
- [x] AI may **draft** replies, summarize feedback, and suggest tags.
- [x] A **human must read and approve** every message before a customer sees it.
- [ ] AI may send messages alone. (Not allowed in this template. See Part 7.)

---

# Part 1: About This Policy

### 1.1 Why does this policy exist?
[FILL IN: 1-3 sentences]
> Example: "So every customer gets a clear, kind, and fast answer, and so we learn from what customers tell us."

### 1.2 Which product(s) does it cover?
- Product name: [FILL IN: {{product_name}}]
- Product type: [FILL IN: web / mobile / both]
- Version or release it applies to: [FILL IN: ]

### 1.3 Which people and groups must follow it?
[FILL IN: list roles, including any AI agents]
> Example: "The founder, any contractor who answers customers, and the AI assistant."

### 1.4 What is NOT covered by this policy?
[FILL IN: list]
> Example: "Legal contracts, the Privacy Policy, the Terms of Service, and security incident reports to authorities. Those have their own documents."

### 1.5 When does this policy start, and how often will it be reviewed?
- Start date: [FILL IN: YYYY-MM-DD]
- Review how often: [FILL IN: e.g., at the start of each phase and every 90 days]

---

# Part 2: Who Does What

> **Solo builder?** Write your own name in every row. That is fine. The goal is that no job is left without a name.

### 2.1 Role table

| Job | Who does it (name) | Backup (name) |
|---|---|---|
| Owns this policy | [FILL IN] | [FILL IN] |
| Reads the support inbox | [FILL IN] | [FILL IN] |
| Approves any message AI wrote | [FILL IN] | [FILL IN] |
| Updates the status page during problems | [FILL IN] | [FILL IN] |
| Collects and sorts feedback | [FILL IN] | [FILL IN] |
| Decides what gets built from feedback | [FILL IN] | [FILL IN] |
| Handles angry or upset customers | [FILL IN] | [FILL IN] |
| Handles privacy and data requests | [FILL IN] | [FILL IN] |

### 2.2 What happens when someone is on holiday or sick?
[FILL IN: who covers, and what the customer is told]
> Example: "Auto-reply says 'We are away until Monday. Urgent problems: reply with URGENT in the subject.' Backup checks the inbox once a day."

---

# Part 3: Who Are Our Customers?

### 3.1 Describe your typical customer in 2-3 sentences.
[FILL IN: ]
> Example: "People aged 20-45 who own houseplants and are new to plant care. They use their phone and expect quick, simple answers."

### 3.2 Customer groups

Different groups can get different reply speeds (see Part 6). Choose the groups you will use and describe each.

| Group name | Who is in it? | Special treatment (if any) |
|---|---|---|
| Beta tester | [FILL IN] | [FILL IN] |
| Free user | [FILL IN] | [FILL IN] |
| Paying customer | [FILL IN] | [FILL IN] |
| Founding / VIP customer | [FILL IN] | [FILL IN] |

> Example for Beta tester: "Invited people testing before launch. They get a direct line to the founder and a thank-you gift."
> Tip: Fewer groups is simpler. Three is plenty.

### 3.3 What do customers care about most?
[FILL IN: top 3]
> Example: "1) It works. 2) It is easy. 3) They get help fast."

### 3.4 Is any customer likely to be under 18 or need extra care?
- [ ] No
- [ ] Yes → [FILL IN: what extra care is needed]
> Warning: If yes, check Part 11 and ask a qualified professional. Children's data has strict rules in many places.

---

# Part 4: Channels (Where We Talk to Customers)

> For each channel you use, answer the questions. For channels you do **not** use, write "Not used" and why.

## 4.1 Email

- Is this channel used? [FILL IN: Yes / No]
- Address customers write to: [FILL IN: {{support_email}}]
- Address that sends product news (if different): [FILL IN: ]
- Who reads it, and how often? [FILL IN: ]
- First-reply promise: [FILL IN: see Part 6]
- Do you send an automatic "we got your message" reply? [FILL IN: Yes / No]
- Email signature (name, role, how to reach you): [FILL IN: ]
> Example: "Sam, Founder, PlantPal. Reply to this email any time."
> Tip: An automatic "we got it" reply is polite, but it is NOT the real reply. Do not count it as your promise.

## 4.2 In-App Chat or Help Button

- Is this channel used? [FILL IN: Yes / No]
- Where does the button appear in the app? [FILL IN: ]
- Hours when a real person is available: [FILL IN: ]
- What does the customer see outside those hours? [FILL IN: ]
- Which tool is used (if any)? [FILL IN: ]
- Does the chat remember past conversations? [FILL IN: Yes / No]
- Are there small in-app messages (tooltips, banners, pop-ups)? Who approves them? [FILL IN: ]
> Example: "Banner at the top of the home screen for outages only. Pop-ups are never used during a customer's first 2 minutes."

## 4.3 Community and Social (Discord, Slack, Reddit, X, forums)

- Is this channel used? [FILL IN: Yes / No]
- Where exactly? [FILL IN: {{community_url}}]
- Who watches it, and when? [FILL IN: ]
- What is allowed and not allowed there (community rules)? [FILL IN: 3-5 rules]
- If someone posts a bug or complaint in public, what do we do? [FILL IN: ]
- If someone posts private info (password, address, card number) by mistake, what do we do? 🔒
  - Required answer: Delete or hide it right away, send the person a private message, and tell them to change the password if needed.
> Example for public complaints: "Reply within 1 business day in the same thread, say sorry, move details to private message, and post back when fixed."

## 4.4 Phone and Video Calls

- Is this channel used? [FILL IN: Yes / No]
- Who gets calls (all customers, or only some groups)? [FILL IN: ]
- How do customers book a call? [FILL IN: link or process]
- Length of a normal call: [FILL IN: ]
- Do you record calls? [FILL IN: Yes / No]
  - If yes, how is permission asked? 🔒 [FILL IN: customer must be told and must agree before recording starts]
- After every call, where are notes saved? [FILL IN: ]
> Example: "Founder only. 20-minute calls booked on Calendly. Notes go into the Feedback Log within 24 hours."

## 4.5 Which channel for which type of message?

| What we need to say | Channel to use | Why |
|---|---|---|
| Welcome and getting started | [FILL IN] | [FILL IN] |
| Answer to a support question | [FILL IN] | [FILL IN] |
| Product news and new features | [FILL IN] | [FILL IN] |
| Planned downtime | [FILL IN] | [FILL IN] |
| Surprise outage | [FILL IN] | [FILL IN] |
| Asking for feedback | [FILL IN] | [FILL IN] |
| Billing or account problems | [FILL IN] | [FILL IN] |

> Warning: Do not put billing, password, or private details in public channels.

---

# Part 5: Tone and Voice (How We Sound)

### 5.1 Our three voice words
[FILL IN: three words, from Quick Start Q7]

### 5.2 For each word, what do we DO and what do we NOT do?

| Voice word | We DO | We do NOT |
|---|---|---|
| [word 1] | [FILL IN] | [FILL IN] |
| [word 2] | [FILL IN] | [FILL IN] |
| [word 3] | [FILL IN] | [FILL IN] |

> Example (word: "Honest"): We DO say "That is a bug and we are fixing it." We do NOT say "That should not happen" when it clearly did.

### 5.3 Words and phrases we always avoid
[FILL IN: list]
> Example: "'Per my last email', 'unfortunately you must', 'as you should know', blaming the customer."

### 5.4 Rules for every message 🔒
- [x] Say hello using the customer's name if we know it.
- [x] Say sorry if we caused a problem. One sincere sentence is enough.
- [x] Tell the customer **what happens next** and **when**.
- [x] Never promise a feature or date we are not sure about.
- [x] Never blame the customer.
- [x] Never share another customer's information.

### 5.4a Our own extra rules
[FILL IN: add 0-3 more]

### 5.5 Language, time zone, and accessibility
- Main language: [FILL IN: {{main_language}}]
- If someone writes in another language, we: [FILL IN: e.g., reply in simple English and offer a translation tool]
- Time zone for all promised times: [FILL IN: {{main_time_zone}}]
- Do messages use plain words and short sentences? [FILL IN: Yes]
- Do images in messages have a text description? [FILL IN: Yes / No]

---

# Part 6: Response Times (How Fast We Reply)

> **Two ideas work together here:**
> **Severity** = how bad is the problem?
> **Customer group** = who is asking?
> The table in 6.3 combines both.

### 6.1 What do we mean by "first reply" and "solved"?
- **First reply** = the first message from a real human (or human-approved message) that actually helps. "We got your message" does not count.
- **Solved** = the customer's problem is fixed and the customer has been told.

### 6.2 Severity levels

| Level | Meaning | Examples (write your own) |
|---|---|---|
| **S1 Critical** | The product is down or unsafe for many people. Data is lost, exposed, or wrong. Money is wrong. | [FILL IN] |
| **S2 High** | A main feature is broken, but there is a workaround. Or a small number of people are blocked. | [FILL IN] |
| **S3 Normal** | Something is annoying or confusing but customers can keep going. | [FILL IN] |
| **S4 Low** | Questions, ideas, compliments, small wishes. | [FILL IN] |

> Example S1: "Login fails for everyone. Customers are charged twice. Another person's data is visible."
> Example S4: "Can you add a dark mode?"

### 6.3 Reply-time grid (first reply target)

Fill in a time in every cell. Keep S1 the fastest. Keep Founding / VIP at least as fast as Paying, and Paying at least as fast as Free.

| Severity | Beta tester | Free user | Paying customer | Founding / VIP |
|---|---|---|---|---|
| **S1 Critical** | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| **S2 High** | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| **S3 Normal** | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |
| **S4 Low** | [FILL IN] | [FILL IN] | [FILL IN] | [FILL IN] |

> Example row for S1: Beta 1 hour | Free 4 hours | Paying 1 hour | VIP 30 minutes.
> Example row for S3: Beta 1 business day | Free 3 business days | Paying 1 business day | VIP 4 business hours.
> Tip: Do not promise what you cannot keep. A promise you miss half the time teaches customers that your promises are empty. Start slower and speed up later.

### 6.4 Update promises while a problem is being fixed

| Severity | We tell the customer what is happening every... |
|---|---|
| S1 Critical | [FILL IN: e.g., 30 minutes until fixed] |
| S2 High | [FILL IN: e.g., 4 hours] |
| S3 Normal | [FILL IN: e.g., 2 business days] |
| S4 Low | [FILL IN: e.g., when we have news] |

> Tip: End every update with "Our next update will be by [time]." It calms people and cuts repeat messages.

### 6.5 Support hours
- Normal hours: [FILL IN: {{support_hours}}]
- Do S1 problems get answered outside these hours? [FILL IN: Yes / No]
  - If yes, how are you alerted? [FILL IN: phone alert, pager app, etc.]
  - If no, what do customers see? [FILL IN: honest message with the next time you will reply]
- Public holidays we are closed: [FILL IN: ]

### 6.6 What if we miss a promised time?
- Who is told inside the team? [FILL IN: ]
- What do we say to the customer? [FILL IN: sorry + new time]
- Do we offer anything (extra days, a credit, a thank-you)? [FILL IN: ]
- Where do we write down the miss so we can learn from it? [FILL IN: ]

---

# Part 7: AI Agents in Customer Communication 🔒

> **Rule of this template: AI drafts. A human approves.**
> The AI may help write. It may never press "send" on its own.

### 7.1 What AI is allowed to do ✅

- [x] Read incoming messages and **suggest a severity** (S1-S4).
- [x] **Suggest tags** (bug, idea, question, praise, billing, etc.).
- [x] **Draft** a reply in our voice (Part 5) for a human to edit and send.
- [x] **Summarize** long threads and feedback into short notes.
- [x] **Find patterns** (e.g., "12 people asked for dark mode this week").
- [x] **Translate** messages, with a human checking before sending.
- [x] **Remind** the team when a promised reply time is close.

### 7.2 What AI must NEVER do ❌

- [x] Send, post, or publish anything to a customer without human approval.
- [x] Promise a feature, date, refund, credit, or discount.
- [x] Give legal, medical, financial, or safety advice.
- [x] Make up facts. If the AI does not know, it must write "needs human check".
- [x] Share one customer's information with another customer.
- [x] Paste customer personal data into AI tools that we have not approved for that use.
- [x] Pretend to be a human if a customer sincerely asks.
- [x] Close or resolve a customer's problem on its own.

### 7.3 Which AI tools are approved?

| Tool name | What it may be used for | Customer data allowed in? (Yes / No / Only anonymized) |
|---|---|---|
| [FILL IN] | [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] | [FILL IN] |

> Example: "Claude — drafting replies and summarizing feedback — Only anonymized (names, emails, and payment details removed)."

### 7.4 The human check: what must the approver look at before sending?
- [ ] Is every fact true? (Check the product, not just the draft.)
- [ ] Is anything promised that we cannot deliver?
- [ ] Does it sound like us (Part 5)?
- [ ] Is private information left out?
- [ ] Does it say what happens next and when?
- [ ] Is the severity right?

### 7.5 If we use a chatbot or automatic answers in the product
- Do we use one? [FILL IN: Yes / No]
- If yes, does it clearly say it is an automated assistant? [FILL IN: Yes / No]
- How can a customer reach a real person at any time? [FILL IN: ]
> Warning: This template assumes **no automatic AI replies**. If you want them, rewrite Part 7 first, then ask a second person to review it.

### 7.6 If AI makes a mistake in front of a customer
- What do we do within 1 hour? [FILL IN: correct the message, apologize, find out why]
- Where is it recorded? [FILL IN: ]

### 7.7 Prompt rules for AI helpers (copy these into your AI tool's instructions)

```text
You help {{product_name}} write messages to customers.
Rules:
1. You write DRAFTS only. A human sends them.
2. Use the voice in Part 5: {{voice_words}}. Short sentences. Plain words.
3. Never promise features, dates, refunds, or credits.
4. If you are not sure about a fact, write: [NEEDS HUMAN CHECK: reason].
5. Never include another customer's information.
6. Always end with what happens next and when.
7. Suggest a severity (S1-S4) and a tag, and explain why in one line.
```

---

# Part 8: The Journey Playbook (Development to First 500 Customers)

> Your product moves through **5 phases**. For each phase, answer the same questions. Change `current_phase` at the top of this file when you move on.

### 8.0 Phase overview

| Phase | Name | Who is using the product | Main goal of communication |
|---|---|---|---|
| 1 | Build | Nobody yet (team only) | Learn what people need before building too much |
| 2 | Private Beta | A small invited group | Find problems and confusing parts |
| 3 | Launch | The public starts arriving | Welcome people, stay stable, answer fast |
| 4 | First 100 customers | Early customers | Make each one successful and learn from each one |
| 5 | Customers 101-500 | A growing group | Stay personal while becoming organized |

> Tip: Moving to the next phase should be a **decision**, not an accident. Use the "Ready to move on?" question at the end of each phase.

---

## Phase 1: Build (before anyone uses it)

**1.1 What do we need to learn from people before launch?**
[FILL IN: 3 questions]
> Example: "Do people understand what the app does? Would they pay? What is missing?"

**1.2 Who will we talk to, and how do we find them?**
[FILL IN: e.g., 10-15 people from friends of friends, online communities, or a waiting list]

**1.3 How will we ask? (interviews, short survey, mock-up test)**
[FILL IN: ]

**1.4 Do we have a waiting list or landing page?**
- [ ] No
- [ ] Yes → What do we promise on it? [FILL IN: ] What email do we send people when they sign up? [FILL IN: ]

**1.5 What must be ready BEFORE the first customer message arrives?**
- [ ] Support email address works ({{support_email}})
- [ ] A way to collect feedback (Quick Start Q9)
- [ ] Reply-time grid filled (Part 6)
- [ ] Basic privacy notice ready (Part 11)
- [ ] Someone is named to answer (Part 2)

**1.6 Ready to move on?** Move to Phase 2 when: [FILL IN: e.g., "the app works end to end and 15 people agreed to test it"]

---

## Phase 2: Private Beta (invited testers)

**2.1 How many testers, and how did we pick them?**
[FILL IN: number and method]

**2.2 What do we tell testers on day 1?** (Include: what is being tested, what is broken, how to report problems, how fast we reply.)
[FILL IN: write the welcome message, or paste a link to it]

**2.3 How do testers report problems?**
[FILL IN: a form, an email, a chat, a call]
> Tip: Make reporting a one-step thing. Every extra step loses reports.

**2.4 What do we ask testers regularly?**
[FILL IN: e.g., a 3-question check-in every Friday]
> Example questions: "What was confusing? What did you love? What almost made you quit?"

**2.5 How do we thank testers?**
[FILL IN: e.g., free year, name in credits, early access]

**2.6 What are the rules for testers?** (Secrecy? Screenshots? Data may be deleted?)
[FILL IN: ]

**2.7 How do we end the beta kindly?**
[FILL IN: a final message and a short exit survey]

**2.8 Ready to move on?** Move to Phase 3 when: [FILL IN: e.g., "no S1 or S2 problems open for 14 days and 70% of testers say they would recommend it"]

---

## Phase 3: Launch (public arrives)

**3.1 Launch date and launch channels (where will we announce)?**
[FILL IN: ]

**3.2 What is the welcome message every new customer gets?**
[FILL IN: paste or link]
> Example: "Hi [Name]! Welcome to PlantPal. Here are 3 things to try first... Questions? Reply to this email."

**3.3 Who is on "launch watch" (extra eyes on messages) and for how long?**
[FILL IN: names, and e.g., first 7 days]

**3.4 During launch week, are the reply times faster, slower, or the same?**
[FILL IN: ]

**3.5 What problems do we expect?** (Write 3 and your planned reply for each.)
| Likely problem | Our planned reply |
|---|---|
| [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] |

**3.6 Do we have a status page ready and tested?** (Part 10)
- [ ] Yes, link: [FILL IN]
- [ ] No (not allowed at launch; set one up first)

**3.7 How do we handle public criticism or bad reviews during launch?**
[FILL IN: reply within X hours, say sorry, fix, ask to update the review when fixed]

**3.8 Ready to move on?** Move to Phase 4 when: [FILL IN: e.g., "the launch week is over and daily messages are under control"]

---

## Phase 4: First 100 Customers

> The goal: **every one of these customers should feel personally looked after.**

**4.1 What do we do for each new customer in their first week?**
[FILL IN: e.g., personal welcome note on day 1, check-in on day 3, tip on day 7]

**4.2 How do we find out whether each customer is successful?** (What action means "they got value"?)
[FILL IN: e.g., "added 3 plants and got 1 reminder"]

**4.3 What do we do if a customer is NOT using the product after 7 days?**
[FILL IN: e.g., one friendly nudge email, then leave them alone]

**4.4 Do we personally talk to customers (calls, chats)? How many per week?**
[FILL IN: ]

**4.5 How do we ask for reviews or testimonials, and when?** 🔒
- Rule: Ask only after the customer succeeded. Never pay for fake reviews. Never write fake ones. Never ask for only good reviews.
[FILL IN: how and when]

**4.6 How do we tell customers what we built because of their feedback?**
[FILL IN: e.g., a monthly "You asked, we built" email]

**4.7 Ready to move on?** Move to Phase 5 when: [FILL IN: e.g., "100 customers and we answer 90% of messages inside the promised time"]

---

## Phase 5: Customers 101 to 500

> The goal: **stay personal while becoming organized.** What worked by memory now needs a system.

**5.1 What can no longer be done by hand?** (List and name the fix.)
| Job that is getting too big | How we will manage it |
|---|---|
| [FILL IN] | [FILL IN] |
| [FILL IN] | [FILL IN] |

**5.2 Do we add a help center / FAQ?**
- [ ] No
- [ ] Yes → Where? [FILL IN] Who keeps it updated? [FILL IN] Which 10 questions go first? [FILL IN]

**5.3 Do we add saved reply templates for common questions?** (Part 14)
[FILL IN: Yes / No, and who owns them]

**5.4 Do we hire help or add a person?** When will we decide?
[FILL IN: e.g., "when more than 40 messages a week" or "when we miss reply times twice in a month"]

**5.5 How do we keep VIP and founding customers feeling special?**
[FILL IN: ]

**5.6 How do we handle customers who ask for things we will never build?**
[FILL IN: a kind "no" with the reason; see Part 14]

**5.7 What do we do when customer number 500 arrives?**
[FILL IN: e.g., thank-you note to the first 500, a customer survey, then write the next policy version]

**5.8 Finished?** At 500 customers, we will: [FILL IN: review the whole policy, update the version history in Part 16, and decide what comes next]

---

# Part 9: Feedback: Collecting It, Sorting It, Using It

> Feedback is only useful if it (1) is collected in one place, (2) is sorted, and (3) leads to a decision and an answer back.

### 9.1 Where does feedback come from?

| Source | Do we use it? | Where does it end up? |
|---|---|---|
| Support emails | [FILL IN] | [FILL IN] |
| In-app chat or form | [FILL IN] | [FILL IN] |
| Community and social posts | [FILL IN] | [FILL IN] |
| Calls and interviews | [FILL IN] | [FILL IN] |
| App store reviews | [FILL IN] | [FILL IN] |
| Surveys | [FILL IN] | [FILL IN] |
| What customers do (usage data) | [FILL IN] | [FILL IN] |

### 9.2 The one place everything is saved (the "Feedback Log")
- Tool or file: [FILL IN: ]
- Link: [FILL IN: ]
- Who can see it: [FILL IN: ]
- Who can edit it: [FILL IN: ]

### 9.3 What must every feedback entry contain? (Do not remove any.)

| Field | Meaning |
|---|---|
| Date | When we received it |
| Source | Which channel |
| Customer group | Beta / Free / Paying / VIP (no names needed) |
| What they said | Short, in their own words |
| Type | Bug / Idea / Question / Confusion / Praise / Billing |
| Severity | S1-S4 (Part 6) |
| Feature or screen | Where in the product |
| Status | New / Reviewed / Planned / Building / Done / Not planned |
| Our decision and why | One sentence |
| Did we tell the customer? | Yes / No, and date |

### 9.4 How do we sort and decide? (the simple way)

Score each idea from 1 to 5 on three things, then add them up:

| Question | Score 1-5 |
|---|---|
| How many customers asked for this? (1 = one person, 5 = many) | |
| How much does it hurt or help them? (1 = a little, 5 = a lot) | |
| How easy is it for us to do? (1 = very hard, 5 = very easy) | |

**Total 12-15 = do soon. 8-11 = maybe. Under 8 = not now.**

Our own rule changes (if any): [FILL IN: ]
> Tip: Never build something just because one loud person asked. Look for patterns across many.

### 9.5 How often do we review feedback?
[FILL IN: e.g., 30 minutes every Friday]

### 9.6 Who decides what gets built?
[FILL IN: name or role]

### 9.7 Closing the loop: telling people what happened 🔒
- Every person who gave feedback gets an answer, even if the answer is "not now".
- Within [FILL IN: number] days of a decision, we tell them.
- When something ships, we tell the people who asked.
- Where do we announce shipped improvements? [FILL IN: ]

### 9.8 What do we do with feedback that is rude, unfair, or unsafe?
[FILL IN: e.g., stay calm, one polite reply, no argument, hide threats or abuse, escalate to Part 13]

---

# Part 10: Problems, Outages, and Downtime Messages

> When something breaks, **say so early, say it plainly, and say when you will say more.**

### 10.1 Where do we post problem updates?
- Status page: [FILL IN: {{status_page_url}}]
- In-app banner: [FILL IN: Yes / No]
- Email to affected customers: [FILL IN: Yes / No, and when]
- Community or social post: [FILL IN: Yes / No]
- Who is allowed to post? [FILL IN: ]

> Tip: Put your status page on a different address and different host from your product, so it still works when the product is down.

### 10.2 The life of a problem (use these 4 steps in every update)

| Step | What we say |
|---|---|
| 1. Investigating | "We know something is wrong. We are looking into it." |
| 2. Identified | "We found the cause. We are working on the fix." |
| 3. Monitoring | "A fix is in. We are watching to be sure." |
| 4. Resolved | "It is fixed. Here is what happened and what we are doing about it." |

### 10.3 When do we post, and how fast?

| Severity | Post the first update within | Then update every |
|---|---|---|
| S1 Critical | [FILL IN] | [FILL IN] |
| S2 High | [FILL IN] | [FILL IN] |

> Example: S1: 15 minutes after we confirm it, then every 30 minutes.

### 10.4 What every problem update must include 🔒
- [x] What is affected (in plain words)
- [x] Who is affected
- [x] What customers can do right now
- [x] The time of this update and the time of the next one
- [x] No blame, no jargon, no guessing about causes before they are known

### 10.5 Planned downtime (maintenance)
- How many days ahead do we tell people? [FILL IN: e.g., 3 days]
- Best time of day or week? [FILL IN: ]
- Where do we announce it? [FILL IN: ]

### 10.6 After a serious problem (S1): the written follow-up
- Do we write a short "what happened" note? [FILL IN: Yes, within X days]
- What does it contain? (what happened, how long, what we fixed, what we will change)
- Where do we publish it? [FILL IN: ]
- Do we offer anything to affected customers? [FILL IN: ]

### 10.7 If customer data may have been lost or exposed 🔒
- Stop. This is a **security and privacy incident**, not just a normal outage.
- Who is told immediately? [FILL IN: name]
- Who decides whether customers and authorities must be told? [FILL IN: name or qualified professional]
- Do not post guesses. Do not delete evidence.
> Warning: Many places have legal deadlines for telling people about data problems. Find out which apply to you (see Part 11).

---

# Part 11: Privacy and Legal Basics (Reminders, Not Legal Advice)

### 11.1 What customer information do we collect when we communicate?
[FILL IN: e.g., name, email, messages, call notes, screenshots, device type]

### 11.2 Why do we keep it, and for how long?
[FILL IN: purpose and period]
> Example: "To answer questions and improve the product. Support messages are deleted after 24 months."

### 11.3 Where is it stored, and who can see it?
[FILL IN: tools and people]

### 11.4 Rules for marketing emails 🔒
- [x] We only email product news to people who agreed to receive it.
- [x] Every marketing email has a working **unsubscribe** link.
- [x] We honor an unsubscribe request quickly (within [FILL IN: days]).
- [x] Support replies are different from marketing. We do not hide promotions inside support replies.
- [x] Our email has a real sender name and a real contact address.

### 11.5 Rules for feedback and testimonials 🔒
- [x] We ask permission before quoting a customer by name or showing their photo.
- [x] We never invent a customer, review, or quote.
- [x] When we share feedback inside the team or with AI tools, we remove names and private details where possible.

### 11.6 Customer requests about their data
- If a customer asks "what do you have on me?" or "delete my data", who handles it? [FILL IN: ]
- How fast do we respond? [FILL IN: ]
- How do we confirm it is really the customer asking? [FILL IN: ]

### 11.7 Is any of this likely to apply to us? (Tick, then research or ask a professional.)
- [ ] Customers in the European Union or United Kingdom (privacy rules like GDPR)
- [ ] Customers in California or other US states with privacy laws
- [ ] Children under 13 or under 16
- [ ] Health, financial, or other sensitive data
- [ ] Customers in countries with data-location rules
- [ ] None that we know of (write the date you checked: [FILL IN])

### 11.8 Where are our official documents?
- Privacy Policy link: [FILL IN]
- Terms of Service link: [FILL IN]
- Who last reviewed them, and when? [FILL IN]

---

# Part 12: Measuring How We Are Doing

> You cannot improve what you do not count. Keep the numbers simple.

### 12.1 Our scoreboard

| What we count | How we count it | Target | Phase it starts |
|---|---|---|---|
| **First reply time** | Time from customer message to first helpful human reply | [FILL IN] | Phase 2 |
| **On-time rate** | Messages answered inside the promise ÷ all messages × 100 | [FILL IN] (e.g., 90%) | Phase 3 |
| **Time to solve** | Time from message to "solved" | [FILL IN] | Phase 3 |
| **Customer happiness (CSAT)** | "Did we help you?" 1-5 after a conversation closes | [FILL IN] | Phase 3 |
| **Recommend score (NPS)** | "How likely are you to recommend us? 0-10" | [FILL IN] | Phase 4 |
| **Message volume** | Number of messages per week | (watch only) | Phase 2 |
| **Top 3 reasons people write** | From tags in the Feedback Log | (watch only) | Phase 2 |
| **Feedback answered** | % of feedback where we told the customer the result | [FILL IN] | Phase 4 |
| **Repeat problems** | Same problem reported again | Going down | Phase 4 |

### 12.2 Where do we write the numbers?
[FILL IN: tool or file and link]

### 12.3 Review rhythm

| How often | What we look at | Who |
|---|---|---|
| Daily (quick) | Anything open longer than promised; any S1/S2 | [FILL IN] |
| Weekly (30 min) | Scoreboard, top feedback, missed promises | [FILL IN] |
| Monthly (60 min) | Trends, what we built from feedback, what to change in this policy | [FILL IN] |
| At each phase change | Re-read this whole policy and update it | [FILL IN] |

### 12.4 What do we do if a number is bad?
[FILL IN: e.g., "If the on-time rate drops under 80% for 2 weeks, we change the promise or add help."]

---

# Part 13: When Things Go Wrong: Escalation and Exceptions

### 13.1 Escalation ladder (who do we pass it to when we cannot solve it)

| Level | Who | When we use it |
|---|---|---|
| Level 1 | [FILL IN: person who first answers] | Every message |
| Level 2 | [FILL IN: person with technical knowledge] | Needs a fix or deeper checking |
| Level 3 | [FILL IN: owner / founder] | S1 problems, legal threats, public blowups, safety, money |

> Solo builder? Write your own name in all three, and add one trusted outside person as a backup for Level 3.

### 13.2 Situations that ALWAYS go straight to Level 3 🔒
- [x] Customer data lost or exposed
- [x] Safety concerns or threats
- [x] Legal threats, or a customer says they will sue
- [x] Press or media asking questions
- [x] Large refunds or payment disputes
- [x] Any message that might be about a child

### 13.3 Upset or angry customers
How do we respond? [FILL IN: steps]
> Example: "1) Thank them for telling us. 2) Say sorry for how it felt. 3) Say what we will do and by when. 4) Do not argue. 5) If still angry after 2 replies, hand to Level 3."

### 13.4 Refunds, credits, and special favors
- Who can approve? [FILL IN: ]
- Up to what amount? [FILL IN: ]
- What do we do when someone asks for an exception? [FILL IN: ]

### 13.5 Customers who break the rules (abuse, spam, threats)
- Warning steps: [FILL IN: e.g., 1 friendly warning, then 1 firm warning, then block]
- Who may block someone? [FILL IN: ]
- How do we record it? [FILL IN: ]

---

# Part 14: Message Templates (Ready-to-Copy Starters)

> Replace everything in `[brackets]`. A person approves every message before it is sent (Part 7).

### 14.1 "We got your message" (automatic)
```text
Hi [Name],
Thanks for writing to {{product_name}}. A real person will reply within [time from Part 6].
If this is urgent (nobody can log in, money looks wrong, or data looks wrong), reply with URGENT in the subject.
— {{product_name}} Team
```

### 14.2 Fixing a problem
```text
Hi [Name],
Thanks for telling us about [problem]. Sorry for the trouble.
Here is what we found: [one plain sentence].
Here is what happens next: [action] by [date/time].
We will write to you again by [date/time], even if we have no news.
— [Your name]
```

### 14.3 Saying thanks for an idea (not decided yet)
```text
Hi [Name],
Thank you for the idea about [idea]. We wrote it down and we read every one.
We are not able to promise a date, but we will tell you when we decide.
— [Your name]
```

### 14.4 Saying no kindly
```text
Hi [Name],
Thanks for suggesting [idea]. We looked at it carefully.
We are not going to build it right now because [honest short reason].
You can tell us more about what you are trying to do, and we may be able to help another way: [option].
— [Your name]
```

### 14.5 We shipped something you asked for
```text
Hi [Name],
You told us [what they asked]. It is live now! Here is how to use it: [one or two lines].
Thank you for helping us make {{product_name}} better.
— [Your name]
```

### 14.6 Problem update (for the status page)
```text
[Time and time zone] — [Investigating / Identified / Monitoring / Resolved]
What is affected: [plain words]
Who is affected: [group]
What you can do now: [workaround or "nothing needed"]
Next update by: [time]
```

### 14.7 Resolved + short "what happened"
```text
[Time] — Resolved.
What happened: [one or two sentences, no blame].
How long: from [start] to [end].
What we are doing so it does not happen again: [one or two actions].
We are sorry. Questions? Write to {{support_email}}.
```

### 14.8 Planned downtime
```text
On [date] from [start] to [end] ([time zone]) {{product_name}} will be unavailable for updates.
What you need to do: [nothing / save your work].
Questions: {{support_email}}.
```

### 14.9 Asking for feedback
```text
Hi [Name],
You have been using {{product_name}} for [time]. Could you answer 3 quick questions? It takes under 2 minutes: [link].
Everything you tell us is read by a real person.
— [Your name]
```

### 14.10 Welcome (new customer)
```text
Hi [Name],
Welcome to {{product_name}}! Here are 3 things to try first:
1. [Step]
2. [Step]
3. [Step]
If you get stuck, reply to this email. A real person will answer within [time].
— [Your name]
```

### 14.11 Our own templates
[FILL IN: add 2-5 more for situations that are common for your product, e.g., password reset trouble, billing question, account deletion]

---

# Part 15: Ready-to-Launch Checklist

> **Tick every box. If one cannot be ticked, write why next to it.** A product is not ready for customers until all boxes are ticked or have an owner and a date.

### 15.1 Document is complete
- [ ] Variables at the top of the file are filled in
- [ ] Search for `FILL` finds **nothing**
- [ ] Search for `{{` finds **nothing** (except inside the AI prompt code block)
- [ ] Every `TBD` has an owner and a date
- [ ] Every example was replaced with our own words

### 15.2 People
- [ ] Every job in Part 2 has a name and a backup
- [ ] Holiday/away plan written

### 15.3 Channels
- [ ] Support email works. We sent a test message and got a reply.
- [ ] In-app help or chat works on both web and mobile (if we have both)
- [ ] Community has posted rules and a named watcher
- [ ] Call booking works (if we offer calls)
- [ ] Test message sent through every channel we listed

### 15.4 Promises
- [ ] Reply-time grid is complete (Part 6.3)
- [ ] We can really keep those promises for the next 30 days
- [ ] Out-of-hours message is written

### 15.5 AI safety
- [ ] Approved AI tools are listed (Part 7.3)
- [ ] Nobody can send AI-written messages without approval
- [ ] AI instructions are saved in the AI tool (Part 7.7)

### 15.6 Feedback
- [ ] Feedback Log exists and we tested adding an entry
- [ ] Review time is booked in the calendar
- [ ] Someone is named to close the loop with customers

### 15.7 Problems and outages
- [ ] Status page exists and was tested (including from a phone)
- [ ] Templates in Part 14 are copied into our tools
- [ ] We practiced one pretend outage message

### 15.8 Privacy and legal
- [ ] Privacy Policy and Terms are live and linked
- [ ] Unsubscribe link works in marketing emails
- [ ] Someone knows how to handle a "delete my data" request
- [ ] We checked Part 11.7 and asked for help where needed

### 15.9 Measuring
- [ ] Scoreboard exists and a person is named to fill it in
- [ ] First weekly review is in the calendar

### 15.10 Final test: "the stranger test"
- [ ] We gave this document to a person who has not seen it. They could answer "Who do I contact, how fast will they reply, and what will they say?" without asking us anything.
- [ ] A second person read it and found no confusing parts.

---

# Part 16: Sign-Off and Version History

### 16.1 Approval

| Role | Name | Date | Signature or "Approved" |
|---|---|---|---|
| Policy owner | [FILL IN] | [FILL IN] | [FILL IN] |
| Reviewer (a second person, if possible) | [FILL IN] | [FILL IN] | [FILL IN] |

### 16.2 Version history (add a new row for every change)

| Version | Date | Phase | What changed | Changed by |
|---|---|---|---|---|
| 1.0 | [FILL IN] | [FILL IN] | First complete version | [FILL IN] |
| | | | | |
| | | | | |

### 16.3 Next review date
[FILL IN: YYYY-MM-DD]

---

# Part 17: Common Mistakes (Read Before You Launch)

| Mistake | Why it hurts | Do this instead |
|---|---|---|
| Promising 1-hour replies when you are one person | You will miss it and customers stop believing you | Promise what you can keep for 30 days. Speed up later. |
| Counting the automatic reply as a real reply | The customer still feels ignored | Count only a helpful human reply |
| Writing "quickly", "soon", "regularly" | Nobody knows what it means | Use numbers and days |
| Letting AI send messages by itself | It can invent facts or promise things | AI drafts. A human approves. |
| Keeping feedback in many places | Patterns are impossible to see | One Feedback Log |
| Collecting feedback and never replying | Customers stop giving it | Close the loop (Part 9.7) |
| Hiding problems | Customers find out anyway and trust drops | Post early, plainly, and often |
| Blaming the customer | Turns small problems into big ones | Say sorry, fix, explain |
| Promising features | You may not be able to deliver | Say "we wrote it down" |
| Copying the examples word for word | They may not fit your product | Use your own words and numbers |
| Skipping privacy | Fines, lost trust, or worse | Do Part 11, and ask a professional when unsure |
| Never reviewing the policy | It gets out of date | Review at every phase change |
| Putting customer private data into any AI tool | Data leaks | Only use approved tools, with private details removed |
| Asking only happy customers for reviews | Fake picture of reality, and may break the rules | Ask fairly and never fake reviews |
| Leaving blanks or "TBD" without an owner | The next person has to guess | Always name an owner and a date |

---

# Part 18: Glossary (Plain Words)

| Word | Easy meaning |
|---|---|
| **AI agent** | A computer helper that can read, write, and sometimes take actions by itself. In this policy, it only drafts. |
| **Beta** | A early test version used by a small group before the public. |
| **Channel** | A place where we talk to customers: email, chat, community, phone. |
| **CSAT** | Customer Satisfaction score. A quick "Did we help you?" rating. |
| **Escalate** | Pass a problem to someone with more power or skill. |
| **Feedback** | Anything a customer tells us: problems, ideas, praise, confusion. |
| **Feedback Log** | The one place where all feedback is written down. |
| **First reply** | The first helpful message from a real person. |
| **Incident** | A problem that hurts the product or customers, like an outage. |
| **Maintenance** | Planned work on the product that may pause it for a short time. |
| **NPS** | Net Promoter Score. "How likely are you to recommend us, 0 to 10?" |
| **Outage** | Time when the product does not work. |
| **Phase** | One of the 5 stages from building to 500 customers. |
| **Policy** | A written set of rules everyone follows. |
| **Severity** | How serious a problem is (S1 worst, S4 smallest). |
| **SLA** | Service Level Agreement. A promise about how fast we reply or fix. |
| **Status page** | A public web page that shows whether the product works right now. |
| **Template** | A ready-made shape that you fill in with your own details. |
| **Tone** | How our words sound: kind, serious, funny, formal. |
| **Triage** | Sorting messages by how urgent and important they are. |
| **Unsubscribe** | A way for a person to stop getting emails from us. |
| **VIP / Founding customer** | One of our earliest or most important customers. |
| **Workaround** | A temporary way to get something done while the real fix is not ready. |

---

*End of template. Master copy version 1.0. Copy this file for each project; do not edit the master.*
