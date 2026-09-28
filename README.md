# Predictive Analytics Project — Stock, Sales & Tips

## Project Summary
This project builds three different predictive analytics models on a synthetic dataset of a fictional company `INNOVATETECH`, a retail chain `BazaarMart`, and a restaurant `SpiceGarden`. The pipeline covers:

1. **Stock Price Prediction** using an LSTM neural network (INNOVATETECH closing prices)
2. **Sales Forecasting** using Holt-Winters Exponential Smoothing (Downtown store)
3. **Waiter Tips Regression** using Linear Regression, Ridge, and Random Forest
4. **Deployment** of the best tips pipeline using `joblib`

## Key Results
- **LSTM Stock Model:** RMSE = **$4.51** on held-out test period
- **Holt-Winters Sales Model:** RMSE = **137.5 units/day** on held-out 60 days
- **Waiter Tips Models:**
  | Model | R² |
  |-------|------|
  | Baseline (total_bill only) | **0.826** |
  | Ridge Regression | 0.821 |
  | Linear Regression (all features) | 0.821 |
  | Random Forest | 0.775 |
- **Best Tips Model:** Baseline + Ridge (Baseline surprisingly performed best)

## Dataset
The synthetic dataset `predictive_analytics_custom.xlsx` contains **three sheets**:
- **Stock_Prices:** 750 trading days of OHLC + volume for INNOVATETECH
- **Sales_Data:** 4 stores × 730 daily sales figures with trend + weekly/yearly seasonality
- **Waiter_Tips:** 300 restaurant bills with tip, party size, day, time, and demographics

## Installation
Install the required dependencies:
```bash
pip install pandas numpy scikit-learn statsmodels tensorflow matplotlib seaborn joblib openpyxl
