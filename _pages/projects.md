---
layout: about
title: research
permalink: /projects/
description: 
nav: true
nav_order: 2
display_categories: 
horizontal: false
selected_papers: true
hide_title: true
---

<div class="col-sm-8 mx-auto">
{% include figure.liquid path="assets/img/haip_full_web.png" class="img-fluid" alt="Laboratory for Human-AI Interaction & Psychology" %}
</div>

The main goal of the HAIP lab is to enable meaningful and effective **human-AI synergy**. We pursue this goal along two axes:

**Synergistic Human-AI Decision-Making:** The goal here is to design AI agents that reason *with* people rather than *for* them. For example, such an agent works from a shared, explicit representation of the decision and its reasons, keeps a model of what the person knows and believes, and revises both as the interaction unfolds. To do this, we use a lot of neurosymbolic AI methods, such as combining logic, and computational argumentation with neural-based models.

**Human-AI Psychology:** We also study how people and AI agents behave, both on their own and together, and how they influence one another under various scenarios. We do this mechanistically (à la neuroscience) and behaviorally (à la cogsci and psychology).



<br> <br>
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
    <div class="row row-cols-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="grid">
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
    <div class="row row-cols-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="grid">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
