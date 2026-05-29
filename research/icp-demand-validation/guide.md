---
layout: default
title: Founder discovery guide — ICP demand validation
permalink: /research/icp-demand-validation/guide/
study_id: "icp-demand-validation"
guide_version: "1.0"
---

# Discussion guide: ICP demand validation (AI UX Audit wedge)

> **Method note — this is *demand discovery*, not a sales call and not usability research.** Follow the Mom Test: ask about the founder's actual past behavior and current pain, never pitch, and never ask "would you pay for X?". The product is not mentioned until the very end, and only to ask for a commitment, not for approval. Question IDs are stable so real transcripts feed [`research-transcript-analysis`](https://github.com/mpaiva/autonomous-ux-01) cleanly.

## Session info
- **Duration:** 25–30 min
- **Format:** 1:1 interview-only (video or async written equivalent). No tasks.
- **Participant profile:** Founder / CEO / Head of Product at a seed–Series A applied-AI startup (~10–50 people) shipping an agentic, copilot, or vertical-AI product to real users. (See [D-0003 ICP]({{ '/decisions/0003-icp-seed-to-series-a/' | relative_url }}).)
- **Interviewer:** A human member of the founding team. (Agents prepared this guide and will synthesize results; the conversation itself is human-to-human.)

## Research goals
1. Confirm or kill that AI-product UX is a *felt, prioritized* problem for this ICP — in their words, unprompted.
2. Learn what specifically hurts (agent supervision / trust / onboarding) and which blocks revenue.
3. Understand current design spend, who controls that budget, and what has triggered past design purchases — **to validate pricing ([D-0006]({{ '/decisions/0006-pricing-hypothesis/' | relative_url }})) without anchoring.**
4. Test whether a fast, fixed-fee AI UX Audit is a wedge they'd actually commit to — measured by a real commitment, not enthusiasm.

## Hypotheses under test
- **H1 (problem):** AI-product UX — especially agent supervision / trust — is a top-3 felt problem blocking retention or enterprise deals.
- **H2 (trigger):** Spend is triggered by a stalled enterprise pilot, a fundraise, or churn — not by a general desire for "better design."
- **H3 (wedge):** A fixed-fee 1–2 week AI UX Audit is a low-enough-risk first step that a founder will commit to a next action.
- **H4 (pricing):** The audit sits in a $6–12k band the budget-holder can approve without a long process.

## Sections

### 1. Background & framing
**Q1.1** Before we start — I'm researching how AI teams handle product experience; I'm not here to sell you anything, and there are no right answers. Can I record so I don't mis-quote you? *(consent — see checklist)*
**Q1.2** Tell me about your product and who's actually using it today.
- Probes: how long shipped? self-serve or sales-led? who's the user vs. the buyer?
- Listen for: agentic/HITL surface area, enterprise vs. prosumer, real usage vs. pilots.

### 2. Current reality & pain (no pitching)
**Q2.1** Walk me through the last time a user got confused, didn't trust the output, or churned. What happened?
- Probes: what did they do? what did *you* do about it? did it cost a deal/renewal?
- Listen for: spontaneous mention of trust, oversight, hallucination, onboarding. **Unprompted = strong signal (H1).**
**Q2.2** What are the top 2–3 things slowing growth or retention right now?
- Probes: where does product experience rank against model quality, GTM, hiring?
- Listen for: whether UX makes the list *without* you raising it.
**Q2.3** For your agent/automation features specifically — how do users know what it's doing, approve it, or step in?
- Probes: have users asked for more visibility/control? lost a deal over "we can't see what it does"?
- Listen for: the agent-supervision/HITL pattern vacuum ([D-0004]({{ '/decisions/0004-anchor-on-agent-trust-ux/' | relative_url }})).
**Q2.4** Has an enterprise buyer ever pushed back on trust, explainability, audit trails, or human oversight? Tell me about that deal.
- Listen for: the "trust = pilot-killer" trigger (H2).

### 3. Past behavior around design (still no pitch)
**Q3.1** How do you handle product/UX design today — in-house, contractor, agency, founder-does-it?
- Probes: who? since when? what made you set it up that way?
**Q3.2** Think of the last time you paid an outside person or firm for design or product work. What triggered it, what did it cost, and were you happy?
- Probes: what was the trigger event? who approved the spend? what would have made you *not* buy?
- Listen for: real triggers and **real numbers, volunteered** (pricing signal, H4 — do NOT state a price yet).
**Q3.3** If product experience is a problem, why hasn't it been fixed yet?
- Listen for: is it truly unprioritized, or just unowned? (Distinguishes "no demand" from "latent demand.")

### 4. Commitment test (the only place the offer appears)
> Only here, and only as a request for a *commitment* (time, intro, money, or a scheduled next step) — not for approval.

**Q4.1** We're considering a fixed-scope, 1–2 week teardown of an AI product's trust/agent/onboarding UX, ending with a prioritized roadmap. If that existed, what would you want it to answer for *your* product?
- Listen for: do they get specific and lean in, or stay polite/vague? **Vague politeness = soft no.**
**Q4.2** Would you want to see a sample teardown of your product? *(Commitment signals, strongest → weakest: introduces us to a peer who needs it now → asks for a proposal/price → books a follow-up → "send me info.")*
**Q4.3** *(Only if they ask the price.)* It's in the range of $6–12k fixed. — then listen, don't justify.
- Listen for: reaction relative to their Q3.2 numbers. Sticker shock vs. "that's reasonable."

### 5. Closing
**Q5.1** Who else in your shoes should I talk to? *(referral = both sourcing and a demand signal)*
**Q5.2** Anything about this I should have asked and didn't?

## Confirm vs. kill signals
*(Defined up front so we read results honestly — see [plan]({{ '/research/icp-demand-validation/plan/' | relative_url }}).)*

| | Confirm the wedge | Kill / pivot signal |
|---|---|---|
| Problem (H1) | ≥3 of 5 raise trust/agent/onboarding UX **unprompted** in §2 | UX never makes their top-3 without prompting |
| Trigger (H2) | Clear, recent revenue-linked trigger named | "It'd be nice someday" / no trigger |
| Commitment (H3) | ≥2 of 5 give a *hard* commitment (intro, proposal req, booked follow-up) | Only "send me info" / polite interest |
| Pricing (H4) | Volunteered/past spend ≥ audit range; no sticker shock | Numbers an order of magnitude below; audit seen as luxury |

## Ethics and consent checklist
- [ ] Recording and its use explained and agreed
- [ ] Confidentiality stated; their product details kept out of the public operating record ([R-06]({{ '/risks/06-confidentiality/' | relative_url }}))
- [ ] Participant may pause or stop at any time
- [ ] No incentive offered (peer research); next steps confirmed only if *they* want them
