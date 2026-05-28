---
title: "MOC — Editorial"
type: moc
status: active
created: 2026-05-26
updated: 2026-05-26
tags: [moc]
---

# MOC — Editorial

[[editorial/README|Editorial overview]] · guides: [[voice]] · [[channels]] ·
roll-up: [[editorial.base]].

## Posts
```dataview
TABLE channel AS "Channel", publish-status AS "Status", publish-date AS "Date"
FROM "editorial/posts"
WHERE type = "post"
SORT publish-date DESC
```

## Ideas
```dataview
LIST
FROM "editorial/ideas"
WHERE type = "idea"
```
