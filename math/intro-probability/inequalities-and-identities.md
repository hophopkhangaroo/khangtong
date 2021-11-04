---
layout: math
title: Inequalities and Identities
usemathjax: true
description:
---

# Probability Inequalities

<div class="box theorem">
<strong>Theorem 3.5.1 (Chebychev's Inequality)</strong>
Let $X$ be a random variable and let $g(x)$ be a nonnegative function. Then, for any $r>0,$
\[P(g(X)\geq r) \leq \frac{\E[g(X)]}{r}.\]
</div>

<div class="box theorem">
<strong>Theorem 3.5.2 (Markov's Inequality)</strong>
If $P(X \geq 0) = 1$ and $P(X = 0) < 1$, then, for any $r>0,$
\[P(X \geq r) \leq \frac{\E(X)}{r}\]
with equality if and only if $P(X = r) = p = 1-P(X = 0),\; 0<p\leq 1.$
</div>

# Identities

<div class="box theorem">
<strong>Theorem 3.5.3</strong>
Let $X_{\alpha,\beta}$ denote a $\text{gamma}(\alpha,\beta)$ random variable with pdf $f(x \vert \alpha,\beta),$ where $\alpha > 1$. Then for any constants $a$ and $b$,
\[P(a < X_{\alpha,\beta} < b) = \beta(f(a \vert \alpha, \beta) - f(b\vert \alpha, \beta)) + P(a<X_{\alpha-1,\beta} < b).\]
</div>

<div class="box theorem">
<strong>Lemma 3.5.4 (Stein's Lemma)</strong>
Let $X \sim n(\theta,\sigma^2),$ and let $g$ be a differentiable function statisfying $\E\vert g^{\prime}(X)\vert < \infty.$ Then
\[\E[g(X)(X-\theta)]= \sigma^2\E[g^{\prime}(X)].\]
</div>

<div class="box theorem">
<strong>Theorem 3.5.5</strong>
Let $\mathcal{X}_p^2$ deonte a chi-squared random variable with $p$ degrees of freedom. For any function $h(x),$
\[\E[h(\mathcal{X}_p^2)] = p\E\left(\frac{h(\mathcal{X}_{p+2}^2)}{\mathcal{X}_{p+2}^2}\right)\]
provided the expectations exist.
</div>

<div class="box theorem">
<strong>Theorem 3.5.6 (Hwang)</strong>
Let $g(x)$ be a function with $-\infty < \E[g(X)] < \infty$ and $-\infty < g(-1) < \infty.$ Then:<br>
a. If $X \sim \text{Poisson}(\lambda),$
\[\E[\lambda g(X)] = \E[Xg(X-1)].\]
b. If $X \sim \text{NegBinom}(r,p),$
\[\E[(1-p)g(X)] = \E\left(\frac{X}{r+X - 1}g(X-1)\right).\]
</div>