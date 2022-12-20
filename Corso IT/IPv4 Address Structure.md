An IPv4 address is a 32-bit hierarchical address.

|   192.168.10.   |      10      |
| :-------------: | :----------: |
| Network Portion | Host Portion |

# Subnet Mask

Identifies the network portion and the host portion.

Each 255 value on a mask identifies the **network portion**. Each 0 value the **host portion**. In a subnet mask, the 1s must ==always== be on the left of the 0s.

It must be configured only on local devices.

# Prefix Length

```ad-abstract
The prefix length is the number of bits set to 1 in the subnet mask. It is written in “slash notation”, which is noted by a forward slash (/) followed by the number of bits set to 1. Therefore, count the number of bits in the subnet mask and prepend it with a slash.
```

Indicates how many 1s are present on a subnet mask. Every bit in a subnet mask with a '1' indicates the fixed bits that a IP Address can't be variable.

| Subnet Mask   | 32-bit Address                      | Prefix length |
| ------------- | ----------------------------------- | ------------- |
| 0.0.0.0       | 00000000.00000000.00000000.00000000 | /0  |
| 255.0.0.0     | 11111111.00000000.00000000.00000000 | /8  |
| 255.255.0.0   | 11111111.11111111.00000000.00000000 | /16 |
| 255.255.255.0 | 11111111.11111111.11111111.00000000 | /24 |

# Determining the Network: Logical AND

Logical AND is the comparison of two bits that produce the results shown below.

The Network Address and the Directed Broadcast can't be assign to a host.

# Examples

## Example 1: Full conversion

**IP Address**: 192.168.10.11
**Subnet Mask**: 255.255.225.128

| Type                       | 1st byte | 2nd byte | 3rd byte | 4th byte  | Action                                    |
| -------------------------- | -------- | -------- | -------- | --------- | ----------------------------------------- |
| IP Address                 | 11000000 | 10101000 | 00001010 | 0 0001011 | Conversion<br>in binary                   |
| Subnet Mask                | 11111111 | 11111111 | 11111111 | 1 0000000 | Conversion<br>in binary                   |
| Network address            | 11000000 | 10101000 | 00001010 | 0 0000000 | AND bit-a-bit                             |
| First Usable<br>Host (FuH) | 10000000 | 10101000 | 00001010 | 0 0000001 | The next possible<br>address              |
| Last Usable<br>host (LuH)  | 10000000 | 10101000 | 00001010 | 0 1111110 | All variable bits <br>(but the last) as 1 | 
| Directed<br>Broadcast (BC) | 10000000 | 10101000 | 00001010 | 0 1111111 | All variable bits as 1                    |

## Example 2: Hybrid Conversion

192.168.160.64 /19 = /8+8+3+0

192          .168          .10100000.01000000	IP Address
11111111.11111111.11100000.00000000	Subnet mask (binary)
255          .255          .11100000.00000000	Subnet mask (hybrid)

192.168.10100000.00000000 = 192.168.160.0		Network Address
192.168.10100000.00000001 = 192.168.160.1		FuH
192.168.10111111.11111110 = 192.168.191.254	LuH
192.168.10111111.11111111 = 192.168.191.255	Broadcast

# Exercise

Net 1
120.80.40.135 /25 /8+8+8+1
120.   80.  40.10000111
255.255.255.10000000	255.255.255.128 mask
120.  80.  40.10000000	120.80.40.128	network address
120.  80.  40.10000001	120.80.40.129	FuH
120.  80.  40.11111110	120.80.40.254	LuH
120.  80.  40.11111111	120.80.40.255	broadcast

135-128=7-4=3

Net 2
100.10.4.240 /22 /8+8+6+0
100.  10.00000100.11110000
255.255.11111100.00000000	255.255.252.0 mask
100.  10.00000100.00000000	100.10.4.0		network
100.  10.00000100.00000001	100.10.4.1		FuH
100.  10.00000111.11111110	100.10.7.254	LuH
100.  10.00000111.11111111	100.10.7.255	Broadcast


240-128=112-64=48-32=16
255-3=252
