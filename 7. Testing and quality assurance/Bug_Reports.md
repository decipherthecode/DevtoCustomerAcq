# HOW TO FILL OUT THIS DOCUMENT (READ THIS FIRST)

> **File:** `Testing and quality assurance/Bug_Reports.md`
> **Template version:** 1.0 | **Works for:** any product, any team, any size project
> **Covers:** the whole AI-Driven Development Life Cycle, from the first line of code to the day your **500th customer** uses the product.

## What is this document?

A **bug** is anything that does not work the way a person would expect. A **bug report** is a short story that tells someone else exactly what went wrong, so they can see it, fix it, and make sure it never comes back.

This one file gives you everything you need:

| Part | What it is | When you use it |
|---|---|---|
| **Part 1** | Project Bug Log (one table for the whole project) | Fill in once per project, add a row for every new bug |
| **Part 2** | Cheat sheets (severity, priority, status, stages, types) | Look things up when a question asks you to choose |
| **Part 3** | The Bug Report Form (the main part) | **Copy it once for every bug** |
| **Part 4** | A finished example | Look at it when you are stuck |
| **Part 5** | Launch gates and the first-500-customers plan | Check before every release |
| **Part 6** | Glossary (word meanings) | Look up any word you do not know |

## The 7 simple rules

1. **Copy, don't edit the template.** Duplicate Part 3 for every new bug. Keep the original clean.
2. **One bug = one report.** Two problems means two reports.
3. **Answer every question.** If you really do not know, write `UNKNOWN` and say why. Never leave a blank and never guess.
4. **Write like you are talking to a friend** who has never seen your product. Short sentences are good.
5. **Show, don't just tell.** Add a screenshot, video, or error text whenever you can.
6. **Never paste secrets.** No passwords, API keys, tokens, credit-card numbers, or customers' private data. Write `[REDACTED]` instead.
7. **Found a security problem?** (Someone can see data they should not, break in, or steal something.) Do **not** post it in a public place. Mark it `SECURITY` and tell the project owner privately right away.

## How the question boxes work

Every question looks like this:

```
Q5. What did you EXPECT to happen?
Why we ask: so the fixer knows what "correct" looks like.
Example: "I expected to see my order list after clicking Save."
Your answer: ______________________________
```

- Replace the underscores with your answer.
- **`[ ]` means a checkbox.** Change it to **`[x]`** to tick it.
- **`(pick one)`** means choose exactly one. **`(pick all that apply)`** means tick as many as you want.
- Items marked **(REQUIRED)** must be filled before you submit. Everything else is **(RECOMMENDED)** or **(IF KNOWN)**.

## The 5-minute version (when you are in a hurry)

Fill in only these questions: **Q1, Q2, Q4, Q6, Q7, Q8, Q9, Q10, Q14, Q15**. Then set the Status to `New`. You can add more details later. A quick report today beats a perfect report next week.

## Who fills what?

| Who | Fills which sections |
|---|---|
| **Reporter** (anyone: tester, developer, support person, customer, AI agent) | Sections A to H |
| **Triage owner** (project manager or lead) | Section I |
| **Developer or AI coding agent** | Sections J, K, and L |
| **QA / Tester** | Section M |
| **Release owner and Support** | Sections N and O |
| **Project owner** | Section P |

---

# PART 1: PROJECT BUG LOG

*Fill the project details once. Add one row per bug. Keep this table updated every day during testing and launch.*

## 1.1 Project details

| Question | Your answer |
|---|---|
| Project name | |
| Product one-line description (what does it do, for whom?) | |
| Project owner (name + contact) | |
| QA lead (name + contact) | |
| Bug tracker used (e.g., this file, GitHub Issues, Jira, Linear, Notion) | |
| Link to the tracker or repository | |
| Bug ID prefix for this project (2 to 5 capital letters, e.g., `SHOP`) | |
| Current product version or build | |
| Current life-cycle stage (see 2.4) | |
| Current customer milestone (see 2.5) | |
| Target launch date | |
| Date this log was last updated | |

## 1.2 Bug summary board (update at least once a day)

| Open Critical (S1) | Open High (S2) | Open Medium (S3) | Open Low (S4) | Fixed this week | Waiting for retest |
|---|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 | 0 |

## 1.3 The bug log table

*Add a new row for every report. The "Report" column should point to the copy of Part 3 for that bug (a link, file name, or ticket number).*

| Bug ID | Title (max 10 words) | Severity | Priority | Status | Stage found | Reporter | Owner | Date found | Date fixed | Report |
|---|---|---|---|---|---|---|---|---|---|---|
| `PROJ-0001` | *(example) Save button does nothing on phone* | S2 | P1 | New | Beta | Sam | Unassigned | 2026-10-18 | | link |
| | | | | | | | | | | |
| | | | | | | | | | | |
| | | | | | | | | | | |

**How to number bugs:** `PREFIX-` plus a 4-digit counter that only goes up: `PROJ-0001`, `PROJ-0002`, `PROJ-0003`. Never reuse a number, even if a bug is deleted or rejected.

---

# PART 2: CHEAT SHEETS (LOOK THINGS UP HERE)

## 2.1 Severity: "How BAD is the damage?"

*Severity is about the damage to the user or the business. The reporter suggests it. The triage owner confirms it.*

