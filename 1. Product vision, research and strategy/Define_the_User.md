# Define the User
**Template Version:** 1.0
**Document Type:** AI-Driven Development Life Cycle (ADLC)
**Phase:** Discovery → Launch → Growth (First 500 Customers)

---

> # 📖 HOW TO USE THIS DOCUMENT
>
> **What is this?**
> This document defines WHO your product is built for. It is the single most important document in your project. Every feature decision, every AI prompt, every design choice flows from this document.
>
> **Who should fill this out?**
> The Product Manager, Founder, or whoever owns the product vision. Fill it out BEFORE writing any code.
>
> **How to fill it:**
> 1. Read each section heading and the instruction block (the grey box that starts with 📝)
> 2. Look at the Example Answer block below it (the green block that starts with 💡)
> 3. Delete the example and write your own answer
> 4. Do NOT leave any section blank — write "Unknown — to be validated" if you truly don't know yet
> 5. Revisit this document at every milestone checkpoint (10, 100, 500 users)
>
> **Golden Rule:** Write like you're explaining your user to a friend who has never met them. Be specific. Avoid vague words like "everyone," "businesses," or "users." Real names and real situations work best.
>
> **Time to complete:** 45–90 minutes for your first project. 20–30 minutes for projects after that.

---

## 📋 Document Metadata

> 📝 **Fill this first.** This is the cover page of your document. It tells people at a glance what project this belongs to and when it was last updated.

