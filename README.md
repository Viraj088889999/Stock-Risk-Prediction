# Stock-Risk-Prediction
Machine Learning project to classify stock market risk using Z-Score and multiple classification algorithms.


# Stock Risk Prediction using Machine Learning

## Predicting the Next Trading Day Risk Level using Historical Stock Market Data

### Developed by

**Viraj Waikar**

---

## Project Overview:

This project focuses on predicting the **next trading day's stock risk level** using Machine Learning algorithms. 
Historical stock market data was collected using Yahoo Finance (`yfinance`), 
followed by feature engineering, data preprocessing, model training, evaluation, and prediction.

The project compares multiple Machine Learning models to identify the best-performing algorithm for stock risk classification.

---
##  Business Problem

Investors and traders face uncertainty due to daily fluctuations in stock prices. Identifying whether the next trading day carries a **Low**, **Medium**, or **High** level of risk can support better decision-making and risk management.

Traditional analysis often requires manual interpretation of historical market trends. This project demonstrates how Machine Learning can automate risk classification by learning patterns from historical stock market data.

---
## Project Objective

The primary objective of this project is to build a Machine Learning model capable of predicting the **next trading day's stock risk category**.

The project includes:

- Collecting historical stock market data using Yahoo Finance (`yfinance`)
- Cleaning and preprocessing the dataset
- Engineering meaningful features
- Creating a target variable for next-day prediction
- Training multiple Machine Learning models
- Comparing model performance
- Selecting the best-performing model
- Saving the trained model for future predictions

---
##  Dataset Information

The dataset was collected using the **Yahoo Finance API (`yfinance`)**, which provides historical stock market data.

### Dataset Features

| Feature | Description |
|----------|-------------|
| Open | Opening price of the stock |
| High | Highest price during the trading day |
| Low | Lowest price during the trading day |
| Close | Closing price of the stock |
| Volume | Number of shares traded |
| Return | Daily percentage return calculated from closing prices |
| ZScore | Standardized return used to measure market volatility |
| Risk_Class | Risk category (Low, Medium, High) based on Z-Score |
| Target | Next trading day's risk category used for prediction |

---
## Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Programming Language |
| Pandas | Data Cleaning & Analysis |
| NumPy | Numerical Computations |
| Matplotlib | Data Visualization |
| Seaborn | Statistical Visualization |
| Scikit-learn | Machine Learning Models |
| yfinance | Historical Stock Data Collection |
| Joblib | Model Serialization |
| Jupyter Notebook | Project Development |

---
## Machine Learning Workflow

The project follows a complete Machine Learning pipeline:

1. Collect historical stock data using Yahoo Finance.
2. Perform data cleaning and preprocessing.
3. Calculate daily stock returns.
4. Compute Z-Score for volatility analysis.
5. Classify each day into Low, Medium, or High Risk.
6. Create the next-day target variable.
7. Split the dataset into training and testing sets.
8. Apply feature scaling.
9. Train multiple Machine Learning models.
10. Compare model performance.
11. Select the best-performing model.
12. Save the trained model, scaler, and label encoder.
13. Predict the next trading day's stock risk.

---
##  Machine Learning Models Used

To identify the most suitable algorithm for stock risk prediction, multiple Machine Learning models were trained and evaluated.

The following classification algorithms were implemented:

| Model | Purpose |
|--------|---------|
| K-Nearest Neighbors (KNN) | Baseline distance-based classification model |
| Decision Tree | Rule-based classification model |
| Random Forest | Ensemble learning model with feature importance analysis |
| Support Vector Machine (SVM) | Classification model for finding the optimal decision boundary |

The performance of all models was evaluated using the testing dataset, and the best-performing model was selected for final deployment.

---
## 📊 Model Performance Comparison

| Machine Learning Model | Accuracy |
|-------------------------|----------|
| K-Nearest Neighbors (KNN) | 68.49% |
| Decision Tree | 54.79% |
| Random Forest | 71.23% |
| Support Vector Machine (SVM) | 76.71% |

###  Best Performing Model

The **Support Vector Machine (SVM)** achieved the highest prediction accuracy and was selected as the final model for predicting the next trading day's stock risk.

---
##  Feature Importance

The Random Forest model was used to analyze feature importance and understand which variables contributed the most to predicting stock risk.

Important features included:

- Daily Return
- Z-Score
- Closing Price
- Trading Volume

This analysis improves model interpretability by identifying the variables that have the greatest influence on stock risk prediction.

---
## Final Prediction

After evaluating multiple Machine Learning algorithms, the **Support Vector Machine (SVM)** was selected as the final model due to its superior performance on the testing dataset.

The trained model predicts the **next trading day's stock risk level** by classifying it into one of the following categories:

- 🟢 Low Risk
- 🟡 Medium Risk
- 🔴 High Risk

The prediction is based on historical stock market data and engineered features such as Daily Return and Z-Score.

---
##  Business Insights

This project demonstrates how Machine Learning can support financial risk analysis by identifying potential market risk levels before the next trading session.

### Key Insights

- Historical stock price movements contain patterns that can be learned using Machine Learning.
- Feature engineering significantly improves prediction performance.
- Comparing multiple algorithms helps identify the most suitable model.
- Support Vector Machine (SVM) provided the highest prediction accuracy among all evaluated models.
- Predicting future risk levels can assist investors in making more informed decisions.

---
##  Project Limitations

Although the project achieved good prediction performance, it has several limitations:

- The model uses only historical stock market data.
- External factors such as news events, economic policies, and market sentiment are not considered.
- Performance may vary across different stocks and market conditions.
- Hyperparameter tuning was limited and could be further optimized.

---
##  Future Improvements

The project can be enhanced by:

- Including technical indicators such as RSI, MACD, and Moving Averages.
- Using deep learning models such as LSTM for time-series forecasting.
- Incorporating financial news sentiment analysis.
- Performing hyperparameter optimization.
- Deploying the trained model as a web application using Flask or Streamlit.

---
##  Project Structure

```text
Stock-Risk-Prediction/
│
├── Stock_Risk_Prediction.ipynb      # Complete Machine Learning notebook
├── README.md                        # Project documentation
├── requirements.txt                 # Python dependencies
│
├── dataset/
│   └── stock_data.csv               # Historical stock market dataset
│
├── models/
│   ├── stock_risk_model.pkl         # Trained SVM model
│   ├── scaler.pkl                   # Saved feature scaler
│   └── label_encoder.pkl            # Saved label encoder
│
└── images/
    ├── 01_dataset_preview.png
    ├── 02_risk_class_distribution.png
    ├── 03_target_verification.png
    ├── 04_model_comparison_table.png
    ├── 05_model_comparison_chart.png
    ├── 06_feature_importance.png
    └── 07_final_prediction.png
```

---
##  How to Run the Project

### Step 1

Clone the repository.

```bash
git clone https://github.com/Viraj088889999/Stock-Risk-Prediction.git
```

### Step 2

Install the required Python libraries.

```bash
pip install -r requirements.txt
```

### Step 3

Open the Jupyter Notebook.

```bash
jupyter notebook
```

### Step 4

Run all notebook cells sequentially to reproduce the complete Machine Learning workflow.

---
## 🏁 Conclusion

This project demonstrates an end-to-end Machine Learning workflow for predicting the next trading day's stock risk using historical market data.

Starting from data collection and preprocessing, the project applies feature engineering, compares multiple Machine Learning algorithms, evaluates their performance, and deploys the best-performing model for prediction.

The project highlights practical applications of Machine Learning in financial risk analysis while following industry-standard practices such as model serialization, reproducibility, and structured project organization.

---

