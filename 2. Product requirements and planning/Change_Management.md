# 📋 HOW TO FILL THIS DOCUMENT (Read This First!)

> **Who is this for?** Anyone on the team — engineer, designer, product manager, or even a new intern — who is making a change to the product. You don't need to be a tech expert. Just answer the questions honestly.
>
> **When do I fill this?** Fill this BEFORE you make any change that could affect the product, its AI systems, or its users. Even a small change.
>
> **How long does it take?** 10–30 minutes depending on how big the change is.
>
> **Step-by-step:**
> 1. 📄 Copy this file. Rename it: `YYYY-MM-DD_Short-Change-Title_CHG-XXX.md` (e.g., `2026-10-14_Update-Pricing-Page_CHG-042.md`)
> 2. ✏️ Replace every `[FILL IN: ...]` placeholder with your real answer.
> 3. 🚫 If a section does not apply, write `N/A — [one sentence why]` instead of deleting it.
> 4. 📤 Submit for approval BEFORE touching production.
> 5. ✅ After the change is live, come back and fill in Sections 10 & 11.
> 6. 📅 Add your change to the **Change Calendar** (Section 14) so the team can see what's planned.
>
> **Emojis in this doc are just visual guides — feel free to remove them when filing officially.**

---

## 🗂️ Git Workflow for This Template

> **One file per change. All files live in your repo under `/docs/changes/`.**

```
your-repo/
└── docs/
    └── changes/
        ├── _template/
        │   └── Change_Management.md        ← This master template (never edit directly)
        ├── 2026-10-14_Update-Pricing-Page_CHG-042.md
        ├── 2026-10-20_Swap-Model-GPT4o-Claude_CHG-043.md
        └── ...
```

**Git commit message convention:**
```
chg(CHG-042): [Draft] Update pricing page prompt — awaiting approval
chg(CHG-042): [Approved] Update pricing page prompt — deploying tonight
chg(CHG-042): [Closed] Update pricing page prompt — successfully deployed
```

**Branch naming:** `change/CHG-042-update-pricing-page`

**PR title:** `[CHG-042] Update Pricing Page Prompt — Change Record`

---

# Change Management Record

| Field | Value |
|-------|-------|
| **Document ID** | `CHG-[FILL IN: Sequential number, e.g., 042]` |
| **Document Version** | `v1.0` *(increment to v1.1, v2.0 when you revise this record)* |
| **Date Submitted** | `[FILL IN: YYYY-MM-DD]` |
| **Date Last Updated** | `[FILL IN: YYYY-MM-DD]` |
| **Product / Project Name** | `[FILL IN: e.g., "AcmeBot AI Assistant"]` |
| **Current Phase** | `[FILL IN: Development / Internal Testing / Beta / Launch / Post-Launch]` |
| **Customer Stage** | `[FILL IN: e.g., "0 customers (dev only)" / "125 of 500 early customers"]` |
| **Change Owner** | `[FILL IN: Full Name + Email of the ONE person responsible]` |
| **Submitted By** | `[FILL IN: Full Name + Email — may be same as Change Owner]` |
| **Compliance Tags** | `[FILL IN: check all that apply → SOC 2 / ISO 27001 / HIPAA / GDPR / None]` |

---

## Section 1 — Change Overview

> 🧒 **Think of it like this:** Imagine you're telling a 10-year-old what you're about to do to the product and why. Be simple and clear.

### 1.1 What is the change?

> *Write 2–4 sentences. What exactly will be different after this change? What are you adding, removing, fixing, or updating?*

```
[FILL IN: Example — "We are updating the AI assistant's system prompt to stop it from
hallucinating product prices. The new prompt adds a strict instruction: 'Only state prices
that appear in the provided database context.' No code changes are involved."]
```

### 1.2 Why is this change needed?

> *What problem does it solve? What would happen if you did NOT make this change?*

```
[FILL IN: Example — "Users have reported the AI quoting wrong prices, leading to 3 support
tickets this week. If not fixed, customers lose trust and may churn. The risk of NOT changing
is higher than the risk of making the change."]
```

### 1.3 Change Type

> *Pick the ONE type that best describes this change. If it's a mix, pick the dominant one and note the secondary type in parentheses.*

- [ ] 🤖 **AI Change** — Prompt update, model swap, agent reconfiguration, dataset change, eval tuning
- [ ] 🚀 **Feature Release** — New feature, UI update, new workflow, new integration
- [ ] 🐛 **Bug Fix / Hotfix** — Fixing a defect; hotfix = urgent production fix done same day
- [ ] 🏗️ **Infrastructure / DevOps** — Cloud, CI/CD pipeline, database, environment, security config
- [ ] 📋 **Policy / Process** — Change to a document, workflow, or internal process (no code change)
- [ ] 🔁 **Rollback** — Reverting a previous change back to an earlier known-good state

**Secondary type (if any):** `[FILL IN or N/A]`

### 1.4 Priority Level

> *How urgent is this? Pick one.*

- [ ] 🔴 **Critical / Emergency** — Production is broken or users are harmed RIGHT NOW. Skip normal queue. Notify owner immediately.
- [ ] 🟠 **High** — Significant impact; must be completed within 24–48 hours.
- [ ] 🟡 **Medium** — Important but not blocking; scheduled within the current sprint (1–2 weeks).
- [ ] 🟢 **Low** — Nice to have; can wait for the next planned release cycle.

**Reason for this priority level:**
```
[FILL IN: e.g., "Medium — the bug is annoying but has a workaround. Targeting next sprint."]
```

---

