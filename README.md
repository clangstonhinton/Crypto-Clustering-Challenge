# Crypto-Clustering-Challenge
Deploy unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes leveraging, Python, K-Means and Principal Component Analysis.

<img width="1134" alt="Screen Shot 2023-04-17 at 5 14 16 PM" src="https://user-images.githubusercontent.com/44728723/232612256-75ac399d-25ca-472f-b155-acc50cf8b60b.png">

## Data Description
- The dataset contained pricing data for 41 cryptocurrencies such as: bitcoin, ethereum, tether and ripple among others.
- 7 columns contain pricing changes for 24-hour, 7-day, 14-day, 30-day, 60-day, 200-day and 1 year periods for each cryptocurrency.

## Approach
- K-means:
  - The data were normalized using the StandardScaler module from scikit-learn
  - Used the elbow method to find the best value for k for the scaled dataset
  - Used K-means to cluster the cryptocurrencies in the scaled dataset
- PCA (Principal Component Analysis)
  - Using the original scaled data, PCA was performed to optimize clusters by reducing the features to three principal components
  - The explained variance was determined for the three principal components
  - The elbow method was used on the PCA data to find the best value for k
  - K-means was used to cluster the cryptocurrencies in the PCA data
- Comparison of K-Means Original Features to the PCA Features
  - Plots of the elbow graph and clustered scatter plots were compared between the two approaches

## Findings
1. The optimal value for k against the original scaled data was determined to be 4 clusters using the elbow-method.
<img width="578" alt="Screen Shot 2023-04-20 at 1 14 17 PM" src="https://user-images.githubusercontent.com/44728723/233440319-cb0fe5bc-ed7c-4ea6-9cf2-b7be20202ed0.png">


    
2. The features were reduced to 3 in the PCA approach and explained 89% of the variance in the dataset.
    
3. The PCA approach indicated that the best value for k continued to be 4 based on the elbow-method. However, the inertia values were smaller with PCA than KMeans approach.
<img width="594" alt="Screen Shot 2023-04-20 at 1 14 54 PM" src="https://user-images.githubusercontent.com/44728723/233440344-03d8bc2b-0e90-4406-a7a3-c7cfd2965a59.png">


    
4. When comparing scatter plots of the clusters from the two approaches, the PCA approach with 3 features produced more tightly grouped clusters than the original KMeans approach.  

<img width="591" alt="Screen Shot 2023-04-20 at 1 07 17 PM" src="https://user-images.githubusercontent.com/44728723/233438607-2722d28e-3b5f-4a7c-b24e-c11b874371b4.png">

    
5. The two outliers (celsius-degree-token and ethelend) are the same in both the KMeans Original Scatter and the PCA Scatter plots. It may be beneficial to re-run the models after removing the two outliers from the dataset.




