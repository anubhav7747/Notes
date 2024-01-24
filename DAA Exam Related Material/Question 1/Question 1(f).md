## Write merge sort algorithm using divide-and-conquer approach and discuss its time complexity.

Sure, here is the **Merge Sort** algorithm using the divide-and-conquer approach⁶:

```python
def mergeSort(arr):
    if len(arr) > 1:
        mid = len(arr)//2
        L = arr[:mid]
        R = arr[mid:]

        mergeSort(L)
        mergeSort(R)

        i = j = k = 0

        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1

        while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1

        while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1
```

In this algorithm:
- The `mergeSort` function repeatedly divides the array into two halves until we reach a stage where we try to perform MergeSort on a subarray of size 1⁶.
- After that, the `merge` function comes into play and combines the sorted arrays into larger arrays until the whole array is merged⁶.

**Time Complexity Analysis**:
- The time complexity of Merge Sort is **O(n log n)** in all cases (best, average, and worst) as merge sort always divides the array into two halves and takes linear time to merge two halves¹.
- The space complexity of Merge Sort is **O(n)** because an extra space of size n is needed for the temporary array¹..

Source: Conversation with Bing, 25/1/2024
1. Merge Sort (With Code in Python/C++/Java/C) - Programiz. https://www.programiz.com/dsa/merge-sort.
2. Time and Space Complexity Analysis of Merge Sort. https://www.geeksforgeeks.org/time-and-space-complexity-analysis-of-merge-sort/.
3. Merge Sort – Data Structure and Algorithms Tutorials. https://www.geeksforgeeks.org/merge-sort/.
4. Merge Sort Algorithm | Studytonight. https://www.studytonight.com/data-structures/merge-sort.
5. What is the Time Complexity of Merge Sort? - Scaler Topics. https://www.scaler.com/topics/merge-sort-time-complexity/.
6. Merge Sort Algorithm: Design, Implementation and Analysis. https://www.enjoyalgorithms.com/blog/merge-sort-algorithm/.
7. Divide and conquer strategy to merge multiple sorted arrays. https://stackoverflow.com/questions/32219070/divide-and-conquer-strategy-to-merge-multiple-sorted-arrays.
8. Merge Sort - javatpoint. https://www.javatpoint.com/merge-sort.
9. Merge sort algorithm overview (article) | Khan Academy. https://www.khanacademy.org/computing/computer-science/algorithms/merge-sort/a/overview-of-merge-sort.
10. github.com. https://github.com/loma373/Sorting-Techniques/tree/aba479e8a8c845ae48e359262e2a2ff1e8413b82/mergeSort.py.
11. github.com. https://github.com/upluke/Hundreds-ALG-0/tree/98cd8b9f16f09e5c1984ba80c8e13c5bee12ec73/README.md.
12. github.com. https://github.com/L200184033/prak_algostruk/tree/4aae81d4f6f7143c9662cfb99c03f59df92d5afe/Modul%206%2FNo%207.py.
13. en.wikipedia.org. https://en.wikipedia.org/wiki/Merge_sort.
