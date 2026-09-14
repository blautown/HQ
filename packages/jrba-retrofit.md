# JRBA retrofit — packaged work

**Status:** In progress, verified against source of truth as each piece
lands. See `TASKS.md`. This file is what GPT/Cursor converts into
Linear tasks — Linear tickets should link back here rather than
restating the work, so there's one place the spec actually lives.

## What this is, and why it's shaped differently from a normal build

This is not a new asset build like `prospect-outreach-manager.md`. JRBA
already has two live agents (Documentation Manager, ShiftCare/Invoice-
Billing Manager) built and refined directly in the field by the
founder, before HQ's current DK:0/DK:1 standard existed. The work is
the reverse of the normal order: stocktake what's already live, close
the gaps against HQ's asset model, and only then hand the founder a
finished package to redeploy — landing back at the same operating
position JRBA is in today, except backed by a real repo, a deployment
record, and complete asset packages instead of ungoverned field builds.

All instance-specific material (binding sheets, redacted recon,
manifests, benchmark evidence, agent home folders) lives in a separate
repo, `binding001-jrba` (`github.com/blautown/binding001-jrba`,
private) — not in this repo. HQ holds only the reusable assets: the
two DK:0 cards and the two new DK:1 plugins.

**Hard execution boundary, confirmed by the founder:** no AI tool
executes live actions against JRBA's actual connected systems (Drive,
ShiftCare) from outside JRBA's own Claude Project — not Claude Code,
and the same logic applies to any Cursor/GPT session. Agents go in and
out of a client's connected systems via one consistent point: the
client's own Claude Project, run by the founder in their admin seat.
This package's remaining live steps are therefore founder-executed,
not GPT/Cursor-executed — Cursor's job here is Linear bookkeeping, not
touching JRBA's systems.

## Distribution

| Item | Deliverable | Owner | Where | State |
| --- | --- | --- | --- | --- |
| Repo scaffold | `binding001-jrba` (binding/, recon/, manifests/, benchmark-evidence/, decisions/, agents/) | Claude Code | `binding001-jrba` | Done |
| Gaps register | `gaps-register.md` | Claude Code | `binding001-jrba` | Done |
| Redacted recon dumps | `recon/documentation-manager-raw-dump.md`, `recon/shiftcare-manager-raw-dump.md` | Claude Code | `binding001-jrba` | Done |
| HQ box-asset additions | `dk0/documentation-manager.md`, `dk0/invoice-billing-manager.md` | Claude Code | This repo | Done |
| DK:1 plugins | `specialties/ndis-audit-readiness.md`, `specialties/ndis-claims-plan-manager.md` | Claude Code | This repo | Done |
| Establishment protocol update | `dk0/establishment.md` (retrofit note + field-tested recon questions) | Claude Code | This repo | Done |
| Agent home folders | `agents/jrba-documentation-manager/`, `agents/jrba-shiftcare-manager/` (birth.md + identity.md + plugin.md mirrors) | Claude Code | `binding001-jrba` | Done |
| Binding-sheet confirmation | `binding/documentation-manager.md`, `binding/invoice-billing-manager.md` — fill `[confirm]` fields (named actor, identity check), resolve which seat carries the claims/plan-manager plugin | **Founder** | JRBA's own live Claude Project, using the two `birth.md` scripts | Pending |
| Connector classes on record | Same two binding-sheet files | **Founder**, written back by Claude Code once reported | `binding001-jrba` | Pending |
| Benchmark Lanes 0-2 (config, boundary, synthetic QA) | Per `benchmark.md` | Claude Code can draft synthetic fixtures; founder runs them against the live seats | `binding001-jrba/benchmark-evidence/` | Not started |
| Benchmark Lanes 3-4 (real supervised task, repeatability) | Per `benchmark.md` | **Founder**, in JRBA's live project | `binding001-jrba/benchmark-evidence/` | Not started |

**Sequence:** repo scaffold → gaps register → redacted recon → HQ
box-asset additions → DK:1 plugins → establishment protocol update →
agent home folders (all done) → founder-run establishment in JRBA's
live project → write-back to `binding001-jrba/binding/*.md` → benchmark
lanes.

## Open item carried into the founder's establishment session

Both `agents/jrba-documentation-manager/birth.md` and
`agents/jrba-shiftcare-manager/birth.md` flag the same unresolved
question: the real bulk-claims/myplace-portal work was observed coming
out of the Documentation Manager seat in the field, but
`specialties/ndis-claims-plan-manager.md` was drafted against the
Invoice/Billing Manager role by subject-matter fit. The founder
resolves this directly, at establishment, not by assuming role-fit
placement — the answer gets recorded on whichever binding sheet ends
up correct.

## Instructions to GPT/Cursor: representing this on Linear

- Create one Linear project/epic: "JRBA retrofit." Link it to this
  file (`packages/jrba-retrofit.md`) rather than copying the table
  into the epic description.
- Create tasks matching the Distribution table's rows. Mark the eight
  "Done" rows as done only after independently confirming the actual
  files exist and match this table — don't take the "Done" state in
  this table on faith; that's exactly the failure mode
  `collaboration.md` warns about (a status report describing an
  intent isn't confirmation until someone re-reads the changed file).
- Create the "Pending"/"Not started" rows as open tasks, assigned to
  the founder, not to GPT or Claude Code — this package has no
  GPT-executed work package in it, unlike `prospect-outreach-manager.md`.
  Do not assign yourself a task here without relaying that back through
  the founder first, per `collaboration.md`'s handoff protocol.
- Set dependencies: binding-sheet confirmation blocks benchmark Lanes
  0-2, which block Lanes 3-4.
- Do not mark a Linear task done when a file merely exists — per
  `collaboration.md`, a task is done once the other side has verified
  the actual diff against source of truth. For the founder-executed
  rows, that means the binding sheet actually reads BOUND with real
  confirmed fields, not a drafted placeholder.
- Don't write a Linear status that reads as GPT (or Claude Code)
  certifying its own work as approved — same rule as
  `claude-code-proposal.md`'s status line and
  `prospect-outreach-manager.md`'s task states. Task state changes;
  founder approval and verification are two different, both-visible
  things.
