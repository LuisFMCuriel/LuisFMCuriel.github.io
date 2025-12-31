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
Click a topic to jump:  
<div class="chips" style="margin-top: 10px;">
  <a class="chip" href="#deep-learning">Deep Learning</a>
  <a class="chip" href="#microscopy">Microscopy</a>
  <a class="chip" href="#simulation">Simulation</a>
  <a class="chip" href="#reinforcement-learning">Reinforcement Learning</a>
</div>

---

## Deep Learning <a id="deep-learning"></a>

<div class="cards">
{% assign items = site.data.projects | sort: "year" | reverse %}
{% for p in items %}
  {% if p.tags contains "Deep Learning" %}
  <div class="card">
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
  {% endif %}
{% endfor %}
</div>

---

## Microscopy <a id="microscopy"></a>

<div class="cards">
{% assign items = site.data.projects | sort: "year" | reverse %}
{% for p in items %}
  {% if p.tags contains "Microscopy" %}
  <div class="card">
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
  {% endif %}
{% endfor %}
</div>

---

## Simulation <a id="simulation"></a>

<div class="cards">
{% assign items = site.data.projects | sort: "year" | reverse %}
{% for p in items %}
  {% if p.tags contains "Computational Simulation" %}
  <div class="card">
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
  {% endif %}
{% endfor %}
</div>

---

## Reinforcement Learning <a id="reinforcement-learning"></a>

<div class="cards">
{% assign items = site.data.projects | sort: "year" | reverse %}
{% for p in items %}
  {% if p.tags contains "Reinforcement Learning" %}
  <div class="card">
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
  {% endif %}
{% endfor %}
</div>
