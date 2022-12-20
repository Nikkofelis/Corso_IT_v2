- **Host firewall**: software installed in the device
- **Perimeter firewall**: divides and control the traffic from the local network from the external networks

# Host Firewall

Useful from mobile devices and local network threats. Doesn't need to decrypt the data (like a perimeter firewall).

Allows 3 profiles:

- **Public**
- **Private**
- **Domain**: automatically decided by the domain, when the latter is available.

```ad-note
title: Windows Connection Awareness

Verify the pairing of Subnet Mask, IP Gateway and MAC Gateway. When the system finds a new combination of these three addresses, it asks if the network is to be considered Private or Public. From this time forward, it will recognise the network as the chosen setting.
```

To configure the firewall, on run, use the command `wf.msc`.

# Perimeter Firewall

Type: 

- Packed filter: Layer 3-4, works on the IP address and Ports
- Application Level Gateway (ALG): Layer 7, confront the data with the expected pattern
- Unified Thread Management (UTM): as ALG, but with more digital signs
