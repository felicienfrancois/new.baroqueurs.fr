---
layout: default
title: L'ensemble
---

# L'ensemble


<ul class="posts noList">
  {% for post in site.musiciens %}
    <li>
    	<div class="floating-image"><img src="{{ post.image }}"></div>
    	<div class="description">{{ post.content }}</div>
    </li>
  {% endfor %}
</ul>