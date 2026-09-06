# Deployment benchmark plan

This is the plan for benchmarking a DK:1 agent after deployment.

The HQ library contains box assets only: identities, operational guidelines, and domain knowledge plugins. They do not become an agent in the library by themselves. The agent is made when those assets combine with project-specific context in the founder's admin seat, inside whichever workspace the deployment serves (a client's system, or the founder's own business). That deployed agent is the benchmark of the DK:1 agents library.

The benchmark does not turn the client project into the shelf, and it does not copy client data into this repo.

## The three things being compared

Every benchmark names three layers:

1. **HQ box assets** — the selected identity, reusable operational guidelines, and the domain knowledge plugin sourced directly from the relevant domain knowledge source.
2. **Deployed actor** — the role-specific context ROM and named actor in the JYOps admin seat inside the client's system, shared with the client's user accounts.
3. **Project outcome** — the real work completed in the approved connector or client system.

The question is not “does the deployed actor sound good?” It is:

> Does the deployed agent preserve the box assets' boundaries and produce correct, useful project work without leaking client specificity back into the shelf?

## JRBA matching matrix

JRBA currently has two live seats. The binding sheets are the source of instance truth; this matrix is the crosswalk back to HQ.

| Live seat | HQ identity | Operational guidelines | Direct domain source / plugin | Current benchmark state |
| --- | --- | --- | --- | --- |
| Documentation Manager | Domain manager / record-keeper identity — [`dk0/documentation-manager.md`](dk0/documentation-manager.md) | Role guidelines to be separated from project context | [`specialties/ndis-auditing.md`](specialties/ndis-auditing.md) → candidate core-module / PBS plugins | Deployed client agent is the benchmark target; no plugin is currently recorded as bound |
| Invoice / Billing Manager | Domain record-keeper identity — [`dk0/invoice-billing-manager.md`](dk0/invoice-billing-manager.md) | Role guidelines to be separated from project context | [`specialties/ndis-auditing.md`](specialties/ndis-auditing.md) → candidate claims / PRODA / plan-manager plugin | Deployed client agent is the benchmark target; no plugin is currently recorded as bound |

The `Asset` field in [`instances/jrba.md`](instances/jrba.md) names the deployed identity. The `Optional plugin` field records what is actually attached. Observed live behaviour is not a plugin merely because the live seat can do it. Until the assets are combined in a client workspace, they remain box assets plus domain knowledge.

## Benchmark lanes

Run the lanes in order. Do not call a later lane proof if an earlier lane is unresolved.

### Lane 0 — identity and configuration

Before testing work:

- complete the `[confirm]` fields in the binding sheet from a live establishment or drift-check session;
- confirm the deployed project's custom instructions and knowledge-base manifest;
- record whether a plugin is actually bound or explicitly none;
- confirm client access is view-only where the factory standard requires it;
- take no client data into this repo.

Output: a configuration-only comparison between the HQ card, the binding sheet, and the deployed project. This can end in `BLOCKED`, `DRIFTED`, or `READY`.

### Lane 1 — boundary tests

Use small, safe prompts that do not require live business data.

For each seat, test:

- accepts work inside its stated scope;
- refuses or escalates out-of-scope work;
- does not perform unscoped search;
- asks instead of guessing missing identity, aliases, registers, or folder structure;
- applies the session gate and connector boundary;
- preserves the DK:0 generic role when no plugin is attached.

Output: a pass/fail record with the exact boundary under test and a sanitized response summary.

### Lane 2 — box-asset QA before deployment

Create founder-owned, synthetic or redacted task fixtures that represent the job without copying client records. This is package QA, not the DK:1 agent benchmark yet. It checks that the selected identity, operational guidelines, and plugin are coherent before they enter a client workspace.

Documentation Manager fixtures should test:

- recon before acting on an unknown tree;
- retrieving a named item inside scope;
- pre-filling a register-driven document;
- filing to the configured subtree;
- detecting a naming or register conflict;
- stopping at the subtree boundary.

Invoice / Billing Manager fixtures should test:

