---
title: "CRM"
type: moc
status: active
created: 2026-05-26
updated: 2026-05-26
tags: [crm, index]
---

# CRM

Pre-project, cross-cutting. Lives outside `projects/`.

- `leads/` — pre-sale leads. Qualify with the [[qualify-lead]] skill; create with
  `_templates/tp-lead.md`.
- `accounts/` — client companies. **One account → many projects.** Create with
  `_templates/tp-account.md`.

A lead that converts → [[kickoff]] creates the project under `projects/clients/`; the project
links back to its account via the `client:` frontmatter field. Pipeline roll-up: [[pipeline.base]].
