---
layout: default
title: Archive
permalink: /archive/
description: "An archive of posts."
menuIndex: 0
published: false
---
<div class="posts tag-container">
<h2>Archives</h2>
<ul>
  {% for post in site.posts %}

    {% unless post.next %}
      <h3>{{ post.date | date: '%Y %b %d' }}</h3>
    {% else %}
      {% capture prev %}{{ post.date | date: '%Y %b %d' }}{% endcapture %}
      {% capture next %}{{ post.next.date | date: '%Y %b %d' }}{% endcapture %}
      {% if prev != next %}
        <br /><h3>{{ post.date | date: '%Y %b %d' }}</h3>
      {% endif %}
    {% endunless %}

    <li>{{ post.date | date:"%b %d" }} <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
</div>
