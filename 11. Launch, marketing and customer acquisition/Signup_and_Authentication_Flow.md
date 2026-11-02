# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

> **Template version:** 2.0 (draft) | **Last standards check:** October 2026
> **What this file is:** a worksheet that explains, in plain words, how a person **signs up**, **logs in**, **stays safe**, and **gets started** in your product. It covers everything from the first line of code until your **first 500 customers** are using the product.
> **Who reads it:** you, your team, your testers, and your **AI coding agents**.
> **Why it matters:** if an answer is missing, someone (or an AI) will **guess**. Guesses cause bugs. Every blank you fill removes one guess.

---

## 0.1 The 6 simple rules

1. **Answer every question.** If it does not apply, write `N/A – because <reason>`. If you do not know yet, write `TBD – who: <name> – by: <date>`.
2. **Use simple words.** Write like you are talking to a friend.
3. **Tick boxes** by changing `☐` to `☒`. Example: `☒ Email + password`.
4. **Write your answers on the `👉` lines.** Do not delete the questions.
5. **Use numbers, not feelings.** Write "within 10 minutes", not "quickly".
6. **Say it once.** If an answer is already somewhere else, write `See Section X`.

## 0.2 What the symbols mean

| Symbol | Meaning |
|---|---|
| 🔴 | **MUST** answer before building starts |
| 🟡 | **SHOULD** answer before launch (a safe default is usually given) |
| 🟢 | **LATER**: can wait until after your first 100 customers |
| ☐ / ☒ | Empty box / ticked box |
| 👉 | Write your answer here |
| 💡 | Hint, or a safe starting answer |
| ✅ **Example** | A sample answer so you can see what "good" looks like |
| ⚠️ | A common mistake |
| 🤖 | A note for AI agents |

## 0.3 The 6 phases of the journey

| Phase | Name | What happens | You are done when |
|---|---|---|---|
| **P0** | Plan | Decide what you are building and for whom | Sections 1–3 answered |
| **P1** | Design | Decide screens, rules, emails, security | Sections 4–23 answered |
| **P2** | Build | People and AI agents write the code | Section 27 followed |
| **P3** | Test | Check it works and is safe | Section 24 passed |
| **P4** | Launch | Product goes live | Section 25 all ticked |
| **P5** | Grow to 500 | First 500 customers sign up and get value | Section 26 reached |

## 0.4 Progress tracker (update as you go)

Change the status to `Not started`, `In progress`, or `Done`.

| # | Section | Phase | Priority | Status |
|---|---|---|---|---|
| 0 | Document control (0.7) | P0 | 🔴 | Not started |
| 1 | Product basics and goals | P0 | 🔴 | Not started |
| 2 | Who signs up | P0 | 🔴 | Not started |
| 3 | Sign-up and login methods | P0 | 🔴 | Not started |
| 4 | Signup screen and fields | P1 | 🔴 | Not started |
| 5 | Verification | P1 | 🔴 | Not started |
| 6 | Login and sessions | P1 | 🔴 | Not started |
| 7 | Passwords and reset | P1 | 🔴 | Not started |
| 8 | Social login | P1 | 🟡 | Not started |
| 9 | Passwordless (links, codes, passkeys) | P1 | 🟢 | Not started |
| 10 | Extra protection (MFA, SSO) | P1 | 🟡 | Not started |
| 11 | Recovery, lockouts, changes | P1 | 🔴 | Not started |
| 12 | Roles and teams | P1 | 🟡 | Not started |
| 13 | Waitlist, invites, referrals | P1 | 🟡 | Not started |
| 14 | Onboarding and activation | P1 | 🔴 | Not started |
| 15 | Emails and messages | P1 | 🔴 | Not started |
| 16 | Security and abuse prevention | P1 | 🔴 | Not started |
| 17 | Legal, privacy, compliance | P1 | 🔴 | Not started |
| 18 | Technical setup | P1 | 🔴 | Not started |
| 19 | Platform notes | P1 | 🟡 | Not started |
| 20 | Analytics and funnel | P1–P5 | 🔴 | Not started |
| 21 | Support and operations | P1–P5 | 🟡 | Not started |
| 22 | Error messages and edge cases | P1 | 🔴 | Not started |
| 23 | Accessibility and language | P1 | 🟡 | Not started |
| 24 | Testing | P3 | 🔴 | Not started |
| 25 | Launch checklist | P4 | 🔴 | Not started |
| 26 | First 500 customers | P5 | 🔴 | Not started |
| 27 | AI Agent Instructions | P2 | 🔴 | Not started |
| 28 | Risks, questions, decisions | All | 🟡 | Not started |
| 29 | Sign-off and change log | All | 🔴 | Not started |

**Overall progress:** ____ of 29 sections done. Next section to do: ____

## 0.5 Quick start (15 minutes)

Short on time? Answer only the 🔴 items in Sections 1–4 first. Then ask an AI to interview you for the rest using the prompt in **0.6**.

## 0.6 Copy-and-paste AI interview prompt

Paste everything inside the box into any AI assistant, then attach this file. The AI will ask you one simple question at a time and fill the document for you.

```text
You are a friendly Senior Product Architect and Technical Writer.
I am attaching a template called "Signup_and_Authentication_Flow.md".
Help me fill it in.

Rules:
1. Ask me ONE simple question at a time, in plain words a 10-year-old can follow.
2. Go in order, section by section. Do the 🔴 items first, then 🟡, then 🟢.
3. For each question, give 2–3 example answers or a safe default I can accept by saying "yes".
4. If my answer is vague (like "fast" or "secure"), ask me for a number or a clear choice.
5. If my answers contradict each other, point it out and ask which one is right.
6. Never invent facts about my product. If I don't know, write "TBD – who – by when".
7. Never ask me for real passwords, API keys, or secrets. Tell me to keep those out of the file.
8. After each section, show me the filled section and ask "Is this right?".
9. At the end, check Section 29.1 and list anything still missing.
10. Output the final document as one Markdown file with the same headings.

Start by asking me for my product name and what it does in one sentence.
```

