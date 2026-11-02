# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> Save this file as `Design_System.md` inside your **UX, UI and Design System** folder.
> Copy it once per project. Never edit the master template; edit your copy.

## What is this file?
This file is the **single source of truth** for how your product looks, feels, sounds and behaves. People and AI agents read it before they design or build anything. If something is not written here, nobody should guess; they should ask or add it here first.

## The 7 simple rules
1. **Fill every `[FILL]`.** Replace it with your answer. Delete the square brackets.
2. **Do not leave blanks.** If a section does not apply, write `N/A - because <reason>`.
3. **Use the examples.** Every question shows an `Example:` line. Copy its shape, not its words.
4. **Be specific.** Write `#1A73E8`, not "a nice blue". Write `16px`, not "some space".
5. **Use the status tags.** Mark each section: `[TODO]` not started, `[DRAFT]` started, `[REVIEW]` needs a second pair of eyes, `[DONE]` finished and checked.
6. **Fill in order the first time.** Sections 0 to 8 are the foundation. Later sections depend on them.
7. **When unsure, write it in Section 24 (Open Questions).** Do not invent an answer.

## Words you will see (kid-friendly glossary)
| Word | Meaning in plain English |
|---|---|
| Design system | A rulebook plus a box of ready-made building blocks for your product |
| Token | A named value, like `color-primary = #1A73E8`. Change it once, it changes everywhere |
| Component | A reusable piece, like a button or a text box |
| Pattern | A recipe that combines components, like a "sign-up form" |
| Breakpoint | The screen width where the layout changes (phone, tablet, laptop) |
| Accessibility (a11y) | Making sure everyone can use the product, including people who cannot see well or cannot use a mouse |
| AI agent | An AI tool that reads this file and builds or checks things for you |
| QA | Quality Assurance: checking that things work and look right |
| Launch | The day real customers can use the product |

## How the status tags look in practice
```
## 5. Color  [DONE]
```

## Quick start (30 minutes)
1. Fill Section 0 (Document Control) and Section 1 (Product Snapshot).
2. Fill Section 3 (Principles) and Section 5.1 (Colors).
3. Hand the file to your AI agent with the prompt in Section 15.3.
4. Come back and finish the rest over the project.

---

# TABLE OF CONTENTS
0. Document Control
1. Product Snapshot
2. Brand Foundations
3. Design Principles
4. Platforms, Devices and Breakpoints
5. Design Tokens (Color, Type, Space, Shape, Elevation, Icons, Imagery, Motion)
6. Token Naming and File Format
7. Component Library
8. UX Patterns
8A. Business Model, Pricing and Monetization UX
9. Content and UX Writing
10. Accessibility
11. Platform-Specific Rules (Web, Mobile, Desktop, Marketing and Email)
12. Internationalization and Localization
13. Performance Budgets
14. Theming and Dark Mode
15. AI-Agent Rules
15A. AI-Agent Workflows by Lifecycle Phase
16. Tools, Files and Folder Structure
17. Governance, Versioning and Change Process
18. Quality Assurance Checklists
19. Analytics and UX Metrics
20. Lifecycle Roadmap: Build to First 500 Customers
21. Launch Readiness Checklist
21A. Legal, Compliance and Data Privacy
22. Customer Feedback and Iteration Loop
22A. Customer Success and Support Operations
23. Risks and Assumptions
24. Open Questions
25. Decision Log
26. Final Completeness Checklist
27. Changelog

---

# 0. DOCUMENT CONTROL  [TODO]

| Field | Your answer | Example |
|---|---|---|
| Project name | [FILL] | Acme Budget App |
| Document owner (one person) | [FILL] | Priya Shah |
| Contributors | [FILL] | Design: Sam; Dev: Lee; AI agent: Claude |
| Current version | [FILL] | 0.1.0 |
| Last updated (YYYY-MM-DD) | [FILL] | 2026-10-17 |
| Current lifecycle phase (see Section 20) | [FILL] | Phase 2 - Build Components |
| Status of this document | [FILL] | DRAFT |
| Where the design files live (link) | [FILL] | figma.com/file/... |
| Where the code lives (link) | [FILL] | github.com/acme/app |

---

# 1. PRODUCT SNAPSHOT  [TODO]

**Why this section exists:** every design choice must point back to who the product is for and what it must achieve.

| Question | Your answer | Example |
|---|---|---|
| What does the product do, in one sentence? | [FILL] | Helps freelancers track money and send invoices |
| Who is the main user? (age, job, skill level) | [FILL] | Freelancers, 25-45, comfortable with phones, not with spreadsheets |
| What is the user's biggest problem? | [FILL] | They lose track of unpaid invoices |
| What is the one action that must feel easy? | [FILL] | Sending an invoice in under 60 seconds |
| What are 3 words customers should say about it? | [FILL] | Simple, trustworthy, fast |
| What is it NOT? (to avoid scope creep) | [FILL] | Not full accounting software |
| Top 3 competitors or inspirations | [FILL] | Wave, FreshBooks, Notion |
| Success goal | [FILL] | 500 paying customers within 6 months of launch |

## 1.1 Product type selector
Tick **one** main type. It tells you which sections need the most attention.

| Type | Tick | Pay extra attention to |
|---|---|---|
| SaaS / business web app | [ ] | Dashboards, tables, teams and roles, billing (Sections 7, 8, 8A) |
| Consumer mobile app | [ ] | Onboarding, notifications, store listing, retention (Sections 8, 11.2, 19) |
| Marketplace (buyers and sellers) | [ ] | Trust signals, search, reviews, payments, two user types (Sections 8, 8A, 21A) |
| Content or media site | [ ] | Reading experience, SEO, ads, performance (Sections 5.2, 11.1, 13) |
| E-commerce store | [ ] | Product pages, cart, checkout, returns (Sections 8, 8A, 21A) |
| Desktop tool | [ ] | Shortcuts, menus, updates (Section 11.3) |
| Other: [FILL] | [ ] | [FILL] |

Secondary types (optional): [FILL]
Number of user types (Example: 1 = customer; 2 = buyer and seller; 3 = customer, admin, support): [FILL]

---

# 2. BRAND FOUNDATIONS  [TODO]

## 2.1 Brand personality
Pick 3 to 5 traits and describe what each means in the product.

| Trait | What it means here | What it does NOT mean |
|---|---|---|
| [FILL] | [FILL] | [FILL] |
| Example: Friendly | Warm greetings, plain words | Jokes during errors |

## 2.2 Logo rules
| Item | Your answer | Example |
|---|---|---|
| Logo file locations | [FILL] | /assets/brand/logo.svg |
| Minimum size | [FILL] | 24px high on screen |
| Clear space around logo | [FILL] | Height of the letter "A" on all sides |
| Allowed backgrounds | [FILL] | White, brand blue, black only |
| Forbidden uses | [FILL] | No stretching, no shadows, no recoloring |

## 2.3 Voice and tone summary
| Situation | Tone | Example sentence |
|---|---|---|
| Success | [FILL] | "Invoice sent. Nice work." |
| Error | [FILL] | "That did not save. Try again." |
| Warning | [FILL] | [FILL] |
| Empty state | [FILL] | [FILL] |

(Full writing rules are in Section 9.)

---

# 3. DESIGN PRINCIPLES  [TODO]

