Safety-boundary sensitivity analysis for formal_v2_noCref
=========================================================

Dataset: [local path removed]
Evaluation set: validation
Fixed agent: [local path removed]

Baseline parameters:
  Original voltage limits: 0.95 <= V <= 1.05 p.u.
  epsV = 0.0050
  Internal projection voltage band: 0.9550 <= V <= 1.0450 p.u.
  Pcur_max_ratio = 0.30

Experiment design:
  epsV sweep: fixed Pcur_max_ratio = 0.30
  Pcur_max_ratio sweep: fixed epsV = 0.0050

Generated files:
  sensitivity_epsV_summary.csv
  sensitivity_epsV_daily_results.csv
  sensitivity_epsV_group_summary.csv
  sensitivity_PcurRatio_summary.csv
  sensitivity_PcurRatio_daily_results.csv
  sensitivity_PcurRatio_group_summary.csv
  safety_boundary_sensitivity_formal_v2_noCref.mat
  figures/Fig_safety_boundary_sensitivity_relative_cost_SCI.pdf
  figures/Fig_safety_boundary_sensitivity_relative_cost_SCI.tif

Interpretation note:
  This analysis fixes the final BC-DDPG agent and only perturbs safety-projection parameters.
  It is not used for retraining or model reselection.
  The baseline setting is treated as the engineering reference point.
