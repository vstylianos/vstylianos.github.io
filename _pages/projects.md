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
---



<figure style="position: relative; width: 100%; height: auto;">
    <img class="img-fluid rounded z-depth-1" style="float: left; margin-right: 25px; width: 240px; height: 240px;" src="{{'../assets/img/HAI_logo.png' | relative_url }}" alt="" title="haxp image"/>
    <figcaption style="text-align:left; margin-left: 5px;">
      My current research agenda focuses on developing human-aware AI systems that can: 

      <ul>
          <li>Engage in collaborative problem-solving with human users.</li>
          <li>Provide natural and intuitive explanations for their decisions and behaviors.</li>
          <li>Dynamically update their world models through interactions with users and the environment.</li>
          <li>Infer and adapt to evolving users' (mental) models, such as their knowledge, beliefs, and goals.</li>
      </ul>

      To achieve this, I draw techniques from the realms of formal logic, planning, argumentation, belief revision, machine learning, as well as philosophy, cognitive science, and psychology. Ultimately, I aim to create AI systems that can seamlessly integrate into various real-world scenarios, paving the way for more intuitive, efficient, and trustworthy human-AI collaborative intelligence.  


      <!-- Why formal languages? In short, because they: enable comprehensive examination of their internal properties through both internal verification methods and external conversational interactions; support the addition of new knowledge and allow the operation of programmatic constructs such as compositionality; and facilitate abstractions for explaining decisions using high-level concepts. These traits are crucial for creating explainable AI systems. -->

      <!-- it's expressive, offers structured semantics, and it's traceable.  -->



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