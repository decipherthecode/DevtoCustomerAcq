# How to fill this document

> **Read this first. It takes 3 minutes.**
> This file helps you build a product that **everyone** can use, including people who are blind, deaf, have shaky hands, find reading hard, or are using a phone in bright sunlight. You will fill it in from the first idea until your first **500 customers**.

## The 8 steps

1. **Copy this file** into your project folder: `UX, UI and Design System/Accessibility_Design_Guidelines.md`. Never edit the original template. Rename your copy `Accessibility_Design_Guidelines_[ProjectName].md`.
2. **Start at Section 0** and go in order. Do not skip ahead. Each section builds on the one before.
3. **Find every `[FILL: ...]`** and replace it with your answer. The words after FILL tell you what to write.
4. **Look at the `Example:` line** under a field if you are stuck. Copy its style, not its words.
5. **Tick the boxes.** Change `- [ ]` to `- [x]` only when the thing is truly done and you can prove it (a screenshot, a test result, a link).
6. **If something does not apply**, do not delete it. Write `N/A because [reason]`. A blank is never allowed; a reason is.
7. **If you cannot meet a rule**, write it in the **Exceptions Log (Section 12)**. Never hide it.
8. **Do not move to the next phase until the Gate at the end of the current phase is fully ticked.** Gates stop problems from piling up.

## Legend (what the symbols mean)

| Symbol | Meaning |
|---|---|
| `[FILL: ...]` | You must write an answer here. |
| `Example:` | A sample answer. Do not copy it blindly. |
| `- [ ]` / `- [x]` | Not done / done (with proof). |
| 🧑 **Human** | A person does this. |
| 🤖 **AI Agent Instructions** | Rules an AI coding or design assistant must follow. Paste these into your agent's prompt. |
| ⛔ **MUST** | Required. Cannot launch without it. |
| ✅ **SHOULD** | Strongly recommended. Skip only with a written reason. |
| 💡 **TIP** | Helpful, optional. |
| 🚦 **GATE** | A checkpoint. Everything above it must be done before you continue. |

## Five golden rules (so nobody has to guess)

1. **Plain words.** If a 10-year-old cannot understand your sentence, rewrite it.
2. **One answer per box.** Do not write "maybe", "TBD" or "later". Write a real answer, or `N/A because ...`.
3. **Proof beats promises.** Every ticked box needs a link, screenshot or test result in the **Proof** column or line.
4. **Names, not "the team".** Every task has one named owner and one due date.
5. **Accessibility is not a final polish step.** It is built in from day 1. Fixing it at the end costs many times more.

## Who does what (roles)

You may be one person wearing all hats. Even then, write your name in each role.

| Role | Plain-words job | Name |
|---|---|---|
| **Product Owner (PO)** | Decides what gets built and what is "good enough" | [FILL: name] |
| **Designer** | Makes how it looks and feels | [FILL: name] |
| **Developer** | Builds it | [FILL: name] |
| **QA (Tester)** | Tries to break it, checks every rule | [FILL: name] |
| **Project Manager (PM)** | Keeps dates and tasks on track | [FILL: name] |
| **AI Agent(s)** | Software helpers (for example Claude, Copilot, Cursor) | [FILL: tool names] |
| **Accessibility Champion** | The person who says "stop, this is not accessible yet" | [FILL: name] |

---

# Table of Contents

- Section 0: Document Control
- Section 1: Project Snapshot
- Section 2: Accessibility Basics (read once)
- Section 3: Standards and Laws
- Section 4: Know Your Users
- Phase 1: Discovery and Planning
- Phase 2: Design and Design System
- Phase 3: Development (with AI agents)
- Phase 4: Testing and QA
- Phase 5: Launch
- Phase 6: Post-Launch, Day 1 to Customer 500
- Section 12: Exceptions Log
- Section 13: Accessibility Statement Template
- Section 14: AI Agent Prompt Library
- Section 15: Glossary
- Section 16: Resources
- Appendix A: Filled Example
- Appendix B: Version History

---

# Section 0: Document Control

| Field | Your answer |
|---|---|
| Project name | [FILL: e.g., PetPal] |
| Template version used | 1.0 |
| Document owner | [FILL: name] |
| Created on | [FILL: YYYY-MM-DD] |
| Last reviewed on | [FILL: YYYY-MM-DD] |
| Next review due | [FILL: YYYY-MM-DD, at least every 90 days] |
| Where this file lives | [FILL: folder path or link] |
| Status | ☐ Draft ☐ In review ☐ Approved |

---

# Section 1: Project Snapshot

Answer in one or two simple sentences each.

| Question | Your answer | Example |
|---|---|---|
| What is the product? | [FILL] | A mobile app that helps people book dog walkers. |
| Who will use it? | [FILL] | Dog owners aged 20 to 70. |
| What is the one big problem it solves? | [FILL] | Finding a trusted walker quickly. |
| Platforms (tick all) | ☐ Web ☐ iOS ☐ Android ☐ Windows ☐ macOS ☐ Linux | ☑ Web ☑ iOS ☑ Android |
| Languages supported at launch | [FILL] | English, Spanish |
| Countries where you will sell | [FILL] | USA, Canada, Germany |
| Planned launch date | [FILL: YYYY-MM-DD] | 2027-03-01 |
| Target: first 500 customers by | [FILL: YYYY-MM-DD] | 2027-09-01 |
| Does it handle payments, health, kids, or government data? | ☐ Yes ☐ No (if yes, describe) | Yes, payments. |
| Is it sold to schools, governments, or large companies? | ☐ Yes ☐ No | No |

**Accessibility target for this project (default is already chosen):**

- [x] **WCAG 2.2 Level AA** is the minimum for every platform.
- Do you want to go higher on some items? [FILL: Yes/No, which ones]
- Rule of thumb: pick **AA**. It is what most laws and customers expect. AAA everywhere is usually not possible, so only add AAA items that are cheap and helpful (for example, plain language).

---

# Section 2: Accessibility Basics (read once)

## What is accessibility (A11y)?

Accessibility means people with different abilities can use your product. "A11y" is short for "accessibility" (A, then 11 letters, then Y).

## The four principles (POUR)

| Letter | Principle | Kid-friendly meaning |
|---|---|---|
| **P** | Perceivable | People can **see, hear or feel** the content in some way. |
| **O** | Operable | People can **use** it with a mouse, keyboard, touch, voice or switch. |
| **U** | Understandable | It makes **sense** and does not surprise or trap you. |
| **R** | Robust | It works with **many tools**, such as screen readers, now and in the future. |

## Conformance levels

| Level | Meaning | Your plan |
|---|---|---|
| **A** | Bare minimum. Without it, some people are completely blocked. | ⛔ MUST |
| **AA** | The standard goal. | ⛔ MUST (default target) |
| **AAA** | Highest. Not always possible for every page. | ✅ SHOULD where cheap |

## Why it matters (so you can explain it to others)

- About 1 in 6 people worldwide lives with a significant disability (WHO). Many more have temporary or situational limits (a broken arm, a noisy train, glare on a screen).
- It is the law in many countries (see Section 3).
- It improves usability, SEO and conversion for **everyone**.

## Needs you must design for

