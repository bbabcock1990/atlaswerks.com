---
layout: page
title: "Certifications"
subtitle: "Industry certifications I currently hold or have earned across cloud, networking, programming, and foundations."
eyebrow: "Credentials"
permalink: /certifications/
---

{% for cat in site.data.certs %}
<section class="cert-section reveal">
  <h3>{{ cat.category }}</h3>
  <div class="cert-grid">
    {% for c in cat.certs %}
    <div class="cert">
      <span class="cert-badge">{% if c.code %}{{ c.code | slice: 0,3 }}{% else %}✓{% endif %}</span>
      <div>
        <div class="cert-name">{{ c.name }}</div>
        <div class="cert-issuer">{{ c.issuer }}{% if c.code %} · {{ c.code }}{% endif %}</div>
      </div>
    </div>
    {% endfor %}
  </div>
</section>
{% endfor %}

<p class="muted small">Certifications are listed for reference. Brandon does not represent Microsoft or any other certification authority.</p>
