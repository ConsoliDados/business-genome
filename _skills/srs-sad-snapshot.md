---
title: "Skill — srs-sad-snapshot"
type: skill
status: active
created: 2026-05-26
tags: [skill, architecture, boundary]
---

# Skill — srs-sad-snapshot

> **CLI:** run to pull a high-level SRS/SAD snapshot from the code repo into the vault.
> **Web-chat:** paste the prompt with the repo doc contents.

**Reads:** `<repo>/docs/.../architecture/{srs,sad,srs+sad}.md` · **Writes:**
`…/architecture/srs-<slug>.md` and `…/architecture/sad-<slug>.md` (named by project, so they're
distinguishable in the `doc-tracker` view — not generic `srs-snapshot.md`).

## Steps
1. Read the **canonical** SRS/SAD from the repo (path in the project's `repo:` field).
2. Distill the **macro** view only: SRS → purpose + functional requirements (REQ-level) +
   NFRs + out-of-scope; SAD → high-level shape + modules + key dependencies + future directions.
3. Set `source:` to the repo path. Mark clearly: **snapshot, not source of truth**.
4. On change, log a "Pending Review — Change Summaries" entry in [[doc-tracker]] (section/line/
   delta) and remove it once the human approves.

## Guard-rails
- **Never** copy ADRs/SDDs/data-model/threat-model up. Never edit the snapshot as if canonical —
  the repo is the source of truth.

---
## Prompt (copy-paste)
> Here is the repo's SRS/SAD. Produce a high-level snapshot for non-engineering stakeholders:
> SRS (purpose, REQ-level functional requirements, NFRs, out-of-scope) and SAD (high-level shape,
> modules, key dependencies, future directions). Mark it clearly as a snapshot whose source of
> truth is the repo.
