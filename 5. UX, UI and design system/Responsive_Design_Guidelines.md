---
document: Responsive_Design_Guidelines
template_version: 1.0.0
location: /UX-UI-and-Design-System/Responsive_Design_Guidelines.md
project_name: "[FILL: your project name]"
owner: "[FILL: name of the person responsible]"
status: DRAFT            # DRAFT | IN_REVIEW | APPROVED | LOCKED
product_types: []        # pick any: web, ios, android, desktop
last_reviewed: "[FILL: YYYY-MM-DD]"
next_review: "[FILL: YYYY-MM-DD]"
standards: [WCAG-2.2-AA, WCAG-2.2-AAA-where-feasible, Core-Web-Vitals, Apple-HIG, Material-3]
approach: mobile-first
agent_rules: strict-never-guess
---

# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

**What is this file?**
It is the single place that explains how your product looks and behaves on every screen size: tiny phones, big phones, tablets, laptops, huge monitors, and folding devices. It also explains how to build, test, launch, and grow the product until your first **500 customers** are using it.

**Who is it for?**
- **Humans** (founders, designers, developers, testers, managers). You fill in the blanks.
- **AI agents** (coding assistants and other tools). They read this file and follow it exactly. They are not allowed to guess.

**Time needed:** about 2 hours for the first fill. Later updates take minutes.

## The 7 rules (simple version)

1. **Go top to bottom.** Do not skip around. Later parts depend on earlier ones.
2. **Find every `[FILL: ...]`.** That is a blank. Replace the whole thing, brackets included, with your answer.
3. **Look at the example** under each blank. It shows what a good answer looks like. Copy the style, not the words.
4. **Pick-one lists look like `☐`.** Change the one you choose to `☑`. Pick exactly one unless the text says "pick any".
5. **Sentence blanks look like `___`.** Write your answer on the line.
6. **Do not know the answer?** Write `[DECIDE BY: date, WHO decides]`. Never leave a blank empty and never invent an answer.
7. **Does this part not apply to you?** Write `N/A: [one-line reason]`. Do not delete the part. Deleting hides the decision from the team and from the AI agents.

## What the markers mean

| Marker | Meaning |
|---|---|
| `[FILL: ...]` | A blank you must answer |
| `☐` / `☑` | Unchecked / checked choice |
| `___` | A short blank inside a sentence |
| `> In plain words:` | A kid-friendly explanation of the part |
| `> Example:` | A filled-in sample. Do not copy it blindly. |
| `🛑 GATE` | A checkpoint. Do not move on until every box is checked. |
| `🤖 AGENT:` | A rule or prompt meant for an AI agent |
| `[DECIDE BY: ...]` | A decision postponed on purpose, with an owner and date |
| `N/A: reason` | This part does not apply, and here is why |

## How to know you are finished

Run this in a terminal from the folder containing this file:

```bash
grep -c "\[FILL" Responsive_Design_Guidelines.md
```

The answer should be `0`. Then fill in the **Completion Scorecard** (Part 16). You need 90 points or more before status can change to `APPROVED`.

## How to reuse this template for a new project

1. Copy this file into the new project's `UX-UI-and-Design-System` folder.
2. Change `project_name`, `owner`, and the dates at the top.
3. Tick the product types in Part 1.
4. Fill every blank. Do not delete parts. Mark non-applicable parts `N/A: reason`.
5. Never edit the template's rules (Part 0) for one project only. If a rule must change, record it in the Decision Log (Part 14) as a project-level exception, with a name and date.

---

# DOCUMENT CONTROL

| Field | Value |
|---|---|
| Project | [FILL: project name] |
| Owner | [FILL: name and role] |
| Reviewers | [FILL: names; at least one designer, one developer, one tester] |
| Approver | [FILL: the one person who can say "approved"] |
| Status | ☐ DRAFT ☐ IN_REVIEW ☐ APPROVED ☐ LOCKED |
| Template version used | 1.0.0 |
| Last reviewed | [FILL: YYYY-MM-DD] |

## Table of contents

0. AI Agent Rules and Guardrails
1. Project Snapshot
2. The AI-Driven Life Cycle (6 phases, at a glance)
3. Foundations: Approach, Breakpoints, Units
4. Layout: Grid, Spacing, Orientation, Safe Areas
5. Typography
6. Navigation Patterns
7. Components: How Each One Adapts
8. Touch, Mouse, Keyboard, and Other Inputs
9. Images, Video, and Icons
10. Forms, Tables, and Data-Heavy Screens
11. Accessibility (WCAG 2.2)
12. Performance Budgets (Core Web Vitals)
13. Device, Browser, and OS Support
14. Decision Log and Changelog
15. Testing and QA
16. Completion Scorecard
17. Phase-by-Phase Playbook (Discover → Grow to 500)
18. Staged Rollout to the First 500 Customers
19. Ready-to-Copy AI Prompts
20. Plain-English Glossary
21. Appendix: A Tiny Filled-In Example

---

# PART 0: AI AGENT RULES AND GUARDRAILS

> In plain words: This is the rulebook for robots. If a robot is not sure, it must stop and ask a human. It must never make something up.

**Strictness level for this project:** `STRICT: NEVER GUESS` (fixed by this template; see Document Control for exceptions).

## 0.1 The Never-Guess Protocol

🤖 AGENT: Follow these steps in order, every time.

1. **Read the whole file** before writing code, designs, or tests.
2. **Search for `[FILL`.** If any `[FILL` remains in a section you need, **stop**. Ask the human exactly which blank to complete. Do not continue on that part.
3. **Search for `[DECIDE BY`.** If the date has passed, tell the human. If it has not, work around the decision using only what is written. Do not choose for them.
4. **Never invent** a number, color, font, breakpoint, URL, device, metric target, or user count. If it is not in this file, it does not exist yet.
5. **If two sections disagree,** follow the **Source-of-Truth Order** below, then report the conflict.
6. **Explain every decision** by naming the section you used, for example "Part 3.2 says the smallest width is 320 px."
7. **Record assumptions.** If a human tells you to proceed with an unconfirmed value, write it in the Assumption Log (0.4) before using it.

## 0.2 Source-of-Truth Order (highest wins)

1. A written, dated instruction from the project **Approver** (Document Control)
2. This file (`Responsive_Design_Guidelines.md`)
3. The project's design tokens or design system files: [FILL: path or link to design tokens / design system]
4. The product requirements document: [FILL: path or link to PRD]
5. Platform guidelines (WCAG 2.2, Apple HIG, Material 3)
6. General best practice

## 0.3 What an AI agent MAY and MAY NOT do

| ✅ MAY | ❌ MAY NOT |
|---|---|
| Read this file and all linked files | Edit Part 0 of this file |
| Propose code, layouts, and tests that follow this file | Change a breakpoint, target size, or budget without a Decision Log entry |
| Run automated tests and report real results | Say "tests pass" without running them |
| Flag conflicts, gaps, and risks | Hide or "fix" a failing check by lowering its threshold |
| Ask the human clarifying questions | Fill in `[FILL]` blanks for the human without being asked |
| Add rows to the Decision Log (as "proposed") | Mark a Decision Log entry "approved" |
| Suggest alternatives, labeled "SUGGESTION" | Ship, publish, or roll out to users without a human's written go-ahead |

## 0.4 Assumption Log (agents and humans)

| # | Date | Assumption | Who allowed it | Evidence | Status (open / confirmed / rejected) |
|---|---|---|---|---|---|
| A-1 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

## 0.5 Agent "Definition of Done"

An agent may say a task is done only when every box is true:

- ☐ Every rule in this file that applies to the task was followed
- ☐ No `[FILL` remained in a section the task depends on
- ☐ The change was checked at **every breakpoint** listed in Part 3.2
- ☐ Automated accessibility and performance checks were **actually run** (Part 15)
- ☐ Real results (numbers, screenshots, logs) are attached or linked
- ☐ Anything not verified is listed as "NOT VERIFIED" in the report
- ☐ The Changelog (Part 14) has a new line

