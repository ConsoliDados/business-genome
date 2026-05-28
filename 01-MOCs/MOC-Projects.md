---
title: "MOC — Projects"
type: moc
status: active
created: 2026-05-26
updated: 2026-05-26
tags: [moc]
---

# MOC — Projects

Dashboards: [[active-projects]] · [[portfolio.base|portfolio]] · [[tasks]] · [[doc-tracker]].

## All projects
```dataview
LIST
FROM "projects"
WHERE type = "project"
SORT project-type ASC
```

## Start one
Describe the intent to the agent (see the routing table in [[AGENTS.md]]), or copy a scaffold
from `96-templates/_project-<type>/`.
