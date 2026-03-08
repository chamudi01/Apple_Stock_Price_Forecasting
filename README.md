# Apple Stock Price Forecasting using ARIMA & SARIMA

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)
![TimeSeries](https://img.shields.io/badge/Model-Time%20Series-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## 📌 Project Overview

This project focuses on forecasting **Apple Inc. (AAPL) stock prices** using **time series forecasting models**.  
The study applies **ARIMA** and **SARIMA** models to historical Apple stock price data to analyze patterns and predict future price movements.

Time series forecasting helps investors and analysts understand potential market trends by analyzing historical data.

---

## 📊 Dataset

The dataset contains **historical Apple stock price data**.

### Main Features
- Date  
- Open Price  
- High Price  
- Low Price  
- Close Price  
- Adjusted Close Price  
- Volume  

For forecasting purposes, the **Close Price** is used as the main variable.

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed before modeling:

- Converted **Date column to datetime format**
- Set **Date as the index**
- Checked and handled **missing values**
- **Detected outliers and replaced them with mean values**
- Sorted the dataset chronologically
- Selected **Close Price** for forecasting
- Split the dataset into **training and testing sets**

---

## 📈 Stationarity Analysis

Time series models such as **ARIMA** require the data to be **stationary**.  
The **Augmented Dickey-Fuller (ADF) Test** was applied to verify stationarity.

If the series showed non-stationarity, **first-order differencing** was applied to stabilize the mean and remove trends.

After differencing, the series fluctuates around a constant mean, making it suitable for ARIMA modeling.

---

## 🔍 Model Identification

To determine the appropriate ARIMA parameters, the following plots were analyzed:

- **ACF (Autocorrelation Function)**
- **PACF (Partial Autocorrelation Function)**

These plots help determine suitable values for **p** and **q** parameters.

### Figures
- 📊 **Figure 7:** ACF Plot  
- 📊 **Figure 8:** PACF Plot  

---

## 🤖 Models Used

### ARIMA Model

The **AutoRegressive Integrated Moving Average (ARIMA)** model captures temporal dependencies in the data.

Components:

- **AR (p)** → Captures dependence on past values  
- **I (d)** → Removes non-stationarity through differencing  
- **MA (q)** → Captures noise and shock effects  

---

### SARIMA Model

The **Seasonal ARIMA (SARIMA)** model extends ARIMA by incorporating **seasonal patterns**.

Model components:

- Non-seasonal: **(p, d, q)**
- Seasonal: **(P, D, Q, s)**

Where:

- **P** → Seasonal autoregressive order  
- **D** → Seasonal differencing  
- **Q** → Seasonal moving average  
- **s** → Length of seasonal cycle  

SARIMA captures repeating patterns that may exist in stock price data.

---

## 📊 Model Evaluation

The forecasting models are evaluated using:

- **RMSE (Root Mean Squared Error)**
- **AIC (Akaike Information Criterion)**

Lower values indicate better model performance.

---

## 📉 Forecasting Results

The project generates visualizations including:

- Historical stock price trends
- ACF and PACF plots
- Model predictions vs actual values
- Future stock price forecasts

These visualizations help interpret the model performance.

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Jupyter Notebook

---

## 📌 Conclusion

This project demonstrates how **ARIMA and SARIMA time series models** can be applied to financial datasets for stock price forecasting.  

Although statistical models capture temporal patterns effectively, real-world stock prices are also influenced by external factors such as economic events, company news, and market sentiment.

---
