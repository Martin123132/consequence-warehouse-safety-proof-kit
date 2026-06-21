# Architecture Overview

Consequence Warehouse Safety is designed as a private engine with a public proof
surface.

## Private Engine

The private engine owns:

- warehouse grid simulation
- robot agents
- package routing
- fault and gate disruption logic
- danger memory
- success memory
- candidate route memory
- stale route demotion
- energy accounting
- scenario runner
- validation tests
- local operator dashboard
- generated evidence bundles

## Public Proof Kit

The public proof kit owns:

- public-safe proof story
- locked headline results
- sanitized evidence cards
- reader-facing verification notes
- architecture and proof-scope documents
- screenshots or demo media that do not expose the private implementation
- access, NDA, commercial-use, and licence path

## Conceptual Flow

```text
warehouse disruption
  -> baseline repeats harmful routes
  -> consequence-aware fleet records outcomes
  -> danger and stale routes are demoted
  -> useful candidates are promoted
  -> fleet improves delivery, damage, fault-hit, and energy metrics
  -> evidence pack summarizes the result
```

## Product Direction

The private product is an operator-grade safety simulator and evidence workflow.
The public proof kit is the outer layer that lets people understand the claim
without receiving the engine.

