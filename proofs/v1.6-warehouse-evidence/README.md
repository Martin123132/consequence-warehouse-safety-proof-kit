# v1.6 Warehouse Evidence

This folder contains the public-safe proof summary for the private
`v1.6` Consequence Warehouse Safety engine checkpoint.

## Scenario

`warehouse_v16_default`

The scenario models a warehouse with a hidden storage fault band, later gate
shift, stale route recovery, candidate route promotion, and energy discipline.

| Field | Value |
| --- | ---: |
| Grid size | 60 |
| Robots | 25 |
| Packages | 40 |
| Steps | 2600 |
| Disruption step | 500 |
| Gate shift step | 1500 |
| Seeds | 10 |

## Modes Compared

Baseline:

`baseline`

Primary consequence-aware mode:

`adaptive_candidate_efficient`

## Mean Results

| Metric | Baseline | Consequence-aware | Change |
| --- | ---: | ---: | ---: |
| Delivered packages | 13.00 | 24.00 | +11.00 |
| Post-shift damage | 1329.20 | 151.80 | -88.6 percent |
| Fault hits | 1122.40 | 284.30 | -74.7 percent |
| Energy per delivery | 6358.05 | 3883.14 | -38.9 percent |

## Interpretation

The consequence-aware mode improves delivery while reducing post-shift damage,
fault hits, and energy per delivery versus baseline.

Recovery delay is not the headline claim for this run. The strongest public
claim is avoided repeated damage, useful throughput, lower fault exposure, and
energy discipline.

The oracle mode from private experiments is a reference mode, not the product
behaviour, because it uses perfect fault knowledge.

## Files

- [warehouse/evidence_card.md](warehouse/evidence_card.md)
- [metrics_summary.json](metrics_summary.json)
- [verification_notes.md](verification_notes.md)

