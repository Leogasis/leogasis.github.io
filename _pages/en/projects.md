---
lang: en
layout: single
title: "Projects"
permalink: /en/projects/
author_profile: true
---

Here is a selection of my work in **Industrial Optimization**, **Artificial Intelligence**, and **Simulation**. These projects demonstrate the application of advanced quantitative methods to solve real-world industrial challenges.

## Optimization & Operations Research
{% for post in site.projects %}
  {% if post.tags contains "Optimization" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Artificial Intelligence & Analytics
{% for post in site.projects %}
  {% if post.tags contains "AI" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Simulation & Stochastic Systems
{% for post in site.projects %}
  {% if post.tags contains "Simulation" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
