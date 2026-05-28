---
title: "Skill — business-plan (orchestrator)"
type: skill
kind: flow
status: active
created: 2026-05-27
tags: [skill, flow, strategy]
---

# Skill — business-plan (orchestrator)

> A business plan covers too much for one pass. **Write it chapter by chapter**, each with its
> own specialized skill — deeper work, and you only load the context for the chapter you're on.
> Structure = generalized **SEBRAE "Plano de Negócios"**. Output assembles into
> `…/strategy/business-plan.md`, one section per chapter.
>
> **CLI:** run a chapter at a time (pick the chapter skill from the map). **Web-chat:** copy the
> chapter skill's prompt.

## Order & chapter → skill map

| # | Chapter | Skill |
|---|---------|-------|
| 1 | Market analysis & sizing | [[market-study]] *(reuse)* |
| 2 | Personas / ICP | [[persona-study]] *(reuse)* |
| 3 | Feasibility (if not done) | [[feasibility-study]] *(reuse)* |
| 4 | Strategic identity (mission/vision/values + positioning) | [[strategic-identity]] |
| 5 | Marketing plan (value prop, pricing, promo, GTM, sales) | [[marketing-plan]] |
| 6 | Operational plan (capacity, processes, staffing) | [[operational-plan]] |
| 7 | Financial plan (investment, revenue, costs, DRE, viability) | [[financial-plan]] |
| 8 | Funding & valuation (if raising) | [[funding-valuation]] |
| 9 | Scenarios (best/base/worst + sensitivity) | [[scenarios]] |
| 10 | Strategic assessment (SWOT / Porter / BCG) | [[strategic-assessment]] |
| 11 | **Executive summary** — write **last** | [[executive-summary]] |

## Rules
- **Reuse, don't duplicate**: market/persona/feasibility already have skills — link their output.
- One chapter = one focused pass; fill that section of `strategy/business-plan.md`, then stop.
- Executive summary is synthesized **after** the rest exists.
- Mark gaps **ASK-CLIENT / ASK-OWNER**; never invent numbers.
- For a **client-simple** project, a summarized subset lives in `strategy/context.md` instead.
