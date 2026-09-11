
# Record Concurrence — Analysis Pipeline

Data (FAOSTAT yield + CRU TS temperature + CROPGRIDS weights, derived country-year
panels `panelv7_*.xlsx`) are already shared on GitHub.
Figures are also shared.
Below are the analysis steps;
all steps are run from a single combined R script.

| Step | Description | Output |
|---|---|---|
| Step 00 | Data preparation | *(GitHub — already shared)* `panelv7_<crop>.xlsx` (8 files) |
| Step 01 | Main analysis: record definitions, Monte Carlo assessment of classical benchmark, Null A vs. Null B, sensitivity checks (min-10, block-resampling, detrending, FDR), spatial map (Moran's I, embedded legend) | `record_montecarlo/results/*.xlsx`, `record_montecarlo/plots/*` |
| Step 02 | Type-I error calibration — 5-scenario dependence grid | `type1_error_scenario_grid.xlsx` |
| Step 03 | Precipitation sensitivity (sorghum, trivariate temp+precip+yield) — Appendix A4 | `precipitation_sensitivity_sorghum.xlsx` |
| Step 04 | Block-resampling sensitivity (sorghum, maize, Null A) — Appendix A5 | `block_resampling_sensitivity.xlsx` |

**Note:** All steps (00–04) run from a single combined R script, top to bottom.
