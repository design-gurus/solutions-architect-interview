# Solutions Architect Interview vs. System Design Interview

A software engineering system design interview asks whether the candidate can build a system. A solutions architect (SA) design interview asks whether the candidate can choose the right system for one customer. Most system design practice carries over, but the SA round adds the customer's constraints, a cost estimate, and a migration plan.

## Eight differences

| Area | Software engineering system design | Solutions architect design |
|---|---|---|
| Main question | Can you build a system that scales? | Can you choose the right system for this customer? |
| Starting point | Usually a new system | The customer's existing systems and contracts |
| Building blocks | Custom components, such as a sharded database | Managed services that the cloud provider runs |
| Cost | Rarely discussed | An estimate with the main cost drivers |
| Compliance | Sometimes mentioned | Often decides where data is stored and who can read it |
| Change | Design the target system | Plan the move from today's system, with a rollback |
| Audience | Another engineer | The customer's engineers and executives |
| Other rounds in the loop | Coding and behavioral | Customer role-play, presentation, and behavioral |

## The same question, answered twice

**The question:** "A university's registration website fails at peak times. Fix it."

**A software engineering answer** estimates the request rate, adds servers behind a load balancer, and replaces the single database with a sharded one. A sharded database splits data across several machines.

**An SA answer** asks about the customer first and learns three facts:

1. Student records stay in a system in the university's own data center, and its contract has three more years.
2. That records system accepts about 50 writes a second.
3. The IT team has 6 people who know Windows servers and SQL databases.

These facts change the design. Every registration must reach the records system, so a sharded database adds work without raising the 50 writes a second limit. The SA design keeps the records system and puts a managed queue in front of it. A custom queue cluster would be a poor choice for a team of 6 with no experience running one.

The difference shows in one sentence. The engineer says "a queue, for scale." The SA says "a queue, because the records system accepts 50 writes a second."

## What carries over

- Load estimates with simple arithmetic.
- Named trade-offs for each decision.
- Failure planning.
- A deep dive on the riskiest part.

Both candidates start with the same request rate. What changes is the reason behind each choice.

## What to add

| Addition | What to practice |
|---|---|
| Discovery | Five questions about goals, current systems, and team skills before drawing |
| Managed services | The managed form of each component, and when not to use it |
| Cost | A monthly estimate with drivers and assumptions |
| Migration | The order of the move, the outage limit, and the rollback |
| Seasonal load | Capacity for real traffic, not for the peak all year |

If registration traffic lasts about two weeks a term, capacity added only for those weeks costs far less than servers sized for the peak all year.

## Converting existing practice

An engineer who has already practiced system design questions can convert each one in 15 minutes. Take a finished design and answer four questions about it.

1. Who is the customer, and what do they run today?
2. Which components can be replaced with managed services?
3. What does it cost each month, and what are the two largest drivers?
4. How does the customer move to it from the current system?

## Which role fits

The SA role suits engineers who prefer many customers and designs to one codebase. An engineer who wants to write production code most days may prefer the forward deployed engineer role. The free [Forward Deployed Engineer Interview](https://github.com/design-gurus/forward-deployed-engineer-interview) guide covers that loop.

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-solutions-architect-vs-system-design-interview) teaches the SA additions through ten case studies: discovery questions, managed service choices, cost estimates, and migration plans.
- [Grokking the System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-solutions-architect-vs-system-design-interview) covers the estimates, components, and trade-offs that both rounds use.
- [Solutions architect interview vs. system design interview](https://www.designgurus.io/answers/detail/solutions-architect-interview-vs-system-design-interview-what-is-the-difference?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-solutions-architect-vs-system-design-interview) is the full written comparison.
