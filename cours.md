---
layout: default
title: Cours informatiques
---

# Cours informatiques

Organisés par sujet et niveau :

{% assign cours_grouped = site.cours | group_by: 'sujet' %}
{% for group in cours_grouped %}
## {{ group.name }}

{% assign sorted_items = group.items | sort: 'niveau' %}
{% for cours in sorted_items %}
- [{{ cours.title }} ({{ cours.niveau }})]({{ cours.url }})
{% endfor %}
{% endfor %}