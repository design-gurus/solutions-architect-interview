# Design Round Framework

A solutions architect (SA) design answer has ten steps in four phases. The framework spends about a quarter of the round on the customer before the first box is drawn. The minutes below are a budget for a 45-minute round, and they should be scaled for a longer one.

## The ten steps

| Phase | Step | Minutes | The question it answers |
|---|---|---:|---|
| Understand | 1. Business goal | 3 | What does success mean to this customer? |
| Understand | 2. Requirements and constraints | 5 | Which numbers and limits shape the design? |
| Understand | 3. Current state | 3 | What runs today, and who operates it? |
| Design | 4. High-level design | 8 | What are the main parts, and why these? |
| Design | 5. Deep dive on the riskiest part | 8 | Which part is most likely to make the project fail? |
| Qualities | 6. Failure and recovery | 4 | What happens when a part fails? |
| Qualities | 7. Security | 3 | Who can reach the data, and how is it protected? |
| Qualities | 8. Cost | 4 | What does it cost each month, and what drives that? |
| Qualities | 9. Migration or rollout | 3 | In what order does the customer move, and how do they go back? |
| Close | 10. Trade-offs and next steps | 4 | What does the design give up, and what happens next? |

The Understand phase takes 11 of 45 minutes. Candidates from software engineering usually spend 2.

## What to ask in the first 11 minutes

| Step | Questions |
|---|---|
| Business goal | "What must be true in a year for this project to count as a success?" "Is the date fixed?" |
| Requirements | "How many requests arrive in the busiest hour?" "Which rules apply to this data?" |
| Constraints | "What is the budget, and who approves it?" "What does the team already know how to operate?" |
| Current state | "What runs today, and where?" "What failed last time, and why?" |

Write each answer where the interviewer can see it. Later steps refer back to these numbers.

## Rules for the Design phase

1. **Let the numbers decide the shape.** If 556 fans arrive each second but only 24,000 orders can succeed, the design needs a waiting line, not 28 times the checkout capacity.
2. **Prefer managed services.** A managed service is one that the cloud provider runs, patches, and scales. The customer's team must operate the design after the architect leaves.
3. **Choose the deep dive by risk.** Go deeper on the part that would break the customer's main goal, not on the part you know best.
4. **Name the rejected option.** One sentence on what you did not choose, and why, shows more judgment than more detail on what you did choose.

## One decision for each quality

Each quality step takes a few minutes and one or two decisions.

| Step | A sufficient answer |
|---|---|
| Failure and recovery | "If the primary database fails, the service switches to the standby. I assume up to 2 minutes, and the load test measures the real time." |
| Security | "Card numbers go only to the payment provider. A web application firewall limits requests from each address." |
| Cost | "Thirty containers for 2 hours a sale, and the standby database all year. The database is the main driver." |
| Migration or rollout | "A load test at twice the expected arrivals three weeks before, then a smaller event on the new system first." |

## When the interviewer interrupts the plan

| The interviewer says | Response |
|---|---|
| "Skip the questions and start designing." | Agree, then state your assumptions aloud and ask for corrections |
| "The requirement has changed." | Recompute the affected number before changing the design |
| "You have five minutes left." | Give each remaining step one sentence, then the main trade-off and the next step |
| "Why not use a different service?" | Agree with any correct part, then give the reason tied to this customer |

## A closing statement template

> "The design meets the goal of [goal] by [main decision]. It gives up [trade-off], which is acceptable because [customer fact]. The largest remaining risk is [risk], and the next step is [test or decision] by [date]."

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-design-round-framework) teaches this method in full and applies it to ten case studies with changing requirements.
- [Grokking the System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-design-round-framework) covers the components used in steps 4 and 5.
- See the method applied in the [architecture design round page](../rounds/architecture-design.md).
