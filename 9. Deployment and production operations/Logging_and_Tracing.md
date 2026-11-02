# How to Fill Out This Document (Read This First)

**What is this document?**
It is the single place where your project decides *how the product writes down what it is doing* (logging) and *how it follows one user request from start to finish* (tracing). When something breaks at 2 AM, this document is what lets your team find out why in minutes instead of days.

**Who can fill it in?** Anyone. You do not need to be an engineer. If you do not know an answer, write `UNKNOWN - ask [name]`. Never leave a blank and never guess silently.

**How every question works**

Each question has four parts:

| Part | Meaning |
|---|---|
| **Question** | What we need to know |
| **Hint** | The question in plain words |
| **Example** | A sample answer so you can copy the style |
| **Answer:** | Where you write. Replace the `___` |

**Rules for answering**

1. Replace every `___` with your answer. Delete the example when you are done, or keep it if it helps.
2. Tick a box by changing `[ ]` to `[x]`.
3. If a question does not apply to your product, write `N/A - because ...` (always give the reason).
4. Use real names, real numbers and real dates. Avoid "soon", "some", "fast", "many". Write "within 5 minutes", "30 days", "99.5%".
5. Never paste passwords, API keys, customer data or tokens into this document.
6. Fill sections in order. The **Final Readiness Checklist (Section 17)** at the end tells you whether you are done.
7. Mark each section status at its top: `Not started` / `In progress` / `Done` / `Reviewed`.

**Legend**

- 🔴 **Required**: the product must not launch without it.
- 🟡 **Recommended**: should have it by the time you reach 500 customers.
- 🟢 **Optional**: nice to have.
- 🤖 **AI-specific**: for AI-driven development and AI-powered features. Skip with a reason if not used.

**The 5 lifecycle phases used in this document**

| Phase | Name | Goal |
|---|---|---|
| 1 | Build | Developers (humans and AI agents) write code with logging built in |
| 2 | Test | QA proves logs and traces are correct, useful and safe |
| 3 | Pre-launch | Production setup, alerts and dashboards are ready and rehearsed |
| 4 | Launch | Launch day and the first 72 hours, with close watching |
| 5 | First 500 customers | Learn, tune, control cost, and decide what to improve |

---

## Quick Start: One-Page Minimum Version (For Tiny or Early Projects)

*Use this if you have less than a day. Answer these 12 questions now, then come back and fill the full document before launch. Anything you skip here must appear in the full document later.*

| # | Question | Answer |
|---|---|---|
| 1 | What does the product do (one sentence)? | ___ |
| 2 | Which parts can produce logs (frontend, backend, database, AI, jobs)? | ___ |
| 3 | Which logging tool/library will we use? | ___ |
| 4 | Will every log be JSON with `timestamp`, `level`, `service`, `trace_id`, `message`? | ☐ Yes ☐ No |
| 5 | What is the one most important user journey to trace end to end? | ___ |
| 6 | What must NEVER be logged (passwords, tokens, card numbers, personal data)? | ___ |
| 7 | How many days do we keep logs? | ___ |
| 8 | Who gets alerted when errors spike, and how? | ___ |
| 9 | What is the error-rate number that makes us roll back? | ___ |
| 10 | Does the product use AI? If yes, do we log model, tokens, cost, and latency (no private text)? | ___ |
| 11 | Can support find a problem from a Reference ID the user reads out? | ☐ Yes ☐ No |
| 12 | Who owns this document and approves launch? | ___ |

**Minimum rule:** if any of questions 4, 6, 8 or 9 is empty, do not launch.

---

## Document Control

**Status of whole document:** `Not started`

| Field | Answer |
|---|---|
| Project name | ___ |
| Project ID / code | ___ |
| Document owner (one person) | ___ |
| Reviewer(s) | ___ |
| Version | 0.2 |
| Date created | ___ |
| Last updated | ___ |
| Related docs (links): Architecture, Incident Response, Security, Runbook, Monitoring/Alerting | ___ |

---

## 1. Project Snapshot 🔴

**Status:** `Not started`

**1.1 What does the product do, in two sentences?**
*Hint: Explain it to a friend who has never heard of it.*
*Example: "A mobile app that lets dog owners book walkers. Owners pay in the app and walkers share live location."*
**Answer:** ___

**1.2 What type of product is it?** (tick all that apply)
- [ ] Website / web app
- [ ] Mobile app (iOS / Android)
- [ ] API / backend service only
- [ ] Desktop software
- [ ] Browser extension
- [ ] AI chatbot / AI agent / AI features inside the product
- [ ] Background jobs / scheduled tasks
- [ ] Other: ___

**1.3 What are the main parts of the system?**
*Hint: List each piece that can produce a log. Frontend, backend, database, payment provider, email service, AI model provider, queue, etc.*

| Component | Technology | Who owns it | Produces logs? | Produces traces? |
|---|---|---|---|---|
| Example: Web frontend | React | Team A | Yes | Yes |
| ___ | ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ | ___ |

**1.4 Where does the product run?**
- [ ] Cloud (name: ___ )
- [ ] On-premise / own servers
- [ ] Serverless (functions)
- [ ] Containers / Kubernetes
- [ ] User's own device
- [ ] Mix: ___

**1.5 Which environments exist?**
*Example: local, development, staging, production.*
**Answer:** ___

**1.6 What is the launch date, and what is the "first 500 customers" target date?**
**Answer:** Launch: ___ | 500 customers target: ___

**1.7 Which countries/regions will customers be in?** (this affects privacy laws, see Section 8)
**Answer:** ___

---

## 2. Goals: Why Do We Log and Trace? 🔴

**Status:** `Not started`

**2.1 What questions must our logs and traces be able to answer within 10 minutes?**
*Hint: Think of the worst day. What would you ask?*
*Examples:*
- *"Why did customer X's payment fail?"*
- *"Which step of sign-up is slow?"*
- *"Did the AI answer using the right documents?"*
- *"What changed right before errors started?"*

**Answer (list at least 5):**
1. ___
2. ___
3. ___
4. ___
5. ___

**2.2 What are the top 3 things that must NEVER go wrong silently?**
*Example: Payments, data deletion, login, AI giving harmful advice.*
**Answer:** ___

