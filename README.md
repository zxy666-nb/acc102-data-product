# 📊 Macroeconomic & Financial Asset Dashboard
**Author:** Xiaoyue.Zhang
**Module:** ACC102 Mini Assignment - Track 4

## 1. Problem & User
This tool addresses the difficulty retail investors and students face in correlating complex macroeconomic shifts with specific asset price movements. It provides an interactive interface to visualize how US inflation (CPI), Non-Farm Payrolls (NFP), and Jobless Claims impact individual asset performance (e.g., TSLA, NVDA, BTC-USD).

## 2. Data
* **Financial Data:** Historical and live asset prices fetched dynamically via the `yfinance` library.
* **Macroeconomic Data:** Real-time US economic indicators (CPI, NFP, Jobless Claims) fetched directly from the Federal Reserve Economic Data (FRED) API.
* **Access Date:** April 2026.
* **Key Fields:** Close Price, Moving Averages (MA20), CPI Actual vs Forecast, Pearson Correlation Coefficient.

## 3. Methods
1. **API Integration:** Automated live data extraction from Yahoo Finance and FRED.
2. **Data Resampling & Alignment:** Utilized Pandas `.resample('MS')` to accurately align daily asset prices with monthly macroeconomic indicator releases.
3. **Quantitative Modeling:** Implemented Pearson Correlation analysis to quantify the linear relationship between inflation and asset depreciation/appreciation.
4. **AI Strategic Integration:** Utilized DeepSeek API (secured via Streamlit Secrets) to generate real-time PEST (Political, Economic, Social, Technological) analysis based on current macro prints.

## 4. Key Findings
* **Macro Sensitivity:** High-growth tech assets and certain cryptocurrencies exhibit distinct volatility patterns immediately surrounding CPI and NFP release dates.
* **Expectation Gap:** Price delivery is heavily influenced by the delta between "Actual vs. Forecast" rather than the raw macroeconomic figure, triggering Smart Money liquidity sweeps.
* **Correlation Divergence:** Weak overall correlation often reveals that short-term price action is driven more by institutional order flow and macro-political events than long-term inflation trends.

## 5. How to run
1. Clone this repository to your local machine.
2. Install all required dependencies: `pip install -r requirements.txt`
3. Local Testing: Temporarily replace `st.secrets` with `st.sidebar.text_input` in `app.py` to input your API key.
4. Launch the application: `streamlit run app.py`

## 6. Product link / Demo
* **Live Web App:** [Insert your Streamlit Cloud link here]
* **Demo Video:** [Insert your 1-3 minute Demo video link here]

## 7. Limitations & next steps
* **Data Limits:** The FRED API integration provides high-quality data but is subject to occasional rate limits or timeout delays. An academic fallback (NumPy simulation) is built-in as a contingency.
* **Next Steps:** Future iterations aim to integrate Open Interest (OI) tracking and Machine Learning models to predict asset price reactions to unexpected macroeconomic prints. leading macro indicators.
