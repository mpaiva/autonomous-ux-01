---
layout: default
title: Research
permalink: /research/
---

<div class="page-head">
  <p class="eyebrow">Operating record</p>
  <h1>Research &amp; market learning</h1>
  <p class="lede">The evidence base under our decisions. Sources are cited; confidence and evidence gaps are stated plainly rather than hidden.</p>
</div>

<ul class="record-list">
  {% assign items = site.research | sort: "date" | reverse %}
  {% for r in items %}
  <li>
    <h3><a href="{{ r.url | relative_url }}">{{ r.title }}</a></h3>
    {% if r.summary %}<p style="color:var(--ink-2);margin:6px 0 0">{{ r.summary }}</p>{% endif %}
    <div class="meta">{{ r.date }}{% if r.confidence %} · confidence: {{ r.confidence }}{% endif %}{% if r.decisions %} · informs {{ r.decisions | join: ", " }}{% endif %}</div>
  </li>
  {% endfor %}
</ul>
