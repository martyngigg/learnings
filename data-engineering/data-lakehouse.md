# Data Lakehouse

<https://www.databricks.com/glossary/data-lakehouse>

The lakehouse seeks to provide database-like interactions and guarantees on top of
data lake instead of simply managing a collection of files in object buckets/containers.

## Lakehouse table formats

<https://opentableformat.github.io/>

- [Apache Iceberg](https://iceberg.apache.org/)
- [Apache Hudi](https://hudi.apache.org/)
- [Delta Lake](https://delta.io/)

### Data partitioning

A fundamental question when loading data from sources systems into the lakehouse
is how to partition the data. There is no one-size fits all option as it is
highly dependent on the query patterns and there are always trade offs.
See <https://www.youtube.com/watch?v=-Q4UcXcIv1o> for an overview of how
Netflix deal with partitioning streaming data.
