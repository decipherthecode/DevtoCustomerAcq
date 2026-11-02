# 📦 Dependency Management

> **Document Version:** `v1.0.0`
> **Last Updated:** `YYYY-MM-DD`
> **Project Name:** `[Your Project Name Here]`
> **Author:** `[Your Name]`
> **Review Cadence:** Weekly (every Monday)

---

<!-- ============================================================
  HOW TO FILL THIS DOCUMENT — READ ME FIRST!
  ============================================================ -->

# 📖 How to Fill This Document

> **You don't need to be a tech expert to fill this in. Just read each section,
> follow the plain-English instructions inside the `<!-- ... -->` boxes and
> `[square brackets]`, replace the placeholder text with your real information,
> and delete the instruction comment when you're done.**

### Quick Start Checklist

- [ ] **Step 1** — Fill in the header table (project name, version, author).
- [ ] **Step 2** — List every library/package your project uses in Section 4.
- [ ] **Step 3** — List every AI-specific library in Section 5.
- [ ] **Step 4** — Update the Health Dashboard in Section 6 weekly.
- [ ] **Step 5** — Run the Security Audit (Section 7) and attach results.
- [ ] **Step 6** — Set your update rules in Section 8.
- [ ] **Step 7** — Review the Rollback Runbook (Section 12) before every release.
- [ ] **Step 8** — Update the Change Log (Section 15) every time this doc changes.

> 💡 **Think of a dependency like a tool you borrow.**
> If your friend lends you a hammer, you need to know: *which hammer*, *what
> version*, *is it safe to use*, and *what do you do if it breaks?*
> This document is your borrowing ledger.

---

<!-- ============================================================
  SECTION 1 — PROJECT SNAPSHOT
  ============================================================ -->

## 1. 🗂️ Project Snapshot

<!-- Fill in every row below. If a field doesn't apply, write "N/A". -->

| Field | Your Answer |
|---|---|
| **Project Name** | `[e.g., SuperApp]` |
| **Product Type** | `[Web App / Mobile App / Both]` |
| **Primary Language(s)** | `[e.g., TypeScript, Python, Kotlin]` |
| **Framework(s)** | `[e.g., React 18, FastAPI, Jetpack Compose]` |
| **Repository URL** | `[e.g., https://github.com/org/repo]` |
| **Package Manager(s)** | `[e.g., npm, pip + Poetry, Gradle]` |
| **Lock File Location(s)** | `[e.g., /package-lock.json, /backend/poetry.lock]` |
| **Current App Version** | `[e.g., v0.3.1]` |
| **Doc Version** | `v1.0.0` |
| **Document Owner** | `[Your Name + email]` |
| **Backup Reviewer** | `[Teammate Name + email or "None"]` |
| **SBOM Output Path** | `[e.g., /docs/sbom/sbom-v1.0.0.json or "Not generated yet"]` |

---

<!-- ============================================================
  SECTION 2 — WHAT IS A DEPENDENCY? (Beginner Explainer)
  ============================================================ -->

## 2. 🧩 What Is a Dependency? (Plain-English Explainer)

> **Skip this section if you already know.** This is here so anyone — even
> someone new to software — can understand what this document is for.

A **dependency** (also called a *package*, *library*, or *module*) is
**someone else's pre-written code that your project uses**.

### Real-World Analogy

Imagine you're baking a cake. You don't grow the flour yourself — you *buy* it
from a store. That flour is your dependency. If the store changes the recipe for
the flour, your cake might taste different. If the flour is recalled for safety
reasons, you need to stop using it immediately.

Software works the same way:

| Baking Term | Software Term |
|---|---|
| Bag of flour | A package (e.g., `react`, `pandas`, `spring-boot`) |
| Flour brand + weight | Package name + version (e.g., `react@18.2.0`) |
| Expiry date | End-of-life date |
| Recall notice | Security vulnerability (CVE) |
| Ingredient list on the bag | Software Bill of Materials (SBOM) |
| Buying from a known store | Using a trusted registry (npm, PyPI, Maven Central) |

### Types of Dependencies

| Type | What It Means | Example |
|---|---|---|
| **Direct** | A package your code imports directly | `import axios from 'axios'` |
| **Transitive (Indirect)** | A package that *your package* uses — you never imported it yourself | axios internally uses `follow-redirects` |
| **Dev-only** | Only needed while coding/testing — NOT shipped to users | `jest`, `eslint`, `pytest` |
| **Production** | Shipped and running on real servers / user devices | `express`, `django`, `retrofit` |
| **Peer** | Required by a library but installed separately | `react` is a peer dep of `react-dom` |
| **Optional** | Not required, but unlocks extra features | `pdfmake` in some reporting libs |

---

<!-- ============================================================
  SECTION 3 — DEPENDENCY ECOSYSTEM SETUP
  ============================================================ -->

## 3. ⚙️ Dependency Ecosystem Setup

<!-- Fill in the rows that match your project. Delete rows you don't use. -->

### 3.1 Package Managers in Use

| Ecosystem | Tool | Config File | Lock File | Registry |
|---|---|---|---|---|
| JavaScript / TypeScript | `[npm / yarn / pnpm]` | `package.json` | `package-lock.json` / `yarn.lock` / `pnpm-lock.yaml` | `[npmjs.com or private URL]` |
| Python | `[pip / Poetry / uv]` | `pyproject.toml` or `requirements.txt` | `poetry.lock` or `uv.lock` | `[pypi.org or private URL]` |
| Android (Java/Kotlin) | `[Gradle]` | `build.gradle` / `build.gradle.kts` | `gradle.lockfile` (if enabled) | `[Maven Central or private]` |
| iOS (Swift) | `[Swift Package Manager / CocoaPods]` | `Package.swift` / `Podfile` | `Package.resolved` / `Podfile.lock` | `[Swift Package Index / private]` |
| Flutter (Dart) | `[pub]` | `pubspec.yaml` | `pubspec.lock` | `[pub.dev]` |
| Other | `[e.g., Go modules]` | `go.mod` | `go.sum` | `[proxy.golang.org]` |

