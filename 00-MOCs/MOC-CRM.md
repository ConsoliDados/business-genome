---
title: "MOC — CRM"
type: moc
status: active
created: 2026-05-26
updated: 2026-05-26
tags: [moc]
---

# MOC — CRM

[[crm/README|CRM overview]] · pipeline roll-up: [[pipeline.base]].

## Leads
```dataview
TABLE company AS "Company", status AS "Stage", engagement-tier AS "Tier"
FROM "crm/leads"
WHERE type = "lead"
SORT status ASC
```

## Accounts
```dataview
LIST
FROM "crm/accounts"
WHERE type = "account"
```
