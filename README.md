# 🧠 Real-Time Crypto Price & Direction Predictor 🚀

This project uses machine learning to predict **future price direction** of cryptocurrencies like **Bitcoin (BTC), Ethereum (ETH)**, and more. It includes real-time data ingestion, feature engineering, classification modeling (LightGBM), and evaluation using finance-relevant metrics.

---

## 📌 Table of Contents

- [🎯 Objective](#-objective)
- [🧩 Problem Statement](#-problem-statement)
- [📚 Data Source](#-data-source)
- [📊 Key Features](#-key-features)
- [🧠 Model Used](#-model-used)
- [📈 Evaluation Metrics](#-evaluation-metrics)
- [📍 Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [🔍 Performance Summary](#-performance-summary)

---

## 🎯 Objective

To build an **intelligent real-time prediction system** that forecasts whether the **next price movement** for a cryptocurrency will be **upward or downward**. The solution must work across multiple crypto symbols (BTC, ETH, XRP) and provide interpretable outputs via KPIs like **Precision**, **Recall**, and **AUC Score**.

---

## 🧩 Problem Statement

Traditional regression-based financial models are difficult to interpret in trading environments. This project addresses that gap by:
- **Converting continuous price prediction into classification** (up/down).
- Supporting **real-time data updates** and multiple crypto symbols.
- Using classification metrics more aligned with **investment decision-making**.

---

## 📚 Data Source

- **Source**: [CryptoCompare API](https://min-api.cryptocompare.com/)
- **Format**: JSON (real-time to CSV conversion)
- **Data Used**: Open, High, Low, Close, VolumeFrom, VolumeTo, Time

---

## 📊 Key Features
- 📡 **Live Data Fetch** from [CryptoCompare API](https://min-api.cryptocompare.com/)
- ⚙️ **Feature Engineering** using:
  - SMA (Simple Moving Average)
  - EMA (Exponential Moving Average)
  - RSI (Relative Strength Index)
  - Day, Month, Year, Day of Week
- 🧠 **Trained Models**: LightGBM, XGBoost, Random Forest
- 📊 **Visualizations**:
  - Actual vs Predicted Price Charts
  - Residual Plots
  - SHAP Feature Importance
  - Arrow-based Next Hour Price Movement
- 📋 **Robust Logging** and Exception Handling
- 📦 Ready for **deployment via Streamlit** or Flask
---

## 🧠 Model Used

| Model           | Description                                                       |
|----------------|-------------------------------------------------------------------|
| 🔷 **LightGBM**     | Gradient Boosting with optimized speed and memory               |
| 🟠 **XGBoost**      | Accurate boosted trees for tabular data                         |
| 🟢 **Random Forest** | Ensemble learning with high variance control                    |

Each model is trained using **TimeSeriesSplit** and tuned for best validation performance using **GridSearchCV** (for LightGBM).

---

## 📈 Evaluation Metrics

To assess model performance, the following regression metrics are computed:

| Metric             | Description                                      |
|--------------------|--------------------------------------------------|
| 📉 MAE (Mean Absolute Error)   | Average absolute difference between actual and predicted values |
| 🧮 RMSE (Root Mean Squared Error) | Penalizes larger errors more heavily |
| 📊 R² Score         | Indicates how well predictions match actual values |
| 🧪 Residual Plots   | Visual checks for bias or variance in predictions |
| 🧠 SHAP Analysis    | Interprets and visualizes feature importance |

Each model's evaluation includes visual comparisons like residual histograms and scatter plots.

---

## 📍 Exploratory Data Analysis (EDA)

Exploratory analysis is performed using `ydata_profiling` and includes:

- ✅ Statistical summary report of all features
- ✅ Univariate visualizations using histograms and KDE plots
- ✅ Bivariate scatter plots with regression lines (feature vs. target)
- ✅ Correlation heatmap for all numerical features
- ✅ Volatility trends and feature dynamics over time

These insights inform feature engineering and model selection strategies.

---

## 🔍 Performance Summary


- **LightGBM** had the best accuracy and lowest errors
- **XGBoost** performed well, especially during volatility
- **Random Forest** was stable but less precise
- All models predicted next-hour price reliably
- Visual plots (like arrows) made the direction easy to interpret

---

## 📈 Sample Visuals
 -    📉 Actual vs Predicted for all models
 -    📊 Feature Importance (SHAP)
 -    ➡️ Next Hour Movement (Arrow Plot)

---

## 🧪 Future Scope
 -   Add LSTM/GRU models for sequence learning
 -   Integrate Twitter/Reddit Sentiment Analysis
 -   Create Streamlit Web App
 -   Multi-symbol portfolio prediction
 -   Backtesting on real trading strategies
---

> 🚨 These results vary slightly depending on crypto symbol and time range used.
