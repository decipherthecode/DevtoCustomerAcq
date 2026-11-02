# HOW TO FILL THIS DOCUMENT (READ THIS FIRST)

**What is this file?**
This is the **Agent Registry**. It is the single list of every AI agent that helps build, test, launch, or run your product, from the first idea until your **first 500 customers** are using it.

Think of it as a **team roster for AI helpers**. For every helper you write down: who it is, what it does, what it may touch, who is in charge of it, and how you know it is doing a good job.

**Why does it matter?**
- Nobody has to guess what an agent is allowed to do.
- If something goes wrong, you know who to call and how to switch the agent off.
- You can copy this file to any new project and start fast.

---

## The 10 simple rules

1. **Fill the blanks.** Anything inside `{{double curly brackets}}` is a blank. Replace the whole thing, brackets included.
   - Before: `Agent name: {{Agent name}}`
   - After: `Agent name: Code Reviewer`
2. **Pick from the lists.** When you see `Choose one:`, keep one option and delete the others.
3. **Do not know an answer? Write `TBD` + who + date.** Example: `TBD (Sam, by 2026-11-01)`. Never leave a blank and never guess. Every `TBD` is collected in Section 13.
4. **Does not apply? Write `N/A` + a reason.** Example: `N/A (this agent never talks to customers)`.
5. **Never write secrets here.** No passwords, API keys, or tokens. Write only *where* they are kept. Example: `Stored in: password manager, vault "Project-Keys"`.
6. **One agent = one card.** Copy the card in Section 5 for every agent. Give each a new ID (AGT-001, AGT-002...).
7. **Use plain words.** If a 10-year-old could not understand a sentence, rewrite it shorter.
8. **Dates look like this:** `YYYY-MM-DD` (example: `2026-10-17`).
9. **Keep it current.** When anything about an agent changes, update the card and add a line to the Change Log (Section 14).
10. **Not sure what a word means?** Check the Glossary (Section 2).

## Quick start (about 30 minutes for your first agent)

| Step | What to do | Where |
|---|---|---|
| 1 | Fill in the project basics | Section 0 and 1 |
| 2 | Read the glossary once | Section 2 |
| 3 | Write the agent's name and job on the index table | Section 4 |
| 4 | Copy the Agent Card and fill every blank | Section 5 |
| 5 | Mark which lifecycle phases each agent works in | Section 3 |
| 6 | Fill the shared rules that apply to all agents | Section 7 |
| 7 | Run the readiness checklist before each phase starts | Section 12 |
| 8 | Clear every `TBD` | Section 13 |
| 9 | Fill the team roles and the budget plan | Section 3.3 and 7.1 |
| 10 | Score your registry (0-100) | Section 15 |

## What the symbols mean

| Symbol | Meaning |
|---|---|
| `{{...}}` | A blank you must fill |
| `Choose one:` | Keep exactly one option |
| `Choose all that apply:` | Keep every option that is true |
| `[ ]` / `[x]` | Unchecked / checked box |
| `TBD` | I do not know yet, and a person and date are attached |
| `N/A` | Does not apply, and a reason is attached |
| 🔴 Required | Must be filled before the agent starts working |
| 🟡 Advanced (optional) | Fill if your project needs it, otherwise write `N/A` + reason |

## How to know you are done

- [ ] No `{{...}}` blanks are left anywhere.
- [ ] Every agent has an owner who is a real, reachable person.
- [ ] Every agent has an autonomy level and a "stop button" (kill switch).
- [ ] All `TBD` items are listed in Section 13 with a person and a date.
- [ ] Another person has read it and says, "I understand it without asking you."

---
---

# AGENT REGISTRY

> **Master template version: 1.0.0** (do not change this line in your project copy; it tells you which template version you started from)

## 0. Document Control 🔴 Required

| Field | Your answer |
|---|---|
| Template version this copy was made from | 1.0.0 |
| Where the master template lives | {{Link or path to the master Agent_Registry.md}} |
| Is a newer master template available? (check every 6 months) | Choose one: `No` / `Yes, upgrade planned on {{YYYY-MM-DD}}` |
| Project name | {{Project name}} |
| Project ID prefix (2-5 capital letters, used in agent IDs) | {{e.g. ACME}} |
| Registry owner (one named person) | {{Full name}} |
| Owner contact (email or chat handle) | {{Contact}} |
| Registry version | {{e.g. 1.0.0}} |
| Last updated | {{YYYY-MM-DD}} |
| Status | Choose one: `Draft` / `In Review` / `Approved` / `Retired` |
| Approved by | {{Full name}} on {{YYYY-MM-DD}} |
| Where this file lives | {{Folder path or link}} |

## 1. Project Snapshot 🔴 Required

| Field | Your answer |
|---|---|
| One sentence: what does the product do? | {{Example: "An app that helps small bakeries take online orders."}} |
| Who is it for? | {{Example: "Bakery owners with 1 to 10 staff."}} |
| Product type | Choose one: `Web app` / `Mobile app` / `Desktop app` / `API / developer tool` / `Internet-of-things / hardware` / `Other: ____` |
| Today's phase (see Section 3) | {{Phase number and name}} |
| Planned launch date | {{YYYY-MM-DD}} |
| Goal | Reach **500 active customers** by {{YYYY-MM-DD}} |
| What counts as a "customer" for this goal? | {{Example: "A person who completed signup and used the product at least once in 30 days."}} |
| Team size (people) | {{Number}} |
| Main AI platforms used | Choose all that apply: `Claude Code` / `Claude API` / `n8n` / `Zapier` / `Make` / `Other: ____` |

## 2. Glossary (Simple Words)

