---
layout: default
title: "Senchabot Blog - Haberler ve Güncellemeler"
lang: tr
---

# Senchabot Blog

Senchabot'taki en son güncellemeleri, sürüm notlarını ve platform duyurularını buradan takip edebilirsiniz. Bot kurulumu ve komutlar hakkında bilgi arıyorsanız [Kullanım Rehberi](/guides/) sayfamıza göz atın.

---

## Son Gelişmeler

<div class="post-list">
  {% for post in site.posts %}
    <article class="post" style="margin-bottom: 2rem;">
      <h3 style="margin-bottom: 0.2rem;">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <small style="color: #666;">
        {{ post.date | date: "%d.%m.%Y" }}
      </small>
      <p style="margin-top: 0.5rem;">
        {{ post.excerpt | strip_html | truncatewords: 35 }}
      </p>
      <a href="{{ post.url | relative_url }}">Devamını Oku &rarr;</a>
    </article>
  {% endfor %}
</div>

<!-- Pagination / Sayfalama -->
{% if paginator.total_pages > 1 %}
<div class="pagination" style="margin-top: 3rem; display: flex; justify-content: space-between;">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; Yeni Yazılar</a>
  {% else %}
    <span style="color: #ccc;">&laquo; Yeni Yazılar</span>
  {% endif %}

  <span>Sayfa {{ paginator.page }} / {{ paginator.total_pages }}</span>

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Eski Yazılar &raquo;</a>
  {% else %}
    <span style="color: #ccc;">Eski Yazılar &raquo;</span>
  {% endif %}
</div>
{% endif %}
