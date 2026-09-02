# Map

Founder centre is **JYOps**. Claude Teams is the factory. This repo is the shelf.

JRBA is a project instance, not the hub.

## Founder → specialties → roles → instance

```mermaid
flowchart TD
  founder[Founder / JYOps]
  factory[Factory: Claude Teams]
  shelf[Shelf: this repo]

  founder --> factory
  founder --> shelf

  specNdis[Specialty: NDIS auditing]
  specPbs[Specialty: PBS]
  shelf --> specNdis
  shelf --> specPbs

  roleDoc[Role: Document Manager]
  roleCrm[Role: CRM Billing Manager]
  shelf --> roleDoc
  shelf --> roleCrm

  instJrba[Instance: JRBA]
  specNdis --> instJrba
  roleDoc --> instJrba
  roleCrm --> instJrba

  instJrba --> seats[Two Claude seats remain JRBA]
  instJrba --> run[Another person runs the org]
  instJrba --> founderAssist[Founder assists backend only]

  specPbs --> util[Utilisation not yet chosen]
```

PBS has no project instance yet. Do not draw one.

## Birth recipe

A shelf asset is born in this order. Binding and the named actor come last.

```mermaid
flowchart LR
  seat[Shared seat]
  process[Scoped process]
  og[Role O.G.]
  connector[Connector class]
  specialty[Specialty]
  bind[Bind org / login]
  actor[Named actor]

  seat --> process --> og --> connector --> specialty --> bind --> actor
```

| Step | Lives | Notes |
| --- | --- | --- |
| Shared seat | Factory | Extra seats only if the project already brings in money. |
| Scoped process | Factory + O.G. | What the actor is allowed to do. |
| Role O.G. | Shelf (`roles/`) | Org-stripped rules. |
| Connector class | Shelf, then bind | e.g. document-store subtree, billing CRM — not a folder ID. |
| Specialty | Shelf (`specialties/`) | Domain, not a client. |
| Bind org / login | Instance / factory | Secrets stay out of this repo. |
| Named actor | Factory | The bound seat on that instance. |

**Shelf** = role O.G. + specialty + connector class (org-stripped).

**Swarm** = more seats on a named binding, not employee CVs.

Work-history files are not part of the recipe.
