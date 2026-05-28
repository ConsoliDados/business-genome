---
title: "Flow — delivery"
type: skill
kind: flow
status: active
created: 2026-05-26
tags: [skill, flow, delivery]
---

# Flow — delivery (roadmap → board → backlog)

> **CLI mode:** run after a project is kicked off and the brief is closed.
> **Web-chat mode:** paste the prompt block.

**Writes:** `11-projects/<area>/<slug>/delivery/`

## Steps
1. [[roadmap]] — seed `delivery/roadmap.md` with committed work as Now / Next / Later.
2. [[board-cards]] — break the "Now" into cards on `delivery/board.md` (Kanban).
3. [[backlog]] — capture the rest as numbered BL-NNN items with priority (product/complete).

This is the **macro** delivery view. Technical sprint/feature working docs stay in the code repo.

## Guard-rails
- Don't duplicate the repo's sprint docs here. Keep this tech-lead-and-up.

---
## Prompt (copy-paste for web chat)
> From this brief/scope, draft a roadmap (Now / Next / Later) of committed work, then break the
> "Now" into concrete board cards, and list the remaining items as a numbered backlog with
> priorities (P0/P1/P2) and rough estimates.
