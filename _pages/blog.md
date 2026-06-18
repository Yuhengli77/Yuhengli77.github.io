---
permalink: /blog/
title: "Blog"
author_profile: true
---

# Hello

Welcome to my blog! I share some interesing projects and thoughts here.

<div class="entries-list">
{% for post in site.posts %}
  <article class="archive__item">
    <h2 class="archive__item-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <p class="page__meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    {% if post.excerpt %}
      <p class="archive__item-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 180 }}</p>
    {% endif %}
  </article>
{% else %}
  <p>No blog posts yet.</p>
{% endfor %}
</div>
