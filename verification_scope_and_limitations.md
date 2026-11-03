# Verification scope and limitations

This is a numerical-result verification dataset. It permits reading independent-test summaries, checking published rounding, recomputing selected three-run statistics where per-seed values are provided, and distinguishing raw-reference voltage violations from executed-action violations. Summary-only files cannot reconstruct policy execution, every node voltage, a training trajectory or the full experiment.

Scientific definitions and limitations are preserved: executed voltage feasibility is evaluated after nonlinear AC power-flow verification and the prescribed projection/recovery procedure. Zero executed violations is an observation on the evaluated data, not an unconditional safety guarantee or proof of zero solver failures. Rejected-domain safety is incomplete and is reported explicitly.

The two networks use feeder-specific scenarios and inverter ratings. The illustrative best observed IEEE69 test run is not a seed average. The IEEE33 historical representative, common-projection, feature-ablation and reward-weight groups are not interchangeable. No summary has been altered to make these groups agree.

The historical representative TD3 voltage RMSE lacks adequate retained raw voltage or equivalent squared-deviation evidence. It is not presented as verified in this package. This limitation is distinct from the independently documented three-seed TD3 common-projection experiment.

Original software-produced experiment records have been exported to general-purpose text formats. This export does not imply that the experiments were performed using different software. Runtime benchmarking is not included; reproducing a runtime claim would require its original timing boundaries, hardware and software disclosures, and a separate controlled execution.

Excluded material includes source code, policy/network weights, optimizer or replay state, training scripts and logs, full scenario arrays, raw sensitivity matrices and full interval-level action/voltage traces. These exclusions protect implementation resources and limit full code-level reproducibility. Further verification material, if appropriate, requires a separate author decision.
