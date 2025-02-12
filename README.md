# Cryptocurrency Market Data Clustering Repository

Welcome to this repository focused on exploring patterns in cryptocurrency market data using unsupervised learning
techniques. This project leverages K-means clustering to group cryptocurrencies based on their market
characteristics, both with and without dimensionality reduction through Principal Component Analysis (PCA).

## Overview

The primary goal of this project is to identify clusters of cryptocurrencies that exhibit similar behaviors in the
market. By analyzing features such as trading volume, returns, and other metrics, the goal is to uncover insights into
how different cryptocurrencies interact within the broader market landscape.

## Usage

### Data Exploration and Preprocessing

Begin with the Jupyter notebook (`Crypto_Clustering.ipynb`) for interactive data exploration:

1. **Data Loading**: Load cryptocurrency market data from a CSV file.
2. **Initial Checks**: Conduct exploratory data analysis to understand feature distributions, such as trading
volumes and returns.

### Feature Scaling

K-means clustering is sensitive to feature scales, so we normalize the data:
```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
scaled_features = scaler.fit_transform(features)
```
*Important to do so, as using the raw data in the form of a dataframe will yield the wrong results*

### Clustering With K-Means

- **Elbow Method**: Determine the optimal number of clusters using the elbow method on scaled features.
- **Elbow Curve**: [Visualization Here](https://mctrashmoney.github.io/CryptoClustering/CryptoClusteringSD/Output_Visualizations/original_elbow_curve.html)
- **K-means Clustering**: Apply K-means to form clusters and analyze their characteristics.
- **Clusters (K-Means)**: [Visualization Here](https://mctrashmoney.github.io/CryptoClustering/CryptoClusteringSD/Output_Visualizations/original_clusters.html)

### Clustering With PCA

- **Dimensionality Reduction**: Use PCA to reduce feature dimensions while retaining significant variance.
- **PCA Elbow Curve**: [Visualization Here](https://mctrashmoney.github.io/CryptoClustering/CryptoClusteringSD/Output_Visualizations/pca_elbow_curve.html)
- **Enhanced Clustering**: Apply K-means on PCA-reduced data to explore more generalized patterns in the market.
- **Clusters With PCA**: [Visualization Here](https://mctrashmoney.github.io/CryptoClustering/CryptoClusteringSD/Output_Visualizations/pca_clusters.html)

### Compared Results
- **Contrasted Elbow Curves**: [Visualization Here](https://mctrashmoney.github.io/CryptoClustering/CryptoClusteringSD/Output_Visualizations/composite_elbow_curve.html)
- **Contrasted Scatter Clusters**: [Visualization Here](https://mctrashmoney.github.io/CryptoClustering/CryptoClusteringSD/Output_Visualizations/composite_clusters.html)

## Files Included

1. **Crypto_Clustering.ipynb**: Interactive notebook for data exploration and analysis.
2. **Output_Visualizations/**: Directory containing generated visual outputs as HTML files.
3. **Resources/**: Directory containing raw data.

## Conclusion

This repository offers a robust framework for clustering cryptocurrencies using both standard K-means and
PCA-enhanced approaches. It serves as a valuable tool for developers and data analysts seeking to understand
market dynamics through data-driven insights.

Original Dataset Visualized 👉🏻 [here](https://mctrashmoney.github.io/CryptoClustering/CryptoClusteringSD/Output_Visualizations/crypto_market_data.html)