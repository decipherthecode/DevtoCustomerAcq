# How to Fill This Document (Read This First)

**File name:** `Feature_Request_Register.md`
**Folder:** `Customer-Feedback-and-Product-Improvement/`
**Template version:** 1.1

## What is this document?

This is a **list of every idea or request** people have for improving your product. A "feature request" is simply: *"Someone wants the product to do something new or work better."*

It follows your product from **first build until your first 500 customers**. Every request gets its own **card** (Part 4). The **summary table** (Part 3) gives a quick overview of all cards.

## The 5 simple rules

1. **One request = one card.** Never put two ideas on one card.
2. **Answer every question.** If you do not know, write `UNKNOWN` and say who can find out. Never leave a blank and never guess.
3. **Use plain words.** Write as if explaining to a friend. No secret abbreviations.
4. **Copy the card, don't change it.** Copy the blank card in Part 4, paste it below the last card, and fill it in. Do not delete questions.
5. **Update the date and status** every time you touch a card.

## How to use this file in 6 steps

| Step | What to do | Where |
|---|---|---|
| 1 | Fill in **Part 1: Project Info** once, at the start. | Part 1 |
| 2 | Someone asks for something? **Copy the blank card** and give it the next ID (FR-001, FR-002, ...). | Part 4 |
| 3 | Answer **every question** on the card. | Part 4 |
| 4 | **Add one row** for the card in the summary table. | Part 3 |
| 5 | As work moves forward, **tick the stage boxes** and change the **Status**. | Part 4 |
| 6 | After launch, fill in **"What we learned"** and update the change log. | Part 4 and Part 6 |

## Words you may not know

| Word | Simple meaning |
|---|---|
| **Feature request** | Something someone wants the product to do or do better |
| **Requester** | The person who asked |
| **Acceptance test** | A yes/no check that proves the feature works ("Click button, file downloads") |
| **Beta** | A small group of real users try it before everyone else |
| **Launch** | Everyone can use it |
| **AI agent** | An AI helper that can write code, tests, or documents for you |
| **Human approval** | A real person must say "yes" before the next step |
| **Out of scope** | Things we are deliberately NOT building in this request |

## How scoring works (no math skills needed)

Give each request three scores from 1 to 3, then add them up.

| Question | 1 | 2 | 3 |
|---|---|---|---|
| **Impact:** How much does this help customers? | A little | Quite a lot | A huge amount |
| **Ease:** How easy is it to build? | Very hard / long | Medium | Easy / quick |
| **Demand:** How many customers asked for it? | 1 person | 2 to 9 people | 10 or more people |

**Total = Impact + Ease + Demand** (lowest 3, highest 9)

| Total | Priority label | Meaning |
|---|---|---|
| 8 to 9 | **Do First** | Plan it right away |
| 6 to 7 | **Do Next** | Plan it after the "Do First" items |
| 3 to 5 | **Do Later** | Keep it on the list, review again later |

## Allowed Status values (use ONLY these)

`New` | `In Review` | `Approved` | `Planned` | `Building` | `Testing` | `Beta` | `Launched` | `Learning` | `On Hold` | `Rejected` | `Duplicate`

## The 8 stages every request travels through

**Idea → Review → Plan → Build → Test → Beta → Launch → Learn**

---

# Part 1: Project Info (Fill In Once)

| Question | Your answer |
|---|---|
| What is the product's name? | |
| In one sentence, what does the product do? | |
| Who is it for? (describe your ideal customer) | |
| Who owns this register? (name and role) | |
| Who is the final decision-maker for feature requests? | |
| Where are customer messages collected? (email address, chat tool, form link) | |
| Which tool or AI agent keeps this file up to date? (or write `Nobody, done by hand`) | |
| Date this register was started (YYYY-MM-DD) | |
| Our goal: first 500 customers by what date? | |
| **Current number of customers today** | |
| **Current phase** (tick one) | ☐ Building  ☐ Private testing  ☐ Beta  ☐ Launched  ☐ Growing to 500 |
| How often will we review this list? (e.g. every Monday) | |

