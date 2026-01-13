# AutoPricePredict

AutoPricePredict explores how vehicle characteristics relate to Manufacturer’s Suggested Retail Price (MSRP) using multiple linear regression, transformations, and interaction terms. The analysis is implemented in an R Markdown report that walks through data preparation, feature engineering, modeling, and diagnostic checks.

## Project contents

- `SM_GroupProject.Rmd`: The full R Markdown analysis with data prep, feature engineering (including one-hot encoding for `Market.Category`), model fitting, and diagnostics.
- `SM_GroupProject.pdf`: A rendered PDF version of the report.

## Data

The report expects a `data.csv` file in the project root. The dataset referenced in the report is a Kaggle automobile pricing dataset containing vehicle attributes (make, model, year, engine specifications, fuel economy, popularity) along with MSRP.

**Setup steps:**
1. Download the dataset from Kaggle (see the report for details on the exact source).
2. Save it as `data.csv` in the project root:
   ```
   /workspace/AutoPricePredict/data.csv
   ```

## Requirements

- R (4.x recommended)
- R packages:
  - `dplyr`
  - `tidyr`
  - `lmtest`
  - `MASS`
  - `knitr` (for rendering)
  - `rmarkdown` (for rendering)

Install dependencies in R if needed:

```r
install.packages(c("dplyr", "tidyr", "lmtest", "MASS", "knitr", "rmarkdown"))
```

## How to run the analysis

From the project root in R:

```r
rmarkdown::render("SM_GroupProject.Rmd")
```

This regenerates `SM_GroupProject.pdf` with the full report.

## Notes on the analysis

- The workflow samples 600 rows from the dataset, uses 500 for training and 100 for testing, and performs feature engineering for `Market.Category`.
- Multiple model specifications are tested, including log and Box–Cox transformations plus interaction terms.
- Model diagnostics include residual plots, Q-Q plots, and tests for heteroscedasticity and normality.

## License

This project is provided as-is for educational purposes.
