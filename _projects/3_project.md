---
layout: page
title: markdown test
description: test
img: 
importance: 10
category: Trigonometry
related_publications: false
permalink: /Putnam_Problems/mtest/
---

# Problem Setup. {#problem-setup. .unnumbered}

Let $d_n$ be the determinant of the $n\times n$ matrix whose entries,
from left to right and then from top to bottom, are
$\cos1,\cos2,\dots,\cos{n^2}$. For example, $$d_3 =
        \begin{vmatrix}
            \cos1 & \cos2 & \cos3 \\
            \cos4 & \cos5 & \cos6 \\
            \cos7 & \cos8 & \cos9
        \end{vmatrix}$$ Note that the argument of $\cos$ is always in
radians, not degrees. Evaluate $\lim_{n\rightarrow\infty}d_n$.

# Solution. {#solution. .unnumbered}

To begin, let us compute $d_3$ explicitly: $$\begin{aligned}
        d_3 &=
        \begin{vmatrix}
            \cos1 & \cos2 & \cos3 \\
            \cos4 & \cos5 & \cos6 \\
            \cos7 & \cos8 & \cos9
        \end{vmatrix} \\[5pt]
        &= \cos7 
        \begin{vmatrix}
            \cos2 & \cos3 \\
            \cos5 & \cos6 \\
        \end{vmatrix}
        - \cos8
        \begin{vmatrix}
            \cos1 & \cos3 \\
            \cos4 & \cos6 \\
        \end{vmatrix}
        + \cos9
        \begin{vmatrix}
            \cos1 & \cos2 \\
            \cos4 & \cos5 \\
        \end{vmatrix} \\[2.5pt]
        &= \cos7(\cos2\cos6-\cos3\cos5)-\cos8(\cos1\cos6-\cos3\cos4)+\cos9(\cos1\cos5-\cos2\cos4) 
    
\end{aligned}$$ Note that each $2 \times 2$ determinant is of the form
$(\cos a\cos b-\cos c \cos d)$, where $a + b = c + d$. This pattern
works nicely with the trigonometric identity
$\cos\alpha\cos\beta=\frac{\cos(\alpha+\beta)+\cos(\alpha-\beta)}{2}$:
$$\begin{aligned}
        d_3 = \quad \cos7\Big(\frac{\cos8+\cos4}{2}-\frac{\cos8+\cos2}{2}\Big) \\[2.5pt]
        -\cos8\Big( \frac{\cos7+\cos5}{2} - \frac{\cos7+\cos1}{2}\Big) \\[2.5pt]
        + \cos9\Big( \frac{\cos6+\cos4}{2}-\frac{\cos6+\cos2}{2} \Big)
    
\end{aligned}$$ We see that the $\cos(\alpha+\beta)$ terms cancel out,
$$\begin{aligned}
        d_3 = \frac{\cos7}{2}(\cos4 - \cos2)-\frac{\cos8}{2}(\cos5 - \cos1)+\frac{\cos9}{2}(\cos4 - \cos2)
    
\end{aligned}$$ Regrouping, $$\begin{aligned}
        d_3 = \Big( \frac{\cos1\cos8}{2} - \frac{\cos2\cos7}{2} \Big) + \Big( \frac{\cos4\cos7}{2}-\frac{\cos2\cos9}{2} \Big) + \Big( \frac{\cos4\cos9}{2}-\frac{\cos5\cos8}{2} \Big)
    
\end{aligned}$$ Applying the cosine identity again, $$\begin{aligned}
        d_3 &= \frac{1}{2}\Big(\frac{\cos3-\cos7}{2}\Big) + \frac{1}{2}\Big(\frac{\cos5-\cos3}{2} \Big) + \frac{1}{2}\Big(\frac{\cos7-\cos5}{2}\Big) \\[5pt]
        &= 0
    
\end{aligned}$$ Our guess, then, is $\lim_{n\rightarrow\infty}d_n=0$.
One way to show this for the general case of $d_n$, is to show that two
columns are linearly dependent. The general form of $d_n$ is $$d_n =
        \begin{vmatrix}
            \cos1 & \cos2 & \cos3 & ... & \cos n\\
            \cos(n+1) & \cos(n+2) & \cos(n+3) & ... & \cos 2n \\
            \cos(2n+1) & \cos(2n+2) & \cos(2n+3) & ... & \cos3n \\
            \cos(3n+1) & \cos(3n+2) & \cos(3n+3) & ... & \cos4n \\
            \vdots     & \vdots     & \vdots     & \vdots & \vdots \\
            \cos\Big((n-1)n + 1\Big) & \cos\Big((n-1)n + 2\Big) & \cos\Big((n-1)n + 3\Big) & \dots & \cos n^2
        \end{vmatrix}$$ We can add column three to column one without
changing the determinant, $$\begin{aligned}
        d_n =
        \begin{vmatrix}
            \cos1 + \cos3 & \cos2 & \cos3 & ... & \cos n\\
            \cos(n+1) + \cos(n+3) & \cos(n+2) & \cos(n+3) & ... & \cos 2n \\
            \cos(2n+1) + \cos(2n+3) & \cos(2n+2) & \cos(2n+3) & ... & \cos3n \\
            \cos(3n+1) + \cos(3n+3) & \cos(3n+2) & \cos(3n+3) & ... & \cos4n \\
            \vdots     & \vdots     & \vdots     & \vdots & \vdots \\
            \cos\Big((n-1)n + 1\Big) + \cos\Big((n-1)n + 3\Big) & \cos\Big((n-1)n + 2\Big) & \cos\Big((n-1)n + 3\Big) & \dots & \cos n^2
        \end{vmatrix}
    
\end{aligned}$$ Using another trig identity,
$\cos\alpha+\cos\beta = 2\cos\frac{\alpha+\beta}{2}\cos\frac{\alpha-\beta}{2}$,
to simplify column one: $$\begin{aligned}
            d_n =
        \begin{vmatrix}
            2\cos2\cos1 & \cos2 & \cos3 & ... & \cos n\\
            2\cos(n + 2)\cos1 & \cos(n+2) & \cos(n+3) & ... & \cos 2n \\
            2\cos(2n+2)\cos1 & \cos(2n+2) & \cos(2n+3) & ... & \cos3n \\
            2\cos(3n+2)\cos1 & \cos(3n+2) & \cos(3n+3) & ... & \cos4n \\
            \vdots     & \vdots     & \vdots     & \vdots & \vdots \\
            2\cos\Big((n-1)n + 2\Big)\cos1 & \cos\Big((n-1)n + 2\Big) & \cos\Big((n-1)n + 3\Big) & \dots & \cos n^2
        \end{vmatrix}
    
\end{aligned}$$ Finally, we can note that column one is a multiple of
column two and therefore the two columns are linearly dependent; the
determinant of a matrix with dependent columns is $0$. Therefore,
$\lim_{n\rightarrow\infty}d_n = 0$.