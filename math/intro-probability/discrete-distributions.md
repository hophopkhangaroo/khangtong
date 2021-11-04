---
layout: math
title: Discrete Distributions
usemathjax: true
description:
---

A random variable $X$ is said to have a discrete distribution if its sample space is countable. 

*Note on notation:* When talking about parametric distributions, where the distribution is dependent on the value of the parameter, we use the symbol "$\vert$", read as "given", after the random variable to emphasize dependence of the distribution on the parameters. In cases where there is no ambiguity, the parameters are sometimes omitted to avoid clutter.

# Discrete Uniform Distribution
A random variable $X$ has a discrete uniform distribution $X\sim (1,N)$ if its pmf is
\\[P(X = x \vert N) = \frac{1}{N}, \;\; x = 1,2,\ldots, N\\]
where $N$ is a specified integer.

\\[E(X) = \frac{N + 1}{2}, \;\; Var(X) = \frac{(N+1)(N-1)}{12}\\]
\\[ M_X(t) = \frac{e^{at} - e^{(b+1)t}}{(b-a+1)(1-e^t)}\\]

# Hypergeometric Distribution

Imagine that there is a large urn filled with $n$ balls, $m$ of whom are red and $n-m$ of whom are blue. Suppose we reach into the urn and grab $k$ balls at random (all at once; i.e. without replacement). Let $X$ denote the amount of red balls we choose. Then $X \sim \text{HyperGeom}(n,m,k)$ has a hypergeometric distribution with pmf

\\[P(X=x \vert n,m,k) = \frac{ {m \choose x} {n-m \choose k-x} }{ {n \choose k} }, \;\; x = 0,1,\ldots,k.\\]

There are $n \choose k$ ways to choose $k$ balls from $n$ total balls. We must choose $x$ red balls and there are $m \choose x$ ways to do so. The remaining $k-x$ balls must be blue and there are $n-m \choose k-x$ ways to choose them.


|:-----------|---------------|
|  \\[E(X)\\] | \\[\frac{km}{n}\\] |
| \\[Var(X)\\] | \\[\frac{km}{n}\left(\frac{(n-m)(n-k)}{n(n-1)} \right)\\] |
| \\[M_X(t)\\] | \\[\text{you don't wanna know}\\]| 


# Bernoulli Distribution

A Bernoulli trial is a trial with only 2 possible outcomes. A random variable $X$ has a $\text{Bernoulli}(p)$ distribution if for $0\leq p \leq 1,$

$$
X = \begin{cases}
	1 & \text{with probability $p$ } \\
	0 & \text{with probability $1-p$}
\end{cases}
$$

|----------|------------|
|\\[\E(X)\\]| \\[p\\]   |
|\\[Var(X)\\]| \\[p(1-p)\\] |
| \\[M_X(t)\\]|\\[1-p+pe^t\\]|

# Binomial Distribution

$X \sim \text{Binomial}(n,p).$

\\[P(X = x\vert n,p) = {n \choose x} p^x(1-p)^{n-x}, \;\; x = 0,1,2,\ldots,n\\]

<div class="box theorem">
<strong>Theorem 3.1.1 (Binomial Theorem)</strong>
For any real numbers $x$ and $y$ and integer $n\geq 0,$
\[(x+y)^n = \sum_{i=0}^n {n \choose i} x^i y^{n-i}.\]
</div>

|-------|--------|
|\\[\E(X)\\]| \\[np\\]|
|\\[Var(X)\\]| \\[np(1-p)\\]|
|\\[M_X(t)\\]| \\[ [pe^t + (1-p)]^n\\]|

# Poisson Distibution

$X \sim \text{Poisson}(\lambda).$

\\[P(X=x\vert \lambda) = \frac{e^{-\lambda}\lambda^x}{x!}, \;\; x= 0,1,\ldots\\]

|----------|----------|
|\\[\E(X)\\]| \\[\lambda\\]|
|\\[Var(X)\\]| \\[\lambda\\]|
|\\[M_X(t)\\]| \\[e^{\lambda(e^t-1)}\\]|

# Negative Binomial Distibution

$X$ denotes the trial at which the $r$th success occurs.

$X \sim \text{NegativeBinomial}(r,p).$

\\[P(X=x\vert r,p) = {x-1 \choose r-1} p^r (1-p)^{x-r}, \;\; x = r, r+1, \ldots\\]

|------------|-------------|
|\\[\E(X)\\]| \\[\frac{r(1-p)}{p}\\]|
|\\[Var(X)\\]| \\[\frac{r(1-p)}{p^2}\\]|

# Geometric Distribution

$X$ denotes the trial at which the first success occurs.

$X \sim \text{Geom}(p).$

\\[P(X = x\vert p) = p(1-p)^{x-1}, \;\; x = 1, 2, \ldots\\]

|----------|----------|
|\\[\E(X)\\]| \\[\frac{1}{p}\\]|
|\\[Var(X)\\]| \\[\frac{1-p}{p^2}\\]|
|\\[M_X(t)\\]| \\[\frac{pe^t}{1-(1-p)e^t}, \;\; t < -\ln (1-p)\\]|
