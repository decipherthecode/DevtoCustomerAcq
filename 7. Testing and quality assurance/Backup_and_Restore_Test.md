# How to fill this document

**Read this box first. It takes 3 minutes.**

## What is this document?
This is your **Backup and Restore Test** plan and record. A *backup* is a safe copy of your product's important stuff. A *restore* is putting that copy back after something breaks. A backup you have never restored is only a hope. This document makes you **prove** it works, **before** customers depend on it.

## Who is it for?
Anyone: a founder, a developer, a helper, or an AI assistant. You do **not** need to be technical to fill in most of it. Where a section is technical, there is a plain-words explanation and an example.

## How to fill it (6 steps)
1. **Copy this file** into your project's `Testing and quality assurance` folder. Keep the name `Backup_and_Restore_Test.md`. Never edit the master template, only your copy.
2. **Fill in the Quick Facts** (Part 0). Takes 2 minutes.
3. **Go top to bottom.** Every part has a *question*, a spot for your answer, and an *Example answer*. Replace each `[ANSWER HERE]` with your answer. Delete the example text if you like, but keep the question.
4. **Tick the boxes.** Change `[ ]` to `[x]` when something is done and true. Never tick a box you did not actually check.
5. **Do not guess.** If you do not know, write `UNKNOWN` and add it to the Open Questions list (Part 14). Do not leave a blank. `UNKNOWN` is an honest answer. A blank is not.
6. **Finish with the Go / No-Go Scorecard** (Part 16) and get a human to sign it (Part 17).

## Symbols used in this document
| Symbol | Meaning |
|---|---|
| `[ANSWER HERE]` | You must replace this with your answer |
| `[ ]` / `[x]` | Not done / done |
| `OPTIONAL` | Skip if it does not apply, but write "Not applicable because ..." |
| `STOP` | Do not continue until this is fixed |
| **Stuck? Ask your AI** | Copy the prompt into an AI assistant to help you answer that section |

## Golden rules
- **Never test on live customer data.** Use a copy, a staging area, or a safe empty space.
- **Never paste passwords, keys or secrets into this file.** Write *where they are stored* (for example "in the password manager, entry called X"), never the secret itself.
- **A human must press the final "approve" button.** AI can help write and review. A person signs.
- **If a test fails, that is a good result.** You found a problem while it was cheap. Write it down in Part 12.
- **One test run = one copy of Part 13.** Re-use this file for every test, and add a new run record each time.

## Which parts do I fill and when?
| Product stage | Fill these parts |
|---|---|
| Starting development | Parts 0 to 5, then 13 (dry run) |
| Before first staging deployment | Parts 0 to 13, run Test Stage **A** |
| Before launch (pre-launch gate) | Everything, run Test Stage **B**, complete Parts 16 and 17 |
| Customer milestones (1, 50, 100, 250, 500) | Re-run Part 13 and update Parts 1, 2, 8, 16 |
| After a big change | Re-run Test Stage **E** (see Part 4) |

## Stuck? Ask your AI (starter prompt)
> "I am filling in a Backup and Restore Test document for my product. Ask me one simple question at a time, as if I am 10 years old, to help me answer Part [number]. When we are done, write my answer in the same format as the template."

---

# Backup and Restore Test

## Part 0. Quick Facts

**Question:** Who, what, when? Fill in these basics.

| Field | Your answer |
|---|---|
| Product name | [ANSWER HERE] |
| Project / repository name | [ANSWER HERE] |
| Document version (start at 1.0) | [ANSWER HERE] |
| Today's date (YYYY-MM-DD) | [ANSWER HERE] |
| Document owner (one person, name and role) | [ANSWER HERE] |
| Backup test runner (the human who runs the test) | [ANSWER HERE] |
| Approver (a human who can say "yes, safe to launch") | [ANSWER HERE] |
| Where this product lives (cloud, host, provider names) | [ANSWER HERE] |
| Current product stage | `[ ] Building` `[ ] Staging` `[ ] Pre-launch` `[ ] Live: 0 to 49 customers` `[ ] Live: 50 to 499 customers` `[ ] Live: 500+ customers` |
| Current number of customers | [ANSWER HERE] |
| Does this product handle personal data? (names, emails, addresses, health or payment info) | `[ ] Yes` `[ ] No` `[ ] Not sure` |

*Example answer:* Product: PetPal. Owner: Sam (founder). Runner: Sam. Approver: Priya (advisor). Lives on: a managed Postgres database, S3 storage, and a hosting service. Stage: Pre-launch. Customers: 0. Personal data: Yes (emails).

> **Stuck? Ask your AI:** "Here is a short description of my product: [paste it]. Help me fill in the Quick Facts table. Mark anything you cannot know as UNKNOWN."

---

