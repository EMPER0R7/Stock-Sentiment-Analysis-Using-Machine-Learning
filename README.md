# Stock Sentiment Analysis

## Introduction
This project focuses on performing **stock sentiment analysis** using news headlines and technical indicators to predict stock price movements. Multiple machine learning models, including Logistic Regression, Random Forest, Support Vector Classifier (SVC), and a Convolutional Neural Network (CNN), were trained to identify buy and sell signals. The best-performing model is used to generate trading signals and evaluate the performance of a trading strategy.

---

## Project Structure
The project consists of two Jupyter Notebooks:
1. **DataScrapp**: Collects news headlines and stock data.
2. **SentimentAnalysis**: Performs complete analysis, model training, and evaluation.

---

## Steps Involved

### 1. Data Collection
- **News Data**: Scraped using the **New York Times API**, covering the period from 2016 to 2019.
- **Stock Data**: Retrieved from the **yfinance** library for the same time range.

---

### 2. Code Explanation

#### Data Preparation:
1. **Import Libraries**: Essential libraries for data manipulation, machine learning, and visualization.
2. **Data Loading**: Load stock price data and news headlines into Pandas DataFrames.
3. **Data Preprocessing**: Convert date columns to datetime format and merge stock data with news data by date.

#### Sentiment Analysis:
4. Perform sentiment analysis on news headlines using **VADER** and **TextBlob**, adding sentiment scores as features to the dataset.

#### Technical Indicators:
5. Add indicators such as **Simple Moving Average (SMA)** and **Relative Strength Index (RSI)** using the `ta` library.

#### Feature Engineering and Model Training:
6. Create new features:
   - Calculate stock returns.
   - Generate binary labels for stock movements (upward = 1, downward = 0).
   - Prepare feature matrix (X) and target vector (y).
7. Train and evaluate multiple models (Logistic Regression, Random Forest, SVC, and CNN) using cross-validation.

---

### 3. Trading Signals and Backtesting

8. **Generate Trading Signals**: Use the best model to predict buy and sell signals.
9. **Backtest Strategy**: Simulate the trading strategy and calculate the portfolio value.
10. **Performance Metrics**:
    - Sharpe Ratio
    - Maximum Drawdown
    - Win Ratio

Additionally, visualize:
- **ROC Curve**
- Buy and sell signals graphically.

---

## Tools and Libraries Used
- **APIs**: New York Times API
- **Libraries**: Pandas, Numpy, VADER, TextBlob, `ta`, Scikit-learn, TensorFlow
- **Data Source**: yfinance

---

## Author
- **Name**: Aditya Kurne
- **Enrollment**: 22123022
- **Program**: EPH

