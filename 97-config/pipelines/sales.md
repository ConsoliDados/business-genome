---
type: pipeline
pipeline: sales
status: active
created: 2026-05-27
updated: 2026-05-27
tags: [pipeline, commercial]
---

# Pipeline — sales (generic)

> A generic senior-consultancy sales flow. **Edit it to your reality** (the [[init]] skill or
> [[pipeline]] skill help). Each stage lists: the **meeting** model, **email/questionnaire**
> models, **documents** to produce (some vary by tier), and the **gate** to advance. When you
> run a stage for a project, the agent copies the stage's models into the project
> (`commercial/`, `meetings/`).

## Stages

### 1. Lead & qualify
- Source the lead → qualify against ICP + identify **tier** (see [[qualify-lead]]).
- **Meeting:** [[first-call]] (questions that reveal the tier + which delivery fits).
- **Email:** [[outreach]].
- **Saves:** `10-crm/leads/<company>.md`.
- **Gate:** ICP fit + tier identified.

### 2. Discovery offer
- Pitch the paid Discovery (value-first) at the right depth for the tier.
- **Email:** [[outreach]] (Discovery + value).  **Doc:** [[discovery-proposal]].
- **Gate:** Discovery accepted (→ contract via [[contracts]] pipeline).

### 3. Discovery kickoff
- Align scope; collect what the client must provide.
- **Meeting:** [[discovery-kickoff]].  **Email/questionnaire:** [[info-request]].
- **Gate:** required info received.

### 4. Discovery research
- Execute discovery; new questions get briefed and gathered into the discovery doc.
- **Email/questionnaire:** [[questionnaire]] (as questions arise).
- **Saves:** `11-projects/clients/<slug>/commercial/discovery.md`.
- **Gate:** discovery doc drafted + project proposal ready.

### 5. Proposal & presentation
- Present the discovery deliverables + the project proposal (**per tier**).
- **Meeting:** [[proposal-presentation]] (vary script by tier).  **Doc:** [[project-proposal]] (3 packages).
- **Gate:** proposal accepted → **contracts** pipeline (service contract) → [[kickoff]].

### 6. Won / lost
- Record outcome; on win, the project is kicked off. On loss, note why (feeds [[portfolio-review]]).
