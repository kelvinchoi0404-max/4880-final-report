# Numerical evidence

These CSV files provide machine-readable provenance for the values reported in
`main.tex`. Values are stored at higher precision than the rounded percentages
shown in the paper.

- `table_dataset_split.csv`: real/AI counts for train, validation, and test.
- `table_three_seed_summary.csv`: mean and sample standard deviation for the
  main baseline and distortion-aware comparison.
- `seed_paired_effects.csv`: seed-matched clean-AUC, transformed-AUC, and gap
  changes for seeds 42, 43, and 44.
- `bootstrap_effects.csv`: seed-42 source-level paired bootstrap estimates and
  95% confidence intervals from 2,000 resamples.
- `per_transform_seed_effects.csv`: per-seed effects for each fixed
  transformation and metric.
- `severity_auc_effects.csv`: three-seed AUC effects for every transformation
  family and severity level.
- `table_severity_summary.csv`: mean and sample standard deviation for all
  severity-sweep metrics.
- `table_augmentation_ablation.csv`: seed-42 single-component training
  comparison.

The CSVs are exports from the saved evaluation results. They are included for
verification and are not required to compile the LaTeX report.