## 0.7 Document control 🔴

| Field | 👉 Answer |
|---|---|
| Project name | |
| Document owner (one person) | |
| Date started | |
| Current phase (P0–P5) | |
| Reviewers (name + role) | |
| Code location (link) | |
| Design location (link) | |
| Task tracker (link) | |

✅ **Example:** Project: WalkMyDog · Owner: Priya · Started: 2026-11-01 · Phase: P0 · Code: github.com/example/walkmydog

## 0.8 Mini glossary

| Word | Plain-English meaning |
|---|---|
| **Signup** | Making a new account for the first time |
| **Login** | Going into an account you already have |
| **Authentication** | Proving "I am who I say I am" |
| **Authorization** | Deciding "what you are allowed to do" |
| **Session** | The time you stay logged in without typing your password again |
| **Token** | A secret digital key the app gives you after login |
| **Verification** | Checking that the email or phone really belongs to the person |
| **MFA / 2FA** | A second proof (like a code on your phone) on top of the password |
| **OTP** | A short code that works only once |
| **Magic link** | A login link sent by email. Click it and you are in |
| **Passkey** | Logging in with fingerprint, face, or phone lock instead of a password |
| **OAuth / social login** | "Continue with Google / Apple" |
| **SSO** | One company login for many apps |
| **Rate limit** | A rule like "only 5 tries per minute" that stops attackers |
| **CAPTCHA / bot check** | A test that tells humans and robots apart |
| **Activation** | The moment a new user first gets real value |
| **Funnel** | The steps from "visited" to "signed up" to "activated" |
| **Acceptance criteria** | A pass/fail sentence that proves something works |
| **PII** | Personal info (name, email, phone, address) that must be protected |

## 0.9 Standards this template follows (checked October 2026)

| Topic | What the template uses | Where to verify |
|---|---|---|
| Passwords | Length matters more than symbols. NIST SP 800-63B-4 (final, Aug 2025): at least 15 characters when a password is the **only** login step, allow at least 64, no forced symbol rules, no forced regular changes, block known-leaked passwords | NIST SP 800-63B-4 |
| Login safety | Rate limits, MFA, neutral error messages, secure sessions | OWASP Authentication & Session Management Cheat Sheets, OWASP Top 10 (Authentication Failures) |
| iOS apps | If you offer Google/Facebook-style login for the main account, Apple Guideline 4.8 requires an equivalent privacy-focused option. Sign in with Apple is the option known to satisfy it | Apple App Review Guidelines, 4.8 |
| Accessibility | WCAG 2.2 AA, including 3.3.8 *Accessible Authentication*: no memory or puzzle tests without an alternative; allow pasting and password managers | W3C WCAG 2.2 |
| Privacy law | Check each region where you have users (GDPR/UK GDPR, CCPA/CPRA, COPPA, CAN-SPAM, CASL) | Official regulator sites + a lawyer |

⚠️ Standards change. Re-check this table at least once a year and before each major launch. This is a planning guide, **not legal or security advice**.

---

# PART A: PLAN (P0)

## 1. Product basics and goals 🔴 `[P0]`

**1.1 In one sentence, what does your product do?**
✅ **Example:** "A phone app where dog owners book trusted local walkers in two minutes."
👉 Answer:

**1.2 Who is it for? (one sentence)**
✅ **Example:** "Busy city dog owners who work long hours."
👉 Answer:

**1.3 Product type (tick all):**
☐ Website / web app ☐ iOS app ☐ Android app ☐ SaaS (monthly plan) ☐ Marketplace (buyers + sellers) ☐ Consumer / social app ☐ Other: ______

**1.4 Why does a person need an account at all?** 🔴
☐ To save their data ☐ To pay ☐ To talk to other users ☐ To protect private info ☐ Legal rule ☐ Other: ______
👉 Can people try the product **before** making an account? ☐ Yes (what can they do? ______) ☐ No
💡 Fewer forced signups = more users.

**1.5 What does success look like?** 🔴

| Goal | 👉 Your target | 💡 Safe starting number |
|---|---|---|
| Customers to reach | 500 | 500 |
| Date to reach 500 | | |
| % of visitors who start signup | | 10% |
| % who start signup and finish it | | 60% or more |
| % of new users who become "activated" | | 40% or more |
| Longest acceptable signup time | | 60 seconds |

**1.6 Where will the first 500 customers come from?** 🟡
☐ Friends / network ☐ Waitlist ☐ Social media ☐ Search engines ☐ Paid ads ☐ Communities / forums ☐ Partners ☐ Launch sites ☐ Cold outreach ☐ Other: ______
👉 Main channel and why:
✅ **Example:** "Local dog-owner Facebook groups, because that is where our first 100 users already talk."

## 2. Who signs up 🔴 `[P0]`

**2.1 List every kind of person who will have an account.**

| Role name | Who they are | Can sign up alone? | Special rules |
|---|---|---|---|
| ✅ Customer | Dog owner | ☒ Yes ☐ No | Must be 18+ |
| | | ☐ Yes ☐ No | |
| | | ☐ Yes ☐ No | |

**2.2 Is there an admin (your team) who manages users?** ☐ Yes ☐ No
👉 What can admins do?
✅ **Example:** "Block a user, send a password reset, see the user list. Cannot see passwords."

**2.3 Minimum age to sign up:** ☐ 13 ☐ 16 ☐ 18 ☐ Other: ____ ☐ No limit
⚠️ If children might use the product, extra laws apply. See Section 17.

