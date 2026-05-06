---
layout: page
title: "Services"
subtitle: "What Atlas Werks shows up for. Clear scope, fixed engagements, real ownership."
eyebrow: "Services"
permalink: /services/
---

<div class="grid-2">
  {% for s in site.data.services %}
  <article class="card reveal">
    <span class="card-icon" aria-hidden="true">
      {% case s.icon %}
        {% when "cloud" %}<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 10h-1.26A8 8 0 1 0 9 20h9a5 5 0 0 0 0-10z"/></svg>
        {% when "arrow-right" %}<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
        {% when "terminal" %}<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="4 17 10 11 4 5"/><line x1="12" y1="19" x2="20" y2="19"/></svg>
        {% when "shield" %}<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
        {% when "tag" %}<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20.59 13.41l-7.17 7.17a2 2 0 0 1-2.83 0L2 12V2h10l8.59 8.59a2 2 0 0 1 0 2.82z"/><line x1="7" y1="7" x2="7.01" y2="7"/></svg>
        {% when "compass" %}<svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><polygon points="16.24 7.76 14.12 14.12 7.76 16.24 9.88 9.88 16.24 7.76"/></svg>
      {% endcase %}
    </span>
    <h3>{{ s.title }}</h3>
    <p>{{ s.summary | strip_newlines }}</p>
    <ul class="card-bullets">
      {% for b in s.bullets %}<li>{{ b }}</li>{% endfor %}
    </ul>
  </article>
  {% endfor %}
</div>

<div class="cta reveal">
  <h2>Need help scoping the right engagement?</h2>
  <p>Tell me a little about the situation and I'll come back with a recommended scope, fee, and timeline — usually within a couple of business days.</p>
  <div class="cta-actions">
    <a class="btn btn-primary btn-lg" href="{{ '/contact/' | relative_url }}">Get in touch →</a>
  </div>
</div>
