---
layout: default
title: Projects
---

{% for p in site.data.projects %}
  <div class="card">
    <h3><a href="{{ p.link }}">{{ p.title }}</a></h3>
    <p>{{ p.description }}</p>
    <small>{{ p.year }} · {{ p.tags | join: " • " }}</small>
  </div>
{% endfor %}
