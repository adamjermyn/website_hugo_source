+++

date = ""
title = "Prioritization"
hidden = false

weight = 2

+++

## Prioritization

Picking the right ideas to work on is **important**.

I write ideas in Markdown notes with one top-level header per idea. To decide what to work on, I use a [python script](https://github.com/adamjermyn/PriorMD) which asks me to compare ideas to one another. The comparison questions are:

1. If both ideas work, what is their relative impact?
2. What are the relative odds of the ideas working?
3. How long will each idea take to implement? (in relative terms)

The answers to these questions then give the ratio of the expected value (utility) per unit time:
$$
\mathrm{Score} = \frac{\mathbb{E}[U_1 / t_1]}{\mathbb{E}[U_2 / t_2]}
$$
Taking the log of both sides produces a series of linear relations between the expected value per unit time for each idea. The script I wrote performs a least squares solve on those relations to produce a (relative) score for each idea. It then outputs a list of ideas ranked by their score.

When I started doing this I was surprised by how much different ideas vary in expected value. On any given day the difference between the best idea I have and the median idea might be an order of magnitude. Over longer periods the range of idea quality is maybe a factor of a thousand. That reinforces the idea that prioritization is important.

For me the value in doing this is not in the precise scores or formulas, but in being forced to make an honest estimate of how much each project I take on is aligned with my goals, how likely it is to succeed, and how big a time commitment it is.

