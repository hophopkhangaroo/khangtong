---
layout: math
title: Almost Sure Convergence
usemathjax: true
description:
---

<p class="box def">
A sequence of random variables, $X_1, X_2,\ldots$ <strong>converges almost surely</strong> to a random variable $X$ if, for every $\varepsilon > 0,$
\[P(\lim_{n\rightarrow\infty}|X_n-X|<\varepsilon) = 1.\]
</p>

<p class="box theorem">
<strong>Theorem 5.6.1 (Strong Law of Large Numbers)</strong>
Let $X_1,X_2,\ldots$ be iid random variables weith $EX_i=\mu$ and $Var\,X_i=\sigma^2 < \infty,$ and define $\overline{X}_n=(1/n)\sum_{i=1}^n X_i.$ Then, for every $\varepsilon>0,$
\[P(\lim_{n\rightarrow\infty}|\overline{X}_n-\mu|<\varepsilon) = 1\]
That is, $\overline{X}_n$ converges almost surely to $\mu.$
</p>