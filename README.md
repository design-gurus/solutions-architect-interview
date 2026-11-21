# Solutions Architect Interview

> The free, open companion to **Grokking the Solutions Architect Interview** by [DesignGurus.io](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme), created by Arslan Ahmad.

[![GitHub stars](https://img.shields.io/github/stars/design-gurus/solutions-architect-interview?style=social)](https://github.com/design-gurus/solutions-architect-interview/stargazers)
[![Last commit](https://img.shields.io/github/last-commit/design-gurus/solutions-architect-interview)](https://github.com/design-gurus/solutions-architect-interview/commits/main)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

A solutions architect (SA) is a technical expert who designs a customer's solution on a vendor's platform and stays involved until it runs in production. The interview loop for this role measures three things that a software engineer loop rarely measures:

1. **A customer in the room.** An interviewer plays a customer, and the candidate must ask questions before proposing anything.
2. **A business constraint.** A budget, a deadline, a compliance rule, or the skills of the customer's team decides the design.
3. **A recommendation that must be defended.** The candidate presents a solution to a senior audience and answers hard questions about it.

This repository is a free guide to every round, the reported loops at five companies, and the reference sheets that support them. Company processes change, so every company detail here is commonly reported, not official. This guide is not affiliated with any company it names.

## Start here

| Your situation | Read this first |
|---|---|
| You have a recruiter call and want the whole loop on one page | [The interview loop](rounds/interview-loop.md) |
| You are a software engineer and know the system design round | [Solutions architect vs. system design interview](cheat-sheets/solutions-architect-vs-system-design-interview.md) |
| You have a presentation round in two weeks | [The presentation round](rounds/presentation.md) |
| You are interviewing at AWS | [AWS solutions architect interview](companies/aws.md) |
| You want questions to practice with today | [Question bank](cheat-sheets/question-bank.md) |

## The loop at a glance

| Stage | Format | What is evaluated |
|---|---|---|
| Recruiter screen | A call of about 30 minutes | Background, motivation, and why this company |
| Technical screen | One interviewer, many short questions | Breadth across compute, storage, networking, security, and databases |
| Architecture design | Whiteboard or shared drawing | Trade-offs, cost, and a design that survives changed requirements |
| Customer role-play | The interviewer plays a customer | Discovery questions and objection handling |
| Presentation | 20 to 60 minutes, depending on the company | Structure, a clear recommendation, and answers to hard questions |
| Behavioral | One to three interviews | Past decisions, conflict, and customer trust |

## Rounds

| Page | What it covers |
|---|---|
| [The interview loop](rounds/interview-loop.md) | Every stage in order, and how loops differ by company type |
| [Architecture design](rounds/architecture-design.md) | The design round, with a worked example that includes cost |
| [Customer discovery role-play](rounds/customer-discovery-role-play.md) | Four kinds of question and a four-step answer to objections |
| [Presentation](rounds/presentation.md) | Reported formats, an eight-slide plan, and four types of hard question |
| [Behavioral](rounds/behavioral.md) | The stories an SA needs, including a lost deal |
| [Technical screen](rounds/technical-screen.md) | Six breadth areas and the three-layer answer |

## Companies

| Page | What it covers |
|---|---|
| [Comparison table](companies/README.md) | Five reported loops side by side |
| [AWS](companies/aws.md) | Leadership Principles, two technical rounds, and the presentation |
| [Microsoft](companies/microsoft.md) | The cloud solution architect role, which works after the sale |
| [Google Cloud](companies/google-cloud.md) | The customer engineer role, which supports the sale |
| [Databricks](companies/databricks.md) | The eight published steps, including a coding assignment |
| [Snowflake](companies/snowflake.md) | A take-home task and a presentation with a demonstration |

## Cheat sheets

| Page | What it covers |
|---|---|
| [Question bank](cheat-sheets/question-bank.md) | 50 questions grouped by round |
| [Design round framework](cheat-sheets/design-round-framework.md) | Ten steps with a minute budget for a 45-minute round |
| [AWS vs. Azure vs. GCP services](cheat-sheets/aws-vs-azure-vs-gcp-services.md) | A service translation table across eight categories |
| [Cost estimation](cheat-sheets/cost-estimation.md) | Five cost drivers and a worked monthly estimate |
| [Migration and disaster recovery](cheat-sheets/migration-and-disaster-recovery.md) | Seven migration strategies and four recovery tiers |
| [Solutions architect vs. system design interview](cheat-sheets/solutions-architect-vs-system-design-interview.md) | What carries over and what changes |
| [Four-week plan](cheat-sheets/four-week-plan.md) | A weekly schedule with a finish condition for each week |
| [Common mistakes](cheat-sheets/common-mistakes.md) | Ten mistakes by round, each with its correction |

## FAQ

### What is asked in a solutions architect interview?

The loop asks five kinds of question: architecture design, rapid cloud fundamentals, customer discovery and objections, presentation follow-ups, and behavioral stories. Each kind tests one part of the job. The [question bank](cheat-sheets/question-bank.md) lists 50 examples.

### Is there coding in a solutions architect interview?

Most cloud provider loops are reported without an algorithm round. Data platform companies are the exception: Databricks lists a coding assignment on data frame operations in Python or Scala. The work is practical data handling, not puzzles. See the [technical screen](rounds/technical-screen.md) page.

### How is it different from a system design interview?

A system design interview asks whether the candidate can build a system that scales. An SA design round asks whether the candidate can choose the right system for one customer, with a cost estimate and a migration plan. The [comparison page](cheat-sheets/solutions-architect-vs-system-design-interview.md) covers eight differences.

### What is the solutions architect presentation round?

The candidate presents a technical solution to interviewers who act as the audience, then answers their questions. Reported lengths range from 20 minutes plus 10 minutes of questions to a full hour. The [presentation page](rounds/presentation.md) gives a slide plan.

### Do I need a cloud certification to pass?

No reported loop requires one. A certification covers service facts, which help in the technical screen, but the loop spends most of its time on judgment, discovery, and communication. Preparation time is usually better spent on design cases and a rehearsed presentation.

### How long does it take to prepare?

Four weeks at 8 to 10 hours a week is a reasonable plan for an engineer who already knows one cloud platform. The [four-week plan](cheat-sheets/four-week-plan.md) divides that time across the rounds.

## Go deeper

This repository gives the shape of each round. The course teaches the skills behind them with complete worked answers.

- **[Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme)** covers every round in this guide: ten architecture case studies, cost estimation, written role-play transcripts that contrast a weak and a strong answer, a full presentation with feedback, and company guides.
- **[Grokking the System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme)** teaches the core designs and trade-offs that the architecture round builds on.
- **[Grokking Modern Behavioral Interview](https://www.designgurus.io/course/grokking-behavioral-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme)** shows how to structure stories with evidence.
- Read the round-by-round answer: [What is the solutions architect interview process like?](https://www.designgurus.io/answers/detail/what-is-the-solutions-architect-interview-process-like-round-by-round?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme)

Related free guides: [Grokking System Design](https://github.com/design-gurus/grokking-system-design), [Forward Deployed Engineer Interview](https://github.com/design-gurus/forward-deployed-engineer-interview), and [Amazon Leadership Principles](https://github.com/design-gurus/amazon-leadership-principles).

## Contributing

Corrections and new questions are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

The content is licensed under [CC BY 4.0](LICENSE). [NOTICE.md](NOTICE.md) explains what the license covers and how to give credit.
