---
layout: default
title: Updates
permalink: /updates/
---

<div class="page-head">
  <p class="eyebrow">Operating record</p>
  <h1>Progress updates</h1>
  <p class="lede">The weekly narrative: what changed, what we shipped, what we learned, and what's next. Written for the Chairman, kept short.</p>
</div>

<ul class="record-list">
  {% assign ups = site.updates | sort: "date" | reverse %}
  {% for u in ups %}
  <li>
    <h3><a href="{{ u.url | relative_url }}">{{ u.title }}</a></h3>
    <div class="meta">Week {{ u.week }} · {{ u.date }}</div>
  </li>
  {% endfor %}
</ul>