| Category | Examples | What helps |
|---|---|---|
| **Vision** | Blind, low vision, color blindness | Screen reader support, text alternatives, strong contrast, zoom, no color-only meaning |
| **Hearing** | Deaf, hard of hearing | Captions, transcripts, visual alerts |
| **Motor / physical** | Tremor, one hand, paralysis, no mouse | Keyboard access, large targets, no timing traps, voice control, switch control |
| **Cognitive / learning** | Dyslexia, ADHD, memory issues, autism | Plain language, consistent layout, clear errors, no time pressure, calm motion |
| **Speech** | Cannot speak or be understood by voice systems | Never require voice only |
| **Seizures / vestibular** | Photosensitive epilepsy, motion sickness | No flashing more than 3 times per second, respect "reduce motion" |
| **Temporary / situational** | Broken arm, bright sun, loud room, new parent holding a baby | Same helpful features above |

---

# Section 3: Standards and Laws

> ⚠️ **Not legal advice.** Laws and dates change. For each row, confirm the current rule with a lawyer or the official source before you rely on it. Write the date you checked.

## 3.1 Which rules apply to me?

Tick every row that matches your project.

| ☐ | Rule | Where | Who it applies to | Technical standard it points to | Plain-words summary | Last checked (FILL) |
|---|---|---|---|---|---|---|
| ☐ | **ADA** (Americans with Disabilities Act), Title III | USA | Businesses open to the public, including most websites and apps (courts apply it widely) | No official standard in law; courts and settlements usually use WCAG 2.1/2.2 AA | If you sell to Americans, expect lawsuits if you are not accessible. | [FILL] |
| ☐ | **ADA Title II web rule** | USA | State and local governments and their vendors | WCAG 2.1 AA (check current compliance dates) | Government sites and apps must meet WCAG 2.1 AA. | [FILL] |
| ☐ | **Section 508** | USA | US federal agencies and vendors selling to them | WCAG 2.0 A/AA (via the 2017 refresh) | If you sell to US federal government, you must provide an ACR (see 3.3). | [FILL] |
| ☐ | **European Accessibility Act (EAA)** | EU | Many consumer products and services (e-commerce, banking, e-books, transport, telecom). In force since 28 June 2025. Micro-enterprises providing services may be exempt. | EN 301 549, which references WCAG 2.1 AA (check for an update that adds WCAG 2.2) | If you sell in the EU, your product must be accessible. | [FILL] |
| ☐ | **EU Web Accessibility Directive** | EU | Public sector bodies | EN 301 549 / WCAG 2.1 AA | Public sector websites and apps. | [FILL] |
| ☐ | **UK Equality Act 2010** and **PSBAR 2018** | UK | Service providers (Equality Act); public sector (PSBAR) | WCAG 2.2 AA is the current monitored level for public sector | Treat people fairly; public sector needs a statement. | [FILL] |
| ☐ | **AODA** | Ontario, Canada | Organizations with 50+ employees (public and large private) | WCAG 2.0 AA | Websites must meet WCAG 2.0 AA. | [FILL] |
| ☐ | **Accessible Canada Act** | Canada (federal) | Federally regulated organizations | Regulations aligned with WCAG | Plan, report and fix barriers. | [FILL] |
| ☐ | **Other** (Australia DDA, India RPwD, Japan JIS X 8341-3, Brazil LBI, etc.) | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

## 3.2 Mapping: WCAG 2.2 AA to each rule

Use this to see whether meeting WCAG 2.2 AA covers you.

| Law or standard | Based on WCAG version | Does WCAG 2.2 AA cover it? | What to add |
|---|---|---|---|
| ADA (private) | Courts use 2.0, 2.1 or 2.2 AA | ✅ Yes (2.2 includes everything in 2.0 and 2.1, except 4.1.1, which was retired) | Nothing |
| ADA Title II rule | 2.1 AA | ✅ Yes | Nothing |
| Section 508 | 2.0 AA | ✅ Yes | ACR document (3.3) |
| EAA / EN 301 549 | 2.1 AA plus extra ICT clauses | ✅ for the WCAG part | Check EN 301 549 extra clauses: documentation, support services, hardware and two-way voice/video, real-time text |
| UK PSBAR | 2.2 AA | ✅ Yes | Published accessibility statement |
| AODA | 2.0 AA | ✅ Yes | Compliance report where required |

**Decision for this project:**
- Rules that apply: [FILL]
- Strictest technical standard among them: [FILL]
- Our target: **WCAG 2.2 AA** (covers all of the above) ☐ Confirmed by [FILL: name, date]

## 3.3 Required papers (tick what you need)

- [ ] **Accessibility Statement** (public page, template in Section 13)
- [ ] **ACR / VPAT** (Accessibility Conformance Report, the standard form buyers in government and big companies ask for)
- [ ] **Feedback and support channel** (email or form for accessibility problems)
- [ ] **Accessibility policy** (a short internal rule saying "we follow WCAG 2.2 AA")

## 3.4 What WCAG 2.2 AA changed from 2.1 (new items)

| Number | Name | Level | Plain-words rule |
|---|---|---|---|
| 2.4.11 | Focus Not Obscured (Minimum) | AA | The keyboard focus is never fully hidden behind sticky headers, banners or chat widgets. |
| 2.5.7 | Dragging Movements | AA | Anything done by dragging also works with a single tap or click. |
| 2.5.8 | Target Size (Minimum) | AA | Click and tap targets are at least 24 by 24 CSS pixels (or have enough spacing). |
| 3.2.6 | Consistent Help | A | Help links (contact, chat, FAQ) appear in the same place on every page. |
| 3.3.7 | Redundant Entry | A | Do not ask people to type the same info twice in one process. |
| 3.3.8 | Accessible Authentication (Minimum) | AA | Logging in does not require solving a puzzle or memorizing; allow paste and password managers. |

---

# Section 4: Know Your Users

## 4.1 Which needs matter most for your product?

| Need category | Relevant? | Why / how it shows up in our product |
|---|---|---|
| Vision | ☐ Yes ☐ No | [FILL] |
| Hearing | ☐ Yes ☐ No | [FILL] |
| Motor / physical | ☐ Yes ☐ No | [FILL] |
| Cognitive / learning | ☐ Yes ☐ No | [FILL] |
| Speech | ☐ Yes ☐ No | [FILL] |
| Seizures / vestibular | ☐ Yes ☐ No | [FILL] |
| Temporary / situational | ☐ Yes ☐ No | [FILL] |

💡 **TIP:** When unsure, answer **Yes**. Your users are more varied than you think.

## 4.2 Three user stories (write real ones)

Format: *"As a [type of person], I want to [do something] so that [reason]."*

1. Example: *As a blind pet owner using VoiceOver, I want to book a walker so that my dog gets exercise.*
   - Yours: [FILL]
2. Example: *As a person with a hand tremor, I want big buttons so that I do not tap the wrong thing.*
   - Yours: [FILL]
3. Example: *As a person with dyslexia, I want short, clear text so that I understand prices.*
   - Yours: [FILL]

## 4.3 Assistive tools your users likely use

| Tool | Platform | We will test with it? |
|---|---|---|
| NVDA (free screen reader) | Windows | ☐ Yes ☐ No |
| JAWS | Windows | ☐ Yes ☐ No |
| VoiceOver | macOS / iOS | ☐ Yes ☐ No |
| TalkBack | Android | ☐ Yes ☐ No |
| Narrator | Windows | ☐ Yes ☐ No |
| Orca | Linux | ☐ Yes ☐ No |
| Voice Control / Voice Access | iOS, macOS / Android | ☐ Yes ☐ No |
| Switch Control / Switch Access | iOS / Android | ☐ Yes ☐ No |
| Screen magnifier / browser zoom | All | ☐ Yes ☐ No |
| Keyboard only | All | ☐ Yes (always) |

---

# PHASE 1: Discovery and Planning

**Goal:** Decide the accessibility rules **before** anyone designs or codes.
**Timing:** [FILL: start date] to [FILL: end date]
**Owner:** [FILL: name]

