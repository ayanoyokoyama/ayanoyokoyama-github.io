---
layout: default
title: Home
has_gradient: true
---

<section class="hero-center">
  <h1 class="hero-name"><span class="grad-poppy">Ayano Yokoyama</span></h1>
  <p class="hero-tagline">
    Content Design & Localization · designing clear, human content with AI
  </p>

  <a href="#work" class="scroll-indicator" aria-label="Scroll to work">
    <span>Scroll for projects</span>
    <svg viewBox="0 0 24 24" class="chev" aria-hidden="true">
      <path d="M6 9l6 6 6-6" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
    </svg>
  </a>
</section>

<!-- anchor target for the top nav and scroll link -->
<a id="work"></a>

<section class="wrap work-section">
  <h2 class="work-heading">Selected work</h2>

  <div class="work-grid">
  {% for p in site.data.projects %}
    <a class="work-card" href="{{ p.url | relative_url }}">
      {% if p.cover %}
        <img class="work-cover" src="{{ p.cover | relative_url }}" alt="">
      {% endif %}
      <div class="meta">
        {% if p.kicker %}<div class="title">{{ p.kicker }}</div>{% endif %}
        <h3 class="work-title">{{ p.title }}</h3>
        {% if p.blurb %}<p class="meta">{{ p.blurb }}</p>{% endif %}

        {% if p.tags %}
        <div style="margin-top:8px">
          {% for t in p.tags %}<span class="badge">{{ t }}</span>{% endfor %}
        </div>
        {% endif %}
      </div>
    </a>
  {% endfor %}
  </div>
</section>
