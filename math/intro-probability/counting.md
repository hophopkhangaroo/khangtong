---
layout: math
title: Counting
usemathjax: true
description:
---

<div class="box theorem">
<strong>Theorem 1.4.1</strong>
If a job consists of $k$ separate tasks, the $i$th of which can be done in $n_i$ ways, $i=1,\ldots,k,$ then the entire job can be done in $n_1 \times \cdots \times n_k$ ways. 
</div>

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

