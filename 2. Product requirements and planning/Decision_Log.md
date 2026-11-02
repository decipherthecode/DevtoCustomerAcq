# 📋 Decision Log — AI-Driven Development Life Cycle

> **Project Name:** `[Replace with your project name]`
> **Product Vision:** `[One sentence — what does this product do and for whom?]`
> **Log Owner:** `[Name of the person responsible for maintaining this file]`
> **Last Updated:** `[YYYY-MM-DD]`
> **Version:** `1.0`

---

---

# 📖 How to Fill This Document

> 💡 **Read this section first — even if you are new to decision logs!**
> Think of this file as a **journal for every important choice** your team makes while building the product.
> Whenever you make a decision that affects the project — big or small — you write it down here so that:
> - Future-you (or anyone who joins later) understands *why* things were built a certain way.
> - You can look back and learn what worked and what didn't.
> - Investors, clients, or teammates can audit the project's thinking.

---

## 🔢 Step 1 — Fill the Document Header (Top of this file)

| Field | What to Write |
|---|---|
| **Project Name** | The name of your product or project (e.g., `SmartHire AI`) |
| **Product Vision** | One sentence: who it is for and what it does (e.g., `An AI copilot that helps recruiters shortlist candidates 10× faster`) |
| **Log Owner** | The person who keeps this file up to date (usually the founder, PM, or tech lead) |
| **Last Updated** | The date you last changed anything in this file (`YYYY-MM-DD` format, e.g., `2026-10-14`) |
| **Version** | Start at `1.0`. Add `0.1` each time you make a significant update (e.g., `1.1`, `1.2`) |

---

## 🔢 Step 2 — Understand the Decision ID System

Every decision gets a **unique ID** so you can reference it anywhere (code comments, PRs, meeting notes).

| Format | Example | What it means |
|---|---|---|
| `DEC-[Phase]-[Number]` | `DEC-D-001` | Discovery, decision #1 |
| | `DEC-A-003` | Architecture, decision #3 |
| | `DEC-V-007` | Development/QA, decision #7 |
| | `DEC-L-002` | Launch & Post-Launch, decision #2 |

**Phase codes:**
- `D` = Discovery & Ideation
- `A` = Architecture & AI Design
- `V` = Development, QA & Safety *(V = Validate)*
- `L` = Launch & Post-Launch (0–500 Customers)

---

## 🔢 Step 3 — Know the Status Lifecycle

Every decision moves through these stages. Update the **Status** field as things progress.

```
Proposed → Under Review → Approved → Implemented → (Superseded if replaced)
```

| Status | Emoji | What it means |
|---|---|---|
| `Proposed` | 🟡 | Someone suggested this decision — it hasn't been approved yet |
| `Under Review` | 🔵 | The team is actively discussing it |
| `Approved` | 🟢 | A decision-maker said "yes, let's go with this" |
| `Implemented` | ✅ | The decision has been acted upon in the product |
| `Superseded` | 🔴 | This decision was replaced by a newer one (link to the new one) |

---

## 🔢 Step 4 — Know the Decision Types

| Type | When to use it |
|---|---|
| `Technical` | Choosing a programming language, database, API, cloud provider, or system architecture |
| `Product` | Deciding on a feature, user flow, screen design, or product scope |
| `Business` | Pricing, partnerships, go-to-market strategy, pivots, or team structure |
| `AI-Specific` | Choosing an AI model, designing prompts, handling training data, setting safety rules |

> ⚠️ A decision can have **more than one type** — just list all that apply, e.g., `Technical + AI-Specific`.

---

## 🔢 Step 5 — Fill Out Each Decision Entry

Each decision is one block of text. Use the **Decision Entry Template** in Section 3.
Fill in every field marked 🔴 **Required**. Fields marked 🟡 **Recommended** are optional but strongly encouraged. Fields marked 🤖 **AI decisions only** are only needed when the decision involves AI/ML.

---

## 🔢 Step 6 — Update the Summary Index (Section 2)

After writing a full entry, add one row to the Summary Index table in Section 2. This gives everyone a quick bird's-eye view of all decisions without having to read every entry.

---

## 🔢 Step 7 — Review Decisions Regularly

Each decision entry has a **Review Date** field. On that date, come back and fill in the **Outcome** field — did the decision work out? This turns the log into a learning tool.

---

---

# 📊 Section 1 — Quick Reference

## Status Legend

| Badge | Status | Meaning |
|---|---|---|
| 🟡 | Proposed | Awaiting discussion |
| 🔵 | Under Review | In active debate |
| 🟢 | Approved | Green-lit |
| ✅ | Implemented | Done and live in the product |
| 🔴 | Superseded | Replaced — see linked decision |

## Customer Impact Legend

