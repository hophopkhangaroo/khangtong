---
layout: math
title: Location and Scale Families
usemathjax: true
description:
---

<div class="box theorem">
<strong>Theorem 3.4.1</strong>
Let $f(X)$ be any pdf and let $\mu$ and $\sigma>0$ be any given constants. Then the function
\[g(x\vert\mu,\sigma) = \frac{1}{\sigma}f\left(\frac{x-\mu}{\sigma}\right)\]
is a pdf.
</div>

<p class="box def">
Let $f(x)$ be any pdf. Then the family of pdfs $f(x-\mu),$ indexed by the parameter $\mu, \; -\infty<\mu<\infty,$ is called the <strong>location family</strong> with standard pdf $f(x)$ and $\mu$ is called the <strong>location parameter</strong> for the family.
</p>

<p class="box def">
Let $f(x)$ be any pdf. Then for any $\sigma>0,$ the family of pdfs $\frac{1}{\sigma}f(\frac{x}{\sigma}),$ indexed by the paramter $\sigma,$ is called the <strong>scale family</strong> with standard pdf $f(x)$ and $\sigma$ is called the <strong>scale parameter</strong> of the family.
</p>

<p class="box def">
Let $f(x)$ be any pdf. Then for any $\mu\; -\infty < \mu < \infty,$ and any $\sigma > 0,$ the family of pdfs $\frac{1}{\sigma}f\left(\frac{(x-\mu)}{\sigma}\right),$ indexed by the parameter $(\mu,\sigma)$, is called the <strong>location-scale family</strong> with standard pdf $f(x)$; $\mu$ is called the <strong>location parameter</strong> and $\sigma$ is called the <strong>scale parameter.</strong>
</p>

<div class="box theorem">
<strong>Theorem 3.4.2</strong>
Let $f(\cdot)$ be any pdf. Let $\mu$ be any real number, and let $\sigma$ be any positive real number. Then $X$ is a random variable with pdf $\frac{1}{\sigma}f\left(\frac{(x-\mu)}{\sigma}\right)$ if and only if there exists a random variable $Z$ with pdf $f(z)$ and $X = \sigma Z + \mu.$
</div>

<div class="box theorem">
<strong>Theorem 3.4.3</strong>
Let $Z$ be a random variable with pdf $f(z).$ Suppose $\E(Z)$ and $Var(Z)$ exist. If $X$ is a random variable with pdf $(\frac{1}{\sigma})f\left(\frac{(x-\mu)}{\sigma}\right),$ then
\[\E(X) = \sigma\E(Z) + \mu \;\; \text{ and } \;\; Var(X) = \sigma^2 Var(Z).\]
In particular, if $\E(Z) = 0$ and $Var(Z) = 1$, then $\E(X) = \mu$ and $Var(X) = \sigma^2.$
</div>