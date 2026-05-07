---
lang: es
layout: single
title: "Divulgación"
permalink: /divulgacion/
author_profile: true
---

En esta sección comparto artículos, charlas y recursos dedicados a la **divulgación científica**. Mi objetivo es acercar la ingeniería industrial, la optimización y la inteligencia artificial a un público más amplio, fomentando la curiosidad y el entendimiento de estas disciplinas.

{% for item in site.divulgacion %}
  {% include archive-single.html %}
{% endfor %}
