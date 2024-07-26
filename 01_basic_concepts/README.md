Distributed systems are complex computing systems that consist of multiple autonomous components located on different nodes, communicating and coordinating with each other to achieve a common goal. Some key characteristics of distributed systems include:

* `Scalability` - should be able to handle large amounts of data and workloads by adding more nodes to the system.
* `Concurrency` - ability to process multiple requests or tasks simultaneously, improving overall system performance.
* `Consistency` - must ensure data consistency across all nodes. 
* `Fault tolerance` - systems can continue to function even if some nodes fail.
* `Availability` - systems should be highly available. 
* `Efficiency` - how well the system performs.
* `Security` - must be designed with security in mind to protect against various threats, such as data breaches, denial-of-service attacks, and unauthorized access.

Following are some of the key concepts and technologies involved in designing distributed systems.

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
* Backup solutions.
* [Reference architecture in AWS](https://aws.amazon.com/blogs/architecture/disaster-recovery-dr-architecture-on-aws-part-i-strategies-for-recovery-in-the-cloud/).
* [Backup and DR strategies for increased resilience in AWS](https://www.youtube.com/watch?v=E073XISxrSU&t=376s).

# Reporting/ analytics
* Hadoop.
* Spark.

# Search service
* Elastic Search.
* SOLR.

# CAP theorem
* [CAP Theorem Simplified](https://www.youtube.com/watch?v=BHqjEjzAicA&t=22s).

# Storage considerations
* Block / Object / File.  
* Replication factor.
* Synchronous and async replication.
* Snapshot capabilities.
* Deduplication.
* Compression.
* Encryption.
* HDD / SSD / NVMe.
* [RAID](https://www.youtube.com/watch?v=2Dovoc9LP34).
* [Erasure coding](https://www.youtube.com/watch?v=Q5kVuM7zEUI).
* Hot / Cold / Archival.

# Network considerations
* NIC teaming/ bonding.
* Spine-Leaf vs traditional architecture.
* Type of network swtiches.
* Type of network interface cards, cables, and interconnects.
* Dell VLT and Cisco VPC.
* Routing protocols (BGP, OSPF, etc.).
* RDMA.

# Compute considerations
* Baremetal / Virtualization / Containerization. 
* Serverless.

# Microservices architecture and Kubernetes
* Microservices architecture provides the business logic and functionality.
* Kubernetes provides the platform for deploying and managing those microservices in a distributed environment.
* Some of the key [non-functional design considerations for a Kubernetes cluster are explained here](https://github.com/vineethac/Kubernetes/tree/main/k8s-nfr-design-considerations).

# On-premises vs cloud vs hybrid infrastructure
* The choice between on-premises, cloud, and hybrid depends on an organization's specific needs, budget, and business requirements.

