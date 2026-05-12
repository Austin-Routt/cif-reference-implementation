# CIF Reference Implementation

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Open-source Python pipeline for designing **Controlled Incremental Filtration (CIF)** microfluidic devices, with COMSOL 3-D Stokes validation of the Dinh 2024 V1 and V3 outlet geometries.

## Repository contents

```
.
├── CIF_Generator_v3_20.ipynb       Main Jupyter notebook
├── COMSOL/                         3-D Stokes outlet-cell artifacts
│   ├── v1 5gap coarse.docx            COMSOL report — Dinh V1, coarse mesh
│   ├── v1 5gap extra coarse.docx      COMSOL report — Dinh V1, extra-coarse mesh
│   ├── v3_5gap_coarse.docx            COMSOL report — Dinh V3, coarse mesh
│   ├── v3_5gap_extra_coarse.docx      COMSOL report — Dinh V3, extra-coarse mesh
│   └── *.mph, *.zip                   Source model files + archives
├── outputs/                        Generated figures + provenance_log.md
├── LICENSE
└── README.md
```

The COMSOL reports tabulate Q-fluxes and pressure samples from V1/V3 × coarse/extra-coarse mesh runs; Block 19 of the notebook transcribes those tables for post-processing. The `.mph` files reproduce the simulations from scratch in COMSOL Multiphysics 6.3 (CFD Module).

## Headline result

Under the 1-D pressure-equilibration assumption and the inlet condition $Q_s(0) = 0$, the volumetric filtrate fraction at a CIF outlet is given exactly by

$$ F \;=\; \frac{2\,R_c}{R_s + 2\,R_c} $$

where $R_c$ and $R_s$ are the per-pitch hydraulic resistances of the center and side channels at the outlet.

- **Closed-form vs. iterative recursion.** Matches the Gifford recursion across five reference devices in three architectural regimes (Gifford 2014 bead; Dinh 2024 V1/V2/V3; Xia 2016 RS-7) to $|\Delta F| \leq 2.35 \times 10^{-4}$.
- **3-D COMSOL Stokes at the Dinh outlets** (Block 19, computed from the transcribed Q-flux tables): matches published measurements within $1\sigma$:
  - V1: $F = 0.5070$ vs. paper $0.505 \pm 0.033$ $(+0.06\sigma)$
  - V3: $F = 0.6281$ vs. paper $0.649 \pm 0.036$ $(-0.58\sigma)$

## Quick start

Tested with Python 3.8.20, NumPy 1.24.4, SciPy 1.10+, Matplotlib 3.7.5, plus `ezdxf` (DXF photomask export), `sympy` (closed-form identity proof), and `jupyter`.

```bash
git clone https://github.com/Austin-Routt/cif-reference-implementation.git
cd cif-reference-implementation
pip install numpy scipy matplotlib ezdxf sympy jupyter
jupyter notebook CIF_Generator_v3_20.ipynb
```

Run the cells top-to-bottom. End-to-end execution produces the Gifford 2014 photomask (`gifford_2014_bead_device.dxf`) and the diagnostic figures already mirrored in `outputs/`. COMSOL is only needed if you want to re-run the `.mph` studies; the notebook itself reads the transcribed tables, not a live COMSOL solution.

## Validation

Validators are implemented as inline notebook checks (helper-function calls that print per-block pass/fail summaries — not a separate `pytest` suite). After a full top-to-bottom run, the §8.8 epilogue ("v3.20 POST-PRIORITY-B SUPPLEMENTARY AUDIT") reports the final state:

- **218 / 218 core validators** across 19 sub-blocks (geometry, manufacturability, PE convergence, numerical stability, dimensional consistency, mask integrity, COMSOL post-processing).
- **19 / 19 supplementary validators** (Priority-B fabrication-tolerance sweep, Xia RS-7 closed-form regression, channel-depth sensitivity, PE half-life cross-validation, effective $R_c / R_s$ from COMSOL).
- **19 regression stamps** (15 core + 4 supplementary). 13 are bit-identical across environments; 2 (Blocks 12 and 15) hash `scipy.sparse.linalg.spsolve` output and reproduce the v3.1 baseline to 12+ decimal places under documented BLAS/LAPACK portability.

An earlier audit cell (§8.5) prints an interim 9 supplementary / 16 stamp count from before the Priority-B blocks ran; the 19 / 19 / 19 figures in the §8.8 epilogue are the final state.

## Scope

The closed-form identity addresses the **volumetric throughput** (filtrate-fraction) design question only. The **size-cutoff** question is still handled by the iterative $f_{\text{gap}}$ calibration described in the source papers. The mask-layout (DXF) module currently produces the Gifford 2014 photomask only; generalized DXF for the remaining reference devices is a documented roadmap item.

## Source papers

- Gifford et al., *Lab on a Chip* **14**, 4496 (2014) — [doi:10.1039/c4lc00785a](https://doi.org/10.1039/c4lc00785a)
- Xia et al., *Scientific Reports* **6**, 35943 (2016) — [doi:10.1038/srep35943](https://doi.org/10.1038/srep35943), with [Author Correction (2022)](https://doi.org/10.1038/s41598-022-18449-5)
- Dinh et al., *Lab on a Chip* **24**, 913 (2024) — [doi:10.1039/D3LC00842H](https://doi.org/10.1039/D3LC00842H)

## Citation

The companion manuscript is in preparation. Until then, please cite this repository as:

```
Routt, A. H. (2026). CIF Reference Implementation v3.20.
https://github.com/Austin-Routt/cif-reference-implementation
```

## License

MIT — see [LICENSE](LICENSE).
