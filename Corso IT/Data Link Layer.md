7. Application
6. Presentation
5. Session
4. Transport
3. Network
2. -> **Data link**
1. Physical

Is responsible for network interface card (NIC) to network interface card communications. Is the last ==hardware dependent== layer.

The data link field is the [Frame](Frame.md). The overhead is greater for wireless connections.

# Functions

- Accept and encapsulate layer 3 packets
- Provide media access control and error detection

# Sublayers

- **Logical Link Control (LLC) Sublayer**: It ==places information in the frame==. It labels the data. It is usually the NIC driver.
- **Media Access Control (MAC) Sublayer**: It is responsible for ==data encapsulation== and ==media access control==. It ==provides data link layer addressing== and it is integrated with various physical layer technologies.
	- Ethernet (IEEE 802.3): cable link
	- WLAN (IEEE 802.11): wireless communications
	- WPAN (IEEE 802.15): Bluetooth, RFID, etc.

During the transmission, the Frame (the header and the trailer, NOT the internal Package) changes based on the physical media used.

# Topologies

## LAN

- **Star**: full duplex
- **Extended Star**: full duplex
- **Bus** (legacy): half duplex
- **Ring** (legacy): token

## WAN

- Point-to-Point (PPP)
- Hub and Spoke (equivalent to star)
- Mash (all devices connected to each other)

```ad-note
title: Half Duplex

Double senses communication, non simultaneous.
```

```ad-note
title: Full Duplex

Double sense communication and simultaneous.
```

## Access Control Network

### Contention-Based Access

All in half-duplex

- **Contention-Based Access - CSMA/CD**: collision detection, it detects collisions through difference of tension
	- Bus topology (legacy)
	- Ethernet hub (legacy)
- **Contention-Based Access - CSMA/CA**: collision avoidance, the end devices sends also a RTS (ready-to-send) along with the frame to request the network usage, the access point (if the network is free) sends back a CTS (Clear-to-send) signal
	- WLAN

### Controlled Access

- Token ring (legacy)
- ARCNET (legacy)
