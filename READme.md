# HOMELAB
 
A personal homelab built for learning network security, self-hosted services, and cybersecurity operations. Documents my hands-on experience building functional environments from scratch.
 
## HARDWARE
 
| Device | Specs | Roles |
| --- | --- | --- |
| Raspberry Pi 5 | 16GB RAM, 512GB NVMe | Server - Pi-hole, Jellyfin, Prometheus, Grafana, Homer |
| Lenovo ThinkPad | 8GB RAM, 256GB SSD | Homelab management + Wazuh SIEM |
| Lenovo Legion | Daily driver | Attack platform + dual boot Kali (coming soon) |
 
## NETWORK
 
* Pi-hole for network-wide DNS filtering and ad blocking
* UFW firewall on all devices
* Isolated VirtualBox host-only network for lab VMs
* Tailscale VPN for secure remote access
* Wazuh SIEM running on ThinkPad for 24/7 monitoring
## THINKPAD SETUP
 
* OS — Ubuntu Desktop 24.04
* OS hardening — UFW, fail2ban, auditd, SSH hardening
* Wazuh Manager + Indexer + Dashboard — full SIEM stack
* Homelab management platform — browser access to all service dashboards
## PI SETUP
 
* OS hardening — UFW, fail2ban, auditd, auto updates, SSH hardening
* Docker and Portainer for container management
* Pi-hole — network-wide DNS filtering with 831,745+ blocked domains
* Jellyfin — self-hosted media server with movies, shows, music and books
* Tailscale — secure remote access via WireGuard VPN
* Homer — homelab dashboard
* Prometheus + Node Exporter — metrics collection and storage
* Grafana — metrics visualization and dashboards
## GOALS
 
* Build hands-on experience with offensive and defensive security operations
* Practice attack/defense scenarios in an isolated lab environment
* Monitor network traffic and detect threats with a self-hosted SIEM
* Document everything for learning and portfolio purposes
