---
title: "Skill — contract"
type: skill
status: active
created: 2026-05-26
tags: [skill, commercial]
---

# Skill — contract

> **CLI:** run to draft contract terms. **Web-chat:** paste the prompt.
> **Pipeline-aware / create-if-missing:** start from a model in `96-templates/contracts/<lang>/`
> (`discovery-contract` / `service-contract` / `nda`). If none exists, create a **generic** one
> first (see [[pipeline]] / [[contracts]]) and flag it as generic + **not legal advice**.

**Writes:** `…/commercial/contract.md` (instance) · models live in `96-templates/contracts/<lang>/`

## Steps
1. Reference the accepted [[proposal]] package.
2. Payment schedule (milestones → [[invoicing]]); Discovery credit applied.
3. **FX clause** for international/long contracts: A USD-anchored via PTAX ±15% collar · B fixed
   BRL with 15% buffer · C annual IPCA/IGP-M readjustment (12+ months).
4. **NDA level:** standard | total (regulated) — premium +25–40%.
5. **Portfolio rights:** name use after 12 months, anonymized screenshots, blog rights,
   LinkedIn mention day 1.

## Guard-rails
- Long T3+ BRL contracts must carry an FX/readjustment clause.

---
## Prompt (copy-paste)
> Draft contract terms from the accepted proposal: payment milestones, FX clause (pick A/B/C),
> NDA level, and portfolio rights. Flag anything that needs legal review.