## Section 2 — Change Classification & Risk Rating

> 🧒 **Think of it like this:** Before you cross a road, you look both ways to check how dangerous it is. This section is your "look both ways" check.

### 2.1 Risk Level

> *Rate this change. When in doubt, go one level HIGHER to be safe.*

| Risk Level | What it means | Examples |
|------------|--------------|---------|
| 🟢 **Low** | Unlikely to break anything; easy to reverse | Typo fix, color change, minor copy edit |
| 🟡 **Medium** | Could affect a feature or a subset of users | New optional feature behind a flag, minor infra tweak |
| 🟠 **High** | Could break core functionality or affect many users | Major feature release, model swap, database migration |
| 🔴 **Critical** | Could cause data loss, major outage, or compliance breach | Production database drop, payment system change, PII schema change |

**Selected Risk Level:** `[FILL IN: 🟢 Low / 🟡 Medium / 🟠 High / 🔴 Critical]`

**Why this risk level?**
```
[FILL IN: e.g., "High — swapping from GPT-4o to Claude 3.5 Sonnet affects every user
interaction. We don't fully know how output quality will shift until regression tests run."]
```

### 2.2 Change Scope

> *How far does this change reach? Tick all that apply.*

- [ ] Single service / microservice
- [ ] Multiple services (list them): `[FILL IN]`
- [ ] Frontend / UI
- [ ] Backend / API
- [ ] Database / Data model
- [ ] AI Layer (prompt, model, agent, embeddings)
- [ ] CI/CD pipeline / Infrastructure
- [ ] Third-party integration / vendor API
- [ ] Customer-facing (users will notice)
- [ ] Internal only (users will NOT notice)

### 2.3 Compliance Impact

> *Does this change touch any regulated area? Tick all that apply and explain briefly.*

| Regulation | Triggered? | Why / What's affected |
|------------|-----------|----------------------|
| SOC 2 (CC8.1 — Change Management) | ☐ Yes ☐ No | `[FILL IN if Yes]` |
| ISO 27001 (A.8.32 — Change Management) | ☐ Yes ☐ No | `[FILL IN if Yes]` |
| HIPAA §164.312(b) — Audit Controls | ☐ Yes ☐ No | `[FILL IN if Yes]` |
| GDPR — Data Processing / PII | ☐ Yes ☐ No | `[FILL IN if Yes]` |
| Other: `[FILL IN]` | ☐ Yes ☐ No | `[FILL IN if Yes]` |

> **Audit Note:** Every "Yes" above means this completed change record becomes an **audit evidence artifact**. Do not delete or modify this file after it is approved and implemented.

---

## Section 3 — AI-Specific Change Details

> 🧒 **Think of it like this:** AI systems are like recipes. Even a tiny change to an ingredient (like a prompt or a model) can make the dish taste completely different. This section tracks those recipe changes carefully.
>
> ⚠️ **Skip this section only if your change type is NOT AI-related.** Write `N/A — This is a [type] change with no AI component.`

### 3.1 Change Category (AI)

- [ ] **Prompt / Agent Versioning** — Changing the system prompt, user prompt template, agent instructions, or chain configuration
- [ ] **Model Swap** — Replacing the underlying LLM (e.g., GPT-4o → Claude 3.5, or upgrading a version)
- [ ] **Dataset / Training Data Change** — Modifying, adding to, or retracting training data, fine-tuning datasets, or RAG knowledge bases
- [ ] **AI Output / Eval Regression** — Changing evaluation benchmarks, scoring rubrics, or automated eval pipelines
- [ ] **Agent Tool / Permission Change** — Modifying which tools an AI agent can call, or its permission boundaries
- [ ] **Embedding / Vector Store Change** — Updating embeddings model or vector database contents

### 3.2 Prompt / Agent Version Tracking

> *Fill this in every time a prompt or agent config changes — even a single word.*

| Field | Details |
|-------|---------|
| **Previous Prompt / Config Version** | `[FILL IN: e.g., v2.3.1 or Git commit SHA abc1234]` |
| **New Prompt / Config Version** | `[FILL IN: e.g., v2.4.0]` |
| **What changed in the prompt/config?** | `[FILL IN: e.g., "Added instruction: 'Never state prices not in context.' Removed instruction: 'Be creative with estimates.'"]` |
| **Where is the prompt stored?** | `[FILL IN: e.g., Git repo path, Bedrock Prompt Management, LangSmith, or file path]` |
| **Semantic version bump reason** | `[FILL IN: Patch (typo/wording) / Minor (new instruction) / Major (complete rewrite)]` |

### 3.3 Model Swap Details

> *Fill this in only if changing the underlying AI model. Otherwise write N/A.*

| Field | Details |
|-------|---------|
| **Previous Model** | `[FILL IN: e.g., "gpt-4o-2024-11-20"]` |
| **New Model** | `[FILL IN: e.g., "claude-3-5-sonnet-20241022"]` |
| **Reason for swap** | `[FILL IN: e.g., cost reduction / better accuracy / vendor contract / new capability]` |
| **Context window change?** | `[FILL IN: e.g., 128k → 200k tokens — impacts chunking logic]` |
| **API compatibility confirmed?** | ☐ Yes ☐ No — `[FILL IN any breaking changes]` |
| **Cost impact estimate** | `[FILL IN: e.g., "Estimated 30% cost reduction; ~$0.003 less per 1k output tokens"]` |

### 3.4 Dataset / Training Data Change

> *Fill this in only if training data, RAG knowledge base, or fine-tuning data is changing. Otherwise write N/A.*

