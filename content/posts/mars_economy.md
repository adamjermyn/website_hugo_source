+++
title = "An Economic Model of Martian Growth"
date = 2020-11-15T16:33:47-05:00
tags = [""]
categories = [""]
draft = false

+++

# An Economic Model of Martian Growth

[Mars is an expensive place to live](http://adamjermyn.com/posts/mars_scales/), but it rapidly becomes cheaper the [more infrastructure](https://caseyhandmer.wordpress.com/2018/09/03/how-to-industrialize-mars/) it has! Because of that the total cost of building a self-sufficient city on Mars depends on how quickly infrastructure can be built. This is the key question I want to understand: what is the best way to invest in Martian infrastructure that minimizes the total cost?



## A Simple Model

To do this I'll build a simple model of economic growth on Mars. In this model, a group of backers on Earth pays for the Martian city until it reaches self-sufficiency. At any time $t$ there are $n(t)$ people on Mars. Each person costs $c_0$ to send to Mars in the first place. They also produce resources $p(t)$, consumes resources $c(t)$, and invest resources $i(t)$ per unit time in local infrastructure and industrial capacity. The resources produced are used to meet consumption and investment needs, not shipped back to Earth for a profit. A minimum condition for self-sufficiency is when production first exceeds consumption ($p(t) = c(t)$), which occurs at time $t_f$.  Assuming a zero discount rate, the total cost of the venture to backers on Earth is then  $T = n(t_f) c_0 + \int_0^{t_f} n(t)(c(t) - p(t)+i(t)) dt$.

A zero discount rate is a reasonable assumption given the time-scales involved. The number of people and their productivity should easily double in just a few years, which is fast compared to typical discount rates of a few percent per year (doubling times of $30+$ years!). Similarly I'll ignore infrastructure depreciation: most of the infrastructure built on Mars should last decades or more, just as on Earth. In an economy where output doubles in a few years this makes depreciation negligible.

I'll assume that launch costs and the cost of producing goods on Earth are both fixed. Because of this, I'll measure production and consumption in terms of the cost to ship goods from Earth **even if they are produced locally**. This is just a choice of units, akin to choosing between measuring in dollars versus yen, but it is a convenient choice because it means that $c$ is constant in time so as long as launch costs and production costs on Earth are fixed.

To complete the model I need to know how the productivity $p(t)$ of people varies with the cumulative investment per person $I(t)=I_0 + (1/n(t))\int_0^t n(t') i(t') dt'$, where $I_0$ is an initial investment per person that is baked into the cost $c_0$ of sending the person to Mars in the first place. In the standard [Solow-Swan model](https://en.wikipedia.org/wiki/Solow–Swan_model) productivity proportional to cumulative investment to some power $0<\alpha<1$, i.e. $p(t) = p_0 (I(t)/I_0)^\alpha$ where $p_0$ is the initial productivity of the first person on Mars.

A feature missing from the Solow model is a dependence on the number of people. For large populations this dependence is small, which is why the Solow model is often used to model the economies of whole nations. For small populations though there are clear efficiency gains with increasing population. For instance it doesn't cost twice as much to build a water treatment plant for two people as to build one for a single person.

A more applicable model then is one where the productivity of each person rises with the number of people, because I'm using units where the per-person costs are fixed. So let's say that $p(t) = p_0 (I(t) / I_0)^\alpha n(t)^\beta$ for some $\beta > 0$.

## Intuition

Before solving this model, it's worth building some intuition. When $\alpha \gg \beta$, productivity increases more with investment than with population, so on the margin the best strategy is to invest more per person, not to fly more people to Mars. This obviously can't scale down to the limit of zero people, but it suggests a small and extremely well-equipped group to start. Eventually this group likely hits diminishing returns from further investment, so $\alpha$ decreases, and it becomes important to start sending more people.

On the other hand when $\beta \gg \alpha$, most productivity gains come from economies of scale and shared infrastructure. In this limit the best strategy is to send as many people to Mars as fast as possible, and to equip them minimally. Like the other limit this can't continue forever; eventually economies of scale dry up and it becomes more important to invest in capital than in population.

## Solution

The backers of this city can determine how many people to send ($n(t)$) and the level of investment $(I(t))$. Let's pick an exponential for both so that $I(t) = I_0 e^{\gamma t}$ and $n(t) = e^{\lambda t}$, giving $\gamma$ and $\lambda$ as free parameters the backers can fiddle with. With this the total cost of the venture is specified by the integral defining $T$. The algebra is messy, but it's available in [this](http://adamjermyn.com/notebooks/mars_economy.nb) Mathematica Notebook. With the assumption that productivity is initially low ($c \gg p_0$) and that the time for the running costs to exceed startup costs is short ($c/c_0 \gg \lambda,\gamma$), the total cost is approximately 
$$
T \approx (c/\lambda) (c/p_0)^{1/(\beta + \alpha\gamma/\lambda)}\frac{\alpha \gamma+\beta\lambda}{\lambda(\alpha\gamma+\beta\lambda+\lambda)} + I_0 (c/p_0)^{(\lambda+\gamma)/(\alpha\gamma+\beta\lambda)}\frac{\gamma}{\gamma+\lambda}​
$$
What does this complicated equation mean? The most important feature is that, because $c \gg p_0$, it depends **strongly** on the two exponents. This dependence might be made clearer if I write it in terms of the constant $k \equiv (c/p_0)^{1/\alpha}$ (dependent only on properties of labor and technology), the ratio $\omega\equiv \beta/\alpha$ of the relative importance of increasing population versus increasing investment, and the ratio $q \equiv \gamma/\lambda$ of the rates of increase of investment and population. In those terms $T \approx (c/\lambda) k^{1/(q+\omega)}(\alpha (q+\omega))/(1+\alpha(q+\omega)) + I_0 k^{q/(q+\omega)}(q/(1+q))$.

## Cost Minimization

 The backers don't control $\omega$ or $k$ because those are just properties of labor and technology. So the backers want to minimize costs by controlling the only knob they have, which is the ratio $q$ of the relative growth rates of investment and population.

To understand how the cost depends on $q$, let's look at a few extreme cases.

If most of the productivity gains come from investing more per person, and not from scaling up the number of people, then $\alpha \gg \beta$ and $\omega \ll 1$. Let's also assume that $\alpha=1$ to keep things simple. In this limit, the cost is $T \approx ((c/\lambda)k^{1/q} + I_0 k)(1/(1+1/q))$. I couldn't find a nice way to solve this, but notice that the first factor increases exponentially in $1/q$ and the second decreases polynomially in $1/q$, suggesting that the optimum is around $q \approx \ln k \gg 1$, likely with some logarithmic dependence on the ratio $c/\lambda I_0 k$ as well. Because $q$ is large, $\gamma \gg \lambda$, and as expected the solution is to invest heavily in infrastructure and equipment and lightly on popoulation.

On the other hand, if most of the gains come from economies of scale then $\omega \gg 1$ and $T \approx (c/\lambda) k^{1/\omega} + I_0 k^{q/\omega}(q/(1+q))$. This clearly decreases with decreasing $q$ all the way down to zero, so the cheapest solution is to invest first and foremost in increasing population ($\lambda \gg \gamma$), and only turn to increasing investment once population gains level off.

## Which limit is real?

Are the opportunities in Martian cities in economies of scale or in investment per person? I don't know, but I suspect that they begin in investment and rapidly switch to scale past a critical point. Initially, increasing investment gives people heavy machinery, robots, ground support, custom control software, and so on. These generate large productivity gains, but eventually run into the problem that some technologies just [require many people](https://caseyhandmer.wordpress.com/2020/07/20/case-study-iceland/) to be economically viable. Building a chip fab or diverse chemical plant requires lots of people, and by the time those are the limits the city is well into the regime where population matters. 