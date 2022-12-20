# Installing

## Try Ubuntu

Launch the OS directly from the CD / .ISO without altering the hard-drive.

Useful for:

- Test the OS
- Use certain features from the virtual OS
- Access a device bypassing the original OS

## Partition

- Primary: first partition to be set
- Logical: partition of primary partition

### Formatting

The OS is formatted in Ext4.

### Mount Point

The **mount point** is the first location of the file hierarchy.

For the first partition, the root is `/`. At least one partition must start from the root `/`.

# File Systems

Standard File Hierarchy System (FHS) Unix

- `/bin`: essential command binary
- `/dev`: device files
- `/etc`: software configuration files
- `/home`: users' folders, user's configurations are listed here
- `/lib`: shared libraries between all or multiple software
- `/opt`: third parties software
- `/sbin`: essential system binary
- `/tmp`: temporary files, shared between users
- `/var`: variable data
	- `/var/cache`: 
	- `/var/log`: list of events on the device
