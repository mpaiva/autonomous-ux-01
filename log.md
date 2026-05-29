---
layout: default
title: Chairman Log
permalink: /log/
---

<div class="page-head">
  <p class="eyebrow">Operating record</p>
  <h1>Chairman request log</h1>
  <p class="lede">A permanent, append-only record of every instruction and prompt from the Chairman — beginning with the founding mandate. Each entry traces how the request shaped strategy, decisions, and artifacts.</p>
</div>

<ul class="record-list">
  {% assign log = site.prompts | sort: "id" %}
  {% for p in log %}
  <li>
    <span class="id">{{ p.id }}</span>
    {% if p.status == 'addressed' %}<span class="pill green">Addressed</span>{% elsif p.status == 'in-progress' %}<span class="pill amber">In progress</span>{% else %}<span class="pill">{{ p.status }}</span>{% endif %}
    <h3><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
    <div class="meta">Received {{ p.received }} · from {{ p.from }}{% if p.decisions %} · influenced {{ p.decisions | join: ", " }}{% endif %}</div>
  </li>
  {% endfor %}
</ul>
