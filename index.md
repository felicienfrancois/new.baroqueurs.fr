---
title: Accueil
layout: default

---
![L'ensemble](/uploads/DSC07985_ensemble.jpg "L'emsemble")

## Programme musical 2020

* Back
* Vivaldi
* Circus

## Prochains concerts :

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

_Retrouvez les enregistrements audios et vidéos des Baroqueurs en concert dans la rubrique_ [_Ecoute d'Extraits_](extraits)

_Retrouvez les dates et le programme des prochains concerts dans la rubrique_ [_Calendrier des Concerts_](calendrier)

_Retrouvez aussi_ [_les Baroqueurs sur Facebook_](https://www.facebook.com/{{ site.social.facebook }})