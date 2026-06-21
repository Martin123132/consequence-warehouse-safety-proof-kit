# Warehouse Evidence Card

## Claim

Shared consequence memory helps warehouse robot fleets avoid repeated damage,
recover from route failures, and improve throughput after disruption.

## Benchmark

`warehouse_v16_default`, 10 seeds.

The benchmark includes:

- 60 by 60 warehouse grid
- 25 robots
- 40 packages
- 2600 steps
- disruption at step 500
- gate shift at step 1500
- hidden storage fault band
- candidate route promotion
- stale route demotion
- energy discipline

## Result

| Metric | Baseline | Consequence-aware | Change |
| --- | ---: | ---: | ---: |
| Delivered packages | 13.00 | 24.00 | +11.00 |
| Post-shift damage | 1329.20 | 151.80 | -88.6 percent |
| Fault hits | 1122.40 | 284.30 | -74.7 percent |
| Energy per delivery | 6358.05 | 3883.14 | -38.9 percent |

## Reader Summary

The baseline keeps finding work, but it pays for it through repeated harm after
the environment changes. The consequence-aware mode shares what the fleet learns
from harmful and useful outcomes. That memory helps the fleet avoid repeated
damage, reduce fault exposure, and spend less energy per successful delivery.

## Limitations

- This card summarizes a seeded benchmark, not a real warehouse deployment.
- Results should be checked against customer-specific layouts and robot
  constraints before any safety claim is made in production.
- The private engine and raw run folders are not included in this public proof
  kit.
- This evidence does not grant commercial use rights.

