# IPv4 Packet

- **Version**: Contains a 4-bit value (nibble) 
- **Internet header length (IHL)**: Shows the length of the header
- **Differentiated Services**: Manages the QoS
- **Total Length**: Header plus data field
- **Identification**: Code number of the packet
- **Flag**: Declare that can't be fragmented
- **Fragment Offset**: Code number of a specific fragment of a packet
- **Time-to-Live (TTL)**: Avoids layer 3 loops, indicates the max "hops" the packet can do between devices.
- **Protocol**: Identifies next level protocol.
- **Header Checksum**: 
- **Source IPv4 Address**: 32 bit
- **Destination IPv4 Address**: 32 bit

## Limitations

- **IPv4 address depletion** - IPv4 has a limited number of unique public addresses available.
- **Lack of end-to-end connectivity** - Network Address Translation (NAT) provides a way for multiple devices to share a single public IPv4 address. However, because the public IPv4 address is shared, the IPv4 address of an internal network host is hidden. This can be problematic for technologies that require end-to-end connectivity.
- **Increased network complexity** – While NAT has extended the lifespan of IPv4 it was only meant as a transition mechanism to IPv6. NAT in its various implementation creates additional complexity in the network, creating latency and making troubleshooting more difficult.

# IPv6 Packet

It weights 40 Bytes

8 groups of hexadecimal digits separated by `::`.

- **Version**
- **Traffic Class**: QoS
- **Flow Label**: 20 bit, suggests to packets with the same Flow Label to be handled in the same way by routers.
- **Payload Length**: Data field length
- **Next Header**: Indicates the data payload type.
- **Hop limit**: like TTL in IPv4
- **Source IPv6 Address**: 128 bit
- **Destination IPv6 Address**: 128 bit
