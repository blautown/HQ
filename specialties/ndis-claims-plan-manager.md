# DK:1 plugin — NDIS claims, bulk payment requests, and the plan-manager split

Read [`../dk0/domain-knowledge-boundaries.md`](../dk0/domain-knowledge-boundaries.md)
first if you haven't.

Clips onto [`../dk0/invoice-billing-manager.md`](../dk0/invoice-billing-manager.md).
Does not restate its process rules — CRM-as-billing-not-contacts, the
backdated/future publish-notify defaults, the "adjustment not trim"
rule, and the alias-file/distinct-namesake gotchas all stay on that
card; this plugin only adds domain content on top of them.

Sourced from [`ndis-auditing.md`](ndis-auditing.md)'s adjacent claims/
billing territory, drafted from a real provider's live operational
experience rather than a direct read of the scheme's own portal
documentation this session. Org-stripped: no client data, no
participant NDIS numbers, no live claim files, no provider registration
number or ABN.

## What this adds

The vocabulary and mechanics an Invoice/Billing Manager needs to
recognise a bulk agency-managed claim correctly, distinct from
invoicing a plan manager directly:

- **Three funding-management types.** A participant's supports can be
  plan-managed (invoiced to a plan manager), agency-managed/NDIA-
  managed (claimed directly against the participant's plan via the
  scheme's own bulk-claim mechanism), or self-managed (out of scope for
  this plugin without separate instruction). A single participant can
  have different management types for different support categories —
  never assume one management type covers everything for a given
  participant.
- **The bulk payment-request CSV.** Agency-managed claims are commonly
  submitted as a single CSV covering many claims across many
  participants/service bookings in one file, rather than one request
  per booking. Real, portal-confirmed columns include: a provider
  registration number; the participant's NDIS number; support-delivery
  start/end dates; a support item code from the current price catalogue;
  an optional claim reference; a quantity or an hours figure (mutually
  exclusive, depending on the item type); a unit price; a GST code
  (most NDIS supports are GST-free); several fields that are
  legitimately blank on a standard, non-cancellation claim; and the
  provider's ABN. Trust a provider's own real, historically-submitted
  header over a generic reference spec if the two ever disagree on a
  column name.
- **Submission mechanics.** Must be a comma-delimited `.csv`; filename
  length is capped short; there's a per-file row cap; no stray rows or
  characters outside the actual claim data. Rows come back success or
  error individually after upload. A rejected request can't be edited
  in place — a correction becomes a brand-new request under a new
  filename, never a re-upload of the original file. Where a claimed
  unit price exceeds the scheme's price-guide cap for that item/region,
  the system pays only up to the cap and flags the line as capped in
  the reconciliation download — claimed and paid amounts are not
  guaranteed to match.
- **Date-format compliance is a live, recurring failure mode.** The
  required date format is not what every historically-prepared file
  has actually used — check every file's date format fresh each time,
  never assume a past or supplied file was compliant just because it's
  archived or was used before.
- **Management-type tracking is commonly ad hoc.** Whether a given
  participant is agency- vs. plan-managed is often resolved case by
  case (a client ledger, the participant's own plan documents, prior
  successful claim history) rather than tracked in one authoritative
  place — this plugin doesn't assume a provider has solved that; flag
  it as an open item for a given deployment rather than assuming a
  clean source of truth exists.

## Cited domain content

Drawn from a real NDIS-registered provider's own multi-year history of
successfully submitting bulk payment requests through the scheme's
provider portal (JRBA), corroborated across several real submissions
spanning 2022–2026, not from a direct read of the NDIS Commission's own
published guide in this session. Treat the column set, submission
mechanics, and price-guide-capping behaviour above as real-world-
confirmed, but re-verify against the scheme's current portal
documentation before this plugin is relied on for an actual submission
— NDIS support item codes and price-guide rates change (typically each
1 July) and portal mechanics can change independently of this plugin.

## Not in this card

Any provider's registration number, ABN, participant NDIS numbers, real
claim data, or actual rate figures. No cancellation-claim field values
are asserted here — those remain genuinely unconfirmed pending a real
cancellation case or a fresh portal check; state that as missing rather
than guessing if it comes up.

## Plugin self-check

- **Detach:** removing this file leaves `dk0/invoice-billing-manager.md`
  exactly as generic as before — no funding-type vocabulary, CSV
  structure, or portal-mechanics content lives on that card.
- **Audit:** this plugin's own recorded scope is the three funding
  types, the CSV column set, the submission mechanics, and the two
  named open items (date-format risk, management-type tracking) above.
  A drift check should confirm no other claims content (real rates,
  a named provider's registration number, live participant data) has
  been added here without a matching citation.

## Open question carried from recon

Which live seat this plugin actually attaches to, for the JRBA
instance specifically, is not yet settled — the bulk-claims work was
observed coming out of the Documentation Manager seat in the field,
not the Invoice/Billing Manager seat this plugin is drafted against by
role-fit. Resolve at the binding stage, not by assuming this card's
role-fit placement is automatically how JRBA's own instance should be
wired.