### 3.2 Lock File Rules

> **Why lock files matter:** A lock file is like a photo of your exact
> ingredients at a moment in time. It guarantees every team member (and your
> server) installs the *exact same* versions. Never delete it.

| Rule | Status |
|---|---|
| Lock file(s) committed to Git | `[ ] Yes  [ ] No  [ ] N/A` |
| Lock file(s) included in CI/CD pipeline | `[ ] Yes  [ ] No  [ ] Not set up yet` |
| Direct installs (no lock file bypass) only | `[ ] Yes  [ ] No` |
| Lock file re-generated on every dependency change | `[ ] Yes  [ ] No` |

---

<!-- ============================================================
  SECTION 4 — DEPENDENCY INVENTORY (MAIN CATALOG)
  ============================================================ -->

## 4. 📋 Dependency Inventory (Main Catalog)

<!-- 
  HOW TO FILL THIS TABLE:
  - Add one row per dependency.
  - Copy the template row as many times as needed.
  - "Type" = Direct / Dev / Transitive / Peer / Optional.
  - "Risk Level" = 🟢 Low / 🟡 Medium / 🔴 High / ⚫ Critical.
  - "Pinned?" = Is the version locked to an exact number (e.g., 18.2.0 vs ^18)?
  - "Last Reviewed" = date you last checked this package is still safe and needed.
  - "Owner" = who on your team is responsible for keeping this updated.
-->

### 4.1 Production Dependencies

| # | Package Name | Version | Ecosystem | Type | Purpose (one line) | Risk Level | Pinned? | Last Reviewed | Owner |
|---|---|---|---|---|---|---|---|---|---|
| 1 | `[e.g., react]` | `[e.g., 18.2.0]` | JS/TS | Direct | UI rendering framework | 🟢 Low | Yes | `YYYY-MM-DD` | `[Name]` |
| 2 | `[e.g., axios]` | `[e.g., 1.6.8]` | JS/TS | Direct | HTTP client | 🟢 Low | Yes | `YYYY-MM-DD` | `[Name]` |
| 3 | `[e.g., fastapi]` | `[e.g., 0.111.0]` | Python | Direct | Web API framework | 🟢 Low | Yes | `YYYY-MM-DD` | `[Name]` |
| 4 | `[package name]` | `[x.y.z]` | `[Ecosystem]` | `[Type]` | `[What does it do?]` | `[🟢/🟡/🔴/⚫]` | `[Yes/No]` | `YYYY-MM-DD` | `[Name]` |

> ➕ **Add more rows as needed. Copy the last row and fill it in.**

### 4.2 Development / Test-Only Dependencies

| # | Package Name | Version | Ecosystem | Purpose | Last Reviewed | Owner |
|---|---|---|---|---|---|---|
| 1 | `[e.g., jest]` | `[e.g., 29.7.0]` | JS/TS | Unit testing | `YYYY-MM-DD` | `[Name]` |
| 2 | `[e.g., pytest]` | `[e.g., 8.2.0]` | Python | Unit testing | `YYYY-MM-DD` | `[Name]` |
| 3 | `[e.g., eslint]` | `[e.g., 9.0.0]` | JS/TS | Code linting | `YYYY-MM-DD` | `[Name]` |
| 4 | `[package name]` | `[x.y.z]` | `[Ecosystem]` | `[Purpose]` | `YYYY-MM-DD` | `[Name]` |

### 4.3 Mobile-Specific Dependencies

<!-- Fill this in only if your project includes iOS/Android/Flutter apps. -->

| # | Package Name | Version | Platform | Type | Purpose | Risk Level | Last Reviewed |
|---|---|---|---|---|---|---|---|
| 1 | `[e.g., retrofit]` | `[e.g., 2.11.0]` | Android | Direct | HTTP networking | 🟢 Low | `YYYY-MM-DD` |
| 2 | `[e.g., alamofire]` | `[e.g., 5.9.1]` | iOS | Direct | HTTP networking | 🟢 Low | `YYYY-MM-DD` |
| 3 | `[e.g., dio]` | `[e.g., 5.4.3]` | Flutter | Direct | HTTP networking | 🟢 Low | `YYYY-MM-DD` |

---

<!-- ============================================================
  SECTION 5 — AI-SPECIFIC DEPENDENCIES
  ============================================================ -->

## 5. 🤖 AI-Specific Dependencies

> **Why a separate section?** AI libraries move *extremely fast*. A model that
> was state-of-the-art last month may be deprecated today. Breaking changes
> happen often. This section keeps all AI-related packages in one place so you
> can watch them more closely.

### 5.1 AI SDK & Model Client Libraries

<!-- These are the official SDKs you use to call AI models (OpenAI, Anthropic, etc.) -->

| # | Package | Version | Provider | Purpose | Pinned? | Breaking Change Risk | Last Reviewed |
|---|---|---|---|---|---|---|---|
| 1 | `[e.g., openai]` | `[e.g., 1.30.0]` | OpenAI | GPT-4o API client | Yes | 🟡 Medium | `YYYY-MM-DD` |
| 2 | `[e.g., anthropic]` | `[e.g., 0.28.0]` | Anthropic | Claude API client | Yes | 🟡 Medium | `YYYY-MM-DD` |
| 3 | `[e.g., google-generativeai]` | `[e.g., 0.6.0]` | Google | Gemini API client | Yes | 🟡 Medium | `YYYY-MM-DD` |
| 4 | `[e.g., transformers]` | `[e.g., 4.41.0]` | HuggingFace | Local model inference | Yes | 🔴 High | `YYYY-MM-DD` |

### 5.2 AI Orchestration & Agent Framework Libraries

