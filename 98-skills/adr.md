---
title: "Skill — adr"
type: skill
status: active
created: 2026-05-26
tags: [skill, decision]
---

# Skill — adr

> **CLI:** run to record a **business** decision. **Web-chat:** paste the prompt.

**Writes:** `…/adrs/NNNN-slug.md` (+ row in `adrs/README.md`). Template: `96-templates/tp-adr.md`.

## Steps
1. Context → Decision ("We will …") → Alternatives considered → Consequences.
2. `decision-status: proposed|accepted|superseded`. Add a row to the ADR index.

## Guard-rails
- **Business/commercial/strategic** decisions only. Technical ADRs live in the code repo.

---
## Prompt (copy-paste)
> Write an ADR for this business decision: context, the decision, alternatives considered, and
> consequences. Keep it to a business/strategic call (not a code architecture decision).
