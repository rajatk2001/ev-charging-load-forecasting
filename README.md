# ev-charging-load-forecasting

"The future of mobility is electric. The future of energy is intelligent. SmartCharge bridges them."
---

## 🚀 Features
* End-to-End Data Pipeline
*  Machine Learning & Deep Learning Models
* Visualization & Insights
* Model Evaluation Framework
* Industry Relevance & Business Impact

  ---
  ## 📁 Repository Structure
  **Forecast next-day/hourly EV charging demand/** <>
1. README.md /                 # Project overview
2. data/                      # Raw and preprocessed datasets
3. models/
   -data_preprocessing.ipynb
   - exploratory_data_analysis.ipynb
   - baseline_forecasting.ipynb
   - ml_forecasting.ipynb
   - evaluation.ipynb
   - results_visualization.ipynb
  4. notebooks/             # Jupyter notebooks for analysis
  5. requirements.txt       # Python dependencies
---
## 📊 Dataset  
**Source**: [ACN EV Charging Dataset (Caltech)](https://ev.caltech.edu/dataset)  
- Contains real EV charging sessions:  
  - `session_id`, `station_id`  
  - `start_time`, `end_time`, `duration`  
  - `energy_kWh`, `max_power`  
- Clean CSV format, easy to preprocess.
---
## 🧠 Workflow  

1. **Problem Statement** – Forecast next-day/hourly EV charging demand.  
2. **Data Preprocessing** – Convert logs to time-series, create features.  
3. **EDA** – Explore peak hours, weekday/weekend patterns, seasonal cycles.  
4. **Baseline Models** – Moving Average, ARIMA, Prophet.  
5. **ML/DL Models** – XGBoost, LSTM, GRU, Transformers.  
6. **Evaluation** – Compare models using RMSE, MAE, MAPE.  
7. **Results** – Plots + error tables, highlighting best-performing model.  
8. **Optional** – Streamlit dashboard for interactive forecasts.
----
## 📈 Sample Results  

| Model       | RMSE   | MAE   | MAPE  |
|-------------|--------|-------|-------|
| ARIMA       | 52.4   | 38.2  | 9.8%  |
| Prophet     | 47.1   | 35.7  | 8.5%  |
| XGBoost     | 43.9   | 32.1  | 7.9%  |
| LSTM        | 39.3   | 28.4  | 6.7%  |
| Transformer | 37.5   | 27.1  | 6.1%  |

📊 Forecast Visualization:  
![Forecast Plot](assets/sample_forecast.png) 
---
## 🚀 Business Value     
- 💰 **Dynamic Pricing** – optimize tariffs based on predicted demand.
- ⚡ **Grid Operators** – anticipate demand spikes & prevent overloads.
- 🏙️ **City Planners** – decide where to install new charging stations.
----
## 🔹 Future Work

*
---
# Install dependencies
pip install -r requirements.txt

# Run notebooks
jupyter notebook
---
## 📞 Contact

Created by **RAJAT KUMAR MISHRAr**. Reach out via [GitHub Issues](...) for questions or suggestions.

