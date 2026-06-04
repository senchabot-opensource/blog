---
layout: default
title: "Senchabot Blog - News and Updates"
lang: en
---

# Senchabot Blog

Keep track of the latest updates, release notes, and platform announcements for Senchabot here. If you are looking for information on bot setup and commands, check out our [Guides](/en/guides/) page.

---

## Latest Updates

<div class="post-list">
  {% for post in site.posts %}
    {% if post.lang == 'en' %}
      <article class="post" style="margin-bottom: 2rem;">
        <h3 style="margin-bottom: 0.2rem;">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>
        <small style="color: #666;">
          {{ post.date | date: "%B %d, %Y" }}
        </small>
        <p style="margin-top: 0.5rem;">
          {{ post.excerpt | strip_html | truncatewords: 35 }}
        </p>
        <a href="{{ post.url | relative_url }}">Read More &rarr;</a>
      </article>
    {% endif %}
  {% endfor %}
</div>

<!-- Pagination / Sayfalama -->
{% if paginator.total_pages > 1 %}
<div class="pagination" style="margin-top: 3rem; display: flex; justify-content: space-between;">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; Newer Posts</a>
  {% else %}
    <span style="color: #ccc;">&laquo; Newer Posts</span>
  {% endif %}

  <span>Page {{ paginator.page }} of {{ paginator.total_pages }}</span>

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Older Posts &raquo;</a>
  {% else %}
    <span style="color: #ccc;">Older Posts &raquo;</span>
  {% endif %}
</div>
{% endif %}
