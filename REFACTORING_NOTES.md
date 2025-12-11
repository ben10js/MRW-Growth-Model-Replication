# Refactoring Notes

This repository was refactored significantly to meet professional software engineering and data science standards.

## Key Changes

### 1. Modular Directory Structure
- **Original**: Flat structure with mixed code and reports.
- **New**: `data/`, `notebooks/`, `reports/` separation (Cookiecutter Data Science style).
- **Reason**: Improves maintainability and clarity. Reviewers can easily find the logic steps.

### 2. Sequential Notebooks
- **Original**: Monolithic `mrw_final_code.ipynb`.
- **New**: Split into `01_data_preparation`, `02_model_estimation`, `03_visualization`.
- **Reason**: Decouples data cleaning from analysis. Makes debugging easier and the workflow logical.

### 3. Reproducibility
- **Original**: Hardcoded paths (e.g., `/content/drive/...`).
- **New**: Relative paths (`../data/raw/`).
- **Reason**: Allows anyone to clone the repo and run it immediately (once data is placed), essential for a "Replication" study.

### 4. Documentation
- Added a comprehensive `README.md` explaining the academic context and usage.
- Added `.gitignore` to prevent large data files from polluting the repo history.
