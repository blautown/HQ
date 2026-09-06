# Prospect/Outreach Manager — packaged work

**Status:** Verified against source of truth and packaged for work. See `TASKS.md`. This file is what GPT converts into individual Linear tasks — Linear tickets should link back here rather than restating the work, so there's one place the spec actually lives.

## What changed since the original build plan

The founder's original plan (drafted, seven work packages, verification checklist) was checked against `dk0/domain-knowledge-boundaries.md`, `dk0/drift-check.md`, `dk0/establishment.md`, `CLAUDE.md`, `workspace.md`, `map.md`, and `grokbot.md`. Two findings came out of that pass:

1. **Fixed — hard-boundary risk.** WP3/WP7 said the binding sheet would store "sending mailbox/identity" at go-live. If that meant the literal Gmail address, it would violate the repo's standing rule against writing emails into HQ markdown. Every prompt below uses "sending display name" instead — the real address lives only in the live Claude Project's connector config, never in this repo.
2. **Fixed — benchmark-location rule corrected.** The plan bound this asset to Jyops itself rather than a served NDIS client, which the boundary doc's wording at the time didn't clearly cover. The founder clarified the actual rule: the benchmark always happens in the founder's own admin seat — that never varies; only the workspace that seat sits inside varies (a client's system, or the founder's own business). `dk0/domain-knowledge-boundaries.md` and every other file repeating the old wording (`CLAUDE.md`, `README.md`, `workspace.md`, `map.md`, `benchmark.md`) were corrected to say this. This asset is now a direct instance of the corrected general rule, not a special case.

The NDIS citation in WP2 (`ndis.gov.au/media/2420/download`, Compliance and Enforcement Framework, Education and Outreach) was independently checked and is real — the document and section content match what WP2 claims. The exact "§4.1.1" numbering was search-confirmed, not byte-verified against the PDF directly (it returned a 403 on direct fetch), so confirm the section number when actually drafting WP2.

## Distribution

| WP | Deliverable | Owner | Where |
|---|---|---|---|
| WP1 | `dk0/prospect-outreach-manager.md` | Claude Code | This repo |
| WP2 | `specialties/ndis-outreach-compliance.md` | Claude Code | This repo |
| WP3 + WP6 | `instances/jyops-outreach.md` | Claude Code | This repo |
| WP5 | Claude Project: Gmail connector + tracking store, pointed at `agents/prospect-outreach-manager/` for its identity | GPT | Cursor / live build |
| WP4 | Executable pre-flight gate + halt-on-escalation logic | GPT | Inside the WP5 Project — not application code in this repo |
| WP7 | Go-live: real values, real gate check, first sends | GPT + founder | Live system, with a write-back to `instances/jyops-outreach.md` (canonical) then `agents/prospect-outreach-manager/binding-sheet.md` (mirror), for non-PII fields only |

**Sequence:** WP1 → WP2 → WP3 (Claude Code) → WP5 → WP4 (GPT) → WP7 (GPT + founder). A quick re-check that WP5/WP4's build didn't leak a live fact back into WP1/WP2/WP3 belongs right before WP7 fires.

**WP5 now starts from `agents/prospect-outreach-manager/`, not a copy-paste handoff.** That folder holds `birth.md` (the onboarding script) plus live mirrors of the identity, plugin, and binding sheet. Point the new Claude Project's knowledge at this folder — or that folder's content, however the Project's connector ingests it — rather than pasting file contents into chat. When a canonical HQ file changes, the mirror in that folder needs a deliberate re-sync; nothing pushes automatically.

## Claude Code prompts

### CC-1 — WP1: DK:0 identity + operational guidelines card

```
Write dk0/prospect-outreach-manager.md, following the exact format of
dk0/documentation-manager.md (identity description, then an "Operational
governance guidelines" section). Read dk0/domain-knowledge-boundaries.md's
DK:0 test first: it must be true and complete for any org running this job.
Zero NDIS content, zero org names, zero register content.

Contents:
- Job: source → enrich → draft → send → track.
- Session gate: Gmail connector authenticated + tracking store reachable +
  bound identity matches the binding sheet — all three, or stay Unbound.
- Scope lock: touches only contacts named in the binding sheet's in-scope line.
- Escalation triggers → Halted, hand to operator, no self-correction: bounce,
  spam complaint, unsubscribe request, ambiguous reply, conflicting contact
  data, anything outside in-scope.
- Generic operating rules: naming, ask-vs-assume, halt-vs-guess.
- Generic email-compliance rules that hold for any org: unsubscribe link,
  sender identification, suppression-list enforcement before every send.

Verify the finished card against domain-knowledge-boundaries.md's DK:0 test
before calling it done.
```

### CC-2 — WP2: DK:1 plugin

