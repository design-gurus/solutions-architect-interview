# Common Mistakes in the Solutions Architect Interview

Most candidates who fail a solutions architect (SA) loop know enough technology to pass it. They fail because they answer as engineers when the loop is measuring an advisor. The ten mistakes below are grouped by round, and each has a correction that can be practiced.

## Architecture design

| Mistake | Why it costs points | Correction |
|---|---|---|
| 1. Drawing in the first minute | The design answers a problem nobody has confirmed | Spend about a quarter of the round on the goal, the limits, and the current state |
| 2. Designing for maximum scale | The customer's team cannot operate the result | Size for the real numbers, and prefer managed services |
| 3. Leaving out cost | Customers always ask, so interviewers do too | Give a monthly estimate, the two largest drivers, and the assumptions |
| 4. Describing only the target system | Most customers already run something | State the order of the move, the outage limit, and the rollback |

**An example of mistake 2.** A candidate proposes a sharded database for a system in which every write must still reach a records system that accepts 50 writes a second. The new database adds work and does not raise the limit.

## Customer role-play

| Mistake | Why it costs points | Correction |
|---|---|---|
| 5. Proposing before asking | It shows weak discovery, which is the skill the round measures | Ask at least five questions first |
| 6. Arguing with an objection | The customer stops listening | Acknowledge, clarify, answer with evidence, and confirm |
| 7. Promising what cannot be delivered | A broken promise costs more than a refusal | Say no, and offer the part that can be delivered by the date |

**An example of mistake 6.**

> **Customer:** "We are worried about being locked in to one vendor."
>
> **Weak:** "Customers never want to leave us."
>
> **Strong:** "That is a reasonable concern. Which part worries you most: the data, the application code, or the contract? For the data, here is what leaving would take and what it would cost."

The weak answer denies a real cost. The strong answer measures it.

## Presentation

| Mistake | Why it costs points | Correction |
|---|---|---|
| 8. A late recommendation | The audience waits 15 minutes to learn the proposal | Put the recommendation on the first slide |
| 9. Running over time | A talk that runs 7 minutes long leaves 3 of the 10 minutes for questions | Plan 18 minutes of speech for a 20-minute slot |

A related problem is the service tour, in which a list of services replaces the reasons for the design. Every slide should support the recommendation, and a slide that does not should become a backup slide.

## Behavioral and technical screen

| Mistake | Why it costs points | Correction |
|---|---|---|
| 10. Guessing a fact | Customers act on what an SA tells them | Say "I do not know", then reason from what you do know |

The same habit appears in behavioral answers as a story told with "we" throughout. The interviewer cannot score the team. Name your own decision, your own mistake, and your own number.

## Mistakes specific to engineers changing roles

Software engineers moving into the role make three further mistakes.

1. **Preparing only the design round.** The design round is about one third of the loop. The role-play and the presentation are where engineers have the least practice.
2. **Having no customer stories.** An internal team that depends on your service is a customer. So is a partner company. Prepare stories about them, and say plainly that they were internal.
3. **Treating the deal as someone else's work.** Hiring managers ask about deals won and lost. Learn how the sales process works at the target company, and ask whether the role is before the sale or after it.

## A check before each round

| Round | Ask yourself |
|---|---|
| Design | Did I write the customer's goal and limits where the interviewer can see them? |
| Role-play | Have I asked five questions? |
| Presentation | Could the audience repeat my recommendation after two minutes? |
| Behavioral | Does this story contain my decision and a number? |
| Screen | Is this answer under two minutes? |

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-common-mistakes) contrasts a weak and a strong answer for every round, with written transcripts and rubrics.
- [What is the solutions architect interview process like?](https://www.designgurus.io/answers/detail/what-is-the-solutions-architect-interview-process-like-round-by-round?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-common-mistakes) describes what each round evaluates.
- Plan the corrections with the [four-week plan](four-week-plan.md).
