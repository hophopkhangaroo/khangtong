---
layout: math
title: Distributions of Functions of a Random Variable
usemathjax: true
description:
---

If $X$ is a random variable with cdf $F_X(x)$, then any function of $X, g(X),$ is also a random variable. Let $Y = g(X).$ For any set $A$,
\\[P(Y \in A) = P(g(X) \in A)\\]

If we write $y = g(x)$, the function $g(x)$ defines a mapping from the original sample space of $X, \mathcal{X},$ to a new sample space $\mathcal{Y}.$ That is,
\\[g(x) : \mathcal{X} \rightarrow \mathcal{Y}\\]

We associate with $g$ an inverse mapping, denoted $g^{-1},$ which is a mapping from subsets of $\mathcal{Y}$ to subsets of $\mathcal{X},$ and is defined by 
\\[g^{-1}(A) = \\{x\in \mathcal{X} : g(x) = y \\}.\\]

\\[\begin{equation}
\label{eq:sample-space}
\mathcal{X} = \\{x : f_X(x) > 0\\} \;\; \text{and} \;\; \mathcal{Y} = \\{y : y = g(x) \text{ for some } x \in \mathcal{X}\\}.
\end{equation}\\]

<div class="box theorem">
<strong>Theorem 2.1.1</strong>
Let $X$ have cdf $F_X(x)$, let $Y = g(X),$ and let $\mathcal{X}, \mathcal{Y}$ be defined as in \ref{eq:sample-space}.<br>
a.) If $g$ is an increasing function on $\mathcal{X}, F_Y(y) = F_X(g^{-1}(y))$ for $y\in \mathcal{Y}.$ <br>
b.) If $g$ is a decreasing function on $\mathcal{X}$ and $X$ is a continuous random variable, $F_Y(y) = 1 - F_X(g^{-1}(y))$ for $y\in \mathcal{Y}.$
</div>

<div class="box theorem">
<strong>Theorem 2.1.2</strong>
Let $X$ have pdf $f_X(x)$ and let $Y = g(X)$, where $g$ is a monotone function. Let $\mathcal{X}$ and $\mathcal{Y}$ be defined by \ref{eq:sample-space}. Suppose that $f_X(x)$ is continuous on $\mathcal{X}$ and that $g^{-1}(y)$ has a continuous derivative on $\mathcal{Y}.$ Then the pdf of $Y$ is given by
\[f_Y(y) = 
\begin{cases}
f_X(g^{-1}(y))\left\vert \dfrac{d}{dy}g^{-1}(y)\right\vert & y\in \mathcal{Y} \\
0 & \text{otherwise.}
\end{cases}\]
</div>

<div class="box theorem">
<strong>Theorem 2.1.3</strong>
Let $X$ have a pdf $F_X(x),$ let $Y=g(X),$ and define the sample space $\mathcal{X}$ as in \ref{eq:sample-space}. Suppose there exists a partition, $A_0,A_1,\ldots,A_k$ of $\mathcal{X}$ such that $P(X\in A_0) = 0$ and $f_X(x)$ is continuous on each $A_i.$ Further, suppose there exist functions $g_1(x),\ldots,g_k(x),$ defined on $A_1,\ldots,A_k$ respectively, satisfying <br>
i.) $g(x) = g_i(x),$ for $x\in A_i,$ <br>
ii.) $g_i(x)$ is monotone on $A_i,$ <br>
iii.) The set $\mathcal{Y} = \{y : g_i(x) \text{ for some } x \in A_i\}$ is the same for each $i=1,\ldots, k,$ and <br>
iv.) $g_i^{-1}(y)$ has a continuous derivative on $\mathcal{Y}$, for each $i=1,\ldots,k.$<br>
Then
\[f_Y(y) = 
\begin{cases}
\sum_{i=1}^{k} f_X(g_i^{-1}(y))\left\vert\dfrac{d}{dy}g_i^{-1}(y)\right\vert & y \in \mathcal{Y} \\
0 & \text{otherwise.}
\end{cases}\]
</div>

<div class="box theorem">
<strong>Theorem 2.1.4 (Probability integral transformation)</strong>
Let $X$ have continuous cdf $F_X(x)$ and define the random variable $Y$ as $Y= F_X(X).$ Then $Y$ is uniformly distributed on $(0,1)$; that is, $P(Y\leq y) = y, 0<y<1.$
</div>