**Instructions:** write 4 to 6 rules that settle arguments. Each must be testable: a person could say "yes, we followed it" or "no, we did not".

| # | Principle | What it means | Do | Don't |
|---|---|---|---|---|
| 1 | [FILL] | [FILL] | [FILL] | [FILL] |
| Example | Clear before clever | Users understand it without help | Use plain labels | Use mystery icons without text |

**Tie-breaker rule:** when two principles disagree, this one wins: [FILL] (Example: Accessibility wins over beauty).

---

# 4. PLATFORMS, DEVICES AND BREAKPOINTS  [TODO]

## 4.1 Which platforms are in scope?
Mark `YES`, `NO` or `LATER`.

| Platform | In scope? | Minimum versions supported |
|---|---|---|
| Web app / website | [FILL] | Chrome, Safari, Firefox, Edge: latest 2 versions |
| iOS app | [FILL] | iOS 16+ |
| Android app | [FILL] | Android 10+ |
| Desktop app (Windows/macOS/Linux) | [FILL] | Windows 10+, macOS 12+ |
| Email | [FILL] | Gmail, Outlook, Apple Mail |
| Marketing and social assets | [FILL] | Landing page, ads, social images |

## 4.2 Breakpoints
| Name | Starts at width | Columns | Gutter | Margin |
|---|---|---|---|---|
| Small phone | 0px | 4 | 16px | 16px |
| Phone | 360px | 4 | 16px | 16px |
| Tablet | 768px | 8 | 24px | 32px |
| Laptop | 1024px | 12 | 24px | 48px |
| Large desktop | 1440px | 12 | 32px | auto (max width 1280px) |

Change the numbers if your product needs it: [FILL]

## 4.3 Layout approach
- Design approach: `[FILL: mobile-first / desktop-first]`
- Maximum content width: [FILL] (Example: 1280px)
- Orientation support (mobile): [FILL] (Example: portrait only)

---

# 5. DESIGN TOKENS  [TODO]

**Reminder:** a token is a named value. Always use the token name, never the raw number, in designs and code.

## 5.1 Color

### 5.1.1 Brand colors
| Token name | Hex | Where to use it | Example use |
|---|---|---|---|
| color-brand-primary | [FILL] | Main buttons, links | "Send invoice" button |
| color-brand-secondary | [FILL] | Supporting accents | Highlight chips |
| color-brand-accent | [FILL] | Rare attention-grabbers | Promo badges |

### 5.1.2 Neutral colors (grays)
| Token | Hex | Use |
|---|---|---|
| color-neutral-0 | #FFFFFF | Page background |
| color-neutral-50 | [FILL] | Subtle background |
| color-neutral-100 | [FILL] | Card background |
| color-neutral-300 | [FILL] | Borders |
| color-neutral-500 | [FILL] | Placeholder text |
| color-neutral-700 | [FILL] | Secondary text |
| color-neutral-900 | [FILL] | Main text |

### 5.1.3 Semantic colors (colors with a job)
| Token | Hex | Meaning |
|---|---|---|
| color-success | [FILL] | Worked, saved, paid |
| color-warning | [FILL] | Careful, almost full |
| color-error | [FILL] | Failed, blocked, delete |
| color-info | [FILL] | Helpful tip |
| color-focus-ring | [FILL] | Keyboard focus outline |

### 5.1.4 Color rules
- Text on background must have contrast of at least **4.5:1** (normal text) and **3:1** (large text and icons). Tool used to check: [FILL]
- Never use color alone to show meaning. Add an icon or text.
- Maximum brand colors on one screen: [FILL] (Example: 2 plus neutrals)
- Gradients allowed? [FILL] If yes, list them: [FILL]

## 5.2 Typography
| Item | Your answer | Example |
|---|---|---|
| Heading font | [FILL] | Inter |
| Body font | [FILL] | Inter |
| Code font | [FILL] | JetBrains Mono |
| Font source and license | [FILL] | Google Fonts, open license |
| Fallback fonts | [FILL] | system-ui, -apple-system, Arial, sans-serif |

### Type scale
| Token | Size / Line height | Weight | Use |
|---|---|---|---|
| text-display | 40 / 48 | 700 | Hero headlines |
| text-h1 | 32 / 40 | 700 | Page titles |
| text-h2 | 24 / 32 | 600 | Section titles |
| text-h3 | 20 / 28 | 600 | Card titles |
| text-body | 16 / 24 | 400 | Normal text |
| text-body-small | 14 / 20 | 400 | Help text |
| text-caption | 12 / 16 | 400 | Labels, footnotes |
| text-button | 16 / 24 | 600 | Buttons |

Change the numbers if needed: [FILL]

Typography rules:
- Minimum body text size: **16px on mobile web** (stops iOS from zooming inputs).
- Line length: 45 to 75 characters.
- Text alignment: left (right for right-to-left languages). Do not justify.

## 5.3 Spacing
Use a base unit of **4px**. Only use multiples.

| Token | Value | Typical use |
|---|---|---|
| space-1 | 4px | Icon to text |
| space-2 | 8px | Tight gaps |
| space-3 | 12px | Inside small components |
| space-4 | 16px | Standard gap |
| space-6 | 24px | Between groups |
| space-8 | 32px | Between sections |
| space-12 | 48px | Large separation |
| space-16 | 64px | Page sections |

## 5.4 Shape (corner radius and borders)
| Token | Value | Use |
|---|---|---|
| radius-sm | [FILL] | Inputs, chips |
| radius-md | [FILL] | Buttons, cards |
| radius-lg | [FILL] | Modals |
| radius-full | 9999px | Avatars, pills |
| border-width-default | 1px | Standard border |
| border-width-focus | 2px | Focus outline |

## 5.5 Elevation (shadows and layers)
| Token | Shadow value | Use |
|---|---|---|
| elevation-0 | none | Flat |
| elevation-1 | [FILL] | Cards |
| elevation-2 | [FILL] | Dropdowns |
| elevation-3 | [FILL] | Modals |

| Layer token (z-index) | Value | Use |
|---|---|---|
| z-base | 0 | Page |
| z-sticky | 100 | Sticky header |
| z-dropdown | 200 | Menus |
| z-modal | 300 | Dialogs |
| z-toast | 400 | Notifications |

## 5.6 Iconography
| Question | Your answer | Example |
|---|---|---|
| Icon set | [FILL] | Lucide |
| Style | [FILL] | Outline, 2px stroke, rounded ends |
| Sizes | [FILL] | 16, 20, 24 |
| Do icons need text labels? | [FILL] | Yes, unless universally known (close, search) |
| Where do icon files live? | [FILL] | /assets/icons |

## 5.7 Imagery and illustration
| Question | Your answer | Example |
|---|---|---|
| Photo style | [FILL] | Real people, natural light, no stock handshakes |
| Illustration style | [FILL] | Flat shapes, brand colors |
| Image aspect ratios allowed | [FILL] | 1:1, 4:3, 16:9 |
| Required alt text? | [FILL] | Yes, for every non-decorative image |
| Image formats and max size | [FILL] | WebP, under 200 KB |

## 5.8 Motion (animation)
| Token | Value | Use |
|---|---|---|
| motion-fast | 100ms | Hover, small changes |
| motion-normal | 200ms | Menus, toggles |
| motion-slow | 300ms | Modals, page changes |
| motion-easing-standard | ease-in-out | Default |

