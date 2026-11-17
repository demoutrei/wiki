Patterns of Data Distribution
=============================

In distributed database systems, **patterns of data distribution** determine how data is stored across multiple servers or locations. Appropriate choices influence reliability, scalability, performance, and security. Three common patterns are **replication**, **vertical partitioning**, and **horizontal partitioning**.


Replication
+++++++++++

**Replication** means storing copies of the same data on multiple nodes. Each replica contains the same logical dataset, although it may not be physically identical at all times due to synchronization delays.

.. admonition:: Key Idea
    :class: tip

    Replication trades increased storage and complexity for improved availability, fault tolerance, and often read performance.

.. admonition:: Advantages and Challenges
    :class: tip

    Availability
      If one server fails, another replica can continue serving requests.

    Read scalability
      Read queries can be distributed across replicas, reducing response times.

    Disaster recovery
      Replicas in different data centers protect against regional failures.

    Consistency management
      Keeping replicas synchronized introduces complexity (e.g. eventual vs strong consistency).
    
    Write overhead
      Updates must be propagated to all replicas, increasing network and processing cost.


Vertical Partitioning
+++++++++++++++++++++

**Vertical partitioning** divides a table by its columns. Different sets of attributes are stored on different nodes, while rows are logically linked via a common key.

.. admonition:: Key Idea
    :class: tip

    Group attributes that are frequently accessed together, and separate those that are rarely used or sensitive, to optimize performance and security.

.. admonition:: Advantages and Challenges
    :class: tip

    Performance
      Queries that need only a subset of columns can be served from a smaller, more efficient partition.

    Security and compliance
      Sensitive attributes (e.g. medical data, financial details) can be stored on hardened nodes with stricter access control.

    Flexibility
      Differnet partitions can be tuned (indexes, storage engines) for specific workloads.

    Join overhead
      Reconstructing full rows may require joins across partitions, increasing query complexity and latency.


Horizontal Partitioning
+++++++++++++++++++++++

**Horizontal partitioning** divides a table by its rows. Each partition contains a subset of rows, usually based on a criterion such as region, time, or range of values.

.. important::

    Horizontal partitioning is often called **sharding** in large-scale systems. It is a primary strategy for scaling write-heavy workloads.

.. admonition:: Advantages and Challenges
    :class: tip

    Scalability
      Data volume and write load are distributed across nodes, allowing the system to grow by adding more shards.

    Locality
      Queries can be directed to the relevant partition (e.g. region-specific data), reducing unnecessary scanning.

    Maintenance
      Backups and maintenance can be performed per partition, reducing downtime.

    Complex queries
      Global queries (e.g. across all region) must aggregate results from ultiple partitions, increasing complexity.


Choosing a Distribution Pattern
+++++++++++++++++++++++++++++++

In practice, systems often combine these patterns. For example, a horizontally partitioned database may also replicate each shard for fault tolerance, and vertically partition sensitive attributes for security. When analyzing or designing a database, it is important to evaluate how distribution choices affect reliability, scalability, efficiency, and protection of sensitive information.