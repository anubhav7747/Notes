## What are commit-protocols? Explain how Two-Phase commit protocol responds to failure of participating site and failure of coordinator.

### Commit Protocols:
Commit protocols are mechanisms used in distributed systems to coordinate and ensure the atomicity and consistency of distributed transactions. These protocols manage the decision-making process regarding whether a distributed transaction should be committed or aborted, taking into account the responses from different participating sites or nodes. One well-known commit protocol is the Two-Phase Commit (2PC) protocol.

### Two-Phase Commit (2PC) Protocol:
The Two-Phase Commit protocol is a distributed algorithm that ensures atomicity in a distributed transaction by coordinating the commit or abort decision among all participating nodes. The protocol involves two phases:

1. **Voting (Prepare) Phase:**
    - The coordinator node sends a prepare message to all participating nodes, asking them if they are ready to commit the transaction.
    - Each participating node replies with a vote, indicating whether it is prepared to commit or abort the transaction.
    - If any node votes to abort or if there is a timeout during this phase, the coordinator decides to abort the transaction.
2. **Decision (Commit or Abort) Phase:**
    - Based on the votes received during the prepare phase, the coordinator makes a global decision to commit or abort the transaction.
    - The coordinator sends a commit or abort decision to all participating nodes.
    - Each participating node performs the committed or abort action accordingly.

### Handling Failures in Two-Phase Commit:
The Two-Phase Commit protocol is designed to handle failures during both the Voting Phase and the Decision Phase.

1. **Failure of a Participating Site:**
    - If a participating site (node) fails during the Voting Phase:
      - The coordinator waits for a response from the failed site for a specified timeout period.
      - If no response is received, the coordinator assumes an implicit vote to abort and proceeds with the Decision Phase.
      - Other participating sites that have voted to commit are not affected.
    - If a participating site fails during the Decision Phase:
      - The coordinator sends a commit or abort decision to the failed site upon recovery.
      - The site then performs the corresponding action based on the decision received.
2. **Failure of the Coordinator:**
    - If the coordinator fails during the Voting Phase:
      - Participants that have voted to commit or abort retain their votes until the coordinator recovers.
      - The coordinator requests votes from participants again upon recovery.
    - If the coordinator fails during the Decision Phase:
      - Participants proceed with the action (commit or abort) based on their votes, assuming the coordinator's decision.

### Advantages and Limitations:
- **Advantages:**
  - Simple and widely used protocol.
  - Guarantees atomicity in a distributed transaction.
- **Limitations:**
  - Blocking problem: If the coordinator crashes after participants have voted to commit but before they receive the decision, the protocol may block.
  - Blocking can be resolved using timeout mechanisms and additional recovery steps.

While the Two-Phase Commit protocol provides a straightforward mechanism for ensuring atomicity in distributed transactions, its blocking behavior and sensitivity to coordinator failures have led to the development of more sophisticated protocols, such as Three-Phase Commit (3PC) and Paxos, to address some of these limitations.

