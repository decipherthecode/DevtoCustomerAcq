# 📖 HOW TO FILL THIS DOCUMENT

> **Read this first before touching anything below.**

---

## 🟢 What Is This Document?

This is your project's **Accessibility Standards file**. It is a living checklist and record that proves your product works for **everyone** — including people who use screen readers, people who cannot use a mouse, people with color blindness, and people who rely on voice control or other assistive technology.

Think of it like a **safety inspection report for your product**. Just like a building needs a fire inspection before people move in, your software needs an accessibility check before real users start using it.

---

## 🟡 Who Should Fill This?

| Role | What They Fill |
|------|----------------|
| **Project Manager (PM)** | Section 1 (Project Info), Section 2 (Compliance), Section 12 (Legal) |
| **Designer (UX/UI)** | Section 5 (Design Phase Checklist) |
| **AI/Prompt Engineer** | Section 6 (AI-Generated Content Rules) |
| **Developer (Frontend/Backend)** | Section 7 (Development Checklist) |
| **QA / Tester** | Section 8 (Testing), Section 9 (Launch Gate) |
| **Accessibility Lead** | All sections — reviews and signs off |
| **Everyone** | Section 11 (Issue Tracker) when they find a problem |

---

## 🔵 How To Fill Each Section

1. **Replace every `[PLACEHOLDER]` or `_____` with your real project information.**
   - Example: `[Project Name]` → `MediBook Patient Portal`

2. **Check the boxes** `[ ]` → `[x]` when a task is done.

3. **If something does not apply to your project**, write `N/A` and explain why in one sentence.

4. **Color guide for status tags:**
   - 🔴 `[NOT STARTED]` — Work hasn't begun
   - 🟡 `[IN PROGRESS]` — Someone is working on it
   - 🟢 `[COMPLETE]` — Done and verified
   - ⚫ `[N/A]` — Does not apply to this project

5. **Save this file in your Git repository** at the path: `docs/Accessibility_Standards.md`

6. **Update the Revision History table** (Section 14) every time you make a significant change.

---

## 🔴 Important Rules

- **Never delete a section** even if it seems irrelevant. Mark it `N/A` instead.
- **Never mark a checkbox `[x]`** unless the work is actually done and you can prove it.
- **The Accessibility Lead must review and sign off** before launch (see Section 9).
- **Every accessibility bug found goes into Section 11** — do not just "fix it and forget it."

---

## 💡 A Quick Note on Why Accessibility Matters

> About **1 in 4 adults** has a disability that affects how they use digital products (CDC, 2023). Making your product accessible is not just the law — it means **25% more people can use what you built**.
>
> In the US, the **ADA (Americans with Disabilities Act)** requires digital accessibility. In the EU, the **European Accessibility Act (EAA)** became enforceable in 2025. Companies that ignore this face lawsuits, fines, and losing enterprise customers who require compliance.

---

---
---

# ♿ ACCESSIBILITY STANDARDS DOCUMENT

**Template Version:** 2.0.0
**WCAG Version Targeted:** WCAG 2.1 AA + WCAG 2.2 AA
**Additional Standards:** Section 508 (US) · EN 301 549 (EU/EAA)
**Last Updated:** [DATE — e.g., October 14, 2026]

---

## SECTION 1 — PROJECT INFORMATION

> 📝 **Instructions:** Fill in every field. This is the "cover page" of your accessibility record. Be specific — vague entries like "TBD" are not acceptable after the project starts.

---

| Field | Your Answer |
|-------|-------------|
| **Project / Product Name** | [e.g., MediBook Patient Portal] |
| **Project Code / ID** | [e.g., PRJ-2026-047] |
| **Product Type** | ☐ Web Application  ☐ Mobile App (iOS)  ☐ Mobile App (Android)  ☐ Both Web + Mobile |
| **Industry / Sector** | ☐ SaaS/Tech  ☐ Healthcare  ☐ Fintech/Banking  ☐ Education  ☐ Other: _______ |
| **Brief Product Description** | [1–2 sentences: What does this product do, and who uses it?] |
| **Target Users** | [e.g., "Healthcare professionals aged 25–60 using Chrome on desktop and iOS Safari on mobile"] |
| **Expected Disabled-User Percentage** | [e.g., "Estimated 15–20% of users may require assistive technology"] |
| **AI Components in Product** | [e.g., "Claude API for patient summary generation; Playwright AI for automated test coverage"] |
| **Accessibility Lead Name** | [Full name + email] |
| **Project Manager Name** | [Full name + email] |
| **Engineering Lead Name** | [Full name + email] |
| **Design Lead Name** | [Full name + email] |
| **QA Lead Name** | [Full name + email] |
| **Project Start Date** | [e.g., January 6, 2026] |
| **Planned Launch Date** | [e.g., April 30, 2026] |
| **First 500 Customers Target Date** | [e.g., July 31, 2026] |
| **Document Status** | 🔴 [NOT STARTED] |

---

## SECTION 2 — COMPLIANCE STANDARDS & TARGETS

> 📝 **Instructions:** This section defines the "rules" your product must follow. Check every standard that applies. For each checked standard, fill in the target conformance level.

---

### 2.1 Standards Checklist

| Standard | Applies? | Target Level | Notes |
|----------|----------|--------------|-------|
| **WCAG 2.1** (Web Content Accessibility Guidelines) | ☐ Yes  ☐ No | ☐ A  ☐ AA  ☐ AAA | Minimum: AA for most projects |
| **WCAG 2.2** (Latest version — adds 9 new criteria) | ☐ Yes  ☐ No | ☐ A  ☐ AA  ☐ AAA | Recommended if launching in 2025+ |
| **Section 508** (US Federal / Government contracts) | ☐ Yes  ☐ No | Full Conformance | Required if serving US government |
| **EN 301 549** (EU — European Accessibility Act) | ☐ Yes  ☐ No | Full Conformance | Required for EU market after June 2025 |
| **ADA Title III** (US — public accommodations) | ☐ Yes  ☐ No | WCAG 2.1 AA | Covers most US consumer-facing products |
| **AODA** (Ontario, Canada) | ☐ Yes  ☐ No | WCAG 2.0 AA | Required for Ontario businesses 20+ employees |
| **CVAA** (US — communications/video) | ☐ Yes  ☐ No | As specified | Only if product includes video/audio calls |

---

### 2.2 WCAG 2.2 New Criteria Status

> 💡 **What is WCAG 2.2?** It's the updated rulebook released in October 2023. It adds 9 new rules to WCAG 2.1. If you're checking the WCAG 2.2 box above, also track the 9 new criteria here.

| New Criterion | ID | What It Means (Plain English) | Status |
|---------------|-----|-------------------------------|--------|
| Focus Not Obscured (Minimum) | 2.4.11 | When you tab to a button, the keyboard focus ring must not be hidden behind floating banners or sticky headers. | 🔴 [NOT STARTED] |
| Focus Not Obscured (Enhanced) | 2.4.12 | The focused element must be fully visible — no partial hiding allowed. | 🔴 [NOT STARTED] |
| Focus Appearance | 2.4.13 | The keyboard focus indicator must be big enough and have enough contrast to see clearly. | 🔴 [NOT STARTED] |
| Dragging Movements | 2.5.7 | Any action done by dragging (e.g., a slider) must also work with a single click/tap. | 🔴 [NOT STARTED] |
| Target Size (Minimum) | 2.5.8 | Clickable/tappable areas must be at least 24×24 pixels. | 🔴 [NOT STARTED] |
| Consistent Help | 3.2.6 | Help links (chat, FAQ, phone) must appear in the same place on every page. | 🔴 [NOT STARTED] |
| Redundant Entry | 3.3.7 | Users should not have to type the same information twice in one session (e.g., address on checkout and delivery). | 🔴 [NOT STARTED] |
| Accessible Authentication (Minimum) | 3.3.8 | Login must not require memory-based cognitive tests (e.g., "solve this puzzle"). | 🔴 [NOT STARTED] |
| Accessible Authentication (Enhanced) | 3.3.9 | Even stricter — no cognitive tests at all in authentication flows. | 🔴 [NOT STARTED] |

---

### 2.3 Conformance Goal

```
Overall Conformance Target:    [e.g., WCAG 2.2 Level AA — Full Conformance]
Acceptable Known Exceptions:   [List any planned exceptions and why they are acceptable]
Conformance Claim Owner:       [Accessibility Lead name]
Claim Review Date:             [Date the conformance claim will be formally reviewed]
```

---

