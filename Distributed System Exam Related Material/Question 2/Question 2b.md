## Discuss Birman Schiper Stephenson protocol with example.
The Birman-Schiper-Stephenson (BSS) protocol is used to maintain the causal ordering of messages in a distributed system¹. This means that if a message M1 is sent before another message M2, then for all processes that receive both messages, M1 should be received before M2¹.

Here's a simplified explanation of how it works:

1. **Sending a Message**: When a process Pi sends a message, it increments its own entry in its vector clock Ci[i] and sets the timestamp tm for the message m to Ci[i]¹.

2. **Receiving a Message**: When a process Pj (j ≠ i) receives a message m with timestamp tm, it delays the delivery of the message until two conditions are met¹:
    - Cj[i] = tm[i] - 1
    - For all k (k ≤ n and k ≠ i), Cj[k] >= tm[k]
   
   Once these conditions are met, the message is delivered to Pj, and Pj's vector clock is updated¹. The process then checks its buffer to see if any other messages can now be delivered¹.

Let's consider an example:

- Initial state for all the processes are 000¹.
- M1 is broadcasted from P3 to P1 and P2. e31 updates the vector clock to (001) and sends P1 and P2¹.
- P2 accepts the M1 with timestamp (001) because when it compares it with its initial timestamp i.e. (000) it finds that M1 is the 1st message it is receiving¹.
- Before M1 could reach P1, P2 sends M2 to P1 and P3 with time stamp (011). P1 could not accept M2 because upon comparing the timestamp of M2 with its initial timestamp a discrepancy is found because P1 has no message with timestamp (001) received earlier, so M2 is stored in buffer¹.
- Now M1 is received by P1 and accepted. M2 is removed from buffer and accepted by P1¹.
- M2 is accepted by P3 as there is no discrepancy in the time stamp¹.

This protocol ensures that the causal ordering of messages is maintained. However, it does require more messages to be sent and maintains limited state information¹.

Source: Conversation with Bing, 23/1/2024
1. Birman Schiper Stephenson Protocol - GeeksforGeeks. https://www.geeksforgeeks.org/birman-schiper-stephenson-protocol/.
2. GeeksforGeeks. https://www.geeksforgeeks.org/birman-schiper-stephenson-protocol/HLD.
3. Birman Schiper Stephenson Protocol - Online Tutorials Library. https://www.tutorialspoint.com/birman-schiper-stephenson-protocol.
4. birman schiper stephenson protocol and Schiper-Eggli-Sandoz - Ques10. https://www.ques10.com/p/17205/birman-schiper-stephenson-protocol-and-schiper-egg/.
