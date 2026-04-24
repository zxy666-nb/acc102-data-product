# 📊 Macroeconomic & Financial Asset Dashboard

**Author:** Xiaoyue.Zhang  
**Module:** ACC102 Mini Assignment - Track 4 (Interactive Tool)

## 1. Problem & Target User
Retail investors often find it difficult to visualize how abstract macroeconomic data (like inflation or employment figures) impacts the specific assets they hold (e.g., TSLA, NVDA, or BTC). This interactive dashboard bridges that gap by providing a unified interface to correlate **complex macroeconomic indicators** with **real-time asset performance**, empowering users with data-backed strategic context.

## 2. Product Access
* **Live Web App:** https://finscopemacro.streamlit.app/
* **Demo Video (1-3 mins):** [Your Demo Video Link Here]

## 3. Data Sources
* **Financial Market Data:** Real-time historical price data (Open, High, Low, Close, Volume) fetched dynamically via the `yfinance` API.
* **Macroeconomic Indicators:** US economic data (CPI YoY, Non-Farm Payrolls, Jobless Claims) fetched directly from the **Federal Reserve Economic Data (FRED) API**.
* **Simulation Engine:** Includes a robust fallback mechanism using `numpy` and `pandas` to ensure analytical stability during API rate-limiting or maintenance.

## 4. Technical Execution
* **Data Alignment:** Implemented `.resample('MS').last()` to align daily market volatility with monthly macroeconomic reporting cycles.
* **Statistical Engine:** Calculated the **Pearson Correlation Coefficient (r)** to quantify the linear strength between inflation trends and asset price action.
* **Modern UI:** Built with `streamlit` using a multi-tab architecture (`st.tabs`) for clear logical separation between Macro, Market, and Correlation modules.
* **AI Strategy:** Integrated the **DeepSeek-V3** large language model (via OpenAI-compatible API) to provide automated PEST strategic analysis.

## 5. 🔒 Security & Professional Practice
To adhere to professional cybersecurity standards and XJTLU academic integrity:
* **Credential Protection:** The DeepSeek API key is managed via **Streamlit Secrets** (`st.secrets`). This ensures that sensitive credentials are never "hardcoded" or leaked into the public GitHub repository history.
* **Error Handling:** The application is designed with a "Graceful Failure" logic—if an API is unavailable, the tool switches to an "Academic Mode" to ensure the user experience is not interrupted.

## 6. Key Findings & Insights
The dashboard automatically generates interpretations based on data outputs:
* **Market Decoupling:** In periods where $|r| < 0.3$, the tool identifies a "decoupling" effect, suggesting that price action is driven by **institutional liquidity sweeps** rather than fundamental macro shifts.
* **Inverse Sensitivity:** The analysis tracks how high CPI prints often lead to capital rotation into "safe havens," a trend clearly visualized in the combined line charts.

## 7. How to Run Locally
1. Clone this repository to your local machine.
2. Install the necessary dependencies:  
   `pip install -r requirements.txt`
3. Launch the dashboard:  
   `streamlit run app.py`

## 8. Limitations & Future Development
* **Limitations:** The current model focuses on linear correlation; future updates will incorporate Non-linear Regression for better anomaly detection.
* **Future Scope:** Integration of real-time Sentiment Analysis from financial news to supplement the PEST strategy module.
