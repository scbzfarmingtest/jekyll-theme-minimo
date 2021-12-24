---
layout: default
title: 标签
permalink: /tags/
---

# 标签

{% for tag in site.tags %}
  <h2>{{ tag[0] }}</h2>
  <span>共({{ tag[1].size }})篇</span>
  <ul>
    {% for post in tag[1] %}
      <li>{{ post.date | date:"%Y %b.%d"}}&emsp;<a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
  <br/>
{% endfor %}