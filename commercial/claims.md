# Claims ledger

Every public marketing claim on the live site must trace to an internal process that actually delivers it. This is not a marketing doc — no rewritten copy, no pricing — it is the audit trail from a published claim back to the mechanism behind it, so the marketing push never outruns what the operation can actually stand behind.

Word meanings live in [`offer.md`](offer.md). This table only traces. A definition is not proof: PARTIAL means the term is defined and the process exists; BACKED means a real run has stood behind it.

| Claim (as published) | Backing process | Status |
| --- | --- | --- |
| "Unregistered provider to registration-ready in less than a week" | [`offer.md`](offer.md) §1 + `factory.md` onboarding steps 1–6 | **PARTIAL** — the landing-page clock and exclusions are now transcribed; no completed run yet proves the duration. |
| Guaranteed audit pass, money-back, complimentary follow-up audit | [`offer.md`](offer.md) §2 | **PARTIAL** — exact published trigger, covered audits, refund scope, timing, exclusions, and remediation are recorded; no completed guarantee run yet proves delivery. |
| Founder personally migrates every client | `factory.md` onboarding steps 1–5 (recon, ROM build, bind, deploy are all founder-run) | **BACKED** |
| 24/7 expert support | Landing-page live chat handoff + [`offer.md`](offer.md) §3 | **PARTIAL** — live chat and the five-business-day written guarantee-claim response are documented; this is not proof of a staffed call-centre SLA. |
| "I'll tell you if I can take it — I almost always can" | `factory.md` step 1 + [`offer.md`](offer.md) §6 | **PARTIAL** — discovery is the gate; the decline list remains a founder proposal, not a published operating term. |
| "One chat. Fifty NDIS functions" | none | **UNPUBLISH** — no inventory on the shelf. See `offer.md` "Not a term yet" |
| "PBS ops" | [`specialties/pbs.md`](../specialties/pbs.md) | **UNPUBLISH** — utilisation not chosen; not approved as a build |
| "Overheads down, guaranteed" | [`offer.md`](offer.md) §4 | **PARTIAL** — the published unit, baseline, 90-day window, refund rule, and exclusions are recorded; no completed measurement proves the outcome. |
| "Guaranteed data safety, backup, and compliant handling" | [`offer.md`](offer.md) §5 | **PARTIAL** — published storage, access, backup, restore, incident-notice, and privacy terms are recorded; this ledger does not independently certify compliance or prove a restore run. |

## How to use this

Add or update a row whenever a marketing claim goes live or changes — before or immediately after the copy ships, not months later. When a row moves from GAP/PARTIAL to BACKED, link the doc that closed it. UNPUBLISH means take it off the live page until the shelf exists; do not "back" it by rephrasing.

Review this alongside `dk0/drift-check.md`'s cadence, or whenever `factory.md` or `offer.md` changes.

A GAP/PARTIAL/UNPUBLISH row is not an emergency to fix before the next sales call — it's a known liability. The point of this file is that it's written down, not that it's zero.
