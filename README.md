#EV-CHARGING-LOAD-FORECASTING

"The future of mobility is electric. The future of energy is intelligent. SmartCharge bridges them."
---
## 🎯 Motivation  
- The Netherlands is a European leader in **EV adoption and workplace charging infrastructure**.  
- Office charging behavior is **unique**: weekday-dominated, linked to work hours, and influenced by holidays.  
- Accurate demand forecasting helps:  
  - **Grid operators** manage local electricity loads.  
  - **Businesses** optimize office charging stations.  
  - **Policy makers** plan for future EV adoption.
 
    ---
## 🚀 Features
* End-to-End Data Pipeline
*  Machine Learning & Deep Learning Models
* Visualization & Insights
* Model Evaluation Framework
* Industry Relevance & Business Impact

  ----

  
## 📊 Dataset  
**Source**: Real-world EV charging sessions at **office locations in the Netherlands** (2020–2024).  
- **Features**:  
  - `session_start`, `session_end` → timestamps  
  - `energy_delivered (kWh)`  
  - `station_id`
  - **Preprocessing**:  
  - Filtered for office locations.  
  - Aggregated into **daily energy demand (kWh)**.  
  - Created features: weekdays/weekends, rolling averages, lags, holidays.

---

## 🔍 Methodology  

### 1. Data Preprocessing  
- Cleaned timestamps and missing values.  
- Resampled into **daily demand** time series.  
- Added calendar-based features for better forecasting.  

### 2. Exploratory Data Analysis (EDA)  
- **Trend**: Rising office EV demand from 2020 → 2024.  
- **Seasonality**: Weekly cycles (low weekends), yearly dips (holidays).  
- **Office Behavior**: High demand during working days/hours.  

### 3. Forecasting Models  
-  **Baseline**:  
  - Moving Average (MA7, MA30).  
- **Statistical**:  
  - ARIMA → captures trend and seasonality.  
- **Machine Learning**:  
  - XGBoost Regression → captures nonlinear relationships, weekday-weekend effects, and holiday dips.  

---
### 4. Evaluation  
- **Train**: 2020–2023.  
- **Test**: 2024.  
- Metrics: **RMSE, MAE, MAPE**.

  ---
  
## 📊 Results  
## 📊 Forecasting Results (2024 Test Data)

| Model            | MAE     | RMSE    | MAPE %   | SMAPE %   | Strengths                          | Weaknesses                           |
|------------------|---------|---------|----------|-----------|------------------------------------|---------------------------------------|
| MA(7)            | 0.0966  | 0.9160  | 100.00   | 2.22      | Very simple baseline                | Ignores seasonality & trend           |
| MA(30)           | 0.0966  | 0.9160  | 100.00   | 2.22      | Smooths longer-term trend           | Misses short-term fluctuations        |
| ARIMA            | 0.1556  | 0.9116  | 99.31    | 199.97    | Good at capturing trend & seasonality | Weak on irregular office-day spikes   |
| **XGBoost** ✅   | 0.3078  | 0.9297  | 92.70    | 199.70    | Best generalization, non-linear effects | Needs careful feature engineering     |

➡ **XGBoost outperformed ARIMA and baseline models**, producing the most reliable forecasts for office EV charging demand in 2024.  


## ✅ Conclusion  
- **ARIMA** → effective for capturing general trend and seasonality but weaker on irregular weekday office patterns.  
- **XGBoost** → leveraged nonlinear features, weekday/weekend cycles, and holiday effects for higher accuracy.  
- **Impact**: This forecasting approach can directly support **grid planning, office EV station optimization, and policy decision-making** in the Netherlands.  

---

## 📌 Tech Stack  
- **Python** (Pandas, Numpy, Scikit-learn, Statsmodels)  
- **ARIMA** (statsmodels)  
- **XGBoost**  
- **Matplotlib / Seaborn** (visualization)  
- **Jupyter Notebooks**  


📊 Forecast Visualization:  


## 🤝 Contributing  
Feel free to fork this repo and suggest improvements via Pull Requests.  

---

## 📧 Contact  
👤 **Name** - Rajat kumar Mishra  
📩 [rarajatk2001@gmail.com]  
🔗 [https://www.linkedin.com/in/rajat-kumar-mishra-a662ba368]  


