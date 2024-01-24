## Write an algorithm for finding maximum and minimum element of an array and analysis best, worst, and average case complexity.

Sure, here is a simple algorithm to find the maximum and minimum elements in an array:

```python
def findMaxMin(arr):
    max_val = arr[0]
    min_val = arr[0]

    for i in range(1, len(arr)):
        if arr[i] > max_val:
            max_val = arr[i]
        elif arr[i] < min_val:
            min_val = arr[i]

    return max_val, min_val
```

In this algorithm, we initialize `max_val` and `min_val` as the first element of the array. Then we iterate over the rest of the array. If we find an element greater than `max_val`, we update `max_val`. Similarly, if we find an element smaller than `min_val`, we update `min_val`. At the end of the iteration, `max_val` and `min_val` hold the maximum and minimum values of the array, respectively¹.

**Time Complexity Analysis**:
- **Best Case**: The best case occurs when the array is already sorted in increasing order. In this case, the algorithm makes `n-1` comparisons, where `n` is the size of the array¹. So, the best case time complexity is **O(n)**¹.
- **Worst Case**: The worst case occurs when the array is sorted in decreasing order. In this case, the algorithm makes `2*(n-1)` comparisons¹. So, the worst case time complexity is **O(n)**¹.
- **Average Case**: On average, the algorithm makes `1.5*(n-1)` comparisons¹. So, the average case time complexity is also **O(n)**¹.

**Space Complexity Analysis**:
The space complexity of the algorithm is **O(1)**, as it uses a constant amount of space to store `max_val` and `min_val`¹.

Source: Conversation with Bing, 25/1/2024
1. Maximum and minimum of an array using minimum number of comparisons .... https://www.geeksforgeeks.org/maximum-and-minimum-in-an-array/.
2. Program to find the minimum (or maximum) element of an array. https://www.geeksforgeeks.org/program-find-minimum-maximum-element-array/.
3. algorithm - How to find max. and min. in array using minimum .... https://stackoverflow.com/questions/13544476/how-to-find-max-and-min-in-array-using-minimum-comparisons.
4. 1 Finding the Maximum and Minimum - IIT Bombay. https://www.cse.iitb.ac.in/~sundar/algorithms/lec5-1.pdf.
5. Time complexity analysis for finding the maximum element. https://stackoverflow.com/questions/30812472/time-complexity-analysis-for-finding-the-maximum-element.
6. Find the minimum and maximum value in an array - AfterAcademy. https://afteracademy.com/blog/find-the-minimum-and-maximum-value/.
7. Find minimum and maximum element in an array - GeeksforGeeks. https://www.geeksforgeeks.org/problems/find-minimum-and-maximum-element-in-an-array4428/1.
8. Average Case Analysis for finding max and min value on an array. https://cs.stackexchange.com/questions/89842/average-case-analysis-for-finding-max-and-min-value-on-an-array.
9. Min and Max element in array - OpenGenus IQ. https://iq.opengenus.org/min-and-max-element-in-array/.
10. Find Maximum and Minimum Element in an Array - EnjoyAlgorithms. https://www.enjoyalgorithms.com/blog/find-the-minimum-and-maximum-value-in-an-array/.
11. K’th Smallest/Largest Element in Unsorted Array - GeeksforGeeks. https://www.geeksforgeeks.org/kth-smallest-largest-element-in-unsorted-array/.
