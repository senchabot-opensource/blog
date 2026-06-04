---
layout: default
title: "Senchabot Blog"
lang: tr
---
# Senchabot Güncellemeleri

<ul>
  {% for post in site.posts %}
    {% if post.lang == 'tr' %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
