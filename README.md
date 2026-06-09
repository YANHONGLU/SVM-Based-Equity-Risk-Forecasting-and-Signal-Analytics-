# SVM-Based Equity Risk Forecasting and Signal Analytics

## Overview

This project develops a machine learning framework for equity risk forecasting and risk-aware signal generation using Support Vector Machines (SVM).

The objective is to identify changing market regimes and potential positive market moves by combining technical indicators, feature selection, model validation and risk analytics.

Workflow:

Data Collection → Feature Engineering → Feature Selection → Model Development → Model Validation → Risk Analytics → Backtesting

---

## Dataset

- Asset: American Express (AXP)
- Data Source: Yahoo Finance
- Frequency: Daily
- Period: 2020–Present
- Engineered Features: 44

---

## Feature Engineering

Constructed 44 technical, momentum, volatility and volume-based indicators, including:

- Momentum Indicators
- Price Change Indicators
- RSI
- MACD
- Bollinger Bands
- ATR
- Volume Indicators
- Volatility Measures

---

## Feature Selection Funnel

A six-stage feature selection framework was implemented to reduce dimensionality and improve robustness:

1. Variance Threshold
2. Correlation Filter
3. Variance Inflation Factor (VIF)
4. ANOVA F-Test
5. Recursive Feature Elimination (RFE)
6. Random Forest Feature Importance

Feature Reduction:

44 Features → 22 → 14 → 6 → 5 → 3 Final Features

---

## Model Development

Algorithm:

- Support Vector Machine (SVM)

Hyperparameter Optimisation:

- GridSearchCV
- TimeSeriesSplit Cross-Validation
- 120 Parameter Combinations
- 600 Model Fits

Parameters Tuned:

- Kernel
- C
- Gamma
- Class Weight

---

## Model Validation

To avoid look-ahead bias commonly found in financial datasets, the model uses:

- Temporal Train/Test Split
- TimeSeriesSplit Cross-Validation

This approach better reflects real-world deployment conditions.

---

## Risk Analytics

The framework incorporates multiple risk-focused evaluation metrics:

- Value-at-Risk (VaR)
- Expected Shortfall (ES)
- Sharpe Ratio
- Maximum Drawdown
- Backtesting Analysis

---

## Key Results

- Developed an end-to-end machine learning framework for equity risk forecasting
- Reduced 44 engineered features to 3 predictive features through a structured feature-selection process
- Applied time-series cross-validation to improve model robustness
- Integrated risk analytics and backtesting for risk-adjusted performance evaluation

---

## Technologies

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- yfinance
