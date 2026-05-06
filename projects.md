---
layout: page
title: "Projects &amp; case studies"
subtitle: "A working portfolio of things Atlas Werks (and I) have shipped. Anything client-specific is anonymized unless I have permission to name names."
eyebrow: "Work"
permalink: /projects/
---

<div class="grid-2">
  {% for p in site.data.projects %}
  <article class="card project-card reveal">
    <div class="project-meta">
      <span class="client">{{ p.client }}</span>
      <span class="status">{{ p.status }}</span>
    </div>
    <h3>{{ p.title }}</h3>
    <p>{{ p.summary | strip_newlines }}</p>
    <div class="project-tags">
      {% for t in p.tags %}<span class="chip">{{ t }}</span>{% endfor %}
    </div>
    {% if p.outcome %}
    <div class="project-outcome">
      <strong>Outcome</strong>
      {{ p.outcome }}
    </div>
    {% endif %}
    {% if p.link != "" %}<a class="project-link" href="{{ p.link | relative_url }}">Read more →</a>{% endif %}
  </article>
  {% endfor %}
</div>

## Skills &amp; tech

<div class="grid-3" style="margin-top: 1.5rem;">
  {% for g in site.data.skills %}
  <div class="skill-group reveal">
    <h3>{{ g.group }}</h3>
    <div class="chips">
      {% for i in g.items %}<span class="chip">{{ i }}</span>{% endfor %}
    </div>
  </div>
  {% endfor %}
</div>

<div class="cta reveal">
  <h2>Have a project that needs an honest second opinion?</h2>
  <p>I take a small number of independent engagements per quarter. If yours sounds like a fit, let's talk.</p>
  <div class="cta-actions">
    <a class="btn btn-primary btn-lg" href="{{ '/contact/' | relative_url }}">Start a conversation →</a>
  </div>
</div>
