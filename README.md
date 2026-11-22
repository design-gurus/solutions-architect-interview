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

## Course lessons to start with

- [How Solutions Architect Interview Loops Test the Job](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/how-solutions-architect-interview-loops-test-the-job?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): how each round maps to a part of the work, in Grokking the Solutions Architect Interview
- [A Method for Architecture Design Answers](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/a-method-for-architecture-design-answers?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): the ordered steps for the design round, in Grokking the Solutions Architect Interview
- [Estimating Cloud Cost](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/estimating-cloud-cost?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): how to put a monthly figure on a design, in Grokking the Solutions Architect Interview
- [Interview Question: Migrate a Web Application to the Cloud](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/interview-question-migrate-a-web-application-to-the-cloud?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): a complete answer to the most common design question, in Grokking the Solutions Architect Interview
- [Running a Discovery Conversation](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/running-a-discovery-conversation?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): the questions that open a customer role-play, in Grokking the Solutions Architect Interview
- [Handling Technical Objections](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/handling-technical-objections?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): how to answer a customer who doubts the design, in Grokking the Solutions Architect Interview
- [Structuring a 20-Minute Technical Presentation](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/structuring-a-20minute-technical-presentation?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): the slide order for the presentation round, in Grokking the Solutions Architect Interview
- [Building a Story Bank](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/building-a-story-bank?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): how to prepare stories for the behavioral round, in Grokking the Solutions Architect Interview
- [What Technical Screens Ask](https://www.designgurus.io/course-play/grokking-the-solutions-architect-interview/doc/what-technical-screens-ask?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): the topics and depth of the first technical call, in Grokking the Solutions Architect Interview
- [The Other Envelope: Cost Estimation](https://www.designgurus.io/course-play/advanced-system-design-fundamentals/doc/the-other-envelope-cost-estimation?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): cost estimation as a second back-of-the-envelope calculation, in Advanced System Design Fundamentals

## Free reading on DesignGurus.io

- Free article: [How to gather and prioritize requirements in system design interviews](https://www.designgurus.io/blog/how-to-gather-requirements-in-system-design-interviews?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): the opening steps of the architecture design round.
- Free article: [System design trade-offs: how to reason about them like a senior engineer](https://www.designgurus.io/blog/complex-system-design-tradeoffs?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): how to explain a choice between two options.
- Free article: [High availability in system design: 15 strategies for always-on systems](https://www.designgurus.io/blog/high-availability-system-design-basics?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): the redundancy and failover methods behind disaster recovery answers.
- Free article: [Amazon's 16 Leadership Principles: behavioral interview guide](https://www.designgurus.io/blog/amazon-leadership-principles-behavioral-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): required reading for the AWS loop.
- Free answer: [Cloud-based system design interview questions for AWS, Azure, and GCP](https://www.designgurus.io/answers/detail/cloud-based-system-design-interview-questions?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): design questions for practice.
- Free answer: [Forward deployed engineer vs. solutions architect vs. software engineer](https://www.designgurus.io/answers/detail/forward-deployed-engineer-vs-solutions-architect-vs-software-engineer-what-is-the-difference?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): how the three roles and their interviews differ.
- Free answer: [Databricks interview process, round by round](https://www.designgurus.io/answers/detail/what-is-the-databricks-interview-process-like-round-by-round?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme): the general engineering process at one of the companies in this guide.

## Go deeper

This repository gives the shape of each round. The course teaches the skills behind them with complete worked answers.

- **[Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme)** covers every round in this guide: ten architecture case studies, cost estimation, written role-play transcripts that contrast a weak and a strong answer, a full presentation with feedback, and company guides.
- **[Grokking the System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme)** teaches the core designs and trade-offs that the architecture round builds on.
- **[Grokking Modern Behavioral Interview](https://www.designgurus.io/course/grokking-behavioral-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme)** shows how to structure stories with evidence.
- Read the round-by-round answer: [What is the solutions architect interview process like?](https://www.designgurus.io/answers/detail/what-is-the-solutions-architect-interview-process-like-round-by-round?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=readme)

Related free guides: [Grokking System Design](https://github.com/design-gurus/grokking-system-design), [Forward Deployed Engineer Interview](https://github.com/design-gurus/forward-deployed-engineer-interview), and [Amazon Leadership Principles](https://github.com/design-gurus/amazon-leadership-principles).

For the system design round, see [Grokking System Design](https://github.com/design-gurus/grokking-system-design), the free companion guide with 30 patterns, 59 question walkthroughs, and 35 cheat sheets.

## More free guides

Every guide below is free, follows the same short-page format, and comes from DesignGurus.io.

- **Core guides:** [Grokking System Design](https://github.com/design-gurus/grokking-system-design), [Grokking Coding Interview](https://github.com/design-gurus/grokking-coding-interview), [Grokking AI System Design](https://github.com/design-gurus/grokking-ai-system-design), [Design Patterns](https://github.com/design-gurus/design-patterns), [Best System Design Resources](https://github.com/design-gurus/best-system-design-resources), [Best System Design Courses](https://github.com/design-gurus/best-system-design-courses)
- **By interview round:** [System Design Numbers](https://github.com/design-gurus/system-design-numbers), [API Design Interview](https://github.com/design-gurus/api-design-interview), [Frontend System Design Interview](https://github.com/design-gurus/frontend-system-design-interview), [Mobile System Design Interview](https://github.com/design-gurus/mobile-system-design-interview), [Microservices Interview Questions](https://github.com/design-gurus/microservices-interview-questions), [Concurrency Interview](https://github.com/design-gurus/concurrency-interview)
- **By role:** [DevOps and SRE Interview](https://github.com/design-gurus/devops-sre-interview), [Data Engineering Interview](https://github.com/design-gurus/data-engineering-interview), [Forward Deployed Engineer Interview](https://github.com/design-gurus/forward-deployed-engineer-interview)
- **Seniority and behavioral:** [Staff Engineer Interview](https://github.com/design-gurus/staff-engineer-interview), [Engineering Manager Interview](https://github.com/design-gurus/engineering-manager-interview), [Amazon Leadership Principles](https://github.com/design-gurus/amazon-leadership-principles), [Software Engineer Levels](https://github.com/design-gurus/software-engineer-levels)
- **By company:** [Google Interview Guide](https://github.com/design-gurus/google-interview-guide), [Meta Interview Guide](https://github.com/design-gurus/meta-interview-guide), [Amazon Interview Guide](https://github.com/design-gurus/amazon-interview-guide), [Microsoft Interview Guide](https://github.com/design-gurus/microsoft-interview-guide), [Apple Interview Guide](https://github.com/design-gurus/apple-interview-guide), [Netflix Interview Guide](https://github.com/design-gurus/netflix-interview-guide), [OpenAI Interview Guide](https://github.com/design-gurus/openai-interview-guide)

## Contributing

Corrections and new questions are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

The content is licensed under [CC BY 4.0](LICENSE). [NOTICE.md](NOTICE.md) explains what the license covers and how to give credit.
