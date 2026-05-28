---
title: "Flow — intake"
type: skill
kind: flow
status: active
created: 2026-05-26
tags: [skill, flow]
---

# Flow — intake (inbox → briefing → kickoff)

> **CLI mode:** run this when the human says *"structure this briefing / start the project"*
> and there's raw material in `02-inbox/`. You pick and chain the atomic skills below.
> **Web-chat mode:** the human pastes the prompt block at the bottom.

**Reads:** `02-inbox/` · **Writes:** `11-projects/<area>/<slug>/` · **Archives:** `95-archive/<slug>/`

## Steps
1. Read the raw material in `02-inbox/`. Identify: client or internal? which project type?
2. **If client:** make sure the lead is qualified ([[qualify-lead]]) and an account exists in
   `10-crm/accounts/`; link it.
3. Run [[briefing]] → fill `00-brief.md`; every gap becomes an **ASK-CLIENT/ASK-PO** item in
   `open-questions.md`. Don't invent requirements.
4. On the human's go, run [[kickoff]]: copy `96-templates/_project-<type>/` into
   `11-projects/<area>/<slug>/`, replace all `{{…}}` tokens (`{{slug}}`, `{{Name}}`, `{{date}}`,
   `{{client-slug}}`, `{{currency}}`, `{{repo}}`), set the
   declarations block, seed `delivery/roadmap.md` + `delivery/board.md`, finalize `README.md`.
5. Move the raw `02-inbox/` original to `95-archive/<slug>/<date>-<name>.md`. Never delete it.

## Guard-rails
- One project = one folder. Pick the lightest type that fits (internal-tool is leanest).
- If type/channel/scope is ambiguous, ASK before scaffolding.

---
## Prompt (copy-paste for web chat)
> Read the notes I pasted. Tell me if this is a client or internal project and which of the 4
> types fits (internal-tool / internal-product / client-simple / client-complete). Then write
> a structured brief (problem, scope in/out, stakeholders, success criteria, risks) and a list
> of open questions — mark anything not stated as ASK-CLIENT/ASK-PO. Don't invent requirements.