| Level | Name | Plain-language meaning | Everyday example |
|---|---|---|---|
| **S1** | Critical | Product is down, data is lost or leaked, money is wrongly taken, or users are unsafe. No workaround. | App crashes for everyone at login. Customers are charged twice. Private data is visible to strangers. |
| **S2** | High | A main feature is broken or badly wrong. A workaround exists but is painful. | "Checkout" button fails on iPhones. Search returns wrong results. |
| **S3** | Medium | A feature works, but not properly. Most people can still finish their task. | A filter forgets your choice after a refresh. A page loads slowly (5 seconds). |
| **S4** | Low | Small or cosmetic. Nobody is blocked. | A typo. A button is 2 pixels off. Slightly wrong color. |

**Quick test:** *"Can the user still finish what they came to do?"* No → S1 or S2. Yes, but with pain → S3. Yes, easily → S4.

## 2.2 Priority: "How SOON must we fix it?"

*Priority is about timing. A bug can be low severity but high priority (the CEO's name is misspelled on the homepage the day before launch).*

| Level | Name | Fix within | Meaning |
|---|---|---|---|
| **P0** | Drop everything | Same day (hours) | Stop other work. Fix now. May need an emergency release (hotfix). |
| **P1** | Urgent | 1 to 3 days | Must be fixed before the next release. |
| **P2** | Normal | Within 2 weeks | Schedule it into the normal plan. |
| **P3** | Someday | Backlog | Fix when there is spare time. Review every month. |

**Default pairings (a starting guess, not a rule):** S1 → P0, S2 → P1, S3 → P2, S4 → P3.

## 2.3 Status: "Where is this bug in its journey?"

```
New → Triaged → Assigned → In Progress → Fixed (in code) → Ready for Retest → Verified → Closed
        ↓                                                      ↓
   Rejected / Duplicate / Cannot Reproduce / Won't Fix     Reopened (back to Assigned)
```

| Status | Meaning | Who changes it |
|---|---|---|
| New | Just reported, nobody has looked yet | Reporter |
| Triaged | Someone checked it, set severity and priority | Triage owner |
| Assigned | A person or AI agent owns it | Triage owner |
| In Progress | Being fixed right now | Developer / AI agent |
| Fixed | Fix is written and merged | Developer / AI agent |
| Ready for Retest | Fix is in a test build; waiting for QA | Developer |
| Verified | QA confirmed the fix works | QA |
| Closed | Done. Released and confirmed. | QA / Release owner |
| Reopened | The fix did not work or the bug came back | QA / Anyone |
| Duplicate | Same as another bug (write that Bug ID) | Triage owner |
| Cannot Reproduce | Nobody could make it happen again after real effort | Triage owner |
| Won't Fix | Decided not to fix (must give a written reason) | Project owner |
| Rejected | Not a bug (works as designed) | Triage owner |
| Blocked | Cannot move forward; waiting on something (write what) | Anyone |

## 2.4 Life-cycle stages: "Where in the product's life was the bug found?"

| Code | Stage | Plain meaning |
|---|---|---|
| **D1** | Idea & Requirements | Writing down what to build. Bugs here are wrong or missing requirements. |
| **D2** | Design & Architecture | Planning screens and structure. Bugs here are design flaws. |
| **D3** | Development (coding, with or without AI) | Building the product. Bugs found by the builder. |
| **D4** | Code Review & Automated Tests | Reviewers or test robots catch problems before merging. |
| **D5** | QA / System Testing | Testers try the whole product on a test version. |
| **D6** | Staging / Pre-Release | A "dress rehearsal" copy that looks like the real thing. |
| **D7** | Alpha (internal users) | Your own team uses it for real. |
| **D8** | Beta (invited outside users) | A small group of trusted outsiders tries it. |
| **D9** | Launch / Release | The day the product goes public. |
| **D10** | Live: Customers 1 to 500 | Real customers are using it. Every bug now has a human cost. |
| **D11** | Live: After 500 customers | Ongoing maintenance and growth. |

## 2.5 Customer milestones (how many real customers had it when the bug happened)

| Code | Milestone | Customers | Extra care needed |
|---|---|---|---|
| **M0** | Pre-users | 0 | None. Internal only. |
| **M1** | Friends & team | 1 to 10 | Personally message each affected person. |
| **M2** | Early adopters | 11 to 50 | Reply to every customer bug report within 24 hours. |
| **M3** | Growing | 51 to 200 | Track trends. Three or more reports of the same bug = raise its priority. |
| **M4** | Almost there | 201 to 499 | Freeze risky changes. Only well-tested fixes go out. |
| **M5** | Milestone reached | 500+ | Run a "first 500" review (see Part 5). |

## 2.6 Bug types: "What kind of problem is it?"

| Type | Meaning | Example |
|---|---|---|
| Functional | A feature does the wrong thing | "Add to cart" adds the wrong item |
| UI / Visual | Looks wrong | Text overlaps a button |
| UX / Usability | Confusing or hard to use | Nobody can find the Logout button |
| Performance | Slow, laggy, uses too much battery or memory | Page takes 12 seconds to open |
| Security | Lets someone do or see what they should not | Any user can open another user's invoice |
| Privacy / Compliance | Mishandles personal data or breaks a rule or law | Emails sent to the wrong person |
| Data | Wrong, missing, duplicated, or corrupted data | Order total is wrong |
| Compatibility | Works on some devices or browsers, not others | Fails on Safari only |
| Accessibility | Hard or impossible for people with disabilities | A screen reader cannot read the button |
| Integration / API | Two systems do not talk properly | Payment provider confirmation never arrives |
| Crash / Hang | App closes or freezes | App quits when opening Settings |
| Content / Copy | Wrong words, translations, images | Spanish page shows English text |
| Documentation | Instructions are wrong or missing | Help page describes a button that is gone |
| Build / Deployment | Problem putting the product online | Release fails at the last step |
| AI-Behavior | An AI feature or AI-written code misbehaves (see Section H) | Chatbot invents a refund policy |
| Other | Does not fit above | Explain in Q12 |

## 2.7 Reproducibility: "How often does it happen?"

| Level | Meaning |
|---|---|
| Always | Happens every time (10 out of 10) |
| Often | Most of the time (6 to 9 out of 10) |
| Sometimes | Occasionally (2 to 5 out of 10) |
| Rarely | Almost never (1 out of 10 or less) |
| Once | Saw it one time and could not make it happen again |
| Unable | Could not reproduce at all (use "Cannot Reproduce" status) |

---

# PART 3: THE BUG REPORT FORM

> ## COPY EVERYTHING FROM THIS LINE TO THE "END OF BUG REPORT" LINE. PASTE IT INTO A NEW FILE OR TICKET FOR EACH BUG. NAME IT: `PROJ-0001_short-title.md`

---

## BUG REPORT: `[PROJ-0000]` *(replace with the real Bug ID)*

### 🤖 Machine-readable summary (for AI agents and tools)

*Fill this small block last, after you finish the form. It copies your main answers into one tidy place so AI agents and automation tools never have to guess. Humans can skip reading it.*

```yaml
bug_id: PROJ-0000
title: ""
status: New
severity: S?          # S1 | S2 | S3 | S4
priority: P?          # P0 | P1 | P2 | P3
type: ""              # from Section 2.6
stage_found: D?       # from Section 2.4
customer_milestone: M?  # from Section 2.5
reproducibility: ""   # from Section 2.7
environment: ""       # e.g., Production | Staging | Local
product_version: ""
affected_component: ""
is_security_issue: false
is_regression: false  # did it work before? true/false/unknown
ai_involved_in_code: unknown   # yes | no | unknown
reporter: ""
owner: ""
date_found: YYYY-MM-DD
one_sentence_summary: ""
expected: ""
actual: ""
repro_steps_count: 0
evidence_attached: false
```

---

### SECTION A: THE BASICS *(REQUIRED)*

**Q1. What is the Bug ID?**
*Why we ask: a unique name so everyone talks about the same bug.*
*Example: `SHOP-0042`. Use the next unused number from the Project Bug Log (1.3).*
**Your answer:** ______________________________

**Q2. Give the bug a short title (max 10 words).**
*Why we ask: so anyone can understand the problem at a glance in a list.*
*Good: "Save button does nothing on iPhone Safari". Bad: "Doesn't work" or "Bug".*
*Tip: use the pattern **WHAT breaks + WHERE**.*
**Your answer:** ______________________________

**Q3. Who is reporting this and how can we reach you?**
*Why we ask: so someone can ask you follow-up questions.*
**Your name:** ______________ **Role** (tester, developer, customer, support, AI agent, other): ______________ **Contact:** ______________

**Q4. When did you find it?**
*Example: 2026-10-18, 3:45 PM, Eastern Time.*
**Your answer (date, time, time zone):** ______________________________

**Q5. Which project and which version or build?**
*Why we ask: the bug may already be fixed in a newer version.*
*Where to find the version: usually in "About", "Settings", or the page footer. For AI-built apps, also write the commit ID or build number if you know it.*
**Project:** ______________ **Version / build / commit:** ______________

**Q6. At what life-cycle stage did you find it?** *(pick one, see 2.4)*
- [ ] D1 Idea & Requirements
- [ ] D2 Design & Architecture
- [ ] D3 Development
- [ ] D4 Code Review & Automated Tests
- [ ] D5 QA / System Testing
- [ ] D6 Staging / Pre-Release
- [ ] D7 Alpha (internal)
- [ ] D8 Beta (invited outside users)
- [ ] D9 Launch / Release
- [ ] D10 Live, customers 1 to 500
- [ ] D11 Live, after 500 customers

**Q7. How many real customers had the product when this happened?** *(pick one, see 2.5)*
- [ ] M0 (0) &nbsp; [ ] M1 (1 to 10) &nbsp; [ ] M2 (11 to 50) &nbsp; [ ] M3 (51 to 200) &nbsp; [ ] M4 (201 to 499) &nbsp; [ ] M5 (500+)

**Q7b. Which part of the product is affected?** *(a screen, feature, API, or module)*
*Example: "Checkout page → payment form".*
**Your answer:** ______________________________

---

### SECTION B: WHAT HAPPENED? *(REQUIRED)*

**Q8. Explain the problem in 2 to 4 simple sentences.**
*Why we ask: this is the story. Imagine telling a friend who has never seen your product.*
*Example: "I typed my email on the sign-up page and pressed Create Account. The page just spun forever. Nothing happened and no error showed."*
**Your answer:** ______________________________

**Q9. What did you EXPECT to happen?**
*Why we ask: so the fixer knows what "correct" looks like.*
*Example: "I expected to see a welcome page and get a confirmation email."*
**Your answer:** ______________________________

**Q10. What ACTUALLY happened?**
*Why we ask: the gap between Q9 and Q10 IS the bug.*
*Example: "The loading circle spun for over 2 minutes. No welcome page and no email."*
**Your answer:** ______________________________

**Q11. Did the exact same thing ever work before?** *(pick one)*
- [ ] Yes, it used to work (this is a **regression**). It worked in version: ______ and broke in version: ______
- [ ] No, it has never worked
- [ ] I don't know → write `UNKNOWN` here and explain: ______

**Q12. What kind of problem is it?** *(pick one; see 2.6)*
- [ ] Functional &nbsp; [ ] UI / Visual &nbsp; [ ] UX / Usability &nbsp; [ ] Performance &nbsp; [ ] Security &nbsp; [ ] Privacy / Compliance
- [ ] Data &nbsp; [ ] Compatibility &nbsp; [ ] Accessibility &nbsp; [ ] Integration / API &nbsp; [ ] Crash / Hang &nbsp; [ ] Content / Copy
- [ ] Documentation &nbsp; [ ] Build / Deployment &nbsp; [ ] AI-Behavior &nbsp; [ ] Other: ______________

---

### SECTION C: HOW TO MAKE IT HAPPEN AGAIN (STEPS TO REPRODUCE) *(REQUIRED)*

**Q13. Write the exact steps, one action per line, so a stranger can repeat them.**
*Why we ask: a bug that cannot be repeated is very hard to fix. This is the most valuable part of the report.*
*Rules: number every step. Say exactly what you clicked or typed. Include the starting point.*

**Before you start (the "setup"):** *(Example: "Be logged out. Use a brand-new account.")*
______________________________

**Steps:**
1. ______________________________
2. ______________________________
3. ______________________________
4. ______________________________
5. ______________________________

*(Example: 1. Open https://example.com/signup. 2. Type `test@example.com` in the Email box. 3. Type any 8-letter password. 4. Click "Create Account". 5. Wait 10 seconds.)*

**Test data you used** *(fake data only!)*: ______________________________

**Q13b. How often does it happen?** *(pick one; see 2.7)*
- [ ] Always &nbsp; [ ] Often &nbsp; [ ] Sometimes &nbsp; [ ] Rarely &nbsp; [ ] Once &nbsp; [ ] Unable to reproduce
**I tried it ____ times and it happened ____ times.**

**Q13c. Is there a workaround?** *(a way for the user to still get the job done)*
- [ ] Yes: ______________________________ &nbsp; [ ] No &nbsp; [ ] Don't know

---

### SECTION D: WHERE DID IT HAPPEN? (ENVIRONMENT) *(REQUIRED)*

**Q14. Which environment?** *(pick one)*
- [ ] Production (the real, live product) &nbsp; [ ] Staging / Pre-release &nbsp; [ ] QA / Test server &nbsp; [ ] Development / My computer &nbsp; [ ] Other: ______

**Q15. What device and software were you using?**
*Why we ask: many bugs only happen on certain devices or browsers.*
*Where to find it: search "what is my browser version" or check Settings → About.*

| Question | Your answer |
|---|---|
| Device (e.g., iPhone 15, Dell laptop, Pixel 8) | |
| Operating system + version (e.g., Windows 11, macOS 15, Android 15, iOS 18) | |
| Browser + version (e.g., Chrome 130) *or* "Mobile app" | |
| App version or build number | |
| Screen size or resolution (if visual bug) | |
| Internet connection (Wi-Fi, 4G/5G, slow, offline) | |
| Language and region (e.g., English, USA) | |
| User role or account type (e.g., admin, free user, guest) | |
| Feature flags or experiments turned on (if known) | |
| Other software involved (extensions, VPN, ad-blocker, accessibility tools) | |

**Q15b. Did you try other environments?** *(helps narrow it down)*
- [ ] Happens on other browsers/devices too. List: ______
- [ ] Only happens on: ______
- [ ] Didn't try

---

### SECTION E: EVIDENCE *(RECOMMENDED; REQUIRED for S1 and S2)*

**Q16. What proof do you have?** *(pick all that apply, then attach or link each one)*
- [ ] Screenshot (circle or arrow the problem): link/file ______
- [ ] Screen recording / video (under 2 minutes is best): link/file ______
- [ ] Error message text (copy the exact words): ______
- [ ] Browser console errors (press F12 → Console; copy any red text): ______
- [ ] Network request that failed (F12 → Network; note the URL and status code like 404 or 500): ______
- [ ] App or server log lines (include the time they happened): ______
- [ ] Crash report or stack trace: ______
- [ ] Customer's original message or support ticket: ______
- [ ] Analytics or monitoring alert (link): ______
- [ ] Failed automated test name and output: ______
- [ ] No evidence available. Reason: ______

*Redaction check: [ ] I removed passwords, keys, tokens, and private customer data from all evidence.*

---

### SECTION F: HOW BAD IS IT? (IMPACT) *(REQUIRED)*

**Q17. Suggest a severity.** *(pick one; see 2.1)*
- [ ] **S1 Critical** (down, data lost or leaked, money wrong, unsafe)
- [ ] **S2 High** (main feature broken)
- [ ] **S3 Medium** (works badly)
- [ ] **S4 Low** (small or cosmetic)

**Q18. Why did you choose that severity?** *(one or two sentences)*
**Your answer:** ______________________________

**Q19. Who is affected, and how many?**

| Question | Your answer |
|---|---|
| Who is affected? (everyone, one customer, one device type, admins only) | |
| About how many users or customers? (number or % of the first 500) | |
| Is a real customer waiting or upset right now? | [ ] Yes [ ] No |
| Could anyone lose money, data, time, or safety? Explain. | |
| Any legal, privacy, or contract risk? (personal data, payments, children's data, health data) | [ ] Yes [ ] No [ ] Unsure |
| Any accessibility harm? (blocks people who use screen readers, keyboards only, etc.) | [ ] Yes [ ] No [ ] Unsure |
| Does this block a launch or milestone? | [ ] Yes: ______ [ ] No |

**Q20. Is this a security or privacy problem?** *(be careful!)*
- [ ] No
- [ ] Yes → **STOP. Do not share publicly.** Tell the project owner privately now, mark the Bug ID `SECURITY`, and share only on a need-to-know basis.
- [ ] Not sure → treat it as **Yes** until someone checks.

---

### SECTION G: EXTRA CLUES *(IF KNOWN)*

**Q21. Anything else that might help?** *(recent changes, unusual data, time of day, related bugs, ideas)*
**Your answer:** ______________________________

**Q22. Related bugs or links?** *(duplicates, similar bugs, design files, requirement docs, pull requests)*
**Your answer:** ______________________________

**Q23. Do you have a guess about the cause?** *(it is OK to guess here; just say it is a guess)*
**Your answer (guess):** ______________________________

---

### SECTION H: AI-DRIVEN DEVELOPMENT DETAILS *(REQUIRED if any AI helped build, test, or run this part of the product)*

*Why we ask: AI tools can write code very fast, and sometimes they write confident mistakes. These answers help us find AI-related causes and teach our AI tools to stop repeating them.*
*If no AI was involved at all, tick the first box and skip to Section I.*

**Q24. Was AI involved?** *(pick all that apply)*
- [ ] No AI involved anywhere (skip to Section I)
- [ ] AI wrote or edited the code that is broken
- [ ] AI wrote the tests (or the tests passed but missed this bug)
- [ ] AI wrote the requirements, design, or documentation
- [ ] The product has an AI feature (chatbot, recommendations, summaries, image generation) and **that feature** misbehaved
- [ ] An AI agent found or reported this bug
- [ ] An AI agent will be asked to fix it
- [ ] I don't know

**Q25. AI tool and model details** *(IF KNOWN)*

| Question | Your answer |
|---|---|
| AI tool or agent used (e.g., Claude Code, Copilot, Cursor, other) | |
| AI model name and version | |
| Date the AI produced the code | |
| Link to the prompt, chat, or agent run that produced it | |
| Was the code reviewed by a human before merging? | [ ] Yes [ ] No [ ] Unknown |
| Did automated tests run on it before merging? | [ ] Yes (passed) [ ] Yes (failed, merged anyway) [ ] No [ ] Unknown |

**Q26. What kind of AI problem is it?** *(pick all that apply)*
- [ ] Made-up (hallucinated) function, library, setting, or fact that does not exist
- [ ] Used an old or wrong version of a library
- [ ] Missed an edge case (empty input, very large input, weird characters, no internet)
- [ ] Changed something it was not asked to change
- [ ] Broke an older feature while adding a new one
- [ ] Security weakness (exposed secret, missing permission check, unsafe input handling)
- [ ] Misunderstood the requirement
- [ ] Tests were weak or fake (tests that always pass)
- [ ] AI feature gave wrong, harmful, biased, or made-up answers to a user
- [ ] AI feature ignored its safety rules or leaked its instructions
- [ ] Cost or speed problem (too many AI calls, too slow, too expensive)
- [ ] Other: ______

**Q27. For AI product features only: what did the user ask, and what did the AI say?**
*Copy the real input and output (remove private data). Add the date, since AI answers can change.*
**User input:** ______________________________
**AI output:** ______________________________
**What the correct answer should have been:** ______________________________

**Q28. AI-agent handoff brief** *(fill this if an AI agent will triage or fix the bug)*
*Why we ask: AI agents work best with clear boundaries. This section tells the agent exactly what it may and may not do.*

| Question | Your answer |
|---|---|
| Files or folders the agent **should** look at | |
| Files or folders the agent **must NOT** change | |
| How to run the project locally (commands) | |
| How to run the tests (commands) | |
| What "fixed" looks like (a test that passes, a screen that works) | |
| Is the agent allowed to change the database, settings, or deploy? | [ ] No (default) [ ] Yes: ______ |
| Must a human approve the fix before merging? | [ ] Yes (default) [ ] No |
| Maximum time or attempts before the agent must stop and ask a human | |

> **Safe-handoff reminder:** An AI agent should **never** receive passwords, real customer data, or permission to push straight to production. Always require a human check for S1 and S2 fixes.

---

### SECTION I: TRIAGE (filled by the Triage Owner) *(REQUIRED before work starts)*

*Triage means "sorting by urgency", like a hospital emergency room.*

**Q29. Is the bug real and complete?**
- [ ] Yes, accepted &nbsp; [ ] Need more info from reporter (ask: ______) &nbsp; [ ] Duplicate of: `PROJ-____` &nbsp; [ ] Cannot reproduce (tried ____ times on ______) &nbsp; [ ] Not a bug (works as designed; link to the requirement: ______) &nbsp; [ ] Won't fix (reason: ______)

**Q30. Final severity and priority** *(pick one each)*
**Severity:** [ ] S1 [ ] S2 [ ] S3 [ ] S4 &nbsp;&nbsp; **Priority:** [ ] P0 [ ] P1 [ ] P2 [ ] P3
**Reason, if different from the reporter's suggestion:** ______________________________

**Q31. Who owns the fix, and by when?**
**Owner** (person or AI agent): ______________ **Due date:** ______________ **Target release:** ______________
**Fixer type:** [ ] Human developer [ ] AI agent with human review [ ] AI agent (low-risk only) [ ] Vendor / third party

**Q32. Does this need a hotfix (emergency release)?** *(usually only for S1 or P0)*
- [ ] No, include it in the normal release
- [ ] Yes → Approved by: ______________ at (date/time): ______________

**Q33. Triage date and name:** ______________

---

### SECTION J: INVESTIGATION & ROOT CAUSE (filled by the Developer or AI agent)

*"Root cause" means the REAL reason it happened, not just where it showed up. Ask "why?" up to five times.*

**Q34. In plain words, what is the real cause?**
*Example: "The sign-up form waited for the email service, but the email service key had expired, so the request never finished."*
**Your answer:** ______________________________

**Q35. The "5 Whys" (optional but powerful)**
1. Why did the problem happen? ______________
2. Why did that happen? ______________
3. Why did that happen? ______________
4. Why did that happen? ______________
5. Why did that happen? ______________

**Q36. Where did the bug come from?** *(pick one)*
- [ ] Requirement was missing or wrong &nbsp; [ ] Design flaw &nbsp; [ ] Coding mistake (human) &nbsp; [ ] Coding mistake (AI-written) &nbsp; [ ] Bad data &nbsp; [ ] Configuration or settings &nbsp; [ ] Third-party service or library &nbsp; [ ] Infrastructure / hosting &nbsp; [ ] Missing or weak test &nbsp; [ ] Unclear. More study needed.

**Q37. Why did we NOT catch it earlier?** *(this is how we get better)*
**Your answer:** ______________________________

---

### SECTION K: THE FIX (filled by the Developer or AI agent)

**Q38. What was changed to fix it?** *(simple summary, then links)*
**Summary:** ______________________________
**Link to code change (pull request / commit):** ______________________________
**Files changed (list):** ______________________________

**Q39. Fix size and risk**
- **Size:** [ ] Tiny (1 to 10 lines) [ ] Small [ ] Medium [ ] Large
- **Risk of breaking something else:** [ ] Low [ ] Medium [ ] High. What could break: ______

**Q40. Developer checklist before saying "Fixed"** *(tick all)*
- [ ] I reproduced the bug first using the steps in Q13
- [ ] I fixed the cause, not just the symptom
- [ ] I added or updated an automated test that fails without the fix and passes with it
- [ ] All existing tests still pass
- [ ] A different person (or reviewer) checked the code
- [ ] No secrets or private data were added to the code
- [ ] I checked for the same mistake in other places
- [ ] If AI wrote the fix, a human read and understood every changed line
- [ ] Documentation or release notes updated (if needed)
- [ ] Data repair needed for affected customers? [ ] No [ ] Yes: described in Q45

---

### SECTION L: PREVENT IT FROM COMING BACK

**Q41. Which safety net did you add?** *(pick all that apply)*
- [ ] New automated test (name it: ______) &nbsp; [ ] Monitoring or alert &nbsp; [ ] Input checks or validation &nbsp; [ ] Code review checklist item &nbsp; [ ] Better error message or logging &nbsp; [ ] Updated requirement or design doc &nbsp; [ ] Updated AI prompt, rule file, or agent instructions (write the new rule: ______) &nbsp; [ ] Team training or note &nbsp; [ ] Nothing needed (explain): ______

**Q42. Related areas that might have the same problem** *(look for "cousins" of this bug)*
**Your answer:** ______________________________

---

### SECTION M: RETEST & VERIFICATION (filled by QA)

**Q43. Verification results**

| Check | Result |
|---|---|
| Build or version tested | |
| Environment tested | |
| Followed the exact steps from Q13 | [ ] Fixed [ ] Still broken |
| Tested on other devices and browsers listed in Q15 | [ ] Pass [ ] Fail [ ] N/A |
| Tested nearby features for new breakage (regression check) | [ ] Pass [ ] Fail |
| New automated test exists and passes | [ ] Yes [ ] No |
| Tester name and date | |

**Q44. Decision**
- [ ] **Verified**, move to Closed after release &nbsp; [ ] **Reopened**, because: ______________ (set Status = Reopened and tell the owner)

---

### SECTION N: RELEASE & CUSTOMER FOLLOW-UP (filled by Release owner and Support)

**Q45. Release details**

| Question | Your answer |
|---|---|
| Released in version / build | |
| Release date and time | |
| Released how? | [ ] Normal release [ ] Hotfix [ ] Feature flag turned off/on [ ] Rollback |
| Data repair needed for affected users? Describe and say who is doing it. | |
| Confirmed fixed in production by (name, date) | |

**Q46. Customer communication** *(required when real customers were affected)*
- [ ] No customers affected, nothing to send
- [ ] Customers affected → Number notified: ______ Method: [ ] Email [ ] In-app message [ ] Status page [ ] Personal message [ ] Support reply
- [ ] Apology, refund, credit, or gift offered? Describe: ______
- [ ] Customer confirmed it works now (for first 500 customers, try to get this from each person)

**Draft message** *(keep it honest, short, and kind: what happened, what we did, what to do now, sorry)*:
______________________________

---

### SECTION O: LESSONS LEARNED *(REQUIRED for S1 and S2; optional for the rest)*

**Q47. What went well?** ______________________________
**Q48. What went wrong?** ______________________________
**Q49. What will we change so this class of bug does not happen again?** *(name an action, an owner, and a date)* ______________________________

---

### SECTION P: CLOSURE & SIGN-OFF

**Q50. Closure checklist** *(all boxes must be ticked before Status = Closed)*
- [ ] Root cause written down (Q34)
- [ ] Fix released and confirmed in production (Q45)
- [ ] QA verified (Q43)
- [ ] A test or safety net added (Q41)
- [ ] Affected customers told, if any (Q46)
- [ ] Project Bug Log row updated (1.3)
- [ ] Lessons learned recorded, if S1/S2 (Q47 to Q49)
- [ ] Security issues handled by the project owner, if any (Q20)

**Sign-off**

| Role | Name | Date |
|---|---|---|
| Reporter | | |
| Developer / AI agent owner | | |
| QA | | |
| Project owner (required for S1/S2 and "Won't Fix") | | |

### CHANGE HISTORY OF THIS REPORT

| Date | Who | What changed (status, severity, notes) |
|---|---|---|
| | | Created |
| | | |

### ✅ BEFORE YOU SUBMIT: THE 10-SECOND QUALITY CHECK

- [ ] The title says WHAT broke and WHERE
- [ ] A stranger could repeat my steps without asking me anything
- [ ] I wrote what I expected AND what actually happened
- [ ] I listed my device, software, and version
- [ ] I attached proof (or explained why not)
- [ ] I removed all secrets and private data
- [ ] I picked severity and explained why
- [ ] This report describes ONE bug only
- [ ] I filled the machine-readable summary at the top
- [ ] I added the bug to the Project Bug Log

## END OF BUG REPORT

> **Stop copying here.**

---

# PART 4: A FINISHED EXAMPLE (LOOK HERE IF YOU ARE STUCK)

*This is a short, filled-in example, not a real bug.*

**Bug ID:** `SHOP-0042`
**Title:** Pay button does nothing on iPhone Safari
**Reporter:** Mia (Tester), mia@example.com | **Found:** 2026-10-12, 2:10 PM ET | **Version:** 1.4.2 (build 311)
**Stage:** D8 Beta | **Customers so far:** M1 (7 customers) | **Affected area:** Checkout → Payment form

**What happened (Q8):** On my iPhone, I added a shirt to the cart and tapped "Pay Now". Nothing happened. No spinner and no error.
**Expected (Q9):** I expected to go to the "Order Confirmed" page.
**Actual (Q10):** The button changed color and then nothing else happened. The page stayed the same.
**Worked before? (Q11):** Yes, it worked in version 1.4.1. This is a **regression**.
**Type (Q12):** Functional

**Steps (Q13):**
1. Open https://shop.example.com on an iPhone using Safari.
2. Tap "Blue Shirt", then "Add to cart".
3. Tap the cart icon, then "Checkout".
4. Fill in the fake test address.
5. Tap "Pay Now".

**How often (Q13b):** Always (5 out of 5). **Workaround (Q13c):** Yes, using Chrome on the same phone works.
**Environment (Q14/Q15):** Staging | iPhone 14, iOS 18.1, Safari | Wi-Fi | English (US) | Guest user
**Evidence (Q16):** Screen recording (22 seconds) attached. Console shows `TypeError: undefined is not a function (payment.js:88)`. Secrets redacted.
**Severity (Q17):** S2 High. *Reason (Q18):* Nobody on iPhone Safari can buy, and about 40% of our beta users use iPhones.
**Security/privacy? (Q20):** No.
**AI involved? (Q24, Q25):** Yes. AI wrote `payment.js` using a coding agent on 2026-10-09. A human reviewer checked it, and the tests passed but did not cover Safari.
**AI problem type (Q26):** Used a browser feature that Safari does not support (made-up compatibility assumption).

**Triage (Q29 to Q32):** Accepted. S2 / P1. Owner: Dev team (AI agent with human review). Due: 2026-10-14. Hotfix: No.
**Root cause (Q34):** The payment code used a browser feature (`Array.at()`) that older Safari versions do not understand.
**Source (Q36):** Coding mistake (AI-written). **Why missed (Q37):** Tests only ran in Chrome.
**Fix (Q38):** Replaced it with a widely supported alternative. PR #218. Size: tiny. Risk: low.
**Safety nets (Q41):** Added a Safari test to the automated test list; added a rule to the AI agent's instructions: "Check browser support before using new JavaScript features."
**Retest (Q43/Q44):** Verified on iPhone 14 and 15 and on desktop Safari on 2026-10-13. Regression check passed.
**Release (Q45):** Version 1.4.3 on 2026-10-14. **Customers (Q46):** The 7 beta users were told; 6 confirmed it works.
**Lesson (Q47 to Q49):** Always test the top 3 browsers. Owner: QA. Done by: 2026-10-20.
**Status:** Closed.

---

# PART 5: LAUNCH GATES & THE FIRST-500-CUSTOMERS PLAN

## 5.1 Bug rules for each release (go / no-go checklist)

*A "gate" is a door that only opens if you meet the rule. Fill this in before every release.*

| Gate | Rule | Met? |
|---|---|---|
| Alpha → Beta (D7 → D8) | 0 open S1. 0 open S2 in core flows (sign-up, login, main feature, payment). | [ ] |
| Beta → Launch (D8 → D9) | 0 open S1. 0 open S2. S3 bugs have a written plan. All security issues closed. | [ ] |
| Launch day (D9) | Rollback plan tested. Support team trained. Bug Log reviewed in the last 24 hours. | [ ] |
| Every release during first 500 customers (D10) | 0 open S1. Any open S2 has owner-approved workaround and customer message. Every fix has a test. | [ ] |
| Hotfix | Needs project owner approval, a rollback plan, and a retest on production right after release. | [ ] |

## 5.2 Customer-bug response times (service targets)

| Severity | First reply to the customer | Fix target | Update every |
|---|---|---|---|
| S1 | 1 hour | Same day | 2 hours |
| S2 | 4 hours | 1 to 3 days | 1 day |
| S3 | 1 business day | 2 weeks | Weekly |
| S4 | 2 business days | Backlog | When fixed |

*Adjust these numbers for your product, and write the new numbers here:* ______________________________

## 5.3 First-500 review (do this when customer #500 arrives)

Answer these questions once, using the Project Bug Log:

1. How many bugs total were found from D1 to D10? ______ How many were S1 / S2 / S3 / S4? ____ / ____ / ____ / ____
2. How many bugs were found by customers instead of by us? ______ **(The goal is to lower this number every release.)**
3. Which 3 areas of the product had the most bugs? ______________________________
4. How many bugs came from AI-written code? ______ How many AI-feature misbehaviors? ______
5. Which Bug types repeated most (see 2.6)? ______________________________
6. Average time from "New" to "Closed" for S1/S2: ______
7. How many bugs were reopened? ______ Why? ______________________________
8. Which customers were affected the most and have we thanked them? ______________________________
9. The top 5 changes we will make to our testing, AI instructions, and release process: ______________________________
10. Is the product stable enough to grow past 500? [ ] Yes [ ] Not yet. Because: ______

---

# PART 6: GLOSSARY (WORD MEANINGS)

| Word | Simple meaning |
|---|---|
| **AI agent** | A computer program powered by AI that can do work (like write or test code) with some independence |
| **API** | A doorway that lets two programs talk to each other |
| **Backlog** | The waiting list of work that will be done later |
| **Beta** | A trial version used by a small group of invited outside people |
| **Build** | One specific packaged version of the product |
| **Cannot Reproduce** | We tried hard and could not make the bug happen again |
| **Commit / Pull request (PR)** | A saved set of code changes / a request to review and merge them |
| **Console** | A hidden browser window that shows technical messages (press F12) |
| **Duplicate** | A bug that has already been reported |
| **Edge case** | A rare or strange situation (like typing 10,000 letters in a name box) |
| **Environment** | The "place" the product is running (live, test, your own computer) |
| **Feature flag** | A hidden on/off switch for a feature |
| **Hallucination** | When an AI confidently says or writes something that is false or does not exist |
| **Hotfix** | A fast emergency fix released outside the normal schedule |
| **Log** | A diary the software writes about what it is doing |
| **Production** | The real, live product that customers use |
| **Regression** | Something that used to work and then broke after a change |
| **Reproduce** | To make the bug happen again by following steps |
| **Rollback** | Going back to the previous working version |
| **Root cause** | The real reason something went wrong |
| **Severity** | How bad the damage is |
| **Priority** | How soon it must be fixed |
| **Staging** | A practice copy of the product that looks like the real one |
| **Triage** | Sorting problems by how urgent they are |
| **Workaround** | A temporary way to get around the problem |

---

# DOCUMENT CONTROL

| Item | Value |
|---|---|
| Document name | Bug_Reports.md |
| Folder | Testing and quality assurance |
| Template version | 1.0 |
| Created | 2026-10-18 |
| Owner of this template | |
| Review schedule | Every 6 months, or after any S1 bug |
| How to suggest an improvement | Write it here or tell the template owner: |

**Template change history**

| Version | Date | Change | By |
|---|---|---|---|
| 1.0 | 2026-10-18 | First version | |