| Field | Details |
|-------|---------|
| **Dataset name / ID** | `[FILL IN]` |
| **Previous dataset version** | `[FILL IN]` |
| **New dataset version** | `[FILL IN]` |
| **What data was added?** | `[FILL IN: e.g., "Added 500 new FAQ pairs from customer support tickets Oct 2026"]` |
| **What data was removed?** | `[FILL IN: e.g., "Removed deprecated pricing data from 2024"]` |
| **PII or sensitive data involved?** | ☐ Yes — describe: `[FILL IN]` ☐ No |
| **Data lineage / source documented?** | ☐ Yes — link: `[FILL IN]` ☐ No |

### 3.5 AI Output Regression Testing

> *Every AI change must pass regression testing BEFORE going to production. No exceptions.*

| Test | Required | Status Before Change | Status After Change |
|------|----------|---------------------|---------------------|
| **Accuracy / Quality Score** (e.g., ROUGE, human eval, LLM-as-judge) | ✅ Required | `[FILL IN: e.g., 84% pass rate]` | `[FILL IN after testing]` |
| **Hallucination / Factuality Rate** | ✅ Required | `[FILL IN]` | `[FILL IN after testing]` |
| **Latency / Response Time (P95)** | ✅ Required | `[FILL IN: e.g., 1.2s]` | `[FILL IN after testing]` |
| **Token Cost per Request** | ✅ Required | `[FILL IN]` | `[FILL IN after testing]` |
| **Safety / Harmful Output Rate** | ✅ Required | `[FILL IN]` | `[FILL IN after testing]` |
| **Eval Dataset Used** | ✅ Required | `[FILL IN: dataset name + version]` | *(same dataset)* |
| **Regression Pass Threshold** | ✅ Required | `[FILL IN: e.g., "Must be ≥ previous score on all 5 metrics"]` | `[FILL IN: Pass / Fail]` |

**Regression Test Result:** ☐ PASS — safe to promote ☐ FAIL — do NOT promote; investigate

**Notes:**
```
[FILL IN: e.g., "Latency improved by 18%. Accuracy score dropped 1.2% on dataset v3.
Within acceptable threshold. Approved to promote."]
```

---

## Section 4 — Technical Implementation Plan

> 🧒 **Think of it like this:** This is your step-by-step recipe for HOW you'll make the change happen — like a cooking recipe but for software.

### 4.1 Pre-Implementation Checklist

> *Complete these BEFORE making any change. Check each box when done.*

- [ ] Feature flag / toggle created and set to OFF in production
- [ ] Change tested in local development environment
- [ ] Change tested in staging / QA environment (mirror of production)
- [ ] All automated tests (unit, integration, E2E) pass in staging
- [ ] AI regression tests pass (Section 3.5) — required for AI changes
- [ ] Database migration script reviewed and tested on a copy (if applicable)
- [ ] Secrets / API keys rotated or confirmed current (if infrastructure change)
- [ ] Third-party vendor APIs confirmed compatible (if integration change)
- [ ] Rollback procedure tested and confirmed working (Section 5)
- [ ] Change window communicated to team (time, date, expected downtime if any)
- [ ] On-call / incident responder identified and available during rollout
- [ ] This change record approved by Change Owner (Section 7)

### 4.2 Implementation Steps

> *Write the exact steps in order. Be specific enough that someone who has never done this before could follow them. Number every step.*

```
[FILL IN: Example —
Step 1: Merge PR #142 (prompt-v2-4-0-pricing-fix) into main branch.
Step 2: CI/CD pipeline triggers automatically. Confirm all tests pass in the pipeline.
Step 3: Deploy to staging environment. Smoke test manually for 15 minutes.
Step 4: Flip feature flag `use_prompt_v2_4_0` to ON for 5% of production traffic (canary).
Step 5: Monitor error rates and latency on Datadog for 30 minutes.
Step 6: If all metrics are green, ramp feature flag to 50%, then 100% over the next 2 hours.
Step 7: Mark deployment complete. Update this record with "Implemented" status.
]
```

### 4.3 Implementation Window

| Field | Details |
|-------|---------|
| **Planned Start Date/Time** | `[FILL IN: YYYY-MM-DD HH:MM UTC]` |
| **Planned End Date/Time** | `[FILL IN: YYYY-MM-DD HH:MM UTC]` |
| **Estimated Duration** | `[FILL IN: e.g., 2 hours]` |
| **Expected User Downtime** | `[FILL IN: e.g., "None — zero-downtime deployment" or "5–10 min maintenance window"]` |
| **Low-traffic window?** | ☐ Yes — `[FILL IN: why this time is low-traffic]` ☐ No — explain: `[FILL IN]` |
| **Person Executing Change** | `[FILL IN: Name + contact]` |
| **Person On-Call / Watching** | `[FILL IN: Name + contact]` |

### 4.4 Infrastructure & Environment Details

| Environment | Status Before Change | Status After Change |
|-------------|---------------------|---------------------|
| **Development** | `[FILL IN]` | `[FILL IN]` |
| **Staging / QA** | `[FILL IN]` | `[FILL IN]` |
| **Production** | `[FILL IN]` | `[FILL IN]` |

**Feature Flag Name (if used):** `[FILL IN: e.g., use_prompt_v2_4_0]`
**Rollout Strategy:** `[FILL IN: e.g., Canary — 5% → 25% → 50% → 100% over 4 hours]`

---

## Section 5 — Rollback Plan

> 🧒 **Think of it like this:** A rollback is your "undo button." This section answers: "If everything goes wrong, how do we go back to how things were?"
>
> ⚠️ **Every change MUST have a rollback plan before it can be approved. No exceptions.**

