---
layout: math
title: Conic Sections and Conics
usemathjax: true
description: In this section, we investigate how to describe conic sections.
---

A conic is a shape obtained from taking a plane slice through a double cone. Below are all the different types of shapes possible. 

[DIAGRAM OF CONIC SHAPES]

*Remark:* A circle is just a special case of an ellipse. Also notice that ellipses and hyperbolas have centers; that is, there exists a point $C$ such that a rotation about $C$ through an angle $\pi$ is a symmetry of the conic.
<p class="box def">
	We define the set of conic sections that are <em>ellipses, parabolas</em>, or <em>hyperbolas</em> to be <strong>non-degenerate conic sections</strong> and we define the set of conic sections that are <em>single points, single lines,</em> or <em>pairs of lines</em> to be <strong>degenerate conic sections</strong>.
</p>

## Circles

Think back to when we were all learning how to draw circles. One technique our teachers might've taught us is to attach one end of a string to a piece of paper and a pencil to the other. Then, with the string stretched outwards, a perfect circle can be drawn with the pencil.

This demonstrates a fundamental property about circles: a circle in $\R^2$ is the set of all points $(x,y)$ that lie a fixed distance, called the *radius*, away from a fixed point, called the *center*. 

Recall that the distance between two points $p_1=(x_1, y_1)$ and $p_2=(x_2, y_2)$ in $\R^2$ is given by the formula $\text{dist}(p_1,p_2) = \sqrt{(x_1-x_2)^2+(y_1-y_2)^2}.$

Then for any circle with center $C=(a, b)$, we have that any arbitrary point, $(x,y)$, on the circle is given by \\[r^2=(x-a)^2+(y-b)^2\\] where $r$ is the radius.

<div class="box example">
	<p><strong>Example 1</strong>
	Determine the equation of each of the circles with the following center and radius: <br>  
		(a) center: origin, radius: $3$ <br>  
		(b) center: $(4,2)$, radius: $7$<br>
		(c) center: $(\sqrt{2}, 3)$, radius: $\sqrt[3]{7}$ <br></p>
	<p style="overflow: auto;"><strong>Solution</strong><br>
	Here, we're just plugging numbers into the formula we found earlier:</p>
		<p style="overflow: auto;">(a) $(x-0)^2 + (y-0)^2 = 3^2 \implies x^2+y^2=9$ </p>
		<p>(b) $(x-4)^2 + (y-2)^2 = 49$ </p>
		<p>(c) Note that $\sqrt[3]{7}=7^{\frac{1}{3}}$. So then $(x-\sqrt{2})^2 + (y-3)^2 = 7^{\frac{2}{3}}$ </p> 
</div>

If we expand our formula, we get that \\[x^2 + y^2 -2ax -2by + (a^2 +b^2 -r^2) = 0.\\]
So then let $f=-2a$, $g=-2b$, and $h=a^2 +b^2 -r^2$. Our equation becomes \\[x^2+y^2+fx+gy+h=0.\\]

<div class="box example">
	<p><strong>Example 2</strong>
	Determine the condition on the numbers $f,g,$ and $h$ in the equation \[x^2+y^2+fx+gy+h=0.\] for the circle with this equation to pass through the origin.</p>
	<p><strong>Solution</strong>
	Since all points on the circle satisfy the given equation, $(0,0)$ must be a solution if our circle contains the origin. Plugging in $0$ for $x$ and $y$, we find that $h=0$. But recall that $h=a^2+b^2-r^2$. Thus, we obtain the three following conditions that $f,g,$ and $h$ must satisfy:</p>
	<p>\[f=-2a\]
		\[g=-2b\]
		\[h=0 \implies r^2=a^2+b^2\]
	</p>
</div>

So we've seen that the equation for a circle can be written as $x^2 + y^2 +fx +gy + h = 0.$ But can we go the other way? In other words, given an equation of the second form, can we determine if it represents a circle and find its center and radius?