Motion rules:
- Respect "reduce motion" settings: turn off or simplify animation when the user asks.
- Nothing flashes more than 3 times per second.
- Motion must explain something (where it came from, what changed). Otherwise remove it.

## 5.9 Sound and haptics (mobile and desktop only)
[FILL or N/A] (Example: Light vibration on successful payment only. No sounds.)

---

# 6. TOKEN NAMING AND FILE FORMAT  [TODO]

## 6.1 Naming pattern
`category-property-variant-state`
Examples: `color-text-primary`, `color-button-primary-hover`, `space-4`, `radius-md`.

Rules:
- lowercase, words joined by hyphens
- names describe the **job**, not the look (`color-error`, not `color-red`)
- no abbreviations unless listed here: [FILL]

## 6.2 Token file
| Question | Your answer | Example |
|---|---|---|
| Format | [FILL] | JSON (W3C Design Tokens style) |
| File path | [FILL] | /design-tokens/tokens.json |
| How tokens reach code | [FILL] | Style Dictionary builds CSS variables and mobile constants |
| Who is allowed to change it | [FILL] | Design owner only, via pull request |

Starter example (copy and edit):
```json
{
  "color": {
    "brand": {
      "primary": { "$value": "#1A73E8", "$type": "color", "$description": "Main buttons and links" }
    }
  },
  "space": {
    "4": { "$value": "16px", "$type": "dimension" }
  }
}
```

---

# 7. COMPONENT LIBRARY  [TODO]

## 7.1 Component inventory
List every component. Mark status: `PLANNED`, `IN DESIGN`, `IN CODE`, `TESTED`, `LIVE`.

| Component | Needed for MVP? | Status | Design link | Code link |
|---|---|---|---|---|
| Button | Yes | [FILL] | [FILL] | [FILL] |
| Text input | [FILL] | [FILL] | [FILL] | [FILL] |
| Textarea | [FILL] | [FILL] | [FILL] | [FILL] |
| Checkbox | [FILL] | [FILL] | [FILL] | [FILL] |
| Radio button | [FILL] | [FILL] | [FILL] | [FILL] |
| Toggle switch | [FILL] | [FILL] | [FILL] | [FILL] |
| Select / dropdown | [FILL] | [FILL] | [FILL] | [FILL] |
| Date picker | [FILL] | [FILL] | [FILL] | [FILL] |
| Link | [FILL] | [FILL] | [FILL] | [FILL] |
| Card | [FILL] | [FILL] | [FILL] | [FILL] |
| Modal / dialog | [FILL] | [FILL] | [FILL] | [FILL] |
| Toast / snackbar | [FILL] | [FILL] | [FILL] | [FILL] |
| Alert banner | [FILL] | [FILL] | [FILL] | [FILL] |
| Tabs | [FILL] | [FILL] | [FILL] | [FILL] |
| Navigation bar / sidebar | [FILL] | [FILL] | [FILL] | [FILL] |
| Table / list | [FILL] | [FILL] | [FILL] | [FILL] |
| Pagination | [FILL] | [FILL] | [FILL] | [FILL] |
| Badge / chip | [FILL] | [FILL] | [FILL] | [FILL] |
| Tooltip | [FILL] | [FILL] | [FILL] | [FILL] |
| Avatar | [FILL] | [FILL] | [FILL] | [FILL] |
| Progress bar / spinner / skeleton | [FILL] | [FILL] | [FILL] | [FILL] |
| Other: [FILL] | | | | |

## 7.2 Component spec template
Copy this block for **each** component. Do not skip states.

```
### Component: [NAME]
Purpose (one sentence): [FILL]
When to use: [FILL]
When NOT to use: [FILL]

Anatomy (parts): [FILL]  (Example: container, label, icon, helper text)
Variants: [FILL]         (Example: primary, secondary, ghost, danger)
Sizes: [FILL]            (Example: small 32px, medium 40px, large 48px)

States (describe or link picture for each):
- Default: [FILL]
- Hover: [FILL]
- Focus (keyboard): [FILL]
- Pressed/Active: [FILL]
- Disabled: [FILL]
- Loading: [FILL]
- Error: [FILL]
- Success: [FILL]
- Empty (if it holds data): [FILL]

Tokens used: [FILL]
Behavior: [FILL]         (Example: Click triggers action once; disabled while loading)
Keyboard support: [FILL] (Example: Enter and Space activate)
Screen reader label: [FILL]
Responsive behavior: [FILL]
Content rules: [FILL]    (Example: max 25 characters, verb first)
Analytics event: [FILL]
Test ideas: [FILL]
```

## 7.3 Worked example: Button
```
### Component: Button
Purpose: Lets the user start an action.
When to use: One clear action, like "Send invoice".
When NOT to use: To go to another page (use Link).

Anatomy: container, label, optional leading icon
Variants: primary (1 per screen), secondary, ghost, danger
Sizes: small 32px, medium 40px, large 48px (minimum 44px touch target on mobile)

States:
- Default: fill color-brand-primary, text white
- Hover: fill color-brand-primary-hover
- Focus: 2px color-focus-ring outline, 2px offset
- Pressed: fill color-brand-primary-pressed
- Disabled: 40% opacity, no pointer, still readable
- Loading: spinner replaces icon, label stays, clicks ignored

Keyboard: Enter and Space activate
Screen reader: label text; loading announced as "Loading"
Content rules: verb first, 1-3 words ("Save", "Send invoice")
Analytics event: button_click { id, screen }
```

---

# 8. UX PATTERNS  [TODO]

For each pattern, write the rule once. Everyone reuses it.

| Pattern | Rule | Example answer |
|---|---|---|
| Navigation | [FILL] | Bottom tab bar on mobile (max 5), left sidebar on laptop |
| Sign up and log in | [FILL] | Email plus magic link; Google sign-in; no password rules longer than needed |
| Onboarding (first 5 minutes) | [FILL] | 3 steps max, skippable, ends with first success |
| Forms | [FILL] | Labels above fields, validate on blur, errors explain how to fix |
| Empty states | [FILL] | Friendly sentence + one clear next action |
| Loading | [FILL] | Skeleton screens over spinners after 300ms |
| Error states | [FILL] | Say what happened, why, and what to do next |
| Success feedback | [FILL] | Toast for small wins; full screen for big wins |
| Destructive actions (delete) | [FILL] | Confirm with the item's name; offer Undo for 10 seconds |
| Search and filters | [FILL] | [FILL] |
| Notifications | [FILL] | Ask permission only after the user sees value |
| Settings and profile | [FILL] | [FILL] |
| Permissions (camera, location) | [FILL] | Explain why before the system pop-up |
| Offline and slow network | [FILL] | Save drafts locally; show "You're offline" banner |
| Pricing and payment | [FILL] | Show total before the pay button; no surprise fees |
| Help and support | [FILL] | Help link in every screen footer or menu |

---

# 8A. BUSINESS MODEL, PRICING AND MONETIZATION UX  [TODO]

**Why this section exists:** how you earn money changes screens, words and trust. Decide it before designing sign-up, upgrade and checkout.

