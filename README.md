# TASI-Hybrid-Pred 🇸🇦
**TASI-Hybrid-Pred** is a high-performance machine learning framework designed for predicting the **Saudi Stock Market (TASI)** index prices.  
By integrating linear structural stability with non-linear residual intelligence, this model provides a strategic **18-day forecasting horizon**, specifically optimized for the unique dynamics of the Saudi financial market.

This repository provides a complete pipeline for time-series forecasting, utilizing a **Residual-Correction Hybrid Architecture** to achieve superior predictive accuracy.

---

## 📊 Key Highlights
- **Performance**: Achieved an **R-squared ($R^2$) of 0.9345** and a **Pearson Correlation (PCC) of 0.9710**.
- **Strategy**: Focused on a mid-term **18-day prediction horizon** to mitigate short-term market noise.
- **Data Source**: Historical TASI dataset (2020-2026) sourced from **Kaggle**.
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
Predicting price trajectories in the Saudi Stock Exchange (TASI) is inherently challenging due to non-linear market shocks. **TASI-Hybrid-Pred** leverages computational intelligence to bridge the gap between linear stability and non-linear adaptability. In alignment with **Saudi Vision 2030**, this project demonstrates how advanced AI can be applied to enhance financial decision-making in emerging markets.
## Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/fahadalthalig/TASI-Hybrid-Pred.git
cd TASI-Hybrid-Pred
pip install -r requirements.txt
```
## Usage

1. **Download the Dataset**: Visit the [Kaggle Dataset link](https://www.kaggle.com/datasets/abdulmalekx/saudi-stocks-prediction-data-tadawul-2020-2026) and download the CSV file.
2. **Setup Data**: Place the downloaded `.csv` file into the `data/` folder within the project directory.
3. **Run the Pipeline**: Open and run the Jupyter notebooks in the `codes/` folder in the following sequence:
   - `01_Preprocessing.ipynb`: To clean the raw Kaggle data and handle dates.
   - `02_Feature_Engineering.ipynb`: To generate the MA200, MA50, and RSI indicators.
   - `03_Hybrid_Model_Training.ipynb`: To train the Ridge and Random Forest models and execute the residual-correction logic.
4. **View Results**: Performance metrics and visualization plots will be automatically generated and saved in the `figures/` folder.
5. **Inference**: Trained models are saved in the `models/` folder and can be loaded for future price predictions without retraining.

## Architecture
The framework employs a **Two-Stage Residual-Correction Engine**:
1. **Linear Baseline (Ridge)**: Establishes the global price trajectory and stabilizes coefficients via L2 regularization.
2. **Stochastic Correction (Random Forest)**: Models the remaining non-linear residuals to account for market anomalies and sudden shifts.
<img width="1920" height="1080" alt="Purple and Pink Geometric Corporate Governance Framework Infographic Presentation (9)" src="https://github.com/user-attachments/assets/c075c50d-4b7b-4743-9077-d9d4491c059c" />



---

## Data & Features
The model utilizes a historical dataset retrieved from Kaggle.

- **Dataset Link**: [Saudi Stocks Prediction Data (2020-2026)](https://www.kaggle.com/datasets/abdulmalekx/saudi-stocks-prediction-data-tadawul-2020-2026)
- **Primary Features**: Open, High, Low, Close, and Volume.
- **Engineered Indicators**: 
  - **MA200 & MA50**: Long-term and medium-term structural trend anchors.
  - **RSI**: Momentum-based Relative Strength Index.
- **Preprocessing**: 
  - Loading from `csv` format.
  - **StandardScaler** for numerical normalization.
  - Chronological 80/20 train-test split to ensure time-series integrity.

---

## Evaluation Metrics
To ensure a robust assessment, the following metrics were implemented:
- **MSE (Mean Squared Error)** / **RMSE (Root Mean Squared Error)**: Measures the magnitude of prediction error.
- **MAE (Mean Absolute Error)**: Quantifies the average absolute magnitude of errors.
- **$R^2$ (Coefficient of Determination)**: Explains the proportion of variance captured by the model (0.9345).
- **PCC (Pearson Correlation)**: Validates directional consistency (0.9710).
- **Weighted Averaging**: Used to synthesize the final prediction from the linear and non-linear streams.

---
## Outputs

The repository provides the following outputs upon execution:

* **Evaluation Metrics**:
  - **$R^2$ (0.9345)**: Quantifies the variance explanation of the TASI index.
  - **PCC (0.9710)**: Validates the directional correlation between actual and predicted prices.
  - **RMSE (79.26)**: Measure of the average error magnitude in SAR.
  - **MAE**: Average absolute error for robustness testing.

* **Visualizations** (`figures/`): 
  - Comparison bar charts and predicted-vs-actual scatter plots.

* **Saved Models** (`models/`): 
  - Serialized `joblib` files for immediate 18-day forecasting.




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
