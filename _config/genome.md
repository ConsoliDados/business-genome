---
type: genome-config
status: template-default
company: "<your company>"
languages: [en]
tiers: [T1.5, T2, T3, T4, T5]
pipelines: [sales, contracts]
modules:
  projects: active
  commercial: active
  crm: active
  finance: active
  editorial: active
integrations: []
created: 2026-05-27
updated: 2026-05-27
tags: [config]
---

# Genome config

> The manifest the agent reads to know **this vault's shape**. Edit by hand or — much easier —
> run the [[init]] skill ("**init genome**"), which interviews you and rewrites this file.
> `status: template-default` means `init` hasn't run yet (fresh clone).

## Modules
Each module is `active | dormant | removed | external:<tool>`:
- **active** — in use.
- **dormant** — not used now but kept for later → its folder is moved to `_dormant/<module>/`
  (out of dashboards/graph/search); reactivate by moving it back.
- **removed** — deleted.
- **external:<tool>** — handled by an outside system (e.g. `crm: external:bitrix24`); see
  `_config/integrations/<tool>.md` for the sync mapping.

## Languages
Content languages for the model library (proposals/contracts/meetings/emails). Models live
under `_templates/<kind>/<lang>/`. `en/` ships by default; `init` generates the others you pick.

## Tiers
The engagement tiers/bands you sell (edit to your own). Used to vary proposals, meeting scripts
and document sets per tier.

## Pipelines
The commercial/ops pipelines you run — one note each in `_config/pipelines/`. Ship generic:
[[sales]] and [[contracts]]. Add/extend via the [[pipeline]] skill (you can have several).

## Integrations
External systems wired to a module (e.g. Bitrix24 for CRM). Each gets a note in
`_config/integrations/`. The vault **models** the integration (what/which fields/direction);
live sync is a separate connector, not done by the vault itself.
