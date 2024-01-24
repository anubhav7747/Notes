## Prove that Travelling Salesman Problem is NP-Complete class of problem.

The **Travelling Salesman Problem (TSP)** is a well-known problem in computer science. It is classified as an NP-Complete problem¹²³⁴. Here's a proof:

First, we need to prove that TSP belongs to NP. If we want to check a tour for credibility, we check that the tour contains each vertex once. Then we sum the total cost of the edges and finally we check if the cost is minimum. This can be completed in polynomial time thus TSP belongs to NP³⁴.

  ![tsp1](https://github.com/anubhav7747/Notes/assets/77168708/6638a263-17c3-4a2b-bee5-0cfca939157d)

To prove that TSP is NP-Complete, we need to show that every problem in NP reduces to TSP, i.e., TSP is NP-Hard². We can do this by reducing a known NP-Hard problem to TSP. A common choice is the Hamiltonian Cycle problem².

Given a graph G = (V, E) as input for the Hamiltonian Cycle problem, we can convert it to a TSP instance consisting of a graph G' = (V', E') and a maximum cost, K². We construct G' as follows:

1. For all the edges e belonging to E, add the cost of edge c(e)=1².
2. Connect the remaining edges, e' belonging to E', that are not present in the original graph G, each with a cost c(e')= 2².
3. Set K=n, where n is the number of vertices².

This reduction can be proved by the following two claims:

1. If the graph G contains a Hamiltonian Cycle, then the graph G' contains a TSP with cost, K=n².
2. If the graph G' contains a TSP with cost, K=n, then the graph G contains a Hamiltonian Cycle².

Therefore, any instance of the Hamiltonian Cycle problem can be reduced to an instance of the TSP. Thus, TSP is NP-Hard².

Since TSP is both in NP and NP-Hard, we can conclude that TSP is NP-Complete¹²³⁴..

Source: Conversation with Bing, 25/1/2024
1. Traveling Salesman Problem is NP-Complete - ProofWiki. https://proofwiki.org/wiki/Traveling_Salesman_Problem_is_NP-Complete.
2. Proof that traveling salesman problem is NP Hard - GeeksforGeeks. https://www.geeksforgeeks.org/proof-that-traveling-salesman-problem-is-np-hard/.
3. Chapter 10. https://www.csd.uoc.gr/~hy583/papers/ch11.pdf.
4. The traveling salesman problem is NP-complete - Physics Forums. https://www.physicsforums.com/threads/the-traveling-salesman-problem-is-np-complete.1030347/.
5. Module 35: NP-Complete proofs - INFLIBNET Centre. https://epgp.inflibnet.ac.in/epgpdata/uploads/epgp_content/S000007CS/P001064/M017978/ET/1480500093Q1-etext-module35.pdf.
6. en.wikipedia.org. https://en.wikipedia.org/wiki/Travelling_salesman_problem.