## 8A.1 Business model
| Question | Your answer | Example |
|---|---|---|
| How does the product make money? | [FILL] | Monthly subscription |
| Model type | [FILL: free / freemium / free trial / paid / usage-based / ads / marketplace fee / one-time purchase] | Freemium |
| Currencies and regions sold in | [FILL] | USD, EUR |
| Who pays: the user, the company, or someone else? | [FILL] | The user |
| Payment provider | [FILL] | Stripe |
| Taxes (sales tax / VAT) handled by | [FILL] | Payment provider tax tool |

## 8A.2 Plans and pricing table
| Plan | Price and billing period | What is included | What is limited | Who it is for |
|---|---|---|---|---|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Example: Free | $0 | 3 invoices per month | No custom logo | Trying it out |
| Example: Pro | $12 per month or $120 per year | Unlimited invoices | None | Working freelancers |

## 8A.3 Money-related UX rules
| Moment | Rule | Example answer |
|---|---|---|
| Pricing page | [FILL] | Show all prices; highlight one plan; no hidden fees |
| Free trial | [FILL] | Say the length and what happens at the end; remind 3 days before |
| Upgrade prompts | [FILL] | Show only when the user hits a real limit; always dismissible |
| Paywall | [FILL] | Explain what is locked and why; never lock data the user already created |
| Checkout | [FILL] | Total, tax and renewal date shown above the pay button |
| Failed payment | [FILL] | Plain message, retry option, grace period of [FILL] days |
| Cancel subscription | [FILL] | As easy as signing up; confirm end date; offer pause, never trick |
| Refunds | [FILL] | Policy link at checkout; process described in plain words |
| Invoices and receipts | [FILL] | Email automatically; downloadable |

## 8A.4 Honest-design rules (never break)
- No fake countdown timers or false "only 2 left".
- No pre-ticked boxes that add costs.
- No hiding the cancel button.
- Auto-renewal is stated clearly before payment.
- Prices shown include required taxes where law requires it.

## 8A.5 Money metrics
| Metric | Meaning | Target |
|---|---|---|
| Free-to-paid conversion | % of free users who pay | [FILL] |
| Trial-to-paid conversion | % of trials that pay | [FILL] |
| Monthly churn | % who cancel each month | [FILL] |
| Average revenue per customer | Money per paying customer | [FILL] |
| Payback time | Months to earn back the cost of getting a customer | [FILL] |

---

# 9. CONTENT AND UX WRITING  [TODO]

## 9.1 Writing rules
| Rule | Your answer | Example |
|---|---|---|
| Reading level | [FILL] | Grade 6-8 |
| Point of view | [FILL] | "You" for the user, "we" for the company |
| Sentence length | [FILL] | Under 20 words |
| Capitalization | [FILL] | Sentence case for buttons and titles |
| Numbers, dates, currency | [FILL] | 17 Oct 2026; $1,200.00 |
| Words we always use | [FILL] | "Invoice", "Client" |
| Words we never use | [FILL] | "Oops", "Whoops", jargon, blame ("You entered it wrong") |
| Emoji allowed? | [FILL] | Only in marketing, never in errors |

## 9.2 Message templates
| Type | Template | Example |
|---|---|---|
| Error | What happened + how to fix | "We could not send the invoice. Check the email address and try again." |
| Empty state | Benefit + action | "No invoices yet. Create your first one." |
| Confirmation | Result + next step | "Invoice sent. View it" |
| Destructive confirm | Name the thing | "Delete invoice #204? This cannot be undone." |

## 9.3 Microcopy library
Keep all repeated text here so it is never rewritten differently.
| Key | Text |
|---|---|
| button.save | Save |
| button.cancel | Cancel |
| error.network | [FILL] |
| error.generic | [FILL] |
| empty.default | [FILL] |

---

# 10. ACCESSIBILITY  [TODO]

**Target standard:** [FILL] (Recommended: WCAG 2.2 Level AA. Add platform rules for iOS and Android.)

## 10.1 Must-pass rules
| Area | Rule | Pass/Fail method |
|---|---|---|
| Color contrast | 4.5:1 text, 3:1 large text and UI parts | Contrast checker |
| Keyboard | Everything usable with keyboard only; visible focus; logical order | Tab through every page |
| Touch targets | At least 44x44 pt (iOS) / 48x48 dp (Android); 24x24 CSS px absolute minimum on web | Inspect sizes |
| Screen readers | All controls have names, roles, states; images have alt text | VoiceOver, TalkBack, NVDA test |
| Text resize | Works at 200% zoom with no lost content | Browser zoom |
| Motion | Respects reduce-motion; no flashing | System setting test |
| Forms | Labels linked to fields; errors announced; not color-only | Screen reader test |
| Headings and landmarks | One H1; headings in order | Outline check |
| Language | Page language set | Inspect |
| Timeouts | Warn before logging out; allow extension | Manual |
| Captions | Video has captions and transcripts | Manual |

## 10.2 Testing plan
| Test | Who | When | Tool |
|---|---|---|---|
| Automated scan | AI agent / developer | Every pull request | [FILL] (Example: axe, Lighthouse) |
| Keyboard test | Developer | Every new screen | Manual |
| Screen reader test | QA | Before each release | [FILL] |
| Real users with disabilities | Founder | Before launch | [FILL] |

Accessibility issue severity: `Blocker` stops launch; `Major` fix in 7 days; `Minor` fix in backlog.

---

# 11. PLATFORM-SPECIFIC RULES  [TODO]

Fill only the platforms marked YES in Section 4.1. Write `N/A` for the rest.

## 11.1 Web app / website
| Item | Your answer | Example |
|---|---|---|
| Framework and UI library | [FILL] | React, Tailwind |
| CSS approach | [FILL] | CSS variables generated from tokens |
| Hover behavior on touch devices | [FILL] | No hover-only features |
| SEO basics (titles, descriptions, headings) | [FILL] | Unique title under 60 chars |
| Browser support | [FILL] | See Section 4.1 |
| Cookie and privacy banner | [FILL] | Reject-all equal in prominence to Accept |

## 11.2 Mobile app (iOS / Android)
| Item | Your answer | Example |
|---|---|---|
| Build approach | [FILL] | React Native / Swift + Kotlin |
| Follow platform guidelines | [FILL] | Apple Human Interface Guidelines; Material Design |
| Navigation pattern | [FILL] | Tab bar (iOS), bottom nav (Android) |
| Safe areas (notch, home bar) | [FILL] | Respect all safe-area insets |
| Back gesture / button | [FILL] | Always supported |
| App icon and splash screen | [FILL] | Files and sizes in /assets/app |
| App store assets | [FILL] | Screenshots, description, privacy labels |
| Push notifications | [FILL] | See Section 8 |

## 11.3 Desktop app
| Item | Your answer | Example |
|---|---|---|
| Technology | [FILL] | Electron / Tauri / native |
| Window sizes (min, default) | [FILL] | 900x600 min |
| Keyboard shortcuts | [FILL] | Cmd/Ctrl+S save, Cmd/Ctrl+K command search |
| Menu bar and right-click | [FILL] | [FILL] |
| Auto update | [FILL] | Silent update with release notes |
| Dark/light follows system | [FILL] | Yes |

## 11.4 Marketing pages and email
| Item | Your answer | Example |
|---|---|---|
| Landing page structure | [FILL] | Hero, proof, 3 benefits, pricing, FAQ, sign-up |
| Email width and layout | [FILL] | 600px single column |
| Email fonts | [FILL] | System fonts only |
| Email images | [FILL] | Always alt text; works with images off |
| Dark mode emails | [FILL] | Tested in Gmail and Apple Mail |
| Unsubscribe and legal footer | [FILL] | Required in every marketing email |
| Social image sizes | [FILL] | 1200x630 link preview |
| Ad creative rules | [FILL] | [FILL] |

