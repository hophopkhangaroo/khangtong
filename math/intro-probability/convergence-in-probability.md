---
layout: math
title: Convergence in Probability
usemathjax: true
description:
---

<p class="box def">
A sequence of random variables, $X_1,X_2,\ldots,$ <strong>converges in probability</strong> to a random variable $X$ if, for every $\varepsilon > 0,$
\[\lim_{n\rightarrow\infty} P(|X_n-X|\geq\varepsilon)=0 \;\;\;\text{ or, equivalently, }\;\;\; \lim_{n\rightarrow\infty}P(|X_n-X|< \varepsilon) = 1.\]
</p>

<p class="box theorem">
<strong>Theorem 5.5.1 (Weak Law of Large Numbers)</strong>
Let $X_1,X_2,\ldots$ be iid random variables with $EX_i=\mu$ and $Var\,X=\sigma^2 < \infty.$ Define $\overline{X}_n =(1/n)\sum_{i=1}^nX_i.$ Then, for every $\varepsilon > 0,$
\[\lim_{n\rightarrow\infty} P(|\overline{X}_n-\mu| < \varepsilon) = 1\]
That is, $\overline{X}_n$ converges in probability to $\mu.$
</p>

<p class="box theorem">
<strong>Theorem 5.5.2</strong>
Suppose that $X_1,X_2,\ldots$ converges in probability to a random variable $X$ and that $h$ is a continuous function. Then $h(X_1),h(X_2),\ldots$ converges in probability to $h(X).$
</p>