**2.4 One account = one person, or shared team accounts?**
☐ One person ☐ Teams (see Section 12) ☐ Both
👉 Answer:

## 3. Choose sign-up and login methods 🔴 `[P0]`

**3.1 Fill the table.**

| Method | Offer it? | Why or why not | Launch or later? |
|---|---|---|---|
| Email + password | ☐ Yes ☐ No | | |
| Continue with Google | ☐ Yes ☐ No | | |
| Continue with Apple | ☐ Yes ☐ No | | |
| Other social (Facebook / X / LinkedIn / GitHub) | ☐ Yes ☐ No | | |
| Magic link (login link by email) | ☐ Yes ☐ No | | |
| One-time code (email or SMS) | ☐ Yes ☐ No | | |
| Passkey (fingerprint / face) | ☐ Yes ☐ No | | |
| Company login (SSO) | ☐ Yes ☐ No | | |
| Guest use (no account) | ☐ Yes ☐ No | | |

✅ **Example:** Email + password: Yes (everyone has email). Google: Yes (fast). Apple: Yes (needed for iOS). Passkeys: Later.
💡 Beginner-safe default: **Email + password** + **Google** (+ **Apple** if you have an iOS app).
⚠️ **iOS rule (Apple Guideline 4.8):** if you offer Google, Facebook or similar for the main account, you must also offer an equivalent privacy-focused option. Sign in with Apple is the one known to pass. Re-read Apple's current rules before you submit.

**3.2 Main login identity:** ☐ Email ☐ Phone ☐ Username ☐ Other: ______
**3.3 Can one person link several methods to one account?** ☐ Yes ☐ No
👉 If someone signs up with Google, but that email already has a password account, what happens?
☐ Ask them to log in first, then link ☐ Link automatically (only if the email is verified) ☐ Block with a message ☐ Other: ______

**3.4 Which login service will you use?** 🔴 (use a trusted service; do not build security from scratch)
☐ Supabase Auth ☐ Firebase Auth ☐ Auth0 ☐ Clerk ☐ AWS Cognito ☐ Okta ☐ Auth.js ☐ Custom (why: ______) ☐ Not decided (who/when: ______)

---

# PART B: DESIGN THE FLOW (P1)

## 4. Signup screen and fields 🔴 `[P1]`

**4.1 What do you ask at signup?** (Ask as little as possible. Every extra field loses people.)

| Field | Ask? | Required? | Rules | Why we need it |
|---|---|---|---|---|
| Email | ☐ Yes ☐ No | ☐ Yes ☐ No | Looks like name@site.com | |
| Password | ☐ Yes ☐ No | ☐ Yes ☐ No | See Section 7 | |
| Name | ☐ Yes ☐ No | ☐ Yes ☐ No | | |
| Phone | ☐ Yes ☐ No | ☐ Yes ☐ No | | |
| Username | ☐ Yes ☐ No | ☐ Yes ☐ No | | |
| Date of birth / age check | ☐ Yes ☐ No | ☐ Yes ☐ No | | |
| Company / team name | ☐ Yes ☐ No | ☐ Yes ☐ No | | |
| Country / language | ☐ Yes ☐ No | ☐ Yes ☐ No | | |
| "How did you hear about us?" | ☐ Yes ☐ No | ☐ Yes ☐ No | | |
| Terms & Privacy checkbox | ☐ Yes ☐ No | ☐ Yes ☐ No | Starts unticked | |
| Marketing email checkbox | ☐ Yes ☐ No | ☐ Yes ☐ No | Starts unticked | |

✅ **Example:** Email (required), Password (required), First name (required), Terms checkbox (required). Nothing else.

**4.2 Describe the screen(s).**
- Number of screens: ☐ 1 ☐ 2 ☐ 3 ☐ More: ____ · Progress bar? ☐ Yes ☐ No
- Link to the design (Figma, sketch, photo): 👉
- Main button text: 👉 ✅ "Create account"
- Text for people who already have an account: 👉 ✅ "Already a member? Log in"

**4.3 The happy path** 🔴 (what happens when everything goes right; one action per step)
✅ **Example:** 1. Visitor opens the signup page. 2. Types email and password. 3. Presses "Create account". 4. App sends a verification email. 5. Visitor clicks the link. 6. App shows the welcome screen.
👉 Steps:
1.
2.
3.
4.
5.
6.

**4.4 Where does the user land right after signup?** 🔴
👉 Screen name / link:

**4.5 Should anyone be stopped from signing up?**
☐ Block disposable emails ☐ Block some countries ☐ Invite-only ☐ None ☐ Other: ______

## 5. Verification (email / phone) 🔴 `[P1]`

| Question | 👉 Answer |
|---|---|
| Must the user verify their email? | ☐ Yes, before anything ☐ Yes, but they can look around first ☐ No |
| How? | ☐ Click a link ☐ Type a code ☐ Both |
| How long is the link or code valid? | ____ minutes (💡 code 10–15 min; link up to 24 h) |
| Can the user ask for a new one? | ☐ Yes (max ____ per hour) ☐ No |
| Phone verification needed? | ☐ Yes (why: ____) ☐ No |
| What does the user see while waiting? | |
| If the user never verifies | ☐ Delete account after ____ days ☐ Send ____ reminders ☐ Nothing |
| If the email was typed wrong | ☐ Let them change it ☐ Start over |

✅ **Example:** Click-a-link, valid 24 h, resend allowed 3 times per hour, user can browse but not book until verified.

## 6. Login and sessions 🔴 `[P1]`