---

# 12. INTERNATIONALIZATION AND LOCALIZATION  [TODO]

| Question | Your answer | Example |
|---|---|---|
| Launch languages | [FILL] | English only |
| Future languages | [FILL] | Spanish, Hindi |
| Right-to-left support needed? | [FILL] | Later |
| Text expansion allowance | [FILL] | Leave 30-40% extra room |
| Date, time, number, currency formats | [FILL] | Use the user's locale |
| Where strings live | [FILL] | /locales/en.json - no text hard-coded in components |
| Images with text inside | [FILL] | Avoid |

---

# 13. PERFORMANCE BUDGETS  [TODO]

| Metric | Target | Your target |
|---|---|---|
| Largest Contentful Paint (main content appears) | Under 2.5 s | [FILL] |
| Interaction to Next Paint (responds to taps/clicks) | Under 200 ms | [FILL] |
| Cumulative Layout Shift (things jumping around) | Under 0.1 | [FILL] |
| App cold start (mobile) | Under 2 s | [FILL] |
| Page weight (web) | Under 1 MB initial | [FILL] |
| Font files | Max 2 families, subsets only | [FILL] |
| Image weight | Under 200 KB each | [FILL] |

Rule: a change that breaks a budget cannot ship without a written exception in Section 25.

---

# 14. THEMING AND DARK MODE  [TODO]

