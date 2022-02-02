---
layout: math
title: Conditional Distributions and Independence
usemathjax: true
description:
---

<p class="box def">
Let $(X,Y)$ be a discrete bivariate random vector with joint pmf $f(x,y)$ and marginal pmfs $f_X(x)$ and $f_Y(y).$ For any $x$ such that $P(X=x)=f_X(x) >0,$ the <strong>conditional pmf of $Y$ given that $X=x$</strong> is the function of $y$ denoted by $f(y\vert x)$ and defined by
\[f(y|x) = P(Y=y | X=x) = \frac{f(x,y)}{f_X(x)}.\]
For any $y$ such that $P(Y=y)=f_Y(y) >0,$ the <strong>conditional pmf of $X$ given that $Y=y$</strong> is the function of $x$ denoted by $f(x\vert y)$ and defined by
\[f(x|y) = P(X=x | Y=y) = \frac{f(x,y)}{f_Y(y)}.\]
</p>

<p class="box def">
Let $(X|Y)$ be a continuous bivariate random vector with joint pdf $f(x,y)$ and marginal pdfs $f_X(x)$ and $f_Y(y).$ For any $x$ such that $f_X(x)>0,$ the <strong>conditional pdf of $Y$ given that $X=x$</strong> is the function of $y$ denoted by $f(y|x)$ and defined by 
\[f(y|x) = \frac{f(x,y)}{f_Y(y)},\]
For any $y$ such that $f_Y(y)>0,$ the <strong>conditional pdf of $X$ given that $Y=y$</strong> is the function of $x$ denoted by $f(x|y)$ and defined by 
\[f(x|y) = \frac{f(x,y)}{f_X(x)},\]
</p>

If $g(Y)$ is a function of $Y$, then the **conditional expected value of $g(Y)$ given that $X=x$** is denoted by $E(g(Y)\|x)$ and is given by 
\\[E(g(Y)|x) = \sum_y g(y)f(y|x) \\:\\: \text{ and } \\:\\: E(g(Y)|x) = \int_{-\infty}^{\infty} g(y)f(y|x)\,dy\\]
in the discrete and continuous cases, respectively.

The variance of the probability distribution described by $f(y\|x)$ is called the **conditional variance of $Y$ given $X=x$** and given by 
\\[Var(Y|x) = E(Y^2|x)-(E(Y|x))^2. \\]

<p class="box def">
Let $X(,Y)$ be a bivariate random vector with joint pdf or pmf $f(x,y)$ and marginal pdf or pmfs $f_X(x)$ and $f_Y(y).$ Then $X$ and $Y$ are called <strong>independent random variables</strong> if, for every $x,y\in\R,$
\[f(x,y) = f_X(x)f_Y(y).\]
</p>

If $X$ and $Y$ are independent, the conditional pdf of $Y$ given $X=x$ is

\begin{align\*}
	f(y\|x) &= \frac{f(x,y)}{f_X(x)} \\\\ 
	&= \frac{f_X(x)f_Y(y)}{f_X(x)} \\\\ 
	&= f_Y(y),
\end{align\*}
regardless of the value of $x.$

<p class="box theorem">
	<strong>Lemma 4.2.1</strong>
		Let $(X,Y)$ be a bivariate random vector with joint pdf or pmf $f(x,y).$ Then $X$ and $Y$ are independent random variables if and only if there exist functions $g(x)$ and $h(y)$ such that, for every $x,y\in\R,$
		\[f(x,y) = g(x)h(y).\]
</p>

<p class="box theorem">
<strong>Theorem 4.2.2</strong>
Let $X$ and $Y$ be independent random variables. <br>
a) For any $A\subset\R$ and $B\subset\R,\; P(X\in A,Y\in B)=P(X\in A)P(Y\in B)$; that is, the events $\{X\in A\}$ and $\{Y\in B\}$ are independent events. <br>
b) Let $g(x)$ be a function only of $x$ and $h(y)$ be a function only of $y.$ Then
\[E(g(X)h(Y)) = (Eg(X))(Eh(Y)).\]
</p>

<p class="box theorem">
<strong>Theorem 4.2.3</strong>
Let $X$ and $Y$ be independent random variables with moment generating functions $M_X(t)$ and $M_Y(t).$ Then the moment generating function of the random variable $Z=X+Y$ is given by
\[M_Z(t) = M_X(t)M_Y(t)\]
</p>

<p class="box theorem">
<strong>Theorem 4.2.4</strong>
Let $X\sim N(\mu,\sigma)$ and $Y\sim N(\gamma, \tau^2)$ be independent normal random variables. Then the random variable $Z=X+Y$ has a $N(\mu + \gamma, \sigma^2 + \tau^2)$ distribution.
</p>