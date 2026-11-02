# HOW TO FILL THIS DOCUMENT (READ THIS FIRST — 3 MINUTES)

**What this is:** A questionnaire that helps you decide one thing: **"Is our product ready to launch, and ready to serve our first 500 customers?"** Your answer is one of three words: **GO**, **CONDITIONAL GO**, or **NO-GO**.

**Who can fill it:** Anyone. If you can read a question and answer *Yes / Partly / No*, you can fill this in. A solo founder can be every role. A team can split the sections.

## The 7 Rules

1. **Answer every question.** Never leave a blank. If a question does not apply, write `N/A` and one short reason.
2. **Use the answer scale exactly as shown.**
   - `2` = **Yes, done, and I can show proof**
   - `1` = **Partly done** (explain what is missing)
   - `0` = **No, not done**
   - `N/A` = Does not apply (write why)
3. **Proof beats opinion.** For every `2`, paste a link, file name, screenshot name, or test result in the **Proof** column. No proof = score it `1` at most.
4. **Never guess.** If you do not know, write `UNKNOWN`, then find out. `UNKNOWN` counts as `0` until resolved.
5. **Every `0` or `1` needs an Owner and a Due date** in the **Fix** column. Name a person, not "the team".
6. **Hard Blockers (Section 5) override everything.** One `No` there = **NO-GO**, even if the score is perfect.
7. **Write dates as `YYYY-MM-DD`** (example: `2026-11-03`). Write times with a timezone (example: `14:00 UTC`).

## Where to write answers
- Replace text inside `[square brackets]` with your answer.
- In checkbox lists, change `[ ]` to `[x]` to tick.
- In tables, type in the empty cells. Do not delete columns.

## How long it takes
| Project size | Time to fill |
|---|---|
| Solo / tiny project | 60–90 minutes |
| Small team (2–3 people) | 45 minutes each, then 30-minute review together |

## When to use this document (the 4 Gates)
You fill this document **once per gate**. Copy the Gate Decision block (Section 11) each time and keep old ones as history.

| Gate | Name | Question it answers | When |
|---|---|---|---|
| **G0** | Build Complete | Is the product built well enough to show real people? | End of development |
| **G1** | Private Beta | Is it safe to let the first 10–50 invited users in? | Before beta invites |
| **G2** | Public Launch | Is it safe to open the doors to everyone? | Before launch day |
| **G3** | Scale to 500 | Can we keep going toward customer #500 without breaking? | At customers 50, 100, 250, 500 |

## Words used in this document (plain English)
- **Go / No-Go:** Yes, launch / No, do not launch.
- **Blocker:** A problem so serious that launching is not allowed until it is fixed.
- **Rollback:** Going back to the last working version if the launch breaks something.
- **Activation:** The moment a new customer first gets real value (you define it in Section 3).
- **Churn:** Customers who leave.
- **AI agent:** A software assistant (like Claude) that writes code, tests, or documents for you.
- **Kill switch:** A button or setting that instantly turns a feature or the whole product off.

---

# 1. DOCUMENT CONTROL

| Field | Your answer |
|---|---|
| Project name | [ ] |
| Product one-line name | [ ] |
| Document version | [v1.0] |
| Gate this document is for | [ ] G0  [ ] G1  [ ] G2  [ ] G3 |
| Date filled in | [YYYY-MM-DD] |
| Filled in by (name + role) | [ ] |
| Planned launch date | [YYYY-MM-DD] |
| Go/No-Go decision meeting date and time | [YYYY-MM-DD HH:MM TZ] |
| Final decision owner (one person only) | [ ] |
| Where is the product code stored? (link) | [ ] |
| Where is the project plan or task board? (link) | [ ] |
| Is this a first launch or an update? | [ ] First launch  [ ] Major update  [ ] Re-launch |

---

# 2. PRODUCT SNAPSHOT

Answer in plain words. A stranger should understand your product after reading this section.

| Question | Your answer |
|---|---|
| In ONE sentence, what does the product do? | [ ] |
| Who is it for? (one specific type of person) | [ ] |
| What problem does it solve for them? | [ ] |
| What do people do today instead? | [ ] |
| Why will they pick yours? (one reason) | [ ] |
| How do you make money? | [ ] Free  [ ] Subscription  [ ] One-time purchase  [ ] Usage-based  [ ] Ads  [ ] Other: [ ] |
| Price (write the exact number or "Free") | [ ] |

**Which platforms are you launching on? (tick all that apply)**
- [ ] Web / SaaS app
- [ ] iOS app
- [ ] Android app
- [ ] API / developer product (other people's software connects to yours)
- [ ] Other: [ ]

> Sections 6-P1, 6-P2 and 6-P3 are platform-specific. Complete only the ones you ticked. Mark the others `N/A`.

**How was the product built? (tick all that apply)**
- [ ] Written by humans only
- [ ] Written mostly by humans with AI help (autocomplete, chat)
- [ ] Written mostly by AI agents with human review
- [ ] Written by AI agents with little or no human review *(Section 6-B becomes extra important)*

---

# 3. LAUNCH GOALS AND THE FIRST-500-CUSTOMERS PLAN

> Rule: a goal without a number is a wish. Every goal below needs a number and a date.

## 3.1 Define the words

| Term | Your definition (be specific) |
|---|---|
| **A "customer" is…** | [Example: someone who has paid at least once / signed up and used the product 1 time] |
| **"Activated" means…** | [Example: created their first project within 24 hours of signing up] |
| **"Retained" means…** | [Example: used the product again in the last 14 days] |
| **"Churned" means…** | [Example: cancelled, or no use for 30 days] |

## 3.2 Targets

| Milestone | Target number | Target date | How you will count it (tool or report) |
|---|---|---|---|
| Beta users invited | [ ] | [ ] | [ ] |
| Customer #10 | 10 | [ ] | [ ] |
| Customer #50 | 50 | [ ] | [ ] |
| Customer #100 | 100 | [ ] | [ ] |
| Customer #250 | 250 | [ ] | [ ] |
| **Customer #500** | **500** | [ ] | [ ] |

## 3.3 Success numbers (fill in real numbers, then use them in Section 12)

| Measure | Minimum acceptable | Target | Where you read it |
|---|---|---|---|
| Visitors-to-signup rate | [ ]% | [ ]% | [ ] |
| Signup-to-activated rate | [ ]% | [ ]% | [ ] |
| Free-to-paid rate (if applicable) | [ ]% | [ ]% | [ ] |
| Week-4 retention | [ ]% | [ ]% | [ ] |
| Monthly churn | max [ ]% | max [ ]% | [ ] |
| Cost to get one customer (CAC) | max [ ] | [ ] | [ ] |
| Customer support tickets per 100 customers | max [ ] | [ ] | [ ] |
| Uptime | [99.5]% | [99.9]% | [ ] |
| Page or screen load time | under [ ] sec | under [ ] sec | [ ] |
| Customer satisfaction (rating or score) | [ ] | [ ] | [ ] |

## 3.4 Budget and limits

| Question | Your answer |
|---|---|
| Total launch budget | [ ] |
| Maximum monthly running cost (servers, tools, AI usage) at 500 customers | [ ] |
| Is the price high enough to cover that running cost per customer? | [ ] Yes  [ ] No  [ ] Unknown |
| Who is working on launch, and how many hours per week? | [ ] |

---

# 4. ROLES AND SIGN-OFF PEOPLE

> **Solo founder?** Write your own name in every row. That is fine. The point is to look at the product through each lens, one at a time.
> **Team?** One person can hold several roles. Each role must have exactly one named person.

| Role | What this person checks | Name | Backup person |
|---|---|---|---|
| **Decision Owner** | Makes the final Go / No-Go call | [ ] | [ ] |
| **Product Owner** | The product does what we promised | [ ] | [ ] |
| **Engineering Lead** | It is built well, deployed, and can be fixed fast | [ ] | [ ] |
| **QA / Testing Lead** | It was tested and known bugs are acceptable | [ ] | [ ] |
| **Security & Privacy Lead** | Customer data is protected | [ ] | [ ] |
| **Marketing Lead** | The message, pages and channels are ready | [ ] | [ ] |
| **Support Lead** | Someone can answer customers quickly | [ ] | [ ] |
| **Finance / Payments Lead** | Billing works and money flows correctly | [ ] | [ ] |
| **Legal / Compliance Lead** | Terms, privacy and rules are covered | [ ] | [ ] |
| **On-Call Person on Launch Day** | Fixes emergencies; reachable by phone | [ ] | [ ] |

## Who does what? (RACI chart)

> **R** = Responsible (does the work) · **A** = Accountable (final say; only ONE per row) · **C** = Consulted (asked for advice before) · **I** = Informed (told afterward).
> Write a letter in each cell, or `-` if the person is not involved. Every row must have exactly one **A**.
> **Solo founder?** Write `A/R` for yourself in every row and skip the rest.

| Task | Decision Owner | Product | Engineering | QA | Security | Marketing | Support | Legal | Finance |
|---|---|---|---|---|---|---|---|---|---|
| Final Go / No-Go | A | C | C | C | C | C | C | C | I |
| Fix blockers (Section 5) | I | C | A/R | R | R | I | I | C | I |
| Run tests and report bugs | I | C | R | A/R | C | - | I | - | - |
| Security and privacy checks | I | C | R | C | A/R | - | - | C | - |
| Launch messages and posts | I | C | - | - | - | A/R | C | C | - |
| Payments and billing | I | C | R | R | C | I | I | C | A |
| Customer support setup | I | C | C | - | - | C | A/R | - | - |
| Rollback if things break | A | I | R | R | C | I | I | - | - |
| Customer-facing announcements about problems | A | C | C | - | - | R | R | C | - |
| Checkpoint reviews (Section 12) | A | R | C | - | - | R | R | - | C |

> Your own row: [Task] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ]

