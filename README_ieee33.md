# IEEE 33-bus numerical verification summaries

These platform-neutral CSV files provide retained numerical summaries supporting the associated manuscript. They contain no source code, trained policy, engineering project, runtime log, time-series trace, or execution-environment record.

## Scope

- The dataset summary records counts, not underlying data.
- The representative comparison is a 15-day independent-test, single-run summary. Rows marked verified have independently recomputed voltage RMSE from retained voltage records. The historical td3 row has a deliberately blank voltage_rmse_pu because complete retained voltage evidence was unavailable; its manuscript value is not represented as verified.
- Three-seed tables report mean and sample standard deviation across independently trained policies and must not be interpreted as the representative single run.
- The rejected-scenario summary is a distinct screened-out stress cohort.
- The safety-boundary file is the voltage-margin portion of the validation sweep.

## Units

Voltage is per unit (_pu). Curtailment is accumulated energy (_kwh); reactive regulation is accumulated absolute reactive energy (_kvarh). Voltage RMSE uses the manuscript definition over 1,440 fifteen-minute intervals and 32 non-slack buses against 1.0 pu. Raw metrics precede safety action adjustment; executed metrics follow it. A violation interval has one or more voltage violations under the stated 0.95--1.05 pu criterion; bus steps count individual bus-interval violations. In the safety-boundary summary, `executed_violation_interval_count` retains the saved record's interval-count field.

`mean_projection_adjustment_squared_norm` in the representative single-run table and `projection_adjustment_normalized_mean` in the three-seed common-projection table are different retained summary definitions and must not be compared or pooled as one metric.

Specifically, the single-run quantity averages the dimensionless per-interval squared normalized correction `C(t) = ||D(t)^(-1)*(a_executed(t)-a_reference(t))||_2^2/(2*n_devices)`. Each diagonal scale in `D(t)` uses the corresponding available control range with the numerical lower bound described in the manuscript. The three-seed normalized adjustment is the per-run average of `sqrt(C(t))`, followed by the mean or sample SD across runs. It is the correction NRMSE, not the square root of the mean squared correction. The separately retrained reward-weight R2 group and the paired feature ablation are distinct from the main-method three-seed group.

## Boundary

The material supports numerical-result checking only. It cannot support retraining, policy execution, optimization re-execution, or power-flow re-execution. Private provenance, hashes, and audit mappings are retained by the authors.
