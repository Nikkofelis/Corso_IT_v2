
```mermaid
flowchart TB
subgraph Apps
direction TB
	Store_Apps & UWP_apps & Desktop_apps
end

subgraph System_Service
direction TB
	Windows_RT_APIs & NET_Framework --- Executive_Services
end

Store_Apps & UWP_apps --> Windows_RT_APIs
UWP_apps & Desktop_apps --> NET_Framework

subgraph Operation_System_Kernel
direction TB
	Device_Drivers --- Windows_kernel
end

Executive_Services --- Device_Drivers

```

- Apps
- [[System Service]]
- Operating System Kernel

```ad-note
title: Driver

Library that instructs the kernel on service usage. Usually digitally signed through [Hashing](#Hashing), for latest devices.
```


Drivers are **architecture** specific:

- x86 drivers
- x64 drivers

Divided into:

- Setup information (.inf)
- DLLs (.sys)
- Catalogue (.cat)

The CPU architecture is determined by the type of **assembler** used.

```ad-note
title: Assembler

Low level language between High Level Language (compiler) and Machine Language (binary)
```

## Checking Hardware

Microsoft Assessment and Planning Toolkit (MAP) is a software that:
- Scans the network
- Locates all the computers on the network
- Checks hardware compatibility with Win 10
- Requires no agent on any client

## Active Directory
#TODO

```mermaid
flowchart TB
Computers & Users & Groups & Groups_Policy ---> Active_Directory
```
