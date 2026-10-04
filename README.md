# CT4101 Machine Learning Portfolio Project - Bank Marketing

Module: CT4101 Machine Learning, University of Galway.

## Dataset

UCI Bank Marketing (bank-additional-full.csv, 41,188 records, 20 input features, binary target y).

Licence: CC BY 4.0. Source, citation and variable descriptions: see data/README.md.

## Folder structure

- notebooks/ - numbered notebooks, run in order (01_..., 02_...)
- src/ - reusable Python functions imported by the notebooks
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
- pip install -r requirements.txt

## Running the work

Open the notebooks in VS Code (or Jupyter), select the .venv kernel, and run each notebook top to bottom (Restart, then Run All) in numerical order.
