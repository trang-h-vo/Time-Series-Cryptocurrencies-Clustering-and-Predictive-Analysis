# Time-Series-Cryptocurrencies-Clustering-and-Predictive-Analysis
This repository looks at the daily price of some top cryptocurrencies, uses clustering method to characterize their monthly volatilities and test Recurrent Neural Networks to predict Bitcoin average daily prices.

## Data description
- The dataset contains more than `942,000 records` of `2,071 cryptocurrencies`. 
- The tokens’ features include: `name`, `symbol`, `ranking`, `market capitalization`, `daily trading volume`, daily market prices (`open` & `close`, `high` & `low`) & `daily spread`.
- The time frame of the dataset is from `28/04/2013` to `30/11/2018`.

## Clustering
- This section focuses on 30 coins ranked in the top 100 and have available data for the period from 2017 to 2018.
- The clustering analysis is based on the selected cryptos’ `monthly price volatilities`. An asset’s price volatility is defined by the standard deviation of the asset’ returns within a chosen time frequency, in which the returns are calculated using continuous compounding.
- Methods: K-Means and Agglomerative Clustering algorithms, combined with Dynamic Time Warping method.

## Predicting Bitcoin prices
- Dataset: `2,042 records of Bitcoin daily average prices`, calculated by averaging daily open, close, high and low prices.
- Window size: `10` lags.
- Models: `Multilayer Perceptron`, `Recurrent Neural Networks` with simple Recurrent cells, `Long Short-Term Memory` cells and `Gated Recurrent Unit` cells. Ensemble method is used for final predictions.
- Scaling: Both the inputs and outputs of train, validation and test sets are standardized, by removing the mean value of train inputs then divided by the train inputs standard deviation. This is to ensure the inputs and outputs of each dataset are on the same scale, helping the models to converge faster. In the inference step, the model predictions will be inversely transformed to the real scale.

## Data source
The raw data is retrieved from the <a href="https://www.kaggle.com/jessevent/all-crypto-currencies"> Every Cryptocurrency Daily Market Price </a> dataset on Kaggle. 