**Who works on launch day, and how do we reach them?**

| Name | Phone or chat handle | Available hours (with timezone) |
|---|---|---|
| [ ] | [ ] | [ ] |

---

# 5. HARD BLOCKERS (ANY "NO" = NO-GO)

> Answer **Yes** or **No** only. No "partly" here. If the answer is **No**, you are not allowed to launch until it becomes **Yes**. Write the proof or the fix.

| # | Blocker question | Yes / No | Proof (link, file, screenshot name) or Fix (owner + date) |
|---|---|---|---|
| B1 | Can a brand-new person complete the main journey (sign up → get the core value) without help and without errors? | [ ] | [ ] |
| B2 | Have you personally tested the main journey on the real production system (not only on a test copy) in the last 48 hours? | [ ] | [ ] |
| B3 | Are there zero open bugs that lose data, expose private data, charge the wrong amount, or crash the app? | [ ] | [ ] |
| B4 | Is customer data protected: passwords stored safely (never in plain text), connections encrypted (HTTPS), and secrets (keys, tokens) not stored in the code? | [ ] | [ ] |
| B5 | Do automatic backups exist, and has a restore been tested at least once successfully? | [ ] | [ ] |
| B6 | Is there a written rollback plan (Section 9) that someone has practiced or walked through? | [ ] | [ ] |
| B7 | Can you take the product (or the risky feature) offline within 5 minutes (kill switch)? | [ ] | [ ] |
| B8 | If you charge money: does a real test payment, refund and cancellation work end to end? *(Free product? Write "N/A — free".)* | [ ] | [ ] |
| B9 | Do the Privacy Policy and Terms of Service exist, are they published at a public link, and do they match what the product actually does? | [ ] | [ ] |
| B10 | Is there a working way for customers to reach a human (email, form or chat), and will someone read it within 24 hours? | [ ] | [ ] |
| B11 | Will you be alerted automatically (email, phone or chat) if the product goes down or errors spike? | [ ] | [ ] |
| B12 | Is a named person available and reachable during the first 72 hours after launch? | [ ] | [ ] |
| B13 | Does everything you claim in marketing (pages, ads, store listing) match what the product truly does today? | [ ] | [ ] |
| B14 | If AI agents wrote any of the code: has a human reviewed all code touching logins, payments, personal data and permissions? *(No AI-written code? Write "N/A".)* | [ ] | [ ] |
| B15 | Are you legally allowed to launch in every country or store you are targeting (checked, not assumed)? | [ ] | [ ] |

**Blocker result (count them):**
- Number of `No` answers: [ ]
- If the number is greater than 0 → **STOP. The decision is NO-GO.** Fix the items and fill this section again.

---

# 6. READINESS SCORECARD

> **How to score each question:** `2` = Yes with proof · `1` = Partly · `0` = No · `N/A` = does not apply.
> **Fix column:** Required for every `0` and `1`. Format: `Owner — Due date — Action`.
> Add your own questions at the end of any area if your project needs them.

## 6-A. Product and Features

| # | Question | Score | Proof | Fix (Owner — Date — Action) |
|---|---|---|---|---|
| A1 | Is there a written list of what is IN the launch and what is NOT in the launch? | [ ] | [ ] | [ ] |
| A2 | Does every promised feature work as described? | [ ] | [ ] | [ ] |
| A3 | Have at least 5 people outside the builders used it and finished the main journey? | [ ] | [ ] | [ ] |
| A4 | Are empty states, error messages and loading states written in plain, friendly words? | [ ] | [ ] | [ ] |
| A5 | Can a customer delete their account and data, or export their data? | [ ] | [ ] | [ ] |
| A6 | Is the product usable by people with common accessibility needs (readable text size, color contrast, keyboard use)? | [ ] | [ ] | [ ] |
| A7 | Is there a short list of "known issues we are launching with" that you are honestly OK with? | [ ] | [ ] | [ ] |
| A8 | Is there a one-page list of features you will add next, so launch day questions have an answer? | [ ] | [ ] | [ ] |

