### Cryptocurrency Clustering

This repository contains code and instructions for clustering cryptocurrencies using K-means algorithm. The clustering is performed on both the original scaled data and the Principal Component Analysis (PCA) data to compare the results.

### Prepare the Data:

Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

### Find the Best Value for k Using the Original Scaled DataFrame:

Use the elbow method to find the best value for k.

Create a line chart with the inertia values computed with different values of k to visually identify the optimal value for k.

![bokeh_plot (4)](https://github.com/ehsanshahrabi/CryptoClustering/assets/124327258/9a9d4adc-6ec1-4c42-8e33-bd9af1f3e741)


### Cluster Cryptocurrencies with K-means Using the Original Scaled Data:

Initialize the K-means model with the best value for k.

Fit the K-means model using the original scaled DataFrame.

Predict the clusters to group the cryptocurrencies.

Create a scatter plot using hvPlot to visualize the clusters.

![bokeh_plot (5)](https://github.com/ehsanshahrabi/CryptoClustering/assets/124327258/3a986cde-a764-490f-82ec-798b67e80ba6)


### Optimize Clusters with Principal Component Analysis:

Perform PCA on the original scaled DataFrame to reduce features to three principal components.

Retrieve the explained variance to determine the information attributed to each principal component.

![Screenshot 2023-06-19 160444](https://github.com/ehsanshahrabi/CryptoClustering/assets/124327258/364dc33c-b15b-4b9a-8e24-f1ef6c905fce)


### Find the Best Value for k Using the PCA Data:

Use the elbow method on the PCA data to find the best value for k.

Create a line chart with the inertia values computed with different values of k to visually identify the optimal value for k.

![bokeh_plot (6)](https://github.com/ehsanshahrabi/CryptoClustering/assets/124327258/d5f12f92-e911-4382-bb4b-07def2ba0819)


### Cluster Cryptocurrencies with K-means Using the PCA Data:

Initialize the K-means model with the best value for k.

Fit the K-means model using the PCA data.

Predict the clusters to group the cryptocurrencies.

Create a scatter plot using hvPlot to visualize the clusters.

![bokeh_plot (7)](https://github.com/ehsanshahrabi/CryptoClustering/assets/124327258/746f767b-cfd7-462c-8996-c5d3db8527f4)


### Visualize and Compare the Results for Elbow curve & Elbow curve PCA:

![bokeh_plot (8)](https://github.com/ehsanshahrabi/CryptoClustering/assets/124327258/9ed03e91-b73f-47ec-ab80-f7e4ccbe6082)


## Visualizing Market Clusters in 3D using Plotly Express

The `scatter_3d` function from Plotly Express is used to create the plot. The `market_pca_data_df_copy` dataframe is used as the data source, with the x, y, and z coordinates specified as the "PC1," "PC2," and "PC3" columns, respectively. The color of the data points is determined by the "MarketCluster" column.

![3d](https://github.com/ehsanshahrabi/CryptoClustering/assets/124327258/0b0580be-76a7-447c-9617-61de2fb3c3bd)


