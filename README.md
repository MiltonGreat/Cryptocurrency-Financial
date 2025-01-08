# Cryptocurrency Trading Strategy Backtesting

### Problem Statement

The volatile nature of cryptocurrency markets presents opportunities and challenges for algorithmic trading. Developing predictive models that account for market fluctuations can enhance trading strategies.

### Solution Approach

Data: Cryptocurrency market data, including daily returns, trading volumes, and volatility indices.

Methods:

- Built machine learning models (Random Forest, Gradient Boosting) to predict daily returns.
- Performed feature engineering to extract indicators like Relative Strength Index (RSI) and Moving Averages (MA).
- Backtested trading strategies using predicted returns to evaluate profitability.
- Tools: Python (Scikit-learn, pandas, backtrader library for backtesting).

### Results

- Achieved reasonable accuracy in predicting cryptocurrency price movements.
- Backtested trading strategy showed consistent gains in stable market conditions but struggled in periods of extreme volatility.

### Key Insights

- Predictive models can identify market trends, but their performance depends on market stability.
- Algorithmic trading requires robust risk management strategies to minimize losses during volatile periods.

### Future Directions

- Incorporate sentiment analysis from social media to improve predictions.
- Explore reinforcement learning to adapt strategies dynamically to changing market conditions.

### Overview

The project uses historical cryptocurrency data (Open, High, Low, Close, Volume, and Market Cap) to build predictive models for assessing the next day's return. The model is trained using various technical indicators, including moving averages and lag features, to predict price movements.

### Dataset

The dataset contains the following columns:

- Currency: The name of the cryptocurrency (e.g., bitcoin, ethereum, etc.)
- Date: The date of the observation.
- Open: The opening price for the day.
- High: The highest price reached during the day.
- Low: The lowest price reached during the day.
- Close: The closing price for the day.
- Volume: The trading volume during the day.
- Market Cap: The market capitalization of the cryptocurrency on the given date.

### Data Preprocessing

Missing Values: The dataset is checked for missing values, which are handled by dropping rows with NaN values.

Feature Engineering:
- Daily Return: The percentage change in closing price from the previous day.
- 7-day MA & 30-day MA: Moving averages over 7 and 30 days to smooth out price fluctuations.
- Lag Features: The previous day's closing price is used as a feature for predicting future prices.

### Model Evaluation

- MAE: 4.4497
- R-squared: 0.8642

These results suggest the model has a good fit and is able to predict cryptocurrency price movements with reasonable accuracy.


### Source

https://www.kaggle.com/datasets/philmohun/cryptocurrency-financial-data
