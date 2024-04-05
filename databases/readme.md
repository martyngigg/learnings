# Databases

## Relational

- [Postgres](https://www.postgresql.org/)
- [MySQL](https://www.mysql.com/):
  - JSON stored as binary
- [MariaDB](https://mariadb.org/):
  - Fork of MySQL after MySQL acquired by Oracle.
  - JSON stored as string

## Analytical

- [StarRocks](https://www.starrocks.io/)
  - New analytical database aiming for querying raw data directly within a
    lakehouse instead of having to maintain complex transformation pipelines.

## Federated Query Engines

Query large datasets across multiple sources using ANSI SQL.

- [Presto](https://prestodb.io)
  - Formerly PrestoDB
  - Developed at Facebook to serve data at Facebook's hyperscale.
- [Trino](https://trino.io/)
  - Formerly PrestoSQL
  - Fork of Presto when original developers left Facebook.
  - Trino developed to serve a broader audience, not just hyperscale companies
- [StarRocks](https://www.starrocks.io/)
  - Able to serve as just query engine as part of a lakehouse architecture, e.g
    query Iceberg tables stored in an object store.
