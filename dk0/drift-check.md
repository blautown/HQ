# DK:0 — drift check

Read [`domain-knowledge-boundaries.md`](domain-knowledge-boundaries.md) first if you haven't.

This is not a work session. Do not do the DK:0 job while running this.

Purpose: turn the two self-audit questions from `domain-knowledge-boundaries.md` — *"what if I need to dismantle this?"* and *"am I operating within my own recorded boundaries?"* — into an actual check, not just a definition.

## Two ways to run it

**With file access** (a terminal session, or any agent given a real workspace): point it at this repo. Read the binding sheet for the instance, the DK:0 card the sheet names, and any bound plugin. Diff against what the operator reports the live seat is doing.

**Without file access** (pasted into a chat seat): ask the operator to paste the binding sheet and the relevant DK:0 / plugin text first. Do not proceed from memory.

Either way: this check reads **configuration**. It does not need, and should not be given, access to the live org's real data (Drive, CRM, MCP service) to run. If it asks for that, it has already drifted into being a second factory surface. Stop instead of asking.

---

## Prompt (paste or run this)

```
You are running a drift check. This is not a normal work session — do not perform the DK:0 job right now.

If you have file access: read the current binding sheet, the DK:0 card it names, and any bound plugin. If you do not have file access: ask the operator to paste those now. Do not proceed from memory.

1. RESTATE what you just read: asset, connector class, in-scope this week, out-of-scope, optional plugin (or none), status.

2. COMPARE that restatement against the binding sheet itself, line by line. Flag any mismatch, however small. A mismatch is a mismatch even if it looks like an improvement.

3. LIST anything done in recent sessions, or currently being asked, that falls outside the in-scope line. Do not soften this. A "helpful" expansion still counts as drift.

4. IF A PLUGIN IS ATTACHED: state exactly how it would be removed, and confirm removing it leaves the DK:0 asset exactly as generic as before. If you cannot describe that cleanly, say so — that is a graft, not a plugin, and it should not have shipped as one.

5. VERDICT — pick one, do not average them into "mostly fine":
   - CLEAN: restatement matches the sheet, nothing done outside scope, plugin (if any) dismantles cleanly.
   - DRIFTED: list the specific mismatches, out-of-scope actions, and any plugin that cannot be cleanly removed.

If DRIFTED: stop. Hand the mismatch list to the operator. Do not edit the binding sheet yourself, and do not "fix" the drift by rewriting your own scope. Only the operator updates the sheet.

Do not request access to the live org's real data to complete this check. If you think you need it, that request is itself a drift signal — say so instead of asking for the access.
```

## When to run it

On a cadence the operator chooses. This is a founder-run shelf, not a monitored system — there is no automatic trigger. Run it when a seat feels like it has expanded, before trusting a "quick fix" a live agent proposed on its own, or as a periodic spot-check.

## What this check needs to exist first

A binding sheet to diff against. If the instance only has a narrative note (no explicit in-scope/out-of-scope line, no status field), there is nothing to compare — write the binding sheet before running this.

## Not in this card

Live org data, credentials, or a running transcript. This card only checks configuration against configuration.
