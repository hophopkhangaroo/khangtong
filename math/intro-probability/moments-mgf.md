---
layout: math
title: Moments and Moment Generating Functions
usemathjax: true
description:
---

<p class="box def">
For each integer $n$, the $n$th <strong>moment</strong> of $X$ (or $F_X(x)),\mu_n^{'},$ is 
\[\mu_n^{'} = \E(X^n)\]
The $n$th <strong>central moment</strong> of $X, \mu_n,$ is 
\[\mu_n = \E(X-\mu)^n\]
where $\mu = \mu_1^{'}=\E(X).$
</p>

<p class="box def">
The <strong>variance</strong> of a random variable $X$ is its second central moment, $Var(X) = \E(X-\E(X))^2.$ The positive square root of $Var(X)$ is the <strong>standard deviation</strong> of $X.$
</p>

<div class="box theorem">
<strong>Theorem 2.3.1</strong>
If $X$ is a random variable with finite variance, then for any constants $a$ and $b$,
\[Var(aX+b) = a^2Var(X)\]
</div>

<p class="box def">
Let $X$ be a random variable with cdf $F_X.$ The <strong>moment generating function (mgf)</strong> of $X$ (or $F_X$), denoted by $M_X(t),$ is 
\[M_X(t) = \E(e^{tX})\]
provided that the expectation exists for $t$ in some neighborhood of $0.$ If the expectation does not exist in a neighborhood of $0,$ then we say that the moment generating function does not exist.<br>
More explicitly, we can write the mgf of $X$ as
\[M_X(t) = \int_{\infty}^{\infty}e^{tx}f_X(x)\,dx \;\;\;\;\text{ if $X$ is continuous}\]
or
\[M_X(t) = \sum_x e^{tx}P(X=x) \;\;\;\; \text{ if $X$ is discrete.}\]
</p>

<div class="box theorem">
<strong>Theorem 2.3.2</strong>
If $X$ has mgf $M_X(t),$ then
\[\E(X^n) = M_X^{(n)}(0),\]
where we define 
\[M_X^{(n)}(0) = \dfrac{d^n}{dt^n}M_X(t) \bigg\vert_{t=0}\]
That is, the $n$th moment is equal to the $n$th derivative of $M_X(t)$ evaluated at $t=0.$
</div>

<div class="box theorem">
<strong>Theorem 2.3.3</strong>
Let $F_X(x)$ and $F_Y(y)$ be two cdfs, all of whose moments exist. <br>
a.) If $X$ and $Y$ have bounded support, then $F_X(u)=F_Y(u)$ for all $u$ if and only if $\E(X^r) = \E(Y^r)$ for all integers $r=0,1,2,\ldots$ <br>
b.) If the moment generating function exists and $M_X(t) = M_Y(t)$ for all $t$ in some neighborhood of $0,$ then $F_X(u) = F_Y(u)$ for all $u.$
</div>

<div class="box theorem">
<strong>Theorem 2.3.4 (Convergence of mgfs)</strong>
Suppose $\{X_i, i=1,2,\ldots\}$ is a sequence of random variables, each with mgf $M_{X_i}(t).$ Furthermore, suppose that
\[\lim_{i \rightarrow \infty} M_{X_i}(t) = M_X(t), \;\;\;\; \text{for all $t$ in a neighborhood of $0,$}\]
and $M_X(t)$ is a mgf. Then there is a unique cdf $F_X$ whose moments are determined by $M_X(t)$ and, for all $x$ where $F_X(X)$ is continuous, we have
\[\lim_{i\rightarrow\infty} F_{X_i}(x) = F_X(x).\]
That is, convergence for $|t|<h$, of mgfs to an mgf implies convergence of cdfs.
</div>

<div class="box theorem">
<strong>Lemma 2.3.5</strong>
Let $a_1,a_2,\ldots$ be a sequence of numbers converging to $a,$ that is, $\lim_{n\rightarrow\infty} a_n=a.$ Then
\[\lim_{n\rightarrow\infty}\left(1+\frac{a_n}{n}\right)^n = e^a.\]
</div>

<div class="box theorem">
<strong> Theorem 2.3.6</strong>
For any constants $a$ and $b$, the mgf of the random variable $aX+b$ is given by 
\[M_{aX+b}(t) = e^{bt}M_X(at).\]
</div>