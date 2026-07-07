# Time Series Forecasting and Portfolio Optimization

## Project Overview

This project applies time series forecasting and portfolio optimization techniques to support investment decision-making for **Guide Me in Finance (GMF) Investments**. The objective is to forecast Tesla (TSLA) stock prices and use those insights to construct an optimized investment portfolio containing **TSLA**, **SPY**, and **BND**.

The project combines financial data analysis, statistical modeling, deep learning, and Modern Portfolio Theory (MPT) to evaluate market trends and develop a data-driven investment strategy.

---

## Objectives

* Collect historical financial data using the **YFinance** API.
* Clean and explore the data through Exploratory Data Analysis (EDA).
* Build and compare **ARIMA/SARIMA** and **LSTM** forecasting models.
* Forecast future Tesla stock prices.
* Optimize a portfolio using **Modern Portfolio Theory (MPT)**.
* Backtest the portfolio strategy against a benchmark.

---

## Dataset

Historical daily market data is collected from **Yahoo Finance** for the following assets:

| Asset                          | Ticker | Purpose                             |
| ------------------------------ | ------ | ----------------------------------- |
| Tesla                          | TSLA   | High-growth stock (forecast target) |
| Vanguard Total Bond Market ETF | BND    | Low-risk bond ETF                   |
| S&P 500 ETF                    | SPY    | Broad market benchmark              |

**Time Period:** January 1, 2015 – June 30, 2026

Available features include:

* Open
* High
* Low
* Close
* Adjusted Close
* Volume

---

## Project Workflow

### Task 1: Data Preprocessing & EDA

* Download historical market data
* Clean and validate the dataset
* Perform exploratory data analysis
* Calculate daily returns and rolling volatility
* Detect outliers
* Test stationarity using the Augmented Dickey–Fuller (ADF) test
* Calculate Value at Risk (VaR) and Sharpe Ratio

### Task 2: Time Series Forecasting

* Prepare chronological train/test datasets
* Build ARIMA/SARIMA models
* Build LSTM models
* Tune model parameters
* Compare models using MAE, RMSE, and MAPE

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* YFinance
* Statsmodels
* pmdarima
* TensorFlow / Keras
* Scikit-learn
* PyPortfolioOpt

---

## Expected Outcomes

* A complete exploratory data analysis notebook
* Forecasting models (ARIMA/SARIMA and LSTM)
* Future Tesla price forecasts
* An optimized investment portfolio
* Portfolio backtesting results
* Business insights and investment recommendations




