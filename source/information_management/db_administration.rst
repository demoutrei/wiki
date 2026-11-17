Database Administration
=======================

Database administration focuses on the operational management of database systems so that they remain available, reliable, secure, and performant. Three core responsibilities are **concurrency ontrol**, **security management**, and **backup and recovery**. These functions direectly affect the quality, reliability, and safety of the data that supports organizational processes.


Concurrency
+++++++++++

**Concurrency** refers to multiple users or applications accessing and modifying the database at the same time. Without proper control, concurrent access can lead to problems such as lost updates, inconsistent reads, or deadlocks.

.. grid:: 1
    :gutter: 3

    .. grid-item-card:: Transaction Management

        Database administrators (ADBs) configure transaction isolation levels (e.g. read committed, repetable read) to balance consistency and performance.

    .. grid-item-card:: Locking Mechanisms

        The DBMS uses locks (row-level, page-level, table-level) to prevent conflicting operations from corrupting data.

    .. grid-item-card:: Daeadlock Prevention

        DBAs monitor and tune systems to detect and resolve deadlocks where transactions wait indefinitely for each other's locks.

.. admonition:: Key Point
    :class: tip

    Concurrency mechanisms allow many users to work with the database at once while preserving data integrity and reliability.


Security
++++++++

**Database security** protects data from unauthorized access, modification, or disclosure. It is closely related to organizational information security but focuses on controls implemented within the DBMS.

.. grid:: 1
    :gutter: 3

    .. grid-item-card:: Authentication

        Verifying user identity (e.g. username/password, multi-factor authentication).

    .. grid-item-card:: Authorization

        Defining roles and privileges that specify which tables, views, and operations (``SELECT``, ``INSERT``, ``UPDATE``, ``DELETE``) each user may perform.

    .. grid-item-card:: Encryption

        Encrypting data at rest and in transit to protect sensitive information such as personal or financial data.

    .. grid-item-card:: Auditing and Logging

        Recording access and changes to deteect misuse and support compliance requirements.

.. admonition:: Security Tip
    :class: tip

    When designing a database, define roles and privileges early. Align them with organizational policies and legal requirements (e.g. data protection regulations) to avoid exposure sensitive data.


Backup and Recovery
+++++++++++++++++++

**Backup and recovery** ensure that data can be restored after failures such as hardware crashes, software errors, or accidental deletions. This is essential for maintaining availability and minimizing data loss.

.. grid:: 1
    :gutter: 3

    .. grid-item-card:: Backup Strategies

        Full, incremental, and differential backups; scheduling (daily, weekly); and retention policies.

    .. grid-item-card:: Recovery Procedures

        Restoring from backups, applying transaction logs, and validating restored data.

    .. grid-item-card:: Disaster Recovery Planning

        Offsite backups, replication to secondary sites, and documented recovery time objectives.


Integration with Database Quality
+++++++++++++++++++++++++++++++++

Concurrency, security, and backup.recovery are not isolated tasks. Together, they determine how reliable, scalable, and secure a database system is:

- Concurrency affects performance and consistency for many simultaneous users.
- Security ensures that only authorized users can access or modify data, preserving confidentiality and integrity.
- Backup and recovery guarantee that data remains available and can be restored after failures, supporting organizational continuity.
