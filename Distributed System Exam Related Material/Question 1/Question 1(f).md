## Explain in detail about Fundamental models of distributed system.
Fundamental models of distributed systems provide a conceptual framework for understanding and designing distributed computing environments. These models help in abstracting the complexities of distributed systems and provide a basis for analysis and development. Here are some fundamental models of distributed systems:

1. **Client-Server Model:**
    - In the client-server model, the system is divided into two main components: clients and servers. Clients initiate requests for services, and servers provide those services. This model facilitates a clear separation of concerns, allowing for easier management, scalability, and resource allocation. Web applications, where browsers (clients) request resources from web servers, are a common example of the client-server model.
2. **Peer-to-Peer Model:**
    - In the peer-to-peer model, all nodes in the network are considered equal, and each node can act as both a client and a server. Peers collaborate and share resources directly with each other, without relying on a central server. Peer-to-peer networks are often used for file sharing, distributed computing, and collaborative applications.
3. **Master-Slave (Primary-Backup) Model:**
    - In the master-slave model, one node (the master or primary) is designated as the main server, and the others (the slaves or backups) replicate the state of the master. The master handles client requests, while the slaves act as backups, ready to take over in case of a failure. This model enhances fault tolerance by ensuring that backup nodes can quickly assume the role of the master.
4. **Three-Tier Architecture:**
    - The three-tier architecture extends the client-server model by introducing an additional layer, known as the application server or middleware, between the client and the database server. This model separates the presentation layer (client), application logic layer (application server), and data storage layer (database server). It provides improved scalability, maintainability, and flexibility.
5. **Object-Oriented Model:**
    - The object-oriented model extends traditional programming paradigms to distributed systems. Objects encapsulate both data and methods, and objects can be distributed across multiple nodes. Object-oriented distributed systems enable the creation of reusable and modular components that can be distributed and executed in a networked environment.
6. **Event-Driven Model:**
    - In the event-driven model, components communicate by generating and responding to events. An event-driven system reacts to events such as user actions, messages from other components, or changes in the environment. This model is often used in graphical user interfaces, real-time systems, and systems with asynchronous communication.
7. **Publish-Subscribe Model:**
    - The publish-subscribe model involves components (publishers) that generate events or messages and other components (subscribers) that express interest in receiving specific types of events. Publishers and subscribers are decoupled, allowing for dynamic, loosely-coupled communication. This model is commonly used in messaging systems and event-driven architectures.
8. **Mobile-Agent Model:**
    - In the mobile-agent model, autonomous agents travel across the network to execute tasks on different nodes. Agents carry both code and state, allowing them to migrate and continue their execution on remote machines. This model is suitable for applications with dynamic environments and distributed problem-solving.
9. **Tuple Space Model (Linda):**
    - The tuple space model, inspired by the Linda coordination language, uses a shared space where processes can read from and write tuples. Processes communicate by depositing and retrieving tuples from this space, providing a form of distributed coordination. Tuple space is used in coordination and communication in parallel and distributed systems.

These fundamental models provide different perspectives on designing and structuring distributed systems, and often, real-world systems combine elements from multiple models to meet specific requirements. The choice of a particular model depends on the goals of the distributed application, the nature of the tasks it needs to perform, and the characteristics of the underlying network.

