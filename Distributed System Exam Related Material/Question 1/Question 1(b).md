## What do you mean by Global state of the distributed system? Also explain the main features of consistent global state.
The global state of a distributed system is a collection of the local states of all the processes and the channels in the system¹⁴. It represents a snapshot of the entire system at a given point in time¹⁴.

A consistent global state has the following main features¹⁵⁶:

1. **Local States**: It comprises the local state of each process at the time the cut event happens¹.
2. **Messages in Transit**: It includes the set of all messages that have been sent but not yet received¹.
3. **Consistency**: A global state computed along a consistent cut is correct¹. This means that every message that is received was previously sent⁵.
4. **Concurrent Local States**: In the causal domain, a global state is a set of local states which are all concurrent with each other⁶. By concurrent, we mean that no two states have a cause and effect relationship with each other⁶.

These features ensure that the global state provides a meaningful and accurate snapshot of the system, which is crucial for various tasks such as debugging, checkpointing, garbage collection, deadlock detection, and termination detection¹.

Source: Conversation with Bing, 23/1/2024
1. Distributed Computing Concepts - Global State in Distributed Systems. https://ics.uci.edu/~cs230/lectures20/distrsyslectureset3-win20.pdf.
2. GLOBAL STATE AND SNAPSHOT RECORDING ALGORITHMS - RCET. https://rcet.org.in/uploads/academics/rohini_38829910137.pdf.
3. Consistent Global States - SJSU. http://www.cs.sjsu.edu/~stamp/CS249/projects/Chapter4.pdf.
4. GLOBAL STATE - Springer. https://link.springer.com/content/pdf/10.1007/978-1-4613-1321-2_4.pdf.
5. Chandy–Lamport’s global state recording algorithm. https://www.geeksforgeeks.org/chandy-lamports-global-state-recording-algorithm/.
6. Chapter 4: Global State and Snapshot Recording Algorithms. https://www.cs.uic.edu/~ajayk/Chapter4.pdf.
7. Distributed Computing Concepts - Global State in Distributed Systems. https://bing.com/search?q=main+features+of+consistent+global+state.

