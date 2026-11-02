# AGENTS-PROMPTS.md: copy-and-paste prompts for your AI agent

> **How to use this:** Copy a prompt, replace anything in `[square brackets]`, and paste it to your agent. Every prompt assumes the agent has read `AGENTS.md`. Start every new session with **Prompt 0**.

---

## 0. Start of every session
```
Read AGENTS.md fully. Then, in 5 lines or fewer: (1) tell me what this project is,
(2) tell me which phase we are in, (3) list every [FILL] or UNKNOWN you found that
could block today's work. Do not start any task until I answer.
```

## 1. Check the file for gaps
```
Summarize AGENTS.md in 5 lines. Then list everything you would have to guess to do
a good job. Do not guess. Just list the questions, most important first.
```

## 2. Idea and requirements
```
Help me fill Sections 4.1 to 4.4 of AGENTS.md. Ask me one question at a time, in
simple words. After each answer, show the filled text and ask if it is right.
```
```
Review my Version 1 must-haves in Section 4.2. Tell me which ones are too big,
unclear, or not needed for a first launch. Propose a smaller list. Do not edit the file.
```

## 3. Design
```
Based on Sections 4 and 5, propose 3 simple screens for the main user journey.
For each screen describe: purpose, what is on it, and its loading, empty and error states.
Wait for my approval before building anything.
```

## 4. Plan a feature
```
Task: [describe the feature using "A user can ..."].
Before writing code: list the files you will change, the tests you will add, and
anything that needs my approval under Section 2. Keep the plan under 15 lines.
Wait for my "go".
```

## 5. Build a feature
```
Go ahead with the approved plan. Work on a new branch named [branch name].
Only change the files in the plan. Run the commands from Section 7 after each step.
If anything is unclear or risky, stop and ask me.
```

## 6. Fix a bug
```
Bug: [what happens] instead of [what should happen]. Steps to repeat it: [steps].
First reproduce it and show me proof. Then explain the cause in plain words.
Then fix it with the smallest change and add a test that would have caught it.
```

## 7. Review a change
```
Review the changes on this branch like a careful senior reviewer. Check against
the Definition of Done (Section 8.3) and Security rules (Section 9). Report:
(1) must-fix problems, (2) risks, (3) nice-to-have improvements. Do not edit anything.
```

## 8. Test and quality
```
Run all checks from Section 7. Test the critical paths in Section 8.1 and tell me
for each one: pass or fail, with evidence. List anything you could not test and why.
```

## 9. Security and privacy check
```
Check this project against Section 9. List: where we collect or store personal data,
anything stored in plain text, any secret that could leak, any dependency with a
known problem. Do not change anything; give me a short fix list ordered by risk.
```

## 10. Prepare for launch
```
Walk through the Go/No-Go checklist in Section 10.1 one item at a time. For each
item say: done, not done, or unknown, with evidence. At the end tell me clearly:
GO or NO-GO, and what blocks us. Do not deploy anything.
```

## 11. Write the release notes and launch post
```
Draft release notes and a short launch announcement for [product]. Use the tone
in Section 5. Use only facts from AGENTS.md and the changelog. Do not invent
features, numbers or customer quotes. Do not post anything.
```

## 12. Onboarding and support
```
Look at this list of customer questions: [paste]. Group them into themes,
draft FAQ answers for the top 5, and suggest one change to the product that
would stop each question from being asked. Do not send anything to customers.
```

## 13. Weekly growth review
```
Run the weekly loop in Section 13.3. Here is this week's real data: [paste numbers
and feedback]. Fill the table in 13.2, name the top 3 problems, and suggest at most
3 changes with the reason for each. Use only the data I pasted. If a number is missing,
say so instead of estimating.
```

## 14. Money check
```
Open the Money tracker in Section 13.4. Here are this month's real bills: [paste].
Update the table, tell me if any item is above 80% of its cap, and suggest where
we can cut cost without hurting customers.
```

## 15. After something goes wrong
```
Something went wrong: [describe]. Follow Section 11. First tell me how serious it is
(S1 to S4). Then give me the safest next step. Do not delete anything or change
production. When it is over, help me write down what happened and how to prevent it.
```

## 16. Keep AGENTS.md healthy
```
Compare AGENTS.md with what is really in the project (commands, folders, tools).
List anything out of date or missing. Propose edits as a list; do not edit the
file until I approve.
```
