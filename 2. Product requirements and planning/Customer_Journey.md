# 🗺️ Customer Journey Template
### AI-Driven Development Life Cycle — From First Build to First 500 Customers
**Template Version:** 1.0.0  
**Template Author:** [Your Name or Team Name]  
**Last Updated:** [YYYY-MM-DD]  
**Compatible With:** SaaS / Web Apps · Mobile Apps · AI-Native Products  

---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- 📖 HOW TO FILL THIS DOCUMENT                                         -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 📖 How to Fill This Document

> **Start here before touching anything else. Read this section once.**

## What Is a Customer Journey?

A **Customer Journey** is the story of one real person — your customer — from the moment they first hear about your product all the way to becoming a loyal, paying, referring customer.

Think of it like a storyboard for a movie. Each phase is a scene. Your job is to describe **what the customer sees, feels, does, and needs** at every scene — and how your AI-powered product helps them move forward.

---

## Step-by-Step Filling Guide

Follow these steps **in order**:

| Step | What to do | Time needed |
|------|-----------|-------------|
| **1** | Fill in **Part 0 — Project Snapshot** first. This sets context for every other section. | 15 min |
| **2** | Read the **Persona Card** instructions and describe your customer like you're telling a friend. | 20 min |
| **3** | Fill **Phase 1 → Phase 4** in order. Each phase has clear prompts. | 30 min each |
| **4** | Use the **🤖 AI Prompt Starters** at the bottom of each section if you get stuck. | As needed |
| **5** | Fill the **First 500 Customers Milestone Tracker** at the end. | 20 min |
| **6** | Review everything once and mark `[TODO]` on anything you'll fill in later. | 10 min |

---

## Symbols Used in This Template

| Symbol | Meaning |
|--------|---------|
| `[YOUR TEXT HERE]` | Replace this with your actual content |
| `[TODO]` | Come back and fill this later |
| `[EXAMPLE: ...]` | An example to help you. **Delete the example** when done. |
| `🤖 AI Prompt` | Paste this into Claude/ChatGPT to help you fill the section |
| `⚠️ Important` | Do not skip this — it's critical |
| `💡 Tip` | A helpful hint for beginners |
| `📏 Metric` | A number you will track here |

---

## Golden Rules

1. **Write like you're talking to a friend, not writing a report.** Simple language is better.
2. **One sentence per bullet point.** Don't write paragraphs inside bullet points.
3. **Be specific.** "Users sign up quickly" is bad. "Users sign up in under 60 seconds" is good.
4. **Leave nothing blank.** If you don't know something yet, write `[TODO — by DATE]`.
5. **Update this document every sprint.** It is a living document, not a one-time write.

---
---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- PART 0: PROJECT SNAPSHOT                                              -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 🧩 Part 0 — Project Snapshot

> **💡 Tip:** Fill this part first. Every other section references this.

---

## 0.1 — Product Identity Card

| Field | Your Answer |
|-------|-------------|
| **Product Name** | `[YOUR PRODUCT NAME]` |
| **One-Line Description** | `[What does it do? For whom? e.g., "AI email writer for solo founders who hate writing"]` |
| **Category** | `[ ] SaaS Web App  [ ] Mobile App  [ ] AI Agent  [ ] API/Dev Tool  [ ] Other: ___` |
| **Platform(s)** | `[e.g., Web (Chrome), iOS, Android, Slack, etc.]` |
| **Stage Right Now** | `[ ] Idea  [ ] Building MVP  [ ] Beta  [ ] Launched  [ ] Growing` |
| **Target Launch Date** | `[YYYY-MM-DD]` |
| **Date First 500 Goal** | `[YYYY-MM-DD — when do you want to reach 500 customers?]` |
| **Document Owner** | `[Your Name]` |
| **Project Repository** | `[Link to GitHub / GitLab / Notion]` |

---

## 0.2 — The Customer Persona Card

> **💡 Tip:** Give your customer a fake name and describe them like a real person. This makes it much easier to write the rest of this document.

### Persona 1 — Primary Customer

```
Name (made up):     [e.g., "Sarah"]
Age:                [e.g., 32]
Job / Role:         [e.g., Solo Founder running an e-commerce brand]
Tech comfort level: [ ] Beginner  [ ] Intermediate  [ ] Expert
Where they spend time online: [e.g., LinkedIn, Twitter/X, YouTube]
Biggest daily frustration:    [e.g., Spends 3 hours a day writing product descriptions]
What they dream about:        [e.g., Launching a product and getting paid while they sleep]
How they find new tools:      [e.g., Google Search, friend recommendations, Product Hunt]
Budget they control:          [e.g., $0–$100/month on tools]
Device they mostly use:       [ ] Desktop browser  [ ] iPhone  [ ] Android  [ ] Tablet
```

### Persona 2 — Secondary Customer *(optional)*

```
Name (made up):     [e.g., "Dev"]
Age:                [e.g., 25]
Job / Role:         [TODO]
Tech comfort level: [ ] Beginner  [ ] Intermediate  [ ] Expert
Biggest daily frustration:    [TODO]
How they find new tools:      [TODO]
```

> 🤖 **AI Prompt — Persona Builder:**
> ```
> I am building a [PRODUCT TYPE] called [PRODUCT NAME].
> It helps [TARGET USER] to [MAIN BENEFIT].
> Please create 2 detailed user personas with: name, age, job, frustrations,
> goals, tech comfort, where they hang out online, and budget for tools.
> Format it as a table.
> ```

---

## 0.3 — The Core Problem & Solution Statement

> ⚠️ **Important:** Fill this before writing any phase. Every phase touchpoint should connect back to this.

### Problem Statement

**The customer faces this problem:**  
`[Describe the problem in 2–3 sentences. Write from the customer's perspective. e.g., "Sarah spends 3 hours every day writing product descriptions for her online store. She's not a writer and the descriptions she writes don't convert well. She knows AI tools exist but doesn't know which one to trust."]`

**Without your product, they currently:**  
- `[What do they do instead? e.g., Hire a freelance copywriter for $200/week]`
- `[Another workaround they use]`
- `[Another workaround they use]`

