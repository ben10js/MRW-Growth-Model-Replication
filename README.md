# MRW Growth Model Replication

## Overview
This project replicates and extends the seminal empirical analysis of **Mankiw, Romer, and Weil's (1992) "A Contribution to the Empirics of Economic Growth"**. By leveraging the Solow growth model augmented with human capital, this study reassesses the drivers of cross-country income differences using modern data from the **Penn World Table (PWT) 10.0**.

<img width="3000" height="1800" alt="human_capital_growth" src="https://github.com/user-attachments/assets/74bce678-cd2d-4254-983d-2b847b08ac91 style="display:inline-block;" />
<img width="3000" height="1800" alt="unconditional_convergence" src="https://github.com/user-attachments/assets/e9a97366-ed85-408f-87c1-c9860f20b39e style="display:inline-block;" />


## Key Features
- **Extended Time Series**: Analyzes data from 1960 to 2019 (original paper: 1960-1985).
- **Human Capital Augmentation**: Utilizes the PWT `hc` index (based on years of schooling and returns to education) instead of secondary school enrollment rates.
- **Convergence Analysis**: Tests for both unconditional and conditional convergence among 28 OECD countries.
- **Modern Stack**: Implemented in Python using `pandas` and `statsmodels`.

## Data Source
The primary data source is the **Penn World Table 10.0**.
- **Download**: [PWT 10.0 Website](https://www.rug.nl/ggdc/productivity/pwt/)
- **File**: `pwt100.xlsx`
- **Instruction**: Place the downloaded Excel file in the `data/raw/` directory.

## Project Structure
```text
MRW-Growth-Model-Replication/
├── data/
│   ├── raw/                # Place 'pwt100.xlsx' here
│   └── processed/          # Generated clean data (mrw_clean_data.csv)
├── notebooks/
│   ├── 01_data_preparation.ipynb  # Data loading, filtering, and variable calculation
│   ├── 02_model_estimation.ipynb  # OLS regression analysis (Solow & Augmented models)
│   └── 03_visualization.ipynb     # Convergence plots and figures
├── reports/
│   ├── figures/            # Saved plots
│   └── MRW_Report.md       # Full analysis report
└── README.md
```

## Usage
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/MRW-Growth-Model-Replication.git
   ```
2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the notebooks in order**:
   - `01_data_preparation.ipynb`: Generates the dataset.
   - `02_model_estimation.ipynb`: Runs the regressions.
   - `03_visualization.ipynb`: Creates the charts.

## Methodology
- **Textbook Solow Model**: Estimates the impact of savings and population growth on income.
- **Augmented Solow Model**: Includes human capital as an additional factor of production.
- **Unconditional Convergence**: Tests if poor countries grow faster than rich ones without controls.

## References
- Mankiw, N. G., Romer, D., & Weil, D. N. (1992). A Contribution to the Empirics of Economic Growth. *The Quarterly Journal of Economics*, 107(2), 407-437.
- Feenstra, R. C., Inklaar, R., & Timmer, M. P. (2015). The Next Generation of the Penn World Table. *American Economic Review*, 105(10), 3150-3182.
