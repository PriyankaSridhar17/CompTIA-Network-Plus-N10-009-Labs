# Lab 01 — Basic Network Connectivity and Troubleshooting
## Objective

Practice fundamental network troubleshooting commands to inspect IP configuration, verify local and external connectivity, test DNS resolution, and trace the network path to a remote destination.

## Lab Environment

- Operating System: Windows 11
- Tool: Windows Command Prompt
- Connection Type: Wi-Fi
- Protocols: TCP/IP, ICMP, DNS

## Commands and Results

| Command | Purpose | Result |
|---|---|---|
| `ipconfig /all` | Identify IP configuration, gateway, and DNS settings | Successful |
| `ping 127.0.0.1` | Test the local TCP/IP stack | 0% packet loss |
| `ping 192.168.0.1` | Verify default gateway connectivity | 0% packet loss |
| `ping 8.8.8.8` | Test connectivity to an external IP address | 0% packet loss, 16 ms average |
| `nslookup example.com` | Test DNS name resolution | Successful after an initial timeout |
| `nslookup example.com 8.8.8.8` | Verify DNS resolution using Google Public DNS | Successful |
| `tracert example.com` | Trace the route to a remote destination | Destination reached in 11 hops |

## Troubleshooting Observations

### 1. IP Configuration

Used `ipconfig /all` to identify the active Wi-Fi adapter, IPv4 address, subnet mask, default gateway, and DNS server.

### 2. Local Connectivity

Verified that the TCP/IP loopback interface responded successfully and that the default gateway was reachable.

### 3. External Connectivity

Successfully pinged Google's public DNS IP address (`8.8.8.8`) with 0% packet loss.

### 4. DNS Troubleshooting

Observed an initial DNS request timeout when querying the router's configured DNS service.

Repeated the lookup using Google Public DNS (`8.8.8.8`) and successfully resolved the domain name.

### 5. Route Tracing

Used `tracert` to examine the network path to `example.com`.

The destination was reached in 11 hops. Some intermediate probes did not receive responses, but the trace completed successfully.

## Key Learning Outcomes

- Understood how IP addresses identify devices on a network.
- Learned the purpose of a subnet mask and default gateway.
- Practiced testing local and external connectivity.
- Learned how DNS resolves domain names.
- Understood how traceroute helps investigate network paths.
- Practiced a structured approach to basic network troubleshooting.

## Conclusion

Successfully completed a foundational network connectivity and troubleshooting lab using Windows Command Prompt.

This lab reinforced basic TCP/IP concepts and introduced practical diagnostic techniques relevant to Network Support, NOC, and IT Infrastructure roles.