## SECTION 3 — ROLES, RESPONSIBILITIES & RACI MATRIX

> 📝 **Instructions:** Fill in the names for each role. Then read the RACI table — it tells everyone exactly who is Responsible (R), who is Accountable (A), who should be Consulted (C), and who should be Informed (I).
>
> **RACI Explained for beginners:**
> - **R = Responsible** → The person who does the actual work
> - **A = Accountable** → The person who must answer if it goes wrong (usually only 1 person)
> - **C = Consulted** → People whose advice must be asked before a decision
> - **I = Informed** → People who need to know what happened (after the fact)

---

### 3.1 Team Directory

| Role | Name | Email | Backup Person |
|------|------|-------|---------------|
| **Accessibility Lead** | [Name] | [email] | [Backup name] |
| **Project Manager** | [Name] | [email] | [Backup name] |
| **Design Lead** | [Name] | [email] | [Backup name] |
| **Frontend Engineer(s)** | [Name(s)] | [email(s)] | [Backup name] |
| **AI/Prompt Engineer** | [Name] | [email] | [Backup name] |
| **QA / Test Engineer** | [Name] | [email] | [Backup name] |
| **Product Owner** | [Name] | [email] | [Backup name] |
| **Legal / Compliance** | [Name] | [email] | [Backup name] |

---

### 3.2 RACI Matrix

| Activity | Accessibility Lead | PM | Designer | Developer | AI Engineer | QA | Product Owner |
|----------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Define accessibility standards for this project | A | C | I | I | I | I | C |
| Design-phase accessibility review | C | I | R | I | I | I | A |
| AI content accessibility guidelines | A | I | C | C | R | I | I |
| Code-level accessibility implementation | C | I | C | R | R | I | A |
| Automated accessibility testing setup | C | I | I | R | R | A | I |
| Manual screen reader testing | R | I | I | C | I | R | A |
| Issue severity rating (P1–P4) | R | C | I | I | I | R | A |
| Launch gate sign-off | A | R | C | C | C | R | C |
| Post-launch monitoring | R | I | I | C | C | R | A |
| Legal/compliance documentation | C | A | I | I | I | I | C |
| Quarterly accessibility audit | R | C | C | C | C | R | A |

---

## SECTION 4 — DISCOVERY & PLANNING PHASE

> 📝 **Instructions:** Complete this section **before design begins**. This is the "set up the rules" phase. The Accessibility Lead and PM fill this together.

---

### 4.1 User Research — Disabled User Personas

> 💡 **What is a persona?** A persona is a made-up profile of a typical user that helps the team design for real people's needs. You must include at least one persona for a disabled user.

**Minimum Required Personas (add more rows as needed):**

| Persona Name | Disability / Condition | Assistive Technology Used | Key Needs & Pain Points |
|--------------|----------------------|--------------------------|------------------------|
| [e.g., "Maria, 52"] | [e.g., Low vision (20/200)] | [e.g., ZoomText + NVDA screen reader on Windows] | [e.g., Needs high contrast, large font, audio descriptions of charts] |
| [e.g., "James, 34"] | [e.g., Motor disability — limited hand mobility] | [e.g., Keyboard-only navigation, voice control via Dragon NaturallySpeaking] | [e.g., Cannot use a mouse; needs all features reachable by Tab key] |
| [e.g., "Priya, 28"] | [e.g., Deaf / hard of hearing] | [e.g., Closed captions; no assistive tech device] | [e.g., All audio content must have captions or transcripts] |
| [e.g., "Eli, 19"] | [e.g., ADHD / cognitive disability] | [e.g., No assistive tech; uses plain language and simplified navigation] | [e.g., Minimal distractions, clear error messages, no time limits on forms] |

---

### 4.2 Assistive Technology (AT) Support Matrix

> 📝 **Instructions:** Tick every AT combination your product must officially support. These become your test targets in Section 8.

| Assistive Technology | Platform | Browser / OS | Must Support? |
|----------------------|----------|-------------|---------------|
| NVDA (screen reader) | Windows | Chrome | ☐ Yes  ☐ No |
| NVDA (screen reader) | Windows | Firefox | ☐ Yes  ☐ No |
| JAWS (screen reader) | Windows | Chrome | ☐ Yes  ☐ No |
| VoiceOver (screen reader) | macOS | Safari | ☐ Yes  ☐ No |
| VoiceOver (screen reader) | iOS | Safari | ☐ Yes  ☐ No |
| TalkBack (screen reader) | Android | Chrome | ☐ Yes  ☐ No |
| Keyboard-only navigation | All | All | ☐ Yes  ☐ No |
| Voice Control | iOS | Safari | ☐ Yes  ☐ No |
| Dragon NaturallySpeaking | Windows | Chrome | ☐ Yes  ☐ No |
| ZoomText / Magnifier | Windows | Any | ☐ Yes  ☐ No |
| High Contrast Mode | Windows | Any | ☐ Yes  ☐ No |
| Switch Access | Android | Chrome | ☐ Yes  ☐ No |
| Braille Display | Any | Any | ☐ Yes  ☐ No |

---

### 4.3 Accessibility Budget & Resources

| Item | Planned Budget | Assigned To | Status |
|------|----------------|-------------|--------|
| Automated testing tool license (e.g., Axe DevTools, Deque) | $_____ | [Name] | 🔴 [NOT STARTED] |
| Manual testing with disabled users (user research sessions) | $_____ | [Name] | 🔴 [NOT STARTED] |
| External accessibility audit (optional) | $_____ | [Name] | 🔴 [NOT STARTED] |
| Accessibility training for team | $_____ | [Name] | 🔴 [NOT STARTED] |
| Screen reader software licenses | $_____ | [Name] | 🔴 [NOT STARTED] |
| **Total** | $_____ | | |

---

### 4.4 Accessibility Milestones

> 📝 **Instructions:** Set specific dates for each milestone. "ASAP" is not a date.

| Milestone | Target Date | Owner | Status |
|-----------|-------------|-------|--------|
| Accessibility Standards document drafted & approved | [DATE] | Accessibility Lead | 🔴 [NOT STARTED] |
| Team accessibility training completed | [DATE] | PM | 🔴 [NOT STARTED] |
| Design accessibility review completed | [DATE] | Design Lead | 🔴 [NOT STARTED] |
| Automated testing CI/CD pipeline set up | [DATE] | Engineering Lead | 🔴 [NOT STARTED] |
| First manual screen reader test pass | [DATE] | QA Lead | 🔴 [NOT STARTED] |
| External audit (if applicable) | [DATE] | Accessibility Lead | 🔴 [NOT STARTED] |
| Launch Gate sign-off | [DATE] | Accessibility Lead | 🔴 [NOT STARTED] |
| Post-launch 30-day accessibility review | [DATE] | Accessibility Lead | 🔴 [NOT STARTED] |
| Post-launch 90-day review (at ~500 users) | [DATE] | Accessibility Lead | 🔴 [NOT STARTED] |

---

## SECTION 5 — DESIGN & PROTOTYPING PHASE CHECKLIST

> 📝 **Instructions:** The **Design Lead** fills this section during the UI/UX design phase — before any code is written. The **Accessibility Lead** reviews and co-signs each item. Do not move to development until all items are ✅ or marked N/A.
>
> **How to mark items:**
> - `[ ]` = Not done yet
> - `[x]` = Done and verified
> - `[N/A]` = Does not apply — explain why in the Notes column

---

### 5.1 Color & Contrast

| # | Requirement | What It Means (Plain English) | Done? | Notes |
|---|-------------|------------------------------|-------|-------|
| 5.1.1 | Normal text contrast ratio ≥ 4.5:1 | Small text (under 18pt) must have a 4.5:1 contrast between text color and background. Use a tool like [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/). | `[ ]` | |
| 5.1.2 | Large text contrast ratio ≥ 3:1 | Big text (18pt regular or 14pt bold) only needs 3:1 contrast. | `[ ]` | |
| 5.1.3 | UI component contrast ≥ 3:1 | Buttons, input borders, focus indicators must have 3:1 contrast against the background. | `[ ]` | |
| 5.1.4 | No information conveyed by color alone | If you use red = error, also use an icon or text label. Color blind users cannot rely on color alone. | `[ ]` | |
| 5.1.5 | Dark Mode variant passes contrast checks | If the product has a dark mode, run all contrast checks again on the dark color palette. | `[ ]` | |
| 5.1.6 | Focus indicator contrast ≥ 3:1 (WCAG 2.2) | The keyboard focus outline must have at least 3:1 contrast against adjacent colors. | `[ ]` | |
| 5.1.7 | Color palette documented in design system | All approved colors with their contrast ratios must be documented in Figma or your design system. | `[ ]` | |

