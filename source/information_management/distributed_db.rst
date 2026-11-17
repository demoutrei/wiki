Distributed Databases
=====================

**Distributed databases** are colelctions of logically related data that are physically stored across multiple sites, servers, or geographical locations. Despite being distributed, they are intended to appear to users as a coherent system that supports consistent storage and retrieval of information.

.. admonition:: Why Use Distributed Databases?
    :class: hint

    Performance
      Data can be stored closer to where it is used, reducing latency.

    Scalability
      Systems can grow by adding more nodes rather than upgrading a single central server.

    Reliability and availability
      Replication and redundancy across sites reduce the risk of total system failure.

    Organizational autonomy
      Different departments or branches can manage their own data while still participating in a larger system.

.. admonition:: Key concept
    :class: tip

    In a distributed database, data is partitioned and/or replicated across multiple nodes, but users should ideally experience a unified view of the data.

  
Homogeneous Distributed Databases
+++++++++++++++++++++++++++++++++

A **homogenous distributed database** uses the same DBMS software and data model at all sites. The systems are highly similar or identical in terms of:

- Database engine (e.g. all nodes run the same version of PostgreSQL)
- Data model (e.g. all nodes are relational)
- Schema conventions and query language (e.g. SQL)

Because of this autonomy, it is generally easier to:

- Maintain consistent schemas and constraints
- Implement global transactions and distributed queries
- Manage replication and synchronization

.. note::

    Homogenous systems are often easier to administer but may be less flexible when integrating external or legacy systems that use different technologies.


Heterogeneous Distributed Databases
+++++++++++++++++++++++++++++++++++

A **heterogeneous distributed database** consists of sites that use different DBMS software, data models, or query languages. Differences may include:

- Relational vs. NoSQL (e.g. PostgreSQL at one site, MongoDB at another)
- Different vendors (e.g. Oracle, SQL server, and MySQL)
- Different schema designs and naming conventions

To function as a distributed system, a heterogeneous environment requires:

- Mediation or translation layers to map queries and data between systems
- Data integrationn mechanisms (e.g. ETL processes, middleware)
- Conflict resolution strategies for differing constraints and semantics


Federated Databases
+++++++++++++++++++

A **federated database** is a special type of heterogeneous distributed database in which multiple anonymous databases are integrated into a unified, virtual database. Each participating database:

- Retains its own schema, DBMS, and local control
- May be independently administered by different departments or organizations
- Is connected through a federation layer tohat provides a global schema or view

The federation layer (sometimes called a **mediator** or **global schema**) is responsible for:

- Mapping global queries to local databases.
- Resolving naming conflicts and schema differences
- Combining partial results into a single response