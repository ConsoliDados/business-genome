---
title: "Skill — briefing"
type: skill
status: active
created: 2026-05-26
tags: [skill, project]
---

# Skill — briefing

> **CLI:** run to turn raw notes into a structured brief. **Web-chat:** paste the prompt.

**Reads:** `_inbox/` · **Writes:** `…/00-brief.md` + `…/open-questions.md`

## Steps
1. Extract: one-liner, problem, proposed solution, scope (in/out), stakeholders, success
   criteria, known risks.
2. Every gap → an item in `open-questions.md` marked **ASK-CLIENT** / **ASK-PO**.
3. Set frontmatter (`type: brief`, `status`, dates).

## Guard-rails
- Don't invent requirements. Surface unstated risks the client/PO didn't mention.

---
## Prompt (copy-paste)
> Structure these notes into a brief: one-liner, problem, proposed solution, scope in/out,
> stakeholders, success criteria, risks. List open questions and mark anything not stated as
> ASK-CLIENT/ASK-PO. Don't invent requirements.
