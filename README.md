# Crypto-Clustering-Challenge
Deploy unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes leveraging, Python, K-Means and Principal Component Analysis.

<img width="1134" alt="Screen Shot 2023-04-17 at 5 14 16 PM" src="https://user-images.githubusercontent.com/44728723/232612256-75ac399d-25ca-472f-b155-acc50cf8b60b.png">

## Data Description
- The dataset contained pricing data for 41 cryptocurrencies such as: bitcoin, ethereum, tether and ripple among others.
- 7 columns contain pricing changes for 24-hour, 7-day, 14-day, 30-day, 60-day, 200-day and 1 year periods for each cryptocurrency.

## Approach
- K-means:
  - The data was normalized using the StandardScaler() module from scikit-learn
  - Used the elbow method to find the best value for k for the scaled dataset (see plot #1 below)
  - Used K-means to cluster the cryptocurrencies in the scaled dataset
- PCA (Principal Component Analysis)
  - Using the original scaled data, PCA was performed to optimize clusters by reducing the features to three principal components
  - The explained variance was determined for the three principal components
  - The elbow method was used on the PCA data to find the best value for k
  - K-means was used to cluster the cryptocurrencies in the PCA data
- Comparison of K-Means Original Features to the PCA Features
  - Plots of the elbow graph and clustered scatter plots were compared between the two approaches

## Findings
