# JYOps HQ — tasks

If this list doesn't happen, the architecture stays in chat and dies.

Board: [Jy-ops HQ](https://linear.app/jyoperatives/project/jy-ops-hq-c97adc455f76). This file stays the ordered list. Linear is the tracker, not a product to build.

Claude Teams: two seats stay JRBA. Do not move them until a starter is clearly better. Extra Claude seat only if that project already makes money.
Live site: GitHub jyoperatives/personal-ops branch claude/jyops-landing-page-xxkxg5. Not this repo.
This repo is founder HQ only.

## Now — write the base (DK:0)
- [x] Put domain-knowledge boundaries card next to the DK classes (`dk0/domain-knowledge-boundaries.md`) — generic boundaries only, ZERO mention of any specialty by name
- [x] Write DK:0 Document Manager O.G. (file hands only: retrieve, pre-fill, file, recon, session gate, subtree lock)
- [x] Write DK:0 Recordkeeper / invoice manager O.G. (plain-English CRM chat + billing/recordkeeping, no specialty)
- [x] Write establishment prompt: first launch is recon to gather instance context from the user, then bind
- [ ] Update map.md: founder → DK:0 agents → DK:1 plugins → project instance (JRBA is one instance, not the chair)
- [x] Name the bind output as role-specific context ROM in map.md — identity, operational guidelines, domain knowledge plugin, and project context attach as separate sources so one breaking doesn't cascade
- [x] Write DK:0 restore point (`dk0/restore-point.md`) — weekly, verified-clean config snapshot chained to a CLEAN drift check; the recovery half drift check itself doesn't provide
- [x] Write `claims.md` — trace every published marketing claim to the process that backs it, flag gaps before pushing marketing harder
- [x] Write and reconcile `offer.md` — transcribe the live landing-page terms for registration-ready, audit-pass, overheads, data handling, and 24/7 support. Commission outcome ≠ JYOps process outcome. Fifty functions / PBS ops stay UNPUBLISH
- [x] Define this workspace and downstream destinations (`workspace.md`) — HQ shelf/control plane, founder benchmark, bound project, client systems/output, private archive, and separate shopfront
- [x] Draft Claude Code execution and verification proposal (`claude-code-proposal.md`) — keep asset production, client deployment, and market/public execution separate
- [x] Reconcile the asset model across `dk0/domain-knowledge-boundaries.md`, `README.md`, `TASKS.md`, and `CLAUDE.md` — identities + operational guidelines + domain knowledge plugins remain box assets until client deployment benchmarks the DK:1 agent
- [x] Define Grokbot participation (`grokbot.md`) — landing-page editing/maintenance, live support chat, notifications, and current Google Ads execution
- [ ] Founder-adopt the published shopfront terms in `offer.md` — confirm the landing-page terms are the controlled JYOps offer, then separately confirm the decline list and any client-seat interpretation
- [ ] Retrofit JRBA's two live seats to current standard (`instances/jrba.md`):
  - [ ] Fill the `[confirm]` fields (Named actor, Identity check) on both binding sheets from a real session — not guessed
  - [ ] Confirm the JRBA operator's project access is view-only, not edit, on both bound projects
  - [ ] Send the operator a filled-in `client-brief.md`
  - [ ] Run a baseline `dk0/drift-check.md` on both seats
  - [ ] Take the first `dk0/restore-point.md` snapshot off the back of a CLEAN result, then start the weekly cadence
- [ ] Benchmark the two JRBA deployments against their HQ identities, operational guidelines, and domain knowledge plugins using [`benchmark.md`](benchmark.md): configuration, boundaries, box-asset QA, supervised real task, repeatability, and plugin extraction decision

## Now — Prospect/Outreach Manager (verified, packaged for work)
Business-development asset: finds NDIS-registered providers who could become JYOps clients. Built with the same DK:0/DK:1 discipline as any other box asset, bound to Jyops itself rather than a served client — a valid case per the corrected benchmark-location rule (`dk0/domain-knowledge-boundaries.md` "Where the benchmark actually lives": benchmarking always happens in the founder's admin seat, whichever workspace that seat sits inside).
- [x] Draft build plan, verify against `dk0/domain-knowledge-boundaries.md` and `dk0/drift-check.md`, fix the two findings (WP3/WP7 "sending mailbox/identity" → "sending display name" to avoid writing an email into HQ; confirm the NDIS citation is real), and correct the benchmark-location rule repo-wide (`dk0/domain-knowledge-boundaries.md`, `CLAUDE.md`, `README.md`, `workspace.md`, `map.md`, `benchmark.md`) — see [`packages/prospect-outreach-manager.md`](packages/prospect-outreach-manager.md) for the packaged work and agent prompts
- [x] WP1 — DK:0 identity + operational guidelines card (`dk0/prospect-outreach-manager.md`) — Claude Code, this repo
- [x] WP2 — DK:1 plugin (`specialties/ndis-outreach-compliance.md`) — Claude Code, this repo
- [x] WP3/WP6 — binding-sheet stub + drift-check compatibility (`instances/jyops-outreach.md`) — Claude Code, this repo
- [x] Create [`agents/prospect-outreach-manager/`](agents/prospect-outreach-manager/) — `birth.md` onboarding script plus live mirrors of the identity, plugin, and binding sheet, so the deployed agent has one named place to point itself at instead of a chat-pasted snapshot
- [ ] WP5 — connector-class build (Claude Project: Gmail + tracking store, pointed at `agents/prospect-outreach-manager/`) — GPT, Cursor / live build
- [ ] WP4 — gate/state wiring (executable checks inside the WP5 Project, not application code in this repo) — GPT, Cursor / live build
- [ ] WP7 — establishment / go-live, per `agents/prospect-outreach-manager/birth.md` — GPT, Cursor / live build, with the founder as the actual operator triggering bind

**Restart note:** the first WP5 build attempt (a Claude Project named "Leads/Outreach") was deleted with nothing retained. Repo documentation was rewound to its pre-WP5 state and this `agents/` folder replaces the earlier copy-paste handoff approach. WP5/WP4/WP7 start fresh from here.

## Next — forge from JRBA without living there
JRBA is the gym/benchmark. Do not centre founder time there.
- [ ] Write down what live Doc Manager actually is: directory assistant + NDIS audit expert + PBS audit register/policy suite
- [ ] Write down what live CRM actually is: bulk shift tool, invoices to plan managers, PRODA bulk claim, plan-managed vs agency-managed, one chat
- [ ] Draft DK:1 plugin: NDIS PBS audit-readiness suite
- [ ] Draft DK:1 plugin: NDIS core-module audit-readiness suite
- [ ] Draft DK:1 plugin: NDIS claims / PRODA / plan-manager split
- [ ] Only if a starter is clearly better than the live seats: redeploy JRBA onto it

## Then — founder pay-off
- [ ] Dissect the running JRBA stack into DK:1 agents on this shelf (whole NDIS-scoped actors, not a plugin drawer)
- [ ] PBS brain pack: assign a job or leave packed (therapy assistant is an example, not approved)

## Not this list
Supabase, NDIS IQ, marketing campaign, swarm, work-history files, charting-tool shopping.
