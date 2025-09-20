---
layout: page
title: 2009 A3
description: A problem with determinants and cosine identities.
img: assets/img/2009_A3.jpg
importance: 2
category: Trigonometry
related_publications: false
permalink: /Putnam_Problems/2009_A3/
---

<h1 class="unnumbered" id="problem-setup.">Problem Setup.</h1>
<p>Let <span class="math inline">\(d_n\)</span> be the determinant of
the <span class="math inline">\(n\times n\)</span> matrix whose entries,
from left to right and then from top to bottom, are <span
class="math inline">\(\cos1,\cos2,\dots,\cos{n^2}\)</span>. For example,
<span class="math display">\[d_3 =
        \begin{vmatrix}
            \cos1 &amp; \cos2 &amp; \cos3 \\
            \cos4 &amp; \cos5 &amp; \cos6 \\
            \cos7 &amp; \cos8 &amp; \cos9
        \end{vmatrix}\]</span> Note that the argument of <span
class="math inline">\(\cos\)</span> is always in radians, not degrees.
Evaluate <span
class="math inline">\(\lim_{n\rightarrow\infty}d_n\)</span>.</p>
<h1 class="unnumbered" id="solution.">Solution.</h1>
<p>To begin, let us compute <span class="math inline">\(d_3\)</span>
explicitly: <span class="math display">\[\begin{aligned}
        d_3 &amp;=
        \begin{vmatrix}
            \cos1 &amp; \cos2 &amp; \cos3 \\
            \cos4 &amp; \cos5 &amp; \cos6 \\
            \cos7 &amp; \cos8 &amp; \cos9
        \end{vmatrix} \\[5pt]
        &amp;= \cos7
        \begin{vmatrix}
            \cos2 &amp; \cos3 \\
            \cos5 &amp; \cos6 \\
        \end{vmatrix}
        - \cos8
        \begin{vmatrix}
            \cos1 &amp; \cos3 \\
            \cos4 &amp; \cos6 \\
        \end{vmatrix}
        + \cos9
        \begin{vmatrix}
            \cos1 &amp; \cos2 \\
            \cos4 &amp; \cos5 \\
        \end{vmatrix} \\[2.5pt]
        &amp;=
\cos7(\cos2\cos6-\cos3\cos5)-\cos8(\cos1\cos6-\cos3\cos4)+\cos9(\cos1\cos5-\cos2\cos4)
    
\end{aligned}\]</span> Note that each <span class="math inline">\(2
\times 2\)</span> determinant is of the form <span
class="math inline">\((\cos a\cos b-\cos c \cos d)\)</span>, where <span
class="math inline">\(a + b = c + d\)</span>. This pattern works nicely
with the trigonometric identity <span
class="math inline">\(\cos\alpha\cos\beta=\frac{\cos(\alpha+\beta)+\cos(\alpha-\beta)}{2}\)</span>:
<span class="math display">\[\begin{aligned}
        d_3 = \quad
\cos7\Big(\frac{\cos8+\cos4}{2}-\frac{\cos8+\cos2}{2}\Big) \\[2.5pt]
        -\cos8\Big( \frac{\cos7+\cos5}{2} - \frac{\cos7+\cos1}{2}\Big)
\\[2.5pt]
        + \cos9\Big( \frac{\cos6+\cos4}{2}-\frac{\cos6+\cos2}{2} \Big)
    
\end{aligned}\]</span> We see that the <span
class="math inline">\(\cos(\alpha+\beta)\)</span> terms cancel out,
<span class="math display">\[\begin{aligned}
        d_3 = \frac{\cos7}{2}(\cos4 - \cos2)-\frac{\cos8}{2}(\cos5 -
\cos1)+\frac{\cos9}{2}(\cos4 - \cos2)
    
\end{aligned}\]</span> Regrouping, <span
class="math display">\[\begin{aligned}
        d_3 = \Big( \frac{\cos1\cos8}{2} - \frac{\cos2\cos7}{2} \Big) +
\Big( \frac{\cos4\cos7}{2}-\frac{\cos2\cos9}{2} \Big) + \Big(
\frac{\cos4\cos9}{2}-\frac{\cos5\cos8}{2} \Big)
    
\end{aligned}\]</span> Applying the cosine identity again, <span
class="math display">\[\begin{aligned}
        d_3 &amp;= \frac{1}{2}\Big(\frac{\cos3-\cos7}{2}\Big) +
\frac{1}{2}\Big(\frac{\cos5-\cos3}{2} \Big) +
\frac{1}{2}\Big(\frac{\cos7-\cos5}{2}\Big) \\[5pt]
        &amp;= 0
    
\end{aligned}\]</span> Our guess, then, is <span
class="math inline">\(\lim_{n\rightarrow\infty}d_n=0\)</span>. One way
to show this for the general case of <span
class="math inline">\(d_n\)</span>, is to show that two columns are
linearly dependent. The general form of <span
class="math inline">\(d_n\)</span> is <span class="math display">\[d_n =
        \begin{vmatrix}
            \cos1 &amp; \cos2 &amp; \cos3 &amp; ... &amp; \cos n\\
            \cos(n+1) &amp; \cos(n+2) &amp; \cos(n+3) &amp; ... &amp;
\cos 2n \\
            \cos(2n+1) &amp; \cos(2n+2) &amp; \cos(2n+3) &amp; ... &amp;
\cos3n \\
            \cos(3n+1) &amp; \cos(3n+2) &amp; \cos(3n+3) &amp; ... &amp;
\cos4n \\
            \vdots     &amp; \vdots     &amp; \vdots     &amp; \vdots
&amp; \vdots \\
            \cos\Big((n-1)n + 1\Big) &amp; \cos\Big((n-1)n + 2\Big)
&amp; \cos\Big((n-1)n + 3\Big) &amp; \dots &amp; \cos n^2
        \end{vmatrix}\]</span> We can add column three to column one
