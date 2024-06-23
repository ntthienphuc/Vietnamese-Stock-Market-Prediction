
# Stock Price Prediction with ARIMA Model

## Introduction
This project aims to predict stock prices for the VN30 and VNINDEX indices using the ARIMA (AutoRegressive Integrated Moving Average) model. The project involves data collection, preprocessing, model development, evaluation, and backtesting to assess the effectiveness of the ARIMA model in real-world trading scenarios.

## Data Collection and Description
### Overview of VN-Index and VN30
The VN-Index and VN30 are two significant indices representing the performance of the Ho Chi Minh Stock Exchange. The VN-Index includes all listed companies on HOSE, serving as a barometer of market health and investor sentiment. The VN30 is a sub-index of the VN-Index, comprising the top 30 largest and most liquid companies on HOSE, providing a benchmark for large-cap stocks.

### Data Source and Retrieval
The dataset was sourced from Vietcap Securities Joint Stock Company (HOSE: VCI) using the vnstock3 library. This library provides access to extensive stock market data from Vietnam, simplifying the data retrieval process.

## Data Cleaning and Preprocessing
The historical stock data for VN30 and VNINDEX indices were cleaned and preprocessed to ensure accuracy and consistency. Essential technical indicators such as Simple Moving Average (SMA), Exponential Moving Average (EMA), Relative Strength Index (RSI), and Moving Average Convergence Divergence (MACD) were added to enhance the model's predictive capabilities.

## Model Development and Evaluation
### Model Training
The ARIMA model was trained using different window sizes (k=30 and k=200) to predict future stock prices. The optimal order parameters (p, d, q) were determined using the auto_arima function, which minimizes error metrics to improve model performance.

### Model Selection
Multiple ARIMA models with different (p, d, q) combinations were evaluated. The model with the lowest Akaike Information Criterion (AIC) and Bayesian Information Criterion (BIC) values was selected as the optimal model.

## Backtesting and Results
### k=30
**VN30 Results:**
- Margin: -31.78
- Maximum Drawdown (MDD): 1132.23 (134.59%)
- Total Trading Quantity: 103
- Profit per Trade: -8.00
- Total Profit: -824.1
- Profit after Fee: -867.5
- Trading Quantity per Day: 0.1098
- Profit per Day after Fee: -0.92
- Annual Return: -27.41%
- Profit per Year: -230.62
- Hit Rate: 0.398
- Hit Rate per Day: 0.428

**VNINDEX Results:**
- Margin: -16.91
- Maximum Drawdown (MDD): 799.29 (88.72%)
- Total Trading Quantity: 83
- Profit per Trade: -4.15
- Total Profit: -344.6
- Profit after Fee: -379.3
- Trading Quantity per Day: 0.0885
- Profit per Day after Fee: -0.40
- Annual Return: -11.19%
- Profit per Year: -100.83
- Hit Rate: 0.446
- Hit Rate per Day: 0.428

### k=200
**VN30 Results:**
- Margin: 45.14
- Maximum Drawdown (MDD): 605.83 (42.35%)
- Total Trading Quantity: 11
- Profit per Trade: 10.24
- Total Profit: 112.7
- Profit after Fee: 108.2
- Trading Quantity per Day: 0.0117
- Profit per Day after Fee: 0.12
- Annual Return: 2.01%
- Profit per Year: 28.76
- Hit Rate: 0.273
- Hit Rate per Day: 0.359

**VNINDEX Results:**
- Margin: 20.62
- Maximum Drawdown (MDD): 499.50 (38.48%)
- Total Trading Quantity: 25
- Profit per Trade: 4.28
- Total Profit: 107.0
- Profit after Fee: 96.9
- Trading Quantity per Day: 0.0267
- Profit per Day after Fee: 0.10
- Annual Return: 1.98%
- Profit per Year: 25.76
- Hit Rate: 0.56
- Hit Rate per Day: 0.351

## Conclusions and Perspectives
This project demonstrated the effectiveness of the ARIMA model with a larger window size (k=200) in capturing long-term trends and providing reliable trading signals, resulting in positive profits and better risk management. The model with a smaller window size (k=30) struggled with short-term volatility, leading to significant losses.

### Recommendations:
- **For Long-Term Predictions:** Using a larger window size (e.g., k=200) is recommended for capturing long-term trends and reducing transaction costs.
- **For Short-Term Predictions:** Further refinement is needed for the ARIMA model with a short window size (e.g., k=30), possibly incorporating additional technical indicators or alternative models.
- **Risk Management:** Implement advanced risk management strategies to mitigate high maximum drawdown and enhance trading strategy stability.

Future work could explore the integration of external factors, application to other markets, and incorporation of advanced risk management techniques to further improve the model's performance.
