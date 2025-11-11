---
layout: page
title: Services
permalink: /services/
---

<div class="grid">
  {% assign sorted_services = site.services | sort: "order" %}
  {% for service in sorted_services %}
  <article class="card">
    {% if service.image %}<img src="{{ service.image | relative_url }}" alt="{{ service.title }}" loading="lazy">{% endif %}
    <h2>{{ service.title }}</h2>
    <p class="tagline">{{ service.tagline }}</p>
    <p class="price">{{ service.price }}</p>
    <a href="{{ service.url | relative_url }}" class="btn">View Project</a>
  </article>
  {% endfor %}
</div>
