# Distributed systems
Distributed systems are complex computing systems that consist of multiple autonomous components located on different nodes, communicating and coordinating with each other to achieve a common goal. Some key characteristics of distributed systems include:

* `Scalability` - should be able to handle large amounts of data and workloads by adding more nodes to the system.
* `Concurrency` - ability to process multiple requests or tasks simultaneously, improving overall system performance.
* `Consistency` - must ensure data consistency across all nodes. 
* `Fault tolerance` - systems can continue to function even if some nodes fail.
* `Availability` - systems should be highly available. 
* `Efficiency` - how well the system performs.
* `Security` - must be designed with security in mind to protect against various threats, such as data breaches, denial-of-service attacks, and unauthorized access.

# DNS
* [How does DNS work?](https://www.youtube.com/watch?v=27r4Bzuj5NQ)
* [Route 53 basics](https://www.youtube.com/watch?v=JRZiQFVWpi8)
* [DNS & Amazon Route 53 Deep dive](https://www.youtube.com/watch?v=94vdYMBcE5Y&t=2495s)  
  * [Simple routing policy](https://youtu.be/94vdYMBcE5Y?t=1186).
  * Latency based routing policy.
  * Weighted routing policy.
  * Geolocation routing policy.
  * Failover routing policy (primary to secondary failover based on health checks).

# Load balancer
* Balance incoming traffic.
* Acts as reverse proxy.
* Authentication/ Authorization.
* Traffic control.
* Rate limiting/ circuit breaking.
* Software or hardware LBs.  
  * Round Robin.  
  * Least connections.
  * Least response time.
  * IP hash.
* L4 vs L7.
* Active-Active / Active-Passive LB config.

# CDN
* To reduce the latency.
* Content can be served from the nearest location of the user.
* Static content like videos, pictures, audio, etc.
* Push/ pull based CDN.

# Front-end servers
* Web servers (stateless lightweight web service).
  * Request validation.
  * Authentication/ Authorization.
  * TLS (SSL) termination.
  * Server side encryption.
  * Caching.
  * Rate limiting.

# App servers
* Any application server (example: image resizing, video resizing, etc.).

# Database servers
### SQL - RDBMS
* MSSQL, Postgres, etc.
* Data saved in tables
* Banking, Financial apps, etc.
* For high consistency.
* ACID properties.

### NoSQL
* MongoDB (DocumentDB, stores like JSON objects), Cassandra (columnar DB), Neo4J (Graph DB), ETCD (key-value DB), etc.
* Unstructured data.
* Dynamic data.
* For less consistency apps like social media.
* Highly scalable than RDBMS.

### Notes
* Reads from all replicas.
* Writes only to primary instances.
* Sync between active and passive replicas.
* Sharding - schema of table stays same, but split across multiple DBs.
* Indexing - uses metadata for faster performance.
* Sync/ async replication between multiple databases instances.

# Caching servers
* Faster reading from memory than from disk.
* Cache hit/ miss.
* TTL of cached data.
* Most accessed/ hot data is cached.
* Cache eviction
  * Prevents stale data.
  * TTL for cached data.
  * LRU/ LFU.
* Write through/ write back cache.
* Cache consistency.
* Redis, Memcached, etc.

# Storage considerations
* Block / Object / File.  
* Replication factor.
* Synchronous and async replication.
* Snapshot capabilities.
* Deduplication.
* Compression.
* Encryption.
* Hot / Cold / Archival.

# Message queues
* Kafka.

# Observability
* Open telemetry instrumentation in application code.

### Metrics
* Prometheus.
* Grafana. 
* Thanos. 
 
### Logs
* Loki. 
* Fluentd. 
* Fluentbit.

### Traces
* Tempo.
* Jaeger.

### Alerts
* Alert manager.

# Disaster recovery (DR) plans
* [Reference architecture in AWS](https://aws.amazon.com/blogs/architecture/disaster-recovery-dr-architecture-on-aws-part-i-strategies-for-recovery-in-the-cloud/)

# Backup

# Reporting/ analytics
* Hadoop.
* Spark.

# Search service
* Elastic Search.
* SOLR.

# CAP theorem

