---
layout: page
title: "Experience"
subtitle: "From Marines to Microsoft — a working timeline of where I've been."
eyebrow: "Background"
permalink: /experience/
---

<div class="timeline">
  {% for r in site.data.experience %}
  <div class="timeline-item{% if r.current %} current{% endif %} reveal">
    <div class="time-meta">
      <span class="date">{{ r.start }} — {{ r.end }}</span>
      {% if r.current %}<span class="badge-current">Current</span>{% endif %}
    </div>
    <h3 class="role-title">{{ r.role }}</h3>
    <div class="role-org">{{ r.org }}</div>
    <ul>
      {% for b in r.bullets %}<li>{{ b }}</li>{% endfor %}
    </ul>
  </div>
  {% endfor %}
</div>

<div class="cta reveal">
  <h2>Want the formal version?</h2>
  <p>The current resume PDF is from 2021 and is being refreshed. For the most up-to-date version, just ask.</p>
  <div class="cta-actions">
    <a class="btn btn-primary" href="{{ '/contact/' | relative_url }}">Request the latest resume →</a>
    <a class="btn btn-ghost" href="{{ '/assets/files/brandon_babcock_resume.pdf' | relative_url }}" target="_blank" rel="noopener">Download 2021 PDF</a>
  </div>
</div>
