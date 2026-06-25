# Consequence Warehouse Safety Proof Kit

Consequence Warehouse Safety is a private-core warehouse robot safety simulator
and evidence prototype for showing how shared consequence memory can help a
robot fleet avoid repeated harm, recover from route failures, and keep delivery
useful after disruption.

It records harmful outcomes as danger memory, useful crossings as success
memory, weak paths as candidates, stale routes as demotion targets, and energy
cost as an operational constraint. The private engine packages those behaviours
into a reproducible Python simulator, scenario runner, evidence reports, tests,
and a local operator dashboard.

This public repository is not the product source code and is not an open-source
release. It is a source-available proof kit for personal and non-commercial
review under the PolyForm Noncommercial License 1.0.0: public-safe evidence,
screenshots, evaluation notes, and an access path for people who want to
request private review.

## Public Proof Release

The current private engine checkpoint is `v1.6`.

Public-safe proof materials in this repo show:

- warehouse routing evidence from the `warehouse_v16_default` scenario
- baseline versus consequence-aware routing metrics
- post-shift damage, fault-hit, delivery, and energy results
- a local operator dashboard interface concept
- the private-core/public-proof publication boundary

## Locked Results

The `v1.6` warehouse evidence summary reports the following 10-seed mean result:

| Proof | What it shows | Headline result |
| --- | --- | ---: |
| [Warehouse evidence](proofs/v1.6-warehouse-evidence/README.md) | Baseline vs consequence-aware routing | 24.00 delivered vs 13.00 baseline |
| [Evidence card](proofs/v1.6-warehouse-evidence/warehouse/evidence_card.md) | Harm reduction after disruption | 88.6 percent lower post-shift damage |
| [Metrics summary](proofs/v1.6-warehouse-evidence/metrics_summary.json) | Machine-readable public summary | 74.7 percent lower fault hits |
| [Interface screenshots](docs/interface-screenshots.md) | Operator dashboard concept | desktop proof surface |

## What This Proves

- Shared consequence memory can improve delivery in the seeded warehouse
  benchmark.
- Consequence-aware routing can reduce repeated post-shift damage versus the
  baseline.
- Consequence-aware routing can reduce fault hits and energy per delivery in
  the locked `v1.6` scenario.
- The project has a reader-facing evidence workflow and an operator dashboard
  direction.
- The private engine has a local validation gate, tests, scenario packs, and a
  local Git checkpoint.

## What This Does Not Prove

- It does not publish the private Consequence Warehouse Safety implementation.
- It is source-available for personal and non-commercial review; it is not an
  open-source release.
- It does not grant a commercial licence.
- It does not grant a patent licence, trademark licence, hosted-service right,
  model-provider right, model-training right, or AI-platform integration right.
- It does not claim every warehouse, robot fleet, or disruption pattern will
  produce the same benchmark deltas.
- It does not replace a private pilot, technical review, safety assessment, or
  customer-specific evaluation.

## Private Engine Access

The private implementation remains closed. Access to the private repository,
source distribution, benchmark internals, full evidence runs, or commercial
evaluation requires written permission from TWO HANDS NETWORK LTD and may
require a signed NDA.

Commercial licensing enquiries should be directed to the COO of TWO HANDS
NETWORK LTD or the company licensing contact designated by TWO HANDS NETWORK
LTD.

Start with:

- [Access Request](ACCESS_REQUEST.md)
- [NDA Access Path](NDA_ACCESS.md)
- [Commercial Use](COMMERCIAL_USE.md)
- [Commercial Licensing](COMMERCIAL-LICENSE.md)
- [Public Materials License](LICENSE.md)
- [Proof Scope](PROOF_SCOPE.md)
- [Publication Checklist](PUBLICATION_CHECKLIST.md)

## Buyer And Reviewer Materials

- [Public proof one-pager](docs/public-proof-one-pager.md)
- [Evidence review guide](docs/evidence-review-guide.md)
- [Architecture overview](docs/architecture-overview.md)
- [Interface screenshots](docs/interface-screenshots.md)
- [Access request checklist](docs/access-request-checklist.md)
- [Publication review](PUBLICATION_REVIEW.md)

## Publication Boundary

This repository exists so interested people can understand the shape of the work
without receiving the private engine.

The public proof kit can be cited, reviewed, and linked for evaluation. The
implementation, private release artifacts, benchmark internals, and commercial
use rights remain private unless granted separately in writing.
