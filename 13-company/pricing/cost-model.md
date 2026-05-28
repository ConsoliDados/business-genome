---
title: "Cost model (markup-divisor)"
type: strategy
status: draft
created: 2026-05-26
updated: 2026-05-26
tags: [pricing, finance]
---

# Cost model — markup-divisor

> **Stub** — unit is the **dev-month**. Plug in real rates.

```
divisor        = 1 / (1 − (tax% + overhead% + margin%))
charged/month  = dev_cost_per_month × divisor
```

## Inputs
- Tax %: 
- Fixed monthly overhead / reference payroll → overhead %: 
- Target margin %: 

## Reconciliation (shown honestly per deal)
- cost · tax · overhead · negotiated discount · net profit · **effective margin**

## Related
- Bands & multipliers: [[tier-ladder]] · Per-project numbers: each project's `finance.md`
