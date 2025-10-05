---
layout: posts
title: List of blog posts
permalink: /blog/posts/
---
Blog posts are grouped according to year and sorted chronologically (starting from most recent).
### 2025

{%- assign date_format = site.minima.date_format | default: '%-d %B' -%}
{%- assign sorted_posts = site.posts | sort: 'date' -%}

{% for post in sorted_posts reversed %}
	{% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
	{% if year == '2025' %}
{{ post.date | date: date_format }}&#58; [{{ post.title }}](..{{ post.url }})
	{% endif %}
{% endfor %}