<!-- These are libs that help you chain AI calls, build agents, or manage prompts. -->

| # | Package | Version | Purpose | Pinned? | Notes |
|---|---|---|---|---|---|
| 1 | `[e.g., langchain]` | `[e.g., 0.2.6]` | Agent chains and prompt orchestration | Yes | `[Any known issues?]` |
| 2 | `[e.g., crewai]` | `[e.g., 0.36.0]` | Multi-agent workflow automation | Yes | `[Any known issues?]` |
| 3 | `[e.g., llama-index]` | `[e.g., 0.10.50]` | RAG (Retrieval-Augmented Generation) | Yes | `[Any known issues?]` |
| 4 | `[e.g., langgraph]` | `[e.g., 0.1.14]` | Stateful agent graphs | Yes | `[Any known issues?]` |

### 5.3 AI Code Generation Tools in Use

<!-- Track which AI coding assistants generate code for this project — they can introduce new deps automatically! -->

| Tool | Version / Tier | Who Uses It | Risk: Unreviewed Deps? | Review Process |
|---|---|---|---|---|
| `[e.g., GitHub Copilot]` | `[e.g., Business]` | `[e.g., All devs]` | `[Yes / No / Sometimes]` | `[e.g., All AI-suggested imports reviewed in PR]` |
| `[e.g., Cursor]` | `[e.g., Pro]` | `[e.g., Solo dev]` | `[Yes / No / Sometimes]` | `[e.g., Run npm audit after every session]` |
| `[e.g., Claude]` | `[e.g., API]` | `[e.g., Automation scripts]` | `[Yes / No / Sometimes]` | `[e.g., Check package name for typosquatting]` |

> ⚠️ **AI-Generated Dependency Warning:** AI coding assistants sometimes suggest
> packages that are:
> - Outdated or unmaintained
> - Misspelled (typosquatting attack — a malicious package with a similar name)
> - Unnecessary (the same feature exists in a package you already have)
>
> **Rule:** Always run `npm audit`, `pip-audit`, or `gradle dependencyCheckAnalyze`
> after an AI assistant adds a new package.

---

<!-- ============================================================
  SECTION 6 — DEPENDENCY HEALTH DASHBOARD
  ============================================================ -->

## 6. 🩺 Dependency Health Dashboard

> **Update this section every Monday.** It's your weekly "health check" for all
> packages. Think of it like a doctor's dashboard for your project's borrowings.

**As of:** `YYYY-MM-DD` | **Checked by:** `[Your Name]`

### 6.1 Overall Health Summary

| Metric | Count | Status |
|---|---|---|
| Total production dependencies | `[e.g., 24]` | — |
| Total dev dependencies | `[e.g., 12]` | — |
| Packages with critical CVEs | `[e.g., 0]` | `[🟢 / 🔴]` |
| Packages with high CVEs | `[e.g., 1]` | `[🟢 / 🟡 / 🔴]` |
| Packages > 2 major versions behind | `[e.g., 3]` | `[🟢 / 🟡 / 🔴]` |
| Packages with no update in 12+ months | `[e.g., 2]` | `[🟢 / 🟡 / 🔴]` |
| Packages with incompatible licenses | `[e.g., 0]` | `[🟢 / 🔴]` |
| SBOM last generated | `YYYY-MM-DD` | `[🟢 Current / 🔴 Outdated]` |

### 6.2 Per-Package Status (Key Packages)

<!-- Only list packages that need attention. Green ones don't need to appear here. -->

| Package | Current Version | Latest Version | CVE Count | License | Status | Action Needed |
|---|---|---|---|---|---|---|
| `[e.g., lodash]` | `[4.17.15]` | `[4.17.21]` | `[2 High]` | MIT | 🔴 Needs Update | Upgrade by `YYYY-MM-DD` |
| `[e.g., log4j]` | `[2.14.0]` | `[2.23.1]` | `[0]` | Apache-2.0 | 🟡 Behind | Schedule upgrade |
| `[package name]` | `[x.y.z]` | `[a.b.c]` | `[count]` | `[License]` | `[🟢/🟡/🔴/⚫]` | `[Action]` |

### 6.3 External Dashboard Links

<!-- Link to the live security/dependency tools your project uses. -->

| Tool | Purpose | Link / Command |
|---|---|---|
| Snyk | Vulnerability scanning | `[https://app.snyk.io/org/YOUR_ORG/projects]` |
| Socket.dev | Supply chain attack detection | `[https://socket.dev/dashboard]` |
| FOSSA | License compliance | `[https://app.fossa.com/projects]` |
| Dependabot Alerts | GitHub auto-alerts | `[https://github.com/ORG/REPO/security/dependabot]` |
| Renovate Dashboard | Automated PR tracking | `[https://app.renovatebot.com/dashboard]` |
| `[Your own tool]` | `[Purpose]` | `[URL or CLI command]` |

> 💡 **No tool set up yet?** Run these free commands right now:
> - JS/TS: `npm audit`
> - Python: `pip-audit` (install with `pip install pip-audit`)
> - Android/Java: `./gradlew dependencyCheckAnalyze`

---

<!-- ============================================================
  SECTION 7 — SECURITY & COMPLIANCE (SBOM + AUDITS)
  ============================================================ -->

## 7. 🔐 Security & Compliance

### 7.1 Software Bill of Materials (SBOM)

> **What is an SBOM?** Think of it as the full ingredient list of your app —
> every package, every version, every license. Just like food packaging laws
> require ingredient lists for safety, enterprise software increasingly requires
> SBOMs for legal and security reasons.

| SBOM Field | Your Answer |
|---|---|
| **SBOM Format** | `[SPDX / CycloneDX / Both]` |
| **Generation Tool** | `[e.g., syft, cdxgen, npm sbom --format=cyclonedx]` |
| **Output File Path** | `[e.g., /docs/sbom/sbom-v1.0.0.json]` |
| **Last Generated** | `YYYY-MM-DD` |
| **Stored In** | `[e.g., /docs/sbom/ folder in repo]` |
| **Shared With** | `[e.g., Legal team, Enterprise customers on request]` |
| **Regenerated On** | `[e.g., Every release + every new dep added]` |

