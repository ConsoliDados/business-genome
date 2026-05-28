---
title: "Flow — business-case"
type: skill
kind: flow
status: active
created: 2026-05-26
tags: [skill, flow, strategy]
---

# Flow — business-case (feasibility → market → persona → business-plan)

> **CLI mode:** run for an internal-product (or a client-complete that needs strategy depth).
> **Web-chat mode:** paste each study's prompt in turn.

**Writes:** `projects/<area>/<slug>/strategy/`

## Steps
1. [[feasibility-study]] → `strategy/feasibility.md` (technical/economic/operational + go-no-go).
2. [[market-study]] → `strategy/market.md` (segment, size, competitors, positioning).
3. [[persona-study]] → `strategy/personas.md` (who, pains, jobs-to-be-done).
4. **[[README|business-plan]]** (orchestrator) → write `strategy/business-plan.md`
   **chapter by chapter** with the specialized skills in `_skills/business-plan/`
   (strategic-identity, marketing-plan, operational-plan, financial-plan, funding-valuation,
   scenarios, strategic-assessment; executive-summary **last**). Reuses steps 1–3.

Cross-link everything; the business plan references market/personas and [[finance]].
Don't write the whole plan in one pass — one chapter, one focused skill.

## Guard-rails
- Structure follows the ConsoliDados Notion source (see those skill files). Cite evidence;
  mark gaps ASK-OWNER / ASK-CLIENT. Don't fabricate market numbers.

---
## Prompt (copy-paste for web chat)
> Build the business case for <product>. Go in order: feasibility (technical/economic/
> operational + go/no-go), market study (segment, size, competitors, positioning), personas,
> then a business plan tying it together with GTM, business model and rough financials. Flag
> every assumption that needs validation.
