# Support Vector Machine #

- Support Vector Machine or SVM is one of the most popular Supervised Learning algorithms, which is used for Classification as well as Regression problems.
- However, primarily it is used for Classification problems in Machine Learning.
- The goal of the SVM algorithm is to create the best line or decision boundary that can segregate n-dimensional space into classes so that we can easily put the new data point in the correct category in the future.
- This best desicion boundary is called a hyperplane.
- There can be multiple lines/decision boundaries to segregate the classes in n-dimensional space, but we need to find out the best decision boundary that helps to classify the data points.
- This best boundary is known as the hyperplane of SVM.
- The dimensions of the hyperplane depend on the features present in the dataset, which means if there are 2 features (as shown in image), then hyperplane will be a straight line.
- And if there are 3 features, then hyperplane will be a 2-dimension plane.
- We always create a hyperplane that has a maximum margin, which means the maximum distance between the data points.

![support-vector-machine-algorithm](https://github.com/anubhav7747/Notes/assets/77168708/1163e88e-b963-4d7f-a608-e249b839c4de)

SVM algorithm can be used for **Face detection**, **image classification**, **text categorization**, etc.

![support-vector-machine-algorithm2](https://github.com/anubhav7747/Notes/assets/77168708/3f281c7b-f5f3-4fa5-8946-f83cd8a01225)


Let’s consider two independent variables x1, x2, and one dependent variable which is either a blue circle or a red circle.
![Capture](https://github.com/anubhav7747/Notes/assets/77168708/1a76b161-a01f-4052-8f39-2babbf7eed2b)

From the figure above it’s very clear that there are multiple lines (our hyperplane here is a line because we are considering only two input features x1, x2) that segregate our data points or do a classification between red and blue circles. So how do we choose the best line or in general the best hyperplane that segregates our data points?



## SVM can be of two types ##
### 1. Linear SVM: ###
- Linear SVM is used for linearly separable data, which means if a dataset can be classified into two classes by using a single straight line, then such data is termed as linearly separable data, and classifier is used called as Linear SVM classifier.
### 2. Non-Linear SVM: ###
- Non-Linear SVM is used for non-linearly separated data, which means if a dataset cannot be classified by using a straight line, then such data is termed as non-linear data and classiifier used is called as Non-linear SVM classiifer.
- If data is linearly arranged, then we can separate it using a straight line, but for non-linear data, we cannot draw a single straight line. So to separate these data points, we need to add one more dimension.
- For linear data, we have used two dimensions x and y, so for non-linear data, we will add a third dimension z.
- It can be calculated as: **z = x<sup>2</sup> + y<sup>2</sup>**



## How does SVM work? ##
**Linear SVM:** The working of the SVM algorithm can be understood by using an example. Suppose we have a dataset that has two tags (green and blue), and the dataset has two features x1 and x2. We want a classifier that can classify the pair(x1, x2) of coordinates in either green or blue. Consider the below image:

![support-vector-machine-algorithm3](https://github.com/anubhav7747/Notes/assets/77168708/10ad62d3-b3f6-4e99-a89e-7f0881bf5d89)

So as it is 2-d space so by just using a straight line, we can easily separate these two classes. But there can be multiple lines that can separate these classes. Consider the below image:

![support-vector-machine-algorithm4](https://github.com/anubhav7747/Notes/assets/77168708/cd8f7100-e3bd-496c-95b4-306f851cec8f)

Hence, the SVM algorithm helps to find the best line or decision boundary; this best boundary or region is called as a hyperplane. SVM algorithm finds the closest point of the lines from both the classes. These points are called support vectors. The distance between the vectors and the hyperplane is called as margin. And the goal of SVM is to maximize this margin. The hyperplane with maximum margin is called the optimal hyperplane.

![support-vector-machine-algorithm5](https://github.com/anubhav7747/Notes/assets/77168708/0d1df9e3-f673-409a-a2a9-808a559dd8ac)

**Non-Linear SVM:** If data is linearly arranged, then we can separate it by using a straight line, but for non-linear data, we cannot draw a single straight line. Consider the below image:

![support-vector-machine-algorithm6](https://github.com/anubhav7747/Notes/assets/77168708/1f9af4ce-5452-480c-ba50-b72e71827b2f)

So to separate these data points, we need to add one more dimension. For linear data, we have used two dimensions x and y, so for non-linear data, we will add a third dimension z. It can be calculated as:

> z = x<sup>2</sup> + y<sup>2</sup>

By adding the third dimension, the sample space will become as below image:

![support-vector-machine-algorithm7](https://github.com/anubhav7747/Notes/assets/77168708/3d3f5c40-c65a-476c-969f-788c8d750327)

So now, SVM will divide the datasets into classes in the following way. Consider the below image:

![support-vector-machine-algorithm8](https://github.com/anubhav7747/Notes/assets/77168708/2b5a08b3-5579-4501-886d-7d954f431e3f)

Since we are in 3-d Space, hence it is looking like a plane parallel to the x-axis. If we convert it in 2d space with z=1, then it will become as:

![support-vector-machine-algorithm9](https://github.com/anubhav7747/Notes/assets/77168708/98d0ed1d-bbba-4d5e-903d-7004879d4138)

Hence we get a circumference of radius 1 in case of non-linear data.

## Applications of support vector machine: ##
1. **Face observation** - It is used for detecting the face according to the classifier and model.
2. **Text and hypertext arrangement** - In this, the categorization technique is used to find important information or you can say required information for arranging text.
3. **Bioinformatics** - It is also used for medical science as well like in labratory, DNA, research, etc.
4. **Handwriting remembrance** - In this, it is used for handwriting recognition.
5. In the case of classification, the goal is to find a boundary that separates the different classes of data as well as possible. The input data is plotted in a high-dimensional space (with as many dimensions as the number of features), and the SVM algorithm finds the best boundary that separates the classes.
6. In the case of regression, the goal is to find the best hyperplane that fits the data. Similar to classification, the data is plotted in a high-dimensional space, but instead of trying to separate the classes, the algorithm is trying to fit the data with the best hyperplane.
7. One of the main advantages of SVM is that it works well in high-dimensional spaces and it’s relatively memory efficient. it also able to handle non-linearly separable data by transforming them into a higher dimensional space where they become linear separable, this is done by using kernel trick.
8. SVMs are not just limited to linear boundaries, it could also handle non-linear boundaries by using kernel functions that allow us to map the input data into a higher-dimensional space where it becomes linearly separable. The most commonly used kernel functions are linear, polynomial and radial basis functions (RBF).
9. SVMs are popular in various applications such as image classification, natural language processing, bioinformatics, and more.
