## What is the problem of distributed deadlock detection? What are the differences in Centralized, Distributed and Hierarchical control organization for distributed deadlock detection? What are advantages of Distributed Control Organization over Centralized Control Organization for distributed deadlock detection?

**Problem of Distributed Deadlock Detection:**

In a distributed system, deadlock can neither be prevented nor avoided due to the vastness and complexity of the system⁶. Therefore, only deadlock detection can be implemented². Detecting deadlocks in distributed systems involves addressing two fundamental issues⁶:
1. **Wait-For Graph (WFG) Maintenance:** Keeping track of the resources each process is holding and waiting for⁶.
2. **Searching the WFG:** Looking for cycles in the graph, which indicate a deadlock⁶.

**Differences in Control Organizations for Distributed Deadlock Detection:**

1. **Centralized Approach:** One central site sets up a global WFG and searches for cycles¹. All decisions are made by the central control node¹. The main advantage is the simplicity of the algorithms¹. However, it suffers from single-point failure and can cause a communication bottleneck due to all the WFG information messages¹².

2. **Distributed Approach:** Different nodes work together to detect deadlocks¹. All sites have an equal amount of information and bear equal responsibility for the final decision in detecting deadlock¹. The global WFG is spread across the sites¹. The main advantage is that there is no central point of failure and the speed of deadlock detection increases². However, resolution may be difficult as not all sites may be aware of the processes involved in the deadlock¹.

3. **Hierarchical Approach:** The sites (nodes) are logically connected in a hierarchical structure (such as a tree). A site can detect deadlock in its descendants¹. This approach combines the advantages of both the centralized and distributed approaches¹².

**Advantages of Distributed Control Organization over Centralized Control Organization:**

The distributed approach has several advantages over the centralized approach:
1. **No Single Point of Failure:** The whole system is not dependent on one node. If one node fails, it does not cause the whole system to crash¹².
2. **Workload Distribution:** The workload is equally divided among all nodes, avoiding the communication bottleneck that can occur in the centralized approach¹².
3. **Increased Speed:** The speed of deadlock detection increases as multiple nodes can initiate the detection at the same time¹².
4. **On-Demand Detection:** The algorithm is only initiated when processes feel there might be a problem, not run periodically¹.

Source: Conversation with Bing, 25/1/2024
1. Deadlock Detection in Distributed Systems - javatpoint. https://www.javatpoint.com/deadlock-detection-in-distributed-systems.
2. Deadlock detection in Distributed systems - GeeksforGeeks. https://www.geeksforgeeks.org/deadlock-detection-in-distributed-systems/.
3. Control Organization for Distributed Deadlock Detection Algorithms. https://www.cs.colostate.edu/~cs551/CourseNotes/Deadlock/DDAlgControl.html.
4. Hierarchical Deadlock Detection in Distributed System. https://www.geeksforgeeks.org/hierarchical-deadlock-detection-in-distributed-system/.
5. Deadlock detection in distributed systems - IEEE Xplore. https://ieeexplore.ieee.org/abstract/document/43525/.
6. Distributed Deadlocks - Rutgers University. https://www.cs.rutgers.edu/~pxk/rutgers/notes/content/deadlocks-slides.pdf.
7. Deadlock Detection Algorithm in Operating System. https://www.geeksforgeeks.org/deadlock-detection-algorithm-in-operating-system/.
8. An Analysis and Improvement of Probe-Based Algorithm for Distributed .... http://www.lnse.org/vol3/205-X0012.pdf.
9. Deadlock Detection in Distributed Systems - University of Illinois Chicago. https://www.cs.uic.edu/~ajayk/Chapter10.pdf.
