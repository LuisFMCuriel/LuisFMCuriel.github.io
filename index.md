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
      <span class="chip">Deep learning</span>
      <span class="chip">Data Science</span>
      <span class="chip">Optics &amp; devices</span>
      <span class="chip">Computer vision</span>
    </div>
  </div>
</div>

<div class="section">
  <h2>What I do</h2>
  <p>
    I build and deploy machine learning systems for imaging and autonomous decision-making,
    with a focus on performance, reliability, and real-world constraints.
  </p>

  <div class="cards" style="margin-top: 12px;">
    <div class="card">
      <h3>Applied machine learning</h3>
      <p>
        Design and training of deep learning models for computer vision and imaging,
        replacing heuristic-based systems with data-driven approaches.
        Experienced with PyTorch, TensorFlow, and production ML pipelines.
      </p>
    </div>

    <div class="card">
      <h3>Real-time &amp; edge systems</h3>
      <p>
        Development and deployment of ML systems under real-time constraints,
        including edge-based inference, autonomous decision-making,
        and hardware-integrated pipelines.
      </p>
    </div>

    <div class="card">
      <h3>Simulation &amp; physical modeling</h3>
      <p>
        Physics-based simulation and modeling to support system design and optimization,
        including heat transfer and microfluidic systems (COMSOL),
        tightly integrated with experimental and ML workflows.
      </p>
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

  <p style="margin-top: 12px;">
    See the full list on <a href="/projects">Projects</a>.
  </p>
</div>

<p style="margin-top: 2rem; opacity: .7;">
  © {{ site.time | date: "%Y" }} Luis F. Curiel
</p>
