---
title: "Skill — proposal"
type: skill
status: active
created: 2026-05-26
tags: [skill, commercial]
---

# Skill — proposal

> **CLI:** run to draft a 3-package proposal. **Web-chat:** paste the prompt.
> **Pipeline-aware / create-if-missing:** start from the model `96-templates/proposals/<lang>/project-proposal.md`.
> If no model (or no [[sales]] pipeline) exists yet, create a **generic** one first via [[pipeline]]
> and tell the user it's generic to adjust.

**Writes:** `…/commercial/proposal.md` (instance) · model lives in `96-templates/proposals/<lang>/`

## Steps
1. Always **3 packages**: A minimum-viable · B recommended · C complete.
2. Each: scope, price ({{currency}}), timeline, assumptions, what's out of scope.
3. **Fixed vs monthly:** above the ceiling (R$700k / $300k) bill monthly (squad), not one-time.
4. Note the Discovery credit applied to invoice 1.

## Guard-rails
- Be explicit about assumptions and out-of-scope — that's where scope creep starts.

---
## Prompt (copy-paste)
> Draft a proposal with 3 packages (minimum-viable / recommended / complete): scope, price
> range, timeline, assumptions, out-of-scope for each. If the value exceeds the fixed ceiling,
> structure it as a monthly squad instead. Note the Discovery credit on invoice 1.