## 6-B. AI-Assisted Development Quality (skip rows only if no AI wrote code)

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| B-1 | Is every AI-generated change reviewed by a human or by a separate review step before it reaches production? | [ ] | [ ] | [ ] |
| B-2 | Does the project have written instructions for AI agents (rules, folder map, how to run tests, what is forbidden)? | [ ] | [ ] | [ ] |
| B-3 | Do automated tests run on every change, and must they pass before release? | [ ] | [ ] | [ ] |
| B-4 | Were AI-suggested software packages and libraries checked to be real, maintained and safely licensed? | [ ] | [ ] | [ ] |
| B-5 | Was the code scanned for leaked secrets (keys, passwords, tokens)? | [ ] | [ ] | [ ] |
| B-6 | Was the code scanned for known security weaknesses (automated scanner or manual review)? | [ ] | [ ] | [ ] |
| B-7 | Can you explain, in plain words, how login, payments and data storage work in your product (not just "the AI did it")? | [ ] | [ ] | [ ] |
| B-8 | Is there a history of every release (who or what changed what, and when) so you can undo a bad change? | [ ] | [ ] | [ ] |
| B-9 | Do AI agents have limited permissions (they cannot delete production data or deploy without approval)? | [ ] | [ ] | [ ] |
| B-10 | Are the AI tools and prompts used to build the product saved somewhere so the work can be repeated by someone else? | [ ] | [ ] | [ ] |

## 6-C. Quality Assurance and Testing

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| C1 | Is there a written test checklist for the main journeys (sign up, log in, core action, pay, cancel, log out)? | [ ] | [ ] | [ ] |
| C2 | Did every item on that checklist pass in the latest version? | [ ] | [ ] | [ ] |
| C3 | Are there automated tests for the most important logic? | [ ] | [ ] | [ ] |
| C4 | Have you tested with bad input (blank fields, very long text, special characters, wrong file types)? | [ ] | [ ] | [ ] |
| C5 | Have you tested on slow internet and on small screens? | [ ] | [ ] | [ ] |
| C6 | Have you tested what happens when many people use it at once (load test), at least 3× your expected day-one traffic? | [ ] | [ ] | [ ] |
| C7 | Are all bugs listed in one place, with severity (Critical / High / Medium / Low)? | [ ] | [ ] | [ ] |
| C8 | Count of open bugs: Critical = [ ] High = [ ] Medium = [ ] Low = [ ]. Is Critical = 0 and High = 0 or accepted in writing? | [ ] | [ ] | [ ] |
| C9 | Were emails, notifications and receipts tested (they arrive, are not marked as spam, and look right)? | [ ] | [ ] | [ ] |

## 6-D. Security and Privacy

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| D1 | Can one customer ever see another customer's data? (Tested on purpose: try it.) | [ ] | [ ] | [ ] |
| D2 | Are login protections in place (strong password rules, limits on repeated wrong tries, password reset that is safe)? | [ ] | [ ] | [ ] |
| D3 | Is two-step login (2FA) available for customers and REQUIRED for your own admin accounts? | [ ] | [ ] | [ ] |
| D4 | Are admin tools hidden from normal customers and protected? | [ ] | [ ] | [ ] |
| D5 | Is a list kept of exactly what personal data you collect, why, and where it is stored? | [ ] | [ ] | [ ] |
| D6 | Do you collect only the data you truly need? | [ ] | [ ] | [ ] |
| D7 | Is there a plan for what to do if data leaks (who to tell, within how many hours, what to say)? | [ ] | [ ] | [ ] |
| D8 | Do third-party tools (analytics, payments, email) have only the access they need? | [ ] | [ ] | [ ] |
| D9 | Are old test accounts, test data and test keys removed from production? | [ ] | [ ] | [ ] |
| D10 | If your product has an API: are keys required, can they be revoked, and are request limits in place? | [ ] | [ ] | [ ] |

## 6-E. Legal, Compliance and Business Setup

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| E1 | Is a legal business or entity set up that can accept money and sign terms? | [ ] | [ ] | [ ] |
| E2 | Are the Terms of Service, Privacy Policy and (if needed) Refund Policy and Cookie notice live and linked in the product and footer? | [ ] | [ ] | [ ] |
| E3 | Have you checked privacy laws that apply to your customers' locations (for example GDPR, CCPA, or local equivalents)? Write which ones: [ ] | [ ] | [ ] | [ ] |
| E4 | If children could use the product, have you checked child-privacy rules and age limits? | [ ] | [ ] | [ ] |
| E5 | Do you have the right to use all images, fonts, music, code and data in the product (licenses saved)? | [ ] | [ ] | [ ] |
| E6 | Is your product name, logo and domain free from obvious conflicts with others (a basic search was done)? | [ ] | [ ] | [ ] |
| E7 | Are taxes (sales tax, VAT) handled, or is a tool or advisor lined up? | [ ] | [ ] | [ ] |
| E8 | Does your industry have special rules (health, finance, education, kids, etc.)? If yes, write them here: [ ] | [ ] | [ ] | [ ] |
| E9 | Are emails and marketing messages allowed by anti-spam rules (consent, unsubscribe link, sender address)? | [ ] | [ ] | [ ] |

## 6-F. Infrastructure, Performance and Reliability

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| F1 | Is the production system separate from test and development systems? | [ ] | [ ] | [ ] |
| F2 | Can the system handle 10× your expected day-one users without failing (or does it grow automatically)? | [ ] | [ ] | [ ] |
| F3 | Do you know the monthly cost at 100, 250 and 500 customers? Write them: [ ] | [ ] | [ ] | [ ] |
| F4 | Are spending alerts set so a surprise bill cannot happen (hosting, AI usage, email, SMS)? | [ ] | [ ] | [ ] |
| F5 | Is the domain name renewed for at least 1 year, and are the SSL/HTTPS certificates set to renew automatically? | [ ] | [ ] | [ ] |
| F6 | Is email sending set up correctly (sender verification) so messages reach inboxes? | [ ] | [ ] | [ ] |
| F7 | Can you deploy a fix to production in under 30 minutes? | [ ] | [ ] | [ ] |
| F8 | Are all accounts for hosting, domain, payments and code storage owned by the company (not a personal login of one person) and documented in a safe place? | [ ] | [ ] | [ ] |
| F9 | Is there a "status page" or a simple way to tell customers when something is down? | [ ] | [ ] | [ ] |

## 6-G. Monitoring, Analytics and Data

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| G1 | Do you track errors (a tool tells you when the product breaks)? | [ ] | [ ] | [ ] |
| G2 | Do you track uptime with alerts to a real person? | [ ] | [ ] | [ ] |
| G3 | Do you track the steps from visitor → signup → activated → paid? | [ ] | [ ] | [ ] |
| G4 | Do you know where each new customer came from (which channel)? | [ ] | [ ] | [ ] |
| G5 | Is there ONE dashboard (or one page) showing the numbers from Section 3.3, updated at least daily? | [ ] | [ ] | [ ] |
| G6 | Are analytics tools consent-compliant (cookie notice where required)? | [ ] | [ ] | [ ] |
| G7 | Did you test that tracking numbers are correct (sign up yourself and check it was counted once)? | [ ] | [ ] | [ ] |

## 6-H. Payments and Billing (write N/A for all rows if free)

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| H1 | Is the payment provider account fully approved for live payments (not test mode)? | [ ] | [ ] | [ ] |
| H2 | Did a real payment of a small amount succeed in live mode, and was it refunded successfully? | [ ] | [ ] | [ ] |
| H3 | Do upgrade, downgrade, cancel, and failed-payment flows work? | [ ] | [ ] | [ ] |
| H4 | Do customers get receipts or invoices automatically? | [ ] | [ ] | [ ] |
| H5 | Is the price shown the same everywhere (website, store listing, checkout)? | [ ] | [ ] | [ ] |
| H6 | Is there a refund and cancellation policy that customers can find in 2 clicks? | [ ] | [ ] | [ ] |
| H7 | Is there a plan for failed payments (retry emails, grace period)? | [ ] | [ ] | [ ] |

