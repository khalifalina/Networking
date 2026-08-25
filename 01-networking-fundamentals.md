# Networking Fundamentals

## What is Computer Networking?

A computer network connects devices so they can communicate and share information and resources.

### Why networking matters

Networking is fundamental to modern infrastructure and DevOps because it enables:

- Communication between devices, servers and applications
- Resource sharing
- Application connectivity and data transfer
- Infrastructure management
- Application deployment and updates
- Troubleshooting, monitoring and performance optimisation

---

## Types of Networks

### LAN — Local Area Network

A LAN covers a relatively small geographical area.

Examples:

- Home network
- Office network
- University network

Devices within a LAN can communicate and share resources.

### WAN — Wide Area Network

A WAN covers a much larger geographical area.

Examples:

- Networks spanning cities or countries
- The Internet

A WAN can connect multiple LANs together.

---

## Key Networking Components

### Router

A router connects different networks and directs traffic between them.

**Main purpose:**

- Connect different networks
- Determine where traffic should be forwarded

### Switch

A switch connects devices within the same network, particularly within a LAN.

**Main purpose:**

- Connect devices
- Manage data flow within a LAN

### Firewall

A firewall protects a network by monitoring and controlling network traffic.

**Main purpose:**

- Prevent unauthorised access
- Control incoming traffic
- Control outgoing traffic

---

# IP Addressing

An IP address is a unique identifier used to identify devices on a network and enable communication.

## IPv4

IPv4 uses a 32-bit address.

Example:

```text
192.168.0.5
```
Each section represents 8 bits.

## IPv6

IPv6 uses a 128-bit address.

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

## MAC Addresses

A MAC (Media Access Control) address is a unique identifier assigned to a network interface.

```text
00:1A:2B:3C:4D:5E
```

### Key characteristics
- 48-bit address
- Used at the Data Link layer
- Identifies network interfaces
- Important for communication within a local network

# Ports and Protocols

## Ports

A port acts as a logical endpoint for network communication.
Applications use ports to communicate over a network.

## Protocols

A protocol is a set of rules that defines how data is transmitted between devices.
Protocols allow devices and applications to communicate using agreed-upon rules.

# TCP

TCP stands for Transmission Control Protocol.

## TCP is:
- Connection-oriented
- Reliable
- Based on a handshake
- Able to provide error checking
- Able to provide flow control
- Designed to deliver data in order

TCP is useful when reliable communication is required.

## TCP Use Cases:
- Web browsing
- Email
- File transfer
- Bidirectional communication

# UDP
UDP stands for User Datagram Protocol.

## UDP is:
- Connectionless
- Fast
- Less reliable than TCP
- Does not require prior communication
- Does not guarantee delivery
- Does not guarantee packet ordering

## UDP Use Cases:
- Video streaming
- Online gaming
- DNS
- VPN

Both TCP and UDP operate at Layer 4 — the Transport Layer of the OSI model.
