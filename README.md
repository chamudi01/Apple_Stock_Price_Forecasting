🍎 Apple Stock Price Forecasting using ARIMA & SARIMA
📌 Project Overview

This project focuses on forecasting Apple Inc. (AAPL) stock prices using time series forecasting models. The study applies ARIMA and SARIMA models to historical Apple stock price data to identify patterns and generate future price predictions.

Time series forecasting plays a crucial role in financial analysis and investment decision-making. By modeling historical stock price behavior, the project aims to evaluate the effectiveness of statistical forecasting models for predicting future stock prices.

📊 Dataset

The dataset used in this project contains historical stock price information for Apple Inc. (AAPL).

Main attributes include:

Date

Open Price

High Price

Low Price

Close Price

Adjusted Close Price

Volume

The Close Price is used as the primary variable for time series forecasting.

🧹 Data Preprocessing

Several preprocessing steps were performed to prepare the dataset for modeling:

Converted the Date column to datetime format

Set Date as the index for time series analysis

Checked and handled missing values

Detected and replaced outliers using mean values

Sorted the dataset in chronological order

Selected the Close price for forecasting

Split the dataset into training and testing sets

These steps ensure the data is clean and suitable for time series modeling.

📈 Stationarity Analysis

Time series models such as ARIMA require the data to be stationary. The Augmented Dickey-Fuller (ADF) test was used to determine stationarity.

If the series was non-stationary, first-order differencing was applied to stabilize the mean and remove trends.

After differencing, the transformed series fluctuates around a constant mean, making it suitable for ARIMA modeling.

🔎 Model Identification

To determine the appropriate ARIMA parameters, the following plots were analyzed:

Autocorrelation Function (ACF)

Partial Autocorrelation Function (PACF)

These plots help identify the values of p (autoregressive) and q (moving average) parameters.

📊 Insert Figure: ACF Plot
📊 Insert Figure: PACF Plot

🤖 Models Used
ARIMA Model

The AutoRegressive Integrated Moving Average (ARIMA) model is used to capture temporal dependencies in the stock price data.

Model components:

AR (p): Captures dependence on previous values

I (d): Differencing to remove non-stationarity

MA (q): Captures error relationships

The ARIMA model is trained using historical closing prices and used to forecast future values.

SARIMA Model

The Seasonal ARIMA (SARIMA) model extends ARIMA by incorporating seasonal components.

Model components:

Non-seasonal: (p, d, q)

Seasonal: (P, D, Q, s)

Where:

P: Seasonal autoregressive order

D: Seasonal differencing

Q: Seasonal moving average

s: Length of seasonal cycle

SARIMA helps capture repeating patterns or periodic fluctuations in stock price movements.

📊 Model Evaluation

The models are evaluated using standard forecasting metrics:

RMSE (Root Mean Squared Error)

AIC (Akaike Information Criterion)

Lower RMSE values indicate better predictive performance.

📉 Forecast Visualization

The project generates visualizations including:

Historical stock price trends

ACF and PACF plots

Model predictions vs actual values

Future stock price forecasts

These visualizations help interpret the forecasting results.

🛠 Technologies Used

Python

Pandas

NumPy

Matplotlib

Statsmodels

Jupyter Notebook

📌 Conclusion

This project demonstrates how time series forecasting models such as ARIMA and SARIMA can be applied to financial datasets. The results show that statistical models can capture important temporal patterns in stock prices, although external factors such as market news and economic events may also influence stock behavior.
