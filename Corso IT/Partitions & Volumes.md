# Partition

Division of a single disk into multiple sectors.

- **Master Boot Record (MBR)**: Counts from the beginning of the disk.
- **Guide Partition Table (GPT)**: More recent and reliable. Only for Win x64 e UEFI.

# Volume

Memory allocation visible to the computer. A volume can include multiple partitions.

It need to be [formatted](File%20Systems.md) -> archive method defined by the file system

# Disk Manager

Tool to manage the disks, volumes and partitions.

Disks can be set on:

- **Simple**: single volume
- **Spanning**: sequentially fills the volume from the first up to the last
- **Mirroring**: clone a volume into a target one
- **Striping**: alternately fills the volume [RAID](RAID.md)
