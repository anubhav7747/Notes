# Network Address Translation (NAT)
Network Address Translation (NAT) is a technique used in computer networking to modify network address information in packet headers while in transit. The primary purpose of NAT is to conserve IP addresses by allowing multiple devices within a private network to share a single public IP address when communicating with external networks like the Internet. NAT operates at the network layer (Layer 3) of the OSI model and is commonly used in home and small office networks.

The basic idea behind NAT is to assign each company a single **public IP address** (or at most, a small number of them) for Internet traffic. Within the company, every computer gets a unique IP address, which is used for routing intramural traffic (within the walls of a building). However, when a packet exits the company and goes to the ISP, an address translation takes place. To make this scheme possible, three ranges of IP addresses have been declared as **private**. Companies may use them internally as they wish. The only rule is that no packets containing these addresses may appear on the Internet itself.

The three reserved ranges are:
1. 10.0.0.0 - 10.255.255.255/8 (16,777,216 hosts)
2. 172.16.0.0 - 172.16.255.255/12 (1,048,576 hosts)
3. 192.168.0.0 - 192.168.255.255/16 (65,536 hosts)

Within the company premises, every machine has a unique address of the form 10.x.y.z. However, when a packet leaves the company premises, it passes through a **NAT box** that converts the internal IP source address, 10.0.0.1 in the figure, to the company's true IP address, 198.60.42.12 in this example.

  ![image](https://github.com/anubhav7747/Notes/assets/77168708/974bcc95-8000-4d93-9af6-dd782b805f76)

- The NAT box is often combined in a single device with a firewall, which provides security by carefully controlling what goes into the company and what comes out.
- The Nat designers observed that most IP packets carry either TCP or UDP payloads. So, when a packet reaches the NAT box, it replaces the source IP address 10.0.0.1 with company's public IP and saves source IP and source port number in table that it  maintains. The index of this table entry replaces the source port address of this outgoing packet. Hence now the packet has public IP as source IP in IP header part and table index as source port address in TCP header part. Finally, both the IP and TCP header checksums are recomputed and inserted into the packet.
- When a packet arrives at the NAT box from the ISP, the Source port in the TCP header is extracted and used as an index into the NAT box's mapping table. From the entry located, the internal IP address and original TCP Source port are extracted and inserted into the packet.
- Then both the IP and TCP checksums are recomputed and inserted into the packet. The packet is then passed to the company router for normal delivery using the 10.x.y.z address.
- NAT can also be used to alleviate the IP shortage for ADSL and cable users. When the ISP assigns each user an address, it uses 10.x.y.z addresses. When packets from user machines exit the ISP and enter the main Internet, they pass through a NAT box that translates them to the ISP's true Internet address. On the way back, packets undergo the reverse mapping. In this respect, to the rest of the Internet, the ISP and its home ADSL/cable users just looks like a big company.




