# Sales Forecasting – SIEMENS (POC)

This project explores the use of **AI-driven Time Series Forecasting models to predict product group Sales** for **SIEMENS**, a multinational technology company. The goal was to provide accurate 10-month sales forecasts using both internal and macroeconomic data, and to support business planning and inventory optimization.

---

## Project Objective

- Predict monthly sales for multiple product groups over a 10-month horizon  
- Leverage internal sales data and macroeconomic indicators  
- Reduce forecasting bias and manual workload by using machine learning models  
- Deliver reliable, explainable forecasts and propose a strategy for long-term model maintenance

---

## Methods & Techniques

- Followed the **CRISP-DM framework**  
- Preprocessed time series data using **ADF test**, feature engineering (e.g., sin/cos of month), and **Granger Causality Tests**  
- Created group-specific feature sets to tailor predictions  
- Trained and evaluated multiple forecasting models:
  - **XGBoost** ✅ (Best performing)
  - Linear Regression  
  - ARIMA  
  - AdaBoost  
  - HistGradientBoosting (excluded due to underperformance)

---

## Datasets Used

- `Case2_Sales.csv` – Internal sales data (Oct 2018 – Apr 2022, 43 months)  
- `Case2_Market.xlsx` – Macroeconomic indicators (218 months, 18+ years)  
- `Case2_Test_Set_Template.csv` – Evaluation template for May 2022 – Feb 2023 forecasts  

---

## Evaluation & Results

- Used **Root Mean Squared Error (RMSE)** and **Root Mean Squared Percentage Error (RMSPE)** to evaluate model accuracy  
- Addressed calculation nuance to stay faithful to mathematical definitions  
- Observed that groups with higher sales volume (Groups #1, #3, and #4) yielded better predictions  
- Final model: **XGBoost**, trained individually per product group

---

## Tools & Libraries

- Python  
- pandas, NumPy  
- XGBoost, statsmodels, scikit-learn  
- matplotlib, seaborn  
- Jupyter Notebook  

---

## Key Insights

- Model performance varied by product group due to volume and seasonal patterns  
- Granger Causality helped identify macroeconomic features with predictive power  
- Avoided synthetic data to maintain model integrity and reduce bias

---

## Deployment & Maintenance

- Designed a **development and maintenance plan**  
- Included guidelines for model retraining, feature update schedules, and performance monitoring

---

## Developed By

- **Moeko Mitani** [LinkedIn](https://www.linkedin.com/in/moeko-mitani/)  
- Ana Caleiro
- Duarte Marques
- Oumaima Ben Hfaiedh 
- Sarah Leuthner
