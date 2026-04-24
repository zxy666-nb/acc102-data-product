Interactive Macro-Finance Dashboard & AI Strategy Analyzer
Author: Xiaoyue.Zhang

1. Problem Definition & Target User
Retail investors and business students often struggle to understand how macroeconomic shifts (like inflation) directly impact specific asset prices. This interactive dashboard bridges that gap by providing a unified visualization tool that calculates correlations and leverages AI to generate strategic PEST (Political, Economic, Social, Technological) insights.

Target Users: * Business and Accounting students analyzing market drivers.

Retail traders seeking data-backed context for price movements.

2. Product Access
Live Web App: [在此处粘贴你的 Streamlit 链接]

Demo Video (1-3 mins): [在此处粘贴你的演示视频链接]

3. Data Sources
Financial Data: Real-time historical monthly close prices fetched via the yfinance API.

Macroeconomic Indicators: Simulated CPI (Consumer Price Index) YoY and NFP (Non-Farm Payroll) data, structured for academic correlation testing.

Scope: Rolling 12-month analysis based on user-selected tickers.

4. Technical Execution
Data Pipeline: Utilized pandas for multi-source data merging, resampling (daily to monthly), and temporal alignment.

Statistical Logic: Implemented Pearson Correlation Coefficient calculations to quantify the linear relationship between inflation and asset performance.

Frontend: Developed with streamlit using an advanced layout (st.tabs, st.columns) for a professional user experience.

AI Integration: Connected to the DeepSeek API for automated, real-time strategic interpretation of market conditions.

5. 🔒 Security & API Key Management
In line with professional software development standards, this project implements a dual-layer security strategy for API credentials:

Cloud Deployment: The live application utilizes Streamlit’s encrypted st.secrets management, ensuring the API key is never exposed in the source code.

Local Execution: To protect developer credentials while maintaining functionality, the app includes a dynamic sidebar password input. Users running the repo locally are prompted to provide their own key, ensuring that no sensitive "hardcoded" strings are committed to the public GitHub history.

6. Key Findings & Analysis
The tool provides automated insights based on mathematical outputs:

Correlation Decoupling: In scenarios where the correlation (r) is low (e.g., < 0.3), the tool identifies a "decoupling" effect.

Market Insight: As demonstrated in the analysis, low correlation suggests that price action is likely driven by institutional liquidity sweeps or macro-political events rather than basic economic fundamentals—adding a layer of sophisticated interpretation beyond simple charting.

7. How to Run Locally
Clone the repository: git clone [Your Repo URL]

Install dependencies: pip install -r requirements.txt

Run the app: streamlit run app.py

Note: Enter your DeepSeek API Key in the sidebar to activate the "Strategic Analysis" module.

8. Reflection & Limitations
Limitations: The macro data currently uses a simulated walk to ensure consistency for the assignment. Future iterations will integrate the fredapi for live Federal Reserve data.

Scalability: The architecture is designed to easily scale from simple correlation to multi-variable regression analysis.
