
# 📈 UnitedHealth Group (UNH) Stock Movement Prediction

This project uses historical stock price data of **UnitedHealth Group (UNH)** to predict the **next day's stock movement** (up or down) using a **Random Forest Classifier**. It demonstrates how machine learning can be applied in financial market analysis with real stock data.

---

## 🧠 Model Objective

Predict whether the stock price of UNH will go **up (`1`)** or **down (`0`)** the next day based on the past 5 days of returns.

---

## 📂 Project Structure

| Section | Description |
|--------|-------------|
| 📥 Data | Downloaded using `yfinance` for UNH from 2018 to June 22, 2025 |
| 🔬 Features | 5 lagged daily return values |
| 🧠 Model | Random Forest Classifier (`scikit-learn`) |
| 📊 Output | Confusion matrix, classification report, and comparison chart of actual vs predicted movement |

---

## 🔧 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `yfinance`
- `scikit-learn`

---

## 🚀 How It Works

1. **Download Data**: Pulls UNH stock data from Yahoo Finance.
2. **Feature Engineering**:
   - Calculates daily returns.
   - Creates 5 lagged return features (`Return_Lag_1` to `Return_Lag_5`).
   - Adds a binary `Direction` column: `1` if return is positive, `0` otherwise.
3. **Train/Test Split**: Uses 80% for training, 20% for testing (no shuffle to preserve time sequence).
4. **Train Model**: A Random Forest Classifier is trained.
5. **Evaluate Model**: Accuracy, confusion matrix, and classification report are printed.
6. **Visualize**: Actual vs. predicted direction plotted over time.

---

## 📉 Sample Output

- **Confusion Matrix**:
  Shows how well the model predicted each class.

- **Classification Report**:
  Includes precision, recall, f1-score.

- **Prediction Chart**:

  ![Prediction Chart](example_plot.png) *(Replace with your actual plot if hosted on GitHub)*

---

## ✅ Example Result

```
Accuracy: 0.63
              precision    recall  f1-score   support

           0       0.60       0.58       0.59       100
           1       0.66       0.68       0.67       120

    accuracy                           0.63       220
```

---

## 📌 Future Enhancements

- Add **technical indicators** like RSI, MACD, Bollinger Bands
- Try **deep learning models** (LSTM for time series)
- Add **Streamlit dashboard** for interactive analysis

---

## 👨‍💻 Author

Harshit Nahata  
Computer Science & Engineering | AI & Finance Enthusiast