## 1.1 Accessibility goals

| Item | Your answer | Example |
|---|---|---|
| Our standard | WCAG 2.2 AA | |
| Which key user journeys must work 100% with keyboard and screen reader? | [FILL] | Sign up, search, book, pay, cancel |
| Our accessibility budget (time or money) | [FILL] | 15% of each sprint |
| Who says "stop, not accessible yet"? | [FILL: Champion name] | |

## 1.2 Choose the 5 to 10 most important journeys

List the journeys users must complete. Test these first and most often.

| # | Journey | Platforms | Owner |
|---|---|---|---|
| 1 | [FILL: e.g., Create account] | | |
| 2 | [FILL] | | |
| 3 | [FILL] | | |
| 4 | [FILL] | | |
| 5 | [FILL] | | |

## 1.3 Risk list (what could go wrong?)

| Risk | How likely (Low/Med/High) | How bad (Low/Med/High) | What we will do |
|---|---|---|---|
| Third-party tools (chat widget, payments, maps) are not accessible | [FILL] | [FILL] | [FILL: ask vendor for their ACR; test before choosing] |
| Videos without captions | [FILL] | [FILL] | [FILL] |
| AI-generated code ignores accessibility | [FILL] | [FILL] | Use the AI rules in this file |
| [FILL: your own risk] | | | |

## 1.4 Buying tools and vendors

⛔ **MUST:** Before buying or choosing any third-party tool, library or component set, ask for its accessibility report (ACR/VPAT) and test it yourself.

| Tool or vendor | What it does | Has ACR? | Our test result | Decision |
|---|---|---|---|---|
| [FILL] | [FILL] | ☐ Yes ☐ No | [FILL] | ☐ Use ☐ Replace |

## 1.5 Requirements writing rule

Every feature request ("user story") must include at least one accessibility acceptance line. Examples:

- "Can be completed using only a keyboard."
- "Screen reader announces the result."
- "Works at 200% zoom with no lost content."

Write your project's standard acceptance lines here: [FILL]

## 🤖 AI Agent Instructions: Phase 1

- Read this whole document before writing any plan, ticket or code.
- For every user story you write, add at least two accessibility acceptance criteria that can be tested as pass/fail.
- Never mark an item "done" without proof in the Proof column.
- If a rule is unclear, ask the human. Do not guess.

## 🚦 GATE 1: Discovery complete

- [ ] Section 1, 3 and 4 are fully filled (no blank `[FILL]` left). Proof: [FILL]
- [ ] Standard (WCAG 2.2 AA) confirmed by the Product Owner. Proof: [FILL]
- [ ] Applicable laws listed with "last checked" dates. Proof: [FILL]
- [ ] Journeys and roles named. Proof: [FILL]
- [ ] Vendor and third-party tools checked. Proof: [FILL]
- Approved by: [FILL: name] on [FILL: date]

---

# PHASE 2: Design and Design System

**Goal:** Make every screen, color, font and component accessible **on paper** before code exists.
**Timing:** [FILL] **Owner:** [FILL: Designer]

## 2.1 Color and contrast

