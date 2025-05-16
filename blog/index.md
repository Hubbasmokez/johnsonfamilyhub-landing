---
layout: default
title: Blog
---

<main>
  <section>
    <h1>📖 Blog Posts</h1>
    <ul>
      {% for post in site.posts %}
        <li>
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
          <p><small>Published on {{ post.date | date: "%B %d, %Y" }}</small></p>
        </li>
      {% endfor %}
    </ul>
  </section>
</main>
