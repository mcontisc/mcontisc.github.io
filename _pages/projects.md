---
layout: page
title: Research
permalink: /projects/
description: 
nav: true
nav_order: 1
display_categories:
horizontal: true
---

I am passionate about analyzing **complex networks** that represent real-world systems, such as social support interactions, citation networks, and ecological food webs. My primary interest lies in uncovering the underlying patterns within these data and understanding the mechanisms that drive the interactions. These characteristics are typically **latent** and must be inferred from the data, a process known as **network inference**. 

My research focuses on developing **probabilistic generative models**, which are powerful and principled statistical tools designed to identify hidden structures in real-world networks. These methods explain how data may be generated through underlying variables and parameters, enabling the incorporation of **prior knowledge**, accounting for the inherent **uncertainty** in observed data, and uncovering **latent patterns**. A key challenge in this development is ensuring that these models effectively capture the multifaceted complexity of real-world data while remaining **computational efficiency**.

Specifically, I have been working in three different directions: 
<ul>
  <li>Developing methods to perform inference on <b>attributed multilayer networks</b>.</li>
  <li>Designing models to characterize the structural organization of <b>higher-order data</b>.</li>
  <li>Exploring theoretical perspectives for incorporating <b>reciprocity</b> in network models through the relaxation of the <b>conditional independence</b> assumption.</li>
</ul>
For additional information, take a look at the projects pages and the complete list of <a href="{{ '/publications/' | relative_url }}">publications</a>.

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
