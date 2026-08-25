# DNS

DNS stands for **Domain Name System**.

DNS translates domain names into IP addresses.

For example:

```text
google.com → IP address
```
This makes it easier for users and applications to access services without having to remember numerical IP addresses.

# Why DNS is Important

## DNS is essential for:
- Accessing websites
- Accessing network services
- Service availability
- Network configuration
- Network troubleshooting
- Managing infrastructure

DNS is particularly important for DevOps engineers because many services communicate using hostnames and domain names.

# DNS Components

## Name Servers
Name servers store DNS settings and configurations.

## They can be:
- Authoritative
- Recursive
- Zone Files

Zone files store information about a domain.
They contain DNS records organised in a readable format.

# DNS Records: 

DNS records are entries in a zone file containing specific information about a domain.

## A DNS record contains information such as:
- Record name
- TTL
- Class
- Type
- Data

# Common DNS Records:
| Record | Description                      |
| ------ | -------------------------------- |
| A      | Maps a domain to an IPv4 address |
| AAAA   | Maps a domain to an IPv6 address |
| CNAME  | Alias from one name to another   |
| MX     | Specifies the mail server        |
| NS     | Name server record               |
| PTR    | Pointer record                   |
| SOA    | Start of Authority               |
| SRV    | Service location                 |
| TXT    | Stores text information          |

# A Record
An A record maps a domain name to an IPv4 address.

## Example:
```text 
google.com → 216.58.204.79
```
# AAAA Record

An AAAA record maps a domain name to an IPv6 address.

## Example:
```text
google.com → 2a00:1450:4009:81d::200e
```

#CNAME Record

A CNAME record creates an alias from one domain name to another.

Example:
```text
www.google.com → google.com
```

CNAME records simplify DNS management.

# MX Record

An MX record specifies the mail server responsible for receiving email for a domain.

MX records also include a priority value.

# TXT Record

TXT records store text information for a domain.

## Common uses include:
- Domain verification
- SPF information
- Other metadata

# DNS Resolution

DNS resolution is the process of converting a domain name into an IP address.

## A simplified process:

User
  ↓
DNS Resolver
  ↓
Root Server
  ↓
TLD Server
  ↓
Authoritative Name Server
  ↓
IP Address

## Example: Resolving google.com
1. The user enters google.com.
2. The query is sent to a DNS resolver.
3. The resolver queries a root server.
4. The root server directs the resolver to the .com TLD server.
5. The .com TLD server directs the resolver to Google's authoritative name server.
6. The authoritative server provides the IP address.
7. The IP address is returned to the user.

# DNS Tools
## nslookup
nslookup is a basic DNS query tool.

```Bash
nslookup google.com
```

Syntax:
```Bash
nslookup [domain]
```
## dig

dig is a more advanced DNS query tool.

```Bash
dig google.com
```

Syntax:
```Bash
dig [domain]
```

## /etc/hosts

/etc/hosts is a local file on a Linux machine used to map domain names to IP addresses.

Format:
```text
IP_address domain_name
```
Example:
```text
127.0.0.1 example.com
```

Entries in /etc/hosts can take precedence over DNS for the domains defined in the file.

# Practical Examples
## Redirect a Domain to Localhost
To map a domain to the local machine:
```text
127.0.0.1 example.com
```
This causes "example.com" to resolve to the local machine.

# Custom Domain for Local Development

A custom local domain can be mapped to a local server IP.

Example:
```text
192.168.1.100 dev.local
```
This can be useful when developing and testing applications locally.
