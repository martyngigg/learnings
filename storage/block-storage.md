# Block Storage

- Data is treated as fixed size blocks.
- Block size can be adjusted to suit the hardware.
- Files are spread over multiple blocks.
- Blocks can be spread out and do not need to be stored together.
- Limited metadata.
- Requires a filesystem (xfs, ntfs, ext4) on top and whatever overhead it adds.
- Typically requires expensive hardware redundancy in a RAID configuration.

## Examples

- Databases typically use block storage, where the block size can be configured.
- VM disks:boot volumes, local storage.
- Shared volumes, single writer/multiple readers
- Backups
