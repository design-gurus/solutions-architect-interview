# Cloud Cost Estimation

A cloud bill is the sum of a few cost drivers, and each driver is a quantity multiplied by a unit price. Solutions architect (SA) candidates are expected to estimate cost in the design round, because customers always ask. The interviewer scores the shape of the calculation and the stated assumptions, not the accuracy of the prices.

**Every price on this page is a round, illustrative unit cost.** None is a quoted price from any provider. Say the same in an interview.

## The five cost drivers

| Driver | Quantity | Note |
|---|---|---|
| Compute hours | Servers x hours running | A month has about 730 hours (8,760 / 12) |
| Storage | Gigabytes stored for one month (GB-month) | Fast disks cost more per GB-month than object storage |
| Requests | Millions of requests | Applies to some services, such as object storage reads |
| Data transfer out | Gigabytes sent to the internet (egress) | Data sent into the cloud is usually free |
| Managed service charges | Hours or usage | A managed database, load balancer, or queue has its own price |

## Five steps to a monthly estimate

1. List the parts of the design.
2. Choose a size for each part.
3. Count the quantities for one month.
4. Multiply each quantity by its unit price.
5. Apply purchase options, then state the assumptions.

## A worked example

An online store handles 600 orders in its busiest normal hour. One server handles 100 orders an hour, so the store needs 6 servers.

| Part | Quantity | Illustrative unit cost | Monthly cost |
|---|---|---:|---:|
| Web servers | 6 x 730 = 4,380 hours | 0.10 an hour | 438 |
| Managed database, primary and standby | 2 x 730 = 1,460 hours | 0.40 an hour | 584 |
| Object storage | 2,000 GB-months | 0.02 | 40 |
| Data transfer out | 5,000 GB | 0.08 | 400 |
| Load balancer | 1 | 25 a month | 25 |
| **Total** | | | **1,487** |

The database and data transfer are 66 percent of the bill. A candidate who says "the main drivers are the database and egress" has given the most useful sentence in the estimate.

## Paying for a peak

The store's sale week needs 6 times normal capacity, which is 36 servers.

| Option | Calculation | Server-hours a year |
|---|---|---:|
| Fixed capacity for the peak | 36 x 8,760 | 315,360 |
| Capacity that grows for the sale week | 6 x 8,760 + 30 x 168 | 57,600 |

Elastic capacity uses about 18 percent of the server-hours. This is the arithmetic behind most cloud cost arguments, and it only holds when the peak is short.

## Purchase options

| Option | How it works | Fits |
|---|---|---|
| On-demand | Paid by the hour with no commitment, at the highest hourly price | Capacity used part of the time |
| Commitment | A discount in return for a promise to pay for one to three years | Capacity that runs all the time |
| Spot | Spare capacity at a large discount, which the provider can take back at short notice | Work that can stop and restart |

**The break-even rule.** With a 30 percent commitment discount, the commitment costs 0.70 of the on-demand price for every hour. Capacity used less than 70 percent of the time is cheaper on-demand. A server that runs 16 hours a day runs 67 percent of the hours, so it should stay on-demand.

Never place a checkout service on spot capacity. An interrupted checkout loses orders.

## Total cost of ownership

Total cost of ownership (TCO) is everything a customer pays to run its systems over a period, not only the provider's bill. For a data center, it includes hardware spread over its useful life, the lease, power, cooling, licenses, and staff. A fair comparison meets the same goal in both columns. If the data center failed during the sale, compare the cloud with a data center sized for the sale.

## Assumptions to state aloud

- The prices are illustrative.
- One server handles 100 orders an hour.
- There is one sale week a year.
- The same team runs both options.
- Traffic growth is not included.

## Two follow-up questions

- **"What if traffic doubles?"** Compute and transfer roughly double, and the database may need a larger size.
- **"Why not commit to all the servers?"** Only the 6 that run all year pass the 70 percent break-even.

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-cost-estimation) teaches cost estimation as a skill and includes a case study on reducing a cloud bill by 40 percent.
- [Advanced System Design Fundamentals](https://www.designgurus.io/course/advanced-system-design-fundamentals?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-cost-estimation) covers capacity and cost estimation for engineers.
- Cost is step 8 of the [design round framework](design-round-framework.md).
