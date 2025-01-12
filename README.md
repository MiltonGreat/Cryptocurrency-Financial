# Cryptocurrency Trading Strategy Backtesting

## Overview

The project focuses on using historical cryptocurrency data to build predictive models that forecast the next day's return. The model is trained using various technical indicators, including moving averages, lag features, and log returns, to predict price movements (up or down). The predictions are then used to inform a trading strategy, which is backtested to assess profitability and risk.

### Problem Statement

The cryptocurrency market is highly volatile, presenting both significant opportunities and risks for algorithmic trading. The goal of this project is to develop machine learning models capable of predicting daily returns and utilizing those predictions to inform trading strategies.

### Dataset

The dataset contains the following columns:

- Currency: The name of the cryptocurrency (e.g., Bitcoin, Ethereum).
- Date: The date of the observation.
- Open: The opening price for the day.
- High: The highest price reached during the day.
- Low: The lowest price reached during the day.
- Close: The closing price for the day.
- Volume: The trading volume during the day.
- Market Cap: The market capitalization of the cryptocurrency on the given date.

### Solution Approach

Data: Cryptocurrency market data, including daily returns, trading volumes, and volatility indices.

#### Methods

1. Data Preprocessing:
- Handled missing values in the dataset by dropping or converting invalid entries.
- Performed feature engineering, such as adding daily returns, log returns, moving averages (7-day and 30-day), and lag features for better predictive accuracy.

2. Machine Learning Models:
- Implemented Random Forest and Logistic Regression models for predicting price movements (up or down).
- Used TimeSeriesSplit for cross-validation to handle the time-series nature of the data.
- Applied class weights to handle class imbalance when predicting price movements (up or down).

3. Backtesting Trading Strategy:
- A trading strategy was backtested based on predicted daily price movements.
- The model makes a prediction for whether the price will go up or down and takes a position accordingly.
- Strategy performance was evaluated by calculating cumulative returns, Sharpe ratio, total return, and maximum drawdown.

### Data Preprocessing

Missing Values: The dataset is checked for missing values, which are handled by dropping rows with NaN values.

Feature Engineering:
- Daily Return: The percentage change in closing price from the previous day.
- 7-day MA & 30-day MA: Moving averages over 7 and 30 days to smooth out price fluctuations.
- Lag Features: The previous day's closing price is used as a feature for predicting future prices.

### Model Evaluation

Model Evaluation
- Accuracy: The Random Forest model achieved an accuracy of 1.00 on the test set.
- Cross-validation: The mean cross-validation score across 5 folds was 1.00.
- Classification Report: The logistic regression model for price movement prediction achieved 74% accuracy with a macro average F1-score of 0.71.

Sharpe Ratio:
- Sharpe Ratio: 0.02, indicating minimal risk-adjusted return for the strategy.

Performance Metrics:
- Total Return: The total return of the strategy was extremely high (based on a backtest).
- Maximum Drawdown: The maximum drawdown observed for the strategy was -67.66%, highlighting the risk involved in cryptocurrency trading.

### Results

- Cross-validation scores: The model achieved a mean cross-validation score of 1.00 on the Random Forest model, indicating high predictive accuracy.
- Accuracy: The Random Forest model achieved an accuracy of 1.00 on the test set, demonstrating strong classification performance.

Trading Strategy:
- The logistic regression-based trading strategy achieved an accuracy of 0.74 in predicting price movements.
- The strategy's backtested total return was exceptionally high, but with a significant drawdown of 67.66%, highlighting the volatility of cryptocurrency markets.

### Key Insights

- Predictive models can effectively identify price movement trends, but their performance is contingent on market stability and the inclusion of robust risk management strategies.
- Algorithmic trading strategies need to be adaptive, especially during periods of extreme market volatility.
- Although the strategy was profitable in stable conditions, more advanced techniques like sentiment analysis or reinforcement learning could enhance the strategy's adaptability and robustness.

### Future Directions

- Sentiment Analysis: Incorporating social media sentiment or news data to improve predictions and enhance the model’s understanding of market-moving events.
- Reinforcement Learning: Exploring reinforcement learning to dynamically adapt trading strategies based on real-time market conditions and feedback.
- Additional Models: Investigating the potential of other machine learning models, such as LSTM or other time-series-based models, to capture long-term dependencies in the data.

### Source

https://www.kaggle.com/datasets/philmohun/cryptocurrency-financial-data
