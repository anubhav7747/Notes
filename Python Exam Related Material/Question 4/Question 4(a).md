## Differentiate between bar() and barh(). In python, what is the default width value of the bars in any bar graph? Write a Python program to draw a pie chart using pie() and legend() methods. Also show the O/P of this code.

In Python's `matplotlib` library, `bar()` and `barh()` are used to generate bar plots. The difference between them lies in the orientation of the bars.

- `bar()`: Creates a **vertical** bar plot. It takes two arguments: categorical variables and values.
- `barh()`: Creates a **horizontal** bar plot. It also takes two arguments: categorical variables and values.

The default width of the bars in a bar graph in matplotlib is `0.8`.

Now, let's write a Python program to draw a pie chart using `pie()` and `legend()` methods:

```python
import matplotlib.pyplot as plt

# Pie chart data
labels = ['Apple', 'Banana', 'Mango', 'Grapes']
sizes = [15, 30, 45, 10]

# Create a pie chart
plt.pie(sizes, labels=labels, autopct='%1.1f%%')

# Add a legend
plt.legend()

# Display the chart
plt.show()
```

In this code, `labels` are the categories and `sizes` are their corresponding values. The `pie()` function creates a pie chart. The `autopct` parameter is used to format the value of each label. The `legend()` function adds a legend to the chart. The `show()` function displays the chart.

Please note that I can't show the output of this code here, but when you run this code in a Python environment that supports plotting (like Jupyter notebook or PyCharm), it will display a pie chart with four sections labeled 'Apple', 'Banana', 'Mango', and 'Grapes'. The sizes of the sections correspond to the values in the `sizes` list, and the percentages represent the proportion of each category. The legend will show the label for each category. Remember to handle exceptions and edge cases as per your requirements. Also, the actual implementation of your code will depend on your specific needs and design choices. This is just a basic example to illustrate the concept.
