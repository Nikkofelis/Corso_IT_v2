Some IPv4 addresses cannot be used to go out to the internet, and others are specifically allocated for routing to the internet.

```ad-warning
Remember
```

These are the ranges for private IP Addresses:

| Network Address and Prefix | RFC 1918 Private Address Ranger |
| -------------------------- | ------------------------------- |
| 10.0.0.0 /8                | 10.0.0.0 - 10.255.255.255       |
| 172.16.0.0 /12             | 172.16.0.0 - 172.31.255.255     |
| 192.168.0.0 /16            | 192.168.0.0 - 192.168.255.255   | 

NAT translate the private IP Address into public IP Address by paying a service provider.

The boundary routers (the routers at the boundary of a private network) translate the private IP in public one.

# Special Addresses

- **Loopback Address**: 127.0.0.0 /8, used for send messages to the source device.
- **Self address**: 127.0.0.1 /8
- **Link-Local Addresses**: 169.254.0.0 /16, **APIPA** self-assigns an IP Address to the device. They are used by a Windows DHCP client to self-configure in the event that there are no DHCP servers available. Same IP assignment is resolved by sending an ARP that must not receive response -> this will means that no other device (in that network) has the same IP.

# Classful Addressing (Legacy)

- **Class A**: 0.0.0.0 /8 - 127.0.0.0 /8
- **Class B**: 128.0.0.0 /16 - 192.255.0.0 /16
- **Class C**: 192.0.0.0 /24 - 223.255.255.0 /24
- **Class D**: 224.0.0.0 - 239.0.0.0
- **Class E**: 240.0.0.0 - 255.0.0.0




