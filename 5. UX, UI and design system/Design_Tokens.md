<!--
FILE:      Design_Tokens.md
LOCATION:  /UX-UI-Design-System/Design_Tokens.md
TEMPLATE:  v1.1.0 (reusable across projects)
PURPOSE:   The ONE place where every design decision (color, text, spacing, tone, legal rules...) is written down
           once, so designers, developers and AI agents never have to guess.
-->

# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What is a "design token"?** A token is a **name with a value**, like a labeled crayon. Instead of "use that blue," everyone uses `color.action.primary` and gets the exact same blue. Change the value once and the whole product updates.

**Five simple rules**

1. **Find every `[FILL]`** and replace it. A value shown as `Default: ...` is a safe starting choice. Keep it or change it.
2. **Unsure? Write `TBD - your name - date`.** Never leave a field empty and never guess silently.
3. **Status stickers (use only these):** `⬜ Not started` · `🟨 In progress` · `✅ Done` · `⛔ Blocked` · `➖ Not needed (say why)`
4. **One source of truth.** If a value lives here, do not repeat it elsewhere. Link to this file.
5. **Symbols:** ✏️ you write · 🔒 needs approval to change · 🤖 rule for AI agents · 🟢 REQUIRED (Minimum Viable) · 🔵 OPTIONAL (add when needed)

**Two ways to use this file**

| Path | For | Do this | Time |
|---|---|---|---|
| **Fast path (Minimum Viable)** | Tiny projects, MVPs, first-time users | Do **Quick Start (Section 0)** + every 🟢 section only | ~20-30 min |
| **Full path** | Real products going to launch | Do all 🟢 and the 🔵 sections that apply (mark the others `➖`) | ~1 day, then it grows |

**Who fills what?**

| Role | Sections |
|---|---|
| Founder / Product owner | 0, 1, 8, 12, 13 |
| Designer | 3, 4, 5, 6 |
| Developer | 2, 7, 9 |
| QA / Tester | 10, 11 |
| AI agent (with human approval) | 9, drafts of 3-6 |

---

# 0. QUICK START: 5 QUESTIONS ✏️ 🟢 (Answer these first)

Pick one option each. The "Then use" column tells you which defaults to keep in Sections 3-5.

| # | Question | Your choice | Then use (defaults) |
|---|---|---|---|
| Q1 | What feeling should the product give? | ☐ Calm/trustworthy ☐ Fun/playful ☐ Serious/professional ☐ Bold/modern | Calm: blue brand, 8px radius, soft shadows · Fun: warm/bright brand, 16px radius · Serious: neutral + dark blue, 4px radius · Bold: strong brand, 0-4px radius, high contrast |
| Q2 | Where will it run? | ☐ Web ☐ iOS ☐ Android ☐ Cross-platform | Fill Section 7 rows only for the platforms you tick |
| Q3 | Dark mode? | ☐ Yes ☐ Later ☐ No | Later = still name tokens by meaning so dark mode is easy to add |
| Q4 | Do you have a brand color and font already? | ☐ Yes (write below) ☐ No | No → Default: brand `#2563EB`, font Inter |
| Q5 | Who approves changes? | [FILL name] | Put it in Section 1 and Section 9 |

**My brand color (if any):** [FILL] · **My font (if any):** [FILL]

---

# 1. PROJECT SNAPSHOT ✏️ 🟢

| Field | Your answer | Example |
|---|---|---|
| Project name | [FILL] | Sunny Tasks |
| One-sentence description | [FILL] | A to-do app for busy parents |
| Project owner / Document owner | [FILL] | Priya S. |
| Platforms | [FILL] | Web + iOS |
| Current lifecycle phase (Section 8) | [FILL: 0-7] | Phase 2 |
| Document version / Last updated (YYYY-MM-DD) | [FILL] | 0.1.0 / 2026-10-17 |
| Links: Figma · Repo · Token JSON | [FILL] | figma.com/... · github.com/... · /tokens/tokens.json |
| Brand personality (3 words) | [FILL] | Friendly, calm, trustworthy |
| Target customer | [FILL] | Parents aged 28-45 |
| Why we have tokens | [FILL] | Consistent look, faster AI-assisted shipping |
| Success looks like (measurable) | [FILL] | Zero hard-coded colors; all text passes contrast AA |
| Out of scope for now | [FILL] | Illustration style, sound |

