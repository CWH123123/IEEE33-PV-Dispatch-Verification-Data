# Mapping to manuscript results

The table and figure references correspond to manuscript revision EPSR-D-26-05858R2; numbering may differ between versions.

| Manuscript location | Available verification material | Scope |
|---|---|---|
| Tables 1–3; Figures 1–3 | Method description in the manuscript | No implementation, network diagrams or training artifacts reproduced in this package |
| Table 4 and dataset construction | IEEE33 dataset summary | Aggregate screening and split counts; no full scenario arrays |
| Table 5; Figures 5–6 | Manuscript only | No training curves or checkpoint-selection traces supplied |
| Table 6 | IEEE33 representative method comparison | Kept separate from the three-seed comparison; historical TD3 voltage RMSE withheld pending adequate source evidence |
| Table 7 | IEEE33 common-projection three-seed summary | Mean/sample SD across three independently trained runs per method |
| Table 8 | IEEE33 sensitivity-ablation summary | Independently selected paired full-feature/no-sensitivity configurations |
| Table 9 | IEEE33 rejected-scenario summary | Executed safety counts from the 1,017-day rejected pool; 97,632 intervals |
| Table 10; Figure 11 | IEEE33 safety-boundary summary | Validation-set parameter sweeps; not independent-test-set tuning |
| Table 11 | IEEE33 reward-weight summary | Three runs per weight setting; reward-study R2 is a separate retrained group |
| Table 12 | Not supplied | Hardware-sensitive timing and runtime provenance are outside this platform-neutral minimal data release |
| Table 13 | IEEE69 representative-run and method-comparison data | Seed-2027 illustrative run and deterministic baselines |
| IEEE69 evaluation and conclusion | IEEE69 per-seed and method summaries | Three-seed mean/sample SD, voltage RMSE and mean squared projection correction |
| Figures 4, 7–10; equation (41) | Selected associated aggregate results only | No claim that the complete original plotted data or all prediction/AC error vectors are supplied |

The voltage RMSE definition is equation (40) of the confirmed marked manuscript: deviation of executed nonlinear AC voltages from 1.0 p.u., excluding the slack bus. Dataset-specific bus counts must be used. The three-seed mean of per-run RMSE values is distinct from a pooled RMSE over all three runs.
