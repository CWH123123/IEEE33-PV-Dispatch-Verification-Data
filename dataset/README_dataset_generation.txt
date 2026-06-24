IEEE33 formal_v2 source--load dataset record
=============================================

This directory contains the formal IEEE 33-bus active distribution network dataset used in the manuscript.
It includes network data, generated source--load scenarios, no-control voltage profiles, train/validation/test split information, normalization statistics, and dataset audit files.

Dataset summary
---------------
- Random seed: 2026
- Total days: 100
- Time steps per day: 96
- Time resolution: 15 min
- Voltage limits: 0.95--1.05 p.u.
- PV buses: 6, 14, 18, 25, 30, and 33
- Scenario categories: 25 normal, 25 low_voltage, 25 high_voltage, and 25 mixed days
- Train/validation/test split: 70/15/15 days
- Split scenario counts:
  - train: normal=18, low_voltage=18, high_voltage=17, mixed=17
  - validation: normal=4, low_voltage=3, high_voltage=4, mixed=4
  - test: normal=3, low_voltage=4, high_voltage=4, mixed=4

Dataset audit
-------------
- No-control global voltage range: 0.899072--1.097335 p.u.
- Projection-screened voltage range: 0.950286--1.045000 p.u.
- Projection-screened total voltage-violation count: 0
- Projection-screened maximum slack: 5.419412e-09

Scientific-use notes
--------------------
1. Node voltages are not manually assigned or modified.
2. V_all and theta_all are obtained from Newton--Raphson AC power flow.
3. Formal train/validation/test days were screened by a projection-based reference controller and nonlinear power-flow verification before model training.
4. Physically uncontrollable candidates were excluded from the formal dataset and are not included in this public package.
5. The train/validation/test split is stratified by no-control voltage-condition labels.
6. Normalization statistics are computed from train_days only.
7. Test days must not be used for checkpoint selection or hyperparameter tuning.
