# Decision Tree
- A Decision Tree is a popular machine learning algorithm used for both classification and regression tasks. It is a tree-like model where an internal node represents a feature or attribute, the branches represent the decision rules, and each leaf node represents the outcome or class label. Decision Trees are intuitive, easy to understand, and can handle both numerical and categorical data.
- In a Decision tree, there are two nodes, which are the Decision Node and Leaf Node. Decision nodes are used to make any decision and have multiple branches, whereas Leaf nodes are the output of those decisions and do not contain any further branches.
- The decisions or the test are performed on the basis of features of the given dataset.
- It is called a decision tree because, similar to a tree, it starts with the root node, which expands on further branches and constructs a tree-like structure.
- A decision tree simply asks a question, and based on the answer (Yes/No), it further split the tree into subtrees.

  ![decision-tree-classification-algorithm](https://github.com/anubhav7747/Notes/assets/77168708/94503032-fcb9-48ab-87b3-860c44d4b20a)


## Why use Decision Trees?
- Decision Trees usually mimic human thinking ability while making a decision, so it is easy to understand.
- The logic behind the decision tree can be easily understood because it shows a tree-like structure.


## Key components and concepts associated with Decision Trees:
1. **Root Node:**
   - The topmost node in the tree, representing the feature that best splits the data based on certain criteria.

2. **Internal Nodes:**
   - Intermediate nodes that represent features and decision rules.
   - Each internal node tests a specific attribute, and the data is split based on the outcome of the test.

3. **Branches:**
   - The branches or edges connecting nodes represent the possible outcomes of a decision rule.
   - For each internal node, there are branches leading to child nodes corresponding to different outcomes of the decision.

4. **Leaf Nodes:**
   - Terminal nodes or leaves represent the final predicted class (for classification) or the predicted value (for regression).
   - Each leaf node contains the majority class (in classification) or the average value (in regression) of the instances that reached that node.

5. **Decision Rules:**
   - Rules that determine how the data is split at each internal node.
   - The decision rules are based on the values of the features.

6. **Splitting Criteria:**
   - The criteria used to determine the best feature to split on at each internal node.
   - For classification, common criteria include Gini impurity and information gain (entropy), while for regression, mean squared error is often used.

7. **Pruning:**
   - Decision Trees can be prone to overfitting, especially if they are deep and capture noise in the training data.
   - Pruning involves removing branches that add little predictive power to improve the tree's generalization to new, unseen data.


## How Decision Tree is formed?
The process of forming a decision tree involves recursively partitioning the data based on the values of different attributes. The algorithm selects the best attribute to split the data at each internal node, based on certain criteria such as information gain or Gini impurity. This splitting process continues until a stopping criterion is met, such as reaching a maximum depth or having a minimum number of instances in a leaf node.


## Decision Tree algorithm
- **Step-1:** Begin the tree with the root node, says S, which contains the complete dataset.
- **Step-2:** Find the best attribute in the dataset using Attribute Selection Measure (ASM).
- **Step-3:** Divide the S into subsets that contains possible values for the best attributes.
- **Step-4:** Generate the decision tree node, which contains the best attribute.
- **Step-5:** Recursively make new decision trees using the subsets of the dataset created in step-3. Continue this process until a stage is reached where you cannot further classify the nodes and called the final node as a leaf node.

### Example
Suppose there is a candidate who has a job offer and wants to decide whether he should accept the offer or Not. So, to solve this problem, the decision tree starts with the root node (Salary attribute by ASM). The root node splits further into the next decision node (distance from the office) and one leaf node based on the corresponding labels. The next decision node further gets split into one decision node (Cab facility) and one leaf node. Finally, the decision node splits into two leaf nodes (Accepted offers and Declined offer). Consider the below diagram:

  ![decision-tree-classification-algorithm2](https://github.com/anubhav7747/Notes/assets/77168708/fe835fe4-b638-478e-b5b2-a030ed5092ca)


## Attribute Selection Measures
The goal is to identify which attributes contribute the most to the predictive accuracy of a model. There are two popular techniques for ASM:

1. **Information Gain:**
   - Information Gain is a measure used in decision trees, particularly in the ID3 (Iterative Dichotomiser 3) algorithm.
   - It calculates how much information a feature provides us about a class.
   - According to the value of information gain, we split the node and build the decision tree.
   - High information gain suggests that the attribute is a good predictor.

2. **Gini Index:**
   - Gini Index is a criterion used in the CART (Classification and Regression Trees) algorithm for decision tree construction.
   - It measures the impurity of a set of examples.
   - A lower Gini Index indicates better purity, meaning the attribute is a good predictor.


## Advantages
- It is simple to understand as it follows the same process which a human follow while making any decision in real-life.
- Handle both numerical and categorical data without requiring extensive preprocessing.
- It can be very useful for solving decision-related problems.
- It helps to think about all the possible outcomes for a problem.
- There is less requirement of data cleaning compared to other algorithms.


## Disadvantages
- The decision tree contains lots of layers, which makes it complex.
- It may have an overfitting issue, which can be resolved using the Random Forest algorithm.
- For more class labels, the computational complexity of the decision tree may increase.

## Conclusion
Decision trees, a key tool in machine learning, model and predict outcomes based on input data through a tree-like structure. They offer interpretability, versatility, and simple visualization, making them valuable for both categorization and regression tasks. While decision trees have advantages like ease of understanding, they may face challenges such as overfitting.
