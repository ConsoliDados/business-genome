---
title: "Skill — meeting-summary"
type: skill
status: active
created: 2026-05-26
tags: [skill, ops]
---

# Skill — meeting-summary

> **CLI:** run to structure raw meeting notes. **Web-chat:** paste the prompt.

**Reads:** `02-inbox/` · **Writes:** `…/meetings/<date>-<topic>.md` (project) or `14-meeting-notes/`
(company). Template: `96-templates/tp-meeting.md`.

## Steps
1. Structure: attendees, agenda, notes, **decisions**, **action items** (checkboxes, owners).
2. New decisions → consider an [[adr]]. New questions → `open-questions.md`.
3. Archive the raw inbox original.

---
## Prompt (copy-paste)
> Turn these meeting notes into: attendees, agenda, notes, decisions, and action items with
> owners. Flag any decision that deserves an ADR and any new open question.
