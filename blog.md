---
layout: page
title: Blog
permalink: blog/
---
<div class="posts">
  {% for post in site.posts %}
    {% unless post.categories contains "portfolio" %}
      <div class="post">
        <h1 class="post-title">
          <a href="{{ post.url }}">{{ post.title }}</a>
        </h1>
        <span class="post-date">{{ post.date | date_to_string }}</span>
        {{ post.content }}
      </div>
    {% endunless %}
  {% endfor %}
</div>
