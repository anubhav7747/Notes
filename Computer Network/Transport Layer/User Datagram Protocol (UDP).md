# User Datagram Protocol (UDP)
- It is a connectionless, unreliable transport layer protocol.
- It offers process-to-process delivery with limited error checking.
- Segments are sent to the destination host without any prior establishment of the connection between communicating hosts.
- By unreliable, we mean that UDP does not perform error and flow control , hence no guarantee about the proper delivery of segments at the destination
- As segments in UDP are not numbered, there is no means to identify the frames that have lost during the transmission.
- Used by a process that has only a small message to send and is not much concerned about the reliability.
- The applications such as speech and video for which instant delivery is more important than accurate delivery, prefer to adopt UDP for transport.
- The UDP packets, known as user datagrams, have a fixed-size header of eight bytes, which is followed by the data
- The header of UDP packet contains four field of 16 bits each as shown in figure below:

  ![transport-layer-protocols2](https://github.com/anubhav7747/Notes/assets/77168708/06d6036a-ccd5-4662-8497-46f2df9ea678)


The description of various field of a UDP packet header is as follows:
- **<ins>Source Port Number</ins>:**
  - It is a 16-bit long field that define the source process port number of sender machine.
  - If the UDP packet is being sent from the client, that is, if the source host is client, then the source port number will be chosen randomly by the UDP software running on the client.
  - If the UDP packet is sent by the server, the source port number will be a well-known port used with UDP.

- Some of the well-known ports used with UDP are listed in following table.
    **Port** | **Protocol** | **Description**
    -------- | ------------ | -------------
    13|Daytime|Returns the date and the time|
    53|Name sever|Domain name service|
    111|RPC|Remote procedure call|
    123|NTP|Network time protocol

- **<ins>Destination Port Number<ins>:**
    - It is a 16-bit long field that define the process running on the destination port number will be an ephemeral port number ranging from 49152 to 65535.

- However, if the destination host is the server, the destination port number will be a well-known port (between 0-1023) used with UDP. Port number range from 1024 to 4915 are known as registered ports. Total Length: It is a 16-bit long field that specific the total length of the UDP packet including header as well as data. The size of this field can range from 0 to 65535 (that is 2<sup>16</sup>-1) bytes but the size of UDP packet must be much less, as it is to be encapsulated in an IP datagram having a total length of 65535 bytes.

- **<ins>Checksum<ins>:**
    - It is a 16-bit long field that is used for error detection over both the header and the data.
    - The checksum is calculated on UDP Header, Data length & pseudo-IP header includes not all fields of regular IP headder rather it includes only Source IP, Destination IP, Protocol number and Data length fields.


### <ins>Uses of UDP</ins>
- It is suitable for multicasting.
- It is used for management processes such as SNMP.
- It is used for the route updating protocols such as routing information protocol (RIP).
