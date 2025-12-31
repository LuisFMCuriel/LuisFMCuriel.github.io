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
  <img class="avatar" src="/assets/img/profile.jpg" alt="Profile photo">
  <div>
    <h1>Luis F. Curiel</h1>
    <p>
      Deep learning for microscopy · Computational imaging · Physics-based simulation
    </p>

    <div class="buttons">
      <a class="btn" href="/projects">View projects</a>
      <a class="btn" href="/cv">View CV</a>
    </div>

    <div class="chips" style="margin-top: 12px;">
      <span class="chip">Microscopy denoising</span>
      <span class="chip">Volumetric imaging</span>
      <span class="chip">Optics &amp; devices</span>
      <span class="chip">RL in PyTorch</span>
    </div>
  </div>
</div>

<div class="section">
  <h2>Focus</h2>
  <p>
    I develop deep learning methods for microscopy and computational imaging, and work on simulation-driven projects in physics/chemistry.
    This site highlights selected research papers and technical projects.
  </p>

  <div class="cards" style="margin-top: 12px;">
    <div class="card">
      <h3>Research</h3>
      <p>Deep learning for microscopy (denoising, reconstruction) and volumetric imaging.</p>
    </div>
    <div class="card">
      <h3>Simulation</h3>
      <p>Computational simulation of photochemical/solar-cell dynamics under incoherent light.</p>
    </div>
    <div class="card">
      <h3>Engineering</h3>
      <p>Optics / neurophotonics development and practical ML implementations.</p>
    </div>
  </div>
</div>

<div class="section">
  <h2>Featured projects</h2>

  <div class="cards">
  {% assign featured = site.data.projects | where: "featured", true %}
  {% for p in featured limit: 4 %}
    <div class="card">
      {% if p.image %}
      <div class="card-img">
        <img src="{{ p.image }}" alt="{{ p.title }}">
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

  <p style="margin-top: 12px;">
    See the full list on <a href="/projects">Projects</a>.
  </p>
</div>

<p style="margin-top: 2rem; opacity: .7;">
  © {{ site.time | date: "%Y" }} Luis F. Curiel
</p>
