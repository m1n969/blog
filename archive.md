---
layout: default
title: 日课档案
permalink: /archive/
---

<div class="page-content">

# 日课档案

{% assign posts_by_month = site.posts | group_by_exp: "post", "post.date | date: '%Y年%m月'" %}
{% for month in posts_by_month %}
## {{ month.name }}

<ul class="post-list">
{% for post in month.items %}
<li>
  <a href="{{ post.url | relative_url }}" class="post-title">{{ post.title }}</a>
  <time>{{ post.date | date: "%m/%d" }}</time>
</li>
{% endfor %}
</ul>
{% endfor %}

{% if site.posts.size == 0 %}
还没有日课。写一篇吧。
{% endif %}

</div>
