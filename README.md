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

- `open`, `high`, `low`, `volumefrom`, `volumeto`
- `day`, `month`, `year`, `dayofweek`
- Target: **Price Up (1)** or **Price Down (0)** (binary classification)

---

## 🧠 Model Used

- **LightGBM Classifier**
  - Fast and efficient gradient boosting framework
  - Suitable for large-scale classification tasks
- Feature Scaling with `StandardScaler`
- Hyperparameter tuning and model evaluation

---

## 📈 Evaluation Metrics

| Metric              | Why Used                                    |
|---------------------|---------------------------------------------|
| Accuracy            | General prediction success                  |
| Precision, Recall   | Investment-focused metric (false alarms)    |
| F1-Score            | Balanced tradeoff between precision/recall  |
| ROC/AUC Score       | True classification power                   |

---

## 📍 Exploratory Data Analysis (EDA)

- 📉 Line plots of closing prices & volume
- 📊 Moving Averages (5-day, 10-day)
- 🔁 RSI & % Price Change
- 🔥 Heatmap of feature correlations
- 📌 Class distribution analysis

---

## 🔍 Performance Summary

| Metric    | Value     |
|-----------|-----------|
| Accuracy  | ~77%      |
| Precision | ~75%      |
| Recall    | ~72%      |
| AUC       | ~0.81     |

> 🚨 These results vary slightly depending on crypto symbol and time range used.

---