| Level | Meaning |
|---|---|
| `Direct` | End users will notice or experience this change (UI, speed, pricing, features) |
| `Indirect` | Users may notice a side-effect (e.g., faster AI responses from an infrastructure change) |
| `Internal only` | Invisible to users — affects only the team, codebase, or operations |

---

## Risk Level Legend

| Badge | Level | Meaning |
|---|---|---|
| 🟢 | Low | Easy to fix if wrong; minimal impact |
| 🟡 | Medium | Some rework needed; noticeable impact |
| 🔴 | High | Hard or costly to undo; major impact on product or users |

## Reversal Cost Legend

| Level | Meaning | Example |
|---|---|---|
| `Easy` | Can be undone in hours or days with low cost | Changing a button colour |
| `Moderate` | Takes 1–2 sprints and some refactoring | Swapping a UI library |
| `Hard` | Major rework; weeks of engineering effort | Migrating databases |
| `Irreversible` | Cannot be undone without starting over or a major incident | Deleting user data, public API contracts |

---

---

# 📑 Section 2 — Decision Summary Index

> 💡 **How to use:** Add one row per decision. Keep this table updated — it is your project's "map" of all decisions made.

| ID | Title | Type | Phase | Status | Owner | Date | Review Date | Superseded By |
|---|---|---|---|---|---|---|---|---|
| `DEC-D-001` | *(example) Validate market with 20 user interviews before building* | Business | Discovery | ✅ Implemented | Alice | 2026-10-01 | 2026-11-01 | — |
| `DEC-A-001` | *(example) Use GPT-4o as primary LLM for MVP* | AI-Specific | Architecture | 🟢 Approved | Bob | 2026-10-05 | 2026-11-15 | — |
| — | — | — | — | — | — | — | — | — |

> ✏️ **Delete the example rows and replace with your own decisions.**

---

---

# 📝 Section 3 — Decision Entry Template

> 💡 **Copy this entire block for every new decision. Paste it into the relevant Phase section below.**
> Delete fields you don't need, but keep all 🔴 Required fields.

---

## Decision Entry: `[DEC-X-000]`

---

### 🏷️ Metadata

| Field | Value |
|---|---|
| 🔴 **Decision ID** | `DEC-X-000` *(replace X with phase code, 000 with next number)* |
| 🔴 **Decision Title** | *(Short name — max 10 words, e.g., "Use PostgreSQL as primary database")* |
| 🔴 **Date Proposed** | `YYYY-MM-DD` |
| 🔴 **Phase** | *(Discovery / Architecture / Dev-QA-Safety / Launch-PostLaunch)* |
| 🔴 **Decision Type** | *(Technical / Product / Business / AI-Specific — pick all that apply)* |
| 🔴 **Status** | 🟡 Proposed |
| 🟡 **Priority** | *(Critical / High / Medium / Low — how urgent is this decision?)* |
| 🟡 **Customer Impact** | *(How does this decision affect the end user? Choose: `Direct — user sees this change` / `Indirect — affects performance or cost the user may notice` / `Internal only — invisible to users`  Then write 1–2 sentences explaining the effect. e.g., "Direct — users will see AI summaries load 40% faster thanks to the model switch.")* |
| 🟡 **Sprint / Milestone** | *(Which sprint or milestone does this decision belong to? e.g., `Sprint 3` / `M1 — MVP Alpha` / `Beta Launch Week`)* |
| 🟡 **Related Decisions** | *(IDs of decisions this one depends on or affects, e.g., `DEC-A-001`)* |
| 🟡 **Blocked By** | *(IDs of decisions that must be made BEFORE this one can be approved, e.g., `DEC-D-002`)* |
| 🟡 **Blocks** | *(IDs of decisions that CANNOT proceed until this one is approved, e.g., `DEC-V-001, DEC-V-002`)* |
| 🟡 **Tags** | *(Free-text keywords for searching, e.g., `#database #performance #mvp`)* |

---

### 🔗 Decision Dependency Map

> 💡 **Use this diagram to show how this decision connects to others.**
> Think of it like a flowchart: arrows point from "must decide first" → "can decide next".
> This helps you see the order in which decisions must be made across the project.
>
> **How to fill it in:**
> - In the `Blocked By` row, list decisions that had to be made *before* this one.
> - In the `Blocks` row, list decisions that are waiting on *this* one.
> - Then draw a simple text diagram below using the format shown.
>
> 💡 **Tip for solo founders:** Even if it's just you, this diagram prevents you from accidentally trying to make Decision B before Decision A is settled.

```
[Draw your dependency chain here using plain text arrows. Example:

  DEC-D-002 (Validate target user)
       ↓
  DEC-A-001 ← YOU ARE HERE (Choose primary LLM)
       ↓
  DEC-V-001 (Define AI eval / acceptance criteria)
  DEC-V-002 (Set safety guardrails policy)

Key:
  ↓ = "must be decided before the next one"
  ← = this is the current decision
]
```

