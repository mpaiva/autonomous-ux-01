---
layout: default
title: Dashboard
---

<div class="page-head">
  <p class="eyebrow">{{ site.data.company.name }} · Chairman dashboard</p>
  <h1>{{ site.data.company.one_liner }}</h1>
  <p class="lede">{{ site.data.company.thesis_short }}</p>
</div>

<p style="color:var(--muted);font-size:14px;margin-top:6px">
  Phase: <strong>{{ site.data.scorecard.phase }}</strong> · Week {{ site.data.scorecard.week }} ·
  As of {{ site.data.scorecard.as_of }}
  {% if site.data.company.working_name %}· <em>“{{ site.data.company.name }}” is a working name pending Chairman trademark sign-off.</em>{% endif %}
</p>

<!-- ====== Scorecard ====== -->
<section>
  <h2>State of the company</h2>
  <div class="scorecard">
    {% for i in site.data.scorecard.indicators %}
    <div class="metric">
      <div class="label"><span class="dot {{ i.status }}"></span>{{ i.label }}</div>
      <div class="value">{{ i.value }}</div>
      <div class="note">{{ i.note }}</div>
    </div>
    {% endfor %}
  </div>
</section>

<!-- ====== Next ====== -->
<section>
  <div class="panel tint">
    <h2>What's next</h2>
    <ul class="checklist">
      {% for n in site.data.scorecard.next %}<li>{{ n }}</li>{% endfor %}
    </ul>
  </div>
</section>

<!-- ====== Latest decisions ====== -->
<section>
  <h2>Latest decisions <span style="font-weight:400;color:var(--muted);font-size:15px">— <a href="{{ '/decisions/' | relative_url }}">see all</a></span></h2>
  <ul class="record-list">
    {% assign decs = site.decisions | sort: "id" | reverse %}
    {% for d in decs limit: 4 %}
    <li>
      <span class="id">{{ d.id }}</span>
      {% if d.status == 'decided' %}<span class="pill green">Decided</span>{% elsif d.status == 'proposed' %}<span class="pill amber">Proposed</span>{% endif %}
      <h3><a href="{{ d.url | relative_url }}">{{ d.title }}</a></h3>
      <div class="meta">{{ d.date }} · owner: {{ d.owner }}</div>
    </li>
    {% endfor %}
  </ul>
</section>

<!-- ====== Open risks ====== -->
<section>
  <h2>Top risks <span style="font-weight:400;color:var(--muted);font-size:15px">— <a href="{{ '/risks/' | relative_url }}">see all</a></span></h2>
  <ul class="record-list">
    {%- comment -%} sort: "severity" is alphabetical (high→low→medium); correct only while there are no low-severity risks. Add a numeric weight field if a low-severity risk is introduced. {%- endcomment -%}
    {% assign risks = site.risks | sort: "severity" %}
    {% for r in risks %}{% if r.status == 'open' or r.status == 'mitigating' %}
    <li>
      <span class="id">{{ r.id }}</span>
      {% if r.severity == 'high' %}<span class="pill red">High</span>{% elsif r.severity == 'medium' %}<span class="pill amber">Medium</span>{% else %}<span class="pill green">Low</span>{% endif %}
      <h3><a href="{{ r.url | relative_url }}">{{ r.title }}</a></h3>
      <div class="meta">Likelihood: {{ r.likelihood }} · owner: {{ r.owner }}</div>
    </li>
    {% endif %}{% endfor %}
  </ul>
</section>

<!-- ====== Latest update ====== -->
<section>
  <h2>Most recent progress update</h2>
  {% assign ups = site.updates | sort: "date" | reverse %}
  {% for u in ups limit: 1 %}
  <div class="panel">
    <h3 style="margin-top:0"><a href="{{ u.url | relative_url }}">{{ u.title }}</a></h3>
    <div class="meta" style="color:var(--muted);font-size:13px">Week {{ u.week }} · {{ u.date }}</div>
    <p style="color:var(--ink-2)">{{ u.excerpt | strip_html | truncatewords: 50 }}</p>
    <a href="{{ u.url | relative_url }}">Read the full update →</a>
  </div>
  {% endfor %}
</section>

<section>
  <p style="color:var(--muted);font-size:14px">
    Every Chairman request is permanently recorded in the
    <a href="{{ '/log/' | relative_url }}">Chairman Log</a>. The company's reasoning lives in
    <a href="{{ '/decisions/' | relative_url }}">Decisions</a> and the evidence behind it in
    <a href="{{ '/research/' | relative_url }}">Research</a>.
  </p>
</section>
