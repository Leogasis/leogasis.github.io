---
lang: es
layout: single
title: "Divulgación"
permalink: /divulgacion/
author_profile: true
---

En esta sección comparto artículos, charlas y recursos dedicados a la **divulgación científica**. Mi objetivo es acercar la ingeniería industrial, la optimización y la inteligencia artificial a un público más amplio, fomentando la curiosidad y el entendimiento de estas disciplinas.

{% for post in site.divulgacion %}
  <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork">
    <h2 class="archive__item-title no_toc" itemprop="headline">
      <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
    </h2>
    {% if post.excerpt %}<p class="archive__item-excerpt" itemprop="description">{{ post.excerpt | markdownify | strip_html | truncate: 160 }}</p>{% endif %}
  </article>
{% endfor %}
