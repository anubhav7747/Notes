Knowledge representation is a fundamental task in artificial intelligence (AI) that involves organizing knowledge into a form that can be used for reasoning, problem-solving, and decision-making. There are mainly four ways of knowledge representation:

  ![ai-techniques-of-knowledge-representation](https://github.com/anubhav7747/Notes/assets/77168708/5e218b9b-e6c7-4dc3-930c-8978e678567d)

1. **Logical Representation**: This is a language with concrete rules dealing with propositions and has no ambiguity in representation. It consists of precisely defined syntax and semantics which supports sound inference. Logical representation can be categorized into mainly two logics: Propositional Logics and Predicate logics.
    - **_Syntax_:**
      - Syntaxes are the rules which decide how we can construct legal sentences in the logic.
      - It determines which symbol we can use in knowledge representation.
      - How to write those symbols.
    - **_Semantics_:**
      - Semantics are the rules by which we can interpret the sentence in the logic.
      - Semantic also involves assigning a meaning to each sentence.

2. **Semantic Network Representation**: In Semantic networks, knowledge is represented in the form of graphical networks. This network consists of nodes representing objects and arcs which describe the relationship between those objects.

    This representation consist of mainly two types of relations:
      - IS-A relation (Inheritance)
      - Kind-of-relation
    
    **_Statements_:**
     - Jerry is a cat.
     - Jerry is a mammal
     - Jerry is owned by Priya.
     - Jerry is brown colored.
     - All Mammals are animal.

4. **Frame Representation**: A frame is a record like structure which consists of a collection of attributes and its values to describe an entity in the world. Frames are the AI data structure which divides knowledge into substructures by representing stereotypes situations. It consists of a collection of slots and slot values. These slots may be of any type and sizes. Slots have names and values which are called facets.

5. **Production Rules**: 
     Production rules system consist of (condition, action) pairs which mean, "If condition then action". It has mainly three parts:
      - The set of production rules
      - Working Memory
      - The recognize-act-cycle
     
     Example:
      1. IF (at bus stop AND bus arrives) THEN action (get into the bus)
      2. IF (on the bus AND paid AND empty seat) THEN action (sit down).
      3. IF (on bus AND unpaid) THEN action (pay charges).
      4. IF (bus arrives at destination) THEN action (get down from the bus).

Each of these techniques has its own syntax and semantics, advantages, and disadvantages. The main challenge in knowledge representation is finding a way to represent knowledge that is understandable by machines and can be used for reasoning and problem-solving.

