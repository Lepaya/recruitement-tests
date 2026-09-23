# DevOps Engineer Assignment

Welcome to our DevOps assignment.

We are interested not only in whether you can build a working system, but in **how you make engineering decisions when AI agents are capable of doing a large part of the implementation for you**.

You are free to use agentic coding tools, and equally free not to. If you do, the goal is to demonstrate that you can **direct, constrain, review, and correct an AI agent** — and to set up session trace capture before you write any code. See *Working With AI Agents* below. That record is a graded deliverable.

**You do not need an AWS account for this assignment, and we do not expect a live deployment.** We evaluate the design, the code, the Terraform, and the pipeline — not whether something is running in a cloud account right now. See *What Counts as Proof* below.

---

## The Task

Design and build a small AWS-based system that synchronizes sensitive data from an S3 CSV file into a database.

### Functional requirements

- A CSV file in an S3 bucket containing randomly generated email addresses. A script that generates it is fine.
- A service that reads the CSV and synchronizes its contents with a database.
- When the CSV changes, the database should eventually mirror the new contents — including rows that were removed.
- The synchronization should run approximately once per hour.
- The workload may be a scheduled Lambda, a container, a cron job, or another reasonable AWS-native solution.
- Infrastructure is provisioned with Terraform.
- Two environments, `staging` and `production`. Show how they are separated. Building one out fully and expressing the other as configuration is enough.
- A GitHub Actions pipeline that runs on every pull request and, at minimum, formats, validates, plans, and tests. Add whatever other gates you believe belong there. An apply/deploy stage should exist, but it may be gated or stubbed since it cannot run without an account.
- Someone cloning the repository should be able to run your tests, your Terraform plan, and the sync locally by following the README.

You are free to choose:

- AWS services
- programming language
- database
- compute platform
- Terraform structure
- CI/CD implementation
- synchronization strategy

There is intentionally no single "correct" architecture. **Explain why you chose yours.**

### Sensitive data

Although the assignment uses randomly generated email addresses, **treat them as production PII throughout the system** and apply the security best practices you would apply to a real customer dataset. A system that is functionally correct but unnecessarily exposes sensitive data is not considered secure. We look at this closely.

### What counts as proof

Since nothing runs in a real account, show us that it would. Any combination of the following is acceptable:

- `terraform validate` passing and a committed `terraform plan` output
- The sync running locally against a local database and a local or mocked S3 (a plain file, moto, LocalStack, or similar)
- Unit or integration tests that exercise the sync logic, including the removal case
- A short written walkthrough of what `apply` would create and what a deploy would do

You do not need all of these. Pick what proves your design, and say what it does not prove.

---

## Working With AI Agents

The finished system shows what your agent can do. The record of how you built it shows what **you** can do. Both ship in the same repo.

**If you use an agent, confirm trace capture works before you start.** Not every tool keeps full history reliably, and a lost session cannot be graded.

Your submission includes two extra deliverables:

**1. Your full session traces, unedited — in a `traces/` directory.**
Do not clean them up. Dead ends, bad prompts, and corrections are the interesting part. **We read them.** Any format works — Claude Code has `/export`, Cursor has *Export Chat*, aider writes `.aider.chat.history.md` on its own. If your tool has no export, copy the sessions out by hand and say so. One exception to "unedited": if a real secret — or any of the generated data — leaked into a trace, redact that value, mark the redaction, and change nothing else. Also commit any instruction files your agent worked under (`AGENTS.md`, `CLAUDE.md`, `.cursorrules`, or similar) in their final, untidied state.

**2. `NOTES.md` — your retrospective.**
Short — one page, two at most. Cover four things:

- **How you decomposed the work** — what you handed to the agent, in what order, and what you kept for yourself.
- **Where you let it run, where you took the wheel** — and why the line sat where it did.
- **One moment you rejected or corrected the agent's output** — what it proposed, why it was wrong, and what you did instead. Point us to it in the traces.
- **Not done, and why** — what you cut, and what you would do with one more day. "I would add X because Y, and it costs Z" is worth more than a half-built X.

If you worked without an agent, that is allowed. Skip the traces, say so in `NOTES.md`, and answer the last point.

Your traces are read by us for evaluating the assignment and not used for anything else. Start fresh sessions for this assignment so your logs contain nothing personal.

---

## Scope: What Is Enough

This assignment can absorb a week. Do not give it one. **It is designed to fit in 4 to 6 focused hours.** If you are far past that, stop building.

That is not enough time to build everything well — that is the point. Infrastructure, security, and plumbing all compete for the same hours, with PII in the middle. We want to see which one you fund first.

- **Build the core path completely.** CSV in, database synchronized, data locked down — end to end in one environment before anything else. Security is not a later pass.
- **Cut consciously.** Monitoring, alerting, dashboards, multi-region, exhaustive tests — skip them and say so in `NOTES.md`.

We do not award points for extra services. **A polished addition on top of a weak core counts against you**, because it tells us where your attention went.

We do not grade language choice, framework fashion, line counts, or how much of the code the agent wrote.

---

## FAQ

**Will Lepaya provide an AWS account?**
No. We do not expect a live, running solution on AWS. The goal is to demonstrate the design, the Terraform, the CI/CD pipeline, and the environment setup. Mocks, local execution, `terraform plan`, or a written explanation of what would happen are all acceptable. See *What Counts as Proof*.

**Will Lepaya provide AI API credits or tokens?**
No. You may use your own tools, licences, and models, or work without an AI agent altogether. If you do use an agent, the traces are required.

**Is LocalStack (or similar) acceptable?**
Yes. It is optional, not expected.

**Do I need a real remote Terraform state backend?**
No. Describe how you would configure it and why. You do not need to create it.

**Do I need to ask before making an assumption?**
For minor ambiguities, make a reasonable assumption and write it down. **That is the job.** For anything that genuinely blocks you, email devops@lepaya.com.

---

## How to Deliver

1. Work in a **private GitHub repository** from the first commit.
2. **Commit as you go.** Small commits, honest messages. The history is part of the submission — a single squashed commit deletes your best exhibit.
3. When you stop building, invite the GitHub user **`lepaya-code-reviewer`** as a collaborator.
4. Email devops@lepaya.com to tell us it is ready.

Good luck!
