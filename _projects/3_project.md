---
layout: page
title: Pigeonhole principle
description: A principle for distributing items.
img: assets/img/pigeon.png
importance: 1
category: Miscellaneous
related_publications: false
permalink: /theorems_and_such/pigeonhole
---

<!-- Inline styling for larger text in Google Sites -->
<div style="font-size: 20px; line-height: 1.5;">

<!-- Begin solution -->
<p>Last updated on 9/15/25</p>
<h2 id="pigeonhole-principle">Pigeonhole principle</h2>
<p>Perhaps the very first idea I was introduced to when learning about
the Putnam was the Pigeonhole principle. The idea itself is pretty
intuitive and generally reads as follows:</p>
<p><em>Suppose there are <span class="math inline">\(n+1\)</span> items
that must be distributed into <span class="math inline">\(n\)</span>
bins. At least one bin contains two or more items.</em></p>
<p>This principle is one that most everyone subconsciously follows on
their day to day; if you have three apples and you only have two
baskets, of course one of the baskets will contain at least two of the
apples. Although a simple principle, it has its applications to the
Putnam. Let’s look at some examples.</p>
<h2 id="examples">Examples</h2>
<p><strong>Putnam 2002 A2.</strong> <em>Given any five points on a
sphere, show that some four of them must lie on a closed
hemisphere.</em></p>
<p>Recall that for any two points on a sphere, there is a unique great
circle (a circle on the sphere that has the same radius of the sphere)
that connects them, splitting the sphere in half. Picking any two of the
five points to be on a great circle leaves three points to be
distributed between two hemispheres. By the pigeonhole principle, two of
these points must lie on the same hemisphere, and therefore four points
must lie on the same closed hemisphere (two on the edge + two on the
"face"). Of course, more than two points can lie on the same great
circle in which case the property is automatically true.</p>

 
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
