---
layout: default
title: 分类
permalink: /categories/
---

# 分类

{% for category in site.categories %}
<h2>{{ category[0] }}</h2>
<span>共({{ category[1].size }})篇</span>
<ul>
    {% for post in category.last %}
        <li>{{ post.date | date:"%Y %b.%d"}}&emsp;<a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
<br/>
{% endfor %}