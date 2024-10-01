# CryptoClustering

This module assignment uses K-means clustering and Principal Component Analysis (PCA) to analyze cryptocurrency market data and group similar cryptocurrencies based on their price change percentages over different time frames.

### Dependencies:
- `pandas`
- `scikit-learn`
- `matplotlib`

### Steps:

1. **Data Loading:**
   - The data is loaded from a CSV file (`crypto_market_data.csv`) and includes columns such as `price_change_percentage_24h`, `price_change_percentage_7d`, and so on.
   
2. **Data Preparation:**
   - The data is normalized using `StandardScaler()` for better performance in clustering algorithms.

3. **Finding Optimal K (Elbow Method):**
   - K-means clustering is performed with various values of `k` (number of clusters). The "Elbow Curve" helps visually determine the optimal number of clusters, which in this case is `4`.

4. **Clustering with K-means:**
   - Using the best value of `k`, the K-means algorithm is applied to cluster the cryptocurrencies. The results are stored in a DataFrame, with a new column indicating the predicted clusters for each cryptocurrency.

5. **Visualization:**
   - A scatter plot is generated to visualize the clusters based on two price change percentages (`24h` and `7d`), color-coded by cluster.

6. **PCA for Dimensionality Reduction:**
   - PCA is used to reduce the data to three principal components while retaining 89.5% of the variance. This helps optimize the clustering process by using the reduced dataset.

7. **Optimal K after PCA:**
   - The Elbow Curve is recalculated using the PCA-reduced data, showing the optimal value of `k`.

### Results:
- The optimal number of clusters is `4`, and PCA explains 89.5% of the variance with 3 principal components.

