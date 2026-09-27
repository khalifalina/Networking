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

## Steps Taken

### 1. Domain Registration
- Purchased the domain **khals.co.uk** and connected it to Cloudflare for DNS management.

### 2. Launching the EC2 Instance
- Launched an **Ubuntu Server** EC2 instance (t3.micro, free-tier eligible) in the AWS Console.
- Created a new key pair for SSH access.
- Configured the security group to allow:
  - **SSH (port 22)** — restricted to my IP
  - **HTTP (port 80)** — open to all (0.0.0.0/0), required for the web page to be publicly reachable

### 3. Installing NGINX
Connected to the instance via SSH and installed NGINX:
```bash
sudo apt update
sudo apt install -y nginx
sudo systemctl enable nginx
sudo systemctl start nginx
```
Verified NGINX was running with `sudo systemctl status nginx`, and confirmed the default page loaded at the instance's public IP before configuring DNS.

### 4. Configuring DNS
- Added an **A record** in Cloudflare pointing `khals.co.uk` → EC2 public IPv4 address.
- Set the record to **DNS only** (not proxied), so the domain resolves directly to the EC2 instance rather than through Cloudflare's proxy — important for this assignment, since the goal is to demonstrate a direct IP-to-domain mapping.

### 5. Custom Landing Page
- Edited `/var/www/html/index.html` to replace the default NGINX page with a custom landing page including my name and links to my LinkedIn and GitHub.

## Testing & Results
- Confirmed DNS resolution using `nslookup khals.co.uk`, verifying it returned the EC2 instance's public IP.
- Visited `http://khals.co.uk` in a browser and confirmed the custom page loaded successfully.

## Challenges & Troubleshooting
- Initially edited the wrong file (`/usr/share/nginx/html/index.html`, the RHEL/Amazon Linux path) instead of the correct Ubuntu path (`/var/www/html/index.html`) — changes weren't reflected until I found the right file.
- The domain initially resolved to Cloudflare's proxy IPs instead of the EC2 IP, resolved by switching the A record from **Proxied** to **DNS only**.

## Screenshots

<img width="1632" height="916" alt="Screenshot_25-9-2026_16498_khals co uk" src="https://github.com/user-attachments/assets/413af211-d2fb-420e-877f-4764ce417f56" />

## Conclusion
This assignment brought together domain registration, EC2 provisioning, security group configuration, NGINX installation, and DNS management into one practical exercise — successfully making a self-hosted web page publicly accessible via a custom domain.
