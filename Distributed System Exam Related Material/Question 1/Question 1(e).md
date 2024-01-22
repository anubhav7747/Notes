## What are the transparencies which can be observed in distributed system? List the basic transparencies which need to be supported by the distributed system.
In distributed systems, transparency is defined as the masking from the user and the application programmer regarding the separation of components, so that the whole system seems to be like a single entity rather than individual components¹. Here are the basic types of transparency that need to be supported by a distributed system:

1. **Access Transparency**: Allows the same operations to be used to access local and remote resources¹.

2. **Location Transparency**: Permits access to resources regardless of their physical or network location¹.

3. **Concurrency Transparency**: Permits many processes to run in parallel using shared resources without interfering with one another¹.

4. **Replication Transparency**: Ensures the existence of numerous instances of resources to improve reliability and performance without having to know about replication to the user¹.

5. **Failure Transparency**: Permits fault abstraction in the background, allowing users and application programs to execute tasks even when hardware and software components fail¹.

6. **Mobility Transparency**: Hides the movement of resources and processes within a system from users¹.

7. **Performance Transparency**: Allows the system to be reconfigured to improve performance as loads vary¹.

8. **Scaling Transparency**: Allows the system and applications to expand in scale without changes to the system structure or the application algorithms¹.

9. **Parallelism Transparency**: Allows multiple resources to be used in parallel to enhance performance¹.

These transparencies are crucial in distributed systems as they allow application programmers to focus on the design of their specific activity without worrying about the underlying complexities of the distributed system¹.

Source: Conversation with Bing, 23/1/2024
1. Types of Transparency in Distributed System - GeeksforGeeks. https://www.geeksforgeeks.org/types-of-transparency-in-distributed-system/.
2. Transparencies in DDBMS - GeeksforGeeks. https://www.geeksforgeeks.org/transparencies-in-ddbms/.
3. (PDF) Transparency in Distributed Systems - Academia.edu. https://www.academia.edu/31423717/Transparency_in_Distributed_Systems.
4. DDBMS - Distribution Transparency - Online Tutorials Library. https://www.tutorialspoint.com/distributed_dbms/distributed_dbms_distribution_transparency.htm.
