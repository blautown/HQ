# DK:1 plugin — NDIS audit-readiness / core-module & PBS register

Read [`../dk0/domain-knowledge-boundaries.md`](../dk0/domain-knowledge-boundaries.md)
first if you haven't.

Clips onto [`../dk0/documentation-manager.md`](../dk0/documentation-manager.md).
Does not restate its process rules — session gate, subtree lock, one-
request-is-one-pass, verify-before-surfacing, and the tool-limitation
handoff pattern all stay on that card; this plugin only adds domain
content on top of them.

Sourced from [`ndis-auditing.md`](ndis-auditing.md), the org-stripped
domain specialty this plugin turns into an attachable form. Org-
stripped: no client data, no participant files, no live register
contents, no internal document-numbering scheme belonging to any one
provider.

## What this adds

An NDIS-registered provider's document manager needs to recognise the
*shape* of what an NDIS Practice Standards audit expects on file, so it
can retrieve, pre-fill, and file correctly without inventing the
framework itself:

- **Category structure.** A provider's audit-readiness documentation
  is generally organised across: organisational policies (governance,
  ethics, conflicts of interest, employment basics); NDIS Practice
  Standards policies (person-centred planning, privacy and dignity,
  informed choice, abuse/neglect response, risk management, quality
  management, incident management, continuity of supports); if the
  provider delivers specialist behaviour support, a further module
  covering restrictive practices, functional behaviour assessments,
  behaviour support plan implementation/monitoring/review, and
  reportable incidents involving restrictive practices; forms/
  checklists (incident investigation, intake, service agreement,
  meeting agenda); registers; and procedure/training documents. Each
  item in this structure typically carries its own status (current,
  needs update, missing, superseded, retired) — that status tracking
  is itself part of what "audit ready" means, not a one-time checklist.
- **Registers are organisation-wide by design.** A provider's registers
  (continuous improvement, feedback and complaints, incidents,
  internal audit, conflicts of interest) are each one file per
  register type, covering the whole practice — never a per-participant
  copy. A per-participant file that looks like a register is a
  duplicate or leftover artifact, not the real thing, and should never
  be treated as satisfying the organisation-wide requirement.
- **Incident investigation is a two-part artifact.** A per-incident
  report (who, what, when, immediate action, signature) is distinct
  from the incident register (a running log entry). Filing the report
  doesn't itself satisfy the register requirement — both need to
  happen, as two separate steps.
- **A document-control register is the yardstick, not something to
  regenerate.** Whatever master checklist the provider maintains for
  "is our documentation current and complete" is the reference frame
  a Documentation Manager checks against — it doesn't invent its own
  competing view of what's required.

## Cited domain content

This plugin's category structure and the organisation-wide-register
rule are drawn from a real NDIS-registered provider's own live audit-
preparation documentation (JRBA's document control register and
sibling registers), cross-referenced against each other for internal
consistency, not against the NDIS Commission's own published Practice
Standards text directly in this session. Treat the category list above
as a well-evidenced real-world shape, not a verified transcription of
the regulation itself — re-confirm against the NDIS Practice Standards
and Quality Indicators (and, where relevant, the NDIS (Provider
Registration and Practice Standards) Rules 2018) before this plugin is
relied on for an actual compliance determination, rather than as
general orientation for a document manager's filing/retrieval work.

## Not in this card

Any provider's actual document-numbering scheme, folder structure,
register contents, participant data, or audit findings. No statute
text is reproduced here — if a specific regulatory citation is needed
for a real compliance question, that is a separate, currently-unheld
citation; state that it's missing rather than inventing it.

## Plugin self-check

- **Detach:** removing this file leaves `dk0/documentation-manager.md`
  exactly as generic as before — no NDIS category structure, register
  rule, or citation lives on that card.
- **Audit:** this plugin's own recorded scope is the category structure,
  the organisation-wide-register rule, and the incident-artifact split
  above, each traced to the cited source. A drift check should confirm
  no other NDIS content (specific register contents, a named provider's
  numbering scheme, actual audit findings) has been added here without
  a matching citation.
