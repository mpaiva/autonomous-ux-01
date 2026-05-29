# Throughline — Company Operating Record

This repository is the operating record and Chairman visibility system for **Throughline**, an AI-native design company serving AI startups. It is a Jekyll site designed to deploy on **classic GitHub Pages (safe mode)** — no custom plugins, so what builds locally is what deploys.

> "Throughline" is a working name pending Chairman trademark sign-off ([D-0010](_decisions/0010-working-name-throughline.md)).

## What this is

Not a marketing brochure — a **living operating record**. The site's collections *are* the company's source of truth:

| Collection | Folder | What lives here |
|---|---|---|
| Decisions | `_decisions/` | Every meaningful call, with rationale + flagged assumptions |
| Research | `_research/` | Cited market learning, with confidence + evidence gaps |
| Risks | `_risks/` | The live risk register |
| Updates | `_updates/` | Weekly Chairman progress narrative |
| Chairman log | `_prompts/` | Permanent, append-only record of every Chairman request |
| Team | `_team/` | The founding operating model (who owns/decides what) |

The Chairman **dashboard** (`index.md`) reads `_data/scorecard.yml` and the collections to answer, in one screen: *what was decided, why, what's next, what's at risk.*

## Run locally

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

## Deploy (Chairman-authorized)

Deployment publishes internal strategy and needs the Chairman's GitHub account — it is a deliberate handoff, not an automatic step ([R-06](_risks/06-confidentiality.md)). When authorized:

1. Create a repo under the Chairman's GitHub account and push this code.
2. Settings → Pages → Build from the `main` branch (root).
3. Set `url` and `baseurl` in `_config.yml` to the published location.

For a **private** or **hybrid** posture, keep the repo private and publish only curated content.

## How to keep the record honest

The discipline that makes this trustworthy (see [operating model](operating-model.md)):

- **Decision made →** add a file to `_decisions/` (rationale + assumptions).
- **Chairman prompt received →** add a file to `_prompts/` (verbatim + interpretation + influence).
- **Risk emerges/changes →** update `_risks/`.
- **Anything ships →** add/extend the weekly note in `_updates/` and bump `_data/scorecard.yml`.
- **Strategy changes →** supersede the prior decision (don't delete it) and note it in `changelog.md`.

## Conventions

- IDs: decisions `D-00NN`, risks `R-NN`, prompts `P-00NN`.
- Company facts live once in `_data/company.yml`; the scorecard in `_data/scorecard.yml`.
- No `!important` in CSS; no custom Jekyll plugins (safe-mode compatibility).
