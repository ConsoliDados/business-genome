---
title: "MOC — Editorial"
type: moc
status: active
created: 2026-05-26
updated: 2026-05-26
tags: [moc]
---

# MOC — Editorial

[[12-editorial/README|Editorial overview]] · guides: [[voice]] · [[channels]] ·
roll-up: [[editorial.base]].

## Posts
```dataview
TABLE channel AS "Channel", publish-status AS "Status", publish-date AS "Date"
FROM "12-editorial/posts"
WHERE type = "post"
SORT publish-date DESC
```

## Ideas
```dataview
LIST
FROM "12-editorial/ideas"
WHERE type = "idea"
```
