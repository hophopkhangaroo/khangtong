---
layout: math
title: Order Statistics
usemathjax: true
description:
---

<p class="box def">
The <strong>order statistics</strong> of a random sample $X_1,\ldots,X_n$ are the sample values placed in ascending order. They are denoted by $X_{(1)},\ldots,X_{(n)}.$
</p>

The order statistics are random variables that satisfy $X_{(1)} \leq \cdots \leq X_{(n)}.$ In particular,
\\[X_{(1)} = \min_{1\leq i \leq n} X_i,\\]
\\[X_{(2)} = \text{ second smallest } X_i,\\]
\\[\vdots\\]
\\[X_{(n)} = \max_{1\leq i \leq n} X_i.\\]

<p class="box def">
The <strong>sample range</strong>, $R=X_{(n)}-X_{(1)},$ is the distance between the smallest and largest observations. <br>
The <strong>sample median</strong>, denoted $M$, is a number such that approximately one-half of the observations are less than $M$ and one-half are greater. We define $M$ by: 
\[M = 
\begin{cases}
X_{((n+1)/2)} & \text{if $n$ is odd} \\ 
\left(X_{(n/2)}+X_{(n/2+1)}\right)/2 & \text{if $n$ is even.}
\end{cases}\]
</p>

<p class="box def">
The notation $\{b\},$ when appearing in a subscript, is defined to be the number $b$ rounded to the nearest integer in the usual way. More precisely, if $i$ is an integer and $i-0.5\leq b< i+ 0.5,$ then $\{b\}=i.$
</p>

<p class="box theorem">
<strong>Theorem 5.4.1</strong>
Let $X_1,\ldots,X_n$ be a random sample from a discrete distribution with pmf $f_X(x_i)=p_i,$ where $x_1< x_2<\cdots$ are possible values of $X$ in ascending order. Define
\[P_0=0\]
\[P_1=p_1\]
\[P_2=p_1+p_2\]
\[\vdots\]
\[P_i = p_1 + p_2 + \cdots + p_i\]
\[\vdots\]
Let $X_{(1)},\ldots,X_{(n)}$ denote the order statistics from the sample. Then
\[P(X_{(j)} \leq x_i) = \sum_{k=j}^n {n \choose k}P_i^k (1-P_i)^{n-k}\]
and
\[P(X_{(j)} = x_i) = \sum_{k=j}^n {n \choose k} \left[P_i^k(1-P_i)^{n-k} - P_{i-1}^k(1-P_{i-1})^{n-k}\right].\]
</p>

<p class="box theorem">
<strong>Theorem 5.4.2</strong>
Let $X_{(1)},\ldots,X_{(n)}$ denote the order statistics of a random sample, $X_1,\ldots,X_n,$ from a continuous population with cdf $F_X(x)$ and pdf $f_X(x).$ Then the pdf of $X_{(j)}$ is 
\[f_{X_{(j)}}(x) = \frac{n!}{(j-1)!(n-j)!}f_X(x)\left[F_X(x)\right]^{j-1}\left[1-F_X(x)\right]^{n-j}.\]
</p>

<p class="box theorem">
<strong>Theorem 5.4.3</strong>
Let $X_{(1)},\ldots,X_{(n)}$ denote the order statistics of a random sample, $X_1,\ldots,X_n,$ from a continuous population with cdf $F_X(x)$ and pdf $f_X(x).$ Then the joint pdf of $X_{(i)}$ and $X_{(j)},\; 1\leq i < j \leq n,$ is  
\[f_{X_{(i)},X_{(j)}}(u,v) = \frac{n!}{(i-1)!(j-1-i)!(n-j)!}f_X(u)f_X(v)\left[F_X(u)\right]^{i-1}\left[F_X(v)-F_X(u)\right]^{j-1-i}\left[1-F_X(v)\right]^{n-j}\]
for $-\infty < u < v < \infty.$<br>
The joint pdf of all the order statistics is given by
\[f_{X_{(1)},\ldots,X_{(n)}}(x_1,\ldots,x_n) = 
\begin{cases}
n!f_X(x_1)\cdots f_X(x_n) & -\infty < x_1 < \cdots < x_n < \infty \\
0 & \text{otherwise.}
\end{cases}\]
</p>