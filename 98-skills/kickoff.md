---
title: "Skill — kickoff"
type: skill
status: active
created: 2026-05-26
tags: [skill, project]
---

# Skill — kickoff

> **CLI:** run to create a project folder from the right scaffold. **Web-chat:** N/A (file ops).

**Writes:** `11-projects/<area>/<slug>/`

## Steps
1. Pick the type: internal-tool | internal-product | client-simple | client-complete (lightest
   that fits).
2. Copy `96-templates/_project-<type>/` → `11-projects/internal|clients/<slug>/`.
3. **Rename for the views** (so notes show by project, not generic names):
   `_home.md` → `<slug>.md`; and if present, `architecture/srs-snapshot.md` → `srs-<slug>.md`
   and `architecture/sad-snapshot.md` → `sad-<slug>.md`. (The home note's links already point
   to `srs-<slug>` / `sad-<slug>` after token replacement.)
4. Replace **all** `{{…}}` tokens: `{{slug}}`, `{{Name}}`, `{{date}}`, `{{client-slug}}`,
   `{{currency}}`, `{{repo}}`.
5. Fill the **declarations block** in `<slug>.md` (doc-tier, engagement-tier, currency,
   language, `client:`, `repo:`).
6. Seed `delivery/roadmap.md` + `delivery/board.md`; finalize the home note's links.
7. For clients: link/create the account in `10-crm/accounts/`.

## Guard-rails
- One project = one folder. Don't carry modules the type doesn't need.

---
*(No web-chat prompt — this is a file-scaffolding action the CLI agent performs.)*
