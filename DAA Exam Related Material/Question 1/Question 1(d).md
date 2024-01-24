## Explain in brief the greedy strategy of algorithm design and write control abstraction of greedy approach.

The **greedy strategy** of algorithm design is an approach that builds up a solution piece by piece, always choosing the next piece that offers the most obvious and immediate benefit⁴⁶. This approach never reconsiders the choices taken previously⁴⁶. The problems where choosing locally optimal also leads to a global solution are the best fit for the Greedy method⁴. For example, consider the Fractional Knapsack Problem⁴.

Here is the **control abstraction** of the greedy approach¹²:

```python
def Greedy(a, n):
    solution = []  # initializes to empty
    for i in range(n):
        x = select(a)
        if feasible(solution, x):
            solution = union(solution, x)
    return solution
```

In this pseudocode:
- `a` is the set of inputs.
- `n` is the number of inputs.
- `select(a)` is a function that selects a candidate from the set `a`.
- `feasible(solution, x)` is a function that checks if it's feasible to add the candidate `x` to the current `solution`.
- `union(solution, x)` is a function that adds the candidate `x` to the `solution` if it's feasible¹².

The **time complexity** of a greedy algorithm depends on the problem being solved⁴⁶. However, in general, greedy algorithms tend to be efficient because they make locally optimal choices at each step⁴⁶.

Source: Conversation with Bing, 25/1/2024
1. Greedy Algorithms - GeeksforGeeks. https://www.geeksforgeeks.org/greedy-algorithms/.
2. Greedy Algorithms - Online Tutorials Library. https://www.tutorialspoint.com/design_and_analysis_of_algorithms/design_and_analysis_of_algorithms_greedy_method.htm.
3. Greedy Method and its control abstraction with Space and Time ... - Studocu. https://www.studocu.com/in/document/sathyabama-institute-of-science-and-technology/computer-science/greedy-method-and-its-control-abstraction-with-space-and-time-complexity/55755316.
4. UNIT-3 The Greedy Method: Introduction, Huffman Trees and ... - PVPSIT. http://www.pvpsiddhartha.ac.in/dep_it/lecture%20notes/DAA19/Unit-3.pdf.
5. Greedy Algorithm - What Every one Has to Say? - CodeCrucks. https://codecrucks.com/greedy-algorithm/.
6. Greedy Algorithms Introduction - javatpoint. https://www.javatpoint.com/greedy-algorithms.
7. Greedy Algorithm - Programiz. https://www.programiz.com/dsa/greedy-algorithm.