---

# 2. TOOLS, NAMING AND STRUCTURE 🔒 🟢

## 2.1 Tool decisions

| Decision | Options | Default | Your choice |
|---|---|---|---|
| Token file format | W3C DTCG JSON · custom JSON · table only | DTCG JSON | [FILL] |
| Design tool | Figma Variables · other · none | Figma Variables | [FILL] |
| Build tool | Style Dictionary · manual | Style Dictionary | [FILL] |
| Web output | CSS variables · Tailwind · both | CSS variables | [FILL] |
| Source of truth | Figma → JSON → code · JSON → Figma + code · code only | Figma → JSON → code | [FILL] |
| Token prefix (optional) | e.g. `sunny-` | none | [FILL] |

## 2.2 Naming rule

**Pattern:** `category.type.item.variant.state` · lowercase · dots between parts · hyphens inside a part · name the *meaning*, not the color.

**Good ✅** `color.action.primary.hover` · `space.4` · `font.size.lg`  **Bad ❌** `blueButton2` · `Color_Main Blue` · `padding-17px`

## 2.3 Three layers

| Layer | Name | Holds | Screens may use? |
|---|---|---|---|
| 1 | Primitive | `color.blue.500 = #2563EB` | ❌ No |
| 2 | Semantic | `color.action.primary = {color.blue.500}` | ✅ Yes |
| 3 | Component | `button.background = {color.action.primary}` | ✅ Only that component |

An **alias** points to another token with `{curly.braces}`. Never copy a raw value twice.

---

# 3. CORE VISUAL TOKENS ✏️ 🟢

Defaults below are ready to use. Change a value only if your brand needs it.

## 3.1 Color primitives (🟢)

| Token | Default | Your value |
|---|---|---|
| `color.brand.50` / `100` / `200` / `300` / `400` | #EFF6FF / #DBEAFE / #BFDBFE / #93C5FD / #60A5FA | [FILL] |
| `color.brand.500` (main) | #2563EB | [FILL] |
| `color.brand.600` / `700` / `800` / `900` | #1D4ED8 / #1E40AF / #1E3A8A / #172554 | [FILL] |
| `color.neutral.0` / `50` / `100` / `200` / `300` | #FFFFFF / #F9FAFB / #F3F4F6 / #E5E7EB / #D1D5DB | [FILL] |
| `color.neutral.500` / `700` / `900` | #6B7280 / #374151 / #111827 | [FILL] |
| `color.red.600` / `green.600` / `yellow.500` / `blue.600` | #DC2626 / #16A34A / #EAB308 / #2563EB | [FILL] |

## 3.2 Color meaning, Layer 2 (🟢)

| Token | Light | Dark | Used for |
|---|---|---|---|
| `color.text.primary` | neutral.900 | neutral.50 | Main text |
| `color.text.secondary` | neutral.700 | neutral.300 | Less important text |
| `color.text.disabled` | neutral.500 | neutral.500 | Disabled text |
| `color.text.inverse` | neutral.0 | neutral.900 | Text on colored backgrounds |
| `color.text.link` | brand.600 | brand.300 | Links |
| `color.background.page` | neutral.0 | neutral.900 | Whole screen |
| `color.background.surface` | neutral.50 | neutral.700 | Cards, sheets |
| `color.border.default` | neutral.200 | neutral.700 | Lines |
| `color.border.focus` | brand.600 | brand.300 | Keyboard focus ring |
| `color.action.primary` (+ `.hover` `.pressed` `.disabled`) | brand.600 (700 / 800 / neutral.300) | brand.400 (300 / 200 / neutral.700) | Main buttons |
| `color.feedback.success / warning / error / info` | green.600 / yellow.500 / red.600 / blue.600 | [FILL] | Messages |
| `color.overlay.scrim` | neutral.900 @ 50% | neutral.900 @ 70% | Dim behind pop-ups |

