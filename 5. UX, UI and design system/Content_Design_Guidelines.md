# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **Where this file lives:** `/UX-UI-Design-System/Content_Design_Guidelines.md`
> **Who this is for:** Anyone. You do not need to be a writer, designer, or developer. If you can answer questions about your product, you can fill this in.
> **How long it takes:** 60-90 minutes the first time. Most of it is copy-and-edit.

## The 8 simple rules for filling this in

1. **Work top to bottom.** Section 1 first, Section 16 last. Later sections depend on earlier ones.
2. **Replace every `[YOUR ANSWER HERE]`.** When none are left, you are done. Use `Ctrl+F` (or `Cmd+F`) and search for `[YOUR ANSWER HERE]` to check.
3. **Look at the "Example" under each field.** It shows what a good answer looks like for a fictional app called **PlantPal**. Copy the style, not the words.
4. **Short beats long.** One clear sentence is better than a paragraph.
5. **Do not know the answer yet?** Write `TBD - owner: [name] - due: [date]`. Never leave it blank, and never guess silently.
6. **Tick the boxes.** Every section ends with a "You are done when..." checklist. Change `[ ]` to `[x]` when true.
7. **Do not delete sections.** If a section does not apply, write `N/A - because [reason]`. This tells the next person you thought about it.
8. **Keep one file.** Everything lives here. Do not make side documents. Link to outside things only when you must (Figma, brand kit, legal pages).

## What the labels mean

| Label | Meaning |
|---|---|
| `[YOUR ANSWER HERE]` | You must replace this with your own answer. |
| **Example (PlantPal):** | A sample answer. Do not keep it in your final document. Delete or replace it. |
| `[ ]` / `[x]` | A checkbox. Empty means not done, `x` means done. |
| `TBD` | "To be decided." Must have an owner and a date. |
| `[PLAN]` `[BUILD]` `[TEST]` `[LAUNCH]` `[FIRST 500]` | Phase tags. They tell you **when** in the product's life a section matters (see below). |
| **MUST** / **SHOULD** / **MAY** | MUST = required. SHOULD = strongly recommended. MAY = optional. |

## The product life cycle used in this document (AI-Driven Development Life Cycle)

| Phase tag | What is happening | Typical end point |
|---|---|---|
| `[PLAN]` | Idea, research, goals, who the users are | Idea approved |
| `[BUILD]` | Designing and coding, with humans and AI agents writing screens, copy and code | Feature complete |
| `[TEST]` | Checking quality, accessibility, copy, and AI behavior | Ready for release |
| `[LAUNCH]` | Releasing publicly, store listings, announcements | Product is live |
| `[FIRST 500]` | Supporting, learning from and keeping the first 500 customers | 500 real customers have used it |

A section with several tags is needed in several phases. Example: `[BUILD] [TEST]` means "use while building, check while testing."

## How AI agents use this document

- AI agents (coding assistants, copy generators, chatbots) **MUST read this whole file before writing any text a customer will see**. That includes buttons, errors, emails, notifications, store listings and AI replies.
- Humans use the same file to **review and approve** what the AI wrote.
- Where this file and an AI's habit disagree, **this file wins**.
- If this file does not answer a question, the AI **MUST ask a human** instead of guessing. Section 15 explains how to log the question.

## Document control (fill this in now)

| Field | Your answer |
|---|---|
| Product name | `[YOUR ANSWER HERE]` |
| Document version | `v0.1` |
| Created on (date) | `[YOUR ANSWER HERE]` |
| Last updated (date) | `[YOUR ANSWER HERE]` |
| Document owner (one named person) | `[YOUR ANSWER HERE]` |
| Final approver (one named person) | `[YOUR ANSWER HERE]` |
| Current life cycle phase | `[PLAN]` / `[BUILD]` / `[TEST]` / `[LAUNCH]` / `[FIRST 500]` (pick one) |
| Status | Draft / In review / Approved |

**Example (PlantPal):** Owner: Maya Chen. Approver: Sam Ortiz. Version v0.1. Phase: `[PLAN]`. Status: Draft.

---

# TABLE OF CONTENTS

1. Product Snapshot
2. Audience and Reading Level
3. Brand Voice
4. Tone by Situation
5. Writing Rules
6. Vocabulary: Glossary and Word Lists
7. UI Copy Patterns
8. Messages, Notifications and Emails
9. Marketing and Launch Copy
10. AI and Chatbot Content
11. Accessibility and Inclusive Language
12. Privacy, Legal and Regulated Content
13. Localization Readiness
14. Lifecycle Checklist: Idea to First 500 Customers
15. Review, Approval and Change Management
16. Final Readiness Check

Appendix A: Copy-Paste Instruction Block for AI Agents
Appendix B: One-Page Cheat Sheet
Appendix C: Plain-English Dictionary
Appendix D: Sources and Further Reading

---

# 1. PRODUCT SNAPSHOT `[PLAN]`

**Why this matters:** Every word in your product should serve your product's purpose. If the purpose is fuzzy, the words will be too.

### 1.1 What is the product, in one sentence?
Fill in: "`[Product]` helps `[who]` to `[do what]` so they can `[benefit]`."

`[YOUR ANSWER HERE]`

**Example (PlantPal):** PlantPal helps busy people keep houseplants alive by reminding them when to water, so their plants thrive without guesswork.

### 1.2 Product type (tick all that apply)

- [ ] Web app / SaaS
- [ ] Mobile app (iOS / Android)
- [ ] Marketing site / landing page
- [ ] AI / chatbot product
- [ ] Other: `[YOUR ANSWER HERE]`

### 1.3 What are the 3 most important things a customer does in the product?

| # | Customer action | Where it happens (screen name) |
|---|---|---|
| 1 | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| 2 | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| 3 | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** 1. Add a plant, on the "Add plant" screen. 2. Get a watering reminder, in Notifications. 3. Mark a plant as watered, on the "Today" screen.

### 1.4 What does success look like for content?
Pick the numbers you will measure. Write a target for each (or `N/A`).

