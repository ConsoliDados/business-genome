---
title: "Skill — pipeline"
type: skill
status: active
created: 2026-05-27
tags: [skill, commercial]
---

# Skill — pipeline

> Define a new pipeline or extend one. **Create-if-missing:** if the user asks for a commercial
> action and the pipeline/model doesn't exist yet, create a **generic** one and say so, so they
> adjust on top. You can have **several** pipelines.

**Writes:** `97-config/pipelines/<name>.md` (+ models in `96-templates/`)

## Steps
1. Name the pipeline; define ordered **stages**. Per stage: purpose · **meeting** model ·
   **email/questionnaire** model · **documents** to produce (optionally per tier) · **gate** to advance.
2. Point each stage at models in `96-templates/{meetings,emails,proposals,contracts}/<lang>/` —
   reuse if present, else create generic ones ([[meeting-template]], [[email-template]]).
3. Register the pipeline in `97-config/genome.md` (`pipelines:`).

## Guard-rails
- Generic first; flag what's generic so the user tailors it. Don't duplicate the shipped
  [[sales]]/[[contracts]] — extend them unless it's a genuinely new flow.

---
## Prompt (copy-paste)
> Define a "<name>" pipeline: list the stages, and for each the meeting/email/questionnaire
> models, the documents to produce (note any that vary by tier), and the gate to advance. Reuse
> existing models or create generic ones, and register it in the genome config.