**2.3 Success targets** 🟡
*Hint: Numbers that tell us logging works.*

| Target | Example | Your target |
|---|---|---|
| Time to detect a problem | under 5 minutes | ___ |
| Time to find the cause | under 30 minutes | ___ |
| % of requests that have a trace ID | 100% | ___ |
| % of errors that have enough detail to fix | 95% | ___ |
| Logging cost limit per month | $300 | ___ |

---

## 3. The Basics (Plain-Words Glossary) 🔴

*You do not need to answer anything here. Read it so the rest makes sense.*

| Word | Plain meaning |
|---|---|
| **Log** | A diary line the product writes: "At 10:01 user 42 logged in." |
| **Trace** | The full journey of one request through every part of the system, like a package tracking page. |
| **Span** | One stop in that journey (e.g., "database query took 40 ms"). A trace is made of many spans. |
| **Trace ID** | A unique number stuck on one journey so all its logs can be found together. |
| **Correlation / Request ID** | A label that ties logs from different services to the same user action. |
| **Metric** | A number over time (requests per second, error rate). |
| **Log level** | How serious a line is: DEBUG, INFO, WARN, ERROR, FATAL. |
| **Structured log** | A log written as labeled fields (JSON), not a loose sentence, so computers can search it. |
| **Sampling** | Keeping only some traces (e.g., 10%) to save money. |
| **Retention** | How long we keep logs before deleting them. |
| **PII** | Personal information: name, email, phone, address, ID numbers, IP address. |
| **Observability** | Being able to understand what is happening inside the system from the outside, using logs, metrics and traces together. |
| **Alert** | An automatic message to a person when something looks wrong. |
| **SLO / SLA** | A promise about reliability (e.g., "99.5% of requests succeed"). |
| **LLM / Agent** | An AI model / an AI that takes multiple steps and uses tools. |
| **Token** | A piece of text the AI reads or writes. More tokens = more cost. |

---

## 4. Logging Design 🔴

**Status:** `Not started`

### 4.1 Log levels

**Q4.1.1 Which log levels will we use, and what does each one mean for us?**
*Hint: Keep the defaults unless you have a strong reason.*

| Level | Default meaning | Shown in production? | Your change (if any) |
|---|---|---|---|
| DEBUG | Detailed developer info | No (turn on temporarily) | ___ |
| INFO | Normal important events (user signed up, order placed) | Yes | ___ |
| WARN | Something odd but the product still works | Yes | ___ |
| ERROR | An action failed | Yes, alert if frequent | ___ |
| FATAL | Product cannot continue | Yes, alert immediately | ___ |

**Q4.1.2 What is the default log level in each environment?**

| Environment | Default level |
|---|---|
| Local | ___ (example: DEBUG) |
| Development | ___ (example: DEBUG) |
| Staging | ___ (example: INFO) |
| Production | ___ (example: INFO) |

**Q4.1.3 Who is allowed to temporarily raise the level in production, for how long, and how is it changed back?**
**Answer:** ___

### 4.2 Log format

**Q4.2.1 What format will all logs use?**
- [ ] JSON (structured), **recommended**
- [ ] Plain text
- [ ] Other: ___

**Q4.2.2 Which fields must EVERY log line contain?** 🔴
*Hint: Tick the ones you want. The first group is strongly recommended.*

- [ ] `timestamp` (UTC, ISO-8601, e.g. 2026-10-18T10:01:05Z)
- [ ] `level`
- [ ] `message` (a short human sentence)
- [ ] `service` (which part wrote it)
- [ ] `environment` (dev / staging / production)
- [ ] `version` (app version or git commit)
- [ ] `trace_id`
- [ ] `span_id`
- [ ] `request_id`
- [ ] `user_id` (an internal ID, **never** email or name)
- [ ] `session_id`
- [ ] `error.type`, `error.message`, `error.stack`
- [ ] `duration_ms`
- [ ] `host` / `container` / `region`
- [ ] `feature_flag` state
- [ ] `tenant_id` / `account_id`
- [ ] Other: ___

**Q4.2.3 Show one example of a perfect log line for your product.**
*Example:*
```json
{"timestamp":"2026-10-18T10:01:05Z","level":"ERROR","service":"payments-api","environment":"production","version":"1.4.2","trace_id":"abc123","request_id":"req-789","user_id":"u_42","message":"Card charge failed","error.type":"CardDeclined","duration_ms":812}
```
**Answer:**
```json
___
```

**Q4.2.4 Naming rules.** Field names style: `snake_case` / `camelCase`? Time zone: UTC only?
**Answer:** ___

### 4.3 What to log

**Q4.3.1 Which events MUST always be logged?** 🔴 (tick all that apply)

- [ ] App start, stop, crash, restart
- [ ] Every incoming request: method, path, status, duration
- [ ] Sign-up, login, logout, failed login, password reset, permission changes
- [ ] Payments, refunds, subscription changes
- [ ] Data created / changed / deleted (audit trail)
- [ ] Calls to outside services (payment, email, SMS, AI provider) with result and time
- [ ] Background job start, success, failure, retry
- [ ] Configuration or feature-flag changes
- [ ] Deployments and rollbacks
- [ ] Security events (blocked requests, suspicious activity, rate-limit hits)
- [ ] Slow operations (above ___ ms)
- [ ] Other: ___

**Q4.3.2 What business events matter for learning about the first 500 customers?** 🟡
*Example: signed_up, finished_onboarding, first_purchase, invited_friend, cancelled.*
**Answer:** ___

### 4.4 What to NEVER log

**Q4.4.1 Tick the data that must NEVER appear in logs.** 🔴

- [ ] Passwords, PINs, security answers
- [ ] API keys, tokens, secrets, private keys
- [ ] Full credit card numbers, bank numbers, CVV
- [ ] Government ID numbers (SSN, passport, Aadhaar, etc.)
- [ ] Health, biometric or children's data
- [ ] Full email, phone, home address (use masked or hashed form)
- [ ] Full request/response bodies containing the above
- [ ] Raw AI prompts or documents that contain customer private data 🤖
- [ ] Other: ___

