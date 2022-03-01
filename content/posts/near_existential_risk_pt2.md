+++
title = "Toy Model of Near-Existential Risk"
date = 2021-04-23T16:05:02-04:00
tags = ["Longtermism"]
categories = [""]
draft = false

+++

I recently wrote about [near-existential risk](https://adamjermyn.com/posts/near_existential_risk/). These are risks which result in massive losses to society of people/technology/capability, but which themselves do not actually end or permanently curtail human existence. Here I want to build a toy model for thinking about these risks and how they relate to actual existential risks.

## A Toy Model

For these purposes I'm going to reduce the many dimensions of loss to a single parameter $\ell$. When $\ell = 0$ nothing is lost, when $\ell = 1$ all is lost. $\ell=1$ therefore denotes existential risks. Think of $\ell$ as a proxy for 'what fraction of people/technology/capability/organization/etc. are lost?'

Similarly, I'm going to reduce the many dimensions of civilizational capability to a parameter $c$. The greater $c$ is the more robust society is against risks, and so an increase in $c$ results in a *decrease* of risks.

To relate $c$, $\ell$, and the probability of risks, I'm going to ignore smaller risks with $\ell < 1/2$  and assume that larger risks with $\ell > 1/2$ are distributed as
$$
\frac{d^2 P(\ell)}{dt d\ell} = \frac{k}{2^c \ell^{c}}
$$
That is, the probability per unit time of a risk of size $\ell$  is proportional to $\ell^{-c}$. Here $k$  is a constant with units of ${\rm time}^{-1}$ and the factor of $2^{c}$ just normalizes the distribution so that overall odds of any risks fall with increasing $c$. For mathematical ease I'm going to allow risks with $\ell > 1$: these are all existential.

This captures the notion that risks are power-law distributed (i.e. a risk that is $N$ times worse is some power of $N$ times less likely). Many risks follow power-law distributions, including [earthquakes](https://en.wikipedia.org/wiki/Gutenberg–Richter_law) and certain kinds of [financial risk](http://hornacek.coa.edu/dave/Junk/farmer2004u.pdf), and the broader class of fat-failed distribution is part of the premise behind [black swan theory](https://en.wikipedia.org/wiki/Black_swan_theory) and Nassim Taleb's broader mantra that risks are dominated the [tails of the distribution](https://www.fooledbyrandomness.com/FatTails.html).

Next, I'm going to assume that on average capability $c$ increases exponentially with time, with an $e$-folding time $\tau$, but that when a risk is realized (i.e. the loss $\ell$ is incurred) it sets capability back by a fractional amount $\ell$. So typically
$$
c \propto e^{t/\tau}
$$
but occasionally
$$
c \rightarrow c(1-\ell)
$$
with the caveat that when $\ell > 1$, $c \rightarrow 0$.

Before exploring the model in detail, I just want to recap the assumptions:

- Risks are power-law distributed in how much loss they cause.
- Risks that would cause more than 100% loss are capped at 100%.
- Capabilities to avert risks grow exponentially with time.

The most suspect of these to my eye is the last one: civilization currently is robust against certain risks that were much worse in the pre-industrial era  (e.g. sudden drought/crop failure) but is much more fragile against brand new kinds of risk, like nuclear war.

## Model Predictions

Setting that aside, what does this model predict?

Over time risks fall on average. The odds of an existential risk are proportional to
$$
\frac{dP(\ell > 1)}{dt} = \int_{1}^{\infty} \frac{k}{2^c\ell^{c}} d\ell = \frac{k}{2^c(c-1)}
$$
which decreases as civilizational capability $c$ increases. Because of this, almost all of the risk happens at early times. At late times $c$ is enormous and we're in the clear. In particular, if the starting capability $c_0$ is large and if we ignore all non-existential risks then the total odds of existential risk are
$$
P_{\rm ex} \approx \int_0^\infty \frac{k}{2^{c_0 e^{t/\tau}} (c_0 e^{t/\tau}-1)} dt \approx \frac{k\tau}{2^{c_0} c_0}
$$
Here I've very crudely approximated the integral by noting that the denominator becomes large on a timescale of $\tau$, so the integral is roughly the integrand at $t=0$ times $\tau$.

At the same time, in this model near-existential risks look pretty bad. Again assuming $c_0 \gg 1$, the odds of existential risk per unit time are roughly $k/c_0$. If suddenly a risk of $\ell=0.9$ happens then the odds of existential risk rise from $k/c_0$ to $10k/c_0$, a ten-fold increase.

More generally, how much larger is $P_{\rm ex}$ once we incorporate near-existential risks? This is like asking about the odds of the pathway of (near-existential risk $\rightarrow$ existential risk).

For these purposes I'll call risks that have $\ell > 1/2$ near-existential (imagine half of all cities disappearing overnight). The odds per unit time of an event with $1/2 < \ell < 1$ are
$$
\frac{dP(1/2 < \ell < 1)}{dt} = \int_{1/2}^{1} \frac{k}{\ell^{c}} d\ell = k\frac{2^{c-1}-1}{2^c (c-1)} \approx \frac{k}{2 c}
$$
which is a factor of $2^{c-1}$ times more likely than existential risks. If one of these risks happen though, the odds of an existential risk increase by a factor of roughly $1/(1-\ell)$, and remain elevated by that much for a time of order $\tau$ (the civilization rebuilding time). Even if all near-existential risks had $\ell=1/2$, that doubles the odds of existential risks for a time $\tau$ before they fall back down. Specifically, the change in $P_{\rm ex}$ is of order
$$
\Delta P_{\rm ex} \approx \int_0^{\infty} \frac{dP(1/2<\ell<1)}{dt'}\int_{t'}^{\infty} \frac{dP(\ell > 1)}{dt} dt  dt' \approx \int_0^{\infty}\frac{k^2\tau}{2^{c_0 e^{t'/\tau}} c_0^2 e^{2 t'/\tau}} dt' \approx \frac{(k\tau)^2}{2^{c_0} c_0^2}
$$
where the double integral is summing over all possible paths of the form "time $t'$ passes before the near-existential risk, then some amount of time later an existential risk happens". This isn't quite right because it ignores the odds of an existential risk happening first, or of multiple non-existential risks, but if all probabilities involved are small the error shouldn't be too large.

The expression above is unwieldy, but can be written instead as
$$
\Delta P_{\rm ex} \approx \frac{k \tau}{c_0} P_{\rm ex}
$$
In other words, whether near-existential risks matter for purposes of existential risk depends entierly on the ratio $k\tau/c_0$. What is that ratio? Unfortunately this is very hard to estimate because (fortunately) large risks of this sort are very rare.

## Rough Estimates

As an extremely rough base rate anchor,  $c_0/k$ is the typical timescale on which we expect large risks ($\ell \sim 1/2$) to occur, and $\tau$ is the timescale on which civilization rebuilds from large losses.  The last $\ell \sim 1/2$ global disaster to occur was the [Plague](https://en.wikipedia.org/wiki/Black_Death) in the 1300s, which killed an estimated 1/4 of all people (30-60% of people in Europe), which suggests that $c_0 / k$ is of order 700 years. World population took a century or so to recover (based on some very quick googling), suggesting that $k\tau/c_0 \approx 1/7$. If that's the case, near-existential risks do not contribute all that much to the overall odds of existential risk.

An alternate anchor is to reason with the inside view. The inside view here says that at least some future near-existential risks have odds of order 0.1 percent per-year[[1](https://www.metaculus.com/questions/3517/will-there-be-a-global-thermonuclear-war-by-2070/),[2](https://www.metaculus.com/questions/1585/ragnar%25C3%25B6k-question-series-if-a-nuclear-catastrophe-occurs-will-it-reduce-the-human-population-by-95-or-more/),[3](https://www.metaculus.com/questions/1493/ragnar%25C3%25B6k-question-series-by-2100-will-the-human-population-decrease-by-at-least-10-during-any-period-of-5-years/)] which means $c_0 / k$ is of order 1000 years. Rebuilding times seem likely to be of order the time it takes for countries to industrialize, which is 50 or so years, giving $k\tau / c_0 \approx 1/20$. The exact figure depends on what size of disaster "counts" for these purposes and what counts as a recovery, but this serves to set an order of magnitude and agrees surprisingly well with the base rate answer.

These estimates suggest that near-existential risks are not a likely pathway to bad-existential outcomes relative to direct existential risks, in contrast to my intuition from [before](https://adamjermyn.com/posts/near_existential_risk/), and this model has caused me to update in the direction of worrying more about existential than near-existential risks.