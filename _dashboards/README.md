---
title: "Dashboards"
type: moc
status: active
created: 2026-05-26
updated: 2026-05-26
tags: [dashboard, index]
---

# Dashboards

Two engines, by design:

- **Bases** (`.base`) — typed portfolio roll-ups: [[portfolio.base|portfolio]],
  [[pipeline.base|pipeline]], [[finance.base|finance]], [[editorial.base|editorial]].
- **Dataview / Tasks** (`.md`) — [[active-projects]], [[tasks]], [[doc-tracker]].

All views are **scoped by folder** so `_templates/` and `_archive/` never pollute them.

> ⚠️ **Bases syntax is Obsidian-version-specific.** On first open, if a `.base` shows an error,
> adjust it in the Bases UI — the schema is small (`filters` / `properties` / `views`). The
> Dataview snippets below are equivalents that work regardless, if you prefer them.

## Dataview equivalents (fallback)

**Leads pipeline** (≈ `pipeline.base`):
```text
```dataview
TABLE company AS "Company", status AS "Stage", engagement-tier AS "Tier", region AS "Region"
FROM "crm/leads"
WHERE type = "lead"
SORT status ASC
```​
```

**Editorial posts** (≈ `editorial.base`):
```text
```dataview
TABLE channel AS "Channel", content-type AS "Format", publish-status AS "Status", publish-date AS "Date"
FROM "editorial/posts"
WHERE type = "post"
SORT publish-date DESC
```​
```

**Finance / margins** (≈ `finance.base`):
```text
```dataview
TABLE currency AS "$", engagement-tier AS "Tier", margin-target AS "Margin↑", margin-effective AS "Margin✓"
FROM "projects"
WHERE type = "project" AND status != "archived"
```​
```
