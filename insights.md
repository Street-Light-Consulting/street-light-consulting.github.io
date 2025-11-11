---
layout: page
title: Insights
permalink: /insights/
---

<div class="grid">
  {% for post in site.posts %}
  <article class="card">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      {% if post.image %}<img class="service-hero" src="{{ post.image | relative_url }}" alt="{{ post.title }}" loading="lazy">{% endif %}
    <p class="meta">{{ post.date | date: "%b %d, %Y" }}</p>
    <p>{{ post.excerpt | markdownify }}</p>
    <a href="{{ post.url | relative_url }}" class="btn">Read More</a>
  </article>
  {% endfor %}
</div>
