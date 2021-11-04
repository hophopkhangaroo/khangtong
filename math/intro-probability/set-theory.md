---
layout: math
title: Set Theory
usemathjax: true
description:
---

In this section we introduce set theory with the aim of defining sample spaces and events.

# Sets and Subsets

A **set** is a collection of objects. For example, the set $\\{1,2,3\\}$ is a set of the numbers 1, 2, and 3 and $\\{a\\}$ is the set containing a single element $a$. For a set $A$, we denote $a \\in A$ (read, $a$ in $A$) to mean that $a$ is an element of the set $A$. We denote $a \\notin A$ (read, $a$ not in $A$) to mean that $a$ is not an element of $A$. 

Ordering and repetition doesn't matter for sets. So $\\{a, b, c\\} = \\{a, c ,b\\}$ and $\\{a, a, b\\} = \\{a, b\\}$

If a set is empty, we call this the **null** or **empty set** and denote it as $\\emptyset$ or $\\{\\}$.

Let $A$ and $B$ be sets. Then if for each $x \\in A$ we have that $x \\in B$, then we say that $A$ is a **subset** of $B.$ We also say that $A$ is **contained** in $B$ which we write as $A \\subset B$ (or that $B$ contains $A$ which is denoted as $B \\supset A$).  

By definition, $A$ is always a subset of itself. Additionally, the empty set is always a subset of $A$.

Two sets are equal if and only if both $A \\subset B$ and $B \\subset A$ are true. This is typically how we prove equality of sets.

You have certainly encountered subsets of the real numbers (We denote the set of real numbers to be $\\mathbb{R}$). For any pair of real numbers $a$ and $b$ such that $a < b$, the set of all real numbers $x$ such that $a \\leq x \\leq b$ is called the **closed interval** from $a$ to $b$ and denoted as $[a,b]$. Similarly, for $a < x < b$, we denote the set as $(a,b)$ and call it the open interval from $a$ to $b$. $a < x \\leq b$ and $a \\leq x < b$ are **half-open intervals** and denoted as $(a,b]$ and $[a,b)$ respectively. Note that $(a,b) \\subset [a,b] \\subset \\mathbb{R}$. 

Additionally, sets can contain other sets. For example, the set $\\{ \\{a,b\\}, \\{1,2\\} \\}$ is a set that contains 2 objects, 1 of which is a set that contains $a$ and $b$ and the other is a set that contains the numbers 1 and 2. 

Let $A$ be any set. The set of all possible subsets of $A$ is called the **power set** and is denoted as $2^A$. That is, $B \\in 2^A \\iff B \\subset A$.

# Set Operations: Union, Intersection, and Complement

Let $A$ and $B$ be sets. The **union** of the sets $A$ and $B$ is the set of all elements $x$ such that $x \\in A$ or $x \\in B$ ("or" in mathematics is inclusive) which we denote 
\\[A \\cup B = \\{x : x\in A \text{ or } x\in B\\}.\\] 
The **intersection** of $A$ and $B$ is the set of all elements $x$ such that $x \\in A$ and $x \\in B$ which we denote 
\\[A \\cap B = \\{x : x\in A \text{ and } x\in B\\}.\\]   

Let $A \\subset S$. The **complement** of $A$ in $S$ is the set of all elements in $S$ but not in $A$ which we denote by $C_S(A)$ or $A^c$ if we assume to be in $S$.
\\[A^c = \\{x : x \notin A\\}\\]

<div class="box theorem">
	<p><strong>Theorem 1.1.1 (DeMorgan's Laws):</strong>
	Let $A \subset S, B \subset S.$ Then</p>
	<p>a.) $(A\cup B)^c = A^c \cap B^c$</p>
	<p>b.) $(A\cap B)^c = A^c \cup B^c$</p>
</div>

**Proof of (a):** Suppose $x \\in (A\\cup B)^c.$ Then $x \\in S$ and $x \\notin A \\cup B.$ Thus, $x\\notin A$ and $x \\notin B,$ which is the same as $x \\in A^c$ and $x \\in B^c.$ Therefore, $x \\in A^c \\cap B^c.$ This shows that 
\\[(A \\cup B)^c \\subset A^c \\cap B^c.\\] 
Conversely, suppose $x \\in A^c \\cap B^c.$ Then $x\\in S$ and $x \\in A^c$ and $x \\in B^c.$ Thus, $x \\notin A$ and $x \\notin B$ and therefore $x \\notin A \\cup B.$ It follows that $x \\in (A \\cup B)^c$ and thus
\\[A^c \\cap B^c \\subset (A \\cup B)^c.\\]
Hence, we have shown that $A^C \\cap B^c = (A \\cup B)^c.$

