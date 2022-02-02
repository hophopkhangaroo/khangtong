---
layout: math
title: Basics of Probability Theory
usemathjax: true
description:
---

In this section, we  build the notion of a probability through an axiomatic approach. 

In essence we want to be able to define for each event $A$ in a sample space $S$ a number between $0$ and $1$. This assignment of numbers is a function which we will call $P$. This mapping works so long as the sets we're working with are "nice enough". 

For these sets of notes we will not concern ourselves with when they are not "nice enough" but the following definition is helpful when defining probability spaces:

<p class="box def">
A collection of subsets of $S$ is called a <strong>sigma algebra</strong> (or <strong>Borel field</strong>), denoted by $\mathcal{B}$, if it satisfies the following three properties:<br>
a.) $\emptyset \in \mathcal{B}$ (the empty set is an element of $\mathcal{B}$).<br>
b.) If $A\in \mathcal{B}$, then $A^c \in \mathcal{B}$ ($\mathcal{B}$ is closed under complementation).<br>
c.) If $A_1, A_2,\ldots \in \mathcal{B}$, then $\cup_{i=1}^{\infty} A_i \in \mathcal{B}$ ($\mathcal{B}$ is closed under countable unions).
</p>

*Note:* It follows from (a) and (b) that $S \in \mathcal{B}$ and from DeMorgan's law that $\cap_{i=1}^{\infty}A_i\in\mathcal{B}$.

<p class="box example">
<strong>Example 1.3.1</strong>
The set $\{\emptyset, S\}$ is the smallest and considered the trivial $\sigma$-algebra. The largest $\sigma$-algebra is $2^S$.
</p>

While there may be many $\sigma$-algebras associated with a sample space, the smallest one which contains all of the open sets in $S$ is typically the only one we're concerned with.

<p class="box example">
<strong>Example 1.3.2</strong>
Let $S=(-\infty,\infty)$. Then $\mathcal{B}$ is chosen to contain all sets of the form 
\[ [a,b], \;\; (a,b], \;\; (a,b), \;\; \text{and} \;\; [a,b) \]
for $a,b\in\R.$
</p>

<p class="box def">
Given a sample space $S$ and an associated sigma algebra $\mathcal{B}$, a <strong>probability function</strong> is a function $P$ with domain $\mathcal{B}$ that satisfies <br>
1. $P(A) \geq 0$ for all $A\in \mathcal{B}.$<br>
2. $P(S) = 1$.<br>
3. If $A_1, A_2,\ldots \in \mathcal{B}$ are pairwise disjoint, then $P(\cup_{i=1}^{\infty} A_i) = \sum_{i=1}^{\infty} P(A_i).$
</p>

In talking about probabilities, we can now define a probability space $(S,\B,P)$ where $S$ is our sample space, $\B$ is a $\sigma$-algebra, and $P$ is a probability function $P:\B\rightarrow [0,1].$

<p class="box theorem">
<strong>Theorem 1.3.3</strong>
Let $S = \{s_1,\ldots,s_n\}$ be a finite set. Let $\mathcal{B}$ be any sigma algebra of subsets of $S.$ Let $p_1,\ldots,p_n$ be nonnegative numbers that sum to $1.$ For any $A\in \mathcal{B},$ define $P(A)$ by 
\[P(A) = \sum_{\{i : s_i\in A\}} p_i\]
(The sum over an empty set is defined to be 0). Then $P$ is a probability function on $\mathcal{B}.$ This remains true if $S= \{s_1,s_2,\ldots\}$ is a countable set.
</p>

<p class="box example">
<strong>Example 1.3.3</strong>
The game of darts is played by throwing a dart and receiving a score based on the region of the dartboard that the dart lands in. Let's assume that the probability of hitting a particular region of the dartboard is proportional to the area of the region.<br>
Let the board have a radius $r$ and let it have $5$ regions of concentric circles with the distance between each ring being $r/5$. Let region $1$ be the outermost ring and $5$ be the innermost. Assuming that the dartboard is always hit, we have
\[P(\text{scoring $i$ points}) = \frac{\text{Area of region $i$}}{\text{Area of dartboard}}\]
For example:
\[P(\text{scoring $1$ points}) =\frac{\pi r^2 - \pi(4r/5)^2}{\pi r^2} = 1-\left(\frac{4}{5}\right)^2\]
And the general formula is:
\[P(\text{scoring $i$ points}) =\frac{(6-i)^2 - (5-i)^2}{5^2}, \;\; i=1,\ldots 5\]
</p>

The following theorems will help in calculating probabilities. 

<p class="box theorem">
<strong>Theorem 1.3.4</strong>
If $P$ is a probability function and $A$ is any set in $\mathcal{B},$ then <br>
a.) $P(\emptyset)=0,$<br>
b.) $P(A) \leq 1.$ <br>
c.) $P(A^c) = 1-P(A).$
</p>

<p class="box theorem">
<strong>Theorem 1.3.5</strong>
If $P$ is a probability function and $A$ and $B$ are any sets in $\mathcal{B}$, then <br>
a.) $P(B\cap A^c) = P(B) - P(A\cap B)$<br>
b.) $P(A\cup B) = P(A) + P(B) - P(A\cap B)$ <br>
c.) If $A\subset B,$ then $P(A) \leq P(B).$
</p>

*Note:* Since $P(A\cup B) \leq 1$, after some rearranging we have from 1.3.5(b):

\\[P(A\cap B) \geq P(A) + P(B) - 1\\]

which is known as *Bonferroni's Inequality*.

<p class="box theorem">
<strong>Theorem 1.3.6</strong>
If $P$ is a probability function, then <br>
a.) $P(A) = \sum_{i=1}^{\infty} P(A\cap C_i)$ for any partition $C_1,C_2,\ldots$<br>
b.) $P(\cup_{i=1}^{\infty}A_i) \leq \sum_{i=1}^{\infty} P(A_i)$ for any sets $A_1, A_2,\ldots\;\;\;$ (Boole's Inequality)
</p>