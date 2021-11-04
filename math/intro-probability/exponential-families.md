---
layout: math
title: Exponential Families
usemathjax: true
description:
---

<p class="box def">
A family of pdfs or pmfs is called an <strong>exponential family</strong> if it can be expressed as
\begin{equation}
\label{eq:exp-fam}
f(x\vert\boldsymbol{\theta}) = h(x)c(\boldsymbol{\theta})\exp{\left(\sum_{i=1}^{k}w_i(\boldsymbol{\theta})t_i(x)\right)}.
\end{equation}
</p>

<div class="box theorem">
<strong>Theorem 3.3.1</strong>
If $X$ is a random variable with pdf or pmf of the form \ref{eq:exp-fam}, then
\begin{equation}
\label{eq:th1-e}
\E\left(\sum_{i=1}^{k} \frac{\partial w_i(\boldsymbol{\theta})}{\partial\theta_j} t_i(X)\right) = -\frac{\partial}{\partial\theta_j}\log c(\boldsymbol{\theta})
\end{equation}

\begin{equation}
\label{eq:th1-var}
Var\left(\sum_{i=1}^{k} \frac{\partial w_i(\boldsymbol{\theta})}{\partial\theta_j} t_i(X)\right) = -\frac{\partial^2}{\partial\theta_j^2}\log c(\boldsymbol{\theta})-\E\left(\sum_{i=1}^{k}\frac{\partial^2 w_i(\boldsymbol{\theta})}{\partial\theta_j^2}t_i(X)\right).
\end{equation}
</div>

<p class="box def">
The <strong>indicator function</strong> of a set $A$, most often denoted by $I_A(x),$ is the function
\[I_A(x)=
\begin{cases}
1 & x\in A \\
0 & x \notin A.
\end{cases}
\]
</p>

<p class="box def">
A <strong>curved exponential family</strong> is a family of densities of the form \ref{eq:exp-fam} for which the dimension of the vector $\boldsymbol{\theta}$ is equal to $d<k.$ If $d=k$, the family of a <strong>full exponential family</strong>.
</p>