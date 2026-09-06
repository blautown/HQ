# Instance: JRBA

Binding sheets for the two bound DK:0 seats. No secrets: no root folder ID, no tenant URL, no staff or participant identifiers. Fields marked `[confirm]` are not invented here — fill them from a real establishment or [drift check](../dk0/drift-check.md) session with the live seat, not from guesswork.

**Specialty:** [NDIS auditing](../specialties/ndis-auditing.md) — instance one of that specialty, not the centre of JYOps.

**What it is:** an NDIS provider. Live. Still needs refining. Founder effort is not centred here.

**Who runs it:** another person runs the org day to day. The founder is audit-authority and still assists on the backend.

**Retrofit pending (see `TASKS.md`):** JRBA was bound before the current standard existed — the `[confirm]` fields below were never filled from a real session, no `client-brief.md` was ever sent, and no drift-check / restore-point cadence has run against it. It should not be held up as proof the standard works until this retrofit closes. This does not change the seat policy — two seats stay JRBA per `README.md`; the retrofit is documentation and governance discipline, not a seat migration.

## HQ asset crosswalk and benchmark

The two live seats are deployments assembled from HQ box assets, not separate assets owned by this instance. Each deployment combines an HQ identity, reusable operational guidelines, a directly sourced domain-knowledge plugin when bound, and JRBA project context. Their matching plan and benchmark sequence are in [`../benchmark.md`](../benchmark.md).

| Live seat | HQ identity | Operational guidelines | Domain/plugin status | What must be benchmarked |
| --- | --- | --- | --- |
| Documentation Manager | Domain manager / record-keeper — [`../dk0/documentation-manager.md`](../dk0/documentation-manager.md) | Reusable documentation role guidelines, without JRBA context | NDIS source → candidate core-module / PBS plugin; none currently recorded as bound | File hands, subtree/session gate, NDIS audit-readiness behaviour, and any PBS register/policy behaviour observed in the live agent |
| Invoice / Billing Manager | Domain record-keeper — [`../dk0/invoice-billing-manager.md`](../dk0/invoice-billing-manager.md) | Reusable billing/recordkeeping role guidelines, without JRBA context | NDIS source → candidate claims / PRODA / plan-manager plugin; none currently recorded as bound | Billing/recordkeeping rules, batch handling, state verification, claims behaviour, and plan-manager split observed in the live agent |

Observed capability is not automatically a plugin. It becomes an HQ plugin only after it is extracted from the deployment, written as org-stripped domain knowledge, shown to detach cleanly from the identity and operational guidelines, and benchmarked through a deployed agent.

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
| Optional plugin | None bound. Candidate NDIS audit-readiness plugins are still drafts — see [`../benchmark.md`](../benchmark.md) and [`../TASKS.md`](../TASKS.md) |
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
| Optional plugin | None bound. Candidate NDIS claims/PRODA/plan-manager plugin is still a draft — see [`../benchmark.md`](../benchmark.md) and [`../TASKS.md`](../TASKS.md) |
| Status | BOUND (live) |

---

**Factory:** two Claude seats. These are the existing seats; they remain JRBA seats per policy.

Do not put JRBA folder roots, logins, tenant URLs, or people into this repo. Those stay in the factory and the live org. When the `[confirm]` fields above are filled in from a live session, keep them to a title or display name — never a login, an ID, or a person.
