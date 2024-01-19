# K-Nearest Neighbor(KNN)
- It is one of the simplest Machine Learning algorithms based on Supervised Learning technique.
- K-NN algorithm assumes the similarity between the new case/data and available cases and put the new case into the category that is most similar to the available categories.
- K-NN algorithm stores all the available data and classifies a new data point based on the similarity. This means when new data appears then it can be easily classified into a well suite category by using K- NN algorithm.
- KNN algorithm at the training phase just stores the dataset and when it gets new data, then it classifies that data into a category that is much similar to the new data.
- It is also called a lazy learner algorithm because it does not learn from the training set immediately instead it stores the dataset and at the time of classification, it performs an action on the dataset.
- K-NN is a non-parametric algorithm, which means it does not make any assumption on underlying data.
- K-NN algorithm can be used for Regression as well as for Classification but mostly it is used for the Classification problems.

## Why do we need a KNN algorithm?
- It does not require any assumptions about the underlying data distribution.
- It can also handle both numerical and categorical data, making it a flexible choice for various types of datasets in classification and regression tasks.
- The K-NN algorithm works by finding the K nearest neighbors to a given data point based on a distance metric, such as Euclidean distance. The class or value of the data point is then determined by the majority vote or average of the K neighbors. This approach allows the algorithm to adapt to different patterns and make predictions based on the local structure of the data.

## How to choose the value of k for KNN Algorithm?
The value of k in the k-nearest neighbors (k-NN) algorithm should be chosen based on the input data. If the input data has more outliers or noise, a higher value of k would be better. It is recommended to choose an odd value for k to avoid ties in classification.

## Working of KNN algorithm
The K-Nearest Neighbors (KNN) algorithm is a supervised learning method used for classification and regression problems. Here's a step-by-step explanation of how it works:

1. **Select the number K of the neighbors**: This is the number of nearest neighbors that the algorithm will consider in the training dataset.

2. **Calculate the Euclidean distance of K number of neighbors**: The algorithm calculates the distance between the new data point and all other points in the dataset. The most common method of calculating distance is the Euclidean distance, but other methods can also be used.

3. **Take the K nearest neighbors as per the calculated Euclidean distance**: The algorithm identifies the K points in the dataset that are closest to the new data point.

4. **Count the number of data points in each category among these K neighbors**: For each of the K nearest neighbors, the algorithm identifies the category of those points.

5. **Assign the new data points to the category for which the number of neighbors is maximum**: The new data point is assigned to the category that has the most neighbors.

This algorithm is based on the concept of similarity, meaning that a new data point will be classified based on how closely it matches the points in the training dataset. It's a non-parametric method, which means it does not make any assumptions about the underlying data distribution. It's widely used in real-life scenarios due to its simplicity and ease of implementation.

## Applications of the KNN Algorithm
Data Preprocessing, Pattern Recognition, Recommendation Engines

## Advantages
- Easy to implement
- Adapts easily
- It can be more effective if the training data is large.

## Disadvantages
- Does not scale
- Always needs to determine the value of K which may be complex some time.
- The computation cost is high because of calculating the distance between the data points for all the training samples.
