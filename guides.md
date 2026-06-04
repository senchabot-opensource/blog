---
layout: default
title: "Kullanım Rehberi"
permalink: /guides/
lang: tr
---

# Senchabot Kullanım Rehberi

<ul>
  {% for guide in site.guides %}
    {% if guide.lang == 'tr' %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
