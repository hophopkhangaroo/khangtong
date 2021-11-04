---
layout: math
title: Density and Mass Functions
usemathjax: true
description:
---

<p class="box def">
The <strong>probability mass function (pmf)</strong> of a discrete random variable $X$ is given by
\[f_X(x) = P(X = x) \text{ for all } x.\]
</p>

<p class="box def">
The <strong>probability density function (pdf)</strong>, $f_X(x)$, of a continuous random variable $X$ is the function that satisfies
\[F_X(x) = \int_{-\infty}^{x} f_X(t)\;dt \text{ for all } x.\] 
</p>

*A note on notation:* The expression "$X$ has distribution given by $F_X(x)$" is abbreviated symbolically by "$X \sim f_X(x),$" where we read the symbol "$\sim$" as "is distributed as." We can similarly write $X \sim f_X(x)$ or, if $X$ and $Y$ have the same distribution, $X \sim Y.$

<div class="box theorem">
<strong>Theorem 1.8.1</strong>
A function $F_X(x)$ is a pdf (or pmf) of a random variable $X$ if and only if <br>
a.) $f_X(x) \geq 0 \text{ for all } x.$ <br>
b.) $\sum_x f_X(x) = 1 \text{ (pmf) } \;\; \text{ or } \;\; \int_{-\infty}^{\infty}f_X(x)\,dx = 1 \text{ (pdf).}$
<div>