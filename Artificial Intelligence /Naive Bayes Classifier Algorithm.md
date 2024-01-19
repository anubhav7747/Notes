# Naive Bayes Classifier Algorithm
Naive Bayes is a probabilistic machine learning algorithm that is commonly used for classification tasks, particularly in natural language processing (NLP) and text classification. It's based on Bayes' theorem, which calculates the probability of a hypothesis (class) given the observed evidence (features). The "naive" assumption in Naive Bayes is that features are conditionally independent, which simplifies the calculation of probabilities.

Here are the key steps in the Naive Bayes algorithm for classification:
1. **Data Preprocessing**
   - Prepare the dataset, ensuring that it is labeled with the classes to be predicted and that features are appropriately represented.

2. **Calculate Class Priors**
   - Calculate the prior probability of each class. This is done by counting the number of occurrences of each class in the training set and dividing by the total number of instances.

     _P(class=c)= (Number of instances with class c) / (Total number of instances)_

3. **Calculate Likelihoods**
   - For each feature, calculate the likelihood of observing that feature given the class. Depending on the type of feature (categorical or continuous), different probability distributions may be used.

     _P(feature = x ∣ class = c)_

   - For continuous features, a common choice is to assume a normal (Gaussian) distribution.

5. **Calculate Posterior Probabilities**
   - Use Bayes' theorem to calculate the posterior probability of each class given the observed features:

     _P(class = c ∣ features) ∝ P(class = c) × ∏<sup>n</sup><sub>i=1</sub> P(feature<sub>i</sub> ∣ class = c)_

   - The symbol **∝** denotes proportionality. The class with the highest posterior probability is the predicted class.

6. **Make Predictions**
   - Assign the instance to the class with the highest posterior probability.

### Example
Consider a spam classification problem where the goal is to determine whether an email is spam or not based on the presence of certain words (features). The Naive Bayes algorithm would calculate the probability of an email being spam given the observed words.
