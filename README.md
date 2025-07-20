# 📈 Bitcoin Price Prediction Using LSTM

A deep learning project using LSTM (Long Short-Term Memory) neural networks to predict Bitcoin closing prices. This project performs time series forecasting based on historical market data including open, high, low, and close prices, as well as volatility and moving averages.

---

## 📊 Overview

This project focuses on analyzing Bitcoin's historical price data and building an LSTM model to forecast its future closing prices. Key stages include:

- Exploratory Data Analysis (EDA)
- Feature engineering (lagged features, SMA, volatility)
- Data normalization
- Time series modeling using LSTM (TensorFlow/Keras)
- Performance visualization

---

## 🧾 Dataset

- **Source**: [Yahoo Finance – BTC-USD](https://finance.yahoo.com/quote/BTC-USD/history)
- **Format**: CSV (`BTC-USD.csv`)
- **Date Range**: 2014-09-17 to 2022-02-19
- **Features**:
  - `Date`, `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`

---

## ⚙️ Tech Stack

- **Languages**: Python
- **Libraries**:
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`
  - `scikit-learn`
  - `tensorflow` (Keras)
  
---

## 🧪 EDA & Preprocessing

- Checked for missing values and data types
- Removed redundant columns (`Adj Close`, `Volume`)
- Set `Date` as index for time series analysis
- Created new features:
  - Simple Moving Averages (30 & 90 days)
  - Daily returns and rolling volatility
  - Lagged features for previous 3 days
- Normalized the data using `MinMaxScaler`

---

## 🧠 LSTM Model

- Two stacked LSTM layers with 50 units each
- Output layer: 1 neuron (regression)
- Optimizer: Adam
- Loss: Mean Squared Error (MSE)
- Training epochs: 10
- Batch size: 32

---

## 📈 Results & Visualizations

- Price trend plots (Open, Close, High, Low)
- Moving averages overlay
- Loss decreased significantly over 10 epochs
- Model captured overall price movement patterns
- Ready for further tuning and forecasting

---

## 📂 Project Structure

