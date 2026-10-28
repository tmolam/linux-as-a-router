# Linux as a Router

## Project Overview

This project demonstrates how to configure an Ubuntu Linux machine to route traffic between two separate internal networks and provide Internet access to both networks.

The virtual lab consists of three Ubuntu machines. One acts as the router, with three network interfaces: one connected to the Internet and two connected to separate internal networks.

## Lab Topology

The Ubuntu router connects both internal networks and forwards their traffic to the Internet.

![Linux router network topology](screenshots/01-network-topology.png)

## Technologies Used

- Ubuntu Linux
- Virtual machines
- IPv4 forwarding
- `iptables`
- NAT/masquerading
- `ping` and `curl` for connectivity testing

## Implementation

### 1. Network Configuration

Configured three network interfaces on the router, connecting it to the Internet and two separate internal networks.

### 2. IP Forwarding and Routing

Enabled IPv4 forwarding and configured firewall forwarding rules to allow traffic between the internal networks and the Internet.

### 3. NAT/Masquerading

Configured NAT/masquerading on the Internet-facing interface so the internal machines could access the Internet through the router.

## Testing and Evidence

### Inter-Network Connectivity

Used `ping` to verify communication between machines on the separate internal networks.

![Ping connectivity tests](screenshots/02-connectivity-tests.png)

### iptables Configuration

The following screenshot shows the forwarding and NAT rules configured in the lab.

![iptables configuration](screenshots/03-iptables-configuration.png)

### HTTP Connectivity

Used `curl` to test HTTP connectivity through the configured network.

![curl HTTP connectivity test](screenshots/04-http-connectivity-test.png)

## Key Learnings

- Configuring Linux network interfaces and IP addressing.
- Routing traffic between separate IP networks.
- Enabling IP forwarding and configuring NAT/masquerading.
- Using `iptables` to manage traffic forwarding.
- Troubleshooting connectivity with `ping` and `curl`.

## Disclaimer

This project was completed in a virtual lab environment for educational purposes. The configuration demonstrates basic routing and connectivity and is not intended as a production-ready network security design.
