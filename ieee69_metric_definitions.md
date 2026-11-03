# IEEE 69 numerical metric definitions

All rows refer to a retained 15-day test partition with 96 intervals per day. Values are numerical summaries from the authors' study, released for result verification only.

- `curtailment_kwh`: total curtailed active energy during the test partition, in kWh.
- `reactive_regulation_kvarh`: sum of absolute reactive-energy regulation during the test partition, in kVArh.
- `voltage_rmse_pu`: `sqrt((1/(T*B))*sum_t sum_b (v[b,t]-1.0)^2)`, where `T=1440` test intervals and `B=68` non-reference buses, in per unit. The DDPG mean is the arithmetic mean of the three seed-specific RMSE values, not a pooled voltage-vector RMSE.
- `raw_violation_intervals` and `raw_violation_bussteps`: violations before the reported safety action. `executed_violation_intervals` and `executed_violation_bussteps` are counted after it. The voltage range used for these counts is 0.95--1.05 p.u.
- `projection_correction_cost_mean`: the 1,440-interval mean of `C_proj(t) = (1/(2*N_D))*||D_x(t)^(-1)*(x_safe(t)-x_raw(t))||_2^2`. `x_raw` is the dispatch reference, `x_safe` is the executed safe action, `N_D` is the number of controlled devices, and diagonal `D_x(t)` normalizes each action coordinate by its current control range with a unit numerical lower bound. Thus the measure is dimensionless and is a normalized mean-squared reference-to-action correction, not total physical control effort.

`mean` and `sample_sd` for DDPG summarize three independently retained seed-specific result records. Here `ddpg` denotes the behavior-cloning-initialized DDPG method. `single_run` denotes one retained baseline result. The test dispatch interval is 15 minutes. The files enable numerical checks of published summaries; they do not provide an executable implementation, model parameters, training materials, or interval-level traces.
