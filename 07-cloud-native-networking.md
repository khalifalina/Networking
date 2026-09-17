# Cloud-Native Networking

## What is Cloud Networking?

Cloud networking refers to networking within cloud environments.

Networking is particularly important for DevOps because applications, services, containers and infrastructure need to communicate with each other.

---

# Key Cloud Networking Components

The course introduces:

- VPCs
- Subnets
- Gateways
- DNS
- Route tables
- Security groups
- Network ACLs
- Container networking

---

# VPC

VPC stands for **Virtual Private Cloud**.

A VPC provides a virtual network within a cloud environment.

A VPC can contain:

- Subnets
- Route tables
- Gateways
- Network security controls

---

# Subnets

Subnets are divisions of a VPC.

They allow a VPC to be separated into smaller network sections.

### Public Subnets

Public subnets are designed for resources that require connectivity to public networks.

### Private Subnets

Private subnets are designed for resources that should not be directly accessible from the public Internet.

---

# AWS Route 53

Route 53 is a managed DNS service provided by AWS.

### Features

Route 53 supports:

- DNS
- Health checks
- Load balancing
- Integration with other AWS services

### Setting Up Route 53

A basic setup involves:

1. Creating a hosted zone
2. Configuring DNS records

---

# AWS Route Tables

Route tables determine how traffic is routed within AWS networking.

A route contains information such as:

- Destination
- Target
- CIDR block

Route tables can be associated with subnets.

---

# Container Networking

Containers need networking to communicate with other containers, hosts and external networks.

---

# Docker Networking

The course covers:

- Bridge networks
- Host networks
- Overlay networks

Docker networks can be configured to control how containers communicate.

---

# Kubernetes Networking

Kubernetes provides networking for pods and services.

Important concepts include:

- Pod networking
- Services
- CNI plugins

---

# Security Groups

Security Groups provide **state-based firewall rules**.

They can be configured with:

- Inbound rules
- Outbound rules

---

# Network ACLs

Network ACLs (NACLs) provide **stateless filtering**.

They can be configured with rules and associated with subnets.

---

# Security Groups vs NACLs

| Feature | Security Groups | NACLs |
|---|---|---|
| Filtering | State-based | Stateless |
| Rules | Inbound and outbound | Network traffic rules |
| Association | Resources | Subnets |

---

# Cloud Networking and DevOps

Cloud networking knowledge is important for DevOps engineers working with:

- Cloud infrastructure
- VPCs
- Subnets
- DNS
- Routing
- Containers
- Kubernetes
- Network security

  
