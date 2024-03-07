# Data Engineering

Notes and resources related to learning the fundamentals of data engineering.

## References

- [Fundamentals of Data Engineering](https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/)
- [Spark and Iceberg Quickstart](https://iceberg.apache.org/spark-quickstart/): Useful docker-compose
  setup to get up and running with a minimal Spark/Apache Iceberg setup.

## Data Engineering Lifecycle

As defined by "Fundamentals of Data Engineering":

_Turns raw data into useful end product for use by_:

- _Analysts_
- _Data Scientists_
- _ML engineers_

### Generation

- Origin of data, usually outside of control of data engineer.
- Typically a transactional database or IoT devices.
- Evaluation. Many key questions to consider:
  - What are the essential characteristics of the data source?
  - Is it an application? A swarm of IoT devices?
  - How is data persisted in the source system?
  - Is data persisted long term, or is it temporary and quickly deleted?
  - At what rate is data generated? How many events per second? How many gigabytes per hour?
  - What level of consistency can data engineers expect from the output data?
  - If you’re running data-quality checks against the output data, how often do data inconsistencies occur: nulls where they aren’t expected, lousy formatting, etc.?
  - How often do errors occur?
  - Will the data contain duplicates?
  - Will some data values arrive late, possibly much later than other messages produced simultaneously?
  - What is the schema of the ingested data? Will data engineers need to join across several tables or even several systems to get a complete picture of the data?
  - If schema changes (say, a new column is added), how is this dealt with and communicated to downstream stakeholders?
  - How frequently should data be pulled from the source system?
  - For stateful systems (e.g., a database tracking customer account information), is data provided as periodic snapshots or update events from change data capture (CDC)?
    What’s the logic for how changes are performed, and how are these tracked in the source database?
  - Who/what is the data provider that will transmit the data for downstream consumption?
  - Will reading from a data source impact its performance?
  - Does the source system have upstream data dependencies? What are the characteristics of these upstream systems?
  - Are data-quality checks in place to check for late or missing data?

### Storage

- Data architectures in the cloud tend to leverage several storage solutions
- Most storage solutions are not just storage but have query/transformation abilities too
- Runs across whole lifecycle
- Key questions to consider:
  - Is this storage solution compatible with the architecture’s required write and read speeds?
  - Will storage create a bottleneck for downstream processes?
  - Do you understand how this storage technology works? Are you utilizing the storage system optimally or committing unnatural acts? For instance, are you applying a high rate of   - random access updates in an object storage system? (This is an antipattern with significant performance overhead.)
  - Will this storage system handle anticipated future scale? You should consider all capacity limits on the storage system:
    - total available storage, read operation rate, write volume etc.
  - Will downstream users and processes be able to retrieve data in the required service-level agreement (SLA)?
  - Are you capturing metadata about schema evolution, data flows, data lineage, and so forth?
    Metadata has a significant impact on the utility of data. Metadata represents an investment in the future, dramatically enhancing discoverability and institutional knowledge to streamline future projects and architecture changes.
  - Is this a pure storage solution (object storage), or does it support complex query patterns (i.e., a cloud data warehouse)?
  - Is the storage system schema-agnostic (object storage)? Flexible schema (Cassandra)? Enforced schema (a cloud data warehouse)?
  - How are you tracking master data, golden records data quality, and data lineage for data governance? (We have more to say on these in “Data Management” on page 50.)
  - How are you handling regulatory compliance and data sovereignty? For example, can you store your data in certain geographical locations but not others?

- Temperature determined by data access frequency
  - Hot: most frequently accessed, many times a day/minute/second - stored for "fast" retrieval
  - Lukewarm: accessed less frequently, weekly/monthly
  - Cold: queried very infrequently and usually archival data

#### Concepts

- See general [storage](../storage/README.md)
- [Data lake](./data-lake.md)

#### Technologies

- [Minio](../storage/minio.md)

### Ingestion

#### Concepts

- [Open-Table Formats](https://opentableformat.github.io/)

#### Technologies

- [Apache Iceberg](./technologies/apache-iceberg.md)

### Transformation

### Serving
