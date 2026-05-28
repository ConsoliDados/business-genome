---
title: "Doc tracker"
type: dashboard
status: active
created: 2026-05-26
updated: 2026-05-26
tags: [dashboard]
---

# Doc tracker

> Tracks the SRS/SAD **snapshots** and the human-in-the-loop review of changes to them.

## Pending Review — Change Summaries

> The `srs-sad-snapshot` skill adds an entry here whenever it edits a snapshot, then removes it
> once you approve. Shape:

<!--
### [[srs-<slug>]] — short summary (YYYY-MM-DD)

| Section | ~Line | What changed |
|---------|-------|--------------|
| §1.2 Functional requirements | ~30 | added REQ-008; reworded REQ-003 |
-->

## Snapshots (source of truth = the code repo)
```dataview
TABLE WITHOUT ID file.link AS "Doc", source AS "Source (repo)", updated AS "Updated"
FROM "projects"
WHERE type = "snapshot"
SORT updated DESC
```
