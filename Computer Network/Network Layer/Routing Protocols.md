## Routing Protocols
Routing protocols are sets of rules that routers use to exchange information and make decisions about the optimal paths for forwarding network traffic. These protocols play a crucial role in the operation of the Internet and other large-scale networks. Here are some commonly used routing protocols:

- **Intra domain** (for communication inside single autonomous system)
  - **Distance Vector:** RIP
  - **Link State:** OSPF
- **Inter Domain** (for communication between autonomous systems): BGP


## Concept of Routing Table
Routing tables are of two types: _static_ and _dynamic routing table_.

1. **Static Routing Table:** This routing table is created manually. The route of each of the destination is entered into the table by the administrator. If there is any change in the network, it is also done manually by the administrator. Any broken link in the network would require the routing tables to be manually reconfigured immediately so that alternate paths could be used. It is not possible to automatically update the table. Static routing tables are well suited for small networks. However, in large networks such as Internet, maintenance of static routing tables can be very tiresome.

2. **Dynamic Routing Table:** This routing table is updated automatically by the dynamic routing protocols such as RIP, BGP and OSPF whenever there is a change in the network. Generally, each router periodically shares its routing information with adjacent or all routers using the routing protocols so that the information about the network could be obtained. If some change is found in the network, the routing protocols automatically update all the routing tables.


## Distance Vector Algorithm
A distance vector algorithm is a type of routing algorithm used in computer networks to determine the best path for routing packets between nodes. The key characteristic of distance vector algorithms is that they consider both the direction and distance (metric) to reachable destinations. The most well-known distance vector routing algorithm is the Routing Information Protocol (RIP).
1. A router transmits its distance vector to each of its neighbors in a rotuing packet.
2. Each router receives and saves the most recently received distance vector from each of its neighbors.
3. A router recalculates its distance vector when:
   - It receives a distance vector from a neighbor containing different information than before.
   - It discovers that a link to a neighbor has gone down.

_The  distance vector calculation is based on minimizing the cost to each destination._


**Information kept by distance vecctor router**
- Each router has an ID
- Associated with each link connected to a router, there is a link cost (static or dynamic).
- Intermediate hops.


**Distance Vector Table Initialization**
- Distance to itself = 0
- Distance to ALL other routers = infinity number.

An example showing distance vector table preparation is given below:

![image](https://github.com/anubhav7747/Notes/assets/77168708/102caea3-186b-4332-a334-e64966bc374d)


**Advantages of distance vector routing**
- It is simple to configure and maintain than link state routing.


**Disadvantages of distance vector routing**
- It is slower to converge than link state.
- It is at risk from the count-to-infinity problem.
- For larger networks, distance vector routing results in larger routing tables than link state since each router must know about all other routers. This can also lead to congestion on WAN links.


## Count-to-infinity problem
- Theoretically, the distance vector routing algorithm works efficiently but practically, it has serious loopholes. Even though a correct answer is derived, it takes time.
- In practice, this algorithm acts quickly to good news but acts very late to bad news.
- For example, let us consider a router whose best route to destination **X** is large. If on the next neighbor exchange, one of its neighbors (say, **A**) declares a short delay to **X**, the router starts using the line through **A** to reach **X**.
- The good news is thus processed by **B** within a single vector exchange. The news spreads even faster as it is received by its neighbors.

  ![image](https://github.com/anubhav7747/Notes/assets/77168708/bad0b1e9-b3fc-475d-84dd-791988cb5742)

- However, the situation is very different in the case of bad news propagation. To understand the propagation of bad news, consider the situation shown in Figure (b).
- Here, initially all routers are properly functioning, and the routers **B**, **C**, **D** and **E** are 1, 2, 3 and 4 hops away from **A**, respectively. Now, if A goes down all of a sudden, the routers still think **A** to be functional.
- At the first vector exchange, no vector is received from **A** but the node **B** sees in the vector received from **C** that **C** has a path of length 2 to **A**. As **B** does not know that path from **C** to **A** goes through it, it updates its routing table with distance to **A** as 3 and via **C**.
- Now, at the second vector exchange, as **C** sees the distance of **B** to **A** as 3, it updates its distance to **A** as 4 and via **B**. Similarly, all the routers continue to update their routing tables and increase their distance to **A** after every vector exchange.
- Eventually, all routers update their routing tables with distance to **A** as infinity where infinity denotes the longest path plus one. This problem is known as the **count-to-infinity** problem.

![image](https://github.com/anubhav7747/Notes/assets/77168708/39362f7f-22bd-4c67-97c9-33ed243d06d1)


## Link State Routing
- It is a dynamic routing algorithm in which each router shares knowledge of its neighbors with every other router in the network.
- A router sends its information about its neighbors only to all the routers through flooding.
- Information sharing takes place only whenever there is a change.
- It makes use of **Dijkstra’s Algorithm** for making routing tables.
- Link-state routing is a type of routing algorithm used in computer networks to determine the optimal path for routing packets between nodes. Unlike distance vector algorithms, link-state routing algorithms focus on building a detailed map of the entire network topology, taking into account the state of each link. One of the most widely used link-state routing protocols is the Open Shortest Path First (OSPF) protocol.


### Problems
Heavy traffic due to flooding of packets. Flooding can result in infinite looping which can be solved by using the **Time to live (TTl)** field.


### Building links state packets
Each router collects calculates link distance with its immediate neighbors and package this information to form a link state packet (LSP).
- Each LSP comprises four fields: the identity of the sending router, sequence number, age and list of its neighboring links. The first and fourth fields of LSP together determine the network topology. The second field indicates the sequence number assigned to the LSP packet; the sequence number is incremented by one each time the packet is created by the router. The third field indicates the duration for which the LSP has been residing in the domain.
- The LSP also includes delay to reach each adjacent neighbor. For example, Figure (b) shows the LSPs for each of the five routers of the subnet shown in Figure (a). After each router has created the LSP, it needs to distribute its LSP to its neighbors in the network. This process is referred to as **flooding**.
- After receiving all LSPs, the next step for a router is to compute the shortest path to every possible destination using the Dijkstra’s algorithm and build the routing table. The routing table of a router lists all the routers in the network, the minimum cost of reaching them and the next router in the path to which the packet should be forwarded.

![image](https://github.com/anubhav7747/Notes/assets/77168708/196f99c3-89ed-44fb-a31c-c43ab122449c)


## Link State versus Distance Vector

**S. No.** | **Distance Vector Routing** | **Link State Routing**
---------- | --------------------------- | ----------------------
1 | Make use of Bellman Ford Algorithm. | Make use of Dijakstra's algorithm.
2 | Count of infinity problem. | No count of infinity problem.
3 | Traffic is less. | Traffic is more.
4 | Practical implementation is RIP and IGRP. | Practical implementation is OSPF and ISIS.
5 | Based on local knowledge, since it update table based on information from neighbors. | Based on global knowledge, it have knowledge about entire network.
6 | Bandwidth required is less due to local sharing, small packets and no flooding. | Bandwidth required is more due to flooding and sending of large link state packets.
7 | Suitable for smaller networks. | Preferred for large and complex networks.

![image](https://github.com/anubhav7747/Notes/assets/77168708/976b5ad0-67c9-4966-9cb3-b0ac1a64a02d)

