# K-Means Clustering
  - It is a popular unsupervised machine learning algorithm used to solve the clustering problems in machine learning or data science.
  - It is used for partitioning a dataset into K distinct, non-overlapping subsets (clusters).
  - The goal of K-Means is to assign each data point to one of K clusters in a way that minimizes the sum of squared distances between the data points and the centroid of their respective clusters.
  - The algorithm is iterative and converges to a solution, but it may find local optima, meaning the result depends on the initial configuration..

> It is an iterative algorithm that divides the unlabeled dataset into k different clusters in such a way that each dataset belongs only one group that has similar properties.

The k-means clustering algorithm mainly performs two tasks:
  1. Determines the best value for K center points or centroids by an iterative process.
  2. Assigns each data point to its closest k-center. Those data points which are near to the particular k-center, create a cluster.

  ![k-means-clustering-algorithm-in-machine-learning](https://github.com/anubhav7747/Notes/assets/77168708/a5cec492-8980-4ee8-82bc-0bc5e5f1df89)

Here are the key steps of the K-Means clustering algorithm:

1. **Initialization:**
    - Choose the number of clusters, K.
    - Randomly initialize K cluster centroids. These centroids represent the initial guess for the cluster centers.
2. **Assignment Step:**
    - Assign each data point to the cluster whose centroid is closest to it. The closeness is often measured using Euclidean distance, but other distance metrics can be used.
3. **Update Step:**
    - Recalculate the centroid of each cluster by taking the mean of all the data points assigned to that cluster.
4. **Repeat:**
    - Repeat steps 2 and 3 until convergence. Convergence occurs when the assignment of data points to clusters no longer changes or changes very minimally.
  
## What is the objective of k-means clustering?
The goal of clustering is to divide the population or set of data points into a number of groups so that the data points within each group are more comparable to one another and different from the data points within the other groups. It is essentially a grouping of things based on how similar and different they are to one another.

## Conclusion
K-means clustering is a powerful unsupervised machine learning algorithm for grouping unlabeled datasets. Its objective is to divide data into clusters, making similar data points part of the same group. The algorithm initializes cluster centroids and iteratively assigns data points to the nearest centroid, updating centroids based on the mean of points in each cluster.
