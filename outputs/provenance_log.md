# CIF Device Generator — Provenance Log

Append-only record of design decisions, verifications, calibrations, and
reviewer sign-offs for the CIF Device Generator research program.

**Specification references:** HANDOFF.md, ADDENDUM_1.md, ADDENDUM_2.md.

**Format conventions:**

- Each entry has an ISO-8601 timestamp, subject line, author, and body.
- Numerical calibrations include the source data file or experimental run ID.
- Reviewer sign-offs cite the reviewer and the document/section reviewed.
- PDF verifications quote the specific caption or text fragment verified.

Do not edit entries once written. Corrections to a prior entry are themselves
new entries that reference the prior timestamp.



---

### 2026-04-30T09:30:19 — v2 notebook shell constructed; kernel imported and stamps verified

**Author:** v2 notebook shell build

The v2 notebook (`CIF_Generator_v2.ipynb`) was constructed per the
plan in Addendum 2 Section 6. Phase One cells 1-77 (Blocks 1-6, fluidic
kernel) were imported verbatim from `CIF_Generator_5_.ipynb`. The six kernel
regression stamps were verified against the handoff's stated values and all
six matched bit-identically:

| Block | Stamp |
|---|---|
| 1 | cba945bf33cb4940 |
| 2 | 1f556ff8640db8bd |
| 3 | c4df786ff256aaf1 |
| 4 | 4b554b7f780857a3 |
| 5 | 8b5fed00afaf1044 |
| 6 | eb02d4e2d3699bc7 |

Post-kernel additions in this notebook: explicit InletCondition enum
(Addendum 2 Correction 13), Dinh variant catalog restructure with
verification guard (Addendum 2 Correction 12, pending PDF verification),
provenance log initialization (this entry).

No downstream bridge work has begun. Bridge One, Bridge Two, Bridge Three,
Bridge Four, and Bridge Five scaffolds follow but contain no implementation
content until their respective closures produce the required inputs.



---

### 2026-04-30T09:30:20 — Dinh 2024 Fig 2 caption verified (Addendum 2 Correction 12 resolved)

**Author:** Block 7a execution

The Dinh 2024 Figure 2 caption was verified directly from the PDF.

**Caption fragment (verbatim):**

> Width of the meandering side channel segments was 28 μm. Width of each side channel at the start of the linear section was wS(in) = 21 μm (for all values of f*gap), widening near the outlet to wS(out) = 44 μm, 48 μm, and 57 μm for f*gap values of 1.04 × 10⁻⁴, 1.12 × 10⁻⁴, and 1.28 × 10⁻⁴, respectively. All filtration gaps in the linear section were 19 μm-wide. The middle channel narrowed from 75 μm near the inlet to 52 μm near the outlet in all designs. Depth of all channels was 140 μm. The scale bars are 50 μm.

**All values match the notebook's reference device catalog:**
- meander_width = 28 μm ✓
- ws_start = 21 μm (all variants) ✓
- gap_size = 19 μm ✓
- wc_start = 75 μm, wc_end = 52 μm ✓
- depth = 140 μm ✓
- Variant 1 (f*_gap=1.04e-4): ws_out = 44 μm ✓
- Variant 2 (f*_gap=1.12e-4): ws_out = 48 μm ✓
- Variant 3 (f*_gap=1.28e-4): ws_out = 57 μm ✓

DINH_VARIANTS_PAIRING_VERIFIED set to True.
Downstream Bridge Four validators may now trust the pairing.


---

### 2026-04-30T15:06:25 — v2 notebook shell constructed; kernel imported and stamps verified

**Author:** v2 notebook shell build

The v2 notebook (`CIF_Generator_v2.ipynb`) was constructed per the
plan in Addendum 2 Section 6. Phase One cells 1-77 (Blocks 1-6, fluidic
kernel) were imported verbatim from `CIF_Generator_5_.ipynb`. The six kernel
regression stamps were verified against the handoff's stated values and all
six matched bit-identically:

| Block | Stamp |
|---|---|
| 1 | cba945bf33cb4940 |
| 2 | 1f556ff8640db8bd |
| 3 | c4df786ff256aaf1 |
| 4 | 4b554b7f780857a3 |
| 5 | 8b5fed00afaf1044 |
| 6 | eb02d4e2d3699bc7 |

Post-kernel additions in this notebook: explicit InletCondition enum
(Addendum 2 Correction 13), Dinh variant catalog restructure with
verification guard (Addendum 2 Correction 12, pending PDF verification),
provenance log initialization (this entry).

No downstream bridge work has begun. Bridge One, Bridge Two, Bridge Three,
Bridge Four, and Bridge Five scaffolds follow but contain no implementation
content until their respective closures produce the required inputs.



---

### 2026-04-30T15:06:26 — Dinh 2024 Fig 2 caption verified (Addendum 2 Correction 12 resolved)

