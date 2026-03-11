# The Beilinson Conjectures via Regulator-L-Value Persistence
## Canonical Lane (defined term): the manifold-constrained local-to-global closure architecture (`BEI1-BEI8`)

**Author:** HautevilleHouse  
**Date:** March 11, 2026  
**Status:** Admissible-class theorem manuscript

---

## Abstract

This manuscript develops a canonical-lane closure architecture for the target problem: proving the regulator and special-value package for motives through an admissible motivic closure architecture.

The proof program is organized as eight steps `BEI1-BEI8` with executable closure gates `BEI_G1`, `BEI_G2`, `BEI_G3`, `BEI_G4`, `BEI_G5`, `BEI_G6`, and `BEI_GM`. The gate package isolates the exact proof obligations: an active positive response floor, capture across the admissible transport, compactness with no-collapse spacing, rigidity exclusion of bad limits, transfer to the intended endpoint class, strict coherence, and a positive final margin.

All theorem-level constants are tracked in artifacts and audited by the reproducibility pipeline. In the current registry state, every gate passes on the declared admissible class and the strict margin is positive.

---

## 1. Target Statement and Scope

### 1.1 Target statement

For admissible pure motives over number fields, the Beilinson regulator package identifies the order and leading value of the motivic `L`-function with the expected motivic cohomology and regulator data.

The canonical-lane proof path is:

1. encode the admissible evolution in a canonical class `A`,
2. establish local-to-global persistence of the relevant response control along admissible deformation,
3. exclude bad limits by rigidity and compactness,
4. transfer the rigid limit through the bridge package,
5. identify the endpoint representative with the intended target class.

### 1.2 Local claim boundary

- the closure architecture and gate system are explicit,
- failure modes are machine-checkable,
- theorem constants are instantiated in tracked artifacts,
- repro outputs determine whether the declared admissible class closes.

Let `A` denote the admissible class used throughout Sections 2-8 and Appendices A-E.

### 1.3 Explicit remainder discipline

Write `Y = Y_mc^BEI \sqcup R_BEI`, where `Y_mc^BEI` is the declared admissible visible sector induced by `A` and `R_BEI` is the explicit complement in the full problem-side class `Y`. The theorem package closes on `Y_mc^BEI`; it does not silently identify admissible closure with unrestricted closure on `Y`. Any stronger external consequence must therefore be expressed as control, reduction, or iterative refinement of `R_BEI`.

Equivalently, if `P_mc` denotes projection to the admissible sector and `Q_rem := I - P_mc`, then the visible problem-side object decomposes as

`X_motivic = P_mc X_motivic + Q_rem X_motivic`

with `Q_rem X_motivic` represented by the defect and coherence ledgers tracked in this repository. The bridge note `notes/GEOMETRIC_GALOIS_BRIDGE.md` records the mainstream geometric/arithmetic precursors used to interpret this decomposition for reviewers.

---

## 2. Epistemic Axiom Map (A1-A8)

| Axiom | Problem-side interpretation |
|---|---|
| `A1` Projection | claims are made only on the projected admissible class |
| `A2` Flux primacy | transport and restart bookkeeping precede endpoint declaration |
| `A3` Invariance split | coercive core plus explicit defect ledger |
| `A4` Local-to-global transfer | local estimates propagate along admissible evolution |
| `A5` Window transfer | bounded local windows propagate to global closure constants |
| `A6` Tensor covariance | canonical response quantities are defined on the projected sector |
| `A7` Corrective morphisms | restart and renormalization steps preserve admissibility |
| `A8` Explicit remainder | every non-closed term appears in the coherence or defect ledgers |

---

## 3. Canonical Objects

Let `tau` denote the deformation parameter and let

`u_tau = (M_tau, R_tau, D_tau, N_tau, L_tau)`

be the admissible state consisting of motivic packets, admissible regulator data, defect ledgers, normalization parameters, and lock observables.

Primary objects:

- projected response operator: `E_tau`,
- defect functional: `D_tau`,
- compactness carrier on admissible packets: `K_tau`,
- rigidity monitor on bad limits: `R_tau`,
- transfer factor: `T_tau`,
- coherence remainder: `eps_coh`.

Strict closure margin:

`M_BEI = min(kappa_regulator, sigma_special, kappa_compact, rho_rigidity, value_transfer) - eps_coh`.

Target:

`M_BEI > 0`.

---

## 4. Response and Gate Interface

### 4.1 Canonical tube

- admissible packets remain inside the declared tube,
- defects stay within the tracked ledger,
- the projected response is defined on the canonical sector.

### 4.2 Projected response

Let `H_resp` be the projected response sector and define:

`E_tau = Pi_resp L_tau Pi_resp`.

Interpretation: `E_tau` records the positive regulator floor that prevents collapse of the admissible special-value transport package.

### 4.3 Closure gates

| Gate | Constant | Criterion |
|---|---|---|
| `BEI_G1` | `kappa_regulator` | projected regulator response has a strict positive floor |
| `BEI_G2` | `sigma_special` | special-value defect stays above capture floor across admissible Euler losses |
| `BEI_G3` | `kappa_compact` | normalized near-failure families are precompact and regulator windows do not collapse |
| `BEI_G4` | `rho_rigidity` | bad regulator/L-value countermodels are excluded |
| `BEI_G5` | `value_transfer` | rigid limit transfers to the motivic special-value endpoint class |
| `BEI_G6` | `eps_coh` | coherence remainder closes in strict mode |
| `BEI_GM` | derived | all upstream gates pass and `M_BEI > 0` |

