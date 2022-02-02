---
layout: math
title: Sums of Random Variables from a Random Sample
usemathjax: true
description:
---

<p class="box def">
Let $X_1,\ldots,X_n$ be a random sample of size $n$ from a population and let $T(x_1,\ldots,x_n)$ be a real-valued or vector-valued function whose domain includes the sample space of $(X_1,\ldots,X_n).$ Then the random variable or random vector $Y=T(X_1,\ldots,X_n)$ is called a <strong>statistic.</strong> The probability distribution of a statistic $Y$ is called the <strong>sampling distribution</strong> of $Y.$
</p>

<p class="box def">
The <strong>sample mean</strong> is the arithmetic average of the values in a random sample. It is usually denoted by
\[\overline{X} = \frac{X_1 + \cdots + X_n}{n} = \frac{1}{n}\sum_{i=1}^n X_i.\]
</p>

<p class="box def">
The <strong>sample variance</strong> is the statistic defined by
\[S^2 = \frac{1}{n-1} \sum_{i=1}^n (X_i-\overline{X})^2.\]
The <strong>sample standard deviation</strong> is the statistic defined by $S=\sqrt{S^2}.$
</p>

<p class="box theorem">
<strong>Theorem 5.2.1</strong>
Let $x_1,\ldots,x_n$ be any numbers and $\bar{x}=(x_1+\cdots x_n)/n.$ Then <br>
a) $\min_a \sum_{i=1}^n (x_i-a)^2 = \sum_{i=1}^n (x_i-\bar{x})^2,$ <br>
b) $(n-1)s^2 = \sum_{i=1}^n (x_i-\bar{x})^2 = \sum_{i=1}^n x_i^2 - n\bar{x}^2.$
</p>

<p class="box theorem">
<strong>Lemma 5.2.2</strong>
Let $X_1,\ldots,X_n$ be a random sample from a population and let $g(x)$ be a function such that $Eg(X_1)$ and $Var\, g(X_1)$ exist. Then 
\[E\left(\sum_{i=1}^n g(X_i)\right) = n(Eg(X_1))\]
and
\[Var\left(\sum_{i=1}^n g(X_i)\right) = n(Var\, g(X_1)).\]
</p>

<p class="box theorem">
<strong>Theorem 5.2.3</strong>
Let $X_1,\ldots,X_n$ be a random sample from a population with mean $\mu$ and variance $\sigma^2 < \infty.$ Then <br>
a) $E\overline{X} = \mu.$ <br>
b) $Var \, \overline{X} = \frac{\sigma^2}{n},$ <br>
c) $ES^2 = \sigma^2.$
</p>

<p class="box theorem">
<strong>Theorem 5.2.4</strong>
Let $X_1,\ldots,X_n$ be a random sample from a population with mgf $M_X(t).$ Then the mgf of the sample mean is
\[M_{\overline{X}}(t) = [M_X(t/n)]^n.\]
</p>

<p class="box theorem">
<strong>Theorem 5.2.5</strong>
If $X$ and $Y$ are independent continuous random variables with pdfs $f_X(x)$ and $f_Y(y),$ then the pdf of $Z=X+Y$ is 
\[f_Z(z) = \int_{-\infty}^{\infty} f_X(w)f_Y(z-w)\,dw.\]
</p>

<p class="box theorem">
<strong>Theorem 5.2.6</strong>
Suppose $X_1,\ldots,X_n$ is a random sample from a pdf or pmf $f(x|\theta),$ where
\[f(x|\theta) = h(x)c(\theta)\exp\left(\sum_{i=1}^k w_i(\theta)t_i(x)\right)\]
is a member of an exponential family. Define statistics $T_1,\ldots,T_k$ by 
\[T_i(X_1,\ldots,X_n) = \sum_{j=1}^n t_i(X_j), \:\: i = 1,\ldots,k.\]
If the set $\{(w_1(\theta),w_2(\theta),\ldots,w_k(\theta)),\, \theta \in \Theta\}$ contains an open subset of $\R^k,$ then the distribution of $(T_1,\ldots,T_k)$ is an exponential family of the form
\[f_T(u_1,\ldots,u_k | \theta) = H(u_1,\ldots,u_k)[c(\theta)]^n\exp\left(\sum_{i=1}^k w_i(\theta)u_i\right)\]
</p>