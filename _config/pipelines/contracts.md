---
type: pipeline
pipeline: contracts
status: active
created: 2026-05-27
updated: 2026-05-27
tags: [pipeline, commercial, legal]
---

# Pipeline — contracts (generic)

> Contract flow that runs alongside [[sales]]. Edit to your jurisdiction/terms. Each stage
> points at a contract model in `_templates/contracts/<lang>/`.

## Stages

### 1. Discovery contract
- Before the paid Discovery starts.
- **Docs:** [[discovery-contract]] + [[nda]] (if regulated/total NDA).
- **Gate:** signed → Discovery executes. (Discovery fee is typically credited to the project's
  first invoice — note it on the contract and in [[invoicing]].)

### 2. Service contract
- After Discovery is delivered and the project proposal is accepted.
- **Doc:** [[service-contract]] (scope ref = the accepted proposal package; payment milestones;
  FX clause if cross-currency/long; portfolio rights).
- **Gate:** signed → [[kickoff]] creates the project; milestones go to [[invoicing]].

> Variations by tier/region (fixed-price vs monthly squad, FX clauses, NDA level) live in the
> model and in the project's `finance.md` / `contract.md`.
