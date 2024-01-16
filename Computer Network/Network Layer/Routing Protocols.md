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



