## Why is scalability an important feature in the design of distributed system? Discuss some of the guiding principles for designing a scalable distributed system.
Scalability is a critical feature in the design of distributed systems for several reasons¹⁶⁷⁸⁹:

1. **Accommodate Growth**: As the number of users and resources grows over time, the system should be capable of extending to handle the increased load¹.
2. **Performance and Efficiency**: The system must maintain its performance and efficiency as it scales. This means that the system and application software should not need to change significantly as the scale of the system increases¹.
3. **Adaptability**: Scalability refers to a system's ability to adapt to changing workloads by altering hardware resources such as processors, memory, and hard disk space, as well as by altering the scheduling mechanism and level of parallelism¹.
4. **Responsiveness**: The system should respond to the user in the same manner as it was responding before scaling¹.

Guiding principles for designing a scalable distributed system include¹²:

1. **Incremental Scalability**: The system should be designed to scale incrementally, allowing for the addition of resources as needed².
2. **Symmetry**: All nodes in the system should be equal, and there should be no central control³.
3. **Decentralization**: The system should be decentralized to avoid bottlenecks and single points of failure².
4. **Work Distribution**: The system should be designed to distribute work evenly across all nodes³.
5. **Size Scalability**: The system should be able to increase in size without sacrificing performance or efficiency¹.
6. **Geographical Scalability**: The addition of new nodes in a physical space should not affect the communication time between the nodes¹.
7. **Administrative Scalability**: The management of new nodes being added to the system should not require significant effort¹.

These principles help ensure that the system can handle increased loads efficiently and effectively, providing a seamless experience for users as the system grows¹²³.

Source: Conversation with Bing, 23/1/2024
1. What is Scalable System in Distributed System? - GeeksforGeeks. https://www.geeksforgeeks.org/what-is-scalable-system-in-distributed-system/.
2. What is Scalability and How to achieve it – Learn System Design. https://www.geeksforgeeks.org/what-is-scalability-and-how-to-achieve-it-learn-system-design/.
3. Three dimensions of distributed system scalability design. https://medium.com/@Pointnity_Network/three-dimensions-of-distributed-system-scalability-design-8e0319163c8d.
4. What are distributed systems? A quick introduction - Educative. https://www.educative.io/blog/distributed-systems-considerations-tradeoffs.
5. Understanding Technical Scalability in Distributed Systems. https://dev.to/er_dward/understanding-technical-scalability-in-distributed-systems-2jop.
6. Design Principles of Scalable, Distributed Systems - Medium. https://medium.com/@tvganesh_85/design-principles-of-scalable-distributed-systems-bbd477904b6b.
7. Design principles of scalable, distributed systems | PPT - SlideShare. https://www.slideshare.net/tinniamvganesh/design-principles-of-scalable-distributed-systems.
8. Grokking Scalability in System Design: How I Learned the Techniques .... https://www.designgurus.io/blog/grokking-system-design-scalability.
9. Free Guide: Scalability Design Principles - elastisys. https://elastisys.com/scalability-design-principles/.
10. undefined. http://gigadom.wordpress.com.

