<!--
TEMPLATE NAME : Component_Library.md
FOLDER        : /UX-UI-and-Design-System/Component_Library.md
TEMPLATE VER  : 1.0.0
PURPOSE       : One reusable file that describes every UI component of a product, from the first
                idea to the first 500 customers. Written so humans AND AI agents never have to guess.
-->

# How to Fill This Document

> Read this whole section first. It takes 5 minutes. Everything else in the file is built on it.

## What is this file?

A **component** is a small reusable piece of a screen: a button, a text box, a menu, a pop-up message.
A **component library** is the list of all those pieces, with clear rules for how each one looks, works, and is tested.

This file is that list for **one project**. Copy it into each new project, fill it in, and keep it up to date.
Designers, developers, testers, managers, and AI agents will all read it, so it must be clear and complete.

## The 6 golden rules

1. **Replace every `[FILL: ...]`.** Each one tells you what to write and often gives an example.
2. **Never leave a blank.** If something does not apply, write `N/A: <short reason>`. If you do not know yet, write `TBD: <who will decide> by <date>`.
3. **Use short, plain sentences.** If a 10-year-old could not understand it, rewrite it.
4. **Use numbers, not feelings.** Write "loads in under 2 seconds", not "loads fast".
5. **One fact lives in one place.** If a color is defined in Section 4, other sections point to its name. They do not repeat the value.
6. **If you change something, write it down** in the Change Log (Section 15). Then update the date in Section 0.

## How to know you are finished

Search this file for the text `FILL:`. **Zero results means every blank is filled.**
Then complete the checklist in **Section 17**. Only then is the document ready.

## What the symbols mean

| Symbol | Meaning |
|---|---|
| `[FILL: ...]` | You must replace this with your own answer. |
| `[ ]` / `[x]` | A checkbox. Change `[ ]` to `[x]` when done. |
| 🛑 | **Human approval stop.** A real person must say "yes" in writing before work continues. AI agents must not skip it. |
| 🤖 | Instruction written for AI agents. |
| 💡 | A tip or example. Delete tips if you want a shorter file. |
| ⚠️ | A warning. Do not ignore it. |

## Words you will see (mini dictionary)

| Word | Simple meaning |
|---|---|
| **Component** | A reusable piece of the screen (button, card, menu). |
| **Token** | A named value, like `color.primary` instead of `#0057FF`. Change it once and it changes everywhere. |
| **Variant** | A different version of the same component (primary button, secondary button). |
| **State** | How a component looks at a moment: normal, hovered, pressed, disabled, loading, error. |
| **Prop** | A setting you can change on a component (for example `size = large`). |
| **Accessibility (a11y)** | Making sure people with different abilities can use the product (screen readers, keyboard only, low vision). |
| **i18n** | Making the product work in many languages and regions. |
| **QA** | Quality Assurance. Testing that things work. |
| **Release** | Giving a new version of the product to users. |
| **Deprecate** | Mark something as "old, stop using it, a better one is coming". |
| **AI agent** | A software helper that reads this file and does tasks such as writing code or tests. |
| **Gate** | A checkpoint. You may not go to the next phase until the checklist is complete. |

## Fill-in order (recommended)

| Step | Sections | Who usually does it | Time |
|---|---|---|---|
| 1 | 0, 1 | Project owner | 20 min |
| 2 | 2, 3 | Project manager + Design lead | 30 min |
| 3 | 4 | Designer | 1 to 3 hours |
| 4 | 5, 6 (one per component), 7 (read the example) | Designer + Developer | Ongoing |
| 5 | 8, 9, 10, 11, 12 | Developer + QA | 1 to 2 hours |
| 6 | 13, 14 | Project owner + Tech lead | 45 min |
| 7 | 15, 16 | Whole team, during and after launch | Ongoing |
| 8 | 17 | Project owner | 15 min |

💡 **Example of filling a blank**
Before: `Product name: [FILL: the name people will see, for example "Pocket Budget"]`
After: `Product name: Pocket Budget`

## Which parts can I skip?

Nothing is skipped silently. If a section does not apply, keep the heading and write `N/A: <reason>` under it. For example, "N/A: we have no mobile app in version 1."

---

# Component Library: [FILL: Project name]

## 0. Document Control

Machine-readable header. 🤖 Agents read this block first.

```yaml
document: Component_Library
template_version: 1.0.0
project_name: "[FILL: product name]"
project_code: "[FILL: short code, e.g. PB]"
document_version: "[FILL: e.g. 0.1.0]"
status: "[FILL: Draft | In Review | Approved | Live]"
last_updated: "[FILL: YYYY-MM-DD]"
owner: "[FILL: person responsible, with contact]"
approvers:
  - "[FILL: name, role]"
current_lifecycle_phase: "[FILL: 0-Plan | 1-Design | 2-Build | 3-Test | 4-Launch | 5-Grow]"
customers_so_far: "[FILL: number, e.g. 0]"
source_of_truth:
  design_files: "[FILL: link to Figma or other design tool]"
  code_repository: "[FILL: link]"
  component_docs_site: "[FILL: link or N/A: reason]"
  issue_tracker: "[FILL: link]"
```

### Who is involved

| Role | Name | Contact | Decides what? |
|---|---|---|---|
| Project owner | [FILL] | [FILL] | Final yes/no on scope and launch |
| Design lead | [FILL] | [FILL] | Look, feel, and usability |
| Tech lead | [FILL] | [FILL] | Code quality, tools, and architecture |
| QA lead | [FILL] | [FILL] | Whether quality is good enough to ship |
| Accessibility owner | [FILL] | [FILL] | Whether the product is usable by everyone |
| AI workflow owner | [FILL] | [FILL] | Which AI agents may do what |

### Document history

| Version | Date | Author | What changed |
|---|---|---|---|
| 0.1.0 | [FILL: date] | [FILL] | First draft |

---

## 1. Project Snapshot

Answer in plain words. Everyone, including AI agents, reads this to understand the product.

| Question | Your answer |
|---|---|
| What does the product do, in one sentence? | [FILL: e.g. "Helps families track shared grocery spending."] |
| Who is it for? | [FILL: e.g. "Parents aged 28 to 45 who manage a home budget."] |
| What problem does it solve? | [FILL] |
| What feeling should the design give? (pick 3 words) | [FILL: e.g. calm, friendly, trustworthy] |
| What should it NEVER feel like? (3 words) | [FILL: e.g. cluttered, childish, cold] |
| Is there an existing brand guide? | [FILL: link or "No"] |
| Which platforms? | [FILL: tick below] |

**Platforms** (tick all that apply)

- [ ] Web (desktop browser)
- [ ] Web (mobile browser)
- [ ] iOS app
- [ ] Android app
- [ ] Tablet
- [ ] Other: [FILL]

**Technology choices**