---

### 5.2 Typography

| # | Requirement | What It Means (Plain English) | Done? | Notes |
|---|-------------|------------------------------|-------|-------|
| 5.2.1 | Minimum body font size ≥ 16px | Body text should be at least 16px on desktop, 14px on mobile (absolute minimum). | `[ ]` | |
| 5.2.2 | Line height ≥ 1.5× font size | Text must have enough space between lines. Example: 16px font → line height ≥ 24px. | `[ ]` | |
| 5.2.3 | Text can be resized to 200% without loss of content | When a user zooms to 200%, no text should be cut off or overlap. | `[ ]` | |
| 5.2.4 | No justified text alignment | Justified text creates uneven spacing that is hard for dyslexic users to read. Use left-align. | `[ ]` | |
| 5.2.5 | Font choices are readable (avoid decorative-only fonts for body) | Save fancy or decorative fonts for logos and headings only. | `[ ]` | |
| 5.2.6 | Letter spacing can be increased by 0.12em without breaking layout | Users with dyslexia often increase letter spacing. Make sure the layout does not break. | `[ ]` | |

---

### 5.3 Layout & Navigation

| # | Requirement | What It Means (Plain English) | Done? | Notes |
|---|-------------|------------------------------|-------|-------|
| 5.3.1 | Clear, consistent navigation across all pages | The navigation menu appears in the same place on every page. | `[ ]` | |
| 5.3.2 | Skip navigation link included | A "Skip to main content" link appears at the top so keyboard users can skip the menu. | `[ ]` | |
| 5.3.3 | Logical heading hierarchy (H1 → H2 → H3) designed | Pages must use headings in order. There is only one H1 per page. Think of it like an outline. | `[ ]` | |
| 5.3.4 | Touch target size ≥ 44×44px on mobile (Apple HIG) | Buttons and links on mobile must be at least 44×44 pixels so fingers can tap them easily. | `[ ]` | |
| 5.3.5 | Touch target size ≥ 24×24px minimum (WCAG 2.2 2.5.8) | The absolute minimum per WCAG 2.2. Aim for 44×44 as best practice. | `[ ]` | |
| 5.3.6 | Adequate spacing between interactive elements | Clickable elements must have at least 8px of space between them to prevent mis-taps. | `[ ]` | |
| 5.3.7 | Responsive design tested at 320px, 768px, 1280px, 1920px breakpoints | The layout must work at all common screen widths. | `[ ]` | |
| 5.3.8 | Content reflows at 400% zoom (no horizontal scroll needed) | At 400% zoom, users should only need to scroll vertically, not horizontally (WCAG 1.4.10). | `[ ]` | |
| 5.3.9 | Reading order matches visual order | The order elements appear when using Tab key or a screen reader must match the visual order on screen. | `[ ]` | |

---

### 5.4 Forms & Interactive Components

| # | Requirement | What It Means (Plain English) | Done? | Notes |
|---|-------------|------------------------------|-------|-------|
| 5.4.1 | Every form field has a visible label | Placeholder text is NOT a label. Every input box needs a label above or beside it that always stays visible. | `[ ]` | |
| 5.4.2 | Error messages describe what went wrong and how to fix it | "Invalid input" is bad. "Please enter a valid email address like name@example.com" is good. | `[ ]` | |
| 5.4.3 | Required fields are clearly marked | Mark required fields with * or "(required)" — not just color. | `[ ]` | |
| 5.4.4 | No time limits on forms (or user can extend) | Users who type slowly or use screen readers need more time. Either remove time limits or provide a way to extend. | `[ ]` | |
| 5.4.5 | Login/authentication works without cognitive puzzles (WCAG 2.2 3.3.8) | CAPTCHAs that require memory or problem-solving are banned at AA level. Use image CAPTCHAs or SMS OTP instead. | `[ ]` | |
| 5.4.6 | Duplicate data entry avoided (WCAG 2.2 3.3.7) | If a user already entered their address, do not ask them to type it again on the next step. | `[ ]` | |
| 5.4.7 | Dropdown menus are accessible via keyboard | All dropdown menus must open with Enter/Space and navigate with arrow keys. | `[ ]` | |
| 5.4.8 | Custom components (date pickers, modals, sliders) have accessibility specs | Every custom interactive element must have documented keyboard behavior and ARIA roles in the design spec. | `[ ]` | |

---

### 5.5 Media & Content

| # | Requirement | What It Means (Plain English) | Done? | Notes |
|---|-------------|------------------------------|-------|-------|
| 5.5.1 | All images have a defined alt-text strategy | Decorative images get empty alt="" . Meaningful images need descriptive alt text. | `[ ]` | |
| 5.5.2 | Icons-only buttons have text alternatives | A button with only a 🔍 icon must also have a screen-reader label like "Search". | `[ ]` | |
| 5.5.3 | Videos have captions | Every video must have synchronized closed captions (not just a transcript). | `[ ]` | |
| 5.5.4 | Videos have audio descriptions (if visuals convey information) | If a video shows data on a chart without narrating it, a text/audio description is needed. | `[ ]` | |
| 5.5.5 | Audio content has a transcript | Podcasts, voice notes, or audio clips must have a full text transcript. | `[ ]` | |
| 5.5.6 | Animations and motion can be paused or turned off | Flashing content that flashes more than 3 times per second can trigger seizures — must be removable. | `[ ]` | |
| 5.5.7 | Moving or scrolling content has a pause control | Auto-playing carousels, tickers, and animations must have a pause button. | `[ ]` | |
| 5.5.8 | PDFs and documents are tagged and accessible | Any PDF linked from the product must be accessible (tagged, proper reading order). | `[ ]` | |

---

### 5.6 Design Sign-Off

```
Design Phase Accessibility Review Completed By:  [Accessibility Lead Name]
Review Date:                                     [DATE]
Overall Design Accessibility Status:             ☐ APPROVED  ☐ APPROVED WITH CONDITIONS  ☐ REJECTED
Conditions / Outstanding Issues:                 [List any issues that must be fixed before dev begins]
Designer Acknowledgment:                         [Designer Name] confirms all flagged items are resolved.
```

---

## SECTION 6 — AI-GENERATED CONTENT ACCESSIBILITY RULES

> 📝 **Instructions:** This section is filled by the **AI/Prompt Engineer** with review from the **Accessibility Lead**. If your product uses any AI — a chatbot, AI-generated summaries, AI-created images, or AI-written text — every rule below applies.
>
> 💡 **Why does AI need special accessibility rules?** AI systems can generate content automatically — text, images, charts, even code. If the AI produces inaccessible output (e.g., an image with no alt text, or a wall of text with no structure), users with disabilities are harmed. These rules prevent that.

---

### 6.1 AI System Inventory

> 📝 **List every AI component in the product.** Add a row for each one.

| AI Component | Purpose | Output Type | Accessibility Risk |
|--------------|---------|-------------|-------------------|
| [e.g., Claude API via Anthropic SDK] | [e.g., Patient summary generation] | [e.g., Long-form text] | [e.g., No heading structure, no reading level control] |
| [e.g., Playwright AI] | [e.g., Automated accessibility test generation] | [e.g., Test scripts, reports] | [e.g., Internal tool — low user-facing risk] |
| [e.g., Image Generation API] | [e.g., Auto-generated product visuals] | [e.g., Images] | [e.g., No automatic alt text generated] |

---

### 6.2 AI Text Output Rules