### 5.1 Rollback Trigger Conditions

> *List the exact conditions that should automatically or manually trigger a rollback. Be specific with numbers.*

```
[FILL IN: Example —
AUTOMATIC TRIGGERS (CI/CD / Feature Flag system triggers these):
- Error rate exceeds 1% for more than 5 consecutive minutes
- P95 response latency exceeds 3 seconds for more than 5 minutes
- Health check endpoint returns non-200 for 3 consecutive checks

MANUAL TRIGGERS (Human decides to roll back):
- AI output safety rate drops below 99.5%
- More than 3 customer reports of same issue within 1 hour
- On-call engineer determines change is causing harm
]
```

### 5.2 Rollback Steps

> *Write the exact steps to undo this change. Test these steps in staging BEFORE the change goes live.*

```
[FILL IN: Example —
Step 1: Flip feature flag `use_prompt_v2_4_0` immediately to OFF (takes effect within 30 seconds).
Step 2: Verify error rate drops back to baseline within 5 minutes.
Step 3: If rollback is due to feature flag, no redeployment needed — done.
Step 4: If a code deployment also happened, revert via: git revert <commit-sha> and redeploy.
Step 5: Notify Change Owner and team via [communication channel] within 15 minutes of rollback.
Step 6: Open a post-mortem document (see Section 10).
]
```

### 5.3 Rollback Details

| Field | Details |
|-------|---------|
| **Rollback Method** | `[FILL IN: Feature Flag / Git Revert / Blue-Green Traffic Shift / Database Snapshot Restore]` |
| **Automated or Manual?** | `[FILL IN: e.g., "Automated via feature flag; manual git revert as backup"]` |
| **Last Known-Good Version** | `[FILL IN: e.g., Git commit SHA abc123 or prompt v2.3.1]` |
| **Rollback Time Estimate** | `[FILL IN: e.g., "< 5 minutes for feature flag flip; 20 minutes for full git revert + redeploy"]` |
| **Rollback Tested in Staging?** | ☐ Yes — tested on: `[date]` ☐ No — explain: `[FILL IN]` |
| **Data Reversible?** | ☐ Yes ☐ No — explain: `[FILL IN: e.g., "Database migration is irreversible. Backup taken at step 0."]` |

### 5.4 Backup & Snapshot

| Item | Backup Location | Taken When |
|------|----------------|-----------|
| Database snapshot | `[FILL IN]` | `[FILL IN: e.g., "Automatically 1 hour before deployment"]` |
| Prompt / config backup | `[FILL IN]` | `[FILL IN]` |
| Infrastructure state backup | `[FILL IN]` | `[FILL IN]` |
| AI model weights / version pin | `[FILL IN]` | `[FILL IN]` |

---

## Section 6 — Testing & Quality Assurance

> 🧒 **Think of it like this:** Before a pilot flies a new plane, engineers check every single part. This section is your quality check before "takeoff."

### 6.1 Testing Completed

> *All boxes should be checked BEFORE requesting approval. Explain any unchecked box.*

| Test Type | Required For | Completed? | Pass/Fail | Evidence Link |
|-----------|-------------|-----------|-----------|---------------|
| Unit Tests | All code changes | ☐ Yes ☐ No ☐ N/A | `[P/F]` | `[FILL IN: link or "see CI run #123"]` |
| Integration Tests | API / service changes | ☐ Yes ☐ No ☐ N/A | `[P/F]` | `[FILL IN]` |
| End-to-End (E2E) Tests | User-facing changes | ☐ Yes ☐ No ☐ N/A | `[P/F]` | `[FILL IN]` |
| AI Regression Tests | All AI changes | ☐ Yes ☐ No ☐ N/A | `[P/F]` | `[FILL IN]` |
| Security Scan (SAST/DAST) | High/Critical changes | ☐ Yes ☐ No ☐ N/A | `[P/F]` | `[FILL IN]` |
| Load / Performance Test | Infrastructure changes | ☐ Yes ☐ No ☐ N/A | `[P/F]` | `[FILL IN]` |
| Manual Smoke Test | All changes | ☐ Yes ☐ No ☐ N/A | `[P/F]` | `[FILL IN]` |
| Accessibility Check | UI/UX changes | ☐ Yes ☐ No ☐ N/A | `[P/F]` | `[FILL IN]` |

### 6.2 Known Issues / Accepted Risks

> *Are there any known issues, edge cases, or accepted risks going into this change? If yes, list them here and explain why you're proceeding anyway.*

```
[FILL IN: Example — "Known: The new model performs 2% worse on German-language queries.
Accepted: Our current user base is 98% English-speaking. Will be addressed in CHG-045."]
```

---

## Section 7 — Approval Workflow

> 🧒 **Think of it like this:** Before a doctor performs surgery, another doctor checks the plan. This section records who approved the change and when.

### 7.1 Approval Decision

| Role | Name | Decision | Date | Signature / Initials |
|------|------|----------|------|---------------------|
| **Change Owner** (required) | `[FILL IN]` | ☐ Approved ☐ Rejected ☐ Needs Changes | `[FILL IN]` | `[FILL IN]` |
| **Technical Reviewer** (required for High/Critical) | `[FILL IN or N/A]` | ☐ Approved ☐ Rejected ☐ Needs Changes | `[FILL IN]` | `[FILL IN]` |
| **Security / Compliance** (required if compliance tag) | `[FILL IN or N/A]` | ☐ Approved ☐ Rejected ☐ Needs Changes | `[FILL IN]` | `[FILL IN]` |

