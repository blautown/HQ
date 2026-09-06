# Claude Teams factory — onboarding & pricing

This is the commercial layer under the "Claude Teams factory" node in [`map.md`](../map.md). It sits around the technical establishment protocol ([`dk0/establishment.md`](../dk0/establishment.md)), not inside it. Establishment is recon-then-bind for one seat; this is how a client gets to the point of having a seat at all, and what they pay for it.

No secrets, no emails, no client billing details, no real dollar commitments — same rule as the rest of this repo. Pricing below is a starting framework, not a rate card until the founder confirms the numbers.

## Seat model

The client owns their own Claude Team plan — their org, their billing relationship with Anthropic, their ToS. The founder does not resell or share a personal seat into client work; JRBA's two seats are a grandfathered exception, not the pattern going forward (see `TASKS.md`).

Every client Team plan includes:
- N seats for their own agent instances (however many DK:0/DK:1 roles the client needs — sized at recon)
- 1 seat bundled in for the founder, priced into the service fee below — this is the founder's entry point into every live client org for 24/7 support, tuning, and upsell

Reference pricing for sizing quotes (Anthropic-set, confirm current rate before quoting a client — this drifts):
- Standard seat: ~$20/mo billed annually, ~$25/mo billed monthly
- Premium seat (Claude Cowork, Fable 5, 6.25x usage): ~$100/mo annually, ~$125/mo monthly
- Plan minimum 2 seats, caps at 150

The bundled founder seat costs a rounding error next to the service fee below — it does not need its own line item to the client.

## Onboarding process (per new client)

1. **Discovery call** — existing "Book a call" CTA. Qualify fit before anything else ("I'll tell you if I can take it — I almost always can").
2. **Recon** — founder-led, per `dk0/establishment.md`: org structure, plan-managed vs agency-managed vs self-managed, current systems, audit history/gaps, worker-screening status, in-scope/out-of-scope per role. This is the "project context" angle of the ROM (`map.md`).
3. **Client provisions their own Claude Team plan**, sized to (agent seats needed) + 1 founder seat.
4. **Founder builds the role-specific context ROM** per agent — DK:0 O.G. plus any relevant DK:1 plugin, fused with the client's recon context.
5. **Bind + deploy** — projects loaded into the client's org; binding sheet recorded under `instances/<client>.md`; founder joins the org via the bundled seat.
6. **Go-live gate** — one real task proven per agent (not a demo) before calling it handed off.
7. **Guarantee checkpoint** — diff the live job against [`offer.md`](offer.md), not against ad copy. Registration-ready clock, audit-pass trigger, money-back, follow-up readiness pass. If a `[confirm]` on that card is still blank, this step has nothing to check — do not pretend the published promise is in force.
8. **24/7 support window opens** — founder monitors and tunes via the bundled seat, in the sense defined in `offer.md` §3. This is also the upsell surface: more agents, more DK:1 modules, tier upgrades.

## Pricing — draft, needs founder sign-off before it goes on the site

Two lines on every proposal, kept visibly separate so there's no ambiguity about who bills what:
- **Client's Claude Team plan** — billed directly by Anthropic to the client. Not JYOps revenue. State the seat math in the proposal.
- **JYOps service fee** — covers recon, ROM build(s), the bundled founder seat, and ongoing 24/7 support/tuning. This is where the business actually earns.

Draft tiers (placeholder numbers — anchor against NDIS compliance-consulting rates, not commodity SaaS; a deregistration or failed audit costs a provider far more than any of these):

| Tier | Fit | Setup fee (one-time) | Monthly retainer |
| --- | --- | --- | --- |
| Starter | Sole trader, 1–2 agents (e.g. Doc Manager only) | `[confirm]` | `[confirm]` |
| Growth | Small team, 3–4 agents, one DK:1 module (e.g. claims/PRODA) | `[confirm]` | `[confirm]` |
| Scale | Multi-agent, PBS or core-module audit suite | Custom quote | Custom quote |

Setup fee should reflect the intensity of the "registration-ready in under a week" push — it is a rush recon-and-build sprint, not a standing cost. Monthly retainer is what funds the 24/7 seat and is the number that should scale with agent count, since agent count tracks both founder attention and upsell surface.

## Access governance

The target market mostly doesn't know what Claude is beyond the name, and once the client owns the Team plan, their own staff have direct seats into the bound projects. Two separate controls, not one:

**Permission tier (stops permanent damage):** every client staff seat is added to each project as **"Can view,"** never "Can edit." Viewers can chat inside the project freely but cannot touch custom instructions or the knowledge base. The founder holds the sole "Can edit" / creator role on every bound project. This is a standing rule, not a per-client judgment call — do not grant a client staff member edit access to a bound project.

**Behavioural expectations (stops a bad single conversation):** view-only access does not stop someone from arguing the agent out of scope mid-chat, or pasting data it doesn't need. Every client gets the one-page brief at go-live: [`client-brief.md`](../client-brief.md). It is generic and exportable — no client specifics — and is what actually gets handed/pasted to the client, same pattern as `dk0/establishment.md`.

**Backstop:** [`dk0/drift-check.md`](../dk0/drift-check.md) is the periodic catch for anything that slips past both controls — restate scope, diff against the binding sheet, confirm the plugin still dismantles cleanly. Drift check only diagnoses; [`dk0/restore-point.md`](../dk0/restore-point.md) is the recovery half — a weekly, verified-clean snapshot taken right after a CLEAN drift check, so a bad edit or drift can be rolled back instead of rebuilt from memory.

## Not yet decided

- Exact `[confirm]` dollar figures.
- Offer terms still `[confirm]` on [`offer.md`](offer.md): registration-ready clock, audit-pass / money-back / follow-up / window, 24/7 first-response, discovery decline list. Cash vs credit for a triggered refund is one of those.
- Offboarding process for the bundled founder seat when a client contract ends.
