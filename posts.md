---
layout: page
title: Posts
permalink: /posts/
---

# Posts

这里记录我的学习笔记、论文阅读、实验记录与技术思考。

{% for post in site.posts %}

## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: "%Y-%m-%d" }}

{% if post.categories %}
Categories: {{ post.categories | join: ", " }}
{% endif %}

{% endfor %}