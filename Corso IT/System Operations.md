# Windows File System

Multiple roots (unlike Linux OS).

```Explorer
/Programms:        
/Programms (x86): 
/Users:           
/Windows
```

# Performance Evaluation

Find the process which is slowing the system

## Resource Monitor

### CPU

If either the % is too high (>90%) or the CPU core partition is high, the issue is in the CPU.

### Memory

The safe threshold is <90%

### Disk

- Coda <= 1: safe load
- Coda > 1: too much load on the disk
	- Slow write speed -> disk issue

### Network

- Ethernet: too much load -> NIC issue
- TCP Connections: too much load could indicate a virus