# Stock Price Prediction with LSTM in PyTorch 📈

## About This Project
This project uses Deep Learning to predict future stock prices based on historical market data. It implements a Long Short-Term Memory (LSTM) neural network built with PyTorch to analyze time-series data and forecast future trends.

Unlike simple models that only look at one variable, this is a **multivariate** model. It takes in 4 specific daily data points to make its predictions:
* **High** Price
* **Low** Price
* **Open** Price
* **Close** Price

## How it Works
1. **Data Preprocessing:** The historical stock data is cleaned, sorted by date, and normalized between -1 and 1 using `MinMaxScaler` from Scikit-Learn to help the neural network learn faster.
2. **Sequence Generation:** The data is split into sequences. The model looks at a rolling training window of the past **7 days** to predict the stock's closing price on the next day.
3. **Model Architecture:** 
   * Input Size: 4 (High, Low, Open, Close)
   * Hidden Layers: 100
   * Output Size: 1 (Predicted Close Price)
   * Optimizer: Adam (Learning Rate = 0.001)
   * Loss Function: Mean Squared Error (MSE)

## Requirements
To run this notebook on your own machine, you will need Python installed along with the libraries listed in the `requirements.txt` file.

You can install them quickly using pip:
```bash
pip install -r requirements.txt
