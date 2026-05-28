---
title: "Active projects"
type: dashboard
status: active
created: 2026-05-26
updated: 2026-05-26
tags: [dashboard]
---

# Active projects

> Dataview view (works out of the box). The typed roll-up lives in `portfolio.base`.

## By status
```dataview
TABLE WITHOUT ID file.link AS "Project", project-type AS "Type", doc-tier AS "Tier", engagement-tier AS "Eng", currency AS "$", status AS "Status"
FROM "projects"
WHERE type = "project"
SORT status ASC, project-type ASC
```

## Clients
```dataview
TABLE WITHOUT ID file.link AS "Project", engagement-tier AS "Tier", status AS "Status", margin-effective AS "Margin"
FROM "projects/clients"
WHERE type = "project"
SORT status ASC
```

## Internal
```dataview
TABLE WITHOUT ID file.link AS "Project", project-type AS "Type", status AS "Status"
FROM "projects/internal"
WHERE type = "project"
SORT status ASC
```
