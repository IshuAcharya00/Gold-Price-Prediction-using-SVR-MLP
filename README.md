Gold Price Prediction using SVR & MLP (Voting Regressor)
This project leverages 25 years of historical gold stock data (2000–2025) to predict the next day's closing price. By employing a Voting Regressor ensemble—combining Support Vector Regression (SVR) and a Multi-Layer Perceptron (MLP)—the model generates a "Buy" or "Sell" trade signal based on the predicted price movement.

Project Overview
The goal of this project is to analyze long-term historical gold price trends and build a robust machine learning model for short-term forecasting.

Data Source: Kaggle (25 years of gold stock data).

Training Period: First 20 years of data.

Testing Period: Last 5 years of data (for performance comparison).

Core Models: SVR (Support Vector Regression) and MLP (Multi-Layer Perceptron).

Ensemble Method: Voting Regressor for improved accuracy.

Output: Next-day predicted closing price and a Buy/Sell signal.

Dataset Description
The dataset includes daily gold price metrics:

Date: The trading date.

GC=F_Open: Opening price.

GC=F_High: Highest price of the day.

GC=F_Low: Lowest price of the day.

GC=F_Close: Closing price (Target Variable).

GC=F_Volume: Total shares traded.


Model Architecture:
Preprocessing: Data is scaled using MinMaxScaler to normalize features for the Neural Network (MLP) and SVR models.

Individual Models:

SVR: Effective for capturing non-linear relationships in time-series data.

MLP: A neural network approach to learn complex patterns in price fluctuations.

Ensemble (Voting Regressor): Combines the predictions of both SVR and MLP to reduce individual model bias and provide a more stable forecast.

Trading Signal Logic:

BUY: If Predicted Close > Current Close.

SELL: If Predicted Close < Current Close.


Results:
The notebook includes a detailed comparison between the Predicted Close and the Actual Close over the 5-year test period to evaluate the model's reliability.

Example Forecast Output:
NEXT DAY GOLD FORECAST (CLOSE ONLY)
----------------------------------
Predicted Close : 3257.92
Current Close   : 3241.40
Change (%)      : 0.51%
TRADE SIGNAL    : BUY

License
This project is for educational and research purposes. Trading stocks involves risk; always perform your own due diligence.

