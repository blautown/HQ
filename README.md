# JYOps-hq

Jacob Yaghmoor's founder base of operations in Cursor.

This repo is **HQ**. It is markdown only: no app, no deploy, no secrets, no client folders.

Claude Teams is the **factory** for paying project work. Seats, connectors, and named actors live there. This repo holds the org-stripped shelf: specialties, role operating guides, and the map of how they bind to a project instance.

Open this folder in Cursor. That is the whole product.

## Policy

- **Founder centre is JYOps**, not any one client project.
- The **two existing Claude Teams seats remain JRBA seats**.
- **Additional Claude seats only if that project already brings in money.**
- A **shelf asset is born** in this order: shared seat + scoped process + role O.G. + connector class + specialty → then bind org/login → named actor.
- **Shelf** = role O.G. + specialty + connector class (org-stripped).
- **Swarm** = more seats on a named binding, not employee CVs.
- **Work-history files are not required.** Do not add them to keep a role or instance "complete."
- **JRBA is instance one** of the NDIS specialty. It is a live project that still needs refining. Founder effort is not centred there.

Do not put personal emails, Drive folder IDs, participant names, staff IDs, or phone numbers in this repo. Bindings and logins stay in the factory (Claude Teams / the live org), not here.

## Layout

| Path | What it is |
| --- | --- |
| [`specialties/`](specialties/) | Domain specialties (org-stripped). |
| [`roles/`](roles/) | Role operating guides (O.G.s). Generic. Reusable. |
| [`instances/`](instances/) | How a shelf asset binds to one organisation. No secrets. |
| [`map.md`](map.md) | Founder map and the birth recipe. |

## How to add a specialty

A specialty is a domain Jacob (or JYOps) already works in. It is not a client and not a seat.

1. Add `specialties/<slug>.md`.
2. State the domain in one paragraph. Name the kind of work, not a customer.
3. Point at which role O.G.s and connector *classes* usually travel with it (Drive, a CRM product family, and so on). Do not paste folder IDs or logins.
4. If utilisation is undecided, say so. Do not invent a rollout.

A specialty can have many instances. JRBA does not *own* NDIS auditing; it is one live binding of that specialty.

## How to add a role

A role is a reusable operating guide. It is shelf material: org-stripped.

1. Add `roles/<slug>.md`.
2. Write the O.G. as rules an actor can follow in *any* org that has that job.
3. Name the **connector class** (for example: document-store subtree; billing CRM), not an org's folder or tenant.
4. Separate **operator** from **audit-authority (founder)** when the role can file or mutate.
5. Leave live trackers, aliases, and org-specific registers out of the O.G. Those belong on the instance, outside this repo if they contain people.

Do not copy a filled JRBA prompt into a new role file. Strip the org first. If it cannot be stripped, it is instance material, not shelf.

## How to add an instance

An instance binds one or more roles + a specialty to one organisation.

1. Add a short note under [`instances/`](instances/) (or a new `instances/<slug>.md` if the note will not fit the index).
2. Record: specialty, roles bound, connector *classes*, seat count, who runs the org, what the founder still touches.
3. No secrets. No emails. No folder IDs. No participant or staff identifiers.
4. Only bind after the shelf asset exists (seat + process + O.G. + connector class + specialty). The named actor is the last step, and it lives in the factory.

JRBA is already instance one. See [`instances/README.md`](instances/README.md).

## Shelf vs swarm

| | Shelf | Swarm |
| --- | --- | --- |
| What | Role O.G. + specialty + connector class, org-stripped | More seats on a **named binding** |
| Where | This repo | Claude Teams (factory) |
| Not | A person's CV or work history | Hiring, or a new specialty |

Do not grow swarm on a project that is not already bringing in money. Do not treat extra seats as a substitute for a missing O.G.

## What this repo is not

Not a client file store. Not a CRM. Not a deploy target. Not a marketing plan. Not a second factory.
