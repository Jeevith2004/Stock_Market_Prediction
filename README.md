<h1> <p style="text-align: center";>  <B> Stock Market Prediction </B> 

 <h2> Problem Background </h2>

 A dataset containing several daily features of S&P 500, NASDAQ Composite, Dow Jones Industrial Average, RUSSELL 2000, and NYSE Composite from 2010 to 2017.

The dataset provides extensive information on stock market trends, volatility, and performance of major indices, offering valuable insights for investors, traders, and financial analysts.

<h2> Core Components & Insights </h2>

  - Business-Relevant Insights: Beyond basic stock trend analysis, this project focuses on real-world financial applications such as risk assessment, anomaly detection, and market trend evaluation.

  - Comprehensive Data Analysis: Includes Exploratory Data Analysis (EDA), Correlation Analysis, Volatility Study, and Predictive Modeling for informed investment decisions.

  - Power BI Dashboard: A visually interactive dashboard for non-technical users, displaying key stock market KPIs that enhance decision-making.

  - Machine Learning for Prediction: Built a model to predict stock movements (up/down) using historical trends, economic indicators, and technical factors.

   <h2> Understanding the Data </h2> 
   
This dataset contains a diverse range of financial indicators, stock prices, technical indicators, economic factors, and commodity prices, which influence stock market movements. Understanding these features is crucial for building a strong predictive model.

- Date & Target Variable
  
  Date: Represents the trading day of the stock market. Used for time-series analysis.
  Close: The closing price of a given index or stock on that day. This is often the target variable for stock price prediction.

- Momentum & Rate of Change Indicators
  
  Momentum indicators help determine trend strength and possible reversals:
  mom, mom1, mom2, mom3: Measures the difference in stock price over different periods, showing price acceleration.
  ROC_5, ROC_10, ROC_15, ROC_20: Rate of Change (ROC) calculates the percentage change in price over different time windows.

- Moving Averages (Trend Indicators)
  
   EMA_10, EMA_20, EMA_50, EMA_200: Exponential Moving Averages (EMAs) smooth out price fluctuations to show long-term trends.
   EMA_10, EMA_20: Short-term trend indicators
   EMA_50: Medium-term trend indicator
   EMA_200: Long-term trend indicator

 - Market Indices & Individual Stocks

  This dataset tracks multiple stock indices and individual stocks, helping analyze market-wide trends and sector performance:
  Major Indices: S&P, NASDAQ, DJI, NYSE, RUSSELL-F, GDAXI, FCHI, FTSE, HSI, IXIC, SSEC
  Blue-Chip Stocks: AAPL, AMZN, GE, JNJ, JPM, MSFT, WFC, XOM

- Interest Rates & Bond Yields (Macroeconomic Factors)

  DTB4WK, DTB3, DTB6, DGS5, DGS10, DAAA, DBAA: These are U.S. Treasury yields and corporate bond rates.
  CTB3M, CTB6M, CTB1Y: Short-term central bank treasury bills.

 - Commodities & Forex (Global Economic Indicators)

  Commodities: Oil, Brent, WIT-oil, Gold, silver-F, copper-F, GAS-F, wheat-F
  Foreign Exchange (FX) Rates: GBP, JPY, CAD, CNY, EUR, AUD, CHF, Dollar index, Dollar index-F
 
 - Futures & Derivatives Market Data

  S&P-F, NASDAQ-F, DJI-F, FTSE-F, gold-F, Nikkei-F, KOSPI-F, RUSSELL-F, Dollar index-F

- Technical Indicators (TE & DE Features)
TE1, TE2, TE3, TE5, TE6, DE1, DE2, DE4, DE5, DE6





 
