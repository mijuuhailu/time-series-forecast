
# Financial Time Series Forecasting and Portfolio Optimization

## Project Overview

This project applies machine learning, statistical forecasting, and Modern Portfolio Theory (MPT) to analyze financial markets and optimize an investment portfolio. Historical market data was collected using the Yahoo Finance API and used to forecast asset prices, evaluate forecasting models, construct an optimal portfolio, and validate the strategy through backtesting.

The project follows the investment workflow used by financial analysts:

1. Collect and preprocess historical market data.
2. Explore trends, volatility, and statistical properties.
3. Build forecasting models.
4. Forecast future market movements.
5. Optimize a portfolio using Modern Portfolio Theory.
6. Evaluate the strategy through historical backtesting.

---

## Business Objective

Guide Me in Finance (GMF) Investments aims to improve investment decision-making by combining time series forecasting with portfolio optimization.

Rather than predicting exact stock prices for trading, the forecasts are used as an input into portfolio construction, helping balance expected return and investment risk.

---

## Assets Used

| Asset | Ticker | Description |
|--------|--------|-------------|
| Tesla | TSLA | High-growth technology stock |
| Vanguard Total Bond Market ETF | BND | Low-risk U.S. bond ETF |
| SPDR S&P 500 ETF | SPY | Broad U.S. equity market ETF |

Historical data covers:

**January 1, 2015 – June 30, 2026**

---

# Project Structure

```
Task 1
│
├── Data Collection
├── Data Cleaning
├── Exploratory Data Analysis
├── Stationarity Testing
└── Risk Metrics

Task 2
│
├── ARIMA Forecasting
├── LSTM Forecasting
└── Model Comparison

Task 3
│
├── Future Price Forecasting
├── Confidence Intervals
└── Trend Analysis

Task 4
│
├── Expected Return Estimation
├── Covariance Matrix
├── Efficient Frontier
└── Portfolio Optimization

Task 5
│
├── Strategy Backtesting
├── Benchmark Comparison
└── Performance Evaluation
```

---

# Task 1 — Data Preprocessing & Exploratory Analysis

Completed:

- Downloaded historical data using **yfinance**
- Cleaned missing values
- Converted dates to time-series index
- Computed descriptive statistics
- Visualized historical closing prices
- Calculated daily returns
- Rolling mean and rolling volatility analysis
- Outlier detection
- Augmented Dickey-Fuller (ADF) stationarity testing
- Calculated Value at Risk (VaR)
- Calculated Sharpe Ratio

Key Findings:

- Tesla exhibits significantly higher volatility than SPY and BND.
- Daily returns for all assets are stationary.
- BND provides portfolio stability.
- SPY demonstrates long-term market growth with moderate risk.

---

# Task 2 — Time Series Forecasting

Two forecasting approaches were implemented.

## ARIMA

- Chronological train-test split
- Parameter selection
- Model fitting
- Forecast generation

Performance:

- MAE: **54.44**
- RMSE: **70.54**
- MAPE: **17.24%**

---

## LSTM

Implemented using TensorFlow/Keras.

Pipeline:

- Min-Max normalization
- Sliding window sequences (60 days)
- LSTM neural network
- Model training
- Test prediction


### Model Comparison for tesla

| Model | MAE | RMSE | MAPE |
|--------|----:|------:|------:|
| ARIMA | 54.44 | 70.54 | 17.24% |
| **LSTM** | **12.50** | **15.98** | **3.52%** |

The LSTM model significantly outperformed ARIMA and was selected for future forecasting.

---

# Task 3 — Future Forecasting

Using the trained LSTM model:

- Generated future forecasts
- Forecast horizon of approximately 12 months
- Visualized historical prices and forecasts
- Added approximate 95% confidence intervals using historical RMSE
- Performed trend analysis

Forecast uncertainty increases over time, illustrating the reduced reliability of long-term predictions.

---

# Task 4 — Portfolio Optimization

Modern Portfolio Theory (MPT) was used to construct an optimal investment portfolio.

Steps:

- Estimated Tesla expected return using the LSTM forecast
- Used historical annual returns for SPY and BND
- Computed annual covariance matrix
- Generated the Efficient Frontier
- Identified:
  - Maximum Sharpe Ratio Portfolio
  - Minimum Volatility Portfolio

Optimization was performed using **PyPortfolioOpt**.

The optimizer balanced expected return against investment risk to recommend an efficient asset allocation.

---

# Task 5 — Strategy Backtesting

The optimized portfolio was evaluated against a benchmark portfolio.

Benchmark:

- 60% SPY
- 40% BND

Performance evaluation included:

- Total Return
- Annualized Return
- Sharpe Ratio
- Maximum Drawdown
- Cumulative Return Visualization

This allowed comparison between the optimized strategy and a passive investment approach.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- yfinance
- statsmodels
- pmdarima
- TensorFlow / Keras
- scikit-learn
- PyPortfolioOpt

---

# Key Learning Outcomes

This project demonstrates:

- Financial data preprocessing
- Time series analysis
- Stationarity testing
- Statistical forecasting using ARIMA
- Deep learning forecasting using LSTM
- Forecast evaluation
- Risk measurement
- Portfolio optimization with Modern Portfolio Theory
- Efficient Frontier analysis
- Portfolio backtesting
- Investment performance evaluation

---

# Conclusion

This project integrates machine learning and financial theory to support investment decision-making. While forecasting future prices remains inherently uncertain due to market efficiency, combining LSTM forecasting with Modern Portfolio Theory provides a practical framework for constructing diversified portfolios and evaluating investment strategies. The results demonstrate that machine learning models can enhance financial analysis when used alongside sound portfolio management principles.