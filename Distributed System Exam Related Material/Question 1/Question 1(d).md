## What are Lamport's Logical Clocks? For Lamport clock system, prove that for any two events 'a' and 'b'; if a → b, then C(a) < C(b) but vice versa is not true.
Lamport's Logical Clocks, created by Leslie Lamport, are a method to determine the order of events in a distributed system¹. They provide a basis for the more advanced Vector Clock Algorithm¹. Due to the absence of a Global Clock in a Distributed Operating System, Lamport Logical Clocks are needed¹.

The algorithm for Lamport's Logical Clocks is based on the "happened before" relation (->), where 'a -> b' means 'a' happened before 'b'¹. The criteria for the logical clocks are:

- [C1]: If 'a' happened before 'b' within the same process, then Ci(a) < Ci(b)¹.
- [C2]: If 'a' happened before 'b' in different processes, then Ci(a) < Cj(b)¹.

The implementation rules are:

- [IR1]: If a -> b [‘a’ happened before ‘b’ within the same process] then, Ci(b) = Ci(a) + d¹.
- [IR2]: Cj = max (Cj, tm + d) [If there’s more number of processes, then tm = value of Ci(a), Cj = max value between Cj and tm + d]¹.

Now, let's prove that for any two events 'a' and 'b'; if a → b, then C(a) < C(b) but vice versa is not true.

- If a → b, then C(a) < C(b) is true because of the implementation rules of Lamport's Logical Clocks¹. If 'a' happens before 'b', then the clock value of 'a' will be less than 'b' in a particular process¹.

- However, the converse, if C(a) < C(b), then a → b, is not necessarily true⁵. This is because it is possible in the system of logical clocks that C(a) < C(b) when we do not have a partial ordering that guarantees the relation a → b⁵. Therefore, if C(a) < C(b), it does not imply that 'a' happened before 'b'⁵.

This limitation is addressed by Vector Clocks, which can determine if any two arbitrarily selected events are causally dependent or concurrent⁶.

Source: Conversation with Bing, 23/1/2024
1. Lamport's logical clock - GeeksforGeeks. https://www.geeksforgeeks.org/lamports-logical-clock/.
2. Why does the converse of the clock condition imply that any two .... https://cs.stackexchange.com/questions/131744/why-does-the-converse-of-the-clock-condition-imply-that-any-two-concurrent-event.
3. Lamport’s Clock limitations - The Renegade Coder. https://therenegadecoder.com/wp-content/uploads/2019/07/osu-cse-6431-distributed-mutual-exclusion-part-2.pdf.
4. Logical clock algorithms - Distributed Systems. https://distributedsystemsblog.com/docs/logical-clock-algorithms/.
5. Lamport timestamp - Wikipedia. https://en.wikipedia.org/wiki/Lamport_timestamp.
6. Educative Answers - Trusted Answers to Developer Questions. https://www.educative.io/answers/what-are-lamport-clocks.
7. Time, Clocks, and the Ordering of Events in a Distributed System. https://courses.cs.washington.edu/courses/csep552/13sp/lectures/2/logicalclocks.pdf.
8. LAMPORT AND VECTOR CLOCKS - University of California, San Diego. https://cseweb.ucsd.edu/classes/sp18/cse124-a/post/schedule/15-LogicalTime.pdf.


