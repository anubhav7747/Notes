## Sort the following list of elements in increasing order using quick sort technique and argue on its running time, L = {60, 65, 70, 75, 80, 55, 50, 45, 40}.

Sure, let's use the QuickSort algorithm to sort the list L = {60, 65, 70, 75, 80, 55, 50, 45, 40} in increasing order. The QuickSort algorithm is a divide-and-conquer algorithm that works by selecting a 'pivot' element from the array and partitioning the other elements into two sub-arrays, according to whether they are less than or greater than the pivot. Here's how it works:

1. **Choose a pivot**: We'll choose 60 as the pivot for simplicity (usually the first element).

2. **Partition**: Rearrange the elements, so all elements less than 60 come before all elements greater than 60. After this step, the pivot is in its final position. This is the key process in the algorithm. The new array after partitioning based on 60 looks like this: {55, 50, 45, 40, 60, 65, 70, 75, 80}.

3. **Recursively apply** steps 1 and 2 to the sub-array of elements with smaller values and separately to the sub-array of elements with greater values.

The base case of the recursion is arrays of size zero or one, which are always sorted.

Here's the QuickSort algorithm in Python:

```python
def partition(arr, low, high):
    i = (low-1)
    pivot = arr[high]

    for j in range(low, high):
        if arr[j] <= pivot:
            i = i+1
            arr[i], arr[j] = arr[j], arr[i]

    arr[i+1], arr[high] = arr[high], arr[i+1]
    return (i+1)

def quickSort(arr, low, high):
    if len(arr) == 1:
        return arr
    if low < high:
        pi = partition(arr, low, high)
        quickSort(arr, low, pi-1)
        quickSort(arr, pi+1, high)
```

**Time Complexity Analysis**:
- **Best Case**: The best case occurs when the partition process always picks the middle element as the pivot. In this case, the time complexity is **O(n log n)**.
- **Worst Case**: The worst case occurs when the partition process always picks the greatest or smallest element as the pivot. If the list is already sorted, this would be the case. In this case, the time complexity is **O(n^2)**.
- **Average Case**: On average, the time complexity is **O(n log n)**.

**Space Complexity Analysis**:
The space complexity of the QuickSort algorithm is **O(log n)** because in the worst case, the maximum depth of the recursion tree is log n.

Source: Conversation with Bing, 25/1/2024
1. github.com. https://github.com/Robertingi00/Lokaverkefni_Reiknirit/tree/f3b252bf4601919eefa859e38c33ce43277b47dc/Algorithms%2FQuickSort%2FquickSort.py.
2. github.com. https://github.com/startupsandcode/codefundamentals/tree/1c77d88e69c83dc33712381c3101d9b04dd69bf6/Python%2Fsorts.py.
3. github.com. https://github.com/krohak/Project_Euler/tree/02b58da4d2a00f76028cb2429936b17df218a090/HackerRank%2FSort%2FQuick%2Fsave%2Fgfg.py.
4. github.com. https://github.com/gillarious/Blue-Studios-Interview-Prep/tree/b4366ac89e78229c5d424c323d7ee01a79fa878c/Lesson%208:%20Search%20and%20Sorting%20Algorithms%2FREADME.md.
5. github.com. https://github.com/L200184033/prak_algostruk/tree/4aae81d4f6f7143c9662cfb99c03f59df92d5afe/Modul%206%2FNo%207.py.
