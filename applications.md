---
layout: default
title: Applications évaluées
---

# Applications évaluées

Critiques et tutoriels :

{% for app in site.applications %}
- [{{ app.title }}]({{ app.url }})
{% endfor %}