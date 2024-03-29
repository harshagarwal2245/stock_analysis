**About** 

This project explores predictability in the market and then designs a decision support framework that can be used by traders 
to provide suggested indications of future stock price direction along with an associated probability of making that move.
Markets do not remain stable and approaches that are highly predictive at one moment may cease to be so as more traders 
spot the patterns and adjust their trading techniques. Ideally, if these “concept drifts” could be anticipated, then the trader
could store models to use with each specific market condition (or concept) and later apply those models to incoming data. 
The assumption however is that the future is uncertain, therefore future concepts are still undecided.
Maintaining a model with only the most up-to-date price data is not necessarily the most ideal choice since the market may stabilize and old knowledge may become useful again. Additionally, decreasing training times to enable modified classifiers to work with streaming high-frequency stock data may result in decreases in performance (e.g. accuracy or AUC) due to insufficient learning times. 
My project takes a different approach to learning with drifting concepts, which is to assume that concept drift occurs and builds this into the model. The project adapts to these market changes by building thousands of traditional base classifiers (SVMs, Decision Trees, and  Random Forest), using random subsets of past data, and covering similar (sector) stocks and heuristically combining the best of these base classifiers.This “ensemble”, or pool of multiple models selected to achieve better predictive performace is then used to predict future market direction. As the market moves, the base classifiers in the ensemble adapt to stay relevant and keep a high level of model
performance. Our approach outperforms existing published algorithms.
The project also discusses specifically class imbalance, attribute creation (e.g. technical and sentiment analysis),
dimensionality reduction, and model performance due to release of news and time of day. Popular methods for dealing with each are discussed

**Working Process in short**

This project has been divided into 6 parts and divided into modules each module has its own result which is being used 
for further development. In first two parts are based on Eda first part is for calculating various indicators like Vwap, trends and second part is
used for Visualizing data using time series along with bollinger bands and other technical indicators like moving average. Next two part is of 
modeling in first part we predict close price by using linear regression and some other variables are considered it also uses CPAT theory which takes
beta values and in second part we created model that will classify trade calls i.e. to hold to buy or to sort calls main indicator used for these is bollinger bands and moving average after training on machine learning model it had given 79% accuracy and other stocks of 50+ accurate which is very good. In next two parts we used other indicators like sharpe ratio to select which stock should be included in your portfiolo or not and recommend the best and similar stocks with help of volatility and standard deviation i.e. doing diverfication analysis. Hence completing modern portfolio stratergy

**Achivement**
1. Investors who had basic idea can use this to get technical indicators and identify trends
2. Who are new to stock market analysis can use this to make trade calls
3. Investors can predict close price of stock and hence decide which stock to sell
4. Investors can used this project to decide weather to include stock in portfolio or not
5. To get recommendation of best stocks from market in 5 seconds
