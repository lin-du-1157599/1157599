# COMP647 Assignment 2 — Height Impact on Volleyball Performance

## Overview
- Research question: How does player height influence performance across positions (attack, block, defense) in VNL 2024?
- Key takeaway: Height most strongly benefits blocking (MB > OH ≈ O > S > L), moderately affects attacking, and has limited effect for setters/liberos.

## Data
- Source files (folder: `COMP647 Assessment 2 DATA/`):
  - `VNL2024Men_Players.csv` (name, position, height, birth year)
  - `VNL2024Men_Attackers.csv` (attack metrics)
  - `VNL2024Men_Blockers.csv` (block metrics)
  - `VNL2024Men_Scorers.csv` (scoring metrics)
  - `VNL2024Men_Setters.csv` (setter metrics)
  - `VNL2024Men_Servers.csv` (serving metrics)
  - `VNL2024Men_Receivers.csv` (reception metrics)

## Environment
- Python 3.10+
- Install dependencies:
  - `pip install -r requirements.txt`
  - Core libs: pandas, numpy, matplotlib, seaborn, scipy, statsmodels, jupyter
 - Recommended: use a virtual environment (`conda` or `venv`).
 - Jupyter kernel: if needed, install and select ipykernel for this env:
   - `pip install ipykernel` then choose the matching kernel in Jupyter/VS Code.

## How to run
- Open `COMP647_Assignment2_Height_Analysis.ipynb` in Jupyter/VS Code
- Run cells from top to bottom

## File structure
- `COMP647_Assignment2_Height_Analysis.ipynb` — main analysis
- `COMP647 Assessment 2 DATA/` — raw data CSVs
- `requirements.txt` — dependencies

## Methods (brief)
- Cleaning: remove duplicates; focus on relevant columns for merge/analysis.
- Missing values: median for numeric; mode for categorical; no imputation for Height/Birth_Year.
- Outliers: IQR for height outliers (Z-score computed for reference, not used to filter).
- EDA: distributions by position (height/age), correlations (heatmap, scatter by position).
- Correlation: Pearson correlation for Height vs key metrics (attack/block/total points).
- Statistical tests: one-way ANOVA for height differences across positions.

## Results (brief)
- Strongest positive link: height ↔ block efficiency (especially MB)
- Moderate: height ↔ attack efficiency
- Limited/negative: height ↔ reception/dig (liberos rely on technique/positioning)
- ANOVA: significant height differences across positions (p < 0.05)

## Notes
- Figures and tables are generated inside the notebook.

## Troubleshooting (quick)
- CSV path: keep the folder name `COMP647 Assessment 2 DATA/` unchanged (includes spaces).
- Kernel not found: install `ipykernel` in your env and select it in Jupyter/VS Code.
- Plots not showing: ensure cells run top-to-bottom; in VS Code, set Jupyter renderers enabled.
