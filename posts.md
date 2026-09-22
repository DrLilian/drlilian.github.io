---
layout: default
title: All Posts
permalink: /posts/
---
<section class="post-list" aria-label="All posts">
  <h1 class="page-title">All Posts</h1>

  {% for post in site.posts %}
    <article class="post-preview">
      <h3 class="post-preview-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p class="post-preview-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
        {% if post.tags and post.tags.size > 0 %}
          · {% for tag in post.tags %}<span class="tag">{{ tag }}</span>{% unless forloop.last %} {% endunless %}{% endfor %}
        {% endif %}
      </p>
      <p class="post-preview-excerpt">{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
    </article>
  {% endfor %}
</section>
