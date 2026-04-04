#HOMELAB

A personal homelab built for learning network security, self-hosted services, and cybersecurity operations. Documents my hands-on experience building functional environments from scratch.

##HARDWARE

| Device | Specs | Roles
|---|---|---|
|Raspberry Pi 5 | 16GB RAM, 1 TB NVMe (expanding to RAID 1 2x2TB) | Server - Pi-hole, Jellyfin, Wazuh, Grafana |
|Lenovo Thinkpad | 8GB RAM | Cybersecurity platform - redteam tools, VM labs | 

##NETWORK

 - Pi-hole for network-wide DNS filtering and ad blocking
 - UFW firewall on all devices
 - Isolated VirtualBox host-only network for lab VMs
 - Wazuh SIEM for centralized logging and threat detection

##THINKPAD SETUP
 - OS hardening - UFW, fail2ban, auditd
 - Red team toolkit - Metasploit, Nmap, Burp Suite, Wireshark, and more
 - VirtualBox Lab with Kali, Metaploitable 2, REMnux, Windows 11
 - Pi-hole Docker instance (temporary during Pi migration)

##PI SETUP
- OS hardening — UFW, fail2ban, auditd, auto updates, SSH hardening
- Docker and Portainer for container management
- Pi-hole — network-wide DNS filtering with 831,745+ blocked domains
- Jellyfin — self-hosted media server with movies, shows, music and books
- Tailscale — secure remote access via WireGuard VPN
- Wazuh SIEM — coming soon
- Prometheus + Grafana — coming soon

##GOALS
 - Build hands-on experience with offensive and defensive security operations
 - Practice attack/defense scenarios in an isolated lab environment
 - Monitor network traffic and detect threats with a self-hosted SIEM
 - Document everything for learning and portfolio purposes


