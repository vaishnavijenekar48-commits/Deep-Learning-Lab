# Dataset Information – LSTM Stock Price Forecasting

## 1. Dataset Name
Apple (AAPL) Historical Stock Price Dataset

## 2. Dataset Source
- **Source:** Yahoo Finance
- **Website:** https://finance.yahoo.com/
- **Python Library:** yfinance
- **Stock Symbol:** AAPL
- **Company:** Apple Inc.
- **Data Duration:** Last 5 years
- **Data Frequency:** Daily

## 3. Dataset Description

This dataset contains historical stock market information for Apple Inc. It includes daily opening, closing, highest and lowest stock prices, along with trading volume.

The dataset is downloaded directly into Google Colab using the yfinance Python library.

## 4. Dataset Features

| Column | Description |
|---|---|
| Date | Date of stock trading |
| Open | Opening stock price |
| High | Highest stock price during the day |
| Low | Lowest stock price during the day |
| Close | Closing stock price after adjustments |
| Volume | Total number of shares traded |

**Note:** Depending on the yfinance version and data settings, the Date may be stored as the DataFrame index rather than a separate column.

## 5. Dataset Download Code

The dataset is downloaded automatically using the following Python code:

```python
import yfinance as yf

# Download Apple's historical stock data
stock_data = yf.download(
    "AAPL",
    period="5y",
    interval="1d",
    auto_adjust=True
)

# Save dataset as CSV
stock_data.to_csv("stock_dataset.csv")

# Display dataset
print(stock_data.head())
```

## 6. Dataset Preprocessing

The following preprocessing operations are performed:

1. Select the Closing Price column.
2. Check and remove missing values.
3. Normalize the closing prices using MinMaxScaler.
4. Create sequences using the previous 60 days of stock prices.
5. Divide the data into training and testing sets in chronological order.

## 7. Dataset Usage

The dataset is used to train an LSTM (Long Short-Term Memory) neural network.

The model takes the previous 60 days of closing prices as input and predicts the next day's closing price.

## 8. Dataset File

**File Name:** `stock_dataset.csv`

**Format:** CSV (Comma-Separated Values)

**Usage:** Training and testing the LSTM-based stock price forecasting model.

## 9. Dataset License and Disclaimer

The data is retrieved through Yahoo Finance using the yfinance library. Refer to Yahoo Finance's terms and conditions for data usage and redistribution.

This dataset is used strictly for educational and academic purposes.

Historical stock prices do not guarantee future stock market performance.
