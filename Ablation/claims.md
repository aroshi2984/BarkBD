# What this ablation supports

- Test set: 2149 images. Baseline `full_model`: 95.95%.
- Noise floor: +/-0.66 pp (SD of 6 baseline runs).
- 3 of 5 variants show no effect distinguishable from that noise.

## Supported
- `without_bark_pattern_convs` uses 52% fewer parameters with accuracy statistically indistinguishable from the full model. State this as *no measurable loss*, not as a gain.
- The architecture is not capacity-limited on this dataset: accuracy varies little across a wide parameter range, which points to a data-limited ceiling.

## NOT supported (yet)
- Any statement that a component *improves* accuracy. Every delta sits at or inside the noise floor.
- Any statement that removing a component *improves* accuracy. Selecting the best of several noisy runs produces an apparent gain of this size by construction.
- Stacking removals. This is a one-factor-at-a-time design; combined models must be trained and measured, and parameter savings are not additive because removing one branch narrows the layers that follow.

## To strengthen
- Train 2-3 more `full_model` seeds and add them to EXTRA_BASELINE_ACCURACIES; that converts the noise floor from an estimate into a measured SD.
- Train the single most promising pruned model directly, with matched seeds, rather than inferring it from this table.