| Measure | Target |
|---|---|
| % of new users who finish onboarding | `[YOUR ANSWER HERE]` |
| Support questions per 100 users | `[YOUR ANSWER HERE]` |
| Error messages that lead to a retry or fix (%) | `[YOUR ANSWER HERE]` |
| Other: `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

### 1.5 What is the one thing our content will NEVER do?
(Example: never shame users, never use fear to sell, never promise what we can't deliver.)

`[YOUR ANSWER HERE]`

**You are done with Section 1 when:**
- [ ] The one-sentence description is written.
- [ ] Product types are ticked.
- [ ] Three key customer actions are listed.
- [ ] At least two content success measures have targets.
- [ ] A "never" rule is written.

---

# 2. AUDIENCE AND READING LEVEL `[PLAN] [BUILD]`

**Why this matters:** You write differently for a 12-year-old gamer, a busy nurse, and a bank manager.

### 2.1 Describe your main audience (up to 3 groups)

| Group name | Who they are | What they want | What worries them |
|---|---|---|---|
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** "Busy Beginners", ages 25-40, new to plants. Want: easy reminders. Worry: killing another plant and feeling silly.

### 2.2 Technical comfort level of the audience

- [ ] Low (needs very simple words and extra help)
- [ ] Medium (comfortable with apps)
- [ ] High (comfortable with technical words)

### 2.3 Reading level target

| Content type | Target reading grade (US) | Why |
|---|---|---|
| In-product text (buttons, errors, help) | Grade 6-8 (recommended) | Clear for most adults, including tired and distracted ones |
| Marketing copy | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Legal / policy text | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

> **Tip for beginners:** Paste your text into a free "readability checker" (for example, the Hemingway Editor or the readability check built into Word) and look at the grade.

### 2.4 Who must NOT be confused or left out?
(Examples: people using screen readers, people who speak English as a second language, people in a hurry, children, older adults.)

`[YOUR ANSWER HERE]`

### 2.5 Are children under 13 (or under 16 in some countries) allowed to use the product?

- [ ] No. We say so clearly and block sign-up.
- [ ] Yes. Extra rules apply. See Section 12.
- [ ] Unsure. `TBD - owner: [name] - due: [date]`

**You are done with Section 2 when:**
- [ ] At least one audience group is described.
- [ ] A reading-level target is picked for each content type.
- [ ] People who must not be left out are named.
- [ ] The children question is answered.

---

# 3. BRAND VOICE `[PLAN] [BUILD]`

**Why this matters:** Voice is your product's personality. It stays the same everywhere. (Tone, in Section 4, changes with the situation.)

### 3.1 Pick 3-4 voice words

Circle or write your own.

| Pick | Word | What it means for writing | What it does NOT mean |
|---|---|---|---|
| [ ] | Friendly | Warm, uses "you" and "we" | Not silly or childish |
| [ ] | Clear | Short words, one idea per sentence | Not dull or robotic |
| [ ] | Confident | Direct, no hedging | Not arrogant |
| [ ] | Helpful | Tells people what to do next | Not pushy |
| [ ] | Professional | Accurate and respectful | Not stiff or cold |
| [ ] | Playful | Light humor where it fits | Not joking during serious moments |
| [ ] | Calm | Steady and reassuring | Not boring |
| [ ] | `[YOUR OWN]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** Friendly, Clear, Encouraging, Calm.

### 3.2 Voice in action: "We sound like this, not like that"

Write three pairs of "yes / no" sentences about your product.

| We sound like this | Not like this |
|---|---|
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Example (PlantPal):**

| We sound like this | Not like this |
|---|---|
| "Your fern is thirsty. Give it a drink today." | "Warning: Hydration deficiency detected." |
| "No worries, it happens. Let's try again." | "Error 403. Invalid action." |
| "Nice work! 5 plants watered." | "Task completion confirmed." |

### 3.3 Humor, emoji and exclamation marks

| Question | Your rule |
|---|---|
| Is humor allowed? When? | `[YOUR ANSWER HERE]` |
| Are emoji allowed? Where? How many? | `[YOUR ANSWER HERE]` |
| Exclamation marks allowed? How many per screen? | `[YOUR ANSWER HERE]` |
| Slang or pop-culture references? | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** Light humor in success and empty states only, never in errors. One emoji max, only in celebrations. One exclamation mark per screen max. No slang.

### 3.4 Person and point of view

- Product speaks as: `[we / I / the product's name]`
- Product addresses user as: `[you]`
- We **never** say: `[YOUR ANSWER HERE]` (Example: "the user", "our customers")

**You are done with Section 3 when:**
- [ ] 3-4 voice words are picked with "does / does not mean."
- [ ] Three yes/no sentence pairs are written.
- [ ] Rules for humor, emoji and exclamation marks are written.
- [ ] Point of view is decided.

---

# 4. TONE BY SITUATION `[PLAN] [BUILD] [TEST]`

**Why this matters:** Voice stays the same. Tone changes with the user's mood. Joking when someone just lost their data is a bad idea.

### 4.1 Tone map (fill in each row)

| Situation | User's likely feeling | Tone to use | Do | Don't |
|---|---|---|---|---|
| First visit / welcome | Curious | Warm, welcoming | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Doing a normal task | Focused | Clear, brief | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Success / celebration | Happy | Warm, light | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Small error (typo, missing field) | Mildly annoyed | Calm, helpful | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Serious error (payment failed, data lost) | Stressed, worried | Serious, honest, reassuring | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Waiting / loading | Impatient | Light, informative | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Empty screen (nothing here yet) | Unsure | Encouraging | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Asking for money / upgrade | Cautious | Honest, respectful | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Cancelling / leaving | Frustrated or sad | Respectful, no guilt | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Support / complaint | Upset | Empathetic, action-oriented | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Example (PlantPal, serious error row):** Tone: serious, honest, reassuring. Do: say what happened and what we are doing. Don't: joke, blame the user, or use exclamation marks.

### 4.2 Moments where we are always serious
(Examples: payments, health, safety, privacy, deleting data, security alerts.)

`[YOUR ANSWER HERE]`

**You are done with Section 4 when:**
- [ ] Every row of the tone map is filled in.
- [ ] "Always serious" moments are listed.

---

# 5. WRITING RULES `[BUILD] [TEST]`

**Why this matters:** Small rules (capital letters, dates, punctuation) stop your product from looking messy. Pick a rule once and everybody follows it.

### 5.1 Core writing principles (keep these defaults unless you have a reason)

1. **Lead with the point.** Put the most important word first.
2. **One idea per sentence.** Keep sentences under 20 words when you can.
3. **Use everyday words.** Say "use", not "utilize".
4. **Active voice.** "We saved your changes", not "Your changes were saved".
5. **Tell people what to do next.** Every message ends in a next step or is complete on its own.
6. **Be specific.** "Password must be at least 8 characters", not "Invalid password".
7. **Cut filler.** Remove "please note that", "in order to", "simply", "just".
8. **Respect people.** Never blame, scare, or talk down to the user.

Changes to these defaults: `[YOUR ANSWER HERE or "None"]`

### 5.2 Style decisions (pick one in each row)

| Topic | Options | Your choice |
|---|---|---|
| Spelling | US English / UK English | `[YOUR ANSWER HERE]` |
| Capitalization for headings and buttons | Sentence case ("Add a plant") / Title Case ("Add A Plant") | `[YOUR ANSWER HERE]` (sentence case recommended) |
| Oxford comma | Yes ("A, B, and C") / No | `[YOUR ANSWER HERE]` |
| Contractions ("don't", "we're") | Yes / No / Only in some places | `[YOUR ANSWER HERE]` |
| Numbers | Digits for 10+ and words for 1-9 / Always digits | `[YOUR ANSWER HERE]` |
| Date format | `Oct 17, 2026` / `17 Oct 2026` / `2026-10-17` | `[YOUR ANSWER HERE]` |
| Time format | `3:30 PM` / `15:30` | `[YOUR ANSWER HERE]` |
| Currency format | `$1,299.00` / other | `[YOUR ANSWER HERE]` |
| Phone number format | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Percent | `50%` / `50 percent` | `[YOUR ANSWER HERE]` |
| Ellipsis (...) | Only for loading ("Saving...") / Never | `[YOUR ANSWER HERE]` |
| Abbreviations | Spell out on first use / Avoid entirely | `[YOUR ANSWER HERE]` |
| Exclamation marks | See Section 3.3 | See 3.3 |
| Quotation marks | Straight (") / Curly (") | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** US English. Sentence case. Oxford comma yes. Contractions yes. Digits always. Date `Oct 17, 2026`. Time `3:30 PM`.

