# 📈 Gold Price Prediction using SVR & MLP (Voting Regressor)

This project leverages **25 years of historical gold price data (2000–2025)** to predict the **next day’s closing gold price**.  
An ensemble **Voting Regressor**, combining **Support Vector Regression (SVR)** and **Multi-Layer Perceptron (MLP)**, is used to enhance prediction stability and accuracy.  
Based on the predicted movement, the system generates a simple **Buy/Sell trading signal**.

---

## 📌 Project Overview

The main objective of this project is to analyze long-term historical trends in gold prices and develop a robust **machine learning-based short-term forecasting model**.

- **Data Source:** Kaggle (25 years of gold stock data)
- **Training Period:** First 20 years (2000–2019)
- **Testing Period:** Last 5 years (2020–2025)
- **Core Models:**  
  - Support Vector Regression (SVR)  
  - Multi-Layer Perceptron (MLP)
- **Ensemble Method:** Voting Regressor
- **Output:**  
  - Next-day predicted closing price  
  - Buy/Sell trading signal

---

## 📊 Dataset Description

The dataset consists of daily gold price metrics with the following features:

| Feature Name       | Description |
|-------------------|-------------|
| Date              | Trading date |
| GC=F_Open         | Opening price |
| GC=F_High         | Highest price of the day |
| GC=F_Low          | Lowest price of the day |
| GC=F_Close        | Closing price (**Target Variable**) |
| GC=F_Volume       | Total trading volume |

---

## 🧠 Model Architecture

### 🔹 Data Preprocessing
- Feature scaling performed using **MinMaxScaler**
- Normalization ensures stable learning for both **SVR** and **MLP**

### 🔹 Individual Models
- **SVR (Support Vector Regression):**  
  Captures non-linear relationships effectively in time-series data.

- **MLP (Multi-Layer Perceptron):**  
  Learns complex patterns and interactions in historical price movements.

### 🔹 Ensemble Model
- **Voting Regressor:**  
  Combines predictions from SVR and MLP to reduce individual model bias and improve overall forecast reliability.

---

## 📈 Trading Signal Logic

Based on the predicted closing price:

- **BUY** → If `Predicted Close > Current Close`
- **SELL** → If `Predicted Close < Current Close`

This logic provides a simple yet interpretable trading recommendation.

---

## ✅ Results & Evaluation

- The model performance is evaluated over the **5-year test period**
- A detailed comparison between:
  - **Actual Closing Price**
  - **Predicted Closing Price**
- Visualization and error metrics are included in the notebook to assess reliability and trend-following behavior.

---

## 🔮 Example Forecast Output

NEXT DAY GOLD FORECAST (CLOSE ONLY)

Predicted Close : 3257.92
Current Close : 3241.40
Change (%) : 0.51%
TRADE SIGNAL : BUY


## 📄 License

This project is open for academic and learning use.  
Feel free to explore, modify, and improve the model for research purposes.