| Word | What it means |
|---|---|
| **Agent** | An AI helper that can do a job, often by using tools, not just chat. |
| **Build-time agent** | An agent that helps *make* the product (writes code, tests, writes docs). Customers never see it. |
| **Product agent** | An agent that is *part of* the product. Customers use it directly or are affected by it. |
| **Owner** | The one real person responsible for an agent. If it breaks, they are called first. |
| **Tool** | Something the agent can use to act: a code editor, a database, email, a web search. |
| **MCP server** | A plug-in connection that gives an agent access to a tool or app (for example Notion or Supabase). |
| **Permission** | What the agent is allowed to do with a tool: read only, write, delete, send, spend money. |
| **Autonomy level** | How much the agent may do without a human saying "yes" (see Section 5, part D). |
| **Human approval** | A person checks and says "OK" before the agent's action happens. |
| **Escalation** | The agent hands the problem to a human because it should not decide alone. |
| **Kill switch** | The fastest safe way to turn an agent off. |
| **Prompt / instructions** | The written rules that tell the agent how to behave. |
| **Model** | The AI "brain" behind the agent (for example Claude Sonnet). |
| **Hallucination** | When an AI states something false as if it were true. |
| **Token** | A small piece of text an AI reads or writes; usage is billed by tokens. |
| **Evaluation (eval)** | A test that checks whether the agent does its job well. |
| **Risk level** | How much harm could happen if the agent makes a mistake: Low, Medium, High, Critical. |
| **PII** | Personal information: names, emails, phone numbers, addresses, payment details. |
| **Lifecycle phase** | One stage of the product journey, from Discover to Maintain/Retire. |
| **Gate** | A checkpoint you must pass before moving to the next phase. |
| **TBD** | "To be decided" with a person and date attached. |

---

## 3. Lifecycle Phases: From First Idea to 500 Customers 🔴 Required

> Every agent is tied to one or more of these 8 phases. Use the same phase numbers everywhere in this file.

| # | Phase | Plain-words goal | Typical agents here | Gate: you may move on when... |
|---|---|---|---|---|
| 1 | **Discover** | Find out if the problem is real | Research agent, interview-summary agent | Problem and target customer are written down |
| 2 | **Plan** | Decide what to build and in what order | Planning agent, spec-writing agent | Requirements (PRD) and scope are approved |
| 3 | **Design** | Decide how it looks and works | Design agent, architecture agent | Design and technical plan are approved |
| 4 | **Build** | Create the product | Coding agent, code-review agent, docs agent | Core features work and code is reviewed |
| 5 | **Test** | Prove it works and is safe | QA/test agent, security-check agent | Test pass bar met; no open critical bugs |
| 6 | **Launch** | Release to real people | Release agent, onboarding agent, monitoring agent | Launch checklist (Section 12) fully ticked |
| 7 | **Grow to 500** | Get and keep the first 500 customers | Support agent, feedback agent, analytics agent | 500 active customers reached (see Section 1 definition) |
| 8 | **Maintain / Retire** | Keep it healthy, or shut it down safely | Maintenance agent, cost-watch agent | Ongoing; retirement checklist if closing |

### 3.1 Phase Gate Log

Fill one row each time a phase ends.

| Phase | Gate passed on | Approved by | Agents added | Agents changed | Agents retired | Notes |
|---|---|---|---|---|---|---|
| {{1 Discover}} | {{YYYY-MM-DD}} | {{Name}} | {{AGT-IDs or none}} | {{AGT-IDs or none}} | {{AGT-IDs or none}} | {{Notes}} |

### 3.2 Which Agent Works in Which Phase

Put `●` if the agent is **active** in that phase, `○` if it is **on standby**, and leave blank if not used. Add one row per agent.

| Agent ID | Agent name | 1 Discover | 2 Plan | 3 Design | 4 Build | 5 Test | 6 Launch | 7 Grow to 500 | 8 Maintain |
|---|---|---|---|---|---|---|---|---|---|
| {{AGT-001}} | {{Name}} | | | | | | | | |

### 3.3 Budget and Billing per Phase

> Fill the **plan** before a phase starts and the **actual** when it ends. This stops surprise bills. Use one currency throughout: {{Currency, e.g. USD}}.

| Phase | Agents active (IDs) | Planned spend | Actual spend | Difference | Who watches the bill | Where we see the bill |
|---|---|---|---|---|---|---|
| 1 Discover | {{AGT-IDs}} | {{Amount}} | {{Amount}} | {{Amount}} | {{Name}} | {{Billing page link}} |
| 2 Plan | {{AGT-IDs}} | {{Amount}} | {{Amount}} | {{Amount}} | {{Name}} | {{Link}} |
| 3 Design | {{AGT-IDs}} | {{Amount}} | {{Amount}} | {{Amount}} | {{Name}} | {{Link}} |
| 4 Build | {{AGT-IDs}} | {{Amount}} | {{Amount}} | {{Amount}} | {{Name}} | {{Link}} |
| 5 Test | {{AGT-IDs}} | {{Amount}} | {{Amount}} | {{Amount}} | {{Name}} | {{Link}} |
| 6 Launch | {{AGT-IDs}} | {{Amount}} | {{Amount}} | {{Amount}} | {{Name}} | {{Link}} |
| 7 Grow to 500 (per month) | {{AGT-IDs}} | {{Amount}} | {{Amount}} | {{Amount}} | {{Name}} | {{Link}} |
| 8 Maintain (per month) | {{AGT-IDs}} | {{Amount}} | {{Amount}} | {{Amount}} | {{Name}} | {{Link}} |

**Rule of thumb:** if actual spend is more than 20% above plan in any phase, the owner writes one sentence of explanation in this table's row and tells the registry owner.

---

## 4. Agent Index (The Quick List) 🔴 Required

> One row per agent. Fill this table *after* you fill the cards, or fill it first and fill the cards next. Both are fine, but both must match.

