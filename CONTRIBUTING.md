# Contributing to VPEI Lab

This document is an admission protocol, not a welcome mat. VPEI Lab is a research program with binding epistemological constraints. If you are looking for a standard open-source project with feature requests and quick fixes, you are in the wrong place.

## 0. Read the Research Charter

If you have not read [docs/GOVERNANCE.md](https://github.com/vpeilab/docs/blob/main/GOVERNANCE.md), stop here. Nothing below will make sense without it.

## 1. Who May Contribute

We accept contributions from three categories:

| Category | Requirement | What They Do |
|----------|-------------|--------------|
| Researchers | Published work in predictive coding, embodied AI, or neuroscience | Challenge architecture, propose falsifiable objections, design experiments |
| Engineers | Can implement the architecture without violating Iron Laws | Build L0–L5 components, maintain interfaces, optimize performance |
| Skeptics | Can identify specific, falsifiable flaws | Open theory challenges, propose counter-experiments, find contradictions |

We reject contributions from:

- Those seeking to add "better text generation" or "faster inference" as goals.
- Those who propose ground truth shortcuts to make the system "work better."
- Those who submit experiments without baseline controls.

## 2. Contribution Types

### 2.1 Architecture Contribution (L0–L5)

- Must preserve all three Iron Laws.
- Must include interface contracts for adjacent layers.
- Must be accompanied by a falsification test: "If this change is wrong, what experiment would detect it?"

### 2.2 Experimental Contribution

- Must follow the four-tier protocol.
- Must include pre-registered hypothesis and explicit failure threshold.
- Must include complete reproduction package (`experiment.json`, `config/`, `src/`, `README.md`).

### 2.3 Theoretical Contribution

- Must identify a specific proposition in our architecture.
- Must provide either a mathematical proof or a concrete experimental design that could falsify it.
- "This seems wrong" is insufficient. "This is wrong because X violates Y, and here is the experiment to prove it" is required.

## 3. Branch Strategy

| Branch | Purpose | Merge Requirement |
|--------|---------|-------------------|
| `main` | Stable, reproducible experiments only | Architecture Committee approval |
| `dev` | Integration branch for cross-layer features | 2 maintainer reviews |
| `feat/<layer>-<description>` | Feature development | Layer maintainer review |
| `fix/<layer>-<description>` | Bug fixes | Layer maintainer review |
| `exp/<name>` | Experiment branches (ephemeral) | Not merged; archived after conclusion |

## 4. Commit Convention


Examples:

- `[L0] feat: add Rapier collision frame timing`
- `[L2] fix: correct cross-gating gradient for dorsal→ventral`
- `[L5] test: verify libet delay measurement under 200ms`
- `[L3] docs: update PC-DF communication protocol`

- `<LAYER>`: L0–L5, or `meta` for infrastructure.
- `<type>`: `feat`, `fix`, `test`, `docs`, `refactor`, `perf`, `chore`.

## 5. Pull Request Checklist

Every PR must satisfy all of the following. Unchecked items result in immediate rejection.

- [ ] I have read the Research Charter and understand the Three Iron Laws.
- [ ] **Reality Boundary:** My code does not leak ground truth (coordinates, labels, collision states) to cognitive modules.
- [ ] **Zero Pretraining:** If this is an experiment, weights were initialized randomly. No external checkpoint was loaded.
- [ ] **Local Learning:** Core system updates are local. Global backprop is used only in baseline models, clearly marked as `baseline_`.
- [ ] **Baseline Comparison:** My experiment includes both PPO (zero reward) and Random baselines under identical conditions.
- [ ] **Reproducibility:** Seeds, configs, and hardware specs are logged in `experiments/<name>/`.
- [ ] **Layer Isolation:** My code does not import from non-adjacent layers.
- [ ] **No Cross-Layer Gradients:** I have verified that no `loss.backward()` traverses the layer hierarchy in the core system.

## 6. Review Process

### 6.1 Automated Checks

CI enforces:

- No imports across layer boundaries in core modules.
- All experiment PRs include `experiment.json`.
- No `torch.load` of external checkpoints in core modules.
- All commits follow the convention.

### 6.2 Human Review

| PR Type | Reviewers Required |
|---------|-------------------|
| L0/L1 | 1 infrastructure team member |
| L2/L3 | 1 architecture committee + 1 experiment reviewer |
| L4/L5 | 2 architecture committee members |
| Tier 3+ experiment | Unanimous architecture committee approval |

### 6.3 Iron Law Violations

If a PR is found to violate an Iron Law:

- **Class I:** Immediate rejection. Contributor may be banned.
- **Class II:** Request changes. 6-month experiment suspension if repeated.
- **Class III:** Standard review feedback.

## 7. Communication

| Channel | Use For |
|---------|---------|
| GitHub Issues (`theory` label) | Technical debate and architecture challenges |
| GitHub Discussions (`benchmarks`) | Experiment coordination and replication planning |
| Private Issue in `.github` (`iron-law` label) | Urgent violation reports |
| contact@vpei.lab | Administrative inquiries only |

## 8. Signature

By opening a Pull Request in any vpeilab repository, you certify that you have read, understood, and agree to be bound by this document and the Research Charter.

> We do not accept contributions. We accept evidence.

