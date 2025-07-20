
# 🪙 Gold Price Forecasting Using Time Series Analysis (ARIMA & SARIMA)

This project performs in-depth **time series analysis** and **forecasting** on monthly gold prices using **ARIMA** and **SARIMA** models. It also features a full-fledged **Streamlit app** for interactive exploration, model selection, and dynamic forecasting.

---

## 📦 Project Features

### ✅ Time Series Workflow Includes:
- Downloading gold price data from **Yahoo Finance**
- **Visualization** of trends over time
- **STL decomposition** to separate trend, seasonality, and noise
- **ADF test** for stationarity
- **Differencing** to make the series stationary
- **ACF and PACF plots** to determine model orders
- **Model building** with ARIMA and SARIMA
- **Forecasting** next 12 months
- **Model comparison** using AIC/BIC
- **Model saving** using pickle

### ✅ Interactive Streamlit Web App:
- Choose between ARIMA and SARIMA models
- Forecast up to 36 months into the future
- Visualize forecast with **confidence intervals**
- View model summary and raw historical data

---

## 🗃️ Repository Structure

```

📁 gold-price-forecasting/
├── app.py                   # Streamlit app
├── arima\_gold\_model.pkl     # Trained ARIMA model (auto-generated)
├── sarima\_gold\_model.pkl    # Trained SARIMA model (auto-generated)
├── model\_training.ipynb     # Main analysis & modeling notebook
├── requirements.txt         # Required packages
└── README.md                # Project overview

````
---

## 🧠 Model Details

| Model  | AIC / BIC | Seasonality | Stationarity | Forecast Horizon |
| ------ | --------- | ----------- | ------------ | ---------------- |
| ARIMA  | Evaluated | ❌ No        | Differenced  | Short-term       |
| SARIMA | Evaluated | ✅ Yes       | Differenced  | Seasonal-aware   |

### 🔬 ACF & PACF Interpretation Tips:

* ACF with spikes at seasonal lags → Add seasonal terms
* PACF cut-off after lag `p` → Suggests AR model order
* ACF cut-off after lag `q` → Suggests MA model order

---

## 🧪 ADF Test Result Sample Output

```
ADF Statistic: -1.56
p-value: 0.51
Conclusion: Time series is **non-stationary**. Differencing is required.

Concusions based on ACF and PACF Plots -> 
(1) Significant spikes are seen at lag 10
(2) PACF cuts after lag (p = 1)
(3) ACF cuts after lag (q = 1)

```

---

## 🧰 Technologies Used

* `Python`
* `Pandas`, `Matplotlib`, `Statsmodels`
* `yfinance` for data fetching
* `Streamlit` for UI
* `Pickle` for model persistence

---

## 📄 License

This project is open-source 

---

## 👤 Author

Developed by **\[Madhura Tonpe]**
📧 Madhura.tonpe@gmail.com
🌐 github.com/MadhuraTonpe165/time_series_model

---

## 📌 `requirements.txt`

If you want to deploy or share the project, use this for your `requirements.txt`:

```

streamlit
pandas
matplotlib
statsmodels
yfinance
python-dateutil

```


