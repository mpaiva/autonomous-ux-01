---
id: D-0009
title: Make this Jekyll site the operating record and Chairman visibility system; host on vanilla GitHub Pages
date: 2026-05-29
status: decided
owner: Managing Partner
deciders: [Founding team]
tags: [operating-model, reporting, infrastructure]
prompts: [P-0001]
---

## Context

The Chairman wants visibility, traceability, and confidence without managing the team. We had to choose the *form* of the reporting system and a hosting approach that won't fail silently.

## Decision

Build the company's reporting as a **living operating record**, not a periodic report: a Jekyll site whose collections *are* the record.

- **Dashboard** (`index`) = the Chairman scorecard: state, what's next, latest decisions, top risks, latest update — answerable in one screen.
- **Collections:** `decisions`, `research`, `updates`, `risks`, `prompts` (the Chairman log), `team`.
- **Hosting:** classic **GitHub Pages in safe mode** — the `github-pages` gem, whitelisted plugins only (`jekyll-feed`, `jekyll-seo-tag`, `jekyll-sitemap`), **no custom `_plugins/`.**

## Rationale

A living record beats a slide deck: it is always current, fully traceable, and doubles as a build-in-public GTM asset. Choosing vanilla GitHub Pages up front avoids the classic trap where a site builds locally but silently fails to deploy because safe mode ignores custom plugins. Collections + Liquid cover every requirement without plugins.

## Consequences

- **Deployment is a Chairman-authorized handoff.** Publishing this record makes internal strategy public and indexable, and requires the Chairman's GitHub account. We build locally and present "make it live" as a decision for the Chairman — see [R-06](/risks/06-confidentiality/).

## Assumptions & risks

- **Assumption:** public build-in-public benefits outweigh strategy exposure — flagged, not yet ratified by the Chairman.
