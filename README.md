# TASI-Hybrid-Pred 🇸🇦
**TASI-Hybrid-Pred** is a high-performance machine learning framework for predicting the **Saudi Stock Market (TASI)** index prices.  
By integrating linear structural stability with non-linear residual intelligence, this model provides a strategic **18-day forecasting horizon**, specifically optimized for the unique dynamics of the Saudi financial market.

This repository provides a complete pipeline for time-series forecasting, utilizing a **Residual-Correction Hybrid Architecture** to achieve superior predictive accuracy.

---

## 📊 Key Highlights
- **Performance**: Achieved an **R-squared ($R^2$) of 0.9345** and a **Pearson Correlation (PCC) of 0.9710**.
- **Strategy**: Focused on a mid-term **18-day prediction horizon** to mitigate short-term market noise.
- **Data Source**: Historical data sourced from **Kaggle** (CSV format).
- **Architecture**: Dual-stage ensemble combining **Ridge Regression** and **Random Forest**.

---

## Table of Contents
- [Introduction](#introduction)
- [Architecture](#architecture)
- [Data & Features](#data--features)
- [Evaluation Metrics](#evaluation-metrics)
- [Repository Structure](#repository-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Outputs](#outputs)

---

## Introduction
Predicting price trajectories in the Saudi Stock Exchange (TASI) is a complex task due to the mixture of stable economic trends and stochastic volatility. **TASI-Hybrid-Pred** bridges this gap by using a two-stage modeling approach. In alignment with **Saudi Vision 2030**, this project demonstrates how advanced AI can be applied to enhance financial decision-making in emerging markets.

---

## Architecture
The framework employs a **Two-Stage Residual-Correction Engine**:
1. **Linear Baseline (Ridge)**: Establishes the global price trajectory and stabilizes coefficients via L2 regularization.
2. **Stochastic Correction (Random Forest)**: Models the remaining non-linear residuals to account for market anomalies and sudden shifts.

<img width="1920" height="1080" alt="Purple and Pink Geometric Corporate Governance Framework Infographic Presentation (9)" src="https://github.com/user-attachments/assets/24e48c81-8c7d-43ac-a4f3-45a24858c759" />

---

## Data & Features
The model utilizes a historical dataset retrieved from **Kaggle** in CSV format.

- **Primary Features**: Open, High, Low, Close, and Volume.
- **Engineered Indicators**: 
  - **MA200 & MA50**: Long-term and medium-term structural trend anchors.
  - **RSI**: Momentum-based Relative Strength Index.
- **Preprocessing**: 
  - Loading from static CSV files.
  - **StandardScaler** for numerical normalization.
  - Chronological 80/20 train-test split to ensure time-series integrity.

---

## Evaluation Metrics
To ensure a robust assessment, the following metrics were implemented:
- **MSE (Mean Squared Error)**: Measures the average squared difference between actual and predicted values.
- **RMSE (Root Mean Squared Error)**: Provides error values in the same unit as stock prices (SAR).
- **MAE (Mean Absolute Error)**: Quantifies the average absolute magnitude of errors.
- **$R^2$ (Coefficient of Determination)**: Explains the proportion of variance captured by the model (0.9345).
- **PCC (Pearson Correlation)**: Validates directional consistency (0.9710).
- **Weighted Averaging**: Used to synthesize the final prediction from the linear and non-linear streams.

---

## Repository Structure
```text
TASI-Hybrid-Pred/
│
├── codes/          # Jupyter notebooks (Preprocessing, FE, Hybrid Training)
├── figures/        # Performance visualizations (PCC charts, Scatter plots)
├── models/         # Saved trained models (.joblib)
├── data/           # Directory for the Kaggle CSV dataset
├── requirements.txt# Project dependencies
└── README.md       # Project documentation
