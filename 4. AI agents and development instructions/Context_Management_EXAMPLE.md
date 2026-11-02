# EXAMPLE: A FULLY FILLED CONTEXT_MANAGEMENT FILE

> This is a **sample** for a made-up app called **PlantPal**. All names, numbers, and links are fictional. It shows what a good, filled file looks like. Copy the structure, not the facts.
> It follows the same section numbers as `Context_Management.md` v1.1.

---

## 1. Document Control

| Field | Answer |
|---|---|
| Project name | PlantPal |
| Owner | Sam Lee (solo founder) |
| Created / Last updated | 2026-10-17 / 2026-10-24 |
| Template version | 1.1 |
| Status | Active |
| Repo | github.com/sam-lee/plantpal (fictional) |
| Memory file | /docs/Project_Memory.md |

## 2. Project Snapshot

| Field | Answer |
|---|---|
| What is it? | A web app and phone app that reminds people to water their houseplants. |
| Problem | People forget to water plants, and plants die. |
| For whom | Busy city adults, 22 to 40, with 3 or more plants. |
| Product type | Web app first, then iPhone and Android |
| Money | Free for up to 5 plants; Pro is $4/month for unlimited plants |
| Success | 500 people using it every week |
| Biggest worry | People may stop using it after week 1 |
| NOT building | Plant shop, social network, plant disease scanner |

## 3. Lifecycle

- **Current phase:** 2 (Build the MVP). Started 2026-10-19. Target end 2026-11-30.
- Phases 0 and 1 are done (14 people interviewed; MVP list frozen on 2026-10-17).
- **Today's hat:** Developer.

## 4. Source of Truth

| Topic | Link |
|---|---|
| Requirements | /docs/requirements.md |
| Designs | Figma file "PlantPal v1" |
| Task board | Notion "PlantPal Board" |
| Diary and decisions | /docs/Project_Memory.md |

Conflict winner order: my chat message → this file → requirements → architecture → code comments.

## 5. Rules for AI Helpers (short version)

- **Start:** read this file + latest diary entry; repeat back project, phase, today's task; ask about any `[UNKNOWN]`.
- **End:** write a diary entry (done, files, not finished, next step).
- 🟢 **Freely:** write code for today's task, add tests, fix typos.
- 🟡 **Ask first:** new libraries, database changes, design changes, anything that costs money.
- 🔴 **Never:** delete customer data, show keys, push to live directly, invent numbers.
- **Answer style:** simple words; short answer first; numbered steps; always say what changed and how to test it.

## 6. Context Hygiene

- **Tier 1 (always):** this file, today's task, latest diary entry.
- **Tier 2 (when needed):** /docs/architecture.md, /docs/data-model.md, /docs/test-plan.md.
- **Tier 3 (archive):** /docs/archive/.
- **Never load:** `.env`, customer exports.
- Limits: this file under 700 lines; diary entries under 15 lines; keep the last 10 entries.

## 7. Tech Stack

| Area | Choice |
|---|---|
| Front end | React + TypeScript |
| Phone app | React Native (Phase 6+) |
| Back end | Node.js |
| Database + login | Supabase (PostgreSQL + Auth) |
| Payments | Stripe |
| Hosting | Vercel |
| Email | Resend |
| Analytics | PostHog |
| Errors | Sentry |

Environments: local `localhost:3000`; staging `staging.plantpal.example`; live `plantpal.example` (fictional).
Commands: install `npm install`; start `npm run dev`; test `npm test`; deploy to staging `npm run deploy:staging`.

## 8. Current Focus

| Field | Answer |
|---|---|
| Today's goal | Let a user add a plant with a name and photo |
| Why | It is the core MVP feature (F-002) |
| Done looks like | Plant appears on the list; test passes; photo limit 5 MB |
| Files | src/pages/AddPlant.tsx, src/api/plants.ts |
| Do NOT touch | Payment code |
| Deadline | 2026-10-20 |