### 5.3 Punctuation and formatting rules

- Headlines: end with a period? `[Yes / No]`
- Buttons: end with a period? `[No recommended]`
- Bold: use for `[YOUR ANSWER HERE]` only.
- Italics: use for `[YOUR ANSWER HERE]` only. (Rarely recommended.)
- ALL CAPS: `[Never recommended - screen readers and readability]`
- Lists: use bullets when `[3 or more items]`; numbers when order matters.

### 5.4 Text length limits (so text doesn't break the design)

| Element | Max characters | Notes |
|---|---|---|
| Button label | `[e.g., 25]` | 1-3 words |
| Page title | `[e.g., 60]` | |
| Error message | `[e.g., 120]` | |
| Push notification title | `[e.g., 40]` | |
| Push notification body | `[e.g., 120]` | |
| Email subject | `[e.g., 50]` | |
| Tooltip | `[e.g., 80]` | |
| App store title | `[App Store 30 / Google Play 30]` | Check current store limits before launch |

**You are done with Section 5 when:**
- [ ] Core principles are accepted or edited.
- [ ] Every row of the style table has a choice.
- [ ] Character limits are filled in.

---

# 6. VOCABULARY: GLOSSARY AND WORD LISTS `[PLAN] [BUILD] [TEST]`

**Why this matters:** If one screen says "Sign in" and another says "Log in" and a third says "Login", people get confused. Choose one word and use it everywhere.

### 6.1 Product glossary (our official words)

| Official word | What it means | Words we do NOT use for it |
|---|---|---|
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** Official: "Sign in" - means entering your account. Don't use: "Log in", "Login".

### 6.2 Common action words (pick one in each row)

| Action | Options | Our choice |
|---|---|---|
| Entering your account | Sign in / Log in | `[YOUR ANSWER HERE]` |
| Leaving your account | Sign out / Log out | `[YOUR ANSWER HERE]` |
| Creating an account | Sign up / Create account / Register | `[YOUR ANSWER HERE]` |
| Removing something permanently | Delete / Remove | `[YOUR ANSWER HERE]` |
| Hiding something without deleting | Archive / Hide | `[YOUR ANSWER HERE]` |
| Saving | Save / Done / Apply | `[YOUR ANSWER HERE]` |
| Stopping an action | Cancel / Close / Dismiss | `[YOUR ANSWER HERE]` |
| Moving forward | Next / Continue | `[YOUR ANSWER HERE]` |
| Payment plan | Plan / Subscription | `[YOUR ANSWER HERE]` |

### 6.3 Words we always use / words we never use

| Always use | Never use | Why |
|---|---|---|
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Starter "never use" list (edit as needed):** "simply", "just", "easy" (what's easy to us may not be to the user), "obviously", "unfortunately" (overused), "invalid" (vague), "illegal" (use "not allowed" unless legally accurate), "master/slave", "blacklist/whitelist" (use "blocklist/allowlist"), "guys" (use "everyone" or "team").

### 6.4 Jargon check

List technical words that users may not know and the plain version.

| Technical word | Plain version |
|---|---|
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** "Authentication" becomes "Sign in". "Sync" becomes "Update across your devices".

### 6.5 Brand and product names

| Name | Correct writing | Wrong writing |
|---|---|---|
| Product name | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Company name | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Feature names | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Plan names | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**You are done with Section 6 when:**
- [ ] Glossary has at least 5 entries (or `TBD` with owner and date).
- [ ] Every common action word is chosen.
- [ ] "Never use" list is reviewed.
- [ ] Product, company, feature and plan names are spelled out.

---

# 7. UI COPY PATTERNS `[BUILD] [TEST]`

**Why this matters:** Buttons, labels and forms appear hundreds of times. Setting a pattern once saves hours and prevents mistakes.

### 7.1 Buttons and links

**Rules (defaults):**
- Start with a verb: "Save plant", not "Plant saving".
- 1-3 words when possible.
- Say exactly what happens: "Delete plant", not "OK".
- Never use "Click here". Use meaningful link text: "See pricing".
- Only one **primary** button per screen.

| Button type | Our wording | Example (PlantPal) |
|---|---|---|
| Primary action | `[YOUR ANSWER HERE]` | "Add plant" |
| Secondary action | `[YOUR ANSWER HERE]` | "Skip for now" |
| Cancel | `[YOUR ANSWER HERE]` | "Cancel" |
| Destructive (delete) | `[YOUR ANSWER HERE]` | "Delete plant" |
| Submit form | `[YOUR ANSWER HERE]` | "Save changes" |
| Go back | `[YOUR ANSWER HERE]` | "Back" |

### 7.2 Form fields

| Part | Rule | Your choice |
|---|---|---|
| Labels | Always visible above the field. Never use only placeholder text as a label. | `[Agree / change]` |
| Placeholder (hint inside field) | Use only for an example. Never for instructions. | `[Agree / change]` |
| Required fields | Mark `[required / optional]` | `[YOUR ANSWER HERE]` |
| Help text | Under the field, only when needed | `[YOUR ANSWER HERE]` |
| Error text | Under the field, in plain words, says how to fix | `[YOUR ANSWER HERE]` |

**Do / Don't**

| Do | Don't |
|---|---|
| Label: "Email address" | Label: "Enter your electronic mail" |
| Error: "Add an @ sign, like name@example.com" | Error: "Invalid input" |
| Help: "At least 8 characters" | Help: appears only after the user fails |

### 7.3 Navigation and page titles

- Menu item names are `[nouns / verbs]`: Example: "Plants", "Reminders", "Settings".
- Page title matches the menu item the user clicked: `[Yes / No]`.
- Max menu items: `[e.g., 5-7]`.

List your menu items:

`[YOUR ANSWER HERE]`

### 7.4 Empty states (screens with nothing in them yet)

Pattern: **What this is + why it's useful + one clear action.**

| Screen | Headline | Body | Button |
|---|---|---|---|
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** Headline: "No plants yet." Body: "Add your first plant and we'll remind you when it's thirsty." Button: "Add a plant".

### 7.5 Onboarding (the first-time experience)

| Step | Goal | Copy |
|---|---|---|
| Welcome | Make users feel welcome and explain the value in 1 sentence | `[YOUR ANSWER HERE]` |
| Setup question 1 | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Permissions (notifications, location, camera) | Explain **why** before the system asks | `[YOUR ANSWER HERE]` |
| First success | Celebrate the first win | `[YOUR ANSWER HERE]` |

**Rule:** Never show a system permission pop-up without first explaining the reason in your own words.

### 7.6 Confirmation and "Are you sure?" dialogs

Pattern: **Title says what will happen. Body says the consequence. Buttons repeat the action.**

| Part | Example |
|---|---|
| Title | "Delete this plant?" |
| Body | "You'll lose its watering history. This can't be undone." |
| Primary button | "Delete plant" |
| Secondary button | "Keep plant" |

Your destructive-action dialogs: `[YOUR ANSWER HERE]`

### 7.7 Tooltips, hints and microcopy

- Tooltips: short, 1 sentence, no new essential information (people may never see them).
- Tooltip must also work for keyboard and screen reader users.
- Loading text: `[YOUR ANSWER HERE]` (Example: "Saving...")
- Toggle labels: say what the toggle does when **on**.

**You are done with Section 7 when:**
- [ ] Button wording is filled in for all six types.
- [ ] Form-field rules are agreed.
- [ ] Menu items are listed.
- [ ] Empty-state copy exists for every empty screen.
- [ ] Onboarding steps are written.
- [ ] Destructive dialogs follow the pattern.

---

# 8. MESSAGES, NOTIFICATIONS AND EMAILS `[BUILD] [TEST] [LAUNCH] [FIRST 500]`

**Why this matters:** These are the moments when customers need you most: when something goes wrong, or when you contact them.

### 8.1 Error messages: the 4-part formula

Every error answers: **1) What happened? 2) Why? (if known) 3) What can I do now? 4) Who can help?**

