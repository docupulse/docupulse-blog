---
layout: default
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
            <a href="{{ '/tags/' | relative_url }}{{ tag | slugify }}" class="tag">{{ tag }}</a>
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

## Use Case Categories

<div class="use-case-categories">
  <div class="category-card">
    <h3><a href="/use-cases/">All Use Cases</a></h3>
    <p>Comprehensive library of DocuPulse use cases across industries and document types.</p>
  </div>
  
  <div class="category-card">
    <h3><a href="{{ '/2025/01/30/investment-agreement-cap-table-analysis/' | relative_url }}">Investment Analysis</a></h3>
    <p>Cap table extraction, equity structure analysis, and investment agreement processing.</p>
  </div>
  
  <div class="category-card">
    <h3><a href="{{ '/2025/01/31/service-offer-comparison-price-analysis/' | relative_url }}">Vendor Management</a></h3>
    <p>Service offer comparison, price analysis, and vendor evaluation automation.</p>
  </div>
</div>