
# Cryptocurrency Clusters

## Background

In this exercise a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. They’ve asked for a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment.

For this we will use unsupervised machine learning as there are no preset labels.

Data Preparation is the first step and this is the outline of what was done prior to building models


* All cryptocurrencies that are not being traded were discarded. Then, the `IsTrading` column was dropped from the dataframe.

* All rows that have at least one null value were removed

* Cryptocurrencies that have been mined were kept.

* Since the coin names do not contribute to the analysis of the data, the column`CoinName` was dropped from the original dataframe.

* The features `Algorithm` and `ProofType` were converted to numerical data using Pandas and create dummies function To accomplish this task.

*  The columns are standarized so that contain larger values do not unduly influence the outcome.

### Dimensionality Reduction

* Creating dummy variables above dramatically increased the number of features in the dataset. Therefore, dimensionality reduction with PCA was performed using the 'explained variance'. For this project, I preserved 90% of the explained variance in dimensionality reduction. 

* Next, I further reduced the dataset dimensions with t-SNE and visually inspected the results using a scatter plot

### Cluster Analysis with k-Means

* I created an elbow plot to identify the best number of clusters using a for-loop to determine the inertia for each `k` between 1 through 10. .

### Recommendation

* Based on running an analysis with k-Means and t-SNE, even with scaling, there really doesn't seem to be any good way to cluster the crypto currencies.
