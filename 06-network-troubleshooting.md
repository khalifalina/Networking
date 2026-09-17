# Network Troubleshooting

## What is Network Troubleshooting?

Network troubleshooting is the process of identifying and resolving network problems.

### Why Troubleshoot?

Network troubleshooting helps to:

- Identify problems
- Fix network issues
- Ensure smooth operation
- Minimise downtime

---

# Common Network Issues

Common problems include:

- DNS resolution failures
- Connectivity loss
- Slow network performance
- IP address conflicts

---

# Identifying Problems

A basic troubleshooting process involves:

1. Observe the problem.
2. Gather information.
3. Check the network configuration.
4. Use network monitoring and diagnostic tools.
5. Test connectivity.
6. Identify the cause.
7. Apply a solution.
8. Test again.

---

# Example: Connectivity Loss

### Symptom

Devices cannot access the network.

### Initial checks

Check:

- Physical connections
- Network configuration
- IP configuration
- Connectivity

Then test the connection using:

```bash
ping <destination>
```

---

# Network Debugging Tools
## Ping

ping tests connectivity to another device or host.

### Example:
```bash
ping google.com
```
### syntax 
```bash
ping [IP address or domain]
```

--- 

## Traceroute

traceroute tracks the path taken to a destination.

### Linux/macOS:
```bash
traceroute google.com
```
### Windows:
```cmd
tracert google.com
```
### Syntax:
```bash
traceroute [domain]
```
Traceroute can help identify where along the network path a problem may be occurring.

---

# Troubleshooting a Website That Cannot Be Reached

A systematic approach could be:
Can I reach the network?
        ↓
      ping
        ↓
Does DNS resolve the domain?
        ↓
    nslookup
        ↓
Where does the network path go?
        ↓
    traceroute


The goal is to gather evidence and isolate the problem rather than immediately changing configurations.

---

