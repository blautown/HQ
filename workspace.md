# Jy-ops HQ workspace charter

## What this workspace is

Jy-ops is both:

1. the founder's reusable asset shelf; and
2. the main operational board for JYOps as clients arrive.

It is not a passive archive. Planning, packaging, development, deployment preparation, client onboarding design, and operational decisions happen here.

It is the place where the founder:

- defines reusable operating assets;
- separates identity, operational guidelines, domain knowledge, and project context;
- builds and packages identities, operational guidelines, and domain knowledge plugins;
- records the rules for establishment, drift, restore, and handoff;
- plans and sequences incoming client work;
- packages proven assets for a client;
- develops and tests the operating system;
- prepares and coordinates deployments;
- turns proven assets into repeatable project bindings; and
- keeps the commercial and public claims aligned with what the operation can actually deliver.

This workspace is the **asset shelf and operational control plane**. It is not itself a client-owned project, live service database, or public website.

The durable question for every document is:

> Is this reusable founder-level knowledge, a bounded domain asset, a project binding, or project output?

If it is none of those, it probably does not belong here.

## What belongs here

### Founder assets

The HQ asset library contains three separate classes:

- **Identities** — domain managers, domain assistants, and domain record-keepers;
- **Operational guidelines** — reusable role instructions without project-specific context; and
- **Domain knowledge plugins** — domain knowledge linked directly to the plugin that uses it.

These remain box assets plus domain knowledge until they are combined with project-specific context in the founder's admin seat, inside whichever workspace the deployment serves (a client's system, or the founder's own business).

The deployed combination is what benchmarks the DK:1 agents library. A box asset in HQ is not yet a deployed agent.

Reusable operating knowledge belongs on the shelf:

- identity definitions;
- operational guidelines;
- domain knowledge sources and plugins;
- establishment and drift procedures;
- restore-point practice;
- commercial onboarding and access rules;
- offer definitions and claim traceability; and
- maps, decisions, and the ordered work list.

Founder assets must be generic where they claim to be generic. A DK:0 card cannot acquire a specialty, client, login, folder ID, participant, staff member, or live register by accident.

### Benchmark material

The benchmark is created in the deployment, not in the box-asset library. A selected identity, its operational guidelines, and its domain knowledge plugin combine with project-specific context in the founder's own admin seat — always that seat, whether the workspace it sits inside belongs to a served client or to the founder's own business.

That deployed agent is then tested against real, supervised work. The benchmark record returns only sanitized learning to HQ; live data stays in the deployment's own workspace.

Named projects and instances are test cases for the library. They are not the owner of the reusable assets and do not define the workspace by themselves.

### Active operations

Operational board work belongs here when it coordinates JYOps delivery:

- client discovery and qualification;
- planning and prioritisation;
- asset selection and packaging;
- deployment preparation and gates;
- development of HQ assets and tooling;
- handoff and support design;
- campaign-to-offer alignment; and
- decisions about what is ready, gated, or not approved.

The board may point to live systems without copying their sensitive contents into this repo. The distinction is **coordination here, execution in the approved destination**.

### Safe instance documentation

This repo may contain an org-stripped instance binding sheet: enough to describe the actor, scope, connector class, and operating boundary without exposing live access or business data.

It must not contain:

- credentials, tokens, or logins;
- tenant URLs or folder IDs;
- participant, client, or staff identifiers;
- live CRM records or document contents; or
- private restore-point snapshots.

## What does not belong here

### Live project execution

The actual work for an organisation ends up in that organisation's bound project, connector, and approved systems. Examples include:

- files in the configured document-store subtree;
- billing and recordkeeping actions in the live CRM;
- the client's Claude Team projects;
- the live organisation's binding and operating records; and
- the final output produced for the organisation.

This repo plans and governs those systems. It is not a mirror of their live data.

### Private recovery material

Restore points contain configuration snapshots for recovery. They belong in the founder's private archive, outside this repo and outside the client organisation. This repo documents the restore-point practice, not the snapshots.

### Public shopfront implementation

The public website and its Worker belong in the separate `jyoperatives/personal-ops` repository. This workspace plans and directs that work, supplies the definitions and claim checks, and may prepare deployment changes; the website repository and Cloudflare deployment contain the implementation and public runtime.

