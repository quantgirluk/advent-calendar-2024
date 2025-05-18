---
title: "Advent Calendar 2024 Day 6: Geometric Brownian Motion"
date: 2024-12-06
tags: 
  - "advent"
  - "mathematics"
  - "python"
  - "statistics"
  - "visualisation"
coverImage: "atkin-and-thyme-christmas-wooden-village-advent-calendar-1024023_1-edited.jpg"
---


### Day 5: Geometric Brownian Motion

Today we keep with variations of the Brownian motion! Geometric Brownian Motion (GBM) is a widely used stochastic process in mathematical finance, economics, and other disciplines to model the dynamics of positive variables that evolve over time under uncertainty, such as stock prices, interest rates, and commodity prices. The advantage of modelling through this process lies in its universality, as it represents an attractor of more complex models that exhibit non-ergodic dynamics.

![](images/image-4.tif)

#### Definition

The Geometric Brownian motion can be defined by the following Stochastic Differential Equation (SDE)

$$dX\_t = \mu X\_t dt + \sigma X\_t dW\_t, \quad t >0,$$

with initial condition $X\_0 =x\_0>0$, and constant parameters $\mu\in \mathbb{R}$, $\sigma>0$. Here, $W\_t$ denotes a standard Brownian motion.

In order to find its solution, let us set $Y\_t = \ln(X\_t)$. Then, Ito's formula implies

$$Y\_t = Y\_0 + \left( \mu-\frac{1}{2}\sigma^2 \right)t + \sigma W\_t,$$

or equivalently

$$\ln(X\_t) = \ln(x\_0) + \left( \mu-\frac{1}{2}\sigma^2 \right)t + \sigma W\_t.$$

From this expression, we obtain the solution as follows:

$$X\_t = x\_0 \exp \left\{ \left( \mu-\frac{1}{2}\sigma^2 \right)t + \sigma W\_t \right\}, \qquad t\geq 0.$$

Thus, for each $t>0$, the variable $\ln (X\_t)|X\_0$ (which will be denoted simply by $\ln(X\_t)$) follows a normal distribution –since it can be expressed as a scaled marginal of the Brownian motion plus a deterministic part. Using the properties of the standard Brownian Motion we can calculate its expectation and variance, and verify that

$$ \ln(X\_t) \sim \mathcal{N}\left(\ln(x\_0) + \left( \mu-\frac{1}{2}\sigma^2 \right)t, \sigma^2 t\right ),$$

and consequently $X\_t$ follows a [Log-normal distribution](https://en.wikipedia.org/wiki/Log-normal_distribution).

![](images/image-5.tif)

#### 🔔 Random Facts 🔔

- In 1952, Paul Samuelson and Robert Merton adapted the Wiener process into what we now recognise as Geometric Brownian Motion. Their modifications addressed the (so-called) shortcoming of the Bachelier’s model by ensuring that the process remains positive.

![](images/image-8.tif)

- GBM serves as the foundation for the famous Black-Scholes-Merton model for option pricing. 

![](images/image-6.tif)

- The asymptotic properties of geometric Brownian motion (GBM) are determined by the quantity $\mu− \frac{\sigma^2}{2}$:

- **$\mu− \frac{\sigma^2}{2} > 0$**: As $t$ approaches infinity, $X\_t$ approaches infinity with probability 1

- **$\mu− \frac{\sigma^2}{2} < 0$**: As $t$ approaches infinity, $X\_t$ approaches zero with probability 1

- **$\mu− \frac{\sigma^2}{2} = 0$**: As $t$ approaches infinity, $X\_t$ has no limit with probability 1 

![](images/image-7.tif)

#### More to Read

- [L. Bachelier, “Theory of Speculation: The Origins of Modern Finance,” Princeton University Press, Princeton, 1900.](https://www.investmenttheory.org/uploads/3/4/8/2/34825752/emhbachelier.pdf)

- [Samuelson, Paul A.. “Rational Theory of Warrant Pricing.” (2015).](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.unisalento.it/documents/20152/615543/Samuelson%2BRational%2BTheory%2Bof%2BWarrant%2BPricing.pdf/290dcd3c-9c3d-3cc2-cc28-353135ceab54%3Fversion%3D1.0%26download%3Dtrue&ved=2ahUKEwjI26z_sZOKAxXRSUEAHZVcBA0QFnoECBsQAQ&usg=AOvVaw3BnrpqbnPygqd8TgHizKIN)

- [Brief History of the Black-Scholes-Merton Model](https://quantgirl.blog/brief-history-of-the-black-scholes-merton-model/)

- [Geometric Brownian Motion Python Notebook](https://quantgirluk.github.io/Understanding-Quantitative-Finance/geometric_brownian_motion.html) (part of my series of notes exploring concepts with Python)

- Stojkoski, V.; Sandev, T.; Basnarkov, L.; Kocarev, L.; Metzler, R. Generalised Geometric Brownian Motion: Theory and Applications to Option Pricing. _Entropy_ **2020**, _22_, 1432. https://doi.org/10.3390/e22121432

P.s. If you are curious about probability distributions visit the [Advent Calendar 2023](https://quantgirl.blog/advent-calendar-2023/) ✨
