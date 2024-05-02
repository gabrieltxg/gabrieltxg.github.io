---
layout: page
title: Notes
permalink: /notes
---

{% for post in site.posts %}
  * <strong>{{ post.date | date_to_string }}</strong> &raquo; [ {{ post.title }} ]({{ post.url }})
  {% if post.excerpt %}
    {{ post.excerpt }}
  {% endif %}
{% endfor %}
