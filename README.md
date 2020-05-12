# Machine-Learning
Machine Learning to forecast time-series model and comparing days/week plots

This purpose of this project is to use ARIMA ('Auto Regressive Integrated Moving Average) for timeseries forecasting sales and the data for this project was taken from kaggle.
I am the sole contributor for this project and here goes my approach to this problem:

1)Data Cleaning, Preprocessing
The table contains individual drugs sold per day. For this project I use total sales and the dataset I will be deadline with will be dates and total sales of all drugs on that particular day. Outliers are removed using Interquartile range and the data is smoothened using moving average.

2)Analyse Data
The data is decomposed to study trend, noise and seasonality. This is important to understand what ARIMA model we use
The data is tested for staionarity (constant mean and standard deviation) to decide the parameters for ARIMA.

3)Deciding parameters
Autocorrelation plot shows a positive lag at 1 which makes q=0. We see two positive lags in acf plot which makes p=2
From stationarity and from null hypothesis testing we see that data is almost stationary (p value = 0.057) but needs some refinement. The first differenced value plot shows that mean and sd are constant that makes d=1.

The predicted model has a mean squared error of 88 and the plot shows that prediction looks quite similar to original.

4) Comparison
The smoothing method can average for month or a week. The plots show a better fir (smaller MSE) for week mainly due to larger number of data points.


