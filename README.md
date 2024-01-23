# Supercharge Your Database, Unleashing High-Load Reads with Database Replication 

In this Repo, let's delve into the fundamentals of database replication and uncover the multitude of advantages it brings. As we navigate through this journey, we'll discover how database replication becomes a crucial precursor for addressing high-load reads, laying the foundation for the seamless integration of Database Sharding. Join me as we unravel the keys to unlocking an efficient, high-performance database landscape.


## 1. Master-Backup vs Multi-Master Replication:

  - Master-Backup involves one primary node accepting writes, with one or more backup nodes receiving those writes.

  - Multi-Master Replication allows multiple nodes to act as masters, each accepting writes and sharing them with other nodes.


## 2. Synchronous vs Asynchronous Replication:

  - Synchronous Replication: A write transaction to the master is blocked until it is replicated to backup/standby nodes.

  - Asynchronous Replication: A write transaction is considered successful once written to the master, with asynchronous replication to backup nodes.


## 3. Demo with Postgres:

  - I recently created a small project showcasing PostgreSQL replication using Docker Compose. One master node and three follower nodes are set up, demonstrating the ease of implementation.


## 4. Pros & Cons of Replication:

  - Pros:

      - Horizontal Scaling: Distribute workload across multiple nodes.
   
      - Region-based Queries: Maintain databases per region for optimized queries.



  - Cons:

      - Eventual Consistency: Replicas may lag behind the master.
   
      - Slow Writes (in synchronous replication).
   
      - Complexity in Implementation (especially with multi-master setups).