| Item | Web | iOS | Android |
|---|---|---|---|
| Framework or language | [FILL: e.g. React + TypeScript, or N/A] | [FILL: e.g. SwiftUI, or N/A] | [FILL: e.g. Jetpack Compose, or N/A] |
| Cross-platform option | [FILL: e.g. React Native, Flutter, or N/A] | same | same |
| Styling method | [FILL: e.g. CSS variables, Tailwind] | [FILL] | [FILL] |
| Component documentation tool | [FILL: e.g. Storybook] | [FILL] | [FILL] |
| Design tool | [FILL: e.g. Figma] | same | same |
| Package manager and build tool | [FILL] | [FILL] | [FILL] |

**Languages and regions at launch:** [FILL: e.g. English (US), Spanish (MX)]
**Right-to-left languages needed (Arabic, Hebrew)?** [FILL: Yes | No | Later]
**Minimum supported devices and browsers:** [FILL: e.g. last 2 versions of Chrome, Safari, Edge; iOS 16+; Android 10+]

**What is in scope for the first 500 customers? What is not?**

| In scope (we will build) | Out of scope (we will NOT build yet) |
|---|---|
| [FILL] | [FILL] |

---

## 2. Lifecycle: From First Idea to the First 500 Customers

This project moves through 6 phases. Each phase ends with a **gate**: a checklist that must be complete before the next phase starts. Each component also has its own status (see Section 5), so you track both the project phase and each component's progress.

```
Phase 0        Phase 1       Phase 2       Phase 3         Phase 4          Phase 5
PLAN     -->   DESIGN  -->   BUILD   -->   TEST &    -->   LAUNCH     -->   GROW TO 500
                                           HARDEN          (beta, then      CUSTOMERS
                                                           public)
```

### Phase summary

| Phase | Goal | AI agents may help with | 🛑 Human must approve |
|---|---|---|---|
| 0. Plan | Know what we are building and for whom | Research, drafting lists, finding gaps | Scope and component list |
| 1. Design | Design foundations and every needed component | Draft specs, check contrast, find inconsistencies | Visual design and token values |
| 2. Build | Code each component to its spec | Write code, stories, and unit tests | Merge of code to the main branch |
| 3. Test & Harden | Prove it works, is accessible, is fast, and is safe | Write and run tests, audit accessibility and performance | QA sign-off |
| 4. Launch | Release to a small beta group, then everyone | Release notes, monitoring checks | Go-live decision |
| 5. Grow to 500 | Learn from real users, and fix and improve | Analyze usage, summarize feedback, propose fixes | Every change to released components |

### Gate checklists

**Gate 0: Ready to Design**
- [ ] Section 1 is complete.
- [ ] The "first 500 customers" scope is written down.
- [ ] The first component list exists in Section 5 (it can be incomplete).
- [ ] The organizing method is chosen (Section 3).
- [ ] 🛑 Project owner approved the scope. Name and date: [FILL]

**Gate 1: Ready to Build**
- [ ] All tokens in Section 4 have real values (no `FILL:` left).
- [ ] Every "Must have" component has a complete spec (Section 6).
- [ ] Contrast and touch-size checks done for all colors and sizes.
- [ ] 🛑 Design lead approved the designs. Name and date: [FILL]

**Gate 2: Ready to Test**
- [ ] Each "Must have" component is coded and matches its spec.
- [ ] Each has a documented example page (Storybook or similar).
- [ ] Unit tests exist and pass.
- [ ] 🛑 Tech lead approved code review. Name and date: [FILL]

**Gate 3: Ready to Launch**
- [ ] The test matrix (Section 12) is complete and passing.
- [ ] Accessibility checks (Section 9) pass at WCAG 2.2 level AA.
- [ ] Performance budgets (Section 10) are met.
- [ ] Security and privacy checks (Section 11) pass.
- [ ] 🛑 QA lead signed off. Name and date: [FILL]

**Gate 4: Ready to Grow (after launch)**
- [ ] Beta group ran for at least [FILL: e.g. 2 weeks] with no critical problems open.
- [ ] Usage tracking (Section 15) is switched on and verified.
- [ ] Feedback intake (Section 15.4) is live.
- [ ] 🛑 Project owner approved public launch. Name and date: [FILL]

**Gate 5: Done (500 customers reached)**
- [ ] 500 customers meet the definition in Section 15.1.
- [ ] A review of the component library is held and its notes saved.
- [ ] Lessons learned are recorded in Section 16.
- [ ] The next version plan is written.

---

## 3. How the Library Is Organized

Pick **one** method for this project and tick it. Delete the other.

- [ ] **Method A: Atomic Design** (small to big)

| Level | Meaning | Examples |
|---|---|---|
| Foundations | Basic design values | Colors, fonts, spacing |
| Atoms | Smallest pieces | Button, Icon, Label, Text input |
| Molecules | A few atoms working together | Search box (input + button), Form field (label + input + help text) |
| Organisms | A bigger section of a screen | Header, Product card list, Login form |
| Templates | Page layouts without real content | Dashboard layout |
| Pages | Templates filled with real content | The actual "Home" page |

- [ ] **Method B: Simple Categories**

| Category | Examples |
|---|---|
| Actions | Button, Link, Icon button |
| Inputs | Text field, Checkbox, Radio, Switch, Select, Date picker |
| Navigation | Tabs, Menu, Breadcrumb, Bottom bar, Sidebar |
| Feedback | Toast, Alert, Progress, Skeleton loader, Empty state |
| Data display | Table, List, Card, Badge, Avatar |
| Overlays | Modal, Drawer, Tooltip, Popover, Bottom sheet |
| Layout | Grid, Stack, Divider, Container |

**Naming rules (everyone follows these)**

| Thing | Rule | Good example | Bad example |
|---|---|---|---|
| Component name | PascalCase, one noun | `Button`, `TextField` | `big-blue-btn` |
| Component ID | `[project code]-[level or category]-[number]` | `PB-ATOM-001` | `button1` |
| Token name | `category.role.variant` in lowercase with dots | `color.text.primary` | `blue2` |
| Variant name | Describes purpose, not looks | `danger` | `red` |
| File name | Same as component name | `Button.tsx` | `btn_final_v2.tsx` |

---

## 4. Design Foundations (Tokens)

Tokens are the names and values everything else uses. **Components must use these tokens and must never use raw values.**

⚠️ Define a token here before using it anywhere else.

### 4.1 Color