| Field | Your Answer |
|---|---|
| **Project / Product Name** | *(Write the name of your product here)* |
| **One-Line Description** | *(What does your product do in one sentence?)* |
| **Document Author** | *(Your name)* |
| **Date Created** | *(Today's date, e.g. October 13, 2026)* |
| **Last Updated** | *(Date you last changed this document)* |
| **Current Version** | *(Start with v1.0, change to v1.1 when you update it)* |
| **Project Status** | *(Choose one: Discovery / In Development / Beta / Launched / Growing)* |
| **Primary AI Tools Used** | *(e.g. Claude, Cursor, GitHub Copilot, ChatGPT — list what you use to build)* |

> 💡 **EXAMPLE ANSWER:**
>
> | Field | Example |
> |---|---|
> | **Project / Product Name** | TaskNest |
> | **One-Line Description** | A task management app for freelance designers who hate admin work |
> | **Document Author** | Sarah Chen |
> | **Date Created** | October 13, 2026 |
> | **Last Updated** | October 13, 2026 |
> | **Current Version** | v1.0 |
> | **Project Status** | Discovery |
> | **Primary AI Tools Used** | Claude Code, Cursor, v0 |

---

## 🧭 Section 1: The Product Context

> 📝 **Why this section?** Before defining the user, AI agents and your team need to understand what the product does. This gives context so that when AI reads this document, it understands the world your user lives in.
>
> Keep your answers short and honest. You don't need to sell anyone here — just be accurate.

### 1.1 What Does This Product Do?

*(Write 2–4 sentences. Explain what the product does and how it helps someone. Imagine explaining it to your grandmother.)*

```
[Write your answer here]
```

> 💡 **EXAMPLE:**
> TaskNest is a task management app that helps freelance designers track their client projects, deadlines, and invoices in one place. Instead of juggling sticky notes, spreadsheets, and email threads, a designer can open TaskNest and see everything they need to do today in under 30 seconds.

---

### 1.2 What Problem Does It Solve?

*(Write 2–3 sentences. What is the pain or frustration that exists in the world RIGHT NOW that your product fixes? Be specific.)*

```
[Write your answer here]
```

> 💡 **EXAMPLE:**
> Freelance designers spend an average of 6 hours per week on admin tasks — tracking revisions, chasing invoices, and remembering which client said what. Most project management tools are built for software teams and feel overwhelming for a solo creative. There is no simple, design-forward tool built specifically for their workflow.

---

### 1.3 What Is NOT This Product?

*(List 2–3 things this product is NOT. This prevents "scope creep" and stops AI agents from building the wrong things.)*

- This product is NOT: *(example: a full accounting or invoicing platform)*
- This product is NOT: *(example: a team collaboration tool for agencies with 50+ people)*
- This product is NOT: *(example: a portfolio or client showcase website)*

> 💡 **EXAMPLE:**
> - This product is NOT a full accounting platform (no tax calculations, no payroll)
> - This product is NOT built for design agencies with teams — only solo freelancers
> - This product is NOT a social network or community for designers

---

## 👥 Section 2: User Types Overview

> 📝 **Why this section?** Most products have more than one type of user. For example, a marketplace has buyers AND sellers. An internal tool has admins AND regular staff. This section maps out all your user types BEFORE you build detailed profiles for each one.
>
> **How to fill it:**
> - List every type of person who will USE your product (not just pay for it)
> - Mark which one is your PRIMARY user (the most important one — build for them first)
> - You will build a full profile for each user type in Section 3

### 2.1 How Many User Types Does This Product Have?

*(Choose one and delete the others)*

- [ ] **1 user type** — Only one type of person uses this product
- [ ] **2 user types** — Two distinct roles (e.g. admin + regular user)
- [ ] **3 user types** — Three distinct roles (e.g. buyer + seller + admin)
- [ ] **4+ user types** — Complex ecosystem (list them all below)

---

### 2.2 User Type Map

> 📝 Fill in the table below. Add or remove rows as needed. For each user type, give them a short nickname (e.g. "The Freelancer," "The Admin," "The Buyer"). You will use these nicknames throughout this document.

| # | User Type Nickname | Real-World Job Title / Role | Primary or Secondary? | Will They Pay? |
|---|---|---|---|---|
| 1 | *(e.g. The Freelancer)* | *(e.g. Freelance Graphic Designer)* | **PRIMARY** | *(Yes / No / Maybe)* |
| 2 | *(e.g. The Client)* | *(e.g. Small Business Owner)* | Secondary | *(Yes / No / Maybe)* |
| 3 | *(Add more rows if needed)* | | | |

> 💡 **EXAMPLE:**
>
> | # | User Type Nickname | Real-World Job Title / Role | Primary or Secondary? | Will They Pay? |
> |---|---|---|---|---|
> | 1 | The Freelancer | Freelance Graphic / UI Designer | **PRIMARY** | Yes — monthly subscription |
> | 2 | The Client | Small business owner hiring the freelancer | Secondary | No — they get a limited view link |

---

### 2.3 Who Are You Building For FIRST?

*(Copy the nickname of your PRIMARY user from the table above. Every feature in version 1.0 should serve this person.)*

> **Primary User for v1.0:** `[Write the nickname here]`

> 💡 **EXAMPLE:** `The Freelancer`

---

## 🧑‍💼 Section 3: User Profiles

> 📝 **This is the heart of the document.** You will complete one full profile for EACH user type listed in Section 2. Copy and paste Section 3 for each additional user type.
>
> **Start with your PRIMARY user.** Do that profile first before moving to secondary users.
>
> ⚠️ **Important for AI agents:** The more specific you are here, the better your AI coding tools (Claude, Cursor, Copilot) will understand who they're building for. Vague profiles = vague code = wrong product.

---

### 👤 User Profile #1 — [Paste User Type Nickname Here]

*(Replace the heading above with the nickname, e.g. "User Profile #1 — The Freelancer")*

---

#### 3.1 Identity Card

> 📝 Give your user a fictional but realistic name and fill in the details below. This makes the user feel like a real person rather than an abstract concept. AI agents use this to set the right tone, vocabulary, and complexity level for every feature.

| Field | Your Answer |
|---|---|
| **First Name** | *(Give them a realistic name, e.g. "Maya")* |
| **Age Range** | *(e.g. 25–35 years old)* |
| **Gender** | *(Optional — only fill if relevant to your product)* |
| **Location** | *(City, country, or region — e.g. "Mid-size US cities")* |
| **Job Title / Role** | *(What do they do for work?)* |
| **Work Setup** | *(e.g. Solo freelancer / Remote employee / In-office team)* |
| **Income Level** | *(e.g. $40,000–$70,000/year — helps set pricing expectations)* |
| **Education** | *(e.g. Design degree / Self-taught / Does not matter)* |
| **Family Situation** | *(e.g. Single, no kids — helps understand time constraints)* |
| **Primary Device** | *(e.g. MacBook Pro + iPhone 14)* |
| **Tech Comfort Level** | *(Choose: Beginner / Moderate / Advanced / Expert)* |

> 💡 **EXAMPLE:**
>
> | Field | Example |
> |---|---|
> | **First Name** | Maya |
> | **Age Range** | 27–34 years old |
> | **Gender** | Not specified (not relevant to product) |
> | **Location** | Mid-size US cities (Austin, Denver, Nashville) |
> | **Job Title / Role** | Freelance UI/UX Designer |
> | **Work Setup** | Solo freelancer, works from home or coffee shops |
> | **Income Level** | $55,000–$85,000/year (variable) |
> | **Education** | Design degree OR self-taught (mix) |
> | **Family Situation** | Single or early relationship, no kids — high personal flexibility |
> | **Primary Device** | MacBook Pro + iPhone 15 |
> | **Tech Comfort Level** | Advanced — comfortable with SaaS tools, not a developer |

---

#### 3.2 The Full Story (A Day in Maya's Life)

> 📝 Write a short story about this user's typical day — specifically the part of their day where YOUR product would fit. Write it like a movie scene. Use the first name you gave them above. This section is used word-for-word to brief AI agents and helps your team empathize with the user.
>
> **Length:** 150–250 words. Use simple sentences. Write in present tense.

```
[Write the story here. Start with: "It's [time of day]. [Name] is [doing something]..."]
```

> 💡 **EXAMPLE:**
>
> It's 9:15 AM on a Monday. Maya is at her kitchen desk with a large coffee, opening her laptop. She has three active client projects — a logo rebrand for a bakery, a mobile app UI for a startup, and a website refresh for a dentist office.
>
> She opens her email first. There are seven new messages. Two clients are asking for updates. One is asking where their invoice is. She doesn't know off the top of her head — she has to open a spreadsheet she built herself six months ago, scroll through color-coded rows, and try to remember what "pending-v2-FINAL-approved" means.
>
> By 10 AM, she has spent 45 minutes just figuring out where things stand — before doing any actual design work.
>
> She knows there has to be a better way. She's tried Asana, Trello, and Notion. They all feel like they were built for software engineering teams, not for her. She ends up back in her spreadsheet because it's familiar, even though she hates it.
>
> TaskNest is what she wishes existed: something that organizes her projects, tracks revisions, and reminds her about invoices — without making her feel like she's managing a NASA mission.

---

#### 3.3 Goals & Motivations

> 📝 What does this user WANT to achieve — in their work and in their life? List their goals in order of importance. Think about both practical goals (finish projects faster) and emotional goals (feel less stressed, feel professional).
>
> **Rule:** Write goals from the USER's perspective, not from a product/feature perspective. NOT "use our dashboard" — YES "know exactly where every project stands without digging."

**Professional Goals** *(What do they want to achieve at work?)*

1. *(Most important goal)*
2.
3.
4.
5.

**Personal / Emotional Goals** *(How do they want to FEEL?)*

1. *(e.g. Feel in control and professional, not chaotic)*
2.
3.

> 💡 **EXAMPLE:**
>
> **Professional Goals**
> 1. Get paid on time, every time — no more chasing invoices
> 2. Never miss a deadline or a revision request
> 3. Spend less than 30 minutes per day on admin so she can focus on design
> 4. Look professional and organized in front of clients
> 5. Scale to 5+ clients simultaneously without burning out
>
> **Personal / Emotional Goals**
> 1. Feel calm and in control at the start of every work day
> 2. Feel confident when a client asks "where are we on the project?"
> 3. Feel like a real business, not just a person making stuff up as they go

---

#### 3.4 Pain Points & Frustrations

> 📝 What FRUSTRATES this user RIGHT NOW, before they have your product? These are the things keeping them up at night, slowing them down, or making them feel bad about their work. Be brutally honest here — this is where great products are born.
>
> **Pro tip:** If you've talked to real users, quote them directly here (in quotation marks). Real quotes are gold.

**Daily Frustrations** *(The small annoying things that happen repeatedly)*

1.
2.
3.

**Bigger Pain Points** *(The deeper problems that have a real cost — time, money, stress)*

1.
2.
3.

**User Quotes** *(Optional but powerful — what have real users actually said about this problem?)*

- *"[Paste a real quote from a user interview, Reddit post, or conversation]"*
- *"[Another real quote]"*

> 💡 **EXAMPLE:**
>
> **Daily Frustrations**
> 1. Opens five different apps every morning just to know what she's supposed to work on
> 2. Clients ask for "just one small change" and she has no record of previous revision rounds
> 3. Forgets to send invoices until weeks after project completion
>
> **Bigger Pain Points**
> 1. Has lost an estimated $3,000+ in a year from late/forgotten invoices
> 2. Took on a 6th client and completely dropped the ball on client #3 — nearly lost them
> 3. Feels unprofessional when she can't quickly answer "when will this be done?"
>
> **User Quotes**
> - *"I have a design degree. I did not sign up to manage spreadsheets all day."*
> - *"Asana makes me feel like I'm a project manager at Boeing. I just need to know what to design today."*
> - *"I lost a client because I missed a deadline I didn't even know about."*

---

#### 3.5 Current Behavior — What Do They Use TODAY?

> 📝 Before your product exists, what is this user doing to solve this problem? List every tool, workaround, or habit they currently use. This tells you who your real competitors are — and it's often not other software products (sometimes it's "a spreadsheet and sticky notes").

