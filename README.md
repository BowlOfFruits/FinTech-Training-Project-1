An important aspect of time series analysis is making sure you do not shuffle the data when splitting it into training, testing and validation set. Doing so can cause the model to be trained on future data in the training set. Initially loss will be extremely low, but when used in the wild, reliability is extremely low.

The main challenge with time series forecasting is the lack of economic data associated with the prices. Furthermore, stock prices are chaotic and is extremely hard to predict with good accuracy.

# Implementation 1 - LSTM
LSTM involves memory storage. This is particularly useful when there is time involved, a trend. We are able to use previous points to make a decision for the future. 

Compared to other models such as tree-based models, LSTM does not require you to provide the context for the model, as it is able to learn by itself. Furthermore, tree-based models are poor at extrapolating on higher or lower values than those seen in training data, so it is almost impossible for them to predict time series, where future values can lie outside of the range seen in training dataset.

# Implementation 2 - ARIMA
In the implemented ARIMA model, no periodical pattern was seen after 1st order differencing. ACF and PACF was extremely low, and thus arima(1,1,1) is a good model to be used.
