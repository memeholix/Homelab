# Network Configuration

Documentation of home network setup including DNS, firewall, and topology.

## Hardware

| Device | Model | Role |
|---|---|---|
| Router | TP-Link Archer BE6100 | Gateway, DHCP, DNS forwarding |
| Server | Raspberry Pi 5 | Pi-hole, Jellyfin, Prometheus, Grafana, Homer |
| Workstation | Lenovo ThinkPad | Cybersecurity platform |

## Network Topology

| Device | IP | Role |
|---|---|---|
| Router | 192.168.0.1 | Gateway |
| Raspberry Pi 5 | 192.168.0.23 (static) | Server |
| ThinkPad | 192.168.0.231 | Workstation |

## DNS Configuration

All DNS traffic routes through Pi-hole for network-wide ad and malware blocking.

| Setting | Value |
|---|---|
| Primary DNS | 192.168.0.23 (Raspberry Pi — Pi-hole) |
| Secondary DNS | 208.67.222.222 (OpenDNS — fallback) |

## Firewall

UFW configured on all Linux devices with the following default policy:

| Direction | Policy |
|---|---|
| Incoming | Deny |
| Outgoing | Allow |

SSH allowed inbound on all devices for remote management.

## VirtualBox Lab Network

Isolated host-only network for security lab VMs.
No lab traffic can reach the home network or internet.

| Setting | Value |
|---|---|
| Interface | vboxnet0 |
| Subnet | 192.168.56.0/24 |
| Host IP | 192.168.56.1 |
| DHCP Range | 192.168.56.101 — 192.168.56.200 |

## Planned Improvements

- Configure Wazuh to monitor network traffic