Your changes: [FILL]

## 3.3 Typography (🟢)

| Field | Default | Your value |
|---|---|---|
| Heading / body font | Inter | [FILL] |
| Code font | JetBrains Mono | [FILL] |
| Fallback | system-ui, -apple-system, sans-serif | [FILL] |
| Font license checked? | ☐ Yes ☐ No | [FILL] |

| Token | Size | Weight | Line height | Used for |
|---|---|---|---|---|
| `font.display` | 48 | 700 | 1.1 | Hero title |
| `font.heading.xl` / `lg` / `md` | 36 / 28 / 22 | 700 / 600 / 600 | 1.2 / 1.25 / 1.3 | Titles |
| `font.body.lg` / `md` / `sm` | 18 / 16 / 14 | 400 | 1.5 / 1.5 / 1.4 | Text |
| `font.label` | 14 | 500 | 1.2 | Buttons, forms |
| `font.caption` | 12 | 400 | 1.3 | Hints |

Units: web `rem` · iOS `pt` (support Dynamic Type) · Android `sp`. **Minimum body size 🔒:** 16.

## 3.4 Spacing (🟢)

**Base unit:** 4 (all spacing is a multiple of it). Your base: [FILL]

| Token | `0` | `1` | `2` | `3` | `4` | `5` | `6` | `8` | `10` | `12` | `16` | `20` |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Value | 0 | 4 | 8 | 12 | 16 | 20 | 24 | 32 | 40 | 48 | 64 | 80 |

Typical use: 2 = small gap · 4 = default gap · 6 = card padding · 8 = section gap · 16 = page sections.
Layout: side margin mobile [FILL] (Default 16) · desktop [FILL] (Default 32) · max content width [FILL] (Default 1200) · columns [FILL] (Default 4 / 8 / 12)

## 3.5 Shape, depth and size (🟢)

| Token | Default | Your value |
|---|---|---|
| `radius.sm` / `md` / `lg` / `full` | 4 / 8 / 16 / 9999 | [FILL] |
| `border.width.thin` / `thick` | 1 / 2 | [FILL] |
| `shadow.sm` | 0 1 2 0 neutral.900 @ 10% | [FILL] |
| `shadow.md` | 0 4 8 0 neutral.900 @ 12% | [FILL] |
| `shadow.lg` | 0 12 24 0 neutral.900 @ 16% | [FILL] |
| `opacity.disabled` | 0.4 | [FILL] |
| `size.touch.min` 🔒 | 44 (iOS/Web) · 48 (Android) | [FILL] |
| `size.icon.sm / md / lg` | 16 / 24 / 32 | [FILL] |
| `size.button.height.sm / md / lg` | 32 / 40 / 48 | [FILL] |

---

# 4. EXTENDED TOKENS ✏️ 🔵 (Add when your product needs them)

## 4.1 Motion

| Token | Default | Your value |
|---|---|---|
| `motion.duration.fast / normal / slow` | 150 / 250 / 400 ms | [FILL] |
| `motion.easing.standard` | cubic-bezier(0.2, 0, 0, 1) | [FILL] |

🔒 **Reduce-motion rule:** if the user asks for less motion, durations above `fast` become 0 ms or a simple fade. ☐ Agreed

## 4.2 Breakpoints and layering

| Token | Default | Your value |
|---|---|---|
| `breakpoint.sm / md / lg / xl` | 480 / 768 / 1024 / 1280 | [FILL] |
| `z.base / sticky / dropdown / modal / toast / tooltip` | 0 / 100 / 200 / 300 / 400 / 500 | [FILL] |

## 4.3 Icons and imagery

