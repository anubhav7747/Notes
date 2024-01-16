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


