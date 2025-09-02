---
layout: default
title: Home
---

<section class="hero">
  <div>
    <h1>Hello, I’m <span class="gradient">Ayano</span></h1>
    <p class="lead">UX writing · Content design · Localization · AI-assisted workflows</p>
    <p style="margin-top:18px;">
      <a class="btn" href="/about/">About me</a>
      <a style="margin-left:10px" href="/contact/">Contact</a>
    </p>
  </div>
  <!-- optional hero image; you can remove this <img> -->
  <div></div>
</section>

<a id="work"></a>
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