| Question | 👉 Answer |
|---|---|
| Login fields | ☐ Email ☐ Username ☐ Phone ☐ Password |
| "Remember me" checkbox? | ☐ Yes ☐ No |
| Stay logged in for | Web ____ days, Mobile ____ days (💡 7–30) |
| Log out automatically when idle? | ☐ Yes (after ____ min) ☐ No |
| Logged in on many devices? | ☐ Yes (max ____) ☐ No |
| Can users see and end other sessions? | ☐ Yes ☐ No |
| "Log out everywhere" button? | ☐ Yes ☐ No |
| Where do they land after login? | |
| If they were opening a private page first | ☐ Send them back there ☐ Always go home |
| Wrong-password message | 💡 Do not reveal which part was wrong: "Email or password is incorrect." |

## 7. Passwords and reset 🔴 `[P1]`
*(No passwords? Write `N/A – no passwords` and skip.)*

| Question | 👉 Answer |
|---|---|
| Minimum length | ____ characters (💡 **15** if the password is the only login step; **8** only if MFA or another strong step is always required) |
| Maximum length | ____ (💡 allow **at least 64**) |
| Force symbols / capitals / numbers? | ☐ Yes ☐ No (💡 **No**. Modern guidance says length beats forced symbols) |
| Force password change every few months? | ☐ Yes ☐ No (💡 **No**. Only force a change if a leak is suspected) |
| Check against leaked-password lists? | ☐ Yes ☐ No (💡 Yes) |
| Show / hide password eye icon? | ☐ Yes ☐ No |
| Allow pasting (password managers)? | ☐ Yes ☐ No (💡 **Yes**; accessibility rules need it) |
| Strength meter? | ☐ Yes ☐ No |
| Password hints ("What was your first pet?") | ☐ No (💡 **No**) |

**Forgot-password steps:**
1. User clicks "Forgot password" → 👉
2. App asks for → 👉
3. App sends → 👉
4. Link valid for ____ minutes. Works ☐ once ☐ many times (💡 once)
5. After reset, other devices are ☐ logged out ☐ stay logged in (💡 logged out)
6. Email the user that the password changed? ☐ Yes ☐ No (💡 Yes)
7. If the email is not in our system, the message is: 👉 (💡 the same friendly message either way)

✅ **Example message:** "If that email has an account, we've sent a reset link."

## 8. Social login 🟡 `[P1]`
*(Not used? Write `N/A`.)*

| Question | 👉 Answer |
|---|---|
| Which providers | |
| Who owns the developer accounts (Google Cloud, Apple Developer, etc.)? | Name: ____ Date: ____ |
| Info we request | ☐ Email ☐ Name ☐ Photo ☐ Other: ____ |
| Allowed redirect addresses (URLs) | Dev: ____ Test: ____ Live: ____ |
| If the provider gives no email (Apple "Hide My Email") | |
| Can users disconnect a provider? | ☐ Yes ☐ No |
| Can they still log in after disconnecting? | ☐ Yes (they have another method) ☐ No |

## 9. Passwordless: links, codes, passkeys 🟢 `[P1]`
*(Not used? Write `N/A`.)*

| Question | 👉 Answer |
|---|---|
| Magic link valid for / single-use? | ____ min / ☐ Yes ☐ No |
| One-time code: digits / valid for | ____ / ____ min |
| Code sent by | ☐ Email ☐ SMS ☐ Authenticator app |
| Wrong attempts before lock | ____ |
| Passkeys: can users add more than one? | ☐ Yes ☐ No |
| Passkeys: what if the user loses the device? | |
| Link opened on a different device than the request | |

✅ **Example:** Magic link valid 15 min, single-use; after 5 wrong codes lock for 15 min.

## 10. Extra protection: MFA and company login (SSO) 🟡 `[P1]`

| Question | 👉 Answer |
|---|---|
| Offer 2-step login (MFA)? | ☐ Required for everyone ☐ Required for admins only ☐ Optional ☐ Not at launch |
| Methods | ☐ Authenticator app ☐ Passkey / security key ☐ SMS ☐ Email code ☐ Backup codes |
| Backup codes given | ____ |
| If the user loses their MFA device | |
| Ask again for risky actions (change email, delete account, pay)? | ☐ Yes ☐ No |
| Company login (SAML / OIDC) | ☐ At launch ☐ Later (when: ____) ☐ Never |
| Auto-join by email domain (@acme.com joins Acme)? | ☐ Yes ☐ No |

💡 Safe default: MFA **required for admins**, **optional** for users.
⚠️ SMS codes are weaker than authenticator apps or passkeys. Offer them only as a fallback.

## 11. Recovery, lockouts, and account changes 🔴 `[P1]`

| Situation | What should happen? 👉 |
|---|---|
| Too many wrong passwords | Slow down or lock for ____ min after ____ tries / show bot check / email the user |
| User forgot which email they used | |
| User lost access to their email | Support steps: |
| User changes email | Verify new email? ☐ Yes ☐ No. Notify old email? ☐ Yes ☐ No |
| User changes password while logged in | Ask for old password? ☐ Yes ☐ No |
| User deletes account | Steps and grace period (e.g., 14 days to undo): |
| Account may be hacked | |
| Admin blocks a user | What the user sees: |

✅ **Example:** After 5 wrong passwords, wait 15 minutes. Email the owner of the account. Show no hint about which email exists.

## 12. Roles and teams 🟡 `[P1]`
*(One simple user type? Write `N/A`.)*

| Action | Role: ____ | Role: ____ | Role: ____ | Role: ____ |
|---|---|---|---|---|
| View own data | ☐ | ☐ | ☐ | ☐ |
| Edit own data | ☐ | ☐ | ☐ | ☐ |
| View others' data | ☐ | ☐ | ☐ | ☐ |
| Invite people | ☐ | ☐ | ☐ | ☐ |
| Remove people | ☐ | ☐ | ☐ | ☐ |
| Manage billing | ☐ | ☐ | ☐ | ☐ |
| Delete account or team | ☐ | ☐ | ☐ | ☐ |

