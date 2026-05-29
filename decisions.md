---
layout: default
title: Decisions
permalink: /decisions/
---

<div class="page-head">
  <p class="eyebrow">Operating record</p>
  <h1>Decisions</h1>
  <p class="lede">Every meaningful call the founding team has made, with rationale and flagged assumptions. This is the company's reasoning, traceable end to end.</p>
</div>

<ul class="record-list">
  {% assign decs = site.decisions | sort: "id" | reverse %}
  {% for d in decs %}
  <li>
    <span class="id">{{ d.id }}</span>
    {% if d.status == 'decided' %}<span class="pill green">Decided</span>
    {% elsif d.status == 'proposed' %}<span class="pill amber">Proposed</span>
    {% elsif d.status == 'reversed' %}<span class="pill red">Reversed</span>
    {% else %}<span class="pill">{{ d.status }}</span>{% endif %}
    <h3><a href="{{ d.url | relative_url }}">{{ d.title }}</a></h3>
    <div class="meta">{{ d.date }} · owner: {{ d.owner }}{% if d.tags %} · {{ d.tags | join: ", " }}{% endif %}</div>
  </li>
  {% endfor %}
</ul>