| Current Solution | What They Use It For | What They Hate About It | Cost (Free / Paid) |
|---|---|---|---|
| *(e.g. Google Sheets)* | *(e.g. Tracking project status)* | *(e.g. I have to manually update everything)* | *(Free)* |
| | | | |
| | | | |
| | | | |

---

**3.5a: Competitor Comparison (Honest Analysis)**

> 📝 For each alternative your user might consider instead of YOUR product, fill in the table below. Be honest — this is for your own team's clarity, not marketing copy. Understanding why competitors fall short helps you define what makes your product different.

| Competitor / Alternative | Who It's Built For | What It Does Well | Why This User Still Leaves / Won't Adopt It | Your Advantage |
|---|---|---|---|---|
| *(e.g. Trello)* | *(e.g. General teams)* | *(e.g. Visual, easy kanban boards)* | *(e.g. No invoicing, no client sharing, feels like a to-do list)* | *(e.g. TaskNest is built specifically for freelancers with client-facing features)* |
| | | | | |
| | | | | |

> 💡 **EXAMPLE:**
>
> | Competitor | Who It's For | Does Well | Why Maya Leaves | Our Advantage |
> |---|---|---|---|---|
> | Trello | General teams | Simple kanban boards | No invoicing, no deadline alerts, no client view | Freelancer-specific, has invoicing |
> | Asana | Software teams | Powerful task management | Overwhelming for a solo user, steep learning curve | 10-minute setup, solo-first design |
> | Notion | Power users | Extremely flexible | Too much setup required, no templates for freelancers | Ready out of the box, zero configuration |
> | Google Sheets | Everyone | Familiar, free | Manual updates, no reminders, visually messy | Automatic tracking, visual design |
> | Honeybook | Freelancers (creative) | CRM + contracts | Too focused on sales/contracts, not project work | More focused on project execution |

**What Would Make Them Switch to YOUR product?**
*(What would have to be true for them to drop their current solution and use yours?)*

```
[Write 2–3 sentences]
```

> 💡 **EXAMPLE:**
> Maya would switch if she could replace at least 3 of her current tools with one that takes under 10 minutes to set up and shows her "today's priorities" without any configuration. The product must feel designed — ugly tools are a dealbreaker for a designer. Seeing ONE clear proof point (e.g. "You would have been paid 3 weeks earlier with TaskNest") will close the deal.

---

#### 3.6 Technology Comfort Level (Detailed)

> 📝 This section helps AI agents calibrate the complexity of UI copy, onboarding flows, error messages, and feature design. A developer building an internal tool can handle "API key" in the UI. A freelance designer cannot.

| Skill | Level | Notes |
|---|---|---|
| **General smartphone use** | *(Beginner / OK / Expert)* | |
| **Desktop/laptop apps (SaaS tools)** | *(Beginner / OK / Expert)* | |
| **Spreadsheets (Excel / Sheets)** | *(Beginner / OK / Expert)* | |
| **Graphic / design tools** | *(Beginner / OK / Expert)* | |
| **Code or programming** | *(Beginner / OK / Expert)* | |
| **AI tools (ChatGPT, etc.)** | *(Beginner / OK / Expert)* | |

**Language & Vocabulary Rules for This User:**

> 📝 List words or jargon that MUST be avoided in the UI and onboarding for this user.

- ❌ NEVER use: *(e.g. "API," "webhook," "pipeline," "deploy")*
- ✅ INSTEAD use: *(e.g. "connection," "automatic update," "step," "publish")*

> 💡 **EXAMPLE:**
>
> | Skill | Level | Notes |
> |---|---|---|
> | **General smartphone use** | Expert | Power user, has 80+ apps |
> | **Desktop/laptop apps (SaaS tools)** | Expert | Uses 10+ SaaS tools regularly |
> | **Spreadsheets (Excel / Sheets)** | OK | Knows formulas but not advanced features |
> | **Graphic / design tools** | Expert | Figma, Adobe CC, Canva — all fluent |
> | **Code or programming** | Beginner | Cannot read code, has no interest in it |
> | **AI tools (ChatGPT, etc.)** | OK | Uses ChatGPT for writing help |
>
> - ❌ NEVER use: "API," "webhook," "OAuth," "database," "environment"
> - ✅ INSTEAD use: "connect your tools," "auto-sync," "sign in with Google," "your data," "workspace"

---

#### 3.7 Triggers — What Makes Them Go Looking for a Solution?

> 📝 Something has to happen in a person's life before they start searching for a new product. What specific events, moments, or feelings trigger this user to finally go look for a tool like yours?
>
> These triggers are important for marketing copy, onboarding, and AI-generated emails.

List 3–5 trigger events:

1. *(e.g. "Just missed a deadline and lost a client")*
2.
3.
4.
5.

> 💡 **EXAMPLE:**
> 1. Just lost a client or got a complaint because of a missed deadline or miscommunication
> 2. Just finished a project and realized she forgot to invoice for 10+ hours of work
> 3. Just took on a new client and realized her current system won't scale to one more project
> 4. A freelancer friend showed her what organized project management looks like and she felt embarrassed
> 5. Just spent a full morning on admin instead of designing — feels burned out and frustrated

---

#### 3.8 Objections — What Might Stop Them From Using Your Product?

> 📝 Even if a user has the problem you solve, they might not sign up. What doubts, fears, or objections might hold them back? Understanding this helps you design onboarding, pricing, and your first-impression experience.

