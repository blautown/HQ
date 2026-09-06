# Jy-ops — founder HQ

This repo is founder HQ: both the reusable asset shelf and the main operational board for JYOps. Planning, packaging, development, deployment preparation, and client operations are coordinated here. It is not JRBA and not the live website.

Claude Teams: two seats stay JRBA. Extra seat only if that project already makes money.
Live site: GitHub `jyoperatives/personal-ops` branch `claude/jyops-landing-page-xxkxg5`. Not this repo.

Markdown only. No secrets, no emails, no Drive IDs, no participant names, no staff IDs.

**Workspace charter:** [`workspace.md`](workspace.md). Read it for what belongs here, how Claude operates in the repo, how Grok campaign bots and the website connect to HQ, where work ends up, and how HQ fits into the wider system.

## HQ asset library

**Read first:** [`dk0/domain-knowledge-boundaries.md`](dk0/domain-knowledge-boundaries.md) — the DK:0 / DK:1 line, before opening any asset below.

Three separate asset classes:

- **Identities** — domain managers, domain assistants, and domain record-keepers.
- **Operational guidelines** — reusable role instructions without project-specific context.
- **Domain knowledge plugins** — domain knowledge linked directly to the plugin that uses it.

These remain box assets plus domain knowledge until they combine with project-specific context in the founder's admin seat, inside whichever workspace the deployment serves (a client's system, or the founder's own business). The resulting deployment is the DK:1 agent benchmark.

- [`dk0/documentation-manager.md`](dk0/documentation-manager.md) — Documentation Manager. File hands: retrieve, pre-fill, file, recon, session gate, subtree lock.
- [`dk0/invoice-billing-manager.md`](dk0/invoice-billing-manager.md) — Invoice / Billing Manager. Plain-English CRM chat + billing/recordkeeping.
- [`dk0/mcp-service-manager.md`](dk0/mcp-service-manager.md) — MCP-connected service manager (placeholder). Identity locks at bind. Not a domain.

## DK:1 — NDIS

NDIS is domain knowledge because of legislative governance (NDIS Rules 2018, practice guidelines, operational governance). Do not invent statute text. Do not sand that off when stripping org names.

First: plugins linked to domain knowledge and attached to the selected identity and operational guidelines at deployment.

- PBS audit-readiness suite
- Core-module audit-readiness suite
- NDIS claims / PRODA / plan-manager

After a client deployment proves the combined package, the result can be treated as a benchmarked **DK:1 agent** and later dissected by role. Until deployment, it remains box assets plus domain knowledge — not an agent.

## Establishment

First launch is recon, then bind. Not a domain. Prompt: [`dk0/establishment.md`](dk0/establishment.md). Paste it into the factory seat. Do not operate until the binding sheet is confirmed and the session gate passes.

## Drift check

Restate scope, diff against the binding sheet, confirm a plugin still dismantles cleanly. Not a monitored system — run it on a cadence you choose, or before trusting a "quick fix" a live seat proposed on its own. Prompt: [`dk0/drift-check.md`](dk0/drift-check.md). Needs a binding sheet to diff against — JRBA's live: [`instances/jrba.md`](instances/jrba.md).

## Restore point

Drift check diagnoses; it does not fix. [`dk0/restore-point.md`](dk0/restore-point.md) is the recovery half — a weekly, verified-clean configuration snapshot taken right after a CLEAN drift check, so a bad edit or drift rolls back instead of getting rebuilt from memory. Not the same word as "benchmark" — JRBA and the founder's seat keep that meaning; this is a dated restore point.

## JRBA is not the chair

JRBA is one project/instance. Gym/benchmark. Founder effort is JYOps.

$61k was JRBA billing, not Jacob's wage. Takeaway: less effort / the worker on the shelf.

## PBS brain

Unused specialty pack. Eleven modules as an MCP pointed at Claude Code. Could later mint a therapy-assistant role. **Not approved as a build.**

## Rules

- Work-history files are not required.
- No swarm design until one real DK:1 exists. Swarm = more seats on a named binding, not CVs.
- Two seats stay JRBA until a starter is clearly better.

## How to add

1. An **identity** — domain manager, domain assistant, or domain record-keeper.
2. **Operational guidelines** — reusable role instructions without project-specific context.
3. A **domain knowledge plugin** — sourced directly from the relevant domain knowledge.
4. A **deployed DK:1 agent** — identity + operational guidelines + plugin + project context, benchmarked in the founder's admin seat.

Ordered list: [`TASKS.md`](TASKS.md). Map: [`map.md`](map.md). Workspace charter: [`workspace.md`](workspace.md). Claude Code execution proposal: [`claude-code-proposal.md`](claude-code-proposal.md). Claude Code's response on GPT/Claude Code roles: [`collaboration.md`](collaboration.md). Grokbot operating boundary: [`grokbot.md`](grokbot.md). Deployment benchmark: [`benchmark.md`](benchmark.md). Onboarding & pricing: [`factory.md`](factory.md). Client-facing behaviour brief: [`client-brief.md`](client-brief.md). Shopfront word meanings: [`offer.md`](offer.md). Marketing-claim traceability: [`claims.md`](claims.md).
