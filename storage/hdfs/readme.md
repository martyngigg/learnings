# Hadoop Distributed File System  (HDFS)

<https://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-hdfs/HdfsDesign.html>

- Distributed file system designed to run on commodity/low-cost hardware.
- Supports traditional, hierarchical file organization.
- Files stored as a sequence of blocks replicated across a cluster for fault
  tolerance.
- Distributed as part of the larger [Hadoop](https://hadoop.apache.org/) framework
  for distributed processing.
- Typically used as the storage system for "big data" projects such as data lakes,
  however more recently object storage has started to become the preference
  in this space.
