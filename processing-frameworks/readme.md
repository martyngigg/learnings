# Processing Frameworks

- [Beam](https://beam.apache.org/)
  - Designed with unification of batch/stream in mind
  - Pipeline API in Java, Python and others
  - Same pipeline code runs on batch/streaming data
  - Build graphs of transformations
  - Streaming data broken down into windows (batch just one global window)
- [Dask](https://github.com/dask/dask)
  - Parallel computing with task scheduling
  - "Dask on Ray" can use scheduler from Ray on Dask task graph
- [Ray](https://github.com/ray-project/ray)
  - Framework for scaling AI and Python applications
  - Core for distributed computing
  - Toolkit libraries for ML applications
- [Spark](https://spark.apache.org/)
  - Supports batch operations as well as as streaming
  - Streaming is handled by Spark Streaming but this is actually
    microbatching and not true streaming.
  - Familiar DataFrame-style APIs
  - Support for SQL, Python, Scala
  - Support for ML