Team rules: Who is owner when a team is made? ____ If the owner leaves? ____ Max team size at launch? ____

## 13. Waitlist, invites, referrals 🟡 `[P1 → P5]`

| Question | 👉 Answer |
|---|---|
| Is signup open to everyone at launch? | ☐ Yes ☐ Waitlist ☐ Invite-only ☐ Mixed |
| Waitlist: what do people give? | ☐ Email only ☐ Email + ____ |
| How are people let in? | ☐ Batches of ____ per week ☐ By score ☐ First come first served |
| Invite codes | ☐ Single-use ☐ Reusable |
| Invite expires after | ____ days |
| Can users invite others? | ☐ Yes (limit ____) ☐ No |
| Referral reward (if any) | |
| How do we stop fake referrals? | |

✅ **Example:** Waitlist emails only; let in 50 people per week; each user gets 3 single-use invites that last 14 days.

## 14. Onboarding and activation 🔴 `[P1 → P5]`

**14.1 What is the "Aha!" moment?** (the first time a new user thinks "this is useful!")
✅ **Example:** "User sends their first booking request."
👉 Answer:

**14.2 Fastest path from signup to Aha!** (number the steps)
1.
2.
3.

| Question | 👉 Answer |
|---|---|
| Welcome screen? | ☐ Yes ☐ No |
| Setup questions? | ☐ Yes (list: ____) ☐ No |
| Can users skip onboarding? | ☐ Yes ☐ No |
| Product tour / tooltips? | ☐ Yes ☐ No |
| Sample data for new users? | ☐ Yes ☐ No |
| What counts as "activated" (use a number) | ✅ "First booking within 7 days" → ____ |
| If the user is not activated after 1 day / 3 days / 7 days | |

## 15. Emails and messages the system sends 🔴 `[P1]`

| # | Message | Sent when | Channel | Must include | Sender |
|---|---|---|---|---|---|
| 1 | Verify your email | Right after signup | ☐ Email ☐ SMS ☐ Push | Button + expiry time | |
| 2 | Welcome | After verification | | First step to take | |
| 3 | Password reset | User asks | | Link + "ignore if not you" | |
| 4 | Password changed alert | After change | | "Not you? Do this" | |
| 5 | New device login alert | New device | | Device, time, place | |
| 6 | Invite | Someone invites | | Who, link, expiry | |
| 7 | Nudge to activate | 24 h, not activated | | One clear action | |
| 8 | "You're in" (waitlist) | Access granted | | Link | |
| 9 | Account deleted | On delete | | Date, how to undo | |
| 10 | Other: ____ | | | | |

| Email setup | 👉 Answer |
|---|---|
| Sending service (e.g., Resend, SendGrid, Postmark, SES) | |
| Sending domain (e.g., mail.yourproduct.com) | |
| Domain proof set up (SPF, DKIM, DMARC)? | ☐ Yes ☐ No ☐ TBD |
| Unsubscribe link in marketing emails? | ☐ Yes (required) |
| Support reply-to address | |

## 16. Security and abuse prevention 🔴 `[P1]`

**16.1 Tick when decided:**
☐ Passwords are never stored as plain text (the login service stores only strong hashes) ☐ HTTPS everywhere ☐ Rate limits on signup, login, reset, and code requests ☐ Bot check on signup ☐ Short-lived tokens ☐ Web cookies marked Secure, HttpOnly, SameSite ☐ Secrets and keys kept out of code and out of this file ☐ Login attempts logged (never log passwords or codes) ☐ Alerts for suspicious activity ☐ Messages do not reveal whether an email is registered ☐ Leaked-password check ☐ Regular security updates

| Question | 👉 Answer |
|---|---|
| Signup attempts allowed per device or IP per hour | ____ (💡 5–10) |
| Login attempts per account per 15 min | ____ (💡 5–10) |
| Bot check tool | ☐ Cloudflare Turnstile ☐ reCAPTCHA ☐ hCaptcha ☐ Built into login service ☐ None yet |
| Bot check has an accessible alternative? | ☐ Yes ☐ No (needed for WCAG 3.3.8) |
| Who receives security alerts? | |
| Where are secrets stored? | |
| Checklist used | ☐ OWASP ASVS / Cheat Sheets ☐ NIST SP 800-63B-4 ☐ Other: ____ |
| Security test before launch | ☐ Self-review ☐ Automated scan ☐ Outside expert |

## 17. Legal, privacy, compliance 🔴 `[P1]`
⚠️ *Planning checklist only, not legal advice. Have a qualified lawyer review it before launch.*

**17.1 Documents needed before launch**

| Document | Ready? | Link | Owner |
|---|---|---|---|
| Terms of Service | ☐ Yes ☐ No | | |
| Privacy Policy | ☐ Yes ☐ No | | |
| Cookie Policy and consent banner | ☐ Yes ☐ No ☐ N/A | | |
| Data Processing Agreement (business customers) | ☐ Yes ☐ No ☐ N/A | | |
| Acceptable Use Policy | ☐ Yes ☐ No ☐ N/A | | |

**17.2 Where are your users?** ☐ USA ☐ California ☐ EU/EEA ☐ UK ☐ Canada ☐ India ☐ Australia ☐ Worldwide ☐ Other: ____
💡 Laws to check: GDPR / UK GDPR, CCPA/CPRA, COPPA (US, under 13), CAN-SPAM, CASL (Canada), cookie rules (ePrivacy/PECR), plus local laws.

| Question | 👉 Answer |
|---|---|
| Personal data collected at signup (list every item) | |
| Why we collect each item | |
| Country/region where data is stored | |
| Outside companies that receive data (email, analytics, login service) | |
| How long we keep it | |
| How users can download their data | |
| How users can delete their data (and how fast) | |
| Consent saved with date, time, and terms version? | ☐ Yes ☐ No |
| Terms checkbox starts unticked? | ☐ Yes |
| Marketing consent kept separate from terms? | ☐ Yes |
| Could children under 13/16 sign up? How do we stop it? | |
| Special data (health, money, biometrics, exact location)? | ☐ Yes (list: ____) ☐ No |
| Data-leak plan: who is told, how fast? | |
| Person in charge of privacy questions | |

