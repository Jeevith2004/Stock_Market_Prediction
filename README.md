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

 <h2> Dashboard Walkthrough </h2>

 __Executive Summary__`:

 ![Screenshot 2025-04-02 180121](https://github.com/user-attachments/assets/c292741c-9c41-47f5-996c-8ead1ef4330b)
 

1. KPI Metrics:
   
- Market Sentiment (70.56) – Positive Market Outlook
  Market sentiment represents the overall mood of investors, and a value of 70.56 suggests a highly optimistic market environment. A sentiment score above 50 typically indicates positive investor confidence, 
  which often leads to increased stock buying activity.

- Volatility Percentage (23.87) – Moderate Market Fluctuations
  Volatility measures the extent to which stock prices fluctuate over time, and a value of 23.87% indicates moderate price swings. While high volatility (above 30%) suggests increased uncertainty and potential 
  risk, moderate volatility (20-30%) can indicate a healthy market with active trading. A volatility level in this range suggests that while the market is experiencing price movements, it is not in a highly 
  unstable phase.

- Maximum Drawdown (-61.21) – Significant Market Crash
  Maximum drawdown measures the largest peak-to-trough decline in stock prices over a period. A drawdown of -61.21% suggests that at some point, the market lost more than 60% of its value before recovering. This 
  indicates that there has been a period of extreme market distress.A high drawdown suggests that the market has faced severe turbulence, and long-term investors must consider such risks when making investment 
  decisions.

- Volume Spike (High Activity) – Increased Trading Volume
  The label "High Activity" suggests that the market is experiencing a significant increase in trading volume. Increased trading volume usually indicates strong investor participation, which can be triggered by 
  events such as earnings reports, major policy changes, or economic data releases.

  __Line Chart: Stock Market Trends vs. Interest Rates__
      This chart shows how different financial indicators, such as stock market performance, interest rates, and commodity prices, interact over time.

- Blue Line (S&P and Market Sentiment):The trend shows that stock prices and market sentiment generally follow each other.When sentiment is high, stock prices rise; when sentiment declines, stock prices fall.
- Orange Line (DGS10 - 10-Year Treasury Yield):Interest rates seem to have an inverse relationship with stock market sentiment.As Treasury yields increase, the stock market tends to struggle, indicating that 
  higher interest rates reduce market liquidity and borrowing.
- Purple Line (Oil Prices):Oil prices show a rising trend from 2014 to 2017, which could signal economic growth or inflation concerns.
- Other Factors (Gold, DTB3 - 3-Month Treasury Bill):Gold is typically considered a safe-haven asset.If gold prices rise while the stock market declines, it suggests investors are seeking safety.

  
2.__Stock Performance and Sector Insights__:
![Screenshot 2025-04-02 180130](https://github.com/user-attachments/assets/c656cd71-fc2f-451a-9d87-3ba7cd09c239)

__Trading Volume vs. Price Movements__

-> Insights:

- Trading volume and price movement do not always correlate directly. In 2011, __the highest volume did not result in the highest closing prices, indicating speculative trading__.__Periods of declining volume 
  (2012- 2014) often indicate reduced market activity__, possibly due to investors waiting for clearer signals.Spikes in trading volume (2011, 2015) are likely associated with key economic events, earnings 
   reports, or major market movements.2016-2017 shows a __declining trading volume (2.6)__, indicating possible investor caution or reduced speculative activity, despite stable closing prices.

__Stock Price Trend with EMA Indicators__

-> Insights:

The __EMA crossover confirms bullish momentum__, meaning short-term moving averages are above long-term ones.Steady price increase after 2012 suggests consistent market confidence and reduced volatility.__EMA indicators help traders identify entry and exit points__. A bullish EMA crossover (shorter EMA crossing above longer EMA) signals a good entry point for buying.No visible EMA 200 crossovers suggest that __no major bearish reversal has occurred yet__.

3. __Stockmarket Trend and microeconomics influences__
   ![Screenshot 2025-04-02 180139](https://github.com/user-attachments/assets/fe3b1bed-d368-45ae-a0ad-5803efe9737f)

 __Momentum vs. Rate of Change (ROC)__

 ->Insights:
  
  Stock price momentum fluctuates within a narrow range most of the time, suggesting that the market does not experience extreme momentum shifts frequently.Outliers indicate sudden price spikes or crashes, which 
  may be due to market news, economic events, or investor reactions.A balanced distribution suggests that the market does not favor either bullish or bearish momentum significantly, meaning trading strategies 
  relying on ROC should consider external macroeconomic factors.Traders can use this information to identify potential breakouts or trend reversals by focusing on extreme values that indicate unusual market 
  behavior.

  __Stock Market Growth Trend Over Time__

  ->  Insights:
    
    The sharp rise in stock prices post-2009 suggests a strong economic recovery phase, possibly due to stimulus measures or improved corporate earnings.Steady growth from 2011 to 2015 reflects market stability 
    and investor confidence, indicating a bullish sentiment during this period.The slight slowdown around 2015 could be linked to external factors like economic policies, interest rate changes, or global market 
    uncertainty.Overall, the stock market has followed a long-term growth trend, making it an attractive investment avenue for long-term investors.

   __Stock Market vs. Bond Yields Over Time__

   -> Insights:

   Stock markets tend to be more volatile than bond yields, as seen from the fluctuations in stock indices.The peak in stock indices around 2010-2011 suggests a strong market rebound, potentially after a 
   financial crisis or recession.The decline in 2015 could be due to economic factors like interest rate hikes, inflation concerns, or policy changes.Bond yields showed relatively lower fluctuations, indicating 
   their role as stable investment options during stock market volatility.A negative correlation is visible at times—when stock markets decline (2012, 2015), bond yields remain steady or slightly rise, 
   suggesting that investors shift to bonds during stock market downturns.

  4. __Interest rate,Oil,Gold and Impact on stocks__
     ![Screenshot 2025-04-02 180154](https://github.com/user-attachments/assets/da212e5c-a645-44be-81e1-a7e3372910d7)

   **Interest Rates vs. Stock Market Performance**

    -> Insights
    
 Stock market performance is more volatile than interest rates, as seen from the fluctuations in S&P 500 and NYSE.Stock markets peaked in __2010-2011 and 2013, indicating economic expansion__, 
 while the  __decline in 2015 suggests a temporary economic slowdown__.Despite stock market fluctuations, interest rates remained relatively stable, indicating that rate hikes or cuts may not have been the 
 primary drivers of market movements.__Long-term interest rates (DGS10) showed mild fluctuations__, suggesting a gradual adjustment in economic policies rather than sudden changes affecting the stock market.A 
 strong stock market recovery in 2016 suggests renewed investor confidence, possibly due to economic stimulus or corporate earnings improvements.

   __Impact of Oil Prices on S&P 500__

   -> Insights

     There is a clear positive correlation between oil prices and stock market performance, __meaning higher oil prices are generally associated with rising S&P 500 levels__.This correlation suggests that oil n 
    price increases may reflect strong economic demand, leading to higher stock prices.__Outliers indicate that in some cases, extreme oil price fluctuations caused market instability__.Investors should monitor 
    oil price trends as they can serve as an early indicator of stock market movements.Periods of __falling oil prices may signal economic weakness__, which could impact stock markets negatively.

   __Stock Market and Commodity Trends Over Time__

   -> Insights:
   Stock market trends closely follow oil prices, meaning both assets tend to perform well in strong economic conditions.Gold acts as a safe-haven asset, moving inversely to stocks and oil, suggesting investors 
   shift to gold during economic uncertainty.The 2015 decline in both stocks and oil suggests a broad market downturn, possibly due to global economic slowdowns or supply-demand imbalances in oil.The recovery in 
   2016 across stocks and oil suggests improved economic conditions, possibly due to fiscal policies or rising demand.Commodities (oil & gold) provide diversification benefits—gold offers protection during 
   downturns, while oil moves in line with economic growth.




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





 
