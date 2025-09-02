---
layout: default
title: Home
has_gradient: true
---

<section class="hero-center">
  <h1 class="hero-name">Ayano Yokoyama</h1>
  <p class="hero-tagline">
    Content Design & Localization - Designing clear and human-centered content with AI and localization
  </p>

  <a href="#work" class="scroll-indicator">
    <span>Scroll for projects</span>
    <svg viewBox="0 0 24 24" class="chev" aria-hidden="true"><path d="M6 9l6 6 6-6" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
  </a>
</section>

<a id="work"></a>
<div class="projects-stack">
  {% for p in site.data.projects %}
  <div class="item">
    <a class="title" href="{{ p.url | relative_url }}">{{ p.title }}</a>
    <p class="desc">{{ p.blurb }}</p>
    <p class="meta">{{ p.kicker }}{% if p.tags %} · {{ p.tags | join: ", " }}{% endif %}</p>
    <img class="thumb" src="{{ p.cover | relative_url }}" alt="">
  </div>
  {% endfor %}
</div>

<h2>Selected work</h2>

<div class="card-grid">
{% for p in site.data.projects %}
  <a class="card" href="{{ p.url | relative_url }}">
    <img src="{{ p.cover | relative_url }}" alt="">
    <div class="meta">
      <div class="kicker">{{ p.kicker }}</div>
      <h3 style="margin:.2rem 0 0">{{ p.title }}</h3>
      <p style="margin:.4rem 0 0; color:#555">{{ p.blurb }}</p>
      <div style="margin-top:8px">
        {% for t in p.tags %}<span class="badge">{{ t }}</span>{% endfor %}
      </div>
    </div>
  </a>
{% endfor %}
</div>
