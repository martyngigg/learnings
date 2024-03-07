# Apache Iceberg

<https://iceberg.apache.org/>

- Open-table specification and libraries.
- Open source.
- Treat data lake as database tables rather than just a collection of files.
- Maintain data in place and avoid moving.
- Unify batch, streaming and ad-hoc.
- Schema evolution.
- Partition evolution: Update partitions without having to rewrite old data.
- Hidden partitioning: Partition based on a transformed value and not only data directly in the table columns as with things Hive.
- Snapshots and time travel.
- Multi-engine support: Trino, Spark...
- Kafka sink connector available.
- Catalog adds support for ACID transactions.
