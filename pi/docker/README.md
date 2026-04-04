# Docker & Portainer

Docker container runtime and Portainer management UI deployed on Raspberry Pi 5.

## Docker

Installed via apt. All services on the Pi run as Docker containers for
easy management, portability, and clean removal.

## Portainer

Web-based Docker management interface. Allows managing all containers,
images, volumes and networks from a browser without needing the command line.

| Setting | Value |
|---|---|
| Web UI | https://192.168.0.23:9443 |
| Restart policy | Unless stopped |

## Containers Running

| Container | Purpose | Port |
|---|---|---|
| Portainer | Docker management UI | 9443 |
| Pi-hole | Network DNS and ad blocking | 53, 80 |
| Jellyfin | Media server | 8096 |

## Notes

- Added piserver user to docker group for non-root container management
- All containers set to restart unless-stopped for automatic recovery on reboot
- Persistent volumes used for all containers so data survives updates