**SBOM Generation Commands:**

```bash
# JavaScript / TypeScript (using syft)
syft dir:. -o cyclonedx-json=sbom-js.json

# Python
syft dir:. -o spdx-json=sbom-python.json

# All-in-one (CycloneDX CLI)
cdxgen -o sbom.json -t nodejs
cdxgen -o sbom.json -t python

# Maven / Gradle
./gradlew cyclonedxBom   # requires cyclonedx-gradle plugin
```

### 7.2 Vulnerability Audit Log

<!-- Add a new row every time you run a security audit. -->

| Date | Who Ran It | Tool Used | Total CVEs Found | Critical | High | Medium | Low | Action Taken | Resolved By |
|---|---|---|---|---|---|---|---|---|---|
| `YYYY-MM-DD` | `[Name]` | `[e.g., npm audit]` | `[#]` | `[#]` | `[#]` | `[#]` | `[#]` | `[e.g., Updated lodash to 4.17.21]` | `YYYY-MM-DD` |
| `YYYY-MM-DD` | `[Name]` | `[Tool]` | `[#]` | `[#]` | `[#]` | `[#]` | `[#]` | `[Action]` | `YYYY-MM-DD` |

### 7.3 License Compliance

> **Why licenses matter:** Every open-source package comes with a license.
> Some licenses (like GPL) can require you to open-source *your own* code if you
> use them. This table tracks which licenses are in use.

| License Type | Examples | Can We Use It? | Notes |
|---|---|---|---|
| **MIT** | react, axios, lodash | ✅ Yes — most permissive | No restrictions |
| **Apache 2.0** | TensorFlow, Kubernetes | ✅ Yes | Must include NOTICE file |
| **BSD 2/3-Clause** | Flask, pytest | ✅ Yes | Attribution required |
| **ISC** | npm itself | ✅ Yes | Very permissive |
| **LGPL** | Some Java libs | ⚠️ Check with legal | Dynamic linking usually OK |
| **GPL v2/v3** | Linux kernel modules | ❌ Consult legal first | May force open-sourcing your code |
| **AGPL** | Some DB tools | ❌ Consult legal first | Network use triggers copyleft |
| **Commercial / Proprietary** | Some AI SDKs | ⚠️ Review contract | Must have valid license key |
| `[Other]` | `[Examples]` | `[✅ / ⚠️ / ❌]` | `[Notes]` |

**Packages with non-standard licenses in this project:**

| Package | License | Reviewed By | Approved? | Notes |
|---|---|---|---|---|
| `[package name]` | `[License]` | `[Name]` | `[Yes / No / Pending]` | `[e.g., Checked with legal on YYYY-MM-DD]` |

### 7.4 Supply Chain Security

<!-- These are checks to protect against attackers injecting malicious code into packages. -->

| Check | Status | Tool / Method |
|---|---|---|
| All packages sourced from official registries only | `[ ] Yes  [ ] No` | `[e.g., .npmrc private registry, pip config]` |
| Package checksums / hashes verified | `[ ] Yes  [ ] No` | `[e.g., package-lock.json integrity field]` |
| Typosquatting check for new packages | `[ ] Yes  [ ] No` | `[e.g., Socket.dev, manual name check]` |
| No packages with `install` scripts that run untrusted code | `[ ] Yes  [ ] No` | `[e.g., npm install --ignore-scripts]` |
| Maintainer reputation checked for critical deps | `[ ] Yes  [ ] No` | `[e.g., Check GitHub stars, last commit date]` |
| Pinned digests (SHA) for Docker base images | `[ ] Yes  [ ] No  [ ] N/A` | `[e.g., FROM node:20@sha256:...]` |

---

<!-- ============================================================
  SECTION 8 — UPDATE POLICY & AUTOMATION
  ============================================================ -->

## 8. 🔄 Update Policy & Automation

> **The Golden Rule of Updates:**
> - **Patch** updates (1.0.0 → 1.0.**1**) = almost always safe. Auto-merge.
> - **Minor** updates (1.0.0 → 1.**1**.0) = usually safe. Review before merging.
> - **Major** updates (1.0.0 → **2**.0.0) = breaking changes likely. Always review.

### 8.1 Update Rules

| Update Type | Auto-Merge Allowed? | Requires Review? | Requires Tests to Pass? | Notes |
|---|---|---|---|---|
| **Patch** (x.y.Z) | ✅ Yes | No | Yes (CI must be green) | `[Any exceptions?]` |
| **Minor** (x.Y.z) | No | ✅ Yes | Yes | `[Manual PR review required]` |
| **Major** (X.y.z) | No | ✅ Yes + QA sign-off | Yes + staging deploy | `[Full regression test]` |
| **Security hotfix** | No | ✅ Expedited review | Yes | Apply within 24–72 hrs of critical CVE |
| **AI SDK / Model libs** | No | ✅ Yes — always | Yes + prompt regression | AI packages can break silently |

### 8.2 Automation Tool Configuration

| Tool | Configured? | Config File Location | Auto-Merge Enabled? | Frequency |
|---|---|---|---|---|
| Dependabot | `[ ] Yes  [ ] No` | `.github/dependabot.yml` | Patch only | `[e.g., Weekly]` |
| Renovate Bot | `[ ] Yes  [ ] No` | `renovate.json` | Patch only | `[e.g., Weekly]` |
| `[Other]` | `[ ] Yes  [ ] No` | `[Path]` | `[Yes/No]` | `[Frequency]` |

### 8.3 Dependency Update Workflow

> **How to safely update a package — step by step:**