**Author:** Block 7a execution

The Dinh 2024 Figure 2 caption was verified directly from the PDF.

**Caption fragment (verbatim):**

> Width of the meandering side channel segments was 28 μm. Width of each side channel at the start of the linear section was wS(in) = 21 μm (for all values of f*gap), widening near the outlet to wS(out) = 44 μm, 48 μm, and 57 μm for f*gap values of 1.04 × 10⁻⁴, 1.12 × 10⁻⁴, and 1.28 × 10⁻⁴, respectively. All filtration gaps in the linear section were 19 μm-wide. The middle channel narrowed from 75 μm near the inlet to 52 μm near the outlet in all designs. Depth of all channels was 140 μm. The scale bars are 50 μm.

**All values match the notebook's reference device catalog:**
- meander_width = 28 μm ✓
- ws_start = 21 μm (all variants) ✓
- gap_size = 19 μm ✓
- wc_start = 75 μm, wc_end = 52 μm ✓
- depth = 140 μm ✓
- Variant 1 (f*_gap=1.04e-4): ws_out = 44 μm ✓
- Variant 2 (f*_gap=1.12e-4): ws_out = 48 μm ✓
- Variant 3 (f*_gap=1.28e-4): ws_out = 57 μm ✓

DINH_VARIANTS_PAIRING_VERIFIED set to True.
Downstream Bridge Four validators may now trust the pairing.


---

### 2026-05-07T13:19:41 — v2 notebook shell constructed; kernel imported and stamps verified

**Author:** v2 notebook shell build

The v2 notebook (`CIF_Generator_v2.ipynb`) was constructed per the
plan in Addendum 2 Section 6. Phase One cells 1-77 (Blocks 1-6, fluidic
kernel) were imported verbatim from `CIF_Generator_5_.ipynb`. The six kernel
regression stamps were verified against the handoff's stated values and all
six matched bit-identically:

| Block | Stamp |
|---|---|
| 1 | cba945bf33cb4940 |
| 2 | 1f556ff8640db8bd |
| 3 | c4df786ff256aaf1 |
| 4 | 4b554b7f780857a3 |
| 5 | 8b5fed00afaf1044 |
| 6 | eb02d4e2d3699bc7 |

Post-kernel additions in this notebook: explicit InletCondition enum
(Addendum 2 Correction 13), Dinh variant catalog restructure with
verification guard (Addendum 2 Correction 12, pending PDF verification),
provenance log initialization (this entry).

No downstream bridge work has begun. Bridge One, Bridge Two, Bridge Three,
Bridge Four, and Bridge Five scaffolds follow but contain no implementation
content until their respective closures produce the required inputs.



---

### 2026-05-07T13:19:41 — Dinh 2024 Fig 2 caption verified (Addendum 2 Correction 12 resolved)

**Author:** Block 7a execution

The Dinh 2024 Figure 2 caption was verified directly from the PDF.

**Caption fragment (verbatim):**

> Width of the meandering side channel segments was 28 μm. Width of each side channel at the start of the linear section was wS(in) = 21 μm (for all values of f*gap), widening near the outlet to wS(out) = 44 μm, 48 μm, and 57 μm for f*gap values of 1.04 × 10⁻⁴, 1.12 × 10⁻⁴, and 1.28 × 10⁻⁴, respectively. All filtration gaps in the linear section were 19 μm-wide. The middle channel narrowed from 75 μm near the inlet to 52 μm near the outlet in all designs. Depth of all channels was 140 μm. The scale bars are 50 μm.

**All values match the notebook's reference device catalog:**
- meander_width = 28 μm ✓
- ws_start = 21 μm (all variants) ✓
- gap_size = 19 μm ✓
- wc_start = 75 μm, wc_end = 52 μm ✓
- depth = 140 μm ✓
- Variant 1 (f*_gap=1.04e-4): ws_out = 44 μm ✓
- Variant 2 (f*_gap=1.12e-4): ws_out = 48 μm ✓
- Variant 3 (f*_gap=1.28e-4): ws_out = 57 μm ✓

DINH_VARIANTS_PAIRING_VERIFIED set to True.
Downstream Bridge Four validators may now trust the pairing.


---

### 2026-05-08T13:49:07 — v2 notebook shell constructed; kernel imported and stamps verified

**Author:** v2 notebook shell build

The v2 notebook (`CIF_Generator_v2.ipynb`) was constructed per the
plan in Addendum 2 Section 6. Phase One cells 1-77 (Blocks 1-6, fluidic
kernel) were imported verbatim from `CIF_Generator_5_.ipynb`. The six kernel
regression stamps were verified against the handoff's stated values and all
six matched bit-identically:

| Block | Stamp |
|---|---|
| 1 | cba945bf33cb4940 |
| 2 | 1f556ff8640db8bd |
| 3 | c4df786ff256aaf1 |
| 4 | 4b554b7f780857a3 |
| 5 | 8b5fed00afaf1044 |
| 6 | eb02d4e2d3699bc7 |