---

### 📌 Context

> 💡 **What is the situation that forced this decision?**
> Write 2–5 sentences that explain the background. Imagine explaining it to a new teammate who wasn't in the room.
> Answer: *What problem exists? What constraint or opportunity triggered this decision?*

```
[Write your context here. Example:
We need to store user profiles, project data, and AI-generated outputs. 
We are a team of 2 engineers with 6 weeks until MVP launch. 
Our budget for infrastructure is under $200/month for the first 6 months.]
```

---

### ❓ Problem Statement

> 💡 **One clear question this decision answers.**

```
[Write the decision question here. Example:
Which database technology should we use for the MVP to balance speed, cost, and our team's skill set?]
```

---

### ✅ Decision Made

> 💡 **Write the final decision in ONE clear sentence. Be specific — avoid vague language.**

```
[Write the decision here. Example:
We will use PostgreSQL hosted on Supabase (free tier) as our primary database for the MVP.]
```

---

### 💡 Rationale

> 💡 **Why did you choose this?** List 3–5 bullet points explaining your reasoning.
> Think: speed of delivery, cost, team skills, scalability, user impact.

- **Reason 1:** *(e.g., Team already knows SQL — no learning curve)*
- **Reason 2:** *(e.g., Supabase free tier covers our load up to ~50,000 rows)*
- **Reason 3:** *(e.g., Built-in auth and storage reduces dev time by ~1 week)*
- **Reason 4:** *(optional)*
- **Reason 5:** *(optional)*

---

### 🔀 Alternatives Considered

> 💡 **List 2–3 other options you thought about.** For each one, write what was good about it and why you didn't pick it.

#### Option 1 — `[Name of Alternative]`