---

# Part 2: Rules for AI Agents and Humans Working Together

Fill these in once. Every card refers back to them.

| Question | Your answer |
|---|---|
| What can an AI agent do **without asking**? (e.g. write draft code, write tests, summarize feedback) | |
| What must an AI agent **never** do on its own? (e.g. delete data, change prices, publish to customers, spend money) | |
| Who must give **human approval** before building starts? | |
| Who must give **human approval** before launch? | |
| Where does the AI agent find project documents? (links or folder names) | |
| What should the AI agent do when unsure? | Write `UNKNOWN`, stop, and ask the person named above. Do not guess. |

---

# Part 3: Summary Table (One Row per Request)

Add one row for every card. Keep this table in sync with the cards.

| ID | Request title (short) | Source | Phase when asked | Customers when asked | Impact | Ease | Demand | Total | Priority | Stage now | Status | Owner | Last updated |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| FR-000 | *(example) Export my data as a file* | Email | Beta | 42 | 3 | 2 | 3 | 8 | Do First | Plan | Planned | Sam | 2026-10-19 |
| | | | | | | | | | | | | | |

---

# Part 4: Request Cards

## Blank Card (Copy Everything from Here to the Line Marked END OF CARD)

### FR-___: (Write a short title, 3 to 8 words)

**Status:** `New`  |  **Current stage:** Idea  |  **Last updated:** YYYY-MM-DD  |  **Card owner:** _____

#### A. Who asked and where did it come from?

| Question | Your answer |
|---|---|
| Date we received it (YYYY-MM-DD) | |
| Where did it come from? (tick one) | ☐ Customer email / support chat  ☐ Interview or survey  ☐ In-app feedback, review, or social media  ☐ Internal team idea / analytics data |
| Who asked? (name, company, or "Anonymous") | |
| Is this person a paying customer? | ☐ Yes  ☐ No  ☐ Not sure |
| Link or copy of the original message | |
| **How many customers did we have when this was asked?** | |
| Has anyone else asked for the same thing? How many people? (search this file first) | |
| Is this a duplicate of another card? | ☐ No  ☐ Yes, it is FR-___ (then set Status to `Duplicate`) |

#### B. What is the problem? (Describe the problem, not the solution)

| Question | Your answer |
|---|---|
| What is the person trying to do? | |
| What stops them or makes it hard today? | |
| How do they work around it today? | |
| How often does this problem happen? | ☐ Every day  ☐ Every week  ☐ Sometimes  ☐ Rarely |
| What happens if we never fix it? (e.g. customers leave, extra support work) | |

#### C. What is the idea? (The feature in plain words)

| Question | Your answer |
|---|---|
| Finish this sentence: *"As a ______ , I want to ______ , so that ______ ."* | |
| What will the customer see or be able to do when it is finished? | |
| What is **NOT** included? (Out of scope. Write at least one thing.) | |
| Are there any pictures, sketches, or example products? (links) | |

#### D. Score and priority

| Question | Your answer |
|---|---|
| Impact (1 to 3) and why | |
| Ease (1 to 3) and why | |
| Demand (1 to 3) and why | |
| **Total** (Impact + Ease + Demand) | |
| **Priority label** | ☐ Do First (8 to 9)  ☐ Do Next (6 to 7)  ☐ Do Later (3 to 5) |
| Does it help us reach our first 500 customers? How? | |
| **Launch-by customer count:** by how many customers should this be live? | |
| Does anything need to be built first? (list FR-IDs or write `Nothing`) | |

#### E. Decision

| Question | Your answer |
|---|---|
| Decision | ☐ Approved  ☐ On Hold  ☐ Rejected  ☐ Need more information |
| Who decided? | |
| Date decided (YYYY-MM-DD) | |
| Reason for the decision (one or two sentences) | |
| If On Hold or Rejected: when do we look at it again? | |
| Did we tell the person who asked? | ☐ Yes, on (date) ______  ☐ No, not yet  ☐ Not needed |

