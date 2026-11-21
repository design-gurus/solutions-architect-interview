# The Technical Screen

The technical screen checks breadth before the full loop. One interviewer asks many short questions across cloud fundamentals, and the candidate has one to two minutes for each. The screen measures how many topics the candidate can answer correctly, so a long answer to one question reduces the score on the others.

## Reported formats

| Company | Commonly reported format |
|---|---|
| Databricks | A 1-hour technical screen, according to the company's own interview guide |
| AWS | A phone screen with one interviewer, mostly technical, with one or two behavioral questions at the end |
| Google Cloud | Broad technical questions as one part of a loop of 4 to 5 interviews |

Some companies send a timed online assessment before any conversation. Reports about the AWS version disagree on its content, so ask the recruiter whether the role uses one.

## The six breadth areas

| Area | What the questions ask | Example |
|---|---|---|
| Compute | Which kind of server to run, and how capacity grows | "When would you choose containers over virtual machines?" |
| Storage | Where files, disks, and backups live, and what each costs | "What is the difference between object storage and block storage?" |
| Networking | How traffic reaches a private application | "How does a private server download updates?" |
| Security | Who is responsible for what, and who may access data | "What is the shared responsibility model?" |
| Databases | Which kind of database fits, and how copies protect it | "What is the difference between a read replica and a standby?" |
| Data and AI | Where analytics data is stored, and how a model uses company documents | "What is the difference between a data warehouse and a data lake?" |

## The three-layer answer

A strong screen answer has three layers and takes about 90 seconds.

**Question:** "When would you put a queue between two services?"

- **Short answer, about 15 seconds:** "When the receiver must not slow down or lose the sender's requests. An example is orders that arrive faster than the payment step can process them."
- **Mechanism, about 45 seconds:** The sender writes each message to the queue and continues. The receiver reads at its own rate and deletes each message after it finishes, so a message whose processing fails is read again.
- **Trade-off, about 30 seconds:** Work finishes later than with a direct call. A message can also arrive twice, so the receiver must be idempotent, which means that repeating an operation has the same effect as doing it once.

The interviewer decides the depth. If they move on after the short answer, stop there. In a 45-minute screen, 3 minutes a topic covers 15 topics, and 4 minutes covers about 11.

## When you do not know

Say that you do not know, then reason from what you do know, and say that it is reasoning. Customers act on what an SA tells them, so a confident wrong number is worse than an honest gap.

- **Weak:** "The limit is 1,000."
- **Strong:** "I do not remember the number. It depends on the memory of the database server, so I would check the documentation for the size we chose and load test before launch."

## Coding and data tasks

Most cloud provider loops are reported without an algorithm round. Data platform roles are different. Databricks lists a coding assignment that covers problem solving, feature implementation, and data frame operations in Python or Scala. A data frame is a table held in memory with named columns, which code can filter, join, and group. Prepare joins, grouping, date filters, and window functions in both SQL and data frame code.

## How to prepare

1. Write one three-layer answer for five questions in each area, 30 answers in total.
2. Say each answer aloud with a timer and keep it near 90 seconds.
3. Learn the service names on the target platform with the [service translation table](../cheat-sheets/aws-vs-azure-vs-gcp-services.md).

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=rounds-technical-screen) includes rapid questions on networking, security, and databases, plus an SQL and data frame exercise for data platform roles.
- [Grokking System Design Fundamentals](https://www.designgurus.io/course/grokking-system-design-fundamentals?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=rounds-technical-screen) explains the building blocks behind most screen questions.
- More practice questions are in the [question bank](../cheat-sheets/question-bank.md).