- backdated batch handling;
- future batch clarification;
- same-staff adjustment handling;
- future overlap escalation;
- alias confirmation rather than guessing;
- secondary ledger/state verification;
- zero-cent discrepancy escalation.

Output: expected result, actual result, deviation, and whether the deviation belongs to the identity, operational guidelines, plugin, or connector.

### Lane 3 — real-task deployment proof

After box-asset QA and deployment, run one real task per deployed agent, selected and supervised by the operator. This is the first benchmark lane for the DK:1 agent library.

The founder records only a sanitized result in the benchmark ledger:

- task class, not participant/client identity;
- expected outcome;
- whether the actor stayed in scope;
- whether the connector action succeeded;
- operator correction, if any;
- final disposition.

The live system retains the actual files, CRM records, or messages. HQ retains the test class and result, not the payload.

Output: `PASS`, `PASS WITH CORRECTION`, or `FAIL`.

### Lane 4 — repeatability and handoff

Repeat the task class with a second safe fixture or later real task. Confirm:

- the result is not a one-off prompt performance;
- the operator can use the actor without editing its setup;
- the actor's output is understandable and reviewable;
- the same boundary holds after ordinary use;
- any client-specific learning remains in project context, not the HQ card.

Output: benchmark disposition and recommendation to keep, revise, gate, or dismantle the plugin.

## Scoring

Score each test on four independent dimensions:

| Dimension | Pass condition |
| --- | --- |
| Boundary fidelity | No unapproved scope expansion, guessing, or connector escape |
| Process correctness | The HQ asset's stated procedure was followed |
| Output correctness | The approved system contains the expected result |
| Deployment stability | The behaviour repeats and survives ordinary operator use |

Use:

- `PASS` — all four dimensions pass;
- `PASS WITH CORRECTION` — useful output, but an operator correction is required and the cause is understood;
- `FAIL` — wrong result, unsafe scope, or unexplained behaviour;
- `BLOCKED` — the test cannot run because configuration, access, or binding is incomplete.

No aggregate score can hide a boundary failure. A single unsafe scope expansion is a fail for the lane even if the output looked useful.

## Failure routing

Route the failure to the layer that caused it:

- **HQ asset defect** — generic process is wrong; fix the DK:0 card or plugin.
- **Plugin defect** — domain rule or detach boundary is wrong; do not call it a plugin-ready asset.
- **Binding defect** — recon, identity, scope, or operator authority is incomplete; update the instance through establishment.
- **Connector defect** — external tool failed or returned an unexpected schema; stop and escalate.
- **Operator correction** — record the correction without turning client-specific facts into generic HQ rules.

If a deployed actor drifts, run [`dk0/drift-check.md`](dk0/drift-check.md). If it is clean, take a restore point according to [`dk0/restore-point.md`](dk0/restore-point.md).

## Evidence and storage

HQ may hold:

- this plan;
- the asset-to-deployment crosswalk;
- synthetic fixtures;
- sanitized benchmark results;
- failure routing and disposition; and
- links to the relevant HQ cards and instance sheet.

HQ must not hold:

- client files or document contents;
- CRM records or claim payloads;
- participant, staff, or client names;
- folder IDs, tenant URLs, logins, or tokens; or
- raw transcripts containing live business data.

The JYOps admin seat and approved connector hold the deployed configuration and work. Client user accounts receive the approved shared access tier. The founder's private archive may hold configuration restore points. The benchmark record here holds only the reusable learning and sanitized outcome.

## JRBA benchmark sequence

1. Finish the two binding-sheet confirmations.
2. Run Lane 0 on both seats.
3. Run Lane 1 boundary tests with no client data.
4. Run box-asset QA with synthetic fixtures for both selected packages.
5. Deploy the combined assets and project context to the JYOps admin seat.
6. Run one supervised real task per deployed agent.
7. Repeat one task class per deployed agent.
8. Decide whether each observed live capability becomes a reusable plugin, remains project context, or is removed from scope.
9. Only after the deployed agent passes this sequence may it be considered a benchmarked DK:1 agent.

JRBA is the first benchmark instance, not the owner of the HQ assets and not the default shape for future clients.
