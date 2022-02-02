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

$X \sim Exp(\lambda).$ With *rate parameter* $\lambda.$

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

Sometimes the exponential distribution is described with a *scale parameter*, $\beta$, instead where $\beta=1/\lambda.$

$$
f(x\vert \beta) = 
\begin{cases}
\frac{1}{\beta} e^{-x/\beta}, & x\geq 0 \\
0, & \text{else}
\end{cases}
$$

# Gamma Distribution

Gamma function:
\\[\Gamma(\alpha) = \int_0^{\infty} t^{\alpha-1}e^{-t}\,dt.\\]
Properties:
\\[\Gamma(\alpha+1) = \alpha\Gamma(\alpha), \quad \alpha>0\\]
\\[\Gamma(n) = (n-1)! \quad \text{if $n$ is an integer}\\]
$X \sim Gamma(\alpha, \beta).$

\\[f(x \vert \alpha, \beta) = \frac{1}{\Gamma(\alpha)\beta^{\alpha}} x^{\alpha-1}e^{-x/\beta}, \quad 0 < x < \infty, \quad \alpha > 0, \quad \beta > 0.\\]

|----------|------------|
|\\[EX\\]  |\\[\alpha\beta\\]|
|\\[Var\,X\\]|\\[\alpha\beta^2\\]|
|\\[M_X(t)\\]|\\[\left(\frac{1}{1-\beta t}\right)^{\alpha}, \quad t< \frac{1}{\beta}\\]

*Note:* $X\sim Exp(\beta)$ is a special case of the gamma distribution when $\alpha=1.$

# Weibull Distribution

If $Y \sim Exp(\beta),$ then $X=Y^{1/\gamma} \sim Weibull(\gamma,\beta).$

\\[f_X(x \vert \gamma,\beta) = \frac{\gamma}{\beta}x^{\gamma-1}e^{-x^{\gamma}/\beta}, \quad 0 < x < \infty, \quad \gamma>0, \quad \beta>0.\\]
However, a reparameterization of $\beta$ gives us the more common pdf:
\\[f_X(x \vert \gamma,\beta) = \frac{\gamma}{\beta}\left(\frac{x}{\beta}\right)^{\gamma-1}e^{-(x/\beta)^{\gamma}}, \quad 0 < x < \infty, \quad \gamma>0, \quad \beta>0.\\]

|------------|--------------|
|\\[EX\\]    |\\[\beta\Gamma\left(1+\frac{1}{\gamma}\right)\\]|
|\\[Var\,X\\]|\\[\beta^2\left[\Gamma\left(1+\frac{2}{\gamma}\right)-\left(\Gamma^2\left(1+\frac{1}{\gamma}\right)\right)\right]\\]|
|\\[M_X(t)\\]|\\[\sum_{n=0}^{\infty} \frac{(t\beta)^n}{n!}\Gamma\left(1+\frac{n}{\gamma}\right),\quad \gamma\geq 1\\]

# Chi-Squared Distribution

Another special case of the gamma distribution is when $\alpha=p/2$ where $p$ is an integer and $\beta=2$ which has pdf
\\[f(x\vert p) = \frac{1}{\Gamma\left(\frac{p}{2}\right)2^{p/2}}x^{p/2-1}e^{-x/2}, \quad 0 < x < \infty\\]
which is called the chi-squared distribution with $p$ degrees of freedom. We write $X \sim \chi_p^2.$

|-------|-------|
|\\[EX\\]| \\[p\\]|
|\\[Var\,X\\]|\\[2p\\]|
|\\[M_X(t)\\]|\\[(1-2t)^{-p/2}, \quad t<\frac{1}{2}\\]|

# Normal Distribution

$X \sim N(\mu, \sigma^2)$

\\[f(x \vert \mu, \sigma^2) = \frac{1}{\sqrt{2\pi}\sigma}e^{-(x-\mu)^2/(2\sigma^2)}, \quad -\infty < x < \infty\\]

|-------|-------|
|\\[EX\\]| \\[\mu\\]|
|\\[Var\,X\\]|\\[\sigma^2\\]|
|\\[M_X(t)\\]|\\[\exp\left(\mu t + \sigma^2 t^2/2\right)\\]|

If $X\sim N(\mu,\sigma^2),$ then the random variable $Z=\displaystyle\frac{X-\mu}{\sigma}$ has an $N(0,1)$ distribution and is called the *standard normal*.
# Beta Distribution

$X\sim Beta(\alpha,\beta).$

\\[f(x \vert \alpha,\beta) = \frac{x^{\alpha-1}(1-x)^{\beta-1}}{B(\alpha,\beta)}, \quad 0< x < 1, \quad \alpha > 0\, \quad \beta > 0\\]
where $B(\alpha, \beta)$ denotes the beta function:
\\[B(\alpha,\beta) = \frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}.\\]

|-------|-------|
|\\[EX\\]| \\[\frac{\alpha}{\alpha+\beta}\\]|
|\\[Var\,X\\]|\\[\frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)}\\]|
|\\[M_X(t)\\]|\\[1 + \sum_{k=1}^{\infty}\left(\prod_{r=0}^{k-1} \frac{\alpha+r}{\alpha+\beta+r}\right)\frac{t^k}{k!}\\]|

# Cauchy Distribution
$X\sim Cauchy(\mu,\sigma)$

\\[f(x\vert\mu,\sigma) = \frac{1}{\sigma\pi\left(1+\left(\frac{x-\mu}{\sigma}\right)^2\right)}, \quad -\infty < x < \infty.\\]

|-------|-------|
|\\[EX\\]| Undefined|
|\\[Var\,X\\]|Undefined|
|\\[M_X(t)\\]|DNE|

# Lognormal Distribution
If $X$ is a random variable whose logarithm is normally distributed (ie, $\ln X \sim N(\mu,\sigma^2)$), then $X$ has a lognormal distribution. 

$X\sim Lognormal(\mu,\sigma^2).$

\\[f(x \vert \mu,\sigma^2) = \frac{1}{\sqrt{2\pi}\sigma x}e^{-(\ln x-\mu)^2/(2\sigma^2)},\quad 0 < x < \infty, \quad -\infty < \mu < \infty, \quad \sigma>0 \\]

|-------|-------|
|\\[EX\\]| \\[e^{\mu + (\sigma^2/2)}\\]|
|\\[Var\,X\\]|\\[e^{2(\mu+\sigma^2)}-e^{2\mu+\sigma^2}\\]|
|\\[M_X(t)\\]|\\[??\\]|

# Double Exponential Distribution

$X \sim DoubleExp(\mu\sigma).$

\\[f(x\vert\mu,\sigma) = \frac{1}{2\sigma}e^{-\|x-\mu\|/\sigma},\quad -\infty < x < \infty,\quad -\infty < \mu < \infty, \quad \sigma>0\\]

|-------|-------|
|\\[EX\\]| \\[\mu\\]|
|\\[Var\,X\\]|\\[2\sigma^2\\]|
|\\[M_X(t)\\]|\\[\frac{e^{\mu t}}{1-\sigma^2t^2},\quad \|t\|<\frac{1}{\sigma}\\]|