| Objection | How Your Product Should Respond |
|---|---|
| *(e.g. "This looks complicated to set up")* | *(e.g. Show setup takes under 5 minutes in onboarding)* |
| *(e.g. "I've tried tools like this before and quit")* | *(e.g. Show a before/after of their specific workflow in the first screen)* |
| *(e.g. "I don't want to pay for another subscription")* | *(e.g. Offer a free tier or 14-day trial, no credit card required)* |
| | |

> 💡 **EXAMPLE:**
>
> | Objection | How Your Product Should Respond |
> |---|---|
> | "This will take too long to learn" | Onboarding shows ONE screen: "Add your first project in 60 seconds" |
> | "I already have Notion / Trello" | Homepage shows a side-by-side: "Built for designers, not developers" |
> | "I can't afford another subscription" | Free plan covers 3 active projects — enough to prove value |
> | "I'll set it up and never use it" | Send a "day 1 nudge" email with the single most useful feature |
> | "What if my client data is not safe?" | SSL badge + one-line privacy promise visible on pricing page |

---

#### 3.9 What Does Success Look Like FOR THIS USER?

> 📝 If your product works perfectly, what is different about this user's life 90 days from now? What can they do, feel, or say that they couldn't before? Write this as a short "after" story. AI agents use this as the north star for feature decisions.

```
[Write 3–5 sentences describing the user's life after your product is working well for them]
```

> 💡 **EXAMPLE:**
>
> Ninety days after using TaskNest, Maya opens her laptop at 9 AM and is in full design mode by 9:05. She has three active clients, two in progress, and one invoice sent automatically last Friday. She hasn't looked at a spreadsheet in two months. When a client messages "where are we on the logo?" she sends them a shared progress link in one click. She feels like a professional studio — not a freelancer making it up as she goes.

---

#### 3.10 Accessibility Needs

> 📝 **Why this matters:** Real users have real physical, cognitive, and situational limitations. A freelancer working in a bright coffee shop can't see low-contrast text. A user with dyslexia needs a readable font. An older user needs larger tap targets. Capturing this here ensures your AI agents build an inclusive product from day one — not as an afterthought.
>
> Check every box that applies to this user type. Leave unchecked if not relevant.

**Visual:**
- [ ] May have color vision deficiency (color blindness) — **do not rely on color alone to convey meaning**
- [ ] May work in bright sunlight or high-glare environments — **ensure strong contrast ratios (4.5:1 minimum)**
- [ ] May have low vision — **support system font size scaling, avoid tiny text below 14px**
- [ ] No known visual considerations

**Motor / Physical:**
- [ ] May use keyboard-only navigation (no mouse)
- [ ] May use a touchscreen with limited precision (large tap targets: min 44×44px)
- [ ] May have hand tremors or limited dexterity — **avoid hover-only interactions**
- [ ] No known motor considerations

**Cognitive:**
- [ ] May have dyslexia — **use plain readable fonts (not thin, condensed, or all-caps)**
- [ ] May be easily distracted or have ADHD — **minimize popups, notifications, and visual clutter**
- [ ] May struggle with dense text or long instructions — **use short sentences, clear headings, icons**
- [ ] Non-native speaker of the product's language — **use plain, simple vocabulary**
- [ ] No known cognitive considerations

**Situational:**
- [ ] Often uses the product on mobile in low-bandwidth environments
- [ ] Often uses the product in noisy environments (no audio cues can be relied on)
- [ ] Often uses the product while multitasking (one-handed, glancing quickly)
- [ ] No known situational considerations

**Any specific accessibility requirements for this user type?**
```
[Write any additional notes here, or write "None identified yet"]
```

> 💡 **EXAMPLE (Maya — The Freelancer):**
>
> - [x] May work in bright coffee shop environments — need strong contrast
> - [x] Primarily uses trackpad on MacBook — keyboard-only navigation not required, but touch targets matter on mobile
> - [x] Non-native English speaker (significant portion of freelancers globally) — keep UI copy short and literal
> - [x] Often works while on calls or listening to music — no audio alerts can be the only signal
>
> **Notes:** Maya uses TaskNest on her phone between client meetings. Every screen must be fully usable one-handed on a 6-inch screen. Avoid hover-only states entirely.

---

#### 3.11 Where to Find This User (User Acquisition Channels)

> 📝 **Why this section?** Knowing WHERE your user hangs out online (and offline) shapes your launch strategy and helps AI agents generate the right marketing copy, onboarding emails, and growth experiments. This is NOT a marketing plan — it's a map of where your primary user already spends their attention.

**Online Channels — Where does this user spend time?**

| Channel | Specific Location | What They Go There For | Potential to Reach Them? |
|---|---|---|---|
| *(e.g. Reddit)* | *(e.g. r/freelance, r/graphic_design)* | *(e.g. Advice, venting, tool recommendations)* | *(High / Medium / Low)* |
| *(e.g. YouTube)* | *(e.g. Freelancing tutorial channels)* | *(e.g. Learning skills, workflow tips)* | *(High / Medium / Low)* |
| *(e.g. LinkedIn)* | | | |
| *(e.g. Instagram / TikTok)* | | | |
| *(e.g. Specific newsletter/podcast)* | | | |
| *(e.g. Slack community / Discord)* | | | |

**Search Intent — What does this user TYPE into Google when they have this problem?**

*(List 5–8 real search phrases your user would type. Be specific — these are future SEO keywords and ad targets.)*

1. *(e.g. "project management for freelancers")*
2.
3.
4.
5.

**Word-of-Mouth — Who does this user trust for tool recommendations?**
*(e.g. A designer friend, a YouTube creator they follow, a blog they read)*

```
[Write 2–3 sentences]
```

**First 10 Users Strategy:** How will you personally get your first 10 users?
*(Be specific — "post on Reddit" is not enough. "Post in r/freelance on Monday morning with a 'I built this for designers like me' story" is better.)*

```
[Write your plan here]
```

