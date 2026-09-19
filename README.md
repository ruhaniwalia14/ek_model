# Coding Task: EK Model

Submission by Ruhani Walia

This README explains what is in the submission and where to find each part of the assignment.

## Contents at a glance

```
Applied Economics Incubator App/
├── README.md              this file
├── MainScript.ipynb       parts ii to v (code, results, written interpretation)
├── Part i                 handwritten derivation for part i
├── Background Notes/      my reading notes on the paper
├── Input/                 the two data files provided with the assignment
└── Output/                exported results per section
```

| Item | What it is |
|---|---|
| `Part i` | My handwritten derivation of the exact hat algebra system and the excess labor demand equation (2). Part i is a derivation, so it is not in the notebook. |
| `MainScript.ipynb` | Jupyter notebook containing parts ii, iii, iv and v: calibration, the counterfactual, real wages and regressions, and the change of transfer numeraire. |
| `Background Notes/` | Notes I made while reading the paper and working out the model. **Included for completeness only.** |
| `Input/` | All input files: `bilateral_trade_country.csv` and `country_list.csv`. |
| `Output/` | All output files, named by the section they belong to (see below). |

## The notebook: `MainScript.ipynb`

The notebook is organized by assignment item, with a table of contents with links at the top. Each part has a short description, commented code, and printed results. Parts iii, iv and v each end with a short written interpretation of the results.

### How to run the notebook

1. Set `input_path` in the first code cell to the location of the `Input` folder on your computer. Same for `Output`
2. Restart the kernel and use **Run All**. It runs in a few seconds (the solver converges in roughly 250 iterations).
3. Packages needed: `numpy`, `pandas`, `statsmodels`. `openpyxl` is optional (only for the Excel export).

## The `Output` folder

The main results are exported by section, so you can check them without reading through the whole notebook. The file names begin with the part they belong to.

| File | Part | Contents |
|---|---|---|
| `part2_X0_matrix.csv` | ii | The 41 x 41 bilateral trade matrix `X0` |
| `part2_income_to_spending.csv` | ii | Total spending, total sales, `y0`, and deficit/surplus label for each country |
| `part3_wage_changes.csv` | iii | Wage change `w_hat` and % change relative to the US for each country |
| `part3_convergence.csv` | iii | Maximum excess labor demand at each iteration of the solver |
| `part4_real_wage_expenditure.csv` | iv | Wage, price index, real wage and real expenditure changes for each country |
| `part4_regressions.csv` | iv | Results of the six regressions |
| `part5_comparison.csv` | v | Real wage and real expenditure under both transfer numeraires, their difference, and `y0` |
| `part5_regressions.csv` | v | Differences in outcomes regressed on the baseline transfer share, `1 - y0` |
| `settings_and_checks.csv` | all | θ, step size, tolerance, iterations and final error for the solver, and China's wage change under each scenario |
| `EK_model_results.xlsx` | all | All of the tables above, one sheet per table |
| `README.txt` | all | A one-line description of each output file |

The notebook itself contains the same results together with the code and explanations.