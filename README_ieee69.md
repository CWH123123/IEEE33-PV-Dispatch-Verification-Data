# IEEE 69 numerical verification subset

This directory contains platform-neutral aggregate data supporting numerical checks of the IEEE 69 results reported in the manuscript. CSV fields use scientific units and definitions are provided in `ieee69_metric_definitions.md`.

## Network-specific context

| quantity | IEEE 69 evaluation | IEEE 33 evaluation |
| --- | ---: | ---: |
| non-reference buses | 68 | 32 |
| PV inverter locations | 11; 18; 27; 35; 50; 61 | not repeated here |
| inverter rating multiplier | 1.40 | 1.10 |
| feeder PV scaling threshold | 2.25 | 1.95 |
| candidate days / reference-screen accepted | 5000 / 2586 | not repeated here |

These are feeder-specific experimental settings, rather than portable defaults.

Scope: these files support aggregation and rounding checks only. They do not support full execution reproduction. No source programs, learned parameter files, training records, scenario time series, interval-level voltage data, internal project structure, or execution logs are included.

Interpretation: `ieee69_seed_test_summary.csv` gives the three retained behavior-cloning-initialized DDPG seed-specific summaries. `ieee69_method_comparison.csv` distinguishes the three-seed mean/sample SD from single baseline summaries. `ieee69_representative_run.csv` uses one representative DDPG seed and must not be interpreted as the DDPG three-seed mean. Each retained DDPG run used a terminal safety fallback in one interval, while its final executed violation counts remained zero; final feasibility must therefore not be interpreted as absence of all safety interventions.

Use limitation: values are released for manuscript-result verification. They must not be used to infer or reconstruct the protected implementation.
