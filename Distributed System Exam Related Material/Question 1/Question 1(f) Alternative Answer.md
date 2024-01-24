## Explain in detail about Fundamental models of distributed system.

The fundamental models of a distributed system provide a broad conceptual framework that helps in understanding the key aspects of distributed systems¹. These models are concerned with a more formal description of properties that are generally common in all architectural models¹. There are three fundamental models³⁵:

1. **Interaction Models:** These models deal with the interaction of processes such as performance and timing of events¹. They address challenges like unpredictable timing and rate of message transmission delivery between processes². Two flavors of interaction models exist²:
    * **Synchronous Model:** Boundaries are known for time to execute a step, message transmission, and clock drift rate². Timeouts are typically used to detect failures².
    * **Asynchronous Model:** No assumptions are made on process time, message transmission, or clock drift². Event ordering cannot be dependent on time².

2. **Failure Models:** These models specify the types of faults that can be exhibited by processes and communication channels¹⁴. They classify failures into different types²:
    * **Omission Failures:** These occur when a process halts (crashed) and will not execute any further². Communication failures occur when messages are "dropped" between the sender and receiver².
    * **Arbitrary (Byzantine) Failures:** These occur in the absence of process and communication omission failures, but the integrity of data or processing steps is in error and undetectable by other processes².

3. **Security Models:** These models deal with threats to processes and communication channels³⁵. They ensure that the system is secure from external threats and attacks¹.

Each of these models plays a crucial role in the design and operation of distributed systems, ensuring efficient interaction, robustness against failures, and security against threats¹. The choice of models depends on the specific requirements and constraints of the distributed system¹.

Source: Conversation with Bing, 25/1/2024
1. Distributed Computing System Models - GeeksforGeeks. https://www.geeksforgeeks.org/distributed-computing-system-models/.
2. System models for distributed systems - Universitetet i Oslo. https://www.uio.no/studier/emner/matnat/ifi/INF5040/h14/lecture-notes/system-modells.pdf.
3. System models for distributed systems - Universitetet i Oslo. https://www.uio.no/studier/emner/matnat/ifi/INF5040/h11/lectures/SystemModels.pdf.
4. Fundamental Distributed System Models. https://www.se.rit.edu/~se442/slides/class/03-SystemModels-Fundamental.pdf.
5. Fundamental Distributed System Models. https://www.se.rit.edu/~swen-342/slides/03-SystemModels-Fundamental.pdf.
