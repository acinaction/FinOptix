# Finoptix Portfolio Project

Welcome to my Finoptix portfolio repository! This project highlights a series of assignments and a final capstone implementation showcasing my skills in quantitative trading, machine learning, and advanced portfolio optimization.

## Table of Contents

1. [Overview](#overview)
2. [Project Structure](#project-structure)
    - [1. Quantitative Trading](#1-quantitative-trading)
    - [2. Machine Learning](#2-machine-learning)
    - [3. Portfolio Optimization](#3-portfolio-optimization)
    - [4. Final Implementation](#4-final-implementation)
3. [Setup and Installation](#setup-and-installation)
4. [Technologies Used](#technologies-used)

## Overview

Throughout this project, I developed robust financial models ranging from basic technical trading strategies to complex, machine-learning-driven portfolio allocation frameworks. 
The highlight of the project is the **Final Implementation**, which blends predictive modeling (XGBoost) with financial heuristics (PE/DE ratios) and the Black-Litterman optimization model to construct a dynamic, robust stock portfolio.

## Project Structure

The repository is divided into four main sections:

### 1. Quantitative Trading
**File:** `01_Quantitative_Trading/Bitcoin_Trading_Strategy.ipynb`
- Developed a backtested trading strategy for Bitcoin (BTC-USD).
- Utilized technical indicators including **MACD** (Moving Average Convergence Divergence) and **RSI** (Relative Strength Index) to generate buy/sell signals.
- Integrated risk management techniques using **ATR** (Average True Range) for stop-loss and trailing take-profit mechanisms.

### 2. Machine Learning
**File:** `02_Machine_Learning/ML_Feature_Selection_and_Classification.ipynb`
- Performed extensive Exploratory Data Analysis (EDA) on a given dataset (correlation heatmaps, distributions).
- Executed feature selection using **Mutual Information**, **PCA (Principal Component Analysis)**, and **Random Forest** feature importances.
- Evaluated multiple classifiers (**Logistic Regression**, **Random Forest**, **Decision Tree**) with cross-validation to achieve the best ROC-AUC score.

### 3. Portfolio Optimization
**File:** `03_Portfolio_Optimization/Fama_French_Black_Litterman_Optimization.ipynb`
- Implemented the **Fama-French 3-Factor Model** to estimate the expected returns of a diverse stock portfolio.
- Transitioned into the **Black-Litterman Model**, integrating market equilibrium returns with specific investor views.
- Calculated optimal weights for the portfolio, utilizing PyPortfolioOpt to maximize the Sharpe Ratio and plot the efficient frontier.

### 4. Final Implementation
**File:** `04_Final_Implementation/Stock_Ranking_and_Portfolio_Allocation.ipynb`
This notebook brings everything together into a robust stock picking and allocation pipeline:
- **Feature Engineering:** Calculated rolling volatilities, moving averages, momentum, and lag returns for a large universe of Indian stocks.
- **Predictive Modeling:** Trained an **XGBoost Regressor** to predict expected future returns for each stock.
- **Fundamental Ranking:** Ranked the top stocks by combining the ML-predicted returns with fundamental metrics like **PE Ratio**, **Debt-to-Equity**, and **Market Cap**.
- **Portfolio Allocation:** Applied the **Black-Litterman Model** on the top selected stocks, formulating views based on the model's predictions, to generate the final, optimal portfolio weights. Simulated the performance against an equal-weight market portfolio.

## Setup and Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/finoptix-portfolio.git
   cd finoptix-portfolio
   ```

2. **Install dependencies:**
   It is recommended to use a virtual environment.
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebooks:**
   Launch Jupyter Notebook or Jupyter Lab to explore the files:
   ```bash
   jupyter notebook
   ```

## Technologies Used
- **Data Analysis & Processing:** Pandas, NumPy
- **Machine Learning:** Scikit-Learn, XGBoost
- **Financial Modeling:** PyPortfolioOpt, Statsmodels
- **Data Gathering:** yfinance
- **Visualization:** Matplotlib, Seaborn, Plotly