| # | Rule | What It Means (Plain English) | Implemented? | How Verified |
|---|------|------------------------------|--------------|--------------|
| 6.2.1 | AI-generated text uses plain language (Flesch-Kincaid Grade ≤ 8) | AI responses must be written so a typical 13-year-old can understand them. No jargon unless the audience is experts. | `[ ]` | [e.g., Use Hemingway Editor or automated readability check on AI outputs] |
| 6.2.2 | AI-generated text includes proper heading structure (H1/H2/H3) when displaying long content | Long AI responses displayed to users must use headings, bullet points, or sections — not one big block of text. | `[ ]` | [e.g., Prompt engineering validation + UI rendering check] |
| 6.2.3 | Markdown/HTML from AI is correctly rendered in the UI | If the AI returns `**bold**` or `## Heading`, the UI must render it visually AND expose it to screen readers properly. | `[ ]` | [e.g., Manual screen reader test of AI output display component] |
| 6.2.4 | AI responses include content warnings if output may contain distressing content | For healthcare/mental health products: AI must warn users before presenting difficult content. | `[ ]` | [e.g., Prompt constraint + UI fallback if AI omits warning] |
| 6.2.5 | AI streaming output (token-by-token display) is screen-reader friendly | When AI types responses in real-time, the screen reader must announce new content without overwhelming the user. Use ARIA live regions correctly. | `[ ]` | [e.g., NVDA + Chrome test of streaming response component] |
| 6.2.6 | AI error messages are clear and actionable | If the AI fails (timeout, content filter), the error shown to the user must explain what happened and what to do next. | `[ ]` | [e.g., Test all AI error states with a screen reader] |
| 6.2.7 | AI-generated tables include column and row headers | Any table generated by AI must have proper `<th>` elements or equivalent ARIA roles. | `[ ]` | [e.g., Automated Axe scan on AI output] |
| 6.2.8 | AI-generated forms or data-entry prompts follow form accessibility rules | If the AI creates any input prompts, they must meet the same standards as human-designed forms (Section 5.4). | `[ ]` | |

---

### 6.3 AI Image & Media Output Rules

| # | Rule | What It Means (Plain English) | Implemented? | How Verified |
|---|------|------------------------------|--------------|--------------|
| 6.3.1 | Every AI-generated image has meaningful alt text | When the AI creates an image, the system must also generate and attach descriptive alt text. Do not display the image without it. | `[ ]` | |
| 6.3.2 | Alt text is generated by AI and reviewed by a human before display | AI-generated alt text must be reviewed for accuracy. Auto-generated alt text alone is not sufficient for high-stakes contexts (medical, financial). | `[ ]` | |
| 6.3.3 | AI-generated charts include a text-based data summary | Any chart created by AI must include a text table or summary of the data shown, so screen reader users get the same information. | `[ ]` | |
| 6.3.4 | AI-generated video/audio content has captions or transcripts | If the AI produces video or audio, automatic captions must be generated AND reviewed for accuracy. | `[ ]` | |

---

### 6.4 AI Prompt Engineering for Accessibility

> 📝 **Instructions:** Document the accessibility constraints built into your AI system prompts. This creates an auditable record of how accessibility is enforced at the AI layer.

**System Prompt Accessibility Constraints in Use:**

```markdown
# Copy or summarize the accessibility-related instructions in your AI system prompt here.
# Example:

- "Always use plain language. Target a reading level of Grade 8 or below."
- "When generating long responses, use H2 and H3 headings to organize content."
- "Never generate content without proper alt text suggestions for any visual description."
- "When generating tables, always include a header row."
- "If content may be distressing, prefix the response with a clear content warning."
```

**Prompt Accessibility Review Date:** [DATE]
**Reviewed By:** [AI Engineer + Accessibility Lead names]

---

### 6.5 Automated AI Accessibility Testing Configuration

| Tool | Purpose | Integrated Into CI/CD? | Run Frequency | Owner |
|------|---------|----------------------|---------------|-------|
| [e.g., Playwright AI + Axe-core] | Automated WCAG scanning on every build | ☐ Yes  ☐ No | [e.g., Every pull request] | [Name] |
| [e.g., Deque Axe DevTools] | Developer browser extension for dev-time scanning | ☐ Yes  ☐ No | [e.g., During code review] | [Name] |
| [e.g., Lighthouse CI] | Performance + accessibility score in CI | ☐ Yes  ☐ No | [e.g., On merge to main] | [Name] |
| [e.g., Pa11y] | CLI-based WCAG scan of rendered pages | ☐ Yes  ☐ No | [e.g., Nightly] | [Name] |

**Minimum Accessibility Score Gate:** Lighthouse Accessibility Score ≥ [e.g., 90/100] required to merge to `main`.

---

## SECTION 7 — DEVELOPMENT PHASE ACCESSIBILITY CHECKLIST

