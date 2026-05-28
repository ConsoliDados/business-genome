---
title: "Flow — client-pipeline"
type: skill
kind: flow
status: active
created: 2026-05-26
tags: [skill, flow, commercial]
---

# Flow — client-pipeline (qualify → proposal → contract → kickoff)

> **CLI mode:** run when moving a lead through the commercial funnel.
> **Web-chat mode:** paste the prompt block per stage.

**Reads:** `10-crm/leads/` · **Writes:** `10-crm/`, then `11-projects/clients/<slug>/commercial/`

## Steps
1. [[qualify-lead]] — score against ICP, classify tier (T1–T5), note multipliers.
2. Route: **free 20-min call** or paid **[[discovery]] Pack** (Light/Standard/Deep).
3. [[proposal]] — fixed price + **3 packages** (minimum-viable / recommended / complete);
   Discovery credit applies to invoice 1.
4. [[contract]] — payment schedule, FX clause (A/B/C), NDA level, portfolio rights.
5. On signature → [[kickoff]] creates `11-projects/clients/<slug>/` and the commercial docs move in.

## Guard-rails
- Above the fixed ceiling (R$700k / $300k) → bill monthly (squad), not one-time.
- Modernization (T4) always needs a Discovery Deep before pricing.

---
## Prompt (copy-paste for web chat)
> Here's the lead. Qualify it against our ICP (R$10M+/yr revenue, ~R$500k/yr tech budget,
> CTO present), classify the tier (T1–T5), list applicable multipliers, and recommend the next
> step (free call vs Discovery Light/Standard/Deep). Then draft a 3-package proposal.
