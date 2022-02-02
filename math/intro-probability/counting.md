---
layout: math
title: Counting
usemathjax: true
description:
---

For discrete sample spaces, counting plays an important role in figuring out probabilities.

<p class="box example">
<strong>Example 1.4.1</strong>
The New York state lottery used to have the following scheme: from the numbers $1,2,\ldots,44$, a person can pick any $6$ for their ticket. The winning number is then decided by randomly selecting six numbers from the forty-four. To calculate the probability of winning we must count how many ways six numbers can be chosen from forty-four.
</p>

<p class="box theorem">
<strong>Theorem 1.4.2 (The Fundamental Theorem of Counting)</strong>
If a job consists of $k$ separate tasks, the $i$th of which can be done in $n_i$ ways, $i=1,\ldots,k,$ then the entire job can be done in $n_1 \times \cdots \times n_k$ ways. 
</p>

<p class="box def">
For a positive integer $n, n!$ (read $n$ <strong>factorial</strong>) is the product of all the positive integers less than or equal to $n.$ That is
\[n! = n\times (n-1) \times (n-2) \times \cdots 3 \times 2 \times 1.\]
Furthermore, we define $0!=1.$
</p>

<p class="box def">
For nonnegative integers $n$ and $r$, where $n \geq r,$ we define the symbol $ n \choose r$, read $n$ choose $r,$ as 
\[{n \choose r} = \frac{n!}{r!(n-r)!}.\]
</p>

Table 1.4.1. Number of possible arrangements of size $r$ from $n$ objects

|           |Without replacement  |With replacement  |
|:---------:|:-------------------:|:----------------:|
|Ordered    |\\[\frac{n!}{(n-r)!}\\]  | \\[n^r\\]            |
|Unordered  |\\[n \choose r\\]        |\\[{n+r-1}\choose r\\]|

