---
layout: page
title: 2023 A1
description: A problem with gratuitous use of the chain and product rules.
img: 
importance: 1
category: General Calculus
related_publications: false
permalink: /Putnam_Problems/2023_A1/
---

<!-- Inline styling for larger text in Google Sites -->
<div style="font-size: 20px; line-height: 1.5;">

<!-- Begin solution -->
<h2 id="problem-setup">Problem Setup</h2>
<p>
    For a positive integer <span class="math inline">\(n\)</span>, let
</p>
<div class="math display">
    \[f_n(x) = \cos(x) \cos(2x) \cos(3x) \cdots \cos(nx).\]
</div>
<p>
    Find the smallest <span class="math inline">\(n\)</span> such that 
    <span class="math inline">\(|f_n''(0)| > 2023\)</span>.
</p>

<h2 id="solution">Solution</h2>

<p>We can first attempt to generalize the first derivative of:</p>
<div class="math display">
    \[f(x) = \cos(x) \cos(2x) \cos(3x) \ldots \cos(nx)\]
</div>
<p>using the product rule:</p>
<div class="math display">
    \[
    f_{n}'(x) = (\cos x)' \left[\cos(2x) \cos(3x) \ldots \cos(nx)\right] 
    + \cos(x) \left[\cos(2x) \cos(3x) \ldots \cos(nx)\right]'
    \]
</div>
<p>This simplifies to:</p>
<div class="math display">
    \[
    -\sin(x) \cos(2x) \ldots + \cos(x) \left[\cos(2x)' \left(\cos(3x) \ldots \cos(nx)\right) 
    + \cos(2x) \left(\cos(3x) \ldots \cos(nx)\right)'\right]
    \]
</div>

<p>Repeating this process, we achieve a series of 
<span class="math inline">\(f_{n}(x)\)</span> similar terms with one 
<span class="math inline">\(- k \sin(kx)\)</span> term replacing the respective cosine term:</p>

<div class="math display">
    \[
    \begin{aligned}
    f_{n}'(x) &= \sum_{k=1}^{n} -k \sin(kx) \prod_{\substack{j=1 \\ j \neq k}}^{n} \cos(jx) \\
              &= -\sin(x)\cos(2x)\ldots\cos(nx) \\
              &\quad - 2\cos(x)\sin(2x)\cos(3x)\ldots\cos(nx) \\
              &\quad - \ldots - n\cos(x)\cos(2x)\ldots\cos((n-1)x)\sin(nx)
    \end{aligned}
    \]
</div>

<p>
    As the first derivative of <span class="math inline">\(f_{n}(x)\)</span> is a collection of terms similar 
    in form to <span class="math inline">\(f_{n}(x)\)</span> itself, finding the second derivative is like 
    finding the first derivative repeatedly:
</p>

<p>First term of <span class="math inline">\(f_{n}'(x)\)</span>:</p>
<div class="math display">
    \[-\sin(x) \cos(2x) \cos(3x) \ldots \cos(nx)\]
</div>

<p>Taking the derivative:</p>
<div class="math display">
    \[
    \begin{aligned}
    \left(-\sin(x) \cos(2x) \cos(3x) \ldots \cos(nx)\right)' 
    &= -\cos(x)\cos(2x)\cos(3x)\ldots\cos(nx) \\
    &\quad + 2\sin(x)\sin(2x)\cos(3x)\ldots\cos(nx) \\
    &\quad + 3\sin(x)\cos(2x)\sin(3x)\ldots\cos(nx) \\
    &\quad + \ldots + n\sin(x)\cos(2x)\ldots\sin(nx)
    \end{aligned}
    \]
</div>

<p>By a similar analysis, the second derivative of the second term is:</p>
<p>
\[
\left(-2\cos(x)\sin(2x)\cos(3x)\ldots\cos(nx)\right)'
\]
</p>
<p>
\[
= -2 \left[-\sin(x)\sin(2x)\ldots\cos(nx) + 2\cos(x)\cos(2x)\ldots\cos(nx) - \ldots - n\cos(x)\sin(2x)\ldots\sin(nx)\right].
\]
</p>

<p>
    Thus, the general form of <span class="math inline">\(f_{n}''(x)\)</span> looks like:
</p>
<div class="math display">
    \[-f_{n}(x) - 2^2 f_{n}(x) - 3^2 f_{n}(x) - \ldots - n^2 f_{n}(x) + \text{forms of } f_{n}(x) \text{ containing sine terms.}\]
</div>

<p>
    Evaluating <span class="math inline">\(f_{n}''(0)\)</span> becomes straightforward since 
    <span class="math inline">\(f_{n}(0) = (\cos 0)^n = 1\)</span> and every sine term vanishes. Therefore:
</p>
<div class="math display">
    \[f_{n}''(0) = -(1^2 + 2^2 + 3^2 + \ldots + n^2).\]
</div>

<h3>Finishing the Problem</h3>
<p>There are two approaches:</p>

<p>1.) <em>The Clever Way</em>:</p>
<p>
    According to Kedlaya’s solution, the sum <span class="math inline">\(\left| f_n''(0) \right|\)</span> simplifies to:
</p>
<div class="math display">
    \[\frac{n(n + 1)(2n + 1)}{6}\]
</div>
<p>
    Using this formula, finding the smallest <span class="math inline">\(n\)</span> such that 
    <span class="math inline">\(\left| f_n''(0) \right| > 2023\)</span> is straightforward.
</p>

<p>2.) <em>The Way I Found \(n\)</em>:</p>
<p>
    I expanded the series term by term until reaching the required value. I won't bore you with the simple multiplication and addition. We find:
</p>
<div class="math display">
    \[\left| f_{17}''(0) \right| = 1785, \quad \left| f_{18}''(0) \right| = 2109\]
</div>

<p>Therefore, the solution to the problem is <span class="math inline">\(n = 18\)</span>. <span class="math inline">\(\square\)</span></p>

 
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

