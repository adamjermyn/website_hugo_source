+++
title = "Mass Scales for Living on Mars"
date = 2020-10-24T15:52:11-04:00
tags = [""]
categories = [""]
draft = false

+++

# Mass Scales for Living on Mars

*Big thanks to Casey Handmer for reading and commenting on an early draft of this.*

One of the most exciting things that may well happen this century is a sustained human presence on Mars. The main reason this is possible at all is that SpaceX has cut launch costs dramatically. Despite this progress, cargo sent from Earth and soft-landed on Mars is likely to be the primary resource constraint in the Martian economy for a very long time, so it is worth exploring the scale of cargo required to support a human presence, and what that translated into in dollars.

As a first cut I want to imagine a single person on Mars, living entirely on cargo shipped from Earth. They don’t produce any goods on Mars and they don’t recycle any of their consumables. The closest analogies on Earth are Antarctic outposts or isolated military installations, though with some key differences. For instance an Antarctic base doesn’t need to carry a supply of Oxygen and Nitrogen to breathe, whereas a person on Mars does.

This scenario sets an upper bound on the cargo needed to sustain a human presence on Mars. Costs fall if there are multiple people who can share resources. Amortized costs also fall if people build local infrastructure and produce or recycle goods locally on Mars, though [the upfront cost may need to be much greater](https://caseyhandmer.wordpress.com/2020/05/21/starting-the-mars-base/) to support shipping industrial equipment.
In addition to setting an upper bound, this scenario demonstrates how the mass budget changes when different categories of goods are produced locally. That suggests an order in which goods should be made locally (see also: [Progression of space industrialization](https://caseyhandmer.wordpress.com/2020/08/23/progression-of-space-industrialization/)).

## What do humans need?
Need is a strong word. For this exercise I'll assume a typical American material quality-of-life, to the extent that this is possible on Mars. The goal is to see what the mass cost is to support someone without making any lifestyle compromises. Those can come later if necessary once we know an upper bound on the mass cost.
Humans need air, water, food, energy, shelter, and "other". Here "other" refers to miscellaneous goods including consumables (medicine, toiletries, etc.) as well as appliances, electronics, bedding, and so on. 

### Water
Of these categories, water is by far the most massive. A typical US household uses 300 gallons of water per day at home (https://www.epa.gov/watersense/how-we-use-water). Assuming four people to a household gives 75 gallons per person per day. If we have to ship all of that water to Mars, that works out to 100 Cargo-tons per person per year.

### Shelter
Shelter is a tough one to estimate for two reasons.

First, homes tend to be durable, so all the cost of shelter is upfront. To convert this into a per-year cost we have to amortize it over the number of years the shelter will be in use, and the answer we get will vary with the time-scale we assume.
Secondly, shelter on Mars isn't much like shelter on Earth. Probably the biggest difference is that shelter on Mars needs to be airtight, and to be able to hold that air in despite the inside air pressure being Earth sea level and the outside pressure being close to zero.

It turns out that making an airtight space that can hold in an atmosphere of pressure isn't that mass intensive, and one comes for free with every cargo shipment. Each SpaceX starship full of cargo [comes with](https://web.archive.org/web/20180808022709/http://www.spacex.com/sites/spacex/files/making_life_multiplanetary_transcript_2017.pdf) $1000\mathrm{m}^3$ of pressurized volume. A typical home in the US has 150 square meters of living area (https://www.bobvila.com/slideshow/this-is-the-average-home-size-in-every-state-53461), and ceilings 2-3 meters high, so each Starship provides housing for two people if it can be converted once on the ground.

What about living area outside the home? On Earth I can walk outside and enjoy acre-sized public spaces that aren’t my home. I’d like to be able to do the same on Mars. For much larger areas we could use multiple empty Starships, or send domes, or more likely send parts for [giant tented areas](https://caseyhandmer.wordpress.com/2019/11/28/domes-are-very-over-rated/). Using Casey Handmer’s estimates for tented areas, a 10m high tent needs 15kg of cable per square meter of floor area. The tent membrane strength is [42MPa](https://en.wikipedia.org/wiki/ETFE), a hemispheresphere 10m in radius needs ~2cm of membrane to hold in one atmosphere of pressure. With a [density](http://sterlingplasticsinc.com/materials/tefzel-etfe-ethylene-tetrafluoroethylene/) of $1.7\mathrm{g\,cm^{-3}}$, that means the cube needs ~20 tons of membrane and ~5 tons of cable, providing an extra $2000\mathrm{m}^3$ of living volume. The mass requirements scale linearly with volume, so covering an acre up to 5m costs ~250 tons.

This is a one-off cost, but we want to be able to think of this as a cost per year that the person is on Mars. Assuming someone goes to Mars for the rest of their natural life, it's not unreasonable to assume that they'll use this shelter for 40 years, giving a cost of ~6 Cargo-tons per person per year.

### Energy
The next biggest category is energy. A typical US household uses 11,000 kWh of electricity per year (https://www.eia.gov/energyexplained/use-of-energy/electricity-use-in-homes.php). A similar amount of energy is used in various forms to heat homes, so let's call the total 22,000kWh/year. Again assuming four people to a household, we find 5500kWh/year/person.
Of course Mars is cold, so we'll need to heat more. Presumably we'll also use much better insulation. I don't want to dive too deeply into the details yet, but to within a factor of a few this estimate of energy use seems fine.
Now how do we send 5500kWh/year to Mars? Solar panels are probably the best way, but let’s try do it entirely with consumables. Suppose we send methane plus enough oxygen to burn it to produce energy. And let's be conservative and say that we can capture that energy for useful work and useful heat at 30% efficiency. methane has a specific energy density of 56MJ/kg. We need 3g of oxygen to burn 1g of methane, so the energy density of the (methane, oxygen) bundle is 14MJ/kg, or 4kWh/kg. So we'll need to send 5500/4 ~ 1400kg of fuel to Mars, or 1.4 Cargo-tons per person per year.

### Food
The average American eats something like 2.5kg/day of food (https://en.wikipedia.org/wiki/Western_pattern_diet#/media/File:US_Food_Consumption_Over_Time.svg). That's 0.9 Cargo-tons per year

### Other
This is another tricky one. By definition this category contains an enormous diversity of goods. We can get a handle on it by noting that all of the goods in this category eventually get thrown out, at least on Earth. So in steady state the rate at which people need new "other" goods is comparable to the rate at which they produce non-food garbage.
In the US garbage production is ~[270 million tons per year](https://www.epa.gov/facts-and-figures-about-materials-waste-and-recycling/national-overview-facts-and-figures-materials). The US population is ~330 million, so that's ~0.8 tons/person/year. Some of this is food waste though. The US produces 133 billion pounds of food waste per year, or ~0.2 tons per year per person. So this "other" category comprises something like 0.8 - 0.2 = 0.6 Cargo-tons per person per year.
Like with shelter, this category is going to be front-loaded: you'll send more "other" things at the beginning than we need on an ongoing basis. Unlike shelter, the goods in "other" are replaced much more often than the physical structure of the shelter. One way to see this is to note that homes are usually older than almost all of their contents, so the amortization is much less important in this case than it was for shelter.

### Air
On average, a human needs to breathe around 0.1 liters/second of air. 80% of this is trivially-reusable inert Nitrogen. The remaining 20% is oxygen, which gets consumed and turned into carbon dioxide at a rate of 0.005 liters/second. That works out to ~150 cubic meters of oxygen per year, massing ~150kg. So we need to send 0.15 Cargo-tons per person per year of oxygen.




## Priorities for Local Production / Reuse
The total mass cost we found above is ~109 Cargo-tons per person per year.

**90% of that mass is water**, and water is conveniently one of the easiest things to clean and reuse. For instance, if we don't care about the energy cost we can just boil the water, condense it, and reuse it. Add a dehumidifier to capture water that gets lost to the air, which is a necessary part of environmental controls anyway, and we can get very high re-use efficiency with a small amount of equipment and complexity. Water can probably also be [mined](https://en.wikipedia.org/wiki/Water_on_Mars#Evidence_from_rocks_and_minerals) from rocks on or near the surface of Mars. So this is a clear place to start trimming mass, and is likely something we can do right from the start, no major infrastructure required.

Of the remaining 9 Cargo-tons per person, the biggest remaining category is the amortized cost of shelter, at 6 Cargo-tons per person per year. This is especially important to either reduce or produce locally because it's heavily front-loaded. Fortunately there are local building materials, and most of what's required are goods like plastics and iron/steel which require relatively little in the way of infrastructure to produce. So shelter can (mostly) be produced locally on Mars early on, and probably should be given that doing so reduces the mass cost by a factor of three%.

The next biggest item is energy. Energy can be produced locally by sending solar panels, which on Earth can produce an output as high as [1.2kW/kg](https://www.spectrolab.com/pv/support/Law%20et%20al.,%20%20WCPEC-4%202006,%20Thin,%20Flexible%20III-V%20MJ%20-%20Final.pdf). Mars is further from the Sun, receiving roughly one third as much light as Earth, so on Mars the same panels should generate 0.4kW/kg during the day, or 0.2kW/kg averaged over one day-night cycle, or 1800kWh/kg/year. That means that order 3kg of solar panels can provide all of a person's energy needs indefinitely (or at least until the panel [**slowly** degrades]( https://www.nrel.gov/docs/fy12osti/51664.pdf)).
People need energy at night too, so to locally produce energy we'll need to send batteries. Current batteries can store up to ~0.25kWh/kg, so to store one day of energy needs takes 60kg of batteries. Batteries decay too, but similarly slowly, and in either case both the mass of solar panels (3kg) and the mass of batteries (60kg) are tiny compared to the savings of 1.4 tons/person/year from not having to power our settlement with methane and oxygen from Earth.

Next comes food. Local food production is a much harder problem. The same holds for "other" goods, which by their very diversity require a large amount of advanced manufacturing infrastructure to produce locally. Oxygen can be produced locally without much cost, but it's such a small part of the mass budget that it doesn't make a difference to the bottom line whether it's made locally or not.

Based on this, early priorities should be, in this order:
\- Water recycling/mining.- Locally built shelter/structures.- Bringing solar panels and batteries from Earth.
These three together bring the cost down from 109 to just 1.6 Cargo-tons per person per year, and all are achievable with robust technologies we more or less have on hand.



## What is a Cargo-ton in USD?

The Perseverance rover launched in July 2020 on an Atlas V rocket for a [cost](https://mars.nasa.gov/news/nasa-awards-launch-services-contract-for-mars-2020-rover-mission/) of \\$243 million. The final mass to be delivered to Mars is just over a ton, so by this estimate one Cargo-ton is \$243 million.

A Falcon 9 launch costs ~\\$60 million and has a similar payload capacity to an Atlas V, giving a
much lower estimate of \\$60 million per Cargo-ton. Even with this lower estimate, supporting people on Mars via cargo from Earth is an
expensive proposition of ~\$100 million per person per year. 

How does this change in the future? SpaceX is currently building a new rocket called Starship, with a goal of having a reusable Starship launch [cost](https://www.space.com/spacex-starship-flight-passenger-cost-elon-musk.html, https://arstechnica.com/science/2020/03/inside-elon-musks-plan-to-build-one-starship-a-week-and-settle-mars/) \\$2 million and an expendable one cost \\$5 million. Starship is also designed to be able to refuel in Earth orbit, allowing it to take 150 tons of payload to Mars. Suppose we send each Starship on a one-way trip to Mars, and have to make of order 5 refueling launches for each. Then a cost of \\$15 million gives 150 tons of shipping to Mars,
or \\$100,000 per Cargo-ton.
These are all rough estimates, but they serve to set the scale of the problem under different assumptions about local (Martian) production and technologies. Consider two kinds of shipping (current rockets versus starship) and two kinds of production (all on Earth versus water, shelter, and energy on Mars). From most expensive to least expensive these give four scenarios:

- Current rockets, no local production: $6.5 billion per person per year.

- Current rockets, minimal local production $100 million per person per year.
- Starship, no local production: \$11 million per person per year.
- Starship, minimal local production: \$160,000 per person per year.

It’s clear from this list that rockets **really** matter. Better rockets make a much bigger difference than producing water and shelter and energy on Mars. At the same time, the ~70x reduction that comes from producing just a few simple goods on Mars is crucial, and brings a sustained human presence on Mars down from the realm of “only global superpowers can do it” to “most countries and many companies can do it if they want”, and that makes a sustained presence on Mars much more plausible.
