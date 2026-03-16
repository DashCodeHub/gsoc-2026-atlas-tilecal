# Optimal Filtering — Paper Reproduction

**Paper:** Fullana et al. (2005), *Optimal Filtering in the ATLAS Hadronic Tile Calorimeter*
ATL-TILECAL-2005-001 / IEEE TNS 53(4):2139, [DOI 10.1109/TNS.2006.877267](https://doi.org/10.1109/TNS.2006.877267)

---

## Notebook Structure

The notebook `tilecal_optimal_filtering_2005.ipynb` follows the paper section by section:

| Notebook section | Paper section | Topic |
|-----------------|---------------|-------|
| 1. Setup & Pulse Shape | §2 | TileCal reference pulse shape `h(t)` and its derivative `dh/dt` |
| 2. Noise Model | §3 | Autocorrelation matrix **R**, electronic + pile-up noise |
| 3. OF2 Weights | §3 | Optimal Filtering weights `a_i` (energy) and `b_i` (timing) from `R⁻¹` |
| 4. Reconstruction & Resolution | §4 | Energy and timing reconstruction on synthetic samples; resolution curves |
| 5. Quality Factor | §4 | χ² quality factor distribution to flag out-of-time pile-up |
| 6. CIS Calibration | §5 | Charge injection system linearity curve (ADC counts vs. injected charge) |

---

## Generated Figures

All figures are saved to `figures/` and correspond to the following paper figures:

| File | Paper figure | Description |
|------|-------------|-------------|
| `fig_shape_form_function.png` | Fig. 1 | Normalized pulse shape `h(t)` and derivative `dh/dt` |
| `fig_of_weights.png` | Fig. 2 | OF2 weights `a_i` and `b_i` for energy and timing |
| `fig_noise_analysis.png` | Fig. 3 | Noise autocorrelation matrix and spectrum |
| `fig_cis_calibration.png` | Fig. 4 | CIS calibration: ADC response vs. injected charge |
| `fig_cis_reconstruction.png` | Fig. 5 | Reconstructed energy vs. true energy (CIS) |
| `fig_quality_factor.png` | Fig. 6 | χ² quality factor distribution |
| `fig_physics_electron.png` | Fig. 7 | Energy resolution for electrons |
| `fig_physics_pion.png` | Fig. 8 | Energy resolution for pions |

---

## Notes

- All data is synthetic. The pulse shape is the standard TileCal reference shape parameterized in the paper.
- The OF2 algorithm uses 7 samples at 25 ns spacing (LHC bunch crossing period).
- Noise is modeled as Gaussian with the autocorrelation structure from Table 1 of the paper.
