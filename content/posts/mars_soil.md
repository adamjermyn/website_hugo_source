+++
title = "Growing Food on Mars"
date = 2021-01-10T10:24:23-05:00
tags = ["Mars"]
categories = [""]
draft = false

+++

Growing food on Mars is a critical component of making a self-sufficient city because [shipping food is expensive](http://adamjermyn.com/posts/mars_scales/).

Unfortunately it seems that Martian regolith is too alkaline and is missing key nutrients [needed to grow crops](https://www.sciencedirect.com/science/article/abs/pii/S0019103520303845). The alkaline issue can be solved by adding acid, which is both low-weight and can be produced locally if need be. The nutrient issue can be addressed either by adding [organic material](https://www.degruyter.com/view/journals/opag/4/1/article-p509.xml?language=en) or by artificial [nutrient supplementation](https://www.sciencedirect.com/science/article/abs/pii/S0019103520303845). Each of those come with their own costs, so I want to examine both and see which is cheaper.

## Organic Matter Economics

For crop experiments NASA produces soil with similar properties to Martian regolith, known as JSC-1A. A [2019 experiment by Wamelink+](https://www.degruyter.com/view/journals/opag/4/1/article-p509.xml?language=en) found that nine common crops including cherry tomatos and rye can be grown in JSC-1A with only slightly lower-than-Earth yields as long as some organic material (lawn cuttings) is added first.

That study used 267g of organic matter for every 7.5L of JSC-1A (roughly 400g), or a mass ratio of 2:3. While they didn't study how much organic matter was needed, I'm going to assume that that ratio is good enough for order-of-magnitude estimates.

I'll use Rye as a typical crop. On Earth, Rye yields roughly [900kcal per square meter](http://www.gardeningplaces.com/articles/nutrition-per-hectare1.htm)per harvest and requires soil roughly [1m deep](https://soilandhealth.org/wp-content/uploads/01aglibrary/010139fieldcroproots/010139ch6.html) for the root system. Wamelink+ found that Rye has a comparable yield in Martian regolith, so I estimate that Rye produces $900{\rm kcal}$ per cubic meter of soil per harvest. A typical period between planting and harvesting is [5 months](https://www.growveg.com/plants/us-and-canada/how-to-grow-cereal-rye/), so the yield is of order 6kcal per day per cubic meter of soil. A typical ~2000kcal diet consists of ~[2.5kg of food](http://adamjermyn.com/posts/mars_scales/), for a typical density of 1.2g/kcal. So 6kcal of Rye offsets the need for ~7g of food shipped in from Earth.

That same cubic meter of soil needs ~33kg of organic material shipped from Earth at the start. After the point human waste and non-harvested plant matter can be put back in the soil in place of shipping more organics from Earth, so this is genuinely a one-time cost. In exchange for that cost, Mars indefinitely reduces its shipping needs by 7g/day.

Even better, Rye *also* produces non-edible organic matter above and beyond what's in the soil, roughly [0.23kg per square meter per harvest](https://lib.dr.iastate.edu/cgi/viewcontent.cgi?article=1044&context=agron_conf), or 1.5g/day per cubic meter of soil, further reducing future shipping needs.

This may sound like a good deal, but a total of 8.5g/day implies a payoff time of 11 *years*! Is it possible to do better?

## Nutrient Supplementation

Instead of adding organic material to Martian regolith, [Eichler+2021](https://www.sciencedirect.com/science/article/abs/pii/S0019103520303845) added [Hoagland nutrient supplement](https://en.wikipedia.org/wiki/Hoagland_solution) to JSC-1A and were able to grow edible plants.

Unfortunately they don't compare the edible biomass to terrestrial yields, and I couldn't find a way to estimate the amount of nutrients they added from the data they provide. However, a crucial advantage of this approach is that the supplements are solutions of relatively simple molecules, mostly ionic salts of various kinds, and the most abundant elements in the supplement are also present at the [percent-or-more level](https://en.wikipedia.org/wiki/Composition_of_Mars) in Martian regolith (K, Mg, S, Cl, O) or in the Martian atmosphere (N, O). That means the nutrient supplement could be made in bulk by mining regolith, capturing atmosphere, and performing a few tens of chemical reactions at scale. This involves much more upfront effort than gradually growing a stock of biomass, but could produce dramatic reductions in shipping cost.

As a very crude estimate, suppose that a nutrient factory has the same mass of equipment as it processes in raw materials in a single batch. This is likely an overestimate given that most equipment has mass scaling like batch surface area (pipes, tubes, vessels, etc.) while batches have mass scaling like their volume. Further suppose that 1% of the raw materials turn into supplement, which seems reasonable given the abundances of supplement-necessary elements in Martian regolith. Finally, suppose that each batch requires one week to process. I picked that timescale to be conservative; it's several times longer than the time it takes to [process crude oil](https://www.petro-online.com/news/analytical-instrumentation/11/breaking-news/how-long-does-it-take-to-produce-petrol/45321). 

With these assumptions, a factory has an upfront cost of 2kg of equipment per 1kg/year of production capacity. If it takes as much supplement as organic matter to make Martian regolith arable then 2kg of equipment *accelerates* crop capacity at a rate of 0.2kcal/day/year.

Of course a factory is unlikely to be as small as 2kg because of fixed overhead costs, so this is a case of [increasing returns to scale](http://adamjermyn.com/posts/alpha_beta/), in which case those overhead costs could end up setting a floor on the minimum desirable Martian population.

## Comparison

Suppose I ship $10^6$kg of organic matter/lawn cuttings (scenario 1) or the same amount of nutrient factory equipment (scenario 2). Ignore the labor cost of assembling the factory and actually doing the farming.

In scenario (1) I can make $30,000{\rm m^2}$ of arable farmland and grow enough food for 90 people indefinitely. As a side benefit I can also produce enough extra biomass to make $500{\rm m^2}$ of arable land each year.

In scenario (2) I can make a factory that produces $260,000{\rm kg}$ of nutrient supplement each year, which is enough to make an additional $8000{\rm m^2}$ of farmland arable each year. Of course this farmland also produces biomass which can then make further arable land over time.

After four years scenario (2) has roughly same amount of arable land as scenario (1), and from that point on scenario (2) significantly out-produces scenario (1), making it the clear favorite.

There are obviously many uncertainties in these calculations, but mostly regarding the efficacy and mass requirements of nutrient supplements. I've tried to pick my assumptions to be as conservatively as possible in filling in the blanks, so the above likely **understates** the advantage of artificial nutrient supplements as a way of producing arable soil on Mars.
