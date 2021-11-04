---
layout: math
title: Continuous Distributions
usemathjax: true
description:
---

A random variable $X$ has a continuous distribution if its sample space is uncountable.

# Uniform Distribtution

$$
f(x\vert a,b) =
\begin{cases}
\frac{1}{b-a} & \text{if $ x \in [a,b]$} \\
0 & \text{otherwise}
\end{cases}
$$

|-----------|----------|
|\\[\E(X)\\]|\\[\frac{b+a}{2}\\]|
|\\[Var(X)\\]|\\[\frac{(b-a)^2}{12}\\]|
|\\[M_X(t)\\]|\\[\frac{e^{tb}-e^{ta}}{t(b-a)}\\]|

# Exponential Distribution

$X \sim Exp(\lambda).$

$$
f(x\vert \lambda) = 
\begin{cases}
\lambda e^{-\lambda x}, & x\geq 0 \\
0, & \text{else}
\end{cases}
$$

|-----------|----------|
|\\[\E(X)\\]|\\[\frac{1}{\lambda}\\]|
|\\[Var(X)\\]|\\[\frac{1}{\lambda^2}\\]|
|\\[M_X(t)\\]|\\[(1-t\lambda^{-1})^{-1}\\]|

# Gamma Distribution

# Weibull Distribution

# Chi-Squared Distribution

# Normal Distribution

# Beta Distribution

# Cauchy Distribution

# Lognormal Distribution

# Double Exponential Distribution

