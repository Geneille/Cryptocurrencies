# Cryptocurrencies

## Overview and Objectives

Investment in cryptocurrency has increased over the last decade. But with many crypotcurreny on the market, selection and investment in the cryptocurreny universe has become challenge for investors, more so new investors trying to cashin. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. 

The aim of this project was to create a report that documents the various cryptocurrencies on the trading market and how they could be grouped to create a classification system for this new investment. Unsupervised machine learning was the method used since the specific output was not known. The cryptocurrencies was grouped using a clustering algorithm.

## Analysis

The Analysis consist of four main parts. Each part with the subsequent steps is summarized below.


### Section 1 - Preprocessing the Data

1. A DataFrame was created with the data provided
2. The DataFrame was filtered so that it only conatins rows where coins are being mined.
3. Unnecessary columns and rows that had atleast one null value was removed.
4. The get_dummies() method was used to create variables for the two text features, and the resulting data was stored data in a new DataFrame.
5. The StandardScaler fit_transform() function was finally used to standardize the features from the new DataFrame.

### Section 2 - Reducing Data Dimensions Using PCA

1. PCA was applied to The DataFrame with the standardize data to reduce the dimensions to three principal components.
2. A new DataFrame  was then created that includes the three principal components.
3. The same index of the original DataFrame was then applied to this new DataFrame.

### Section 3 - Clustering Cryptocurrencies Using K-means

1. The dataset in the DataFrame created in the previous section was reduced to three dimensions.
2. An elbow curve was created using hvPlot to find the best value for K for the DataFrame created in the previous section.
4. The K-means algorithm was then used on the above-mentioned DataFrame to make predictions of the K clusters for the cryptocurrencies’ data.
5. A new DataFrame was then created by concatenating the two above mentioned  DataFrames on the same columns.
6. In this new DataFrame the CoinName column that holds the names of the cryptocurrencies was merged
7. Finally, a new column named Class that holds the predictions, i.e., model.labels_, was included in the DataFrame.

### Section 4 - Clustering Cryptocurrencies Using K-means

1. A 3D scatter plot using the Plotly Express scatter_3d() function was used to plot the three clusters.
2. The CoinName and Algorithm columns was added to the hover_name and hover_data parameters, respectively, so each data point shows the CoinName and Algorithm on hover.
3. A table with tradable cryptocurrencies was then created using the hvplot.table() function.
4. The MinMaxScaler().fit_transform method was utilized to scale the TotalCoinSupply and TotalCoinsMined columns between the given range of zero and one.
5. A new DataFrame using the scaled data was then created, and the same index as the original DataFrame was assigned.
6. Two columns, CoinName and Class from the previously created was then added. DataFrame to the new DataFrame.
7. A hvplot scatter plot was then created.


## Results

Figure 1 below displays the orginal Dataframe


Figure 2 below provides a preview of the DataFrame after preprocessing