```
Step 1 → Check what changed: read the CHANGELOG or release notes for the package.
           Example: https://github.com/axios/axios/releases

Step 2 → Update in a new branch (never directly on main).
           Example: git checkout -b deps/update-axios-1.7.0

Step 3 → Run the update command:
           npm update axios          (JS/TS)
           poetry update httpx       (Python)
           ./gradlew dependencies    (Android/Java)

Step 4 → Run all tests: npm test / pytest / ./gradlew test

Step 5 → Run security audit: npm audit / pip-audit

Step 6 → Open a Pull Request with the label "dependency-update".

Step 7 → Merge only after CI is green and at least one reviewer approves.

Step 8 → Update the Inventory table in Section 4 with the new version and date.

Step 9 → Regenerate SBOM if this was a production dependency.
```

---

<!-- ============================================================
  SECTION 9 — CI/CD GATE RULES
  ============================================================ -->

## 9. 🚦 CI/CD Gate Rules

> **A "gate" is a check that must pass before your code can ship.**
> If a gate fails, the deployment stops automatically. This protects users.

### 9.1 Dependency Gates (Blocking)

| Gate | Blocks Deploy? | Tool / Command | Threshold |
|---|---|---|---|
| Critical CVE detected | ✅ YES — hard block | `npm audit --audit-level=critical` | 0 critical CVEs allowed |
| High CVE detected | ✅ YES — hard block | `npm audit --audit-level=high` | 0 high CVEs allowed in production |
| License policy violation | ✅ YES | FOSSA / custom script | 0 GPL in closed-source products |
| Lock file not committed | ✅ YES | Git diff check | Lock file must match manifest |
| SBOM not regenerated | ⚠️ Warning only | CI script | SBOM must be < 7 days old |
| Dep added without review | ✅ YES | PR label check | Must have "dep-reviewed" label |
| Tests fail after update | ✅ YES | Test runner | 100% existing tests must pass |

### 9.2 Sample CI Configuration Snippet

```yaml
# .github/workflows/dependency-check.yml
name: Dependency Security Gate

on: [push, pull_request]

jobs:
  audit:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      # JavaScript / TypeScript audit
      - name: npm audit
        run: npm audit --audit-level=critical
        working-directory: ./frontend

      # Python audit
      - name: pip-audit
        run: |
          pip install pip-audit
          pip-audit --requirement requirements.txt

      # Lock file drift check
      - name: Check lock file is up to date
        run: |
          npm ci --dry-run
          git diff --exit-code package-lock.json

      # SBOM generation (optional — remove if not needed yet)
      - name: Generate SBOM
        run: npx @cyclonedx/cyclonedx-npm --output-file sbom.json
```

> 📝 **Replace `./frontend`** with your actual folder path.
> Add or remove steps to match your tech stack.

---

<!-- ============================================================
  SECTION 10 — WEEKLY AUDIT CHECKLIST
  ============================================================ -->

## 10. ✅ Weekly Audit Checklist

> **Run this every Monday. Takes about 15–30 minutes.**
> Check each box when done. Write your name and date at the top.

**Week of:** `YYYY-MM-DD` | **Performed by:** `[Your Name]`

### 10.1 Vulnerability Check

- [ ] Ran `npm audit` (or yarn/pnpm equivalent) for all JS/TS packages
- [ ] Ran `pip-audit` for all Python packages
- [ ] Ran `./gradlew dependencyCheckAnalyze` for Android/Java (if applicable)
- [ ] Checked Dependabot / Renovate alerts on GitHub/GitLab
- [ ] Checked Snyk / Socket dashboard for new findings
- [ ] Zero critical CVEs confirmed (or documented exceptions below)

**Exceptions / Open Vulnerabilities This Week:**

| Package | CVE ID | Severity | Reason Not Fixed Yet | Fix Target Date |
|---|---|---|---|---|
| `[package]` | `[CVE-YYYY-XXXXX]` | `[Critical/High/Med/Low]` | `[e.g., No patch available yet]` | `YYYY-MM-DD` |

### 10.2 Outdated Package Check

- [ ] Ran `npm outdated` / `pip list --outdated` / `./gradlew dependencyUpdates`
- [ ] Listed packages that are 1+ major version behind
- [ ] Created update tickets / issues for any package > 2 major versions behind

### 10.3 AI Dependency Check

- [ ] Checked latest release notes for all AI SDK packages (OpenAI, Anthropic, etc.)
- [ ] Checked for model deprecation notices (e.g., GPT-3.5 deprecation, Claude 2 EOL)
- [ ] Verified agent framework libs (LangChain, CrewAI) have no breaking changes in latest release
- [ ] Reviewed any new packages introduced by AI coding assistants this week

### 10.4 License & Compliance Check

- [ ] No new packages added with GPL/AGPL license without legal approval
- [ ] FOSSA / license scanner shows no new violations
- [ ] SBOM is up to date (regenerate if any dep changed this week)

### 10.5 Sign-Off

| Reviewer | Date | Notes |
|---|---|---|
| `[Name]` | `YYYY-MM-DD` | `[Any concerns or action items]` |

---

<!-- ============================================================
  SECTION 11 — CUSTOMER PHASE DEPENDENCIES
  (Beta → Launch → First 500 Customers)
  ============================================================ -->

## 11. 🚀 Customer Phase Dependencies

> This section tracks packages that are *specifically important* at each stage
> of getting real users onto your product. Different stages need different tools.

### 11.1 Phase Overview

| Phase | Who's Using It | Dependencies Focus |
|---|---|---|
| **🔬 Alpha / Internal** | Just you and your team | Core framework, CI/CD, testing |
| **🧪 Beta / Private Preview** | Invited early users (< 50) | Feature flags, crash reporting |
| **🌐 Public Launch** | First paying customers | Observability, payments, auth |
| **📈 First 500 Customers** | Growing user base | Scalability, caching, queues |

### 11.2 Beta / Private Preview Dependencies