⛔ **MUST** meet these ratios (use a free contrast checker such as the Colour Contrast Analyser or WebAIM's checker):

| What | Minimum contrast |
|---|---|
| Normal text (under 18pt, or under 14pt bold) | **4.5 : 1** |
| Large text (18pt or bigger, or 14pt bold or bigger) | **3 : 1** |
| Icons, input borders, focus rings, chart lines (parts needed to understand) | **3 : 1** against neighbors |
| Disabled buttons and purely decorative items | No requirement, but make them still readable |

**Never use color alone to carry meaning.** Add an icon, text or pattern.
Example: an error field has a red border **and** a warning icon **and** the words "Email is not valid".

**Color palette table (fill for your brand):**

| Name | Hex | Used for | On what background | Ratio | Passes? |
|---|---|---|---|---|---|
| [FILL: Primary text] | [FILL: #1A1A1A] | Body text | [FILL: #FFFFFF] | [FILL] | ☐ |
| [FILL: Primary button] | [FILL] | | | | ☐ |
| [FILL: Error] | [FILL] | | | | ☐ |
| [FILL: Link] | [FILL] | | | | ☐ |

- [ ] ⛔ **Dark mode** palette also checked (same ratios).
- [ ] ✅ **High contrast / forced colors** mode will not break the design.

## 2.2 Text and typography

| Rule | Level | Our value (FILL) | Example |
|---|---|---|---|
| Body font size | ✅ SHOULD be at least 16px (web) / 17pt (iOS body) / 16sp (Android) | [FILL] | 16px |
| Text resizes to 200% without losing content or function | ⛔ MUST | ☐ | |
| Supports platform text scaling (iOS Dynamic Type, Android font scale) | ⛔ MUST on mobile | ☐ | |
| Line height | ✅ SHOULD be at least 1.5 | [FILL] | 1.5 |
| Paragraph spacing | ✅ SHOULD be at least 2 × font size | [FILL] | |
| No justified full-width walls of text | ✅ SHOULD | ☐ | |
| Line length | ✅ SHOULD be under about 80 characters | [FILL] | |
| Users can override spacing (line, letter, word) without breakage | ⛔ MUST | ☐ | |
| Avoid text inside images (except logos) | ⛔ MUST | ☐ | |
| Plain language, short sentences | ✅ SHOULD | ☐ | |

Font family choices: [FILL]. 💡 Pick fonts with clear letter shapes (distinguish `I`, `l`, `1`, `O`, `0`).

## 2.3 Layout and responsive design

- [ ] ⛔ **Reflow:** content works at **320 CSS px width** (equals 400% zoom on a 1280px screen) with no sideways scrolling, except for things like data tables, maps and code.
- [ ] ⛔ **Orientation:** works in portrait and landscape unless truly impossible.
- [ ] ⛔ **Consistent navigation:** menus and help links are in the same place on every screen (3.2.3, 3.2.4, 3.2.6).
- [ ] ✅ Page titles and headings clearly describe the screen. One main heading (`h1`) per page.
- [ ] ✅ Logical reading order (top-left to bottom-right in left-to-right languages).
- [ ] ✅ Plenty of white space. Do not crowd.

## 2.4 Touch and click targets

| Platform | Minimum (MUST) | Recommended (SHOULD) |
|---|---|---|
| Web (WCAG 2.2 AA, 2.5.8) | 24 × 24 CSS px, or enough spacing so a 24px circle does not overlap another target | 44 × 44 px |
| iOS (Apple HIG) | 44 × 44 pt | 44 × 44 pt or more |
| Android (Material) | 48 × 48 dp | 48 × 48 dp with 8dp spacing |
| Desktop | 24 × 24 px | 32 × 32 px or more |

- [ ] ⛔ Anything done by **dragging** (sliders, reorder lists, maps) also has a click/tap alternative (2.5.7).
- [ ] ⛔ No action fires on pointer **down** only. Allow cancel by moving away before release (2.5.2).
- [ ] ✅ Gesture shortcuts (pinch, multi-finger swipe) always have a simple alternative.

## 2.5 Focus, keyboard and navigation

- [ ] ⛔ Every clickable thing can be reached and used with the **keyboard** (Tab, Shift+Tab, Enter, Space, Arrow keys, Esc).
- [ ] ⛔ A **visible focus indicator** on every focusable item. Aim for a 2px outline with 3:1 contrast against both the item and its background (the stronger AAA rule 2.4.13 is a good model).
- [ ] ⛔ Focus is **never completely hidden** by sticky bars, cookie banners or popups (2.4.11).
- [ ] ⛔ No **keyboard trap** (users can always leave a widget with the keyboard).
- [ ] ⛔ Focus order is logical and matches visual order.
- [ ] ✅ A "Skip to main content" link on web pages.
- [ ] ⛔ Single-character shortcuts can be turned off or remapped (2.1.4).

Focus style we will use: [FILL: e.g., 3px solid #005FCC outline, 2px offset]

## 2.6 Images, icons, video and audio

| Content | Rule | Level |
|---|---|---|
| Informative image | Write short, useful alt text. Example: "Dog walker holding two leashes". | ⛔ |
| Decorative image | Empty alt (`alt=""`) so screen readers skip it. | ⛔ |
| Icon-only button | Has a text name, for example "Search". | ⛔ |
| Chart or graph | Text summary or data table next to it. | ⛔ |
| Pre-recorded video | Captions + audio description (or text alternative) | ⛔ |
| Live video | Live captions | ⛔ (AA) |
| Audio only | Transcript | ⛔ |
| Auto-playing media | No autoplay over 3 seconds, or provide an easy pause/stop control. | ⛔ |
| Flashing | Nothing flashes more than 3 times per second. | ⛔ |
| Animation and motion | Respect "reduce motion" settings; no required motion to understand. | ⛔ |
| Captcha / puzzle | Offer an alternative and never rely on a single sense (2.2 AA: 3.3.8). | ⛔ |

Alt text style guide for our project: [FILL: e.g., max 125 characters, do not start with "image of"]

## 2.7 Forms and errors

- [ ] ⛔ Every input has a **visible label** (not just placeholder text).
- [ ] ⛔ Required fields are marked with text, not color alone. Example: "(required)".
- [ ] ⛔ Errors say **what is wrong and how to fix it**, in text, next to the field. Example: "Enter an email like name@example.com".
- [ ] ⛔ Errors are announced to screen readers and keyboard focus moves to the first error.
- [ ] ⛔ Help text is linked to the field.
- [ ] ⛔ Do not ask to re-enter info already given in the same flow (3.3.7).
- [ ] ⛔ Allow **paste** and password managers in login fields; no memory tests or puzzles (3.3.8).
- [ ] ⛔ Important actions (payments, deleting, legal) can be **reviewed, corrected or undone** (3.3.4).
- [ ] ✅ Use correct input types and autocomplete values (`email`, `tel`, `cc-number`, etc.) (1.3.5).
- [ ] ⛔ No time limit, or user can turn off, extend or adjust it (2.2.1).

## 2.8 Mobile and desktop app specifics

| Topic | iOS | Android | Desktop (Win/Mac/Linux) |
|---|---|---|---|
| Screen reader | VoiceOver labels, traits, hints | TalkBack `contentDescription`, roles | UI Automation (Windows), NSAccessibility (macOS), AT-SPI (Linux) |
| Text size | Dynamic Type | Font scale and `sp` units | OS text scaling |
| Reduce motion | `UIAccessibility.isReduceMotionEnabled` | Animator duration scale | OS reduce-motion setting |
| Contrast / dark | Increase Contrast, Dark Mode | High contrast text, Dark theme | High contrast / forced colors |
| Alternative input | Switch Control, Voice Control | Switch Access, Voice Access | Keyboard, voice control, switches |
| Touch targets | 44 pt | 48 dp | 24 px (min) |

- Platform notes for this project: [FILL]
- [ ] ⛔ Use **native, standard components** whenever possible (they are accessible for free). Custom components need extra proof.
- [ ] ⛔ Do not lock the screen orientation unless essential.
- [ ] ⛔ Do not block screen readers, zoom or copy.

## 2.9 Accessible components checklist (design system)

For each reusable component, fill one row **before** developers build it. Add rows as needed.

| Component | Keyboard behavior (which keys) | Screen reader name / role / state | Contrast OK? | Min size OK? | Proof (Figma link) |
|---|---|---|---|---|---|
| Button | Enter and Space activate | "Save, button" | ☐ | ☐ | [FILL] |
| Link | Enter activates | "Pricing, link" | ☐ | ☐ | [FILL] |
| Text input | Type, Tab away | "Email, edit text, required" | ☐ | ☐ | [FILL] |
| Checkbox / radio | Space toggles / arrows move | "Newsletter, checkbox, checked" | ☐ | ☐ | [FILL] |
| Dropdown / select | Arrow keys, Enter, Esc | "Country, collapsed, combo box" | ☐ | ☐ | [FILL] |
| Modal / dialog | Focus moves in, trapped inside, returns on close, Esc closes | "Confirm delete, dialog" | ☐ | ☐ | [FILL] |
| Tabs | Arrow keys switch tabs | "Details, tab 1 of 3, selected" | ☐ | ☐ | [FILL] |
| Menu / navigation | Tab / arrows / Esc | "Main, navigation" | ☐ | ☐ | [FILL] |
| Toast / alert | Announced without stealing focus | "Saved" (status) | ☐ | ☐ | [FILL] |
| Table | Header cells marked | "Row 2 of 5, Price column" | ☐ | ☐ | [FILL] |
| Date picker | Type or pick; keyboard accessible | "Choose date" | ☐ | ☐ | [FILL] |
| Carousel | Pause button, keyboard arrows | "Slide 2 of 5" | ☐ | ☐ | [FILL] |
| [FILL: own] | | | | | |

## 🤖 AI Agent Instructions: Phase 2

- Never pick a color pair without calculating its contrast ratio and writing the number down.
- Never use color alone to carry meaning.
- Every component you design must list: name, role, states (default, hover, focus, active, disabled, error), keyboard keys, and screen reader announcement.
- Use design tokens (named values) for colors, sizes and spacing so they can be fixed in one place.
- Provide alt text suggestions for every image and mark decorative images.
- If you generate screens, also generate a short "reading order" list per screen.

## 🚦 GATE 2: Design complete

- [ ] Palette passes contrast (light and dark). Proof: [FILL]
- [ ] Type, spacing and zoom rules defined. Proof: [FILL]
- [ ] Targets sized correctly on all platforms. Proof: [FILL]
- [ ] Focus style defined. Proof: [FILL]
- [ ] Every component in the table is filled. Proof: [FILL]
- [ ] Top journeys reviewed by a person using keyboard-only and screen reader on prototypes. Proof: [FILL]
- Approved by: [FILL] on [FILL]

---

# PHASE 3: Development (with AI agents)

**Goal:** Build it so it works with keyboards, screen readers and every device.
**Timing:** [FILL] **Owner:** [FILL: Developer]

## 3.1 Code rules (all platforms)

| # | Rule | Level |
|---|---|---|
| 1 | Use **native** elements first (web: `button`, `a`, `input`, `label`, `nav`, `main`, `h1` to `h6`; mobile: standard controls). Do not use a `div` with a click handler as a button. | ⛔ |
| 2 | Use ARIA only when native elements cannot do the job. "No ARIA is better than bad ARIA." | ⛔ |
| 3 | Every interactive element has an accessible **name**, **role** and **state** (expanded, selected, checked, disabled, invalid). | ⛔ |
| 4 | Page language set (`<html lang="en">`) and any change of language marked. | ⛔ |
| 5 | Unique, meaningful page titles. | ⛔ |
| 6 | Heading levels are in order (no skipping from `h1` to `h4` just for looks). | ✅ |
| 7 | Landmarks used: `header`, `nav`, `main`, `footer`. | ✅ |
| 8 | Dynamic updates announced with live regions (`aria-live`) or platform announcements, without stealing focus. | ⛔ |
| 9 | When a dialog opens, focus moves in; when it closes, focus returns where it was. | ⛔ |
| 10 | Do not use positive `tabindex` values (anything above 0). | ⛔ |
| 11 | Do not remove focus outlines (`outline: none`) without a better replacement. | ⛔ |
| 12 | Respect user settings: `prefers-reduced-motion`, `prefers-color-scheme`, `prefers-contrast`, OS font scale. | ⛔ |
| 13 | Use relative units (`rem`, `em`, `%`, `sp`) so text can scale. | ✅ |
| 14 | Provide text alternatives for images, icons, canvas, SVG and charts. | ⛔ |
| 15 | Make sticky elements (headers, banners) not hide focused items (use `scroll-padding`). | ⛔ |
| 16 | Do not rely on hover alone; hover content must be dismissible, hoverable and persistent (1.4.13). | ⛔ |
| 17 | Respect status messages (3.3.1, 4.1.3). | ⛔ |
| 18 | Parsing is robust; unique IDs, valid markup. | ✅ |

## 3.2 Platform rules (fill in your stack)

| Platform | Our stack | Rules we follow | Doc link |
|---|---|---|---|
| Web | [FILL: React / Vue / plain HTML] | WCAG 2.2 AA; WAI-ARIA Authoring Practices | [FILL] |
| iOS | [FILL: SwiftUI / UIKit] | Apple Human Interface Guidelines, accessibility modifiers | [FILL] |
| Android | [FILL: Compose / Views] | Material accessibility, `semantics` / `contentDescription` | [FILL] |
| Desktop | [FILL: Electron / .NET / Qt / native] | Platform accessibility APIs, WCAG2ICT | [FILL] |
| Cross-platform | [FILL: Flutter / React Native / etc.] | Semantics widgets / accessibility props; test on real devices | [FILL] |

## 3.3 Automated checks built into the pipeline

| Check | Tool examples | Runs when | Blocks the merge if it fails? |
|---|---|---|---|
| Linting for accessibility | `eslint-plugin-jsx-a11y`, Android Lint, Xcode Accessibility Inspector audit | Every save / commit | ☐ Yes |
| Automated page scans | axe-core / axe DevTools, Lighthouse, Pa11y | Every pull request | ☐ Yes |
| Component tests | Jest + `jest-axe`, Storybook a11y add-on, Playwright + axe | Every pull request | ☐ Yes |
| Mobile scans | Accessibility Scanner (Android), Accessibility Inspector (Xcode) | Every release candidate | ☐ Yes |

⚠️ **Automated tools find only about 30 to 40% of problems.** They are necessary, but they are never enough. Manual testing in Phase 4 is required.

## 3.4 Definition of Done (for every task)

A task is **not done** until:

- [ ] Works with keyboard only.
- [ ] Works with a screen reader (quick check).
- [ ] Passes automated scan with zero serious or critical issues.
- [ ] Looks right at 200% zoom and 320px width.
- [ ] Respects reduced motion and dark mode.
- [ ] Alt text, labels and error messages written.
- [ ] Reviewed by a second person or a different AI agent.
- [ ] Proof attached to the ticket.

## 3.5 Rules for working with AI coding agents

1. **AI writes the first draft, humans (or a second AI) review.** Never ship unreviewed AI code.
2. Paste the **AI Agent Instructions** from every phase into the agent's system prompt or project rules file (for example `CLAUDE.md`, `AGENTS.md`, or Cursor rules).
3. Tell the agent your standard (**WCAG 2.2 AA**) and platform every time.
4. Ask the agent to **explain** how each component meets keyboard, screen reader and contrast needs.
5. Do not accept `div`-based buttons, missing labels, empty links, or `outline: none`.
6. Keep an **AI mistakes log** (Section 14.4). When an agent makes the same mistake twice, add a rule to your prompt.
7. Do not give agents real customer data.

## 🤖 AI Agent Instructions: Phase 3

- Target: WCAG 2.2 AA on [FILL: platforms].
- Use native, semantic elements before anything custom. Do not add ARIA that duplicates native meaning.
- Every interactive element must have: a name, a role, states, keyboard operation, and a visible focus indicator.
- Never remove focus outlines. Never set `tabindex` above 0.
- Never convey information by color alone. Never put important text in images.
- Support reduced motion, dark mode, text scaling, and 320px reflow.
- Write alt text and error messages in plain words.
- After each change, run the automated accessibility tests and report the results. If any serious issue appears, fix it before continuing.
- Add or update unit tests for keyboard and screen reader behavior.
- If you are unsure whether something is accessible, say so and ask. Do not claim "fully accessible". Say "meets the following checks: ...".

## 🚦 GATE 3: Development complete

- [ ] Code rules (3.1) followed. Proof: [FILL]
- [ ] Automated checks run in the pipeline and block on failure. Proof: [FILL]
- [ ] Definition of Done met on all top journeys. Proof: [FILL]
- [ ] AI-generated code reviewed by a human. Proof: [FILL]
- Approved by: [FILL] on [FILL]

---

# PHASE 4: Testing and QA

**Goal:** Prove it works for real people.
**Timing:** [FILL] **Owner:** [FILL: QA]

## 4.1 Test layers (do all four)

1. **Automated scans** (fast, catch about a third of issues)
2. **Manual checks** (keyboard, zoom, contrast, content)
3. **Assistive technology tests** (screen readers, voice, switch)
4. **Real users with disabilities** (the most valuable)

## 4.2 Manual test script (5-minute smoke test per screen)

| # | Test | How | Pass? | Proof |
|---|---|---|---|---|
| 1 | **Keyboard only** | Unplug the mouse. Tab through everything. Can you do every task? Can you always see where you are? | ☐ | [FILL] |
| 2 | **No traps** | Can you always leave menus, modals and widgets using the keyboard? | ☐ | [FILL] |
| 3 | **Zoom 200%** | Browser zoom or OS text size to 200%. Is anything cut off or overlapping? | ☐ | [FILL] |
| 4 | **Reflow 320px** | Narrow the window to 320px. Any sideways scroll? | ☐ | [FILL] |
| 5 | **Text spacing** | Apply a text spacing bookmarklet. Does text still fit? | ☐ | [FILL] |
| 6 | **Color** | Use grayscale or a color-blindness simulator. Is meaning still clear? | ☐ | [FILL] |
| 7 | **Contrast** | Check text and UI parts with a contrast tool. | ☐ | [FILL] |
| 8 | **Screen reader pass** | Turn the screen off. Can you finish the top journey? | ☐ | [FILL] |
| 9 | **Voice control** | Say "click [label]". Do names match what is shown? | ☐ | [FILL] |
| 10 | **Reduce motion / dark mode / high contrast** | Turn the OS setting on. | ☐ | [FILL] |
| 11 | **Captions and transcripts** | Play every video and audio file. | ☐ | [FILL] |
| 12 | **Errors** | Submit forms with mistakes. Are errors announced and clear? | ☐ | [FILL] |
| 13 | **Timeouts** | Wait. Does the session expire without warning? | ☐ | [FILL] |
| 14 | **Orientation** | Rotate the device. | ☐ | [FILL] |

## 4.3 Screen reader test matrix (minimum)

| Platform | Screen reader + browser/app | Journeys tested | Result | Tester | Date |
|---|---|---|---|---|---|
| Windows | NVDA + Firefox or Chrome | [FILL] | ☐ Pass ☐ Fail | [FILL] | [FILL] |
| macOS | VoiceOver + Safari | [FILL] | ☐ Pass ☐ Fail | [FILL] | [FILL] |
| iOS | VoiceOver + Safari / app | [FILL] | ☐ Pass ☐ Fail | [FILL] | [FILL] |
| Android | TalkBack + Chrome / app | [FILL] | ☐ Pass ☐ Fail | [FILL] | [FILL] |
| Windows (optional) | JAWS or Narrator | [FILL] | ☐ Pass ☐ Fail | [FILL] | [FILL] |
| Linux (if supported) | Orca | [FILL] | ☐ Pass ☐ Fail | [FILL] | [FILL] |

## 4.4 WCAG 2.2 AA quick audit table

Mark each: ✅ Pass, ❌ Fail, ➖ N/A (give a reason). Use this as a final review, not as a replacement for testing.

| Principle | Check (plain words) | WCAG | Result | Notes |
|---|---|---|---|---|
| Perceivable | Images have alt text | 1.1.1 | | |
| | Video has captions; audio has transcript | 1.2.1 to 1.2.5 | | |
| | Structure is in code, not just looks | 1.3.1 | | |
| | Reading order is logical | 1.3.2 | | |
| | Instructions do not rely on shape, color or position alone | 1.3.3, 1.4.1 | | |
| | Works in both orientations | 1.3.4 | | |
| | Inputs have autocomplete info | 1.3.5 | | |
| | Text contrast 4.5:1 / 3:1 | 1.4.3 | | |
| | Text resizes to 200% | 1.4.4 | | |
| | No images of text | 1.4.5 | | |
| | Reflow at 320px | 1.4.10 | | |
| | UI part contrast 3:1 | 1.4.11 | | |
| | Text spacing override works | 1.4.12 | | |
| | Hover/focus content is dismissible and persistent | 1.4.13 | | |
| Operable | Everything works by keyboard | 2.1.1 | | |
| | No keyboard trap | 2.1.2 | | |
| | Shortcut keys can be turned off | 2.1.4 | | |
| | Time limits adjustable | 2.2.1 | | |
| | Pause, stop, hide moving content | 2.2.2 | | |
| | Nothing flashes more than 3 times/sec | 2.3.1 | | |
| | Skip links / bypass blocks | 2.4.1 | | |
| | Page titles | 2.4.2 | | |
| | Focus order | 2.4.3 | | |
| | Link purpose clear | 2.4.4 | | |
| | More than one way to find pages | 2.4.5 | | |
| | Headings and labels descriptive | 2.4.6 | | |
| | Focus visible | 2.4.7 | | |
| | Focus not obscured | 2.4.11 | | |
| | Pointer gestures have simple alternatives | 2.5.1 | | |
| | Pointer cancellation | 2.5.2 | | |
| | Label in name | 2.5.3 | | |
| | Motion actuation has alternative | 2.5.4 | | |
| | Dragging has alternative | 2.5.7 | | |
| | Target size minimum | 2.5.8 | | |
| Understandable | Page language set | 3.1.1, 3.1.2 | | |
| | No surprise on focus or input | 3.2.1, 3.2.2 | | |
| | Consistent navigation and identification | 3.2.3, 3.2.4 | | |
| | Consistent help | 3.2.6 | | |
| | Errors identified and explained | 3.3.1, 3.3.3 | | |
| | Labels or instructions | 3.3.2 | | |
| | Error prevention (legal, financial, data) | 3.3.4 | | |
| | No redundant entry | 3.3.7 | | |
| | Accessible authentication | 3.3.8 | | |
| Robust | Status messages announced | 4.1.3 | | |
| | Names, roles, values exposed | 4.1.2 | | |

Note: WCAG 4.1.1 (Parsing) is retired in 2.2 and no longer needs testing, but valid code is still good practice.

## 4.5 Testing with real people

- [ ] ✅ Recruit **at least 5 people** with different needs (for example 2 screen reader users, 1 low-vision, 1 motor, 1 cognitive).
- [ ] ✅ Pay them fairly for their time.
- [ ] ✅ Ask them to complete the top journeys. Watch, do not coach.
- [ ] ✅ Record results and fix before launch.

| Participant (anonymous) | Need / tool | Journeys | Problems found | Fixed? |
|---|---|---|---|---|
| P1 | [FILL] | [FILL] | [FILL] | ☐ |
| P2 | [FILL] | [FILL] | [FILL] | ☐ |
| P3 | [FILL] | [FILL] | [FILL] | ☐ |

## 4.6 How serious is a bug?

| Severity | Meaning | Example | Fix by |
|---|---|---|---|
| **Blocker** | A person cannot finish a main journey. | Cannot pay with a screen reader. | **Before launch** |
| **Critical** | Very hard to finish, or a legal-level failure. | Focus disappears in checkout. | Before launch |
| **Major** | Annoying and slow but possible to finish. | Missing label on a field. | Within [FILL: e.g., 14 days] |
| **Minor** | Small issue, low impact. | Duplicate alt text. | Within [FILL: e.g., 60 days] |

## 4.7 Bug report template (copy for each bug)

```
Title:            [short, plain summary]
Severity:         [Blocker / Critical / Major / Minor]
WCAG criterion:   [e.g., 2.4.7 Focus Visible]
Platform/Device:  [e.g., iPhone 14, iOS 18, VoiceOver]
Steps to repeat:  1) ...  2) ...  3) ...
What happened:    [...]
What should happen: [...]
Proof:            [screenshot / recording / link]
Owner:            [name]
Due date:         [YYYY-MM-DD]
Status:           [Open / In progress / Fixed / Verified]
```

## 4.8 Create the ACR / VPAT (if needed)

- [ ] Fill the official ITI **VPAT 2.5** (or newer) based on the audit in 4.4. Mark each criterion Supports, Partially Supports, Does Not Support, or N/A.
- [ ] Link: [FILL]

## 🤖 AI Agent Instructions: Phase 4

- Write tests that cover keyboard navigation, focus, names and roles, contrast and zoom. Do not write tests that only check that elements "exist".
- Generate the bug report using the template in 4.7. Never close a bug without proof of verification.
- Do not claim a screen reader test passed. You cannot run real assistive technology. Mark it "needs human verification" unless a human confirms.
- Summarize audit results in plain words, with counts per severity.

## 🚦 GATE 4: Testing complete

- [ ] Automated scan: zero Blocker/Critical issues. Proof: [FILL]
- [ ] Manual smoke tests passed for all top journeys. Proof: [FILL]
- [ ] Screen reader matrix filled and passed. Proof: [FILL]
- [ ] Real-user test completed. Proof: [FILL]
- [ ] All Blockers and Criticals fixed and verified. Proof: [FILL]
- [ ] Remaining Majors and Minors are logged with dates. Proof: [FILL]
- Approved by: [FILL] on [FILL]

---

# PHASE 5: Launch

**Goal:** Go live safely, with a way for people to tell you about problems.
**Timing:** [FILL] **Owner:** [FILL: PM]

## 5.1 Launch checklist

- [ ] ⛔ **Accessibility Statement** published (Section 13). Link: [FILL]
- [ ] ⛔ **Feedback channel** live (email, form or phone). Contact: [FILL]
- [ ] ⛔ Promise a response time. Our promise: [FILL: e.g., reply within 2 business days]
- [ ] ⛔ **Exceptions Log** (Section 12) is up to date and every item has a plan and date.
- [ ] ⛔ **ACR / VPAT** completed, if required (Section 3.3).
- [ ] ⛔ Support team trained to take accessibility reports and not to say "we do not support that".
- [ ] ⛔ App store pages include accessibility information (iOS Accessibility Nutrition Labels where available, Google Play listing details).
- [ ] ✅ Marketing site, emails, social posts, help center, PDFs and videos are accessible too.
- [ ] ✅ Legal reviewed the statement and the laws list. Reviewer: [FILL]
- [ ] ⛔ Monitoring in place (Phase 6).
- [ ] ⛔ Rollback plan if an accessibility bug is found in the release.

## 5.2 Go / No-Go decision

| Question | Yes / No |
|---|---|
| Are all top journeys usable with keyboard and screen reader? | ☐ |
| Are there zero open Blocker or Critical issues? | ☐ |
| Is there a public way to report problems? | ☐ |
| Is there a named owner for accessibility after launch? | ☐ |

**All four must be Yes to launch.** If any is No, you may only launch with a signed exception in Section 12.

Decision: ☐ GO ☐ NO-GO Decided by: [FILL] Date: [FILL]

## 🤖 AI Agent Instructions: Phase 5

- Draft the accessibility statement from Section 13 using real test results only. Do not invent conformance claims.
- Draft support-team scripts for accessibility reports in plain language.
- Check that every release note and help article follows plain-language and heading rules.

## 🚦 GATE 5: Launch approved

- [ ] Section 5.1 checklist complete. Proof: [FILL]
- [ ] Go / No-Go signed. Proof: [FILL]

---

# PHASE 6: Post-Launch, Day 1 to Customer 500

**Goal:** Keep it accessible while you grow from 0 to 500 customers, and learn from real users.
**Owner:** [FILL: Accessibility Champion]

## 6.1 Growth milestones

| Milestone | What to do | Done? | Date |
|---|---|---|---|
| **Day 1 to 7** | Watch support and feedback daily. Fix Blockers within 48 hours. | ☐ | [FILL] |
| **First 10 customers** | Ask each: "Was anything hard to use?" Include at least 1 question on accessibility. | ☐ | [FILL] |
| **First 50 customers** | Run a full audit again (Phase 4 smoke tests and automated scan). Fix new Majors. | ☐ | [FILL] |
| **First 100 customers** | Interview at least 3 users with disabilities. Update the Exceptions Log. | ☐ | [FILL] |
| **First 250 customers** | Re-test with the latest OS, browser and screen reader versions. Review third-party tools. | ☐ | [FILL] |
| **Customer 500** | Full audit, update Accessibility Statement and ACR, run a retrospective (6.6). | ☐ | [FILL] |

## 6.2 Ongoing routine

| How often | Task | Owner |
|---|---|---|
| Every release | Automated accessibility tests in CI, Definition of Done | [FILL] |
| Every sprint | Review accessibility bug backlog; fix at least [FILL: number] items | [FILL] |
| Monthly | Review feedback inbox and support tickets for accessibility topics | [FILL] |
| Quarterly | Manual audit of top journeys; update document review date | [FILL] |
| Every OS / browser major release | Re-test top journeys | [FILL] |
| Yearly | Independent audit by an accessibility specialist; re-check laws list (Section 3) | [FILL] |

## 6.3 Measure it (track these numbers)

| Metric | How to measure | Target | Current |
|---|---|---|---|
| Open accessibility bugs by severity | Issue tracker label `a11y` | 0 Blockers, 0 Critical | [FILL] |
| Automated scan score / issue count | axe / Lighthouse in CI | Zero serious issues | [FILL] |
| Time to fix a Blocker | Days from report to fix | 2 days or fewer | [FILL] |
| Time to respond to feedback | Hours or days | [FILL: promise from 5.1] | [FILL] |
| Task success of assistive tech users | Moderated test | 90% or more | [FILL] |
| Accessibility reports per 100 customers | Support tickets | Trending down | [FILL] |
| Percent of releases that passed the Definition of Done | Release checklist | 100% | [FILL] |

## 6.4 Stop regressions (stop old bugs from returning)

- [ ] ⛔ Every fixed accessibility bug gets an automated test or a manual test step added to the smoke test.
- [ ] ⛔ New components must be added to the component table (2.9) before use.
- [ ] ✅ Keep a "known good" screen-reader recording of top journeys to compare.
- [ ] ✅ Add accessibility to the pull request template.

## 6.5 Handling feedback

1. **Say thanks** and confirm receipt within the promised time.
2. **Log** the report in the tracker with label `a11y` and severity (4.6).
3. **Offer a workaround** if the fix will take time (for example, a phone number or alternate form).
4. **Fix**, **verify** with the reporter if they are willing.
5. **Update** the Exceptions Log and the statement if needed.

## 6.6 Retrospective at customer 500

Answer honestly.

| Question | Your answer |
|---|---|
| What accessibility problems appeared most often? | [FILL] |
| What did we catch too late? | [FILL] |
| What rule in this template should be changed? | [FILL] |
| What do we do differently for the next project? | [FILL] |
| Customers who told us about accessibility problems | [FILL: number] |
| Customers who said accessibility helped them | [FILL: number] |

➡️ **Send improvements back to the master template** (Appendix B).

## 🤖 AI Agent Instructions: Phase 6

- Read the accessibility feedback inbox summaries and cluster them by WCAG criterion and severity.
- Propose fixes and tests, but do not close tickets without human verification.
- When asked to update the statement, change only what test evidence supports.
- Never delete or hide negative feedback.

## 🚦 GATE 6: Customer-500 review

- [ ] Customer 500 audit done. Proof: [FILL]
- [ ] Statement and ACR updated. Proof: [FILL]
- [ ] Retrospective done and template improvements sent. Proof: [FILL]

---

# Section 12: Exceptions Log

Use this when you **cannot** meet a rule right now. Honesty here protects you legally and morally. Every exception needs an owner, an alternative and a date.

| # | Rule / WCAG item | Where (screen, page) | Why we cannot meet it | Who is affected | Alternative offered | Plan to fix | Owner | Fix by | Approved by | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | [FILL: e.g., 1.2.5 audio description] | [FILL: Intro video] | [FILL: Vendor tool lacks it] | [FILL: Blind users] | [FILL: Text transcript with visual details] | [FILL] | [FILL] | [FILL] | [FILL] | ☐ Open ☐ Closed |
| 2 | | | | | | | | | | |

Rules:
- "It is too hard" or "no time" is **not** a valid reason by itself. Write the real constraint.
- No exception may block a main journey from being completed. If it does, you cannot launch.
- Review the log every month.

---

# Section 13: Accessibility Statement Template

Copy this onto a public page called "Accessibility". Replace everything in brackets. Only write things that are true.

```
# Accessibility Statement for [Product Name]

[Company Name] is committed to making [Product Name] usable by everyone,
including people with disabilities.

## Our standard
We aim to meet the Web Content Accessibility Guidelines (WCAG) 2.2, Level AA.

## Where we are today
Status: [Fully / Partially / Not yet] meets WCAG 2.2 AA.
Last tested: [date]. How we tested: [automated tools, manual checks,
screen readers (list them), and testing with people with disabilities].

## Known issues
- [Issue 1, where it is, and the workaround]
- [Issue 2, planned fix date]

## Platforms covered
[Website / iOS app / Android app / Windows / macOS / Linux]

## Tell us about a problem
Email: [address]    Phone: [number]    Form: [link]
We reply within [number] business days.

## Alternative ways to get help
[Phone ordering, live chat, etc.]

## If we do not reply or fix the problem
[Regulator or enforcement body for your country, if required by law,
for example the national enforcement body in your EU country.]

Last updated: [date]
```

---

# Section 14: AI Agent Prompt Library

Copy these prompts into your AI tool. Replace the `[brackets]`.

## 14.1 Master "project rules" prompt (paste once at the start of every project)

```
You are building [Product Name] for [platforms].
Our accessibility standard is WCAG 2.2 Level AA. This is a hard requirement.

Always:
- Use native, semantic elements before custom ones; avoid unnecessary ARIA.
- Give every interactive element a name, role, state, keyboard support,
  and a visible focus indicator (never remove outlines).
- Never convey meaning by color alone. Meet 4.5:1 text contrast and 3:1 for UI parts.
- Support 200% text size, 320px reflow, reduced motion, and dark mode.
- Make touch targets at least 44x44 (iOS/web) or 48x48 (Android).
- Write plain-language labels, errors, and alt text.
- Run the accessibility tests after every change and show me the results.
- If unsure, ask. Never claim something is "fully accessible"; list the checks it passed.
```

## 14.2 Component prompt

```
Create an accessible [component] for [platform/framework].
Return: 1) the code, 2) keyboard keys it supports, 3) what a screen reader announces,
4) all states (default, hover, focus, active, disabled, error),
5) automated and manual tests, 6) contrast numbers used.
```

## 14.3 Review prompt (use a different AI session than the one that wrote the code)

```
Review the following code against WCAG 2.2 AA.
List each problem with: WCAG number, severity (Blocker/Critical/Major/Minor),
where it is, why it is a problem in plain words, and the exact fix.
Do not invent problems. If something cannot be checked from code alone, say
"needs human testing".
```

## 14.4 AI mistakes log

| Date | Tool | What it got wrong | Rule added to prompt |
|---|---|---|---|
| [FILL] | [FILL] | [FILL: e.g., used div as button] | [FILL] |

---

# Section 15: Glossary (plain words)

| Word | Meaning |
|---|---|
| **A11y** | Short for "accessibility". |
| **WCAG** | Web Content Accessibility Guidelines, the world's main accessibility rulebook. |
| **Level A / AA / AAA** | How strict the rule is. AA is the usual goal. |
| **Assistive technology (AT)** | Tools disabled people use, such as screen readers or switches. |
| **Screen reader** | Software that reads the screen aloud or to a braille display. |
| **Alt text** | A short text description of an image. |
| **ARIA** | Extra code labels that help assistive tools when normal elements are not enough. |
| **Semantic HTML** | Using the right tag for the right job (button for buttons). |
| **Focus** | Which item the keyboard is currently on. |
| **Focus indicator** | The visible outline showing where focus is. |
| **Keyboard trap** | A place where the keyboard gets stuck. |
| **Contrast ratio** | How different two colors are, measured as a number such as 4.5:1. |
| **Reflow** | Content rearranging itself when the screen is narrow or zoomed. |
| **Target size** | How big a button or link is to tap or click. |
| **Live region** | A part of the screen whose changes are announced automatically. |
| **Captions** | Text for spoken audio in video. |
| **Audio description** | Spoken explanation of important visuals in video. |
| **Transcript** | Full text version of audio or video. |
| **ACR / VPAT** | A report that says how well a product meets accessibility rules. |
| **EAA** | European Accessibility Act. |
| **ADA** | Americans with Disabilities Act. |
| **Section 508** | US law on accessible technology for federal government. |
| **Regression** | An old bug coming back. |
| **Definition of Done** | The checklist that says a task is really finished. |
| **Gate** | A checkpoint you must pass before the next phase. |
| **Design token** | A named value (such as a color) stored in one place and reused everywhere. |

---

# Section 16: Resources

> Check these are still current before sharing. Write the date you last checked: [FILL]

- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- WCAG quick reference: https://www.w3.org/WAI/WCAG22/quickref/
- Understanding WCAG 2.2: https://www.w3.org/WAI/WCAG22/Understanding/
- WAI-ARIA Authoring Practices: https://www.w3.org/WAI/ARIA/apg/
- WCAG2ICT (applying WCAG to apps and non-web software): https://www.w3.org/TR/wcag2ict/
- Mobile accessibility at W3C: https://www.w3.org/WAI/standards-guidelines/mobile/
- Apple Accessibility (HIG): https://developer.apple.com/design/human-interface-guidelines/accessibility
- Android Accessibility: https://developer.android.com/guide/topics/ui/accessibility
- Material Design Accessibility: https://m3.material.io/foundations/accessible-design/overview
- Microsoft Accessibility: https://learn.microsoft.com/windows/apps/design/accessibility/
- GOV.UK Accessibility: https://www.gov.uk/guidance/accessibility-requirements-for-public-sector-websites-and-apps
- WebAIM (articles, contrast checker, WAVE): https://webaim.org/
- axe DevTools: https://www.deque.com/axe/
- NVDA screen reader (free): https://www.nvaccess.org/
- Colour Contrast Analyser (free): https://www.tpgi.com/color-contrast-checker/
- ITI VPAT: https://www.itic.org/policy/accessibility/vpat
- Section508.gov: https://www.section508.gov/
- European Accessibility Act (EU): https://ec.europa.eu/social/main.jsp?catId=1202
- EN 301 549: https://www.etsi.org/standards (search "EN 301 549")

---

# Appendix A: Filled Example (a tiny sample, "PetPal")

Use this only to see what a good answer looks like.

**Section 1:** PetPal is a mobile and web app where dog owners book walkers. Users: owners aged 20 to 70. Platforms: Web, iOS, Android. Languages: English, Spanish. Countries: USA, Canada, Germany. Payments: yes. Launch: 2027-03-01. First 500 customers by: 2027-09-01. Target: WCAG 2.2 AA.

**Section 3 decision:** ADA (USA), EAA (Germany), Accessible Canada Act not applicable (not federally regulated), AODA not applicable (fewer than 50 employees, but we meet WCAG anyway). Strictest standard: EN 301 549 (WCAG 2.1 AA plus extras). Our target: WCAG 2.2 AA. Checked by Ana, 2026-11-02.

**Phase 1 journeys:** 1) Sign up, 2) Search walkers, 3) Book and pay, 4) Cancel booking, 5) Contact support.

