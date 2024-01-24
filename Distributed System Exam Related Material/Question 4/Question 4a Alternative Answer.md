## Discuss how the efficiency of distributed shared memory system depends on the size of granularity and protocol used for page replacement.

**Granularity and Efficiency:**

Granularity refers to the size of the shared memory unit⁶. It can be a byte, a word, a page, or another type of unit³. The choice of granularity is a major issue in distributed shared memory (DSM) systems because it deals with the amount of computation done between synchronization or communication points³.

- **Small Granularity:** If the granularity is small, then the overhead of sending many small update-messages can reduce efficiency⁹. However, it can lead to less false sharing⁸.
- **Large Granularity:** If the granularity is large, it can provide more locality, less communication overheads, but more contention and more false sharing⁸. Large granularity means data is moved in large blocks, which can reduce network traffic¹.

**Page Replacement Protocol and Efficiency:**

The protocol used for page replacement also plays a crucial role in the efficiency of a DSM system[^10^]. When a process addresses a memory location that is not mapped into the current physical memory, a page fault occurs¹². The operating system then locates the referred page, transfers its content over the network, and maps it to physical memory¹². At that point, the application can continue¹².

- **Efficient Page Replacement:** An efficient page replacement strategy is vital in the design of a DSM system⁶. If the local memory of a node is full, a cache miss at the node implies not just a retrieval of the accessed data block from a remote node but also a replacement⁶. A data block of the local memory should be replaced by the new data block⁶.
- **Avoiding Thrashing:** The DSM system should use an approach to avoid a situation generally known as thrashing⁶. In a DSM system, data blocks move between nodes on demand. If two nodes compete for write access to a single data item, the data relating data block might be moved back and forth at such a high rate that no real work can get done⁶.

In conclusion, both the size of granularity and the protocol used for page replacement significantly impact the efficiency of a distributed shared memory system⁶⁸[^10^]¹².

Source: Conversation with Bing, 25/1/2024
1. Design and Implementation Issue of Distributed Shared Memory. https://www.geeksforgeeks.org/design-and-implementation-issue-of-distributed-shared-memory/.
2. Consistency Issues in Distributed Shared Memory Systems. https://crystal.uta.edu/~kumar/cse6306/papers/Chingwen.pdf.
3. 16 Distributed Shared Memory - KIT. https://os.itec.kit.edu/downloads/DS16_DSM1.pdf.
4. COP 5611 L15c - Florida State University. http://websrv.cs.fsu.edu/~xyuan/cop5611/lecture19.html.
5. What is Distributed shared memory and its advantages. https://www.geeksforgeeks.org/what-is-distributed-shared-memory-and-its-advantages/.
6. PAGE BASED DISTRIBUTED SHARED MEMORY - ijirt. https://ijirt.org/master/publishedpaper/IJIRT101270_PAPER.pdf.
7. DISTRIBUTED SYSTEMS PRINCIPLES AND PARADIGMS - Indian Institute of .... https://profile.iiita.ac.in/bibhas.ghoshal/lecture_slides/distributed/DSTanenbaumsolutions.pdf.
8. PLUS: The Distributed Shared Memory - GeeksforGeeks. https://www.geeksforgeeks.org/plus-the-distributed-shared-memory/.
9. Distributed Shared Memory and its advantages and disadvantages. https://binfintech.com/introduction-to-distributed-shared-memory/.
10. Shared Memory And Distributed Shared Memory Systems: A Survey. https://web.engr.oregonstate.edu/~benl/Publications/Book_Chapters/Advances_in_Computers_DSM00.pdf.
11. Distributed Shared Memory | part of Distributed Operating Systems .... https://ieeexplore.ieee.org/document/5487828/.
12. CHAPTER 7: DISTRIBUTED SHARED MEMORY - Computer & Information Science .... https://www.cise.ufl.edu/~nemo/cop5615/chow/ch7.pdf.
13. Overview Distributed Shared Memory - University at Buffalo. https://cse.buffalo.edu/~stevko/courses/cse486/spring19/lectures/30-dsm.pdf.
14. Distributed Shared Memory - Rutgers University. https://people.cs.rutgers.edu/~pxk/rutgers/notes/content/09-dsm.pdf.
15. undefined. https://ieeexplore.ieee.org/servlet/opac?punumber=5487818.
