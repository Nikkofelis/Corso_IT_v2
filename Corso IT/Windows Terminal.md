# Prompt

- **Absolute Path**: Start from the root directory (`C:\Users\user\`)
- **Relative Path**: Start from the current directory (`user\`)

The standard output is the screen, but it can be changed (i.e. on a file) through the symbol:
- `>` to substitute the content
- `>>` to add to the content

````ad-example
```cmd
C:\Users\user\Desktop> echo "text" > "filename.txt"
```
````

## Special Characters

`[command] /?`: command guide
`?`: a single character
`*`: any number of characters (0-n)
`%VARIABLE.NAME%`: call an environment variable

## Command List

`..`: identifies the parent directory of the current one
`arp`: shows the ARP table
`cd`: change directory
`cls`: clear the prompt screen
`copy [source file] [destination directory or file]`: copy a file into a new location/file
`del [file]`: remove a file
`dir`: list content of a directory (default: current directory)
`echo [text] [destination file]`: print messages or activate/deactivate command repetition (can be used to create files)
`help`: shows all available commands
`md [directory]`: create a directory (default: current directory)
`net [start/stop] "[service name]"`: starts or stops a service
`nslookup`: 
`rd [directory]`: remove a directory
`Robocopy.exe [source directory] [destination directory]`: tool to efficiently copy files and directories
`set`: shows, set or modify environment variables for cmd.exe
`shutdown`: power off the machine

### Robocopy.exe

Incrementally transfer files

`/MIR`: clone two folders
`/W`: waiting time between attempts
`/R`: how many attempts
`/LOG`: shows the logs of the last operation

## Logical Functions

### FOR

`FOR %[parametre] IN ([set]) DO [command]`

`FOR /L %[parametre] IN ([start],[increment],[stop]) DO [command]`

For multiple commands, include all commands between ( ).

## Scripting

A text file .bat (batch) can carry a prompt script. By running it, it will execute the listed commands.

The command `@echo off` disables the command line, showing just the output.

Everything written after `REM` will comment off all afterwards.

```ad-warning
The Parametres in .bat files must follow the symbol `%%`. NOT `%` as in the cmd.
```

# PowerShell
