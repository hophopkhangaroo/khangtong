---
layout: math
title: Multivariate Distributions
usemathjax: true
description:
---

*A note on notation:* We will use boldface letters to denote multiple variates. So we write $\mathbf{X}$ to denote the random variables $X_1,\ldots,X_n$ and $\mathbf{x}$ to denote the sample $x_1,\ldots,x_n.$ 

The random vector $\mathbf{X}=(X_1,\ldots,X_n)$ has a sample space that is a subset of $\R^n.$ If $\mathbf{X}$ is a discrete random vector, then the joint pmf of $\mathbf{X}$ is $f(\mathbf{x})=f(x_1,\ldots,x_n) = P(X_1=x_1,\ldots,X_n=x_n)$ for each $(x_1,\ldots,x_n) \in \R^n.$

For any $A\subset \R^n,$

\\[P(\mathbf{X} \in A) = \sum_{\mathbf{x}\in A} f(\mathbf{x}).\\]

If $\mathbf{X}$ is a continuous random vector, the joint pdf of $(X_1,\ldots,X_n)$ is a function $f(x_1,\ldots,x_n)$ that satisfies

\\[P(\mathbf{X}\in A) = \int \cdots \int_A f(\mathbf{x})\,d\mathbf{x} = \int \cdots \int_A f(x_1,\ldots,x_n)\,dx_1\cdots dx_n.\\]

Let $g(\mathbf{X})$ be a real-valued function defined on the sample space of $\mathbf{X}$. Then $g(\mathbf{X})$ is a random variable and its expected value is 

\\[Eg(\mathbf{X}) = \int_{-\infty}^{\infty} \cdots \int_{-\infty}^{\infty} g(\mathbf{x})f(\mathbf{x})\,d\mathbf{x} \\:\\: \text{ and } \\:\\: Eg(\mathbf{X}) = \sum_{\mathbf{x}\in\R^n} g(\mathbf{x})f(\mathbf{x})\\]

in the continuous and discrete cases respectively. 

The marginal pdf or pmf of any subset of the coordinates of $(X_1,\ldots,X_n)$ can be computed by integrating or summing the joint pdf or pmf over all possible values of the other coordinates. For example, the marginal distribution of $(X_1,\ldots,X_k),$ the first $k$ coordinates of $(X_1,\ldots,X_n),$ is given by the pdf or pmf
\\[f(x_1,\ldots,x_n) = \int_{-\infty}^{\infty} \cdots \int_{-\infty}^{\infty} f(x_1,\ldots,x_n)\,dx_{k+1}\cdots dx_n\\]
or
\\[f(x_1,\ldots,x_n) = \sum_{(x_{k+1},\ldots,x_n)\in\R^{n-k}} f(x_1,\ldots,x_n)\\]
for every $(x_1,\ldots,x_k)\in\R^k.$

The conditional pdf or pmf of a subset of the corrdinates of $(X_1,\ldots,X_n)$ given the values of the remaining coordinates is obtained by dividing the joint pdf or pmf by the marginal pdf or pmf of the remaining coordinates. For example, if $f(x_1,\ldots,x_k)>0,$ the conditional pdf or pmf of $(X_{k+1},\ldots,X_n)$ given $X_1=x_1,\ldots,X_k=x_k$ is the function of $(x_{k+1},\ldots,x_n)$ defined by 
\\[f(x_{k+1},\ldots,x_n \| x_1,\ldots,x_k) = \frac{f(x_1,\ldots,x_n)}{f(x_1,\ldots,x_k)}.\\]

<p class="box def">
Let $n$ and $m$ be positive integers and let $p_1,\ldots,p_n$ be numbers satisfying $0\leq p_i \leq 1, \; i=1,\ldots,n,$ and $\sum_{i=1}^{n} p_i = 1.$ Then the random vector $(X_1,\ldots,X_n)$ has a <strong>multinomial distribution with $m$ trials and cell probabilities $p_1,\ldots,p_n$</strong> if the joint pmf of $(X_1,\ldots,X_n)$ is
\[f(x_1,\ldots,x_n) = \frac{m!}{x_1!\cdots x_n!} p_1^{x_1} \cdots p_n^{x_n} = m!\prod_{i=1}^n \frac{p_i^{x_i}}{x_i!}\]
on the set of $(x_1,\ldots,x_n)$ such that each $x_i$ is a nonnegative integer and $\sum_{i=1}^n x_i = m.$
</p>

The factor $m!/(x_1!\cdots x_n!)$ is called a **multinomial coefficient.** It is the number of ways that $m$ objects can be divided into $n$ groups with $x_1$ in the first group, $x_2$ in the second group$,\ldots,$ and $x_n$ in the $n$th group.

