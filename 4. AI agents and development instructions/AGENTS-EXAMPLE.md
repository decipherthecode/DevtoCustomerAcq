# AGENTS-EXAMPLE.md: a completed sample (fictional product "Tiny Tasks")

> **How to use this:** This shows what a well-filled `AGENTS.md` looks like. Every name, link and number is made up. It shows the *key* sections filled in; your real file keeps all sections from the template. Notice three things: answers are short, commands are exact, and unknowns say `UNKNOWN`.

---

# AGENTS.md: Tiny Tasks

**Last updated:** 2026-10-17 | **Owner:** Asha Rao | **Status:** Building

## 1. PROJECT CARD
| Question | Your answer |
|---|---|
| Product name | Tiny Tasks |
| One-sentence description | A weekly planner for busy parents that builds a family to-do plan in under 2 minutes. |
| The problem it solves | Parents lose track of school, chores and appointments across chats and sticky notes. |
| Who is the customer? | Working parents of kids aged 5-12 in the US and India |
| Platforms | Web + Mobile (web first, Android second, iOS later) |
| Business model | Subscription |
| Price (if any) | $4/month or $36/year; 14-day free trial |
| Main goal for this phase | Launch and get the first 500 paying users |
| Target launch date | 2027-02-15 |
| Budget limit for tools and services | $150 per month max |
| Repository link | https://example.com/tinytasks (fake) |
| Live product link | not live yet |

## 2. AGENT PERMISSIONS (custom lines added)
- ✅ Add your own: update test snapshots only when the task is about UI text.
- ⚠️ Add your own: any change to the reminder-sending code (it can text real parents).
- ⛔ Add your own: never touch `legacy-import/`; it is being deleted by a human.

## 3. ROLES
| Job | Name | What they decide |
|---|---|---|
| Product owner | Asha Rao | Scope, priorities, launch go/no-go |
| Builder | Asha Rao + AI agent | How to build it |
| Quality checker | Asha Rao (+ one friend, Dev, on real phones) | Is it good enough to ship? |
| Launch owner | Asha Rao | When and how it goes live |
| Customer support owner | Asha Rao | Replies to users |
| Emergency contact | Asha Rao, asha@example.com (fake) | Whether to roll back |

## 4. WHAT WE ARE BUILDING
**4.1 The customer**
- **Who:** A parent with two kids who works full time.
- **Their situation:** Sunday night, trying to plan the week while tired.
- **How they solve it today:** A paper calendar plus a family chat group.
- **Why ours is better:** One tap turns messy notes into a week plan everyone can see.

**4.2 Version 1 must-haves**
| # | Feature | A user can... | Priority |
|---|---|---|---|
| 1 | Sign up | A user can create an account with email and password. | Must |
| 2 | Add tasks | A user can add a task with a day and a person. | Must |
| 3 | Week view | A user can see all tasks for the week on one screen. | Must |
| 4 | Reminders | A user can get a reminder the evening before a task. | Should |

**4.3 Not now:** shared family accounts, school-calendar import, dark mode, iOS app.

**4.4 Success numbers**
| Measure | Target | When |
|---|---|---|
| Sign-ups | 1,500 | 2027-05-15 |
| People who finish setup (activation) | 50% add 5+ tasks in week 1 | 2027-05-15 |
| Paying customers | 500 | 2027-05-15 |
| Still using after 30 days | 40% | 2027-05-15 |

## 6. TECH STACK (excerpt)
| Part | Choice and version |
|---|---|
| Language(s) | TypeScript 5.6 |
| Web framework | Next.js 15 |
| Mobile framework | React Native (Expo) 52 |
| Database | PostgreSQL via Supabase |
| Payments | Stripe (test mode locally) |
| Hosting | Vercel |
| Package manager | pnpm |

## 7. COMMANDS (excerpt)
| Job | Command |
|---|---|
| Install everything | `pnpm install` |
| Start the app locally | `pnpm dev` |
| Run all tests | `pnpm test` |
| Run one test file | `pnpm test path/to/file.test.ts` |
| Check code style (lint) | `pnpm lint` |
| Check types | `pnpm typecheck` |
| Build for production | `pnpm build` |
| Run database migrations | `pnpm db:migrate` ⚠️ ask first |

## 8.1 Must always work
1. Sign up and log in
2. Add a task and see it in the week view
3. Pay for a subscription and cancel it
4. Receive the evening reminder

## 10. ENVIRONMENTS AND ROLLBACK
| Environment | Link | Who may deploy |
|---|---|---|
| Local | localhost:3000 | Agent ✅ |
| Staging | staging.example.com (fake) | Agent ⚠️ ask first |
| Production | example.com (fake) | Human only |

**Rollback:** Open the Vercel dashboard → Deployments → choose the previous green deployment → Redeploy. Database changes are never rolled back by the agent; tell Asha.

## 13. THE ROAD TO 500
**Our definition of "customer":** a person who has paid for at least one month.

| Milestone | Date goal | How we will find them | Gate to move on |
|---|---|---|---|
| 0 → 10 | 2027-02-28 | Friends, school parent groups | 7 of 10 reach the first win |
| 10 → 50 | 2027-03-15 | Local parent communities, 10 interviews | 5 paying |
| 50 → 100 | 2027-03-31 | Short how-to videos, referrals | One channel brings 30%+ of sign-ups |
| 100 → 250 | 2027-04-30 | Parent bloggers, SEO articles | Support under 1 hour/day |
| 250 → 500 | 2027-05-15 | Repeat what works | 500 reached and 30-day retention stable |

**13.4 Money tracker (excerpt)**
| Item | Provider | Cost per month | Monthly cap |
|---|---|---|---|
| Hosting | Vercel | $20 | $30 |
| Database | Supabase | $25 | $40 |
| Email / SMS | (reminders) | $10 | $25 |
| Marketing / ads | none for now | $0 | $40 |
| **Total** | | **$55** | **$135 (budget $150)** |

## 17. DECISIONS, ASSUMPTIONS AND OPEN QUESTIONS
| Date | Type | What | Who | Status |
|---|---|---|---|---|
| 2026-10-20 | Decision | Web first; Android after 100 customers | Asha | Done |
| 2026-10-18 | Question | Which SMS provider supports India and the US? | Asha | Open |
| 2026-10-17 | Approval | Approved to build Version 1 | Asha | Done |

> **What makes this good:** No empty brackets. Unknown things are written down as Open Questions, so the agent asks rather than guesses.
