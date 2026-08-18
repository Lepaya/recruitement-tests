# DevOps Engineer Assignment

Welcome to our DevOps assignment.

We are interested not only in whether you can build a working system, but in **how you make engineering decisions when AI agents are capable of doing a large part of the implementation for you**.

You are free to use agentic coding tools. The goal is not to demonstrate that you can avoid AI. The goal is to demonstrate that you can **direct, constrain, review, and correct an AI agent.**

**Before you write any code, set up session trace capture** — see *Show Your Work* below. That record is a graded deliverable.

---

## The Task

Build a small AWS-based system that synchronizes sensitive data from an S3 CSV file into a database.

### Functional requirements

- Create a CSV file in an S3 bucket containing randomly generated email addresses.
- Create a service that reads the CSV and synchronizes its contents with a database.
- When the CSV changes, the database should eventually mirror the new contents — including rows that were removed.
- The synchronization should run approximately once per hour.
- The workload may be implemented as a scheduled Lambda, container, cron job, or another reasonable AWS-native solution.
- Use Terraform for infrastructure provisioning.
- Use at least two environments:
  - `staging`
  - `production`
- Create a GitHub CI/CD pipeline capable of deploying the infrastructure and application.
- The system must be reproducible by someone cloning the repository.


You are free to choose:

- AWS services
- programming language
- database
- compute platform
- Terraform structure
- CI/CD implementation
- synchronization strategy

There is intentionally no single "correct" architecture.

**Explain why you chose yours.**

---

## The Important Part: Assume the Data Is Sensitive

Although the assignment uses randomly generated email addresses, **treat them as production PII throughout the system.**
A system that is functionally correct but unnecessarily exposes sensitive data is not considered secure.

---

## The Other Important Part: Show Your Work

The finished system shows what your agent can do. The record of how you built it shows what **you** can do. Both ship in the same repo.

**Confirm trace capture works before you start.** Not every tool keeps full history reliably, and a lost session cannot be graded.

Your submission includes three extra deliverables:

**1. Your full session traces, unedited — in a `traces/` directory.**
Do not clean them up. Dead ends, bad prompts, and corrections are the interesting part. **We read them.** Any format works — Claude Code has `/export`, Cursor has *Export Chat*, aider writes `.aider.chat.history.md` on its own. If your tool has no export, copy the sessions out by hand and say so. One exception to "unedited": if a real secret — or any of the generated data — leaked into a trace, redact that value, mark the redaction, and change nothing else.

**2. `AGENTS.md` — the instructions your agent worked under.**
Commit its final state, untidied — your commit history already shows how it evolved. If you steered through prompts alone and never wrote one, say so — your traces then carry that weight.

**3. `AGENT-NOTES.md` — your retrospective.**
Short — one page, two at most. Cover 3 things:

- **How you decomposed the work** — what you handed to the agent, in what order, and what you kept for yourself.
- **Where you let it run, where you took the wheel** — and why the line sat where it did.
- **What you would do differently** — next time, or with one more day.

If you genuinely worked without an agent, that is allowed. Say so in `AGENT-NOTES.md`. 

Your traces are read by the us for evaluating assignment and not used for nothing else. Start fresh sessions for this assignment so your logs contain nothing personal.

---

## Scope: What Is Enough

This assignment can absorb a week. Do not give it one. **It is designed to fit in roughly half focused day.** If you are far past that, stop building.

That is not enough time to build everything well — that is the point. Infrastructure, security, and plumbing all compete for the same hours, with PII in the middle. We want to see which one you fund first.

- **Build the core path completely.** CSV in, database synchronized, data locked down — end to end in one environment before anything else. Security is not a later pass.
- **Cut consciously.** Monitoring, alerting, dashboards, multi-region, exhaustive tests — skip them and say so.
- **Write up the rest.** Add a *"Not done, and why"* section to your README. "I would add X because Y, and it costs Z" is worth more than a half-built X.

We do not award points for extra services. **A polished addition on top of a weak core counts against you**, because it tells us where your attention went.

We do not grade language choice, framework fashion, line counts, or how much of the code the agent wrote.

---

## How to Deliver

1. Work in a **private GitHub repository** from the first commit.
2. **Commit as you go.** Small commits, honest messages. The history is part of the submission — a single squashed commit deletes your best exhibit.
3. When you stop building, invite the GitHub user **`realsby`** as a collaborator.
4. Email us to tell us it is ready.

For minor ambiguities, make a reasonable assumption and write it down. **That is the job.**

Good luck!