The proof of (b) follows similarly.

# Indexed Families of Sets

Let $I$ be a set, not necessarily countable. For each $\\alpha \\in I,$ let $A_{\\alpha}$ be a subset of a given set $S.$ We call $I$ an **indexing set** and the collection of the subsets of $S$ indexed by the elements of $I$ an **indexed family** of subsets of $S.$ We denote this indexed family of subsets of $S$ by $\\{A_{\\alpha}\\}_{\\alpha\\in I}$ (read, "A sub-alpha, alpha in $I$").

<p>Let $\{A_{\alpha}\}_{\alpha \in I}$ be an indexed family of subsets of a set $S.$ The union of this indexed family, written $\cup_{\alpha\in I} A_{\alpha},$ (read "union over $\alpha$ in $I$ of $A_{\alpha}$") is the set of all elements $x \in S$ such that $x \in A_{\beta}$ for at least one index $\beta \in I.$ The intersection of this indexed family, written $\cap_{\alpha\in I} A_{\alpha}$ (read "intersection over $\alpha$ in $I$ of $A_{\alpha}$") is the set of all elements $x \in S$ such that $x \in A_{\beta}$ for each $\beta \in I.$</p>

For example, let $A_1, A_2, A_3, A_4$ be respectively the set of freshmen, sophomores, juniors, and seniors at UCSD. Here, we have $I = \\{1, 2, 3, 4\\}$ as an indexing set, and $\cup_{\alpha\in I} A_{\alpha}$ is the set of undergraduates while $\cap_{\alpha\in I}A_{\alpha}=\emptyset.$

If $I=\emptyset,$ then 
\\[\cup_{\alpha\in \emptyset}A_{\alpha}=\emptyset\\]
\\[\cap_{\alpha\in\emptyset} A_{\alpha} = S.\\]

<div class="box theorem">
<p><strong>Theorem 1.1.2 (DeMorgan's Laws):</strong>
Let $\{A_{\alpha}\}_{\alpha\in I}$ be an indexed family of subsets of a set $S.$ Then</p>
<p> a.) $(\cup_{\alpha\in I}\, A_{\alpha})^c = \cap_{\alpha\in I} \, A_{\alpha}^c$</p>
<p> b.) $(\cap_{\alpha\in I}\, A_{\alpha})^c = \cup_{\alpha\in I} \, A_{\alpha}^c$</p>
</div>

# Products of Sets

Let $x$ and $y$ be objects. Then the **ordered pair** $(x,y)$ is a sequence of two objects. Note that unlike sets, where ordering doesn't matter, if $x \neq y,$ then $(x,y) \neq (y,x).$

Let $A$ and $B$ be sets. The **Cartesian product** of $A$ and $B$, written $A \times B,$ (read "$A$ cross $B$") is the set whose elements are all ordered pairs $(x,y)$ such that $x\in A$ and $y \in B.$

For example, $\\{a, b\\} \times \\{1,2\\} = \\{(a, 1), (a, 2), (b,1), (b,2)\\}.$ Also, the familiar 2d coordinate plane is the Cartesian product of $\R$ and $\R$, denoted $\R\times\R$ or $\R^2.$

Unless $A=B,$ then $A\times B$ and $B\times A$ are distinct.

Let $A_1, A_2, \ldots , A_n$ be a finite sequence of sets, indexed by $\\{1,2,\ldots,n\\}.$ The **direct product** of $A_1, A_2, \ldots , A_n$,  written 
\\[\prod_{i=1}^{n} A_i\\]
is the set consisting of all sequences $(a_1, a_2, \ldots, a_n)$ such that $a_1 \in A_1, a_2 \in A_2 , \ldots, a_n\in A_n.$

The set of points of Euclidean $n$-space is an example of a direct product of sets.
\\[\R^n = \prod_{i=1}^{n} A_i\\]

An element $x\in \R^n$ is a sequence $x=(x_1,\ldots,x_n)$ of real numbers. In general, if the sets $A_1,\ldots,A_n$ are all equal to the same set $A$, we write 
\\[A^n = \prod_{i=1}^{n} A_i\\]
and call an element $a=(a_1,a_2,\ldots,A_n)\in A^n$ an $n$-tuple.