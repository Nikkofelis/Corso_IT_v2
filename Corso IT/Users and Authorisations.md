# Users

Single admin user (**root user**) special permissions:

- Install programs
- Access file systems
- Change permission to directory
- Create and manage users

Root user is automatically created, but without credentials, at the OS installation.

## User Creation

Can be done either from the GUI or from the [Terminal](Ubuntu%20Terminal.md) by the command `useradd`.

The list of users is located in `/etc/passwd` Each user has:

- Name
- ID
- Group ID
- Root location
- Shell location (default: `/bin/bash`)

The passwords are located into the file `/etc/shadow`. The symbol `!` indicates an absence of password.

# Groups Management

To create a new group, use the command `groupadd`.

To change a user group, use the command `usermod` (see [Ubuntu Terminal](Ubuntu%20Terminal.md)).

The file containing all groups and relative users is located in `/etc/group`.

# Authorisations

Every file is described by an i-node.

The metadata of a file includes:

- Owner user
- Owner group
- 12 bits to identify authorisations

Authorisations are changed by the command `chmod`. 

## Metadata

Each file contains some metadata, shown by the command `ls -l`

| Authorisations | User Owner | Group | Data Stamp   |
| -------------- | ---------- | ----- | ------------ |
| drwxr-xr-x     | user       | user  | dic 12 12:15 |

The authorisation field includes, separated by `-` (all users can be indicated by `a`):

- Owner authorisations (u)
- Group authorisations (g)
- Other users authorisations (o)

The letter identifies the operation available:

- r: Read
- w: Modify
- x: Execute

# Owners

The file owner is the user who created a file or directory. The owner has special authorisations over a certain file (see [Metadata](#Metadata)).