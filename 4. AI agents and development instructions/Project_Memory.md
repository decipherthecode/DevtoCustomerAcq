# PROJECT MEMORY (THE DIARY)

> **Template version:** 1.1 | **Pairs with:** `Context_Management.md`
> **Project:** ✏️ `________`  **Last updated:** ✏️ `____-__-__`

## How to use this file

This is your project's **diary**. `Context_Management.md` holds the rules; this file holds **what happened**.

- **Newest entries go at the TOP** of each section.
- Write after **every** work session (5 minutes).
- Keep each entry **under 15 lines**.
- Keep only the **latest 10 session entries** here. Move older ones to `/docs/archive/Project_Memory_YYYY-MM.md`.
- Never put passwords, keys, or private customer data here.
- Use markers: `[TODO]`, `[N/A]`, `[UNKNOWN]`, `[DECIDED]`.

**AI helper:** read the **top session entry** and **all open questions** at the start of every session. Add a new entry at the end.

---

# A. SESSION LOG (NEWEST FIRST)

### Entry template (copy for every session)

```
## Session: YYYY-MM-DD | Hat: [Developer/QA/etc.] | Phase: [#]
**Goal of this session:**
**What got done:**
**Files changed:**
**What is NOT finished:**
**Problems or surprises:**
**Decisions made (add big ones to Section B):**
**Next step (one clear sentence):**
**Questions I need answered (add to Section C):**
```

### 💡 Example entry

```
## Session: 2026-10-17 | Hat: Developer | Phase: 2
**Goal of this session:** Add "Add plant" form.
**What got done:** Form with name + photo upload works locally.
**Files changed:** src/pages/AddPlant.tsx, src/api/plants.ts
**What is NOT finished:** Photo size limit; error message for failed upload.
**Problems or surprises:** Photos over 5 MB fail silently.
**Decisions made:** Limit photos to 5 MB (D-003).
**Next step:** Add the photo size check and error message.
**Questions I need answered:** Should photos be optional? (Q-001)
```

✏️ **Your entries start here:**

---

# B. DECISION LOG

📖 Big choices and the reasons, so nobody argues them again. **Newest first.**

| ID | Date | Decision | Why | Other options | Status |
|---|---|---|---|---|---|
| D-001 | 💡 2026-10-17 | Use Supabase for database and login | Fast to start; free tier | Firebase; own server | `[DECIDED]` |
| D-002 | | | | | |

**Rule:** the AI may not change a `[DECIDED]` item without asking me and logging a new decision.

---

# C. OPEN QUESTIONS, ASSUMPTIONS & RISKS

| Type | ID | What | Owner | Due | Status |
|---|---|---|---|---|---|
| Question | Q-001 | 💡 Should photos be optional? | Me | 2026-10-20 | Open |
| Assumption | A-001 | 💡 Users have a smartphone | Me | n/a | Not checked |
| Risk | R-001 | 💡 Reminder emails may land in spam | Me | 2026-11-01 | Watching |

---

# D. BUG & ISSUE LOG

| ID | Date found | What happened | Level (Critical/High/Medium/Low) | Status | Fixed on |
|---|---|---|---|---|---|
| B-001 | 💡 2026-10-17 | Big photos fail silently | Medium | Open | |

---

# E. WEEKLY LOOK-BACKS

| Week of | Weekly goal | Done? | Went well | Slowed me down | Change next week |
|---|---|---|---|---|---|
| 💡 2026-10-19 | Add and view plants | Yes | Fast progress | Photo bug | Test uploads earlier |
| | | | | | |

---

# F. MILESTONE LOG

| Date | Milestone (phase done, launch, customer count) | Notes |
|---|---|---|
| 💡 2026-10-17 | Phase 1 complete | MVP list frozen |
| | | |

---

# G. ARCHIVE INDEX

| Archive file | Covers dates |
|---|---|
| | |
