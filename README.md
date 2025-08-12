# S-P-500-Weekly-Model

S&P 500 Weekly Movements Final Report

https://github.com/jlatouche7/S-P-500-Weekly-Model
Question: How can small companies leverage and effectively invest their extra resources so they can become a more profitable company or scale up in size?

Problem: The S&P 500 is often used to gauge general market trends, and many people consider it to be a gauge of the overall economic health of the United States. Many companies, especially smaller companies, lack the resources and tools to invest their extra funds properly. My goal is to give these companies a tool that can give them a general idea of the S&P 500’s upcoming movements. A model that can predict the S&P 500’s long-term movements and week-to-week returns could be very useful to the company in determining entry and exit points for the investment decisions. If this question remains unanswered, it could lead to them making poor investment decisions that could potentially hurt the company’s financial standing. Most importantly, I hope my analysis will provide the companies with conviction in their investment decisions. While many of us have sentiments based on news and other information we gather daily, it is hard to have conviction in your investment decisions if that is all you are basing it off. I hope to provide security and conviction to the company by using historical data to inform what is likely to come on a short and long-term basis, based on decades of history.

Data Acquisition:  I used a combination of financial data, mostly coming from FRED, a database that includes a plethora of historical time series data. I compiled a dataset including market data, macroeconomic data and sentiment analysis data as well.

Methodology: When it comes to financial modeling, capturing the sequential aspect of the data is essential to building a useful model. Financial markets can move very quickly, especially when fear enters the market, like during COVID and the 2008 financial crisis. I wanted to show how important this aspect is when modeling financial data, so I built a standard linear regression model and multiple AutoRegressive Integrated Moving Average models. 
My linear regression model was built simply to see how a model that did not capture time series data would perform. Next, I built a baseline model called Random Walk. This model assumes that the best prediction for the next week is the result of last week. This is what I used to base the success of my other models on. Finally I built two different ARIMA models, one that used only the final close price of the S&P500 and the date, and then another that factored in a plethora of other features as well.

Results:
Firstly, my initial thoughts were confirmed with a standard linear regression. It was unable to capture the sequential aspect to the data and was essentially useless in predicting anything.  
With my ARIMA models, I found that a standard ARMA was the best at predicting the last 6 years of S&P500 data. I chose this period to see how a model could handle the adjustment to and from COVID. My SARIMAX model that includes lots of financial features, struggled to compute this. Overall, I was able to build a model that is successfully able to predict from week to week, in normal market environments and was also able to adapt to rapidly changing market conditions. 

