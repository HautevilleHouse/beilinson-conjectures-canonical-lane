# Canonical Routing Index (BEI)

| Gate | Main preprint location | Mirror note | Registry/artifact key(s) |
|---|---|---|---|
| `BEI_G1` | `Section 4`, `Appendix A` | `notes/EG1_public.md` | `kappa_regulator` |
| `BEI_G2` | `Section 5`, `Appendix B` | `notes/EG2_public.md` | `sigma_special` |
| `BEI_G3` | `Section 5`, `Appendix C` | `notes/EG3_public.md` | `kappa_compact` |
| `BEI_G4` | `Section 6.1`, `Appendix D` | `notes/EG4_public.md` | `rho_rigidity` |
| `BEI_G5` | `Section 6.2`, `Appendix E.4` | `notes/EG4_public.md` | `value_transfer` |
| `BEI_G6` | `Section 6.3`, `Appendix E.6` | `notes/IDENTIFICATION_BRIDGE.md` | `eps_coh` |
| `Bridge` | `Section 1.3`, `Section 6.3` | `notes/GEOMETRIC_GALOIS_BRIDGE.md` | `eps_coh`, defect/coherence ledgers, admissible remainder |
| `BEI_GM` | `Section 8`, `Appendix E.5` | `derived` | `all above keys` |

## Repro Routing

- Runner: `repro/run_repro.sh`
- Guard: `scripts/bei_closure_guard.py`
- Runtime certificate: `repro/certificate_runtime.json`
- Baseline certificate: `repro/certificate_baseline.json`
- Registry: `artifacts/constants_registry.json`
- Stitch constants: `artifacts/stitch_constants.json`