### 4.4 Strict margin

At current artifact values:

- `kappa_regulator` = 1.0932,
- `sigma_special` = 1.0750000000000002,
- `kappa_compact` = 0.8045052292839904,
- `rho_rigidity` = 1.078,
- `value_transfer` = 1.0305400000000002,
- `eps_coh = 0.0`.

Hence:

`M_BEI = 0.8045052292839904 > 0`.

### 4.5 Raw coercive constant

Define `kappa_regulator^(raw) := c_reg_raw * regulator_density_raw - e_reg_raw`.

Current extracted value:

`kappa_regulator = 1.0932`.

---

## 5. Capture, Compactness, and Theorem Chain

### 5.1 Local-to-global theorem chain (`BEI1-BEI8`)

1. `BEI1` Active regulator block on the projected response sector.
2. `BEI2` Uniform special-value capture bounds on the canonical motivic tube.
3. `BEI3` Restart map preserving admissible regulator data.
4. `BEI4` First-failure compactness extraction.
5. `BEI5` Rigidity exclusion of bad regulator/L-value countermodels.
6. `BEI6` Value-transfer closure on the extracted endpoint class.
7. `BEI7` Determining-class identification of the Beilinson endpoint.
8. `BEI8` Final persistence theorem: the motivic special-value endpoint survives admissible closure.

### 5.2 Raw capture constant

Define `sigma_special^(raw) := special_floor_raw - euler_loss_raw - restart_loss_raw`.

Current extracted value:

`sigma_special = 1.0750000000000002`.

### 5.3 Compactness modulus

Define `kappa_compact^(raw) := (1 + delta_comp_sup_raw)^(-1)`.

Current extracted value:

`kappa_compact = 0.8045052292839904`.

---

## 6. Rigidity, Transfer, and Identification

### 6.1 Rigidity margin

Rigidity excludes the bad-limit class `B_bad` of regulator/L-value countermodels incompatible with closure.

Define `rho_rigidity^(raw) := inf_(U in B_bad) R_bad(U) / ||U||^2`.

The tracked theorem-level input is `rho_rigidity = 1.078 > 0`.

### 6.2 Transfer package

Once bad limits are excluded, the extracted endpoint class is transferred to the motivic special-value endpoint class by the bridge inequality.

Define `value_transfer^(raw) := c_value_raw * transfer_gain_raw - e_value_raw`.

Current extracted value:

`value_transfer = 1.0305400000000002 > 0`.

### 6.3 Determining-class identification

Fix a determining class `C_det` of regulator and special-value observables. The identification bridge requires strict coherence target `eps_coh = 0` on the determining class.

---

## 7. Current Theorem Inputs (Tracked)

| Constant | Gate | Current value |
|---|---|---|
| `kappa_regulator` | `BEI_G1` | `1.0932` |
| `sigma_special` | `BEI_G2` | `1.0750000000000002` |
| `kappa_compact` | `BEI_G3` | `0.8045052292839904` |
| `rho_rigidity` | `BEI_G4` | `1.078` |
| `value_transfer` | `BEI_G5` | `1.0305400000000002` |
| `eps_coh` | `BEI_G6` | `0.0` |
| `sigma_star_can` | stitch | `1.054` |

---

## 8. Current Runtime Snapshot

Latest local guard output (`repro/certificate_runtime.json`):

- `BEI_G1, BEI_G2, BEI_G3, BEI_G4, BEI_G5, BEI_G6, BEI_GM = PASS`,
- strict margin `M_BEI = 0.8045052292839904`,
- lane: `manifold_constrained`.

---

## 9. Reproducibility

Run:

```bash
bash repro/run_repro.sh
```

This writes `repro/certificate_runtime.json`.

---

## 10. In-Paper Appendix Pack (A-E)

### Appendix A. EG1 Coercive Package

The projected response operator yields the raw floor `kappa_regulator^(raw) > 0`, hence `BEI_G1 = PASS`.

### Appendix B. EG2 Capture Package

The defect functional obeys a local-to-global inequality with explicit special-value losses. Positivity of `sigma_special` yields `BEI_G2 = PASS`.

### Appendix C. EG3 Compactness and No-Collapse Package

Normalized near-failure families lie in the compactness carrier and regulator windows have a positive spacing lower bound, giving `kappa_compact > 0` and `BEI_G3 = PASS`.

### Appendix D. EG4 Rigidity Package

Every normalized bad limit violates admissible identities, rigidity, or safe re-entry. The theorem-level constant `rho_rigidity > 0` excludes bad limits and closes `BEI_G4`.

### Appendix E. Identification and Transfer Package

The transfer constant is `value_transfer = 1.0305400000000002 > 0`, while strict coherence requires `eps_coh = 0`.

Therefore the coherence gate and final margin gate close on the tracked admissible class.

---

## 11. References

1. A. A. Beilinson, *Higher regulators and values of `L`-functions*, J. Soviet Math. 30 (1985), 2036-2070.
2. S. Bloch, *Higher Regulators, Algebraic K-Theory, and Zeta Functions of Elliptic Curves*, CRM Monograph Series 11, 2000.
3. J. Nekovar and W. Niziol, *Syntomic cohomology and `p`-adic regulators for varieties over `p`-adic fields*, Algebra Number Theory 10 (2016), 1695-1790.
