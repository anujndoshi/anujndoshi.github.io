---
layout: page
title: Writing
permalink: /writing/
eyebrow: Writing
lede: Essays, notes, and project write-ups. The archive is intentionally small for now.
---

<p class="archive-intro">
  Essays, notes, and project write-ups.
</p>

{% if site.posts.size > 0 %}
  <div class="archive-list">
    {% for post in site.posts %}
      <article class="archive-item">
        <p class="archive-date">{{ post.date | date: "%B %-d, %Y" }}</p>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.description %}
          <p>{{ post.description }}</p>
        {% elsif post.excerpt %}
          <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
        {% endif %}
      </article>
    {% endfor %}
  </div>
{% else %}
  <div class="empty-state">
    <p>The archive is still getting started.</p>
  </div>
{% endif %}
