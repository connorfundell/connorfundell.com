---
layout: page
title: Chinese remainder theorem
description: A theorem for determining an unknown integer from known remainders.
img: assets/img/chinese.png
importance: 1
category: Number_Theory
related_publications: false
permalink: /theorems_and_such/chinese_remainder
---

<!-- Inline styling for larger text in Google Sites -->
<div style="font-size: 20px; line-height: 1.5;">

<p>Last updated on 10/5/25</p>
<p>Before formally stating the theorem, let’s build up some intuition
for the main result. Imagine that we have a natural number, <span
class="math inline">\(n\)</span>, which is unknown, and suppose the only
information we are given about the number is <span
class="math display">\[\begin{align*}
    n&amp;\equiv 2 \text{ (mod 3)} \\
    n &amp;\equiv 1 \text{ (mod 2)}
\end{align*}\]</span></p>
<p>Are we able to narrow down what values of <span
class="math inline">\(n\)</span> are possible given these two
statements? Writing out some of the first numbers, we can begin to
eliminate possible choices. First, all numbers that do not satisfy <span
class="math inline">\(x\equiv 2 \text{ (mod 3)}\)</span> - 2, 5, etc. -
can be removed from the list of possible choices. <span
class="math display">\[\begin{equation*}
    \cancel{1} \quad 2 \quad \cancel{3} \quad \cancel{4} \quad 5 \quad
\cancel{6}
\end{equation*}\]</span> Next, we remove all numbers that do not satisfy
<span class="math inline">\(x\equiv 1 \text{ (mod 2)}\)</span>: <span
class="math display">\[\begin{equation*}
    \cancel{1} \quad \cancel{2} \quad \cancel{3} \quad \cancel{4} \quad
\tikz[baseline=(char.base)]{
            \node[shape=circle,draw,inner sep=2pt] (char) {5};} \quad
\cancel{6}
\end{equation*}\]</span> Therefore, 5 is the only number less than 6
that satisfies the given modular relations.</p>
<p>Let’s try another example, this time with <span
class="math display">\[\begin{align*}
    n &amp;\equiv 1 \text{ (mod 3)} \\
    n&amp;\equiv 2 \text{ (mod 5)}
\end{align*}\]</span> Crossing off number that do not satisfy the first
relation, <span class="math display">\[\begin{equation*}
    1 \quad \cancel{2} \quad \cancel{3} \quad 4 \quad \cancel{5} \quad
\cancel{6} \quad 7 \quad \cancel{8} \quad \cancel{9} \quad 10 \quad
\cancel{11} \quad \cancel{12} \quad 13 \quad \cancel{14} \quad
\cancel{15}
\end{equation*}\]</span> Now the second relation, <span
class="math display">\[\begin{equation*}
    \cancel{1} \quad \cancel{2} \quad \cancel{3} \quad \cancel{4} \quad
\cancel{5} \quad \cancel{6} \quad \tikz[baseline=(char.base)]{
            \node[shape=circle,draw,inner sep=2pt] (char) {7};} \quad
\cancel{8} \quad \cancel{9} \quad \cancel{10} \quad \cancel{11} \quad
\cancel{12} \quad \cancel{13} \quad \cancel{14} \quad \cancel{15}
\end{equation*}\]</span> Thus, 7 must be the only natural number less
than 15 that satisfies the limited information given about <span
class="math inline">\(n\)</span>.</p>
<p>What then do we notice from these two examples? Well, if we have an
unknown integer which has known remainders for some given integers, then
there is only one number less than the product of the dividing integers
that satisfies the modular relationships. This is the main idea of the
Chinese remainder theorem. A more formal statement follows.</p>
<p><strong>The Chinese remainder theorem statement.</strong><a href="https://en.wikipedia.org/wiki/Chinese_remainder_theorem"> (source)</a></p> 
<p>Let <span class="math inline">\(n_1, \dots , n_k\)</span> be integer
divisors greater than 1, and let <span
class="math inline">\(N=n_1n_2\dots n_i\)</span>. If all <span
class="math inline">\(n_i\)</span> are relatively prime (pairwise
coprime), and if <span class="math inline">\(a_1, \dots, a_k\)</span>
are integers such that <span class="math inline">\(0\leq a_i &lt;
n_i\)</span> for every <span class="math inline">\(i\)</span>, then
there is one and only one integer <span class="math inline">\(x\)</span>
such that <span class="math inline">\(0\le x &lt; N\)</span> where the
remainder of <span class="math inline">\(x / n\)</span> is <span
class="math inline">\(a_i\)</span> for every <span
class="math inline">\(i\)</span>.</p>
<p>Perhaps more clearly the theorem can be restated in terms of
congruences. Using the same definitions as above, then the system <span
class="math display">\[\begin{align*}
    x &amp;\equiv a_1 \text{ (mod } n_1 \text{)} \\
    \vdots \\
    x &amp;\equiv a_k \text{ (mod } n_k \text{)}
\end{align*}\]</span> has a solution, and any two solutions <span
class="math inline">\(x_1\)</span> and <span
class="math inline">\(x_2\)</span> are congruent modulo <span
class="math inline">\(N\)</span>: <span
class="math display">\[\begin{equation*}
    x_1 \equiv x_2 \text{ (mod N)}
\end{equation*}\]</span></p>

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