| Field | Default | Your value |
|---|---|---|
| Icon set | Lucide | [FILL] |
| Icon stroke | 1.5 | [FILL] |
| Default icon color token | `color.text.secondary` | [FILL] |
| Image ratios / corner token | 1:1, 4:3, 16:9 / `radius.md` | [FILL] |

## 4.4 Themes and modes

| Theme | Needed? | How | Token file |
|---|---|---|---|
| Light | ☐ Yes | Default | [FILL] |
| Dark | ☐ Yes ☐ Later ☐ No | Same semantic names, new values | [FILL] |
| High contrast | ☐ Yes ☐ Later ☐ No | | [FILL] |
| White-label (per customer) | ☐ Yes ☐ Later ☐ No | Swap Layers 1 and 2 only | [FILL] |
| Density (compact / comfortable) | ☐ Yes ☐ Later ☐ No | Swap spacing tokens | [FILL] |

---

# 5. COMPONENT TOKENS ✏️ 🔵 (Fill as you build)

Values must point to Layer 2 tokens, never raw values.

| Component | Token | Points to | Status |
|---|---|---|---|
| Button primary | `button.primary.background` | `{color.action.primary}` | ⬜ |
| Button primary | `button.primary.text` | `{color.text.inverse}` | ⬜ |
| Button | `button.radius` / `button.padding.x` | `{radius.md}` / `{space.4}` | ⬜ |
| Input | `input.border` / `input.border.error` | `{color.border.default}` / `{color.feedback.error}` | ⬜ |
| Card | `card.background` / `card.shadow` | `{color.background.surface}` / `{shadow.sm}` | ⬜ |
| Modal | `modal.scrim` | `{color.overlay.scrim}` | ⬜ |
| [FILL] | | | ⬜ |

---

# 6. ACCESSIBILITY, CONTENT AND LEGAL RULES

## 6.1 Accessibility 🔒 🟢

| Rule | Target | Status |
|---|---|---|
| Normal text contrast | ≥ 4.5:1 (WCAG 2.2 AA) | ⬜ |
| Large text and UI parts (borders, icons, focus ring) | ≥ 3:1 | ⬜ |
| Touch target | ≥ 44×44 (Android 48×48) | ⬜ |
| Focus always visible | Uses `color.border.focus` | ⬜ |
| Color never the only signal | Add icon or text | ⬜ |
| Text scales to 200% without breaking | Tested | ⬜ |

**Approved pairs:** `color.text.primary` on `color.background.page` = [FILL]:1 ☐ · `color.text.inverse` on `color.action.primary` = [FILL]:1 ☐

## 6.2 Content and voice tokens ✏️ 🔵

| Field | Default | Your value |
|---|---|---|
| `voice.tone` (3 words) | Clear, kind, direct | [FILL] |
| `voice.reading.level` | Grade 6-8 | [FILL] |
| `content.button.case` | Sentence case ("Save changes") | [FILL] |
| `content.error.pattern` | What happened + how to fix it | [FILL] |
| `content.date.format` / `number.format` / `currency` | Locale-based | [FILL] |
| `i18n.languages` (now / later) | English / [FILL] | [FILL] |
| `i18n.direction` | LTR (RTL: ☐ later) | [FILL] |
| `i18n.text.expansion` | Allow +30% text length | [FILL] |
| Words to avoid | [FILL] | [FILL] |

## 6.3 Legal and compliance tokens ✏️ 🔵

| Field | Your answer |
|---|---|
| Brand usage rules (logo clear space, minimum size, wrong uses) | [FILL] |
| Font and icon licenses (name · license · commercial OK? ☐) | [FILL] |
| Cookie / consent banner uses tokens, no pre-ticked boxes ☐ | [FILL] |
| Privacy and terms link style: `color.text.link`, always visible ☐ | [FILL] |
| Store rules checked (Apple, Google Play): ☐ yes ☐ n/a | [FILL] |
| Regulations that apply (GDPR, CCPA, accessibility law, other) | [FILL] |
| Legal reviewer name and date | [FILL] |

*This section is a checklist, not legal advice. Have a qualified person review it.*

---

