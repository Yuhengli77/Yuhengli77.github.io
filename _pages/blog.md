---
permalink: /blog/
title: "Blog"
author_profile: true
---

# Hello

Welcome to my blog! I share some interesing projects and thoughts here.

<div class="entries-list">
{% assign pinned_posts = site.posts | where: "pinned", true %}
{% assign regular_posts = site.posts | where_exp: "post", "post.pinned != true" %}

{% for post in pinned_posts %}
  <article class="archive__item">
    <h2 class="archive__item-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <p class="page__meta">Pinned · {{ post.date | date: "%B %-d, %Y" }}</p>
    {% if post.excerpt %}
      <p class="archive__item-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 180 }}</p>
    {% endif %}
  </article>
{% endfor %}

{% for post in regular_posts %}
  <article class="archive__item">
    <h2 class="archive__item-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <p class="page__meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    {% if post.excerpt %}
      <p class="archive__item-excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 180 }}</p>
    {% endif %}
  </article>
{% endfor %}

{% if site.posts.size == 0 %}
  <p>No blog posts yet.</p>
{% endif %}
</div>
