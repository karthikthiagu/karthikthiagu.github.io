---
title: <h1> Articles </h1>
layout: default
mathjax: true
---

{% for category in site.categories %}
  {% unless category contains 'Problems' %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      <br>
      {{ post.excerpt }}
    {% endfor %}
  </ul>
  {% endunless %}
{% endfor %}

<!--<ul class="myposts">
{% for post in site.posts %}
    <li><a href="{{ post.url }}">{{ post.title}}</a>
    </li>
{% endfor %}
</ul>-->
