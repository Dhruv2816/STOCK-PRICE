# Stock Price Prediction using LSTM  

## Project Overview  
The **Stock Price Prediction** project utilizes **Long Short-Term Memory (LSTM)** neural networks to forecast future stock closing prices. By leveraging historical stock data, this model aims to provide valuable insights for traders and investors. The approach is **generalized** and can be applied to predict the stock prices of **any company** with minimal modifications.  

## Technologies Used  
- **Python** – Core programming language for data analysis and model development.  
- **Pandas** – Data preprocessing and manipulation.  
- **NumPy** – Numerical computations.  
- **Matplotlib & Seaborn** – Data visualization.  
- **yFinance** – Fetching historical stock price data from Yahoo Finance.  
- **Scikit-Learn** – Data scaling using `MinMaxScaler`.  
- **Keras & TensorFlow** – Building and training the LSTM neural network.  

## Data Collection  
Historical stock price data is collected using the **yFinance** library. The dataset includes:  
- **Open, High, Low, Close, Volume, and Adjusted Close** prices.  
- A customizable date range (e.g., **January 1, 2005 – December 31, 2024** for testing).  

## Data Preprocessing  
1. **Handling Missing Values** – Any rows with missing data are dropped.  
2. **Feature Selection** – Only the **‘Close’** price is used for prediction.  
3. **Scaling** – The data is normalized to a range of **0 to 1** using `MinMaxScaler`.  
4. **Train-Test Split** – Data is divided into:  
   - **80% training set**  
   - **20% testing set**  
5. **Generating Sequences** – The model takes sequences of **100 days** as input to predict the next day's closing price.  

## Model Development  
The **LSTM model** is built using the **Keras** library with the following architecture:  
- **Four LSTM layers** with units (50, 60, 80, 120)  
- **Dropout layers** after each LSTM layer to prevent overfitting  
- **Dense layer** to produce the final output  
- Compiled using:  
  - **Optimizer** – `adam`  
  - **Loss function** – `mean squared error (MSE)`  

## Model Training  
- Trained for **50 epochs** with a **batch size of 32**.  
- The model minimizes the **loss function** to optimize prediction accuracy.  

## Results and Predictions  
- The trained model predicts stock prices on the test dataset.  
- Predictions are visualized against actual prices to evaluate performance.  
- The model provides insights into stock trends based on historical data.  

## Deployment  
- A **web application** is built to allow users to input a date range and get predicted stock prices.  
- This enables **real-time predictions** with a user-friendly interface.  

## Future Enhancements  
- **Incorporate More Features** – Include trading volume, technical indicators, and news sentiment analysis.  
- **Model Optimization** – Experiment with different architectures and hyperparameters.  
- **Expand to More Stocks** – Generalize the model for multiple stock predictions.  
- **Real-time Data** – Integrate live stock data for up-to-date forecasting.  

## Conclusion  
This project demonstrates the potential of **LSTM neural networks** for **time series forecasting** in stock price prediction. By providing **accurate forecasts** and an **interactive web interface**, the model can assist traders and investors in making **informed decisions**.  
