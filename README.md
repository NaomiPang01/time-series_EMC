# time-series_EMC
時間序列課程——期末報告（EMC）

# 📈 EMC Stock Time Series Analysis (2018–2022)

[![R](https://img.shields.io/badge/Language-R-blue.svg)](https://www.r-project.org/)
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()

This project presents a comprehensive time series analysis of EMC stock data from 2018 to 2022. The objective is to examine the statistical properties of the stock price and its returns, test for stationarity, verify financial stylized facts, and lay the groundwork for advanced volatility modeling (such as GARCH).

---

## 🛠️ Key Analysis Steps

1. **Data Transformation & Stationarity Testing**:
   - Converted closing prices into log returns, 1st differences, and 2nd differences.
   - Performed **Augmented Dickey-Fuller (ADF)** tests to check for stationarity.
   - *Result*: The 1st difference of return was found to be stationary and used for subsequent analysis.

2. **Autocorrelation Analysis**:
   - Analyzed **ACF** and **PACF** for returns, absolute returns, and squared returns.

3. **Stylized Facts of Financial Data**:
   - **Distribution**: Tested for normality using the **Jarque-Bera test** and evaluated skewness and kurtosis (revealing positive/negative skewness and fat-tailed distributions).
   - **Autocorrelation in Returns**: Checked via the **Ljung-Box test**.
   - **Volatility Clustering**: Analyzed rolling 1-month volatility to observe large/small return clustering.

---

## 📦 Required R Packages

Make sure you have the following libraries installed before running the R Markdown file:

```R
install.packages(c("quantmod", "lmtest", "dplyr", "PerformanceAnalytics", 
                   "ggplot2", "xts", "tidyverse", "feasts", "fable", 
                   "lubridate", "gridExtra", "tseries", "forecast", "rugarch"))