### 7.2 Rejection / Change Request Notes

> *If the approver said "Rejected" or "Needs Changes," record their feedback here so it's not lost.*

```
[FILL IN: or "N/A — Approved on first submission."]
```

### 7.3 Emergency Override

> *Only for Critical / Emergency changes where there is no time to follow the normal approval flow.*

- **Was an emergency override used?** ☐ Yes ☐ No
- **Reason for override:** `[FILL IN]`
- **Post-emergency approval obtained from:** `[FILL IN: Name + Date]`
- **Time between override and post-approval:** `[FILL IN: e.g., "2 hours"]`

> ⚠️ Emergency overrides must ALWAYS be followed by a post-emergency approval within 24 hours. This is a SOC 2 and ISO 27001 requirement.

---

## Section 8 — Customer Impact Assessment

> 🧒 **Think of it like this:** Your first 500 customers are like the first 500 guests at a new restaurant. A bad experience for any of them could spread fast. This section makes sure you've thought about every way this change could affect them.

### 8.1 Impact Summary

| Question | Answer |
|----------|--------|
| **Will users experience any downtime?** | ☐ Yes — duration: `[FILL IN]` ☐ No |
| **Will users see different behavior after this change?** | ☐ Yes — describe: `[FILL IN]` ☐ No |
| **Could this change cause data loss for users?** | ☐ Yes — mitigated by: `[FILL IN]` ☐ No |
| **Does this change affect user billing or payments?** | ☐ Yes — describe: `[FILL IN]` ☐ No |
| **Does this change affect user privacy or PII?** | ☐ Yes — describe: `[FILL IN]` ☐ No |
| **Could AI output change in ways users will notice?** | ☐ Yes — describe: `[FILL IN]` ☐ No |

### 8.2 Affected User Segments

> *Who specifically might be affected? Be as precise as you can.*

```
[FILL IN: Example —
- ALL users: Will see slightly faster response times (good impact)
- Users on Free plan: No change
- Users on Pro plan: Will see new "Generate Report" button (new feature)
- Users in the EU: Privacy policy footnote updated to reflect new model vendor
]
```

**Estimated number of users affected (out of current total):** `[FILL IN: e.g., "~120 of 210 current beta users"]`

### 8.3 Customer Communication Plan

> *What will you tell customers, if anything? When and how?*

| Channel | Message Summary | Send When | Sent By |
|---------|----------------|-----------|---------|
| `[FILL IN: e.g., In-app banner]` | `[FILL IN: e.g., "We improved response accuracy — enjoy!"]` | `[FILL IN: e.g., After deploy, same day]` | `[FILL IN: Name]` |
| `[FILL IN: e.g., Email newsletter]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN: e.g., Status page]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

**If NO customer communication is planned, explain why:**
```
[FILL IN: e.g., "Change is invisible to users — backend prompt update only. No user-facing
behavior change confirmed by regression testing."]
```

### 8.4 Support Team Briefing

> *Does the support team need to know about this change so they can handle incoming questions?*

- **Support team briefed?** ☐ Yes — briefed on: `[date]` ☐ No — reason: `[FILL IN]`
- **New FAQ / knowledge base article needed?** ☐ Yes — link: `[FILL IN]` ☐ No
- **Expected increase in support volume?** ☐ Yes — estimate: `[FILL IN]` ☐ No

---

## Section 9 — Monitoring & Success Criteria

> 🧒 **Think of it like this:** After a rocket launches, mission control watches a bunch of screens to make sure everything is OK. This section defines what "OK" looks like for your change.

### 9.1 Success Metrics

> *How will you know this change worked? Define clear, measurable targets.*

| Metric | Baseline (Before) | Target (After) | Alert Threshold (triggers rollback) |
|--------|------------------|----------------|--------------------------------------|
| `[FILL IN: e.g., Error rate]` | `[FILL IN: e.g., 0.2%]` | `[FILL IN: e.g., ≤ 0.2%]` | `[FILL IN: e.g., > 1% for 5 min]` |
| `[FILL IN: e.g., API latency P95]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN: e.g., AI accuracy score]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN: e.g., User-reported bugs]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN: e.g., Cost per request]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

### 9.2 Monitoring Setup

