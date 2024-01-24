## What are commit-protocols? Explain how Two-Phase commit protocol responds to failure of participating site and failure of coordinator.

**Commit Protocols:**

Commit protocols are used to ensure atomicity across sites in a distributed system³. A transaction that executes at multiple sites must either be committed at all the sites, or aborted at all the sites³. It's not acceptable to have a transaction committed at one site and aborted at another³. The most straightforward and popular commit method is the Two-Phase Commit Protocol (2PC)¹.

**Two-Phase Commit Protocol (2PC):**

The 2PC protocol reduces the vulnerability of one-phase commit protocols¹. It involves two phases¹:

1. **Prepare Phase:** After each site has locally completed its transaction, it sends a "DONE" message to the coordinator. When the coordinator has received "DONE" messages from all sites, it sends a "Prepare" message to the sites. The sites vote on whether they still want to commit or not¹.
2. **Commit/Abort Phase:** After the coordinator has received "Ready" messages from all the sites, it sends a "Global Commit" message to the sites. The sites apply the transaction and send a "Commit ACK" message to the coordinator¹.

**Response to Failures:**

* **Failure of Participating Site:** If the coordinator detects that a site has crashed, it takes the following actions⁶:
    * If the site has failed before responding with a "ready T" message to the coordinator, the coordinator assumes that the site has responded with an "abort T" message⁶.
    * If the site has failed after sending a "ready T" message to the coordinator, the coordinator will ignore the site failure and will execute the rest of the commit protocol in the usual manner⁶.
    * When the failed site recovers from failure, the site will examine its log record to know the destiny of the transaction⁶.

* **Failure of Coordinator:** If the coordinator fails in the midst of the execution of the transaction in 2PC, then participating sites must decide the destiny of the transaction⁶. In certain cases, participating sites can't decide whether to commit or abort the transaction and therefore these sites must wait for the recovery of the failed coordinator⁶.

Source: Conversation with Bing, 25/1/2024
1. CS60002: Distributed Systems - IIT Kgp. https://cse.iitkgp.ac.in/~pallab/dist_sys/Lec-11-CommitProtocols.pdf.
2. COMMIT Protocol in DBMS - javatpoint. https://www.javatpoint.com/commit-protocol-in-dbms.
3. Recovery from failures in Two Phase Commit Protocol (Distributed .... https://www.geeksforgeeks.org/recovery-from-failures-in-two-phase-commit-protocol-distributed-transaction/.
4. Distributed DBMS - Commit Protocols - Online Tutorials Library. https://www.tutorialspoint.com/distributed_dbms/distributed_dbms_commit_protocols.htm.
5. Nonblocking Commit Protocols* - Department of Computer Science. https://www.cs.cornell.edu/courses/cs614/2004sp/papers/Ske81.pdf.
6. Distributed DBMS - Failure & Commit - Online Tutorials Library. https://www.tutorialspoint.com/distributed_dbms/distributed_dbms_failure_commit.htm.
7. Two Phase Commit blocking on coordinator failure. https://stackoverflow.com/questions/63121233/two-phase-commit-blocking-on-coordinator-failure.
8. distributed systems - Why is Two-Phase Commit (2PC) blocking .... https://cs.stackexchange.com/questions/76192/why-is-two-phase-commit-2pc-blocking.
9. Two-phase commit protocol - Wikipedia. https://en.wikipedia.org/wiki/Two-phase_commit_protocol.
10. Two-Phase Commit - Martin Fowler. https://martinfowler.com/articles/patterns-of-distributed-systems/two-phase-commit.html.
11. Two Phase Commit Protocol (Distributed Transaction Management). https://www.geeksforgeeks.org/two-phase-commit-protocol-distributed-transaction-management/.
12. How the two-phase commit protocol handles failures - IBM. https://www.ibm.com/docs/en/informix-servers/12.10?topic=protocol-how-two-phase-commit-handles-failures.
