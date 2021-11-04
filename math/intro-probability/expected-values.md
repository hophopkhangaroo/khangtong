---
layout: math
title: Expected Values
usemathjax: true
description:
---

<p class="box def">
The <strong>expected value</strong> or <strong>mean</strong> of a random variable $g(X),$ denoted by $\E(g(X)),$ is
\[\E(g(X)) = 
\begin{cases}
\int_{-\infty}^{\infty} g(x) f_X(x)\, dx & \text{if } X \text{ is continuous} \\
\sum_{x\in\mathcal{X}} g(x)f_X(x) = \sum_{x\in\mathcal{X}} g(x) P(X=x) & \text{if } X \text{ is discrete}
\end{cases}\]
provided that the integral or sum exists.  If $\E|g(X)| = \infty,$ we say that $\E(g(X))$ does not exist.
</p>

<div class="box theorem">
<strong>Theorem 2.2.1</strong>
Let $X$ be a random variable and let $a,b,$ and $c$ be constants. Then for any functions $g_1(x)$ and $g_2(x)$ whose expectations exist, <br>
a.) $\E(ag_1(X) + bg_2(X) + c) = a\E(g_1(X)) + b\E(g_2(X)) + c$ <br>
b.) If $g_1(x) \geq 0$ for all $x,$ then $\E(g_1(X))\geq 0.$ <br>
c.) If $g_1(x) \geq g_2(x)$ for all $x,$ then $\E(g_1(X)) \geq \E(g_2(X)).$ <br>
d.) If $a \leq g_1(x) \leq b$ for all $x,$ then $a \leq E(g_1(X)) \leq b.$
</div>