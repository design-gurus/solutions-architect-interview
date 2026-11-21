# Migration and Disaster Recovery

Two question types appear in most solutions architect (SA) design rounds: "move this to the cloud" and "make this survive a failure". Each has a standard vocabulary. A migration answer chooses one of seven strategies for each application, and a recovery answer chooses one of four tiers from two numbers the customer provides.

## Seven migration strategies

| Strategy | What it means | Choose it when |
|---|---|---|
| Retire | Switch it off and move nothing | Nobody uses the application |
| Retain | Keep it in the data center for now | A contract, a license, or a dependency blocks the move |
| Rehost | Move it to a cloud virtual machine unchanged | The deadline is close and the application works as it is |
| Relocate | Move the whole virtualization platform to the cloud | Many virtual machines must move with no changes at all |
| Repurchase | Replace it with a product bought as a service | A standard product does the same job |
| Replatform | Move it with a small change, such as a managed database | One change removes most of the operating work |
| Refactor | Rewrite it to use cloud services fully | The application limits the business, and there is time |

The strategies rise in effort from top to bottom. A strong answer assigns a strategy to each application, with a reason, and does not apply one strategy to everything.

## A worked migration

A travel company runs four applications on 14 servers. Its data center contract ends in 9 months.

| Application | Strategy | Reason |
|---|---|---|
| Reporting server | Retire | Discovery found that nobody has opened it in a year |
| Booking website | Rehost | It works today, and 9 months is too short for a rewrite |
| Booking database, 2 TB | Replatform | A managed database removes backups and patching from a small team |
| Email system | Repurchase | A standard service replaces it |

The plan copies the database while the website keeps running, switches over inside a 30-minute outage limit, and keeps a rollback path for 14 days. The follow-up "Why not move everything in one weekend?" has a numeric answer: copying 2 TB over the free part of the network link takes about 9 hours.

## Two recovery numbers

- **Recovery time objective (RTO):** the longest time the business accepts for a system to be unavailable after a failure.
- **Recovery point objective (RPO):** the largest amount of recent data, measured in time, that the business accepts losing.

Ask for both numbers before choosing a design. An RTO of 12 hours and an RTO of 5 minutes lead to different architectures and very different costs.

## Four recovery tiers

| Tier | What runs in the second region | Typical RTO | Relative cost |
|---|---|---|---|
| Backup and restore | Only copies of the data and backups | Hours | Lowest |
| Pilot light | A live copy of the data, with no application running | Tens of minutes | Low |
| Warm standby | A live copy of the data and a small running application | Minutes | Medium |
| Multi-site active-active | A full system that serves traffic all the time | Near zero | Highest |

Pilot light and warm standby both copy the data continuously, so their RPO is the same. They differ in RTO, because pilot light must start the application before it can serve traffic.

## Choosing a tier

Choose the lowest-cost tier that meets both numbers.

| The customer says | Tier |
|---|---|
| "Payroll runs twice a month. We can wait 12 hours." | Backup and restore |
| "We can be down for 30 minutes, and we can lose 5 minutes of data." | Pilot light |
| "We can be down for 5 minutes." | Warm standby |
| "We lose revenue every second we are down." | Multi-site active-active |

Then state what the choice rejects: "Active-active would run a second full system all year to save hours that this business does not need."

## Three points that candidates miss

1. **A recovery plan that has never been tested is an assumption.** Include a recovery test at least once a year, and measure the real RTO.
2. **Recovery covers more than the database.** DNS, secrets, and access rules must also exist in the second region.
3. **Going back is part of the plan.** State how the system returns to the primary region after the failure ends.

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-migration-and-disaster-recovery) includes full case studies on migrating a web application and on multi-region disaster recovery, each with cost figures for the options.
- [Advanced System Design Fundamentals](https://www.designgurus.io/course/advanced-system-design-fundamentals?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-migration-and-disaster-recovery) teaches zero-downtime migration mechanics, including dual writes and backfills.
- Practice both question types from the [question bank](question-bank.md).
