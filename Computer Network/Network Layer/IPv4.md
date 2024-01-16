# IPv4

![image](https://github.com/anubhav7747/Notes/assets/77168708/7551b574-37c9-4849-b5a9-e33962a168a2)

- The IPv4 (Internet Protocol version 4) header is a fundamental component of the Internet Protocol suite and is used to facilitate communication between devices in a network.
- The IPv4 header is located at the beginning of an IPv4 packet and contains various fields that provide essential information for the transmission and delivery of data.
- Here is a breakdown of the key fields in the IPv4 header:

  - **Version (4 bits)**
    - It indicates the version being used.
    - The current version of IP is 4.

  - **Internet Header Length (IHL) (4 bits)**
    - Specifies the length of the IP header in 32-bit words.
    - This field is crucial for locating the start of the data in the packet.
    - The minimum length of IPv4 header is five 32-bit words.
    - Value is to be multiplied by 4 for valid header values in 4 bits.

  - **Type of Service (TOS) or Differentiated Services Code Point (DSCP) (8 bits)**
    - Originally used for specifying the quality of service such as precedence, delay, throughput and reliability.
    - This field has been redefined for Differentiated Services Code Point in modern networks.

  - **Total Length (16 bits)**
    - Indicates the total length of the IP packet, including both the header and the data.
    - The maximum permitted length is 65,535 (2<sup>16</sup>–1) bytes with 20–60 bytes for header and rest for data.

  - **Identification (16 bits)**
    - Used for uniquely identifying a particular datagram, especially useful for fragmentation and reassembly of packets.
    - The datagrams can be fragmented at the sender’s end for transmission and then reassembled at the receiver’s end.
    - When a datagram is fragmented into multiple datagrams, all datagrams belonging to the same datagram are labelled with same identification number and the datagrams having same identification number are reassembled at the receiving side.

  - **Flags (3 bits)**
    - Contains control flags, including the Don't Fragment (DF) flag, the More Fragments (MF) flag, and a reserved flag.
    - It is a 3-bit long field in which the first bit is reserved and always zero, the second bit is do not fragment (DF) and the third bit is more fragment (MF).
    - If DF bit is set to 1 then it means the datagram must not be fragmented while a value of zero indicates the fragmentation of the datagram.
    - If MF bit is set to zero, then it means this fragment is the last fragment.
    - If MF bit is zero then it means there are more fragments after this fragment.

  - **Fragmentation Offset (13 bits)**
    - Specifies the offset of the data in the original IP packet concerning the beginning of the entire datagram.
    - It is used for reassembly of fragmented packets.
    - It is measured in units of eight octets (64 bits).
    - The first fragment is set to the offset zero.

  - **Time-to-Live (TTL) (8 bits)**
    - Represents the maximum time the packet is allowed to traverse the network.
    - It indicates the total time (in seconds) or number of hops (routers) that an IPv4 datagram can survive before being discarded.
    - As a router receives a datagram, it decrements the TTL value of datagram by one and then forwards that datagram to the next hop and so on.
    - When the TTL value becomes zero, it is discarded.
    - Generally, when a datagram is sent by the source node, its TTL value is set to the two times of the maximum number of routes between the sending and the receiving hosts.

  - **Protocol (8 bits)**
    - Identifies the higher-layer protocol that is carried in the data field of the IPv4 packet (e.g., TCP, UDP, ICMP).

  - **Header Checksum (16 bits)**
    - Provides error-checking for the header itself.

  - **Source IP Address (32 bits)**
    - holds the IPv4 address of the sending host.
    - This field remains unchanged during the lifetime of the datagram.

  - **Destination IP Address (32 bits)**
    - holds the IPv4 address of the receiving host.
    - This field remains unchanged during the lifetime of the datagram.

  - **Options (upto 40 bytes)**
    - These are included in the variable part of header and can be of maximum 40 bytes.
    - These are optional fields, which are used for debugging and network testing.
    - However, if they are present in the header then all implementations must able to handle these options.
    - Some examples are record route and strict source route.

The IPv4 header is followed by the data payload, which can be from the transport layer protocol indicated in the Protocol field, such as TCP or UDP.
