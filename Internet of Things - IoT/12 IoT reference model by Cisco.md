## IoT Reference Model by Cisco

The Cisco IoT reference model is a conceptual framework that provides a structured approach to understanding, designing, and deploying Internet of Things (IoT) solutions. It is composed of seven levels:

1. **Physical Devices and Controllers**: This level includes the actual devices, such as sensors, machines, and intelligent edge nodes.
2. **Connectivity**: This level supports information transmission between devices and the network.
3. **Edge/Fog Computing**: This level links information technology and operational technology.
4. **Data Accumulation**: This level manages and converts data between devices and applications.
5. **Data Abstraction**: This level supports developing simple and performant applications.
6. **Applications**: This level includes control applications or mobile applications or business intelligence and analytics.
7. **Collaboration and Processes**: This level enables communication and collaboration between people while focusing on business processes.

This model helps IT departments, CIOs, and developers by offering practical suggestions for addressing IoT challenges such as scalability, interoperability, agility, and compatibility with legacy systems.

<br>

## Detailed view:
**Level 1: Physical Devices and Controllers (Edge; Things)**
- This level is also called the "edge level".
- It contains the "things", such as sensors, devices and machines, virtual objects.

**Level 2: Connectivity**
- This level consists of the communication and processing units.
- It carries out routing, switching, and the translation of protocols.
- It facilitates communications between Level 1 devcices and with Level 1 devcices, as well as communication across networks.
- Security and self-learning network analytics are also provided at this level.

**Level 3: Edge (Fog) Computing**
- This level receives the data packets and outputs data understandable to higher levels.
- It combines network and data level analytics.
- It performs data element analysis and transformation, data filtering, cleanup, aggregation, and packet content inspection.
- It can also generate events.
 
**Level 4: Data Accumulation (Storage)**
- This level converts data-in-motion to data-at-rest.
- Data format is converted from network packets to database relational tables.
- It transforms event-based computing to query based computing.
- Data is also reduced through filtering and selective storage.

**Level 5: Data Abstraction (Aggregation and Access)**
- This level creates schemas and views of data in the manner that applications want.
- It combines data from multiple sources.
- It simplifies, filters, selects, projects and reformats data to serve client applications.
- It reconciles the differences in data shape, format, semantics, access protocol and security.

**Level 6: Application (Reporting, Analytics, Control)**
- This level controls the applications and performs business intelligence and analytics.

**Level 7: Collaboration and Processes**
- This level involves the people and business processes.


Levels 1 to 3 are also called the "edge-side layer".

Levels 4 to 6 are also called the "server/cloud-side layer".

Level 7 is also called the "user-side layer".
