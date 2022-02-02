---
layout: math
title: The Delta Method
usemathjax: true
description:
---

<p class="box def">
If a function $g(x)$ has derivatives of order $r,$ that is, $g^{(r)}(x) = \frac{d^r}{dx^r}g(x)$ exists, then for any constant $a,$ the <strong>Taylor polynomial of order $r$ about $a$</strong> is
\[T_r(x) = \sum_{i=0}^r\frac{g^{(i)}(a)}{i!}(x-a)^i.\]
</p>

<p class="box theorem">
<strong>Theorem 5.8.1 (Taylor)</strong>
If $g^{(r)}(a)=\frac{d^r}{dx^r}g(x)\vert_{x=a}$ exists, then
\[\lim_{x\rightarrow a} \frac{g(x) - T_r(x)}{(x-a)^r} = 0.\]
</p>

<p class="box theorem">
<strong>Theorem 5.8.2 (Delta Method)</strong>
Let $Y_n$ be a sequence of random variables that satisfies $\sqrt{n}(Y_n-\theta) \rightarrow N(0, \sigma^2)$ in distribution. For a given function $g$ and a specific value of $\theta$, suppose that $g^{\prime}(\theta)$ exists and is not $0.$ Then
\[\sqrt{n}\left[g(Y_n)-g(\theta)\right]\rightarrow N(0,\sigma^2\left[g^{\prime}(\theta)\right]^2) \text{ in distribution.}\]
</p>

<p class="box theorem">
<strong>Theorem 5.8.3 (Second-order Delta Method)</strong>
Let $Y_n$ be a sequence of random variables that satisfies $\sqrt{n}(Y_n-\theta) \rightarrow N(0, \sigma^2)$ in distribution. For a given function $g$ and a specific value of $\theta$, suppose that $g^{\prime}(\theta)=0$ and $g^{\prime\prime}(\theta)$ exists and is not $0.$ Then
\[n\left[g(Y_n)-g(\theta)\right]\rightarrow \sigma^2\frac{g^{\prime\prime}(\theta)}{2}\chi_1^2 \;\;\text{ in distribution.}\]
</p>

<p class="box theorem">
<strong>Theorem 5.8.4 (Multivariate Delta Method)</strong>
Let $\mathbf{X}_1,\ldots,\mathbf{X}_n$ be a random sample with $E(X_{ij}) = \mu_i$ and $Cov(X_{ik},X_{jk})=\sigma_{ij}.$ For a given function $g$ with continuous first partial derivatives and a specific value of $\boldsymbol{\mu} = (\mu_1,\ldots,\mu_p)$ for which $\tau^2 = \sum\sum\sigma_{ij}\frac{\partial g(\boldsymbol{\mu})}{\partial\mu_i}\cdot\frac{\partial g(\boldsymbol{\mu})}{\partial\mu_j} > 0,$
\[\sqrt{n}\left[g(\overline{X}_1,\ldots,\overline{X}_s) - g(\mu_1,\ldots,\mu_p)\right] \rightarrow N(0, \tau^2) \text{ in distrrbution.}\]
</p>