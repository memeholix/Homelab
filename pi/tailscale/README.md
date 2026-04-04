# Tailscale

WireGuard-based VPN providing secure remote access to the homelab
from anywhere without opening ports on the router.

## Devices

| Device | Role |
|---|---|
| Raspberry Pi 5 | Homelab server |
| ThinkPad | Cybersecurity workstation |

## Use Cases

- SSH into Pi from anywhere using Tailscale IP
- Access Jellyfin, Pi-hole, Portainer remotely
- Secure access to homelab during relocation
- No port forwarding required on router

## Services Accessible Remotely

| Service | URL |
|---|---|
| Jellyfin | http://[tailscale-ip]:8096 |
| Pi-hole | http://[tailscale-ip]/admin |
| Portainer | https://[tailscale-ip]:9443 |
| SSH | ssh piserver@[tailscale-ip] |

## Notes

- Authenticated via GitHub account
- Free tier supports up to 100 devices
- Built on WireGuard protocol
- No open ports needed on home router
