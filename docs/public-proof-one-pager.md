# Public Proof One-Pager

## Simulator Claim

Shared consequence memory helps warehouse robot fleets avoid repeated damage,
recover from route failures, and improve useful delivery after disruption.

## Scenario

The public proof summarizes the locked `warehouse_v16_default` scenario:

| Field | Value |
| --- | ---: |
| Grid size | 60 |
| Robots | 25 |
| Packages | 40 |
| Steps | 2600 |
| Disruption step | 500 |
| Gate shift step | 1500 |
| Seeds | 10 |

## Headline Result

| Metric | Baseline | Consequence-aware | Change |
| --- | ---: | ---: | ---: |
| Delivered packages | 13.00 | 24.00 | +11.00 |
| Post-shift damage | 1329.20 | 151.80 | -88.6 percent |
| Fault hits | 1122.40 | 284.30 | -74.7 percent |
| Energy per delivery | 6358.05 | 3883.14 | -38.9 percent |

## Why It Matters

The baseline keeps paying for repeated harmful routes after disruption. The
consequence-aware mode shares operational memory across the fleet, demotes stale
routes, promotes safer candidates, and keeps energy cost visible.

The result is not just a prettier route. It is a better operating story:
more delivery, less repeated damage, fewer fault hits, and lower energy per
delivery in the locked benchmark.

## Boundary

This is a public simulator proof summary. It is not a production safety
certification. The private engine, implementation, full run folders, notebook
source, and commercial use rights are not included.
