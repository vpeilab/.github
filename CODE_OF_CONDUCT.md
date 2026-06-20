# Code of Conduct

**Version:** v1.0.0-alpha  
**Authority Level:** Constitutional  
**Status:** Draft  
**Maintainer:** @vpeilab/architecture-committee  
**Last Modified:** 2026-06-19

---

## 1. Pledge

We pledge to make VPEI Lab a space for rigorous, honest, and fearless inquiry. We do not pledge comfort, consensus, or courtesy at the expense of truth.

---

## 2. Standards

### 2.1 Intellectual Honesty

- Report negative results with the same care as positive ones. A failed Tier 4 experiment that rigorously follows protocol is more valuable than a successful Tier 1 with sloppy controls.
- Never omit baseline failures to make a result look better. If Baseline A passed and you did not report it, you are committing fraud.
- Never modify a protocol after seeing the data. If you change your failure threshold post-hoc, you are p-hacking.
- Never fabricate or selectively edit data. If you cannot reproduce a result, say so. Do not cherry-pick seeds.

### 2.2 Iron Law Compliance

- The Three Iron Laws are architectural invariants, not stylistic preferences.
- Violating them to "make the system work" is equivalent to data fabrication.
- Claiming compliance while bypassing the Reality Boundary is academic misconduct.

### 2.3 Respectful Disagreement

- Technical arguments are encouraged. Personal attacks are not.
- "Your architecture is wrong because X" is welcome.
- "You are stupid" is not.
- Ad hominem is a sign that you have no argument.

---

## 3. Enforcement

### 3.1 Violation Classes

| Class | Definition | Examples | Consequence |
|-------|------------|----------|-------------|
| I | Direct violation of an Iron Law | Leaking object coordinates to L2; loading pretrained weights in a Tier 3 experiment; using global backprop in the core system | Permanent ban from organization; public retraction of all affected work; prohibition from citing VPEI Lab affiliation |
| II | Procedural violation that compromises validity | Missing baselines; unlogged random seeds; unreproducible configs; post-hoc protocol modification | PR rejection; mandatory correction; 6-month experiment suspension |
| III | Documentation or style violation | Typos; incomplete API docs; inconsistent naming; heated but non-personal technical disputes | Standard review feedback; no punitive action |

### 3.2 Reporting Mechanism

| Channel | Visibility | Use For |
|---------|------------|---------|
| Public Issue in `vpeilab/.github` (`conduct` label) | Public | Class III violations; process questions; general disputes |
| Private Issue in `vpeilab/.github` | AC + ERB only | Class II violations; sensitive disputes; pre-publication concerns |
| `conduct@vpei.lab` | AC Chair + external ombudsperson | Class I violations; fraud allegations; whistleblower reports |

### 3.3 Adjudication Timeline

| Class | Investigation | Decision | Appeal |
|-------|---------------|----------|--------|
| I | 7 days | 14 days | None. AC decision is final. |
| II | 3 days | 7 days | 7 days to AC |
| III | N/A | PR review cycle | N/A |

### 3.4 Public Record

All Class I violations are documented in `vpeilab/docs/archive/violations/` with:

- The violated law.
- The evidence.
- The decision.
- The consequence.

This record is permanent and immutable. It is not deleted upon appeal or apology.

---

## 4. Dispute Resolution

### 4.1 Technical Disputes

Disputes about architecture, protocols, or experimental interpretation are resolved by:

1. Replication. The party claiming a result must replicate it under the challenger's observation.
2. If replication fails, the claim is withdrawn.
3. If replication succeeds, the challenger must either accept the result or propose a modified protocol that would falsify it.

### 4.2 Governance Disputes

Disputes about the Charter itself are resolved by:

1. Written appeal to the AC Chair.
2. AC vote within 14 days.
3. If the AC is deadlocked, the matter is escalated to an external ethics board (to be appointed).

---

## 5. Signature

By contributing to, accessing, or referencing any repository under the vpeilab GitHub organization, you acknowledge that you have read, understood, and agree to be bound by this Code of Conduct.

| | |
|---|---|
| **Code of Conduct:** | `CODE_OF_CONDUCT.md` |
| **Repository:** | `vpeilab/.github` |
| **Version:** | v1.0.0-alpha |
| **Status:** | Draft |
| **Authority:** | Constitutional |
| **Effective:** | 2026-06-19 |

---

> This Code of Conduct is subordinate to the Research Charter. In case of conflict, the Charter prevails.
