# CT4101 Machine Learning Portfolio Project - Bank Marketing

Module: CT4101 Machine Learning, University of Galway.

## Predicting Term Deposit Uptake in Bank Telemarketing
## Using only information available before a call is made, will a contacted client subscribe to a term deposit (yes/no)?

## Dataset

UCI Bank Marketing (bank-additional-full.csv, 41,188 records, 20 input features, binary target y).

Licence: CC BY 4.0. Source, citation and variable descriptions: see data/README.md.

## Folder structure

- notebooks/ - numbered notebooks, run in order (01_..., 02_...)
- src/ - reusable Python functions
- data/raw/ - original dataset, unmodified
- data/README.md - dataset source, licence and citation
- reports/ - milestone documents, final report and figures
- ASSISTANCE.md - declaration of external code, collaboration and AI assistance

## Setup

Tested with Python 3.14 on Windows 11.

- git clone https://github.com/MirjaWulff/ct4101-bank-marketing.git
- cd ct4101-bank-marketing
- python -m venv .venv
- .venv\Scripts\activate
- python -m pip install -r requirements.txt

## Running the work

Open the notebooks in VS Code (or Jupyter), select the .venv kernel, and run each notebook top to bottom (Restart, then Run All) in numerical order. The notebooks read the data from ../data/raw/, so run them from the notebooks/ folder (VS Code does this by default).

- notebooks/01_data_audit.ipynb - data audit: shape, variable types, missing values, duplicates, target distribution, outliers.
- notebooks/02_baseline.ipynb - cleaning, train/test split and cross-validation design, preprocessing pipeline, baseline results.

## Evaluation design

- 80/20 stratified train/test split (random_state=42). The test set is only used once, for the final model.
- 5-fold stratified cross-validation on the training set. Preprocessing is inside a scikit-learn Pipeline, so it is fitted on the training folds only.
- Main metric: F1. Also reported: ROC-AUC, precision, recall, accuracy.
- `duration` is removed because it is only known after the call (data leakage).

