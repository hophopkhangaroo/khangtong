---
layout: math
title: Basics of Probability Theory
usemathjax: true
description:
---

<p class="box def">
A collection of subsets of $S$ is called a <strong>sigma algebra</strong> (or <strong>Borel field</strong>), denoted by $\mathcal{B}$, if it satisfies the following three properties:<br>
a.) $\emptyset \in \mathcal{B}$ (the empty set is an element of $\mathcal{B}$).<br>
b.) If $A\in \mathcal{B}$, then $A^c \in \mathcal{B}$ ($\mathcal{B}$ is closed under complementation).<br>
c.) If $A_1, A_2,\ldots \in \mathcal{B}$, then $\cup_{i=1}^{\infty} A_i \in \mathcal{B}$ ($\mathcal{B}$ is closed under countable unions).
</p>

<p class="box def">
Given a sample space $S$ and an associated sigma algebra $\mathcal{B}$, a <strong>probability function</strong> is a function $P$ with domain $\mathcal{B}$ that satisfies <br>
1. $P(A) \geq 0$ for all $A\in \mathcal{B}.$<br>
2. $P(S) = 1$.<br>
3. If $A_1, A_2,\ldots \in \mathcal{B}$ are pairwise disjoint, then $P(\cup_{i=1}^{\infty} A_i) = \sum_{i=1}^{\infty} P(A_i).$
</p>

<div class="box theorem">
<strong>Theorem 1.3.1</strong>
Let $S = \{s_1,\ldots,s_n\}$ be a finite set. Let $\mathcal{B}$ be any sigma algebra of subsets of $S.$ Let $p_1,\ldots,p_n$ be nonnegative numbers that sum to $1.$ For any $A\in \mathcal{B}<$ define $P(A)$ by 
\[P(A) = \sum_{\{i : s_i\in A\}} p_i\]
(The sum over an empty set is defined to be 0). Then $P$ is a probability function on $\mathcal{B}.$ This remains true if $S= \{s_1,s_2,\ldots\}$ is a countable set.
</div>

<div class="box theorem">
<strong>Theorem 1.3.2</strong>
If $P$ is a probability function and $A$ is any set in $\mathcal{B},$ then <br>
a.) $P(\emptyset)=0,$<br>
b.) $P(A) \leq 1.$ <br>
c.) $P(A^c) = 1-P(A).$
</div>

<div class="box theorem">
<strong>Theorem 1.3.3</strong>
If $P$ is a probability function and $A$ and $B$ are any sets in $\mathcal{B}$, then <br>
a.) $P(B\cap A^c) = P(B) - P(A\cap B)$<br>
b.) $P(A\cup B) = P(A) + P(B) - P(A\cap B)$ <br>
c.) If $A\subset B,$ then $P(A) \leq P(B).$
</div>

<div class="box theorem">
<strong>Theorem 1.3.4</strong>
If $P$ is a probability function, then <br>
a.) $P(A) = \sum_{i=1}^{\infty} P(A\cap C_i)$ for any partition $C_1,C_2,\ldots$<br>
b.) $P(\cup_{i=1}^{\infty}A_i) \leq \sum_{i=1}^{\infty} P(A_i)$ for any sets $A_1, A_2,\ldots$ 
</div>