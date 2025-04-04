# lstm-stock-market-prediction
# 📈 LSTM Stock Market Price Prediction

This project demonstrates the use of Long Short-Term Memory (LSTM) networks for forecasting stock prices using historical data. The goal is to explore the power of deep learning in time-series prediction by training an LSTM model on Apple Inc. (AAPL) stock prices.

---

##  Overview

Using historical stock data, this project:
- Preprocesses and cleans the dataset.
- Normalizes price values for stable training.
- Generates time-series sequences.
- Trains a deep LSTM network to predict future closing prices.
- Evaluates model performance using metrics and visualizations.

---

## Files Included

- `AAPL_historical_data.csv`: Raw stock price data (Date, Open, High, Low, Close, Volume).
- `Code LSTM STOCK MARKET.html`: Full code notebook for data processing, model training, and visualization.
- `REPORT_LSTM.pdf`: Summary report explaining each step and model performance.

---

## Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib

---

##  Methodology

### 1. Data Preprocessing
- Cleaned data, removed null values.
- Converted "Date" to datetime and set it as index.
- Selected "Close" prices as the target variable.

### 2. Normalization
- Applied Min-Max Scaling to [0, 1] range.

### 3. Sequence Creation
- Created input sequences of 50-day closing prices to predict the 51st day.
- Split into 80% training and 20% testing sets.

### 4. Model Architecture
- **2 LSTM Layers** with 50 units each.
- **Dropout Layers** (20%) to prevent overfitting.
- **Dense Layers** for final prediction.
- Optimizer: Adam  
- Loss Function: Mean Squared Error (MSE)

### 5. Training & Evaluation
- Trained for 50 epochs with batch size 32.
- Achieved low training and validation loss:
  - Training Loss: ↓ 0.0023 to **1.1072e-04**
  - Validation Loss: ↓ 9.77e-04 to **9.80e-04**
- Detected slight overfitting, but generalization remained strong.

---

##  Results

- The model accurately captured price trends and predicted future values with high precision.
- Effective use of LSTM's memory retention for sequential patterns.

---

## Conclusion

This project demonstrates the effectiveness of LSTM networks in stock price prediction and serves as a foundation for more advanced financial forecasting. Future improvements could include:
- Incorporating additional features (Open, High, Volume)
- Applying attention mechanisms
- Hyperparameter tuning

---

## 🔗 Author

Adithya CH 
MSc Data Science | Aspiring Data Scientist  
[LinkedIn](https://www.linkedin.com/in/adithya-c-h-589345291)  | [GitHub](https://github.com/Adithyme)
