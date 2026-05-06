---
layout: default
title: 月省
permalink: /monthly/
---

<div class="page-content">

# 月省

{% if site.monthly.size > 0 %}
<ul class="post-list">
{% for m in site.monthly reversed %}
<li>
  <a href="{{ m.url | relative_url }}" class="post-title">{{ m.title }}</a>
</li>
{% endfor %}
</ul>
{% else %}
还没有月省记录。
{% endif %}

</div>