# 7. PLATFORM MAPPING AND TOKEN FILE ✏️ 🟢

Generated by the build tool. **Never hand-edit `/dist`.** 🔒

| Platform | Output file | Example | Status |
|---|---|---|---|
| Web CSS | `/dist/web/tokens.css` | `--color-action-primary: #2563EB;` | ⬜ |
| Tailwind | `/dist/web/tailwind.tokens.js` | `action: { primary: 'var(--color-action-primary)' }` | ⬜ |
| iOS (SwiftUI) | `/dist/ios/Tokens.swift` | `static let actionPrimary = Color(hex: 0x2563EB)` | ⬜ |
| Android (Compose) | `/dist/android/Tokens.kt` | `val ActionPrimary = Color(0xFF2563EB)` | ⬜ |
| React Native / Flutter | `/dist/rn/tokens.ts` · `/dist/flutter/tokens.dart` | `actionPrimary: '#2563EB'` | ⬜ |

**Sample token source (DTCG JSON) 🔒**

```json
{
  "color": {
    "blue": { "500": { "$type": "color", "$value": "#2563EB" } },
    "action": { "primary": { "$type": "color", "$value": "{color.blue.500}", "$description": "Main button color" } }
  },
  "space": { "4": { "$type": "dimension", "$value": "16px" } }
}
```

**Figma Variables:** collections `Primitives`, `Semantic`, `Component` · modes `Light`, `Dark` · names match Section 2 exactly. ☐ Done
**Sync method (Figma → JSON → code):** [FILL]

**Use in code**

```css
/* ✅ Good */ .button { background: var(--color-action-primary); padding: var(--space-3) var(--space-4); }
/* ❌ Bad  */ .button { background: #2563EB; padding: 12px 16px; }
```

---

# 8. LIFECYCLE: FIRST IDEA TO FIRST 500 CUSTOMERS ✏️ 🟢

Move on only when the **Gate** is fully ticked. Update Section 1 when you move.
**🤖 AI does** = work the AI agent may do. **👤 Human approves** = a person must check it. **📈 Track** = numbers to write down.

## Phase 0: Idea and Discovery
- [ ] Brand personality and 3 reference products written: [FILL]
- 🤖 AI does: summarize competitor looks, suggest 3 palettes · 👤 Human approves: final direction
- 📈 Track: interviews done (goal 5+): [FILL]
- **Gate:** We know who it is for and the feeling it gives. ☐

## Phase 1: Foundation (design the tokens)
- [ ] Sections 0-3 filled and contrast checked · [ ] Figma Variables created
- 🤖 AI does: draft scales, run contrast checks · 👤 Human approves: brand color, font, all 🔒 items
- 📈 Track: tokens defined: [FILL] · contrast failures: [FILL] (goal 0)
- **Gate:** No `[FILL]` in 🟢 sections and a human signed off. ☐

## Phase 2: Build (tokens into code)
- [ ] Token JSON committed · [ ] build creates `/dist` for every platform · [ ] Section 9 rules installed in the AI agent's instruction file · [ ] first 5 components use only tokens
- 🤖 AI does: write build config, generate components from tokens · 👤 Human approves: pull requests
- 📈 Track: hard-coded values found: [FILL] (goal 0)
- **Gate:** Search finds zero raw colors/spacing in app code. ☐

## Phase 3: Test
- [ ] Section 10 checks all pass · [ ] real devices tested: [FILL] · [ ] dark/high contrast checked (if promised)
- 🤖 AI does: run automated checks, write test scripts · 👤 Human approves: visual review on devices
- 📈 Track: open bugs (critical / minor): [FILL]
- **Gate:** No critical issues open. ☐

## Phase 4: Private Beta (10-50 users)
- [ ] Feedback on readability and look collected: [FILL link] · [ ] fixes logged in Section 11
- 🤖 AI does: group feedback into themes, propose token fixes · 👤 Human approves: which fixes ship
- 📈 Track: signups [FILL] · activated (finished first task) [FILL]% · design complaints [FILL]
- **Gate:** Top 3 design complaints fixed or planned. ☐

