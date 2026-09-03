# Instance: JRBA

Binding sheets for the two bound DK:0 seats. No secrets: no root folder ID, no tenant URL, no staff or participant identifiers. Fields marked `[confirm]` are not invented here — fill them from a real establishment or [drift check](../dk0/drift-check.md) session with the live seat, not from guesswork.

**Specialty:** [NDIS auditing](../specialties/ndis-auditing.md) — instance one of that specialty, not the centre of JYOps.

**What it is:** an NDIS provider. Live. Still needs refining. Founder effort is not centred here.

**Who runs it:** another person runs the org day to day. The founder is audit-authority and still assists on the backend.

---

## Binding sheet — Documentation Manager

| Field | Value |
| --- | --- |
| Asset | [Documentation Manager](../dk0/documentation-manager.md) |
| Org display name | JRBA |
| Named actor | `[confirm]` |
| Operator / audit-authority | Org operator runs day to day; founder is audit-authority |
| Connector class | Document-store subtree (Google Drive) |
| Identity check | `[confirm]` — root folder title, not an ID |
| In-scope | Retrieve, report, pre-fill, file inside the configured Drive subtree; register-driven naming |
| Out-of-scope | Anything outside the configured subtree; unscoped search; structure changes without founder-led reorg |
| Optional plugin | None bound. NDIS audit-readiness plugins are still drafts — see [`TASKS.md`](../TASKS.md) |
| Status | BOUND (live) |

## Binding sheet — Invoice / Billing Manager

| Field | Value |
| --- | --- |
| Asset | [Invoice / Billing Manager](../dk0/invoice-billing-manager.md) |
| Org display name | JRBA |
| Named actor | `[confirm]` |
| Operator / audit-authority | Org operator runs day to day; founder is audit-authority |
| Connector class | Billing CRM (ShiftCare) |
| Identity check | `[confirm]` — CRM display name for the identity check |
| In-scope | Billing/recordkeeping batches and notes in the CRM; billing automation |
| Out-of-scope | Linked contacts, nominees, or access records in the CRM; alias guesses without operator confirmation |
| Optional plugin | None bound. NDIS claims/PRODA plugin is still a draft — see [`TASKS.md`](../TASKS.md) |
| Status | BOUND (live) |

---

**Factory:** two Claude seats. These are the existing seats; they remain JRBA seats per policy.

Do not put JRBA folder roots, logins, tenant URLs, or people into this repo. Those stay in the factory and the live org. When the `[confirm]` fields above are filled in from a live session, keep them to a title or display name — never a login, an ID, or a person.