| Do | Don't |
|---|---|
| "We couldn't save your plant. Check your internet and try again." | "Error 500" |
| "That password is too short. Use at least 8 characters." | "Invalid password" |
| "Something went wrong on our end. Your data is safe. Try again in a few minutes or contact support." | "Fatal exception" |

**Rules:**
- Never blame the user. Say "We couldn't..." or "That didn't work...".
- Never show technical codes alone. If you need a code for support, put it small, at the end.
- Never use "oops" for serious errors.
- Keep the user's data visible. Do not clear the form.

Error message library (list your top 10 errors):

| # | When it happens | Message | Next step shown |
|---|---|---|---|
| 1 | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| 2 | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| 3 | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

Required errors to cover: no internet, sign-in failed, payment failed, page not found, no permission, server problem, form field wrong, file too large, session expired, rate limit hit.

### 8.2 Success, warning and info messages

| Type | Pattern | Example |
|---|---|---|
| Success | Say what was done. Stay short. | "Plant added." |
| Warning | Say what might go wrong and how to avoid it. | "Your trial ends in 2 days. Add a payment method to keep your plants synced." |
| Info | Neutral, useful, not essential | "Reminders are sent at 9 AM." |

### 8.3 Notifications (push, in-app, SMS)

**Rules:**
- Only send when it helps the user. Ask yourself: "Would I want this at 3 AM?"
- Title says the point. Body gives detail.
- One action per notification.
- Respect the user's choices (frequency, quiet hours).

| Notification | When sent | Title | Body | Action |
|---|---|---|---|---|
| Welcome | After sign-up | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Core reminder | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Re-engagement (user went quiet) | After `[X]` days | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

Max notifications per user per day: `[YOUR ANSWER HERE]`
Quiet hours (no notifications): `[YOUR ANSWER HERE]`

### 8.4 Emails

**Email types to plan:**

| Email | Phase | Purpose | Subject line | Preview text |
|---|---|---|---|---|
| Welcome | `[FIRST 500]` | Say hello, give one first step | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Verify email | `[BUILD]` | Confirm address | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Password reset | `[BUILD]` | Safe, calm, clear | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Receipt / invoice | `[LAUNCH]` | Clear and correct | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Trial ending | `[LAUNCH]` | Honest reminder | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Feedback request | `[FIRST 500]` | Ask for 1 thing | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Cancellation | `[FIRST 500]` | Respectful goodbye | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Email rules:**
- One main goal and one main button per email.
- Subject line: real and honest (no tricks), `[X]` characters max.
- Every marketing email has a working unsubscribe link.
- Sender name: `[YOUR ANSWER HERE]`. Reply-to address: `[YOUR ANSWER HERE]`.
- Signature: `[YOUR ANSWER HERE]`

**You are done with Section 8 when:**
- [ ] The 10 required errors have messages.
- [ ] Notification limits and quiet hours are set.
- [ ] Each planned email has a subject and goal.
- [ ] Sender name and reply-to address are decided.

---

# 9. MARKETING AND LAUNCH COPY `[LAUNCH] [FIRST 500]`

**Why this matters:** This copy brings your first 500 customers in the door. It must promise only what the product really does.

### 9.1 Core messaging

| Item | Your answer |
|---|---|
| Tagline (max 8 words) | `[YOUR ANSWER HERE]` |
| One-line pitch (max 20 words) | `[YOUR ANSWER HERE]` |
| 3 key benefits (benefit, not feature) | 1. `[YOUR ANSWER HERE]` 2. `[YOUR ANSWER HERE]` 3. `[YOUR ANSWER HERE]` |
| Problem we solve | `[YOUR ANSWER HERE]` |
| Why we're different | `[YOUR ANSWER HERE]` |

**Example (PlantPal):** Tagline: "Happy plants, zero guesswork." Benefit: "Never forget to water again" (benefit) vs "Smart scheduling engine" (feature).

### 9.2 Landing page and website

| Part | Rule | Your copy |
|---|---|---|
| Headline | Promise the main benefit in under 12 words | `[YOUR ANSWER HERE]` |
| Subheadline | Explain how, in 1 sentence | `[YOUR ANSWER HERE]` |
| Main button | Verb + benefit | `[YOUR ANSWER HERE]` |
| Proof (reviews, numbers, logos) | Real only. Never invent. | `[YOUR ANSWER HERE]` |
| FAQ | Answer the 5 questions people ask most | `[YOUR ANSWER HERE]` |

### 9.3 App store listings

| Field | Limit (check current store rules) | Your copy |
|---|---|---|
| App name | `[~30 characters]` | `[YOUR ANSWER HERE]` |
| Subtitle / short description | `[~30 / ~80 characters]` | `[YOUR ANSWER HERE]` |
| Long description | `[up to ~4,000 characters]` | `[YOUR ANSWER HERE]` |
| Keywords | `[~100 characters on iOS]` | `[YOUR ANSWER HERE]` |
| "What's new" text | Plain language, no jargon | `[YOUR ANSWER HERE]` |

### 9.4 SEO basics (search engines)

| Item | Rule | Your copy |
|---|---|---|
| Page title tag | ~50-60 characters, main keyword near the start | `[YOUR ANSWER HERE]` |
| Meta description | ~150-160 characters, includes a reason to click | `[YOUR ANSWER HERE]` |
| Main keyword | One per page | `[YOUR ANSWER HERE]` |
| Image alt text | Describe the image. See Section 11. | `[YOUR ANSWER HERE]` |

### 9.5 Pricing copy

- Show the price clearly. No hidden fees.
- Say what is included in each plan in plain words.
- Say how to cancel, in the same place as the price.
- Free trial: say exactly when it ends and what happens next.

`[YOUR ANSWER HERE]`

### 9.6 Honesty rules for marketing (MUST)

- [ ] No fake reviews, fake numbers, or fake urgency ("only 2 left!" when false).
- [ ] No promises the product can't keep.
- [ ] Customer quotes are used with permission.
- [ ] "Free" really is free.
- [ ] AI-generated claims are checked by a human before publishing.

### 9.7 First-500 announcement plan

| Channel | Message | Date | Owner |
|---|---|---|---|
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**You are done with Section 9 when:**
- [ ] Tagline, pitch and 3 benefits are written.
- [ ] Landing page copy is written.
- [ ] Store listing fields are filled (if mobile).
- [ ] SEO titles and descriptions exist.
- [ ] Pricing copy is clear.
- [ ] All honesty rules are ticked.