## Part 1. What Are We Protecting? (Inventory)

**Question:** If your product's computer exploded tonight, what would you be sad to lose? List everything that matters. This is your **Protection List**. Anything not on this list will **not** be backed up or tested.

### 1A. Databases
*(Where your product stores customer accounts, orders, settings, etc.)*

| # | Name | Type (e.g. Postgres, MySQL, MongoDB, Supabase) | Where it runs | Rough size | Contains personal data? | Importance (High / Medium / Low) |
|---|---|---|---|---|---|---|
| D1 | [ANSWER HERE] | | | | | |
| D2 | | | | | | |

*Example answer:* D1 | main-db | Postgres (Supabase) | Supabase cloud | 200 MB | Yes (emails) | High

### 1B. Files and uploads
*(Photos, documents, videos, exports that customers or you upload)*

| # | Name | Where stored (e.g. S3 bucket, disk) | Rough size | Contains personal data? | Importance |
|---|---|---|---|---|---|
| F1 | [ANSWER HERE] | | | | |

### 1C. Settings, secrets and code
*(Things that make your product run, but are not customer data)*

| # | Item | Where it lives | Backed up where? | Importance |
|---|---|---|---|---|
| C1 | Source code | [ANSWER HERE] | | High |
| C2 | Environment variables / config files | [ANSWER HERE] | | High |
| C3 | Secrets and keys (**write location only, never the secret**) | [ANSWER HERE] | | High |
| C4 | Infrastructure setup (Terraform, Docker files, deploy scripts) | [ANSWER HERE] | | High |
| C5 | Domain names and DNS records | [ANSWER HERE] | | High |
| C6 | Third-party accounts and settings (payments, email sender, analytics) | [ANSWER HERE] | | Medium |

### 1D. Whole servers or containers
*OPTIONAL: skip if you use only managed services. If skipped, write "Not applicable because ...".*

| # | Server / container / cluster | What it does | Can it be rebuilt from code? (Yes / No / Partly) | Importance |
|---|---|---|---|---|
| S1 | [ANSWER HERE] | | | |

### 1E. Things that are NOT backed up on purpose
**Question:** What are you choosing *not* to back up, and why?

[ANSWER HERE]

*Example answer:* Temporary cache and thumbnails. They are rebuilt automatically.

**Checklist for Part 1**
- [ ] Every database is listed
- [ ] Every place files are stored is listed
- [ ] Secrets are listed by *location only*
- [ ] I asked a teammate or AI "what did I forget?" and added the answer
- [ ] Each item has an importance level

> **Stuck? Ask your AI:** "My product uses [list tools]. Help me find everything that needs backing up: databases, file storage, secrets, config, code, domains, third-party services. Ask me questions if you are unsure. Do not guess."

---

## Part 2. Recovery Targets (How Fast? How Much Can We Lose?)

**Two simple ideas:**
- **RPO ("how much can we lose?")**: If we must restore, how far back in time can the data be? *"We can lose up to 1 hour of new data."*
- **RTO ("how long can we be down?")**: How long until the product works again after a disaster? *"Back within 4 hours."*

### 2A. Pick a preset (tick ONE)

| Preset | Who it fits | Max data loss (RPO) | Max downtime (RTO) | Typical backup rhythm |
|---|---|---|---|---|
| `[ ]` **Hobby / Prototype** | No real customers, nothing painful to lose | 24 hours | 3 days | Daily |
| `[ ]` **Early Launch** | 1 to 49 customers, free or low-paid | 12 hours | 24 hours | Daily + before every release |
| `[ ]` **Growing (Recommended from 50 customers)** | 50 to 499 customers, paying | 1 hour | 8 hours | Hourly or continuous + daily full |
| `[ ]` **Business Critical** | 500+ customers, money or health data involved | 5 to 15 minutes | 1 to 4 hours | Continuous + daily full + off-site copy |
| `[ ]` **Custom** | None of these fit | Fill in 2B | Fill in 2B | Fill in 2B |

### 2B. Custom row (only if you ticked Custom, or want to override a preset)

| Item | Your number | Why this number? |
|---|---|---|
| Max data loss (RPO) | [ANSWER HERE] | |
| Max downtime (RTO) | [ANSWER HERE] | |
| Backup rhythm | [ANSWER HERE] | |

### 2C. Different targets for different items? (OPTIONAL)
| Protection List item (D1, F1, ...) | RPO | RTO |
|---|---|---|
| [ANSWER HERE] | | |

### 2D. Is the target realistic?
**Question:** Do you have the people, money and tools to meet this target?
- [ ] Yes, and I checked
- [ ] No. I will lower the target or fix the gap (explain): [ANSWER HERE]

**Rule:** *Moving up a preset is allowed at any time. Moving down needs the Approver's written OK in Part 17.*

