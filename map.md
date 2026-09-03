# Map

This repo is founder HQ (Jy-ops). Not JRBA. Not the shopfront.

DK:0 = no domain knowledge. Three separate assets: Documentation Manager (file hands), Invoice / Billing Manager (plain-English CRM chat + billing), MCP-connected service manager (placeholder until bind). DK:0 cards never name a specialty.

DK:1 = NDIS. First as plugins clipped onto DK:0. After a deploy proves it, dissect by role into DK:1 agents — whole NDIS-scoped actors, not a plugin drawer.

NDIS is domain knowledge because of legislative governance (NDIS Rules 2018, practice guidelines, operational governance). Do not invent statute text. Do not sand that off when stripping org names.

JRBA is one project. Gym/benchmark. Not the chair. Orange pays rent. Grey is not the chair.

## Founder map

YOU → NDIS domain filter → two bound DK:0 roles + PBS pack → JRBA → Claude Teams factory.

MCP placeholder hangs off YOU. Blue. Not bound. No edge to JRBA until establishment.

Shopfront hangs off YOU. Separate. Grey. Not HQ.

PBS pack stays packed. Not approved as a build. No edge to JRBA.

```mermaid
flowchart TD
  classDef you fill:#1B4D3E,stroke:#0F2E25,color:#FFFFFF
  classDef ndis fill:#C45C26,stroke:#8A3E18,color:#FFFFFF
  classDef dk0 fill:#2C5F8A,stroke:#1D4060,color:#FFFFFF
  classDef grey fill:#5C5C5C,stroke:#3D3D3D,color:#FFFFFF
  classDef factory fill:#6B4C9A,stroke:#4A346C,color:#FFFFFF

  you["YOU / Jy-ops"]:::you
  filter["NDIS domain filter"]:::ndis
  doc["DK:0 Documentation Manager"]:::dk0
  rec["DK:0 Invoice / Billing Manager"]:::dk0
  mcp["DK:0 MCP service manager"]:::dk0
  pbs["PBS brain pack"]:::ndis
  jrba["JRBA project"]:::grey
  teams["Claude Teams factory"]:::factory
  shop["Shopfront"]:::grey

  you --> filter
  you --> shop
  you --> mcp
  filter --> doc
  filter --> rec
  filter --> pbs
  doc --> jrba
  rec --> jrba
  jrba --> teams
```

Orange pays rent. Grey is not the chair.

## Birth recipe

Shared seat + scoped process + DK:0 O.G. + connector class + optional DK:1 plugin → establishment bind → named actor → project output (dump).

Shelf gets the DK:0 O.G. now, and DK:1 agents later. Swarm = more seats on a named binding. Not before one real DK:1 exists.

```mermaid
flowchart LR
  classDef you fill:#1B4D3E,stroke:#0F2E25,color:#FFFFFF
  classDef ndis fill:#C45C26,stroke:#8A3E18,color:#FFFFFF
  classDef dk0 fill:#2C5F8A,stroke:#1D4060,color:#FFFFFF
  classDef grey fill:#5C5C5C,stroke:#3D3D3D,color:#FFFFFF
  classDef factory fill:#6B4C9A,stroke:#4A346C,color:#FFFFFF

  seat["Shared seat"]:::factory
  process["Scoped process"]:::factory
  og0["DK:0 O.G."]:::dk0
  conn["Connector class"]:::dk0
  plug["Optional DK:1 plugin"]:::ndis
  estab["Establishment bind"]:::you
  actor["Named actor"]:::factory
  dump["Project output"]:::grey
  shelf["Shelf"]:::you
  later["Later DK:1 agents"]:::ndis

  seat --> process --> og0 --> conn --> plug --> estab --> actor --> dump
  og0 --> shelf
  later --> shelf
```

Establishment is recon, then bind. Not a domain. Do not use a reserved mermaid id (`end`) for the dump.
