---
layout: math
title: Conic Sections and Conics
usemathjax: true
description: A brief review of conic sections and conics.
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

Recall that the distance between two points $p_1=(x_1, y_1)$ and $p_2=(x_2, y_2)$ in $\R^2$ is given by the formula $\text{dist}(p_1,p_2) = \sqrt{(x_1-x_2)^2+(y_1-y_2)^2}$.

Then for any circle with center $C=(a, b)$, we have that any arbitrary point, $(x,y)$, on the circle is given by \\[r^2=(x-a)^2+(y-b)^2\\] where $r$ is the radius.

<div class="box example">
	<p><strong>Example 1</strong>
	Determine the equation of each of the circles with the following center and radius: <br>  
		(a) center: origin, radius: $3$ <br>  
		(b) center: $(4,2)$, radius: $7$<br>
		(c) center: $(\sqrt{2}, 3)$, radius: $\sqrt[3]{7}$ <br></p>
	<p><strong>Solution</strong><br>
	Here, we're just plugging numbers into the formula we found earlier:</p>
		<p>(a) $(x-0)^2 + (y-0)^2 = 3^2 \implies x^2+y^2=9$ </p>
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

Recall [completing the square](https://www.mathsisfun.com/algebra/completing-square.html){:target="_blank" rel="noopener noreferrer"}. Isolate terms that involve only $x$ and terms that involve only $y$. Complete the squares of these two expressions and plug back into the original equation. For example, consider \\[x^2=y^2-2x-4y+2=0.\\] Writing only the terms that involve $x$ and the terms that involve $y$ and completing the square, we obtain \\[x^2-2x = (x-1)^2-1\\] \\[y^2-4y=(y-2)^2-4.\\]

Plugging this back into our original equation, we get 
\\[\begin{align}
	(x-1)^2-1+(y-2)^2-4+2 &= 0 \\\\ (x-1)^2+(y-2)^2 &= 3
\end{align}\\]
We can now easily see that the center is $(1,2)$ and the radius is $\sqrt{3}$.

Similarly, if we apply the same method to the general form $x^2 + y^2 +fx +gy + h = 0,$ we obtain the equation \\[\left(x+\frac{1}{2}f\right)^2 +\left(y+\frac{1}{2}g\right)^2 = \frac{1}{4}f^2+\frac{1}{4}g^2-h.\\]

<div class="box theorem">
	<p><strong>Theorem 1</strong>
	An equation of the form \[x^2 + y^2 +fx +gy + h = 0\] represents a circle with</p>
	<p style="text-align:center;">center $(-\frac{1}{2}f, -\frac{1}{2}g)$ and radius $\sqrt{\frac{1}{4}f^2=\frac{1}{4}g^2-h},$</p>
	<p>Provided that $\frac{1}{4}f^2+\frac{1}{4}g^2-h > 0.$</p>
</div>