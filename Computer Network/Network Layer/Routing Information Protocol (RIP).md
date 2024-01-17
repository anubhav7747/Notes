# Routing Information Protocol (RIP)
- An intradomain routing protocol (also known as **interior gateway protocol**) which is used inside an autonomous system. It is a simple protocol whose operating procedures are similar to the widely used distance vector routing. The operation of RIP is based on certain considerations, which are as follows:
  - RIP is used in autonomous systems, which consists of routers and networks (links). Routing tables are created for the routers, but the networks do not implement any such table.
  - As the first column of a routing table specifies a destination and in case of RIP, the destination is the network; therefore, a network address is defined in the first column of the R routing table.
  - The metric used by RIP is the hop count where the term hop defines the number of subnets traversed from the source router to the destination subnet with including the destination subnet.
  - The maximum cost of a path in RIP cannot be more than 15, that is, any route in an autonomous system cannot have more than 15 hops.
  - The next-node column in the routing table of RIP contains the address of the router to which the packet is to be forwarded (the first hop to be done).

- Consider an autonomous system consisting of three networks and three routers are shown in figure.

  ![image](https://github.com/anubhav7747/Notes/assets/77168708/fcc84661-f9a3-4006-b1fe-3b9ecd708212)


- Each router has its own routing table showing how to reach each network existing in the AS. Let us study the routing tables at RouterA, RouterB & RouterC.
- The networks 10.0.0.0, 20.0.0, and 192.168.2.0 are directly connected to the router RouterB; therefore, RouterB need not make any hop count entries for these networks.
- The packets destined for these networks can be sent directly by the router; however, such forwarding cannot be done in the case of the other networks.
- For example, if the router RouterB needs to send packets to the two networks; 192.168.1.0 and 192.168.3.0, then it has to forward the packets to the router RouterA and RouterC respectively. Thus, for these two networks, the next-node column of the routing table at RouterB stores the interface of RouterA with the IP address 192.168.1.0 and RouterC with IP 192.168.3.0.
- Similarly, routing tables for RouterA and RouterC can also be explained in the same manner.

  ![image](https://github.com/anubhav7747/Notes/assets/77168708/4f4c15b2-aba3-42e7-8c4f-042be4c2ce6d)

