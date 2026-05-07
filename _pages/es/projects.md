---
lang: es
layout: single
title: "Proyectos"
permalink: /es/projects/
author_profile: true
---

Aquí presento una selección de mi trabajo en **Optimización Industrial**, **Inteligencia Artificial** y **Simulación**. Estos proyectos demuestran la aplicación de métodos cuantitativos avanzados para resolver desafíos industriales del mundo real.

## Optimización e Investigación de Operaciones
{% for post in site.projects %}
  {% if post.tags contains "Optimization" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Inteligencia Artificial y Analítica
{% for post in site.projects %}
  {% if post.tags contains "AI" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Simulación y Sistemas Estocásticos
{% for post in site.projects %}
  {% if post.tags contains "Simulation" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
