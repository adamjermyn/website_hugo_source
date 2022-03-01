+++
title = "Eliciting Latent Knowledge - Take 1"
date = 2022-01-28T15:55:42-05:00
tags = ["AI Safety"]
categories = [""]
draft = true

+++

Let's say I've built WeatherBot, a new machine learning system designed to predict the weather ten days from now. And let's say WeatherBot is very, very good. Every morning I feed WeatherBot new measurements of temperatures and wind speeds and humidities, and it spits out a new (correct) prediction of what the weather will be in ten days.

Somewhere deep inside WeatherBot there has to be a very accurate model of atmospheric science. WeatherBot has to know, in some sense, an awful lot about fluid mechanics and chemistry and insolation and all the other bits of physics that make weather prediction so difficult.

In fact, WeatherBot might even know more than atmospheric scientists do! They might want to learn from it. The trouble is, WeatherBot doesn't speak English. It can't answer their questions. WeatherBot is "just" a giant pile of linear algebra that takes in temperatures and humidities and so on and spits out accurate weather forecasts.

<img src=https://imgs.xkcd.com/comics/machine_learning.png style="max-width:100%;max-height:100%;display:block;margin-left:auto;margin-right:auto">

The things WeatherBot knows about atmospheric science are examples of **Latent Knowledge**. More generally, latent knowledge is anything that a machine learning model knows (because it needs to in order to function) but that it doesn't directly output.

There is currently a [contest](https://www.alignmentforum.org/posts/QEYWkRoCn4fZxXQAY/prizes-for-elk-proposals) for techniques to [elicit latent knowledge](https://docs.google.com/document/u/0/d/1WwsnJQstPq91_Yh-Ch2XRL8H_EpsnjrC1dwZXR37PC8/edit) in AI systems. At a high level what this means is developing ways to ask machine learning models to explain their latent knowledge. So for instance you could imagine strapping a language model like [GPT-3](https://en.wikipedia.org/wiki/GPT-3) to WeatherBot and training it to answer questions about atmospheric science in addition to predicting the weather.

I submitted an entry to this contest, and some 
