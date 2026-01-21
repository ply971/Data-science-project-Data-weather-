# Aswan Weather Data - Solar PV Output Prediction

This project analyzes weather data from Aswan, Egypt and builds regression
models to predict solar PV output. The work is done in a single Jupyter
notebook and covers data cleaning, feature engineering, visualization, and
model comparison.

## Dataset

Source file: `Datatset/Aswan Weather Data.csv`

Columns:
- Date
- AvgTemp
- AverageDew
- Humidity
- Wind
- Pressure
- Solar(PV)

## Project Structure

- `Project weather .ipynb` - main notebook (EDA + modeling)
- `Datatset/Aswan Weather Data.csv` - dataset
- `NOTEBOOK FILES/` - placeholder for exports (currently empty)

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install numpy pandas matplotlib seaborn scikit-learn scipy jupyter
```

## Run

```bash
jupyter notebook "Project weather .ipynb"
```

## Workflow Summary

- Fill missing `AvgTemp` values with forward fill
- Handle outliers (IQR clipping) and negative solar values
- Create seasonal features from the date
- Standardize numeric features
- Compare models: Linear, Polynomial (deg 2/3), Ridge, Lasso, Decision Tree,
  Random Forest
- Evaluate via MAE, MSE, RMSE, and R^2

## Results

Polynomial Regression (degree 2) performed best in the notebook run. See the
notebook for plots and metrics.

## Notes

The notebook currently reads `Aswan Weather Data.csv` from the working
directory. If you run it from repo root, update the path to
`Datatset/Aswan Weather Data.csv` or move the CSV to the root.
