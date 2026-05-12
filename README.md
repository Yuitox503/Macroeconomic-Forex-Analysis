# Macroeconomic Forex Analysis
![image alt](https://github.com/Yuitox503/Macroeconomic-Forex-Analysis/blob/main/Overview.jpg?raw=true)

## Project Overview
This project explores the relationship between macroeconomic indicators and forex market movements using Python and Jupyter Notebook. The objective is to uncover how economic variables such as inflation, GDP growth, interest rates, and employment data influence EUR/USD and GBP/USD exchange rate trends.

The project combines exploratory data analysis, correlation studies, and machine learning forecasting to deliver a complete end-to-end analysis of forex market dynamics.

## Objectives
- Analyze the historical relationship between EUR/USD and GBP/USD exchange rates
- Investigate how macroeconomic indicators interact with each other over time
- Assess the impact of economic variables on forex price movements
- Build predictive machine learning models to forecast next-month EUR/USD prices

## Tech Stack
- Python (Pandas, NumPy, Scikit-learn, XGBoost, LightGBM)
- Yahoo Finance API (yfinance)
- Jupyter Notebook (EDA and Modeling)

## Exploratory Data Analysis (EDA)
Key insights from the dataset include:
- EUR/USD and GBP/USD exhibit a strong positive correlation of approximately 0.75, meaning both pairs tend to move together in response to USD-driven conditions
- GBP/USD displays greater historical volatility than EUR/USD, largely attributable to political events such as Brexit
- Significant fluctuations in both pairs are observable during the 2008 financial crisis and periods of aggressive Federal Reserve rate hikes
- EUR/USD shows a negative correlation with NASDAQ (-0.56), personal consumption expenditure (-0.62), and disposable income (-0.63), suggesting that a stronger US economy tends to strengthen the dollar

## Feature Engineering
- Merged monthly macroeconomic data with forex closing prices across a unified date range (2005–2022)
- Removed data leakage variables irrelevant to future price prediction
- Engineered a target variable representing next-month EUR/USD closing price
- Prepared dataset for both random and time-based train-test splits

## Machine Learning Models
Models implemented:
- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor (SVR)
- XGBoost Regressor
- K-Nearest Neighbors Regressor

### Final Model: Gradient Boosting Regressor
![image alt](https://github.com/Yuitox503/Macroeconomic-Forex-Analysis/blob/main/Model%20Result.jpg?raw=true)

Performance (time-based split):
- R² Score: ~0.45
- MAE: reported per model evaluation
- RMSE: reported per model evaluation

The Gradient Boosting and XGBoost models demonstrated the most consistent performance across both evaluation strategies, making them the strongest candidates for this forecasting task.

## Macroeconomic Indicator Analysis

Key findings from the indicator correlation analysis:
- Inflation and interest rates exhibit a strong inverse correlation (~-0.65), consistent with central bank policy responses to rising prices
- GDP growth and unemployment maintain a negative correlation (~-0.7), aligning with Okun's Law
- Interest rate changes have a lagging effect on both inflation and GDP growth, typically influencing economic conditions over several quarters

## Key Business Insights
- EUR/USD and GBP/USD can be used as partial proxies for each other, but individual economic and political factors must still be considered separately
- Random train-test splits produce misleadingly high model accuracy; time-based splits are essential for realistic evaluation of financial forecasting models
- Macroeconomic data alone is insufficient for reliable forex prediction — geopolitical events, central bank surprises, and market sentiment introduce noise that historical indicators cannot capture
- Gradient Boosting and XGBoost are better suited for this problem than linear or distance-based models due to the non-linear nature of currency markets

## Business Impact
- Provides analysts and traders with a data-driven framework for understanding USD strength through macroeconomic lenses
- Highlights which economic indicators carry the strongest predictive signal for EUR/USD movements
- Demonstrates the importance of time-aware model evaluation in financial data science
- Establishes a baseline for more advanced forecasting pipelines

## Future Improvements
- Implement advanced time-series models such as LSTM networks, ARIMA, or Transformer-based architectures
- Incorporate sentiment analysis from financial news and social media
- Expand the dataset to include trade balances, government debt levels, and consumer confidence indices
- Build a real-time dashboard with automated macroeconomic data feeds
- Integrate geopolitical risk indices to account for external market shocks

## Dataset
- EUR/USD & GBP/USD historical prices: Yahoo Finance via `yfinance`
- US macroeconomic indicators: [Kaggle](https://www.kaggle.com/)

## Author
[@FerdinandTaslim](https://github.com/your-username)
