---
layout: page
title: Theorems & Properties
permalink: /theorems/
description: A 'dictionary' of theorems and principles that are useful in studying for the Putnam and as a personal reference. 
nav: false
display_categories: [Miscellaneous]
horizontal: false
---

<!-- pages/theorems.md -->
<div class="theorems">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized theorems -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_theorems = site.theorems | where: "category", category %}
  {% assign sorted_theorems = categorized_theorems | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_theorems %}
      {% include theorems_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_theorems %}
      {% include theorems.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display theorems without categories -->

{% assign sorted_theorems = site.theorems | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_theorems %}
      {% include theorems_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_theorems %}
      {% include theorems.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
