---
layout: default
title: Projects
---

<link rel="stylesheet" href="/assets/css/style.css">

<ul class="nav">
  <li><a href="/">Home</a></li>
  <li><a href="/projects">Projects</a></li>
  <li><a href="/cv">CV</a></li>
</ul>

# Projects

A curated list of papers and technical projects.

<div class="cards">
{% assign items = site.data.projects | sort: "year" | reverse %}
{% for p in items %}
  <div class="card">
    {% if p.image %}
    <div class="card-img">
      <img src="{{ p.image | relative_url }}" alt="{{ p.title | escape }}">
    </div>
    {% endif %}

    <h3><a href="{{ p.link }}" target="_blank" rel="noopener">{{ p.title }}</a></h3>
    <p>{{ p.description }}</p>

    <div class="meta">
      <span>{{ p.year }}</span>
      <div class="chips">
        {% for t in p.tags %}
          <span class="chip">{{ t }}</span>
        {% endfor %}
      </div>
    </div>
  </div>
{% endfor %}
</div>
