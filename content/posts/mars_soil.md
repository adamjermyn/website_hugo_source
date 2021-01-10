+++
title = "Growing Food on Mars"
date = 2021-01-10T10:24:23-05:00
tags = ["Mars"]
categories = [""]
draft = true

+++

Growing food on Mars is a critical component of making a self-sufficient city because [shipping food is expensive](http://adamjermyn.com/posts/mars_scales/). Unfortunately it seems that Martian regolith is too alkaline and has none of the organic material [needed to grow crops](https://www.sciencedirect.com/science/article/abs/pii/S0019103520303845). These issues can be addressed by adding acid and [organic material](https://www.degruyter.com/view/journals/opag/4/1/article-p509.xml?language=en), but those come with their own costs unless also produced locally.

## Organic Matter Costs

For crop experiments NASA produces soil with similar properties to Martian regolith, known as JSC-1A. A [2019 experiment by Wamelink+](https://www.degruyter.com/view/journals/opag/4/1/article-p509.xml?language=en) found that nine common crops including cherry tomatos and rye can be grown in JSC-1A with only slightly lower-than-Earth yields so long as some organic material (lawn cuttings) is added first.

That study used 267g of organic matter for every 7.5L of JSC-1A (roughly 400g), or a mass ratio of 2:3. While they didn't study how much organic matter was needed, I'm going to assume that that ratio is good enough for order-of-magnitude estimates.

I'll use Rye as a typical crop. On Earth, Rye yields roughly [900kcal per square meter](http://www.gardeningplaces.com/articles/nutrition-per-hectare1.htm)per harvest and requires soil roughly [1m deep](https://www.tandfonline.com/doi/full/10.1080/00288233.2010.514927) for the root system. Wamelink+ found that Rye has a comparable yield in Martian regolith, so I estimate that Rye produces $900{\rm kcal}$ per cubic meter of soil per harvest. A typical period between planting and harvesting is [5 months](https://www.growveg.com/plants/us-and-canada/how-to-grow-cereal-rye/), so the yield is of order 6kcal per day per cubic meter of soil.

That same cubic meter of soil needs ~33kg of organic material at the start.



## Scaling Laws

A rough rule of thumb for trees is that the volume of soil the tree needs is proportional to the volume of the "crown" of leaves. That is, for a tree whose branches span a distance $d_b$, the roots span a similar distance $d_r \approx d_b$.

The fruit yield of a tree scales like the photosynthesis rate, which scales like the area of light captured. That in turn scales like the **area** spanned by the branches and leaves, so the yield scales like $d_b^2$ while the soil requirement scales like $d_r^3 \approx d_b^3$. So the *ratio* of fruit yield to soil cost scales like $d_b^{-1}$, favouring more smaller trees over fewer large ones.

These scaling laws break down at the very small end. Most vegetables are made by smaller plants which don't follow a clear scaling relation. **look into this**

  