<!-- These packages help you control who sees what feature, before full launch. -->

| Package | Purpose | Configured? | Notes |
|---|---|---|---|
| `[e.g., LaunchDarkly SDK]` | Feature flags — show features to selected users only | `[ ] Yes  [ ] No` | `[Flag naming conventions, etc.]` |
| `[e.g., PostHog]` | Beta user analytics and session replay | `[ ] Yes  [ ] No` | `[Data residency region]` |
| `[e.g., Sentry]` | Crash and error reporting for beta users | `[ ] Yes  [ ] No` | `[Source maps uploaded?]` |
| `[package name]` | `[Purpose]` | `[ ] Yes  [ ] No` | `[Notes]` |

### 11.3 Launch-Ready Observability Dependencies

<!-- These packages let you see what's happening in production in real time. -->

| Package | Purpose | Configured? | Alert Set Up? | Notes |
|---|---|---|---|---|
| `[e.g., @sentry/node]` | Error tracking | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | `[DSN configured?]` |
| `[e.g., opentelemetry-api]` | Distributed tracing | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | `[Exporter: Jaeger/Datadog?]` |
| `[e.g., pino]` | Structured logging | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | `[Log level in prod: info]` |
| `[e.g., @datadog/datadog-ci]` | APM / metrics | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | `[Agent configured?]` |
| `[package name]` | `[Purpose]` | `[ ] Yes  [ ] No` | `[ ] Yes  [ ] No` | `[Notes]` |

### 11.4 Scalability Dependencies (First 500 Customers)

<!-- These packages help your app handle more users without crashing or slowing down. -->

| Package | Purpose | When to Add | Current Status | Notes |
|---|---|---|---|---|
| `[e.g., ioredis]` | Redis client — caching and sessions | When response times > 500ms | `[Added / Planned / N/A]` | `[Redis host URL configured?]` |
| `[e.g., bullmq]` | Job queue — background task processing | When users wait > 2s for heavy ops | `[Added / Planned / N/A]` | `[Worker count?]` |
| `[e.g., pg-pool]` | PostgreSQL connection pooling | From day 1 in production | `[Added / Planned / N/A]` | `[Pool size?]` |
| `[e.g., aws-sdk]` | AWS SDK — S3, SQS, CloudFront | When storing user files or using CDN | `[Added / Planned / N/A]` | `[IAM role configured?]` |
| `[package name]` | `[Purpose]` | `[Trigger]` | `[Status]` | `[Notes]` |

### 11.5 Authentication & Security Dependencies

| Package | Purpose | Configured? | Notes |
|---|---|---|---|
| `[e.g., next-auth / passport.js]` | User login / OAuth | `[ ] Yes  [ ] No` | `[Providers: Google, GitHub?]` |
| `[e.g., jsonwebtoken]` | JWT token signing | `[ ] Yes  [ ] No` | `[Secret rotation plan?]` |
| `[e.g., helmet]` | HTTP security headers | `[ ] Yes  [ ] No` | `[CSP configured?]` |
| `[e.g., zod]` | Input validation | `[ ] Yes  [ ] No` | `[All user inputs validated?]` |
| `[package name]` | `[Purpose]` | `[ ] Yes  [ ] No` | `[Notes]` |

---

<!-- ============================================================
  SECTION 12 — ROLLBACK RUNBOOK
  ============================================================ -->

## 12. 🔁 Rollback Runbook

> **When to use this:** A dependency update shipped to production and something
> broke. Users are affected. You need to move fast. Follow these steps in order.

### 12.1 Severity Classification

| Severity | Signs | Response Time | Who to Alert |
|---|---|---|---|
| **P0 — Critical** | App is down for all users | Immediately | All hands + stakeholders |
| **P1 — High** | Key feature broken for many users | < 1 hour | Dev lead + QA |
| **P2 — Medium** | Edge case broken, workaround exists | < 4 hours | Dev lead |
| **P3 — Low** | Cosmetic issue or minor slowdown | < 24 hours | Developer |

### 12.2 Step-by-Step Rollback Procedure

```
════════════════════════════════════════════════════
 DEPENDENCY ROLLBACK — STEP BY STEP
════════════════════════════════════════════════════

STEP 1 — IDENTIFY the bad dependency
  → Check recent Dependabot / Renovate PRs that were merged.
  → Check git log for recent lock file changes:
      git log --oneline --follow package-lock.json
      git log --oneline --follow poetry.lock

STEP 2 — CONFIRM the bad version
  → Compare the current lock file to the last working version:
      git diff HEAD~1 package-lock.json   (or poetry.lock, etc.)

STEP 3 — PIN the old version in your manifest
  → package.json:   change "axios": "^1.7.0" to "axios": "1.6.8"
  → pyproject.toml: change httpx = "^0.27" to httpx = "=0.26.0"
  → build.gradle:   pin version string to exact known-good version

STEP 4 — REINSTALL with pinned version
  → JS/TS:   npm ci   (uses lock file exactly)
  → Python:  poetry install
  → Android: ./gradlew dependencies

STEP 5 — VERIFY locally
  → Run all tests: npm test / pytest / ./gradlew test
  → Smoke-test the broken feature manually

STEP 6 — DEPLOY the rollback
  → Create a hotfix branch: git checkout -b hotfix/rollback-dep-PACKAGE-NAME
  → Commit the lock file and manifest changes
  → Push and create an emergency PR (bypass normal review if P0)
  → Deploy immediately to production

STEP 7 — ALERT users (if applicable)
  → Post a status update on your status page / Slack / email

STEP 8 — DOCUMENT the incident in Section 12.3 below

STEP 9 — BEGIN POST-MORTEM (Section 12.4)

════════════════════════════════════════════════════
```

### 12.3 Rollback Incident Log

<!-- Add one row per rollback event. -->

