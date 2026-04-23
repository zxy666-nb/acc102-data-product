# acc102-data-product
# Macroeconomic & Financial Asset Dashboard
**Author:** Xiaoyue.Zhang
**Module:** ACC102 Mini Assignment - Track 4

## 1. Problem & User
This tool addresses the difficulty retail investors face in correlating macroeconomic shifts with specific asset price movements. It provides an interactive interface for students and investors to visualize how US inflation (CPI) and employment data (NFP) impact individual stock performance (e.g., TSLA, NVDA).

## 2. Data
* **Financial Data:** Historical and live stock prices fetched from Yahoo Finance via the `yfinance` library.
* **Macroeconomic Data:** Simulated indicators for US CPI (YoY), Non-Farm Payrolls, and Jobless Claims.
* **Access Date:** April 2026.
* **Key Fields:** Close Price, Moving Averages (MA20), CPI Actual/Forecast, Pearson Correlation Coefficient.

## 3. Methods
1. **Data Resampling:** Used `.resample('ME').last()` to align daily stock prices with monthly macro indicators.
2. **Correlation Modeling:** Implemented Pearson Correlation analysis to quantify the linear relationship between variables.
3. **Interactive Visualization:** Developed a Streamlit interface with dynamic charting and metric comparisons.
4. **AI Integration:** Integrated DeepSeek API for automated PEST (Political, Economic, Social, Technological) strategic analysis.

## 4. Key Findings
* **Macro Sensitivity:** Identified measurable correlations between US CPI fluctuations and target asset volatility.
* **Expectation Gap:** Observed how price movements often react more to the "Actual vs. Forecast" delta than the raw figure itself.
* **Strategic Insight:** The AI-driven PEST analysis revealed that technological factors often outweigh short-term economic headwinds for high-growth tickers.

## 5. How to run
1. Install dependencies: `pip install -r requirements.txt`
2. Launch the dashboard: `streamlit run app.py`
3. Enter a ticker symbol in the sidebar to begin analysis.

## 6. Product link / Demo
* **Live App:** [Insert Streamlit Link]
* **Demo Video:** [Insert Video Link]

## 7. Limitations & next steps
* **Data Authenticity:** The macro engine currently uses simulated data; future versions will integrate the FRED API for real-time government statistics.
* **Predictive Modeling:** Next steps involve adding a Machine Learning module to forecast asset prices based on leading macro indicators.
