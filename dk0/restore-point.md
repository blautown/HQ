# DK:0 — restore point

Read [`drift-check.md`](drift-check.md) first. This card is its missing other half: drift check only diagnoses ("if DRIFTED: stop, hand to operator") — it has no recovery step. A restore point is that recovery step.

Not the same word as "benchmark." JRBA is the benchmark (the proven instance). The founder's seat is the asset benchmark library. A restore point is neither of those — it is a dated, known-good snapshot of one bound project's configuration, taken so a bad edit or drift can be rolled back instead of rebuilt from memory.

## What gets snapshotted

Configuration only, same boundary as drift check:
- The project's custom instructions, verbatim
- The list of knowledge-base files and their current versions (the files themselves stay wherever they already live — Drive, the live org — this is a manifest, not a duplicate archive)
- The binding sheet as it stands that week

Not the live org's real data (Drive contents, CRM records, MCP payloads). If a restore point starts pulling in real business data, it has become a second factory surface — stop.

## Where it lives

Not this repo, and not inside the live client project either — a restore point that lives only in the thing it's meant to protect is not a backup. Keep it in the founder's own private archive (dated folder, per instance), outside both the client org and this HQ repo. This repo tracks the *practice*, not the snapshots themselves — same rule as `instances/jrba.md`: no logins, no tenant URLs, no client data in HQ markdown.

## Cadence

Weekly, chained to drift check, not standalone:

1. Run [`drift-check.md`](drift-check.md).
2. If **CLEAN** — take the restore point now. A clean state is the only state worth saving.
3. If **DRIFTED** — do not snapshot. Fix or accept the drift with the operator first, re-run drift check, then snapshot the result.

This means every restore point is, by construction, a verified-clean state — never a snapshot of something already broken.

## Restore procedure

1. Confirm the current state is actually broken (bad edit, unwanted drift, accidental deletion) — do not restore over something merely unfamiliar.
2. Paste the restore point's custom instructions back into the project, replacing the current ones.
3. Re-sync the knowledge-base file list against the manifest; re-add anything missing from the live org's own copies.
4. Run drift check again. It must come back CLEAN against the restored binding sheet before calling the restore complete.
5. Log the restore (date, what broke, which restore point was used) — this is what tells you if a client's seat needs tighter view-only enforcement or a behaviour-brief refresh, not just a rollback.

## Not in this card

Live org data, credentials, or a running transcript — identical boundary to drift check. This card only snapshots and restores configuration.
