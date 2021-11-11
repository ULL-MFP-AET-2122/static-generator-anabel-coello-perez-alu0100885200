---
layout: single
title: Mi blog personal
permanlink: /blog
toc: true
---

{%- for post in site.categories ["blog"] %}
* [{{post.title}}]({{post.url}})
{% endfor %}