---

## Part 3. How Are Backups Made Today?

**Question:** Describe each backup. If a backup does not exist yet, write `NOT YET`, and that becomes a STOP item.

### 3A. Backup list

| # | Protects (D1, F1, C1, ...) | Method (automatic provider backup, script, snapshot, git, manual) | How often | Where the copy is stored | Different location from the original? (Yes / No) | How long is it kept? |
|---|---|---|---|---|---|---|
| B1 | [ANSWER HERE] | | | | | |
| B2 | | | | | | |

*Example answer:* B1 | D1 | Provider automatic backup with point-in-time recovery | Continuous + daily | Provider's storage in another region | Yes | 30 days

### 3B. The 3-2-1 check (a simple safety rule)
Good backups follow **3-2-1**: **3** copies, on **2** different kinds of storage, with **1** copy far away (another region or provider).

- [ ] I have at least 3 copies (the live one + 2 backups)
- [ ] They are on at least 2 different kinds of storage or services
- [ ] At least 1 copy is in a different location or provider
- [ ] I cannot meet 3-2-1 yet. Reason and plan: [ANSWER HERE]

### 3C. Backup safety
- [ ] Backups are **encrypted** (scrambled so thieves cannot read them)
- [ ] Only named people (or named systems) can read or delete backups
- [ ] Backups cannot be changed or deleted by the same account that runs the live product (protection against mistakes and ransomware)
- [ ] Someone gets an alert if a backup **fails** or is **missing**
- [ ] The place where the encryption keys are stored is written down (location only): [ANSWER HERE]
- [ ] The *recovery instructions and keys* are stored **outside** the system being backed up (otherwise you cannot get in during a disaster)

