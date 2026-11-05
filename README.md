# CVD-Risk-Prediction-Pipeline

Analysis code for "Machine learning identifies under-recognized predictors of 10-year mortality in older adults with
cardiovascular disease: a sex-specific analysis of a population-based longitudinal study of 18,603 participants"
(revised manuscript, The Journals of Gerontology, Series A).

## Data and environment

- The analysis uses linked 45 and Up Study data (Sax Institute) and was run inside the Secure Unified Research
  Environment (SURE). No data, participant-level outputs or trained models are included in this repository.
  Data can be requested from the Sax Institute with the appropriate approvals.
- Software used for the reported results: Python 3.11.9, scikit-learn 1.7.1, scikit-survival 0.25.0, LightGBM 4.6.0,
  XGBoost 2.0.3, lifelines 0.30.0, SHAP 0.48.0, pandas 2.3.2, numpy 2.2.0, scipy 1.16.1, matplotlib 3.10.6.

## Running

`CVD_revision_stepwise.ipynb` is run top to bottom. File paths and settings are in Section 1 (Cells 2-4);
`QUICK_TEST = True` gives a short test run. Aggregate tables and figures are written to `tables/` and `figures/`;
participant-level files are written to `participant_level/` and stay within SURE. Cell headers mark each cell as
original, original modified, or new, and state the change.

## Where the reported results come from

| Manuscript / supplement | Notebook |
|---|---|
| eTable 1 | Section 11, Cell 58 |
| eTable 3 | Section 11, Cell 59 |
| eTable 6a (C-index) | Section 6, Cells 22-28 and Cell 31 |
| eTables 6b and 6c, Figure 2 (10-year AUROC of all models) | Section 8, Cell 37 |
| Paired AUROC differences (Results; eTable 6c footnote) | Section 8, Cell 39 (LightGBM vs logistic regression and vs penalized Cox) |
| Table 1, eTable 6d (discrimination and calibration before and after Platt recalibration) | Section 9, Cells 42-43 |
| eTable 7 (operating characteristics, confusion matrices) | Section 9, Cell 46 |
| eFigures 1-5 | Section 9, Cells 45 and 47; Section 10, Cells 48-52 |
| Figure 3 and SHAP results in the text | Section 11, Cells 53, 54 and 56 |
| eTable 8 (internal validation) | Section 12, Cells 61-63 |
| eTable 9 (demographic, demographic + clinical and full LightGBM models; both sexes, 10 years) | Section 14, Cells 65-67 |
| eTable 10 (multiple imputation) | Section 16, Cells 70, 71 and 73 |
| eFigure 6 (ridge Cox hazard ratios) | Section 22, Cells 81-82 |
| Variable definition checks (SF-36 scale, CVD variables) | Section 23, Cells 84-86 |

The remaining sections and cells (for example Sections 6b, 6c, 13, 15, 17-21, Cell 83 and the additional
missing-data strategies in Cell 72) are exploratory checks that are not reported in the manuscript.
# CVD-Risk-Prediction-Pipeline
