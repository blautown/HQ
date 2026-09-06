**Mirror of** [`instances/jyops-outreach.md`](../../instances/jyops-outreach.md) **— canonical source is that file, not this copy.** If this copy and the canonical file ever disagree, the canonical file is right; this one is stale and needs re-syncing. Once this agent actually binds, the real values get written into the *canonical* file first, then mirrored here — never the reverse.

---

# Instance: Jyops (Prospect/Outreach Manager)

Binding-sheet **stub** — pending the future onboarding-intake template (see `TASKS.md`). This is not the final binding-sheet design; it exists only so [drift check](../../dk0/drift-check.md) has something real to diff against once this asset is established. No secrets: no literal sending address, no tenant/API credentials, no contact PII.

**Bound org:** Jyops itself — the founder's own business, not a served NDIS client. Per the corrected rule in [`domain-knowledge-boundaries.md`](../../dk0/domain-knowledge-boundaries.md) ("Where the benchmark actually lives"), this is benchmarked in the founder's own admin seat exactly like any client-bound instance; only the workspace it sits inside differs.

**What it is:** the business-development instance of the [Prospect/Outreach Manager](identity.md) — finds NDIS-registered providers who could become JYOps clients. Not yet established; see `Status` below.

**Who runs it:** the founder, as both operator and audit-authority. No separate org operator — this instance has no served client.

## HQ asset crosswalk

| Field | Value |
| --- | --- |
| Asset | [Prospect/Outreach Manager](identity.md) |
| Operational guidelines | Reusable outreach role guidelines, without project-specific context |
| Domain/plugin status | [NDIS outreach compliance framing](plugin.md) v1 |

---

## Binding sheet — Prospect/Outreach Manager

| Field | Value |
| --- | --- |
| Asset | [Prospect/Outreach Manager](identity.md) |
| Org display name | Jyops (founder's own business) |
| Named actor | `[confirm]` |
| Operator / audit-authority | Founder (both roles — no separate served client) |
| Connector class | Email connector (sending) + tracking store |
| Sending display name | `[confirm]` — display name only, never the literal email address |
| In-scope | `[confirm]` — the real prospect list/ICP, once defined |
| ICP description | `[confirm]` |
| Volume cap | `[confirm]` |
| Approval-gate | `[confirm]` — on/off |
| Out-of-scope | JRBA and every existing client, always suppressed; never shared to any NDIS client seat/org |
| Optional plugin | [NDIS outreach compliance framing](plugin.md) v1 |
| Status | UNBOUND (stub) |

---

**Stub notice:** every `[confirm]` field above is a placeholder, not a guess. This sheet is not the final binding-sheet design — a future onboarding-intake template will supersede it (see `TASKS.md`). It exists now only so `birth.md`'s Phase 2 has a real sheet to fill in, and so [`dk0/drift-check.md`](../../dk0/drift-check.md) has the explicit in-scope / out-of-scope / status fields it requires to diff against.

Do not put the sending address's literal text, tenant or API credentials, or any contact's PII into this repo. Those stay in the live connector and tracking store.