without changing the determinant, <span
class="math display">\[\begin{aligned}
        d_n =
        \begin{vmatrix}
            \cos1 + \cos3 &amp; \cos2 &amp; \cos3 &amp; ... &amp; \cos
n\\
            \cos(n+1) + \cos(n+3) &amp; \cos(n+2) &amp; \cos(n+3) &amp;
... &amp; \cos 2n \\
            \cos(2n+1) + \cos(2n+3) &amp; \cos(2n+2) &amp; \cos(2n+3)
&amp; ... &amp; \cos3n \\
            \cos(3n+1) + \cos(3n+3) &amp; \cos(3n+2) &amp; \cos(3n+3)
&amp; ... &amp; \cos4n \\
            \vdots     &amp; \vdots     &amp; \vdots     &amp; \vdots
&amp; \vdots \\
            \cos\Big((n-1)n + 1\Big) + \cos\Big((n-1)n + 3\Big) &amp;
\cos\Big((n-1)n + 2\Big) &amp; \cos\Big((n-1)n + 3\Big) &amp; \dots
&amp; \cos n^2
        \end{vmatrix}
    
\end{aligned}\]</span> Using another trig identity, <span
class="math inline">\(\cos\alpha+\cos\beta =
2\cos\frac{\alpha+\beta}{2}\cos\frac{\alpha-\beta}{2}\)</span>, to
simplify column one: <span class="math display">\[\begin{aligned}
            d_n =
        \begin{vmatrix}
            2\cos2\cos1 &amp; \cos2 &amp; \cos3 &amp; ... &amp; \cos n\\
            2\cos(n + 2)\cos1 &amp; \cos(n+2) &amp; \cos(n+3) &amp; ...
&amp; \cos 2n \\
            2\cos(2n+2)\cos1 &amp; \cos(2n+2) &amp; \cos(2n+3) &amp; ...
&amp; \cos3n \\
            2\cos(3n+2)\cos1 &amp; \cos(3n+2) &amp; \cos(3n+3) &amp; ...
&amp; \cos4n \\
            \vdots     &amp; \vdots     &amp; \vdots     &amp; \vdots
&amp; \vdots \\
            2\cos\Big((n-1)n + 2\Big)\cos1 &amp; \cos\Big((n-1)n +
2\Big) &amp; \cos\Big((n-1)n + 3\Big) &amp; \dots &amp; \cos n^2
        \end{vmatrix}
    
\end{aligned}\]</span> Finally, we can note that column one is a
multiple of column two and therefore the two columns are linearly
dependent; the determinant of a matrix with dependent columns is <span
class="math inline">\(0\)</span>. Therefore, <span
class="math inline">\(\lim_{n\rightarrow\infty}d_n = 0\)</span>.</p>