| | Detail |
|---|---|
| **What it is** | *(Brief description)* |
| **Pros** | *(What would have been good about it)* |
| **Cons** | *(Why you didn't choose it)* |

#### Option 2 — `[Name of Alternative]`

| | Detail |
|---|---|
| **What it is** | *(Brief description)* |
| **Pros** | *(What would have been good about it)* |
| **Cons** | *(Why you didn't choose it)* |

#### Option 3 — `[Name of Alternative]` *(optional)*

| | Detail |
|---|---|
| **What it is** | *(Brief description)* |
| **Pros** | *(What would have been good about it)* |
| **Cons** | *(Why you didn't choose it)* |

---

### ⚠️ Risk Assessment

> 💡 **Every decision has risks. Be honest here — it helps you plan ahead.**

| Field | Value |
|---|---|
| **Risk Level** | 🟢 Low / 🟡 Medium / 🔴 High *(delete the ones that don't apply)* |
| **Risk Description** | *(What could go wrong? E.g., "Supabase free tier may not scale past 500 users")* |
| **Mitigation Plan** | *(What will you do if the risk happens? E.g., "Upgrade to Pro plan at 400 users; budget is allocated")* |
| **Probability** | *(Low / Medium / High — how likely is this risk to happen?)* |
| **Impact if it happens** | *(Low / Medium / High — how badly would it hurt the project?)* |

---

### 🔁 Reversal Cost

> 💡 **How hard would it be to undo this decision if it turns out to be wrong?**

| Field | Value |
|---|---|
| **Reversal Cost** | `Easy / Moderate / Hard / Irreversible` |
| **Reversal Notes** | *(Explain what undoing this decision would require. E.g., "Migrating from PostgreSQL to MongoDB would take ~2 sprints and require rewriting all data access layers")* |

---

### 🤖 AI-Specific Fields *(Fill this section ONLY for AI/ML decisions — skip for non-AI decisions)*

#### Model / Tool Selection

| Field | Value |
|---|---|
| **Model / Tool Chosen** | *(e.g., `GPT-4o via OpenAI API`, `Claude 3.5 Sonnet`, `Llama 3 self-hosted`)* |
| **Why This Model** | *(Key reasons: capability, cost, context window, latency, licensing)* |
| **Models Evaluated** | *(List other models you tested or compared)* |
| **Benchmark / Eval Results** | *(Share any test scores, accuracy %, or qualitative observations)* |

#### Prompt Strategy

| Field | Value |
|---|---|
| **Prompt Approach** | *(e.g., Zero-shot / Few-shot / Chain-of-thought / RAG / Fine-tuning)* |
| **System Prompt Summary** | *(1–2 sentences describing what the system prompt instructs the model to do)* |
| **Prompt Version** | *(e.g., `v1.0` — increment when prompt changes significantly)* |
| **Prompt File / Location** | *(Path or link to where the prompt is stored, e.g., `/prompts/resume_parser_v1.txt`)* |

#### Data, Privacy & Safety

| Field | Value |
|---|---|
| **Data Used** | *(What data feeds into the AI? e.g., "User-uploaded resumes, job descriptions")* |
| **PII / Sensitive Data?** | *(Yes / No — if Yes, describe how it is handled)* |
| **Data Retention Policy** | *(How long is data stored? Who can access it?)* |
| **Privacy Compliance** | *(GDPR / CCPA / HIPAA / None — circle what applies)* |
| **Safety Guardrails** | *(What filters, limits, or content policies are in place?)* |
| **Bias Checks Done?** | *(Yes / No / Planned — describe what was tested)* |
| **Red-Teaming Done?** | *(Yes / No / Planned — who tested it for misuse?)* |

#### Cost & Latency Trade-offs

| Field | Value |
|---|---|
| **Estimated Cost Per Request** | *(e.g., `~$0.002 per resume parsed`)* |
| **Estimated Monthly AI Cost at MVP Scale** | *(e.g., `~$40/month at 500 users × 20 requests`)* |
| **Average Latency** | *(e.g., `~2.3 seconds per request`)* |
| **Acceptable Latency Threshold** | *(What's the max latency before user experience degrades? e.g., `< 5 seconds`)* |
| **Cost Optimisation Plan** | *(What will you do if costs spike? e.g., "Cache frequent requests; switch to GPT-4o-mini for simple tasks")* |

---

### 🖊️ Sign-Off Chain & RACI Matrix

> 💡 **Record who proposed, reviewed, and approved this decision.**
> If you are a solo founder, you are all three roles — just put your name in every row.
>
> **RACI explained in plain English:**
> - **R = Responsible** — the person who *does the work* (writes the proposal, builds the thing)
> - **A = Accountable** — the person who makes the *final call* and owns the outcome (usually the founder, PM, or tech lead)
> - **C = Consulted** — people whose *input is needed* before deciding (domain experts, senior engineers, advisors)
> - **I = Informed** — people who need to *know the outcome* but don't vote (investors, other teams, stakeholders)
>
> 💡 Every decision must have **exactly one A** (Accountable). It can have multiple R, C, or I.

#### Sign-Off Chain

| Role | Name | Date | Status |
|---|---|---|---|
| **Proposer** *(who suggested this — usually R)* | | `YYYY-MM-DD` | |
| **Reviewer 1** *(who gave feedback — C)* | | `YYYY-MM-DD` | *(approved / requested changes / abstained)* |
| **Reviewer 2** *(optional — C)* | | `YYYY-MM-DD` | *(approved / requested changes / abstained)* |
| **Decision Maker / Accountable** *(final call — A)* | | `YYYY-MM-DD` | *(approved / rejected / deferred)* |

#### RACI Matrix

> 💡 List every person or role involved in this decision and their RACI code.
> Example: "Alice — R, A | Bob — C | Carol — I | Investor Update — I"

| Name / Role | RACI Code | Notes |
|---|---|---|
| *(e.g., Lead Engineer)* | R | *(Writes the proposal and implements the decision)* |
| *(e.g., Founder / PM)* | A | *(Makes the final call)* |
| *(e.g., UX Designer)* | C | *(Consulted on user impact)* |
| *(e.g., Investor)* | I | *(Informed via monthly update email)* |
| | | |

---

### 🛠️ Implementation Notes

> 💡 **Once the decision is Approved, fill this section to guide whoever implements it.**

| Field | Value |
|---|---|
| **Action Items** | *(List the specific tasks needed to carry out this decision, e.g., "1. Create Supabase project; 2. Run migration scripts; 3. Update .env")* |
| **Owner(s)** | *(Who is responsible for implementing this?)* |
| **Target Implementation Date** | `YYYY-MM-DD` |
| **Actual Implementation Date** | `YYYY-MM-DD` *(fill in when done)* |
| **PR / Commit / Branch** | *(Link or reference to the code change, e.g., `PR #42`)* |
| **Docs / Config Updated?** | *(Yes / No — which files were updated?)* |

---

### 📅 Review & Outcome

> 💡 **Come back to this section on the Review Date to reflect on whether this decision was the right one.**

| Field | Value |
|---|---|
| **Review Date** | `YYYY-MM-DD` *(set this 4–8 weeks after implementation)* |
| **Reviewed On** | `YYYY-MM-DD` *(fill in when you actually review)* |
| **Outcome** | 🟢 Good call / 🟡 Partially right / 🔴 Wrong call *(delete what doesn't apply)* |
| **What Happened** | *(In 2–4 sentences: did it work as expected? Any surprises?)* |
| **Lessons Learned** | *(What would you do differently next time?)* |
| **Superseded By** | *(If this decision was replaced, write the new decision ID here, e.g., `DEC-A-004`)* |

---

### 🕓 Decision Entry Changelog

> 💡 **Track every significant edit made to THIS decision entry after it was first written.**
> This is NOT the product changelog — it is the audit trail for the decision document itself.
> You do NOT need to log every typo fix. Log changes that affect the decision, risk, or outcome.

| Version | Date | Edited By | What Changed |
|---|---|---|---|
| 1.0 | `YYYY-MM-DD` | *(Name)* | Initial entry created |
| 1.1 | | | *(e.g., Risk level updated from Medium to High after load test results)* |
| | | | |

---

---

# 🗂️ Section 4 — Decisions by Phase

> 💡 **Paste copies of the Decision Entry Template (Section 3) into the correct phase below.**
> Each phase has a short description to remind you what kinds of decisions belong there.

---

## 🔍 Phase 1: Discovery & Ideation

> **What this phase is about:**
> You are figuring out *what* to build and *for whom*. Decisions here are about validating the problem,
> understanding users, scoping the MVP, and choosing the business model before a single line of code is written.
>
> **Example decisions in this phase:**
> - "We will validate the product idea by interviewing 20 potential users before building anything."
> - "Our target customer is a freelance designer, not an enterprise team."
> - "We will charge a $29/month subscription, not a per-use fee."
> - "We will build an AI writing assistant, not a grammar checker."

---

### `DEC-D-001` — *(Your first discovery decision goes here)*

*(Paste a completed Decision Entry Template here)*

---

### `DEC-D-002` — *(Add more as needed)*

*(Paste a completed Decision Entry Template here)*

---

## 🏗️ Phase 2: Architecture & AI Design

> **What this phase is about:**
> You are deciding *how* to build it. This includes the tech stack, AI model selection, data architecture,
> system design, and infrastructure choices. Decisions here are often hard to reverse — take your time.
>
> **Example decisions in this phase:**
> - "We will use Next.js + Supabase + OpenAI API as our core stack."
> - "We will use GPT-4o for complex tasks and GPT-4o-mini for simple ones to control cost."
> - "We will use RAG (Retrieval-Augmented Generation) instead of fine-tuning for our knowledge base feature."
> - "User data will be stored in the EU region to comply with GDPR."

---

### `DEC-A-001` — ✅ EXAMPLE: Choose Primary LLM for MVP Resume Parsing Feature

> 🟩 **This is a fully completed example entry.** Read it to understand how to fill in your own decisions.
> When you are ready, delete this example or replace it with your real decision.

---

#### 🏷️ Metadata

| Field | Value |
|---|---|
| **Decision ID** | `DEC-A-001` |
| **Decision Title** | Use GPT-4o as the primary LLM for resume parsing |
| **Date Proposed** | `2026-10-05` |
| **Phase** | Architecture & AI Design |
| **Decision Type** | AI-Specific + Technical |
| **Status** | ✅ Implemented |
| **Priority** | Critical |
| **Customer Impact** | Direct — users receive parsed resume summaries in under 3 seconds, which is the core product promise |
| **Sprint / Milestone** | `Sprint 2 — Core AI Integration` |
| **Related Decisions** | `DEC-D-002` (validated user need for AI-powered parsing in discovery) |
| **Blocked By** | `DEC-D-002` (must confirm target user and core use case before choosing the AI model) |
| **Blocks** | `DEC-V-001` (AI eval framework), `DEC-V-002` (safety guardrails policy) |
| **Tags** | `#llm #openai #gpt4o #resume #parsing #mvp #cost` |

---

#### 🔗 Decision Dependency Map

```
  DEC-D-002 (Validate: target users need AI-powered resume parsing)
       ↓
  DEC-A-001 ← YOU ARE HERE (Choose primary LLM for resume parsing)
       ↓               ↓
  DEC-V-001         DEC-V-002
  (AI eval          (Safety
   framework)        guardrails)
```

---

#### 📌 Context

```
We are building SmartHire AI — a tool that helps recruiters automatically parse and score 
candidate resumes against a job description. Resume parsing is the core AI feature of the MVP.
We need an LLM that can extract structured data (name, skills, experience years, education) 
from unstructured PDF text reliably. Our team of 2 engineers has 4 weeks until beta launch.
We have a monthly AI budget of $150 for the first 3 months.
```

---

#### ❓ Problem Statement

```
Which LLM should we use to parse resumes accurately, within our $150/month budget, 
with response times under 5 seconds, using only our current team's skills (no ML ops)?
```

---

#### ✅ Decision Made

```
We will use OpenAI's GPT-4o via the OpenAI API as our primary model for all resume 
parsing tasks, with structured JSON output mode enabled.
```

---

#### 💡 Rationale

- **Reason 1:** GPT-4o's JSON output mode guarantees structured responses — critical for parsing into our database schema without post-processing
- **Reason 2:** Average latency of ~2.1 seconds per resume parse is well within our <5s threshold
- **Reason 3:** At our projected volume (500 users × avg 10 resumes/week), estimated cost is ~$90/month — within budget
- **Reason 4:** The team already has OpenAI API experience — no new SDKs or infrastructure needed
- **Reason 5:** OpenAI's SOC 2 compliance and data processing agreement (DPA) meets our initial privacy requirements

---

#### 🔀 Alternatives Considered

##### Option 1 — Claude 3.5 Sonnet (Anthropic)

| | Detail |
|---|---|
| **What it is** | Anthropic's mid-tier model, known for strong reasoning and instruction-following |
| **Pros** | Slightly cheaper per token; excellent at structured tasks; strong safety defaults |
| **Cons** | Team has no prior experience with Anthropic SDK; JSON mode less mature at the time of evaluation; would add ~1 day of integration time we don't have |

##### Option 2 — Llama 3 70B (Self-hosted via Groq)

| | Detail |
|---|---|
| **What it is** | Open-source LLM hosted on Groq's fast inference infrastructure |
| **Pros** | Near-zero token cost; very fast inference (~0.8s/request); no data sent to third parties |
| **Cons** | Lower accuracy on complex structured extraction in our evals (82% vs GPT-4o's 96%); requires managing Groq API keys and rate limits; free tier has strict limits |

##### Option 3 — Fine-tuned GPT-4o-mini

| | Detail |
|---|---|
| **What it is** | A smaller, cheaper model fine-tuned on our own resume examples |
| **Pros** | Would reduce cost by ~70% once trained; faster inference |
| **Cons** | Requires 500+ labelled training examples we don't have; 3–4 week delay to collect and train; not viable for MVP timeline |

---

#### ⚠️ Risk Assessment

| Field | Value |
|---|---|
| **Risk Level** | 🟡 Medium |
| **Risk Description** | OpenAI API outages or price increases could affect availability and cost projections |
| **Mitigation Plan** | 1) Implement a fallback to GPT-4o-mini for basic parsing if GPT-4o is unavailable. 2) Set a cost alert at $120/month (80% of budget). 3) Abstract the LLM call behind an internal service so we can swap providers without changing product code. |
| **Probability** | Low (OpenAI SLA is 99.9%) |
| **Impact if it happens** | High — resume parsing is the core feature; an outage degrades the core UX |

---

#### 🔁 Reversal Cost

| Field | Value |
|---|---|
| **Reversal Cost** | `Moderate` |
| **Reversal Notes** | Switching to a different LLM provider would require updating the API client, prompt formatting, and output parsing layer. Estimated effort: 2–3 days. Our internal service abstraction reduces this from Hard to Moderate. |

---

#### 🤖 AI-Specific Fields

##### Model / Tool Selection

| Field | Value |
|---|---|
| **Model / Tool Chosen** | `GPT-4o` via OpenAI API (model: `gpt-4o-2024-08-06`) |
| **Why This Model** | Best structured extraction accuracy (96% on our 50-resume eval set); JSON mode; team familiarity |
| **Models Evaluated** | GPT-4o, Claude 3.5 Sonnet, Llama 3 70B via Groq, GPT-4o-mini |
| **Benchmark / Eval Results** | GPT-4o: 96% field-extraction accuracy on 50 labelled resumes; Llama 3 70B: 82%; GPT-4o-mini: 89% |

##### Prompt Strategy

| Field | Value |
|---|---|
| **Prompt Approach** | Few-shot (3 examples) + JSON output mode |
| **System Prompt Summary** | The system prompt instructs the model to act as a structured data extractor, output only valid JSON, and never hallucinate missing fields — use `null` for absent data |
| **Prompt Version** | `v1.0` |
| **Prompt File / Location** | `/prompts/resume_parser_v1.0.txt` |

##### Data, Privacy & Safety

| Field | Value |
|---|---|
| **Data Used** | User-uploaded resume PDFs (converted to plain text before sending to API) |
| **PII / Sensitive Data?** | Yes — resumes contain names, emails, phone numbers, addresses |
| **Data Retention Policy** | Raw text is sent to OpenAI API and not stored by us after parsing. Parsed JSON is stored in our DB for 90 days unless user deletes their account. |
| **Privacy Compliance** | GDPR — we have signed OpenAI's DPA; users consent to AI processing in our ToS |
| **Safety Guardrails** | System prompt instructs model to extract only factual data, not make judgements about candidates |
| **Bias Checks Done?** | Planned — we will run a bias audit on parsed outputs across 5 demographic groups in Sprint 3 |
| **Red-Teaming Done?** | Yes — tested with adversarial inputs (e.g., resumes designed to inject instructions). Model correctly ignored injected text. |

##### Cost & Latency Trade-offs

| Field | Value |
|---|---|
| **Estimated Cost Per Request** | ~$0.0018 per resume parsed (avg 900 input tokens + 200 output tokens) |
| **Estimated Monthly AI Cost at MVP Scale** | ~$90/month at 500 users × 10 resumes/week |
| **Average Latency** | 2.1 seconds per resume (measured across 100 test calls) |
| **Acceptable Latency Threshold** | < 5 seconds |
| **Cost Optimisation Plan** | At $120/month: switch simple single-field queries to GPT-4o-mini. At $150/month: implement a request cache for duplicate resumes. At 1,000+ users: evaluate fine-tuning GPT-4o-mini on our dataset. |

---

#### 🖊️ Sign-Off Chain & RACI Matrix

##### Sign-Off Chain

| Role | Name | Date | Status |
|---|---|---|---|
| **Proposer (R)** | Alice Chen (Lead Engineer) | `2026-10-05` | Proposed |
| **Reviewer 1 (C)** | Bob Marsh (Product) | `2026-10-06` | Approved — confirmed accuracy threshold meets user expectations |
| **Decision Maker (A)** | Alice Chen (Founder / Lead Eng) | `2026-10-07` | Approved |

##### RACI Matrix

| Name / Role | RACI Code | Notes |
|---|---|---|
| Alice Chen (Lead Engineer) | R, A | Owns implementation and final decision |
| Bob Marsh (Product) | C | Confirmed user experience requirements |
| Investor Monthly Update | I | Noted in October update email |

---

#### 🛠️ Implementation Notes

| Field | Value |
|---|---|
| **Action Items** | 1. Create OpenAI project and generate API key. 2. Implement `LLMService.parseResume()` wrapper. 3. Write prompt and store at `/prompts/resume_parser_v1.0.txt`. 4. Enable JSON output mode. 5. Add cost alert webhook at $120/month in OpenAI dashboard. |
| **Owner(s)** | Alice Chen |
| **Target Implementation Date** | `2026-10-14` |
| **Actual Implementation Date** | `2026-10-13` |
| **PR / Commit / Branch** | `feat/resume-parsing-llm` — merged to `main` |
| **Docs / Config Updated?** | Yes — `.env.example` updated with `OPENAI_API_KEY` placeholder; README updated with LLM setup instructions |

---

#### 📅 Review & Outcome

| Field | Value |
|---|---|
| **Review Date** | `2026-11-15` |
| **Reviewed On** | `2026-11-16` |
| **Outcome** | 🟢 Good call |
| **What Happened** | Parsing accuracy held at 94% on real user resumes (slightly below our 96% lab result but above our 90% threshold). Actual cost was $78/month at 420 active users — under budget. Average latency improved to 1.8s after we optimised the prompt to reduce input token count. |
| **Lessons Learned** | Lab eval accuracy (96%) was slightly optimistic vs production (94%) because lab resumes were cleaner. Next time, include messier real-world samples in the eval set. |
| **Superseded By** | — |

---

#### 🕓 Decision Entry Changelog

| Version | Date | Edited By | What Changed |
|---|---|---|---|
| 1.0 | `2026-10-05` | Alice Chen | Initial entry created |
| 1.1 | `2026-10-13` | Alice Chen | Updated Actual Implementation Date and PR reference after merge |
| 1.2 | `2026-11-16` | Alice Chen | Filled in Review & Outcome after first-month review |

---

> 🟩 **End of example.** Copy the Decision Entry Template from Section 3 for your real entries below.

---

### `DEC-A-002` — *(Your next architecture decision goes here)*

*(Paste a completed Decision Entry Template here)*

---

## 🧪 Phase 3: Development, QA & Safety

> **What this phase is about:**
> You are building and validating the product. Decisions here are about feature prioritisation,
> sprint scope, testing strategy, AI evaluation frameworks, safety guardrails, and quality benchmarks.
>
> **Example decisions in this phase:**
> - "We will cut the 'team collaboration' feature from v1 and ship it in v1.1."
> - "We will use a 95% pass rate on our eval suite as the threshold before any AI model upgrade goes live."
> - "We will red-team the AI for jailbreaking and prompt injection before beta launch."
> - "We will require a human-in-the-loop review for all AI outputs above a confidence threshold of 0.7."

---

### `DEC-V-001` — *(Your first dev/QA decision goes here)*

*(Paste a completed Decision Entry Template here)*

---

### `DEC-V-002` — *(Add more as needed)*

*(Paste a completed Decision Entry Template here)*

---

## 🚀 Phase 4: Launch & Post-Launch (0–500 Customers)

> **What this phase is about:**
> You have shipped — now you are learning from real users and growing. Decisions here are about
> the launch strategy, onboarding, pricing adjustments, feedback-driven pivots, scaling infrastructure,
> and responding to real-world usage of your AI features.
>
> **Example decisions in this phase:**
> - "We will do a soft launch to 50 beta users before opening signups publicly."
> - "We will increase our Supabase plan from Free to Pro after reaching 200 users."
> - "Based on user feedback, we will pivot the AI output format from a report to a bullet-point summary."
> - "We will implement rate limiting at 50 AI requests/user/day after one user accidentally spent $80 in tokens."

---

### `DEC-L-001` — *(Your first launch decision goes here)*

*(Paste a completed Decision Entry Template here)*

---

### `DEC-L-002` — *(Add more as needed)*

*(Paste a completed Decision Entry Template here)*

---

---

# 📚 Section 5 — Appendix

## A. Glossary

| Term | Plain-English Definition |
|---|---|
| **ADR** | Architectural Decision Record — a document (like this one) that logs a key design or technical decision |
| **AI / LLM** | Artificial Intelligence / Large Language Model — the AI brain powering features like text generation, classification, or summarisation |
| **Chain-of-Thought** | A prompting technique where you ask the AI to "think step by step" to improve accuracy |
| **Context Window** | How much text an AI model can read and remember at once (measured in tokens) |
| **GDPR / CCPA** | Privacy laws in Europe / California that control how you handle personal user data |
| **GTM** | Go-To-Market — your strategy for reaching and acquiring customers |
| **Guardrails** | Rules and filters that prevent an AI from producing harmful, offensive, or out-of-scope outputs |
| **MVP** | Minimum Viable Product — the simplest version of your product you can ship to real users |
| **PII** | Personally Identifiable Information — data that can identify a real person (name, email, phone number, etc.) |
| **Prompt** | The instruction or question you send to an AI model |
| **RAG** | Retrieval-Augmented Generation — a technique where the AI searches a knowledge base before answering |
| **Red-Teaming** | Deliberately trying to break or misuse your AI to find vulnerabilities before bad actors do |
| **Reversal Cost** | How hard it would be to undo a decision if it turns out to be wrong |
| **Sprint** | A fixed period (usually 1–2 weeks) in which your team works toward a specific set of goals |
| **Tech Stack** | The combination of technologies (programming languages, databases, frameworks) used to build the product |
| **Token** | The unit of text that AI models process — roughly ¾ of a word; you are billed by token usage |

---

## B. Decision ID Quick-Generator

Use this formula every time you create a new decision:

```
DEC - [Phase Code] - [Next Number in that Phase]

Phase codes:
  D = Discovery & Ideation
  A = Architecture & AI Design
  V = Development, QA & Safety
  L = Launch & Post-Launch

Example sequence:
  DEC-D-001, DEC-D-002, DEC-D-003 ...
  DEC-A-001, DEC-A-002 ...
  DEC-V-001 ...
  DEC-L-001 ...
```

---

## C. Decision Health Checklist

> Run through this checklist before marking any decision as **Approved**.

- [ ] The decision title is specific enough that a stranger knows what was decided
- [ ] The problem statement is written as a clear question
- [ ] The decision is written as one unambiguous sentence
- [ ] Customer Impact is filled in (Direct / Indirect / Internal only)
- [ ] At least 2 alternatives were considered and documented
- [ ] Risk level is set and a mitigation plan exists for Medium/High risks
- [ ] Reversal cost is assessed
- [ ] For AI decisions: model, prompt version, cost estimate, and safety considerations are all filled in
- [ ] RACI matrix is filled in — exactly one person/role is Accountable (A)
- [ ] The sign-off chain has at least a Proposer and a Decision Maker
- [ ] A Review Date is set
- [ ] The Decision Entry Changelog has at least a v1.0 row
- [ ] The Summary Index (Section 2) has been updated

---

## D. When to Create a New Decision Entry

> Ask yourself: *"If someone new joined the team tomorrow, would they be confused about why we made this choice?"*
> If the answer is **yes** — log the decision.

**Always log decisions about:**
- Choosing a technology, tool, or vendor
- Cutting or changing a feature
- Changing the product's target user or pricing
- Choosing an AI model, prompt strategy, or data handling policy
- Any choice that costs more than 1 day of engineering effort to reverse
- Any external commitment (partnership, public API, data contract)

**You can skip logging for:**
- Naming a variable
- Minor copy changes
- Internal refactors that don't change behaviour
- Decisions that can be undone in under an hour

---

## E. Changelog

> Track major changes to this *template itself* (not the decisions inside it).

| Version | Date | Changed By | What Changed |
|---|---|---|---|
| 1.0 | `YYYY-MM-DD` | *(Your name)* | Initial template created |
| | | | |

---

*Template designed for AI-Driven Development Life Cycle — Discovery through first 500 customers.*
*Covers: Technical · Product · Business · AI-Specific decisions.*
*Approval flow: Proposed → Under Review → Approved → Implemented → Superseded.*
