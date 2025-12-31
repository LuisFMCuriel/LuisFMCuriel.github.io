---
layout: default
title: Home
---

<link rel="stylesheet" href="/assets/css/style.css">

<ul class="nav">
  <li><a href="/">Home</a></li>
  <li><a href="/projects">Projects</a></li>
  <li><a href="/cv">CV</a></li>
</ul>

<div class="hero">
  <!-- Optional: add a profile photo at assets/img/profile.jpg -->
  <img class="avatar" src="/assets/img/profile.jpg" alt="Profile photo">
  <div>
    <h1>Luis F. Curiel</h1>
    <p>
      Deep learning for microscopy · Computational imaging · Physics-based simulation
    </p>
    <div class="buttons">
      <a class="btn" href="/projects">View projects</a>
      <a class="btn" href="/cv">View CV</a>
      <!-- Optional later: publications page -->
      <!-- <a class="btn" href="/publications">Publications</a> -->
    </div>
  </div>
</div>

<div class="section">
  <h2>About</h2>
  <p>
    My work focuses on deep learning methods for microscopy and computational imaging,
    with applications to biological imaging and physics-based simulation.
    I have contributed to peer-reviewed publications and open technical tutorials.
  </p>
</div>


<div class="section">
  <h2>Featured projects</h2>

  <div class="cards">
  {% assign featured = site.data.projects | where: "featured", true %}
  {% for p in featured limit: 4 %}
    <div class="card">
      <h3><a href="{{ p.link }}" target="_blank" rel="noopener">{{ p.title }}</a></h3>
      <p>{{ p.description }}</p>
      <div class="meta">{{ p.year }} · {{ p.tags | join: " • " }}</div>
    </div>
  {% endfor %}
  </div>

  <p style="margin-top: 12px;">
    See the full list on <a href="/projects">Projects</a>.
  </p>
</div>