| What is being monitored | Tool / Dashboard | Who monitors it | For how long after deploy |
|------------------------|-----------------|----------------|--------------------------|
| `[FILL IN: e.g., API error rates]` | `[FILL IN: e.g., TBD / Datadog / CloudWatch]` | `[FILL IN: Name]` | `[FILL IN: e.g., 24 hours]` |
| `[FILL IN: e.g., AI output safety]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN: e.g., Customer support tickets]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

**Monitoring review frequency:** `[FILL IN: e.g., Every 30 min for first 4 hours, then daily for 1 week]`

---

## Section 10 — Implementation Record

> 📌 **Fill this section AFTER the change is implemented.** Come back and update this file.

### 10.1 Deployment Log

| Event | Date/Time (UTC) | Performed By | Notes |
|-------|----------------|--------------|-------|
| Pre-deployment checklist completed | `[FILL IN]` | `[FILL IN]` | |
| Change deployed to staging | `[FILL IN]` | `[FILL IN]` | |
| Staging smoke test passed | `[FILL IN]` | `[FILL IN]` | |
| Canary rollout started (% of traffic) | `[FILL IN]` | `[FILL IN]` | `[FILL IN: e.g., 5% canary started]` |
| Full rollout to 100% | `[FILL IN]` | `[FILL IN]` | |
| Feature flag confirmed ON in production | `[FILL IN]` | `[FILL IN]` | |
| Monitoring period started | `[FILL IN]` | `[FILL IN]` | |
| Change declared SUCCESSFUL | `[FILL IN]` | `[FILL IN]` | |

**Was a rollback required?** ☐ Yes — `[FILL IN: what happened, see Section 10.2]` ☐ No

### 10.2 Rollback Record (fill only if rollback occurred)

| Field | Details |
|-------|---------|
| **Rollback triggered at** | `[FILL IN: date/time UTC]` |
| **Triggered by** | `[FILL IN: Automated system / Person name]` |
| **Trigger condition that fired** | `[FILL IN: exact metric or observation]` |
| **Rollback completed at** | `[FILL IN: date/time UTC]` |
| **Total time to recover** | `[FILL IN: e.g., 8 minutes]` |
| **Users impacted during incident** | `[FILL IN: e.g., "~45 users saw errors for 8 min"]` |
| **Root cause (initial assessment)** | `[FILL IN]` |
| **Follow-up change record created?** | ☐ Yes — ID: `[FILL IN]` ☐ No |

---

## Section 11 — Post-Implementation Review (PIR)

> 🧒 **Think of it like this:** After a game, teams review what went well and what they could do better next time. This is your team's "game tape review."
>
> 📌 **Complete within 5 business days of the change going live.** Required for all High and Critical changes. Recommended for all others.

### 11.1 Outcome Summary

**Overall result:** ☐ Fully successful ☐ Partially successful (issues encountered) ☐ Unsuccessful (rolled back)

**Brief summary:**
```
[FILL IN: Example — "Change deployed successfully with zero downtime. AI accuracy improved
by 3.1% above baseline. Token cost reduced 12%. Two minor edge cases discovered in
German-language queries (tracked in CHG-045). Monitoring will continue for 5 more days."]
```

### 11.2 Success Metrics — Actual Results

| Metric | Baseline | Target | Actual Result | Pass? |
|--------|---------|--------|---------------|-------|
| `[copy from 9.1]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | ☐ Yes ☐ No |
| | | | | |

### 11.3 Lessons Learned

> *What did you learn from this change? Even if it went perfectly, what could be done faster or better next time?*

**What went well?**
```
[FILL IN: e.g., "Feature flag rollout worked exactly as planned. Canary detected zero issues.
Having a pre-tested rollback gave the team confidence to proceed."]
```

**What could be improved?**
```
[FILL IN: e.g., "The regression eval dataset was too small (only 50 examples). We need ≥ 200
examples to catch edge cases like the German-language issue. Will expand dataset before CHG-045."]
```

**Action items from this PIR:**

| Action Item | Owner | Due Date | Linked to |
|------------|-------|----------|-----------|
| `[FILL IN: e.g., Expand eval dataset to 200+ examples]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN: e.g., CHG-045]` |
| | | | |

### 11.4 PIR Sign-Off

| Role | Name | Sign-Off Date |
|------|------|--------------|
| Change Owner | `[FILL IN]` | `[FILL IN]` |
| Technical Reviewer (if applicable) | `[FILL IN or N/A]` | `[FILL IN or N/A]` |

---

## Section 12 — Audit Trail & Compliance Evidence

> 📌 This section is auto-completed as you fill the rest of the document. Review before closing the record.

> ⚠️ **DO NOT DELETE OR MODIFY THIS FILE** after it has been approved and implemented. It serves as a compliance audit evidence artifact for SOC 2 (CC8.1), ISO 27001 (A.8.32), and HIPAA (§164.312(b)).

### 12.1 Evidence Checklist

- [ ] Change rationale documented (Section 1.2)
- [ ] Risk assessment completed (Section 2)
- [ ] Compliance impact assessed (Section 2.3)
- [ ] AI-specific controls documented (Section 3) — or marked N/A
- [ ] Testing evidence referenced (Section 6.1)
- [ ] Rollback plan documented and tested (Section 5)
- [ ] Approval obtained from authorized person (Section 7)
- [ ] Customer impact assessed (Section 8)
- [ ] Implementation log filled in (Section 10)
- [ ] Post-implementation review completed (Section 11)

### 12.2 Linked Artifacts

> *List all related documents, tickets, PRs, and records that are part of this change's evidence package.*

| Artifact Type | Title / ID | Link / Location |
|--------------|-----------|----------------|
| Pull Request / Code Review | `[FILL IN: e.g., PR #142]` | `[FILL IN: link]` |
| CI/CD Pipeline Run | `[FILL IN: e.g., Build #507]` | `[FILL IN: link]` |
| AI Regression Test Report | `[FILL IN]` | `[FILL IN]` |
| Staging Test Evidence | `[FILL IN]` | `[FILL IN]` |
| Security Scan Report | `[FILL IN or N/A]` | `[FILL IN or N/A]` |
| Customer Communication Sent | `[FILL IN or N/A]` | `[FILL IN or N/A]` |
| Related Ticket / Issue | `[FILL IN: e.g., JIRA-1042 or GitHub Issue #88]` | `[FILL IN]` |
| Previous Change Record | `[FILL IN: e.g., CHG-041 — prior model version]` | `[FILL IN]` |

---

## Section 13 — Change Log (Document History)

> *Every time you edit this document, add a row here. This is how auditors and team members can see what changed in the record itself.*

| Version | Date | Changed By | What Changed |
|---------|------|-----------|--------------|
| v1.0 | `[FILL IN]` | `[FILL IN]` | Initial submission |
| | | | |

---

## Section 14 — Change Calendar

> 🧒 **Think of it like this:** Imagine a school timetable, but instead of classes, it shows when each team's changes are going live. This stops two big changes from happening at the same time and causing confusion.
>
> 📌 **This section lives in ONE shared file** — not in each individual change record. Keep a `CHANGE_CALENDAR.md` file at `docs/changes/CHANGE_CALENDAR.md` and update it whenever a new change record is created or its schedule changes.
>
> **How to use:** Add one row per change. Update the Status column as the change moves through the lifecycle.

### 14.1 Upcoming & Active Changes

| CHG ID | Change Title | Type | Owner | Risk | Planned Deploy | Status | Notes |
|--------|-------------|------|-------|------|---------------|--------|-------|
| `CHG-XXX` | `[FILL IN]` | `AI / Feature / Bug / Infra` | `[Name]` | `🟢/🟡/🟠/🔴` | `YYYY-MM-DD` | `Draft / Approved / In-Progress / Done / Rolled Back` | `[FILL IN]` |
| | | | | | | | |

### 14.2 Blackout Windows

> *List periods when NO changes should go to production — holidays, high-traffic events, board presentations, compliance audits, etc.*

| Period | Start | End | Reason | Approved By |
|--------|-------|-----|--------|-------------|
| `[FILL IN: e.g., Holiday freeze]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN: e.g., SOC 2 audit window]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| `[FILL IN: e.g., Product launch week]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |

### 14.3 Change Frequency Limits

> *These limits protect your first 500 customers from "change fatigue" — too many changes at once confuses both users and the support team.*

| Environment | Max changes per day | Max changes per week | Notes |
|-------------|--------------------|--------------------|-------|
| Production | `[FILL IN: e.g., 3]` | `[FILL IN: e.g., 10]` | `[FILL IN: adjust based on team size]` |
| Staging | No limit | No limit | Staging is safe to experiment |
| AI (prompt/model) | `[FILL IN: e.g., 1]` | `[FILL IN: e.g., 3]` | AI changes need 24h observation window |

---

## Section 15 — Stakeholder Register

> 🧒 **Think of it like this:** Before a concert, the stage manager has a list of who needs to know what — the lighting team, the sound team, the performers. This section is your "who needs to know" list for every type of change.
>
> 📌 **This section also lives in ONE shared file** — keep it at `docs/changes/STAKEHOLDER_REGISTER.md` and update it when the team grows or roles change.

### 15.1 Stakeholder Map by Change Type

> *For each change type, list who must be Informed (I), Consulted (C), or must Approve (A). This is called a RACI-lite model.*
>
> - **A = Approves** — Must sign off. Change cannot proceed without them.
> - **C = Consulted** — Their input is needed. Loop them in during planning.
> - **I = Informed** — They need to know after decisions are made. Don't block on them.

| Role / Person | AI Change | Feature Release | Bug Fix / Hotfix | Infra Change |
|--------------|-----------|-----------------|-----------------|--------------|
| **Change Owner** | A | A | A | A |
| **Lead Engineer / Tech Lead** | C | C | I | A |
| **Product Manager** | C | A | I | I |
| **QA Lead** | C | C | C | C |
| **Security / Compliance Officer** | I | I | I | A |
| **Customer Support Lead** | I | I | I | I |
| **CEO / Founder** (Critical only) | I | I | I | A |
| **End Users / Customers** | I | I | I | I |

> ✏️ Customize the roles above to match your team. Add rows for your actual names/emails.

### 15.2 Stakeholder Contact Directory

> *Fill this in once and keep it updated. Reference names in other sections by their Role title.*

| Role | Name | Email | Backup Contact | Best Way to Reach |
|------|------|-------|---------------|------------------|
| Change Owner | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN: e.g., Slack @username]` |
| Tech Lead | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Product Manager | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| QA Lead | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Security / Compliance | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| Customer Support Lead | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` |
| On-Call Engineer | `[FILL IN]` | `[FILL IN]` | `[FILL IN]` | `[FILL IN: PagerDuty / Phone]` |