## Phase 5: Launch
- [ ] Token version tagged: [FILL v1.0.0] · [ ] rollback plan written: [FILL] · [ ] Section 12 checklist ticked · [ ] legal items (Section 6.3) reviewed
- 🤖 AI does: prepare release notes, final automated scan · 👤 Human approves: go / no-go
- 📈 Track: signups day 1/7/30 · crash or layout bug reports
- **Gate:** Sign-offs in Section 12 complete. ☐

## Phase 6: Grow to 500 customers
- [ ] Weekly metrics (Section 13) · [ ] changes only via Section 11 · [ ] new features use existing tokens first · [ ] monthly unused/duplicate token review
- 🤖 AI does: weekly metric summary, flag drift from tokens · 👤 Human approves: any new or changed token
- 📈 Track: **customers** ☐ 10 ☐ 50 ☐ 100 ☐ 250 ☐ **500** · activation % · week-4 retention % · support tickets about looks/usability
- **Gate:** At 500 customers, run the Tokens Health Review (Section 13) and plan v2. ☐

## Phase 7: Scale and Review (after 500)
- [ ] Decide: white-label, new platform, new theme? [FILL] · [ ] update this template with lessons (Section 13)

| Phase | Owner | Start | Target end | Actual end | Status |
|---|---|---|---|---|---|
| 0 | [FILL] | | | | ⬜ |
| 1 | [FILL] | | | | ⬜ |
| 2 | [FILL] | | | | ⬜ |
| 3 | [FILL] | | | | ⬜ |
| 4 | [FILL] | | | | ⬜ |
| 5 | [FILL] | | | | ⬜ |
| 6 | [FILL] | | | | ⬜ |

---

# 9. RULES FOR AI AGENTS 🤖🔒 🟢

Tool-neutral. Copy this section into the agent's instruction file or link to it.

**MUST ✅**
1. Use only tokens listed here. Never invent one. If missing, **stop and ask**, or log it in Section 11.
2. Use Layer 2 or Layer 3 tokens in screens, never primitives.
3. Never type raw values (`#2563EB`, `16px`, `0.2s`) in screen code.
4. Follow the naming pattern in Section 2.
5. Run the Section 10 checks before saying "done" and report the results.
6. When a token changes, update this file, the token JSON and the change log in the same pull request, and explain what and why.

**MUST NOT ❌**
1. Edit `/dist` by hand. · 2. Delete or rename a published token (deprecate it). · 3. Lower accessibility targets. · 4. Change 🔒 items without human approval. · 5. Guess brand colors, fonts or legal wording from memory.

**Allowed without asking:** a new *component* token that points to existing Layer 2 tokens.
**Needs approval:** any new primitive or semantic token, any value change, any removal.
**Approver:** [FILL name/role]

**Prompt starter (copy/paste):**
> "Read Design_Tokens.md fully. Use only tokens defined there. If something is missing, list it under Open Questions in Section 11 instead of inventing it. Never hard-code colors, spacing, fonts or timing. Finish by running the Section 10 checks and reporting results."

---

# 10. QUALITY CHECKLIST ✏️ 🟢

| # | Check | Pass |
|---|---|---|
| 1 | Token JSON is valid and builds | ☐ |
| 2 | Every `{alias}` points to a real token; no duplicate names | ☐ |
| 3 | No hard-coded colors, spacing, fonts or durations in app code (lint/search) | ☐ |
| 4 | Light and dark values exist for every semantic color (if dark mode promised) | ☐ |
| 5 | All Section 6.1 contrast pairs pass | ☐ |
| 6 | Figma names match JSON names; `/dist` is rebuilt, not hand-edited | ☐ |
| 7 | Components match design on each platform | ☐ |
| 8 | Text at 200%, reduced motion and keyboard focus tested | ☐ |
| 9 | This document is updated | ☐ |

**Set up once:** token build in CI · lint rule against hex values · visual screenshot tests · contrast script.

