---
layout: math
title: Distribution Functions
usemathjax: true
description:
---

<p class="box def">
The <strong>cummulative distribution function</strong> or <strong>cdf</strong> of a random variable $X$, denoted by $F_X(x),$ is defined by 
\[F_X(x) = P_X(X\leq x), \; \text{ for all }x.\]
</p>

<div class="box theorem">
<strong>Theorem 1.7.1</strong>
The function $F(x)$ is a cdf if and only if the following three conditions hold: <br>
a.) $\lim_{x\rightarrow -\infty} F(x) = 0$ and $\lim_{x\rightarrow \infty} F(x) = 1.$ <br>
b.) $F(x)$ is a nondecreasing function of $x$. <br>
c.) $F(x)$ is right continuous; that is, for every number $x_0, \lim_{x\rightarrow x_0^+} F(x) = F(x_0).$
</div>

*Recall:* The partial sum of the geometric series is 
\\[\sum_{k=1}^n t^{k-1} = \frac{1-t^n}{1-t}, \; t\neq 1.\\]

<p class="box def">
A random variable $X$ is <strong>continuous</strong> if $F_X(x)$ is a continuous function of $x.$ A random variable $X$ is <strong>discrete</strong> if $F_X(x)$ is a step function of $x.$
</p>

<p class="box def">
The random variables $X$ and $Y$ are <strong>identically distributed</strong> if, for every set $A\in \mathcal{B^1},P(X\in A) = P(Y \in A).$
</p>

*Note:* Two random variables that are identically distributed are not necessarily equal. I.e., identically distributed does not imply $X=Y.$

<div class="box theorem">
<strong>Theorem 1.7.2</strong>
The following two statements are equivalent: <br>
a.) The random variables $X$ and $Y$ are identically distributed. <br>
b.) $F_X(x) = F_Y(x)$ for every $x.$
</div>
