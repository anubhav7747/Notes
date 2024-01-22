## Draw a schematic diagram of the distributed transaction management model. Explain each component in brief.
A distributed transaction management model is a group of operations performed across more than one database or data repository. These operations are performed by multiple nodes connected to a single network¹. The distributed transaction ensures ACID (Atomicity, Consistency, Isolation, Durability) properties and data integrity¹. 

Here's a brief explanation of each component involved in a distributed transaction¹²:

  ![new](https://github.com/anubhav7747/Notes/assets/77168708/b33f4e90-ebe7-4915-91ad-63a762783b93)


1. **Application to Resource**: The application initiates the transaction by sending the request to the available resources. The request consists of details such as operations that are to be performed by each resource in the given transaction¹.

2. **Resource 1 to Resource 2**: Once the resource receives the transaction request, resource 1 contacts resource 2 and asks resource 2 to prepare the commit. This step makes sure that both the available resources are able to perform the dedicated tasks and successfully complete the given transaction¹.

3. **Resource 2 to Resource 1**: After the second step, Resource 2 receives the request from Resource 1, it prepares for the commit. Resource 2 makes a response to resource 1 with an acknowledgment and confirms that it is ready to go ahead with the allocated transaction¹.

4. **Resource 1 to Resource 2**: Once Resource 1 receives an acknowledgment from Resource 2, it sends a request to Resource 2 and provides an instruction to commit the transaction. This step makes sure that Resource 1 has completed its task in the given transaction and now it is ready for Resource 2 to finalize the operation¹.

5. **Resource 2 to Resource 1**: When Resource 2 receives the commit request from Resource 1, it provides Resource 1 with a response and makes an acknowledgment that it has successfully committed the transaction it was assigned to. This step ensures that Resource 2 has completed its task from the operation and makes sure that both the resources have synchronized their states¹.

In the Two-Phase Commit Protocol, a coordinator is assigned to confirm whether the distributed transaction would abort or commit. The coordinator sends a Prepare T message to all the sites where the transaction executed. Transaction manager at each site on receiving this message Prepare T decides whether to commit or abort its component of T².

Source: Conversation with Bing, 23/1/2024
1. What is a Distributed Transaction? - GeeksforGeeks. https://www.geeksforgeeks.org/what-is-a-distributed-transaction/.
2. Two Phase Commit Protocol (Distributed Transaction Management). https://www.geeksforgeeks.org/two-phase-commit-protocol-distributed-transaction-management/.
3. Transaction Management - GeeksforGeeks. https://www.geeksforgeeks.org/transaction-management/.