**Q4.4.2 How will sensitive data be protected when it must appear?**
- [ ] Masking (j***@mail.com)
- [ ] Hashing
- [ ] Tokenization / replace with internal ID
- [ ] Drop the field entirely
- [ ] Automatic scrubbing tool (name: ___ )

**Q4.4.3 How will we catch accidental leaks?** (e.g., automated test that scans logs for emails/card numbers)
**Answer:** ___

### 4.5 Error handling in logs

**Q4.5.1 Rules for errors.** Tick the ones you agree with:
- [ ] Log an error once, at the place that handles it (no duplicate logs of the same error)
- [ ] Always include what failed, why, and which user action was affected
- [ ] Include stack trace for unexpected errors only
- [ ] Never log an expected situation (like "wrong password") as ERROR; use INFO/WARN
- [ ] Error messages are searchable (use stable error codes like `PAY-1001`)

**Q4.5.2 Do we have an error-code list?** Where: ___

---

## 5. Tracing Design 🔴

**Status:** `Not started`

**Q5.1 Will we use distributed tracing?**
- [ ] Yes, from day one (**recommended** if more than one service or an AI/agent flow)
- [ ] Only request IDs (single simple app)
- [ ] Later (reason and date): ___

**Q5.2 Which standard will we follow?**
- [ ] OpenTelemetry (**recommended**, vendor-neutral)
- [ ] Vendor's own agent (name: ___ )
- [ ] Other: ___

**Q5.3 Which journeys MUST be traced end to end?** 🔴
*Hint: The paths that make or lose money or trust.*
*Example: Sign-up → Verify email → First login; Add to cart → Pay → Confirmation email.*

| # | Journey name | Start point | End point | Components crossed |
|---|---|---|---|---|
| 1 | ___ | ___ | ___ | ___ |
| 2 | ___ | ___ | ___ | ___ |
| 3 | ___ | ___ | ___ | ___ |

**Q5.4 How will the trace ID travel between parts?**
- [ ] W3C `traceparent` HTTP header (**recommended**)
- [ ] Message-queue headers/metadata
- [ ] Included in background job payloads
- [ ] Passed from frontend/mobile to backend
- [ ] Returned to the user in error screens so support can look it up ("Reference: abc123")

**Q5.5 Sampling: how much do we keep?** 🟡
*Hint: Keeping 100% is best for small products (under 500 customers) if cost allows.*

| Environment | Normal requests kept | Errors kept | Slow requests kept |
|---|---|---|---|
| Staging | ___ (example: 100%) | 100% | 100% |
| Production | ___ (example: 100% until 500 customers) | 100% | 100% |

**Q5.6 What extra details (attributes) do we attach to spans?**
*Example: user_id (internal), plan type, feature flag, region, app version.*
**Answer:** ___

**Q5.7 Which operations get their own span?**
- [ ] Incoming request
- [ ] Database query
- [ ] Cache call
- [ ] Outside API call
- [ ] Queue publish / consume
- [ ] Background job
- [ ] File upload / download
- [ ] AI model call 🤖
- [ ] Other: ___

**Q5.8 How long do we keep traces?** ___ days (example: 14)

---

## 6. Metrics and the Three Pillars 🟡

**Status:** `Not started`

*Logs say what happened. Traces say where. Metrics say how much. We need all three.*

**Q6.1 Which key numbers (metrics) will we watch?**

| Metric | Why it matters | Example target | Your target |
|---|---|---|---|
| Request rate | Is traffic normal? | n/a | ___ |
| Error rate | Are users failing? | under 1% | ___ |
| Latency p50 / p95 / p99 | Is it slow? | p95 under 500 ms | ___ |
| CPU / memory / disk | Is the server running out of room? | under 80% | ___ |
| Queue length / job failures | Is background work stuck? | under 100 | ___ |
| Sign-ups per day | Business health | ___ | ___ |
| Payment success rate | Money health | over 97% | ___ |
| AI cost per user per day 🤖 | Cost control | under $___ | ___ |

**Q6.2 How do logs, metrics and traces link together?** (e.g., click a spike on a chart → see traces → see logs by trace_id)
**Answer:** ___

---

## 6A. Reliability Promises: SLIs, SLOs and Error Budgets 🟡

**Status:** `Not started`

*Plain words: An **SLI** is a number we measure (like "% of requests that worked"). An **SLO** is the goal for that number ("99.5% over 30 days"). An **error budget** is how much failure we can afford before we stop adding features and fix things (100% minus the SLO).*

**Q6A.1 Which user journeys deserve a reliability promise?**
*Hint: Start with the journeys in Q5.3. Pick 2 to 4 for the first 500 customers.*

| Journey | SLI (what we measure) | How it is measured (log, trace or metric) | SLO target | Window | Error budget |
|---|---|---|---|---|---|
| Example: Login | % of login requests returning success within 1 second | Trace on `/login` | 99.5% | 30 days | 0.5% (about 3.6 hours of full failure) |
| Example: Payment | % of payments that complete without error | Payment-service logs | 99% | 30 days | 1% |
| Example: AI answer 🤖 | % of AI answers returned in under 8 seconds with no error | AI trace spans | 98% | 30 days | 2% |
| ___ | ___ | ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ | ___ | ___ |