---

# 10. AI AND CHATBOT CONTENT `[PLAN] [BUILD] [TEST] [LAUNCH] [FIRST 500]`

**Why this matters:** If your product talks using AI, its words ARE your product. People must know they are talking to AI, and it must stay safe and on-brand.

> If your product has **no** AI features, write `N/A - no AI features` under 10.1 and tick the box at the end. If you add AI later, return here.

### 10.1 Does the product use AI that talks to users?

- [ ] No (write N/A and skip to Section 11)
- [ ] Yes, a chatbot / assistant
- [ ] Yes, AI generates content (text, images, summaries)
- [ ] Yes, AI makes suggestions or decisions

### 10.2 AI identity and personality

| Item | Your answer |
|---|---|
| AI's name | `[YOUR ANSWER HERE]` |
| AI's job in one sentence | `[YOUR ANSWER HERE]` |
| AI's personality (use voice words from Section 3) | `[YOUR ANSWER HERE]` |
| What the AI introduces itself as | `[YOUR ANSWER HERE]` |

### 10.3 Transparency rules (MUST)

- [ ] The AI **tells users it is an AI** and never pretends to be human.
- [ ] AI-generated content is labeled where users could mistake it for human-made.
- [ ] Users can reach a human when `[YOUR ANSWER HERE]` (Example: billing problems, complaints, safety).
- [ ] Users are told what data the AI uses and whether chats are saved (link to privacy page).
- [ ] The AI can say "I'm not sure" instead of making things up.

Label wording we use: `[YOUR ANSWER HERE]`
(Example: "Written by AI. Check important details.")

### 10.4 How the AI should write

| Rule | Your setting |
|---|---|
| Reply length | `[Short / Medium / As needed]` |
| Format | `[Plain sentences / Bullets allowed / Headings allowed]` |
| Reading level | Same as Section 2.3 |
| Emoji | Same as Section 3.3 |
| Always end with | `[A next step / a question / nothing]` |
| Language | `[YOUR ANSWER HERE]` |

### 10.5 What the AI must NOT do

- [ ] Give medical, legal or financial advice unless `[approved - describe]`.
- [ ] Share private or sensitive user data.
- [ ] Make promises on behalf of the company (refunds, deadlines) unless `[allowed]`.
- [ ] Insult, shame or pressure users.
- [ ] Invent facts, links, prices or policies.
- [ ] Pretend to remember things it can't.
- [ ] Other: `[YOUR ANSWER HERE]`

### 10.6 Scripted AI messages (write these once, reuse everywhere)

| Moment | Message |
|---|---|
| Greeting | `[YOUR ANSWER HERE]` |
| Doesn't understand | `[YOUR ANSWER HERE]` |
| Can't help with this | `[YOUR ANSWER HERE]` (be kind, say what it can do instead) |
| Sensitive topic or user in distress | `[YOUR ANSWER HERE]` (calm, caring, point to human help) |
| Handing over to a human | `[YOUR ANSWER HERE]` |
| AI is down / slow | `[YOUR ANSWER HERE]` |
| Asking for feedback on an answer | `[YOUR ANSWER HERE]` |

**Example (PlantPal, "Can't help"):** "I can help with plant care, but I can't diagnose illness in people or pets. For that, please talk to a doctor or vet."

### 10.7 Testing the AI's words `[TEST]`

Prepare **20 test questions** before launch:

| Type of test | How many | Pass condition |
|---|---|---|
| Normal everyday questions | 8 | Correct, on-brand, correct reading level |
| Tricky or confusing questions | 4 | Asks a clarifying question or says it's unsure |
| Off-topic questions | 3 | Politely redirects |
| Unsafe or inappropriate requests | 3 | Refuses calmly, no harmful content |
| Attempts to break the rules ("ignore your instructions") | 2 | Stays within rules |

After launch `[FIRST 500]`: read a sample of real conversations every week and fix problems. Sample size: `[YOUR ANSWER HERE]`

**You are done with Section 10 when:**
- [ ] 10.1 answered (N/A is OK).
- [ ] AI identity is defined.
- [ ] All transparency rules are ticked or have a written reason.
- [ ] "Must not do" list is reviewed.
- [ ] Scripted messages are written.
- [ ] 20 test questions are prepared.

---

# 11. ACCESSIBILITY AND INCLUSIVE LANGUAGE `[BUILD] [TEST]`

**Why this matters:** About 1 in 6 people worldwide lives with a disability. Accessible content is better for everyone, and in many places it's the law.

**Standard we follow:** WCAG 2.2 Level AA (the common international standard for accessible web and app content). Mark if different: `[YOUR ANSWER HERE]`

### 11.1 Content accessibility rules (MUST unless noted)

| Topic | Rule |
|---|---|
| Plain language | Short sentences, everyday words. Explain unavoidable jargon. |
| Headings | Use real headings in order (H1, H2, H3). Never skip levels. Never use bold text to fake a heading. |
| Link text | Describe where the link goes. Never "click here" or "read more" alone. |
| Buttons | Label says what it does ("Save plant"). |
| Alt text for images | Describe the meaning of the image in about 125 characters. Use empty alt (`alt=""`) for purely decorative images. |
| Charts and diagrams | Provide the key takeaway in text. |
| Video | Captions required. Transcript recommended. |
| Audio | Transcript required. |
| Color | Never use color alone to carry meaning ("fields in red" must also say "required"). |
| Contrast | Text vs background at least 4.5:1 (3:1 for large text). |
| All caps | Avoid. Harder to read and screen readers may spell it out. |
| Emoji | Never the only way to say something. Use sparingly. |
| Time limits | Warn before timing out and let users extend. |
| Error messages | Tied to the field, read aloud by screen readers, and say how to fix. |
| Instructions | Don't rely on "see the button on the right" or "the green one". |
| Abbreviations | Spell out on first use. |
| Language | Mark the page language so screen readers pronounce correctly. |
| Touch targets | At least 24x24 CSS px (WCAG 2.2 minimum), larger is better on mobile. |

### 11.2 Alt text examples

