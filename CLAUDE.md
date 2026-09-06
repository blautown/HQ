# CLAUDE.md — operating contract for Jy-ops HQ

Read [`workspace.md`](workspace.md) and [`map.md`](map.md) before planning or architecture work. This file turns that charter into working instructions. If it conflicts with either source, the source wins and this file must be updated.

## Workspace role

Jy-ops HQ is both the JYOps asset library and the main operational board. Claude Code works here through the IDE and terminal for planning, development, packaging, deployment preparation, client coordination, and verification.

The live client system, client-owned data, public website runtime, and campaign execution remain downstream surfaces. HQ coordinates them without becoming a copy of them.

## Asset model

The HQ library contains three separate box-asset classes:

- **Identities** — domain managers, domain assistants, and domain record-keepers.
- **Operational guidelines** — reusable role instructions without project-specific context.
- **Domain knowledge plugins** — domain knowledge linked directly to the plugin that uses it.

Domain knowledge is the direct source for a plugin. It is not a filter applied to an identity.

Before deployment, these remain box assets plus domain knowledge. They are not yet agents. A DK:1 agent is created and benchmarked only when the selected identity, operational guidelines, and plugin combine with project-specific context in the founder's admin seat, inside whichever workspace the deployment serves (a client's system, or the founder's own business).

## Hard boundaries

- Markdown only. Do not add application code here.
- Never write credentials, tokens, API keys, tenant or Drive URLs/IDs, emails, phone numbers, participant/client/staff identifiers, live CRM records, live document contents, raw client transcripts, or private restore-point snapshots into this repo.
- Identities and operational guidelines must remain reusable. Project facts and specialty-specific rules belong in project context or the domain knowledge source/plugin.
- Instance files stay org-stripped. They may describe scope, actor, connector class, and boundaries, but not live access or personal data.
- Do not invent governing text. If a source rule is not held here, state that it is missing.
- Do not treat a draft, box asset, or untested plugin as a deployed or benchmarked agent.

## Execution processes

### Asset library process

Keep this separate from deployment:

```text
Need
  → identity
  → reusable operational guidelines
  → domain knowledge source
  → domain knowledge plugin
  → selected box-asset package
```

No client identity, project context, live record, or deployment workaround may flow backward into the reusable package by default.

### Deployment process

```text
Deployment need
  → project recon/context
  → selected box-asset package
  → establishment
  → role-specific context ROM
  → founder's admin seat, in the deployment's workspace
  → shared user access
  → deployed DK:1 agent benchmark
```

Use [`dk0/establishment.md`](dk0/establishment.md) for recon then bind. Do not operate between those states.

### Market/public process

```text
HQ offer / claims
  → Grok campaign execution
  → personal-ops / Cloudflare
  → landing pages and live support chat
```

## How Claude Code should work

### Before editing

1. Read `workspace.md`, `map.md`, the relevant source card, and `TASKS.md`.
2. Classify the request as asset library, operational board, client deployment, instance documentation, benchmark evidence, or market/public coordination.
3. Identify the affected layer: identity, operational guidelines, domain knowledge/plugin, project context, deployment, or output.
4. State the intended files, destination, and verification condition.
5. Ask before editing if the requested layer or destination is materially ambiguous.

### During editing

- Prefer small, reviewable edits to broad cleanup.
- Link to existing documents instead of duplicating them.
- Keep identity, guidelines, plugin, and project context separate.
- Preserve the ordering in `TASKS.md`.
- Do not mark work proven because it merely reads well.
- Keep `CLAUDE.md` aligned with the charter; it cannot silently override it.

### After editing

Report:

- files changed;
- process and layer affected;
- verification performed;
- assumptions and unresolved `[confirm]` items;
- downstream destination; and
- next handoff.

## Verification contract

Verification is layered. Passing one level does not imply passing the next.

### 1. Repository integrity

After substantive edits:

- run the linter on changed files;
- run `git diff --check`;
- confirm referenced files and links exist;
- inspect the diff for secrets, client data, and accidental scope leakage.

### 2. Box-asset integrity

For an identity, guideline, or plugin:

- scope and destination are written;
- project-specific facts are absent;
- domain rules are in the domain source/plugin, not the reusable identity/guideline;
- a plugin detaches without damaging the identity or operational guidelines;
- the plugin can state and check its own recorded boundary.

### 3. Deployment integrity

Before calling a deployment ready:

- the binding sheet is complete enough to check;
- project context is distinct from HQ assets;
- the JYOps admin seat is identified;
- client access has the approved permission tier;
- connector and identity checks pass;
- the deployed ROM is the actual combination being used.

### 4. DK:1 agent benchmark

Use [`benchmark.md`](benchmark.md):

1. configuration comparison;
2. boundary tests;
3. box-asset QA before deployment;
4. one supervised real task after deployment;
5. repeatability and handoff.

The first real task in the deployment workspace is the first benchmark evidence for the DK:1 agent library. Record only sanitized task class, expected result, outcome, correction, and disposition in HQ.

Use `PASS`, `PASS WITH CORRECTION`, `FAIL`, or `BLOCKED`. A useful output does not excuse a boundary failure.

### 5. Drift and recovery

If deployed behaviour or configuration differs from its binding:

1. stop treating it as proven;
2. run [`dk0/drift-check.md`](dk0/drift-check.md);
3. route the failure to asset, plugin, binding, connector, or operator;
4. do not rewrite the reusable asset to hide project drift;
5. after `CLEAN`, take a private restore point using [`dk0/restore-point.md`](dk0/restore-point.md).

Drift check diagnoses. It does not repair or redefine scope.

## Definition of done

- **HQ asset:** reusable, scoped, source-linked, and boundary-tested.
- **Operational item:** owner, action, destination, dependency, and verification condition recorded.
- **Client deployment:** package, project context, ROM, JYOps admin seat, sharing, and connector checks recorded or explicitly blocked.
- **Benchmarked agent:** deployed agent has passed the required benchmark lanes with sanitized evidence and no unresolved boundary failure.
- **Public claim:** defined in `offer.md`, backed by a process, bounded by exclusions, and recorded in `claims.md`.

## Navigation

- [`workspace.md`](workspace.md) — workspace charter
- [`map.md`](map.md) — architecture and separated processes
- [`TASKS.md`](TASKS.md) — ordered work
- [`claude-code-proposal.md`](claude-code-proposal.md) — GPT's execution/verification proposal (adopted)
- [`collaboration.md`](collaboration.md) — Claude Code's response: role split and handoff protocol with GPT
- [`benchmark.md`](benchmark.md) — deployment benchmark
- [`grokbot.md`](grokbot.md) — Grokbot landing page, live chat, and Google Ads boundary
- [`dk0/domain-knowledge-boundaries.md`](dk0/domain-knowledge-boundaries.md) — asset/domain/context boundary
- [`dk0/establishment.md`](dk0/establishment.md) — recon then bind
- [`dk0/drift-check.md`](dk0/drift-check.md) — configuration drift check
- [`dk0/restore-point.md`](dk0/restore-point.md) — recovery practice
