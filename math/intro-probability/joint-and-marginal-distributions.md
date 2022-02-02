---
layout: math
title: Joint and Marginal Distributions
usemathjax: true
description:
---

<p class="box def">
An <strong>n-dimensional random vector</strong> is a function from a sample space $S$ into $\R^n,$ $n$-dimensional Euclidean space. 
</p>

<p class="box def">
Let $(X,Y)$ be a discrete bivariate random vector. Then the function $f(x,y)$ from $\R^2$ into $\R$ defined by $f(x,y)=P(X=x,Y=y)$ is called the <strong>joint probability mass function</strong> or <strong>joint pmf</strong> of $(X,Y).$ If it is necessary to stress the fact that $f$ is the joint pmf of the vector $(X,Y)$ rather than some other vector, the notation $f_{X,Y}(x,y)$ will be used.
</p>

<p class="box theorem">
<strong>Theorem 4.1.1</strong>
Let $(X,Y)$ be a discrete bivariate random vector with joint pmf $f_{X,Y}(x,y).$ Then the marginal pmfs of $X$ and $Y,$ $f_X(x)=P(X=x)$ and $f_Y(y)=P(Y=y),$ are given by
\[f_X(x) = \sum_{y\in\R} f_{X,Y}(x,y)\:\: \text{ and } \:\:f_Y(y) = \sum_{x\in\R}f_{X,Y} (x,y).\]
</p>

*Note:* The marginal distributions of $X$ and $Y$, described by the marginal pmfs $f_X(x)$ and $f_Y(y),$ do not completely describe the joint distribution of $X$ and $Y.$ There can be many different joint pmfs for the same set of marginal pmfs. 

<p class="box def">
A function $f(x,y)$ from $\R^2$ into $\R$ is called a <strong>joint probability density function</strong> or <strong>joint pdf</strong> of the continuous bivariate random vector $(X,Y)$ if, for every $A \subset \R^2,$
\[P((X,Y)\in A) = \iint\limits_{A} f(x,y)\,dxdy.\]
</p>

The joint probability distribution of $(X,Y)$ can be completely described with the <strong>joint cdf</strong> rather than with the joint pmf or the joint pdf. The joint cdf is the function $F(x,y)$ defined by 
\\[F(x,y) = \int_{-\infty}^x \int_{-\infty}^y f(s,t)\,dtds\\]
From the bivariate Fundamental Theorem of Calculus, this implies that 
\\[\frac{\partial^2F(x,y)}{\partial x \partial y} = f(x,y)\\]
at continuity points of $f(x,y).$