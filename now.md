---
layout: page
title: "Now"
subtitle: "What I'm focused on right now. Inspired by Derek Sivers' /now movement."
eyebrow: "Current focus"
permalink: /now/
---

<p class="muted small">Last updated <time datetime="{{ site.data.now.updated }}">{{ site.data.now.updated | date: "%B %-d, %Y" }}</time> from {{ site.data.now.location }}.</p>

<div class="now-block">
  <h3>Working on</h3>
  <ul>
    {% for f in site.data.now.focus %}<li>{{ f }}</li>{% endfor %}
  </ul>
</div>

<div class="now-block">
  <h3>Reading</h3>
  <ul>
    {% for r in site.data.now.reading %}<li>{{ r }}</li>{% endfor %}
  </ul>
</div>

<div class="now-block">
  <h3>Listening</h3>
  <ul>
    {% for l in site.data.now.listening %}<li>{{ l }}</li>{% endfor %}
  </ul>
</div>

<p class="muted small">{{ site.data.now.notes }}</p>
