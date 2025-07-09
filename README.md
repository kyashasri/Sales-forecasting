# 📈 Sales Forecasting using LSTM

This project focuses on forecasting chocolate product sales using **LSTM (Long Short-Term Memory)** — a type of Recurrent Neural Network designed for sequence modeling and time series prediction.

🚀 **Live App**: [Click here to try it on Streamlit](https://yashasri-sales-forecast.streamlit.app/)

---

## 🧠 LSTM Approach

LSTM is well-suited for capturing temporal dependencies in sequential data like monthly or weekly sales. Here's a breakdown of the process I followed:

### 🧹 Data Preprocessing

- ✅ **Outlier removal** to clean noisy spikes in sales data  
- ✅ **Smoothing and interpolation** for missing or irregular values  
- ✅ **Sequence creation** with `seq_len = 4` (i.e., using the last 4 time steps to predict the next one)

### 🏗️ Model Building

- Used **Keras LSTM layers** with:
  - EarlyStopping to prevent overfitting
  - Best epoch selection based on validation loss
- Compared **actual vs predicted sales** for evaluation

### 📊 Evaluation Metrics

| Metric      | Value     |
|-------------|-----------|
| **MAPE**     | 7.4%      |
| **MAE**      | 802.2     |
| **RMSE**     | 1083.0    |
| **RMSE %**   | 9.6%      |
| **R² Score** | 0.90      |

The model showed strong accuracy, explaining **90% of the variance** in sales data.

---

## 🔮 Future Forecasting

After training, the model was used to forecast **sales for the next 4 weeks** for each product, helping visualize expected trends and aiding in planning.

---