---

# 11. CHANGES, VERSIONS, QUESTIONS AND RISKS 🔒 🟢

**Version numbers:** PATCH 1.0.1 = tiny fix · MINOR 1.1.0 = new tokens, nothing breaks · MAJOR 2.0.0 = rename/remove, apps must update.

**To change a token:** 1) log the request below · 2) designer + developer review, human approves · 3) change this file, JSON and Figma together · 4) run Section 10 · 5) release with a new version.

**Deprecating:** mark `deprecated`, name the replacement, keep for [FILL: 2 releases / 90 days], then remove.

| Date | Version | Token(s) | What and why | Requested by | Approved by |
|---|---|---|---|---|---|
| [FILL] | 0.1.0 | All | First draft | [FILL] | [FILL] |

| # | Question / Assumption / Risk | Owner | Due | Status |
|---|---|---|---|---|
| 1 | [FILL] | [FILL] | | ⬜ |

*Common risks:* brand color fails contrast · font license cost · Figma and code drift · AI invents tokens · too many tokens · dark mode added too late.

---

# 12. LAUNCH SIGN-OFF ✏️ 🟢

- [ ] All 🟢 sections have no `[FILL]` left · [ ] Section 6.1 passes · [ ] Section 10 passes · [ ] version tagged · [ ] rollback tested · [ ] Section 9 installed · [ ] Section 6.3 reviewed (if used)

| Role | Name | Date | OK |
|---|---|---|---|
| Founder / Product owner | [FILL] | | ☐ |
| Designer | [FILL] | | ☐ |
| Developer | [FILL] | | ☐ |
| QA | [FILL] | | ☐ |

---

# 13. METRICS AND LESSONS ✏️ 🔵 (Phases 4-7)

| Metric | Target | Now |
|---|---|---|
| Token coverage in screens | 100% | [FILL] |
| Hard-coded values | 0 | [FILL] |
| Contrast failures | 0 | [FILL] |
| Time to build a new screen | Falling | [FILL] |
| Design-related bug reports | Falling | [FILL] |
| Unused tokens | < 10% | [FILL] |
| Customers (progress to 500) | 500 | [FILL] |

**Tokens Health Review (at 500):** worked well [FILL] · confused people [FILL] · merge/remove [FILL] · add for v2 [FILL]

| What happened | What we learned | Template change |
|---|---|---|
| [FILL] | | |

---

# 14. GLOSSARY AND FINAL TEST

| Word | Simple meaning |
|---|---|
| Token | A named design decision, like a labeled crayon |
| Primitive / Semantic | The raw value / the job of that value |
| Alias | A token that points to another token |
| Mode / Theme | A different set of values (light vs dark) |
| Contrast | How easy it is to tell text from its background |
| WCAG | International rules for making products usable by everyone |
| Breakpoint | Screen width where the layout changes |
| Hard-coded | A raw value typed in instead of a token (avoid) |
| Deprecate | Mark "stop using, will be removed" |
| DTCG / Style Dictionary | Standard token file format / tool that turns it into code for every platform |
| Gate | A checklist to pass before the next phase |

**Is this document done?**
- [ ] A new person can build a screen using only this file
- [ ] Searching for `[FILL]` finds nothing in 🟢 sections
- [ ] Nobody has to ask "which color, spacing or font?"
- [ ] AI rules installed; version, date and owner are correct

**If every box is ticked, the document is ready.** 🎉

---

**Appendix: filled mini example ("Sunny Tasks")** · `color.brand.500` = #F59E0B · `color.action.primary` = `{color.brand.500}` (light) / `{color.brand.400}` (dark) · `font.body.md` = Inter 16/400/1.5 · `space.4` = 16 · `radius.md` = 8 · contrast text on page = 16.1:1 ✅

**References (verify links before use):** W3C Design Tokens Community Group format · Style Dictionary docs · WCAG 2.2 Quick Reference · Apple Human Interface Guidelines · Material Design 3 · Figma Variables docs

# END OF DOCUMENT
