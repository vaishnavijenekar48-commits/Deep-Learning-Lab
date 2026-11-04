# Assignment 4: LSTM-Based Stock Price Forecasting

## 1. Aim
To develop an LSTM (Long Short-Term Memory) based deep learning model for time-series forecasting using historical stock market data to predict future stock closing prices.

## 2. Introduction
Time-series forecasting is a technique used to predict future values based on previously observed data.

In this assignment, an LSTM-based neural network is developed to predict Apple's (AAPL) stock closing prices using historical stock market data.

LSTM is a type of Recurrent Neural Network (RNN) that can learn long-term dependencies in sequential data. It is useful for time-series forecasting because it can remember important patterns from previous observations.

## 3. Dataset Information

- **Dataset:** Apple (AAPL) Historical Stock Prices
- **Source:** Yahoo Finance
- **Download Method:** Python `yfinance` library
- **Duration:** Last 5 years of historical data
- **Frequency:** Daily stock prices

### Dataset Features

| Feature | Description |
|---|---|
| Open | Opening stock price |
| High | Highest stock price of the day |
| Low | Lowest stock price of the day |
| Close | Closing stock price |
| Volume | Number of shares traded |

The model uses the **Closing Price** column for prediction.

## 4. Technologies and Libraries Used

- Python
- Google Colab
- TensorFlow and Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- yfinance

## 5. Methodology

The following steps are performed:

1. Download historical Apple stock price data using Yahoo Finance.
2. Load and preprocess the dataset.
3. Select the closing price for forecasting.
4. Normalize the data using MinMaxScaler.
5. Create sequences using the previous 60 days of stock prices.
6. Split the dataset into 80% training and 20% testing data.
7. Build an LSTM neural network with two LSTM layers and Dropout layers.
8. Train the model using the Adam optimizer.
9. Predict stock prices using testing data.
10. Evaluate performance using MSE, MAE, and RMSE.
11. Visualize actual and predicted stock prices.
12. Predict the next day's closing price.

## 6. Model Architecture

The LSTM model consists of:

- First LSTM Layer: 50 units
- Dropout Layer: 20%
- Second LSTM Layer: 50 units
- Dropout Layer: 20%
- Dense Layer: 1 output neuron

**Optimizer:** Adam

**Loss Function:** Mean Squared Error

**Epochs:** 20

**Batch Size:** 32

## 7. Evaluation Metrics

The model is evaluated using the following metrics:

- **Mean Squared Error (MSE):** Measures the average squared difference between actual and predicted values.
- **Mean Absolute Error (MAE):** Measures the average absolute prediction error.
- **Root Mean Squared Error (RMSE):** Measures the square root of the average squared prediction error.

Lower error values generally indicate better model performance.

## 8. Expected Output

The assignment generates:

- Historical stock price visualization.
- Training and validation loss graph.
- Actual vs predicted stock price graph.
- MSE, MAE, and RMSE evaluation results.
- Predicted next-day closing stock price.

## 9. Files Included

| File | Description |
|---|---|
| LSTM_Stock_Forecasting.ipynb | Complete Python code with executed outputs |
| stock_dataset.csv | Downloaded historical stock price dataset |
| prediction_results.csv | Actual and predicted stock prices |
| lstm_stock_model.keras | Saved trained LSTM model |
| README.md | Assignment documentation |

## 10. Conclusion

In this assignment, an LSTM-based deep learning model was successfully developed for stock price time-series forecasting.

The model learns patterns from historical stock closing prices and uses the previous 60 days of data to predict the next day's closing price.

The performance is evaluated using MSE, MAE, and RMSE, along with graphical comparisons of actual and predicted prices.

This assignment demonstrates how deep learning techniques such as LSTM can be applied to sequential data and time-series forecasting.

**Note:** Stock price predictions are estimates for educational purposes and should not be considered guaranteed future market prices.