### 15.3 Notification Templates

> *Use these as starting points. Copy, fill in the blanks, and send.*

**🟡 Standard Change Notification (send to: I-list, 24h before)**
```
Subject: [CHG-XXX] Planned Change: [Change Title] — [YYYY-MM-DD]

Hi team,

We are planning to deploy [brief description] on [date] at [time UTC].

What changes for you: [one sentence — or "Nothing visible to you."]
Expected downtime: [None / X minutes]
Rollback plan: [Yes, automated via feature flag]

Questions? Reach out to [Change Owner name] at [email/Slack].
```

**🔴 Emergency Change Notification (send immediately to: A and C list)**
```
Subject: 🚨 [EMERGENCY CHG-XXX] [Change Title] — Deploying NOW

URGENT — We are making an emergency change to production right now.

Reason: [one sentence — what broke]
Change being made: [one sentence]
Rollback ready: [Yes/No]
ETA to resolve: [X minutes]

Change Owner: [Name] | On-call: [Name]
Updates every 15 min in [channel/thread].
```

**✅ Change Complete Notification (send after successful deploy)**
```
Subject: ✅ [CHG-XXX] Complete: [Change Title]

The change has been successfully deployed.

What happened: [one sentence summary]
Users affected: [number or "none"]
Monitoring: Active for next [X hours]

Post-implementation review: [date]
Questions? [Change Owner contact]
```

---

## Section 16 — Risk Matrix

> 🧒 **Think of it like this:** Imagine a danger map. The further right on the map (more likely to happen) AND the further up (worse outcome), the more careful you need to be.