### Solution Statement

**Your product solves this by:**  
`[Describe your solution in 2–3 sentences. Be concrete. e.g., "Our AI agent learns Sarah's brand voice in 5 minutes, then generates conversion-optimized product descriptions in seconds — directly inside her Shopify dashboard."]`

**Your unfair advantage (what makes you different):**  
`[What does your product do that no competitor does? Be honest and specific.]`

> 🤖 **AI Prompt — Problem/Solution:**
> ```
> My product is called [PRODUCT NAME]. 
> Target customer: [PERSONA DESCRIPTION].
> Core problem they face: [DESCRIBE IN YOUR WORDS].
> My solution: [DESCRIBE IN YOUR WORDS].
> 
> Please rewrite the Problem Statement and Solution Statement in clear,
> simple language that a non-technical person would instantly understand.
> Include an "unfair advantage" that differentiates this product.
> ```

---
---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- PHASE 1: AWARENESS → ACQUISITION                                      -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 🔦 Phase 1 — Awareness → Acquisition

> **What this phase is about:**  
> The customer doesn't know you exist yet. This phase covers everything from the moment they first **hear about your product** to the moment they **sign up or download it**.  
> **Think of this like:** A stranger seeing your store window and walking through the door.

---

## 1.1 — Customer Awareness Journey

> **💡 Tip:** Pick the channels where your persona actually spends time — don't list every possible channel.

### How does your customer currently discover tools like yours?

| Discovery Channel | Is This Relevant? | Your Specific Plan |
|-------------------|------------------|-------------------|
| Google / Bing Search | `[ ] Yes  [ ] No` | `[e.g., Target keyword: "AI product description writer"]` |
| Social Media (LinkedIn) | `[ ] Yes  [ ] No` | `[TODO]` |
| Social Media (X/Twitter) | `[ ] Yes  [ ] No` | `[TODO]` |
| YouTube / Reels / TikTok | `[ ] Yes  [ ] No` | `[TODO]` |
| Product Hunt Launch | `[ ] Yes  [ ] No` | `[TODO]` |
| Newsletter / Email | `[ ] Yes  [ ] No` | `[TODO]` |
| Podcast / Webinar | `[ ] Yes  [ ] No` | `[TODO]` |
| Community (Reddit, Discord, Slack) | `[ ] Yes  [ ] No` | `[TODO]` |
| Friend / Colleague Referral | `[ ] Yes  [ ] No` | `[TODO]` |
| Paid Ads (Google, Meta) | `[ ] Yes  [ ] No` | `[TODO]` |
| App Store (iOS / Android) | `[ ] Yes  [ ] No` | `[TODO]` |

### Top 3 Acquisition Channels *(prioritized)*

1. `[Channel #1 — e.g., SEO Blog posts targeting "AI for e-commerce"]`
2. `[Channel #2 — e.g., LinkedIn posts by founder showing live product demos]`
3. `[Channel #3 — e.g., Product Hunt launch on Day 1]`

---

## 1.2 — The First Impression (Landing / App Store Page)

> This is your **shop window**. The customer has 8 seconds to decide if they stay or leave.

### Landing Page / App Store Page Checklist

| Element | Done? | Notes |
|---------|-------|-------|
| **Headline** — What is it + who is it for | `[ ] Yes  [ ] No` | `[e.g., "Write 10x more product listings in 10 minutes"]` |
| **Sub-headline** — One-sentence elaboration | `[ ] Yes  [ ] No` | `[TODO]` |
| **Hero Visual** — Screenshot, GIF, or video of product | `[ ] Yes  [ ] No` | `[TODO]` |
| **3 Core Benefits** (not features) | `[ ] Yes  [ ] No` | `[TODO]` |
| **Social Proof** — Testimonial or "X users" badge | `[ ] Yes  [ ] No` | `[TODO]` |
| **Clear CTA button** (Sign up / Download / Try Free) | `[ ] Yes  [ ] No` | `[TODO]` |
| **No password required** (or "Sign in with Google") | `[ ] Yes  [ ] No` | `[TODO]` |
| **Mobile responsive** | `[ ] Yes  [ ] No` | `[TODO]` |
| **Page load speed < 3 seconds** | `[ ] Yes  [ ] No` | `[TODO]` |

### Your Primary Call-to-Action (CTA)

```
CTA Button Text:  [e.g., "Try it free — no credit card needed"]
Where it links:   [e.g., /signup page]
Secondary CTA:    [e.g., "Watch 2-min demo"]
```

---

## 1.3 — Sign-Up / Download Flow

> **💡 Tip:** The fewer steps to sign up, the more people will complete it. Aim for under 60 seconds.

### Sign-Up Steps (map your current flow)

```
Step 1: [e.g., Click "Get Started" on landing page]
Step 2: [e.g., Enter email + password OR click "Sign in with Google"]
Step 3: [e.g., Verify email (if required)]
Step 4: [e.g., Answer 2 onboarding questions]
Step 5: [e.g., Land on dashboard for first time]

Total estimated time for a new user: [__ minutes __ seconds]
```

### Friction Points to Remove

> List anything that could make a user give up during sign-up:
- `[e.g., Forcing a credit card before the user sees value]`
- `[e.g., Email verification with a 5-minute wait]`
- `[TODO]`

---

## 1.4 — 🤖 AI Agent Touchpoints in Phase 1

> **💡 What is an AI Agent Touchpoint?** A moment in the customer journey where an AI does something automatically to help the customer — like a chatbot, a smart recommendation, or an auto-filled form.

