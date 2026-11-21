# The Architecture Design Round

In the architecture design round, the candidate designs a system for one customer's need and defends each trade-off while the interviewer changes the requirements. The round resembles a system design interview, but the customer's existing systems, budget, deadline, and team skills decide the answer. A design that ignores them fails, even when it scales.

## What the interviewer scores

| Signal | Weak answer | Strong answer |
|---|---|---|
| Discovery | Starts drawing in the first minute | Spends about a quarter of the round on goals, limits, and the current state |
| Fit to the customer | Proposes the most scalable design | Proposes a design the customer's team can operate |
| Building blocks | Custom components | Managed services, which the cloud provider runs, patches, and scales |
| Cost | Not mentioned | An estimate with the main cost drivers and stated assumptions |
| Change | Describes only the target system | Explains the order of the move and how to go back |
| Trade-offs | "It depends" | Names what the design gives up and why that is acceptable |

## Typical questions

- "A travel booking company runs its website on 14 servers in its own data center, and the contract ends in 9 months. How would you move it to the cloud?"
- "A payroll service runs in one cloud region. Design disaster recovery that survives the loss of that region."
- "Design a platform that serves 3,000 business customers and keeps each customer's data apart."
- "Our cloud bill has doubled in two years. The board wants it 40 percent lower within one quarter. Where do we start?"

## A worked example

**The question:** "A ticket seller must put 60,000 concert seats on sale in 10 weeks. Last year the site failed within 4 minutes."

**Discovery turns the goal into numbers.** About 500,000 fans arrive in the first 15 minutes, and the average order is 2.5 seats. Ticketing runs on 12 servers with a fixed count and one database with no standby copy.

**The numbers decide the shape.** 500,000 fans in 900 seconds is about 556 arrivals a second. Only 60,000 / 2.5 = 24,000 orders can ever succeed. Sizing checkout for 556 buyers a second would pay for capacity that mostly serves fans who cannot receive a seat.

**The design.** A waiting room page, served from a content delivery network (CDN), holds the arrivals and admits 20 fans a second to checkout. At that rate, 24,000 orders complete in 20 minutes. Checkout runs on containers that are added for the sale only, and the database gains a standby copy.

**The deep dive goes to the largest risk.** Selling one seat twice breaks the customer's main goal, so the deep dive covers how checkout holds a seat, not how the waiting room page is served.

**The trade-off, stated aloud:** "Fans wait in a line instead of seeing errors. The design rejects capacity for every arrival, because that capacity would be used for 20 minutes a year."

## When the interviewer changes a requirement

Requirements change in this round on purpose. Recompute before answering. If fans spend 10 minutes in checkout instead of 5, twice as many are active at once, so checkout needs twice the containers. The sell-out time stays at 20 minutes, because it depends only on the admission rate.

## How to prepare

1. Learn one method and use it on every practice case. The [design round framework](../cheat-sheets/design-round-framework.md) gives ten steps with a minute budget.
2. Add a cost estimate to every design. The [cost estimation sheet](../cheat-sheets/cost-estimation.md) shows the calculation.
3. Practice migration and recovery questions with the [migration and disaster recovery sheet](../cheat-sheets/migration-and-disaster-recovery.md).

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=rounds-architecture-design) works through ten architecture case studies, including a migration, multi-region recovery, a 40 percent cost reduction, and a data residency design.
- [Grokking the System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=rounds-architecture-design) teaches the components and estimates that both kinds of design round use.
- [Solutions architect interview vs. system design interview](https://www.designgurus.io/answers/detail/solutions-architect-interview-vs-system-design-interview-what-is-the-difference?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=rounds-architecture-design) explains the difference in detail.
