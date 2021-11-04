---
layout: math
title: Conditional Probability and Independence
usemathjax: true
description:
---

<p class="box def">
If $A$ and $B$ are events in $S$, and $P(B) > 0,$ then the <strong>conditional probability of $A$ given $B$</strong>, written $P(A\vert B)$, is 
\[P(A\vert B) = \frac{P(A\cap B)}{P(B)}.\]
</p>

<div class="box theorem">
<strong>Theorem 1.5.1 (Baye's Rule)</strong>
Let $A_1,A_2,\ldots$ be a partition of the sample space, and let $B$ be any set. Then for each $i=1,2,\ldots,$
\[P(A_i\vert B) = \frac{P(B \vert A_i) P(A_i)}{\sum_{j=1}^{\infty} P(B\vert A_j)P(A_j)}.\]
</div> 

<p class="box def">
Two events, $A$ and $B$, are <strong>statisticaly independent</strong> if 
\[P(A\cap B) = P(A)P(B)\]
</p>

<div class="box theorem">
<strong>Theorem 1.5.2</strong>
If $A$ and $B$ are independent events, then the following pairs are also independent: <br>
a.) $A$ and $B^c$<br>
b.) $A^c$ and $B$ <br>
c.) $A^c$ and $B^c$
</div>

<p class="box def">
A collection of events $A_1, \ldots, A_n$ are <strong>mutually independent</strong> if for any subcollection $A_{i_1},\ldots,A_{i_k},$ we have
\[P\left(\bigcap_{j=1}^{k} A_{i_j}\right) = \prod_{j=1}^{k} P(A_{i_j}).\]
</p>