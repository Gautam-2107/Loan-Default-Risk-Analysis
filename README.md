# Loan Default Risk Analysis and Prediction Using R

A data analysis and machine learning case study using R to explore loan default risk and compare predictive models.

## Project Overview

This project analyzes borrower and loan characteristics to understand patterns associated with loan default and builds classification models to predict whether a loan is likely to default.

## Objectives

- Explore the dataset and identify patterns associated with loan default.
- Clean and prepare the data for analysis and modeling.
- Visualize relationships between borrower characteristics, loan features, and default status.
- Build and evaluate predictive models using classification metrics.
- Examine model predictions with feature importance and a local explanation example.

## Dataset

The project uses the **Credit Risk Dataset** (`credit_risk_dataset.csv`), containing borrower details, loan information, credit history, and the target variable `loan_status`.

- `loan_status = 0`: non-default
- `loan_status = 1`: default


## Files

- `ids_casestudy.ipynb` — analysis notebook.
- `Loan_Default_Risk_Analysis_Report.Rmd` — R Markdown report.
- `credit_risk_dataset.csv` — dataset, only if redistribution is permitted.

Update these names if your local files use different filenames.

## Methods

The analysis includes data cleaning, exploratory data analysis, visualizations, statistical association tests, and classification modeling.

Models and evaluation approaches covered include:

- Logistic Regression
- Random Forest
- Accuracy, precision, recall, F1-score, and ROC-AUC
- A Random Forest probability-threshold experiment
- Random Forest feature importance
- A LIME explanation for an individual prediction

## Main Findings

- Default rates vary substantially across loan grades, with higher-risk grades showing higher observed default rates.
- Loan purpose, home ownership, and previous default history are associated with differences in observed default rates.
- Random Forest performed better than Logistic Regression on the reported test-set metrics in this project.
- Adjusting the Random Forest decision threshold changed the precision–recall trade-off.
- Feature importance and LIME are interpretability aids; they do not establish that a feature causes default.

## Model Results

Reported baseline test-set results:

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 86.19% | 75.54% | 54.48% | 0.6330 | 0.8639 |
| Random Forest (threshold 0.50) | 93.75% | 97.65% | 73.18% | 0.8366 | 0.9384 |

A separate Random Forest threshold experiment at 0.40 reported 93.64% accuracy, 94.67% precision, 75.16% recall, and an F1-score of 0.8379. This threshold was selected after examining test-set performance, so it should be treated as an experiment rather than an unbiased final model-selection result. A validation set would be preferable for choosing a threshold.

## Limitations

- Model performance depends on the dataset and the train/test split.
- Observed associations should not be interpreted as causal relationships.
- Threshold selection should be performed using validation data to avoid test-set leakage.
- The LIME example had a low reported explanation fit, so its individual feature contributions should be interpreted cautiously.
- Results may not generalize to other lending populations or time periods without further testing.

## Reproducibility

1. Obtain the dataset from its original source and place it in the project directory if permitted.
2. Open the notebook in Jupyter or VS Code and run the cells in order.
3. Open the `.Rmd` report in RStudio or another compatible R Markdown environment.
4. Confirm the file paths and install the R packages required by the code before running the analysis.

The report has not been independently verified by knitting it from start to finish. Review the file paths, package dependencies, and outputs before treating it as a fully reproducible report.

## Tools

- R
- R Markdown
- Jupyter Notebook
- VS Code / Git / GitHub

## Author

Gautam Raju 
CBIT
