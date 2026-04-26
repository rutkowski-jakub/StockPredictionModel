# StockPredictionModel

The following code takes stock market data from a given stock in this case Microsoft from 01/01/1990 - 31/12/2025, training the model to predict if the stock price will increase in 90 days time, the algorithm used for this was Random Forests. The model uses a backtest function that takes 2500 trading days as training, then tries predicitng whether the price will increase in 90 days time for every day in a 180 day range, then it will train the data again on the 2500 + 180 days and do this until the end of the time range.

The features used for the predicition were a mix of exponentially smoothed OHLC data and techinical indicators, following work from (Khaidem et al., 2016).

The code being run in its entirety will select the data, make features using functions, apply the features to the data and use the RF to predict the pricing trends for 90 days cycles. It will produce a feature importance graph, OOB score, AUC curve and an implementation in trading with comparison to the S&P 500 and a baseline test. 
