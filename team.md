---
layout: default
title: Team
permalink: /team/
---

<div class="page-head">
  <p class="eyebrow">Operating record</p>
  <h1>Founding team</h1>
  <p class="lede">Throughline self-organized into four founding functions, each defined by a real company need — not borrowed org-chart titles. This is an operating model, not a cast of characters: it says who owns what, who decides what, and when each role becomes a hire.</p>
</div>

<div class="panel tint" style="margin-bottom:24px">
  <h2 style="margin-top:0">How we decide</h2>
  <p style="color:var(--ink-2);margin:0">{{ site.data.company.decision_rule }}</p>
  <p style="color:var(--ink-2);margin:10px 0 0"><strong>Cadence:</strong> {{ site.data.company.cadence }}</p>
</div>

<ul class="record-list">
  {% assign members = site.team | sort: "order" %}
  {% for m in members %}
  <li>
    <h3><a href="{{ m.url | relative_url }}">{{ m.name }}</a></h3>
    <div class="meta">{{ m.role }}{% if m.when %} · {{ m.when }}{% endif %}</div>
    {% if m.owns %}<div class="meta" style="margin-top:6px">Owns: {{ m.owns | join: ", " }}</div>{% endif %}
  </li>
  {% endfor %}
</ul>

<p style="margin-top:24px;color:var(--muted);font-size:14px">See also: <a href="{{ '/operating-model/' | relative_url }}">how the company operates week to week →</a></p>
