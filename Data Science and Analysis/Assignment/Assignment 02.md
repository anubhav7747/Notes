## Calculate the mean, median, mode, standard deviation on the following dataset: 7, 10, 5, 13, 14, 9, 15.

1. **Mean**: The mean (or average) is the sum of all numbers divided by the count of numbers. 

$$\text{Mean} = \frac{7 + 10 + 5 + 13 + 14 + 9 + 15}{7} = 10.43$$

2. **Median**: The median is the middle number in a sorted list. If the list has an even number of observations, the median is the average of the two middle numbers. 

Sorted dataset: 5, 7, 9, 10, 13, 14, 15

$$\text{Median} = 10$$

3. **Mode**: The mode is the number that appears most frequently. In this case, all numbers appear only once, so there is no mode.

4. **Standard Deviation**: The standard deviation measures the amount of variation or dispersion in a set of values. 

First, calculate the variance (the average of the squared differences from the mean), then take the square root to get the standard deviation.

$$\text{Variance} = \frac{(7-10.43)^2 + (10-10.43)^2 + (5-10.43)^2 + (13-10.43)^2 + (14-10.43)^2 + (9-10.43)^2 + (15-10.43)^2}{7} = 11.67$$

$$\text{Standard Deviation} = \sqrt{11.67} = 3.42$$

So, the mean is **10.43**, the median is **10**, there is no mode, and the standard deviation is **3.42**.

<br>

## Write a short note on skewness and kurtosis. And their types.

1. **Skewness**: Skewness measures the asymmetry of a probability distribution about its mean. It can be of three types:
    - **Positive Skewness**: When the tail on the right side of the distribution is longer or fatter, the function is positively skewed. Here, the mean and median will be greater than the mode.
    - **Negative Skewness**: When the tail on the left side of the distribution is longer or fatter, the function is negatively skewed. Here, the mean and median will be less than the mode.
    - **Zero Skewness**: If the tails on both sides of the mean balance out overall, this is referred to as zero skewness or no skew.

2. **Kurtosis**: Kurtosis measures the "tailedness" of the probability distribution. It can be of three types:
    - **Leptokurtic**: If the distribution has heavier tails and a sharper peak than the normal distribution, it is referred to as leptokurtic. Leptokurtic distributions have positive excess kurtosis.
    - **Platykurtic**: If the distribution has lighter tails and a flatter peak than the normal distribution, it is referred to as platykurtic. Platykurtic distributions have negative excess kurtosis.
    - **Mesokurtic**: If the distribution has the same kurtosis as the normal distribution, it is referred to as mesokurtic. Mesokurtic distributions have zero excess kurtosis.

These measures are used to understand the shape of the distribution and provide insights into the dataset. They are especially useful in exploratory data analysis and predictive modeling.

<br>

## Explain pearson correlation coefficient.

The Pearson correlation coefficient, also referred to as Pearson's r, is a measure of the linear correlation between two variables X and Y. It has a value between +1 and -1, where:

- **1** is total positive linear correlation,
- **0** is no linear correlation, and
- **-1** is total negative linear correlation.

The formula for the Pearson correlation coefficient is:

$$r = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n} (x_i - \bar{x})^2(y_i - \bar{y})^2}}$$

where:
- \(x_i\) and \(y_i\) are the individual sample points indexed with \(i\),
- \(\bar{x}\) and \(\bar{y}\) are the means of \(x\) and \(y\),
- \(n\) is the total number of samples.

This coefficient is used in statistics to measure how strong a relationship is between two variables. For example, it could be used to relate the incomes of persons with their years of education, or to compare the performance of two stocks over time. It's a fundamental tool in the fields of statistics and data science.

<br>

## What are the various strategies for collecting data? Discuss the advantages and disadvantages of each strategies.

There are several strategies for collecting data, each with its own advantages and disadvantages. Here are a few common ones:

1. **Surveys**: Surveys involve asking a series of questions to a group of individuals. They can be conducted in person, over the phone, or online.

    *Advantages*: Surveys can reach a large number of people and provide quantitative data that is easy to analyze.
    
    *Disadvantages*: The quality of the data depends on the quality of the questions asked. Also, response rates can be low, especially for online surveys.

2. **Interviews**: Interviews involve one-on-one conversations between the researcher and the participant. They can be structured (with predetermined questions) or unstructured (more like a conversation).

    *Advantages*: Interviews provide in-depth, qualitative data and allow for more nuanced responses than surveys.
    
    *Disadvantages*: Interviews are time-consuming and the data can be difficult to analyze.

3. **Observations**: Observations involve watching and recording behavior or events as they occur naturally.

    *Advantages*: Observations can provide rich, qualitative data and allow for the study of behavior as it occurs naturally.
    
    *Disadvantages*: Observations can be time-consuming and the presence of the observer can influence the behavior being observed.

4. **Experiments**: Experiments involve manipulating one variable and observing the effect on another variable.

    *Advantages*: Experiments can establish cause-and-effect relationships and provide controlled conditions for testing hypotheses.
    
    *Disadvantages*: Experimental conditions may not reflect real-world conditions, and ethical considerations can limit the types of experiments that can be conducted.

5. **Secondary Data Analysis**: Secondary data analysis involves analyzing data that was collected by someone else.

    *Advantages*: Secondary data analysis can save time and resources since the data has already been collected.
    
    *Disadvantages*: The researcher has no control over what data was collected or how it was collected.

Each of these strategies can be effective depending on the research question and resources available. Often, a combination of strategies is used to provide a more complete picture of the phenomenon being studied.

<br>

## Construct a box plot for the following dataset: 7, 9, 11, 6, 10, 14, 8, 12.

A box plot (also known as a whisker plot) displays a summary of a set of data values. The box represents the interquartile range (the 25th to the 75th percentiles), the line inside the box is for the median (50th percentile) and the lines outside the box are for the minimum and maximum data values excluding outliers.

Here's how you can compute the components for your dataset (6, 7, 8, 9, 10, 11, 12, 14):

1. **Minimum**: The smallest number in the dataset. In this case, it's 6.
2. **First quartile (Q1)**: The middle number between the minimum and the median of the dataset. Here, it's 8.
3. **Median (Q2)**: The middle number of the dataset. When the dataset has an even number of observations, the median is the average of the two middle numbers. Here, it's 9.5.
4. **Third quartile (Q3)**: The middle value between the median and the maximum of the dataset. Here, it's 11.
5. **Maximum**: The largest number in the dataset. In this case, it's 14.

You can use these values to construct a box plot. If you're using a software like Excel or a programming language like Python or R, they have built-in functions to create box plots.