> 📝 **Instructions:** **Frontend Developers** fill this section as they build features. The **Accessibility Lead** reviews before code is merged. Run the automated scanner AND do a manual check for each item.
>
> 💡 **Quick Reference:** Open Chrome DevTools → Accessibility tree to inspect ARIA roles in real-time. Install the [Axe DevTools browser extension](https://www.deque.com/axe/devtools/) for instant feedback as you code.

---

### 7.1 Semantic HTML & Document Structure

| # | Requirement | What It Means (Plain English) | Done? | Evidence / Link |
|---|-------------|------------------------------|-------|-----------------|
| 7.1.1 | Use semantic HTML elements (`<nav>`, `<main>`, `<article>`, `<section>`, `<header>`, `<footer>`, `<button>`, `<a>`) | Do not use `<div>` for everything. Use the right HTML tag for the right thing. A button must be `<button>`, not `<div onclick>`. | `[ ]` | |
| 7.1.2 | One `<h1>` per page; headings do not skip levels (H1 → H2 → H3) | Each page has exactly one H1 (the page title). Subheadings flow logically: H2 → H3, never H1 → H3. | `[ ]` | |
| 7.1.3 | Page has a `<title>` element that is unique and descriptive | `<title>` in the browser tab must describe the current page. "My App" alone is bad; "Login — My App" is good. | `[ ]` | |
| 7.1.4 | Language attribute set on `<html>` element (`lang="en"`) | Screen readers use this to know what language to speak the content in. | `[ ]` | |
| 7.1.5 | If page switches language, mark with `lang` on the element | If a French quote appears on an English page, wrap it: `<span lang="fr">…</span>`. | `[ ]` | |
| 7.1.6 | Lists use `<ul>`, `<ol>`, `<dl>` semantically | Use `<ul>` for unordered lists, `<ol>` for numbered steps, `<dl>` for definition lists. | `[ ]` | |
| 7.1.7 | Tables use `<th>` for headers, `scope` attribute, and `<caption>` | Data tables must have a header row with `<th scope="col">` and a `<caption>` describing what the table contains. | `[ ]` | |

---

### 7.2 ARIA (Accessible Rich Internet Applications)

> 💡 **What is ARIA?** ARIA is a set of special HTML attributes (like `role="button"` or `aria-label="Close"`) that tell screen readers what a custom UI element is and what it does. **Rule #1: If a standard HTML element exists, use it instead of ARIA.** Only use ARIA for custom components.

| # | Requirement | What It Means (Plain English) | Done? | Evidence / Link |
|---|-------------|------------------------------|-------|-----------------|
| 7.2.1 | All ARIA `role`, `state`, and `property` attributes are used correctly | Check the [ARIA specification](https://www.w3.org/TR/wai-aria/) for correct usage. Wrong ARIA is worse than no ARIA. | `[ ]` | |
| 7.2.2 | `aria-label` or `aria-labelledby` on all interactive elements that have no visible text | Icon-only buttons must have `aria-label="Search"` so screen readers announce the purpose. | `[ ]` | |
| 7.2.3 | `aria-live` regions used correctly for dynamic content updates | When content changes dynamically (notifications, AI streaming, search results), use `aria-live="polite"` or `aria-live="assertive"`. | `[ ]` | |
| 7.2.4 | Modal dialogs trap focus and announce to screen readers | When a modal opens, keyboard focus moves inside it and cannot escape until the modal is closed. Use `role="dialog"` and `aria-modal="true"`. | `[ ]` | |
| 7.2.5 | `aria-expanded` used on accordion/dropdown triggers | Buttons that open dropdowns must have `aria-expanded="false"` (closed) / `aria-expanded="true"` (open). | `[ ]` | |
| 7.2.6 | `aria-describedby` used for error messages linked to form fields | Error messages must be programmatically connected to their input: `<input aria-describedby="email-error">`. | `[ ]` | |
| 7.2.7 | `aria-required="true"` on required form fields (or use `required` attribute) | Screen readers must announce when a field is required. | `[ ]` | |
| 7.2.8 | No `aria-hidden="true"` on focusable elements | Elements hidden from screen readers must also be hidden from keyboard focus. | `[ ]` | |

---

### 7.3 Keyboard Navigation

| # | Requirement | What It Means (Plain English) | Done? | Evidence / Link |
|---|-------------|------------------------------|-------|-----------------|
| 7.3.1 | All interactive elements reachable by Tab key | Every button, link, input, and interactive control must be reachable using the Tab key. | `[ ]` | |
| 7.3.2 | Logical, predictable Tab order | When the user presses Tab, focus must move in a logical order (usually top to bottom, left to right). | `[ ]` | |
| 7.3.3 | Visible focus indicator on all interactive elements | When any element has keyboard focus, a visible outline/ring must be visible. Never use `outline: none` without providing an equally visible alternative. | `[ ]` | |
| 7.3.4 | Focus not obscured by sticky headers or floating banners (WCAG 2.2 2.4.11) | When tabbing through a page, the focused element must be visible — not hidden behind a fixed header or cookie banner. | `[ ]` | |
| 7.3.5 | No keyboard traps (user can always Tab away from any element) | A user must never get "stuck" on an element with no way to move focus forward or backward. | `[ ]` | |
| 7.3.6 | Escape key closes modals, dropdowns, and tooltips | Pressing Escape must always close any floating overlay. | `[ ]` | |
| 7.3.7 | Arrow key navigation for widget patterns (menus, tabs, radio buttons) | Inside a navigation menu or radio group, arrow keys (not Tab) move between options. Follow [ARIA Authoring Practices Guide (APG)](https://www.w3.org/WAI/ARIA/apg/) patterns. | `[ ]` | |
| 7.3.8 | Drag-and-drop functionality has a keyboard alternative (WCAG 2.2 2.5.7) | Any drag action (e.g., reorder list items) must also be achievable with keyboard-only controls. | `[ ]` | |
| 7.3.9 | `tabindex` used correctly (only 0 and -1; no positive values) | Avoid `tabindex="5"` etc. — it breaks natural Tab order. Use `tabindex="0"` to add to Tab order and `tabindex="-1"` to remove. | `[ ]` | |

---

### 7.4 Images & Non-Text Content

| # | Requirement | What It Means (Plain English) | Done? | Evidence / Link |
|---|-------------|------------------------------|-------|-----------------|
| 7.4.1 | Meaningful images have descriptive `alt` text | `<img src="chart.png" alt="Bar chart showing 40% user growth in Q3 2026">` — describe what the image shows. | `[ ]` | |
| 7.4.2 | Decorative images have empty `alt=""` | If an image is just decoration (e.g., a background pattern), set `alt=""` so screen readers skip it. | `[ ]` | |
| 7.4.3 | Complex images (charts, diagrams, infographics) have an extended description | A short alt text is not enough for complex charts. Provide a text table or long description. | `[ ]` | |
| 7.4.4 | SVG icons are accessible | Inline SVGs need `<title>` and `aria-labelledby`. Decorative SVGs need `aria-hidden="true"`. | `[ ]` | |
| 7.4.5 | CAPTCHAs have an audio alternative | If a visual CAPTCHA is used, users must be able to switch to an audio version. | `[ ]` | |
| 7.4.6 | AI-generated images always have programmatic alt text | Never display an AI-generated image to users without an alt text being set in the DOM. | `[ ]` | |

---

### 7.5 Color, Contrast & Visual

| # | Requirement | What It Means (Plain English) | Done? | Evidence / Link |
|---|-------------|------------------------------|-------|-----------------|
| 7.5.1 | Contrast ratios meet design specs (from Section 5.1) | Verify in code that the implemented colors match the approved accessible palette. Use Axe DevTools to check automatically. | `[ ]` | |
| 7.5.2 | Windows High Contrast Mode supported | Test the app with Windows High Contrast mode on. CSS must not rely on background images to convey meaning. | `[ ]` | |
| 7.5.3 | Dark mode implementation passes all contrast checks | Run Axe scan with dark mode enabled. | `[ ]` | |
| 7.5.4 | No flashing content > 3 Hz | No content flashes more than 3 times per second. Use the [Photosensitive Epilepsy Analysis Tool (PEAT)](https://trace.umd.edu/peat/) to verify. | `[ ]` | |

---

### 7.6 Forms

| # | Requirement | What It Means (Plain English) | Done? | Evidence / Link |
|---|-------------|------------------------------|-------|-----------------|
| 7.6.1 | All form inputs have a `<label>` associated by `for`/`id` | `<label for="email">Email</label><input id="email" type="email">` — they must be linked. | `[ ]` | |
| 7.6.2 | Placeholder text is supplemental, not the only label | Placeholder disappears when typing begins — users forget what the field is for. The label must always be visible. | `[ ]` | |
| 7.6.3 | Error messages are programmatically associated with their fields | Use `aria-describedby` to link error text to its input field. | `[ ]` | |
| 7.6.4 | Success messages are announced to screen readers | Use `aria-live="polite"` for success/confirmation messages. | `[ ]` | |
| 7.6.5 | Autocomplete attributes set on personal data fields | `<input autocomplete="email">` — this helps users with cognitive disabilities and motor impairments who rely on autofill. | `[ ]` | |
| 7.6.6 | Form validation does not rely on color alone | An error state must use more than just a red border — include an error icon and text message. | `[ ]` | |

---

### 7.7 Mobile-Specific (iOS & Android)

| # | Requirement | What It Means (Plain English) | Done? | Evidence / Link |
|---|-------------|------------------------------|-------|-----------------|
| 7.7.1 | All touch targets ≥ 44×44 points (iOS HIG) | This is Apple's recommendation. Points ≠ pixels; check against device physical size. | `[ ]` | |
| 7.7.2 | VoiceOver (iOS) tested on primary user flows | Test the top 5 user flows using VoiceOver on a real iPhone or simulator. | `[ ]` | |
| 7.7.3 | TalkBack (Android) tested on primary user flows | Test the top 5 user flows using TalkBack on a real Android device or emulator. | `[ ]` | |
| 7.7.4 | Pinch-to-zoom not disabled | Never add `user-scalable=no` to the viewport meta tag. Users must be able to zoom. | `[ ]` | |
| 7.7.5 | Device font size changes respected | When a user increases font size in device settings, the app must not clip or overflow text. | `[ ]` | |
| 7.7.6 | Haptic/vibration feedback supports audio-only UX | If your app uses haptics, ensure they are not the sole means of conveying information. | `[ ]` | |
| 7.7.7 | Landscape and portrait orientations both accessible | Do not lock orientation. Ensure the app is usable in both orientations. | `[ ]` | |

---

### 7.8 Performance & Cognitive Accessibility

| # | Requirement | What It Means (Plain English) | Done? | Evidence / Link |
|---|-------------|------------------------------|-------|-----------------|
| 7.8.1 | Session timeout warnings given ≥ 20 seconds before expiry | If a session will expire, show a warning at least 20 seconds before and let the user extend it. | `[ ]` | |
| 7.8.2 | Error recovery is simple and forgiving | Users must be able to go back, fix a mistake, and resubmit without losing all their data. | `[ ]` | |
| 7.8.3 | Instructions do not rely on sensory characteristics alone | Avoid "Click the round button on the left" — users with vision impairments cannot see shape or position. Say "Click the Submit button". | `[ ]` | |
| 7.8.4 | Reading level of UI microcopy is Grade 8 or below | Error messages, tooltips, and labels must be written in plain language. | `[ ]` | |
| 7.8.5 | Consistent help mechanism present (WCAG 2.2 3.2.6) | A help link, contact option, or FAQ link must appear in the same place on every page. | `[ ]` | |

---

## SECTION 8 — TESTING & QUALITY ASSURANCE

> 📝 **Instructions:** The **QA Lead** owns this section. Complete all testing tiers before the Launch Gate (Section 9). Document your results — "we tested it" is not enough; record what you found and how it was resolved.

---

### 8.1 Automated Testing Results

| Tool | Pages / Flows Tested | Issues Found | Issues Fixed | Date | Report Link |
|------|---------------------|--------------|--------------|------|-------------|
| Axe-core (CI/CD) | [e.g., All 28 routes] | [#] | [#] | [DATE] | [Link to CI report] |
| Lighthouse CI | [e.g., Homepage, Dashboard, Checkout] | Score: [X/100] | N/A | [DATE] | [Link] |
| Pa11y CLI | [e.g., 15 critical user flows] | [#] | [#] | [DATE] | [Link] |
| Playwright AI scans | [e.g., Full E2E regression] | [#] | [#] | [DATE] | [Link] |

**Minimum Passing Score:** All automated tools must return 0 critical (P1) violations before launch.

---

### 8.2 Manual Screen Reader Testing

> 📝 **Instructions:** Complete manual testing with each AT combination listed in your Section 4.2 matrix. Test the **5 most critical user flows** at minimum.

**Critical User Flows Tested (define your own based on your product):**

| # | User Flow | e.g., MediBook Example |
|---|-----------|----------------------|
| Flow 1 | [Core action #1] | [e.g., Patient login → view appointment list] |
| Flow 2 | [Core action #2] | [e.g., Book a new appointment] |
| Flow 3 | [Core action #3] | [e.g., Read AI-generated health summary] |
| Flow 4 | [Core action #4] | [e.g., Fill medication form] |
| Flow 5 | [Core action #5] | [e.g., Receive and understand an error message] |

---

**Screen Reader Test Results:**

| Flow | NVDA + Chrome | JAWS + Chrome | VoiceOver macOS | VoiceOver iOS | TalkBack Android | Keyboard Only |
|------|:---:|:---:|:---:|:---:|:---:|:---:|
| Flow 1: [Name] | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail |
| Flow 2: [Name] | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail |
| Flow 3: [Name] | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail |
| Flow 4: [Name] | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail |
| Flow 5: [Name] | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail | ☐ Pass ☐ Fail |

**Notes on Failures:** [Describe each failure and link to the issue in Section 11]

---

### 8.3 User Testing with Disabled Participants

> 💡 **Why test with real users?** Automated tools catch ~30–40% of accessibility issues. Real users with disabilities find the other 60%. This step is not optional for high-stakes products.

| Item | Detail |
|------|--------|
| Number of participants recruited | [Minimum: 3 participants. Recommended: 5+] |
| Disability types represented | ☐ Visual  ☐ Motor  ☐ Hearing  ☐ Cognitive  ☐ Multiple |
| Session format | ☐ Moderated (facilitated)  ☐ Unmoderated (recorded)  ☐ Remote  ☐ In-person |
| Flows tested in sessions | [List flow names] |
| Recruitment source | [e.g., Fable.co, local disability organizations, internal employee network] |
| Date of sessions | [DATE] |
| Findings summary | [Link to user testing report or summary document] |
| Critical issues found | [#] |
| Issues resolved before launch | [#] |

---

### 8.4 Zoom & Magnification Testing

| Test | Zoom Level | Result | Notes |
|------|-----------|--------|-------|
| Content reflows (no horizontal scroll) | 400% | ☐ Pass ☐ Fail | |
| Text not cut off or overlapping | 200% | ☐ Pass ☐ Fail | |
| ZoomText / Windows Magnifier (full screen) | N/A | ☐ Pass ☐ Fail | |
| iOS pinch-to-zoom | 2× | ☐ Pass ☐ Fail | |
| Android font size Large & Extra Large | N/A | ☐ Pass ☐ Fail | |

---

## SECTION 9 — LAUNCH GATE CHECKLIST

> 📝 **Instructions:** This is the **final checkpoint before the product goes live**. The **Accessibility Lead signs off**. If any P1 item is not checked, the launch is **blocked** until it is resolved.
>
> 🚨 **P1 items are non-negotiable launch blockers.** Do not go live with an open P1 issue.

---

### 9.1 Pre-Launch Gate — Final Checklist

| Priority | Item | Status | Owner | Evidence |
|----------|------|--------|-------|----------|
| **🔴 P1 — LAUNCH BLOCKER** | Zero automated critical violations in production build | `[ ]` Done | QA Lead | [CI report link] |
| **🔴 P1 — LAUNCH BLOCKER** | All 5 critical user flows pass screen reader testing | `[ ]` Done | QA Lead | [Test report link] |
| **🔴 P1 — LAUNCH BLOCKER** | No keyboard traps in any user flow | `[ ]` Done | QA Lead | |
| **🔴 P1 — LAUNCH BLOCKER** | Login / authentication accessible (no cognitive CAPTCHA) | `[ ]` Done | Developer | |
| **🔴 P1 — LAUNCH BLOCKER** | All AI-generated images have alt text before display | `[ ]` Done | AI Engineer | |
| **🔴 P1 — LAUNCH BLOCKER** | Accessibility feedback channel configured and live | `[ ]` Done | PM | [URL / email] |
| **🟠 P2 — MUST FIX WITHIN 2 WEEKS** | All form fields have visible labels and error messages | `[ ]` Done | Developer | |
| **🟠 P2 — MUST FIX WITHIN 2 WEEKS** | All images have correct alt text | `[ ]` Done | Developer | |
| **🟠 P2 — MUST FIX WITHIN 2 WEEKS** | Color contrast passes for all text | `[ ]` Done | Developer | |
| **🟠 P2 — MUST FIX WITHIN 2 WEEKS** | Visible focus indicator on all interactive elements | `[ ]` Done | Developer | |
| **🟡 P3 — MUST FIX WITHIN 4 WEEKS** | WCAG 2.2 new criteria implemented | `[ ]` Done | Developer | |
| **🟡 P3 — MUST FIX WITHIN 4 WEEKS** | User testing with disabled participants completed | `[ ]` Done | QA Lead | |
| **⬜ P4 — PLANNED IMPROVEMENT** | Quarterly audit schedule established | `[ ]` Done | PM | |
| **⬜ P4 — PLANNED IMPROVEMENT** | VPAT / Accessibility Conformance Report drafted (if B2B) | `[ ]` Done | Accessibility Lead | |

---

### 9.2 Accessibility Statement Published

> 💡 **What is an Accessibility Statement?** It is a public page on your website (e.g., `/accessibility`) that tells users what standards you meet, how to report problems, and who to contact. It is legally required in the EU (EAA) and strongly recommended everywhere else.

| Item | Status | Link / Evidence |
|------|--------|-----------------|
| Accessibility Statement page live on production | ☐ Yes  ☐ No | [URL] |
| Statement includes compliance level (e.g., WCAG 2.2 AA) | ☐ Yes  ☐ No | |
| Statement includes known limitations | ☐ Yes  ☐ No | |
| Statement includes contact email for accessibility issues | ☐ Yes  ☐ No | [email] |
| Statement includes date of last review | ☐ Yes  ☐ No | |
| Statement reviewed by legal team | ☐ Yes  ☐ No | |

---

### 9.3 Launch Gate Sign-Off

```
Accessibility Lead Sign-Off:    _________________________________
Name:                           [Full Name]
Date:                           [DATE]
Launch Decision:                ☐ APPROVED FOR LAUNCH
                                ☐ APPROVED WITH CONDITIONS (list conditions below)
                                ☐ BLOCKED — DO NOT LAUNCH (list blockers below)

Conditions / Blockers:
[List any outstanding items here. For each: describe the issue, the P-level, the fix deadline,
and who owns the fix.]

PM Acknowledgment:              _________________________________
Engineering Lead Acknowledgment: _________________________________
```

---

## SECTION 10 — POST-LAUNCH MONITORING (FIRST 500 CUSTOMERS)

> 📝 **Instructions:** The work does not end at launch. This section tracks accessibility health from Day 1 through your first 500 users. The **Accessibility Lead and PM** co-own this section.

---

### 10.1 Accessibility Feedback Channel

| Channel Type | Details | Responsible Person | Status |
|---|---|---|---|
| In-app feedback button | [e.g., "Report Accessibility Issue" link in footer] | [Name] | 🔴 [NOT STARTED] |
| Dedicated email address | [e.g., accessibility@yourcompany.com] | [Name] | 🔴 [NOT STARTED] |
| Public issue tracker | [e.g., GitHub Issues with "accessibility" label] | [Name] | 🔴 [NOT STARTED] |
| Response SLA for accessibility reports | P1: [e.g., 24h] · P2: [e.g., 5 days] · P3: [e.g., 2 weeks] | [Name] | 🔴 [NOT STARTED] |

---

### 10.2 Automated Regression Monitoring

| Item | Tool | Schedule | Alert Recipient | Status |
|------|------|----------|-----------------|--------|
| Axe-core scan on every production deploy | [e.g., Playwright CI] | Every deploy | [Engineering Lead email] | 🔴 [NOT STARTED] |
| Weekly Lighthouse accessibility score report | [e.g., Lighthouse CI] | Weekly | [Accessibility Lead email] | 🔴 [NOT STARTED] |
| Slack/email alert when accessibility score drops below [X] | [e.g., Datadog + Lighthouse CI integration] | Real-time | [Team Slack channel] | 🔴 [NOT STARTED] |
| Broken AT compatibility alert (e.g., VoiceOver regression) | [e.g., BrowserStack Automate] | Weekly | [QA Lead email] | 🔴 [NOT STARTED] |

**Accessibility Score Baseline (set at launch):**

| Metric | Launch Score | Current Score | Target Score |
|--------|-------------|---------------|--------------|
| Lighthouse Accessibility | [X/100] | [Track here] | ≥ [90]/100 |
| Axe Critical Violations | [0] | [Track here] | 0 |
| Axe Serious Violations | [X] | [Track here] | 0 |

---

### 10.3 Assistive Technology Analytics

> 💡 **What to track:** These analytics tell you whether real users with disabilities are successfully using your product. Low completion rates for AT users = accessibility problems.

| Metric | Tracking Method | Baseline at Launch | Current Value | Target |
|--------|-----------------|-------------------|---------------|--------|
| % of sessions using screen reader (estimated via AT detection) | [e.g., Google Analytics custom event] | [X]% | [Track] | ≥ industry avg |
| % of sessions keyboard-only (no mouse events) | [e.g., GA4 event tracking] | [X]% | [Track] | |
| Task completion rate for keyboard-only users | [e.g., A/B comparison in analytics] | [X]% | [Track] | ≥ 90% |
| Task completion rate for AT users vs. non-AT users | [e.g., Hotjar / FullStory] | [X]% | [Track] | Within 10% of non-AT rate |
| # Accessibility complaints received | [e.g., Zendesk tag count] | 0 | [Track monthly] | 0 P1s |

---

### 10.4 Milestone Reviews — First 500 Customers

| Milestone | Customer Count | Review Actions | Date | Owner | Status |
|-----------|----------------|----------------|------|-------|--------|
| **30-Day Review** | ~[X] customers | • Review all AT analytics · Triage all accessibility feedback received · Fix any new P1/P2 issues found | [DATE] | Accessibility Lead | 🔴 [NOT STARTED] |
| **90-Day Review** | ~[X] customers | • Run full Axe + Lighthouse scan · Repeat 3 user testing sessions with disabled users · Update Accessibility Statement if needed | [DATE] | Accessibility Lead | 🔴 [NOT STARTED] |
| **500-Customer Review** | ~500 customers | • Commission third-party accessibility audit · Publish updated VPAT (if B2B) · Set next quarterly audit date · Review legal/compliance status | [DATE] | Accessibility Lead + PM | 🔴 [NOT STARTED] |

---

### 10.5 Quarterly Audit Schedule

| Quarter | Target Date | Audit Scope | Auditor | Status |
|---------|-------------|-------------|---------|--------|
| Q1 Post-Launch | [DATE] | Full WCAG 2.2 AA scan of all pages/flows | [Internal / External firm name] | 🔴 [NOT STARTED] |
| Q2 Post-Launch | [DATE] | Focus on new features shipped since Q1 | [Internal / External firm name] | 🔴 [NOT STARTED] |
| Q3 Post-Launch | [DATE] | Full re-audit + AT user testing session | [Internal / External firm name] | 🔴 [NOT STARTED] |
| Q4 Post-Launch | [DATE] | Annual comprehensive audit + compliance re-check | [External firm recommended] | 🔴 [NOT STARTED] |

---

## SECTION 11 — ISSUE TRACKER & SEVERITY RATING SYSTEM

> 📝 **Instructions:** Every accessibility issue found — whether by automated tools, manual testing, or user reports — must be logged here. **Do not fix an issue without logging it first.** This creates the audit trail that protects the company legally.

---

### 11.1 Severity Definitions (P1–P4)

| Priority | Name | Definition | Launch Impact | Fix Deadline |
|----------|------|------------|---------------|--------------|
| 🔴 **P1** | **Critical** | Prevents a user with a disability from completing a core task. Examples: keyboard trap, unlabelled login form, broken screen reader on checkout. | **LAUNCH BLOCKER** | Before launch / within 24h post-discovery |
| 🟠 **P2** | **Serious** | Significantly degrades the experience but a workaround exists. Examples: missing image alt text, poor contrast on non-critical text, error message not announced. | Launch allowed with documented plan | Within 14 days |
| 🟡 **P3** | **Moderate** | Minor barrier that affects some users in some situations. Examples: missing focus indicator on low-priority element, WCAG 2.2 only criteria, slightly insufficient spacing. | Launch allowed | Within 30 days |
| ⬜ **P4** | **Low** | Minor improvement that enhances experience but does not create a barrier. Examples: enhanced alt text, better reading level, added keyboard shortcut. | Launch allowed | Next planned release |

---

### 11.2 Issue Log

> 💡 **How to add a new issue:** Copy the empty row template and fill in every column. Never leave a column blank — write "Unknown" if you don't know yet.

| ID | Priority | Page / Component | Issue Description | WCAG Criterion | Found By | Found Date | Assigned To | Fix PR / Commit | Resolved Date | Status |
|----|----------|-----------------|-------------------|---------------|----------|-----------|-------------|-----------------|---------------|--------|
| A-001 | 🔴 P1 | [e.g., Login Page] | [e.g., Password field has no label — screen reader announces "edit text" with no context] | 1.3.1 (Info and Relationships), 4.1.2 (Name, Role, Value) | [e.g., NVDA manual test] | [DATE] | [Developer Name] | [Link to PR] | [DATE or OPEN] | 🔴 OPEN |
| A-002 | 🟠 P2 | [e.g., Dashboard Header] | [e.g., Navigation logo has no alt text] | 1.1.1 (Non-text Content) | [e.g., Axe-core CI] | [DATE] | [Developer Name] | [Link to PR] | [DATE or OPEN] | 🟢 CLOSED |
| A-003 | | | | | | | | | | |
| A-004 | | | | | | | | | | |

**Running Totals:**

| Priority | Open | Closed | Total |
|----------|------|--------|-------|
| 🔴 P1 Critical | [#] | [#] | [#] |
| 🟠 P2 Serious | [#] | [#] | [#] |
| 🟡 P3 Moderate | [#] | [#] | [#] |
| ⬜ P4 Low | [#] | [#] | [#] |

---

## SECTION 12 — LEGAL & COMPLIANCE RISK DOCUMENTATION

> 📝 **Instructions:** The **PM and Legal/Compliance** team fill this section. This is not legal advice — consult a qualified attorney for your specific situation.

---

### 12.1 Applicable Laws by Market

| Country / Region | Applicable Law | Enforcement Body | Risk if Non-Compliant | Notes |
|------------------|---------------|-----------------|----------------------|-------|
| **United States** | Americans with Disabilities Act (ADA) Title III | DOJ; Private litigation | Lawsuits, settlements, attorney fee awards (avg. $25K–$100K+ per case) | Web covered under ADA per DOJ 2024 rule |
| **European Union** | European Accessibility Act (EAA) — Directive 2019/882 | National enforcement authorities | Fines up to €[varies by member state]; market access ban | Enforceable from June 28, 2025 |
| **United Kingdom** | Equality Act 2010 + Public Sector Bodies Accessibility Regulations | Equality and Human Rights Commission | Discrimination claims, fines | |
| **Canada (Ontario)** | AODA — Integrated Accessibility Standards Regulation | AODA Directorate, Ontario | Fines up to $100,000/day for organizations | Applies to businesses with 20+ employees |
| **Australia** | Disability Discrimination Act 1992 | Australian Human Rights Commission | Complaints, investigations, settlements | |
| **[Add your market]** | [Law name] | [Body] | [Risk] | |

---

### 12.2 Legal Risk Assessment

| Risk Item | Likelihood | Impact | Mitigation |
|-----------|-----------|--------|------------|
| ADA demand letter / lawsuit | ☐ Low ☐ Medium ☐ High | ☐ Low ☐ Medium ☐ High | [e.g., WCAG 2.1 AA conformance; published Accessibility Statement; active feedback channel] |
| EAA non-compliance enforcement | ☐ Low ☐ Medium ☐ High | ☐ Low ☐ Medium ☐ High | [e.g., WCAG 2.2 AA conformance; EN 301 549 audit planned] |
| Enterprise B2B contract requirement (VPAT) | ☐ Low ☐ Medium ☐ High | ☐ Low ☐ Medium ☐ High | [e.g., VPAT 2.5 in progress, expected by [DATE]] |
| Healthcare-specific (Section 508 for HHS grants) | ☐ Low ☐ Medium ☐ High | ☐ Low ☐ Medium ☐ High | [e.g., Section 508 audit scheduled] |

---

### 12.3 Voluntary Product Accessibility Template (VPAT)

> 💡 **What is a VPAT?** A VPAT is a standardized document that enterprise customers — especially governments and large corporations — require from software vendors to prove accessibility compliance. If you're selling B2B, you'll need one.

| Item | Status | Notes |
|------|--------|-------|
| VPAT Version: 2.5 (WCAG 2.1 + Section 508 + EN 301 549) | ☐ Required  ☐ Not Required | |
| VPAT preparation started | ☐ Yes  ☐ No | Start Date: [DATE] |
| VPAT completed and reviewed | ☐ Yes  ☐ No | Completion Date: [DATE] |
| VPAT published / provided to customers | ☐ Yes  ☐ No | Location: [URL or "On request"] |
| VPAT next review date | [DATE — review at least annually] | |

---

### 12.4 Incident Response Plan

> 📝 **What to do if you receive an accessibility complaint, demand letter, or lawsuit:**

```
Step 1: [Within 24 hours] Notify: Legal team, PM, Accessibility Lead
Step 2: [Within 48 hours] Log the complaint in the Issue Tracker (Section 11) as P1
Step 3: [Within 72 hours] Investigate and reproduce the reported barrier
Step 4: [Within 5 business days] Provide a written response to the complainant with:
         - Acknowledgment of the issue
         - Your plan to fix it (with date)
         - Interim workaround (if available)
Step 5: Fix the issue per P1 timeline (before launch or within 24h)
Step 6: Notify complainant when fixed
Step 7: Update this document and the Issue Log

Legal Contact:    [Attorney name and contact information]
Accessibility Lead Contact:  [Name, email, phone]
```

---

## SECTION 13 — TOOLS & RESOURCES REFERENCE

> 📝 **Instructions:** This section is pre-filled. Add any project-specific tools your team uses.

---

### 13.1 Testing Tools

| Category | Tool | Free / Paid | What It Does | Link |
|----------|------|-------------|-------------|------|
| **Browser Extension** | Axe DevTools | Free (basic) / Paid | Instant WCAG scan in Chrome/Firefox during development | [deque.com/axe](https://www.deque.com/axe/) |
| **Browser Extension** | WAVE | Free | Visual accessibility feedback overlay | [wave.webaim.org](https://wave.webaim.org/) |
| **CI/CD Integration** | Axe-core (npm) | Free (OSS) | Programmatic WCAG testing in Playwright/Jest/Cypress | [github.com/dequelabs/axe-core](https://github.com/dequelabs/axe-core) |
| **Automated Audit** | Lighthouse CI | Free | Accessibility score in CI/CD pipelines | [github.com/GoogleChrome/lighthouse-ci](https://github.com/GoogleChrome/lighthouse-ci) |
| **Automated Audit** | Pa11y | Free (OSS) | CLI-based WCAG audit of URLs | [pa11y.org](https://pa11y.org/) |
| **Color Contrast** | WebAIM Contrast Checker | Free | Check any color pair for WCAG contrast ratio | [webaim.org/resources/contrastchecker](https://webaim.org/resources/contrastchecker/) |
| **Color Contrast** | Colour Contrast Analyser | Free | Desktop app for checking colors on screen | [tpgi.com/color-contrast-checker](https://www.tpgi.com/color-contrast-checker/) |
| **Screen Reader** | NVDA | Free | Screen reader for Windows | [nvaccess.org](https://www.nvaccess.org/) |
| **Screen Reader** | JAWS | Paid | Professional-grade Windows screen reader | [freedomscientific.com](https://www.freedomscientific.com/) |
| **Screen Reader** | VoiceOver | Free (built-in) | macOS and iOS screen reader | Built into Apple devices |
| **Screen Reader** | TalkBack | Free (built-in) | Android screen reader | Built into Android |
| **User Testing** | Fable | Paid | Testing with real disabled users | [makeitfable.com](https://makeitfable.com/) |
| **Seizure Check** | PEAT | Free | Check content for seizure risk | [trace.umd.edu/peat](https://trace.umd.edu/peat/) |
| **Reading Level** | Hemingway Editor | Free | Check reading level of text | [hemingwayapp.com](https://hemingwayapp.com/) |
| **Keyboard Testing** | Manual | Free | Unplug your mouse and navigate using Tab only | N/A |

---

### 13.2 Learning Resources

| Resource | Who It's For | Link |
|----------|-------------|------|
| WCAG 2.2 Quick Reference | All team members | [w3.org/WAI/WCAG22/quickref](https://www.w3.org/WAI/WCAG22/quickref/) |
| ARIA Authoring Practices Guide (APG) | Developers | [w3.org/WAI/ARIA/apg](https://www.w3.org/WAI/ARIA/apg/) |
| WebAIM Screen Reader User Survey | PMs, Designers | [webaim.org/projects/screenreadersurvey](https://webaim.org/projects/screenreadersurvey/) |
| Apple Human Interface Guidelines — Accessibility | iOS Developers | [developer.apple.com/design/human-interface-guidelines/accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility) |
| Android Accessibility — Developer Guide | Android Developers | [developer.android.com/guide/topics/ui/accessibility](https://developer.android.com/guide/topics/ui/accessibility) |
| Inclusive Design Principles | All team members | [inclusivedesignprinciples.org](https://inclusivedesignprinciples.org/) |
| A11y Project Checklist | QA / Developers | [a11yproject.com/checklist](https://www.a11yproject.com/checklist/) |
| Deque University (courses) | All team members | [dequeuniversity.com](https://dequeuniversity.com/) |
| UK Home Office Accessibility Posters | Designers | [github.com/UKHomeOffice/posters](https://github.com/UKHomeOffice/posters/) |

---

## SECTION 14 — DOCUMENT REVISION HISTORY

> 📝 **Instructions:** Every time this document is meaningfully changed, add a new row. "Meaningful change" means: adding or removing a checklist item, changing a sign-off, updating a test result, or changing a deadline.

| Version | Date | Changed By | Summary of Changes |
|---------|------|-----------|-------------------|
| 1.0.0 | [DATE] | [Name] | Initial document created from template |
| 1.0.1 | [DATE] | [Name] | [e.g., Added Section 4.2 AT support matrix; updated team directory] |
| 1.1.0 | [DATE] | [Name] | [e.g., Design phase checklist completed and signed off] |
| 1.2.0 | [DATE] | [Name] | [e.g., QA testing results entered; 3 P1 issues logged] |
| 2.0.0 | [DATE] | [Name] | [e.g., Launch gate signed off; post-launch monitoring activated] |

---

## SECTION 15 — QUICK REFERENCE CHEAT SHEET

> 💡 **Print this page and pin it to your team's wall (or pin it in Slack/Notion).**

---

```
┌─────────────────────────────────────────────────────────────────────┐
│               ♿  ACCESSIBILITY QUICK REFERENCE                     │
├──────────────────────────┬──────────────────────────────────────────┤
│  CONTRAST RATIOS         │  TOUCH TARGETS                          │
│  Normal text:  ≥ 4.5:1  │  Mobile (best): 44 × 44 px              │
│  Large text:   ≥ 3:1    │  Mobile (min):  24 × 24 px (WCAG 2.2)  │
│  UI elements:  ≥ 3:1    │  Space between: ≥ 8 px                  │
├──────────────────────────┼──────────────────────────────────────────┤
│  TEXT SIZE               │  SEVERITY                               │
│  Min body: 16 px         │  🔴 P1 = Launch Blocker                 │
│  Line height: 1.5×       │  🟠 P2 = Fix in 14 days                 │
│  Zoom to 200%: no loss   │  🟡 P3 = Fix in 30 days                 │
│  Zoom to 400%: reflow    │  ⬜ P4 = Next release                   │
├──────────────────────────┼──────────────────────────────────────────┤
│  EVERY IMAGE NEEDS alt=""│  EVERY FORM FIELD NEEDS <label>         │
│  (empty if decorative)   │  (placeholder ≠ label!)                 │
├──────────────────────────┼──────────────────────────────────────────┤
│  KEYBOARD: Tab → forward │  SCREEN READERS: NVDA, JAWS, VoiceOver  │
│  Shift+Tab → back        │  TalkBack (Android)                     │
│  Escape → close overlay  │  Test all critical flows!               │
├──────────────────────────┼──────────────────────────────────────────┤
│  NEVER:                  │  ALWAYS:                                │
│  ✗ outline: none         │  ✓ Visible focus ring                   │
│  ✗ user-scalable=no      │  ✓ Semantic HTML first                  │
│  ✗ Color alone = meaning │  ✓ One H1 per page                      │
│  ✗ div onclick           │  ✓ Test with keyboard only              │
└──────────────────────────┴──────────────────────────────────────────┘

Accessibility Lead: [NAME] — [EMAIL]
```

---

*This document is a living record. It grows with your product.*
*Last reviewed: [DATE] | Next scheduled review: [DATE]*
*Template Version 2.0.0 — AI-Driven Development Lifecycle Edition*
