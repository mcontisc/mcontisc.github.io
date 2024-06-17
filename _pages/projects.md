---
layout: page
title: Research
permalink: /projects/
description: 
nav: true
nav_order: 1
display_categories: [work, fun]
horizontal: true
---

I am interested in developing **probabilistic generative models** to 

I am interested in analysing 

In this thesis, we present principled and efficient approaches that aim to broaden the range of techniques available for modelling complex networks. Specifically, we work in three principal directions: i) developing flexible methods to perform inference on attributed multilayer networks, ii) exploring innovative theoretical perspectives for incorporating reciprocity and loosening the assumption of conditional independence in network models, iii) designing foundational models to characterize the structural organization of higher-order data.
We first extend standard generative models for the analysis of multilayer networks to integrate node metadata into the inference process with the network topology. In addition to applying these methods to already explored real-world data, such as social and biological networks, we introduce this methodology to another field for the first time, that is patent citation networks. We show how incorporating additional information not only boosts performance, but also leads to more interpretable structures.
Next, we propose approaches to handle the pairwise dependencies between two directed edges connecting node pairs, which come with the relaxation of the assumption that edges are independent of each other. We demonstrate the flexibility and relevancy of our mathematical frameworks in various contexts, such as the analysis of dynamic networks, identification of anomalies, and estimation of unobserved network structures using multiple reports. By explicitly accounting for reciprocity, it improves edge prediction and network reconstruction, while also shedding light on the underlying mechanisms driving edge formation.
Finally, we present principled methods to define and identify the mesoscale organization of higher- order data. We evaluate their effectiveness on a variety of small- and large-scale real-world systems. Notably, these models display good performance in effectively retrieving both robust and flexible community structures, while reliably predicting higher-order interactions of arbitrary size. As an additional contribution, we present a newly developed Python library specifically designed for analyzing data with higher-order interactions.


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
