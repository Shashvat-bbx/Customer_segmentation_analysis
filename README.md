
# Customer Segmentation using Clustering Algorithms

## Overview

This notebook demonstrates customer segmentation using various clustering algorithms such as K-Means, DBSCAN, and Agglomerative Clustering. The segmentation is based on a dataset with various customer features such as balance, purchase frequency, cash advance usage, and credit limit. The goal is to group customers into meaningful clusters that can help in profiling customer behavior and tailoring marketing strategies.

## Dataset

The dataset contains customer financial information, including:

- **BALANCE**: The account balance of the customer.
- **BALANCE_FREQUENCY**: How frequently the balance is updated.
- **PURCHASES**: Total purchases made by the customer.
- **ONEOFF_PURCHASES**: One-time purchases made by the customer.
- **INSTALLMENTS_PURCHASES**: Purchases made in installments.
- **CASH_ADVANCE**: Cash advances taken by the customer.
- **CREDIT_LIMIT**: The credit limit of the customer.
- **PAYMENTS**: Total payments made by the customer.
- **MINIMUM_PAYMENTS**: Minimum payments made by the customer.
- **PRC_FULL_PAYMENT**: Percentage of full payments made by the customer.
- **TENURE**: The duration of the customer's account.

## Preprocessing

1. **Missing Value Imputation**: SimpleImputer is used to fill missing values in the dataset using the mean strategy.
2. **Feature Scaling**: StandardScaler is applied to ensure features are on the same scale, which is crucial for clustering.
3. **Outlier and Distribution Analysis**: Histograms, boxplots, and correlation heatmaps are generated to visualize feature distributions and relationships.

## Clustering Algorithms

1. **K-Means Clustering**:
   - Optimal number of clusters determined using the Elbow method.
   - Silhouette score used to evaluate cluster quality.
   - Customer profiling based on clusters formed by K-Means.

2. **DBSCAN Clustering**:
   - Density-based clustering algorithm.
   - Noise points are identified and excluded from cluster evaluation.
   - Silhouette score calculated (if multiple clusters are formed).

3. **Agglomerative Clustering**:
   - Hierarchical clustering using Euclidean distance and Ward linkage.
   - Silhouette score used to assess cluster separation.

## Dimensionality Reduction

1. **PCA (Principal Component Analysis)**:
   - Data is reduced to 2 dimensions to visualize clusters formed by the algorithms.

2. **t-SNE (t-distributed Stochastic Neighbor Embedding)**:
   - Non-linear dimensionality reduction technique used for visualizing clusters in 2D space.

## Customer Profiling

- Each cluster formed by K-Means is analyzed based on average values of key features like balance, purchases, credit limit, and payments.
- Insights into customer behavior such as high spenders, low-frequency payers, and cash advance users are provided.
- Marketing strategies are suggested for each customer group.

## Visualizations

- **Histograms**: Display feature distributions.
- **Boxplots**: Visualize the spread and outliers for each feature.
- **Correlation Heatmaps**: Show relationships between features.
- **Scatter Plots**: Visualize clusters using PCA and t-SNE.

## Usage

1. Install the required libraries:
   ```
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```

2. Run the notebook in a Jupyter environment:
   ```
   jupyter notebook customer_segmentation.ipynb
   ```

## Clustering Results

- Silhouette scores are calculated for each clustering method to evaluate the quality of clusters.
- The notebook provides detailed visualizations and insights into each cluster’s characteristics.