## 6-I. Customer Support and Documentation

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| I1 | Is there a Help or FAQ page covering the top 10 questions you expect? | [ ] | [ ] | [ ] |
| I2 | Is there a "Getting Started" guide (text, video or both) that a first-time user can follow in under 10 minutes? | [ ] | [ ] | [ ] |
| I3 | Is there one support inbox or tool, and is a person assigned to check it every day? | [ ] | [ ] | [ ] |
| I4 | Do you have ready-made reply templates for common issues (login problem, refund, bug report, feature request)? | [ ] | [ ] | [ ] |
| I5 | Is the promised reply time written down? Write it: [ ] hours | [ ] | [ ] | [ ] |
| I6 | Is there a way to collect bug reports and feedback inside the product or by one simple form? | [ ] | [ ] | [ ] |
| I7 | Is there a written rule for what counts as an emergency and who gets woken up? | [ ] | [ ] | [ ] |
| I8 | For API products: are the docs complete, with working copy-paste examples and an error-code list? | [ ] | [ ] | [ ] |

## 6-J. Marketing Message and Assets

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| J1 | Is there a clear "who it is for + what it does + why it is different" message, tested on at least 5 people from your target group? | [ ] | [ ] | [ ] |
| J2 | Is the landing page live, fast, and does it have ONE clear action button? | [ ] | [ ] | [ ] |
| J3 | Does the landing page show proof (testimonials, demo, numbers, screenshots, logos)? Never invent proof. | [ ] | [ ] | [ ] |
| J4 | Are the pricing page, FAQ and "About" page live? | [ ] | [ ] | [ ] |
| J5 | Are launch assets ready (logo, screenshots, demo video or GIF, short and long descriptions)? | [ ] | [ ] | [ ] |
| J6 | Are social pages and a shared email address set up under the product name? | [ ] | [ ] | [ ] |
| J7 | Are the launch announcement posts and emails written, proofread, and scheduled? | [ ] | [ ] | [ ] |
| J8 | Is there a press or community kit (one-paragraph story, founder bio, product images, contact)? | [ ] | [ ] | [ ] |
| J9 | Are the page titles and descriptions set so search engines show them properly (basic SEO), and is the site allowed to be found? | [ ] | [ ] | [ ] |
| J10 | Do shared links show a proper preview image and title (test on 2 platforms)? | [ ] | [ ] | [ ] |

## 6-K. Customer Acquisition Channels (the path to 500)

> List every channel you will use. Pick **no more than 3 main channels** at the start. Many channels at once means none work well.

| Channel | Why it fits your customer | Planned action | Weekly effort (hours) | Goal (visitors or signups) | Owner | Ready? (2/1/0) |
|---|---|---|---|---|---|---|
| [Example: Email list] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Example: Social posts] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Example: Community posts] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Example: Product directories] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Example: Partnerships] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Example: Paid ads] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Example: Content or search] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| [Example: Direct outreach to people] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| K1 | Do you already have a list of at least [ ] people who asked to hear about the launch (waitlist, email list, followers)? | [ ] | [ ] | [ ] |
| K2 | Can you name 20 specific people or places where your target customers gather, and the plan to reach them? | [ ] | [ ] | [ ] |
| K3 | Is there a simple estimate showing how your channels can reach 500 customers (visitors × signup rate × activation rate)? | [ ] | [ ] | [ ] |
| K4 | If you use paid ads: is a small test budget set, with a stop-loss limit (stop if cost per customer goes above [ ])? | [ ] | [ ] | [ ] |
| K5 | Are tracking links set up for every channel so you know which one works? | [ ] | [ ] | [ ] |
| K6 | Is there a plan to ask the first happy customers for reviews, testimonials or referrals? | [ ] | [ ] | [ ] |

## 6-L. Onboarding and Activation

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| L1 | After signing up, is the next step obvious, and does the user reach the first value in under [ ] minutes? | [ ] | [ ] | [ ] |
| L2 | Is there a welcome email (or message) sent automatically within 5 minutes of signup? | [ ] | [ ] | [ ] |
| L3 | Is there a follow-up message for people who sign up but do not activate (day 1, day 3, day 7)? | [ ] | [ ] | [ ] |
| L4 | Is there a plan to talk personally to your first 20 customers (calls or messages) to learn what confuses them? | [ ] | [ ] | [ ] |
| L5 | Is there a feedback question at a natural moment ("How is it going?")? | [ ] | [ ] | [ ] |
| L6 | Is there a "win-back" message for customers who leave? | [ ] | [ ] | [ ] |

## 6-M. Team Readiness and Operations

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| M1 | Does everyone know their job on launch day (Section 8 is shared and read)? | [ ] | [ ] | [ ] |
| M2 | Is anyone planning vacation, travel, or other unavailability in the first 2 weeks after launch? If yes, who covers? | [ ] | [ ] | [ ] |
| M3 | Is there a quiet "rest plan" so people are not exhausted by week 2? | [ ] | [ ] | [ ] |
| M4 | Is the way of communicating on launch day agreed (one chat channel, one call link)? | [ ] | [ ] | [ ] |
| M5 | Is there a short written how-to for the 5 most likely emergencies (site down, payments failing, login broken, email not sending, data bug)? | [ ] | [ ] | [ ] |
| M6 | Is all important knowledge written down so no single person is the only one who knows how it works? | [ ] | [ ] | [ ] |

## 6-P1. Web / SaaS Extras (write N/A if not a web product)

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| P1-1 | Does it work on the latest versions of Chrome, Safari, Firefox and Edge? | [ ] | [ ] | [ ] |
| P1-2 | Does it work well on phones and tablets in the browser? | [ ] | [ ] | [ ] |
| P1-3 | Does the signup form work with password managers and "Sign in with…" options you offer? | [ ] | [ ] | [ ] |
| P1-4 | Are your custom 404 (page not found) and error pages friendly? | [ ] | [ ] | [ ] |
| P1-5 | Is the site safe from being embedded or copied by others (basic security headers set)? | [ ] | [ ] | [ ] |
| P1-6 | If you have teams or workspaces: can an admin invite and remove members, and do roles work correctly? | [ ] | [ ] | [ ] |

## 6-P2. Mobile App Extras (write N/A if no mobile app)

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| P2-1 | Is the app submitted AND approved by the app store(s), with the release set for the right date? *(Review can take days. Submit early.)* | [ ] | [ ] | [ ] |
| P2-2 | Are store listing items complete (name, icon, screenshots for all required sizes, description, keywords, age rating, privacy details)? | [ ] | [ ] | [ ] |
| P2-3 | Have you tested on at least 3 different real devices and 2 OS versions? | [ ] | [ ] | [ ] |
| P2-4 | Does the app behave well with no internet, weak internet, and when switching apps? | [ ] | [ ] | [ ] |
| P2-5 | Are permissions (camera, location, notifications) asked at a sensible moment with a clear reason? | [ ] | [ ] | [ ] |
| P2-6 | Does in-app purchase follow store rules (if you sell digital items)? | [ ] | [ ] | [ ] |
| P2-7 | Is there a way to force users on a broken old version to update? | [ ] | [ ] | [ ] |
| P2-8 | Is crash reporting working in the release build? | [ ] | [ ] | [ ] |
| P2-9 | Do push notifications work and can users turn them off? | [ ] | [ ] | [ ] |

