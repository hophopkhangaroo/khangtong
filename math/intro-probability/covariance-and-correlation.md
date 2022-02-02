---
layout: math
title: Covariance and Correlation
usemathjax: true
description:
---

<p class="box def">
The <strong>covariance</strong> of $X$ and $Y$ is the number defined by 
\[Cov(X,Y) = E((X-\mu_X)(Y-\mu_Y)).\]
</p>

<p class="box def">
The <strong>correlation</strong> of $X$ and $Y$ is the number defined by 
\[\rho_{XY}=\frac{Cov(X,Y)}{\sigma_X \sigma_Y}.\]
The value $\rho_{XY}$ is also called the <strong>correlation coefficient</strong>
</p>

<p class="box theorem">
<strong>Theorem 4.5.1</strong>
For any random variables $X$ and $Y,$
\[Cov(X,Y) = EXY - \mu_X \mu_Y.\]
</p>

<p class="box theorem">
<strong>Theorem 4.5.2</strong>
If $X$ and $Y$ are independent random variables, then $Cov(X,Y)=0$ and $\rho_{XY}=0.$
</p>

<p class="box theorem">
<strong>Theorem 4.5.3</strong>
If $X$ and $Y$ are any two random variables and $a$ and $b$ are any two constants, then 
\[Var(aX + bY) = a^2VarX + b^2VarY + 2abCov(X,Y).\]
If $X$ and $Y$ are independent random variables, then 
\[Var(aX + bY) = a^2VarX + b^2VarY\]
</p>

<p class="box theorem">
<strong>Theorem 4.5.4</strong>
For any random variables $X$ and $Y,$ <br>
a) $-1\leq \rho_{XY} \leq 1.$ <br>
b) $|\rho_{XY}| = 1$ if and only if there exist numbers $a\neq 0$ and $b$ such that $P(Y=aX +b) = 1.$ If $\rho_{XY}=1,$ then $a>0,$ and if $\rho_{XY} = -1,$ then $a<0.$
</p>

<p class="box def">
Let $-\infty < \mu_X < \infty, -\infty < \mu_Y < \infty, \;0 < \sigma_X,\; 0< \sigma_Y,$ and $-1 < \rho < 1$ be five real numbers. The <strong>bivariate normal pdf with means $\mu_X$ and $\mu_Y,$ variances $\sigma_X^2$ and $\sigma_Y^2,$ and correlation $\rho$</strong> is the bivariate pdf given by
\[f(x,y) = \left(2\pi\sigma_x \sigma_Y \sqrt{1-\rho^2}\right)^{-1}\exp\left(-\frac{1}{2(1-\rho^2)}\left(\left(\frac{x-\mu_X}{\sigma_X}\right)^2-2\rho\left(\frac{x-\mu_X}{\sigma_X}\right)\left(\frac{y-\mu_Y}{\sigma_Y}\right)+\left(\frac{y-\mu_Y}{\sigma_Y}\right)^2\right)\right)\]
for $-\infty < x < \infty$ and $-\infty < y < \infty.$
</p>

Properties of this distribution include:

a. The marginal distribution of $X$ is $N(\mu_X, \sigma_X^2).$

b. The marginal distribution of $Y$ is $N(\mu_Y, \sigma_Y^2).$

c. The correlation between $X$ and $Y$ is $\rho_{XY} = \rho.$

d. For any constants $a$ and $b,$ the distribution of $aX+bY$ is $N(a\mu_X + b\mu_Y, a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\rho\sigma_X\sigma_Y).$