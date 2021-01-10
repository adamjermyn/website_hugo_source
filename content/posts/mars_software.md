+++
title = "Early Martian Software"
date = 2021-01-01T14:29:20-05:00
tags = ["Mars"]
categories = [""]
draft = false

+++

Building a city on Mars will be [very capital intensive](http://adamjermyn.com/posts/alpha_beta/) because in the early stages it's extremely expensive to sustain people on Mars. But capital is a vague term: what does this actually look like?

<img src="https://upload.wikimedia.org/wikipedia/commons/f/f2/Mir_during_STS-74_%28cropped%29.jpg" alt="The MIR space station" style="zoom:200%;display:block;margin-left:auto;margin-right:auto" />

The last few attempts at a human presence in space primarily used *physical* capital: heavy machinery, [giant rockets](https://en.wikipedia.org/wiki/Saturn_V) and space stations and industrial equipment. Mars will need all of that too. But the last few times were in the 1960s-90s, when computers were slow and software much more limited and expensive than today. Even in the early 90s there weren't many opportunities to save human labor with software, outside of routine tasks ("regulate Oxygen levels in this range").

With lower costs and dramatically greater capabilities, a Martian city should be heavily supported by custom software written on Earth **in response to the city's needs**.

## A Day in the Life

Imagine you're on Mars. You wake up, eat breakfast, and get to work. Your work happens in a pressurized environment under [giant tents](https://caseyhandmer.wordpress.com/2019/11/28/domes-are-very-over-rated/). Your first task of the day: assemble ten robot arms from parts that landed last week.

You strap on augmented-reality glasses. The glasses pick up a QR code on the containers of robot parts, and load software that guides you through the assembly, highlighting which pieces go where and which tools you need to attach them.

After you finish the first robot arm you give it a test. It's supposed to move items from one conveyor belt to another, [Factorio-style](https://wiki.factorio.com/Inserters#Belt_to_chest_.28perpendicular.29). The arm successfully picks up the test rock, but then drops it while the arm is still moving, causing it to miss the drop area. You fill in a bug report, send it back to Earth, and move on to the next job. Tomorrow there'll be an update from Earth that fixes the bug.

## Speed

Why is the turnaround so fast? Simple: early on, keeping you alive and working on Mars [costs of order](http://adamjermyn.com/posts/mars_scales/) \$100 million per year. That kind of money can pay for an awful lot of software engineers, so rather than sending 100+1 people to Mars, better to send 100 people and hire 40 software engineers to tend to their every software need. Better yet, send 90 people and hire 440 software engineers. That's enough for everyone on Mars to a team dedicated to just the problems that they personally encounter.

Some of this [already happens](https://www.nasa.gov/centers/johnson/pdf/584732main_Wings-ch4f-pgs256-269.pdf) on the International Space Station, where the investment in software tooling is much higher than for almost any other workplace. My prediction is that this will be even more extreme for Mars, with higher cost-per-Martian driving a larger investment in software.

Another driver of software on Mars will be a very different demand and incentive structure. The goal of building a city on Mars is to get to industrial or financial self-sufficiency. Every step in that direction saves money **on an ongoing basis**, so there's a huge incentive to develop infrastructure as fast as possible. It's more like a race or a pre-cash-flow startup than a science experiment.

## Reliability

Software written for the ISS has to be *very* safe, and the ISS can afford the time it takes to do extensive testing. This is because there's only one ISS, it's relatively fragile, it isn't expanding rapidly, and it's a **known environment**. All of those factors point to a longer turnaround and high reliability.

A Martian city sits in the opposite limit. It's expanding rapidly, so losing the occasional part is acceptable. It's much more self-sufficient, so it's not nearly as fragile as the ISS. It's also a mostly-unknown environment: except in the broadest terms we don't know what tools will work well on Mars, how they'll fit together, or what a Martian city will actually look like. All of these factors point to consumer-grade software that's developed, deployed, and tested in-situ with a fast turnaround time.

## Conclusion

Building a city on Mars is going to involve *a lot* of software and digital/intellectual capital more broadly. It's going to be developed with fast turnaround and feedback from use in-situ. And this is all because the incentive of any commerical Mars venture is to reach self-sufficiency as fast as possible and with as few people on Mars as possible, which means a heavy reliance on automation.