## 6-P3. API / Developer Product Extras (write N/A if no API)

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| P3-1 | Is the API documented with every endpoint, input, output and error? | [ ] | [ ] | [ ] |
| P3-2 | Is the API versioned so you can change it later without breaking existing users? | [ ] | [ ] | [ ] |
| P3-3 | Are rate limits and fair-use rules set and explained? | [ ] | [ ] | [ ] |
| P3-4 | Is there a free test environment (sandbox) for developers? | [ ] | [ ] | [ ] |
| P3-5 | Are there working code examples or SDKs in the top languages your users need? | [ ] | [ ] | [ ] |
| P3-6 | Is there a public changelog and a plan to warn users before breaking changes? | [ ] | [ ] | [ ] |
| P3-7 | Is there a developer support path (docs search, community, email) with a promised reply time? | [ ] | [ ] | [ ] |

## 6-N. Accessibility and Localization

> **Example of a good answer:** N1 → Score `2`, Proof: `accessibility-check-2026-11-01.pdf (all pages pass, no serious issues)`.

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| N1 | Has an accessibility checker been run on the main pages and screens, and were serious issues fixed? | [ ] | [ ] | [ ] |
| N2 | Can the main journey be completed using only a keyboard (web) or a screen reader (web and mobile)? | [ ] | [ ] | [ ] |
| N3 | Do text and buttons have enough contrast and readable size, and do images have text descriptions? | [ ] | [ ] | [ ] |
| N4 | Does the product work when a user sets a larger system font size or reduced motion? | [ ] | [ ] | [ ] |
| N5 | Which languages and countries are you launching in? Write them: [ ] Are all customer-facing words (product, emails, help pages, store listing) available in each? | [ ] | [ ] | [ ] |
| N6 | Are dates, times, numbers, currencies and time zones shown correctly for each country? | [ ] | [ ] | [ ] |
| N7 | Does the layout survive longer text (German, Finnish) and right-to-left languages (Arabic, Hebrew), if you support them? | [ ] | [ ] | [ ] |
| N8 | Can customers in each country actually pay (supported currencies and payment methods)? | [ ] | [ ] | [ ] |
| N9 | Is support available in the languages and hours you promise? | [ ] | [ ] | [ ] |

## 6-O. Pricing and Packaging

> **Example of a good answer:** O2 → Score `1`, Proof: `12 interviews: 8 said $15/mo is fair`, Fix: `Sam — 2026-11-05 — ask 8 more people`.

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| O1 | Are your plans, prices and limits written in one table (what each plan includes)? | [ ] | [ ] | [ ] |
| O2 | Have at least 10 people from your target group told you what they would pay (not just "sounds good")? | [ ] | [ ] | [ ] |
| O3 | Is the price above your running cost per customer (Section 3.4), with room for support, fees and tax? | [ ] | [ ] | [ ] |
| O4 | Are free-plan and trial limits clear, and do they push people to upgrade only after they feel value? | [ ] | [ ] | [ ] |
| O5 | Are discount, coupon and launch-offer rules written down (who, how much, until when, can it be abused)? | [ ] | [ ] | [ ] |
| O6 | Is it clear what happens when a customer goes over a limit (blocked, warned, or charged)? | [ ] | [ ] | [ ] |
| O7 | Do you have a plan to change prices later without upsetting early customers (for example price lock for first 100)? | [ ] | [ ] | [ ] |
| O8 | Is there one pricing page and one checkout showing the same plans and the same prices? | [ ] | [ ] | [ ] |

## 6-P4. AI/LLM Features Inside Your Product (optional — write N/A for all rows if your product has no AI features)

> This block is about AI that **your customers use**, not AI that helped you build the product (that is 6-B).

| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| P4-1 | Is there a test set of at least 50 realistic questions or tasks with known good answers, and does the AI pass your minimum rate? Write it: [ ]% | [ ] | [ ] | [ ] |
| P4-2 | Have you tested what the AI does when it does not know (does it admit it, or make things up)? | [ ] | [ ] | [ ] |
| P4-3 | Have you tried to trick it (hidden instructions in user text or files, requests to leak its rules or other users' data)? | [ ] | [ ] | [ ] |
| P4-4 | Does it refuse unsafe, illegal or harmful requests, and is the refusal message friendly? | [ ] | [ ] | [ ] |
| P4-5 | Is private customer data kept out of other customers' answers, and are you sure what data is sent to the AI provider? | [ ] | [ ] | [ ] |
| P4-6 | Does the product clearly tell users when they are talking to AI, and warn that results can be wrong where it matters? | [ ] | [ ] | [ ] |
| P4-7 | Are there limits per user (requests, length) and a cost alert so one customer cannot create a huge bill? | [ ] | [ ] | [ ] |
| P4-8 | Do you know the average AI cost per customer per month, and does your price cover it? | [ ] | [ ] | [ ] |
| P4-9 | If the AI provider is slow, down, or changes the model, does the product still work gracefully (fallback message or backup)? | [ ] | [ ] | [ ] |
| P4-10 | Can you turn the AI feature off alone (kill switch) without taking down the whole product? | [ ] | [ ] | [ ] |
| P4-11 | Can users report a bad AI answer in one click, and does someone review those reports weekly? | [ ] | [ ] | [ ] |
| P4-12 | Are the prompts, model name and version saved and tracked like code, so a change can be undone? | [ ] | [ ] | [ ] |

---

# 7. RISK REGISTER

> List what could go wrong. A risk you wrote down is a risk you can handle. Rate each from 1 (low) to 3 (high).
> **Risk score = Chance × Damage.** Any score of 6 or 9 needs a prevention plan AND a backup plan.

| # | What could go wrong? | Chance (1-3) | Damage (1-3) | Score | How we prevent it | What we do if it happens | Owner |
|---|---|---|---|---|---|---|---|
| R1 | Too many visitors crash the product | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R2 | Payments fail on launch day | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R3 | A security or data leak happens | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R4 | A bad release breaks the product | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R5 | Nobody shows up (low traffic or signups) | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R6 | Customers sign up but do not activate | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R7 | Costs spike (hosting, AI usage, ads) | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R8 | App store rejects or delays the app | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R9 | Key person gets sick or unreachable | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R10 | Negative public reaction or review wave | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R11 | AI-written code contains a hidden bug or weakness | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R12 | A third-party service we depend on goes down | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R13 | [Add your own] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

**Third-party services we depend on (if any one fails, what happens?)**

| Service | What it does for us | If it goes down, we… | Status page link |
|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] |

---

# 8. LAUNCH DAY PLAN (HOUR BY HOUR)

> Write real times. Each line needs one person and one clear action. Add rows as needed.

