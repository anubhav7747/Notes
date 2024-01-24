## define solution space and e-node. consider a combination of lock for a bicycle that consists of a set of N switches each of which can be 'on' or 'off'. Suppose you have forgotten this combination and you are willing to try all the combination so that lock must get open. You need to model (represent all combinations as binary tree and show backtrack assume N=4) each possible combination with an n-tuple of 0's and 1's, where 1 for the switch on, 0 for switch off and also need to show backtracks. Consider N-Queens problem, suppose two queens are placed at positions (i, j) and (k, l). how to verify that two queens are in same diagonal.

1. **Solution Space**: A solution space is the set of all potential solutions for a problem¹. In the context of linear algebra, a solution space is the vector space containing all solutions to a given system¹. It follows the properties of vector spaces, so if vectors $$\vec{x}_1$$ and $$\vec{x}_2$$ are solutions to $$A\vec{x} = \vec{b}$$, then $$k_1\vec{x}_1 + k_2\vec{x}_2$$ is a solution for any values of $$k_1,k_2$$¹.

2. **E-node**: In the context of branch and bound algorithms, an E-node is a live node whose children are currently being explored⁵⁶. In other words, an E-node is a node currently being expanded⁶. All children of an E-node in a state space tree are produced before any live node gets converted into an E-node⁵.

3. **Modeling all combinations of N switches as a binary tree**: For a set of N switches, each of which can be 'on' or 'off', you can represent each possible combination with an n-tuple of 0's and 1's, where 1 represents the switch being on and 0 represents the switch being off. This can be modeled as a binary tree, where each node represents a switch state (0 or 1), and each level of the tree represents a switch. The root of the tree represents the first switch, the children of the root represent the second switch, and so on. The leaf nodes of the tree represent all possible combinations of the switches. Backtracking can be used to traverse this tree to find a specific combination.

4. **Verifying two queens are in the same diagonal in N-Queens problem**: In the N-Queens problem, two queens are placed at positions (i, j) and (k, l). They are on the same diagonal if and only if the absolute difference between their row positions equals the absolute difference between their column positions. In other words, if $$|i - k| = |j - l|$$, then the two queens are on the same diagonal¹⁸²³.

Source: Conversation with Bing, 25/1/2024
1. Solution space - Linear algebra | Elevri. https://www.elevri.com/courses/linear-algebra/solution-space.
2. Data Structures and Algorithms Tutorial - GeeksforGeeks. https://www.geeksforgeeks.org/introduction-to-branch-and-bound-data-structures-and-algorithms-tutorial/.
3. UNIT 4 - G PULLAIAH COLLEGE OF ENGINEERING & TECHNOLOGY. http://www.gpcet.ac.in/wp-content/uploads/2018/03/DAA-Notes_0-125-143.pdf.
4. N Queens Problems - javatpoint. https://www.javatpoint.com/n-queens-problems.
5. c++ - How do you test for diagonal in n-queens? - Stack Overflow. https://stackoverflow.com/questions/19524155/how-do-you-test-for-diagonal-in-n-queens.
6. Solution Space - Linear Algebra - Mathematics Stack Exchange. https://math.stackexchange.com/questions/1294949/solution-space-linear-algebra.
7. What is Solution Space | IGI Global. https://www.igi-global.com/dictionary/present-state-of-swarm-intelligence-and-future-directions/41383.
8. Problem space vs solution space | Customers | Teams | Examples. https://userstorymap.io/problem-space-vs-solution-space/.
9. Node (networking) - Wikipedia. https://en.wikipedia.org/wiki/Node_%28networking%29.
10. NODE Definition & Usage Examples | Dictionary.com. https://www.dictionary.com/browse/node.
11. Node (circuits) - Wikipedia. https://en.wikipedia.org/wiki/Node_%28circuits%29.
12. Backtracking Algorithms - GeeksforGeeks. https://www.geeksforgeeks.org/backtracking-algorithms/.
13. How is Backtracking done using recusrion in Binary Tree. https://stackoverflow.com/questions/23059127/how-is-backtracking-done-using-recusrion-in-binary-tree.
14. DFS traversal of a Tree - GeeksforGeeks. https://www.geeksforgeeks.org/dfs-traversal-of-a-tree-using-recursion/.
15. Backtracking :: AlgoTree. https://algotree.org/algorithms/backtracking/.
16. Generating all possible topologies in a full binary tree having n nodes .... https://stackoverflow.com/questions/18654085/generating-all-possible-topologies-in-a-full-binary-tree-having-n-nodes.
17. How many possible combinations of numbers make the same binary tree. https://stackoverflow.com/questions/28412298/how-many-possible-combinations-of-numbers-make-the-same-binary-tree.
18. Print all possible N-nodes Full Binary Trees - GeeksforGeeks. https://www.geeksforgeeks.org/print-all-possible-n-nodes-full-binary-trees/.
19. N Queen Problem - GeeksforGeeks. https://www.geeksforgeeks.org/n-queen-problem-backtracking-3/.
20. The n -queens completion problem - Springer. https://link.springer.com/article/10.1007/s40687-022-00335-1.
21. N Queen Problem - Scaler Topics. https://www.scaler.com/topics/n-queen-problem/.
22. Need Help With N Queens Program ( checking diagonals ). https://stackoverflow.com/questions/3209165/need-help-with-n-queens-program-checking-diagonals.
23. python - checking for diagonals on N-queens - Stack Overflow. https://stackoverflow.com/questions/36298512/checking-for-diagonals-on-n-queens.
