# OSI Model

The OSI Model stands for **Open Systems Interconnection Model**.

It provides a standard way of understanding how communication happens across a network.

The OSI model contains **7 layers**.

---

# Why Do We Need a Communication Model?

A communication model provides a standard structure for networking.

### Benefits

#### Decoupled Innovation

Innovation can happen within individual layers without affecting the entire networking system.

#### Simplified Network Equipment Management

A standard model makes it easier to understand and manage network equipment.

#### Application Independence

Applications do not need to understand the underlying physical network.

For example, an application should not need a different version depending on whether the network uses:

- Wi-Fi
- Ethernet
- Fibre

---

# The 7 OSI Layers

| Layer | Name | Main Concept | Examples |
|---|---|---|---|
| 7 | Application | End user | HTTP, FTP, SSH, DNS |
| 6 | Presentation | Data representation | SSL, SSH, JPEG, MPEG |
| 5 | Session | Session management | APIs, Sockets |
| 4 | Transport | End-to-end connections | TCP, UDP |
| 3 | Network | Packets and routing | IP, ICMP |
| 2 | Data Link | Frames and local communication | Ethernet, PPP |
| 1 | Physical | Physical transmission | Fibre, Wireless, Cables |

---

# Layer 1 — Physical Layer

The Physical Layer is responsible for transmitting raw bits over a physical medium.

### Components

- Cables
- Network interface cards
- Physical networking equipment
- Fibre
- Wireless
- Hubs
- Repeaters

### Data Unit
```text
Bits
```

# Layer 2 — Data Link Layer

The Data Link Layer provides node-to-node data transfer.

It ensures that data is transferred correctly between adjacent network nodes.

It can also detect and potentially correct errors originating at the Physical Layer.

## Key Components
- MAC addresses
- Ethernet
- PPP
- Switches
- Bridges

### Example:
#### MAC Address: 
```text
00:1A:2B:3C:4D:5E
```
#### Data Unit:
```text
Frames
```

# Layer 3 — Network Layer

The Network Layer determines how data is sent to its destination.

It manages packet forwarding and routing through intermediate routers.

## Key Components
- IP addresses
- Routers

### Example:
#### IP Address:
```text
192.168.0.5
```
## Protocols
- IP
- ICMP
- IPSec
- IGMP
### Data Unit:
```text
Packets
```

# Layer 4 — Transport Layer

The Transport Layer provides end-to-end communication.

## It is responsible for:
- Reliable data transfer
- Segmenting data
- Reassembling data
- Communication between endpoints

## Protocols:
- TCP
- UDP
- Data Unit
- Segments

# Layer 5 — Session Layer

The Session Layer manages sessions between applications.

## Functions
- Establishes sessions
- Maintains sessions
- Terminates sessions
- Synchronises communication
  
## Components
- APIs
- Sockets
- Winsock

# Layer 6 — Presentation Layer

The Presentation Layer translates data between the application and network formats.

It ensures that data is in a usable format.

## Functions: 
- Data formatting
- Data translation
- Encryption

## Examples
- SSL
- SSH
- IMAP
- FTP
- MPEG
- JPEG

# Layer 7 — Application Layer

The Application Layer provides network services directly to applications.

It is the layer closest to the end user.

## Examples:
- HTTP
- FTP
- IRC
- SSH
- DNS
- SMTP

# TCP/IP Model

The TCP/IP model contains four layers:

1. Application Layer
2. Transport Layer
3. Internet Layer
4. Network Access Layer

| TCP/IP Layer   | Examples               |
| -------------- | ---------------------- |
| Application    | HTTP, TLS, DNS         |
| Transport      | TCP, UDP               |
| Internet       | IP                     |
| Network Access | Ethernet, Wireless LAN |

