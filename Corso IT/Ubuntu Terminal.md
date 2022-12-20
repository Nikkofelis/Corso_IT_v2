TAB single tap: completes the current command
TAB double tab: shows the possible next command

- **Absolute Path**: Start from the root directory (`/home/user/`)
- **Relative Path**: Start from the current directory (`user/`)

## Shell Expansions

`?`: a single character
`*`: any number of characters (0-n)

## Basic Commands List

`..`: identifies the parent directory of the current one
`apt`: command-line package manager
	`apt install [packet name]`: download and 
	`apt search [packet name]`: search in the packet manifest the searched name
	`apr update`: updates the list of available packets
`cat`: concatenate files and print them in plain text
`cd`: change current directory (default: home directory)
`chmod [mode] [file name]`: change file authorisations
	i.e. `ugmod UG+rw file1`: grants read and modify (owner and group) to file1 (see [Metadata](Users%20and%20Authorisations.md#Metadata) for more details)
`chown [user][:[group]] [file name]`: change file owner and group
`clear`: clear the terminal screen
`groupadd`: create a new group
`history`: print the list of used commands
`ls`: list content of a directory (default: current directory)
`man [command]`: shows the manual of a command
`mkdir [dir.name]`: create a directory (default: current directory)
`nano [file.name]`: file editor, can modify or create a new file
`passwd [user name]`: change user's password
`pwd`: print working directory
`rm [file name]`: remove file
	`rm -r [directory name]`: remove directory and content
`su [user name]`: switch user, requires name and password of the target user
`sudo [command]`: do as super user, run a single command with root privilege
`tree [directory]`\*: print the tree from that directory
`touch [file.name]`: modifies a file timestamp (default: create a new file)
`useradd [user name]`: creates a new user
`usermod`: modifies a user account

\* Requires packet installation (see command `apt`)

```ad-warning
title: Remember

When using the `help` function of a command, the ALLCAP name is the required input.
If no ALLCAP is present, the Option doensn't require any.
```
