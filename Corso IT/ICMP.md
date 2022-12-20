**Destination**: either unicast, multicast or broadcast
**Methods**: echo-request and echo-reply

Called by the command `ping` or `tracert` (windows).

# Trace Route

```prompt
C:\> tracert -d ADDRESS

1	x ms	x ms	x ms	DEFAULT GATEWAY ADDRESS
2	x ms	x ms	x ms	ADDRESS
3	x ms	x ms	x ms	ADDRESS
4	x ms	x ms	x ms	DESTINATION ADDRESS
```

`tracert` sends a series of ICMP messages with an incremental TTL number to discover all the routers on the way to the receiver.
Each time a message reaches 0 on the TTL, the last router that received the message sends an error message with its IP address to populate the table of `tracert`.

Each probe is sent with 3 instances.

A `*` in a time column shows a missing reply from a device.

