## What are agreement protocols? What are Byzantine agreement problem, the Consensus problem and Interactive consistency problem?

**Agreement Protocols:**

Agreement protocols are a fundamental tool for ensuring coordination and consistency in a distributed system¹. In distributed systems, many nodes must collaborate to achieve a similar goal, yet due to network delays and faults, separate nodes may have different perspectives of the system state¹. An agreement protocol’s purpose is to ensure that all nodes in the system finally reach the same decision, even if some nodes fail or act maliciously¹. There are various forms of agreement protocols, but the consensus protocol is the most well-known and commonly utilized¹.

**Byzantine Agreement Problem:**

The Byzantine agreement problem necessitates that a single value be agreed upon by all non-faulty processors, with the initial value chosen by an arbitrarily chosen processor¹. The source processor broadcasts this initial value to all other processors, and the solution must assure agreement on the same value among all non-faulty processors¹. If the source processor is not faulty, the agreed-upon value must match the source’s initial value¹.

**Consensus Problem:**

Consensus refers to an agreement on any subject by a group of participants¹¹. In a distributed system, nodes are distributed across the network. Some of these nodes might get failed (crash fault) or start behaving abnormally (Byzantine Fault)¹¹. In such a scenario, it becomes difficult to come to a common decision¹¹. The task is to make all the non-faulty processes agree on some value (s) even in the presence of the faulty processes¹¹.

**Interactive Consistency Problem:**

The Interactive consistency problem necessitates the agreement of all non-faulty processors on a set of common values, each with its unique initial value¹. Each CPU broadcasts its initial value to all other processors, and the solution must assure agreement on the same vector across all non-faulty processes¹.

Source: Conversation with Bing, 25/1/2024
1. Agreement Protocol in Distributed Systems - GeeksforGeeks. https://www.geeksforgeeks.org/agreement-protocol-in-distributed-systems/.
2. Consensus Problem of Distributed Systems - GeeksforGeeks. https://www.geeksforgeeks.org/consensus-problem-of-distributed-systems/.
3. Ch. 9 Agreement Protocols - Indian Institute of Information Technology .... https://profile.iiita.ac.in/bibhas.ghoshal/lecture_slides/distributed/ch9.pdf.
4. Distributed Consensus in Distributed System - Online Tutorials Library. https://www.tutorialspoint.com/distributed-consensus-in-distributed-system.
5. Distributed Consensus Protocols and Algorithms. https://cybersecurity.seas.wustl.edu/ning/paper/consensus19.pdf.
6. Interactive Consistency in practical, mostly-asynchronous systems. https://arxiv.org/pdf/1410.7256.pdf.
7. Interactive Consistency in practical, mostly-asynchronous systems. https://arxiv.org/abs/1410.7256.
8. Interactive Consistency in practical, mostly-asynchronous systems. https://arxiv.org/pdf/1410.7256v4.
9. Byzantine Generals Problem in Blockchain - GeeksforGeeks. https://www.geeksforgeeks.org/byzantine-generals-problem-in-blockchain/.
10. Byzantine Agreement Problem Geeksforgeeks – Learning Dream Land. https://learningdreamland.in/byzantine-agreement-problem-geeksforgeeks/.
11. Byzantine fault - Wikipedia. https://en.wikipedia.org/wiki/Byzantine_fault.
12. Consensus Algorithms in Distributed Systems - Baeldung. https://www.baeldung.com/cs/consensus-algorithms-distributed-systems.
13. Consensus (computer science) - Wikipedia. https://en.wikipedia.org/wiki/Consensus_%28computer_science%29.
14. Consensus - Rutgers University. https://www.cs.rutgers.edu/%7Epxk/417/notes/content/consensus.html.