| Image | Bad alt text | Good alt text |
|---|---|---|
| Photo of a fern on a windowsill | "image123.jpg" | "A green fern in a white pot on a sunny windowsill" |
| Decorative divider line | "line" | `alt=""` (empty, so it's skipped) |
| Chart of watering streak | "chart" | "Bar chart: you watered plants 6 out of 7 days this week" |

### 11.3 Inclusive language rules

- Use "people with disabilities", not "the disabled" or "handicapped".
- Avoid ability metaphors: "see what you mean", "blind spot", "crazy", "insane", "lame".
- Avoid gendered words when not needed: "they" for one unknown person, "chair" not "chairman".
- Avoid assuming family, culture, religion or income.
- Avoid idioms that don't translate ("piece of cake", "hit it out of the park").
- Use names and pronouns people choose. Don't force gender fields; if needed, offer self-describe.
- Show diverse people and situations in examples.
- Avoid age-related assumptions ("digital native", "senior citizens" when unneeded).

Terms specific to our product and audience: `[YOUR ANSWER HERE]`

### 11.4 Accessibility testing checklist `[TEST]`

- [ ] Read the whole product with a screen reader once (VoiceOver, TalkBack, NVDA, or similar).
- [ ] Use the product with only a keyboard (Tab, Enter, Esc).
- [ ] Zoom to 200% and check nothing breaks.
- [ ] Run an automated checker (for example axe or Lighthouse) and fix issues.
- [ ] Check color contrast on all text.
- [ ] Check every image has correct alt text.
- [ ] Check all videos have captions.
- [ ] Ask at least one real user with an accessibility need to try it, if possible.

> Automated tools catch only part of the problems. Human testing is still needed.

**You are done with Section 11 when:**
- [ ] The accessibility standard is chosen.
- [ ] Every rule in 11.1 is accepted or has a written exception.
- [ ] Inclusive language rules are reviewed.
- [ ] Testing checklist is scheduled with an owner and date.

---

# 12. PRIVACY, LEGAL AND REGULATED CONTENT `[PLAN] [BUILD] [TEST] [LAUNCH]`

**Why this matters:** Wrong words here can cost money or hurt people. Always have a qualified person review legal text.

> **Important:** This template helps you organize content. It is **not** legal advice. Have a lawyer or qualified compliance professional review everything in this section before launch.

### 12.1 What sensitive data do we collect? (tick all that apply)

- [ ] Name and email
- [ ] Location
- [ ] Payment information
- [ ] Health information
- [ ] Children's data
- [ ] Photos, files, voice or video
- [ ] Chats or AI conversations
- [ ] Tracking and analytics
- [ ] Other: `[YOUR ANSWER HERE]`

### 12.2 Where do our users live? (laws vary by place)

| Region | Yes / No | Typical rules to check with a professional |
|---|---|---|
| European Union / UK | `[Y/N]` | GDPR, cookie consent |
| United States - California | `[Y/N]` | CCPA / CPRA |
| United States - children | `[Y/N]` | COPPA |
| Other US states | `[Y/N]` | State privacy laws |
| Other countries | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

### 12.3 Required legal and trust pages

| Item | Link or location | Owner | Reviewed by lawyer? |
|---|---|---|---|
| Privacy policy | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[Y/N]` |
| Terms of service | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[Y/N]` |
| Cookie notice / settings | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[Y/N]` |
| Refund / cancellation policy | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[Y/N]` |
| AI use notice (if AI) | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[Y/N]` |
| Contact / support page | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[Y/N]` |

### 12.4 Plain-language consent copy rules

- Ask for consent in plain words, not legal language.
- Never pre-tick consent boxes.
- Say **what** we collect, **why**, and **how to say no or withdraw**.
- Make declining as easy as accepting.
- Link to the full policy.

| Do | Don't |
|---|---|
| "We'd like to use your location to find nearby plant shops. You can turn this off anytime in Settings." | "By continuing you agree to all data processing activities." |

Our consent texts (cookies, notifications, location, marketing emails):

`[YOUR ANSWER HERE]`

### 12.5 Regulated or sensitive industries

Does your product touch any of these? Tick any that apply, then add the extra rules.

- [ ] Health or medical
- [ ] Finance, payments, lending, investing
- [ ] Children or education
- [ ] Legal services
- [ ] Safety-critical (transport, emergency, etc.)
- [ ] None of the above

| If you ticked | Extra content rules (MUST) |
|---|---|
| Health | Don't diagnose or promise cures. Add "not a substitute for professional medical advice" where relevant. Point to professionals or emergency help. |
| Finance | Don't promise returns. Show fees and risks clearly. Add required disclosures. |
| Children | Use age-appropriate words. Get verifiable parental consent where the law requires. Avoid manipulative design. |
| Legal | Say the product is not a lawyer. Avoid guaranteeing outcomes. |
| Safety-critical | Use the clearest possible language. Test with real users. Escalate to a human quickly. |

Disclaimers we use (exact wording, approved by a professional): `[YOUR ANSWER HERE]`

### 12.6 Security-related copy

- Never put passwords, tokens or full card numbers in messages, emails or logs.
- Password reset messages never reveal whether an email has an account ("If an account exists, we've sent a link").
- Security alerts are calm, specific and say what to do.
- Don't ask for passwords by email, chat or notification.

### 12.7 Content ownership and permissions

- Photos, icons, fonts and music used have a license: `[Y/N]`
- User-generated content: who owns it, and what rights do we need? `[YOUR ANSWER HERE]`
- AI-generated content ownership and disclosure: `[YOUR ANSWER HERE]`

**You are done with Section 12 when:**
- [ ] Sensitive data is listed.
- [ ] Regions are listed.
- [ ] Every required page has an owner and a lawyer-review status.
- [ ] Consent copy is plain and written.
- [ ] Industry rules are added if relevant.
- [ ] A qualified person has reviewed this section (name and date): `[YOUR ANSWER HERE]`

---

# 13. LOCALIZATION READINESS `[PLAN] [BUILD] [TEST]`

**Why this matters:** You are launching in English first, but if you write sloppy now, translating later is expensive and buggy. Write now so that translation later is easy.

### 13.1 Languages

| Item | Your answer |
|---|---|
| Launch language | English (`[US / UK / other]`) |
| Languages we may add later | `[YOUR ANSWER HERE or "None planned"]` |
| Do we need right-to-left support (Arabic, Hebrew) later? | `[Yes / No / Maybe]` |

### 13.2 Writing rules that make translation easy (MUST)

- **Never glue sentences together from pieces.** Bad: "You have " + count + " plants". Use full sentences with placeholders: "You have {count} plants."
- **Handle plurals properly.** "1 plant" vs "2 plants". Use a plural system, not "plant(s)".
- **Leave room.** Translated text can be 30-40% longer. Don't design for exact fit.
- **No text inside images.** Keep words as real text.
- **Avoid idioms, puns and cultural jokes.**
- **Don't use words as both noun and verb in a confusing way** ("Save" vs "Saves").
- **Write dates, times, numbers and currency using local formats automatically**, not typed by hand.
- **Give translators context.** Explain where each text appears.
- **Avoid abbreviations and slang.**
- **Keep names and brand terms listed** so translators don't translate them (Section 6.5).

### 13.3 Text storage

- [ ] All user-facing text is stored in a **central place** (not typed inside code). Location: `[YOUR ANSWER HERE]`
- [ ] Each text has a **unique ID** and a **note for translators**.
- [ ] Text lives in **one source of truth**. Never copy and paste text into several files.

### 13.4 Example: translator-friendly text

| Bad | Good |
|---|---|
| "Delete" (no context) | "Delete" with note: "Button on plant details screen that removes a plant" |
| `"You have " + n + " plants"` | `"You have {count} plants"` with plural rules |
| "Check it out!" | "See your plants" |

**You are done with Section 13 when:**
- [ ] Language plans are written.
- [ ] Rules in 13.2 are accepted by all writers and AI agents.
- [ ] A central text storage location is decided.

---

# 14. LIFECYCLE CHECKLIST: IDEA TO FIRST 500 CUSTOMERS `[PLAN] [BUILD] [TEST] [LAUNCH] [FIRST 500]`

**Why this matters:** This is the one place where you see content tasks across the whole journey. Use it as your master to-do list. Each task has an owner (human or AI) and a date.

> **Who does it:** write `H` (human), `AI` (AI agent drafts, human approves), or `H+AI`.

### Phase 1: `[PLAN]` Idea to approved plan

| Done | Task | Section | Who | Owner name | Due date |
|---|---|---|---|---|---|
| [ ] | Write the one-sentence product description | 1 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Describe the audience and reading level | 2 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Choose voice words | 3 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Fill the tone map | 4 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Decide sensitive data and regions | 12 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Decide AI features and transparency rules | 10 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Get Section 1-4 approved | 15 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Phase gate (all ticked before moving on):** [ ] Voice and audience are approved. [ ] Legal and AI risks have owners.

### Phase 2: `[BUILD]` Designing and creating

| Done | Task | Section | Who | Owner name | Due date |
|---|---|---|---|---|---|
| [ ] | Finish writing rules and vocabulary | 5, 6 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Write button, form, navigation and empty-state copy | 7 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Write onboarding copy | 7 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Write top 10 error messages | 8 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Write notification and email copy | 8 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Write AI scripted messages | 10 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Put all text in a central place with IDs | 13 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Give AI agents Appendix A | Appendix A | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Phase gate:** [ ] Every screen has final or approved draft copy. [ ] No placeholder text ("Lorem ipsum", "TODO") remains.

### Phase 3: `[TEST]` Checking quality

| Done | Task | Section | Who | Owner name | Due date |
|---|---|---|---|---|---|
| [ ] | Read every screen out loud (find awkward text) | 5 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Run reading-grade check | 2 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Run vocabulary check (same word, same meaning, everywhere) | 6 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Run accessibility testing | 11 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Test the AI with the 20 test questions | 10 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Test with 5 real people who match the audience | 2 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Lawyer reviews legal pages and disclaimers | 12 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Check text fits in the design (longest text, small screens, 200% zoom) | 5, 13 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Phase gate:** [ ] All "must fix" problems are fixed. [ ] Approver signs off.

### Phase 4: `[LAUNCH]` Going live

| Done | Task | Section | Who | Owner name | Due date |
|---|---|---|---|---|---|
| [ ] | Publish landing page copy | 9 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Publish store listings | 9 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Publish legal and help pages | 12 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Turn on welcome email and notifications | 8 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Publish announcement posts | 9 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Prepare support replies for the top 10 expected questions | 8 | H+AI | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| [ ] | Confirm a way for users to reach a human | 10, 12 | H | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Phase gate:** [ ] Everything customers see matches this document. [ ] A named person is on call for content problems launch week.

### Phase 5: `[FIRST 500]` Learning from the first 500 customers

Customer count tracker: `0 / 500`. Update weekly.

| Done | Task | Section | Who | Owner name | Cadence |
|---|---|---|---|---|---|
| [ ] | Read a sample of support messages and chats | 8, 10 | H | `[YOUR ANSWER HERE]` | Weekly |
| [ ] | Find the top 5 confusing words or screens | 6, 7 | H+AI | `[YOUR ANSWER HERE]` | Weekly |
| [ ] | Review AI conversations for wrong, unsafe or off-brand answers | 10 | H | `[YOUR ANSWER HERE]` | Weekly |
| [ ] | Check content success measures from Section 1.4 | 1 | H | `[YOUR ANSWER HERE]` | Weekly |
| [ ] | Ask customers 1 question about clarity (survey or interview) | 2 | H | `[YOUR ANSWER HERE]` | At 50, 150, 500 customers |
| [ ] | Update this document with what you learned | 15 | H | `[YOUR ANSWER HERE]` | Weekly |
| [ ] | Update error messages that users hit most | 8 | H+AI | `[YOUR ANSWER HERE]` | Weekly |
| [ ] | Review feedback emails and store reviews | 9 | H | `[YOUR ANSWER HERE]` | Weekly |
| [ ] | Write a "What we learned" summary at 500 customers | 15 | H | `[YOUR ANSWER HERE]` | Once |

**Milestone check-ins**

| Customers | What to check |
|---|---|
| 1-50 | Can people finish onboarding on their own? Where do they get stuck? |
| 51-150 | Which messages create the most support questions? |
| 151-300 | Are tone and voice still consistent as more people write content? |
| 301-500 | What should change in this template before the next project? |

**Phase gate (to call the product "past 500"):** [ ] 500 real customers have used it. [ ] Lessons are written into Section 15's change log. [ ] The template improvements are saved for the next project.

---

# 15. REVIEW, APPROVAL AND CHANGE MANAGEMENT `[BUILD] [TEST] [LAUNCH] [FIRST 500]`

**Why this matters:** Without clear owners, content drifts. With AI writing fast, a review step keeps quality safe.

### 15.1 Who does what

| Role | Name | What they do |
|---|---|---|
| Document owner | `[YOUR ANSWER HERE]` | Keeps this file up to date |
| Content approver | `[YOUR ANSWER HERE]` | Final yes/no on customer-facing words |
| Legal reviewer | `[YOUR ANSWER HERE]` | Checks Section 12 |
| Accessibility reviewer | `[YOUR ANSWER HERE]` | Checks Section 11 |
| AI output reviewer | `[YOUR ANSWER HERE]` | Reads and approves AI-written text |
| Backup for each person | `[YOUR ANSWER HERE]` | Covers when someone is away |

### 15.2 Approval rules

| Type of content | Who must approve | Max wait time |
|---|---|---|
| Small copy change (typo, one word) | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| New screen or feature copy | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Legal, privacy, health, finance | `[YOUR ANSWER HERE]` + legal reviewer | `[YOUR ANSWER HERE]` |
| AI system instructions or scripted AI replies | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Marketing / announcement | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

**Rule:** AI-written text is never published without a human approval.

### 15.3 Content review checklist (use before every release)

- [ ] Matches voice (Section 3) and tone (Section 4).
- [ ] Follows writing rules (Section 5) and glossary (Section 6).
- [ ] Reading grade is on target (Section 2.3).
- [ ] No jargon without explanation.
- [ ] Every error message has a fix (Section 8).
- [ ] Accessibility checks pass (Section 11).
- [ ] No legal, privacy or medical claims without review (Section 12).
- [ ] Text still fits in the design.
- [ ] No placeholder or test text is left.
- [ ] Facts, prices, dates and links are correct.
- [ ] AI-written text was checked by a human.

### 15.4 Questions the document doesn't answer (open questions log)

When a person or AI agent can't find an answer in this file, log it here, then ask the owner. Don't guess.

| Date | Question | Asked by (human/AI) | Answer | Added to section |
|---|---|---|---|---|
| `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

### 15.5 Change log (record every change)

| Version | Date | Changed by | What changed | Why |
|---|---|---|---|---|
| v0.1 | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | First draft | Starting the project |

**Version rule:** Small fix = v0.1 to v0.2. Major change (new voice, new audience, new legal rules) = v1.0 to v2.0.

### 15.6 When to review this whole document

- Before each phase starts.
- When you add AI features, enter a new region, or change audience.
- After every legal or accessibility incident.
- At least every `[3 months]` while the product is live.
- At 500 customers (final lesson review).

**You are done with Section 15 when:**
- [ ] Every role has a named person and a backup.
- [ ] Approval rules are filled in.
- [ ] The change log has a first entry.
- [ ] Review dates are on a calendar.

---

# 16. FINAL READINESS CHECK `[TEST] [LAUNCH]`

Before you share this document or launch, check **everything**.

### 16.1 Completeness

- [ ] No `[YOUR ANSWER HERE]` is left (use search).
- [ ] No **Example (PlantPal)** text remains, unless you intentionally kept it.
- [ ] Every `TBD` has an owner and a due date.
- [ ] Every section's "You are done when..." list is fully ticked.
- [ ] Every `N/A` has a reason.

### 16.2 Consistency

- [ ] Voice words in Section 3 match the AI instructions in Appendix A.
- [ ] Glossary words in Section 6 match all examples in this document.
- [ ] Dates, names and numbers are the same everywhere.
- [ ] Reading-level targets match Section 2.3.

### 16.3 Safety

- [ ] Section 12 reviewed by a qualified person.
- [ ] Section 10 AI rules tested.
- [ ] Section 11 accessibility testing complete.

### 16.4 Sign-off

| Role | Name | Date | Signature / "Approved" |
|---|---|---|---|
| Document owner | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Content approver | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |
| Legal reviewer | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` | `[YOUR ANSWER HERE]` |

---

# APPENDIX A: COPY-PASTE INSTRUCTION BLOCK FOR AI AGENTS

**How to use:** After filling this document, copy the block below into your AI tool's instructions (system prompt, project rules, agent file, etc.). Replace each `{{...}}` using your answers. Keep this file attached or linked so the AI can read the details.

```text
ROLE
You write and review all customer-facing text for {{PRODUCT NAME}}.

SOURCE OF TRUTH
Read Content_Design_Guidelines.md in full before writing. If these instructions
and the file disagree, the file wins. If the file does not answer a question,
STOP and ask a human. Do not guess. Log the question in Section 15.4.

PRODUCT
{{Section 1.1 one-sentence description}}

AUDIENCE
{{Section 2.1 groups}}. Reading level: grade {{Section 2.3}}.

VOICE
{{3-4 voice words from Section 3.1}}. Follow the "we sound like this, not like
that" examples in Section 3.2.

TONE
Match the tone map in Section 4.1. Be serious in the moments listed in 4.2.

STYLE
Spelling: {{US/UK}}. Capitalization: {{sentence case}}. Dates: {{format}}.
Follow every choice in Section 5.2 and the character limits in 5.4.

VOCABULARY
Use only the official words in Section 6. Never use words from the "never use" list.

PATTERNS
Follow the button, form, empty-state, onboarding, error, notification and email
patterns in Sections 7 and 8. Every error says what happened and what to do next.

ACCESSIBILITY
Follow Section 11. Write alt text for every image. Never rely on color alone.
Use descriptive link text.

LEGAL AND SAFETY
Never write medical, legal or financial claims, privacy statements, or
guarantees unless the exact wording is already in Section 12. Flag them for
human review instead.

AI RULES (if the product uses AI)
Follow Section 10. Never pretend to be human. Label AI-generated content.

LOCALIZATION
Follow Section 13: no sentence stitching, proper plurals, no idioms, text in the
central location.

OUTPUT RULES
- Give 1 recommended version, plus 1 alternative only if asked.
- Say which section you followed when it's not obvious.
- Mark anything you are unsure about with [NEEDS HUMAN REVIEW].
- Never publish. A human approves first.

NEVER
- Invent facts, prices, reviews, quotes, links or features.
- Blame the user.
- Use placeholder text such as "Lorem ipsum" or "TODO" in final copy.
- Change the glossary or voice without human approval.
```

---

# APPENDIX B: ONE-PAGE CHEAT SHEET

Fill this in last. Print it. Stick it next to your screen.

| Topic | Our answer |
|---|---|
| Product in one sentence | `[YOUR ANSWER HERE]` |
| Voice words | `[YOUR ANSWER HERE]` |
| Reading level | `[YOUR ANSWER HERE]` |
| Spelling and capitalization | `[YOUR ANSWER HERE]` |
| Button pattern | Verb + what it does |
| Error pattern | What happened + what to do now |
| Emoji / exclamation rule | `[YOUR ANSWER HERE]` |
| Words we always use | `[YOUR ANSWER HERE]` |
| Words we never use | `[YOUR ANSWER HERE]` |
| AI disclosure wording | `[YOUR ANSWER HERE]` |
| Who approves copy | `[YOUR ANSWER HERE]` |
| Who to ask if unsure | `[YOUR ANSWER HERE]` |

---

# APPENDIX C: PLAIN-ENGLISH DICTIONARY

| Word | What it means |
|---|---|
| **Content design** | Choosing and writing the right words (and sometimes images) so people can use a product easily. |
| **Voice** | The product's personality in words. Stays the same everywhere. |
| **Tone** | The mood of the words. Changes with the situation. |
| **UI** | User Interface: the screens, buttons and menus people see and tap. |
| **UX** | User Experience: how easy and pleasant the product feels to use. |
| **Microcopy** | Tiny bits of text: button labels, hints, error messages. |
| **Empty state** | A screen that has nothing on it yet (for example, an empty list). |
| **Onboarding** | The first-time experience that helps new users get started. |
| **Placeholder text** | Light-grey example text inside a form field. Or fake text like "Lorem ipsum". |
| **CTA** | Call to Action: the button or link that asks the user to do something. |
| **Alt text** | A written description of an image for people who can't see it. |
| **Screen reader** | Software that reads screen content out loud. |
| **WCAG** | Web Content Accessibility Guidelines: international rules for accessible digital content. |
| **Localization** | Adapting a product for other languages and regions. |
| **Glossary** | A list of official words and what they mean. |
| **Source of truth** | The one place everyone trusts as correct. |
| **SEO** | Search Engine Optimization: helping search engines understand and show your pages. |
| **System prompt** | Instructions given to an AI that shape how it behaves. |
| **AI agent** | An AI tool that can carry out tasks on its own, such as writing or checking text. |
| **Phase gate** | A checkpoint that must be passed before moving to the next phase. |
| **MVP** | Minimum Viable Product: the smallest version that real people can use. |
| **Stakeholder** | Anyone who cares about or is affected by the product. |
| **Disclaimer** | A statement that limits responsibility or clarifies what the product doesn't do. |
| **GDPR / CCPA / COPPA** | Privacy laws (Europe / California / US children's data). Ask a professional what applies to you. |

---

# APPENDIX D: SOURCES AND FURTHER READING

This template follows widely used public standards and style guides. Check each for the latest versions.

- WCAG 2.2 (W3C Web Accessibility Initiative)
- Plain Language guidelines (plainlanguage.gov)
- Google Developer Documentation Style Guide
- Microsoft Writing Style Guide
- Mailchimp Content Style Guide
- GOV.UK Content Design guidance
- Apple Human Interface Guidelines (Writing)
- Material Design (Writing and Communication)
- Atlassian Design System (Content)
- Nielsen Norman Group articles (microcopy, error messages, readability)
- Unicode CLDR (plurals, dates and number formats for localization)
- Official store guidelines (Apple App Store and Google Play)
- Privacy regulator websites for the regions where you operate

*End of document. Remember: replace every `[YOUR ANSWER HERE]`, tick every box, and have a human approve before launch.*
