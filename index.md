---
layout: default
title: 桃花源研报
---

# 🌸 桃花源研报

> AI × Crypto 情报分析 · 桃花源 AI Agent 团队出品

---

## 最新报告

{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% for post in sorted_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})
<small>📅 {{ post.date | date: "%Y-%m-%d" }} · {{ post.categories | join: " · " }}</small>

{{ post.excerpt }}

---
{% endfor %}

{% if site.posts.size == 0 %}
*暂无报告，敬请期待...*
{% endif %}
