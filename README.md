# Cryptocurency Price Prediction

In this project, the price of a cryptocurrency is estimated using two artificial intelligence methods:
- Gradient Boosting Enssemble as the machine learnign technique.
- Recurrent Neural Networks as the deep learning technique

The data is taken form different sources:
- CoinAPI to get the OHLCV indicators (open High Low Close Volume)
- Augemnto API to get sentiment indicators about the cryptocurrenices
- Technical indicators are calculated using the python ta lybrary

The strucutre of the porject is as follows:
- File GetInformation: This is where data is being extracted form the APIs and the final dfData.csv dataset is generated. Since I am using the free connections, I export several files such as "symbols.json" (which contains all the coints that CoinAPI offers) so I do not have to consume free credit making more calls to the API to get the available cryptocurrencies. The final dataset "dfData.csv" contains all the needed information for the next two files to operate

At predicting the price of the crypto, the last 4 weeks of the data is keeped for testing purposes meanwhile the rest of the data is used for training the model. The OHLCV prices are on a daily interval, same as the interval for the published sentiment articles. Since this is a comparison, for both techniques the same time intervals have been used. 

- File GradientBoosting: This is the algorithm where the Gradient Boosting technique to predict the price of the crypto.

- File LTSM Model: This is the Long Short Term Memory algorithm to predict the price of the crypto. 

I am curently creating a file which includes an investing strategy algorithm. Still in progress. (Estimated for June)
None of the investing will be done in real time, instead, i allways use the dfData.csv which has the past history of the cryptocurrency and I keep a timeline form that information for testing purposes and the rest for training. 
