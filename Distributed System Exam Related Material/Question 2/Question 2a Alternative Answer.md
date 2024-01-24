## Define fault tolerance. Explain how fault tolerance is ensured in distributed system. What are the different fault tolerance techniques?

**Fault Tolerance:**

Fault tolerance is the ability of a system to maintain proper operation in the event of failures or faults in one or more of its components¹. If its operating quality decreases at all, the decrease is proportional to the severity of the failure, as compared to a naively designed system, in which even a small failure can lead to total breakdown¹.

**Ensuring Fault Tolerance in Distributed Systems:**

Fault tolerance in distributed systems is achieved through various strategies²⁸:

1. **Redundancy:** This involves keeping a backup plan for hardware devices such as memory, CPUs, communication links, and I/O devices⁷. In software fault tolerance, specific programs are included to deal with faults⁷.
2. **Standbys:** A standby is a redundant set of functionality or data waiting on standby that may be swapped to replace another failing instance⁶.
3. **Feature Flags:** These are used to hide, enable or disable features during runtime. They provide the ability to turn features on and off without deploying new code⁶.
4. **Asynchrony:** This involves processes running independently of each other, which can help prevent a single point of failure from bringing down the entire system⁶.

**Different Fault Tolerance Techniques:**

1. **Hardware Fault Tolerance:** This involves keeping a backup plan for hardware devices such as memory, CPUs, communication links, and I/O devices².
2. **Software Fault Tolerance:** This is a type of fault tolerance where dedicated software is used in order to deal with faults².
3. **System-Level Fault Tolerance:** This involves techniques that ensure the system as a whole can tolerate faults and continue to function².
4. **N-version Programming:** N versions of software are developed by N individuals or groups of developers. All the redundant copies are run concurrently and the result obtained is different from each processing⁵.
5. **Recovery Blocks:** Redundant copies are generated using different algorithms only. All the redundant copies are not run concurrently and these copies are run one by one⁵.
6. **Check-pointing and Rollback Recovery:** The system is tested each time when we perform some computation. This technique is basically useful when there is processor failure or data corruption⁵.

Source: Conversation with Bing, 25/1/2024
1. Fault tolerance - Wikipedia. https://en.wikipedia.org/wiki/Fault_tolerance.
2. Fault Tolerance in Distributed System - GeeksforGeeks. https://www.geeksforgeeks.org/fault-tolerance-in-distributed-system/.
3. Fault Tolerance in Distributed Systems: Strategies and Case Studies. https://dev.to/nekto0n/fault-tolerance-in-distributed-systems-strategies-and-case-studies-29d2.
4. Fault Tolerance Mechanisms in Distributed Systems. https://file.scirp.org/pdf/IJCNS_2015121715094011.pdf.
5. Distributed Systems Basics - Handling Failure: Fault Tolerance and .... https://katemats.com/blog/distributed-systems-basics-handling-failure-fault-tolerance-and-monitoring.
6. Fault-tolerance Techniques in Computer System - GeeksforGeeks. https://www.geeksforgeeks.org/fault-tolerance-techniques-in-computer-system/.
7. What is Fault Tolerance? - Definition from Techopedia. https://www.techopedia.com/definition/3362/fault-tolerance.
8. What Is Fault Tolerance? | Creating a Fault-tolerant System - Fortinet. https://www.fortinet.com/resources/cyberglossary/fault-tolerance.
9. Engineering a fault tolerant distributed system - Ably Realtime. https://ably.com/blog/engineering-dependability-and-fault-tolerance-in-a-distributed-system.
