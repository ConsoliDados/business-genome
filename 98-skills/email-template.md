---
title: "Skill — email-template"
type: skill
status: active
created: 2026-05-27
tags: [skill, commercial]
---

# Skill — email-template

> Create or customize an **email / questionnaire model** in the library.

**Writes:** `96-templates/emails/<lang>/<name>.md`

## Steps
1. Define purpose + the pipeline stage it serves.
2. Write subject + body with `<…>` fill-ins; for questionnaires, group questions and say why each
   matters (improves answers).
3. Multi-language → one file per `<lang>` subfolder.

## Guard-rails
- Keep it short and human. `type: model` frontmatter.

---
## Prompt (copy-paste)
> Write an email/questionnaire template "<name>" for <stage/purpose>: subject + a short body with
> <…> placeholders (group questions and note why each matters).
