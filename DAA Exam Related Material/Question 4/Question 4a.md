## Define approximation algorithm. Write the performance ratios for approximation algorithm. Explain travelling-salesman problem with the triangle inequality.

An **approximation algorithm** is a way of dealing with NP-completeness for an optimization problem¹⁵⁶. This technique does not guarantee the best solution. The goal of the approximation algorithm is to come as close as possible to the optimal solution in polynomial time¹⁵⁶. Such algorithms are called approximation algorithms or heuristic algorithms¹.

The **performance ratios** for approximation algorithms are defined as follows¹²³⁴:
- Suppose that we are working on an optimization problem in which each potential solution has a cost, and we wish to find a near-optimal solution. Depending on the problem, we may define an optimal solution as one with maximum possible cost or one with minimum possible cost, i.e., the problem can either be a maximization or minimization problem¹.
- We say that an algorithm for a problem has an approximation ratio of P(n) if, for any input of size n, the cost C of the solution produced by the algorithm is within a factor of P(n) of the cost C* of an optimal solution¹. This is expressed as: max (C/C*,C*/C)<=P(n)¹.
- If an algorithm reaches an approximation ratio of P(n), then we call it a P(n)-approximation algorithm¹. For a maximization problem, 0< C < C*, and the ratio of C*/C gives the factor by which the cost of an optimal solution is larger than the cost of the approximate algorithm¹. For a minimization problem, 0< C* < C, and the ratio of C/C* gives the factor by which the cost of an approximate solution is larger than the cost of an optimal solution¹.

The **Travelling Salesman Problem (TSP)** is a well-known problem in computer science. It involves finding the shortest possible route that a traveling salesman can take to visit each city once and return to the original city⁷⁸⁹. When the cost function satisfies the triangle inequality, we can design an approximate algorithm for TSP that returns a tour whose cost is never more than twice the cost of an optimal tour⁷. The triangle inequality implies that for all vertices u, v, w in V, it is true that t(u, w) ≤ t(u, v) + t(v, w), where t is the cost function[^10^]. This means that the shortest path to reach a vertex w from u is always to reach w directly from u, rather than through some other vertex v[^10^]. This property is crucial for the design of approximation algorithms for the TSP⁷⁸⁹.

Source: Conversation with Bing, 25/1/2024
1. Approximation Algorithms - GeeksforGeeks. https://www.geeksforgeeks.org/approximation-algorithms/.
2. Approximation algorithm - Wikipedia. https://en.wikipedia.org/wiki/Approximation_algorithm.
3. Introduction to Approximation Algorithms - IIT Guwahati. https://www.iitg.ac.in/gkd/aie/slide/approximation-algorithms.pdf.
4. DAA | Approximation Algorithm - javatpoint. https://www.javatpoint.com/daa-approximate-algorithms.
5. Introduction to Approximation Algorithms 1 Approximation algorithms and .... https://cse.buffalo.edu/~hungngo/classes/2004/531/notes/Approx-Intro.pdf.
6. Approximation Algorithm - iitp.ac.in. https://www.iitp.ac.in/~sourav/CS204_2022/16.ApproximationAlgorithm.pdf.
7. Approximate solution for Travelling Salesman Problem using MST. https://www.geeksforgeeks.org/approximate-solution-for-travelling-salesman-problem-using-mst/.
8. 1 Traveling Salesman Problem - TUM. https://www14.in.tum.de/personen/khan/Arindam%20Khan_files/2.%20metric%20TSP.pdf.
9. THE TRAVELING SALESMAN PROBLEM - arXiv.org. https://arxiv.org/pdf/1001.0236v1.pdf.
10. Chapter 10. https://www.csd.uoc.gr/~hy583/papers/ch11.pdf.