**Q6A.2 Which events do NOT count against the promise?** (planned maintenance, customer's own mistakes, outside-provider outages we cannot control)
**Answer:** ___

**Q6A.3 What do we do when the error budget is nearly used up?**
*Example: At 50% used → team lead is told. At 80% used → pause risky releases. At 100% used → only fixes ship until recovered.*

| Budget used | Action | Who decides |
|---|---|---|
| 50% | ___ | ___ |
| 80% | ___ | ___ |
| 100% | ___ | ___ |

**Q6A.4 Are alerts based on how fast we are burning the budget?** 🟡
*Example: "Page a person if we would use 2% of the monthly budget in 1 hour" (fast burn); "Ticket if we would use 10% in 3 days" (slow burn).*
**Answer:** ___

**Q6A.5 Is there a customer-facing promise (SLA) that is different from our internal goal?**
☐ No ☐ Yes → what and where written: ___ (internal SLO should be stricter than the SLA)

**Q6A.6 With few customers, are the numbers statistically meaningful?**
*Hint: With under 500 customers a single failed request can swing the percentage. Write how you will avoid false alarms (for example, alert on counts, not just percentages, when traffic is low).*
**Answer:** ___

---

## 6B. Frontend, Mobile and Client-Side Logging 🟡

**Status:** `Not started` (mark `N/A - no client app` if skipped)

*Plain words: Problems often happen on the customer's phone or browser, where we cannot see them unless the app tells us.*

**Q6B.1 Which client apps exist?** (tick all)
- [ ] Web (browser)
- [ ] iOS
- [ ] Android
- [ ] Desktop app
- [ ] Browser extension
- [ ] Other: ___

**Q6B.2 What do we capture from clients?** (tick all)
- [ ] Crashes and unhandled errors, with app version and OS/browser version
- [ ] Failed network calls (URL path, status, time; never full body)
- [ ] Slow screens/pages (page load, time to first screen, slow taps)
- [ ] Web performance numbers (Core Web Vitals: LCP, INP, CLS)
- [ ] Key user actions ("tapped Pay", "finished onboarding")
- [ ] Breadcrumbs (last 20 actions before an error)
- [ ] Device info: model, memory, battery state, network type (Wi-Fi/4G/offline)
- [ ] Session replay or screenshots (only if privacy-approved; mask inputs)
- [ ] Release version and feature flags active
- [ ] Other: ___

**Q6B.3 How does the client join the trace?**
- [ ] Client creates the trace ID and sends it to the backend in every request header
- [ ] Backend creates it and returns it for the client to show
- [ ] Not joined yet (reason): ___

**Q6B.4 Privacy on the client.** 🔴 (tick all we enforce)
- [ ] Ask consent where the law requires it (cookies/analytics banners, app tracking prompts)
- [ ] Text typed into fields is never captured (passwords, card, messages)
- [ ] Mask or block sensitive screens in session replay
- [ ] No device advertising IDs or precise location unless approved
- [ ] Users can opt out of diagnostics: where: ___

**Q6B.5 Mobile-specific questions.**
- Offline: how long do we store logs on the device (___ MB / ___ days) and when are they sent?
- Battery/data: do we send logs only on Wi-Fi or when charging? ___
- Crash symbol files (dSYM / ProGuard-R8 mapping / source maps) uploaded for each release? ☐ Yes ☐ No (needed to read crash stack traces)
- How do we handle old app versions that are still installed? ___
- Maximum size of one log batch: ___ KB

**Q6B.6 Protect against noise and abuse.**
- [ ] Rate-limit client logs per user (max ___ events/minute)
- [ ] Drop duplicate errors (group by error signature)
- [ ] Reject logs from unknown apps (use app key; remember keys can be copied, so never trust client logs for security decisions)
- [ ] Limit log size per event

**Q6B.7 What does the user see when something fails?**
*Example: "Something went wrong. Reference ID: abc123. Tap to copy." The Reference ID must be the trace ID or request ID.*
**Answer:** ___

---

## 7. AI-Specific Logging and Tracing 🤖

**Status:** `Not started` (mark `N/A - no AI in product` if skipped)

### 7.1 AI inside the product (chatbots, agents, recommendations)

**Q7.1.1 Which AI features exist?**
**Answer:** ___ (example: support chatbot using Claude; document summarizer)

**Q7.1.2 For every AI call, which details are recorded?** (tick all)
- [ ] Trace ID and user/session ID (internal IDs)
- [ ] Model name and version
- [ ] Prompt template name and version (not the full private prompt)
- [ ] Parameters (temperature, max tokens)
- [ ] Input token count, output token count, **cost**
- [ ] Latency (time to first token and total)
- [ ] Result status (success, refused, timeout, rate-limited, error)
- [ ] Tool calls the agent made (tool name, inputs summary, result summary, duration)
- [ ] Each agent step as its own span (plan → tool → observe → answer)
- [ ] Documents/sources retrieved (IDs only) for retrieval-based answers
- [ ] Safety/guardrail filter results
- [ ] User feedback (thumbs up/down, report)
- [ ] Number of retries and fallbacks to other models
- [ ] Other: ___

**Q7.1.3 Do we store the full prompt and answer text?**
- [ ] No, only metadata (**safest**)
- [ ] Yes, with redaction of private data
- [ ] Yes, only for users who gave consent
- [ ] Yes, only in staging/test
  Reason, and retention days: ___

**Q7.1.4 How do we check AI quality in production?** 🟡
*Example: random 1% reviewed by a human weekly; automatic scoring; user thumbs-down triggers review.*
**Answer:** ___

**Q7.1.5 Which AI problems must raise an alert?**
- [ ] Sudden cost spike
- [ ] Spike in refusals or errors
- [ ] Very slow answers
- [ ] Spike in thumbs-down
- [ ] Possible prompt-injection or abuse patterns
- [ ] Model provider outage
- [ ] Other: ___

### 7.2 AI used to build the product (AI-driven development)

**Q7.2.1 Do AI coding agents write or change code in this project?**
- [ ] Yes, tools: ___
- [ ] No

**Q7.2.2 Rules we give the AI agents about logging.** (tick all we enforce)
- [ ] Use the project's logger only. No `print` / `console.log` in production code
- [ ] Follow the field list in Q4.2.2
- [ ] Never log anything from Q4.4.1
- [ ] Every new endpoint, job and external call gets a log and a span
- [ ] Every new error gets a stable error code
- [ ] AI-generated code must pass the logging checks in Section 12 before merge
- [ ] A human reviews any change that touches logging, tracing, or privacy
- [ ] Other: ___

**Q7.2.3 Where do we write these rules for the AI agent?** (e.g., `AGENTS.md`, `CLAUDE.md`, a prompt template)
**Answer:** ___

**Q7.2.4 Do we keep a record of AI-agent actions during development and deployment (who/what changed what, when)?**
**Answer:** ___

---

## 8. Privacy, Security and Compliance 🔴

**Status:** `Not started`

**Q8.1 Which rules apply to us?** (tick all that apply, or write "not sure, ask legal")
- [ ] GDPR (Europe)
- [ ] UK GDPR
- [ ] CCPA / CPRA (California)
- [ ] HIPAA (US health)
- [ ] PCI-DSS (cards)
- [ ] SOC 2
- [ ] ISO 27001
- [ ] India DPDP / other country law: ___
- [ ] Children's privacy rules (COPPA etc.)
- [ ] None known / unsure → owner to check with: ___

**Q8.2 Who can see logs and traces, and who cannot?**

| Role | Can read logs? | Can read traces? | Can see raw user data? | Can delete? |
|---|---|---|---|---|
| Developers | ___ | ___ | ___ | ___ |
| Support team | ___ | ___ | ___ | ___ |
| Managers | ___ | ___ | ___ | ___ |
| Contractors | ___ | ___ | ___ | ___ |
| AI agents | ___ | ___ | ___ | ___ |

**Q8.3 How do we protect the logs?**
- [ ] Encrypted in transit (TLS)
- [ ] Encrypted at rest
- [ ] Access needs sign-in with two-step verification
- [ ] Access to logs is itself logged (audit)
- [ ] Logs cannot be edited (tamper-resistant) for security/audit events
- [ ] Separate secure storage for audit logs

**Q8.4 How long do we keep each kind of data, and what happens after?** 🔴

| Data | Keep for | After that | Reason |
|---|---|---|---|
| Application logs (hot, quick search) | ___ (example 14 days) | ___ (archive/delete) | ___ |
| Application logs (archive) | ___ (example 90 days) | ___ | ___ |
| Security / audit logs | ___ (example 1 year) | ___ | ___ |
| Traces | ___ | ___ | ___ |
| AI prompts/answers (if stored) | ___ | ___ | ___ |
| Debug logs | ___ (example 3 days) | ___ | ___ |

**Q8.5 When a customer asks us to delete their data, how do we handle the logs?**
**Answer:** ___ (example: logs only contain internal IDs; delete mapping table so logs cannot be linked)

**Q8.6 Is any log data sent to another company or country?** (third-party tool, region)
**Answer:** ___

---

## 9. Tools and Infrastructure 🔴

**Status:** `Not started`

**Q9.1 Which tools do we use?** (write the name for each row, or `none yet`)

| Job | Tool name | Who owns it | Monthly cost | Reason chosen |
|---|---|---|---|---|
| Create logs (logging library) | ___ | ___ | ___ | ___ |
| Collect and ship logs | ___ (example: OpenTelemetry Collector, Fluent Bit) | ___ | ___ | ___ |
| Store and search logs | ___ (example: Loki, Elasticsearch, Datadog, CloudWatch) | ___ | ___ | ___ |
| Collect traces | ___ | ___ | ___ | ___ |
| View traces | ___ (example: Jaeger, Tempo, Datadog APM) | ___ | ___ | ___ |
| Metrics and dashboards | ___ (example: Prometheus, Grafana) | ___ | ___ | ___ |
| Alerting and paging | ___ (example: PagerDuty, Opsgenie) | ___ | ___ | ___ |
| Frontend / mobile errors | ___ (example: Sentry) | ___ | ___ | ___ |
| Uptime checks | ___ | ___ | ___ | ___ |
| AI tracing 🤖 | ___ (example: Langfuse, LangSmith, OpenTelemetry GenAI) | ___ | ___ | ___ |

**Q9.2 What happens if the logging system itself breaks?**
- [ ] The product keeps working (logging must never crash the product)
- [ ] Logs are buffered locally and re-sent
- [ ] We get an alert when logs stop arriving
- [ ] Backup place for logs: ___

**Q9.3 Can we switch tools later without rewriting the product?**
- [ ] Yes (we use open standards such as OpenTelemetry)
- [ ] No, locked in. Accepted because: ___

**Q9.4 Time sync:** Are all servers using the same clock (NTP) so timestamps line up? ☐ Yes ☐ No ☐ Unknown

---

## 10. Dashboards, Alerts and On-Call 🔴

**Status:** `Not started`

### 10.1 Dashboards

**Q10.1.1 Which dashboards will exist?**

| Dashboard | Who uses it | What it shows | Link |
|---|---|---|---|
| Health overview | Everyone | Errors, latency, traffic | ___ |
| Launch-day dashboard | Launch team | Sign-ups, payments, errors, AI cost | ___ |
| Customer-journey | Product | Where users drop off | ___ |
| Cost | Finance/owner | Logging, tracing and AI spend | ___ |
| AI quality 🤖 | AI owner | Refusals, thumbs-down, latency | ___ |

### 10.2 Alerts

**Q10.2.1 List the alerts.** 🔴
*Rule of thumb: every alert must tell a person exactly what to do. If nobody needs to act, it is not an alert, it is a dashboard.*

| Alert name | Condition (with numbers) | Severity (Critical / Warning / Info) | Who is told | How (phone, chat, email) | First action to take |
|---|---|---|---|---|---|
| Example: High error rate | Errors over 5% for 5 minutes | Critical | On-call engineer | Phone call | Open the health dashboard, check last deploy |
| Example: Logs stopped | No logs from payments for 10 minutes | Critical | On-call | Phone | Check collector and service |
| ___ | ___ | ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ | ___ | ___ |

**Q10.2.2 How do we avoid alert overload?**
- [ ] Weekly review: delete or fix noisy alerts
- [ ] Group related alerts
- [ ] Quiet hours rule: ___
- [ ] Every alert links to a runbook

### 10.3 On-call and incidents

**Q10.3.1 Who is on call, when, and who is the backup?**
**Answer:** ___

**Q10.3.2 Escalation: if the first person does not answer in ___ minutes, who is next?**
**Answer:** ___

**Q10.3.3 Where is the incident process and the runbook?** (link) ___

**Q10.3.4 After every serious incident, do we write a short review ("what happened, why, how to prevent it") and update logging/tracing if something was missing?**
☐ Yes ☐ No

---

## 11. Phase-by-Phase Plan (Development → First 500 Customers) 🔴

**Status:** `Not started`

*For each phase, answer the questions, then tick the checklist. A phase is "Done" only when every 🔴 box is ticked.*

### Phase 1: Build

**Q11.1.1 Who sets up logging and tracing in the code base, and by when?** ___
**Q11.1.2 Is there a shared logging library/template so every service logs the same way?** ☐ Yes (link: ___) ☐ No

**Checklist**
- [ ] 🔴 Logging library chosen and added to every service
- [ ] 🔴 Standard fields from Q4.2.2 are added automatically
- [ ] 🔴 Trace/request ID is created at the entry point and passed everywhere
- [ ] 🔴 Secrets and personal data masked automatically
- [ ] 🔴 Log levels controlled by configuration (no code change needed)
- [ ] 🔴 Error codes list started
- [ ] 🟡 Local setup lets a developer see logs and traces on their own computer
- [ ] 🟡 Code review checklist includes "logging and tracing present and safe"
- [ ] 🤖 AI agent rules added (Q7.2.2)

### Phase 2: Test

**Q11.2.1 How will QA test logging and tracing?** (tick all)
- [ ] Trigger a known error and confirm the log appears with the right fields
- [ ] Follow one request across all services using only the trace ID
- [ ] Automated test: scan logs for emails, tokens, card numbers (must find none)
- [ ] Load test: logs and traces still arrive under heavy traffic
- [ ] Failure test: switch off the logging system; the product must keep working
- [ ] Alert test: cause each alert on purpose and confirm the right person is told
- [ ] 🤖 Run sample AI conversations and confirm AI traces, token counts and costs are correct

**Checklist**
- [ ] 🔴 Every journey in Q5.3 can be traced start to finish in staging
- [ ] 🔴 Privacy scan passed (no sensitive data in logs)
- [ ] 🔴 Every critical alert fired successfully in a test
- [ ] 🟡 Log volume per user measured, and monthly cost estimated
- [ ] 🟡 A new team member can find the cause of a planted bug using only logs and traces

### Phase 3: Pre-launch

**Checklist**
- [ ] 🔴 Production logging, tracing and alerting turned on and verified
- [ ] 🔴 Retention and access rules from Section 8 applied
- [ ] 🔴 On-call schedule published and people confirmed
- [ ] 🔴 Runbook links attached to every critical alert
- [ ] 🔴 Dashboards from 10.1.1 built
- [ ] 🔴 Dry run ("fire drill"): a pretend incident was solved using these tools
- [ ] 🔴 Rollback plan ready, and rollback events appear in logs
- [ ] 🟡 Cost alerts and budget limits set
- [ ] 🟡 Support team trained to ask customers for the "Reference ID" (trace ID)
- [ ] 🟡 Status page or customer-message plan ready

### Phase 4: Launch (Launch day to +72 hours)

**Q11.4.1 Who watches the launch dashboard, in which shifts?**
**Answer:** ___

**Q11.4.2 Launch "stop and rollback" triggers.** Write numbers.
*Example: error rate above 5% for 10 minutes; payment success below 90%; AI cost 3x forecast.*
**Answer:** ___

**Checklist**
- [ ] 🔴 Launch team online, with a shared chat channel
- [ ] 🔴 Check every hour for the first 6 hours: errors, latency, sign-ups, payments
- [ ] 🔴 Temporary extra logging allowed, with an end time to turn it off
- [ ] 🔴 Every issue found gets a ticket and an owner
- [ ] 🟡 Review of the first 72 hours written (what we saw, what we fixed)

### Phase 5: First 500 customers

**Q11.5.1 Customer-count checkpoints.** Fill in what you will review at each point.

| Checkpoint | Review these | Decisions to make | Date reviewed |
|---|---|---|---|
| 10 customers | Do logs show real behavior? Any missing fields? | Fix gaps | ___ |
| 50 customers | Noisy logs, alert quality, slow journeys | Tune alerts and levels | ___ |
| 100 customers | Cost per customer, retention settings | Adjust sampling and retention | ___ |
| 250 customers | Capacity, trace storage, AI quality | Plan scaling | ___ |
| 500 customers | Full review of this document | Update template and set next goals | ___ |

**Checklist**
- [ ] 🔴 Weekly 30-minute review of top errors, slowest journeys and alert noise
- [ ] 🔴 Every customer-reported problem can be matched to a trace within 10 minutes
- [ ] 🟡 Monthly cost report: logs, traces, AI
- [ ] 🟡 Remove logs nobody uses; add logs for questions nobody could answer
- [ ] 🟡 Re-check privacy scan after every big release
- [ ] 🟢 Share lessons learned back into this template

---

## 12. Quality Gates (Rules for Merging and Releasing) 🔴

**Status:** `Not started`

**Q12.1 Which checks must pass before code is merged or released?** (tick all you enforce)
- [ ] Logging/tracing included for new code (checked by reviewer or automated rule)
- [ ] Linter blocks `print` / `console.log`
- [ ] Automated privacy scan of logs in test runs
- [ ] No secrets in code or logs (secret scanner)
- [ ] New alerts have runbook link and owner
- [ ] Log volume impact checked for loops and high-traffic paths
- [ ] 🤖 AI-generated code reviewed by a human for logging and privacy
- [ ] Other: ___

**Q12.2 Who can approve exceptions, and where is each exception written down?** ___

---

## 13. Cost Control 🟡

**Status:** `Not started`

**Q13.1 What is the maximum monthly budget for logs + traces + AI tracing?** $___

**Q13.2 Which cost-saving rules do we use?** (tick all)
- [ ] DEBUG off in production by default
- [ ] Sampling for very high-volume, low-value traces after 500 customers
- [ ] Shorter retention for noisy logs
- [ ] Move old logs to cheap storage
- [ ] Drop health-check noise
- [ ] Limit size of each log line (max ___ KB)
- [ ] Alert when daily volume is over ___ GB
- [ ] Other: ___

**Q13.3 Who reviews cost, and how often?** ___

---

## 14. Roles and Responsibilities 🔴

**Status:** `Not started`

| Job | Name | Backup |
|---|---|---|
| Owner of this document | ___ | ___ |
| Owner of logging standards | ___ | ___ |
| Owner of tracing setup | ___ | ___ |
| Owner of alerts and dashboards | ___ | ___ |
| Privacy / security approver | ___ | ___ |
| QA owner for logging tests | ___ | ___ |
| AI quality owner 🤖 | ___ | ___ |
| Launch commander | ___ | ___ |
| Support lead (uses Reference IDs) | ___ | ___ |
| Final approver | ___ | ___ |

---

## 15. Risks and Decisions 🟡

**15.1 Risk list**
*Example risks: logs leak personal data; logging bill explodes; alerts ignored; trace ID lost between services; AI prompts stored without consent.*

| # | Risk | How likely (Low/Med/High) | How bad (Low/Med/High) | Plan to reduce it | Owner |
|---|---|---|---|---|---|
| 1 | ___ | ___ | ___ | ___ | ___ |
| 2 | ___ | ___ | ___ | ___ | ___ |
| 3 | ___ | ___ | ___ | ___ | ___ |

**15.2 Decision log** (write down choices so nobody has to guess later)

| Date | Decision | Why | Who decided |
|---|---|---|---|
| ___ | ___ | ___ | ___ |

**15.3 Open questions** (things still unknown)

| # | Question | Who will answer | Due date |
|---|---|---|---|
| 1 | ___ | ___ | ___ |

---

## 16. Quick Troubleshooting Guide (Fill in for Your Product) 🟡

*Hint: Write the first three steps for common problems so anyone can start.*

| Problem | Step 1 | Step 2 | Step 3 |
|---|---|---|---|
| A customer says "it failed" | Ask for the Reference ID | Search the trace ID in ___ | Read the failing span and its logs |
| Errors suddenly spike | Check the deploy history | Compare errors by version | Roll back if over the trigger in Q11.4.2 |
| No logs from a service | Check the service is running | Check the collector | Check credentials and network |
| App is slow | Open the latency dashboard | Find the slowest span in a trace | Check the database and outside calls |
| AI answers are wrong or costly 🤖 | Open the AI trace | Check prompt version, sources, model | Switch to the fallback or older prompt version |
| ___ | ___ | ___ | ___ |

---

## 17. Final Readiness Checklist (Is This Document Good to Go?) 🔴

Tick every box. If any 🔴 box is empty, the product is **not ready** for launch.

**Completeness**
- [ ] 🔴 No `___` blanks remain (use `N/A - reason` or `UNKNOWN - owner` instead)
- [ ] 🔴 Every section's status is `Done` or `Reviewed`
- [ ] 🔴 Every name in Section 14 has confirmed they accept the role
- [ ] 🔴 Links in the Document Control table all open

**Safety**
- [ ] 🔴 Q4.4.1 "never log" list is agreed, and the privacy scan passes
- [ ] 🔴 Retention is defined for every data type (Q8.4)
- [ ] 🔴 Legal or privacy owner has reviewed Section 8

**Reliability and clients**
- [ ] 🟡 SLIs, SLOs and error-budget actions defined for the key journeys (Section 6A)
- [ ] 🟡 Client crash reporting works, with readable stack traces (Section 6B)
- [ ] 🔴 Client apps never capture passwords, card data or typed private text

**Visibility**
- [ ] 🔴 Every critical journey (Q5.3) is traceable end to end in production
- [ ] 🔴 Critical alerts tested and reach a real person
- [ ] 🔴 A fire drill has been completed

**People**
- [ ] 🔴 Someone new can follow Section 16 without help
- [ ] 🟡 Support team knows how to use the Reference ID

**Sign-off**

| Role | Name | Date | Signature / approval link |
|---|---|---|---|
| Document owner | ___ | ___ | ___ |
| Engineering lead | ___ | ___ | ___ |
| QA lead | ___ | ___ | ___ |
| Security / privacy | ___ | ___ | ___ |
| Final approver | ___ | ___ | ___ |

---

## 18. Change History

| Version | Date | Author | What changed |
|---|---|---|---|
| 0.1 | ___ | ___ | First draft |
| 0.2 | ___ | ___ | Added Quick Start, SLI/SLO section (6A), frontend/mobile section (6B), code snippets (Appendix C), filled-in example (Appendix D) |

---

## Appendix A: Copy-Paste Starter Standards (Edit to Fit)

**A1. Recommended default log levels:** Local=DEBUG, Dev=DEBUG, Staging=INFO, Production=INFO.

**A2. Recommended default retention:** App logs 14 days hot + 90 days archive; security/audit logs 1 year; traces 14 days; debug logs 3 days. Confirm with legal.

**A3. Recommended starter alerts:** Error rate over 5% for 5 min; p95 latency over 2x normal for 10 min; no logs from a critical service for 10 min; payment success under 90%; disk over 85%; job failures over 10 in 15 min; AI cost over 3x daily forecast 🤖.

**A4. Recommended "Reference ID" message for users:**
"Something went wrong. Please contact support and quote this Reference ID: `{trace_id}`."

**A5. Naming a good log message:** Say *what happened*, to *what*, with *what result*. Example: "Charge failed for order o_981: card declined." Avoid: "Error!", "Something broke", "Here".

## Appendix B: Plain-Words Reminders

- Logs are a diary. Traces are a package-tracking page. Metrics are a speedometer.
- If it is not written down, it did not happen.
- If it has personal data, hide it.
- If an alert fires and nobody knows what to do, the alert is unfinished.
- If you do not know, write `UNKNOWN - ask [name]`. Never guess silently.

## Appendix C: Starter Code Snippets (Adapt to Your Stack)

*Developers and AI coding agents can copy these. Replace names with your own. Non-technical fillers can skip this appendix.*

**C1. Structured JSON logging with trace ID (Python, standard library + OpenTelemetry)**
```python
import json, logging, os
from opentelemetry import trace

SENSITIVE_KEYS = {"password", "token", "authorization", "card_number", "email"}

class JsonFormatter(logging.Formatter):
    def format(self, record):
        span = trace.get_current_span().get_span_context()
        data = {
            "timestamp": self.formatTime(record, "%Y-%m-%dT%H:%M:%S%z"),
            "level": record.levelname,
            "service": os.getenv("SERVICE_NAME", "unknown"),
            "environment": os.getenv("APP_ENV", "dev"),
            "version": os.getenv("APP_VERSION", "0.0.0"),
            "trace_id": format(span.trace_id, "032x") if span.is_valid else None,
            "span_id": format(span.span_id, "016x") if span.is_valid else None,
            "message": record.getMessage(),
        }
        extra = getattr(record, "fields", {})
        for k, v in extra.items():
            data[k] = "[REDACTED]" if k.lower() in SENSITIVE_KEYS else v
        if record.exc_info:
            data["error.stack"] = self.formatException(record.exc_info)
        return json.dumps(data)

handler = logging.StreamHandler()
handler.setFormatter(JsonFormatter())
log = logging.getLogger("app")
log.addHandler(handler)
log.setLevel(os.getenv("LOG_LEVEL", "INFO"))

log.info("Order placed", extra={"fields": {"order_id": "o_981", "user_id": "u_42"}})
```

**C2. Structured logging with trace ID (Node.js, pino + OpenTelemetry)**
```javascript
const pino = require("pino");
const { trace } = require("@opentelemetry/api");

const logger = pino({
  level: process.env.LOG_LEVEL || "info",
  base: { service: process.env.SERVICE_NAME, environment: process.env.APP_ENV, version: process.env.APP_VERSION },
  redact: ["req.headers.authorization", "password", "token", "card_number", "email"],
  mixin() {
    const ctx = trace.getActiveSpan()?.spanContext();
    return ctx ? { trace_id: ctx.traceId, span_id: ctx.spanId } : {};
  },
});

logger.info({ order_id: "o_981", user_id: "u_42" }, "Order placed");
```

**C3. Sampling and propagation (environment variables, OpenTelemetry standard)**
```bash
OTEL_SERVICE_NAME=payments-api
OTEL_RESOURCE_ATTRIBUTES=deployment.environment=production,service.version=1.4.2
OTEL_TRACES_SAMPLER=parentbased_traceidratio
OTEL_TRACES_SAMPLER_ARG=1.0          # 1.0 = keep 100%. Lower later to save cost.
OTEL_PROPAGATORS=tracecontext,baggage
OTEL_EXPORTER_OTLP_ENDPOINT=https://collector.example.com:4318
```

**C4. Recording an AI call as a span (language-neutral checklist) 🤖**
For every model call, create a span named `llm.call` and set these attributes:
`llm.model`, `llm.prompt_template_version`, `llm.input_tokens`, `llm.output_tokens`, `llm.cost_usd`, `llm.latency_ms`, `llm.status`, `llm.retry_count`. Create child spans for each tool call (`agent.tool.<name>`). Do **not** store prompt or answer text unless Q7.1.3 allows it.

**C5. Example alert rule in plain words**
"If the share of requests with status 500 is above 5% for 5 minutes in production, page the on-call engineer and link the runbook `runbooks/high-error-rate.md`."

## Appendix D: Fully Filled-In Example (Fictional "PawWalk" App)

*Use this to see what a good answer looks like. Everything here is invented. Do not copy it blindly.*

**Project:** PawWalk, a mobile app (iOS and Android) plus a web admin and a backend API. Owners book dog walkers, pay in-app, and watch live walks. It has an AI helper that answers owner questions.

**Q1.3 Components**

| Component | Technology | Owner | Logs? | Traces? |
|---|---|---|---|---|
| Mobile apps | Swift / Kotlin | Mobile team | Yes | Yes |
| Backend API | Node.js on containers | Backend team | Yes | Yes |
| Database | PostgreSQL (managed) | Backend team | Yes | Yes |
| Payment provider | Third-party | Backend team | Via our API logs | Via our spans |
| AI helper | Claude API via our backend | AI owner | Yes | Yes |

**Q2.1 Questions logs must answer:** Why did a booking fail? Which walker location update was late? Why did a payment decline? Did the AI helper use the right FAQ pages? What changed before errors started?

**Q2.3 Targets:** Detect in under 5 min; find cause in under 30 min; 100% of API requests carry a trace ID; logging budget $250 per month.

**Q4.2 Standard fields:** timestamp, level, service, environment, version, trace_id, span_id, request_id, user_id (internal), duration_ms, error.type, error.message.

**Q4.4 Never log:** passwords, tokens, card data, full phone numbers, exact home address, dog-owner chat text, raw AI prompts. Phone numbers shown as `***-***-1234`. Daily automated scan checks staging logs for emails and card patterns.

**Q5.3 Journeys:** (1) Sign-up → verify phone → first login. (2) Book walk → pay → walker accepts. (3) Live walk location updates. (4) Ask AI helper → answer shown.

**Q5.5 Sampling:** Production 100% of traces until 500 customers; then review.

**Q6A SLOs:** Booking success 99% over 30 days (budget 1%). Payment success 99%. AI answer in under 8 s for 98%. Budget 80% used → pause risky releases.

**Q6B Client logging:** Crashes with symbol files uploaded each release; failed network calls (path and status only); no typed text; session replay off; opt-out in Settings → Privacy; offline logs stored up to 5 MB for 3 days, sent on Wi-Fi.

**Q7.1 AI logging:** Model, prompt template version, tokens, cost, latency, status, retries, FAQ document IDs, thumbs up/down. No prompt or answer text stored; 1% of thumbs-down chats reviewed with user consent.

**Q8.4 Retention:** App logs 14 days hot and 90 days archive; security logs 1 year; traces 14 days; debug logs 3 days.

**Q10.2 Example alerts**

| Alert | Condition | Severity | Who | First action |
|---|---|---|---|---|
| High API errors | 5xx over 5% for 5 min | Critical | On-call, phone | Check last deploy; roll back if over 10 min |
| Payment drop | Success under 90% for 10 min | Critical | On-call + owner | Check payment provider status page |
| AI cost spike | Daily cost 3x forecast | Warning | AI owner, chat | Check for abuse or a looping agent |
| Logs stopped | No API logs for 10 min | Critical | On-call, phone | Check collector and credentials |

**Q11.4.2 Launch rollback triggers:** error rate above 5% for 10 min; payment success under 90%; AI cost 3x forecast.

**Q11.5.1 Checkpoints:** 10 customers → confirm real-world logs have all fields; 50 → tune noisy alerts; 100 → review cost per customer; 250 → plan capacity; 500 → full document review and update this template.