| ID | Agent name | Type | One-line job | Autonomy (L0-L3) | Risk | Owner | Status | Card |
|---|---|---|---|---|---|---|---|---|
| {{AGT-001}} | {{Name}} | `Build-time` / `Product` | {{One short sentence}} | {{L0-L3}} | {{Low/Med/High/Critical}} | {{Name}} | {{Status}} | [Go to card](#agt-001) |

**How the columns work**
- **ID:** use `{{PREFIX}}-AGT-001`, then `002`, `003`... Never reuse an ID, even for a retired agent.
- **Type:** `Build-time` (helps make the product) or `Product` (customers use it or are affected).
- **Status:** `Idea` / `Planned` / `In Development` / `Testing` / `Live` / `Paused` / `Retired`.

---

## 5. Agent Card (Copy This Section for Every Agent) 🔴 Required

> **How to use:** Copy everything from `### AGT-001` down to the line `--- end of card ---`. Paste it below the last card. Change the ID, then fill every blank.
> Put a heading like `### AGT-001: Code Reviewer` so the index links work.

<a id="agt-001"></a>
### AGT-001: {{Agent name}}

#### A. Identity

| Field | Your answer |
|---|---|
| Agent ID | {{PREFIX-AGT-001}} |
| Agent name | {{Short, clear name. Example: "Code Reviewer"}} |
| Agent version | {{e.g. 1.0.0}} (see "Version rules" in Section 11) |
| Type | Choose one: `Build-time` / `Product` |
| Status | Choose one: `Idea` / `Planned` / `In Development` / `Testing` / `Live` / `Paused` / `Retired` |
| Owner (one named person) | {{Full name}} |
| Backup owner | {{Full name}} |
| How to reach the owner | {{Email or chat handle}} |
| Created on | {{YYYY-MM-DD}} |
| Created by | {{Person or "Claude Code"}} |

#### B. Purpose: What Is This Agent's Job?

| Field | Your answer |
|---|---|
| Job in ONE sentence | {{Example: "Reads every new piece of code and lists problems before a human reviews it."}} |
| Why does this agent exist? What problem does it solve? | {{Example: "Reviews take 2 hours per day; this cuts it to 30 minutes."}} |
| Who benefits? | {{Example: "The developers" or "Customers who ask support questions"}} |
| Who will use it or talk to it? | Choose all that apply: `Developers` / `Project manager` / `Testers` / `Customers` / `Other agents` / `Other: ____` |
| **Does:** the 3 to 5 things it SHOULD do | 1. {{Task}}<br>2. {{Task}}<br>3. {{Task}} |
| **Does NOT:** things it must NEVER do | 1. {{Example: "Never merge code by itself."}}<br>2. {{Example: "Never promise refunds."}}<br>3. {{Task}} |
| Out of scope (not its job, even if asked) | {{Example: "Legal advice, medical advice."}} |

#### C. Lifecycle: When Does It Work?

| Field | Your answer |
|---|---|
| Active phases (from Section 3) | Choose all that apply: `1 Discover` / `2 Plan` / `3 Design` / `4 Build` / `5 Test` / `6 Launch` / `7 Grow to 500` / `8 Maintain` |
| What starts it? (trigger) | Choose one: `A person asks` / `A schedule (e.g. every night)` / `A new event (e.g. new pull request, new customer message)` / `Another agent calls it` |
| Trigger details | {{Example: "Runs whenever a pull request is opened."}} |
| What does "finished" look like? | {{Example: "A review comment is posted listing issues, ranked by importance."}} |

#### D. Autonomy and Human Approval (How Much May It Do Alone?)

| Level | Name | Meaning in plain words |
|---|---|---|
| **L0** | Suggest only | The agent gives ideas. A human does every action. |
| **L1** | Act after approval | The agent prepares the action, a human clicks "OK", then it happens. |
| **L2** | Act, then report | The agent acts alone inside strict limits and tells a human afterwards. |
| **L3** | Fully autonomous (within limits) | The agent acts alone and only reports problems. Use only for low-risk jobs. |

| Field | Your answer |
|---|---|
| Autonomy level | Choose one: `L0` / `L1` / `L2` / `L3` |
| Why this level? | {{Example: "L1 because it posts to customers and mistakes are visible."}} |
| Actions that ALWAYS need human approval | {{Example: "Sending email to customers, deleting data, spending money, publishing code."}} |
| Who approves? | {{Name or role}} |
| How fast must approval happen? | {{Example: "Within 1 business day."}} |
| When must it hand over to a human (escalation)? | {{Example: "When the customer is angry, mentions legal action, asks for a refund, or when it is less than 80% sure."}} |
| Who receives the escalation? | {{Name or role, plus contact}} |

#### E. Tools and Access (What Can It Touch?)

> Rule: give the agent the **least** access it needs to do its job. If in doubt, choose `Read only`.

| Tool / app / MCP server | What it uses it for | Permission | Where the key is stored (never the key itself) |
|---|---|---|---|
| {{Example: GitHub}} | {{Read code, post comments}} | Choose one: `Read only` / `Read + write` / `Read + write + delete` / `Spend money` | {{Example: "Password manager, vault Project-Keys"}} |
| {{Tool 2}} | {{Use}} | {{Permission}} | {{Location}} |

| Field | Your answer |
|---|---|
| Can it connect to the internet? | Choose one: `No` / `Yes, only these sites: ____` / `Yes, any site` |
| Can it run code or commands? | Choose one: `No` / `Yes, in a safe sandbox only` / `Yes, on real systems` |
| Can it send messages to people outside the team? | Choose one: `No` / `Yes, only after approval` / `Yes, automatically` |
| Can it spend money? | Choose one: `No` / `Yes, up to {{amount}} per {{day/month}}` |
| Key rotation (how often keys are changed) | {{Example: "Every 90 days, by Sam."}} |

#### F. Data (What Information Does It See?)

| Field | Your answer |
|---|---|
| What data can it **read**? | {{Example: "Source code, public docs."}} |
| What data can it **write or change**? | {{Example: "Review comments only."}} |
| Does it see personal information (PII)? | Choose one: `No` / `Yes: ____ (names, emails, payments, health, children's data, other)` |
| Data sensitivity | Choose one: `Public` / `Internal` / `Confidential` / `Highly sensitive (payments, health, IDs)` |
| Where is the data stored? | {{Example: "Supabase, region EU."}} |
| Is data sent to an outside AI provider? | Choose one: `No` / `Yes: ____ (provider name)` |
| How long is data kept? | {{Example: "30 days, then deleted."}} |
| Is it used to train any AI model? | Choose one: `No` / `Yes` / `TBD (name, date)` |

#### G. Inputs and Outputs (What Goes In, What Comes Out?)

| Field | Your answer |
|---|---|
| Inputs (what it receives) | {{Example: "A pull request link and the project style guide."}} |
| Outputs (what it produces) | {{Example: "A review comment with a list of issues."}} |
| Output format | Choose one: `Text message` / `Document` / `Code` / `Table` / `Data file` / `Action in another app` / `Other: ____` |
| Where do outputs go? | {{Example: "Posted on the pull request."}} |
| Language(s) | {{Example: "English, Spanish."}} |
| Tone (for agents that write to people) | {{Example: "Friendly, short, no jargon."}} |

#### H. Brain and Instructions (Model and Prompt)

| Field | Your answer |
|---|---|
| Platform | Choose one: `Claude Code` / `Claude API` / `n8n` / `Zapier` / `Make` / `Other: ____` |
| Model name and version | {{Example: "Claude Sonnet 5.5"}} |
| Why this model? | {{Example: "Good balance of speed and cost."}} |
| Fallback if the model is down | {{Example: "Switch to Haiku, or pause and alert owner."}} |
| Instructions file (the prompt) | {{Link or file path}} |
| Instructions version | {{e.g. 1.3.0}} |
| Who may change the instructions? | {{Name or role}} |
| Extra knowledge it reads (docs, FAQs, files) | {{Links or paths}} |
| Memory (does it remember past chats?) | Choose one: `No` / `Yes, for this task only` / `Yes, long term: ____` |

**Prompt Library (the agent's written instructions and example prompts)**

> Keep the *full* instructions in the file linked above. Here, keep the short, most important parts so anyone can understand the agent at a glance. Never paste secrets.

| Item | Your answer |
|---|---|
| Role line (who the agent is told it is) | {{Example: "You are a careful code reviewer for a small web app."}} |
| Top 5 rules in the instructions | 1. {{Rule}}<br>2. {{Rule}}<br>3. {{Rule}}<br>4. {{Rule}}<br>5. {{Rule}} |
| "Good" example: a request and the answer you want | Request: {{Example}}<br>Ideal answer: {{Example}} |
| "Bad" example: a request and an answer you do NOT want | Request: {{Example}}<br>Bad answer: {{Example}}<br>Why it is bad: {{Reason}} |
| Words or topics it must refuse | {{Example: "Refund promises, legal advice."}} |
| What it says when it does not know | {{Example: "I'm not sure about that. Let me pass you to a person."}} |
| Prompt change history link | {{Link or "Same as card change log"}} |

#### I. Teamwork (Who Does It Work With?)

| Field | Your answer |
|---|---|
| Gets work from | {{Agent IDs / people / apps, or "A person"}} |
| Hands work to | {{Agent IDs / people / apps}} |
| What is handed over, and in what form? | {{Example: "A pass/fail report in a table."}} |
| If a hand-off fails, what happens? | {{Example: "Alert owner and retry once after 10 minutes."}} |

#### J. Quality and Testing (How Do We Know It Is Good?)

| Field | Your answer |
|---|---|
| How was it tested before going live? | Choose all that apply: `Tried by hand 10+ times` / `Test set with known right answers` / `Tried by someone other than its author` / `Tried with tricky or hostile input` / `Not tested yet` |
| Test evidence (link) | {{Link or path, or "TBD (name, date)"}} |
| Pass bar (minimum score to go live) | {{Example: "At least 90 of 100 test cases correct."}} |
| Last tested on | {{YYYY-MM-DD}} |
| Known weaknesses | {{Example: "Struggles with very long files."}} |
| How do people report a bad answer? | {{Example: "Thumbs-down button, then #agent-issues channel."}} |

#### K. Success Numbers (Targets Until 500 Customers)

> Pick a target you can measure. Write where you read the number from.

| Metric | What it means | Target | Where we read it | Check how often |
|---|---|---|---|---|
| **Task success rate** | % of jobs done correctly | {{e.g. 95%}} | {{Dashboard / log}} | {{Daily / weekly}} |
| **Error rate** | % of jobs that fail or are wrong | {{e.g. under 3%}} | {{Source}} | {{Frequency}} |
| **Cost per task** | Money spent per finished job | {{e.g. under $0.05}} | {{Billing page}} | {{Frequency}} |
| **Monthly cost** | Total spend per month | {{e.g. under $200}} | {{Billing page}} | {{Monthly}} |
| **Customer satisfaction (CSAT)** | Customer rating of the agent | {{e.g. 4.5 out of 5}} | {{Survey / thumbs}} | {{Weekly}} |
| **Escalation rate** | % of jobs a human must take over | {{e.g. under 15%}} | {{Source}} | {{Weekly}} |
| **Time saved / speed** | Hours saved or response time | {{e.g. replies in under 10 seconds}} | {{Source}} | {{Weekly}} |

> For build-time agents, "customer satisfaction" can mean **team satisfaction** (do the developers find it useful?).

**Red-light rule:** if any metric misses its target for {{e.g. 3 days in a row}}, the owner must {{e.g. lower autonomy by one level and investigate}}.

#### L. Risk and Safety (What Could Go Wrong?)

| Field | Your answer |
|---|---|
| Risk level | Choose one: `Low` (small, easy to undo) / `Medium` (annoying, fixable) / `High` (money, privacy, or customer trust at stake) / `Critical` (safety, legal, or large financial harm) |
| Who decided the risk level? | {{Name}} (do not rate your own agent alone when risk is High or Critical) |
| Top 3 things that could go wrong | 1. {{Example: "Posts a wrong answer to a customer."}}<br>2. {{Example: "Leaks a customer email."}}<br>3. {{Example: "Runs up a huge bill."}} |
| How we prevent each | 1. {{Prevention}}<br>2. {{Prevention}}<br>3. {{Prevention}} |
| 🛑 **Kill switch** (fastest way to turn it off) | {{Example: "Owner sets AGENT_ENABLED=false in settings. Takes 1 minute."}} |
| Who may press the kill switch? | {{Names}} |
| Fallback while it is off | {{Example: "A human answers support emails."}} |
| Does it tell customers they are talking to AI? | Choose one: `Yes` / `No, because it never talks to customers` |
| Spending limit (hard cap) | {{Amount per day/month, or "N/A (no spending)"}} |
| Logging: where are its actions recorded? | {{Link or path}} |

#### M. Lifecycle and Reviews (Keeping It Fresh)

| Field | Your answer |
|---|---|
| Review how often | Choose one: `Every month` / `Every 3 months` / `Every 6 months` (High/Critical risk: monthly or quarterly only) |
| Last review date | {{YYYY-MM-DD}} |
| Next review date | {{YYYY-MM-DD}} |
| Reviewed by | {{Name}} |
| Expires or must be re-approved on | {{YYYY-MM-DD}} |
| Retirement plan (how to switch off for good) | {{Example: "Remove keys, archive logs, mark Retired here."}} |
| Replacement agent (if any) | {{AGT-ID or "None"}} |

#### N. 🟡 Advanced / Strict Block (Optional)

> Fill this if the agent is customer-facing, handles personal data, or the risk is High or Critical. Otherwise write `N/A` with a reason on the first line and skip the rest.

| Field | Your answer |
|---|---|
| Skip this block? | `N/A (reason: ____)` or `Filling it` |
| Rules or laws that apply | Choose all that apply: `GDPR` / `CCPA` / `HIPAA` / `SOC 2` / `PCI-DSS` / `EU AI Act` / `Children's privacy (COPPA)` / `Other: ____` / `None` / `TBD (name, date)` |
| EU AI Act category (if relevant) | Choose one: `Minimal` / `Limited (must tell people it is AI)` / `High` / `Not relevant` / `TBD (name, date)` |
| Legal or privacy reviewer | {{Name}} |
| Privacy review done on | {{YYYY-MM-DD}} |
| Audit log location and retention | {{Link, and how long kept}} |
| Evaluation evidence (links to test reports) | {{Links}} |
| Red-team test (someone tried to break it) done on | {{YYYY-MM-DD or "Not done"}} |
| Customer data deletion process | {{How a customer can ask to delete their data}} |
| Incident contact (outside the team, if any) | {{Name, email}} |
| Terms of use / privacy policy updated for this agent? | Choose one: `Yes` / `No` / `Not needed` |

#### O. Card Change Log

| Date | Version | What changed | Who changed it | Approved by |
|---|---|---|---|---|
| {{YYYY-MM-DD}} | {{1.0.0}} | First version | {{Name}} | {{Name}} |

--- end of card ---

---

## 6. Hand-Off Map (Who Talks to Whom)

> Draw or list how work moves between agents and people. One line per hand-off. Shows gaps and loops at a glance.

| From | To | What is passed | Trigger | If it fails |
|---|---|---|---|---|
| {{Person / AGT-001}} | {{AGT-002 / Person}} | {{Example: "Approved spec document"}} | {{Example: "Spec marked Approved"}} | {{Example: "Notify owner"}} |

Optional simple picture (replace with your own):

```text
Idea -> [Planning Agent] -> [Coding Agent] -> [Code Review Agent] -> Human approves
     -> [QA Agent] -> [Release Agent] -> Live product -> [Support Agent] -> Human (if escalated)
```

---

## 7. Shared Rules for ALL Agents 🔴 Required

> These rules apply to every agent in this project. If a single card contradicts a shared rule, the **shared rule wins** unless the owner and registry owner both approve an exception (write it in the card).

| # | Rule | Your answer |
|---|---|---|
| 1 | No agent may reveal secrets (keys, passwords) in any output. | `Agreed` / `Change: ____` |
| 2 | No agent may delete or overwrite important data without human approval. | `Agreed` / `Change: ____` |
| 3 | Every agent has one named human owner. | `Agreed` / `Change: ____` |
| 4 | Every agent has a kill switch and a fallback. | `Agreed` / `Change: ____` |
| 5 | Customers must be told when they are talking to AI. | `Agreed` / `Change: ____` |
| 6 | Agents must say "I am not sure" instead of making things up. | `Agreed` / `Change: ____` |
| 7 | Agents never give legal, medical, or financial advice. | `Agreed` / `Change: ____` |
| 8 | Agents get the least access they need (start read-only). | `Agreed` / `Change: ____` |
| 9 | Every agent action is logged. | `Agreed` / `Change: ____` |
| 10 | New or changed agents must pass the checklist in Section 12 first. | `Agreed` / `Change: ____` |
| 11 | Project-specific rule: {{Your rule}} | {{Your answer}} |

**Global spending cap for all agents together:** {{Amount per month}}
**Who is told when the cap is 80% used?** {{Name and contact}}

### 7.1 Team Roles and Who Does What (RACI)

> **R**esponsible = does the work. **A**ccountable = final say, exactly **one** person per row. **C**onsulted = asked for advice before. **I**nformed = told after.
> Write a person's name in each cell that applies. Leave a cell empty if the person has no role in that activity. Every row needs exactly one **A**.

| Activity | Registry owner | Agent owner | Developer | QA / tester | Legal / privacy | Support lead | Project manager |
|---|---|---|---|---|---|---|---|
| Add a new agent to the registry | {{A}} | {{R}} | {{C}} | {{I}} | {{C}} | {{I}} | {{I}} |
| Change an agent's permissions or autonomy | {{A}} | {{R}} | {{C}} | {{C}} | {{C}} | {{I}} | {{I}} |
| Test an agent before it goes Live | {{I}} | {{A}} | {{C}} | {{R}} | {{I}} | {{I}} | {{I}} |
| Press the kill switch | {{I}} | {{A}} | {{R}} | {{I}} | {{I}} | {{I}} | {{I}} |
| Handle a customer-facing incident | {{I}} | {{R}} | {{C}} | {{I}} | {{C}} | {{R}} | {{A}} |
| Monthly or quarterly agent review | {{A}} | {{R}} | {{C}} | {{C}} | {{I}} | {{C}} | {{I}} |
| Retire an agent | {{A}} | {{R}} | {{C}} | {{I}} | {{C}} | {{I}} | {{I}} |

> The letters above are a starting suggestion. Replace each `{{letter}}` with the person's **name and letter**, for example `Sam (R)`. Change the columns if your team has different roles.

| Role | Person's name | Contact |
|---|---|---|
| Registry owner | {{Name}} | {{Contact}} |
| Developer lead | {{Name}} | {{Contact}} |
| QA / tester lead | {{Name}} | {{Contact}} |
| Legal / privacy contact | {{Name or "TBD (name, date)"}} | {{Contact}} |
| Support lead | {{Name}} | {{Contact}} |
| Project manager | {{Name}} | {{Contact}} |

---

## 8. Incident Playbook (If an Agent Misbehaves)

> Fill once per project. Keep it short enough to follow while stressed.

| Step | What to do | Who | Max time |
|---|---|---|---|
| 1. **Stop it** | Press the agent's kill switch (see its card, part L). | {{Name}} | {{e.g. 5 minutes}} |
| 2. **Tell people** | Message the owner and the registry owner. If customers are affected, tell {{Name}} who contacts them. | {{Name}} | {{e.g. 30 minutes}} |
| 3. **Protect data** | If personal data leaked, change keys and follow the privacy steps in Section 5 N. | {{Name}} | {{e.g. 1 hour}} |
| 4. **Switch to fallback** | Humans take over the job (see card, part L). | {{Name}} | {{e.g. 1 hour}} |
| 5. **Fix and test** | Find the cause, fix it, test again (card, part J). | {{Name}} | {{e.g. 2 days}} |
| 6. **Write it down** | Add a row to the table below and update the card change log. | {{Name}} | {{e.g. 2 days}} |

### 8.1 Incident Log

| Date | Agent ID | What happened | Customers affected | Root cause | Fix | Prevented next time by |
|---|---|---|---|---|---|---|
| {{YYYY-MM-DD}} | {{AGT-ID}} | {{What}} | {{Number or none}} | {{Cause}} | {{Fix}} | {{Prevention}} |

---

## 9. Road to 500 Customers: Agent Check-ins

> At each milestone, stop for 30 minutes and answer the questions. This keeps agents healthy while the customer count grows.

| Milestone | Customers reached (date) | Questions to answer | Decisions made | Who |
|---|---|---|---|---|
| **Launch day** | {{YYYY-MM-DD}} | Did every Live agent pass the readiness checklist? Are kill switches tested? | {{Decision}} | {{Name}} |
| **First 10** | {{YYYY-MM-DD}} | Are any customers confused by an agent? Any escalations? Read every conversation. | {{Decision}} | {{Name}} |
| **First 50** | {{YYYY-MM-DD}} | Are the success, error, and escalation numbers on target? Is cost per task as planned? | {{Decision}} | {{Name}} |
| **First 100** | {{YYYY-MM-DD}} | Can the support agent handle volume? Do we need to raise or lower any autonomy level? | {{Decision}} | {{Name}} |
| **First 250** | {{YYYY-MM-DD}} | Are monthly costs still under the cap at 2x growth? Are reviews up to date? | {{Decision}} | {{Name}} |
| **500 reached** | {{YYYY-MM-DD}} | What worked, what failed, which agents to keep, change, or retire? Plan for the next 5,000. | {{Decision}} | {{Name}} |

**Cost forecast at 500 customers (all agents):** {{Amount per month}}
**Biggest risk we see at 500 customers:** {{Sentence}}

---

## 10. Related Files (Links to Other Documents)

> Link every file an agent depends on. Write `N/A` or `TBD` rather than leaving a blank.

| Document | Link / path | Owner | Last updated |
|---|---|---|---|
| Agent instructions file (AGENTS.md or CLAUDE.md) | {{Path}} | {{Name}} | {{Date}} |
| Product Requirements (PRD) | {{Path}} | {{Name}} | {{Date}} |
| Technical specification / architecture | {{Path}} | {{Name}} | {{Date}} |
| Design files | {{Link}} | {{Name}} | {{Date}} |
| Test plan and test results | {{Path}} | {{Name}} | {{Date}} |
| Launch checklist | {{Path}} | {{Name}} | {{Date}} |
| Security and privacy notes | {{Path}} | {{Name}} | {{Date}} |
| Customer support playbook | {{Path}} | {{Name}} | {{Date}} |
| Cost and budget tracker | {{Path}} | {{Name}} | {{Date}} |
| Project roadmap / task board | {{Link}} | {{Name}} | {{Date}} |

---

## 11. Rules for Names, IDs, and Versions

- **Agent ID:** `{{PREFIX}}-AGT-###` (example: `ACME-AGT-004`). IDs never change and are never reused.
- **Version numbers:** `MAJOR.MINOR.PATCH` (example: `1.2.0`).
  - **PATCH** (1.2.**1**): small fix, same behavior. Example: fix a typo in the instructions.
  - **MINOR** (1.**3**.0): new ability or tool added, nothing removed.
  - **MAJOR** (**2**.0.0): big change (new model, new permissions, new autonomy level). **Needs approval and a new test.**
- **Any change to permissions, autonomy level, model, or data access = MAJOR change** and must be approved by the registry owner.
- **Statuses move in this order:** `Idea` → `Planned` → `In Development` → `Testing` → `Live` → (`Paused` ↔ `Live`) → `Retired`.

---

## 12. Readiness Checklists

### 12.1 Before ANY agent goes `Live`
- [ ] Card is 100% filled (no `{{...}}`).
- [ ] Owner and backup owner are named and have agreed.
- [ ] Autonomy level is chosen and approved.
- [ ] Permissions are the minimum needed.
- [ ] Kill switch has been **tested once** (date: {{YYYY-MM-DD}}).
- [ ] Fallback plan works without the agent.
- [ ] It passed its test pass bar (card, part J).
- [ ] Logs are on and someone knows where to read them.
- [ ] Spending cap is set.
- [ ] Added to the Agent Index (Section 4) and phase table (Section 3.2).

### 12.2 Before the LAUNCH phase (Phase 6)
- [ ] All Live agents pass 12.1.
- [ ] Customer-facing agents tell people they are AI.
- [ ] Customers can reach a human.
- [ ] Privacy policy and terms mention the agents (if personal data is used).
- [ ] Incident Playbook (Section 8) was read by everyone on call.
- [ ] Monitoring shows success, error, cost, and escalation numbers.
- [ ] Global spending cap (Section 7) is set.

### 12.3 Before RETIRING an agent
- [ ] Replacement or manual process is ready.
- [ ] Keys and access removed.
- [ ] Data kept or deleted according to the card.
- [ ] Status set to `Retired` and the ID is kept in the index.
- [ ] Change Log updated.

---

## 13. Open Questions: All TBD Items in One Place

> Every time you write `TBD` anywhere in this file, add a row here. **No open TBD may remain when you pass the Launch gate.**

| # | Where (section / agent ID) | What we need to find out | Who will answer | Due date | Done? |
|---|---|---|---|---|---|
| 1 | {{Section or AGT-ID}} | {{Question}} | {{Name}} | {{YYYY-MM-DD}} | `[ ]` |

---

## 14. Registry Change Log

| Date | Registry version | What changed (agents added, changed, retired) | Who | Approved by |
|---|---|---|---|---|
| {{YYYY-MM-DD}} | {{1.0.0}} | Created registry | {{Name}} | {{Name}} |

---

## 15. Registry Health Score (0 to 100)

> Score yourself on the first day of each month and before each phase gate. Answer each question honestly with **Yes** (full points) or **No** (0 points). If a question does not apply, mark `N/A` and give those points to "Yes".

| # | Question | Points | Yes / No / N/A |
|---|---|---|---|
| 1 | Does every agent have a named owner and a backup owner? | 10 | {{Yes/No/N/A}} |
| 2 | Is every agent card free of `{{...}}` blanks? | 10 | {{Yes/No/N/A}} |
| 3 | Does every agent have an autonomy level and a reason for it? | 8 | {{Yes/No/N/A}} |
| 4 | Has every kill switch been tested in the last 90 days? | 12 | {{Yes/No/N/A}} |
| 5 | Is every agent's last review date within its review cadence? | 12 | {{Yes/No/N/A}} |
| 6 | Does every agent meet its test pass bar, with evidence linked? | 10 | {{Yes/No/N/A}} |
| 7 | Are all permissions the minimum needed (nothing extra)? | 8 | {{Yes/No/N/A}} |
| 8 | Are all spending caps set, and is spend within 20% of plan? | 8 | {{Yes/No/N/A}} |
| 9 | Are all High and Critical agents rated by someone other than their owner? | 6 | {{Yes/No/N/A}} |
| 10 | Is the TBD list (Section 13) empty or on schedule? | 6 | {{Yes/No/N/A}} |
| 11 | Does the Agent Index (Section 4) match the cards exactly? | 5 | {{Yes/No/N/A}} |
| 12 | Is the Incident Log up to date (or confirmed "no incidents")? | 5 | {{Yes/No/N/A}} |
| | **Total** | **100** | **{{Your total}}** |

| Score | What it means | What to do |
|---|---|---|
| **90-100** | Healthy | Keep going. Review again next month. |
| **70-89** | Needs attention | Fix every "No" within 2 weeks. |
| **50-69** | At risk | Pause new agents. Fix before the next phase gate. |
| **Below 50** | Not safe | Stop launching. Registry owner leads a clean-up now. |

### 15.1 Score History

| Date | Score | Biggest problem found | Fixed by |
|---|---|---|---|
| {{YYYY-MM-DD}} | {{Score}} | {{Problem}} | {{Date}} |

---

## Appendix A. Worked Example (Copy the Style, Not the Content)

> This is a **filled-in sample** so you can see what a good answer looks like. Delete it from your real project.

### Example Index Row

| ID | Agent name | Type | One-line job | Autonomy | Risk | Owner | Status |
|---|---|---|---|---|---|---|---|
| BAKE-AGT-001 | Code Reviewer | Build-time | Checks every new piece of code and lists problems | L1 | Low | Sam Lee | Live |
| BAKE-AGT-002 | Support Helper | Product | Answers customers' how-to questions | L2 | High | Priya Rao | Testing |

### Example Card (shortened)

**BAKE-AGT-002: Support Helper**

| Field | Example answer |
|---|---|
| Job in ONE sentence | Answers customers' how-to questions using our help articles. |
| Does | 1. Finds the right help article. 2. Explains the steps in simple words. 3. Offers to connect a human. |
| Does NOT | 1. Never promises refunds. 2. Never asks for card numbers. 3. Never gives legal advice. |
| Active phases | `6 Launch`, `7 Grow to 500` |
| Autonomy | `L2` (replies alone inside limits, reports daily summary) |
| Always needs approval | Anything involving refunds or account deletion |
| Escalates when | Customer is angry, mentions a lawyer, or the agent is less than 80% sure |
| Tools | Help-center search (read only), ticket system (read + write notes) |
| Sees personal info? | Yes: customer name and email. Sensitivity: Confidential |
| Platform / model | Claude API / Claude Sonnet 5.5 |
| Success targets | Success 92%, error under 4%, cost per chat under $0.04, CSAT 4.5/5, escalation under 15% |
| Risk | High: a wrong answer could upset a customer or leak an email |
| Kill switch | Owner turns off "Support Helper" in the settings page (1 minute); chats route to the support inbox |
| Review | Every month; last 2026-10-01, next 2026-11-01 |

---

## Appendix B. Choose-From Lists (Copy These Values)

| List | Allowed values |
|---|---|
| Agent type | `Build-time`, `Product` |
| Status | `Idea`, `Planned`, `In Development`, `Testing`, `Live`, `Paused`, `Retired` |
| Autonomy | `L0 Suggest only`, `L1 Act after approval`, `L2 Act then report`, `L3 Fully autonomous (within limits)` |
| Risk level | `Low`, `Medium`, `High`, `Critical` |
| Permission | `Read only`, `Read + write`, `Read + write + delete`, `Spend money` |
| Data sensitivity | `Public`, `Internal`, `Confidential`, `Highly sensitive` |
| Phases | `1 Discover`, `2 Plan`, `3 Design`, `4 Build`, `5 Test`, `6 Launch`, `7 Grow to 500`, `8 Maintain/Retire` |
| Trigger | `A person asks`, `A schedule`, `A new event`, `Another agent calls it` |
| Review cadence | `Every month`, `Every 3 months`, `Every 6 months` |

## Appendix C. Common Mistakes (Avoid These)

| Mistake | Why it hurts | Do this instead |
|---|---|---|
| Owner is "the team" | Nobody feels responsible | Name one person |
| Giving full access "to make it easy" | One mistake can do big damage | Start read-only, add access later |
| No kill switch | You cannot stop a runaway agent | Write the exact steps and test them |
| Vague job ("helps with stuff") | Agent drifts outside its job | One clear sentence plus a Does NOT list |
| Never updating the registry | Looks official but is wrong | Review on the date in part M |
| Writing keys in this file | Anyone who reads it can steal them | Write only where keys are stored |
| Skipping testing because "it seems fine" | Problems appear in front of customers | Use a pass bar and write down the result |
| Guessing an answer | Wrong facts spread | Write `TBD` + person + date |

---

## Appendix D. Full Sample Project: "BakeBox"

> A short, completed registry for a made-up product so you can see how all the sections fit together. Everything here is invented. Delete this appendix from your real project.

### D.1 Project Snapshot (Sections 0 and 1)

| Field | Sample answer |
|---|---|
| Project name / prefix | BakeBox / BAKE |
| Registry owner | Sam Lee (sam@example.com) |
| Product | A web app that lets small bakeries take online orders |
| Customers | Bakery owners with 1 to 10 staff |
| Goal | 500 active customers by 2027-09-30 ("active" = placed or received at least 1 order in the last 30 days) |
| Launch date | 2027-02-15 |
| Platforms | Claude Code, Claude API, n8n |
| Registry version / date | 1.2.0 / 2026-10-17 |

### D.2 Agent Index (Section 4)

| ID | Agent name | Type | One-line job | Autonomy | Risk | Owner | Status |
|---|---|---|---|---|---|---|---|
| BAKE-AGT-001 | Spec Writer | Build-time | Turns interview notes into a clear list of requirements | L0 | Low | Sam Lee | Live |
| BAKE-AGT-002 | Code Reviewer | Build-time | Checks every new piece of code and lists problems | L1 | Low | Dev Patel | Live |
| BAKE-AGT-003 | Test Buddy | Build-time | Runs tests nightly and reports what broke | L2 | Low | Mia Chen | Testing |
| BAKE-AGT-004 | Support Helper | Product | Answers bakery owners' how-to questions | L2 | High | Priya Rao | Testing |
| BAKE-AGT-005 | Cost Watcher | Build-time | Checks AI spend daily and warns when it gets high | L2 | Medium | Sam Lee | Planned |

### D.3 Who Works in Which Phase (Section 3.2)

| Agent | 1 Discover | 2 Plan | 3 Design | 4 Build | 5 Test | 6 Launch | 7 Grow to 500 | 8 Maintain |
|---|---|---|---|---|---|---|---|---|
| AGT-001 Spec Writer | ● | ● | ○ | | | | | |
| AGT-002 Code Reviewer | | | | ● | ● | ○ | ○ | ● |
| AGT-003 Test Buddy | | | | ○ | ● | ● | ● | ● |
| AGT-004 Support Helper | | | | | ○ | ● | ● | ● |
| AGT-005 Cost Watcher | | | | | | ● | ● | ● |

### D.4 Hand-Offs (Section 6)

| From | To | What is passed | Trigger | If it fails |
|---|---|---|---|---|
| Sam Lee | AGT-001 | Interview notes | Notes saved in /discovery | Sam reads notes manually |
| AGT-001 | Sam Lee | Draft requirements | Draft finished | Sam is emailed |
| Developer | AGT-002 | Pull request link | PR opened | PR waits for human review |
| AGT-003 | Mia Chen | Pass/fail report | Every night at 2 am | Mia is messaged and runs tests by hand |
| AGT-004 | Priya Rao | Escalated customer chat | Customer upset or agent unsure | Chat goes to the support inbox |
| AGT-005 | Sam Lee | Spend alert | Spend over 80% of monthly cap | Sam checks the billing page daily |

### D.5 Budget Plan (Section 3.3, excerpt, USD)

| Phase | Agents | Planned | Actual | Difference | Watches the bill |
|---|---|---|---|---|---|
| 4 Build | AGT-002 | 120 | 135 | +15 | Sam Lee |
| 5 Test | AGT-002, AGT-003 | 150 | 140 | -10 | Sam Lee |
| 6 Launch | AGT-003, AGT-004, AGT-005 | 250 | TBD | TBD | Sam Lee |
| 7 Grow to 500 (per month) | AGT-003, AGT-004, AGT-005 | 600 | TBD | TBD | Sam Lee |

### D.6 Support Helper Card (shortened to the fields that matter most)

| Part | Sample answer |
|---|---|
| **A. Identity** | BAKE-AGT-004, version 0.9.0, Product, Testing, owner Priya Rao, backup Dev Patel |
| **B. Purpose** | Answers how-to questions using our help articles. Does NOT: promise refunds, ask for card numbers, give legal advice. |
| **C. Lifecycle** | Phases 6 and 7. Triggered when a customer sends a chat message. |
| **D. Autonomy** | L2: replies alone and sends Priya a daily summary. Refunds and account deletion always need Priya's approval. Escalates if customer is angry, mentions a lawyer, or the agent is under 80% sure. |
| **E. Tools** | Help-center search (read only); ticket system (read + write notes). No internet, no code running, cannot spend money. Keys stored in the password manager, vault "BakeBox-Keys", rotated every 90 days. |
| **F. Data** | Sees customer name and email. Confidential. Stored in Supabase (EU region). Kept 30 days. Sent to Anthropic's API. Not used for training (per provider terms, checked 2026-10-02). |
| **H. Brain** | Claude API, Claude Sonnet 5.5, fallback Claude Haiku 5.5. Instructions in /agents/support-helper.md v0.9.1. Memory: this chat only. |
| **J. Testing** | 100-question test set; pass bar 90; last score 93 on 2026-10-10. Tried with hostile input by Mia. |
| **K. Targets** | Success 92%, errors under 4%, cost per chat under $0.04, CSAT 4.5/5, escalation under 15%, first reply in under 10 seconds. |
| **L. Risk** | High. Worst cases: wrong answer upsets a customer; leaks an email; high bill. Kill switch: Priya turns off "Support Helper" in the admin page (1 minute); chats go to the support inbox. Spending cap: $300/month. Tells customers it is AI: Yes. |
| **M. Reviews** | Monthly. Last 2026-10-10, next 2026-11-10, re-approval 2027-02-15. |
| **N. Strict block** | GDPR applies; EU AI Act "Limited" (must tell people it is AI); privacy review by Legal on 2026-09-28; red-team test done 2026-10-05; customers can request deletion at settings > privacy. |

### D.7 Road to 500 (Section 9, partly filled)

| Milestone | Date | Decision |
|---|---|---|
| Launch day | 2027-02-15 | Planned: all Live agents pass the checklist; kill switches tested on 2027-02-10 |
| First 10 | TBD | Sam reads every Support Helper chat |
| First 50 | TBD | Compare targets; decide if Support Helper can move to L3 (answer: only if escalation under 10% for 30 days) |
| 500 reached | TBD | Plan the next phase |

### D.8 Open Questions (Section 13)

| # | Where | Question | Who | Due | Done? |
|---|---|---|---|---|---|
| 1 | AGT-005, part E | Which billing dashboard API will Cost Watcher read? | Sam Lee | 2026-11-01 | `[ ]` |
| 2 | AGT-004, part N | Does BakeBox need a Data Protection Officer? | Legal contact | 2026-11-15 | `[ ]` |

### D.9 Health Score Example (Section 15)

| Question group | Result |
|---|---|
| Owners and backups named | Yes (10/10) |
| Cards without blanks | No: AGT-005 unfinished (0/10) |
| Kill switches tested in 90 days | Yes (12/12) |
| Reviews on time | Yes (12/12) |
| Everything else | 55 of 56 points |
| **Total** | **89 / 100: "Needs attention." Finish AGT-005's card within 2 weeks.** |
