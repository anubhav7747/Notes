## Write and explain an algorithm for n-queens problem using backtracking method and comments on its time complexity.

Sure, here is the algorithm for the N-Queens problem using the backtracking method¹:

```python
def isSafe(board, row, col, N):
    # Check this row on left side
    for i in range(col):
        if board[row][i] == 1:
            return False

    # Check upper diagonal on left side
    for i, j in zip(range(row, -1, -1), range(col, -1, -1)):
        if board[i][j] == 1:
            return False

    # Check lower diagonal on left side
    for i, j in zip(range(row, N, 1), range(col, -1, -1)):
        if board[i][j] == 1:
            return False

    return True

def solveNQUtil(board, col, N):
    # base case: If all queens are placed
    # then return true
    if col >= N:
        return True

    # Consider this column and try placing
    # this queen in all rows one by one
    for i in range(N):

        if isSafe(board, i, col, N):
            # Place this queen in board[i][col]
            board[i][col] = 1

            # recur to place rest of the queens
            if solveNQUtil(board, col + 1, N) == True:
                return True

            # If placing queen in board[i][col
            # doesn't lead to a solution, then
            # remove queen from board[i][col]
            board[i][col] = 0

    # If the queen cannot be placed in any row in
    # this column col then return false
    return False

def solveNQ(N):
    board = [[0]*N for _ in range(N)]

    if solveNQUtil(board, 0, N) == False:
        print("Solution does not exist")
        return False

    printSolution(board)
    return True
```

In this algorithm:
- `isSafe()` checks if a queen can be placed on the board at the given position.
- `solveNQUtil()` uses backtracking to try different row numbers for a given column.
- If placing a queen in a certain position leads to a solution, it returns `True`.
- If placing a queen doesn't lead to a solution, then it backtracks and removes the queen from the current position and continues to the next position.
- `solveNQ()` initializes the problem and calls `solveNQUtil()`.

The **time complexity** of the N-Queens problem using the backtracking method is O(N!) in the worst case⁶⁷. This is because in the worst case, the algorithm generates all possible permutations of the N queens and then checks each permutation for feasibility⁶⁷. However, the backtracking method significantly reduces the search space, making the algorithm faster in practice⁶⁷.

Source: Conversation with Bing, 25/1/2024
1. N Queen Problem - GeeksforGeeks. https://www.geeksforgeeks.org/n-queen-problem-backtracking-3/.
2. Time complexity of N Queen using backtracking? - Stack Overflow. https://stackoverflow.com/questions/21059422/time-complexity-of-n-queen-using-backtracking.
3. Solving N Queens Problem Using Backtracking :: AlgoTree. https://algotree.org/algorithms/backtracking/nqueens/.
4. N Queens Problems - javatpoint. https://www.javatpoint.com/n-queens-problems.
5. Beginner's guide to Solving the N- Queens problem using backtracking method. http://www.facweb.iitkgp.ac.in/~bibhas/Bactracking.pdf.
6. N Queen's problem and solution using backtracking algorithm. https://www.includehelp.com/algorithms/n-queens-problem-and-solution-using-backtracking-algorithm.aspx.
7. N-Queens solving algorithm by sets and backtracking. https://ieeexplore.ieee.org/document/7506688/.
8. 8 Queens Problem using Backtracking - OpenGenus IQ. https://iq.opengenus.org/8-queens-problem-backtracking/.
9. undefined. https://sites.google.com/site/nqueensolver/home/algorithm-results.
10. undefined. https://sites.google.com/site/nqueensolver/home/algorithms/2backtracking-algorithm.
11. github.com. https://github.com/prakashsellathurai/a-grim-loth/tree/4cbbe0e76809379e4f3b8ada4051c7bac20dfea7/python%2Fproblems%2Frecursion-and-backtracking.py.
12. github.com. https://github.com/leroydeniz/MAC/tree/f3de83334f72e4b46ee41749f921cbb2f8742a6e/LAB10%2FCode%20for%20Students%2Fnqueens_backtracking.py.
13. github.com. https://github.com/maximised/College_work/tree/054c029378b9692845c02c1c33862f3badfc16dc/Personal_projects%2FJupyter_Notebook%2Fqueens.py.
14. github.com. https://github.com/rakshakrawat/analysis-of-algorithms/tree/a93a538ca63a09b7ef4b0c47ac1272a629237248/N%20Queen%27s%20problem.py.
15. github.com. https://github.com/preethi-sv/Backtracking-problems/tree/07d61f93689016b965fafe992804fd92f177d079/nQueens.py.
16. github.com. https://github.com/vishrutkmr7/DailyPracticeProblemsDIP/tree/1b750fd0e06eeb84b06c5f9ca45b8ce8b45f3601/2020%2F01%20January%2Fdp01052020.py.
17. github.com. https://github.com/deshmukhrajvardhan/DailyCodingProblem/tree/231636aff6020b9b0b2ae831cd5870f83403bbc0/solutions%2Fqueen.py.
