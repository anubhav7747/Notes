## What do you mean by problem of Mutual Exclusion in distributed system? What are the requirements of a good mutual exclusion algorithm? Explain the performance matrices to judge the performance of distributed mutual exclusion algorithm.

**Mutual Exclusion in Distributed Systems:**

Mutual exclusion is a concurrency control property introduced to prevent race conditions. It ensures that only one process is allowed to execute the critical section at any given instance of time¹. In distributed systems, we neither have shared memory nor a common physical clock, therefore we cannot solve the mutual exclusion problem using shared variables¹. To eliminate the mutual exclusion problem in distributed systems, an approach based on message passing is used¹.

**Requirements of a Good Mutual Exclusion Algorithm:**

1. **No Deadlock:** Two or more sites should not endlessly wait for any message that will never arrive¹.
2. **No Starvation:** Every site who wants to execute the critical section should get an opportunity to execute it in finite time¹.
3. **Fairness:** Each site should get a fair chance to execute the critical section. Any request to execute the critical section must be executed in the order they are made¹.
4. **Fault Tolerance:** In case of failure, it should be able to recognize it by itself in order to continue functioning without any disruption¹.

**Performance Metrics for Distributed Mutual Exclusion Algorithms:**

1. **Response Time:** The interval of time when a request waits for the end of its critical section execution after its solicitation messages have been delivered⁵.
2. **Synchronization Delay:** The time required for the next process to enter the critical section after a process leaves the critical section⁵.
3. **Message Complexity:** The number of messages needed to execute each critical section by the process⁵.
4. **Throughput:** Throughput is the amount at which the system executes requests for the critical section⁵.

Source: Conversation with Bing, 25/1/2024
1. Mutual exclusion in distributed system - GeeksforGeeks. https://www.geeksforgeeks.org/mutual-exclusion-in-distributed-system/.
2. Performance Metrics For Mutual Exclusion Algorithm. https://www.geeksforgeeks.org/performance-metrics-for-mutual-exclusion-algorithm/.
3. Mutual exclusion in a distributed system - Online Tutorials Library. https://www.tutorialspoint.com/mutual-exclusion-in-a-distributed-system.
4. Distributed mutual exclusion algorithms (Chapter 9) - Distributed Computing. https://www.cambridge.org/core/books/distributed-computing/distributed-mutual-exclusion-algorithms/F819BE611EE98FD80D4DF2A6237F79DA.
5. Chapter 9: Distributed Mutual Exclusion Algorithms. https://www.cs.uic.edu/~ajayk/Chapter9.pdf.
6. Performance metrics for mutual exclusion Algorithm. https://www.tutorialspoint.com/performance-metrics-for-mutual-exclusion-algorithm.
7. Comparison of Algorithms for Distributed Mutual Exclusion through .... https://arxiv.org/abs/2211.01747v2.
8. Methodology for Simulation-based Comparison of Algorithms for .... https://arxiv.org/pdf/2211.01747.pdf.
9. 3.1. DISTRIBUTED MUTUAL EXCLUSION ALGORITHMS: INTRODUCTION. https://www.jeppiaarinstitute.org/pdf/lectures/143.pdf.
10. Distributed Mutual Exclusion - Indian Institute of Information .... https://profile.iiita.ac.in/bibhas.ghoshal/lecture_slides/distributed/MutualExclusion.pdf.
