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
- Notebook: `Cryptos_Clustering_Visualization.ipynb` in this repo, or click <a href="https://nbviewer.jupyter.org/github/trang-h-vo/Time-Series-Cryptocurrencies-Clustering-and-Predictive-Analysis/blob/main/Cryptos_Clustering_Visualization.ipynb"> here </a> for a quick browser view.

## Predicting Bitcoin prices
- This section tests Neural Networks to predict Bitcoin daily average prices, using windowed dataset of 10 lags.
- Models used: `Multilayer Perceptron`, `Recurrent Neural Networks` with simple Recurrent cells, `Long Short-Term Memory` cells and `Gated Recurrent Unit` cells. Ensemble method is used for final predictions.
- Notebook: `Predicting_Bitcoin_Prices_with_NNs.ipynb` in this repo, or click <a href="https://nbviewer.jupyter.org/github/trang-h-vo/Time-Series-Cryptocurrencies-Clustering-and-Predictive-Analysis/blob/main/Predicting_Bitcoin_Prices_with_NNs.ipynb"> here </a> for a quick browser view.
- Future improvements: Experiement with different number of lags; Add features such as day-of-week to capture weekly seasonality (if any), lagged daily trading volume and/or spread; Hyperparameter tuning with Keras Tuners; Train models multiple times using different random seeds to inspect the performance stability.

## Data source
The raw data is retrieved from the <a href="https://www.kaggle.com/jessevent/all-crypto-currencies"> Every Cryptocurrency Daily Market Price </a> dataset on Kaggle. 

