---
layout: default
title: Risks
permalink: /risks/
---

<div class="page-head">
  <p class="eyebrow">Operating record</p>
  <h1>Risks &amp; open questions</h1>
  <p class="lede">What could derail the company, what we're doing about it, and the questions we don't yet have answers to. Updated as the picture changes.</p>
</div>

<ul class="record-list">
  {% assign risks = site.risks | sort: "id" %}
  {% for r in risks %}
  <li>
    <span class="id">{{ r.id }}</span>
    {% if r.severity == 'high' %}<span class="pill red">High</span>{% elsif r.severity == 'medium' %}<span class="pill amber">Medium</span>{% else %}<span class="pill green">Low</span>{% endif %}
    {% if r.status == 'open' %}<span class="pill">Open</span>{% elsif r.status == 'mitigating' %}<span class="pill amber">Mitigating</span>{% elsif r.status == 'closed' %}<span class="pill green">Closed</span>{% else %}<span class="pill">{{ r.status }}</span>{% endif %}
    <h3><a href="{{ r.url | relative_url }}">{{ r.title }}</a></h3>
    <div class="meta">Likelihood: {{ r.likelihood }} · owner: {{ r.owner }}</div>
  </li>
  {% endfor %}
</ul>
