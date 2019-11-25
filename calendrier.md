---
title: Calendrier des concerts
layout: default
menu:
  header:
    title: Calendrier des Concerts
    weight: 3

---
<h1>Concerts à venir</h1>
<ul class="posts noList">
  {% assign next_concerts = site.concerts | reverse  %}
  {% for post in next_concerts %}
    {% if post.date >= site.time %}
    <li>
    	<span class="date">{{ post.date | date: "%d/%m/%Y" }}</span><br>
    	<a href="{{ post.url }}">{{ post.title }}</a>
    	<p class="description">{{ post.adresse }}</p>
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
    	<p class="description">{{ post.adresse }}</p>
    </li>
    {% endif %}
  {% endfor %}
</ul>