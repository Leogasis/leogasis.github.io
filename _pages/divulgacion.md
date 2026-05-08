---
lang: es
layout: single
title: "Divulgación Científica"
permalink: /divulgacion/
author_profile: true
classes: wide
---

En esta sección comparto artículos, reflexiones y recursos dedicados a la **apropiación social del conocimiento**. Mi objetivo es acercar temas complejos de ingeniería industrial, optimización e inteligencia artificial a un público más amplio, fomentando la curiosidad y el entendimiento de las tecnologías que están moldeando nuestro futuro.

---

<div class="entries-grid">
  {% assign divulgacion = site.divulgacion | sort: 'date' | reverse %}
  {% for post in divulgacion %}
    <div class="grid__item">
      <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork">
        {% if post.header.teaser %}
          <div class="archive__item-teaser">
            <img src="{{ post.header.teaser | relative_url }}" alt="">
          </div>
        {% endif %}
        <h2 class="archive__item-title no_toc" itemprop="headline">
          <a href="{{ post.url | relative_url }}" rel="permalink">{{ post.title }}</a>
        </h2>
        
        <p class="page__meta"><i class="far fa-calendar-alt" aria-hidden="true"></i> {{ post.date | date: "%B %d, %Y" }}</p>

        {% if post.excerpt %}
          <p class="archive__item-excerpt" itemprop="description">{{ post.excerpt | markdownify | strip_html | truncate: 160 }}</p>
        {% endif %}
      </article>
    </div>
  {% endfor %}
</div>
