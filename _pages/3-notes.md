---
layout: page
title: Notes
permalink: /notes
---

{% for post in site.posts %}
{% if post.layout == "post" %}
  * <strong>{{ post.date | date_to_string }}</strong> &raquo; [ {{ post.title }} ]({{ post.url }})
  {% if post.excerpt %}
    <small>{{ post.excerpt }}</small>
  {% endif %}
{% endif %}
{% endfor %}

<!--
{% for post in site.posts %}
  * <strong>{{ post.date | date_to_string }}</strong> &raquo; [ {{ post.title }} ]({{ post.url }})
  {% if post.excerpt %}
    <small>{{ post.excerpt }}</small>
  {% endif %}
{% endfor %}

<div class="posts">
  {% for post in paginator.posts %}
  <div class="post">
    <h1 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <span class="post-date">{{ post.date | date_to_string }}</span>

    {{ post.description }}
  </div>
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ site.baseurl }}page{{paginator.next_page}}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    {% if paginator.page == 2 %}
      <a class="pagination-item newer" href="/notes/">Newer</a>
    {% else %}
      <a class="pagination-item newer" href="{{ site.baseurl }}page{{paginator.previous_page}}">Newer</a>
    {% endif %}
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
 </div>
-->

