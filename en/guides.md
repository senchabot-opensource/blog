---
layout: default
title: "Guides & Documentation"
permalink: /en/guides/
lang: en
---

# Senchabot Guides

<ul>
  {% for guide in site.guides %}
    {% if guide.lang == 'en' %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
