---
layout: single
title: Mis publicaciones sobre la docencia
permanlink: /docencia
toc: true
---

{%- for post in site.categories ["docencia"] %}
* [{{post.title}}]({{post.url}})
{% endfor %}