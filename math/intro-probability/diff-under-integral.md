---
layout: math
title: Differentiation Under the Integral Sign
usemathjax: true
description:
---

Proving [Theorem 2.3.2](moments-mgf) utilized the assumption that we could differentiate under the integral sign. Since it is a useful technique in theoretical statistics, we characterize the conditions under which interchanging derivatives and integrals is possible. 

We wish to calculate

\\[\frac{d}{d\theta} \int_{a(\theta)}^{b(\theta)} f(x, \theta) \, dx\\]

where $\-infty < a(\theta), b(\theta) < \infty$ for all $\theta.$ The rule for differentiating the above is called Leibnitz's Rule and is an application of the Fundamental Theorem of Calculus and the chain rule.

<div class="box theorem">
<strong>Theorem 2.4.1 (Leibnitz's Rule)</strong>
If $f(x,\theta), a(\theta),$ and $b(\theta)$ are differentiable with respect to $\theta,$ then 
\[\frac{d}{d\theta} \int_{a(\theta)}^{b(\theta)} f(x,\theta) \, dx = f(b(\theta), \theta) \frac{d}{d\theta} b(\theta) - f(a(\theta), \theta)\frac{d}{d\theta} a(\theta) + \int_{a(\theta)}^{b(\theta)}\frac{\partial}{\partial\theta}f(x,\theta)\, dx.\]
<em>Note:</em> If $a(\theta)$ and $b(\theta)$ are constants, then we have a special case of Leibnitz's Rule:
\[\frac{d}{d(\theta)} \int_a^b f(x,\theta) \, dx = \int_a^b \frac{\partial}{\partial\theta} f(x,\theta) \, dx.\]
</div>

<div class="box theorem">
<strong>Theorem 2.4.2</strong>
Suppose the function $h(x,y)$ is continuous at $y_0$ for each $x,$ and there exists a function $g(x)$ satisfying <br>
i. $|h(x,y)| \leq g(x)$ for all $x$ and $y,$ <br>
ii. $\int_{-\infty}^{\infty} g(x) \, dx < \infty.$<br>
Then
\[\lim_{y \rightarrow y_0} \int_{-\infty}^{\infty} h(x,y) \, dx = \int_{-\infty}^{\infty} \lim_{y \rightarrow y_0} h(x,y) \, dx.\]
</div>

<div class="box theorem">
<strong>Theorem 2.4.3</strong>
Suppose $f(x,\theta)$ is differentiable at $\theta = \theta_0,$ that is,
\[\lim_{\delta \rightarrow 0}\frac{f(x, \theta_0 + \delta) - f(x, \theta_0)}{\delta} = \frac{\partial}{\partial\theta}f(x,\theta)\bigg\vert_\theta=\theta_0\]
exists for every $x$, and there exists a function $g(x, \theta_0)$ and a constant $\delta_0>0$ such that <br>
i. $\displaystyle\left\vert \frac{f(x, \theta_0 + \delta) - f(x, \theta_0)}{\delta}\right\vert \leq g(x,\theta_0),$ for all $x$ and $|\delta |\leq \delta_0.$ <br>
ii. $\int_{-\infty}^{\infty} g(x,\theta_0) \, dx < \infty.$ <br>
Then
\[\frac{d}{d\theta}\int_{-\infty}^{\infty} f(x,\theta) \, dx \bigg\vert_{\theta=\theta_0} = \int_{-\infty}^{\infty} \left[\frac{\partial}{\partial\theta} f(x, \theta)\bigg\vert_{\theta=\theta_0}\right]\,dx.\]
</div>

\begin{equation}
\label{eq:interchange}
\frac{d}{d\theta} \int_{-\infty}^{\infty} f(x,\theta) \, dx = \int_{-\infty}^{\infty} \frac{\partial}{\partial \theta} f(x,\theta) \, dx.
\end{equation}
\begin{equation}
\label{eq:bound}
\left\vert\frac{\partial}{\partial\theta}f(x,\theta)\right\vert_{\theta=\theta^{\prime}}\bigg\vert\leq g(x,\theta) \;\;\;\;\text{ for all $\theta^{\prime}$ such that $|\theta^{\prime}-\theta | \leq \delta_0$.}
\end{equation}

<div class="box theorem">
<strong>Corollary 2.4.4</strong>
Suppose $f(x,\theta)$ is differentiable in $\theta$ and there exists a function $g(x,\theta)$ such that \ref{eq:bound} is satisfied and $\int_{-\infty}^{\infty} g(x,\theta)\, dx < \infty.$ Then \ref{eq:interchange} holds.
</div>

<div class="box theorem">
<strong>Theorem 2.4.5</strong>
Suppose that the series $\sum_{x=0}^{\infty} h(\theta,x)$ converges for all $\theta$ in an interval $(a,b)$ of real numbers and <br>
i. $\frac{\partial}{\partial\theta}h(\theta,x)$ is continuous in $\theta$ for each $x,$<br>
ii. $\sum_{x=0}^{\infty}\frac{\partial}{\partial\theta} h(\theta,x)$ converges uniformly on every closed bounded subinterval of $(a,b).$<br>
Then
\[\frac{d}{d\theta}\sum_{x=0}^{\infty}h(\theta,x) = \sum_{x=0}^{\infty}\frac{\partial}{\partial\theta} h(\theta,x).\]
</div>

<div class="box theorem">
<strong>Theorem 2.4.6</strong>
Suppose the series $\sum_{x=0}^{\infty} h(\theta,x)$ converges uniformly on $[a,b]$ and that, for each $x, \; h(\theta,x)$ is a continuous function of $\theta.$ Then 
\[\int_a^b \sum_{x=0}^{\infty} h(\theta,x) \, d\theta = \sum_{x=0}^{\infty} \int_a^b h(\theta,x) \, d\theta. \]
</div>