## 18. Technical setup (developers and AI agents) 🔴 `[P1]`

| Question | 👉 Answer |
|---|---|
| Front end (website/app) technology | |
| Back end / API technology | |
| Database | |
| Hosting | |
| Environments | ☐ Local ☐ Test/Staging ☐ Live |
| User record fields | ✅ id, email, email_verified, created_at, last_login_at, status, role |
| Account statuses | ☐ pending ☐ active ☐ blocked ☐ deleted ☐ other: ____ |
| Email must be unique (ignore upper/lowercase)? | ☐ Yes |
| Extra tables (sessions, invites, audit log, consent log) | |
| Connected services (analytics, CRM, email, payments) | |
| Send new users to a CRM / email tool? | ☐ Yes (which: ____) ☐ No |
| Endpoints needed | ✅ signup, login, logout, verify, reset, refresh, me, delete |
| Coding rules link | |

## 19. Platform notes 🟡 `[P1]`

**Web:** Browsers supported: ____ · Password-manager friendly forms? ☐ Yes ☐ No
**iOS:** Sign in with Apple needed (see Section 3)? ☐ Yes ☐ No · Links that open the app for verification? ☐ Yes ☐ No · Face ID / Touch ID? ☐ Yes ☐ No
**Android:** Google sign-in set up? ☐ Yes ☐ No · App Links for verification? ☐ Yes ☐ No · Fingerprint login? ☐ Yes ☐ No
**Marketplace:** Buyers and sellers sign up differently? ☐ Yes (how: ____) ☐ No · Identity checks (KYC) for sellers? ☐ Yes ☐ No · One account can be both? ☐ Yes ☐ No
**Consumer / social:** Public profile made at signup? ☐ Yes ☐ No · Username rules: ____ · Blocked words: ____
**SaaS:** Free trial or free plan? ☐ Yes (length: ____) ☐ No · Card needed at signup? ☐ Yes ☐ No · Plan chosen at signup? ☐ Yes ☐ No

## 20. Analytics and funnel 🔴 `[P1 → P5]`

| Event name | Fires when | Save these details | Tracked? |
|---|---|---|---|
| `landing_viewed` | Visitor sees the page | source, campaign | ☐ |
| `signup_started` | Opens signup form | method | ☐ |
| `signup_submitted` | Presses Create | method | ☐ |
| `signup_failed` | Error shown | error type | ☐ |
| `email_verified` | Verifies | minutes taken | ☐ |
| `login_succeeded` / `login_failed` | Login | method, reason | ☐ |
| `onboarding_step_completed` | Each step | step name | ☐ |
| `activated` | Aha! moment | time since signup | ☐ |
| `invite_sent` / `invite_accepted` | Invites | | ☐ |
| `password_reset_requested` / `_completed` | Reset | | ☐ |
| `account_deleted` | Delete | reason | ☐ |

⚠️ Never put passwords, codes, or full personal details in analytics events.

| Question | 👉 Answer |
|---|---|
| Analytics tool | |
| Dashboard link | |
| Who checks it, and how often? | |
| Funnel steps (in order) | ✅ Visit → Signup started → Submitted → Verified → Activated |
| Alert if signup success falls below | ____ % |
| Tracking consent handled? | ☐ Yes ☐ No |

## 21. Support and operations 🟡 `[P1 → P5]`

| Question | 👉 Answer |
|---|---|
| Where users ask for help | ☐ Email ☐ Chat ☐ Help center ☐ Form |
| Support hours and reply-time promise | |
| Top 5 expected signup/login problems and the answers | 1. 2. 3. 4. 5. |
| Who can manually verify, unblock, or delete a user? | |
| How support checks identity before changing an account | |
| Who is on call if signup breaks? | |
| Outage message / status page plan | |

## 22. Error messages and edge cases 🔴 `[P1]`

**22.1 Write exactly what the user sees** (kind, clear, tells them what to do next)

| Situation | Message 👉 |
|---|---|
| Email already registered | ✅ "That email is already in use. Try logging in or resetting your password." |
| Invalid email format | |
| Password too short | |
| Passwords do not match | |
| Verification link expired | |
| Verification code wrong | |
| Too many attempts | |
| Social login cancelled | |
| Social login failed | |
| Internet lost during signup | |
| Server error | |
| Account blocked | |
| Session expired | |

**22.2 Decide each edge case**

| Edge case | Decision 👉 |
|---|---|
| User double-clicks "Create account" | |
| User closes the tab mid-signup, returns later | |
| User opens verification link on a different device | |
| Email typed with capitals or extra spaces | |
| Same person tries Google, then email, with the same address | |
| Slow connection | |
| User presses Back mid-signup | |
| Verification email arrives late | |
| Very long email or special characters | |
| User signs up while already logged in elsewhere | |

## 23. Accessibility and language 🟡 `[P1]`

| Question | 👉 Answer |
|---|---|
| Accessibility target | 💡 WCAG 2.2 AA |
| Whole flow works with keyboard only? | ☐ Yes |
| Works with screen readers? | ☐ Yes |
| Login does not depend on memory or puzzles alone (WCAG 3.3.8)? | ☐ Yes (paste allowed, password manager works, alternative to CAPTCHA) |
| Errors not shown by color alone? | ☐ Yes |
| Languages at launch | |
| Right-to-left languages? | ☐ Yes ☐ No |
| Time zones and date formats | |

---

# PART C: BUILD, TEST, LAUNCH, GROW (P2 → P5)

