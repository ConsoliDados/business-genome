# ConsoliDados — Business Vault (template genome)

Agentic Obsidian vault for **business-level project management** at ConsoliDados:
internal projects (own tools & products) and client engagements, plus CRM, company strategy,
finance and editorial content. The **business/commercial/macro** layer — the technical
architecture docs live with the code, in each project's repo.

> **The brain is [[AGENTS.md]]** (`CLAUDE.md` symlinks to it). Any CLI agent reads it first.

## Use it for your own company (clone → `init genome`)

This is a **generic template**. To make it yours:
1. **Clone** this vault folder and open it in your agent (Claude Code / OpenCode).
2. Say **"init genome"** → the agent runs the [[init]] skill: an interview that configures your
   **pipelines** (sales + contracts ship generic — you edit on top), **languages** (model library
   in EN/PT/ES/…), **tiers**, **module states**, and **integrations** (e.g. CRM via Bitrix24).
3. In `init` you can keep a module, set it **dormant** ("no CRM yet" → moved to `99-dormant/`,
   reactivate later), **remove** it, or mark it **external** (run by another tool).

Config lives in `97-config/` (`genome.md` manifest + `pipelines/` + `integrations/`). Reusable
commercial models (proposals, contracts, meetings, emails/questionnaires) live in
`96-templates/<kind>/<lang>/` — generic, and the agent **creates them on demand** if missing.

## Pillars

| Folder | What |
|---|---|
| `11-projects/internal/`, `11-projects/clients/` | one folder per project; 4 modular types |
| `10-crm/` | `leads/` (pre-sale) + `accounts/` (client companies) |
| `13-company/` | `strategy/` `pricing/` `finance/` `people/` (company-level) |
| `12-editorial/` | multi-channel content: `ideas/` `posts/` `series/` `guides/` |
| `02-inbox/` → `95-archive/` | raw capture → dead storage (excluded from queries) |
| `97-config/` | `genome.md` manifest + `pipelines/` + `integrations/` (set by `init`) |
| `96-templates/` | 4 project scaffolds + Templater files + **model library** (`meetings/ emails/ proposals/ contracts/` per language) |
| `98-skills/` | layered playbooks: `_flows/` (multi-step) + atomic skills |
| `00-dashboards/` | Bases roll-ups + Dataview/Tasks views |
| `99-dormant/` | modules turned off (excluded from queries; reactivate by moving back) |
| `01-MOCs/`, `14-meeting-notes/`, `15-daily/` | indexes, company meetings, dailies |

## Project types

- **internal-tool** — lean: brief → kickoff → board.
- **internal-product** — heavy: feasibility, market, personas, business-plan + product delivery.
- **client-simple** — T1.5/T2, fixed-price, lean commercial.
- **client-complete** — T3/T4, discovery → proposal → contract → multi-sprint delivery.

## Starting a new project

**Driven by a CLI agent (recommended):** just describe the intent — *"qualify this lead",
"structure the briefing and start the project"* — the agent picks the skill in `98-skills/` and
copies the right scaffold. See the routing table in [[AGENTS.md]].

**Manual (Obsidian):** copy `96-templates/_project-<type>/` into `11-projects/<area>/<slug>/`,
**rename the home note `_home.md` → `<slug>.md`** (so it shows by project name, not "README"),
replace the `{{…}}` tokens (`{{slug}}`, `{{Name}}`, `{{date}}`, `{{client-slug}}`,
`{{currency}}`, `{{repo}}`), and fill the declarations block in `<slug>.md`.

## Conventions (short)

Mandatory frontmatter (`type`, `status`, `created`) · wikilinks only · lowercase-kebab-case ·
English-first (per-project content may be pt_BR for BR clients) · one project = one folder ·
never delete `02-inbox/` originals (archive them). Full rules in [[AGENTS.md]].

## The boundary

Business truth → this vault. Technical/architecture truth → the code repo. SRS/SAD here are
**snapshots** with a `source:` pointer; never the canonical original.
