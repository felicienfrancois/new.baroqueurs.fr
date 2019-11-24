---
title: Accueil
layout: default
---

![L'ensemble](assets/img/DSC07985_ensemble.jpg "L'emsemble")

## Programme musical 2020

- Back
- Vivaldi
- Circus

## Prochains concerts :

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

_Retrouvez les enregistrements audios et vidéos des Baroqueurs en concert dans la rubrique [Ecoute d'Extraits](extraits)_

_Retrouvez les dates et le programme des prochains concerts dans la rubrique [Calendrier des Concerts](calendrier)_

_Retrouvez aussi [les Baroqueurs sur Facebook](https://www.facebook.com/{{ site.social.facebook }})_