| Date | Package | Bad Version | Rolled Back To | Severity | Duration of Impact | Detected By | Fixed By |
|---|---|---|---|---|---|---|---|
| `YYYY-MM-DD` | `[e.g., axios]` | `[e.g., 1.7.0]` | `[e.g., 1.6.8]` | `[P0/P1/P2/P3]` | `[e.g., 47 minutes]` | `[e.g., Sentry alert]` | `[Name]` |

### 12.4 Post-Mortem Template

> **Fill this in within 48 hours of every P0 or P1 rollback.**
> Be honest and blame-free — the goal is to learn, not to blame.

---

**Post-Mortem — Dependency Incident**
**Date:** `YYYY-MM-DD`
**Severity:** `[P0 / P1]`
**Author:** `[Your Name]`

#### What Happened?
> *(Describe in 2–4 sentences. What broke? Which package? When was it discovered?)*

`[Write your answer here]`

#### Timeline

| Time | Event |
|---|---|
| `HH:MM` | Dependency update deployed to production |
| `HH:MM` | First error detected (by: `[Sentry / user report / monitoring]`) |
| `HH:MM` | Incident declared |
| `HH:MM` | Root cause identified |
| `HH:MM` | Rollback initiated |
| `HH:MM` | Service restored |

#### Root Cause
> *(What specifically in the new package version caused the problem?)*

`[Write your answer here]`

#### Impact
- **Users affected:** `[e.g., All users / users on mobile / admin users only]`
- **Duration:** `[e.g., 1 hour 12 minutes]`
- **Revenue impact:** `[e.g., N/A / Estimated $X]`

#### What Went Well?
- `[e.g., Sentry caught the error within 2 minutes]`
- `[e.g., Rollback took only 8 minutes]`

#### What Needs Improvement?
- `[e.g., No staging environment to catch this first]`
- `[e.g., Major version updates should require more testing]`

#### Action Items

| Action | Owner | Due Date | Done? |
|---|---|---|---|
| `[e.g., Add staging environment]` | `[Name]` | `YYYY-MM-DD` | `[ ]` |
| `[e.g., Add integration test for the affected feature]` | `[Name]` | `YYYY-MM-DD` | `[ ]` |
| `[e.g., Add major-version gate in CI]` | `[Name]` | `YYYY-MM-DD` | `[ ]` |

---

<!-- ============================================================
  SECTION 13 — DEPENDENCY DECISION LOG
  ============================================================ -->

## 13. 📝 Dependency Decision Log

> **Why this section?** Every time you choose to *add*, *remove*, or *reject* a
> package, write down why. Future-you (or your next teammate) will thank you.

| Date | Package | Decision | Reason | Alternatives Considered | Decided By |
|---|---|---|---|---|---|
| `YYYY-MM-DD` | `[e.g., moment.js]` | ❌ Rejected | Deprecated; use day.js instead | `[day.js, date-fns]` | `[Name]` |
| `YYYY-MM-DD` | `[e.g., zod]` | ✅ Added | Best TypeScript-first validation library | `[yup, joi]` | `[Name]` |
| `YYYY-MM-DD` | `[e.g., webpack]` | 🔁 Replaced | Swapped for Vite; 10x faster dev builds | `[esbuild, rollup]` | `[Name]` |
| `YYYY-MM-DD` | `[Package]` | `[✅/❌/🔁]` | `[Reason]` | `[Others considered]` | `[Name]` |

---

<!-- ============================================================
  SECTION 14 — DEPENDENCY RETIREMENT & CLEANUP
  ============================================================ -->

## 14. 🗑️ Dependency Retirement & Cleanup

> **A package you don't use is a package that can attack you.**
> Review this quarterly and remove anything that's no longer needed.

### 14.1 Packages Flagged for Removal

| Package | Reason for Removal | Blocked By | Target Removal Date | Removed? |
|---|---|---|---|---|
| `[e.g., moment.js]` | Deprecated; replaced by day.js | `[Nothing]` | `YYYY-MM-DD` | `[ ] Yes  [ ] No` |
| `[e.g., request]` | Unmaintained since 2020 | `[Dependency of old-lib]` | `YYYY-MM-DD` | `[ ] Yes  [ ] No` |
| `[package name]` | `[Reason]` | `[Blocker or None]` | `YYYY-MM-DD` | `[ ] Yes  [ ] No` |

### 14.2 How to Safely Remove a Package

```
Step 1 → Search your codebase for every import/require of the package:
           grep -r "require('package-name')" ./src
           grep -r "from 'package-name'" ./src

Step 2 → Remove the import from all files.

Step 3 → Uninstall the package:
           npm uninstall package-name
           pip uninstall package-name
           # Remove from build.gradle manually

Step 4 → Run all tests to confirm nothing broke.

Step 5 → Commit the updated lock file and manifest.

Step 6 → Update the Dependency Inventory in Section 4 (remove the row).
```

---

<!-- ============================================================
  SECTION 15 — GLOSSARY
  ============================================================ -->

## 15. 📚 Glossary

> **Not sure what a word means? Look it up here.**

