# Jy-ops HQ

Jy-ops HQ is the founder's reusable asset shelf and operational board for JYOps: where identities, operational guidelines, and domain-knowledge plugins are built, packaged, and prepared for deployment. Full charter: [`workspace.md`](workspace.md). Architecture: [`map.md`](map.md).

Markdown only. No secrets, no emails, no tenant/Drive IDs, no participant or staff identifiers.

## Repository purpose and boundaries

Jy-ops HQ is the founder's product control plane and asset factory for
JYOps: identities, operational guidelines, domain-knowledge plugins, and
packaged deployment templates are defined, reviewed, and versioned here.

HQ is not a live client system, a secrets store, or a runtime. It must
never contain credentials, tokens, API keys, tenant or database IDs,
participant/staff/customer identifiers, live CRM or document contents, raw
chat transcripts, or private restore-point snapshots.

Commercial and legal content (pricing, guarantees, claims, marketing
governance) lives in `commercial/`, separate from the reusable agent
architecture in `agents/`, `packages/`, `specialties/`, and `dk0/`.

## Repo structure

- [`workspace.md`](workspace.md) — what belongs here, what doesn't, and where work ends up
- [`map.md`](map.md) — architecture: the asset library, deployment, and market/public processes
- [`CLAUDE.md`](CLAUDE.md) — operating contract for Claude Code in this repo
- [`collaboration.md`](collaboration.md) / [`claude-code-proposal.md`](claude-code-proposal.md) — role split and handoff protocol between GPT and Claude Code
- [`TASKS.md`](TASKS.md) — the ordered work list
- `dk0/` — identities and operational guidelines (box assets, no domain knowledge). Read [`dk0/domain-knowledge-boundaries.md`](dk0/domain-knowledge-boundaries.md) first, before opening any other file in this folder.
- `specialties/` — domain-knowledge sources and DK:1 plugins that clip onto a `dk0/` identity
- `instances/` — safe, org-stripped binding sheets for established deployments
- `agents/` — one dedicated folder per deployed agent: a `birth.md` onboarding script plus live mirrors of that agent's box assets and binding sheet
- `packages/` — verified work-package breakdowns and agent prompts for building a new asset
- [`benchmark.md`](benchmark.md) — how a deployment gets benchmarked into a proven DK:1 agent
- `commercial/` — pricing, guarantees, claims, and marketing-governance content, separate from the reusable agent architecture
- [`commercial/grokbot.md`](commercial/grokbot.md) — Grok bots' operating boundary (landing page, live chat, ad campaign)
- [`commercial/offer.md`](commercial/offer.md) / [`commercial/claims.md`](commercial/claims.md) — shopfront word meanings and public-claim traceability
- [`commercial/factory.md`](commercial/factory.md) / [`client-brief.md`](client-brief.md) — commercial onboarding and handoff

## Asset model

Three box-asset classes, kept separate so any one can be corrected or upgraded without touching the others:

- **Identities** — domain managers, domain assistants, and domain record-keepers.
- **Operational guidelines** — reusable role instructions, no project-specific context.
- **Domain knowledge plugins** — domain knowledge linked directly to the plugin that uses it, clipped onto an identity's operational guidelines.

These stay box assets plus domain knowledge until they combine with project-specific context in the founder's admin seat — that combination is what benchmarks a deployment into a proven DK:1 agent. Establishment (recon, then bind) is documented in [`dk0/establishment.md`](dk0/establishment.md); drift check and restore point in [`dk0/drift-check.md`](dk0/drift-check.md) and [`dk0/restore-point.md`](dk0/restore-point.md).

## How to add a new asset

1. An **identity** — domain manager, domain assistant, or domain record-keeper.
2. **Operational guidelines** — reusable role instructions without project-specific context.
3. A **domain knowledge plugin** — sourced directly from the relevant domain knowledge, if the role needs one.
4. A **deployed agent** — identity + operational guidelines + plugin + project context, benchmarked in the founder's admin seat.

See `packages/` for the verified work-package pattern, and `agents/` for how a deployed agent gets its own live-mirror folder once built.