Recall [completing the square](https://www.mathsisfun.com/algebra/completing-square.html){:target="_blank" rel="noopener noreferrer"}. Isolate terms that involve only $x$ and terms that involve only $y$. Complete the squares of these two expressions and plug back into the original equation. For example, consider \\[x^2+y^2-2x-4y+2=0.\\] Writing only the terms that involve $x$ and the terms that involve $y$ and completing the square, we obtain \\[x^2-2x = (x-1)^2-1\\] \\[y^2-4y=(y-2)^2-4.\\]

Plugging this back into our original equation, we get 

\begin{align\*}
	(x-1)^2-1+(y-2)^2-4+2 &= 0 \\\\ (x-1)^2+(y-2)^2 &= 3
\end{align\*}

We can now easily see that the center is $(1,2)$ and the radius is $\sqrt{3}$.

Similarly, if we apply the same method to the general form $x^2 + y^2 +fx +gy + h = 0,$ we obtain the equation \\[\left(x+\frac{1}{2}f\right)^2 +\left(y+\frac{1}{2}g\right)^2 = \frac{1}{4}f^2+\frac{1}{4}g^2-h.\\]

<div class="box theorem">
	<p><strong>Theorem 1</strong>
	An equation of the form \[x^2 + y^2 +fx +gy + h = 0\] represents a circle with</p>
	<p style="text-align:center;">center $(-\frac{1}{2}f, -\frac{1}{2}g)$ and radius $\sqrt{\frac{1}{4}f^2+\frac{1}{4}g^2-h},$</p>
	<p>provided that $\frac{1}{4}f^2+\frac{1}{4}g^2-h > 0.$</p>
</div>

<div class="box example">
	<p><strong>Example 3</strong>
	Determine the center and the radius of the following equation:
	\[4x^2+4y^2-12x-40y=0.\]</p>
	<p><strong>Solution</strong>
	Since the coefficient in front of the $x^2$ and $y^2$ term is not $1$, divide the equation by $4$ to obtain \[x^2+y^2-3x-10y=0.\] Note that $f=-3,$ $g=-10,$ and $h=0.$ By theorem $1,$ we have that this equation describes a circle with center at $(\frac{3}{2}, 5)$ and radius $\frac{\sqrt{109}}{2}.$</p>
</div>

### Orthogonal Circles

Here, we pose the question: under what conditions will two intersecting circles intersect at right angles?

Consider a circle $C_1$ with center $A = (-\frac{1}{2}f_1, -\frac{1}{2}g_1)$ and radius $r_1=\sqrt{\frac{1}{4}f_1^2 + \frac{1}{4}g_1^2-h_1}$ and a circle $C_2$ with center $B = (-\frac{1}{2}f_2, -\frac{1}{2}g_2)$ and radius $r_2=\sqrt{\frac{1}{4}f_2^2 + \frac{1}{4}g_2^2-h_2}.$ Let $P$ be one of their points of intersection and examine the triangle $\triangle ABP.$

[DIAGRAM OF INTERESECTING CIRCLES]

If the circles intersect orthogonally, then the line $AP$ is tangent to $C_2$ which makes it orthogonal to $PB.$ Thus, $\triangle ABP$ is a right triangle and we can apply the Pythagorean Theorem to obtain
\begin{equation}
	\label{eq:orthog}
	(AP)^2 + (PB)^2 = (AB^2)
\end{equation}
But $AP$ and $PB$ are just the radii of their respective circles. Thus, we know their values:
\begin{align\*}
	(AP)^2 &= r_1^2 = \frac{1}{4}f_1^2 + \frac{1}{4}g_1^2-h_1 \;\text{ and} \\\\ 
	(PB)^2 &= r_2^2 = \frac{1}{4}f_2^2 + \frac{1}{4}g_2^2-h_2.
\end{align\*}
And using the distance formula,
\begin{align\*}
	(AB)^2 &= (\frac{1}{2}f_1 - \frac{1}{2}f_2)^2 + (\frac{1}{2}g_1 - \frac{1}{2}g_2)^2 \\\\ 
	&=(\frac{1}{4}f_1^2- \frac{1}{2}f_1f_2 + \frac{1}{4}f_2^2) + (\frac{1}{4}g_1^2- \frac{1}{2}g_1g_2 + \frac{1}{4}g_2^2)
\end{align*}
Substituting these values into equation \ref{eq:orthog} and simplifying, we find that 
\begin{align\*}
	-h_1 - h_2 &= -\frac{1}{2}f_1f_2 - \frac{1}{2}g_1g_2 \\\\  
	\implies f_1f_2 + g_1g_2 &= 2(h_1 + h_2)
\end{align\*}
Thus, we arrive at our second theorem:

<div class="box theorem">
	<p><strong>Theorem 2</strong>
	Two intersecting circles $C_1$ and $C_2$ with equations
	\begin{align*}
		x^2 + y^2 +f_1x +g_1y + h_1 &= 0 \;\text{ and} \\
		x^2 + y^2 +f_2x +g_2y + h_2 &= 0
	\end{align*}
	respectively, are orthogonal if and only if 
	\[f_1f_2 + g_1g_2 = 2(h_1 + h_2).\]</p>
</div>

**Proof** &ensp; See the above discussion.
### Circles Through Two Points

Suppose now we wish to find the set of all circles that pass through two given points. Let $C_1$ and $C_2$ be circles with equations as before and suppose that they intersect at points $P$ and $Q.$ Then, if $k\neq -1,$
\begin{equation}
	\label{eq:circtwopoints}
	x^2 + y^2 +f_1x +g_1y + h_1 +k(x^2 + y^2 +f_2x +g_2y + h_2) = 0
\end{equation}
represents a circle that passes through $P$ and $Q.$ To convince yourself of this fact, note that the above equation can be turned into a general form for a circle for any value of $k.$ Additionally, the left side equals $0$ because of the general definition of a circle for $C_1$ and $C_2.$

If $k=-1,$ then equation \ref{eq:circtwopoints} represents a line that passes through $P$ and $Q.$

**Remark** &ensp; We can consider the circle $C_2$ to be the $k=\infty$ case. To see this, divide equation \ref{eq:circtwopoints} by $k$ and let $k\rightarrow\infty.$

<div class="box theorem">
	<p><strong>Theorem 3</strong>
	Let $C_1$ and $C_2$ be circles with equations 
	\begin{align*}
		x^2 + y^2 +f_1x +g_1y + h_1 &= 0 \; \text{ and} \\  
		x^2 + y^2 +f_2x +g_2y + h_2 &= 0
	\end{align*}
	that intersect at distinct points $P$ and $Q.$ Then the line and any circle (other than $C_2$) through $P$ and $Q$ have an equation of the form 
	\[x^2 + y^2 +f_1x +g_1y + h_1 +k(x^2 + y^2 +f_2x +g_2y + h_2) = 0\]
	for some number $k\in\R.$</p>
	<p> If $k\neq -1,$ this is an equation for a circle; if $k=-1,$ this is the equation of a line.</p>
</div>
## Focus-Directrix Definition of the Non-Degenerate Conics

So far in this section, we've explored circles by defining it as a set of points at a fixed distance from a fixed point. Now, we wish to explore the other non-degenerate conics. These can be defined as a set of points $P$ that is a distance away from a fixed point, which we call its *focus*. This distance from the focus is a constant multiple, which we call its *eccentricity* $(e)$, of the distance from a fixed line, which we call its *directrix*.

<p class="box def">
	<strong>Eccentricity</strong>
	A non-degenerate conic is an ellipse if $0\leq e < 1,$ a parabola if $e=1,$ or a hyperbola if $e>1.$
</p>

### Parabola $(e=1)$

### Ellipse $(0\leq e < 1)$

### Hyperbola $(e>1)$

## Focal Distance Properties of Ellipse and Hyperbola

## Dandelin Spheres



