---
layout: math
title: Functional Inequalities
usemathjax: true
description:
---

<p class="box def">
A function $g(x)$ is <strong>convex</strong> if for all $x$ and $y$, and $0<\lambda<1,$ we have that 
\[g(\lambda x +(1-\lambda)y) \leq \lambda g (x) + (1-\lambda)g(y).\]  The function $g(x)$ is <strong>concave</strong> if $-g(x)$ is convex.
</p>

<p class="box theorem">
<strong>Theorem 4.8.1 (Jensen's Inequality)</strong>
For any random variable $X,$ if $g(x)$ is a convex function, then 
\[Eg(X) \geq g(EX).\]
Equality holds if and only if, for every line $a + bx$ that is tangent to $g(x)$ at $x=EX,\; P(g(X) = a + bX) = 1.$
</p>

<p class="box theorem">
<strong>Theorem 4.8.2 (Covariance Inequality)</strong>
Let $X$ be any random variable and $g(x)$ and $h(x)$ any functions such that $Eg(X), \; Eh(X),$ and $E(g(X)h(X))$ exist. <br>
a) If $g(x)$ is a nondecreasing function and $h(x)$ is a nonincreasing function, then 
\[E(g(X)h(X)) \leq (Eg(X))(Eh(X)).\]
b) If $g(x)$ and $h(x)$ are either both nondecreasing or both nonincreasing, then 
\[E(g(X)h(X)) \geq (Eg(X))(Eh(X)).\]
</p>