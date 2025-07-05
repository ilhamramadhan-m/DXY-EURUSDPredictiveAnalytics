# 💱 Interdependency Analysis and Forecasting of the US Dollar Index and EUR/USD Exchange Rate using Vector Autoregressive Model

## 📌 Background

The foreign exchange market is a key indicator of global economic conditions. The relationship between the **US Dollar Index (DXY)** and the **EUR/USD exchange rate** reflects interactions between two major economic powers: the United States and the European Union. Given the strong influence these currencies have on global trade and investment, understanding their interdependency and forecasting future movements is crucial for policy makers, investors, and financial analysts.

This project applies **Vector Autoregressive (VAR)** modeling to analyze and forecast the dynamics between the DXY and EUR/USD over a ten-year period (July 2015 – June 2025).

## 🛠 Methodology

The analysis includes the following steps:

1. **Data Acquisition**: Monthly data of DXY and EUR/USD from [Investing.com](https://www.investing.com/).
2. **Exploratory Analysis**: Visualization and descriptive statistics of both time series.
3. **Linearity Check**: Applying Terasvirta’s test to assess model suitability.
4. **Stationarity Tests**: Using Box-Cox transformation and Dickey-Fuller test to ensure stationarity in variance and mean.
5. **Granger Causality Test**: Evaluating whether past values of one series help predict the other.
6. **VAR Modeling**:

   * Lag selection based on AIC.
   * Parameter estimation using least squares.
7. **Diagnostic Checking**:

   * White noise test (Ljung-Box).
   * Multivariate normality test (Mardia’s test).
   * Heteroskedasticity test (ARCH-LM).
8. **Forecasting**: Predicting both series for the next 6 months.
9. **Model Evaluation**: Assessing forecast accuracy using Mean Absolute Percentage Error (MAPE).

## 📊 Key Insights

* The **VAR(3)** model was selected as optimal based on AIC criteria.
* **No direct causality** was found via Granger test, but lag-3 interdependencies exist between DXY and EUR/USD.
* Diagnostic tests confirmed that the residuals of the final model are white noise, normally distributed, and homoskedastic.
* Forecasting results show high accuracy with **MAPE of 2.95% for DXY** and **3.2% for EUR/USD**, indicating strong predictive power.
* The final model equations reveal that **both variables significantly influence each other at lag-3**, supporting the use of multivariate modeling in exchange rate forecasting.

This analysis demonstrates the effectiveness of VAR in capturing dynamic relationships in financial time series and provides a useful tool for market forecasting and economic decision-making.
