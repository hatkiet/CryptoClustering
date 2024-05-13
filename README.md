# CryptoClustering
In this challenge, I have used our knowledge of Python and unsupervised learning (activities in class) to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

Data Source: "crypto_market_data.csv"

***Original Data:***
<img width="1162" alt="Original data" src="https://github.com/hatkiet/CryptoClustering/assets/154276115/b6fb6c82-35e4-4d20-85e9-d53413894ba9">

* Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

* Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

<img width="2387" alt="Original scaled values" src="https://github.com/hatkiet/CryptoClustering/assets/154276115/9d19c21f-8531-4caf-acd1-88e1f0ad9a9c">

Used the Elbow Method to find the best value of k by using original scaled and PCA Datasets

<img width="2033" alt="Elbow plots" src="https://github.com/hatkiet/CryptoClustering/assets/154276115/c000a31d-4e97-4258-a752-6c4944d49145">

* Question: What is the best value for k?

* Answer: _According to the Elbow Curve, the "k" value of 4 is the best option for both, since it represents a strong inflection point._

**Optimize Clusters with PCA**

<img width="712" alt="PCAs values" src="https://github.com/hatkiet/CryptoClustering/assets/154276115/d9594b06-7efc-4c33-9ed6-3f5796451522">

**Clustered Cryptocurrencies with K-Means using Original Scaled and PCA Dataset**

<img width="2033" alt="Clusters plots" src="https://github.com/hatkiet/CryptoClustering/assets/154276115/63badc38-1f21-4525-83c9-2bfbb08a8ed0">

* Question: After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?
  
* Answer: _Based on the elbow curves, it was discovered that employing fewer features yielded comparable outcomes to the initial model. Both models exhibited a peak k-value of 4. However, upon visualizing the data through scatter plots utilizing PCA, disparities surfaced when compared to the original depiction. While utilizing numerous features may seem advantageous, it can sometimes lead to overfitting. On the other hand, using fewer features in the right-hand plot provides a more distinguishable portrayal of clusters. For example, clusters 0 and 2, which seem indistinguishable in the original data plot owing to their proximity, are distinctly separated in the PCA-based plot. Similarly, the distinction between clusters 1 and 2 is more visible in the PCA-based visualization on the right side of the plot._