> 💡 **EXAMPLE (Maya — The Freelancer):**
>
> | Channel | Specific Location | What They Go There For | Potential |
> |---|---|---|---|
> | Reddit | r/freelance, r/graphic_design, r/webdesign | Venting + asking for tool recs | **High** |
> | YouTube | Charli Marie, Will Paterson, The Futur channel | Workflow and business tips | **High** |
> | Instagram | #FreelanceDesigner, #UIDesign | Inspiration, community | Medium |
> | Twitter/X | Design Twitter (#designtwitter) | Hot takes, tool debates | Medium |
> | Newsletters | Creativerly, Dense Discovery | Tool recommendations and productivity | **High** |
> | Discord | Figma Community Server, ADPList community | Real-time help + advice | Medium |
>
> **Search phrases:**
> 1. "project management app for freelancers"
> 2. "best tool for tracking freelance projects"
> 3. "how to organize freelance clients"
> 4. "freelance invoice tracker app"
> 5. "simple project management solo freelancer"
> 6. "alternatives to Asana for freelancers"
>
> **Word-of-mouth:** Maya trusts recommendations from design YouTubers she watches regularly (The Futur, Charli Marie) and threads in r/freelance where real freelancers share honest tool reviews. She is skeptical of sponsored content.
>
> **First 10 users:** Post a genuine "I built this because I was frustrated" story in r/freelance and r/graphic_design on a Tuesday morning. DM 5 freelancer designer friends directly. Offer a free lifetime account to the first 10 users who give feedback.

---

*(🔁 REPEAT SECTION 3 FOR EACH ADDITIONAL USER TYPE — copy and paste the entire section above and replace the user type nickname in the heading)*

---

## 🤖 Section 4: AI Agent Context Block

> 📝 **This section is for AI tools.** Copy and paste the block below directly into your AI coding assistant (Claude, Cursor, Copilot, etc.) at the start of any new feature or coding session. It gives the AI the exact context it needs to build the right thing.
>
> **How to use it:**
> 1. Fill in the blanks in the block below using what you've written in Sections 1–3
> 2. At the start of every AI coding session, paste it as your first message or system prompt
> 3. Update this block every time you update this document

---

### 4.1 Ready-to-Paste AI System Prompt Block

```
=== USER CONTEXT FOR THIS PROJECT ===

PRODUCT: [Product Name]
WHAT IT DOES: [Your 1-sentence description from Section 1.1]
PROBLEM SOLVED: [Your answer from Section 1.2]

PRIMARY USER: [User Type Nickname]
NAME (PERSONA): [First name from Section 3.1]
AGE: [Age range]
JOB: [Job title]
TECH LEVEL: [Beginner / Moderate / Advanced / Expert]

WHAT THEY NEED FROM THIS PRODUCT:
- [Goal #1 from Section 3.3]
- [Goal #2]
- [Goal #3]

WHAT FRUSTRATES THEM NOW:
- [Pain Point #1 from Section 3.4]
- [Pain Point #2]
- [Pain Point #3]

LANGUAGE RULES — NEVER USE IN UI:
- [Word/phrase to avoid from Section 3.6]
- [Word/phrase to avoid]

LANGUAGE RULES — ALWAYS USE INSTEAD:
- [Plain-language replacement]
- [Plain-language replacement]

SUCCESS DEFINITION: [Your answer from Section 3.9 — what does success look like for this user?]

WHAT THIS PRODUCT IS NOT: [Your answer from Section 1.3]

When building features, always ask: "Would [First Name] understand this immediately? Would it solve one of their top 3 goals or eliminate one of their top 3 pain points?"
=== END USER CONTEXT ===
```

> 💡 **EXAMPLE (filled in for TaskNest):**
>
> ```
> === USER CONTEXT FOR THIS PROJECT ===
>
> PRODUCT: TaskNest
> WHAT IT DOES: Task management app for freelance designers who hate admin work
> PROBLEM SOLVED: Freelancers waste 6+ hours/week on admin. Existing tools are built for dev teams and feel overwhelming.
>
> PRIMARY USER: The Freelancer
> NAME (PERSONA): Maya
> AGE: 27–34
> JOB: Freelance UI/UX Designer
> TECH LEVEL: Advanced (for design tools) / Beginner (for code or technical concepts)
>
> WHAT THEY NEED FROM THIS PRODUCT:
> - Know exactly what to work on today without digging through emails
> - Never miss a deadline or invoice
> - Look professional and organized in front of clients
>
> WHAT FRUSTRATES THEM NOW:
> - Spends 45+ minutes every morning figuring out where projects stand
> - Has lost $3,000+ from forgotten or late invoices
> - Existing tools feel built for software teams, not solo creatives
>
> LANGUAGE RULES — NEVER USE IN UI:
> - "API," "webhook," "OAuth," "pipeline," "deploy," "environment"
>
> LANGUAGE RULES — ALWAYS USE INSTEAD:
> - "connect," "auto-sync," "sign in with Google," "send," "publish," "workspace"
>
> SUCCESS DEFINITION: Maya opens her laptop, sees exactly what to do today in under 30 seconds, and hasn't touched a spreadsheet in 60 days.
>
> WHAT THIS PRODUCT IS NOT: Not an accounting tool. Not built for design agencies. Not a portfolio site.
>
> When building features, always ask: "Would Maya understand this immediately? Would it solve one of her top 3 goals or eliminate one of her top 3 pain points?"
> === END USER CONTEXT ===
> ```

---

### 4.2 Feature Decision Filter

> 📝 Before building ANY new feature, run it through this filter. This prevents wasted development time and keeps your AI agents from going off-track. Answer "YES" or "NO" for each question.

**Feature Being Considered:** `[Write the feature name here]`

| Question | Answer (YES / NO) | Notes |
|---|---|---|
| Would [Primary User Name] use this feature at least once per week? | | |
| Does this feature solve one of their top 3 pain points? | | |
| Can [Primary User Name] understand what this does in under 5 seconds? | | |
| Does this fit within what the product IS (not what it is NOT)? | | |
| Is this something the primary user would actively search for? | | |
| Can it be built without confusing or cluttering the core experience? | | |
| **TOTAL YES answers:** | **___ / 6** | |

> **Decision Rule:**
> - **5–6 YES:** Build it. High priority.
> - **3–4 YES:** Consider it for a later version. Not now.
> - **0–2 YES:** Do NOT build it. Even if it sounds cool.

> 💡 **EXAMPLE:**
>
> **Feature Being Considered:** `AI-powered client communication suggestions`
>
> | Question | Answer | Notes |
> |---|---|---|
> | Would Maya use this at least once per week? | YES | She emails clients constantly |
> | Does this solve one of her top 3 pain points? | YES | Saves time on admin/writing |
> | Can Maya understand what this does in under 5 seconds? | YES | "AI writes your client update" is clear |
> | Does this fit within what the product IS? | YES | Fits project management + communication |
> | Is this something Maya would actively search for? | YES | "Save time on client emails" = her pain |
> | Can it be built without cluttering the core experience? | YES | Hide behind a button, not front-and-center |
> | **TOTAL YES answers:** | **6 / 6** | |
>
> **Decision: Build it. High priority.**

---

### 4.3 Claude-Specific System Prompt (Copy into Claude Projects)

> 📝 **What is this?** Claude Projects lets you save a custom system prompt that Claude reads at the start of every conversation in that project. Paste the block below into your Claude Project's **"Project Instructions"** field. This means every conversation in that project — whether you're writing code, designing features, or planning marketing — starts with Claude knowing exactly who your user is.
>
> **How to use:**
> 1. Open Claude → click **"Projects"** → create a project for your product
> 2. Click **"Edit Project Instructions"**
> 3. Fill in the block below and paste it there

```xml
<project_context>
  <product>
    <name>[Product Name]</name>
    <description>[One-sentence description from Section 1.1]</description>
    <problem_solved>[Answer from Section 1.2]</problem_solved>
    <not_this_product>
      - [Anti-scope item 1 from Section 1.3]
      - [Anti-scope item 2]
      - [Anti-scope item 3]
    </not_this_product>
  </product>

  <primary_user>
    <nickname>[User Type Nickname from Section 2]</nickname>
    <persona_name>[First name from Section 3.1]</persona_name>
    <age>[Age range]</age>
    <job>[Job title]</job>
    <tech_level>[Beginner / Moderate / Advanced / Expert]</tech_level>
    <location>[Location]</location>
  </primary_user>

  <user_goals>
    <goal priority="1">[Top goal from Section 3.3]</goal>
    <goal priority="2">[Second goal]</goal>
    <goal priority="3">[Third goal]</goal>
  </user_goals>

  <user_pain_points>
    <pain>[Pain point #1 from Section 3.4]</pain>
    <pain>[Pain point #2]</pain>
    <pain>[Pain point #3]</pain>
  </user_pain_points>

  <language_rules>
    <never_use>[Word/phrase to avoid]</never_use>
    <never_use>[Word/phrase to avoid]</never_use>
    <always_use_instead>[Plain language replacement]</always_use_instead>
    <always_use_instead>[Plain language replacement]</always_use_instead>
  </language_rules>

  <success_definition>[Answer from Section 3.9 — what success looks like for the user]</success_definition>

  <acquisition_channels>
    <channel>[Top channel from Section 3.11]</channel>
    <channel>[Second channel]</channel>
  </acquisition_channels>
</project_context>

<instructions>
You are a Senior Product Engineer and Technical Writer working on [Product Name].

Always make decisions through the lens of the primary user ([Persona Name], described above).

Before suggesting any feature, copy, or technical solution, silently ask yourself:
1. Would [Persona Name] understand this immediately?
2. Does this serve one of her top 3 goals or eliminate one of her top 3 pain points?
3. Does this fit within what the product IS (not what it is NOT)?

If the answer to any of these is NO, suggest a simpler alternative or flag the concern.

Use plain, friendly language in all UI copy. Never use technical jargon in anything the user sees.
</instructions>
```

> 💡 **EXAMPLE (TaskNest, filled in):**
>
> ```xml
> <project_context>
>   <product>
>     <name>TaskNest</name>
>     <description>Task management app for freelance designers who hate admin work</description>
>     <problem_solved>Freelancers waste 6+ hours/week on admin. Existing tools are built for software teams and feel overwhelming for solo creatives.</problem_solved>
>     <not_this_product>
>       - Not a full accounting or invoicing platform
>       - Not built for design agencies with teams
>       - Not a portfolio or client showcase website
>     </not_this_product>
>   </product>
>
>   <primary_user>
>     <nickname>The Freelancer</nickname>
>     <persona_name>Maya</persona_name>
>     <age>27–34</age>
>     <job>Freelance UI/UX Designer</job>
>     <tech_level>Advanced for design tools / Beginner for technical concepts</tech_level>
>     <location>Mid-size US cities — Austin, Denver, Nashville</location>
>   </primary_user>
>
>   <user_goals>
>     <goal priority="1">Know exactly what to work on today without digging through emails</goal>
>     <goal priority="2">Never miss a deadline or lose money on forgotten invoices</goal>
>     <goal priority="3">Look and feel like a professional studio to clients</goal>
>   </user_goals>
>
>   <user_pain_points>
>     <pain>Spends 45+ minutes every morning figuring out where projects stand</pain>
>     <pain>Has lost $3,000+ from forgotten or late invoices</pain>
>     <pain>Existing tools feel like they were built for NASA, not a solo creative</pain>
>   </user_pain_points>
>
>   <language_rules>
>     <never_use>API, webhook, OAuth, pipeline, deploy, environment, database</never_use>
>     <always_use_instead>connect, auto-sync, sign in with Google, send, publish, workspace</always_use_instead>
>   </language_rules>
>
>   <success_definition>Maya opens her laptop, sees exactly what to do today in 30 seconds, and has not touched a spreadsheet in 60 days.</success_definition>
>
>   <acquisition_channels>
>     <channel>Reddit: r/freelance, r/graphic_design</channel>
>     <channel>YouTube: design workflow channels (The Futur, Charli Marie)</channel>
>   </acquisition_channels>
> </project_context>
>
> <instructions>
> You are a Senior Product Engineer and Technical Writer working on TaskNest.
> Always make decisions through the lens of Maya (The Freelancer), described above.
> Before suggesting any feature, copy, or technical solution, silently ask yourself:
> 1. Would Maya understand this immediately?
> 2. Does this serve one of her top 3 goals or eliminate one of her top 3 pain points?
> 3. Does this fit within what TaskNest IS (not what it is NOT)?
> If the answer to any of these is NO, suggest a simpler alternative or flag the concern.
> Use plain, friendly language in all UI copy. Never use technical jargon in anything the user sees.
> </instructions>
> ```

---

### 4.4 AI Agent Task Delegation Block

> 📝 **What is this?** When you use AI agent workflows (e.g. multi-step Claude pipelines, Cursor agents, AutoGPT-style flows, or custom agent systems), each sub-agent that handles a piece of work needs to know who the user is — even if it only sees a small slice of the project.
>
> Copy and paste the relevant block below at the top of each sub-agent's task prompt. Choose the block that matches what the agent is doing.

---

**Block A: For agents writing UI copy, error messages, or onboarding flows**

```
[USER CONTEXT — UI COPY AGENT]
You are writing UI text for [Product Name].

The primary user is [Persona Name], a [age]-year-old [job title].
Tech level: [Beginner / Moderate / Advanced / Expert].

RULES:
- Write at a [Grade 6 / Grade 8 / Grade 10] reading level (choose based on tech level)
- Never use: [list words to avoid from Section 3.6]
- Always use instead: [plain language alternatives]
- Every button label, error message, and tooltip must be understandable in under 3 seconds
- When in doubt, use shorter words and fewer of them

USER'S EMOTIONAL STATE when they see this UI: [e.g. "Slightly overwhelmed, in a hurry, wants to feel in control"]
```

---

**Block B: For agents writing features, APIs, or database schemas**

```
[USER CONTEXT — ENGINEERING AGENT]
You are building a feature for [Product Name].

The primary user is [Persona Name], a [job title].
They are NOT a developer. They will never see code, config files, or technical error details.

USER'S TOP 3 GOALS this feature must serve:
1. [Goal from Section 3.3]
2. [Goal 2]
3. [Goal 3]

USER'S TOP 3 PAIN POINTS this feature must eliminate or reduce:
1. [Pain point from Section 3.4]
2. [Pain 2]
3. [Pain 3]

SUCCESS CONDITION: The feature is done when [Persona Name] can complete [specific task] in under [N] steps without any instructions or tooltips.

ANTI-SCOPE: This feature must NOT require the user to [list anything that goes beyond their tech comfort level].
```

---

**Block C: For agents running market research, user interview synthesis, or analytics**

```
[USER CONTEXT — RESEARCH AGENT]
You are analyzing data about users of [Product Name].

The EXPECTED primary user profile is:
- Nickname: [User Type Nickname]
- Age: [Age range]
- Job: [Job title]
- Location: [Location]
- Tech level: [Level]
- Key goals: [Goals from Section 3.3]
- Key pain points: [Pain points from Section 3.4]

Your task: [Describe what the agent should analyze or research]

Flag any findings that:
1. Contradict the expected user profile above
2. Suggest a new user type we haven't accounted for
3. Indicate that our assumptions about pain points were wrong

Output format: Start with a one-paragraph summary of whether real user behavior matches the expected profile. Then list findings.
```

> 💡 **EXAMPLE — Block B filled in for TaskNest:**
>
> ```
> [USER CONTEXT — ENGINEERING AGENT]
> You are building the "Invoice Reminder" feature for TaskNest.
>
> The primary user is Maya, a freelance UI/UX designer.
> She is NOT a developer. She will never see code, config files, or technical error details.
>
> USER'S TOP 3 GOALS this feature must serve:
> 1. Get paid on time without having to manually track invoice dates
> 2. Look professional and organized in front of clients
> 3. Spend less than 30 minutes per day on admin
>
> USER'S TOP 3 PAIN POINTS this feature must eliminate:
> 1. Forgot to invoice for completed work and lost $3,000+ last year
> 2. Has to manually check every project to see if it was invoiced
> 3. Feels embarrassed chasing clients for payment
>
> SUCCESS CONDITION: The feature is done when Maya can set up automatic invoice reminders for a project in under 3 clicks, with no configuration screens or technical options visible.
>
> ANTI-SCOPE: This feature must NOT require Maya to understand payment APIs, set up bank connections, or configure webhooks. It sends a reminder email — nothing more in v1.0.
> ```

---

## ✅ Section 5: Core Use Cases — What the User MUST Be Able To Do

> 📝 List the TOP 5 things your primary user absolutely MUST be able to do with your product. These become your v1.0 feature requirements. If a user cannot do all 5 of these things, the product is not ready to launch.
>
> Write each use case as: "As [User Nickname], I need to [action] so that [outcome]."

| # | Use Case | Priority (Must Have / Nice to Have) |
|---|---|---|
| 1 | As [User Nickname], I need to _____ so that _____ | **Must Have** |
| 2 | As [User Nickname], I need to _____ so that _____ | **Must Have** |
| 3 | As [User Nickname], I need to _____ so that _____ | **Must Have** |
| 4 | As [User Nickname], I need to _____ so that _____ | Must Have |
| 5 | As [User Nickname], I need to _____ so that _____ | Nice to Have |

> 💡 **EXAMPLE:**
>
> | # | Use Case | Priority |
> |---|---|---|
> | 1 | As The Freelancer, I need to see all my active projects on one screen so that I know exactly what to work on today | **Must Have** |
> | 2 | As The Freelancer, I need to track revision rounds per project so that I never do free work again | **Must Have** |
> | 3 | As The Freelancer, I need to send an invoice with one click so that I get paid on time | **Must Have** |
> | 4 | As The Freelancer, I need to set a deadline and get a reminder 48 hours before so that I never miss a client due date | **Must Have** |
> | 5 | As The Freelancer, I need to share a project status link with my client so that they stop emailing me for updates | Nice to Have |

---

## 🚫 Section 6: What Users Do NOT Need (Anti-Scope)

> 📝 List features that SOUND useful but are NOT what your primary user needs. This is your "no-build" list. Share it with your AI agents so they don't suggest or build these.
>
> Being clear about what you WON'T build is just as important as knowing what you will build.

| Feature That Sounds Good | Why This User Doesn't Actually Need It |
|---|---|
| *(e.g. Gantt chart timeline view)* | *(e.g. Maya works alone — Gantt charts are for teams with dependencies)* |
| | |
| | |
| | |

> 💡 **EXAMPLE:**
>
> | Feature That Sounds Good | Why Maya Doesn't Actually Need It |
> |---|---|
> | Gantt chart / timeline view | She works alone — Gantt charts are for multi-person teams with complex dependencies |
> | Team collaboration / comments | Her "team" is just her. Adding collaboration features would confuse the UI |
> | Time tracking / billable hours | Nice, but scope creep — she doesn't bill hourly, she bills per project |
> | Client CRM / contact management | She has fewer than 10 clients — her email is fine for this |
> | Budget / expense tracking | This belongs in accounting software, not TaskNest |

---

## 🏁 Section 7: Milestone Validation Checkpoints

> 📝 **Why this section?** Your understanding of the user will change as real people use your product. This section is a set of checkpoints where you STOP and ask: "Is this still the right user? Did our assumptions hold up?"
>
> **When to use each checkpoint:**
> - **Checkpoint 1 (Discovery):** Fill in BEFORE writing any code
> - **Checkpoint 2 (Beta / 10 Users):** Fill in after your first 10 real users
> - **Checkpoint 3 (Launch / 100 Users):** Fill in after your first 100 sign-ups
> - **Checkpoint 4 (Growth / 500 Users):** Fill in after reaching 500 customers

---

### 🔵 Checkpoint 1: Discovery (Before You Build)

**Date:** `[Date you filled this out]`
**Status:** `[ ] Not started / [ ] In progress / [ ] Complete`

| Assumption You're Making About the User | How You Will Validate It | Confidence Level (Low / Medium / High) |
|---|---|---|
| *(e.g. Freelance designers lose money on forgotten invoices)* | *(e.g. Interview 5 freelancers before building)* | *(e.g. Medium — heard this in 2 conversations)* |
| | | |
| | | |

**Have you talked to at least 3 real potential users before building?**
- [ ] Yes — here's what I learned: `[Write 2–3 sentences]`
- [ ] No — here's my plan to do so: `[Write when and how you will talk to users]`

---

### 🟡 Checkpoint 2: Beta (First 10 Users)

**Date:** `[Date you reached 10 users]`
**Status:** `[ ] Not started / [ ] In progress / [ ] Complete`

**Did the right type of user sign up?**
- [ ] YES — most users match the primary user profile
- [ ] PARTIALLY — some match, some don't (explain below)
- [ ] NO — different users showed up (explain below)

**Notes:** `[What did you observe? Who actually signed up vs. who you expected?]`

**Top 3 things users did that you did NOT expect:**
1.
2.
3.

**Do you need to update the User Profile?**
- [ ] Yes — what changed: `[Write what changed about your understanding of the user]`
- [ ] No — original profile holds

---

### 🟠 Checkpoint 3: Launch (First 100 Users)

**Date:** `[Date you reached 100 users]`
**Status:** `[ ] Not started / [ ] In progress / [ ] Complete`

**User Snapshot at 100:**

| Metric | Target | Actual | Match? |
|---|---|---|---|
| % of users matching primary user profile | *(e.g. 80%)* | *(Track in your analytics)* | *(YES / NO)* |
| Most-used feature | *(e.g. Project dashboard)* | *(Check your analytics)* | |
| Least-used feature | *(e.g. Invoice templates)* | *(Check your analytics)* | |
| Top support request / complaint | *(e.g. "I can't find X")* | *(From support inbox)* | |

**What has changed about your understanding of the user?**
`[Write 3–5 sentences. Are they who you thought they were?]`

**Feature Decision Review:** Go back to Section 6 (Anti-Scope). Are any of those features now being REQUESTED by real users?
- [ ] No — stay the course
- [ ] Yes — requests for: `[List features]` — update decision in Section 6

---

### 🟢 Checkpoint 4: Growth (First 500 Customers)

**Date:** `[Date you reached 500 paying or active customers]`
**Status:** `[ ] Not started / [ ] In progress / [ ] Complete`

**Are there user types you didn't expect that represent 15%+ of your users?**
- [ ] No — one clear primary user as expected
- [ ] Yes — a new user type emerged: `[Describe them]`

**If a new user type emerged:**
> 📝 Go back to Section 2 and add them as a new user type. Then complete a full Section 3 profile for them. Decide: should they become your new primary user for v2.0?

**User Health Score at 500:**

| Question | Your Answer |
|---|---|
| What % of users are active weekly? | |
| What is the #1 reason users stay? | |
| What is the #1 reason users cancel/leave? | |
| What do your best users (top 20%) have in common? | |
| Has your primary user definition changed from v1.0? | YES / NO |

**If your primary user definition changed:** What changed and why?
`[Write here]`

**Version 2.0 User Decision:**
Based on everything learned from 500 customers, who is the primary user for the NEXT version?
`[Write 2–3 sentences — same user with new needs, or a new user type entirely?]`

---

## 📌 Section 8: User Assumptions Log

> 📝 Every product starts with assumptions. Write them all down here so you can track which ones were right and which ones were wrong. This is one of the most valuable learning tools in your project.

| # | Assumption | Date Written | Validated? | What We Learned |
|---|---|---|---|---|
| 1 | *(e.g. Freelancers lose money on invoicing)* | *(Date)* | *(YES / NO / PARTIAL)* | *(Write what you actually discovered)* |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

---

## 📜 Section 9: Document Change Log

> 📝 Every time you update this document, add a row to this log. This helps your team (and your AI agents) know which version of the user definition they're working with.

| Version | Date | Changed By | What Changed |
|---|---|---|---|
| v1.0 | *(Date)* | *(Your name)* | Initial draft — created before development |
| v1.1 | | | *(e.g. Updated pain points after 10-user beta interviews)* |
| v1.2 | | | |

---

## 🔗 Section 10: Related Documents

> 📝 Link to other project documents here so everything is connected. This helps your AI agents and team find the full picture.

| Document Name | Location / Link | Status |
|---|---|---|
| Project Overview / PRD | *(Link or file path)* | *(Draft / Final)* |
| Define the Problem | *(Link or file path)* | |
| Define the Features | *(Link or file path)* | |
| Define the Architecture | *(Link or file path)* | |
| User Interview Notes | *(Link or file path)* | |
| Analytics Dashboard | *(Link or file path)* | |

---

> ---
> ## ✅ Final Checklist Before You Share This Document
>
> Run through this before sharing with your team or AI agents:
>
> - [ ] Section 1 (Product Context) is filled in completely
> - [ ] At least 1 full User Profile is complete in Section 3 (3.1–3.11)
> - [ ] Competitor comparison table (Section 3.5a) has at least 3 rows filled
> - [ ] Accessibility needs (Section 3.10) are checked for the primary user
> - [ ] User acquisition channels (Section 3.11) have at least 3 channels and 5 search phrases
> - [ ] The AI Agent Context Block (Section 4.1) is filled and ready to paste into Cursor / Copilot
> - [ ] The Claude System Prompt (Section 4.3) is pasted into your Claude Project Instructions
> - [ ] The Feature Decision Filter (Section 4.2) has been used at least once
> - [ ] At least 5 Core Use Cases are listed in Section 5
> - [ ] At least 3 Anti-Scope items are listed in Section 6
> - [ ] Checkpoint 1 (Discovery) in Section 7 is complete
> - [ ] No section was left blank (write "Unknown — to be validated" if genuinely unsure)
> - [ ] The Change Log in Section 9 has at least one row (v1.0)
>
> **If all boxes are checked: This document is ready. Share it. 🚀**

---

*Template created for AI-Driven Development Life Cycle (ADLC) | Version 1.0 | October 2026*
*Covers: Discovery → Beta (10 users) → Launch (100 users) → Growth (500 customers)*