| Term | Plain-English Definition |
|---|---|
| **Dependency** | A piece of code written by someone else that your app uses. Like a borrowed tool. |
| **Package** | A bundle of code, usually downloadable from a registry like npm or PyPI. Same as dependency. |
| **Version** | A specific snapshot of a package. `1.0.0` is different from `1.1.0`. |
| **Semver** | Short for Semantic Versioning. A 3-number system: `MAJOR.MINOR.PATCH`. |
| **Lock file** | A file that freezes the exact versions of all packages so everyone installs the same thing. |
| **Manifest** | The file that *declares* which packages your app needs (e.g., `package.json`, `pyproject.toml`). |
| **Registry** | An online store of packages (e.g., npmjs.com, pypi.org, Maven Central). |
| **CVE** | Common Vulnerabilities and Exposures. A numbered security flaw in a package. |
| **SBOM** | Software Bill of Materials. A complete list of all packages and their versions in your app. |
| **Transitive dependency** | A package used by your package — you didn't install it directly. |
| **Audit** | A check that scans your packages for known security problems. |
| **Pinning** | Locking a package to an exact version (e.g., `18.2.0` instead of `^18`). |
| **Patch update** | A small update that fixes bugs. Usually safe (1.0.0 → 1.0.**1**). |
| **Minor update** | Adds new features, backward-compatible (1.0.0 → 1.**1**.0). |
| **Major update** | Can break things. API may have changed (1.0.0 → **2**.0.0). |
| **Typosquatting** | An attacker publishes a malicious package with a name very similar to a popular one. |
| **Deprecation** | The package author signals they will no longer maintain or update the package. |
| **EOL** | End of Life. The package or framework version will no longer receive security fixes. |
| **FOSSA** | A tool that scans your dependencies for license and vulnerability issues. |
| **Snyk** | A tool that scans your code and dependencies for security vulnerabilities. |
| **Dependabot** | A GitHub bot that automatically opens PRs to update your dependencies. |
| **Renovate** | Similar to Dependabot but more configurable. Opens automated update PRs. |
| **CI/CD** | Continuous Integration / Continuous Delivery. Automated pipelines that test and ship your code. |
| **Gate** | A check in CI/CD that blocks deployment if it fails. |
| **Feature flag** | A switch that lets you turn a feature on/off for specific users without redeploying. |
| **APM** | Application Performance Monitoring. Tools that measure speed and errors in your running app. |
| **RAG** | Retrieval-Augmented Generation. An AI technique that fetches relevant data before generating a response. |

---

<!-- ============================================================
  SECTION 16 — CHANGE LOG
  ============================================================ -->

## 16. 📜 Document Change Log

> **Update this table every time this document is changed.**
> Even small changes count. This is your paper trail.

| Version | Date | Changed By | What Changed |
|---|---|---|---|
| `v1.0.0` | `YYYY-MM-DD` | `[Your Name]` | Initial version created |
| `v1.0.1` | `YYYY-MM-DD` | `[Name]` | `[e.g., Added 3 new packages to inventory]` |
| `v1.1.0` | `YYYY-MM-DD` | `[Name]` | `[e.g., Added rollback incident #1 post-mortem]` |
| `v2.0.0` | `YYYY-MM-DD` | `[Name]` | `[e.g., Major restructure for v2.0 product launch]` |

---

<!-- ============================================================
  APPENDIX A — QUICK-REFERENCE COMMANDS
  ============================================================ -->

## Appendix A: ⚡ Quick-Reference Commands

```bash
# ─── JavaScript / TypeScript ─────────────────────────────────
npm install                     # Install all deps from lock file
npm audit                       # Check for vulnerabilities
npm audit fix                   # Auto-fix safe vulnerabilities
npm outdated                    # List packages with newer versions
npm update PACKAGE_NAME         # Update one package (respects semver range)
npm uninstall PACKAGE_NAME      # Remove a package

# ─── Python (pip + pip-audit) ────────────────────────────────
pip install -r requirements.txt # Install all deps
pip-audit                       # Check for vulnerabilities (pip install pip-audit first)
pip list --outdated             # List outdated packages
pip install --upgrade PACKAGE   # Upgrade one package

# ─── Python (Poetry) ─────────────────────────────────────────
poetry install                  # Install from poetry.lock
poetry update PACKAGE_NAME      # Update one package
poetry show --outdated          # List outdated packages
poetry audit                    # Check for vulnerabilities (needs poetry-audit plugin)

# ─── Android / Java (Gradle) ─────────────────────────────────
./gradlew dependencies          # Show full dependency tree
./gradlew dependencyUpdates     # List available updates (needs ben-manes plugin)
./gradlew dependencyCheckAnalyze # OWASP vulnerability scan

# ─── SBOM Generation ─────────────────────────────────────────
npx @cyclonedx/cyclonedx-npm --output-file sbom.json    # JS/TS
cdxgen -o sbom.json -t python                           # Python
./gradlew cyclonedxBom                                  # Gradle

# ─── Useful Git Commands ─────────────────────────────────────
git log --oneline -10 -- package-lock.json    # Last 10 changes to lock file
git diff HEAD~1 -- package-lock.json          # What changed in last commit
git show HEAD:package-lock.json               # View lock file at last commit
```

---

<!-- ============================================================
  APPENDIX B — TEMPLATE CHECKLIST BEFORE SHARING
  ============================================================ -->

## Appendix B: 📋 "Is This Doc Ready?" Checklist

> Before you share this document with your team or store it in your repo,
> make sure you can check every box below.

**Project Setup**
- [ ] Section 1 (Project Snapshot) is completely filled in
- [ ] Package managers and lock file locations are listed
- [ ] SBOM tool is chosen and command is documented

**Inventory**
- [ ] All production dependencies are in Section 4.1
- [ ] All dev dependencies are in Section 4.2
- [ ] All AI-specific packages are in Section 5
- [ ] Every package has a version, owner, and last-reviewed date

**Security**
- [ ] At least one vulnerability audit has been run and logged in Section 7.2
- [ ] All licenses reviewed; GPL/AGPL packages flagged or cleared
- [ ] SBOM generated and stored at the path listed in Section 7.1

**Health & Process**
- [ ] Health Dashboard (Section 6) is up to date
- [ ] External dashboard links (Snyk, Dependabot, etc.) are filled in
- [ ] CI/CD gate rules are configured (Section 9)
- [ ] Rollback runbook (Section 12) has been read by at least one person

**Documentation**
- [ ] Change Log (Section 16) has an entry for today
- [ ] Document version matches the app version or is independently semver'd

---

*Template designed for AI-Driven Development Life Cycle — from development to first 500 customers.*
*Keep this document in your repository at: `/docs/Dependency_Management.md`*