| Token name | Light mode value | Dark mode value | Used for | Contrast check |
|---|---|---|---|---|
| `color.brand.primary` | [FILL: #hex] | [FILL: #hex or N/A] | Main buttons, links | [FILL: ratio against its background] |
| `color.brand.secondary` | [FILL] | [FILL] | Supporting actions | [FILL] |
| `color.text.primary` | [FILL] | [FILL] | Main text | [FILL] |
| `color.text.secondary` | [FILL] | [FILL] | Hints, captions | [FILL] |
| `color.text.inverse` | [FILL] | [FILL] | Text on dark/brand backgrounds | [FILL] |
| `color.background.page` | [FILL] | [FILL] | Page background | [FILL] |
| `color.background.surface` | [FILL] | [FILL] | Cards, panels | [FILL] |
| `color.border.default` | [FILL] | [FILL] | Lines and outlines | [FILL] |
| `color.status.success` | [FILL] | [FILL] | Good news | [FILL] |
| `color.status.warning` | [FILL] | [FILL] | Be careful | [FILL] |
| `color.status.error` | [FILL] | [FILL] | Problems | [FILL] |
| `color.status.info` | [FILL] | [FILL] | Neutral information | [FILL] |
| `color.focus.ring` | [FILL] | [FILL] | Keyboard focus outline | [FILL] |
| `color.disabled.background` | [FILL] | [FILL] | Disabled items | N/A (exempt) |

**Color rules**
- Text contrast must be at least **4.5 : 1** (large text at least **3 : 1**). UI borders, icons, and focus rings at least **3 : 1**.
- Never use color alone to show meaning. Add an icon or text too (for example, an error shows a red color and an error icon and words).
- Dark mode supported? [FILL: Yes | No | Later]

### 4.2 Typography

| Token | Font family | Size (web px / mobile pt or sp) | Weight | Line height | Used for |
|---|---|---|---|---|---|
| `type.display` | [FILL] | [FILL] | [FILL] | [FILL] | Big headlines |
| `type.heading.1` | [FILL] | [FILL] | [FILL] | [FILL] | Page titles |
| `type.heading.2` | [FILL] | [FILL] | [FILL] | [FILL] | Section titles |
| `type.heading.3` | [FILL] | [FILL] | [FILL] | [FILL] | Sub-sections |
| `type.body.default` | [FILL] | [FILL] | [FILL] | [FILL] | Normal text |
| `type.body.small` | [FILL] | [FILL] | [FILL] | [FILL] | Notes, captions |
| `type.label` | [FILL] | [FILL] | [FILL] | [FILL] | Buttons, form labels |
| `type.code` | [FILL] | [FILL] | [FILL] | [FILL] | Code or numbers |

- Fallback fonts if the main font fails to load: [FILL]
- Text must still work when the user enlarges text to **200%**. Confirmed? [ ]
- Font license checked? [ ] Link to license: [FILL]

### 4.3 Spacing and Sizing

| Token | Value | Typical use |
|---|---|---|
| `space.1` | [FILL: e.g. 4] | Tiny gaps |
| `space.2` | [FILL: e.g. 8] | Icon to text |
| `space.3` | [FILL: e.g. 12] | Inside small items |
| `space.4` | [FILL: e.g. 16] | Standard padding |
| `space.6` | [FILL: e.g. 24] | Between groups |
| `space.8` | [FILL: e.g. 32] | Between sections |
| `space.12` | [FILL: e.g. 48] | Big separations |

- **Minimum touch/click target:** Web at least 24 x 24 px (WCAG 2.2 minimum), but aim for 44 x 44 px. iOS at least 44 x 44 pt. Android at least 48 x 48 dp. Adopted size: [FILL]

### 4.4 Shape, Depth, and Layers

| Token | Value | Used for |
|---|---|---|
| `radius.small` | [FILL] | Inputs, tags |
| `radius.medium` | [FILL] | Buttons, cards |
| `radius.large` | [FILL] | Modals, sheets |
| `radius.full` | [FILL] | Pills, avatars |
| `shadow.low` | [FILL] | Cards |
| `shadow.medium` | [FILL] | Dropdowns |
| `shadow.high` | [FILL] | Modals |
| `layer.dropdown` | [FILL: z-index] | Menus |
| `layer.modal` | [FILL] | Pop-ups |
| `layer.toast` | [FILL] | Messages |

### 4.5 Layout and Screen Sizes

| Name | Width range | Columns | Margin | Gutter |
|---|---|---|---|---|
| Small (phone) | [FILL: e.g. 0 to 599] | [FILL] | [FILL] | [FILL] |
| Medium (tablet) | [FILL: 600 to 1023] | [FILL] | [FILL] | [FILL] |
| Large (desktop) | [FILL: 1024+] | [FILL] | [FILL] | [FILL] |

- **Mobile safe areas** (notches, home bar): components must respect them. Confirmed? [ ]
- **Orientation supported** (portrait / landscape): [FILL]

### 4.6 Motion

| Token | Duration | Easing | Used for |
|---|---|---|---|
| `motion.fast` | [FILL: e.g. 100ms] | [FILL] | Hover, press |
| `motion.normal` | [FILL: e.g. 200ms] | [FILL] | Opening menus |
| `motion.slow` | [FILL: e.g. 400ms] | [FILL] | Page changes |

- **Reduced motion rule:** When a user turns on "reduce motion" in their device, animations must be removed or become simple fades. Confirmed? [ ]
- Nothing may flash more than 3 times per second.

### 4.7 Icons and Images

| Item | Decision |
|---|---|
| Icon set | [FILL: name and link] |
| Icon sizes | [FILL: e.g. 16, 20, 24, 32] |
| Icon style | [FILL: outline | filled] |
| Image formats allowed | [FILL: e.g. WebP, AVIF, SVG] |
| Every meaningful image has a text description? | [FILL: Yes, required] |

### 4.8 Token Source Files

| Item | Location |
|---|---|
| Token file in code | [FILL: e.g. `/design-tokens/tokens.json`] |
| Token file in design tool | [FILL: link] |
| How tokens sync between design and code | [FILL: e.g. manual copy | automated export] |

---

## 5. Component Inventory (Master List)

One row per component. This is the **single list of truth**. A component that is not here does not officially exist.

**Priority:** `Must` (needed for the first 500 customers), `Should` (helpful soon), `Could` (nice to have), `Won't` (not now).

**Status values:** `Idea` → `Designed` → `Built` → `Tested` → `Live` → `Deprecated`

| ID | Name | Level / Category | Priority | Status | Platforms (W / iOS / A) | Spec link | Code link | Design link | Owner | Last updated |
|---|---|---|---|---|---|---|---|---|---|---|
| [FILL: PB-ATOM-001] | [FILL: Button] | [FILL] | [FILL] | [FILL] | [FILL: W, iOS, A] | [FILL: Section 6/7 anchor] | [FILL] | [FILL] | [FILL] | [FILL] |
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

💡 Most products need these 25 starter components. Add or remove as needed:
Button, Icon button, Link, Text field, Text area, Checkbox, Radio, Switch, Select/Dropdown, Form field wrapper, Search, Tabs, Menu, Navigation bar (top/bottom), Card, List item, Badge, Avatar, Modal/Dialog, Bottom sheet, Toast/Snackbar, Alert banner, Tooltip, Progress/Loading indicator, Empty state.

**Progress tracker**

| Status | Count | % of Must components |
|---|---|---|
| Idea | [FILL] | [FILL] |
| Designed | [FILL] | [FILL] |
| Built | [FILL] | [FILL] |
| Tested | [FILL] | [FILL] |
| Live | [FILL] | [FILL] |

---

## 6. Component Spec Template

**Copy this whole section once for every component in Section 5.** Paste the copies after Section 7, or in a docs folder linked from the inventory. 🤖 Agents must read the YAML block first, then the notes.

### 6.A Machine-readable spec

```yaml
component:
  id: "[FILL: matches Section 5]"
  name: "[FILL: PascalCase name]"
  level_or_category: "[FILL]"
  status: "[FILL: Idea | Designed | Built | Tested | Live | Deprecated]"
  version: "[FILL: e.g. 1.0.0]"
  owner: "[FILL]"
  platforms: ["[FILL: web | ios | android]"]
  summary: "[FILL: one sentence, what it is and what it does]"

usage:
  use_when:
    - "[FILL: situation where this is the right choice]"
  do_not_use_when:
    - "[FILL: situation where a different component is better. Name the other component's ID]"
  anatomy:           # the named parts, from outside to inside
    - "[FILL: e.g. container, icon, label]"

variants:            # different purposes
  - name: "[FILL: e.g. primary]"
    purpose: "[FILL]"
sizes: ["[FILL: e.g. small, medium, large]"]

props:               # the settings someone can change
  - name: "[FILL]"
    type: "[FILL: text | number | true/false | one-of(...) | function]"
    default: "[FILL]"
    required: "[FILL: yes | no]"
    description: "[FILL]"

states:              # every state must be shown in the design and tested
  - "default"
  - "hover"          # web only
  - "focus"
  - "pressed"
  - "disabled"
  - "loading"
  - "error"
  - "[FILL: others, or remove the ones that do not apply and say why]"

tokens_used:
  color: ["[FILL: token names from Section 4]"]
  type: ["[FILL]"]
  space: ["[FILL]"]
  radius: ["[FILL]"]
  motion: ["[FILL]"]

behavior:
  interactions: "[FILL: what happens on click/tap/drag/keypress]"
  responsive: "[FILL: how it changes at small/medium/large screens]"
  content_rules: "[FILL: text length limits, what to do with very long text, empty data]"

accessibility:
  role_or_native_element: "[FILL: e.g. native <button>, or ARIA role]"
  keyboard: "[FILL: Tab, Enter, Space, Esc, arrow keys, as they apply]"
  screen_reader_text: "[FILL: what is announced]"
  focus_visible: "[FILL: yes, using color.focus.ring]"
  min_target_size: "[FILL: meets Section 4.3]"
  contrast_checked: "[FILL: yes/no, with date]"
  motion: "[FILL: respects reduced motion yes/no/N/A]"
  mobile_screen_readers: "[FILL: VoiceOver and TalkBack labels, or N/A]"

internationalization:
  text_comes_from: "[FILL: translation keys, not hard-coded text]"
  supports_right_to_left: "[FILL: yes | no | N/A]"
  handles_text_growth: "[FILL: yes, up to +40% longer text]"

performance:
  max_size_kb: "[FILL: from Section 10]"
  renders_without_layout_shift: "[FILL: yes | no]"

security_privacy:
  accepts_user_input: "[FILL: yes | no]"
  input_is_sanitized: "[FILL: yes | no | N/A]"
  shows_personal_data: "[FILL: yes | no, and how it is protected]"

analytics_events:    # only events agreed in Section 15.2
  - name: "[FILL: e.g. button_click]"
    when: "[FILL]"
    data_sent: "[FILL: never personal data]"

dependencies:
  uses_components: ["[FILL: IDs]"]
  used_by_components: ["[FILL: IDs]"]
  third_party_libraries: ["[FILL: name, version, license, or none]"]

testing:
  unit: "[FILL: what is checked]"
  visual: "[FILL: snapshot of each state]"
  accessibility: "[FILL: automated tool and manual steps]"
  devices: "[FILL: from Section 12]"

links:
  design: "[FILL]"
  code: "[FILL]"
  docs: "[FILL]"

ai_notes:            # extra hints for AI agents
  must_not: ["[FILL: e.g. never change the focus ring, never add new variants without approval]"]
  ask_human_if: ["[FILL: situations where the agent must stop and ask]"]
```

### 6.B Human notes

| Question | Answer |
|---|---|
| A picture or link showing every variant and state | [FILL] |
| Why does this component exist? | [FILL] |
| What mistakes do people often make with it? | [FILL] |
| Do / Don't examples | Do: [FILL]. Don't: [FILL] |
| Open questions | [FILL: or "None"] |

### 6.C Component done-checklist

- [ ] Designed with all variants and states
- [ ] Uses only tokens from Section 4
- [ ] Coded and matches the design
- [ ] Documented with live examples
- [ ] Unit tests pass
- [ ] Visual tests pass
- [ ] Accessibility checked (automated and by hand)
- [ ] Works on all required devices and browsers
- [ ] Performance budget met
- [ ] Text is translatable
- [ ] 🛑 Reviewer approved. Name and date: [FILL]
- [ ] Inventory row in Section 5 updated

---

## 7. Worked Example: Button (fully filled in)

Use this to see what a finished component looks like. **Delete it from your project copy if you want, or keep it for reference.**

```yaml
component:
  id: "PB-ATOM-001"
  name: "Button"
  level_or_category: "Atom / Actions"
  status: "Live"
  version: "1.2.0"
  owner: "Mia (Design), Sam (Engineering)"
  platforms: ["web", "ios", "android"]
  summary: "A tappable control that starts an action, such as saving or sending."

usage:
  use_when:
    - "The user needs to do something now (Save, Pay, Send)."
  do_not_use_when:
    - "The user only needs to go to another page. Use Link (PB-ATOM-003)."
    - "The action is an icon with no text. Use Icon button (PB-ATOM-002)."
  anatomy: ["container", "optional leading icon", "label", "optional loading spinner"]

variants:
  - { name: "primary",   purpose: "The one main action on a screen" }
  - { name: "secondary", purpose: "Other actions" }
  - { name: "danger",    purpose: "Actions that delete or cannot be undone" }
sizes: ["small", "medium", "large"]

props:
  - { name: "variant",  type: "one-of(primary, secondary, danger)", default: "primary", required: "no", description: "Which style to use" }
  - { name: "size",     type: "one-of(small, medium, large)", default: "medium", required: "no", description: "How big" }
  - { name: "label",    type: "text", default: "none", required: "yes", description: "Words on the button, 1 to 3 words" }
  - { name: "disabled", type: "true/false", default: "false", required: "no", description: "Stops all clicks" }
  - { name: "loading",  type: "true/false", default: "false", required: "no", description: "Shows a spinner and blocks repeat clicks" }
  - { name: "onPress",  type: "function", default: "none", required: "yes", description: "What happens on click or tap" }

states: ["default", "hover", "focus", "pressed", "disabled", "loading"]

tokens_used:
  color: ["color.brand.primary", "color.text.inverse", "color.status.error", "color.focus.ring"]
  type: ["type.label"]
  space: ["space.3", "space.4"]
  radius: ["radius.medium"]
  motion: ["motion.fast"]

behavior:
  interactions: "Click, tap, Enter key, or Space key triggers onPress. While loading, extra presses are ignored."
  responsive: "On small screens the primary button may stretch to full width."
  content_rules: "Label max 24 characters. Longer text is shortened with '...' and the full text is available as a tooltip on web."

accessibility:
  role_or_native_element: "Native button element on web; native button on iOS and Android"
  keyboard: "Tab to reach, Enter or Space to press"
  screen_reader_text: "Announces the label and 'button'. When loading, announces 'busy'."
  focus_visible: "yes, 2px ring using color.focus.ring"
  min_target_size: "44 x 44 px minimum"
  contrast_checked: "yes, 2026-09-01, all variants 4.5:1 or better"
  motion: "yes, spinner stays but any extra animation is removed"
  mobile_screen_readers: "VoiceOver and TalkBack read the label"

internationalization:
  text_comes_from: "translation key"
  supports_right_to_left: "yes, icon moves to the right side"
  handles_text_growth: "yes, button grows up to its max width"

performance:
  max_size_kb: "2"
  renders_without_layout_shift: "yes"

security_privacy:
  accepts_user_input: "no"
  input_is_sanitized: "N/A"
  shows_personal_data: "no"

analytics_events:
  - { name: "button_click", when: "Pressed", data_sent: "component id, variant, screen name. No personal data." }

dependencies:
  uses_components: ["PB-ATOM-004 (Icon)", "PB-ATOM-005 (Spinner)"]
  used_by_components: ["PB-MOL-002 (Search box)", "PB-ORG-001 (Login form)"]
  third_party_libraries: ["none"]

testing:
  unit: "Press triggers onPress; disabled and loading block presses"
  visual: "Snapshot for every variant x size x state"
  accessibility: "Automated scan + keyboard-only walkthrough + VoiceOver + TalkBack"
  devices: "Matrix in Section 12"

links:
  design: "https://example.com/figma/button"
  code: "/src/components/Button"
  docs: "https://example.com/storybook/button"

ai_notes:
  must_not: ["Add new variants without approval", "Use raw hex colors", "Remove the focus ring"]
  ask_human_if: ["A screen needs two primary buttons", "The label is longer than 24 characters"]
```

---

## 8. Patterns (How Components Work Together)

A pattern is a repeatable solution made from several components. Fill in the rules your product uses.

| Pattern | Rule for this project | Components used |
|---|---|---|
| Forms and validation | [FILL: e.g. "Check when the user leaves a field. Show the error text under the field in `color.status.error` with an icon."] | [FILL: IDs] |
| Loading | [FILL: e.g. "Under 1 second: nothing. 1 to 10 seconds: skeleton. Over 10 seconds: progress bar with text."] | [FILL] |
| Empty states | [FILL: e.g. "Always show a picture, one friendly sentence, and one button."] | [FILL] |
| Error messages | [FILL: e.g. "Say what happened and how to fix it. No blame. No codes only."] | [FILL] |
| Success feedback | [FILL] | [FILL] |
| Confirmation of risky actions | [FILL] | [FILL] |
| Navigation | [FILL: top bar, bottom bar, side menu] | [FILL] |
| Search and filters | [FILL] | [FILL] |
| Onboarding / first-time use | [FILL: matters a lot for your first 500 customers] | [FILL] |
| Offline or slow network (esp. mobile) | [FILL] | [FILL] |
| Permission requests (camera, location, notifications) | [FILL: e.g. "Explain why before the system pop-up appears."] | [FILL] |

**Writing style for all text**

| Item | Rule |
|---|---|
| Tone | [FILL: e.g. friendly, clear, no jargon] |
| Reading level | [FILL: e.g. age 12 or lower] |
| Button labels | [FILL: e.g. start with a verb: "Save", "Send message"] |
| Capitalization | [FILL: Sentence case | Title Case] |
| Date, time, number, currency format | [FILL: follows user's region] |

---

## 9. Accessibility Standard

**Target: WCAG 2.2, level AA.** Plus platform rules for iOS and Android. This applies to every component.

### Rules every component must follow

- [ ] **Keyboard:** Everything works with keyboard only. No keyboard traps. Focus order makes sense.
- [ ] **Focus:** The focus outline is always visible and not hidden by other elements.
- [ ] **Contrast:** Text 4.5:1, large text 3:1, UI parts and icons 3:1.
- [ ] **Not just color:** Meaning is also shown with text or an icon.
- [ ] **Touch size:** Targets meet Section 4.3.
- [ ] **Names and roles:** Every control has a name a screen reader can read.
- [ ] **Images:** Meaningful images have text descriptions. Decorative ones are hidden from screen readers.
- [ ] **Forms:** Every input has a visible label, clear errors, and helpful hints. No unnecessary re-typing of information.
- [ ] **Text size:** Works at 200% zoom and with large system text on phones. No loss of content.
- [ ] **Motion:** Respects reduce-motion. No auto-playing content that cannot be paused.
- [ ] **Time:** No time limits without a way to extend them.
- [ ] **Dragging:** Anything done by dragging also has a simple tap or click alternative.
- [ ] **Language:** The page and app language is set correctly. Screen readers need this.
- [ ] **Mobile:** Works with VoiceOver (iOS) and TalkBack (Android). Works in portrait and landscape unless truly impossible.

### How we check

| Check | Tool or method | Who | When |
|---|---|---|---|
| Automatic scan | [FILL: e.g. axe, Lighthouse, Accessibility Scanner] | Developer, AI agent | Every code change |
| Keyboard-only walkthrough | By hand | QA | Every component and every release |
| Screen reader walkthrough | VoiceOver, TalkBack, [FILL: NVDA/JAWS] | QA | Before every release |
| Contrast check | [FILL: tool] | Designer | When colors change |
| Test with real people with disabilities | [FILL: plan, or TBD] | Project owner | Before public launch if possible |

**Accessibility statement link (public):** [FILL: link or TBD]
**Known accessibility issues and fix dates:** [FILL: or "None"]

---

## 10. Performance Budgets

Budgets are limits. If a limit is passed, the build must be fixed or an exception must be approved.

| Measure | Budget | How measured | Status |
|---|---|---|---|
| Largest Contentful Paint (LCP) | [FILL: e.g. ≤ 2.5 s] | [FILL: Lighthouse, real-user data] | [FILL] |
| Interaction to Next Paint (INP) | [FILL: e.g. ≤ 200 ms] | [FILL] | [FILL] |
| Cumulative Layout Shift (CLS) | [FILL: e.g. ≤ 0.1] | [FILL] | [FILL] |
| Total JavaScript on first load (web) | [FILL: e.g. ≤ 200 KB compressed] | [FILL] | [FILL] |
| Single component size | [FILL: e.g. ≤ 5 KB unless approved] | [FILL] | [FILL] |
| Animation smoothness | [FILL: e.g. 60 frames per second] | [FILL] | [FILL] |
| App start time (mobile) | [FILL: e.g. ≤ 2 s on a mid-range phone] | [FILL] | [FILL] |
| App size (mobile) | [FILL: e.g. ≤ 50 MB] | [FILL] | [FILL] |
| Test device (slow phone used for checks) | [FILL: model] | | |
| Test network (slow connection used for checks) | [FILL: e.g. "Slow 4G"] | | |

---

## 11. Security, Privacy, and Languages

### 11.1 Security

- [ ] All text typed by users is cleaned before it is shown or stored (no raw HTML insertion).
- [ ] Password fields hide text by default and allow "show password".
- [ ] Components never print secrets, tokens, or personal data to logs or error messages.
- [ ] Third-party libraries are listed with name, version, and license. They are checked for known problems before use. 🛑 New libraries need approval.
- [ ] Links that open new tabs are safe.
- [ ] Payment or sensitive forms use the approved provider's components only.

### 11.2 Privacy

| Question | Answer |
|---|---|
| Which components collect personal data? | [FILL: e.g. Text field in Sign-up form] |
| What does each one collect and why? | [FILL] |
| Where is consent shown (cookie banner, permissions)? | [FILL] |
| What laws apply to our users? | [FILL: e.g. GDPR, CCPA, COPPA, or TBD: legal contact] |
| Do any users include children under 13 (or 16)? | [FILL: Yes | No] |
| Analytics data never contains personal data? | [ ] Confirmed |

### 11.3 Languages and regions (i18n)

- [ ] No text is typed directly into components. All text comes from translation files.
- [ ] Components survive 40% longer text (many languages are longer than English).
- [ ] Layout flips correctly for right-to-left languages (if needed).
- [ ] Dates, times, numbers, and currencies use the user's region format.
- [ ] Names, addresses, and phone numbers accept international formats.
- [ ] Icons and pictures are not offensive or confusing in target regions.

---

## 12. Testing and QA Matrix

### 12.1 Types of tests

| Test | What it proves | Tool | Who runs it | When |
|---|---|---|---|---|
| Unit test | One component works alone | [FILL] | Developer, AI agent | Every code change |
| Interaction test | Clicks, taps, and keys work | [FILL] | Developer, AI agent | Every code change |
| Visual regression | Looks have not changed by accident | [FILL] | Automated | Every pull request |
| Accessibility test | Meets Section 9 | [FILL] | Automated + QA | Every release |
| Performance test | Meets Section 10 | [FILL] | Automated | Every release |
| Cross-device test | Works on real devices | [FILL: BrowserStack, real phones] | QA | Before launch and monthly |
| Usability test | Real people can finish tasks | 5 users by hand | Design + QA | Before launch |
| Security test | Meets Section 11 | [FILL] | Tech lead | Before launch |

### 12.2 Device and browser matrix

| Platform | Version / Model | Priority | Tested? | Date | By |
|---|---|---|---|---|---|
| Chrome (desktop) | [FILL: latest 2] | High | [ ] | | |
| Safari (desktop) | [FILL] | High | [ ] | | |
| Firefox | [FILL] | Medium | [ ] | | |
| Edge | [FILL] | Medium | [ ] | | |
| Safari on iPhone | [FILL] | High | [ ] | | |
| Chrome on Android | [FILL] | High | [ ] | | |
| iOS app (small, large phone, tablet) | [FILL] | [FILL] | [ ] | | |
| Android app (low-end, mid, high-end, tablet) | [FILL] | [FILL] | [ ] | | |
| Screen reader pairs: VoiceOver + Safari, TalkBack + Chrome, NVDA + Firefox | [FILL] | High | [ ] | | |

### 12.3 Bug severity (everyone uses the same words)

| Level | Meaning | Fix by |
|---|---|---|
| Critical | Users cannot do the main task, data is lost, or security/privacy is broken | Before launch, or immediately if live |
| High | A main feature is hurt, or an accessibility blocker | [FILL: e.g. 3 days] |
| Medium | Annoying but there is a workaround | [FILL: e.g. next release] |
| Low | Cosmetic | [FILL: when time allows] |

**Release rule:** [FILL: e.g. "No Critical or High bugs may be open at launch."]

---

## 13. AI Agent Rules, Prompts, and Hand-offs

🤖 **This section is the instruction manual for any AI agent working in this project. Humans, edit it carefully.**

### 13.1 Reading order for agents

1. Section 0 (status and links)
2. Section 1 (what the product is)
3. Section 4 (tokens)
4. The component's spec in Section 6 or 7
5. Sections 8 to 12 (rules)
6. Section 13.2 below (rules), then do the task

### 13.2 The 12 rules AI agents must follow

1. **Do not guess.** If a needed fact says `TBD` or is missing, stop and ask a human. Do not invent it.
2. **Use only tokens from Section 4.** Never hard-code colors, sizes, spacing, or fonts.
3. **Use only components from Section 5.** Do not create a new component without a request approved under Section 14.
4. **One component per task.** Small, reviewable changes.
5. **Follow the spec exactly.** If the spec seems wrong, report it. Do not silently change it.
6. **Add tests** for every change (Section 12), and run them.
7. **Check accessibility** (Section 9) before saying "done".
8. **No new libraries** without approval (🛑 Section 11.1).
9. **Never include secrets or personal data** in code, logs, examples, or test data. Use fake data only.
10. **Show your work:** end every task with what was done, what was tested, and what you could not verify.
11. **Stop at every 🛑.** An agent cannot approve its own work.
12. **Update the documentation:** the inventory row (Section 5) and change log (Section 15.5) must match your change.

### 13.3 Task Card (the standard way to give work to an AI agent)

Copy this block for each task. A human fills it in, and the agent reads it.

```yaml
task_card:
  id: "[FILL: e.g. TASK-0042]"
  title: "[FILL: short, e.g. Build the Button component for web]"
  requested_by: "[FILL: name]"
  component_id: "[FILL: from Section 5]"
  phase: "[FILL: 0 to 5]"
  goal: "[FILL: what should be true when finished]"
  context_files:
    - "[FILL: spec link]"
    - "[FILL: design link]"
  constraints:
    - "[FILL: e.g. use TypeScript, no new libraries]"
  acceptance_criteria:        # each one must be checkable with yes/no
    - "[FILL: e.g. all 6 states match the design]"
    - "[FILL: e.g. passes the automated accessibility scan]"
  out_of_scope:
    - "[FILL: what must NOT be changed]"
  how_to_verify:
    - "[FILL: commands or steps, e.g. 'run unit tests', 'open Storybook page']"
  stop_and_ask_if:
    - "[FILL: e.g. a token is missing, the design conflicts with the spec]"
  human_checkpoint: "[FILL: who reviews and what they approve (🛑)]"
  deadline: "[FILL: date]"
  output_expected: "[FILL: e.g. pull request + short report]"
```

### 13.4 Agent report format (what the agent must send back)

```yaml
agent_report:
  task_id: ""
  status: "done | blocked | needs-human-decision"
  what_changed: []
  tests_run: []
  tests_passed: []
  accessibility_result: ""
  performance_result: ""
  could_not_verify: []
  assumptions_made: []      # should be empty, per rule 1
  questions_for_humans: []
  files_changed: []
  docs_updated: []
```

### 13.5 Copy-paste prompts

Replace the text in `[brackets]` before sending.

**Build a component**
> You are a senior front-end/mobile engineer. Read `Component_Library.md` sections 0, 1, 4, 13 and the spec for component `[ID]`. Build it for `[platform]`. Follow every rule in section 13.2. Use only existing tokens. Include unit, visual, and accessibility tests. If anything is `TBD` or unclear, stop and list your questions. When finished, reply using the agent report format in 13.4.

**Review accessibility**
> You are an accessibility specialist. Check component `[ID]` against WCAG 2.2 AA and Section 9. Test keyboard use, focus, contrast, names and roles, touch size, text zoom, and reduced motion. List each problem with severity (Section 12.3), where it is, and how to fix it. Do not change code unless asked.

**Write tests**
> You are a QA engineer. For component `[ID]`, write tests for every state and variant in its spec, plus keyboard use and error cases. Use fake data only. Report what is not covered.

**Create or update the documentation page**
> You are a technical writer. Using the spec of `[ID]`, write a documentation page for beginners: what it is, when to use it, when not to, a live example for each variant, and a Do/Don't list. Keep sentences short.

**Audit library usage (after launch)**
> You are a product analyst. Using the data in `[location]`, compare the components actually used on screens with Section 5. List components that are unused, components used in ways the spec forbids, and custom UI that should become a component. Give evidence for each point.

**Summarize user feedback**
> You are a UX researcher. Read the feedback in `[location]`. Group it by component and by theme. For each group give the number of users affected, a quote-free summary, a suggested change, and a suggested priority. Never include personal data.

**Prepare a deprecation**
> You are a release manager. Component `[ID]` will be deprecated in favor of `[new ID]`. Draft the migration guide, the list of screens affected, the timeline, and the release note in plain language.

### 13.6 Human approval checkpoints (🛑 summary)

| # | When | Who approves | What they check | Recorded where |
|---|---|---|---|---|
| 1 | End of Phase 0 | Project owner | Scope | Gate 0 |
| 2 | Token values final | Design lead | Look and contrast | Gate 1 |
| 3 | Component designs final | Design lead | Matches the spec | Section 6.C |
| 4 | Before merging code | Tech lead | Code review | Section 6.C |
| 5 | Before launch | QA lead | Test results | Gate 3 |
| 6 | Go-live | Project owner | Launch readiness | Gate 4 |
| 7 | Every change to a Live component | Design lead + Tech lead | Section 14 process | Change Log |
| 8 | Any new library | Tech lead | Security and license | Section 11.1 |
| 9 | Any use of customer data by AI | Project owner + legal contact | Privacy | [FILL] |

### 13.7 What AI agents are allowed to do

| Action | Allowed? |
|---|---|
| Read this file and project files | Yes |
| Draft specs, code, tests, docs | Yes, then a human reviews |
| Run tests | Yes |
| Merge to the main branch | [FILL: No (recommended)] |
| Publish a release | [FILL: No (recommended)] |
| Change token values | [FILL: No without 🛑] |
| Access real customer data | [FILL: No (recommended)] |
| Contact customers | [FILL: No (recommended)] |

**Approved AI tools and versions:** [FILL]
**Where AI-generated work is recorded (for traceability):** [FILL: e.g. pull-request label "ai-assisted"]

---

## 14. Governance: Changing the Library Safely

### 14.1 How to request a new component or change

Fill this out and send it to the Design lead.

```yaml
change_request:
  id: "[FILL: CR-001]"
  date: "[FILL]"
  requested_by: "[FILL]"
  type: "[FILL: new component | change | bug fix | deprecation]"
  component_id: "[FILL or 'new']"
  problem: "[FILL: what is hard or missing today, with a screenshot or link]"
  evidence: "[FILL: user feedback, data, or support tickets]"
  proposed_solution: "[FILL]"
  alternatives_considered: "[FILL: can an existing component do the job?]"
  impact: "[FILL: which screens and platforms change]"
  risk: "[FILL: low | medium | high, and why]"
  decision: "[Approved | Rejected | Needs more info | Postponed]"
  decided_by_and_date: "[FILL]"
  reason_for_decision: "[FILL]"
```

### 14.2 Decision rules

| Question | Rule |
|---|---|
| Can an existing component do this? | If yes, use it. Do not add a new one. |
| When is a new component allowed? | When the need appears in [FILL: e.g. 3 or more places] or is required for a launch feature. |
| Who decides? | Design lead (look and use) + Tech lead (code). Tie goes to Project owner. |
| How long does a decision take? | [FILL: e.g. 5 working days] |

### 14.3 Versioning rules

We use **Semantic Versioning: MAJOR.MINOR.PATCH** (for example, 2.4.1).

| Change | Version part | Example |
|---|---|---|
| Breaks existing use (renamed prop, removed variant) | MAJOR | 1.4.2 → 2.0.0 |
| New feature that does not break anything | MINOR | 1.4.2 → 1.5.0 |
| Bug fix or small visual fix | PATCH | 1.4.2 → 1.4.3 |

### 14.4 How to retire a component (deprecation)

1. Mark status `Deprecated` in Section 5 and name the replacement.
2. Announce in the release notes.
3. Keep it working for at least [FILL: e.g. 2 releases or 90 days].
4. Publish a migration guide.
5. Remove it only after usage reaches zero (check Section 15.2).

### 14.5 Review rhythm

| Meeting | How often | Who | What for |
|---|---|---|---|
| Library review | [FILL: every 2 weeks] | Design, Tech, QA | Requests, bugs, status |
| Accessibility check-in | [FILL: monthly] | A11y owner, QA | Open issues |
| Full audit | [FILL: every 3 months and at 500 customers] | Everyone | Unused or inconsistent components |

---

## 15. Launch and the First 500 Customers

### 15.1 Define success clearly

| Item | Definition |
|---|---|
| What counts as a "customer"? | [FILL: e.g. "a person who created an account AND finished setup AND used the product on 2 different days"] |
| How do we count them? | [FILL: tool or report name] |
| Who is the beta group? | [FILL: number and how chosen, e.g. 25 invited users] |
| Target date for 500 | [FILL: date or TBD] |

### 15.2 Component usage and adoption tracking

Track whether the library is really used. Anything custom or one-off hurts consistency.

| Metric | How to measure | Target | Check how often |
|---|---|---|---|
| Library coverage (% of screens built only from library components) | [FILL: code scan or design audit] | [FILL: e.g. ≥ 90%] | [FILL: every release] |
| Custom or one-off UI count | [FILL] | [FILL: e.g. decreasing] | [FILL] |
| Usage count per component | [FILL: analytics event or code search] | n/a | [FILL] |
| Unused components | [FILL] | [FILL: review for removal] | [FILL: quarterly] |
| Version spread (people using old versions) | [FILL] | [FILL] | [FILL] |
| Time to build a new screen using the library | [FILL] | [FILL: decreasing] | [FILL] |

### 15.3 User-experience signals

Measure how the components work for real customers. Never record personal data.

| Signal | What it tells us | Source | Healthy range | Alert level |
|---|---|---|---|---|
| Task success rate (can users finish sign-up, pay, etc.) | Are the components clear? | [FILL] | [FILL: e.g. ≥ 85%] | [FILL: e.g. < 70%] |
| Time to finish key tasks | Are things too slow? | [FILL] | [FILL] | [FILL] |
| Form error rate (per field) | Which fields confuse people? | [FILL] | [FILL] | [FILL] |
| Form or flow abandonment | Where do people give up? | [FILL] | [FILL] | [FILL] |
| Rage taps/clicks, dead clicks | Things that look tappable but are not | [FILL] | [FILL] | [FILL] |
| Support tickets tagged with a component ID | Which components cause trouble? | [FILL] | [FILL] | [FILL] |
| Accessibility complaints | Who is being excluded? | [FILL] | 0 | Any |
| Crash and error rate (mobile and web) | Is it stable? | [FILL] | [FILL] | [FILL] |
| Real-user speed (Section 10 numbers) | Is it fast on real devices? | [FILL] | [FILL] | [FILL] |
| Satisfaction score (e.g. quick 1 to 5 question) | Do people like it? | [FILL] | [FILL] | [FILL] |

### 15.4 Feedback and change-request intake

| Item | Answer |
|---|---|
| Where can customers send feedback? | [FILL: in-app button, email, form] |
| Where can the team log issues? | [FILL: tracker link] |
| Required tags on every item | Component ID, platform, severity (Section 12.3), phase |
| How fast do we reply? | [FILL: e.g. within 2 working days] |
| Who reads and sorts feedback? | [FILL: name or role] |
| How often is feedback reviewed? | [FILL: weekly] |
| How do accepted items enter the process? | Through the Change Request in Section 14.1 |
| How do we tell users what we fixed? | [FILL: release notes, email] |

### 15.5 Release and change log

Newest at the top. One row per release.

| Version | Release date | Type (Major/Minor/Patch) | Components affected | What changed (simple words) | Breaking? | Migration notes | Approved by |
|---|---|---|---|---|---|---|---|
| [FILL: 1.0.0] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

**Release steps**

1. [ ] All Gate 3 items are green.
2. [ ] Release notes written in simple words.
3. [ ] Rollback plan written: how to go back to the last good version in [FILL: e.g. 15 minutes]. 
4. [ ] Release to [FILL: e.g. 10%] of users first, if possible.
5. [ ] Watch Section 15.3 alert levels for [FILL: e.g. 24 hours].
6. [ ] Release to everyone.
7. [ ] 🛑 Project owner confirms.

### 15.6 Growth milestones

Copy the numbers into the table each time you check.

| Milestone | Date reached | Component library health (Section 15.2) | UX health (Section 15.3) | Top 3 issues | Decisions made |
|---|---|---|---|---|---|
| 10 customers | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| 50 customers | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| 100 customers | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| 250 customers | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| 500 customers | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

### 15.7 Support and incident plan

| Item | Answer |
|---|---|
| Who is on call for launch week? | [FILL] |
| How do we know something is broken? | [FILL: monitoring tool, alerts] |
| Who decides to roll back? | [FILL] |
| How do we talk to affected users? | [FILL] |
| After a problem, we write a short "what happened and how we prevent it" note and save it at | [FILL] |

---

## 16. Risks, Open Questions, and Lessons Learned

### 16.1 Risks

| # | Risk | Chance (L/M/H) | Impact (L/M/H) | What we do about it | Owner |
|---|---|---|---|---|---|
| 1 | [FILL: e.g. AI-written code ignores tokens] | [FILL] | [FILL] | [FILL: e.g. automated token lint in build] | [FILL] |
| 2 | [FILL: e.g. design and code drift apart] | [FILL] | [FILL] | [FILL] | [FILL] |
| 3 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

### 16.2 Open questions

| # | Question | Who must answer | Due date | Answer |
|---|---|---|---|---|
| 1 | [FILL or "None"] | [FILL] | [FILL] | [FILL] |

### 16.3 Lessons learned (fill after the 500-customer milestone)

| What went well | What did not | What we change next time |
|---|---|---|
| [FILL] | [FILL] | [FILL] |

---

## 17. Final Readiness Checklist (Is This Document Perfect?)

Tick every box before you call this document finished.

**Completeness**
- [ ] Searching for `FILL:` finds nothing.
- [ ] Every `TBD` has an owner and a date.
- [ ] Every `N/A` has a reason.
- [ ] Section 0 version, date, and phase are current.

**Clarity**
- [ ] A new teammate could understand Section 1 in under 5 minutes.
- [ ] No sentence needs a dictionary. Hard words are in the mini dictionary.
- [ ] No fact appears in two places with different values.

**Design system health**
- [ ] Every token has a value and a use.
- [ ] Every "Must" component has a complete spec.
- [ ] Inventory (Section 5) matches the specs and the code.

**Quality**
- [ ] Accessibility, performance, security, privacy, and language rules are filled in.
- [ ] Test matrix has real devices listed.

**AI readiness**
- [ ] Section 13 rules reviewed by a human.
- [ ] A sample Task Card was tried with an AI agent and the report came back complete.
- [ ] All 🛑 checkpoints have a named person.

**Launch readiness**
- [ ] Success definition and tracking (Section 15) are ready.
- [ ] Rollback plan exists.
- [ ] Feedback intake is open.

🛑 **Final approval**
Approved by: [FILL: name, role] Date: [FILL]

---

## Appendix A: Quick Reference Cards

**Status flow of a component**

`Idea → Designed → Built → Tested → Live → Deprecated`

**Priority words:** Must, Should, Could, Won't (now)

**Severity words:** Critical, High, Medium, Low

**Approval symbol:** 🛑 means a person must say yes. An AI agent cannot do it.

**Where do I look?**

| I want to know... | Go to |
|---|---|
| What colors or fonts to use | Section 4 |
| Which components exist | Section 5 |
| How to describe a new component | Section 6 |
| What a finished component looks like | Section 7 |
| How to give a task to AI | Section 13.3 |
| How to ask for a change | Section 14.1 |
| How we measure success | Section 15 |

## Appendix B: Standards and References Behind This Template

This template follows widely used public standards. Check each source for its latest version before you start a new project.

| Topic | Source |
|---|---|
| Accessibility rules | W3C Web Content Accessibility Guidelines (WCAG) 2.2, plus WAI-ARIA Authoring Practices Guide |
| Mobile accessibility and sizing | Apple Human Interface Guidelines; Google Material Design and Android accessibility guidance |
| Component organization | Brad Frost, "Atomic Design" |
| Design tokens | W3C Design Tokens Community Group format |
| Version numbers | Semantic Versioning 2.0.0 (semver.org) |
| Web speed measures | Google Core Web Vitals (LCP, INP, CLS) |
| Security basics | OWASP Top 10 and OWASP Mobile Application Security guidance |
| Privacy | GDPR, CCPA/CPRA, COPPA (confirm which apply with your legal contact) |
| Change logs | Keep a Changelog (keepachangelog.com) |

<!-- END OF TEMPLATE. Delete this comment and the "How to Fill This Document" section's tips if you want a shorter project copy, but keep the golden rules. -->
