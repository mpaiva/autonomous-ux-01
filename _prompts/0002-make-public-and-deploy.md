---
id: P-0002
title: Make the operating record public and deploy to GitHub Pages
received: 2026-05-29
from: Chairman
status: addressed
decisions: [D-0009]
artifacts:
  - Live site at https://mpaiva.github.io/autonomous-ux-01/
  - "_config.yml url/baseurl set; R-06 resolved to the public posture"
---

## Interpretation

The Chairman ratified the **public** posture for the operating record and authorized deployment to GitHub Pages — resolving the open escalation in [R-06](/risks/06-confidentiality/). The team confirmed the owning account (**mpaiva**) before publishing, since account choice determines ownership and the live URL.

## Actions taken

- Set `url`/`baseurl` in `_config.yml` to `https://mpaiva.github.io` + `/autonomous-ux-01`.
- Resolved [R-06](/risks/06-confidentiality/) to **accepted (public)** — the build-in-public stance is now the ratified default.
- Created a public repository under the **mpaiva** account and pushed `main`.
- Enabled GitHub Pages (build from `main`, root) — classic safe-mode build, matching our plugin choices in [D-0009](/decisions/0009-operating-record-and-hosting/).

## Status

**Addressed.** The operating record is public. Note this ratified *posture and hosting only* — the working name **"Throughline"** ([D-0010](/decisions/0010-working-name-throughline/)) remains `proposed` and is still the Chairman's to confirm or redirect.
