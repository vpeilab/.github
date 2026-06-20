<p align="center">
  <img src="https://github.com/vpeilab/.github/raw/main/profile/IMG_1211.jpeg" width="96" height="96" alt="VPEI Lab">
</p>

<h1 align="center">VPEI Lab</h1>
<p align="center"><b>Visual-Native Predictive Embodied Intelligence</b></p>

<p align="center">
  <a href="https://github.com/vpeilab/docs/blob/main/GOVERNANCE.md">Charter</a> •
  <a href="https://github.com/vpeilab/docs">Specs</a> •
  <a href="https://github.com/vpeilab/benchmarks">Benchmarks</a>
</p>

---

## What We Are Doing

We are building machines that learn the causal structure of the world **from scratch**—through embodied interaction, prediction error, and nothing else.

No pre-training on human datasets. No hand-crafted rewards. No ground truth leaked from the simulator.

If it works, it will be the first system to demonstrate that general intelligence can emerge from a closed, self-organizing loop of prediction and action.

If it fails, we will publish the failure with equal rigor.

---

## The Architecture

| Layer | Repository | Function |
|:-----:|:-----------|:---------|
| **L0** | [`embodied-env`](https://github.com/vpeilab/embodied-env) | Physics & sensors. The Reality Boundary. |
| **L1** | [`vss`](https://github.com/vpeilab/vss) | Visual-native symbol encoding. All modalities become images. |
| **L2** | [`dppcm`](https://github.com/vpeilab/dppcm) | Dual-pathway predictive coding. Ventral What + Dorsal Where. |
| **L3** | [`ltcp`](https://github.com/vpeilab/ltcp) | Local temporal causal plasticity. No global backprop. |
| **L4** | [`vpl`](https://github.com/vpeilab/vpl) | Predictive coding language & global workspace. |
| **L5** | [`gwt-consciousness`](https://github.com/vpeilab/gwt-consciousness) | Consciousness verification via efference copy. |

---

## The Three Iron Laws

These are not guidelines. They are architectural invariants. Violating them invalidates any experimental result.

1. **Reality Boundary.** Cognitive modules receive only pixels and actions. No coordinates, no labels, no collision events.
2. **Zero Pretraining.** Every causal learning experiment starts from random weights. Loading pre-trained parameters and claiming emergence is fraud.
3. **Local Learning Only.** Synaptic updates are local. Global backpropagation is permitted only in baseline models for comparison.

---

## The Four Tiers of Verification

We do not benchmark. We **falsify**.

| Tier | Phenomenon | Pass Criterion | Baselines Must Fail |
|:----:|:-----------|:---------------|:--------------------|
| **T1** | Active exploration without reward | Prediction error ↓ 80%; novelty focus ≥ 70% | PPO + Random |
| **T2** | Few-shot causal learning | Rule in ≤5 interactions; counterfactuals 100% | All statistical models |
| **T3** | Autonomous tool use & goal chaining | ≥3 self-generated goals; tool in ≤1000 steps | All RL agents |
| **T4** | Blind-box causality | Novel rule in ≤30 interactions; 100% reproduction | **Everything** |

If a system passes all four tiers while all baselines fail, it is intelligent.

---

## How to Engage

We do not accept feature requests. We accept:

- **Theoretical objections** that identify falsifiable contradictions in our architecture.
- **Experimental replications** that follow the four-tier protocol with full baseline controls.
- **Architectural proposals** that preserve the Iron Laws while improving capability.

Start here: [`docs/GOVERNANCE.md`](https://github.com/vpeilab/docs/blob/main/GOVERNANCE.md)

---

<p align="center">
  <i>We do not train models. We grow minds.</i><br>
  <i>Or we fail, and we publish the failure.</i>
</p>