```
Write specialties/ndis-outreach-compliance.md, clipping onto
dk0/prospect-outreach-manager.md (reference it, don't restate its rules).

Contents:
- NDIS provider vocabulary/roles: registered provider, Support Coordinator,
  Plan Manager, SIL, etc. — so drafted copy reads as informed.
- Cited domain content: NDIS Compliance and Enforcement Framework, Education
  and Outreach section (https://www.ndis.gov.au/media/2420/download).
  Confirm the exact section number against the live PDF before citing it
  numerically — it was search-confirmed as real but not byte-verified.
- State plainly the citation informs messaging credibility (framing outreach
  around the provider's own proactive-compliance posture), not legal
  permission to solicit. If an actual outreach-conduct restriction specific
  to NDIS is needed later, that's a separate, currently-unheld citation —
  do not invent it now.
- Carries no live org data.

Verify the finished plugin against both of domain-knowledge-boundaries.md's
plugin tests (clean detach, self-auditable against its own recorded scope)
before calling it done.
```

### CC-3 — WP3 + WP6: binding-sheet stub

```
Write instances/jyops-outreach.md, following the format of instances/jrba.md.
Bound org: Jyops itself (the founder's own business) — per the corrected
rule in dk0/domain-knowledge-boundaries.md, this is benchmarked in the
founder's own admin seat exactly like any client-bound instance.

Fields: asset name, connector class, in-scope (placeholder for the real
prospect list/ICP), out-of-scope (explicitly: JRBA and every existing
client, always suppressed; explicitly: never shared to any NDIS client
seat/org), plugin attached + version, status, sending display name — never
the literal email address, per CLAUDE.md's hard boundary — ICP description,
volume cap, approval-gate on/off.

State plainly that this is a stub pending the future onboarding-intake
template, not the final binding-sheet design.

Confirm the fields satisfy dk0/drift-check.md's requirement (explicit
in-scope / out-of-scope / status, something real to diff against) before
calling it done.
```

## GPT prompts (Cursor / live build)

### GPT-1 — WP5: connector-class build

```
Build the Claude Project for the Prospect/Outreach Manager: a Gmail
connector for sending, and a Google Sheet tracking store for lead/message
state. Start from agents/prospect-outreach-manager/birth.md — read it and
its identity.md/plugin.md/binding-sheet.md in full before doing anything
else. Point the Project's own knowledge at that folder rather than pasting
file contents into chat, if the Project's connector setup allows it; if it
doesn't, treat the folder as what you re-fetch from whenever you need to
confirm something, not a one-time copy. Sourcing, enrichment, and
draft-generation logic live as Project instructions/skills built from those
files — don't reconstruct the job from memory. Add a Claude Code Routine
for scheduling only if the Project can't run unattended on its own — decide
this at build time, not before. No Supabase, no OpenRouter, unless this
build hits a real wall neither can clear.
```

### GPT-2 — WP4: gate/state wiring

```
Inside that same Claude Project — not as application code in the Jy-ops HQ
repo, which is markdown-only — implement the session gate and Halted logic
as real, executable checks: a pre-flight check before any send (Gmail
connector authenticated + tracking store reachable + bound identity matches
the binding sheet — all three, or refuse to proceed), and a hard
stop-and-notify on every escalation trigger listed in
agents/prospect-outreach-manager/identity.md (bounce, spam complaint,
unsubscribe request, ambiguous reply, conflicting contact data, anything
outside in-scope). No self-correction path anywhere in the build.
```

### GPT-3 — WP7: establishment / go-live

```
Run agents/prospect-outreach-manager/birth.md as written — that file is the
establishment script for this asset now, not an ad hoc process. Collect the
real binding-sheet values from the founder, write them into the canonical
instances/jyops-outreach.md first, then update the
agents/prospect-outreach-manager/binding-sheet.md mirror to match. Run the
gate check for real per birth.md's Phase 3. If it passes, that's the
founder's "bind": Bound → Operating, and the pipeline starts
sourcing/drafting against the real ICP; if the approval-gate is on, first
sends queue for review rather than going out unreviewed. If the gate fails
on anything, stop and state exactly what's missing — do not go live
half-configured.
```

## Instructions to GPT: representing this on Linear

- Create one Linear project/epic: "Prospect/Outreach Manager." Link it to this file (`packages/prospect-outreach-manager.md`) rather than copying the prompts into the epic description — this file is the spec; Linear tracks state, it doesn't hold a second copy of the spec.
- Create six tasks, one per row in the Distribution table above (WP3 and WP6 are one task, not two — WP6 has no separate build). Name them exactly as the row's deliverable (e.g. "WP1 — dk0/prospect-outreach-manager.md"), not a paraphrase, so the Linear task and the file it produces are recognizably the same thing.
- Set task dependencies matching the Sequence line: WP1 → WP2 → WP3 blocks WP5 → WP4, which blocks WP7.
- Assign WP1/WP2/WP3 to Claude Code, WP5/WP4/WP7 to GPT, per the Distribution table — don't reassign without relaying that back through the founder first, per `collaboration.md`'s handoff protocol.
- Do not mark a Linear task done when its file is drafted. Per `collaboration.md`, a task is done once the other side has verified the actual diff against source of truth — for WP1–WP3 that means Claude Code's own boundary-test pass; for WP4/WP5 it means the pre-flight gate actually blocks a bad send in a real test, not just reads correctly.
- Don't write a status onto a Linear task that reads as GPT (or Claude Code) certifying its own work as approved — the same rule that applied to `claude-code-proposal.md`'s status line applies here. Task state changes; founder approval and verification are two different, both-visible things.