#### F. Instructions for the AI agent (fill in only after "Approved")

| Question | Your answer |
|---|---|
| **AI-ready task description:** explain in 3 to 6 short sentences exactly what to build. Use plain words. | |
| **Acceptance tests:** write 3 to 5 yes/no checks. Example: *"Click Export, a file downloads."* | 1. <br>2. <br>3. |
| **The AI may change or create:** (name files, screens, or areas) | |
| **The AI must NOT touch:** (name files, screens, data, or settings) | |
| **Links the AI should read first:** (specs, designs, related cards, past decisions) | |
| **Human approval needed before building:** who? | |
| **Human approval needed before launch:** who? | |
| What should the AI do if something is unclear? | Write `UNKNOWN`, stop, and ask the person above. Do not guess. |

#### G. Risks and privacy / security check

| Question | Your answer |
|---|---|
| What is the worst thing that could go wrong if we build this? | |
| Does this feature collect, show, or store customer information? (names, emails, payments, files) | ☐ No  ☐ Yes, it handles: ______ |
| Does it change who can see or edit something? | ☐ No  ☐ Yes, describe: ______ |
| Could it break something that works today? | ☐ No  ☐ Yes, which part: ______ |
| Does it involve rules or laws? (privacy, payments, children's data, accessibility) | ☐ No  ☐ Yes  ☐ Not sure, ask: ______ |
| How serious is the biggest risk? | ☐ Low  ☐ Medium  ☐ High (High needs human approval before building) |
| What will we do to reduce that risk? | |
| Who checked this section? (name and date) | |

#### H. Cost and time estimate

| Question | Your answer |
|---|---|
| How long will it take? | ☐ Under 1 day  ☐ 1 to 3 days  ☐ 1 to 2 weeks  ☐ More than 2 weeks |
| How many people (or AI agents) are needed, and who? | |
| Extra money needed? (tools, services, fees; write `0` if none) | |
| Does it add ongoing monthly cost after launch? | ☐ No  ☐ Yes: about ______ per month |
| How sure are you about this estimate? | ☐ Very sure  ☐ Somewhat sure  ☐ A guess |
| Who approved the time and money? (name and date) | |

#### I. Release and rollback plan

| Question | Your answer |
|---|---|
| Who gets it first? | ☐ Our team only  ☐ A small beta group (how many? ____)  ☐ Everyone |
| How will we release it? | ☐ All at once  ☐ Slowly to more and more customers  ☐ Switched on with an on/off setting |
| How will we know it is working? (what do we watch?) | |
| What would tell us something is wrong? (examples: errors, angry messages, drop in usage) | |
| **How do we undo it?** (step-by-step, in plain words) | |
| Who can press the "undo" button, and how fast? | |
| How will we tell customers about it? (email, in-app message, notes, nothing) | |
| Who must say "go" on launch day? (name) | |

#### J. Stage tracker (tick each box when finished, add the date)

| Stage | What "done" means | Done? | Date | Who |
|---|---|---|---|---|
| 1. Idea | Card is filled in through Section C | ☐ | | |
| 2. Review | Scored (Section D) and decided (Section E) | ☐ | | |
| 3. Plan | Sections F, G, H and I filled in, owner and target date set | ☐ | | |
| 4. Build | Feature is built and the AI/developer says it works | ☐ | | |
| 5. Test | Every acceptance test in Section F passes, and no serious bugs remain | ☐ | | |
| 6. Beta | A small group tried it and gave feedback | ☐ | | |
| 7. Launch | Everyone can use it and the requester has been told | ☐ | | |
| 8. Learn | We checked the results (Section K) | ☐ | | |

| Question | Your answer |
|---|---|
| Target date for the next stage (YYYY-MM-DD) | |
| Is anything blocking us? (write `Nothing` if clear) | |
| Link to the work (code, design, or task tracker) | |

#### K. What did we learn? (Fill in 2 to 4 weeks after launch)

| Question | Your answer |
|---|---|
| How many customers used the feature? | |
| Did it solve the problem? | ☐ Yes  ☐ Partly  ☐ No |
| What did customers say? (copy 1 to 3 comments) | |
| Did support questions go up or down? | ☐ Up  ☐ Down  ☐ Same |
| **Customer count at launch** | |
| What would we do differently next time? | |
| Do we need a new card (FR-___) as a follow-up? | ☐ No  ☐ Yes: FR-___ |

**Card history:** (add one line each time something changes)
- YYYY-MM-DD: Card created by ______

**END OF CARD**

---

## Filled Example (Read This to See How It Looks)

### FR-000: Export my data as a file

**Status:** `Planned`  |  **Current stage:** Plan  |  **Last updated:** 2026-10-19  |  **Card owner:** Sam

#### A. Who asked and where did it come from?

| Question | Your answer |
|---|---|
| Date we received it | 2026-10-12 |
| Where did it come from? | ☒ Customer email / support chat |
| Who asked? | Priya, owner of a small bakery |
| Paying customer? | ☒ Yes |
| Link or copy of the original message | "I want to download all my orders so I can send them to my accountant." |
| Customers when asked | 42 |
| Has anyone else asked? | Yes, 9 other people (see support inbox, tag `export`) |
| Duplicate? | ☒ No |

#### B. What is the problem?

| Question | Your answer |
|---|---|
| What is the person trying to do? | Send her order history to her accountant. |
| What stops them today? | There is no download button. |
| Workaround today | Copies orders by hand into a spreadsheet; takes about 2 hours a month. |
| How often? | ☒ Every week |
| If we never fix it? | Customers may leave for a product that offers export. |

#### C. What is the idea?

| Question | Your answer |
|---|---|
| Sentence | As a shop owner, I want to download my orders as a file, so that I can share them with my accountant. |
| What will the customer see? | An "Export" button on the Orders page that downloads a spreadsheet file. |
| NOT included | Exporting customer lists. Choosing a date range (maybe later). |
| Pictures or examples | None yet |

#### D. Score and priority

| Question | Your answer |
|---|---|
| Impact | 3, saves hours every month |
| Ease | 2, medium effort |
| Demand | 3, 10 people asked |
| **Total** | 8 |
| **Priority label** | ☒ Do First |
| Helps reach 500? | Yes, accountants often recommend the product to other shop owners if reports are easy. |
| Launch-by customer count | 100 |
| Needs anything first? | Nothing |

#### E. Decision

| Question | Your answer |
|---|---|
| Decision | ☒ Approved |
| Who decided? | Alex (product owner) |
| Date decided | 2026-10-15 |
| Reason | High demand, medium effort, matches our goal. |
| Told the requester? | ☒ Yes, on 2026-10-16 |

*(Sections F to K are filled in the same way as the work moves forward.)*

---

## Your Cards Start Here

*(Paste copies of the blank card below this line. Newest at the bottom.)*

---

# Part 5: Final Check Before You Save (Tick Every Box)

- ☐ Part 1 (Project Info) is fully filled in.
- ☐ Part 2 (AI and human rules) is fully filled in.
- ☐ Every card has a unique ID (FR-001, FR-002, ...).
- ☐ Every card has a row in the summary table.
- ☐ No answer is blank. Unknown answers say `UNKNOWN` plus who will find out.
- ☐ Every `Approved` card has at least 3 acceptance tests.
- ☐ Every `Approved` card has a "must NOT touch" list.
- ☐ Every card moving to Plan has Sections G (risks), H (cost and time), and I (release and undo plan) filled in.
- ☐ Every card with a High risk has a named human approver.
- ☐ Every card has a written "how do we undo it" answer before Launch.
- ☐ Every status uses only the allowed words.
- ☐ Every date is written as YYYY-MM-DD.
- ☐ The "Customers when asked" and "Launch-by customer count" fields are filled in.
- ☐ The "Current number of customers" in Part 1 is up to date.

---

# Part 6: Register Change Log

| Date | Who | What changed |
|---|---|---|
| YYYY-MM-DD | | Register created from template v1.1 |
