# Rainfall Prediction using Hybrid ML model

This repository contains the implementation of a hybrid rainfall forecasting model that combines SARIMAX (Seasonal Auto-Regressive Integrated Moving Average with eXogenous regressors) with Gradient Boosting Machines (GBM) for accurate monthly rainfall prediction. The approach is tailored for Indian monsoon seasonality and rainfall spikes, addressing both trend accuracy and extreme event prediction.

🧠 Designed for 20+ years of historical monthly rainfall data.
📈 Produces 5-year forecasts with realistic seasonality and spike behavior.

🧪 Key Features
Hybrid Forecasting Architecture

Base: SARIMAX for capturing linear trend and seasonality.

Residual Correction: GBM trained on lag, rolling stats, and seasonal features.

Meta-GBM optional for blending trend and spike models.

Spike Month Prioritization

July > August > September > June > October enforced using engineered features.

Forecast Evaluation

Metrics: RMSE, R², and optionally SMAPE.

Visualization: Year-wise forecast vs. actual plots.

Realistic Forecasting Behavior

Soft clipping of spike magnitudes using historical percentiles.

Forecast noise injection for interannual variability.


📉 Evaluation Metrics
Root Mean Squared Error (RMSE) : 1.18

Coefficient of Determination (R²) : 0.73

classification report accuracy: 0.78

🖼️ Screenshots
1. Sample Forecast vs Actual Plot
<img width="1241" height="382" alt="Screenshot 2025-06-28 003455" src="https://github.com/user-attachments/assets/b6b26262-402c-45b7-8c3f-8627135b83c1" />

2. Residual ACF/PACF Diagnostics
<img width="940" height="382" alt="image" src="https://github.com/user-attachments/assets/68a1d439-f2c6-4fb9-93b8-e11d48ae5d04" />

3. SARIMAX Fit and Residual Trend
<img width="940" height="414" alt="image" src="https://github.com/user-attachments/assets/5b90c9ed-cb61-4f05-9f6d-7564dd80dc91" />

4. Forecast for future 5-year rainfall
<img width="940" height="378" alt="image" src="https://github.com/user-attachments/assets/447e6bc1-8b2f-4b1b-bfe0-b07628f27330" />

