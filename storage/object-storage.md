# Object Storage

- Files stored on distributed shards with metadata, object ID and additional
  attributes.
- Reassembled on request.
- Unlimited metadata (depending on the provider).
- Files can be versioned.
- Unlimited scalability.
- Accessed via REST API.
- Searchability is good due to rich metadata.
- REST API offers low overhead access.
- Peformance is largely network and disk bound. Adding new storage does not
  require additional CPU/RAM capacity to cope.
- Can use off the shelf hardware.
- Erasure coding for redundancy.

## Examples

- Documents/File share: Can have a file-like access layer to be treated as file share.
- Websites can be fully hosted as everything accessed over https.
- Backup and tape replacement
