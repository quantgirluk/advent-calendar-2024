---
title: "Advent Calendar 2024 Day 4: Brownian Motion"
date: 2024-12-04
tags: 
  - "advent"
  - "mathematics"
  - "python"
  - "statistics"
  - "visualisation"
coverImage: "atkin-and-thyme-christmas-wooden-village-advent-calendar-1024023_1-edited.jpg"
---


### Day 4: Brownian Motion

Brownian motion or Brownian movement generally refers to the random motion of [particles](https://en.wikipedia.org/wiki/Particle) suspended in a medium (a [liquid](https://en.wikipedia.org/wiki/Liquid) or a [gas](https://en.wikipedia.org/wiki/Gas)). It is named after the Scottish botanist [Robert Brown](https://en.wikipedia.org/wiki/Robert_Brown_\(botanist,_born_1773\)), who first described the phenomenon in 1827, while looking through a microscope at [pollen](https://en.wikipedia.org/wiki/Pollen) of the plant _[Clarkia pulchella](https://en.wikipedia.org/wiki/Clarkia_pulchella)_ immersed in water. He saw something like this:

<iframe width="560" height="315" src="https://www.youtube.com/embed/R5t-oA796to?si=n03dqKMom0-eA093" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

In mathematics, Brownian motion is described by the [Wiener process](https://en.wikipedia.org/wiki/Wiener_process), a continuous-time [stochastic process](https://en.wikipedia.org/wiki/Stochastic_process) named after American computer scientist, mathematician, and philosopher [Norbert Wiener](https://en.wikipedia.org/wiki/Norbert_Wiener). It is probably the most well-known [Lévy processes](https://en.wikipedia.org/wiki/L%C3%A9vy_process) ([càdlàg](https://en.wikipedia.org/wiki/C%C3%A0dl%C3%A0g) stochastic processes with [stationary](https://en.wikipedia.org/wiki/Stationary_increments) [independent increments](https://en.wikipedia.org/wiki/Independent_increments)) since occurs frequently in pure and applied mathematics, [economics](https://en.wikipedia.org/wiki/Economy) and [physics](https://en.wikipedia.org/wiki/Physics).

- ![](images/robert_brown.png)


#### Definition

A standard (one dimensional) Wiener process (or Brownian motion) is a stochastic process $W =\{W(t), t\geq 0\},$ characterised by the following four properties:

1\. $W(0) = 0$

2\. $W(t)-W(s) \sim N(0, t-s),$ for any $0\leq s \leq t$

3\. $W$ has independent increments

4\. $W$ is almost surely continuous.

![](images/tempImageRWyL8N.jpg)

A standard d−dimensional Wiener process is a vector-valued stochastic process defined as

$$W(t) = (W_1(t) ,W_2(t), \cdots, W_d(t)), \qquad t\geq 0,$$  
whose components $W_i$ are independent, standard one-dimensional Wiener processes.

![](images/tempImageaD4GRp.jpg)

#### 🔔 Random Facts 🔔

- In 1905, Albert Einstein’s published _Investigations on the Theory of Brownian Movement_ a groundbreaking work that provided a deep theoretical explanation of Brownian motion. He developed a mathematical framework linking the seemingly random motion of particles to the kinetic theory of heat, thereby confirming the existence of atoms and molecules as physical entities. He derived an expression that related the diffusion coefficient of particles to measurable properties such as temperature, viscosity, and particle size, enabling experimental validation.

![This image has an empty alt attribute; its file name is tempImageeAsG3y.jpg](images/image.jpeg)

A copy of the original books is available [online](https://archive.org/details/investigationont0000albe/page/n5/mode/2up) and you can even buy a [modern edition on Amazon](https://www.amazon.co.uk/Investigations-Theory-Brownian-Movement-Physics/dp/0486603040)!

- In 1923, Norbert Wiener formally proved the existence of the Wiener process. Its mathematical framework indirectly influenced Richard Feynman’s path integral formulation of quantum mechanics. The Wiener process provides a probabilistic foundation for simulating quantum particle paths, as the sum over all possible paths in Feynman's formulation is conceptually akin to the summation over random Brownian trajectories. 

- The Wiener process can be constructed as the [scaling limit](https://en.wikipedia.org/wiki/Scaling_limit) of a [Random Walk](https://en.wikipedia.org/wiki/Random_walk). This is known as Donsker's theorem. Check out my previous [post](https://quantgirl.blog/donsker-random-walk/) about this construction.

- Like the Random Walk, the Wiener process is recurrent in one or two dimensions (meaning that it returns almost surely to any fixed [neighborhood](https://en.wikipedia.org/wiki/Neighborhood_\(mathematics\)) of the origin infinitely often) whereas it is not recurrent in dimensions three and higher.

- The Brownian motion, has significant applications in finance, tracing back to French mathematician [Louis Bachelier’s](https://en.wikipedia.org/wiki/Louis_Bachelier) pioneering 1900 thesis, _[Theory of Speculation](https://www.investmenttheory.org/uploads/3/4/8/2/34825752/emhbachelier.pdf)_. Bachelier was the first to apply the mathematics of Brownian motion to model stock price movements, preceding Einstein’s formalisation of the phenomenon. His work introduced the concept of price fluctuations as a random walk, laying the foundation for modern financial mathematics. Today, the Wiener process is a key component of models like the Black-Scholes equation for option pricing and is used extensively to model asset prices, interest rates, and risk in stochastic calculus frameworks.

#### More to Read

- [Feynman, Richard (1964).](https://www.feynmanlectures.caltech.edu/I_41.html) ["The Brownian Movement"](https://feynmanlectures.caltech.edu/I_41.html). _The Feynman Lectures of Physics, Volume I_. p. 41.

- [Discontinuous Structure of Matter](https://www.nobelprize.org/prizes/physics/1926/perrin/lecture/), Jean Baptiste Perrin Nobel Lecture ["The Nobel Prize in Physics 1926"](https://www.nobelprize.org/prizes/physics/1926/perrin/lecture/). _NobelPrize.org_. Retrieved 29 May 2019.

- [Brownian Motion Notebook](https://quantgirluk.github.io/Understanding-Quantitative-Finance/brownian_motion.html) (part of my series of notes exploring concepts with Python)

P.s. If you are curious about probability distributions visit the [Advent Calendar 2023](https://quantgirl.blog/advent-calendar-2023/) ✨
