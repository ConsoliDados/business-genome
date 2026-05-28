---
title: "Skill — qualify-lead"
type: skill
status: active
created: 2026-05-26
tags: [skill, commercial, crm]
---

# Skill — qualify-lead

> **CLI:** run to qualify a lead against ICP + classify tier. **Web-chat:** paste the prompt.

**Reads/Writes:** `crm/leads/<slug>.md`

## Steps
1. **ICP fit:** ~R$10M+/yr revenue · ~R$500k/yr tech budget (≈5%) · CTO/Head of Tech present ·
   region BR/INTL. Verdict: fit / stretch / no-fit.
2. **projectType:** ai-agent | ai-chatbot | ai-automation | performance | legacy-modernization |
   custom-software | not-sure.
3. **Tier (T1–T5):** Discovery(T1) · Micro(T1.5) · Pequeno(T2) · Médio(T3) · Grande(T4) ·
   Squad(T5).
4. **Multipliers** (note which apply): urgency, compliance, on-prem, 3+ integrations, bilingual,
   junior-maintained, prior-failure, NDA-total; discounts: referral / upfront / annual / NGO.
5. Recommend next step: free call vs Discovery Light/Standard/Deep.

## Guard-rails
- Output ranges (faixas), **never a hard number** before Discovery. T4 modernization always
  needs a Discovery Deep first.

---
## Prompt (copy-paste)
> Qualify this lead: ICP fit (R$10M+/yr revenue, ~R$500k/yr tech budget, CTO present, BR/INTL),
> projectType, tier T1–T5, applicable multipliers, and recommended next step. Give ranges only,
> no hard price.
