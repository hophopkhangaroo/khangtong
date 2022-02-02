---
layout: math
title: Hierarchical Models and Mixture Distributions
usemathjax: true
description:
---

<p class="box theorem">
<strong>Theorem 4.4.1</strong>
If $X$ and $Y$ are any two random variables, then 
\[EX = E(E(X|Y)),\]
provided that the expectations exist.
</p>

<p class="box def">
A random variable $X$ is said to have a <strong>mixture distribution</strong> if the distribution of $X$ depends on a quantity that also has a distribution.
</p>

<p class="box theorem">
<strong>Theorem 4.4.2 (Conditional Variance Identity)</strong>
For any two random variables $X$ and $Y,$
\[Var(X) = E(var(X|Y)) + Var(E(X|Y)),\]
provided that the expectations exist.
</p>