---
layout: page
title: 2024 A1
description: A problem about raising integers to an arbitrary power. 
img: assets/img/2024_A1.png
importance: 1
category: Number Theory
related_publications: false
permalink: /Putnam_Problems/2024_A1/
---

<!-- Inline styling for larger text in Google Sites -->
<div style="font-size: 20px; line-height: 1.5;">

<!-- Begin solution -->
<p>Last updated 9/20/25</p>
<h2 id="problem-setup">Problem Setup</h2>
<p>Determine all positive integers <span
class="math inline">\(n\)</span> for which there exist positive integers
<span class="math inline">\(a,b,\)</span> and <span
class="math inline">\(c\)</span> satisfying <span
class="math display">\[\begin{equation*}
    2a^n + 3 b^n = 4c^n
\end{equation*}\]</span></p>
<h2 id="solution">Solution</h2>
<p>For <span class="math inline">\(n=1\)</span>, brief trial and error
will find that <span class="math inline">\(a=3\)</span>, <span
class="math inline">\(b=2\)</span>, <span
class="math inline">\(c=3\)</span> is a solution: <span
class="math display">\[\begin{align*}
    2(3)^1 + 3(2)^1 &amp;= 4(3)^1 \\
    6+6 &amp;= 12
\end{align*}\]</span> For <span class="math inline">\(n=2\)</span>, we
can assume that <span class="math inline">\(a,b,\)</span> and <span
class="math inline">\(c\)</span> are relatively prime. Should there be a
<span class="math inline">\(g = \text{gcd}(a,b,c)\)</span>, then we
could divide out the common term a return the original problem: <span
class="math display">\[\begin{align*}
    2(gx)^n + 3 (gy)^n &amp;= 4 (gz)^n \qquad x,y,z \in \mathbb{N}\\
    g^n(2x^n + 3y^n) &amp;= g^n (4z^n) \\
    2x^n + 3y^n &amp;= 4z^n
\end{align*}\]</span> We can then note that <span
class="math inline">\(3b^2 = 4c^2 - 2a^2\)</span> implies <span
class="math display">\[\begin{equation*}
    a^2+c^2 \equiv 0 \, \text{ mod(3)}
\end{equation*}\]</span> Furthermore, all perfect squares are either 0
(mod 3) or 1 (mod 3): <span class="math display">\[\begin{align*}
    (3r)^2 &amp;= 0 \text{ (mod 3)} \\
    (3r+1)^2 &amp;= (3r)^2 +2(3r) +1  = 3(r^3 +2r) +1  = 1 \text{ (mod
3)} \\
    (3r +2)^2 &amp;= (3r)^2 + 4(3r) + 4 = 3(r^2 +4r + 1) +1 = 1 \text{
(mod 3) }
\end{align*}\]</span> and so <span class="math inline">\(a^2 \equiv c^2
\equiv 0\)</span> (mod 3), since neither <span
class="math inline">\(a^2\)</span> or <span
class="math inline">\(c^2\)</span> can be 1 (mod 3) and retain <span
class="math inline">\(a^2+c^2 \equiv 0\)</span> (mod 3). Therefore,
<span class="math inline">\(a\)</span> and <span
class="math inline">\(c\)</span> are multiples of 3. Then, <span
class="math display">\[\begin{align*}
    3b^2 &amp;= 4(3^2)\Big(\frac{c}{3} \Big)^2 - 2(3^2) \Big(
\frac{a}{3} \Big)^2 \\
    b^2 &amp;= 12 \Big(\frac{c}{3} \Big)^2 - 6  \Big( \frac{a}{3}
\Big)^2
\end{align*}\]</span> which means that <span
class="math inline">\(b\)</span> is also a multiple of 3, which
contradicts our assumption that <span
class="math inline">\(a,b,c\)</span> are relatively prime. There are no
positive integers <span class="math inline">\(a, b,\)</span> and <span
class="math inline">\(c\)</span> for which the given statement is true
for <span class="math inline">\(n=2.\)</span></p>
<p>For the general case of <span class="math inline">\(n &gt;
2\)</span>, we can note that <span class="math inline">\(b\)</span> must
be even, since <span class="math inline">\(3b^n = 4c^n - 2 a^n\)</span>,
and <span class="math inline">\(3b^n\)</span> is even only if <span
class="math inline">\(b\)</span> is even. We can rearrange the original
equation to be of the form <span
class="math display">\[\begin{equation*}
    2a^n = 4c^n-3b^n
\end{equation*}\]</span> which we can consider for the different
parities of <span class="math inline">\(a\)</span> and <span
class="math inline">\(c\)</span>.</p>
<ol>
<li><p>If <span class="math inline">\(a\)</span> and <span
class="math inline">\(c\)</span> are both even, the our original
requirement of <span class="math inline">\(\text{gcd}(a,b,c) =
1\)</span> is violated, since <span class="math inline">\(a,b,c\)</span>
all have a common factor of 2.</p></li>
<li><p>If <span class="math inline">\(a\)</span> and <span
class="math inline">\(c\)</span> are both odd, then for <span
class="math inline">\(x,y,z \in \mathbb{N}\)</span> we have <span
class="math display">\[\begin{align*}
            2(2x+1)^n &amp;= 4(2z+1)^n - 3(2y)^n \\[5pt]
            (2x+1)^n &amp;= 2(2z+1)^n-2^{n-1}(3y^n)
        
\end{align*}\]</span> which cannot be true since the left side is odd
and the right side is even.</p></li>
<li><p>If <span class="math inline">\(a\)</span> is odd and <span
class="math inline">\(c\)</span> is even, then <span
class="math display">\[\begin{align*}
            2(2x+1)^n \neq 4(2z)^n - 3(2y)^n
        
\end{align*}\]</span> by the same argument as in the last case.</p></li>
<li><p>Finally, if <span class="math inline">\(a\)</span> is even and
<span class="math inline">\(c\)</span> is odd, we have <span
class="math display">\[\begin{align*}
            2(2x)^n &amp;= 4(2z+1)^n - 3(2y)^n \\[5pt]
            2^{n-1}x^n &amp;= (2z+1)^n - 2^{n-2}(3y^n)
        
\end{align*}\]</span> which, for <span
class="math inline">\(n&gt;2\)</span>, cannot be true since the right
side is even and the left is odd.</p></li>
</ol>
<p>Therefore, the problem statement is only true for <span
class="math inline">\(n=1\)</span>.</p>

 
</div>

<!-- MathJax Configuration to Scale Font Size for Math -->
<script type="text/javascript">
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']]
    },
    chtml: {
      scale: 0.5  // Scale up the math font size
    }
  };
</script>

<!-- MathJax Script -->
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.0/es5/tex-mml-chtml.js">
</script>