### 16.1 How to Use the Risk Matrix

**Step 1:** Estimate the **Likelihood** that something goes wrong (1 = Very Unlikely → 5 = Almost Certain)
**Step 2:** Estimate the **Impact** if it does go wrong (1 = Barely noticeable → 5 = Catastrophic)
**Step 3:** Multiply: `Risk Score = Likelihood × Impact`
**Step 4:** Find your risk level in the table below

### 16.2 Risk Score Matrix

```
         │      IMPACT (How bad if it happens?)
         │  1-Minor  2-Low   3-Medium  4-High  5-Critical
─────────┼──────────────────────────────────────────────────
5-Almost │    5       10       15        20       25 🔴
Certain  │
         │
4-Likely │    4        8       12        16 🟠   20 🔴
         │
3-Possible│   3        6        9 🟡     12 🟠   15 🔴
         │
2-Unlikely│   2        4        6        8 🟡    10 🟠
         │
1-Rare   │   1        2        3         4        5 🟡
─────────┴──────────────────────────────────────────────────
          LIKELIHOOD (How likely is something to go wrong?)
```

| Score Range | Risk Level | Action Required |
|-------------|-----------|----------------|
| 1–4 | 🟢 **Low** | Document and monitor. Standard change process. |
| 5–9 | 🟡 **Medium** | Require tested rollback plan. Schedule in low-traffic window. |
| 10–16 | 🟠 **High** | Require technical reviewer sign-off. Canary rollout mandatory. 24h monitoring. |
| 17–25 | 🔴 **Critical** | Change Owner + Security approval required. Executive notification. Tested rollback rehearsed in staging. |

### 16.3 Risk Assessment for This Change

> *Fill this in for the change you are documenting. Use it to validate the risk level you selected in Section 2.1.*

| Risk Factor | Likelihood (1–5) | Impact (1–5) | Score | Notes |
|------------|-----------------|-------------|-------|-------|
| `[FILL IN: e.g., Deployment fails mid-way]` | `[#]` | `[#]` | `[L×I]` | `[FILL IN]` |
| `[FILL IN: e.g., AI outputs degrade in quality]` | `[#]` | `[#]` | `[L×I]` | `[FILL IN]` |
| `[FILL IN: e.g., Rollback takes longer than expected]` | `[#]` | `[#]` | `[L×I]` | `[FILL IN]` |
| `[FILL IN: e.g., Customer data affected]` | `[#]` | `[#]` | `[L×I]` | `[FILL IN]` |
| `[FILL IN: Add more rows as needed]` | | | | |

**Highest risk score:** `[FILL IN]` → **Final risk level:** `[🟢 / 🟡 / 🟠 / 🔴]`

> ✅ Verify this matches what you selected in Section 2.1. If they don't match, update Section 2.1.

---

## Quick-Reference Glossary

> 🧒 **Not sure what a word means? Check here first.**

| Term | Plain-English Explanation |
|------|--------------------------|
| **Change Record** | This document. A written proof that a change was planned, approved, and tracked. |
| **Feature Flag** | An on/off switch in code. Lets you turn a new feature on for some users without deploying new code. Think of it like a light switch. |
| **Canary Deployment** | Rolling out a change to 5% of users first. If nothing breaks, you roll out to everyone else. Named after canaries miners used to detect danger. |
| **Rollback** | Pressing the "undo" button on a change. Going back to the version that was working before. |
| **Regression Testing** | Running tests to make sure new changes didn't break things that were already working. |
| **P95 Latency** | The response time that 95 out of 100 requests are faster than. A way to measure "typical worst case" speed. |
| **SOC 2** | A security standard that proves your company has good controls. Auditors check your change records. |
| **ISO 27001** | An international information security standard. Requires evidence that changes are controlled. |
| **HIPAA** | U.S. law protecting patient health data. Requires audit logs of system changes. |
| **PIR** | Post-Implementation Review. A debrief after a change to learn what went well and what to improve. |
| **Prompt Versioning** | Tracking every change made to an AI's instructions, just like tracking code changes in Git. |
| **LLM** | Large Language Model — the AI brain (e.g., GPT-4, Claude, Gemini). |
| **SAST / DAST** | Automated security scanning tools. SAST scans code before it runs; DAST tests a running app. |
| **PII** | Personally Identifiable Information — data that can identify a real person (name, email, SSN, etc.). |
| **Eval** | Short for "evaluation." Testing the quality of AI outputs using a benchmark dataset. |

---

---

## Companion Files (Create These in Your Repo)

When you set up this template in your Git repo, create these three companion files alongside it:

```
docs/changes/
├── _template/
│   └── Change_Management.md          ← This file (master template — never edit)
├── CHANGE_CALENDAR.md                 ← Copy Section 14 here; shared across all changes
├── STAKEHOLDER_REGISTER.md            ← Copy Section 15 here; shared across all changes
└── RISK_MATRIX.md                     ← Copy Section 16 here; reference for all changes
```

> **Why separate files?** The calendar and stakeholder register are shared resources. Keeping them in one place means everyone updates the same source of truth instead of maintaining duplicates in hundreds of change records.

---

*Template Version: 2.0 | Last Revised: 2026-10-14 | Standard: ITIL v4 / SOC 2 CC8.1 / ISO 27001 A.8.32 / HIPAA §164.312(b)*
*Designed for: AI-Driven Development Life Cycle — Development through First 500 Customers*
*Total Sections: 16 | Companion Files: CHANGE_CALENDAR.md · STAKEHOLDER_REGISTER.md · RISK_MATRIX.md*
