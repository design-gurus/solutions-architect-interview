# The Customer Discovery Role-Play

In the customer role-play, the interviewer acts as a customer and the candidate acts as the solutions architect (SA). The round measures discovery, which is a conversation in which the architect asks questions to learn the customer's goals and limits. It also measures objection handling. A solution proposed before any questions is the most common reason candidates fail this round.

## Who the interviewer may play

Preparation guides describe four characters. Each one needs different evidence.

| Character | What they care about | What convinces them |
|---|---|---|
| A skeptical engineering leader | Whether the design really works | A test result or a rejected alternative with reasons |
| A cost-focused executive | The yearly cost and the risk | A comparison with today's cost and its assumptions |
| A security team that blocks the project | Who can access the data | Named controls and audit documents they can check |
| A customer who uses a competitor | The cost of changing | A small first step with a measurable result |

## Four kinds of discovery question

Discovery moves from wide to narrow. Ask at least five questions before proposing anything.

| Kind | Purpose | Example |
|---|---|---|
| Open | Find the topics | "What happened during the last sale?" |
| Specific | Find the facts | "How many servers run the online store today?" |
| Quantifying | Find the numbers | "How many orders arrive in the busiest hour?" |
| Confirming | Check understanding | "So the lease ends in 18 months, and the date cannot move?" |

Avoid a question that suggests its own answer, such as "You would want automatic scaling, right?" It produces no new information.

## What a first conversation must learn

1. **Business drivers:** the business reasons behind the project, such as a lease that ends or sales lost in an outage.
2. **The current state:** what runs today, who operates it, and what limits it.
3. **Success criteria:** the measurable results that will show the project worked.
4. **The decision process:** who approves, who influences, and when the decision is due.

End the conversation with a summary and ask the customer to correct it. A useful target is to speak for less than one third of the time.

## Answering an objection in four steps

An objection is a concern that blocks a decision until it is answered. Most objections contain a real risk.

1. **Acknowledge.** Say that the concern is reasonable, without agreeing with the conclusion.
2. **Clarify.** Ask which part matters most, because one objection often hides several.
3. **Answer with evidence.** Use the customer's own numbers, a test result, or a document they can check.
4. **Confirm.** Ask whether the answer resolves the concern, and agree on a next step if it does not.

## A short example

> **Customer:** "Your platform costs 30 percent more than your competitor's."
>
> **Weak answer:** "Our platform has more features, and the difference pays for itself."
>
> **Strong answer:** "That gap deserves a careful look. Which workloads does the 30 percent cover, and over what period? If it compares capacity sized for your sale week all year, the comparison changes, because you need 6 times normal capacity for one week in 52."

The strong answer asks before it answers. It also uses arithmetic the customer can check. Fixed capacity for the peak is 6 units for 52 weeks, or 312 unit-weeks. Capacity that grows only for the sale is 1 x 51 + 6 x 1 = 57 unit-weeks.

## Two answers that candidates avoid

- **"I do not know."** Say it, write the question down, and promise an answer by a named date.
- **"No."** When a deadline cannot be met, say so and offer the part that can be delivered by that date.

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=rounds-customer-discovery-role-play) has a six-lesson chapter on discovery and objections, with written role-play transcripts that contrast a weak and a strong answer line by line.
- [What questions are asked in a solutions architect interview?](https://www.designgurus.io/answers/detail/what-questions-are-asked-in-a-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=rounds-customer-discovery-role-play) lists the objections candidates hear most.
- Practice with the role-play questions in the [question bank](../cheat-sheets/question-bank.md).
