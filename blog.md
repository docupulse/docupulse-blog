---
layout: page
title: Blog
permalink: /blog/
---

# Latest Posts

<div class="post-list">
  {% for post in site.posts %}
    <article class="post-item">
      <div class="post-meta">
        <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
        <div class="post-tags">
          {% for tag in post.tags %}
            <a href="/tags/{{ tag | slugify }}" class="tag">{{ tag }}</a>
          {% endfor %}
        </div>
      </div>
      <h2 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h2>
      <div class="post-excerpt">
        {{ post.excerpt | strip_html | truncatewords: 30 }}
      </div>
      <a href="{{ post.url | relative_url }}" class="btn btn-primary">Read More</a>
    </article>
  {% endfor %}
</div>
