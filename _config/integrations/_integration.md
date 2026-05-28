---
type: integration
tool: "<tool-name>"
module: "<which module, e.g. crm>"
direction: "<vault→tool | tool→vault | two-way>"
status: planned
created: 2026-05-27
updated: 2026-05-27
tags: [integration]
---

# Integration — <tool> (e.g. Bitrix24 for CRM)

> Template for documenting how an external system maps to a vault module. **The vault models the
> integration; it does not run a live sync by itself** — actual syncing is a separate connector
> (the tool's API / a script / an automation platform). This note is the spec for that.

## Why
- What this tool owns vs what the vault owns. (e.g. Bitrix24 = system of record for the CRM
  pipeline; vault keeps the strategic/commercial docs and links out.)

## Field mapping
| Vault field | Tool field | Direction | Notes |
|-------------|-----------|-----------|-------|
| lead.status | deal.stage | tool→vault |  |
| account     | company   | two-way   |  |

## Sync approach
- Mechanism (API/webhook/export), cadence, source of truth per field, conflict rule.

## Module state
- Set the module to `external:<tool>` in [[genome]] (or `dormant` if not used yet).

## Open items
- [ ] … **ASK**