<p class="box theorem">
<strong>Theorem 4.6.1 (Multinomial Theorem)</strong>
Let $m$ and $n$ be positive integers. Let $A$ be the set of vectors $\mathbf{x} = (x_1,\ldots,x_n)$ such that each $x_i$ is a nonnegative integer and $\sum_{i=1}^n x_i = m.$ Then, for any real numbers $p_1,\ldots,p_n,$
\[(p_1 + \cdots + p_n)^m = \sum_{\mathbf{x}\in A} \frac{m!}{x_1!\cdots x_n!} p_1^{x_1} \cdots p_n^{x_n}.\]
</p>

<p class="box def">
Let $\mathbf{X}_1,\ldots,\mathbf{X}_n$ be random vectors with joint pdf or pmf $f(\mathbf{x}_1,\ldots,\mathbf{x}_n).$ let $f_{\mathbf{X}_i} (\mathbf{x}_i)$ denote the marginal pdf or pmf of $\mathbf{X}_i.$ Then $\mathbf{X}_1,\ldots,\mathbf{X}_n$ are called <strong>mutually independent random vectors</strong> if, for every $(\mathbf{x}_1,\ldots,\mathbf{x}_n),$
\[f(\mathbf{x}_1,\ldots,\mathbf{x}_n)=f_{\mathbf{X}_1} (\mathbf{x}_1) \cdots f_{\mathbf{X}_n} (\mathbf{x}_n) = \prod_{i=1}^n f_{\mathbf{X}_i} (\mathbf{x}_i).\]
If the $X_i$s are all one-dimensional, then $X_1,\ldots,X_n$ are called <strong>mutually independent random variables.</strong>
</p>

<p class="box theorem">
<strong>Theorem 4.6.2 (Generalization of Theorem 4.2.?)</strong>
Let $X_1,\ldots,X_n$ be mutually independent random variables. Let $g_1,\ldots,g_n$ be real-valued functions such that $g_i(x_i)$ is a function only of $x_i, \; i=1,\ldots,n.$ Then 
\[E(g_1(X_1)\cdots g_n(X_n)) = (Eg_1(X_1))\cdots(Eg_n(X_n)).\]
</p>

<p class="box theorem">
<strong>Theorem 4.6.3 (Generalization of Theorem 4.2.?</strong>
Let $X_1,\ldots,X_n$ be mutually independent random variables with mgfs $M_{X_1}(t),\ldots,M_{X_n}(t).$ Let $Z = X_1 + \cdots + X_n.$ Then the mgf of $Z$ is 
\[M_Z(t) = M_{X_1}(t)\cdots M_{X_n}(t).\]
In particular, if $X_1,\ldots,X_n$ all have the same distribution with mgf $M_X(t),$ then 
\[M_Z(t) = (M_X(t))^n.\]
</p>

<p class="box theorem">
<strong>Corollary 4.6.4</strong>
Let $X_1,\ldots,X_n$ be mutually independent random variables with mgfs $M_{X_1}(t),\ldots,M_{X_n}(t).$ Let $a_1,\ldots,a_n$ and $b_1,\ldots,b_n$ be fixed constants. Let $Z= (a_1X_1 + b_1) + \cdots (a_nX_n + b_n).$ Then the mgf of $Z$ is 
\[M_Z(t) = (e^{t(\sum b_i)})M_{X_1}(a_1t)\cdots M_{X_n}(a_nt).\]
</p>

<p class="box theorem">
<strong>Corollary 4.6.5</strong>
Let $X_1,\ldots,X_n$ be mutually independent random variables with $X_i \sim N(\mu_i, \sigma_i^2).$ Let $a_1,\ldots,a_n$ and $b_1,\ldots,b_n$ be fixed constants. Then 
\[ Z = \sum_{i=1}^n (a_iX_i + b_i) \sim N\left(\sum_{i=1}^n (a_i\mu_i + b_i), \sum_{i=1}^n a_i^2 \sigma_i^2 \right)\]
</p>

<p class="box theorem">
<strong>Theorem 4.6.6 (Generalization of Lemma 4.2.?)</strong>
Let $\mathbf{X}_1,\ldots,\mathbf{X}_n$ be random vectors. Then $\mathbf{X}_1,\ldots,\mathbf{X}_n$ are mutually independent random vectors if and only if there exist functions $g_i(\mathbf{x}_i), \; i=1,\ldots,n,$ such that the joint pdf or pmf of $(\mathbf{X}_1,\ldots,\mathbf{X}_n)$ can be written as
\[f(\mathbf{x}_1,\ldots,\mathbf{x}_n) = g_1(\mathbf{x}_1) \cdots g_n(\mathbf{x}_n). \]
</p>

<p class="box theorem">
<strong>Theorem 4.6.7 (Generalization of Theorem 4.3.?)</strong>
Let $\mathbf{X}_1,\ldots,\mathbf{X}_n$ be independent random vectors. Let $g_i(\mathbf{x}_i)$ be a function only of $\mathbf{x}_i, \; i=1,\ldots,n.$ Then the random variables $U_i = g_i(\mathbf{X}_i), \; i=1,\ldots,n$ are mutually independent.
</p>