# Statistics & Probability using Financial Dataset

A Jupyter notebook that applies core descriptive statistics, probability, and inferential statistics concepts to a financial dataset using Python.

## Overview

This notebook walks through an exploratory statistical analysis of a financial dataset, covering everything from basic data inspection to hypothesis testing and correlation analysis.

## Requirements

- Python 3.x
- Jupyter Notebook / JupyterLab

### Python Libraries
```
numpy
pandas
matplotlib
seaborn
scipy
```

Install dependencies with:
```bash
pip install numpy pandas matplotlib seaborn scipy
```

## Data

The notebook expects a CSV file at:
```
Downloads/Finance_data.csv
```

Update the `data_path` variable in the second cell if your file is located elsewhere:
```python
data_path = "Downloads/Finance_data.csv"
```

## What the Notebook Does

1. **Setup** – Imports required libraries (`numpy`, `pandas`, `matplotlib`, `seaborn`, `scipy.stats`) and sets the plotting style.
2. **Data Loading** – Reads the financial dataset into a pandas DataFrame and previews the first few rows.
3. **Data Inspection** – Uses `.info()`, `.shape`, `.columns`, and `.describe()` to understand structure, data types, and summary statistics.
4. **Central Tendency** – Computes mean, median, and mode for all numerical columns.
5. **Dispersion** – Computes variance, standard deviation, and range for all numerical columns.
6. **Distribution Visualization** – Plots histograms for all numerical variables to visualize their distributions.
7. **Outlier Detection** – Generates box plots for all numerical variables to spot outliers and compare spreads.
8. **Probability Estimation** – Calculates the empirical probability that a sample column's values exceed its mean.
9. **Z-Scores** – Computes standardized z-scores for a sample column to identify how far individual values deviate from the mean.
10. **Correlation Analysis** – Builds a correlation matrix and visualizes it as a heatmap to identify relationships between variables.
11. **Hypothesis Testing** – Runs a one-sample t-test (`scipy.stats.ttest_1samp`) to test whether the sample mean differs significantly from the population mean.

## How to Run

1. Place `Finance_data.csv` in the expected path (or update `data_path`).
2. Open the notebook:
   ```bash
   jupyter notebook "Statistics_&_Probability_using_Financial_Dataset.ipynb"
   ```
3. Run all cells in order (Cell → Run All).

## Notes

- The notebook currently analyzes `numerical_cols.columns[0]` as the "sample" column for probability, z-score, and t-test sections — update this if you want to analyze a different variable.
- Ensure your CSV contains numerical financial columns (e.g., prices, returns, volumes) for the statistical methods to be meaningful.
