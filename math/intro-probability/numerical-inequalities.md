---
layout: math
title: Numerical Inequalities
usemathjax: true
description:
---

<p class="box theorem">
<strong>Lemma 4.7.1</strong>
Let $a$ and $b$ be any positive numbers, and let $p$ and $q$ be any positive numbers (necessarily greater than $1$) satisfying
\begin{equation}
\label{eq:lemma}
\frac{1}{p} + \frac{1}{q} = 1.
\end{equation}
Then
\[\frac{1}{p}a^p + \frac{1}{q}b^q \geq ab\]
with equality if and only if $a^p = b^q.$
</p>

<p class="box theorem">
<strong>Theorem 4.7.2 (H&ouml;lder's Inequality)</strong>
Let $X$ and $Y$ be any two random variables, and let $p$ and $q$ satisfy \ref{eq:lemma}. Then
\[|EXY| \leq E|XY| \leq (E|X|^p)^{1/p}(E|Y|^q)^{1/q}.\]
</p>

<p class="box theorem">
<strong>Theorem 4.7.3 (Cauchy-Schwarz Inequality)</strong>
For any two random variables $X$ and $Y,$
\[|EXY| \leq E|XY| \leq (E|X|^2)^{1/2}(E|Y|^2)^{1/2}.\]
</p>

<p class="box theorem">
<strong>Theorem 4.7.4 (Minkowski's Inequality)</strong>
Let $X$ and $Y$ be any two random variables. Then for $1\leq p < \infty,$
\[[E|X+Y|^p]^{1/p} \leq [E|X|^p]^{1/p} + [E|Y|^p]^{1/p}\]
</p>