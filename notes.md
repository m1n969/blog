---
layout: default
title: 札记
permalink: /notes/
---

<div class="page-content">

# 札记



{% assign notes = site.posts | where: "category", "札记" %}
{% if notes.size > 0 %}
<ul class="post-list">
{% for post in notes %}
<li>
  <a href="{{ post.url | relative_url }}" class="post-title">{{ post.title }}</a>
  <time>{{ post.date | date: "%Y/%m/%d" }}</time>
</li>
{% endfor %}
</ul>
{% else %}
还没有札记。
{% endif %}

</div>
