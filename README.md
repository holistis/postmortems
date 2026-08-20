# Postmortems

Short writeups of things that looked right and turned out wrong. Not marketing, not a highlight reel. The point is showing the actual process: a claim gets made, gets tested, sometimes survives, sometimes falls apart.

## 2026-08-20: Why our expected profit was not profit

We run an automated fleet of bots that look for opportunities in DeFi: liquidations and prize claims. On one side, the fleet worked exactly as intended. Opportunities were detected reliably. On the other side, it failed almost completely. Those opportunities were almost never captured.

The first suspect was a bug in execution. Wrong timing, wrong gas price, a race we kept losing. That was the obvious place to look first.

The real cause was deeper. The bots calculated their own expected value for every opportunity. That calculation looked convincing. Numbers, a formula, a positive result. We treated that result as proof. It was an assumption that had never been tested.

Only after we ran an adversarial verification pass did it fall apart. Not a check that confirms what you already believe. Multiple independent checks that actively try to disprove the hypothesis. That process exposed two things.

First, competitors had already priced the opportunity down to almost nothing. The opportunity existed, but by the time our bot saw it, there was nothing left to take.

Second, and this is the part that stung: our first recalculation, the one that supposedly fixed the mistake and landed on a positive number, contained two of its own optimism errors. We had corrected a wrong conclusion with a second wrong conclusion. Both times the result looked certain.

The lesson is easy to write down and hard to hold onto. Only count what actually lands in the wallet as profit. Not what a model says you could have made.

This goes beyond trading bots. Any AI system that treats its own output as evidence instead of a claim runs into the same wall. A summary of your own reasoning is not verification. Repeating your own calculation is not a second opinion.

Core lesson: if a model says it is profit, it is a claim, not a result, until an independent, actively adversarial check survives it.