| Question | Your answer | Example |
|---|---|---|
| Themes supported | [FILL] | Light, Dark, High contrast |
| Follows system setting? | [FILL] | Yes, with manual override |
| How tokens change by theme | [FILL] | Same token names, different values per theme |
| Dark mode rules | [FILL] | No pure black (#000) backgrounds; reduce shadow, use surface tint |
| Contrast check done for each theme? | [FILL] | Yes, required |
| Brand customization (white label)? | [FILL] | No |

---

# 15. AI-AGENT RULES  [TODO]

**Purpose:** AI agents follow this file literally. These rules make them safe, consistent and honest about what they do not know.

## 15.1 Source-of-truth order (highest wins)
1. This `Design_System.md`
2. Token file (Section 6.2)
3. Component code and Storybook (Section 16)
4. Design files (Figma)
5. Anything else (examples from the internet, the agent's memory)

## 15.2 Always / Never
**The agent must ALWAYS:**
- Use token names, never raw hex, pixels or font names.
- Reuse an existing component before creating a new one.
- Implement all states from Section 7.2.
- Check accessibility rules in Section 10 before saying "done".
- Write a short summary of what changed and which files it touched.
- Say "I do not know" and add a line to Section 24 when this file does not answer the question.

**The agent must NEVER:**
- Invent colors, fonts, spacing, copy or features not listed here.
- Edit this file without being asked; propose the change instead.
- Delete tokens or components that are in use.
- Add new libraries or dependencies without approval.
- Use real customer data in examples, tests or screenshots.
- Skip tests to finish faster.

## 15.3 Starter prompt to paste into any AI tool
```
You are working on the project described in Design_System.md. Read it fully first.
Rules: follow Section 15 exactly. Use only tokens and components defined in it.
If something is missing or unclear, STOP and ask me. Do not guess.
Task: [describe what you want built or checked]
When finished, give me: (1) what you changed, (2) which sections of the
design system you followed, (3) which accessibility checks you ran,
(4) anything you were unsure about.
```

## 15.4 Ambiguity protocol
1. Search this file. 2. If not found, check Section 24 for an open question. 3. If still unclear, ask the owner. 4. Record the answer in Section 25.

## 15.5 Definition of Done (for any AI or human task)
- [ ] Matches the design system (tokens, components, copy)
- [ ] All states implemented
- [ ] Passes Section 10 accessibility rules
- [ ] Works at all breakpoints in Section 4.2
- [ ] Meets budgets in Section 13
- [ ] Tests written and passing
- [ ] Analytics events added (Section 19)
- [ ] Documentation and changelog updated

## 15.6 Human review gates (AI cannot self-approve)
| Gate | Reviewer |
|---|---|
| New token or component | [FILL] |
| Anything involving payments, privacy, legal text | [FILL] |
| Release to customers | [FILL] |

---

# 15A. AI-AGENT WORKFLOWS BY LIFECYCLE PHASE  [TODO]

**Why this section exists:** Section 15 says how agents must behave. This section says **which agent does what, when, and who checks it**.

## 15A.1 Agent roles
| Role | Job | Reads | Writes | Cannot do |
|---|---|---|---|---|
| Researcher agent | Summarize interviews, competitors, market facts | Notes, links | Research summaries | Decide product direction |
| Designer agent | Draft screens, tokens, copy from this file | This file, token file | Design drafts, microcopy | Approve its own work |
| Builder agent | Write code from specs | This file, components | Code, tests | Add libraries without approval |
| QA agent | Run checklists, write tests, scan accessibility | This file, code | Bug reports | Fix and approve the same bug |
| Support agent | Draft replies, group feedback | Feedback, help articles | Reply drafts | Send without human OK (until you allow it) |
| Reviewer agent | Compare output against Section 15.5 | Everything | Review notes | Merge or publish |

Your agent tools for each role: [FILL] (Example: Builder = Claude Code; Designer = Claude + Figma)

## 15A.2 The working loop for every task
1. **Human** writes the task in one paragraph, linked to the section(s) of this file.
2. **Agent** restates the task and lists what it will touch. Human says OK.
3. **Agent** does the work and fills the report below.
4. **Different agent or human** reviews against Section 15.5.
5. **Human** approves at the gates in Section 15.6.
6. **Agent** updates the changelog and Open Questions.

## 15A.3 Agent report format (agents must reply this way)
```
TASK: <one line>
SECTIONS FOLLOWED: <list>
FILES CHANGED: <list>
ACCESSIBILITY CHECKS RUN: <list and results>
TESTS RUN: <list and results>
THINGS I ASSUMED: <list, should be empty>
QUESTIONS FOR OWNER: <list>
```

## 15A.4 Prompt library by phase
| Phase | Ready-to-use prompt (edit the brackets) |
|---|---|
| 0 Discover | "Read these [interview notes]. List the top 5 problems users mention, with quotes from the notes and how many people said each." |
| 1 Foundations | "Using Section 5.1 brand colors, generate the full neutral and semantic palette. Check every text/background pair for 4.5:1 contrast and list failures." |
| 2 Components | "Build the [Button] component exactly from its spec in Section 7. Include all states, keyboard support and tests." |
| 3 Screens | "Using only components in Section 7 and patterns in Section 8, draft the [Sign-up] screen at phone and laptop sizes. List any missing component." |
| 4 Build | "Implement [feature] following Section 15.5. Add analytics events from Section 19.1." |
| 5 Quality | "Run the checklists in Section 18 against [staging link]. Report failures by severity." |
| 6 Beta | "Group these [feedback items] into themes, count each, and propose the top 3 fixes." |
| 7 Launch | "Walk through Section 21 and tell me which boxes are not yet provable from evidence." |
| 8 Growth | "Compare Section 19.2 numbers for the last 2 weeks. Explain changes and suggest one experiment." |

## 15A.5 Trust and safety for agents
| Rule | Your answer | Example |
|---|---|---|
| What data can agents see? | [FILL] | Test data only; no real customer data |
| Which systems can agents change? | [FILL] | Code repo branches; not production |
| What needs a human click? | [FILL] | Merge, deploy, payments, emails to customers |
| How are agent actions logged? | [FILL] | Reports saved in /handoff |
| Where do agent secrets (keys) live? | [FILL] | Secret manager; never inside this file |
| If an agent is wrong twice in a row | [FILL] | Stop, update this file, retry |

## 15A.6 Improving the loop
When an agent guesses wrong, fix **this file**, not just the output. Record it in Section 25.

---

# 16. TOOLS, FILES AND FOLDER STRUCTURE  [TODO]

## 16.1 Tools
| Purpose | Tool | Link |
|---|---|---|
| Design | [FILL] (Example: Figma) | [FILL] |
| Component playground | [FILL] (Example: Storybook) | [FILL] |
| Code hosting | [FILL] | [FILL] |
| Task tracking | [FILL] | [FILL] |
| Analytics | [FILL] | [FILL] |
| Feedback collection | [FILL] | [FILL] |
| Error monitoring | [FILL] | [FILL] |
| AI agents used | [FILL] | [FILL] |

## 16.2 Recommended folder structure
```
/ux-ui-design-system
  Design_System.md          <- this file
  /design-tokens            <- tokens.json
  /assets
    /brand                  <- logos
    /icons
    /illustrations
    /app                    <- app icon, splash
  /components               <- one spec per component (Section 7.2)
  /patterns
  /research                 <- interviews, surveys
  /accessibility-reports
  /handoff                  <- exports, specs for developers
```
Your actual structure: [FILL or "same as recommended"]

## 16.3 File naming
Pattern: `[FILL]` (Example: `component-button-primary-large.svg`, all lowercase, hyphens, no spaces)

---

# 17. GOVERNANCE, VERSIONING AND CHANGE PROCESS  [TODO]

## 17.1 Version numbers
`MAJOR.MINOR.PATCH`
- MAJOR: breaking change (a token renamed or removed)
- MINOR: new token or component
- PATCH: fix or wording change

## 17.2 How to change the design system
1. Write the request: what, why, who is affected.
2. Check whether an existing token or component already solves it.
3. Design it, including all states.
4. Review: accessibility + consistency.
5. Build, test, document.
6. Update version and Section 27.
7. Announce the change.

## 17.3 Deprecation
Mark as `DEPRECATED` for [FILL] days (Example: 30), name the replacement, then remove.

## 17.4 Ownership
| Area | Owner | Backup |
|---|---|---|
| Tokens | [FILL] | [FILL] |
| Components | [FILL] | [FILL] |
| Content and voice | [FILL] | [FILL] |
| Accessibility | [FILL] | [FILL] |

## 17.5 Review rhythm
Review this document every [FILL] (Example: 2 weeks during build, monthly after launch).

---

# 18. QUALITY ASSURANCE CHECKLISTS  [TODO]

## 18.1 Visual QA (every screen)
- [ ] Only design-system tokens used
- [ ] Spacing is on the 4px grid
- [ ] Text matches the type scale
- [ ] Every state looked at (hover, focus, disabled, loading, error, empty)
- [ ] Works at every breakpoint
- [ ] Light and dark themes checked
- [ ] Long text, very short text and missing images checked
- [ ] No placeholder text ("Lorem ipsum") remains

## 18.2 Functional QA
- [ ] Main user journey works start to finish
- [ ] Wrong input handled with helpful messages
- [ ] Slow network and offline tested
- [ ] Back button and refresh behave sensibly
- [ ] Payment flow tested in test mode (if applicable)
- [ ] Emails and notifications received and readable

## 18.3 Device and browser matrix
| Platform | Minimum set to test | Your set |
|---|---|---|
| Web | Chrome, Safari, Firefox, Edge | [FILL] |
| iOS | Smallest supported iPhone + newest iPhone | [FILL] |
| Android | One low-cost phone + one flagship | [FILL] |
| Desktop | Windows + macOS | [FILL] |
| Email | Gmail, Outlook, Apple Mail | [FILL] |

## 18.4 Bug severity
| Level | Meaning | Response |
|---|---|---|
| Blocker | Cannot use product or data lost | Fix before anything else |
| Major | Main feature broken, workaround exists | Fix within [FILL] days |
| Minor | Small visual or wording problem | Backlog |

## 18.5 Security and privacy design checks
- [ ] No secrets or personal data visible in the interface or URLs
- [ ] Passwords hidden with a show/hide option
- [ ] Privacy policy and terms linked at sign-up
- [ ] Data collection explained in plain words
- [ ] Consent (cookies, tracking) is a real choice

---

# 19. ANALYTICS AND UX METRICS  [TODO]

## 19.1 Events to track
| Event name | When it fires | Properties | Why we track it |
|---|---|---|---|
| signup_started | User opens sign-up | source | Funnel |
| signup_completed | Account created | method | Funnel |
| onboarding_completed | Last step finished | time_taken | Activation |
| first_key_action | [FILL: first value moment] | [FILL] | Activation |
| [FILL] | [FILL] | [FILL] | [FILL] |

Naming rule: `object_action` in lowercase with underscores.

## 19.2 Key numbers (fill your targets)
| Metric | Meaning | Target |
|---|---|---|
| Activation rate | % of sign-ups who do the first key action | [FILL] |
| Time to first value | Minutes from sign-up to first success | [FILL] |
| Task success rate | % who finish the main task | [FILL] |
| Week-1 / Week-4 retention | % who come back | [FILL] |
| Satisfaction (CSAT or NPS) | How happy people are | [FILL] |
| Support tickets per 100 users | Confusion signal | [FILL] |
| Crash-free sessions | Stability | 99.5%+ |

## 19.3 Privacy for analytics
Tracking consent method: [FILL]. Data retention: [FILL]. No personal data in event properties unless approved.

---

# 20. LIFECYCLE ROADMAP: BUILD TO FIRST 500 CUSTOMERS  [TODO]

**How to use:** this is your map. Mark the current phase in Section 0. A phase is finished only when its **exit gate** is fully checked.

## Phase 0 - Discover and Define
| Item | Details |
|---|---|
| Goal | Know who it is for and what problem to solve |
| Work | User interviews (aim 5-10), competitor review, Sections 1-3 of this file |
| AI agent helps with | Summarizing interviews, listing competitor patterns, drafting personas (human verifies) |
| Exit gate | - [ ] Problem statement agreed - [ ] Target user described - [ ] MVP scope written (must / should / won't) |
| Target dates | Start [FILL] End [FILL] |

## Phase 1 - Design Foundations
| Item | Details |
|---|---|
| Goal | Tokens and rules ready |
| Work | Sections 4-6, 9, 10, 14; build style tile; contrast checks |
| AI agent helps with | Generating token files, checking contrast, drafting microcopy |
| Exit gate | - [ ] All tokens defined - [ ] Contrast passes - [ ] Token file in repo |
| Target dates | [FILL] |

## Phase 2 - Component Library
| Item | Details |
|---|---|
| Goal | Reusable parts built once, tested |
| Work | Section 7 for MVP components; Storybook set up |
| AI agent helps with | Building components from specs, writing tests, accessibility scans |
| Exit gate | - [ ] Every MVP component has all states - [ ] A11y scan clean - [ ] Documented |
| Target dates | [FILL] |

## Phase 3 - Screens, Flows and Prototype
| Item | Details |
|---|---|
| Goal | Full user journey designed and clickable |
| Work | Wireframes, high-fidelity screens, Section 8 patterns, prototype test with 5 people |
| AI agent helps with | Screen drafts from patterns, copy variants, edge-case lists |
| Exit gate | - [ ] Main journey tested with real people - [ ] Top 5 problems fixed |
| Target dates | [FILL] |

## Phase 4 - Build the Product (Development)
| Item | Details |
|---|---|
| Goal | Working product |
| Work | Build screens from components; connect data; analytics events (Section 19) |
| AI agent helps with | Code, unit tests, code review against Section 15.5 |
| Exit gate | - [ ] MVP features complete - [ ] Definition of Done met for every task - [ ] Staging site/app works |
| Target dates | [FILL] |

## Phase 5 - Quality and Hardening
| Item | Details |
|---|---|
| Goal | Find and fix problems before customers do |
| Work | Section 18 checklists; performance (Section 13); security review; accessibility audit |
| AI agent helps with | Test generation, regression runs, log review |
| Exit gate | - [ ] No Blocker bugs - [ ] No Major accessibility issues - [ ] Budgets met |
| Target dates | [FILL] |

## Phase 6 - Private Beta (first 10-50 people)
| Item | Details |
|---|---|
| Goal | Learn from friendly real users |
| Work | Invite list, onboarding check, feedback form, weekly check-ins |
| AI agent helps with | Grouping feedback into themes, drafting replies |
| Exit gate | - [ ] 70%+ of beta users complete first key action - [ ] Top 10 issues fixed |
| Target dates | [FILL] |

## Phase 7 - Public Launch
| Item | Details |
|---|---|
| Goal | Product open to everyone |
| Work | Section 21 checklist; app store submission; landing page; announcement; support ready |
| AI agent helps with | Launch copy drafts, FAQ drafts, monitoring alerts |
| Exit gate | - [ ] Launch checklist 100% - [ ] Rollback plan ready |
| Target dates | [FILL] |

## Phase 8 - Growth to Customers 1-500
Use milestones. At each, repeat the loop in Section 22.

| Milestone | Customers | Main focus | Design system work |
|---|---|---|---|
| M1 | 1-10 | Talk to every customer; fix onboarding blockers | Quick fixes, record patterns that confuse |
| M2 | 11-50 | Find the first value moment; reduce time to it | Simplify onboarding components; add missing states |
| M3 | 51-100 | Stability and support load | Stabilize components; accessibility fixes; help content |
| M4 | 101-250 | Retention and word of mouth | Settings, notifications, empty-state improvements; performance tuning |
| M5 | 251-500 | Repeatable growth and pricing clarity | Scale patterns; release design system v1.0; clean up deprecated items |

| Milestone exit check | Your answer |
|---|---|
| Customers reached (date) | [FILL] |
| Activation rate | [FILL] |
| Biggest complaint | [FILL] |
| Biggest compliment | [FILL] |
| Next decision | [FILL] |

---

# 21. LAUNCH READINESS CHECKLIST  [TODO]

Check every box. Any unchecked item must have an owner and a date.

**Product and design**
- [ ] All MVP screens match the design system
- [ ] Empty, loading, error states exist everywhere
- [ ] Accessibility audit passed (Section 10)
- [ ] Performance budgets met (Section 13)

**Trust and legal**
- [ ] Privacy policy, terms and cookie notice live
- [ ] Data deletion and export path exist (if required where you operate)
- [ ] Payment, tax and refund text reviewed
- [ ] Licenses for fonts, icons, images confirmed

**Operations**
- [ ] Error monitoring and alerts on
- [ ] Backups tested
- [ ] Support email or chat ready; reply target set: [FILL]
- [ ] Help center or FAQ written
- [ ] Rollback plan written and tested

**Marketing**
- [ ] Landing page live and tested on phone
- [ ] Email welcome sequence tested
- [ ] Social images and launch posts ready
- [ ] App store listing approved (if mobile)

**Measurement**
- [ ] Analytics events verified with test data
- [ ] Dashboard for Section 19.2 numbers ready

**People**
- [ ] Everyone knows who decides "go / no-go": [FILL]
- [ ] Launch day on-call person: [FILL]

---

# 21A. LEGAL, COMPLIANCE AND DATA PRIVACY  [TODO]

> This section helps you ask the right questions. It is **not legal advice**. Have a qualified lawyer review anything involving payments, children, health, finance or user data before launch.

## 21A.1 Where and who
| Question | Your answer | Example |
|---|---|---|
| Company legal name and country | [FILL] | Acme Ltd, UK |
| Countries your customers live in | [FILL] | US, UK, EU |
| Do you serve children under 13 (or 16)? | [FILL] | No; 18+ only |
| Do you handle health, financial or other sensitive data? | [FILL] | Financial: invoices only |
| Do you take payments yourself or via a provider? | [FILL] | Provider (Stripe) |

## 21A.2 Laws and rules that may apply (tick those that apply)
| Rule | Applies? | What it affects in design |
|---|---|---|
| GDPR (EU/UK) | [ ] | Consent, access, delete, export, privacy notice |
| CCPA/CPRA (California) | [ ] | "Do not sell or share" choice, data rights requests |
| COPPA (US children under 13) / age-appropriate design codes | [ ] | Age gate, parental consent, limited data |
| ePrivacy / cookie laws | [ ] | Cookie banner, tracking consent |
| Accessibility laws (ADA, Section 508, EN 301 549, European Accessibility Act) | [ ] | Meeting Section 10 |
| Payment rules (PCI DSS, strong customer authentication) | [ ] | Never store card numbers yourself; use provider fields |
| Consumer protection and auto-renewal laws | [ ] | Section 8A.4 honest design, cancel flow |
| Email and SMS rules (CAN-SPAM, CASL, TCPA) | [ ] | Consent, unsubscribe, sender identity |
| Industry rules (HIPAA, financial, education) | [ ] | [FILL] |
| App store rules (Apple, Google) | [ ] | Privacy labels, in-app purchase rules, account deletion |
| AI-related rules (disclosing AI use, content labeling) | [ ] | Tell users when they talk to AI or see AI output |
| Other: [FILL] | [ ] | [FILL] |

## 21A.3 Data map
| Data we collect | Why | Where stored | Who can see it | How long kept | User can delete? |
|---|---|---|---|---|---|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Example: Email address | Log in, receipts | Auth provider | Support, owner | Until account deleted | Yes |

## 21A.4 Required screens and texts
| Item | Where it appears | Owner | Done? |
|---|---|---|---|
| Privacy policy | Sign-up, footer, store listing | [FILL] | [ ] |
| Terms of service | Sign-up, footer | [FILL] | [ ] |
| Cookie and tracking choices | First visit | [FILL] | [ ] |
| Consent checkboxes (never pre-ticked) | Sign-up, marketing | [FILL] | [ ] |
| Data export and delete | Settings | [FILL] | [ ] |
| Age check (if needed) | Sign-up | [FILL] | [ ] |
| Security notice for breaches | Process document | [FILL] | [ ] |

## 21A.5 Security basics for design and build
- [ ] Passwords never shown in plain text unless user taps "show"
- [ ] Two-step login offered for important accounts
- [ ] No personal data in URLs, logs or analytics properties
- [ ] Rate limits and lockout messages that do not reveal whether an account exists
- [ ] Least-access rule: people and agents get only what they need
- [ ] Backups and a written breach plan: [FILL link]

## 21A.6 Sign-off
| Reviewer | Role | Date | Notes |
|---|---|---|---|
| [FILL] | Lawyer or advisor | [FILL] | [FILL] |

---

# 22. CUSTOMER FEEDBACK AND ITERATION LOOP  [TODO]

## 22.1 Where feedback comes from
| Source | How collected | Reviewed how often |
|---|---|---|
| Support messages | [FILL] | [FILL] |
| In-app feedback button | [FILL] | [FILL] |
| Interviews (aim 3-5 per week early on) | [FILL] | [FILL] |
| Analytics funnels | [FILL] | [FILL] |
| App store reviews | [FILL] | [FILL] |

## 22.2 The loop
1. **Collect** feedback in one list.
2. **Group** into themes (AI agent may draft; a human confirms).
3. **Score** each theme: How many users? How bad? How easy to fix?
4. **Decide** the top 3 to fix this cycle.
5. **Change** the design system first if the issue is a shared pattern.
6. **Release** and tell customers.
7. **Measure** whether the number in Section 19.2 moved.

## 22.3 Design debt list
| Issue | Where | Impact | Planned fix date |
|---|---|---|---|
| [FILL] | [FILL] | [FILL] | [FILL] |

---

# 22A. CUSTOMER SUCCESS AND SUPPORT OPERATIONS  [TODO]

**Goal:** every one of your first 500 customers reaches their first win quickly and gets help fast.

## 22A.1 Customer journey and touchpoints
| Stage | Customer goal | What we send or show | Channel | Owner |
|---|---|---|---|---|
| Discover | Understand what it is | Landing page, demo | Web | [FILL] |
| Sign up | Create account | Welcome screen, welcome email | App, email | [FILL] |
| Activate | Reach first win | Guided first step, checklist | App | [FILL] |
| Day 1-3 | Build the habit | Tip email, check-in | Email, in-app | [FILL] |
| Week 2 | See value | "Here is what you achieved" | Email | [FILL] |
| Before trial ends / renewal | Decide | Reminder with clear price | Email | [FILL] |
| At risk (inactive) | Come back | Friendly nudge, not guilt | Email | [FILL] |
| Cancel | Leave smoothly | Cancel flow, short survey | App | [FILL] |
| Advocate | Tell others | Referral or review ask | Email, in-app | [FILL] |

## 22A.2 Support setup
| Question | Your answer | Example |
|---|---|---|
| Support channels | [FILL] | Email and in-app chat |
| Support hours and time zone | [FILL] | Mon-Fri 9-18 UTC |
| First reply target | [FILL] | Within 4 working hours |
| Fix or answer target | [FILL] | Within 2 working days |
| Language(s) supported | [FILL] | English |
| Who answers? | [FILL] | Founder first; AI agent drafts, human sends |
| Where tickets live | [FILL] | [FILL] |

## 22A.3 Ticket categories and priority
| Category | Example | Priority | Response target |
|---|---|---|---|
| Cannot log in or pay | Locked out | Urgent | [FILL] |
| Bug | Button does nothing | High | [FILL] |
| How do I... | Question | Normal | [FILL] |
| Feature request | Idea | Low | [FILL] |
| Billing | Refund | High | [FILL] |
| Privacy request | Delete my data | Urgent (legal deadline) | [FILL] |

## 22A.4 Help content
| Item | Done? | Link |
|---|---|---|
| FAQ (top 10 questions) | [ ] | [FILL] |
| Getting started guide | [ ] | [FILL] |
| Short video or GIF walk-throughs | [ ] | [FILL] |
| Status page for outages | [ ] | [FILL] |
| Contact page with real human contact | [ ] | [FILL] |
| Changelog / "What's new" | [ ] | [FILL] |

## 22A.5 Rules for replies
- Say sorry once, then fix.
- Use the customer's name and own words.
- Give the next step and the time it will take.
- Never say "as I said" or blame the customer.
- Save any new answer into the help center within 48 hours.
- Tag every ticket with a theme so Section 22 can count them.

## 22A.6 Customer health tracking
| Signal | Healthy | At risk | Action |
|---|---|---|---|
| First key action within [FILL] days | Yes | No | Personal email or guided prompt |
| Logins per week | [FILL] | [FILL] | [FILL] |
| Support tickets | [FILL] | [FILL] | [FILL] |
| Payment failed | No | Yes | Retry message (Section 8A.3) |

## 22A.7 Founder-led learning for the first 500
- Talk to the first [FILL] customers personally (recommended: 20).
- Keep a "customer quotes" list; the best ones go to the landing page **with permission**.
- Review the top 3 pain points every [FILL] (Example: Friday) and update Section 22.3.

---

# 23. RISKS AND ASSUMPTIONS  [TODO]

| # | Risk or assumption | Likelihood (L/M/H) | Impact (L/M/H) | What we will do | Owner |
|---|---|---|---|---|---|
| 1 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Example | Users will not understand the dashboard | M | H | Test with 5 people before build | Priya |

---

# 24. OPEN QUESTIONS  [TODO]

Anything unknown goes here. Nobody guesses.

| # | Question | Asked by | Owner | Due | Answer |
|---|---|---|---|---|---|
| 1 | [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |

---

# 25. DECISION LOG  [TODO]

Write every important choice so nobody argues about it twice.

| Date | Decision | Why | Options rejected | Decided by |
|---|---|---|---|---|
| [FILL] | [FILL] | [FILL] | [FILL] | [FILL] |
| Example 2026-10-17 | Use Inter font | Free, readable, fast | Roboto, Poppins | Priya |

---

# 26. FINAL COMPLETENESS CHECKLIST  [TODO]

Before you call this document `[DONE]`, tick every box:

- [ ] No `[FILL]` is left anywhere (search the file)
- [ ] Every section has a status tag
- [ ] Every color passes contrast
- [ ] Every MVP component has a spec with all states
- [ ] A person who never saw the project could build a screen from this file alone
- [ ] An AI agent given only this file would not need to guess colors, text or behavior
- [ ] Section 20 shows the current phase and dates
- [ ] Open questions in Section 24 are answered or have an owner and due date
- [ ] Version and date in Section 0 are updated
- [ ] Product type chosen in Section 1.1
- [ ] Pricing and money rules written (Section 8A) or marked N/A
- [ ] Laws checked and legal reviewer named (Section 21A)
- [ ] Agent roles and human approval gates defined (Section 15A)
- [ ] Support hours, targets and help content ready (Section 22A)
- [ ] Another person has reviewed it

**Final test (the "10-year-old test"):** hand the file to someone new. If they cannot tell what to do next in any section, rewrite that section in simpler words.

---

# 27. CHANGELOG  [TODO]

| Version | Date | Who | What changed |
|---|---|---|---|
| 0.1.0 | [FILL] | [FILL] | First draft from master template |
| Template 1.1 | 2026-10-17 | Template author | Added Sections 1.1, 8A, 15A, 21A, 22A |
