# Characteristics

- Security
- Quotas: Limitation of data per user

# Formatting

## Resilient File System (ReFS)

## New Technology File System (NTFS)

Transaction Log: Creates logs of the on-going operations
Compression
Security/Encryption

## File Allocation Table (FAT)

Less overhead of ReFS and NTFS
Compatible with everything
Often used with removable media
No Security service

## Extended File Allocation Table (exFAT)

- Microsoft file system
- Optimised for flash drives
- No security service

# Permissions

The user's database can be stored:

- **[Internally](Local%20Users%20and%20Groups.md)**: into SAM files
- **By Domain**: in Active Directory (AD)

User are identified by file **SID**. The **SID** file contains the permissions for the user (create, read and modify files).

User can also be defined by groups ==to simplify permissions and to implement inheritance==.

```ad-note
title: Inheritance

The permissions of a specific folder are **inherited** by all the child folders.
This can be interrupted through inheritance interruption:

- Copy: modify existing permissions.
- Remove: delete all permissions (risky).

```

# Windows Registry

To view the file registry use the run application with the command `regedit`.

## Pros

- The registry use the same format.
- The backup is simpler than .INI files.
- Registry files are rarely damaged.
- User settings and device settings are separated.

## Cons

- A damaged registry can be usually solved only by re-installing the OS.
- Manipulating the registry is risky.
- Il backup can be done only by apposite tools.