Board: T-001 Add-plant form (Now) · T-002 Watering schedule picker (Next) · T-003 Reminder email (Next) · T-004 Pro plan checkout (Later).

## 9. Weekly Rhythm

Monday 9:00 plan (30 min) · Wednesday check (10 min) · Friday 16:00 review + look-back (35 min).
Week of 2026-10-19 goal: *"A user can sign up, add a plant, and see it on a list."*

## 10. Requirements (MVP)

| ID | Feature | Priority | Done when |
|---|---|---|---|
| F-001 | Sign up with email | Must | Account created; welcome email arrives |
| F-002 | Add a plant (name, photo) | Must | Plant shows on list |
| F-003 | Pick watering days | Must | Schedule saved |
| F-004 | Get a reminder email | Must | Email arrives on the right day |
| F-005 | Pro plan checkout | Should | Test payment works |

Journey: open app → add plant → pick days → get reminder.
Targets: opens in under 2 seconds; Chrome/Safari latest 2 versions; iOS 16+; Android 11+; English only; 99% uptime.

## 11. Quality Checks

- Automatic tests must pass before saving code. Manual checklist: /docs/test-plan.md.
- Launch blocker: any open Critical or High bug.
- Tested by: Sam + 3 friends.
- "Done" = works, tests pass, no new log errors, works on phone and computer, diary entry written.

## 12. Security & Privacy

- Secrets only in `.env`, never in code or chat.
- Stored: email, plant names, photos. **Never stored:** card numbers (Stripe holds them).
- Backups: daily; restore tested monthly.
- Data leak plan: tell customers within 72 hours.

## 13. Legal & Compliance (progress)

Privacy Policy ☑ · Terms ☑ · Cookie notice ☐ (Phase 5) · GDPR/CCPA review ☐ (Phase 5) · Under-13 users: not allowed, 13+ in Terms ☑ · App Store rules read ☐ (Phase 3). *(Reminder: ask a qualified lawyer.)*

## 14. Architecture Summary

Users open the web app → it calls the API → the API reads/writes Supabase → a daily job sends reminder emails.

## 15. Release & Launch

- Merge to `main` → auto-deploy to staging → I check → promote to live.
- Rollback: redeploy the previous version in Vercel.
- Phone store review: allow 3 to 7 days.
- Launch checklist: see template Section 15.2.

## 16. Customer Growth (target numbers)

20 sign-ups/week · 60% add a plant · 40% weekly active · 25% still here at week 4 · 5% pay.

## 17. Support Playbook (short)

support@plantpal.example · reply within 24 hours on weekdays · refund in full within 14 days · the AI drafts, **Sam sends** · never promise feature dates.
P1 (app down, wrong charge): reply in 1 hour. P2: fix this week. P3: add to board. P4: add to feedback log.

## 18. Budget

| Cost | Monthly |
|---|---|
| Hosting (Vercel) | $20 |
| Database (Supabase) | $25 |
| AI tools | $40 |
| Email (Resend) | $0 |
| Domain | $2 |
| **Total** | **$87** |

Hard cap: $120/month. The AI never starts anything that costs money without Sam's "yes".

## 19. Prompt Library

Uses the standard prompts from the template (Start session, End session, Plan a task, Build a feature, Fix a bug, Review, Reply to customer, Weekly look-back, Launch check, Shrink context), plus one custom prompt:
`Check every plant-photo upload path for the 5 MB limit and list any path that skips it.`

## 20. Glossary

| Word | Meaning |
|---|---|
| Plant | One item a user is tracking |
| Reminder | One email telling a user to water a plant |
| Pro | The paid plan |

## 21. Change Log

| Date | Version | Change |
|---|---|---|
| 2026-10-17 | 0.1 | Created from template |
| 2026-10-24 | 0.2 | Filled Sections 1 to 12 |

## 22. Ready-to-use check

All required sections filled ☑ · diary file has an entry ☑ · no secrets present ☑ · AI repeated back project and task correctly ☑
