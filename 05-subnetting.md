# Subnetting

## What is Subnetting?

Subnetting is the process of dividing a network into smaller networks called subnets.

### Benefits

- Improves network management
- Improves network efficiency
- Organises networks into smaller sections
- Determines network and host portions of an IP address

---

# CIDR Notation

CIDR stands for **Classless Inter-Domain Routing**.

CIDR notation uses:

```text
IP_address/prefix_length
```
## Example:
```text
192.168.1.0/24
```
The /24 indicates the network prefix length.

---

# Subnet Masks

A subnet mask defines the network and host portions of an IP address.

## Example:
```text
255.255.255.0
```
This is equivalent to:
```text
/24
```

---

# Example: 192.168.1.0/24

## Network:

192.168.1.0/24

## Subnet mask:

255.255.255.0

## Usable IP range:

192.168.1.1 - 192.168.1.254

---

# Binary Basics

Binary is a base-2 number system.

## It uses only:

0
1

Binary is fundamental to computer networking because IP addresses and subnet masks can be represented in binary.

---

# Binary Place Values

An 8-bit binary number has the following place values:

```text
128 64 32 16 8 4 2 1
```

## Example:
```text
11001010
```
Each position represents a power of 2.

---

# Binary and IP Addresses

IPv4 addresses contain 32 bits divided into four 8-bit sections.

## Example:

```text
192.168.1.1
```
can be represented in binary.

Subnet masks can also be represented in binary.

# Example:
```text
255.255.255.0
```

---

# Calculating Subnets

## Subnet calculations determine:

1. Number of subnets
2. Subnet mask
3. Network addresses
4. Broadcast addresses
5. Host ranges

## General Process
1. Determine the required number of subnets.
2. Calculate the required prefix length.
3. Determine the subnet mask.
4. Determine the network addresses.
5. Determine the broadcast addresses.
6. Determine the usable host ranges

---
# Example: /24 Split into 4 Subnets

## Starting network:
```text
192.168.1.0/24
```

To create four subnets, the network can be divided into /26 networks.

## The resulting networks are:

```text
192.168.1.0/26
192.168.1.64/26
192.168.1.128/26
192.168.1.192/26
```

---

# Host Ranges

## Example:
```text
192.168.1.0/26
```

## Network address:
```text
192.168.1.0
```
## Usable host range:
```text
192.168.1.1 - 192.168.1.62
```

## Broadcast address:
```text
192.168.1.63
```

---
# NAT

NAT stands for Network Address Translation.
NAT translates private IP addresses to public IP addresses.
It allows devices on an internal network to communicate with external networks such as the Internet.

## How NAT Works

### Example:
```text
Private Device
192.168.1.10
      ↓
    Router
      ↓
Public IP
98.117.53.254
      ↓
  Internet
```

The router translates the private source IP into the public IP.

The external service sees the public IP rather than the device's private IP.

---

# Types of NAT

## The main types covered are:
- Static NAT
- Dynamic NAT
- PAT (Port Address Translation)
- Benefits of NAT

## NAT can:
- Conserve public IP addresses
- Simplify network design
- Simplify network management
- Improve network security
  
