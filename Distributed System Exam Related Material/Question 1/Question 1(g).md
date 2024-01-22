## What are Vector Clocks? Explain with the help of implementation rule of Vector Clocks, how they are incremented. What are the advantages of Vector Clocks over Lamport Clock?
Vector Clocks are a type of logical clock used in distributed systems to generate a partial ordering of events and detect causality violations¹. They expand on scalar time to provide a causally consistent view of the distributed system¹.

Here's how the Vector Clock algorithm works:

1. **Initialization**: Initially, all the clocks are set to zero¹.
2. **Internal Event**: Every time an internal event occurs in a process, the value of the process's logical clock in the vector is incremented by 1¹.
3. **Sending a Message**: Every time a process sends a message, the value of the process's logical clock in the vector is incremented by 1¹.
4. **Receiving a Message**: Every time a process receives a message, the value of the process's logical clock in the vector is incremented by 1. Moreover, each element is updated by taking the maximum of the value in its own vector clock and the value in the vector in the received message¹.

Vector Clocks have several advantages over Lamport Clocks:

1. **Causality Detection**: Vector Clocks can determine if any two arbitrarily selected events are causally dependent or concurrent⁶. Lamport Clocks cannot do this⁶.
2. **Efficient Identification of Concurrent Events**: Compared to Lamport’s clock, Vector Clocks can identify concurrent events more efficiently⁷.
3. **Partial Ordering of Events**: Vector Clocks provide a partial causal ordering of events, which is useful in understanding the sequence of events in a distributed system¹.

However, one drawback of Vector Clocks is that they require overhead proportional to the number of nodes, making them less compact than Lamport Clocks⁶.

Source: Conversation with Bing, 23/1/2024
1. Vector Clocks in Distributed Systems - GeeksforGeeks. https://www.geeksforgeeks.org/vector-clocks-in-distributed-systems/.
2. Difference between Lamport timestamps and Vector clocks. https://cs.stackexchange.com/questions/101496/difference-between-lamport-timestamps-and-vector-clocks.
3. Vector Clocks. Like Lamport’s Clock, Vector Clock is… | by Sruthi Sree .... https://medium.com/big-data-processing/vector-clocks-182007060193.
4. Vector clock - Wikipedia. https://en.wikipedia.org/wiki/Vector_clock.
5. Vector Clocks: Keeping time in check - Distributed Computing Musings. https://distributed-computing-musings.com/2022/05/vector-clocks-keeping-time-in-check/.
6. Distributed Systems: Physical, Logical, and Vector Clocks. https://levelup.gitconnected.com/distributed-systems-physical-logical-and-vector-clocks-7ca989f5f780.
7. Vector Clock & Applications. Overview | by Vaibhav Kumar - Medium. https://flurryhead.medium.com/vector-clock-applications-965677624b94.
8. concurrency - Logical Time, Lamport Timestamps and Vector Clocks in .... https://stackoverflow.com/questions/74830259/logical-time-lamport-timestamps-and-vector-clocks-in-distributed-systems.
9. undefined. https://cse.buffalo.edu/tech-reports/2014-04.pdf.
