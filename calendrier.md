---
layout: default
title: Calendrier des concerts
---

<h1>Concerts à venir</h1>
<ul class="posts noList">
  {% assign next_concerts = site.concerts | reverse  %}
  {% for post in next_concerts %}
    {% if post.date >= site.time %}
    <li>
    	<span class="date">{{ post.date | date: "%d/%m/%Y" }}</span><br>
    	<a href="{{ post.url }}">{{ post.title }}</a>
    	<p class="description">{{ post.address }}</p>
    </li>
    {% endif %}
  {% endfor %}
</ul>

<h1>Concerts passés</h1>
<ul class="posts noList">
  {% for post in site.concerts %}
    {% if post.date < site.time %}
    <li>
    	<span class="date">{{ post.date | date: "%d/%m/%Y" }}</span><br>
    	<a href="{{ post.url }}">{{ post.title }}</a>
    	<p class="description">{{ post.address }}</p>
    </li>
    {% endif %}
  {% endfor %}
</ul>