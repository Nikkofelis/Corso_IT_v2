Redundancy: RAID

```ad-note
title: Hardware RAID

Usage of a device that manages multiple disks to provide to a PC (**Controller**). The PC will see all of these disks as one.
```

```ad-note
title: Software RAID

The PC itself manages multiple disks.
```

```ad-warning
RAID is not a [Backup](Backup.md) system.
```

Provides either speed or security

# Levels

0. **Striping**: Divides the data. *Speed*.

```mermaid
flowchart LR
RAID("Data: 12345678") --- Disk1("1357") & Disk2("2468")
```

1. **Mirroring**: Clones a disk. *Security*.

```mermaid
flowchart LR
RAID("Data: 12345678") --- Disk1("12345678") & Disk2("12345678")
```

5. **Parity**: Divides the data between multiple disks alongside the function XOR. *Speed and Security*.

```mermaid
flowchart LR
RAID("Data: 12345678") --- Disk1("13P7") & Disk2("2P58") & Disk3("P46P")
```

6. **Dual Parity**: Like **Parity** but with two parity disks. *Speed and Security*.

```mermaid
flowchart LR
RAID("Data: 12345678") --- Disk1("13PP") & Disk2("2PP5") & Disk3("PP67") & Disk4("P48P")
```

10. **Strip Mirror**: Two pairs of **Mirror** disks in **Striping**. *Speed and Security*.

```mermaid
flowchart LR
RAID("Data: 12345678") --- 0("RAID 0") 
0 --- 1("RAID 1") & 2("RAID 1")
1 --- Disk1("1357") & Disk2("1357")
2 --- Disk3("2468") & Disk4("2468")
```

50. : Clusters of 3 **Parity** disks in **Striping**. *Speed and Security*.

```mermaid
flowchart LR
RAID("Data: 12345678") --- 0("RAID 0")
0 --- 1("RAID 5") & 2("RAID 5")
1 --- Disk1("1P8") & Disk2("25P") & Disk3("P5P")
2 --- Disk4("3PP") & Disk5("46P") & Disk6("P7P")
```

60. : Cluster of 4 **Dual Parity** disks in **Striping**. *Speed and Security*.

```mermaid
flowchart LR
RAID("Data: 12345678") --- 0("RAID 0")
0 --- 1("RAID 6") & 2("RAID 65")
1 --- Disk1("1P8") & Disk2("25P") & Disk3("P5P") & Disk4("3PP")
2 --- Disk5("46P") & Disk6("P7P") & Disk7 & Disk8
```

| RAID | Min Disks | Max Disks  |    Volume    |      Fault Tolerance      |
|:----:|:---------:|:----------:|:------------:|:-------------------------:|
|  0   |     2     |     2      |   disk * 2   |             1             |
|  1   |     2     |     2      |     disk     |             -             |
|  5   |     3     |    inf     | disk * (n-1) |             1             |
|  6   |     4     |    inf     | disk * (n-2) |             2             |
|  10  |     4     |     4      |   disk / 2   | 2 (not in the same group) |
|  50  |     6     | inf (even) | disk * (n-3) |                           |
|  60  |     8     | inf (even) | disk * (n-4) |                           |




