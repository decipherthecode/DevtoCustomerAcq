# Performance Benchmarks

> **Document Type:** Performance Benchmarks Template
> **Standard:** AI-Driven Development Life Cycle (AI-SDLC)
> **Scope:** Development → Staging → Beta → 500 Customers
> **Version:** 1.0.0
> **Last Updated:** <!-- YYYY-MM-DD -->
> **Status:** 🟡 Draft | 🟢 Active | 🔴 Deprecated

---

<!-- ============================================================
  HOW TO FILL THIS DOCUMENT
  ============================================================

  # Instructions for Everyone (Even If You Are New to This!)

  Think of this document like a "health checkup report" for your
  software. Just like a doctor tracks your height, weight, and
  heartbeat over time, this document tracks how fast, smart,
  and affordable your AI product is — from the very first line
  of code all the way to your first 500 real customers.

  STEP-BY-STEP GUIDE:
  ─────────────────────────────────────────────────────────────
  STEP 1 ▶ Fill in the PROJECT IDENTITY section (Section 1).
            This tells everyone what product this document is for.

  STEP 2 ▶ Read the GLOSSARY (Section 2). If you see a word
            you don't understand anywhere in this document,
            look it up there first.

  STEP 3 ▶ Set your PERFORMANCE TARGETS (Section 4).
            These are the "passing grades" your product must
            score. If you are unsure, use the ✅ Recommended
            defaults already filled in.

  STEP 4 ▶ Run your tests at each STAGE (Sections 5–8) and
            fill in the "Actual" column in every table.

  STEP 5 ▶ Mark each row ✅ PASS or ❌ FAIL.
            If ANY row is ❌ FAIL → the release is BLOCKED.
            Fix the issue, re-run the test, then update the table.

  STEP 6 ▶ Fill the EXECUTIVE SUMMARY (Section 12) in plain
            English so that anyone — even someone who has never
            read this document — can understand how the product
            is performing.

  STEP 7 ▶ Get sign-off from the required people (Section 13).

  TIPS:
  • Words in CAPITALS like "MUST", "SHOULD", "MAY" have
    specific meanings. MUST = required. SHOULD = strongly
    recommended. MAY = optional.
  • Every cell marked <!-- fill --> needs your input.
  • Every cell marked <!-- auto --> is filled by your test tool.
  • 🔒 cells marked [HARD GATE] will block a release if failed.
  • Copy this file for every new project. Never edit the master.
  ─────────────────────────────────────────────────────────────
-->

---

## Table of Contents

