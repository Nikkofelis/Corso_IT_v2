128-bit length address.

Not compatible with IPv4

# Representation (hexadecimal)

16-bit (2 Bytes) Hextets

|  X   |  X   |  X   |  X   |  X   |  X   |  X   |  X   |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 0000 | 0000 | 0000 | 0000 | 0000 | 0000 | 0000 | 0000 |
|  to  |  to  |  to  |  to  |  to  |  to  |  to  |  to  | 
| ffff | ffff | ffff | ffff | ffff | ffff | ffff | ffff |

## Hextet Form (binary)

| 0000 | 0000 | 0000 | 0000 |
|:----:|:----:|:----:|:----:|
|  to  |  to  |  to  |  to  |
| 1111 | 1111 | 1111 | 1111 |

[[How to represent IPv6]]

# Special IPv6 Addresses

0:0:0:0:0:0:0:1 = ::1 -> Local Host
FF02::1 -> Broadcast to all hosts in the local network
FF02::2 -> Multicast to all routers

# Types

- **[[Unicast IPv6]]**: uniquely identifies an interface on an IPv6-enabled device.
- **Multicast**: to send a single IPv6 packet to multiple destinations. For IPv6, the multicast is processed by the NIC. A special case of Multicast is an all-nodes multicast (same function of broadcast). All multicast addresses starts by FF...::
- **Anycast**: any IPv6 unicast address that can be assigned to multiple devices.

# Prefix Length

The subnet mask can only be represented in **Prefix Length**, and it can range from 0 to 128, the most used is the /64. This is because stateless address auto-configuration (SLAAC) uses 64 bits for the Interface ID. It also makes subnetting easier to create and manage.

|    Prefix    | Interface ID |
|:------------:|:------------:|
| 2001:bd8:a:0 |   0:0:0:0    | 

2001:bd8:a:: /64

# [[Router Configuration for IPv6]]