## 24. Testing 🔴 `[P3]`

Write the *expected result* now. Testers fill the rest later.

| ID | What to test | Expected result | Pass / Fail | Who / date |
|---|---|---|---|---|
| T01 | Signup with valid email + password | Account made, verification sent | | |
| T02 | Signup with an existing email | Clear message, no duplicate account | | |
| T03 | Signup with invalid email | Inline error | | |
| T04 | Too-short or leaked password | Rejected with a helpful message | | |
| T05 | Verify email by link | Verified; user lands on ____ | | |
| T06 | Expired verification link | Expiry message + resend option | | |
| T07 | Login with correct details | Logged in | | |
| T08 | Login with wrong password | Neutral error | | |
| T09 | Lockout after too many tries | Locks as in Section 11 | | |
| T10 | Forgot-password full flow | Password changed, old link dead | | |
| T11 | Reuse an old reset link | Rejected | | |
| T12 | Each social login | Account made or linked | | |
| T13 | Social login cancelled | Friendly message | | |
| T14 | Logout | Session ended on this device | | |
| T15 | Session expiry | Re-login as in Section 6 | | |
| T16 | MFA setup and login (if used) | Works, including backup codes | | |
| T17 | Invite accepted | Joins the right team and role | | |
| T18 | Role permissions | Each role does only what is allowed | | |
| T19 | Change email | Verified; old email notified | | |
| T20 | Delete account | Data handled as in Section 17 | | |
| T21 | Phone and tablet sizes | No broken layout | | |
| T22 | Keyboard-only and screen reader | Fully usable | | |
| T23 | Rate limit and bot test | Blocked correctly | | |
| T24 | Emails reach inbox (3 major providers) | Not in spam | | |
| T25 | Analytics events | All Section 20 events appear | | |
| T26 | Paste into password fields; password manager | Works | | |

**Quality gate (all must be ☒ before launch):**
☐ All 🔴 tests pass ☐ No open critical or high bugs ☐ Section 16 done ☐ Section 17 approved ☐ Load test: ____ signups per minute handled ☐ Backup and restore tested ☐ Rollback plan written

## 25. Launch checklist 🔴 `[P4]`

| Area | Check | Owner | Done |
|---|---|---|---|
| Product | Signup works on the **live** site, not only test | | ☐ |
| Product | Real email arrives from the live sending domain | | ☐ |
| Product | Live social-login keys installed (not test keys) | | ☐ |
| Legal | Terms, Privacy, cookie banner live and linked from signup | | ☐ |
| Security | Test accounts and test keys removed | | ☐ |
| Security | Admin accounts protected with MFA | | ☐ |
| Data | Backups running | | ☐ |
| Monitoring | Error and signup-rate alerts on | | ☐ |
| Analytics | Dashboard shows live events | | ☐ |
| Support | Help page and support email ready | | ☐ |
| Marketing | Landing page → signup link tested from every channel | | ☐ |
| Marketing | Welcome and nudge emails scheduled | | ☐ |
| Team | Launch-day roles and contacts shared | | ☐ |
| Rollback | Steps to quickly pause new signups | | ☐ |

**Launch day:** Date/time ____ · Who presses "go" ____ · Who watches the dashboard ____ · Who answers support ____ · Pause signups if failures exceed ____ %

## 26. Journey to the first 500 customers 🔴 `[P5]`

**26.1 Milestones**

| Milestone | Target date | What we check | What we do if it looks bad |
|---|---|---|---|
| First real user (not the team) | | Can they sign up alone? | |
| 10 users | | Watch or talk to 5: where did they get stuck? | |
| 50 users | | Finish-signup % and activation % | |
| 100 users | | Support questions, top 3 complaints | |
| 250 users | | Spam signups, email delivery | |
| 500 users | | Are the Section 1.5 goals met? | |

**26.2 Weekly review**

| Week | New signups | Started→Finished % | Verified % | Activated % | Biggest problem | Fix chosen | Shipped? |
|---|---|---|---|---|---|---|---|
| 1 | | | | | | | |
| 2 | | | | | | | |
| 3 | | | | | | | |
| 4 | | | | | | | |

**26.3 Improvement rules** (💡 change one thing at a time)
☐ Decide using Section 20 data ☐ Every change has a written goal ☐ Every change is logged in Section 29.3

**26.4 After 500, what next?** 👉 ✅ "Open to everyone, add passkeys, raise rate limits."

## 27. AI Agent Instructions 🔴 `[P2]`

🤖 **AI agents: read this whole document before writing code. This section is a contract.**

**27.1 Rules**
1. This document is the source of truth. If an answer is blank, `TBD`, or contradicts another section, **stop and ask the owner. Do not guess.**
2. Use the login service chosen in Section 3.4. Do **not** write your own password hashing, token signing, or cryptography.
3. Never put secrets, keys, passwords, or real user data in code, logs, tests, screenshots, or this file.
4. Never weaken a security rule (rate limits, verification, cookie flags) to make a test pass.
5. Write a test for each acceptance criterion (27.3), before or together with the code.
6. Make the smallest change that meets the requirement. Do not add features that are not listed.
7. Show error messages exactly as written in Section 22.
8. After each task, send the hand-off report in 27.6.

**27.2 Forbidden actions**
- Turning off or skipping email verification, MFA, or rate limits (except local test mode)
- Logging passwords, tokens, or one-time codes
- Revealing whether an email is registered (login and reset messages stay neutral)
- Using live data or live keys in non-live environments
- Deleting or migrating user data without owner approval
- Changing legal text without owner approval

**27.3 Acceptance criteria** (one pass/fail sentence per requirement)
💡 Format: **GIVEN** a situation, **WHEN** the user does X, **THEN** Y happens.

