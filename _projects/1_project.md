---
layout: page
title: 2023 A1
description: We love chain and product rules!
img: assets/img/12.jpg
importance: 1
category: General Calculus
related_publications: false
permalink: /Putnam_Problems/2023_A1/
---

<!-- Inline styling for larger text in Google Sites -->
<div style="font-size: 20px; line-height: 1.5;">

<h2 id="problem-setup">Problem Setup</h2>
<p>For a positive integer <span class="math inline">\(n\)</span>, let
<span class="math display">\[f_n(x) = \cos(x) \cos(2x) \cos(3x) \cdots
\cos(nx).\]</span> Find the smallest <span
class="math inline">\(n\)</span> such that <span
class="math inline">\(|f_n&#39;&#39;(0)| &gt; 2023\)</span>.</p>
<h2 id="solution">Solution</h2>
<p>We can first attempt to generalize the first derivative of <span
class="math display">\[f(x) = \cos(x) \cos(2x) \cos(3x) \ldots
\cos(nx)\]</span> using the product rule: <span
class="math display">\[f_{n}&#39;(x) = \left( \cos x
\right)^{&#39;}\left\lbrack \cos(2x)\cos(3x)\ldots\cos(nx) \right\rbrack
+ \cos{x}\lbrack\cos(2x)\cos(3x)\ldots\cos(nx)\rbrack&#39;.\]</span>
This simplifies to: <span class="math display">\[\hspace{27pt} = - \sin
x \cos(2x) \ldots + \cos(x)\left[ \cos(2x)&#39;\left(
\cos(3x)\ldots\cos(nx) \right) + \cos(2x)\left( \cos(3x)\ldots\cos(nx)
\right)^{&#39;} \right].\]</span></p>
<p>Repeating this process, we achieve a series of <span
class="math inline">\(f_{n}(x)\)</span> similar terms with one <span
class="math inline">\(- k \sin(kx)\)</span> term replacing the
respective cosine term:</p>
<p><span class="math display">\[\begin{aligned}
f_{n}^{&#39;}(x) &amp;= \sum_{k=1}^{n} -k \sin(kx) \prod_{\begin{matrix}
j=1 \\
j \neq k
\end{matrix}}^{n} \cos(jx) \\
&amp;= -\sin(x)\cos(2x)\ldots\cos(nx) \\
&amp;\quad - 2\cos(x)\sin(2x)\cos(3x)\ldots\cos(nx) \\
&amp;\quad - \ldots - n\cos(x)\cos(2x)\ldots\cos\left( (n - 1)x
\right)\sin(nx)
\end{aligned}\]</span></p>
<p>As the first derivative of <span
class="math inline">\(f_{n}(x)\)</span> is a collection of terms similar
in form to <span class="math inline">\(f_{n}(x)\)</span> itself, finding
the second derivative is like finding the first derivative <span
class="math inline">\(n\)</span> times:</p>
<p>First term of <span class="math inline">\(f_{n}^{&#39;}(x)\)</span>:
<span class="math display">\[- \sin x
\cos{(2x)\cos{(3x)\ldots\cos(nx)}}\]</span></p>
<p>Taking the derivative: <span class="math display">\[\begin{aligned}
\left( -\sin x \cos(2x) \cos(3x) \ldots \cos(nx) \right)&#39; &amp;=
-\cos(x)\cos(2x)\cos(3x)\ldots\cos(nx) \\
&amp;\quad + 2\sin(x)\sin(2x)\cos(3x)\ldots\cos(nx) \\
&amp;\quad + 3\sin(x)\cos(2x)\sin(3x)\ldots\cos(nx) \\
&amp;\quad + \ldots + n\sin(x)\cos(2x)\ldots \sin(nx)
\end{aligned}\]</span></p>
<p>By similar analysis, the second derivative of the second term is:
<span class="math display">\[\begin{aligned}
(-2\cos(x)\sin(2x)\cos(3x)\ldots\cos(nx))&#39; = -2\lbrack
&amp;-\sin(x)\sin(2x)\ldots\cos(nx) \\
&amp;+ 2\cos(x)\cos(2x)\ldots\cos(nx) \\
&amp;- \ldots - n\cos(x)\sin(2x)\ldots\sin(nx)
\rbrack
\end{aligned}\]</span></p>
<p>As such, the general form of <span
class="math inline">\(f_{n}^{&#39;&#39;}(x)\)</span> looks like: <span
class="math display">\[- f_{n}(x) - 2^{2} f_{n}(x) - 3^{2} f_{n}(x) -
\ldots - n^{2} f_{n}(x) + \text{forms of } f_{n}(x) \text{ containing
sine terms.}\]</span></p>
<p>Evaluating <span class="math inline">\(f_{n}^{&#39;&#39;}(0)\)</span>
becomes elementary, as <span class="math inline">\(f_{n}(0) = \left(
\cos 0 \right)^{n} = 1\)</span>, and every term containing sine becomes
0. Therefore, <span class="math display">\[f_{n}^{&#39;&#39;}(0) = -
(1^{2} + 2^{2} + 3^{2} + \ldots + n^{2}).\]</span></p>
 
</div>
<!-- MathJax Configuration to Scale Font Size for Math -->
<script type="text/javascript">
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']]
    },
    chtml: {
      scale: 0.8  // Scale up the math font size
    }
  };
</script>

<!-- MathJax Script -->
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.0/es5/tex-mml-chtml.js">
</script>

