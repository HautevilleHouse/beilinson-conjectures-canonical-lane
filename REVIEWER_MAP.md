# Reviewer Map

## Claim Scope

- Canonical-lane claim: inside the `manifold_constrained` lane, if the theorem chain in this repository holds and the guard certificate passes, the repository-level closure claim is satisfied.
- Standard target claim: carried by the in-repo bridge theorems tying the lane to the target statement.
- External-strengthening rule: any statement beyond the admissible class must retain the explicit remainder carried by the defect/coherence ledgers; see `notes/GEOMETRIC_GALOIS_BRIDGE.md`.

## Theorem Dependency Chain

1. `EG1`: coercive response and active control floor.
2. `EG2`: capture and admissible continuation.
3. `EG3`: compactness and no-collapse spacing.
4. `EG4`: rigidity and transfer.
5. Identification bridge: strict coherence on the determining class.
6. Scalar closure: `BEI_G1, BEI_G2, BEI_G3, BEI_G4, BEI_G5, BEI_G6, BEI_GM` all `PASS`.

Primary files:

- `paper/BEILINSON_CONJECTURES_PREPRINT.md`
- `notes/EG1_public.md`
- `notes/EG2_public.md`
- `notes/EG3_public.md`
- `notes/EG4_public.md`
- `notes/IDENTIFICATION_BRIDGE.md`
- `notes/GEOMETRIC_GALOIS_BRIDGE.md`

## Closure Gates

| Gate | Constant | Description |
|------|----------|-------------|
| `BEI_G1` | `kappa_regulator` | projected regulator response has a strict positive floor |
| `BEI_G2` | `sigma_special` | special-value defect stays above capture floor across admissible Euler losses |
| `BEI_G3` | `kappa_compact` | normalized near-failure families are precompact and regulator windows do not collapse |
| `BEI_G4` | `rho_rigidity` | bad regulator/L-value countermodels are excluded |
| `BEI_G5` | `value_transfer` | rigid limit transfers to the motivic special-value endpoint class |
| `BEI_G6` | `eps_coh` | strict coherence / identification closure |
| `BEI_GM` | derived | final strict margin |

## Falsification Conditions

- `repro/certificate_runtime.json` has any non-`PASS` gate.
- `lane.active_lane != "manifold_constrained"`.
- `all_pass != true`.
- Any manifest hash mismatch under `repro/repro_manifest.json`.
- A verified counterexample to any EG theorem statement used in the paper.