| ID | From section | GIVEN / WHEN / THEN | Priority |
|---|---|---|---|
| AC-01 | 4 | GIVEN a new visitor, WHEN they submit a valid email and password, THEN an account is created and a verification email arrives within ____ seconds | 🔴 |
| AC-02 | 22 | GIVEN an existing email, WHEN signup is submitted, THEN ____ | 🔴 |
| AC-03 | 5 | | 🔴 |
| AC-04 | 6 | | 🔴 |
| AC-05 | 11 | | 🔴 |
| AC-06 | 7 | | 🔴 |
| AC-07 | 8 | | 🟡 |
| AC-08 | 12 | | 🟡 |
| AC-09 | 20 | | 🔴 |
| AC-10 | 23 | | 🟡 |
| | | | |

**27.4 Definition of Done** (all must be ☒)
☐ Code written and reviewed ☐ Acceptance criteria met ☐ Tests added and passing ☐ No secrets in code ☐ Messages match Section 22 ☐ Analytics events fire ☐ This file updated ☐ Owner approved

**27.5 Suggested build order**
1. Project and environments → 2. Login service setup → 3. Signup + verification → 4. Login / logout / sessions → 5. Password reset → 6. Social login → 7. Emails → 8. Roles and invites → 9. Onboarding → 10. Analytics → 11. Security hardening → 12. Tests → 13. Launch checklist

**27.6 Hand-off report (use after every task)**
```text
TASK: <id and name>
WHAT CHANGED: <plain words>
FILES: <list>
TESTS RUN: <names> → <pass/fail>
OPEN QUESTIONS / ASSUMPTIONS: <list, or "none">
NEXT STEP: <one line>
```

## 28. Risks, questions, decisions 🟡 `[All phases]`

**28.1 Risks**

| # | Risk | Chance (L/M/H) | Damage (L/M/H) | What we do | Owner |
|---|---|---|---|---|---|
| R1 | Verification emails land in spam | | | | |
| R2 | Bots flood signup | | | | |
| R3 | Login service goes down | | | | |
| R4 | People quit at the signup form | | | | |
| R5 | Legal or privacy problem | | | | |
| R6 | | | | | |

**28.2 Open questions**

| # | Question | Owner | Due | Answer |
|---|---|---|---|---|
| Q1 | | | | |
| Q2 | | | | |

**28.3 Decision log** (write *why*, so nobody reopens it by accident)

| Date | Decision | Why | Who |
|---|---|---|---|
| | | | |

## 29. Sign-off and change log 🔴 `[All phases]`

**29.1 Final self-check** (all must be ☒ before you share this file)
☐ No blank answers (each is filled, `N/A – reason`, or `TBD – who – by`) ☐ No passwords, keys, or secrets written here ☐ Every 🔴 item is answered ☐ Sections agree with each other ☐ Error messages written ☐ Acceptance criteria written ☐ Legal items reviewed ☐ Someone who did not write it has read it ☐ Progress tracker (0.4) is up to date

**29.2 Approvals**

| Role | Name | Date | ☐ Approved |
|---|---|---|---|
| Product owner | | | ☐ |
| Tech lead / developer | | | ☐ |
| QA / tester | | | ☐ |
| Legal / privacy reviewer | | | ☐ |
| Marketing / growth | | | ☐ |

**29.3 Change log**

| Version | Date | Changed by | What changed |
|---|---|---|---|
| 0.1 | | | First draft |
| | | | |

---

# APPENDIX A: Full mini example ("WalkMyDog")

> **1.1** An app where dog owners book trusted local walkers in under two minutes.
> **3.1** ☒ Email + password ☒ Continue with Google ☒ Continue with Apple. Everything else: later.
> **4.1** Email (required), Password (required), First name (required). Nothing else.
> **5** Click-a-link, valid 24 hours; user may browse but cannot book until verified.
> **7** Minimum 15 characters (password is the only step at launch), maximum 128, no forced symbols, leaked-password check on, pasting allowed.
> **10** MFA required for admins, optional for users.
> **14.1** Aha! moment: "User sends their first booking request."
> **22** Email exists: "That email is already in use. Try logging in or resetting your password."
> **AC-01** GIVEN a new visitor, WHEN they submit a valid email and a 15+ character password, THEN an account is created and a verification email is sent within 30 seconds.

# APPENDIX B: Sections at a glance

| Part | Sections | Phase |
|---|---|---|
| A. Plan | 1 Basics · 2 Users · 3 Methods | P0 |
| B. Design | 4 Form · 5 Verify · 6 Login · 7 Passwords · 8 Social · 9 Passwordless · 10 MFA/SSO · 11 Recovery · 12 Roles · 13 Waitlist · 14 Onboarding · 15 Emails · 16 Security · 17 Legal · 18 Tech · 19 Platforms · 20 Analytics · 21 Support · 22 Errors · 23 Accessibility | P1 |
| C. Build → Grow | 24 Testing · 25 Launch · 26 First 500 · 27 AI Agents · 28 Risks · 29 Sign-off | P2–P5 |

# APPENDIX C: Reference sources (verify the current version each time)

- NIST SP 800-63B-4, *Digital Identity Guidelines: Authentication and Authenticator Management* (final, August 2025)
- OWASP Authentication Cheat Sheet, Session Management Cheat Sheet, Password Storage Cheat Sheet, ASVS, and Top 10 (Authentication Failures)
- W3C WCAG 2.2 (including Success Criterion 3.3.8, Accessible Authentication)
- Apple App Review Guidelines (4.8 Login Services) and Google Play policies
- Your login service's own security and setup documentation
- Regulator guidance for each region where you have users (GDPR, CCPA/CPRA, COPPA, CAN-SPAM, CASL)

*End of template. For each new project, copy this file and rename it, for example `Signup_and_Authentication_Flow_<ProjectName>.md`.*
