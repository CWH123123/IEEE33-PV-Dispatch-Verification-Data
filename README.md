Minimal public dataset and verification files for EPSR submission
================================================================

This archive contains the public data package supporting the manuscript:
"Voltage-Constrained Dispatch of Distributed Energy Resources via Sensitivity-Enhanced Reinforcement Learning and Safe Action Projection".

The package is intentionally limited to the generated IEEE 33-bus source--load dataset and numerical verification files. It does not include MATLAB source code, training scripts, plotting scripts, pretrained actors, trained reinforcement-learning agents, or project-specific implementation files. Therefore, this package supports data transparency and numerical-result verification, but it is not a full code-level reproduction package.

Folder contents
---------------

1. dataset/
   Formal IEEE 33-bus source--load scenario dataset used in the manuscript. It includes network data, load and PV scenario matrices, no-control voltage profiles, train/validation/test split information, normalization statistics, sensitivity-base data, and dataset audit files.

2. verification/hyperparameter_validation/
   Validation files for the five hyperparameter settings A--E. The files named with "corrected" and the safe-candidate summary are the authoritative files for the manuscript hyperparameter-screening table. The candidate-level validation files support the checkpoint-reward curve.

3. verification/final_BC_DDPG_test/
   Independent test-set summaries for the selected BC-DDPG policy-projection method.

4. verification/representative_test_days/
   Representative test-day daily summaries corresponding to the manuscript representative cases: test day 9 (normal), test day 13 (low_voltage), test day 14 (high_voltage), and test day 6 (mixed).

5. verification/method_comparison/
   Method-comparison result tables for no control, projection-only dispatch, TD3, DDPG without behavior-cloning initialization, and the proposed BC-DDPG method.

6. verification/safety_boundary_sensitivity/
   Safety-boundary sensitivity results for the voltage-security margin and maximum active-curtailment ratio.

Key values corresponding to the manuscript
------------------------------------------

Dataset:
- Formal dataset: 100 daily scenarios; train/validation/test = 70/15/15 days.
- Scenario categories: 25 normal, 25 low_voltage, 25 high_voltage, and 25 mixed days.
- No-control global voltage range in the formal dataset: 0.899072--1.097335 p.u.
- Projection-screened dataset response: 0.950286--1.045000 p.u., zero voltage violations, maximum slack 5.419412e-09.

Final BC-DDPG test result:
- Agent identifier in result tables: D_gamma095_seed2028_ep0200.
- Success days: 15/15.
- Voltage range: 0.950990--1.044560 p.u.
- Total voltage-violation count: 0.
- Maximum voltage violation: 0.
- Total active-energy curtailment: 5526.879264 kWh.
- Total absolute reactive regulation: 157629.165456 kVArh.
- Projection fallback count: 0.
- Maximum relaxation: 6.755696e-13.

No-control test-set statistics:
- Voltage range: 0.903022--1.097335 p.u.
- Violating dispatch intervals: 338.
- Violating bus-steps: 4274.
These are different statistical levels. The manuscript table uses violating dispatch intervals, whereas the conclusion may use violating bus-steps if explicitly stated.

Representative test days:
- Normal: test day 9, raw day 66, voltage range 0.963194--1.018627 p.u.
- Low_voltage: test day 13, raw day 47, voltage range 0.951236--1.000000 p.u.
- High_voltage: test day 14, raw day 18, voltage range 0.972835--1.044556 p.u.
- Mixed: test day 6, raw day 10, voltage range 0.950990--1.044393 p.u.

Use notes
---------
- CSV files are the primary source for manuscript tables and reported numerical values.
- The .mat files in dataset/ are scenario and network data containers only. They are not trained agents and do not contain the implementation code.
- Local project paths have been removed or sanitized from the public package.
- After deposition, replace the manuscript Data Availability placeholder with the final repository DOI or permanent URL.

Suggested data-availability wording
-----------------------------------
The dataset and numerical verification files supporting the reported simulation results are available in [Repository name] at [DOI/URL]. The shared files include the generated IEEE 33-bus source--load scenarios, scenario labels, train--validation--test split, no-control voltage profiles, validation and test result tables, method-comparison results, representative-day summaries, and safety-boundary sensitivity results. The implementation code, trained reinforcement-learning agents, and project-specific training scripts are not publicly available.

License
-------
Specify the repository license before release. If no code is included, a data-oriented license such as CC BY 4.0 is usually appropriate, subject to institutional approval.