The shopfront is a separate commercial surface. It must not expose this workspace's internal architecture, JRBA context, binding sheets, or factory prompts.

## Operating surfaces

JYOps currently operates across three connected surfaces:

### 1. Jy-ops HQ repository

This is the main board and asset shelf. Claude operates in this repository through the IDE and terminal. Planning, packaging, development, deployment preparation, documentation, and operational decisions are recorded here.

### 2. Grok campaign bots

Grok bots running on the founder's phone handle the active marketing and advertising campaign, operate the landing page's live support chat, and make/maintain required landing-page edits. See [`grokbot.md`](grokbot.md). They are an execution and notification surface, not the source of truth for JYOps architecture, offer definitions, client bindings, or deployment state.

Campaign work must point back to the relevant HQ offer and claims definitions. Marketing activity does not by itself make a capability real or a claim backed.

### 3. Website and live support

The landing pages and live support chat run on the separate website stack. That stack is the public and customer-facing execution surface. It receives approved definitions and deployment changes from HQ; it does not replace HQ as the operational board.

## Where work goes next

The asset and deployment lifecycles are separate:

```text
Asset lifecycle:
HQ plan → develop → package → benchmark → proven JYOps package

Deployment lifecycle:
deployment need → project recon/context → proven package
  → establish → ROM → founder's admin seat
  → shared access → deployment workspace/output
```

The operational board coordinates both lifecycles, but the client context does not flow backward into the reusable asset by default.

The public/commercial path is separate:

```text
HQ definition or campaign decision
  → claims ledger and offer check
  → Grok campaign execution and/or approved shopfront copy
  → separate website repository and deployment
  → landing page and live support chat
```

The work ends at different places depending on its type:

| Work type | Ends up in |
| --- | --- |
| Reusable process or architecture | This repo |
| Planning, packaging, development, and deployment coordination | This repo and its operational board |
| DK:0 asset or DK:1 plugin | This repo, then a controlled founder benchmark |
| Project-specific identity and scope | A safe instance binding and the live project |
| Client files, records, or claims | The client's approved systems |
| Configuration recovery snapshot | Founder private archive |
| Marketing and advertising campaign execution | Grok bots on the founder's phone, directed by HQ definitions |
| Public sales copy and web behaviour | `jyoperatives/personal-ops` and its deployment |
| Landing pages and live support chat | Website runtime / Cloudflare deployment |
| Commercial delivery | Client-owned Claude Team and connected systems |

## What “done” means here

An HQ item is done when its boundary, operational owner, destination, and handoff are explicit, not merely when a document exists.

For a reusable asset, done means:

1. its scope is written;
2. its DK:0 / DK:1 boundary is clear;
3. its inputs and outputs are known;
4. it can be established without guessing;
5. it can be checked for drift;
6. it can be detached or restored safely where applicable; and
7. its downstream project destination is named.

For a public claim, done means:

1. the words have a defined meaning;
2. a real process backs the meaning;
3. exclusions and failure conditions are written; and
4. `claims.md` records whether the claim is backed, partial, or unpublished.

For a bound project, done means the real operator can use the actor in the approved system, while HQ retains only the safe reusable pattern and non-sensitive binding description.

## Navigation

- [`README.md`](README.md) — short entry point
- [`map.md`](map.md) — architecture and flow
- [`TASKS.md`](TASKS.md) — ordered work
- [`dk0/domain-knowledge-boundaries.md`](dk0/domain-knowledge-boundaries.md) — DK:0 / DK:1 boundary
- [`dk0/establishment.md`](dk0/establishment.md) — recon then bind
- [`factory.md`](factory.md) — commercial onboarding and handoff
- [`offer.md`](offer.md) — shopfront word meanings
- [`claims.md`](claims.md) — public-claim traceability
- [`grokbot.md`](grokbot.md) — Grokbot operating boundary
- [`instances/`](instances/) — safe project binding notes
- [`packages/`](packages/) — verified work-package breakdowns, agent prompts, and Linear-representation instructions for new assets
- [`agents/`](agents/) — one dedicated folder per deployed agent, holding a live-mirror set of its box assets and binding sheet plus a `birth.md` onboarding script; this is the one named location that agent points itself at, not a chat-pasted snapshot
