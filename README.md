# IEEE 33-bus and IEEE 69-bus numerical verification summaries

This directory contains supplementary, platform-neutral numerical summaries associated with the manuscript **"Voltage-Constrained PV Inverter Dispatch via Sensitivity-Enhanced Reinforcement Learning and Safe Action Projection"** (EPSR-D-26-05858R2).

## Contents

- [`ieee33/`](ieee33/README_ieee33.md): dataset-screening counts, representative and three-seed method comparisons, safety-boundary analysis, sensitivity-feature ablation, reward-weight sensitivity and rejected-scenario outcomes.
- [`ieee69/`](ieee69/README_ieee69.md): dataset-summary counts, representative and three-seed test statistics, method comparisons and metric definitions.
- [`docs/manuscript_result_mapping.md`](docs/manuscript_result_mapping.md): mapping between manuscript tables and available numerical summaries.
- [`docs/verification_scope_and_limitations.md`](docs/verification_scope_and_limitations.md): interpretation, provenance boundaries and limitations.
- [`MANIFEST_public_files.csv`](MANIFEST_public_files.csv) and [`CHECKSUMS_SHA256.csv`](CHECKSUMS_SHA256.csv): file inventory and SHA-256 checksums.

## Verification scope

The supplied files support inspection of selected aggregate results, checking reported rounding and recomputing certain multi-seed statistics. They are **not** a complete executable reproduction package. They do not include implementation source code, trained agents, model weights, training scripts, full time-series scenarios or interval-level voltage/action records.

Results for one representative run and results aggregated across three independently trained seeds must not be treated as interchangeable. Zero observed executed voltage violations refers only to the stated evaluation scenarios and does not imply unconditional safety. The limitations documents identify which historical values cannot be independently reconstructed from the retained records in this release.

The original repository's existing files are outside this directory; this supplementary summary folder does not replace or modify them.
