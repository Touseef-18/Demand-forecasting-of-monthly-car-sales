# Demand-forecasting-of-monthly-car-sales
The notebook is doing monthly car sales demand forecasting using two approaches:

1.LSTM (Deep Learning Model)

2.SARIMA (Seasonal ARIMA - Time Series Regression)
1. LSTM Section
Preprocessing:
Convert Month to datetime and use it as an index.

Normalize sales values to using MinMaxScaler.

Create time window sequences (12 months history → next month target).
Results:
Training converges well; Validation loss improves steadily.

Plot: Predicted vs Actual sales for the test set.

The LSTM captures seasonality and trends in the car sales data.

2. SARIMA Section
Approach:
Uses statsmodels SARIMAX model.

Detects and sets seasonality period (12 months).

Configured with (p,d,q) and seasonal (P,D,Q,12) values determined heuristically.

Output:
SARIMA forecasts next 12 months beyond the dataset.

Produces a forecast plot showing actual sales + f