| When | Action | Owner | Done? |
|---|---|---|---|
| **T-7 days** | Code freeze: no new features, bug fixes only | [ ] | [ ] |
| T-7 days | Final full test of main journeys on production | [ ] | [ ] |
| T-3 days | Confirm backups, alerts and on-call schedule | [ ] | [ ] |
| T-3 days | Schedule all announcements and emails | [ ] | [ ] |
| **T-1 day** | Hold the Go / No-Go meeting (Section 11) | [Decision Owner] | [ ] |
| T-1 day | Share this plan with everyone involved | [ ] | [ ] |
| T-1 day | Sleep and rest | Everyone | [ ] |
| **T-2 hours** | Final test: sign up, pay, log out, log in | [ ] | [ ] |
| T-1 hour | Open dashboard and chat channel | [ ] | [ ] |
| **T-0 (launch)** | Switch product live / publish announcement | [ ] | [ ] |
| T+15 min | Test the live product again from a clean device | [ ] | [ ] |
| T+1 hour | Check errors, signups, payments, speed | [ ] | [ ] |
| T+4 hours | Reply to every comment and support message | [ ] | [ ] |
| T+8 hours | Status note to the team: numbers + problems | [ ] | [ ] |
| T+24 hours | Launch day review (Section 13, first half) | [ ] | [ ] |
| T+72 hours | 3-day health check against Section 12 | [ ] | [ ] |

**During launch, who has the authority to say "STOP, roll back"?** [Name — one person]
**How will they tell everyone?** [Chat channel or call link]

---

# 9. ROLLBACK AND EMERGENCY PLAN

| Question | Your answer |
|---|---|
| What is the exact step-by-step way to go back to the last working version? | [Write numbered steps. Another person must be able to follow them.] |
| How long does it take? | [ ] minutes |
| Have you practiced this at least once? | [ ] Yes, date: [ ]  [ ] No |
| Where is the kill switch and who can press it? | [ ] |
| What will you tell customers if something breaks? (write the message now) | [ ] |
| Where will you post status updates? | [ ] |
| Who do you call if the main person is unreachable? | [ ] |
| What will we do if a data leak is suspected? (first 3 steps) | 1. [ ] 2. [ ] 3. [ ] |

**Rollback triggers: roll back immediately if any of these happen**
- [ ] Customers cannot log in for more than [ ] minutes
- [ ] Payments fail for more than [ ] % of attempts
- [ ] Error rate is above [ ] %
- [ ] Any report of one customer seeing another customer's data
- [ ] [Add your own]

---

# 10. SCORE CALCULATION

> Do this after finishing Section 6. A spreadsheet or calculator helps. An AI agent can do the math for you (see Appendix B).

**Step 1: Count your scores for each area. Skip all `N/A` rows.**

| Area | Questions scored (not N/A) | Maximum points (questions × 2) | Points earned | Area % (earned ÷ max × 100) |
|---|---|---|---|---|
| 6-A Product | [ ] | [ ] | [ ] | [ ]% |
| 6-B AI-Assisted Development | [ ] | [ ] | [ ] | [ ]% |
| 6-C QA and Testing | [ ] | [ ] | [ ] | [ ]% |
| 6-D Security and Privacy | [ ] | [ ] | [ ] | [ ]% |
| 6-E Legal and Business | [ ] | [ ] | [ ] | [ ]% |
| 6-F Infrastructure | [ ] | [ ] | [ ] | [ ]% |
| 6-G Monitoring and Data | [ ] | [ ] | [ ] | [ ]% |
| 6-H Payments | [ ] | [ ] | [ ] | [ ]% |
| 6-I Support and Docs | [ ] | [ ] | [ ] | [ ]% |
| 6-J Marketing | [ ] | [ ] | [ ] | [ ]% |
| 6-K Acquisition | [ ] | [ ] | [ ] | [ ]% |
| 6-L Onboarding | [ ] | [ ] | [ ] | [ ]% |
| 6-M Team | [ ] | [ ] | [ ] | [ ]% |
| 6-N Accessibility and Localization | [ ] | [ ] | [ ] | [ ]% |
| 6-O Pricing and Packaging | [ ] | [ ] | [ ] | [ ]% |
| 6-P1 / P2 / P3 Platform | [ ] | [ ] | [ ] | [ ]% |
| 6-P4 AI Features (optional) | [ ] | [ ] | [ ] | [ ]% |
| **TOTAL** | [ ] | [ ] | [ ] | **[ ]%** |

**Step 2: Apply the decision rules (edit the percentages below only once, for all projects, and write down why)**

| Condition | Result |
|---|---|
| Any Hard Blocker (Section 5) is `No` | **NO-GO** (always, no exceptions) |
| Total is 85% or higher AND every area is 70% or higher AND Security (6-D) is 85% or higher | **GO** |
| Total is 70-84%, OR one area is below 70% (but Security is 85% or higher) | **CONDITIONAL GO** (allowed only if every `0` and `1` has an Owner and a Due date, and nothing is a blocker) |
| Total is below 70%, OR Security (6-D) is below 85% | **NO-GO** |

**Step 3: Gate-specific minimums (the bar rises as the audience grows)**

| Gate | Minimum total for GO | Notes |
|---|---|---|
| G0 Build Complete | 60% | Focus on 6-A, 6-B, 6-C |
| G1 Private Beta | 75% | Focus on 6-C, 6-D, 6-G, 6-I |
| G2 Public Launch | 85% | All areas |
| G3 Scale to 500 | 85%, and all Section 12 health checks green | Focus on 6-F, 6-G, 6-I, 6-L |

**Your result**

| Item | Value |
|---|---|
| Blockers failed | [ ] |
| Total score | [ ]% |
| Lowest area and its score | [ ] — [ ]% |
| Security score | [ ]% |
| **Recommended decision (from the rules above)** | [ ] GO  [ ] CONDITIONAL GO  [ ] NO-GO |

---

# 11. GO / NO-GO DECISION RECORD

> Copy this section for each gate (G0, G1, G2, G3). Fill it in during the decision meeting. Keep every copy.

| Field | Your answer |
|---|---|
| Gate | [ ] G0  [ ] G1  [ ] G2  [ ] G3 |
| Meeting date and time | [ ] |
| People present | [ ] |
| Blockers failed (from Section 5) | [ ] |
| Total score (from Section 10) | [ ]% |
| Recommended decision | [ ] |
| **FINAL DECISION** | [ ] GO  [ ] CONDITIONAL GO  [ ] NO-GO |
| If different from the recommended decision, why? (required) | [ ] |
| Main reasons for this decision (max 3) | 1. [ ] 2. [ ] 3. [ ] |

**Conditions (only if CONDITIONAL GO). Every condition has an owner and a deadline.**

| # | Condition that must be true | Owner | Must be done by | Done? |
|---|---|---|---|---|
| 1 | [ ] | [ ] | [ ] | [ ] |
| 2 | [ ] | [ ] | [ ] | [ ] |

**If NO-GO: what must change, and when will we meet again?**
[ ]

**Sign-off (type your name and date; each person confirms they answered honestly)**

| Role | Name | Decision (Go / Conditional / No-Go) | Date | Comment |
|---|---|---|---|---|
| Decision Owner | [ ] | [ ] | [ ] | [ ] |
| Product Owner | [ ] | [ ] | [ ] | [ ] |
| Engineering Lead | [ ] | [ ] | [ ] | [ ] |
| QA Lead | [ ] | [ ] | [ ] | [ ] |
| Security & Privacy Lead | [ ] | [ ] | [ ] | [ ] |
| Marketing Lead | [ ] | [ ] | [ ] | [ ] |
| Support Lead | [ ] | [ ] | [ ] | [ ] |
| Legal / Compliance Lead | [ ] | [ ] | [ ] | [ ] |

