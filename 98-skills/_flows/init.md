---
title: "Flow — init (init genome)"
type: skill
kind: flow
status: active
created: 2026-05-27
tags: [skill, flow, setup]
---

# Flow — init ("init genome")

> Run **once on a fresh clone** to configure the vault to *this* user's profile. The human says
> **"init genome"** (CLI) and you run this interview + reconfigure. The template ships generic
> defaults — your job is to tailor them, explaining each generic piece so the user adjusts on top.

**When:** `97-config/genome.md` has `status: template-default`.
**Reads/Writes:** `97-config/genome.md`, `97-config/pipelines/*`, `97-config/integrations/*`,
`96-templates/*`, and moves folders into `99-dormant/`.

## Interview — ask one topic at a time; never assume
1. **Company profile** — name, what you sell, ICP.
2. **Languages** for the model library (`en`, `pt`, `es`, …).
3. **Tiers/bands** you sell (default `T1.5–T5`).
4. **Pipelines** — walk through the generic [[sales]] and [[contracts]] (explain each stage);
   let the user edit stages / add pipelines. Most flows are standard; capture the bespoke bits.
5. **Modules** — for `projects / commercial / crm / finance / editorial`, set
   **active | dormant | removed | external:<tool>**. (e.g. "no CRM now, keep for later" → dormant;
   "we use Bitrix24" → external:bitrix24.)
6. **Integrations** — for each `external:<tool>`, fill an [[integration]] note.

## Reconfigure
- **Detach from the template's git history** — this clone becomes the user's own vault and will
  hold real business/client data, so it must be **private** and must NOT share history with the
  public template:
  ```
  rm -rf .git && git init -b main
  gh repo create --private <org>/<name> --source=. --remote=origin
  ```
  (Confirm the org/name with the user. Never push a configured vault to the public template repo.)
- Rewrite `97-config/genome.md`: `status: configured`, company, languages, tiers, pipelines,
  module states, integrations.
- Tailor `97-config/pipelines/*` to the user's stages (or add new pipeline notes).
- Generate the **model library** in the chosen languages: copy `96-templates/<kind>/en/` →
  `<kind>/<lang>/` and adapt/translate. Explain each generic model as you go.
- **Dormant** module → move its folder to `99-dormant/<module>/` (out of dashboards; reactivate by
  moving back). **Removed** → delete (**confirm first**). **External** → write the integration note.

## Guard-rails
- **Confirm before deleting** anything. Don't invent the user's pipeline — ask. Keep English-first
  structure; content language follows their choice.

---
## Prompt (copy-paste for web chat)
> Walk me through setting up this business vault: ask me about my company, the languages I want
> templates in, my tiers, the sales/contract pipelines (start from the generic ones and let me
> edit), which modules to keep/dormant/remove, and any CRM/tool integrations. Then tell me exactly
> what you'd change in `97-config/` and `96-templates/`.
