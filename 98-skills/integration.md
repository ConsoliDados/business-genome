---
title: "Skill — integration"
type: skill
status: active
created: 2026-05-27
tags: [skill, integration]
---

# Skill — integration

> Wire a module to an external tool (e.g. **Bitrix24** for CRM). The vault **models** the
> integration; it does not run a live sync itself.

**Writes:** `97-config/integrations/<tool>.md` (from `_integration.md`) + updates [[genome]].

## Steps
1. Copy `97-config/integrations/_integration.md` → `<tool>.md`.
2. Fill: why (what the tool owns vs the vault), **field mapping** table, sync approach
   (API/webhook/export, cadence, source-of-truth per field, conflict rule), direction.
3. Set the module to `external:<tool>` in `97-config/genome.md` (or `dormant` if not live yet).

## Guard-rails
- Be explicit that **live sync is a separate connector** (API/script/automation), not the vault.
  This note is its spec.

---
## Prompt (copy-paste)
> Set up an integration note for <tool> handling the <module> (e.g. Bitrix24 / CRM): what it owns
> vs the vault, a field-mapping table, the sync approach and direction. Mark the module external in
> the genome config.