**Phase 2 palette row:** Primary text #1A1A1A on #FFFFFF = 17.4:1, passes. Primary button #0B5FFF with white text = 5.3:1, passes. Error text #B00020 on white = 7.1:1, passes (and always paired with an icon and words).

**Phase 2 component row:** Button. Enter and Space activate. Announces "Book walk, button". Contrast passes. Size 48 × 48 dp. Proof: link to the Figma frame.

**Phase 3 DoD proof:** Pull request #42 includes a screen recording using only a keyboard, an axe report with zero serious issues, and a VoiceOver recording of the booking flow.

**Phase 4 bug example:**
- Title: Focus hidden behind sticky header on the Checkout page
- Severity: Critical
- WCAG: 2.4.11 Focus Not Obscured
- Platform: Chrome on Windows, keyboard only
- Fix: added `scroll-padding-top: 80px`
- Status: Verified by QA on 2027-02-10

**Phase 5:** Statement published at petpal.example/accessibility. Feedback email: access@petpal.example. Response promise: 2 business days. GO decided by Priya on 2027-02-25.

**Phase 6, Customer 100:** Interviewed 3 users (2 blind, 1 low vision). Found that the map is hard to use with a screen reader. Added a list view alternative. Logged exception #1 until the new map library arrives, with a fix date of 2027-07-01.

---

# Appendix B: Version History

| Version | Date | Changed by | What changed |
|---|---|---|---|
| 1.0 | [FILL: YYYY-MM-DD] | [FILL] | First version of the template |
| | | | |

**Template improvement ideas collected from projects:**

- [FILL]

---

*End of document. If every Gate is ticked and every `[FILL]` is replaced, you are ready. Keep this file alive: review it at least every 90 days.*
