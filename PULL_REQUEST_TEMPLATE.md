## Summary

<!-- One sentence. What does this change? -->

## Layer(s) Affected

- [ ] L0: embodied-env
- [ ] L1: vss
- [ ] L2: dppcm
- [ ] L3: ltcp
- [ ] L4: vpl
- [ ] L5: gwt-consciousness
- [ ] Meta: governance / infrastructure

## Type

- [ ] Architecture change (affects interface contracts)
- [ ] Experimental contribution (follows four-tier protocol)
- [ ] Theoretical contribution (falsifiable objection or proof)
- [ ] Bug fix
- [ ] Documentation

## Iron Law Compliance

- [ ] **Reality Boundary:** I have verified that no coordinate, velocity, or object ID enters the cognitive module.
- [ ] **Zero Pretraining:** If this is an experiment, weights were initialized randomly. No external checkpoint was loaded.
- [ ] **Local Learning:** Core system updates are local. Global backprop is used only in baseline models, clearly marked as `baseline_`.
- [ ] **Baseline Comparison:** Includes PPO (zero reward) and Random baselines under identical conditions.
- [ ] **Reproducibility:** Seeds, configs, and hardware logged in `experiments/<name>/`.

## Review Checklist

- [ ] I have read the Research Charter.
- [ ] I understand that Iron Law violations result in permanent rejection regardless of technical merit.
- [ ] This PR does not break layer isolation (no cross-layer imports in core modules).
- [ ] This PR does not introduce global backpropagation in the core system.
- [ ] All new code includes tests or is marked with `TODO(test)`.
- [ ] Documentation updated (if applicable).

## Related

Closes #(issue) or References #(discussion)