> Solo founder? Sign each row separately, one role at a time, after you have actually looked at that area.

---

# 12. THE ROAD TO 500 CUSTOMERS — CHECKPOINTS

> Fill this in at each checkpoint. Each checkpoint asks: *Are we healthy enough to keep growing?* Use the numbers from Section 3.3.
> **Traffic-light rule:** 🟢 Green = at or better than target · 🟡 Yellow = between minimum and target · 🔴 Red = worse than minimum.
> **Any red = pause paid growth and fix before continuing. Two or more yellows in a row = review the plan.**

## 12.1 Checkpoint table (copy one block per milestone)

### Checkpoint: Customer #10 / #50 / #100 / #250 / #500 (circle one)

| Item | Date | [ ] |
|---|---|---|
| Date reached | [ ] | |
| Days since public launch | [ ] | |

| Measure | Minimum | Target | Actual | Light (🟢🟡🔴) |
|---|---|---|---|---|
| Signup → activated rate | [ ]% | [ ]% | [ ]% | [ ] |
| Free → paid rate | [ ]% | [ ]% | [ ]% | [ ] |
| Week-4 retention | [ ]% | [ ]% | [ ]% | [ ] |
| Monthly churn | max [ ]% | max [ ]% | [ ]% | [ ] |
| Cost to get one customer | max [ ] | [ ] | [ ] | [ ] |
| Support tickets per 100 customers | max [ ] | [ ] | [ ] | [ ] |
| Uptime this period | [ ]% | [ ]% | [ ]% | [ ] |
| Average reply time to customers | max [ ] hrs | [ ] hrs | [ ] hrs | [ ] |
| Customer satisfaction | [ ] | [ ] | [ ] | [ ] |
| Cost to run per customer | max [ ] | [ ] | [ ] | [ ] |

**Which channels brought the most customers?**

| Channel | Customers | Cost | Quality (do they stay?) |
|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] |

**What do customers say? (read at least 10 messages, write the top 3 themes)**
1. [ ]
2. [ ]
3. [ ]

**Can we handle the next stage?** (answer Yes / No / Partly)

| Question | Answer | Fix |
|---|---|---|
| Can the product handle 2× the current customers? | [ ] | [ ] |
| Can support handle 2× the messages? | [ ] | [ ] |
| Can the budget handle 2× the costs? | [ ] | [ ] |
| Is the team rested and not burned out? | [ ] | [ ] |

**Checkpoint decision:** [ ] Keep growing  [ ] Grow slowly while fixing  [ ] Pause growth and fix  [ ] Change plan
**What we will do next (max 3 actions):**
1. [ ] — Owner: [ ] — Date: [ ]
2. [ ] — Owner: [ ] — Date: [ ]
3. [ ] — Owner: [ ] — Date: [ ]

## 12.2 What to focus on at each milestone

| Milestone | Main question | What you are really doing |
|---|---|---|
| **#10** | Does it work for real people? | Talk to every customer personally. Fix everything that confuses them. |
| **#50** | Do people get value and stay? | Improve onboarding. Check retention. Start writing down what works. |
| **#100** | Can we repeat how we get customers? | Double down on the 1-2 best channels. Cut the rest. |
| **#250** | Does it still work when it is bigger? | Check speed, costs, support load and automation. |
| **#500** | Are we a real business now? | Review the whole journey. Decide: grow, fix, or change direction. Fill Section 13. |

---

# 13. POST-LAUNCH REVIEW (FILL AT DAY 7, DAY 30 AND CUSTOMER #500)

| Question | Day 7 | Day 30 | Customer #500 |
|---|---|---|---|
| Date | [ ] | [ ] | [ ] |
| Customers so far | [ ] | [ ] | [ ] |
| Did we hit our targets from Section 3.2? | [ ] | [ ] | [ ] |
| What went better than expected? | [ ] | [ ] | [ ] |
| What went worse than expected? | [ ] | [ ] | [ ] |
| Biggest surprise | [ ] | [ ] | [ ] |
| Biggest customer complaint | [ ] | [ ] | [ ] |
| Biggest customer compliment | [ ] | [ ] | [ ] |
| Any incidents (outages, bugs, data issues)? Write what, when, and how long. | [ ] | [ ] | [ ] |
| Which risks from Section 7 actually happened? | [ ] | [ ] | [ ] |
| Which questions in this template were wrong, missing or confusing? | [ ] | [ ] | [ ] |
| What will we do differently next time? | [ ] | [ ] | [ ] |

**Update the template:** After every launch, write down improvements to this template here, then update the master copy.

| Improvement to the template | Who will update it | Date |
|---|---|---|
| [ ] | [ ] | [ ] |

---

# 14. FILLED-IN EXAMPLE (SO YOU CAN SEE WHAT "GOOD" LOOKS LIKE)

**Question B3 (Hard Blocker):** *Are there zero open bugs that lose data, expose private data, charge the wrong amount, or crash the app?*

| Answer | Proof / Fix |
|---|---|
| **Yes** | Bug list in `https://example.com/bugs` filtered by "Critical" shows 0 open. Checked 2026-11-02 by Sam. |

**Question C6 (Scorecard):** *Have you tested what happens when many people use it at once?*

| Score | Proof | Fix |
|---|---|---|
| **1** | Test with 100 users passed. 500-user test not yet done. Report: `load-test-100.pdf` | Sam — 2026-11-04 — Run the 500-user test and fix anything that slows down. |

**Bad answer (do not write like this):** `Score: 2 · Proof: "should be fine" · Fix: "later"`
*Why it is bad: no proof, no owner, no date.*

## More examples, one per part of the document

**Section 3.1: Defining words**
| Term | Good answer | Bad answer |
|---|---|---|
| "Customer" is… | Someone who paid at least once and was not refunded | "A user" |
| "Activated" means… | Created and saved their first invoice within 24 hours of signup | "Used the product" |

**Section 3.3: Success numbers**
| Measure | Minimum | Target | Where you read it |
|---|---|---|---|
| Signup → activated | 30% | 45% | Analytics dashboard, "Activation" report |

**Section 5: Hard blocker with a fix**
| # | Question | Yes / No | Proof or Fix |
|---|---|---|---|
| B5 | Backups exist and restore was tested? | **No** | Fix: Alex — 2026-11-03 — run restore test on staging copy. *(Decision stays NO-GO until this is Yes.)* |

**Section 6-D: Security (score 0 example)**
| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| D1 | Can one customer ever see another's data? | **0** | I tried changing the number in the page address and saw someone else's invoice | Alex — 2026-11-01 — add a check that the invoice belongs to the logged-in user; re-test |

**Section 6-J: Marketing (score 1 example)**
| # | Question | Score | Proof | Fix |
|---|---|---|---|---|
| J3 | Does the landing page show proof? | **1** | Has 2 real testimonials with permission (`testimonials-permission.pdf`) | Priya — 2026-11-06 — add 3 more real ones from beta users; do not invent any |

