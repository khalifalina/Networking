# Core Assignment — Domain + EC2 + DNS

## What is Amazon EC2?

**Amazon EC2 (Elastic Compute Cloud)** is an AWS service that provides virtual servers, known as **instances**, that can be used to run applications and services in the cloud. Instead of needing to own and maintain physical hardware, users can create and manage virtual machines on AWS.

For this assignment, an EC2 instance acts as the **server** hosting the NGINX web server. The instance is assigned a public IPv4 address, allowing it to be reached over the Internet.

## Why is EC2 Relevant to DevOps?

EC2 is highly relevant to DevOps because it provides an environment where applications and services can be deployed, configured, managed, and tested without requiring physical infrastructure.

It also connects several of the networking concepts covered in this course. In this assignment, I will use:

* **IP addressing** — using the EC2 instance's public IPv4 address
* **Ports** — allowing HTTP traffic through port 80
* **DNS** — connecting a domain name to the EC2 instance using an A record
* **Routing** — allowing traffic to reach the EC2 instance over the Internet
* **Hosting** — deploying NGINX on the EC2 instance and serving a web page

The assignment therefore brings these concepts together into a practical example of deploying a web service in a cloud environment.

## Assignment Objective

The objective is to purchase a domain, deploy NGINX on an EC2 instance, configure DNS, and make the NGINX page accessible through the chosen domain.

The overall flow is:

```text
Domain Name
     ↓
    DNS
     ↓
A Record → EC2 Public IPv4 Address
     ↓
EC2 Instance
     ↓
Port 80 (HTTP)
     ↓
NGINX
     ↓
Web Page
```