### 3D. Who gets alerted when a backup fails?
[ANSWER HERE] *(a person's name and how they are told: email, chat, phone)*

> **Stuck? Ask your AI:** "Here is how my product is hosted: [paste]. What backup features does it offer by default? Which of my items are NOT covered? Say 'I am not sure' if you are not sure."

---

## Part 4. When Will We Test? (Test Schedule Across the Product's Life)

**Question:** Backups must be tested at certain moments. This table is your schedule. Fill in planned dates, then update actual dates when done.

| Test Stage | When | Goal | Planned date | Actual date | Result (Pass / Fail / Not run) |
|---|---|---|---|---|---|
| **A. First dry run** | Before the first staging deployment | Prove the basic backup and restore works while data is small | [ANSWER HERE] | | |
| **B. Pre-launch gate** | Before real customers can sign up | **Must PASS to launch.** Full test of everything on the Protection List | [ANSWER HERE] | | |
| **C1. Milestone: first customer** | Within 7 days of customer #1 | Check that real data is being backed up correctly | [ANSWER HERE] | | |
| **C2. Milestone: 50 customers** | Within 14 days of reaching 50 | Re-check size, speed and targets | [ANSWER HERE] | | |
| **C3. Milestone: 100 customers** | Within 14 days of reaching 100 | Same | [ANSWER HERE] | | |
| **C4. Milestone: 250 customers** | Within 14 days of reaching 250 | Same, plus check cost and storage growth | [ANSWER HERE] | | |
| **C5. Milestone: 500 customers** | Within 14 days of reaching 500 | Full test again. Decide whether to upgrade the preset (Part 2) | [ANSWER HERE] | | |
| **D. Regular re-test** | Every 3 months (or monthly at Business Critical) | Make sure nothing quietly broke | [ANSWER HERE] | | |
| **E. After a big change** | Any time you change database, host, provider, encryption, or backup tool | Prove the new setup still restores | As needed | | |

**What counts as a "big change" (Test Stage E)?** Tick all that happened since the last test:
- [ ] New or upgraded database version
- [ ] Moved to a new host, cloud or region
- [ ] Changed how files are stored
- [ ] Changed backup tool, schedule or settings
- [ ] Changed who owns the keys or accounts
- [ ] Big new feature that adds a new kind of data
- [ ] Security incident or near-miss

---

## Part 5. Test Preparation

### 5A. Where will we practice? (the "safe room")
**Question:** Where will you restore the backup so that live customers are never affected?

| Option | Tick one |
|---|---|
| A separate empty copy of the environment (best) | `[ ]` |
| A staging environment | `[ ]` |
| A temporary project or database created just for this test | `[ ]` |
| A local computer (only for small data, no personal data) | `[ ]` |
| **Never** the live system | **STOP if this is the only option** |

Name and location of the safe room: [ANSWER HERE]

**Safe-room checks**
- [ ] It cannot send real emails, texts or payments (they are switched off or pointed to test mode)
- [ ] It cannot connect to live databases or live storage
- [ ] It is deleted or wiped after the test (see 5D)
- [ ] If it holds real personal data, access is limited and the data is deleted after the test

### 5B. Team and roles

| Role | Name | What they do |
|---|---|---|
| Test Runner (human) | [ANSWER HERE] | Does the steps, records results |
| Second Pair of Eyes (human) | [ANSWER HERE] | Checks the results (can be the Approver on tiny teams) |
| Approver (human) | [ANSWER HERE] | Final yes / no |
| AI Assistant (optional) | [ANSWER HERE] | Drafts, reviews, helps explain (see Part 11) |

*Tiny team?* The Runner and the Second Pair of Eyes can be the same person **only if** the Approver is a different person, or you wait 24 hours and re-read the results fresh.

### 5C. Before-you-start checklist
- [ ] I told everyone affected that a test is happening (date and time)
- [ ] I picked a quiet time
- [ ] I have the recovery instructions (this document) open
- [ ] I have access to the backups (accounts, keys) *without* needing the live system
- [ ] I have a stopwatch or clock to time each step
- [ ] I know the **abort rule**: *If anything touches live customer data, stop, write what happened, and tell the Approver.*
- [ ] I wrote down the **start time** in Part 13

### 5D. After-you-finish cleanup plan
- [ ] Safe room deleted or wiped on (date): [ANSWER HERE]
- [ ] Restored copies of personal data deleted
- [ ] Any temporary keys or access removed
- [ ] Costs checked (nothing left running that charges money)

---

## Part 6. The Backup Test (Is the Backup Good?)

**Question:** Before restoring, check that backups exist and look healthy. Tick each box only after you actually looked.

| # | Check | Done | Notes |
|---|---|---|---|
| 6.1 | Latest backup exists for every item on the Protection List | `[ ]` | |
| 6.2 | The backup date and time is recent (within the RPO from Part 2) | `[ ]` | |
| 6.3 | The backup size looks sensible (not 0 bytes, not suddenly tiny) | `[ ]` | |
| 6.4 | The backup tool reports "success" with no warnings | `[ ]` | |
| 6.5 | The backup is stored in the location written in Part 3 | `[ ]` | |
| 6.6 | The backup is encrypted | `[ ]` | |
| 6.7 | An older backup exists too (one from at least a week ago) | `[ ]` | |
| 6.8 | A backup failure alert was tested (OPTIONAL but recommended) | `[ ]` | |
| 6.9 | A *new* backup was created on purpose during this test and timed | `[ ]` | |

**Write the numbers:**
- Latest backup time: [ANSWER HERE]
- Backup size: [ANSWER HERE]
- Time to make a fresh backup: [ANSWER HERE]

`STOP` if 6.1 to 6.5 are not all ticked. Fix the backups first, then start again.

---

## Part 7. The Restore Test (Can We Really Get It Back?)

**Question:** Follow the steps for each item type. Write what you actually did. Start the timer at Step 1 of the first item.

> **Why timing matters:** Your **real restore time** is compared to your **RTO** in Part 2. Write honest times, including waiting time.

### 7A. Database restore
*Skip if you have no database. Write "Not applicable because ...".*

| Step | What to do | Done | Time taken |
|---|---|---|---|
| 7A.1 | Choose the backup to restore (write its date/time): [ANSWER HERE] | `[ ]` | |
| 7A.2 | Create an empty safe-room database | `[ ]` | |
| 7A.3 | Restore the backup into it (write the exact command or button you used): [ANSWER HERE] | `[ ]` | |
| 7A.4 | Wait until it says finished with **no errors** | `[ ]` | |
| 7A.5 | Connect the safe-room version of the product to it | `[ ]` | |
| 7A.6 | Do the checks in Part 8 | `[ ]` | |

**Also try a "point in time" restore** (restore to a moment, e.g. "30 minutes ago") if your provider offers it.
- [ ] Tried, worked
- [ ] Not offered
- [ ] Tried, failed (record in Part 12)

### 7B. Files and uploads restore

| Step | What to do | Done | Time taken |
|---|---|---|---|
| 7B.1 | Choose the file backup (date/time): [ANSWER HERE] | `[ ]` | |
| 7B.2 | Restore into an empty safe-room storage area | `[ ]` | |
| 7B.3 | Count the files: original ____ vs restored ____ | `[ ]` | |
| 7B.4 | Open 5 random files (photos, PDFs, etc.) and confirm they open properly | `[ ]` | |
| 7B.5 | Restore **one deleted file** by itself (practice for the common "oops, I deleted it" case) | `[ ]` | |

### 7C. Settings, secrets and code restore

| Step | What to do | Done | Time taken |
|---|---|---|---|
| 7C.1 | Get the code from its backup/repository onto a clean computer or server | `[ ]` | |
| 7C.2 | Re-create settings and environment variables from the written list (not from memory) | `[ ]` | |
| 7C.3 | Fetch secrets from the password manager / secret store (confirm you could log in without the live system) | `[ ]` | |
| 7C.4 | Rebuild and start the product in the safe room | `[ ]` | |
| 7C.5 | Domain and DNS records can be re-created from the written list | `[ ]` | |

### 7D. Whole server or container restore
*OPTIONAL. Skip if you use managed services only. Write "Not applicable because ...".*

| Step | What to do | Done | Time taken |
|---|---|---|---|
| 7D.1 | Re-create the server or container from the snapshot or from code | `[ ]` | |
| 7D.2 | It starts without manual patches | `[ ]` | |
| 7D.3 | Things that had to be done by hand (write them; they should become written steps): [ANSWER HERE] | `[ ]` | |

### 7E. "Everything is gone" drill (required at Test Stage B and C5; OPTIONAL otherwise)
**Question:** Pretend your main account, host and database are all unavailable. Can you rebuild from the off-site backups and written steps only?
- [ ] Yes, in this total time: [ANSWER HERE]
- [ ] No. What blocked us: [ANSWER HERE]

---

## Part 8. Did the Restore Really Work? (Proof Checks)

**Question:** "No error message" does not mean "it worked." Check the data itself.

### 8A. Data checks

| # | Check | Expected | Actual | Pass? |
|---|---|---|---|---|
| 8.1 | Number of customer accounts (original vs restored) | Same, or only newer ones missing | [ANSWER HERE] | `[ ]` |
| 8.2 | Number of rows in the 3 biggest tables | Same, or explained | [ANSWER HERE] | `[ ]` |
| 8.3 | Newest record's date | Within the RPO | [ANSWER HERE] | `[ ]` |
| 8.4 | Spot-check 5 customer records by eye | Look right | [ANSWER HERE] | `[ ]` |
| 8.5 | Relationships are intact (e.g. orders still point to the right customers) | Yes | [ANSWER HERE] | `[ ]` |
| 8.6 | File counts and sizes | Match | [ANSWER HERE] | `[ ]` |
| 8.7 | Files open correctly | Yes | [ANSWER HERE] | `[ ]` |

### 8B. Product checks (use the safe-room copy like a customer would)

- [ ] I can log in with a test account
- [ ] I can see existing data
- [ ] I can create new data
- [ ] Core feature #1 works: [ANSWER HERE]
- [ ] Core feature #2 works: [ANSWER HERE]
- [ ] Core feature #3 works: [ANSWER HERE]
- [ ] Payments / emails are in test mode and behaved safely
- [ ] There are no scary errors in the logs

*Example answer for core features:* "Create a pet profile", "Upload a photo", "Book a vet visit".

### 8C. Missing-data note
**Question:** Was any data newer than the backup lost? How much?
- Time between the latest data and the restored data (actual data loss): [ANSWER HERE]
- Is that within the RPO? `[ ] Yes` `[ ] No`

---

## Part 9. Results vs Targets

| Measure | Target (Part 2) | Actual result | Within target? |
|---|---|---|---|
| Data loss (RPO) | [ANSWER HERE] | | `[ ]` Yes `[ ]` No |
| Time to restore database | | | |
| Time to restore files | | | |
| Time to restore everything (RTO) | | | |
| Number of manual surprises | 0 | | |

**Plain-words summary (2 to 4 sentences):** What happened?

[ANSWER HERE]

*Example answer:* "The database restored in 22 minutes with no data loss. Files took 1 hour 10 minutes, longer than expected, but within the 8 hour target. We forgot one environment variable, which we added to the list."

---

## Part 10. Privacy and Compliance (Fill the parts that apply)

**Question:** Does this product hold personal data (Part 0)? If **No**, tick here and skip to Part 11: `[ ]` No personal data, skip.

### 10A. Privacy laws (GDPR / CCPA / similar)
- [ ] I know which countries or states my customers live in: [ANSWER HERE]
- [ ] Backups of personal data have a **maximum keep time** (written in Part 3)
- [ ] I know what happens when a customer asks to be **deleted**: how it is handled in backups (e.g. deleted again after any restore, or backups expire within ___ days): [ANSWER HERE]
- [ ] After a restore, **customer deletion requests made since the backup are re-applied**
- [ ] Backups are stored in allowed regions (check provider region): [ANSWER HERE]
- [ ] Restoring into the safe room did not copy real personal data to an unprotected place
- [ ] Test copies of personal data were deleted (5D)

### 10B. SOC 2 / ISO 27001 style evidence (OPTIONAL: for customers or auditors that ask)
- [ ] Test plan exists (this document)
- [ ] Test was run on the schedule in Part 4
- [ ] Results, screenshots and logs are saved in Part 13 evidence links
- [ ] Failures were tracked to closure (Part 12)
- [ ] Someone other than the Runner reviewed the results
- [ ] Access to backups is limited and reviewed (date of last review): [ANSWER HERE]

### 10C. Health or payment data (HIPAA / PCI-DSS) (OPTIONAL)
- [ ] I have confirmed whether my product is *covered* by HIPAA or PCI-DSS (ask a qualified professional if unsure): [ANSWER HERE]
- [ ] Backups containing health or payment data are encrypted at rest and in transit
- [ ] Access to those backups is logged
- [ ] Test restores never used real health or payment data unless the safe room has the same protections as live
- [ ] Card numbers are **not** stored by us (payment provider stores them), or the PCI plan is attached: [ANSWER HERE]
- [ ] Our provider agreements (for example a HIPAA business associate agreement) are in place: [ANSWER HERE]

> This template is guidance, **not legal advice**. If you are unsure about legal duties, ask a qualified professional.

---

## Part 11. Rules for AI Assistants and AI Agents

**This project's AI mode:** *AI drafts, human runs and approves.*

### 11A. What AI **may** do
- Help fill in questions, suggest missing items, and explain steps in simple words
- Draft checklists, summaries and the results write-up
- Review results and point out mismatches or things that look wrong
- Draft the issues list (Part 12) and suggested fixes
- Compare numbers to the targets in Part 2
- Remind people of the schedule in Part 4

### 11B. What AI **must NOT** do
- Run restore or delete commands, or touch live systems, accounts or backups
- Tick a box it did not verify with evidence a human can see
- Invent numbers, dates, names or results. If unknown, write `UNKNOWN`
- Handle passwords, keys or real customer data
- Approve, sign off, or say "safe to launch" on its own
- Lower the targets in Part 2

### 11C. AI honesty rules
- Mark every AI-written answer with `(AI draft, needs human check)` until a human confirms it.
- When the AI is not sure, it must say so and list what it needs to know.
- The human removes the `(AI draft)` tag only after checking.

### 11D. Copy-paste prompts

**Draft help**
> "Act as a careful QA assistant. I am filling in the Backup and Restore Test template. Here are my answers for Parts 0 to 5: [paste]. Find gaps, contradictions and anything marked UNKNOWN. Do not invent facts. Give me a list of questions I should answer next."

**Result review**
> "Here are my test results from Parts 6 to 9: [paste]. Compare them with my targets in Part 2. Tell me, in simple words, what passed, what failed, and what looks suspicious. Do not decide for me. List what a human should double-check."

**Plain-words summary**
> "Summarize these results in 4 sentences a 10-year-old could understand, then list the 3 most important fixes: [paste]."

**Issue drafting**
> "For each failed check below, draft an issue with: what happened, why it matters, a suggested fix, and who should look at it. Mark guesses as guesses: [paste]."

---

## Part 12. Problems Found and Fixes (Issues Log)

**Question:** Anything that went wrong, was slow, was confusing, or needed a workaround goes here. Failures are useful, so record them.

| ID | Date found | What happened (plain words) | How serious? (High / Medium / Low) | Fix planned | Owner | Due date | Re-tested and fixed? |
|---|---|---|---|---|---|---|---|
| I-1 | [ANSWER HERE] | | | | | | `[ ]` |
| I-2 | | | | | | | `[ ]` |

**Severity guide**
- **High:** Data could not be restored, or restore is slower than the RTO, or data loss is bigger than the RPO. `STOP` for launch.
- **Medium:** It worked, but needed manual hacks, was unclear, or one backup was missing.
- **Low:** Small wording, naming or cosmetic fixes.

**Rule:** Every **High** issue must be fixed and **re-tested** before the Go / No-Go in Part 16.

---

## Part 13. Test Run Record (Copy this part for EVERY test run)

> Make a new copy of this part each time you run a test (Stage A, B, C1 to C5, D, E). Put the newest on top. Keep old ones. They are your proof.

### Run ID: RUN-[number] (e.g. RUN-001)

| Field | Your answer |
|---|---|
| Test Stage (A / B / C1 to C5 / D / E) | [ANSWER HERE] |
| Date and start time | [ANSWER HERE] |
| End time | [ANSWER HERE] |
| Runner (name) | [ANSWER HERE] |
| Second Pair of Eyes (name) | [ANSWER HERE] |
| Safe room used | [ANSWER HERE] |
| Which backup was restored (date/time) | [ANSWER HERE] |
| Number of customers at test time | [ANSWER HERE] |
| Parts 6 to 8 all completed? | `[ ]` Yes `[ ]` No (explain): |
| Result | `[ ]` PASS `[ ]` PASS with issues `[ ]` FAIL |
| Total restore time | [ANSWER HERE] |
| Data loss measured | [ANSWER HERE] |
| Issues found (IDs from Part 12) | [ANSWER HERE] |
| Evidence links (screenshots, logs, command output; **no secrets**) | [ANSWER HERE] |
| Cleanup done (5D)? | `[ ]` Yes |
| Next test planned for | [ANSWER HERE] |

---

## Part 14. Open Questions (Things Nobody Knows Yet)

| # | Question | Who can answer? | Needed by | Answer |
|---|---|---|---|---|
| Q1 | [ANSWER HERE] | | | |

**Rule:** The Go / No-Go in Part 16 cannot say GO while a question affecting backups, restores or privacy is still unanswered.

---

## Part 15. Emergency Quick Guide ("If it breaks for real")

**Question:** Fill this in *now*, while calm. Print it or save it outside your main system. In a real emergency, you will not want to think.

| Question | Your answer |
|---|---|
| Who do I call first? (name, phone) | [ANSWER HERE] |
| Second person? | [ANSWER HERE] |
| Where are the backups? | [ANSWER HERE] |
| Where are the keys / passwords kept (location only)? | [ANSWER HERE] |
| Where is the step-by-step restore guide (link to Part 7, runbook)? | [ANSWER HERE] |
| Who tells customers, and where do we post updates (status page, email)? | [ANSWER HERE] |
| What is the first thing I do? | `STOP changing anything. Write the time. Do not delete anything.` Then call the first person above. |

- [ ] This page is also saved **outside** the system it protects (printed, or another account)
- [ ] Customers can be told what happened (template message prepared): [ANSWER HERE]

---

## Part 16. Go / No-Go Scorecard

**Question:** Is it safe to launch, or to keep going? Score honestly. One **NO** in the "must" list means **NO-GO**.

### 16A. Must-haves (all must be YES)

| # | Question | YES | NO |
|---|---|---|---|
| M1 | Every important item is on the Protection List (Part 1) | `[ ]` | `[ ]` |
| M2 | A recovery preset or custom target is chosen (Part 2) | `[ ]` | `[ ]` |
| M3 | Backups exist for every item and are recent (Part 6) | `[ ]` | `[ ]` |
| M4 | A full restore was done in a safe room, not on live data (Part 7) | `[ ]` | `[ ]` |
| M5 | Restored data was checked and is correct (Part 8) | `[ ]` | `[ ]` |
| M6 | Real restore time is within the RTO (Part 9) | `[ ]` | `[ ]` |
| M7 | Real data loss is within the RPO (Part 9) | `[ ]` | `[ ]` |
| M8 | At least one backup copy is in a separate location (Part 3) | `[ ]` | `[ ]` |
| M9 | Backups are encrypted and access is limited (Part 3) | `[ ]` | `[ ]` |
| M10 | A human, not AI, ran or directly watched the test (Part 11) | `[ ]` | `[ ]` |
| M11 | No High issues are open (Part 12) | `[ ]` | `[ ]` |
| M12 | Emergency Quick Guide is filled in (Part 15) | `[ ]` | `[ ]` |
| M13 | Privacy checks are done if there is personal data (Part 10) | `[ ]` | `[ ]` |
| M14 | Test copies were cleaned up (5D) | `[ ]` | `[ ]` |

### 16B. Nice-to-haves (score 1 point each)

| # | Question | Point |
|---|---|---|
| N1 | Point-in-time restore worked | `[ ]` |
| N2 | A single deleted file or row was restored on its own | `[ ]` |
| N3 | "Everything is gone" drill passed (7E) | `[ ]` |
| N4 | Backup failure alert was tested (6.8) | `[ ]` |
| N5 | Two different people each did a restore | `[ ]` |
| N6 | Restore is a written script or one-click, not manual | `[ ]` |
| N7 | Backups are tested automatically on a schedule | `[ ]` |
| N8 | Cost of backups per month is known: [ANSWER HERE] | `[ ]` |

**Nice-to-have score: ____ / 8** *(0 to 3: improve soon. 4 to 6: good. 7 to 8: excellent)*

### 16C. Decision

| Decision | Tick |
|---|---|
| **GO**: all Must-haves are YES | `[ ]` |
| **GO with conditions**: a Medium issue remains, with owner and date written in Part 12 | `[ ]` |
| **NO-GO**: any Must-have is NO | `[ ]` |

Reason in one sentence: [ANSWER HERE]

**Gate rules by stage**
- **Stage A (before first staging deploy):** Needs M1 to M5 and M8. The rest may be NO but must have a plan.
- **Stage B (pre-launch):** **All** Must-haves are YES. No exceptions without the Approver's written reason.
- **Milestones (C1 to C5):** All Must-haves are YES again. At C2, C4 and C5, also review whether the preset in Part 2 should go up.

---

## Part 17. Sign-Off

By signing, I say I read the results and the decision above is true to the best of my knowledge.

| Role | Name | Decision (Approve / Reject) | Date | Signature (typed name is fine) |
|---|---|---|---|---|
| Test Runner | [ANSWER HERE] | | | |
| Second Pair of Eyes | | | | |
| **Approver (human, required)** | | | | |

- [ ] A person other than the AI approved this
- [ ] Next scheduled test is on the calendar (date): [ANSWER HERE]

---

# Appendix A. Worked Example (Fictional: "PetPal")

> This is a short, finished sample so you can see what good answers look like. It is **not** your project.

**Product:** PetPal, an app where owners track pet health and book vet visits. 12 beta users. Stage: Pre-launch (Stage B).

**Part 1 (Protection List)**
- D1 main-db, Postgres on a managed provider, 200 MB, emails and pet names, High
- F1 pet-photos, cloud storage bucket, 3 GB, photos of pets (some with owners in them), Medium
- C1 code in a Git host, C2 config in the host's settings list, C3 secrets in the password manager entry "PetPal Prod", C4 deploy files in the repository, C5 domain at the registrar, High
- Not backed up: thumbnails cache (rebuilt automatically)

**Part 2:** Preset **Early Launch** (RPO 12 hours, RTO 24 hours). Will move to **Growing** at 50 customers.

**Part 3:** Provider daily backups kept 14 days; weekly copy to a second provider kept 8 weeks; encrypted; failure alerts go to Sam's email and chat. 3-2-1 met.

**Part 5:** Safe room = a temporary project created for the test, named `petpal-restore-test`, deleted the next day.

**Part 7 / 8 results**
- Database restore: 18 minutes, 12 of 12 accounts present, newest record 3 hours old (within 12 hours)
- Files restore: 41 minutes, 3,104 of 3,104 files; 5 random photos opened fine
- Surprise: one environment variable (`MAP_API_KEY` location) was missing from the written list. Added.

**Part 9:** Total 1 hour 20 minutes vs target 24 hours. Pass.

**Part 12:** I-1 (Medium): environment variable not documented. Fixed and re-tested the same day.

**Part 16:** All Must-haves YES. Nice-to-have 5 / 8. Decision: **GO**. Next test: at first paying customer (C1).

---

# Appendix B. Glossary (Plain Words)

| Word | Simple meaning |
|---|---|
| **Backup** | A safe copy of your stuff, kept somewhere else |
| **Restore** | Putting the safe copy back so the product works again |
| **RPO** (Recovery Point Objective) | How much new data you are OK losing. "Up to 1 hour of work." |
| **RTO** (Recovery Time Objective) | How long you are OK being broken. "Up to 4 hours." |
| **Snapshot** | A photo of a server or disk at one moment |
| **Point-in-time recovery** | Rewinding a database to an exact moment, like rewinding a video |
| **Staging** | A practice copy of your product that is not used by real customers |
| **Safe room** | The separate, safe place where you practice restoring |
| **Production / Live** | The real product that customers use |
| **Encryption** | Scrambling data so only people with the key can read it |
| **Secret / Key** | A password-like value that lets software talk to other services |
| **3-2-1 rule** | 3 copies, 2 kinds of storage, 1 far away |
| **Off-site** | Stored in a different place or provider than the original |
| **Retention** | How long you keep old backups before deleting them |
| **Runbook** | A step-by-step guide anyone can follow in an emergency |
| **Point of failure** | One thing that, if it breaks, breaks everything |
| **Integrity check** | Proof that data is complete and not damaged |
| **Ransomware** | Bad software that locks your data and demands money |
| **Compliance** | Following the rules and laws about data |
| **Evidence** | Proof, like screenshots and logs, that a step really happened |
| **Go / No-Go** | The decision to continue (Go) or stop and fix things first (No-Go) |
| **Milestone** | A checkpoint, such as reaching 100 customers |

---

# Appendix C. Common Mistakes (Avoid These)

1. **"We have backups" but nobody ever restored one.** A backup is not proven until restored.
2. **Backups live in the same place as the original.** One accident destroys both.
3. **Keys or recovery steps are stored only inside the system that broke.**
4. **Testing on live customer data** and causing the very outage you feared.
5. **Only the database is backed up.** Files, settings and secrets are forgotten.
6. **Only checking that "no errors" appeared**, without checking the data itself.
7. **Never timing the restore**, so the RTO is a fantasy.
8. **Forgetting deleted-customer requests** after a restore (privacy problem).
9. **Test done once, then never again** while the product keeps changing.
10. **AI ticks the boxes** without a human verifying.

---

# Appendix D. Change History of This Document

| Version | Date | Who | What changed |
|---|---|---|---|
| 1.0 | [ANSWER HERE] | [ANSWER HERE] | First version |
