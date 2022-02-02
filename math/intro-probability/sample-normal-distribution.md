---
layout: math
title: Sampling from the Normal Distribution
usemathjax: true
description:
---

<p class="box theorem">
<strong>Theorem 5.3.1</strong>
Let $X_1,\ldots,X_n$ be a random sample from a $N(\mu. \sigma^2)$ distribution, and let $\overline{X}= \frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n(X_i - \overline{X})^2.$ Then <br>
a) $\overline{X}$ and $S^2$ are independent random variables,<br>
b) $\overline{X}$ has a $N(\mu, \sigma^2/n)$ distribution,<br>
c) $\displaystyle\frac{(n-1)S^2}{\sigma^2}$ has a chi-squared distribution with $n-1$ degrees of freedom.
</p>

<p class="box theorem">
<strong>Lemma 5.3.2 (Facts about chi-squared random variables)</strong>
We use the notation $\chi_p^2$ to denote a chi-squared random variable with $p$ degrees of freedom.<br>
a) If $Z$ is a $N(0,1)$ random variable, then $Z^2 \sim \chi_1^2;$ that is, the square of a standard normal random variable is a chi-squared random variable. <br>
b) If $X_1,\ldots,X_n$ are independent and $X_i \sim \chi_{p_i}^2,$ then $X_1+ \cdots + X_n \sim \chi_{p_1+\cdots+p_n}^2;$ that is, independent chi-squared random variables add to a chi-sqared random variable, and the degrees of freedom also add.
</p>

<p class="box theorem">
<strong>Lemma 5.3.3</strong>
Let $X_j \sim N(\mu_j, \sigma_j^2), \; j = 1,\ldots, n,$ independent. For constants $a_{ij}$ and $b_{rj} \; (j=1,\ldots,n; \, i=1,\ldots,k; \, r=1,\ldots,m),$ where $k+m \leq n,$ define
\[U_i = \sum_{j=1}^n a_{ij}X_j, \; i=1,\ldots,k,\]
\[V_r = \sum_{j=1}^n b_{rj}X_j, \; r=1,\ldots,m.\]
a) The random variables $U_i$ and $V_r$ are independent if and only if $Cov(U_i,V_r)=0.$ Furthermore, $Cov(U_i, V_r) = \sum_{j=1}^n a_{ij}b_{rj}\sigma_j^2.$<br>
b) The random vectors $(U_1,\ldots,U_k)$ and $(V_1,\ldots,V_m)$ are independent if and only if $U_i$ is independent of $V_r$ for all pairs $i,r \; (i=1,\ldots,k; \, r = 1,\ldots,m).$
</p>

<p class="box def">
Let $X_1,\ldots,X_n$ be a random sample from a $N(\mu,\sigma^2)$ distribution. The quantity $\displaystyle\frac{\overline{X}-\mu}{S/\sqrt{n}}$ has a <strong>Student's t distribution</strong> with $n-1$ degrees of freedom. Equivalently, a random variable $T$ has a Student's $t$ distribution with $p$ degrees of freedom, and we write $T\sim t_p$ if it has pdf
\[f_T(t) = \frac{\Gamma\left(\frac{p+1}{2}\right)}{\Gamma\left(\frac{p}{2}\right)}\frac{1}{(p\pi)^{1/2}}\frac{1}{(1+t^2/p)^{(p+1)/2}}, \:\: -\infty < t < \infty.\]
</p>

<p class="box def">
Let $X_1,\ldots,X_n$ be a random sample from a $N(\mu_X,\sigma_X^2)$ population, and let $Y_1,\ldots,Y_m$ be a random sample from an independent $N(\mu_Y, \sigma_Y^2)$ population. The random variable $\displaystyle F=\frac{S_X^2/\sigma_X^2}{S_Y^2/\sigma_Y^2}$ has a <strong>Snedecor's F distribution</strong> with $n-1$ and $m-1$ degrees of freedom. Equivalently, the random variable $F$ has the $F$ distribution with $p$ and $q$ degrees of freedom if it has pdf
\[f_F(x) = \frac{\Gamma\left(\frac{p+q}{2}\right)}{\Gamma(\frac{p}{2})\Gamma(\frac{q}{2})}\left(\frac{p}{q}\right)^{p/2}\frac{x^{(p/2)-1}}{[1+(p/q)x]^{(p+q)/2}}, \:\: 0 < x < \infty.\]
</p>

<p class="box theorem">
<strong>Theorem 5.3.4</strong><br>
a) If $X\sim F_{p,q},$ then $1/X \sim F_{q,p};$ that is, the reciprocal of an $F$ random variable is again an $F$ random variable. <br>
b) If $X \sim t_q,$ then $X^2 \sim F_{1,q}.$<br>
c) If $X\sim F_{p,q},$ then $\displaystyle\frac{(p/q)X}{1+(p/q)X} \sim Beta\left(\frac{p}{2}, \frac{q}{2}\right).$
</p>