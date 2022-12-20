The purpose of the data link address is to deliver the data link frame from one network interface to another network interface ==on the same network==.

Data Link addresses are **physical**, and **they change at each hop** between devices.

# Fields

| Frame Format | Frame Fields                                 |
| ------------ | -------------------------------------------- |
| Header       | Frame Start<br>Addressing<br>Type<br>Control |
| Package      | Data                                         |
| Trailer      | Error Detection<br>Frame Stop                |

- **Frame start and stop**: Used to identify the beginning and end limits of the frame. The stop is optional.
- **Addressing**: Indicates the source and destination of the data. ==Destination NIC / Source NIC==
- **Type**: Identifies the layer 3 protocol.
- **Control**: (Optional) Identifies flow control like QoS.
- **Data**: Frame payload.
- **Error Detection**: (Optional) Scraps the data if damaged.

## Ethernet Frame

```ad-warning
title: Very Important
```

![Ethernet Frame FIelds](Ethernet%20Frame%20FIelds.png)

- Preamble and Start Frame Delimiter (SFD): Respectively 7 and 1 bytes
- Destination MAC Address
- Source MAC Address
- Type / Length: now used only for "type"
- Data
- Frame Check Sequences (FSC): used by the receiver to compare to the message sent

When a NIC receives a frame, it examines the destination MAC address. If the destination MAC address is the same of the device, it accept the message, otherwise it ignores it.
