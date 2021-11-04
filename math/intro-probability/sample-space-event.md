---
layout: math
title: The Sample Space and Events
usemathjax: true
description:
---

One of the first steps in designing a model or conducting an experiment is to identify all the possible outcomes. 

<p class="box def">
The set, $S$, of all possible outcomes of a particular experiment is called the <strong>sample space</strong> for the experiment.
</p>

For example, the experiment of flipping a coin once has only 2 possible outcomes, heads and tails. So the sample space is
\\[S = \\{H,T\\}.\\]

If the experiment was to measure reaction time in seconds, then the sample space would be $S = (0,\infty).$ 

In the experiment of flipping a coin, our sample space was countable and in the experiment of measuring reaction time, our sample space was the set of positive real numbers, which is uncountable. The distinction is important because the way we assign probabilities depends on the countability of our sample space (it is usually much easier to deal with uncountable sample spaces). We note that some believe there to not be any true uncountable sample spaces in practice, since we have finite accuracy in measurement. However, analysis of uncountable sample spaces usually closely approximates the true situation.

Having defined our sample space, we now define subsets of that space, which we will call events. 

<p class="box def">
An <strong>event</strong> is any collection of possible outcomes of an experiment, that is, any subset of $S$ (including $S$ itself).
</p>

For any set $A$, a subset of $S$, we say that event $A$ occurs if the outcome of the experiment is in $A.$ In talking about probabilities, we typically speak of the probability of an event.

<div class="box example">
<p><strong>Example 1.2.1</strong>
Consider the experiment of rolling a dice and noting the outcome. The sample space is
\[S = \{1,2,3,4,5,6\},\]
and some possible events are 
\[A = \{1,3,5\} \text{ and } B = \{1,2\}.\]
</p></div>

$A$ is the event of rolling an odd number. 

Notice that $A\cup B = S$ (the event $S$) and $(A\cup B)^c = \emptyset.$

Recall that unions can be defined on an indexing set $I$ where $I$ need not be countable.

<div class="box example">
<p><strong>Example 1.2.2</strong>
Let $S = (0,1]$ and define $A_i = [(1/i), 1].$ Then 
\[
\begin{align*}
\bigcup_{i=1}^{\infty} A_i =& \bigcup_{i=1}^{\infty}[(1/i),1] = \{x\in (0,1]: x\in [(1/i),1 \text{ for some }i\} \\
=& \{x \in (0,1]\} = (0,1] \\
\end{align*}
\]
\[
\begin{align*}
\bigcap_{i=1}^{\infty} A_i =& \bigcap_{i=1}^{\infty} [(1/i),1] = \{x\in (0,1] : x\in [(1/i),1] \text{ for all } i\} \\
=& \{x\in (0,1] : x \in [1,1]\} = \{1\}.
\end{align*}
\] </p>
</div>

<p class="box def">
Two events $A$ and $B$ are <strong>disjoint</strong> (or <strong>mutually exclusive</strong>) if $A\cap B= \emptyset.$
<br>
The events $A_1,A_2,\ldots,$ are <strong>pairwise disjoint</strong> (or <strong>mutually exclusive</strong>) if $A_i\cap A_j = \emptyset$ for all $i\neq j.$
</p>

In other words, disjoint sets are sets that have no points in common. For example, the collection 
\\[A_i = [i,i+1), \; i=0,1,2,\ldots\\]
consists of pairwise disjoint sets.

<p class="box def">
If $A_1,A_2,\ldots$ are pairwise disjoin and $\cup_{i=1}^{\infty} A_i = S,$ then the collection $A_1,A_2,\ldots$ forms a <strong>partition</strong> of $S.$
</p>

The sets $A_i = [i, i+1)$ form a partition of $[0,\infty).$