| Touchpoint | What the AI Does | Channel |
|------------|-----------------|---------|
| `[e.g., AI chatbot on landing page]` | `[e.g., Answers "what does this do?" questions in real-time]` | `[Web Widget]` |
| `[e.g., AI-powered exit intent popup]` | `[e.g., Detects when user is leaving and shows a personalized offer]` | `[Web]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

### 🧠 Prompt / LLM Design Notes for Phase 1

> **What is this?** If your AI agent talks to customers in this phase, write what it should say and how it should behave here.

```
AI Agent Name/Role:   [e.g., "Luna — our landing page AI assistant"]
Tone:                 [e.g., Friendly, concise, never pushy]
Primary Goal:         [e.g., Answer the top 5 questions visitors ask, then guide to sign-up]
What it should NOT say: [e.g., Never mention competitor pricing, never make pricing promises]
Fallback behavior:    [e.g., If it can't answer, collect email and say "We'll follow up in 24h"]

Sample prompt system instruction:
"""
You are Luna, a helpful AI assistant for [PRODUCT NAME].
Your job is to help visitors understand what [PRODUCT NAME] does and
encourage them to try it for free. Be warm, concise, and helpful.
Never discuss competitor products. If asked about pricing, direct them to /pricing.
If you cannot answer a question, say: "Great question! Let me get a human to follow up."
"""
```

---

## 1.5 — Phase 1 Success Metrics

> **💡 Tip:** Pick 3–5 numbers you'll actually track. Too many metrics = tracking nothing.

| Metric | Definition | Your Target | Current Baseline |
|--------|-----------|-------------|-----------------|
| **Website Visitors** | Monthly unique visitors | `[e.g., 1,000/month by Month 1]` | `[TODO]` |
| **Landing Page Conversion Rate** | % of visitors who click sign-up | `[e.g., 5–10%]` | `[TODO]` |
| **Sign-Up Completion Rate** | % who start sign-up and finish it | `[e.g., > 70%]` | `[TODO]` |
| **Cost per Acquisition (CPA)** | Avg. cost to acquire 1 user | `[e.g., < $10 during beta]` | `[TODO]` |
| **Top Traffic Source** | Which channel sends the most signups | `[TODO]` | `[TODO]` |

### Phase 1 Exit Criteria *(When is Phase 1 "working"?)*

> You know Phase 1 is healthy when:
- `[ ]` `[e.g., At least 100 sign-ups per month coming in organically]`
- `[ ]` `[e.g., Landing page converts at > 5%]`
- `[ ]` `[e.g., Sign-up flow completes in < 60 seconds]`

> 🤖 **AI Prompt — Phase 1 Metrics:**
> ```
> My product is [PRODUCT NAME]. It is a [TYPE] for [PERSONA].
> We are launching to our first 500 customers.
> What are the 5 most important acquisition metrics I should track,
> with realistic benchmark ranges for an early-stage AI product?
> Format as a table with: Metric Name | Why It Matters | Benchmark Range | How to Track.
> ```

---
---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- PHASE 2: ONBOARDING → ACTIVATION                                      -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 🚀 Phase 2 — Onboarding → Activation

> **What this phase is about:**  
> The customer just signed up. They are inside your product for the **very first time**. This phase covers everything from that first login to the moment they experience the **"Aha! This works!"** feeling.  
> **Think of this like:** A new employee's first day at work — make it welcoming and productive.

---

## 2.1 — The "Aha Moment" Definition

> ⚠️ **Important:** The "Aha Moment" is the single most important moment in your customer journey. It's the moment the customer **feels the value** of your product for the first time.

### Define Your Aha Moment

```
The moment of value happens when the customer:
[Describe the exact action or outcome. e.g., "Generates their first AI product 
description and sees it's better than what they'd write manually — within 3 minutes 
of signing up."]

This should happen within:
[ ] 60 seconds of signing up
[ ] 5 minutes
[ ] First session (< 30 minutes)
[ ] First day
[ ] Other: ___________

The customer's emotion at this moment:
[e.g., "Wow, it actually works! This just saved me an hour."]
```

---

## 2.2 — Onboarding Flow Map

> **💡 Tip:** Draw this like a flowchart using text. Every step should push the user toward the Aha Moment faster.

### First Session Steps

```
[START] User logs in for the first time
    │
    ▼
Step 1: [e.g., Welcome screen with a 30-second product tour video]
    │
    ▼
Step 2: [e.g., AI asks 2 setup questions: "What's your brand name?" + "What do you sell?"]
    │
    ▼
Step 3: [e.g., AI generates a sample output using their real data — in 10 seconds]
    │
    ▼
Step 4: [e.g., User edits or approves the output]
    │
    ▼
Step 5: [e.g., AI confirms: "You just saved 45 minutes! 🎉" + shows dashboard]
    │
    ▼
[AHA MOMENT ✨] — User sees real value. Session complete.
```

### Onboarding Checklist for the User

> These are the milestones you want **the user** to hit in their first session:
- `[ ]` `[e.g., Completed profile setup]`
- `[ ]` `[e.g., Connected their first data source / account]`
- `[ ]` `[e.g., Generated their first AI output]`
- `[ ]` `[e.g., Saved or exported a result]`
- `[ ]` `[e.g., Invited one teammate (if applicable)]`

---

## 2.3 — Empty State Design

> **What is an "empty state"?** It's what the user sees when they log in and have NO data yet. A bad empty state = user confusion. A good empty state = user is guided to take action.

### Empty State Strategy

| Screen | What the user sees when empty | What your product shows instead |
|--------|------------------------------|--------------------------------|
| `[e.g., Dashboard]` | `[Blank screen with no data]` | `[e.g., A sample project pre-loaded with their name to show what it looks like]` |
| `[e.g., Projects list]` | `[Blank list]` | `[e.g., "Create your first project" button with a one-click template]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

---

## 2.4 — Onboarding Emails / Push Notifications Sequence

> **💡 Tip:** Even if your product is great, some users will sign up and never come back. A well-timed email sequence brings them back.

| # | Trigger | Timing | Subject Line | Goal |
|---|---------|--------|-------------|------|
| 1 | User signs up | Immediately | `[e.g., "Welcome to [Product] — here's how to get started in 3 min"]` | `[Confirm signup, link to tutorial]` |
| 2 | User hasn't logged in again | Day 2 | `[e.g., "Did you try [Product] yet? Pick up where you left off"]` | `[Drive return visit]` |
| 3 | User logged in but didn't hit Aha Moment | Day 3 | `[e.g., "Let us help — here's a 60-second setup video"]` | `[Remove friction]` |
| 4 | User hit Aha Moment | Day 5 | `[e.g., "You're on fire 🔥 — here's what to do next"]` | `[Deepen engagement]` |
| 5 | No activity for 7 days | Day 7 | `[e.g., "We miss you — here's something new you haven't tried yet"]` | `[Re-engagement]` |

---

## 2.5 — 🤖 AI Agent Touchpoints in Phase 2

| Touchpoint | What the AI Does | When It Triggers |
|------------|-----------------|-----------------|
| `[e.g., AI onboarding wizard]` | `[e.g., Asks 2 personalization questions and configures the product automatically]` | `[Immediately on first login]` |
| `[e.g., AI-generated sample output]` | `[e.g., Creates a demo result using the user's real name/brand before they do anything]` | `[Within first 30 seconds]` |
| `[e.g., AI progress coach]` | `[e.g., Pops up if user is idle for 2 minutes and suggests the next step]` | `[After 2 min of inactivity in first session]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

### 🧠 Prompt / LLM Design Notes for Phase 2

```
Onboarding AI Behavior:

Goal:          [e.g., Get the user to their first AI-generated output in < 3 minutes]
Tone:          [e.g., Encouraging, celebratory, never overwhelming]
Personalization: [e.g., Use their first name in every message]
Progress tracking: [e.g., Show "Step 2 of 4" so they know how close they are to done]

Key LLM instructions for onboarding:
"""
You are [PRODUCT NAME]'s onboarding guide.
Your goal is to help [USER FIRST NAME] complete their setup in under 5 minutes.
Ask ONE question at a time. Keep responses under 50 words.
Celebrate every step they complete with a short encouraging message.
If they seem confused (no action for 60 seconds), offer to do it for them automatically.
"""
```

### 🔄 Feedback Loop in Phase 2

> **What is a feedback loop?** It's how your AI learns from what the user does, to get better over time.

| User Action | Data Captured | How AI Uses It |
|------------|--------------|---------------|
| `[e.g., User edits the AI output]` | `[e.g., Which words they changed]` | `[e.g., AI learns their writing style for next time]` |
| `[e.g., User clicks "Regenerate"]` | `[e.g., Which output they rejected]` | `[e.g., AI avoids that pattern in future]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

---

## 2.6 — Phase 2 Success Metrics

| Metric | Definition | Your Target | Current Baseline |
|--------|-----------|-------------|-----------------|
| **Activation Rate** | % of signups who hit the Aha Moment | `[e.g., > 40% in first session]` | `[TODO]` |
| **Time-to-Value (TTV)** | Time from sign-up to first Aha Moment | `[e.g., < 5 minutes]` | `[TODO]` |
| **Onboarding Completion Rate** | % who finish the full onboarding flow | `[e.g., > 60%]` | `[TODO]` |
| **Day-1 Return Rate** | % of signups who log in again within 24h | `[e.g., > 30%]` | `[TODO]` |
| **Session Duration (First)** | How long the first session lasts | `[e.g., 5–15 min target]` | `[TODO]` |

### Phase 2 Exit Criteria

> You know Phase 2 is working when:
- `[ ]` `[e.g., > 40% of all new signups reach the Aha Moment in their first session]`
- `[ ]` `[e.g., Median Time-to-Value is under 5 minutes]`
- `[ ]` `[e.g., Onboarding email sequence achieves > 25% open rate]`

> 🤖 **AI Prompt — Onboarding Flow:**
> ```
> My product is [PRODUCT NAME]. The Aha Moment is when [DESCRIBE AHA MOMENT].
> Current onboarding steps are: [LIST YOUR STEPS].
> 
> Please redesign this onboarding flow to:
> 1. Reach the Aha Moment in under 3 minutes
> 2. Remove any unnecessary steps
> 3. Add AI-driven personalization to make it feel magical
> 4. Write the first 3 onboarding email subject lines and body copy
> ```

---
---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- PHASE 3: ENGAGEMENT → RETENTION                                       -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 🔁 Phase 3 — Engagement → Retention

> **What this phase is about:**  
> The customer has used your product at least once and found value. Now you need them to **come back regularly** and build a habit around your product.  
> **Think of this like:** Getting someone to go to the gym regularly — first visit is exciting; keeping the habit is the real challenge.

---

## 3.1 — Core Habit Loop Design

> **What is a habit loop?** It's a cycle of: **Trigger → Action → Reward → Repeat**. Great products build this loop naturally.

### Your Product's Habit Loop

```
TRIGGER (What reminds the user to return?):
→ [e.g., Daily email digest showing new AI-generated content ready to review]
→ [e.g., Mobile push notification: "Your weekly report is ready 📊"]
→ [TODO]

ACTION (What do they do when they come back?):
→ [e.g., Review and publish AI-generated descriptions]
→ [e.g., Check their performance metrics]
→ [TODO]

REWARD (What do they get that feels good?):
→ [e.g., Sees "You saved 3 hours this week" stat]
→ [e.g., New badge unlocked: "Power User 🏆"]
→ [TODO]

INVESTMENT (What makes it harder to leave?):
→ [e.g., Their entire product catalog is now in the system]
→ [e.g., AI has learned their specific brand voice over 30+ interactions]
→ [TODO]
```

---

## 3.2 — Feature Engagement Map

> **💡 Tip:** List your top features and note which type of users engage with each one. This helps you understand what drives retention.

| Feature | What it does | Who uses it most | Engagement frequency | Core to retention? |
|---------|-------------|-----------------|---------------------|-------------------|
| `[e.g., AI Writer]` | `[Generates descriptions]` | `[All users]` | `[Daily]` | `[ ] Yes  [ ] No` |
| `[e.g., Analytics Dashboard]` | `[Shows time saved + output count]` | `[Power users]` | `[Weekly]` | `[ ] Yes  [ ] No` |
| `[e.g., Team sharing]` | `[Invite colleagues]` | `[Teams > 2 people]` | `[Monthly]` | `[ ] Yes  [ ] No` |
| `[TODO]` | `[TODO]` | `[TODO]` | `[TODO]` | `[ ] Yes  [ ] No` |

### Sticky Features *(The ones users can't live without)*

1. `[Feature #1 — e.g., AI learns your brand voice — the longer you use it, the better it gets]`
2. `[Feature #2 — TODO]`
3. `[Feature #3 — TODO]`

---

## 3.3 — Re-Engagement Strategy

> For users who have gone quiet (haven't logged in for 7+ days):

| Scenario | Trigger | Action | Message |
|----------|---------|--------|---------|
| **7-day inactive** | No login in 7 days | `[e.g., Send re-engagement email]` | `[e.g., "Your AI is waiting — here's what's new"]` |
| **30-day inactive** | No login in 30 days | `[e.g., Email + in-app banner on next visit]` | `[e.g., "Come back — we've added [NEW FEATURE] since you last visited"]` |
| **Churned (cancelled)** | Account downgrade / deletion | `[e.g., Exit survey email]` | `[e.g., "We're sorry to see you go. What went wrong? (2-question survey)"]` |

---

## 3.4 — 🤖 AI Agent Touchpoints in Phase 3

| Touchpoint | What the AI Does | When It Triggers |
|------------|-----------------|-----------------|
| `[e.g., AI Weekly Digest]` | `[e.g., Auto-generates a personalized weekly summary of the user's activity and suggestions]` | `[Every Monday at 9am user's local time]` |
| `[e.g., AI Smart Suggestions]` | `[e.g., Proactively suggests: "You haven't updated your winter collection yet — want me to generate it?"]` | `[When user has not used a feature in 14 days]` |
| `[e.g., AI Skill Coach]` | `[e.g., Sends a "Power tip of the week" based on which features the user hasn't tried]` | `[Day 14 post-activation]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

### 🔄 Feedback Loop in Phase 3

| User Signal | Data Captured | How AI Uses It |
|------------|--------------|---------------|
| `[e.g., User saves or stars an output]` | `[Which style/format they preferred]` | `[AI generates similar style by default next time]` |
| `[e.g., User uses product on a specific day/time every week]` | `[Behavioral pattern]` | `[AI schedules suggestions to align with their natural rhythm]` |
| `[e.g., User clicks on a specific feature suggestion]` | `[Feature interest signal]` | `[AI shows more of that feature in next session]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

### 🧠 Prompt / LLM Design Notes for Phase 3

```
Retention AI Behavior:

Goal:         [e.g., Make users feel the product is getting smarter over time]
Pattern:      [e.g., Show personalized "you saved X hours this week" messaging]
Tone:         [e.g., Like a knowledgeable colleague who knows your work habits]
Key signal:   [e.g., If user hasn't logged in for 5 days, trigger a re-engagement prompt]

Weekly digest LLM prompt:
"""
You are [PRODUCT NAME]'s AI assistant. Generate a personalized weekly summary
for [USER NAME] based on their usage this week:
- Sessions: [COUNT]
- AI outputs generated: [COUNT]
- Estimated time saved: [CALCULATE BASED ON AVERAGE TIME PER TASK]

Format: 3 bullet points max. Be warm and celebratory. End with ONE actionable 
suggestion for what they should do next week. Keep under 80 words total.
"""
```

---

## 3.5 — Phase 3 Success Metrics

| Metric | Definition | Your Target | Current Baseline |
|--------|-----------|-------------|-----------------|
| **Day-7 Retention** | % of users still active 7 days after signup | `[e.g., > 40%]` | `[TODO]` |
| **Day-30 Retention** | % of users still active 30 days after signup | `[e.g., > 20%]` | `[TODO]` |
| **Day-90 Retention** | % of users still active 90 days after signup | `[e.g., > 15%]` | `[TODO]` |
| **Sessions per User/Week** | Average number of logins per active user | `[e.g., > 3/week]` | `[TODO]` |
| **Feature Adoption Rate** | % of users who use at least 2 core features | `[e.g., > 50%]` | `[TODO]` |
| **Monthly Churn Rate** | % of paying customers who cancel per month | `[e.g., < 5%]` | `[TODO]` |

### Phase 3 Exit Criteria

> You know Phase 3 is working when:
- `[ ]` `[e.g., Day-30 retention is above 20%]`
- `[ ]` `[e.g., Average user logs in at least 3x per week]`
- `[ ]` `[e.g., Users who complete the habit loop show < 3% monthly churn]`

> 🤖 **AI Prompt — Retention Strategy:**
> ```
> My product is [PRODUCT NAME]. It's a [TYPE] for [PERSONA].
> Current Day-7 retention is [X%] and Day-30 is [Y%].
> Core feature that drives retention is: [FEATURE].
> 
> Please suggest:
> 1. 3 habit loop improvements I can build into the product
> 2. A 5-email re-engagement drip sequence for users who haven't logged in 7 days
> 3. 3 AI-powered personalization features that would increase retention
> 4. The single most impactful thing I can build to reduce churn from [Y%] to [TARGET]%
> ```

---
---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- PHASE 4: REVENUE → REFERRAL                                            -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 💰 Phase 4 — Revenue → Referral

> **What this phase is about:**  
> The customer is engaged and getting value. Now it's time to convert them into **paying customers** and turn them into **advocates who bring others**.  
> **Think of this like:** A happy restaurant customer who pays the bill AND tells all their friends to go there.

---

## 4.1 — Pricing Model

> **💡 Tip:** Pick the simplest pricing model that makes sense for your product. Don't over-engineer this.

### Pricing Structure

| Tier | Name | Price | Who is it for | What it includes |
|------|------|-------|--------------|-----------------|
| Free | `[e.g., "Starter"]` | `$0/month` | `[e.g., Solo founders testing the product]` | `[e.g., 10 AI outputs/month, 1 user]` |
| Paid Tier 1 | `[e.g., "Pro"]` | `$[XX]/month` | `[e.g., Active businesses with daily usage]` | `[e.g., Unlimited outputs, 3 users, priority support]` |
| Paid Tier 2 | `[e.g., "Team"]` | `$[XX]/month` | `[e.g., Teams > 5 people]` | `[e.g., Everything in Pro + SSO + custom AI training]` |
| Enterprise | `[e.g., "Enterprise"]` | `Custom` | `[e.g., Companies > 50 users]` | `[e.g., Custom contract, dedicated support, SLA]` |

### Pricing Strategy Notes

```
Free → Paid conversion trigger:  [e.g., User hits their 10-output limit and wants more]
Trial length (if applicable):    [e.g., 14-day free trial of Pro features]
Annual discount offered:         [ ] Yes — [X]% off  [ ] No
Payment processor:               [e.g., Stripe]
Billing model:                   [ ] Monthly  [ ] Annual  [ ] Usage-based  [ ] Per-seat
```

---

## 4.2 — Conversion Moments

> These are the specific moments when a free user is most likely to upgrade. Map them carefully.

| Moment | What triggers it | What you show | Target conversion |
|--------|-----------------|---------------|------------------|
| `[e.g., Hit the free limit]` | `[User generates their 10th output]` | `[Upgrade prompt with "Get unlimited for $X/month"]` | `[e.g., 15% convert here]` |
| `[e.g., Trying a Pro feature]` | `[User clicks on a feature locked behind paywall]` | `[Feature preview + "Upgrade to unlock"]` | `[e.g., 10% convert here]` |
| `[e.g., Sharing with a teammate]` | `[User tries to invite a 2nd team member]` | `["Invite your team — upgrade to Pro"]` | `[e.g., 20% convert here]` |
| `[TODO]` | `[TODO]` | `[TODO]` | `[TODO]` |

---

## 4.3 — Referral & Word-of-Mouth Strategy

> **💡 Tip:** The cheapest and most effective marketing is a happy customer telling a friend. Build this intentionally.

### Referral Program Design

```
Program Name:         [e.g., "Refer a Friend — Both Get 1 Month Free"]
Referrer reward:      [e.g., 1 free month of Pro for every friend who pays]
Referee reward:       [e.g., 30% off first 3 months]
How they share:       [e.g., Unique referral link + pre-written social post template]
Where it lives:       [e.g., Dashboard sidebar + post-payment confirmation screen]
Tracking tool:        [e.g., Rewardful / Viral Loops / Custom built]
```

### Organic Referral Triggers *(moments users naturally want to share)*

| Moment | What happens | Sharing prompt |
|--------|-------------|---------------|
| `[e.g., User hits a milestone]` | `[e.g., "You've saved 10 hours this month! 🎉"]` | `[e.g., "Share this win on LinkedIn →"]` |
| `[e.g., User gets a great AI output]` | `[e.g., Quality output is generated]` | `[e.g., One-click "Share this on Twitter"]` |
| `[e.g., User upgrades]` | `[e.g., Confirmation screen]` | `[e.g., "Tell a friend and you both get a free month →"]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

---

## 4.4 — Customer Success & Support

> ⚠️ **Important:** Happy customers who get quick help become your best salespeople.

### Support Structure

| Support Channel | Availability | Response SLA | Who handles it |
|----------------|-------------|-------------|---------------|
| `[e.g., In-app AI chatbot]` | `[24/7]` | `[Instant]` | `[AI — escalate to human if unresolved]` |
| `[e.g., Email support]` | `[Business hours]` | `[< 24 hours]` | `[Founder / Support rep]` |
| `[e.g., Help center / docs]` | `[24/7 self-serve]` | `[N/A]` | `[Written content]` |
| `[e.g., Community Discord/Slack]` | `[Async]` | `[< 48 hours]` | `[Community manager + power users]` |
| `[TODO]` | `[TODO]` | `[TODO]` | `[TODO]` |

### Top 5 Support Questions You Expect

> Pre-answer these before launching — add them to your help center and train your AI chatbot on them.

1. `[e.g., "How do I connect my Shopify store?"]`
2. `[e.g., "Why is the AI output not matching my brand voice?"]`
3. `[e.g., "How do I cancel my subscription?"]`
4. `[e.g., "Can I export my outputs to CSV?"]`
5. `[TODO]`

---

## 4.5 — 🤖 AI Agent Touchpoints in Phase 4

| Touchpoint | What the AI Does | When It Triggers |
|------------|-----------------|-----------------|
| `[e.g., AI upgrade nudge]` | `[e.g., Sends personalized upgrade message based on how close they are to their limit]` | `[When user has used 80% of their free quota]` |
| `[e.g., AI support bot]` | `[e.g., Resolves top 80% of support tickets automatically]` | `[Any time a support chat is opened]` |
| `[e.g., AI success story generator]` | `[e.g., Auto-creates a shareable "Here's what I achieved" summary for the user]` | `[Monthly, on plan anniversary date]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

### 🔄 Feedback Loop in Phase 4

| User Signal | Data Captured | How AI Uses It |
|------------|--------------|---------------|
| `[e.g., User reads but doesn't click upgrade prompt]` | `[Prompt seen, not acted on]` | `[AI waits 3 more days and tries a different message]` |
| `[e.g., User submits support ticket]` | `[Issue category + resolution]` | `[AI adds to knowledge base, auto-answers next similar ticket]` |
| `[e.g., User refers a friend]` | `[Referral conversion rate]` | `[AI personalizes future referral prompts based on what worked]` |
| `[TODO]` | `[TODO]` | `[TODO]` |

### 🧠 Prompt / LLM Design Notes for Phase 4

```
Revenue AI Behavior:

Goal:           [e.g., Convert 15% of free users to paid within 14 days of activation]
Upgrade tone:   [e.g., Never pushy — lead with value, not pressure]
Key trigger:    [e.g., When user hits 80% of free limit, show upgrade prompt]

Upgrade message LLM prompt:
"""
The user [USER NAME] has used [X] of their [LIMIT] free outputs this month.
Generate a personalized, friendly upgrade message that:
1. Acknowledges what they've accomplished (use their stats)
2. Shows what they're missing on the free plan
3. Offers to upgrade with a clear, low-friction CTA
Keep it under 60 words. Tone: warm, helpful, not salesy.
"""
```

---

## 4.6 — Phase 4 Success Metrics

| Metric | Definition | Your Target | Current Baseline |
|--------|-----------|-------------|-----------------|
| **Free-to-Paid Conversion Rate** | % of free users who upgrade | `[e.g., 10–15% within 30 days]` | `[TODO]` |
| **Monthly Recurring Revenue (MRR)** | Total revenue per month | `[e.g., $5,000 MRR by 500 customers]` | `[TODO]` |
| **Average Revenue Per User (ARPU)** | MRR ÷ paying users | `[e.g., $25–$50/user]` | `[TODO]` |
| **Customer Lifetime Value (LTV)** | Avg. total revenue per customer | `[e.g., $300+ over 12 months]` | `[TODO]` |
| **Referral Rate** | % of customers who refer at least 1 person | `[e.g., > 10%]` | `[TODO]` |
| **Net Promoter Score (NPS)** | Would customers recommend you? (0–10 scale) | `[e.g., > 50]` | `[TODO]` |

### Phase 4 Exit Criteria

> You know Phase 4 is working when:
- `[ ]` `[e.g., > 10% of free users convert to paid within their first 30 days]`
- `[ ]` `[e.g., NPS score is > 50]`
- `[ ]` `[e.g., At least 10% of new signups come from referrals]`

> 🤖 **AI Prompt — Conversion Strategy:**
> ```
> My product is [PRODUCT NAME]. Current free-to-paid conversion rate is [X%].
> Pricing is: Free (limited), Pro at $[XX]/month.
> The most common moment users upgrade is: [DESCRIBE].
> 
> Please:
> 1. Write 3 upgrade prompt messages (A/B/C test variants) for when users hit 80% of free limit
> 2. Design a referral program structure optimized for SaaS virality
> 3. List the top 5 moments in the user journey where I should prompt for upgrade
> 4. Write 1 NPS survey email to send after 30 days of paid use
> ```

---
---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- MILESTONE TRACKER: FIRST 500 CUSTOMERS                                -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 🏆 First 500 Customers Milestone Tracker

> **What this section is for:**  
> Track your progress from 0 → 500 customers. Update this every week or every sprint. This is your product's launch scoreboard.

---

## 5.1 — Customer Growth Milestones

| Milestone | Target Date | Actual Date | Notes |
|-----------|------------|------------|-------|
| **1st customer (real, non-friend)** | `[YYYY-MM-DD]` | `[ ]` | `[Who are they? How did they find you?]` |
| **10 customers** | `[YYYY-MM-DD]` | `[ ]` | `[What channel did they come from?]` |
| **50 customers** | `[YYYY-MM-DD]` | `[ ]` | `[What's working? What's not?]` |
| **100 customers** | `[YYYY-MM-DD]` | `[ ]` | `[First retention data available]` |
| **250 customers** | `[YYYY-MM-DD]` | `[ ]` | `[First cohort hitting 90-day mark]` |
| **500 customers** 🎯 | `[YYYY-MM-DD]` | `[ ]` | `[Retrospective complete — see section 5.4]` |

---

## 5.2 — Weekly Scoreboard

> Update this every Monday. Keep old rows — they show your trajectory.

| Week | New Signups | New Paid | Total Users | Total Paying | MRR | Top Acquisition Channel | Key Learning |
|------|------------|---------|------------|-------------|-----|------------------------|-------------|
| Week 1 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `$[ ]` | `[ ]` | `[ ]` |
| Week 2 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `$[ ]` | `[ ]` | `[ ]` |
| Week 3 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `$[ ]` | `[ ]` | `[ ]` |
| Week 4 | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `$[ ]` | `[ ]` | `[ ]` |

---

## 5.3 — Cohort Retention Dashboard

> A **cohort** is a group of users who signed up in the same week. Tracking them separately shows if your product is improving.

| Cohort (Signup Week) | Users | Wk 1 Active | Wk 2 Active | Wk 4 Active | Wk 8 Active | Converted to Paid |
|----------------------|-------|------------|------------|------------|------------|------------------|
| `[e.g., Oct Week 1]` | `[ ]` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` |
| `[e.g., Oct Week 2]` | `[ ]` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` | `[ ]%` |

---

## 5.4 — 500-Customer Retrospective

> Fill this section when you hit 500 customers. It's your treasure map for the next growth phase.

### What worked well?

- `[Acquisition: Which channels actually worked?]`
- `[Onboarding: What made users activate fast?]`
- `[Retention: What kept users coming back?]`
- `[Revenue: What made users pay?]`

### What didn't work?

- `[What did you waste time or money on?]`
- `[Which assumptions were wrong?]`
- `[What did you build that nobody used?]`

### Key Stats at 500 Customers

| Metric | Number |
|--------|--------|
| Time to reach 500 customers | `[ ] weeks / months` |
| Paying customers (% of 500) | `[ ]%` |
| Monthly Recurring Revenue | `$[ ]` |
| Average Time-to-Value | `[ ] minutes` |
| Net Promoter Score | `[ ]` |
| #1 acquisition channel | `[ ]` |
| #1 reason users stayed | `[ ]` |
| #1 reason users churned | `[ ]` |

---
---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- APPENDIX: MASTER AI PROMPT LIBRARY                                     -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 🤖 Appendix — Master AI Prompt Library

> **How to use this section:**  
> These prompts help you fill any section of this document faster. Copy the prompt, fill in the `[BRACKETS]`, and paste it into Claude or ChatGPT.

---

## A. Getting Started Prompts

### A1 — Generate Your Entire Customer Journey Outline
```
I am building a [SaaS / Mobile App] called [PRODUCT NAME].
It's for [TARGET PERSONA — describe them in 2 sentences].
The core problem it solves: [DESCRIBE PROBLEM].
My solution: [DESCRIBE SOLUTION].

Please generate a complete Customer Journey outline for this product covering:
1. Awareness and Acquisition (how they find us)
2. Onboarding and Activation (first value moment)
3. Engagement and Retention (habit building)
4. Revenue and Referral (conversion and growth)

For each phase, include:
- 3 key customer actions
- 2 AI agent touchpoints
- 3 success metrics with benchmarks
- 1 biggest risk and how to mitigate it
```

### A2 — Define Your Target Persona
```
I am building [PRODUCT NAME] that helps [WHO] to [DO WHAT].
Please create a detailed primary user persona with:
- Fictional name, age, job title
- Daily frustrations (at least 3)
- Goals and dreams (at least 3)
- Where they find new products
- What they've tried before and why it failed
- Their budget for software tools
- What would make them switch to a new tool instantly
Format as a table and a 3-sentence narrative summary.
```

---

## B. Phase-Specific Prompts

### B1 — Awareness / Landing Page
```
Help me write a landing page for [PRODUCT NAME].
Target customer: [PERSONA]
Core benefit: [MAIN VALUE PROPOSITION]
Please write:
- 1 headline (under 8 words)
- 1 sub-headline (under 15 words)
- 3 benefit bullets (not features — benefits)
- 1 CTA button text
- 2 social proof snippets (made-up examples are fine for now)
```

### B2 — Aha Moment Definition
```
My product is [PRODUCT NAME]. It does [WHAT IT DOES].
Help me define the exact "Aha Moment" — the first time a new user 
feels the product is truly valuable.
Please suggest:
1. The specific action that triggers the Aha Moment
2. How to get users to that moment in under 3 minutes
3. The emotion the user should feel at that moment
4. How to measure whether users have reached the Aha Moment
```

### B3 — Onboarding Email Sequence
```
Write a 5-email onboarding sequence for [PRODUCT NAME].
Product: [DESCRIBE IN 1 SENTENCE]
User persona: [DESCRIBE BRIEFLY]
Aha Moment: [DESCRIBE]

Email 1: Welcome (send immediately)
Email 2: Re-engage if they haven't logged in (Day 2)
Email 3: Help email if they haven't hit Aha Moment (Day 3)
Email 4: Celebrate if they have hit Aha Moment (Day 5)
Email 5: Feature discovery (Day 10)

For each email include: Subject line, 3-sentence body, and 1 CTA button text.
Keep each email under 100 words. Tone: warm, human, helpful.
```

### B4 — Retention & Habit Loop
```
My product is [PRODUCT NAME]. Core feature: [FEATURE].
Current Day-30 retention is [X%]. Target is [Y%].

Please design a habit loop for this product using the Hook Model:
- Trigger (internal or external)
- Action (what the user does)
- Variable Reward (what feels good)
- Investment (what makes it sticky)

Also suggest 3 AI-powered personalization features that would 
strengthen this habit loop and increase Day-30 retention.
```

### B5 — Revenue / Upgrade Prompts (A/B/C Test)
```
My product [PRODUCT NAME] has a free plan with [LIMIT].
Paid plan is $[PRICE]/month with [BENEFITS].

Write 3 upgrade prompt message variants (A/B/C test) for when 
a free user hits 80% of their limit.
Each variant should:
- Be under 60 words
- Lead with value (not fear)
- Include a clear CTA
- Have a different emotional angle:
  A: FOMO (what they're missing)
  B: Achievement (celebrate their success, invite more)
  C: Social proof (others like them upgraded)
```

### B6 — Referral Program Design
```
My product is [PRODUCT NAME] at $[PRICE]/month.
Current customer count: [NUMBER]. NPS: [SCORE].

Design a referral program for early-stage SaaS:
1. Referral incentive for the referrer
2. Incentive for the new user (referee)
3. The exact sharing message (pre-written tweet/post)
4. Where to surface the referral CTA in the product (3 locations)
5. How to track referrals without expensive tooling
```

---

## C. AI Design Prompts

### C1 — AI Agent Prompt System Instructions
```
I am building an AI assistant for [PRODUCT NAME].
This assistant appears at [WHERE — e.g., onboarding wizard / support chat].
Its job is to: [WHAT IT MUST DO]
It must not: [WHAT IT MUST NEVER SAY OR DO]
Tone: [DESCRIBE — e.g., warm, concise, encouraging]

Please write the full system prompt instruction for this AI agent.
Include:
- Role definition
- Primary objective
- Rules and constraints
- Fallback behavior when it can't help
- Sample response to the most common question: "[COMMON QUESTION]"
```

### C2 — Feedback Loop Design
```
My AI-powered product captures this user data: [LIST WHAT YOU TRACK].
The AI currently does: [WHAT IT DOES TODAY].

Please design a feedback loop where:
1. User actions improve the AI's output quality over time
2. The improvement is visible to the user (so they feel the AI getting smarter)
3. No manual labeling is required from the user
4. The loop can be implemented by a solo developer

Describe the technical architecture in simple, non-jargon language.
```

---
---

<!-- ════════════════════════════════════════════════════════════════════ -->
<!-- DOCUMENT CONTROL                                                       -->
<!-- ════════════════════════════════════════════════════════════════════ -->

# 📋 Document Control

| Field | Value |
|-------|-------|
| **Document Title** | Customer Journey — AI-Driven Development Life Cycle |
| **Version** | `[e.g., v1.0]` |
| **Status** | `[ ] Draft  [ ] In Review  [ ] Approved  [ ] Archived` |
| **Owner** | `[Your Name]` |
| **Created** | `[YYYY-MM-DD]` |
| **Last Updated** | `[YYYY-MM-DD]` |
| **Next Review Date** | `[YYYY-MM-DD — suggest: every 2 weeks during early growth]` |
| **Reviewed By** | `[Name / Role]` |
| **Change Log** | `v1.0 — Initial draft created` |

---

> 🎉 **You've filled the template! Before you share it:**
> 1. Search for `[TODO]` — replace or note a date when you'll fill it
> 2. Search for `[YOUR` — make sure no placeholder text remains
> 3. Delete any `[EXAMPLE: ...]` lines you haven't replaced
> 4. Have one other person read it and ask them: "What's confusing?" — fix those parts
> 5. Set a calendar reminder to update the **Weekly Scoreboard (Section 5.2)** every Monday

---
*Template built for AI-Driven Development Life Cycle · Version 1.0 · October 2026*