---

# PART 1: PROJECT SNAPSHOT

> In plain words: Tell us what you are building and for whom, so nobody has to guess.

## 1.1 What is this product?

**One sentence:** `[FILL: "___ helps ___ do ___"]`

> Example: "PlantPal helps busy people remember to water their plants."

**Who will use it?** `[FILL: describe your main users; age, job, where they use it]`

> Example: "Adults 25–45, mostly on phones, often on slow mobile data, sometimes one-handed."

## 1.2 Product types (pick any)

☐ **Web** (website, web app, dashboard, landing page)
☐ **iOS app**
☐ **Android app**
☐ **Desktop app** (Windows / macOS / Linux)

> The sections labeled 🌐 apply to Web, 📱 to iOS and Android, 🖥️ to Desktop. If you did not tick a type, mark its sections `N/A: not building this`.

## 1.3 Main devices your users actually use

`[FILL: list from real data (analytics, survey, interviews). If you have no data yet, write "NO DATA: assumed from [source], to be verified by [date]".]`

| Device group | Estimated share of users | Source of the number |
|---|---|---|
| Small phones (under 360 px wide) | [FILL: %] | [FILL] |
| Regular phones (360–599 px) | [FILL: %] | [FILL] |
| Large phones / small tablets (600–839 px) | [FILL: %] | [FILL] |
| Tablets, foldables unfolded (840–1199 px) | [FILL: %] | [FILL] |
| Laptops and desktops (1200+ px) | [FILL: %] | [FILL] |

## 1.4 Key goals for responsive design (pick the top 3)

☐ Everything works on a small phone
☐ Looks great on large monitors
☐ Fast on slow networks
☐ Works with screen readers and keyboards
☐ Same brand feel on every device
☐ Works offline or on poor connections
☐ Other: [FILL]

## 1.5 Things we will NOT support (be honest; it saves money)

`[FILL: list devices, browsers, or sizes you will not support, with a reason]`

> Example: "Internet Explorer 11: under 0.1% of users; high cost."

---

# PART 2: THE AI-DRIVEN LIFE CYCLE (AT A GLANCE)

> In plain words: Building a product is like building a house. You plan, draw, build, inspect, open the doors, and then make sure the first 500 guests are happy. Each step has a checkpoint (🛑 GATE) so mistakes get caught early.

| Phase | Name | Goal | Human owner | AI agent's job | Exit gate |
|---|---|---|---|---|---|
| 1 | **Discover** | Understand users, devices, and limits | [FILL] | Summarize research; list gaps | G1 |
| 2 | **Design** | Draw layouts for every size class | [FILL] | Draft layouts and tokens from this file | G2 |
| 3 | **Build** | Write the code | [FILL] | Generate code that follows this file | G3 |
| 4 | **Test** | Prove it works everywhere | [FILL] | Run tests, report results honestly | G4 |
| 5 | **Launch** | Release carefully | [FILL] | Prepare checklists; never deploy alone | G5 |
| 6 | **Grow to 500** | Reach and keep your first 500 customers | [FILL] | Watch metrics; summarize feedback | G6 |

**Project dates:**

| Phase | Planned start | Planned end | Actual end |
|---|---|---|---|
| 1 Discover | [FILL: YYYY-MM-DD] | [FILL] | [FILL] |
| 2 Design | [FILL] | [FILL] | [FILL] |
| 3 Build | [FILL] | [FILL] | [FILL] |
| 4 Test | [FILL] | [FILL] | [FILL] |
| 5 Launch | [FILL] | [FILL] | [FILL] |
| 6 Grow to 500 | [FILL] | [FILL] | [FILL] |

The full details for each phase are in **Part 17**. Staged rollout rules are in **Part 18**.

---

# PART 3: FOUNDATIONS: APPROACH, BREAKPOINTS, UNITS

## 3.1 Our approach

> In plain words: "Mobile-first" means we design for the smallest screen first, then add extras as the screen gets bigger. It is easier to add than to squeeze.

**Default for this template:** ☑ **Mobile-first** (design the smallest layout first, then enhance upward).

Exception for this project? ☐ No exception ☐ Yes, we use ☐ Desktop-first ☐ Content-first (container queries): reason: `[FILL: reason + who approved + date]`

## 3.2 Breakpoints (the sizes where the layout changes)

> In plain words: A breakpoint is a screen width where the layout rearranges itself, like a classroom changing from one long row of desks to several groups.

The template uses the **same five size classes for web, iOS, Android, and desktop**, so designers and developers talk about one set of sizes. The boundaries follow the Material 3 / Android window size classes.

| Size class | Width starts at | Typical devices (examples only; sizes decide, not devices) | Columns | Side margin | Gutter |
|---|---|---|---|---|---|
| **Compact** | 0 (design for 320 as the smallest) | Phones, portrait | 4 | [FILL: 16] px | [FILL: 16] px |
| **Medium** | 600 | Large phones landscape, small tablets, some foldables | 8 | [FILL: 24] px | [FILL: 24] px |
| **Expanded** | 840 | Tablets, unfolded foldables, small laptops | 12 | [FILL: 24] px | [FILL: 24] px |
| **Large** | 1200 | Laptops, desktops | 12 | [FILL: 32] px | [FILL: 24] px |
| **Extra-large** | 1600 | Big monitors | 12 | [FILL: 32] px | [FILL: 24] px |

> The numbers in `[FILL]` above are suggested starting values from common design systems. Confirm or change each one. If you change a **width boundary**, write the reason in the Decision Log (Part 14).

**Smallest width we guarantee to work:** `___ px` (WCAG 2.2 requires content to work without two-direction scrolling at **320 CSS px** wide, so never go above 320).

