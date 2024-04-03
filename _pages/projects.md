---
layout: page
title: research
permalink: /projects/
description: 
nav: true
nav_order: 2
display_categories: 
horizontal: false
---



<figure style="position: relative; width: 100%; height: auto;">
    <img class="img-fluid rounded z-depth-1" style="float: left; margin-right: 10px; width: 240px; height: 240px;" src="{{ '/assets/img/HAI_logo.png' | relative_url }}" alt="" title="haxp image"/>
    <figcaption style="text-align:left; margin-left: 5px;">
      My research interests are currently surrounding Human-Aware AI, that is, an area in AI concerning the design of AI agents that can interact (in some manner) with humans in a natural fashion. Specifically, I've been using logic-based techniques to create explanation generation frameworks for various problems, such as planning and scheduling. Why logic? In short, because it's expressive, offers structured semantics, and it's traceable. Below you can see some of the projects related to my research.
    </figcaption>
    <div style="clear: both;"></div>
</figure>





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