Post-kernel additions in this notebook: explicit InletCondition enum
(Addendum 2 Correction 13), Dinh variant catalog restructure with
verification guard (Addendum 2 Correction 12, pending PDF verification),
provenance log initialization (this entry).

No downstream bridge work has begun. Bridge One, Bridge Two, Bridge Three,
Bridge Four, and Bridge Five scaffolds follow but contain no implementation
content until their respective closures produce the required inputs.



---

### 2026-05-08T13:49:07 — Dinh 2024 Fig 2 caption verified (Addendum 2 Correction 12 resolved)

**Author:** Block 7a execution

The Dinh 2024 Figure 2 caption was verified directly from the PDF.

**Caption fragment (verbatim):**

> Width of the meandering side channel segments was 28 μm. Width of each side channel at the start of the linear section was wS(in) = 21 μm (for all values of f*gap), widening near the outlet to wS(out) = 44 μm, 48 μm, and 57 μm for f*gap values of 1.04 × 10⁻⁴, 1.12 × 10⁻⁴, and 1.28 × 10⁻⁴, respectively. All filtration gaps in the linear section were 19 μm-wide. The middle channel narrowed from 75 μm near the inlet to 52 μm near the outlet in all designs. Depth of all channels was 140 μm. The scale bars are 50 μm.

**All values match the notebook's reference device catalog:**
- meander_width = 28 μm ✓
- ws_start = 21 μm (all variants) ✓
- gap_size = 19 μm ✓
- wc_start = 75 μm, wc_end = 52 μm ✓
- depth = 140 μm ✓
- Variant 1 (f*_gap=1.04e-4): ws_out = 44 μm ✓
- Variant 2 (f*_gap=1.12e-4): ws_out = 48 μm ✓
- Variant 3 (f*_gap=1.28e-4): ws_out = 57 μm ✓

DINH_VARIANTS_PAIRING_VERIFIED set to True.
Downstream Bridge Four validators may now trust the pairing.


---

### 2026-05-09T13:41:45 — v2 notebook shell constructed; kernel imported and stamps verified

**Author:** v2 notebook shell build

The v2 notebook (`CIF_Generator_v2.ipynb`) was constructed per the
plan in Addendum 2 Section 6. Phase One cells 1-77 (Blocks 1-6, fluidic
kernel) were imported verbatim from `CIF_Generator_5_.ipynb`. The six kernel
regression stamps were verified against the handoff's stated values and all
six matched bit-identically:

| Block | Stamp |
|---|---|
| 1 | cba945bf33cb4940 |
| 2 | 1f556ff8640db8bd |
| 3 | c4df786ff256aaf1 |
| 4 | 4b554b7f780857a3 |
| 5 | 8b5fed00afaf1044 |
| 6 | eb02d4e2d3699bc7 |

Post-kernel additions in this notebook: explicit InletCondition enum
(Addendum 2 Correction 13), Dinh variant catalog restructure with
verification guard (Addendum 2 Correction 12, pending PDF verification),
provenance log initialization (this entry).

No downstream bridge work has begun. Bridge One, Bridge Two, Bridge Three,
Bridge Four, and Bridge Five scaffolds follow but contain no implementation
content until their respective closures produce the required inputs.



---

### 2026-05-09T13:41:45 — Dinh 2024 Fig 2 caption verified (Addendum 2 Correction 12 resolved)

**Author:** Block 7a execution

The Dinh 2024 Figure 2 caption was verified directly from the PDF.

**Caption fragment (verbatim):**

> Width of the meandering side channel segments was 28 μm. Width of each side channel at the start of the linear section was wS(in) = 21 μm (for all values of f*gap), widening near the outlet to wS(out) = 44 μm, 48 μm, and 57 μm for f*gap values of 1.04 × 10⁻⁴, 1.12 × 10⁻⁴, and 1.28 × 10⁻⁴, respectively. All filtration gaps in the linear section were 19 μm-wide. The middle channel narrowed from 75 μm near the inlet to 52 μm near the outlet in all designs. Depth of all channels was 140 μm. The scale bars are 50 μm.

**All values match the notebook's reference device catalog:**
- meander_width = 28 μm ✓
- ws_start = 21 μm (all variants) ✓
- gap_size = 19 μm ✓
- wc_start = 75 μm, wc_end = 52 μm ✓
- depth = 140 μm ✓
- Variant 1 (f*_gap=1.04e-4): ws_out = 44 μm ✓
- Variant 2 (f*_gap=1.12e-4): ws_out = 48 μm ✓
- Variant 3 (f*_gap=1.28e-4): ws_out = 57 μm ✓

DINH_VARIANTS_PAIRING_VERIFIED set to True.
Downstream Bridge Four validators may now trust the pairing.