**Section 6-K: Channel row**
| Channel | Why it fits | Planned action | Weekly hours | Goal | Owner | Ready? |
|---|---|---|---|---|---|---|
| Email list | 400 people already asked to hear about launch | 3 emails over 10 days | 3 | 60 signups | Priya | 2 |

**Section 7: Risk row**
| # | What could go wrong? | Chance | Damage | Score | Prevent | If it happens | Owner |
|---|---|---|---|---|---|---|---|
| R2 | Payments fail on launch day | 2 | 3 | 6 | Live-mode test payment the day before | Switch checkout to "contact us" page, email affected users within 1 hour | Sam |

**Section 8: Launch day row**
| When | Action | Owner | Done? |
|---|---|---|---|
| T-2 hours | Sign up with a new email, pay with a real card, log out and log in | Sam | [x] |

**Section 9: Rollback steps (good = a stranger could follow it)**
1. Open the deployment tool at `[link]`. 2. Click "Releases". 3. Choose the release marked "last stable". 4. Click "Redeploy". 5. Wait 3 minutes. 6. Open the live product and log in to confirm. 7. Post the status message from the message template.

**Section 11: Conditional Go condition**
| # | Condition | Owner | Must be done by | Done? |
|---|---|---|---|---|
| 1 | Run the 500-user load test and fix anything slower than 3 seconds | Sam | 2026-11-04 (before announcements go out) | [ ] |

**Section 12: Traffic light**
| Measure | Minimum | Target | Actual | Light |
|---|---|---|---|---|
| Week-4 retention | 20% | 35% | 27% | 🟡 |

**Section 13: Review answers**
- *What went worse than expected?* "Signups were 40% below target; most traffic came from one post that stopped working after day 2."
- *What will we do differently?* "Start outreach 2 weeks earlier and test 3 channels, not 1."

---

# 15. APPENDICES

## Appendix A. Quick one-page checklist (print this for launch morning)

- [ ] All Hard Blockers (Section 5) are Yes
- [ ] Total score meets the gate minimum (Section 10)
- [ ] Final decision signed (Section 11)
- [ ] Rollback steps are written and the person who can press it is awake and reachable
- [ ] Alerts go to a real phone
- [ ] Support inbox is open and someone is watching it
- [ ] Payment test passed in live mode
- [ ] Announcements are scheduled
- [ ] Dashboard is open on a screen
- [ ] Everyone has eaten and slept

## Appendix B. Instructions for an AI Agent filling or checking this document

> Paste this section (or point your AI agent to this file) when you want an AI assistant to help. The agent must follow these rules.

1. **Never invent proof.** If a link, file, test result or number is not provided or cannot be verified, write `UNKNOWN`, score the item `0`, and ask the human for it.
2. **Never change a Hard Blocker answer** to Yes without proof that a human has confirmed.
3. **Never fill a decision or sign-off field.** Only humans decide and sign. The agent may fill "Recommended decision" in Section 10 only.
4. **Do the math.** Calculate area scores and the total in Section 10 and show the numbers.
5. **Check completeness.** List every blank, `[ ]`, `UNKNOWN`, and every `0` or `1` without an Owner and Due date.
6. **Check consistency.** Flag contradictions (for example: "Free product" in Section 2 but payments scored `2` in 6-H; or price different in marketing and checkout).
7. **Ask before assuming.** If a question is unclear, ask the human one short question instead of guessing.
8. **Output a summary** at the end: decision recommended, blockers failed, three biggest risks, and the top five fixes in priority order.
9. **Keep a change log** of what the agent filled in so a human can review it.

## Appendix C. AI-Driven Development Life Cycle map (where each section is used)

| Phase | What happens | Where this document is used |
|---|---|---|
| 1. Idea and goals | Decide what to build and for whom | Sections 2, 3 |
| 2. Plan and design | Write specs, break into tasks, assign AI and human work | Sections 3, 4, 6-B |
| 3. Build | Humans and AI agents write code and content | Section 6-A, 6-B |
| 4. Test | Automated and manual testing | Section 6-C, 6-D |
| 4b. Early customer talks | Interview first users | Appendix E |
| 5. **Gate G0** Build Complete | Fill Sections 5-6, decide | Sections 5, 6, 10, 11 |
| 6. Private beta | Invite 10-50 people | Gate G1, Sections 6-I, 6-L |
| 7. Fix and polish | Resolve beta feedback | Sections 6, 7 |
| 8. Pre-launch | Marketing, support, payments, stores ready | Sections 6-H, 6-I, 6-J, 6-K, 6-P |
| 9. **Gate G2** Public Launch | Final decision meeting | Sections 5, 10, 11 |
| 10. Launch day | Execute the plan | Sections 8, 9 |
| 11. Grow to 500 | Run checkpoints | Sections 12, **Gate G3** |
| 12. Review and improve | Learn, update template | Section 13 |

## Appendix D. Where to store files related to this launch

Recommended folder layout (create once, reuse for every project):

```
Launch, marketing and customer acquisition/
└── [Project Name]/
    ├── Launch_Go_No_Go.md          ← this file (copy it per project)
    ├── proof/                      ← screenshots, test reports, exports named by question number (e.g. C6-load-test.pdf)
    ├── decisions/                  ← one saved copy of Section 11 per gate
    └── checkpoints/                ← one saved copy of Section 12 per milestone
```

## Appendix E. Customer Interview Script (for your first 20 customers)

> **Goal:** Learn what is really happening, not to hear compliments. Keep it to 15-20 minutes. Ask permission before recording. Never argue or defend the product. Write answers right after each call.
> **Rule:** Ask about *what they did*, not *what they might do*.

**Before the call**
- [ ] Look up what the person did in the product (signup date, activated or not)
- [ ] Have 3 questions you most need answered
- [ ] Tell them: "I'm not selling anything. There are no wrong answers. Bad news helps me most."

**Opening (2 minutes)**
1. What do you do day-to-day? (so you understand their world)
2. How did you hear about us?

**Their problem (5 minutes)**
3. What were you trying to get done when you signed up?
4. How were you doing it before? What was annoying about that?
5. When was the last time that problem happened? Walk me through it.

**Their experience (5 minutes)**
6. What was the first thing you tried in the product? What happened?
7. Was there a moment you felt confused or stuck? Where?
8. Was there a moment you thought "this is useful"? What was it?
9. What nearly stopped you from signing up or paying?

**Value and price (3 minutes)**
10. If we took the product away tomorrow, what would you do instead? How disappointed would you be (very / somewhat / not)?
11. What would you tell a friend about it, in your own words?
12. Which price would feel too cheap to trust and which too expensive? *(do not name your price first)*

**Closing (2 minutes)**
13. What is the one thing you would change first?
14. Who else should I talk to?
15. May I follow up when we fix it?

**Record each interview here**

| # | Date | Customer type | Activated? | Top problem | Best quote (exact words, with permission) | Very disappointed if gone? | Action we will take |
|---|---|---|---|---|---|---|---|
| 1 | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

**After 10 interviews:** count the "very disappointed" answers. If fewer than 4 in 10 are "very disappointed" (the common 40% rule of thumb), fix the core value before spending on growth.

## Appendix F. Change log of this template (for the template owner)

| Version | Date | Changed by | What changed and why |
|---|---|---|---|
| v1.0 | [YYYY-MM-DD] | [ ] | First version |
