---
layout: math
title: Convergence in Distribution
usemathjax: true
description:
---

<p class="box def">
A sequence of random variables, $X_1,X_2,\ldots$ <strong>converges in distribution</strong> to a random variable $X$ if
\[\lim_{n\rightarrow\infty}F_{X_n}(x) = F_X(x)\]
at all points $x$ where $F_X(x)$ is continuous.
</p>

<p class="box theorem">
<strong>Theorem 5.7.1</strong>
If the sequence of random variables, $X_1,X_2,\ldots$ converges in probability to a random variable $X$, the sequence also converges in distribution to $X.$
</p>

<p class="box theorem">
<strong>Theorem 5.7.2 (Central Limit Theorem)</strong>
Let $X_1,X_2,\ldots$ be a sequence of iid random variables whose mgfs exist in a neighborhood of $0$ (that is, $M_{X_i}(t)$ exists for $|t|< h,$ for some positive $h$). Let $EX_i=\mu$ and $Var\,X_i = \sigma^2 > 0.$ (Both $\mu$ and $\sigma^2$ are finite since the mgf exists.) Define $\overline{X}_n=\frac{1}{n}\sum_{i=1}^n X_i.$ Let $G_n(x)$ denote the cdf of $\displaystyle\frac{\overline{X}_n-\mu}{\sigma/\sqrt{n}}.$ Then, for any $x,\; -\infty< x <\infty,$
\[\lim_{n\rightarrow\infty}G_n(x) = \int_{-\infty}^x \frac{1}{\sqrt{2\pi}}e^{-y^2/2}\,dy\]
That is, $\displaystyle\frac{\overline{X}_n-\mu}{\sigma/\sqrt{n}}$ has a limiting standard normal distribution.
</p>

<p class="box theorem">
<strong>Theorem 5.7.3 (Stronger form of the Central Limit Theorem)</strong>
Let $X_1,X_2,\ldots$ be a sequence of iid random variables with $EX_i=\mu$ and $0 < Var\,X_i = \sigma^2 < \infty.$ Define $\overline{X}_n=\frac{1}{n}\sum_{i=1}^n X_i.$ Let $G_n(x)$ denote the cdf of $\displaystyle\frac{\overline{X}_n-\mu}{\sigma/\sqrt{n}}.$ Then, for any $x,\; -\infty< x <\infty,$
\[\lim_{n\rightarrow\infty}G_n(x) = \int_{-\infty}^x \frac{1}{\sqrt{2\pi}}e^{-y^2/2}\,dy\]
That is, $\displaystyle\frac{\overline{X}_n-\mu}{\sigma/\sqrt{n}}$ has a limiting standard normal distribution.
</p>

<p class="box theorem">
<strong>Theorem 5.7.4 (Slutsky's Theorem)</strong>
If $X_n\rightarrow X$ in distribution and $Y_n\rightarrow c,$ a constant, in probability, then <br>
a) $Y_nX_n \rightarrow cX$ in distribution. <br>
b) $X_n + Y_n \rightarrow X+c$ in distribution.
</p>