---
title: "Skill — financial-plan"
type: skill
status: active
created: 2026-05-27
tags: [skill, strategy, business-plan, finance]
---

# Skill — financial-plan

> Chapter of [[README|business-plan]]. The deepest area — give it its own pass. **CLI:** run for
> the financial chapter. **Web-chat:** paste.

**Writes:** the *Financial plan* section of `…/strategy/business-plan.md` (+ project [[finance]])

## Steps
1. **Investments** — fixed/CapEx + pre-operating, **phased** (Stage | Period | Amount) → total.
2. **Working capital** (rule of thumb if used, e.g. % of monthly gross).
3. **Revenue forecast** — ramp → steady-state; per line; state assumptions.
4. **Cost structure** — COGS/inputs, commercialization/commissions, labor, depreciation, fixed
   monthly. (Dev-month basis + markup-divisor → [[cost-model]].)
5. **Income statement (DRE / P&L)** — revenue → −COGS → gross → −OpEx → EBITDA → net.
6. **Viability indicators** — break-even (qty & value) · profitability (net margin) ·
   ROI / rentability · payback period · (NPV / IRR if multi-year).

## Guard-rails
- Every number carries its assumption. Don't fabricate — mark unknowns ASK-*. Reconcile margin
  honestly (cost · tax · overhead · discount · net · effective margin).

---
## Prompt (copy-paste)
> Build the financial plan for <product>: phased investments + total, working capital, revenue
> forecast (ramp→steady, with assumptions), full cost structure, an income statement (DRE), and
> viability indicators (break-even, profitability, ROI, payback). State every assumption.
