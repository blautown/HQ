# Proposal to Claude Code: execution and verification in Jy-ops HQ

**Status:** Adopted into [`CLAUDE.md`](CLAUDE.md) by founder decision. This file remains the rationale and detailed proposal record.

## 1. Mission of this workspace

Jy-ops HQ is both:

- the JYOps asset library; and
- the main operational board for planning, packaging, development, deployment preparation, and client coordination.

Claude Code works in this repository through the IDE and terminal. It maintains the reusable founder layer and coordinates work that will execute elsewhere.

The workspace is not the live client system. It must not become a copy of client data, a secret store, or an unreviewed transcript dump.

## 2. The asset model Claude must preserve

The HQ asset library has three separate box-asset classes:

1. **Identities** — domain managers, domain assistants, and domain record-keepers.
2. **Operational guidelines** — reusable instructions for those roles, without project-specific context.
3. **Domain knowledge plugins** — domain knowledge linked directly to the plugin that uses it.

Domain knowledge is a direct source for a plugin. It is not a filter applied to the identity.

Before deployment, these remain separate box assets plus domain knowledge. They are not yet agents.

An agent is created when the selected identity, operational guidelines, and plugin combine with project-specific context in a client workspace. That deployed agent, in the JYOps admin seat, is what benchmarks the DK:1 agent library.

## 3. Two execution processes

Claude must keep these processes separate.

### A. Asset library process

This happens in HQ:

```text
Identify need
  → define or select identity
  → write reusable operational guidelines
  → source domain knowledge
  → build domain knowledge plugin
  → package the box assets
```

This process must not absorb a client's identity, project facts, live records, or deployment-specific workarounds.

### B. Client deployment process

This is coordinated in HQ and executed in the client's system:

```text
Client need
  → project recon and context
  → select HQ box-asset package
  → combine at establishment
  → create role-specific context ROM
  → deploy to JYOps admin seat
  → share with client user accounts
  → benchmark the deployed agent
```

The project context belongs to the deployment. It must not silently flow backward into the reusable asset library.

Marketing and the public website are a separate operating surface:

```text
HQ offer / claims
  → Grok campaign execution
  → personal-ops / Cloudflare
  → landing pages and live support chat
```

## 4. How Claude should execute work

### Before changing files

1. Read `workspace.md`, `map.md`, and the relevant source card.
2. Check `TASKS.md` for ordering and existing work.
3. Classify the request:
   - asset library;
   - operational board;
   - client deployment coordination;
   - instance documentation;
   - benchmark evidence; or
   - public/commercial coordination.
4. State the intended files and destination.
5. Identify whether the change is reusable HQ knowledge or project-specific context.

If the classification is unclear or the change would materially alter the architecture, stop and ask the founder before editing.

### During changes

- Prefer a small, reviewable edit over broad cleanup.
- Preserve the separation between identity, operational guidelines, plugin, and project context.
- Link to existing documents instead of duplicating them.
- Treat `instances/` as safe binding descriptions, not as a place for live data.
- Never invent missing client facts, governing text, credentials, identifiers, or operational results.
- Do not mark an agent, plugin, claim, or deployment as proven merely because it has been drafted.
- Keep `CLAUDE.md` aligned with approved workspace documentation; do not use it to silently override the charter.

### After changes

Report:

- files changed;
- the process and layer affected;
- what was verified;
- what remains unverified;
- any assumptions or `[confirm]` items; and
- the next handoff or destination.

## 5. Verification contract

Verification has multiple levels. Passing one level does not imply passing the next.

### Level 1 — repository integrity

After every substantive edit:

- run the editor linter on changed files;
- run `git diff --check`;
- confirm links and filenames used by the change exist;
- inspect the final diff for accidental secrets or scope leakage.

### Level 2 — asset integrity

For an identity, operational guideline, or plugin:

- confirm its scope and destination are written;
- confirm project-specific facts have not entered a reusable asset;
- check the DK:0 / positive-DK boundary;
- confirm a plugin's detach path leaves the underlying identity and guidelines intact;
- confirm the plugin can state and check its own recorded boundaries.

### Level 3 — deployment integrity

Before calling a deployed agent ready:

- the binding sheet is complete enough to check;
- project context is separated from HQ assets;
- the JYOps admin seat is identified in the client system;
- client user access is at the approved permission tier;
- the connector and identity checks pass;
- the role-specific ROM is the actual combination being deployed.

Use `dk0/establishment.md` for recon then bind. Do not operate between those states.

### Level 4 — agent benchmark

Use [`benchmark.md`](benchmark.md):

1. configuration comparison;
2. boundary tests;
3. box-asset QA before deployment;
4. one supervised real task after deployment;
5. repeatability and handoff.

The first real-task result in the client workspace is the first benchmark evidence for the DK:1 agent. Record only sanitized task class, expected result, outcome, correction, and disposition in HQ.

Use these dispositions:

- `PASS`;
- `PASS WITH CORRECTION`;
- `FAIL`; or
- `BLOCKED`.

A useful output does not excuse a boundary failure.

### Level 5 — drift and recovery

If the deployed actor's behaviour or configuration differs from its binding:

1. stop treating it as proven;
2. run `dk0/drift-check.md`;
3. route the failure to asset, plugin, binding, connector, or operator;
4. do not rewrite the asset to hide project drift;
5. after a `CLEAN` result, take a private restore point using `dk0/restore-point.md`.

Drift check diagnoses. It does not repair or redefine scope.

## 6. Verification evidence boundaries

Claude may keep in HQ:

- plans and decisions;
- reusable asset text;
- safe instance crosswalks;
- synthetic fixtures;
- sanitized benchmark outcomes;
- failure routing; and
- links to downstream destinations.

Claude must not write into HQ:

- passwords, tokens, API keys, or logins;
- tenant URLs, Drive IDs, or folder IDs;
- emails, phone numbers, participant, client, or staff identifiers;
- live document contents, CRM records, or claim payloads;
- raw client transcripts; or
- private restore-point snapshots.

The live client system holds live work. The founder's private archive holds recovery snapshots. The separate website repository and deployment hold public implementation. HQ holds the reusable pattern, operational decision, and sanitized verification record.

## 7. Definition of done for Claude

Claude should not report “done” until the relevant condition is true:

### HQ asset

The asset is scoped, reusable, linked to its source, and tested for boundary/detach integrity.

### Operational board item

The owner, next action, destination, dependency, and verification condition are recorded.

### Client deployment

The package, project context, ROM, JYOps admin seat, client sharing, and connector checks are recorded or explicitly marked blocked.

### Benchmarked agent

The deployed agent has passed the benchmark lanes required for the claim being made, with sanitized evidence and no unresolved boundary failure.

### Public claim

The term is defined in `offer.md`, the mechanism exists, exclusions are written, and `claims.md` records the current status.

## 8. Adoption result

The execution and verification contract has been folded into [`CLAUDE.md`](CLAUDE.md). The detailed benchmark procedure remains in [`benchmark.md`](benchmark.md), the workspace boundary remains in [`workspace.md`](workspace.md), and the architecture remains in [`map.md`](map.md).