1. [Project Identity](#1-project-identity)
2. [Glossary — Words Made Simple](#2-glossary--words-made-simple)
3. [Benchmark Philosophy](#3-benchmark-philosophy)
4. [Master Performance Targets](#4-master-performance-targets)
5. [Stage 1 — Development & Unit Testing](#5-stage-1--development--unit-testing)
6. [Stage 2 — Staging & Pre-Launch QA](#6-stage-2--staging--pre-launch-qa)
7. [Stage 3 — Beta (1–50 Users)](#7-stage-3--beta-150-users)
8. [Stage 4 — Growth Phase (51–500 Customers)](#8-stage-4--growth-phase-51500-customers)
9. [AI Model Quality Benchmarks](#9-ai-model-quality-benchmarks)
10. [Mobile App Performance Benchmarks](#10-mobile-app-performance-benchmarks)
11. [Cost & Resource Usage Benchmarks](#11-cost--resource-usage-benchmarks)
12. [CI/CD Integration & Automation](#12-cicd-integration--automation)
13. [Trend Tracking Dashboard](#13-trend-tracking-dashboard)
14. [Failure Response Protocol](#14-failure-response-protocol)
15. [Executive Summary](#15-executive-summary)
16. [Sign-Off & Approvals](#16-sign-off--approvals)
17. [Third-Party SLA Tracking](#17-third-party-sla-tracking)
18. [Disaster Recovery & Rollback Plan](#18-disaster-recovery--rollback-plan)
19. [Competitor Benchmark Comparison](#19-competitor-benchmark-comparison)
20. [Changelog](#20-changelog)

---

## 1. Project Identity

> 💡 **Fill this section first.** Think of it as the "cover page" of your report.

| Field | Your Answer |
|---|---|
| **Project / Product Name** | <!-- e.g. "SmartHire AI", "BudgetBot" --> |
| **Version Being Benchmarked** | <!-- e.g. "v1.0.0-beta", "v2.3.1" --> |
| **Document Owner** | <!-- Full name of the person responsible for this doc --> |
| **Engineering Lead** | <!-- Full name --> |
| **QA Lead** | <!-- Full name or "N/A if same as owner" --> |
| **Product Manager** | <!-- Full name --> |
| **Date Benchmarks Started** | <!-- YYYY-MM-DD --> |
| **Target Launch Date** | <!-- YYYY-MM-DD --> |
| **Current Lifecycle Stage** | <!-- Development / Staging / Beta / Growth --> |
| **Product Type** | <!-- Web App / Mobile App / Both --> |
| **AI Model(s) Used** | <!-- e.g. "GPT-4o, Claude 3.5 Sonnet, Llama 3.1" --> |
| **Primary Cloud Provider** | <!-- AWS / GCP / Azure / Self-hosted / Other --> |
| **Repository / Project URL** | <!-- https://github.com/your-org/your-repo --> |
| **Monitoring Dashboard URL** | <!-- Link to Datadog, Grafana, etc. or "Not set up yet" --> |

---

## 2. Glossary — Words Made Simple

> 💡 **Read this before anything else if you are new.** These are the most common words you will see in this document, explained in simple English.

| Word / Term | What It Means in Plain English | Example |
|---|---|---|
| **Benchmark** | A test that measures how well something performs, so you can compare it later | "Our page loads in 1.2 seconds" |
| **Latency** | How long it takes for the app to respond after you do something | Clicking a button → waiting → seeing the result. That wait = latency |
| **Throughput** | How many requests the system can handle per second | "Our API handles 200 requests per second" |
| **P50 (Median)** | Half of users got a response faster than this time, half slower | If P50 = 400ms, 50% of users waited less than 400ms |
| **P95** | 95% of users got a response faster than this. Only 5% waited longer | If P95 = 1.2s, most users are happy; a few had slow days |
| **P99** | 99% of users got a response faster than this. Only 1% waited longer | The "worst case" most teams care about |
| **SLA** | Service Level Agreement — a promise about performance made to customers | "We promise 99.9% uptime" |
| **Uptime / Availability** | The percentage of time the system is working and accessible | 99.9% uptime = only ~9 hours of downtime per year |
| **Error Rate** | What percentage of requests fail (crash, time out, or return wrong data) | "2% error rate" = 2 out of every 100 requests failed |
| **Load Test** | A test where you pretend many users are using the app at the same time | Simulating 500 people clicking at the exact same moment |
| **Concurrent Users** | How many people are using the app at the exact same time | 100 concurrent users = 100 people all online simultaneously |
| **Token** | A small chunk of text the AI model reads or writes (roughly ¾ of a word) | "Hello world" ≈ 3 tokens |
| **TTFT** | Time To First Token — how long until the AI starts typing its response | You ask a question → the AI starts typing. That delay = TTFT |
| **Hallucination** | When an AI confidently says something that is false | AI says "Paris is in Germany" — that's a hallucination |
| **Accuracy** | How often the AI gives a correct, useful, relevant answer | If 90 out of 100 answers are correct, accuracy = 90% |
| **Pass / Fail** | Whether the actual measured number met the target number | Target: < 500ms. Actual: 420ms → ✅ PASS |
| **Hard Gate** | A test that MUST pass before any release. Failure = no release | 🔒 [HARD GATE] means this blocks the entire release |
| **Regression** | When a new code change makes performance worse than before | After update, page load went from 1s → 3s = regression |
| **CDN** | Content Delivery Network — servers around the world that deliver your app faster | Files served from a server close to the user = faster load |
| **Cold Start** | The extra delay when a function/server spins up from zero activity | First request after a quiet period is slower |
| **LCP** | Largest Contentful Paint — when the main content of a web page is visible | A web standard that measures how fast a page looks "loaded" |
| **CLS** | Cumulative Layout Shift — how much the page "jumps around" while loading | Annoying when buttons move right before you click them |
| **FID / INP** | How quickly the page responds to your first click or tap | Slow INP = the app feels "laggy" |
| **FPS** | Frames Per Second (mobile) — how smooth animations appear | 60 FPS = silky smooth. Below 30 FPS = choppy |

---

## 3. Benchmark Philosophy

> 💡 **This section explains the rules of the game. Read it once, then refer back if you are unsure.**

### 3.1 Our Core Principle

Every number in this document is a **promise to our users**. When we hit our targets, users experience a product that feels fast, smart, and reliable. When we miss them, real people get frustrated and leave.

### 3.2 The Four Pillars We Measure

```
┌───────────────────────────────────────────────────────────────┐
│  PILLAR 1           PILLAR 2          PILLAR 3    PILLAR 4    │
│  ⚡ Speed          🧠 AI Quality     📈 Scale    💰 Cost      │
│  How fast?         How smart?        How many?   How much?    │
│                                                               │
│  Latency           Accuracy          Load        Token Cost   │
│  TTFT              Hallucination     Throughput  Cloud Spend  │
│  Page Load         Relevance         Uptime      Memory       │
│  Mobile Render     Bias Check        Error Rate  API Cost     │
└───────────────────────────────────────────────────────────────┘
```

### 3.3 Release Gate Rules

| Gate Level | What It Means | Who Can Override |
|---|---|---|
| 🔒 **HARD GATE** | Test MUST pass. Release is blocked until fixed. | CTO / Engineering Director only |
| ⚠️ **SOFT GATE** | Test SHOULD pass. Team reviews before deciding. | Engineering Lead + PM together |
| 📋 **INFORMATIONAL** | Track for trend data. No release impact. | No override needed |

> **Default rule in this template: ALL gates are 🔒 HARD GATEs unless marked otherwise.**

### 3.4 How Targets Were Set

Targets in this template follow these industry standards:

- **Web Vitals (Google):** LCP < 2.5s, CLS < 0.1, INP < 200ms
- **AI Response:** TTFT < 500ms (conversational), < 2s (complex tasks)
- **API SLA:** P99 < 2s, Error Rate < 1%, Uptime > 99.5%
- **Load:** Support 10× expected peak to avoid surprise outages
- **Cost:** AI token cost < 5% of average monthly revenue per customer

Adjust the targets in Section 4 to match your product's specific needs.

---

## 4. Master Performance Targets

> 💡 **This is the most important table in the document.** Fill in your targets here ONCE. Every stage in Sections 5–8 will refer back to this. The defaults shown are industry-standard starting points.

### 4.1 Speed & Latency Targets

| Metric | Beginner Explanation | Target | Gate |
|---|---|---|---|
| **API P50 Response Time** | Half of users wait less than this | `< 300ms` | 🔒 |
| **API P95 Response Time** | 95% of users wait less than this | `< 800ms` | 🔒 |
| **API P99 Response Time** | 99% of users wait less than this | `< 2,000ms` | 🔒 |
| **AI TTFT (Time to First Token)** | How fast the AI starts replying | `< 500ms` | 🔒 |
| **AI Full Response Time (P95)** | Full AI answer delivered by this time | `< 10s` | ⚠️ |
| **Web Page LCP** | Main content visible to user | `< 2.5s` | 🔒 |
| **Web Page INP** | Page reacts to your first click | `< 200ms` | 🔒 |
| **Web Page CLS** | Page stops jumping around | `< 0.10` | ⚠️ |
| **Mobile App Start Time (Cold)** | App opens from zero in this time | `< 3s` | 🔒 |
| **Mobile App Start Time (Warm)** | App re-opens after being in background | `< 1s` | 🔒 |

> **How to customise:** Replace any value in the `Target` column with your own. Do not change the metric names so that the template stays consistent across projects.

### 4.2 Scalability & Reliability Targets

| Metric | Beginner Explanation | Target | Gate |
|---|---|---|---|
| **System Uptime / Availability** | What % of the time the app is working | `≥ 99.5%` | 🔒 |
| **API Error Rate** | What % of requests crash or fail | `< 1%` | 🔒 |
| **Max Concurrent Users (Supported)** | How many people can use it at once | <!-- fill: e.g. 500 --> | 🔒 |
| **Throughput (Requests per Second)** | How many requests per second we handle | <!-- fill: e.g. 200 rps --> | 🔒 |
| **Max Response Degradation Under Load** | How much slower we get at peak vs normal | `< 20% slower` | ⚠️ |
| **Recovery Time After Crash** | How fast the system restarts after failure | `< 60 seconds` | 🔒 |
| **Database Query P95** | Most DB queries finish in this time | `< 100ms` | ⚠️ |

### 4.3 AI Model Quality Targets

| Metric | Beginner Explanation | Target | Gate |
|---|---|---|---|
| **Task Accuracy** | Correct, relevant AI answers out of 100 | `≥ 85%` | 🔒 |
| **Hallucination Rate** | AI saying false things confidently | `< 5%` | 🔒 |
| **Response Relevance Score** | AI answered what was actually asked | `≥ 4.0 / 5.0` | 🔒 |
| **Bias / Fairness Check** | AI treats all user groups equally | `No critical bias` | 🔒 |
| **Safety / Guardrail Pass Rate** | AI refuses harmful requests correctly | `≥ 99%` | 🔒 |
| **Prompt Injection Resistance** | AI ignores attempts to hijack it | `≥ 99%` | 🔒 |
| **Context Retention** | AI remembers earlier parts of a conversation | `≥ 90%` | ⚠️ |

### 4.4 Cost & Resource Targets

| Metric | Beginner Explanation | Target | Gate |
|---|---|---|---|
| **AI Token Cost per User/Month** | How much it costs the company per user | `< $X.XX` <!-- fill --> | ⚠️ |
| **Cloud Infrastructure Cost/Month** | Total cloud bill at expected usage | `< $X,XXX` <!-- fill --> | ⚠️ |
| **CPU Usage at Peak Load** | Server processing power at busiest time | `< 70%` | ⚠️ |
| **Memory Usage at Peak Load** | Server RAM used at busiest time | `< 80%` | ⚠️ |
| **API Call Cost per Feature** | Cloud/third-party API charges per action | <!-- fill --> | 📋 |
| **Storage Growth Rate/Month** | How fast data storage is growing | <!-- fill: e.g. < 10 GB/month --> | 📋 |

---

## 5. Stage 1 — Development & Unit Testing

> 💡 **Who fills this:** Developers, as they write code.
> **When to fill this:** Every time a significant feature or change is completed, before submitting code for review.
> **Goal:** Catch performance problems early — it is 10× cheaper to fix them here than later.

---

### 5.1 Stage 1 Context

| Field | Details |
|---|---|
| **Stage Name** | Development / Unit Testing |
| **Environment** | Local machine / Developer workstation |
| **Testing Done By** | <!-- Developer's name --> |
| **Date of Test Run** | <!-- YYYY-MM-DD --> |
| **Code Branch / PR Link** | <!-- e.g. feature/ai-chat-v2 → https://github.com/... --> |
| **Test Tool(s) Used** | <!-- e.g. k6 local, Jest, Pytest, manual curl --> |
| **AI Model Version Tested** | <!-- e.g. GPT-4o-2024-08-06, Claude 3.5 Sonnet --> |
| **Dataset / Test Prompts Used** | <!-- e.g. "internal_test_prompts_v3.json" --> |

---

### 5.2 Stage 1 — Speed & Latency Results

> Run at least **100 requests** per endpoint. Record the median (P50), P95, and P99 values.

| Endpoint / Feature | Target P50 | Actual P50 | Target P95 | Actual P95 | Target P99 | Actual P99 | Status |
|---|---|---|---|---|---|---|---|
| `POST /api/chat` | < 300ms | <!-- auto --> | < 800ms | <!-- auto --> | < 2,000ms | <!-- auto --> | ⬜ |
| `GET /api/results` | < 300ms | <!-- auto --> | < 800ms | <!-- auto --> | < 2,000ms | <!-- auto --> | ⬜ |
| `POST /api/[your endpoint]` | <!-- fill --> | <!-- auto --> | <!-- fill --> | <!-- auto --> | <!-- fill --> | <!-- auto --> | ⬜ |
| **AI TTFT** | < 500ms | <!-- auto --> | — | — | — | — | ⬜ |
| **AI Full Response** | — | <!-- auto --> | < 10s | <!-- auto --> | — | — | ⬜ |

> **How to mark Status:** ✅ PASS — all targets met | ❌ FAIL — one or more targets missed | ⏭️ SKIP — endpoint not yet built

---

### 5.3 Stage 1 — AI Quality Spot-Check

> Run a minimum of **50 test prompts** from your test dataset. Record the counts.

| AI Quality Check | Test Sample Size | Passed | Failed | Pass Rate | Target | Status |
|---|---|---|---|---|---|---|
| **Accuracy** (correct answer) | <!-- fill: e.g. 50 --> | <!-- auto --> | <!-- auto --> | <!-- auto --> | ≥ 85% | ⬜ |
| **Hallucination Check** | <!-- fill: e.g. 50 --> | <!-- auto --> | <!-- auto --> | <!-- auto --> | < 5% fail rate | ⬜ |
| **Relevance** (answered what was asked) | <!-- fill: e.g. 50 --> | <!-- auto --> | <!-- auto --> | <!-- auto --> | ≥ 80% | ⬜ |
| **Safety Guardrails** | <!-- fill: e.g. 20 --> | <!-- auto --> | <!-- auto --> | <!-- auto --> | ≥ 99% | ⬜ |

---

### 5.4 Stage 1 — Resource Usage (Local Machine)

| Resource | Idle | At Load | Target (At Load) | Status |
|---|---|---|---|---|
| **CPU Usage** | <!-- auto --> | <!-- auto --> | < 70% | ⬜ |
| **RAM / Memory** | <!-- auto --> | <!-- auto --> | < 80% | ⬜ |
| **Token Count per Request (avg)** | — | <!-- fill --> | <!-- fill --> | ⬜ |
| **Estimated Token Cost per 1,000 Requests** | — | <!-- fill: $ --> | <!-- fill: $ --> | ⬜ |

---

### 5.5 Stage 1 — Issues Found & Actions

> List every ❌ FAIL here. **No empty table = no release to next stage.**

| # | Failing Metric | Actual Value | Target | Root Cause | Fix Assigned To | Fix Due Date | Fixed? |
|---|---|---|---|---|---|---|---|
| 1 | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- YYYY-MM-DD --> | ⬜ |
| 2 | | | | | | | ⬜ |

---

### 5.6 Stage 1 — Sign-Off

| Reviewer | Role | Decision | Date | Signature / Initials |
|---|---|---|---|---|
| <!-- fill --> | Developer | ✅ Approved to merge / ❌ Blocked | <!-- YYYY-MM-DD --> | <!-- fill --> |

---

## 6. Stage 2 — Staging & Pre-Launch QA

> 💡 **Who fills this:** Developer + QA Lead (if separate).
> **When to fill this:** After all features are merged into the `staging` or `pre-production` branch — BEFORE going live.
> **Goal:** Prove the full system works correctly under realistic conditions.

---

### 6.1 Stage 2 Context

| Field | Details |
|---|---|
| **Stage Name** | Staging / Pre-Launch QA |
| **Environment** | Staging / Pre-Production server (NOT production) |
| **Testing Done By** | <!-- Name(s) --> |
| **Date of Test Run** | <!-- YYYY-MM-DD --> |
| **Build / Release Tag** | <!-- e.g. v1.0.0-rc1 --> |
| **Staging URL** | <!-- https://staging.yourapp.com --> |
| **Test Tool(s) Used** | <!-- e.g. k6, Locust, Postman, LangSmith --> |
| **Test Data Used** | <!-- e.g. "anonymised_production_sample_500.json" --> |
| **Simulated Concurrent Users** | <!-- e.g. 100 --> |
| **Test Duration** | <!-- e.g. 30 minutes --> |

---

### 6.2 Stage 2 — Full Load Test Results

> Run a **sustained load test** for at least 30 minutes at your expected peak traffic.

#### 6.2.1 Response Time Under Load 🔒 [HARD GATE]

| Endpoint | Target P50 | Actual P50 | Target P95 | Actual P95 | Target P99 | Actual P99 | Status |
|---|---|---|---|---|---|---|---|
| `POST /api/chat` | < 300ms | <!-- auto --> | < 800ms | <!-- auto --> | < 2,000ms | <!-- auto --> | ⬜ |
| `GET /api/results` | < 300ms | <!-- auto --> | < 800ms | <!-- auto --> | < 2,000ms | <!-- auto --> | ⬜ |
| `POST /api/[fill]` | <!-- fill --> | <!-- auto --> | <!-- fill --> | <!-- auto --> | <!-- fill --> | <!-- auto --> | ⬜ |
| **AI TTFT at peak** | < 500ms | <!-- auto --> | — | — | — | — | ⬜ |

#### 6.2.2 System Reliability 🔒 [HARD GATE]

| Metric | Target | Actual | Status |
|---|---|---|---|
| **Overall Error Rate** | < 1% | <!-- auto --> | ⬜ |
| **System Uptime During Test** | ≥ 99.5% | <!-- auto --> | ⬜ |
| **Peak Concurrent Users Handled** | ≥ <!-- fill: your target --> | <!-- auto --> | ⬜ |
| **Throughput (Requests/Second)** | ≥ <!-- fill: your target --> rps | <!-- auto --> | ⬜ |
| **Zero data loss during test** | 100% | <!-- auto --> | ⬜ |
| **Recovery time after simulated crash** | < 60 seconds | <!-- auto --> | ⬜ |

---

### 6.3 Stage 2 — Web Performance (Core Web Vitals) 🔒 [HARD GATE]

> Measure using Google Lighthouse, PageSpeed Insights, or WebPageTest.
> Test from at least 3 geographic regions. Record the average.

| Web Vital | What It Measures | Target | Actual (Desktop) | Actual (Mobile) | Status |
|---|---|---|---|---|---|
| **LCP** (Largest Contentful Paint) | When main content appears | < 2.5s | <!-- auto --> | <!-- auto --> | ⬜ |
| **INP** (Interaction to Next Paint) | How fast clicks respond | < 200ms | <!-- auto --> | <!-- auto --> | ⬜ |
| **CLS** (Cumulative Layout Shift) | Page stability / no jumping | < 0.10 | <!-- auto --> | <!-- auto --> | ⬜ |
| **TTFB** (Time to First Byte) | Server responds to request | < 800ms | <!-- auto --> | <!-- auto --> | ⬜ |
| **Total Page Weight** | How big the page is to download | < 3 MB | <!-- auto --> | <!-- auto --> | ⬜ |
| **Lighthouse Performance Score** | Overall score (0–100) | ≥ 80 | <!-- auto --> | <!-- auto --> | ⬜ |

> **Tool Instructions (Beginner):**
> 1. Open Chrome → press F12 → click "Lighthouse" tab → click "Analyse page load"
> 2. Or go to https://pagespeed.web.dev and enter your staging URL
> 3. Copy the numbers into the table above

---

### 6.4 Stage 2 — Full AI Quality Benchmark 🔒 [HARD GATE]

> Use at least **200 test prompts** covering all major features. See Section 9 for full details.

| AI Quality Metric | Sample Size | Target | Actual | Status |
|---|---|---|---|---|
| **Task Accuracy** | ≥ 200 | ≥ 85% | <!-- fill --> | ⬜ |
| **Hallucination Rate** | ≥ 200 | < 5% | <!-- fill --> | ⬜ |
| **Response Relevance (avg score)** | ≥ 200 | ≥ 4.0 / 5.0 | <!-- fill --> | ⬜ |
| **Safety / Guardrail Pass Rate** | ≥ 50 adversarial | ≥ 99% | <!-- fill --> | ⬜ |
| **Bias Check — Gender** | ≥ 50 paired | No critical bias | <!-- fill --> | ⬜ |
| **Bias Check — Race / Ethnicity** | ≥ 50 paired | No critical bias | <!-- fill --> | ⬜ |
| **Prompt Injection Resistance** | ≥ 30 attacks | ≥ 99% | <!-- fill --> | ⬜ |
| **Context Retention (multi-turn)** | ≥ 50 conversations | ≥ 90% | <!-- fill --> | ⬜ |

---

### 6.5 Stage 2 — Infrastructure Cost Projection

| Cost Metric | Unit | Projected Monthly Cost | Acceptable Limit | Status |
|---|---|---|---|---|
| **AI API Token Cost** | Per 1,000 tokens | $<!-- fill --> | $<!-- fill --> | ⬜ |
| **Cloud Compute (EC2/Cloud Run/etc.)** | Per month | $<!-- fill --> | $<!-- fill --> | ⬜ |
| **Database Cost** | Per month | $<!-- fill --> | $<!-- fill --> | ⬜ |
| **CDN / Bandwidth Cost** | Per month | $<!-- fill --> | $<!-- fill --> | ⬜ |
| **Total Estimated Infrastructure Cost** | Per month | **$<!-- fill -->** | **$<!-- fill -->** | ⬜ |
| **Cost per Active User (estimated)** | Per user/month | $<!-- fill --> | $<!-- fill --> | ⬜ |

---

### 6.6 Stage 2 — Security & Compliance Quick Check

> These are not full security tests — those go in a separate Security document. This is a performance-adjacent safety check.

| Check | Required | Status | Notes |
|---|---|---|---|
| Rate limiting enabled on all AI endpoints | ✅ Required | ⬜ | <!-- fill --> |
| Authentication verified on load test | ✅ Required | ⬜ | <!-- fill --> |
| No PII exposed in error messages or logs | ✅ Required | ⬜ | <!-- fill --> |
| HTTPS enforced (no HTTP fallback) | ✅ Required | ⬜ | <!-- fill --> |
| AI output filtered for PII before returning to user | ✅ Required | ⬜ | <!-- fill --> |

---

### 6.7 Stage 2 — Issues Found & Actions

| # | Failing Metric | Actual | Target | Root Cause | Assigned To | Fix Due | Fixed? |
|---|---|---|---|---|---|---|---|
| 1 | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- YYYY-MM-DD --> | ⬜ |
| 2 | | | | | | | ⬜ |

---

### 6.8 Stage 2 — Sign-Off (Required Before Launch)

> 🔒 All three approvals are required before proceeding to Beta.

| Reviewer | Role | Decision | Date | Signature / Initials |
|---|---|---|---|---|
| <!-- fill --> | Engineering Lead | ✅ Approved / ❌ Blocked | <!-- YYYY-MM-DD --> | <!-- fill --> |
| <!-- fill --> | Product Manager | ✅ Approved / ❌ Blocked | <!-- YYYY-MM-DD --> | <!-- fill --> |
| <!-- fill --> | QA Lead | ✅ Approved / ❌ Blocked | <!-- YYYY-MM-DD --> | <!-- fill --> |

---

## 7. Stage 3 — Beta (1–50 Users)

> 💡 **Who fills this:** Engineering Lead + Developer monitoring production.
> **When to fill this:** During the beta period, updated weekly.
> **Goal:** Confirm that real-world usage matches what we saw in staging. Real users behave differently from test scripts.

---

### 7.1 Stage 3 Context

| Field | Details |
|---|---|
| **Stage Name** | Beta — Real Users (1–50) |
| **Environment** | Production (limited access / invite only) |
| **Monitoring Done By** | <!-- Name(s) --> |
| **Beta Start Date** | <!-- YYYY-MM-DD --> |
| **Reporting Period** | <!-- e.g. Week 1: Oct 14 – Oct 21, 2026 --> |
| **Total Beta Users So Far** | <!-- e.g. 23 --> |
| **Monitoring Tools** | <!-- e.g. Datadog, Helicone, custom logging --> |
| **Total Requests Recorded** | <!-- e.g. 4,821 --> |

---

### 7.2 Stage 3 — Real-World Latency (Production Data)

| Endpoint | Target P50 | Actual P50 | Target P95 | Actual P95 | Target P99 | Actual P99 | Status |
|---|---|---|---|---|---|---|---|
| `POST /api/chat` | < 300ms | <!-- auto --> | < 800ms | <!-- auto --> | < 2,000ms | <!-- auto --> | ⬜ |
| `GET /api/results` | < 300ms | <!-- auto --> | < 800ms | <!-- auto --> | < 2,000ms | <!-- auto --> | ⬜ |
| `POST /api/[fill]` | <!-- fill --> | <!-- auto --> | <!-- fill --> | <!-- auto --> | <!-- fill --> | <!-- auto --> | ⬜ |
| **AI TTFT (real users)** | < 500ms | <!-- auto --> | — | — | — | — | ⬜ |

---

### 7.3 Stage 3 — Real-World Reliability

| Metric | Target | This Week Actual | Cumulative Actual | Status |
|---|---|---|---|---|
| **Uptime** | ≥ 99.5% | <!-- auto --> | <!-- auto --> | ⬜ |
| **Error Rate** | < 1% | <!-- auto --> | <!-- auto --> | ⬜ |
| **Incidents (P1 — service down)** | 0 | <!-- fill --> | <!-- fill --> | ⬜ |
| **Incidents (P2 — degraded service)** | ≤ 1/week | <!-- fill --> | <!-- fill --> | ⬜ |
| **User-Reported Bugs (performance)** | <!-- fill --> | <!-- fill --> | <!-- fill --> | ⬜ |

---

### 7.4 Stage 3 — Beta User Experience Signals

> Collect this from user interviews, feedback forms, or in-app ratings.

| Signal | How to Collect | Target | Actual | Status |
|---|---|---|---|---|
| **"The app feels fast"** (user rating) | In-app 5-star rating or survey | ≥ 4.0 / 5.0 | <!-- fill --> | ⬜ |
| **"The AI answers were helpful"** | In-app thumbs up/down | ≥ 75% thumbs up | <!-- fill --> | ⬜ |
| **Session length (avg)** | Analytics (Mixpanel, PostHog, etc.) | ≥ <!-- fill: e.g. 5 min --> | <!-- fill --> | ⬜ |
| **Return visit rate** | Analytics | ≥ <!-- fill: e.g. 40% --> | <!-- fill --> | ⬜ |
| **Support tickets about slowness** | Help desk / Intercom | ≤ 2 per week | <!-- fill --> | ⬜ |

---

### 7.5 Stage 3 — Cost Actuals vs Projection

| Cost Metric | Projected (from Stage 2) | Actual (This Period) | On Track? | Action Needed |
|---|---|---|---|---|
| **AI Token Cost** | $<!-- fill --> | $<!-- fill --> | ⬜ Yes / ❌ No | <!-- fill or "None" --> |
| **Cloud Compute** | $<!-- fill --> | $<!-- fill --> | ⬜ Yes / ❌ No | <!-- fill or "None" --> |
| **Total Cost** | $<!-- fill --> | $<!-- fill --> | ⬜ Yes / ❌ No | <!-- fill or "None" --> |
| **Cost per Active User** | $<!-- fill --> | $<!-- fill --> | ⬜ Yes / ❌ No | <!-- fill or "None" --> |

---

### 7.6 Stage 3 — Issues & Observations

| # | Issue | Impact | Severity | Assigned To | Fix Due | Fixed? |
|---|---|---|---|---|---|---|
| 1 | <!-- fill --> | <!-- High / Medium / Low --> | <!-- P1 / P2 / P3 --> | <!-- fill --> | <!-- YYYY-MM-DD --> | ⬜ |
| 2 | | | | | | ⬜ |

---

### 7.7 Stage 3 — Weekly Sign-Off

| Reviewer | Role | Sign-Off | Date |
|---|---|---|---|
| <!-- fill --> | Engineering Lead | ✅ Continue Beta / ⚠️ Pause / ❌ Rollback | <!-- YYYY-MM-DD --> |

---

## 8. Stage 4 — Growth Phase (51–500 Customers)

> 💡 **Who fills this:** Engineering Lead + Product Manager, reviewed monthly.
> **When to fill this:** Monthly, as the customer base grows.
> **Goal:** Confirm the system scales gracefully. Catch cost overruns early. Maintain quality as volume grows.

---

### 8.1 Stage 4 Context

| Field | Details |
|---|---|
| **Stage Name** | Growth Phase (51–500 Customers) |
| **Environment** | Production |
| **Report Period** | <!-- e.g. "Month 2: November 2026" --> |
| **Total Customers at End of Period** | <!-- e.g. 127 --> |
| **Total Requests This Period** | <!-- e.g. 1,240,000 --> |
| **Peak Concurrent Users Observed** | <!-- e.g. 89 --> |
| **Prepared By** | <!-- Name --> |

---

### 8.2 Stage 4 — Scalability Milestone Targets

> Fill in the "Actual" column each month. If a target is missed, trigger the Failure Response Protocol (Section 14).

| Milestone | Customer Count | Target P95 Latency | Actual P95 | Target Error Rate | Actual Error Rate | Target Uptime | Actual Uptime | Status |
|---|---|---|---|---|---|---|---|---|
| **Early Growth** | 51–100 | < 900ms | <!-- fill --> | < 1% | <!-- fill --> | ≥ 99.5% | <!-- fill --> | ⬜ |
| **Mid Growth** | 101–250 | < 1,000ms | <!-- fill --> | < 1% | <!-- fill --> | ≥ 99.5% | <!-- fill --> | ⬜ |
| **Late Growth** | 251–500 | < 1,200ms | <!-- fill --> | < 1.5% | <!-- fill --> | ≥ 99.5% | <!-- fill --> | ⬜ |

> ⚠️ **Note:** Slight latency increase is acceptable at higher scale IF total system health is maintained. Do not accept latency increases above 50% from Stage 2 baseline without a capacity review.

---

### 8.3 Stage 4 — Throughput & Capacity

| Metric | Month 2 | Month 3 | Month 4 | Month 5 | Month 6 | Target at 500 Users |
|---|---|---|---|---|---|---|
| **Peak Requests/Second** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| **Avg Concurrent Users** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| **Peak Concurrent Users** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| **Total Requests/Month** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |

---

### 8.4 Stage 4 — Cost Scaling Actuals

| Cost Metric | Target per 100 Users | Month 2 | Month 3 | Month 4 | Month 5 | Month 6 | On Track? |
|---|---|---|---|---|---|---|---|
| **AI Token Cost** | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ |
| **Cloud Compute** | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ |
| **Storage** | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ |
| **Total Infra Cost** | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ |
| **Cost per Active User** | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ |

> 🚨 **Alert Trigger:** If `Cost per Active User` grows more than 30% month-over-month without a matching revenue increase, escalate immediately to the CTO.

---

### 8.5 Stage 4 — AI Quality at Scale

> Re-run a sample of 500+ live requests through your AI quality evaluation monthly.

| AI Quality Metric | Month 2 | Month 3 | Month 4 | Month 5 | Month 6 | Target |
|---|---|---|---|---|---|---|
| **Accuracy** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ≥ 85% |
| **Hallucination Rate** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | < 5% |
| **Relevance Score** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ≥ 4.0 |
| **Safety Pass Rate** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ≥ 99% |
| **User Thumbs-Up Rate** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ≥ 75% |

---

### 8.6 Stage 4 — Monthly Sign-Off

| Month | Engineering Lead | Product Manager | Decision | Signed Date |
|---|---|---|---|---|
| Month 2 | <!-- fill --> | <!-- fill --> | ✅ Healthy / ⚠️ Watch / ❌ Action Required | <!-- YYYY-MM-DD --> |
| Month 3 | <!-- fill --> | <!-- fill --> | ✅ Healthy / ⚠️ Watch / ❌ Action Required | <!-- YYYY-MM-DD --> |
| Month 4 | <!-- fill --> | <!-- fill --> | ✅ Healthy / ⚠️ Watch / ❌ Action Required | <!-- YYYY-MM-DD --> |
| Month 5 | <!-- fill --> | <!-- fill --> | ✅ Healthy / ⚠️ Watch / ❌ Action Required | <!-- YYYY-MM-DD --> |
| Month 6 | <!-- fill --> | <!-- fill --> | ✅ Healthy / ⚠️ Watch / ❌ Action Required | <!-- YYYY-MM-DD --> |

---

## 9. AI Model Quality Benchmarks

> 💡 **This section is the full detail behind the AI quality rows in Sections 5–8.** Think of it as the "AI Report Card." Fill this once per major release and update it monthly during growth.
>
> **Two modes available:**
> - **Quick Check (9.0)** — 4 metrics, fits in 5 minutes. Use during Development (Stage 1).
> - **Full Evaluation (9.1–9.7)** — Complete report. Use at Staging and every month during Growth.

---

### 9.0 AI Quality — Quick Check (Lightweight Version)

> ⚡ **Use this in Stage 1 (Development) or any time you need a fast gut-check.**
> Run at least **30 test prompts**. Mark each row and move on. Full detail is in 9.1–9.7.

| Metric | Plain-English Question | Sample Size | Result | Target | Status |
|---|---|---|---|---|---|
| **Accuracy** | Did the AI give the right answer? | ≥ 30 | <!-- fill: e.g. "27/30 = 90%" --> | ≥ 85% | ⬜ |
| **Hallucination** | Did the AI make anything up? | ≥ 30 | <!-- fill: e.g. "1/30 = 3%" --> | < 5% | ⬜ |
| **Safety** | Did the AI refuse harmful prompts? | ≥ 10 | <!-- fill: e.g. "10/10 = 100%" --> | ≥ 99% | ⬜ |
| **Relevance** | Did the AI answer what was actually asked? | ≥ 30 | <!-- fill: e.g. "4.2 / 5.0 avg" --> | ≥ 4.0 / 5.0 | ⬜ |

> ✅ If all 4 are green → proceed to next step.
> ❌ If any are red → investigate before moving forward. Escalate to Full Evaluation (9.1–9.7).

---

### 9.1 AI Quality — Test Dataset Details

| Field | Details |
|---|---|
| **Dataset Name / Version** | <!-- e.g. "eval_dataset_v3_oct2026.json" --> |
| **Total Prompts in Dataset** | <!-- e.g. 500 --> |
| **Dataset Created By** | <!-- Name --> |
| **Last Updated** | <!-- YYYY-MM-DD --> |
| **Coverage** | <!-- e.g. "Covers 12 use cases: scheduling, Q&A, summarisation, data extraction..." --> |
| **Adversarial / Edge Case %** | <!-- e.g. "10% are adversarial prompts testing safety" --> |
| **Storage Location** | <!-- e.g. "s3://your-bucket/eval-datasets/v3/" --> |
| **Evaluation Method** | <!-- e.g. "GPT-4o as judge + 2 human reviewers" --> |

---

### 9.2 AI Accuracy — Detailed Breakdown

> Break down accuracy by feature category so you know which areas need improvement.

| Feature / Use Case | Test Prompts | Correct | Incorrect | Accuracy | Target | Status |
|---|---|---|---|---|---|---|
| <!-- e.g. "Summarisation" --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 85% | ⬜ |
| <!-- e.g. "Question Answering" --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 85% | ⬜ |
| <!-- e.g. "Data Extraction" --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 85% | ⬜ |
| <!-- e.g. "Code Generation" --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 85% | ⬜ |
| <!-- e.g. "Recommendations" --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 85% | ⬜ |
| **TOTAL / AVERAGE** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 85% | ⬜ |

---

### 9.3 Hallucination Tracking

> 💡 **What is a hallucination?** When the AI confidently states something that is false or made-up.
> **How to detect:** Have a human reviewer (or a second AI judge) mark each response as True/False/Hallucination.

| Hallucination Type | Count Found | Out of Total | Rate | Acceptable Rate | Status |
|---|---|---|---|---|---|
| **Factual errors** (wrong facts) | <!-- fill --> | <!-- fill --> | <!-- auto --> | < 3% | ⬜ |
| **Made-up references** (fake URLs, names) | <!-- fill --> | <!-- fill --> | <!-- auto --> | < 1% | ⬜ |
| **Contradictions within one response** | <!-- fill --> | <!-- fill --> | <!-- auto --> | < 2% | ⬜ |
| **Out-of-scope confident claims** | <!-- fill --> | <!-- fill --> | <!-- auto --> | < 2% | ⬜ |
| **TOTAL HALLUCINATION RATE** | <!-- fill --> | <!-- fill --> | <!-- auto --> | < 5% | ⬜ |

---

### 9.4 Relevance & Quality Scoring

> Use a 1–5 scale. Have at least 2 human reviewers score a sample of 100 responses.
> Scale: 1 = Completely off-topic | 3 = Partially relevant | 5 = Perfectly on-target

| Reviewer | Sample Size | Avg Relevance Score | Avg Completeness Score | Avg Tone Score | Overall Avg |
|---|---|---|---|---|---|
| <!-- Name --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- Name --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| **Consensus Average** | | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| **Target** | | ≥ 4.0 | ≥ 3.5 | ≥ 4.0 | **≥ 4.0** |
| **Status** | | ⬜ | ⬜ | ⬜ | ⬜ |

---

### 9.5 Safety & Guardrail Testing

> 🔒 [HARD GATE] — ALL safety checks must pass before any launch.

| Safety Test Category | Prompts Tested | Correctly Blocked | Leaked Through | Pass Rate | Target | Status |
|---|---|---|---|---|---|---|
| **Harmful content generation** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 99% | ⬜ |
| **PII / personal data exposure** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 99% | ⬜ |
| **Prompt injection attacks** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 99% | ⬜ |
| **Jailbreak attempts** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 99% | ⬜ |
| **System prompt extraction** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- auto --> | ≥ 99% | ⬜ |

---

### 9.6 Bias & Fairness Check

> 💡 **Why this matters:** If the AI answers differently depending on the gender, name, or background described in the prompt, that is a bias problem. Use paired prompts — same question, only the demographic detail changes.

| Bias Dimension | Paired Prompts | Bias Detected? | Severity | Notes | Status |
|---|---|---|---|---|---|
| **Gender** | <!-- e.g. 50 pairs --> | ✅ No / ❌ Yes | <!-- None / Low / Medium / Critical --> | <!-- fill --> | ⬜ |
| **Race / Ethnicity** | <!-- e.g. 50 pairs --> | ✅ No / ❌ Yes | <!-- None / Low / Medium / Critical --> | <!-- fill --> | ⬜ |
| **Age** | <!-- e.g. 30 pairs --> | ✅ No / ❌ Yes | <!-- None / Low / Medium / Critical --> | <!-- fill --> | ⬜ |
| **Socioeconomic language** | <!-- e.g. 30 pairs --> | ✅ No / ❌ Yes | <!-- None / Low / Medium / Critical --> | <!-- fill --> | ⬜ |
| **Geography / Culture** | <!-- e.g. 30 pairs --> | ✅ No / ❌ Yes | <!-- None / Low / Medium / Critical --> | <!-- fill --> | ⬜ |

> **Rule:** Any bias rated `Critical` is a 🔒 HARD GATE failure. `Medium` requires a documented mitigation plan before launch.

---

### 9.7 Model Version & Prompt Change Log

> Every time you change the AI model version or update a system prompt, log it here. This helps you trace quality changes over time.

| Date | Change Type | Description | Accuracy Before | Accuracy After | Changed By |
|---|---|---|---|---|---|
| <!-- YYYY-MM-DD --> | <!-- Model / Prompt / Config --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- YYYY-MM-DD --> | | | | | |

---

## 10. Mobile App Performance Benchmarks

> 💡 **Skip this section if your product is web-only.** For mobile apps, this section tracks the metrics that matter most on phones and tablets.

---

### 10.1 Mobile Test Devices

> Test on at least one low-end and one high-end device per platform.

| Device | OS Version | Category | Used for Testing? |
|---|---|---|---|
| <!-- e.g. iPhone 15 Pro --> | <!-- iOS 18 --> | High-end | ⬜ Yes / ❌ No |
| <!-- e.g. iPhone 12 --> | <!-- iOS 17 --> | Mid-range | ⬜ Yes / ❌ No |
| <!-- e.g. Samsung Galaxy A14 --> | <!-- Android 14 --> | Low-end | ⬜ Yes / ❌ No |
| <!-- e.g. Samsung Galaxy S24 --> | <!-- Android 14 --> | High-end | ⬜ Yes / ❌ No |

---

### 10.2 Mobile App Launch & Rendering

| Metric | Platform | Target | Actual (Low-end) | Actual (High-end) | Status |
|---|---|---|---|---|---|
| **Cold Start Time** | iOS | < 3s | <!-- fill --> | <!-- fill --> | ⬜ |
| **Cold Start Time** | Android | < 3s | <!-- fill --> | <!-- fill --> | ⬜ |
| **Warm Start Time** | iOS | < 1s | <!-- fill --> | <!-- fill --> | ⬜ |
| **Warm Start Time** | Android | < 1s | <!-- fill --> | <!-- fill --> | ⬜ |
| **Time to Interactive** | iOS | < 4s | <!-- fill --> | <!-- fill --> | ⬜ |
| **Time to Interactive** | Android | < 4s | <!-- fill --> | <!-- fill --> | ⬜ |
| **Screen Render Time** | iOS | < 16ms/frame (60fps) | <!-- fill --> | <!-- fill --> | ⬜ |
| **Screen Render Time** | Android | < 16ms/frame (60fps) | <!-- fill --> | <!-- fill --> | ⬜ |

---

### 10.3 Mobile App Resource Usage

| Metric | Platform | Target | Actual (Idle) | Actual (Active) | Status |
|---|---|---|---|---|---|
| **CPU Usage (Active)** | iOS | < 30% sustained | <!-- fill --> | <!-- fill --> | ⬜ |
| **CPU Usage (Active)** | Android | < 30% sustained | <!-- fill --> | <!-- fill --> | ⬜ |
| **RAM / Memory** | iOS | < 200 MB | <!-- fill --> | <!-- fill --> | ⬜ |
| **RAM / Memory** | Android | < 200 MB | <!-- fill --> | <!-- fill --> | ⬜ |
| **Battery Drain (per 30 min use)** | iOS | < 5% drain | <!-- fill --> | <!-- fill --> | ⬜ |
| **Battery Drain (per 30 min use)** | Android | < 5% drain | <!-- fill --> | <!-- fill --> | ⬜ |
| **Network Data Usage (per session)** | Both | < 5 MB | <!-- fill --> | <!-- fill --> | ⬜ |

---

### 10.4 Mobile — Offline & Network Degradation

| Scenario | Expected Behaviour | Actual Behaviour | Status |
|---|---|---|---|
| No internet connection | Show clear error message, no crash | <!-- fill --> | ⬜ |
| Slow 3G connection (< 1 Mbps) | App loads within 6 seconds | <!-- fill --> | ⬜ |
| Network drops mid-session | Session recovers gracefully | <!-- fill --> | ⬜ |
| Background → Foreground (5 min gap) | State is preserved, no re-login | <!-- fill --> | ⬜ |

---

## 11. Cost & Resource Usage Benchmarks

> 💡 **Think of this section as your "electricity bill tracker" for the product.** It tracks how much money it costs to run the AI every month and whether that cost stays under control as more users join.

---

### 11.1 AI Model Token Cost Analysis

| AI Feature / Endpoint | Avg Input Tokens | Avg Output Tokens | Cost per 1K Tokens | Avg Cost per Call | Calls/Day (Expected) | Daily Cost | Monthly Cost |
|---|---|---|---|---|---|---|---|
| <!-- e.g. "Chat message" --> | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> |
| <!-- e.g. "Document summary" --> | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> |
| <!-- e.g. "Recommendation" --> | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> |
| **TOTAL** | | | | | | **$<!-- fill -->** | **$<!-- fill -->** |

---

### 11.2 Token Optimisation Strategies

> Check which optimisations you have implemented. Every ✅ checked item saves money.

| Optimisation | Status | Est. Saving |
|---|---|---|
| Prompt compression (removing redundant context) | ✅ Done / ⬜ Planned / ❌ Not applicable | <!-- fill: e.g. "~15% token reduction" --> |
| Caching repeated AI calls (same input → same output) | ✅ Done / ⬜ Planned / ❌ Not applicable | <!-- fill --> |
| Truncating conversation history to last N turns | ✅ Done / ⬜ Planned / ❌ Not applicable | <!-- fill --> |
| Using smaller model for simple tasks | ✅ Done / ⬜ Planned / ❌ Not applicable | <!-- fill --> |
| Streaming responses (avoids timeout costs) | ✅ Done / ⬜ Planned / ❌ Not applicable | <!-- fill --> |
| Rate limiting per user to prevent abuse | ✅ Done / ⬜ Planned / ❌ Not applicable | <!-- fill --> |

---

### 11.3 Infrastructure Cost Breakdown

| Resource | Provider | Tier / Instance | Monthly Cost (Current) | Monthly Cost (at 500 Users) | Status |
|---|---|---|---|---|---|
| **Application Server(s)** | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ On track |
| **Database** | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ On track |
| **AI API (OpenAI / Anthropic / etc.)** | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ On track |
| **CDN / Bandwidth** | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ On track |
| **Storage (S3 / GCS / etc.)** | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ On track |
| **Monitoring / Logging tools** | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ On track |
| **Other** | <!-- fill --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | ⬜ On track |
| **TOTAL** | | | **$<!-- fill -->** | **$<!-- fill -->** | ⬜ |

---

### 11.4 Unit Economics (Per User)

| Metric | Formula | Current Value | Target Value | Status |
|---|---|---|---|---|
| **Monthly Infrastructure Cost / Active Users** | Total Infra ÷ Active Users | $<!-- fill --> | < $<!-- fill --> | ⬜ |
| **AI Token Cost / Active Users** | Total Token Cost ÷ Active Users | $<!-- fill --> | < $<!-- fill --> | ⬜ |
| **Total COGS per User** | All costs ÷ Active Users | $<!-- fill --> | < $<!-- fill --> | ⬜ |
| **Gross Margin** | (Revenue − COGS) ÷ Revenue | <!-- fill: e.g. "65%" --> | > <!-- fill: e.g. "60%" --> | ⬜ |

---

## 12. CI/CD Integration & Automation

> 💡 **This section explains how to make performance tests run automatically** every time someone pushes new code, so you never accidentally make the product slower.

---

### 12.1 Automated Test Pipeline Overview

```
Developer pushes code
        │
        ▼
  ┌─────────────┐     FAIL → ❌ PR blocked
  │  Unit Tests  │──────────────────────────▶ Notify developer
  │  (Stage 1)  │
  └──────┬──────┘
         │ PASS
         ▼
  ┌────────────────────┐     FAIL → ❌ Merge blocked
  │  Perf Benchmark    │──────────────────────────────▶ Alert team
  │  (k6 / Locust)     │
  └────────┬───────────┘
           │ PASS
           ▼
  ┌─────────────────┐     FAIL → ❌ Deploy to staging blocked
  │  AI Quality     │──────────────────────────────────────▶ Alert team
  │  Eval Suite     │
  └────────┬────────┘
           │ PASS
           ▼
  ✅ Auto-deploy to Staging
```

---

### 12.2 CI/CD Configuration Checklist

| Task | Tool / Command | Status | Notes |
|---|---|---|---|
| Load test runs on every PR | <!-- e.g. "k6 run scripts/load_test.js" --> | ⬜ Done | <!-- fill --> |
| P95 latency gate is set | <!-- e.g. threshold in k6: "p(95)<800" --> | ⬜ Done | <!-- fill --> |
| Error rate gate is set | <!-- e.g. "rate<0.01" --> | ⬜ Done | <!-- fill --> |
| AI quality eval runs on merge to main | <!-- e.g. "python run_evals.py" --> | ⬜ Done | <!-- fill --> |
| Performance badge in README | <!-- link to badge --> | ⬜ Done | <!-- fill --> |
| Slack / email alert on failure | <!-- fill --> | ⬜ Done | <!-- fill --> |
| Cost alert threshold set | <!-- e.g. AWS Budget Alert at $500 --> | ⬜ Done | <!-- fill --> |

---

### 12.3 Performance Health Score

> This is a single number (0–100) you can use in dashboards and READMEs to communicate system health at a glance.

**Formula:**
```
Health Score = (Speed Score × 40%) + (AI Quality Score × 35%) + (Reliability Score × 25%)

Where:
  Speed Score     = % of latency targets met (0–100)
  AI Quality Score = % of AI quality targets met (0–100)
  Reliability Score = Uptime % over the reporting period
```

| Component | Weight | This Period Score | Weighted Score |
|---|---|---|---|
| Speed / Latency | 40% | <!-- fill: 0–100 --> | <!-- auto --> |
| AI Quality | 35% | <!-- fill: 0–100 --> | <!-- auto --> |
| Reliability | 25% | <!-- fill: 0–100 --> | <!-- auto --> |
| **OVERALL HEALTH SCORE** | 100% | | **<!-- auto -->/ 100** |

| Score Range | Meaning | Action |
|---|---|---|
| 90–100 | 🟢 Excellent | No action needed |
| 75–89 | 🟡 Good | Monitor closely |
| 60–74 | 🟠 Needs Attention | Investigate within 48 hours |
| Below 60 | 🔴 Critical | Stop release. Hotfix required. |

---

## 13. Trend Tracking Dashboard

> 💡 **This section tracks progress over time.** Instead of just passing or failing today, we look at whether we are getting better or worse. A product that is slowing down month over month will eventually fail, even if it is passing today.

---

### 13.1 Latency Trend (P95 — Main AI Endpoint)

> Update this table each time you run a full benchmark (at each stage and monthly during growth).

| Date | Stage | Users | P95 Latency | AI TTFT | Error Rate | Uptime | Health Score |
|---|---|---|---|---|---|---|---|
| <!-- YYYY-MM-DD --> | Dev | 1 (local) | <!-- fill --> | <!-- fill --> | <!-- fill --> | N/A | <!-- fill --> |
| <!-- YYYY-MM-DD --> | Staging | ~100 (simulated) | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- YYYY-MM-DD --> | Beta (1–50) | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- YYYY-MM-DD --> | Growth (51–100) | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- YYYY-MM-DD --> | Growth (101–250) | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- YYYY-MM-DD --> | Growth (251–500) | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |

---

### 13.2 AI Quality Trend

| Date | Stage | Accuracy | Hallucination Rate | Relevance Score | Safety Pass Rate |
|---|---|---|---|---|---|
| <!-- YYYY-MM-DD --> | Dev | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- YYYY-MM-DD --> | Staging | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- YYYY-MM-DD --> | Beta | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| <!-- YYYY-MM-DD --> | Growth | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |

---

### 13.3 Cost Trend (Monthly)

| Month | Active Users | AI Token Cost | Infra Cost | Total Cost | Cost/User | On Budget? |
|---|---|---|---|---|---|---|
| <!-- e.g. Oct 2026 --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ✅ / ❌ |
| <!-- Nov 2026 --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ✅ / ❌ |
| <!-- Dec 2026 --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ✅ / ❌ |
| <!-- Jan 2027 --> | <!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | $<!-- fill --> | ✅ / ❌ |

---

## 14. Failure Response Protocol

> 💡 **What to do when something fails.** This section is like a "fire drill" guide — you hope you never need it, but when you do, you will be very glad it exists.

---

### 14.1 Failure Severity Levels

| Level | Name | Description | Example | Response Time |
|---|---|---|---|---|
| **P1** | 🔴 Critical | Product is completely down or unsafe | App returns 500 errors for all users | Within 1 hour |
| **P2** | 🟠 High | Major feature broken or very slow | AI response taking > 30 seconds | Within 4 hours |
| **P3** | 🟡 Medium | Performance degraded but usable | P95 latency up from 800ms to 1,500ms | Within 24 hours |
| **P4** | 🔵 Low | Minor, small percentage of users affected | 1 edge case prompt giving wrong answer | Next sprint |

---

### 14.2 Failure Response Runbook

```
WHEN A BENCHMARK FAILS:

STEP 1: IDENTIFY
  ├── Which metric failed?
  ├── What is the actual value vs target?
  └── Which stage / environment?

STEP 2: CLASSIFY
  ├── Is this a P1 (service down)?   → Page on-call engineer NOW
  ├── Is this a P2 (major feature)?  → Notify team in Slack immediately
  ├── Is this a P3 (degraded)?       → Create ticket, schedule fix
  └── Is this a P4 (minor)?          → Log and add to next sprint

STEP 3: CONTAIN (if P1 or P2)
  ├── Roll back to last known good version
  ├── Enable feature flag to disable broken feature
  └── Communicate status to users if > 5 min outage

STEP 4: FIX & VERIFY
  ├── Fix the root cause (not just the symptom)
  ├── Re-run the failing benchmark
  ├── Confirm it now passes
  └── Update the Issues table in the relevant Stage section

STEP 5: DOCUMENT
  ├── Write a post-mortem (what happened, why, how to prevent)
  └── Update this document with the fix date and resolution
```

---

### 14.3 Failure Log

| # | Date | Stage | Failing Metric | Actual Value | Target | P-Level | Root Cause | Fix Applied | Re-tested & Passed | Post-Mortem Written? |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | <!-- YYYY-MM-DD --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- P1/P2/P3/P4 --> | <!-- fill --> | <!-- fill --> | ✅ / ❌ | ✅ / ❌ |
| 2 | | | | | | | | | ✅ / ❌ | ✅ / ❌ |

---

## 15. Executive Summary

> 💡 **Write this section LAST, after all tests are done.** This is the only section that a CEO, investor, or non-technical stakeholder will read. Write it in plain English as if you are explaining the product's health to a smart friend who is not a developer.
> Keep it to 1–2 short paragraphs per question.

---

### 15.1 Current Snapshot

**What is the product, and what stage is it at?**
> <!-- e.g. "BudgetBot is an AI-powered personal finance assistant available as a web and iOS app. As of October 2026, we are in the Beta stage with 23 invited users." -->

**Is the product performing well overall?**
> <!-- e.g. "Yes. The product meets all speed and reliability targets. Our Health Score is 88/100 (Good). The main area to watch is AI accuracy, which is at 87% — above our 85% target but below our aspirational goal of 92%." -->

---

### 15.2 Key Wins This Period

> List 3–5 things that are going well.

- <!-- e.g. "API response time improved by 35% after database query optimisation in Sprint 12." -->
- <!-- fill -->
- <!-- fill -->

---

### 15.3 Key Risks & Actions

> List any open risks and what is being done about them.

| Risk | Likelihood | Impact | Mitigation Plan | Owner | Due Date |
|---|---|---|---|---|---|
| <!-- e.g. "AI token costs may exceed budget at 200 users" --> | <!-- High/Med/Low --> | <!-- High/Med/Low --> | <!-- fill --> | <!-- fill --> | <!-- YYYY-MM-DD --> |
| <!-- fill --> | | | | | |

---

### 15.4 Readiness Rating

| Gate | Status | Notes |
|---|---|---|
| ✅ Safe to develop? | ✅ Yes / ❌ No | <!-- fill --> |
| ✅ Safe to deploy to staging? | ✅ Yes / ❌ No | <!-- fill --> |
| ✅ Safe to launch beta? | ✅ Yes / ❌ No | <!-- fill --> |
| ✅ Safe to open to 500 customers? | ✅ Yes / ❌ No | <!-- fill --> |

---

## 16. Sign-Off & Approvals

> 🔒 This section records the final approval for each milestone. No milestone is official until signed off here.

### 16.1 Milestone Approvals

| Milestone | Required Approvers | All Approved? | Date Approved |
|---|---|---|---|
| **Stage 1 Complete** (Dev Benchmarks Pass) | Engineering Lead | ⬜ | <!-- YYYY-MM-DD --> |
| **Stage 2 Complete** (Staging Benchmarks Pass) | Engineering Lead + PM + QA Lead | ⬜ | <!-- YYYY-MM-DD --> |
| **Beta Launch Approved** | Engineering Lead + PM | ⬜ | <!-- YYYY-MM-DD --> |
| **Public Launch Approved** | Engineering Lead + PM + (CTO if applicable) | ⬜ | <!-- YYYY-MM-DD --> |
| **500-Customer Milestone Healthy** | Engineering Lead + PM | ⬜ | <!-- YYYY-MM-DD --> |

### 16.2 Approver Details

| Name | Role | Email | Approvals Granted | Date |
|---|---|---|---|---|
| <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- Stage 1 / 2 / Beta / Launch / 500 --> | <!-- YYYY-MM-DD --> |
| <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- Stage 1 / 2 / Beta / Launch / 500 --> | <!-- YYYY-MM-DD --> |
| <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- Stage 1 / 2 / Beta / Launch / 500 --> | <!-- YYYY-MM-DD --> |

---

## 17. Third-Party SLA Tracking

> 💡 **Your product depends on other companies' services** — like OpenAI for AI, AWS for servers, or Stripe for payments. If they go down, your product goes down too. This section tracks their uptime promises so you know exactly what you are depending on and whether they are keeping their promises.

---

### 17.1 Third-Party Service Registry

| Service | Provider | What You Use It For | SLA Promised | SLA URL | Status Page URL |
|---|---|---|---|---|---|
| <!-- e.g. AI API --> | <!-- e.g. Anthropic / OpenAI --> | <!-- e.g. "Core AI responses" --> | <!-- e.g. 99.9% --> | <!-- https://... --> | <!-- https://status.openai.com --> |
| <!-- e.g. Cloud Compute --> | <!-- e.g. AWS EC2 --> | <!-- e.g. "Application servers" --> | <!-- e.g. 99.99% --> | <!-- https://... --> | <!-- https://health.aws.amazon.com --> |
| <!-- e.g. Database --> | <!-- e.g. Supabase / RDS --> | <!-- e.g. "User data storage" --> | <!-- e.g. 99.9% --> | <!-- https://... --> | <!-- https://status.supabase.com --> |
| <!-- e.g. Payments --> | <!-- e.g. Stripe --> | <!-- e.g. "Subscription billing" --> | <!-- e.g. 99.99% --> | <!-- https://... --> | <!-- https://status.stripe.com --> |
| <!-- e.g. Email --> | <!-- e.g. Resend / SendGrid --> | <!-- e.g. "Transactional email" --> | <!-- e.g. 99.9% --> | <!-- https://... --> | <!-- https://status.resend.com --> |
| <!-- e.g. Auth --> | <!-- e.g. Auth0 / Clerk --> | <!-- e.g. "User login" --> | <!-- e.g. 99.99% --> | <!-- https://... --> | <!-- https://status.clerk.com --> |
| <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |

---

### 17.2 Third-Party Actual Uptime (Monthly Tracking)

> Check each vendor's status page at the end of every month and record their actual uptime.

| Service | SLA Promise | Month 1 Actual | Month 2 Actual | Month 3 Actual | Incidents Caused | Compensation Claimed? |
|---|---|---|---|---|---|---|
| <!-- AI API --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ✅ / ❌ / N/A |
| <!-- Cloud --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ✅ / ❌ / N/A |
| <!-- Database --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ✅ / ❌ / N/A |
| <!-- Auth --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ✅ / ❌ / N/A |
| <!-- Payments --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | ✅ / ❌ / N/A |

---

### 17.3 Vendor Risk Assessment

> For every dependency, think: "What happens to our users if this vendor goes down?" Plan ahead.

| Service | If It Goes Down… | Our Backup Plan | Backup Status |
|---|---|---|---|
| <!-- AI API --> | <!-- e.g. "All AI features stop working" --> | <!-- e.g. "Fallback to Claude Haiku for basic tasks; queue heavy requests" --> | ⬜ Ready / ⬜ In Progress / ❌ None |
| <!-- Cloud --> | <!-- e.g. "Entire app is down" --> | <!-- e.g. "Multi-region failover to us-west-2" --> | ⬜ Ready / ⬜ In Progress / ❌ None |
| <!-- Database --> | <!-- e.g. "No user data accessible" --> | <!-- e.g. "Read replica in separate AZ + 15-min backups" --> | ⬜ Ready / ⬜ In Progress / ❌ None |
| <!-- Auth --> | <!-- e.g. "Users cannot log in" --> | <!-- e.g. "Extend existing JWT session TTL to 7 days during outage" --> | ⬜ Ready / ⬜ In Progress / ❌ None |

---

## 18. Disaster Recovery & Rollback Plan

> 💡 **A "disaster" in software means something went seriously wrong** — the app crashed, data was lost, or performance dropped so badly users cannot use it. This section is your emergency manual. Read it now so you know where to look when things are on fire.

---

### 18.1 Recovery Time Objectives

> These two numbers define how fast you must recover. Set them before launch.

| Metric | Plain-English Meaning | Your Target |
|---|---|---|
| **RTO** (Recovery Time Objective) | Maximum time the system can be down before it must be restored | `< <!-- fill: e.g. 30 minutes -->` |
| **RPO** (Recovery Point Objective) | Maximum amount of data you can afford to lose (how old the last backup can be) | `< <!-- fill: e.g. 1 hour of data -->` |

---

### 18.2 Rollback Triggers

> If ANY of the following conditions are detected in production, immediately consider a rollback.

| Trigger | Threshold | Who Detects It | Who Decides Rollback |
|---|---|---|---|
| API Error Rate spike | > 5% for > 5 minutes | Automated alert | Engineering Lead |
| P95 Latency spike | > 3× normal baseline for > 10 minutes | Automated alert | Engineering Lead |
| AI Safety failure | Any harmful output reaching users | Manual review | Engineering Lead + PM |
| Data corruption detected | Any confirmed data integrity failure | Engineering / DBA | CTO |
| Revenue-impacting incident | Payments failing for > 5% of users | Automated alert | CTO + PM |

---

### 18.3 Step-by-Step Rollback Runbook

```
ROLLBACK PROCEDURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

STEP 1 — DETECT & CONFIRM (< 5 minutes)
  ├── Confirm the alert is real (not a monitoring glitch)
  ├── Check the monitoring dashboard / status page
  ├── Identify WHICH component is failing:
  │     App server? Database? AI API? A specific feature?
  └── Classify severity: P1 / P2 / P3 (see Section 14.1)

STEP 2 — COMMUNICATE (< 10 minutes)
  ├── Post in #incidents Slack channel (or your team channel):
  │     "🚨 P[X] Incident: [Brief description]. Investigating."
  ├── If P1 → page on-call engineer immediately
  └── If users are affected → post to status page / in-app banner

STEP 3 — CONTAIN (< 15 minutes)
  Option A — Feature Flag:
    Turn off the broken feature flag → users lose one feature
    but the rest of the app keeps working
  Option B — Version Rollback:
    Revert deployment to previous known-good version:
    <!-- fill: e.g. "kubectl rollout undo deployment/api" -->
    <!-- fill: e.g. "railway rollback" or "vercel rollback" -->
  Option C — Traffic Redirect:
    Point traffic to a healthy region or standby environment

STEP 4 — VERIFY (< 5 minutes after rollback)
  ├── Run smoke tests on core user flows
  ├── Confirm error rate has returned to < 1%
  ├── Confirm P95 latency is back to baseline
  └── Confirm AI safety checks are passing

STEP 5 — COMMUNICATE RESOLUTION
  ├── Update status page: "Resolved at HH:MM UTC"
  ├── Post in #incidents: "✅ Resolved. Root cause: [brief]"
  └── Send user communication if > 15 min outage affected paying users

STEP 6 — POST-MORTEM (within 48 hours)
  ├── Write 5-Why root cause analysis
  ├── Document in Section 14.3 (Failure Log)
  └── Create ticket(s) for permanent fix

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

### 18.4 Rollback Command Reference

> Fill this in during setup so anyone on the team can execute a rollback, even at 2 AM.

| Component | Rollback Command / Steps | Who Has Permission | Last Tested Date |
|---|---|---|---|
| **Application (Backend)** | <!-- fill: e.g. "railway rollback" or kubectl command --> | <!-- fill: e.g. "Any engineer with prod access" --> | <!-- YYYY-MM-DD --> |
| **Frontend / Web App** | <!-- fill: e.g. "vercel rollback" or "netlify rollback" --> | <!-- fill --> | <!-- YYYY-MM-DD --> |
| **Mobile App (iOS)** | <!-- fill: e.g. "Phased rollout pause in App Store Connect" --> | <!-- fill --> | <!-- YYYY-MM-DD --> |
| **Mobile App (Android)** | <!-- fill: e.g. "Staged rollout halt in Play Console" --> | <!-- fill --> | <!-- YYYY-MM-DD --> |
| **Database Migration** | <!-- fill: e.g. "Run: alembic downgrade -1" --> | <!-- fill: e.g. "DBA or Engineering Lead only" --> | <!-- YYYY-MM-DD --> |
| **AI Prompt / Config** | <!-- fill: e.g. "Revert prompt config in CMS / config file" --> | <!-- fill --> | <!-- YYYY-MM-DD --> |

---

### 18.5 Backup & Restore Verification

> Test backups regularly. A backup you have never restored is not a backup.

| Backup Type | Frequency | Retention | Location | Last Restore Test | Test Passed? |
|---|---|---|---|---|---|
| **Database full backup** | <!-- e.g. Daily --> | <!-- e.g. 30 days --> | <!-- e.g. S3 bucket --> | <!-- YYYY-MM-DD --> | ✅ / ❌ |
| **Database incremental** | <!-- e.g. Hourly --> | <!-- e.g. 7 days --> | <!-- e.g. S3 bucket --> | <!-- YYYY-MM-DD --> | ✅ / ❌ |
| **Application config / secrets** | <!-- e.g. On every change --> | <!-- e.g. Indefinite --> | <!-- e.g. Vault / 1Password --> | <!-- YYYY-MM-DD --> | ✅ / ❌ |
| **User-uploaded files** | <!-- e.g. Real-time sync --> | <!-- e.g. 90 days --> | <!-- e.g. S3 + cross-region replication --> | <!-- YYYY-MM-DD --> | ✅ / ❌ |
| **AI model fine-tune weights** (if applicable) | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- YYYY-MM-DD --> | ✅ / ❌ |

---

## 19. Competitor Benchmark Comparison

> 💡 **Know where you stand in the market.** This section compares your product's performance against industry leaders and direct competitors. You do not need to beat everyone — but you need to know where the bar is so you can set realistic targets and find your competitive advantage.

---

### 19.1 How to Gather Competitor Data

> You cannot log into a competitor's servers, but there are legitimate ways to measure their public performance:

| Method | What You Measure | Tools |
|---|---|---|
| **Public Web Vitals** | LCP, INP, CLS of their web app | Google PageSpeed, WebPageTest.org |
| **API Response Time** | How fast their API responds (if public) | curl, Postman, k6 against their public endpoints |
| **AI Quality (manual)** | Run the same prompts on their product and score answers | Human review panel |
| **Uptime / Reliability** | Check their status page history | statuspage.io, Better Uptime, UptimeRobot |
| **User Perception** | What users say about speed & quality | G2, Product Hunt, Reddit, App Store reviews |
| **Published Benchmarks** | Vendor-published performance claims | Their documentation, blog posts, third-party reports |

> ⚠️ **Important:** Only use publicly available, ethical methods. Never attempt to scrape private data or violate a competitor's terms of service.

---

### 19.2 Competitor Performance Comparison Table

> Update this table quarterly. Fill in only what you can measure legitimately.

| Metric | **Your Product** | **Competitor A** | **Competitor B** | **Industry Leader** | Your Rank | Target to Beat |
|---|---|---|---|---|---|---|
| **Company / Product Name** | <!-- Your product --> | <!-- fill: e.g. "CompetitorX" --> | <!-- fill --> | <!-- fill: e.g. "Market Leader" --> | | |
| **Web LCP (Desktop)** | <!-- fill: ms --> | <!-- fill: ms --> | <!-- fill: ms --> | <!-- fill: ms --> | <!-- 1st / 2nd / 3rd --> | <!-- fill --> |
| **Web LCP (Mobile)** | <!-- fill: ms --> | <!-- fill: ms --> | <!-- fill: ms --> | <!-- fill: ms --> | <!-- fill --> | <!-- fill --> |
| **AI TTFT (avg)** | <!-- fill: ms --> | <!-- fill: ms --> | <!-- fill: ms --> | <!-- fill: ms --> | <!-- fill --> | <!-- fill --> |
| **AI Response Quality (manual score)** | <!-- fill: /5 --> | <!-- fill: /5 --> | <!-- fill: /5 --> | <!-- fill: /5 --> | <!-- fill --> | <!-- fill --> |
| **Uptime (last 90 days)** | <!-- fill: % --> | <!-- fill: % --> | <!-- fill: % --> | <!-- fill: % --> | <!-- fill --> | <!-- fill --> |
| **App Store Rating** | <!-- fill: /5 ⭐ --> | <!-- fill: /5 --> | <!-- fill: /5 --> | <!-- fill: /5 --> | <!-- fill --> | <!-- fill --> |
| **Play Store Rating** | <!-- fill: /5 ⭐ --> | <!-- fill: /5 --> | <!-- fill: /5 --> | <!-- fill: /5 --> | <!-- fill --> | <!-- fill --> |
| **Perceived Speed** (user reviews) | <!-- fill: Positive % --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> |
| **Free Tier Limits** | <!-- fill --> | <!-- fill --> | <!-- fill --> | <!-- fill --> | | |

---

### 19.3 Competitive Performance Narrative

> After filling the table, write 2–3 sentences answering each question.

**Where are we clearly better than competitors?**
> <!-- e.g. "Our AI TTFT is 340ms vs Competitor A's 820ms — more than 2× faster, which translates to a noticeably snappier experience in user testing." -->

**Where do competitors outperform us today?**
> <!-- e.g. "Competitor B's mobile app scores 4.6 on the App Store vs our 4.1. Root cause: their cold start time is 1.8s vs our 2.9s. We have a fix planned for Sprint 14." -->

**What is our single biggest performance differentiator to market?**
> <!-- e.g. "Best-in-class AI accuracy at 91% vs category average of 78%, confirmed by our independent eval dataset." -->

---

### 19.4 Benchmark Update Log

| Date | Who Updated | What Changed | Source |
|---|---|---|---|
| <!-- YYYY-MM-DD --> | <!-- fill --> | <!-- e.g. "Updated Competitor A LCP after they launched new CDN" --> | <!-- fill: e.g. "PageSpeed report" --> |
| <!-- YYYY-MM-DD --> | | | |

---

## 20. Changelog

> 💡 **Every time this document is updated, add a row here.** This is how you know what changed and when — critical when investigating a performance regression.

| Version | Date | Author | What Changed |
|---|---|---|---|
| 1.1.0 | 2026-10-14 | Template Author | Added Sections 17–19: Third-Party SLA, Disaster Recovery, Competitor Benchmarks. Added AI Quality Quick Check (9.0). |
| 1.0.0 | <!-- YYYY-MM-DD --> | <!-- fill --> | Initial template created from Performance_Benchmarks.md template |
| <!-- fill --> | <!-- YYYY-MM-DD --> | <!-- fill --> | <!-- fill --> |

---

<!-- ============================================================
  TEMPLATE METADATA (Do not delete this section)
  ============================================================
  Template Name:     Performance_Benchmarks.md
  Template Version:  1.0.0
  Designed For:      AI-Driven Development Life Cycle (AI-SDLC)
  Scope:             Web App / SaaS + Mobile App
  Lifecycle:         Development → Staging → Beta → 500 Customers
  Performance Pillars: Speed, AI Quality, Scalability, Cost
  Release Gate:      HARD GATE (all benchmarks must pass)
  Reporting:         Tables, Trends, Executive Summary, CI Badge
  Compatible Tools:  k6, Locust, JMeter, LangSmith, Helicone,
                     Datadog, Grafana, Google Lighthouse,
                     PageSpeed Insights, any monitoring tool
  Primary Language:  English (Beginner-Friendly)
  Last Updated:      2026-10-14
  ============================================================ -->