**Largest content width (so text lines don't stretch across a huge monitor):** `___ px`

> Example: "1280 px; centered; extra space becomes margin."

**Height classes (needed for landscape phones and foldables):**

| Height class | Height starts at | Rule |
|---|---|---|
| Compact | 0 | Two-pane layouts are NOT allowed; use one pane |
| Medium | 480 | [FILL: rule] |
| Expanded | 900 | [FILL: rule] |

🤖 AGENT: Check **both** width and height. A phone turned sideways can be Medium width but Compact height.

**Rule for deciding the class:** use the **window or container size that is actually available**, never the device name. Never write `isTablet` or `isPhone` logic.

## 3.3 When the layout is allowed to change (pick any)

☐ At viewport breakpoints (the whole window)
☐ At container breakpoints (a card changes based on the space it sits in) 🌐
☐ Fluid scaling between breakpoints (sizes grow smoothly)

`[FILL: one sentence on which one you use for page layout, and which for components]`

> Example: "Page layout changes at viewport breakpoints. Cards, tables, and sidebars use container queries."

## 3.4 Required setup per platform

🌐 **Web**
- ☐ Viewport tag is present: `<meta name="viewport" content="width=device-width, initial-scale=1">`
- ☐ Zooming is **not** disabled (do not use `user-scalable=no` or `maximum-scale=1`)
- ☐ Layout uses relative units, not fixed pixel widths for containers
- ☐ Safe-area insets are used on notched devices: `env(safe-area-inset-*)`
- ☐ Dynamic viewport units (`dvh`, `svh`, `lvh`) are used where the mobile browser toolbar changes height

📱 **iOS:** ☐ Auto Layout / SwiftUI adaptive layouts ☐ Safe area respected ☐ Dynamic Type supported ☐ iPad multitasking sizes tested

📱 **Android:** ☐ Window size classes used ☐ Edge-to-edge with insets handled ☐ Font scaling supported ☐ Foldable postures and multi-window tested

🖥️ **Desktop:** ☐ Window can be resized freely ☐ Minimum window size set to `___ × ___` ☐ Display scaling (125%, 150%, 200%) tested

## 3.5 Units (the measuring sticks)

| Use this | For | Not this |
|---|---|---|
| `rem` (🌐) / `sp` (Android) / Dynamic Type (iOS) | Text sizes | Fixed `px` for body text |
| `%`, `fr`, `minmax()`, flex | Widths of layout areas | Fixed `px` widths on containers |
| `px` / `dp` / `pt` | Borders, hairlines, small fixed icons | Page-level widths |
| `clamp()` | Fluid type and spacing between a min and a max | Many separate breakpoints for tiny size changes |

**Our spacing scale (base unit):** `___ px` (commonly 4 or 8)

> Example: "Base 4 px. Steps: 4, 8, 12, 16, 24, 32, 48, 64."

**Our scale steps:** `[FILL: list]`

---

# PART 4: LAYOUT: GRID, SPACING, ORIENTATION, SAFE AREAS

## 4.1 Page layout patterns per size class

> In plain words: Say what each page looks like at each size. Words are enough. Sketches are even better.

| Page / screen | Compact | Medium | Expanded | Large / Extra-large |
|---|---|---|---|---|
| [FILL: e.g., Home] | [FILL: e.g., 1 column] | [FILL] | [FILL] | [FILL] |
| [FILL: e.g., Dashboard] | [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL: e.g., Settings] | [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL: add rows for every main screen] | | | | |

> Example row: Home | 1 column, cards stacked | 2 columns | 3 columns + side filter | 3 columns + side filter, max width 1280 px

**Canonical layouts we use (pick any):**
☐ **List-detail** (a list next to its details; stacks into two screens on Compact)
☐ **Supporting pane** (main content plus a helper panel)
☐ **Feed** (cards in a flowing grid)
☐ **Single column** (reading or forms)
☐ **Other:** [FILL]

## 4.2 Content priority (what survives on the smallest screen)

`[FILL: list the 5 most important things users do, in order]`

1. [FILL]
2. [FILL]
3. [FILL]
4. [FILL]
5. [FILL]

**Rule:** Anything *not* on this list can be hidden behind a menu on Compact. Nothing on the list may be hidden.

🤖 AGENT: Never remove content or features on small screens unless this list says it is lower priority. Hide = move behind a clear control. Never delete.

## 4.3 Orientation

- ☐ Both portrait and landscape are supported (**required** for WCAG 2.2 unless essential)
- Exceptions (rare; must be essential, such as a piano app): `[FILL: or "None"]`

## 4.4 Foldables and multi-window

☐ We support foldable devices ☐ We do not (reason: [FILL])

If supported: `[FILL: what happens when the screen unfolds, folds, or is split]`

> Example: "Unfolding moves us from Compact to Expanded. The list-detail layout appears with no reload and keeps the user's place."

## 4.5 Safe areas and system bars

☐ Content never hides under notches, camera cutouts, the home indicator, or system bars
☐ Backgrounds may extend edge-to-edge; **interactive items may not**

## 4.6 Spacing rules

| Thing | Compact | Medium+ |
|---|---|---|
| Space between sections | [FILL] | [FILL] |
| Space inside cards (padding) | [FILL] | [FILL] |
| Space between tappable items | at least [FILL] | at least [FILL] |

## 4.7 Scrolling rules

- **No two-direction scrolling** for normal content at 320 px wide (WCAG 1.4.10). Allowed exceptions: maps, big data tables, images that need two dimensions, code blocks, toolbars. List yours: `[FILL]`
- Sticky headers/footers may cover at most `___ %` of screen height on Compact.
- ☐ Scroll position is kept when rotating or resizing.

---

# PART 5: TYPOGRAPHY

> In plain words: Letters must be big enough to read, and lines must not be too long or too short.

## 5.1 Fonts

| Role | Font family | Fallback fonts |
|---|---|---|
| Headings | [FILL] | [FILL] |
| Body | [FILL] | [FILL] |
| Code / numbers (optional) | [FILL] | [FILL] |

## 5.2 Type scale

| Style | Compact size | Large size | Line height | Weight |
|---|---|---|---|---|
| Display / Hero | [FILL] | [FILL] | [FILL] | [FILL] |
| Heading 1 | [FILL] | [FILL] | [FILL] | [FILL] |
| Heading 2 | [FILL] | [FILL] | [FILL] | [FILL] |
| Heading 3 | [FILL] | [FILL] | [FILL] | [FILL] |
| **Body (the most important row)** | at least **16 px** (🌐) | [FILL] | 1.4 to 1.6 | [FILL] |
| Small / caption | [FILL: not below 12 px] | [FILL] | [FILL] | [FILL] |

## 5.3 Rules

- **Body text at least 16 px / 16 sp / 17 pt** on Compact. (Recommended default; change only with a Decision Log entry.)
- **Line length:** about **45–75 characters** per line for reading text.
- Text must stay readable at **200% zoom/font size** without cut-off or overlap (WCAG 1.4.4).
- Text spacing must be adjustable without breaking layout (WCAG 1.4.12): line height 1.5×, paragraph spacing 2×, letter spacing 0.12×, word spacing 0.16×.
- **Never** fix the height of a box that contains text. Let it grow.
- Long words, emails, and URLs must wrap or truncate with a way to see the full text.
- ☐ Fluid type is used (`clamp()`): `[FILL: min size, preferred, max size]`

## 5.4 Text and background colors (contrast)

| Text type | WCAG 2.2 AA (**required**) | AAA (**where feasible**) |
|---|---|---|
| Normal text | 4.5 : 1 | 7 : 1 |
| Large text (24 px+, or 18.66 px+ bold) | 3 : 1 | 4.5 : 1 |
| Icons, input borders, focus rings | 3 : 1 | 3 : 1 |

Where we aim for AAA: `[FILL: e.g., "body text and all error messages"]`

---

# PART 6: NAVIGATION PATTERNS

> In plain words: Menus must fit the screen. A phone has thumbs near the bottom; a big monitor has room on the side.

| Size class | Primary navigation pattern (pick one per column) | Secondary navigation |
|---|---|---|
| Compact | ☐ Bottom bar ☐ Top bar + menu button ☐ Drawer | [FILL] |
| Medium | ☐ Navigation rail ☐ Bottom bar ☐ Drawer | [FILL] |
| Expanded | ☐ Navigation rail ☐ Permanent side menu | [FILL] |
| Large / Extra-large | ☐ Permanent side menu ☐ Top bar | [FILL] |

**Rules:**
- Bottom bar holds **3 to 5** items. More than 5 → "More" menu. Final count: `___`
- Same destinations and **same order** at every size.
- The current location is always visible and not shown by color alone.
- Back behavior: `[FILL: what Back does at each size]`
- Keyboard users can skip to main content in **one** keypress (🌐 skip link).
- Menus opened by tap must also open by keyboard.

---

# PART 7: COMPONENTS: HOW EACH ONE ADAPTS

> In plain words: Every building block (button, card, table, popup) needs instructions for each screen size. If you don't write them, the developer or the AI will guess.

Fill one row per component your product uses. Add rows as needed. Delete none.

| Component | Compact | Medium | Expanded+ | Notes / special rules |
|---|---|---|---|---|
| Button | [FILL: e.g., full width] | [FILL] | [FILL] | [FILL] |
| Text input | [FILL] | [FILL] | [FILL] | [FILL] |
| Card | [FILL] | [FILL] | [FILL] | [FILL] |
| Data table | [FILL: e.g., becomes a card list] | [FILL] | [FILL] | [FILL] |
| Modal / dialog | [FILL: e.g., full-screen sheet] | [FILL] | [FILL: centered, max __ px] | [FILL] |
| Dropdown / select | [FILL] | [FILL] | [FILL] | [FILL] |
| Tabs | [FILL] | [FILL] | [FILL] | [FILL] |
| Toast / alert | [FILL] | [FILL] | [FILL] | [FILL] |
| Search | [FILL] | [FILL] | [FILL] | [FILL] |
| Footer | [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL: your own] | | | | |

🤖 AGENT: If a component is used in the product but missing from this table, **stop and ask** for its row. Do not invent its responsive behavior.

---

# PART 8: TOUCH, MOUSE, KEYBOARD, AND OTHER INPUTS

> In plain words: Fingers are bigger than mouse arrows. Buttons must be big enough to hit, and everything must work without a mouse.

## 8.1 Target size (how big a tappable thing must be)

| Rule | Size | Source | Our setting |
|---|---|---|---|
| **Minimum, never smaller** (WCAG 2.2 AA, SC 2.5.8) | 24 × 24 CSS px, or enough spacing around smaller targets | WCAG 2.2 | **Required** |
| Apple recommendation | 44 × 44 pt | Apple HIG | ☐ Use on iOS |
| Material recommendation | 48 × 48 dp | Material 3 | ☐ Use on Android |
| AAA enhanced (SC 2.5.5) | 44 × 44 CSS px | WCAG 2.2 | ☐ Use where feasible |

**Our default for touch targets on Compact and Medium:** `___ × ___ px` (recommended: **at least 44 × 44**)
**Space between neighboring targets:** at least `___ px` (recommended: 8)

Inline links inside a sentence are exempt from the minimum size.

## 8.2 Thumb reach

`[FILL: where the main action button lives on Compact]`

> Example: "Primary action sits in the bottom third of the screen, in reach of one thumb."

## 8.3 Input methods we support (pick any)

☐ Touch ☐ Mouse ☐ Keyboard ☐ Stylus ☐ Voice control ☐ Screen reader ☐ Game controller / TV remote ☐ Switch access

## 8.4 Rules

- Every action available by pointer is available by **keyboard** (Tab, Enter, Space, Esc, arrow keys).
- **Visible focus indicator** on everything focusable, 3:1 contrast, never removed.
- Hover is a **bonus, never the only way** to see information (touch has no hover).
- Complex gestures (pinch, multi-finger swipe, drag) always have a **single-tap alternative** (WCAG 2.5.1, 2.5.7).
- Drag-and-drop always has a non-drag alternative.
- Don't trigger actions on touch-down; use touch-up so people can slide away to cancel.
- ☐ Respect `prefers-reduced-motion` and the platform "reduce motion" setting.

---

# PART 9: IMAGES, VIDEO, AND ICONS

> In plain words: Big pictures on a small phone waste data and slow everything down. Give each screen the right size of picture.

🌐 **Web rules**
- ☐ Responsive images (`srcset` and `sizes`, or `<picture>`) are used for photos
- ☐ Every image has **width and height** (or aspect ratio) set to prevent layout jumps
- ☐ Images below the first screen use `loading="lazy"`; the main (hero) image does **not**
- ☐ Modern formats with fallback: `[FILL: e.g., AVIF, WebP, JPEG]`
- ☐ Vector (SVG) for logos and icons

**Image widths we export:** `[FILL: e.g., 320, 640, 960, 1280, 1920]`
**Maximum file size per image on Compact:** `___ KB`
**Maximum total image weight on first screen:** `___ KB`

📱 **Native:** provide @1x/@2x/@3x (iOS) and density buckets or vector assets (Android). `[FILL: asset pipeline]`

**Rules for all products**
- Every meaningful image has alt text; decorative images are marked decorative.
- Text is **never** baked into an image (it won't scale or translate).
- Videos: don't autoplay with sound; give controls; provide captions; choose a lower quality on slow networks. `[FILL: video rules]`
- Image **cropping** per size class: `[FILL: e.g., "hero is 4:5 on Compact, 16:9 on Large; focal point kept in frame"]`

---

# PART 10: FORMS, TABLES, AND DATA-HEAVY SCREENS

## 10.1 Forms

- ☐ One column on Compact; multi-column only from `[FILL: size class]`
- ☐ Labels are visible and always above or beside the field, never only inside it as placeholder text
- ☐ Right keyboard type per field (`inputmode`, `type="email"`, number pad, etc.)
- ☐ Autocomplete attributes are set (`autocomplete="email"`, etc.)
- ☐ Errors are shown **next to the field** in text, not by color alone, and a summary is given at the top for long forms
- ☐ The on-screen keyboard never hides the active field or the submit button
- ☐ Users never have to re-type information they already gave (WCAG 3.3.7)
- ☐ Submit button is reachable without extra scrolling after the last field

## 10.2 Tables

Pick one approach **per table type**:

| Table | On Compact | Why |
|---|---|---|
| [FILL: name] | ☐ Cards ☐ Horizontal scroll with sticky first column ☐ Hide low-priority columns ☐ Other | [FILL] |

Columns that are **never** hidden: `[FILL]`

## 10.3 Charts and dashboards

- Charts resize to container width; text inside charts stays at least `___ px`.
- On Compact, show `[FILL: e.g., a simplified version or a summary number plus "see details"]`.
- Information is never carried by color alone; add labels, patterns, or icons.

## 10.4 Long content (articles, docs)

`[FILL: table of contents behavior, code block behavior, image captions]`

---

# PART 11: ACCESSIBILITY (WCAG 2.2)

> In plain words: Everyone should be able to use your product: people who can't see well, can't use a mouse, have shaky hands, or use a screen reader. Responsive design and accessibility are best friends.

**Target level:** ☑ **WCAG 2.2 Level AA is required.** ☐ We also target **AAA** for these items: `[FILL: list, or "none yet"]`

## 11.1 Responsive-relevant checks

| # | Check | WCAG | Level | Pass? |
|---|---|---|---|---|
| 1 | Content works at **320 × 256 CSS px** (equal to 400% zoom on a 1280 × 1024 window) with no two-direction scrolling | 1.4.10 Reflow | AA | ☐ |
| 2 | Text can be enlarged to **200%** without loss of content or function | 1.4.4 Resize Text | AA | ☐ |
| 3 | Text spacing can be changed without breakage | 1.4.12 | AA | ☐ |
| 4 | Both portrait and landscape work | 1.3.4 Orientation | AA | ☐ |
| 5 | Targets are at least **24 × 24 CSS px** (or spaced) | 2.5.8 Target Size (Minimum) | AA | ☐ |
| 6 | Targets are **44 × 44** where feasible | 2.5.5 Target Size (Enhanced) | AAA | ☐ |
| 7 | Content on hover or focus is dismissible, hoverable, persistent | 1.4.13 | AA | ☐ |
| 8 | Focus is never hidden behind sticky headers/footers | 2.4.11 Focus Not Obscured (Minimum) | AA | ☐ |
| 9 | Gestures have simple alternatives; dragging has alternatives | 2.5.1, 2.5.7 | A / AA | ☐ |
| 10 | Contrast: text 4.5:1 (3:1 large); UI parts 3:1 | 1.4.3, 1.4.11 | AA | ☐ |
| 11 | Reading order and focus order stay logical when the layout reorders | 1.3.2, 2.4.3 | A | ☐ |
| 12 | Page titles, headings, and landmarks are correct at every size | 2.4.2, 1.3.1 | A | ☐ |
| 13 | Reduced motion is respected | 2.3.3 (AAA) / best practice | AAA | ☐ |
| 14 | Help and contact info is in the same place on every page | 3.2.6 | A | ☐ |

🤖 AGENT: Visual order and reading/tab order must match. Never reorder with CSS `order` or absolute positioning in a way that breaks the tab sequence.

## 11.2 Assistive tech we test with

| Platform | Tool | Tester | Date |
|---|---|---|---|
| iOS | VoiceOver | [FILL] | [FILL] |
| Android | TalkBack | [FILL] | [FILL] |
| Windows | NVDA or Narrator | [FILL] | [FILL] |
| macOS | VoiceOver | [FILL] | [FILL] |
| All | Keyboard only | [FILL] | [FILL] |
| All | 200% text size and 400% zoom | [FILL] | [FILL] |

---

# PART 12: PERFORMANCE BUDGETS (CORE WEB VITALS)

> In plain words: A page that loads slowly or jumps around makes people leave. We set speed limits and don't break them.

## 12.1 Targets (Google "good" thresholds, measured at the 75th percentile of real users)

| Metric | What it measures | Good | Needs work | Poor |
|---|---|---|---|---|
| **LCP** (Largest Contentful Paint) | When the main content shows up | ≤ 2.5 s | 2.5–4.0 s | > 4.0 s |
| **INP** (Interaction to Next Paint) | How fast the page reacts to taps and clicks | ≤ 200 ms | 200–500 ms | > 500 ms |
| **CLS** (Cumulative Layout Shift) | How much things jump around | ≤ 0.1 | 0.1–0.25 | > 0.25 |

*Thresholds were checked against current sources in October 2026. FID no longer exists; INP replaced it in 2024. Re-check before each major release.*

## 12.2 Our budgets per device class

| Device class | LCP target | INP target | CLS target | Max page weight (first load) | Max JavaScript |
|---|---|---|---|---|---|
| Compact on slow 4G / mid-range phone | [FILL: ≤ 2.5 s] | [FILL: ≤ 200 ms] | [FILL: ≤ 0.1] | [FILL] KB | [FILL] KB |
| Medium/Expanded | [FILL] | [FILL] | [FILL] | [FILL] KB | [FILL] KB |
| Large/Extra-large on broadband | [FILL] | [FILL] | [FILL] | [FILL] KB | [FILL] KB |

**Test device and network profile used to measure "slow":** `[FILL: e.g., mid-range Android phone, Slow 4G throttling]`

## 12.3 Responsive performance rules

- Don't download desktop-size assets on phones.
- Reserve space for images, ads, embeds, and late-loading content (prevents CLS).
- Load the main (LCP) image early; lazy-load the rest.
- Use system fonts or `font-display: swap/optional`, and preload only critical fonts.
- Break up long tasks; keep taps responding within the INP budget.
- 📱 Native: `[FILL: app launch time target, frame rate target, memory limit]`

## 12.4 Real-user measurement when you have few users

With under about 500 users, public datasets such as CrUX often have **no data** for your site. So:

- ☐ We collect our own real-user data (for example, the open-source `web-vitals` library or equivalent): `[FILL: tool name]`
- ☐ Every number is reported **with its sample size** ("LCP p75 = 2.1 s from n = 38 visits")
- ☐ We don't call a metric "passing" if n is below `___` (recommended: 30 per device class)

---

# PART 13: DEVICE, BROWSER, AND OS SUPPORT

> In plain words: Choose exactly which devices and software you promise to support, so testers know what to check.

## 13.1 Support policy

| Level | Meaning |
|---|---|
| **A: Fully supported** | Everything works and looks right. Bugs are fixed quickly. |
| **B: Works** | Everything works; small visual differences are OK. |
| **C: Not supported** | We don't test or fix. |

## 13.2 Matrix (fill it with real analytics where possible)

🌐 **Browsers**

| Browser | Minimum version | Level | Source of decision |
|---|---|---|---|
| Chrome (desktop + Android) | [FILL] | [FILL: A/B/C] | [FILL] |
| Safari (macOS + iOS) | [FILL] | [FILL] | [FILL] |
| Firefox | [FILL] | [FILL] | [FILL] |
| Edge | [FILL] | [FILL] | [FILL] |
| Samsung Internet | [FILL] | [FILL] | [FILL] |
| Other: [FILL] | [FILL] | [FILL] | [FILL] |

📱 **Mobile OS**

| OS | Minimum version | Level |
|---|---|---|
| iOS / iPadOS | [FILL] | [FILL] |
| Android | [FILL] | [FILL] |

🖥️ **Desktop OS**

| OS | Minimum version | Level |
|---|---|---|
| Windows | [FILL] | [FILL] |
| macOS | [FILL] | [FILL] |
| Linux | [FILL] | [FILL] |

## 13.3 Required real-device test set

Test on real devices, not only emulators. List at least one device per row.

| Slot | Device (exact model) | OS version | Owner of device | Notes |
|---|---|---|---|---|
| Smallest phone | [FILL] | [FILL] | [FILL] | [FILL] |
| Common phone | [FILL] | [FILL] | [FILL] | [FILL] |
| Largest phone | [FILL] | [FILL] | [FILL] | [FILL] |
| Low-end phone (slow) | [FILL] | [FILL] | [FILL] | [FILL] |
| Tablet | [FILL] | [FILL] | [FILL] | [FILL] |
| Foldable (if supported) | [FILL] | [FILL] | [FILL] | [FILL] |
| Laptop | [FILL] | [FILL] | [FILL] | [FILL] |
| Big monitor | [FILL] | [FILL] | [FILL] | [FILL] |

## 13.4 Other conditions to cover (pick any you support)

☐ Dark mode ☐ High-contrast mode ☐ Right-to-left languages (Arabic, Hebrew) ☐ Long translated text (German, Finnish) ☐ Slow or offline network ☐ Data saver mode ☐ Large system font ☐ Reduced motion

`[FILL: languages supported at launch]`

---

# PART 14: DECISION LOG AND CHANGELOG

> In plain words: Write down *why* you chose something. Future you and the AI will thank you.

## 14.1 Decision Log

| ID | Date | Decision | Why | Alternatives rejected | Decided by | Affects sections | Status |
|---|---|---|---|---|---|---|---|
| D-001 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | ☐ Proposed ☐ Approved ☐ Replaced |
| D-002 | | | | | | | |

**Rule:** An AI agent may add a row with status "Proposed." Only a human **Approver** may change it to "Approved."

## 14.2 Changelog

| Version | Date | Author | What changed | Sections |
|---|---|---|---|---|
| 0.1.0 | [FILL] | [FILL] | First draft from template 1.0.0 | All |

Versioning: `MAJOR.MINOR.PATCH`. MAJOR = a rule changed. MINOR = a section added or filled. PATCH = typo or clarification.

---

# PART 15: TESTING AND QA

> In plain words: Don't say "it works." Prove it, on real devices, with notes anybody can read.

## 15.1 Test types

| Test | What it checks | Tool we use | Who runs it | When |
|---|---|---|---|---|
| Visual check at every breakpoint | Layout at **319/320, 359, 599, 600, 839, 840, 1199, 1200, 1599, 1600 px** (just below and at each boundary) | [FILL] | [FILL] | Every change |
| Real-device test | Touch, keyboard, safe areas | [FILL] | [FILL] | Before each release |
| Accessibility, automated | Contrast, labels, target size | [FILL: e.g., axe, Lighthouse] | [FILL] | Every pull request |
| Accessibility, manual | Screen reader, keyboard, zoom | [FILL] | [FILL] | Before each release |
| Performance | LCP, INP, CLS, weight | [FILL: e.g., Lighthouse CI, real-user monitoring] | [FILL] | Every pull request + live |
| Orientation / resize | Rotate, split screen, fold/unfold | [FILL] | [FILL] | Before each release |
| Text zoom | 200% and 400% | [FILL] | [FILL] | Before each release |
| Cross-browser | Matrix in Part 13 | [FILL] | [FILL] | Before each release |
| Slow network | Throttled network | [FILL] | [FILL] | Before each release |

## 15.2 Severity levels

| Level | Meaning | Example | Fix deadline |
|---|---|---|---|
| **P0 Blocker** | Can't use a main feature, or data loss | Checkout button off-screen on common phones | [FILL: e.g., same day] |
| **P1 Major** | Feature works badly | Text overlaps at 200% zoom | [FILL: e.g., 3 days] |
| **P2 Minor** | Looks off, still usable | 4 px misalignment at one size | [FILL: e.g., next sprint] |
| **P3 Polish** | Nice to have | Better image crop | [FILL: backlog] |

## 15.3 Responsive QA checklist (run per screen)

- ☐ No horizontal scroll at 320 px (except allowed exceptions in 4.7)
- ☐ Nothing overlaps, is cut off, or hidden unexpectedly
- ☐ Layout switches correctly at each boundary
- ☐ All content on the Priority list (4.2) is reachable on Compact
- ☐ Tap targets meet Part 8 sizes
- ☐ Text is readable at 200%
- ☐ Rotating the device keeps state
- ☐ Keyboard shows no hidden fields or buttons
- ☐ Focus order is logical; focus is visible
- ☐ Images are the right size and aren't blurry or huge
- ☐ No layout jump during load
- ☐ Looks right in dark mode / high contrast (if supported)
- ☐ Long text (translations) doesn't break the layout
- ☐ Works on slow network

## 15.4 Bug report template (copy for each bug)

```
Title:
Severity (P0–P3):
Screen / feature:
Device + OS + browser/app version:
Window size or size class:
Orientation / zoom / font size:
Steps to reproduce:
What I expected:
What happened:
Screenshot or video:
Related section of this guide:
```

---

# PART 16: COMPLETION SCORECARD

> In plain words: A score that tells you if this document is ready. Be honest.

| # | Question | Points | Yes? |
|---|---|---|---|
| 1 | No `[FILL` remain (`grep -c` returns 0) | 15 | ☐ |
| 2 | Every `[DECIDE BY]` has an owner and a future date | 5 | ☐ |
| 3 | Breakpoints confirmed with the designer **and** developer | 8 | ☐ |
| 4 | Content Priority list (4.2) written | 6 | ☐ |
| 5 | Every component in the product has a row in Part 7 | 8 | ☐ |
| 6 | Touch target sizes set (Part 8) | 5 | ☐ |
| 7 | Accessibility checks assigned to owners (Part 11) | 8 | ☐ |
| 8 | Performance budgets set for every device class (Part 12) | 8 | ☐ |
| 9 | Support matrix based on data, or marked "NO DATA" with a date to verify | 6 | ☐ |
| 10 | Real-device list filled with exact models | 6 | ☐ |
| 11 | Testing owners and tools named (Part 15) | 6 | ☐ |
| 12 | All 6 lifecycle phases have owners and dates (Part 2) | 5 | ☐ |
| 13 | Rollout stages and rollback rules filled (Part 18) | 8 | ☐ |
| 14 | A second person reviewed this file | 4 | ☐ |
| 15 | Approver named and has signed off | 2 | ☐ |
| | **Total** | **100** | **Score: ___** |

**Result:** 90–100 ✅ ready to approve. 70–89 ⚠️ close; fix the missing items. Under 70 ❌ not ready; do not start building from it.

---

# PART 17: PHASE-BY-PHASE PLAYBOOK (DISCOVER → GROW TO 500)

> In plain words: What to do, who does it, and what proves you are done, for each of the six phases.

Each phase has: **Tasks**, **Outputs**, **AI agent role**, and a **🛑 GATE**.

## PHASE 1: DISCOVER

**Goal:** Know your users, devices, and limits before drawing anything.

| ☐ | Task | Owner | Output |
|---|---|---|---|
| ☐ | Interview or survey at least `___` target users (recommended: 5+) about their devices and habits | [FILL] | Notes file |
| ☐ | Fill Part 1 (Project Snapshot) with real data | [FILL] | Part 1 complete |
| ☐ | Study 3 competitors on phone, tablet, and desktop | [FILL] | Screenshots + notes |
| ☐ | Write the Content Priority list (4.2) | [FILL] | Part 4.2 |
| ☐ | Choose support levels (Part 13) | [FILL] | Part 13 |
| ☐ | List accessibility needs of your users | [FILL] | Part 11 notes |

🤖 AGENT: Summarize research. List **gaps** instead of filling them. Label every statement "from data" or "assumed."

**🛑 GATE G1 (all must be true):**
☐ Part 1 and Part 13 have no `[FILL` ☐ Priority list approved ☐ Top 3 goals chosen ☐ Approver signed

## PHASE 2: DESIGN

**Goal:** Draw every important screen at every size class.

| ☐ | Task | Owner | Output |
|---|---|---|---|
| ☐ | Confirm breakpoints, grid, spacing, type (Parts 3–5) | [FILL] | Design tokens |
| ☐ | Design Compact first, then Medium, Expanded, Large | [FILL] | Design files: [FILL link] |
| ☐ | Define navigation per size (Part 6) | [FILL] | Part 6 |
| ☐ | Define component behavior (Part 7) | [FILL] | Part 7 |
| ☐ | Check contrast and target sizes in the design | [FILL] | Checklist |
| ☐ | Design "stress cases": long names, no data, errors, 400% zoom | [FILL] | Frames |
| ☐ | Hand-off notes for developers | [FILL] | Notes |

🤖 AGENT: Generate token files and layout specs **only from filled values**. List every value you had to ask about.

**🛑 GATE G2:**
☐ Parts 3–10 have no `[FILL` ☐ Every main screen exists at all 4+ size classes ☐ Designer and developer agree breakpoints ☐ Accessibility pre-check passed ☐ Approver signed

## PHASE 3: BUILD

**Goal:** Write the code exactly as designed.

| ☐ | Task | Owner | Output |
|---|---|---|---|
| ☐ | Set up viewport, tokens, grid, base styles | [FILL] | Starter code |
| ☐ | Build components mobile-first | [FILL] | Component library |
| ☐ | Build pages from the Part 4.1 table | [FILL] | Pages |
| ☐ | Add automated checks (accessibility, performance, visual) to the build pipeline | [FILL] | CI config |
| ☐ | Add real-user performance measuring (12.4) | [FILL] | Monitoring |
| ☐ | Code review against this file | [FILL] | Review notes |

🤖 AGENT: Work in small steps. After each step, list which Part you followed and which checks you ran. Never merge your own work.

**🛑 GATE G3:**
☐ All pages built at all size classes ☐ Automated checks run on every change ☐ No open P0/P1 ☐ Code reviewed by a human ☐ Approver signed

## PHASE 4: TEST

**Goal:** Prove it works on real devices, for real needs.

| ☐ | Task | Owner | Output |
|---|---|---|---|
| ☐ | Run the full QA checklist (15.3) on the real-device set (13.3) | [FILL] | Test report |
| ☐ | Run manual accessibility tests (11.2) | [FILL] | A11y report |
| ☐ | Run performance tests on the slow profile (12.2) | [FILL] | Perf report |
| ☐ | Test with `___` people from your target users (recommended: 5+) | [FILL] | Usability notes |
| ☐ | Fix all P0 and P1 bugs; decide P2 and P3 | [FILL] | Bug list |
| ☐ | Prepare rollback plan (18.5) | [FILL] | Rollback doc |

🤖 AGENT: Report **real results only**. If a test could not be run, write "NOT RUN: reason." Never round up a score or lower a threshold.

**🛑 GATE G4:**
☐ Zero open P0/P1 ☐ Performance budgets met on the slow profile ☐ WCAG 2.2 AA checks all pass or have approved exceptions in the Decision Log ☐ Scorecard ≥ 90 ☐ Approver signed

## PHASE 5: LAUNCH

**Goal:** Release calmly and safely, to a small group first.

| ☐ | Task | Owner | Output |
|---|---|---|---|
| ☐ | Final check of Part 18 (rollout stages, metrics, rollback) | [FILL] | Part 18 complete |
| ☐ | Set up dashboards and alerts (18.4) | [FILL] | Dashboard link: [FILL] |
| ☐ | Set up feedback channel (18.6) | [FILL] | Channel: [FILL] |
| ☐ | Prepare support answers for the 10 most likely device problems | [FILL] | FAQ |
| ☐ | Start **Stage 0** (internal) of the rollout | [FILL] | Stage 0 report |

🤖 AGENT: Prepare checklists and drafts. **Never deploy, publish, or send messages to users.** A human performs and confirms each release step.

**🛑 GATE G5:**
☐ Rollback tested at least once ☐ Alerts proven to fire (send a test alert) ☐ Support team knows the plan ☐ Approver gave **written** go-ahead

## PHASE 6: GROW TO 500

**Goal:** Reach 500 real customers while keeping the experience good on every device.

Follow **Part 18** stage by stage. After each stage, a human completes the Stage Review.

**🛑 GATE G6 (project milestone reached):**
☐ 500 customers have **used** the product (definition in 18.1) ☐ Stage 4 review complete ☐ No open P0/P1 responsive bugs ☐ Lessons added to the Decision Log ☐ Next-steps plan written

---

# PART 18: STAGED ROLLOUT TO THE FIRST 500 CUSTOMERS

> In plain words: Don't invite everyone at once. Let a few people in, check that nothing is broken, then let more in. Like testing a new swimming pool one toe, then one foot, then everyone.

## 18.1 What counts as a "customer who used the product"?

`[FILL: write one clear sentence.]`

> Example: "A person who created an account and completed the main action (watered-plant reminder set) at least once."

Count only **unique real people**, not team members, test accounts, or bots. Exclusion rules: `[FILL]`

## 18.2 Stages

| Stage | Who | Customers | Min. time in stage | Goal |
|---|---|---|---|---|
| **0: Internal** | Team + friends running the real-device list | 5–10 | [FILL: e.g., 3 days] | Catch obvious bugs on every device in 13.3 |
| **1: Private beta** | Hand-picked, friendly users | up to **10** | [FILL: e.g., 5 days] | Find real-world layout and usability problems |
| **2: Small launch** | Invited users | up to **50** | [FILL] | Confirm fixes; first real-user performance data |
| **3: Wider launch** | Waitlist or limited public | up to **150** | [FILL] | Check different devices, networks, and countries |
| **4: Open to 500** | Public or open invites | up to **500** | [FILL] | Reach the milestone with stable quality |

Planned dates: Stage 0 `___` · Stage 1 `___` · Stage 2 `___` · Stage 3 `___` · Stage 4 `___`

How people are invited to each stage: `[FILL: e.g., email list, invite codes, feature flag by percentage]`

## 18.3 Go / No-Go gates (check before moving to the next stage)

A stage moves forward **only if every line is ☑**. A human decides; an AI agent may only prepare the evidence.

| # | Condition | Stage 0→1 | Stage 1→2 | Stage 2→3 | Stage 3→4 |
|---|---|---|---|---|---|
| 1 | Open **P0** responsive bugs | 0 | 0 | 0 | 0 |
| 2 | Open **P1** responsive bugs | [FILL: ≤ _] | [FILL] | [FILL] | [FILL] |
| 3 | Customers able to finish the main task on their first try | [FILL: ≥ _%] | [FILL] | [FILL] | [FILL] |
| 4 | LCP / INP / CLS meet Part 12 at p75 *(report sample size)* | [FILL: yes/n/a] | [FILL] | [FILL] | [FILL] |
| 5 | Crash or error rate | [FILL: ≤ _%] | [FILL] | [FILL] | [FILL] |
| 6 | Device-specific complaints in last 7 days | [FILL: ≤ _] | [FILL] | [FILL] | [FILL] |
| 7 | Accessibility issues reported by users | [FILL: 0 unresolved P0/P1] | [FILL] | [FILL] | [FILL] |
| 8 | Support questions answered within | [FILL: _ hours] | [FILL] | [FILL] | [FILL] |
| 9 | Stage review written and signed | ☐ | ☐ | ☐ | ☐ |

## 18.4 Responsive metrics dashboard

Every metric below is split by **size class and device type** so one bad device can't hide inside an average.

| Metric | Why it matters | Split by | Target | Alert if | Tool |
|---|---|---|---|---|---|
| Sign-ups and activation (finished the main task) | Shows if the product works for people | Size class, OS | [FILL] | Drops below [FILL] | [FILL] |
| Task completion rate per key screen | Finds broken layouts | Size class | [FILL] | Drops by [FILL] % vs. other classes | [FILL] |
| Bounce / early exit rate | Finds confusing first screens | Size class, network | [FILL] | Higher than [FILL] | [FILL] |
| LCP, INP, CLS (p75 + sample size n) | Speed and stability | Size class, device class | Part 12 | Over target | [FILL] |
| JavaScript / app errors | Finds device-specific failures | Browser/OS/model | [FILL] | Above [FILL] | [FILL] |
| Rage clicks / dead taps | Finds buttons that are too small or not working | Size class | [FILL] | Spike of [FILL] | [FILL] |
| Orientation changes and resize errors | Finds layout breaks | Device | [FILL] | Any error | [FILL] |
| Accessibility settings in use (large text, reduce motion, screen reader, if measurable) | Shows real needs | Platform | Info only | n/a | [FILL] |
| Support tickets tagged "device/layout" | Shows human pain | Size class | [FILL] | Above [FILL] / week | [FILL] |
| Customer count toward 500 | Progress | Stage | 500 | n/a | [FILL] |

**Review rhythm:** Stage 0–1: daily. Stage 2–3: every `[FILL]` days. Stage 4: at least twice a week. Reviewer: `[FILL: name]`

**Privacy:** collect only what the Privacy Policy allows. Ask consent where the law requires. Never record passwords or payment data in session replays. Policy link: `[FILL]`

## 18.5 Rollback and hotfix rules

> In plain words: If something goes wrong, we know exactly who pauses it, how, and how fast.

| Situation | Action | Who decides | Max time to act |
|---|---|---|---|
| A **P0** bug appears on any supported device class | **Pause new invites immediately.** Roll back or hotfix. | [FILL] | [FILL: e.g., 1 hour] |
| A **P1** bug affects over `___` % of one device class | Pause invites; fix; re-test; resume | [FILL] | [FILL] |
| Performance falls below "Poor" (LCP > 4.0 s, INP > 500 ms, CLS > 0.25) for a device class | Investigate; pause the next stage | [FILL] | [FILL] |
| A serious accessibility barrier is reported | Fix within the P1 deadline; tell the reporter | [FILL] | [FILL] |
| Customer data or security concern | Follow the security plan: [FILL link]; stop rollout | [FILL] | immediately |

**How we roll back:** `[FILL: e.g., turn off the feature flag, redeploy previous version, pull the app update]`
**Who has permission to do it (name two people):** `[FILL]`
**We tested the rollback on:** `[FILL: date]`

**Hotfix path:** Reproduce on the real device → write a failing test → fix → run the full responsive checklist (15.3) for the touched screens → human approval → release to the same stage → watch the dashboard for `___` hours → resume.

🤖 AGENT: You may draft the fix and the test. You may **not** roll out, roll back, or resume invites.

## 18.6 Feedback loop

> In plain words: Listen to users, sort what they say, fix the most important things first, and tell them you fixed it.

**Where users send feedback (pick any):**
☐ In-app button ☐ Email: [FILL] ☐ Chat/community: [FILL] ☐ Short survey after the first task ☐ Scheduled calls

**Every piece of feedback is tagged with:**
- Size class and device (ask or detect, whichever the law and ethics allow)
- Screen and feature
- Type: `bug | confusion | request | accessibility | praise`
- Severity (P0–P3 using 15.2)

**Weekly triage:** Every `[FILL: weekday]`, `[FILL: owner]` sorts feedback into: **Fix now / Schedule / Decide later / Won't do**, and logs the reason in the Decision Log (Part 14) when it changes a rule in this document.

**Close the loop:** Everyone who reported a bug gets a reply when it is fixed. Owner: `[FILL]`

**Short survey questions (edit):**
1. "Were you able to do ___ easily on your device?" (Yes / Somewhat / No)
2. "What device are you using?" (Auto-fill if possible)
3. "What was the hardest part?" (free text)

## 18.7 Stage review (copy and fill after each stage)

```
Stage: ___            Dates: ___ to ___
Customers reached: ___ (unique, real; see 18.1)
Go/No-Go table (18.3): all ☑? yes / no
Top 3 problems found:
 1.
 2.
 3.
Top 3 things that worked:
 1.
 2.
 3.
Device classes with the worst experience:
Metrics with sample sizes (n):
Changes made to this document (Decision Log IDs):
Decision: ☐ GO to next stage  ☐ STAY  ☐ ROLL BACK
Signed (Approver): ___________  Date: ______
```

---

# PART 19: READY-TO-COPY AI PROMPTS

> In plain words: Copy a prompt, paste it into your AI tool, and attach this file. The prompts make the AI follow the rules and never guess.

**Always start with this line (the "Guardrail Prompt"):**

```
Read Responsive_Design_Guidelines.md completely before doing anything. Follow Part 0 exactly.
If any [FILL] or expired [DECIDE BY] affects this task, stop and ask me. Do not guess values.
Cite the section number for every decision. List anything you could not verify as "NOT VERIFIED".
```

### Phase 1: Discover
```
Using only the research I attach, summarize who the users are and what devices they use.
Fill nothing in the guide. Instead, list every question in Part 1 and Part 13 that the research
does NOT answer. Label each statement "FROM DATA" or "ASSUMED".
```

### Phase 2: Design
```
Create design tokens (spacing, type scale, breakpoints, grid) from Parts 3–5 only.
Then describe the layout of [SCREEN NAME] for Compact, Medium, Expanded, and Large using Part 4.1 and Part 7.
If a value is missing, list it under "NEED FROM HUMAN" and stop that item.
```

### Phase 3: Build
```
Build [COMPONENT/PAGE] mobile-first, following Parts 3–10.
Use the breakpoints from Part 3.2 exactly. Do not add new breakpoints.
After coding, give me: (1) the sections you followed, (2) checks you ran with real output,
(3) anything NOT VERIFIED. Do not merge or deploy.
```

### Phase 4: Test
```
Review [PR/URL/screens] against Parts 8, 11, 12, and 15.3. Test at every boundary width in 15.1.
Report each issue using the bug template in 15.4 with a severity from 15.2.
Do not say "pass" for anything you did not run. Write "NOT RUN: reason" instead.
```

### Phase 5: Launch
```
Check Part 18 for completeness. List every blank, every missing owner, and every gate in G5 that is not yet true.
Draft the support FAQ for the 10 most likely device problems using only facts in this file.
Do not publish or send anything.
```

### Phase 6: Grow to 500
```
Here is this week's dashboard export: [ATTACH]. Fill the Stage Review template (18.7) using only this data.
Show sample sizes. Highlight any device class that is worse than the rest. Recommend GO / STAY / ROLL BACK
with evidence, but I will make the decision.
```

### Feedback triage
```
Sort the attached feedback using 18.6 (size class, screen, type, severity). Propose Fix now / Schedule /
Decide later / Won't do for each item, with a one-line reason. Do not contact customers.
```

### Document health check
```
Count remaining [FILL] and [DECIDE BY] markers. Compare each Part against the Completion Scorecard (Part 16).
Report the score you can verify and what is missing. Do not edit the file.
```

---

# PART 20: PLAIN-ENGLISH GLOSSARY

| Word | Simple meaning |
|---|---|
| **Responsive design** | A product that rearranges itself to fit any screen size |
| **Mobile-first** | Design the small screen first, then add more for bigger screens |
| **Viewport** | The visible part of the screen where your product shows |
| **Breakpoint** | A screen width where the layout changes |
| **Size class** | A named group of widths: Compact, Medium, Expanded, Large, Extra-large |
| **Grid / column** | Invisible lines that keep things lined up |
| **Gutter** | The gap between columns |
| **Margin** | The empty space at the left and right edges |
| **Fluid** | Sizes that grow and shrink smoothly with the screen |
| **Container query** | A rule that changes a part (like a card) based on its own space, not the whole screen |
| **Safe area** | The part of the screen free from notches, rounded corners, and bars |
| **Touch target** | The area you can tap to press a button or link |
| **CSS pixel (px)** | A web measuring unit that is about the same size on every device |
| **dp / pt / sp** | Measuring units on Android (dp, sp) and iOS (pt) |
| **Dynamic Type / font scaling** | The system setting that makes text bigger or smaller |
| **Reflow** | Text and layout re-fitting to a narrow space without side-scrolling |
| **Contrast** | How different the text color is from the background color |
| **WCAG** | The world's rules for accessible websites and apps |
| **AA / AAA** | Levels of WCAG. AA is the standard goal; AAA is stricter |
| **Screen reader** | Software that reads the screen aloud (VoiceOver, TalkBack, NVDA) |
| **Focus** | Which item the keyboard is "on" right now |
| **LCP** | How fast the main thing on the page shows up |
| **INP** | How quickly the page responds when you tap or click |
| **CLS** | How much things jump around while loading |
| **p75 (75th percentile)** | The speed that 3 out of 4 visitors are as fast as or faster than |
| **Real-user monitoring** | Measuring speed from real visitors, not only tests |
| **Foldable** | A phone or tablet that bends and changes screen size |
| **Feature flag** | A switch that turns a feature on or off for some people without a new release |
| **Rollout** | Releasing to people in small groups instead of all at once |
| **Rollback** | Going back to the last working version |
| **Hotfix** | A fast, small fix for a serious problem |
| **Go / No-Go** | A checkpoint where a person says "continue" or "stop" |
| **P0 / P1 / P2 / P3** | Bug severity from "must fix now" to "nice to have" |
| **Design tokens** | A list of saved design values (colors, sizes, spacing) used everywhere |
| **Source of truth** | The one place that wins when things disagree |
| **AI agent** | A computer helper that can read, write, and act on instructions |

---

# PART 21: APPENDIX: A TINY FILLED-IN EXAMPLE

*This shows the style of good answers. It is for a fake app called PlantPal. Do not copy the values.*

**1.1 One sentence:** PlantPal helps busy people remember to water their plants.

**3.2 Breakpoints (changed):** None. Template defaults used (600 / 840 / 1200 / 1600).

**4.1 Home screen row:** Compact: 1 column of plant cards | Medium: 2 columns | Expanded: 3 columns with a filter on the left | Large: same as Expanded, max width 1280 px.

**4.2 Priority list:** 1) See today's watering list 2) Mark a plant as watered 3) Add a plant 4) See plant details 5) Set reminder time.

**7 Data table row (Care history):** Compact: becomes a list of cards | Medium: 3 columns | Expanded+: full table | Notes: date and plant name never hidden.

**8.1 Touch target default:** 48 × 48 px; 8 px between targets.

**12.2 Budgets (Compact, slow 4G):** LCP ≤ 2.5 s, INP ≤ 200 ms, CLS ≤ 0.1, first load ≤ 500 KB, JavaScript ≤ 170 KB.

**18.1 Customer definition:** A real person who created an account and set at least one watering reminder.

**18.3 Row 3 (Stage 1→2):** At least 70% finish "add a plant" on their first try.

**18.5 P0 action:** Pause all invites, flip the feature flag off, and the engineering lead decides within 1 hour.

**14.1 Decision D-001:** Chose a bottom bar with 4 items on Compact. Why: the main actions are reachable by thumb. Alternative rejected: hamburger menu (hides key actions). Decided by Maria (Approver), 2026-11-03.

---

*End of template. Template version 1.0.0. Standards referenced: WCAG 2.2 (including 1.4.4, 1.4.10, 1.4.12, 2.5.8), Core Web Vitals (LCP, INP, CLS), Material 3 window size classes, Apple Human Interface Guidelines. Re-check thresholds and versions at least once a year.*
