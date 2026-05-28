---
title: "Skill — meeting-template"
type: skill
status: active
created: 2026-05-27
tags: [skill, commercial]
---

# Skill — meeting-template

> Create or customize a **meeting model** in the library (e.g. a per-tier presentation script).

**Writes:** `96-templates/meetings/<lang>/<name>.md`

## Steps
1. Start from [[generic]] (or the closest existing model).
2. Fill: goal, agenda, the **questions/sections** that matter for this meeting type, the read-out
   and next step. For commercial meetings, tie to the pipeline stage.
3. If multi-language, create one per `<lang>` subfolder.

## Guard-rails
- Models use `<…>` fill-ins (the agent/user fills per use). Keep frontmatter `type: model`.

---
## Prompt (copy-paste)
> Create a meeting template "<name>" for <purpose/stage>: goal, agenda, the key questions/sections,
> read-out and next step. Keep it generic with <…> placeholders.
