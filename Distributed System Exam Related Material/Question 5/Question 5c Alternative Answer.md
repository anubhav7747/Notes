## What is a transaction? What are the two main factors that threaten the atomicity of transaction? Describe how atomicity is ensured for a transaction in both commit and abort.

**Transaction:**

A transaction is a single logical unit of work that accesses and possibly modifies the contents of a database⁵. In distributed systems, a transaction is defined as a group of operations that are to be performed across more than one database or data repository⁹. The operations are performed by multiple nodes that are connected to a single network⁹. The distributed transaction ensures ACID (Atomicity, Consistency, Isolation, Durability) properties and data integrity⁹.

**Factors Threatening Atomicity:**

1. **Partial Execution:** Atomicity can be threatened if a transaction is partially executed. This means that if a transaction fails at any point during its execution, some operations may have been executed while others have not¹.
2. **System Failures:** System failures such as power outages, errors, or system crashes can also threaten atomicity. If a system failure occurs during the execution of a transaction, it may result in only a portion of the transaction being executed².

**Ensuring Atomicity:**

Atomicity is ensured through the use of commit and abort operations⁵:

1. **Commit:** If a transaction commits, all changes made by the transaction are permanently saved to the database⁵. For example, in the Shadow Copy Scheme, a transaction is said to be committed only if the updated database pointer is written on disk¹.
2. **Abort:** If a transaction aborts, all changes made by the transaction are discarded, and the database remains in its original state before the transaction started⁵. In the Shadow Copy Scheme, if a transaction fails at any time before the database pointer is updated, the old content of the database is not affected. The abort can be done by deleting the new copy of the database¹.

Source: Conversation with Bing, 25/1/2024
1. ACID Properties in DBMS - GeeksforGeeks. https://www.geeksforgeeks.org/acid-properties-in-dbms/.
2. What is a Distributed Transaction? - GeeksforGeeks. https://www.geeksforgeeks.org/what-is-a-distributed-transaction/.
3. How to Implement Atomicity and Durability in Transactions in DBMS .... https://www.geeksforgeeks.org/how-to-implement-atomicity-and-durability-in-transactions-in-dbms/.
4. Atomicity in Database Management Systems - Medium. https://medium.com/@siddharth.sabron/atomicity-in-database-management-systems-c850526e0df2.
5. Atomicity (database systems) - Wikipedia. https://en.wikipedia.org/wiki/Atomicity_%28database_systems%29.
6. Data - (Transaction|Action) Atomicity - Datacadamia. https://datacadamia.com/data/property/atomicity.
7. Atomic Commit Protocol in Distributed System - GeeksforGeeks. https://www.geeksforgeeks.org/atomic-commit-protocol-in-distributed-system/.
8. Transactions – Recovery - IIT Bombay. https://www.cse.iitb.ac.in/~cs317/Resources/lectures/Transactions-Recovery.pdf.
9. Lecture 04 Argus, Atomicity, and Two Phase Commit · CS6963. https://users.cs.utah.edu/~stutsman/cs6963/lecture/f15-04-argus/.
10. Distributed transactions: What, why, and how to build a distributed .... https://www.cockroachlabs.com/blog/distributed-transactions-what-why-and-how-to-build-a-distributed-transactional-application/.
11. Distributed transaction - Wikipedia. https://en.wikipedia.org/wiki/Distributed_transaction.
12. Distributed Transactions: The basics and overview. https://blog.sofwancoder.com/distributed-transactions-overview.
