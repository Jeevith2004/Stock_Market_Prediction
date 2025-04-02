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

 <h2> Data Preprocessing </h2>

During the Data Preprocessing phase, a significant number of missing values were identified across multiple features. To ensure data integrity  consistency, mean imputation was applied to fill in the missing values. This approach helped preserve the overall distribution of the data while minimizing potential biases. After imputation, the dataset was re-evaluated to confirm that the adjustments did not distort key statistical properties, ensuring a reliable foundation for further analysis.



   <h2> Exploratory Data Analysis </h2> 

-  **Python & Pandas** were used for cleaning and analyzing stock trends.
-  **Matplotlib & Seaborn** were used for visualizing stock movements.
-  **Power BI Dashboard**  provides an intuitive and interactive way to explore key stock market insights.  
-  The full EDA code is available here

__Stock Market Trends & Insights__: A Data-Driven Analysis

   This section presents key insights derived from stock market data through exploratory data analysis (EDA). By leveraging various visualizations, we uncover patterns in market sentiment, stock price movements, 
   correlations, and performance across different market conditions.

1️ Market Sentiment & Stock Indices Performance (Smoothed)

![Screenshot 2025-04-02 154252](https://github.com/user-attachments/assets/3070f909-a91f-4cab-8d47-5d39172f3656)


 What This Chart Shows:

- This graph visualizes the smoothed performance of key stock indices (DJI, NASDAQ-F, S&P) alongside commodities (Gold, Oil) and the Dollar Index.

- The smoothing effect removes noise, making it easier to identify long-term trends and periods of high or low volatility.

- A significant drop between 2011 and 2012 suggests a market correction, likely due to global economic factors such as the European debt crisis or U.S. fiscal concerns.

->  Insights:

- Volatility spikes __indicate periods of uncertainty__ these are typically caused by economic policy changes, earnings reports, or geopolitical events.The correlation between commodities and stock indices can 
  reveal __market sentiment shifts__ (e.g., when stocks fall, gold often rises as investors seek safe-haven assets).The Dollar Index’s role: A strengthening dollar often __impacts multinational corporations__, 
  as a stronger USD makes U.S. exports more expensive.

  2️ Stock Price Movement Over Time
  ![Screenshot 2025-04-02 154358](https://github.com/user-attachments/assets/9e0ad71c-976b-413e-b066-25fd397e2a22)

   What This Chart Shows:

- The stock price movements of major companies (AAPL, AMZN, JPM, XOM, MSFT) over time.

- Sharp peaks and drops indicate periods of high volatility, potentially driven by earnings reports, regulatory changes, or macroeconomic shifts.

- A major dip around early 2013 could be linked to external factors such as Federal Reserve interest rate changes or company-specific earnings downturns.

 -> Insights:

 - Growth stocks vs. defensive stocks: Tech companies (AAPL, AMZN) often __show higher volatility__ compared to financial (JPM) or energy (XOM) stocks, which are more stable.Earnings cycles and trends: Some 
   stocks exhibit periodic patterns, suggesting a strong link to quarterly earnings reports and investor expectations.Liquidity and investor behavior: High spikes in volatility may indicate increased trading 
   volume, suggesting that certain price points act as resistance/support levels.

3️ Stock Correlation Matrix 
![Screenshot 2025-04-02 154418](https://github.com/user-attachments/assets/97ac2279-226a-46d1-93f5-1c98272d41e2)

 What This Chart Shows:

- A correlation matrix displaying the relationships between different stocks.

- A value close to 1 means the stocks move in sync, while values closer to 0 or negative indicate little to no correlation.

- Tech stocks (AAPL, AMZN) show a high correlation, indicating that they often move together based on broader technology sector trends.

 -> Insights:

- Diversification strategy: Investors should __avoid holding highly correlated stocks in the same portfolio__, as market movements would affect them similarly.Sectoral trends: __Financial stocks (JPM) and energy 
  stocks (XOM) show lower correlations__ with tech stocks, making them good candidates for portfolio diversification.Market sentiment impact: If correlations between all stocks increase (i.e., during a market 
  crash), diversification benefits decrease as all assets start moving in the same direction.

  4️ Stock Performance in Bull vs. Bear Markets
  ![Screenshot 2025-04-02 154457](https://github.com/user-attachments/assets/9f3fef09-cfb3-4296-8e7e-d44c598c2eaf)

 What This Chart Shows:

 - A comparison of stock performance in bull (growth) vs. bear (declining) markets.

- Stocks like AMZN and AAPL perform exceptionally well in bull markets, while others like XOM and JPM show stability across both market conditions.

 -> Insights:

- Growth vs. value investing:Growth stocks (AMZN, AAPL) outperform in bull markets due to increased investor optimism.
  Value stocks (XOM, JPM) tend to be stable, making them safer in downturns.Sector resilience:Tech and consumer stocks thrive in bull markets but are riskier in bear markets.Financial and energy stocks offer 
  stability due to strong underlying assets or dividend yields.Risk management strategies:Investors may rotate their holdings between growth and defensive stocks based on the economic cycle.

<h2> Modeling & Prediction </h2>
1️ Model Selection & Justification

- The chosen model is Logistic Regression, a widely used classification algorithm for binary outcomes.

- It was selected for its interpretability and ability to provide probabilistic outputs, which are useful for stock movement prediction (Up/Down).

2️ Feature Engineering & Selection

- Initially, the model achieved an accuracy of 99%, which indicated potential bias or overfitting.

- To mitigate this, highly correlated features (correlation > 0.95) were removed to reduce redundancy and multicollinearity.

- The following features were dropped:
['EMA_10', 'EMA_20', 'EMA_50', 'EMA_200', 'DTB3', 'DTB6', 'S&P', 'NYSE', 'TE2', 'TE3', 'DES', 'DE6', 'CAC-F', 'DAX-F', 'DJI-F', 'NASDAQ-F', 'RUSSELL-F', 'S&P-F', 'SMA_10', 'SMA_50', 'HOM', 'SOM', 'MOM_10', 'SP_vs_NASDAQ', 'Close_Lag_1', 'Close_Lag_5', 'SMA_10_Lag_1', 'Date_numeric', 'Year']

- This step helped improve model generalization and reduced overfitting risks.

3 L1 Regularization for Feature Selection

- L1 regularization (Lasso) was applied using Logistic Regression with an L1 penalty.

- Regularization strength was controlled using C=0.1, preventing overfitting by reducing the impact of less relevant features.

- The accuracy dropped slightly to 0.9697, indicating that regularization led to a simpler model with fewer active features.

4 Principal Component Analysis (PCA) for Dimensionality Reduction

- PCA was applied to reduce features to 10 principal components, preserving the most critical information while removing noise.

- After dimensionality reduction, the model was retrained and achieved an accuracy of 0.9370.





 
